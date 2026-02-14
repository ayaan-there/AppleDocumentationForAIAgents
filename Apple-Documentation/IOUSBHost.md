# IOUSBHost Documentation

Source: https://sosumi.ai/documentation/iousbhost

---
title: IOUSBHost
source: https://developer.apple.com/documentation/iousbhost
timestamp: 2026-02-13T18:58:26.897Z
---

## Function Drivers

- [IOUSBHostInterface](/documentation/iousbhost/iousbhostinterface)

### Retrieving Function Descriptors

- [var configurationDescriptor: UnsafePointer<IOUSBConfigurationDescriptor>](/documentation/iousbhost/iousbhostinterface/configurationdescriptor)
- [var interfaceDescriptor: UnsafePointer<IOUSBInterfaceDescriptor>](/documentation/iousbhost/iousbhostinterface/interfacedescriptor)

### Managing Pipes

- [func selectAlternateSetting(Int) throws](/documentation/iousbhost/iousbhostinterface/selectalternatesetting(_:))
- [func copyPipe(withAddress: Int) throws -> IOUSBHostPipe](/documentation/iousbhost/iousbhostinterface/copypipe(withaddress:))

### Enabling Power Savings

- [var idleTimeout: TimeInterval](/documentation/iousbhost/iousbhostinterface/idletimeout)
- [func setIdleTimeout(TimeInterval) throws](/documentation/iousbhost/iousbhostinterface/setidletimeout(_:))
- [IOUSBHostPipe](/documentation/iousbhost/iousbhostpipe)

### Sending Bulk and Interrupt I/O

- [IOUSBHostCompletionHandler](/documentation/iousbhost/iousbhostcompletionhandler)
- [let IOUSBHostDefaultControlCompletionTimeout: TimeInterval](/documentation/iousbhost/iousbhostdefaultcontrolcompletiontimeout)
- [func enqueueIORequest(with: NSMutableData?, completionTimeout: TimeInterval, completionHandler: ((IOReturn, Int) -> Void)?) throws](/documentation/iousbhost/iousbhostpipe/enqueueiorequest(with:completiontimeout:completionhandler:))
- [func clearStall() throws](/documentation/iousbhost/iousbhostpipe/clearstall())

### Sending Isochronous I/O

- [IOUSBHostIsochronousCompletionHandler](/documentation/iousbhost/iousbhostisochronouscompletionhandler)
- [IOUSBHostTime](/documentation/iousbhost/iousbhosttime)
- [IOUSBHostIsochronousFrame](/documentation/iousbhost/iousbhostisochronousframe)

#### Frame Structure

- [var status: IOReturn](/documentation/iousbhost/iousbhostisochronousframe/status)
- [var requestCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/requestcount)
- [var completeCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/completecount)
- [var timeStamp: IOUSBHostTime](/documentation/iousbhost/iousbhostisochronousframe/timestamp)

#### Initializing the Structure

- [init()](/documentation/iousbhost/iousbhostisochronousframe/init())

#### Initializers

- [init(status: IOReturn, requestCount: UInt32, completeCount: UInt32, reserved: UInt32, timeStamp: IOUSBHostTime)](/documentation/iousbhost/iousbhostisochronousframe/init(status:requestcount:completecount:reserved:timestamp:))

#### Instance Properties

- [var reserved: UInt32](/documentation/iousbhost/iousbhostisochronousframe/reserved)
- [var completeCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/completecount)
- [var requestCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/requestcount)
- [var reserved: UInt32](/documentation/iousbhost/iousbhostisochronousframe/reserved)
- [var status: IOReturn](/documentation/iousbhost/iousbhostisochronousframe/status)
- [var timeStamp: IOUSBHostTime](/documentation/iousbhost/iousbhostisochronousframe/timestamp)
- [func enqueueIORequest(with: NSMutableData, frameList: UnsafeMutablePointer<IOUSBHostIsochronousFrame>, frameListCount: Int, firstFrameNumber: UInt64, completionHandler: ((IOReturn, UnsafeMutablePointer<IOUSBHostIsochronousFrame>) -> Void)?) throws](/documentation/iousbhost/iousbhostpipe/enqueueiorequest(with:framelist:framelistcount:firstframenumber:completionhandler:))
- [func sendIORequest(with: NSMutableData, frameList: UnsafeMutablePointer<IOUSBHostIsochronousFrame>, frameListCount: Int, firstFrameNumber: UInt64) throws](/documentation/iousbhost/iousbhostpipe/sendiorequest(with:framelist:framelistcount:firstframenumber:))

### Sending Control Requests

- [func IOUSBHostDeviceRequestType(tIOUSBDeviceRequestDirectionValue, tIOUSBDeviceRequestTypeValue, tIOUSBDeviceRequestRecipientValue) -> UInt8](/documentation/iousbhost/iousbhostdevicerequesttype(_:_:_:))
- [let IOUSBHostDefaultControlCompletionTimeout: TimeInterval](/documentation/iousbhost/iousbhostdefaultcontrolcompletiontimeout)
- [IOUSBHostCompletionHandler](/documentation/iousbhost/iousbhostcompletionhandler)

### Managing Periodic Bandwidth

- [IOUSBHostIOSourceDescriptors](/documentation/iousbhost/iousbhostiosourcedescriptors)

#### Descriptors

- [var bcdUSB: UInt16](/documentation/iousbhost/iousbhostiosourcedescriptors/bcdusb)
- [var descriptor: IOUSBEndpointDescriptor](/documentation/iousbhost/iousbhostiosourcedescriptors/descriptor)
- [var ssCompanionDescriptor: IOUSBSuperSpeedEndpointCompanionDescriptor](/documentation/iousbhost/iousbhostiosourcedescriptors/sscompaniondescriptor)
- [var sspCompanionDescriptor: IOUSBSuperSpeedPlusIsochronousEndpointCompanionDescriptor](/documentation/iousbhost/iousbhostiosourcedescriptors/sspcompaniondescriptor)

#### Initializing the Structure

- [init()](/documentation/iousbhost/iousbhostiosourcedescriptors/init())
- [init(bcdUSB: UInt16, descriptor: IOUSBEndpointDescriptor, ssCompanionDescriptor: IOUSBSuperSpeedEndpointCompanionDescriptor, sspCompanionDescriptor: IOUSBSuperSpeedPlusIsochronousEndpointCompanionDescriptor)](/documentation/iousbhost/iousbhostiosourcedescriptors/init(bcdusb:descriptor:sscompaniondescriptor:sspcompaniondescriptor:))
- [func adjust(with: UnsafePointer<IOUSBHostIOSourceDescriptors>) throws](/documentation/iousbhost/iousbhostpipe/adjust(with:))
- [var descriptors: UnsafePointer<IOUSBHostIOSourceDescriptors>](/documentation/iousbhost/iousbhostpipe/descriptors)
- [var originalDescriptors: UnsafePointer<IOUSBHostIOSourceDescriptors>](/documentation/iousbhost/iousbhostpipe/originaldescriptors)

### Enabling Power Savings

- [func setIdleTimeout(TimeInterval) throws](/documentation/iousbhost/iousbhostpipe/setidletimeout(_:))
- [var idleTimeout: TimeInterval](/documentation/iousbhost/iousbhostpipe/idletimeout)

### Managing Streams

- [func enableStreams() throws](/documentation/iousbhost/iousbhostpipe/enablestreams())
- [func copyStream(withStreamID: Int) throws -> IOUSBHostStream](/documentation/iousbhost/iousbhostpipe/copystream(withstreamid:))
- [func disableStreams() throws](/documentation/iousbhost/iousbhostpipe/disablestreams())

### Instance Methods

- [func enqueueIORequest(with: NSMutableData, transactionList: UnsafeMutablePointer<IOUSBHostIsochronousTransaction>, transactionListCount: Int, firstFrameNumber: UInt64, options: IOUSBHostIsochronousTransferOptions, completionHandler: ((IOReturn, UnsafeMutablePointer<IOUSBHostIsochronousTransaction>) -> Void)?) throws](/documentation/iousbhost/iousbhostpipe/enqueueiorequest(with:transactionlist:transactionlistcount:firstframenumber:options:completionhandler:))
- [func sendIORequest(with: NSMutableData, transactionList: UnsafeMutablePointer<IOUSBHostIsochronousTransaction>, transactionListCount: Int, firstFrameNumber: UInt64, options: IOUSBHostIsochronousTransferOptions) throws](/documentation/iousbhost/iousbhostpipe/sendiorequest(with:transactionlist:transactionlistcount:firstframenumber:options:))
- [IOUSBHostStream](/documentation/iousbhost/iousbhoststream)

### Sending I/O

- [IOUSBHostCompletionHandler](/documentation/iousbhost/iousbhostcompletionhandler)
- [func enqueueIORequest(with: NSMutableData?, completionHandler: ((IOReturn, Int) -> Void)?) throws](/documentation/iousbhost/iousbhoststream/enqueueiorequest(with:completionhandler:))
- [func abort(with: IOUSBHostAbortOption) throws](/documentation/iousbhost/iousbhoststream/abort(with:))

#### Options

- [IOUSBHostAbortOption](/documentation/iousbhost/iousbhostabortoption)

##### Options

- [case synchronous](/documentation/iousbhost/iousbhostabortoption/synchronous)
- [case asynchronous](/documentation/iousbhost/iousbhostabortoption/asynchronous)

##### Initializers

- [init?(rawValue: UInt)](/documentation/iousbhost/iousbhostabortoption/init(rawvalue:))
- [func abort() throws](/documentation/iousbhost/iousbhoststream/abort())

### Getting the Pipe Object

- [var hostPipe: IOUSBHostPipe](/documentation/iousbhost/iousbhoststream/hostpipe)

### Getting the Stream ID

- [var streamID: Int](/documentation/iousbhost/iousbhoststream/streamid)

## Device Drivers

- [IOUSBHostDevice](/documentation/iousbhost/iousbhostdevice)

### Retrieving Device Descriptors

- [var configurationDescriptor: UnsafePointer<IOUSBConfigurationDescriptor>?](/documentation/iousbhost/iousbhostdevice/configurationdescriptor)

### Resetting the Device

- [func reset() throws](/documentation/iousbhost/iousbhostdevice/reset())

## Base Classes

- [IOUSBHostObject](/documentation/iousbhost/iousbhostobject)

### Managing the Object Life Cycle

- [IOUSBHostObjectInitOptions](/documentation/iousbhost/iousbhostobjectinitoptions)

#### Options

- [static var deviceCapture: IOUSBHostObjectInitOptions](/documentation/iousbhost/iousbhostobjectinitoptions/devicecapture)

#### Initializing the Structure

- [init(rawValue: UInt)](/documentation/iousbhost/iousbhostobjectinitoptions/init(rawvalue:))

#### Type Properties

- [static var deviceSeize: IOUSBHostObjectInitOptions](/documentation/iousbhost/iousbhostobjectinitoptions/deviceseize)
- [IOUSBHostInterestHandler](/documentation/iousbhost/iousbhostinteresthandler)
- [var ioService: io_service_t](/documentation/iousbhost/iousbhostobject/ioservice)
- [var queue: dispatch_queue_t](/documentation/iousbhost/iousbhostobject/queue)
- [func destroy()](/documentation/iousbhost/iousbhostobject/destroy())

### Retrieving Base Class Descriptors

- [Parsing USB Descriptors](/documentation/iousbhost/parsing-usb-descriptors)

#### Configuration Descriptor Parsing

