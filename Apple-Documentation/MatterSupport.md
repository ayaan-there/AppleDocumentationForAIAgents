# MatterSupport Documentation

Source: https://sosumi.ai/documentation/mattersupport

---
title: MatterSupport
source: https://developer.apple.com/documentation/mattersupport
timestamp: 2026-02-13T18:59:18.850Z
---

## Adding a device

- [Adding Matter support to your ecosystem](/documentation/mattersupport/adding-matter-support-to-your-ecosystem)
- [MatterAddDeviceRequest](/documentation/mattersupport/matteradddevicerequest)

### Creating the request

- [init(from: any Decoder) throws](/documentation/mattersupport/matteradddevicerequest/init(from:))
- [init(topology: MatterAddDeviceRequest.Topology, setupPayload: MTRSetupPayload?, showing: MatterAddDeviceRequest.DeviceCriteria)](/documentation/mattersupport/matteradddevicerequest/init(topology:setuppayload:showing:))
- [init(topology: MatterAddDeviceRequest.Topology, setupPayload: MTRSetupPayload?, showing: MatterAddDeviceRequest.DeviceCriteria, shouldScanNetworks: Bool)](/documentation/mattersupport/matteradddevicerequest/init(topology:setuppayload:showing:shouldscannetworks:))

### Setting up the request

- [MatterAddDeviceRequest.Home](/documentation/mattersupport/matteradddevicerequest/home)

#### Creating the home

- [init(from: any Decoder) throws](/documentation/mattersupport/matteradddevicerequest/init(from:))
- [init(displayName: String)](/documentation/mattersupport/matteradddevicerequest/home/init(displayname:))

#### Getting the properties

- [var displayName: String](/documentation/mattersupport/matteradddevicerequest/home/displayname)
- [MatterAddDeviceRequest.Room](/documentation/mattersupport/matteradddevicerequest/room)

#### Creating the room

- [init(from: any Decoder) throws](/documentation/mattersupport/matteradddevicerequest/init(from:))
- [init(displayName: String)](/documentation/mattersupport/matteradddevicerequest/room/init(displayname:))

#### Getting the properties

- [var displayName: String](/documentation/mattersupport/matteradddevicerequest/room/displayname)
- [MatterAddDeviceRequest.Topology](/documentation/mattersupport/matteradddevicerequest/topology-swift.struct)

#### Creating the topology

- [init(from: any Decoder) throws](/documentation/mattersupport/matteradddevicerequest/init(from:))
- [init(ecosystemName: String, homes: [MatterAddDeviceRequest.Home])](/documentation/mattersupport/matteradddevicerequest/topology-swift.struct/init(ecosystemname:homes:))

#### Getting the properties

- [var ecosystemName: String](/documentation/mattersupport/matteradddevicerequest/topology-swift.struct/ecosystemname)
- [var homes: [MatterAddDeviceRequest.Home]](/documentation/mattersupport/matteradddevicerequest/topology-swift.struct/homes)
- [var setupPayload: MTRSetupPayload?](/documentation/mattersupport/matteradddevicerequest/setuppayload)
- [var topology: MatterAddDeviceRequest.Topology](/documentation/mattersupport/matteradddevicerequest/topology-swift.property)

### Defining the device criteria

- [MatterAddDeviceRequest.DeviceCriteria](/documentation/mattersupport/matteradddevicerequest/devicecriteria)

#### Creating criteria

- [init(from: any Decoder) throws](/documentation/mattersupport/matteradddevicerequest/init(from:))

#### Defining the criteria

- [case allDevices](/documentation/mattersupport/matteradddevicerequest/devicecriteria/alldevices)
- [case all([MatterAddDeviceRequest.DeviceCriteria])](/documentation/mattersupport/matteradddevicerequest/devicecriteria/all(_:))
- [case any([MatterAddDeviceRequest.DeviceCriteria])](/documentation/mattersupport/matteradddevicerequest/devicecriteria/any(_:))
- [case commissioningID(UUID)](/documentation/mattersupport/matteradddevicerequest/devicecriteria/commissioningid(_:))
- [case fabricNode(rootPublicKey: Data, nodeID: UInt64)](/documentation/mattersupport/matteradddevicerequest/devicecriteria/fabricnode(rootpublickey:nodeid:))
- [case not(MatterAddDeviceRequest.DeviceCriteria)](/documentation/mattersupport/matteradddevicerequest/devicecriteria/not(_:))
- [case productID(Int)](/documentation/mattersupport/matteradddevicerequest/devicecriteria/productid(_:))
- [case serialNumber(String)](/documentation/mattersupport/matteradddevicerequest/devicecriteria/serialnumber(_:))
- [case vendorID(Int)](/documentation/mattersupport/matteradddevicerequest/devicecriteria/vendorid(_:))
- [var showDeviceCriteria: MatterAddDeviceRequest.DeviceCriteria](/documentation/mattersupport/matteradddevicerequest/showdevicecriteria)

### Performing the request

- [var shouldScanNetworks: Bool](/documentation/mattersupport/matteradddevicerequest/shouldscannetworks)
- [func perform() async throws](/documentation/mattersupport/matteradddevicerequest/perform())

### Type Properties

- [static var isSupported: Bool](/documentation/mattersupport/matteradddevicerequest/issupported)

### Default Implementations

