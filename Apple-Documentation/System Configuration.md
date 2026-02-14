# System Configuration Documentation

Source: https://sosumi.ai/documentation/systemconfiguration

---
title: System Configuration
source: https://developer.apple.com/documentation/systemconfiguration
timestamp: 2026-02-13T19:02:52.113Z
---

## Reference

- [SCDynamicStore](/documentation/systemconfiguration/scdynamicstore-gb2)

### Creating a Dynamic Store Session

- [func SCDynamicStoreCreateWithOptions(CFAllocator?, CFString, CFDictionary?, SCDynamicStoreCallBack?, UnsafeMutablePointer<SCDynamicStoreContext>?) -> SCDynamicStore?](/documentation/systemconfiguration/scdynamicstorecreatewithoptions(_:_:_:_:_:))
- [func SCDynamicStoreCreate(CFAllocator?, CFString, SCDynamicStoreCallBack?, UnsafeMutablePointer<SCDynamicStoreContext>?) -> SCDynamicStore?](/documentation/systemconfiguration/scdynamicstorecreate(_:_:_:_:))

### Adding or Updating Keys and Values

- [func SCDynamicStoreAddTemporaryValue(SCDynamicStore, CFString, CFPropertyList) -> Bool](/documentation/systemconfiguration/scdynamicstoreaddtemporaryvalue(_:_:_:))
- [func SCDynamicStoreAddValue(SCDynamicStore?, CFString, CFPropertyList) -> Bool](/documentation/systemconfiguration/scdynamicstoreaddvalue(_:_:_:))
- [func SCDynamicStoreSetMultiple(SCDynamicStore?, CFDictionary?, CFArray?, CFArray?) -> Bool](/documentation/systemconfiguration/scdynamicstoresetmultiple(_:_:_:_:))
- [func SCDynamicStoreSetValue(SCDynamicStore?, CFString, CFPropertyList) -> Bool](/documentation/systemconfiguration/scdynamicstoresetvalue(_:_:_:))

### Getting Keys and Values

- [func SCDynamicStoreCopyKeyList(SCDynamicStore?, CFString) -> CFArray?](/documentation/systemconfiguration/scdynamicstorecopykeylist(_:_:))
- [func SCDynamicStoreCopyMultiple(SCDynamicStore?, CFArray?, CFArray?) -> CFDictionary?](/documentation/systemconfiguration/scdynamicstorecopymultiple(_:_:_:))
- [func SCDynamicStoreCopyNotifiedKeys(SCDynamicStore) -> CFArray?](/documentation/systemconfiguration/scdynamicstorecopynotifiedkeys(_:))
- [func SCDynamicStoreCopyValue(SCDynamicStore?, CFString) -> CFPropertyList?](/documentation/systemconfiguration/scdynamicstorecopyvalue(_:_:))

### Monitoring Keys and Values

- [func SCDynamicStoreNotifyValue(SCDynamicStore?, CFString) -> Bool](/documentation/systemconfiguration/scdynamicstorenotifyvalue(_:_:))
- [func SCDynamicStoreSetNotificationKeys(SCDynamicStore, CFArray?, CFArray?) -> Bool](/documentation/systemconfiguration/scdynamicstoresetnotificationkeys(_:_:_:))
- [func SCDynamicStoreSetDispatchQueue(SCDynamicStore, dispatch_queue_t?) -> Bool](/documentation/systemconfiguration/scdynamicstoresetdispatchqueue(_:_:))

### Removing Keys and Values

- [func SCDynamicStoreRemoveValue(SCDynamicStore?, CFString) -> Bool](/documentation/systemconfiguration/scdynamicstoreremovevalue(_:_:))

### Creating a Run Loop Source

- [func SCDynamicStoreCreateRunLoopSource(CFAllocator?, SCDynamicStore, CFIndex) -> CFRunLoopSource?](/documentation/systemconfiguration/scdynamicstorecreaterunloopsource(_:_:_:))

### Getting Information About the Dynamic Store

- [func SCDynamicStoreGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scdynamicstoregettypeid())

### Data Types

- [SCDynamicStoreCallBack](/documentation/systemconfiguration/scdynamicstorecallback)

#### Fields

- [store](/documentation/systemconfiguration/1807875-store)
- [changedKeys](/documentation/systemconfiguration/1807876-changedkeys)
- [info](/documentation/systemconfiguration/1807877-info)
- [SCDynamicStoreContext](/documentation/systemconfiguration/scdynamicstorecontext)

#### Initializers

- [init()](/documentation/systemconfiguration/scdynamicstorecontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer?, retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?, release: ((UnsafeRawPointer) -> Void)?, copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?)](/documentation/systemconfiguration/scdynamicstorecontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?](/documentation/systemconfiguration/scdynamicstorecontext/copydescription)
- [var info: UnsafeMutableRawPointer?](/documentation/systemconfiguration/scdynamicstorecontext/info)
- [var release: ((UnsafeRawPointer) -> Void)?](/documentation/systemconfiguration/scdynamicstorecontext/release)
- [var retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?](/documentation/systemconfiguration/scdynamicstorecontext/retain)
- [var version: CFIndex](/documentation/systemconfiguration/scdynamicstorecontext/version)
- [SCDynamicStore](/documentation/systemconfiguration/scdynamicstore)

### Constants

- [Dynamic Store Options Keys](/documentation/systemconfiguration/dynamic-store-options-keys)

#### Constants

- [let kSCDynamicStoreUseSessionKeys: CFString](/documentation/systemconfiguration/kscdynamicstoreusesessionkeys)
- [SCDynamicStoreCopySpecific](/documentation/systemconfiguration/scdynamicstorecopyspecific)

### Group

- [func SCDynamicStoreCopyComputerName(SCDynamicStore?, UnsafeMutablePointer<CFStringEncoding>?) -> CFString?](/documentation/systemconfiguration/scdynamicstorecopycomputername(_:_:))
- [func SCDynamicStoreCopyConsoleUser(SCDynamicStore?, UnsafeMutablePointer<uid_t>?, UnsafeMutablePointer<gid_t>?) -> CFString?](/documentation/systemconfiguration/scdynamicstorecopyconsoleuser(_:_:_:))
- [func SCDynamicStoreCopyLocalHostName(SCDynamicStore?) -> CFString?](/documentation/systemconfiguration/scdynamicstorecopylocalhostname(_:))
- [func SCDynamicStoreCopyLocation(SCDynamicStore?) -> CFString?](/documentation/systemconfiguration/scdynamicstorecopylocation(_:))
- [func SCDynamicStoreCopyProxies(SCDynamicStore?) -> CFDictionary?](/documentation/systemconfiguration/scdynamicstorecopyproxies(_:))
- [SCDynamicStoreKey](/documentation/systemconfiguration/scdynamicstorekey)

### Group

- [func SCDynamicStoreKeyCreateNetworkGlobalEntity(CFAllocator?, CFString, CFString) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreatenetworkglobalentity(_:_:_:))
- [func SCDynamicStoreKeyCreateNetworkInterface(CFAllocator?, CFString) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreatenetworkinterface(_:_:))
- [func SCDynamicStoreKeyCreateNetworkInterfaceEntity(CFAllocator?, CFString, CFString, CFString?) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreatenetworkinterfaceentity(_:_:_:_:))
- [func SCDynamicStoreKeyCreateNetworkServiceEntity(CFAllocator?, CFString, CFString, CFString?) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreatenetworkserviceentity(_:_:_:_:))
- [func SCDynamicStoreKeyCreateComputerName(CFAllocator?) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreatecomputername(_:))
- [func SCDynamicStoreKeyCreateConsoleUser(CFAllocator?) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreateconsoleuser(_:))
- [func SCDynamicStoreKeyCreateHostNames(CFAllocator?) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreatehostnames(_:))
- [func SCDynamicStoreKeyCreateLocation(CFAllocator?) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreatelocation(_:))
- [func SCDynamicStoreKeyCreateProxies(CFAllocator?) -> CFString](/documentation/systemconfiguration/scdynamicstorekeycreateproxies(_:))
- [SCNetwork](/documentation/systemconfiguration/scnetwork)

### Constants

- [SCNetworkConnectionFlags](/documentation/systemconfiguration/scnetworkconnectionflags)

#### Constants

- [var kSCNetworkFlagsTransientConnection: Int](/documentation/systemconfiguration/kscnetworkflagstransientconnection)
- [var kSCNetworkFlagsReachable: Int](/documentation/systemconfiguration/kscnetworkflagsreachable)
- [var kSCNetworkFlagsConnectionRequired: Int](/documentation/systemconfiguration/kscnetworkflagsconnectionrequired)
- [var kSCNetworkFlagsConnectionAutomatic: Int](/documentation/systemconfiguration/kscnetworkflagsconnectionautomatic)
- [var kSCNetworkFlagsInterventionRequired: Int](/documentation/systemconfiguration/kscnetworkflagsinterventionrequired)
- [var kSCNetworkFlagsIsLocalAddress: Int](/documentation/systemconfiguration/kscnetworkflagsislocaladdress)
- [var kSCNetworkFlagsIsDirect: Int](/documentation/systemconfiguration/kscnetworkflagsisdirect)
- [SCNetworkConfiguration](/documentation/systemconfiguration/scnetworkconfiguration)

### Configuring Ethernet Bond Interfaces

- [func SCBondInterfaceCopyAll(SCPreferences) -> CFArray](/documentation/systemconfiguration/scbondinterfacecopyall(_:))
- [func SCBondInterfaceCopyAvailableMemberInterfaces(SCPreferences) -> CFArray](/documentation/systemconfiguration/scbondinterfacecopyavailablememberinterfaces(_:))
- [func SCBondInterfaceCopyStatus(SCBondInterface) -> SCBondStatus?](/documentation/systemconfiguration/scbondinterfacecopystatus(_:))
- [func SCBondInterfaceCreate(SCPreferences) -> SCBondInterface?](/documentation/systemconfiguration/scbondinterfacecreate(_:))
- [func SCBondInterfaceGetMemberInterfaces(SCBondInterface) -> CFArray?](/documentation/systemconfiguration/scbondinterfacegetmemberinterfaces(_:))
- [func SCBondInterfaceGetOptions(SCBondInterface) -> CFDictionary?](/documentation/systemconfiguration/scbondinterfacegetoptions(_:))
- [func SCBondInterfaceRemove(SCBondInterface) -> Bool](/documentation/systemconfiguration/scbondinterfaceremove(_:))
- [func SCBondInterfaceSetLocalizedDisplayName(SCBondInterface, CFString) -> Bool](/documentation/systemconfiguration/scbondinterfacesetlocalizeddisplayname(_:_:))
- [func SCBondInterfaceSetMemberInterfaces(SCBondInterface, CFArray) -> Bool](/documentation/systemconfiguration/scbondinterfacesetmemberinterfaces(_:_:))
- [func SCBondInterfaceSetOptions(SCBondInterface, CFDictionary) -> Bool](/documentation/systemconfiguration/scbondinterfacesetoptions(_:_:))
- [func SCBondStatusGetInterfaceStatus(SCBondStatus, SCNetworkInterface?) -> CFDictionary?](/documentation/systemconfiguration/scbondstatusgetinterfacestatus(_:_:))
- [func SCBondStatusGetMemberInterfaces(SCBondStatus) -> CFArray?](/documentation/systemconfiguration/scbondstatusgetmemberinterfaces(_:))
- [func SCBondStatusGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scbondstatusgettypeid())

### Configuring Network Interfaces

