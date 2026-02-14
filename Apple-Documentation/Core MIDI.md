# Core MIDI Documentation

Source: https://sosumi.ai/documentation/coremidi

---
title: Core MIDI
source: https://developer.apple.com/documentation/coremidi
timestamp: 2026-02-13T18:55:31.849Z
---

## Services

- [MIDI Services](/documentation/coremidi/midi-services)

### MIDI object configuration

- [func MIDIObjectFindByUniqueID(MIDIUniqueID, UnsafeMutablePointer<MIDIObjectRef>?, UnsafeMutablePointer<MIDIObjectType>?) -> OSStatus](/documentation/coremidi/midiobjectfindbyuniqueid(_:_:_:))

#### Parameter Types

- [MIDIUniqueID](/documentation/coremidi/midiuniqueid)
- [var kMIDIInvalidUniqueID: MIDIUniqueID](/documentation/coremidi/kmidiinvaliduniqueid)
- [MIDIObjectType](/documentation/coremidi/midiobjecttype)

##### Object Types

- [case other](/documentation/coremidi/midiobjecttype/other)
- [case device](/documentation/coremidi/midiobjecttype/device)
- [case entity](/documentation/coremidi/midiobjecttype/entity)
- [case source](/documentation/coremidi/midiobjecttype/source)
- [case destination](/documentation/coremidi/midiobjecttype/destination)
- [case externalDevice](/documentation/coremidi/midiobjecttype/externaldevice)
- [case externalEntity](/documentation/coremidi/midiobjecttype/externalentity)
- [case externalSource](/documentation/coremidi/midiobjecttype/externalsource)
- [case externalDestination](/documentation/coremidi/midiobjecttype/externaldestination)
- [let kMIDIObjectType_ExternalMask: MIDIObjectType](/documentation/coremidi/kmidiobjecttype_externalmask)

##### Initializers

- [init?(rawValue: Int32)](/documentation/coremidi/midiobjecttype/init(rawvalue:))
- [MIDIObjectRef](/documentation/coremidi/midiobjectref)
- [MIDI Object Properties](/documentation/coremidi/midi-object-properties)

#### Identification

- [let kMIDIPropertyName: CFString](/documentation/coremidi/kmidipropertyname)
- [let kMIDIPropertyModel: CFString](/documentation/coremidi/kmidipropertymodel)
- [let kMIDIPropertyManufacturer: CFString](/documentation/coremidi/kmidipropertymanufacturer)
- [let kMIDIPropertyUniqueID: CFString](/documentation/coremidi/kmidipropertyuniqueid)
- [let kMIDIPropertyDeviceID: CFString](/documentation/coremidi/kmidipropertydeviceid)

#### Capabilities

- [let kMIDIPropertySupportsMMC: CFString](/documentation/coremidi/kmidipropertysupportsmmc)
- [let kMIDIPropertySupportsGeneralMIDI: CFString](/documentation/coremidi/kmidipropertysupportsgeneralmidi)
- [let kMIDIPropertySupportsShowControl: CFString](/documentation/coremidi/kmidipropertysupportsshowcontrol)

#### Configuration

- [let kMIDIPropertyNameConfigurationDictionary: CFString](/documentation/coremidi/kmidipropertynameconfigurationdictionary)
- [let kMIDIPropertyMaxSysExSpeed: CFString](/documentation/coremidi/kmidipropertymaxsysexspeed)
- [let kMIDIPropertyDriverDeviceEditorApp: CFString](/documentation/coremidi/kmidipropertydriverdeviceeditorapp)
- [let kMIDIPropertyNameConfiguration: CFString](/documentation/coremidi/kmidipropertynameconfiguration)

#### Presentation

- [let kMIDIPropertyImage: CFString](/documentation/coremidi/kmidipropertyimage)
- [let kMIDIPropertyDisplayName: CFString](/documentation/coremidi/kmidipropertydisplayname)

#### Audio

- [let kMIDIPropertyPanDisruptsStereo: CFString](/documentation/coremidi/kmidipropertypandisruptsstereo)

#### Protocols

- [let kMIDIPropertyProtocolID: CFString](/documentation/coremidi/kmidipropertyprotocolid)

#### Timing

- [let kMIDIPropertyTransmitsMTC: CFString](/documentation/coremidi/kmidipropertytransmitsmtc)
- [let kMIDIPropertyReceivesMTC: CFString](/documentation/coremidi/kmidipropertyreceivesmtc)
- [let kMIDIPropertyTransmitsClock: CFString](/documentation/coremidi/kmidipropertytransmitsclock)
- [let kMIDIPropertyReceivesClock: CFString](/documentation/coremidi/kmidipropertyreceivesclock)
- [let kMIDIPropertyAdvanceScheduleTimeMuSec: CFString](/documentation/coremidi/kmidipropertyadvancescheduletimemusec)

#### Roles

- [let kMIDIPropertyIsMixer: CFString](/documentation/coremidi/kmidipropertyismixer)
- [let kMIDIPropertyIsSampler: CFString](/documentation/coremidi/kmidipropertyissampler)
- [let kMIDIPropertyIsEffectUnit: CFString](/documentation/coremidi/kmidipropertyiseffectunit)
- [let kMIDIPropertyIsDrumMachine: CFString](/documentation/coremidi/kmidipropertyisdrummachine)

#### Status

- [let kMIDIPropertyOffline: CFString](/documentation/coremidi/kmidipropertyoffline)
- [let kMIDIPropertyPrivate: CFString](/documentation/coremidi/kmidipropertyprivate)

#### Drivers

- [let kMIDIPropertyDriverOwner: CFString](/documentation/coremidi/kmidipropertydriverowner)
- [let kMIDIPropertyDriverVersion: CFString](/documentation/coremidi/kmidipropertydriverversion)

#### Connections

- [let kMIDIPropertyCanRoute: CFString](/documentation/coremidi/kmidipropertycanroute)
- [let kMIDIPropertyIsBroadcast: CFString](/documentation/coremidi/kmidipropertyisbroadcast)
- [let kMIDIPropertyConnectionUniqueID: CFString](/documentation/coremidi/kmidipropertyconnectionuniqueid)
- [let kMIDIPropertyIsEmbeddedEntity: CFString](/documentation/coremidi/kmidipropertyisembeddedentity)
- [let kMIDIPropertySingleRealtimeEntity: CFString](/documentation/coremidi/kmidipropertysinglerealtimeentity)

#### Channels

- [let kMIDIPropertyReceiveChannels: CFString](/documentation/coremidi/kmidipropertyreceivechannels)
- [let kMIDIPropertyTransmitChannels: CFString](/documentation/coremidi/kmidipropertytransmitchannels)
- [let kMIDIPropertyMaxReceiveChannels: CFString](/documentation/coremidi/kmidipropertymaxreceivechannels)
- [let kMIDIPropertyMaxTransmitChannels: CFString](/documentation/coremidi/kmidipropertymaxtransmitchannels)

#### Banks

- [let kMIDIPropertyReceivesBankSelectLSB: CFString](/documentation/coremidi/kmidipropertyreceivesbankselectlsb)
- [let kMIDIPropertyReceivesBankSelectMSB: CFString](/documentation/coremidi/kmidipropertyreceivesbankselectmsb)
- [let kMIDIPropertyTransmitsBankSelectLSB: CFString](/documentation/coremidi/kmidipropertytransmitsbankselectlsb)
- [let kMIDIPropertyTransmitsBankSelectMSB: CFString](/documentation/coremidi/kmidipropertytransmitsbankselectmsb)

#### Notes

- [let kMIDIPropertyReceivesNotes: CFString](/documentation/coremidi/kmidipropertyreceivesnotes)
- [let kMIDIPropertyTransmitsNotes: CFString](/documentation/coremidi/kmidipropertytransmitsnotes)

#### Program Changes

- [let kMIDIPropertyReceivesProgramChanges: CFString](/documentation/coremidi/kmidipropertyreceivesprogramchanges)
- [let kMIDIPropertyTransmitsProgramChanges: CFString](/documentation/coremidi/kmidipropertytransmitsprogramchanges)

#### Property Accessors

- [func MIDIObjectGetProperties(MIDIObjectRef, UnsafeMutablePointer<Unmanaged<CFPropertyList>?>, Bool) -> OSStatus](/documentation/coremidi/midiobjectgetproperties(_:_:_:))
- [func MIDIObjectRemoveProperty(MIDIObjectRef, CFString) -> OSStatus](/documentation/coremidi/midiobjectremoveproperty(_:_:))
- [func MIDIObjectGetStringProperty(MIDIObjectRef, CFString, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/coremidi/midiobjectgetstringproperty(_:_:_:))
- [func MIDIObjectSetStringProperty(MIDIObjectRef, CFString, CFString) -> OSStatus](/documentation/coremidi/midiobjectsetstringproperty(_:_:_:))
- [func MIDIObjectGetIntegerProperty(MIDIObjectRef, CFString, UnsafeMutablePointer<Int32>) -> OSStatus](/documentation/coremidi/midiobjectgetintegerproperty(_:_:_:))
- [func MIDIObjectSetIntegerProperty(MIDIObjectRef, CFString, Int32) -> OSStatus](/documentation/coremidi/midiobjectsetintegerproperty(_:_:_:))
- [func MIDIObjectGetDataProperty(MIDIObjectRef, CFString, UnsafeMutablePointer<Unmanaged<CFData>?>) -> OSStatus](/documentation/coremidi/midiobjectgetdataproperty(_:_:_:))
- [func MIDIObjectSetDataProperty(MIDIObjectRef, CFString, CFData) -> OSStatus](/documentation/coremidi/midiobjectsetdataproperty(_:_:_:))
- [func MIDIObjectGetDictionaryProperty(MIDIObjectRef, CFString, UnsafeMutablePointer<Unmanaged<CFDictionary>?>) -> OSStatus](/documentation/coremidi/midiobjectgetdictionaryproperty(_:_:_:))
- [func MIDIObjectSetDictionaryProperty(MIDIObjectRef, CFString, CFDictionary) -> OSStatus](/documentation/coremidi/midiobjectsetdictionaryproperty(_:_:_:))

#### Notifications

- [MIDIObjectAddRemoveNotification](/documentation/coremidi/midiobjectaddremovenotification)

##### Inspecting the Notification

- [var messageID: MIDINotificationMessageID](/documentation/coremidi/midiobjectaddremovenotification/messageid)
- [var messageSize: UInt32](/documentation/coremidi/midiobjectaddremovenotification/messagesize)
- [var parent: MIDIObjectRef](/documentation/coremidi/midiobjectaddremovenotification/parent)
- [var parentType: MIDIObjectType](/documentation/coremidi/midiobjectaddremovenotification/parenttype)
- [var child: MIDIObjectRef](/documentation/coremidi/midiobjectaddremovenotification/child)
- [var childType: MIDIObjectType](/documentation/coremidi/midiobjectaddremovenotification/childtype)

##### Initializers

- [init()](/documentation/coremidi/midiobjectaddremovenotification/init())
- [init(messageID: MIDINotificationMessageID, messageSize: UInt32, parent: MIDIObjectRef, parentType: MIDIObjectType, child: MIDIObjectRef, childType: MIDIObjectType)](/documentation/coremidi/midiobjectaddremovenotification/init(messageid:messagesize:parent:parenttype:child:childtype:))
- [MIDIObjectPropertyChangeNotification](/documentation/coremidi/midiobjectpropertychangenotification)

##### Inspecting the Notification

- [var messageID: MIDINotificationMessageID](/documentation/coremidi/midiobjectpropertychangenotification/messageid)
- [var messageSize: UInt32](/documentation/coremidi/midiobjectpropertychangenotification/messagesize)
- [var object: MIDIObjectRef](/documentation/coremidi/midiobjectpropertychangenotification/object)
- [var objectType: MIDIObjectType](/documentation/coremidi/midiobjectpropertychangenotification/objecttype)
- [var propertyName: Unmanaged<CFString>](/documentation/coremidi/midiobjectpropertychangenotification/propertyname)

##### Initializers

- [init(messageID: MIDINotificationMessageID, messageSize: UInt32, object: MIDIObjectRef, objectType: MIDIObjectType, propertyName: Unmanaged<CFString>)](/documentation/coremidi/midiobjectpropertychangenotification/init(messageid:messagesize:object:objecttype:propertyname:))

### Client management

- [Incorporating MIDI 2 into your apps](/documentation/coremidi/incorporating-midi-2-into-your-apps)
- [func MIDIClientCreate(CFString, MIDINotifyProc?, UnsafeMutableRawPointer?, UnsafeMutablePointer<MIDIClientRef>) -> OSStatus](/documentation/coremidi/midiclientcreate(_:_:_:_:))

#### Callbacks

- [MIDINotifyProc](/documentation/coremidi/midinotifyproc)
- [MIDINotification](/documentation/coremidi/midinotification)

##### Inspecting the Notification

- [MIDINotificationMessageID](/documentation/coremidi/midinotificationmessageid)

###### Change Types

- [case msgSetupChanged](/documentation/coremidi/midinotificationmessageid/msgsetupchanged)
- [case msgObjectAdded](/documentation/coremidi/midinotificationmessageid/msgobjectadded)
- [case msgObjectRemoved](/documentation/coremidi/midinotificationmessageid/msgobjectremoved)
- [case msgPropertyChanged](/documentation/coremidi/midinotificationmessageid/msgpropertychanged)
- [case msgThruConnectionsChanged](/documentation/coremidi/midinotificationmessageid/msgthruconnectionschanged)
- [case msgSerialPortOwnerChanged](/documentation/coremidi/midinotificationmessageid/msgserialportownerchanged)
- [case msgIOError](/documentation/coremidi/midinotificationmessageid/msgioerror)

###### Enumeration Cases

- [case msgInternalStart](/documentation/coremidi/midinotificationmessageid/msginternalstart)

###### Initializers

- [init?(rawValue: Int32)](/documentation/coremidi/midinotificationmessageid/init(rawvalue:))
- [var messageID: MIDINotificationMessageID](/documentation/coremidi/midinotification/messageid)
- [var messageSize: UInt32](/documentation/coremidi/midinotification/messagesize)

##### Initializers

- [init()](/documentation/coremidi/midinotification/init())
- [init(messageID: MIDINotificationMessageID, messageSize: UInt32)](/documentation/coremidi/midinotification/init(messageid:messagesize:))
- [func MIDIClientCreateWithBlock(CFString, UnsafeMutablePointer<MIDIClientRef>, MIDINotifyBlock?) -> OSStatus](/documentation/coremidi/midiclientcreatewithblock(_:_:_:))

#### Callbacks

- [MIDINotifyBlock](/documentation/coremidi/midinotifyblock)
- [MIDINotification](/documentation/coremidi/midinotification)

##### Inspecting the Notification

- [MIDINotificationMessageID](/documentation/coremidi/midinotificationmessageid)

###### Change Types

- [case msgSetupChanged](/documentation/coremidi/midinotificationmessageid/msgsetupchanged)
- [case msgObjectAdded](/documentation/coremidi/midinotificationmessageid/msgobjectadded)
- [case msgObjectRemoved](/documentation/coremidi/midinotificationmessageid/msgobjectremoved)
- [case msgPropertyChanged](/documentation/coremidi/midinotificationmessageid/msgpropertychanged)
- [case msgThruConnectionsChanged](/documentation/coremidi/midinotificationmessageid/msgthruconnectionschanged)
- [case msgSerialPortOwnerChanged](/documentation/coremidi/midinotificationmessageid/msgserialportownerchanged)
- [case msgIOError](/documentation/coremidi/midinotificationmessageid/msgioerror)

###### Enumeration Cases

- [case msgInternalStart](/documentation/coremidi/midinotificationmessageid/msginternalstart)

###### Initializers

- [init?(rawValue: Int32)](/documentation/coremidi/midinotificationmessageid/init(rawvalue:))
- [var messageID: MIDINotificationMessageID](/documentation/coremidi/midinotification/messageid)
- [var messageSize: UInt32](/documentation/coremidi/midinotification/messagesize)

##### Initializers

- [init()](/documentation/coremidi/midinotification/init())
- [init(messageID: MIDINotificationMessageID, messageSize: UInt32)](/documentation/coremidi/midinotification/init(messageid:messagesize:))
- [func MIDIClientDispose(MIDIClientRef) -> OSStatus](/documentation/coremidi/midiclientdispose(_:))
- [MIDIClientRef](/documentation/coremidi/midiclientref)

### Device lookup

- [func MIDIGetNumberOfDevices() -> Int](/documentation/coremidi/midigetnumberofdevices())
- [func MIDIGetDevice(Int) -> MIDIDeviceRef](/documentation/coremidi/midigetdevice(_:))
- [func MIDIGetNumberOfExternalDevices() -> Int](/documentation/coremidi/midigetnumberofexternaldevices())
- [func MIDIGetExternalDevice(Int) -> MIDIDeviceRef](/documentation/coremidi/midigetexternaldevice(_:))
- [func MIDIDeviceGetNumberOfEntities(MIDIDeviceRef) -> Int](/documentation/coremidi/mididevicegetnumberofentities(_:))
- [func MIDIDeviceGetEntity(MIDIDeviceRef, Int) -> MIDIEntityRef](/documentation/coremidi/mididevicegetentity(_:_:))
- [MIDIDeviceRef](/documentation/coremidi/midideviceref)

### Entity lookup

- [func MIDIEntityGetDevice(MIDIEntityRef, UnsafeMutablePointer<MIDIDeviceRef>?) -> OSStatus](/documentation/coremidi/midientitygetdevice(_:_:))
- [func MIDIEntityGetNumberOfSources(MIDIEntityRef) -> Int](/documentation/coremidi/midientitygetnumberofsources(_:))
- [func MIDIEntityGetSource(MIDIEntityRef, Int) -> MIDIEndpointRef](/documentation/coremidi/midientitygetsource(_:_:))
- [func MIDIEntityGetNumberOfDestinations(MIDIEntityRef) -> Int](/documentation/coremidi/midientitygetnumberofdestinations(_:))
- [func MIDIEntityGetDestination(MIDIEntityRef, Int) -> MIDIEndpointRef](/documentation/coremidi/midientitygetdestination(_:_:))
- [MIDIEntityRef](/documentation/coremidi/midientityref)

### Port management

- [func MIDIInputPortCreateWithProtocol(MIDIClientRef, CFString, MIDIProtocolID, UnsafeMutablePointer<MIDIPortRef>, MIDIReceiveBlock) -> OSStatus](/documentation/coremidi/midiinputportcreatewithprotocol(_:_:_:_:_:))
- [func MIDIOutputPortCreate(MIDIClientRef, CFString, UnsafeMutablePointer<MIDIPortRef>) -> OSStatus](/documentation/coremidi/midioutputportcreate(_:_:_:))
- [func MIDIPortDispose(MIDIPortRef) -> OSStatus](/documentation/coremidi/midiportdispose(_:))
- [func MIDIPortConnectSource(MIDIPortRef, MIDIEndpointRef, UnsafeMutableRawPointer?) -> OSStatus](/documentation/coremidi/midiportconnectsource(_:_:_:))
- [func MIDIPortDisconnectSource(MIDIPortRef, MIDIEndpointRef) -> OSStatus](/documentation/coremidi/midiportdisconnectsource(_:_:))
- [MIDIPortRef](/documentation/coremidi/midiportref)
- [MIDIReceiveBlock](/documentation/coremidi/midireceiveblock)

### Endpoint management

- [func MIDIEndpointDispose(MIDIEndpointRef) -> OSStatus](/documentation/coremidi/midiendpointdispose(_:))
- [func MIDIEndpointGetEntity(MIDIEndpointRef, UnsafeMutablePointer<MIDIEntityRef>?) -> OSStatus](/documentation/coremidi/midiendpointgetentity(_:_:))
- [func MIDIEndpointGetRefCons(MIDIEndpointRef, UnsafeMutablePointer<UnsafeMutableRawPointer>?, UnsafeMutablePointer<UnsafeMutableRawPointer>?) -> OSStatus](/documentation/coremidi/midiendpointgetrefcons(_:_:_:))
- [func MIDIEndpointSetRefCons(MIDIEndpointRef, UnsafeMutableRawPointer?, UnsafeMutableRawPointer?) -> OSStatus](/documentation/coremidi/midiendpointsetrefcons(_:_:_:))
- [func MIDISourceCreateWithProtocol(MIDIClientRef, CFString, MIDIProtocolID, UnsafeMutablePointer<MIDIEndpointRef>) -> OSStatus](/documentation/coremidi/midisourcecreatewithprotocol(_:_:_:_:))
- [func MIDIGetSource(Int) -> MIDIEndpointRef](/documentation/coremidi/midigetsource(_:))
- [func MIDIGetNumberOfSources() -> Int](/documentation/coremidi/midigetnumberofsources())
- [func MIDIDestinationCreateWithProtocol(MIDIClientRef, CFString, MIDIProtocolID, UnsafeMutablePointer<MIDIEndpointRef>, MIDIReceiveBlock) -> OSStatus](/documentation/coremidi/mididestinationcreatewithprotocol(_:_:_:_:_:))
- [func MIDIGetDestination(Int) -> MIDIEndpointRef](/documentation/coremidi/midigetdestination(_:))
- [func MIDIGetNumberOfDestinations() -> Int](/documentation/coremidi/midigetnumberofdestinations())
- [MIDIEndpointRef](/documentation/coremidi/midiendpointref)

### Event list management

- [func MIDIEventListInit(UnsafeMutablePointer<MIDIEventList>, MIDIProtocolID) -> UnsafeMutablePointer<MIDIEventPacket>](/documentation/coremidi/midieventlistinit(_:_:))
- [func MIDIEventListAdd(UnsafeMutablePointer<MIDIEventList>, Int, UnsafeMutablePointer<MIDIEventPacket>, MIDITimeStamp, Int, UnsafePointer<UInt32>) -> UnsafeMutablePointer<MIDIEventPacket>](/documentation/coremidi/midieventlistadd(_:_:_:_:_:_:))
- [func MIDIEventPacketNext(UnsafePointer<MIDIEventPacket>) -> UnsafeMutablePointer<MIDIEventPacket>](/documentation/coremidi/midieventpacketnext(_:))
- [func MIDISendEventList(MIDIPortRef, MIDIEndpointRef, UnsafePointer<MIDIEventList>) -> OSStatus](/documentation/coremidi/midisendeventlist(_:_:_:))
- [func MIDIReceivedEventList(MIDIEndpointRef, UnsafePointer<MIDIEventList>) -> OSStatus](/documentation/coremidi/midireceivedeventlist(_:_:))
- [MIDIEventList](/documentation/coremidi/midieventlist)

#### Configuring an Event List

- [var `protocol`: MIDIProtocolID](/documentation/coremidi/midieventlist/protocol)
- [var numPackets: UInt32](/documentation/coremidi/midieventlist/numpackets)
- [var packet: MIDIEventPacket](/documentation/coremidi/midieventlist/packet)

#### Classes

- [MIDIEventList.Builder](/documentation/coremidi/midieventlist/builder)

##### Initializers

- [init(inProtocol: MIDIProtocolID, wordSize: Int)](/documentation/coremidi/midieventlist/builder/init(inprotocol:wordsize:))

##### Instance Properties

- [var count: Int](/documentation/coremidi/midieventlist/builder/count)

##### Instance Methods

- [func append(timestamp: MIDITimeStamp, words: [UInt32]) -> UnsafePointer<MIDIEventPacket>?](/documentation/coremidi/midieventlist/builder/append(timestamp:words:))
- [func clear()](/documentation/coremidi/midieventlist/builder/clear())
- [func withUnsafeMutableMIDIEventListPointer<Result>((inout UnsafeMutableMIDIEventListPointer) -> Result) -> Result](/documentation/coremidi/midieventlist/builder/withunsafemutablemidieventlistpointer(_:))
- [func withUnsafePointer<Result>((UnsafePointer<MIDIEventList>) -> Result) -> Result](/documentation/coremidi/midieventlist/builder/withunsafepointer(_:))

#### Structures

- [MIDIEventList.UnsafeSequence](/documentation/coremidi/midieventlist/unsafesequence)

##### Instance Properties

- [var count: Int](/documentation/coremidi/midieventlist/unsafesequence/count)

#### Initializers

- [init()](/documentation/coremidi/midieventlist/init())
- [init(protocol: MIDIProtocolID, numPackets: UInt32, packet: MIDIEventPacket)](/documentation/coremidi/midieventlist/init(protocol:numpackets:packet:))

#### Type Methods

- [static func sizeInBytes(pktList: UnsafePointer<MIDIEventList>) -> Int](/documentation/coremidi/midieventlist/sizeinbytes(pktlist:))
- [MIDIEventPacket](/documentation/coremidi/midieventpacket)

#### Configuring an Event Packet

- [var timeStamp: MIDITimeStamp](/documentation/coremidi/midieventpacket/timestamp)
- [var wordCount: UInt32](/documentation/coremidi/midieventpacket/wordcount)
- [var words: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32)](/documentation/coremidi/midieventpacket/words)

