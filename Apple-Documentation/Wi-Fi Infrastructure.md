# Wi-Fi Infrastructure Documentation

Source: https://sosumi.ai/documentation/wifiinfrastructure

---
title: Wi-Fi Infrastructure
source: https://developer.apple.com/documentation/wifiinfrastructure
timestamp: 2026-02-13T19:04:14.533Z
---

## Essentials

- [com.apple.developer.wifi-infrastructure](/documentation/bundleresources/entitlements/com.apple.developer.wifi-infrastructure)
- [Sharing Wi-Fi network credentials](/documentation/wifiinfrastructure/sharing-wi-fi-network-credentials)

## Network sharing

- [WINetworkSharingController](/documentation/wifiinfrastructure/winetworksharingcontroller)

### Getting the controlled accessory

- [let accessory: ASAccessory](/documentation/wifiinfrastructure/winetworksharingcontroller/accessory)

### Authorizing an accessory for network sharing

- [func requestAuthorization() async throws -> WINetworkSharingController.AuthorizationState](/documentation/wifiinfrastructure/winetworksharingcontroller/requestauthorization())
- [WINetworkSharingController.AuthorizationState](/documentation/wifiinfrastructure/winetworksharingcontroller/authorizationstate)

#### Checking authorization state

- [case undetermined](/documentation/wifiinfrastructure/winetworksharingcontroller/authorizationstate/undetermined)
- [case denied](/documentation/wifiinfrastructure/winetworksharingcontroller/authorizationstate/denied)
- [case askToShare](/documentation/wifiinfrastructure/winetworksharingcontroller/authorizationstate/asktoshare)
- [case automatic](/documentation/wifiinfrastructure/winetworksharingcontroller/authorizationstate/automatic)

### Signaling your App Extension to ask for a network

- [func askToShare() async throws -> WINetworkSharingAskToShareState](/documentation/wifiinfrastructure/winetworksharingcontroller/asktoshare())

### Initializers

- [init(for: ASAccessory) async throws](/documentation/wifiinfrastructure/winetworksharingcontroller/init(for:))
- [WINetworkSharingProvider](/documentation/wifiinfrastructure/winetworksharingprovider)

### Getting accessory data

- [let accessory: ASAccessory](/documentation/wifiinfrastructure/winetworksharingprovider/accessory)

### Getting network updates

- [func networkEvents(matching: Predicate<WINetworkSharingProvider.Network>?) -> some Sendable & AsyncSequence<WINetworkSharingProvider.NetworkEvent, any Error>
](/documentation/wifiinfrastructure/winetworksharingprovider/networkevents(matching:))
- [WINetworkSharingProvider.NetworkEvent](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent)

#### Identifying an event

- [WINetworkSharingProvider.NetworkEvent.ID](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/id-swift.typealias)
- [var id: WINetworkSharingProvider.NetworkEvent.ID](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/id-swift.property)

#### Getting network data

- [let networks: [WINetworkSharingProvider.Network]](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/networks)
- [let networksUpdateCounter: UInt64](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/networksupdatecounter)

#### Getting event signals

- [let newShareableNetworkAvailable: Bool](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/newshareablenetworkavailable)
- [let appRequestedSharing: Bool](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/apprequestedsharing)

#### Getting the event time

- [let timestamp: Date](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/timestamp)

#### Getting the event description

- [var description: String](/documentation/wifiinfrastructure/winetworksharingprovider/networkevent/description)
- [WINetworkSharingProvider.Network](/documentation/wifiinfrastructure/winetworksharingprovider/network)

#### Identifying a network

- [var id: WINetworkSharingProvider.Network.ID](/documentation/wifiinfrastructure/winetworksharingprovider/network/id-swift.property)
- [WINetworkSharingProvider.Network.ID](/documentation/wifiinfrastructure/winetworksharingprovider/network/id-swift.struct)

#### Getting the network SSID