- [func IOUSBGetNextDescriptor(UnsafePointer<IOUSBConfigurationDescriptor>!, UnsafePointer<IOUSBDescriptorHeader>!) -> UnsafePointer<IOUSBDescriptorHeader>!](/documentation/iousbhost/iousbgetnextdescriptor(_:_:))
- [func IOUSBGetNextDescriptorWithType(UnsafePointer<IOUSBConfigurationDescriptor>!, UnsafePointer<IOUSBDescriptorHeader>!, UInt8) -> UnsafePointer<IOUSBDescriptorHeader>!](/documentation/iousbhost/iousbgetnextdescriptorwithtype(_:_:_:))
- [func IOUSBGetNextAssociatedDescriptor(UnsafePointer<IOUSBConfigurationDescriptor>!, UnsafePointer<IOUSBDescriptorHeader>!, UnsafePointer<IOUSBDescriptorHeader>!) -> UnsafePointer<IOUSBDescriptorHeader>!](/documentation/iousbhost/iousbgetnextassociateddescriptor(_:_:_:))
- [func IOUSBGetNextAssociatedDescriptorWithType(UnsafePointer<IOUSBConfigurationDescriptor>!, UnsafePointer<IOUSBDescriptorHeader>!, UnsafePointer<IOUSBDescriptorHeader>!, UInt8) -> UnsafePointer<IOUSBDescriptorHeader>!](/documentation/iousbhost/iousbgetnextassociateddescriptorwithtype(_:_:_:_:))
- [func IOUSBGetNextInterfaceAssociationDescriptor(UnsafePointer<IOUSBConfigurationDescriptor>!, UnsafePointer<IOUSBDescriptorHeader>!) -> UnsafePointer<IOUSBInterfaceAssociationDescriptor>!](/documentation/iousbhost/iousbgetnextinterfaceassociationdescriptor(_:_:))
- [func IOUSBGetNextInterfaceDescriptor(UnsafePointer<IOUSBConfigurationDescriptor>!, UnsafePointer<IOUSBDescriptorHeader>!) -> UnsafePointer<IOUSBInterfaceDescriptor>!](/documentation/iousbhost/iousbgetnextinterfacedescriptor(_:_:))
- [func IOUSBGetConfigurationMaxPowerMilliAmps(UInt32, UnsafePointer<IOUSBConfigurationDescriptor>!) -> UInt32](/documentation/iousbhost/iousbgetconfigurationmaxpowermilliamps(_:_:))

#### BOS Descriptor Parsing

- [func IOUSBGetUSB20ExtensionDeviceCapabilityDescriptor(UnsafePointer<IOUSBBOSDescriptor>!) -> UnsafePointer<IOUSBDeviceCapabilityUSB2Extension>!](/documentation/iousbhost/iousbgetusb20extensiondevicecapabilitydescriptor(_:))
- [func IOUSBGetNextCapabilityDescriptorWithType(UnsafePointer<IOUSBBOSDescriptor>!, UnsafePointer<IOUSBDeviceCapabilityDescriptorHeader>!, UInt8) -> UnsafePointer<IOUSBDeviceCapabilityDescriptorHeader>!](/documentation/iousbhost/iousbgetnextcapabilitydescriptorwithtype(_:_:_:))
- [func IOUSBGetNextCapabilityDescriptor(UnsafePointer<IOUSBBOSDescriptor>!, UnsafePointer<IOUSBDeviceCapabilityDescriptorHeader>!) -> UnsafePointer<IOUSBDeviceCapabilityDescriptorHeader>!](/documentation/iousbhost/iousbgetnextcapabilitydescriptor(_:_:))
- [func IOUSBGetSuperSpeedDeviceCapabilityDescriptor(UnsafePointer<IOUSBBOSDescriptor>!) -> UnsafePointer<IOUSBDeviceCapabilitySuperSpeedUSB>!](/documentation/iousbhost/iousbgetsuperspeeddevicecapabilitydescriptor(_:))
- [func IOUSBGetContainerIDDescriptor(UnsafePointer<IOUSBBOSDescriptor>!) -> UnsafePointer<IOUSBDeviceCapabilityContainerID>!](/documentation/iousbhost/iousbgetcontaineriddescriptor(_:))
- [func IOUSBGetBillboardDescriptor(UnsafePointer<IOUSBBOSDescriptor>!) -> UnsafePointer<IOUSBDeviceCapabilityBillboard>!](/documentation/iousbhost/iousbgetbillboarddescriptor(_:))

#### Endpoint Descriptor Parsing

