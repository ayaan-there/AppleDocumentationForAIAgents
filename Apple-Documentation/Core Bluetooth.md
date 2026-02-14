# Core Bluetooth Documentation

Source: https://sosumi.ai/documentation/corebluetooth

---
title: Core Bluetooth
source: https://developer.apple.com/documentation/corebluetooth
timestamp: 2026-02-13T18:55:14.426Z
---

## Centrals

- [CBCentral](/documentation/corebluetooth/cbcentral)

### Identifying a Remote Central

- [var maximumUpdateValueLength: Int](/documentation/corebluetooth/cbcentral/maximumupdatevaluelength)

#### Related Documentation

- [func updateValue(Data, for: CBMutableCharacteristic, onSubscribedCentrals: [CBCentral]?) -> Bool](/documentation/corebluetooth/cbperipheralmanager/updatevalue(_:for:onsubscribedcentrals:))
- [CBCentralManager](/documentation/corebluetooth/cbcentralmanager)

### Initializing a Central Manager

- [convenience init()](/documentation/corebluetooth/cbcentralmanager/init())
- [convenience init(delegate: (any CBCentralManagerDelegate)?, queue: dispatch_queue_t?)](/documentation/corebluetooth/cbcentralmanager/init(delegate:queue:))
- [init(delegate: (any CBCentralManagerDelegate)?, queue: dispatch_queue_t?, options: [String : Any]?)](/documentation/corebluetooth/cbcentralmanager/init(delegate:queue:options:))
- [Central Manager Initialization Options](/documentation/corebluetooth/central-manager-initialization-options)

#### Constants

- [let CBCentralManagerOptionShowPowerAlertKey: String](/documentation/corebluetooth/cbcentralmanageroptionshowpoweralertkey)
- [let CBCentralManagerOptionRestoreIdentifierKey: String](/documentation/corebluetooth/cbcentralmanageroptionrestoreidentifierkey)
- [Central Manager State Restoration Options](/documentation/corebluetooth/central-manager-state-restoration-options)

#### State Restoration Options

- [let CBCentralManagerRestoredStatePeripheralsKey: String](/documentation/corebluetooth/cbcentralmanagerrestoredstateperipheralskey)
- [let CBCentralManagerRestoredStateScanServicesKey: String](/documentation/corebluetooth/cbcentralmanagerrestoredstatescanserviceskey)
- [let CBCentralManagerRestoredStateScanOptionsKey: String](/documentation/corebluetooth/cbcentralmanagerrestoredstatescanoptionskey)

### Establishing or Canceling Connections with Peripherals

- [func connect(CBPeripheral, options: [String : Any]?)](/documentation/corebluetooth/cbcentralmanager/connect(_:options:))
- [Peripheral Connection Options](/documentation/corebluetooth/peripheral-connection-options)

#### Options

- [let CBConnectPeripheralOptionEnableAutoReconnect: String](/documentation/corebluetooth/cbconnectperipheraloptionenableautoreconnect)
- [let CBConnectPeripheralOptionEnableTransportBridgingKey: String](/documentation/corebluetooth/cbconnectperipheraloptionenabletransportbridgingkey)
- [let CBConnectPeripheralOptionNotifyOnConnectionKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyonconnectionkey)
- [let CBConnectPeripheralOptionNotifyOnDisconnectionKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyondisconnectionkey)
- [let CBConnectPeripheralOptionNotifyOnNotificationKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyonnotificationkey)
- [let CBConnectPeripheralOptionRequiresANCS: String](/documentation/corebluetooth/cbconnectperipheraloptionrequiresancs)
- [let CBConnectPeripheralOptionStartDelayKey: String](/documentation/corebluetooth/cbconnectperipheraloptionstartdelaykey)
- [func cancelPeripheralConnection(CBPeripheral)](/documentation/corebluetooth/cbcentralmanager/cancelperipheralconnection(_:))

### Retrieving Lists of Peripherals

- [func retrieveConnectedPeripherals(withServices: [CBUUID]) -> [CBPeripheral]](/documentation/corebluetooth/cbcentralmanager/retrieveconnectedperipherals(withservices:))
- [func retrievePeripherals(withIdentifiers: [UUID]) -> [CBPeripheral]](/documentation/corebluetooth/cbcentralmanager/retrieveperipherals(withidentifiers:))

### Scanning or Stopping Scans of Peripherals

- [func scanForPeripherals(withServices: [CBUUID]?, options: [String : Any]?)](/documentation/corebluetooth/cbcentralmanager/scanforperipherals(withservices:options:))
- [Peripheral Scanning Options](/documentation/corebluetooth/peripheral-scanning-options)

#### Constants

- [let CBCentralManagerScanOptionAllowDuplicatesKey: String](/documentation/corebluetooth/cbcentralmanagerscanoptionallowduplicateskey)
- [let CBCentralManagerScanOptionSolicitedServiceUUIDsKey: String](/documentation/corebluetooth/cbcentralmanagerscanoptionsolicitedserviceuuidskey)
- [func stopScan()](/documentation/corebluetooth/cbcentralmanager/stopscan())
- [var isScanning: Bool](/documentation/corebluetooth/cbcentralmanager/isscanning)

### Inspecting Feature Support

- [class func supports(CBCentralManager.Feature) -> Bool](/documentation/corebluetooth/cbcentralmanager/supports(_:))
- [CBCentralManager.Feature](/documentation/corebluetooth/cbcentralmanager/feature)

#### Creating a Central Manager Feature Instance

- [init(rawValue: UInt)](/documentation/corebluetooth/cbcentralmanager/feature/init(rawvalue:))

#### Extended Scan Features

- [static var extendedScanAndConnect: CBCentralManager.Feature](/documentation/corebluetooth/cbcentralmanager/feature/extendedscanandconnect)

### Monitoring Properties

- [var delegate: (any CBCentralManagerDelegate)?](/documentation/corebluetooth/cbcentralmanager/delegate)

### Receiving Connection Events

- [func registerForConnectionEvents(options: [CBConnectionEventMatchingOption : Any]?)](/documentation/corebluetooth/cbcentralmanager/registerforconnectionevents(options:))
- [Peripheral Connection Options](/documentation/corebluetooth/peripheral-connection-options)

#### Options

- [let CBConnectPeripheralOptionEnableAutoReconnect: String](/documentation/corebluetooth/cbconnectperipheraloptionenableautoreconnect)
- [let CBConnectPeripheralOptionEnableTransportBridgingKey: String](/documentation/corebluetooth/cbconnectperipheraloptionenabletransportbridgingkey)
- [let CBConnectPeripheralOptionNotifyOnConnectionKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyonconnectionkey)
- [let CBConnectPeripheralOptionNotifyOnDisconnectionKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyondisconnectionkey)
- [let CBConnectPeripheralOptionNotifyOnNotificationKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyonnotificationkey)
- [let CBConnectPeripheralOptionRequiresANCS: String](/documentation/corebluetooth/cbconnectperipheraloptionrequiresancs)
- [let CBConnectPeripheralOptionStartDelayKey: String](/documentation/corebluetooth/cbconnectperipheraloptionstartdelaykey)
- [CBConnectionEvent](/documentation/corebluetooth/cbconnectionevent)

