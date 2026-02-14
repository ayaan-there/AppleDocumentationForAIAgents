# IOBluetooth Documentation

Source: https://sosumi.ai/documentation/iobluetooth

---
title: IOBluetooth
source: https://developer.apple.com/documentation/iobluetooth
timestamp: 2026-02-13T18:58:17.134Z
---

## Classes

- [IOBluetoothDevice](/documentation/iobluetooth/iobluetoothdevice)

### Initializers

- [convenience init!(address: UnsafePointer<BluetoothDeviceAddress>!)](/documentation/iobluetooth/iobluetoothdevice/init(address:))
- [convenience init!(addressString: String!)](/documentation/iobluetooth/iobluetoothdevice/init(addressstring:))

### Instance Properties

- [var addressString: String!](/documentation/iobluetooth/iobluetoothdevice/addressstring)
- [var classOfDevice: BluetoothClassOfDevice](/documentation/iobluetooth/iobluetoothdevice/classofdevice)
- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/iobluetoothdevice/connectionhandle)
- [var deviceClassMajor: BluetoothDeviceClassMajor](/documentation/iobluetooth/iobluetoothdevice/deviceclassmajor)
- [var deviceClassMinor: BluetoothDeviceClassMinor](/documentation/iobluetooth/iobluetoothdevice/deviceclassminor)
- [var isHandsFreeAudioGateway: Bool](/documentation/iobluetooth/iobluetoothdevice/ishandsfreeaudiogateway)
- [var isHandsFreeDevice: Bool](/documentation/iobluetooth/iobluetoothdevice/ishandsfreedevice)
- [var lastNameUpdate: Date!](/documentation/iobluetooth/iobluetoothdevice/lastnameupdate)
- [var name: String!](/documentation/iobluetooth/iobluetoothdevice/name)
- [var nameOrAddress: String!](/documentation/iobluetooth/iobluetoothdevice/nameoraddress)
- [var serviceClassMajor: BluetoothServiceClassMajor](/documentation/iobluetooth/iobluetoothdevice/serviceclassmajor)
- [var services: [Any]!](/documentation/iobluetooth/iobluetoothdevice/services)

### Instance Methods

- [func addToFavorites() -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/addtofavorites())
- [func awakeAfter(using: NSCoder!) -> Any!](/documentation/iobluetooth/iobluetoothdevice/awakeafter(using:))
- [func closeConnection() -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/closeconnection())
- [func getAddress() -> UnsafePointer<BluetoothDeviceAddress>!](/documentation/iobluetooth/iobluetoothdevice/getaddress())
- [func getClockOffset() -> BluetoothClockOffset](/documentation/iobluetooth/iobluetoothdevice/getclockoffset())
- [func getEncryptionMode() -> BluetoothHCIEncryptionMode](/documentation/iobluetooth/iobluetoothdevice/getencryptionmode())
- [func getLastInquiryUpdate() -> Date!](/documentation/iobluetooth/iobluetoothdevice/getlastinquiryupdate())
- [func getLastServicesUpdate() -> Date!](/documentation/iobluetooth/iobluetoothdevice/getlastservicesupdate())
- [func getLinkType() -> BluetoothLinkType](/documentation/iobluetooth/iobluetoothdevice/getlinktype())
- [func getPageScanMode() -> BluetoothPageScanMode](/documentation/iobluetooth/iobluetoothdevice/getpagescanmode())
- [func getPageScanPeriodMode() -> BluetoothPageScanPeriodMode](/documentation/iobluetooth/iobluetoothdevice/getpagescanperiodmode())
- [func getPageScanRepetitionMode() -> BluetoothPageScanRepetitionMode](/documentation/iobluetooth/iobluetoothdevice/getpagescanrepetitionmode())
- [func getServiceRecord(for: IOBluetoothSDPUUID!) -> IOBluetoothSDPServiceRecord!](/documentation/iobluetooth/iobluetoothdevice/getservicerecord(for:))
- [func handsFreeAudioGatewayServiceRecord() -> IOBluetoothSDPServiceRecord!](/documentation/iobluetooth/iobluetoothdevice/handsfreeaudiogatewayservicerecord())
- [func handsFreeDeviceServiceRecord() -> IOBluetoothSDPServiceRecord!](/documentation/iobluetooth/iobluetoothdevice/handsfreedeviceservicerecord())
- [func isConnected() -> Bool](/documentation/iobluetooth/iobluetoothdevice/isconnected())
- [func isFavorite() -> Bool](/documentation/iobluetooth/iobluetoothdevice/isfavorite())
- [func isIncoming() -> Bool](/documentation/iobluetooth/iobluetoothdevice/isincoming())
- [func isPaired() -> Bool](/documentation/iobluetooth/iobluetoothdevice/ispaired())
- [func openConnection() -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openconnection())
- [func openConnection(Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openconnection(_:))
- [func openConnection(Any!, withPageTimeout: BluetoothHCIPageTimeout, authenticationRequired: Bool) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openconnection(_:withpagetimeout:authenticationrequired:))
- [func openL2CAPChannelAsync(AutoreleasingUnsafeMutablePointer<IOBluetoothL2CAPChannel?>!, withPSM: BluetoothL2CAPPSM, delegate: Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openl2capchannelasync(_:withpsm:delegate:))
- [func openL2CAPChannelAsync(AutoreleasingUnsafeMutablePointer<IOBluetoothL2CAPChannel?>!, withPSM: BluetoothL2CAPPSM, withConfiguration: [AnyHashable : Any]!, delegate: Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openl2capchannelasync(_:withpsm:withconfiguration:delegate:))
- [func openL2CAPChannelSync(AutoreleasingUnsafeMutablePointer<IOBluetoothL2CAPChannel?>!, withPSM: BluetoothL2CAPPSM, delegate: Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openl2capchannelsync(_:withpsm:delegate:))
- [func openL2CAPChannelSync(AutoreleasingUnsafeMutablePointer<IOBluetoothL2CAPChannel?>!, withPSM: BluetoothL2CAPPSM, withConfiguration: [AnyHashable : Any]!, delegate: Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openl2capchannelsync(_:withpsm:withconfiguration:delegate:))
- [func openRFCOMMChannelAsync(AutoreleasingUnsafeMutablePointer<IOBluetoothRFCOMMChannel?>!, withChannelID: BluetoothRFCOMMChannelID, delegate: Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openrfcommchannelasync(_:withchannelid:delegate:))
- [func openRFCOMMChannelSync(AutoreleasingUnsafeMutablePointer<IOBluetoothRFCOMMChannel?>!, withChannelID: BluetoothRFCOMMChannelID, delegate: Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/openrfcommchannelsync(_:withchannelid:delegate:))
- [func performSDPQuery(Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/performsdpquery(_:))
- [func performSDPQuery(Any!, uuids: [Any]!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/performsdpquery(_:uuids:))
- [func rawRSSI() -> BluetoothHCIRSSIValue](/documentation/iobluetooth/iobluetoothdevice/rawrssi())
- [func recentAccessDate() -> Date!](/documentation/iobluetooth/iobluetoothdevice/recentaccessdate())
- [func register(forDisconnectNotification: Any!, selector: Selector!) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothdevice/register(fordisconnectnotification:selector:))
- [func remoteNameRequest(Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/remotenamerequest(_:))
- [func remoteNameRequest(Any!, withPageTimeout: BluetoothHCIPageTimeout) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/remotenamerequest(_:withpagetimeout:))
- [func removeFromFavorites() -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/removefromfavorites())
- [func requestAuthentication() -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/requestauthentication())
- [func rssi() -> BluetoothHCIRSSIValue](/documentation/iobluetooth/iobluetoothdevice/rssi())
- [func sendL2CAPEchoRequest(UnsafeMutableRawPointer!, length: UInt16) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/sendl2capechorequest(_:length:))
- [func setSupervisionTimeout(UInt16) -> IOReturn](/documentation/iobluetooth/iobluetoothdevice/setsupervisiontimeout(_:))

### Type Methods

- [class func favoriteDevices() -> [Any]!](/documentation/iobluetooth/iobluetoothdevice/favoritedevices())
- [class func pairedDevices() -> [Any]!](/documentation/iobluetooth/iobluetoothdevice/paireddevices())
- [class func recentDevices(UInt) -> [Any]!](/documentation/iobluetooth/iobluetoothdevice/recentdevices(_:))
- [class func register(forConnectNotifications: Any!, selector: Selector!) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothdevice/register(forconnectnotifications:selector:))
- [IOBluetoothDeviceInquiry](/documentation/iobluetooth/iobluetoothdeviceinquiry)

### Initializers

- [init!(delegate: Any!)](/documentation/iobluetooth/iobluetoothdeviceinquiry/init(delegate:))

### Instance Properties

- [var delegate: AnyObject?](/documentation/iobluetooth/iobluetoothdeviceinquiry/delegate)
- [var inquiryLength: UInt8](/documentation/iobluetooth/iobluetoothdeviceinquiry/inquirylength)
- [var searchType: IOBluetoothDeviceSearchTypes](/documentation/iobluetooth/iobluetoothdeviceinquiry/searchtype)
- [var updateNewDeviceNames: Bool](/documentation/iobluetooth/iobluetoothdeviceinquiry/updatenewdevicenames)

### Instance Methods

- [func clearFoundDevices()](/documentation/iobluetooth/iobluetoothdeviceinquiry/clearfounddevices())
- [func foundDevices() -> [Any]!](/documentation/iobluetooth/iobluetoothdeviceinquiry/founddevices())
- [func setSearchCriteria(BluetoothServiceClassMajor, majorDeviceClass: BluetoothDeviceClassMajor, minorDeviceClass: BluetoothDeviceClassMinor)](/documentation/iobluetooth/iobluetoothdeviceinquiry/setsearchcriteria(_:majordeviceclass:minordeviceclass:))
- [func start() -> IOReturn](/documentation/iobluetooth/iobluetoothdeviceinquiry/start())
- [func stop() -> IOReturn](/documentation/iobluetooth/iobluetoothdeviceinquiry/stop())
- [IOBluetoothDevicePair](/documentation/iobluetooth/iobluetoothdevicepair)

### Initializers

- [convenience init!(device: IOBluetoothDevice!)](/documentation/iobluetooth/iobluetoothdevicepair/init(device:))

### Instance Properties

- [var delegate: AnyObject!](/documentation/iobluetooth/iobluetoothdevicepair/delegate)

### Instance Methods

- [func device() -> IOBluetoothDevice!](/documentation/iobluetooth/iobluetoothdevicepair/device())
- [func replyPINCode(Int, pinCode: UnsafeMutablePointer<BluetoothPINCode>!)](/documentation/iobluetooth/iobluetoothdevicepair/replypincode(_:pincode:))
- [func replyUserConfirmation(Bool)](/documentation/iobluetooth/iobluetoothdevicepair/replyuserconfirmation(_:))
- [func setDevice(IOBluetoothDevice!)](/documentation/iobluetooth/iobluetoothdevicepair/setdevice(_:))
- [func start() -> IOReturn](/documentation/iobluetooth/iobluetoothdevicepair/start())
- [func stop()](/documentation/iobluetooth/iobluetoothdevicepair/stop())
- [IOBluetoothDeviceRef](/documentation/iobluetooth/iobluetoothdeviceref)
- [IOBluetoothHandsFree](/documentation/iobluetooth/iobluetoothhandsfree)

### Initializers

- [init!(device: IOBluetoothDevice!, delegate: (any IOBluetoothHandsFreeDelegate)!)](/documentation/iobluetooth/iobluetoothhandsfree/init(device:delegate:))

### Instance Properties

- [var delegate: (any IOBluetoothHandsFreeDelegate)!](/documentation/iobluetooth/iobluetoothhandsfree/delegate)
- [var device: IOBluetoothDevice!](/documentation/iobluetooth/iobluetoothhandsfree/device)
- [var deviceCallHoldModes: UInt32](/documentation/iobluetooth/iobluetoothhandsfree/devicecallholdmodes)
- [var deviceSupportedFeatures: UInt32](/documentation/iobluetooth/iobluetoothhandsfree/devicesupportedfeatures)
- [var deviceSupportedSMSServices: UInt32](/documentation/iobluetooth/iobluetoothhandsfree/devicesupportedsmsservices)
- [var inputVolume: Float](/documentation/iobluetooth/iobluetoothhandsfree/inputvolume)
- [var isConnected: Bool](/documentation/iobluetooth/iobluetoothhandsfree/isconnected)
- [var isInputMuted: Bool](/documentation/iobluetooth/iobluetoothhandsfree/isinputmuted)
- [var isOutputMuted: Bool](/documentation/iobluetooth/iobluetoothhandsfree/isoutputmuted)
- [var isSMSEnabled: Bool](/documentation/iobluetooth/iobluetoothhandsfree/issmsenabled)
- [var outputVolume: Float](/documentation/iobluetooth/iobluetoothhandsfree/outputvolume)
- [var smsMode: IOBluetoothSMSMode](/documentation/iobluetooth/iobluetoothhandsfree/smsmode)
- [var supportedFeatures: UInt32](/documentation/iobluetooth/iobluetoothhandsfree/supportedfeatures)

### Instance Methods

- [func connect()](/documentation/iobluetooth/iobluetoothhandsfree/connect())
- [func connectSCO()](/documentation/iobluetooth/iobluetoothhandsfree/connectsco())
- [func disconnect()](/documentation/iobluetooth/iobluetoothhandsfree/disconnect())
- [func disconnectSCO()](/documentation/iobluetooth/iobluetoothhandsfree/disconnectsco())
- [func indicator(String!) -> Int32](/documentation/iobluetooth/iobluetoothhandsfree/indicator(_:))
- [func isSCOConnected() -> Bool](/documentation/iobluetooth/iobluetoothhandsfree/isscoconnected())
- [func setIndicator(String!, value: Int32)](/documentation/iobluetooth/iobluetoothhandsfree/setindicator(_:value:))
- [IOBluetoothHandsFreeAudioGateway](/documentation/iobluetooth/iobluetoothhandsfreeaudiogateway)

### Creating a Gateway

- [init!(device: IOBluetoothDevice!, delegate: Any!)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogateway/init(device:delegate:))

### Showing Status Indicators

- [func createIndicator(String!, min: Int32, max: Int32, currentValue: Int32)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogateway/createindicator(_:min:max:currentvalue:))
- [Status Indicator Constants](/documentation/iobluetooth/status-indicator-constants)

#### Call Status

- [let IOBluetoothHandsFreeIndicatorCall: String](/documentation/iobluetooth/iobluetoothhandsfreeindicatorcall)
- [let IOBluetoothHandsFreeIndicatorCallHeld: String](/documentation/iobluetooth/iobluetoothhandsfreeindicatorcallheld)
- [let IOBluetoothHandsFreeIndicatorCallSetup: String](/documentation/iobluetooth/iobluetoothhandsfreeindicatorcallsetup)

#### Phone Network Connection

- [let IOBluetoothHandsFreeIndicatorRoam: String](/documentation/iobluetooth/iobluetoothhandsfreeindicatorroam)
- [let IOBluetoothHandsFreeIndicatorSignal: String](/documentation/iobluetooth/iobluetoothhandsfreeindicatorsignal)
- [let IOBluetoothHandsFreeIndicatorService: String](/documentation/iobluetooth/iobluetoothhandsfreeindicatorservice)

#### Phone Status

- [let IOBluetoothHandsFreeIndicatorBattChg: String](/documentation/iobluetooth/iobluetoothhandsfreeindicatorbattchg)

### Sending and Receiving Commands

- [func sendResponse(String!)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogateway/sendresponse(_:))
- [func sendResponse(String!, withOK: Bool)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogateway/sendresponse(_:withok:))
- [func sendOKResponse()](/documentation/iobluetooth/iobluetoothhandsfreeaudiogateway/sendokresponse())
- [func process(atCommand: String!)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogateway/process(atcommand:))
- [IOBluetoothHandsFreeDevice](/documentation/iobluetooth/iobluetoothhandsfreedevice)

### Creating a Hands-Free Device Manager

- [init!(device: IOBluetoothDevice!, delegate: Any!)](/documentation/iobluetooth/iobluetoothhandsfreedevice/init(device:delegate:))

### Accepting Calls

- [func acceptCall()](/documentation/iobluetooth/iobluetoothhandsfreedevice/acceptcall())
- [func acceptCallOnPhone()](/documentation/iobluetooth/iobluetoothhandsfreedevice/acceptcallonphone())
- [func callTransfer()](/documentation/iobluetooth/iobluetoothhandsfreedevice/calltransfer())

### Dialing Calls

- [func dialNumber(String!)](/documentation/iobluetooth/iobluetoothhandsfreedevice/dialnumber(_:))
- [func memoryDial(Int32)](/documentation/iobluetooth/iobluetoothhandsfreedevice/memorydial(_:))
- [func redial()](/documentation/iobluetooth/iobluetoothhandsfreedevice/redial())

### Holding Calls

- [func holdCall()](/documentation/iobluetooth/iobluetoothhandsfreedevice/holdcall())
- [func addHeldCall()](/documentation/iobluetooth/iobluetoothhandsfreedevice/addheldcall())
- [func placeAllOthers(onHold: Int32)](/documentation/iobluetooth/iobluetoothhandsfreedevice/placeallothers(onhold:))

### Ending Calls

- [func endCall()](/documentation/iobluetooth/iobluetoothhandsfreedevice/endcall())
- [func releaseCall(Int32)](/documentation/iobluetooth/iobluetoothhandsfreedevice/releasecall(_:))
- [func releaseActiveCalls()](/documentation/iobluetooth/iobluetoothhandsfreedevice/releaseactivecalls())
- [func releaseHeldCalls()](/documentation/iobluetooth/iobluetoothhandsfreedevice/releaseheldcalls())

### Sending Messages and Commands

- [func sendSMS(String!, message: String!)](/documentation/iobluetooth/iobluetoothhandsfreedevice/sendsms(_:message:))
- [func sendDTMF(String!)](/documentation/iobluetooth/iobluetoothhandsfreedevice/senddtmf(_:))
- [func send(atCommand: String!)](/documentation/iobluetooth/iobluetoothhandsfreedevice/send(atcommand:))
- [func send(atCommand: String!, timeout: Float, selector: Selector!, target: Any!)](/documentation/iobluetooth/iobluetoothhandsfreedevice/send(atcommand:timeout:selector:target:))

### Requesting Status Information

- [func subscriberNumber()](/documentation/iobluetooth/iobluetoothhandsfreedevice/subscribernumber())
- [func currentCallList()](/documentation/iobluetooth/iobluetoothhandsfreedevice/currentcalllist())

### Transferring Audio

- [func transferAudioToComputer()](/documentation/iobluetooth/iobluetoothhandsfreedevice/transferaudiotocomputer())
- [func transferAudioToPhone()](/documentation/iobluetooth/iobluetoothhandsfreedevice/transferaudiotophone())
- [IOBluetoothHostController](/documentation/iobluetooth/iobluetoothhostcontroller)

### Instance Properties

- [var delegate: AnyObject!](/documentation/iobluetooth/iobluetoothhostcontroller/delegate)
- [var powerState: BluetoothHCIPowerState](/documentation/iobluetooth/iobluetoothhostcontroller/powerstate)

### Instance Methods

- [func addressAsString() -> String!](/documentation/iobluetooth/iobluetoothhostcontroller/addressasstring())
- [func classOfDevice() -> BluetoothClassOfDevice](/documentation/iobluetooth/iobluetoothhostcontroller/classofdevice())
- [func nameAsString() -> String!](/documentation/iobluetooth/iobluetoothhostcontroller/nameasstring())
- [func setClassOfDevice(BluetoothClassOfDevice, forTimeInterval: TimeInterval) -> IOReturn](/documentation/iobluetooth/iobluetoothhostcontroller/setclassofdevice(_:fortimeinterval:))

### Type Methods

- [class func `default`() -> Self!](/documentation/iobluetooth/iobluetoothhostcontroller/default())
- [IOBluetoothL2CAPChannel](/documentation/iobluetooth/iobluetoothl2capchannel)

### Instance Properties

- [var device: IOBluetoothDevice!](/documentation/iobluetooth/iobluetoothl2capchannel/device)
- [var incomingMTU: BluetoothL2CAPMTU](/documentation/iobluetooth/iobluetoothl2capchannel/incomingmtu)
- [var localChannelID: BluetoothL2CAPChannelID](/documentation/iobluetooth/iobluetoothl2capchannel/localchannelid)
- [var objectID: IOBluetoothObjectID](/documentation/iobluetooth/iobluetoothl2capchannel/objectid)
- [var outgoingMTU: BluetoothL2CAPMTU](/documentation/iobluetooth/iobluetoothl2capchannel/outgoingmtu)
- [var psm: BluetoothL2CAPPSM](/documentation/iobluetooth/iobluetoothl2capchannel/psm)
- [var remoteChannelID: BluetoothL2CAPChannelID](/documentation/iobluetooth/iobluetoothl2capchannel/remotechannelid)

### Instance Methods

- [func close() -> IOReturn](/documentation/iobluetooth/iobluetoothl2capchannel/close())
- [func delegate() -> Any!](/documentation/iobluetooth/iobluetoothl2capchannel/delegate())
- [func isIncoming() -> Bool](/documentation/iobluetooth/iobluetoothl2capchannel/isincoming())
- [func register(forChannelCloseNotification: Any!, selector: Selector!) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothl2capchannel/register(forchannelclosenotification:selector:))
- [func requestRemoteMTU(BluetoothL2CAPMTU) -> IOReturn](/documentation/iobluetooth/iobluetoothl2capchannel/requestremotemtu(_:))
- [func setDelegate(Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothl2capchannel/setdelegate(_:))
- [func setDelegate(Any!, withConfiguration: [AnyHashable : Any]!) -> IOReturn](/documentation/iobluetooth/iobluetoothl2capchannel/setdelegate(_:withconfiguration:))
- [func writeAsync(UnsafeMutableRawPointer!, length: UInt16, refcon: UnsafeMutableRawPointer!) -> IOReturn](/documentation/iobluetooth/iobluetoothl2capchannel/writeasync(_:length:refcon:))
- [func writeAsyncTrap(UnsafeMutableRawPointer!, length: UInt16, refcon: UnsafeMutableRawPointer!) -> IOReturn](/documentation/iobluetooth/iobluetoothl2capchannel/writeasynctrap(_:length:refcon:))
- [func writeSync(UnsafeMutableRawPointer!, length: UInt16) -> IOReturn](/documentation/iobluetooth/iobluetoothl2capchannel/writesync(_:length:))

### Type Methods

- [class func register(forChannelOpenNotifications: Any!, selector: Selector!) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothl2capchannel/register(forchannelopennotifications:selector:))
- [class func register(forChannelOpenNotifications: Any!, selector: Selector!, withPSM: BluetoothL2CAPPSM, direction: IOBluetoothUserNotificationChannelDirection) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothl2capchannel/register(forchannelopennotifications:selector:withpsm:direction:))
- [class func withObjectID(IOBluetoothObjectID) -> Self!](/documentation/iobluetooth/iobluetoothl2capchannel/withobjectid(_:))
- [IOBluetoothL2CAPChannelRef](/documentation/iobluetooth/iobluetoothl2capchannelref)
- [IOBluetoothOBEXSession](/documentation/iobluetooth/iobluetoothobexsession)

### Initializers

- [init!(device: IOBluetoothDevice!, channelID: BluetoothRFCOMMChannelID)](/documentation/iobluetooth/iobluetoothobexsession/init(device:channelid:))
- [init!(incomingRFCOMMChannel: IOBluetoothRFCOMMChannel!, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!)](/documentation/iobluetooth/iobluetoothobexsession/init(incomingrfcommchannel:eventselector:selectortarget:refcon:))
- [init!(sdpServiceRecord: IOBluetoothSDPServiceRecord!)](/documentation/iobluetooth/iobluetoothobexsession/init(sdpservicerecord:))

### Instance Methods

- [func closeTransportConnection() -> OBEXError](/documentation/iobluetooth/iobluetoothobexsession/closetransportconnection())
- [func getDevice() -> IOBluetoothDevice!](/documentation/iobluetooth/iobluetoothobexsession/getdevice())
- [func getRFCOMMChannel() -> IOBluetoothRFCOMMChannel!](/documentation/iobluetooth/iobluetoothobexsession/getrfcommchannel())
- [func hasOpenTransportConnection() -> Bool](/documentation/iobluetooth/iobluetoothobexsession/hasopentransportconnection())
- [func isSessionTargetAMac() -> Bool](/documentation/iobluetooth/iobluetoothobexsession/issessiontargetamac())
- [func openTransportConnection(Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/iobluetoothobexsession/opentransportconnection(_:selectortarget:refcon:))
- [func restartTransmission()](/documentation/iobluetooth/iobluetoothobexsession/restarttransmission())
- [func sendBufferTroughChannel() -> IOReturn](/documentation/iobluetooth/iobluetoothobexsession/sendbuffertroughchannel())
- [func sendData(toTransport: UnsafeMutableRawPointer!, dataLength: Int) -> OBEXError](/documentation/iobluetooth/iobluetoothobexsession/senddata(totransport:datalength:))
- [func setOBEXSessionOpenConnectionCallback(IOBluetoothOBEXSessionOpenConnectionCallback!, refCon: UnsafeMutableRawPointer!)](/documentation/iobluetooth/iobluetoothobexsession/setobexsessionopenconnectioncallback(_:refcon:))
- [func setOpenTransportConnectionAsyncSelector(Selector!, target: Any!, refCon: UnsafeMutableRawPointer!)](/documentation/iobluetooth/iobluetoothobexsession/setopentransportconnectionasyncselector(_:target:refcon:))

### Type Methods

- [class func withDevice(IOBluetoothDevice!, channelID: BluetoothRFCOMMChannelID) -> Self!](/documentation/iobluetooth/iobluetoothobexsession/withdevice(_:channelid:))
- [class func withIncomingRFCOMMChannel(IOBluetoothRFCOMMChannel!, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> Self!](/documentation/iobluetooth/iobluetoothobexsession/withincomingrfcommchannel(_:eventselector:selectortarget:refcon:))
- [class func withSDPServiceRecord(IOBluetoothSDPServiceRecord!) -> Self!](/documentation/iobluetooth/iobluetoothobexsession/withsdpservicerecord(_:))
- [IOBluetoothObject](/documentation/iobluetooth/iobluetoothobject)
- [IOBluetoothObjectRef](/documentation/iobluetooth/iobluetoothobjectref)
- [IOBluetoothRFCOMMChannel](/documentation/iobluetooth/iobluetoothrfcommchannel)

### Instance Methods

- [func close() -> IOReturn](/documentation/iobluetooth/iobluetoothrfcommchannel/close())
- [func delegate() -> Any!](/documentation/iobluetooth/iobluetoothrfcommchannel/delegate())
- [func getDevice() -> IOBluetoothDevice!](/documentation/iobluetooth/iobluetoothrfcommchannel/getdevice())
- [func getID() -> BluetoothRFCOMMChannelID](/documentation/iobluetooth/iobluetoothrfcommchannel/getid())
- [func getMTU() -> BluetoothRFCOMMMTU](/documentation/iobluetooth/iobluetoothrfcommchannel/getmtu())
- [func getObjectID() -> IOBluetoothObjectID](/documentation/iobluetooth/iobluetoothrfcommchannel/getobjectid())
- [func getRef() -> Unmanaged<IOBluetoothRFCOMMChannelRef>!](/documentation/iobluetooth/iobluetoothrfcommchannel/getref())
- [func isIncoming() -> Bool](/documentation/iobluetooth/iobluetoothrfcommchannel/isincoming())
- [func isOpen() -> Bool](/documentation/iobluetooth/iobluetoothrfcommchannel/isopen())
- [func isTransmissionPaused() -> Bool](/documentation/iobluetooth/iobluetoothrfcommchannel/istransmissionpaused())
- [func register(forChannelCloseNotification: Any!, selector: Selector!) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothrfcommchannel/register(forchannelclosenotification:selector:))
- [func sendRemoteLineStatus(BluetoothRFCOMMLineStatus) -> IOReturn](/documentation/iobluetooth/iobluetoothrfcommchannel/sendremotelinestatus(_:))
- [func setDelegate(Any!) -> IOReturn](/documentation/iobluetooth/iobluetoothrfcommchannel/setdelegate(_:))
- [func setSerialParameters(UInt32, dataBits: UInt8, parity: BluetoothRFCOMMParityType, stopBits: UInt8) -> IOReturn](/documentation/iobluetooth/iobluetoothrfcommchannel/setserialparameters(_:databits:parity:stopbits:))
- [func writeAsync(UnsafeMutableRawPointer!, length: UInt16, refcon: UnsafeMutableRawPointer!) -> IOReturn](/documentation/iobluetooth/iobluetoothrfcommchannel/writeasync(_:length:refcon:))
- [func writeSync(UnsafeMutableRawPointer!, length: UInt16) -> IOReturn](/documentation/iobluetooth/iobluetoothrfcommchannel/writesync(_:length:))

### Type Methods

- [class func register(forChannelOpenNotifications: Any!, selector: Selector!) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothrfcommchannel/register(forchannelopennotifications:selector:))
- [class func register(forChannelOpenNotifications: Any!, selector: Selector!, withChannelID: BluetoothRFCOMMChannelID, direction: IOBluetoothUserNotificationChannelDirection) -> IOBluetoothUserNotification!](/documentation/iobluetooth/iobluetoothrfcommchannel/register(forchannelopennotifications:selector:withchannelid:direction:))
- [class func withObjectID(IOBluetoothObjectID) -> Self!](/documentation/iobluetooth/iobluetoothrfcommchannel/withobjectid(_:))
- [class func withRFCOMMChannelRef(IOBluetoothRFCOMMChannelRef!) -> Self!](/documentation/iobluetooth/iobluetoothrfcommchannel/withrfcommchannelref(_:))
- [IOBluetoothRFCOMMChannelRef](/documentation/iobluetooth/iobluetoothrfcommchannelref)
- [IOBluetoothSDPDataElement](/documentation/iobluetooth/iobluetoothsdpdataelement)

### Initializers

- [init!(elementValue: NSObject!)](/documentation/iobluetooth/iobluetoothsdpdataelement/init(elementvalue:))
- [init!(type: BluetoothSDPDataElementTypeDescriptor, sizeDescriptor: BluetoothSDPDataElementSizeDescriptor, size: UInt32, value: NSObject!)](/documentation/iobluetooth/iobluetoothsdpdataelement/init(type:sizedescriptor:size:value:))

### Instance Methods

- [func contains(IOBluetoothSDPDataElement!) -> Bool](/documentation/iobluetooth/iobluetoothsdpdataelement/contains(_:))
- [func containsValue(NSObject!) -> Bool](/documentation/iobluetooth/iobluetoothsdpdataelement/containsvalue(_:))
- [func getArrayValue() -> [Any]!](/documentation/iobluetooth/iobluetoothsdpdataelement/getarrayvalue())
- [func getDataValue() -> Data!](/documentation/iobluetooth/iobluetoothsdpdataelement/getdatavalue())
- [func getNumberValue() -> NSNumber!](/documentation/iobluetooth/iobluetoothsdpdataelement/getnumbervalue())
- [func getRef() -> Unmanaged<IOBluetoothSDPDataElementRef>!](/documentation/iobluetooth/iobluetoothsdpdataelement/getref())
- [func getSize() -> UInt32](/documentation/iobluetooth/iobluetoothsdpdataelement/getsize())
- [func getSizeDescriptor() -> BluetoothSDPDataElementSizeDescriptor](/documentation/iobluetooth/iobluetoothsdpdataelement/getsizedescriptor())
- [func getStringValue() -> String!](/documentation/iobluetooth/iobluetoothsdpdataelement/getstringvalue())
- [func getTypeDescriptor() -> BluetoothSDPDataElementTypeDescriptor](/documentation/iobluetooth/iobluetoothsdpdataelement/gettypedescriptor())
- [func getUUIDValue() -> IOBluetoothSDPUUID!](/documentation/iobluetooth/iobluetoothsdpdataelement/getuuidvalue())
- [func getValue() -> NSObject!](/documentation/iobluetooth/iobluetoothsdpdataelement/getvalue())

### Type Methods

- [class func withElementValue(NSObject!) -> Self!](/documentation/iobluetooth/iobluetoothsdpdataelement/withelementvalue(_:))
- [class func withSDPDataElementRef(IOBluetoothSDPDataElementRef!) -> Self!](/documentation/iobluetooth/iobluetoothsdpdataelement/withsdpdataelementref(_:))
- [class func withType(BluetoothSDPDataElementTypeDescriptor, sizeDescriptor: BluetoothSDPDataElementSizeDescriptor, size: UInt32, value: NSObject!) -> Self!](/documentation/iobluetooth/iobluetoothsdpdataelement/withtype(_:sizedescriptor:size:value:))
- [IOBluetoothSDPDataElementRef](/documentation/iobluetooth/iobluetoothsdpdataelementref)
- [IOBluetoothSDPServiceAttribute](/documentation/iobluetooth/iobluetoothsdpserviceattribute)

### Initializers

- [init!(id: BluetoothSDPServiceAttributeID, attributeElement: IOBluetoothSDPDataElement!)](/documentation/iobluetooth/iobluetoothsdpserviceattribute/init(id:attributeelement:))
- [init!(id: BluetoothSDPServiceAttributeID, attributeElementValue: NSObject!)](/documentation/iobluetooth/iobluetoothsdpserviceattribute/init(id:attributeelementvalue:))

### Instance Methods

- [func getDataElement() -> IOBluetoothSDPDataElement!](/documentation/iobluetooth/iobluetoothsdpserviceattribute/getdataelement())
- [func getID() -> BluetoothSDPServiceAttributeID](/documentation/iobluetooth/iobluetoothsdpserviceattribute/getid())
- [func getIDDataElement() -> IOBluetoothSDPDataElement!](/documentation/iobluetooth/iobluetoothsdpserviceattribute/getiddataelement())

### Type Methods

- [class func withID(BluetoothSDPServiceAttributeID, attributeElement: IOBluetoothSDPDataElement!) -> Self!](/documentation/iobluetooth/iobluetoothsdpserviceattribute/withid(_:attributeelement:))
- [class func withID(BluetoothSDPServiceAttributeID, attributeElementValue: NSObject!) -> Self!](/documentation/iobluetooth/iobluetoothsdpserviceattribute/withid(_:attributeelementvalue:))
- [IOBluetoothSDPServiceRecord](/documentation/iobluetooth/iobluetoothsdpservicerecord)

### Initializers

- [init!(serviceDictionary: [AnyHashable : Any]!, device: IOBluetoothDevice!)](/documentation/iobluetooth/iobluetoothsdpservicerecord/init(servicedictionary:device:))

### Instance Properties

- [var attributes: [AnyHashable : Any]!](/documentation/iobluetooth/iobluetoothsdpservicerecord/attributes)
- [var device: IOBluetoothDevice!](/documentation/iobluetooth/iobluetoothsdpservicerecord/device)
- [var sortedAttributes: [Any]!](/documentation/iobluetooth/iobluetoothsdpservicerecord/sortedattributes-swift.property)

### Instance Methods

- [func getAttributeDataElement(BluetoothSDPServiceAttributeID) -> IOBluetoothSDPDataElement!](/documentation/iobluetooth/iobluetoothsdpservicerecord/getattributedataelement(_:))
- [func getHandle(UnsafeMutablePointer<BluetoothSDPServiceRecordHandle>!) -> IOReturn](/documentation/iobluetooth/iobluetoothsdpservicerecord/gethandle(_:))
- [func getL2CAPPSM(UnsafeMutablePointer<BluetoothL2CAPPSM>!) -> IOReturn](/documentation/iobluetooth/iobluetoothsdpservicerecord/getl2cappsm(_:))
- [func getRFCOMMChannelID(UnsafeMutablePointer<BluetoothRFCOMMChannelID>!) -> IOReturn](/documentation/iobluetooth/iobluetoothsdpservicerecord/getrfcommchannelid(_:))
- [func getRef() -> Unmanaged<IOBluetoothSDPServiceRecordRef>!](/documentation/iobluetooth/iobluetoothsdpservicerecord/getref())
- [func getServiceName() -> String!](/documentation/iobluetooth/iobluetoothsdpservicerecord/getservicename())
- [func handsFreeSupportedFeatures() -> UInt16](/documentation/iobluetooth/iobluetoothsdpservicerecord/handsfreesupportedfeatures())
- [func hasService(from: [Any]!) -> Bool](/documentation/iobluetooth/iobluetoothsdpservicerecord/hasservice(from:))
- [func matchesSearch([Any]!) -> Bool](/documentation/iobluetooth/iobluetoothsdpservicerecord/matchessearch(_:))
- [func matchesUUID16(BluetoothSDPUUID16) -> Bool](/documentation/iobluetooth/iobluetoothsdpservicerecord/matchesuuid16(_:))
- [func matchesUUIDArray([Any]!) -> Bool](/documentation/iobluetooth/iobluetoothsdpservicerecord/matchesuuidarray(_:))
- [func remove() -> IOReturn](/documentation/iobluetooth/iobluetoothsdpservicerecord/remove())

### Type Methods

- [class func publishedServiceRecord(with: [AnyHashable : Any]!) -> Self!](/documentation/iobluetooth/iobluetoothsdpservicerecord/publishedservicerecord(with:))
- [class func withSDPServiceRecordRef(IOBluetoothSDPServiceRecordRef!) -> Self!](/documentation/iobluetooth/iobluetoothsdpservicerecord/withsdpservicerecordref(_:))
- [class func withServiceDictionary([AnyHashable : Any]!, device: IOBluetoothDevice!) -> Self!](/documentation/iobluetooth/iobluetoothsdpservicerecord/withservicedictionary(_:device:))
- [IOBluetoothSDPServiceRecordRef](/documentation/iobluetooth/iobluetoothsdpservicerecordref)
- [IOBluetoothSDPUUID](/documentation/iobluetooth/iobluetoothsdpuuid)

### Initializers

- [convenience init!(bytes: UnsafeRawPointer!, length: UInt32)](/documentation/iobluetooth/iobluetoothsdpuuid/init(bytes:length:))
- [convenience init!(data: Data!)](/documentation/iobluetooth/iobluetoothsdpuuid/init(data:))
- [init!(uuid16: BluetoothSDPUUID16)](/documentation/iobluetooth/iobluetoothsdpuuid/init(uuid16:))
- [init!(uuid32: BluetoothSDPUUID32)](/documentation/iobluetooth/iobluetoothsdpuuid/init(uuid32:))

### Instance Methods

- [func classForArchiver() -> AnyClass!](/documentation/iobluetooth/iobluetoothsdpuuid/classforarchiver())
- [func classForCoder() -> AnyClass!](/documentation/iobluetooth/iobluetoothsdpuuid/classforcoder())
- [func classForPortCoder() -> AnyClass!](/documentation/iobluetooth/iobluetoothsdpuuid/classforportcoder())
- [func getWithLength(UInt32) -> Self!](/documentation/iobluetooth/iobluetoothsdpuuid/getwithlength(_:))
- [func isEqual(to: IOBluetoothSDPUUID!) -> Bool](/documentation/iobluetooth/iobluetoothsdpuuid/isequal(to:))

### Type Methods

- [class func uuid16(BluetoothSDPUUID16) -> Self!](/documentation/iobluetooth/iobluetoothsdpuuid/uuid16(_:))
- [class func uuid32(BluetoothSDPUUID32) -> Self!](/documentation/iobluetooth/iobluetoothsdpuuid/uuid32(_:))
- [IOBluetoothSDPUUIDRef](/documentation/iobluetooth/iobluetoothsdpuuidref)
- [IOBluetoothUserNotification](/documentation/iobluetooth/iobluetoothusernotification)

### Instance Methods

- [func unregister()](/documentation/iobluetooth/iobluetoothusernotification/unregister())
- [IOBluetoothUserNotificationRef](/documentation/iobluetooth/iobluetoothusernotificationref)
- [OBEXFileTransferServices](/documentation/iobluetooth/obexfiletransferservices)

### Initializers

- [init!(obexSession: IOBluetoothOBEXSession!)](/documentation/iobluetooth/obexfiletransferservices/init(obexsession:))

### Instance Properties

- [var delegate: AnyObject!](/documentation/iobluetooth/obexfiletransferservices/delegate)

### Instance Methods

- [func abort() -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/abort())
- [func changeCurrentFolderBackward() -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/changecurrentfolderbackward())
- [func changeCurrentFolderForward(toPath: String!) -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/changecurrentfolderforward(topath:))
- [func changeCurrentFolderToRoot() -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/changecurrentfoldertoroot())
- [func connectToFTPService() -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/connecttoftpservice())
- [func connectToObjectPushService() -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/connecttoobjectpushservice())
- [func copyRemoteFile(String!, toLocalPath: String!) -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/copyremotefile(_:tolocalpath:))
- [func createFolder(String!) -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/createfolder(_:))
- [func currentPath() -> String!](/documentation/iobluetooth/obexfiletransferservices/currentpath())
- [func disconnect() -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/disconnect())
- [func getDefaultVCard(String!) -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/getdefaultvcard(_:))
- [func isBusy() -> Bool](/documentation/iobluetooth/obexfiletransferservices/isbusy())
- [func isConnected() -> Bool](/documentation/iobluetooth/obexfiletransferservices/isconnected())
- [func removeItem(String!) -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/removeitem(_:))
- [func retrieveFolderListing() -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/retrievefolderlisting())
- [func send(Data!, type: String!, name: String!) -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/send(_:type:name:))
- [func sendFile(String!) -> OBEXError](/documentation/iobluetooth/obexfiletransferservices/sendfile(_:))

### Type Methods

- [class func withOBEXSession(IOBluetoothOBEXSession!) -> Self!](/documentation/iobluetooth/obexfiletransferservices/withobexsession(_:))
- [OBEXSession](/documentation/iobluetooth/obexsession)

### DataTypes

- [OBEXTransportEvent](/documentation/iobluetooth/obextransportevent)

#### Initializers

- [init()](/documentation/iobluetooth/obextransportevent/init())
- [init(type: OBEXTransportEventType, status: OBEXError, dataPtr: UnsafeMutableRawPointer!, dataLength: Int)](/documentation/iobluetooth/obextransportevent/init(type:status:dataptr:datalength:))

#### Instance Properties

- [var dataLength: Int](/documentation/iobluetooth/obextransportevent/datalength)
- [var dataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obextransportevent/dataptr)
- [var status: OBEXError](/documentation/iobluetooth/obextransportevent/status)
- [var type: OBEXTransportEventType](/documentation/iobluetooth/obextransportevent/type)
- [OBEXTransportEventType](/documentation/iobluetooth/obextransporteventtype)

### Instance Methods

- [func clientHandleIncomingData(UnsafeMutablePointer<OBEXTransportEvent>!)](/documentation/iobluetooth/obexsession/clienthandleincomingdata(_:))
- [func closeTransportConnection() -> OBEXError](/documentation/iobluetooth/obexsession/closetransportconnection())
- [func getAvailableCommandPayloadLength(OBEXOpCode) -> OBEXMaxPacketLength](/documentation/iobluetooth/obexsession/getavailablecommandpayloadlength(_:))
- [func getAvailableCommandResponsePayloadLength(OBEXOpCode) -> OBEXMaxPacketLength](/documentation/iobluetooth/obexsession/getavailablecommandresponsepayloadlength(_:))
- [func getMaxPacketLength() -> OBEXMaxPacketLength](/documentation/iobluetooth/obexsession/getmaxpacketlength())
- [func hasOpenOBEXConnection() -> Bool](/documentation/iobluetooth/obexsession/hasopenobexconnection())
- [func hasOpenTransportConnection() -> Bool](/documentation/iobluetooth/obexsession/hasopentransportconnection())
- [func obexAbort(UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexabort(_:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexAbortResponse(OBEXOpCode, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexabortresponse(_:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexConnect(OBEXFlags, maxPacketLength: OBEXMaxPacketLength, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexconnect(_:maxpacketlength:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexConnectResponse(OBEXOpCode, flags: OBEXFlags, maxPacketLength: OBEXMaxPacketLength, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexconnectresponse(_:flags:maxpacketlength:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexDisconnect(UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexdisconnect(_:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexDisconnectResponse(OBEXOpCode, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexdisconnectresponse(_:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexGet(Bool, headers: UnsafeMutableRawPointer!, headersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexget(_:headers:headerslength:eventselector:selectortarget:refcon:))
- [func obexGetResponse(OBEXOpCode, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexgetresponse(_:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexPut(Bool, headersData: UnsafeMutableRawPointer!, headersDataLength: Int, bodyData: UnsafeMutableRawPointer!, bodyDataLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexput(_:headersdata:headersdatalength:bodydata:bodydatalength:eventselector:selectortarget:refcon:))
- [func obexPutResponse(OBEXOpCode, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexputresponse(_:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexSetPath(OBEXFlags, constants: OBEXConstants, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexsetpath(_:constants:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func obexSetPathResponse(OBEXOpCode, optionalHeaders: UnsafeMutableRawPointer!, optionalHeadersLength: Int, eventSelector: Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/obexsetpathresponse(_:optionalheaders:optionalheaderslength:eventselector:selectortarget:refcon:))
- [func openTransportConnection(Selector!, selectorTarget: Any!, refCon: UnsafeMutableRawPointer!) -> OBEXError](/documentation/iobluetooth/obexsession/opentransportconnection(_:selectortarget:refcon:))
- [func sendData(toTransport: UnsafeMutableRawPointer!, dataLength: Int) -> OBEXError](/documentation/iobluetooth/obexsession/senddata(totransport:datalength:))
- [func serverHandleIncomingData(UnsafeMutablePointer<OBEXTransportEvent>!)](/documentation/iobluetooth/obexsession/serverhandleincomingdata(_:))
- [func setEventCallback(OBEXSessionEventCallback!)](/documentation/iobluetooth/obexsession/seteventcallback(_:))
- [func setEventRefCon(UnsafeMutableRawPointer!)](/documentation/iobluetooth/obexsession/seteventrefcon(_:))
- [func setEventSelector(Selector!, target: Any!, refCon: UnsafeMutableRawPointer!)](/documentation/iobluetooth/obexsession/seteventselector(_:target:refcon:))

## Protocols

- [IOBluetoothDeviceAsyncCallbacks](/documentation/iobluetooth/iobluetoothdeviceasynccallbacks)

### Instance Methods

- [func connectionComplete(IOBluetoothDevice!, status: IOReturn)](/documentation/iobluetooth/iobluetoothdeviceasynccallbacks/connectioncomplete(_:status:))
- [func remoteNameRequestComplete(IOBluetoothDevice!, status: IOReturn)](/documentation/iobluetooth/iobluetoothdeviceasynccallbacks/remotenamerequestcomplete(_:status:))
- [func sdpQueryComplete(IOBluetoothDevice!, status: IOReturn)](/documentation/iobluetooth/iobluetoothdeviceasynccallbacks/sdpquerycomplete(_:status:))
- [IOBluetoothDeviceInquiryDelegate](/documentation/iobluetooth/iobluetoothdeviceinquirydelegate)

### Instance Methods

- [func deviceInquiryComplete(IOBluetoothDeviceInquiry!, error: IOReturn, aborted: Bool)](/documentation/iobluetooth/iobluetoothdeviceinquirydelegate/deviceinquirycomplete(_:error:aborted:))
- [func deviceInquiryDeviceFound(IOBluetoothDeviceInquiry!, device: IOBluetoothDevice!)](/documentation/iobluetooth/iobluetoothdeviceinquirydelegate/deviceinquirydevicefound(_:device:))
- [func deviceInquiryDeviceNameUpdated(IOBluetoothDeviceInquiry!, device: IOBluetoothDevice!, devicesRemaining: UInt32)](/documentation/iobluetooth/iobluetoothdeviceinquirydelegate/deviceinquirydevicenameupdated(_:device:devicesremaining:))
- [func deviceInquiryStarted(IOBluetoothDeviceInquiry!)](/documentation/iobluetooth/iobluetoothdeviceinquirydelegate/deviceinquirystarted(_:))
- [func deviceInquiryUpdatingDeviceNamesStarted(IOBluetoothDeviceInquiry!, devicesRemaining: UInt32)](/documentation/iobluetooth/iobluetoothdeviceinquirydelegate/deviceinquiryupdatingdevicenamesstarted(_:devicesremaining:))
- [IOBluetoothDevicePairDelegate](/documentation/iobluetooth/iobluetoothdevicepairdelegate)

### Instance Methods

- [func devicePairingConnected(Any!)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicepairingconnected(_:))
- [func devicePairingConnecting(Any!)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicepairingconnecting(_:))
- [func devicePairingFinished(Any!, error: IOReturn)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicepairingfinished(_:error:))
- [func devicePairingPINCodeRequest(Any!)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicepairingpincoderequest(_:))
- [func devicePairingStarted(Any!)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicepairingstarted(_:))
- [func devicePairingUserConfirmationRequest(Any!, numericValue: BluetoothNumericValue)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicepairinguserconfirmationrequest(_:numericvalue:))
- [func devicePairingUserPasskeyNotification(Any!, passkey: BluetoothPasskey)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicepairinguserpasskeynotification(_:passkey:))
- [func deviceSimplePairingComplete(Any!, status: BluetoothHCIEventStatus)](/documentation/iobluetooth/iobluetoothdevicepairdelegate/devicesimplepairingcomplete(_:status:))
- [IOBluetoothHandsFreeAudioGatewayDelegate](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewaydelegate)

### Receiving Status Change Information

- [func handsFree(IOBluetoothHandsFreeAudioGateway!, hangup: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewaydelegate/handsfree(_:hangup:))
- [func handsFree(IOBluetoothHandsFreeAudioGateway!, redial: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewaydelegate/handsfree(_:redial:))
- [IOBluetoothHandsFreeDelegate](/documentation/iobluetooth/iobluetoothhandsfreedelegate)

### Instance Methods

- [func handsFree(IOBluetoothHandsFree!, connected: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedelegate/handsfree(_:connected:))
- [func handsFree(IOBluetoothHandsFree!, disconnected: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedelegate/handsfree(_:disconnected:))
- [func handsFree(IOBluetoothHandsFree!, scoConnectionClosed: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedelegate/handsfree(_:scoconnectionclosed:))
- [func handsFree(IOBluetoothHandsFree!, scoConnectionOpened: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedelegate/handsfree(_:scoconnectionopened:))
- [IOBluetoothHandsFreeDeviceDelegate](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate)

### Receiving Status Indicator Changes

- [func handsFree(IOBluetoothHandsFreeDevice!, callSetupMode: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:callsetupmode:))
- [func handsFree(IOBluetoothHandsFreeDevice!, isCallActive: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:iscallactive:))
- [func handsFree(IOBluetoothHandsFreeDevice!, isServiceAvailable: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:isserviceavailable:))
- [func handsFree(IOBluetoothHandsFreeDevice!, signalStrength: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:signalstrength:))
- [func handsFree(IOBluetoothHandsFreeDevice!, callHoldState: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:callholdstate:))
- [func handsFree(IOBluetoothHandsFreeDevice!, isRoaming: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:isroaming:))
- [func handsFree(IOBluetoothHandsFreeDevice!, batteryCharge: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:batterycharge:))

### Receiving Call Status

- [func handsFree(IOBluetoothHandsFreeDevice!, incomingCallFrom: String!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:incomingcallfrom:))
- [func handsFree(IOBluetoothHandsFreeDevice!, currentCall: [AnyHashable : Any]!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:currentcall:))
- [Current Call Information Constants](/documentation/iobluetooth/current-call-information-constants)

#### Call Information

- [let IOBluetoothHandsFreeCallDirection: String](/documentation/iobluetooth/iobluetoothhandsfreecalldirection)
- [let IOBluetoothHandsFreeCallIndex: String](/documentation/iobluetooth/iobluetoothhandsfreecallindex)
- [let IOBluetoothHandsFreeCallMode: String](/documentation/iobluetooth/iobluetoothhandsfreecallmode)
- [let IOBluetoothHandsFreeCallMultiparty: String](/documentation/iobluetooth/iobluetoothhandsfreecallmultiparty)
- [let IOBluetoothHandsFreeCallStatus: String](/documentation/iobluetooth/iobluetoothhandsfreecallstatus)

#### Remote Number Information

- [let IOBluetoothHandsFreeCallNumber: String](/documentation/iobluetooth/iobluetoothhandsfreecallnumber)
- [let IOBluetoothHandsFreeCallType: String](/documentation/iobluetooth/iobluetoothhandsfreecalltype)
- [let IOBluetoothHandsFreeCallName: String](/documentation/iobluetooth/iobluetoothhandsfreecallname)

### Receiving SMS Information

- [func handsFree(IOBluetoothHandsFreeDevice!, incomingSMS: [AnyHashable : Any]!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:incomingsms:))
- [SMS Dictionary Key Constants](/documentation/iobluetooth/sms-dictionary-key-constants)

#### Sender Information

- [let IOBluetoothPDUOriginatingAddress: String](/documentation/iobluetooth/iobluetoothpduoriginatingaddress)
- [let IOBluetoothPDUOriginatingAddressType: String](/documentation/iobluetooth/iobluetoothpduoriginatingaddresstype)
- [let IOBluetoothPDUServicCenterAddress: String](/documentation/iobluetooth/iobluetoothpduserviccenteraddress)
- [let IOBluetoothPDUServiceCenterAddressType: String](/documentation/iobluetooth/iobluetoothpduservicecenteraddresstype)

#### Message Information

- [let IOBluetoothPDUProtocolID: String](/documentation/iobluetooth/iobluetoothpduprotocolid)
- [let IOBluetoothPDUUserData: String](/documentation/iobluetooth/iobluetoothpduuserdata)
- [let IOBluetoothPDUTimestamp: String](/documentation/iobluetooth/iobluetoothpdutimestamp)
- [let IOBluetoothPDUType: String](/documentation/iobluetooth/iobluetoothpdutype)
- [let IOBluetoothPDUEncoding: String](/documentation/iobluetooth/iobluetoothpduencoding)

### Receiving Other Information

- [func handsFree(IOBluetoothHandsFreeDevice!, subscriberNumber: String!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:subscribernumber:))
- [func handsFree(IOBluetoothHandsFreeDevice!, ringAttempt: NSNumber!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:ringattempt:))
- [func handsFree(IOBluetoothHandsFreeDevice!, unhandledResultCode: String!)](/documentation/iobluetooth/iobluetoothhandsfreedevicedelegate/handsfree(_:unhandledresultcode:))
- [IOBluetoothL2CAPChannelDelegate](/documentation/iobluetooth/iobluetoothl2capchanneldelegate)

### Instance Methods

- [func l2capChannelClosed(IOBluetoothL2CAPChannel!)](/documentation/iobluetooth/iobluetoothl2capchanneldelegate/l2capchannelclosed(_:))
- [func l2capChannelData(IOBluetoothL2CAPChannel!, data: UnsafeMutableRawPointer!, length: Int)](/documentation/iobluetooth/iobluetoothl2capchanneldelegate/l2capchanneldata(_:data:length:))
- [func l2capChannelOpenComplete(IOBluetoothL2CAPChannel!, status: IOReturn)](/documentation/iobluetooth/iobluetoothl2capchanneldelegate/l2capchannelopencomplete(_:status:))
- [func l2capChannelQueueSpaceAvailable(IOBluetoothL2CAPChannel!)](/documentation/iobluetooth/iobluetoothl2capchanneldelegate/l2capchannelqueuespaceavailable(_:))
- [func l2capChannelReconfigured(IOBluetoothL2CAPChannel!)](/documentation/iobluetooth/iobluetoothl2capchanneldelegate/l2capchannelreconfigured(_:))
- [func l2capChannelWriteComplete(IOBluetoothL2CAPChannel!, refcon: UnsafeMutableRawPointer!, status: IOReturn)](/documentation/iobluetooth/iobluetoothl2capchanneldelegate/l2capchannelwritecomplete(_:refcon:status:))
- [IOBluetoothRFCOMMChannelDelegate](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate)

### Instance Methods

- [func rfcommChannelClosed(IOBluetoothRFCOMMChannel!)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchannelclosed(_:))
- [func rfcommChannelControlSignalsChanged(IOBluetoothRFCOMMChannel!)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchannelcontrolsignalschanged(_:))
- [func rfcommChannelData(IOBluetoothRFCOMMChannel!, data: UnsafeMutableRawPointer!, length: Int)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchanneldata(_:data:length:))
- [func rfcommChannelFlowControlChanged(IOBluetoothRFCOMMChannel!)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchannelflowcontrolchanged(_:))
- [func rfcommChannelOpenComplete(IOBluetoothRFCOMMChannel!, status: IOReturn)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchannelopencomplete(_:status:))
- [func rfcommChannelQueueSpaceAvailable(IOBluetoothRFCOMMChannel!)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchannelqueuespaceavailable(_:))
- [func rfcommChannelWriteComplete(IOBluetoothRFCOMMChannel!, refcon: UnsafeMutableRawPointer!, status: IOReturn)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchannelwritecomplete(_:refcon:status:))
- [func rfcommChannelWriteComplete(IOBluetoothRFCOMMChannel!, refcon: UnsafeMutableRawPointer!, status: IOReturn, bytesWritten: Int)](/documentation/iobluetooth/iobluetoothrfcommchanneldelegate/rfcommchannelwritecomplete(_:refcon:status:byteswritten:))

## Reference

- [Bluetooth.h User-Space](/documentation/iobluetooth/bluetooth-h-user-space)

### Constants

- [BluetoothHCIUSBDeviceMatchingConstants](/documentation/iobluetooth/bluetoothhciusbdevicematchingconstants-8yru7)

#### Constants

- [var kBluetoothHCITransportUSBClassCode: Int](/documentation/iobluetooth/kbluetoothhcitransportusbclasscode)
- [var kBluetoothHCITransportUSBProtocolCode: Int](/documentation/iobluetooth/kbluetoothhcitransportusbprotocolcode)
- [var kBluetoothHCITransportUSBSubClassCode: Int](/documentation/iobluetooth/kbluetoothhcitransportusbsubclasscode)
- [IOBluetoothUserLib.h](/documentation/iobluetooth/iobluetoothuserlib-h)

### Miscellaneous

- [func IOBluetoothIgnoreHIDDevice(IOBluetoothDeviceRef!)](/documentation/iobluetooth/iobluetoothignorehiddevice(_:))
- [func IOBluetoothL2CAPChannelRegisterForChannelCloseNotification(IOBluetoothL2CAPChannelRef!, IOBluetoothUserNotificationCallback!, UnsafeMutableRawPointer!) -> Unmanaged<IOBluetoothUserNotificationRef>!](/documentation/iobluetooth/iobluetoothl2capchannelregisterforchannelclosenotification(_:_:_:))
- [func IOBluetoothRemoveIgnoredHIDDevice(IOBluetoothDeviceRef!)](/documentation/iobluetooth/iobluetoothremoveignoredhiddevice(_:))
- [func IOBluetoothUserNotificationUnregister(IOBluetoothUserNotificationRef!)](/documentation/iobluetooth/iobluetoothusernotificationunregister(_:))

### Callbacks

- [IOBluetoothUserNotificationCallback](/documentation/iobluetooth/iobluetoothusernotificationcallback)

### Data Types

- [IOBluetoothDeviceSearchOptions](/documentation/iobluetooth/iobluetoothdevicesearchoptions)
- [IOBluetoothDeviceSearchAttributes](/documentation/iobluetooth/iobluetoothdevicesearchattributes)

#### Initializers

- [init()](/documentation/iobluetooth/iobluetoothdevicesearchattributes/init())
- [init(options: IOBluetoothDeviceSearchOptions, maxResults: IOItemCount, deviceAttributeCount: IOItemCount, attributeList: UnsafeMutablePointer<IOBluetoothDeviceSearchDeviceAttributes>!)](/documentation/iobluetooth/iobluetoothdevicesearchattributes/init(options:maxresults:deviceattributecount:attributelist:))

#### Instance Properties

- [var attributeList: UnsafeMutablePointer<IOBluetoothDeviceSearchDeviceAttributes>!](/documentation/iobluetooth/iobluetoothdevicesearchattributes/attributelist)
- [var deviceAttributeCount: IOItemCount](/documentation/iobluetooth/iobluetoothdevicesearchattributes/deviceattributecount)
- [var maxResults: IOItemCount](/documentation/iobluetooth/iobluetoothdevicesearchattributes/maxresults)
- [var options: IOBluetoothDeviceSearchOptions](/documentation/iobluetooth/iobluetoothdevicesearchattributes/options)
- [IOBluetoothDeviceSearchDeviceAttributes](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes)

#### Initializers

- [init()](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/init())
- [init(address: BluetoothDeviceAddress, name: BluetoothDeviceName, serviceClassMajor: BluetoothServiceClassMajor, deviceClassMajor: BluetoothDeviceClassMajor, deviceClassMinor: BluetoothDeviceClassMinor)](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/init(address:name:serviceclassmajor:deviceclassmajor:deviceclassminor:))

#### Instance Properties

- [var address: BluetoothDeviceAddress](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/address)
- [var deviceClassMajor: BluetoothDeviceClassMajor](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/deviceclassmajor)
- [var deviceClassMinor: BluetoothDeviceClassMinor](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/deviceclassminor)
- [var name: BluetoothDeviceName](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/name)
- [var serviceClassMajor: BluetoothServiceClassMajor](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/serviceclassmajor)

### Constants

- [IOBluetoothDeviceSearchDeviceAttributes](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes)

#### Initializers

- [init()](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/init())
- [init(address: BluetoothDeviceAddress, name: BluetoothDeviceName, serviceClassMajor: BluetoothServiceClassMajor, deviceClassMajor: BluetoothDeviceClassMajor, deviceClassMinor: BluetoothDeviceClassMinor)](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/init(address:name:serviceclassmajor:deviceclassmajor:deviceclassminor:))

#### Instance Properties

- [var address: BluetoothDeviceAddress](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/address)
- [var deviceClassMajor: BluetoothDeviceClassMajor](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/deviceclassmajor)
- [var deviceClassMinor: BluetoothDeviceClassMinor](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/deviceclassminor)
- [var name: BluetoothDeviceName](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/name)
- [var serviceClassMajor: BluetoothServiceClassMajor](/documentation/iobluetooth/iobluetoothdevicesearchdeviceattributes/serviceclassmajor)
- [IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits)

#### Constants

- [var kIOBluetoothDeviceSearchClassic: IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/kiobluetoothdevicesearchclassic)
- [var kIOBluetoothDeviceSearchLE: IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/kiobluetoothdevicesearchle)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/rawvalue)
- [IOBluetoothUtilities.h](/documentation/iobluetooth/iobluetoothutilities-h)

### Miscellaneous

- [func IOBluetoothFindNumberOfRegistryEntriesOfClassName(UnsafePointer<CChar>!) -> Int](/documentation/iobluetooth/iobluetoothfindnumberofregistryentriesofclassname(_:))
- [func IOBluetoothGetUniqueFileNameAndPath(String!, String!) -> String!](/documentation/iobluetooth/iobluetoothgetuniquefilenameandpath(_:_:))
- [func IOBluetoothIsFileAppleDesignatedPIMData(String!) -> Bool](/documentation/iobluetooth/iobluetoothisfileappledesignatedpimdata(_:))
- [func IOBluetoothNSStringFromDeviceAddress(UnsafePointer<BluetoothDeviceAddress>!) -> String!](/documentation/iobluetooth/iobluetoothnsstringfromdeviceaddress(_:))
- [func IOBluetoothNSStringToDeviceAddress(String!, UnsafeMutablePointer<BluetoothDeviceAddress>!) -> IOReturn](/documentation/iobluetooth/iobluetoothnsstringtodeviceaddress(_:_:))
- [func IOBluetoothNumberOfAvailableHIDDevices() -> Int](/documentation/iobluetooth/iobluetoothnumberofavailablehiddevices())
- [func IOBluetoothNumberOfKeyboardHIDDevices() -> Int](/documentation/iobluetooth/iobluetoothnumberofkeyboardhiddevices())
- [func IOBluetoothNumberOfPointingHIDDevices() -> Int](/documentation/iobluetooth/iobluetoothnumberofpointinghiddevices())
- [func IOBluetoothNumberOfTabletHIDDevices() -> Int](/documentation/iobluetooth/iobluetoothnumberoftablethiddevices())
- [OBEX.h](/documentation/iobluetooth/obex-h)

### Miscellaneous

- [func OBEXAddApplicationParameterHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddapplicationparameterheader(_:_:_:))
- [func OBEXAddAuthorizationChallengeHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddauthorizationchallengeheader(_:_:_:))
- [func OBEXAddAuthorizationResponseHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddauthorizationresponseheader(_:_:_:))
- [func OBEXAddBodyHeader(UnsafeRawPointer!, UInt32, Bool, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddbodyheader(_:_:_:_:))
- [func OBEXAddByteSequenceHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddbytesequenceheader(_:_:_:))
- [func OBEXAddConnectionIDHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddconnectionidheader(_:_:_:))
- [func OBEXAddCountHeader(UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddcountheader(_:_:))
- [func OBEXAddDescriptionHeader(CFString!, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexadddescriptionheader(_:_:))
- [func OBEXAddHTTPHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddhttpheader(_:_:_:))
- [func OBEXAddLengthHeader(UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddlengthheader(_:_:))
- [func OBEXAddNameHeader(CFString!, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddnameheader(_:_:))
- [func OBEXAddObjectClassHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddobjectclassheader(_:_:_:))
- [func OBEXAddTargetHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddtargetheader(_:_:_:))
- [func OBEXAddTime4ByteHeader(UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddtime4byteheader(_:_:))
- [func OBEXAddTimeISOHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddtimeisoheader(_:_:_:))
- [func OBEXAddTypeHeader(CFString!, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddtypeheader(_:_:))
- [func OBEXAddUserDefinedHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexadduserdefinedheader(_:_:_:))
- [func OBEXAddWhoHeader(UnsafeRawPointer!, UInt32, CFMutableDictionary!) -> OBEXError](/documentation/iobluetooth/obexaddwhoheader(_:_:_:))
- [func OBEXGetHeaders(UnsafeRawPointer!, Int) -> CFDictionary!](/documentation/iobluetooth/obexgetheaders(_:_:))
- [func OBEXHeadersToBytes(CFDictionary!) -> Unmanaged<CFMutableData>!](/documentation/iobluetooth/obexheaderstobytes(_:))

### Data Types

- [OBEXSessionEvent](/documentation/iobluetooth/obexsessionevent)

#### Initializers

- [init()](/documentation/iobluetooth/obexsessionevent/init())
- [init(type: OBEXSessionEventType, session: OBEXSessionRef!, refCon: UnsafeMutableRawPointer!, isEndOfEventData: DarwinBoolean, reserved1: UnsafeMutableRawPointer!, reserved2: UnsafeMutableRawPointer!, u: OBEXSessionEvent.__Unnamed_union_u)](/documentation/iobluetooth/obexsessionevent/init(type:session:refcon:isendofeventdata:reserved1:reserved2:u:))

#### Instance Properties

- [var isEndOfEventData: DarwinBoolean](/documentation/iobluetooth/obexsessionevent/isendofeventdata)
- [var refCon: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexsessionevent/refcon)
- [var reserved1: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexsessionevent/reserved1)
- [var reserved2: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexsessionevent/reserved2)
- [var session: OBEXSessionRef!](/documentation/iobluetooth/obexsessionevent/session)
- [var type: OBEXSessionEventType](/documentation/iobluetooth/obexsessionevent/type)
- [var u: OBEXSessionEvent.__Unnamed_union_u](/documentation/iobluetooth/obexsessionevent/u)
- [OBEXAbortCommandData](/documentation/iobluetooth/obexabortcommanddata)

#### Initializers

- [init()](/documentation/iobluetooth/obexabortcommanddata/init())
- [init(headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int)](/documentation/iobluetooth/obexabortcommanddata/init(headerdataptr:headerdatalength:))

#### Instance Properties

- [var headerDataLength: Int](/documentation/iobluetooth/obexabortcommanddata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexabortcommanddata/headerdataptr)
- [OBEXAbortCommandResponseData](/documentation/iobluetooth/obexabortcommandresponsedata)

#### Initializers

- [init()](/documentation/iobluetooth/obexabortcommandresponsedata/init())
- [init(serverResponseOpCode: OBEXOpCode, headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int)](/documentation/iobluetooth/obexabortcommandresponsedata/init(serverresponseopcode:headerdataptr:headerdatalength:))

#### Instance Properties

- [var headerDataLength: Int](/documentation/iobluetooth/obexabortcommandresponsedata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexabortcommandresponsedata/headerdataptr)
- [var serverResponseOpCode: OBEXOpCode](/documentation/iobluetooth/obexabortcommandresponsedata/serverresponseopcode)
- [OBEXConnectCommandData](/documentation/iobluetooth/obexconnectcommanddata)

#### Initializers

- [init()](/documentation/iobluetooth/obexconnectcommanddata/init())
- [init(headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int, maxPacketSize: OBEXMaxPacketLength, version: OBEXVersion, flags: OBEXFlags)](/documentation/iobluetooth/obexconnectcommanddata/init(headerdataptr:headerdatalength:maxpacketsize:version:flags:))

#### Instance Properties

- [var flags: OBEXFlags](/documentation/iobluetooth/obexconnectcommanddata/flags)
- [var headerDataLength: Int](/documentation/iobluetooth/obexconnectcommanddata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexconnectcommanddata/headerdataptr)
- [var maxPacketSize: OBEXMaxPacketLength](/documentation/iobluetooth/obexconnectcommanddata/maxpacketsize)
- [var version: OBEXVersion](/documentation/iobluetooth/obexconnectcommanddata/version)
- [OBEXConnectCommandResponseData](/documentation/iobluetooth/obexconnectcommandresponsedata)

#### Initializers

- [init()](/documentation/iobluetooth/obexconnectcommandresponsedata/init())
- [init(serverResponseOpCode: OBEXOpCode, headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int, maxPacketSize: OBEXMaxPacketLength, version: OBEXVersion, flags: OBEXFlags)](/documentation/iobluetooth/obexconnectcommandresponsedata/init(serverresponseopcode:headerdataptr:headerdatalength:maxpacketsize:version:flags:))

#### Instance Properties

- [var flags: OBEXFlags](/documentation/iobluetooth/obexconnectcommandresponsedata/flags)
- [var headerDataLength: Int](/documentation/iobluetooth/obexconnectcommandresponsedata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexconnectcommandresponsedata/headerdataptr)
- [var maxPacketSize: OBEXMaxPacketLength](/documentation/iobluetooth/obexconnectcommandresponsedata/maxpacketsize)
- [var serverResponseOpCode: OBEXOpCode](/documentation/iobluetooth/obexconnectcommandresponsedata/serverresponseopcode)
- [var version: OBEXVersion](/documentation/iobluetooth/obexconnectcommandresponsedata/version)
- [OBEXDisconnectCommandData](/documentation/iobluetooth/obexdisconnectcommanddata)

#### Initializers

- [init()](/documentation/iobluetooth/obexdisconnectcommanddata/init())
- [init(headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int)](/documentation/iobluetooth/obexdisconnectcommanddata/init(headerdataptr:headerdatalength:))

#### Instance Properties

- [var headerDataLength: Int](/documentation/iobluetooth/obexdisconnectcommanddata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexdisconnectcommanddata/headerdataptr)
- [OBEXDisconnectCommandResponseData](/documentation/iobluetooth/obexdisconnectcommandresponsedata)

#### Initializers

- [init()](/documentation/iobluetooth/obexdisconnectcommandresponsedata/init())
- [init(serverResponseOpCode: OBEXOpCode, headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int)](/documentation/iobluetooth/obexdisconnectcommandresponsedata/init(serverresponseopcode:headerdataptr:headerdatalength:))

#### Instance Properties

- [var headerDataLength: Int](/documentation/iobluetooth/obexdisconnectcommandresponsedata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexdisconnectcommandresponsedata/headerdataptr)
- [var serverResponseOpCode: OBEXOpCode](/documentation/iobluetooth/obexdisconnectcommandresponsedata/serverresponseopcode)
- [OBEXErrorData](/documentation/iobluetooth/obexerrordata)

#### Initializers

- [init()](/documentation/iobluetooth/obexerrordata/init())
- [init(error: OBEXError, dataPtr: UnsafeMutableRawPointer!, dataLength: Int)](/documentation/iobluetooth/obexerrordata/init(error:dataptr:datalength:))

#### Instance Properties

- [var dataLength: Int](/documentation/iobluetooth/obexerrordata/datalength)
- [var dataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexerrordata/dataptr)
- [var error: OBEXError](/documentation/iobluetooth/obexerrordata/error)
- [OBEXGetCommandData](/documentation/iobluetooth/obexgetcommanddata)

#### Initializers

- [init()](/documentation/iobluetooth/obexgetcommanddata/init())
- [init(headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int)](/documentation/iobluetooth/obexgetcommanddata/init(headerdataptr:headerdatalength:))

#### Instance Properties

- [var headerDataLength: Int](/documentation/iobluetooth/obexgetcommanddata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexgetcommanddata/headerdataptr)
- [OBEXGetCommandResponseData](/documentation/iobluetooth/obexgetcommandresponsedata)

#### Initializers

- [init()](/documentation/iobluetooth/obexgetcommandresponsedata/init())
- [init(serverResponseOpCode: OBEXOpCode, headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int)](/documentation/iobluetooth/obexgetcommandresponsedata/init(serverresponseopcode:headerdataptr:headerdatalength:))

#### Instance Properties

- [var headerDataLength: Int](/documentation/iobluetooth/obexgetcommandresponsedata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexgetcommandresponsedata/headerdataptr)
- [var serverResponseOpCode: OBEXOpCode](/documentation/iobluetooth/obexgetcommandresponsedata/serverresponseopcode)
- [OBEXPutCommandData](/documentation/iobluetooth/obexputcommanddata)

#### Initializers

- [init()](/documentation/iobluetooth/obexputcommanddata/init())
- [init(headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int, bodyDataLeftToSend: Int)](/documentation/iobluetooth/obexputcommanddata/init(headerdataptr:headerdatalength:bodydatalefttosend:))

#### Instance Properties

- [var bodyDataLeftToSend: Int](/documentation/iobluetooth/obexputcommanddata/bodydatalefttosend)
- [var headerDataLength: Int](/documentation/iobluetooth/obexputcommanddata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexputcommanddata/headerdataptr)
- [OBEXPutCommandResponseData](/documentation/iobluetooth/obexputcommandresponsedata)

#### Initializers

- [init()](/documentation/iobluetooth/obexputcommandresponsedata/init())
- [init(serverResponseOpCode: OBEXOpCode, headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int)](/documentation/iobluetooth/obexputcommandresponsedata/init(serverresponseopcode:headerdataptr:headerdatalength:))

#### Instance Properties

- [var headerDataLength: Int](/documentation/iobluetooth/obexputcommandresponsedata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexputcommandresponsedata/headerdataptr)
- [var serverResponseOpCode: OBEXOpCode](/documentation/iobluetooth/obexputcommandresponsedata/serverresponseopcode)
- [OBEXSetPathCommandData](/documentation/iobluetooth/obexsetpathcommanddata)

#### Initializers

- [init()](/documentation/iobluetooth/obexsetpathcommanddata/init())
- [init(headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int, flags: OBEXFlags, constants: OBEXConstants)](/documentation/iobluetooth/obexsetpathcommanddata/init(headerdataptr:headerdatalength:flags:constants:))

#### Instance Properties

- [var constants: OBEXConstants](/documentation/iobluetooth/obexsetpathcommanddata/constants)
- [var flags: OBEXFlags](/documentation/iobluetooth/obexsetpathcommanddata/flags)
- [var headerDataLength: Int](/documentation/iobluetooth/obexsetpathcommanddata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexsetpathcommanddata/headerdataptr)
- [OBEXSetPathCommandResponseData](/documentation/iobluetooth/obexsetpathcommandresponsedata)

#### Initializers

- [init()](/documentation/iobluetooth/obexsetpathcommandresponsedata/init())
- [init(serverResponseOpCode: OBEXOpCode, headerDataPtr: UnsafeMutableRawPointer!, headerDataLength: Int, flags: OBEXFlags, constants: OBEXConstants)](/documentation/iobluetooth/obexsetpathcommandresponsedata/init(serverresponseopcode:headerdataptr:headerdatalength:flags:constants:))

#### Instance Properties

- [var constants: OBEXConstants](/documentation/iobluetooth/obexsetpathcommandresponsedata/constants)
- [var flags: OBEXFlags](/documentation/iobluetooth/obexsetpathcommandresponsedata/flags)
- [var headerDataLength: Int](/documentation/iobluetooth/obexsetpathcommandresponsedata/headerdatalength)
- [var headerDataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obexsetpathcommandresponsedata/headerdataptr)
- [var serverResponseOpCode: OBEXOpCode](/documentation/iobluetooth/obexsetpathcommandresponsedata/serverresponseopcode)

### Constants

- [OBEXConnectFlagValues](/documentation/iobluetooth/obexconnectflagvalues)

#### Constants

- [var kOBEXConnectFlag1Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag1reserved)
- [var kOBEXConnectFlag2Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag2reserved)
- [var kOBEXConnectFlag3Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag3reserved)
- [var kOBEXConnectFlag4Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag4reserved)
- [var kOBEXConnectFlag5Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag5reserved)
- [var kOBEXConnectFlag6Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag6reserved)
- [var kOBEXConnectFlag7Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag7reserved)
- [var kOBEXConnectFlagNone: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflagnone)
- [var kOBEXConnectFlagSupportMultipleItLMPConnections: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflagsupportmultipleitlmpconnections)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexconnectflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexconnectflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexconnectflagvalues/rawvalue)
- [OBEXError](/documentation/iobluetooth/obexerror)

#### Constants

- [var kOBEXErrorRangeMin: OBEXErrorCodes](/documentation/iobluetooth/kobexerrorrangemin)
- [var kOBEXErrorRangeMax: OBEXErrorCodes](/documentation/iobluetooth/kobexerrorrangemax)
- [OBEXHeaderIdentifiers](/documentation/iobluetooth/obexheaderidentifiers)

#### Constants

- [var kOBEXHeaderIDAppParameters: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidappparameters)
- [var kOBEXHeaderIDAuthorizationChallenge: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidauthorizationchallenge)
- [var kOBEXHeaderIDAuthorizationResponse: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidauthorizationresponse)
- [var kOBEXHeaderIDBody: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidbody)
- [var kOBEXHeaderIDConnectionID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidconnectionid)
- [var kOBEXHeaderIDCount: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidcount)
- [var kOBEXHeaderIDDescription: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiddescription)
- [var kOBEXHeaderIDEndOfBody: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidendofbody)
- [var kOBEXHeaderIDHTTP: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidhttp)
- [var kOBEXHeaderIDLength: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidlength)
- [var kOBEXHeaderIDName: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidname)
- [var kOBEXHeaderIDOBEX13CreatorID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13creatorid)
- [var kOBEXHeaderIDOBEX13ObjectClass: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13objectclass)
- [var kOBEXHeaderIDOBEX13SessionParameters: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13sessionparameters)
- [var kOBEXHeaderIDOBEX13SessionSequenceNumber: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13sessionsequencenumber)
- [var kOBEXHeaderIDOBEX13WANUUID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13wanuuid)
- [var kOBEXHeaderIDObjectClass: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobjectclass)
- [var kOBEXHeaderIDReservedRangeEnd: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidreservedrangeend)
- [var kOBEXHeaderIDReservedRangeStart: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidreservedrangestart)
- [var kOBEXHeaderIDTarget: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtarget)
- [var kOBEXHeaderIDTime4Byte: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtime4byte)
- [var kOBEXHeaderIDTimeISO: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtimeiso)
- [var kOBEXHeaderIDType: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtype)
- [var kOBEXHeaderIDUserDefinedRangeEnd: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiduserdefinedrangeend)
- [var kOBEXHeaderIDUserDefinedRangeStart: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiduserdefinedrangestart)
- [var kOBEXHeaderIDWho: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidwho)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexheaderidentifiers/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexheaderidentifiers/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexheaderidentifiers/rawvalue)
- [OBEXNonceFlagValues](/documentation/iobluetooth/obexnonceflagvalues)

#### Constants

- [var kOBEXNonceFlag2Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag2reserved)
- [var kOBEXNonceFlag3Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag3reserved)
- [var kOBEXNonceFlag4Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag4reserved)
- [var kOBEXNonceFlag5Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag5reserved)
- [var kOBEXNonceFlag6Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag6reserved)
- [var kOBEXNonceFlag7Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag7reserved)
- [var kOBEXNonceFlagAccessModeReadOnly: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagaccessmodereadonly)
- [var kOBEXNonceFlagNone: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagnone)
- [var kOBEXNonceFlagSendUserIDInResponse: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagsenduseridinresponse)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexnonceflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexnonceflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexnonceflagvalues/rawvalue)
- [OBEXOpCodeCommandValues](/documentation/iobluetooth/obexopcodecommandvalues)

#### Constants

- [var kOBEXOpCodeAbort: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeabort)
- [var kOBEXOpCodeConnect: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeconnect)
- [var kOBEXOpCodeDisconnect: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodedisconnect)
- [var kOBEXOpCodeGet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeget)
- [var kOBEXOpCodeGetWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodegetwithhighbitset)
- [var kOBEXOpCodePut: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeput)
- [var kOBEXOpCodePutWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeputwithhighbitset)
- [var kOBEXOpCodeReserved: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereserved)
- [var kOBEXOpCodeReservedRangeEnd: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedrangeend)
- [var kOBEXOpCodeReservedRangeStart: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedrangestart)
- [var kOBEXOpCodeReservedWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedwithhighbitset)
- [var kOBEXOpCodeSetPath: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodesetpath)
- [var kOBEXOpCodeUserDefinedEnd: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeuserdefinedend)
- [var kOBEXOpCodeUserDefinedStart: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeuserdefinedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcodecommandvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcodecommandvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcodecommandvalues/rawvalue)
- [OBEXOpCodeResponseValues](/documentation/iobluetooth/obexopcoderesponsevalues)

#### Constants

- [var kOBEXResponseCodeAccepted: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeaccepted)
- [var kOBEXResponseCodeAcceptedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeacceptedwithfinalbit)
- [var kOBEXResponseCodeBadGateway: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadgateway)
- [var kOBEXResponseCodeBadGatewayWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadgatewaywithfinalbit)
- [var kOBEXResponseCodeBadRequest: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadrequest)
- [var kOBEXResponseCodeBadRequestWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadrequestwithfinalbit)
- [var kOBEXResponseCodeConflict: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeconflict)
- [var kOBEXResponseCodeConflictWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeconflictwithfinalbit)
- [var kOBEXResponseCodeContinue: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecontinue)
- [var kOBEXResponseCodeContinueWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecontinuewithfinalbit)
- [var kOBEXResponseCodeCreated: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecreated)
- [var kOBEXResponseCodeCreatedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecreatedwithfinalbit)
- [var kOBEXResponseCodeDatabaseFull: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabasefull)
- [var kOBEXResponseCodeDatabaseFullWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabasefullwithfinalbit)
- [var kOBEXResponseCodeDatabaseLocked: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabaselocked)
- [var kOBEXResponseCodeDatabaseLockedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabaselockedwithfinalbit)
- [var kOBEXResponseCodeForbidden: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeforbidden)
- [var kOBEXResponseCodeForbiddenWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeforbiddenwithfinalbit)
- [var kOBEXResponseCodeGatewayTimeout: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegatewaytimeout)
- [var kOBEXResponseCodeGatewayTimeoutWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegatewaytimeoutwithfinalbit)
- [var kOBEXResponseCodeGone: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegone)
- [var kOBEXResponseCodeGoneWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegonewithfinalbit)
- [var kOBEXResponseCodeHTTPVersionNotSupported: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodehttpversionnotsupported)
- [var kOBEXResponseCodeHTTPVersionNotSupportedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodehttpversionnotsupportedwithfinalbit)
- [var kOBEXResponseCodeInternalServerError: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeinternalservererror)
- [var kOBEXResponseCodeInternalServerErrorWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeinternalservererrorwithfinalbit)
- [var kOBEXResponseCodeLengthRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodelengthrequired)
- [var kOBEXResponseCodeLengthRequiredFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodelengthrequiredfinalbit)
- [var kOBEXResponseCodeMethodNotAllowed: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemethodnotallowed)
- [var kOBEXResponseCodeMethodNotAllowedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemethodnotallowedwithfinalbit)
- [var kOBEXResponseCodeMovedPermanently: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedpermanently)
- [var kOBEXResponseCodeMovedPermanentlyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedpermanentlywithfinalbit)
- [var kOBEXResponseCodeMovedTemporarily: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedtemporarily)
- [var kOBEXResponseCodeMovedTemporarilyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedtemporarilywithfinalbit)
- [var kOBEXResponseCodeMultipleChoices: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemultiplechoices)
- [var kOBEXResponseCodeMultipleChoicesWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemultiplechoiceswithfinalbit)
- [var kOBEXResponseCodeNoContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenocontent)
- [var kOBEXResponseCodeNoContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenocontentwithfinalbit)
- [var kOBEXResponseCodeNonAuthoritativeInfo: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenonauthoritativeinfo)
- [var kOBEXResponseCodeNonAuthoritativeInfoWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenonauthoritativeinfowithfinalbit)
- [var kOBEXResponseCodeNotAcceptable: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotacceptable)
- [var kOBEXResponseCodeNotAcceptableWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotacceptablewithfinalbit)
- [var kOBEXResponseCodeNotFound: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotfound)
- [var kOBEXResponseCodeNotFoundWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotfoundwithfinalbit)
- [var kOBEXResponseCodeNotImplemented: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotimplemented)
- [var kOBEXResponseCodeNotImplementedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotimplementedwithfinalbit)
- [var kOBEXResponseCodeNotModified: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotmodified)
- [var kOBEXResponseCodeNotModifiedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotmodifiedwithfinalbit)
- [var kOBEXResponseCodePartialContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepartialcontent)
- [var kOBEXResponseCodePartialContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepartialcontentwithfinalbit)
- [var kOBEXResponseCodePaymentRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepaymentrequired)
- [var kOBEXResponseCodePaymentRequiredWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepaymentrequiredwithfinalbit)
- [var kOBEXResponseCodePreconditionFailed: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepreconditionfailed)
- [var kOBEXResponseCodePreconditionFailedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepreconditionfailedwithfinalbit)
- [var kOBEXResponseCodeProxyAuthenticationRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeproxyauthenticationrequired)
- [var kOBEXResponseCodeProxyAuthenticationRequiredWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeproxyauthenticationrequiredwithfinalbit)
- [var kOBEXResponseCodeRequestTimeOut: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesttimeout)
- [var kOBEXResponseCodeRequestTimeOutWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesttimeoutwithfinalbit)
- [var kOBEXResponseCodeRequestURLTooLarge: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesturltoolarge)
- [var kOBEXResponseCodeRequestURLTooLargeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesturltoolargewithfinalbit)
- [var kOBEXResponseCodeRequestedEntityTooLarge: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequestedentitytoolarge)
- [var kOBEXResponseCodeRequestedEntityTooLargeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequestedentitytoolargewithfinalbit)
- [var kOBEXResponseCodeReservedRangeEnd: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodereservedrangeend)
- [var kOBEXResponseCodeReservedRangeStart: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodereservedrangestart)
- [var kOBEXResponseCodeResetContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderesetcontent)
- [var kOBEXResponseCodeResetContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderesetcontentwithfinalbit)
- [var kOBEXResponseCodeSeeOther: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeseeother)
- [var kOBEXResponseCodeSeeOtherWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeseeotherwithfinalbit)
- [var kOBEXResponseCodeServiceUnavailable: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeserviceunavailable)
- [var kOBEXResponseCodeServiceUnavailableWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeserviceunavailablewithfinalbit)
- [var kOBEXResponseCodeSuccess: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodesuccess)
- [var kOBEXResponseCodeSuccessWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodesuccesswithfinalbit)
- [var kOBEXResponseCodeUnauthorized: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunauthorized)
- [var kOBEXResponseCodeUnauthorizedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunauthorizedwithfinalbit)
- [var kOBEXResponseCodeUnsupportedMediaType: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunsupportedmediatype)
- [var kOBEXResponseCodeUnsupportedMediaTypeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunsupportedmediatypewithfinalbit)
- [var kOBEXResponseCodeUseProxy: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeuseproxy)
- [var kOBEXResponseCodeUseProxyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeuseproxywithfinalbit)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcoderesponsevalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcoderesponsevalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcoderesponsevalues/rawvalue)
- [OBEXOpCodeSessionValues](/documentation/iobluetooth/obexopcodesessionvalues)

#### Constants

- [var kOBEXOpCodeCloseSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodeclosesession)
- [var kOBEXOpCodeCreateSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodecreatesession)
- [var kOBEXOpCodeResumeSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcoderesumesession)
- [var kOBEXOpCodeSetTimeout: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodesettimeout)
- [var kOBEXOpCodeSuspendSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodesuspendsession)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcodesessionvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcodesessionvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcodesessionvalues/rawvalue)
- [OBEXPutFlagValues](/documentation/iobluetooth/obexputflagvalues)

#### Constants

- [var kOBEXPutFlag2Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag2reserved)
- [var kOBEXPutFlag3Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag3reserved)
- [var kOBEXPutFlag4Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag4reserved)
- [var kOBEXPutFlag5Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag5reserved)
- [var kOBEXPutFlag6Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag6reserved)
- [var kOBEXPutFlag7Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag7reserved)
- [var kOBEXPutFlagDontCreateDirectory: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflagdontcreatedirectory)
- [var kOBEXPutFlagGoToParentDirFirst: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflaggotoparentdirfirst)
- [var kOBEXPutFlagNone: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflagnone)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexputflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexputflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexputflagvalues/rawvalue)
- [OBEXRealmValues](/documentation/iobluetooth/obexrealmvalues)

#### Constants

- [var kOBEXRealmASCII: OBEXRealmValues](/documentation/iobluetooth/kobexrealmascii)
- [var kOBEXRealmISO88591: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88591)
- [var kOBEXRealmISO88592: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88592)
- [var kOBEXRealmISO88593: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88593)
- [var kOBEXRealmISO88594: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88594)
- [var kOBEXRealmISO88595: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88595)
- [var kOBEXRealmISO88596: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88596)
- [var kOBEXRealmISO88597: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88597)
- [var kOBEXRealmISO88598: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88598)
- [var kOBEXRealmISO88599: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88599)
- [var kOBEXRealmUNICODE: OBEXRealmValues](/documentation/iobluetooth/kobexrealmunicode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexrealmvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexrealmvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexrealmvalues/rawvalue)
- [OBEXSessionEventTypes](/documentation/iobluetooth/obexsessioneventtypes)

#### Constants

- [var kOBEXSessionEventTypeAbortCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeabortcommandreceived)
- [var kOBEXSessionEventTypeAbortCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeabortcommandresponsereceived)
- [var kOBEXSessionEventTypeConnectCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeconnectcommandreceived)
- [var kOBEXSessionEventTypeConnectCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeconnectcommandresponsereceived)
- [var kOBEXSessionEventTypeDisconnectCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypedisconnectcommandreceived)
- [var kOBEXSessionEventTypeDisconnectCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypedisconnectcommandresponsereceived)
- [var kOBEXSessionEventTypeError: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeerror)
- [var kOBEXSessionEventTypeGetCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypegetcommandreceived)
- [var kOBEXSessionEventTypeGetCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypegetcommandresponsereceived)
- [var kOBEXSessionEventTypePutCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeputcommandreceived)
- [var kOBEXSessionEventTypePutCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeputcommandresponsereceived)
- [var kOBEXSessionEventTypeSetPathCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypesetpathcommandreceived)
- [var kOBEXSessionEventTypeSetPathCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypesetpathcommandresponsereceived)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexsessioneventtypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexsessioneventtypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexsessioneventtypes/rawvalue)
- [OBEXSessionParameterTags](/documentation/iobluetooth/obexsessionparametertags)

#### Constants

- [var kOBEXSessionParameterTagDeviceAddress: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagdeviceaddress)
- [var kOBEXSessionParameterTagNextSequenceNumber: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagnextsequencenumber)
- [var kOBEXSessionParameterTagNonce: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagnonce)
- [var kOBEXSessionParameterTagSessionID: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagsessionid)
- [var kOBEXSessionParameterTagSessionOpcode: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagsessionopcode)
- [var kOBEXSessionParameterTagTimeout: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagtimeout)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexsessionparametertags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexsessionparametertags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexsessionparametertags/rawvalue)
- [OBEXVersions](/documentation/iobluetooth/obexversions)

#### Constants

- [var kOBEXVersion10: OBEXVersions](/documentation/iobluetooth/kobexversion10)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexversions/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexversions/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexversions/rawvalue)

### Macros

- [OBEX Convenience Macros](/documentation/iobluetooth/obex-convenience-macros)
- [OBEXBluetooth.h](/documentation/iobluetooth/obexbluetooth-h)
- [OBEXFileTransferServices.h](/documentation/iobluetooth/obexfiletransferservices-h)

### Constants

- [Global Variables](/documentation/iobluetooth/global-variables)

#### Constants

- [var kFTSListingNameKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftslistingnamekey)
- [var kFTSListingSizeKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftslistingsizekey)
- [var kFTSListingTypeKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftslistingtypekey)
- [var kFTSProgressBytesTotalKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftsprogressbytestotalkey)
- [var kFTSProgressBytesTransferredKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftsprogressbytestransferredkey)
- [var kFTSProgressEstimatedTimeKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftsprogressestimatedtimekey)
- [var kFTSProgressPercentageKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftsprogresspercentagekey)
- [var kFTSProgressTimeElapsedKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftsprogresstimeelapsedkey)
- [var kFTSProgressTransferRateKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftsprogresstransferratekey)
- [IOBluetooth Structures](/documentation/iobluetooth/iobluetooth-structures)

### Structures

- [BluetoothAFHHostChannelClassification](/documentation/iobluetooth/bluetoothafhhostchannelclassification)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothafhhostchannelclassification/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothafhhostchannelclassification/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothafhhostchannelclassification/data)
- [BluetoothAFHResults](/documentation/iobluetooth/bluetoothafhresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothafhresults/init())
- [init(handle: BluetoothConnectionHandle, mode: BluetoothAFHMode, afhMap: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothafhresults/init(handle:mode:afhmap:))

#### Instance Properties

- [var afhMap: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothafhresults/afhmap)
- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothafhresults/handle)
- [var mode: BluetoothAFHMode](/documentation/iobluetooth/bluetoothafhresults/mode)
- [BluetoothAMPCommandRejectReason](/documentation/iobluetooth/bluetoothampcommandrejectreason)

#### Constants

- [var kBluetoothAMPManagerCommandRejectReasonCommandNotRecognized: BluetoothAMPCommandRejectReason](/documentation/iobluetooth/kbluetoothampmanagercommandrejectreasoncommandnotrecognized)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampcommandrejectreason/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampcommandrejectreason/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampcommandrejectreason/rawvalue)
- [BluetoothAMPCreatePhysicalLinkResponseStatus](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus/rawvalue)
- [BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus)

#### Constants

- [var kBluetoothAMPManagerDisconnectPhysicalLinkResponseInvalidControllerID: BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/kbluetoothampmanagerdisconnectphysicallinkresponseinvalidcontrollerid)
- [var kBluetoothAMPManagerDisconnectPhysicalLinkResponseNoPhysicalLink: BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/kbluetoothampmanagerdisconnectphysicallinkresponsenophysicallink)
- [var kBluetoothAMPManagerDisconnectPhysicalLinkResponseSuccess: BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/kbluetoothampmanagerdisconnectphysicallinkresponsesuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus/rawvalue)
- [BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus)

#### Constants

- [var kBluetoothAMPManagerDiscoverResponseControllerStatusBluetoothOnly: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusbluetoothonly)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusFullCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusfullcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusHighCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatushighcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusLowCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatuslowcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusMediumCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusmediumcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusNoCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusnocapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusPoweredDown: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatuspowereddown)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus/rawvalue)
- [BluetoothAMPGetAssocResponseStatus](/documentation/iobluetooth/bluetoothampgetassocresponsestatus)

#### Constants

- [var kBluetoothAMPManagerGetAssocResponseInvalidControllerID: BluetoothAMPGetAssocResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetassocresponseinvalidcontrollerid)
- [var kBluetoothAMPManagerGetAssocResponseSuccess: BluetoothAMPGetAssocResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetassocresponsesuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampgetassocresponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampgetassocresponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampgetassocresponsestatus/rawvalue)
- [BluetoothAMPGetInfoResponseStatus](/documentation/iobluetooth/bluetoothampgetinforesponsestatus)

#### Constants

- [var kBluetoothAMPManagerGetInfoResponseInvalidControllerID: BluetoothAMPGetInfoResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetinforesponseinvalidcontrollerid)
- [var kBluetoothAMPManagerGetInfoResponseSuccess: BluetoothAMPGetInfoResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetinforesponsesuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampgetinforesponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampgetinforesponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampgetinforesponsestatus/rawvalue)
- [BluetoothAMPManagerCode](/documentation/iobluetooth/bluetoothampmanagercode)

#### Constants

- [var kBluetoothAMPManagerCodeAMPChangeNotify: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampchangenotify)
- [var kBluetoothAMPManagerCodeAMPChangeResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampchangeresponse)
- [var kBluetoothAMPManagerCodeAMPCommandReject: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampcommandreject)
- [var kBluetoothAMPManagerCodeAMPCreatePhysicalLinkRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampcreatephysicallinkrequest)
- [var kBluetoothAMPManagerCodeAMPCreatePhysicalLinkResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampcreatephysicallinkresponse)
- [var kBluetoothAMPManagerCodeAMPDisconnectPhysicalLinkRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdisconnectphysicallinkrequest)
- [var kBluetoothAMPManagerCodeAMPDisconnectPhysicalLinkResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdisconnectphysicallinkresponse)
- [var kBluetoothAMPManagerCodeAMPDiscoverRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdiscoverrequest)
- [var kBluetoothAMPManagerCodeAMPDiscoverResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdiscoverresponse)
- [var kBluetoothAMPManagerCodeAMPGetAssocRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetassocrequest)
- [var kBluetoothAMPManagerCodeAMPGetAssocResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetassocresponse)
- [var kBluetoothAMPManagerCodeAMPGetInfoRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetinforequest)
- [var kBluetoothAMPManagerCodeAMPGetInfoResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetinforesponse)
- [var kBluetoothAMPManagerCodeReserved: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodereserved)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampmanagercode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampmanagercode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampmanagercode/rawvalue)
- [BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues)

#### Constants

- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequired: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequired)
- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequiredDedicatedBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequireddedicatedbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequiredGeneralBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequiredgeneralbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequiredNoBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequirednobonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequired: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequired)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequiredDedicatedBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequireddedicatedbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequiredGeneralBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequiredgeneralbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequiredNoBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequirednobonding)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues/rawvalue)
- [BluetoothCompanyIdentifers](/documentation/iobluetooth/bluetoothcompanyidentifers)

#### Constants

- [var kBluetoothCompanyIdentifer3Com: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer3com)
- [var kBluetoothCompanyIdentifer3DSP: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer3dsp)
- [var kBluetoothCompanyIdentifer3DiJoy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer3dijoy)
- [var kBluetoothCompanyIdentiferAPT: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferapt)
- [var kBluetoothCompanyIdentiferAVMBerlin: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferavmberlin)
- [var kBluetoothCompanyIdentiferAccelSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaccelsemiconductor)
- [var kBluetoothCompanyIdentiferAlcatel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferalcatel)
- [var kBluetoothCompanyIdentiferApple: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferapple)
- [var kBluetoothCompanyIdentiferAtherosCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferatheroscommunications)
- [var kBluetoothCompanyIdentiferAtmel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferatmel)
- [var kBluetoothCompanyIdentiferAvagoTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferavagotechnologies)
- [var kBluetoothCompanyIdentiferBandspeed: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbandspeed)
- [var kBluetoothCompanyIdentiferBluegiga: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbluegiga)
- [var kBluetoothCompanyIdentiferBluetoothSIG: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbluetoothsig)
- [var kBluetoothCompanyIdentiferBroadcom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbroadcom)
- [var kBluetoothCompanyIdentiferCATC: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercatc)
- [var kBluetoothCompanyIdentiferCONWISETechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconwisetechnology)
- [var kBluetoothCompanyIdentiferCTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferctechnologies)
- [var kBluetoothCompanyIdentiferCambridgeSiliconRadio: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercambridgesiliconradio)
- [var kBluetoothCompanyIdentiferCommil: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercommil)
- [var kBluetoothCompanyIdentiferConexantSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconexantsystems)
- [var kBluetoothCompanyIdentiferContinentialAutomotiveSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercontinentialautomotivesystems)
- [var kBluetoothCompanyIdentiferDigianswerAS: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdigiansweras)
- [var kBluetoothCompanyIdentiferEMMicroElectronicMarin: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferemmicroelectronicmarin)
- [var kBluetoothCompanyIdentiferEclipse: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifereclipse)
- [var kBluetoothCompanyIdentiferEricssonTechnologyLicensing: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferericssontechnologylicensing)
- [var kBluetoothCompanyIdentiferFree2Move: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfree2move)
- [var kBluetoothCompanyIdentiferGCTSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergctsemiconductor)
- [var kBluetoothCompanyIdentiferGennum: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergennum)
- [var kBluetoothCompanyIdentiferHarmonInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferharmoninternational)
- [var kBluetoothCompanyIdentiferHitachi: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhitachi)
- [var kBluetoothCompanyIdentiferIBM: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferibm)
- [var kBluetoothCompanyIdentiferIPextreme: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferipextreme)
- [var kBluetoothCompanyIdentiferInfineonTechnologiesAG: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinfineontechnologiesag)
- [var kBluetoothCompanyIdentiferIntegratedSiliconSolution: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferintegratedsiliconsolution)
- [var kBluetoothCompanyIdentiferIntegratedSystemSolution: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferintegratedsystemsolution)
- [var kBluetoothCompanyIdentiferIntel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferintel)
- [var kBluetoothCompanyIdentiferInteropIdentifier: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinteropidentifier)
- [var kBluetoothCompanyIdentiferInventel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinventel)
- [var kBluetoothCompanyIdentiferJandM: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjandm)
- [var kBluetoothCompanyIdentiferKCTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkctechnology)
- [var kBluetoothCompanyIdentiferLucent: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlucent)
- [var kBluetoothCompanyIdentiferMacronixInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermacronixinternational)
- [var kBluetoothCompanyIdentiferMansella: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermansella)
- [var kBluetoothCompanyIdentiferMarvellTechnologyGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermarvelltechnologygroup)
- [var kBluetoothCompanyIdentiferMatsushitaElectricIndustrial: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermatsushitaelectricindustrial)
- [var kBluetoothCompanyIdentiferMediaTek: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermediatek)
- [var kBluetoothCompanyIdentiferMewTelTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermewteltechnology)
- [var kBluetoothCompanyIdentiferMicrosoft: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermicrosoft)
- [var kBluetoothCompanyIdentiferMistubishiElectric: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermistubishielectric)
- [var kBluetoothCompanyIdentiferMitelSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermitelsemiconductor)
- [var kBluetoothCompanyIdentiferMobilian: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermobilian)
- [var kBluetoothCompanyIdentiferMotorola: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermotorola)
- [var kBluetoothCompanyIdentiferNEC: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernec)
- [var kBluetoothCompanyIdentiferNewlogic: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernewlogic)
- [var kBluetoothCompanyIdentiferNokiaMobilePhones: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernokiamobilephones)
- [var kBluetoothCompanyIdentiferNordicSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernordicsemiconductor)
- [var kBluetoothCompanyIdentiferNorwoodSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernorwoodsystems)
- [var kBluetoothCompanyIdentiferOpenInterface: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferopeninterface)
- [var kBluetoothCompanyIdentiferParrotSA: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferparrotsa)
- [var kBluetoothCompanyIdentiferParthusTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferparthustechnologies)
- [var kBluetoothCompanyIdentiferPhilipsSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferphilipssemiconductor)
- [var kBluetoothCompanyIdentiferPlantronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferplantronics)
- [var kBluetoothCompanyIdentiferQualcomm: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcomm)
- [var kBluetoothCompanyIdentiferRFCMicroDevices: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrfcmicrodevices)
- [var kBluetoothCompanyIdentiferRTXTelecom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrtxtelecom)
- [var kBluetoothCompanyIdentiferRedMCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferredmcommunications)
- [var kBluetoothCompanyIdentiferRenesasTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrenesastechnology)
- [var kBluetoothCompanyIdentiferResearchInMotion: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferresearchinmotion)
- [var kBluetoothCompanyIdentiferRohdeandSchwarz: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrohdeandschwarz)
- [var kBluetoothCompanyIdentiferSTMicroelectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstmicroelectronics)
- [var kBluetoothCompanyIdentiferSeikoEpson: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferseikoepson)
- [var kBluetoothCompanyIdentiferSiRFTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersirftechnology)
- [var kBluetoothCompanyIdentiferSigniaTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersigniatechnologies)
- [var kBluetoothCompanyIdentiferSiliconWave: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersiliconwave)
- [var kBluetoothCompanyIdentiferSocketCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersocketcommunications)
- [var kBluetoothCompanyIdentiferSonyEricssonMobileCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersonyericssonmobilecommunications)
- [var kBluetoothCompanyIdentiferStaccatoCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstaccatocommunications)
- [var kBluetoothCompanyIdentiferSymbolTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersymboltechnologies)
- [var kBluetoothCompanyIdentiferSynopsys: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersynopsys)
- [var kBluetoothCompanyIdentiferSystemsAndChips: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersystemsandchips)
- [var kBluetoothCompanyIdentiferTTPCom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferttpcom)
- [var kBluetoothCompanyIdentiferTZeroTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertzerotechnologies)
- [var kBluetoothCompanyIdentiferTenovis: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertenovis)
- [var kBluetoothCompanyIdentiferTerax: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferterax)
- [var kBluetoothCompanyIdentiferTexasInstruments: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertexasinstruments)
- [var kBluetoothCompanyIdentiferToshiba: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertoshiba)
- [var kBluetoothCompanyIdentiferTransilica: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertransilica)
- [var kBluetoothCompanyIdentiferVisio: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervisio)
- [var kBluetoothCompanyIdentiferWavePlusTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwaveplustechnology)
- [var kBluetoothCompanyIdentiferWidcomm: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwidcomm)
- [var kBluetoothCompanyIdentiferZeevo: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzeevo)
- [var kBluetoothCompanyIdentifer9SolutionsOy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer9solutionsoy)
- [var kBluetoothCompanyIdentiferAAMPofAmerica: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaampofamerica)
- [var kBluetoothCompanyIdentiferAAndDEngineering: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaanddengineering)
- [var kBluetoothCompanyIdentiferAAndRCambridge: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaandrcambridge)
- [var kBluetoothCompanyIdentiferACTSTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferactstechnologies)
- [var kBluetoothCompanyIdentiferAMICCOMElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferamiccomelectronics)
- [var kBluetoothCompanyIdentiferARCHOS: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferarchos)
- [var kBluetoothCompanyIdentiferARPDevicesUnlimited: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferarpdevicesunlimited)
- [var kBluetoothCompanyIdentiferAboveAverageOutcomes: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaboveaverageoutcomes)
- [var kBluetoothCompanyIdentiferAceSensor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferacesensor)
- [var kBluetoothCompanyIdentiferAceUni: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaceuni)
- [var kBluetoothCompanyIdentiferAdidas: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferadidas)
- [var kBluetoothCompanyIdentiferAdvancedPANMOBILSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferadvancedpanmobilsystems)
- [var kBluetoothCompanyIdentiferAirohaTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferairohatechnology)
- [var kBluetoothCompanyIdentiferAlpwise: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferalpwise)
- [var kBluetoothCompanyIdentiferAplix: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaplix)
- [var kBluetoothCompanyIdentiferAustcoCommunicationsSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaustcocommunicationssystems)
- [var kBluetoothCompanyIdentiferAutonetMobile: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferautonetmobile)
- [var kBluetoothCompanyIdentiferBDETechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbdetechnology)
- [var kBluetoothCompanyIdentiferBandXIInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbandxiinternational)
- [var kBluetoothCompanyIdentiferBangAndOlufson: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbangandolufson)
- [var kBluetoothCompanyIdentiferBeatsElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbeatselectronics)
- [var kBluetoothCompanyIdentiferBeautifulEnterprise: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbeautifulenterprise)
- [var kBluetoothCompanyIdentiferBekey: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbekey)
- [var kBluetoothCompanyIdentiferBelkinInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbelkininternational)
- [var kBluetoothCompanyIdentiferBinauricSE: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbinauricse)
- [var kBluetoothCompanyIdentiferBioResearchAssociates: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbioresearchassociates)
- [var kBluetoothCompanyIdentiferBiosentronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbiosentronics)
- [var kBluetoothCompanyIdentiferBitsplitters: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbitsplitters)
- [var kBluetoothCompanyIdentiferBlueRadios: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferblueradios)
- [var kBluetoothCompanyIdentiferBose: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbose)
- [var kBluetoothCompanyIdentiferBriarTek: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbriartek)
- [var kBluetoothCompanyIdentiferCaenRFID: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercaenrfid)
- [var kBluetoothCompanyIdentiferCinetix: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercinetix)
- [var kBluetoothCompanyIdentiferClarinoxTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferclarinoxtechnologies)
- [var kBluetoothCompanyIdentiferColorfy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercolorfy)
- [var kBluetoothCompanyIdentiferConnectBlueAB: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconnectblueab)
- [var kBluetoothCompanyIdentiferConnecteDevice: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconnectedevice)
- [var kBluetoothCompanyIdentiferCreativeTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercreativetechnology)
- [var kBluetoothCompanyIdentiferCrystalCode: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercrystalcode)
- [var kBluetoothCompanyIdentiferDanlers: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdanlers)
- [var kBluetoothCompanyIdentiferDeLormePublishingCompany: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdelormepublishingcompany)
- [var kBluetoothCompanyIdentiferDelphi: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdelphi)
- [var kBluetoothCompanyIdentiferDexcom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdexcom)
- [var kBluetoothCompanyIdentiferDialogSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdialogsemiconductor)
- [var kBluetoothCompanyIdentiferEcotest: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferecotest)
- [var kBluetoothCompanyIdentiferEdenSoftwareConsultants: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferedensoftwareconsultants)
- [var kBluetoothCompanyIdentiferElcometer: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferelcometer)
- [var kBluetoothCompanyIdentiferElgatoSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferelgatosystems)
- [var kBluetoothCompanyIdentiferEquinux: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferequinux)
- [var kBluetoothCompanyIdentiferEvluma: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferevluma)
- [var kBluetoothCompanyIdentiferFreshtemp: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfreshtemp)
- [var kBluetoothCompanyIdentiferFuGoo: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfugoo)
- [var kBluetoothCompanyIdentiferFunaiElectric: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfunaielectric)
- [var kBluetoothCompanyIdentiferGNNetcom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergnnetcom)
- [var kBluetoothCompanyIdentiferGNResound: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergnresound)
- [var kBluetoothCompanyIdentiferGarminInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergarmininternational)
- [var kBluetoothCompanyIdentiferGeLo: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergelo)
- [var kBluetoothCompanyIdentiferGeneq: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergeneq)
- [var kBluetoothCompanyIdentiferGeneralMotors: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergeneralmotors)
- [var kBluetoothCompanyIdentiferGeoforce: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergeoforce)
- [var kBluetoothCompanyIdentiferGibsonGuitars: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergibsonguitars)
- [var kBluetoothCompanyIdentiferGimbal: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergimbal)
- [var kBluetoothCompanyIdentiferGoogle: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergoogle)
- [var kBluetoothCompanyIdentiferGreenThrottleGames: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergreenthrottlegames)
- [var kBluetoothCompanyIdentiferGroupSense: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergroupsense)
- [var kBluetoothCompanyIdentiferHanlynnTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhanlynntechnologies)
- [var kBluetoothCompanyIdentiferHewlettPackard: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhewlettpackard)
- [var kBluetoothCompanyIdentiferHosiden: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhosiden)
- [var kBluetoothCompanyIdentiferITechDynamicGlobalDistribution: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferitechdynamicglobaldistribution)
- [var kBluetoothCompanyIdentiferInMusicBrands: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinmusicbrands)
- [var kBluetoothCompanyIdentiferIngenieurSystemgruppeZahn: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferingenieursystemgruppezahn)
- [var kBluetoothCompanyIdentiferInnovativeYachtterSolutions: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinnovativeyachttersolutions)
- [var kBluetoothCompanyIdentiferJawbone: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjawbone)
- [var kBluetoothCompanyIdentiferJiangsuToppowerAutomotiveElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjiangsutoppowerautomotiveelectronics)
- [var kBluetoothCompanyIdentiferJohnsonControls: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjohnsoncontrols)
- [var kBluetoothCompanyIdentiferJollyLogic: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjollylogic)
- [var kBluetoothCompanyIdentiferKOUKAMM: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkoukamm)
- [var kBluetoothCompanyIdentiferKSTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkstechnologies)
- [var kBluetoothCompanyIdentiferKawantech: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkawantech)
- [var kBluetoothCompanyIdentiferKeiser: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkeiser)
- [var kBluetoothCompanyIdentiferKensingtonComputerProductsGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkensingtoncomputerproductsgroup)
- [var kBluetoothCompanyIdentiferKentDisplays: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkentdisplays)
- [var kBluetoothCompanyIdentiferLGElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlgelectronics)
- [var kBluetoothCompanyIdentiferLSResearch: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlsresearch)
- [var kBluetoothCompanyIdentiferLairdTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlairdtechnologies)
- [var kBluetoothCompanyIdentiferLessWire: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlesswire)
- [var kBluetoothCompanyIdentiferLinak: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlinak)
- [var kBluetoothCompanyIdentiferLudusHelsinki: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferludushelsinki)
- [var kBluetoothCompanyIdentiferMC10: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermc10)
- [var kBluetoothCompanyIdentiferMStarTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermstartechnologies)
- [var kBluetoothCompanyIdentiferMagnetiMarelli: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermagnetimarelli)
- [var kBluetoothCompanyIdentiferMesoInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermesointernational)
- [var kBluetoothCompanyIdentiferMetaWatch: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermetawatch)
- [var kBluetoothCompanyIdentiferMiCommand: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermicommand)
- [var kBluetoothCompanyIdentiferMicrochipTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermicrochiptechnology)
- [var kBluetoothCompanyIdentiferMindTree: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermindtree)
- [var kBluetoothCompanyIdentiferMisfitWearables: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermisfitwearables)
- [var kBluetoothCompanyIdentiferMonster: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermonster)
- [var kBluetoothCompanyIdentiferMorseProject: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermorseproject)
- [var kBluetoothCompanyIdentiferMusik: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermusik)
- [var kBluetoothCompanyIdentiferNECLightning: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferneclightning)
- [var kBluetoothCompanyIdentiferNautilus: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernautilus)
- [var kBluetoothCompanyIdentiferNielsenKellerman: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernielsenkellerman)
- [var kBluetoothCompanyIdentiferNike: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernike)
- [var kBluetoothCompanyIdentiferODMTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferodmtechnology)
- [var kBluetoothCompanyIdentiferOTLDynamics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferotldynamics)
- [var kBluetoothCompanyIdentiferOmegawave: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferomegawave)
- [var kBluetoothCompanyIdentiferOnsetComputer: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferonsetcomputer)
- [var kBluetoothCompanyIdentiferPLUSLocationSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpluslocationsystems)
- [var kBluetoothCompanyIdentiferPandaOcean: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpandaocean)
- [var kBluetoothCompanyIdentiferPassifSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpassifsemiconductor)
- [var kBluetoothCompanyIdentiferPayPal: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpaypal)
- [var kBluetoothCompanyIdentiferPeterSystemtechnik: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpetersystemtechnik)
- [var kBluetoothCompanyIdentiferPolarElectroEurope: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpolarelectroeurope)
- [var kBluetoothCompanyIdentiferPolarElectroOY: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpolarelectrooy)
- [var kBluetoothCompanyIdentiferProctorAndGamble: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferproctorandgamble)
- [var kBluetoothCompanyIdentiferQualcommConnectedExperiences: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcommconnectedexperiences)
- [var kBluetoothCompanyIdentiferQualcommInnovationCenter: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcomminnovationcenter)
- [var kBluetoothCompanyIdentiferQualcommTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcommtechnologies)
- [var kBluetoothCompanyIdentiferQuintic: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferquintic)
- [var kBluetoothCompanyIdentiferQuupa: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferquupa)
- [var kBluetoothCompanyIdentiferRDAMicroelectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrdamicroelectronics)
- [var kBluetoothCompanyIdentiferRalinkTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferralinktechnology)
- [var kBluetoothCompanyIdentiferRealtekSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrealteksemiconductor)
- [var kBluetoothCompanyIdentiferRivieraWaves: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrivierawaves)
- [var kBluetoothCompanyIdentiferSPowerElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferspowerelectronics)
- [var kBluetoothCompanyIdentiferSRMedizinelektronik: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersrmedizinelektronik)
- [var kBluetoothCompanyIdentiferSamsungElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersamsungelectronics)
- [var kBluetoothCompanyIdentiferSarisCyclingGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersariscyclinggroup)
- [var kBluetoothCompanyIdentiferSeersTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferseerstechnology)
- [var kBluetoothCompanyIdentiferSelflyBV: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferselflybv)
- [var kBluetoothCompanyIdentiferSemilink: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersemilink)
- [var kBluetoothCompanyIdentiferSennheiserCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersennheisercommunications)
- [var kBluetoothCompanyIdentiferServerTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferservertechnology)
- [var kBluetoothCompanyIdentiferShangHaiSuperSmartElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifershanghaisupersmartelectronics)
- [var kBluetoothCompanyIdentiferShenzhenExcelsecuDataTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifershenzhenexcelsecudatatechnology)
- [var kBluetoothCompanyIdentiferSmartifier: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersmartifier)
- [var kBluetoothCompanyIdentiferSoundID: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersoundid)
- [var kBluetoothCompanyIdentiferSportsTrackingTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersportstrackingtechnologies)
- [var kBluetoothCompanyIdentiferStalmartTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstalmarttechnology)
- [var kBluetoothCompanyIdentiferStanleyBlackAndDecker: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstanleyblackanddecker)
- [var kBluetoothCompanyIdentiferStarkeyLaboratories: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstarkeylaboratories)
- [var kBluetoothCompanyIdentiferStickNFind: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersticknfind)
- [var kBluetoothCompanyIdentiferStonestreetOne: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstonestreetone)
- [var kBluetoothCompanyIdentiferSummitDataCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersummitdatacommunications)
- [var kBluetoothCompanyIdentiferSuuntoOy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersuuntooy)
- [var kBluetoothCompanyIdentiferSwirlNetworks: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferswirlnetworks)
- [var kBluetoothCompanyIdentiferTaixingbangTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertaixingbangtechnology)
- [var kBluetoothCompanyIdentiferTelitWirelessSolutions: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertelitwirelesssolutions)
- [var kBluetoothCompanyIdentiferThinkOptics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferthinkoptics)
- [var kBluetoothCompanyIdentiferTimeKeepingSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertimekeepingsystems)
- [var kBluetoothCompanyIdentiferTimexGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertimexgroup)
- [var kBluetoothCompanyIdentiferTomTomInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertomtominternational)
- [var kBluetoothCompanyIdentiferTopconPositioningSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertopconpositioningsystems)
- [var kBluetoothCompanyIdentiferTreLab: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertrelab)
- [var kBluetoothCompanyIdentiferTypeProducts: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertypeproducts)
- [var kBluetoothCompanyIdentiferUbiquitousComputingTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferubiquitouscomputingtechnology)
- [var kBluetoothCompanyIdentiferUniversalElectriconics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferuniversalelectriconics)
- [var kBluetoothCompanyIdentiferVSNTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervsntechnologies)
- [var kBluetoothCompanyIdentiferValenceTech: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervalencetech)
- [var kBluetoothCompanyIdentiferVertu: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervertu)
- [var kBluetoothCompanyIdentiferVisteon: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervisteon)
- [var kBluetoothCompanyIdentiferVoyetraTurtleBeach: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervoyetraturtlebeach)
- [var kBluetoothCompanyIdentiferVtrackSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervtracksystems)
- [var kBluetoothCompanyIdentiferWicentric: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwicentric)
- [var kBluetoothCompanyIdentiferWilliamDemantHolding: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwilliamdemantholding)
- [var kBluetoothCompanyIdentiferWitronTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwitrontechnology)
- [var kBluetoothCompanyIdentiferWuXiVimicro: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwuxivimicro)
- [var kBluetoothCompanyIdentiferZero1TV: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzero1tv)
- [var kBluetoothCompanyIdentiferZomm: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzomm)
- [var kBluetoothCompanyIdentiferZscanSoftware: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzscansoftware)
- [var kBluetoothCompanyIdentifertxtrGMBH: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertxtrgmbh)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothcompanyidentifers/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothcompanyidentifers/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothcompanyidentifers/rawvalue)
- [BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothdeviceaddress)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothdeviceaddress/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothdeviceaddress/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothdeviceaddress/data)
- [BluetoothEnhancedSynchronousConnectionInfo](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/init())
- [init(transmitBandWidth: BluetoothHCITransmitBandwidth, receiveBandWidth: BluetoothHCIReceiveBandwidth, transmitCodingFormat: BluetoothHCITransmitCodingFormat, receiveCodingFormat: BluetoothHCIReceiveCodingFormat, transmitCodecFrameSize: BluetoothHCITransmitCodecFrameSize, receiveCodecFrameSize: BluetoothHCIReceiveCodecFrameSize, inputBandwidth: BluetoothHCIInputBandwidth, outputBandwidth: BluetoothHCIOutputBandwidth, inputCodingFormat: BluetoothHCIInputCodingFormat, outputCodingFormat: BluetoothHCIOutputCodingFormat, inputCodedDataSize: BluetoothHCIInputCodedDataSize, outputCodedDataSize: BluetoothHCIOutputCodedDataSize, inputPCMDataFormat: BluetoothHCIInputPCMDataFormat, outputPCMDataFormat: BluetoothHCIOutputPCMDataFormat, inputPCMSampelPayloadMSBPosition: BluetoothHCIInputPCMSamplePayloadMSBPosition, outputPCMSampelPayloadMSBPosition: BluetoothHCIOutputPCMSamplePayloadMSBPosition, inputDataPath: BluetoothHCIInputDataPath, outputDataPath: BluetoothHCIOutputDataPath, inputTransportUnitSize: BluetoothHCIInputTransportUnitSize, outputTransportUnitSize: BluetoothHCIOutputTransportUnitSize, maxLatency: BluetoothHCIMaxLatency, voiceSetting: BluetoothHCIVoiceSetting, retransmissionEffort: BluetoothHCIRetransmissionEffort, packetType: BluetoothPacketType)](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/init(transmitbandwidth:receivebandwidth:transmitcodingformat:receivecodingformat:transmitcodecframesize:receivecodecframesize:inputbandwidth:outputbandwidth:inputcodingformat:outputcodingformat:inputcodeddatasize:outputcodeddatasize:inputpc-5g3ma)

#### Instance Properties

- [var inputBandwidth: BluetoothHCIInputBandwidth](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/inputbandwidth)
- [var inputCodedDataSize: BluetoothHCIInputCodedDataSize](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/inputcodeddatasize)
- [var inputCodingFormat: BluetoothHCIInputCodingFormat](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/inputcodingformat)
- [var inputDataPath: BluetoothHCIInputDataPath](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/inputdatapath)
- [var inputPCMDataFormat: BluetoothHCIInputPCMDataFormat](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/inputpcmdataformat)
- [var inputPCMSampelPayloadMSBPosition: BluetoothHCIInputPCMSamplePayloadMSBPosition](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/inputpcmsampelpayloadmsbposition)
- [var inputTransportUnitSize: BluetoothHCIInputTransportUnitSize](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/inputtransportunitsize)
- [var maxLatency: BluetoothHCIMaxLatency](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/maxlatency)
- [var outputBandwidth: BluetoothHCIOutputBandwidth](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/outputbandwidth)
- [var outputCodedDataSize: BluetoothHCIOutputCodedDataSize](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/outputcodeddatasize)
- [var outputCodingFormat: BluetoothHCIOutputCodingFormat](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/outputcodingformat)
- [var outputDataPath: BluetoothHCIOutputDataPath](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/outputdatapath)
- [var outputPCMDataFormat: BluetoothHCIOutputPCMDataFormat](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/outputpcmdataformat)
- [var outputPCMSampelPayloadMSBPosition: BluetoothHCIOutputPCMSamplePayloadMSBPosition](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/outputpcmsampelpayloadmsbposition)
- [var outputTransportUnitSize: BluetoothHCIOutputTransportUnitSize](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/outputtransportunitsize)
- [var packetType: BluetoothPacketType](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/packettype)
- [var receiveBandWidth: BluetoothHCIReceiveBandwidth](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/receivebandwidth)
- [var receiveCodecFrameSize: BluetoothHCIReceiveCodecFrameSize](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/receivecodecframesize)
- [var receiveCodingFormat: BluetoothHCIReceiveCodingFormat](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/receivecodingformat)
- [var retransmissionEffort: BluetoothHCIRetransmissionEffort](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/retransmissioneffort)
- [var transmitBandWidth: BluetoothHCITransmitBandwidth](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/transmitbandwidth)
- [var transmitCodecFrameSize: BluetoothHCITransmitCodecFrameSize](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/transmitcodecframesize)
- [var transmitCodingFormat: BluetoothHCITransmitCodingFormat](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/transmitcodingformat)
- [var voiceSetting: BluetoothHCIVoiceSetting](/documentation/iobluetooth/bluetoothenhancedsynchronousconnectioninfo/voicesetting)
- [BluetoothEventFilterCondition](/documentation/iobluetooth/bluetootheventfiltercondition)

#### Initializers

- [init()](/documentation/iobluetooth/bluetootheventfiltercondition/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetootheventfiltercondition/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetootheventfiltercondition/data)
- [BluetoothFeatureBits](/documentation/iobluetooth/bluetoothfeaturebits)

#### Constants

- [var kBluetoothFeature3SlotEnhancedDataRateACLPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeature3slotenhanceddatarateaclpackets)
- [var kBluetoothFeature3SlotEnhancedDataRateeSCOPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeature3slotenhanceddatarateescopackets)
- [var kBluetoothFeature5SlotEnhancedDataRateACLPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeature5slotenhanceddatarateaclpackets)
- [var kBluetoothFeatureAFHCapableMaster: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhcapablemaster)
- [var kBluetoothFeatureAFHCapableSlave: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhcapableslave)
- [var kBluetoothFeatureAFHClassificationMaster: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhclassificationmaster)
- [var kBluetoothFeatureAFHClassificationSlave: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhclassificationslave)
- [var kBluetoothFeatureALawLog: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturealawlog)
- [var kBluetoothFeatureAbsenceMasks: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureabsencemasks)
- [var kBluetoothFeatureAliasAuhentication: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturealiasauhentication)
- [var kBluetoothFeatureBroadcastEncryption: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturebroadcastencryption)
- [var kBluetoothFeatureCVSD: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturecvsd)
- [var kBluetoothFeatureChannelQuality: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturechannelquality)
- [var kBluetoothFeatureEV4Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureev4packets)
- [var kBluetoothFeatureEV5Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureev5packets)
- [var kBluetoothFeatureEncapsulatedPDU: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureencapsulatedpdu)
- [var kBluetoothFeatureEncryption: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureencryption)
- [var kBluetoothFeatureEnhancedDataRateACL2MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateacl2mbpsmode)
- [var kBluetoothFeatureEnhancedDataRateACL3MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateacl3mbpsmode)
- [var kBluetoothFeatureEnhancedDataRateeSCO2MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateesco2mbpsmode)
- [var kBluetoothFeatureEnhancedDataRateeSCO3MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateesco3mbpsmode)
- [var kBluetoothFeatureEnhancedInquiryScan: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhancedinquiryscan)
- [var kBluetoothFeatureErroneousDataReporting: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureerroneousdatareporting)
- [var kBluetoothFeatureExtendedFeatures: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureextendedfeatures)
- [var kBluetoothFeatureExtendedInquiryResponse: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureextendedinquiryresponse)
- [var kBluetoothFeatureExtendedSCOLink: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureextendedscolink)
- [var kBluetoothFeatureFiveSlotPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturefiveslotpackets)
- [var kBluetoothFeatureFlowControlLagBit0: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureflowcontrollagbit0)
- [var kBluetoothFeatureFlowControlLagBit1: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureflowcontrollagbit1)
- [var kBluetoothFeatureFlowControlLagBit2: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureflowcontrollagbit2)
- [var kBluetoothFeatureHV2Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturehv2packets)
- [var kBluetoothFeatureHV3Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturehv3packets)
- [var kBluetoothFeatureHoldMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureholdmode)
- [var kBluetoothFeatureInquiryTransmissionPowerLevel: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureinquirytransmissionpowerlevel)
- [var kBluetoothFeatureInterlacedInquiryScan: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureinterlacedinquiryscan)
- [var kBluetoothFeatureInterlacedPageScan: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureinterlacedpagescan)
- [var kBluetoothFeatureLESupportedController: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturelesupportedcontroller)
- [var kBluetoothFeatureLinkSupervisionTimeoutChangedEvent: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturelinksupervisiontimeoutchangedevent)
- [var kBluetoothFeatureNonFlushablePacketBoundaryFlag: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturenonflushablepacketboundaryflag)
- [var kBluetoothFeaturePagingScheme: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepagingscheme)
- [var kBluetoothFeatureParkMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureparkmode)
- [var kBluetoothFeaturePauseEncryption: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepauseencryption)
- [var kBluetoothFeaturePowerControl: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepowercontrol)
- [var kBluetoothFeaturePowerControlRequests: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepowercontrolrequests)
- [var kBluetoothFeatureRSSI: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturerssi)
- [var kBluetoothFeatureRSSIWithInquiryResult: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturerssiwithinquiryresult)
- [var kBluetoothFeatureSCOLink: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturescolink)
- [var kBluetoothFeatureScatterMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturescattermode)
- [var kBluetoothFeatureSecureSimplePairing: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturesecuresimplepairing)
- [var kBluetoothFeatureSlotOffset: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureslotoffset)
- [var kBluetoothFeatureSniffMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturesniffmode)
- [var kBluetoothFeatureSniffSubrating: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturesniffsubrating)
- [var kBluetoothFeatureSwitchRoles: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureswitchroles)
- [var kBluetoothFeatureThreeSlotPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturethreeslotpackets)
- [var kBluetoothFeatureTimingAccuracy: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturetimingaccuracy)
- [var kBluetoothFeatureTransparentSCOData: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturetransparentscodata)
- [var kBluetoothFeatureULawLog: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureulawlog)
- [var KBluetoothExtendedFeatureSecureConnectionsHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturesecureconnectionshostmode)
- [var kBluetoothExtendedFeatureLEAndBREDRToSameDeviceHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeatureleandbredrtosamedevicehostmode)
- [var kBluetoothExtendedFeatureLESupportedHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturelesupportedhostmode)
- [var kBluetoothExtendedFeaturePing: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeatureping)
- [var kBluetoothExtendedFeatureReserved: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturereserved)
- [var kBluetoothExtendedFeatureSecureConnectionsControllerSupport: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturesecureconnectionscontrollersupport)
- [var kBluetoothExtendedFeatureSimpleSecurePairingHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturesimplesecurepairinghostmode)
- [var kBluetoothExtendedFeatureSlotAvailabilityMask: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeatureslotavailabilitymask)
- [var kBluetoothExtendedFeatureTrainNudging: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturetrainnudging)
- [var kBluetoothFeatureAFHCapablePeripheral: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhcapableperipheral)
- [var kBluetoothFeatureAFHClassificationPeripheral: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhclassificationperipheral)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothfeaturebits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothfeaturebits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothfeaturebits/rawvalue)
- [BluetoothHCIAFHChannelAssessmentModes](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes)

#### Constants

- [var kAFHChannelAssessmentModeDisabled: BluetoothHCIAFHChannelAssessmentModes](/documentation/iobluetooth/kafhchannelassessmentmodedisabled)
- [var kAFHChannelAssessmentModeEnabled: BluetoothHCIAFHChannelAssessmentModes](/documentation/iobluetooth/kafhchannelassessmentmodeenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes/rawvalue)
- [BluetoothHCIAcceptSynchronousConnectionRequestParams](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/init())
- [init(transmitBandwidth: UInt32, receiveBandwidth: UInt32, maxLatency: UInt16, contentFormat: UInt16, retransmissionEffort: UInt8, packetType: UInt16)](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/init(transmitbandwidth:receivebandwidth:maxlatency:contentformat:retransmissioneffort:packettype:))

#### Instance Properties

- [var contentFormat: UInt16](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/contentformat)
- [var maxLatency: UInt16](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/maxlatency)
- [var packetType: UInt16](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/packettype)
- [var receiveBandwidth: UInt32](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/receivebandwidth)
- [var retransmissionEffort: UInt8](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/retransmissioneffort)
- [var transmitBandwidth: UInt32](/documentation/iobluetooth/bluetoothhciacceptsynchronousconnectionrequestparams/transmitbandwidth)
- [BluetoothHCIAuthentionEnableModes](/documentation/iobluetooth/bluetoothhciauthentionenablemodes)

#### Constants

- [var kAuthenticationDisabled: BluetoothHCIAuthentionEnableModes](/documentation/iobluetooth/kauthenticationdisabled)
- [var kAuthenticationEnabled: BluetoothHCIAuthentionEnableModes](/documentation/iobluetooth/kauthenticationenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciauthentionenablemodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciauthentionenablemodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciauthentionenablemodes/rawvalue)
- [BluetoothHCIAutomaticFlushTimeoutInfo](/documentation/iobluetooth/bluetoothhciautomaticflushtimeoutinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciautomaticflushtimeoutinfo/init())
- [init(handle: BluetoothConnectionHandle, timeout: BluetoothHCIAutomaticFlushTimeout)](/documentation/iobluetooth/bluetoothhciautomaticflushtimeoutinfo/init(handle:timeout:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhciautomaticflushtimeoutinfo/handle)
- [var timeout: BluetoothHCIAutomaticFlushTimeout](/documentation/iobluetooth/bluetoothhciautomaticflushtimeoutinfo/timeout)
- [BluetoothHCIBufferSize](/documentation/iobluetooth/bluetoothhcibuffersize)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcibuffersize/init())
- [init(ACLDataPacketLength: UInt16, SCODataPacketLength: UInt8, totalNumACLDataPackets: UInt16, totalNumSCODataPackets: UInt16)](/documentation/iobluetooth/bluetoothhcibuffersize/init(acldatapacketlength:scodatapacketlength:totalnumacldatapackets:totalnumscodatapackets:))

#### Instance Properties

- [var ACLDataPacketLength: UInt16](/documentation/iobluetooth/bluetoothhcibuffersize/acldatapacketlength)
- [var SCODataPacketLength: UInt8](/documentation/iobluetooth/bluetoothhcibuffersize/scodatapacketlength)
- [var totalNumACLDataPackets: UInt16](/documentation/iobluetooth/bluetoothhcibuffersize/totalnumacldatapackets)
- [var totalNumSCODataPackets: UInt16](/documentation/iobluetooth/bluetoothhcibuffersize/totalnumscodatapackets)
- [BluetoothHCIConnectionModes](/documentation/iobluetooth/bluetoothhciconnectionmodes)

#### Constants

- [var kConnectionActiveMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionactivemode)
- [var kConnectionHoldMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionholdmode)
- [var kConnectionModeReservedForFutureUse: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionmodereservedforfutureuse)
- [var kConnectionParkMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionparkmode)
- [var kConnectionSniffMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionsniffmode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciconnectionmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciconnectionmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciconnectionmodes/rawvalue)
- [BluetoothHCICurrentInquiryAccessCodes](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodes)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodes/init())
- [init(count: BluetoothHCIInquiryAccessCodeCount, codes: UnsafeMutablePointer<BluetoothHCIInquiryAccessCode>!)](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodes/init(count:codes:))

#### Instance Properties

- [var codes: UnsafeMutablePointer<BluetoothHCIInquiryAccessCode>!](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodes/codes)
- [var count: BluetoothHCIInquiryAccessCodeCount](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodes/count)
- [BluetoothHCICurrentInquiryAccessCodesForWrite](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodesforwrite)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodesforwrite/init())
- [init(count: BluetoothHCIInquiryAccessCodeCount, codes: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodesforwrite/init(count:codes:))

#### Instance Properties

- [var codes: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodesforwrite/codes)
- [var count: BluetoothHCIInquiryAccessCodeCount](/documentation/iobluetooth/bluetoothhcicurrentinquiryaccesscodesforwrite/count)
- [BluetoothHCIDeleteStoredLinkKeyFlags](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags)

#### Constants

- [var kDeleteAllStoredLinkKeys: BluetoothHCIDeleteStoredLinkKeyFlags](/documentation/iobluetooth/kdeleteallstoredlinkkeys)
- [var kDeleteKeyForSpecifiedDeviceOnly: BluetoothHCIDeleteStoredLinkKeyFlags](/documentation/iobluetooth/kdeletekeyforspecifieddeviceonly)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags/rawvalue)
- [BluetoothHCIEncryptionModes](/documentation/iobluetooth/bluetoothhciencryptionmodes)

#### Constants

- [var kEncryptionDisabled: BluetoothHCIEncryptionModes](/documentation/iobluetooth/kencryptiondisabled)
- [var kEncryptionForBothPointToPointAndBroadcastPackets: BluetoothHCIEncryptionModes](/documentation/iobluetooth/kencryptionforbothpointtopointandbroadcastpackets)
- [var kEncryptionOnlyForPointToPointPackets: BluetoothHCIEncryptionModes](/documentation/iobluetooth/kencryptiononlyforpointtopointpackets)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciencryptionmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciencryptionmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciencryptionmodes/rawvalue)
- [BluetoothHCIEnhancedAcceptSynchronousConnectionRequestParams](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/init())
- [init(transmitBandwidth: UInt32, receiveBandwidth: UInt32, transmitCodingFormat: UInt64, receiveCodingFormat: UInt64, transmitCodecFrameSize: UInt16, receiveCodecFrameSize: UInt16, inputBandwidth: UInt32, outputBandwidth: UInt32, inputCodingFormat: UInt64, outputCodingFormat: UInt64, inputCodedDataSize: UInt16, outputCodedDataSize: UInt16, inputPCMDataFormat: UInt8, outputPCMDataFormat: UInt8, inputPCMSamplePayloadMSBPosition: UInt8, outputPCMSamplePayloadMSBPosition: UInt8, inputDataPath: UInt8, outputDataPath: UInt8, inputTransportUnitSize: UInt8, outputTransportUnitSize: UInt8, maxLatency: UInt16, packetType: UInt16, retransmissionEffort: UInt8)](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/init(transmitbandwidth:receivebandwidth:transmitcodingformat:receivecodingformat:transmitcodecframesize:receivecodecframesize:inputbandwidth:outputbandwidth:inputcodingformat:outputcodingformat:inputcodeddatasize:outputcodeddatasize:inputpc-4r4o8)

#### Instance Properties

- [var inputBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/inputbandwidth)
- [var inputCodedDataSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/inputcodeddatasize)
- [var inputCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/inputcodingformat)
- [var inputDataPath: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/inputdatapath)
- [var inputPCMDataFormat: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/inputpcmdataformat)
- [var inputPCMSamplePayloadMSBPosition: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/inputpcmsamplepayloadmsbposition)
- [var inputTransportUnitSize: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/inputtransportunitsize)
- [var maxLatency: UInt16](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/maxlatency)
- [var outputBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/outputbandwidth)
- [var outputCodedDataSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/outputcodeddatasize)
- [var outputCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/outputcodingformat)
- [var outputDataPath: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/outputdatapath)
- [var outputPCMDataFormat: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/outputpcmdataformat)
- [var outputPCMSamplePayloadMSBPosition: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/outputpcmsamplepayloadmsbposition)
- [var outputTransportUnitSize: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/outputtransportunitsize)
- [var packetType: UInt16](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/packettype)
- [var receiveBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/receivebandwidth)
- [var receiveCodecFrameSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/receivecodecframesize)
- [var receiveCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/receivecodingformat)
- [var retransmissionEffort: UInt8](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/retransmissioneffort)
- [var transmitBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/transmitbandwidth)
- [var transmitCodecFrameSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/transmitcodecframesize)
- [var transmitCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedacceptsynchronousconnectionrequestparams/transmitcodingformat)
- [BluetoothHCIEnhancedSetupSynchronousConnectionParams](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/init())
- [init(transmitBandwidth: UInt32, receiveBandwidth: UInt32, transmitCodingFormat: UInt64, receiveCodingFormat: UInt64, transmitCodecFrameSize: UInt16, receiveCodecFrameSize: UInt16, inputBandwidth: UInt32, outputBandwidth: UInt32, inputCodingFormat: UInt64, outputCodingFormat: UInt64, inputCodedDataSize: UInt16, outputCodedDataSize: UInt16, inputPCMDataFormat: UInt8, outputPCMDataFormat: UInt8, inputPCMSamplePayloadMSBPosition: UInt8, outputPCMSamplePayloadMSBPosition: UInt8, inputDataPath: UInt8, outputDataPath: UInt8, inputTransportUnitSize: UInt8, outputTransportUnitSize: UInt8, maxLatency: UInt16, packetType: UInt16, retransmissionEffort: UInt8)](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/init(transmitbandwidth:receivebandwidth:transmitcodingformat:receivecodingformat:transmitcodecframesize:receivecodecframesize:inputbandwidth:outputbandwidth:inputcodingformat:outputcodingformat:inputcodeddatasize:outputcodeddatasize:inputpc-4r4o8)

#### Instance Properties

- [var inputBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/inputbandwidth)
- [var inputCodedDataSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/inputcodeddatasize)
- [var inputCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/inputcodingformat)
- [var inputDataPath: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/inputdatapath)
- [var inputPCMDataFormat: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/inputpcmdataformat)
- [var inputPCMSamplePayloadMSBPosition: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/inputpcmsamplepayloadmsbposition)
- [var inputTransportUnitSize: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/inputtransportunitsize)
- [var maxLatency: UInt16](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/maxlatency)
- [var outputBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/outputbandwidth)
- [var outputCodedDataSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/outputcodeddatasize)
- [var outputCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/outputcodingformat)
- [var outputDataPath: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/outputdatapath)
- [var outputPCMDataFormat: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/outputpcmdataformat)
- [var outputPCMSamplePayloadMSBPosition: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/outputpcmsamplepayloadmsbposition)
- [var outputTransportUnitSize: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/outputtransportunitsize)
- [var packetType: UInt16](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/packettype)
- [var receiveBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/receivebandwidth)
- [var receiveCodecFrameSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/receivecodecframesize)
- [var receiveCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/receivecodingformat)
- [var retransmissionEffort: UInt8](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/retransmissioneffort)
- [var transmitBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/transmitbandwidth)
- [var transmitCodecFrameSize: UInt16](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/transmitcodecframesize)
- [var transmitCodingFormat: UInt64](/documentation/iobluetooth/bluetoothhcienhancedsetupsynchronousconnectionparams/transmitcodingformat)
- [BluetoothHCIEventAuthenticationCompleteResults](/documentation/iobluetooth/bluetoothhcieventauthenticationcompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventauthenticationcompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhcieventauthenticationcompleteresults/init(connectionhandle:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventauthenticationcompleteresults/connectionhandle)
- [BluetoothHCIEventChangeConnectionLinkKeyCompleteResults](/documentation/iobluetooth/bluetoothhcieventchangeconnectionlinkkeycompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventchangeconnectionlinkkeycompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhcieventchangeconnectionlinkkeycompleteresults/init(connectionhandle:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventchangeconnectionlinkkeycompleteresults/connectionhandle)
- [BluetoothHCIEventConnectionCompleteResults](/documentation/iobluetooth/bluetoothhcieventconnectioncompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventconnectioncompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, deviceAddress: BluetoothDeviceAddress, linkType: BluetoothLinkType, encryptionMode: BluetoothHCIEncryptionMode)](/documentation/iobluetooth/bluetoothhcieventconnectioncompleteresults/init(connectionhandle:deviceaddress:linktype:encryptionmode:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventconnectioncompleteresults/connectionhandle)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventconnectioncompleteresults/deviceaddress)
- [var encryptionMode: BluetoothHCIEncryptionMode](/documentation/iobluetooth/bluetoothhcieventconnectioncompleteresults/encryptionmode)
- [var linkType: BluetoothLinkType](/documentation/iobluetooth/bluetoothhcieventconnectioncompleteresults/linktype)
- [BluetoothHCIEventConnectionPacketTypeResults](/documentation/iobluetooth/bluetoothhcieventconnectionpackettyperesults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventconnectionpackettyperesults/init())
- [init(connectionHandle: BluetoothConnectionHandle, packetType: BluetoothPacketType)](/documentation/iobluetooth/bluetoothhcieventconnectionpackettyperesults/init(connectionhandle:packettype:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventconnectionpackettyperesults/connectionhandle)
- [var packetType: BluetoothPacketType](/documentation/iobluetooth/bluetoothhcieventconnectionpackettyperesults/packettype)
- [BluetoothHCIEventConnectionRequestResults](/documentation/iobluetooth/bluetoothhcieventconnectionrequestresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventconnectionrequestresults/init())
- [init(deviceAddress: BluetoothDeviceAddress, classOfDevice: BluetoothClassOfDevice, linkType: BluetoothLinkType)](/documentation/iobluetooth/bluetoothhcieventconnectionrequestresults/init(deviceaddress:classofdevice:linktype:))

#### Instance Properties

- [var classOfDevice: BluetoothClassOfDevice](/documentation/iobluetooth/bluetoothhcieventconnectionrequestresults/classofdevice)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventconnectionrequestresults/deviceaddress)
- [var linkType: BluetoothLinkType](/documentation/iobluetooth/bluetoothhcieventconnectionrequestresults/linktype)
- [BluetoothHCIEventDataBufferOverflowResults](/documentation/iobluetooth/bluetoothhcieventdatabufferoverflowresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventdatabufferoverflowresults/init())
- [init(linkType: BluetoothLinkType)](/documentation/iobluetooth/bluetoothhcieventdatabufferoverflowresults/init(linktype:))

#### Instance Properties

- [var linkType: BluetoothLinkType](/documentation/iobluetooth/bluetoothhcieventdatabufferoverflowresults/linktype)
- [BluetoothHCIEventDisconnectionCompleteResults](/documentation/iobluetooth/bluetoothhcieventdisconnectioncompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventdisconnectioncompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, reason: BluetoothReasonCode)](/documentation/iobluetooth/bluetoothhcieventdisconnectioncompleteresults/init(connectionhandle:reason:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventdisconnectioncompleteresults/connectionhandle)
- [var reason: BluetoothReasonCode](/documentation/iobluetooth/bluetoothhcieventdisconnectioncompleteresults/reason)
- [BluetoothHCIEventEncryptionChangeResults](/documentation/iobluetooth/bluetoothhcieventencryptionchangeresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventencryptionchangeresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, enable: BluetoothEncryptionEnable)](/documentation/iobluetooth/bluetoothhcieventencryptionchangeresults/init(connectionhandle:enable:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventencryptionchangeresults/connectionhandle)
- [var enable: BluetoothEncryptionEnable](/documentation/iobluetooth/bluetoothhcieventencryptionchangeresults/enable)
- [BluetoothHCIEventEncryptionKeyRefreshCompleteResults](/documentation/iobluetooth/bluetoothhcieventencryptionkeyrefreshcompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventencryptionkeyrefreshcompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhcieventencryptionkeyrefreshcompleteresults/init(connectionhandle:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventencryptionkeyrefreshcompleteresults/connectionhandle)
- [BluetoothHCIEventFlowSpecificationData](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/init())
- [init(connectionHandle: BluetoothConnectionHandle, flags: UInt8, flowDirection: UInt8, serviceType: UInt8, tokenRate: UInt32, tokenBucketSize: UInt32, peakBandwidth: UInt32, accessLatency: UInt32)](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/init(connectionhandle:flags:flowdirection:servicetype:tokenrate:tokenbucketsize:peakbandwidth:accesslatency:))

#### Instance Properties

- [var accessLatency: UInt32](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/accesslatency)
- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/connectionhandle)
- [var flags: UInt8](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/flags)
- [var flowDirection: UInt8](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/flowdirection)
- [var peakBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/peakbandwidth)
- [var serviceType: UInt8](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/servicetype)
- [var tokenBucketSize: UInt32](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/tokenbucketsize)
- [var tokenRate: UInt32](/documentation/iobluetooth/bluetoothhcieventflowspecificationdata/tokenrate)
- [BluetoothHCIEventFlushOccurredResults](/documentation/iobluetooth/bluetoothhcieventflushoccurredresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventflushoccurredresults/init())
- [init(connectionHandle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhcieventflushoccurredresults/init(connectionhandle:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventflushoccurredresults/connectionhandle)
- [BluetoothHCIEventHardwareErrorResults](/documentation/iobluetooth/bluetoothhcieventhardwareerrorresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventhardwareerrorresults/init())
- [init(error: BluetoothHCIStatus)](/documentation/iobluetooth/bluetoothhcieventhardwareerrorresults/init(error:))

#### Instance Properties

- [var error: BluetoothHCIStatus](/documentation/iobluetooth/bluetoothhcieventhardwareerrorresults/error)
- [BluetoothHCIEventLEConnectionCompleteResults](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, role: UInt8, peerAddressType: UInt8, peerAddress: BluetoothDeviceAddress, connInterval: UInt16, connLatency: UInt16, supervisionTimeout: UInt16, masterClockAccuracy: UInt8)](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/init(connectionhandle:role:peeraddresstype:peeraddress:conninterval:connlatency:supervisiontimeout:masterclockaccuracy:))

#### Instance Properties

- [var connInterval: UInt16](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/conninterval)
- [var connLatency: UInt16](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/connlatency)
- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/connectionhandle)
- [var masterClockAccuracy: UInt8](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/masterclockaccuracy)
- [var peerAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/peeraddress)
- [var peerAddressType: UInt8](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/peeraddresstype)
- [var role: UInt8](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/role)
- [var supervisionTimeout: UInt16](/documentation/iobluetooth/bluetoothhcieventleconnectioncompleteresults/supervisiontimeout)
- [BluetoothHCIEventLEConnectionUpdateCompleteResults](/documentation/iobluetooth/bluetoothhcieventleconnectionupdatecompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventleconnectionupdatecompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, connInterval: UInt16, connLatency: UInt16, supervisionTimeout: UInt16)](/documentation/iobluetooth/bluetoothhcieventleconnectionupdatecompleteresults/init(connectionhandle:conninterval:connlatency:supervisiontimeout:))

#### Instance Properties

- [var connInterval: UInt16](/documentation/iobluetooth/bluetoothhcieventleconnectionupdatecompleteresults/conninterval)
- [var connLatency: UInt16](/documentation/iobluetooth/bluetoothhcieventleconnectionupdatecompleteresults/connlatency)
- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventleconnectionupdatecompleteresults/connectionhandle)
- [var supervisionTimeout: UInt16](/documentation/iobluetooth/bluetoothhcieventleconnectionupdatecompleteresults/supervisiontimeout)
- [BluetoothHCIEventLELongTermKeyRequestResults](/documentation/iobluetooth/bluetoothhcieventlelongtermkeyrequestresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventlelongtermkeyrequestresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, randomNumber: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8), ediv: UInt16)](/documentation/iobluetooth/bluetoothhcieventlelongtermkeyrequestresults/init(connectionhandle:randomnumber:ediv:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventlelongtermkeyrequestresults/connectionhandle)
- [var ediv: UInt16](/documentation/iobluetooth/bluetoothhcieventlelongtermkeyrequestresults/ediv)
- [var randomNumber: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhcieventlelongtermkeyrequestresults/randomnumber)
- [BluetoothHCIEventLEMetaResults](/documentation/iobluetooth/bluetoothhcieventlemetaresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventlemetaresults/init())
- [init(length: UInt8, data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhcieventlemetaresults/init(length:data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhcieventlemetaresults/data)
- [var length: UInt8](/documentation/iobluetooth/bluetoothhcieventlemetaresults/length)
- [BluetoothHCIEventLEReadRemoteUsedFeaturesCompleteResults](/documentation/iobluetooth/bluetoothhcieventlereadremoteusedfeaturescompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventlereadremoteusedfeaturescompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, usedFeatures: BluetoothHCISupportedFeatures)](/documentation/iobluetooth/bluetoothhcieventlereadremoteusedfeaturescompleteresults/init(connectionhandle:usedfeatures:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventlereadremoteusedfeaturescompleteresults/connectionhandle)
- [var usedFeatures: BluetoothHCISupportedFeatures](/documentation/iobluetooth/bluetoothhcieventlereadremoteusedfeaturescompleteresults/usedfeatures)
- [BluetoothHCIEventLinkKeyNotificationResults](/documentation/iobluetooth/bluetoothhcieventlinkkeynotificationresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventlinkkeynotificationresults/init())
- [init(deviceAddress: BluetoothDeviceAddress, linkKey: BluetoothKey, keyType: BluetoothKeyType)](/documentation/iobluetooth/bluetoothhcieventlinkkeynotificationresults/init(deviceaddress:linkkey:keytype:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventlinkkeynotificationresults/deviceaddress)
- [var keyType: BluetoothKeyType](/documentation/iobluetooth/bluetoothhcieventlinkkeynotificationresults/keytype)
- [var linkKey: BluetoothKey](/documentation/iobluetooth/bluetoothhcieventlinkkeynotificationresults/linkkey)
- [BluetoothHCIEventMasterLinkKeyCompleteResults](/documentation/iobluetooth/bluetoothhcieventmasterlinkkeycompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventmasterlinkkeycompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, keyFlag: BluetoothKeyFlag)](/documentation/iobluetooth/bluetoothhcieventmasterlinkkeycompleteresults/init(connectionhandle:keyflag:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventmasterlinkkeycompleteresults/connectionhandle)
- [var keyFlag: BluetoothKeyFlag](/documentation/iobluetooth/bluetoothhcieventmasterlinkkeycompleteresults/keyflag)
- [BluetoothHCIEventMaxSlotsChangeResults](/documentation/iobluetooth/bluetoothhcieventmaxslotschangeresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventmaxslotschangeresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, maxSlots: BluetoothMaxSlots)](/documentation/iobluetooth/bluetoothhcieventmaxslotschangeresults/init(connectionhandle:maxslots:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventmaxslotschangeresults/connectionhandle)
- [var maxSlots: BluetoothMaxSlots](/documentation/iobluetooth/bluetoothhcieventmaxslotschangeresults/maxslots)
- [BluetoothHCIEventModeChangeResults](/documentation/iobluetooth/bluetoothhcieventmodechangeresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventmodechangeresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, mode: BluetoothHCIConnectionMode, modeInterval: BluetoothHCIModeInterval)](/documentation/iobluetooth/bluetoothhcieventmodechangeresults/init(connectionhandle:mode:modeinterval:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventmodechangeresults/connectionhandle)
- [var mode: BluetoothHCIConnectionMode](/documentation/iobluetooth/bluetoothhcieventmodechangeresults/mode)
- [var modeInterval: BluetoothHCIModeInterval](/documentation/iobluetooth/bluetoothhcieventmodechangeresults/modeinterval)
- [BluetoothHCIEventPageScanModeChangeResults](/documentation/iobluetooth/bluetoothhcieventpagescanmodechangeresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventpagescanmodechangeresults/init())
- [init(deviceAddress: BluetoothDeviceAddress, pageScanMode: BluetoothPageScanMode)](/documentation/iobluetooth/bluetoothhcieventpagescanmodechangeresults/init(deviceaddress:pagescanmode:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventpagescanmodechangeresults/deviceaddress)
- [var pageScanMode: BluetoothPageScanMode](/documentation/iobluetooth/bluetoothhcieventpagescanmodechangeresults/pagescanmode)
- [BluetoothHCIEventPageScanRepetitionModeChangeResults](/documentation/iobluetooth/bluetoothhcieventpagescanrepetitionmodechangeresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventpagescanrepetitionmodechangeresults/init())
- [init(deviceAddress: BluetoothDeviceAddress, pageScanRepetitionMode: BluetoothPageScanRepetitionMode)](/documentation/iobluetooth/bluetoothhcieventpagescanrepetitionmodechangeresults/init(deviceaddress:pagescanrepetitionmode:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventpagescanrepetitionmodechangeresults/deviceaddress)
- [var pageScanRepetitionMode: BluetoothPageScanRepetitionMode](/documentation/iobluetooth/bluetoothhcieventpagescanrepetitionmodechangeresults/pagescanrepetitionmode)
- [BluetoothHCIEventQoSSetupCompleteResults](/documentation/iobluetooth/bluetoothhcieventqossetupcompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventqossetupcompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, setupParams: BluetoothHCIQualityOfServiceSetupParams)](/documentation/iobluetooth/bluetoothhcieventqossetupcompleteresults/init(connectionhandle:setupparams:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventqossetupcompleteresults/connectionhandle)
- [var setupParams: BluetoothHCIQualityOfServiceSetupParams](/documentation/iobluetooth/bluetoothhcieventqossetupcompleteresults/setupparams)
- [BluetoothHCIEventQoSViolationResults](/documentation/iobluetooth/bluetoothhcieventqosviolationresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventqosviolationresults/init())
- [init(connectionHandle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhcieventqosviolationresults/init(connectionhandle:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventqosviolationresults/connectionhandle)
- [BluetoothHCIEventReadClockOffsetResults](/documentation/iobluetooth/bluetoothhcieventreadclockoffsetresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventreadclockoffsetresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, clockOffset: BluetoothClockOffset)](/documentation/iobluetooth/bluetoothhcieventreadclockoffsetresults/init(connectionhandle:clockoffset:))

#### Instance Properties

- [var clockOffset: BluetoothClockOffset](/documentation/iobluetooth/bluetoothhcieventreadclockoffsetresults/clockoffset)
- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventreadclockoffsetresults/connectionhandle)
- [BluetoothHCIEventReadExtendedFeaturesResults](/documentation/iobluetooth/bluetoothhcieventreadextendedfeaturesresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventreadextendedfeaturesresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, supportedFeaturesInfo: BluetoothHCIExtendedFeaturesInfo)](/documentation/iobluetooth/bluetoothhcieventreadextendedfeaturesresults/init(connectionhandle:supportedfeaturesinfo:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventreadextendedfeaturesresults/connectionhandle)
- [var supportedFeaturesInfo: BluetoothHCIExtendedFeaturesInfo](/documentation/iobluetooth/bluetoothhcieventreadextendedfeaturesresults/supportedfeaturesinfo)
- [BluetoothHCIEventReadRemoteExtendedFeaturesResults](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults/init())
- [init(error: BluetoothHCIStatus, connectionHandle: BluetoothConnectionHandle, page: BluetoothHCIPageNumber, maxPage: BluetoothHCIPageNumber, lmpFeatures: BluetoothHCISupportedFeatures)](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults/init(error:connectionhandle:page:maxpage:lmpfeatures:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults/connectionhandle)
- [var error: BluetoothHCIStatus](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults/error)
- [var lmpFeatures: BluetoothHCISupportedFeatures](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults/lmpfeatures)
- [var maxPage: BluetoothHCIPageNumber](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults/maxpage)
- [var page: BluetoothHCIPageNumber](/documentation/iobluetooth/bluetoothhcieventreadremoteextendedfeaturesresults/page)
- [BluetoothHCIEventReadRemoteSupportedFeaturesResults](/documentation/iobluetooth/bluetoothhcieventreadremotesupportedfeaturesresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventreadremotesupportedfeaturesresults/init())
- [init(error: BluetoothHCIStatus, connectionHandle: BluetoothConnectionHandle, lmpFeatures: BluetoothHCISupportedFeatures)](/documentation/iobluetooth/bluetoothhcieventreadremotesupportedfeaturesresults/init(error:connectionhandle:lmpfeatures:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventreadremotesupportedfeaturesresults/connectionhandle)
- [var error: BluetoothHCIStatus](/documentation/iobluetooth/bluetoothhcieventreadremotesupportedfeaturesresults/error)
- [var lmpFeatures: BluetoothHCISupportedFeatures](/documentation/iobluetooth/bluetoothhcieventreadremotesupportedfeaturesresults/lmpfeatures)
- [BluetoothHCIEventReadRemoteVersionInfoResults](/documentation/iobluetooth/bluetoothhcieventreadremoteversioninforesults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventreadremoteversioninforesults/init())
- [init(connectionHandle: BluetoothConnectionHandle, lmpVersion: BluetoothLMPVersion, manufacturerName: BluetoothManufacturerName, lmpSubversion: BluetoothLMPSubversion)](/documentation/iobluetooth/bluetoothhcieventreadremoteversioninforesults/init(connectionhandle:lmpversion:manufacturername:lmpsubversion:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventreadremoteversioninforesults/connectionhandle)
- [var lmpSubversion: BluetoothLMPSubversion](/documentation/iobluetooth/bluetoothhcieventreadremoteversioninforesults/lmpsubversion)
- [var lmpVersion: BluetoothLMPVersion](/documentation/iobluetooth/bluetoothhcieventreadremoteversioninforesults/lmpversion)
- [var manufacturerName: BluetoothManufacturerName](/documentation/iobluetooth/bluetoothhcieventreadremoteversioninforesults/manufacturername)
- [BluetoothHCIEventReadSupportedFeaturesResults](/documentation/iobluetooth/bluetoothhcieventreadsupportedfeaturesresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventreadsupportedfeaturesresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, supportedFeatures: BluetoothHCISupportedFeatures)](/documentation/iobluetooth/bluetoothhcieventreadsupportedfeaturesresults/init(connectionhandle:supportedfeatures:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventreadsupportedfeaturesresults/connectionhandle)
- [var supportedFeatures: BluetoothHCISupportedFeatures](/documentation/iobluetooth/bluetoothhcieventreadsupportedfeaturesresults/supportedfeatures)
- [BluetoothHCIEventRemoteNameRequestResults](/documentation/iobluetooth/bluetoothhcieventremotenamerequestresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventremotenamerequestresults/init())
- [init(deviceAddress: BluetoothDeviceAddress, deviceName: BluetoothDeviceName)](/documentation/iobluetooth/bluetoothhcieventremotenamerequestresults/init(deviceaddress:devicename:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventremotenamerequestresults/deviceaddress)
- [var deviceName: BluetoothDeviceName](/documentation/iobluetooth/bluetoothhcieventremotenamerequestresults/devicename)
- [BluetoothHCIEventReturnLinkKeysResults](/documentation/iobluetooth/bluetoothhcieventreturnlinkkeysresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventreturnlinkkeysresults/init())

#### Instance Properties

- [var numLinkKeys: UInt8](/documentation/iobluetooth/bluetoothhcieventreturnlinkkeysresults/numlinkkeys)
- [BluetoothHCIEventRoleChangeResults](/documentation/iobluetooth/bluetoothhcieventrolechangeresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventrolechangeresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, deviceAddress: BluetoothDeviceAddress, role: BluetoothRole)](/documentation/iobluetooth/bluetoothhcieventrolechangeresults/init(connectionhandle:deviceaddress:role:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventrolechangeresults/connectionhandle)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventrolechangeresults/deviceaddress)
- [var role: BluetoothRole](/documentation/iobluetooth/bluetoothhcieventrolechangeresults/role)
- [BluetoothHCIEventSimplePairingCompleteResults](/documentation/iobluetooth/bluetoothhcieventsimplepairingcompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventsimplepairingcompleteresults/init())
- [init(deviceAddress: BluetoothDeviceAddress)](/documentation/iobluetooth/bluetoothhcieventsimplepairingcompleteresults/init(deviceaddress:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventsimplepairingcompleteresults/deviceaddress)
- [BluetoothHCIEventSniffSubratingResults](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, maxTransmitLatency: UInt16, maxReceiveLatency: UInt16, minRemoteTimeout: UInt16, minLocalTimeout: UInt16)](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults/init(connectionhandle:maxtransmitlatency:maxreceivelatency:minremotetimeout:minlocaltimeout:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults/connectionhandle)
- [var maxReceiveLatency: UInt16](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults/maxreceivelatency)
- [var maxTransmitLatency: UInt16](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults/maxtransmitlatency)
- [var minLocalTimeout: UInt16](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults/minlocaltimeout)
- [var minRemoteTimeout: UInt16](/documentation/iobluetooth/bluetoothhcieventsniffsubratingresults/minremotetimeout)
- [BluetoothHCIEventSynchronousConnectionChangedResults](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, transmissionInterval: UInt8, retransmissionWindow: UInt8, receivePacketLength: UInt16, transmitPacketLength: UInt16)](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults/init(connectionhandle:transmissioninterval:retransmissionwindow:receivepacketlength:transmitpacketlength:))

#### Instance Properties

- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults/connectionhandle)
- [var receivePacketLength: UInt16](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults/receivepacketlength)
- [var retransmissionWindow: UInt8](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults/retransmissionwindow)
- [var transmissionInterval: UInt8](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults/transmissioninterval)
- [var transmitPacketLength: UInt16](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectionchangedresults/transmitpacketlength)
- [BluetoothHCIEventSynchronousConnectionCompleteResults](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, deviceAddress: BluetoothDeviceAddress, linkType: BluetoothLinkType, transmissionInterval: UInt8, retransmissionWindow: UInt8, receivePacketLength: UInt16, transmitPacketLength: UInt16, airMode: BluetoothAirMode)](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/init(connectionhandle:deviceaddress:linktype:transmissioninterval:retransmissionwindow:receivepacketlength:transmitpacketlength:airmode:))

#### Instance Properties

- [var airMode: BluetoothAirMode](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/airmode)
- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/connectionhandle)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/deviceaddress)
- [var linkType: BluetoothLinkType](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/linktype)
- [var receivePacketLength: UInt16](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/receivepacketlength)
- [var retransmissionWindow: UInt8](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/retransmissionwindow)
- [var transmissionInterval: UInt8](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/transmissioninterval)
- [var transmitPacketLength: UInt16](/documentation/iobluetooth/bluetoothhcieventsynchronousconnectioncompleteresults/transmitpacketlength)
- [BluetoothHCIEventVendorSpecificResults](/documentation/iobluetooth/bluetoothhcieventvendorspecificresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventvendorspecificresults/init())
- [init(length: UInt8, data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhcieventvendorspecificresults/init(length:data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhcieventvendorspecificresults/data)
- [var length: UInt8](/documentation/iobluetooth/bluetoothhcieventvendorspecificresults/length)
- [BluetoothHCIExtendedFeaturesInfo](/documentation/iobluetooth/bluetoothhciextendedfeaturesinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciextendedfeaturesinfo/init())
- [init(page: BluetoothHCIPageNumber, maxPage: BluetoothHCIPageNumber, data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhciextendedfeaturesinfo/init(page:maxpage:data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhciextendedfeaturesinfo/data)
- [var maxPage: BluetoothHCIPageNumber](/documentation/iobluetooth/bluetoothhciextendedfeaturesinfo/maxpage)
- [var page: BluetoothHCIPageNumber](/documentation/iobluetooth/bluetoothhciextendedfeaturesinfo/page)
- [BluetoothHCIExtendedInquiryResponse](/documentation/iobluetooth/bluetoothhciextendedinquiryresponse)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciextendedinquiryresponse/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhciextendedinquiryresponse/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhciextendedinquiryresponse/data)
- [BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes)

#### Constants

- [var kBluetoothHCIExtendedInquiryResponseDataType128BitServiceClassUUIDsCompleteList: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype128bitserviceclassuuidscompletelist)
- [var kBluetoothHCIExtendedInquiryResponseDataType128BitServiceClassUUIDsWithMoreAvailable: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype128bitserviceclassuuidswithmoreavailable)
- [var kBluetoothHCIExtendedInquiryResponseDataType16BitServiceClassUUIDsCompleteList: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype16bitserviceclassuuidscompletelist)
- [var kBluetoothHCIExtendedInquiryResponseDataType16BitServiceClassUUIDsWithMoreAvailable: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype16bitserviceclassuuidswithmoreavailable)
- [var kBluetoothHCIExtendedInquiryResponseDataType32BitServiceClassUUIDsCompleteList: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype32bitserviceclassuuidscompletelist)
- [var kBluetoothHCIExtendedInquiryResponseDataType32BitServiceClassUUIDsWithMoreAvailable: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype32bitserviceclassuuidswithmoreavailable)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeAppearance: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeappearance)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeCompleteLocalName: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypecompletelocalname)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeDeviceID: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypedeviceid)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeFlags: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeflags)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeManufacturerSpecificData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypemanufacturerspecificdata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypePublicTargetAddress: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypepublictargetaddress)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeRandomTargetAddress: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatyperandomtargetaddress)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSSPOOBClassOfDevice: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesspoobclassofdevice)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSSPOOBSimplePairingHashC: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesspoobsimplepairinghashc)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSSPOOBSimplePairingRandomizerR: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesspoobsimplepairingrandomizerr)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecurityManagerOOBFlags: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecuritymanageroobflags)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecurityManagerTKValue: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecuritymanagertkvalue)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicedata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceSolicitation128BitUUIDs: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicesolicitation128bituuids)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceSolicitation16BitUUIDs: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicesolicitation16bituuids)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeShortenedLocalName: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeshortenedlocalname)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSlaveConnectionIntervalRange: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeslaveconnectionintervalrange)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeTransmitPowerLevel: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypetransmitpowerlevel)
- [var kBluetoothHCIExtendedInquiryResponseDataType3DInformationData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype3dinformationdata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeAdvertisingInterval: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeadvertisinginterval)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeLEBluetoothDeviceAddress: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypelebluetoothdeviceaddress)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeLERole: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypelerole)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecureConnectionsConfirmationValue: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecureconnectionsconfirmationvalue)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecureConnectionsRandomValue: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecureconnectionsrandomvalue)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceData128BitUUID: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicedata128bituuid)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceData32BitUUID: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicedata32bituuid)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceSolicitation32BitUUIDs: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicesolicitation32bituuids)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSimplePairingHash: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesimplepairinghash)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSimplePairingRandomizer: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesimplepairingrandomizer)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeIndoorPositioning: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeindoorpositioning)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeTransportDiscoveryData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypetransportdiscoverydata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeURI: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeuri)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeCsisRsiData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypecsisrsidata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypePeripheralConnectionIntervalRange: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeperipheralconnectionintervalrange)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes/rawvalue)
- [BluetoothHCIExtendedInquiryResult](/documentation/iobluetooth/bluetoothhciextendedinquiryresult)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/init())
- [init(numberOfReponses: UInt8, deviceAddress: BluetoothDeviceAddress, pageScanRepetitionMode: BluetoothPageScanRepetitionMode, reserved: UInt8, classOfDevice: BluetoothClassOfDevice, clockOffset: BluetoothClockOffset, RSSIValue: BluetoothHCIRSSIValue, extendedInquiryResponse: BluetoothHCIExtendedInquiryResponse)](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/init(numberofreponses:deviceaddress:pagescanrepetitionmode:reserved:classofdevice:clockoffset:rssivalue:extendedinquiryresponse:))

#### Instance Properties

- [var RSSIValue: BluetoothHCIRSSIValue](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/rssivalue)
- [var classOfDevice: BluetoothClassOfDevice](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/classofdevice)
- [var clockOffset: BluetoothClockOffset](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/clockoffset)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/deviceaddress)
- [var extendedInquiryResponse: BluetoothHCIExtendedInquiryResponse](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/extendedinquiryresponse)
- [var numberOfReponses: UInt8](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/numberofreponses)
- [var pageScanRepetitionMode: BluetoothPageScanRepetitionMode](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/pagescanrepetitionmode)
- [var reserved: UInt8](/documentation/iobluetooth/bluetoothhciextendedinquiryresult/reserved)
- [BluetoothHCIFECRequiredValues](/documentation/iobluetooth/bluetoothhcifecrequiredvalues)

#### Constants

- [var kBluetoothHCIFECNotRequired: BluetoothHCIFECRequiredValues](/documentation/iobluetooth/kbluetoothhcifecnotrequired)
- [var kBluetoothHCIFECRequired: BluetoothHCIFECRequiredValues](/documentation/iobluetooth/kbluetoothhcifecrequired)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcifecrequiredvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcifecrequiredvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcifecrequiredvalues/rawvalue)
- [BluetoothHCIFailedContactInfo](/documentation/iobluetooth/bluetoothhcifailedcontactinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcifailedcontactinfo/init())
- [init(count: BluetoothHCIFailedContactCount, handle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhcifailedcontactinfo/init(count:handle:))

#### Instance Properties

- [var count: BluetoothHCIFailedContactCount](/documentation/iobluetooth/bluetoothhcifailedcontactinfo/count)
- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcifailedcontactinfo/handle)
- [BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates)

#### Constants

- [var kHCIACLDataPacketsOffHCISCODataPacketsOn: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khciacldatapacketsoffhciscodatapacketson)
- [var kHCIACLDataPacketsOnHCISCODataPacketsOff: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khciacldatapacketsonhciscodatapacketsoff)
- [var kHCIACLDataPacketsOnHCISCODataPacketsOn: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khciacldatapacketsonhciscodatapacketson)
- [var kHostControllerToHostFlowControlOff: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khostcontrollertohostflowcontroloff)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates/rawvalue)
- [BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates)

#### Constants

- [var kMaintainCurrentPowerState: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/kmaintaincurrentpowerstate)
- [var kSuspendInquiryScan: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/ksuspendinquiryscan)
- [var kSuspendPageScan: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/ksuspendpagescan)
- [var kSuspendPeriodicInquiries: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/ksuspendperiodicinquiries)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates/rawvalue)
- [BluetoothHCIInquiryAccessCode](/documentation/iobluetooth/bluetoothhciinquiryaccesscode)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciinquiryaccesscode/init())
- [init(data: (UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhciinquiryaccesscode/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhciinquiryaccesscode/data)
- [BluetoothHCIInquiryModes](/documentation/iobluetooth/bluetoothhciinquirymodes)

#### Constants

- [var kBluetoothHCIInquiryModeResultFormatStandard: BluetoothHCIInquiryModes](/documentation/iobluetooth/kbluetoothhciinquirymoderesultformatstandard)
- [var kBluetoothHCIInquiryModeResultFormatWithRSSI: BluetoothHCIInquiryModes](/documentation/iobluetooth/kbluetoothhciinquirymoderesultformatwithrssi)
- [var kBluetoothHCIInquiryModeResultFormatWithRSSIOrExtendedInquiryResultFormat: BluetoothHCIInquiryModes](/documentation/iobluetooth/kbluetoothhciinquirymoderesultformatwithrssiorextendedinquiryresultformat)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciinquirymodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciinquirymodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciinquirymodes/rawvalue)
- [BluetoothHCIInquiryResult](/documentation/iobluetooth/bluetoothhciinquiryresult)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciinquiryresult/init())
- [init(deviceAddress: BluetoothDeviceAddress, pageScanRepetitionMode: BluetoothPageScanRepetitionMode, pageScanPeriodMode: BluetoothHCIPageScanPeriodMode, pageScanMode: BluetoothHCIPageScanMode, classOfDevice: BluetoothClassOfDevice, clockOffset: BluetoothClockOffset)](/documentation/iobluetooth/bluetoothhciinquiryresult/init(deviceaddress:pagescanrepetitionmode:pagescanperiodmode:pagescanmode:classofdevice:clockoffset:))

#### Instance Properties

- [var classOfDevice: BluetoothClassOfDevice](/documentation/iobluetooth/bluetoothhciinquiryresult/classofdevice)
- [var clockOffset: BluetoothClockOffset](/documentation/iobluetooth/bluetoothhciinquiryresult/clockoffset)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhciinquiryresult/deviceaddress)
- [var pageScanMode: BluetoothHCIPageScanMode](/documentation/iobluetooth/bluetoothhciinquiryresult/pagescanmode)
- [var pageScanPeriodMode: BluetoothHCIPageScanPeriodMode](/documentation/iobluetooth/bluetoothhciinquiryresult/pagescanperiodmode)
- [var pageScanRepetitionMode: BluetoothPageScanRepetitionMode](/documentation/iobluetooth/bluetoothhciinquiryresult/pagescanrepetitionmode)
- [BluetoothHCIInquiryResults](/documentation/iobluetooth/bluetoothhciinquiryresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciinquiryresults/init())
- [init(results: (BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult), count: IOItemCount)](/documentation/iobluetooth/bluetoothhciinquiryresults/init(results:count:))

#### Instance Properties

- [var count: IOItemCount](/documentation/iobluetooth/bluetoothhciinquiryresults/count)
- [var results: (BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult, BluetoothHCIInquiryResult)](/documentation/iobluetooth/bluetoothhciinquiryresults/results)
- [BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/bluetoothhciinquiryscantypes)

#### Constants

- [var kBluetoothHCIInquiryScanTypeInterlaced: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypeinterlaced)
- [var kBluetoothHCIInquiryScanTypeReservedEnd: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypereservedend)
- [var kBluetoothHCIInquiryScanTypeReservedStart: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypereservedstart)
- [var kBluetoothHCIInquiryScanTypeStandard: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypestandard)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciinquiryscantypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciinquiryscantypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciinquiryscantypes/rawvalue)
- [BluetoothHCIInquiryWithRSSIResult](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/init())
- [init(deviceAddress: BluetoothDeviceAddress, pageScanRepetitionMode: BluetoothPageScanRepetitionMode, reserved: UInt8, classOfDevice: BluetoothClassOfDevice, clockOffset: BluetoothClockOffset, RSSIValue: BluetoothHCIRSSIValue)](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/init(deviceaddress:pagescanrepetitionmode:reserved:classofdevice:clockoffset:rssivalue:))

#### Instance Properties

- [var RSSIValue: BluetoothHCIRSSIValue](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/rssivalue)
- [var classOfDevice: BluetoothClassOfDevice](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/classofdevice)
- [var clockOffset: BluetoothClockOffset](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/clockoffset)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/deviceaddress)
- [var pageScanRepetitionMode: BluetoothPageScanRepetitionMode](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/pagescanrepetitionmode)
- [var reserved: UInt8](/documentation/iobluetooth/bluetoothhciinquirywithrssiresult/reserved)
- [BluetoothHCIInquiryWithRSSIResults](/documentation/iobluetooth/bluetoothhciinquirywithrssiresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciinquirywithrssiresults/init())
- [init(results: (BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult), count: IOItemCount)](/documentation/iobluetooth/bluetoothhciinquirywithrssiresults/init(results:count:))

#### Instance Properties

- [var count: IOItemCount](/documentation/iobluetooth/bluetoothhciinquirywithrssiresults/count)
- [var results: (BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult, BluetoothHCIInquiryWithRSSIResult)](/documentation/iobluetooth/bluetoothhciinquirywithrssiresults/results)
- [BluetoothHCILEBufferSize](/documentation/iobluetooth/bluetoothhcilebuffersize)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcilebuffersize/init())
- [init(ACLDataPacketLength: UInt16, totalNumACLDataPackets: UInt8)](/documentation/iobluetooth/bluetoothhcilebuffersize/init(acldatapacketlength:totalnumacldatapackets:))

#### Instance Properties

- [var ACLDataPacketLength: UInt16](/documentation/iobluetooth/bluetoothhcilebuffersize/acldatapacketlength)
- [var totalNumACLDataPackets: UInt8](/documentation/iobluetooth/bluetoothhcilebuffersize/totalnumacldatapackets)
- [BluetoothHCILinkPolicySettingsInfo](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsinfo/init())
- [init(settings: BluetoothHCILinkPolicySettings, handle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsinfo/init(settings:handle:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsinfo/handle)
- [var settings: BluetoothHCILinkPolicySettings](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsinfo/settings)
- [BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues)

#### Constants

- [var kDisableAllLMModes: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kdisablealllmmodes)
- [var kEnableHoldMode: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenableholdmode)
- [var kEnableMasterSlaveSwitch: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenablemasterslaveswitch)
- [var kEnableParkMode: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenableparkmode)
- [var kEnableSniffMode: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenablesniffmode)
- [var kReservedForFutureUse: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kreservedforfutureuse)
- [var kEnableCentralPeripheralSwitch: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenablecentralperipheralswitch)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues/rawvalue)
- [BluetoothHCILinkQualityInfo](/documentation/iobluetooth/bluetoothhcilinkqualityinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcilinkqualityinfo/init())
- [init(handle: BluetoothConnectionHandle, qualityValue: BluetoothHCILinkQuality)](/documentation/iobluetooth/bluetoothhcilinkqualityinfo/init(handle:qualityvalue:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcilinkqualityinfo/handle)
- [var qualityValue: BluetoothHCILinkQuality](/documentation/iobluetooth/bluetoothhcilinkqualityinfo/qualityvalue)
- [BluetoothHCILinkSupervisionTimeout](/documentation/iobluetooth/bluetoothhcilinksupervisiontimeout)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcilinksupervisiontimeout/init())
- [init(handle: BluetoothConnectionHandle, timeout: UInt16)](/documentation/iobluetooth/bluetoothhcilinksupervisiontimeout/init(handle:timeout:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcilinksupervisiontimeout/handle)
- [var timeout: UInt16](/documentation/iobluetooth/bluetoothhcilinksupervisiontimeout/timeout)
- [BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/bluetoothhcipagescanenablestates)

#### Constants

- [var kInquiryScanDisabledPageScanEnabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/kinquiryscandisabledpagescanenabled)
- [var kInquiryScanEnabledPageScanDisabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/kinquiryscanenabledpagescandisabled)
- [var kInquiryScanEnabledPageScanEnabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/kinquiryscanenabledpagescanenabled)
- [var kNoScansEnabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/knoscansenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescanenablestates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescanenablestates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescanenablestates/rawvalue)
- [BluetoothHCIPageScanModes](/documentation/iobluetooth/bluetoothhcipagescanmodes)

#### Constants

- [var kMandatoryPageScanMode: BluetoothHCIPageScanModes](/documentation/iobluetooth/kmandatorypagescanmode)
- [var kOptionalPageScanMode1: BluetoothHCIPageScanModes](/documentation/iobluetooth/koptionalpagescanmode1)
- [var kOptionalPageScanMode2: BluetoothHCIPageScanModes](/documentation/iobluetooth/koptionalpagescanmode2)
- [var kOptionalPageScanMode3: BluetoothHCIPageScanModes](/documentation/iobluetooth/koptionalpagescanmode3)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescanmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescanmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescanmodes/rawvalue)
- [BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes)

#### Constants

- [var kP0Mode: BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/kp0mode)
- [var kP1Mode: BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/kp1mode)
- [var kP2Mode: BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/kp2mode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes/rawvalue)
- [BluetoothHCIPageScanTypes](/documentation/iobluetooth/bluetoothhcipagescantypes)

#### Constants

- [var kBluetoothHCIPageScanTypeInterlaced: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypeinterlaced)
- [var kBluetoothHCIPageScanTypeReservedEnd: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypereservedend)
- [var kBluetoothHCIPageScanTypeReservedStart: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypereservedstart)
- [var kBluetoothHCIPageScanTypeStandard: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypestandard)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescantypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescantypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescantypes/rawvalue)
- [BluetoothHCIPowerState](/documentation/iobluetooth/bluetoothhcipowerstate)

#### Constants

- [var kBluetoothHCIPowerStateOFF: BluetoothHCIPowerState](/documentation/iobluetooth/kbluetoothhcipowerstateoff)
- [var kBluetoothHCIPowerStateON: BluetoothHCIPowerState](/documentation/iobluetooth/kbluetoothhcipowerstateon)
- [var kBluetoothHCIPowerStateUnintialized: BluetoothHCIPowerState](/documentation/iobluetooth/kbluetoothhcipowerstateunintialized)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipowerstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipowerstate/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipowerstate/rawvalue)
- [BluetoothHCIQualityOfServiceSetupParams](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/init())
- [init(flags: UInt8, serviceType: UInt8, tokenRate: UInt32, peakBandwidth: UInt32, latency: UInt32, delayVariation: UInt32)](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/init(flags:servicetype:tokenrate:peakbandwidth:latency:delayvariation:))

#### Instance Properties

- [var delayVariation: UInt32](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/delayvariation)
- [var flags: UInt8](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/flags)
- [var latency: UInt32](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/latency)
- [var peakBandwidth: UInt32](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/peakbandwidth)
- [var serviceType: UInt8](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/servicetype)
- [var tokenRate: UInt32](/documentation/iobluetooth/bluetoothhciqualityofservicesetupparams/tokenrate)
- [BluetoothHCIRSSIInfo](/documentation/iobluetooth/bluetoothhcirssiinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcirssiinfo/init())
- [init(handle: BluetoothConnectionHandle, RSSIValue: BluetoothHCIRSSIValue)](/documentation/iobluetooth/bluetoothhcirssiinfo/init(handle:rssivalue:))

#### Instance Properties

- [var RSSIValue: BluetoothHCIRSSIValue](/documentation/iobluetooth/bluetoothhcirssiinfo/rssivalue)
- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcirssiinfo/handle)
- [BluetoothHCIReadExtendedInquiryResponseResults](/documentation/iobluetooth/bluetoothhcireadextendedinquiryresponseresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcireadextendedinquiryresponseresults/init())
- [init(outFECRequired: BluetoothHCIFECRequired, extendedInquiryResponse: BluetoothHCIExtendedInquiryResponse)](/documentation/iobluetooth/bluetoothhcireadextendedinquiryresponseresults/init(outfecrequired:extendedinquiryresponse:))

#### Instance Properties

- [var extendedInquiryResponse: BluetoothHCIExtendedInquiryResponse](/documentation/iobluetooth/bluetoothhcireadextendedinquiryresponseresults/extendedinquiryresponse)
- [var outFECRequired: BluetoothHCIFECRequired](/documentation/iobluetooth/bluetoothhcireadextendedinquiryresponseresults/outfecrequired)
- [BluetoothHCIReadLMPHandleResults](/documentation/iobluetooth/bluetoothhcireadlmphandleresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcireadlmphandleresults/init())
- [init(handle: BluetoothConnectionHandle, lmp_handle: BluetoothLMPHandle, reserved: UInt32)](/documentation/iobluetooth/bluetoothhcireadlmphandleresults/init(handle:lmp_handle:reserved:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcireadlmphandleresults/handle)
- [var lmp_handle: BluetoothLMPHandle](/documentation/iobluetooth/bluetoothhcireadlmphandleresults/lmp_handle)
- [var reserved: UInt32](/documentation/iobluetooth/bluetoothhcireadlmphandleresults/reserved)
- [BluetoothHCIReadLocalOOBDataResults](/documentation/iobluetooth/bluetoothhcireadlocaloobdataresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcireadlocaloobdataresults/init())
- [init(hash: BluetoothHCISimplePairingOOBData, randomizer: BluetoothHCISimplePairingOOBData)](/documentation/iobluetooth/bluetoothhcireadlocaloobdataresults/init(hash:randomizer:))

#### Instance Properties

- [var hash: BluetoothHCISimplePairingOOBData](/documentation/iobluetooth/bluetoothhcireadlocaloobdataresults/hash)
- [var randomizer: BluetoothHCISimplePairingOOBData](/documentation/iobluetooth/bluetoothhcireadlocaloobdataresults/randomizer)
- [BluetoothHCIReadStoredLinkKeysFlags](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags)

#### Constants

- [var kReadAllStoredLinkKeys: BluetoothHCIReadStoredLinkKeysFlags](/documentation/iobluetooth/kreadallstoredlinkkeys)
- [var kReturnLinkKeyForSpecifiedDeviceOnly: BluetoothHCIReadStoredLinkKeysFlags](/documentation/iobluetooth/kreturnlinkkeyforspecifieddeviceonly)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags/rawvalue)
- [BluetoothHCIRequestCallbackInfo](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo/init())
- [init(userCallback: mach_vm_address_t, userRefCon: mach_vm_address_t, internalRefCon: mach_vm_address_t, asyncIDRefCon: mach_vm_address_t, reserved: mach_vm_address_t)](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo/init(usercallback:userrefcon:internalrefcon:asyncidrefcon:reserved:))

#### Instance Properties

- [var asyncIDRefCon: mach_vm_address_t](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo/asyncidrefcon)
- [var internalRefCon: mach_vm_address_t](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo/internalrefcon)
- [var reserved: mach_vm_address_t](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo/reserved)
- [var userCallback: mach_vm_address_t](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo/usercallback)
- [var userRefCon: mach_vm_address_t](/documentation/iobluetooth/bluetoothhcirequestcallbackinfo/userrefcon)
- [BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes)

#### Constants

- [var kHCIRetransmissionEffortTypeAtLeastOneAndOptimizeForPower: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypeatleastoneandoptimizeforpower)
- [var kHCIRetransmissionEffortTypeAtLeastOneAndOptimizeLinkQuality: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypeatleastoneandoptimizelinkquality)
- [var kHCIRetransmissionEffortTypeDontCare: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypedontcare)
- [var kHCIRetransmissionEffortTypeNone: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypenone)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes/rawvalue)
- [BluetoothHCIRoleInfo](/documentation/iobluetooth/bluetoothhciroleinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciroleinfo/init())
- [init(role: UInt8, handle: BluetoothConnectionHandle)](/documentation/iobluetooth/bluetoothhciroleinfo/init(role:handle:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhciroleinfo/handle)
- [var role: UInt8](/documentation/iobluetooth/bluetoothhciroleinfo/role)
- [BluetoothHCIRoles](/documentation/iobluetooth/bluetoothhciroles)

#### Constants

- [var kBluetoothHCIMasterRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhcimasterrole)
- [var kBluetoothHCISlaveRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhcislaverole)
- [var kBluetoothHCICentralRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhcicentralrole)
- [var kBluetoothHCIPeripheralRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhciperipheralrole)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciroles/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciroles/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciroles/rawvalue)
- [BluetoothHCISCOFlowControlStates](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates)

#### Constants

- [var kSCOFlowControlDisabled: BluetoothHCISCOFlowControlStates](/documentation/iobluetooth/kscoflowcontroldisabled)
- [var kSCOFlowControlEnabled: BluetoothHCISCOFlowControlStates](/documentation/iobluetooth/kscoflowcontrolenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates/rawvalue)
- [BluetoothHCIScanActivity](/documentation/iobluetooth/bluetoothhciscanactivity)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciscanactivity/init())
- [init(scanInterval: UInt16, scanWindow: UInt16)](/documentation/iobluetooth/bluetoothhciscanactivity/init(scaninterval:scanwindow:))

#### Instance Properties

- [var scanInterval: UInt16](/documentation/iobluetooth/bluetoothhciscanactivity/scaninterval)
- [var scanWindow: UInt16](/documentation/iobluetooth/bluetoothhciscanactivity/scanwindow)
- [BluetoothHCISetupSynchronousConnectionParams](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/init())
- [init(transmitBandwidth: UInt32, receiveBandwidth: UInt32, maxLatency: UInt16, voiceSetting: UInt16, retransmissionEffort: UInt8, packetType: UInt16)](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/init(transmitbandwidth:receivebandwidth:maxlatency:voicesetting:retransmissioneffort:packettype:))

#### Instance Properties

- [var maxLatency: UInt16](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/maxlatency)
- [var packetType: UInt16](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/packettype)
- [var receiveBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/receivebandwidth)
- [var retransmissionEffort: UInt8](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/retransmissioneffort)
- [var transmitBandwidth: UInt32](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/transmitbandwidth)
- [var voiceSetting: UInt16](/documentation/iobluetooth/bluetoothhcisetupsynchronousconnectionparams/voicesetting)
- [BluetoothHCISimplePairingModes](/documentation/iobluetooth/bluetoothhcisimplepairingmodes)

#### Constants

- [var kBluetoothHCISimplePairingModeEnabled: BluetoothHCISimplePairingModes](/documentation/iobluetooth/kbluetoothhcisimplepairingmodeenabled)
- [var kBluetoothHCISimplePairingModeNotSet: BluetoothHCISimplePairingModes](/documentation/iobluetooth/kbluetoothhcisimplepairingmodenotset)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcisimplepairingmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcisimplepairingmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcisimplepairingmodes/rawvalue)
- [BluetoothHCISimplePairingOOBData](/documentation/iobluetooth/bluetoothhcisimplepairingoobdata)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcisimplepairingoobdata/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhcisimplepairingoobdata/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhcisimplepairingoobdata/data)
- [BluetoothHCIStoredLinkKeysInfo](/documentation/iobluetooth/bluetoothhcistoredlinkkeysinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcistoredlinkkeysinfo/init())
- [init(numLinkKeysRead: UInt16, maxNumLinkKeysAllowedInDevice: UInt16)](/documentation/iobluetooth/bluetoothhcistoredlinkkeysinfo/init(numlinkkeysread:maxnumlinkkeysallowedindevice:))

#### Instance Properties

- [var maxNumLinkKeysAllowedInDevice: UInt16](/documentation/iobluetooth/bluetoothhcistoredlinkkeysinfo/maxnumlinkkeysallowedindevice)
- [var numLinkKeysRead: UInt16](/documentation/iobluetooth/bluetoothhcistoredlinkkeysinfo/numlinkkeysread)
- [BluetoothHCISupportedCommands](/documentation/iobluetooth/bluetoothhcisupportedcommands)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcisupportedcommands/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhcisupportedcommands/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhcisupportedcommands/data)
- [BluetoothHCISupportedFeatures](/documentation/iobluetooth/bluetoothhcisupportedfeatures)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcisupportedfeatures/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothhcisupportedfeatures/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothhcisupportedfeatures/data)
- [BluetoothHCITimeoutValues](/documentation/iobluetooth/bluetoothhcitimeoutvalues)

#### Constants

- [var kDefaultPageTimeout: BluetoothHCITimeoutValues](/documentation/iobluetooth/kdefaultpagetimeout)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcitimeoutvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcitimeoutvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcitimeoutvalues/rawvalue)
- [BluetoothHCITransmitPowerLevelInfo](/documentation/iobluetooth/bluetoothhcitransmitpowerlevelinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcitransmitpowerlevelinfo/init())
- [init(handle: BluetoothConnectionHandle, level: BluetoothHCITransmitPowerLevel)](/documentation/iobluetooth/bluetoothhcitransmitpowerlevelinfo/init(handle:level:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcitransmitpowerlevelinfo/handle)
- [var level: BluetoothHCITransmitPowerLevel](/documentation/iobluetooth/bluetoothhcitransmitpowerlevelinfo/level)
- [BluetoothHCITransmitReadPowerLevelTypes](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes)

#### Constants

- [var kReadCurrentTransmitPowerLevel: BluetoothHCITransmitReadPowerLevelTypes](/documentation/iobluetooth/kreadcurrenttransmitpowerlevel)
- [var kReadMaximumTransmitPowerLevel: BluetoothHCITransmitReadPowerLevelTypes](/documentation/iobluetooth/kreadmaximumtransmitpowerlevel)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes/rawvalue)
- [BluetoothHCIVersionInfo](/documentation/iobluetooth/bluetoothhciversioninfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciversioninfo/init())
- [init(manufacturerName: BluetoothManufacturerName, lmpVersion: BluetoothLMPVersion, lmpSubVersion: BluetoothLMPSubversion, hciVersion: UInt8, hciRevision: UInt16)](/documentation/iobluetooth/bluetoothhciversioninfo/init(manufacturername:lmpversion:lmpsubversion:hciversion:hcirevision:))

#### Instance Properties

- [var hciRevision: UInt16](/documentation/iobluetooth/bluetoothhciversioninfo/hcirevision)
- [var hciVersion: UInt8](/documentation/iobluetooth/bluetoothhciversioninfo/hciversion)
- [var lmpSubVersion: BluetoothLMPSubversion](/documentation/iobluetooth/bluetoothhciversioninfo/lmpsubversion)
- [var lmpVersion: BluetoothLMPVersion](/documentation/iobluetooth/bluetoothhciversioninfo/lmpversion)
- [var manufacturerName: BluetoothManufacturerName](/documentation/iobluetooth/bluetoothhciversioninfo/manufacturername)
- [BluetoothHCIVersions](/documentation/iobluetooth/bluetoothhciversions)

#### Constants

- [var kBluetoothHCIVersionCoreSpecification1_0b: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification1_0b)
- [var kBluetoothHCIVersionCoreSpecification1_1: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification1_1)
- [var kBluetoothHCIVersionCoreSpecification1_2: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification1_2)
- [var kBluetoothHCIVersionCoreSpecification2_0EDR: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification2_0edr)
- [var kBluetoothHCIVersionCoreSpecification2_1EDR: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification2_1edr)
- [var kBluetoothHCIVersionCoreSpecification3_0HS: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification3_0hs)
- [var kBluetoothHCIVersionCoreSpecification4_0: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification4_0)
- [var kBluetoothHCIVersionCoreSpecification4_1: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification4_1)
- [var kBluetoothHCIVersionCoreSpecification4_2: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification4_2)
- [var kBluetoothHCIVersionCoreSpecification5_0: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_0)
- [var kBluetoothHCIVersionCoreSpecification5_1: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_1)
- [var kBluetoothHCIVersionCoreSpecification5_2: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_2)
- [var kBluetoothHCIVersionCoreSpecification5_3: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_3)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciversions/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciversions/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciversions/rawvalue)
- [BluetoothIOCapabilities](/documentation/iobluetooth/bluetoothiocapabilities)

#### Constants

- [var kBluetoothCapabilityTypeDisplayOnly: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypedisplayonly)
- [var kBluetoothCapabilityTypeDisplayYesNo: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypedisplayyesno)
- [var kBluetoothCapabilityTypeKeyboardOnly: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypekeyboardonly)
- [var kBluetoothCapabilityTypeNoInputNoOutput: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypenoinputnooutput)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothiocapabilities/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothiocapabilities/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothiocapabilities/rawvalue)
- [BluetoothIOCapabilityResponse](/documentation/iobluetooth/bluetoothiocapabilityresponse)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothiocapabilityresponse/init())
- [init(deviceAddress: BluetoothDeviceAddress, ioCapability: BluetoothIOCapability, OOBDataPresence: BluetoothOOBDataPresence, authenticationRequirements: BluetoothAuthenticationRequirements)](/documentation/iobluetooth/bluetoothiocapabilityresponse/init(deviceaddress:iocapability:oobdatapresence:authenticationrequirements:))

#### Instance Properties

- [var OOBDataPresence: BluetoothOOBDataPresence](/documentation/iobluetooth/bluetoothiocapabilityresponse/oobdatapresence)
- [var authenticationRequirements: BluetoothAuthenticationRequirements](/documentation/iobluetooth/bluetoothiocapabilityresponse/authenticationrequirements)
- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothiocapabilityresponse/deviceaddress)
- [var ioCapability: BluetoothIOCapability](/documentation/iobluetooth/bluetoothiocapabilityresponse/iocapability)
- [BluetoothIRK](/documentation/iobluetooth/bluetoothirk)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothirk/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothirk/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothirk/data)
- [BluetoothKey](/documentation/iobluetooth/bluetoothkey)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothkey/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothkey/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothkey/data)
- [BluetoothKeypressNotification](/documentation/iobluetooth/bluetoothkeypressnotification)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothkeypressnotification/init())
- [init(deviceAddress: BluetoothDeviceAddress, notificationType: BluetoothKeypressNotificationType)](/documentation/iobluetooth/bluetoothkeypressnotification/init(deviceaddress:notificationtype:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothkeypressnotification/deviceaddress)
- [var notificationType: BluetoothKeypressNotificationType](/documentation/iobluetooth/bluetoothkeypressnotification/notificationtype)
- [BluetoothKeypressNotificationTypes](/documentation/iobluetooth/bluetoothkeypressnotificationtypes)

#### Constants

- [var kBluetoothKeypressNotificationTypePasskeyCleared: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeycleared)
- [var kBluetoothKeypressNotificationTypePasskeyDigitEntered: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeydigitentered)
- [var kBluetoothKeypressNotificationTypePasskeyDigitErased: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeydigiterased)
- [var kBluetoothKeypressNotificationTypePasskeyEntryCompleted: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeyentrycompleted)
- [var kBluetoothKeypressNotificationTypePasskeyEntryStarted: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeyentrystarted)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothkeypressnotificationtypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothkeypressnotificationtypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothkeypressnotificationtypes/rawvalue)
- [BluetoothL2CAPCommandCode](/documentation/iobluetooth/bluetoothl2capcommandcode)

#### Constants

- [var kBluetoothL2CAPCommandCodeCommandReject: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodecommandreject)
- [var kBluetoothL2CAPCommandCodeConfigureRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconfigurerequest)
- [var kBluetoothL2CAPCommandCodeConfigureResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconfigureresponse)
- [var kBluetoothL2CAPCommandCodeConnectionParameterUpdateRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionparameterupdaterequest)
- [var kBluetoothL2CAPCommandCodeConnectionParameterUpdateResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionparameterupdateresponse)
- [var kBluetoothL2CAPCommandCodeConnectionRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionrequest)
- [var kBluetoothL2CAPCommandCodeConnectionResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionresponse)
- [var kBluetoothL2CAPCommandCodeCreateChannelRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodecreatechannelrequest)
- [var kBluetoothL2CAPCommandCodeCreateChannelResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodecreatechannelresponse)
- [var kBluetoothL2CAPCommandCodeDisconnectionRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodedisconnectionrequest)
- [var kBluetoothL2CAPCommandCodeDisconnectionResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodedisconnectionresponse)
- [var kBluetoothL2CAPCommandCodeEchoRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeechorequest)
- [var kBluetoothL2CAPCommandCodeEchoResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeechoresponse)
- [var kBluetoothL2CAPCommandCodeInformationRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeinformationrequest)
- [var kBluetoothL2CAPCommandCodeInformationResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeinformationresponse)
- [var kBluetoothL2CAPCommandCodeLECreditBasedConnectionRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodelecreditbasedconnectionrequest)
- [var kBluetoothL2CAPCommandCodeLECreditBasedConnectionResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodelecreditbasedconnectionresponse)
- [var kBluetoothL2CAPCommandCodeLEFlowControlCredit: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeleflowcontrolcredit)
- [var kBluetoothL2CAPCommandCodeMoveChannelConfirmation: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelconfirmation)
- [var kBluetoothL2CAPCommandCodeMoveChannelConfirmationResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelconfirmationresponse)
- [var kBluetoothL2CAPCommandCodeMoveChannelRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelrequest)
- [var kBluetoothL2CAPCommandCodeMoveChannelResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelresponse)
- [var kBluetoothL2CAPCommandCodeReserved: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodereserved)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capcommandcode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capcommandcode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capcommandcode/rawvalue)
- [BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/bluetoothl2capcommandrejectreason)

#### Constants

- [var kBluetoothL2CAPCommandRejectReasonCommandNotUnderstood: BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/kbluetoothl2capcommandrejectreasoncommandnotunderstood)
- [var kBluetoothL2CAPCommandRejectReasonInvalidCIDInRequest: BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/kbluetoothl2capcommandrejectreasoninvalidcidinrequest)
- [var kBluetoothL2CAPCommandRejectReasonSignallingMTUExceeded: BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/kbluetoothl2capcommandrejectreasonsignallingmtuexceeded)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capcommandrejectreason/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capcommandrejectreason/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capcommandrejectreason/rawvalue)
- [BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/bluetoothl2capconfigurationoption)

#### Constants

- [var kBluetoothL2CAPConfigurationOptionExtendedFlowSpecification: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionextendedflowspecification)
- [var kBluetoothL2CAPConfigurationOptionExtendedWindowSize: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionextendedwindowsize)
- [var kBluetoothL2CAPConfigurationOptionFlushTimeout: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionflushtimeout)
- [var kBluetoothL2CAPConfigurationOptionFrameCheckSequence: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionframechecksequence)
- [var kBluetoothL2CAPConfigurationOptionMTU: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionmtu)
- [var kBluetoothL2CAPConfigurationOptionQoS: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionqos)
- [var kBluetoothL2CAPConfigurationOptionRetransmissionAndFlowControl: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionretransmissionandflowcontrol)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationoption/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationoption/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconfigurationoption/rawvalue)
- [BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/bluetoothl2capconfigurationresult)

#### Constants

- [var kBluetoothL2CAPConfigurationResultRejected: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultrejected)
- [var kBluetoothL2CAPConfigurationResultSuccess: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultsuccess)
- [var kBluetoothL2CAPConfigurationResultUnacceptableParams: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultunacceptableparams)
- [var kBluetoothL2CAPConfigurationResultUnknownOptions: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultunknownoptions)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationresult/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationresult/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconfigurationresult/rawvalue)
- [BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags)

#### Constants

- [var kBluetoothL2CAPConfigurationBasicL2CAPModeFlag: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationbasicl2capmodeflag)
- [var kBluetoothL2CAPConfigurationEnhancedRetransmissionMode: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationenhancedretransmissionmode)
- [var kBluetoothL2CAPConfigurationFlowControlModeFlag: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationflowcontrolmodeflag)
- [var kBluetoothL2CAPConfigurationRetransmissionModeFlag: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationretransmissionmodeflag)
- [var kBluetoothL2CAPConfigurationStreamingMode: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationstreamingmode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags/rawvalue)
- [BluetoothL2CAPConnectionResult](/documentation/iobluetooth/bluetoothl2capconnectionresult)

#### Constants

- [var kBluetoothL2CAPConnectionResultPending: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultpending)
- [var kBluetoothL2CAPConnectionResultRefusedNoResources: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusednoresources)
- [var kBluetoothL2CAPConnectionResultRefusedPSMNotSupported: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedpsmnotsupported)
- [var kBluetoothL2CAPConnectionResultRefusedSecurityBlock: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedsecurityblock)
- [var kBluetoothL2CAPConnectionResultSuccessful: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultsuccessful)
- [var kBluetoothL2CAPConnectionResultRefusedInvalidSourceCID: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedinvalidsourcecid)
- [var kBluetoothL2CAPConnectionResultRefusedReserved: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedreserved)
- [var kBluetoothL2CAPConnectionResultRefusedSourceCIDAlreadyAllocated: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedsourcecidalreadyallocated)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionresult/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionresult/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconnectionresult/rawvalue)
- [BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/bluetoothl2capconnectionstatus)

#### Constants

- [var kBluetoothL2CAPConnectionStatusAuthenticationPending: BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/kbluetoothl2capconnectionstatusauthenticationpending)
- [var kBluetoothL2CAPConnectionStatusAuthorizationPending: BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/kbluetoothl2capconnectionstatusauthorizationpending)
- [var kBluetoothL2CAPConnectionStatusNoInfoAvailable: BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/kbluetoothl2capconnectionstatusnoinfoavailable)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionstatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionstatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconnectionstatus/rawvalue)
- [BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask)

#### Constants

- [var kBluetoothL2CAPInformationBidirectionalQoS: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationbidirectionalqos)
- [var kBluetoothL2CAPInformationEnhancedRetransmissionMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationenhancedretransmissionmode)
- [var kBluetoothL2CAPInformationExtendedFlowSpecification: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationextendedflowspecification)
- [var kBluetoothL2CAPInformationExtendedWindowSize: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationextendedwindowsize)
- [var kBluetoothL2CAPInformationFCSOption: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationfcsoption)
- [var kBluetoothL2CAPInformationFixedChannels: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationfixedchannels)
- [var kBluetoothL2CAPInformationFlowControlMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationflowcontrolmode)
- [var kBluetoothL2CAPInformationNoExtendedFeatures: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationnoextendedfeatures)
- [var kBluetoothL2CAPInformationRetransmissionMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationretransmissionmode)
- [var kBluetoothL2CAPInformationStreamingMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationstreamingmode)
- [var kBluetoothL2CAPUnicastConnectionlessDataReception: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capunicastconnectionlessdatareception)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask/rawvalue)
- [BluetoothL2CAPInformationResult](/documentation/iobluetooth/bluetoothl2capinformationresult)

#### Constants

- [var kBluetoothL2CAPInformationResultNotSupported: BluetoothL2CAPInformationResult](/documentation/iobluetooth/kbluetoothl2capinformationresultnotsupported)
- [var kBluetoothL2CAPInformationResultSuccess: BluetoothL2CAPInformationResult](/documentation/iobluetooth/kbluetoothl2capinformationresultsuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capinformationresult/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capinformationresult/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capinformationresult/rawvalue)
- [BluetoothL2CAPInformationType](/documentation/iobluetooth/bluetoothl2capinformationtype)

#### Constants

- [var kBluetoothL2CAPInformationTypeConnectionlessMTU: BluetoothL2CAPInformationType](/documentation/iobluetooth/kbluetoothl2capinformationtypeconnectionlessmtu)
- [var kBluetoothL2CAPInformationTypeExtendedFeatures: BluetoothL2CAPInformationType](/documentation/iobluetooth/kbluetoothl2capinformationtypeextendedfeatures)
- [var kBluetoothL2CAPInformationTypeFixedChannelsSupported: BluetoothL2CAPInformationType](/documentation/iobluetooth/kbluetoothl2capinformationtypefixedchannelssupported)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capinformationtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capinformationtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capinformationtype/rawvalue)
- [BluetoothL2CAPQoSType](/documentation/iobluetooth/bluetoothl2capqostype)

#### Constants

- [var kBluetoothL2CAPQoSTypeBestEffort: BluetoothL2CAPQoSType](/documentation/iobluetooth/kbluetoothl2capqostypebesteffort)
- [var kBluetoothL2CAPQoSTypeGuaranteed: BluetoothL2CAPQoSType](/documentation/iobluetooth/kbluetoothl2capqostypeguaranteed)
- [var kBluetoothL2CAPQoSTypeNoTraffic: BluetoothL2CAPQoSType](/documentation/iobluetooth/kbluetoothl2capqostypenotraffic)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capqostype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capqostype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capqostype/rawvalue)
- [BluetoothL2CAPQualityOfServiceOptions](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/init())
- [init(flags: UInt8, serviceType: UInt8, tokenRate: UInt32, tokenBucketSize: UInt32, peakBandwidth: UInt32, latency: UInt32, delayVariation: UInt32)](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/init(flags:servicetype:tokenrate:tokenbucketsize:peakbandwidth:latency:delayvariation:))

#### Instance Properties

- [var delayVariation: UInt32](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/delayvariation)
- [var flags: UInt8](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/flags)
- [var latency: UInt32](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/latency)
- [var peakBandwidth: UInt32](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/peakbandwidth)
- [var serviceType: UInt8](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/servicetype)
- [var tokenBucketSize: UInt32](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/tokenbucketsize)
- [var tokenRate: UInt32](/documentation/iobluetooth/bluetoothl2capqualityofserviceoptions/tokenrate)
- [BluetoothL2CAPRetransmissionAndFlowControlOptions](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/init())
- [init(flags: UInt8, txWindowSize: UInt8, maxTransmit: UInt8, retransmissionTimeout: UInt16, monitorTimeout: UInt16, maxPDUPayloadSize: UInt16)](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/init(flags:txwindowsize:maxtransmit:retransmissiontimeout:monitortimeout:maxpdupayloadsize:))

#### Instance Properties

- [var flags: UInt8](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/flags)
- [var maxPDUPayloadSize: UInt16](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/maxpdupayloadsize)
- [var maxTransmit: UInt8](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/maxtransmit)
- [var monitorTimeout: UInt16](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/monitortimeout)
- [var retransmissionTimeout: UInt16](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/retransmissiontimeout)
- [var txWindowSize: UInt8](/documentation/iobluetooth/bluetoothl2capretransmissionandflowcontroloptions/txwindowsize)
- [BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly)

#### Constants

- [var kBluetoothL2CAPSegmentationAndReassemblyContinuationOfSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblycontinuationofsdu)
- [var kBluetoothL2CAPSegmentationAndReassemblyEndOfSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblyendofsdu)
- [var kBluetoothL2CAPSegmentationAndReassemblyStartOfSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblystartofsdu)
- [var kBluetoothL2CAPSegmentationAndReassemblyUnsegmentedSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblyunsegmentedsdu)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly/rawvalue)
- [BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype)

#### Constants

- [var kBluetoothL2CAPSupervisoryFuctionTypeReceiverNotReady: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypereceivernotready)
- [var kBluetoothL2CAPSupervisoryFuctionTypeReceiverReady: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypereceiverready)
- [var kBluetoothL2CAPSupervisoryFuctionTypeReject: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypereject)
- [var kBluetoothL2CAPSupervisoryFuctionTypeSelectiveReject: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypeselectivereject)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype/rawvalue)
- [BluetoothLEAddressType](/documentation/iobluetooth/bluetoothleaddresstype)

#### Constants

- [var BluetoothLEAddressTypePublic: BluetoothLEAddressType](/documentation/iobluetooth/bluetoothleaddresstypepublic)
- [var BluetoothLEAddressTypeRandom: BluetoothLEAddressType](/documentation/iobluetooth/bluetoothleaddresstyperandom)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothleaddresstype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothleaddresstype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothleaddresstype/rawvalue)
- [BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtype)

#### Constants

- [var BluetoothLEAdvertisingTypeConnectableDirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypeconnectabledirected)
- [var BluetoothLEAdvertisingTypeConnectableUndirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypeconnectableundirected)
- [var BluetoothLEAdvertisingTypeDiscoverableUndirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypediscoverableundirected)
- [var BluetoothLEAdvertisingTypeNonConnectableUndirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypenonconnectableundirected)
- [var BluetoothLEAdvertisingTypeScanResponse: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypescanresponse)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothleadvertisingtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothleadvertisingtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothleadvertisingtype/rawvalue)
- [BluetoothLEConnectionInterval](/documentation/iobluetooth/bluetoothleconnectioninterval)

#### Constants

- [var BluetoothLEConnectionIntervalMax: BluetoothLEConnectionInterval](/documentation/iobluetooth/bluetoothleconnectionintervalmax)
- [var BluetoothLEConnectionIntervalMin: BluetoothLEConnectionInterval](/documentation/iobluetooth/bluetoothleconnectionintervalmin)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothleconnectioninterval/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothleconnectioninterval/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothleconnectioninterval/rawvalue)
- [BluetoothLEFeatureBits](/documentation/iobluetooth/bluetoothlefeaturebits)

#### Constants

- [var kBluetoothLEFeatureConnectionParamsRequestProcedure: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureconnectionparamsrequestprocedure)
- [var kBluetoothLEFeatureExtendedRejectIndication: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureextendedrejectindication)
- [var kBluetoothLEFeatureExtendedScannerFilterPolicies: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureextendedscannerfilterpolicies)
- [var kBluetoothLEFeatureLEDataPacketLengthExtension: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureledatapacketlengthextension)
- [var kBluetoothLEFeatureLEEncryption: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureleencryption)
- [var kBluetoothLEFeatureLEPing: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureleping)
- [var kBluetoothLEFeatureLLPrivacy: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeaturellprivacy)
- [var kBluetoothLEFeatureSlaveInitiatedFeaturesExchange: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureslaveinitiatedfeaturesexchange)
- [var kBluetoothLEFeaturePeripheralInitiatedFeaturesExchange: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureperipheralinitiatedfeaturesexchange)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlefeaturebits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlefeaturebits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlefeaturebits/rawvalue)
- [BluetoothLEScan](/documentation/iobluetooth/bluetoothlescan)

#### Constants

- [var BluetoothLEScanDisable: BluetoothLEScan](/documentation/iobluetooth/bluetoothlescandisable)
- [var BluetoothLEScanEnable: BluetoothLEScan](/documentation/iobluetooth/bluetoothlescanenable)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescan/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescan/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescan/rawvalue)
- [BluetoothLEScanDuplicateFilter](/documentation/iobluetooth/bluetoothlescanduplicatefilter)

#### Constants

- [var BluetoothLEScanDuplicateFilterDisable: BluetoothLEScanDuplicateFilter](/documentation/iobluetooth/bluetoothlescanduplicatefilterdisable)
- [var BluetoothLEScanDuplicateFilterEnable: BluetoothLEScanDuplicateFilter](/documentation/iobluetooth/bluetoothlescanduplicatefilterenable)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescanduplicatefilter/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescanduplicatefilter/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescanduplicatefilter/rawvalue)
- [BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfilter)

#### Constants

- [var BluetoothLEScanFilterNone: BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfilternone)
- [var BluetoothLEScanFilterWhitelist: BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfilterwhitelist)
- [var BluetoothLEScanFilterSafelist: BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfiltersafelist)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescanfilter/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescanfilter/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescanfilter/rawvalue)
- [BluetoothLEScanType](/documentation/iobluetooth/bluetoothlescantype)

#### Constants

- [var BluetoothLEScanTypeActive: BluetoothLEScanType](/documentation/iobluetooth/bluetoothlescantypeactive)
- [var BluetoothLEScanTypePassive: BluetoothLEScanType](/documentation/iobluetooth/bluetoothlescantypepassive)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescantype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescantype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescantype/rawvalue)
- [BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode)

#### Constants

- [var kBluetoothLESecurityManagerCommandCodeEncryptionInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodeencryptioninfo)
- [var kBluetoothLESecurityManagerCommandCodeIdentityAddressInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodeidentityaddressinfo)
- [var kBluetoothLESecurityManagerCommandCodeIdentityInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodeidentityinfo)
- [var kBluetoothLESecurityManagerCommandCodeMasterIdentification: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodemasteridentification)
- [var kBluetoothLESecurityManagerCommandCodePairingConfirm: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingconfirm)
- [var kBluetoothLESecurityManagerCommandCodePairingDHKeyCheck: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingdhkeycheck)
- [var kBluetoothLESecurityManagerCommandCodePairingFailed: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingfailed)
- [var kBluetoothLESecurityManagerCommandCodePairingKeypressNotification: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingkeypressnotification)
- [var kBluetoothLESecurityManagerCommandCodePairingPublicKey: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingpublickey)
- [var kBluetoothLESecurityManagerCommandCodePairingRandom: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingrandom)
- [var kBluetoothLESecurityManagerCommandCodePairingRequest: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingrequest)
- [var kBluetoothLESecurityManagerCommandCodePairingResponse: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingresponse)
- [var kBluetoothLESecurityManagerCommandCodeReserved: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodereserved)
- [var kBluetoothLESecurityManagerCommandCodeReservedEnd: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodereservedend)
- [var kBluetoothLESecurityManagerCommandCodeReservedStart: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodereservedstart)
- [var kBluetoothLESecurityManagerCommandCodeSecurityRequest: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodesecurityrequest)
- [var kBluetoothLESecurityManagerCommandCodeSigningInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodesigninginfo)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode/rawvalue)
- [BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability)

#### Constants

- [var kBluetoothLESecurityManagerIOCapabilityDisplayOnly: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitydisplayonly)
- [var kBluetoothLESecurityManagerIOCapabilityDisplayYesNo: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitydisplayyesno)
- [var kBluetoothLESecurityManagerIOCapabilityKeyboardDisplay: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitykeyboarddisplay)
- [var kBluetoothLESecurityManagerIOCapabilityKeyboardOnly: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitykeyboardonly)
- [var kBluetoothLESecurityManagerIOCapabilityNoInputNoOutput: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitynoinputnooutput)
- [var kBluetoothLESecurityManagerIOCapabilityReservedEnd: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilityreservedend)
- [var kBluetoothLESecurityManagerIOCapabilityReservedStart: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilityreservedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability/rawvalue)
- [BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat)

#### Constants

- [var kBluetoothLESecurityManagerEncryptionKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanagerencryptionkey)
- [var kBluetoothLESecurityManagerIDKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanageridkey)
- [var kBluetoothLESecurityManagerLinkKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanagerlinkkey)
- [var kBluetoothLESecurityManagerSignKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanagersignkey)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat/rawvalue)
- [BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype)

#### Constants

- [var kBluetoothLESecurityManagerNotificationTypePasskeyCleared: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeycleared)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyDigitEntered: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeydigitentered)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyDigitErased: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeydigiterased)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyEntryCompleted: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeyentrycompleted)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyEntryStarted: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeyentrystarted)
- [var kBluetoothLESecurityManagerNotificationTypeReservedEnd: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypereservedend)
- [var kBluetoothLESecurityManagerNotificationTypeReservedStart: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypereservedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype/rawvalue)
- [BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata)

#### Constants

- [var kBluetoothLESecurityManagerOOBAuthenticationDataNotPresent: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobauthenticationdatanotpresent)
- [var kBluetoothLESecurityManagerOOBAuthenticationDataPresent: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobauthenticationdatapresent)
- [var kBluetoothLESecurityManagerOOBDataReservedEnd: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobdatareservedend)
- [var kBluetoothLESecurityManagerOOBDataReservedStart: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobdatareservedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata/rawvalue)
- [BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode)

#### Constants

- [var kBluetoothLESecurityManagerReasonCodeAuthenticationRequirements: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeauthenticationrequirements)
- [var kBluetoothLESecurityManagerReasonCodeBREDRPairingInProgress: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodebredrpairinginprogress)
- [var kBluetoothLESecurityManagerReasonCodeCommandNotSupported: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodecommandnotsupported)
- [var kBluetoothLESecurityManagerReasonCodeConfirmValueFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeconfirmvaluefailed)
- [var kBluetoothLESecurityManagerReasonCodeCrossTransportKeyDerivationGenerationNotAllowed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodecrosstransportkeyderivationgenerationnotallowed)
- [var kBluetoothLESecurityManagerReasonCodeDHKeyCheckFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodedhkeycheckfailed)
- [var kBluetoothLESecurityManagerReasonCodeEncryptionKeySize: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeencryptionkeysize)
- [var kBluetoothLESecurityManagerReasonCodeInvalidParameters: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeinvalidparameters)
- [var kBluetoothLESecurityManagerReasonCodeNumericComparisonFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodenumericcomparisonfailed)
- [var kBluetoothLESecurityManagerReasonCodeOOBNotAvailbale: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeoobnotavailbale)
- [var kBluetoothLESecurityManagerReasonCodePairingNotSupported: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodepairingnotsupported)
- [var kBluetoothLESecurityManagerReasonCodePasskeyEntryFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodepasskeyentryfailed)
- [var kBluetoothLESecurityManagerReasonCodeRepeatedAttempts: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncoderepeatedattempts)
- [var kBluetoothLESecurityManagerReasonCodeReserved: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodereserved)
- [var kBluetoothLESecurityManagerReasonCodeReservedEnd: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodereservedend)
- [var kBluetoothLESecurityManagerReasonCodeReservedStart: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodereservedstart)
- [var kBluetoothLESecurityManagerReasonCodeUnspecifiedReason: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeunspecifiedreason)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode/rawvalue)
- [BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability)

#### Constants

- [var kBluetoothLESecurityManagerUserInputCapabilityKeyboard: BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruserinputcapabilitykeyboard)
- [var kBluetoothLESecurityManagerUserInputCapabilityNoInput: BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruserinputcapabilitynoinput)
- [var kBluetoothLESecurityManagerUserInputCapabilityYesNo: BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruserinputcapabilityyesno)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability/rawvalue)
- [BluetoothLESecurityManagerUserOutputCapability](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability)

#### Constants

- [var kBluetoothLESecurityManagerUserOutputCapabilityNoOutput: BluetoothLESecurityManagerUserOutputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruseroutputcapabilitynooutput)
- [var kBluetoothLESecurityManagerUserOutputCapabilityNumericOutput: BluetoothLESecurityManagerUserOutputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruseroutputcapabilitynumericoutput)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability/rawvalue)
- [BluetoothLMPVersions](/documentation/iobluetooth/bluetoothlmpversions)

#### Constants

- [var kBluetoothLMPVersionCoreSpecification1_0b: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification1_0b)
- [var kBluetoothLMPVersionCoreSpecification1_1: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification1_1)
- [var kBluetoothLMPVersionCoreSpecification1_2: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification1_2)
- [var kBluetoothLMPVersionCoreSpecification2_0EDR: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification2_0edr)
- [var kBluetoothLMPVersionCoreSpecification2_1EDR: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification2_1edr)
- [var kBluetoothLMPVersionCoreSpecification3_0HS: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification3_0hs)
- [var kBluetoothLMPVersionCoreSpecification4_0: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification4_0)
- [var kBluetoothLMPVersionCoreSpecification4_1: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification4_1)
- [var kBluetoothLMPVersionCoreSpecification4_2: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification4_2)
- [var kBluetoothLMPVersionCoreSpecification5_0: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification5_0)
- [var kBluetoothLMPVersionCoreSpecification5_1: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification5_1)
- [var kBluetoothLMPVersionCoreSpecification5_2: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification5_2)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlmpversions/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlmpversions/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlmpversions/rawvalue)
- [BluetoothLinkTypes](/documentation/iobluetooth/bluetoothlinktypes)

#### Constants

- [var kBluetoothACLConnection: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothaclconnection)
- [var kBluetoothESCOConnection: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothescoconnection)
- [var kBluetoothLinkTypeNone: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothlinktypenone)
- [var kBluetoothSCOConnection: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothscoconnection)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlinktypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlinktypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlinktypes/rawvalue)
- [BluetoothOOBDataPresenceValues](/documentation/iobluetooth/bluetoothoobdatapresencevalues)

#### Constants

- [var kBluetoothOOBAuthenticationDataFromRemoteDevicePresent: BluetoothOOBDataPresenceValues](/documentation/iobluetooth/kbluetoothoobauthenticationdatafromremotedevicepresent)
- [var kBluetoothOOBAuthenticationDataNotPresent: BluetoothOOBDataPresenceValues](/documentation/iobluetooth/kbluetoothoobauthenticationdatanotpresent)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothoobdatapresencevalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothoobdatapresencevalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothoobdatapresencevalues/rawvalue)
- [BluetoothPINCode](/documentation/iobluetooth/bluetoothpincode)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothpincode/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothpincode/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothpincode/data)
- [BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatus)

#### Constants

- [var BluetoothRFCOMMLineStatusFramingError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusframingerror)
- [var BluetoothRFCOMMLineStatusNoError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusnoerror)
- [var BluetoothRFCOMMLineStatusOverrunError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusoverrunerror)
- [var BluetoothRFCOMMLineStatusParityError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusparityerror)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothrfcommlinestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothrfcommlinestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothrfcommlinestatus/rawvalue)
- [BluetoothRFCOMMParityType](/documentation/iobluetooth/bluetoothrfcommparitytype)

#### Constants

- [var kBluetoothRFCOMMParityTypeEvenParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypeevenparity)
- [var kBluetoothRFCOMMParityTypeMaxParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypemaxparity)
- [var kBluetoothRFCOMMParityTypeNoParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypenoparity)
- [var kBluetoothRFCOMMParityTypeOddParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypeoddparity)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothrfcommparitytype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothrfcommparitytype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothrfcommparitytype/rawvalue)
- [BluetoothReadClockInfo](/documentation/iobluetooth/bluetoothreadclockinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothreadclockinfo/init())
- [init(handle: BluetoothConnectionHandle, clock: UInt32, accuracy: UInt16)](/documentation/iobluetooth/bluetoothreadclockinfo/init(handle:clock:accuracy:))

#### Instance Properties

- [var accuracy: UInt16](/documentation/iobluetooth/bluetoothreadclockinfo/accuracy)
- [var clock: UInt32](/documentation/iobluetooth/bluetoothreadclockinfo/clock)
- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothreadclockinfo/handle)
- [BluetoothRemoteHostSupportedFeaturesNotification](/documentation/iobluetooth/bluetoothremotehostsupportedfeaturesnotification)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothremotehostsupportedfeaturesnotification/init())
- [init(deviceAddress: BluetoothDeviceAddress, hostSupportedFeatures: BluetoothHCISupportedFeatures)](/documentation/iobluetooth/bluetoothremotehostsupportedfeaturesnotification/init(deviceaddress:hostsupportedfeatures:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothremotehostsupportedfeaturesnotification/deviceaddress)
- [var hostSupportedFeatures: BluetoothHCISupportedFeatures](/documentation/iobluetooth/bluetoothremotehostsupportedfeaturesnotification/hostsupportedfeatures)
- [BluetoothSetEventMask](/documentation/iobluetooth/bluetoothseteventmask)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothseteventmask/init())
- [init(data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/iobluetooth/bluetoothseteventmask/init(data:))

#### Instance Properties

- [var data: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/iobluetooth/bluetoothseteventmask/data)
- [BluetoothSimplePairingDebugModes](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes)

#### Constants

- [var kBluetoothHCISimplePairingDebugModeDisabled: BluetoothSimplePairingDebugModes](/documentation/iobluetooth/kbluetoothhcisimplepairingdebugmodedisabled)
- [var kBluetoothHCISimplePairingDebugModeEnabled: BluetoothSimplePairingDebugModes](/documentation/iobluetooth/kbluetoothhcisimplepairingdebugmodeenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes/rawvalue)
- [BluetoothSynchronousConnectionInfo](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/init())
- [init(transmitBandWidth: BluetoothHCITransmitBandwidth, receiveBandWidth: BluetoothHCIReceiveBandwidth, maxLatency: BluetoothHCIMaxLatency, voiceSetting: BluetoothHCIVoiceSetting, retransmissionEffort: BluetoothHCIRetransmissionEffort, packetType: BluetoothPacketType)](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/init(transmitbandwidth:receivebandwidth:maxlatency:voicesetting:retransmissioneffort:packettype:))

#### Instance Properties

- [var maxLatency: BluetoothHCIMaxLatency](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/maxlatency)
- [var packetType: BluetoothPacketType](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/packettype)
- [var receiveBandWidth: BluetoothHCIReceiveBandwidth](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/receivebandwidth)
- [var retransmissionEffort: BluetoothHCIRetransmissionEffort](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/retransmissioneffort)
- [var transmitBandWidth: BluetoothHCITransmitBandwidth](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/transmitbandwidth)
- [var voiceSetting: BluetoothHCIVoiceSetting](/documentation/iobluetooth/bluetoothsynchronousconnectioninfo/voicesetting)
- [BluetoothTransportInfo](/documentation/iobluetooth/bluetoothtransportinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothtransportinfo/init())
- [init(productID: UInt32, vendorID: UInt32, type: UInt32, productName: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar), vendorName: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar), totalDataBytesSent: UInt64, totalSCOBytesSent: UInt64, totalDataBytesReceived: UInt64, totalSCOBytesReceived: UInt64)](/documentation/iobluetooth/bluetoothtransportinfo/init(productid:vendorid:type:productname:vendorname:totaldatabytessent:totalscobytessent:totaldatabytesreceived:totalscobytesreceived:))

#### Instance Properties

- [var productID: UInt32](/documentation/iobluetooth/bluetoothtransportinfo/productid)
- [var productName: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar)](/documentation/iobluetooth/bluetoothtransportinfo/productname)
- [var totalDataBytesReceived: UInt64](/documentation/iobluetooth/bluetoothtransportinfo/totaldatabytesreceived)
- [var totalDataBytesSent: UInt64](/documentation/iobluetooth/bluetoothtransportinfo/totaldatabytessent)
- [var totalSCOBytesReceived: UInt64](/documentation/iobluetooth/bluetoothtransportinfo/totalscobytesreceived)
- [var totalSCOBytesSent: UInt64](/documentation/iobluetooth/bluetoothtransportinfo/totalscobytessent)
- [var type: UInt32](/documentation/iobluetooth/bluetoothtransportinfo/type)
- [var vendorID: UInt32](/documentation/iobluetooth/bluetoothtransportinfo/vendorid)
- [var vendorName: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar)](/documentation/iobluetooth/bluetoothtransportinfo/vendorname)
- [BluetoothTransportTypes](/documentation/iobluetooth/bluetoothtransporttypes)

#### Constants

- [var kBluetoothTransportTypePCCard: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypepccard)
- [var kBluetoothTransportTypePCICard: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypepcicard)
- [var kBluetoothTransportTypeUART: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypeuart)
- [var kBluetoothTransportTypeUSB: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypeusb)
- [var kBluetoothTransportTypePCIe: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypepcie)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothtransporttypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothtransporttypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothtransporttypes/rawvalue)
- [BluetoothUserConfirmationRequest](/documentation/iobluetooth/bluetoothuserconfirmationrequest)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothuserconfirmationrequest/init())
- [init(deviceAddress: BluetoothDeviceAddress, numericValue: BluetoothNumericValue)](/documentation/iobluetooth/bluetoothuserconfirmationrequest/init(deviceaddress:numericvalue:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothuserconfirmationrequest/deviceaddress)
- [var numericValue: BluetoothNumericValue](/documentation/iobluetooth/bluetoothuserconfirmationrequest/numericvalue)
- [BluetoothUserPasskeyNotification](/documentation/iobluetooth/bluetoothuserpasskeynotification)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothuserpasskeynotification/init())
- [init(deviceAddress: BluetoothDeviceAddress, passkey: BluetoothPasskey)](/documentation/iobluetooth/bluetoothuserpasskeynotification/init(deviceaddress:passkey:))

#### Instance Properties

- [var deviceAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothuserpasskeynotification/deviceaddress)
- [var passkey: BluetoothPasskey](/documentation/iobluetooth/bluetoothuserpasskeynotification/passkey)
- [FTSFileType](/documentation/iobluetooth/ftsfiletype)

#### Constants

- [var kFTSFileTypeFile: FTSFileType](/documentation/iobluetooth/kftsfiletypefile)
- [var kFTSFileTypeFolder: FTSFileType](/documentation/iobluetooth/kftsfiletypefolder)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/ftsfiletype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/ftsfiletype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/ftsfiletype/rawvalue)
- [IOBluetoothDeviceSearchAttributes](/documentation/iobluetooth/iobluetoothdevicesearchattributes)

#### Initializers

- [init()](/documentation/iobluetooth/iobluetoothdevicesearchattributes/init())
- [init(options: IOBluetoothDeviceSearchOptions, maxResults: IOItemCount, deviceAttributeCount: IOItemCount, attributeList: UnsafeMutablePointer<IOBluetoothDeviceSearchDeviceAttributes>!)](/documentation/iobluetooth/iobluetoothdevicesearchattributes/init(options:maxresults:deviceattributecount:attributelist:))

#### Instance Properties

- [var attributeList: UnsafeMutablePointer<IOBluetoothDeviceSearchDeviceAttributes>!](/documentation/iobluetooth/iobluetoothdevicesearchattributes/attributelist)
- [var deviceAttributeCount: IOItemCount](/documentation/iobluetooth/iobluetoothdevicesearchattributes/deviceattributecount)
- [var maxResults: IOItemCount](/documentation/iobluetooth/iobluetoothdevicesearchattributes/maxresults)
- [var options: IOBluetoothDeviceSearchOptions](/documentation/iobluetooth/iobluetoothdevicesearchattributes/options)
- [IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits)

#### Constants

- [var kSearchOptionsAlwaysStartInquiry: IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/ksearchoptionsalwaysstartinquiry)
- [var kSearchOptionsDiscardCachedResults: IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/ksearchoptionsdiscardcachedresults)
- [var kSearchOptionsNone: IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/ksearchoptionsnone)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits/rawvalue)
- [IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits)

#### Constants

- [var kIOBluetoothDeviceSearchClassic: IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/kiobluetoothdevicesearchclassic)
- [var kIOBluetoothDeviceSearchLE: IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/kiobluetoothdevicesearchle)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/rawvalue)
- [IOBluetoothL2CAPChannelDataBlock](/documentation/iobluetooth/iobluetoothl2capchanneldatablock)

#### Initializers

- [init()](/documentation/iobluetooth/iobluetoothl2capchanneldatablock/init())
- [init(dataPtr: UnsafeMutableRawPointer!, dataSize: Int)](/documentation/iobluetooth/iobluetoothl2capchanneldatablock/init(dataptr:datasize:))

#### Instance Properties

- [var dataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/iobluetoothl2capchanneldatablock/dataptr)
- [var dataSize: Int](/documentation/iobluetooth/iobluetoothl2capchanneldatablock/datasize)
- [IOBluetoothL2CAPChannelEvent](/documentation/iobluetooth/iobluetoothl2capchannelevent)

#### Initializers

- [init()](/documentation/iobluetooth/iobluetoothl2capchannelevent/init())
- [init(eventType: IOBluetoothL2CAPChannelEventType, u: IOBluetoothL2CAPChannelEvent.__Unnamed_union_u, status: IOReturn)](/documentation/iobluetooth/iobluetoothl2capchannelevent/init(eventtype:u:status:))

#### Instance Properties

- [var eventType: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/iobluetoothl2capchannelevent/eventtype)
- [var status: IOReturn](/documentation/iobluetooth/iobluetoothl2capchannelevent/status)
- [var u: IOBluetoothL2CAPChannelEvent.__Unnamed_union_u](/documentation/iobluetooth/iobluetoothl2capchannelevent/u)
- [IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/iobluetoothl2capchanneleventtype)

#### Constants

- [var kIOBluetoothL2CAPChannelEventTypeClosed: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypeclosed)
- [var kIOBluetoothL2CAPChannelEventTypeData: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypedata)
- [var kIOBluetoothL2CAPChannelEventTypeOpenComplete: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypeopencomplete)
- [var kIOBluetoothL2CAPChannelEventTypeQueueSpaceAvailable: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypequeuespaceavailable)
- [var kIOBluetoothL2CAPChannelEventTypeReconfigured: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypereconfigured)
- [var kIOBluetoothL2CAPChannelEventTypeWriteComplete: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypewritecomplete)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothl2capchanneleventtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothl2capchanneleventtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothl2capchanneleventtype/rawvalue)
- [IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection)

#### Constants

- [var kIOBluetoothUserNotificationChannelDirectionAny: IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/kiobluetoothusernotificationchanneldirectionany)
- [var kIOBluetoothUserNotificationChannelDirectionIncoming: IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/kiobluetoothusernotificationchanneldirectionincoming)
- [var kIOBluetoothUserNotificationChannelDirectionOutgoing: IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/kiobluetoothusernotificationchanneldirectionoutgoing)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection/rawvalue)
- [OBEXConnectFlagValues](/documentation/iobluetooth/obexconnectflagvalues)

#### Constants

- [var kOBEXConnectFlag1Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag1reserved)
- [var kOBEXConnectFlag2Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag2reserved)
- [var kOBEXConnectFlag3Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag3reserved)
- [var kOBEXConnectFlag4Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag4reserved)
- [var kOBEXConnectFlag5Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag5reserved)
- [var kOBEXConnectFlag6Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag6reserved)
- [var kOBEXConnectFlag7Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag7reserved)
- [var kOBEXConnectFlagNone: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflagnone)
- [var kOBEXConnectFlagSupportMultipleItLMPConnections: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflagsupportmultipleitlmpconnections)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexconnectflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexconnectflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexconnectflagvalues/rawvalue)
- [OBEXErrorCodes](/documentation/iobluetooth/obexerrorcodes)

#### Constants

- [var kOBEXBadArgumentError: OBEXErrorCodes](/documentation/iobluetooth/kobexbadargumenterror)
- [var kOBEXBadRequestError: OBEXErrorCodes](/documentation/iobluetooth/kobexbadrequesterror)
- [var kOBEXCancelledError: OBEXErrorCodes](/documentation/iobluetooth/kobexcancellederror)
- [var kOBEXConflictError: OBEXErrorCodes](/documentation/iobluetooth/kobexconflicterror)
- [var kOBEXErrorRangeMax: OBEXErrorCodes](/documentation/iobluetooth/kobexerrorrangemax)
- [var kOBEXErrorRangeMin: OBEXErrorCodes](/documentation/iobluetooth/kobexerrorrangemin)
- [var kOBEXForbiddenError: OBEXErrorCodes](/documentation/iobluetooth/kobexforbiddenerror)
- [var kOBEXGeneralError: OBEXErrorCodes](/documentation/iobluetooth/kobexgeneralerror)
- [var kOBEXInternalError: OBEXErrorCodes](/documentation/iobluetooth/kobexinternalerror)
- [var kOBEXMethodNotAllowedError: OBEXErrorCodes](/documentation/iobluetooth/kobexmethodnotallowederror)
- [var kOBEXNoResourcesError: OBEXErrorCodes](/documentation/iobluetooth/kobexnoresourceserror)
- [var kOBEXNotAcceptableError: OBEXErrorCodes](/documentation/iobluetooth/kobexnotacceptableerror)
- [var kOBEXNotFoundError: OBEXErrorCodes](/documentation/iobluetooth/kobexnotfounderror)
- [var kOBEXNotImplementedError: OBEXErrorCodes](/documentation/iobluetooth/kobexnotimplementederror)
- [var kOBEXPreconditionFailedError: OBEXErrorCodes](/documentation/iobluetooth/kobexpreconditionfailederror)
- [var kOBEXSessionAlreadyConnectedError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionalreadyconnectederror)
- [var kOBEXSessionBadRequestError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionbadrequesterror)
- [var kOBEXSessionBadResponseError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionbadresponseerror)
- [var kOBEXSessionBusyError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionbusyerror)
- [var kOBEXSessionNoTransportError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionnotransporterror)
- [var kOBEXSessionNotConnectedError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionnotconnectederror)
- [var kOBEXSessionTimeoutError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessiontimeouterror)
- [var kOBEXSessionTransportDiedError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessiontransportdiederror)
- [var kOBEXSuccess: OBEXErrorCodes](/documentation/iobluetooth/kobexsuccess)
- [var kOBEXTimeoutError: OBEXErrorCodes](/documentation/iobluetooth/kobextimeouterror)
- [var kOBEXUnauthorizedError: OBEXErrorCodes](/documentation/iobluetooth/kobexunauthorizederror)
- [var kOBEXUnsupportedError: OBEXErrorCodes](/documentation/iobluetooth/kobexunsupportederror)

#### Initializers

- [init(Int32)](/documentation/iobluetooth/obexerrorcodes/init(_:))
- [init(rawValue: Int32)](/documentation/iobluetooth/obexerrorcodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: Int32](/documentation/iobluetooth/obexerrorcodes/rawvalue)
- [OBEXHeaderIdentifiers](/documentation/iobluetooth/obexheaderidentifiers)

#### Constants

- [var kOBEXHeaderIDAppParameters: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidappparameters)
- [var kOBEXHeaderIDAuthorizationChallenge: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidauthorizationchallenge)
- [var kOBEXHeaderIDAuthorizationResponse: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidauthorizationresponse)
- [var kOBEXHeaderIDBody: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidbody)
- [var kOBEXHeaderIDConnectionID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidconnectionid)
- [var kOBEXHeaderIDCount: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidcount)
- [var kOBEXHeaderIDDescription: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiddescription)
- [var kOBEXHeaderIDEndOfBody: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidendofbody)
- [var kOBEXHeaderIDHTTP: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidhttp)
- [var kOBEXHeaderIDLength: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidlength)
- [var kOBEXHeaderIDName: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidname)
- [var kOBEXHeaderIDOBEX13CreatorID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13creatorid)
- [var kOBEXHeaderIDOBEX13ObjectClass: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13objectclass)
- [var kOBEXHeaderIDOBEX13SessionParameters: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13sessionparameters)
- [var kOBEXHeaderIDOBEX13SessionSequenceNumber: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13sessionsequencenumber)
- [var kOBEXHeaderIDOBEX13WANUUID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13wanuuid)
- [var kOBEXHeaderIDObjectClass: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobjectclass)
- [var kOBEXHeaderIDReservedRangeEnd: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidreservedrangeend)
- [var kOBEXHeaderIDReservedRangeStart: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidreservedrangestart)
- [var kOBEXHeaderIDTarget: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtarget)
- [var kOBEXHeaderIDTime4Byte: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtime4byte)
- [var kOBEXHeaderIDTimeISO: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtimeiso)
- [var kOBEXHeaderIDType: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtype)
- [var kOBEXHeaderIDUserDefinedRangeEnd: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiduserdefinedrangeend)
- [var kOBEXHeaderIDUserDefinedRangeStart: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiduserdefinedrangestart)
- [var kOBEXHeaderIDWho: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidwho)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexheaderidentifiers/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexheaderidentifiers/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexheaderidentifiers/rawvalue)
- [OBEXNonceFlagValues](/documentation/iobluetooth/obexnonceflagvalues)

#### Constants

- [var kOBEXNonceFlag2Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag2reserved)
- [var kOBEXNonceFlag3Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag3reserved)
- [var kOBEXNonceFlag4Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag4reserved)
- [var kOBEXNonceFlag5Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag5reserved)
- [var kOBEXNonceFlag6Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag6reserved)
- [var kOBEXNonceFlag7Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag7reserved)
- [var kOBEXNonceFlagAccessModeReadOnly: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagaccessmodereadonly)
- [var kOBEXNonceFlagNone: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagnone)
- [var kOBEXNonceFlagSendUserIDInResponse: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagsenduseridinresponse)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexnonceflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexnonceflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexnonceflagvalues/rawvalue)
- [OBEXOpCodeCommandValues](/documentation/iobluetooth/obexopcodecommandvalues)

#### Constants

- [var kOBEXOpCodeAbort: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeabort)
- [var kOBEXOpCodeConnect: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeconnect)
- [var kOBEXOpCodeDisconnect: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodedisconnect)
- [var kOBEXOpCodeGet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeget)
- [var kOBEXOpCodeGetWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodegetwithhighbitset)
- [var kOBEXOpCodePut: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeput)
- [var kOBEXOpCodePutWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeputwithhighbitset)
- [var kOBEXOpCodeReserved: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereserved)
- [var kOBEXOpCodeReservedRangeEnd: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedrangeend)
- [var kOBEXOpCodeReservedRangeStart: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedrangestart)
- [var kOBEXOpCodeReservedWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedwithhighbitset)
- [var kOBEXOpCodeSetPath: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodesetpath)
- [var kOBEXOpCodeUserDefinedEnd: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeuserdefinedend)
- [var kOBEXOpCodeUserDefinedStart: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeuserdefinedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcodecommandvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcodecommandvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcodecommandvalues/rawvalue)
- [OBEXOpCodeResponseValues](/documentation/iobluetooth/obexopcoderesponsevalues)

#### Constants

- [var kOBEXResponseCodeAccepted: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeaccepted)
- [var kOBEXResponseCodeAcceptedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeacceptedwithfinalbit)
- [var kOBEXResponseCodeBadGateway: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadgateway)
- [var kOBEXResponseCodeBadGatewayWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadgatewaywithfinalbit)
- [var kOBEXResponseCodeBadRequest: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadrequest)
- [var kOBEXResponseCodeBadRequestWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadrequestwithfinalbit)
- [var kOBEXResponseCodeConflict: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeconflict)
- [var kOBEXResponseCodeConflictWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeconflictwithfinalbit)
- [var kOBEXResponseCodeContinue: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecontinue)
- [var kOBEXResponseCodeContinueWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecontinuewithfinalbit)
- [var kOBEXResponseCodeCreated: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecreated)
- [var kOBEXResponseCodeCreatedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecreatedwithfinalbit)
- [var kOBEXResponseCodeDatabaseFull: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabasefull)
- [var kOBEXResponseCodeDatabaseFullWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabasefullwithfinalbit)
- [var kOBEXResponseCodeDatabaseLocked: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabaselocked)
- [var kOBEXResponseCodeDatabaseLockedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabaselockedwithfinalbit)
- [var kOBEXResponseCodeForbidden: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeforbidden)
- [var kOBEXResponseCodeForbiddenWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeforbiddenwithfinalbit)
- [var kOBEXResponseCodeGatewayTimeout: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegatewaytimeout)
- [var kOBEXResponseCodeGatewayTimeoutWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegatewaytimeoutwithfinalbit)
- [var kOBEXResponseCodeGone: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegone)
- [var kOBEXResponseCodeGoneWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegonewithfinalbit)
- [var kOBEXResponseCodeHTTPVersionNotSupported: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodehttpversionnotsupported)
- [var kOBEXResponseCodeHTTPVersionNotSupportedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodehttpversionnotsupportedwithfinalbit)
- [var kOBEXResponseCodeInternalServerError: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeinternalservererror)
- [var kOBEXResponseCodeInternalServerErrorWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeinternalservererrorwithfinalbit)
- [var kOBEXResponseCodeLengthRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodelengthrequired)
- [var kOBEXResponseCodeLengthRequiredFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodelengthrequiredfinalbit)
- [var kOBEXResponseCodeMethodNotAllowed: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemethodnotallowed)
- [var kOBEXResponseCodeMethodNotAllowedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemethodnotallowedwithfinalbit)
- [var kOBEXResponseCodeMovedPermanently: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedpermanently)
- [var kOBEXResponseCodeMovedPermanentlyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedpermanentlywithfinalbit)
- [var kOBEXResponseCodeMovedTemporarily: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedtemporarily)
- [var kOBEXResponseCodeMovedTemporarilyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedtemporarilywithfinalbit)
- [var kOBEXResponseCodeMultipleChoices: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemultiplechoices)
- [var kOBEXResponseCodeMultipleChoicesWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemultiplechoiceswithfinalbit)
- [var kOBEXResponseCodeNoContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenocontent)
- [var kOBEXResponseCodeNoContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenocontentwithfinalbit)
- [var kOBEXResponseCodeNonAuthoritativeInfo: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenonauthoritativeinfo)
- [var kOBEXResponseCodeNonAuthoritativeInfoWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenonauthoritativeinfowithfinalbit)
- [var kOBEXResponseCodeNotAcceptable: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotacceptable)
- [var kOBEXResponseCodeNotAcceptableWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotacceptablewithfinalbit)
- [var kOBEXResponseCodeNotFound: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotfound)
- [var kOBEXResponseCodeNotFoundWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotfoundwithfinalbit)
- [var kOBEXResponseCodeNotImplemented: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotimplemented)
- [var kOBEXResponseCodeNotImplementedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotimplementedwithfinalbit)
- [var kOBEXResponseCodeNotModified: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotmodified)
- [var kOBEXResponseCodeNotModifiedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotmodifiedwithfinalbit)
- [var kOBEXResponseCodePartialContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepartialcontent)
- [var kOBEXResponseCodePartialContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepartialcontentwithfinalbit)
- [var kOBEXResponseCodePaymentRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepaymentrequired)
- [var kOBEXResponseCodePaymentRequiredWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepaymentrequiredwithfinalbit)
- [var kOBEXResponseCodePreconditionFailed: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepreconditionfailed)
- [var kOBEXResponseCodePreconditionFailedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepreconditionfailedwithfinalbit)
- [var kOBEXResponseCodeProxyAuthenticationRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeproxyauthenticationrequired)
- [var kOBEXResponseCodeProxyAuthenticationRequiredWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeproxyauthenticationrequiredwithfinalbit)
- [var kOBEXResponseCodeRequestTimeOut: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesttimeout)
- [var kOBEXResponseCodeRequestTimeOutWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesttimeoutwithfinalbit)
- [var kOBEXResponseCodeRequestURLTooLarge: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesturltoolarge)
- [var kOBEXResponseCodeRequestURLTooLargeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesturltoolargewithfinalbit)
- [var kOBEXResponseCodeRequestedEntityTooLarge: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequestedentitytoolarge)
- [var kOBEXResponseCodeRequestedEntityTooLargeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequestedentitytoolargewithfinalbit)
- [var kOBEXResponseCodeReservedRangeEnd: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodereservedrangeend)
- [var kOBEXResponseCodeReservedRangeStart: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodereservedrangestart)
- [var kOBEXResponseCodeResetContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderesetcontent)
- [var kOBEXResponseCodeResetContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderesetcontentwithfinalbit)
- [var kOBEXResponseCodeSeeOther: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeseeother)
- [var kOBEXResponseCodeSeeOtherWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeseeotherwithfinalbit)
- [var kOBEXResponseCodeServiceUnavailable: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeserviceunavailable)
- [var kOBEXResponseCodeServiceUnavailableWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeserviceunavailablewithfinalbit)
- [var kOBEXResponseCodeSuccess: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodesuccess)
- [var kOBEXResponseCodeSuccessWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodesuccesswithfinalbit)
- [var kOBEXResponseCodeUnauthorized: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunauthorized)
- [var kOBEXResponseCodeUnauthorizedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunauthorizedwithfinalbit)
- [var kOBEXResponseCodeUnsupportedMediaType: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunsupportedmediatype)
- [var kOBEXResponseCodeUnsupportedMediaTypeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunsupportedmediatypewithfinalbit)
- [var kOBEXResponseCodeUseProxy: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeuseproxy)
- [var kOBEXResponseCodeUseProxyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeuseproxywithfinalbit)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcoderesponsevalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcoderesponsevalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcoderesponsevalues/rawvalue)
- [OBEXOpCodeSessionValues](/documentation/iobluetooth/obexopcodesessionvalues)

#### Constants

- [var kOBEXOpCodeCloseSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodeclosesession)
- [var kOBEXOpCodeCreateSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodecreatesession)
- [var kOBEXOpCodeResumeSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcoderesumesession)
- [var kOBEXOpCodeSetTimeout: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodesettimeout)
- [var kOBEXOpCodeSuspendSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodesuspendsession)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcodesessionvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcodesessionvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcodesessionvalues/rawvalue)
- [OBEXPutFlagValues](/documentation/iobluetooth/obexputflagvalues)

#### Constants

- [var kOBEXPutFlag2Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag2reserved)
- [var kOBEXPutFlag3Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag3reserved)
- [var kOBEXPutFlag4Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag4reserved)
- [var kOBEXPutFlag5Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag5reserved)
- [var kOBEXPutFlag6Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag6reserved)
- [var kOBEXPutFlag7Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag7reserved)
- [var kOBEXPutFlagDontCreateDirectory: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflagdontcreatedirectory)
- [var kOBEXPutFlagGoToParentDirFirst: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflaggotoparentdirfirst)
- [var kOBEXPutFlagNone: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflagnone)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexputflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexputflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexputflagvalues/rawvalue)
- [OBEXRealmValues](/documentation/iobluetooth/obexrealmvalues)

#### Constants

- [var kOBEXRealmASCII: OBEXRealmValues](/documentation/iobluetooth/kobexrealmascii)
- [var kOBEXRealmISO88591: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88591)
- [var kOBEXRealmISO88592: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88592)
- [var kOBEXRealmISO88593: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88593)
- [var kOBEXRealmISO88594: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88594)
- [var kOBEXRealmISO88595: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88595)
- [var kOBEXRealmISO88596: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88596)
- [var kOBEXRealmISO88597: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88597)
- [var kOBEXRealmISO88598: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88598)
- [var kOBEXRealmISO88599: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88599)
- [var kOBEXRealmUNICODE: OBEXRealmValues](/documentation/iobluetooth/kobexrealmunicode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexrealmvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexrealmvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexrealmvalues/rawvalue)
- [OBEXSessionEventTypes](/documentation/iobluetooth/obexsessioneventtypes)

#### Constants

- [var kOBEXSessionEventTypeAbortCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeabortcommandreceived)
- [var kOBEXSessionEventTypeAbortCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeabortcommandresponsereceived)
- [var kOBEXSessionEventTypeConnectCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeconnectcommandreceived)
- [var kOBEXSessionEventTypeConnectCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeconnectcommandresponsereceived)
- [var kOBEXSessionEventTypeDisconnectCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypedisconnectcommandreceived)
- [var kOBEXSessionEventTypeDisconnectCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypedisconnectcommandresponsereceived)
- [var kOBEXSessionEventTypeError: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeerror)
- [var kOBEXSessionEventTypeGetCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypegetcommandreceived)
- [var kOBEXSessionEventTypeGetCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypegetcommandresponsereceived)
- [var kOBEXSessionEventTypePutCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeputcommandreceived)
- [var kOBEXSessionEventTypePutCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeputcommandresponsereceived)
- [var kOBEXSessionEventTypeSetPathCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypesetpathcommandreceived)
- [var kOBEXSessionEventTypeSetPathCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypesetpathcommandresponsereceived)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexsessioneventtypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexsessioneventtypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexsessioneventtypes/rawvalue)
- [OBEXSessionParameterTags](/documentation/iobluetooth/obexsessionparametertags)

#### Constants

- [var kOBEXSessionParameterTagDeviceAddress: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagdeviceaddress)
- [var kOBEXSessionParameterTagNextSequenceNumber: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagnextsequencenumber)
- [var kOBEXSessionParameterTagNonce: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagnonce)
- [var kOBEXSessionParameterTagSessionID: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagsessionid)
- [var kOBEXSessionParameterTagSessionOpcode: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagsessionopcode)
- [var kOBEXSessionParameterTagTimeout: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagtimeout)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexsessionparametertags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexsessionparametertags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexsessionparametertags/rawvalue)
- [OBEXTransportEvent](/documentation/iobluetooth/obextransportevent)

#### Initializers

- [init()](/documentation/iobluetooth/obextransportevent/init())
- [init(type: OBEXTransportEventType, status: OBEXError, dataPtr: UnsafeMutableRawPointer!, dataLength: Int)](/documentation/iobluetooth/obextransportevent/init(type:status:dataptr:datalength:))

#### Instance Properties

- [var dataLength: Int](/documentation/iobluetooth/obextransportevent/datalength)
- [var dataPtr: UnsafeMutableRawPointer!](/documentation/iobluetooth/obextransportevent/dataptr)
- [var status: OBEXError](/documentation/iobluetooth/obextransportevent/status)
- [var type: OBEXTransportEventType](/documentation/iobluetooth/obextransportevent/type)
- [OBEXTransportEventTypes](/documentation/iobluetooth/obextransporteventtypes)

#### Constants

- [var kOBEXTransportEventTypeDataReceived: OBEXTransportEventTypes](/documentation/iobluetooth/kobextransporteventtypedatareceived)
- [var kOBEXTransportEventTypeStatus: OBEXTransportEventTypes](/documentation/iobluetooth/kobextransporteventtypestatus)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obextransporteventtypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obextransporteventtypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obextransporteventtypes/rawvalue)
- [OBEXVersions](/documentation/iobluetooth/obexversions)

#### Constants

- [var kOBEXVersion10: OBEXVersions](/documentation/iobluetooth/kobexversion10)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexversions/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexversions/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexversions/rawvalue)
- [ProtocolParameters](/documentation/iobluetooth/protocolparameters)

#### Constants

- [var kBluetoothSDPProtocolParameterBNEPSupportedNetworkPacketTypeList: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterbnepsupportednetworkpackettypelist)
- [var kBluetoothSDPProtocolParameterBNEPVersion: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterbnepversion)
- [var kBluetoothSDPProtocolParameterL2CAPPSM: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterl2cappsm)
- [var kBluetoothSDPProtocolParameterRFCOMMChannel: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterrfcommchannel)
- [var kBluetoothSDPProtocolParameterTCPPort: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparametertcpport)
- [var kBluetoothSDPProtocolParameterUDPPort: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterudpport)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/protocolparameters/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/protocolparameters/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/protocolparameters/rawvalue)
- [SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/sdpattributedeviceidentificationrecord)

#### Constants

- [var kBluetoothSDPAttributeDeviceIdentifierClientExecutableURL: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierclientexecutableurl)
- [var kBluetoothSDPAttributeDeviceIdentifierDocumentationURL: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierdocumentationurl)
- [var kBluetoothSDPAttributeDeviceIdentifierPrimaryRecord: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierprimaryrecord)
- [var kBluetoothSDPAttributeDeviceIdentifierProductID: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierproductid)
- [var kBluetoothSDPAttributeDeviceIdentifierReservedRangeEnd: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierreservedrangeend)
- [var kBluetoothSDPAttributeDeviceIdentifierReservedRangeStart: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierreservedrangestart)
- [var kBluetoothSDPAttributeDeviceIdentifierServiceDescription: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierservicedescription)
- [var kBluetoothSDPAttributeDeviceIdentifierSpecificationID: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierspecificationid)
- [var kBluetoothSDPAttributeDeviceIdentifierVendorID: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifiervendorid)
- [var kBluetoothSDPAttributeDeviceIdentifierVendorIDSource: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifiervendoridsource)
- [var kBluetoothSDPAttributeDeviceIdentifierVersion: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierversion)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/sdpattributedeviceidentificationrecord/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/sdpattributedeviceidentificationrecord/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/sdpattributedeviceidentificationrecord/rawvalue)
- [SDPAttributeIdentifierCodes](/documentation/iobluetooth/sdpattributeidentifiercodes)

#### Constants

- [var kBluetoothSDPAttributeIdentifierAdditionalProtocolsDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifieradditionalprotocolsdescriptorlist)
- [var kBluetoothSDPAttributeIdentifierAudioFeedbackSupport: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifieraudiofeedbacksupport)
- [var kBluetoothSDPAttributeIdentifierBluetoothProfileDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierbluetoothprofiledescriptorlist)
- [var kBluetoothSDPAttributeIdentifierBrowseGroupList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierbrowsegrouplist)
- [var kBluetoothSDPAttributeIdentifierClientExecutableURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierclientexecutableurl)
- [var kBluetoothSDPAttributeIdentifierDocumentationURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierdocumentationurl)
- [var kBluetoothSDPAttributeIdentifierExternalNetwork: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierexternalnetwork)
- [var kBluetoothSDPAttributeIdentifierFaxClass1Support: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierfaxclass1support)
- [var kBluetoothSDPAttributeIdentifierFaxClass2Support: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierfaxclass2support)
- [var kBluetoothSDPAttributeIdentifierFaxClass2_0Support: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierfaxclass2_0support)
- [var kBluetoothSDPAttributeIdentifierGroupID: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiergroupid)
- [var kBluetoothSDPAttributeIdentifierHIDBatteryPower: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidbatterypower)
- [var kBluetoothSDPAttributeIdentifierHIDBootDevice: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidbootdevice)
- [var kBluetoothSDPAttributeIdentifierHIDCountryCode: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidcountrycode)
- [var kBluetoothSDPAttributeIdentifierHIDDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhiddescriptorlist)
- [var kBluetoothSDPAttributeIdentifierHIDDeviceSubclass: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhiddevicesubclass)
- [var kBluetoothSDPAttributeIdentifierHIDLangIDBaseList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidlangidbaselist)
- [var kBluetoothSDPAttributeIdentifierHIDNormallyConnectable: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidnormallyconnectable)
- [var kBluetoothSDPAttributeIdentifierHIDParserVersion: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidparserversion)
- [var kBluetoothSDPAttributeIdentifierHIDProfileVersion: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidprofileversion)
- [var kBluetoothSDPAttributeIdentifierHIDReconnectInitiate: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidreconnectinitiate)
- [var kBluetoothSDPAttributeIdentifierHIDReleaseNumber: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidreleasenumber)
- [var kBluetoothSDPAttributeIdentifierHIDRemoteWake: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidremotewake)
- [var kBluetoothSDPAttributeIdentifierHIDSDPDisable: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidsdpdisable)
- [var kBluetoothSDPAttributeIdentifierHIDSSRHostMaxLatency: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidssrhostmaxlatency)
- [var kBluetoothSDPAttributeIdentifierHIDSSRHostMinTimeout: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidssrhostmintimeout)
- [var kBluetoothSDPAttributeIdentifierHIDSupervisionTimeout: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidsupervisiontimeout)
- [var kBluetoothSDPAttributeIdentifierHIDVirtualCable: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidvirtualcable)
- [var kBluetoothSDPAttributeIdentifierHomepageURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhomepageurl)
- [var kBluetoothSDPAttributeIdentifierIPSubnet: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifieripsubnet)
- [var kBluetoothSDPAttributeIdentifierIconURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiericonurl)
- [var kBluetoothSDPAttributeIdentifierLanguageBaseAttributeIDList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierlanguagebaseattributeidlist)
- [var kBluetoothSDPAttributeIdentifierMaxNetAccessRate: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiermaxnetaccessrate)
- [var kBluetoothSDPAttributeIdentifierNetAccessType: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiernetaccesstype)
- [var kBluetoothSDPAttributeIdentifierNetwork: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiernetwork)
- [var kBluetoothSDPAttributeIdentifierNetworkAddress: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiernetworkaddress)
- [var kBluetoothSDPAttributeIdentifierProtocolDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierprotocoldescriptorlist)
- [var kBluetoothSDPAttributeIdentifierProviderName: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierprovidername)
- [var kBluetoothSDPAttributeIdentifierRemoteAudioVolumeControl: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierremoteaudiovolumecontrol)
- [var kBluetoothSDPAttributeIdentifierSecurityDescription: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersecuritydescription)
- [var kBluetoothSDPAttributeIdentifierServiceAvailability: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceavailability)
- [var kBluetoothSDPAttributeIdentifierServiceClassIDList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceclassidlist)
- [var kBluetoothSDPAttributeIdentifierServiceDatabaseState: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicedatabasestate)
- [var kBluetoothSDPAttributeIdentifierServiceDescription: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicedescription)
- [var kBluetoothSDPAttributeIdentifierServiceID: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceid)
- [var kBluetoothSDPAttributeIdentifierServiceInfoTimeToLive: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceinfotimetolive)
- [var kBluetoothSDPAttributeIdentifierServiceName: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicename)
- [var kBluetoothSDPAttributeIdentifierServiceRecordHandle: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicerecordhandle)
- [var kBluetoothSDPAttributeIdentifierServiceRecordState: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicerecordstate)
- [var kBluetoothSDPAttributeIdentifierServiceVersion: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceversion)
- [var kBluetoothSDPAttributeIdentifierSupportedCapabilities: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupportedcapabilities)
- [var kBluetoothSDPAttributeIdentifierSupportedDataStoresList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupporteddatastoreslist)
- [var kBluetoothSDPAttributeIdentifierSupportedFeatures: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupportedfeatures)
- [var kBluetoothSDPAttributeIdentifierSupportedFunctions: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupportedfunctions)
- [var kBluetoothSDPAttributeIdentifierSupporterFormatsList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupporterformatslist)
- [var kBluetoothSDPAttributeIdentifierTotalImagingDataCapacity: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiertotalimagingdatacapacity)
- [var kBluetoothSDPAttributeIdentifierVersionNumberList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierversionnumberlist)
- [var kBluetoothSDPAttributeIdentifierWAPGateway: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierwapgateway)
- [var kBluetoothSDPAttributeIdentifierWAPStackType: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierwapstacktype)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/sdpattributeidentifiercodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/sdpattributeidentifiercodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/sdpattributeidentifiercodes/rawvalue)
- [SDPServiceClasses](/documentation/iobluetooth/sdpserviceclasses)

#### Constants

- [var kBluetoothSDPUUID16ServiceClassAVRemoteControl: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassavremotecontrol)
- [var kBluetoothSDPUUID16ServiceClassAVRemoteControlController: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassavremotecontrolcontroller)
- [var kBluetoothSDPUUID16ServiceClassAVRemoteControlTarget: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassavremotecontroltarget)
- [var kBluetoothSDPUUID16ServiceClassAdvancedAudioDistribution: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassadvancedaudiodistribution)
- [var kBluetoothSDPUUID16ServiceClassAudioSink: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassaudiosink)
- [var kBluetoothSDPUUID16ServiceClassAudioSource: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassaudiosource)
- [var kBluetoothSDPUUID16ServiceClassAudioVideo: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassaudiovideo)
- [var kBluetoothSDPUUID16ServiceClassBasicPrinting: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassbasicprinting)
- [var kBluetoothSDPUUID16ServiceClassBrowseGroupDescriptor: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassbrowsegroupdescriptor)
- [var kBluetoothSDPUUID16ServiceClassCommonISDNAccess: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasscommonisdnaccess)
- [var kBluetoothSDPUUID16ServiceClassCordlessTelephony: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasscordlesstelephony)
- [var kBluetoothSDPUUID16ServiceClassDialupNetworking: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassdialupnetworking)
- [var kBluetoothSDPUUID16ServiceClassDirectPrinting: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassdirectprinting)
- [var kBluetoothSDPUUID16ServiceClassDirectPrintingReferenceObjectsService: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassdirectprintingreferenceobjectsservice)
- [var kBluetoothSDPUUID16ServiceClassFax: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassfax)
- [var kBluetoothSDPUUID16ServiceClassGN: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgn)
- [var kBluetoothSDPUUID16ServiceClassGenericAudio: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenericaudio)
- [var kBluetoothSDPUUID16ServiceClassGenericFileTransfer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenericfiletransfer)
- [var kBluetoothSDPUUID16ServiceClassGenericNetworking: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenericnetworking)
- [var kBluetoothSDPUUID16ServiceClassGenericTelephony: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenerictelephony)
- [var kBluetoothSDPUUID16ServiceClassGlobalNavigationSatelliteSystem: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassglobalnavigationsatellitesystem)
- [var kBluetoothSDPUUID16ServiceClassGlobalNavigationSatelliteSystemServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassglobalnavigationsatellitesystemserver)
- [var kBluetoothSDPUUID16ServiceClassHCR_Print: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshcr_print)
- [var kBluetoothSDPUUID16ServiceClassHCR_Scan: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshcr_scan)
- [var kBluetoothSDPUUID16ServiceClassHandsFree: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshandsfree)
- [var kBluetoothSDPUUID16ServiceClassHandsFreeAudioGateway: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshandsfreeaudiogateway)
- [var kBluetoothSDPUUID16ServiceClassHardcopyCableReplacement: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshardcopycablereplacement)
- [var kBluetoothSDPUUID16ServiceClassHeadset: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassheadset)
- [var kBluetoothSDPUUID16ServiceClassHeadsetAudioGateway: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassheadsetaudiogateway)
- [var kBluetoothSDPUUID16ServiceClassHeadset_HS: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassheadset_hs)
- [var kBluetoothSDPUUID16ServiceClassHealthDevice: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshealthdevice)
- [var kBluetoothSDPUUID16ServiceClassHealthDeviceSink: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshealthdevicesink)
- [var kBluetoothSDPUUID16ServiceClassHealthDeviceSource: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshealthdevicesource)
- [var kBluetoothSDPUUID16ServiceClassHumanInterfaceDeviceService: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshumaninterfacedeviceservice)
- [var kBluetoothSDPUUID16ServiceClassImaging: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimaging)
- [var kBluetoothSDPUUID16ServiceClassImagingAutomaticArchive: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimagingautomaticarchive)
- [var kBluetoothSDPUUID16ServiceClassImagingReferencedObjects: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimagingreferencedobjects)
- [var kBluetoothSDPUUID16ServiceClassImagingResponder: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimagingresponder)
- [var kBluetoothSDPUUID16ServiceClassIntercom: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassintercom)
- [var kBluetoothSDPUUID16ServiceClassIrMCSync: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassirmcsync)
- [var kBluetoothSDPUUID16ServiceClassIrMCSyncCommand: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassirmcsynccommand)
- [var kBluetoothSDPUUID16ServiceClassLANAccessUsingPPP: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasslanaccessusingppp)
- [var kBluetoothSDPUUID16ServiceClassMessageAccessProfile: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassmessageaccessprofile)
- [var kBluetoothSDPUUID16ServiceClassMessageAccessServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassmessageaccessserver)
- [var kBluetoothSDPUUID16ServiceClassMessageNotificationServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassmessagenotificationserver)
- [var kBluetoothSDPUUID16ServiceClassNAP: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassnap)
- [var kBluetoothSDPUUID16ServiceClassOBEXFileTransfer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassobexfiletransfer)
- [var kBluetoothSDPUUID16ServiceClassOBEXObjectPush: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassobexobjectpush)
- [var kBluetoothSDPUUID16ServiceClassPANU: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasspanu)
- [var kBluetoothSDPUUID16ServiceClassPhonebookAccess: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassphonebookaccess)
- [var kBluetoothSDPUUID16ServiceClassPhonebookAccess_PCE: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassphonebookaccess_pce)
- [var kBluetoothSDPUUID16ServiceClassPhonebookAccess_PSE: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassphonebookaccess_pse)
- [var kBluetoothSDPUUID16ServiceClassPnPInformation: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasspnpinformation)
- [var kBluetoothSDPUUID16ServiceClassPrintingStatus: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassprintingstatus)
- [var kBluetoothSDPUUID16ServiceClassPublicBrowseGroup: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasspublicbrowsegroup)
- [var kBluetoothSDPUUID16ServiceClassReferencePrinting: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassreferenceprinting)
- [var kBluetoothSDPUUID16ServiceClassReflectedUI: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassreflectedui)
- [var kBluetoothSDPUUID16ServiceClassSIM_Access: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasssim_access)
- [var kBluetoothSDPUUID16ServiceClassSerialPort: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassserialport)
- [var kBluetoothSDPUUID16ServiceClassServiceDiscoveryServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassservicediscoveryserver)
- [var kBluetoothSDPUUID16ServiceClassUDI_MT: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassudi_mt)
- [var kBluetoothSDPUUID16ServiceClassUDI_TA: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassudi_ta)
- [var kBluetoothSDPUUID16ServiceClassVideoConferencingGW: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideoconferencinggw)
- [var kBluetoothSDPUUID16ServiceClassVideoDistribution: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideodistribution)
- [var kBluetoothSDPUUID16ServiceClassVideoSink: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideosink)
- [var kBluetoothSDPUUID16ServiceClassVideoSource: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideosource)
- [var kBluetoothSDPUUID16ServiceClassWAP: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasswap)
- [var kBluetoothSDPUUID16ServiceClassWAPClient: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasswapclient)
- [var kBluetoothSDPUUID16ServiceClassGATT: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgatt)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/sdpserviceclasses/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/sdpserviceclasses/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/sdpserviceclasses/rawvalue)
- [BluetoothHCIEncryptionKeySizeInfo](/documentation/iobluetooth/bluetoothhciencryptionkeysizeinfo)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhciencryptionkeysizeinfo/init())
- [init(handle: BluetoothConnectionHandle, keySize: BluetoothHCIEncryptionKeySize)](/documentation/iobluetooth/bluetoothhciencryptionkeysizeinfo/init(handle:keysize:))

#### Instance Properties

- [var handle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhciencryptionkeysizeinfo/handle)
- [var keySize: BluetoothHCIEncryptionKeySize](/documentation/iobluetooth/bluetoothhciencryptionkeysizeinfo/keysize)
- [BluetoothHCIEventLEEnhancedConnectionCompleteResults](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults)

#### Initializers

- [init()](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/init())
- [init(connectionHandle: BluetoothConnectionHandle, role: UInt8, peerAddressType: UInt8, peerAddress: BluetoothDeviceAddress, localResolvablePrivateAddress: BluetoothDeviceAddress, peerResolvablePrivateAddress: BluetoothDeviceAddress, connInterval: UInt16, connLatency: UInt16, supervisionTimeout: UInt16, masterClockAccuracy: UInt8)](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/init(connectionhandle:role:peeraddresstype:peeraddress:localresolvableprivateaddress:peerresolvableprivateaddress:conninterval:connlatency:supervisiontimeout:masterclockaccuracy:))

#### Instance Properties

- [var connInterval: UInt16](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/conninterval)
- [var connLatency: UInt16](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/connlatency)
- [var connectionHandle: BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/connectionhandle)
- [var localResolvablePrivateAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/localresolvableprivateaddress)
- [var masterClockAccuracy: UInt8](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/masterclockaccuracy)
- [var peerAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/peeraddress)
- [var peerAddressType: UInt8](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/peeraddresstype)
- [var peerResolvablePrivateAddress: BluetoothDeviceAddress](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/peerresolvableprivateaddress)
- [var role: UInt8](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/role)
- [var supervisionTimeout: UInt16](/documentation/iobluetooth/bluetoothhcieventleenhancedconnectioncompleteresults/supervisiontimeout)
- [IOBluetooth Enumerations](/documentation/iobluetooth/iobluetooth-enumerations)

### Enumerations

- [BluetoothAMPCommandRejectReason](/documentation/iobluetooth/bluetoothampcommandrejectreason)

#### Constants

- [var kBluetoothAMPManagerCommandRejectReasonCommandNotRecognized: BluetoothAMPCommandRejectReason](/documentation/iobluetooth/kbluetoothampmanagercommandrejectreasoncommandnotrecognized)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampcommandrejectreason/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampcommandrejectreason/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampcommandrejectreason/rawvalue)
- [BluetoothAMPCreatePhysicalLinkResponseStatus](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampcreatephysicallinkresponsestatus/rawvalue)
- [BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus)

#### Constants

- [var kBluetoothAMPManagerDisconnectPhysicalLinkResponseInvalidControllerID: BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/kbluetoothampmanagerdisconnectphysicallinkresponseinvalidcontrollerid)
- [var kBluetoothAMPManagerDisconnectPhysicalLinkResponseNoPhysicalLink: BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/kbluetoothampmanagerdisconnectphysicallinkresponsenophysicallink)
- [var kBluetoothAMPManagerDisconnectPhysicalLinkResponseSuccess: BluetoothAMPDisconnectPhysicalLinkResponseStatus](/documentation/iobluetooth/kbluetoothampmanagerdisconnectphysicallinkresponsesuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampdisconnectphysicallinkresponsestatus/rawvalue)
- [BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus)

#### Constants

- [var kBluetoothAMPManagerDiscoverResponseControllerStatusBluetoothOnly: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusbluetoothonly)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusFullCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusfullcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusHighCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatushighcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusLowCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatuslowcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusMediumCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusmediumcapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusNoCapacity: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatusnocapacity)
- [var kBluetoothAMPManagerDiscoverResponseControllerStatusPoweredDown: BluetoothAMPDiscoverResponseControllerStatus](/documentation/iobluetooth/kbluetoothampmanagerdiscoverresponsecontrollerstatuspowereddown)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampdiscoverresponsecontrollerstatus/rawvalue)
- [BluetoothAMPGetAssocResponseStatus](/documentation/iobluetooth/bluetoothampgetassocresponsestatus)

#### Constants

- [var kBluetoothAMPManagerGetAssocResponseInvalidControllerID: BluetoothAMPGetAssocResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetassocresponseinvalidcontrollerid)
- [var kBluetoothAMPManagerGetAssocResponseSuccess: BluetoothAMPGetAssocResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetassocresponsesuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampgetassocresponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampgetassocresponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampgetassocresponsestatus/rawvalue)
- [BluetoothAMPGetInfoResponseStatus](/documentation/iobluetooth/bluetoothampgetinforesponsestatus)

#### Constants

- [var kBluetoothAMPManagerGetInfoResponseInvalidControllerID: BluetoothAMPGetInfoResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetinforesponseinvalidcontrollerid)
- [var kBluetoothAMPManagerGetInfoResponseSuccess: BluetoothAMPGetInfoResponseStatus](/documentation/iobluetooth/kbluetoothampmanagergetinforesponsesuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampgetinforesponsestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampgetinforesponsestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampgetinforesponsestatus/rawvalue)
- [BluetoothAMPManagerCode](/documentation/iobluetooth/bluetoothampmanagercode)

#### Constants

- [var kBluetoothAMPManagerCodeAMPChangeNotify: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampchangenotify)
- [var kBluetoothAMPManagerCodeAMPChangeResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampchangeresponse)
- [var kBluetoothAMPManagerCodeAMPCommandReject: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampcommandreject)
- [var kBluetoothAMPManagerCodeAMPCreatePhysicalLinkRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampcreatephysicallinkrequest)
- [var kBluetoothAMPManagerCodeAMPCreatePhysicalLinkResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampcreatephysicallinkresponse)
- [var kBluetoothAMPManagerCodeAMPDisconnectPhysicalLinkRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdisconnectphysicallinkrequest)
- [var kBluetoothAMPManagerCodeAMPDisconnectPhysicalLinkResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdisconnectphysicallinkresponse)
- [var kBluetoothAMPManagerCodeAMPDiscoverRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdiscoverrequest)
- [var kBluetoothAMPManagerCodeAMPDiscoverResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampdiscoverresponse)
- [var kBluetoothAMPManagerCodeAMPGetAssocRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetassocrequest)
- [var kBluetoothAMPManagerCodeAMPGetAssocResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetassocresponse)
- [var kBluetoothAMPManagerCodeAMPGetInfoRequest: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetinforequest)
- [var kBluetoothAMPManagerCodeAMPGetInfoResponse: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodeampgetinforesponse)
- [var kBluetoothAMPManagerCodeReserved: BluetoothAMPManagerCode](/documentation/iobluetooth/kbluetoothampmanagercodereserved)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothampmanagercode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothampmanagercode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothampmanagercode/rawvalue)
- [BluetoothHCIPowerState](/documentation/iobluetooth/bluetoothhcipowerstate)

#### Constants

- [var kBluetoothHCIPowerStateOFF: BluetoothHCIPowerState](/documentation/iobluetooth/kbluetoothhcipowerstateoff)
- [var kBluetoothHCIPowerStateON: BluetoothHCIPowerState](/documentation/iobluetooth/kbluetoothhcipowerstateon)
- [var kBluetoothHCIPowerStateUnintialized: BluetoothHCIPowerState](/documentation/iobluetooth/kbluetoothhcipowerstateunintialized)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipowerstate/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipowerstate/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipowerstate/rawvalue)
- [BluetoothL2CAPCommandCode](/documentation/iobluetooth/bluetoothl2capcommandcode)

#### Constants

- [var kBluetoothL2CAPCommandCodeCommandReject: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodecommandreject)
- [var kBluetoothL2CAPCommandCodeConfigureRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconfigurerequest)
- [var kBluetoothL2CAPCommandCodeConfigureResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconfigureresponse)
- [var kBluetoothL2CAPCommandCodeConnectionParameterUpdateRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionparameterupdaterequest)
- [var kBluetoothL2CAPCommandCodeConnectionParameterUpdateResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionparameterupdateresponse)
- [var kBluetoothL2CAPCommandCodeConnectionRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionrequest)
- [var kBluetoothL2CAPCommandCodeConnectionResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeconnectionresponse)
- [var kBluetoothL2CAPCommandCodeCreateChannelRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodecreatechannelrequest)
- [var kBluetoothL2CAPCommandCodeCreateChannelResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodecreatechannelresponse)
- [var kBluetoothL2CAPCommandCodeDisconnectionRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodedisconnectionrequest)
- [var kBluetoothL2CAPCommandCodeDisconnectionResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodedisconnectionresponse)
- [var kBluetoothL2CAPCommandCodeEchoRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeechorequest)
- [var kBluetoothL2CAPCommandCodeEchoResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeechoresponse)
- [var kBluetoothL2CAPCommandCodeInformationRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeinformationrequest)
- [var kBluetoothL2CAPCommandCodeInformationResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeinformationresponse)
- [var kBluetoothL2CAPCommandCodeLECreditBasedConnectionRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodelecreditbasedconnectionrequest)
- [var kBluetoothL2CAPCommandCodeLECreditBasedConnectionResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodelecreditbasedconnectionresponse)
- [var kBluetoothL2CAPCommandCodeLEFlowControlCredit: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodeleflowcontrolcredit)
- [var kBluetoothL2CAPCommandCodeMoveChannelConfirmation: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelconfirmation)
- [var kBluetoothL2CAPCommandCodeMoveChannelConfirmationResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelconfirmationresponse)
- [var kBluetoothL2CAPCommandCodeMoveChannelRequest: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelrequest)
- [var kBluetoothL2CAPCommandCodeMoveChannelResponse: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodemovechannelresponse)
- [var kBluetoothL2CAPCommandCodeReserved: BluetoothL2CAPCommandCode](/documentation/iobluetooth/kbluetoothl2capcommandcodereserved)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capcommandcode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capcommandcode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capcommandcode/rawvalue)
- [BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/bluetoothl2capcommandrejectreason)

#### Constants

- [var kBluetoothL2CAPCommandRejectReasonCommandNotUnderstood: BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/kbluetoothl2capcommandrejectreasoncommandnotunderstood)
- [var kBluetoothL2CAPCommandRejectReasonInvalidCIDInRequest: BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/kbluetoothl2capcommandrejectreasoninvalidcidinrequest)
- [var kBluetoothL2CAPCommandRejectReasonSignallingMTUExceeded: BluetoothL2CAPCommandRejectReason](/documentation/iobluetooth/kbluetoothl2capcommandrejectreasonsignallingmtuexceeded)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capcommandrejectreason/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capcommandrejectreason/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capcommandrejectreason/rawvalue)
- [BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/bluetoothl2capconfigurationoption)

#### Constants

- [var kBluetoothL2CAPConfigurationOptionExtendedFlowSpecification: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionextendedflowspecification)
- [var kBluetoothL2CAPConfigurationOptionExtendedWindowSize: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionextendedwindowsize)
- [var kBluetoothL2CAPConfigurationOptionFlushTimeout: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionflushtimeout)
- [var kBluetoothL2CAPConfigurationOptionFrameCheckSequence: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionframechecksequence)
- [var kBluetoothL2CAPConfigurationOptionMTU: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionmtu)
- [var kBluetoothL2CAPConfigurationOptionQoS: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionqos)
- [var kBluetoothL2CAPConfigurationOptionRetransmissionAndFlowControl: BluetoothL2CAPConfigurationOption](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionretransmissionandflowcontrol)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationoption/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationoption/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconfigurationoption/rawvalue)
- [BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/bluetoothl2capconfigurationresult)

#### Constants

- [var kBluetoothL2CAPConfigurationResultRejected: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultrejected)
- [var kBluetoothL2CAPConfigurationResultSuccess: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultsuccess)
- [var kBluetoothL2CAPConfigurationResultUnacceptableParams: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultunacceptableparams)
- [var kBluetoothL2CAPConfigurationResultUnknownOptions: BluetoothL2CAPConfigurationResult](/documentation/iobluetooth/kbluetoothl2capconfigurationresultunknownoptions)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationresult/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationresult/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconfigurationresult/rawvalue)
- [BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags)

#### Constants

- [var kBluetoothL2CAPConfigurationBasicL2CAPModeFlag: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationbasicl2capmodeflag)
- [var kBluetoothL2CAPConfigurationEnhancedRetransmissionMode: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationenhancedretransmissionmode)
- [var kBluetoothL2CAPConfigurationFlowControlModeFlag: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationflowcontrolmodeflag)
- [var kBluetoothL2CAPConfigurationRetransmissionModeFlag: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationretransmissionmodeflag)
- [var kBluetoothL2CAPConfigurationStreamingMode: BluetoothL2CAPConfigurationRetransmissionAndFlowControlFlags](/documentation/iobluetooth/kbluetoothl2capconfigurationstreamingmode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconfigurationretransmissionandflowcontrolflags/rawvalue)
- [BluetoothL2CAPConnectionResult](/documentation/iobluetooth/bluetoothl2capconnectionresult)

#### Constants

- [var kBluetoothL2CAPConnectionResultPending: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultpending)
- [var kBluetoothL2CAPConnectionResultRefusedNoResources: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusednoresources)
- [var kBluetoothL2CAPConnectionResultRefusedPSMNotSupported: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedpsmnotsupported)
- [var kBluetoothL2CAPConnectionResultRefusedSecurityBlock: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedsecurityblock)
- [var kBluetoothL2CAPConnectionResultSuccessful: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultsuccessful)
- [var kBluetoothL2CAPConnectionResultRefusedInvalidSourceCID: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedinvalidsourcecid)
- [var kBluetoothL2CAPConnectionResultRefusedReserved: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedreserved)
- [var kBluetoothL2CAPConnectionResultRefusedSourceCIDAlreadyAllocated: BluetoothL2CAPConnectionResult](/documentation/iobluetooth/kbluetoothl2capconnectionresultrefusedsourcecidalreadyallocated)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionresult/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionresult/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconnectionresult/rawvalue)
- [BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/bluetoothl2capconnectionstatus)

#### Constants

- [var kBluetoothL2CAPConnectionStatusAuthenticationPending: BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/kbluetoothl2capconnectionstatusauthenticationpending)
- [var kBluetoothL2CAPConnectionStatusAuthorizationPending: BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/kbluetoothl2capconnectionstatusauthorizationpending)
- [var kBluetoothL2CAPConnectionStatusNoInfoAvailable: BluetoothL2CAPConnectionStatus](/documentation/iobluetooth/kbluetoothl2capconnectionstatusnoinfoavailable)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionstatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capconnectionstatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capconnectionstatus/rawvalue)
- [BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask)

#### Constants

- [var kBluetoothL2CAPInformationBidirectionalQoS: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationbidirectionalqos)
- [var kBluetoothL2CAPInformationEnhancedRetransmissionMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationenhancedretransmissionmode)
- [var kBluetoothL2CAPInformationExtendedFlowSpecification: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationextendedflowspecification)
- [var kBluetoothL2CAPInformationExtendedWindowSize: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationextendedwindowsize)
- [var kBluetoothL2CAPInformationFCSOption: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationfcsoption)
- [var kBluetoothL2CAPInformationFixedChannels: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationfixedchannels)
- [var kBluetoothL2CAPInformationFlowControlMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationflowcontrolmode)
- [var kBluetoothL2CAPInformationNoExtendedFeatures: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationnoextendedfeatures)
- [var kBluetoothL2CAPInformationRetransmissionMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationretransmissionmode)
- [var kBluetoothL2CAPInformationStreamingMode: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capinformationstreamingmode)
- [var kBluetoothL2CAPUnicastConnectionlessDataReception: BluetoothL2CAPInformationExtendedFeaturesMask](/documentation/iobluetooth/kbluetoothl2capunicastconnectionlessdatareception)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capinformationextendedfeaturesmask/rawvalue)
- [BluetoothL2CAPInformationResult](/documentation/iobluetooth/bluetoothl2capinformationresult)

#### Constants

- [var kBluetoothL2CAPInformationResultNotSupported: BluetoothL2CAPInformationResult](/documentation/iobluetooth/kbluetoothl2capinformationresultnotsupported)
- [var kBluetoothL2CAPInformationResultSuccess: BluetoothL2CAPInformationResult](/documentation/iobluetooth/kbluetoothl2capinformationresultsuccess)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capinformationresult/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capinformationresult/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capinformationresult/rawvalue)
- [BluetoothL2CAPInformationType](/documentation/iobluetooth/bluetoothl2capinformationtype)

#### Constants

- [var kBluetoothL2CAPInformationTypeConnectionlessMTU: BluetoothL2CAPInformationType](/documentation/iobluetooth/kbluetoothl2capinformationtypeconnectionlessmtu)
- [var kBluetoothL2CAPInformationTypeExtendedFeatures: BluetoothL2CAPInformationType](/documentation/iobluetooth/kbluetoothl2capinformationtypeextendedfeatures)
- [var kBluetoothL2CAPInformationTypeFixedChannelsSupported: BluetoothL2CAPInformationType](/documentation/iobluetooth/kbluetoothl2capinformationtypefixedchannelssupported)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capinformationtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capinformationtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capinformationtype/rawvalue)
- [BluetoothL2CAPQoSType](/documentation/iobluetooth/bluetoothl2capqostype)

#### Constants

- [var kBluetoothL2CAPQoSTypeBestEffort: BluetoothL2CAPQoSType](/documentation/iobluetooth/kbluetoothl2capqostypebesteffort)
- [var kBluetoothL2CAPQoSTypeGuaranteed: BluetoothL2CAPQoSType](/documentation/iobluetooth/kbluetoothl2capqostypeguaranteed)
- [var kBluetoothL2CAPQoSTypeNoTraffic: BluetoothL2CAPQoSType](/documentation/iobluetooth/kbluetoothl2capqostypenotraffic)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capqostype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capqostype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capqostype/rawvalue)
- [BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly)

#### Constants

- [var kBluetoothL2CAPSegmentationAndReassemblyContinuationOfSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblycontinuationofsdu)
- [var kBluetoothL2CAPSegmentationAndReassemblyEndOfSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblyendofsdu)
- [var kBluetoothL2CAPSegmentationAndReassemblyStartOfSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblystartofsdu)
- [var kBluetoothL2CAPSegmentationAndReassemblyUnsegmentedSDU: BluetoothL2CAPSegmentationAndReassembly](/documentation/iobluetooth/kbluetoothl2capsegmentationandreassemblyunsegmentedsdu)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capsegmentationandreassembly/rawvalue)
- [BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype)

#### Constants

- [var kBluetoothL2CAPSupervisoryFuctionTypeReceiverNotReady: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypereceivernotready)
- [var kBluetoothL2CAPSupervisoryFuctionTypeReceiverReady: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypereceiverready)
- [var kBluetoothL2CAPSupervisoryFuctionTypeReject: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypereject)
- [var kBluetoothL2CAPSupervisoryFuctionTypeSelectiveReject: BluetoothL2CAPSupervisoryFuctionType](/documentation/iobluetooth/kbluetoothl2capsupervisoryfuctiontypeselectivereject)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothl2capsupervisoryfuctiontype/rawvalue)
- [BluetoothLEAddressType](/documentation/iobluetooth/bluetoothleaddresstype)

#### Constants

- [var BluetoothLEAddressTypePublic: BluetoothLEAddressType](/documentation/iobluetooth/bluetoothleaddresstypepublic)
- [var BluetoothLEAddressTypeRandom: BluetoothLEAddressType](/documentation/iobluetooth/bluetoothleaddresstyperandom)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothleaddresstype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothleaddresstype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothleaddresstype/rawvalue)
- [BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtype)

#### Constants

- [var BluetoothLEAdvertisingTypeConnectableDirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypeconnectabledirected)
- [var BluetoothLEAdvertisingTypeConnectableUndirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypeconnectableundirected)
- [var BluetoothLEAdvertisingTypeDiscoverableUndirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypediscoverableundirected)
- [var BluetoothLEAdvertisingTypeNonConnectableUndirected: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypenonconnectableundirected)
- [var BluetoothLEAdvertisingTypeScanResponse: BluetoothLEAdvertisingType](/documentation/iobluetooth/bluetoothleadvertisingtypescanresponse)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothleadvertisingtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothleadvertisingtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothleadvertisingtype/rawvalue)
- [BluetoothLEConnectionInterval](/documentation/iobluetooth/bluetoothleconnectioninterval)

#### Constants

- [var BluetoothLEConnectionIntervalMax: BluetoothLEConnectionInterval](/documentation/iobluetooth/bluetoothleconnectionintervalmax)
- [var BluetoothLEConnectionIntervalMin: BluetoothLEConnectionInterval](/documentation/iobluetooth/bluetoothleconnectionintervalmin)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothleconnectioninterval/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothleconnectioninterval/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothleconnectioninterval/rawvalue)
- [BluetoothLEScan](/documentation/iobluetooth/bluetoothlescan)

#### Constants

- [var BluetoothLEScanDisable: BluetoothLEScan](/documentation/iobluetooth/bluetoothlescandisable)
- [var BluetoothLEScanEnable: BluetoothLEScan](/documentation/iobluetooth/bluetoothlescanenable)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescan/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescan/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescan/rawvalue)
- [BluetoothLEScanDuplicateFilter](/documentation/iobluetooth/bluetoothlescanduplicatefilter)

#### Constants

- [var BluetoothLEScanDuplicateFilterDisable: BluetoothLEScanDuplicateFilter](/documentation/iobluetooth/bluetoothlescanduplicatefilterdisable)
- [var BluetoothLEScanDuplicateFilterEnable: BluetoothLEScanDuplicateFilter](/documentation/iobluetooth/bluetoothlescanduplicatefilterenable)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescanduplicatefilter/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescanduplicatefilter/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescanduplicatefilter/rawvalue)
- [BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfilter)

#### Constants

- [var BluetoothLEScanFilterNone: BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfilternone)
- [var BluetoothLEScanFilterWhitelist: BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfilterwhitelist)
- [var BluetoothLEScanFilterSafelist: BluetoothLEScanFilter](/documentation/iobluetooth/bluetoothlescanfiltersafelist)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescanfilter/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescanfilter/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescanfilter/rawvalue)
- [BluetoothLEScanType](/documentation/iobluetooth/bluetoothlescantype)

#### Constants

- [var BluetoothLEScanTypeActive: BluetoothLEScanType](/documentation/iobluetooth/bluetoothlescantypeactive)
- [var BluetoothLEScanTypePassive: BluetoothLEScanType](/documentation/iobluetooth/bluetoothlescantypepassive)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlescantype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlescantype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlescantype/rawvalue)
- [BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode)

#### Constants

- [var kBluetoothLESecurityManagerCommandCodeEncryptionInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodeencryptioninfo)
- [var kBluetoothLESecurityManagerCommandCodeIdentityAddressInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodeidentityaddressinfo)
- [var kBluetoothLESecurityManagerCommandCodeIdentityInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodeidentityinfo)
- [var kBluetoothLESecurityManagerCommandCodeMasterIdentification: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodemasteridentification)
- [var kBluetoothLESecurityManagerCommandCodePairingConfirm: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingconfirm)
- [var kBluetoothLESecurityManagerCommandCodePairingDHKeyCheck: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingdhkeycheck)
- [var kBluetoothLESecurityManagerCommandCodePairingFailed: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingfailed)
- [var kBluetoothLESecurityManagerCommandCodePairingKeypressNotification: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingkeypressnotification)
- [var kBluetoothLESecurityManagerCommandCodePairingPublicKey: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingpublickey)
- [var kBluetoothLESecurityManagerCommandCodePairingRandom: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingrandom)
- [var kBluetoothLESecurityManagerCommandCodePairingRequest: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingrequest)
- [var kBluetoothLESecurityManagerCommandCodePairingResponse: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodepairingresponse)
- [var kBluetoothLESecurityManagerCommandCodeReserved: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodereserved)
- [var kBluetoothLESecurityManagerCommandCodeReservedEnd: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodereservedend)
- [var kBluetoothLESecurityManagerCommandCodeReservedStart: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodereservedstart)
- [var kBluetoothLESecurityManagerCommandCodeSecurityRequest: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodesecurityrequest)
- [var kBluetoothLESecurityManagerCommandCodeSigningInfo: BluetoothLESecurityManagerCommandCode](/documentation/iobluetooth/kbluetoothlesecuritymanagercommandcodesigninginfo)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagercommandcode/rawvalue)
- [BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability)

#### Constants

- [var kBluetoothLESecurityManagerIOCapabilityDisplayOnly: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitydisplayonly)
- [var kBluetoothLESecurityManagerIOCapabilityDisplayYesNo: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitydisplayyesno)
- [var kBluetoothLESecurityManagerIOCapabilityKeyboardDisplay: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitykeyboarddisplay)
- [var kBluetoothLESecurityManagerIOCapabilityKeyboardOnly: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitykeyboardonly)
- [var kBluetoothLESecurityManagerIOCapabilityNoInputNoOutput: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilitynoinputnooutput)
- [var kBluetoothLESecurityManagerIOCapabilityReservedEnd: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilityreservedend)
- [var kBluetoothLESecurityManagerIOCapabilityReservedStart: BluetoothLESecurityManagerIOCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageriocapabilityreservedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageriocapability/rawvalue)
- [BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype)

#### Constants

- [var kBluetoothLESecurityManagerNotificationTypePasskeyCleared: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeycleared)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyDigitEntered: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeydigitentered)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyDigitErased: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeydigiterased)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyEntryCompleted: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeyentrycompleted)
- [var kBluetoothLESecurityManagerNotificationTypePasskeyEntryStarted: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypepasskeyentrystarted)
- [var kBluetoothLESecurityManagerNotificationTypeReservedEnd: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypereservedend)
- [var kBluetoothLESecurityManagerNotificationTypeReservedStart: BluetoothLESecurityManagerKeypressNotificationType](/documentation/iobluetooth/kbluetoothlesecuritymanagernotificationtypereservedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagerkeypressnotificationtype/rawvalue)
- [BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata)

#### Constants

- [var kBluetoothLESecurityManagerOOBAuthenticationDataNotPresent: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobauthenticationdatanotpresent)
- [var kBluetoothLESecurityManagerOOBAuthenticationDataPresent: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobauthenticationdatapresent)
- [var kBluetoothLESecurityManagerOOBDataReservedEnd: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobdatareservedend)
- [var kBluetoothLESecurityManagerOOBDataReservedStart: BluetoothLESecurityManagerOOBData](/documentation/iobluetooth/kbluetoothlesecuritymanageroobdatareservedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageroobdata/rawvalue)
- [BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode)

#### Constants

- [var kBluetoothLESecurityManagerReasonCodeAuthenticationRequirements: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeauthenticationrequirements)
- [var kBluetoothLESecurityManagerReasonCodeBREDRPairingInProgress: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodebredrpairinginprogress)
- [var kBluetoothLESecurityManagerReasonCodeCommandNotSupported: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodecommandnotsupported)
- [var kBluetoothLESecurityManagerReasonCodeConfirmValueFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeconfirmvaluefailed)
- [var kBluetoothLESecurityManagerReasonCodeCrossTransportKeyDerivationGenerationNotAllowed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodecrosstransportkeyderivationgenerationnotallowed)
- [var kBluetoothLESecurityManagerReasonCodeDHKeyCheckFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodedhkeycheckfailed)
- [var kBluetoothLESecurityManagerReasonCodeEncryptionKeySize: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeencryptionkeysize)
- [var kBluetoothLESecurityManagerReasonCodeInvalidParameters: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeinvalidparameters)
- [var kBluetoothLESecurityManagerReasonCodeNumericComparisonFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodenumericcomparisonfailed)
- [var kBluetoothLESecurityManagerReasonCodeOOBNotAvailbale: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeoobnotavailbale)
- [var kBluetoothLESecurityManagerReasonCodePairingNotSupported: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodepairingnotsupported)
- [var kBluetoothLESecurityManagerReasonCodePasskeyEntryFailed: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodepasskeyentryfailed)
- [var kBluetoothLESecurityManagerReasonCodeRepeatedAttempts: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncoderepeatedattempts)
- [var kBluetoothLESecurityManagerReasonCodeReserved: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodereserved)
- [var kBluetoothLESecurityManagerReasonCodeReservedEnd: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodereservedend)
- [var kBluetoothLESecurityManagerReasonCodeReservedStart: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodereservedstart)
- [var kBluetoothLESecurityManagerReasonCodeUnspecifiedReason: BluetoothLESecurityManagerPairingFailedReasonCode](/documentation/iobluetooth/kbluetoothlesecuritymanagerreasoncodeunspecifiedreason)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagerpairingfailedreasoncode/rawvalue)
- [BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability)

#### Constants

- [var kBluetoothLESecurityManagerUserInputCapabilityKeyboard: BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruserinputcapabilitykeyboard)
- [var kBluetoothLESecurityManagerUserInputCapabilityNoInput: BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruserinputcapabilitynoinput)
- [var kBluetoothLESecurityManagerUserInputCapabilityYesNo: BluetoothLESecurityManagerUserInputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruserinputcapabilityyesno)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageruserinputcapability/rawvalue)
- [BluetoothLESecurityManagerUserOutputCapability](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability)

#### Constants

- [var kBluetoothLESecurityManagerUserOutputCapabilityNoOutput: BluetoothLESecurityManagerUserOutputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruseroutputcapabilitynooutput)
- [var kBluetoothLESecurityManagerUserOutputCapabilityNumericOutput: BluetoothLESecurityManagerUserOutputCapability](/documentation/iobluetooth/kbluetoothlesecuritymanageruseroutputcapabilitynumericoutput)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanageruseroutputcapability/rawvalue)
- [BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatus)

#### Constants

- [var BluetoothRFCOMMLineStatusFramingError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusframingerror)
- [var BluetoothRFCOMMLineStatusNoError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusnoerror)
- [var BluetoothRFCOMMLineStatusOverrunError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusoverrunerror)
- [var BluetoothRFCOMMLineStatusParityError: BluetoothRFCOMMLineStatus](/documentation/iobluetooth/bluetoothrfcommlinestatusparityerror)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothrfcommlinestatus/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothrfcommlinestatus/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothrfcommlinestatus/rawvalue)
- [BluetoothRFCOMMParityType](/documentation/iobluetooth/bluetoothrfcommparitytype)

#### Constants

- [var kBluetoothRFCOMMParityTypeEvenParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypeevenparity)
- [var kBluetoothRFCOMMParityTypeMaxParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypemaxparity)
- [var kBluetoothRFCOMMParityTypeNoParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypenoparity)
- [var kBluetoothRFCOMMParityTypeOddParity: BluetoothRFCOMMParityType](/documentation/iobluetooth/kbluetoothrfcommparitytypeoddparity)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothrfcommparitytype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothrfcommparitytype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothrfcommparitytype/rawvalue)
- [IOBluetoothHandsFreeAudioGatewayFeatures](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures)

#### Enumeration Cases

- [case attachedNumberToVoiceTag](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/attachednumbertovoicetag)
- [case codecNegotiation](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/codecnegotiation)
- [case ecAndOrNRFunction](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/ecandornrfunction)
- [case enhancedCallControl](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/enhancedcallcontrol)
- [case enhancedCallStatus](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/enhancedcallstatus)
- [case extendedErrorResultCodes](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/extendederrorresultcodes)
- [case inBandRingTone](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/inbandringtone)
- [case none](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/none)
- [case rejectCallCapability](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/rejectcallcapability)
- [case threeWayCalling](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/threewaycalling)
- [case voiceRecognition](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/voicerecognition)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothhandsfreeaudiogatewayfeatures/init(rawvalue:))
- [IOBluetoothHandsFreeCallHoldModes](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes)

#### Enumeration Cases

- [case mode0](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/mode0)
- [case mode1](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/mode1)
- [case mode1idx](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/mode1idx)
- [case mode2](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/mode2)
- [case mode2idx](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/mode2idx)
- [case mode3](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/mode3)
- [case mode4](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/mode4)

#### Initializers

- [init?(rawValue: UInt)](/documentation/iobluetooth/iobluetoothhandsfreecallholdmodes/init(rawvalue:))
- [IOBluetoothHandsFreeCodecID](/documentation/iobluetooth/iobluetoothhandsfreecodecid)

#### Enumeration Cases

- [case IDAACELD](/documentation/iobluetooth/iobluetoothhandsfreecodecid/idaaceld)
- [case IDCVSD](/documentation/iobluetooth/iobluetoothhandsfreecodecid/idcvsd)
- [case iDmSBC](/documentation/iobluetooth/iobluetoothhandsfreecodecid/idmsbc)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/iobluetooth/iobluetoothhandsfreecodecid/init(rawvalue:))
- [IOBluetoothHandsFreeDeviceFeatures](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures)

#### Enumeration Cases

- [case cliPresentation](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/clipresentation)
- [case codecNegotiation](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/codecnegotiation)
- [case ecAndOrNRFunction](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/ecandornrfunction)
- [case enhancedCallControl](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/enhancedcallcontrol)
- [case enhancedCallStatus](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/enhancedcallstatus)
- [case none](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/none)
- [case remoteVolumeControl](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/remotevolumecontrol)
- [case threeWayCalling](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/threewaycalling)
- [case voiceRecognition](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/voicerecognition)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothhandsfreedevicefeatures/init(rawvalue:))
- [IOBluetoothHandsFreePDUMessageStatus](/documentation/iobluetooth/iobluetoothhandsfreepdumessagestatus)

#### Enumeration Cases

- [case statusAll](/documentation/iobluetooth/iobluetoothhandsfreepdumessagestatus/statusall)
- [case statusRecRead](/documentation/iobluetooth/iobluetoothhandsfreepdumessagestatus/statusrecread)
- [case statusRecUnread](/documentation/iobluetooth/iobluetoothhandsfreepdumessagestatus/statusrecunread)
- [case statusStoSent](/documentation/iobluetooth/iobluetoothhandsfreepdumessagestatus/statusstosent)
- [case statusStoUnsent](/documentation/iobluetooth/iobluetoothhandsfreepdumessagestatus/statusstounsent)

#### Initializers

- [init?(rawValue: UInt)](/documentation/iobluetooth/iobluetoothhandsfreepdumessagestatus/init(rawvalue:))
- [IOBluetoothHandsFreeSMSSupport](/documentation/iobluetooth/iobluetoothhandsfreesmssupport)

#### Enumeration Cases

- [case manufactureSpecificSMSSupport](/documentation/iobluetooth/iobluetoothhandsfreesmssupport/manufacturespecificsmssupport)
- [case phase2SMSSupport](/documentation/iobluetooth/iobluetoothhandsfreesmssupport/phase2smssupport)
- [case phase2pSMSSupport](/documentation/iobluetooth/iobluetoothhandsfreesmssupport/phase2psmssupport)

#### Initializers

- [init?(rawValue: UInt)](/documentation/iobluetooth/iobluetoothhandsfreesmssupport/init(rawvalue:))
- [IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/iobluetoothl2capchanneleventtype)

#### Constants

- [var kIOBluetoothL2CAPChannelEventTypeClosed: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypeclosed)
- [var kIOBluetoothL2CAPChannelEventTypeData: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypedata)
- [var kIOBluetoothL2CAPChannelEventTypeOpenComplete: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypeopencomplete)
- [var kIOBluetoothL2CAPChannelEventTypeQueueSpaceAvailable: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypequeuespaceavailable)
- [var kIOBluetoothL2CAPChannelEventTypeReconfigured: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypereconfigured)
- [var kIOBluetoothL2CAPChannelEventTypeWriteComplete: IOBluetoothL2CAPChannelEventType](/documentation/iobluetooth/kiobluetoothl2capchanneleventtypewritecomplete)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothl2capchanneleventtype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothl2capchanneleventtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothl2capchanneleventtype/rawvalue)
- [IOBluetoothSMSMode](/documentation/iobluetooth/iobluetoothsmsmode)

#### Enumeration Cases

- [case PDU](/documentation/iobluetooth/iobluetoothsmsmode/pdu)
- [case text](/documentation/iobluetooth/iobluetoothsmsmode/text)

#### Initializers

- [init?(rawValue: UInt)](/documentation/iobluetooth/iobluetoothsmsmode/init(rawvalue:))
- [IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection)

#### Constants

- [var kIOBluetoothUserNotificationChannelDirectionAny: IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/kiobluetoothusernotificationchanneldirectionany)
- [var kIOBluetoothUserNotificationChannelDirectionIncoming: IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/kiobluetoothusernotificationchanneldirectionincoming)
- [var kIOBluetoothUserNotificationChannelDirectionOutgoing: IOBluetoothUserNotificationChannelDirection](/documentation/iobluetooth/kiobluetoothusernotificationchanneldirectionoutgoing)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothusernotificationchanneldirection/rawvalue)
- [Bluetooth logical channel constants](/documentation/iobluetooth/bluetooth-channel-constants-185mv)

#### Constants

- [var kBluetoothACLLogicalChannelL2CAPContinue: Int](/documentation/iobluetooth/kbluetoothacllogicalchannell2capcontinue)
- [var kBluetoothACLLogicalChannelL2CAPStart: Int](/documentation/iobluetooth/kbluetoothacllogicalchannell2capstart)
- [var kBluetoothACLLogicalChannelLMP: Int](/documentation/iobluetooth/kbluetoothacllogicalchannellmp)
- [var kBluetoothACLLogicalChannelReserved: Int](/documentation/iobluetooth/kbluetoothacllogicalchannelreserved)
- [var kBluetoothL2CAPMaxPacketSize: Int](/documentation/iobluetooth/kbluetoothl2capmaxpacketsize)
- [BluetoothVoiceSettingInputSampleSize constants](/documentation/iobluetooth/bluetoothvoicesettinginputsamplesize-constants-1bmtk)

#### Constants

- [var kBluetoothVoiceSettingInputSampleSize16Bit: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputsamplesize16bit)
- [var kBluetoothVoiceSettingInputSampleSize8Bit: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputsamplesize8bit)
- [var kBluetoothVoiceSettingInputSampleSizeMask: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputsamplesizemask)
- [BluetoothEncryptionEnable constants](/documentation/iobluetooth/bluetoothencryptionenable-constants-1cxrq)

#### Constants

- [var kBluetoothEncryptionEnableBREDRAESCCM: Int](/documentation/iobluetooth/kbluetoothencryptionenablebredraesccm)
- [var kBluetoothEncryptionEnableBREDRE0: Int](/documentation/iobluetooth/kbluetoothencryptionenablebredre0)
- [var kBluetoothEncryptionEnableLEAESCCM: Int](/documentation/iobluetooth/kbluetoothencryptionenableleaesccm)
- [var kBluetoothEncryptionEnableOff: Int](/documentation/iobluetooth/kbluetoothencryptionenableoff)
- [var kBluetoothEncryptionEnableOn: Int](/documentation/iobluetooth/kbluetoothencryptionenableon)
- [BluetoothL2CAPConfigurationOption constants](/documentation/iobluetooth/bluetoothl2capconfigurationoption-constants-1hjhz)

#### Constants

- [var kBluetoothL2CAPConfigurationOptionFlushTimeoutLength: Int](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionflushtimeoutlength)
- [var kBluetoothL2CAPConfigurationOptionMTULength: Int](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionmtulength)
- [var kBluetoothL2CAPConfigurationOptionQoSLength: Int](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionqoslength)
- [var kBluetoothL2CAPConfigurationOptionRetransmissionAndFlowControlLength: Int](/documentation/iobluetooth/kbluetoothl2capconfigurationoptionretransmissionandflowcontrollength)
- [BluetoothL2CAPTCIEventID constants](/documentation/iobluetooth/bluetoothl2captcieventid-constants-1tcfj)

#### Constants

- [var kBluetoothL2CAPTCIEventIDL2CA_ConfigInd: Int](/documentation/iobluetooth/kbluetoothl2captcieventidl2ca_configind)
- [var kBluetoothL2CAPTCIEventIDL2CA_ConnectInd: Int](/documentation/iobluetooth/kbluetoothl2captcieventidl2ca_connectind)
- [var kBluetoothL2CAPTCIEventIDL2CA_DisconnectInd: Int](/documentation/iobluetooth/kbluetoothl2captcieventidl2ca_disconnectind)
- [var kBluetoothL2CAPTCIEventIDL2CA_QoSViolationInd: Int](/documentation/iobluetooth/kbluetoothl2captcieventidl2ca_qosviolationind)
- [var kBluetoothL2CAPTCIEventIDL2CA_TimeOutInd: Int](/documentation/iobluetooth/kbluetoothl2captcieventidl2ca_timeoutind)
- [var kBluetoothL2CAPTCIEventIDReserved: Int](/documentation/iobluetooth/kbluetoothl2captcieventidreserved)
- [BluetoothL2CAPPacketHeaderSize constants](/documentation/iobluetooth/bluetoothl2cappacketheadersize-constants-2k6pk)

#### Constants

- [var kBluetoothL2CAPPacketHeaderSize: Int](/documentation/iobluetooth/kbluetoothl2cappacketheadersize)
- [BluetoothGAPAppearance constants](/documentation/iobluetooth/bluetoothgapappearance-constants-2lmnv)

#### Constants

- [var kBluetoothGAPAppearanceGenericBarcodeScanner: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericbarcodescanner)
- [var kBluetoothGAPAppearanceGenericBloodPressure: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericbloodpressure)
- [var kBluetoothGAPAppearanceGenericClock: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericclock)
- [var kBluetoothGAPAppearanceGenericComputer: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericcomputer)
- [var kBluetoothGAPAppearanceGenericCycling: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericcycling)
- [var kBluetoothGAPAppearanceGenericDisplay: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericdisplay)
- [var kBluetoothGAPAppearanceGenericEyeGlasses: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericeyeglasses)
- [var kBluetoothGAPAppearanceGenericGlucoseMeter: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericglucosemeter)
- [var kBluetoothGAPAppearanceGenericHeartrateSensor: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericheartratesensor)
- [var kBluetoothGAPAppearanceGenericHumanInterfaceDevice: Int](/documentation/iobluetooth/kbluetoothgapappearancegenerichumaninterfacedevice)
- [var kBluetoothGAPAppearanceGenericKeyring: Int](/documentation/iobluetooth/kbluetoothgapappearancegenerickeyring)
- [var kBluetoothGAPAppearanceGenericMediaPlayer: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericmediaplayer)
- [var kBluetoothGAPAppearanceGenericPhone: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericphone)
- [var kBluetoothGAPAppearanceGenericRemoteControl: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericremotecontrol)
- [var kBluetoothGAPAppearanceGenericRunningWalkingSensor: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericrunningwalkingsensor)
- [var kBluetoothGAPAppearanceGenericTag: Int](/documentation/iobluetooth/kbluetoothgapappearancegenerictag)
- [var kBluetoothGAPAppearanceGenericThermometer: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericthermometer)
- [var kBluetoothGAPAppearanceGenericWatch: Int](/documentation/iobluetooth/kbluetoothgapappearancegenericwatch)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceBarcodeScanner: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicebarcodescanner)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceCardReader: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicecardreader)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceDigitalPen: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicedigitalpen)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceDigitizerTablet: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicedigitizertablet)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceGamepad: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicegamepad)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceJoystick: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicejoystick)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceKeyboard: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicekeyboard)
- [var kBluetoothGAPAppearanceHumanInterfaceDeviceMouse: Int](/documentation/iobluetooth/kbluetoothgapappearancehumaninterfacedevicemouse)
- [var kBluetoothGAPAppearanceUnknown: Int](/documentation/iobluetooth/kbluetoothgapappearanceunknown)
- [BluetoothLETX constants](/documentation/iobluetooth/bluetoothletx-constants-2rrb0)

#### Constants

- [var kBluetoothLETXOctetsDefault: Int](/documentation/iobluetooth/kbluetoothletxoctetsdefault)
- [var kBluetoothLETXOctetsMax: Int](/documentation/iobluetooth/kbluetoothletxoctetsmax)
- [var kBluetoothLETXOctetsMin: Int](/documentation/iobluetooth/kbluetoothletxoctetsmin)
- [var kBluetoothLETXTimeDefault: Int](/documentation/iobluetooth/kbluetoothletxtimedefault)
- [var kBluetoothLETXTimeMax: Int](/documentation/iobluetooth/kbluetoothletxtimemax)
- [var kBluetoothLETXTimeMin: Int](/documentation/iobluetooth/kbluetoothletxtimemin)
- [BluetoothKeyFlag constants](/documentation/iobluetooth/bluetoothkeyflag-constants-33gk5)

#### Constants

- [var kBluetoothKeyFlagSemiPermanent: Int](/documentation/iobluetooth/kbluetoothkeyflagsemipermanent)
- [var kBluetoothKeyFlagTemporary: Int](/documentation/iobluetooth/kbluetoothkeyflagtemporary)
- [BluetoothHCILoopbackMode constants](/documentation/iobluetooth/bluetoothhciloopbackmode-constants-366i1)

#### Constants

- [var kBluetoothHCILoopbackModeLocal: Int](/documentation/iobluetooth/kbluetoothhciloopbackmodelocal)
- [var kBluetoothHCILoopbackModeOff: Int](/documentation/iobluetooth/kbluetoothhciloopbackmodeoff)
- [var kBluetoothHCILoopbackModeRemote: Int](/documentation/iobluetooth/kbluetoothhciloopbackmoderemote)
- [BluetoothSDPDataElementType constants](/documentation/iobluetooth/bluetoothsdpdataelementtype-constants-3dgra)

#### Constants

- [var kBluetoothSDPDataElementTypeBoolean: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypeboolean)
- [var kBluetoothSDPDataElementTypeDataElementAlternative: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypedataelementalternative)
- [var kBluetoothSDPDataElementTypeDataElementSequence: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypedataelementsequence)
- [var kBluetoothSDPDataElementTypeNil: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypenil)
- [var kBluetoothSDPDataElementTypeReservedEnd: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypereservedend)
- [var kBluetoothSDPDataElementTypeReservedStart: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypereservedstart)
- [var kBluetoothSDPDataElementTypeSignedInt: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypesignedint)
- [var kBluetoothSDPDataElementTypeString: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypestring)
- [var kBluetoothSDPDataElementTypeURL: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypeurl)
- [var kBluetoothSDPDataElementTypeUUID: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypeuuid)
- [var kBluetoothSDPDataElementTypeUnsignedInt: Int](/documentation/iobluetooth/kbluetoothsdpdataelementtypeunsignedint)
- [BluetoothLEMaxTX constants](/documentation/iobluetooth/bluetoothlemaxtx-constants-3tkwh)

#### Constants

- [var kBluetoothLEMaxTXOctetsDefault: Int](/documentation/iobluetooth/kbluetoothlemaxtxoctetsdefault)
- [var kBluetoothLEMaxTXOctetsMax: Int](/documentation/iobluetooth/kbluetoothlemaxtxoctetsmax)
- [var kBluetoothLEMaxTXOctetsMin: Int](/documentation/iobluetooth/kbluetoothlemaxtxoctetsmin)
- [var kBluetoothLEMaxTXTimeDefault: Int](/documentation/iobluetooth/kbluetoothlemaxtxtimedefault)
- [var kBluetoothLEMaxTXTimeMax: Int](/documentation/iobluetooth/kbluetoothlemaxtxtimemax)
- [var kBluetoothLEMaxTXTimeMin: Int](/documentation/iobluetooth/kbluetoothlemaxtxtimemin)
- [BluetoothVoiceSettingInputCoding constants](/documentation/iobluetooth/bluetoothvoicesettinginputcoding-constants-3xsmm)

#### Constants

- [var kBluetoothVoiceSettingInputCodingALawInputCoding: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputcodingalawinputcoding)
- [var kBluetoothVoiceSettingInputCodingLinearInputCoding: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputcodinglinearinputcoding)
- [var kBluetoothVoiceSettingInputCodingMask: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputcodingmask)
- [var kBluetoothVoiceSettingInputCodingULawInputCoding: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputcodingulawinputcoding)
- [BluetoothHCIEventMask constants](/documentation/iobluetooth/bluetoothhcieventmask-constants-3y92r)

#### Constants

- [var kBluetoothHCIEventMaskAll: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskall)
- [var kBluetoothHCIEventMaskAuthenticationComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskauthenticationcomplete)
- [var kBluetoothHCIEventMaskChangeConnectionLinkKeyComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskchangeconnectionlinkkeycomplete)
- [var kBluetoothHCIEventMaskCommandComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskcommandcomplete)
- [var kBluetoothHCIEventMaskCommandStatus: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskcommandstatus)
- [var kBluetoothHCIEventMaskConnectionComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskconnectioncomplete)
- [var kBluetoothHCIEventMaskConnectionPacketTypeChanged: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskconnectionpackettypechanged)
- [var kBluetoothHCIEventMaskConnectionRequest: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskconnectionrequest)
- [var kBluetoothHCIEventMaskDataBufferOverflow: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskdatabufferoverflow)
- [var kBluetoothHCIEventMaskDefault: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskdefault)
- [var kBluetoothHCIEventMaskDisconnectionComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskdisconnectioncomplete)
- [var kBluetoothHCIEventMaskEncryptionChange: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskencryptionchange)
- [var kBluetoothHCIEventMaskFlushOccurred: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskflushoccurred)
- [var kBluetoothHCIEventMaskHardwareError: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskhardwareerror)
- [var kBluetoothHCIEventMaskInquiryComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskinquirycomplete)
- [var kBluetoothHCIEventMaskInquiryResult: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskinquiryresult)
- [var kBluetoothHCIEventMaskLinkKeyNotification: UInt32](/documentation/iobluetooth/kbluetoothhcieventmasklinkkeynotification)
- [var kBluetoothHCIEventMaskLinkKeyRequest: UInt32](/documentation/iobluetooth/kbluetoothhcieventmasklinkkeyrequest)
- [var kBluetoothHCIEventMaskLoopbackCommand: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskloopbackcommand)
- [var kBluetoothHCIEventMaskMasterLinkKeyComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskmasterlinkkeycomplete)
- [var kBluetoothHCIEventMaskMaxSlotsChange: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskmaxslotschange)
- [var kBluetoothHCIEventMaskModeChange: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskmodechange)
- [var kBluetoothHCIEventMaskNone: UInt32](/documentation/iobluetooth/kbluetoothhcieventmasknone)
- [var kBluetoothHCIEventMaskNumberOfCompletedPackets: UInt32](/documentation/iobluetooth/kbluetoothhcieventmasknumberofcompletedpackets)
- [var kBluetoothHCIEventMaskPINCodeRequest: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskpincoderequest)
- [var kBluetoothHCIEventMaskPageScanModeChange: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskpagescanmodechange)
- [var kBluetoothHCIEventMaskPageScanRepetitionModeChange: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskpagescanrepetitionmodechange)
- [var kBluetoothHCIEventMaskQoSSetupComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskqossetupcomplete)
- [var kBluetoothHCIEventMaskQoSViolation: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskqosviolation)
- [var kBluetoothHCIEventMaskReadClockOffsetComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskreadclockoffsetcomplete)
- [var kBluetoothHCIEventMaskReadRemoteSupportedFeaturesComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskreadremotesupportedfeaturescomplete)
- [var kBluetoothHCIEventMaskReadRemoteVersionInformationComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskreadremoteversioninformationcomplete)
- [var kBluetoothHCIEventMaskRemoteNameRequestComplete: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskremotenamerequestcomplete)
- [var kBluetoothHCIEventMaskReturnLinkKeys: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskreturnlinkkeys)
- [var kBluetoothHCIEventMaskRoleChange: UInt32](/documentation/iobluetooth/kbluetoothhcieventmaskrolechange)
- [var kBluetoothHCIEvnetMaskEnhancedFlushCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcievnetmaskenhancedflushcompleteevent)
- [var kBluetoothHCIEvnetMaskLinkSupervisionTimeoutChangedEvent: Int64](/documentation/iobluetooth/kbluetoothhcievnetmasklinksupervisiontimeoutchangedevent)
- [BluetoothDeviceNameMaxLength constants](/documentation/iobluetooth/bluetoothdevicenamemaxlength-constants-4che4)

#### Constants

- [var kBluetoothDeviceNameMaxLength: Int](/documentation/iobluetooth/kbluetoothdevicenamemaxlength)
- [BluetoothVoiceSettingPCMBitPositionMask constants](/documentation/iobluetooth/bluetoothvoicesettingpcmbitpositionmask-constants-4frpt)

#### Constants

- [var kBluetoothVoiceSettingPCMBitPositionMask: Int](/documentation/iobluetooth/kbluetoothvoicesettingpcmbitpositionmask)
- [BluetoothHCIErrorPowerIsOFF constants](/documentation/iobluetooth/bluetoothhcierrorpowerisoff-constants-4z8d6)

#### Constants

- [var kBluetoothHCIErrorPowerIsOFF: Int](/documentation/iobluetooth/kbluetoothhcierrorpowerisoff)
- [BluetoothHCI packet size constants](/documentation/iobluetooth/bluetoothhci-packet-constants-511bu)

#### Constants

- [var kBluetoothHCICommandPacketHeaderSize: Int](/documentation/iobluetooth/kbluetoothhcicommandpacketheadersize)
- [var kBluetoothHCICommandPacketMaxDataSize: Int](/documentation/iobluetooth/kbluetoothhcicommandpacketmaxdatasize)
- [var kBluetoothHCIDataPacketHeaderSize: Int](/documentation/iobluetooth/kbluetoothhcidatapacketheadersize)
- [var kBluetoothHCIDataPacketMaxDataSize: Int](/documentation/iobluetooth/kbluetoothhcidatapacketmaxdatasize)
- [var kBluetoothHCIEventPacketHeaderSize: Int](/documentation/iobluetooth/kbluetoothhcieventpacketheadersize)
- [var kBluetoothHCIEventPacketMaxDataSize: Int](/documentation/iobluetooth/kbluetoothhcieventpacketmaxdatasize)
- [var kBluetoothHCIMaxCommandPacketSize: Int](/documentation/iobluetooth/kbluetoothhcimaxcommandpacketsize)
- [var kBluetoothHCIMaxDataPacketSize: Int](/documentation/iobluetooth/kbluetoothhcimaxdatapacketsize)
- [var kBluetoothHCIMaxEventPacketSize: Int](/documentation/iobluetooth/kbluetoothhcimaxeventpacketsize)
- [BluetoothVoiceSettingAirCodingFormat constants](/documentation/iobluetooth/bluetoothvoicesettingaircodingformat-constants-53tsp)

#### Constants

- [var kBluetoothVoiceSettingAirCodingFormatALaw: Int](/documentation/iobluetooth/kbluetoothvoicesettingaircodingformatalaw)
- [var kBluetoothVoiceSettingAirCodingFormatCVSD: Int](/documentation/iobluetooth/kbluetoothvoicesettingaircodingformatcvsd)
- [var kBluetoothVoiceSettingAirCodingFormatMask: Int](/documentation/iobluetooth/kbluetoothvoicesettingaircodingformatmask)
- [var kBluetoothVoiceSettingAirCodingFormatTransparentData: Int](/documentation/iobluetooth/kbluetoothvoicesettingaircodingformattransparentdata)
- [var kBluetoothVoiceSettingAirCodingFormatULaw: Int](/documentation/iobluetooth/kbluetoothvoicesettingaircodingformatulaw)
- [BluetoothKeyType constants](/documentation/iobluetooth/bluetoothkeytype-constants-5cjrj)

#### Constants

- [var kBluetoothKeyTypeAuthenticatedCombination: Int](/documentation/iobluetooth/kbluetoothkeytypeauthenticatedcombination)
- [var kBluetoothKeyTypeChangedCombination: Int](/documentation/iobluetooth/kbluetoothkeytypechangedcombination)
- [var kBluetoothKeyTypeCombination: Int](/documentation/iobluetooth/kbluetoothkeytypecombination)
- [var kBluetoothKeyTypeDebugCombination: Int](/documentation/iobluetooth/kbluetoothkeytypedebugcombination)
- [var kBluetoothKeyTypeLocalUnit: Int](/documentation/iobluetooth/kbluetoothkeytypelocalunit)
- [var kBluetoothKeyTypeRemoteUnit: Int](/documentation/iobluetooth/kbluetoothkeytyperemoteunit)
- [var kBluetoothKeyTypeUnauthenticatedCombination: Int](/documentation/iobluetooth/kbluetoothkeytypeunauthenticatedcombination)
- [var kBluetoothKeyTypeAuthenticatedCombinationP256: Int](/documentation/iobluetooth/kbluetoothkeytypeauthenticatedcombinationp256)
- [var kBluetoothKeyTypeUnauthenticatedCombinationP256: Int](/documentation/iobluetooth/kbluetoothkeytypeunauthenticatedcombinationp256)
- [BluetoothL2CAP constants](/documentation/iobluetooth/bluetoothl2cap-constants-5jo8y)

#### Constants

- [var kBluetoothL2CAPFlushTimeoutDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capflushtimeoutdefault)
- [var kBluetoothL2CAPMTUDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capmtudefault)
- [var kBluetoothL2CAPMTULowEnergyDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capmtulowenergydefault)
- [var kBluetoothL2CAPMTUMaximum: UInt32](/documentation/iobluetooth/kbluetoothl2capmtumaximum)
- [var kBluetoothL2CAPMTUMinimum: UInt32](/documentation/iobluetooth/kbluetoothl2capmtuminimum)
- [var kBluetoothL2CAPMTUSIG: UInt32](/documentation/iobluetooth/kbluetoothl2capmtusig)
- [var kBluetoothL2CAPMTUStart: UInt32](/documentation/iobluetooth/kbluetoothl2capmtustart)
- [var kBluetoothL2CAPQoSDelayVariationDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capqosdelayvariationdefault)
- [var kBluetoothL2CAPQoSFlagsDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capqosflagsdefault)
- [var kBluetoothL2CAPQoSLatencyDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capqoslatencydefault)
- [var kBluetoothL2CAPQoSPeakBandwidthDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capqospeakbandwidthdefault)
- [var kBluetoothL2CAPQoSTokenBucketSizeDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capqostokenbucketsizedefault)
- [var kBluetoothL2CAPQoSTokenRateDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capqostokenratedefault)
- [var kBluetoothL2CAPQoSTypeDefault: UInt32](/documentation/iobluetooth/kbluetoothl2capqostypedefault)
- [var kBluetoothL2CAPMTULowEnergyMax: UInt32](/documentation/iobluetooth/kbluetoothl2capmtulowenergymax)
- [BluetoothL2CAPFlushTimeout constants](/documentation/iobluetooth/bluetoothl2capflushtimeout-constants-5me0)

#### Constants

- [var kBluetoothL2CAPFlushTimeoutEnd: Int](/documentation/iobluetooth/kbluetoothl2capflushtimeoutend)
- [var kBluetoothL2CAPFlushTimeoutForever: Int](/documentation/iobluetooth/kbluetoothl2capflushtimeoutforever)
- [var kBluetoothL2CAPFlushTimeoutImmediate: Int](/documentation/iobluetooth/kbluetoothl2capflushtimeoutimmediate)
- [var kBluetoothL2CAPFlushTimeoutUseExisting: Int](/documentation/iobluetooth/kbluetoothl2capflushtimeoutuseexisting)
- [BluetoothHCI event constants](/documentation/iobluetooth/bluetoothhci-event-constants-5mz8f)

#### Constants

- [var kBluetoothHCIEventAMPReceiverReport: Int](/documentation/iobluetooth/kbluetoothhcieventampreceiverreport)
- [var kBluetoothHCIEventAMPStartTest: Int](/documentation/iobluetooth/kbluetoothhcieventampstarttest)
- [var kBluetoothHCIEventAMPStatusChange: Int](/documentation/iobluetooth/kbluetoothhcieventampstatuschange)
- [var kBluetoothHCIEventAMPTestEnd: Int](/documentation/iobluetooth/kbluetoothhcieventamptestend)
- [var kBluetoothHCIEventAuthenticationComplete: Int](/documentation/iobluetooth/kbluetoothhcieventauthenticationcomplete)
- [var kBluetoothHCIEventChangeConnectionLinkKeyComplete: Int](/documentation/iobluetooth/kbluetoothhcieventchangeconnectionlinkkeycomplete)
- [var kBluetoothHCIEventChannelSelected: Int](/documentation/iobluetooth/kbluetoothhcieventchannelselected)
- [var kBluetoothHCIEventCommandComplete: Int](/documentation/iobluetooth/kbluetoothhcieventcommandcomplete)
- [var kBluetoothHCIEventCommandStatus: Int](/documentation/iobluetooth/kbluetoothhcieventcommandstatus)
- [var kBluetoothHCIEventConnectionComplete: Int](/documentation/iobluetooth/kbluetoothhcieventconnectioncomplete)
- [var kBluetoothHCIEventConnectionPacketType: Int](/documentation/iobluetooth/kbluetoothhcieventconnectionpackettype)
- [var kBluetoothHCIEventConnectionRequest: Int](/documentation/iobluetooth/kbluetoothhcieventconnectionrequest)
- [var kBluetoothHCIEventDataBufferOverflow: Int](/documentation/iobluetooth/kbluetoothhcieventdatabufferoverflow)
- [var kBluetoothHCIEventDisconnectionComplete: Int](/documentation/iobluetooth/kbluetoothhcieventdisconnectioncomplete)
- [var kBluetoothHCIEventDisconnectionLogicalLinkComplete: Int](/documentation/iobluetooth/kbluetoothhcieventdisconnectionlogicallinkcomplete)
- [var kBluetoothHCIEventDisconnectionPhysicalLinkComplete: Int](/documentation/iobluetooth/kbluetoothhcieventdisconnectionphysicallinkcomplete)
- [var kBluetoothHCIEventEncryptionChange: Int](/documentation/iobluetooth/kbluetoothhcieventencryptionchange)
- [var kBluetoothHCIEventEncryptionKeyRefreshComplete: Int](/documentation/iobluetooth/kbluetoothhcieventencryptionkeyrefreshcomplete)
- [var kBluetoothHCIEventEnhancedFlushComplete: Int](/documentation/iobluetooth/kbluetoothhcieventenhancedflushcomplete)
- [var kBluetoothHCIEventExtendedInquiryResult: Int](/documentation/iobluetooth/kbluetoothhcieventextendedinquiryresult)
- [var kBluetoothHCIEventFlowSpecModifyComplete: Int](/documentation/iobluetooth/kbluetoothhcieventflowspecmodifycomplete)
- [var kBluetoothHCIEventFlowSpecificationComplete: Int](/documentation/iobluetooth/kbluetoothhcieventflowspecificationcomplete)
- [var kBluetoothHCIEventFlushOccurred: Int](/documentation/iobluetooth/kbluetoothhcieventflushoccurred)
- [var kBluetoothHCIEventHardwareError: Int](/documentation/iobluetooth/kbluetoothhcieventhardwareerror)
- [var kBluetoothHCIEventIOCapabilityRequest: Int](/documentation/iobluetooth/kbluetoothhcieventiocapabilityrequest)
- [var kBluetoothHCIEventIOCapabilityResponse: Int](/documentation/iobluetooth/kbluetoothhcieventiocapabilityresponse)
- [var kBluetoothHCIEventInquiryComplete: Int](/documentation/iobluetooth/kbluetoothhcieventinquirycomplete)
- [var kBluetoothHCIEventInquiryResult: Int](/documentation/iobluetooth/kbluetoothhcieventinquiryresult)
- [var kBluetoothHCIEventInquiryResultWithRSSI: Int](/documentation/iobluetooth/kbluetoothhcieventinquiryresultwithrssi)
- [var kBluetoothHCIEventKeypressNotification: Int](/documentation/iobluetooth/kbluetoothhcieventkeypressnotification)
- [var kBluetoothHCIEventLEMetaEvent: Int](/documentation/iobluetooth/kbluetoothhcieventlemetaevent)
- [var kBluetoothHCIEventLinkKeyNotification: Int](/documentation/iobluetooth/kbluetoothhcieventlinkkeynotification)
- [var kBluetoothHCIEventLinkKeyRequest: Int](/documentation/iobluetooth/kbluetoothhcieventlinkkeyrequest)
- [var kBluetoothHCIEventLinkSupervisionTimeoutChanged: Int](/documentation/iobluetooth/kbluetoothhcieventlinksupervisiontimeoutchanged)
- [var kBluetoothHCIEventLogicalLinkComplete: Int](/documentation/iobluetooth/kbluetoothhcieventlogicallinkcomplete)
- [var kBluetoothHCIEventLogoTesting: Int](/documentation/iobluetooth/kbluetoothhcieventlogotesting)
- [var kBluetoothHCIEventLoopbackCommand: Int](/documentation/iobluetooth/kbluetoothhcieventloopbackcommand)
- [var kBluetoothHCIEventMasterLinkKeyComplete: Int](/documentation/iobluetooth/kbluetoothhcieventmasterlinkkeycomplete)
- [var kBluetoothHCIEventMaxSlotsChange: Int](/documentation/iobluetooth/kbluetoothhcieventmaxslotschange)
- [var kBluetoothHCIEventModeChange: Int](/documentation/iobluetooth/kbluetoothhcieventmodechange)
- [var kBluetoothHCIEventNumberOfCompletedDataBlocks: Int](/documentation/iobluetooth/kbluetoothhcieventnumberofcompleteddatablocks)
- [var kBluetoothHCIEventNumberOfCompletedPackets: Int](/documentation/iobluetooth/kbluetoothhcieventnumberofcompletedpackets)
- [var kBluetoothHCIEventPINCodeRequest: Int](/documentation/iobluetooth/kbluetoothhcieventpincoderequest)
- [var kBluetoothHCIEventPageScanModeChange: Int](/documentation/iobluetooth/kbluetoothhcieventpagescanmodechange)
- [var kBluetoothHCIEventPageScanRepetitionModeChange: Int](/documentation/iobluetooth/kbluetoothhcieventpagescanrepetitionmodechange)
- [var kBluetoothHCIEventPhysicalLinkComplete: Int](/documentation/iobluetooth/kbluetoothhcieventphysicallinkcomplete)
- [var kBluetoothHCIEventPhysicalLinkLossEarlyWarning: Int](/documentation/iobluetooth/kbluetoothhcieventphysicallinklossearlywarning)
- [var kBluetoothHCIEventPhysicalLinkRecovery: Int](/documentation/iobluetooth/kbluetoothhcieventphysicallinkrecovery)
- [var kBluetoothHCIEventQoSSetupComplete: Int](/documentation/iobluetooth/kbluetoothhcieventqossetupcomplete)
- [var kBluetoothHCIEventQoSViolation: Int](/documentation/iobluetooth/kbluetoothhcieventqosviolation)
- [var kBluetoothHCIEventReadClockOffsetComplete: Int](/documentation/iobluetooth/kbluetoothhcieventreadclockoffsetcomplete)
- [var kBluetoothHCIEventReadRemoteExtendedFeaturesComplete: Int](/documentation/iobluetooth/kbluetoothhcieventreadremoteextendedfeaturescomplete)
- [var kBluetoothHCIEventReadRemoteSupportedFeaturesComplete: Int](/documentation/iobluetooth/kbluetoothhcieventreadremotesupportedfeaturescomplete)
- [var kBluetoothHCIEventReadRemoteVersionInformationComplete: Int](/documentation/iobluetooth/kbluetoothhcieventreadremoteversioninformationcomplete)
- [var kBluetoothHCIEventRemoteHostSupportedFeaturesNotification: Int](/documentation/iobluetooth/kbluetoothhcieventremotehostsupportedfeaturesnotification)
- [var kBluetoothHCIEventRemoteNameRequestComplete: Int](/documentation/iobluetooth/kbluetoothhcieventremotenamerequestcomplete)
- [var kBluetoothHCIEventRemoteOOBDataRequest: Int](/documentation/iobluetooth/kbluetoothhcieventremoteoobdatarequest)
- [var kBluetoothHCIEventReturnLinkKeys: Int](/documentation/iobluetooth/kbluetoothhcieventreturnlinkkeys)
- [var kBluetoothHCIEventRoleChange: Int](/documentation/iobluetooth/kbluetoothhcieventrolechange)
- [var kBluetoothHCIEventShortRangeModeChangeComplete: Int](/documentation/iobluetooth/kbluetoothhcieventshortrangemodechangecomplete)
- [var kBluetoothHCIEventSimplePairingComplete: Int](/documentation/iobluetooth/kbluetoothhcieventsimplepairingcomplete)
- [var kBluetoothHCIEventSniffSubrating: Int](/documentation/iobluetooth/kbluetoothhcieventsniffsubrating)
- [var kBluetoothHCIEventSynchronousConnectionChanged: Int](/documentation/iobluetooth/kbluetoothhcieventsynchronousconnectionchanged)
- [var kBluetoothHCIEventSynchronousConnectionComplete: Int](/documentation/iobluetooth/kbluetoothhcieventsynchronousconnectioncomplete)
- [var kBluetoothHCIEventUserConfirmationRequest: Int](/documentation/iobluetooth/kbluetoothhcieventuserconfirmationrequest)
- [var kBluetoothHCIEventUserPasskeyNotification: Int](/documentation/iobluetooth/kbluetoothhcieventuserpasskeynotification)
- [var kBluetoothHCIEventUserPasskeyRequest: Int](/documentation/iobluetooth/kbluetoothhcieventuserpasskeyrequest)
- [var kBluetoothHCIEventVendorSpecific: Int](/documentation/iobluetooth/kbluetoothhcieventvendorspecific)
- [var kBluetoothHCISubEventLEAdvertisingReport: Int](/documentation/iobluetooth/kbluetoothhcisubeventleadvertisingreport)
- [var kBluetoothHCISubEventLEConnectionComplete: Int](/documentation/iobluetooth/kbluetoothhcisubeventleconnectioncomplete)
- [var kBluetoothHCISubEventLEConnectionUpdateComplete: Int](/documentation/iobluetooth/kbluetoothhcisubeventleconnectionupdatecomplete)
- [var kBluetoothHCISubEventLELongTermKeyRequest: Int](/documentation/iobluetooth/kbluetoothhcisubeventlelongtermkeyrequest)
- [var kBluetoothHCISubEventLEReadRemoteUsedFeaturesComplete: Int](/documentation/iobluetooth/kbluetoothhcisubeventlereadremoteusedfeaturescomplete)
- [var kBluetoothHCISubEventLEDataLengthChange: Int](/documentation/iobluetooth/kbluetoothhcisubeventledatalengthchange)
- [var kBluetoothHCISubEventLEDirectAdvertisingReport: Int](/documentation/iobluetooth/kbluetoothhcisubeventledirectadvertisingreport)
- [var kBluetoothHCISubEventLEEnhancedConnectionComplete: Int](/documentation/iobluetooth/kbluetoothhcisubeventleenhancedconnectioncomplete)
- [var kBluetoothHCISubEventLEGenerateDHKeyComplete: Int](/documentation/iobluetooth/kbluetoothhcisubeventlegeneratedhkeycomplete)
- [var kBluetoothHCISubEventLEReadLocalP256PublicKeyComplete: Int](/documentation/iobluetooth/kbluetoothhcisubeventlereadlocalp256publickeycomplete)
- [var kBluetoothHCISubEventLERemoteConnectionParameterRequest: Int](/documentation/iobluetooth/kbluetoothhcisubeventleremoteconnectionparameterrequest)
- [var kBluetoothHCISubEventLEAdvertisingSetTerminated: Int](/documentation/iobluetooth/kbluetoothhcisubeventleadvertisingsetterminated)
- [var kBluetoothHCISubEventLEChannelSelectionAlgorithm: Int](/documentation/iobluetooth/kbluetoothhcisubeventlechannelselectionalgorithm)
- [var kBluetoothHCISubEventLEExtendedAdvertising: Int](/documentation/iobluetooth/kbluetoothhcisubeventleextendedadvertising)
- [var kBluetoothHCISubEventLEPeriodicAdvertisingReport: Int](/documentation/iobluetooth/kbluetoothhcisubeventleperiodicadvertisingreport)
- [var kBluetoothHCISubEventLEPeriodicAdvertisingSyncEstablished: Int](/documentation/iobluetooth/kbluetoothhcisubeventleperiodicadvertisingsyncestablished)
- [var kBluetoothHCISubEventLEPeriodicAdvertisingSyncLost: Int](/documentation/iobluetooth/kbluetoothhcisubeventleperiodicadvertisingsynclost)
- [var kBluetoothHCISubEventLEPhyUpdateComplete: Int](/documentation/iobluetooth/kbluetoothhcisubeventlephyupdatecomplete)
- [var kBluetoothHCISubEventLEScanRequestReceived: Int](/documentation/iobluetooth/kbluetoothhcisubeventlescanrequestreceived)
- [var kBluetoothHCISubEventLEScanTimeout: Int](/documentation/iobluetooth/kbluetoothhcisubeventlescantimeout)
- [BluetoothSDPPDUID constants](/documentation/iobluetooth/bluetoothsdppduid-constants-62inr)

#### Constants

- [var kBluetoothSDPPDUIDErrorResponse: Int](/documentation/iobluetooth/kbluetoothsdppduiderrorresponse)
- [var kBluetoothSDPPDUIDReserved: Int](/documentation/iobluetooth/kbluetoothsdppduidreserved)
- [var kBluetoothSDPPDUIDServiceAttributeRequest: Int](/documentation/iobluetooth/kbluetoothsdppduidserviceattributerequest)
- [var kBluetoothSDPPDUIDServiceAttributeResponse: Int](/documentation/iobluetooth/kbluetoothsdppduidserviceattributeresponse)
- [var kBluetoothSDPPDUIDServiceSearchAttributeRequest: Int](/documentation/iobluetooth/kbluetoothsdppduidservicesearchattributerequest)
- [var kBluetoothSDPPDUIDServiceSearchAttributeResponse: Int](/documentation/iobluetooth/kbluetoothsdppduidservicesearchattributeresponse)
- [var kBluetoothSDPPDUIDServiceSearchRequest: Int](/documentation/iobluetooth/kbluetoothsdppduidservicesearchrequest)
- [var kBluetoothSDPPDUIDServiceSearchResponse: Int](/documentation/iobluetooth/kbluetoothsdppduidservicesearchresponse)
- [BluetoothLESecurityManager constants](/documentation/iobluetooth/bluetoothlesecuritymanager-constants-67vw)

#### Constants

- [var kBluetoothLESecurityManagerBonding: Int](/documentation/iobluetooth/kbluetoothlesecuritymanagerbonding)
- [var kBluetoothLESecurityManagerNoBonding: Int](/documentation/iobluetooth/kbluetoothlesecuritymanagernobonding)
- [var kBluetoothLESecurityManagerReservedEnd: Int](/documentation/iobluetooth/kbluetoothlesecuritymanagerreservedend)
- [var kBluetoothLESecurityManagerReservedStart: Int](/documentation/iobluetooth/kbluetoothlesecuritymanagerreservedstart)
- [BluetoothSynchronousConnectionPacketType constants](/documentation/iobluetooth/bluetoothsynchronousconnectionpackettype-constants-6b7qe)

#### Constants

- [var kBluetoothSynchronousConnectionPacketType2EV3Omit: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettype2ev3omit)
- [var kBluetoothSynchronousConnectionPacketType2EV5Omit: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettype2ev5omit)
- [var kBluetoothSynchronousConnectionPacketType3EV3Omit: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettype3ev3omit)
- [var kBluetoothSynchronousConnectionPacketType3EV5Omit: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettype3ev5omit)
- [var kBluetoothSynchronousConnectionPacketTypeAll: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypeall)
- [var kBluetoothSynchronousConnectionPacketTypeEV3: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypeev3)
- [var kBluetoothSynchronousConnectionPacketTypeEV4: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypeev4)
- [var kBluetoothSynchronousConnectionPacketTypeEV5: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypeev5)
- [var kBluetoothSynchronousConnectionPacketTypeEnd: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypeend)
- [var kBluetoothSynchronousConnectionPacketTypeFutureUse: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypefutureuse)
- [var kBluetoothSynchronousConnectionPacketTypeHV1: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypehv1)
- [var kBluetoothSynchronousConnectionPacketTypeHV2: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypehv2)
- [var kBluetoothSynchronousConnectionPacketTypeHV3: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypehv3)
- [var kBluetoothSynchronousConnectionPacketTypeNone: Int](/documentation/iobluetooth/kbluetoothsynchronousconnectionpackettypenone)
- [BluetoothHCI command constants](/documentation/iobluetooth/bluetoothhci-command-constants-6buqn)

#### Constants

- [var kBluetoothHCICommandAMPTest: Int](/documentation/iobluetooth/kbluetoothhcicommandamptest)
- [var kBluetoothHCICommandAMPTestEnd: Int](/documentation/iobluetooth/kbluetoothhcicommandamptestend)
- [var kBluetoothHCICommandAcceptConnectionRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandacceptconnectionrequest)
- [var kBluetoothHCICommandAcceptSniffRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandacceptsniffrequest)
- [var kBluetoothHCICommandAcceptSynchronousConnectionRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandacceptsynchronousconnectionrequest)
- [var kBluetoothHCICommandAddSCOConnection: Int](/documentation/iobluetooth/kbluetoothhcicommandaddscoconnection)
- [var kBluetoothHCICommandAuthenticationRequested: Int](/documentation/iobluetooth/kbluetoothhcicommandauthenticationrequested)
- [var kBluetoothHCICommandChangeConnectionLinkKey: Int](/documentation/iobluetooth/kbluetoothhcicommandchangeconnectionlinkkey)
- [var kBluetoothHCICommandChangeConnectionPacketType: Int](/documentation/iobluetooth/kbluetoothhcicommandchangeconnectionpackettype)
- [var kBluetoothHCICommandChangeLocalName: Int](/documentation/iobluetooth/kbluetoothhcicommandchangelocalname)
- [var kBluetoothHCICommandCreateConnection: Int](/documentation/iobluetooth/kbluetoothhcicommandcreateconnection)
- [var kBluetoothHCICommandCreateConnectionCancel: Int](/documentation/iobluetooth/kbluetoothhcicommandcreateconnectioncancel)
- [var kBluetoothHCICommandCreateNewUnitKey: Int](/documentation/iobluetooth/kbluetoothhcicommandcreatenewunitkey)
- [var kBluetoothHCICommandDeleteReservedLTADDR: Int](/documentation/iobluetooth/kbluetoothhcicommanddeletereservedltaddr)
- [var kBluetoothHCICommandDeleteStoredLinkKey: Int](/documentation/iobluetooth/kbluetoothhcicommanddeletestoredlinkkey)
- [var kBluetoothHCICommandDisconnect: Int](/documentation/iobluetooth/kbluetoothhcicommanddisconnect)
- [var kBluetoothHCICommandEnableAMPReceiverReports: Int](/documentation/iobluetooth/kbluetoothhcicommandenableampreceiverreports)
- [var kBluetoothHCICommandEnableDeviceUnderTestMode: Int](/documentation/iobluetooth/kbluetoothhcicommandenabledeviceundertestmode)
- [var kBluetoothHCICommandEnhancedAcceptSynchronousConnectionRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandenhancedacceptsynchronousconnectionrequest)
- [var kBluetoothHCICommandEnhancedFlush: Int](/documentation/iobluetooth/kbluetoothhcicommandenhancedflush)
- [var kBluetoothHCICommandEnhancedSetupSynchronousConnection: Int](/documentation/iobluetooth/kbluetoothhcicommandenhancedsetupsynchronousconnection)
- [var kBluetoothHCICommandExitParkMode: Int](/documentation/iobluetooth/kbluetoothhcicommandexitparkmode)
- [var kBluetoothHCICommandExitPeriodicInquiryMode: Int](/documentation/iobluetooth/kbluetoothhcicommandexitperiodicinquirymode)
- [var kBluetoothHCICommandExitSniffMode: Int](/documentation/iobluetooth/kbluetoothhcicommandexitsniffmode)
- [var kBluetoothHCICommandFlowSpecification: Int](/documentation/iobluetooth/kbluetoothhcicommandflowspecification)
- [var kBluetoothHCICommandFlush: Int](/documentation/iobluetooth/kbluetoothhcicommandflush)
- [var kBluetoothHCICommandGetLinkQuality: Int](/documentation/iobluetooth/kbluetoothhcicommandgetlinkquality)
- [var kBluetoothHCICommandGetMWSTransportLayerConfiguration: Int](/documentation/iobluetooth/kbluetoothhcicommandgetmwstransportlayerconfiguration)
- [var kBluetoothHCICommandGroupHostController: Int](/documentation/iobluetooth/kbluetoothhcicommandgrouphostcontroller)
- [var kBluetoothHCICommandGroupInformational: Int](/documentation/iobluetooth/kbluetoothhcicommandgroupinformational)
- [var kBluetoothHCICommandGroupLinkControl: Int](/documentation/iobluetooth/kbluetoothhcicommandgrouplinkcontrol)
- [var kBluetoothHCICommandGroupLinkPolicy: Int](/documentation/iobluetooth/kbluetoothhcicommandgrouplinkpolicy)
- [var kBluetoothHCICommandGroupLogoTesting: Int](/documentation/iobluetooth/kbluetoothhcicommandgrouplogotesting)
- [var kBluetoothHCICommandGroupLowEnergy: Int](/documentation/iobluetooth/kbluetoothhcicommandgrouplowenergy)
- [var kBluetoothHCICommandGroupMax: Int](/documentation/iobluetooth/kbluetoothhcicommandgroupmax)
- [var kBluetoothHCICommandGroupNoOp: Int](/documentation/iobluetooth/kbluetoothhcicommandgroupnoop)
- [var kBluetoothHCICommandGroupStatus: Int](/documentation/iobluetooth/kbluetoothhcicommandgroupstatus)
- [var kBluetoothHCICommandGroupTesting: Int](/documentation/iobluetooth/kbluetoothhcicommandgrouptesting)
- [var kBluetoothHCICommandGroupVendorSpecific: Int](/documentation/iobluetooth/kbluetoothhcicommandgroupvendorspecific)
- [var kBluetoothHCICommandHoldMode: Int](/documentation/iobluetooth/kbluetoothhcicommandholdmode)
- [var kBluetoothHCICommandHostBufferSize: Int](/documentation/iobluetooth/kbluetoothhcicommandhostbuffersize)
- [var kBluetoothHCICommandHostNumberOfCompletedPackets: Int](/documentation/iobluetooth/kbluetoothhcicommandhostnumberofcompletedpackets)
- [var kBluetoothHCICommandIOCapabilityRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommandiocapabilityrequestnegativereply)
- [var kBluetoothHCICommandIOCapabilityRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommandiocapabilityrequestreply)
- [var kBluetoothHCICommandInquiry: Int](/documentation/iobluetooth/kbluetoothhcicommandinquiry)
- [var kBluetoothHCICommandInquiryCancel: Int](/documentation/iobluetooth/kbluetoothhcicommandinquirycancel)
- [var kBluetoothHCICommandLEAddDeviceToResolvingList: Int](/documentation/iobluetooth/kbluetoothhcicommandleadddevicetoresolvinglist)
- [var kBluetoothHCICommandLEAddDeviceToWhiteList: Int](/documentation/iobluetooth/kbluetoothhcicommandleadddevicetowhitelist)
- [var kBluetoothHCICommandLEClearResolvingList: Int](/documentation/iobluetooth/kbluetoothhcicommandleclearresolvinglist)
- [var kBluetoothHCICommandLEClearWhiteList: Int](/documentation/iobluetooth/kbluetoothhcicommandleclearwhitelist)
- [var kBluetoothHCICommandLEConnectionUpdate: Int](/documentation/iobluetooth/kbluetoothhcicommandleconnectionupdate)
- [var kBluetoothHCICommandLECreateConnection: Int](/documentation/iobluetooth/kbluetoothhcicommandlecreateconnection)
- [var kBluetoothHCICommandLECreateConnectionCancel: Int](/documentation/iobluetooth/kbluetoothhcicommandlecreateconnectioncancel)
- [var kBluetoothHCICommandLEEncrypt: Int](/documentation/iobluetooth/kbluetoothhcicommandleencrypt)
- [var kBluetoothHCICommandLEGenerateDHKey: Int](/documentation/iobluetooth/kbluetoothhcicommandlegeneratedhkey)
- [var kBluetoothHCICommandLELongTermKeyRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommandlelongtermkeyrequestnegativereply)
- [var kBluetoothHCICommandLELongTermKeyRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommandlelongtermkeyrequestreply)
- [var kBluetoothHCICommandLERand: Int](/documentation/iobluetooth/kbluetoothhcicommandlerand)
- [var kBluetoothHCICommandLEReadAdvertisingChannelTxPower: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadadvertisingchanneltxpower)
- [var kBluetoothHCICommandLEReadBufferSize: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadbuffersize)
- [var kBluetoothHCICommandLEReadChannelMap: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadchannelmap)
- [var kBluetoothHCICommandLEReadLocalP256PublicKey: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadlocalp256publickey)
- [var kBluetoothHCICommandLEReadLocalResolvableAddress: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadlocalresolvableaddress)
- [var kBluetoothHCICommandLEReadLocalSupportedFeatures: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadlocalsupportedfeatures)
- [var kBluetoothHCICommandLEReadMaximumDataLength: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadmaximumdatalength)
- [var kBluetoothHCICommandLEReadPeerResolvableAddress: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadpeerresolvableaddress)
- [var kBluetoothHCICommandLEReadRemoteUsedFeatures: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadremoteusedfeatures)
- [var kBluetoothHCICommandLEReadResolvingListSize: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadresolvinglistsize)
- [var kBluetoothHCICommandLEReadSuggestedDefaultDataLength: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadsuggesteddefaultdatalength)
- [var kBluetoothHCICommandLEReadSupportedStates: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadsupportedstates)
- [var kBluetoothHCICommandLEReadWhiteListSize: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadwhitelistsize)
- [var kBluetoothHCICommandLEReceiverTest: Int](/documentation/iobluetooth/kbluetoothhcicommandlereceivertest)
- [var kBluetoothHCICommandLERemoteConnectionParameterRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommandleremoteconnectionparameterrequestnegativereply)
- [var kBluetoothHCICommandLERemoteConnectionParameterRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommandleremoteconnectionparameterrequestreply)
- [var kBluetoothHCICommandLERemoveDeviceFromResolvingList: Int](/documentation/iobluetooth/kbluetoothhcicommandleremovedevicefromresolvinglist)
- [var kBluetoothHCICommandLERemoveDeviceFromWhiteList: Int](/documentation/iobluetooth/kbluetoothhcicommandleremovedevicefromwhitelist)
- [var kBluetoothHCICommandLESetAddressResolutionEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetaddressresolutionenable)
- [var kBluetoothHCICommandLESetAdvertiseEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetadvertiseenable)
- [var kBluetoothHCICommandLESetAdvertisingData: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetadvertisingdata)
- [var kBluetoothHCICommandLESetAdvertisingParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetadvertisingparameters)
- [var kBluetoothHCICommandLESetDataLength: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetdatalength)
- [var kBluetoothHCICommandLESetEventMask: Int](/documentation/iobluetooth/kbluetoothhcicommandleseteventmask)
- [var kBluetoothHCICommandLESetHostChannelClassification: Int](/documentation/iobluetooth/kbluetoothhcicommandlesethostchannelclassification)
- [var kBluetoothHCICommandLESetRandomAddress: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetrandomaddress)
- [var kBluetoothHCICommandLESetResolvablePrivateAddressTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetresolvableprivateaddresstimeout)
- [var kBluetoothHCICommandLESetScanEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetscanenable)
- [var kBluetoothHCICommandLESetScanParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetscanparameters)
- [var kBluetoothHCICommandLESetScanResponseData: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetscanresponsedata)
- [var kBluetoothHCICommandLEStartEncryption: Int](/documentation/iobluetooth/kbluetoothhcicommandlestartencryption)
- [var kBluetoothHCICommandLETestEnd: Int](/documentation/iobluetooth/kbluetoothhcicommandletestend)
- [var kBluetoothHCICommandLETransmitterTest: Int](/documentation/iobluetooth/kbluetoothhcicommandletransmittertest)
- [var kBluetoothHCICommandLEWriteSuggestedDefaultDataLength: Int](/documentation/iobluetooth/kbluetoothhcicommandlewritesuggesteddefaultdatalength)
- [var kBluetoothHCICommandLinkKeyRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommandlinkkeyrequestnegativereply)
- [var kBluetoothHCICommandLinkKeyRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommandlinkkeyrequestreply)
- [var kBluetoothHCICommandMasterLinkKey: Int](/documentation/iobluetooth/kbluetoothhcicommandmasterlinkkey)
- [var kBluetoothHCICommandMax: Int](/documentation/iobluetooth/kbluetoothhcicommandmax)
- [var kBluetoothHCICommandNoOp: Int](/documentation/iobluetooth/kbluetoothhcicommandnoop)
- [var kBluetoothHCICommandPINCodeRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommandpincoderequestnegativereply)
- [var kBluetoothHCICommandPINCodeRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommandpincoderequestreply)
- [var kBluetoothHCICommandParkMode: Int](/documentation/iobluetooth/kbluetoothhcicommandparkmode)
- [var kBluetoothHCICommandPeriodicInquiryMode: Int](/documentation/iobluetooth/kbluetoothhcicommandperiodicinquirymode)
- [var kBluetoothHCICommandQoSSetup: Int](/documentation/iobluetooth/kbluetoothhcicommandqossetup)
- [var kBluetoothHCICommandReadAFHChannelAssessmentMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadafhchannelassessmentmode)
- [var kBluetoothHCICommandReadAFHMappings: Int](/documentation/iobluetooth/kbluetoothhcicommandreadafhmappings)
- [var kBluetoothHCICommandReadAuthenticatedPayloadTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadauthenticatedpayloadtimeout)
- [var kBluetoothHCICommandReadAuthenticationEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandreadauthenticationenable)
- [var kBluetoothHCICommandReadAutomaticFlushTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadautomaticflushtimeout)
- [var kBluetoothHCICommandReadBestEffortFlushTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadbesteffortflushtimeout)
- [var kBluetoothHCICommandReadBufferSize: Int](/documentation/iobluetooth/kbluetoothhcicommandreadbuffersize)
- [var kBluetoothHCICommandReadClassOfDevice: Int](/documentation/iobluetooth/kbluetoothhcicommandreadclassofdevice)
- [var kBluetoothHCICommandReadClock: Int](/documentation/iobluetooth/kbluetoothhcicommandreadclock)
- [var kBluetoothHCICommandReadClockOffset: Int](/documentation/iobluetooth/kbluetoothhcicommandreadclockoffset)
- [var kBluetoothHCICommandReadConnectionAcceptTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadconnectionaccepttimeout)
- [var kBluetoothHCICommandReadCountryCode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadcountrycode)
- [var kBluetoothHCICommandReadCurrentIACLAP: Int](/documentation/iobluetooth/kbluetoothhcicommandreadcurrentiaclap)
- [var kBluetoothHCICommandReadDataBlockSize: Int](/documentation/iobluetooth/kbluetoothhcicommandreaddatablocksize)
- [var kBluetoothHCICommandReadDefaultErroneousDataReporting: Int](/documentation/iobluetooth/kbluetoothhcicommandreaddefaulterroneousdatareporting)
- [var kBluetoothHCICommandReadDefaultLinkPolicySettings: Int](/documentation/iobluetooth/kbluetoothhcicommandreaddefaultlinkpolicysettings)
- [var kBluetoothHCICommandReadDeviceAddress: Int](/documentation/iobluetooth/kbluetoothhcicommandreaddeviceaddress)
- [var kBluetoothHCICommandReadEncryptionKeySize: Int](/documentation/iobluetooth/kbluetoothhcicommandreadencryptionkeysize)
- [var kBluetoothHCICommandReadEncryptionMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadencryptionmode)
- [var kBluetoothHCICommandReadEnhancedTransmitPowerLevel: Int](/documentation/iobluetooth/kbluetoothhcicommandreadenhancedtransmitpowerlevel)
- [var kBluetoothHCICommandReadExtendedInquiryLength: Int](/documentation/iobluetooth/kbluetoothhcicommandreadextendedinquirylength)
- [var kBluetoothHCICommandReadExtendedInquiryResponse: Int](/documentation/iobluetooth/kbluetoothhcicommandreadextendedinquiryresponse)
- [var kBluetoothHCICommandReadExtendedPageTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadextendedpagetimeout)
- [var kBluetoothHCICommandReadFailedContactCounter: Int](/documentation/iobluetooth/kbluetoothhcicommandreadfailedcontactcounter)
- [var kBluetoothHCICommandReadFlowControlMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadflowcontrolmode)
- [var kBluetoothHCICommandReadHoldModeActivity: Int](/documentation/iobluetooth/kbluetoothhcicommandreadholdmodeactivity)
- [var kBluetoothHCICommandReadInquiryMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadinquirymode)
- [var kBluetoothHCICommandReadInquiryResponseTransmitPower: Int](/documentation/iobluetooth/kbluetoothhcicommandreadinquiryresponsetransmitpower)
- [var kBluetoothHCICommandReadInquiryScanActivity: Int](/documentation/iobluetooth/kbluetoothhcicommandreadinquiryscanactivity)
- [var kBluetoothHCICommandReadInquiryScanType: Int](/documentation/iobluetooth/kbluetoothhcicommandreadinquiryscantype)
- [var kBluetoothHCICommandReadLEHostSupported: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlehostsupported)
- [var kBluetoothHCICommandReadLMPHandle: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlmphandle)
- [var kBluetoothHCICommandReadLinkPolicySettings: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlinkpolicysettings)
- [var kBluetoothHCICommandReadLinkSupervisionTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlinksupervisiontimeout)
- [var kBluetoothHCICommandReadLocalAMPASSOC: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalampassoc)
- [var kBluetoothHCICommandReadLocalAMPInfo: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalampinfo)
- [var kBluetoothHCICommandReadLocalExtendedFeatures: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalextendedfeatures)
- [var kBluetoothHCICommandReadLocalName: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalname)
- [var kBluetoothHCICommandReadLocalOOBData: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocaloobdata)
- [var kBluetoothHCICommandReadLocalOOBExtendedData: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocaloobextendeddata)
- [var kBluetoothHCICommandReadLocalSupportedCodecs: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalsupportedcodecs)
- [var kBluetoothHCICommandReadLocalSupportedCommands: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalsupportedcommands)
- [var kBluetoothHCICommandReadLocalSupportedFeatures: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalsupportedfeatures)
- [var kBluetoothHCICommandReadLocalVersionInformation: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocalversioninformation)
- [var kBluetoothHCICommandReadLocationData: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlocationdata)
- [var kBluetoothHCICommandReadLogicalLinkAcceptTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadlogicallinkaccepttimeout)
- [var kBluetoothHCICommandReadLoopbackMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadloopbackmode)
- [var kBluetoothHCICommandReadNumberOfBroadcastRetransmissions: Int](/documentation/iobluetooth/kbluetoothhcicommandreadnumberofbroadcastretransmissions)
- [var kBluetoothHCICommandReadNumberOfSupportedIAC: Int](/documentation/iobluetooth/kbluetoothhcicommandreadnumberofsupportediac)
- [var kBluetoothHCICommandReadPINType: Int](/documentation/iobluetooth/kbluetoothhcicommandreadpintype)
- [var kBluetoothHCICommandReadPageScanActivity: Int](/documentation/iobluetooth/kbluetoothhcicommandreadpagescanactivity)
- [var kBluetoothHCICommandReadPageScanMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadpagescanmode)
- [var kBluetoothHCICommandReadPageScanPeriodMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadpagescanperiodmode)
- [var kBluetoothHCICommandReadPageScanType: Int](/documentation/iobluetooth/kbluetoothhcicommandreadpagescantype)
- [var kBluetoothHCICommandReadPageTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandreadpagetimeout)
- [var kBluetoothHCICommandReadRSSI: Int](/documentation/iobluetooth/kbluetoothhcicommandreadrssi)
- [var kBluetoothHCICommandReadRemoteExtendedFeatures: Int](/documentation/iobluetooth/kbluetoothhcicommandreadremoteextendedfeatures)
- [var kBluetoothHCICommandReadRemoteSupportedFeatures: Int](/documentation/iobluetooth/kbluetoothhcicommandreadremotesupportedfeatures)
- [var kBluetoothHCICommandReadRemoteVersionInformation: Int](/documentation/iobluetooth/kbluetoothhcicommandreadremoteversioninformation)
- [var kBluetoothHCICommandReadSCOFlowControlEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandreadscoflowcontrolenable)
- [var kBluetoothHCICommandReadScanEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandreadscanenable)
- [var kBluetoothHCICommandReadSecureConnectionsHostSupport: Int](/documentation/iobluetooth/kbluetoothhcicommandreadsecureconnectionshostsupport)
- [var kBluetoothHCICommandReadSimplePairingMode: Int](/documentation/iobluetooth/kbluetoothhcicommandreadsimplepairingmode)
- [var kBluetoothHCICommandReadStoredLinkKey: Int](/documentation/iobluetooth/kbluetoothhcicommandreadstoredlinkkey)
- [var kBluetoothHCICommandReadSynchronizationTrainParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandreadsynchronizationtrainparameters)
- [var kBluetoothHCICommandReadTransmitPowerLevel: Int](/documentation/iobluetooth/kbluetoothhcicommandreadtransmitpowerlevel)
- [var kBluetoothHCICommandReadVoiceSetting: Int](/documentation/iobluetooth/kbluetoothhcicommandreadvoicesetting)
- [var kBluetoothHCICommandReceiveSynchronizationTrain: Int](/documentation/iobluetooth/kbluetoothhcicommandreceivesynchronizationtrain)
- [var kBluetoothHCICommandRefreshEncryptionKey: Int](/documentation/iobluetooth/kbluetoothhcicommandrefreshencryptionkey)
- [var kBluetoothHCICommandRejectConnectionRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandrejectconnectionrequest)
- [var kBluetoothHCICommandRejectSniffRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandrejectsniffrequest)
- [var kBluetoothHCICommandRejectSynchronousConnectionRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandrejectsynchronousconnectionrequest)
- [var kBluetoothHCICommandRemoteNameRequest: Int](/documentation/iobluetooth/kbluetoothhcicommandremotenamerequest)
- [var kBluetoothHCICommandRemoteNameRequestCancel: Int](/documentation/iobluetooth/kbluetoothhcicommandremotenamerequestcancel)
- [var kBluetoothHCICommandRemoteOOBDataRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommandremoteoobdatarequestnegativereply)
- [var kBluetoothHCICommandRemoteOOBDataRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommandremoteoobdatarequestreply)
- [var kBluetoothHCICommandRemoteOOBExtendedDataRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommandremoteoobextendeddatarequestreply)
- [var kBluetoothHCICommandReset: Int](/documentation/iobluetooth/kbluetoothhcicommandreset)
- [var kBluetoothHCICommandResetFailedContactCounter: Int](/documentation/iobluetooth/kbluetoothhcicommandresetfailedcontactcounter)
- [var kBluetoothHCICommandRoleDiscovery: Int](/documentation/iobluetooth/kbluetoothhcicommandrolediscovery)
- [var kBluetoothHCICommandSendKeypressNotification: Int](/documentation/iobluetooth/kbluetoothhcicommandsendkeypressnotification)
- [var kBluetoothHCICommandSetAFHClassification: Int](/documentation/iobluetooth/kbluetoothhcicommandsetafhclassification)
- [var kBluetoothHCICommandSetConnectionEncryption: Int](/documentation/iobluetooth/kbluetoothhcicommandsetconnectionencryption)
- [var kBluetoothHCICommandSetConnectionlessSlaveBroadcast: Int](/documentation/iobluetooth/kbluetoothhcicommandsetconnectionlessslavebroadcast)
- [var kBluetoothHCICommandSetConnectionlessSlaveBroadcastData: Int](/documentation/iobluetooth/kbluetoothhcicommandsetconnectionlessslavebroadcastdata)
- [var kBluetoothHCICommandSetConnectionlessSlaveBroadcastReceive: Int](/documentation/iobluetooth/kbluetoothhcicommandsetconnectionlessslavebroadcastreceive)
- [var kBluetoothHCICommandSetEventFilter: Int](/documentation/iobluetooth/kbluetoothhcicommandseteventfilter)
- [var kBluetoothHCICommandSetEventMask: Int](/documentation/iobluetooth/kbluetoothhcicommandseteventmask)
- [var kBluetoothHCICommandSetEventMaskPageTwo: Int](/documentation/iobluetooth/kbluetoothhcicommandseteventmaskpagetwo)
- [var kBluetoothHCICommandSetExternalFrameConfiguration: Int](/documentation/iobluetooth/kbluetoothhcicommandsetexternalframeconfiguration)
- [var kBluetoothHCICommandSetHostControllerToHostFlowControl: Int](/documentation/iobluetooth/kbluetoothhcicommandsethostcontrollertohostflowcontrol)
- [var kBluetoothHCICommandSetMWSChannelParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandsetmwschannelparameters)
- [var kBluetoothHCICommandSetMWSPATTERNConfiguration: Int](/documentation/iobluetooth/kbluetoothhcicommandsetmwspatternconfiguration)
- [var kBluetoothHCICommandSetMWSScanFrequencyTable: Int](/documentation/iobluetooth/kbluetoothhcicommandsetmwsscanfrequencytable)
- [var kBluetoothHCICommandSetMWSSignaling: Int](/documentation/iobluetooth/kbluetoothhcicommandsetmwssignaling)
- [var kBluetoothHCICommandSetMWSTransportLayer: Int](/documentation/iobluetooth/kbluetoothhcicommandsetmwstransportlayer)
- [var kBluetoothHCICommandSetReservedLTADDR: Int](/documentation/iobluetooth/kbluetoothhcicommandsetreservedltaddr)
- [var kBluetoothHCICommandSetTriggeredClockCapture: Int](/documentation/iobluetooth/kbluetoothhcicommandsettriggeredclockcapture)
- [var kBluetoothHCICommandSetupSynchronousConnection: Int](/documentation/iobluetooth/kbluetoothhcicommandsetupsynchronousconnection)
- [var kBluetoothHCICommandShortRangeMode: Int](/documentation/iobluetooth/kbluetoothhcicommandshortrangemode)
- [var kBluetoothHCICommandSniffMode: Int](/documentation/iobluetooth/kbluetoothhcicommandsniffmode)
- [var kBluetoothHCICommandSniffSubrating: Int](/documentation/iobluetooth/kbluetoothhcicommandsniffsubrating)
- [var kBluetoothHCICommandStartSynchronizationTrain: Int](/documentation/iobluetooth/kbluetoothhcicommandstartsynchronizationtrain)
- [var kBluetoothHCICommandSwitchRole: Int](/documentation/iobluetooth/kbluetoothhcicommandswitchrole)
- [var kBluetoothHCICommandTruncatedPage: Int](/documentation/iobluetooth/kbluetoothhcicommandtruncatedpage)
- [var kBluetoothHCICommandTruncatedPageCancel: Int](/documentation/iobluetooth/kbluetoothhcicommandtruncatedpagecancel)
- [var kBluetoothHCICommandUserConfirmationRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommanduserconfirmationrequestnegativereply)
- [var kBluetoothHCICommandUserConfirmationRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommanduserconfirmationrequestreply)
- [var kBluetoothHCICommandUserPasskeyRequestNegativeReply: Int](/documentation/iobluetooth/kbluetoothhcicommanduserpasskeyrequestnegativereply)
- [var kBluetoothHCICommandUserPasskeyRequestReply: Int](/documentation/iobluetooth/kbluetoothhcicommanduserpasskeyrequestreply)
- [var kBluetoothHCICommandWriteAFHChannelAssessmentMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteafhchannelassessmentmode)
- [var kBluetoothHCICommandWriteAuthenticatedPayloadTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteauthenticatedpayloadtimeout)
- [var kBluetoothHCICommandWriteAuthenticationEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteauthenticationenable)
- [var kBluetoothHCICommandWriteAutomaticFlushTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteautomaticflushtimeout)
- [var kBluetoothHCICommandWriteBestEffortFlushTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwritebesteffortflushtimeout)
- [var kBluetoothHCICommandWriteClassOfDevice: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteclassofdevice)
- [var kBluetoothHCICommandWriteConnectionAcceptTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteconnectionaccepttimeout)
- [var kBluetoothHCICommandWriteCurrentIACLAP: Int](/documentation/iobluetooth/kbluetoothhcicommandwritecurrentiaclap)
- [var kBluetoothHCICommandWriteDefaultErroneousDataReporting: Int](/documentation/iobluetooth/kbluetoothhcicommandwritedefaulterroneousdatareporting)
- [var kBluetoothHCICommandWriteDefaultLinkPolicySettings: Int](/documentation/iobluetooth/kbluetoothhcicommandwritedefaultlinkpolicysettings)
- [var kBluetoothHCICommandWriteEncryptionMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteencryptionmode)
- [var kBluetoothHCICommandWriteExtendedInquiryLength: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteextendedinquirylength)
- [var kBluetoothHCICommandWriteExtendedInquiryResponse: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteextendedinquiryresponse)
- [var kBluetoothHCICommandWriteExtendedPageTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteextendedpagetimeout)
- [var kBluetoothHCICommandWriteFlowControlMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteflowcontrolmode)
- [var kBluetoothHCICommandWriteHoldModeActivity: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteholdmodeactivity)
- [var kBluetoothHCICommandWriteInquiryMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteinquirymode)
- [var kBluetoothHCICommandWriteInquiryResponseTransmitPower: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteinquiryresponsetransmitpower)
- [var kBluetoothHCICommandWriteInquiryScanActivity: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteinquiryscanactivity)
- [var kBluetoothHCICommandWriteInquiryScanType: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteinquiryscantype)
- [var kBluetoothHCICommandWriteLEHostSupported: Int](/documentation/iobluetooth/kbluetoothhcicommandwritelehostsupported)
- [var kBluetoothHCICommandWriteLinkPolicySettings: Int](/documentation/iobluetooth/kbluetoothhcicommandwritelinkpolicysettings)
- [var kBluetoothHCICommandWriteLinkSupervisionTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwritelinksupervisiontimeout)
- [var kBluetoothHCICommandWriteLocationData: Int](/documentation/iobluetooth/kbluetoothhcicommandwritelocationdata)
- [var kBluetoothHCICommandWriteLogicalLinkAcceptTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwritelogicallinkaccepttimeout)
- [var kBluetoothHCICommandWriteLoopbackMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteloopbackmode)
- [var kBluetoothHCICommandWriteNumberOfBroadcastRetransmissions: Int](/documentation/iobluetooth/kbluetoothhcicommandwritenumberofbroadcastretransmissions)
- [var kBluetoothHCICommandWritePINType: Int](/documentation/iobluetooth/kbluetoothhcicommandwritepintype)
- [var kBluetoothHCICommandWritePageScanActivity: Int](/documentation/iobluetooth/kbluetoothhcicommandwritepagescanactivity)
- [var kBluetoothHCICommandWritePageScanMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwritepagescanmode)
- [var kBluetoothHCICommandWritePageScanPeriodMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwritepagescanperiodmode)
- [var kBluetoothHCICommandWritePageScanType: Int](/documentation/iobluetooth/kbluetoothhcicommandwritepagescantype)
- [var kBluetoothHCICommandWritePageTimeout: Int](/documentation/iobluetooth/kbluetoothhcicommandwritepagetimeout)
- [var kBluetoothHCICommandWriteRemoteAMPASSOC: Int](/documentation/iobluetooth/kbluetoothhcicommandwriteremoteampassoc)
- [var kBluetoothHCICommandWriteSCOFlowControlEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandwritescoflowcontrolenable)
- [var kBluetoothHCICommandWriteScanEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandwritescanenable)
- [var kBluetoothHCICommandWriteSecureConnectionsHostSupport: Int](/documentation/iobluetooth/kbluetoothhcicommandwritesecureconnectionshostsupport)
- [var kBluetoothHCICommandWriteSimplePairingDebugMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwritesimplepairingdebugmode)
- [var kBluetoothHCICommandWriteSimplePairingMode: Int](/documentation/iobluetooth/kbluetoothhcicommandwritesimplepairingmode)
- [var kBluetoothHCICommandWriteStoredLinkKey: Int](/documentation/iobluetooth/kbluetoothhcicommandwritestoredlinkkey)
- [var kBluetoothHCICommandWriteSynchronizationTrainParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandwritesynchronizationtrainparameters)
- [var kBluetoothHCICommandWriteVoiceSetting: Int](/documentation/iobluetooth/kbluetoothhcicommandwritevoicesetting)
- [var kBluetoothHCIOpCodeNoOp: Int](/documentation/iobluetooth/kbluetoothhciopcodenoop)
- [var kBluetoothHCICommandLEAddDeviceToPeriodicAdvertiserList: Int](/documentation/iobluetooth/kbluetoothhcicommandleadddevicetoperiodicadvertiserlist)
- [var kBluetoothHCICommandLEClearAdvertisingSets: Int](/documentation/iobluetooth/kbluetoothhcicommandleclearadvertisingsets)
- [var kBluetoothHCICommandLEClearPeriodicAdvertiserList: Int](/documentation/iobluetooth/kbluetoothhcicommandleclearperiodicadvertiserlist)
- [var kBluetoothHCICommandLEEnhancedReceiverTest: Int](/documentation/iobluetooth/kbluetoothhcicommandleenhancedreceivertest)
- [var kBluetoothHCICommandLEEnhancedTransmitterTest: Int](/documentation/iobluetooth/kbluetoothhcicommandleenhancedtransmittertest)
- [var kBluetoothHCICommandLEExtendedCreateConnection: Int](/documentation/iobluetooth/kbluetoothhcicommandleextendedcreateconnection)
- [var kBluetoothHCICommandLEPeriodicAdvertisingCreateSync: Int](/documentation/iobluetooth/kbluetoothhcicommandleperiodicadvertisingcreatesync)
- [var kBluetoothHCICommandLEPeriodicAdvertisingCreateSyncCancel: Int](/documentation/iobluetooth/kbluetoothhcicommandleperiodicadvertisingcreatesynccancel)
- [var kBluetoothHCICommandLEPeriodicAdvertisingTerminateSync: Int](/documentation/iobluetooth/kbluetoothhcicommandleperiodicadvertisingterminatesync)
- [var kBluetoothHCICommandLEReadMaximumAdvertisingDataLength: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadmaximumadvertisingdatalength)
- [var kBluetoothHCICommandLEReadNumberofSupportedAdvertisingSets: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadnumberofsupportedadvertisingsets)
- [var kBluetoothHCICommandLEReadPeriodicAdvertiserListSize: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadperiodicadvertiserlistsize)
- [var kBluetoothHCICommandLEReadPhy: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadphy)
- [var kBluetoothHCICommandLEReadRFPathCompensation: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadrfpathcompensation)
- [var kBluetoothHCICommandLEReadTransmitPower: Int](/documentation/iobluetooth/kbluetoothhcicommandlereadtransmitpower)
- [var kBluetoothHCICommandLERemoveAdvertisingSet: Int](/documentation/iobluetooth/kbluetoothhcicommandleremoveadvertisingset)
- [var kBluetoothHCICommandLERemoveDeviceFromPeriodicAdvertiserList: Int](/documentation/iobluetooth/kbluetoothhcicommandleremovedevicefromperiodicadvertiserlist)
- [var kBluetoothHCICommandLESetAdvertisingSetRandomAddress: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetadvertisingsetrandomaddress)
- [var kBluetoothHCICommandLESetDefaultPhy: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetdefaultphy)
- [var kBluetoothHCICommandLESetExtendedAdvertisingData: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetextendedadvertisingdata)
- [var kBluetoothHCICommandLESetExtendedAdvertisingEnableCommand: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetextendedadvertisingenablecommand)
- [var kBluetoothHCICommandLESetExtendedAdvertisingParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetextendedadvertisingparameters)
- [var kBluetoothHCICommandLESetExtendedScanEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetextendedscanenable)
- [var kBluetoothHCICommandLESetExtendedScanParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetextendedscanparameters)
- [var kBluetoothHCICommandLESetExtendedScanResponseData: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetextendedscanresponsedata)
- [var kBluetoothHCICommandLESetPeriodicAdvertisingData: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetperiodicadvertisingdata)
- [var kBluetoothHCICommandLESetPeriodicAdvertisingEnable: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetperiodicadvertisingenable)
- [var kBluetoothHCICommandLESetPeriodicAdvertisingParameters: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetperiodicadvertisingparameters)
- [var kBluetoothHCICommandLESetPhy: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetphy)
- [var kBluetoothHCICommandLESetPrivacyMode: Int](/documentation/iobluetooth/kbluetoothhcicommandlesetprivacymode)
- [var kBluetoothHCICommandLEWriteRFPathCompensation: Int](/documentation/iobluetooth/kbluetoothhcicommandlewriterfpathcompensation)
- [var kBluetoothHCICommandSetConnectionlessPeripheralBroadcast: Int](/documentation/iobluetooth/kbluetoothhcicommandsetconnectionlessperipheralbroadcast)
- [var kBluetoothHCICommandSetConnectionlessPeripheralBroadcastData: Int](/documentation/iobluetooth/kbluetoothhcicommandsetconnectionlessperipheralbroadcastdata)
- [var kBluetoothHCICommandSetConnectionlessPeripheralBroadcastReceive: Int](/documentation/iobluetooth/kbluetoothhcicommandsetconnectionlessperipheralbroadcastreceive)
- [BluetoothHCIErroneousDataReporting constants](/documentation/iobluetooth/bluetoothhcierroneousdatareporting-constants-6tt47)

#### Constants

- [var kBluetoothHCIErroneousDataReportingDisabled: Int](/documentation/iobluetooth/kbluetoothhcierroneousdatareportingdisabled)
- [var kBluetoothHCIErroneousDataReportingEnabled: Int](/documentation/iobluetooth/kbluetoothhcierroneousdatareportingenabled)
- [var kBluetoothHCIErroneousDataReportingReservedEnd: Int](/documentation/iobluetooth/kbluetoothhcierroneousdatareportingreservedend)
- [var kBluetoothHCIErroneousDataReportingReservedStart: Int](/documentation/iobluetooth/kbluetoothhcierroneousdatareportingreservedstart)
- [BluetoothL2CAPTCICommand constants](/documentation/iobluetooth/bluetoothl2captcicommand-constants-6uh3g)

#### Constants

- [var kBluetoothL2CAPTCICommandL2CA_ConfigReq: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_configreq)
- [var kBluetoothL2CAPTCICommandL2CA_ConfigResp: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_configresp)
- [var kBluetoothL2CAPTCICommandL2CA_ConnectReq: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_connectreq)
- [var kBluetoothL2CAPTCICommandL2CA_ConnectResp: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_connectresp)
- [var kBluetoothL2CAPTCICommandL2CA_DisableCLT: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_disableclt)
- [var kBluetoothL2CAPTCICommandL2CA_DisconnectReq: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_disconnectreq)
- [var kBluetoothL2CAPTCICommandL2CA_DisconnectResp: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_disconnectresp)
- [var kBluetoothL2CAPTCICommandL2CA_EnableCLT: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_enableclt)
- [var kBluetoothL2CAPTCICommandL2CA_GetInfo: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_getinfo)
- [var kBluetoothL2CAPTCICommandL2CA_GroupAddMember: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_groupaddmember)
- [var kBluetoothL2CAPTCICommandL2CA_GroupClose: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_groupclose)
- [var kBluetoothL2CAPTCICommandL2CA_GroupCreate: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_groupcreate)
- [var kBluetoothL2CAPTCICommandL2CA_GroupMembership: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_groupmembership)
- [var kBluetoothL2CAPTCICommandL2CA_GroupRemoveMember: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_groupremovemember)
- [var kBluetoothL2CAPTCICommandL2CA_Ping: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_ping)
- [var kBluetoothL2CAPTCICommandL2CA_ReadData: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_readdata)
- [var kBluetoothL2CAPTCICommandL2CA_Reserved1: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_reserved1)
- [var kBluetoothL2CAPTCICommandL2CA_Reserved2: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_reserved2)
- [var kBluetoothL2CAPTCICommandL2CA_WriteData: Int](/documentation/iobluetooth/kbluetoothl2captcicommandl2ca_writedata)
- [var kBluetoothL2CAPTCICommandReserved: Int](/documentation/iobluetooth/kbluetoothl2captcicommandreserved)
- [BluetoothSDPErrorCode constants](/documentation/iobluetooth/bluetoothsdperrorcode-constants-70sy7)

#### Constants

- [var kBluetoothSDPErrorCodeInsufficientResources: Int](/documentation/iobluetooth/kbluetoothsdperrorcodeinsufficientresources)
- [var kBluetoothSDPErrorCodeInvalidContinuationState: Int](/documentation/iobluetooth/kbluetoothsdperrorcodeinvalidcontinuationstate)
- [var kBluetoothSDPErrorCodeInvalidPDUSize: Int](/documentation/iobluetooth/kbluetoothsdperrorcodeinvalidpdusize)
- [var kBluetoothSDPErrorCodeInvalidRequestSyntax: Int](/documentation/iobluetooth/kbluetoothsdperrorcodeinvalidrequestsyntax)
- [var kBluetoothSDPErrorCodeInvalidSDPVersion: Int](/documentation/iobluetooth/kbluetoothsdperrorcodeinvalidsdpversion)
- [var kBluetoothSDPErrorCodeInvalidServiceRecordHandle: Int](/documentation/iobluetooth/kbluetoothsdperrorcodeinvalidservicerecordhandle)
- [var kBluetoothSDPErrorCodeReserved: Int](/documentation/iobluetooth/kbluetoothsdperrorcodereserved)
- [var kBluetoothSDPErrorCodeReservedEnd: Int](/documentation/iobluetooth/kbluetoothsdperrorcodereservedend)
- [var kBluetoothSDPErrorCodeReservedStart: Int](/documentation/iobluetooth/kbluetoothsdperrorcodereservedstart)
- [var kBluetoothSDPErrorCodeSuccess: Int](/documentation/iobluetooth/kbluetoothsdperrorcodesuccess)
- [BluetoothConnectionHandleNone constants](/documentation/iobluetooth/bluetoothconnectionhandlenone-constants-73lg2)

#### Constants

- [var kBluetoothConnectionHandleNone: Int](/documentation/iobluetooth/kbluetoothconnectionhandlenone)
- [BluetoothVoiceSettingInputDataFormat constants](/documentation/iobluetooth/bluetoothvoicesettinginputdataformat-constants-7fqp2)

#### Constants

- [var kBluetoothVoiceSettingInputDataFormat1sComplement: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputdataformat1scomplement)
- [var kBluetoothVoiceSettingInputDataFormat2sComplement: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputdataformat2scomplement)
- [var kBluetoothVoiceSettingInputDataFormatMask: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputdataformatmask)
- [var kBluetoothVoiceSettingInputDataFormatSignMagnitude: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputdataformatsignmagnitude)
- [var kBluetoothVoiceSettingInputDataFormatUnsigned: Int](/documentation/iobluetooth/kbluetoothvoicesettinginputdataformatunsigned)
- [BluetoothPacketType constants](/documentation/iobluetooth/bluetoothpackettype-constants-7r3q3)

#### Constants

- [var kBluetoothPacketType2DH1Omit: Int](/documentation/iobluetooth/kbluetoothpackettype2dh1omit)
- [var kBluetoothPacketType2DH3Omit: Int](/documentation/iobluetooth/kbluetoothpackettype2dh3omit)
- [var kBluetoothPacketType2DH5Omit: Int](/documentation/iobluetooth/kbluetoothpackettype2dh5omit)
- [var kBluetoothPacketType3DH1Omit: Int](/documentation/iobluetooth/kbluetoothpackettype3dh1omit)
- [var kBluetoothPacketType3DH3Omit: Int](/documentation/iobluetooth/kbluetoothpackettype3dh3omit)
- [var kBluetoothPacketType3DM5Omit: Int](/documentation/iobluetooth/kbluetoothpackettype3dm5omit)
- [var kBluetoothPacketTypeAUX: Int](/documentation/iobluetooth/kbluetoothpackettypeaux)
- [var kBluetoothPacketTypeDH1: Int](/documentation/iobluetooth/kbluetoothpackettypedh1)
- [var kBluetoothPacketTypeDH3: Int](/documentation/iobluetooth/kbluetoothpackettypedh3)
- [var kBluetoothPacketTypeDH5: Int](/documentation/iobluetooth/kbluetoothpackettypedh5)
- [var kBluetoothPacketTypeDM1: Int](/documentation/iobluetooth/kbluetoothpackettypedm1)
- [var kBluetoothPacketTypeDM3: Int](/documentation/iobluetooth/kbluetoothpackettypedm3)
- [var kBluetoothPacketTypeDM5: Int](/documentation/iobluetooth/kbluetoothpackettypedm5)
- [var kBluetoothPacketTypeDV: Int](/documentation/iobluetooth/kbluetoothpackettypedv)
- [var kBluetoothPacketTypeEnd: Int](/documentation/iobluetooth/kbluetoothpackettypeend)
- [var kBluetoothPacketTypeHV1: Int](/documentation/iobluetooth/kbluetoothpackettypehv1)
- [var kBluetoothPacketTypeHV2: Int](/documentation/iobluetooth/kbluetoothpackettypehv2)
- [var kBluetoothPacketTypeHV3: Int](/documentation/iobluetooth/kbluetoothpackettypehv3)
- [var kBluetoothPacketTypeReserved1: Int](/documentation/iobluetooth/kbluetoothpackettypereserved1)
- [BluetoothAirMode constants](/documentation/iobluetooth/bluetoothairmode-constants-8csay)

#### Constants

- [var kBluetoothAirModeALawLog: Int](/documentation/iobluetooth/kbluetoothairmodealawlog)
- [var kBluetoothAirModeCVSD: Int](/documentation/iobluetooth/kbluetoothairmodecvsd)
- [var kBluetoothAirModeTransparentData: Int](/documentation/iobluetooth/kbluetoothairmodetransparentdata)
- [var kBluetoothAirModeULawLog: Int](/documentation/iobluetooth/kbluetoothairmodeulawlog)
- [BluetoothL2CAPPSM constants](/documentation/iobluetooth/bluetoothl2cappsm-constants-8dvu9)

#### Constants

- [var kBluetoothL2CAPPSMATT: Int](/documentation/iobluetooth/kbluetoothl2cappsmatt)
- [var kBluetoothL2CAPPSMAVCTP: Int](/documentation/iobluetooth/kbluetoothl2cappsmavctp)
- [var kBluetoothL2CAPPSMAVCTP_Browsing: Int](/documentation/iobluetooth/kbluetoothl2cappsmavctp_browsing)
- [var kBluetoothL2CAPPSMAVDTP: Int](/documentation/iobluetooth/kbluetoothl2cappsmavdtp)
- [var kBluetoothL2CAPPSMBNEP: Int](/documentation/iobluetooth/kbluetoothl2cappsmbnep)
- [var kBluetoothL2CAPPSMD2D: Int](/documentation/iobluetooth/kbluetoothl2cappsmd2d)
- [var kBluetoothL2CAPPSMDynamicEnd: Int](/documentation/iobluetooth/kbluetoothl2cappsmdynamicend)
- [var kBluetoothL2CAPPSMDynamicStart: Int](/documentation/iobluetooth/kbluetoothl2cappsmdynamicstart)
- [var kBluetoothL2CAPPSMHIDControl: Int](/documentation/iobluetooth/kbluetoothl2cappsmhidcontrol)
- [var kBluetoothL2CAPPSMHIDInterrupt: Int](/documentation/iobluetooth/kbluetoothl2cappsmhidinterrupt)
- [var kBluetoothL2CAPPSMNone: Int](/documentation/iobluetooth/kbluetoothl2cappsmnone)
- [var kBluetoothL2CAPPSMRFCOMM: Int](/documentation/iobluetooth/kbluetoothl2cappsmrfcomm)
- [var kBluetoothL2CAPPSMReservedEnd: Int](/documentation/iobluetooth/kbluetoothl2cappsmreservedend)
- [var kBluetoothL2CAPPSMReservedStart: Int](/documentation/iobluetooth/kbluetoothl2cappsmreservedstart)
- [var kBluetoothL2CAPPSMSDP: Int](/documentation/iobluetooth/kbluetoothl2cappsmsdp)
- [var kBluetoothL2CAPPSMTCS_BIN: Int](/documentation/iobluetooth/kbluetoothl2cappsmtcs_bin)
- [var kBluetoothL2CAPPSMTCS_BIN_Cordless: Int](/documentation/iobluetooth/kbluetoothl2cappsmtcs_bin_cordless)
- [var kBluetoothL2CAPPSMUID_C_Plane: Int](/documentation/iobluetooth/kbluetoothl2cappsmuid_c_plane)
- [var kBluetoothL2CAPPSMAACP: Int](/documentation/iobluetooth/kbluetoothl2cappsmaacp)
- [BluetoothDeviceClassMinor constants](/documentation/iobluetooth/bluetoothdeviceclassminor-constants-8ex6p)

#### Constants

- [var kBluetoothDeviceClassMinorAny: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorany)
- [var kBluetoothDeviceClassMinorAudioCamcorder: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiocamcorder)
- [var kBluetoothDeviceClassMinorAudioCar: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiocar)
- [var kBluetoothDeviceClassMinorAudioGamingToy: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiogamingtoy)
- [var kBluetoothDeviceClassMinorAudioHandsFree: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiohandsfree)
- [var kBluetoothDeviceClassMinorAudioHeadphones: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudioheadphones)
- [var kBluetoothDeviceClassMinorAudioHeadset: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudioheadset)
- [var kBluetoothDeviceClassMinorAudioHiFi: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiohifi)
- [var kBluetoothDeviceClassMinorAudioLoudspeaker: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudioloudspeaker)
- [var kBluetoothDeviceClassMinorAudioMicrophone: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiomicrophone)
- [var kBluetoothDeviceClassMinorAudioPortable: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudioportable)
- [var kBluetoothDeviceClassMinorAudioReserved1: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudioreserved1)
- [var kBluetoothDeviceClassMinorAudioReserved2: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudioreserved2)
- [var kBluetoothDeviceClassMinorAudioSetTopBox: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiosettopbox)
- [var kBluetoothDeviceClassMinorAudioUnclassified: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiounclassified)
- [var kBluetoothDeviceClassMinorAudioVCR: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiovcr)
- [var kBluetoothDeviceClassMinorAudioVideoCamera: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiovideocamera)
- [var kBluetoothDeviceClassMinorAudioVideoConferencing: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiovideoconferencing)
- [var kBluetoothDeviceClassMinorAudioVideoDisplayAndLoudspeaker: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiovideodisplayandloudspeaker)
- [var kBluetoothDeviceClassMinorAudioVideoMonitor: Int](/documentation/iobluetooth/kbluetoothdeviceclassminoraudiovideomonitor)
- [var kBluetoothDeviceClassMinorComputerDesktopWorkstation: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorcomputerdesktopworkstation)
- [var kBluetoothDeviceClassMinorComputerHandheld: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorcomputerhandheld)
- [var kBluetoothDeviceClassMinorComputerLaptop: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorcomputerlaptop)
- [var kBluetoothDeviceClassMinorComputerPalmSized: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorcomputerpalmsized)
- [var kBluetoothDeviceClassMinorComputerServer: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorcomputerserver)
- [var kBluetoothDeviceClassMinorComputerUnclassified: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorcomputerunclassified)
- [var kBluetoothDeviceClassMinorComputerWearable: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorcomputerwearable)
- [var kBluetoothDeviceClassMinorEnd: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorend)
- [var kBluetoothDeviceClassMinorHealthBloodPressureMonitor: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealthbloodpressuremonitor)
- [var kBluetoothDeviceClassMinorHealthDataDisplay: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealthdatadisplay)
- [var kBluetoothDeviceClassMinorHealthGlucoseMeter: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealthglucosemeter)
- [var kBluetoothDeviceClassMinorHealthHeartRateMonitor: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealthheartratemonitor)
- [var kBluetoothDeviceClassMinorHealthPulseOximeter: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealthpulseoximeter)
- [var kBluetoothDeviceClassMinorHealthScale: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealthscale)
- [var kBluetoothDeviceClassMinorHealthThermometer: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealththermometer)
- [var kBluetoothDeviceClassMinorHealthUndefined: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorhealthundefined)
- [var kBluetoothDeviceClassMinorImaging1Camera: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorimaging1camera)
- [var kBluetoothDeviceClassMinorImaging1Display: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorimaging1display)
- [var kBluetoothDeviceClassMinorImaging1Printer: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorimaging1printer)
- [var kBluetoothDeviceClassMinorImaging1Scanner: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorimaging1scanner)
- [var kBluetoothDeviceClassMinorImaging2Unclassified: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorimaging2unclassified)
- [var kBluetoothDeviceClassMinorNone: Int](/documentation/iobluetooth/kbluetoothdeviceclassminornone)
- [var kBluetoothDeviceClassMinorPeripheral1Combo: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral1combo)
- [var kBluetoothDeviceClassMinorPeripheral1Keyboard: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral1keyboard)
- [var kBluetoothDeviceClassMinorPeripheral1Pointing: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral1pointing)
- [var kBluetoothDeviceClassMinorPeripheral2AnyPointing: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2anypointing)
- [var kBluetoothDeviceClassMinorPeripheral2CardReader: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2cardreader)
- [var kBluetoothDeviceClassMinorPeripheral2DigitalPen: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2digitalpen)
- [var kBluetoothDeviceClassMinorPeripheral2DigitizerTablet: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2digitizertablet)
- [var kBluetoothDeviceClassMinorPeripheral2Gamepad: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2gamepad)
- [var kBluetoothDeviceClassMinorPeripheral2GesturalInputDevice: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2gesturalinputdevice)
- [var kBluetoothDeviceClassMinorPeripheral2HandheldScanner: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2handheldscanner)
- [var kBluetoothDeviceClassMinorPeripheral2Joystick: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2joystick)
- [var kBluetoothDeviceClassMinorPeripheral2RemoteControl: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2remotecontrol)
- [var kBluetoothDeviceClassMinorPeripheral2SensingDevice: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2sensingdevice)
- [var kBluetoothDeviceClassMinorPeripheral2Unclassified: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorperipheral2unclassified)
- [var kBluetoothDeviceClassMinorPhoneCellular: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorphonecellular)
- [var kBluetoothDeviceClassMinorPhoneCommonISDNAccess: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorphonecommonisdnaccess)
- [var kBluetoothDeviceClassMinorPhoneCordless: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorphonecordless)
- [var kBluetoothDeviceClassMinorPhoneSmartPhone: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorphonesmartphone)
- [var kBluetoothDeviceClassMinorPhoneUnclassified: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorphoneunclassified)
- [var kBluetoothDeviceClassMinorPhoneWiredModemOrVoiceGateway: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorphonewiredmodemorvoicegateway)
- [var kBluetoothDeviceClassMinorToyController: Int](/documentation/iobluetooth/kbluetoothdeviceclassminortoycontroller)
- [var kBluetoothDeviceClassMinorToyDollActionFigure: Int](/documentation/iobluetooth/kbluetoothdeviceclassminortoydollactionfigure)
- [var kBluetoothDeviceClassMinorToyGame: Int](/documentation/iobluetooth/kbluetoothdeviceclassminortoygame)
- [var kBluetoothDeviceClassMinorToyRobot: Int](/documentation/iobluetooth/kbluetoothdeviceclassminortoyrobot)
- [var kBluetoothDeviceClassMinorToyVehicle: Int](/documentation/iobluetooth/kbluetoothdeviceclassminortoyvehicle)
- [var kBluetoothDeviceClassMinorWearableGlasses: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorwearableglasses)
- [var kBluetoothDeviceClassMinorWearableHelmet: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorwearablehelmet)
- [var kBluetoothDeviceClassMinorWearableJacket: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorwearablejacket)
- [var kBluetoothDeviceClassMinorWearablePager: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorwearablepager)
- [var kBluetoothDeviceClassMinorWearableWristWatch: Int](/documentation/iobluetooth/kbluetoothdeviceclassminorwearablewristwatch)
- [BluetoothServiceClassMajor constants](/documentation/iobluetooth/bluetoothserviceclassmajor-constants-8lf4f)

#### Constants

- [var kBluetoothServiceClassMajorAny: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorany)
- [var kBluetoothServiceClassMajorAudio: Int](/documentation/iobluetooth/kbluetoothserviceclassmajoraudio)
- [var kBluetoothServiceClassMajorCapturing: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorcapturing)
- [var kBluetoothServiceClassMajorEnd: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorend)
- [var kBluetoothServiceClassMajorInformation: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorinformation)
- [var kBluetoothServiceClassMajorLimitedDiscoverableMode: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorlimiteddiscoverablemode)
- [var kBluetoothServiceClassMajorNetworking: Int](/documentation/iobluetooth/kbluetoothserviceclassmajornetworking)
- [var kBluetoothServiceClassMajorNone: Int](/documentation/iobluetooth/kbluetoothserviceclassmajornone)
- [var kBluetoothServiceClassMajorObjectTransfer: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorobjecttransfer)
- [var kBluetoothServiceClassMajorPositioning: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorpositioning)
- [var kBluetoothServiceClassMajorRendering: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorrendering)
- [var kBluetoothServiceClassMajorReserved1: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorreserved1)
- [var kBluetoothServiceClassMajorReserved2: Int](/documentation/iobluetooth/kbluetoothserviceclassmajorreserved2)
- [var kBluetoothServiceClassMajorTelephony: Int](/documentation/iobluetooth/kbluetoothserviceclassmajortelephony)
- [BluetoothL2CAPChannel constants](/documentation/iobluetooth/bluetoothl2capchannel-constants-8u90e)

#### Constants

- [var kBluetoothL2CAPChannelAMPManagerProtocol: Int](/documentation/iobluetooth/kbluetoothl2capchannelampmanagerprotocol)
- [var kBluetoothL2CAPChannelAttributeProtocol: Int](/documentation/iobluetooth/kbluetoothl2capchannelattributeprotocol)
- [var kBluetoothL2CAPChannelConnectionLessData: Int](/documentation/iobluetooth/kbluetoothl2capchannelconnectionlessdata)
- [var kBluetoothL2CAPChannelDynamicEnd: Int](/documentation/iobluetooth/kbluetoothl2capchanneldynamicend)
- [var kBluetoothL2CAPChannelDynamicStart: Int](/documentation/iobluetooth/kbluetoothl2capchanneldynamicstart)
- [var kBluetoothL2CAPChannelEnd: Int](/documentation/iobluetooth/kbluetoothl2capchannelend)
- [var kBluetoothL2CAPChannelLEAP: Int](/documentation/iobluetooth/kbluetoothl2capchannelleap)
- [var kBluetoothL2CAPChannelLEAS: Int](/documentation/iobluetooth/kbluetoothl2capchannelleas)
- [var kBluetoothL2CAPChannelLESignalling: Int](/documentation/iobluetooth/kbluetoothl2capchannellesignalling)
- [var kBluetoothL2CAPChannelMagnet: Int](/documentation/iobluetooth/kbluetoothl2capchannelmagnet)
- [var kBluetoothL2CAPChannelNull: Int](/documentation/iobluetooth/kbluetoothl2capchannelnull)
- [var kBluetoothL2CAPChannelReservedEnd: Int](/documentation/iobluetooth/kbluetoothl2capchannelreservedend)
- [var kBluetoothL2CAPChannelReservedStart: Int](/documentation/iobluetooth/kbluetoothl2capchannelreservedstart)
- [var kBluetoothL2CAPChannelSecurityManager: Int](/documentation/iobluetooth/kbluetoothl2capchannelsecuritymanager)
- [var kBluetoothL2CAPChannelSignalling: Int](/documentation/iobluetooth/kbluetoothl2capchannelsignalling)
- [var kBluetoothL2CAPChannelMagicPairing: Int](/documentation/iobluetooth/kbluetoothl2capchannelmagicpairing)
- [var kBluetoothL2CAPChannelAMPTestManager: Int](/documentation/iobluetooth/kbluetoothl2capchannelamptestmanager)
- [var kBluetoothL2CAPChannelBREDRSecurityManager: Int](/documentation/iobluetooth/kbluetoothl2capchannelbredrsecuritymanager)
- [BluetoothDeviceClassMajor constants](/documentation/iobluetooth/bluetoothdeviceclassmajor-constants-8xnan)

#### Constants

- [var kBluetoothDeviceClassMajorAny: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorany)
- [var kBluetoothDeviceClassMajorAudio: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajoraudio)
- [var kBluetoothDeviceClassMajorComputer: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorcomputer)
- [var kBluetoothDeviceClassMajorEnd: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorend)
- [var kBluetoothDeviceClassMajorHealth: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorhealth)
- [var kBluetoothDeviceClassMajorImaging: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorimaging)
- [var kBluetoothDeviceClassMajorLANAccessPoint: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorlanaccesspoint)
- [var kBluetoothDeviceClassMajorMiscellaneous: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajormiscellaneous)
- [var kBluetoothDeviceClassMajorNone: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajornone)
- [var kBluetoothDeviceClassMajorPeripheral: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorperipheral)
- [var kBluetoothDeviceClassMajorPhone: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorphone)
- [var kBluetoothDeviceClassMajorToy: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajortoy)
- [var kBluetoothDeviceClassMajorUnclassified: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorunclassified)
- [var kBluetoothDeviceClassMajorWearable: Int](/documentation/iobluetooth/kbluetoothdeviceclassmajorwearable)
- [BluetoothHCIUSBDeviceMatchingConstants](/documentation/iobluetooth/bluetoothhciusbdevicematchingconstants-8yru7)

#### Constants

- [var kBluetoothHCITransportUSBClassCode: Int](/documentation/iobluetooth/kbluetoothhcitransportusbclasscode)
- [var kBluetoothHCITransportUSBProtocolCode: Int](/documentation/iobluetooth/kbluetoothhcitransportusbprotocolcode)
- [var kBluetoothHCITransportUSBSubClassCode: Int](/documentation/iobluetooth/kbluetoothhcitransportusbsubclasscode)
- [MaximumNumberOfInquiryAccessCodes constants](/documentation/iobluetooth/maximumnumberofinquiryaccesscodes-constants-925y5)

#### Constants

- [var kMaximumNumberOfInquiryAccessCodes: Int](/documentation/iobluetooth/kmaximumnumberofinquiryaccesscodes)
- [BluetoothL2CAPInfoTypeMaxConnectionlessMTUSize constants](/documentation/iobluetooth/bluetoothl2capinfotypemaxconnectionlessmtusize-constants-92xuw)

#### Constants

- [var kBluetoothL2CAPInfoTypeMaxConnectionlessMTUSize: Int](/documentation/iobluetooth/kbluetoothl2capinfotypemaxconnectionlessmtusize)
- [BluetoothHCIError constants](/documentation/iobluetooth/bluetoothhcierror-constants-9nq10)

#### Constants

- [var kBluetoothHCIErrorACLConnectionAlreadyExists: Int](/documentation/iobluetooth/kbluetoothhcierroraclconnectionalreadyexists)
- [var kBluetoothHCIErrorAuthenticationFailure: Int](/documentation/iobluetooth/kbluetoothhcierrorauthenticationfailure)
- [var kBluetoothHCIErrorChannelClassificationNotSupported: Int](/documentation/iobluetooth/kbluetoothhcierrorchannelclassificationnotsupported)
- [var kBluetoothHCIErrorCommandDisallowed: Int](/documentation/iobluetooth/kbluetoothhcierrorcommanddisallowed)
- [var kBluetoothHCIErrorConnectionFailedToBeEstablished: Int](/documentation/iobluetooth/kbluetoothhcierrorconnectionfailedtobeestablished)
- [var kBluetoothHCIErrorConnectionRejectedDueToNoSuitableChannelFound: Int](/documentation/iobluetooth/kbluetoothhcierrorconnectionrejectedduetonosuitablechannelfound)
- [var kBluetoothHCIErrorConnectionTerminatedByLocalHost: Int](/documentation/iobluetooth/kbluetoothhcierrorconnectionterminatedbylocalhost)
- [var kBluetoothHCIErrorConnectionTerminatedDueToMICFailure: Int](/documentation/iobluetooth/kbluetoothhcierrorconnectionterminatedduetomicfailure)
- [var kBluetoothHCIErrorConnectionTimeout: Int](/documentation/iobluetooth/kbluetoothhcierrorconnectiontimeout)
- [var kBluetoothHCIErrorControllerBusy: Int](/documentation/iobluetooth/kbluetoothhcierrorcontrollerbusy)
- [var kBluetoothHCIErrorDifferentTransactionCollision: Int](/documentation/iobluetooth/kbluetoothhcierrordifferenttransactioncollision)
- [var kBluetoothHCIErrorDirectedAdvertisingTimeout: Int](/documentation/iobluetooth/kbluetoothhcierrordirectedadvertisingtimeout)
- [var kBluetoothHCIErrorEncryptionModeNotAcceptable: Int](/documentation/iobluetooth/kbluetoothhcierrorencryptionmodenotacceptable)
- [var kBluetoothHCIErrorExtendedInquiryResponseTooLarge: Int](/documentation/iobluetooth/kbluetoothhcierrorextendedinquiryresponsetoolarge)
- [var kBluetoothHCIErrorHardwareFailure: Int](/documentation/iobluetooth/kbluetoothhcierrorhardwarefailure)
- [var kBluetoothHCIErrorHostBusyPairing: Int](/documentation/iobluetooth/kbluetoothhcierrorhostbusypairing)
- [var kBluetoothHCIErrorHostRejectedLimitedResources: Int](/documentation/iobluetooth/kbluetoothhcierrorhostrejectedlimitedresources)
- [var kBluetoothHCIErrorHostRejectedRemoteDeviceIsPersonal: Int](/documentation/iobluetooth/kbluetoothhcierrorhostrejectedremotedeviceispersonal)
- [var kBluetoothHCIErrorHostRejectedSecurityReasons: Int](/documentation/iobluetooth/kbluetoothhcierrorhostrejectedsecurityreasons)
- [var kBluetoothHCIErrorHostRejectedUnacceptableDeviceAddress: Int](/documentation/iobluetooth/kbluetoothhcierrorhostrejectedunacceptabledeviceaddress)
- [var kBluetoothHCIErrorHostTimeout: Int](/documentation/iobluetooth/kbluetoothhcierrorhosttimeout)
- [var kBluetoothHCIErrorInstantPassed: Int](/documentation/iobluetooth/kbluetoothhcierrorinstantpassed)
- [var kBluetoothHCIErrorInsufficientSecurity: Int](/documentation/iobluetooth/kbluetoothhcierrorinsufficientsecurity)
- [var kBluetoothHCIErrorInvalidHCICommandParameters: Int](/documentation/iobluetooth/kbluetoothhcierrorinvalidhcicommandparameters)
- [var kBluetoothHCIErrorInvalidLMPParameters: Int](/documentation/iobluetooth/kbluetoothhcierrorinvalidlmpparameters)
- [var kBluetoothHCIErrorKeyMissing: Int](/documentation/iobluetooth/kbluetoothhcierrorkeymissing)
- [var kBluetoothHCIErrorLMPErrorTransactionCollision: Int](/documentation/iobluetooth/kbluetoothhcierrorlmperrortransactioncollision)
- [var kBluetoothHCIErrorLMPPDUNotAllowed: Int](/documentation/iobluetooth/kbluetoothhcierrorlmppdunotallowed)
- [var kBluetoothHCIErrorLMPResponseTimeout: Int](/documentation/iobluetooth/kbluetoothhcierrorlmpresponsetimeout)
- [var kBluetoothHCIErrorMACConnectionFailed: Int](/documentation/iobluetooth/kbluetoothhcierrormacconnectionfailed)
- [var kBluetoothHCIErrorMax: Int](/documentation/iobluetooth/kbluetoothhcierrormax)
- [var kBluetoothHCIErrorMaxNumberOfConnections: Int](/documentation/iobluetooth/kbluetoothhcierrormaxnumberofconnections)
- [var kBluetoothHCIErrorMaxNumberOfSCOConnectionsToADevice: Int](/documentation/iobluetooth/kbluetoothhcierrormaxnumberofscoconnectionstoadevice)
- [var kBluetoothHCIErrorMemoryFull: Int](/documentation/iobluetooth/kbluetoothhcierrormemoryfull)
- [var kBluetoothHCIErrorNoConnection: Int](/documentation/iobluetooth/kbluetoothhcierrornoconnection)
- [var kBluetoothHCIErrorOtherEndTerminatedConnectionAboutToPowerOff: Int](/documentation/iobluetooth/kbluetoothhcierrorotherendterminatedconnectionabouttopoweroff)
- [var kBluetoothHCIErrorOtherEndTerminatedConnectionLowResources: Int](/documentation/iobluetooth/kbluetoothhcierrorotherendterminatedconnectionlowresources)
- [var kBluetoothHCIErrorOtherEndTerminatedConnectionUserEnded: Int](/documentation/iobluetooth/kbluetoothhcierrorotherendterminatedconnectionuserended)
- [var kBluetoothHCIErrorPageTimeout: Int](/documentation/iobluetooth/kbluetoothhcierrorpagetimeout)
- [var kBluetoothHCIErrorPairingNotAllowed: Int](/documentation/iobluetooth/kbluetoothhcierrorpairingnotallowed)
- [var kBluetoothHCIErrorPairingWithUnitKeyNotSupported: Int](/documentation/iobluetooth/kbluetoothhcierrorpairingwithunitkeynotsupported)
- [var kBluetoothHCIErrorParameterOutOfMandatoryRange: Int](/documentation/iobluetooth/kbluetoothhcierrorparameteroutofmandatoryrange)
- [var kBluetoothHCIErrorQoSNotSupported: Int](/documentation/iobluetooth/kbluetoothhcierrorqosnotsupported)
- [var kBluetoothHCIErrorQoSRejected: Int](/documentation/iobluetooth/kbluetoothhcierrorqosrejected)
- [var kBluetoothHCIErrorQoSUnacceptableParameter: Int](/documentation/iobluetooth/kbluetoothhcierrorqosunacceptableparameter)
- [var kBluetoothHCIErrorRepeatedAttempts: Int](/documentation/iobluetooth/kbluetoothhcierrorrepeatedattempts)
- [var kBluetoothHCIErrorReservedSlotViolation: Int](/documentation/iobluetooth/kbluetoothhcierrorreservedslotviolation)
- [var kBluetoothHCIErrorRoleChangeNotAllowed: Int](/documentation/iobluetooth/kbluetoothhcierrorrolechangenotallowed)
- [var kBluetoothHCIErrorRoleSwitchFailed: Int](/documentation/iobluetooth/kbluetoothhcierrorroleswitchfailed)
- [var kBluetoothHCIErrorRoleSwitchPending: Int](/documentation/iobluetooth/kbluetoothhcierrorroleswitchpending)
- [var kBluetoothHCIErrorSCOAirModeRejected: Int](/documentation/iobluetooth/kbluetoothhcierrorscoairmoderejected)
- [var kBluetoothHCIErrorSCOIntervalRejected: Int](/documentation/iobluetooth/kbluetoothhcierrorscointervalrejected)
- [var kBluetoothHCIErrorSCOOffsetRejected: Int](/documentation/iobluetooth/kbluetoothhcierrorscooffsetrejected)
- [var kBluetoothHCIErrorSecureSimplePairingNotSupportedByHost: Int](/documentation/iobluetooth/kbluetoothhcierrorsecuresimplepairingnotsupportedbyhost)
- [var kBluetoothHCIErrorSuccess: Int](/documentation/iobluetooth/kbluetoothhcierrorsuccess)
- [var kBluetoothHCIErrorUnacceptableConnectionInterval: Int](/documentation/iobluetooth/kbluetoothhcierrorunacceptableconnectioninterval)
- [var kBluetoothHCIErrorUnitKeyUsed: Int](/documentation/iobluetooth/kbluetoothhcierrorunitkeyused)
- [var kBluetoothHCIErrorUnknownHCICommand: Int](/documentation/iobluetooth/kbluetoothhcierrorunknownhcicommand)
- [var kBluetoothHCIErrorUnknownLMPPDU: Int](/documentation/iobluetooth/kbluetoothhcierrorunknownlmppdu)
- [var kBluetoothHCIErrorUnspecifiedError: Int](/documentation/iobluetooth/kbluetoothhcierrorunspecifiederror)
- [var kBluetoothHCIErrorUnsupportedFeatureOrParameterValue: Int](/documentation/iobluetooth/kbluetoothhcierrorunsupportedfeatureorparametervalue)
- [var kBluetoothHCIErrorUnsupportedLMPParameterValue: Int](/documentation/iobluetooth/kbluetoothhcierrorunsupportedlmpparametervalue)
- [var kBluetoothHCIErrorUnsupportedRemoteFeature: Int](/documentation/iobluetooth/kbluetoothhcierrorunsupportedremotefeature)
- [var kBluetoothHCIErrorCoarseClockAdjustmentRejected: Int](/documentation/iobluetooth/kbluetoothhcierrorcoarseclockadjustmentrejected)
- [BluetoothPageScanMode constants](/documentation/iobluetooth/bluetoothpagescanmode-constants-9oksh)

#### Constants

- [var kBluetoothPageScanModeMandatory: Int](/documentation/iobluetooth/kbluetoothpagescanmodemandatory)
- [var kBluetoothPageScanModeOptional1: Int](/documentation/iobluetooth/kbluetoothpagescanmodeoptional1)
- [var kBluetoothPageScanModeOptional2: Int](/documentation/iobluetooth/kbluetoothpagescanmodeoptional2)
- [var kBluetoothPageScanModeOptional3: Int](/documentation/iobluetooth/kbluetoothpagescanmodeoptional3)
- [BluetoothSDPUUID16 constants](/documentation/iobluetooth/bluetoothsdpuuid16-constants-9owo4)

#### Constants

- [var kBluetoothSDPUUID16AVCTP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16avctp)
- [var kBluetoothSDPUUID16AVDTP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16avdtp)
- [var kBluetoothSDPUUID16BNEP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16bnep)
- [var kBluetoothSDPUUID16Base: Int](/documentation/iobluetooth/kbluetoothsdpuuid16base)
- [var kBluetoothSDPUUID16CMPT: Int](/documentation/iobluetooth/kbluetoothsdpuuid16cmpt)
- [var kBluetoothSDPUUID16FTP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16ftp)
- [var kBluetoothSDPUUID16HIDP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16hidp)
- [var kBluetoothSDPUUID16HTTP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16http)
- [var kBluetoothSDPUUID16HardcopyControlChannel: Int](/documentation/iobluetooth/kbluetoothsdpuuid16hardcopycontrolchannel)
- [var kBluetoothSDPUUID16HardcopyDataChannel: Int](/documentation/iobluetooth/kbluetoothsdpuuid16hardcopydatachannel)
- [var kBluetoothSDPUUID16HardcopyNotification: Int](/documentation/iobluetooth/kbluetoothsdpuuid16hardcopynotification)
- [var kBluetoothSDPUUID16IP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16ip)
- [var kBluetoothSDPUUID16L2CAP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16l2cap)
- [var kBluetoothSDPUUID16MCAPControlChannel: Int](/documentation/iobluetooth/kbluetoothsdpuuid16mcapcontrolchannel)
- [var kBluetoothSDPUUID16MCAPDataChannel: Int](/documentation/iobluetooth/kbluetoothsdpuuid16mcapdatachannel)
- [var kBluetoothSDPUUID16OBEX: Int](/documentation/iobluetooth/kbluetoothsdpuuid16obex)
- [var kBluetoothSDPUUID16RFCOMM: Int](/documentation/iobluetooth/kbluetoothsdpuuid16rfcomm)
- [var kBluetoothSDPUUID16SDP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16sdp)
- [var kBluetoothSDPUUID16TCP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16tcp)
- [var kBluetoothSDPUUID16TCSAT: Int](/documentation/iobluetooth/kbluetoothsdpuuid16tcsat)
- [var kBluetoothSDPUUID16TCSBIN: Int](/documentation/iobluetooth/kbluetoothsdpuuid16tcsbin)
- [var kBluetoothSDPUUID16UDI_C_Plane: Int](/documentation/iobluetooth/kbluetoothsdpuuid16udi_c_plane)
- [var kBluetoothSDPUUID16UDP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16udp)
- [var kBluetoothSDPUUID16UPNP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16upnp)
- [var kBluetoothSDPUUID16WSP: Int](/documentation/iobluetooth/kbluetoothsdpuuid16wsp)
- [var kBluetoothSDPUUID16ATT: Int](/documentation/iobluetooth/kbluetoothsdpuuid16att)
- [BluetoothPageScanPeriodMode constants](/documentation/iobluetooth/bluetoothpagescanperiodmode-constants-9v205)

#### Constants

- [var kBluetoothPageScanPeriodModeP0: Int](/documentation/iobluetooth/kbluetoothpagescanperiodmodep0)
- [var kBluetoothPageScanPeriodModeP1: Int](/documentation/iobluetooth/kbluetoothpagescanperiodmodep1)
- [var kBluetoothPageScanPeriodModeP2: Int](/documentation/iobluetooth/kbluetoothpagescanperiodmodep2)
- [Bluetooth role switch constants](/documentation/iobluetooth/bluetooth-roleswitch-constants-9vwwq)

#### Constants

- [var kBluetoothAllowRoleSwitch: Int](/documentation/iobluetooth/kbluetoothallowroleswitch)
- [var kBluetoothDontAllowRoleSwitch: Int](/documentation/iobluetooth/kbluetoothdontallowroleswitch)
- [Bluetooth access inquiry constants](/documentation/iobluetooth/bluetooth-access-constants-9y49w)

#### Constants

- [var kBluetoothGeneralInquiryAccessCodeIndex: Int](/documentation/iobluetooth/kbluetoothgeneralinquiryaccesscodeindex)
- [var kBluetoothGeneralInquiryAccessCodeLAPValue: Int](/documentation/iobluetooth/kbluetoothgeneralinquiryaccesscodelapvalue)
- [var kBluetoothLimitedInquiryAccessCodeEnd: Int](/documentation/iobluetooth/kbluetoothlimitedinquiryaccesscodeend)
- [var kBluetoothLimitedInquiryAccessCodeIndex: Int](/documentation/iobluetooth/kbluetoothlimitedinquiryaccesscodeindex)
- [var kBluetoothLimitedInquiryAccessCodeLAPValue: Int](/documentation/iobluetooth/kbluetoothlimitedinquiryaccesscodelapvalue)
- [BluetoothPageScanRepetitionMode constants](/documentation/iobluetooth/bluetoothpagescanrepetitionmode-constants-dctr)

#### Constants

- [var kBluetoothPageScanRepetitionModeR0: Int](/documentation/iobluetooth/kbluetoothpagescanrepetitionmoder0)
- [var kBluetoothPageScanRepetitionModeR1: Int](/documentation/iobluetooth/kbluetoothpagescanrepetitionmoder1)
- [var kBluetoothPageScanRepetitionModeR2: Int](/documentation/iobluetooth/kbluetoothpagescanrepetitionmoder2)
- [IOBluetooth Constants](/documentation/iobluetooth/iobluetooth-constants)

### Constants

- [var kFTSProgressPrecentageKey: Unmanaged<CFString>!](/documentation/iobluetooth/kftsprogressprecentagekey)
- [var kOBEXHeaderIDKeyAppParameters: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyappparameters)
- [var kOBEXHeaderIDKeyAuthorizationChallenge: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyauthorizationchallenge)
- [var kOBEXHeaderIDKeyAuthorizationResponse: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyauthorizationresponse)
- [var kOBEXHeaderIDKeyBody: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeybody)
- [var kOBEXHeaderIDKeyByteSequence: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeybytesequence)
- [var kOBEXHeaderIDKeyConnectionID: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyconnectionid)
- [var kOBEXHeaderIDKeyCount: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeycount)
- [var kOBEXHeaderIDKeyDescription: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeydescription)
- [var kOBEXHeaderIDKeyEndOfBody: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyendofbody)
- [var kOBEXHeaderIDKeyHTTP: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyhttp)
- [var kOBEXHeaderIDKeyLength: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeylength)
- [var kOBEXHeaderIDKeyName: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyname)
- [var kOBEXHeaderIDKeyObjectClass: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyobjectclass)
- [var kOBEXHeaderIDKeyTarget: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeytarget)
- [var kOBEXHeaderIDKeyTime4Byte: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeytime4byte)
- [var kOBEXHeaderIDKeyTimeISO: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeytimeiso)
- [var kOBEXHeaderIDKeyType: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeytype)
- [var kOBEXHeaderIDKeyUnknown1ByteQuantity: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyunknown1bytequantity)
- [var kOBEXHeaderIDKeyUnknown4ByteQuantity: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyunknown4bytequantity)
- [var kOBEXHeaderIDKeyUnknownByteSequence: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyunknownbytesequence)
- [var kOBEXHeaderIDKeyUnknownUnicodeText: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyunknownunicodetext)
- [var kOBEXHeaderIDKeyUserDefined: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeyuserdefined)
- [var kOBEXHeaderIDKeyWho: Unmanaged<CFString>!](/documentation/iobluetooth/kobexheaderidkeywho)
- [var kBluetoothHCIEventMaskAll64Bit: UInt64](/documentation/iobluetooth/kbluetoothhcieventmaskall64bit)
- [var kBluetoothHCIEventMaskDefault64Bit: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskdefault64bit)
- [var kBluetoothHCIEventMaskEncryptionChangeEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskencryptionchangeevent)
- [var kBluetoothHCIEventMaskEncryptionKeyRefreshCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskencryptionkeyrefreshcompleteevent)
- [var kBluetoothHCIEventMaskEnhancedFlushCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskenhancedflushcompleteevent)
- [var kBluetoothHCIEventMaskExtendedInquiryResultEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskextendedinquiryresultevent)
- [var kBluetoothHCIEventMaskFlowSpecificationCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskflowspecificationcompleteevent)
- [var kBluetoothHCIEventMaskIOCapabilityRequestEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskiocapabilityrequestevent)
- [var kBluetoothHCIEventMaskIOCapabilityRequestReplyEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskiocapabilityrequestreplyevent)
- [var kBluetoothHCIEventMaskInquiryResultWithRSSIEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskinquiryresultwithrssievent)
- [var kBluetoothHCIEventMaskKeypressNotificationEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskkeypressnotificationevent)
- [var kBluetoothHCIEventMaskLEDefault64Bit: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskledefault64bit)
- [var kBluetoothHCIEventMaskLEMetaEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmasklemetaevent)
- [var kBluetoothHCIEventMaskLinkSupervisionTimeoutChangedEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmasklinksupervisiontimeoutchangedevent)
- [var kBluetoothHCIEventMaskReadRemoteExtendedFeaturesCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskreadremoteextendedfeaturescompleteevent)
- [var kBluetoothHCIEventMaskRemoteHostSupportedFeaturesNotificationEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskremotehostsupportedfeaturesnotificationevent)
- [var kBluetoothHCIEventMaskRemoteOOBDataRequestEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskremoteoobdatarequestevent)
- [var kBluetoothHCIEventMaskSimplePairingCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmasksimplepairingcompleteevent)
- [var kBluetoothHCIEventMaskSniffSubratingEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmasksniffsubratingevent)
- [var kBluetoothHCIEventMaskSynchronousConnectionChangedEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmasksynchronousconnectionchangedevent)
- [var kBluetoothHCIEventMaskSynchronousConnectionCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmasksynchronousconnectioncompleteevent)
- [var kBluetoothHCIEventMaskUserConfirmationRequestEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskuserconfirmationrequestevent)
- [var kBluetoothHCIEventMaskUserPasskeyNotificationEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskuserpasskeynotificationevent)
- [var kBluetoothHCIEventMaskUserPasskeyRequestEvent: Int64](/documentation/iobluetooth/kbluetoothhcieventmaskuserpasskeyrequestevent)
- [var kBluetoothHCIEvnetMaskEnhancedFlushCompleteEvent: Int64](/documentation/iobluetooth/kbluetoothhcievnetmaskenhancedflushcompleteevent)
- [var kBluetoothHCIEvnetMaskLinkSupervisionTimeoutChangedEvent: Int64](/documentation/iobluetooth/kbluetoothhcievnetmasklinksupervisiontimeoutchangedevent)
- [var kBluetoothHCIInquiryResultsMaxResults: Int32](/documentation/iobluetooth/kbluetoothhciinquiryresultsmaxresults)
- [var kBluetoothLESMPMaxEncryptionKeySize: Int32](/documentation/iobluetooth/kbluetoothlesmpmaxencryptionkeysize)
- [var kBluetoothLESMPMinEncryptionKeySize: Int32](/documentation/iobluetooth/kbluetoothlesmpminencryptionkeysize)
- [var kBluetoothLESMPTimeout: Int32](/documentation/iobluetooth/kbluetoothlesmptimeout)
- [var kBluetoothTargetDoesNotRespondToCallbackExceptionName: String](/documentation/iobluetooth/kbluetoothtargetdoesnotrespondtocallbackexceptionname)
- [var kCharsetStringISO88591: String](/documentation/iobluetooth/kcharsetstringiso88591)
- [var kCharsetStringUTF8: String](/documentation/iobluetooth/kcharsetstringutf8)
- [var kEncodingString8Bit: String](/documentation/iobluetooth/kencodingstring8bit)
- [var kEncodingStringBase64: String](/documentation/iobluetooth/kencodingstringbase64)
- [var kEncodingStringQuotedPrintable: String](/documentation/iobluetooth/kencodingstringquotedprintable)
- [var kIOBluetoothDeviceInquiryInfoChangedNotification: String](/documentation/iobluetooth/kiobluetoothdeviceinquiryinfochangednotification)
- [var kIOBluetoothDeviceNameChangedNotification: String](/documentation/iobluetooth/kiobluetoothdevicenamechangednotification)
- [var kIOBluetoothDeviceNotificationNameConnected: String](/documentation/iobluetooth/kiobluetoothdevicenotificationnameconnected)
- [var kIOBluetoothDeviceNotificationNameDisconnected: String](/documentation/iobluetooth/kiobluetoothdevicenotificationnamedisconnected)
- [var kIOBluetoothDeviceServicesChangedNotification: String](/documentation/iobluetooth/kiobluetoothdeviceserviceschangednotification)
- [var kIOBluetoothL2CAPChannelDesiredOutgoingMTU: String](/documentation/iobluetooth/kiobluetoothl2capchanneldesiredoutgoingmtu)
- [var kIOBluetoothL2CAPChannelMaxAllowedIncomingMTU: String](/documentation/iobluetooth/kiobluetoothl2capchannelmaxallowedincomingmtu)
- [var kIOBluetoothObjectIDNULL: IOBluetoothObjectID](/documentation/iobluetooth/kiobluetoothobjectidnull)
- [var kInfoStringMaxLength: Int32](/documentation/iobluetooth/kinfostringmaxlength)
- [var kMaxChannelIDPerSide: Int32](/documentation/iobluetooth/kmaxchannelidperside)
- [var kBluetoothRoleBecomeCentral: Int](/documentation/iobluetooth/kbluetoothrolebecomecentral)
- [var kBluetoothRoleBecomeMaster: Int](/documentation/iobluetooth/kbluetoothrolebecomemaster)
- [var kBluetoothRoleRemainPeripheral: Int](/documentation/iobluetooth/kbluetoothroleremainperipheral)
- [var kBluetoothRoleRemainSlave: Int](/documentation/iobluetooth/kbluetoothroleremainslave)
- [IOBluetooth Functions](/documentation/iobluetooth/iobluetooth-functions)

### Functions

- [func IOBluetoothNSStringFromDeviceAddressColon(UnsafePointer<BluetoothDeviceAddress>!) -> String!](/documentation/iobluetooth/iobluetoothnsstringfromdeviceaddresscolon(_:))
- [func IOBluetoothPackDataList(UnsafeMutableRawPointer!, UnsafePointer<CChar>!, CVaListPointer) -> Int](/documentation/iobluetooth/iobluetoothpackdatalist(_:_:_:))
- [func IOBluetoothUnpackDataList(Int, UnsafeRawPointer!, UnsafePointer<CChar>!, CVaListPointer) -> Int](/documentation/iobluetooth/iobluetoothunpackdatalist(_:_:_:_:))
- [IOBluetooth Data Types](/documentation/iobluetooth/iobluetooth-data-types)

### Data Types

- [BluetoothAFHMode](/documentation/iobluetooth/bluetoothafhmode)
- [BluetoothAirMode](/documentation/iobluetooth/bluetoothairmode)
- [BluetoothAllowRoleSwitch](/documentation/iobluetooth/bluetoothallowroleswitch)
- [BluetoothAuthenticationRequirements](/documentation/iobluetooth/bluetoothauthenticationrequirements)
- [BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues)

#### Constants

- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequired: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequired)
- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequiredDedicatedBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequireddedicatedbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequiredGeneralBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequiredgeneralbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionNotRequiredNoBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionnotrequirednobonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequired: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequired)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequiredDedicatedBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequireddedicatedbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequiredGeneralBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequiredgeneralbonding)
- [var kBluetoothAuthenticationRequirementsMITMProtectionRequiredNoBonding: BluetoothAuthenticationRequirementsValues](/documentation/iobluetooth/kbluetoothauthenticationrequirementsmitmprotectionrequirednobonding)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothauthenticationrequirementsvalues/rawvalue)
- [BluetoothClassOfDevice](/documentation/iobluetooth/bluetoothclassofdevice)
- [BluetoothClockOffset](/documentation/iobluetooth/bluetoothclockoffset)
- [BluetoothCompanyIdentifers](/documentation/iobluetooth/bluetoothcompanyidentifers)

#### Constants

- [var kBluetoothCompanyIdentifer3Com: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer3com)
- [var kBluetoothCompanyIdentifer3DSP: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer3dsp)
- [var kBluetoothCompanyIdentifer3DiJoy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer3dijoy)
- [var kBluetoothCompanyIdentiferAPT: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferapt)
- [var kBluetoothCompanyIdentiferAVMBerlin: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferavmberlin)
- [var kBluetoothCompanyIdentiferAccelSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaccelsemiconductor)
- [var kBluetoothCompanyIdentiferAlcatel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferalcatel)
- [var kBluetoothCompanyIdentiferApple: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferapple)
- [var kBluetoothCompanyIdentiferAtherosCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferatheroscommunications)
- [var kBluetoothCompanyIdentiferAtmel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferatmel)
- [var kBluetoothCompanyIdentiferAvagoTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferavagotechnologies)
- [var kBluetoothCompanyIdentiferBandspeed: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbandspeed)
- [var kBluetoothCompanyIdentiferBluegiga: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbluegiga)
- [var kBluetoothCompanyIdentiferBluetoothSIG: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbluetoothsig)
- [var kBluetoothCompanyIdentiferBroadcom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbroadcom)
- [var kBluetoothCompanyIdentiferCATC: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercatc)
- [var kBluetoothCompanyIdentiferCONWISETechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconwisetechnology)
- [var kBluetoothCompanyIdentiferCTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferctechnologies)
- [var kBluetoothCompanyIdentiferCambridgeSiliconRadio: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercambridgesiliconradio)
- [var kBluetoothCompanyIdentiferCommil: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercommil)
- [var kBluetoothCompanyIdentiferConexantSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconexantsystems)
- [var kBluetoothCompanyIdentiferContinentialAutomotiveSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercontinentialautomotivesystems)
- [var kBluetoothCompanyIdentiferDigianswerAS: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdigiansweras)
- [var kBluetoothCompanyIdentiferEMMicroElectronicMarin: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferemmicroelectronicmarin)
- [var kBluetoothCompanyIdentiferEclipse: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifereclipse)
- [var kBluetoothCompanyIdentiferEricssonTechnologyLicensing: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferericssontechnologylicensing)
- [var kBluetoothCompanyIdentiferFree2Move: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfree2move)
- [var kBluetoothCompanyIdentiferGCTSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergctsemiconductor)
- [var kBluetoothCompanyIdentiferGennum: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergennum)
- [var kBluetoothCompanyIdentiferHarmonInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferharmoninternational)
- [var kBluetoothCompanyIdentiferHitachi: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhitachi)
- [var kBluetoothCompanyIdentiferIBM: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferibm)
- [var kBluetoothCompanyIdentiferIPextreme: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferipextreme)
- [var kBluetoothCompanyIdentiferInfineonTechnologiesAG: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinfineontechnologiesag)
- [var kBluetoothCompanyIdentiferIntegratedSiliconSolution: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferintegratedsiliconsolution)
- [var kBluetoothCompanyIdentiferIntegratedSystemSolution: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferintegratedsystemsolution)
- [var kBluetoothCompanyIdentiferIntel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferintel)
- [var kBluetoothCompanyIdentiferInteropIdentifier: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinteropidentifier)
- [var kBluetoothCompanyIdentiferInventel: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinventel)
- [var kBluetoothCompanyIdentiferJandM: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjandm)
- [var kBluetoothCompanyIdentiferKCTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkctechnology)
- [var kBluetoothCompanyIdentiferLucent: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlucent)
- [var kBluetoothCompanyIdentiferMacronixInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermacronixinternational)
- [var kBluetoothCompanyIdentiferMansella: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermansella)
- [var kBluetoothCompanyIdentiferMarvellTechnologyGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermarvelltechnologygroup)
- [var kBluetoothCompanyIdentiferMatsushitaElectricIndustrial: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermatsushitaelectricindustrial)
- [var kBluetoothCompanyIdentiferMediaTek: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermediatek)
- [var kBluetoothCompanyIdentiferMewTelTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermewteltechnology)
- [var kBluetoothCompanyIdentiferMicrosoft: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermicrosoft)
- [var kBluetoothCompanyIdentiferMistubishiElectric: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermistubishielectric)
- [var kBluetoothCompanyIdentiferMitelSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermitelsemiconductor)
- [var kBluetoothCompanyIdentiferMobilian: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermobilian)
- [var kBluetoothCompanyIdentiferMotorola: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermotorola)
- [var kBluetoothCompanyIdentiferNEC: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernec)
- [var kBluetoothCompanyIdentiferNewlogic: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernewlogic)
- [var kBluetoothCompanyIdentiferNokiaMobilePhones: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernokiamobilephones)
- [var kBluetoothCompanyIdentiferNordicSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernordicsemiconductor)
- [var kBluetoothCompanyIdentiferNorwoodSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernorwoodsystems)
- [var kBluetoothCompanyIdentiferOpenInterface: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferopeninterface)
- [var kBluetoothCompanyIdentiferParrotSA: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferparrotsa)
- [var kBluetoothCompanyIdentiferParthusTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferparthustechnologies)
- [var kBluetoothCompanyIdentiferPhilipsSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferphilipssemiconductor)
- [var kBluetoothCompanyIdentiferPlantronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferplantronics)
- [var kBluetoothCompanyIdentiferQualcomm: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcomm)
- [var kBluetoothCompanyIdentiferRFCMicroDevices: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrfcmicrodevices)
- [var kBluetoothCompanyIdentiferRTXTelecom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrtxtelecom)
- [var kBluetoothCompanyIdentiferRedMCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferredmcommunications)
- [var kBluetoothCompanyIdentiferRenesasTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrenesastechnology)
- [var kBluetoothCompanyIdentiferResearchInMotion: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferresearchinmotion)
- [var kBluetoothCompanyIdentiferRohdeandSchwarz: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrohdeandschwarz)
- [var kBluetoothCompanyIdentiferSTMicroelectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstmicroelectronics)
- [var kBluetoothCompanyIdentiferSeikoEpson: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferseikoepson)
- [var kBluetoothCompanyIdentiferSiRFTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersirftechnology)
- [var kBluetoothCompanyIdentiferSigniaTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersigniatechnologies)
- [var kBluetoothCompanyIdentiferSiliconWave: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersiliconwave)
- [var kBluetoothCompanyIdentiferSocketCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersocketcommunications)
- [var kBluetoothCompanyIdentiferSonyEricssonMobileCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersonyericssonmobilecommunications)
- [var kBluetoothCompanyIdentiferStaccatoCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstaccatocommunications)
- [var kBluetoothCompanyIdentiferSymbolTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersymboltechnologies)
- [var kBluetoothCompanyIdentiferSynopsys: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersynopsys)
- [var kBluetoothCompanyIdentiferSystemsAndChips: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersystemsandchips)
- [var kBluetoothCompanyIdentiferTTPCom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferttpcom)
- [var kBluetoothCompanyIdentiferTZeroTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertzerotechnologies)
- [var kBluetoothCompanyIdentiferTenovis: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertenovis)
- [var kBluetoothCompanyIdentiferTerax: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferterax)
- [var kBluetoothCompanyIdentiferTexasInstruments: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertexasinstruments)
- [var kBluetoothCompanyIdentiferToshiba: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertoshiba)
- [var kBluetoothCompanyIdentiferTransilica: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertransilica)
- [var kBluetoothCompanyIdentiferVisio: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervisio)
- [var kBluetoothCompanyIdentiferWavePlusTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwaveplustechnology)
- [var kBluetoothCompanyIdentiferWidcomm: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwidcomm)
- [var kBluetoothCompanyIdentiferZeevo: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzeevo)
- [var kBluetoothCompanyIdentifer9SolutionsOy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifer9solutionsoy)
- [var kBluetoothCompanyIdentiferAAMPofAmerica: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaampofamerica)
- [var kBluetoothCompanyIdentiferAAndDEngineering: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaanddengineering)
- [var kBluetoothCompanyIdentiferAAndRCambridge: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaandrcambridge)
- [var kBluetoothCompanyIdentiferACTSTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferactstechnologies)
- [var kBluetoothCompanyIdentiferAMICCOMElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferamiccomelectronics)
- [var kBluetoothCompanyIdentiferARCHOS: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferarchos)
- [var kBluetoothCompanyIdentiferARPDevicesUnlimited: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferarpdevicesunlimited)
- [var kBluetoothCompanyIdentiferAboveAverageOutcomes: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaboveaverageoutcomes)
- [var kBluetoothCompanyIdentiferAceSensor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferacesensor)
- [var kBluetoothCompanyIdentiferAceUni: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaceuni)
- [var kBluetoothCompanyIdentiferAdidas: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferadidas)
- [var kBluetoothCompanyIdentiferAdvancedPANMOBILSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferadvancedpanmobilsystems)
- [var kBluetoothCompanyIdentiferAirohaTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferairohatechnology)
- [var kBluetoothCompanyIdentiferAlpwise: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferalpwise)
- [var kBluetoothCompanyIdentiferAplix: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaplix)
- [var kBluetoothCompanyIdentiferAustcoCommunicationsSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferaustcocommunicationssystems)
- [var kBluetoothCompanyIdentiferAutonetMobile: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferautonetmobile)
- [var kBluetoothCompanyIdentiferBDETechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbdetechnology)
- [var kBluetoothCompanyIdentiferBandXIInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbandxiinternational)
- [var kBluetoothCompanyIdentiferBangAndOlufson: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbangandolufson)
- [var kBluetoothCompanyIdentiferBeatsElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbeatselectronics)
- [var kBluetoothCompanyIdentiferBeautifulEnterprise: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbeautifulenterprise)
- [var kBluetoothCompanyIdentiferBekey: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbekey)
- [var kBluetoothCompanyIdentiferBelkinInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbelkininternational)
- [var kBluetoothCompanyIdentiferBinauricSE: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbinauricse)
- [var kBluetoothCompanyIdentiferBioResearchAssociates: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbioresearchassociates)
- [var kBluetoothCompanyIdentiferBiosentronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbiosentronics)
- [var kBluetoothCompanyIdentiferBitsplitters: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbitsplitters)
- [var kBluetoothCompanyIdentiferBlueRadios: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferblueradios)
- [var kBluetoothCompanyIdentiferBose: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbose)
- [var kBluetoothCompanyIdentiferBriarTek: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferbriartek)
- [var kBluetoothCompanyIdentiferCaenRFID: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercaenrfid)
- [var kBluetoothCompanyIdentiferCinetix: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercinetix)
- [var kBluetoothCompanyIdentiferClarinoxTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferclarinoxtechnologies)
- [var kBluetoothCompanyIdentiferColorfy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercolorfy)
- [var kBluetoothCompanyIdentiferConnectBlueAB: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconnectblueab)
- [var kBluetoothCompanyIdentiferConnecteDevice: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferconnectedevice)
- [var kBluetoothCompanyIdentiferCreativeTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercreativetechnology)
- [var kBluetoothCompanyIdentiferCrystalCode: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifercrystalcode)
- [var kBluetoothCompanyIdentiferDanlers: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdanlers)
- [var kBluetoothCompanyIdentiferDeLormePublishingCompany: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdelormepublishingcompany)
- [var kBluetoothCompanyIdentiferDelphi: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdelphi)
- [var kBluetoothCompanyIdentiferDexcom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdexcom)
- [var kBluetoothCompanyIdentiferDialogSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferdialogsemiconductor)
- [var kBluetoothCompanyIdentiferEcotest: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferecotest)
- [var kBluetoothCompanyIdentiferEdenSoftwareConsultants: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferedensoftwareconsultants)
- [var kBluetoothCompanyIdentiferElcometer: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferelcometer)
- [var kBluetoothCompanyIdentiferElgatoSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferelgatosystems)
- [var kBluetoothCompanyIdentiferEquinux: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferequinux)
- [var kBluetoothCompanyIdentiferEvluma: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferevluma)
- [var kBluetoothCompanyIdentiferFreshtemp: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfreshtemp)
- [var kBluetoothCompanyIdentiferFuGoo: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfugoo)
- [var kBluetoothCompanyIdentiferFunaiElectric: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferfunaielectric)
- [var kBluetoothCompanyIdentiferGNNetcom: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergnnetcom)
- [var kBluetoothCompanyIdentiferGNResound: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergnresound)
- [var kBluetoothCompanyIdentiferGarminInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergarmininternational)
- [var kBluetoothCompanyIdentiferGeLo: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergelo)
- [var kBluetoothCompanyIdentiferGeneq: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergeneq)
- [var kBluetoothCompanyIdentiferGeneralMotors: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergeneralmotors)
- [var kBluetoothCompanyIdentiferGeoforce: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergeoforce)
- [var kBluetoothCompanyIdentiferGibsonGuitars: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergibsonguitars)
- [var kBluetoothCompanyIdentiferGimbal: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergimbal)
- [var kBluetoothCompanyIdentiferGoogle: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergoogle)
- [var kBluetoothCompanyIdentiferGreenThrottleGames: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergreenthrottlegames)
- [var kBluetoothCompanyIdentiferGroupSense: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifergroupsense)
- [var kBluetoothCompanyIdentiferHanlynnTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhanlynntechnologies)
- [var kBluetoothCompanyIdentiferHewlettPackard: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhewlettpackard)
- [var kBluetoothCompanyIdentiferHosiden: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferhosiden)
- [var kBluetoothCompanyIdentiferITechDynamicGlobalDistribution: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferitechdynamicglobaldistribution)
- [var kBluetoothCompanyIdentiferInMusicBrands: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinmusicbrands)
- [var kBluetoothCompanyIdentiferIngenieurSystemgruppeZahn: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferingenieursystemgruppezahn)
- [var kBluetoothCompanyIdentiferInnovativeYachtterSolutions: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferinnovativeyachttersolutions)
- [var kBluetoothCompanyIdentiferJawbone: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjawbone)
- [var kBluetoothCompanyIdentiferJiangsuToppowerAutomotiveElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjiangsutoppowerautomotiveelectronics)
- [var kBluetoothCompanyIdentiferJohnsonControls: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjohnsoncontrols)
- [var kBluetoothCompanyIdentiferJollyLogic: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferjollylogic)
- [var kBluetoothCompanyIdentiferKOUKAMM: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkoukamm)
- [var kBluetoothCompanyIdentiferKSTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkstechnologies)
- [var kBluetoothCompanyIdentiferKawantech: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkawantech)
- [var kBluetoothCompanyIdentiferKeiser: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkeiser)
- [var kBluetoothCompanyIdentiferKensingtonComputerProductsGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkensingtoncomputerproductsgroup)
- [var kBluetoothCompanyIdentiferKentDisplays: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferkentdisplays)
- [var kBluetoothCompanyIdentiferLGElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlgelectronics)
- [var kBluetoothCompanyIdentiferLSResearch: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlsresearch)
- [var kBluetoothCompanyIdentiferLairdTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlairdtechnologies)
- [var kBluetoothCompanyIdentiferLessWire: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlesswire)
- [var kBluetoothCompanyIdentiferLinak: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferlinak)
- [var kBluetoothCompanyIdentiferLudusHelsinki: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferludushelsinki)
- [var kBluetoothCompanyIdentiferMC10: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermc10)
- [var kBluetoothCompanyIdentiferMStarTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermstartechnologies)
- [var kBluetoothCompanyIdentiferMagnetiMarelli: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermagnetimarelli)
- [var kBluetoothCompanyIdentiferMesoInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermesointernational)
- [var kBluetoothCompanyIdentiferMetaWatch: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermetawatch)
- [var kBluetoothCompanyIdentiferMiCommand: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermicommand)
- [var kBluetoothCompanyIdentiferMicrochipTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermicrochiptechnology)
- [var kBluetoothCompanyIdentiferMindTree: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermindtree)
- [var kBluetoothCompanyIdentiferMisfitWearables: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermisfitwearables)
- [var kBluetoothCompanyIdentiferMonster: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermonster)
- [var kBluetoothCompanyIdentiferMorseProject: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermorseproject)
- [var kBluetoothCompanyIdentiferMusik: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifermusik)
- [var kBluetoothCompanyIdentiferNECLightning: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferneclightning)
- [var kBluetoothCompanyIdentiferNautilus: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernautilus)
- [var kBluetoothCompanyIdentiferNielsenKellerman: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernielsenkellerman)
- [var kBluetoothCompanyIdentiferNike: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifernike)
- [var kBluetoothCompanyIdentiferODMTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferodmtechnology)
- [var kBluetoothCompanyIdentiferOTLDynamics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferotldynamics)
- [var kBluetoothCompanyIdentiferOmegawave: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferomegawave)
- [var kBluetoothCompanyIdentiferOnsetComputer: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferonsetcomputer)
- [var kBluetoothCompanyIdentiferPLUSLocationSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpluslocationsystems)
- [var kBluetoothCompanyIdentiferPandaOcean: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpandaocean)
- [var kBluetoothCompanyIdentiferPassifSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpassifsemiconductor)
- [var kBluetoothCompanyIdentiferPayPal: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpaypal)
- [var kBluetoothCompanyIdentiferPeterSystemtechnik: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpetersystemtechnik)
- [var kBluetoothCompanyIdentiferPolarElectroEurope: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpolarelectroeurope)
- [var kBluetoothCompanyIdentiferPolarElectroOY: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferpolarelectrooy)
- [var kBluetoothCompanyIdentiferProctorAndGamble: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferproctorandgamble)
- [var kBluetoothCompanyIdentiferQualcommConnectedExperiences: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcommconnectedexperiences)
- [var kBluetoothCompanyIdentiferQualcommInnovationCenter: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcomminnovationcenter)
- [var kBluetoothCompanyIdentiferQualcommTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferqualcommtechnologies)
- [var kBluetoothCompanyIdentiferQuintic: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferquintic)
- [var kBluetoothCompanyIdentiferQuupa: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferquupa)
- [var kBluetoothCompanyIdentiferRDAMicroelectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrdamicroelectronics)
- [var kBluetoothCompanyIdentiferRalinkTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferralinktechnology)
- [var kBluetoothCompanyIdentiferRealtekSemiconductor: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrealteksemiconductor)
- [var kBluetoothCompanyIdentiferRivieraWaves: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferrivierawaves)
- [var kBluetoothCompanyIdentiferSPowerElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferspowerelectronics)
- [var kBluetoothCompanyIdentiferSRMedizinelektronik: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersrmedizinelektronik)
- [var kBluetoothCompanyIdentiferSamsungElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersamsungelectronics)
- [var kBluetoothCompanyIdentiferSarisCyclingGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersariscyclinggroup)
- [var kBluetoothCompanyIdentiferSeersTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferseerstechnology)
- [var kBluetoothCompanyIdentiferSelflyBV: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferselflybv)
- [var kBluetoothCompanyIdentiferSemilink: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersemilink)
- [var kBluetoothCompanyIdentiferSennheiserCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersennheisercommunications)
- [var kBluetoothCompanyIdentiferServerTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferservertechnology)
- [var kBluetoothCompanyIdentiferShangHaiSuperSmartElectronics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifershanghaisupersmartelectronics)
- [var kBluetoothCompanyIdentiferShenzhenExcelsecuDataTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifershenzhenexcelsecudatatechnology)
- [var kBluetoothCompanyIdentiferSmartifier: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersmartifier)
- [var kBluetoothCompanyIdentiferSoundID: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersoundid)
- [var kBluetoothCompanyIdentiferSportsTrackingTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersportstrackingtechnologies)
- [var kBluetoothCompanyIdentiferStalmartTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstalmarttechnology)
- [var kBluetoothCompanyIdentiferStanleyBlackAndDecker: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstanleyblackanddecker)
- [var kBluetoothCompanyIdentiferStarkeyLaboratories: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstarkeylaboratories)
- [var kBluetoothCompanyIdentiferStickNFind: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersticknfind)
- [var kBluetoothCompanyIdentiferStonestreetOne: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferstonestreetone)
- [var kBluetoothCompanyIdentiferSummitDataCommunications: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersummitdatacommunications)
- [var kBluetoothCompanyIdentiferSuuntoOy: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifersuuntooy)
- [var kBluetoothCompanyIdentiferSwirlNetworks: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferswirlnetworks)
- [var kBluetoothCompanyIdentiferTaixingbangTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertaixingbangtechnology)
- [var kBluetoothCompanyIdentiferTelitWirelessSolutions: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertelitwirelesssolutions)
- [var kBluetoothCompanyIdentiferThinkOptics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferthinkoptics)
- [var kBluetoothCompanyIdentiferTimeKeepingSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertimekeepingsystems)
- [var kBluetoothCompanyIdentiferTimexGroup: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertimexgroup)
- [var kBluetoothCompanyIdentiferTomTomInternational: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertomtominternational)
- [var kBluetoothCompanyIdentiferTopconPositioningSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertopconpositioningsystems)
- [var kBluetoothCompanyIdentiferTreLab: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertrelab)
- [var kBluetoothCompanyIdentiferTypeProducts: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertypeproducts)
- [var kBluetoothCompanyIdentiferUbiquitousComputingTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferubiquitouscomputingtechnology)
- [var kBluetoothCompanyIdentiferUniversalElectriconics: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferuniversalelectriconics)
- [var kBluetoothCompanyIdentiferVSNTechnologies: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervsntechnologies)
- [var kBluetoothCompanyIdentiferValenceTech: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervalencetech)
- [var kBluetoothCompanyIdentiferVertu: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervertu)
- [var kBluetoothCompanyIdentiferVisteon: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervisteon)
- [var kBluetoothCompanyIdentiferVoyetraTurtleBeach: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervoyetraturtlebeach)
- [var kBluetoothCompanyIdentiferVtrackSystems: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifervtracksystems)
- [var kBluetoothCompanyIdentiferWicentric: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwicentric)
- [var kBluetoothCompanyIdentiferWilliamDemantHolding: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwilliamdemantholding)
- [var kBluetoothCompanyIdentiferWitronTechnology: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwitrontechnology)
- [var kBluetoothCompanyIdentiferWuXiVimicro: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferwuxivimicro)
- [var kBluetoothCompanyIdentiferZero1TV: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzero1tv)
- [var kBluetoothCompanyIdentiferZomm: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzomm)
- [var kBluetoothCompanyIdentiferZscanSoftware: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentiferzscansoftware)
- [var kBluetoothCompanyIdentifertxtrGMBH: BluetoothCompanyIdentifers](/documentation/iobluetooth/kbluetoothcompanyidentifertxtrgmbh)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothcompanyidentifers/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothcompanyidentifers/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothcompanyidentifers/rawvalue)
- [BluetoothConnectionHandle](/documentation/iobluetooth/bluetoothconnectionhandle)
- [BluetoothDeviceClassMajor](/documentation/iobluetooth/bluetoothdeviceclassmajor)
- [BluetoothDeviceClassMinor](/documentation/iobluetooth/bluetoothdeviceclassminor)
- [BluetoothDeviceName](/documentation/iobluetooth/bluetoothdevicename)
- [BluetoothEncryptionEnable](/documentation/iobluetooth/bluetoothencryptionenable)
- [BluetoothFeatureBits](/documentation/iobluetooth/bluetoothfeaturebits)

#### Constants

- [var kBluetoothFeature3SlotEnhancedDataRateACLPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeature3slotenhanceddatarateaclpackets)
- [var kBluetoothFeature3SlotEnhancedDataRateeSCOPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeature3slotenhanceddatarateescopackets)
- [var kBluetoothFeature5SlotEnhancedDataRateACLPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeature5slotenhanceddatarateaclpackets)
- [var kBluetoothFeatureAFHCapableMaster: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhcapablemaster)
- [var kBluetoothFeatureAFHCapableSlave: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhcapableslave)
- [var kBluetoothFeatureAFHClassificationMaster: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhclassificationmaster)
- [var kBluetoothFeatureAFHClassificationSlave: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhclassificationslave)
- [var kBluetoothFeatureALawLog: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturealawlog)
- [var kBluetoothFeatureAbsenceMasks: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureabsencemasks)
- [var kBluetoothFeatureAliasAuhentication: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturealiasauhentication)
- [var kBluetoothFeatureBroadcastEncryption: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturebroadcastencryption)
- [var kBluetoothFeatureCVSD: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturecvsd)
- [var kBluetoothFeatureChannelQuality: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturechannelquality)
- [var kBluetoothFeatureEV4Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureev4packets)
- [var kBluetoothFeatureEV5Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureev5packets)
- [var kBluetoothFeatureEncapsulatedPDU: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureencapsulatedpdu)
- [var kBluetoothFeatureEncryption: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureencryption)
- [var kBluetoothFeatureEnhancedDataRateACL2MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateacl2mbpsmode)
- [var kBluetoothFeatureEnhancedDataRateACL3MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateacl3mbpsmode)
- [var kBluetoothFeatureEnhancedDataRateeSCO2MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateesco2mbpsmode)
- [var kBluetoothFeatureEnhancedDataRateeSCO3MbpsMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhanceddatarateesco3mbpsmode)
- [var kBluetoothFeatureEnhancedInquiryScan: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureenhancedinquiryscan)
- [var kBluetoothFeatureErroneousDataReporting: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureerroneousdatareporting)
- [var kBluetoothFeatureExtendedFeatures: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureextendedfeatures)
- [var kBluetoothFeatureExtendedInquiryResponse: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureextendedinquiryresponse)
- [var kBluetoothFeatureExtendedSCOLink: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureextendedscolink)
- [var kBluetoothFeatureFiveSlotPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturefiveslotpackets)
- [var kBluetoothFeatureFlowControlLagBit0: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureflowcontrollagbit0)
- [var kBluetoothFeatureFlowControlLagBit1: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureflowcontrollagbit1)
- [var kBluetoothFeatureFlowControlLagBit2: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureflowcontrollagbit2)
- [var kBluetoothFeatureHV2Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturehv2packets)
- [var kBluetoothFeatureHV3Packets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturehv3packets)
- [var kBluetoothFeatureHoldMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureholdmode)
- [var kBluetoothFeatureInquiryTransmissionPowerLevel: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureinquirytransmissionpowerlevel)
- [var kBluetoothFeatureInterlacedInquiryScan: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureinterlacedinquiryscan)
- [var kBluetoothFeatureInterlacedPageScan: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureinterlacedpagescan)
- [var kBluetoothFeatureLESupportedController: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturelesupportedcontroller)
- [var kBluetoothFeatureLinkSupervisionTimeoutChangedEvent: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturelinksupervisiontimeoutchangedevent)
- [var kBluetoothFeatureNonFlushablePacketBoundaryFlag: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturenonflushablepacketboundaryflag)
- [var kBluetoothFeaturePagingScheme: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepagingscheme)
- [var kBluetoothFeatureParkMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureparkmode)
- [var kBluetoothFeaturePauseEncryption: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepauseencryption)
- [var kBluetoothFeaturePowerControl: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepowercontrol)
- [var kBluetoothFeaturePowerControlRequests: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturepowercontrolrequests)
- [var kBluetoothFeatureRSSI: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturerssi)
- [var kBluetoothFeatureRSSIWithInquiryResult: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturerssiwithinquiryresult)
- [var kBluetoothFeatureSCOLink: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturescolink)
- [var kBluetoothFeatureScatterMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturescattermode)
- [var kBluetoothFeatureSecureSimplePairing: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturesecuresimplepairing)
- [var kBluetoothFeatureSlotOffset: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureslotoffset)
- [var kBluetoothFeatureSniffMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturesniffmode)
- [var kBluetoothFeatureSniffSubrating: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturesniffsubrating)
- [var kBluetoothFeatureSwitchRoles: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureswitchroles)
- [var kBluetoothFeatureThreeSlotPackets: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturethreeslotpackets)
- [var kBluetoothFeatureTimingAccuracy: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturetimingaccuracy)
- [var kBluetoothFeatureTransparentSCOData: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeaturetransparentscodata)
- [var kBluetoothFeatureULawLog: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureulawlog)
- [var KBluetoothExtendedFeatureSecureConnectionsHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturesecureconnectionshostmode)
- [var kBluetoothExtendedFeatureLEAndBREDRToSameDeviceHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeatureleandbredrtosamedevicehostmode)
- [var kBluetoothExtendedFeatureLESupportedHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturelesupportedhostmode)
- [var kBluetoothExtendedFeaturePing: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeatureping)
- [var kBluetoothExtendedFeatureReserved: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturereserved)
- [var kBluetoothExtendedFeatureSecureConnectionsControllerSupport: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturesecureconnectionscontrollersupport)
- [var kBluetoothExtendedFeatureSimpleSecurePairingHostMode: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturesimplesecurepairinghostmode)
- [var kBluetoothExtendedFeatureSlotAvailabilityMask: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeatureslotavailabilitymask)
- [var kBluetoothExtendedFeatureTrainNudging: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothextendedfeaturetrainnudging)
- [var kBluetoothFeatureAFHCapablePeripheral: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhcapableperipheral)
- [var kBluetoothFeatureAFHClassificationPeripheral: BluetoothFeatureBits](/documentation/iobluetooth/kbluetoothfeatureafhclassificationperipheral)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothfeaturebits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothfeaturebits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothfeaturebits/rawvalue)
- [BluetoothHCIACLDataByteCount](/documentation/iobluetooth/bluetoothhciacldatabytecount)
- [BluetoothHCIAFHChannelAssessmentMode](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmode)
- [BluetoothHCIAFHChannelAssessmentModes](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes)

#### Constants

- [var kAFHChannelAssessmentModeDisabled: BluetoothHCIAFHChannelAssessmentModes](/documentation/iobluetooth/kafhchannelassessmentmodedisabled)
- [var kAFHChannelAssessmentModeEnabled: BluetoothHCIAFHChannelAssessmentModes](/documentation/iobluetooth/kafhchannelassessmentmodeenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciafhchannelassessmentmodes/rawvalue)
- [BluetoothHCIAuthenticationEnable](/documentation/iobluetooth/bluetoothhciauthenticationenable)
- [BluetoothHCIAuthentionEnableModes](/documentation/iobluetooth/bluetoothhciauthentionenablemodes)

#### Constants

- [var kAuthenticationDisabled: BluetoothHCIAuthentionEnableModes](/documentation/iobluetooth/kauthenticationdisabled)
- [var kAuthenticationEnabled: BluetoothHCIAuthentionEnableModes](/documentation/iobluetooth/kauthenticationenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciauthentionenablemodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciauthentionenablemodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciauthentionenablemodes/rawvalue)
- [BluetoothHCIAutomaticFlushTimeout](/documentation/iobluetooth/bluetoothhciautomaticflushtimeout)
- [BluetoothHCICommandOpCode](/documentation/iobluetooth/bluetoothhcicommandopcode)
- [BluetoothHCICommandOpCodeCommand](/documentation/iobluetooth/bluetoothhcicommandopcodecommand)
- [BluetoothHCICommandOpCodeGroup](/documentation/iobluetooth/bluetoothhcicommandopcodegroup)
- [BluetoothHCIConnectionAcceptTimeout](/documentation/iobluetooth/bluetoothhciconnectionaccepttimeout)
- [BluetoothHCIConnectionMode](/documentation/iobluetooth/bluetoothhciconnectionmode)
- [BluetoothHCIConnectionModes](/documentation/iobluetooth/bluetoothhciconnectionmodes)

#### Constants

- [var kConnectionActiveMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionactivemode)
- [var kConnectionHoldMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionholdmode)
- [var kConnectionModeReservedForFutureUse: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionmodereservedforfutureuse)
- [var kConnectionParkMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionparkmode)
- [var kConnectionSniffMode: BluetoothHCIConnectionModes](/documentation/iobluetooth/kconnectionsniffmode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciconnectionmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciconnectionmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciconnectionmodes/rawvalue)
- [BluetoothHCIContentFormat](/documentation/iobluetooth/bluetoothhcicontentformat)
- [BluetoothHCICountryCode](/documentation/iobluetooth/bluetoothhcicountrycode)
- [BluetoothHCIDataID](/documentation/iobluetooth/bluetoothhcidataid)
- [BluetoothHCIDeleteStoredLinkKeyFlag](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflag)
- [BluetoothHCIDeleteStoredLinkKeyFlags](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags)

#### Constants

- [var kDeleteAllStoredLinkKeys: BluetoothHCIDeleteStoredLinkKeyFlags](/documentation/iobluetooth/kdeleteallstoredlinkkeys)
- [var kDeleteKeyForSpecifiedDeviceOnly: BluetoothHCIDeleteStoredLinkKeyFlags](/documentation/iobluetooth/kdeletekeyforspecifieddeviceonly)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcideletestoredlinkkeyflags/rawvalue)
- [BluetoothHCIEncryptionMode](/documentation/iobluetooth/bluetoothhciencryptionmode)
- [BluetoothHCIEncryptionModes](/documentation/iobluetooth/bluetoothhciencryptionmodes)

#### Constants

- [var kEncryptionDisabled: BluetoothHCIEncryptionModes](/documentation/iobluetooth/kencryptiondisabled)
- [var kEncryptionForBothPointToPointAndBroadcastPackets: BluetoothHCIEncryptionModes](/documentation/iobluetooth/kencryptionforbothpointtopointandbroadcastpackets)
- [var kEncryptionOnlyForPointToPointPackets: BluetoothHCIEncryptionModes](/documentation/iobluetooth/kencryptiononlyforpointtopointpackets)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciencryptionmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciencryptionmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciencryptionmodes/rawvalue)
- [BluetoothHCIErroneousDataReporting](/documentation/iobluetooth/bluetoothhcierroneousdatareporting)
- [BluetoothHCIEventCode](/documentation/iobluetooth/bluetoothhcieventcode)
- [BluetoothHCIEventID](/documentation/iobluetooth/bluetoothhcieventid)
- [BluetoothHCIEventMask](/documentation/iobluetooth/bluetoothhcieventmask)
- [BluetoothHCIEventStatus](/documentation/iobluetooth/bluetoothhcieventstatus)
- [BluetoothHCIExtendedInquiryResponseDataType](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatype)
- [BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes)

#### Constants

- [var kBluetoothHCIExtendedInquiryResponseDataType128BitServiceClassUUIDsCompleteList: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype128bitserviceclassuuidscompletelist)
- [var kBluetoothHCIExtendedInquiryResponseDataType128BitServiceClassUUIDsWithMoreAvailable: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype128bitserviceclassuuidswithmoreavailable)
- [var kBluetoothHCIExtendedInquiryResponseDataType16BitServiceClassUUIDsCompleteList: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype16bitserviceclassuuidscompletelist)
- [var kBluetoothHCIExtendedInquiryResponseDataType16BitServiceClassUUIDsWithMoreAvailable: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype16bitserviceclassuuidswithmoreavailable)
- [var kBluetoothHCIExtendedInquiryResponseDataType32BitServiceClassUUIDsCompleteList: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype32bitserviceclassuuidscompletelist)
- [var kBluetoothHCIExtendedInquiryResponseDataType32BitServiceClassUUIDsWithMoreAvailable: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype32bitserviceclassuuidswithmoreavailable)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeAppearance: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeappearance)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeCompleteLocalName: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypecompletelocalname)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeDeviceID: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypedeviceid)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeFlags: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeflags)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeManufacturerSpecificData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypemanufacturerspecificdata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypePublicTargetAddress: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypepublictargetaddress)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeRandomTargetAddress: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatyperandomtargetaddress)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSSPOOBClassOfDevice: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesspoobclassofdevice)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSSPOOBSimplePairingHashC: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesspoobsimplepairinghashc)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSSPOOBSimplePairingRandomizerR: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesspoobsimplepairingrandomizerr)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecurityManagerOOBFlags: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecuritymanageroobflags)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecurityManagerTKValue: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecuritymanagertkvalue)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicedata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceSolicitation128BitUUIDs: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicesolicitation128bituuids)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceSolicitation16BitUUIDs: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicesolicitation16bituuids)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeShortenedLocalName: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeshortenedlocalname)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSlaveConnectionIntervalRange: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeslaveconnectionintervalrange)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeTransmitPowerLevel: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypetransmitpowerlevel)
- [var kBluetoothHCIExtendedInquiryResponseDataType3DInformationData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatype3dinformationdata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeAdvertisingInterval: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeadvertisinginterval)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeLEBluetoothDeviceAddress: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypelebluetoothdeviceaddress)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeLERole: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypelerole)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecureConnectionsConfirmationValue: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecureconnectionsconfirmationvalue)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSecureConnectionsRandomValue: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesecureconnectionsrandomvalue)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceData128BitUUID: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicedata128bituuid)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceData32BitUUID: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicedata32bituuid)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeServiceSolicitation32BitUUIDs: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeservicesolicitation32bituuids)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSimplePairingHash: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesimplepairinghash)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeSimplePairingRandomizer: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypesimplepairingrandomizer)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeIndoorPositioning: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeindoorpositioning)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeTransportDiscoveryData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypetransportdiscoverydata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeURI: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeuri)
- [var kBluetoothHCIExtendedInquiryResponseDataTypeCsisRsiData: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypecsisrsidata)
- [var kBluetoothHCIExtendedInquiryResponseDataTypePeripheralConnectionIntervalRange: BluetoothHCIExtendedInquiryResponseDataTypes](/documentation/iobluetooth/kbluetoothhciextendedinquiryresponsedatatypeperipheralconnectionintervalrange)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciextendedinquiryresponsedatatypes/rawvalue)
- [BluetoothHCIFECRequired](/documentation/iobluetooth/bluetoothhcifecrequired)
- [BluetoothHCIFECRequiredValues](/documentation/iobluetooth/bluetoothhcifecrequiredvalues)

#### Constants

- [var kBluetoothHCIFECNotRequired: BluetoothHCIFECRequiredValues](/documentation/iobluetooth/kbluetoothhcifecnotrequired)
- [var kBluetoothHCIFECRequired: BluetoothHCIFECRequiredValues](/documentation/iobluetooth/kbluetoothhcifecrequired)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcifecrequiredvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcifecrequiredvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcifecrequiredvalues/rawvalue)
- [BluetoothHCIFailedContactCount](/documentation/iobluetooth/bluetoothhcifailedcontactcount)
- [BluetoothHCIFlowControlState](/documentation/iobluetooth/bluetoothhciflowcontrolstate)
- [BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates)

#### Constants

- [var kHCIACLDataPacketsOffHCISCODataPacketsOn: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khciacldatapacketsoffhciscodatapacketson)
- [var kHCIACLDataPacketsOnHCISCODataPacketsOff: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khciacldatapacketsonhciscodatapacketsoff)
- [var kHCIACLDataPacketsOnHCISCODataPacketsOn: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khciacldatapacketsonhciscodatapacketson)
- [var kHostControllerToHostFlowControlOff: BluetoothHCIGeneralFlowControlStates](/documentation/iobluetooth/khostcontrollertohostflowcontroloff)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcigeneralflowcontrolstates/rawvalue)
- [BluetoothHCIHoldModeActivity](/documentation/iobluetooth/bluetoothhciholdmodeactivity)
- [BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates)

#### Constants

- [var kMaintainCurrentPowerState: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/kmaintaincurrentpowerstate)
- [var kSuspendInquiryScan: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/ksuspendinquiryscan)
- [var kSuspendPageScan: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/ksuspendpagescan)
- [var kSuspendPeriodicInquiries: BluetoothHCIHoldModeActivityStates](/documentation/iobluetooth/ksuspendperiodicinquiries)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciholdmodeactivitystates/rawvalue)
- [BluetoothHCIInputBandwidth](/documentation/iobluetooth/bluetoothhciinputbandwidth)
- [BluetoothHCIInputCodedDataSize](/documentation/iobluetooth/bluetoothhciinputcodeddatasize)
- [BluetoothHCIInputCodingFormat](/documentation/iobluetooth/bluetoothhciinputcodingformat)
- [BluetoothHCIInputDataPath](/documentation/iobluetooth/bluetoothhciinputdatapath)
- [BluetoothHCIInputPCMDataFormat](/documentation/iobluetooth/bluetoothhciinputpcmdataformat)
- [BluetoothHCIInputPCMSamplePayloadMSBPosition](/documentation/iobluetooth/bluetoothhciinputpcmsamplepayloadmsbposition)
- [BluetoothHCIInputTransportUnitSize](/documentation/iobluetooth/bluetoothhciinputtransportunitsize)
- [BluetoothHCIInquiryAccessCodeCount](/documentation/iobluetooth/bluetoothhciinquiryaccesscodecount)
- [BluetoothHCIInquiryLength](/documentation/iobluetooth/bluetoothhciinquirylength)
- [BluetoothHCIInquiryMode](/documentation/iobluetooth/bluetoothhciinquirymode)
- [BluetoothHCIInquiryModes](/documentation/iobluetooth/bluetoothhciinquirymodes)

#### Constants

- [var kBluetoothHCIInquiryModeResultFormatStandard: BluetoothHCIInquiryModes](/documentation/iobluetooth/kbluetoothhciinquirymoderesultformatstandard)
- [var kBluetoothHCIInquiryModeResultFormatWithRSSI: BluetoothHCIInquiryModes](/documentation/iobluetooth/kbluetoothhciinquirymoderesultformatwithrssi)
- [var kBluetoothHCIInquiryModeResultFormatWithRSSIOrExtendedInquiryResultFormat: BluetoothHCIInquiryModes](/documentation/iobluetooth/kbluetoothhciinquirymoderesultformatwithrssiorextendedinquiryresultformat)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciinquirymodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciinquirymodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciinquirymodes/rawvalue)
- [BluetoothHCIInquiryScanType](/documentation/iobluetooth/bluetoothhciinquiryscantype)
- [BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/bluetoothhciinquiryscantypes)

#### Constants

- [var kBluetoothHCIInquiryScanTypeInterlaced: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypeinterlaced)
- [var kBluetoothHCIInquiryScanTypeReservedEnd: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypereservedend)
- [var kBluetoothHCIInquiryScanTypeReservedStart: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypereservedstart)
- [var kBluetoothHCIInquiryScanTypeStandard: BluetoothHCIInquiryScanTypes](/documentation/iobluetooth/kbluetoothhciinquiryscantypestandard)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciinquiryscantypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciinquiryscantypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciinquiryscantypes/rawvalue)
- [BluetoothHCILESupportedFeatures](/documentation/iobluetooth/bluetoothhcilesupportedfeatures)
- [BluetoothHCILEUsedFeatures](/documentation/iobluetooth/bluetoothhcileusedfeatures)
- [BluetoothHCILinkPolicySettings](/documentation/iobluetooth/bluetoothhcilinkpolicysettings)
- [BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues)

#### Constants

- [var kDisableAllLMModes: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kdisablealllmmodes)
- [var kEnableHoldMode: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenableholdmode)
- [var kEnableMasterSlaveSwitch: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenablemasterslaveswitch)
- [var kEnableParkMode: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenableparkmode)
- [var kEnableSniffMode: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenablesniffmode)
- [var kReservedForFutureUse: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kreservedforfutureuse)
- [var kEnableCentralPeripheralSwitch: BluetoothHCILinkPolicySettingsValues](/documentation/iobluetooth/kenablecentralperipheralswitch)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcilinkpolicysettingsvalues/rawvalue)
- [BluetoothHCILinkQuality](/documentation/iobluetooth/bluetoothhcilinkquality)
- [BluetoothHCILoopbackMode](/documentation/iobluetooth/bluetoothhciloopbackmode)
- [BluetoothHCIMaxLatency](/documentation/iobluetooth/bluetoothhcimaxlatency)
- [BluetoothHCIModeInterval](/documentation/iobluetooth/bluetoothhcimodeinterval)
- [BluetoothHCINumBroadcastRetransmissions](/documentation/iobluetooth/bluetoothhcinumbroadcastretransmissions)
- [BluetoothHCINumLinkKeysDeleted](/documentation/iobluetooth/bluetoothhcinumlinkkeysdeleted)
- [BluetoothHCINumLinkKeysToWrite](/documentation/iobluetooth/bluetoothhcinumlinkkeystowrite)
- [BluetoothHCIOperationID](/documentation/iobluetooth/bluetoothhcioperationid)
- [BluetoothHCIOutputBandwidth](/documentation/iobluetooth/bluetoothhcioutputbandwidth)
- [BluetoothHCIOutputCodedDataSize](/documentation/iobluetooth/bluetoothhcioutputcodeddatasize)
- [BluetoothHCIOutputCodingFormat](/documentation/iobluetooth/bluetoothhcioutputcodingformat)
- [BluetoothHCIOutputDataPath](/documentation/iobluetooth/bluetoothhcioutputdatapath)
- [BluetoothHCIOutputPCMDataFormat](/documentation/iobluetooth/bluetoothhcioutputpcmdataformat)
- [BluetoothHCIOutputPCMSamplePayloadMSBPosition](/documentation/iobluetooth/bluetoothhcioutputpcmsamplepayloadmsbposition)
- [BluetoothHCIOutputTransportUnitSize](/documentation/iobluetooth/bluetoothhcioutputtransportunitsize)
- [BluetoothHCIPageNumber](/documentation/iobluetooth/bluetoothhcipagenumber)
- [BluetoothHCIPageScanEnableState](/documentation/iobluetooth/bluetoothhcipagescanenablestate)
- [BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/bluetoothhcipagescanenablestates)

#### Constants

- [var kInquiryScanDisabledPageScanEnabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/kinquiryscandisabledpagescanenabled)
- [var kInquiryScanEnabledPageScanDisabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/kinquiryscanenabledpagescandisabled)
- [var kInquiryScanEnabledPageScanEnabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/kinquiryscanenabledpagescanenabled)
- [var kNoScansEnabled: BluetoothHCIPageScanEnableStates](/documentation/iobluetooth/knoscansenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescanenablestates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescanenablestates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescanenablestates/rawvalue)
- [BluetoothHCIPageScanMode](/documentation/iobluetooth/bluetoothhcipagescanmode)
- [BluetoothHCIPageScanModes](/documentation/iobluetooth/bluetoothhcipagescanmodes)

#### Constants

- [var kMandatoryPageScanMode: BluetoothHCIPageScanModes](/documentation/iobluetooth/kmandatorypagescanmode)
- [var kOptionalPageScanMode1: BluetoothHCIPageScanModes](/documentation/iobluetooth/koptionalpagescanmode1)
- [var kOptionalPageScanMode2: BluetoothHCIPageScanModes](/documentation/iobluetooth/koptionalpagescanmode2)
- [var kOptionalPageScanMode3: BluetoothHCIPageScanModes](/documentation/iobluetooth/koptionalpagescanmode3)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescanmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescanmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescanmodes/rawvalue)
- [BluetoothHCIPageScanPeriodMode](/documentation/iobluetooth/bluetoothhcipagescanperiodmode)
- [BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes)

#### Constants

- [var kP0Mode: BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/kp0mode)
- [var kP1Mode: BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/kp1mode)
- [var kP2Mode: BluetoothHCIPageScanPeriodModes](/documentation/iobluetooth/kp2mode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescanperiodmodes/rawvalue)
- [BluetoothHCIPageScanType](/documentation/iobluetooth/bluetoothhcipagescantype)
- [BluetoothHCIPageScanTypes](/documentation/iobluetooth/bluetoothhcipagescantypes)

#### Constants

- [var kBluetoothHCIPageScanTypeInterlaced: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypeinterlaced)
- [var kBluetoothHCIPageScanTypeReservedEnd: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypereservedend)
- [var kBluetoothHCIPageScanTypeReservedStart: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypereservedstart)
- [var kBluetoothHCIPageScanTypeStandard: BluetoothHCIPageScanTypes](/documentation/iobluetooth/kbluetoothhcipagescantypestandard)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcipagescantypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcipagescantypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcipagescantypes/rawvalue)
- [BluetoothHCIPageTimeout](/documentation/iobluetooth/bluetoothhcipagetimeout)
- [BluetoothHCIParamByteCount](/documentation/iobluetooth/bluetoothhciparambytecount)
- [BluetoothHCIParkModeBeaconInterval](/documentation/iobluetooth/bluetoothhciparkmodebeaconinterval)
- [BluetoothHCIQoSFlags](/documentation/iobluetooth/bluetoothhciqosflags)
- [BluetoothHCIRSSIValue](/documentation/iobluetooth/bluetoothhcirssivalue)
- [BluetoothHCIReadStoredLinkKeysFlag](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflag)
- [BluetoothHCIReadStoredLinkKeysFlags](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags)

#### Constants

- [var kReadAllStoredLinkKeys: BluetoothHCIReadStoredLinkKeysFlags](/documentation/iobluetooth/kreadallstoredlinkkeys)
- [var kReturnLinkKeyForSpecifiedDeviceOnly: BluetoothHCIReadStoredLinkKeysFlags](/documentation/iobluetooth/kreturnlinkkeyforspecifieddeviceonly)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcireadstoredlinkkeysflags/rawvalue)
- [BluetoothHCIReceiveBandwidth](/documentation/iobluetooth/bluetoothhcireceivebandwidth)
- [BluetoothHCIReceiveCodecFrameSize](/documentation/iobluetooth/bluetoothhcireceivecodecframesize)
- [BluetoothHCIReceiveCodingFormat](/documentation/iobluetooth/bluetoothhcireceivecodingformat)
- [BluetoothHCIRequestID](/documentation/iobluetooth/bluetoothhcirequestid)
- [BluetoothHCIResponseCount](/documentation/iobluetooth/bluetoothhciresponsecount)
- [BluetoothHCIRetransmissionEffort](/documentation/iobluetooth/bluetoothhciretransmissioneffort)
- [BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes)

#### Constants

- [var kHCIRetransmissionEffortTypeAtLeastOneAndOptimizeForPower: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypeatleastoneandoptimizeforpower)
- [var kHCIRetransmissionEffortTypeAtLeastOneAndOptimizeLinkQuality: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypeatleastoneandoptimizelinkquality)
- [var kHCIRetransmissionEffortTypeDontCare: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypedontcare)
- [var kHCIRetransmissionEffortTypeNone: BluetoothHCIRetransmissionEffortTypes](/documentation/iobluetooth/khciretransmissionefforttypenone)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciretransmissionefforttypes/rawvalue)
- [BluetoothHCIRole](/documentation/iobluetooth/bluetoothhcirole)
- [BluetoothHCIRoles](/documentation/iobluetooth/bluetoothhciroles)

#### Constants

- [var kBluetoothHCIMasterRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhcimasterrole)
- [var kBluetoothHCISlaveRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhcislaverole)
- [var kBluetoothHCICentralRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhcicentralrole)
- [var kBluetoothHCIPeripheralRole: BluetoothHCIRoles](/documentation/iobluetooth/kbluetoothhciperipheralrole)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciroles/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciroles/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciroles/rawvalue)
- [BluetoothHCISCODataByteCount](/documentation/iobluetooth/bluetoothhciscodatabytecount)
- [BluetoothHCISCOFlowControlStates](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates)

#### Constants

- [var kSCOFlowControlDisabled: BluetoothHCISCOFlowControlStates](/documentation/iobluetooth/kscoflowcontroldisabled)
- [var kSCOFlowControlEnabled: BluetoothHCISCOFlowControlStates](/documentation/iobluetooth/kscoflowcontrolenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciscoflowcontrolstates/rawvalue)
- [BluetoothHCISignalID](/documentation/iobluetooth/bluetoothhcisignalid)
- [BluetoothHCISimplePairingMode](/documentation/iobluetooth/bluetoothhcisimplepairingmode)
- [BluetoothHCISimplePairingModes](/documentation/iobluetooth/bluetoothhcisimplepairingmodes)

#### Constants

- [var kBluetoothHCISimplePairingModeEnabled: BluetoothHCISimplePairingModes](/documentation/iobluetooth/kbluetoothhcisimplepairingmodeenabled)
- [var kBluetoothHCISimplePairingModeNotSet: BluetoothHCISimplePairingModes](/documentation/iobluetooth/kbluetoothhcisimplepairingmodenotset)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcisimplepairingmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcisimplepairingmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcisimplepairingmodes/rawvalue)
- [BluetoothHCISniffAttemptCount](/documentation/iobluetooth/bluetoothhcisniffattemptcount)
- [BluetoothHCISniffTimeout](/documentation/iobluetooth/bluetoothhcisnifftimeout)
- [BluetoothHCIStatus](/documentation/iobluetooth/bluetoothhcistatus)
- [BluetoothHCISupportedIAC](/documentation/iobluetooth/bluetoothhcisupportediac)
- [BluetoothHCITimeoutValues](/documentation/iobluetooth/bluetoothhcitimeoutvalues)

#### Constants

- [var kDefaultPageTimeout: BluetoothHCITimeoutValues](/documentation/iobluetooth/kdefaultpagetimeout)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcitimeoutvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcitimeoutvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcitimeoutvalues/rawvalue)
- [BluetoothHCITransmitBandwidth](/documentation/iobluetooth/bluetoothhcitransmitbandwidth)
- [BluetoothHCITransmitCodecFrameSize](/documentation/iobluetooth/bluetoothhcitransmitcodecframesize)
- [BluetoothHCITransmitCodingFormat](/documentation/iobluetooth/bluetoothhcitransmitcodingformat)
- [BluetoothHCITransmitPowerLevel](/documentation/iobluetooth/bluetoothhcitransmitpowerlevel)
- [BluetoothHCITransmitPowerLevelType](/documentation/iobluetooth/bluetoothhcitransmitpowerleveltype)
- [BluetoothHCITransmitReadPowerLevelTypes](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes)

#### Constants

- [var kReadCurrentTransmitPowerLevel: BluetoothHCITransmitReadPowerLevelTypes](/documentation/iobluetooth/kreadcurrenttransmitpowerlevel)
- [var kReadMaximumTransmitPowerLevel: BluetoothHCITransmitReadPowerLevelTypes](/documentation/iobluetooth/kreadmaximumtransmitpowerlevel)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhcitransmitreadpowerleveltypes/rawvalue)
- [BluetoothHCITransportCommandID](/documentation/iobluetooth/bluetoothhcitransportcommandid)
- [BluetoothHCITransportID](/documentation/iobluetooth/bluetoothhcitransportid)
- [BluetoothHCIVendorCommandSelector](/documentation/iobluetooth/bluetoothhcivendorcommandselector)
- [BluetoothHCIVersions](/documentation/iobluetooth/bluetoothhciversions)

#### Constants

- [var kBluetoothHCIVersionCoreSpecification1_0b: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification1_0b)
- [var kBluetoothHCIVersionCoreSpecification1_1: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification1_1)
- [var kBluetoothHCIVersionCoreSpecification1_2: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification1_2)
- [var kBluetoothHCIVersionCoreSpecification2_0EDR: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification2_0edr)
- [var kBluetoothHCIVersionCoreSpecification2_1EDR: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification2_1edr)
- [var kBluetoothHCIVersionCoreSpecification3_0HS: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification3_0hs)
- [var kBluetoothHCIVersionCoreSpecification4_0: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification4_0)
- [var kBluetoothHCIVersionCoreSpecification4_1: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification4_1)
- [var kBluetoothHCIVersionCoreSpecification4_2: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification4_2)
- [var kBluetoothHCIVersionCoreSpecification5_0: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_0)
- [var kBluetoothHCIVersionCoreSpecification5_1: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_1)
- [var kBluetoothHCIVersionCoreSpecification5_2: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_2)
- [var kBluetoothHCIVersionCoreSpecification5_3: BluetoothHCIVersions](/documentation/iobluetooth/kbluetoothhciversioncorespecification5_3)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothhciversions/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothhciversions/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothhciversions/rawvalue)
- [BluetoothHCIVoiceSetting](/documentation/iobluetooth/bluetoothhcivoicesetting)
- [BluetoothIOCapabilities](/documentation/iobluetooth/bluetoothiocapabilities)

#### Constants

- [var kBluetoothCapabilityTypeDisplayOnly: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypedisplayonly)
- [var kBluetoothCapabilityTypeDisplayYesNo: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypedisplayyesno)
- [var kBluetoothCapabilityTypeKeyboardOnly: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypekeyboardonly)
- [var kBluetoothCapabilityTypeNoInputNoOutput: BluetoothIOCapabilities](/documentation/iobluetooth/kbluetoothcapabilitytypenoinputnooutput)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothiocapabilities/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothiocapabilities/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothiocapabilities/rawvalue)
- [BluetoothIOCapability](/documentation/iobluetooth/bluetoothiocapability)
- [BluetoothKeyFlag](/documentation/iobluetooth/bluetoothkeyflag)
- [BluetoothKeyType](/documentation/iobluetooth/bluetoothkeytype)
- [BluetoothKeypressNotificationType](/documentation/iobluetooth/bluetoothkeypressnotificationtype)
- [BluetoothKeypressNotificationTypes](/documentation/iobluetooth/bluetoothkeypressnotificationtypes)

#### Constants

- [var kBluetoothKeypressNotificationTypePasskeyCleared: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeycleared)
- [var kBluetoothKeypressNotificationTypePasskeyDigitEntered: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeydigitentered)
- [var kBluetoothKeypressNotificationTypePasskeyDigitErased: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeydigiterased)
- [var kBluetoothKeypressNotificationTypePasskeyEntryCompleted: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeyentrycompleted)
- [var kBluetoothKeypressNotificationTypePasskeyEntryStarted: BluetoothKeypressNotificationTypes](/documentation/iobluetooth/kbluetoothkeypressnotificationtypepasskeyentrystarted)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothkeypressnotificationtypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothkeypressnotificationtypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothkeypressnotificationtypes/rawvalue)
- [BluetoothL2CAPByteCount](/documentation/iobluetooth/bluetoothl2capbytecount)
- [BluetoothL2CAPChannelID](/documentation/iobluetooth/bluetoothl2capchannelid)
- [BluetoothL2CAPCommandByteCount](/documentation/iobluetooth/bluetoothl2capcommandbytecount)
- [BluetoothL2CAPCommandID](/documentation/iobluetooth/bluetoothl2capcommandid)
- [BluetoothL2CAPFlushTimeout](/documentation/iobluetooth/bluetoothl2capflushtimeout)
- [BluetoothL2CAPGroupID](/documentation/iobluetooth/bluetoothl2capgroupid)
- [BluetoothL2CAPLinkTimeout](/documentation/iobluetooth/bluetoothl2caplinktimeout)
- [BluetoothL2CAPMTU](/documentation/iobluetooth/bluetoothl2capmtu)
- [BluetoothL2CAPPSM](/documentation/iobluetooth/bluetoothl2cappsm)
- [BluetoothLAP](/documentation/iobluetooth/bluetoothlap)
- [BluetoothLEFeatureBits](/documentation/iobluetooth/bluetoothlefeaturebits)

#### Constants

- [var kBluetoothLEFeatureConnectionParamsRequestProcedure: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureconnectionparamsrequestprocedure)
- [var kBluetoothLEFeatureExtendedRejectIndication: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureextendedrejectindication)
- [var kBluetoothLEFeatureExtendedScannerFilterPolicies: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureextendedscannerfilterpolicies)
- [var kBluetoothLEFeatureLEDataPacketLengthExtension: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureledatapacketlengthextension)
- [var kBluetoothLEFeatureLEEncryption: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureleencryption)
- [var kBluetoothLEFeatureLEPing: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureleping)
- [var kBluetoothLEFeatureLLPrivacy: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeaturellprivacy)
- [var kBluetoothLEFeatureSlaveInitiatedFeaturesExchange: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureslaveinitiatedfeaturesexchange)
- [var kBluetoothLEFeaturePeripheralInitiatedFeaturesExchange: BluetoothLEFeatureBits](/documentation/iobluetooth/kbluetoothlefeatureperipheralinitiatedfeaturesexchange)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlefeaturebits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlefeaturebits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlefeaturebits/rawvalue)
- [BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat)

#### Constants

- [var kBluetoothLESecurityManagerEncryptionKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanagerencryptionkey)
- [var kBluetoothLESecurityManagerIDKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanageridkey)
- [var kBluetoothLESecurityManagerLinkKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanagerlinkkey)
- [var kBluetoothLESecurityManagerSignKey: BluetoothLESecurityManagerKeyDistributionFormat](/documentation/iobluetooth/kbluetoothlesecuritymanagersignkey)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlesecuritymanagerkeydistributionformat/rawvalue)
- [BluetoothLMPHandle](/documentation/iobluetooth/bluetoothlmphandle)
- [BluetoothLMPSubversion](/documentation/iobluetooth/bluetoothlmpsubversion)
- [BluetoothLMPVersion](/documentation/iobluetooth/bluetoothlmpversion)
- [BluetoothLMPVersions](/documentation/iobluetooth/bluetoothlmpversions)

#### Constants

- [var kBluetoothLMPVersionCoreSpecification1_0b: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification1_0b)
- [var kBluetoothLMPVersionCoreSpecification1_1: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification1_1)
- [var kBluetoothLMPVersionCoreSpecification1_2: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification1_2)
- [var kBluetoothLMPVersionCoreSpecification2_0EDR: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification2_0edr)
- [var kBluetoothLMPVersionCoreSpecification2_1EDR: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification2_1edr)
- [var kBluetoothLMPVersionCoreSpecification3_0HS: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification3_0hs)
- [var kBluetoothLMPVersionCoreSpecification4_0: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification4_0)
- [var kBluetoothLMPVersionCoreSpecification4_1: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification4_1)
- [var kBluetoothLMPVersionCoreSpecification4_2: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification4_2)
- [var kBluetoothLMPVersionCoreSpecification5_0: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification5_0)
- [var kBluetoothLMPVersionCoreSpecification5_1: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification5_1)
- [var kBluetoothLMPVersionCoreSpecification5_2: BluetoothLMPVersions](/documentation/iobluetooth/kbluetoothlmpversioncorespecification5_2)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlmpversions/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlmpversions/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlmpversions/rawvalue)
- [BluetoothLinkType](/documentation/iobluetooth/bluetoothlinktype)
- [BluetoothLinkTypes](/documentation/iobluetooth/bluetoothlinktypes)

#### Constants

- [var kBluetoothACLConnection: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothaclconnection)
- [var kBluetoothESCOConnection: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothescoconnection)
- [var kBluetoothLinkTypeNone: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothlinktypenone)
- [var kBluetoothSCOConnection: BluetoothLinkTypes](/documentation/iobluetooth/kbluetoothscoconnection)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothlinktypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothlinktypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothlinktypes/rawvalue)
- [BluetoothManufacturerName](/documentation/iobluetooth/bluetoothmanufacturername)
- [BluetoothMaxSlots](/documentation/iobluetooth/bluetoothmaxslots)
- [BluetoothNumericValue](/documentation/iobluetooth/bluetoothnumericvalue)
- [BluetoothOOBDataPresence](/documentation/iobluetooth/bluetoothoobdatapresence)
- [BluetoothOOBDataPresenceValues](/documentation/iobluetooth/bluetoothoobdatapresencevalues)

#### Constants

- [var kBluetoothOOBAuthenticationDataFromRemoteDevicePresent: BluetoothOOBDataPresenceValues](/documentation/iobluetooth/kbluetoothoobauthenticationdatafromremotedevicepresent)
- [var kBluetoothOOBAuthenticationDataNotPresent: BluetoothOOBDataPresenceValues](/documentation/iobluetooth/kbluetoothoobauthenticationdatanotpresent)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothoobdatapresencevalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothoobdatapresencevalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothoobdatapresencevalues/rawvalue)
- [BluetoothPINType](/documentation/iobluetooth/bluetoothpintype)
- [BluetoothPacketType](/documentation/iobluetooth/bluetoothpackettype)
- [BluetoothPageScanMode](/documentation/iobluetooth/bluetoothpagescanmode)
- [BluetoothPageScanPeriodMode](/documentation/iobluetooth/bluetoothpagescanperiodmode)
- [BluetoothPageScanRepetitionMode](/documentation/iobluetooth/bluetoothpagescanrepetitionmode)
- [BluetoothPasskey](/documentation/iobluetooth/bluetoothpasskey)
- [BluetoothRFCOMMChannelID](/documentation/iobluetooth/bluetoothrfcommchannelid)
- [BluetoothRFCOMMMTU](/documentation/iobluetooth/bluetoothrfcommmtu)
- [BluetoothReasonCode](/documentation/iobluetooth/bluetoothreasoncode)
- [BluetoothRole](/documentation/iobluetooth/bluetoothrole)
- [BluetoothSDPDataElementSizeDescriptor](/documentation/iobluetooth/bluetoothsdpdataelementsizedescriptor)
- [BluetoothSDPDataElementTypeDescriptor](/documentation/iobluetooth/bluetoothsdpdataelementtypedescriptor)
- [BluetoothSDPErrorCode](/documentation/iobluetooth/bluetoothsdperrorcode)
- [BluetoothSDPPDUID](/documentation/iobluetooth/bluetoothsdppduid)
- [BluetoothSDPServiceAttributeID](/documentation/iobluetooth/bluetoothsdpserviceattributeid)
- [BluetoothSDPServiceRecordHandle](/documentation/iobluetooth/bluetoothsdpservicerecordhandle)
- [BluetoothSDPTransactionID](/documentation/iobluetooth/bluetoothsdptransactionid)
- [BluetoothSDPUUID16](/documentation/iobluetooth/bluetoothsdpuuid16)
- [BluetoothSDPUUID32](/documentation/iobluetooth/bluetoothsdpuuid32)
- [BluetoothServiceClassMajor](/documentation/iobluetooth/bluetoothserviceclassmajor)
- [BluetoothSimplePairingDebugMode](/documentation/iobluetooth/bluetoothsimplepairingdebugmode)
- [BluetoothSimplePairingDebugModes](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes)

#### Constants

- [var kBluetoothHCISimplePairingDebugModeDisabled: BluetoothSimplePairingDebugModes](/documentation/iobluetooth/kbluetoothhcisimplepairingdebugmodedisabled)
- [var kBluetoothHCISimplePairingDebugModeEnabled: BluetoothSimplePairingDebugModes](/documentation/iobluetooth/kbluetoothhcisimplepairingdebugmodeenabled)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothsimplepairingdebugmodes/rawvalue)
- [BluetoothTransportInfoPtr](/documentation/iobluetooth/bluetoothtransportinfoptr)
- [BluetoothTransportTypes](/documentation/iobluetooth/bluetoothtransporttypes)

#### Constants

- [var kBluetoothTransportTypePCCard: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypepccard)
- [var kBluetoothTransportTypePCICard: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypepcicard)
- [var kBluetoothTransportTypeUART: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypeuart)
- [var kBluetoothTransportTypeUSB: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypeusb)
- [var kBluetoothTransportTypePCIe: BluetoothTransportTypes](/documentation/iobluetooth/kbluetoothtransporttypepcie)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/bluetoothtransporttypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/bluetoothtransporttypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/bluetoothtransporttypes/rawvalue)
- [FTSFileType](/documentation/iobluetooth/ftsfiletype)

#### Constants

- [var kFTSFileTypeFile: FTSFileType](/documentation/iobluetooth/kftsfiletypefile)
- [var kFTSFileTypeFolder: FTSFileType](/documentation/iobluetooth/kftsfiletypefolder)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/ftsfiletype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/ftsfiletype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/ftsfiletype/rawvalue)
- [IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits)

#### Constants

- [var kSearchOptionsAlwaysStartInquiry: IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/ksearchoptionsalwaysstartinquiry)
- [var kSearchOptionsDiscardCachedResults: IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/ksearchoptionsdiscardcachedresults)
- [var kSearchOptionsNone: IOBluetoothDeviceSearchOptionsBits](/documentation/iobluetooth/ksearchoptionsnone)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothdevicesearchoptionsbits/rawvalue)
- [IOBluetoothDeviceSearchTypes](/documentation/iobluetooth/iobluetoothdevicesearchtypes)
- [IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits)

#### Constants

- [var kIOBluetoothDeviceSearchClassic: IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/kiobluetoothdevicesearchclassic)
- [var kIOBluetoothDeviceSearchLE: IOBluetoothDeviceSearchTypesBits](/documentation/iobluetooth/kiobluetoothdevicesearchle)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/iobluetoothdevicesearchtypesbits/rawvalue)
- [IOBluetoothL2CAPChannelIncomingDataListener](/documentation/iobluetooth/iobluetoothl2capchannelincomingdatalistener)
- [IOBluetoothL2CAPChannelIncomingEventListener](/documentation/iobluetooth/iobluetoothl2capchannelincomingeventlistener)
- [IOBluetoothOBEXSessionOpenConnectionCallback](/documentation/iobluetooth/iobluetoothobexsessionopenconnectioncallback)
- [IOBluetoothObjectID](/documentation/iobluetooth/iobluetoothobjectid)
- [OBEXConnectFlagValues](/documentation/iobluetooth/obexconnectflagvalues)

#### Constants

- [var kOBEXConnectFlag1Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag1reserved)
- [var kOBEXConnectFlag2Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag2reserved)
- [var kOBEXConnectFlag3Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag3reserved)
- [var kOBEXConnectFlag4Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag4reserved)
- [var kOBEXConnectFlag5Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag5reserved)
- [var kOBEXConnectFlag6Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag6reserved)
- [var kOBEXConnectFlag7Reserved: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflag7reserved)
- [var kOBEXConnectFlagNone: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflagnone)
- [var kOBEXConnectFlagSupportMultipleItLMPConnections: OBEXConnectFlagValues](/documentation/iobluetooth/kobexconnectflagsupportmultipleitlmpconnections)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexconnectflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexconnectflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexconnectflagvalues/rawvalue)
- [OBEXConstants](/documentation/iobluetooth/obexconstants)
- [OBEXErrorCodes](/documentation/iobluetooth/obexerrorcodes)

#### Constants

- [var kOBEXBadArgumentError: OBEXErrorCodes](/documentation/iobluetooth/kobexbadargumenterror)
- [var kOBEXBadRequestError: OBEXErrorCodes](/documentation/iobluetooth/kobexbadrequesterror)
- [var kOBEXCancelledError: OBEXErrorCodes](/documentation/iobluetooth/kobexcancellederror)
- [var kOBEXConflictError: OBEXErrorCodes](/documentation/iobluetooth/kobexconflicterror)
- [var kOBEXErrorRangeMax: OBEXErrorCodes](/documentation/iobluetooth/kobexerrorrangemax)
- [var kOBEXErrorRangeMin: OBEXErrorCodes](/documentation/iobluetooth/kobexerrorrangemin)
- [var kOBEXForbiddenError: OBEXErrorCodes](/documentation/iobluetooth/kobexforbiddenerror)
- [var kOBEXGeneralError: OBEXErrorCodes](/documentation/iobluetooth/kobexgeneralerror)
- [var kOBEXInternalError: OBEXErrorCodes](/documentation/iobluetooth/kobexinternalerror)
- [var kOBEXMethodNotAllowedError: OBEXErrorCodes](/documentation/iobluetooth/kobexmethodnotallowederror)
- [var kOBEXNoResourcesError: OBEXErrorCodes](/documentation/iobluetooth/kobexnoresourceserror)
- [var kOBEXNotAcceptableError: OBEXErrorCodes](/documentation/iobluetooth/kobexnotacceptableerror)
- [var kOBEXNotFoundError: OBEXErrorCodes](/documentation/iobluetooth/kobexnotfounderror)
- [var kOBEXNotImplementedError: OBEXErrorCodes](/documentation/iobluetooth/kobexnotimplementederror)
- [var kOBEXPreconditionFailedError: OBEXErrorCodes](/documentation/iobluetooth/kobexpreconditionfailederror)
- [var kOBEXSessionAlreadyConnectedError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionalreadyconnectederror)
- [var kOBEXSessionBadRequestError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionbadrequesterror)
- [var kOBEXSessionBadResponseError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionbadresponseerror)
- [var kOBEXSessionBusyError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionbusyerror)
- [var kOBEXSessionNoTransportError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionnotransporterror)
- [var kOBEXSessionNotConnectedError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessionnotconnectederror)
- [var kOBEXSessionTimeoutError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessiontimeouterror)
- [var kOBEXSessionTransportDiedError: OBEXErrorCodes](/documentation/iobluetooth/kobexsessiontransportdiederror)
- [var kOBEXSuccess: OBEXErrorCodes](/documentation/iobluetooth/kobexsuccess)
- [var kOBEXTimeoutError: OBEXErrorCodes](/documentation/iobluetooth/kobextimeouterror)
- [var kOBEXUnauthorizedError: OBEXErrorCodes](/documentation/iobluetooth/kobexunauthorizederror)
- [var kOBEXUnsupportedError: OBEXErrorCodes](/documentation/iobluetooth/kobexunsupportederror)

#### Initializers

- [init(Int32)](/documentation/iobluetooth/obexerrorcodes/init(_:))
- [init(rawValue: Int32)](/documentation/iobluetooth/obexerrorcodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: Int32](/documentation/iobluetooth/obexerrorcodes/rawvalue)
- [OBEXFlags](/documentation/iobluetooth/obexflags)
- [OBEXHeaderIdentifier](/documentation/iobluetooth/obexheaderidentifier)
- [OBEXHeaderIdentifiers](/documentation/iobluetooth/obexheaderidentifiers)

#### Constants

- [var kOBEXHeaderIDAppParameters: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidappparameters)
- [var kOBEXHeaderIDAuthorizationChallenge: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidauthorizationchallenge)
- [var kOBEXHeaderIDAuthorizationResponse: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidauthorizationresponse)
- [var kOBEXHeaderIDBody: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidbody)
- [var kOBEXHeaderIDConnectionID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidconnectionid)
- [var kOBEXHeaderIDCount: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidcount)
- [var kOBEXHeaderIDDescription: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiddescription)
- [var kOBEXHeaderIDEndOfBody: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidendofbody)
- [var kOBEXHeaderIDHTTP: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidhttp)
- [var kOBEXHeaderIDLength: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidlength)
- [var kOBEXHeaderIDName: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidname)
- [var kOBEXHeaderIDOBEX13CreatorID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13creatorid)
- [var kOBEXHeaderIDOBEX13ObjectClass: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13objectclass)
- [var kOBEXHeaderIDOBEX13SessionParameters: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13sessionparameters)
- [var kOBEXHeaderIDOBEX13SessionSequenceNumber: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13sessionsequencenumber)
- [var kOBEXHeaderIDOBEX13WANUUID: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobex13wanuuid)
- [var kOBEXHeaderIDObjectClass: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidobjectclass)
- [var kOBEXHeaderIDReservedRangeEnd: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidreservedrangeend)
- [var kOBEXHeaderIDReservedRangeStart: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidreservedrangestart)
- [var kOBEXHeaderIDTarget: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtarget)
- [var kOBEXHeaderIDTime4Byte: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtime4byte)
- [var kOBEXHeaderIDTimeISO: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtimeiso)
- [var kOBEXHeaderIDType: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidtype)
- [var kOBEXHeaderIDUserDefinedRangeEnd: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiduserdefinedrangeend)
- [var kOBEXHeaderIDUserDefinedRangeStart: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderiduserdefinedrangestart)
- [var kOBEXHeaderIDWho: OBEXHeaderIdentifiers](/documentation/iobluetooth/kobexheaderidwho)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexheaderidentifiers/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexheaderidentifiers/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexheaderidentifiers/rawvalue)
- [OBEXMaxPacketLength](/documentation/iobluetooth/obexmaxpacketlength)
- [OBEXNonceFlagValues](/documentation/iobluetooth/obexnonceflagvalues)

#### Constants

- [var kOBEXNonceFlag2Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag2reserved)
- [var kOBEXNonceFlag3Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag3reserved)
- [var kOBEXNonceFlag4Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag4reserved)
- [var kOBEXNonceFlag5Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag5reserved)
- [var kOBEXNonceFlag6Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag6reserved)
- [var kOBEXNonceFlag7Reserved: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflag7reserved)
- [var kOBEXNonceFlagAccessModeReadOnly: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagaccessmodereadonly)
- [var kOBEXNonceFlagNone: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagnone)
- [var kOBEXNonceFlagSendUserIDInResponse: OBEXNonceFlagValues](/documentation/iobluetooth/kobexnonceflagsenduseridinresponse)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexnonceflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexnonceflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexnonceflagvalues/rawvalue)
- [OBEXOpCode](/documentation/iobluetooth/obexopcode)
- [OBEXOpCodeCommandValues](/documentation/iobluetooth/obexopcodecommandvalues)

#### Constants

- [var kOBEXOpCodeAbort: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeabort)
- [var kOBEXOpCodeConnect: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeconnect)
- [var kOBEXOpCodeDisconnect: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodedisconnect)
- [var kOBEXOpCodeGet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeget)
- [var kOBEXOpCodeGetWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodegetwithhighbitset)
- [var kOBEXOpCodePut: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeput)
- [var kOBEXOpCodePutWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeputwithhighbitset)
- [var kOBEXOpCodeReserved: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereserved)
- [var kOBEXOpCodeReservedRangeEnd: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedrangeend)
- [var kOBEXOpCodeReservedRangeStart: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedrangestart)
- [var kOBEXOpCodeReservedWithHighBitSet: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodereservedwithhighbitset)
- [var kOBEXOpCodeSetPath: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodesetpath)
- [var kOBEXOpCodeUserDefinedEnd: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeuserdefinedend)
- [var kOBEXOpCodeUserDefinedStart: OBEXOpCodeCommandValues](/documentation/iobluetooth/kobexopcodeuserdefinedstart)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcodecommandvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcodecommandvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcodecommandvalues/rawvalue)
- [OBEXOpCodeResponseValues](/documentation/iobluetooth/obexopcoderesponsevalues)

#### Constants

- [var kOBEXResponseCodeAccepted: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeaccepted)
- [var kOBEXResponseCodeAcceptedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeacceptedwithfinalbit)
- [var kOBEXResponseCodeBadGateway: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadgateway)
- [var kOBEXResponseCodeBadGatewayWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadgatewaywithfinalbit)
- [var kOBEXResponseCodeBadRequest: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadrequest)
- [var kOBEXResponseCodeBadRequestWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodebadrequestwithfinalbit)
- [var kOBEXResponseCodeConflict: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeconflict)
- [var kOBEXResponseCodeConflictWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeconflictwithfinalbit)
- [var kOBEXResponseCodeContinue: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecontinue)
- [var kOBEXResponseCodeContinueWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecontinuewithfinalbit)
- [var kOBEXResponseCodeCreated: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecreated)
- [var kOBEXResponseCodeCreatedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodecreatedwithfinalbit)
- [var kOBEXResponseCodeDatabaseFull: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabasefull)
- [var kOBEXResponseCodeDatabaseFullWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabasefullwithfinalbit)
- [var kOBEXResponseCodeDatabaseLocked: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabaselocked)
- [var kOBEXResponseCodeDatabaseLockedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodedatabaselockedwithfinalbit)
- [var kOBEXResponseCodeForbidden: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeforbidden)
- [var kOBEXResponseCodeForbiddenWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeforbiddenwithfinalbit)
- [var kOBEXResponseCodeGatewayTimeout: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegatewaytimeout)
- [var kOBEXResponseCodeGatewayTimeoutWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegatewaytimeoutwithfinalbit)
- [var kOBEXResponseCodeGone: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegone)
- [var kOBEXResponseCodeGoneWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodegonewithfinalbit)
- [var kOBEXResponseCodeHTTPVersionNotSupported: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodehttpversionnotsupported)
- [var kOBEXResponseCodeHTTPVersionNotSupportedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodehttpversionnotsupportedwithfinalbit)
- [var kOBEXResponseCodeInternalServerError: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeinternalservererror)
- [var kOBEXResponseCodeInternalServerErrorWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeinternalservererrorwithfinalbit)
- [var kOBEXResponseCodeLengthRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodelengthrequired)
- [var kOBEXResponseCodeLengthRequiredFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodelengthrequiredfinalbit)
- [var kOBEXResponseCodeMethodNotAllowed: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemethodnotallowed)
- [var kOBEXResponseCodeMethodNotAllowedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemethodnotallowedwithfinalbit)
- [var kOBEXResponseCodeMovedPermanently: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedpermanently)
- [var kOBEXResponseCodeMovedPermanentlyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedpermanentlywithfinalbit)
- [var kOBEXResponseCodeMovedTemporarily: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedtemporarily)
- [var kOBEXResponseCodeMovedTemporarilyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemovedtemporarilywithfinalbit)
- [var kOBEXResponseCodeMultipleChoices: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemultiplechoices)
- [var kOBEXResponseCodeMultipleChoicesWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodemultiplechoiceswithfinalbit)
- [var kOBEXResponseCodeNoContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenocontent)
- [var kOBEXResponseCodeNoContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenocontentwithfinalbit)
- [var kOBEXResponseCodeNonAuthoritativeInfo: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenonauthoritativeinfo)
- [var kOBEXResponseCodeNonAuthoritativeInfoWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenonauthoritativeinfowithfinalbit)
- [var kOBEXResponseCodeNotAcceptable: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotacceptable)
- [var kOBEXResponseCodeNotAcceptableWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotacceptablewithfinalbit)
- [var kOBEXResponseCodeNotFound: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotfound)
- [var kOBEXResponseCodeNotFoundWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotfoundwithfinalbit)
- [var kOBEXResponseCodeNotImplemented: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotimplemented)
- [var kOBEXResponseCodeNotImplementedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotimplementedwithfinalbit)
- [var kOBEXResponseCodeNotModified: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotmodified)
- [var kOBEXResponseCodeNotModifiedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodenotmodifiedwithfinalbit)
- [var kOBEXResponseCodePartialContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepartialcontent)
- [var kOBEXResponseCodePartialContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepartialcontentwithfinalbit)
- [var kOBEXResponseCodePaymentRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepaymentrequired)
- [var kOBEXResponseCodePaymentRequiredWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepaymentrequiredwithfinalbit)
- [var kOBEXResponseCodePreconditionFailed: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepreconditionfailed)
- [var kOBEXResponseCodePreconditionFailedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodepreconditionfailedwithfinalbit)
- [var kOBEXResponseCodeProxyAuthenticationRequired: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeproxyauthenticationrequired)
- [var kOBEXResponseCodeProxyAuthenticationRequiredWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeproxyauthenticationrequiredwithfinalbit)
- [var kOBEXResponseCodeRequestTimeOut: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesttimeout)
- [var kOBEXResponseCodeRequestTimeOutWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesttimeoutwithfinalbit)
- [var kOBEXResponseCodeRequestURLTooLarge: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesturltoolarge)
- [var kOBEXResponseCodeRequestURLTooLargeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequesturltoolargewithfinalbit)
- [var kOBEXResponseCodeRequestedEntityTooLarge: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequestedentitytoolarge)
- [var kOBEXResponseCodeRequestedEntityTooLargeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderequestedentitytoolargewithfinalbit)
- [var kOBEXResponseCodeReservedRangeEnd: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodereservedrangeend)
- [var kOBEXResponseCodeReservedRangeStart: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodereservedrangestart)
- [var kOBEXResponseCodeResetContent: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderesetcontent)
- [var kOBEXResponseCodeResetContentWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecoderesetcontentwithfinalbit)
- [var kOBEXResponseCodeSeeOther: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeseeother)
- [var kOBEXResponseCodeSeeOtherWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeseeotherwithfinalbit)
- [var kOBEXResponseCodeServiceUnavailable: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeserviceunavailable)
- [var kOBEXResponseCodeServiceUnavailableWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeserviceunavailablewithfinalbit)
- [var kOBEXResponseCodeSuccess: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodesuccess)
- [var kOBEXResponseCodeSuccessWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodesuccesswithfinalbit)
- [var kOBEXResponseCodeUnauthorized: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunauthorized)
- [var kOBEXResponseCodeUnauthorizedWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunauthorizedwithfinalbit)
- [var kOBEXResponseCodeUnsupportedMediaType: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunsupportedmediatype)
- [var kOBEXResponseCodeUnsupportedMediaTypeWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeunsupportedmediatypewithfinalbit)
- [var kOBEXResponseCodeUseProxy: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeuseproxy)
- [var kOBEXResponseCodeUseProxyWithFinalBit: OBEXOpCodeResponseValues](/documentation/iobluetooth/kobexresponsecodeuseproxywithfinalbit)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcoderesponsevalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcoderesponsevalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcoderesponsevalues/rawvalue)
- [OBEXOpCodeSessionValues](/documentation/iobluetooth/obexopcodesessionvalues)

#### Constants

- [var kOBEXOpCodeCloseSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodeclosesession)
- [var kOBEXOpCodeCreateSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodecreatesession)
- [var kOBEXOpCodeResumeSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcoderesumesession)
- [var kOBEXOpCodeSetTimeout: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodesettimeout)
- [var kOBEXOpCodeSuspendSession: OBEXOpCodeSessionValues](/documentation/iobluetooth/kobexopcodesuspendsession)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexopcodesessionvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexopcodesessionvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexopcodesessionvalues/rawvalue)
- [OBEXPutFlagValues](/documentation/iobluetooth/obexputflagvalues)

#### Constants

- [var kOBEXPutFlag2Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag2reserved)
- [var kOBEXPutFlag3Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag3reserved)
- [var kOBEXPutFlag4Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag4reserved)
- [var kOBEXPutFlag5Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag5reserved)
- [var kOBEXPutFlag6Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag6reserved)
- [var kOBEXPutFlag7Reserved: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflag7reserved)
- [var kOBEXPutFlagDontCreateDirectory: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflagdontcreatedirectory)
- [var kOBEXPutFlagGoToParentDirFirst: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflaggotoparentdirfirst)
- [var kOBEXPutFlagNone: OBEXPutFlagValues](/documentation/iobluetooth/kobexputflagnone)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexputflagvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexputflagvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexputflagvalues/rawvalue)
- [OBEXRealmValues](/documentation/iobluetooth/obexrealmvalues)

#### Constants

- [var kOBEXRealmASCII: OBEXRealmValues](/documentation/iobluetooth/kobexrealmascii)
- [var kOBEXRealmISO88591: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88591)
- [var kOBEXRealmISO88592: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88592)
- [var kOBEXRealmISO88593: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88593)
- [var kOBEXRealmISO88594: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88594)
- [var kOBEXRealmISO88595: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88595)
- [var kOBEXRealmISO88596: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88596)
- [var kOBEXRealmISO88597: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88597)
- [var kOBEXRealmISO88598: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88598)
- [var kOBEXRealmISO88599: OBEXRealmValues](/documentation/iobluetooth/kobexrealmiso88599)
- [var kOBEXRealmUNICODE: OBEXRealmValues](/documentation/iobluetooth/kobexrealmunicode)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexrealmvalues/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexrealmvalues/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexrealmvalues/rawvalue)
- [OBEXSessionEventCallback](/documentation/iobluetooth/obexsessioneventcallback)
- [OBEXSessionEventType](/documentation/iobluetooth/obexsessioneventtype)
- [OBEXSessionEventTypes](/documentation/iobluetooth/obexsessioneventtypes)

#### Constants

- [var kOBEXSessionEventTypeAbortCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeabortcommandreceived)
- [var kOBEXSessionEventTypeAbortCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeabortcommandresponsereceived)
- [var kOBEXSessionEventTypeConnectCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeconnectcommandreceived)
- [var kOBEXSessionEventTypeConnectCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeconnectcommandresponsereceived)
- [var kOBEXSessionEventTypeDisconnectCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypedisconnectcommandreceived)
- [var kOBEXSessionEventTypeDisconnectCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypedisconnectcommandresponsereceived)
- [var kOBEXSessionEventTypeError: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeerror)
- [var kOBEXSessionEventTypeGetCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypegetcommandreceived)
- [var kOBEXSessionEventTypeGetCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypegetcommandresponsereceived)
- [var kOBEXSessionEventTypePutCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeputcommandreceived)
- [var kOBEXSessionEventTypePutCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypeputcommandresponsereceived)
- [var kOBEXSessionEventTypeSetPathCommandReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypesetpathcommandreceived)
- [var kOBEXSessionEventTypeSetPathCommandResponseReceived: OBEXSessionEventTypes](/documentation/iobluetooth/kobexsessioneventtypesetpathcommandresponsereceived)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexsessioneventtypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexsessioneventtypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexsessioneventtypes/rawvalue)
- [OBEXSessionParameterTags](/documentation/iobluetooth/obexsessionparametertags)

#### Constants

- [var kOBEXSessionParameterTagDeviceAddress: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagdeviceaddress)
- [var kOBEXSessionParameterTagNextSequenceNumber: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagnextsequencenumber)
- [var kOBEXSessionParameterTagNonce: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagnonce)
- [var kOBEXSessionParameterTagSessionID: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagsessionid)
- [var kOBEXSessionParameterTagSessionOpcode: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagsessionopcode)
- [var kOBEXSessionParameterTagTimeout: OBEXSessionParameterTags](/documentation/iobluetooth/kobexsessionparametertagtimeout)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexsessionparametertags/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexsessionparametertags/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexsessionparametertags/rawvalue)
- [OBEXSessionRef](/documentation/iobluetooth/obexsessionref)
- [OBEXTransportEventType](/documentation/iobluetooth/obextransporteventtype)
- [OBEXTransportEventTypes](/documentation/iobluetooth/obextransporteventtypes)

#### Constants

- [var kOBEXTransportEventTypeDataReceived: OBEXTransportEventTypes](/documentation/iobluetooth/kobextransporteventtypedatareceived)
- [var kOBEXTransportEventTypeStatus: OBEXTransportEventTypes](/documentation/iobluetooth/kobextransporteventtypestatus)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obextransporteventtypes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obextransporteventtypes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obextransporteventtypes/rawvalue)
- [OBEXVersion](/documentation/iobluetooth/obexversion)
- [OBEXVersions](/documentation/iobluetooth/obexversions)

#### Constants

- [var kOBEXVersion10: OBEXVersions](/documentation/iobluetooth/kobexversion10)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/obexversions/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/obexversions/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/obexversions/rawvalue)
- [PrivOBEXSessionDataRef](/documentation/iobluetooth/privobexsessiondataref)
- [ProtocolParameters](/documentation/iobluetooth/protocolparameters)

#### Constants

- [var kBluetoothSDPProtocolParameterBNEPSupportedNetworkPacketTypeList: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterbnepsupportednetworkpackettypelist)
- [var kBluetoothSDPProtocolParameterBNEPVersion: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterbnepversion)
- [var kBluetoothSDPProtocolParameterL2CAPPSM: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterl2cappsm)
- [var kBluetoothSDPProtocolParameterRFCOMMChannel: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterrfcommchannel)
- [var kBluetoothSDPProtocolParameterTCPPort: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparametertcpport)
- [var kBluetoothSDPProtocolParameterUDPPort: ProtocolParameters](/documentation/iobluetooth/kbluetoothsdpprotocolparameterudpport)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/protocolparameters/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/protocolparameters/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/protocolparameters/rawvalue)
- [SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/sdpattributedeviceidentificationrecord)

#### Constants

- [var kBluetoothSDPAttributeDeviceIdentifierClientExecutableURL: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierclientexecutableurl)
- [var kBluetoothSDPAttributeDeviceIdentifierDocumentationURL: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierdocumentationurl)
- [var kBluetoothSDPAttributeDeviceIdentifierPrimaryRecord: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierprimaryrecord)
- [var kBluetoothSDPAttributeDeviceIdentifierProductID: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierproductid)
- [var kBluetoothSDPAttributeDeviceIdentifierReservedRangeEnd: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierreservedrangeend)
- [var kBluetoothSDPAttributeDeviceIdentifierReservedRangeStart: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierreservedrangestart)
- [var kBluetoothSDPAttributeDeviceIdentifierServiceDescription: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierservicedescription)
- [var kBluetoothSDPAttributeDeviceIdentifierSpecificationID: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierspecificationid)
- [var kBluetoothSDPAttributeDeviceIdentifierVendorID: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifiervendorid)
- [var kBluetoothSDPAttributeDeviceIdentifierVendorIDSource: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifiervendoridsource)
- [var kBluetoothSDPAttributeDeviceIdentifierVersion: SDPAttributeDeviceIdentificationRecord](/documentation/iobluetooth/kbluetoothsdpattributedeviceidentifierversion)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/sdpattributedeviceidentificationrecord/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/sdpattributedeviceidentificationrecord/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/sdpattributedeviceidentificationrecord/rawvalue)
- [SDPAttributeIdentifierCodes](/documentation/iobluetooth/sdpattributeidentifiercodes)

#### Constants

- [var kBluetoothSDPAttributeIdentifierAdditionalProtocolsDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifieradditionalprotocolsdescriptorlist)
- [var kBluetoothSDPAttributeIdentifierAudioFeedbackSupport: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifieraudiofeedbacksupport)
- [var kBluetoothSDPAttributeIdentifierBluetoothProfileDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierbluetoothprofiledescriptorlist)
- [var kBluetoothSDPAttributeIdentifierBrowseGroupList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierbrowsegrouplist)
- [var kBluetoothSDPAttributeIdentifierClientExecutableURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierclientexecutableurl)
- [var kBluetoothSDPAttributeIdentifierDocumentationURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierdocumentationurl)
- [var kBluetoothSDPAttributeIdentifierExternalNetwork: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierexternalnetwork)
- [var kBluetoothSDPAttributeIdentifierFaxClass1Support: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierfaxclass1support)
- [var kBluetoothSDPAttributeIdentifierFaxClass2Support: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierfaxclass2support)
- [var kBluetoothSDPAttributeIdentifierFaxClass2_0Support: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierfaxclass2_0support)
- [var kBluetoothSDPAttributeIdentifierGroupID: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiergroupid)
- [var kBluetoothSDPAttributeIdentifierHIDBatteryPower: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidbatterypower)
- [var kBluetoothSDPAttributeIdentifierHIDBootDevice: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidbootdevice)
- [var kBluetoothSDPAttributeIdentifierHIDCountryCode: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidcountrycode)
- [var kBluetoothSDPAttributeIdentifierHIDDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhiddescriptorlist)
- [var kBluetoothSDPAttributeIdentifierHIDDeviceSubclass: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhiddevicesubclass)
- [var kBluetoothSDPAttributeIdentifierHIDLangIDBaseList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidlangidbaselist)
- [var kBluetoothSDPAttributeIdentifierHIDNormallyConnectable: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidnormallyconnectable)
- [var kBluetoothSDPAttributeIdentifierHIDParserVersion: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidparserversion)
- [var kBluetoothSDPAttributeIdentifierHIDProfileVersion: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidprofileversion)
- [var kBluetoothSDPAttributeIdentifierHIDReconnectInitiate: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidreconnectinitiate)
- [var kBluetoothSDPAttributeIdentifierHIDReleaseNumber: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidreleasenumber)
- [var kBluetoothSDPAttributeIdentifierHIDRemoteWake: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidremotewake)
- [var kBluetoothSDPAttributeIdentifierHIDSDPDisable: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidsdpdisable)
- [var kBluetoothSDPAttributeIdentifierHIDSSRHostMaxLatency: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidssrhostmaxlatency)
- [var kBluetoothSDPAttributeIdentifierHIDSSRHostMinTimeout: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidssrhostmintimeout)
- [var kBluetoothSDPAttributeIdentifierHIDSupervisionTimeout: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidsupervisiontimeout)
- [var kBluetoothSDPAttributeIdentifierHIDVirtualCable: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhidvirtualcable)
- [var kBluetoothSDPAttributeIdentifierHomepageURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierhomepageurl)
- [var kBluetoothSDPAttributeIdentifierIPSubnet: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifieripsubnet)
- [var kBluetoothSDPAttributeIdentifierIconURL: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiericonurl)
- [var kBluetoothSDPAttributeIdentifierLanguageBaseAttributeIDList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierlanguagebaseattributeidlist)
- [var kBluetoothSDPAttributeIdentifierMaxNetAccessRate: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiermaxnetaccessrate)
- [var kBluetoothSDPAttributeIdentifierNetAccessType: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiernetaccesstype)
- [var kBluetoothSDPAttributeIdentifierNetwork: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiernetwork)
- [var kBluetoothSDPAttributeIdentifierNetworkAddress: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiernetworkaddress)
- [var kBluetoothSDPAttributeIdentifierProtocolDescriptorList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierprotocoldescriptorlist)
- [var kBluetoothSDPAttributeIdentifierProviderName: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierprovidername)
- [var kBluetoothSDPAttributeIdentifierRemoteAudioVolumeControl: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierremoteaudiovolumecontrol)
- [var kBluetoothSDPAttributeIdentifierSecurityDescription: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersecuritydescription)
- [var kBluetoothSDPAttributeIdentifierServiceAvailability: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceavailability)
- [var kBluetoothSDPAttributeIdentifierServiceClassIDList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceclassidlist)
- [var kBluetoothSDPAttributeIdentifierServiceDatabaseState: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicedatabasestate)
- [var kBluetoothSDPAttributeIdentifierServiceDescription: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicedescription)
- [var kBluetoothSDPAttributeIdentifierServiceID: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceid)
- [var kBluetoothSDPAttributeIdentifierServiceInfoTimeToLive: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceinfotimetolive)
- [var kBluetoothSDPAttributeIdentifierServiceName: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicename)
- [var kBluetoothSDPAttributeIdentifierServiceRecordHandle: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicerecordhandle)
- [var kBluetoothSDPAttributeIdentifierServiceRecordState: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierservicerecordstate)
- [var kBluetoothSDPAttributeIdentifierServiceVersion: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierserviceversion)
- [var kBluetoothSDPAttributeIdentifierSupportedCapabilities: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupportedcapabilities)
- [var kBluetoothSDPAttributeIdentifierSupportedDataStoresList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupporteddatastoreslist)
- [var kBluetoothSDPAttributeIdentifierSupportedFeatures: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupportedfeatures)
- [var kBluetoothSDPAttributeIdentifierSupportedFunctions: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupportedfunctions)
- [var kBluetoothSDPAttributeIdentifierSupporterFormatsList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiersupporterformatslist)
- [var kBluetoothSDPAttributeIdentifierTotalImagingDataCapacity: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifiertotalimagingdatacapacity)
- [var kBluetoothSDPAttributeIdentifierVersionNumberList: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierversionnumberlist)
- [var kBluetoothSDPAttributeIdentifierWAPGateway: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierwapgateway)
- [var kBluetoothSDPAttributeIdentifierWAPStackType: SDPAttributeIdentifierCodes](/documentation/iobluetooth/kbluetoothsdpattributeidentifierwapstacktype)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/sdpattributeidentifiercodes/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/sdpattributeidentifiercodes/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/sdpattributeidentifiercodes/rawvalue)
- [SDPServiceClasses](/documentation/iobluetooth/sdpserviceclasses)

#### Constants

- [var kBluetoothSDPUUID16ServiceClassAVRemoteControl: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassavremotecontrol)
- [var kBluetoothSDPUUID16ServiceClassAVRemoteControlController: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassavremotecontrolcontroller)
- [var kBluetoothSDPUUID16ServiceClassAVRemoteControlTarget: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassavremotecontroltarget)
- [var kBluetoothSDPUUID16ServiceClassAdvancedAudioDistribution: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassadvancedaudiodistribution)
- [var kBluetoothSDPUUID16ServiceClassAudioSink: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassaudiosink)
- [var kBluetoothSDPUUID16ServiceClassAudioSource: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassaudiosource)
- [var kBluetoothSDPUUID16ServiceClassAudioVideo: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassaudiovideo)
- [var kBluetoothSDPUUID16ServiceClassBasicPrinting: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassbasicprinting)
- [var kBluetoothSDPUUID16ServiceClassBrowseGroupDescriptor: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassbrowsegroupdescriptor)
- [var kBluetoothSDPUUID16ServiceClassCommonISDNAccess: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasscommonisdnaccess)
- [var kBluetoothSDPUUID16ServiceClassCordlessTelephony: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasscordlesstelephony)
- [var kBluetoothSDPUUID16ServiceClassDialupNetworking: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassdialupnetworking)
- [var kBluetoothSDPUUID16ServiceClassDirectPrinting: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassdirectprinting)
- [var kBluetoothSDPUUID16ServiceClassDirectPrintingReferenceObjectsService: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassdirectprintingreferenceobjectsservice)
- [var kBluetoothSDPUUID16ServiceClassFax: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassfax)
- [var kBluetoothSDPUUID16ServiceClassGN: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgn)
- [var kBluetoothSDPUUID16ServiceClassGenericAudio: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenericaudio)
- [var kBluetoothSDPUUID16ServiceClassGenericFileTransfer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenericfiletransfer)
- [var kBluetoothSDPUUID16ServiceClassGenericNetworking: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenericnetworking)
- [var kBluetoothSDPUUID16ServiceClassGenericTelephony: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgenerictelephony)
- [var kBluetoothSDPUUID16ServiceClassGlobalNavigationSatelliteSystem: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassglobalnavigationsatellitesystem)
- [var kBluetoothSDPUUID16ServiceClassGlobalNavigationSatelliteSystemServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassglobalnavigationsatellitesystemserver)
- [var kBluetoothSDPUUID16ServiceClassHCR_Print: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshcr_print)
- [var kBluetoothSDPUUID16ServiceClassHCR_Scan: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshcr_scan)
- [var kBluetoothSDPUUID16ServiceClassHandsFree: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshandsfree)
- [var kBluetoothSDPUUID16ServiceClassHandsFreeAudioGateway: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshandsfreeaudiogateway)
- [var kBluetoothSDPUUID16ServiceClassHardcopyCableReplacement: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshardcopycablereplacement)
- [var kBluetoothSDPUUID16ServiceClassHeadset: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassheadset)
- [var kBluetoothSDPUUID16ServiceClassHeadsetAudioGateway: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassheadsetaudiogateway)
- [var kBluetoothSDPUUID16ServiceClassHeadset_HS: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassheadset_hs)
- [var kBluetoothSDPUUID16ServiceClassHealthDevice: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshealthdevice)
- [var kBluetoothSDPUUID16ServiceClassHealthDeviceSink: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshealthdevicesink)
- [var kBluetoothSDPUUID16ServiceClassHealthDeviceSource: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshealthdevicesource)
- [var kBluetoothSDPUUID16ServiceClassHumanInterfaceDeviceService: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasshumaninterfacedeviceservice)
- [var kBluetoothSDPUUID16ServiceClassImaging: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimaging)
- [var kBluetoothSDPUUID16ServiceClassImagingAutomaticArchive: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimagingautomaticarchive)
- [var kBluetoothSDPUUID16ServiceClassImagingReferencedObjects: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimagingreferencedobjects)
- [var kBluetoothSDPUUID16ServiceClassImagingResponder: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassimagingresponder)
- [var kBluetoothSDPUUID16ServiceClassIntercom: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassintercom)
- [var kBluetoothSDPUUID16ServiceClassIrMCSync: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassirmcsync)
- [var kBluetoothSDPUUID16ServiceClassIrMCSyncCommand: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassirmcsynccommand)
- [var kBluetoothSDPUUID16ServiceClassLANAccessUsingPPP: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasslanaccessusingppp)
- [var kBluetoothSDPUUID16ServiceClassMessageAccessProfile: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassmessageaccessprofile)
- [var kBluetoothSDPUUID16ServiceClassMessageAccessServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassmessageaccessserver)
- [var kBluetoothSDPUUID16ServiceClassMessageNotificationServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassmessagenotificationserver)
- [var kBluetoothSDPUUID16ServiceClassNAP: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassnap)
- [var kBluetoothSDPUUID16ServiceClassOBEXFileTransfer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassobexfiletransfer)
- [var kBluetoothSDPUUID16ServiceClassOBEXObjectPush: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassobexobjectpush)
- [var kBluetoothSDPUUID16ServiceClassPANU: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasspanu)
- [var kBluetoothSDPUUID16ServiceClassPhonebookAccess: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassphonebookaccess)
- [var kBluetoothSDPUUID16ServiceClassPhonebookAccess_PCE: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassphonebookaccess_pce)
- [var kBluetoothSDPUUID16ServiceClassPhonebookAccess_PSE: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassphonebookaccess_pse)
- [var kBluetoothSDPUUID16ServiceClassPnPInformation: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasspnpinformation)
- [var kBluetoothSDPUUID16ServiceClassPrintingStatus: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassprintingstatus)
- [var kBluetoothSDPUUID16ServiceClassPublicBrowseGroup: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasspublicbrowsegroup)
- [var kBluetoothSDPUUID16ServiceClassReferencePrinting: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassreferenceprinting)
- [var kBluetoothSDPUUID16ServiceClassReflectedUI: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassreflectedui)
- [var kBluetoothSDPUUID16ServiceClassSIM_Access: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasssim_access)
- [var kBluetoothSDPUUID16ServiceClassSerialPort: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassserialport)
- [var kBluetoothSDPUUID16ServiceClassServiceDiscoveryServer: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassservicediscoveryserver)
- [var kBluetoothSDPUUID16ServiceClassUDI_MT: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassudi_mt)
- [var kBluetoothSDPUUID16ServiceClassUDI_TA: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassudi_ta)
- [var kBluetoothSDPUUID16ServiceClassVideoConferencingGW: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideoconferencinggw)
- [var kBluetoothSDPUUID16ServiceClassVideoDistribution: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideodistribution)
- [var kBluetoothSDPUUID16ServiceClassVideoSink: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideosink)
- [var kBluetoothSDPUUID16ServiceClassVideoSource: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassvideosource)
- [var kBluetoothSDPUUID16ServiceClassWAP: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasswap)
- [var kBluetoothSDPUUID16ServiceClassWAPClient: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclasswapclient)
- [var kBluetoothSDPUUID16ServiceClassGATT: SDPServiceClasses](/documentation/iobluetooth/kbluetoothsdpuuid16serviceclassgatt)

#### Initializers

- [init(UInt32)](/documentation/iobluetooth/sdpserviceclasses/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetooth/sdpserviceclasses/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetooth/sdpserviceclasses/rawvalue)
- [TransmissionPower](/documentation/iobluetooth/transmissionpower)
- [BluetoothHCIEncryptionKeySize](/documentation/iobluetooth/bluetoothhciencryptionkeysize)

## Variables

- [var kBluetoothConnectionHandleSerialDeviceReserved: Int](/documentation/iobluetooth/kbluetoothconnectionhandleserialdevicereserved)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