- [func IOUSBGetNextEndpointDescriptor(UnsafePointer<IOUSBConfigurationDescriptor>!, UnsafePointer<IOUSBInterfaceDescriptor>!, UnsafePointer<IOUSBDescriptorHeader>!) -> UnsafePointer<IOUSBEndpointDescriptor>!](/documentation/iousbhost/iousbgetnextendpointdescriptor(_:_:_:))
- [func IOUSBGetEndpointDirection(UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt8](/documentation/iousbhost/iousbgetendpointdirection(_:))
- [func IOUSBGetEndpointAddress(UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt8](/documentation/iousbhost/iousbgetendpointaddress(_:))
- [func IOUSBGetEndpointNumber(UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt8](/documentation/iousbhost/iousbgetendpointnumber(_:))
- [func IOUSBGetEndpointType(UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt8](/documentation/iousbhost/iousbgetendpointtype(_:))
- [func IOUSBGetEndpointMaxPacketSize(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt16](/documentation/iousbhost/iousbgetendpointmaxpacketsize(_:_:))
- [func IOUSBGetEndpointIntervalEncodedMicroframes(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt32](/documentation/iousbhost/iousbgetendpointintervalencodedmicroframes(_:_:))
- [func IOUSBGetEndpointIntervalMicroframes(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt32](/documentation/iousbhost/iousbgetendpointintervalmicroframes(_:_:))
- [func IOUSBGetEndpointIntervalFrames(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt32](/documentation/iousbhost/iousbgetendpointintervalframes(_:_:))
- [func IOUSBGetEndpointMaxStreamsEncoded(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!, UnsafePointer<IOUSBSuperSpeedEndpointCompanionDescriptor>!) -> UInt32](/documentation/iousbhost/iousbgetendpointmaxstreamsencoded(_:_:_:))
- [func IOUSBGetEndpointMaxStreams(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!, UnsafePointer<IOUSBSuperSpeedEndpointCompanionDescriptor>!) -> UInt32](/documentation/iousbhost/iousbgetendpointmaxstreams(_:_:_:))

### Creating I/O Buffers

- [func ioData(withCapacity: Int) throws -> NSMutableData](/documentation/iousbhost/iousbhostobject/iodata(withcapacity:))

### Sending Device Requests

- [func IOUSBHostDeviceRequestType(tIOUSBDeviceRequestDirectionValue, tIOUSBDeviceRequestTypeValue, tIOUSBDeviceRequestRecipientValue) -> UInt8](/documentation/iousbhost/iousbhostdevicerequesttype(_:_:_:))
- [let IOUSBHostDefaultControlCompletionTimeout: TimeInterval](/documentation/iousbhost/iousbhostdefaultcontrolcompletiontimeout)

### Enqueueing Device Requests

- [IOUSBHostCompletionHandler](/documentation/iousbhost/iousbhostcompletionhandler)

### Aborting Device Requests

- [IOUSBHostAbortOption](/documentation/iousbhost/iousbhostabortoption)

#### Options

- [case synchronous](/documentation/iousbhost/iousbhostabortoption/synchronous)
- [case asynchronous](/documentation/iousbhost/iousbhostabortoption/asynchronous)

#### Initializers

- [init?(rawValue: UInt)](/documentation/iousbhost/iousbhostabortoption/init(rawvalue:))

### Getting Host Information

- [var deviceAddress: Int](/documentation/iousbhost/iousbhostobject/deviceaddress)

### Instance Properties

- [var capabilityDescriptors: UnsafePointer<IOUSBBOSDescriptor>?](/documentation/iousbhost/iousbhostobject/capabilitydescriptors)
- [var deviceDescriptor: UnsafePointer<IOUSBDeviceDescriptor>?](/documentation/iousbhost/iousbhostobject/devicedescriptor)

### Instance Methods

- [func configurationDescriptor(with: Int) throws -> UnsafePointer<IOUSBConfigurationDescriptor>](/documentation/iousbhost/iousbhostobject/configurationdescriptor(with:))
- [func configurationDescriptor(withConfigurationValue: Int) throws -> UnsafePointer<IOUSBConfigurationDescriptor>](/documentation/iousbhost/iousbhostobject/configurationdescriptor(withconfigurationvalue:))
- [func destroy(options: IOUSBHostObjectDestroyOptions)](/documentation/iousbhost/iousbhostobject/destroy(options:))

### Related Documentation

- [IOUSBHostDevice](/documentation/iousbhost/iousbhostdevice)

#### Retrieving Device Descriptors

- [var configurationDescriptor: UnsafePointer<IOUSBConfigurationDescriptor>?](/documentation/iousbhost/iousbhostdevice/configurationdescriptor)

#### Resetting the Device

- [func reset() throws](/documentation/iousbhost/iousbhostdevice/reset())
- [IOUSBHostInterface](/documentation/iousbhost/iousbhostinterface)

#### Retrieving Function Descriptors

- [var configurationDescriptor: UnsafePointer<IOUSBConfigurationDescriptor>](/documentation/iousbhost/iousbhostinterface/configurationdescriptor)
- [var interfaceDescriptor: UnsafePointer<IOUSBInterfaceDescriptor>](/documentation/iousbhost/iousbhostinterface/interfacedescriptor)

#### Managing Pipes

- [func selectAlternateSetting(Int) throws](/documentation/iousbhost/iousbhostinterface/selectalternatesetting(_:))
- [func copyPipe(withAddress: Int) throws -> IOUSBHostPipe](/documentation/iousbhost/iousbhostinterface/copypipe(withaddress:))

#### Enabling Power Savings

- [var idleTimeout: TimeInterval](/documentation/iousbhost/iousbhostinterface/idletimeout)
- [func setIdleTimeout(TimeInterval) throws](/documentation/iousbhost/iousbhostinterface/setidletimeout(_:))
- [IOUSBHostIOSource](/documentation/iousbhost/iousbhostiosource)

### Obtaining Device Information

- [var deviceAddress: Int](/documentation/iousbhost/iousbhostiosource/deviceaddress)
- [var endpointAddress: Int](/documentation/iousbhost/iousbhostiosource/endpointaddress)
- [var hostInterface: IOUSBHostInterface](/documentation/iousbhost/iousbhostiosource/hostinterface)

### Related Documentation

- [IOUSBHostPipe](/documentation/iousbhost/iousbhostpipe)

#### Sending Bulk and Interrupt I/O

- [IOUSBHostCompletionHandler](/documentation/iousbhost/iousbhostcompletionhandler)
- [let IOUSBHostDefaultControlCompletionTimeout: TimeInterval](/documentation/iousbhost/iousbhostdefaultcontrolcompletiontimeout)
- [func enqueueIORequest(with: NSMutableData?, completionTimeout: TimeInterval, completionHandler: ((IOReturn, Int) -> Void)?) throws](/documentation/iousbhost/iousbhostpipe/enqueueiorequest(with:completiontimeout:completionhandler:))
- [func clearStall() throws](/documentation/iousbhost/iousbhostpipe/clearstall())

#### Sending Isochronous I/O

- [IOUSBHostIsochronousCompletionHandler](/documentation/iousbhost/iousbhostisochronouscompletionhandler)
- [IOUSBHostTime](/documentation/iousbhost/iousbhosttime)
- [IOUSBHostIsochronousFrame](/documentation/iousbhost/iousbhostisochronousframe)

##### Frame Structure

- [var status: IOReturn](/documentation/iousbhost/iousbhostisochronousframe/status)
- [var requestCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/requestcount)
- [var completeCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/completecount)
- [var timeStamp: IOUSBHostTime](/documentation/iousbhost/iousbhostisochronousframe/timestamp)

##### Initializing the Structure

- [init()](/documentation/iousbhost/iousbhostisochronousframe/init())

##### Initializers

- [init(status: IOReturn, requestCount: UInt32, completeCount: UInt32, reserved: UInt32, timeStamp: IOUSBHostTime)](/documentation/iousbhost/iousbhostisochronousframe/init(status:requestcount:completecount:reserved:timestamp:))

##### Instance Properties

- [var reserved: UInt32](/documentation/iousbhost/iousbhostisochronousframe/reserved)
- [var completeCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/completecount)
- [var requestCount: UInt32](/documentation/iousbhost/iousbhostisochronousframe/requestcount)
- [var reserved: UInt32](/documentation/iousbhost/iousbhostisochronousframe/reserved)
- [var status: IOReturn](/documentation/iousbhost/iousbhostisochronousframe/status)
- [var timeStamp: IOUSBHostTime](/documentation/iousbhost/iousbhostisochronousframe/timestamp)
- [func enqueueIORequest(with: NSMutableData, frameList: UnsafeMutablePointer<IOUSBHostIsochronousFrame>, frameListCount: Int, firstFrameNumber: UInt64, completionHandler: ((IOReturn, UnsafeMutablePointer<IOUSBHostIsochronousFrame>) -> Void)?) throws](/documentation/iousbhost/iousbhostpipe/enqueueiorequest(with:framelist:framelistcount:firstframenumber:completionhandler:))
- [func sendIORequest(with: NSMutableData, frameList: UnsafeMutablePointer<IOUSBHostIsochronousFrame>, frameListCount: Int, firstFrameNumber: UInt64) throws](/documentation/iousbhost/iousbhostpipe/sendiorequest(with:framelist:framelistcount:firstframenumber:))

#### Sending Control Requests

- [func IOUSBHostDeviceRequestType(tIOUSBDeviceRequestDirectionValue, tIOUSBDeviceRequestTypeValue, tIOUSBDeviceRequestRecipientValue) -> UInt8](/documentation/iousbhost/iousbhostdevicerequesttype(_:_:_:))
- [let IOUSBHostDefaultControlCompletionTimeout: TimeInterval](/documentation/iousbhost/iousbhostdefaultcontrolcompletiontimeout)
- [IOUSBHostCompletionHandler](/documentation/iousbhost/iousbhostcompletionhandler)

#### Managing Periodic Bandwidth

- [IOUSBHostIOSourceDescriptors](/documentation/iousbhost/iousbhostiosourcedescriptors)

##### Descriptors

- [var bcdUSB: UInt16](/documentation/iousbhost/iousbhostiosourcedescriptors/bcdusb)
- [var descriptor: IOUSBEndpointDescriptor](/documentation/iousbhost/iousbhostiosourcedescriptors/descriptor)
- [var ssCompanionDescriptor: IOUSBSuperSpeedEndpointCompanionDescriptor](/documentation/iousbhost/iousbhostiosourcedescriptors/sscompaniondescriptor)
- [var sspCompanionDescriptor: IOUSBSuperSpeedPlusIsochronousEndpointCompanionDescriptor](/documentation/iousbhost/iousbhostiosourcedescriptors/sspcompaniondescriptor)

##### Initializing the Structure

- [init()](/documentation/iousbhost/iousbhostiosourcedescriptors/init())
- [init(bcdUSB: UInt16, descriptor: IOUSBEndpointDescriptor, ssCompanionDescriptor: IOUSBSuperSpeedEndpointCompanionDescriptor, sspCompanionDescriptor: IOUSBSuperSpeedPlusIsochronousEndpointCompanionDescriptor)](/documentation/iousbhost/iousbhostiosourcedescriptors/init(bcdusb:descriptor:sscompaniondescriptor:sspcompaniondescriptor:))
- [func adjust(with: UnsafePointer<IOUSBHostIOSourceDescriptors>) throws](/documentation/iousbhost/iousbhostpipe/adjust(with:))
- [var descriptors: UnsafePointer<IOUSBHostIOSourceDescriptors>](/documentation/iousbhost/iousbhostpipe/descriptors)
- [var originalDescriptors: UnsafePointer<IOUSBHostIOSourceDescriptors>](/documentation/iousbhost/iousbhostpipe/originaldescriptors)

#### Enabling Power Savings

- [func setIdleTimeout(TimeInterval) throws](/documentation/iousbhost/iousbhostpipe/setidletimeout(_:))
- [var idleTimeout: TimeInterval](/documentation/iousbhost/iousbhostpipe/idletimeout)

#### Managing Streams

- [func enableStreams() throws](/documentation/iousbhost/iousbhostpipe/enablestreams())
- [func copyStream(withStreamID: Int) throws -> IOUSBHostStream](/documentation/iousbhost/iousbhostpipe/copystream(withstreamid:))
- [func disableStreams() throws](/documentation/iousbhost/iousbhostpipe/disablestreams())

#### Instance Methods

- [func enqueueIORequest(with: NSMutableData, transactionList: UnsafeMutablePointer<IOUSBHostIsochronousTransaction>, transactionListCount: Int, firstFrameNumber: UInt64, options: IOUSBHostIsochronousTransferOptions, completionHandler: ((IOReturn, UnsafeMutablePointer<IOUSBHostIsochronousTransaction>) -> Void)?) throws](/documentation/iousbhost/iousbhostpipe/enqueueiorequest(with:transactionlist:transactionlistcount:firstframenumber:options:completionhandler:))
- [func sendIORequest(with: NSMutableData, transactionList: UnsafeMutablePointer<IOUSBHostIsochronousTransaction>, transactionListCount: Int, firstFrameNumber: UInt64, options: IOUSBHostIsochronousTransferOptions) throws](/documentation/iousbhost/iousbhostpipe/sendiorequest(with:transactionlist:transactionlistcount:firstframenumber:options:))
- [IOUSBHostStream](/documentation/iousbhost/iousbhoststream)

#### Sending I/O

- [IOUSBHostCompletionHandler](/documentation/iousbhost/iousbhostcompletionhandler)
- [func enqueueIORequest(with: NSMutableData?, completionHandler: ((IOReturn, Int) -> Void)?) throws](/documentation/iousbhost/iousbhoststream/enqueueiorequest(with:completionhandler:))
- [func abort(with: IOUSBHostAbortOption) throws](/documentation/iousbhost/iousbhoststream/abort(with:))

##### Options

- [IOUSBHostAbortOption](/documentation/iousbhost/iousbhostabortoption)

###### Options

- [case synchronous](/documentation/iousbhost/iousbhostabortoption/synchronous)
- [case asynchronous](/documentation/iousbhost/iousbhostabortoption/asynchronous)

###### Initializers

- [init?(rawValue: UInt)](/documentation/iousbhost/iousbhostabortoption/init(rawvalue:))
- [func abort() throws](/documentation/iousbhost/iousbhoststream/abort())

#### Getting the Pipe Object

- [var hostPipe: IOUSBHostPipe](/documentation/iousbhost/iousbhoststream/hostpipe)

#### Getting the Stream ID

- [var streamID: Int](/documentation/iousbhost/iousbhoststream/streamid)

## IOServicePlane Properties

- [IOUSBHostInterfacePropertyKey](/documentation/iousbhost/iousbhostinterfacepropertykey)

### Properties

- [static let alternateSetting: IOUSBHostInterfacePropertyKey](/documentation/iousbhost/iousbhostinterfacepropertykey/alternatesetting)

### Initializing the Structure

- [init(rawValue: String)](/documentation/iousbhost/iousbhostinterfacepropertykey/init(rawvalue:))
- [IOUSBHostDevicePropertyKey](/documentation/iousbhost/iousbhostdevicepropertykey)

### Properties

- [static let currentConfiguration: IOUSBHostDevicePropertyKey](/documentation/iousbhost/iousbhostdevicepropertykey/currentconfiguration)
- [static let containerID: IOUSBHostDevicePropertyKey](/documentation/iousbhost/iousbhostdevicepropertykey/containerid)
- [static let serialNumberString: IOUSBHostDevicePropertyKey](/documentation/iousbhost/iousbhostdevicepropertykey/serialnumberstring)
- [static let vendorString: IOUSBHostDevicePropertyKey](/documentation/iousbhost/iousbhostdevicepropertykey/vendorstring)
- [IOUSBHostPropertyKey](/documentation/iousbhost/iousbhostpropertykey)

#### Properties

- [let IOUSBHostPropertyKeyLocationID: String](/documentation/iousbhost/iousbhostpropertykeylocationid)

### Initializing the Properties

- [init(rawValue: String)](/documentation/iousbhost/iousbhostdevicepropertykey/init(rawvalue:))
- [IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey)

### Device Properties

- [static let vendorID: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/vendorid)
- [static let productID: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/productid)
- [static let deviceReleaseNumber: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/devicereleasenumber)
- [static let configurationValue: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/configurationvalue)
- [static let speed: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/speed)
- [static let productIDArray: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/productidarray)
- [static let productIDMask: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/productidmask)

### Interface Properties

- [static let interfaceNumber: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/interfacenumber)
- [static let interfaceClass: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/interfaceclass)
- [static let interfaceSubClass: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/interfacesubclass)
- [static let interfaceProtocol: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/interfaceprotocol)

### Protocol and Class Properties

- [static let deviceProtocol: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/deviceprotocol)
- [static let deviceClass: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/deviceclass)
- [static let deviceSubClass: IOUSBHostMatchingPropertyKey](/documentation/iousbhost/iousbhostmatchingpropertykey/devicesubclass)

### Initializing the Structure

- [init(rawValue: String)](/documentation/iousbhost/iousbhostmatchingpropertykey/init(rawvalue:))
- [IOUSBHostPropertyKey](/documentation/iousbhost/iousbhostpropertykey)

### Properties

- [let IOUSBHostPropertyKeyLocationID: String](/documentation/iousbhost/iousbhostpropertykeylocationid)

## Error Domain

- [let IOUSBHostErrorDomain: String](/documentation/iousbhost/iousbhosterrordomain)

## Classes

- [IOUSBHostCIControllerStateMachine](/documentation/iousbhost/iousbhostcicontrollerstatemachine)

### Instance Properties

- [var controllerInterface: IOUSBHostControllerInterface](/documentation/iousbhost/iousbhostcicontrollerstatemachine/controllerinterface)
- [var controllerState: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstatemachine/controllerstate)

### Instance Methods

- [func enqueueUpdatedFrame(UInt64, timestamp: UInt64) throws](/documentation/iousbhost/iousbhostcicontrollerstatemachine/enqueueupdatedframe(_:timestamp:))
- [func inspectCommand(UnsafePointer<IOUSBHostCIMessage>) throws](/documentation/iousbhost/iousbhostcicontrollerstatemachine/inspectcommand(_:))
- [func respond(toCommand: UnsafePointer<IOUSBHostCIMessage>, status: IOUSBHostCIMessageStatus) throws](/documentation/iousbhost/iousbhostcicontrollerstatemachine/respond(tocommand:status:))
- [func respond(toCommand: UnsafePointer<IOUSBHostCIMessage>, status: IOUSBHostCIMessageStatus, frame: UInt64, timestamp: UInt64) throws](/documentation/iousbhost/iousbhostcicontrollerstatemachine/respond(tocommand:status:frame:timestamp:))
- [IOUSBHostCIDeviceStateMachine](/documentation/iousbhost/iousbhostcidevicestatemachine)

### Instance Properties

- [var completeRoute: Int](/documentation/iousbhost/iousbhostcidevicestatemachine/completeroute)
- [var controllerInterface: IOUSBHostControllerInterface](/documentation/iousbhost/iousbhostcidevicestatemachine/controllerinterface)
- [var deviceAddress: Int](/documentation/iousbhost/iousbhostcidevicestatemachine/deviceaddress)
- [var deviceState: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestatemachine/devicestate)

### Instance Methods

- [func inspectCommand(UnsafePointer<IOUSBHostCIMessage>) throws](/documentation/iousbhost/iousbhostcidevicestatemachine/inspectcommand(_:))
- [func respond(toCommand: UnsafePointer<IOUSBHostCIMessage>, status: IOUSBHostCIMessageStatus) throws](/documentation/iousbhost/iousbhostcidevicestatemachine/respond(tocommand:status:))
- [func respond(toCommand: UnsafePointer<IOUSBHostCIMessage>, status: IOUSBHostCIMessageStatus, deviceAddress: Int) throws](/documentation/iousbhost/iousbhostcidevicestatemachine/respond(tocommand:status:deviceaddress:))
- [IOUSBHostCIEndpointStateMachine](/documentation/iousbhost/iousbhostciendpointstatemachine)

### Instance Properties

- [var controllerInterface: IOUSBHostControllerInterface](/documentation/iousbhost/iousbhostciendpointstatemachine/controllerinterface)
- [var currentTransferMessage: UnsafePointer<IOUSBHostCIMessage>](/documentation/iousbhost/iousbhostciendpointstatemachine/currenttransfermessage)
- [var deviceAddress: Int](/documentation/iousbhost/iousbhostciendpointstatemachine/deviceaddress)
- [var endpointAddress: Int](/documentation/iousbhost/iousbhostciendpointstatemachine/endpointaddress)
- [var endpointState: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatemachine/endpointstate)

### Instance Methods

- [func enqueueTransferCompletion(for: UnsafePointer<IOUSBHostCIMessage>, status: IOUSBHostCIMessageStatus, transferLength: Int) throws](/documentation/iousbhost/iousbhostciendpointstatemachine/enqueuetransfercompletion(for:status:transferlength:))
- [func inspectCommand(UnsafePointer<IOUSBHostCIMessage>) throws](/documentation/iousbhost/iousbhostciendpointstatemachine/inspectcommand(_:))
- [func processDoorbell(IOUSBHostCIDoorbell) throws](/documentation/iousbhost/iousbhostciendpointstatemachine/processdoorbell(_:))
- [func respond(toCommand: UnsafePointer<IOUSBHostCIMessage>, status: IOUSBHostCIMessageStatus) throws](/documentation/iousbhost/iousbhostciendpointstatemachine/respond(tocommand:status:))
- [IOUSBHostCIPortStateMachine](/documentation/iousbhost/iousbhostciportstatemachine)

### Instance Properties

- [var connected: Bool](/documentation/iousbhost/iousbhostciportstatemachine/connected)
- [var controllerInterface: IOUSBHostControllerInterface](/documentation/iousbhost/iousbhostciportstatemachine/controllerinterface)
- [var linkState: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostciportstatemachine/linkstate)
- [var overcurrent: Bool](/documentation/iousbhost/iousbhostciportstatemachine/overcurrent)
- [var portNumber: Int](/documentation/iousbhost/iousbhostciportstatemachine/portnumber)
- [var portState: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstatemachine/portstate)
- [var portStatus: IOUSBHostCIPortStatus](/documentation/iousbhost/iousbhostciportstatemachine/portstatus)
- [var powered: Bool](/documentation/iousbhost/iousbhostciportstatemachine/powered)
- [var speed: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostciportstatemachine/speed)

### Instance Methods

- [func inspectCommand(UnsafePointer<IOUSBHostCIMessage>) throws](/documentation/iousbhost/iousbhostciportstatemachine/inspectcommand(_:))
- [func respond(toCommand: UnsafePointer<IOUSBHostCIMessage>, status: IOUSBHostCIMessageStatus) throws](/documentation/iousbhost/iousbhostciportstatemachine/respond(tocommand:status:))
- [func updateLinkState(IOUSBHostCILinkState, speed: IOUSBHostCIDeviceSpeed, inhibitLinkStateChange: Bool) throws](/documentation/iousbhost/iousbhostciportstatemachine/updatelinkstate(_:speed:inhibitlinkstatechange:))
- [IOUSBHostControllerInterface](/documentation/iousbhost/iousbhostcontrollerinterface)

### Instance Properties

- [var capabilities: UnsafePointer<IOUSBHostCIMessage>](/documentation/iousbhost/iousbhostcontrollerinterface/capabilities)
- [var controllerStateMachine: IOUSBHostCIControllerStateMachine](/documentation/iousbhost/iousbhostcontrollerinterface/controllerstatemachine)
- [var interruptRateHz: Int](/documentation/iousbhost/iousbhostcontrollerinterface/interruptratehz)
- [var queue: dispatch_queue_t](/documentation/iousbhost/iousbhostcontrollerinterface/queue)
- [var uuid: UUID](/documentation/iousbhost/iousbhostcontrollerinterface/uuid)

### Instance Methods

- [func capabilities(forPort: Int) -> UnsafePointer<IOUSBHostCIMessage>](/documentation/iousbhost/iousbhostcontrollerinterface/capabilities(forport:))
- [func description(for: UnsafePointer<IOUSBHostCIMessage>) -> String](/documentation/iousbhost/iousbhostcontrollerinterface/description(for:))
- [func destroy()](/documentation/iousbhost/iousbhostcontrollerinterface/destroy())
- [func enqueueInterrupt(UnsafePointer<IOUSBHostCIMessage>) throws](/documentation/iousbhost/iousbhostcontrollerinterface/enqueueinterrupt(_:))
- [func enqueueInterrupt(UnsafePointer<IOUSBHostCIMessage>, expedite: Bool) throws](/documentation/iousbhost/iousbhostcontrollerinterface/enqueueinterrupt(_:expedite:))
- [func enqueueInterrupts(UnsafePointer<IOUSBHostCIMessage>, count: Int) throws](/documentation/iousbhost/iousbhostcontrollerinterface/enqueueinterrupts(_:count:))
- [func enqueueInterrupts(UnsafePointer<IOUSBHostCIMessage>, count: Int, expedite: Bool) throws](/documentation/iousbhost/iousbhostcontrollerinterface/enqueueinterrupts(_:count:expedite:))
- [func getPortStateMachine(forCommand: UnsafePointer<IOUSBHostCIMessage>, error: NSErrorPointer) -> IOUSBHostCIPortStateMachine](/documentation/iousbhost/iousbhostcontrollerinterface/getportstatemachine(forcommand:error:))
- [func getPortStateMachine(forPort: Int, error: NSErrorPointer) -> IOUSBHostCIPortStateMachine](/documentation/iousbhost/iousbhostcontrollerinterface/getportstatemachine(forport:error:))

## Reference

- [IOUSBHost Structures](/documentation/iousbhost/iousbhost-structures)

### Structures

- [IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcicontrollerstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcicontrollerstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIControllerStateActive: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstateactive)
- [var IOUSBHostCIControllerStateOff: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstateoff)
- [var IOUSBHostCIControllerStatePaused: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstatepaused)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcicontrollerstate/rawvalue)
- [IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeed)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcidevicespeed/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcidevicespeed/init(rawvalue:))

#### Constants

- [var IOUSBHostCIDeviceSpeedFull: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedfull)
- [var IOUSBHostCIDeviceSpeedHigh: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedhigh)
- [var IOUSBHostCIDeviceSpeedLow: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedlow)
- [var IOUSBHostCIDeviceSpeedNone: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeednone)
- [var IOUSBHostCIDeviceSpeedSuper: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuper)
- [var IOUSBHostCIDeviceSpeedSuperPlus: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuperplus)
- [var IOUSBHostCIDeviceSpeedSuperPlusBy2: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuperplusby2)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcidevicespeed/rawvalue)
- [IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcidevicestate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcidevicestate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIDeviceStateActive: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestateactive)
- [var IOUSBHostCIDeviceStateDestroyed: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestatedestroyed)
- [var IOUSBHostCIDeviceStatePaused: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestatepaused)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcidevicestate/rawvalue)
- [IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciendpointstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciendpointstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIEndpointStateActive: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstateactive)
- [var IOUSBHostCIEndpointStateDestroyed: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatedestroyed)
- [var IOUSBHostCIEndpointStateHalted: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatehalted)
- [var IOUSBHostCIEndpointStatePaused: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatepaused)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciendpointstate/rawvalue)
- [IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontype)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciexceptiontype/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciexceptiontype/init(rawvalue:))

#### Constants

- [var IOUSBHostCIExceptionTypeCapabilitiesInvalid: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecapabilitiesinvalid)
- [var IOUSBHostCIExceptionTypeCommandFailure: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandfailure)
- [var IOUSBHostCIExceptionTypeCommandReadCollision: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandreadcollision)
- [var IOUSBHostCIExceptionTypeCommandTimeout: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandtimeout)
- [var IOUSBHostCIExceptionTypeCommandWriteFailed: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandwritefailed)
- [var IOUSBHostCIExceptionTypeDoorbellOverflow: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypedoorbelloverflow)
- [var IOUSBHostCIExceptionTypeDoorbellReadCollision: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypedoorbellreadcollision)
- [var IOUSBHostCIExceptionTypeFrameUpdateError: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeframeupdateerror)
- [var IOUSBHostCIExceptionTypeInterruptInvalid: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeinterruptinvalid)
- [var IOUSBHostCIExceptionTypeInterruptOverflow: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeinterruptoverflow)
- [var IOUSBHostCIExceptionTypeProtocolError: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeprotocolerror)
- [var IOUSBHostCIExceptionTypeTerminated: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeterminated)
- [var IOUSBHostCIExceptionTypeUnknown: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeunknown)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciexceptiontype/rawvalue)
- [IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcilinkstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcilinkstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCILinkStateCompliance: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatecompliance)
- [var IOUSBHostCILinkStateDisabled: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatedisabled)
- [var IOUSBHostCILinkStateInactive: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateinactive)
- [var IOUSBHostCILinkStatePolling: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatepolling)
- [var IOUSBHostCILinkStateRecovery: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstaterecovery)
- [var IOUSBHostCILinkStateReset: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatereset)
- [var IOUSBHostCILinkStateResume: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateresume)
- [var IOUSBHostCILinkStateRxDetect: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstaterxdetect)
- [var IOUSBHostCILinkStateTest: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatetest)
- [var IOUSBHostCILinkStateU0: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu0)
- [var IOUSBHostCILinkStateU1: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu1)
- [var IOUSBHostCILinkStateU2: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu2)
- [var IOUSBHostCILinkStateU3: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu3)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcilinkstate/rawvalue)
- [IOUSBHostCIMessage](/documentation/iousbhost/iousbhostcimessage)

