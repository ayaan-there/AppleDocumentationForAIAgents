# Playground Bluetooth Documentation

Source: https://sosumi.ai/documentation/playgroundbluetooth

---
title: Playground Bluetooth
source: https://developer.apple.com/documentation/playgroundbluetooth
timestamp: 2026-02-13T19:00:41.730Z
---

## Peripheral Connection

- [Connecting to Bluetooth Peripherals in Swift Playgrounds](/documentation/playgroundbluetooth/connecting_to_bluetooth_peripherals_in_swift_playgrounds)
- [PlaygroundBluetoothCentralManager](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager)

### Configuring Central Managers

- [init(services: [CBUUID]?, queue: DispatchQueue)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029470-init)
- [var delegate: PlaygroundBluetoothCentralManagerDelegate?](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029468-delegate)
- [var scanning: Bool](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029471-scanning)

### Connecting Peripherals

- [func connect(to: CBPeripheral, timeout: TimeInterval?, callback: ((CBPeripheral, Error?) -> Void)?)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029464-connect)
- [func connect(toPeripheralWithUUID: UUID, timeout: TimeInterval, callback: ((CBPeripheral?, Error?) -> Void)?)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029465-connect)
- [func connectToLastConnectedPeripheral(timeout: TimeInterval, callback: ((CBPeripheral?, Error?) -> Void)?) -> Bool](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029466-connecttolastconnectedperipheral)
- [PlaygroundBluetoothCentralManager.ConnectionError](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror)

#### Handling Errors

- [case connectionFailed](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror/connectionfailed)
- [case connectionLost](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror/connectionlost)
- [case excessiveConnections](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror/excessiveconnections)
- [case invalidState](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror/invalidstate)
- [case timeoutExpired](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror/timeoutexpired)

#### Displaying Errors

- [var localizedDescription: String](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror/3029462-localizeddescription)

#### Comparing Errors

- [static func != (PlaygroundBluetoothCentralManager.ConnectionError, PlaygroundBluetoothCentralManager.ConnectionError) -> Bool](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/connectionerror/3029457)

### Disconnecting Peripherals