#### Classes

- [MIDIEventPacket.Builder](/documentation/coremidi/midieventpacket/builder)

##### Initializers

- [init(maximumNumberMIDIWords: Int)](/documentation/coremidi/midieventpacket/builder/init(maximumnumbermidiwords:))

##### Instance Properties

- [var capacity: Int](/documentation/coremidi/midieventpacket/builder/capacity)
- [var count: Int](/documentation/coremidi/midieventpacket/builder/count)
- [var timeStamp: Int](/documentation/coremidi/midieventpacket/builder/timestamp)

##### Instance Methods

- [func append(UInt32...)](/documentation/coremidi/midieventpacket/builder/append(_:))
- [func withUnsafeMutableMIDIEventPacketPointer<Result>((inout UnsafeMutableMIDIEventPacketPointer) -> Result) -> Result](/documentation/coremidi/midieventpacket/builder/withunsafemutablemidieventpacketpointer(_:))
- [func withUnsafePointer<Result>((UnsafePointer<MIDIEventPacket>) -> Result) -> Result](/documentation/coremidi/midieventpacket/builder/withunsafepointer(_:))

#### Structures

- [MIDIEventPacket.WordCollection](/documentation/coremidi/midieventpacket/wordcollection)

##### Initializers

- [init(UnsafePointer<MIDIEventPacket>)](/documentation/coremidi/midieventpacket/wordcollection/init(_:)-81z9r)
- [init?(UnsafePointer<MIDIEventPacket>?)](/documentation/coremidi/midieventpacket/wordcollection/init(_:)-922um)

##### Instance Properties

- [var count: Int](/documentation/coremidi/midieventpacket/wordcollection/count)
- [var endIndex: Int](/documentation/coremidi/midieventpacket/wordcollection/endindex)
- [var startIndex: Int](/documentation/coremidi/midieventpacket/wordcollection/startindex)

##### Subscripts

- [subscript(MIDIEventPacket.WordCollection.Index) -> MIDIEventPacket.WordCollection.Element](/documentation/coremidi/midieventpacket/wordcollection/subscript(_:))
- [MIDIEventPacket.WordSequence](/documentation/coremidi/midieventpacket/wordsequence)

##### Instance Properties

- [var count: Int](/documentation/coremidi/midieventpacket/wordsequence/count)

#### Initializers

- [init()](/documentation/coremidi/midieventpacket/init())
- [init(timeStamp: MIDITimeStamp, wordCount: UInt32, words: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32))](/documentation/coremidi/midieventpacket/init(timestamp:wordcount:words:))
- [UnsafeMutableMIDIEventListPointer](/documentation/coremidi/unsafemutablemidieventlistpointer)

#### Initializers

- [init?(UnsafeMutablePointer<MIDIEventList>?, wordSize: Int)](/documentation/coremidi/unsafemutablemidieventlistpointer/init(_:wordsize:))
- [init(UnsafeMutablePointer<MIDIEventList>, wordSize: Int, inProtocol: MIDIProtocolID)](/documentation/coremidi/unsafemutablemidieventlistpointer/init(_:wordsize:inprotocol:))

#### Instance Properties

- [var count: Int](/documentation/coremidi/unsafemutablemidieventlistpointer/count)
- [var lastPacket: UnsafeMutablePointer<MIDIEventPacket>?](/documentation/coremidi/unsafemutablemidieventlistpointer/lastpacket)
- [var listSizeInBytes: Int](/documentation/coremidi/unsafemutablemidieventlistpointer/listsizeinbytes)
- [var midiProtocol: MIDIProtocolID](/documentation/coremidi/unsafemutablemidieventlistpointer/midiprotocol)

#### Instance Methods

- [func append(timestamp: MIDITimeStamp, words: [UInt32]) -> UnsafePointer<MIDIEventPacket>?](/documentation/coremidi/unsafemutablemidieventlistpointer/append(timestamp:words:))
- [func clear()](/documentation/coremidi/unsafemutablemidieventlistpointer/clear())
- [UnsafeMutableMIDIEventPacketPointer](/documentation/coremidi/unsafemutablemidieventpacketpointer)

#### Initializers

- [init(UnsafeMutablePointer<MIDIEventPacket>)](/documentation/coremidi/unsafemutablemidieventpacketpointer/init(_:)-2pp97)
- [init?(UnsafeMutablePointer<MIDIEventPacket>?)](/documentation/coremidi/unsafemutablemidieventpacketpointer/init(_:)-91lug)

#### Instance Properties

- [var count: Int](/documentation/coremidi/unsafemutablemidieventpacketpointer/count)
- [var timeStamp: Int](/documentation/coremidi/unsafemutablemidieventpacketpointer/timestamp)

#### Default Implementations

- [MutableCollection Implementations](/documentation/coremidi/unsafemutablemidieventpacketpointer/mutablecollection-implementations)

##### Subscripts

- [subscript(UnsafeMutableMIDIEventPacketPointer.Index) -> UnsafeMutableMIDIEventPacketPointer.Element](/documentation/coremidi/unsafemutablemidieventpacketpointer/subscript(_:))
- [RandomAccessCollection Implementations](/documentation/coremidi/unsafemutablemidieventpacketpointer/randomaccesscollection-implementations)

##### Instance Properties

- [var endIndex: Int](/documentation/coremidi/unsafemutablemidieventpacketpointer/endindex)
- [var startIndex: Int](/documentation/coremidi/unsafemutablemidieventpacketpointer/startindex)

### Packet list management

- [func MIDIPacketNext(UnsafePointer<MIDIPacket>) -> UnsafeMutablePointer<MIDIPacket>](/documentation/coremidi/midipacketnext(_:))
- [MIDIPacket](/documentation/coremidi/midipacket)

#### Configuring a Packet

- [var timeStamp: MIDITimeStamp](/documentation/coremidi/midipacket/timestamp)
- [var length: UInt16](/documentation/coremidi/midipacket/length)
- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/coremidi/midipacket/data)

#### Classes

- [MIDIPacket.Builder](/documentation/coremidi/midipacket/builder)

##### Initializers

- [init(maximumNumberMIDIBytes: Int)](/documentation/coremidi/midipacket/builder/init(maximumnumbermidibytes:))

##### Instance Properties

- [var capacity: Int](/documentation/coremidi/midipacket/builder/capacity)
- [var count: Int](/documentation/coremidi/midipacket/builder/count)
- [var timeStamp: Int](/documentation/coremidi/midipacket/builder/timestamp)

##### Instance Methods

- [func append(UInt8...)](/documentation/coremidi/midipacket/builder/append(_:))
- [func withUnsafeMutableMIDIPacketPointer<Result>((inout UnsafeMutableMIDIPacketPointer) -> Result) -> Result](/documentation/coremidi/midipacket/builder/withunsafemutablemidipacketpointer(_:))
- [func withUnsafePointer<Result>((UnsafePointer<MIDIPacket>) -> Result) -> Result](/documentation/coremidi/midipacket/builder/withunsafepointer(_:))

#### Structures

- [MIDIPacket.ByteCollection](/documentation/coremidi/midipacket/bytecollection)

##### Initializers

- [init(UnsafePointer<MIDIPacket>)](/documentation/coremidi/midipacket/bytecollection/init(_:)-5j13x)
- [init?(UnsafePointer<MIDIPacket>?)](/documentation/coremidi/midipacket/bytecollection/init(_:)-8ul4l)

##### Instance Properties

- [var count: Int](/documentation/coremidi/midipacket/bytecollection/count)
- [var endIndex: Int](/documentation/coremidi/midipacket/bytecollection/endindex)
- [var startIndex: Int](/documentation/coremidi/midipacket/bytecollection/startindex)

##### Subscripts

- [subscript(MIDIPacket.ByteCollection.Index) -> MIDIPacket.ByteCollection.Element](/documentation/coremidi/midipacket/bytecollection/subscript(_:))
- [MIDIPacket.ByteSequence](/documentation/coremidi/midipacket/bytesequence)

##### Instance Properties

- [var count: Int](/documentation/coremidi/midipacket/bytesequence/count)

#### Initializers