#### Initializers

- [init()](/documentation/iousbhost/iousbhostcimessage/init())
- [init(control: UInt32, data0: UInt32, data1: UInt64)](/documentation/iousbhost/iousbhostcimessage/init(control:data0:data1:))

#### Instance Properties

- [var control: UInt32](/documentation/iousbhost/iousbhostcimessage/control)
- [var data0: UInt32](/documentation/iousbhost/iousbhostcimessage/data0)
- [var data1: UInt64](/documentation/iousbhost/iousbhostcimessage/data1)
- [IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatus)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcimessagestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcimessagestatus/init(rawvalue:))

#### Constants

- [var IOUSBHostCIMessageStatusBadArgument: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusbadargument)
- [var IOUSBHostCIMessageStatusEndpointStopped: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusendpointstopped)
- [var IOUSBHostCIMessageStatusError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatuserror)
- [var IOUSBHostCIMessageStatusMissedServiceError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusmissedserviceerror)
- [var IOUSBHostCIMessageStatusNoResources: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusnoresources)
- [var IOUSBHostCIMessageStatusNotPermitted: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusnotpermitted)
- [var IOUSBHostCIMessageStatusOffline: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusoffline)
- [var IOUSBHostCIMessageStatusOverrunError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusoverrunerror)
- [var IOUSBHostCIMessageStatusProtocolError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusprotocolerror)
- [var IOUSBHostCIMessageStatusReserved: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusreserved)
- [var IOUSBHostCIMessageStatusStallError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusstallerror)
- [var IOUSBHostCIMessageStatusSuccess: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatussuccess)
- [var IOUSBHostCIMessageStatusTimeout: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatustimeout)
- [var IOUSBHostCIMessageStatusTransactionError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatustransactionerror)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcimessagestatus/rawvalue)
- [IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetype)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcimessagetype/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcimessagetype/init(rawvalue:))