#### Events

- [case peerConnected](/documentation/corebluetooth/cbconnectionevent/peerconnected)
- [case peerDisconnected](/documentation/corebluetooth/cbconnectionevent/peerdisconnected)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbconnectionevent/init(rawvalue:))
- [CBConnectionEventMatchingOption](/documentation/corebluetooth/cbconnectioneventmatchingoption)

#### Creating a Matching Option Instance

- [init(rawValue: String)](/documentation/corebluetooth/cbconnectioneventmatchingoption/init(rawvalue:))

#### Matching Options

- [static let peripheralUUIDs: CBConnectionEventMatchingOption](/documentation/corebluetooth/cbconnectioneventmatchingoption/peripheraluuids)
- [static let serviceUUIDs: CBConnectionEventMatchingOption](/documentation/corebluetooth/cbconnectioneventmatchingoption/serviceuuids)

### Deprecated

- [CBCentralManagerState](/documentation/corebluetooth/cbcentralmanagerstate)

#### Constants

- [case poweredOff](/documentation/corebluetooth/cbcentralmanagerstate/poweredoff)
- [case poweredOn](/documentation/corebluetooth/cbcentralmanagerstate/poweredon)
- [case resetting](/documentation/corebluetooth/cbcentralmanagerstate/resetting)
- [case unauthorized](/documentation/corebluetooth/cbcentralmanagerstate/unauthorized)
- [case unknown](/documentation/corebluetooth/cbcentralmanagerstate/unknown)
- [case unsupported](/documentation/corebluetooth/cbcentralmanagerstate/unsupported)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbcentralmanagerstate/init(rawvalue:))
- [CBCentralManagerDelegate](/documentation/corebluetooth/cbcentralmanagerdelegate)

### Monitoring Connections with Peripherals

- [func centralManager(CBCentralManager, didConnect: CBPeripheral)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:didconnect:))
- [func centralManager(CBCentralManager, didDisconnectPeripheral: CBPeripheral, error: (any Error)?)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:diddisconnectperipheral:error:))
- [func centralManager(CBCentralManager, didFailToConnect: CBPeripheral, error: (any Error)?)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:didfailtoconnect:error:))
- [func centralManager(CBCentralManager, connectionEventDidOccur: CBConnectionEvent, for: CBPeripheral)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:connectioneventdidoccur:for:))

### Discovering and Retrieving Peripherals

- [func centralManager(CBCentralManager, didDiscover: CBPeripheral, advertisementData: [String : Any], rssi: NSNumber)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:diddiscover:advertisementdata:rssi:))
- [Advertisement Data Retrieval Keys](/documentation/corebluetooth/advertisement-data-retrieval-keys)

#### Advertisement Keys

- [let CBAdvertisementDataLocalNameKey: String](/documentation/corebluetooth/cbadvertisementdatalocalnamekey)
- [let CBAdvertisementDataManufacturerDataKey: String](/documentation/corebluetooth/cbadvertisementdatamanufacturerdatakey)
- [let CBAdvertisementDataServiceDataKey: String](/documentation/corebluetooth/cbadvertisementdataservicedatakey)
- [let CBAdvertisementDataServiceUUIDsKey: String](/documentation/corebluetooth/cbadvertisementdataserviceuuidskey)
- [let CBAdvertisementDataOverflowServiceUUIDsKey: String](/documentation/corebluetooth/cbadvertisementdataoverflowserviceuuidskey)
- [let CBAdvertisementDataTxPowerLevelKey: String](/documentation/corebluetooth/cbadvertisementdatatxpowerlevelkey)
- [let CBAdvertisementDataIsConnectable: String](/documentation/corebluetooth/cbadvertisementdataisconnectable)
- [let CBAdvertisementDataSolicitedServiceUUIDsKey: String](/documentation/corebluetooth/cbadvertisementdatasolicitedserviceuuidskey)

### Monitoring the Central Manager’s State

- [func centralManagerDidUpdateState(CBCentralManager)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanagerdidupdatestate(_:))
- [func centralManager(CBCentralManager, willRestoreState: [String : Any])](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:willrestorestate:))

### Monitoring the Central Manager’s Authorization

- [func centralManager(CBCentralManager, didUpdateANCSAuthorizationFor: CBPeripheral)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:didupdateancsauthorizationfor:))

### Instance Methods

- [func centralManager(CBCentralManager, didDisconnectPeripheral: CBPeripheral, timestamp: CFAbsoluteTime, isReconnecting: Bool, error: (any Error)?)](/documentation/corebluetooth/cbcentralmanagerdelegate/centralmanager(_:diddisconnectperipheral:timestamp:isreconnecting:error:))

## Peripherals

- [CBPeripheral](/documentation/corebluetooth/cbperipheral)

### Identifying a Peripheral

- [var name: String?](/documentation/corebluetooth/cbperipheral/name)

#### Related Documentation

- [func peripheralDidUpdateName(CBPeripheral)](/documentation/corebluetooth/cbperipheraldelegate/peripheraldidupdatename(_:))
- [var delegate: (any CBPeripheralDelegate)?](/documentation/corebluetooth/cbperipheral/delegate)

### Discovering Services

- [func discoverServices([CBUUID]?)](/documentation/corebluetooth/cbperipheral/discoverservices(_:))
- [func discoverIncludedServices([CBUUID]?, for: CBService)](/documentation/corebluetooth/cbperipheral/discoverincludedservices(_:for:))
- [var services: [CBService]?](/documentation/corebluetooth/cbperipheral/services)

### Discovering Characteristics and Descriptors

- [func discoverCharacteristics([CBUUID]?, for: CBService)](/documentation/corebluetooth/cbperipheral/discovercharacteristics(_:for:))
- [func discoverDescriptors(for: CBCharacteristic)](/documentation/corebluetooth/cbperipheral/discoverdescriptors(for:))

### Reading Characteristic and Descriptor Values

- [func readValue(for: CBCharacteristic)](/documentation/corebluetooth/cbperipheral/readvalue(for:)-6u2kr)
- [func readValue(for: CBDescriptor)](/documentation/corebluetooth/cbperipheral/readvalue(for:)-91hhp)

### Writing Characteristic and Descriptor Values

