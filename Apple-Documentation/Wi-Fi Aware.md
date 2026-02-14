# Wi-Fi Aware Documentation

Source: https://sosumi.ai/documentation/wifiaware

---
title: Wi-Fi Aware
source: https://developer.apple.com/documentation/wifiaware
timestamp: 2026-02-13T19:04:12.486Z
---

## Essentials

- [Building peer-to-peer apps](/documentation/wifiaware/building-peer-to-peer-apps)
- [Connecting devices for peer-to-peer Wi-Fi](/documentation/wifiaware/connecting-paired-devices)
- [Adopting Wi-Fi Aware](/documentation/wifiaware/adopting-wi-fi-aware)
- [com.apple.developer.wifi-aware](/documentation/bundleresources/entitlements/com.apple.developer.wifi-aware)
- [WiFiAwareServices](/documentation/bundleresources/information-property-list/wifiawareservices)

## Host capabilities

- [WACapabilities](/documentation/wifiaware/wacapabilities)

### Checking features supported by host device

- [WACapabilities.Feature](/documentation/wifiaware/wacapabilities/feature)

#### Checking for Wi-Fi Aware support

- [case wifiAware](/documentation/wifiaware/wacapabilities/feature/wifiaware)
- [static var supportedFeatures: Set<WACapabilities.Feature>](/documentation/wifiaware/wacapabilities/supportedfeatures)

### Checking for the maximum devices and services

- [static var maximumConnectableDevices: Int](/documentation/wifiaware/wacapabilities/maximumconnectabledevices)
- [static var maximumPublishableServices: Int](/documentation/wifiaware/wacapabilities/maximumpublishableservices)
- [static var maximumSubscribableServices: Int](/documentation/wifiaware/wacapabilities/maximumsubscribableservices)
- [WACapabilities.Feature](/documentation/wifiaware/wacapabilities/feature)

### Checking for Wi-Fi Aware support

- [case wifiAware](/documentation/wifiaware/wacapabilities/feature/wifiaware)

## Services to discover

- [WAService](/documentation/wifiaware/waservice)

### Selecting from your app’s services

- [static var allServices: [String : Self]](/documentation/wifiaware/waservice/allservices)

### Checking a service name

- [var name: String](/documentation/wifiaware/waservice/name)
- [WASubscribableService](/documentation/wifiaware/wasubscribableservice)

### Selecting from your app’s subscribable services

- [static var allServices: [WASubscribableService.ID : WASubscribableService]](/documentation/wifiaware/wasubscribableservice/allservices)

### Checking a service name and ID

- [WASubscribableService.ID](/documentation/wifiaware/wasubscribableservice/id-swift.typealias)
- [var id: WASubscribableService.ID](/documentation/wifiaware/wasubscribableservice/id-swift.property)
- [let name: String](/documentation/wifiaware/wasubscribableservice/name)

### Getting a String description

- [var description: String](/documentation/wifiaware/wasubscribableservice/description)
- [WAPublishableService](/documentation/wifiaware/wapublishableservice)

### Selecting from your app’s publishable services

- [static var allServices: [WAPublishableService.ID : WAPublishableService]](/documentation/wifiaware/wapublishableservice/allservices)

### Checking a service name and ID

- [WAPublishableService.ID](/documentation/wifiaware/wapublishableservice/id-swift.typealias)
- [var id: WAPublishableService.ID](/documentation/wifiaware/wapublishableservice/id-swift.property)
- [let name: String](/documentation/wifiaware/wapublishableservice/name)

### Getting a string description

- [var description: String](/documentation/wifiaware/wapublishableservice/description)

## Paired devices

- [WAPairedDevice](/documentation/wifiaware/wapaireddevice)

### Selecting from your app’s paired devices

- [WAPairedDevice.Devices](/documentation/wifiaware/wapaireddevice/devices)
- [static var allDevices: WAPairedDevice.DevicesSequence](/documentation/wifiaware/wapaireddevice/alldevices)
- [static func allDevices(matching: Predicate<WAPairedDevice>) -> WAPairedDevice.DevicesSequence](/documentation/wifiaware/wapaireddevice/alldevices(matching:))
- [WAPairedDevice.DevicesSequence](/documentation/wifiaware/wapaireddevice/devicessequence)

#### Getting an initial snapshot

- [func current() async throws -> WAPairedDevice.DevicesSequence.Element?](/documentation/wifiaware/wapaireddevice/devicessequence/current())