#### Constants

- [var IOUSBHostCIMessageTypeCommandMax: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecommandmax)
- [var IOUSBHostCIMessageTypeCommandMin: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecommandmin)
- [var IOUSBHostCIMessageTypeControllerCapabilities: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollercapabilities)
- [var IOUSBHostCIMessageTypeControllerFrameNumber: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerframenumber)
- [var IOUSBHostCIMessageTypeControllerPause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpause)
- [var IOUSBHostCIMessageTypeControllerPowerOff: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpoweroff)
- [var IOUSBHostCIMessageTypeControllerPowerOn: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpoweron)
- [var IOUSBHostCIMessageTypeControllerStart: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerstart)
- [var IOUSBHostCIMessageTypeDeviceCreate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicecreate)
- [var IOUSBHostCIMessageTypeDeviceDestroy: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicedestroy)
- [var IOUSBHostCIMessageTypeDevicePause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicepause)
- [var IOUSBHostCIMessageTypeDeviceStart: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicestart)
- [var IOUSBHostCIMessageTypeDeviceUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedeviceupdate)
- [var IOUSBHostCIMessageTypeEndpointCreate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointcreate)
- [var IOUSBHostCIMessageTypeEndpointDestroy: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointdestroy)
- [var IOUSBHostCIMessageTypeEndpointPause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointpause)
- [var IOUSBHostCIMessageTypeEndpointReset: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointreset)
- [var IOUSBHostCIMessageTypeEndpointSetNextTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointsetnexttransfer)
- [var IOUSBHostCIMessageTypeEndpointUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointupdate)
- [var IOUSBHostCIMessageTypeEndpoint_reserved_: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpoint_reserved_)
- [var IOUSBHostCIMessageTypeFrameNumberUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeframenumberupdate)
- [var IOUSBHostCIMessageTypeFrameTimestampUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeframetimestampupdate)
- [var IOUSBHostCIMessageTypeIsochronousTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeisochronoustransfer)
- [var IOUSBHostCIMessageTypeLink: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypelink)
- [var IOUSBHostCIMessageTypeNormalTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypenormaltransfer)
- [var IOUSBHostCIMessageTypePortCapabilities: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportcapabilities)
- [var IOUSBHostCIMessageTypePortDisable: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportdisable)
- [var IOUSBHostCIMessageTypePortEvent: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportevent)
- [var IOUSBHostCIMessageTypePortPowerOff: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportpoweroff)
- [var IOUSBHostCIMessageTypePortPowerOn: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportpoweron)
- [var IOUSBHostCIMessageTypePortReset: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportreset)
- [var IOUSBHostCIMessageTypePortResume: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportresume)
- [var IOUSBHostCIMessageTypePortStatus: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportstatus)
- [var IOUSBHostCIMessageTypePortSuspend: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportsuspend)
- [var IOUSBHostCIMessageTypeSetupTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypesetuptransfer)
- [var IOUSBHostCIMessageTypeStatusTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypestatustransfer)
- [var IOUSBHostCIMessageTypeTransferComplete: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypetransfercomplete)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcimessagetype/rawvalue)
- [IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciportstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciportstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIPortStateActive: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstateactive)
- [var IOUSBHostCIPortStateOff: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstateoff)
- [var IOUSBHostCIPortStatePowered: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstatepowered)
- [var IOUSBHostCIPortStateSuspended: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstatesuspended)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciportstate/rawvalue)
- [IOUSBHostCIUserClientVersion](/documentation/iousbhost/iousbhostciuserclientversion)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciuserclientversion/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciuserclientversion/init(rawvalue:))

#### Constants

- [var IOUSBHostCIUserClientVersion100: IOUSBHostCIUserClientVersion](/documentation/iousbhost/iousbhostciuserclientversion100)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciuserclientversion/rawvalue)
- [IOUSBHostIsochronousTransaction](/documentation/iousbhost/iousbhostisochronoustransaction)

#### Initializers

- [init()](/documentation/iousbhost/iousbhostisochronoustransaction/init())
- [init(status: IOReturn, requestCount: UInt32, offset: UInt32, completeCount: UInt32, timeStamp: IOUSBHostTime, options: IOUSBHostIsochronousTransactionOptions)](/documentation/iousbhost/iousbhostisochronoustransaction/init(status:requestcount:offset:completecount:timestamp:options:))

#### Instance Properties

- [var completeCount: UInt32](/documentation/iousbhost/iousbhostisochronoustransaction/completecount)
- [var offset: UInt32](/documentation/iousbhost/iousbhostisochronoustransaction/offset)
- [var options: IOUSBHostIsochronousTransactionOptions](/documentation/iousbhost/iousbhostisochronoustransaction/options)
- [var requestCount: UInt32](/documentation/iousbhost/iousbhostisochronoustransaction/requestcount)
- [var status: IOReturn](/documentation/iousbhost/iousbhostisochronoustransaction/status)
- [var timeStamp: IOUSBHostTime](/documentation/iousbhost/iousbhostisochronoustransaction/timestamp)
- [IOUSBHostIsochronousTransactionOptions](/documentation/iousbhost/iousbhostisochronoustransactionoptions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostisochronoustransactionoptions/init(rawvalue:))

#### Type Properties

- [static var wrap: IOUSBHostIsochronousTransactionOptions](/documentation/iousbhost/iousbhostisochronoustransactionoptions/wrap)
- [IOUSBHostIsochronousTransferOptions](/documentation/iousbhost/iousbhostisochronoustransferoptions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostisochronoustransferoptions/init(rawvalue:))
- [IOUSBHostObjectDestroyOptions](/documentation/iousbhost/iousbhostobjectdestroyoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/iousbhost/iousbhostobjectdestroyoptions/init(rawvalue:))

#### Type Properties

- [static var deviceSurrender: IOUSBHostObjectDestroyOptions](/documentation/iousbhost/iousbhostobjectdestroyoptions/devicesurrender)
- [IOUSBHost Enumerations](/documentation/iousbhost/iousbhost-enumerations)

### Enumerations

- [Anonymous](/documentation/iousbhost/3612464-anonymous)

#### Constants

- [var IOUSBHostCICapabilitiesMessageControlPortCount: Int](/documentation/iousbhost/iousbhostcicapabilitiesmessagecontrolportcount)
- [var IOUSBHostCICapabilitiesMessageControlPortCountPhase: Int](/documentation/iousbhost/iousbhostcicapabilitiesmessagecontrolportcountphase)
- [var IOUSBHostCICapabilitiesMessageData0CommandTimeoutThreshold: Int](/documentation/iousbhost/iousbhostcicapabilitiesmessagedata0commandtimeoutthreshold)
- [var IOUSBHostCICapabilitiesMessageData0CommandTimeoutThresholdPhase: Int](/documentation/iousbhost/iousbhostcicapabilitiesmessagedata0commandtimeoutthresholdphase)
- [var IOUSBHostCICapabilitiesMessageData0ConnectionLatency: Int](/documentation/iousbhost/iousbhostcicapabilitiesmessagedata0connectionlatency)
- [var IOUSBHostCICapabilitiesMessageData0ConnectionLatencyPhase: Int](/documentation/iousbhost/iousbhostcicapabilitiesmessagedata0connectionlatencyphase)
- [Anonymous](/documentation/iousbhost/3612465-anonymous)

#### Constants

- [var IOUSBHostCICommandMessageControlStatus: UInt32](/documentation/iousbhost/iousbhostcicommandmessagecontrolstatus)
- [var IOUSBHostCICommandMessageControlStatusPhase: UInt32](/documentation/iousbhost/iousbhostcicommandmessagecontrolstatusphase)
- [var IOUSBHostCICommandMessageData0DeviceAddress: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0deviceaddress)
- [var IOUSBHostCICommandMessageData0DeviceAddressPhase: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0deviceaddressphase)
- [var IOUSBHostCICommandMessageData0EndpointAddress: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0endpointaddress)
- [var IOUSBHostCICommandMessageData0EndpointAddressPhase: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0endpointaddressphase)
- [var IOUSBHostCICommandMessageData0RootPort: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0rootport)
- [var IOUSBHostCICommandMessageData0RootPortPhase: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0rootportphase)
- [var IOUSBHostCICommandMessageData0StreamID: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0streamid)
- [var IOUSBHostCICommandMessageData0StreamIDPhase: UInt32](/documentation/iousbhost/iousbhostcicommandmessagedata0streamidphase)
- [Anonymous](/documentation/iousbhost/3612466-anonymous)

#### Constants

- [var IOUSBHostCIDeviceCreateCommandData0RootPort: Int](/documentation/iousbhost/iousbhostcidevicecreatecommanddata0rootport)
- [var IOUSBHostCIDeviceCreateCommandData0RootPortPhase: Int](/documentation/iousbhost/iousbhostcidevicecreatecommanddata0rootportphase)
- [var IOUSBHostCIDeviceCreateCommandData0Route: Int](/documentation/iousbhost/iousbhostcidevicecreatecommanddata0route)
- [var IOUSBHostCIDeviceCreateCommandData0RoutePhase: Int](/documentation/iousbhost/iousbhostcidevicecreatecommanddata0routephase)
- [var IOUSBHostCIDeviceCreateCommandData1DeviceAddress: Int](/documentation/iousbhost/iousbhostcidevicecreatecommanddata1deviceaddress)
- [var IOUSBHostCIDeviceCreateCommandData1DeviceAddressPhase: Int](/documentation/iousbhost/iousbhostcidevicecreatecommanddata1deviceaddressphase)
- [Anonymous](/documentation/iousbhost/3612467-anonymous)

#### Constants

- [var IOUSBHostCIDoorbellDeviceAddress: UInt32](/documentation/iousbhost/iousbhostcidoorbelldeviceaddress)
- [var IOUSBHostCIDoorbellDeviceAddressPhase: UInt32](/documentation/iousbhost/iousbhostcidoorbelldeviceaddressphase)
- [var IOUSBHostCIDoorbellEndpointAddress: UInt32](/documentation/iousbhost/iousbhostcidoorbellendpointaddress)
- [var IOUSBHostCIDoorbellEndpointAddressPhase: UInt32](/documentation/iousbhost/iousbhostcidoorbellendpointaddressphase)
- [var IOUSBHostCIDoorbellStreamID: UInt32](/documentation/iousbhost/iousbhostcidoorbellstreamid)
- [var IOUSBHostCIDoorbellStreamIDPhase: UInt32](/documentation/iousbhost/iousbhostcidoorbellstreamidphase)
- [Anonymous](/documentation/iousbhost/3612468-anonymous)

#### Constants

- [var IOUSBHostCIEndpointCreateCommandData1Descriptor: UInt](/documentation/iousbhost/iousbhostciendpointcreatecommanddata1descriptor)
- [var IOUSBHostCIEndpointCreateCommandData1DescriptorPhase: UInt](/documentation/iousbhost/iousbhostciendpointcreatecommanddata1descriptorphase)
- [Anonymous](/documentation/iousbhost/3612469-anonymous)

#### Constants

