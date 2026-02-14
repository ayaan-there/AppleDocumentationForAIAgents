# dnssd Documentation

Source: https://sosumi.ai/documentation/dnssd

---
title: dnssd
source: https://developer.apple.com/documentation/dnssd
timestamp: 2026-02-13T18:56:26.360Z
---

## Reference

- [DNS Service Discovery C](/documentation/dnssd/dns-service-discovery-c)

### Version checking

- [func DNSServiceGetProperty(UnsafePointer<CChar>!, UnsafeMutableRawPointer!, UnsafeMutablePointer<UInt32>!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicegetproperty(_:_:_:))

### Unix Domain Socket access, DNSServiceRef deallocation, and data processing functions

- [func DNSServiceProcessResult(DNSServiceRef!) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceprocessresult(_:))
- [func DNSServiceRefDeallocate(DNSServiceRef!)](/documentation/dnssd/dnsservicerefdeallocate(_:))
- [func DNSServiceRefSockFD(DNSServiceRef!) -> dnssd_sock_t](/documentation/dnssd/dnsservicerefsockfd(_:))

### Unified lookup of both IPv4 and IPv6 addresses for a fully qualified hostname

- [func DNSServiceGetAddrInfo(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, UInt32, DNSServiceProtocol, UnsafePointer<CChar>!, DNSServiceGetAddrInfoReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicegetaddrinfo(_:_:_:_:_:_:_:))

### TXT Record Parsing Functions

- [DNSServiceCreateDelegateConnection](/documentation/dnssd/dnsservicecreatedelegateconnection)
- [func DNSServiceSetDispatchQueue(DNSServiceRef!, dispatch_queue_t!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicesetdispatchqueue(_:_:))
- [func TXTRecordContainsKey(UInt16, UnsafeRawPointer!, UnsafePointer<CChar>!) -> Int32](/documentation/dnssd/txtrecordcontainskey(_:_:_:))
- [func TXTRecordGetCount(UInt16, UnsafeRawPointer!) -> UInt16](/documentation/dnssd/txtrecordgetcount(_:_:))
- [func TXTRecordGetItemAtIndex(UInt16, UnsafeRawPointer!, UInt16, UInt16, UnsafeMutablePointer<CChar>!, UnsafeMutablePointer<UInt8>!, UnsafeMutablePointer<UnsafeRawPointer?>!) -> DNSServiceErrorType](/documentation/dnssd/txtrecordgetitematindex(_:_:_:_:_:_:_:))
- [func TXTRecordGetValuePtr(UInt16, UnsafeRawPointer!, UnsafePointer<CChar>!, UnsafeMutablePointer<UInt8>!) -> UnsafeRawPointer!](/documentation/dnssd/txtrecordgetvalueptr(_:_:_:_:))

### TXT Record Construction Functions

- [func TXTRecordCreate(UnsafeMutablePointer<TXTRecordRef>!, UInt16, UnsafeMutableRawPointer!)](/documentation/dnssd/txtrecordcreate(_:_:_:))
- [func TXTRecordDeallocate(UnsafeMutablePointer<TXTRecordRef>!)](/documentation/dnssd/txtrecorddeallocate(_:))
- [func TXTRecordGetBytesPtr(UnsafePointer<TXTRecordRef>!) -> UnsafeRawPointer!](/documentation/dnssd/txtrecordgetbytesptr(_:))
- [func TXTRecordGetLength(UnsafePointer<TXTRecordRef>!) -> UInt16](/documentation/dnssd/txtrecordgetlength(_:))
- [func TXTRecordRemoveValue(UnsafeMutablePointer<TXTRecordRef>!, UnsafePointer<CChar>!) -> DNSServiceErrorType](/documentation/dnssd/txtrecordremovevalue(_:_:))
- [func TXTRecordSetValue(UnsafeMutablePointer<TXTRecordRef>!, UnsafePointer<CChar>!, UInt8, UnsafeRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/txtrecordsetvalue(_:_:_:_:))

### Special Purpose Calls

- [func DNSServiceCreateConnection(UnsafeMutablePointer<DNSServiceRef?>!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicecreateconnection(_:))
- [func DNSServiceReconfirmRecord(DNSServiceFlags, UInt32, UnsafePointer<CChar>!, UInt16, UInt16, UInt16, UnsafeRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicereconfirmrecord(_:_:_:_:_:_:_:))
- [func DNSServiceRegisterRecord(DNSServiceRef!, UnsafeMutablePointer<DNSRecordRef?>!, DNSServiceFlags, UInt32, UnsafePointer<CChar>!, UInt16, UInt16, UInt16, UnsafeRawPointer!, UInt32, DNSServiceRegisterRecordReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceregisterrecord(_:_:_:_:_:_:_:_:_:_:_:_:))
- [func PeerConnectionRelease(DNSServiceFlags, UnsafePointer<CChar>!, UnsafePointer<CChar>!, UnsafePointer<CChar>!) -> DNSServiceErrorType](/documentation/dnssd/peerconnectionrelease(_:_:_:_:))

### Service Registration

- [func DNSServiceAddRecord(DNSServiceRef!, UnsafeMutablePointer<DNSRecordRef?>!, DNSServiceFlags, UInt16, UInt16, UnsafeRawPointer!, UInt32) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceaddrecord(_:_:_:_:_:_:_:))
- [func DNSServiceRegister(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, UInt32, UnsafePointer<CChar>!, UnsafePointer<CChar>!, UnsafePointer<CChar>!, UnsafePointer<CChar>!, UInt16, UInt16, UnsafeRawPointer!, DNSServiceRegisterReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceregister(_:_:_:_:_:_:_:_:_:_:_:_:))
- [func DNSServiceRemoveRecord(DNSServiceRef!, DNSRecordRef!, DNSServiceFlags) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceremoverecord(_:_:_:))
- [func DNSServiceUpdateRecord(DNSServiceRef!, DNSRecordRef!, DNSServiceFlags, UInt16, UnsafeRawPointer!, UInt32) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceupdaterecord(_:_:_:_:_:_:))

### Service Discovery

- [func DNSServiceBrowse(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, UInt32, UnsafePointer<CChar>!, UnsafePointer<CChar>!, DNSServiceBrowseReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicebrowse(_:_:_:_:_:_:_:))
- [func DNSServiceResolve(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, UInt32, UnsafePointer<CChar>!, UnsafePointer<CChar>!, UnsafePointer<CChar>!, DNSServiceResolveReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceresolve(_:_:_:_:_:_:_:_:))

### Querying Individual Specific Records

- [func DNSServiceQueryRecord(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, UInt32, UnsafePointer<CChar>!, UInt16, UInt16, DNSServiceQueryRecordReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicequeryrecord(_:_:_:_:_:_:_:_:))

### NAT Port Mapping

- [func DNSServiceNATPortMappingCreate(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, UInt32, DNSServiceProtocol, UInt16, UInt16, UInt32, DNSServiceNATPortMappingReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicenatportmappingcreate(_:_:_:_:_:_:_:_:_:))

### General Utility Functions

- [func DNSServiceConstructFullName(UnsafeMutablePointer<CChar>!, UnsafePointer<CChar>!, UnsafePointer<CChar>!, UnsafePointer<CChar>!) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceconstructfullname(_:_:_:_:))

### Domain Enumeration

- [func DNSServiceEnumerateDomains(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, UInt32, DNSServiceDomainEnumReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceenumeratedomains(_:_:_:_:_:))

### Callbacks

- [DNSServiceGetAddrInfoReply](/documentation/dnssd/dnsservicegetaddrinforeply)
- [DNSServiceRegisterRecordReply](/documentation/dnssd/dnsserviceregisterrecordreply)
- [DNSServiceRegisterReply](/documentation/dnssd/dnsserviceregisterreply)
- [DNSServiceBrowseReply](/documentation/dnssd/dnsservicebrowsereply)
- [DNSServiceResolveReply](/documentation/dnssd/dnsserviceresolvereply)
- [DNSServiceQueryRecordReply](/documentation/dnssd/dnsservicequeryrecordreply)
- [DNSServiceNATPortMappingReply](/documentation/dnssd/dnsservicenatportmappingreply)
- [DNSServiceDomainEnumReply](/documentation/dnssd/dnsservicedomainenumreply)

### Data Types

- [DNSServiceErrorType](/documentation/dnssd/dnsserviceerrortype)
- [DNSServiceFlags](/documentation/dnssd/dnsserviceflags)
- [DNSServiceProtocol](/documentation/dnssd/dnsserviceprotocol)
- [TXTRecordRef](/documentation/dnssd/txtrecordref)

#### Miscellaneous

- [Force Natural Alignment](/documentation/dnssd/force-natural-alignment)
- [Private Data](/documentation/dnssd/private-data)

### Constants

- [Constants for specifying an interface index](/documentation/dnssd/constants-for-specifying-an-interface-index)

#### Constants

- [var kDNSServiceInterfaceIndexAny: Int32](/documentation/dnssd/kdnsserviceinterfaceindexany)
- [var kDNSServiceInterfaceIndexLocalOnly: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexlocalonly)
- [var kDNSServiceInterfaceIndexP2P: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexp2p)
- [var kDNSServiceInterfaceIndexUnicast: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexunicast)
- [Miscellaneous Defines](/documentation/dnssd/miscellaneous-defines)

#### Constants

- [_DNS_SD_H](/documentation/dnssd/dns_sd_h)
- [var kDNSServiceMaxDomainName: Int32](/documentation/dnssd/kdnsservicemaxdomainname)
- [var kDNSServiceMaxServiceName: Int32](/documentation/dnssd/kdnsservicemaxservicename)
- [var kDNSServiceProperty_DaemonVersion: String](/documentation/dnssd/kdnsserviceproperty_daemonversion)
- [dnssd Enumerations](/documentation/dnssd/dnssd-enumerations)

### Enumerations

- [DNSServiceAAAAPolicy](/documentation/dnssd/dnsserviceaaaapolicy)

#### Initializers

- [init(UInt32)](/documentation/dnssd/dnsserviceaaaapolicy/init(_:))
- [init(rawValue: UInt32)](/documentation/dnssd/dnsserviceaaaapolicy/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/dnssd/dnsserviceaaaapolicy/rawvalue)
- [dnssd Functions](/documentation/dnssd/dnssd-functions)

### Functions

- [func DNSServiceSleepKeepalive(UnsafeMutablePointer<DNSServiceRef?>!, DNSServiceFlags, Int32, UInt32, DNSServiceSleepKeepaliveReply!, UnsafeMutableRawPointer!) -> DNSServiceErrorType](/documentation/dnssd/dnsservicesleepkeepalive(_:_:_:_:_:_:))
- [func DNSServiceAttributeCreate() -> DNSServiceAttributeRef?](/documentation/dnssd/dnsserviceattributecreate())
- [func DNSServiceAttributeDeallocate(DNSServiceAttributeRef)](/documentation/dnssd/dnsserviceattributedeallocate(_:))
- [func DNSServiceAttributeSetAAAAPolicy(DNSServiceAttributeRef, DNSServiceAAAAPolicy) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceattributesetaaaapolicy(_:_:))
- [func DNSServiceAttributeSetHostKeyHash(DNSServiceAttributeRef, UInt32) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceattributesethostkeyhash(_:_:))
- [func DNSServiceAttributeSetTimestamp(DNSServiceAttributeRef, UInt32) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceattributesettimestamp(_:_:))
- [func DNSServiceQueryRecordWithAttribute(UnsafeMutablePointer<DNSServiceRef>?, DNSServiceFlags, UInt32, UnsafePointer<CChar>?, UInt16, UInt16, OpaquePointer?, DNSServiceQueryRecordReply?, UnsafeMutableRawPointer?) -> DNSServiceErrorType](/documentation/dnssd/dnsservicequeryrecordwithattribute(_:_:_:_:_:_:_:_:_:))
- [func DNSServiceRegisterRecordWithAttribute(DNSServiceRef?, UnsafeMutablePointer<DNSRecordRef>?, DNSServiceFlags, UInt32, UnsafePointer<CChar>?, UInt16, UInt16, UInt16, UnsafeRawPointer?, UInt32, DNSServiceAttributeRef?, DNSServiceRegisterRecordReply?, UnsafeMutableRawPointer?) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceregisterrecordwithattribute(_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func DNSServiceRegisterWithAttribute(UnsafeMutablePointer<DNSServiceRef>?, DNSServiceFlags, UInt32, UnsafePointer<CChar>?, UnsafePointer<CChar>?, UnsafePointer<CChar>?, UnsafePointer<CChar>?, UInt16, UInt16, UnsafeRawPointer?, DNSServiceAttributeRef?, DNSServiceRegisterReply?, UnsafeMutableRawPointer?) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceregisterwithattribute(_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func DNSServiceSendQueuedRequests(DNSServiceRef?) -> DNSServiceErrorType](/documentation/dnssd/dnsservicesendqueuedrequests(_:))
- [func DNSServiceUpdateRecordWithAttribute(DNSServiceRef?, DNSRecordRef?, DNSServiceFlags, UInt16, UnsafeRawPointer?, UInt32, DNSServiceAttributeRef?) -> DNSServiceErrorType](/documentation/dnssd/dnsserviceupdaterecordwithattribute(_:_:_:_:_:_:_:))
- [dnssd Data Types](/documentation/dnssd/dnssd-data-types)

### Data Types

- [CompileTimeAssertionChecks_DNS_SD](/documentation/dnssd/compiletimeassertionchecks_dns_sd)

#### Instance Properties

- [var assert0: CChar](/documentation/dnssd/compiletimeassertionchecks_dns_sd/assert0)

#### Initializers

- [init()](/documentation/dnssd/compiletimeassertionchecks_dns_sd/init())
- [init(assert0: CChar)](/documentation/dnssd/compiletimeassertionchecks_dns_sd/init(assert0:))
- [DNSRecordRef](/documentation/dnssd/dnsrecordref)
- [DNSServiceRef](/documentation/dnssd/dnsserviceref)
- [DNSServiceSleepKeepaliveReply](/documentation/dnssd/dnsservicesleepkeepalivereply)
- [dnssd_sock_t](/documentation/dnssd/dnssd_sock_t)
- [DNSServiceAttributeRef](/documentation/dnssd/dnsserviceattributeref)
- [dnssd Constants](/documentation/dnssd/dnssd-constants)

### Constants

- [var DNS_SD_ORIGINAL_ENCODING_VERSION_NUMBER_MAX: Int32](/documentation/dnssd/dns_sd_original_encoding_version_number_max)
- [let kDNSServiceAttributeAAAAFallback: <<error type>>](/documentation/dnssd/kdnsserviceattributeaaaafallback)
- [var kDNSServiceInterfaceIndexAny: Int32](/documentation/dnssd/kdnsserviceinterfaceindexany)
- [var kDNSServiceInterfaceIndexBLE: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexble)
- [var kDNSServiceInterfaceIndexInfra: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexinfra)
- [var kDNSServiceInterfaceIndexLocalOnly: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexlocalonly)
- [var kDNSServiceInterfaceIndexP2P: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexp2p)
- [var kDNSServiceInterfaceIndexUnicast: UInt32](/documentation/dnssd/kdnsserviceinterfaceindexunicast)
- [var kDNSServiceMaxDomainName: Int32](/documentation/dnssd/kdnsservicemaxdomainname)
- [var kDNSServiceMaxServiceName: Int32](/documentation/dnssd/kdnsservicemaxservicename)
- [var kDNSServiceProperty_DaemonVersion: String](/documentation/dnssd/kdnsserviceproperty_daemonversion)

## Variables

- [var kDNSServiceAAAAPolicyFallback: DNSServiceAAAAPolicy](/documentation/dnssd/kdnsserviceaaaapolicyfallback)
- [var kDNSServiceAAAAPolicyNone: DNSServiceAAAAPolicy](/documentation/dnssd/kdnsserviceaaaapolicynone)
- [var kDNSServiceClass_IN: Int](/documentation/dnssd/kdnsserviceclass_in)
- [var kDNSServiceErr_AlreadyRegistered: Int](/documentation/dnssd/kdnsserviceerr_alreadyregistered)
- [var kDNSServiceErr_BadFlags: Int](/documentation/dnssd/kdnsserviceerr_badflags)
- [var kDNSServiceErr_BadInterfaceIndex: Int](/documentation/dnssd/kdnsserviceerr_badinterfaceindex)
- [var kDNSServiceErr_BadKey: Int](/documentation/dnssd/kdnsserviceerr_badkey)
- [var kDNSServiceErr_BadParam: Int](/documentation/dnssd/kdnsserviceerr_badparam)
- [var kDNSServiceErr_BadReference: Int](/documentation/dnssd/kdnsserviceerr_badreference)
- [var kDNSServiceErr_BadSig: Int](/documentation/dnssd/kdnsserviceerr_badsig)
- [var kDNSServiceErr_BadState: Int](/documentation/dnssd/kdnsserviceerr_badstate)
- [var kDNSServiceErr_BadTime: Int](/documentation/dnssd/kdnsserviceerr_badtime)
- [var kDNSServiceErr_DefunctConnection: Int](/documentation/dnssd/kdnsserviceerr_defunctconnection)
- [var kDNSServiceErr_DoubleNAT: Int](/documentation/dnssd/kdnsserviceerr_doublenat)
- [var kDNSServiceErr_Firewall: Int](/documentation/dnssd/kdnsserviceerr_firewall)
- [var kDNSServiceErr_Incompatible: Int](/documentation/dnssd/kdnsserviceerr_incompatible)
- [var kDNSServiceErr_Invalid: Int](/documentation/dnssd/kdnsserviceerr_invalid)
- [var kDNSServiceErr_NATPortMappingDisabled: Int](/documentation/dnssd/kdnsserviceerr_natportmappingdisabled)
- [var kDNSServiceErr_NATPortMappingUnsupported: Int](/documentation/dnssd/kdnsserviceerr_natportmappingunsupported)
- [var kDNSServiceErr_NATTraversal: Int](/documentation/dnssd/kdnsserviceerr_nattraversal)
- [var kDNSServiceErr_NameConflict: Int](/documentation/dnssd/kdnsserviceerr_nameconflict)
- [var kDNSServiceErr_NoAuth: Int](/documentation/dnssd/kdnsserviceerr_noauth)
- [var kDNSServiceErr_NoError: Int](/documentation/dnssd/kdnsserviceerr_noerror)
- [var kDNSServiceErr_NoMemory: Int](/documentation/dnssd/kdnsserviceerr_nomemory)
- [var kDNSServiceErr_NoRouter: Int](/documentation/dnssd/kdnsserviceerr_norouter)
- [var kDNSServiceErr_NoSuchKey: Int](/documentation/dnssd/kdnsserviceerr_nosuchkey)
- [var kDNSServiceErr_NoSuchName: Int](/documentation/dnssd/kdnsserviceerr_nosuchname)
- [var kDNSServiceErr_NoSuchRecord: Int](/documentation/dnssd/kdnsserviceerr_nosuchrecord)
- [var kDNSServiceErr_NotInitialized: Int](/documentation/dnssd/kdnsserviceerr_notinitialized)
- [var kDNSServiceErr_NotPermitted: Int](/documentation/dnssd/kdnsserviceerr_notpermitted)
- [var kDNSServiceErr_PolicyDenied: Int](/documentation/dnssd/kdnsserviceerr_policydenied)
- [var kDNSServiceErr_PollingMode: Int](/documentation/dnssd/kdnsserviceerr_pollingmode)
- [var kDNSServiceErr_Refused: Int](/documentation/dnssd/kdnsserviceerr_refused)
- [var kDNSServiceErr_ServiceNotRunning: Int](/documentation/dnssd/kdnsserviceerr_servicenotrunning)
- [var kDNSServiceErr_StaleData: Int](/documentation/dnssd/kdnsserviceerr_staledata)
- [var kDNSServiceErr_Timeout: Int](/documentation/dnssd/kdnsserviceerr_timeout)
- [var kDNSServiceErr_Transient: Int](/documentation/dnssd/kdnsserviceerr_transient)
- [var kDNSServiceErr_Unknown: Int](/documentation/dnssd/kdnsserviceerr_unknown)
- [var kDNSServiceErr_Unsupported: Int](/documentation/dnssd/kdnsserviceerr_unsupported)
- [var kDNSServiceFlagAnsweredFromCache: UInt32](/documentation/dnssd/kdnsserviceflagansweredfromcache)
- [var kDNSServiceFlagsAdd: UInt32](/documentation/dnssd/kdnsserviceflagsadd)
- [var kDNSServiceFlagsAllowExpiredAnswers: UInt32](/documentation/dnssd/kdnsserviceflagsallowexpiredanswers)
- [var kDNSServiceFlagsAllowRemoteQuery: UInt32](/documentation/dnssd/kdnsserviceflagsallowremotequery)
- [var kDNSServiceFlagsAutoTrigger: UInt32](/documentation/dnssd/kdnsserviceflagsautotrigger)
- [var kDNSServiceFlagsBackgroundTrafficClass: UInt32](/documentation/dnssd/kdnsserviceflagsbackgroundtrafficclass)
- [var kDNSServiceFlagsBogus: UInt32](/documentation/dnssd/kdnsserviceflagsbogus)
- [var kDNSServiceFlagsBrowseDomains: UInt32](/documentation/dnssd/kdnsserviceflagsbrowsedomains)
- [var kDNSServiceFlagsDefault: UInt32](/documentation/dnssd/kdnsserviceflagsdefault)
- [var kDNSServiceFlagsEnableDNSSEC: UInt32](/documentation/dnssd/kdnsserviceflagsenablednssec)
- [var kDNSServiceFlagsExpiredAnswer: UInt32](/documentation/dnssd/kdnsserviceflagsexpiredanswer)
- [var kDNSServiceFlagsForce: UInt32](/documentation/dnssd/kdnsserviceflagsforce)
- [var kDNSServiceFlagsForceMulticast: UInt32](/documentation/dnssd/kdnsserviceflagsforcemulticast)
- [var kDNSServiceFlagsIncludeAWDL: UInt32](/documentation/dnssd/kdnsserviceflagsincludeawdl)
- [var kDNSServiceFlagsIncludeP2P: UInt32](/documentation/dnssd/kdnsserviceflagsincludep2p)
- [var kDNSServiceFlagsIndeterminate: UInt32](/documentation/dnssd/kdnsserviceflagsindeterminate)
- [var kDNSServiceFlagsInsecure: UInt32](/documentation/dnssd/kdnsserviceflagsinsecure)
- [var kDNSServiceFlagsKnownUnique: UInt32](/documentation/dnssd/kdnsserviceflagsknownunique)
- [var kDNSServiceFlagsLongLivedQuery: UInt32](/documentation/dnssd/kdnsserviceflagslonglivedquery)
- [var kDNSServiceFlagsMoreComing: UInt32](/documentation/dnssd/kdnsserviceflagsmorecoming)
- [var kDNSServiceFlagsNoAutoRename: UInt32](/documentation/dnssd/kdnsserviceflagsnoautorename)
- [var kDNSServiceFlagsPrivateFive: UInt32](/documentation/dnssd/kdnsserviceflagsprivatefive)
- [var kDNSServiceFlagsPrivateFour: UInt32](/documentation/dnssd/kdnsserviceflagsprivatefour)
- [var kDNSServiceFlagsPrivateOne: UInt32](/documentation/dnssd/kdnsserviceflagsprivateone)
- [var kDNSServiceFlagsPrivateThree: UInt32](/documentation/dnssd/kdnsserviceflagsprivatethree)
- [var kDNSServiceFlagsPrivateTwo: UInt32](/documentation/dnssd/kdnsserviceflagsprivatetwo)
- [var kDNSServiceFlagsQueueRequest: UInt32](/documentation/dnssd/kdnsserviceflagsqueuerequest)
- [var kDNSServiceFlagsRegistrationDomains: UInt32](/documentation/dnssd/kdnsserviceflagsregistrationdomains)
- [var kDNSServiceFlagsReturnIntermediates: UInt32](/documentation/dnssd/kdnsserviceflagsreturnintermediates)
- [var kDNSServiceFlagsSecure: UInt32](/documentation/dnssd/kdnsserviceflagssecure)
- [var kDNSServiceFlagsShareConnection: UInt32](/documentation/dnssd/kdnsserviceflagsshareconnection)
- [var kDNSServiceFlagsShared: UInt32](/documentation/dnssd/kdnsserviceflagsshared)
- [var kDNSServiceFlagsSuppressUnusable: UInt32](/documentation/dnssd/kdnsserviceflagssuppressunusable)
- [var kDNSServiceFlagsThresholdFinder: UInt32](/documentation/dnssd/kdnsserviceflagsthresholdfinder)
- [var kDNSServiceFlagsThresholdOne: UInt32](/documentation/dnssd/kdnsserviceflagsthresholdone)
- [var kDNSServiceFlagsThresholdReached: UInt32](/documentation/dnssd/kdnsserviceflagsthresholdreached)
- [var kDNSServiceFlagsTimeout: UInt32](/documentation/dnssd/kdnsserviceflagstimeout)
- [var kDNSServiceFlagsUnicastResponse: UInt32](/documentation/dnssd/kdnsserviceflagsunicastresponse)
- [var kDNSServiceFlagsUnique: UInt32](/documentation/dnssd/kdnsserviceflagsunique)
- [var kDNSServiceFlagsValidate: UInt32](/documentation/dnssd/kdnsserviceflagsvalidate)
- [var kDNSServiceFlagsValidateOptional: UInt32](/documentation/dnssd/kdnsserviceflagsvalidateoptional)
- [var kDNSServiceFlagsWakeOnResolve: UInt32](/documentation/dnssd/kdnsserviceflagswakeonresolve)
- [var kDNSServiceFlagsWakeOnlyService: UInt32](/documentation/dnssd/kdnsserviceflagswakeonlyservice)
- [var kDNSServiceProtocol_IPv4: Int](/documentation/dnssd/kdnsserviceprotocol_ipv4)
- [var kDNSServiceProtocol_IPv6: Int](/documentation/dnssd/kdnsserviceprotocol_ipv6)
- [var kDNSServiceProtocol_TCP: Int](/documentation/dnssd/kdnsserviceprotocol_tcp)
- [var kDNSServiceProtocol_UDP: Int](/documentation/dnssd/kdnsserviceprotocol_udp)
- [var kDNSServiceType_A: Int](/documentation/dnssd/kdnsservicetype_a)
- [var kDNSServiceType_A6: Int](/documentation/dnssd/kdnsservicetype_a6)
- [var kDNSServiceType_AAAA: Int](/documentation/dnssd/kdnsservicetype_aaaa)
- [var kDNSServiceType_AFSDB: Int](/documentation/dnssd/kdnsservicetype_afsdb)
- [var kDNSServiceType_ANY: Int](/documentation/dnssd/kdnsservicetype_any)
- [var kDNSServiceType_APL: Int](/documentation/dnssd/kdnsservicetype_apl)
- [var kDNSServiceType_ATMA: Int](/documentation/dnssd/kdnsservicetype_atma)
- [var kDNSServiceType_AXFR: Int](/documentation/dnssd/kdnsservicetype_axfr)
- [var kDNSServiceType_CERT: Int](/documentation/dnssd/kdnsservicetype_cert)
- [var kDNSServiceType_CNAME: Int](/documentation/dnssd/kdnsservicetype_cname)
- [var kDNSServiceType_DHCID: Int](/documentation/dnssd/kdnsservicetype_dhcid)
- [var kDNSServiceType_DNAME: Int](/documentation/dnssd/kdnsservicetype_dname)
- [var kDNSServiceType_DNSKEY: Int](/documentation/dnssd/kdnsservicetype_dnskey)
- [var kDNSServiceType_DS: Int](/documentation/dnssd/kdnsservicetype_ds)
- [var kDNSServiceType_EID: Int](/documentation/dnssd/kdnsservicetype_eid)
- [var kDNSServiceType_GID: Int](/documentation/dnssd/kdnsservicetype_gid)
- [var kDNSServiceType_GPOS: Int](/documentation/dnssd/kdnsservicetype_gpos)
- [var kDNSServiceType_HINFO: Int](/documentation/dnssd/kdnsservicetype_hinfo)
- [var kDNSServiceType_HIP: Int](/documentation/dnssd/kdnsservicetype_hip)
- [var kDNSServiceType_HTTPS: Int](/documentation/dnssd/kdnsservicetype_https)
- [var kDNSServiceType_IPSECKEY: Int](/documentation/dnssd/kdnsservicetype_ipseckey)
- [var kDNSServiceType_ISDN: Int](/documentation/dnssd/kdnsservicetype_isdn)
- [var kDNSServiceType_IXFR: Int](/documentation/dnssd/kdnsservicetype_ixfr)
- [var kDNSServiceType_KEY: Int](/documentation/dnssd/kdnsservicetype_key)
- [var kDNSServiceType_KX: Int](/documentation/dnssd/kdnsservicetype_kx)
- [var kDNSServiceType_LOC: Int](/documentation/dnssd/kdnsservicetype_loc)
- [var kDNSServiceType_MAILA: Int](/documentation/dnssd/kdnsservicetype_maila)
- [var kDNSServiceType_MAILB: Int](/documentation/dnssd/kdnsservicetype_mailb)
- [var kDNSServiceType_MB: Int](/documentation/dnssd/kdnsservicetype_mb)
- [var kDNSServiceType_MD: Int](/documentation/dnssd/kdnsservicetype_md)
- [var kDNSServiceType_MF: Int](/documentation/dnssd/kdnsservicetype_mf)
- [var kDNSServiceType_MG: Int](/documentation/dnssd/kdnsservicetype_mg)
- [var kDNSServiceType_MINFO: Int](/documentation/dnssd/kdnsservicetype_minfo)
- [var kDNSServiceType_MR: Int](/documentation/dnssd/kdnsservicetype_mr)
- [var kDNSServiceType_MX: Int](/documentation/dnssd/kdnsservicetype_mx)
- [var kDNSServiceType_NAPTR: Int](/documentation/dnssd/kdnsservicetype_naptr)
- [var kDNSServiceType_NIMLOC: Int](/documentation/dnssd/kdnsservicetype_nimloc)
- [var kDNSServiceType_NS: Int](/documentation/dnssd/kdnsservicetype_ns)
- [var kDNSServiceType_NSAP: Int](/documentation/dnssd/kdnsservicetype_nsap)
- [var kDNSServiceType_NSAP_PTR: Int](/documentation/dnssd/kdnsservicetype_nsap_ptr)
- [var kDNSServiceType_NSEC: Int](/documentation/dnssd/kdnsservicetype_nsec)
- [var kDNSServiceType_NSEC3: Int](/documentation/dnssd/kdnsservicetype_nsec3)
- [var kDNSServiceType_NSEC3PARAM: Int](/documentation/dnssd/kdnsservicetype_nsec3param)
- [var kDNSServiceType_NULL: Int](/documentation/dnssd/kdnsservicetype_null)
- [var kDNSServiceType_NXT: Int](/documentation/dnssd/kdnsservicetype_nxt)
- [var kDNSServiceType_OPT: Int](/documentation/dnssd/kdnsservicetype_opt)
- [var kDNSServiceType_PTR: Int](/documentation/dnssd/kdnsservicetype_ptr)
- [var kDNSServiceType_PX: Int](/documentation/dnssd/kdnsservicetype_px)
- [var kDNSServiceType_RP: Int](/documentation/dnssd/kdnsservicetype_rp)
- [var kDNSServiceType_RRSIG: Int](/documentation/dnssd/kdnsservicetype_rrsig)
- [var kDNSServiceType_RT: Int](/documentation/dnssd/kdnsservicetype_rt)
- [var kDNSServiceType_SIG: Int](/documentation/dnssd/kdnsservicetype_sig)
- [var kDNSServiceType_SINK: Int](/documentation/dnssd/kdnsservicetype_sink)
- [var kDNSServiceType_SOA: Int](/documentation/dnssd/kdnsservicetype_soa)
- [var kDNSServiceType_SPF: Int](/documentation/dnssd/kdnsservicetype_spf)
- [var kDNSServiceType_SRV: Int](/documentation/dnssd/kdnsservicetype_srv)
- [var kDNSServiceType_SSHFP: Int](/documentation/dnssd/kdnsservicetype_sshfp)
- [var kDNSServiceType_SVCB: Int](/documentation/dnssd/kdnsservicetype_svcb)
- [var kDNSServiceType_TKEY: Int](/documentation/dnssd/kdnsservicetype_tkey)
- [var kDNSServiceType_TSIG: Int](/documentation/dnssd/kdnsservicetype_tsig)
- [var kDNSServiceType_TXT: Int](/documentation/dnssd/kdnsservicetype_txt)
- [var kDNSServiceType_UID: Int](/documentation/dnssd/kdnsservicetype_uid)
- [var kDNSServiceType_UINFO: Int](/documentation/dnssd/kdnsservicetype_uinfo)
- [var kDNSServiceType_UNSPEC: Int](/documentation/dnssd/kdnsservicetype_unspec)
- [var kDNSServiceType_WKS: Int](/documentation/dnssd/kdnsservicetype_wks)
- [var kDNSServiceType_X25: Int](/documentation/dnssd/kdnsservicetype_x25)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
