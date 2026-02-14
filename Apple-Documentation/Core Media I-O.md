# CoreMediaIO Documentation

Source: https://sosumi.ai/documentation/coremediaio

---
title: Core Media I/O
source: https://developer.apple.com/documentation/coremediaio
timestamp: 2026-02-13T19:58:02.290Z
---

## Providers

- [Creating a camera extension with Core Media I/O](/documentation/coremediaio/creating-a-camera-extension-with-core-media-i-o)
- [Overriding the default USB video class extension](/documentation/coremediaio/overriding-the-default-usb-video-class-extension)
- [CMIOExtensionProvider](/documentation/coremediaio/cmioextensionprovider)

### Creating a Provider

- [init(source: any CMIOExtensionProviderSource, clientQueue: dispatch_queue_t?)](/documentation/coremediaio/cmioextensionprovider/init(source:clientqueue:))

### Inspecting a Provider

- [var clientQueue: dispatch_queue_t](/documentation/coremediaio/cmioextensionprovider/clientqueue)
- [var source: (any CMIOExtensionProviderSource)?](/documentation/coremediaio/cmioextensionprovider/source)

### Starting a Provider

- [class func startService(provider: CMIOExtensionProvider)](/documentation/coremediaio/cmioextensionprovider/startservice(provider:))

### Managing Devices

- [var devices: [CMIOExtensionDevice]](/documentation/coremediaio/cmioextensionprovider/devices)
- [func addDevice(CMIOExtensionDevice) throws](/documentation/coremediaio/cmioextensionprovider/adddevice(_:))
- [func removeDevice(CMIOExtensionDevice) throws](/documentation/coremediaio/cmioextensionprovider/removedevice(_:))

### Managing Clients

- [var connectedClients: [CMIOExtensionClient]](/documentation/coremediaio/cmioextensionprovider/connectedclients)
- [func notifyPropertiesChanged([CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>])](/documentation/coremediaio/cmioextensionprovider/notifypropertieschanged(_:))

### Type Methods

- [class func ignoreSIGTERM()](/documentation/coremediaio/cmioextensionprovider/ignoresigterm())
- [class func stopService(provider: CMIOExtensionProvider)](/documentation/coremediaio/cmioextensionprovider/stopservice(provider:))
- [CMIOExtensionProviderSource](/documentation/coremediaio/cmioextensionprovidersource)

### Managing Connections

- [func connect(to: CMIOExtensionClient) throws](/documentation/coremediaio/cmioextensionprovidersource/connect(to:))
- [func disconnect(from: CMIOExtensionClient)](/documentation/coremediaio/cmioextensionprovidersource/disconnect(from:))

### Configuring Properties

- [var availableProperties: Set<CMIOExtensionProperty>](/documentation/coremediaio/cmioextensionprovidersource/availableproperties)
- [func providerProperties(forProperties: Set<CMIOExtensionProperty>) throws -> CMIOExtensionProviderProperties](/documentation/coremediaio/cmioextensionprovidersource/providerproperties(forproperties:))
- [func setProviderProperties(CMIOExtensionProviderProperties) throws](/documentation/coremediaio/cmioextensionprovidersource/setproviderproperties(_:))
- [CMIOExtensionProviderProperties](/documentation/coremediaio/cmioextensionproviderproperties)

### Creating Provider Properties

- [init(dictionary: [CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>])](/documentation/coremediaio/cmioextensionproviderproperties/init(dictionary:))

### Managing Properties

- [var name: String?](/documentation/coremediaio/cmioextensionproviderproperties/name)
- [var manufacturer: String?](/documentation/coremediaio/cmioextensionproviderproperties/manufacturer)
- [func setPropertyState(CMIOExtensionPropertyState<AnyObject>?, forProperty: CMIOExtensionProperty)](/documentation/coremediaio/cmioextensionproviderproperties/setpropertystate(_:forproperty:))
- [var propertiesDictionary: [CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>]](/documentation/coremediaio/cmioextensionproviderproperties/propertiesdictionary)

## Devices

- [CMIOExtensionDevice](/documentation/coremediaio/cmioextensiondevice)

### Creating a Device

- [convenience init(localizedName: String, deviceID: UUID, source: any CMIOExtensionDeviceSource)](/documentation/coremediaio/cmioextensiondevice/init(localizedname:deviceid:source:))
- [init(localizedName: String, deviceID: UUID, legacyDeviceID: String?, source: any CMIOExtensionDeviceSource)](/documentation/coremediaio/cmioextensiondevice/init(localizedname:deviceid:legacydeviceid:source:))

### Identifying a Device

- [var localizedName: String](/documentation/coremediaio/cmioextensiondevice/localizedname)
- [var deviceID: UUID](/documentation/coremediaio/cmioextensiondevice/deviceid)
- [var legacyDeviceID: String](/documentation/coremediaio/cmioextensiondevice/legacydeviceid)

### Managing Streams

- [var streams: [CMIOExtensionStream]](/documentation/coremediaio/cmioextensiondevice/streams)
- [func addStream(CMIOExtensionStream) throws](/documentation/coremediaio/cmioextensiondevice/addstream(_:))
- [func removeStream(CMIOExtensionStream) throws](/documentation/coremediaio/cmioextensiondevice/removestream(_:))

### Accessing the Device Source

- [var source: (any CMIOExtensionDeviceSource)?](/documentation/coremediaio/cmioextensiondevice/source)

### Posting Property Changes

- [func notifyPropertiesChanged([CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>])](/documentation/coremediaio/cmioextensiondevice/notifypropertieschanged(_:))
- [CMIOExtensionDeviceSource](/documentation/coremediaio/cmioextensiondevicesource)

### Managing Properties

- [var availableProperties: Set<CMIOExtensionProperty>](/documentation/coremediaio/cmioextensiondevicesource/availableproperties)
- [func deviceProperties(forProperties: Set<CMIOExtensionProperty>) throws -> CMIOExtensionDeviceProperties](/documentation/coremediaio/cmioextensiondevicesource/deviceproperties(forproperties:))
- [func setDeviceProperties(CMIOExtensionDeviceProperties) throws](/documentation/coremediaio/cmioextensiondevicesource/setdeviceproperties(_:))
- [CMIOExtensionDeviceProperties](/documentation/coremediaio/cmioextensiondeviceproperties)

### Creating Device Properties

- [init(dictionary: [CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>])](/documentation/coremediaio/cmioextensiondeviceproperties/init(dictionary:))

### Configuring Device Properties

- [var model: String?](/documentation/coremediaio/cmioextensiondeviceproperties/model)
- [var linkedCoreAudioDeviceUID: String?](/documentation/coremediaio/cmioextensiondeviceproperties/linkedcoreaudiodeviceuid)
- [var transportType: Int?](/documentation/coremediaio/cmioextensiondeviceproperties/transporttype-96gm)
- [var suspended: Bool?](/documentation/coremediaio/cmioextensiondeviceproperties/suspended-eru0)
- [func setPropertyState(CMIOExtensionPropertyState<AnyObject>?, forProperty: CMIOExtensionProperty)](/documentation/coremediaio/cmioextensiondeviceproperties/setpropertystate(_:forproperty:))
- [var propertiesDictionary: [CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>]](/documentation/coremediaio/cmioextensiondeviceproperties/propertiesdictionary)

## Streams

- [CMIOExtensionStream](/documentation/coremediaio/cmioextensionstream)

### Creating a Stream

- [init(localizedName: String, streamID: UUID, direction: CMIOExtensionStream.Direction, clockType: CMIOExtensionStream.ClockType, source: any CMIOExtensionStreamSource)](/documentation/coremediaio/cmioextensionstream/init(localizedname:streamid:direction:clocktype:source:))
- [init(localizedName: String, streamID: UUID, direction: CMIOExtensionStream.Direction, customClockConfiguration: CMIOExtensionStreamCustomClockConfiguration, source: any CMIOExtensionStreamSource)](/documentation/coremediaio/cmioextensionstream/init(localizedname:streamid:direction:customclockconfiguration:source:))

### Identifying a Stream

- [var localizedName: String](/documentation/coremediaio/cmioextensionstream/localizedname)
- [var streamID: UUID](/documentation/coremediaio/cmioextensionstream/streamid)

### Accessing Clients

- [var streamingClients: [CMIOExtensionClient]](/documentation/coremediaio/cmioextensionstream/streamingclients)

### Inspecting a Stream

- [var source: (any CMIOExtensionStreamSource)?](/documentation/coremediaio/cmioextensionstream/source)
- [var direction: CMIOExtensionStream.Direction](/documentation/coremediaio/cmioextensionstream/direction-swift.property)
- [CMIOExtensionStream.Direction](/documentation/coremediaio/cmioextensionstream/direction-swift.enum)

#### Directions

- [case source](/documentation/coremediaio/cmioextensionstream/direction-swift.enum/source)
- [case sink](/documentation/coremediaio/cmioextensionstream/direction-swift.enum/sink)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremediaio/cmioextensionstream/direction-swift.enum/init(rawvalue:))
- [var clockType: CMIOExtensionStream.ClockType](/documentation/coremediaio/cmioextensionstream/clocktype-swift.property)
- [CMIOExtensionStream.ClockType](/documentation/coremediaio/cmioextensionstream/clocktype-swift.enum)

#### Clock Types