- [func SCNetworkInterfaceCopyAll() -> CFArray](/documentation/systemconfiguration/scnetworkinterfacecopyall())
- [func SCNetworkInterfaceCopyMTU(SCNetworkInterface, UnsafeMutablePointer<Int32>?, UnsafeMutablePointer<Int32>?, UnsafeMutablePointer<Int32>?) -> Bool](/documentation/systemconfiguration/scnetworkinterfacecopymtu(_:_:_:_:))
- [func SCNetworkInterfaceCopyMediaOptions(SCNetworkInterface, UnsafeMutablePointer<Unmanaged<CFDictionary>?>?, UnsafeMutablePointer<Unmanaged<CFDictionary>?>?, UnsafeMutablePointer<Unmanaged<CFArray>?>?, Bool) -> Bool](/documentation/systemconfiguration/scnetworkinterfacecopymediaoptions(_:_:_:_:_:))
- [func SCNetworkInterfaceCopyMediaSubTypeOptions(CFArray, CFString) -> CFArray?](/documentation/systemconfiguration/scnetworkinterfacecopymediasubtypeoptions(_:_:))
- [func SCNetworkInterfaceCopyMediaSubTypes(CFArray) -> CFArray?](/documentation/systemconfiguration/scnetworkinterfacecopymediasubtypes(_:))
- [func SCNetworkInterfaceCreateWithInterface(SCNetworkInterface, CFString) -> SCNetworkInterface?](/documentation/systemconfiguration/scnetworkinterfacecreatewithinterface(_:_:))
- [func SCNetworkInterfaceForceConfigurationRefresh(SCNetworkInterface) -> Bool](/documentation/systemconfiguration/scnetworkinterfaceforceconfigurationrefresh(_:))
- [func SCNetworkInterfaceGetBSDName(SCNetworkInterface) -> CFString?](/documentation/systemconfiguration/scnetworkinterfacegetbsdname(_:))
- [func SCNetworkInterfaceGetConfiguration(SCNetworkInterface) -> CFDictionary?](/documentation/systemconfiguration/scnetworkinterfacegetconfiguration(_:))
- [func SCNetworkInterfaceGetExtendedConfiguration(SCNetworkInterface, CFString) -> CFDictionary?](/documentation/systemconfiguration/scnetworkinterfacegetextendedconfiguration(_:_:))
- [func SCNetworkInterfaceGetHardwareAddressString(SCNetworkInterface) -> CFString?](/documentation/systemconfiguration/scnetworkinterfacegethardwareaddressstring(_:))
- [func SCNetworkInterfaceGetInterface(SCNetworkInterface) -> SCNetworkInterface?](/documentation/systemconfiguration/scnetworkinterfacegetinterface(_:))
- [func SCNetworkInterfaceGetInterfaceType(SCNetworkInterface) -> CFString?](/documentation/systemconfiguration/scnetworkinterfacegetinterfacetype(_:))
- [func SCNetworkInterfaceGetLocalizedDisplayName(SCNetworkInterface) -> CFString?](/documentation/systemconfiguration/scnetworkinterfacegetlocalizeddisplayname(_:))
- [func SCNetworkInterfaceGetSupportedInterfaceTypes(SCNetworkInterface) -> CFArray?](/documentation/systemconfiguration/scnetworkinterfacegetsupportedinterfacetypes(_:))
- [func SCNetworkInterfaceGetSupportedProtocolTypes(SCNetworkInterface) -> CFArray?](/documentation/systemconfiguration/scnetworkinterfacegetsupportedprotocoltypes(_:))
- [func SCNetworkInterfaceGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scnetworkinterfacegettypeid())
- [func SCNetworkInterfaceSetConfiguration(SCNetworkInterface, CFDictionary?) -> Bool](/documentation/systemconfiguration/scnetworkinterfacesetconfiguration(_:_:))
- [func SCNetworkInterfaceSetExtendedConfiguration(SCNetworkInterface, CFString, CFDictionary?) -> Bool](/documentation/systemconfiguration/scnetworkinterfacesetextendedconfiguration(_:_:_:))
- [func SCNetworkInterfaceSetMTU(SCNetworkInterface, Int32) -> Bool](/documentation/systemconfiguration/scnetworkinterfacesetmtu(_:_:))
- [func SCNetworkInterfaceSetMediaOptions(SCNetworkInterface, CFString?, CFArray?) -> Bool](/documentation/systemconfiguration/scnetworkinterfacesetmediaoptions(_:_:_:))

### Configuring Network Protocols

- [func SCNetworkProtocolGetConfiguration(SCNetworkProtocol) -> CFDictionary?](/documentation/systemconfiguration/scnetworkprotocolgetconfiguration(_:))
- [func SCNetworkProtocolGetEnabled(SCNetworkProtocol) -> Bool](/documentation/systemconfiguration/scnetworkprotocolgetenabled(_:))
- [func SCNetworkProtocolGetProtocolType(SCNetworkProtocol) -> CFString?](/documentation/systemconfiguration/scnetworkprotocolgetprotocoltype(_:))
- [func SCNetworkProtocolGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scnetworkprotocolgettypeid())
- [func SCNetworkProtocolSetConfiguration(SCNetworkProtocol, CFDictionary?) -> Bool](/documentation/systemconfiguration/scnetworkprotocolsetconfiguration(_:_:))
- [func SCNetworkProtocolSetEnabled(SCNetworkProtocol, Bool) -> Bool](/documentation/systemconfiguration/scnetworkprotocolsetenabled(_:_:))

### Configuring Network Services

- [func SCNetworkServiceAddProtocolType(SCNetworkService, CFString) -> Bool](/documentation/systemconfiguration/scnetworkserviceaddprotocoltype(_:_:))
- [func SCNetworkServiceCopy(SCPreferences, CFString) -> SCNetworkService?](/documentation/systemconfiguration/scnetworkservicecopy(_:_:))
- [func SCNetworkServiceCopyAll(SCPreferences) -> CFArray?](/documentation/systemconfiguration/scnetworkservicecopyall(_:))
- [func SCNetworkServiceCopyProtocol(SCNetworkService, CFString) -> SCNetworkProtocol?](/documentation/systemconfiguration/scnetworkservicecopyprotocol(_:_:))
- [func SCNetworkServiceCopyProtocols(SCNetworkService) -> CFArray?](/documentation/systemconfiguration/scnetworkservicecopyprotocols(_:))
- [func SCNetworkServiceCreate(SCPreferences, SCNetworkInterface) -> SCNetworkService?](/documentation/systemconfiguration/scnetworkservicecreate(_:_:))
- [func SCNetworkServiceEstablishDefaultConfiguration(SCNetworkService) -> Bool](/documentation/systemconfiguration/scnetworkserviceestablishdefaultconfiguration(_:))
- [func SCNetworkServiceGetEnabled(SCNetworkService) -> Bool](/documentation/systemconfiguration/scnetworkservicegetenabled(_:))
- [func SCNetworkServiceGetInterface(SCNetworkService) -> SCNetworkInterface?](/documentation/systemconfiguration/scnetworkservicegetinterface(_:))
- [func SCNetworkServiceGetName(SCNetworkService) -> CFString?](/documentation/systemconfiguration/scnetworkservicegetname(_:))
- [func SCNetworkServiceGetServiceID(SCNetworkService) -> CFString?](/documentation/systemconfiguration/scnetworkservicegetserviceid(_:))
- [func SCNetworkServiceGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scnetworkservicegettypeid())
- [func SCNetworkServiceRemove(SCNetworkService) -> Bool](/documentation/systemconfiguration/scnetworkserviceremove(_:))
- [func SCNetworkServiceRemoveProtocolType(SCNetworkService, CFString) -> Bool](/documentation/systemconfiguration/scnetworkserviceremoveprotocoltype(_:_:))
- [func SCNetworkServiceSetEnabled(SCNetworkService, Bool) -> Bool](/documentation/systemconfiguration/scnetworkservicesetenabled(_:_:))
- [func SCNetworkServiceSetName(SCNetworkService, CFString?) -> Bool](/documentation/systemconfiguration/scnetworkservicesetname(_:_:))

### Configuring Network Sets

- [func SCNetworkSetAddService(SCNetworkSet, SCNetworkService) -> Bool](/documentation/systemconfiguration/scnetworksetaddservice(_:_:))
- [func SCNetworkSetContainsInterface(SCNetworkSet, SCNetworkInterface) -> Bool](/documentation/systemconfiguration/scnetworksetcontainsinterface(_:_:))
- [func SCNetworkSetCopy(SCPreferences, CFString) -> SCNetworkSet?](/documentation/systemconfiguration/scnetworksetcopy(_:_:))
- [func SCNetworkSetCopyAll(SCPreferences) -> CFArray?](/documentation/systemconfiguration/scnetworksetcopyall(_:))
- [func SCNetworkSetCopyCurrent(SCPreferences) -> SCNetworkSet?](/documentation/systemconfiguration/scnetworksetcopycurrent(_:))
- [func SCNetworkSetCopyServices(SCNetworkSet) -> CFArray?](/documentation/systemconfiguration/scnetworksetcopyservices(_:))
- [func SCNetworkSetCreate(SCPreferences) -> SCNetworkSet?](/documentation/systemconfiguration/scnetworksetcreate(_:))
- [func SCNetworkSetGetName(SCNetworkSet) -> CFString?](/documentation/systemconfiguration/scnetworksetgetname(_:))
- [func SCNetworkSetGetServiceOrder(SCNetworkSet) -> CFArray?](/documentation/systemconfiguration/scnetworksetgetserviceorder(_:))
- [func SCNetworkSetGetSetID(SCNetworkSet) -> CFString?](/documentation/systemconfiguration/scnetworksetgetsetid(_:))
- [func SCNetworkSetGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scnetworksetgettypeid())
- [func SCNetworkSetRemove(SCNetworkSet) -> Bool](/documentation/systemconfiguration/scnetworksetremove(_:))
- [func SCNetworkSetRemoveService(SCNetworkSet, SCNetworkService) -> Bool](/documentation/systemconfiguration/scnetworksetremoveservice(_:_:))
- [func SCNetworkSetSetCurrent(SCNetworkSet) -> Bool](/documentation/systemconfiguration/scnetworksetsetcurrent(_:))
- [func SCNetworkSetSetName(SCNetworkSet, CFString?) -> Bool](/documentation/systemconfiguration/scnetworksetsetname(_:_:))
- [func SCNetworkSetSetServiceOrder(SCNetworkSet, CFArray) -> Bool](/documentation/systemconfiguration/scnetworksetsetserviceorder(_:_:))

### Configuring VLAN Interfaces

- [func SCVLANInterfaceCopyAll(SCPreferences) -> CFArray](/documentation/systemconfiguration/scvlaninterfacecopyall(_:))
- [func SCVLANInterfaceCopyAvailablePhysicalInterfaces() -> CFArray](/documentation/systemconfiguration/scvlaninterfacecopyavailablephysicalinterfaces())
- [func SCVLANInterfaceCreate(SCPreferences, SCNetworkInterface, CFNumber) -> SCVLANInterface?](/documentation/systemconfiguration/scvlaninterfacecreate(_:_:_:))
- [func SCVLANInterfaceGetOptions(SCVLANInterface) -> CFDictionary?](/documentation/systemconfiguration/scvlaninterfacegetoptions(_:))
- [func SCVLANInterfaceGetPhysicalInterface(SCVLANInterface) -> SCNetworkInterface?](/documentation/systemconfiguration/scvlaninterfacegetphysicalinterface(_:))
- [func SCVLANInterfaceGetTag(SCVLANInterface) -> CFNumber?](/documentation/systemconfiguration/scvlaninterfacegettag(_:))
- [func SCVLANInterfaceRemove(SCVLANInterface) -> Bool](/documentation/systemconfiguration/scvlaninterfaceremove(_:))
- [func SCVLANInterfaceSetLocalizedDisplayName(SCVLANInterface, CFString) -> Bool](/documentation/systemconfiguration/scvlaninterfacesetlocalizeddisplayname(_:_:))
- [func SCVLANInterfaceSetOptions(SCVLANInterface, CFDictionary) -> Bool](/documentation/systemconfiguration/scvlaninterfacesetoptions(_:_:))
- [func SCVLANInterfaceSetPhysicalInterfaceAndTag(SCVLANInterface, SCNetworkInterface, CFNumber) -> Bool](/documentation/systemconfiguration/scvlaninterfacesetphysicalinterfaceandtag(_:_:_:))

### Data Types