- [func disconnect(from: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029469-disconnect)

### Inspecting Central Managers

- [var connectedPeripherals: [CBPeripheral]](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029467-connectedperipherals)
- [var state: CBManagerState](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanager/3029472-state)
- [PlaygroundBluetoothCentralManagerDelegate](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanagerdelegate)

### Discovering Peripherals

- [func centralManager(PlaygroundBluetoothCentralManager, didDiscover: CBPeripheral, withAdvertisementData: [String : Any]?, rssi: Double)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanagerdelegate/3029478-centralmanager)
- [func centralManager(PlaygroundBluetoothCentralManager, willConnectTo: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanagerdelegate/3029482-centralmanager)
- [func centralManager(PlaygroundBluetoothCentralManager, didConnectTo: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanagerdelegate/3029474-centralmanager)

### Handling State Changes

- [func centralManagerStateDidChange(PlaygroundBluetoothCentralManager)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanagerdelegate/3029484-centralmanagerstatedidchange)

### Handling Disconnects

- [func centralManager(PlaygroundBluetoothCentralManager, didDisconnectFrom: CBPeripheral, error: Error?)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanagerdelegate/3029476-centralmanager)
- [func centralManager(PlaygroundBluetoothCentralManager, didFailToConnectTo: CBPeripheral, error: Error?)](/documentation/playgroundbluetooth/playgroundbluetoothcentralmanagerdelegate/3029480-centralmanager)

## Peripheral Display

- [PlaygroundBluetoothConnectionView](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview)

### Creating Connection Views

- [init(centralManager: PlaygroundBluetoothCentralManager, delegate: PlaygroundBluetoothConnectionViewDelegate?, dataSource: PlaygroundBluetoothConnectionViewDataSource?)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029511-init)
- [init?(coder: NSCoder)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029512-init)
- [var dataSource: PlaygroundBluetoothConnectionViewDataSource?](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029509-datasource)

### Displaying Peripherals

- [func setItem(PlaygroundBluetoothConnectionView.Item, forPeripheral: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029517-setitem)
- [PlaygroundBluetoothConnectionView.Item](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item)

#### Displaying Peripheral Information

- [init(name: String, icon: UIImage, issueIcon: UIImage, firmwareStatus: PlaygroundBluetoothConnectionView.Item.FirmwareStatus?, batteryLevel: Double?)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/3029497-init)
- [var name: String](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/3029499-name)

#### Displaying Icons

- [var icon: UIImage](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/3029496-icon)
- [var issueIcon: UIImage](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/3029498-issueicon)

#### Displaying Statuses

- [var batteryLevel: Double?](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/3029494-batterylevel)
- [var firmwareStatus: PlaygroundBluetoothConnectionView.Item.FirmwareStatus?](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/3029495-firmwarestatus)
- [PlaygroundBluetoothConnectionView.Item.FirmwareStatus](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/firmwarestatus)

##### Determining Firmware Status

- [case outOfDate](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/firmwarestatus/outofdate)
- [case upToDate](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/firmwarestatus/uptodate)
- [static func != (PlaygroundBluetoothConnectionView.Item.FirmwareStatus, PlaygroundBluetoothConnectionView.Item.FirmwareStatus) -> Bool](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/item/firmwarestatus/3029491)

### Handling State Changes

- [var delegate: PlaygroundBluetoothConnectionViewDelegate?](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029510-delegate)
- [PlaygroundBluetoothConnectionView.State](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/state)

#### Waiting for Connections

- [case connecting](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/state/connecting)
- [case noConnection](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/state/noconnection)
- [case searchingForPeripherals](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/state/searchingforperipherals)

#### Selecting Connections

- [case selectingPeripherals](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/state/selectingperipherals)

#### Handling Old Firmware

- [case connectedPeripheralFirmwareOutOfDate](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/state/connectedperipheralfirmwareoutofdate)

#### Comparing Connection States

- [static func != (PlaygroundBluetoothConnectionView.State, PlaygroundBluetoothConnectionView.State) -> Bool](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/state/3029501)

### Displaying Individual Details

- [func setBatteryLevel(Double?, forPeripheral: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029513-setbatterylevel)
- [func setFirmwareStatus(PlaygroundBluetoothConnectionView.Item.FirmwareStatus?, forPeripheral: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029514-setfirmwarestatus)
- [func setIcon(UIImage, forPeripheral: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029515-seticon)
- [func setIssueIcon(UIImage, forPeripheral: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029516-setissueicon)
- [func setName(String, forPeripheral: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionview/3029518-setname)
- [PlaygroundBluetoothConnectionViewDelegate](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdelegate)

### Displaying New Peripherals

- [func connectionView(PlaygroundBluetoothConnectionView, shouldConnectTo: CBPeripheral, withAdvertisementData: [String : Any]?) -> Bool](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdelegate/3029523-connectionview)
- [func connectionView(PlaygroundBluetoothConnectionView, shouldDisplayDiscovered: CBPeripheral, withAdvertisementData: [String : Any]?, rssi: Double) -> Bool](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdelegate/3029525-connectionview)
- [func connectionView(PlaygroundBluetoothConnectionView, titleFor: PlaygroundBluetoothConnectionView.State) -> String](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdelegate/3029527-connectionview)

### Displaying Firmware Update Information

- [func connectionView(PlaygroundBluetoothConnectionView, firmwareUpdateInstructionsFor: CBPeripheral) -> String](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdelegate/3029522-connectionview)

### Disconnecting from Peripherals

- [func connectionView(PlaygroundBluetoothConnectionView, willDisconnectFrom: CBPeripheral)](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdelegate/3029528-connectionview)
- [PlaygroundBluetoothConnectionViewDataSource](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdatasource)

### Displaying Connection View Items

- [func connectionView(PlaygroundBluetoothConnectionView, itemForPeripheral: CBPeripheral, withAdvertisementData: [String : Any]?) -> PlaygroundBluetoothConnectionView.Item](/documentation/playgroundbluetooth/playgroundbluetoothconnectionviewdatasource/3029520-connectionview)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