- [init()](/documentation/coremidi/midipacket/init())
- [init(timeStamp: MIDITimeStamp, length: UInt16, data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/coremidi/midipacket/init(timestamp:length:data:))
- [MIDIPacketList](/documentation/coremidi/midipacketlist)

#### Inspecting a Packet List

- [var numPackets: UInt32](/documentation/coremidi/midipacketlist/numpackets)
- [var packet: MIDIPacket](/documentation/coremidi/midipacketlist/packet)

#### Classes

- [MIDIPacketList.Builder](/documentation/coremidi/midipacketlist/builder)

##### Initializers

- [init(byteSize: Int)](/documentation/coremidi/midipacketlist/builder/init(bytesize:))

##### Instance Properties

- [var count: Int](/documentation/coremidi/midipacketlist/builder/count)

##### Instance Methods

- [func append(timestamp: MIDITimeStamp, data: [UInt8]) -> UnsafePointer<MIDIPacket>?](/documentation/coremidi/midipacketlist/builder/append(timestamp:data:))
- [func clear()](/documentation/coremidi/midipacketlist/builder/clear())
- [func withUnsafeMutableMIDIPacketListPointer<Result>((inout UnsafeMutableMIDIPacketListPointer) -> Result) -> Result](/documentation/coremidi/midipacketlist/builder/withunsafemutablemidipacketlistpointer(_:))
- [func withUnsafePointer<Result>((UnsafePointer<MIDIPacketList>) -> Result) -> Result](/documentation/coremidi/midipacketlist/builder/withunsafepointer(_:))

#### Structures

- [MIDIPacketList.UnsafeSequence](/documentation/coremidi/midipacketlist/unsafesequence)

##### Instance Properties

- [var count: Int](/documentation/coremidi/midipacketlist/unsafesequence/count)

#### Initializers

- [init()](/documentation/coremidi/midipacketlist/init())
- [init(numPackets: UInt32, packet: MIDIPacket)](/documentation/coremidi/midipacketlist/init(numpackets:packet:))

#### Type Methods

- [static func sizeInBytes(pktList: UnsafePointer<MIDIPacketList>) -> Int](/documentation/coremidi/midipacketlist/sizeinbytes(pktlist:))
- [MIDITimeStamp](/documentation/coremidi/miditimestamp)
- [UnsafeMutableMIDIPacketListPointer](/documentation/coremidi/unsafemutablemidipacketlistpointer)

#### Initializers

- [init(UnsafeMutablePointer<MIDIPacketList>, byteSize: Int)](/documentation/coremidi/unsafemutablemidipacketlistpointer/init(_:bytesize:)-8acwt)
- [init?(UnsafeMutablePointer<MIDIPacketList>?, byteSize: Int)](/documentation/coremidi/unsafemutablemidipacketlistpointer/init(_:bytesize:)-96k5n)

#### Instance Properties

- [var count: Int](/documentation/coremidi/unsafemutablemidipacketlistpointer/count)
- [var lastPacket: UnsafeMutablePointer<MIDIPacket>?](/documentation/coremidi/unsafemutablemidipacketlistpointer/lastpacket)
- [var listSizeInBytes: Int](/documentation/coremidi/unsafemutablemidipacketlistpointer/listsizeinbytes)

#### Instance Methods

- [func append(timestamp: MIDITimeStamp, data: [UInt8]) -> UnsafePointer<MIDIPacket>?](/documentation/coremidi/unsafemutablemidipacketlistpointer/append(timestamp:data:))
- [func clear()](/documentation/coremidi/unsafemutablemidipacketlistpointer/clear())
- [UnsafeMutableMIDIPacketPointer](/documentation/coremidi/unsafemutablemidipacketpointer)

#### Initializers

- [init(UnsafeMutablePointer<MIDIPacket>)](/documentation/coremidi/unsafemutablemidipacketpointer/init(_:)-5z9po)
- [init?(UnsafeMutablePointer<MIDIPacket>?)](/documentation/coremidi/unsafemutablemidipacketpointer/init(_:)-7ypj1)

#### Instance Properties

- [var count: Int](/documentation/coremidi/unsafemutablemidipacketpointer/count)
- [var timeStamp: Int](/documentation/coremidi/unsafemutablemidipacketpointer/timestamp)

#### Default Implementations

- [MutableCollection Implementations](/documentation/coremidi/unsafemutablemidipacketpointer/mutablecollection-implementations)

##### Subscripts

- [subscript(UnsafeMutableMIDIPacketPointer.Index) -> UnsafeMutableMIDIPacketPointer.Element](/documentation/coremidi/unsafemutablemidipacketpointer/subscript(_:))
- [RandomAccessCollection Implementations](/documentation/coremidi/unsafemutablemidipacketpointer/randomaccesscollection-implementations)

##### Instance Properties

- [var endIndex: Int](/documentation/coremidi/unsafemutablemidipacketpointer/endindex)
- [var startIndex: Int](/documentation/coremidi/unsafemutablemidipacketpointer/startindex)

### I/O management

- [MIDISysexSendRequest](/documentation/coremidi/midisysexsendrequest)

#### Creating a request

- [init(destination: MIDIEndpointRef, data: UnsafePointer<UInt8>, bytesToSend: UInt32, complete: DarwinBoolean, reserved: (UInt8, UInt8, UInt8), completionProc: MIDICompletionProc, completionRefCon: UnsafeMutableRawPointer?)](/documentation/coremidi/midisysexsendrequest/init(destination:data:bytestosend:complete:reserved:completionproc:completionrefcon:))

#### Configuring a request

- [var destination: MIDIEndpointRef](/documentation/coremidi/midisysexsendrequest/destination)
- [var data: UnsafePointer<UInt8>](/documentation/coremidi/midisysexsendrequest/data)
- [var bytesToSend: UInt32](/documentation/coremidi/midisysexsendrequest/bytestosend)
- [var complete: DarwinBoolean](/documentation/coremidi/midisysexsendrequest/complete)
- [MIDICompletionProc](/documentation/coremidi/midicompletionproc)
- [var completionProc: MIDICompletionProc](/documentation/coremidi/midisysexsendrequest/completionproc)
- [var completionRefCon: UnsafeMutableRawPointer?](/documentation/coremidi/midisysexsendrequest/completionrefcon)
- [var reserved: (UInt8, UInt8, UInt8)](/documentation/coremidi/midisysexsendrequest/reserved)

#### Sending a request

- [func MIDISendSysex(UnsafeMutablePointer<MIDISysexSendRequest>) -> OSStatus](/documentation/coremidi/midisendsysex(_:))
- [MIDISysexSendRequestUMP](/documentation/coremidi/midisysexsendrequestump)

#### Creating a request

- [init(destination: MIDIEndpointRef, words: UnsafeMutablePointer<UInt32>, wordsToSend: UInt32, complete: DarwinBoolean, completionProc: MIDICompletionProcUMP, completionRefCon: UnsafeMutableRawPointer?)](/documentation/coremidi/midisysexsendrequestump/init(destination:words:wordstosend:complete:completionproc:completionrefcon:))

#### Configuring and inspecting a request

- [var destination: MIDIEndpointRef](/documentation/coremidi/midisysexsendrequestump/destination)
- [var words: UnsafeMutablePointer<UInt32>](/documentation/coremidi/midisysexsendrequestump/words)
- [var wordsToSend: UInt32](/documentation/coremidi/midisysexsendrequestump/wordstosend)
- [var complete: DarwinBoolean](/documentation/coremidi/midisysexsendrequestump/complete)
- [MIDICompletionProcUMP](/documentation/coremidi/midicompletionprocump)
- [var completionProc: MIDICompletionProcUMP](/documentation/coremidi/midisysexsendrequestump/completionproc)
- [var completionRefCon: UnsafeMutableRawPointer?](/documentation/coremidi/midisysexsendrequestump/completionrefcon)
- [func MIDIEventPacketSysexBytesForGroup(UnsafePointer<MIDIEventPacket>, UInt8, UnsafeMutablePointer<Unmanaged<CFData>?>) -> OSStatus](/documentation/coremidi/midieventpacketsysexbytesforgroup(_:_:_:))

#### Sending a request

- [func MIDISendUMPSysex(UnsafeMutablePointer<MIDISysexSendRequestUMP>) -> OSStatus](/documentation/coremidi/midisendumpsysex(_:))
- [func MIDISendUMPSysex8(UnsafeMutablePointer<MIDISysexSendRequestUMP>) -> OSStatus](/documentation/coremidi/midisendumpsysex8(_:))
- [func MIDIFlushOutput(MIDIEndpointRef) -> OSStatus](/documentation/coremidi/midiflushoutput(_:))
- [func MIDIRestart() -> OSStatus](/documentation/coremidi/midirestart())
- [MIDIIOErrorNotification](/documentation/coremidi/midiioerrornotification)

#### Creating an error notification

- [init()](/documentation/coremidi/midiioerrornotification/init())
- [init(messageID: MIDINotificationMessageID, messageSize: UInt32, driverDevice: MIDIDeviceRef, errorCode: OSStatus)](/documentation/coremidi/midiioerrornotification/init(messageid:messagesize:driverdevice:errorcode:))

#### Inspecting an error notification

- [var messageID: MIDINotificationMessageID](/documentation/coremidi/midiioerrornotification/messageid)
- [var messageSize: UInt32](/documentation/coremidi/midiioerrornotification/messagesize)
- [var driverDevice: MIDIDeviceRef](/documentation/coremidi/midiioerrornotification/driverdevice)
- [var errorCode: OSStatus](/documentation/coremidi/midiioerrornotification/errorcode)

### Errors

- [MIDI Services Errors](/documentation/coremidi/midi-services-errors)

#### Error Codes

- [var kMIDIInvalidClient: OSStatus](/documentation/coremidi/kmidiinvalidclient)
- [var kMIDIInvalidPort: OSStatus](/documentation/coremidi/kmidiinvalidport)
- [var kMIDIWrongEndpointType: OSStatus](/documentation/coremidi/kmidiwrongendpointtype)
- [var kMIDINoConnection: OSStatus](/documentation/coremidi/kmidinoconnection)
- [var kMIDIUnknownEndpoint: OSStatus](/documentation/coremidi/kmidiunknownendpoint)
- [var kMIDIUnknownProperty: OSStatus](/documentation/coremidi/kmidiunknownproperty)
- [var kMIDIWrongPropertyType: OSStatus](/documentation/coremidi/kmidiwrongpropertytype)
- [var kMIDINoCurrentSetup: OSStatus](/documentation/coremidi/kmidinocurrentsetup)
- [var kMIDIMessageSendErr: OSStatus](/documentation/coremidi/kmidimessagesenderr)
- [var kMIDIServerStartErr: OSStatus](/documentation/coremidi/kmidiserverstarterr)
- [var kMIDISetupFormatErr: OSStatus](/documentation/coremidi/kmidisetupformaterr)
- [var kMIDIWrongThread: OSStatus](/documentation/coremidi/kmidiwrongthread)
- [var kMIDIObjectNotFound: OSStatus](/documentation/coremidi/kmidiobjectnotfound)
- [var kMIDIIDNotUnique: OSStatus](/documentation/coremidi/kmidiidnotunique)
- [var kMIDINotPermitted: OSStatus](/documentation/coremidi/kmidinotpermitted)
- [var kMIDIUnknownError: OSStatus](/documentation/coremidi/kmidiunknownerror)

### Deprecated

- [Deprecated Symbols](/documentation/coremidi/deprecated-symbols)

#### Deprecated Functions

- [func MIDIInputPortCreate(MIDIClientRef, CFString, MIDIReadProc, UnsafeMutableRawPointer?, UnsafeMutablePointer<MIDIPortRef>) -> OSStatus](/documentation/coremidi/midiinputportcreate(_:_:_:_:_:))
- [func MIDIInputPortCreateWithBlock(MIDIClientRef, CFString, UnsafeMutablePointer<MIDIPortRef>, MIDIReadBlock) -> OSStatus](/documentation/coremidi/midiinputportcreatewithblock(_:_:_:_:))
- [func MIDISourceCreate(MIDIClientRef, CFString, UnsafeMutablePointer<MIDIEndpointRef>) -> OSStatus](/documentation/coremidi/midisourcecreate(_:_:_:))
- [func MIDIDestinationCreate(MIDIClientRef, CFString, MIDIReadProc, UnsafeMutableRawPointer?, UnsafeMutablePointer<MIDIEndpointRef>) -> OSStatus](/documentation/coremidi/mididestinationcreate(_:_:_:_:_:))
- [func MIDIDestinationCreateWithBlock(MIDIClientRef, CFString, UnsafeMutablePointer<MIDIEndpointRef>, MIDIReadBlock) -> OSStatus](/documentation/coremidi/mididestinationcreatewithblock(_:_:_:_:))
- [func MIDIPacketListInit(UnsafeMutablePointer<MIDIPacketList>) -> UnsafeMutablePointer<MIDIPacket>](/documentation/coremidi/midipacketlistinit(_:))
- [func MIDIPacketListAdd(UnsafeMutablePointer<MIDIPacketList>, Int, UnsafeMutablePointer<MIDIPacket>, MIDITimeStamp, Int, UnsafePointer<UInt8>) -> UnsafeMutablePointer<MIDIPacket>](/documentation/coremidi/midipacketlistadd(_:_:_:_:_:_:))
- [func MIDISend(MIDIPortRef, MIDIEndpointRef, UnsafePointer<MIDIPacketList>) -> OSStatus](/documentation/coremidi/midisend(_:_:_:))
- [func MIDIReceived(MIDIEndpointRef, UnsafePointer<MIDIPacketList>) -> OSStatus](/documentation/coremidi/midireceived(_:_:))
- [MIDIReadProc](/documentation/coremidi/midireadproc)
- [MIDIReadBlock](/documentation/coremidi/midireadblock)
- [MIDI System Setup](/documentation/coremidi/midi-system-setup)

### Managing Devices

- [func MIDISetupAddDevice(MIDIDeviceRef) -> OSStatus](/documentation/coremidi/midisetupadddevice(_:))
- [func MIDISetupRemoveDevice(MIDIDeviceRef) -> OSStatus](/documentation/coremidi/midisetupremovedevice(_:))

### Managing External Devices

- [func MIDIExternalDeviceCreate(CFString, CFString, CFString, UnsafeMutablePointer<MIDIDeviceRef>) -> OSStatus](/documentation/coremidi/midiexternaldevicecreate(_:_:_:_:))
- [func MIDISetupAddExternalDevice(MIDIDeviceRef) -> OSStatus](/documentation/coremidi/midisetupaddexternaldevice(_:))
- [func MIDISetupRemoveExternalDevice(MIDIDeviceRef) -> OSStatus](/documentation/coremidi/midisetupremoveexternaldevice(_:))

### Managing Entities

- [func MIDIDeviceNewEntity(MIDIDeviceRef, CFString, MIDIProtocolID, Bool, Int, Int, UnsafeMutablePointer<MIDIEntityRef>) -> OSStatus](/documentation/coremidi/mididevicenewentity(_:_:_:_:_:_:_:))
- [func MIDIDeviceRemoveEntity(MIDIDeviceRef, MIDIEntityRef) -> OSStatus](/documentation/coremidi/midideviceremoveentity(_:_:))
- [func MIDIEntityAddOrRemoveEndpoints(MIDIEntityRef, Int, Int) -> OSStatus](/documentation/coremidi/midientityaddorremoveendpoints(_:_:_:))

### Deprecated

- [Deprecated Symbols](/documentation/coremidi/deprecated-symbols)

#### Deprecated Functions

- [func MIDIInputPortCreate(MIDIClientRef, CFString, MIDIReadProc, UnsafeMutableRawPointer?, UnsafeMutablePointer<MIDIPortRef>) -> OSStatus](/documentation/coremidi/midiinputportcreate(_:_:_:_:_:))
- [func MIDIInputPortCreateWithBlock(MIDIClientRef, CFString, UnsafeMutablePointer<MIDIPortRef>, MIDIReadBlock) -> OSStatus](/documentation/coremidi/midiinputportcreatewithblock(_:_:_:_:))
- [func MIDISourceCreate(MIDIClientRef, CFString, UnsafeMutablePointer<MIDIEndpointRef>) -> OSStatus](/documentation/coremidi/midisourcecreate(_:_:_:))
- [func MIDIDestinationCreate(MIDIClientRef, CFString, MIDIReadProc, UnsafeMutableRawPointer?, UnsafeMutablePointer<MIDIEndpointRef>) -> OSStatus](/documentation/coremidi/mididestinationcreate(_:_:_:_:_:))
- [func MIDIDestinationCreateWithBlock(MIDIClientRef, CFString, UnsafeMutablePointer<MIDIEndpointRef>, MIDIReadBlock) -> OSStatus](/documentation/coremidi/mididestinationcreatewithblock(_:_:_:_:))
- [func MIDIPacketListInit(UnsafeMutablePointer<MIDIPacketList>) -> UnsafeMutablePointer<MIDIPacket>](/documentation/coremidi/midipacketlistinit(_:))
- [func MIDIPacketListAdd(UnsafeMutablePointer<MIDIPacketList>, Int, UnsafeMutablePointer<MIDIPacket>, MIDITimeStamp, Int, UnsafePointer<UInt8>) -> UnsafeMutablePointer<MIDIPacket>](/documentation/coremidi/midipacketlistadd(_:_:_:_:_:_:))
- [func MIDISend(MIDIPortRef, MIDIEndpointRef, UnsafePointer<MIDIPacketList>) -> OSStatus](/documentation/coremidi/midisend(_:_:_:))
- [func MIDIReceived(MIDIEndpointRef, UnsafePointer<MIDIPacketList>) -> OSStatus](/documentation/coremidi/midireceived(_:_:))
- [MIDIReadProc](/documentation/coremidi/midireadproc)
- [MIDIReadBlock](/documentation/coremidi/midireadblock)
- [MIDI Bluetooth](/documentation/coremidi/midi-bluetooth)

### Managing Device Connections

- [func MIDIBluetoothDriverActivateAllConnections() -> OSStatus](/documentation/coremidi/midibluetoothdriveractivateallconnections())
- [func MIDIBluetoothDriverDisconnect(CFString) -> OSStatus](/documentation/coremidi/midibluetoothdriverdisconnect(_:))
- [MIDI Messages](/documentation/coremidi/midi-messages)

### MIDI 1.0 Messages

- [func MIDI1UPNoteOn(UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1upnoteon(_:_:_:_:))
- [func MIDI1UPNoteOff(UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1upnoteoff(_:_:_:_:))
- [func MIDI1UPPitchBend(UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1uppitchbend(_:_:_:_:))
- [func MIDI1UPControlChange(UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1upcontrolchange(_:_:_:_:))
- [func MIDI1UPSystemCommon(UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1upsystemcommon(_:_:_:_:))
- [func MIDI1UPChannelVoiceMessage(UInt8, UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1upchannelvoicemessage(_:_:_:_:_:))
- [func MIDIMessageTypeForUPWord(UInt32) -> MIDIMessageType](/documentation/coremidi/midimessagetypeforupword(_:))

### MIDI 2.0 Messages

- [func MIDI2ChannelVoiceMessage(UInt8, UInt8, UInt8, UInt16, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2channelvoicemessage(_:_:_:_:_:))
- [func MIDI2NoteOn(UInt8, UInt8, UInt8, UInt8, UInt16, UInt16) -> MIDIMessage_64](/documentation/coremidi/midi2noteon(_:_:_:_:_:_:))
- [func MIDI2NoteOff(UInt8, UInt8, UInt8, UInt8, UInt16, UInt16) -> MIDIMessage_64](/documentation/coremidi/midi2noteoff(_:_:_:_:_:_:))
- [func MIDI2ControlChange(UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2controlchange(_:_:_:_:))
- [func MIDI2ProgramChange(UInt8, UInt8, Bool, UInt8, UInt8, UInt8) -> MIDIMessage_64](/documentation/coremidi/midi2programchange(_:_:_:_:_:_:))
- [func MIDI2PitchBend(UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2pitchbend(_:_:_:))
- [func MIDI2PerNotePitchBend(UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2pernotepitchbend(_:_:_:_:))
- [func MIDI2ChannelPressure(UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2channelpressure(_:_:_:))
- [func MIDI2PolyPressure(UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2polypressure(_:_:_:_:))
- [func MIDI2AssignableControl(UInt8, UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2assignablecontrol(_:_:_:_:_:))
- [func MIDI2RelRegisteredControl(UInt8, UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2relregisteredcontrol(_:_:_:_:_:))
- [func MIDI2AssignablePNC(UInt8, UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2assignablepnc(_:_:_:_:_:))
- [func MIDI2RegisteredPNC(UInt8, UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2registeredpnc(_:_:_:_:_:))
- [func MIDI2RelAssignableControl(UInt8, UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2relassignablecontrol(_:_:_:_:_:))
- [func MIDI2RegisteredControl(UInt8, UInt8, UInt8, UInt8, UInt32) -> MIDIMessage_64](/documentation/coremidi/midi2registeredcontrol(_:_:_:_:_:))
- [func MIDI2PerNoteManagment(UInt8, UInt8, UInt8, Bool, Bool) -> MIDIMessage_64](/documentation/coremidi/midi2pernotemanagment(_:_:_:_:_:))

### Common

- [MIDICVStatus](/documentation/coremidi/midicvstatus)

#### MIDI 1.0

- [case noteOff](/documentation/coremidi/midicvstatus/noteoff)
- [case noteOn](/documentation/coremidi/midicvstatus/noteon)
- [case polyPressure](/documentation/coremidi/midicvstatus/polypressure)
- [case controlChange](/documentation/coremidi/midicvstatus/controlchange)
- [case programChange](/documentation/coremidi/midicvstatus/programchange)
- [case channelPressure](/documentation/coremidi/midicvstatus/channelpressure)
- [case pitchBend](/documentation/coremidi/midicvstatus/pitchbend)

#### MIDI 2.0

- [case registeredPNC](/documentation/coremidi/midicvstatus/registeredpnc)
- [case assignablePNC](/documentation/coremidi/midicvstatus/assignablepnc)
- [case registeredControl](/documentation/coremidi/midicvstatus/registeredcontrol)
- [case assignableControl](/documentation/coremidi/midicvstatus/assignablecontrol)
- [case relRegisteredControl](/documentation/coremidi/midicvstatus/relregisteredcontrol)
- [case relAssignableControl](/documentation/coremidi/midicvstatus/relassignablecontrol)
- [case perNotePitchBend](/documentation/coremidi/midicvstatus/pernotepitchbend)
- [case perNoteMgmt](/documentation/coremidi/midicvstatus/pernotemgmt)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coremidi/midicvstatus/init(rawvalue:))
- [MIDIProtocolID](/documentation/coremidi/midiprotocolid)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coremidi/midiprotocolid/init(rawvalue:))
- [MIDISysExStatus](/documentation/coremidi/midisysexstatus)

#### Status Types

- [case complete](/documentation/coremidi/midisysexstatus/complete)
- [case start](/documentation/coremidi/midisysexstatus/start)
- [case `continue`](/documentation/coremidi/midisysexstatus/continue)
- [case end](/documentation/coremidi/midisysexstatus/end)

#### Enumeration Cases

- [case mixedDataSetHeader](/documentation/coremidi/midisysexstatus/mixeddatasetheader)
- [case mixedDataSetPayload](/documentation/coremidi/midisysexstatus/mixeddatasetpayload)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coremidi/midisysexstatus/init(rawvalue:))
- [MIDISystemStatus](/documentation/coremidi/midisystemstatus)

#### Status Types

- [case statusActiveSending](/documentation/coremidi/midisystemstatus/statusactivesending)
- [case statusContinue](/documentation/coremidi/midisystemstatus/statuscontinue)
- [case statusEndOfExclusive](/documentation/coremidi/midisystemstatus/statusendofexclusive)
- [case statusMTC](/documentation/coremidi/midisystemstatus/statusmtc)
- [case statusSongPosPointer](/documentation/coremidi/midisystemstatus/statussongpospointer)
- [case statusSongSelect](/documentation/coremidi/midisystemstatus/statussongselect)
- [case statusStart](/documentation/coremidi/midisystemstatus/statusstart)
- [case statusStartOfExclusive](/documentation/coremidi/midisystemstatus/statusstartofexclusive)
- [case statusStop](/documentation/coremidi/midisystemstatus/statusstop)
- [case statusSystemReset](/documentation/coremidi/midisystemstatus/statussystemreset)
- [case statusTimingClock](/documentation/coremidi/midisystemstatus/statustimingclock)
- [case statusTuneRequest](/documentation/coremidi/midisystemstatus/statustunerequest)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coremidi/midisystemstatus/init(rawvalue:))

#### Type Properties

- [static var statusActiveSensing: MIDISystemStatus](/documentation/coremidi/midisystemstatus/statusactivesensing)
- [MIDIMessage_128](/documentation/coremidi/midimessage_128)

#### Words

- [var word0: UInt32](/documentation/coremidi/midimessage_128/word0)
- [var word1: UInt32](/documentation/coremidi/midimessage_128/word1)
- [var word2: UInt32](/documentation/coremidi/midimessage_128/word2)
- [var word3: UInt32](/documentation/coremidi/midimessage_128/word3)

#### Initializers

- [init()](/documentation/coremidi/midimessage_128/init())
- [init(word0: UInt32, word1: UInt32, word2: UInt32, word3: UInt32)](/documentation/coremidi/midimessage_128/init(word0:word1:word2:word3:))
- [MIDIMessage_96](/documentation/coremidi/midimessage_96)

#### Words

- [var word0: UInt32](/documentation/coremidi/midimessage_96/word0)
- [var word1: UInt32](/documentation/coremidi/midimessage_96/word1)
- [var word2: UInt32](/documentation/coremidi/midimessage_96/word2)

#### Initializers

- [init()](/documentation/coremidi/midimessage_96/init())
- [init(word0: UInt32, word1: UInt32, word2: UInt32)](/documentation/coremidi/midimessage_96/init(word0:word1:word2:))
- [MIDIMessage_64](/documentation/coremidi/midimessage_64)

#### Words

- [var word0: UInt32](/documentation/coremidi/midimessage_64/word0)
- [var word1: UInt32](/documentation/coremidi/midimessage_64/word1)

#### Initializers

- [init()](/documentation/coremidi/midimessage_64/init())
- [init(word0: UInt32, word1: UInt32)](/documentation/coremidi/midimessage_64/init(word0:word1:))
- [MIDIMessage_32](/documentation/coremidi/midimessage_32)
- [MIDIMessageType](/documentation/coremidi/midimessagetype)

#### Message Types

- [case channelVoice1](/documentation/coremidi/midimessagetype/channelvoice1)
- [case channelVoice2](/documentation/coremidi/midimessagetype/channelvoice2)
- [case data128](/documentation/coremidi/midimessagetype/data128)
- [case sysEx](/documentation/coremidi/midimessagetype/sysex)
- [case system](/documentation/coremidi/midimessagetype/system)
- [case utility](/documentation/coremidi/midimessagetype/utility)

#### Enumeration Cases

- [case flexData](/documentation/coremidi/midimessagetype/flexdata)
- [case invalid](/documentation/coremidi/midimessagetype/invalid)
- [case unknownF](/documentation/coremidi/midimessagetype/unknownf)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coremidi/midimessagetype/init(rawvalue:))

#### Type Properties

- [static var stream: MIDIMessageType](/documentation/coremidi/midimessagetype/stream)
- [MIDI Thru Connection](/documentation/coremidi/midi-thru-connection)

### Finding Connections

- [func MIDIThruConnectionFind(CFString, UnsafeMutablePointer<Unmanaged<CFData>>) -> OSStatus](/documentation/coremidi/midithruconnectionfind(_:_:))

### Managing Connections

- [func MIDIThruConnectionCreate(CFString?, CFData, UnsafeMutablePointer<MIDIThruConnectionRef>) -> OSStatus](/documentation/coremidi/midithruconnectioncreate(_:_:_:))
- [func MIDIThruConnectionDispose(MIDIThruConnectionRef) -> OSStatus](/documentation/coremidi/midithruconnectiondispose(_:))
- [MIDIThruConnectionRef](/documentation/coremidi/midithruconnectionref)
- [MIDIThruConnectionEndpoint](/documentation/coremidi/midithruconnectionendpoint)

#### Configuring an Endpoint

- [var uniqueID: MIDIUniqueID](/documentation/coremidi/midithruconnectionendpoint/uniqueid)
- [var endpointRef: MIDIEndpointRef](/documentation/coremidi/midithruconnectionendpoint/endpointref)

#### Initializers

- [init()](/documentation/coremidi/midithruconnectionendpoint/init())
- [init(endpointRef: MIDIEndpointRef, uniqueID: MIDIUniqueID)](/documentation/coremidi/midithruconnectionendpoint/init(endpointref:uniqueid:))
- [Endpoint Configuration](/documentation/coremidi/endpoint-configuration)

#### Configuration Constants

- [var kMIDIThruConnection_MaxEndpoints: Int](/documentation/coremidi/kmidithruconnection_maxendpoints)

### Configuring Parameters

- [MIDIThruConnectionParams](/documentation/coremidi/midithruconnectionparams)

#### Connection Parameters

- [var noteNumber: MIDITransform](/documentation/coremidi/midithruconnectionparams/notenumber)
- [var lowNote: UInt8](/documentation/coremidi/midithruconnectionparams/lownote)
- [var highNote: UInt8](/documentation/coremidi/midithruconnectionparams/highnote)
- [var velocity: MIDITransform](/documentation/coremidi/midithruconnectionparams/velocity)
- [var lowVelocity: UInt8](/documentation/coremidi/midithruconnectionparams/lowvelocity)
- [var highVelocity: UInt8](/documentation/coremidi/midithruconnectionparams/highvelocity)
- [var keyPressure: MIDITransform](/documentation/coremidi/midithruconnectionparams/keypressure)
- [var channelPressure: MIDITransform](/documentation/coremidi/midithruconnectionparams/channelpressure)
- [var version: UInt32](/documentation/coremidi/midithruconnectionparams/version)
- [var numSources: UInt32](/documentation/coremidi/midithruconnectionparams/numsources)
- [var sources: (MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint)](/documentation/coremidi/midithruconnectionparams/sources)
- [var numDestinations: UInt32](/documentation/coremidi/midithruconnectionparams/numdestinations)
- [var destinations: (MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint)](/documentation/coremidi/midithruconnectionparams/destinations)
- [var channelMap: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/coremidi/midithruconnectionparams/channelmap)
- [var filterOutAllControls: UInt8](/documentation/coremidi/midithruconnectionparams/filteroutallcontrols)
- [var filterOutBeatClock: UInt8](/documentation/coremidi/midithruconnectionparams/filteroutbeatclock)
- [var filterOutMTC: UInt8](/documentation/coremidi/midithruconnectionparams/filteroutmtc)
- [var filterOutSysEx: UInt8](/documentation/coremidi/midithruconnectionparams/filteroutsysex)
- [var filterOutTuneRequest: UInt8](/documentation/coremidi/midithruconnectionparams/filterouttunerequest)
- [var numControlTransforms: UInt16](/documentation/coremidi/midithruconnectionparams/numcontroltransforms)
- [var numMaps: UInt16](/documentation/coremidi/midithruconnectionparams/nummaps)
- [var pitchBend: MIDITransform](/documentation/coremidi/midithruconnectionparams/pitchbend)
- [var programChange: MIDITransform](/documentation/coremidi/midithruconnectionparams/programchange)
- [var reserved2: (UInt8, UInt8, UInt8)](/documentation/coremidi/midithruconnectionparams/reserved2)
- [var reserved3: (UInt16, UInt16, UInt16, UInt16)](/documentation/coremidi/midithruconnectionparams/reserved3)

#### Initializers

- [init()](/documentation/coremidi/midithruconnectionparams/init())
- [init(version: UInt32, numSources: UInt32, sources: (MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint), numDestinations: UInt32, destinations: (MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint, MIDIThruConnectionEndpoint), channelMap: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8), lowVelocity: UInt8, highVelocity: UInt8, lowNote: UInt8, highNote: UInt8, noteNumber: MIDITransform, velocity: MIDITransform, keyPressure: MIDITransform, channelPressure: MIDITransform, programChange: MIDITransform, pitchBend: MIDITransform, filterOutSysEx: UInt8, filterOutMTC: UInt8, filterOutBeatClock: UInt8, filterOutTuneRequest: UInt8, reserved2: (UInt8, UInt8, UInt8), filterOutAllControls: UInt8, numControlTransforms: UInt16, numMaps: UInt16, reserved3: (UInt16, UInt16, UInt16, UInt16))](/documentation/coremidi/midithruconnectionparams/init(version:numsources:sources:numdestinations:destinations:channelmap:lowvelocity:highvelocity:lownote:highnote:notenumber:velocity:keypressure:channelpressure:programchange:pitchbend:filteroutsysex:filteroutmtc:filteroutbeatclock:filtero-6y1ig)
- [func MIDIThruConnectionParamsSize(UnsafePointer<MIDIThruConnectionParams>) -> Int](/documentation/coremidi/midithruconnectionparamssize(_:))
- [func MIDIThruConnectionParamsInitialize(UnsafeMutablePointer<MIDIThruConnectionParams>)](/documentation/coremidi/midithruconnectionparamsinitialize(_:))
- [func MIDIThruConnectionGetParams(MIDIThruConnectionRef, UnsafeMutablePointer<Unmanaged<CFData>>) -> OSStatus](/documentation/coremidi/midithruconnectiongetparams(_:_:))
- [func MIDIThruConnectionSetParams(MIDIThruConnectionRef, CFData) -> OSStatus](/documentation/coremidi/midithruconnectionsetparams(_:_:))

### Transforming Values

- [MIDIValueMap](/documentation/coremidi/midivaluemap)

#### Creating a Value Map

- [init()](/documentation/coremidi/midivaluemap/init())
- [init(value: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/coremidi/midivaluemap/init(value:))

#### Configuring a Value Map

- [var value: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/coremidi/midivaluemap/value)
- [MIDIControlTransform](/documentation/coremidi/midicontroltransform)

#### Configuring a Control Transform

- [var controlType: MIDITransformControlType](/documentation/coremidi/midicontroltransform/controltype)
- [var remappedControlType: MIDITransformControlType](/documentation/coremidi/midicontroltransform/remappedcontroltype)
- [var controlNumber: UInt16](/documentation/coremidi/midicontroltransform/controlnumber)
- [var transform: MIDITransformType](/documentation/coremidi/midicontroltransform/transform)
- [var param: Int16](/documentation/coremidi/midicontroltransform/param)

#### Initializers

- [init()](/documentation/coremidi/midicontroltransform/init())
- [init(controlType: MIDITransformControlType, remappedControlType: MIDITransformControlType, controlNumber: UInt16, transform: MIDITransformType, param: Int16)](/documentation/coremidi/midicontroltransform/init(controltype:remappedcontroltype:controlnumber:transform:param:))
- [MIDITransform](/documentation/coremidi/miditransform)

#### Configuring a Transform

- [var param: Int16](/documentation/coremidi/miditransform/param)
- [var transform: MIDITransformType](/documentation/coremidi/miditransform/transform)

#### Initializers

- [init()](/documentation/coremidi/miditransform/init())
- [init(transform: MIDITransformType, param: Int16)](/documentation/coremidi/miditransform/init(transform:param:))
- [MIDITransformType](/documentation/coremidi/miditransformtype)

#### Transform Types

- [case none](/documentation/coremidi/miditransformtype/none)
- [case filterOut](/documentation/coremidi/miditransformtype/filterout)
- [case mapControl](/documentation/coremidi/miditransformtype/mapcontrol)
- [case add](/documentation/coremidi/miditransformtype/add)
- [case scale](/documentation/coremidi/miditransformtype/scale)
- [case minValue](/documentation/coremidi/miditransformtype/minvalue)
- [case maxValue](/documentation/coremidi/miditransformtype/maxvalue)
- [case mapValue](/documentation/coremidi/miditransformtype/mapvalue)

#### Initializers

- [init?(rawValue: UInt16)](/documentation/coremidi/miditransformtype/init(rawvalue:))
- [MIDITransformControlType](/documentation/coremidi/miditransformcontroltype)

#### Transform Control Types

- [case controlType_7Bit](/documentation/coremidi/miditransformcontroltype/controltype_7bit)
- [case controlType_14Bit](/documentation/coremidi/miditransformcontroltype/controltype_14bit)
- [case controlType_7BitRPN](/documentation/coremidi/miditransformcontroltype/controltype_7bitrpn)
- [case controlType_14BitRPN](/documentation/coremidi/miditransformcontroltype/controltype_14bitrpn)
- [case controlType_7BitNRPN](/documentation/coremidi/miditransformcontroltype/controltype_7bitnrpn)
- [case controlType_14BitNRPN](/documentation/coremidi/miditransformcontroltype/controltype_14bitnrpn)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coremidi/miditransformcontroltype/init(rawvalue:))
- [MIDI Networking](/documentation/coremidi/midi-networking)

### Networking

- [MIDINetworkHost](/documentation/coremidi/midinetworkhost)

#### Creating Network Hosts

- [convenience init(name: String, address: String, port: Int)](/documentation/coremidi/midinetworkhost/init(name:address:port:))
- [convenience init(name: String, netService: NetService)](/documentation/coremidi/midinetworkhost/init(name:netservice:))
- [convenience init(name: String, netServiceName: String, netServiceDomain: String)](/documentation/coremidi/midinetworkhost/init(name:netservicename:netservicedomain:))
- [let MIDINetworkBonjourServiceType: String](/documentation/coremidi/midinetworkbonjourservicetype)

#### Inspecting Host Properties

- [var name: String](/documentation/coremidi/midinetworkhost/name)
- [var netServiceName: String?](/documentation/coremidi/midinetworkhost/netservicename)
- [var netServiceDomain: String?](/documentation/coremidi/midinetworkhost/netservicedomain)
- [var address: String](/documentation/coremidi/midinetworkhost/address)
- [var port: Int](/documentation/coremidi/midinetworkhost/port)

#### Comparing Hosts

- [func hasSameAddress(as: MIDINetworkHost) -> Bool](/documentation/coremidi/midinetworkhost/hassameaddress(as:))
- [MIDINetworkConnection](/documentation/coremidi/midinetworkconnection)

#### Creating Connections

- [convenience init(host: MIDINetworkHost)](/documentation/coremidi/midinetworkconnection/init(host:))

#### Accessing Connections

- [var host: MIDINetworkHost](/documentation/coremidi/midinetworkconnection/host)
- [MIDINetworkSession](/documentation/coremidi/midinetworksession)

#### Configuring a Session

- [class func `default`() -> MIDINetworkSession](/documentation/coremidi/midinetworksession/default())
- [var isEnabled: Bool](/documentation/coremidi/midinetworksession/isenabled)
- [var connectionPolicy: MIDINetworkConnectionPolicy](/documentation/coremidi/midinetworksession/connectionpolicy)

##### Connection Policies

- [MIDINetworkConnectionPolicy](/documentation/coremidi/midinetworkconnectionpolicy)

###### Connection Policies

- [case noOne](/documentation/coremidi/midinetworkconnectionpolicy/noone)
- [case hostsInContactList](/documentation/coremidi/midinetworkconnectionpolicy/hostsincontactlist)
- [case anyone](/documentation/coremidi/midinetworkconnectionpolicy/anyone)

###### Initializers

- [init?(rawValue: UInt)](/documentation/coremidi/midinetworkconnectionpolicy/init(rawvalue:))

#### Inspecting a Sessions

- [var localName: String](/documentation/coremidi/midinetworksession/localname)
- [var networkName: String](/documentation/coremidi/midinetworksession/networkname)
- [var networkPort: Int](/documentation/coremidi/midinetworksession/networkport)
- [func sourceEndpoint() -> MIDIEndpointRef](/documentation/coremidi/midinetworksession/sourceendpoint())
- [func destinationEndpoint() -> MIDIEndpointRef](/documentation/coremidi/midinetworksession/destinationendpoint())

#### Managing Connections

- [func connections() -> Set<MIDINetworkConnection>](/documentation/coremidi/midinetworksession/connections())
- [func addConnection(MIDINetworkConnection) -> Bool](/documentation/coremidi/midinetworksession/addconnection(_:))
- [func removeConnection(MIDINetworkConnection) -> Bool](/documentation/coremidi/midinetworksession/removeconnection(_:))

#### Managing Contacts

- [func contacts() -> Set<MIDINetworkHost>](/documentation/coremidi/midinetworksession/contacts())
- [func addContact(MIDINetworkHost) -> Bool](/documentation/coremidi/midinetworksession/addcontact(_:))
- [func removeContact(MIDINetworkHost) -> Bool](/documentation/coremidi/midinetworksession/removecontact(_:))
- [let MIDINetworkNotificationContactsDidChange: String](/documentation/coremidi/midinetworknotificationcontactsdidchange)

#### Observing State Changes

- [let MIDINetworkNotificationSessionDidChange: String](/documentation/coremidi/midinetworknotificationsessiondidchange)
- [MIDI Drivers](/documentation/coremidi/midi-drivers)

### Managing Device Lifecyle

- [func MIDIDeviceCreate(MIDIDriverRef?, CFString, CFString, CFString, UnsafeMutablePointer<MIDIDeviceRef>) -> OSStatus](/documentation/coremidi/mididevicecreate(_:_:_:_:_:))
- [func MIDIDeviceDispose(MIDIDeviceRef) -> OSStatus](/documentation/coremidi/mididevicedispose(_:))
- [MIDIDeviceRef](/documentation/coremidi/midideviceref)

### Managing Device Lists

- [func MIDIDeviceListGetNumberOfDevices(MIDIDeviceListRef) -> Int](/documentation/coremidi/mididevicelistgetnumberofdevices(_:))
- [func MIDIDeviceListGetDevice(MIDIDeviceListRef, Int) -> MIDIDeviceRef](/documentation/coremidi/mididevicelistgetdevice(_:_:))
- [func MIDIDeviceListAddDevice(MIDIDeviceListRef, MIDIDeviceRef) -> OSStatus](/documentation/coremidi/mididevicelistadddevice(_:_:))
- [func MIDIDeviceListDispose(MIDIDeviceListRef) -> OSStatus](/documentation/coremidi/mididevicelistdispose(_:))
- [MIDIDeviceListRef](/documentation/coremidi/mididevicelistref)

### Inspecting a Driver

- [func MIDIGetDriverDeviceList(MIDIDriverRef) -> MIDIDeviceListRef](/documentation/coremidi/midigetdriverdevicelist(_:))
- [func MIDIDriverEnableMonitoring(MIDIDriverRef, Bool) -> OSStatus](/documentation/coremidi/mididriverenablemonitoring(_:_:))
- [func MIDIGetDriverIORunLoop() -> Unmanaged<CFRunLoop>](/documentation/coremidi/midigetdriveriorunloop())
- [let kMIDIDriverPropertyUsesSerial: CFString](/documentation/coremidi/kmididriverpropertyusesserial)
- [MIDIDriverInterface](/documentation/coremidi/mididriverinterface)

#### Properties

- [var FindDevices: (MIDIDriverRef, MIDIDeviceListRef) -> OSStatus](/documentation/coremidi/mididriverinterface/finddevices)
- [var Start: (MIDIDriverRef, MIDIDeviceListRef) -> OSStatus](/documentation/coremidi/mididriverinterface/start)
- [var Stop: (MIDIDriverRef) -> OSStatus](/documentation/coremidi/mididriverinterface/stop)
- [var Configure: (MIDIDriverRef, MIDIDeviceRef) -> OSStatus](/documentation/coremidi/mididriverinterface/configure)
- [var Send: (MIDIDriverRef, UnsafePointer<MIDIPacketList>, UnsafeMutableRawPointer, UnsafeMutableRawPointer) -> OSStatus](/documentation/coremidi/mididriverinterface/send)
- [var EnableSource: (MIDIDriverRef, MIDIEndpointRef, DarwinBoolean) -> OSStatus](/documentation/coremidi/mididriverinterface/enablesource)
- [var Flush: (MIDIDriverRef, MIDIEndpointRef, UnsafeMutableRawPointer?, UnsafeMutableRawPointer?) -> OSStatus](/documentation/coremidi/mididriverinterface/flush)
- [var Monitor: (MIDIDriverRef, MIDIEndpointRef, UnsafePointer<MIDIPacketList>) -> OSStatus](/documentation/coremidi/mididriverinterface/monitor)
- [var MonitorEvents: (MIDIDriverRef, MIDIEndpointRef, UnsafePointer<MIDIEventList>) -> OSStatus](/documentation/coremidi/mididriverinterface/monitorevents)
- [var SendPackets: (MIDIDriverRef, UnsafePointer<MIDIEventList>, UnsafeMutableRawPointer, UnsafeMutableRawPointer) -> OSStatus](/documentation/coremidi/mididriverinterface/sendpackets)
- [var AddRef: (UnsafeMutableRawPointer) -> ULONG](/documentation/coremidi/mididriverinterface/addref)
- [var QueryInterface: (UnsafeMutableRawPointer, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT](/documentation/coremidi/mididriverinterface/queryinterface)
- [var Release: (UnsafeMutableRawPointer) -> ULONG](/documentation/coremidi/mididriverinterface/release)
- [MIDIDriverRef](/documentation/coremidi/mididriverref)
- [MIDI Capability Inquiry](/documentation/coremidi/midi-capability-inquiry)

### Capability Inquiry

- [MIDICIDiscoveryManager](/documentation/coremidi/midicidiscoverymanager)

#### Accessing the Shared Instance

- [class func sharedInstance() -> MIDICIDiscoveryManager](/documentation/coremidi/midicidiscoverymanager/sharedinstance())

#### Discovering Nodes

- [func discover(handler: MIDICIDiscoveryResponseBlock)](/documentation/coremidi/midicidiscoverymanager/discover(handler:))

##### Handling Callbacks

- [MIDICIDiscoveryResponseBlock](/documentation/coremidi/midicidiscoveryresponseblock)
- [MIDICIDiscoveredNode](/documentation/coremidi/midicidiscoverednode)

###### Inspecting a Node

- [var destination: MIDIEntityRef](/documentation/coremidi/midicidiscoverednode/destination)
- [var deviceInfo: MIDICIDeviceInfo](/documentation/coremidi/midicidiscoverednode/deviceinfo)
- [var supportsProfiles: Bool](/documentation/coremidi/midicidiscoverednode/supportsprofiles)
- [var supportsProperties: Bool](/documentation/coremidi/midicidiscoverednode/supportsproperties)
- [var maximumSysExSize: NSNumber](/documentation/coremidi/midicidiscoverednode/maximumsysexsize)
- [MIDICISession](/documentation/coremidi/midicisession)

#### Creating a Session

- [init(discoveredNode: MIDICIDiscoveredNode, dataReadyHandler: () -> Void, disconnectHandler: MIDICISessionDisconnectBlock)](/documentation/coremidi/midicisession/init(discoverednode:datareadyhandler:disconnecthandler:))

##### Handling Callbacks

- [MIDICISessionDisconnectBlock](/documentation/coremidi/midicisessiondisconnectblock)

#### Configuring a Session

- [func profileState(forChannel: MIDIChannelNumber) -> MIDICIProfileState](/documentation/coremidi/midicisession/profilestate(forchannel:))
- [func enable(MIDICIProfile, onChannel: MIDIChannelNumber) throws](/documentation/coremidi/midicisession/enable(_:onchannel:))
- [func disableProfile(MIDICIProfile, onChannel: MIDIChannelNumber) throws](/documentation/coremidi/midicisession/disableprofile(_:onchannel:))
- [MIDICIProfileChangedBlock](/documentation/coremidi/midiciprofilechangedblock)
- [var profileChangedCallback: MIDICIProfileChangedBlock?](/documentation/coremidi/midicisession/profilechangedcallback)
- [func send(MIDICIProfile, onChannel: MIDIChannelNumber, profileData: Data) -> Bool](/documentation/coremidi/midicisession/send(_:onchannel:profiledata:))
- [MIDICIProfileSpecificDataBlock](/documentation/coremidi/midiciprofilespecificdatablock)
- [var profileSpecificDataHandler: MIDICIProfileSpecificDataBlock?](/documentation/coremidi/midicisession/profilespecificdatahandler)
- [let MIDIChannelsWholePort: MIDIChannelNumber](/documentation/coremidi/midichannelswholeport)

#### Inspecting a Session

- [var deviceInfo: MIDICIDeviceInfo](/documentation/coremidi/midicisession/deviceinfo)
- [var maxSysExSize: NSNumber](/documentation/coremidi/midicisession/maxsysexsize)
- [var midiDestination: MIDIEntityRef](/documentation/coremidi/midicisession/mididestination)
- [var maxPropertyRequests: NSNumber](/documentation/coremidi/midicisession/maxpropertyrequests)
- [var supportsProfileCapability: Bool](/documentation/coremidi/midicisession/supportsprofilecapability)
- [var supportsPropertyCapability: Bool](/documentation/coremidi/midicisession/supportspropertycapability)
- [MIDICIProfile](/documentation/coremidi/midiciprofile)

#### Creating a Profile

- [init(data: Data)](/documentation/coremidi/midiciprofile/init(data:))
- [init(data: Data, name: String)](/documentation/coremidi/midiciprofile/init(data:name:))

#### Inspecting a Profile

- [var name: String](/documentation/coremidi/midiciprofile/name)
- [var profileID: Data](/documentation/coremidi/midiciprofile/profileid)
- [MIDICIProfileState](/documentation/coremidi/midiciprofilestate)

#### Creating a Profile State

- [init(channel: MIDIChannelNumber, enabledProfiles: [MIDICIProfile], disabledProfiles: [MIDICIProfile])](/documentation/coremidi/midiciprofilestate/init(channel:enabledprofiles:disabledprofiles:))
- [init(enabledProfiles: [MIDICIProfile], disabledProfiles: [MIDICIProfile])](/documentation/coremidi/midiciprofilestate/init(enabledprofiles:disabledprofiles:))

#### Accessing the MIDI Channel

- [var midiChannel: MIDIChannelNumber](/documentation/coremidi/midiciprofilestate/midichannel)

#### Accessing Profiles

- [var enabledProfiles: [MIDICIProfile]](/documentation/coremidi/midiciprofilestate/enabledprofiles)
- [var disabledProfiles: [MIDICIProfile]](/documentation/coremidi/midiciprofilestate/disabledprofiles)
- [MIDICIResponder](/documentation/coremidi/midiciresponder)

#### Creating a Responder

- [init(deviceInfo: MIDICIDeviceInfo, profileDelegate: any MIDICIProfileResponderDelegate, profileStates: [MIDICIProfileState], supportProperties: Bool)](/documentation/coremidi/midiciresponder/init(deviceinfo:profiledelegate:profilestates:supportproperties:))

#### Managing the Life Cycle

- [func start() -> Bool](/documentation/coremidi/midiciresponder/start())
- [func stop()](/documentation/coremidi/midiciresponder/stop())

#### Setting a Responder Delegate

- [var profileDelegate: any MIDICIProfileResponderDelegate](/documentation/coremidi/midiciresponder/profiledelegate)
- [MIDICIProfileResponderDelegate](/documentation/coremidi/midiciprofileresponderdelegate)

##### Protocol Methods

- [func connectInitiator(MIDICIInitiatiorMUID, with: MIDICIDeviceInfo) -> Bool](/documentation/coremidi/midiciprofileresponderdelegate/connectinitiator(_:with:))
- [func handleData(for: MIDICIProfile, onChannel: MIDIChannelNumber, data: Data)](/documentation/coremidi/midiciprofileresponderdelegate/handledata(for:onchannel:data:))
- [func willSetProfile(MIDICIProfile, onChannel: MIDIChannelNumber, enabled: Bool) -> Bool](/documentation/coremidi/midiciprofileresponderdelegate/willsetprofile(_:onchannel:enabled:))
- [func initiatorDisconnected(MIDICIInitiatiorMUID)](/documentation/coremidi/midiciprofileresponderdelegate/initiatordisconnected(_:))

#### Inspecting a Responder

- [MIDICIInitiatiorMUID](/documentation/coremidi/midiciinitiatiormuid)
- [var initiators: [MIDICIInitiatiorMUID]](/documentation/coremidi/midiciresponder/initiators)
- [MIDICIDeviceIdentification](/documentation/coremidi/midicideviceidentification)

##### Configuring Device Identification

- [var manufacturer: (UInt8, UInt8, UInt8)](/documentation/coremidi/midicideviceidentification/manufacturer)
- [var modelNumber: (UInt8, UInt8)](/documentation/coremidi/midicideviceidentification/modelnumber)
- [var family: (UInt8, UInt8)](/documentation/coremidi/midicideviceidentification/family)
- [var revisionLevel: (UInt8, UInt8, UInt8, UInt8)](/documentation/coremidi/midicideviceidentification/revisionlevel)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/coremidi/midicideviceidentification/reserved)

##### Initializers

- [init()](/documentation/coremidi/midicideviceidentification/init())
- [init(manufacturer: (UInt8, UInt8, UInt8), family: (UInt8, UInt8), modelNumber: (UInt8, UInt8), revisionLevel: (UInt8, UInt8, UInt8, UInt8), reserved: (UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/coremidi/midicideviceidentification/init(manufacturer:family:modelnumber:revisionlevel:reserved:))
- [MIDICIDeviceInfo](/documentation/coremidi/midicideviceinfo)

##### Creating Device Information

- [init(destination: MIDIEntityRef, manufacturer: Data, family: Data, model: Data, revision: Data)](/documentation/coremidi/midicideviceinfo/init(destination:manufacturer:family:model:revision:))

##### Inspecting a Device

- [var manufacturerID: Data](/documentation/coremidi/midicideviceinfo/manufacturerid)
- [var family: Data](/documentation/coremidi/midicideviceinfo/family)
- [var modelNumber: Data](/documentation/coremidi/midicideviceinfo/modelnumber)
- [var revisionLevel: Data](/documentation/coremidi/midicideviceinfo/revisionlevel)
- [var midiDestination: MIDIEndpointRef](/documentation/coremidi/midicideviceinfo/mididestination)
- [var deviceInfo: MIDICIDeviceInfo](/documentation/coremidi/midiciresponder/deviceinfo)

#### Broadcasting Profile Changes

- [func notify(MIDICIProfile, onChannel: MIDIChannelNumber, isEnabled: Bool) -> Bool](/documentation/coremidi/midiciresponder/notify(_:onchannel:isenabled:))
- [func send(MIDICIProfile, onChannel: MIDIChannelNumber, profileData: Data) -> Bool](/documentation/coremidi/midiciresponder/send(_:onchannel:profiledata:))

## Reference

- [Core MIDI Structures](/documentation/coremidi/core-midi-structures)

### Structures

- [MIDI2DeviceManufacturer](/documentation/coremidi/midi2devicemanufacturer)

#### Initializers

- [init()](/documentation/coremidi/midi2devicemanufacturer/init())
- [init(sysExIDByte: (UInt8, UInt8, UInt8))](/documentation/coremidi/midi2devicemanufacturer/init(sysexidbyte:))

#### Instance Properties

- [var sysExIDByte: (UInt8, UInt8, UInt8)](/documentation/coremidi/midi2devicemanufacturer/sysexidbyte)
- [MIDI2DeviceRevisionLevel](/documentation/coremidi/midi2devicerevisionlevel)

#### Initializers

- [init()](/documentation/coremidi/midi2devicerevisionlevel/init())
- [init(revisionLevel: (UInt8, UInt8, UInt8, UInt8))](/documentation/coremidi/midi2devicerevisionlevel/init(revisionlevel:))

#### Instance Properties

- [var revisionLevel: (UInt8, UInt8, UInt8, UInt8)](/documentation/coremidi/midi2devicerevisionlevel/revisionlevel)
- [MIDICIProfileID](/documentation/coremidi/midiciprofileid)

#### Initializers

- [init()](/documentation/coremidi/midiciprofileid/init())
- [init(manufacturerSpecific: MIDICIProfileIDManufacturerSpecific)](/documentation/coremidi/midiciprofileid/init(manufacturerspecific:))
- [init(standard: MIDICIProfileIDStandard)](/documentation/coremidi/midiciprofileid/init(standard:))

#### Instance Properties

- [var manufacturerSpecific: MIDICIProfileIDManufacturerSpecific](/documentation/coremidi/midiciprofileid/manufacturerspecific)
- [var standard: MIDICIProfileIDStandard](/documentation/coremidi/midiciprofileid/standard)
- [MIDICIProfileIDManufacturerSpecific](/documentation/coremidi/midiciprofileidmanufacturerspecific)

#### Initializers

- [init()](/documentation/coremidi/midiciprofileidmanufacturerspecific/init())
- [init(sysExID1: MIDIUInteger7, sysExID2: MIDIUInteger7, sysExID3: MIDIUInteger7, info1: MIDIUInteger7, info2: MIDIUInteger7)](/documentation/coremidi/midiciprofileidmanufacturerspecific/init(sysexid1:sysexid2:sysexid3:info1:info2:))

#### Instance Properties

- [var info1: MIDIUInteger7](/documentation/coremidi/midiciprofileidmanufacturerspecific/info1)
- [var info2: MIDIUInteger7](/documentation/coremidi/midiciprofileidmanufacturerspecific/info2)
- [var sysExID1: MIDIUInteger7](/documentation/coremidi/midiciprofileidmanufacturerspecific/sysexid1)
- [var sysExID2: MIDIUInteger7](/documentation/coremidi/midiciprofileidmanufacturerspecific/sysexid2)
- [var sysExID3: MIDIUInteger7](/documentation/coremidi/midiciprofileidmanufacturerspecific/sysexid3)
- [MIDICIProfileIDStandard](/documentation/coremidi/midiciprofileidstandard)

#### Initializers

- [init()](/documentation/coremidi/midiciprofileidstandard/init())
- [init(profileIDByte1: MIDIUInteger7, profileBank: MIDIUInteger7, profileNumber: MIDIUInteger7, profileVersion: MIDIUInteger7, profileLevel: MIDIUInteger7)](/documentation/coremidi/midiciprofileidstandard/init(profileidbyte1:profilebank:profilenumber:profileversion:profilelevel:))

#### Instance Properties

- [var profileBank: MIDIUInteger7](/documentation/coremidi/midiciprofileidstandard/profilebank)
- [var profileIDByte1: MIDIUInteger7](/documentation/coremidi/midiciprofileidstandard/profileidbyte1)
- [var profileLevel: MIDIUInteger7](/documentation/coremidi/midiciprofileidstandard/profilelevel)
- [var profileNumber: MIDIUInteger7](/documentation/coremidi/midiciprofileidstandard/profilenumber)
- [var profileVersion: MIDIUInteger7](/documentation/coremidi/midiciprofileidstandard/profileversion)
- [MIDIUniversalMessage](/documentation/coremidi/midiuniversalmessage)

#### Initializers

- [init()](/documentation/coremidi/midiuniversalmessage/init())

#### Instance Properties

- [var channelVoice1: MIDIUniversalMessage.__Unnamed_union___Anonymous_field3.__Unnamed_struct_channelVoice1](/documentation/coremidi/midiuniversalmessage/channelvoice1-3muv1)
- [var channelVoice2: MIDIUniversalMessage.__Unnamed_union___Anonymous_field3.__Unnamed_struct_channelVoice2](/documentation/coremidi/midiuniversalmessage/channelvoice2-3muv2)
- [var data128: MIDIUniversalMessage.__Unnamed_union___Anonymous_field3.__Unnamed_struct_data128](/documentation/coremidi/midiuniversalmessage/data128-3jrad)
- [var group: UInt8](/documentation/coremidi/midiuniversalmessage/group)
- [var reserved: (UInt8, UInt8, UInt8)](/documentation/coremidi/midiuniversalmessage/reserved)
- [var sysEx: MIDIUniversalMessage.__Unnamed_union___Anonymous_field3.__Unnamed_struct_sysEx](/documentation/coremidi/midiuniversalmessage/sysex-2jr6w)
- [var system: MIDIUniversalMessage.__Unnamed_union___Anonymous_field3.__Unnamed_struct_system](/documentation/coremidi/midiuniversalmessage/system-6vxkw)
- [var type: MIDIMessageType](/documentation/coremidi/midiuniversalmessage/type)
- [var unknown: MIDIUniversalMessage.__Unnamed_union___Anonymous_field3.__Unnamed_struct_unknown](/documentation/coremidi/midiuniversalmessage/unknown-9rrub)
- [var utility: MIDIUniversalMessage.__Unnamed_union___Anonymous_field3.__Unnamed_struct_utility](/documentation/coremidi/midiuniversalmessage/utility-1trwz)
- [Core MIDI Enumerations](/documentation/coremidi/core-midi-enumerations)

### Enumerations

- [var kMIDIInvalidUniqueID: MIDIUniqueID](/documentation/coremidi/kmidiinvaliduniqueid)
- [MIDICICategoryOptions](/documentation/coremidi/midicicategoryoptions)

#### Initializers

- [init(rawValue: MIDIUInteger7)](/documentation/coremidi/midicicategoryoptions/init(rawvalue:))

#### Type Properties

- [static var processInquirySupported: MIDICICategoryOptions](/documentation/coremidi/midicicategoryoptions/processinquirysupported)
- [static var profileConfigurationSupported: MIDICICategoryOptions](/documentation/coremidi/midicicategoryoptions/profileconfigurationsupported)
- [static var propertyExchangeSupported: MIDICICategoryOptions](/documentation/coremidi/midicicategoryoptions/propertyexchangesupported)
- [static var protocolNegotiation: MIDICICategoryOptions](/documentation/coremidi/midicicategoryoptions/protocolnegotiation)
- [MIDICIDeviceType](/documentation/coremidi/midicidevicetype)

#### Enumeration Cases

- [case legacyMIDI1](/documentation/coremidi/midicidevicetype/legacymidi1)
- [case unknown](/documentation/coremidi/midicidevicetype/unknown)
- [case usbMIDI](/documentation/coremidi/midicidevicetype/usbmidi)
- [case virtual](/documentation/coremidi/midicidevicetype/virtual)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coremidi/midicidevicetype/init(rawvalue:))
- [MIDICIManagementMessageType](/documentation/coremidi/midicimanagementmessagetype)

#### Enumeration Cases

- [case discovery](/documentation/coremidi/midicimanagementmessagetype/discovery)
- [case inquiryEndpointInformation](/documentation/coremidi/midicimanagementmessagetype/inquiryendpointinformation)
- [case invalidateMUID](/documentation/coremidi/midicimanagementmessagetype/invalidatemuid)
- [case midiCIACK](/documentation/coremidi/midicimanagementmessagetype/midiciack)
- [case midiNAK](/documentation/coremidi/midicimanagementmessagetype/midinak)
- [case replyToDiscovery](/documentation/coremidi/midicimanagementmessagetype/replytodiscovery)
- [case replyToEndpointInformation](/documentation/coremidi/midicimanagementmessagetype/replytoendpointinformation)

#### Initializers

- [init?(rawValue: MIDIUInteger7)](/documentation/coremidi/midicimanagementmessagetype/init(rawvalue:))
- [MIDICIProcessInquiryMessageType](/documentation/coremidi/midiciprocessinquirymessagetype)

#### Enumeration Cases

- [case endOfMIDIMessageReport](/documentation/coremidi/midiciprocessinquirymessagetype/endofmidimessagereport)
- [case inquiryMIDIMessageReport](/documentation/coremidi/midiciprocessinquirymessagetype/inquirymidimessagereport)
- [case inquiryProcessInquiryCapabilities](/documentation/coremidi/midiciprocessinquirymessagetype/inquiryprocessinquirycapabilities)
- [case replyToMIDIMessageReport](/documentation/coremidi/midiciprocessinquirymessagetype/replytomidimessagereport)
- [case replyToProcessInquiryCapabilities](/documentation/coremidi/midiciprocessinquirymessagetype/replytoprocessinquirycapabilities)

#### Initializers

- [init?(rawValue: MIDIUInteger7)](/documentation/coremidi/midiciprocessinquirymessagetype/init(rawvalue:))
- [MIDICIProfileMessageType](/documentation/coremidi/midiciprofilemessagetype)

#### Enumeration Cases

- [case detailsInquiry](/documentation/coremidi/midiciprofilemessagetype/detailsinquiry)
- [case profileAdded](/documentation/coremidi/midiciprofilemessagetype/profileadded)
- [case profileDisabledReport](/documentation/coremidi/midiciprofilemessagetype/profiledisabledreport)
- [case profileEnabledReport](/documentation/coremidi/midiciprofilemessagetype/profileenabledreport)
- [case profileInquiry](/documentation/coremidi/midiciprofilemessagetype/profileinquiry)
- [case profileRemoved](/documentation/coremidi/midiciprofilemessagetype/profileremoved)
- [case profileSpecificData](/documentation/coremidi/midiciprofilemessagetype/profilespecificdata)
- [case replyToDetailsInquiry](/documentation/coremidi/midiciprofilemessagetype/replytodetailsinquiry)
- [case replyToProfileInquiry](/documentation/coremidi/midiciprofilemessagetype/replytoprofileinquiry)
- [case setProfileOff](/documentation/coremidi/midiciprofilemessagetype/setprofileoff)
- [case setProfileOn](/documentation/coremidi/midiciprofilemessagetype/setprofileon)

#### Initializers

- [init?(rawValue: MIDIUInteger7)](/documentation/coremidi/midiciprofilemessagetype/init(rawvalue:))
- [MIDICIProfileType](/documentation/coremidi/midiciprofiletype)

#### Enumeration Cases

- [case functionBlock](/documentation/coremidi/midiciprofiletype/functionblock)
- [case group](/documentation/coremidi/midiciprofiletype/group)
- [case multichannel](/documentation/coremidi/midiciprofiletype/multichannel)
- [case singleChannel](/documentation/coremidi/midiciprofiletype/singlechannel)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coremidi/midiciprofiletype/init(rawvalue:))
- [MIDICIPropertyExchangeMessageType](/documentation/coremidi/midicipropertyexchangemessagetype)

#### Enumeration Cases

- [case inquiryGetPropertyData](/documentation/coremidi/midicipropertyexchangemessagetype/inquirygetpropertydata)
- [case inquiryHasPropertyData_Reserved](/documentation/coremidi/midicipropertyexchangemessagetype/inquiryhaspropertydata_reserved)
- [case inquiryPropertyExchangeCapabilities](/documentation/coremidi/midicipropertyexchangemessagetype/inquirypropertyexchangecapabilities)
- [case inquiryReplyToHasPropertyData_Reserved](/documentation/coremidi/midicipropertyexchangemessagetype/inquiryreplytohaspropertydata_reserved)
- [case inquirySetPropertyData](/documentation/coremidi/midicipropertyexchangemessagetype/inquirysetpropertydata)
- [case notify](/documentation/coremidi/midicipropertyexchangemessagetype/notify)
- [case replyToGetProperty](/documentation/coremidi/midicipropertyexchangemessagetype/replytogetproperty)
- [case replyToPropertyExchangeCapabilities](/documentation/coremidi/midicipropertyexchangemessagetype/replytopropertyexchangecapabilities)
- [case replyToSetPropertyData](/documentation/coremidi/midicipropertyexchangemessagetype/replytosetpropertydata)
- [case replyToSubscription](/documentation/coremidi/midicipropertyexchangemessagetype/replytosubscription)
- [case subscription](/documentation/coremidi/midicipropertyexchangemessagetype/subscription)

#### Initializers

- [init?(rawValue: MIDIUInteger7)](/documentation/coremidi/midicipropertyexchangemessagetype/init(rawvalue:))
- [MIDINetworkConnectionPolicy](/documentation/coremidi/midinetworkconnectionpolicy)

#### Connection Policies

- [case noOne](/documentation/coremidi/midinetworkconnectionpolicy/noone)
- [case hostsInContactList](/documentation/coremidi/midinetworkconnectionpolicy/hostsincontactlist)
- [case anyone](/documentation/coremidi/midinetworkconnectionpolicy/anyone)

#### Initializers

- [init?(rawValue: UInt)](/documentation/coremidi/midinetworkconnectionpolicy/init(rawvalue:))
- [MIDINoteAttribute](/documentation/coremidi/midinoteattribute)

#### Enumeration Cases

- [case manufacturerSpecific](/documentation/coremidi/midinoteattribute/manufacturerspecific)
- [case none](/documentation/coremidi/midinoteattribute/none)
- [case pitch](/documentation/coremidi/midinoteattribute/pitch)
- [case profileSpecific](/documentation/coremidi/midinoteattribute/profilespecific)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coremidi/midinoteattribute/init(rawvalue:))
- [MIDIPerNoteManagementOptions](/documentation/coremidi/midipernotemanagementoptions)

#### Initializers

- [init(rawValue: UInt8)](/documentation/coremidi/midipernotemanagementoptions/init(rawvalue:))

#### Type Properties

- [static var detach: MIDIPerNoteManagementOptions](/documentation/coremidi/midipernotemanagementoptions/detach)
- [static var reset: MIDIPerNoteManagementOptions](/documentation/coremidi/midipernotemanagementoptions/reset)
- [MIDIProgramChangeOptions](/documentation/coremidi/midiprogramchangeoptions)

#### Initializers

- [init(rawValue: UInt8)](/documentation/coremidi/midiprogramchangeoptions/init(rawvalue:))

#### Type Properties

- [static var bankValid: MIDIProgramChangeOptions](/documentation/coremidi/midiprogramchangeoptions/bankvalid)
- [MIDIUMPCIObjectBackingType](/documentation/coremidi/midiumpciobjectbackingtype)

#### Enumeration Cases

- [case driverDevice](/documentation/coremidi/midiumpciobjectbackingtype/driverdevice)
- [case unknown](/documentation/coremidi/midiumpciobjectbackingtype/unknown)
- [case usbMIDI](/documentation/coremidi/midiumpciobjectbackingtype/usbmidi)
- [case virtual](/documentation/coremidi/midiumpciobjectbackingtype/virtual)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coremidi/midiumpciobjectbackingtype/init(rawvalue:))
- [MIDIUMPFunctionBlockDirection](/documentation/coremidi/midiumpfunctionblockdirection)

#### Enumeration Cases

- [case bidirectional](/documentation/coremidi/midiumpfunctionblockdirection/bidirectional)
- [case input](/documentation/coremidi/midiumpfunctionblockdirection/input)
- [case output](/documentation/coremidi/midiumpfunctionblockdirection/output)
- [case unknown](/documentation/coremidi/midiumpfunctionblockdirection/unknown)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coremidi/midiumpfunctionblockdirection/init(rawvalue:))
- [MIDIUMPFunctionBlockMIDI1Info](/documentation/coremidi/midiumpfunctionblockmidi1info)

#### Enumeration Cases

- [case notMIDI1](/documentation/coremidi/midiumpfunctionblockmidi1info/notmidi1)
- [case restrictedBandwidth](/documentation/coremidi/midiumpfunctionblockmidi1info/restrictedbandwidth)
- [case unrestrictedBandwidth](/documentation/coremidi/midiumpfunctionblockmidi1info/unrestrictedbandwidth)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coremidi/midiumpfunctionblockmidi1info/init(rawvalue:))
- [MIDIUMPFunctionBlockUIHint](/documentation/coremidi/midiumpfunctionblockuihint)

#### Enumeration Cases

- [case receiver](/documentation/coremidi/midiumpfunctionblockuihint/receiver)
- [case sender](/documentation/coremidi/midiumpfunctionblockuihint/sender)
- [case senderReceiver](/documentation/coremidi/midiumpfunctionblockuihint/senderreceiver)
- [case unknown](/documentation/coremidi/midiumpfunctionblockuihint/unknown)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coremidi/midiumpfunctionblockuihint/init(rawvalue:))
- [MIDIUMPProtocolOptions](/documentation/coremidi/midiumpprotocoloptions)

#### Initializers

- [init(rawValue: MIDIUInteger4)](/documentation/coremidi/midiumpprotocoloptions/init(rawvalue:))

#### Type Properties

- [static var midi1: MIDIUMPProtocolOptions](/documentation/coremidi/midiumpprotocoloptions/midi1)
- [static var midi2: MIDIUMPProtocolOptions](/documentation/coremidi/midiumpprotocoloptions/midi2)
- [MIDIUtilityStatus](/documentation/coremidi/midiutilitystatus)

#### Enumeration Cases

- [case NOOP](/documentation/coremidi/midiutilitystatus/noop)
- [case deltaClockstampTicksPerQuarterNote](/documentation/coremidi/midiutilitystatus/deltaclockstampticksperquarternote)
- [case jitterReductionClock](/documentation/coremidi/midiutilitystatus/jitterreductionclock)
- [case jitterReductionTimestamp](/documentation/coremidi/midiutilitystatus/jitterreductiontimestamp)
- [case ticksSinceLastEvent](/documentation/coremidi/midiutilitystatus/tickssincelastevent)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coremidi/midiutilitystatus/init(rawvalue:))
- [UMPStreamMessageFormat](/documentation/coremidi/umpstreammessageformat)

#### Enumeration Cases

- [case complete](/documentation/coremidi/umpstreammessageformat/complete)
- [case continuing](/documentation/coremidi/umpstreammessageformat/continuing)
- [case end](/documentation/coremidi/umpstreammessageformat/end)
- [case start](/documentation/coremidi/umpstreammessageformat/start)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coremidi/umpstreammessageformat/init(rawvalue:))
- [UMPStreamMessageStatus](/documentation/coremidi/umpstreammessagestatus)

#### Enumeration Cases

- [case deviceIdentityNotification](/documentation/coremidi/umpstreammessagestatus/deviceidentitynotification)
- [case endOfClip](/documentation/coremidi/umpstreammessagestatus/endofclip)
- [case endpointDiscovery](/documentation/coremidi/umpstreammessagestatus/endpointdiscovery)
- [case endpointInfoNotification](/documentation/coremidi/umpstreammessagestatus/endpointinfonotification)
- [case endpointNameNotification](/documentation/coremidi/umpstreammessagestatus/endpointnamenotification)
- [case functionBlockDiscovery](/documentation/coremidi/umpstreammessagestatus/functionblockdiscovery)
- [case functionBlockInfoNotification](/documentation/coremidi/umpstreammessagestatus/functionblockinfonotification)
- [case functionBlockNameNotification](/documentation/coremidi/umpstreammessagestatus/functionblocknamenotification)
- [case productInstanceIDNotification](/documentation/coremidi/umpstreammessagestatus/productinstanceidnotification)
- [case startOfClip](/documentation/coremidi/umpstreammessagestatus/startofclip)
- [case streamConfigurationNotification](/documentation/coremidi/umpstreammessagestatus/streamconfigurationnotification)
- [case streamConfigurationRequest](/documentation/coremidi/umpstreammessagestatus/streamconfigurationrequest)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coremidi/umpstreammessagestatus/init(rawvalue:))
- [Core MIDI Constants](/documentation/coremidi/core-midi-constants)

### Constants

- [let kMIDI1UPMaxSysexSize: UInt8](/documentation/coremidi/kmidi1upmaxsysexsize)
- [let kMIDIDeviceIDFunctionBlock: MIDICIDeviceID](/documentation/coremidi/kmidideviceidfunctionblock)
- [let kMIDIDeviceIDUMPGroup: MIDICIDeviceID](/documentation/coremidi/kmidideviceidumpgroup)
- [let kMIDIPropertyAssociatedEndpoint: CFString](/documentation/coremidi/kmidipropertyassociatedendpoint)
- [let kMIDIPropertyUMPActiveGroupBitmap: CFString](/documentation/coremidi/kmidipropertyumpactivegroupbitmap)
- [let kMIDIPropertyUMPCanTransmitGroupless: CFString](/documentation/coremidi/kmidipropertyumpcantransmitgroupless)
- [let kMIDIUInteger14Max: MIDIUInteger14](/documentation/coremidi/kmidiuinteger14max)
- [let kMIDIUInteger28Max: MIDIUInteger28](/documentation/coremidi/kmidiuinteger28max)
- [let kMIDIUInteger2Max: MIDIUInteger2](/documentation/coremidi/kmidiuinteger2max)
- [let kMIDIUInteger4Max: MIDIUInteger4](/documentation/coremidi/kmidiuinteger4max)
- [let kMIDIUInteger7Max: MIDIUInteger7](/documentation/coremidi/kmidiuinteger7max)
- [Core MIDI Functions](/documentation/coremidi/core-midi-functions)

### Functions

- [func MIDI1UPChannelPressure(UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1upchannelpressure(_:_:_:))
- [func MIDI1UPPolyPressure(UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1uppolypressure(_:_:_:_:))
- [func MIDI1UPProgramChange(UInt8, UInt8, UInt8) -> MIDIMessage_32](/documentation/coremidi/midi1upprogramchange(_:_:_:))
- [func MIDI1UPSysEx(UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_64](/documentation/coremidi/midi1upsysex(_:_:_:_:_:_:_:_:_:))
- [func MIDI1UPSysExArray(UInt8, UInt8, UnsafePointer<UInt8>!, UnsafePointer<UInt8>!) -> MIDIMessage_64](/documentation/coremidi/midi1upsysexarray(_:_:_:_:))
- [func MIDI2EndOfClipMessage() -> MIDIMessage_128](/documentation/coremidi/midi2endofclipmessage())
- [func MIDI2EndpointDeviceIdentityNotificationMessage(MIDIUInteger7, MIDIUInteger7, MIDIUInteger7, MIDIUInteger14, MIDIUInteger14, MIDIUInteger28) -> MIDIMessage_128](/documentation/coremidi/midi2endpointdeviceidentitynotificationmessage(_:_:_:_:_:_:))
- [func MIDI2EndpointDiscoveryMessage(UInt8, UInt8, Bool, Bool, Bool, Bool, Bool) -> MIDIMessage_128](/documentation/coremidi/midi2endpointdiscoverymessage(_:_:_:_:_:_:_:))
- [func MIDI2EndpointInfoNotificationMessage(UInt8, UInt8, Bool, UInt8, Bool, Bool, Bool, Bool) -> MIDIMessage_128](/documentation/coremidi/midi2endpointinfonotificationmessage(_:_:_:_:_:_:_:_:))
- [func MIDI2EndpointNameNotificationMessage(UMPStreamMessageFormat, UnsafePointer<CChar>!, Int) -> MIDIMessage_128](/documentation/coremidi/midi2endpointnamenotificationmessage(_:_:_:))
- [func MIDI2EndpointProductInstanceIDNotificationMessage(UMPStreamMessageFormat, UnsafePointer<CChar>!, Int) -> MIDIMessage_128](/documentation/coremidi/midi2endpointproductinstanceidnotificationmessage(_:_:_:))
- [func MIDI2FlexDataMessage(MIDIUInteger4, MIDIUInteger2, MIDIUInteger2, MIDIUInteger4, UInt8, UInt8, UInt32, UInt32, UInt32) -> MIDIMessage_128](/documentation/coremidi/midi2flexdatamessage(_:_:_:_:_:_:_:_:_:))
- [func MIDI2FunctionBlockDiscoveryMessage(UInt8, Bool, Bool) -> MIDIMessage_128](/documentation/coremidi/midi2functionblockdiscoverymessage(_:_:_:))
- [func MIDI2FunctionBlockInfoNotificationMessage(Bool, MIDIUInteger7, MIDIUMPFunctionBlockUIHint, MIDIUMPFunctionBlockMIDI1Info, MIDIUMPFunctionBlockDirection, UInt8, UInt8, UInt8, UInt8) -> MIDIMessage_128](/documentation/coremidi/midi2functionblockinfonotificationmessage(_:_:_:_:_:_:_:_:_:))
- [func MIDI2FunctionBlockNameNotificationMessage(UMPStreamMessageFormat, UInt8, UnsafePointer<CChar>!, Int) -> MIDIMessage_128](/documentation/coremidi/midi2functionblocknamenotificationmessage(_:_:_:_:))
- [func MIDI2StartOfClipMessage() -> MIDIMessage_128](/documentation/coremidi/midi2startofclipmessage())
- [func MIDI2StreamConfigurationNotificationMessage(UInt8, Bool, Bool) -> MIDIMessage_128](/documentation/coremidi/midi2streamconfigurationnotificationmessage(_:_:_:))
- [func MIDI2StreamConfigurationRequestMessage(UInt8, Bool, Bool) -> MIDIMessage_128](/documentation/coremidi/midi2streamconfigurationrequestmessage(_:_:_:))
- [func MIDI2StreamMessage(UMPStreamMessageFormat, UMPStreamMessageStatus, UInt16, UInt32, UInt32, UInt32) -> MIDIMessage_128](/documentation/coremidi/midi2streammessage(_:_:_:_:_:_:))
- [func MIDI2StreamMessageFromData(UMPStreamMessageFormat, UMPStreamMessageStatus, UnsafePointer<UInt8>!, Int) -> MIDIMessage_128](/documentation/coremidi/midi2streammessagefromdata(_:_:_:_:))
- [func MIDIDeltaClockstampTicksPerQuarterNoteMessage(UInt16) -> MIDIMessage_32](/documentation/coremidi/midideltaclockstampticksperquarternotemessage(_:))
- [func MIDIDeviceAddEntity(MIDIDeviceRef, CFString, Bool, Int, Int, UnsafeMutablePointer<MIDIEntityRef>) -> OSStatus](/documentation/coremidi/midideviceaddentity(_:_:_:_:_:_:))
- [func MIDIEventListForEachEvent(UnsafePointer<MIDIEventList>!, MIDIEventVisitor!, UnsafeMutableRawPointer!)](/documentation/coremidi/midieventlistforeachevent(_:_:_:))
- [func MIDIJitterReductionClockMessage(UInt16) -> MIDIMessage_32](/documentation/coremidi/midijitterreductionclockmessage(_:))
- [func MIDIJitterReductionTimestampMessage(UInt16) -> MIDIMessage_32](/documentation/coremidi/midijitterreductiontimestampmessage(_:))
- [func MIDINoOpMessage() -> MIDIMessage_32](/documentation/coremidi/midinoopmessage())
- [func MIDITicksSinceLastEventMessage(UInt32) -> MIDIMessage_32](/documentation/coremidi/miditickssincelasteventmessage(_:))
- [Core MIDI Data Types](/documentation/coremidi/core-midi-data-types)

### Data Types

- [MIDICIDeviceID](/documentation/coremidi/midicideviceid)
- [MIDICIDeviceManager.DictionaryKey](/documentation/coremidi/midicidevicemanager/dictionarykey)

#### Type Properties

- [static let deviceObject: MIDICIDeviceManager.DictionaryKey](/documentation/coremidi/midicidevicemanager/dictionarykey/deviceobject)
- [static let profileObject: MIDICIDeviceManager.DictionaryKey](/documentation/coremidi/midicidevicemanager/dictionarykey/profileobject)

#### Initializers

- [init(rawValue: String)](/documentation/coremidi/midicidevicemanager/dictionarykey/init(rawvalue:))
- [MIDICIMUID](/documentation/coremidi/midicimuid)
- [MIDICIPropertyExchangeRequestID](/documentation/coremidi/midicipropertyexchangerequestid)

#### Initializers

- [init(UInt8)](/documentation/coremidi/midicipropertyexchangerequestid/init(_:))
- [init(rawValue: UInt8)](/documentation/coremidi/midicipropertyexchangerequestid/init(rawvalue:))
- [MIDIEventVisitor](/documentation/coremidi/midieventvisitor)
- [MIDIUInteger14](/documentation/coremidi/midiuinteger14)
- [MIDIUInteger2](/documentation/coremidi/midiuinteger2)
- [MIDIUInteger28](/documentation/coremidi/midiuinteger28)
- [MIDIUInteger4](/documentation/coremidi/midiuinteger4)
- [MIDIUInteger7](/documentation/coremidi/midiuinteger7)
- [MIDIUMPEndpointManager.DictionaryKey](/documentation/coremidi/midiumpendpointmanager/dictionarykey)

#### Initializers

- [init(rawValue: String)](/documentation/coremidi/midiumpendpointmanager/dictionarykey/init(rawvalue:))
- [MIDIUMPFunctionBlockID](/documentation/coremidi/midiumpfunctionblockid)
- [MIDIUMPGroupNumber](/documentation/coremidi/midiumpgroupnumber)
- [MIDICIDiscoveryResponseBlock](/documentation/coremidi/midicidiscoveryresponseblock)
- [MIDICISessionDisconnectBlock](/documentation/coremidi/midicisessiondisconnectblock)
- [MIDIChannelNumber](/documentation/coremidi/midichannelnumber)
- [MIDISetupRef](/documentation/coremidi/midisetupref)
- [Core MIDI Macros](/documentation/coremidi/coremidi-macros)

### Macros

- [static var badRequestID: MIDICIPropertyExchangeRequestID](/documentation/coremidi/midicipropertyexchangerequestid/badrequestid)
- [static let endpointObject: MIDIUMPEndpointManager.DictionaryKey](/documentation/coremidi/midiumpendpointmanager/dictionarykey/endpointobject)
- [static let functionBlockObject: MIDIUMPEndpointManager.DictionaryKey](/documentation/coremidi/midiumpendpointmanager/dictionarykey/functionblockobject)

## Articles

- [Deprecated Symbols](/documentation/coremidi/midi_system_setup-deprecated-symbols)

### Managing System Setup

- [MIDISetupRef](/documentation/coremidi/midisetupref)

### Managing MIDI Devices

- [func MIDIDeviceAddEntity(MIDIDeviceRef, CFString, Bool, Int, Int, UnsafeMutablePointer<MIDIEntityRef>) -> OSStatus](/documentation/coremidi/midideviceaddentity(_:_:_:_:_:_:))
- [let kMIDIObjectType_ExternalMask: MIDIObjectType](/documentation/coremidi/kmidiobjecttype_externalmask)

## Classes

- [MIDI2DeviceInfo](/documentation/coremidi/midi2deviceinfo)

### Initializers

- [init(manufacturerID: MIDI2DeviceManufacturer, family: MIDIUInteger14, modelNumber: MIDIUInteger14, revisionLevel: MIDI2DeviceRevisionLevel)](/documentation/coremidi/midi2deviceinfo/init(manufacturerid:family:modelnumber:revisionlevel:))

### Instance Properties

- [var family: MIDIUInteger14](/documentation/coremidi/midi2deviceinfo/family)
- [var manufacturerID: MIDI2DeviceManufacturer](/documentation/coremidi/midi2deviceinfo/manufacturerid)
- [var modelNumber: MIDIUInteger14](/documentation/coremidi/midi2deviceinfo/modelnumber)
- [var revisionLevel: MIDI2DeviceRevisionLevel](/documentation/coremidi/midi2deviceinfo/revisionlevel)
- [MIDICIDevice](/documentation/coremidi/midicidevice)

### Instance Properties

- [var deviceInfo: MIDI2DeviceInfo](/documentation/coremidi/midicidevice/deviceinfo)
- [var deviceType: MIDICIDeviceType](/documentation/coremidi/midicidevice/devicetype)
- [var maxPropertyExchangeRequests: Int](/documentation/coremidi/midicidevice/maxpropertyexchangerequests)
- [var maxSysExSize: Int](/documentation/coremidi/midicidevice/maxsysexsize)
- [var muid: MIDICIMUID](/documentation/coremidi/midicidevice/muid)
- [var profiles: [MIDIUMPCIProfile]](/documentation/coremidi/midicidevice/profiles)
- [var supportsProcessInquiry: Bool](/documentation/coremidi/midicidevice/supportsprocessinquiry)
- [var supportsProfileConfiguration: Bool](/documentation/coremidi/midicidevice/supportsprofileconfiguration)
- [var supportsPropertyExchange: Bool](/documentation/coremidi/midicidevice/supportspropertyexchange)
- [var supportsProtocolNegotiation: Bool](/documentation/coremidi/midicidevice/supportsprotocolnegotiation)
- [MIDICIDeviceManager](/documentation/coremidi/midicidevicemanager)

### Type Aliases

- [MIDICIDeviceManager.DictionaryKey](/documentation/coremidi/midicidevicemanager/dictionarykey)

#### Type Properties

- [static let deviceObject: MIDICIDeviceManager.DictionaryKey](/documentation/coremidi/midicidevicemanager/dictionarykey/deviceobject)
- [static let profileObject: MIDICIDeviceManager.DictionaryKey](/documentation/coremidi/midicidevicemanager/dictionarykey/profileobject)

#### Initializers

- [init(rawValue: String)](/documentation/coremidi/midicidevicemanager/dictionarykey/init(rawvalue:))

### Instance Properties

- [var discoveredCIDevices: [MIDICIDevice]](/documentation/coremidi/midicidevicemanager/discoveredcidevices)

### Type Properties

- [class let deviceWasAddedNotification: NSNotification.Name](/documentation/coremidi/midicidevicemanager/devicewasaddednotification)
- [class let deviceWasRemovedNotification: NSNotification.Name](/documentation/coremidi/midicidevicemanager/devicewasremovednotification)
- [class let profileWasRemovedNotification: NSNotification.Name](/documentation/coremidi/midicidevicemanager/profilewasremovednotification)
- [class let profileWasUpdatedNotification: NSNotification.Name](/documentation/coremidi/midicidevicemanager/profilewasupdatednotification)
- [class var shared: MIDICIDeviceManager](/documentation/coremidi/midicidevicemanager/shared)
- [MIDICIDiscoveredNode](/documentation/coremidi/midicidiscoverednode)

### Inspecting a Node

- [var destination: MIDIEntityRef](/documentation/coremidi/midicidiscoverednode/destination)
- [var deviceInfo: MIDICIDeviceInfo](/documentation/coremidi/midicidiscoverednode/deviceinfo)
- [var supportsProfiles: Bool](/documentation/coremidi/midicidiscoverednode/supportsprofiles)
- [var supportsProperties: Bool](/documentation/coremidi/midicidiscoverednode/supportsproperties)
- [var maximumSysExSize: NSNumber](/documentation/coremidi/midicidiscoverednode/maximumsysexsize)
- [MIDIUMPCIProfile](/documentation/coremidi/midiumpciprofile)

### Instance Properties

- [var enabledChannelCount: MIDIUInteger14](/documentation/coremidi/midiumpciprofile/enabledchannelcount)
- [var firstChannel: MIDIChannelNumber](/documentation/coremidi/midiumpciprofile/firstchannel)
- [var groupOffset: MIDIUMPGroupNumber](/documentation/coremidi/midiumpciprofile/groupoffset)
- [var isEnabled: Bool](/documentation/coremidi/midiumpciprofile/isenabled)
- [var name: String](/documentation/coremidi/midiumpciprofile/name)
- [var profileID: MIDICIProfileID](/documentation/coremidi/midiumpciprofile/profileid)
- [var profileType: MIDICIProfileType](/documentation/coremidi/midiumpciprofile/profiletype)
- [var totalChannelCount: MIDIUInteger14](/documentation/coremidi/midiumpciprofile/totalchannelcount)

### Instance Methods

- [func setProfileState(Bool, enabledChannelCount: MIDIUInteger14) throws](/documentation/coremidi/midiumpciprofile/setprofilestate(_:enabledchannelcount:))
- [MIDIUMPEndpoint](/documentation/coremidi/midiumpendpoint)

### Instance Properties

- [var deviceInfo: MIDI2DeviceInfo](/documentation/coremidi/midiumpendpoint/deviceinfo)
- [var endpointType: MIDIUMPCIObjectBackingType](/documentation/coremidi/midiumpendpoint/endpointtype)
- [var functionBlocks: [MIDIUMPFunctionBlock]](/documentation/coremidi/midiumpendpoint/functionblocks)
- [var hasJRTSReceiveCapability: Bool](/documentation/coremidi/midiumpendpoint/hasjrtsreceivecapability)
- [var hasJRTSTransmitCapability: Bool](/documentation/coremidi/midiumpendpoint/hasjrtstransmitcapability)
- [var hasStaticFunctionBlocks: Bool](/documentation/coremidi/midiumpendpoint/hasstaticfunctionblocks)
- [var midiDestination: MIDIEndpointRef](/documentation/coremidi/midiumpendpoint/mididestination)
- [var midiProtocol: MIDIProtocolID](/documentation/coremidi/midiumpendpoint/midiprotocol)
- [var midiSource: MIDIEndpointRef](/documentation/coremidi/midiumpendpoint/midisource)
- [var name: String](/documentation/coremidi/midiumpendpoint/name)
- [var productInstanceID: String](/documentation/coremidi/midiumpendpoint/productinstanceid)
- [var supportedMIDIProtocols: MIDIUMPProtocolOptions](/documentation/coremidi/midiumpendpoint/supportedmidiprotocols)
- [MIDIUMPEndpointManager](/documentation/coremidi/midiumpendpointmanager)

### Instance Properties

- [var umpEndpoints: [MIDIUMPEndpoint]](/documentation/coremidi/midiumpendpointmanager/umpendpoints)

### Type Properties

- [class var shared: MIDIUMPEndpointManager](/documentation/coremidi/midiumpendpointmanager/shared)

### Constants

- [MIDIUMPEndpointManager.DictionaryKey](/documentation/coremidi/midiumpendpointmanager/dictionarykey)

#### Initializers

- [init(rawValue: String)](/documentation/coremidi/midiumpendpointmanager/dictionarykey/init(rawvalue:))
- [class let endpointWasAddedNotification: NSNotification.Name](/documentation/coremidi/midiumpendpointmanager/endpointwasaddednotification)
- [class let endpointWasRemovedNotification: NSNotification.Name](/documentation/coremidi/midiumpendpointmanager/endpointwasremovednotification)
- [class let endpointWasUpdatedNotification: NSNotification.Name](/documentation/coremidi/midiumpendpointmanager/endpointwasupdatednotification)
- [class let functionBlockWasUpdatedNotification: NSNotification.Name](/documentation/coremidi/midiumpendpointmanager/functionblockwasupdatednotification)
- [MIDIUMPFunctionBlock](/documentation/coremidi/midiumpfunctionblock)

### Instance Properties

- [var direction: MIDIUMPFunctionBlockDirection](/documentation/coremidi/midiumpfunctionblock/direction)
- [var firstGroup: MIDIUMPGroupNumber](/documentation/coremidi/midiumpfunctionblock/firstgroup)
- [var functionBlockID: MIDIUMPFunctionBlockID](/documentation/coremidi/midiumpfunctionblock/functionblockid)
- [var isEnabled: Bool](/documentation/coremidi/midiumpfunctionblock/isenabled)
- [var maxSysEx8Streams: UInt8](/documentation/coremidi/midiumpfunctionblock/maxsysex8streams)
- [var midi1Info: MIDIUMPFunctionBlockMIDI1Info](/documentation/coremidi/midiumpfunctionblock/midi1info)
- [var midiCIDevice: MIDICIDevice?](/documentation/coremidi/midiumpfunctionblock/midicidevice)
- [var name: String](/documentation/coremidi/midiumpfunctionblock/name)
- [var totalGroupsSpanned: MIDIUInteger7](/documentation/coremidi/midiumpfunctionblock/totalgroupsspanned)
- [var uiHint: MIDIUMPFunctionBlockUIHint](/documentation/coremidi/midiumpfunctionblock/uihint)
- [var umpEndpoint: MIDIUMPEndpoint?](/documentation/coremidi/midiumpfunctionblock/umpendpoint)
- [MIDIUMPMutableEndpoint](/documentation/coremidi/midiumpmutableendpoint)

### Initializers

- [init?(name: String, deviceInfo: MIDI2DeviceInfo, productInstanceID: String, midiProtocol: MIDIProtocolID, destinationCallback: MIDIReceiveBlock)](/documentation/coremidi/midiumpmutableendpoint/init(name:deviceinfo:productinstanceid:midiprotocol:destinationcallback:))

### Instance Properties

- [var isEnabled: Bool](/documentation/coremidi/midiumpmutableendpoint/isenabled)
- [var mutableFunctionBlocks: [MIDIUMPMutableFunctionBlock]](/documentation/coremidi/midiumpmutableendpoint/mutablefunctionblocks)

### Instance Methods

- [func registerFunctionBlocks([MIDIUMPMutableFunctionBlock], markAsStatic: Bool) throws](/documentation/coremidi/midiumpmutableendpoint/registerfunctionblocks(_:markasstatic:))
- [func setEnabled(Bool) throws](/documentation/coremidi/midiumpmutableendpoint/setenabled(_:))
- [func setName(String) throws](/documentation/coremidi/midiumpmutableendpoint/setname(_:))
- [MIDIUMPMutableFunctionBlock](/documentation/coremidi/midiumpmutablefunctionblock)

### Initializers

- [init?(name: String, direction: MIDIUMPFunctionBlockDirection, firstGroup: MIDIUMPGroupNumber, totalGroupsSpanned: MIDIUInteger7, maxSysEx8Streams: MIDIUInteger7, midi1Info: MIDIUMPFunctionBlockMIDI1Info, uiHint: MIDIUMPFunctionBlockUIHint, isEnabled: Bool)](/documentation/coremidi/midiumpmutablefunctionblock/init(name:direction:firstgroup:totalgroupsspanned:maxsysex8streams:midi1info:uihint:isenabled:))

### Instance Properties

- [var umpEndpoint: MIDIUMPMutableEndpoint?](/documentation/coremidi/midiumpmutablefunctionblock/umpendpoint)

### Instance Methods

- [func reconfigure(firstGroup: MIDIUMPGroupNumber, direction: MIDIUMPFunctionBlockDirection, MIDI1Info: MIDIUMPFunctionBlockMIDI1Info, UIHint: MIDIUMPFunctionBlockUIHint) throws](/documentation/coremidi/midiumpmutablefunctionblock/reconfigure(firstgroup:direction:midi1info:uihint:))
- [func setEnabled(Bool) throws](/documentation/coremidi/midiumpmutablefunctionblock/setenabled(_:))
- [func setName(String) throws](/documentation/coremidi/midiumpmutablefunctionblock/setname(_:))

## Variables

- [var kMIDINoteAttributeManufacturerSpecific: Int](/documentation/coremidi/kmidinoteattributemanufacturerspecific)
- [var kMIDINoteAttributeNone: Int](/documentation/coremidi/kmidinoteattributenone)
- [var kMIDINoteAttributePitch: Int](/documentation/coremidi/kmidinoteattributepitch)
- [var kMIDINoteAttributeProfileSpecific: Int](/documentation/coremidi/kmidinoteattributeprofilespecific)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