- [case hostTime](/documentation/coremediaio/cmioextensionstream/clocktype-swift.enum/hosttime)
- [case linkedCoreAudioDeviceUID](/documentation/coremediaio/cmioextensionstream/clocktype-swift.enum/linkedcoreaudiodeviceuid)
- [case custom](/documentation/coremediaio/cmioextensionstream/clocktype-swift.enum/custom)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremediaio/cmioextensionstream/clocktype-swift.enum/init(rawvalue:))
- [var customClockConfiguration: CMIOExtensionStreamCustomClockConfiguration?](/documentation/coremediaio/cmioextensionstream/customclockconfiguration)
- [CMIOExtensionStreamCustomClockConfiguration](/documentation/coremediaio/cmioextensionstreamcustomclockconfiguration)

#### Creating a Clock Configuration

- [init(clockName: String, sourceIdentifier: UUID, getTimeCallMinimumInterval: CMTime, numberOfEventsForRateSmoothing: UInt32, numberOfAveragesForRateSmoothing: UInt32)](/documentation/coremediaio/cmioextensionstreamcustomclockconfiguration/init(clockname:sourceidentifier:gettimecallminimuminterval:numberofeventsforratesmoothing:numberofaveragesforratesmoothing:))

#### Inspecting the Configuration

- [var clockName: String](/documentation/coremediaio/cmioextensionstreamcustomclockconfiguration/clockname)
- [var sourceIdentifier: UUID](/documentation/coremediaio/cmioextensionstreamcustomclockconfiguration/sourceidentifier)
- [var getTimeCallMinimumInterval: CMTime](/documentation/coremediaio/cmioextensionstreamcustomclockconfiguration/gettimecallminimuminterval)
- [var numberOfEventsForRateSmoothing: UInt32](/documentation/coremediaio/cmioextensionstreamcustomclockconfiguration/numberofeventsforratesmoothing)
- [var numberOfAveragesForRateSmoothing: UInt32](/documentation/coremediaio/cmioextensionstreamcustomclockconfiguration/numberofaveragesforratesmoothing)

### Processing Data

- [func consumeSampleBuffer(from: CMIOExtensionClient, completionHandler: (CMSampleBuffer?, UInt64, CMIOExtensionStream.DiscontinuityFlags, Bool, (any Error)?) -> Void)](/documentation/coremediaio/cmioextensionstream/consumesamplebuffer(from:completionhandler:))
- [func send(CMSampleBuffer, discontinuity: CMIOExtensionStream.DiscontinuityFlags, hostTimeInNanoseconds: UInt64)](/documentation/coremediaio/cmioextensionstream/send(_:discontinuity:hosttimeinnanoseconds:))
- [CMIOExtensionStream.DiscontinuityFlags](/documentation/coremediaio/cmioextensionstream/discontinuityflags)

#### Discontinuity Flags

- [static var unknown: CMIOExtensionStream.DiscontinuityFlags](/documentation/coremediaio/cmioextensionstream/discontinuityflags/unknown)
- [static var time: CMIOExtensionStream.DiscontinuityFlags](/documentation/coremediaio/cmioextensionstream/discontinuityflags/time)
- [static var sampleDropped: CMIOExtensionStream.DiscontinuityFlags](/documentation/coremediaio/cmioextensionstream/discontinuityflags/sampledropped)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coremediaio/cmioextensionstream/discontinuityflags/init(rawvalue:))

### Posting Property Changes

- [func notifyPropertiesChanged([CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>])](/documentation/coremediaio/cmioextensionstream/notifypropertieschanged(_:))

### Managing Scheduled Output

- [func notifyScheduledOutputChanged(CMIOExtensionScheduledOutput)](/documentation/coremediaio/cmioextensionstream/notifyscheduledoutputchanged(_:))
- [CMIOExtensionScheduledOutput](/documentation/coremediaio/cmioextensionscheduledoutput)

#### Creating a Scheduled Output

- [init(sequenceNumber: UInt64, hostTimeInNanoseconds: UInt64)](/documentation/coremediaio/cmioextensionscheduledoutput/init(sequencenumber:hosttimeinnanoseconds:))

#### Inspecting the Output

- [var sequenceNumber: UInt64](/documentation/coremediaio/cmioextensionscheduledoutput/sequencenumber)
- [var hostTimeInNanoseconds: UInt64](/documentation/coremediaio/cmioextensionscheduledoutput/hosttimeinnanoseconds)
- [CMIOExtensionStreamSource](/documentation/coremediaio/cmioextensionstreamsource)

### Accessing the Source Format

- [var formats: [CMIOExtensionStreamFormat]](/documentation/coremediaio/cmioextensionstreamsource/formats)
- [CMIOExtensionStreamFormat](/documentation/coremediaio/cmioextensionstreamformat)

#### Creating a Stream Format

- [convenience init(formatDescription: CMFormatDescription, maxFrameDuration: CMTime, minFrameDuration: CMTime, validFrameDurations: [CMTime]?)](/documentation/coremediaio/cmioextensionstreamformat/init(formatdescription:maxframeduration:minframeduration:validframedurations:))

#### Configuring Frame Durations

- [var minFrameDuration: CMTime](/documentation/coremediaio/cmioextensionstreamformat/minframeduration)
- [var maxFrameDuration: CMTime](/documentation/coremediaio/cmioextensionstreamformat/maxframeduration)
- [var validFrameDurations: [CMTime]?](/documentation/coremediaio/cmioextensionstreamformat/validframedurations-707st)

#### Accessing the Format Description

- [var formatDescription: CMFormatDescription](/documentation/coremediaio/cmioextensionstreamformat/formatdescription)

### Managing Stream Properties

- [var availableProperties: Set<CMIOExtensionProperty>](/documentation/coremediaio/cmioextensionstreamsource/availableproperties)
- [func streamProperties(forProperties: Set<CMIOExtensionProperty>) throws -> CMIOExtensionStreamProperties](/documentation/coremediaio/cmioextensionstreamsource/streamproperties(forproperties:))
- [func setStreamProperties(CMIOExtensionStreamProperties) throws](/documentation/coremediaio/cmioextensionstreamsource/setstreamproperties(_:))

### Managing a Stream

- [func authorizedToStartStream(for: CMIOExtensionClient) -> Bool](/documentation/coremediaio/cmioextensionstreamsource/authorizedtostartstream(for:))
- [func startStream() throws](/documentation/coremediaio/cmioextensionstreamsource/startstream())
- [func stopStream() throws](/documentation/coremediaio/cmioextensionstreamsource/stopstream())
- [CMIOExtensionStreamProperties](/documentation/coremediaio/cmioextensionstreamproperties)

### Creating Stream Properties

- [init(dictionary: [CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>])](/documentation/coremediaio/cmioextensionstreamproperties/init(dictionary:))

### Configuring Sink Properties

- [var sinkBufferQueueSize: Int?](/documentation/coremediaio/cmioextensionstreamproperties/sinkbufferqueuesize-9b80c)
- [var sinkBuffersRequiredForStartup: Int?](/documentation/coremediaio/cmioextensionstreamproperties/sinkbuffersrequiredforstartup-1bgyq)
- [var sinkBufferUnderrunCount: Int?](/documentation/coremediaio/cmioextensionstreamproperties/sinkbufferunderruncount-1qmbb)
- [var sinkEndOfData: Int?](/documentation/coremediaio/cmioextensionstreamproperties/sinkendofdata-8fswu)

### Configuring Source Properties

- [var activeFormatIndex: Int?](/documentation/coremediaio/cmioextensionstreamproperties/activeformatindex-83u7z)
- [var frameDuration: CMTime?](/documentation/coremediaio/cmioextensionstreamproperties/frameduration-4rnl9)
- [var maxFrameDuration: CMTime?](/documentation/coremediaio/cmioextensionstreamproperties/maxframeduration-5qqg)

### Managing Property State

- [var propertiesDictionary: [CMIOExtensionProperty : CMIOExtensionPropertyState<AnyObject>]](/documentation/coremediaio/cmioextensionstreamproperties/propertiesdictionary)
- [func setPropertyState(CMIOExtensionPropertyState<AnyObject>?, forProperty: CMIOExtensionProperty)](/documentation/coremediaio/cmioextensionstreamproperties/setpropertystate(_:forproperty:))
- [CMIOExtensionClient](/documentation/coremediaio/cmioextensionclient)

### Identifying a Client

- [var clientID: UUID](/documentation/coremediaio/cmioextensionclient/clientid)
- [var pid: pid_t](/documentation/coremediaio/cmioextensionclient/pid)

### Instance Properties

- [var signingID: String?](/documentation/coremediaio/cmioextensionclient/signingid)

## Properties

- [CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty)

### Provider Properties

- [static let providerName: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/providername)
- [static let providerManufacturer: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/providermanufacturer)

### Device Properties

- [static let deviceModel: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicemodel)
- [static let deviceIsSuspended: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/deviceissuspended)
- [static let deviceTransportType: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicetransporttype)
- [static let deviceLinkedCoreAudioDeviceUID: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicelinkedcoreaudiodeviceuid)
- [static let deviceCanBeDefaultInputDevice: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicecanbedefaultinputdevice)
- [static let deviceCanBeDefaultOutputDevice: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicecanbedefaultoutputdevice)

### Stream Properties

- [static let streamActiveFormatIndex: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamactiveformatindex)
- [static let streamFrameDuration: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamframeduration)
- [static let streamMaxFrameDuration: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streammaxframeduration)
- [static let streamSinkBufferQueueSize: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkbufferqueuesize)
- [static let streamSinkBuffersRequiredForStartup: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkbuffersrequiredforstartup)
- [static let streamSinkBufferUnderrunCount: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkbufferunderruncount)
- [static let streamSinkEndOfData: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkendofdata)

