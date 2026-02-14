# Core WLAN Documentation

Source: https://sosumi.ai/documentation/corewlan

---
title: Core WLAN
source: https://developer.apple.com/documentation/corewlan
timestamp: 2026-02-13T18:55:52.255Z
---

## Classes

- [CWChannel](/documentation/corewlan/cwchannel)

### Comparing channels

- [func isEqual(to: CWChannel) -> Bool](/documentation/corewlan/cwchannel/isequal(to:))

### Instance Properties

- [var channelBand: CWChannelBand](/documentation/corewlan/cwchannel/channelband)
- [var channelNumber: Int](/documentation/corewlan/cwchannel/channelnumber)
- [var channelWidth: CWChannelWidth](/documentation/corewlan/cwchannel/channelwidth)
- [CWConfiguration](/documentation/corewlan/cwconfiguration)

### Creating a configuration

- [init()](/documentation/corewlan/cwconfiguration/init())
- [init(configuration: CWConfiguration)](/documentation/corewlan/cwconfiguration/init(configuration:))

### Comparing configurations

- [func isEqual(to: CWConfiguration) -> Bool](/documentation/corewlan/cwconfiguration/isequal(to:))

### Instance Properties

- [var networkProfiles: NSOrderedSet](/documentation/corewlan/cwconfiguration/networkprofiles)
- [var rememberJoinedNetworks: Bool](/documentation/corewlan/cwconfiguration/rememberjoinednetworks)
- [var requireAdministratorForAssociation: Bool](/documentation/corewlan/cwconfiguration/requireadministratorforassociation)
- [var requireAdministratorForIBSSMode: Bool](/documentation/corewlan/cwconfiguration/requireadministratorforibssmode)
- [var requireAdministratorForPower: Bool](/documentation/corewlan/cwconfiguration/requireadministratorforpower)
- [CWInterface](/documentation/corewlan/cwinterface)

### Setting interface parameters

- [func setPairwiseMasterKey(Data?) throws](/documentation/corewlan/cwinterface/setpairwisemasterkey(_:))
- [func setPower(Bool) throws](/documentation/corewlan/cwinterface/setpower(_:))
- [func setWEPKey(Data?, flags: CWCipherKeyFlags, index: Int) throws](/documentation/corewlan/cwinterface/setwepkey(_:flags:index:))
- [func setWLANChannel(CWChannel) throws](/documentation/corewlan/cwinterface/setwlanchannel(_:))

### Scanning for networks

- [func scanForNetworks(withName: String?) throws -> Set<CWNetwork>](/documentation/corewlan/cwinterface/scanfornetworks(withname:))
- [func scanForNetworks(withSSID: Data?) throws -> Set<CWNetwork>](/documentation/corewlan/cwinterface/scanfornetworks(withssid:))

### Getting an interface

- [init(interfaceName: String?)](/documentation/corewlan/cwinterface/init(interfacename:))
- [convenience init(name: String?)](/documentation/corewlan/cwinterface/init(name:))

### Getting all attached interfaces

- [class func interfaceNames() -> Set<String>?](/documentation/corewlan/cwinterface/interfacenames())

### Disassociating from a network

- [func disassociate()](/documentation/corewlan/cwinterface/disassociate())

### Creating computer-to-computer networks

- [func startIBSSMode(withSSID: Data, security: CWIBSSModeSecurity, channel: Int, password: String?) throws](/documentation/corewlan/cwinterface/startibssmode(withssid:security:channel:password:))

### Committing a configuration

- [func commitConfiguration(CWConfiguration, authorization: SFAuthorization?) throws](/documentation/corewlan/cwinterface/commitconfiguration(_:authorization:))

### Associating to a network

- [func associate(toEnterpriseNetwork: CWNetwork, identity: SecIdentity?, username: String?, password: String?) throws](/documentation/corewlan/cwinterface/associate(toenterprisenetwork:identity:username:password:))
- [func associate(to: CWNetwork, password: String?) throws](/documentation/corewlan/cwinterface/associate(to:password:))

### Instance Properties

- [var interfaceName: String?](/documentation/corewlan/cwinterface/interfacename)

### Instance Methods