#### Getting async updates

- [WAPairedDevice.DevicesSequence.AsyncIterator](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator)

##### Getting the next asynchronous update

- [WAPairedDevice.DevicesSequence.AsyncIterator.Element](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator/element)
- [func next() async throws -> WAPairedDevice.DevicesSequence.AsyncIterator.Element?](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator/next())

##### Throwing an error

- [WAPairedDevice.DevicesSequence.AsyncIterator.Failure](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator/failure)
- [func makeAsyncIterator() -> WAPairedDevice.DevicesSequence.AsyncIterator](/documentation/wifiaware/wapaireddevice/devicessequence/makeasynciterator())
- [WAPairedDevice.DevicesSequence.Element](/documentation/wifiaware/wapaireddevice/devicessequence/element)

### Getting the app-specific identifier

- [WAPairedDevice.ID](/documentation/wifiaware/wapaireddevice/id-swift.typealias)
- [let id: WAPairedDevice.ID](/documentation/wifiaware/wapaireddevice/id-swift.property)

### Getting the configured device name

- [let name: String?](/documentation/wifiaware/wapaireddevice/name)

### Getting pairing-related device data

- [let pairingInfo: WAPairedDevice.PairingInfo?](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.property)
- [WAPairedDevice.PairingInfo](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct)

#### Receiving device information

- [let vendorName: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/vendorname)
- [let modelName: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/modelname)
- [let pairingName: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/pairingname)

#### Getting a string description

- [var description: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/description)

### Getting a string description

- [var description: String](/documentation/wifiaware/wapaireddevice/description)
- [WAPairedDevice.Devices](/documentation/wifiaware/wapaireddevice/devices)
- [WAPairedDevice.DevicesSequence](/documentation/wifiaware/wapaireddevice/devicessequence)

### Getting an initial snapshot

- [func current() async throws -> WAPairedDevice.DevicesSequence.Element?](/documentation/wifiaware/wapaireddevice/devicessequence/current())

### Getting async updates

- [WAPairedDevice.DevicesSequence.AsyncIterator](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator)

#### Getting the next asynchronous update

- [WAPairedDevice.DevicesSequence.AsyncIterator.Element](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator/element)
- [func next() async throws -> WAPairedDevice.DevicesSequence.AsyncIterator.Element?](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator/next())

#### Throwing an error

- [WAPairedDevice.DevicesSequence.AsyncIterator.Failure](/documentation/wifiaware/wapaireddevice/devicessequence/asynciterator/failure)
- [func makeAsyncIterator() -> WAPairedDevice.DevicesSequence.AsyncIterator](/documentation/wifiaware/wapaireddevice/devicessequence/makeasynciterator())
- [WAPairedDevice.DevicesSequence.Element](/documentation/wifiaware/wapaireddevice/devicessequence/element)
- [WAPairedDevice.PairingInfo](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct)

### Receiving device information

- [let vendorName: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/vendorname)
- [let modelName: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/modelname)
- [let pairingName: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/pairingname)

### Getting a string description

- [var description: String](/documentation/wifiaware/wapaireddevice/pairinginfo-swift.struct/description)

## Subscriber

- [WASubscriberBrowser](/documentation/wifiaware/wasubscriberbrowser)

### Configuring a browser

- [WASubscriberBrowser.Action](/documentation/wifiaware/wasubscriberbrowser/action)

#### Creating a browser

- [static func connecting(to: WASubscriberBrowser.Devices, from: WASubscribableService) -> WASubscriberBrowser.Action](/documentation/wifiaware/wasubscriberbrowser/action/connecting(to:from:))
- [WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices)

#### Selecting devices to connect to

- [static func selected(WAPairedDevice.Devices) -> WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/selected(_:)-8myz8)
- [static func selected(some Sequence<WAPairedDevice>) -> WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/selected(_:)-5arv0)
- [static let userSpecifiedDevices: WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/userspecifieddevices)

#### Using a live matching filter

- [static func matching(Predicate<WAPairedDevice>) -> WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/matching(_:))

#### Connecting to all paired devices

- [static let allPairedDevices: WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/allpaireddevices)

### Processing Wi-Fi Aware subscribe results

- [WASubscriberBrowser.Endpoint](/documentation/wifiaware/wasubscriberbrowser/endpoint)

### Creating browser implementation details