- [func writeValue(Data, for: CBCharacteristic, type: CBCharacteristicWriteType)](/documentation/corebluetooth/cbperipheral/writevalue(_:for:type:))
- [func writeValue(Data, for: CBDescriptor)](/documentation/corebluetooth/cbperipheral/writevalue(_:for:))
- [func maximumWriteValueLength(for: CBCharacteristicWriteType) -> Int](/documentation/corebluetooth/cbperipheral/maximumwritevaluelength(for:))
- [CBCharacteristicWriteType](/documentation/corebluetooth/cbcharacteristicwritetype)

#### Write Types

- [case withResponse](/documentation/corebluetooth/cbcharacteristicwritetype/withresponse)
- [case withoutResponse](/documentation/corebluetooth/cbcharacteristicwritetype/withoutresponse)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbcharacteristicwritetype/init(rawvalue:))

### Setting Notifications for a Characteristic’s Value

- [func setNotifyValue(Bool, for: CBCharacteristic)](/documentation/corebluetooth/cbperipheral/setnotifyvalue(_:for:))

#### Related Documentation

- [let CBConnectPeripheralOptionNotifyOnNotificationKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyonnotificationkey)

### Monitoring a Peripheral’s Connection State

- [var state: CBPeripheralState](/documentation/corebluetooth/cbperipheral/state)
- [CBPeripheralState](/documentation/corebluetooth/cbperipheralstate)

#### Peripheral States

- [case disconnected](/documentation/corebluetooth/cbperipheralstate/disconnected)
- [case connecting](/documentation/corebluetooth/cbperipheralstate/connecting)
- [case connected](/documentation/corebluetooth/cbperipheralstate/connected)
- [case disconnecting](/documentation/corebluetooth/cbperipheralstate/disconnecting)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbperipheralstate/init(rawvalue:))
- [var canSendWriteWithoutResponse: Bool](/documentation/corebluetooth/cbperipheral/cansendwritewithoutresponse)

### Accessing a Peripheral’s Signal Strength

- [func readRSSI()](/documentation/corebluetooth/cbperipheral/readrssi())
- [var rssi: NSNumber?](/documentation/corebluetooth/cbperipheral/rssi)

### Working with L2CAP Channels

- [func openL2CAPChannel(CBL2CAPPSM)](/documentation/corebluetooth/cbperipheral/openl2capchannel(_:))
- [CBL2CAPChannel](/documentation/corebluetooth/cbl2capchannel)

#### Accessing Streams

- [var inputStream: InputStream!](/documentation/corebluetooth/cbl2capchannel/inputstream)
- [var outputStream: OutputStream!](/documentation/corebluetooth/cbl2capchannel/outputstream)

#### Accessing the Peer

- [var peer: CBPeer!](/documentation/corebluetooth/cbl2capchannel/peer)

#### Accessing the Protocol/Service Multiplexer

- [var psm: CBL2CAPPSM](/documentation/corebluetooth/cbl2capchannel/psm)
- [CBL2CAPPSM](/documentation/corebluetooth/cbl2cappsm)

### Working with Apple Notification Center Service (ANCS)

- [var ancsAuthorized: Bool](/documentation/corebluetooth/cbperipheral/ancsauthorized)
- [CBPeripheralDelegate](/documentation/corebluetooth/cbperipheraldelegate)

### Discovering Services

- [func peripheral(CBPeripheral, didDiscoverServices: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:diddiscoverservices:))
- [func peripheral(CBPeripheral, didDiscoverIncludedServicesFor: CBService, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:diddiscoverincludedservicesfor:error:))

### Discovering Characteristics and their Descriptors

- [func peripheral(CBPeripheral, didDiscoverCharacteristicsFor: CBService, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:diddiscovercharacteristicsfor:error:))
- [func peripheral(CBPeripheral, didDiscoverDescriptorsFor: CBCharacteristic, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:diddiscoverdescriptorsfor:error:))

### Retrieving Characteristic and Descriptor Values

- [func peripheral(CBPeripheral, didUpdateValueFor: CBCharacteristic, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didupdatevaluefor:error:)-1xyna)
- [func peripheral(CBPeripheral, didUpdateValueFor: CBDescriptor, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didupdatevaluefor:error:)-1t3wm)

### Writing Characteristic and Descriptor Values

- [func peripheral(CBPeripheral, didWriteValueFor: CBCharacteristic, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didwritevaluefor:error:)-4f5ea)
- [func peripheral(CBPeripheral, didWriteValueFor: CBDescriptor, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didwritevaluefor:error:)-1ybl3)
- [func peripheralIsReady(toSendWriteWithoutResponse: CBPeripheral)](/documentation/corebluetooth/cbperipheraldelegate/peripheralisready(tosendwritewithoutresponse:))

### Managing Notifications for a Characteristic’s Value

- [func peripheral(CBPeripheral, didUpdateNotificationStateFor: CBCharacteristic, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didupdatenotificationstatefor:error:))

### Retrieving a Peripheral’s RSSI Data

- [func peripheral(CBPeripheral, didReadRSSI: NSNumber, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didreadrssi:error:))
- [func peripheralDidUpdateRSSI(CBPeripheral, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheraldidupdaterssi(_:error:))

### Monitoring Changes to a Peripheral’s Name or Services

- [func peripheralDidUpdateName(CBPeripheral)](/documentation/corebluetooth/cbperipheraldelegate/peripheraldidupdatename(_:))
- [func peripheral(CBPeripheral, didModifyServices: [CBService])](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didmodifyservices:))

### Monitoring L2CAP Channels

- [func peripheral(CBPeripheral, didOpen: CBL2CAPChannel?, error: (any Error)?)](/documentation/corebluetooth/cbperipheraldelegate/peripheral(_:didopen:error:))
- [CBPeripheralManager](/documentation/corebluetooth/cbperipheralmanager)

### Initializing a Peripheral Manager

- [convenience init()](/documentation/corebluetooth/cbperipheralmanager/init())
- [convenience init(delegate: (any CBPeripheralManagerDelegate)?, queue: dispatch_queue_t?)](/documentation/corebluetooth/cbperipheralmanager/init(delegate:queue:))
- [init(delegate: (any CBPeripheralManagerDelegate)?, queue: dispatch_queue_t?, options: [String : Any]?)](/documentation/corebluetooth/cbperipheralmanager/init(delegate:queue:options:))
- [var delegate: (any CBPeripheralManagerDelegate)?](/documentation/corebluetooth/cbperipheralmanager/delegate)
- [Peripheral Manager Initialization Options](/documentation/corebluetooth/peripheral-manager-initialization-options)

#### Initialization Options

- [let CBPeripheralManagerOptionShowPowerAlertKey: String](/documentation/corebluetooth/cbperipheralmanageroptionshowpoweralertkey)
- [let CBPeripheralManagerOptionRestoreIdentifierKey: String](/documentation/corebluetooth/cbperipheralmanageroptionrestoreidentifierkey)

### Monitoring the State of a Peripheral Manager