- [SCNetworkInterface](/documentation/systemconfiguration/scnetworkinterface)
- [SCBondInterface](/documentation/systemconfiguration/scbondinterface)
- [SCBondStatus](/documentation/systemconfiguration/scbondstatus)
- [SCVLANInterface](/documentation/systemconfiguration/scvlaninterface)
- [SCNetworkProtocol](/documentation/systemconfiguration/scnetworkprotocol)
- [SCNetworkService](/documentation/systemconfiguration/scnetworkservice)
- [SCNetworkSet](/documentation/systemconfiguration/scnetworkset)

### Constants

- [Ethernet Bond Aggregation Status](/documentation/systemconfiguration/1546981-ethernet-bond-aggregation-status)

#### Constants

- [var kSCBondStatusOK: Int](/documentation/systemconfiguration/kscbondstatusok)
- [var kSCBondStatusLinkInvalid: Int](/documentation/systemconfiguration/kscbondstatuslinkinvalid)
- [var kSCBondStatusNoPartner: Int](/documentation/systemconfiguration/kscbondstatusnopartner)
- [var kSCBondStatusNotInActiveGroup: Int](/documentation/systemconfiguration/kscbondstatusnotinactivegroup)
- [var kSCBondStatusUnknown: Int](/documentation/systemconfiguration/kscbondstatusunknown)
- [Ethernet Bond Status Constants](/documentation/systemconfiguration/ethernet-bond-status-constants)

#### Constants

- [let kSCBondStatusDeviceAggregationStatus: CFString](/documentation/systemconfiguration/kscbondstatusdeviceaggregationstatus)
- [let kSCBondStatusDeviceCollecting: CFString](/documentation/systemconfiguration/kscbondstatusdevicecollecting)
- [let kSCBondStatusDeviceDistributing: CFString](/documentation/systemconfiguration/kscbondstatusdevicedistributing)
- [Network Interface Types](/documentation/systemconfiguration/network-interface-types)

#### Constants

- [let kSCNetworkInterfaceType6to4: CFString](/documentation/systemconfiguration/kscnetworkinterfacetype6to4)
- [let kSCNetworkInterfaceTypeBluetooth: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypebluetooth)
- [let kSCNetworkInterfaceTypeBond: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypebond)
- [let kSCNetworkInterfaceTypeEthernet: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypeethernet)
- [let kSCNetworkInterfaceTypeFireWire: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypefirewire)
- [let kSCNetworkInterfaceTypeIEEE80211: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypeieee80211)
- [let kSCNetworkInterfaceTypeIPSec: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypeipsec)
- [let kSCNetworkInterfaceTypeIrDA: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypeirda)
- [let kSCNetworkInterfaceTypeL2TP: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypel2tp)
- [let kSCNetworkInterfaceTypeModem: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypemodem)
- [let kSCNetworkInterfaceTypePPP: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypeppp)
- [let kSCNetworkInterfaceTypePPTP: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypepptp)
- [let kSCNetworkInterfaceTypeSerial: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypeserial)
- [let kSCNetworkInterfaceTypeVLAN: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypevlan)
- [let kSCNetworkInterfaceTypeWWAN: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypewwan)
- [let kSCNetworkInterfaceTypeIPv4: CFString](/documentation/systemconfiguration/kscnetworkinterfacetypeipv4)
- [let kSCNetworkInterfaceIPv4: SCNetworkInterface](/documentation/systemconfiguration/kscnetworkinterfaceipv4)
- [Network Protocol Types](/documentation/systemconfiguration/network-protocol-types)

#### Constants

- [let kSCNetworkProtocolTypeDNS: CFString](/documentation/systemconfiguration/kscnetworkprotocoltypedns)
- [let kSCNetworkProtocolTypeIPv4: CFString](/documentation/systemconfiguration/kscnetworkprotocoltypeipv4)
- [let kSCNetworkProtocolTypeIPv6: CFString](/documentation/systemconfiguration/kscnetworkprotocoltypeipv6)
- [let kSCNetworkProtocolTypeProxies: CFString](/documentation/systemconfiguration/kscnetworkprotocoltypeproxies)
- [let kSCNetworkProtocolTypeSMB: CFString](/documentation/systemconfiguration/kscnetworkprotocoltypesmb)
- [SCNetworkConnection](/documentation/systemconfiguration/scnetworkconnection-g7e)

### Getting Connection-Status Information

- [func SCNetworkConnectionGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scnetworkconnectiongettypeid())
- [func SCNetworkConnectionCopyUserPreferences(CFDictionary?, UnsafeMutablePointer<Unmanaged<CFString>?>, UnsafeMutablePointer<Unmanaged<CFDictionary>?>) -> Bool](/documentation/systemconfiguration/scnetworkconnectioncopyuserpreferences(_:_:_:))
- [func SCNetworkConnectionCopyServiceID(SCNetworkConnection) -> CFString?](/documentation/systemconfiguration/scnetworkconnectioncopyserviceid(_:))
- [func SCNetworkConnectionGetStatus(SCNetworkConnection) -> SCNetworkConnectionStatus](/documentation/systemconfiguration/scnetworkconnectiongetstatus(_:))
- [func SCNetworkConnectionCopyExtendedStatus(SCNetworkConnection) -> CFDictionary?](/documentation/systemconfiguration/scnetworkconnectioncopyextendedstatus(_:))
- [func SCNetworkConnectionCopyStatistics(SCNetworkConnection) -> CFDictionary?](/documentation/systemconfiguration/scnetworkconnectioncopystatistics(_:))
- [func SCNetworkConnectionCopyUserOptions(SCNetworkConnection) -> CFDictionary?](/documentation/systemconfiguration/scnetworkconnectioncopyuseroptions(_:))

### Starting and Stopping a Connection

- [func SCNetworkConnectionStart(SCNetworkConnection, CFDictionary?, Bool) -> Bool](/documentation/systemconfiguration/scnetworkconnectionstart(_:_:_:))
- [func SCNetworkConnectionStop(SCNetworkConnection, Bool) -> Bool](/documentation/systemconfiguration/scnetworkconnectionstop(_:_:))

### Scheduling a Connection Reference on a Run Loop

- [func SCNetworkConnectionScheduleWithRunLoop(SCNetworkConnection, CFRunLoop, CFString) -> Bool](/documentation/systemconfiguration/scnetworkconnectionschedulewithrunloop(_:_:_:))
- [func SCNetworkConnectionUnscheduleFromRunLoop(SCNetworkConnection, CFRunLoop, CFString) -> Bool](/documentation/systemconfiguration/scnetworkconnectionunschedulefromrunloop(_:_:_:))

### Creating a Connection Reference

- [func SCNetworkConnectionCreateWithServiceID(CFAllocator?, CFString, SCNetworkConnectionCallBack?, UnsafeMutablePointer<SCNetworkConnectionContext>?) -> SCNetworkConnection?](/documentation/systemconfiguration/scnetworkconnectioncreatewithserviceid(_:_:_:_:))

### Specifying a Dispatch Queue and Enabling Notifications

- [func SCNetworkConnectionSetDispatchQueue(SCNetworkConnection, dispatch_queue_t?) -> Bool](/documentation/systemconfiguration/scnetworkconnectionsetdispatchqueue(_:_:))

### Data Types

- [SCNetworkConnection](/documentation/systemconfiguration/scnetworkconnection)
- [SCNetworkConnectionCallBack](/documentation/systemconfiguration/scnetworkconnectioncallback)

#### Fields

- [connection](/documentation/systemconfiguration/1807883-connection)
- [status](/documentation/systemconfiguration/1807884-status)
- [SCNetworkConnectionContext](/documentation/systemconfiguration/scnetworkconnectioncontext)

#### Initializers

- [init()](/documentation/systemconfiguration/scnetworkconnectioncontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer?, retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?, release: ((UnsafeRawPointer) -> Void)?, copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?)](/documentation/systemconfiguration/scnetworkconnectioncontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?](/documentation/systemconfiguration/scnetworkconnectioncontext/copydescription)
- [var info: UnsafeMutableRawPointer?](/documentation/systemconfiguration/scnetworkconnectioncontext/info)
- [var release: ((UnsafeRawPointer) -> Void)?](/documentation/systemconfiguration/scnetworkconnectioncontext/release)
- [var retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?](/documentation/systemconfiguration/scnetworkconnectioncontext/retain)
- [var version: CFIndex](/documentation/systemconfiguration/scnetworkconnectioncontext/version)

### Constants

- [SCNetworkConnectionStatus](/documentation/systemconfiguration/scnetworkconnectionstatus)

#### Constants

- [case invalid](/documentation/systemconfiguration/scnetworkconnectionstatus/invalid)
- [case disconnected](/documentation/systemconfiguration/scnetworkconnectionstatus/disconnected)
- [case connecting](/documentation/systemconfiguration/scnetworkconnectionstatus/connecting)
- [case connected](/documentation/systemconfiguration/scnetworkconnectionstatus/connected)
- [case disconnecting](/documentation/systemconfiguration/scnetworkconnectionstatus/disconnecting)

#### Initializers

- [init?(rawValue: Int32)](/documentation/systemconfiguration/scnetworkconnectionstatus/init(rawvalue:))
- [SCNetworkConnectionPPPStatus](/documentation/systemconfiguration/scnetworkconnectionpppstatus)

#### Constants

- [case disconnected](/documentation/systemconfiguration/scnetworkconnectionpppstatus/disconnected)
- [case initializing](/documentation/systemconfiguration/scnetworkconnectionpppstatus/initializing)
- [case connectingLink](/documentation/systemconfiguration/scnetworkconnectionpppstatus/connectinglink)
- [case dialOnTraffic](/documentation/systemconfiguration/scnetworkconnectionpppstatus/dialontraffic)
- [case negotiatingLink](/documentation/systemconfiguration/scnetworkconnectionpppstatus/negotiatinglink)
- [case authenticating](/documentation/systemconfiguration/scnetworkconnectionpppstatus/authenticating)
- [case waitingForCallBack](/documentation/systemconfiguration/scnetworkconnectionpppstatus/waitingforcallback)
- [case negotiatingNetwork](/documentation/systemconfiguration/scnetworkconnectionpppstatus/negotiatingnetwork)
- [case connected](/documentation/systemconfiguration/scnetworkconnectionpppstatus/connected)
- [case terminating](/documentation/systemconfiguration/scnetworkconnectionpppstatus/terminating)
- [case disconnectingLink](/documentation/systemconfiguration/scnetworkconnectionpppstatus/disconnectinglink)
- [case holdingLinkOff](/documentation/systemconfiguration/scnetworkconnectionpppstatus/holdinglinkoff)
- [case suspended](/documentation/systemconfiguration/scnetworkconnectionpppstatus/suspended)
- [case waitingForRedial](/documentation/systemconfiguration/scnetworkconnectionpppstatus/waitingforredial)

#### Initializers

- [init?(rawValue: Int32)](/documentation/systemconfiguration/scnetworkconnectionpppstatus/init(rawvalue:))
- [Statistics Dictionary Keys](/documentation/systemconfiguration/statistics-dictionary-keys)

#### Constants

- [var kSCNetworkConnectionBytesIn: String](/documentation/systemconfiguration/kscnetworkconnectionbytesin)
- [var kSCNetworkConnectionBytesOut: String](/documentation/systemconfiguration/kscnetworkconnectionbytesout)
- [var kSCNetworkConnectionPacketsIn: String](/documentation/systemconfiguration/kscnetworkconnectionpacketsin)
- [var kSCNetworkConnectionPacketsOut: String](/documentation/systemconfiguration/kscnetworkconnectionpacketsout)
- [var kSCNetworkConnectionErrorsIn: String](/documentation/systemconfiguration/kscnetworkconnectionerrorsin)
- [var kSCNetworkConnectionErrorsOut: String](/documentation/systemconfiguration/kscnetworkconnectionerrorsout)
- [Selection Options Dictionary Keys](/documentation/systemconfiguration/selection-options-dictionary-keys)

#### Constants

- [var kSCNetworkConnectionSelectionOptionOnDemandHostName: String](/documentation/systemconfiguration/kscnetworkconnectionselectionoptionondemandhostname)
- [var kSCNetworkConnectionSelectionOptionOnDemandRetry: String](/documentation/systemconfiguration/kscnetworkconnectionselectionoptionondemandretry)
- [SCNetworkReachability](/documentation/systemconfiguration/scnetworkreachability-g7d)