- [func activePHYMode() -> CWPHYMode](/documentation/corewlan/cwinterface/activephymode())
- [func bssid() -> String?](/documentation/corewlan/cwinterface/bssid())
- [func cachedScanResults() -> Set<CWNetwork>?](/documentation/corewlan/cwinterface/cachedscanresults())
- [func configuration() -> CWConfiguration?](/documentation/corewlan/cwinterface/configuration())
- [func countryCode() -> String?](/documentation/corewlan/cwinterface/countrycode())
- [func hardwareAddress() -> String?](/documentation/corewlan/cwinterface/hardwareaddress())
- [func interfaceMode() -> CWInterfaceMode](/documentation/corewlan/cwinterface/interfacemode())
- [func noiseMeasurement() -> Int](/documentation/corewlan/cwinterface/noisemeasurement())
- [func powerOn() -> Bool](/documentation/corewlan/cwinterface/poweron())
- [func rssiValue() -> Int](/documentation/corewlan/cwinterface/rssivalue())
- [func scanForNetworks(withName: String?, includeHidden: Bool) throws -> Set<CWNetwork>](/documentation/corewlan/cwinterface/scanfornetworks(withname:includehidden:))
- [func scanForNetworks(withSSID: Data?, includeHidden: Bool) throws -> Set<CWNetwork>](/documentation/corewlan/cwinterface/scanfornetworks(withssid:includehidden:))
- [func security() -> CWSecurity](/documentation/corewlan/cwinterface/security())
- [func serviceActive() -> Bool](/documentation/corewlan/cwinterface/serviceactive())
- [func ssid() -> String?](/documentation/corewlan/cwinterface/ssid())
- [func ssidData() -> Data?](/documentation/corewlan/cwinterface/ssiddata())
- [func supportedWLANChannels() -> Set<CWChannel>?](/documentation/corewlan/cwinterface/supportedwlanchannels())
- [func transmitPower() -> Int](/documentation/corewlan/cwinterface/transmitpower())
- [func transmitRate() -> Double](/documentation/corewlan/cwinterface/transmitrate())
- [func wlanChannel() -> CWChannel?](/documentation/corewlan/cwinterface/wlanchannel())
- [CWMutableConfiguration](/documentation/corewlan/cwmutableconfiguration)

### Configuring Preferred Networks

- [var networkProfiles: NSOrderedSet](/documentation/corewlan/cwmutableconfiguration/networkprofiles)

### Configuring Settings

- [var rememberJoinedNetworks: Bool](/documentation/corewlan/cwmutableconfiguration/rememberjoinednetworks)
- [var requireAdministratorForAssociation: Bool](/documentation/corewlan/cwmutableconfiguration/requireadministratorforassociation)
- [var requireAdministratorForPower: Bool](/documentation/corewlan/cwmutableconfiguration/requireadministratorforpower)
- [var requireAdministratorForIBSSMode: Bool](/documentation/corewlan/cwmutableconfiguration/requireadministratorforibssmode)
- [CWMutableNetworkProfile](/documentation/corewlan/cwmutablenetworkprofile)

### Configuring Network Profiles

- [var ssidData: Data?](/documentation/corewlan/cwmutablenetworkprofile/ssiddata)
- [var security: CWSecurity](/documentation/corewlan/cwmutablenetworkprofile/security)
- [CWNetwork](/documentation/corewlan/cwnetwork)

### Getting supported security types

- [func supportsSecurity(CWSecurity) -> Bool](/documentation/corewlan/cwnetwork/supportssecurity(_:))

### Getting supported PHY modes

- [func supportsPHYMode(CWPHYMode) -> Bool](/documentation/corewlan/cwnetwork/supportsphymode(_:))

### Comparing wireless networks

- [func isEqual(to: CWNetwork) -> Bool](/documentation/corewlan/cwnetwork/isequal(to:))

### Instance Properties

- [var beaconInterval: Int](/documentation/corewlan/cwnetwork/beaconinterval)
- [var bssid: String?](/documentation/corewlan/cwnetwork/bssid)
- [var countryCode: String?](/documentation/corewlan/cwnetwork/countrycode)
- [var ibss: Bool](/documentation/corewlan/cwnetwork/ibss)
- [var informationElementData: Data?](/documentation/corewlan/cwnetwork/informationelementdata)
- [var noiseMeasurement: Int](/documentation/corewlan/cwnetwork/noisemeasurement)
- [var rssiValue: Int](/documentation/corewlan/cwnetwork/rssivalue)
- [var ssid: String?](/documentation/corewlan/cwnetwork/ssid)
- [var ssidData: Data?](/documentation/corewlan/cwnetwork/ssiddata)
- [var wlanChannel: CWChannel?](/documentation/corewlan/cwnetwork/wlanchannel)
- [CWNetworkProfile](/documentation/corewlan/cwnetworkprofile)