### Type Properties

- [static let deviceLatency: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicelatency)
- [static let streamLatency: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamlatency)
- [init(rawValue: String)](/documentation/coremediaio/cmioextensionproperty/init(rawvalue:))
- [CMIOExtensionPropertyState](/documentation/coremediaio/cmioextensionpropertystate)

### Creating a Property State

- [convenience init(value: ObjectType?)](/documentation/coremediaio/cmioextensionpropertystate/init(value:))
- [init(value: ObjectType?, attributes: CMIOExtensionPropertyAttributes<ObjectType>?)](/documentation/coremediaio/cmioextensionpropertystate/init(value:attributes:))

### Inspecting a Property State

- [var value: ObjectType?](/documentation/coremediaio/cmioextensionpropertystate/value)
- [var attributes: CMIOExtensionPropertyAttributes<ObjectType>?](/documentation/coremediaio/cmioextensionpropertystate/attributes)
- [CMIOExtensionPropertyAttributes](/documentation/coremediaio/cmioextensionpropertyattributes)

### Creating Property Attributes

- [init(minValue: ObjectType?, maxValue: ObjectType?, validValues: [ObjectType]?, readOnly: Bool)](/documentation/coremediaio/cmioextensionpropertyattributes/init(minvalue:maxvalue:validvalues:readonly:))

### Inspecting Attributes

- [var isReadOnly: Bool](/documentation/coremediaio/cmioextensionpropertyattributes/isreadonly)
- [var minValue: ObjectType?](/documentation/coremediaio/cmioextensionpropertyattributes/minvalue)
- [var maxValue: ObjectType?](/documentation/coremediaio/cmioextensionpropertyattributes/maxvalue)
- [var validValues: [ObjectType]?](/documentation/coremediaio/cmioextensionpropertyattributes/validvalues)

### Specifying a Read-Only Attribute

- [class var readOnlyPropertyAttribute: CMIOExtensionPropertyAttributes<AnyObject>](/documentation/coremediaio/cmioextensionpropertyattributes/readonlypropertyattribute)
- [let CMIOExtensionInfoDictionaryKey: String](/documentation/coremediaio/cmioextensioninfodictionarykey)
- [let CMIOExtensionMachServiceNameKey: String](/documentation/coremediaio/cmioextensionmachservicenamekey)

## DAL Plug-Ins

- [Device Abstraction Layer (DAL) Plug-Ins](/documentation/coremediaio/device-abstraction-layer-dal-plug-ins)

### Reference

- [DAL plug-in structures](/documentation/coremediaio/core-media-i-o-structures)

#### Structures

- [CMIODeviceAVCCommand](/documentation/coremediaio/cmiodeviceavccommand)

##### Initializers

- [init()](/documentation/coremediaio/cmiodeviceavccommand/init())
- [init(mCommand: UnsafeMutablePointer<UInt8>!, mCommandLength: UInt32, mResponse: UnsafeMutablePointer<UInt8>!, mResponseLength: UInt32, mResponseUsed: UInt32)](/documentation/coremediaio/cmiodeviceavccommand/init(mcommand:mcommandlength:mresponse:mresponselength:mresponseused:))

##### Instance Properties

- [var mCommand: UnsafeMutablePointer<UInt8>!](/documentation/coremediaio/cmiodeviceavccommand/mcommand)
- [var mCommandLength: UInt32](/documentation/coremediaio/cmiodeviceavccommand/mcommandlength)
- [var mResponse: UnsafeMutablePointer<UInt8>!](/documentation/coremediaio/cmiodeviceavccommand/mresponse)
- [var mResponseLength: UInt32](/documentation/coremediaio/cmiodeviceavccommand/mresponselength)
- [var mResponseUsed: UInt32](/documentation/coremediaio/cmiodeviceavccommand/mresponseused)
- [CMIODeviceRS422Command](/documentation/coremediaio/cmiodevicers422command)

##### Initializers

- [init()](/documentation/coremediaio/cmiodevicers422command/init())
- [init(mCommand: UnsafeMutablePointer<UInt8>!, mCommandLength: UInt32, mResponse: UnsafeMutablePointer<UInt8>!, mResponseLength: UInt32, mResponseUsed: UInt32)](/documentation/coremediaio/cmiodevicers422command/init(mcommand:mcommandlength:mresponse:mresponselength:mresponseused:))

##### Instance Properties

- [var mCommand: UnsafeMutablePointer<UInt8>!](/documentation/coremediaio/cmiodevicers422command/mcommand)
- [var mCommandLength: UInt32](/documentation/coremediaio/cmiodevicers422command/mcommandlength)
- [var mResponse: UnsafeMutablePointer<UInt8>!](/documentation/coremediaio/cmiodevicers422command/mresponse)
- [var mResponseLength: UInt32](/documentation/coremediaio/cmiodevicers422command/mresponselength)
- [var mResponseUsed: UInt32](/documentation/coremediaio/cmiodevicers422command/mresponseused)
- [CMIODeviceSMPTETimeCallback](/documentation/coremediaio/cmiodevicesmptetimecallback)

##### Initializers

- [init()](/documentation/coremediaio/cmiodevicesmptetimecallback/init())
- [init(mGetSMPTETimeProc: CMIODeviceGetSMPTETimeProc!, mRefCon: UnsafeMutableRawPointer!)](/documentation/coremediaio/cmiodevicesmptetimecallback/init(mgetsmptetimeproc:mrefcon:))

##### Instance Properties

- [var mGetSMPTETimeProc: CMIODeviceGetSMPTETimeProc!](/documentation/coremediaio/cmiodevicesmptetimecallback/mgetsmptetimeproc)
- [var mRefCon: UnsafeMutableRawPointer!](/documentation/coremediaio/cmiodevicesmptetimecallback/mrefcon)
- [CMIODeviceStreamConfiguration](/documentation/coremediaio/cmiodevicestreamconfiguration)

##### Initializers

- [init()](/documentation/coremediaio/cmiodevicestreamconfiguration/init())

##### Instance Properties

- [var mNumberStreams: UInt32](/documentation/coremediaio/cmiodevicestreamconfiguration/mnumberstreams)
- [CMIOObjectPropertyAddress](/documentation/coremediaio/cmioobjectpropertyaddress)

##### Initializers

- [init()](/documentation/coremediaio/cmioobjectpropertyaddress/init())
- [init(mSelector: CMIOObjectPropertySelector, mScope: CMIOObjectPropertyScope, mElement: CMIOObjectPropertyElement)](/documentation/coremediaio/cmioobjectpropertyaddress/init(mselector:mscope:melement:))

##### Instance Properties

- [var mElement: CMIOObjectPropertyElement](/documentation/coremediaio/cmioobjectpropertyaddress/melement)
- [var mScope: CMIOObjectPropertyScope](/documentation/coremediaio/cmioobjectpropertyaddress/mscope)
- [var mSelector: CMIOObjectPropertySelector](/documentation/coremediaio/cmioobjectpropertyaddress/mselector)
- [CMIOStreamDeck](/documentation/coremediaio/cmiostreamdeck)

##### Initializers

- [init()](/documentation/coremediaio/cmiostreamdeck/init())
- [init(mStatus: UInt32, mState: UInt32, mState2: UInt32)](/documentation/coremediaio/cmiostreamdeck/init(mstatus:mstate:mstate2:))

##### Instance Properties

- [var mState: UInt32](/documentation/coremediaio/cmiostreamdeck/mstate)
- [var mState2: UInt32](/documentation/coremediaio/cmiostreamdeck/mstate2)
- [var mStatus: UInt32](/documentation/coremediaio/cmiostreamdeck/mstatus)
- [CMIOStreamScheduledOutputNotificationProcAndRefCon](/documentation/coremediaio/cmiostreamscheduledoutputnotificationprocandrefcon)

##### Initializers

- [init()](/documentation/coremediaio/cmiostreamscheduledoutputnotificationprocandrefcon/init())
- [init(scheduledOutputNotificationProc: CMIOStreamScheduledOutputNotificationProc!, scheduledOutputNotificationRefCon: UnsafeMutableRawPointer!)](/documentation/coremediaio/cmiostreamscheduledoutputnotificationprocandrefcon/init(scheduledoutputnotificationproc:scheduledoutputnotificationrefcon:))

##### Instance Properties

- [var scheduledOutputNotificationProc: CMIOStreamScheduledOutputNotificationProc!](/documentation/coremediaio/cmiostreamscheduledoutputnotificationprocandrefcon/scheduledoutputnotificationproc)
- [var scheduledOutputNotificationRefCon: UnsafeMutableRawPointer!](/documentation/coremediaio/cmiostreamscheduledoutputnotificationprocandrefcon/scheduledoutputnotificationrefcon)
- [DAL plug-in functions](/documentation/coremediaio/core-media-i-o-functions)

#### Functions