- [class func authorizationStatus() -> CBPeripheralManagerAuthorizationStatus](/documentation/corebluetooth/cbperipheralmanager/authorizationstatus())
- [CBPeripheralManagerAuthorizationStatus](/documentation/corebluetooth/cbperipheralmanagerauthorizationstatus)

#### Constants

- [case notDetermined](/documentation/corebluetooth/cbperipheralmanagerauthorizationstatus/notdetermined)
- [case restricted](/documentation/corebluetooth/cbperipheralmanagerauthorizationstatus/restricted)
- [case denied](/documentation/corebluetooth/cbperipheralmanagerauthorizationstatus/denied)
- [case authorized](/documentation/corebluetooth/cbperipheralmanagerauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbperipheralmanagerauthorizationstatus/init(rawvalue:))
- [CBPeripheralManagerState](/documentation/corebluetooth/cbperipheralmanagerstate)

#### Constants

- [case unknown](/documentation/corebluetooth/cbperipheralmanagerstate/unknown)
- [case resetting](/documentation/corebluetooth/cbperipheralmanagerstate/resetting)
- [case unsupported](/documentation/corebluetooth/cbperipheralmanagerstate/unsupported)
- [case unauthorized](/documentation/corebluetooth/cbperipheralmanagerstate/unauthorized)
- [case poweredOff](/documentation/corebluetooth/cbperipheralmanagerstate/poweredoff)
- [case poweredOn](/documentation/corebluetooth/cbperipheralmanagerstate/poweredon)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbperipheralmanagerstate/init(rawvalue:))

### Adding and Removing Services

- [func add(CBMutableService)](/documentation/corebluetooth/cbperipheralmanager/add(_:))
- [func remove(CBMutableService)](/documentation/corebluetooth/cbperipheralmanager/remove(_:))
- [func removeAllServices()](/documentation/corebluetooth/cbperipheralmanager/removeallservices())

### Managing Advertising

- [func startAdvertising([String : Any]?)](/documentation/corebluetooth/cbperipheralmanager/startadvertising(_:))

#### Related Documentation

- [let CBAdvertisementDataOverflowServiceUUIDsKey: String](/documentation/corebluetooth/cbadvertisementdataoverflowserviceuuidskey)
- [Advertising Data](/documentation/corebluetooth/advertising-data)

#### Advertising Keys

- [let CBAdvertisementDataIsConnectable: String](/documentation/corebluetooth/cbadvertisementdataisconnectable)
- [let CBAdvertisementDataLocalNameKey: String](/documentation/corebluetooth/cbadvertisementdatalocalnamekey)
- [let CBAdvertisementDataManufacturerDataKey: String](/documentation/corebluetooth/cbadvertisementdatamanufacturerdatakey)
- [let CBAdvertisementDataOverflowServiceUUIDsKey: String](/documentation/corebluetooth/cbadvertisementdataoverflowserviceuuidskey)
- [let CBAdvertisementDataServiceDataKey: String](/documentation/corebluetooth/cbadvertisementdataservicedatakey)
- [let CBAdvertisementDataServiceUUIDsKey: String](/documentation/corebluetooth/cbadvertisementdataserviceuuidskey)
- [let CBAdvertisementDataSolicitedServiceUUIDsKey: String](/documentation/corebluetooth/cbadvertisementdatasolicitedserviceuuidskey)
- [let CBAdvertisementDataTxPowerLevelKey: String](/documentation/corebluetooth/cbadvertisementdatatxpowerlevelkey)
- [func stopAdvertising()](/documentation/corebluetooth/cbperipheralmanager/stopadvertising())
- [var isAdvertising: Bool](/documentation/corebluetooth/cbperipheralmanager/isadvertising)

### Sending Updates of a Characteristic’s Value

- [func updateValue(Data, for: CBMutableCharacteristic, onSubscribedCentrals: [CBCentral]?) -> Bool](/documentation/corebluetooth/cbperipheralmanager/updatevalue(_:for:onsubscribedcentrals:))

### Responding to Read and Write Requests

- [func respond(to: CBATTRequest, withResult: CBATTError.Code)](/documentation/corebluetooth/cbperipheralmanager/respond(to:withresult:))

### Setting Connection Latency

- [func setDesiredConnectionLatency(CBPeripheralManagerConnectionLatency, for: CBCentral)](/documentation/corebluetooth/cbperipheralmanager/setdesiredconnectionlatency(_:for:))
- [CBPeripheralManagerConnectionLatency](/documentation/corebluetooth/cbperipheralmanagerconnectionlatency)

#### Latency Values

- [case low](/documentation/corebluetooth/cbperipheralmanagerconnectionlatency/low)
- [case medium](/documentation/corebluetooth/cbperipheralmanagerconnectionlatency/medium)
- [case high](/documentation/corebluetooth/cbperipheralmanagerconnectionlatency/high)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbperipheralmanagerconnectionlatency/init(rawvalue:))

### Using L2CAP Channels

- [func publishL2CAPChannel(withEncryption: Bool)](/documentation/corebluetooth/cbperipheralmanager/publishl2capchannel(withencryption:))
- [func unpublishL2CAPChannel(CBL2CAPPSM)](/documentation/corebluetooth/cbperipheralmanager/unpublishl2capchannel(_:))
- [CBPeripheralManagerDelegate](/documentation/corebluetooth/cbperipheralmanagerdelegate)

### Monitoring Changes to the Peripheral Manager’s State

- [func peripheralManagerDidUpdateState(CBPeripheralManager)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanagerdidupdatestate(_:))
- [func peripheralManager(CBPeripheralManager, willRestoreState: [String : Any])](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:willrestorestate:))
- [Peripheral Manager State Restoration Options](/documentation/corebluetooth/peripheral-manager-state-restoration-options)

#### State Restoration Dictionary Keys

- [let CBPeripheralManagerRestoredStateServicesKey: String](/documentation/corebluetooth/cbperipheralmanagerrestoredstateserviceskey)
- [let CBPeripheralManagerRestoredStateAdvertisementDataKey: String](/documentation/corebluetooth/cbperipheralmanagerrestoredstateadvertisementdatakey)

### Adding Services

- [func peripheralManager(CBPeripheralManager, didAdd: CBService, error: (any Error)?)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:didadd:error:))

### Advertising Peripheral Data

- [func peripheralManagerDidStartAdvertising(CBPeripheralManager, error: (any Error)?)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanagerdidstartadvertising(_:error:))

### Monitoring Subscriptions to Characteristic Values

- [func peripheralManager(CBPeripheralManager, central: CBCentral, didSubscribeTo: CBCharacteristic)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:central:didsubscribeto:))
- [func peripheralManager(CBPeripheralManager, central: CBCentral, didUnsubscribeFrom: CBCharacteristic)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:central:didunsubscribefrom:))
- [func peripheralManagerIsReady(toUpdateSubscribers: CBPeripheralManager)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanagerisready(toupdatesubscribers:))