### Getting a network profile

- [init()](/documentation/corewlan/cwnetworkprofile/init())
- [init(networkProfile: CWNetworkProfile)](/documentation/corewlan/cwnetworkprofile/init(networkprofile:))

### Comparing network profiles

- [func isEqual(to: CWNetworkProfile) -> Bool](/documentation/corewlan/cwnetworkprofile/isequal(to:))

### Instance Properties

- [var security: CWSecurity](/documentation/corewlan/cwnetworkprofile/security)
- [var ssid: String?](/documentation/corewlan/cwnetworkprofile/ssid)
- [var ssidData: Data?](/documentation/corewlan/cwnetworkprofile/ssiddata)
- [CWWiFiClient](/documentation/corewlan/cwwificlient)

### Getting the Shared Instance

- [class func shared() -> CWWiFiClient](/documentation/corewlan/cwwificlient/shared())

### Initializing a Wi-Fi Client

- [init()](/documentation/corewlan/cwwificlient/init())

### Setting a Delegate

- [var delegate: AnyObject?](/documentation/corewlan/cwwificlient/delegate)

### Getting Interfaces

- [func interface() -> CWInterface?](/documentation/corewlan/cwwificlient/interface())
- [func interface(withName: String?) -> CWInterface?](/documentation/corewlan/cwwificlient/interface(withname:))
- [func interfaces() -> [CWInterface]?](/documentation/corewlan/cwwificlient/interfaces())
- [class func interfaceNames() -> [String]?](/documentation/corewlan/cwwificlient/interfacenames()-swift.type.method)

### Monitoring Events

- [func startMonitoringEvent(with: CWEventType) throws](/documentation/corewlan/cwwificlient/startmonitoringevent(with:))
- [func stopMonitoringAllEvents() throws](/documentation/corewlan/cwwificlient/stopmonitoringallevents())
- [func stopMonitoringEvent(with: CWEventType) throws](/documentation/corewlan/cwwificlient/stopmonitoringevent(with:))

### Instance Methods

- [func interfaceNames() -> [String]?](/documentation/corewlan/cwwificlient/interfacenames()-swift.method)

## Protocols

- [CWEventDelegate](/documentation/corewlan/cweventdelegate)

### Instance Methods

- [func bssidDidChangeForWiFiInterface(withName: String)](/documentation/corewlan/cweventdelegate/bssiddidchangeforwifiinterface(withname:))
- [func clientConnectionInterrupted()](/documentation/corewlan/cweventdelegate/clientconnectioninterrupted())
- [func clientConnectionInvalidated()](/documentation/corewlan/cweventdelegate/clientconnectioninvalidated())
- [func countryCodeDidChangeForWiFiInterface(withName: String)](/documentation/corewlan/cweventdelegate/countrycodedidchangeforwifiinterface(withname:))
- [func linkDidChangeForWiFiInterface(withName: String)](/documentation/corewlan/cweventdelegate/linkdidchangeforwifiinterface(withname:))
- [func linkQualityDidChangeForWiFiInterface(withName: String, rssi: Int, transmitRate: Double)](/documentation/corewlan/cweventdelegate/linkqualitydidchangeforwifiinterface(withname:rssi:transmitrate:))
- [func modeDidChangeForWiFiInterface(withName: String)](/documentation/corewlan/cweventdelegate/modedidchangeforwifiinterface(withname:))
- [func powerStateDidChangeForWiFiInterface(withName: String)](/documentation/corewlan/cweventdelegate/powerstatedidchangeforwifiinterface(withname:))
- [func scanCacheUpdatedForWiFiInterface(withName: String)](/documentation/corewlan/cweventdelegate/scancacheupdatedforwifiinterface(withname:))
- [func ssidDidChangeForWiFiInterface(withName: String)](/documentation/corewlan/cweventdelegate/ssiddidchangeforwifiinterface(withname:))

## Reference

- [CoreWLANConstants.h](/documentation/corewlan/corewlanconstants-h)

### Constants