- [var IOUSBHostCIEndpointResetCommandData1ClearState: Int](/documentation/iousbhost/iousbhostciendpointresetcommanddata1clearstate)
- [Anonymous](/documentation/iousbhost/3612470-anonymous)

#### Constants

- [var IOUSBHostCIEndpointSetNextTransferCommandData1Address: UInt](/documentation/iousbhost/iousbhostciendpointsetnexttransfercommanddata1address)
- [var IOUSBHostCIEndpointSetNextTransferCommandData1AddressPhase: UInt](/documentation/iousbhost/iousbhostciendpointsetnexttransfercommanddata1addressphase)
- [Anonymous](/documentation/iousbhost/3612471-anonymous)

#### Constants

- [var IOUSBHostCIIsochronousTransferControlASAP: Int](/documentation/iousbhost/iousbhostciisochronoustransfercontrolasap)
- [var IOUSBHostCIIsochronousTransferControlFrameNumber: Int](/documentation/iousbhost/iousbhostciisochronoustransfercontrolframenumber)
- [var IOUSBHostCIIsochronousTransferControlFrameNumberPhase: Int](/documentation/iousbhost/iousbhostciisochronoustransfercontrolframenumberphase)
- [var IOUSBHostCIIsochronousTransferData0Length: Int](/documentation/iousbhost/iousbhostciisochronoustransferdata0length)
- [var IOUSBHostCIIsochronousTransferData0LengthPhase: Int](/documentation/iousbhost/iousbhostciisochronoustransferdata0lengthphase)
- [var IOUSBHostCIIsochronousTransferData1Buffer: UInt](/documentation/iousbhost/iousbhostciisochronoustransferdata1buffer)
- [var IOUSBHostCIIsochronousTransferData1BufferPhase: UInt](/documentation/iousbhost/iousbhostciisochronoustransferdata1bufferphase)
- [Anonymous](/documentation/iousbhost/3612472-anonymous)

#### Constants

- [var IOUSBHostCIMessageControlNoResponse: Int](/documentation/iousbhost/iousbhostcimessagecontrolnoresponse)
- [var IOUSBHostCIMessageControlStatus: Int](/documentation/iousbhost/iousbhostcimessagecontrolstatus)
- [var IOUSBHostCIMessageControlStatusPhase: Int](/documentation/iousbhost/iousbhostcimessagecontrolstatusphase)
- [var IOUSBHostCIMessageControlType: Int](/documentation/iousbhost/iousbhostcimessagecontroltype)
- [var IOUSBHostCIMessageControlTypePhase: Int](/documentation/iousbhost/iousbhostcimessagecontroltypephase)
- [var IOUSBHostCIMessageControlValid: Int](/documentation/iousbhost/iousbhostcimessagecontrolvalid)
- [Anonymous](/documentation/iousbhost/3612473-anonymous)

#### Constants

- [var IOUSBHostCINormalTransferData0Length: Int](/documentation/iousbhost/iousbhostcinormaltransferdata0length)
- [var IOUSBHostCINormalTransferData0LengthPhase: Int](/documentation/iousbhost/iousbhostcinormaltransferdata0lengthphase)
- [var IOUSBHostCINormalTransferData1Buffer: UInt](/documentation/iousbhost/iousbhostcinormaltransferdata1buffer)
- [var IOUSBHostCINormalTransferData1BufferPhase: UInt](/documentation/iousbhost/iousbhostcinormaltransferdata1bufferphase)
- [Anonymous](/documentation/iousbhost/3612474-anonymous)

#### Constants

- [var IOUSBHostCIPortCapabilitiesMessageControlConnectorType: UInt32](/documentation/iousbhost/iousbhostciportcapabilitiesmessagecontrolconnectortype)
- [var IOUSBHostCIPortCapabilitiesMessageControlConnectorTypePhase: UInt32](/documentation/iousbhost/iousbhostciportcapabilitiesmessagecontrolconnectortypephase)
- [var IOUSBHostCIPortCapabilitiesMessageControlInternalConnector: UInt32](/documentation/iousbhost/iousbhostciportcapabilitiesmessagecontrolinternalconnector)
- [var IOUSBHostCIPortCapabilitiesMessageControlPortNumber: UInt32](/documentation/iousbhost/iousbhostciportcapabilitiesmessagecontrolportnumber)
- [var IOUSBHostCIPortCapabilitiesMessageControlPortNumberPhase: UInt32](/documentation/iousbhost/iousbhostciportcapabilitiesmessagecontrolportnumberphase)
- [var IOUSBHostCIPortCapabilitiesMessageData0MaxPower: UInt32](/documentation/iousbhost/iousbhostciportcapabilitiesmessagedata0maxpower)
- [var IOUSBHostCIPortCapabilitiesMessageData0MaxPowerPhase: UInt32](/documentation/iousbhost/iousbhostciportcapabilitiesmessagedata0maxpowerphase)
- [Anonymous](/documentation/iousbhost/3612475-anonymous)

#### Constants

- [var IOUSBHostCIPortEventMessageData0PortNumber: Int](/documentation/iousbhost/iousbhostciporteventmessagedata0portnumber)
- [var IOUSBHostCIPortEventMessageData0PortNumberPhase: Int](/documentation/iousbhost/iousbhostciporteventmessagedata0portnumberphase)
- [Anonymous](/documentation/iousbhost/3612476-anonymous)

#### Constants

- [var IOUSBHostCIPortStatusCommandData1ChangeMask: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1changemask)
- [var IOUSBHostCIPortStatusCommandData1ConnectChange: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1connectchange)
- [var IOUSBHostCIPortStatusCommandData1Connected: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1connected)
- [var IOUSBHostCIPortStatusCommandData1LinkState: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1linkstate)
- [var IOUSBHostCIPortStatusCommandData1LinkStateChange: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1linkstatechange)
- [var IOUSBHostCIPortStatusCommandData1LinkStatePhase: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1linkstatephase)
- [var IOUSBHostCIPortStatusCommandData1Overcurrent: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1overcurrent)
- [var IOUSBHostCIPortStatusCommandData1OvercurrentChange: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1overcurrentchange)
- [var IOUSBHostCIPortStatusCommandData1Powered: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1powered)
- [var IOUSBHostCIPortStatusCommandData1Speed: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1speed)
- [var IOUSBHostCIPortStatusCommandData1SpeedPhase: Int](/documentation/iousbhost/iousbhostciportstatuscommanddata1speedphase)
- [Anonymous](/documentation/iousbhost/3612477-anonymous)

#### Constants

- [var IOUSBHostCIPortStatusChangeMask: Int](/documentation/iousbhost/iousbhostciportstatuschangemask)
- [var IOUSBHostCIPortStatusConnectChange: Int](/documentation/iousbhost/iousbhostciportstatusconnectchange)
- [var IOUSBHostCIPortStatusConnected: Int](/documentation/iousbhost/iousbhostciportstatusconnected)
- [var IOUSBHostCIPortStatusLinkState: Int](/documentation/iousbhost/iousbhostciportstatuslinkstate)
- [var IOUSBHostCIPortStatusLinkStateChange: Int](/documentation/iousbhost/iousbhostciportstatuslinkstatechange)
- [var IOUSBHostCIPortStatusLinkStatePhase: Int](/documentation/iousbhost/iousbhostciportstatuslinkstatephase)
- [var IOUSBHostCIPortStatusOvercurrent: Int](/documentation/iousbhost/iousbhostciportstatusovercurrent)
- [var IOUSBHostCIPortStatusOvercurrentChange: Int](/documentation/iousbhost/iousbhostciportstatusovercurrentchange)
- [var IOUSBHostCIPortStatusPowered: Int](/documentation/iousbhost/iousbhostciportstatuspowered)
- [var IOUSBHostCIPortStatusSpeed: Int](/documentation/iousbhost/iousbhostciportstatusspeed)
- [var IOUSBHostCIPortStatusSpeedPhase: Int](/documentation/iousbhost/iousbhostciportstatusspeedphase)
- [Anonymous](/documentation/iousbhost/3612478-anonymous)

#### Constants

- [var IOUSBHostCISetupTransferData1bRequest: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1brequest)
- [var IOUSBHostCISetupTransferData1bRequestPhase: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1brequestphase)
- [var IOUSBHostCISetupTransferData1bmRequestType: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1bmrequesttype)
- [var IOUSBHostCISetupTransferData1bmRequestTypePhase: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1bmrequesttypephase)
- [var IOUSBHostCISetupTransferData1wIndex: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1windex)
- [var IOUSBHostCISetupTransferData1wIndexPhase: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1windexphase)
- [var IOUSBHostCISetupTransferData1wLength: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1wlength)
- [var IOUSBHostCISetupTransferData1wLengthPhase: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1wlengthphase)
- [var IOUSBHostCISetupTransferData1wValue: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1wvalue)
- [var IOUSBHostCISetupTransferData1wValuePhase: UInt](/documentation/iousbhost/iousbhostcisetuptransferdata1wvaluephase)
- [Anonymous](/documentation/iousbhost/3612479-anonymous)

#### Constants

- [var IOUSBHostCITransferCompletionMessageControlDeviceAddress: UInt32](/documentation/iousbhost/iousbhostcitransfercompletionmessagecontroldeviceaddress)
- [var IOUSBHostCITransferCompletionMessageControlDeviceAddressPhase: UInt32](/documentation/iousbhost/iousbhostcitransfercompletionmessagecontroldeviceaddressphase)
- [var IOUSBHostCITransferCompletionMessageControlEndpointAddress: UInt32](/documentation/iousbhost/iousbhostcitransfercompletionmessagecontrolendpointaddress)
- [var IOUSBHostCITransferCompletionMessageControlEndpointAddressPhase: UInt32](/documentation/iousbhost/iousbhostcitransfercompletionmessagecontrolendpointaddressphase)
- [var IOUSBHostCITransferCompletionMessageControlStatus: UInt32](/documentation/iousbhost/iousbhostcitransfercompletionmessagecontrolstatus)
- [var IOUSBHostCITransferCompletionMessageControlStatusPhase: UInt32](/documentation/iousbhost/iousbhostcitransfercompletionmessagecontrolstatusphase)
- [var IOUSBHostCITransferCompletionMessageData0TransferLength: Int](/documentation/iousbhost/iousbhostcitransfercompletionmessagedata0transferlength)
- [var IOUSBHostCITransferCompletionMessageData0TransferLengthPhase: Int](/documentation/iousbhost/iousbhostcitransfercompletionmessagedata0transferlengthphase)
- [var IOUSBHostCITransferCompletionMessageData1TransferStructure: UInt](/documentation/iousbhost/iousbhostcitransfercompletionmessagedata1transferstructure)
- [var IOUSBHostCITransferCompletionMessageData1TransferStructurePhase: UInt](/documentation/iousbhost/iousbhostcitransfercompletionmessagedata1transferstructurephase)
- [Anonymous](/documentation/iousbhost/3857646-anonymous)

#### Constants

- [var IOUSBHostCIDeviceUpdateCommandData1DescriptorAddress: UInt](/documentation/iousbhost/iousbhostcideviceupdatecommanddata1descriptoraddress)
- [var IOUSBHostCIDeviceUpdateCommandData1DescriptorAddressPhase: UInt](/documentation/iousbhost/iousbhostcideviceupdatecommanddata1descriptoraddressphase)
- [Anonymous](/documentation/iousbhost/3857647-anonymous)

#### Constants

- [var IOUSBHostCIEndpointUpdateCommandData1Descriptor: UInt](/documentation/iousbhost/iousbhostciendpointupdatecommanddata1descriptor)
- [var IOUSBHostCIEndpointUpdateCommandData1DescriptorPhase: UInt](/documentation/iousbhost/iousbhostciendpointupdatecommanddata1descriptorphase)
- [Anonymous](/documentation/iousbhost/3857648-anonymous)

#### Constants