- [func makeDescriptor() -> NWBrowser.Descriptor](/documentation/wifiaware/wasubscriberbrowser/makedescriptor())
- [func configureParameters(NWParameters?) -> NWParameters](/documentation/wifiaware/wasubscriberbrowser/configureparameters(_:))
- [func makeEndpoint(from: NWBrowser.Result) throws -> WASubscriberBrowser.Endpoint?](/documentation/wifiaware/wasubscriberbrowser/makeendpoint(from:))
- [WASubscriberBrowser.Action](/documentation/wifiaware/wasubscriberbrowser/action)

### Creating a browser

- [static func connecting(to: WASubscriberBrowser.Devices, from: WASubscribableService) -> WASubscriberBrowser.Action](/documentation/wifiaware/wasubscriberbrowser/action/connecting(to:from:))
- [WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices)

### Selecting devices to connect to

- [static func selected(WAPairedDevice.Devices) -> WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/selected(_:)-8myz8)
- [static func selected(some Sequence<WAPairedDevice>) -> WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/selected(_:)-5arv0)
- [static let userSpecifiedDevices: WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/userspecifieddevices)

### Using a live matching filter

- [static func matching(Predicate<WAPairedDevice>) -> WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/matching(_:))

### Connecting to all paired devices

- [static let allPairedDevices: WASubscriberBrowser.Devices](/documentation/wifiaware/wasubscriberbrowser/devices/allpaireddevices)

## Publisher

- [WAPublisherListener](/documentation/wifiaware/wapublisherlistener)

### Configuring a listener

- [WAPublisherListener.Action](/documentation/wifiaware/wapublisherlistener/action)

#### Creating a listener

- [static func connecting(to: WAPublishableService, from: WAPublisherListener.Devices, datapath: WAPublisherListener.DatapathParameters?) -> WAPublisherListener.Action](/documentation/wifiaware/wapublisherlistener/action/connecting(to:from:datapath:))
- [WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices)

#### Selecting specific devices

- [static func selected(WAPairedDevice.Devices) -> WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/selected(_:)-56vig)
- [static func selected(some Sequence<WAPairedDevice>) -> WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/selected(_:)-1e2)
- [static let userSpecifiedDevices: WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/userspecifieddevices)

#### Using a live matching filter

- [static func matching(Predicate<WAPairedDevice>) -> WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/matching(_:))

#### Allowing your paired devices to connect

- [static let allPairedDevices: WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/allpaireddevices)
- [WAPublisherListener.DatapathParameters](/documentation/wifiaware/wapublisherlistener/datapathparameters)

#### Setting performance modes

- [static let defaults: WAPublisherListener.DatapathParameters](/documentation/wifiaware/wapublisherlistener/datapathparameters/defaults)
- [static let realtime: WAPublisherListener.DatapathParameters](/documentation/wifiaware/wapublisherlistener/datapathparameters/realtime)

### Creating publisher implementation details

- [func configureParameters(NWParameters)](/documentation/wifiaware/wapublisherlistener/configureparameters(_:))
- [var service: NWListener.Service](/documentation/wifiaware/wapublisherlistener/service)
- [var isApplicationService: Bool](/documentation/wifiaware/wapublisherlistener/isapplicationservice)
- [WAPublisherListener.Action](/documentation/wifiaware/wapublisherlistener/action)

### Creating a listener

- [static func connecting(to: WAPublishableService, from: WAPublisherListener.Devices, datapath: WAPublisherListener.DatapathParameters?) -> WAPublisherListener.Action](/documentation/wifiaware/wapublisherlistener/action/connecting(to:from:datapath:))
- [WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices)

### Selecting specific devices

- [static func selected(WAPairedDevice.Devices) -> WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/selected(_:)-56vig)
- [static func selected(some Sequence<WAPairedDevice>) -> WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/selected(_:)-1e2)
- [static let userSpecifiedDevices: WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/userspecifieddevices)

### Using a live matching filter

- [static func matching(Predicate<WAPairedDevice>) -> WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/matching(_:))

### Allowing your paired devices to connect

- [static let allPairedDevices: WAPublisherListener.Devices](/documentation/wifiaware/wapublisherlistener/devices/allpaireddevices)
- [WAPublisherListener.DatapathParameters](/documentation/wifiaware/wapublisherlistener/datapathparameters)

### Setting performance modes