- [Global Constants](/documentation/corewlan/global-constants)

#### Constants

- [let CWErrorDomain: String](/documentation/corewlan/cwerrordomain)
- [let CWLinkQualityNotificationRSSIKey: String](/documentation/corewlan/cwlinkqualitynotificationrssikey)
- [let CWLinkQualityNotificationTransmitRateKey: String](/documentation/corewlan/cwlinkqualitynotificationtransmitratekey)
- [CoreWLANTypes.h](/documentation/corewlan/corewlantypes-h)

### Constants

- [CWChannelBand](/documentation/corewlan/cwchannelband)

#### Constants

- [case bandUnknown](/documentation/corewlan/cwchannelband/bandunknown)
- [case band2GHz](/documentation/corewlan/cwchannelband/band2ghz)
- [case band5GHz](/documentation/corewlan/cwchannelband/band5ghz)

#### Enumeration Cases

- [case band6GHz](/documentation/corewlan/cwchannelband/band6ghz)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwchannelband/init(rawvalue:))
- [CWChannelWidth](/documentation/corewlan/cwchannelwidth)

#### Constants

- [case widthUnknown](/documentation/corewlan/cwchannelwidth/widthunknown)
- [case width20MHz](/documentation/corewlan/cwchannelwidth/width20mhz)
- [case width40MHz](/documentation/corewlan/cwchannelwidth/width40mhz)
- [case width80MHz](/documentation/corewlan/cwchannelwidth/width80mhz)
- [case width160MHz](/documentation/corewlan/cwchannelwidth/width160mhz)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwchannelwidth/init(rawvalue:))
- [CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags)

#### Constants

- [static var unicast: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/unicast)
- [static var multicast: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/multicast)
- [static var tx: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/tx)
- [static var rx: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/rx)

#### Initializers

- [init(rawValue: UInt)](/documentation/corewlan/cwcipherkeyflags/init(rawvalue:))
- [CWErr](/documentation/corewlan/cwerr)

#### Constants

- [case cwapFullErr](/documentation/corewlan/cwerr/cwapfullerr)
- [case cwAssociationDeniedErr](/documentation/corewlan/cwerr/cwassociationdeniederr)
- [case cwAuthenticationAlgorithmUnsupportedErr](/documentation/corewlan/cwerr/cwauthenticationalgorithmunsupportederr)
- [case cwChallengeFailureErr](/documentation/corewlan/cwerr/cwchallengefailureerr)
- [case cwCipherSuiteRejectedErr](/documentation/corewlan/cwerr/cwciphersuiterejectederr)
- [case cwdsssofdmUnsupportedErr](/documentation/corewlan/cwerr/cwdsssofdmunsupportederr)
- [case cweapolErr](/documentation/corewlan/cwerr/cweapolerr)
- [case cwErr](/documentation/corewlan/cwerr/cwerr)
- [case cwhtFeaturesNotSupportedErr](/documentation/corewlan/cwerr/cwhtfeaturesnotsupportederr)
- [case cwipcFailureErr](/documentation/corewlan/cwerr/cwipcfailureerr)
- [case cwInvalidAKMPErr](/documentation/corewlan/cwerr/cwinvalidakmperr)
- [case cwInvalidAuthenticationSequenceNumberErr](/documentation/corewlan/cwerr/cwinvalidauthenticationsequencenumbererr)
- [case cwInvalidFormatErr](/documentation/corewlan/cwerr/cwinvalidformaterr)
- [case cwInvalidGroupCipherErr](/documentation/corewlan/cwerr/cwinvalidgroupciphererr)
- [case cwInvalidInformationElementErr](/documentation/corewlan/cwerr/cwinvalidinformationelementerr)
- [case cwInvalidPMKErr](/documentation/corewlan/cwerr/cwinvalidpmkerr)
- [case cwInvalidPairwiseCipherErr](/documentation/corewlan/cwerr/cwinvalidpairwiseciphererr)
- [case cwInvalidParameterErr](/documentation/corewlan/cwerr/cwinvalidparametererr)
- [case cwInvalidRSNCapabilitiesErr](/documentation/corewlan/cwerr/cwinvalidrsncapabilitieserr)
- [case cwNoErr](/documentation/corewlan/cwerr/cwnoerr)
- [case cwNoMemoryErr](/documentation/corewlan/cwerr/cwnomemoryerr)
- [case cwNotSupportedErr](/documentation/corewlan/cwerr/cwnotsupportederr)
- [case cwOperationNotPermittedErr](/documentation/corewlan/cwerr/cwoperationnotpermittederr)
- [case cwpcoTransitionTimeNotSupportedErr](/documentation/corewlan/cwerr/cwpcotransitiontimenotsupportederr)
- [case cwReassociationDeniedErr](/documentation/corewlan/cwerr/cwreassociationdeniederr)
- [case cwReferenceNotBoundErr](/documentation/corewlan/cwerr/cwreferencenotbounderr)
- [case cwShortSlotUnsupportedErr](/documentation/corewlan/cwerr/cwshortslotunsupportederr)
- [case cwSupplicantTimeoutErr](/documentation/corewlan/cwerr/cwsupplicanttimeouterr)
- [case cwTimeoutErr](/documentation/corewlan/cwerr/cwtimeouterr)
- [case cwUnknownErr](/documentation/corewlan/cwerr/cwunknownerr)
- [case cwUnspecifiedFailureErr](/documentation/corewlan/cwerr/cwunspecifiedfailureerr)
- [case cwUnsupportedCapabilitiesErr](/documentation/corewlan/cwerr/cwunsupportedcapabilitieserr)
- [case cwUnsupportedRSNVersionErr](/documentation/corewlan/cwerr/cwunsupportedrsnversionerr)
- [case cwUnsupportedRateSetErr](/documentation/corewlan/cwerr/cwunsupportedrateseterr)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwerr/init(rawvalue:))
- [CWIBSSModeSecurity](/documentation/corewlan/cwibssmodesecurity)