### Creating a Reachability Reference

- [func SCNetworkReachabilityCreateWithAddress(CFAllocator?, UnsafePointer<sockaddr>) -> SCNetworkReachability?](/documentation/systemconfiguration/scnetworkreachabilitycreatewithaddress(_:_:))
- [func SCNetworkReachabilityCreateWithAddressPair(CFAllocator?, UnsafePointer<sockaddr>?, UnsafePointer<sockaddr>?) -> SCNetworkReachability?](/documentation/systemconfiguration/scnetworkreachabilitycreatewithaddresspair(_:_:_:))
- [func SCNetworkReachabilityCreateWithName(CFAllocator?, UnsafePointer<CChar>) -> SCNetworkReachability?](/documentation/systemconfiguration/scnetworkreachabilitycreatewithname(_:_:))

### Determining Reachability Status

- [func SCNetworkReachabilityGetFlags(SCNetworkReachability, UnsafeMutablePointer<SCNetworkReachabilityFlags>) -> Bool](/documentation/systemconfiguration/scnetworkreachabilitygetflags(_:_:))

### Preparing to Determine Reachability

- [func SCNetworkReachabilityGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scnetworkreachabilitygettypeid())
- [func SCNetworkReachabilitySetCallback(SCNetworkReachability, SCNetworkReachabilityCallBack?, UnsafeMutablePointer<SCNetworkReachabilityContext>?) -> Bool](/documentation/systemconfiguration/scnetworkreachabilitysetcallback(_:_:_:))
- [func SCNetworkReachabilityScheduleWithRunLoop(SCNetworkReachability, CFRunLoop, CFString) -> Bool](/documentation/systemconfiguration/scnetworkreachabilityschedulewithrunloop(_:_:_:))
- [func SCNetworkReachabilityUnscheduleFromRunLoop(SCNetworkReachability, CFRunLoop, CFString) -> Bool](/documentation/systemconfiguration/scnetworkreachabilityunschedulefromrunloop(_:_:_:))
- [func SCNetworkReachabilitySetDispatchQueue(SCNetworkReachability, dispatch_queue_t?) -> Bool](/documentation/systemconfiguration/scnetworkreachabilitysetdispatchqueue(_:_:))

### Callbacks

- [SCNetworkReachabilityCallBack](/documentation/systemconfiguration/scnetworkreachabilitycallback)

### Data Types

- [SCNetworkReachability](/documentation/systemconfiguration/scnetworkreachability)
- [SCNetworkReachabilityContext](/documentation/systemconfiguration/scnetworkreachabilitycontext)

#### Initializers

- [init()](/documentation/systemconfiguration/scnetworkreachabilitycontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer?, retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?, release: ((UnsafeRawPointer) -> Void)?, copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?)](/documentation/systemconfiguration/scnetworkreachabilitycontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?](/documentation/systemconfiguration/scnetworkreachabilitycontext/copydescription)
- [var info: UnsafeMutableRawPointer?](/documentation/systemconfiguration/scnetworkreachabilitycontext/info)
- [var release: ((UnsafeRawPointer) -> Void)?](/documentation/systemconfiguration/scnetworkreachabilitycontext/release)
- [var retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?](/documentation/systemconfiguration/scnetworkreachabilitycontext/retain)
- [var version: CFIndex](/documentation/systemconfiguration/scnetworkreachabilitycontext/version)

### Constants

- [SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags)

#### Constants

- [static var transientConnection: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/transientconnection)
- [static var reachable: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/reachable)
- [static var connectionRequired: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/connectionrequired)
- [static var connectionOnTraffic: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/connectionontraffic)
- [static var interventionRequired: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/interventionrequired)
- [static var connectionOnDemand: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/connectionondemand)
- [static var isLocalAddress: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/islocaladdress)
- [static var isDirect: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/isdirect)
- [static var isWWAN: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/iswwan)
- [static var connectionAutomatic: SCNetworkReachabilityFlags](/documentation/systemconfiguration/scnetworkreachabilityflags/connectionautomatic)

#### Initializers

- [init(rawValue: UInt32)](/documentation/systemconfiguration/scnetworkreachabilityflags/init(rawvalue:))
- [SCPreferences](/documentation/systemconfiguration/scpreferences-ft8)

### Creating a Preferences Session

- [func SCPreferencesCreate(CFAllocator?, CFString, CFString?) -> SCPreferences?](/documentation/systemconfiguration/scpreferencescreate(_:_:_:))
- [func SCPreferencesCreateWithAuthorization(CFAllocator?, CFString, CFString?, AuthorizationRef?) -> SCPreferences?](/documentation/systemconfiguration/scpreferencescreatewithauthorization(_:_:_:_:))

### Getting Information About a Preferences Session

- [func SCPreferencesGetTypeID() -> CFTypeID](/documentation/systemconfiguration/scpreferencesgettypeid())
- [func SCPreferencesCopyKeyList(SCPreferences) -> CFArray?](/documentation/systemconfiguration/scpreferencescopykeylist(_:))
- [func SCPreferencesGetSignature(SCPreferences) -> CFData?](/documentation/systemconfiguration/scpreferencesgetsignature(_:))

### Adding, Getting, and Removing Values

- [func SCPreferencesAddValue(SCPreferences, CFString, CFPropertyList) -> Bool](/documentation/systemconfiguration/scpreferencesaddvalue(_:_:_:))
- [func SCPreferencesGetValue(SCPreferences, CFString) -> CFPropertyList?](/documentation/systemconfiguration/scpreferencesgetvalue(_:_:))
- [func SCPreferencesSetValue(SCPreferences, CFString, CFPropertyList) -> Bool](/documentation/systemconfiguration/scpreferencessetvalue(_:_:_:))
- [func SCPreferencesRemoveValue(SCPreferences, CFString) -> Bool](/documentation/systemconfiguration/scpreferencesremovevalue(_:_:))

### Applying and Committing Changes

- [func SCPreferencesApplyChanges(SCPreferences) -> Bool](/documentation/systemconfiguration/scpreferencesapplychanges(_:))
- [func SCPreferencesCommitChanges(SCPreferences) -> Bool](/documentation/systemconfiguration/scpreferencescommitchanges(_:))
- [func SCPreferencesSynchronize(SCPreferences)](/documentation/systemconfiguration/scpreferencessynchronize(_:))

### Managing Notifications and Callbacks

- [func SCPreferencesSetCallback(SCPreferences, SCPreferencesCallBack?, UnsafeMutablePointer<SCPreferencesContext>?) -> Bool](/documentation/systemconfiguration/scpreferencessetcallback(_:_:_:))
- [func SCPreferencesScheduleWithRunLoop(SCPreferences, CFRunLoop, CFString) -> Bool](/documentation/systemconfiguration/scpreferencesschedulewithrunloop(_:_:_:))
- [func SCPreferencesUnscheduleFromRunLoop(SCPreferences, CFRunLoop, CFString) -> Bool](/documentation/systemconfiguration/scpreferencesunschedulefromrunloop(_:_:_:))
- [func SCPreferencesSetDispatchQueue(SCPreferences, dispatch_queue_t?) -> Bool](/documentation/systemconfiguration/scpreferencessetdispatchqueue(_:_:))

### Managing Access to a Preferences Session

- [func SCPreferencesLock(SCPreferences, Bool) -> Bool](/documentation/systemconfiguration/scpreferenceslock(_:_:))
- [func SCPreferencesUnlock(SCPreferences) -> Bool](/documentation/systemconfiguration/scpreferencesunlock(_:))

### Data Types

- [SCPreferences](/documentation/systemconfiguration/scpreferences)
- [SCPreferencesContext](/documentation/systemconfiguration/scpreferencescontext)

#### Initializers

- [init()](/documentation/systemconfiguration/scpreferencescontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer?, retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?, release: ((UnsafeRawPointer) -> Void)?, copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?)](/documentation/systemconfiguration/scpreferencescontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer) -> Unmanaged<CFString>)?](/documentation/systemconfiguration/scpreferencescontext/copydescription)
- [var info: UnsafeMutableRawPointer?](/documentation/systemconfiguration/scpreferencescontext/info)
- [var release: ((UnsafeRawPointer) -> Void)?](/documentation/systemconfiguration/scpreferencescontext/release)
- [var retain: ((UnsafeRawPointer) -> UnsafeRawPointer)?](/documentation/systemconfiguration/scpreferencescontext/retain)
- [var version: CFIndex](/documentation/systemconfiguration/scpreferencescontext/version)
- [SCPreferencesCallBack](/documentation/systemconfiguration/scpreferencescallback)

#### Fields

- [prefs](/documentation/systemconfiguration/1808420-prefs)
- [notificationType](/documentation/systemconfiguration/1808421-notificationtype)

### Constants

- [SCPreferencesNotification](/documentation/systemconfiguration/scpreferencesnotification)

#### Constants

- [static var commit: SCPreferencesNotification](/documentation/systemconfiguration/scpreferencesnotification/commit)
- [static var apply: SCPreferencesNotification](/documentation/systemconfiguration/scpreferencesnotification/apply)

#### Initializers

- [init(rawValue: UInt32)](/documentation/systemconfiguration/scpreferencesnotification/init(rawvalue:))
- [SCPreferencesPath](/documentation/systemconfiguration/scpreferencespath)

### Creating a New Path

- [func SCPreferencesPathCreateUniqueChild(SCPreferences, CFString) -> CFString?](/documentation/systemconfiguration/scpreferencespathcreateuniquechild(_:_:))

### Associating Information with a Path

- [func SCPreferencesPathSetValue(SCPreferences, CFString, CFDictionary) -> Bool](/documentation/systemconfiguration/scpreferencespathsetvalue(_:_:_:))
- [func SCPreferencesPathSetLink(SCPreferences, CFString, CFString) -> Bool](/documentation/systemconfiguration/scpreferencespathsetlink(_:_:_:))

### Getting or Removing Information Associated with a Path

- [func SCPreferencesPathGetValue(SCPreferences, CFString) -> CFDictionary?](/documentation/systemconfiguration/scpreferencespathgetvalue(_:_:))
- [func SCPreferencesPathGetLink(SCPreferences, CFString) -> CFString?](/documentation/systemconfiguration/scpreferencespathgetlink(_:_:))
- [func SCPreferencesPathRemoveValue(SCPreferences, CFString) -> Bool](/documentation/systemconfiguration/scpreferencespathremovevalue(_:_:))
- [SCPreferencesSetSpecific](/documentation/systemconfiguration/scpreferencessetspecific)

### Setting Configuration Information

- [func SCPreferencesSetComputerName(SCPreferences, CFString?, CFStringEncoding) -> Bool](/documentation/systemconfiguration/scpreferencessetcomputername(_:_:_:))
- [func SCPreferencesSetLocalHostName(SCPreferences, CFString?) -> Bool](/documentation/systemconfiguration/scpreferencessetlocalhostname(_:_:))
- [SCSchemaDefinitions](/documentation/systemconfiguration/scschemadefinitions)

### Constants

- [Generic Keys](/documentation/systemconfiguration/generic-keys)

#### Constants

- [let kSCPropInterfaceName: CFString](/documentation/systemconfiguration/kscpropinterfacename-swift.var)
- [let kSCPropMACAddress: CFString](/documentation/systemconfiguration/kscpropmacaddress-swift.var)
- [let kSCPropUserDefinedName: CFString](/documentation/systemconfiguration/kscpropuserdefinedname-swift.var)
- [let kSCPropVersion: CFString](/documentation/systemconfiguration/kscpropversion-swift.var)
- [Preference Keys](/documentation/systemconfiguration/preference-keys)

#### Constants

- [let kSCPrefCurrentSet: CFString](/documentation/systemconfiguration/kscprefcurrentset-swift.var)
- [let kSCPrefNetworkServices: CFString](/documentation/systemconfiguration/kscprefnetworkservices-swift.var)
- [let kSCPrefSets: CFString](/documentation/systemconfiguration/kscprefsets-swift.var)
- [let kSCPrefSystem: CFString](/documentation/systemconfiguration/kscprefsystem-swift.var)
- [Component Keys](/documentation/systemconfiguration/component-keys)