- [static let defaults: WAPublisherListener.DatapathParameters](/documentation/wifiaware/wapublisherlistener/datapathparameters/defaults)
- [static let realtime: WAPublisherListener.DatapathParameters](/documentation/wifiaware/wapublisherlistener/datapathparameters/realtime)

## Parameters

- [NWParameters](/documentation/network/nwparameters)
- [NWParametersBuilder](/documentation/network/nwparametersbuilder)
- [WAParameters](/documentation/wifiaware/waparameters)

### Setting common configurations

- [static let defaults: WAParameters](/documentation/wifiaware/waparameters/defaults)
- [static let realtime: WAParameters](/documentation/wifiaware/waparameters/realtime)

### Checking the configured performance mode

- [var performanceMode: WAPerformanceMode](/documentation/wifiaware/waparameters/performancemode)
- [init(performanceMode: WAPerformanceMode)](/documentation/wifiaware/waparameters/init(performancemode:))

## Connections

- [WAEndpoint](/documentation/wifiaware/waendpoint)

### Getting the service

- [var publishedService: WAPublishableService?](/documentation/wifiaware/waendpoint/publishedservice)
- [var subscribedService: WASubscribableService?](/documentation/wifiaware/waendpoint/subscribedservice)

### Getting the device anchoring the endpoint

- [let device: WAPairedDevice](/documentation/wifiaware/waendpoint/device)

### Getting a string description

- [var description: String](/documentation/wifiaware/waendpoint/description)

### Hashing and comparing

- [static func == (WAEndpoint, WAEndpoint) -> Bool](/documentation/wifiaware/waendpoint/==(_:_:))
- [func hash(into: inout Hasher)](/documentation/wifiaware/waendpoint/hash(into:))

## Connection performance

- [NWPath](/documentation/network/nwpath)
- [WAPath](/documentation/wifiaware/wapath)

### Getting a connection endpoint

- [let endpoint: WAEndpoint](/documentation/wifiaware/wapath/endpoint)

### Getting a current performance

- [let performance: WAPerformanceReport](/documentation/wifiaware/wapath/performance)

### Getting path metrics

- [let durationActive: Duration](/documentation/wifiaware/wapath/durationactive)
- [WAPerformanceMode](/documentation/wifiaware/waperformancemode)

### Setting performance modes

- [case bulk](/documentation/wifiaware/waperformancemode/bulk)
- [case realtime](/documentation/wifiaware/waperformancemode/realtime)
- [WAAccessCategory](/documentation/wifiaware/waaccesscategory)

### Providing throughput

- [case bestEffort](/documentation/wifiaware/waaccesscategory/besteffort)
- [case background](/documentation/wifiaware/waaccesscategory/background)
- [case interactiveVideo](/documentation/wifiaware/waaccesscategory/interactivevideo)
- [case interactiveVoice](/documentation/wifiaware/waaccesscategory/interactivevoice)
- [WAPerformanceReport](/documentation/wifiaware/waperformancereport)

### Reporting the data collection time

- [let timestamp: Date](/documentation/wifiaware/waperformancereport/timestamp)
- [let localTimestamp: ContinuousClock.Instant](/documentation/wifiaware/waperformancereport/localtimestamp)

### Getting the throughput metrics

- [let throughputCeiling: Double?](/documentation/wifiaware/waperformancereport/throughputceiling)
- [let throughputCapacity: Double?](/documentation/wifiaware/waperformancereport/throughputcapacity)
- [var throughputCapacityRatio: Double?](/documentation/wifiaware/waperformancereport/throughputcapacityratio)

### Getting the latency metrics

- [let transmitLatency: [WAAccessCategory : WAPerformanceReport.TransmitLatencyMetrics]](/documentation/wifiaware/waperformancereport/transmitlatency)
- [WAPerformanceReport.TransmitLatencyMetrics](/documentation/wifiaware/waperformancereport/transmitlatencymetrics)

#### Identifying the Wi-Fi access category

- [let accessCategory: WAAccessCategory](/documentation/wifiaware/waperformancereport/transmitlatencymetrics/accesscategory)

#### Getting the average Latency

- [let average: Duration?](/documentation/wifiaware/waperformancereport/transmitlatencymetrics/average)

### Getting the radio metrics

- [let signalStrength: Double?](/documentation/wifiaware/waperformancereport/signalstrength)

## Errors

- [NWError](/documentation/network/nwerror)
- [WAError](/documentation/wifiaware/waerror)