- [func CMIODeviceProcessAVCCommand(CMIODeviceID, UnsafeMutablePointer<CMIODeviceAVCCommand>!) -> OSStatus](/documentation/coremediaio/cmiodeviceprocessavccommand(_:_:))
- [func CMIODeviceProcessRS422Command(CMIODeviceID, UnsafeMutablePointer<CMIODeviceRS422Command>!) -> OSStatus](/documentation/coremediaio/cmiodeviceprocessrs422command(_:_:))
- [func CMIODeviceStartStream(CMIODeviceID, CMIOStreamID) -> OSStatus](/documentation/coremediaio/cmiodevicestartstream(_:_:))
- [func CMIODeviceStopStream(CMIODeviceID, CMIOStreamID) -> OSStatus](/documentation/coremediaio/cmiodevicestopstream(_:_:))
- [func CMIOObjectAddPropertyListener(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, CMIOObjectPropertyListenerProc!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/coremediaio/cmioobjectaddpropertylistener(_:_:_:_:))
- [func CMIOObjectAddPropertyListenerBlock(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, dispatch_queue_t!, CMIOObjectPropertyListenerBlock!) -> OSStatus](/documentation/coremediaio/cmioobjectaddpropertylistenerblock(_:_:_:_:))
- [func CMIOObjectGetPropertyData(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, UInt32, UnsafeRawPointer!, UInt32, UnsafeMutablePointer<UInt32>!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/coremediaio/cmioobjectgetpropertydata(_:_:_:_:_:_:_:))
- [func CMIOObjectGetPropertyDataSize(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, UInt32, UnsafeRawPointer!, UnsafeMutablePointer<UInt32>!) -> OSStatus](/documentation/coremediaio/cmioobjectgetpropertydatasize(_:_:_:_:_:))
- [func CMIOObjectHasProperty(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!) -> Bool](/documentation/coremediaio/cmioobjecthasproperty(_:_:))
- [func CMIOObjectIsPropertySettable(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, UnsafeMutablePointer<DarwinBoolean>!) -> OSStatus](/documentation/coremediaio/cmioobjectispropertysettable(_:_:_:))
- [func CMIOObjectRemovePropertyListener(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, CMIOObjectPropertyListenerProc!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/coremediaio/cmioobjectremovepropertylistener(_:_:_:_:))
- [func CMIOObjectRemovePropertyListenerBlock(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, dispatch_queue_t!, CMIOObjectPropertyListenerBlock!) -> OSStatus](/documentation/coremediaio/cmioobjectremovepropertylistenerblock(_:_:_:_:))
- [func CMIOObjectSetPropertyData(CMIOObjectID, UnsafePointer<CMIOObjectPropertyAddress>!, UInt32, UnsafeRawPointer!, UInt32, UnsafeRawPointer!) -> OSStatus](/documentation/coremediaio/cmioobjectsetpropertydata(_:_:_:_:_:_:))
- [func CMIOObjectShow(CMIOObjectID)](/documentation/coremediaio/cmioobjectshow(_:))
- [func CMIOStreamClockConvertHostTimeToDeviceTime(UInt64, CFTypeRef!) -> CMTime](/documentation/coremediaio/cmiostreamclockconverthosttimetodevicetime(_:_:))
- [func CMIOStreamClockCreate(CFAllocator!, CFString!, UnsafeRawPointer!, CMTime, UInt32, UInt32, UnsafeMutablePointer<Unmanaged<CFTypeRef>?>!) -> OSStatus](/documentation/coremediaio/cmiostreamclockcreate(_:_:_:_:_:_:_:))
- [func CMIOStreamClockInvalidate(CFTypeRef!) -> OSStatus](/documentation/coremediaio/cmiostreamclockinvalidate(_:))
- [func CMIOStreamClockPostTimingEvent(CMTime, UInt64, Bool, CFTypeRef!) -> OSStatus](/documentation/coremediaio/cmiostreamclockposttimingevent(_:_:_:_:))
- [func CMIOStreamCopyBufferQueue(CMIOStreamID, CMIODeviceStreamQueueAlteredProc!, UnsafeMutableRawPointer!, UnsafeMutablePointer<Unmanaged<CMSimpleQueue>?>!) -> OSStatus](/documentation/coremediaio/cmiostreamcopybufferqueue(_:_:_:_:))
- [func CMIOStreamDeckCueTo(CMIOStreamID, UInt64, Bool) -> OSStatus](/documentation/coremediaio/cmiostreamdeckcueto(_:_:_:))
- [func CMIOStreamDeckJog(CMIOStreamID, Int32) -> OSStatus](/documentation/coremediaio/cmiostreamdeckjog(_:_:))
- [func CMIOStreamDeckPlay(CMIOStreamID) -> OSStatus](/documentation/coremediaio/cmiostreamdeckplay(_:))
- [func CMIOStreamDeckStop(CMIOStreamID) -> OSStatus](/documentation/coremediaio/cmiostreamdeckstop(_:))
- [DAL plug-in enumerations](/documentation/coremediaio/core-media-i-o-enumerations)

#### Constants

- [CMIOAVCDeviceType constants](/documentation/coremediaio/cmioavcdevicetype-constants)

##### Constants

- [var kCMIOAVCDeviceType_DVCPro100_720p: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcpro100_720p)
- [var kCMIOAVCDeviceType_DVCPro100_NTSC: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcpro100_ntsc)
- [var kCMIOAVCDeviceType_DVCPro100_PAL: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcpro100_pal)
- [var kCMIOAVCDeviceType_DVCPro50_NTSC: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcpro50_ntsc)
- [var kCMIOAVCDeviceType_DVCPro50_PAL: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcpro50_pal)
- [var kCMIOAVCDeviceType_DVCProHD_1080i50: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcprohd_1080i50)
- [var kCMIOAVCDeviceType_DVCProHD_1080i60: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcprohd_1080i60)
- [var kCMIOAVCDeviceType_DVCPro_NTSC: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcpro_ntsc)
- [var kCMIOAVCDeviceType_DVCPro_PAL: Int](/documentation/coremediaio/kcmioavcdevicetype_dvcpro_pal)
- [var kCMIOAVCDeviceType_DV_NTSC: Int](/documentation/coremediaio/kcmioavcdevicetype_dv_ntsc)
- [var kCMIOAVCDeviceType_DV_PAL: Int](/documentation/coremediaio/kcmioavcdevicetype_dv_pal)
- [var kCMIOAVCDeviceType_MPEG2: Int](/documentation/coremediaio/kcmioavcdevicetype_mpeg2)
- [var kCMIOAVCDeviceType_Unknown: Int](/documentation/coremediaio/kcmioavcdevicetype_unknown)
- [CMIOBooleanControl properties](/documentation/coremediaio/cmiobooleancontrol-properties)

##### Constants

- [var kCMIOBooleanControlPropertyValue: Int](/documentation/coremediaio/kcmiobooleancontrolpropertyvalue)
- [CMIOBooleanControl subclass IDs](/documentation/coremediaio/cmiobooleancontrol-subclass-ids)

##### Constants

- [var kCMIODirectionControlClassID: Int](/documentation/coremediaio/kcmiodirectioncontrolclassid)
- [var kCMIOJackControlClassID: Int](/documentation/coremediaio/kcmiojackcontrolclassid)
- [CMIOControl base class IDs](/documentation/coremediaio/cmiocontrol-base-class-ids)

##### Constants

- [var kCMIOBooleanControlClassID: Int](/documentation/coremediaio/kcmiobooleancontrolclassid)
- [var kCMIOControlClassID: Int](/documentation/coremediaio/kcmiocontrolclassid)
- [var kCMIOFeatureControlClassID: Int](/documentation/coremediaio/kcmiofeaturecontrolclassid)
- [var kCMIOSelectorControlClassID: Int](/documentation/coremediaio/kcmioselectorcontrolclassid)
- [CMIOControl properties](/documentation/coremediaio/cmiocontrol-properties)

##### Constants

- [var kCMIOControlPropertyElement: Int](/documentation/coremediaio/kcmiocontrolpropertyelement)
- [var kCMIOControlPropertyScope: Int](/documentation/coremediaio/kcmiocontrolpropertyscope)
- [var kCMIOControlPropertyVariant: Int](/documentation/coremediaio/kcmiocontrolpropertyvariant)
- [CMIODeckShuttle speed constants](/documentation/coremediaio/cmiodeckshuttle-speed-constants)

##### Constants

- [var kCMIODeckShuttlePause: Int](/documentation/coremediaio/kcmiodeckshuttlepause)
- [var kCMIODeckShuttlePlay1x: Int](/documentation/coremediaio/kcmiodeckshuttleplay1x)
- [var kCMIODeckShuttlePlayFast: Int](/documentation/coremediaio/kcmiodeckshuttleplayfast)
- [var kCMIODeckShuttlePlayFaster: Int](/documentation/coremediaio/kcmiodeckshuttleplayfaster)
- [var kCMIODeckShuttlePlayFastest: Int](/documentation/coremediaio/kcmiodeckshuttleplayfastest)
- [var kCMIODeckShuttlePlayHighSpeed: Int](/documentation/coremediaio/kcmiodeckshuttleplayhighspeed)
- [var kCMIODeckShuttlePlayNextFrame: Int](/documentation/coremediaio/kcmiodeckshuttleplaynextframe)
- [var kCMIODeckShuttlePlayPreviousFrame: Int](/documentation/coremediaio/kcmiodeckshuttleplaypreviousframe)
- [var kCMIODeckShuttlePlaySlow1: Int](/documentation/coremediaio/kcmiodeckshuttleplayslow1)
- [var kCMIODeckShuttlePlaySlow2: Int](/documentation/coremediaio/kcmiodeckshuttleplayslow2)
- [var kCMIODeckShuttlePlaySlow3: Int](/documentation/coremediaio/kcmiodeckshuttleplayslow3)
- [var kCMIODeckShuttlePlaySlowest: Int](/documentation/coremediaio/kcmiodeckshuttleplayslowest)
- [var kCMIODeckShuttleReverse1x: Int](/documentation/coremediaio/kcmiodeckshuttlereverse1x)
- [var kCMIODeckShuttleReverseFast: Int](/documentation/coremediaio/kcmiodeckshuttlereversefast)
- [var kCMIODeckShuttleReverseFaster: Int](/documentation/coremediaio/kcmiodeckshuttlereversefaster)
- [var kCMIODeckShuttleReverseFastest: Int](/documentation/coremediaio/kcmiodeckshuttlereversefastest)
- [var kCMIODeckShuttleReverseHighSpeed: Int](/documentation/coremediaio/kcmiodeckshuttlereversehighspeed)
- [var kCMIODeckShuttleReverseSlow1: Int](/documentation/coremediaio/kcmiodeckshuttlereverseslow1)
- [var kCMIODeckShuttleReverseSlow2: Int](/documentation/coremediaio/kcmiodeckshuttlereverseslow2)
- [var kCMIODeckShuttleReverseSlow3: Int](/documentation/coremediaio/kcmiodeckshuttlereverseslow3)
- [var kCMIODeckShuttleReverseSlowest: Int](/documentation/coremediaio/kcmiodeckshuttlereverseslowest)
- [CMIODeckState constants](/documentation/coremediaio/cmiodeckstate-constants)

##### Constants

- [var kCMIODeckStateFastForward: Int](/documentation/coremediaio/kcmiodeckstatefastforward)
- [var kCMIODeckStateFastRewind: Int](/documentation/coremediaio/kcmiodeckstatefastrewind)
- [var kCMIODeckStatePause: Int](/documentation/coremediaio/kcmiodeckstatepause)
- [var kCMIODeckStatePlay: Int](/documentation/coremediaio/kcmiodeckstateplay)
- [var kCMIODeckStatePlayReverse: Int](/documentation/coremediaio/kcmiodeckstateplayreverse)
- [var kCMIODeckStatePlaySlow: Int](/documentation/coremediaio/kcmiodeckstateplayslow)
- [var kCMIODeckStateReverseSlow: Int](/documentation/coremediaio/kcmiodeckstatereverseslow)
- [var kCMIODeckStateStop: Int](/documentation/coremediaio/kcmiodeckstatestop)
- [CMIODeckStatus constants](/documentation/coremediaio/cmiodeckstatus-constants)

##### Constants

- [var kCMIODeckStatusBusy: Int](/documentation/coremediaio/kcmiodeckstatusbusy)
- [var kCMIODeckStatusLocal: Int](/documentation/coremediaio/kcmiodeckstatuslocal)
- [var kCMIODeckStatusNoDevice: Int](/documentation/coremediaio/kcmiodeckstatusnodevice)
- [var kCMIODeckStatusNotThreaded: Int](/documentation/coremediaio/kcmiodeckstatusnotthreaded)
- [var kCMIODeckStatusOpcode: Int](/documentation/coremediaio/kcmiodeckstatusopcode)
- [var kCMIODeckStatusSearchingForDevice: Int](/documentation/coremediaio/kcmiodeckstatussearchingfordevice)
- [var kCMIODeckStatusTapeInserted: Int](/documentation/coremediaio/kcmiodeckstatustapeinserted)
- [CMIODevice constants](/documentation/coremediaio/cmiodevice-constants)

##### Constants

- [var kCMIODeviceClassID: Int](/documentation/coremediaio/kcmiodeviceclassid)
- [var kCMIODevicePropertyScopeInput: Int](/documentation/coremediaio/kcmiodevicepropertyscopeinput)
- [var kCMIODevicePropertyScopeOutput: Int](/documentation/coremediaio/kcmiodevicepropertyscopeoutput)
- [var kCMIODevicePropertyScopePlayThrough: Int](/documentation/coremediaio/kcmiodevicepropertyscopeplaythrough)
- [var kCMIODeviceUnknown: Int](/documentation/coremediaio/kcmiodeviceunknown)
- [CMIODevice properties](/documentation/coremediaio/cmiodevice-properties)

##### Constants

- [var kCMIODevicePropertyAVCDeviceSignalMode: Int](/documentation/coremediaio/kcmiodevicepropertyavcdevicesignalmode)
- [var kCMIODevicePropertyAVCDeviceType: Int](/documentation/coremediaio/kcmiodevicepropertyavcdevicetype)
- [var kCMIODevicePropertyCanProcessAVCCommand: Int](/documentation/coremediaio/kcmiodevicepropertycanprocessavccommand)
- [var kCMIODevicePropertyCanProcessRS422Command: Int](/documentation/coremediaio/kcmiodevicepropertycanprocessrs422command)
- [var kCMIODevicePropertyCanSwitchFrameRatesWithoutFrameDrops: Int](/documentation/coremediaio/kcmiodevicepropertycanswitchframerateswithoutframedrops)
- [var kCMIODevicePropertyClientSyncDiscontinuity: Int](/documentation/coremediaio/kcmiodevicepropertyclientsyncdiscontinuity)
- [var kCMIODevicePropertyDeviceCanBeDefaultDevice: Int](/documentation/coremediaio/kcmiodevicepropertydevicecanbedefaultdevice)
- [var kCMIODevicePropertyDeviceHasChanged: Int](/documentation/coremediaio/kcmiodevicepropertydevicehaschanged)
- [var kCMIODevicePropertyDeviceIsAlive: Int](/documentation/coremediaio/kcmiodevicepropertydeviceisalive)
- [var kCMIODevicePropertyDeviceIsRunning: Int](/documentation/coremediaio/kcmiodevicepropertydeviceisrunning)
- [var kCMIODevicePropertyDeviceIsRunningSomewhere: Int](/documentation/coremediaio/kcmiodevicepropertydeviceisrunningsomewhere)
- [var kCMIODevicePropertyDeviceMaster: Int](/documentation/coremediaio/kcmiodevicepropertydevicemaster)
- [var kCMIODevicePropertyDeviceUID: Int](/documentation/coremediaio/kcmiodevicepropertydeviceuid)
- [var kCMIODevicePropertyExcludeNonDALAccess: Int](/documentation/coremediaio/kcmiodevicepropertyexcludenondalaccess)
- [var kCMIODevicePropertyHogMode: Int](/documentation/coremediaio/kcmiodevicepropertyhogmode)
- [var kCMIODevicePropertyIIDCCSRData: Int](/documentation/coremediaio/kcmiodevicepropertyiidccsrdata)
- [var kCMIODevicePropertyIIDCInitialUnitSpace: Int](/documentation/coremediaio/kcmiodevicepropertyiidcinitialunitspace)
- [var kCMIODevicePropertyLatency: Int](/documentation/coremediaio/kcmiodevicepropertylatency)
- [var kCMIODevicePropertyLinkedAndSyncedCoreAudioDeviceUID: Int](/documentation/coremediaio/kcmiodevicepropertylinkedandsyncedcoreaudiodeviceuid)
- [var kCMIODevicePropertyLinkedCoreAudioDeviceUID: Int](/documentation/coremediaio/kcmiodevicepropertylinkedcoreaudiodeviceuid)
- [var kCMIODevicePropertyModelUID: Int](/documentation/coremediaio/kcmiodevicepropertymodeluid)
- [var kCMIODevicePropertyPlugIn: Int](/documentation/coremediaio/kcmiodevicepropertyplugin)
- [var kCMIODevicePropertySMPTETimeCallback: Int](/documentation/coremediaio/kcmiodevicepropertysmptetimecallback)
- [var kCMIODevicePropertyStreamConfiguration: Int](/documentation/coremediaio/kcmiodevicepropertystreamconfiguration)
- [var kCMIODevicePropertyStreams: Int](/documentation/coremediaio/kcmiodevicepropertystreams)
- [var kCMIODevicePropertySuspendedByUser: Int](/documentation/coremediaio/kcmiodevicepropertysuspendedbyuser)
- [var kCMIODevicePropertyTransportType: Int](/documentation/coremediaio/kcmiodevicepropertytransporttype)
- [var kCMIODevicePropertyVideoDigitizerComponents: Int](/documentation/coremediaio/kcmiodevicepropertyvideodigitizercomponents)
- [var kCMIODevicePropertyDeviceControl: Int](/documentation/coremediaio/kcmiodevicepropertydevicecontrol)
- [var kCMIODevicePropertyDeviceHasStreamingError: Int](/documentation/coremediaio/kcmiodevicepropertydevicehasstreamingerror)
- [var kCMIODevicePropertyLocation: Int](/documentation/coremediaio/kcmiodevicepropertylocation)
- [CMIODeviceAVCSignal mode types](/documentation/coremediaio/cmiodeviceavcsignal-mode-types)

##### Constants

- [var kCMIODeviceAVCSignalMode8mmNTSC: Int](/documentation/coremediaio/kcmiodeviceavcsignalmode8mmntsc)
- [var kCMIODeviceAVCSignalMode8mmPAL: Int](/documentation/coremediaio/kcmiodeviceavcsignalmode8mmpal)
- [var kCMIODeviceAVCSignalModeAudio: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodeaudio)
- [var kCMIODeviceAVCSignalModeDVCPro100_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodedvcpro100_50)
- [var kCMIODeviceAVCSignalModeDVCPro100_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodedvcpro100_60)
- [var kCMIODeviceAVCSignalModeDVCPro25_525_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodedvcpro25_525_60)
- [var kCMIODeviceAVCSignalModeDVCPro25_625_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodedvcpro25_625_50)
- [var kCMIODeviceAVCSignalModeDVCPro50_525_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodedvcpro50_525_60)
- [var kCMIODeviceAVCSignalModeDVCPro50_625_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodedvcpro50_625_50)
- [var kCMIODeviceAVCSignalModeDVHS: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodedvhs)
- [var kCMIODeviceAVCSignalModeHD1125_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehd1125_60)
- [var kCMIODeviceAVCSignalModeHD1250_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehd1250_50)
- [var kCMIODeviceAVCSignalModeHDV1_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehdv1_50)
- [var kCMIODeviceAVCSignalModeHDV1_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehdv1_60)
- [var kCMIODeviceAVCSignalModeHDV2_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehdv2_50)
- [var kCMIODeviceAVCSignalModeHDV2_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehdv2_60)
- [var kCMIODeviceAVCSignalModeHi8NTSC: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehi8ntsc)
- [var kCMIODeviceAVCSignalModeHi8PAL: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodehi8pal)
- [var kCMIODeviceAVCSignalModeMPEG12Mbps_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodempeg12mbps_50)
- [var kCMIODeviceAVCSignalModeMPEG12Mbps_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodempeg12mbps_60)
- [var kCMIODeviceAVCSignalModeMPEG25Mbps_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodempeg25mbps_50)
- [var kCMIODeviceAVCSignalModeMPEG25Mbps_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodempeg25mbps_60)
- [var kCMIODeviceAVCSignalModeMPEG6Mbps_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodempeg6mbps_50)
- [var kCMIODeviceAVCSignalModeMPEG6Mbps_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodempeg6mbps_60)
- [var kCMIODeviceAVCSignalModeMicroMV12Mbps_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodemicromv12mbps_50)
- [var kCMIODeviceAVCSignalModeMicroMV12Mbps_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodemicromv12mbps_60)
- [var kCMIODeviceAVCSignalModeMicroMV6Mbps_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodemicromv6mbps_50)
- [var kCMIODeviceAVCSignalModeMicroMV6Mbps_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodemicromv6mbps_60)
- [var kCMIODeviceAVCSignalModeSD525_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodesd525_60)
- [var kCMIODeviceAVCSignalModeSD625_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodesd625_50)
- [var kCMIODeviceAVCSignalModeSDL525_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodesdl525_60)
- [var kCMIODeviceAVCSignalModeSDL625_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodesdl625_50)
- [var kCMIODeviceAVCSignalModeSVHS525_60: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodesvhs525_60)
- [var kCMIODeviceAVCSignalModeSVHS625_50: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodesvhs625_50)
- [var kCMIODeviceAVCSignalModeVHSMESECAM: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodevhsmesecam)
- [var kCMIODeviceAVCSignalModeVHSMPAL: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodevhsmpal)
- [var kCMIODeviceAVCSignalModeVHSNPAL: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodevhsnpal)
- [var kCMIODeviceAVCSignalModeVHSNTSC: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodevhsntsc)
- [var kCMIODeviceAVCSignalModeVHSPAL: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodevhspal)
- [var kCMIODeviceAVCSignalModeVHSSECAM: Int](/documentation/coremediaio/kcmiodeviceavcsignalmodevhssecam)
- [CMIODevicePropertyLocation constants](/documentation/coremediaio/cmiodevicepropertylocation-values)

##### Constants

- [var kCMIODevicePropertyLocationBuiltInDisplay: Int](/documentation/coremediaio/kcmiodevicepropertylocationbuiltindisplay)
- [var kCMIODevicePropertyLocationExternalDevice: Int](/documentation/coremediaio/kcmiodevicepropertylocationexternaldevice)
- [var kCMIODevicePropertyLocationExternalDisplay: Int](/documentation/coremediaio/kcmiodevicepropertylocationexternaldisplay)
- [var kCMIODevicePropertyLocationExternalWirelessDevice: Int](/documentation/coremediaio/kcmiodevicepropertylocationexternalwirelessdevice)
- [var kCMIODevicePropertyLocationUnknown: Int](/documentation/coremediaio/kcmiodevicepropertylocationunknown)
- [CMIOExposureControl properties](/documentation/coremediaio/cmioexposurecontrol-properties)

##### Constants

- [var kCMIOExposureControlPropertyConvergenceSpeed: Int](/documentation/coremediaio/kcmioexposurecontrolpropertyconvergencespeed)
- [var kCMIOExposureControlPropertyIntegrationTime: Int](/documentation/coremediaio/kcmioexposurecontrolpropertyintegrationtime)
- [var kCMIOExposureControlPropertyLockThreshold: Int](/documentation/coremediaio/kcmioexposurecontrolpropertylockthreshold)
- [var kCMIOExposureControlPropertyMaximumGain: Int](/documentation/coremediaio/kcmioexposurecontrolpropertymaximumgain)
- [var kCMIOExposureControlPropertyRegionOfInterest: Int](/documentation/coremediaio/kcmioexposurecontrolpropertyregionofinterest)
- [var kCMIOExposureControlPropertyStability: Int](/documentation/coremediaio/kcmioexposurecontrolpropertystability)
- [var kCMIOExposureControlPropertyStable: Int](/documentation/coremediaio/kcmioexposurecontrolpropertystable)
- [var kCMIOExposureControlPropertyTarget: Int](/documentation/coremediaio/kcmioexposurecontrolpropertytarget)
- [var kCMIOExposureControlPropertyUnlockThreshold: Int](/documentation/coremediaio/kcmioexposurecontrolpropertyunlockthreshold)
- [CMIOFeatureControl properties](/documentation/coremediaio/cmiofeaturecontrol-properties)

##### Constants

- [var kCMIOFeatureControlPropertyAbsoluteNative: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyabsolutenative)
- [var kCMIOFeatureControlPropertyAbsoluteRange: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyabsoluterange)
- [var kCMIOFeatureControlPropertyAbsoluteUnitName: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyabsoluteunitname)
- [var kCMIOFeatureControlPropertyAbsoluteValue: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyabsolutevalue)
- [var kCMIOFeatureControlPropertyAutomaticManual: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyautomaticmanual)
- [var kCMIOFeatureControlPropertyConvertAbsoluteToNative: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyconvertabsolutetonative)
- [var kCMIOFeatureControlPropertyConvertNativeToAbsolute: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyconvertnativetoabsolute)
- [var kCMIOFeatureControlPropertyNativeRange: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertynativerange)
- [var kCMIOFeatureControlPropertyNativeValue: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertynativevalue)
- [var kCMIOFeatureControlPropertyOnOff: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertyonoff)
- [var kCMIOFeatureControlPropertyTune: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertytune)
- [var kCMIOFeatureControlPropertyNativeData: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertynativedata)
- [var kCMIOFeatureControlPropertyNativeDataRange: Int](/documentation/coremediaio/kcmiofeaturecontrolpropertynativedatarange)
- [CMIOFeatureControl subclass IDs](/documentation/coremediaio/cmiofeaturecontrol-subclass-ids)

##### Constants

- [var kCMIOBacklightCompensationControlClassID: Int](/documentation/coremediaio/kcmiobacklightcompensationcontrolclassid)
- [var kCMIOBlackLevelControlClassID: Int](/documentation/coremediaio/kcmioblacklevelcontrolclassid)
- [var kCMIOBrightnessControlClassID: Int](/documentation/coremediaio/kcmiobrightnesscontrolclassid)
- [var kCMIOContrastControlClassID: Int](/documentation/coremediaio/kcmiocontrastcontrolclassid)
- [var kCMIOExposureControlClassID: Int](/documentation/coremediaio/kcmioexposurecontrolclassid)
- [var kCMIOFocusControlClassID: Int](/documentation/coremediaio/kcmiofocuscontrolclassid)
- [var kCMIOGainControlClassID: Int](/documentation/coremediaio/kcmiogaincontrolclassid)
- [var kCMIOGammaControlClassID: Int](/documentation/coremediaio/kcmiogammacontrolclassid)
- [var kCMIOHueControlClassID: Int](/documentation/coremediaio/kcmiohuecontrolclassid)
- [var kCMIOIrisControlClassID: Int](/documentation/coremediaio/kcmioiriscontrolclassid)
- [var kCMIONoiseReductionControlClassID: Int](/documentation/coremediaio/kcmionoisereductioncontrolclassid)
- [var kCMIOOpticalFilterClassID: Int](/documentation/coremediaio/kcmioopticalfilterclassid)
- [var kCMIOPanControlClassID: Int](/documentation/coremediaio/kcmiopancontrolclassid)
- [var kCMIOPowerLineFrequencyControlClassID: Int](/documentation/coremediaio/kcmiopowerlinefrequencycontrolclassid)
- [var kCMIOSaturationControlClassID: Int](/documentation/coremediaio/kcmiosaturationcontrolclassid)
- [var kCMIOSharpnessControlClassID: Int](/documentation/coremediaio/kcmiosharpnesscontrolclassid)
- [var kCMIOShutterControlClassID: Int](/documentation/coremediaio/kcmioshuttercontrolclassid)
- [var kCMIOTemperatureControlClassID: Int](/documentation/coremediaio/kcmiotemperaturecontrolclassid)
- [var kCMIOTiltControlClassID: Int](/documentation/coremediaio/kcmiotiltcontrolclassid)
- [var kCMIOWhiteBalanceControlClassID: Int](/documentation/coremediaio/kcmiowhitebalancecontrolclassid)
- [var kCMIOWhiteBalanceUControlClassID: Int](/documentation/coremediaio/kcmiowhitebalanceucontrolclassid)
- [var kCMIOWhiteBalanceVControlClassID: Int](/documentation/coremediaio/kcmiowhitebalancevcontrolclassid)
- [var kCMIOWhiteLevelControlClassID: Int](/documentation/coremediaio/kcmiowhitelevelcontrolclassid)
- [var kCMIOZoomControlClassID: Int](/documentation/coremediaio/kcmiozoomcontrolclassid)
- [var kCMIOPanTiltAbsoluteControlClassID: Int](/documentation/coremediaio/kcmiopantiltabsolutecontrolclassid)
- [var kCMIOPanTiltRelativeControlClassID: Int](/documentation/coremediaio/kcmiopantiltrelativecontrolclassid)
- [var kCMIORollAbsoluteControlClassID: Int](/documentation/coremediaio/kcmiorollabsolutecontrolclassid)
- [var kCMIOZoomRelativeControlClassID: Int](/documentation/coremediaio/kcmiozoomrelativecontrolclassid)
- [CMIOObject constants](/documentation/coremediaio/cmioobject-constants)

##### Constants

- [var kCMIOObjectClassID: Int](/documentation/coremediaio/kcmioobjectclassid)
- [var kCMIOObjectClassIDWildcard: Int](/documentation/coremediaio/kcmioobjectclassidwildcard)
- [var kCMIOObjectPropertyElementMaster: Int](/documentation/coremediaio/kcmioobjectpropertyelementmaster)
- [var kCMIOObjectPropertyScopeGlobal: Int](/documentation/coremediaio/kcmioobjectpropertyscopeglobal)
- [var kCMIOObjectUnknown: Int](/documentation/coremediaio/kcmioobjectunknown)
- [var kCMIOObjectPropertyElementMain: Int](/documentation/coremediaio/kcmioobjectpropertyelementmain)
- [CMIOObject properties](/documentation/coremediaio/cmioobject-properties)

##### Constants

- [var kCMIOObjectPropertyClass: Int](/documentation/coremediaio/kcmioobjectpropertyclass)
- [var kCMIOObjectPropertyCreator: Int](/documentation/coremediaio/kcmioobjectpropertycreator)
- [var kCMIOObjectPropertyElementCategoryName: Int](/documentation/coremediaio/kcmioobjectpropertyelementcategoryname)
- [var kCMIOObjectPropertyElementName: Int](/documentation/coremediaio/kcmioobjectpropertyelementname)
- [var kCMIOObjectPropertyElementNumberName: Int](/documentation/coremediaio/kcmioobjectpropertyelementnumbername)
- [var kCMIOObjectPropertyListenerAdded: Int](/documentation/coremediaio/kcmioobjectpropertylisteneradded)
- [var kCMIOObjectPropertyListenerRemoved: Int](/documentation/coremediaio/kcmioobjectpropertylistenerremoved)
- [var kCMIOObjectPropertyManufacturer: Int](/documentation/coremediaio/kcmioobjectpropertymanufacturer)
- [var kCMIOObjectPropertyName: Int](/documentation/coremediaio/kcmioobjectpropertyname)
- [var kCMIOObjectPropertyOwnedObjects: Int](/documentation/coremediaio/kcmioobjectpropertyownedobjects)
- [var kCMIOObjectPropertyOwner: Int](/documentation/coremediaio/kcmioobjectpropertyowner)
- [CMIOObject property wildcard constants](/documentation/coremediaio/cmioobject-property-wildcard-constants)

##### Wildcards

- [var kCMIOObjectPropertyElementWildcard: UInt32](/documentation/coremediaio/kcmioobjectpropertyelementwildcard)
- [var kCMIOObjectPropertyScopeWildcard: UInt32](/documentation/coremediaio/kcmioobjectpropertyscopewildcard)
- [var kCMIOObjectPropertySelectorWildcard: UInt32](/documentation/coremediaio/kcmioobjectpropertyselectorwildcard)
- [CMIOPlugIn constants](/documentation/coremediaio/cmioplugin-constants)

##### Constants

- [var kCMIOPlugInClassID: Int](/documentation/coremediaio/kcmiopluginclassid)
- [CMIOPlugIn properties](/documentation/coremediaio/cmioplugin-properties)

##### Constants

- [var kCMIOPlugInPropertyBundleID: Int](/documentation/coremediaio/kcmiopluginpropertybundleid)
- [var kCMIOPlugInPropertyIsExtension: Int](/documentation/coremediaio/kcmiopluginpropertyisextension)
- [CMIOSampleBuffer attachment constants](/documentation/coremediaio/cmiosamplebufferattachment-constants)
- [CMIOSampleBuffer no-data event constants](/documentation/coremediaio/cmiosamplebuffer-no-data-event-constants)
- [CMIOSampleBuffer discontinuity flags](/documentation/coremediaio/cmiosamplebuffer-discontinuity-flag-constants)
- [CMIOSelectorControl properties](/documentation/coremediaio/cmioselectorcontrol-properties)

##### Constants

- [var kCMIOSelectorControlPropertyAvailableItems: Int](/documentation/coremediaio/kcmioselectorcontrolpropertyavailableitems)
- [var kCMIOSelectorControlPropertyCurrentItem: Int](/documentation/coremediaio/kcmioselectorcontrolpropertycurrentitem)
- [var kCMIOSelectorControlPropertyItemName: Int](/documentation/coremediaio/kcmioselectorcontrolpropertyitemname)
- [var kCMIOSelectorControlPropertyAvailableItemNames: Int](/documentation/coremediaio/kcmioselectorcontrolpropertyavailableitemnames)
- [CMIOSelectorControl subclass IDs](/documentation/coremediaio/cmioselectorcontrol-subclass-ids)

##### Constants

- [var kCMIODataDestinationControlClassID: Int](/documentation/coremediaio/kcmiodatadestinationcontrolclassid)
- [var kCMIODataSourceControlClassID: Int](/documentation/coremediaio/kcmiodatasourcecontrolclassid)
- [CMIOStream constants](/documentation/coremediaio/cmiostream-constants)

##### Constants

- [var kCMIOStreamClassID: Int](/documentation/coremediaio/kcmiostreamclassid)
- [var kCMIOStreamUnknown: Int](/documentation/coremediaio/kcmiostreamunknown)
- [CMIOStream properties](/documentation/coremediaio/cmiostream-properties)

##### Constants

- [var kCMIOStreamPropertyCanProcessDeckCommand: Int](/documentation/coremediaio/kcmiostreampropertycanprocessdeckcommand)
- [var kCMIOStreamPropertyClock: Int](/documentation/coremediaio/kcmiostreampropertyclock)
- [var kCMIOStreamPropertyDeck: Int](/documentation/coremediaio/kcmiostreampropertydeck)
- [var kCMIOStreamPropertyDeckCueing: Int](/documentation/coremediaio/kcmiostreampropertydeckcueing)
- [var kCMIOStreamPropertyDeckDropness: Int](/documentation/coremediaio/kcmiostreampropertydeckdropness)
- [var kCMIOStreamPropertyDeckFrameNumber: Int](/documentation/coremediaio/kcmiostreampropertydeckframenumber)
- [var kCMIOStreamPropertyDeckLocal: Int](/documentation/coremediaio/kcmiostreampropertydecklocal)
- [var kCMIOStreamPropertyDeckThreaded: Int](/documentation/coremediaio/kcmiostreampropertydeckthreaded)
- [var kCMIOStreamPropertyDeviceSyncTimeoutInMSec: Int](/documentation/coremediaio/kcmiostreampropertydevicesynctimeoutinmsec)
- [var kCMIOStreamPropertyDirection: Int](/documentation/coremediaio/kcmiostreampropertydirection)
- [var kCMIOStreamPropertyEndOfData: Int](/documentation/coremediaio/kcmiostreampropertyendofdata)
- [var kCMIOStreamPropertyFirstOutputPresentationTimeStamp: Int](/documentation/coremediaio/kcmiostreampropertyfirstoutputpresentationtimestamp)
- [var kCMIOStreamPropertyFormatDescription: Int](/documentation/coremediaio/kcmiostreampropertyformatdescription)
- [var kCMIOStreamPropertyFormatDescriptions: Int](/documentation/coremediaio/kcmiostreampropertyformatdescriptions)
- [var kCMIOStreamPropertyFrameRate: Int](/documentation/coremediaio/kcmiostreampropertyframerate)
- [var kCMIOStreamPropertyFrameRateRanges: Int](/documentation/coremediaio/kcmiostreampropertyframerateranges)
- [var kCMIOStreamPropertyFrameRates: Int](/documentation/coremediaio/kcmiostreampropertyframerates)
- [var kCMIOStreamPropertyInitialPresentationTimeStampForLinkedAndSyncedAudio: Int](/documentation/coremediaio/kcmiostreampropertyinitialpresentationtimestampforlinkedandsyncedaudio)
- [var kCMIOStreamPropertyLatency: Int](/documentation/coremediaio/kcmiostreampropertylatency)
- [var kCMIOStreamPropertyMinimumFrameRate: Int](/documentation/coremediaio/kcmiostreampropertyminimumframerate)
- [var kCMIOStreamPropertyNoDataEventCount: Int](/documentation/coremediaio/kcmiostreampropertynodataeventcount)
- [var kCMIOStreamPropertyNoDataTimeoutInMSec: Int](/documentation/coremediaio/kcmiostreampropertynodatatimeoutinmsec)
- [var kCMIOStreamPropertyOutputBufferQueueSize: Int](/documentation/coremediaio/kcmiostreampropertyoutputbufferqueuesize)
- [var kCMIOStreamPropertyOutputBufferRepeatCount: Int](/documentation/coremediaio/kcmiostreampropertyoutputbufferrepeatcount)
- [var kCMIOStreamPropertyOutputBufferUnderrunCount: Int](/documentation/coremediaio/kcmiostreampropertyoutputbufferunderruncount)
- [var kCMIOStreamPropertyOutputBuffersNeededForThrottledPlayback: Int](/documentation/coremediaio/kcmiostreampropertyoutputbuffersneededforthrottledplayback)
- [var kCMIOStreamPropertyOutputBuffersRequiredForStartup: Int](/documentation/coremediaio/kcmiostreampropertyoutputbuffersrequiredforstartup)
- [var kCMIOStreamPropertyPreferredFormatDescription: Int](/documentation/coremediaio/kcmiostreampropertypreferredformatdescription)
- [var kCMIOStreamPropertyPreferredFrameRate: Int](/documentation/coremediaio/kcmiostreampropertypreferredframerate)
- [var kCMIOStreamPropertyScheduledOutputNotificationProc: Int](/documentation/coremediaio/kcmiostreampropertyscheduledoutputnotificationproc)
- [var kCMIOStreamPropertyStartingChannel: Int](/documentation/coremediaio/kcmiostreampropertystartingchannel)
- [var kCMIOStreamPropertyStillImage: Int](/documentation/coremediaio/kcmiostreampropertystillimage)
- [var kCMIOStreamPropertyStillImageFormatDescriptions: Int](/documentation/coremediaio/kcmiostreampropertystillimageformatdescriptions)
- [var kCMIOStreamPropertyTerminalType: Int](/documentation/coremediaio/kcmiostreampropertyterminaltype)
- [CMIOSystemObject constants](/documentation/coremediaio/cmiosystemobject-constants)

##### Constants

- [var kCMIOObjectSystemObject: Int](/documentation/coremediaio/kcmioobjectsystemobject)
- [var kCMIOSystemObjectClassID: Int](/documentation/coremediaio/kcmiosystemobjectclassid)
- [CMIOSystemObject properties](/documentation/coremediaio/cmiosystemobject-properties)

##### Constants

- [var kCMIOHardwarePropertyAllowScreenCaptureDevices: Int](/documentation/coremediaio/kcmiohardwarepropertyallowscreencapturedevices)
- [var kCMIOHardwarePropertyAllowWirelessScreenCaptureDevices: Int](/documentation/coremediaio/kcmiohardwarepropertyallowwirelessscreencapturedevices)
- [var kCMIOHardwarePropertyDefaultInputDevice: Int](/documentation/coremediaio/kcmiohardwarepropertydefaultinputdevice)
- [var kCMIOHardwarePropertyDefaultOutputDevice: Int](/documentation/coremediaio/kcmiohardwarepropertydefaultoutputdevice)
- [var kCMIOHardwarePropertyDeviceForUID: Int](/documentation/coremediaio/kcmiohardwarepropertydeviceforuid)
- [var kCMIOHardwarePropertyDevices: Int](/documentation/coremediaio/kcmiohardwarepropertydevices)
- [var kCMIOHardwarePropertyIsInitingOrExiting: Int](/documentation/coremediaio/kcmiohardwarepropertyisinitingorexiting)
- [var kCMIOHardwarePropertyPlugInForBundleID: Int](/documentation/coremediaio/kcmiohardwarepropertypluginforbundleid)
- [var kCMIOHardwarePropertyProcessIsMain: Int](/documentation/coremediaio/kcmiohardwarepropertyprocessismain)
- [var kCMIOHardwarePropertyProcessIsMaster: Int](/documentation/coremediaio/kcmiohardwarepropertyprocessismaster)
- [var kCMIOHardwarePropertySleepingIsAllowed: Int](/documentation/coremediaio/kcmiohardwarepropertysleepingisallowed)
- [var kCMIOHardwarePropertySuspendedBySystem: Int](/documentation/coremediaio/kcmiohardwarepropertysuspendedbysystem)
- [var kCMIOHardwarePropertyUnloadingIsAllowed: Int](/documentation/coremediaio/kcmiohardwarepropertyunloadingisallowed)
- [var kCMIOHardwarePropertyUserSessionIsActiveOrHeadless: Int](/documentation/coremediaio/kcmiohardwarepropertyusersessionisactiveorheadless)
- [DAL plug-in data types](/documentation/coremediaio/core-media-i-o-data-types)

#### Data Types

- [CMIOClassID](/documentation/coremediaio/cmioclassid)
- [CMIOControlID](/documentation/coremediaio/cmiocontrolid)
- [CMIODeviceGetSMPTETimeProc](/documentation/coremediaio/cmiodevicegetsmptetimeproc)
- [CMIODeviceID](/documentation/coremediaio/cmiodeviceid)
- [CMIODevicePropertyID](/documentation/coremediaio/cmiodevicepropertyid)
- [CMIODeviceStreamQueueAlteredProc](/documentation/coremediaio/cmiodevicestreamqueuealteredproc)
- [CMIOHardwarePropertyID](/documentation/coremediaio/cmiohardwarepropertyid)
- [CMIOObjectID](/documentation/coremediaio/cmioobjectid)
- [CMIOObjectPropertyElement](/documentation/coremediaio/cmioobjectpropertyelement)
- [CMIOObjectPropertyListenerBlock](/documentation/coremediaio/cmioobjectpropertylistenerblock)
- [CMIOObjectPropertyListenerProc](/documentation/coremediaio/cmioobjectpropertylistenerproc)
- [CMIOObjectPropertyScope](/documentation/coremediaio/cmioobjectpropertyscope)
- [CMIOObjectPropertySelector](/documentation/coremediaio/cmioobjectpropertyselector)
- [CMIOStreamID](/documentation/coremediaio/cmiostreamid)
- [CMIOStreamScheduledOutputNotificationProc](/documentation/coremediaio/cmiostreamscheduledoutputnotificationproc)
- [CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty)

##### Provider Properties

- [static let providerName: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/providername)
- [static let providerManufacturer: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/providermanufacturer)

##### Device Properties

- [static let deviceModel: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicemodel)
- [static let deviceIsSuspended: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/deviceissuspended)
- [static let deviceTransportType: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicetransporttype)
- [static let deviceLinkedCoreAudioDeviceUID: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicelinkedcoreaudiodeviceuid)
- [static let deviceCanBeDefaultInputDevice: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicecanbedefaultinputdevice)
- [static let deviceCanBeDefaultOutputDevice: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicecanbedefaultoutputdevice)

##### Stream Properties

- [static let streamActiveFormatIndex: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamactiveformatindex)
- [static let streamFrameDuration: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamframeduration)
- [static let streamMaxFrameDuration: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streammaxframeduration)
- [static let streamSinkBufferQueueSize: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkbufferqueuesize)
- [static let streamSinkBuffersRequiredForStartup: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkbuffersrequiredforstartup)
- [static let streamSinkBufferUnderrunCount: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkbufferunderruncount)
- [static let streamSinkEndOfData: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamsinkendofdata)

##### Type Properties

- [static let deviceLatency: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/devicelatency)
- [static let streamLatency: CMIOExtensionProperty](/documentation/coremediaio/cmioextensionproperty/streamlatency)
- [init(rawValue: String)](/documentation/coremediaio/cmioextensionproperty/init(rawvalue:))
- [DAL plug-in errors](/documentation/coremediaio/core-media-i-o-errors)

#### Constants

- [var kCMIODevicePermissionsError: Int](/documentation/coremediaio/kcmiodevicepermissionserror)
- [var kCMIODeviceUnsupportedFormatError: Int](/documentation/coremediaio/kcmiodeviceunsupportedformaterror)
- [var kCMIOHardwareBadDeviceError: Int](/documentation/coremediaio/kcmiohardwarebaddeviceerror)
- [var kCMIOHardwareBadObjectError: Int](/documentation/coremediaio/kcmiohardwarebadobjecterror)
- [var kCMIOHardwareBadPropertySizeError: Int](/documentation/coremediaio/kcmiohardwarebadpropertysizeerror)
- [var kCMIOHardwareBadStreamError: Int](/documentation/coremediaio/kcmiohardwarebadstreamerror)
- [var kCMIOHardwareIllegalOperationError: Int](/documentation/coremediaio/kcmiohardwareillegaloperationerror)
- [var kCMIOHardwareNoError: Int](/documentation/coremediaio/kcmiohardwarenoerror)
- [var kCMIOHardwareNotRunningError: Int](/documentation/coremediaio/kcmiohardwarenotrunningerror)
- [var kCMIOHardwareNotStoppedError: Int](/documentation/coremediaio/kcmiohardwarenotstoppederror)
- [var kCMIOHardwareSuspendedBySystemError: Int](/documentation/coremediaio/kcmiohardwaresuspendedbysystemerror)
- [var kCMIOHardwareUnknownPropertyError: Int](/documentation/coremediaio/kcmiohardwareunknownpropertyerror)
- [var kCMIOHardwareUnspecifiedError: Int](/documentation/coremediaio/kcmiohardwareunspecifiederror)
- [var kCMIOHardwareUnsupportedOperationError: Int](/documentation/coremediaio/kcmiohardwareunsupportedoperationerror)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