### Receiving Read and Write Requests

- [func peripheralManager(CBPeripheralManager, didReceiveRead: CBATTRequest)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:didreceiveread:))
- [func peripheralManager(CBPeripheralManager, didReceiveWrite: [CBATTRequest])](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:didreceivewrite:))

### Using L2CAP Channels

- [func peripheralManager(CBPeripheralManager, didPublishL2CAPChannel: CBL2CAPPSM, error: (any Error)?)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:didpublishl2capchannel:error:))
- [func peripheralManager(CBPeripheralManager, didUnpublishL2CAPChannel: CBL2CAPPSM, error: (any Error)?)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:didunpublishl2capchannel:error:))
- [func peripheralManager(CBPeripheralManager, didOpen: CBL2CAPChannel?, error: (any Error)?)](/documentation/corebluetooth/cbperipheralmanagerdelegate/peripheralmanager(_:didopen:error:))
- [CBAttribute](/documentation/corebluetooth/cbattribute)

### Identifying an Attribute

- [var uuid: CBUUID](/documentation/corebluetooth/cbattribute/uuid)
- [CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions)

### Creating a Permissions Instance

- [init(rawValue: UInt)](/documentation/corebluetooth/cbattributepermissions/init(rawvalue:))

### Permissions

- [static var readable: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/readable)
- [static var writeable: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/writeable)
- [static var readEncryptionRequired: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/readencryptionrequired)
- [static var writeEncryptionRequired: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/writeencryptionrequired)

## Data Transfer

- [Transferring Data Between Bluetooth Low Energy Devices](/documentation/corebluetooth/transferring-data-between-bluetooth-low-energy-devices)

## Services

- [CBService](/documentation/corebluetooth/cbservice)

### Identifying a Service

- [var peripheral: CBPeripheral?](/documentation/corebluetooth/cbservice/peripheral)
- [var isPrimary: Bool](/documentation/corebluetooth/cbservice/isprimary)

### Accessing Service Data

- [var characteristics: [CBCharacteristic]?](/documentation/corebluetooth/cbservice/characteristics)
- [var includedServices: [CBService]?](/documentation/corebluetooth/cbservice/includedservices)
- [CBMutableService](/documentation/corebluetooth/cbmutableservice)

### Creating a Mutable Service

- [init(type: CBUUID, primary: Bool)](/documentation/corebluetooth/cbmutableservice/init(type:primary:))

### Managing a Mutable Service

- [var characteristics: [CBCharacteristic]?](/documentation/corebluetooth/cbmutableservice/characteristics)
- [var includedServices: [CBService]?](/documentation/corebluetooth/cbmutableservice/includedservices)
- [CBCharacteristic](/documentation/corebluetooth/cbcharacteristic)

### Identifying a Characteristic

- [var service: CBService?](/documentation/corebluetooth/cbcharacteristic/service)

### Accessing Characteristic Data

- [var value: Data?](/documentation/corebluetooth/cbcharacteristic/value)
- [var descriptors: [CBDescriptor]?](/documentation/corebluetooth/cbcharacteristic/descriptors)
- [var properties: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristic/properties)
- [CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties)

#### Creating a Characteristic Properties Instance

- [init(rawValue: UInt)](/documentation/corebluetooth/cbcharacteristicproperties/init(rawvalue:))

#### Characteristic Properties

- [static var broadcast: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/broadcast)
- [static var read: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/read)
- [static var writeWithoutResponse: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/writewithoutresponse)
- [static var write: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/write)
- [static var notify: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/notify)
- [static var indicate: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/indicate)
- [static var authenticatedSignedWrites: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/authenticatedsignedwrites)
- [static var extendedProperties: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/extendedproperties)
- [static var notifyEncryptionRequired: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/notifyencryptionrequired)
- [static var indicateEncryptionRequired: CBCharacteristicProperties](/documentation/corebluetooth/cbcharacteristicproperties/indicateencryptionrequired)
- [var isNotifying: Bool](/documentation/corebluetooth/cbcharacteristic/isnotifying)

#### Related Documentation

- [func setNotifyValue(Bool, for: CBCharacteristic)](/documentation/corebluetooth/cbperipheral/setnotifyvalue(_:for:))

##### Related Documentation

- [let CBConnectPeripheralOptionNotifyOnNotificationKey: String](/documentation/corebluetooth/cbconnectperipheraloptionnotifyonnotificationkey)
- [var isBroadcasted: Bool](/documentation/corebluetooth/cbcharacteristic/isbroadcasted)
- [CBMutableCharacteristic](/documentation/corebluetooth/cbmutablecharacteristic)

### Creating a Mutable Characteristic

- [init(type: CBUUID, properties: CBCharacteristicProperties, value: Data?, permissions: CBAttributePermissions)](/documentation/corebluetooth/cbmutablecharacteristic/init(type:properties:value:permissions:))

### Managing a Mutable Characteristic

- [var value: Data?](/documentation/corebluetooth/cbmutablecharacteristic/value)
- [var descriptors: [CBDescriptor]?](/documentation/corebluetooth/cbmutablecharacteristic/descriptors)
- [var properties: CBCharacteristicProperties](/documentation/corebluetooth/cbmutablecharacteristic/properties)
- [var permissions: CBAttributePermissions](/documentation/corebluetooth/cbmutablecharacteristic/permissions)
- [CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions)

#### Creating a Permissions Instance

- [init(rawValue: UInt)](/documentation/corebluetooth/cbattributepermissions/init(rawvalue:))

#### Permissions

- [static var readable: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/readable)
- [static var writeable: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/writeable)
- [static var readEncryptionRequired: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/readencryptionrequired)
- [static var writeEncryptionRequired: CBAttributePermissions](/documentation/corebluetooth/cbattributepermissions/writeencryptionrequired)
- [var subscribedCentrals: [CBCentral]?](/documentation/corebluetooth/cbmutablecharacteristic/subscribedcentrals)

#### Related Documentation

- [func updateValue(Data, for: CBMutableCharacteristic, onSubscribedCentrals: [CBCentral]?) -> Bool](/documentation/corebluetooth/cbperipheralmanager/updatevalue(_:for:onsubscribedcentrals:))
- [CBDescriptor](/documentation/corebluetooth/cbdescriptor)

### Identifying a Descriptor

- [var characteristic: CBCharacteristic?](/documentation/corebluetooth/cbdescriptor/characteristic)

### Accessing Descriptor Data

- [var value: Any?](/documentation/corebluetooth/cbdescriptor/value)
- [CBMutableDescriptor](/documentation/corebluetooth/cbmutabledescriptor)

### Creating a Mutable Descriptor