#### Constants

- [let kSCCompNetwork: CFString](/documentation/systemconfiguration/ksccompnetwork-swift.var)
- [let kSCCompService: CFString](/documentation/systemconfiguration/ksccompservice-swift.var)
- [let kSCCompGlobal: CFString](/documentation/systemconfiguration/ksccompglobal-swift.var)
- [let kSCCompHostNames: CFString](/documentation/systemconfiguration/ksccomphostnames-swift.var)
- [let kSCCompInterface: CFString](/documentation/systemconfiguration/ksccompinterface-swift.var)
- [let kSCCompSystem: CFString](/documentation/systemconfiguration/ksccompsystem-swift.var)
- [let kSCCompUsers: CFString](/documentation/systemconfiguration/ksccompusers-swift.var)
- [let kSCCompAnyRegex: CFString](/documentation/systemconfiguration/ksccompanyregex-swift.var)
- [Network Dictionary Keys](/documentation/systemconfiguration/network-dictionary-keys)

#### Constants

- [let kSCPropNetOverridePrimary: CFString](/documentation/systemconfiguration/kscpropnetoverrideprimary-swift.var)
- [let kSCPropNetServiceOrder: CFString](/documentation/systemconfiguration/kscpropnetserviceorder-swift.var)
- [let kSCPropNetPPPOverridePrimary: CFString](/documentation/systemconfiguration/kscpropnetpppoverrideprimary-swift.var)
- [Interface Dictionary Keys](/documentation/systemconfiguration/interface-dictionary-keys)

#### Constants

- [let kSCPropNetInterfaces: CFString](/documentation/systemconfiguration/kscpropnetinterfaces-swift.var)
- [Hostnames Dictionary Keys](/documentation/systemconfiguration/hostnames-dictionary-keys)

#### Constants

- [let kSCPropNetLocalHostName: CFString](/documentation/systemconfiguration/kscpropnetlocalhostname-swift.var)
- [Network Entity Keys](/documentation/systemconfiguration/network-entity-keys)

#### Constants

- [let kSCEntNetAirPort: CFString](/documentation/systemconfiguration/kscentnetairport-swift.var)
- [let kSCEntNetDHCP: CFString](/documentation/systemconfiguration/kscentnetdhcp-swift.var)
- [let kSCEntNetDNS: CFString](/documentation/systemconfiguration/kscentnetdns-swift.var)
- [let kSCEntNetEthernet: CFString](/documentation/systemconfiguration/kscentnetethernet-swift.var)
- [let kSCEntNetFireWire: CFString](/documentation/systemconfiguration/kscentnetfirewire-swift.var)
- [let kSCEntNetInterface: CFString](/documentation/systemconfiguration/kscentnetinterface-swift.var)
- [let kSCEntNetIPSec: CFString](/documentation/systemconfiguration/kscentnetipsec-swift.var)
- [let kSCEntNetIPv4: CFString](/documentation/systemconfiguration/kscentnetipv4-swift.var)
- [let kSCEntNetIPv6: CFString](/documentation/systemconfiguration/kscentnetipv6-swift.var)
- [let kSCEntNetL2TP: CFString](/documentation/systemconfiguration/kscentnetl2tp-swift.var)
- [let kSCEntNetLink: CFString](/documentation/systemconfiguration/kscentnetlink-swift.var)
- [let kSCEntNetModem: CFString](/documentation/systemconfiguration/kscentnetmodem-swift.var)
- [let kSCEntNetPPP: CFString](/documentation/systemconfiguration/kscentnetppp-swift.var)
- [let kSCEntNetPPPoE: CFString](/documentation/systemconfiguration/kscentnetpppoe-swift.var)
- [let kSCEntNetPPPSerial: CFString](/documentation/systemconfiguration/kscentnetpppserial-swift.var)
- [let kSCEntNetPPTP: CFString](/documentation/systemconfiguration/kscentnetpptp-swift.var)
- [let kSCEntNetProxies: CFString](/documentation/systemconfiguration/kscentnetproxies-swift.var)
- [let kSCEntNetSMB: CFString](/documentation/systemconfiguration/kscentnetsmb-swift.var)
- [let kSCEntNet6to4: CFString](/documentation/systemconfiguration/kscentnet6to4-swift.var)
- [DNS Entity Keys](/documentation/systemconfiguration/dns-entity-keys)

#### Constants

- [let kSCPropNetDNSDomainName: CFString](/documentation/systemconfiguration/kscpropnetdnsdomainname-swift.var)
- [let kSCPropNetDNSOptions: CFString](/documentation/systemconfiguration/kscpropnetdnsoptions-swift.var)
- [let kSCPropNetDNSSearchDomains: CFString](/documentation/systemconfiguration/kscpropnetdnssearchdomains-swift.var)
- [let kSCPropNetDNSSearchOrder: CFString](/documentation/systemconfiguration/kscpropnetdnssearchorder-swift.var)
- [let kSCPropNetDNSServerAddresses: CFString](/documentation/systemconfiguration/kscpropnetdnsserveraddresses-swift.var)
- [let kSCPropNetDNSServerPort: CFString](/documentation/systemconfiguration/kscpropnetdnsserverport-swift.var)
- [let kSCPropNetDNSServerTimeout: CFString](/documentation/systemconfiguration/kscpropnetdnsservertimeout-swift.var)
- [let kSCPropNetDNSSortList: CFString](/documentation/systemconfiguration/kscpropnetdnssortlist-swift.var)
- [let kSCPropNetDNSSupplementalMatchDomains: CFString](/documentation/systemconfiguration/kscpropnetdnssupplementalmatchdomains-swift.var)
- [let kSCPropNetDNSSupplementalMatchOrders: CFString](/documentation/systemconfiguration/kscpropnetdnssupplementalmatchorders-swift.var)
- [Ethernet Entity Keys](/documentation/systemconfiguration/ethernet-entity-keys)

#### Constants

- [let kSCPropNetEthernetMediaSubType: CFString](/documentation/systemconfiguration/kscpropnetethernetmediasubtype-swift.var)
- [let kSCPropNetEthernetMediaOptions: CFString](/documentation/systemconfiguration/kscpropnetethernetmediaoptions-swift.var)
- [let kSCPropNetEthernetMTU: CFString](/documentation/systemconfiguration/kscpropnetethernetmtu-swift.var)
- [Interface Entity Keys](/documentation/systemconfiguration/interface-entity-keys)

#### Constants

- [let kSCPropNetInterfaceDeviceName: CFString](/documentation/systemconfiguration/kscpropnetinterfacedevicename-swift.var)
- [let kSCPropNetInterfaceHardware: CFString](/documentation/systemconfiguration/kscpropnetinterfacehardware-swift.var)
- [let kSCPropNetInterfaceType: CFString](/documentation/systemconfiguration/kscpropnetinterfacetype-swift.var)
- [let kSCPropNetInterfaceSubType: CFString](/documentation/systemconfiguration/kscpropnetinterfacesubtype-swift.var)
- [let kSCPropNetInterfaceSupportsModemOnHold: CFString](/documentation/systemconfiguration/kscpropnetinterfacesupportsmodemonhold-swift.var)

#### Interface Type Values

- [let kSCValNetInterfaceTypeEthernet: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypeethernet-swift.var)
- [let kSCValNetInterfaceTypeFireWire: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypefirewire-swift.var)
- [let kSCValNetInterfaceTypePPP: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypeppp-swift.var)
- [let kSCValNetInterfaceType6to4: CFString](/documentation/systemconfiguration/kscvalnetinterfacetype6to4-swift.var)
- [let kSCValNetInterfaceTypeIPSec: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypeipsec-swift.var)

#### Interface Subtype Values

- [let kSCValNetInterfaceSubTypePPPoE: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypepppoe-swift.var)
- [let kSCValNetInterfaceSubTypePPPSerial: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypepppserial-swift.var)
- [let kSCValNetInterfaceSubTypeL2TP: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypel2tp-swift.var)
- [let kSCValNetInterfaceSubTypePPTP: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypepptp-swift.var)
- [IPSec Entity Keys](/documentation/systemconfiguration/ipsec-entity-keys)

#### Constants

- [let kSCPropNetIPSecLocalIdentifier: CFString](/documentation/systemconfiguration/kscpropnetipseclocalidentifier-swift.var)
- [let kSCPropNetIPSecLocalIdentifierType: CFString](/documentation/systemconfiguration/kscpropnetipseclocalidentifiertype-swift.var)
- [let kSCPropNetIPSecAuthenticationMethod: CFString](/documentation/systemconfiguration/kscpropnetipsecauthenticationmethod-swift.var)
- [let kSCPropNetIPSecSharedSecret: CFString](/documentation/systemconfiguration/kscpropnetipsecsharedsecret-swift.var)
- [let kSCPropNetIPSecSharedSecretEncryption: CFString](/documentation/systemconfiguration/kscpropnetipsecsharedsecretencryption-swift.var)
- [let kSCPropNetIPSecLocalCertificate: CFString](/documentation/systemconfiguration/kscpropnetipseclocalcertificate-swift.var)
- [let kSCPropNetIPSecConnectTime: CFString](/documentation/systemconfiguration/kscpropnetipsecconnecttime-swift.var)
- [let kSCPropNetIPSecRemoteAddress: CFString](/documentation/systemconfiguration/kscpropnetipsecremoteaddress-swift.var)
- [let kSCPropNetIPSecStatus: CFString](/documentation/systemconfiguration/kscpropnetipsecstatus-swift.var)
- [let kSCPropNetIPSecXAuthEnabled: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthenabled-swift.var)
- [let kSCPropNetIPSecXAuthName: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthname-swift.var)
- [let kSCPropNetIPSecXAuthPassword: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthpassword-swift.var)
- [let kSCPropNetIPSecXAuthPasswordEncryption: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthpasswordencryption-swift.var)

#### Authentication Method Values

- [let kSCValNetIPSecAuthenticationMethodSharedSecret: CFString](/documentation/systemconfiguration/kscvalnetipsecauthenticationmethodsharedsecret-swift.var)
- [let kSCValNetIPSecAuthenticationMethodCertificate: CFString](/documentation/systemconfiguration/kscvalnetipsecauthenticationmethodcertificate-swift.var)
- [let kSCValNetIPSecAuthenticationMethodHybrid: CFString](/documentation/systemconfiguration/kscvalnetipsecauthenticationmethodhybrid-swift.var)

#### Local Identifier Type Values

- [let kSCValNetIPSecLocalIdentifierTypeKeyID: CFString](/documentation/systemconfiguration/kscvalnetipseclocalidentifiertypekeyid-swift.var)

#### IPSec Shared Secret Encryption Values

- [let kSCValNetIPSecSharedSecretEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetipsecsharedsecretencryptionkeychain-swift.var)

#### XAuth Password Encryption Values

- [let kSCValNetIPSecXAuthPasswordEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetipsecxauthpasswordencryptionkeychain-swift.var)
- [let kSCValNetIPSecXAuthPasswordEncryptionPrompt: CFString](/documentation/systemconfiguration/kscvalnetipsecxauthpasswordencryptionprompt-swift.var)
- [IPv4 Entity Keys](/documentation/systemconfiguration/ipv4-entity-keys)

#### Constants

- [let kSCPropNetIPv4Addresses: CFString](/documentation/systemconfiguration/kscpropnetipv4addresses-swift.var)
- [let kSCPropNetIPv4ConfigMethod: CFString](/documentation/systemconfiguration/kscpropnetipv4configmethod-swift.var)
- [let kSCPropNetIPv4DHCPClientID: CFString](/documentation/systemconfiguration/kscpropnetipv4dhcpclientid-swift.var)
- [let kSCPropNetIPv4Router: CFString](/documentation/systemconfiguration/kscpropnetipv4router-swift.var)
- [let kSCPropNetIPv4SubnetMasks: CFString](/documentation/systemconfiguration/kscpropnetipv4subnetmasks-swift.var)
- [let kSCPropNetIPv4DestAddresses: CFString](/documentation/systemconfiguration/kscpropnetipv4destaddresses-swift.var)
- [let kSCPropNetIPv4BroadcastAddresses: CFString](/documentation/systemconfiguration/kscpropnetipv4broadcastaddresses-swift.var)