- [Decodable Implementations](/documentation/mattersupport/matteradddevicerequest/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/mattersupport/matteradddevicerequest/init(from:))
- [MatterAddDeviceExtensionRequestHandler](/documentation/mattersupport/matteradddeviceextensionrequesthandler)

### Creating the request handler

- [init()](/documentation/mattersupport/matteradddeviceextensionrequesthandler/init())

### Configuring and validating the device

- [func configureDevice(named: String, in: MatterAddDeviceRequest.Room?) async](/documentation/mattersupport/matteradddeviceextensionrequesthandler/configuredevice(named:in:))
- [func validateDeviceCredential(MatterAddDeviceExtensionRequestHandler.DeviceCredential) async throws](/documentation/mattersupport/matteradddeviceextensionrequesthandler/validatedevicecredential(_:))
- [MatterAddDeviceExtensionRequestHandler.DeviceCredential](/documentation/mattersupport/matteradddeviceextensionrequesthandler/devicecredential)

#### Creating the credential

- [init(certificationDeclaration: Data, deviceAttestationCertificate: Data, productAttestationIntermediateCertificate: Data)](/documentation/mattersupport/matteradddeviceextensionrequesthandler/devicecredential/init(certificationdeclaration:deviceattestationcertificate:productattestationintermediatecertificate:))

#### Getting the properties

- [var certificationDeclaration: Data](/documentation/mattersupport/matteradddeviceextensionrequesthandler/devicecredential/certificationdeclaration)
- [var deviceAttestationCertificate: Data](/documentation/mattersupport/matteradddeviceextensionrequesthandler/devicecredential/deviceattestationcertificate)
- [var productAttestationIntermediateCertificate: Data](/documentation/mattersupport/matteradddeviceextensionrequesthandler/devicecredential/productattestationintermediatecertificate)
- [func rooms(in: MatterAddDeviceRequest.Home?) async -> [MatterAddDeviceRequest.Room]](/documentation/mattersupport/matteradddeviceextensionrequesthandler/rooms(in:))

### Commissioning the device

- [func commissionDevice(in: MatterAddDeviceRequest.Home?, onboardingPayload: String, commissioningID: UUID) async throws](/documentation/mattersupport/matteradddeviceextensionrequesthandler/commissiondevice(in:onboardingpayload:commissioningid:))

### Selecting the Thread network

- [func selectThreadNetwork(from: [MatterAddDeviceExtensionRequestHandler.ThreadScanResult]) async throws -> MatterAddDeviceExtensionRequestHandler.ThreadNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/selectthreadnetwork(from:))
- [MatterAddDeviceExtensionRequestHandler.ThreadScanResult](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult)

#### Creating the result

- [init(networkName: String, panID: UInt16, extendedPANID: UInt64, channel: UInt16, extendedAddress: Data, rssi: Int8, version: UInt8, linkQualityIndicator: UInt8)](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/init(networkname:panid:extendedpanid:channel:extendedaddress:rssi:version:linkqualityindicator:))

#### Getting result information

- [var channel: UInt16](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/channel)
- [var extendedAddress: Data](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/extendedaddress)
- [var extendedPANID: UInt64](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/extendedpanid)
- [var linkQualityIndicator: UInt8](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/linkqualityindicator)
- [var networkName: String](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/networkname)
- [var panID: UInt16](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/panid)
- [var rssi: Int8](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/rssi)
- [var version: UInt8](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadscanresult/version)
- [MatterAddDeviceExtensionRequestHandler.ThreadNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadnetworkassociation)

#### Getting network information

- [static var defaultSystemNetwork: MatterAddDeviceExtensionRequestHandler.ThreadNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadnetworkassociation/defaultsystemnetwork)
- [static func network(extendedPANID: UInt64) -> MatterAddDeviceExtensionRequestHandler.ThreadNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/threadnetworkassociation/network(extendedpanid:))

### Selecting the Wi-Fi network

- [func selectWiFiNetwork(from: [MatterAddDeviceExtensionRequestHandler.WiFiScanResult]) async throws -> MatterAddDeviceExtensionRequestHandler.WiFiNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/selectwifinetwork(from:))
- [MatterAddDeviceExtensionRequestHandler.WiFiScanResult](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifiscanresult)

#### Creating the result

- [init(ssid: Data, rssi: Int8, security: MTRNetworkCommissioningWiFiSecurity, band: MTRNetworkCommissioningWiFiBand)](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifiscanresult/init(ssid:rssi:security:band:))

#### Getting result information

- [var band: MTRNetworkCommissioningWiFiBand](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifiscanresult/band)
- [var rssi: Int8](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifiscanresult/rssi)
- [var security: MTRNetworkCommissioningWiFiSecurity](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifiscanresult/security)
- [var ssid: Data](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifiscanresult/ssid)
- [MatterAddDeviceExtensionRequestHandler.WiFiNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifinetworkassociation)

#### Getting network information

- [static var defaultSystemNetwork: MatterAddDeviceExtensionRequestHandler.WiFiNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifinetworkassociation/defaultsystemnetwork)
- [static func network(ssid: Data, credentials: Data) -> MatterAddDeviceExtensionRequestHandler.WiFiNetworkAssociation](/documentation/mattersupport/matteradddeviceextensionrequesthandler/wifinetworkassociation/network(ssid:credentials:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