#### Constants

- [case none](/documentation/corewlan/cwibssmodesecurity/none)
- [case WEP40](/documentation/corewlan/cwibssmodesecurity/wep40)
- [case WEP104](/documentation/corewlan/cwibssmodesecurity/wep104)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwibssmodesecurity/init(rawvalue:))
- [CWPHYMode](/documentation/corewlan/cwphymode)

#### Constants

- [case modeNone](/documentation/corewlan/cwphymode/modenone)
- [case mode11a](/documentation/corewlan/cwphymode/mode11a)
- [case mode11b](/documentation/corewlan/cwphymode/mode11b)
- [case mode11g](/documentation/corewlan/cwphymode/mode11g)
- [case mode11n](/documentation/corewlan/cwphymode/mode11n)
- [case mode11ac](/documentation/corewlan/cwphymode/mode11ac)

#### Enumeration Cases

- [case mode11ax](/documentation/corewlan/cwphymode/mode11ax)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwphymode/init(rawvalue:))
- [CWSecurity](/documentation/corewlan/cwsecurity)

#### Constants

- [case none](/documentation/corewlan/cwsecurity/none)
- [case WEP](/documentation/corewlan/cwsecurity/wep)
- [case wpaPersonal](/documentation/corewlan/cwsecurity/wpapersonal)
- [case wpaPersonalMixed](/documentation/corewlan/cwsecurity/wpapersonalmixed)
- [case wpa2Personal](/documentation/corewlan/cwsecurity/wpa2personal)
- [case personal](/documentation/corewlan/cwsecurity/personal)
- [case dynamicWEP](/documentation/corewlan/cwsecurity/dynamicwep)
- [case wpaEnterprise](/documentation/corewlan/cwsecurity/wpaenterprise)
- [case wpaEnterpriseMixed](/documentation/corewlan/cwsecurity/wpaenterprisemixed)
- [case wpa2Enterprise](/documentation/corewlan/cwsecurity/wpa2enterprise)
- [case enterprise](/documentation/corewlan/cwsecurity/enterprise)
- [case wpa3Personal](/documentation/corewlan/cwsecurity/wpa3personal)
- [case wpa3Enterprise](/documentation/corewlan/cwsecurity/wpa3enterprise)
- [case wpa3Transition](/documentation/corewlan/cwsecurity/wpa3transition)
- [case unknown](/documentation/corewlan/cwsecurity/unknown)

#### Enumeration Cases

- [case OWE](/documentation/corewlan/cwsecurity/owe)
- [case oweTransition](/documentation/corewlan/cwsecurity/owetransition)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwsecurity/init(rawvalue:))
- [CoreWLANUtil.h](/documentation/corewlan/corewlanutil-h)