#### IPv4 Configuration Method Values

- [let kSCValNetIPv4ConfigMethodAutomatic: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodautomatic-swift.var)
- [let kSCValNetIPv4ConfigMethodBOOTP: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodbootp-swift.var)
- [let kSCValNetIPv4ConfigMethodDHCP: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethoddhcp-swift.var)
- [let kSCValNetIPv4ConfigMethodINFORM: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodinform-swift.var)
- [let kSCValNetIPv4ConfigMethodLinkLocal: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodlinklocal-swift.var)
- [let kSCValNetIPv4ConfigMethodManual: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodmanual-swift.var)
- [let kSCValNetIPv4ConfigMethodPPP: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodppp-swift.var)
- [IPv6 Entity Keys](/documentation/systemconfiguration/ipv6-entity-keys)

#### Constants

- [let kSCPropNetIPv6Addresses: CFString](/documentation/systemconfiguration/kscpropnetipv6addresses-swift.var)
- [let kSCPropNetIPv6ConfigMethod: CFString](/documentation/systemconfiguration/kscpropnetipv6configmethod-swift.var)
- [let kSCPropNetIPv6DestAddresses: CFString](/documentation/systemconfiguration/kscpropnetipv6destaddresses-swift.var)
- [let kSCPropNetIPv6Flags: CFString](/documentation/systemconfiguration/kscpropnetipv6flags-swift.var)
- [let kSCPropNetIPv6PrefixLength: CFString](/documentation/systemconfiguration/kscpropnetipv6prefixlength-swift.var)
- [let kSCPropNetIPv6Router: CFString](/documentation/systemconfiguration/kscpropnetipv6router-swift.var)

#### IPv6 Configuration Method Values

- [let kSCValNetIPv6ConfigMethodAutomatic: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodautomatic-swift.var)
- [let kSCValNetIPv6ConfigMethodLinkLocal: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodlinklocal-swift.var)
- [let kSCValNetIPv6ConfigMethodManual: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodmanual-swift.var)
- [let kSCValNetIPv6ConfigMethodRouterAdvertisement: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodrouteradvertisement-swift.var)
- [let kSCValNetIPv6ConfigMethod6to4: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethod6to4-swift.var)
- [6to4 Entity Keys](/documentation/systemconfiguration/6to4-entity-keys)

#### Constants

- [let kSCPropNet6to4Relay: CFString](/documentation/systemconfiguration/kscpropnet6to4relay-swift.var)
- [Link Entity Keys](/documentation/systemconfiguration/link-entity-keys)

#### Constants

- [let kSCPropNetLinkActive: CFString](/documentation/systemconfiguration/kscpropnetlinkactive-swift.var)
- [let kSCPropNetLinkDetaching: CFString](/documentation/systemconfiguration/kscpropnetlinkdetaching-swift.var)
- [Modem Entity Keys](/documentation/systemconfiguration/modem-entity-keys)

#### Constants

- [let kSCPropNetModemAccessPointName: CFString](/documentation/systemconfiguration/kscpropnetmodemaccesspointname-swift.var)
- [let kSCPropNetModemConnectionPersonality: CFString](/documentation/systemconfiguration/kscpropnetmodemconnectionpersonality-swift.var)
- [let kSCPropNetModemConnectionScript: CFString](/documentation/systemconfiguration/kscpropnetmodemconnectionscript-swift.var)
- [let kSCPropNetModemConnectSpeed: CFString](/documentation/systemconfiguration/kscpropnetmodemconnectspeed-swift.var)
- [let kSCPropNetModemDataCompression: CFString](/documentation/systemconfiguration/kscpropnetmodemdatacompression-swift.var)
- [let kSCPropNetModemDeviceContextID: CFString](/documentation/systemconfiguration/kscpropnetmodemdevicecontextid-swift.var)
- [let kSCPropNetModemDeviceModel: CFString](/documentation/systemconfiguration/kscpropnetmodemdevicemodel-swift.var)
- [let kSCPropNetModemDeviceVendor: CFString](/documentation/systemconfiguration/kscpropnetmodemdevicevendor-swift.var)
- [let kSCPropNetModemDialMode: CFString](/documentation/systemconfiguration/kscpropnetmodemdialmode-swift.var)
- [let kSCPropNetModemErrorCorrection: CFString](/documentation/systemconfiguration/kscpropnetmodemerrorcorrection-swift.var)
- [let kSCPropNetModemHoldCallWaitingAudibleAlert: CFString](/documentation/systemconfiguration/kscpropnetmodemholdcallwaitingaudiblealert-swift.var)
- [let kSCPropNetModemHoldDisconnectOnAnswer: CFString](/documentation/systemconfiguration/kscpropnetmodemholddisconnectonanswer-swift.var)
- [let kSCPropNetModemHoldEnabled: CFString](/documentation/systemconfiguration/kscpropnetmodemholdenabled-swift.var)
- [let kSCPropNetModemHoldReminder: CFString](/documentation/systemconfiguration/kscpropnetmodemholdreminder-swift.var)
- [let kSCPropNetModemHoldReminderTime: CFString](/documentation/systemconfiguration/kscpropnetmodemholdremindertime-swift.var)
- [let kSCPropNetModemNote: CFString](/documentation/systemconfiguration/kscpropnetmodemnote-swift.var)
- [let kSCPropNetModemPulseDial: CFString](/documentation/systemconfiguration/kscpropnetmodempulsedial-swift.var)
- [let kSCPropNetModemSpeaker: CFString](/documentation/systemconfiguration/kscpropnetmodemspeaker-swift.var)
- [let kSCPropNetModemSpeed: CFString](/documentation/systemconfiguration/kscpropnetmodemspeed-swift.var)

#### Modem Dial Mode Values

- [let kSCValNetModemDialModeIgnoreDialTone: CFString](/documentation/systemconfiguration/kscvalnetmodemdialmodeignoredialtone-swift.var)
- [let kSCValNetModemDialModeManual: CFString](/documentation/systemconfiguration/kscvalnetmodemdialmodemanual-swift.var)
- [let kSCValNetModemDialModeWaitForDialTone: CFString](/documentation/systemconfiguration/kscvalnetmodemdialmodewaitfordialtone-swift.var)
- [PPP Entity Keys](/documentation/systemconfiguration/ppp-entity-keys)

#### Constants

- [let kSCPropNetPPPACSPEnabled: CFString](/documentation/systemconfiguration/kscpropnetpppacspenabled-swift.var)
- [let kSCPropNetPPPConnectTime: CFString](/documentation/systemconfiguration/kscpropnetpppconnecttime-swift.var)
- [let kSCPropNetPPPDeviceLastCause: CFString](/documentation/systemconfiguration/kscpropnetpppdevicelastcause-swift.var)
- [let kSCPropNetPPPDialOnDemand: CFString](/documentation/systemconfiguration/kscpropnetpppdialondemand-swift.var)
- [let kSCPropNetPPPDisconnectOnFastUserSwitch: CFString](/documentation/systemconfiguration/kscpropnetpppdisconnectonfastuserswitch-swift.var)
- [let kSCPropNetPPPDisconnectOnIdle: CFString](/documentation/systemconfiguration/kscpropnetpppdisconnectonidle-swift.var)
- [let kSCPropNetPPPDisconnectOnIdleTimer: CFString](/documentation/systemconfiguration/kscpropnetpppdisconnectonidletimer-swift.var)
- [let kSCPropNetPPPDisconnectOnLogout: CFString](/documentation/systemconfiguration/kscpropnetpppdisconnectonlogout-swift.var)
- [let kSCPropNetPPPDisconnectOnSleep: CFString](/documentation/systemconfiguration/kscpropnetpppdisconnectonsleep-swift.var)
- [let kSCPropNetPPPDisconnectTime: CFString](/documentation/systemconfiguration/kscpropnetpppdisconnecttime-swift.var)
- [let kSCPropNetPPPIdleReminderTimer: CFString](/documentation/systemconfiguration/kscpropnetpppidleremindertimer-swift.var)
- [let kSCPropNetPPPIdleReminder: CFString](/documentation/systemconfiguration/kscpropnetpppidlereminder-swift.var)
- [let kSCPropNetPPPLastCause: CFString](/documentation/systemconfiguration/kscpropnetppplastcause-swift.var)
- [let kSCPropNetPPPLogfile: CFString](/documentation/systemconfiguration/kscpropnetppplogfile-swift.var)
- [let kSCPropNetPPPPlugins: CFString](/documentation/systemconfiguration/kscpropnetpppplugins-swift.var)
- [let kSCPropNetPPPRetryConnectTime: CFString](/documentation/systemconfiguration/kscpropnetpppretryconnecttime-swift.var)
- [let kSCPropNetPPPSessionTimer: CFString](/documentation/systemconfiguration/kscpropnetpppsessiontimer-swift.var)
- [let kSCPropNetPPPStatus: CFString](/documentation/systemconfiguration/kscpropnetpppstatus-swift.var)
- [let kSCPropNetPPPUseSessionTimer: CFString](/documentation/systemconfiguration/kscpropnetpppusesessiontimer-swift.var)
- [let kSCPropNetPPPVerboseLogging: CFString](/documentation/systemconfiguration/kscpropnetpppverboselogging-swift.var)
- [let kSCPropNetPPPAuthEAPPlugins: CFString](/documentation/systemconfiguration/kscpropnetpppautheapplugins-swift.var)
- [let kSCPropNetPPPAuthName: CFString](/documentation/systemconfiguration/kscpropnetpppauthname-swift.var)
- [let kSCPropNetPPPAuthPassword: CFString](/documentation/systemconfiguration/kscpropnetpppauthpassword-swift.var)
- [let kSCPropNetPPPAuthPasswordEncryption: CFString](/documentation/systemconfiguration/kscpropnetpppauthpasswordencryption-swift.var)
- [let kSCPropNetPPPAuthPrompt: CFString](/documentation/systemconfiguration/kscpropnetpppauthprompt-swift.var)
- [let kSCPropNetPPPAuthProtocol: CFString](/documentation/systemconfiguration/kscpropnetpppauthprotocol-swift.var)
- [let kSCPropNetPPPCommAlternateRemoteAddress: CFString](/documentation/systemconfiguration/kscpropnetpppcommalternateremoteaddress-swift.var)
- [let kSCPropNetPPPCommConnectDelay: CFString](/documentation/systemconfiguration/kscpropnetpppcommconnectdelay-swift.var)
- [let kSCPropNetPPPCommDisplayTerminalWindow: CFString](/documentation/systemconfiguration/kscpropnetpppcommdisplayterminalwindow-swift.var)
- [let kSCPropNetPPPCommRedialCount: CFString](/documentation/systemconfiguration/kscpropnetpppcommredialcount-swift.var)
- [let kSCPropNetPPPCommRedialEnabled: CFString](/documentation/systemconfiguration/kscpropnetpppcommredialenabled-swift.var)
- [let kSCPropNetPPPCommRedialInterval: CFString](/documentation/systemconfiguration/kscpropnetpppcommredialinterval-swift.var)
- [let kSCPropNetPPPCommRemoteAddress: CFString](/documentation/systemconfiguration/kscpropnetpppcommremoteaddress-swift.var)
- [let kSCPropNetPPPCommTerminalScript: CFString](/documentation/systemconfiguration/kscpropnetpppcommterminalscript-swift.var)
- [let kSCPropNetPPPCommUseTerminalScript: CFString](/documentation/systemconfiguration/kscpropnetpppcommuseterminalscript-swift.var)
- [let kSCPropNetPPPCCPEnabled: CFString](/documentation/systemconfiguration/kscpropnetpppccpenabled-swift.var)
- [let kSCPropNetPPPCCPMPPE40Enabled: CFString](/documentation/systemconfiguration/kscpropnetpppccpmppe40enabled-swift.var)
- [let kSCPropNetPPPCCPMPPE128Enabled: CFString](/documentation/systemconfiguration/kscpropnetpppccpmppe128enabled-swift.var)
- [let kSCPropNetPPPIPCPCompressionVJ: CFString](/documentation/systemconfiguration/kscpropnetpppipcpcompressionvj-swift.var)
- [let kSCPropNetPPPIPCPUsePeerDNS: CFString](/documentation/systemconfiguration/kscpropnetpppipcpusepeerdns-swift.var)
- [let kSCPropNetPPPLCPEchoEnabled: CFString](/documentation/systemconfiguration/kscpropnetppplcpechoenabled-swift.var)
- [let kSCPropNetPPPLCPEchoFailure: CFString](/documentation/systemconfiguration/kscpropnetppplcpechofailure-swift.var)
- [let kSCPropNetPPPLCPEchoInterval: CFString](/documentation/systemconfiguration/kscpropnetppplcpechointerval-swift.var)
- [let kSCPropNetPPPLCPCompressionACField: CFString](/documentation/systemconfiguration/kscpropnetppplcpcompressionacfield-swift.var)
- [let kSCPropNetPPPLCPCompressionPField: CFString](/documentation/systemconfiguration/kscpropnetppplcpcompressionpfield-swift.var)
- [let kSCPropNetPPPLCPMRU: CFString](/documentation/systemconfiguration/kscpropnetppplcpmru-swift.var)
- [let kSCPropNetPPPLCPMTU: CFString](/documentation/systemconfiguration/kscpropnetppplcpmtu-swift.var)
- [let kSCPropNetPPPLCPReceiveACCM: CFString](/documentation/systemconfiguration/kscpropnetppplcpreceiveaccm-swift.var)
- [let kSCPropNetPPPLCPTransmitACCM: CFString](/documentation/systemconfiguration/kscpropnetppplcptransmitaccm-swift.var)