- [let ssid: WISSID](/documentation/wifiinfrastructure/winetworksharingprovider/network/ssid)
- [let isSSIDBroadcast: Bool](/documentation/wifiinfrastructure/winetworksharingprovider/network/isssidbroadcast)

#### Getting the network credentials

- [let securityPolicy: Set<WINetworkSharingProvider.Network.SecurityPolicy>](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.property)
- [WINetworkSharingProvider.Network.SecurityPolicy](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.enum)

##### Enumeration Cases

- [case open](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.enum/open)
- [case owe](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.enum/owe)
- [case wep](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.enum/wep)
- [case wpa](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.enum/wpa)
- [case wpa2](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.enum/wpa2)
- [case wpa3](/documentation/wifiinfrastructure/winetworksharingprovider/network/securitypolicy-swift.enum/wpa3)
- [let credentials: WINetworkSharingProvider.Network.Credentials](/documentation/wifiinfrastructure/winetworksharingprovider/network/credentials-swift.property)
- [WINetworkSharingProvider.Network.Credentials](/documentation/wifiinfrastructure/winetworksharingprovider/network/credentials-swift.enum)

##### Enumeration Cases

- [case none](/documentation/wifiinfrastructure/winetworksharingprovider/network/credentials-swift.enum/none)
- [case password(String)](/documentation/wifiinfrastructure/winetworksharingprovider/network/credentials-swift.enum/password(_:))

##### Instance Properties

- [var description: String](/documentation/wifiinfrastructure/winetworksharingprovider/network/credentials-swift.enum/description)
- [let captivePortalLogin: WINetworkSharingProvider.Network.CaptivePortalLogin?](/documentation/wifiinfrastructure/winetworksharingprovider/network/captiveportallogin-swift.property)
- [WINetworkSharingProvider.Network.CaptivePortalLogin](/documentation/wifiinfrastructure/winetworksharingprovider/network/captiveportallogin-swift.struct)

##### Instance Properties

- [var description: String](/documentation/wifiinfrastructure/winetworksharingprovider/network/captiveportallogin-swift.struct/description)
- [let userEnteredFormValues: [String : String]](/documentation/wifiinfrastructure/winetworksharingprovider/network/captiveportallogin-swift.struct/userenteredformvalues)

#### Getting the date

- [let lastModified: Date](/documentation/wifiinfrastructure/winetworksharingprovider/network/lastmodified)
- [let firstShared: Date](/documentation/wifiinfrastructure/winetworksharingprovider/network/firstshared)

#### Getting a network description

- [var description: String](/documentation/wifiinfrastructure/winetworksharingprovider/network/description)

### Displaying network selection

- [func presentAskToShareUI(scanProvider: ((ASAccessory, WINetworkSharingProvider.AccessoryScanRequest) async -> WINetworkSharingProvider.AccessoryScanResponse?)?) async throws -> WINetworkSharingAskToShareState](/documentation/wifiinfrastructure/winetworksharingprovider/presentasktoshareui(scanprovider:))
- [WINetworkSharingProvider.AccessoryScanRequest](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanrequest)

#### Identifying a scan request

- [WINetworkSharingProvider.AccessoryScanRequest.ID](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanrequest/id-swift.typealias)
- [var id: WINetworkSharingProvider.AccessoryScanRequest.ID](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanrequest/id-swift.property)
- [WINetworkSharingProvider.AccessoryScanResponse](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresponse)

#### Identifying a scan response

- [WINetworkSharingProvider.AccessoryScanResponse.ID](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresponse/id-swift.typealias)
- [var id: WINetworkSharingProvider.AccessoryScanResponse.ID](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresponse/id-swift.property)

#### Getting the originating scan request

- [let scanRequest: WINetworkSharingProvider.AccessoryScanRequest](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresponse/scanrequest)

#### Getting the scan results from the Accessory

- [let results: [WINetworkSharingProvider.AccessoryScanResult]](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresponse/results)

#### Initializers