- [init(type: CBUUID, value: Any?)](/documentation/corebluetooth/cbmutabledescriptor/init(type:value:))

## Supporting Types

- [CBManager](/documentation/corebluetooth/cbmanager)

### Accessing the Manager’s Properties

- [var state: CBManagerState](/documentation/corebluetooth/cbmanager/state)
- [CBManagerState](/documentation/corebluetooth/cbmanagerstate)

#### Manager States

- [case poweredOff](/documentation/corebluetooth/cbmanagerstate/poweredoff)
- [case poweredOn](/documentation/corebluetooth/cbmanagerstate/poweredon)
- [case resetting](/documentation/corebluetooth/cbmanagerstate/resetting)
- [case unauthorized](/documentation/corebluetooth/cbmanagerstate/unauthorized)
- [case unknown](/documentation/corebluetooth/cbmanagerstate/unknown)
- [case unsupported](/documentation/corebluetooth/cbmanagerstate/unsupported)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbmanagerstate/init(rawvalue:))

### Determining Authorization State

- [class var authorization: CBManagerAuthorization](/documentation/corebluetooth/cbmanager/authorization-swift.type.property)
- [CBManagerAuthorization](/documentation/corebluetooth/cbmanagerauthorization)

#### Authorization States

- [case allowedAlways](/documentation/corebluetooth/cbmanagerauthorization/allowedalways)
- [case denied](/documentation/corebluetooth/cbmanagerauthorization/denied)
- [case notDetermined](/documentation/corebluetooth/cbmanagerauthorization/notdetermined)
- [case restricted](/documentation/corebluetooth/cbmanagerauthorization/restricted)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbmanagerauthorization/init(rawvalue:))

### Deprecated Properties

- [var authorization: CBManagerAuthorization](/documentation/corebluetooth/cbmanager/authorization-swift.property)
- [CBATTRequest](/documentation/corebluetooth/cbattrequest)

### Requesting to Read and Write Characteristic Values

- [var central: CBCentral](/documentation/corebluetooth/cbattrequest/central)
- [var characteristic: CBCharacteristic](/documentation/corebluetooth/cbattrequest/characteristic)
- [var value: Data?](/documentation/corebluetooth/cbattrequest/value)
- [var offset: Int](/documentation/corebluetooth/cbattrequest/offset)
- [CBPeer](/documentation/corebluetooth/cbpeer)

### Identifying a Peer

- [var identifier: UUID](/documentation/corebluetooth/cbpeer/identifier)
- [CBUUID](/documentation/corebluetooth/cbuuid)

### Creating New CBUUID Objects

- [init(string: String)](/documentation/corebluetooth/cbuuid/init(string:))
- [init(data: Data)](/documentation/corebluetooth/cbuuid/init(data:))
- [init(cfuuid: CFUUID)](/documentation/corebluetooth/cbuuid/init(cfuuid:))
- [init(nsuuid: UUID)](/documentation/corebluetooth/cbuuid/init(nsuuid:))

### Inspecting CBUUID Properties

- [var data: Data](/documentation/corebluetooth/cbuuid/data)
- [var uuidString: String](/documentation/corebluetooth/cbuuid/uuidstring)

### UUID Constants

- [Characteristic Descriptors](/documentation/corebluetooth/characteristic-descriptors)

#### Characteristic Descriptors

- [let CBUUIDCharacteristicExtendedPropertiesString: String](/documentation/corebluetooth/cbuuidcharacteristicextendedpropertiesstring)
- [let CBUUIDCharacteristicUserDescriptionString: String](/documentation/corebluetooth/cbuuidcharacteristicuserdescriptionstring)
- [let CBUUIDClientCharacteristicConfigurationString: String](/documentation/corebluetooth/cbuuidclientcharacteristicconfigurationstring)
- [let CBUUIDServerCharacteristicConfigurationString: String](/documentation/corebluetooth/cbuuidservercharacteristicconfigurationstring)
- [let CBUUIDCharacteristicFormatString: String](/documentation/corebluetooth/cbuuidcharacteristicformatstring)
- [let CBUUIDCharacteristicAggregateFormatString: String](/documentation/corebluetooth/cbuuidcharacteristicaggregateformatstring)
- [let CBUUIDL2CAPPSMCharacteristicString: String](/documentation/corebluetooth/cbuuidl2cappsmcharacteristicstring)

## Bluetooth Classic Support

- [Using Core Bluetooth Classic](/documentation/corebluetooth/using-core-bluetooth-classic)

## Errors

- [CBError](/documentation/corebluetooth/cberror-swift.struct)

### Error Codes

- [static var unknown: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/unknown)
- [static var invalidParameters: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/invalidparameters)
- [static var invalidHandle: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/invalidhandle)
- [static var notConnected: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/notconnected)
- [static var outOfSpace: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/outofspace)
- [static var operationCancelled: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/operationcancelled)
- [static var connectionTimeout: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/connectiontimeout)
- [static var peripheralDisconnected: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/peripheraldisconnected)
- [static var uuidNotAllowed: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/uuidnotallowed)
- [static var alreadyAdvertising: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/alreadyadvertising)
- [static var connectionFailed: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/connectionfailed)
- [static var connectionLimitReached: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/connectionlimitreached)
- [static var operationNotSupported: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/operationnotsupported)
- [static var unknownDevice: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/unknowndevice)
- [static var unkownDevice: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/unkowndevice)

### Type Properties

- [static var encryptionTimedOut: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/encryptiontimedout)
- [static var leGattExceededBackgroundNotificationLimit: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/legattexceededbackgroundnotificationlimit)
- [static var leGattNearBackgroundNotificationLimit: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/legattnearbackgroundnotificationlimit)
- [static var peerRemovedPairingInformation: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/peerremovedpairinginformation)
- [static var tooManyLEPairedDevices: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/toomanylepaireddevices)
- [static var errorDomain: String](/documentation/corebluetooth/cberror-swift.struct/errordomain)

### Enumerations

- [CBError.Code](/documentation/corebluetooth/cberror-swift.struct/code)

#### Error Codes

- [case unknown](/documentation/corebluetooth/cberror-swift.struct/code/unknown)
- [case invalidParameters](/documentation/corebluetooth/cberror-swift.struct/code/invalidparameters)
- [case invalidHandle](/documentation/corebluetooth/cberror-swift.struct/code/invalidhandle)
- [case notConnected](/documentation/corebluetooth/cberror-swift.struct/code/notconnected)
- [case outOfSpace](/documentation/corebluetooth/cberror-swift.struct/code/outofspace)
- [case operationCancelled](/documentation/corebluetooth/cberror-swift.struct/code/operationcancelled)
- [case connectionTimeout](/documentation/corebluetooth/cberror-swift.struct/code/connectiontimeout)
- [case peripheralDisconnected](/documentation/corebluetooth/cberror-swift.struct/code/peripheraldisconnected)
- [case uuidNotAllowed](/documentation/corebluetooth/cberror-swift.struct/code/uuidnotallowed)
- [case alreadyAdvertising](/documentation/corebluetooth/cberror-swift.struct/code/alreadyadvertising)
- [case connectionFailed](/documentation/corebluetooth/cberror-swift.struct/code/connectionfailed)
- [case connectionLimitReached](/documentation/corebluetooth/cberror-swift.struct/code/connectionlimitreached)
- [case operationNotSupported](/documentation/corebluetooth/cberror-swift.struct/code/operationnotsupported)
- [static var unknownDevice: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/code/unknowndevice)
- [case unkownDevice](/documentation/corebluetooth/cberror-swift.struct/code/unkowndevice)