#### Password Encryption Values

- [let kSCValNetPPPAuthPasswordEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetpppauthpasswordencryptionkeychain-swift.var)
- [let kSCValNetPPPAuthPasswordEncryptionToken: CFString](/documentation/systemconfiguration/kscvalnetpppauthpasswordencryptiontoken-swift.var)

#### Prompt Values

- [let kSCValNetPPPAuthPromptBefore: CFString](/documentation/systemconfiguration/kscvalnetpppauthpromptbefore-swift.var)
- [let kSCValNetPPPAuthPromptAfter: CFString](/documentation/systemconfiguration/kscvalnetpppauthpromptafter-swift.var)

#### Protocol Values

- [let kSCValNetPPPAuthProtocolCHAP: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolchap-swift.var)
- [let kSCValNetPPPAuthProtocolEAP: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocoleap-swift.var)
- [let kSCValNetPPPAuthProtocolMSCHAP1: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolmschap1-swift.var)
- [let kSCValNetPPPAuthProtocolMSCHAP2: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolmschap2-swift.var)
- [let kSCValNetPPPAuthProtocolPAP: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolpap-swift.var)
- [L2TP Entity Keys](/documentation/systemconfiguration/l2tp-entity-keys)

#### Constants

- [let kSCPropNetL2TPIPSecSharedSecret: CFString](/documentation/systemconfiguration/kscpropnetl2tpipsecsharedsecret-swift.var)
- [let kSCPropNetL2TPIPSecSharedSecretEncryption: CFString](/documentation/systemconfiguration/kscpropnetl2tpipsecsharedsecretencryption-swift.var)
- [let kSCPropNetL2TPTransport: CFString](/documentation/systemconfiguration/kscpropnetl2tptransport-swift.var)

#### L2TP Shared Secret Encryption Values

- [let kSCValNetL2TPIPSecSharedSecretEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetl2tpipsecsharedsecretencryptionkeychain-swift.var)

#### Transport Values

- [let kSCValNetL2TPTransportIP: CFString](/documentation/systemconfiguration/kscvalnetl2tptransportip-swift.var)
- [let kSCValNetL2TPTransportIPSec: CFString](/documentation/systemconfiguration/kscvalnetl2tptransportipsec-swift.var)
- [Proxies Entity Keys](/documentation/systemconfiguration/proxies-entity-keys)

#### Constants

- [let kSCPropNetProxiesExceptionsList: CFString](/documentation/systemconfiguration/kscpropnetproxiesexceptionslist-swift.var)
- [let kSCPropNetProxiesExcludeSimpleHostnames: CFString](/documentation/systemconfiguration/kscpropnetproxiesexcludesimplehostnames-swift.var)
- [let kSCPropNetProxiesFTPEnable: CFString](/documentation/systemconfiguration/kscpropnetproxiesftpenable-swift.var)
- [let kSCPropNetProxiesFTPPassive: CFString](/documentation/systemconfiguration/kscpropnetproxiesftppassive-swift.var)
- [let kSCPropNetProxiesFTPPort: CFString](/documentation/systemconfiguration/kscpropnetproxiesftpport-swift.var)
- [let kSCPropNetProxiesFTPProxy: CFString](/documentation/systemconfiguration/kscpropnetproxiesftpproxy-swift.var)
- [let kSCPropNetProxiesGopherEnable: CFString](/documentation/systemconfiguration/kscpropnetproxiesgopherenable-swift.var)
- [let kSCPropNetProxiesGopherPort: CFString](/documentation/systemconfiguration/kscpropnetproxiesgopherport-swift.var)
- [let kSCPropNetProxiesGopherProxy: CFString](/documentation/systemconfiguration/kscpropnetproxiesgopherproxy-swift.var)
- [let kSCPropNetProxiesHTTPEnable: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpenable-swift.var)
- [let kSCPropNetProxiesHTTPPort: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpport-swift.var)
- [let kSCPropNetProxiesHTTPProxy: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpproxy-swift.var)
- [let kSCPropNetProxiesHTTPSEnable: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpsenable-swift.var)
- [let kSCPropNetProxiesHTTPSPort: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpsport-swift.var)
- [let kSCPropNetProxiesHTTPSProxy: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpsproxy-swift.var)
- [let kSCPropNetProxiesRTSPEnable: CFString](/documentation/systemconfiguration/kscpropnetproxiesrtspenable-swift.var)
- [let kSCPropNetProxiesRTSPPort: CFString](/documentation/systemconfiguration/kscpropnetproxiesrtspport-swift.var)
- [let kSCPropNetProxiesRTSPProxy: CFString](/documentation/systemconfiguration/kscpropnetproxiesrtspproxy-swift.var)
- [let kSCPropNetProxiesSOCKSEnable: CFString](/documentation/systemconfiguration/kscpropnetproxiessocksenable-swift.var)
- [let kSCPropNetProxiesSOCKSPort: CFString](/documentation/systemconfiguration/kscpropnetproxiessocksport-swift.var)
- [let kSCPropNetProxiesSOCKSProxy: CFString](/documentation/systemconfiguration/kscpropnetproxiessocksproxy-swift.var)
- [let kSCPropNetProxiesProxyAutoConfigEnable: CFString](/documentation/systemconfiguration/kscpropnetproxiesproxyautoconfigenable-swift.var)
- [let kSCPropNetProxiesProxyAutoConfigJavaScript: CFString](/documentation/systemconfiguration/kscpropnetproxiesproxyautoconfigjavascript-swift.var)
- [let kSCPropNetProxiesProxyAutoConfigURLString: CFString](/documentation/systemconfiguration/kscpropnetproxiesproxyautoconfigurlstring-swift.var)
- [let kSCPropNetProxiesProxyAutoDiscoveryEnable: CFString](/documentation/systemconfiguration/kscpropnetproxiesproxyautodiscoveryenable-swift.var)
- [SMB Entity Keys](/documentation/systemconfiguration/smb-entity-keys)

#### Constants

- [let kSCPropNetSMBNetBIOSName: CFString](/documentation/systemconfiguration/kscpropnetsmbnetbiosname-swift.var)
- [let kSCPropNetSMBNetBIOSNodeType: CFString](/documentation/systemconfiguration/kscpropnetsmbnetbiosnodetype-swift.var)
- [let kSCPropNetSMBWINSAddresses: CFString](/documentation/systemconfiguration/kscpropnetsmbwinsaddresses-swift.var)
- [let kSCPropNetSMBWorkgroup: CFString](/documentation/systemconfiguration/kscpropnetsmbworkgroup-swift.var)

#### NetBIOS Node Type Values

- [let kSCValNetSMBNetBIOSNodeTypeBroadcast: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypebroadcast-swift.var)
- [let kSCValNetSMBNetBIOSNodeTypePeer: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypepeer-swift.var)
- [let kSCValNetSMBNetBIOSNodeTypeMixed: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypemixed-swift.var)
- [let kSCValNetSMBNetBIOSNodeTypeHybrid: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypehybrid-swift.var)
- [CompUsers Entity Keys](/documentation/systemconfiguration/compusers-entity-keys)

#### Constants

- [let kSCEntUsersConsoleUser: CFString](/documentation/systemconfiguration/kscentusersconsoleuser-swift.var)
- [CompSystem Entity Keys](/documentation/systemconfiguration/compsystem-entity-keys)

#### Constants

- [let kSCPropSystemComputerName: CFString](/documentation/systemconfiguration/kscpropsystemcomputername-swift.var)
- [let kSCPropSystemComputerNameEncoding: CFString](/documentation/systemconfiguration/kscpropsystemcomputernameencoding-swift.var)
- [Dynamic Store Domain Prefixes](/documentation/systemconfiguration/dynamic-store-domain-prefixes)

#### Constants

- [let kSCDynamicStoreDomainFile: CFString](/documentation/systemconfiguration/kscdynamicstoredomainfile-swift.var)
- [let kSCDynamicStoreDomainPlugin: CFString](/documentation/systemconfiguration/kscdynamicstoredomainplugin-swift.var)
- [let kSCDynamicStoreDomainSetup: CFString](/documentation/systemconfiguration/kscdynamicstoredomainsetup-swift.var)
- [let kSCDynamicStoreDomainState: CFString](/documentation/systemconfiguration/kscdynamicstoredomainstate-swift.var)
- [let kSCDynamicStoreDomainPrefs: CFString](/documentation/systemconfiguration/kscdynamicstoredomainprefs-swift.var)
- [Dynamic Store Entity Keys](/documentation/systemconfiguration/dynamic-store-entity-keys)

#### Constants

- [let kSCDynamicStorePropSetupCurrentSet: CFString](/documentation/systemconfiguration/kscdynamicstorepropsetupcurrentset-swift.var)
- [let kSCDynamicStorePropSetupLastUpdated: CFString](/documentation/systemconfiguration/kscdynamicstorepropsetuplastupdated-swift.var)
- [let kSCDynamicStorePropNetInterfaces: CFString](/documentation/systemconfiguration/kscdynamicstorepropnetinterfaces-swift.var)
- [let kSCDynamicStorePropNetPrimaryInterface: CFString](/documentation/systemconfiguration/kscdynamicstorepropnetprimaryinterface-swift.var)
- [let kSCDynamicStorePropNetPrimaryService: CFString](/documentation/systemconfiguration/kscdynamicstorepropnetprimaryservice-swift.var)
- [let kSCDynamicStorePropNetServiceIDs: CFString](/documentation/systemconfiguration/kscdynamicstorepropnetserviceids-swift.var)
- [Reserved Keys](/documentation/systemconfiguration/reserved-keys)

#### Constants

- [let kSCResvLink: CFString](/documentation/systemconfiguration/kscresvlink-swift.var)
- [let kSCResvInactive: CFString](/documentation/systemconfiguration/kscresvinactive-swift.var)
- [System Configuration](/documentation/systemconfiguration/system-configuration)

### Functions

- [func SCCopyLastError() -> CFError](/documentation/systemconfiguration/sccopylasterror())
- [func SCError() -> Int32](/documentation/systemconfiguration/scerror())
- [func SCErrorString(Int32) -> UnsafePointer<CChar>](/documentation/systemconfiguration/scerrorstring(_:))

### Constants

- [Status and Error Codes](/documentation/systemconfiguration/1518026-status-and-error-codes)

#### Constants