### Utility Methods

- [func CWKeychainCopyEAPIdentityList(UnsafeMutablePointer<Unmanaged<CFArray>?>?) -> OSStatus](/documentation/corewlan/cwkeychaincopyeapidentitylist(_:))
- [func CWMergeNetworks(Set<CWNetwork>) -> Set<CWNetwork>](/documentation/corewlan/cwmergenetworks(_:))
- [CoreWLAN Enumerations](/documentation/corewlan/corewlan-enumerations)

### Enumerations

- [CWChannelBand](/documentation/corewlan/cwchannelband)

#### Constants

- [case bandUnknown](/documentation/corewlan/cwchannelband/bandunknown)
- [case band2GHz](/documentation/corewlan/cwchannelband/band2ghz)
- [case band5GHz](/documentation/corewlan/cwchannelband/band5ghz)

#### Enumeration Cases

- [case band6GHz](/documentation/corewlan/cwchannelband/band6ghz)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwchannelband/init(rawvalue:))
- [CWChannelWidth](/documentation/corewlan/cwchannelwidth)

#### Constants

- [case widthUnknown](/documentation/corewlan/cwchannelwidth/widthunknown)
- [case width20MHz](/documentation/corewlan/cwchannelwidth/width20mhz)
- [case width40MHz](/documentation/corewlan/cwchannelwidth/width40mhz)
- [case width80MHz](/documentation/corewlan/cwchannelwidth/width80mhz)
- [case width160MHz](/documentation/corewlan/cwchannelwidth/width160mhz)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwchannelwidth/init(rawvalue:))
- [CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags)

#### Constants

- [static var unicast: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/unicast)
- [static var multicast: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/multicast)
- [static var tx: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/tx)
- [static var rx: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/rx)

#### Initializers

- [init(rawValue: UInt)](/documentation/corewlan/cwcipherkeyflags/init(rawvalue:))
- [CWErr](/documentation/corewlan/cwerr)

#### Constants

- [case cwapFullErr](/documentation/corewlan/cwerr/cwapfullerr)
- [case cwAssociationDeniedErr](/documentation/corewlan/cwerr/cwassociationdeniederr)
- [case cwAuthenticationAlgorithmUnsupportedErr](/documentation/corewlan/cwerr/cwauthenticationalgorithmunsupportederr)
- [case cwChallengeFailureErr](/documentation/corewlan/cwerr/cwchallengefailureerr)
- [case cwCipherSuiteRejectedErr](/documentation/corewlan/cwerr/cwciphersuiterejectederr)
- [case cwdsssofdmUnsupportedErr](/documentation/corewlan/cwerr/cwdsssofdmunsupportederr)
- [case cweapolErr](/documentation/corewlan/cwerr/cweapolerr)
- [case cwErr](/documentation/corewlan/cwerr/cwerr)
- [case cwhtFeaturesNotSupportedErr](/documentation/corewlan/cwerr/cwhtfeaturesnotsupportederr)
- [case cwipcFailureErr](/documentation/corewlan/cwerr/cwipcfailureerr)
- [case cwInvalidAKMPErr](/documentation/corewlan/cwerr/cwinvalidakmperr)
- [case cwInvalidAuthenticationSequenceNumberErr](/documentation/corewlan/cwerr/cwinvalidauthenticationsequencenumbererr)
- [case cwInvalidFormatErr](/documentation/corewlan/cwerr/cwinvalidformaterr)
- [case cwInvalidGroupCipherErr](/documentation/corewlan/cwerr/cwinvalidgroupciphererr)
- [case cwInvalidInformationElementErr](/documentation/corewlan/cwerr/cwinvalidinformationelementerr)
- [case cwInvalidPMKErr](/documentation/corewlan/cwerr/cwinvalidpmkerr)
- [case cwInvalidPairwiseCipherErr](/documentation/corewlan/cwerr/cwinvalidpairwiseciphererr)
- [case cwInvalidParameterErr](/documentation/corewlan/cwerr/cwinvalidparametererr)
- [case cwInvalidRSNCapabilitiesErr](/documentation/corewlan/cwerr/cwinvalidrsncapabilitieserr)
- [case cwNoErr](/documentation/corewlan/cwerr/cwnoerr)
- [case cwNoMemoryErr](/documentation/corewlan/cwerr/cwnomemoryerr)
- [case cwNotSupportedErr](/documentation/corewlan/cwerr/cwnotsupportederr)
- [case cwOperationNotPermittedErr](/documentation/corewlan/cwerr/cwoperationnotpermittederr)
- [case cwpcoTransitionTimeNotSupportedErr](/documentation/corewlan/cwerr/cwpcotransitiontimenotsupportederr)
- [case cwReassociationDeniedErr](/documentation/corewlan/cwerr/cwreassociationdeniederr)
- [case cwReferenceNotBoundErr](/documentation/corewlan/cwerr/cwreferencenotbounderr)
- [case cwShortSlotUnsupportedErr](/documentation/corewlan/cwerr/cwshortslotunsupportederr)
- [case cwSupplicantTimeoutErr](/documentation/corewlan/cwerr/cwsupplicanttimeouterr)
- [case cwTimeoutErr](/documentation/corewlan/cwerr/cwtimeouterr)
- [case cwUnknownErr](/documentation/corewlan/cwerr/cwunknownerr)
- [case cwUnspecifiedFailureErr](/documentation/corewlan/cwerr/cwunspecifiedfailureerr)
- [case cwUnsupportedCapabilitiesErr](/documentation/corewlan/cwerr/cwunsupportedcapabilitieserr)
- [case cwUnsupportedRSNVersionErr](/documentation/corewlan/cwerr/cwunsupportedrsnversionerr)
- [case cwUnsupportedRateSetErr](/documentation/corewlan/cwerr/cwunsupportedrateseterr)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwerr/init(rawvalue:))
- [CWEventType](/documentation/corewlan/cweventtype)