#### Enumeration Cases

- [case encryptionTimedOut](/documentation/corebluetooth/cberror-swift.struct/code/encryptiontimedout)
- [case leGattExceededBackgroundNotificationLimit](/documentation/corebluetooth/cberror-swift.struct/code/legattexceededbackgroundnotificationlimit)
- [case leGattNearBackgroundNotificationLimit](/documentation/corebluetooth/cberror-swift.struct/code/legattnearbackgroundnotificationlimit)
- [case peerRemovedPairingInformation](/documentation/corebluetooth/cberror-swift.struct/code/peerremovedpairinginformation)
- [case tooManyLEPairedDevices](/documentation/corebluetooth/cberror-swift.struct/code/toomanylepaireddevices)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cberror-swift.struct/code/init(rawvalue:))
- [let CBErrorDomain: String](/documentation/corebluetooth/cberrordomain)
- [CBError.Code](/documentation/corebluetooth/cberror-swift.struct/code)

### Error Codes

- [case unknown](/documentation/corebluetooth/cberror-swift.struct/code/unknown)
- [case invalidParameters](/documentation/corebluetooth/cberror-swift.struct/code/invalidparameters)
- [case invalidHandle](/documentation/corebluetooth/cberror-swift.struct/code/invalidhandle)
- [case notConnected](/documentation/corebluetooth/cberror-swift.struct/code/notconnected)
- [case outOfSpace](/documentation/corebluetooth/cberror-swift.struct/code/outofspace)
- [case operationCancelled](/documentation/corebluetooth/cberror-swift.struct/code/operationcancelled)
- [case connectionTimeout](/documentation/corebluetooth/cberror-swift.struct/code/connectiontimeout)
- [case peripheralDisconnected](/documentation/corebluetooth/cberror-swift.struct/code/peripheraldisconnected)
- [case uuidNotAllowed](/documentation/corebluetooth/cberror-swift.struct/code/uuidnotallowed)
- [case alreadyAdvertising](/documentation/corebluetooth/cberror-swift.struct/code/alreadyadvertising)
- [case connectionFailed](/documentation/corebluetooth/cberror-swift.struct/code/connectionfailed)
- [case connectionLimitReached](/documentation/corebluetooth/cberror-swift.struct/code/connectionlimitreached)
- [case operationNotSupported](/documentation/corebluetooth/cberror-swift.struct/code/operationnotsupported)
- [static var unknownDevice: CBError.Code](/documentation/corebluetooth/cberror-swift.struct/code/unknowndevice)
- [case unkownDevice](/documentation/corebluetooth/cberror-swift.struct/code/unkowndevice)

### Enumeration Cases

- [case encryptionTimedOut](/documentation/corebluetooth/cberror-swift.struct/code/encryptiontimedout)
- [case leGattExceededBackgroundNotificationLimit](/documentation/corebluetooth/cberror-swift.struct/code/legattexceededbackgroundnotificationlimit)
- [case leGattNearBackgroundNotificationLimit](/documentation/corebluetooth/cberror-swift.struct/code/legattnearbackgroundnotificationlimit)
- [case peerRemovedPairingInformation](/documentation/corebluetooth/cberror-swift.struct/code/peerremovedpairinginformation)
- [case tooManyLEPairedDevices](/documentation/corebluetooth/cberror-swift.struct/code/toomanylepaireddevices)

### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cberror-swift.struct/code/init(rawvalue:))
- [CBATTError](/documentation/corebluetooth/cbatterror-swift.struct)

### Error Codes

- [static var success: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/success)
- [static var invalidHandle: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidhandle)
- [static var readNotPermitted: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/readnotpermitted)
- [static var writeNotPermitted: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/writenotpermitted)
- [static var invalidPdu: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidpdu)
- [static var insufficientAuthentication: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientauthentication)
- [static var requestNotSupported: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/requestnotsupported)
- [static var invalidOffset: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidoffset)
- [static var insufficientAuthorization: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientauthorization)
- [static var prepareQueueFull: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/preparequeuefull)
- [static var attributeNotFound: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/attributenotfound)
- [static var attributeNotLong: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/attributenotlong)
- [static var insufficientEncryptionKeySize: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientencryptionkeysize)
- [static var invalidAttributeValueLength: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidattributevaluelength)
- [static var unlikelyError: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/unlikelyerror)
- [static var insufficientEncryption: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientencryption)
- [static var unsupportedGroupType: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/unsupportedgrouptype)
- [static var insufficientResources: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientresources)

### Enumerations

- [CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/code)

#### Error Codes

- [case success](/documentation/corebluetooth/cbatterror-swift.struct/code/success)
- [case invalidHandle](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidhandle)
- [case readNotPermitted](/documentation/corebluetooth/cbatterror-swift.struct/code/readnotpermitted)
- [case writeNotPermitted](/documentation/corebluetooth/cbatterror-swift.struct/code/writenotpermitted)
- [case invalidPdu](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidpdu)
- [case insufficientAuthentication](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientauthentication)
- [case requestNotSupported](/documentation/corebluetooth/cbatterror-swift.struct/code/requestnotsupported)
- [case invalidOffset](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidoffset)
- [case insufficientAuthorization](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientauthorization)
- [case prepareQueueFull](/documentation/corebluetooth/cbatterror-swift.struct/code/preparequeuefull)
- [case attributeNotFound](/documentation/corebluetooth/cbatterror-swift.struct/code/attributenotfound)
- [case attributeNotLong](/documentation/corebluetooth/cbatterror-swift.struct/code/attributenotlong)
- [case insufficientEncryptionKeySize](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientencryptionkeysize)
- [case invalidAttributeValueLength](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidattributevaluelength)
- [case unlikelyError](/documentation/corebluetooth/cbatterror-swift.struct/code/unlikelyerror)
- [case insufficientEncryption](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientencryption)
- [case unsupportedGroupType](/documentation/corebluetooth/cbatterror-swift.struct/code/unsupportedgrouptype)
- [case insufficientResources](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientresources)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbatterror-swift.struct/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/corebluetooth/cbatterror-swift.struct/errordomain)
- [let CBATTErrorDomain: String](/documentation/corebluetooth/cbatterrordomain)
- [CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/code)