- [var kSCStatusOK: Int](/documentation/systemconfiguration/kscstatusok)
- [var kSCStatusFailed: Int](/documentation/systemconfiguration/kscstatusfailed)
- [var kSCStatusInvalidArgument: Int](/documentation/systemconfiguration/kscstatusinvalidargument)
- [var kSCStatusAccessError: Int](/documentation/systemconfiguration/kscstatusaccesserror)
- [var kSCStatusNoKey: Int](/documentation/systemconfiguration/kscstatusnokey)
- [var kSCStatusKeyExists: Int](/documentation/systemconfiguration/kscstatuskeyexists)
- [var kSCStatusLocked: Int](/documentation/systemconfiguration/kscstatuslocked)
- [var kSCStatusNeedLock: Int](/documentation/systemconfiguration/kscstatusneedlock)
- [var kSCStatusNoStoreSession: Int](/documentation/systemconfiguration/kscstatusnostoresession)
- [var kSCStatusNoStoreServer: Int](/documentation/systemconfiguration/kscstatusnostoreserver)
- [var kSCStatusNotifierActive: Int](/documentation/systemconfiguration/kscstatusnotifieractive)
- [var kSCStatusNoPrefsSession: Int](/documentation/systemconfiguration/kscstatusnoprefssession)
- [var kSCStatusPrefsBusy: Int](/documentation/systemconfiguration/kscstatusprefsbusy)
- [var kSCStatusNoConfigFile: Int](/documentation/systemconfiguration/kscstatusnoconfigfile)
- [var kSCStatusNoLink: Int](/documentation/systemconfiguration/kscstatusnolink)
- [var kSCStatusStale: Int](/documentation/systemconfiguration/kscstatusstale)
- [var kSCStatusMaxLink: Int](/documentation/systemconfiguration/kscstatusmaxlink)
- [var kSCStatusReachabilityUnknown: Int](/documentation/systemconfiguration/kscstatusreachabilityunknown)
- [var kSCStatusConnectionNoService: Int](/documentation/systemconfiguration/kscstatusconnectionnoservice)
- [var kSCStatusConnectionIgnore: Int](/documentation/systemconfiguration/kscstatusconnectionignore)
- [Error Domain](/documentation/systemconfiguration/error-domain)

#### Constants

- [let kCFErrorDomainSystemConfiguration: CFString](/documentation/systemconfiguration/kcferrordomainsystemconfiguration)
- [SystemConfiguration Enumerations](/documentation/systemconfiguration/systemconfiguration-enumerations)

### Enumerations

- [Anonymous](/documentation/systemconfiguration/1420190-anonymous)

#### Constants

- [var kSCNetworkFlagsConnectionAutomatic: Int](/documentation/systemconfiguration/kscnetworkflagsconnectionautomatic)
- [var kSCNetworkFlagsConnectionRequired: Int](/documentation/systemconfiguration/kscnetworkflagsconnectionrequired)
- [var kSCNetworkFlagsInterventionRequired: Int](/documentation/systemconfiguration/kscnetworkflagsinterventionrequired)
- [var kSCNetworkFlagsIsDirect: Int](/documentation/systemconfiguration/kscnetworkflagsisdirect)
- [var kSCNetworkFlagsIsLocalAddress: Int](/documentation/systemconfiguration/kscnetworkflagsislocaladdress)
- [var kSCNetworkFlagsReachable: Int](/documentation/systemconfiguration/kscnetworkflagsreachable)
- [var kSCNetworkFlagsTransientConnection: Int](/documentation/systemconfiguration/kscnetworkflagstransientconnection)
- [SystemConfiguration Constants](/documentation/systemconfiguration/systemconfiguration-constants)

### Constants

- [let kSCCompAnyRegex: CFString](/documentation/systemconfiguration/ksccompanyregex-swift.var)
- [let kSCPropNetIPSecConnectTime: CFString](/documentation/systemconfiguration/kscpropnetipsecconnecttime-swift.var)
- [let kSCPropNetIPSecRemoteAddress: CFString](/documentation/systemconfiguration/kscpropnetipsecremoteaddress-swift.var)
- [let kSCPropNetIPSecStatus: CFString](/documentation/systemconfiguration/kscpropnetipsecstatus-swift.var)
- [let kSCPropNetIPSecXAuthEnabled: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthenabled-swift.var)
- [let kSCPropNetIPSecXAuthName: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthname-swift.var)
- [let kSCPropNetIPSecXAuthPassword: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthpassword-swift.var)
- [let kSCPropNetIPSecXAuthPasswordEncryption: CFString](/documentation/systemconfiguration/kscpropnetipsecxauthpasswordencryption-swift.var)
- [let kSCPropNetProxiesProxyAutoConfigJavaScript: CFString](/documentation/systemconfiguration/kscpropnetproxiesproxyautoconfigjavascript-swift.var)
- [let kSCResvInactive: CFString](/documentation/systemconfiguration/kscresvinactive-swift.var)
- [let kSCResvLink: CFString](/documentation/systemconfiguration/kscresvlink-swift.var)
- [let kSCValNetIPSecAuthenticationMethodCertificate: CFString](/documentation/systemconfiguration/kscvalnetipsecauthenticationmethodcertificate-swift.var)
- [let kSCValNetIPSecAuthenticationMethodHybrid: CFString](/documentation/systemconfiguration/kscvalnetipsecauthenticationmethodhybrid-swift.var)
- [let kSCValNetIPSecAuthenticationMethodSharedSecret: CFString](/documentation/systemconfiguration/kscvalnetipsecauthenticationmethodsharedsecret-swift.var)
- [let kSCValNetIPSecLocalIdentifierTypeKeyID: CFString](/documentation/systemconfiguration/kscvalnetipseclocalidentifiertypekeyid-swift.var)
- [let kSCValNetIPSecSharedSecretEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetipsecsharedsecretencryptionkeychain-swift.var)
- [let kSCValNetIPSecXAuthPasswordEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetipsecxauthpasswordencryptionkeychain-swift.var)
- [let kSCValNetIPSecXAuthPasswordEncryptionPrompt: CFString](/documentation/systemconfiguration/kscvalnetipsecxauthpasswordencryptionprompt-swift.var)
- [let kSCValNetIPv4ConfigMethodAutomatic: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodautomatic-swift.var)
- [let kSCValNetIPv4ConfigMethodBOOTP: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodbootp-swift.var)
- [let kSCValNetIPv4ConfigMethodDHCP: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethoddhcp-swift.var)
- [let kSCValNetIPv4ConfigMethodINFORM: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodinform-swift.var)
- [let kSCValNetIPv4ConfigMethodLinkLocal: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodlinklocal-swift.var)
- [let kSCValNetIPv4ConfigMethodManual: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodmanual-swift.var)
- [let kSCValNetIPv4ConfigMethodPPP: CFString](/documentation/systemconfiguration/kscvalnetipv4configmethodppp-swift.var)
- [let kSCValNetIPv6ConfigMethod6to4: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethod6to4-swift.var)
- [let kSCValNetIPv6ConfigMethodAutomatic: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodautomatic-swift.var)
- [let kSCValNetIPv6ConfigMethodLinkLocal: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodlinklocal-swift.var)
- [let kSCValNetIPv6ConfigMethodManual: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodmanual-swift.var)
- [let kSCValNetIPv6ConfigMethodRouterAdvertisement: CFString](/documentation/systemconfiguration/kscvalnetipv6configmethodrouteradvertisement-swift.var)
- [let kSCValNetInterfaceSubTypeL2TP: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypel2tp-swift.var)
- [let kSCValNetInterfaceSubTypePPPSerial: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypepppserial-swift.var)
- [let kSCValNetInterfaceSubTypePPPoE: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypepppoe-swift.var)
- [let kSCValNetInterfaceSubTypePPTP: CFString](/documentation/systemconfiguration/kscvalnetinterfacesubtypepptp-swift.var)
- [let kSCValNetInterfaceType6to4: CFString](/documentation/systemconfiguration/kscvalnetinterfacetype6to4-swift.var)
- [let kSCValNetInterfaceTypeEthernet: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypeethernet-swift.var)
- [let kSCValNetInterfaceTypeFireWire: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypefirewire-swift.var)
- [let kSCValNetInterfaceTypeIPSec: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypeipsec-swift.var)
- [let kSCValNetInterfaceTypePPP: CFString](/documentation/systemconfiguration/kscvalnetinterfacetypeppp-swift.var)
- [let kSCValNetL2TPIPSecSharedSecretEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetl2tpipsecsharedsecretencryptionkeychain-swift.var)
- [let kSCValNetL2TPTransportIP: CFString](/documentation/systemconfiguration/kscvalnetl2tptransportip-swift.var)
- [let kSCValNetL2TPTransportIPSec: CFString](/documentation/systemconfiguration/kscvalnetl2tptransportipsec-swift.var)
- [let kSCValNetModemDialModeIgnoreDialTone: CFString](/documentation/systemconfiguration/kscvalnetmodemdialmodeignoredialtone-swift.var)
- [let kSCValNetModemDialModeManual: CFString](/documentation/systemconfiguration/kscvalnetmodemdialmodemanual-swift.var)
- [let kSCValNetModemDialModeWaitForDialTone: CFString](/documentation/systemconfiguration/kscvalnetmodemdialmodewaitfordialtone-swift.var)
- [let kSCValNetPPPAuthPasswordEncryptionKeychain: CFString](/documentation/systemconfiguration/kscvalnetpppauthpasswordencryptionkeychain-swift.var)
- [let kSCValNetPPPAuthPasswordEncryptionToken: CFString](/documentation/systemconfiguration/kscvalnetpppauthpasswordencryptiontoken-swift.var)
- [let kSCValNetPPPAuthPromptAfter: CFString](/documentation/systemconfiguration/kscvalnetpppauthpromptafter-swift.var)
- [let kSCValNetPPPAuthPromptBefore: CFString](/documentation/systemconfiguration/kscvalnetpppauthpromptbefore-swift.var)
- [let kSCValNetPPPAuthProtocolCHAP: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolchap-swift.var)
- [let kSCValNetPPPAuthProtocolEAP: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocoleap-swift.var)
- [let kSCValNetPPPAuthProtocolMSCHAP1: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolmschap1-swift.var)
- [let kSCValNetPPPAuthProtocolMSCHAP2: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolmschap2-swift.var)
- [let kSCValNetPPPAuthProtocolPAP: CFString](/documentation/systemconfiguration/kscvalnetpppauthprotocolpap-swift.var)
- [let kSCValNetSMBNetBIOSNodeTypeBroadcast: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypebroadcast-swift.var)
- [let kSCValNetSMBNetBIOSNodeTypeHybrid: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypehybrid-swift.var)
- [let kSCValNetSMBNetBIOSNodeTypeMixed: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypemixed-swift.var)
- [let kSCValNetSMBNetBIOSNodeTypePeer: CFString](/documentation/systemconfiguration/kscvalnetsmbnetbiosnodetypepeer-swift.var)
- [let kSCPropNetProxiesFTPUser: CFString](/documentation/systemconfiguration/kscpropnetproxiesftpuser-swift.var)
- [let kSCPropNetProxiesGopherUser: CFString](/documentation/systemconfiguration/kscpropnetproxiesgopheruser-swift.var)
- [let kSCPropNetProxiesHTTPSUser: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpsuser-swift.var)
- [let kSCPropNetProxiesHTTPUser: CFString](/documentation/systemconfiguration/kscpropnetproxieshttpuser-swift.var)
- [let kSCPropNetProxiesRTSPUser: CFString](/documentation/systemconfiguration/kscpropnetproxiesrtspuser-swift.var)
- [let kSCPropNetProxiesSOCKSUser: CFString](/documentation/systemconfiguration/kscpropnetproxiessocksuser-swift.var)
- [SystemConfiguration Functions](/documentation/systemconfiguration/systemconfiguration-functions)
- [SystemConfiguration Data Types](/documentation/systemconfiguration/systemconfiguration-data-types)

### Data Types

- [AuthorizationRef](/documentation/security/authorizationref)

## Entitlements

- [Access Wi-Fi Information Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.wifi-info)

## Type Aliases

- [AuthorizationRef](/documentation/systemconfiguration/authorizationref)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