#### Constants

- [case none](/documentation/corewlan/cweventtype/none)
- [case powerDidChange](/documentation/corewlan/cweventtype/powerdidchange)
- [case ssidDidChange](/documentation/corewlan/cweventtype/ssiddidchange)
- [case bssidDidChange](/documentation/corewlan/cweventtype/bssiddidchange)
- [case countryCodeDidChange](/documentation/corewlan/cweventtype/countrycodedidchange)
- [case linkDidChange](/documentation/corewlan/cweventtype/linkdidchange)
- [case linkQualityDidChange](/documentation/corewlan/cweventtype/linkqualitydidchange)
- [case modeDidChange](/documentation/corewlan/cweventtype/modedidchange)
- [case scanCacheUpdated](/documentation/corewlan/cweventtype/scancacheupdated)
- [case unknown](/documentation/corewlan/cweventtype/unknown)

#### Enumeration Cases

- [case btCoexStats](/documentation/corewlan/cweventtype/btcoexstats)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cweventtype/init(rawvalue:))
- [CWIBSSModeSecurity](/documentation/corewlan/cwibssmodesecurity)

#### Constants

- [case none](/documentation/corewlan/cwibssmodesecurity/none)
- [case WEP40](/documentation/corewlan/cwibssmodesecurity/wep40)
- [case WEP104](/documentation/corewlan/cwibssmodesecurity/wep104)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwibssmodesecurity/init(rawvalue:))
- [CWInterfaceMode](/documentation/corewlan/cwinterfacemode)

#### Constants

- [case none](/documentation/corewlan/cwinterfacemode/none)
- [case station](/documentation/corewlan/cwinterfacemode/station)
- [case IBSS](/documentation/corewlan/cwinterfacemode/ibss)
- [case hostAP](/documentation/corewlan/cwinterfacemode/hostap)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwinterfacemode/init(rawvalue:))
- [CWKeychainDomain](/documentation/corewlan/cwkeychaindomain)

#### Constants

- [case none](/documentation/corewlan/cwkeychaindomain/none)
- [case user](/documentation/corewlan/cwkeychaindomain/user)
- [case system](/documentation/corewlan/cwkeychaindomain/system)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwkeychaindomain/init(rawvalue:))
- [CWPHYMode](/documentation/corewlan/cwphymode)

#### Constants

- [case modeNone](/documentation/corewlan/cwphymode/modenone)
- [case mode11a](/documentation/corewlan/cwphymode/mode11a)
- [case mode11b](/documentation/corewlan/cwphymode/mode11b)
- [case mode11g](/documentation/corewlan/cwphymode/mode11g)
- [case mode11n](/documentation/corewlan/cwphymode/mode11n)
- [case mode11ac](/documentation/corewlan/cwphymode/mode11ac)