### Error Codes

- [case success](/documentation/corebluetooth/cbatterror-swift.struct/code/success)
- [case invalidHandle](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidhandle)
- [case readNotPermitted](/documentation/corebluetooth/cbatterror-swift.struct/code/readnotpermitted)
- [case writeNotPermitted](/documentation/corebluetooth/cbatterror-swift.struct/code/writenotpermitted)
- [case invalidPdu](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidpdu)
- [case insufficientAuthentication](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientauthentication)
- [case requestNotSupported](/documentation/corebluetooth/cbatterror-swift.struct/code/requestnotsupported)
- [case invalidOffset](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidoffset)
- [case insufficientAuthorization](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientauthorization)
- [case prepareQueueFull](/documentation/corebluetooth/cbatterror-swift.struct/code/preparequeuefull)
- [case attributeNotFound](/documentation/corebluetooth/cbatterror-swift.struct/code/attributenotfound)
- [case attributeNotLong](/documentation/corebluetooth/cbatterror-swift.struct/code/attributenotlong)
- [case insufficientEncryptionKeySize](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientencryptionkeysize)
- [case invalidAttributeValueLength](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidattributevaluelength)
- [case unlikelyError](/documentation/corebluetooth/cbatterror-swift.struct/code/unlikelyerror)
- [case insufficientEncryption](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientencryption)
- [case unsupportedGroupType](/documentation/corebluetooth/cbatterror-swift.struct/code/unsupportedgrouptype)
- [case insufficientResources](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientresources)

### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbatterror-swift.struct/code/init(rawvalue:))
- [CBATTError](/documentation/corebluetooth/cbatterror-swift.struct)

### Error Codes

- [static var success: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/success)
- [static var invalidHandle: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidhandle)
- [static var readNotPermitted: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/readnotpermitted)
- [static var writeNotPermitted: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/writenotpermitted)
- [static var invalidPdu: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidpdu)
- [static var insufficientAuthentication: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientauthentication)
- [static var requestNotSupported: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/requestnotsupported)
- [static var invalidOffset: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidoffset)
- [static var insufficientAuthorization: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientauthorization)
- [static var prepareQueueFull: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/preparequeuefull)
- [static var attributeNotFound: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/attributenotfound)
- [static var attributeNotLong: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/attributenotlong)
- [static var insufficientEncryptionKeySize: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientencryptionkeysize)
- [static var invalidAttributeValueLength: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/invalidattributevaluelength)
- [static var unlikelyError: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/unlikelyerror)
- [static var insufficientEncryption: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientencryption)
- [static var unsupportedGroupType: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/unsupportedgrouptype)
- [static var insufficientResources: CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/insufficientresources)

### Enumerations

- [CBATTError.Code](/documentation/corebluetooth/cbatterror-swift.struct/code)

#### Error Codes

- [case success](/documentation/corebluetooth/cbatterror-swift.struct/code/success)
- [case invalidHandle](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidhandle)
- [case readNotPermitted](/documentation/corebluetooth/cbatterror-swift.struct/code/readnotpermitted)
- [case writeNotPermitted](/documentation/corebluetooth/cbatterror-swift.struct/code/writenotpermitted)
- [case invalidPdu](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidpdu)
- [case insufficientAuthentication](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientauthentication)
- [case requestNotSupported](/documentation/corebluetooth/cbatterror-swift.struct/code/requestnotsupported)
- [case invalidOffset](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidoffset)
- [case insufficientAuthorization](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientauthorization)
- [case prepareQueueFull](/documentation/corebluetooth/cbatterror-swift.struct/code/preparequeuefull)
- [case attributeNotFound](/documentation/corebluetooth/cbatterror-swift.struct/code/attributenotfound)
- [case attributeNotLong](/documentation/corebluetooth/cbatterror-swift.struct/code/attributenotlong)
- [case insufficientEncryptionKeySize](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientencryptionkeysize)
- [case invalidAttributeValueLength](/documentation/corebluetooth/cbatterror-swift.struct/code/invalidattributevaluelength)
- [case unlikelyError](/documentation/corebluetooth/cbatterror-swift.struct/code/unlikelyerror)
- [case insufficientEncryption](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientencryption)
- [case unsupportedGroupType](/documentation/corebluetooth/cbatterror-swift.struct/code/unsupportedgrouptype)
- [case insufficientResources](/documentation/corebluetooth/cbatterror-swift.struct/code/insufficientresources)

#### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbatterror-swift.struct/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/corebluetooth/cbatterror-swift.struct/errordomain)

## Deprecated

- [CBCentralManagerState](/documentation/corebluetooth/cbcentralmanagerstate)

### Constants

- [case poweredOff](/documentation/corebluetooth/cbcentralmanagerstate/poweredoff)
- [case poweredOn](/documentation/corebluetooth/cbcentralmanagerstate/poweredon)
- [case resetting](/documentation/corebluetooth/cbcentralmanagerstate/resetting)
- [case unauthorized](/documentation/corebluetooth/cbcentralmanagerstate/unauthorized)
- [case unknown](/documentation/corebluetooth/cbcentralmanagerstate/unknown)
- [case unsupported](/documentation/corebluetooth/cbcentralmanagerstate/unsupported)

### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbcentralmanagerstate/init(rawvalue:))
- [CBPeripheralManagerState](/documentation/corebluetooth/cbperipheralmanagerstate)

### Constants

- [case unknown](/documentation/corebluetooth/cbperipheralmanagerstate/unknown)
- [case resetting](/documentation/corebluetooth/cbperipheralmanagerstate/resetting)
- [case unsupported](/documentation/corebluetooth/cbperipheralmanagerstate/unsupported)
- [case unauthorized](/documentation/corebluetooth/cbperipheralmanagerstate/unauthorized)
- [case poweredOff](/documentation/corebluetooth/cbperipheralmanagerstate/poweredoff)
- [case poweredOn](/documentation/corebluetooth/cbperipheralmanagerstate/poweredon)

### Initializers

- [init?(rawValue: Int)](/documentation/corebluetooth/cbperipheralmanagerstate/init(rawvalue:))
- [Deprecated Constants](/documentation/corebluetooth/deprecated-constants)

### Constants

- [let CBCentralManagerOptionDeviceAccessForMedia: String](/documentation/corebluetooth/cbcentralmanageroptiondeviceaccessformedia)
- [let CBUUIDCharacteristicValidRangeString: String](/documentation/corebluetooth/cbuuidcharacteristicvalidrangestring)

## Variables

- [let CBUUIDCharacteristicObservationScheduleString: String](/documentation/corebluetooth/cbuuidcharacteristicobservationschedulestring)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