### Checking for general errors

- [case error(WAError.ErrorDetails)](/documentation/wifiaware/waerror/error(_:))
- [WAError.ErrorDetails](/documentation/wifiaware/waerror/errordetails)

### Checking for missing entitlement

- [WAError.EntitlementMissingDetails](/documentation/wifiaware/waerror/entitlementmissingdetails)
- [case entitlementMissing(WAError.EntitlementMissingDetails)](/documentation/wifiaware/waerror/entitlementmissing(_:))

### Checking for unsupported host hardware

- [case wifiAwareUnsupported(WAError.WiFiAwareUnsupportedDetails)](/documentation/wifiaware/waerror/wifiawareunsupported(_:))
- [WAError.WiFiAwareUnsupportedDetails](/documentation/wifiaware/waerror/wifiawareunsupporteddetails)

### Checking for insufficient radio resources

- [case noRadioResources(WAError.NoRadioResourcesDetails)](/documentation/wifiaware/waerror/noradioresources(_:))
- [WAError.NoRadioResourcesDetails](/documentation/wifiaware/waerror/noradioresourcesdetails)

### Checking for undeclared services

- [case serviceNotDeclared(WAError.ServiceNotDeclaredDetails)](/documentation/wifiaware/waerror/servicenotdeclared(_:))
- [WAError.ServiceNotDeclaredDetails](/documentation/wifiaware/waerror/servicenotdeclareddetails)

### Checking for service already in use

- [case serviceAlreadySubscribing(WAError.ServiceAlreadySubscribingDetails)](/documentation/wifiaware/waerror/servicealreadysubscribing(_:))
- [WAError.ServiceAlreadySubscribingDetails](/documentation/wifiaware/waerror/servicealreadysubscribingdetails)
- [case serviceAlreadyPublishing(WAError.ServiceAlreadyPublishingDetails)](/documentation/wifiaware/waerror/servicealreadypublishing(_:))
- [WAError.ServiceAlreadyPublishingDetails](/documentation/wifiaware/waerror/servicealreadypublishingdetails)

### Checking if paired devices are present or specified

- [case noPairedDevices(WAError.NoPairedDevicesDetails)](/documentation/wifiaware/waerror/nopaireddevices(_:))
- [WAError.NoPairedDevicesDetails](/documentation/wifiaware/waerror/nopaireddevicesdetails)

### Checking for invalid device

- [case deviceInvalid(WAError.DeviceInvalidDetails)](/documentation/wifiaware/waerror/deviceinvalid(_:))
- [WAError.DeviceInvalidDetails](/documentation/wifiaware/waerror/deviceinvaliddetails)

### Checking for unavailable device

- [case deviceNoLongerAvailable(WAError.DeviceNoLongerAvailableDetails)](/documentation/wifiaware/waerror/devicenolongeravailable(_:))
- [WAError.DeviceNoLongerAvailableDetails](/documentation/wifiaware/waerror/devicenolongeravailabledetails)

### Checking for connection

- [case connectionFailed(WAError.ConnectionFailedDetails)](/documentation/wifiaware/waerror/connectionfailed(_:))
- [WAError.ConnectionFailedDetails](/documentation/wifiaware/waerror/connectionfaileddetails)

### Checking for timeouts

- [case connectionIdleTimeout(WAError.ConnectionIdleTimeoutDetails)](/documentation/wifiaware/waerror/connectionidletimeout(_:))
- [case publisherTimeout(WAError.PublisherTimeoutDetails)](/documentation/wifiaware/waerror/publishertimeout(_:))
- [case subscriberTimeout(WAError.SubscriberTimeoutDetails)](/documentation/wifiaware/waerror/subscribertimeout(_:))
- [WAError.ConnectionIdleTimeoutDetails](/documentation/wifiaware/waerror/connectionidletimeoutdetails)
- [WAError.PublisherTimeoutDetails](/documentation/wifiaware/waerror/publishertimeoutdetails)
- [WAError.SubscriberTimeoutDetails](/documentation/wifiaware/waerror/subscribertimeoutdetails)

### Checking for terminated connection

- [case connectionTerminated(WAError.ConnectionTerminatedDetails)](/documentation/wifiaware/waerror/connectionterminated(_:))
- [WAError.ConnectionTerminatedDetails](/documentation/wifiaware/waerror/connectionterminateddetails)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