- [init(scanRequest: WINetworkSharingProvider.AccessoryScanRequest, results: [WINetworkSharingProvider.AccessoryScanResult])](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresponse/init(scanrequest:results:))
- [WINetworkSharingProvider.AccessoryScanResult](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresult)

#### Getting network definitions

- [let ssid: WISSID?](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresult/ssid)

#### Getting network performance indicators

- [let signalStrength: Double](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresult/signalstrength)

#### Getting network connection state

- [let isConnected: Bool](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresult/isconnected)

#### Initializers

- [init(ssid: WISSID?, signalStrength: Double, isConnected: Bool)](/documentation/wifiinfrastructure/winetworksharingprovider/accessoryscanresult/init(ssid:signalstrength:isconnected:))

### Initializers

- [init(for: ASAccessory) async throws](/documentation/wifiinfrastructure/winetworksharingprovider/init(for:))
- [WINetworkSharingAskToShareState](/documentation/wifiinfrastructure/winetworksharingasktosharestate)

### Checking authorization state

- [case undetermined](/documentation/wifiinfrastructure/winetworksharingasktosharestate/undetermined)
- [case denied](/documentation/wifiinfrastructure/winetworksharingasktosharestate/denied)
- [case approved](/documentation/wifiinfrastructure/winetworksharingasktosharestate/approved)

## Common data

- [WISSID](/documentation/wifiinfrastructure/wissid)

### Working with SSIDs as a string

- [init?(String, encoding: String.Encoding)](/documentation/wifiinfrastructure/wissid/init(_:encoding:))
- [func stringRepresentation(encoding: String.Encoding) -> String?](/documentation/wifiinfrastructure/wissid/stringrepresentation(encoding:))

### Working with raw SSID data

- [init?(Data)](/documentation/wifiinfrastructure/wissid/init(_:))
- [let data: Data](/documentation/wifiinfrastructure/wissid/data)

### Getting a description

- [var description: String](/documentation/wifiinfrastructure/wissid/description)

## Errors

- [WINetworkSharingError](/documentation/wifiinfrastructure/winetworksharingerror)

### Checking for general errors

- [case error](/documentation/wifiinfrastructure/winetworksharingerror/error)

### Checking for timeouts

- [case timeout](/documentation/wifiinfrastructure/winetworksharingerror/timeout)

### Checking for app issues

- [case appNotPermitted](/documentation/wifiinfrastructure/winetworksharingerror/appnotpermitted)
- [case appNotInForeground](/documentation/wifiinfrastructure/winetworksharingerror/appnotinforeground)

### Checking for unsupported host capabilities

- [case wifiNetworkSharingUnsupported](/documentation/wifiinfrastructure/winetworksharingerror/wifinetworksharingunsupported)

### Checking for communication failures

- [case communicationFailure](/documentation/wifiinfrastructure/winetworksharingerror/communicationfailure)

### Checking for no available networks

- [case noAvailableNetworks](/documentation/wifiinfrastructure/winetworksharingerror/noavailablenetworks)

### Checking for excessive requests

- [case tooManyRequests](/documentation/wifiinfrastructure/winetworksharingerror/toomanyrequests)

### Checking for accessory issues

- [case accessoryNotConfigured](/documentation/wifiinfrastructure/winetworksharingerror/accessorynotconfigured)
- [case accessoryNotAuthorized](/documentation/wifiinfrastructure/winetworksharingerror/accessorynotauthorized)
- [case accessoryNotConnected](/documentation/wifiinfrastructure/winetworksharingerror/accessorynotconnected)
- [case noAccessoryScanResponse](/documentation/wifiinfrastructure/winetworksharingerror/noaccessoryscanresponse)
- [case accessoryTransportNotSecured](/documentation/wifiinfrastructure/winetworksharingerror/accessorytransportnotsecured)
- [case noMatchingAccessoryScanRequest](/documentation/wifiinfrastructure/winetworksharingerror/nomatchingaccessoryscanrequest)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