- [var IOUSBHostCILinkData1TransferStructureAddress: UInt](/documentation/iousbhost/iousbhostcilinkdata1transferstructureaddress)
- [var IOUSBHostCILinkData1TransferStructureAddressPhase: UInt](/documentation/iousbhost/iousbhostcilinkdata1transferstructureaddressphase)
- [IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcicontrollerstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcicontrollerstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIControllerStateActive: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstateactive)
- [var IOUSBHostCIControllerStateOff: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstateoff)
- [var IOUSBHostCIControllerStatePaused: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstatepaused)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcicontrollerstate/rawvalue)
- [IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeed)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcidevicespeed/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcidevicespeed/init(rawvalue:))

#### Constants

- [var IOUSBHostCIDeviceSpeedFull: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedfull)
- [var IOUSBHostCIDeviceSpeedHigh: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedhigh)
- [var IOUSBHostCIDeviceSpeedLow: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedlow)
- [var IOUSBHostCIDeviceSpeedNone: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeednone)
- [var IOUSBHostCIDeviceSpeedSuper: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuper)
- [var IOUSBHostCIDeviceSpeedSuperPlus: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuperplus)
- [var IOUSBHostCIDeviceSpeedSuperPlusBy2: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuperplusby2)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcidevicespeed/rawvalue)
- [IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcidevicestate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcidevicestate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIDeviceStateActive: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestateactive)
- [var IOUSBHostCIDeviceStateDestroyed: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestatedestroyed)
- [var IOUSBHostCIDeviceStatePaused: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestatepaused)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcidevicestate/rawvalue)
- [IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciendpointstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciendpointstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIEndpointStateActive: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstateactive)
- [var IOUSBHostCIEndpointStateDestroyed: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatedestroyed)
- [var IOUSBHostCIEndpointStateHalted: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatehalted)
- [var IOUSBHostCIEndpointStatePaused: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatepaused)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciendpointstate/rawvalue)
- [IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontype)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciexceptiontype/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciexceptiontype/init(rawvalue:))

#### Constants

- [var IOUSBHostCIExceptionTypeCapabilitiesInvalid: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecapabilitiesinvalid)
- [var IOUSBHostCIExceptionTypeCommandFailure: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandfailure)
- [var IOUSBHostCIExceptionTypeCommandReadCollision: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandreadcollision)
- [var IOUSBHostCIExceptionTypeCommandTimeout: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandtimeout)
- [var IOUSBHostCIExceptionTypeCommandWriteFailed: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandwritefailed)
- [var IOUSBHostCIExceptionTypeDoorbellOverflow: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypedoorbelloverflow)
- [var IOUSBHostCIExceptionTypeDoorbellReadCollision: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypedoorbellreadcollision)
- [var IOUSBHostCIExceptionTypeFrameUpdateError: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeframeupdateerror)
- [var IOUSBHostCIExceptionTypeInterruptInvalid: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeinterruptinvalid)
- [var IOUSBHostCIExceptionTypeInterruptOverflow: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeinterruptoverflow)
- [var IOUSBHostCIExceptionTypeProtocolError: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeprotocolerror)
- [var IOUSBHostCIExceptionTypeTerminated: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeterminated)
- [var IOUSBHostCIExceptionTypeUnknown: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeunknown)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciexceptiontype/rawvalue)
- [IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcilinkstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcilinkstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCILinkStateCompliance: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatecompliance)
- [var IOUSBHostCILinkStateDisabled: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatedisabled)
- [var IOUSBHostCILinkStateInactive: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateinactive)
- [var IOUSBHostCILinkStatePolling: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatepolling)
- [var IOUSBHostCILinkStateRecovery: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstaterecovery)
- [var IOUSBHostCILinkStateReset: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatereset)
- [var IOUSBHostCILinkStateResume: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateresume)
- [var IOUSBHostCILinkStateRxDetect: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstaterxdetect)
- [var IOUSBHostCILinkStateTest: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatetest)
- [var IOUSBHostCILinkStateU0: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu0)
- [var IOUSBHostCILinkStateU1: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu1)
- [var IOUSBHostCILinkStateU2: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu2)
- [var IOUSBHostCILinkStateU3: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu3)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcilinkstate/rawvalue)
- [IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatus)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcimessagestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcimessagestatus/init(rawvalue:))

#### Constants

- [var IOUSBHostCIMessageStatusBadArgument: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusbadargument)
- [var IOUSBHostCIMessageStatusEndpointStopped: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusendpointstopped)
- [var IOUSBHostCIMessageStatusError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatuserror)
- [var IOUSBHostCIMessageStatusMissedServiceError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusmissedserviceerror)
- [var IOUSBHostCIMessageStatusNoResources: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusnoresources)
- [var IOUSBHostCIMessageStatusNotPermitted: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusnotpermitted)
- [var IOUSBHostCIMessageStatusOffline: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusoffline)
- [var IOUSBHostCIMessageStatusOverrunError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusoverrunerror)
- [var IOUSBHostCIMessageStatusProtocolError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusprotocolerror)
- [var IOUSBHostCIMessageStatusReserved: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusreserved)
- [var IOUSBHostCIMessageStatusStallError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusstallerror)
- [var IOUSBHostCIMessageStatusSuccess: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatussuccess)
- [var IOUSBHostCIMessageStatusTimeout: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatustimeout)
- [var IOUSBHostCIMessageStatusTransactionError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatustransactionerror)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcimessagestatus/rawvalue)
- [IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetype)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostcimessagetype/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostcimessagetype/init(rawvalue:))

#### Constants

- [var IOUSBHostCIMessageTypeCommandMax: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecommandmax)
- [var IOUSBHostCIMessageTypeCommandMin: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecommandmin)
- [var IOUSBHostCIMessageTypeControllerCapabilities: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollercapabilities)
- [var IOUSBHostCIMessageTypeControllerFrameNumber: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerframenumber)
- [var IOUSBHostCIMessageTypeControllerPause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpause)
- [var IOUSBHostCIMessageTypeControllerPowerOff: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpoweroff)
- [var IOUSBHostCIMessageTypeControllerPowerOn: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpoweron)
- [var IOUSBHostCIMessageTypeControllerStart: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerstart)
- [var IOUSBHostCIMessageTypeDeviceCreate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicecreate)
- [var IOUSBHostCIMessageTypeDeviceDestroy: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicedestroy)
- [var IOUSBHostCIMessageTypeDevicePause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicepause)
- [var IOUSBHostCIMessageTypeDeviceStart: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicestart)
- [var IOUSBHostCIMessageTypeDeviceUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedeviceupdate)
- [var IOUSBHostCIMessageTypeEndpointCreate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointcreate)
- [var IOUSBHostCIMessageTypeEndpointDestroy: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointdestroy)
- [var IOUSBHostCIMessageTypeEndpointPause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointpause)
- [var IOUSBHostCIMessageTypeEndpointReset: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointreset)
- [var IOUSBHostCIMessageTypeEndpointSetNextTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointsetnexttransfer)
- [var IOUSBHostCIMessageTypeEndpointUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointupdate)
- [var IOUSBHostCIMessageTypeEndpoint_reserved_: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpoint_reserved_)
- [var IOUSBHostCIMessageTypeFrameNumberUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeframenumberupdate)
- [var IOUSBHostCIMessageTypeFrameTimestampUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeframetimestampupdate)
- [var IOUSBHostCIMessageTypeIsochronousTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeisochronoustransfer)
- [var IOUSBHostCIMessageTypeLink: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypelink)
- [var IOUSBHostCIMessageTypeNormalTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypenormaltransfer)
- [var IOUSBHostCIMessageTypePortCapabilities: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportcapabilities)
- [var IOUSBHostCIMessageTypePortDisable: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportdisable)
- [var IOUSBHostCIMessageTypePortEvent: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportevent)
- [var IOUSBHostCIMessageTypePortPowerOff: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportpoweroff)
- [var IOUSBHostCIMessageTypePortPowerOn: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportpoweron)
- [var IOUSBHostCIMessageTypePortReset: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportreset)
- [var IOUSBHostCIMessageTypePortResume: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportresume)
- [var IOUSBHostCIMessageTypePortStatus: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportstatus)
- [var IOUSBHostCIMessageTypePortSuspend: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportsuspend)
- [var IOUSBHostCIMessageTypeSetupTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypesetuptransfer)
- [var IOUSBHostCIMessageTypeStatusTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypestatustransfer)
- [var IOUSBHostCIMessageTypeTransferComplete: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypetransfercomplete)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostcimessagetype/rawvalue)
- [IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstate)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciportstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciportstate/init(rawvalue:))

#### Constants

- [var IOUSBHostCIPortStateActive: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstateactive)
- [var IOUSBHostCIPortStateOff: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstateoff)
- [var IOUSBHostCIPortStatePowered: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstatepowered)
- [var IOUSBHostCIPortStateSuspended: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstatesuspended)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciportstate/rawvalue)
- [IOUSBHostCIUserClientVersion](/documentation/iousbhost/iousbhostciuserclientversion)

#### Initializers

- [init(UInt32)](/documentation/iousbhost/iousbhostciuserclientversion/init(_:))
- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostciuserclientversion/init(rawvalue:))

#### Constants

- [var IOUSBHostCIUserClientVersion100: IOUSBHostCIUserClientVersion](/documentation/iousbhost/iousbhostciuserclientversion100)

#### Instance Properties

- [var rawValue: UInt32](/documentation/iousbhost/iousbhostciuserclientversion/rawvalue)
- [IOUSBHostIsochronousTransactionOptions](/documentation/iousbhost/iousbhostisochronoustransactionoptions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostisochronoustransactionoptions/init(rawvalue:))

#### Type Properties

- [static var wrap: IOUSBHostIsochronousTransactionOptions](/documentation/iousbhost/iousbhostisochronoustransactionoptions/wrap)
- [IOUSBHostIsochronousTransferOptions](/documentation/iousbhost/iousbhostisochronoustransferoptions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/iousbhost/iousbhostisochronoustransferoptions/init(rawvalue:))
- [IOUSBHost Constants](/documentation/iousbhost/iousbhost-constants)

### Constants