#### Enumeration Cases

- [case mode11ax](/documentation/corewlan/cwphymode/mode11ax)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwphymode/init(rawvalue:))
- [CWSecurity](/documentation/corewlan/cwsecurity)

#### Constants

- [case none](/documentation/corewlan/cwsecurity/none)
- [case WEP](/documentation/corewlan/cwsecurity/wep)
- [case wpaPersonal](/documentation/corewlan/cwsecurity/wpapersonal)
- [case wpaPersonalMixed](/documentation/corewlan/cwsecurity/wpapersonalmixed)
- [case wpa2Personal](/documentation/corewlan/cwsecurity/wpa2personal)
- [case personal](/documentation/corewlan/cwsecurity/personal)
- [case dynamicWEP](/documentation/corewlan/cwsecurity/dynamicwep)
- [case wpaEnterprise](/documentation/corewlan/cwsecurity/wpaenterprise)
- [case wpaEnterpriseMixed](/documentation/corewlan/cwsecurity/wpaenterprisemixed)
- [case wpa2Enterprise](/documentation/corewlan/cwsecurity/wpa2enterprise)
- [case enterprise](/documentation/corewlan/cwsecurity/enterprise)
- [case wpa3Personal](/documentation/corewlan/cwsecurity/wpa3personal)
- [case wpa3Enterprise](/documentation/corewlan/cwsecurity/wpa3enterprise)
- [case wpa3Transition](/documentation/corewlan/cwsecurity/wpa3transition)
- [case unknown](/documentation/corewlan/cwsecurity/unknown)

#### Enumeration Cases

- [case OWE](/documentation/corewlan/cwsecurity/owe)
- [case oweTransition](/documentation/corewlan/cwsecurity/owetransition)

#### Initializers

- [init?(rawValue: Int)](/documentation/corewlan/cwsecurity/init(rawvalue:))
- [CoreWLAN Functions](/documentation/corewlan/corewlan-functions)

### Functions

- [func CWKeychainCopyWiFiEAPIdentity(CWKeychainDomain, Data, UnsafeMutablePointer<Unmanaged<SecIdentity>?>?) -> OSStatus](/documentation/corewlan/cwkeychaincopywifieapidentity(_:_:_:))
- [func CWKeychainDeleteWiFiEAPUsernameAndPassword(CWKeychainDomain, Data) -> OSStatus](/documentation/corewlan/cwkeychaindeletewifieapusernameandpassword(_:_:))
- [func CWKeychainDeleteWiFiPassword(CWKeychainDomain, Data) -> OSStatus](/documentation/corewlan/cwkeychaindeletewifipassword(_:_:))
- [func CWKeychainFindWiFiEAPUsernameAndPassword(CWKeychainDomain, Data, AutoreleasingUnsafeMutablePointer<NSString?>?, AutoreleasingUnsafeMutablePointer<NSString?>?) -> OSStatus](/documentation/corewlan/cwkeychainfindwifieapusernameandpassword(_:_:_:_:))
- [func CWKeychainFindWiFiPassword(CWKeychainDomain, Data, AutoreleasingUnsafeMutablePointer<NSString?>?) -> OSStatus](/documentation/corewlan/cwkeychainfindwifipassword(_:_:_:))
- [func CWKeychainSetWiFiEAPIdentity(CWKeychainDomain, Data, SecIdentity?) -> OSStatus](/documentation/corewlan/cwkeychainsetwifieapidentity(_:_:_:))
- [func CWKeychainSetWiFiEAPUsernameAndPassword(CWKeychainDomain, Data, String?, String?) -> OSStatus](/documentation/corewlan/cwkeychainsetwifieapusernameandpassword(_:_:_:_:))
- [func CWKeychainSetWiFiPassword(CWKeychainDomain, Data, String) -> OSStatus](/documentation/corewlan/cwkeychainsetwifipassword(_:_:_:))

## Structures

- [CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags)

### Constants

- [static var unicast: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/unicast)
- [static var multicast: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/multicast)
- [static var tx: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/tx)
- [static var rx: CWCipherKeyFlags](/documentation/corewlan/cwcipherkeyflags/rx)

### Initializers

- [init(rawValue: UInt)](/documentation/corewlan/cwcipherkeyflags/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