- [var IOUSBHostCIControllerStateActive: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstateactive)
- [var IOUSBHostCIControllerStateOff: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstateoff)
- [var IOUSBHostCIControllerStatePaused: IOUSBHostCIControllerState](/documentation/iousbhost/iousbhostcicontrollerstatepaused)
- [var IOUSBHostCIDeviceSpeedFull: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedfull)
- [var IOUSBHostCIDeviceSpeedHigh: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedhigh)
- [var IOUSBHostCIDeviceSpeedLow: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedlow)
- [var IOUSBHostCIDeviceSpeedNone: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeednone)
- [var IOUSBHostCIDeviceSpeedSuper: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuper)
- [var IOUSBHostCIDeviceSpeedSuperPlus: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuperplus)
- [var IOUSBHostCIDeviceSpeedSuperPlusBy2: IOUSBHostCIDeviceSpeed](/documentation/iousbhost/iousbhostcidevicespeedsuperplusby2)
- [var IOUSBHostCIDeviceStateActive: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestateactive)
- [var IOUSBHostCIDeviceStateDestroyed: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestatedestroyed)
- [var IOUSBHostCIDeviceStatePaused: IOUSBHostCIDeviceState](/documentation/iousbhost/iousbhostcidevicestatepaused)
- [var IOUSBHostCIEndpointStateActive: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstateactive)
- [var IOUSBHostCIEndpointStateDestroyed: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatedestroyed)
- [var IOUSBHostCIEndpointStateHalted: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatehalted)
- [var IOUSBHostCIEndpointStatePaused: IOUSBHostCIEndpointState](/documentation/iousbhost/iousbhostciendpointstatepaused)
- [var IOUSBHostCIExceptionTypeCapabilitiesInvalid: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecapabilitiesinvalid)
- [var IOUSBHostCIExceptionTypeCommandFailure: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandfailure)
- [var IOUSBHostCIExceptionTypeCommandReadCollision: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandreadcollision)
- [var IOUSBHostCIExceptionTypeCommandTimeout: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandtimeout)
- [var IOUSBHostCIExceptionTypeCommandWriteFailed: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypecommandwritefailed)
- [var IOUSBHostCIExceptionTypeDoorbellOverflow: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypedoorbelloverflow)
- [var IOUSBHostCIExceptionTypeDoorbellReadCollision: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypedoorbellreadcollision)
- [var IOUSBHostCIExceptionTypeFrameUpdateError: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeframeupdateerror)
- [var IOUSBHostCIExceptionTypeInterruptInvalid: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeinterruptinvalid)
- [var IOUSBHostCIExceptionTypeInterruptOverflow: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeinterruptoverflow)
- [var IOUSBHostCIExceptionTypeProtocolError: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeprotocolerror)
- [var IOUSBHostCIExceptionTypeTerminated: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeterminated)
- [var IOUSBHostCIExceptionTypeUnknown: IOUSBHostCIExceptionType](/documentation/iousbhost/iousbhostciexceptiontypeunknown)
- [var IOUSBHostCILinkStateCompliance: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatecompliance)
- [var IOUSBHostCILinkStateDisabled: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatedisabled)
- [var IOUSBHostCILinkStateInactive: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateinactive)
- [var IOUSBHostCILinkStatePolling: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatepolling)
- [var IOUSBHostCILinkStateRecovery: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstaterecovery)
- [var IOUSBHostCILinkStateReset: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatereset)
- [var IOUSBHostCILinkStateResume: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateresume)
- [var IOUSBHostCILinkStateRxDetect: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstaterxdetect)
- [var IOUSBHostCILinkStateTest: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstatetest)
- [var IOUSBHostCILinkStateU0: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu0)
- [var IOUSBHostCILinkStateU1: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu1)
- [var IOUSBHostCILinkStateU2: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu2)
- [var IOUSBHostCILinkStateU3: IOUSBHostCILinkState](/documentation/iousbhost/iousbhostcilinkstateu3)
- [var IOUSBHostCIMessageStatusBadArgument: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusbadargument)
- [var IOUSBHostCIMessageStatusEndpointStopped: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusendpointstopped)
- [var IOUSBHostCIMessageStatusError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatuserror)
- [var IOUSBHostCIMessageStatusMissedServiceError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusmissedserviceerror)
- [var IOUSBHostCIMessageStatusNoResources: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusnoresources)
- [var IOUSBHostCIMessageStatusNotPermitted: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusnotpermitted)
- [var IOUSBHostCIMessageStatusOffline: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusoffline)
- [var IOUSBHostCIMessageStatusOverrunError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusoverrunerror)
- [var IOUSBHostCIMessageStatusProtocolError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusprotocolerror)
- [var IOUSBHostCIMessageStatusReserved: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusreserved)
- [var IOUSBHostCIMessageStatusStallError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusstallerror)
- [var IOUSBHostCIMessageStatusSuccess: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatussuccess)
- [var IOUSBHostCIMessageStatusTimeout: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatustimeout)
- [var IOUSBHostCIMessageStatusTransactionError: IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatustransactionerror)
- [var IOUSBHostCIMessageTypeCommandMax: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecommandmax)
- [var IOUSBHostCIMessageTypeCommandMin: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecommandmin)
- [var IOUSBHostCIMessageTypeControllerCapabilities: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollercapabilities)
- [var IOUSBHostCIMessageTypeControllerFrameNumber: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerframenumber)
- [var IOUSBHostCIMessageTypeControllerPause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpause)
- [var IOUSBHostCIMessageTypeControllerPowerOff: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpoweroff)
- [var IOUSBHostCIMessageTypeControllerPowerOn: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerpoweron)
- [var IOUSBHostCIMessageTypeControllerStart: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypecontrollerstart)
- [var IOUSBHostCIMessageTypeDeviceCreate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicecreate)
- [var IOUSBHostCIMessageTypeDeviceDestroy: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicedestroy)
- [var IOUSBHostCIMessageTypeDevicePause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicepause)
- [var IOUSBHostCIMessageTypeDeviceStart: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedevicestart)
- [var IOUSBHostCIMessageTypeDeviceUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypedeviceupdate)
- [var IOUSBHostCIMessageTypeEndpointCreate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointcreate)
- [var IOUSBHostCIMessageTypeEndpointDestroy: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointdestroy)
- [var IOUSBHostCIMessageTypeEndpointPause: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointpause)
- [var IOUSBHostCIMessageTypeEndpointReset: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointreset)
- [var IOUSBHostCIMessageTypeEndpointSetNextTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointsetnexttransfer)
- [var IOUSBHostCIMessageTypeEndpointUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpointupdate)
- [var IOUSBHostCIMessageTypeEndpoint_reserved_: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeendpoint_reserved_)
- [var IOUSBHostCIMessageTypeFrameNumberUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeframenumberupdate)
- [var IOUSBHostCIMessageTypeFrameTimestampUpdate: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeframetimestampupdate)
- [var IOUSBHostCIMessageTypeIsochronousTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeisochronoustransfer)
- [var IOUSBHostCIMessageTypeLink: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypelink)
- [var IOUSBHostCIMessageTypeNormalTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypenormaltransfer)
- [var IOUSBHostCIMessageTypePortCapabilities: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportcapabilities)
- [var IOUSBHostCIMessageTypePortDisable: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportdisable)
- [var IOUSBHostCIMessageTypePortEvent: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportevent)
- [var IOUSBHostCIMessageTypePortPowerOff: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportpoweroff)
- [var IOUSBHostCIMessageTypePortPowerOn: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportpoweron)
- [var IOUSBHostCIMessageTypePortReset: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportreset)
- [var IOUSBHostCIMessageTypePortResume: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportresume)
- [var IOUSBHostCIMessageTypePortStatus: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportstatus)
- [var IOUSBHostCIMessageTypePortSuspend: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypeportsuspend)
- [var IOUSBHostCIMessageTypeSetupTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypesetuptransfer)
- [var IOUSBHostCIMessageTypeStatusTransfer: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypestatustransfer)
- [var IOUSBHostCIMessageTypeTransferComplete: IOUSBHostCIMessageType](/documentation/iousbhost/iousbhostcimessagetypetransfercomplete)
- [var IOUSBHostCIPortStateActive: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstateactive)
- [var IOUSBHostCIPortStateOff: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstateoff)
- [var IOUSBHostCIPortStatePowered: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstatepowered)
- [var IOUSBHostCIPortStateSuspended: IOUSBHostCIPortState](/documentation/iousbhost/iousbhostciportstatesuspended)
- [var IOUSBHostCIUserClientVersion100: IOUSBHostCIUserClientVersion](/documentation/iousbhost/iousbhostciuserclientversion100)
- [IOUSBHost Functions](/documentation/iousbhost/iousbhost-functions)

### Functions

- [func IOUSBGetEndpointBurstSize(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!, UnsafePointer<IOUSBSuperSpeedEndpointCompanionDescriptor>!, UnsafePointer<IOUSBSuperSpeedPlusIsochronousEndpointCompanionDescriptor>!) -> UInt32](/documentation/iousbhost/iousbgetendpointburstsize(_:_:_:_:))
- [func IOUSBGetEndpointMult(UInt32, UnsafePointer<IOUSBEndpointDescriptor>!, UnsafePointer<IOUSBSuperSpeedEndpointCompanionDescriptor>!, UnsafePointer<IOUSBSuperSpeedPlusIsochronousEndpointCompanionDescriptor>!) -> UInt8](/documentation/iousbhost/iousbgetendpointmult(_:_:_:_:))
- [func IOUSBGetEndpointSynchronizationType(UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt8](/documentation/iousbhost/iousbgetendpointsynchronizationtype(_:))
- [func IOUSBGetEndpointUsageType(UnsafePointer<IOUSBEndpointDescriptor>!) -> UInt8](/documentation/iousbhost/iousbgetendpointusagetype(_:))
- [func IOUSBGetPlatformCapabilityDescriptor(UnsafePointer<IOUSBBOSDescriptor>!) -> UnsafePointer<IOUSBPlatformCapabilityDescriptor>!](/documentation/iousbhost/iousbgetplatformcapabilitydescriptor(_:))
- [func IOUSBGetPlatformCapabilityDescriptorWithUUID(UnsafePointer<IOUSBBOSDescriptor>!, UnsafeMutablePointer<UInt8>!) -> UnsafePointer<IOUSBPlatformCapabilityDescriptor>!](/documentation/iousbhost/iousbgetplatformcapabilitydescriptorwithuuid(_:_:))
- [func IOUSBGetSuperSpeedPlusDeviceCapabilityDescriptor(UnsafePointer<IOUSBBOSDescriptor>!) -> UnsafePointer<IOUSBDeviceCapabilitySuperSpeedPlusUSB>!](/documentation/iousbhost/iousbgetsuperspeedplusdevicecapabilitydescriptor(_:))
- [func IOUSBHostCIControllerStateToString(IOUSBHostCIControllerState) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostcicontrollerstatetostring(_:))
- [func IOUSBHostCIDeviceSpeedToString(IOUSBHostCIDeviceSpeed) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostcidevicespeedtostring(_:))
- [func IOUSBHostCIDeviceStateToString(IOUSBHostCIDeviceState) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostcidevicestatetostring(_:))
- [func IOUSBHostCIEndpointStateToString(IOUSBHostCIEndpointState) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostciendpointstatetostring(_:))
- [func IOUSBHostCIExceptionTypeToString(IOUSBHostCIExceptionType) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostciexceptiontypetostring(_:))
- [func IOUSBHostCILinkStateEnabled(IOUSBHostCILinkState) -> Bool](/documentation/iousbhost/iousbhostcilinkstateenabled(_:))
- [func IOUSBHostCILinkStateToString(IOUSBHostCILinkState) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostcilinkstatetostring(_:))
- [func IOUSBHostCIMessageStatusFromIOReturn(IOReturn) -> IOUSBHostCIMessageStatus](/documentation/iousbhost/iousbhostcimessagestatusfromioreturn(_:))
- [func IOUSBHostCIMessageStatusToIOReturn(IOUSBHostCIMessageStatus) -> IOReturn](/documentation/iousbhost/iousbhostcimessagestatustoioreturn(_:))
- [func IOUSBHostCIMessageStatusToString(IOUSBHostCIMessageStatus) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostcimessagestatustostring(_:))
- [func IOUSBHostCIMessageTypeToString(IOUSBHostCIMessageType) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostcimessagetypetostring(_:))
- [func IOUSBHostCIPortStateToString(IOUSBHostCIPortState) -> UnsafePointer<CChar>!](/documentation/iousbhost/iousbhostciportstatetostring(_:))
- [IOUSBHost Data Types](/documentation/iousbhost/iousbhost-data-types)

### Data Types

- [IOUSBHostCIDoorbell](/documentation/iousbhost/iousbhostcidoorbell)
- [IOUSBHostCIPortStatus](/documentation/iousbhost/iousbhostciportstatus)
- [IOUSBHostControllerInterfaceCommandHandler](/documentation/iousbhost/iousbhostcontrollerinterfacecommandhandler)
- [IOUSBHostControllerInterfaceDoorbellHandler](/documentation/iousbhost/iousbhostcontrollerinterfacedoorbellhandler)
- [IOUSBHostIsochronousTransactionCompletionHandler](/documentation/iousbhost/iousbhostisochronoustransactioncompletionhandler)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
