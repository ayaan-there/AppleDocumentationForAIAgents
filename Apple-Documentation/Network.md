# Network Documentation

Source: https://sosumi.ai/documentation/network

---
title: Network
source: https://developer.apple.com/documentation/network
timestamp: 2026-02-13T18:59:59.308Z
---

## Essentials

- [NWEndpoint](/documentation/network/nwendpoint)

### Endpoint Types

- [case hostPort(host: NWEndpoint.Host, port: NWEndpoint.Port)](/documentation/network/nwendpoint/hostport(host:port:))
- [case service(name: String, type: String, domain: String, interface: NWInterface?)](/documentation/network/nwendpoint/service(name:type:domain:interface:))
- [case url(URL)](/documentation/network/nwendpoint/url(_:))
- [case unix(path: String)](/documentation/network/nwendpoint/unix(path:))

### Host and Ports

- [NWEndpoint.Host](/documentation/network/nwendpoint/host)

#### Creating Hosts

- [init(String)](/documentation/network/nwendpoint/host/init(_:))

#### Accessing Host Types

- [case name(String, NWInterface?)](/documentation/network/nwendpoint/host/name(_:_:))
- [case ipv4(IPv4Address)](/documentation/network/nwendpoint/host/ipv4(_:))
- [case ipv6(IPv6Address)](/documentation/network/nwendpoint/host/ipv6(_:))

#### Requiring Interfaces

- [var interface: NWInterface?](/documentation/network/nwendpoint/host/interface)
- [NWEndpoint.Port](/documentation/network/nwendpoint/port)

#### Creating Ports

- [init?(String)](/documentation/network/nwendpoint/port/init(_:))

#### Setting Well-Known Ports

- [static let any: NWEndpoint.Port](/documentation/network/nwendpoint/port/any)
- [static let ssh: NWEndpoint.Port](/documentation/network/nwendpoint/port/ssh)
- [static let smtp: NWEndpoint.Port](/documentation/network/nwendpoint/port/smtp)
- [static let http: NWEndpoint.Port](/documentation/network/nwendpoint/port/http)
- [static let pop: NWEndpoint.Port](/documentation/network/nwendpoint/port/pop)
- [static let imap: NWEndpoint.Port](/documentation/network/nwendpoint/port/imap)
- [static let https: NWEndpoint.Port](/documentation/network/nwendpoint/port/https)
- [static let imaps: NWEndpoint.Port](/documentation/network/nwendpoint/port/imaps)
- [static let socks: NWEndpoint.Port](/documentation/network/nwendpoint/port/socks)

### Internet Addresses

- [IPAddress](/documentation/network/ipaddress)

#### Creating Addresses

- [init?(String)](/documentation/network/ipaddress/init(_:))
- [init?(Data, NWInterface?)](/documentation/network/ipaddress/init(_:_:))

#### Inspecting Address Properties

- [var rawValue: Data](/documentation/network/ipaddress/rawvalue)
- [var interface: NWInterface?](/documentation/network/ipaddress/interface)
- [var isLinkLocal: Bool](/documentation/network/ipaddress/islinklocal)
- [var isLoopback: Bool](/documentation/network/ipaddress/isloopback)
- [var isMulticast: Bool](/documentation/network/ipaddress/ismulticast)
- [IPv4Address](/documentation/network/ipv4address)

#### Creating Addresses

- [init?(String)](/documentation/network/ipv4address/init(_:))
- [init?(Data, NWInterface?)](/documentation/network/ipv4address/init(_:_:))

#### Inspecting Address Properties

- [var rawValue: Data](/documentation/network/ipv4address/rawvalue)
- [let interface: NWInterface?](/documentation/network/ipv4address/interface)
- [var isLinkLocal: Bool](/documentation/network/ipv4address/islinklocal)
- [var isLoopback: Bool](/documentation/network/ipv4address/isloopback)
- [var isMulticast: Bool](/documentation/network/ipv4address/ismulticast)

#### Setting Well-Known Addresses

- [static let any: IPv4Address](/documentation/network/ipv4address/any)
- [static let broadcast: IPv4Address](/documentation/network/ipv4address/broadcast)
- [static let loopback: IPv4Address](/documentation/network/ipv4address/loopback)
- [static let allHostsGroup: IPv4Address](/documentation/network/ipv4address/allhostsgroup)
- [static let allRoutersGroup: IPv4Address](/documentation/network/ipv4address/allroutersgroup)
- [static let allReportsGroup: IPv4Address](/documentation/network/ipv4address/allreportsgroup)
- [static let mdnsGroup: IPv4Address](/documentation/network/ipv4address/mdnsgroup)
- [IPv6Address](/documentation/network/ipv6address)

#### Creating Addresses

- [init?(String)](/documentation/network/ipv6address/init(_:))
- [init?(Data, NWInterface?)](/documentation/network/ipv6address/init(_:_:))
- [var asIPv4: IPv4Address?](/documentation/network/ipv6address/asipv4)

#### Inspecting Address Properties

- [var rawValue: Data](/documentation/network/ipv6address/rawvalue)
- [let interface: NWInterface?](/documentation/network/ipv6address/interface)
- [var multicastScope: IPv6Address.Scope?](/documentation/network/ipv6address/multicastscope)
- [IPv6Address.Scope](/documentation/network/ipv6address/scope)

##### Scope Values

- [case nodeLocal](/documentation/network/ipv6address/scope/nodelocal)
- [case linkLocal](/documentation/network/ipv6address/scope/linklocal)
- [case siteLocal](/documentation/network/ipv6address/scope/sitelocal)
- [case organizationLocal](/documentation/network/ipv6address/scope/organizationlocal)
- [case global](/documentation/network/ipv6address/scope/global)
- [var isAny: Bool](/documentation/network/ipv6address/isany)
- [var is6to4: Bool](/documentation/network/ipv6address/is6to4)
- [var isIPv4Compatabile: Bool](/documentation/network/ipv6address/isipv4compatabile)
- [var isIPv4Mapped: Bool](/documentation/network/ipv6address/isipv4mapped)
- [var isLinkLocal: Bool](/documentation/network/ipv6address/islinklocal)
- [var isLoopback: Bool](/documentation/network/ipv6address/isloopback)
- [var isMulticast: Bool](/documentation/network/ipv6address/ismulticast)

#### Setting Well-Known Addresses

- [static let any: IPv6Address](/documentation/network/ipv6address/any)
- [static let broadcast: IPv6Address](/documentation/network/ipv6address/broadcast)
- [static let loopback: IPv6Address](/documentation/network/ipv6address/loopback)
- [static let nodeLocalNodes: IPv6Address](/documentation/network/ipv6address/nodelocalnodes)
- [static let linkLocalNodes: IPv6Address](/documentation/network/ipv6address/linklocalnodes)
- [static let linkLocalRouters: IPv6Address](/documentation/network/ipv6address/linklocalrouters)

#### Instance Properties

- [var isUniqueLocal: Bool](/documentation/network/ipv6address/isuniquelocal)

### Endpoint Properties

- [var interface: NWInterface?](/documentation/network/nwendpoint/interface)

### Enumeration Cases

- [case opaque(nw_endpoint_t)](/documentation/network/nwendpoint/opaque(_:))

### Instance Properties

- [var txtRecord: NWTXTRecord?](/documentation/network/nwendpoint/txtrecord)
- [NWParameters](/documentation/network/nwparameters)

### Creating Parameters

- [class var tls: NWParameters](/documentation/network/nwparameters/tls)
- [class var tcp: NWParameters](/documentation/network/nwparameters/tcp)
- [class var dtls: NWParameters](/documentation/network/nwparameters/dtls)
- [class var udp: NWParameters](/documentation/network/nwparameters/udp)
- [class func quic(alpn: [String]) -> NWParameters](/documentation/network/nwparameters/quic(alpn:))
- [class func quicDatagram(alpn: [String]) -> NWParameters](/documentation/network/nwparameters/quicdatagram(alpn:))
- [convenience init(tls: NWProtocolTLS.Options?, tcp: NWProtocolTCP.Options)](/documentation/network/nwparameters/init(tls:tcp:))
- [convenience init(dtls: NWProtocolTLS.Options?, udp: NWProtocolUDP.Options)](/documentation/network/nwparameters/init(dtls:udp:))
- [convenience init(quic: NWProtocolQUIC.Options)](/documentation/network/nwparameters/init(quic:))
- [init()](/documentation/network/nwparameters/init())
- [init(customIPProtocolNumber: UInt8)](/documentation/network/nwparameters/init(customipprotocolnumber:))
- [func copy() -> NWParameters](/documentation/network/nwparameters/copy())

### Modifying Protocol Stacks

- [var defaultProtocolStack: NWParameters.ProtocolStack](/documentation/network/nwparameters/defaultprotocolstack)
- [NWParameters.ProtocolStack](/documentation/network/nwparameters/protocolstack)

#### Adding Application Protocols

- [var applicationProtocols: [NWProtocolOptions]](/documentation/network/nwparameters/protocolstack/applicationprotocols)

#### Configuring Lower Protocols

- [var transportProtocol: NWProtocolOptions?](/documentation/network/nwparameters/protocolstack/transportprotocol)
- [var internetProtocol: NWProtocolOptions?](/documentation/network/nwparameters/protocolstack/internetprotocol)
- [NWProtocol](/documentation/network/nwprotocol)

#### Adding Protocols to Connections

- [NWProtocolOptions](/documentation/network/nwprotocoloptions)
- [NWProtocolDefinition](/documentation/network/nwprotocoldefinition)

##### Inspecting Protocol Definitions

- [let name: String](/documentation/network/nwprotocoldefinition/name)

#### Interacting with Protocols

- [NWProtocolMetadata](/documentation/network/nwprotocolmetadata)

### Selecting Paths

- [var requiredInterfaceType: NWInterface.InterfaceType](/documentation/network/nwparameters/requiredinterfacetype)
- [var requiredInterface: NWInterface?](/documentation/network/nwparameters/requiredinterface)
- [var requiredLocalEndpoint: NWEndpoint?](/documentation/network/nwparameters/requiredlocalendpoint)
- [var prohibitConstrainedPaths: Bool](/documentation/network/nwparameters/prohibitconstrainedpaths)
- [var prohibitExpensivePaths: Bool](/documentation/network/nwparameters/prohibitexpensivepaths)
- [var prohibitedInterfaceTypes: [NWInterface.InterfaceType]?](/documentation/network/nwparameters/prohibitedinterfacetypes)
- [var prohibitedInterfaces: [NWInterface]?](/documentation/network/nwparameters/prohibitedinterfaces)

### Customizing Connection Options

- [var multipathServiceType: NWParameters.MultipathServiceType](/documentation/network/nwparameters/multipathservicetype-swift.property)
- [NWParameters.MultipathServiceType](/documentation/network/nwparameters/multipathservicetype-swift.enum)

#### Multipath Service Types

- [case disabled](/documentation/network/nwparameters/multipathservicetype-swift.enum/disabled)
- [case handover](/documentation/network/nwparameters/multipathservicetype-swift.enum/handover)
- [case interactive](/documentation/network/nwparameters/multipathservicetype-swift.enum/interactive)
- [case aggregate](/documentation/network/nwparameters/multipathservicetype-swift.enum/aggregate)
- [var serviceClass: NWParameters.ServiceClass](/documentation/network/nwparameters/serviceclass-swift.property)
- [NWParameters.ServiceClass](/documentation/network/nwparameters/serviceclass-swift.enum)

#### Service Classes

- [case bestEffort](/documentation/network/nwparameters/serviceclass-swift.enum/besteffort)
- [case background](/documentation/network/nwparameters/serviceclass-swift.enum/background)
- [case interactiveVideo](/documentation/network/nwparameters/serviceclass-swift.enum/interactivevideo)
- [case interactiveVoice](/documentation/network/nwparameters/serviceclass-swift.enum/interactivevoice)
- [case responsiveData](/documentation/network/nwparameters/serviceclass-swift.enum/responsivedata)
- [case signaling](/documentation/network/nwparameters/serviceclass-swift.enum/signaling)
- [var allowFastOpen: Bool](/documentation/network/nwparameters/allowfastopen)
- [var expiredDNSBehavior: NWParameters.ExpiredDNSBehavior](/documentation/network/nwparameters/expireddnsbehavior-swift.property)
- [NWParameters.ExpiredDNSBehavior](/documentation/network/nwparameters/expireddnsbehavior-swift.enum)

#### Behaviors

- [case systemDefault](/documentation/network/nwparameters/expireddnsbehavior-swift.enum/systemdefault)
- [case allow](/documentation/network/nwparameters/expireddnsbehavior-swift.enum/allow)
- [case prohibit](/documentation/network/nwparameters/expireddnsbehavior-swift.enum/prohibit)

#### Enumeration Cases

- [case persistent](/documentation/network/nwparameters/expireddnsbehavior-swift.enum/persistent)
- [var requiresDNSSECValidation: Bool](/documentation/network/nwparameters/requiresdnssecvalidation)
- [var preferNoProxies: Bool](/documentation/network/nwparameters/prefernoproxies)
- [var includePeerToPeer: Bool](/documentation/network/nwparameters/includepeertopeer)
- [var allowLocalEndpointReuse: Bool](/documentation/network/nwparameters/allowlocalendpointreuse)
- [var acceptLocalOnly: Bool](/documentation/network/nwparameters/acceptlocalonly)

### Configuring Privacy Settings

- [func setPrivacyContext(NWParameters.PrivacyContext)](/documentation/network/nwparameters/setprivacycontext(_:))
- [NWParameters.PrivacyContext](/documentation/network/nwparameters/privacycontext)

#### Configuring Custom Privacy Settings

- [init(description: String)](/documentation/network/nwparameters/privacycontext/init(description:))
- [static let `default`: NWParameters.PrivacyContext](/documentation/network/nwparameters/privacycontext/default)
- [func disableLogging()](/documentation/network/nwparameters/privacycontext/disablelogging())
- [func flushCache()](/documentation/network/nwparameters/privacycontext/flushcache())

#### Requiring Encrypted DNS

- [func requireEncryptedNameResolution(Bool, fallbackResolver: NWParameters.PrivacyContext.ResolverConfiguration?)](/documentation/network/nwparameters/privacycontext/requireencryptednameresolution(_:fallbackresolver:))
- [NWParameters.PrivacyContext.ResolverConfiguration](/documentation/network/nwparameters/privacycontext/resolverconfiguration)

##### Resolver Types

- [case https(URL, serverAddresses: [NWEndpoint])](/documentation/network/nwparameters/privacycontext/resolverconfiguration/https(_:serveraddresses:))
- [case tls(NWEndpoint, serverAddresses: [NWEndpoint])](/documentation/network/nwparameters/privacycontext/resolverconfiguration/tls(_:serveraddresses:))

#### Configuring Proxies

- [var proxyConfigurations: [ProxyConfiguration]](/documentation/network/nwparameters/privacycontext/proxyconfigurations)
- [ProxyConfiguration](/documentation/network/proxyconfiguration)

##### Creating Proxy Configurations

- [init(relayHops: [ProxyConfiguration.RelayHop])](/documentation/network/proxyconfiguration/init(relayhops:))
- [ProxyConfiguration.RelayHop](/documentation/network/proxyconfiguration/relayhop)

###### Creating Relay Hops

- [init(http3RelayEndpoint: NWEndpoint, http2RelayEndpoint: NWEndpoint?, tlsOptions: NWProtocolTLS.Options, additionalHTTPHeaderFields: [String : String])](/documentation/network/proxyconfiguration/relayhop/init(http3relayendpoint:http2relayendpoint:tlsoptions:additionalhttpheaderfields:))
- [init(http2RelayEndpoint: NWEndpoint, tlsOptions: NWProtocolTLS.Options, additionalHTTPHeaderFields: [String : String])](/documentation/network/proxyconfiguration/relayhop/init(http2relayendpoint:tlsoptions:additionalhttpheaderfields:))
- [init(httpCONNECTProxy: NWEndpoint, tlsOptions: NWProtocolTLS.Options?)](/documentation/network/proxyconfiguration/init(httpconnectproxy:tlsoptions:))
- [init(socksv5Proxy: NWEndpoint)](/documentation/network/proxyconfiguration/init(socksv5proxy:))

##### Customizing Proxy Behavior

- [var allowFailover: Bool](/documentation/network/proxyconfiguration/allowfailover)
- [func applyCredential(username: String, password: String)](/documentation/network/proxyconfiguration/applycredential(username:password:))

##### Initializers

- [init(obliviousHTTPRelay: ProxyConfiguration.RelayHop, relayResourcePath: String, gatewayKeyConfig: Data, matchDomains: [String])](/documentation/network/proxyconfiguration/init(oblivioushttprelay:relayresourcepath:gatewaykeyconfig:matchdomains:))

##### Instance Properties

- [var excludedDomains: [String]](/documentation/network/proxyconfiguration/excludeddomains)
- [var matchDomains: [String]](/documentation/network/proxyconfiguration/matchdomains)

### Instance Properties

- [var allowUltraConstrainedPaths: Bool](/documentation/network/nwparameters/allowultraconstrainedpaths)
- [var attribution: NWParameters.Attribution](/documentation/network/nwparameters/attribution-swift.property)
- [var wifiAware: WAParameters](/documentation/network/nwparameters/wifiaware)

### Instance Methods

- [func wifiAware((inout WAParameters) -> Void) -> Self](/documentation/network/nwparameters/wifiaware(_:))

### Type Properties

- [class var applicationService: NWParameters](/documentation/network/nwparameters/applicationservice)

### Enumerations

- [NWParameters.Attribution](/documentation/network/nwparameters/attribution-swift.enum)

#### Enumeration Cases

- [case developer](/documentation/network/nwparameters/attribution-swift.enum/developer)
- [case user](/documentation/network/nwparameters/attribution-swift.enum/user)

## Connections and Listeners

- [NWConnection](/documentation/network/nwconnection)

### Creating Connections

- [convenience init(host: NWEndpoint.Host, port: NWEndpoint.Port, using: NWParameters)](/documentation/network/nwconnection/init(host:port:using:))
- [init(to: NWEndpoint, using: NWParameters)](/documentation/network/nwconnection/init(to:using:))
- [func start(queue: DispatchQueue)](/documentation/network/nwconnection/start(queue:))
- [func restart()](/documentation/network/nwconnection/restart())

### Handling State Updates

- [var state: NWConnection.State](/documentation/network/nwconnection/state-swift.property)
- [NWConnection.State](/documentation/network/nwconnection/state-swift.enum)

#### States

- [case setup](/documentation/network/nwconnection/state-swift.enum/setup)
- [case waiting(NWError)](/documentation/network/nwconnection/state-swift.enum/waiting(_:))
- [case preparing](/documentation/network/nwconnection/state-swift.enum/preparing)
- [case ready](/documentation/network/nwconnection/state-swift.enum/ready)
- [case failed(NWError)](/documentation/network/nwconnection/state-swift.enum/failed(_:))
- [case cancelled](/documentation/network/nwconnection/state-swift.enum/cancelled)
- [var stateUpdateHandler: ((NWConnection.State) -> Void)?](/documentation/network/nwconnection/stateupdatehandler)

### Sending and Receiving Data

- [func send(content: Data?, contentContext: NWConnection.ContentContext, isComplete: Bool, completion: NWConnection.SendCompletion)](/documentation/network/nwconnection/send(content:contentcontext:iscomplete:completion:)-5ecuz)
- [func send<Content>(content: Content?, contentContext: NWConnection.ContentContext, isComplete: Bool, completion: NWConnection.SendCompletion)](/documentation/network/nwconnection/send(content:contentcontext:iscomplete:completion:)-3mfmt)
- [NWConnection.SendCompletion](/documentation/network/nwconnection/sendcompletion)

#### Completions

- [case contentProcessed((NWError?) -> Void)](/documentation/network/nwconnection/sendcompletion/contentprocessed(_:))
- [case idempotent](/documentation/network/nwconnection/sendcompletion/idempotent)
- [func receive(minimumIncompleteLength: Int, maximumLength: Int, completion: (Data?, NWConnection.ContentContext?, Bool, NWError?) -> Void)](/documentation/network/nwconnection/receive(minimumincompletelength:maximumlength:completion:))
- [func receiveMessage(completion: (Data?, NWConnection.ContentContext?, Bool, NWError?) -> Void)](/documentation/network/nwconnection/receivemessage(completion:))
- [func batch(() -> Void)](/documentation/network/nwconnection/batch(_:))
- [NWConnection.ContentContext](/documentation/network/nwconnection/contentcontext)

#### Using Constant Send Contexts

- [static let defaultMessage: NWConnection.ContentContext](/documentation/network/nwconnection/contentcontext/defaultmessage)
- [static let finalMessage: NWConnection.ContentContext](/documentation/network/nwconnection/contentcontext/finalmessage)
- [static let defaultStream: NWConnection.ContentContext](/documentation/network/nwconnection/contentcontext/defaultstream)

#### Creating Custom Send Contexts

- [init(identifier: String, expiration: UInt64, priority: Double, isFinal: Bool, antecedent: NWConnection.ContentContext?, metadata: [NWProtocolMetadata]?)](/documentation/network/nwconnection/contentcontext/init(identifier:expiration:priority:isfinal:antecedent:metadata:))
- [let identifier: String](/documentation/network/nwconnection/contentcontext/identifier)
- [var protocolMetadata: [NWProtocolMetadata]](/documentation/network/nwconnection/contentcontext/protocolmetadata)
- [NWProtocolMetadata](/documentation/network/nwprotocolmetadata)
- [let antecedent: NWConnection.ContentContext?](/documentation/network/nwconnection/contentcontext/antecedent)
- [let expirationMilliseconds: UInt64](/documentation/network/nwconnection/contentcontext/expirationmilliseconds)
- [let relativePriority: Double](/documentation/network/nwconnection/contentcontext/relativepriority)

#### Inspecting Receive Contexts

- [let isFinal: Bool](/documentation/network/nwconnection/contentcontext/isfinal)
- [func protocolMetadata(definition: NWProtocolDefinition) -> NWProtocolMetadata?](/documentation/network/nwconnection/contentcontext/protocolmetadata(definition:))
- [var maximumDatagramSize: Int](/documentation/network/nwconnection/maximumdatagramsize)

### Canceling Connections

- [func cancel()](/documentation/network/nwconnection/cancel())
- [func forceCancel()](/documentation/network/nwconnection/forcecancel())
- [func cancelCurrentEndpoint()](/documentation/network/nwconnection/cancelcurrentendpoint())

### Handling Path Updates

- [var currentPath: NWPath?](/documentation/network/nwconnection/currentpath)
- [var pathUpdateHandler: ((NWPath) -> Void)?](/documentation/network/nwconnection/pathupdatehandler)
- [var viabilityUpdateHandler: ((Bool) -> Void)?](/documentation/network/nwconnection/viabilityupdatehandler)
- [var betterPathUpdateHandler: ((Bool) -> Void)?](/documentation/network/nwconnection/betterpathupdatehandler)

### Collecting Connection Metrics

- [Collecting Network Connection Metrics](/documentation/network/collecting-network-connection-metrics)
- [func requestEstablishmentReport(queue: DispatchQueue, completion: (NWConnection.EstablishmentReport?) -> Void)](/documentation/network/nwconnection/requestestablishmentreport(queue:completion:))
- [NWConnection.EstablishmentReport](/documentation/network/nwconnection/establishmentreport)

#### Inspecting Connection Attempts

- [let duration: TimeInterval](/documentation/network/nwconnection/establishmentreport/duration)
- [let previousAttemptCount: Int](/documentation/network/nwconnection/establishmentreport/previousattemptcount)
- [let attemptStartedAfterInterval: TimeInterval](/documentation/network/nwconnection/establishmentreport/attemptstartedafterinterval)

#### Inspecting Resolution

- [let resolutions: [NWConnection.EstablishmentReport.Resolution]](/documentation/network/nwconnection/establishmentreport/resolutions)
- [NWConnection.EstablishmentReport.Resolution](/documentation/network/nwconnection/establishmentreport/resolution)

##### Measuring Performance

- [let duration: TimeInterval](/documentation/network/nwconnection/establishmentreport/resolution/duration)
- [let source: NWConnection.EstablishmentReport.Resolution.Source](/documentation/network/nwconnection/establishmentreport/resolution/source-swift.property)
- [NWConnection.EstablishmentReport.Resolution.Source](/documentation/network/nwconnection/establishmentreport/resolution/source-swift.enum)

###### Resolution Sources

- [case query](/documentation/network/nwconnection/establishmentreport/resolution/source-swift.enum/query)
- [case cache](/documentation/network/nwconnection/establishmentreport/resolution/source-swift.enum/cache)
- [case expiredCache](/documentation/network/nwconnection/establishmentreport/resolution/source-swift.enum/expiredcache)
- [var dnsProtocol: NWConnection.EstablishmentReport.Resolution.DNSProtocol](/documentation/network/nwconnection/establishmentreport/resolution/dnsprotocol-swift.property)
- [NWConnection.EstablishmentReport.Resolution.DNSProtocol](/documentation/network/nwconnection/establishmentreport/resolution/dnsprotocol-swift.enum)

###### Resolution Transports

- [case unknown](/documentation/network/nwconnection/establishmentreport/resolution/dnsprotocol-swift.enum/unknown)
- [case udp](/documentation/network/nwconnection/establishmentreport/resolution/dnsprotocol-swift.enum/udp)
- [case tcp](/documentation/network/nwconnection/establishmentreport/resolution/dnsprotocol-swift.enum/tcp)
- [case tls](/documentation/network/nwconnection/establishmentreport/resolution/dnsprotocol-swift.enum/tls)
- [case https](/documentation/network/nwconnection/establishmentreport/resolution/dnsprotocol-swift.enum/https)

##### Examining Resolved Endpoints

- [let successfulEndpoint: NWEndpoint](/documentation/network/nwconnection/establishmentreport/resolution/successfulendpoint)
- [let preferredEndpoint: NWEndpoint](/documentation/network/nwconnection/establishmentreport/resolution/preferredendpoint)
- [let endpointCount: Int](/documentation/network/nwconnection/establishmentreport/resolution/endpointcount)

#### Inspecting Protocol Handshakes

- [let handshakes: [NWConnection.EstablishmentReport.Handshake]](/documentation/network/nwconnection/establishmentreport/handshakes)
- [NWConnection.EstablishmentReport.Handshake](/documentation/network/nwconnection/establishmentreport/handshake)

##### Measuring Performance

- [let handshakeDuration: TimeInterval](/documentation/network/nwconnection/establishmentreport/handshake/handshakeduration)
- [let handshakeRTT: TimeInterval](/documentation/network/nwconnection/establishmentreport/handshake/handshakertt)

##### Identifying Protocols

- [let definition: NWProtocolDefinition](/documentation/network/nwconnection/establishmentreport/handshake/definition)

#### Checking for Proxies

- [let proxyConfigured: Bool](/documentation/network/nwconnection/establishmentreport/proxyconfigured)
- [let usedProxy: Bool](/documentation/network/nwconnection/establishmentreport/usedproxy)
- [let proxyEndpoint: NWEndpoint?](/documentation/network/nwconnection/establishmentreport/proxyendpoint)
- [func startDataTransferReport() -> NWConnection.PendingDataTransferReport](/documentation/network/nwconnection/startdatatransferreport())
- [NWConnection.PendingDataTransferReport](/documentation/network/nwconnection/pendingdatatransferreport)

#### Collecting Reports

- [func collect(queue: DispatchQueue, completion: (NWConnection.DataTransferReport) -> Void)](/documentation/network/nwconnection/pendingdatatransferreport/collect(queue:completion:))
- [NWConnection.DataTransferReport](/documentation/network/nwconnection/datatransferreport)

#### Examining Data Transfer

- [let aggregatePathReport: NWConnection.DataTransferReport.PathReport](/documentation/network/nwconnection/datatransferreport/aggregatepathreport)
- [let pathReports: [NWConnection.DataTransferReport.PathReport]](/documentation/network/nwconnection/datatransferreport/pathreports)
- [NWConnection.DataTransferReport.PathReport](/documentation/network/nwconnection/datatransferreport/pathreport)

##### Identifying Paths

- [let interface: NWInterface](/documentation/network/nwconnection/datatransferreport/pathreport/interface)

##### Inspecting Application Metrics

- [let receivedApplicationByteCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/receivedapplicationbytecount)
- [let sentApplicationByteCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/sentapplicationbytecount)

##### Inspecting Transport Metrics

- [let receivedTransportByteCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/receivedtransportbytecount)
- [let receivedTransportDuplicateByteCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/receivedtransportduplicatebytecount)
- [let receivedTransportOutOfOrderByteCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/receivedtransportoutoforderbytecount)
- [let sentTransportByteCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/senttransportbytecount)
- [let retransmittedTransportByteCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/retransmittedtransportbytecount)
- [let transportSmoothedRTT: TimeInterval](/documentation/network/nwconnection/datatransferreport/pathreport/transportsmoothedrtt)
- [let transportMinimumRTT: TimeInterval](/documentation/network/nwconnection/datatransferreport/pathreport/transportminimumrtt)
- [let transportRTTVariance: TimeInterval](/documentation/network/nwconnection/datatransferreport/pathreport/transportrttvariance)

##### Inspecting Packet Metrics

- [let receivedIPPacketCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/receivedippacketcount)
- [let sentIPPacketCount: UInt64](/documentation/network/nwconnection/datatransferreport/pathreport/sentippacketcount)

##### Instance Properties

- [var radioType: NWInterface.RadioType?](/documentation/network/nwconnection/datatransferreport/pathreport/radiotype)

#### Summarizing Reports

- [let duration: TimeInterval](/documentation/network/nwconnection/datatransferreport/duration)

### Inspecting Connections

- [func metadata(definition: NWProtocolDefinition) -> NWProtocolMetadata?](/documentation/network/nwconnection/metadata(definition:))
- [NWProtocolMetadata](/documentation/network/nwprotocolmetadata)
- [let endpoint: NWEndpoint](/documentation/network/nwconnection/endpoint)
- [let parameters: NWParameters](/documentation/network/nwconnection/parameters)
- [var queue: DispatchQueue?](/documentation/network/nwconnection/queue)

### Initializers

- [convenience init?(from: NWConnectionGroup, to: NWEndpoint?, using: NWProtocolOptions?)](/documentation/network/nwconnection/init(from:to:using:))
- [convenience init?(message: NWConnectionGroup.Message)](/documentation/network/nwconnection/init(message:))

### Instance Methods

- [func receiveDiscontiguous(minimumIncompleteLength: Int, maximumLength: Int, completion: (DispatchData?, NWConnection.ContentContext?, Bool, NWError?) -> Void)](/documentation/network/nwconnection/receivediscontiguous(minimumincompletelength:maximumlength:completion:))
- [func receiveMessageDiscontiguous(completion: (DispatchData?, NWConnection.ContentContext?, Bool, NWError?) -> Void)](/documentation/network/nwconnection/receivemessagediscontiguous(completion:))
- [NWListener](/documentation/network/nwlistener)

### Creating Listeners

- [init(using: NWParameters, on: NWEndpoint.Port) throws](/documentation/network/nwlistener/init(using:on:))
- [func start(queue: DispatchQueue)](/documentation/network/nwlistener/start(queue:))
- [var stateUpdateHandler: ((NWListener.State) -> Void)?](/documentation/network/nwlistener/stateupdatehandler)
- [NWListener.State](/documentation/network/nwlistener/state-swift.enum)

#### States

- [case setup](/documentation/network/nwlistener/state-swift.enum/setup)
- [case waiting(NWError)](/documentation/network/nwlistener/state-swift.enum/waiting(_:))
- [case ready](/documentation/network/nwlistener/state-swift.enum/ready)
- [case failed(NWError)](/documentation/network/nwlistener/state-swift.enum/failed(_:))
- [case cancelled](/documentation/network/nwlistener/state-swift.enum/cancelled)
- [var port: NWEndpoint.Port?](/documentation/network/nwlistener/port)
- [func cancel()](/documentation/network/nwlistener/cancel())

### Receiving Connections

- [var newConnectionHandler: ((NWConnection) -> Void)?](/documentation/network/nwlistener/newconnectionhandler)
- [var newConnectionLimit: Int](/documentation/network/nwlistener/newconnectionlimit)
- [static let InfiniteConnectionLimit: Int](/documentation/network/nwlistener/infiniteconnectionlimit)

### Advertising Bonjour Services

- [NSBonjourServices](/documentation/bundleresources/information-property-list/nsbonjourservices)
- [NSLocalNetworkUsageDescription](/documentation/bundleresources/information-property-list/nslocalnetworkusagedescription)
- [var service: NWListener.Service?](/documentation/network/nwlistener/service-swift.property)
- [NWListener.Service](/documentation/network/nwlistener/service-swift.struct)

#### Defining Services

- [init(name: String?, type: String, domain: String?, txtRecord: Data?)](/documentation/network/nwlistener/service-swift.struct/init(name:type:domain:txtrecord:)-1lb30)
- [init(name: String?, type: String, domain: String?, txtRecord: NWTXTRecord)](/documentation/network/nwlistener/service-swift.struct/init(name:type:domain:txtrecord:)-8qh5)
- [var noAutoRename: Bool](/documentation/network/nwlistener/service-swift.struct/noautorename)

#### Inspecting Services

- [let name: String?](/documentation/network/nwlistener/service-swift.struct/name)
- [let type: String](/documentation/network/nwlistener/service-swift.struct/type)
- [let domain: String?](/documentation/network/nwlistener/service-swift.struct/domain)
- [var txtRecordObject: NWTXTRecord?](/documentation/network/nwlistener/service-swift.struct/txtrecordobject)
- [let txtRecord: Data?](/documentation/network/nwlistener/service-swift.struct/txtrecord)

#### Initializers

- [init(applicationService: String)](/documentation/network/nwlistener/service-swift.struct/init(applicationservice:))
- [var serviceRegistrationUpdateHandler: ((NWListener.ServiceRegistrationChange) -> Void)?](/documentation/network/nwlistener/serviceregistrationupdatehandler)
- [NWListener.ServiceRegistrationChange](/documentation/network/nwlistener/serviceregistrationchange)

#### Changes

- [case add(NWEndpoint)](/documentation/network/nwlistener/serviceregistrationchange/add(_:))
- [case remove(NWEndpoint)](/documentation/network/nwlistener/serviceregistrationchange/remove(_:))

### Inspecting Listeners

- [let parameters: NWParameters](/documentation/network/nwlistener/parameters)
- [var queue: DispatchQueue?](/documentation/network/nwlistener/queue)

### Initializers

- [convenience init(applicationService: String, using: NWParameters) throws](/documentation/network/nwlistener/init(applicationservice:using:))
- [convenience init?(launchd: String, using: NWParameters)](/documentation/network/nwlistener/init(launchd:using:))
- [convenience init(launchdSocketKey: String, parameters: NWParameters)](/documentation/network/nwlistener/init(launchdsocketkey:parameters:))
- [convenience init(service: NWListener.Service, using: NWParameters) throws](/documentation/network/nwlistener/init(service:using:))

### Instance Properties

- [var newConnectionGroupHandler: ((NWConnectionGroup) -> Void)?](/documentation/network/nwlistener/newconnectiongrouphandler)
- [var state: NWListener.State](/documentation/network/nwlistener/state-swift.property)
- [NWBrowser](/documentation/network/nwbrowser)

### Essentials

- [NSBonjourServices](/documentation/bundleresources/information-property-list/nsbonjourservices)
- [NSLocalNetworkUsageDescription](/documentation/bundleresources/information-property-list/nslocalnetworkusagedescription)

### Browsing for Services

- [init(for: NWBrowser.Descriptor, using: NWParameters)](/documentation/network/nwbrowser/init(for:using:))
- [NWBrowser.Descriptor](/documentation/network/nwbrowser/descriptor-swift.enum)

#### Descriptor Types

- [case bonjour(type: String, domain: String?)](/documentation/network/nwbrowser/descriptor-swift.enum/bonjour(type:domain:))
- [case bonjourWithTXTRecord(type: String, domain: String?)](/documentation/network/nwbrowser/descriptor-swift.enum/bonjourwithtxtrecord(type:domain:))

#### Enumeration Cases

- [case applicationService(name: String)](/documentation/network/nwbrowser/descriptor-swift.enum/applicationservice(name:))
- [func start(queue: DispatchQueue)](/documentation/network/nwbrowser/start(queue:))
- [var browseResultsChangedHandler: ((Set<NWBrowser.Result>, Set<NWBrowser.Result.Change>) -> Void)?](/documentation/network/nwbrowser/browseresultschangedhandler)
- [NWBrowser.Result](/documentation/network/nwbrowser/result)

#### Evaluating Browser Results

- [let endpoint: NWEndpoint](/documentation/network/nwbrowser/result/endpoint)
- [let interfaces: [NWInterface]](/documentation/network/nwbrowser/result/interfaces)
- [let metadata: NWBrowser.Result.Metadata](/documentation/network/nwbrowser/result/metadata-swift.property)
- [NWBrowser.Result.Metadata](/documentation/network/nwbrowser/result/metadata-swift.enum)

##### Metadata Types

- [case bonjour(NWTXTRecord)](/documentation/network/nwbrowser/result/metadata-swift.enum/bonjour(_:))
- [case none](/documentation/network/nwbrowser/result/metadata-swift.enum/none)
- [NWTXTRecord](/documentation/network/nwtxtrecord)

##### Creating TXT Records

- [init([String : String])](/documentation/network/nwtxtrecord/init(_:)-566pd)
- [func removeEntry(key: String) -> Bool](/documentation/network/nwtxtrecord/removeentry(key:))
- [func setEntry(NWTXTRecord.Entry, for: String) -> Bool](/documentation/network/nwtxtrecord/setentry(_:for:))
- [NWTXTRecord.Entry](/documentation/network/nwtxtrecord/entry)

###### Entry Types

- [case none](/documentation/network/nwtxtrecord/entry/none)
- [case empty](/documentation/network/nwtxtrecord/entry/empty)
- [case string(String)](/documentation/network/nwtxtrecord/entry/string(_:))

###### Enumeration Cases

- [case data(Data)](/documentation/network/nwtxtrecord/entry/data(_:))

###### Initializers

- [init(Data?)](/documentation/network/nwtxtrecord/entry/init(_:))

###### Instance Properties

- [var data: Data?](/documentation/network/nwtxtrecord/entry/data)

##### Examining TXT Records

- [func getEntry(for: String) -> NWTXTRecord.Entry?](/documentation/network/nwtxtrecord/getentry(for:))
- [subscript(String) -> String?](/documentation/network/nwtxtrecord/subscript(_:))
- [var dictionary: [String : String]](/documentation/network/nwtxtrecord/dictionary)

##### Initializers

- [init(Data)](/documentation/network/nwtxtrecord/init(_:)-30jy4)

##### Instance Properties

- [var data: Data](/documentation/network/nwtxtrecord/data)

#### Comparing Results

- [NWBrowser.Result.Change](/documentation/network/nwbrowser/result/change)

##### Inspecting Change Types

- [case identical](/documentation/network/nwbrowser/result/change/identical)
- [case added(NWBrowser.Result)](/documentation/network/nwbrowser/result/change/added(_:))
- [case removed(NWBrowser.Result)](/documentation/network/nwbrowser/result/change/removed(_:))
- [case changed(old: NWBrowser.Result, new: NWBrowser.Result, flags: NWBrowser.Result.Change.Flags)](/documentation/network/nwbrowser/result/change/changed(old:new:flags:))
- [NWBrowser.Result.Change.Flags](/documentation/network/nwbrowser/result/change/flags)

###### Change Flags

- [static let identical: NWBrowser.Result.Change.Flags](/documentation/network/nwbrowser/result/change/flags/identical)
- [static let interfaceAdded: NWBrowser.Result.Change.Flags](/documentation/network/nwbrowser/result/change/flags/interfaceadded)
- [static let interfaceRemoved: NWBrowser.Result.Change.Flags](/documentation/network/nwbrowser/result/change/flags/interfaceremoved)
- [static let metadataChanged: NWBrowser.Result.Change.Flags](/documentation/network/nwbrowser/result/change/flags/metadatachanged)

##### Calculating Result Changes

- [init(between: NWBrowser.Result?, NWBrowser.Result?)](/documentation/network/nwbrowser/result/change/init(between:_:))
- [var browseResults: Set<NWBrowser.Result>](/documentation/network/nwbrowser/browseresults)

### Managing Browsers

- [var stateUpdateHandler: ((NWBrowser.State) -> Void)?](/documentation/network/nwbrowser/stateupdatehandler)
- [NWBrowser.State](/documentation/network/nwbrowser/state-swift.enum)

#### States

- [case setup](/documentation/network/nwbrowser/state-swift.enum/setup)
- [case ready](/documentation/network/nwbrowser/state-swift.enum/ready)
- [case failed(NWError)](/documentation/network/nwbrowser/state-swift.enum/failed(_:))
- [case cancelled](/documentation/network/nwbrowser/state-swift.enum/cancelled)

#### Enumeration Cases

- [case waiting(NWError)](/documentation/network/nwbrowser/state-swift.enum/waiting(_:))
- [var state: NWBrowser.State](/documentation/network/nwbrowser/state-swift.property)
- [func cancel()](/documentation/network/nwbrowser/cancel())

### Inspecting Browsers

- [let descriptor: NWBrowser.Descriptor](/documentation/network/nwbrowser/descriptor-swift.property)
- [let parameters: NWParameters](/documentation/network/nwbrowser/parameters)
- [var queue: DispatchQueue?](/documentation/network/nwbrowser/queue)
- [NWConnectionGroup](/documentation/network/nwconnectiongroup)

### Establishing Group Connectivity

- [init(with: any NWGroupDescriptor, using: NWParameters)](/documentation/network/nwconnectiongroup/init(with:using:))
- [NWMulticastGroup](/documentation/network/nwmulticastgroup)

#### Essentials

- [com.apple.developer.networking.multicast](/documentation/bundleresources/entitlements/com.apple.developer.networking.multicast)

#### Defining Multicast Groups

- [init(for: [NWEndpoint], from: NWEndpoint?, disableUnicast: Bool) throws](/documentation/network/nwmulticastgroup/init(for:from:disableunicast:))

#### Inspecting Multicast Groups

- [var members: [NWEndpoint]](/documentation/network/nwmulticastgroup/members)
- [let sourceFilter: NWEndpoint?](/documentation/network/nwmulticastgroup/sourcefilter)
- [let isUnicastDisabled: Bool](/documentation/network/nwmulticastgroup/isunicastdisabled)
- [NWGroupDescriptor](/documentation/network/nwgroupdescriptor)

#### Inspecting Groups

- [var members: [NWEndpoint]](/documentation/network/nwgroupdescriptor/members)
- [func start(queue: DispatchQueue)](/documentation/network/nwconnectiongroup/start(queue:))

### Sending and Receiving Group Messages

- [func setReceiveHandler(maximumMessageSize: Int, rejectOversizedMessages: Bool, handler: ((NWConnectionGroup.Message, Data?, Bool) -> Void)?)](/documentation/network/nwconnectiongroup/setreceivehandler(maximummessagesize:rejectoversizedmessages:handler:))
- [func send(content: Data?, to: NWEndpoint?, message: NWConnectionGroup.Message, completion: (NWError?) -> Void)](/documentation/network/nwconnectiongroup/send(content:to:message:completion:))
- [NWConnectionGroup.Message](/documentation/network/nwconnectiongroup/message)

#### Inspecting Received Messages

- [var remoteEndpoint: NWEndpoint?](/documentation/network/nwconnectiongroup/message/remoteendpoint)
- [var localEndpoint: NWEndpoint?](/documentation/network/nwconnectiongroup/message/localendpoint)
- [var path: NWPath?](/documentation/network/nwconnectiongroup/message/path)

#### Replying to Received Messages

- [func reply(content: Data?, message: NWConnectionGroup.Message)](/documentation/network/nwconnectiongroup/message/reply(content:message:))
- [func extractConnection() -> NWConnection?](/documentation/network/nwconnectiongroup/message/extractconnection())

#### Sending Messages

- [static let `default`: NWConnectionGroup.Message](/documentation/network/nwconnectiongroup/message/default)
- [init(identifier: String, expiration: UInt64, priority: Double, isFinal: Bool, antecedent: NWConnection.ContentContext?, metadata: [NWProtocolMetadata]?)](/documentation/network/nwconnectiongroup/message/init(identifier:expiration:priority:isfinal:antecedent:metadata:))

#### Initializers

- [init(nw: nw_content_context_t)](/documentation/network/nwconnectiongroup/message/init(nw:))

#### Instance Methods

- [func metadata(definition: NWProtocolDefinition) -> NWProtocolMetadata?](/documentation/network/nwconnectiongroup/message/metadata(definition:))

### Managing Groups

- [var stateUpdateHandler: ((NWConnectionGroup.State) -> Void)?](/documentation/network/nwconnectiongroup/stateupdatehandler)
- [NWConnectionGroup.State](/documentation/network/nwconnectiongroup/state-swift.enum)

#### States

- [case setup](/documentation/network/nwconnectiongroup/state-swift.enum/setup)
- [case waiting(NWError)](/documentation/network/nwconnectiongroup/state-swift.enum/waiting(_:))
- [case ready](/documentation/network/nwconnectiongroup/state-swift.enum/ready)
- [case failed(NWError)](/documentation/network/nwconnectiongroup/state-swift.enum/failed(_:))
- [case cancelled](/documentation/network/nwconnectiongroup/state-swift.enum/cancelled)
- [var state: NWConnectionGroup.State](/documentation/network/nwconnectiongroup/state-swift.property)
- [func cancel()](/documentation/network/nwconnectiongroup/cancel())

### Inspecting Groups

- [let descriptor: any NWGroupDescriptor](/documentation/network/nwconnectiongroup/descriptor)
- [let parameters: NWParameters](/documentation/network/nwconnectiongroup/parameters)
- [var queue: DispatchQueue?](/documentation/network/nwconnectiongroup/queue)

### Instance Properties

- [var newConnectionHandler: ((NWConnection) -> Void)?](/documentation/network/nwconnectiongroup/newconnectionhandler)

### Instance Methods

- [func extract(connectionTo: NWEndpoint?, using: NWProtocolOptions?) -> NWConnection?](/documentation/network/nwconnectiongroup/extract(connectionto:using:))
- [func metadata(definition: NWProtocolDefinition) -> NWProtocolMetadata?](/documentation/network/nwconnectiongroup/metadata(definition:))
- [func reinsert(connection: NWConnection) -> Bool](/documentation/network/nwconnectiongroup/reinsert(connection:))
- [NWEthernetChannel](/documentation/network/nwethernetchannel)

### Managing Ethernet Channels

- [init(on: NWInterface, etherType: UInt16)](/documentation/network/nwethernetchannel/init(on:ethertype:))
- [func start(queue: DispatchQueue)](/documentation/network/nwethernetchannel/start(queue:))
- [func cancel()](/documentation/network/nwethernetchannel/cancel())

### Handling State Updates

- [var state: NWEthernetChannel.State](/documentation/network/nwethernetchannel/state-swift.property)
- [NWEthernetChannel.State](/documentation/network/nwethernetchannel/state-swift.enum)

#### States

- [case setup](/documentation/network/nwethernetchannel/state-swift.enum/setup)
- [case waiting(NWError)](/documentation/network/nwethernetchannel/state-swift.enum/waiting(_:))
- [case preparing](/documentation/network/nwethernetchannel/state-swift.enum/preparing)
- [case ready](/documentation/network/nwethernetchannel/state-swift.enum/ready)
- [case failed(NWError)](/documentation/network/nwethernetchannel/state-swift.enum/failed(_:))
- [case cancelled](/documentation/network/nwethernetchannel/state-swift.enum/cancelled)
- [var stateUpdateHandler: ((NWEthernetChannel.State) -> Void)?](/documentation/network/nwethernetchannel/stateupdatehandler)

### Sending and Receiving Ethernet Frames

- [func send(content: Data, to: NWEthernetChannel.EthernetAddress, vlanTag: UInt16, completion: (NWError?) -> Void)](/documentation/network/nwethernetchannel/send(content:to:vlantag:completion:))
- [var receiveHandler: ((Data, UInt16, NWEthernetChannel.EthernetAddress, NWEthernetChannel.EthernetAddress) -> Void)?](/documentation/network/nwethernetchannel/receivehandler)
- [NWEthernetChannel.EthernetAddress](/documentation/network/nwethernetchannel/ethernetaddress)

#### Creating Addresses

- [init?(Data)](/documentation/network/nwethernetchannel/ethernetaddress/init(_:)-62x9i)
- [init?(String)](/documentation/network/nwethernetchannel/ethernetaddress/init(_:)-1brh7)

#### Inspecting Addresses

- [var rawValue: Data](/documentation/network/nwethernetchannel/ethernetaddress/rawvalue)

### Inspecting Ethernet Channels

- [let etherType: UInt16](/documentation/network/nwethernetchannel/ethertype)
- [let interface: NWInterface](/documentation/network/nwethernetchannel/interface)
- [var queue: DispatchQueue?](/documentation/network/nwethernetchannel/queue)

### Initializers

- [init(on: NWInterface, etherType: UInt16, parameters: NWParameters)](/documentation/network/nwethernetchannel/init(on:ethertype:parameters:))

### Instance Properties

- [var maximumPayloadSize: Int](/documentation/network/nwethernetchannel/maximumpayloadsize)

## Network Protocols

- [Building a custom peer-to-peer protocol](/documentation/network/building-a-custom-peer-to-peer-protocol)
- [Connecting iPadOS and visionOS apps over the local network](/documentation/visionos/connecting-ipados-and-visionos-apps-over-the-local-network)
- [NWProtocolTCP](/documentation/network/nwprotocoltcp)

### Creating TCP Connections

- [NWProtocolTCP.Options](/documentation/network/nwprotocoltcp/options)

#### Customizing TCP Options

- [init()](/documentation/network/nwprotocoltcp/options/init())
- [var enableFastOpen: Bool](/documentation/network/nwprotocoltcp/options/enablefastopen)
- [var maximumSegmentSize: Int](/documentation/network/nwprotocoltcp/options/maximumsegmentsize)
- [var noDelay: Bool](/documentation/network/nwprotocoltcp/options/nodelay)
- [var noOptions: Bool](/documentation/network/nwprotocoltcp/options/nooptions)
- [var noPush: Bool](/documentation/network/nwprotocoltcp/options/nopush)
- [var retransmitFinDrop: Bool](/documentation/network/nwprotocoltcp/options/retransmitfindrop)
- [var disableAckStretching: Bool](/documentation/network/nwprotocoltcp/options/disableackstretching)
- [var disableECN: Bool](/documentation/network/nwprotocoltcp/options/disableecn)

#### Configuring Keepalives

- [var enableKeepalive: Bool](/documentation/network/nwprotocoltcp/options/enablekeepalive)
- [var keepaliveIdle: Int](/documentation/network/nwprotocoltcp/options/keepaliveidle)
- [var keepaliveCount: Int](/documentation/network/nwprotocoltcp/options/keepalivecount)
- [var keepaliveInterval: Int](/documentation/network/nwprotocoltcp/options/keepaliveinterval)

#### Setting Timeouts

- [var connectionTimeout: Int](/documentation/network/nwprotocoltcp/options/connectiontimeout)
- [var connectionDropTime: Int](/documentation/network/nwprotocoltcp/options/connectiondroptime)
- [var persistTimeout: Int](/documentation/network/nwprotocoltcp/options/persisttimeout)
- [static let definition: NWProtocolDefinition](/documentation/network/nwprotocoltcp/definition)

### Inspecting TCP State

- [NWProtocolTCP.Metadata](/documentation/network/nwprotocoltcp/metadata)

#### Inspecting TCP State

- [var availableSendBuffer: UInt32](/documentation/network/nwprotocoltcp/metadata/availablesendbuffer)
- [var availableReceiveBuffer: UInt32](/documentation/network/nwprotocoltcp/metadata/availablereceivebuffer)
- [NWProtocolTLS](/documentation/network/nwprotocoltls)

### Creating TLS Connections

- [NWProtocolTLS.Options](/documentation/network/nwprotocoltls/options)

#### Customizing TLS Connections

- [init()](/documentation/network/nwprotocoltls/options/init())
- [var securityProtocolOptions: sec_protocol_options_t](/documentation/network/nwprotocoltls/options/securityprotocoloptions)
- [static let definition: NWProtocolDefinition](/documentation/network/nwprotocoltls/definition)

### Inspecting TLS State

- [NWProtocolTLS.Metadata](/documentation/network/nwprotocoltls/metadata)

#### Inspecting TLS State

- [var securityProtocolMetadata: sec_protocol_metadata_t](/documentation/network/nwprotocoltls/metadata/securityprotocolmetadata)
- [NWProtocolQUIC](/documentation/network/nwprotocolquic)

### Creating QUIC Connections

- [NWProtocolQUIC.Options](/documentation/network/nwprotocolquic/options)

#### Customizing Connection Options

- [convenience init(alpn: [String])](/documentation/network/nwprotocolquic/options/init(alpn:))
- [init()](/documentation/network/nwprotocolquic/options/init())
- [var alpn: [String]](/documentation/network/nwprotocolquic/options/alpn)
- [var idleTimeout: Int](/documentation/network/nwprotocolquic/options/idletimeout)
- [var initialMaxData: Int](/documentation/network/nwprotocolquic/options/initialmaxdata)
- [var initialMaxStreamDataBidirectionalLocal: Int](/documentation/network/nwprotocolquic/options/initialmaxstreamdatabidirectionallocal)
- [var initialMaxStreamDataBidirectionalRemote: Int](/documentation/network/nwprotocolquic/options/initialmaxstreamdatabidirectionalremote)
- [var initialMaxStreamDataUnidirectional: Int](/documentation/network/nwprotocolquic/options/initialmaxstreamdataunidirectional)
- [var initialMaxStreamsBidirectional: Int](/documentation/network/nwprotocolquic/options/initialmaxstreamsbidirectional)
- [var initialMaxStreamsUnidirectional: Int](/documentation/network/nwprotocolquic/options/initialmaxstreamsunidirectional)
- [var maxDatagramFrameSize: Int](/documentation/network/nwprotocolquic/options/maxdatagramframesize)
- [var maxUDPPayloadSize: Int](/documentation/network/nwprotocolquic/options/maxudppayloadsize)
- [var securityProtocolOptions: sec_protocol_options_t](/documentation/network/nwprotocolquic/options/securityprotocoloptions)

#### Customizing Stream Options

- [var direction: NWProtocolQUIC.Options.Direction](/documentation/network/nwprotocolquic/options/direction-swift.property)
- [NWProtocolQUIC.Options.Direction](/documentation/network/nwprotocolquic/options/direction-swift.enum)

##### Direction Values

- [case bidirectional](/documentation/network/nwprotocolquic/options/direction-swift.enum/bidirectional)
- [case unidirectional](/documentation/network/nwprotocolquic/options/direction-swift.enum/unidirectional)
- [var isDatagram: Bool](/documentation/network/nwprotocolquic/options/isdatagram)
- [static let definition: NWProtocolDefinition](/documentation/network/nwprotocolquic/definition)

### Inspecting QUIC State

- [NWProtocolQUIC.Metadata](/documentation/network/nwprotocolquic/metadata)

#### Inspecting Connection State

- [var negotiatedALPN: String?](/documentation/network/nwprotocolquic/metadata/negotiatedalpn)
- [var localMaxStreamsBidirectional: Int](/documentation/network/nwprotocolquic/metadata/localmaxstreamsbidirectional)
- [var localMaxStreamsUnidirectional: Int](/documentation/network/nwprotocolquic/metadata/localmaxstreamsunidirectional)
- [var remoteMaxStreamsBidirectional: Int](/documentation/network/nwprotocolquic/metadata/remotemaxstreamsbidirectional)
- [var remoteMaxStreamsUnidirectional: Int](/documentation/network/nwprotocolquic/metadata/remotemaxstreamsunidirectional)
- [var remoteIdleTimeout: Int](/documentation/network/nwprotocolquic/metadata/remoteidletimeout)
- [var securityProtocolMetadata: sec_protocol_metadata_t](/documentation/network/nwprotocolquic/metadata/securityprotocolmetadata)

#### Inspecting Stream State

- [var streamIdentifier: UInt64](/documentation/network/nwprotocolquic/metadata/streamidentifier)
- [var usableDatagramFrameSize: Int](/documentation/network/nwprotocolquic/metadata/usabledatagramframesize)

#### Handling Errors

- [var applicationError: NWProtocolQUIC.ApplicationError](/documentation/network/nwprotocolquic/metadata/applicationerror)
- [NWProtocolQUIC.ApplicationError](/documentation/network/nwprotocolquic/applicationerror)

##### Configuring Application Errors

- [init(code: UInt64, reason: String?)](/documentation/network/nwprotocolquic/applicationerror/init(code:reason:))

##### Inspecting Application Errors

- [let code: UInt64](/documentation/network/nwprotocolquic/applicationerror/code)
- [let reason: String?](/documentation/network/nwprotocolquic/applicationerror/reason)
- [var streamApplicationErrorCode: UInt64](/documentation/network/nwprotocolquic/metadata/streamapplicationerrorcode)

#### Configuring Keepalives

- [var keepAlive: NWProtocolQUIC.Metadata.KeepAliveBehavior](/documentation/network/nwprotocolquic/metadata/keepalive)
- [NWProtocolQUIC.Metadata.KeepAliveBehavior](/documentation/network/nwprotocolquic/metadata/keepalivebehavior)

##### Keepalive Behaviors

- [case on](/documentation/network/nwprotocolquic/metadata/keepalivebehavior/on)
- [case off](/documentation/network/nwprotocolquic/metadata/keepalivebehavior/off)
- [case seconds(Int)](/documentation/network/nwprotocolquic/metadata/keepalivebehavior/seconds(_:))

### Structures

- [NWProtocolQUIC.ApplicationError](/documentation/network/nwprotocolquic/applicationerror)

#### Configuring Application Errors

- [init(code: UInt64, reason: String?)](/documentation/network/nwprotocolquic/applicationerror/init(code:reason:))

#### Inspecting Application Errors

- [let code: UInt64](/documentation/network/nwprotocolquic/applicationerror/code)
- [let reason: String?](/documentation/network/nwprotocolquic/applicationerror/reason)
- [NWProtocolUDP](/documentation/network/nwprotocoludp)

### Creating UDP Connections

- [NWProtocolUDP.Options](/documentation/network/nwprotocoludp/options)

#### Customizing UDP Connections

- [init()](/documentation/network/nwprotocoludp/options/init())
- [var preferNoChecksum: Bool](/documentation/network/nwprotocoludp/options/prefernochecksum)
- [static let definition: NWProtocolDefinition](/documentation/network/nwprotocoludp/definition)

### Sending UDP Messages

- [NWProtocolUDP.Metadata](/documentation/network/nwprotocoludp/metadata)

#### Creating UDP Messages

- [init()](/documentation/network/nwprotocoludp/metadata/init())
- [NWProtocolIP](/documentation/network/nwprotocolip)

### Handling IP Packets

- [NWProtocolIP.Metadata](/documentation/network/nwprotocolip/metadata)

#### Sending IP Options

- [init()](/documentation/network/nwprotocolip/metadata/init())
- [var ecn: NWProtocolIP.ECN](/documentation/network/nwprotocolip/metadata/ecn)
- [NWProtocolIP.ECN](/documentation/network/nwprotocolip/ecn)

##### ECN Flags

- [case nonECT](/documentation/network/nwprotocolip/ecn/nonect)
- [case ect0](/documentation/network/nwprotocolip/ecn/ect0)
- [case ect1](/documentation/network/nwprotocolip/ecn/ect1)
- [case ce](/documentation/network/nwprotocolip/ecn/ce)
- [var serviceClass: NWParameters.ServiceClass](/documentation/network/nwprotocolip/metadata/serviceclass)

#### Receiving IP Packets

- [var receiveTime: UInt64](/documentation/network/nwprotocolip/metadata/receivetime)

#### Instance Methods

- [func ecn(NWProtocolIP.ECN) -> Self](/documentation/network/nwprotocolip/metadata/ecn(_:))
- [func serviceClass(NWParameters.ServiceClass) -> Self](/documentation/network/nwprotocolip/metadata/serviceclass(_:))

### Configuring IP Connections

- [NWProtocolIP.Options](/documentation/network/nwprotocolip/options)

#### Selecting an IP Version

- [var version: NWProtocolIP.Options.Version](/documentation/network/nwprotocolip/options/version-swift.property)
- [NWProtocolIP.Options.Version](/documentation/network/nwprotocolip/options/version-swift.enum)

##### Versions

- [case any](/documentation/network/nwprotocolip/options/version-swift.enum/any)
- [case v4](/documentation/network/nwprotocolip/options/version-swift.enum/v4)
- [case v6](/documentation/network/nwprotocolip/options/version-swift.enum/v6)

#### Customizing IP Behavior

- [var shouldCalculateReceiveTime: Bool](/documentation/network/nwprotocolip/options/shouldcalculatereceivetime)
- [var hopLimit: UInt8](/documentation/network/nwprotocolip/options/hoplimit)
- [var useMinimumMTU: Bool](/documentation/network/nwprotocolip/options/useminimummtu)
- [var disableFragmentation: Bool](/documentation/network/nwprotocolip/options/disablefragmentation)

#### Instance Properties

- [var disableMulticastLoopback: Bool](/documentation/network/nwprotocolip/options/disablemulticastloopback)
- [var localAddressPreference: NWProtocolIP.Options.AddressPreference](/documentation/network/nwprotocolip/options/localaddresspreference)

#### Enumerations

- [NWProtocolIP.Options.AddressPreference](/documentation/network/nwprotocolip/options/addresspreference)

##### Enumeration Cases

- [case `default`](/documentation/network/nwprotocolip/options/addresspreference/default)
- [case stable](/documentation/network/nwprotocolip/options/addresspreference/stable)
- [case temporary](/documentation/network/nwprotocolip/options/addresspreference/temporary)
- [static let definition: NWProtocolDefinition](/documentation/network/nwprotocolip/definition)

### Enumerations

- [NWProtocolIP.ECN](/documentation/network/nwprotocolip/ecn)

#### ECN Flags

- [case nonECT](/documentation/network/nwprotocolip/ecn/nonect)
- [case ect0](/documentation/network/nwprotocolip/ecn/ect0)
- [case ect1](/documentation/network/nwprotocolip/ecn/ect1)
- [case ce](/documentation/network/nwprotocolip/ecn/ce)
- [NWProtocolWebSocket](/documentation/network/nwprotocolwebsocket)

### Creating WebSocket Connections

- [NWProtocolWebSocket.Options](/documentation/network/nwprotocolwebsocket/options)

#### Configuring WebSocket Options

- [init(NWProtocolWebSocket.Version)](/documentation/network/nwprotocolwebsocket/options/init(_:))
- [NWProtocolWebSocket.Version](/documentation/network/nwprotocolwebsocket/version)

##### Versions

- [case version13](/documentation/network/nwprotocolwebsocket/version/version13)
- [var autoReplyPing: Bool](/documentation/network/nwprotocolwebsocket/options/autoreplyping)
- [var maximumMessageSize: Int](/documentation/network/nwprotocolwebsocket/options/maximummessagesize)

#### Configuring Client Handshakes

- [func setAdditionalHeaders([(name: String, value: String)])](/documentation/network/nwprotocolwebsocket/options/setadditionalheaders(_:))
- [func setSubprotocols([String])](/documentation/network/nwprotocolwebsocket/options/setsubprotocols(_:))
- [var skipHandshake: Bool](/documentation/network/nwprotocolwebsocket/options/skiphandshake)

#### Handling Server Handshakes

- [func setClientRequestHandler(DispatchQueue, handler: ([String], [(name: String, value: String)]) -> NWProtocolWebSocket.Response)](/documentation/network/nwprotocolwebsocket/options/setclientrequesthandler(_:handler:))
- [NWProtocolWebSocket.Response](/documentation/network/nwprotocolwebsocket/response)

##### Sending Handshake Responses

- [init(status: NWProtocolWebSocket.Response.Status, subprotocol: String?, additionalHeaders: [(name: String, value: String)]?)](/documentation/network/nwprotocolwebsocket/response/init(status:subprotocol:additionalheaders:))
- [NWProtocolWebSocket.Response.Status](/documentation/network/nwprotocolwebsocket/response/status-swift.enum)

###### Handshake Status Values

- [case accept](/documentation/network/nwprotocolwebsocket/response/status-swift.enum/accept)
- [case reject](/documentation/network/nwprotocolwebsocket/response/status-swift.enum/reject)
- [let status: NWProtocolWebSocket.Response.Status](/documentation/network/nwprotocolwebsocket/response/status-swift.property)
- [let subprotocol: String?](/documentation/network/nwprotocolwebsocket/response/subprotocol)
- [let additionalHeaders: [(name: String, value: String)]?](/documentation/network/nwprotocolwebsocket/response/additionalheaders)
- [static let definition: NWProtocolDefinition](/documentation/network/nwprotocolwebsocket/definition)

### Handling WebSocket Messages

- [NWProtocolWebSocket.Metadata](/documentation/network/nwprotocolwebsocket/metadata)

#### Sending Messages

- [init(opcode: NWProtocolWebSocket.Opcode)](/documentation/network/nwprotocolwebsocket/metadata/init(opcode:))
- [NWProtocolWebSocket.Opcode](/documentation/network/nwprotocolwebsocket/opcode)

##### Data Types

- [case binary](/documentation/network/nwprotocolwebsocket/opcode/binary)
- [case text](/documentation/network/nwprotocolwebsocket/opcode/text)
- [case cont](/documentation/network/nwprotocolwebsocket/opcode/cont)

##### Control Types

- [case ping](/documentation/network/nwprotocolwebsocket/opcode/ping)
- [case pong](/documentation/network/nwprotocolwebsocket/opcode/pong)
- [case close](/documentation/network/nwprotocolwebsocket/opcode/close)
- [func setPongHandler(DispatchQueue, handler: (NWError?) -> Void)](/documentation/network/nwprotocolwebsocket/metadata/setponghandler(_:handler:))
- [var closeCode: NWProtocolWebSocket.CloseCode](/documentation/network/nwprotocolwebsocket/metadata/closecode)
- [NWProtocolWebSocket.CloseCode](/documentation/network/nwprotocolwebsocket/closecode)

##### Close Code Types

- [init(rawValue: UInt16) throws](/documentation/network/nwprotocolwebsocket/closecode/init(rawvalue:))
- [case protocolCode(NWProtocolWebSocket.CloseCode.Defined)](/documentation/network/nwprotocolwebsocket/closecode/protocolcode(_:))
- [NWProtocolWebSocket.CloseCode.Defined](/documentation/network/nwprotocolwebsocket/closecode/defined)

###### Defined Close Codes

- [case normalClosure](/documentation/network/nwprotocolwebsocket/closecode/defined/normalclosure)
- [case goingAway](/documentation/network/nwprotocolwebsocket/closecode/defined/goingaway)
- [case protocolError](/documentation/network/nwprotocolwebsocket/closecode/defined/protocolerror)
- [case unsupportedData](/documentation/network/nwprotocolwebsocket/closecode/defined/unsupporteddata)
- [case noStatusReceived](/documentation/network/nwprotocolwebsocket/closecode/defined/nostatusreceived)
- [case abnormalClosure](/documentation/network/nwprotocolwebsocket/closecode/defined/abnormalclosure)
- [case invalidFramePayloadData](/documentation/network/nwprotocolwebsocket/closecode/defined/invalidframepayloaddata)
- [case policyViolation](/documentation/network/nwprotocolwebsocket/closecode/defined/policyviolation)
- [case messageTooBig](/documentation/network/nwprotocolwebsocket/closecode/defined/messagetoobig)
- [case mandatoryExtension](/documentation/network/nwprotocolwebsocket/closecode/defined/mandatoryextension)
- [case internalServerError](/documentation/network/nwprotocolwebsocket/closecode/defined/internalservererror)
- [case tlsHandshake](/documentation/network/nwprotocolwebsocket/closecode/defined/tlshandshake)
- [case applicationCode(UInt16)](/documentation/network/nwprotocolwebsocket/closecode/applicationcode(_:))
- [case privateCode(UInt16)](/documentation/network/nwprotocolwebsocket/closecode/privatecode(_:))

#### Receiving Messages

- [let opcode: NWProtocolWebSocket.Opcode](/documentation/network/nwprotocolwebsocket/metadata/opcode)
- [var closeCode: NWProtocolWebSocket.CloseCode](/documentation/network/nwprotocolwebsocket/metadata/closecode)
- [NWProtocolWebSocket.CloseCode](/documentation/network/nwprotocolwebsocket/closecode)

##### Close Code Types

- [init(rawValue: UInt16) throws](/documentation/network/nwprotocolwebsocket/closecode/init(rawvalue:))
- [case protocolCode(NWProtocolWebSocket.CloseCode.Defined)](/documentation/network/nwprotocolwebsocket/closecode/protocolcode(_:))
- [NWProtocolWebSocket.CloseCode.Defined](/documentation/network/nwprotocolwebsocket/closecode/defined)

###### Defined Close Codes

- [case normalClosure](/documentation/network/nwprotocolwebsocket/closecode/defined/normalclosure)
- [case goingAway](/documentation/network/nwprotocolwebsocket/closecode/defined/goingaway)
- [case protocolError](/documentation/network/nwprotocolwebsocket/closecode/defined/protocolerror)
- [case unsupportedData](/documentation/network/nwprotocolwebsocket/closecode/defined/unsupporteddata)
- [case noStatusReceived](/documentation/network/nwprotocolwebsocket/closecode/defined/nostatusreceived)
- [case abnormalClosure](/documentation/network/nwprotocolwebsocket/closecode/defined/abnormalclosure)
- [case invalidFramePayloadData](/documentation/network/nwprotocolwebsocket/closecode/defined/invalidframepayloaddata)
- [case policyViolation](/documentation/network/nwprotocolwebsocket/closecode/defined/policyviolation)
- [case messageTooBig](/documentation/network/nwprotocolwebsocket/closecode/defined/messagetoobig)
- [case mandatoryExtension](/documentation/network/nwprotocolwebsocket/closecode/defined/mandatoryextension)
- [case internalServerError](/documentation/network/nwprotocolwebsocket/closecode/defined/internalservererror)
- [case tlsHandshake](/documentation/network/nwprotocolwebsocket/closecode/defined/tlshandshake)
- [case applicationCode(UInt16)](/documentation/network/nwprotocolwebsocket/closecode/applicationcode(_:))
- [case privateCode(UInt16)](/documentation/network/nwprotocolwebsocket/closecode/privatecode(_:))

#### Inspecting Handshake Results

- [var selectedSubprotocol: String?](/documentation/network/nwprotocolwebsocket/metadata/selectedsubprotocol)
- [var additionalServerHeaders: [(String, String)]?](/documentation/network/nwprotocolwebsocket/metadata/additionalserverheaders)

### Structures

- [NWProtocolWebSocket.Response](/documentation/network/nwprotocolwebsocket/response)

#### Sending Handshake Responses

- [init(status: NWProtocolWebSocket.Response.Status, subprotocol: String?, additionalHeaders: [(name: String, value: String)]?)](/documentation/network/nwprotocolwebsocket/response/init(status:subprotocol:additionalheaders:))
- [NWProtocolWebSocket.Response.Status](/documentation/network/nwprotocolwebsocket/response/status-swift.enum)

##### Handshake Status Values

- [case accept](/documentation/network/nwprotocolwebsocket/response/status-swift.enum/accept)
- [case reject](/documentation/network/nwprotocolwebsocket/response/status-swift.enum/reject)
- [let status: NWProtocolWebSocket.Response.Status](/documentation/network/nwprotocolwebsocket/response/status-swift.property)
- [let subprotocol: String?](/documentation/network/nwprotocolwebsocket/response/subprotocol)
- [let additionalHeaders: [(name: String, value: String)]?](/documentation/network/nwprotocolwebsocket/response/additionalheaders)

### Enumerations

- [NWProtocolWebSocket.CloseCode](/documentation/network/nwprotocolwebsocket/closecode)

#### Close Code Types

- [init(rawValue: UInt16) throws](/documentation/network/nwprotocolwebsocket/closecode/init(rawvalue:))
- [case protocolCode(NWProtocolWebSocket.CloseCode.Defined)](/documentation/network/nwprotocolwebsocket/closecode/protocolcode(_:))
- [NWProtocolWebSocket.CloseCode.Defined](/documentation/network/nwprotocolwebsocket/closecode/defined)

##### Defined Close Codes

- [case normalClosure](/documentation/network/nwprotocolwebsocket/closecode/defined/normalclosure)
- [case goingAway](/documentation/network/nwprotocolwebsocket/closecode/defined/goingaway)
- [case protocolError](/documentation/network/nwprotocolwebsocket/closecode/defined/protocolerror)
- [case unsupportedData](/documentation/network/nwprotocolwebsocket/closecode/defined/unsupporteddata)
- [case noStatusReceived](/documentation/network/nwprotocolwebsocket/closecode/defined/nostatusreceived)
- [case abnormalClosure](/documentation/network/nwprotocolwebsocket/closecode/defined/abnormalclosure)
- [case invalidFramePayloadData](/documentation/network/nwprotocolwebsocket/closecode/defined/invalidframepayloaddata)
- [case policyViolation](/documentation/network/nwprotocolwebsocket/closecode/defined/policyviolation)
- [case messageTooBig](/documentation/network/nwprotocolwebsocket/closecode/defined/messagetoobig)
- [case mandatoryExtension](/documentation/network/nwprotocolwebsocket/closecode/defined/mandatoryextension)
- [case internalServerError](/documentation/network/nwprotocolwebsocket/closecode/defined/internalservererror)
- [case tlsHandshake](/documentation/network/nwprotocolwebsocket/closecode/defined/tlshandshake)
- [case applicationCode(UInt16)](/documentation/network/nwprotocolwebsocket/closecode/applicationcode(_:))
- [case privateCode(UInt16)](/documentation/network/nwprotocolwebsocket/closecode/privatecode(_:))
- [NWProtocolWebSocket.Opcode](/documentation/network/nwprotocolwebsocket/opcode)

#### Data Types

- [case binary](/documentation/network/nwprotocolwebsocket/opcode/binary)
- [case text](/documentation/network/nwprotocolwebsocket/opcode/text)
- [case cont](/documentation/network/nwprotocolwebsocket/opcode/cont)

#### Control Types

- [case ping](/documentation/network/nwprotocolwebsocket/opcode/ping)
- [case pong](/documentation/network/nwprotocolwebsocket/opcode/pong)
- [case close](/documentation/network/nwprotocolwebsocket/opcode/close)
- [NWProtocolWebSocket.Version](/documentation/network/nwprotocolwebsocket/version)

#### Versions

- [case version13](/documentation/network/nwprotocolwebsocket/version/version13)
- [NWProtocolFramer](/documentation/network/nwprotocolframer)

### Implementing Framer Protocols

- [NWProtocolFramerImplementation](/documentation/network/nwprotocolframerimplementation)

#### Handling Instance Lifetime

- [init(framer: NWProtocolFramer.Instance)](/documentation/network/nwprotocolframerimplementation/init(framer:))
- [func start(framer: NWProtocolFramer.Instance) -> NWProtocolFramer.StartResult](/documentation/network/nwprotocolframerimplementation/start(framer:))
- [NWProtocolFramer.StartResult](/documentation/network/nwprotocolframer/startresult)

##### Start Results

- [case ready](/documentation/network/nwprotocolframer/startresult/ready)
- [case willMarkReady](/documentation/network/nwprotocolframer/startresult/willmarkready)
- [func wakeup(framer: NWProtocolFramer.Instance)](/documentation/network/nwprotocolframerimplementation/wakeup(framer:))
- [func stop(framer: NWProtocolFramer.Instance) -> Bool](/documentation/network/nwprotocolframerimplementation/stop(framer:))
- [func cleanup(framer: NWProtocolFramer.Instance)](/documentation/network/nwprotocolframerimplementation/cleanup(framer:))
- [static var label: String](/documentation/network/nwprotocolframerimplementation/label)

#### Handling Data

- [func handleOutput(framer: NWProtocolFramer.Instance, message: NWProtocolFramer.Message, messageLength: Int, isComplete: Bool)](/documentation/network/nwprotocolframerimplementation/handleoutput(framer:message:messagelength:iscomplete:))
- [func handleInput(framer: NWProtocolFramer.Instance) -> Int](/documentation/network/nwprotocolframerimplementation/handleinput(framer:))
- [NWProtocolFramer.Instance](/documentation/network/nwprotocolframer/instance)

#### Writing Output

- [func parseOutput(minimumIncompleteLength: Int, maximumLength: Int, parse: (UnsafeMutableRawBufferPointer?, Bool) -> Int) -> Bool](/documentation/network/nwprotocolframer/instance/parseoutput(minimumincompletelength:maximumlength:parse:))
- [func writeOutput(data: Data)](/documentation/network/nwprotocolframer/instance/writeoutput(data:)-ydvk)
- [func writeOutputNoCopy(length: Int) throws](/documentation/network/nwprotocolframer/instance/writeoutputnocopy(length:))
- [func passThroughOutput()](/documentation/network/nwprotocolframer/instance/passthroughoutput())

#### Delivering Input

- [func parseInput(minimumIncompleteLength: Int, maximumLength: Int, parse: (UnsafeMutableRawBufferPointer?, Bool) -> Int) -> Bool](/documentation/network/nwprotocolframer/instance/parseinput(minimumincompletelength:maximumlength:parse:))
- [func deliverInput(data: Data, message: NWProtocolFramer.Message, isComplete: Bool)](/documentation/network/nwprotocolframer/instance/deliverinput(data:message:iscomplete:))
- [func deliverInputNoCopy(length: Int, message: NWProtocolFramer.Message, isComplete: Bool) -> Bool](/documentation/network/nwprotocolframer/instance/deliverinputnocopy(length:message:iscomplete:))
- [func passThroughInput()](/documentation/network/nwprotocolframer/instance/passthroughinput())

#### Managing Instance Lifetime

- [func markReady()](/documentation/network/nwprotocolframer/instance/markready())
- [func markFailed(error: NWError?)](/documentation/network/nwprotocolframer/instance/markfailed(error:))
- [func prependApplicationProtocol(options: NWProtocolOptions) throws](/documentation/network/nwprotocolframer/instance/prependapplicationprotocol(options:))

#### Inspecting Instance Properties

- [var remote: NWEndpoint?](/documentation/network/nwprotocolframer/instance/remote)
- [var local: NWEndpoint?](/documentation/network/nwprotocolframer/instance/local)
- [var parameters: NWParameters?](/documentation/network/nwprotocolframer/instance/parameters)

#### Handling Asynchronous Events

- [func async(execute: () -> Void)](/documentation/network/nwprotocolframer/instance/async(execute:))
- [func scheduleWakeup(wakeupTime: NWProtocolFramer.Instance.WakeupTime)](/documentation/network/nwprotocolframer/instance/schedulewakeup(wakeuptime:))
- [NWProtocolFramer.Instance.WakeupTime](/documentation/network/nwprotocolframer/instance/wakeuptime)

##### Time Values

- [case milliseconds(UInt64)](/documentation/network/nwprotocolframer/instance/wakeuptime/milliseconds(_:))
- [case forever](/documentation/network/nwprotocolframer/instance/wakeuptime/forever)

#### Instance Properties

- [var options: NWProtocolFramer.Options](/documentation/network/nwprotocolframer/instance/options)

#### Instance Methods

- [func writeOutput<Output>(data: Output)](/documentation/network/nwprotocolframer/instance/writeoutput(data:)-9axn3)

### Using Framers with Connections

- [NWProtocolFramer.Definition](/documentation/network/nwprotocolframer/definition)

#### Defining Framer Protocols

- [init(implementation: any NWProtocolFramerImplementation.Type)](/documentation/network/nwprotocolframer/definition/init(implementation:))
- [NWProtocolFramer.Options](/documentation/network/nwprotocolframer/options)

#### Creating Framer Options

- [init(definition: NWProtocolFramer.Definition)](/documentation/network/nwprotocolframer/options/init(definition:))

#### Subscripts

- [subscript(String) -> Any?](/documentation/network/nwprotocolframer/options/subscript(_:))
- [NWProtocolFramer.Message](/documentation/network/nwprotocolframer/message)

#### Creating Framer Messages

- [init(definition: NWProtocolFramer.Definition)](/documentation/network/nwprotocolframer/message/init(definition:))
- [init(instance: NWProtocolFramer.Instance)](/documentation/network/nwprotocolframer/message/init(instance:))

#### Accessing Message Metadata

- [subscript(String) -> Any?](/documentation/network/nwprotocolframer/message/subscript(_:))

### Enumerations

- [NWProtocolFramer.StartResult](/documentation/network/nwprotocolframer/startresult)

#### Start Results

- [case ready](/documentation/network/nwprotocolframer/startresult/ready)
- [case willMarkReady](/documentation/network/nwprotocolframer/startresult/willmarkready)

## Network Security and Privacy

- [Security Options](/documentation/network/security-options)

### Configuring TLS Handshake Options

- [sec_protocol_options_t](/documentation/security/sec_protocol_options_t)
- [OS_sec_protocol_options](/documentation/security/os_sec_protocol_options)
- [func sec_protocol_options_set_tls_server_name(sec_protocol_options_t, UnsafePointer<CChar>)](/documentation/security/sec_protocol_options_set_tls_server_name(_:_:))
- [func sec_protocol_options_add_pre_shared_key(sec_protocol_options_t, dispatch_data_t, dispatch_data_t)](/documentation/security/sec_protocol_options_add_pre_shared_key(_:_:_:))
- [func sec_protocol_options_add_tls_application_protocol(sec_protocol_options_t, UnsafePointer<CChar>)](/documentation/security/sec_protocol_options_add_tls_application_protocol(_:_:))
- [func sec_protocol_options_append_tls_ciphersuite(sec_protocol_options_t, tls_ciphersuite_t)](/documentation/security/sec_protocol_options_append_tls_ciphersuite(_:_:))
- [func sec_protocol_options_append_tls_ciphersuite_group(sec_protocol_options_t, tls_ciphersuite_group_t)](/documentation/security/sec_protocol_options_append_tls_ciphersuite_group(_:_:))
- [func sec_protocol_options_add_tls_ciphersuite(sec_protocol_options_t, SSLCipherSuite)](/documentation/security/sec_protocol_options_add_tls_ciphersuite(_:_:))
- [func sec_protocol_options_add_tls_ciphersuite_group(sec_protocol_options_t, SSLCiphersuiteGroup)](/documentation/security/sec_protocol_options_add_tls_ciphersuite_group(_:_:))
- [func sec_protocol_options_set_tls_diffie_hellman_parameters(sec_protocol_options_t, dispatch_data_t)](/documentation/security/sec_protocol_options_set_tls_diffie_hellman_parameters(_:_:))
- [func sec_protocol_options_are_equal(sec_protocol_options_t, sec_protocol_options_t) -> Bool](/documentation/security/sec_protocol_options_are_equal(_:_:))

### Configuring TLS Versions

- [func sec_protocol_options_set_min_tls_protocol_version(sec_protocol_options_t, tls_protocol_version_t)](/documentation/security/sec_protocol_options_set_min_tls_protocol_version(_:_:))
- [func sec_protocol_options_set_max_tls_protocol_version(sec_protocol_options_t, tls_protocol_version_t)](/documentation/security/sec_protocol_options_set_max_tls_protocol_version(_:_:))
- [func sec_protocol_options_get_default_min_tls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_min_tls_protocol_version())
- [func sec_protocol_options_get_default_max_tls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_max_tls_protocol_version())
- [func sec_protocol_options_get_default_min_dtls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_min_dtls_protocol_version())
- [func sec_protocol_options_get_default_max_dtls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_max_dtls_protocol_version())
- [func sec_protocol_options_set_tls_min_version(sec_protocol_options_t, SSLProtocol)](/documentation/security/sec_protocol_options_set_tls_min_version(_:_:))
- [func sec_protocol_options_set_tls_max_version(sec_protocol_options_t, SSLProtocol)](/documentation/security/sec_protocol_options_set_tls_max_version(_:_:))

### Configuring TLS Behavior

- [func sec_protocol_options_set_tls_resumption_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_resumption_enabled(_:_:))
- [func sec_protocol_options_set_tls_tickets_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_tickets_enabled(_:_:))
- [func sec_protocol_options_set_tls_false_start_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_false_start_enabled(_:_:))
- [func sec_protocol_options_set_tls_sct_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_sct_enabled(_:_:))
- [func sec_protocol_options_set_tls_ocsp_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_ocsp_enabled(_:_:))
- [func sec_protocol_options_set_tls_renegotiation_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_renegotiation_enabled(_:_:))
- [func sec_protocol_options_set_peer_authentication_required(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_peer_authentication_required(_:_:))
- [func sec_protocol_options_set_tls_is_fallback_attempt(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_is_fallback_attempt(_:_:))
- [func sec_protocol_options_set_tls_pre_shared_key_identity_hint(sec_protocol_options_t, dispatch_data_t)](/documentation/security/sec_protocol_options_set_tls_pre_shared_key_identity_hint(_:_:))

### Handling TLS Events

- [func sec_protocol_options_set_verify_block(sec_protocol_options_t, sec_protocol_verify_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_verify_block(_:_:_:))
- [sec_protocol_verify_t](/documentation/security/sec_protocol_verify_t)
- [sec_protocol_verify_complete_t](/documentation/security/sec_protocol_verify_complete_t)
- [func sec_protocol_options_set_challenge_block(sec_protocol_options_t, sec_protocol_challenge_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_challenge_block(_:_:_:))
- [sec_protocol_challenge_t](/documentation/security/sec_protocol_challenge_t)
- [sec_protocol_challenge_complete_t](/documentation/security/sec_protocol_challenge_complete_t)
- [func sec_protocol_options_set_key_update_block(sec_protocol_options_t, sec_protocol_key_update_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_key_update_block(_:_:_:))
- [sec_protocol_key_update_t](/documentation/security/sec_protocol_key_update_t)
- [sec_protocol_key_update_complete_t](/documentation/security/sec_protocol_key_update_complete_t)
- [func sec_protocol_options_set_pre_shared_key_selection_block(sec_protocol_options_t, sec_protocol_pre_shared_key_selection_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_pre_shared_key_selection_block(_:_:_:))
- [sec_protocol_pre_shared_key_selection_t](/documentation/security/sec_protocol_pre_shared_key_selection_t)
- [sec_protocol_pre_shared_key_selection_complete_t](/documentation/security/sec_protocol_pre_shared_key_selection_complete_t)

### Inspecting TLS State

- [sec_protocol_metadata_t](/documentation/security/sec_protocol_metadata_t)
- [OS_sec_protocol_metadata](/documentation/security/os_sec_protocol_metadata)
- [func sec_protocol_metadata_get_negotiated_protocol(sec_protocol_metadata_t) -> UnsafePointer<CChar>?](/documentation/security/sec_protocol_metadata_get_negotiated_protocol(_:))
- [func sec_protocol_metadata_get_server_name(sec_protocol_metadata_t) -> UnsafePointer<CChar>?](/documentation/security/sec_protocol_metadata_get_server_name(_:))
- [func sec_protocol_metadata_get_negotiated_tls_protocol_version(sec_protocol_metadata_t) -> tls_protocol_version_t](/documentation/security/sec_protocol_metadata_get_negotiated_tls_protocol_version(_:))
- [func sec_protocol_metadata_get_negotiated_tls_ciphersuite(sec_protocol_metadata_t) -> tls_ciphersuite_t](/documentation/security/sec_protocol_metadata_get_negotiated_tls_ciphersuite(_:))
- [func sec_protocol_metadata_get_negotiated_protocol_version(sec_protocol_metadata_t) -> SSLProtocol](/documentation/security/sec_protocol_metadata_get_negotiated_protocol_version(_:))
- [func sec_protocol_metadata_get_negotiated_ciphersuite(sec_protocol_metadata_t) -> SSLCipherSuite](/documentation/security/sec_protocol_metadata_get_negotiated_ciphersuite(_:))
- [func sec_protocol_metadata_get_early_data_accepted(sec_protocol_metadata_t) -> Bool](/documentation/security/sec_protocol_metadata_get_early_data_accepted(_:))
- [func sec_protocol_metadata_copy_peer_public_key(sec_protocol_metadata_t) -> dispatch_data_t?](/documentation/security/sec_protocol_metadata_copy_peer_public_key(_:))

### Handling TLS Challenges

- [func sec_protocol_metadata_access_distinguished_names(sec_protocol_metadata_t, (dispatch_data_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_distinguished_names(_:_:))
- [func sec_protocol_metadata_access_ocsp_response(sec_protocol_metadata_t, (dispatch_data_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_ocsp_response(_:_:))
- [func sec_protocol_metadata_access_peer_certificate_chain(sec_protocol_metadata_t, (sec_certificate_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_peer_certificate_chain(_:_:))
- [func sec_protocol_metadata_access_supported_signature_algorithms(sec_protocol_metadata_t, (UInt16) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_supported_signature_algorithms(_:_:))
- [func sec_protocol_metadata_access_pre_shared_keys(sec_protocol_metadata_t, (dispatch_data_t, dispatch_data_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_pre_shared_keys(_:_:))
- [func sec_protocol_metadata_create_secret(sec_protocol_metadata_t, Int, UnsafePointer<CChar>, Int) -> dispatch_data_t?](/documentation/security/sec_protocol_metadata_create_secret(_:_:_:_:))
- [func sec_protocol_metadata_create_secret_with_context(sec_protocol_metadata_t, Int, UnsafePointer<CChar>, Int, UnsafePointer<UInt8>, Int) -> dispatch_data_t?](/documentation/security/sec_protocol_metadata_create_secret_with_context(_:_:_:_:_:_:))
- [func sec_protocol_metadata_peers_are_equal(sec_protocol_metadata_t, sec_protocol_metadata_t) -> Bool](/documentation/security/sec_protocol_metadata_peers_are_equal(_:_:))
- [func sec_protocol_metadata_challenge_parameters_are_equal(sec_protocol_metadata_t, sec_protocol_metadata_t) -> Bool](/documentation/security/sec_protocol_metadata_challenge_parameters_are_equal(_:_:))

### Handling Certificates

- [sec_certificate_t](/documentation/security/sec_certificate_t)
- [OS_sec_certificate](/documentation/security/os_sec_certificate)
- [func sec_certificate_create(SecCertificate) -> sec_certificate_t?](/documentation/security/sec_certificate_create(_:))
- [func sec_certificate_copy_ref(sec_certificate_t) -> Unmanaged<SecCertificate>](/documentation/security/sec_certificate_copy_ref(_:))

### Handling Identities

- [func sec_protocol_options_set_local_identity(sec_protocol_options_t, sec_identity_t)](/documentation/security/sec_protocol_options_set_local_identity(_:_:))
- [sec_identity_t](/documentation/security/sec_identity_t)
- [OS_sec_identity](/documentation/security/os_sec_identity)
- [func sec_identity_create(SecIdentity) -> sec_identity_t?](/documentation/security/sec_identity_create(_:))
- [func sec_identity_create_with_certificates(SecIdentity, CFArray) -> sec_identity_t?](/documentation/security/sec_identity_create_with_certificates(_:_:))
- [func sec_identity_copy_ref(sec_identity_t) -> Unmanaged<SecIdentity>?](/documentation/security/sec_identity_copy_ref(_:))
- [func sec_identity_access_certificates(sec_identity_t, (sec_certificate_t) -> Void) -> Bool](/documentation/security/sec_identity_access_certificates(_:_:))
- [func sec_identity_copy_certificates_ref(sec_identity_t) -> Unmanaged<CFArray>?](/documentation/security/sec_identity_copy_certificates_ref(_:))

### Handling Trust

- [sec_trust_t](/documentation/security/sec_trust_t)
- [OS_sec_trust](/documentation/security/os_sec_trust)
- [func sec_trust_create(SecTrust) -> sec_trust_t?](/documentation/security/sec_trust_create(_:))
- [func sec_trust_copy_ref(sec_trust_t) -> Unmanaged<SecTrust>](/documentation/security/sec_trust_copy_ref(_:))

### Managing Security Objects

- [func sec_release(UnsafeMutableRawPointer!)](/documentation/security/sec_release(_:))
- [func sec_retain(UnsafeMutableRawPointer!) -> UnsafeMutableRawPointer!](/documentation/security/sec_retain(_:))
- [sec_object_t](/documentation/security/sec_object_t)
- [OS_sec_object](/documentation/security/os_sec_object)
- [Privacy Management](/documentation/network/privacy-management)

### Traffic Attribution

- [Inspecting app activity data](/documentation/network/inspecting-app-activity-data)
- [Indicating the source of network activity](/documentation/network/indicating-the-source-of-network-activity)
- [func nw_parameters_set_attribution(nw_parameters_t, nw_parameters_attribution_t)](/documentation/network/nw_parameters_set_attribution(_:_:))
- [func nw_parameters_get_attribution(nw_parameters_t) -> nw_parameters_attribution_t](/documentation/network/nw_parameters_get_attribution(_:))
- [nw_parameters_attribution_t](/documentation/network/nw_parameters_attribution_t)

#### Request Sources

- [case developer](/documentation/network/nw_parameters_attribution_t/developer)
- [case user](/documentation/network/nw_parameters_attribution_t/user)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/network/nw_parameters_attribution_t/init(rawvalue:))
- [Creating an Identity for Local Network TLS](/documentation/network/creating-an-identity-for-local-network-tls)

## Paths and Interfaces

- [NWPath](/documentation/network/nwpath)

### Checking Path Availability

- [let status: NWPath.Status](/documentation/network/nwpath/status-swift.property)
- [NWPath.Status](/documentation/network/nwpath/status-swift.enum)

#### Status Values

- [case unsatisfied](/documentation/network/nwpath/status-swift.enum/unsatisfied)
- [case satisfied](/documentation/network/nwpath/status-swift.enum/satisfied)
- [case requiresConnection](/documentation/network/nwpath/status-swift.enum/requiresconnection)

### Inspecting Interfaces

- [func usesInterfaceType(NWInterface.InterfaceType) -> Bool](/documentation/network/nwpath/usesinterfacetype(_:))
- [let availableInterfaces: [NWInterface]](/documentation/network/nwpath/availableinterfaces)
- [var gateways: [NWEndpoint]](/documentation/network/nwpath/gateways)

### Checking Path Capabilities

- [let supportsIPv4: Bool](/documentation/network/nwpath/supportsipv4)
- [let supportsIPv6: Bool](/documentation/network/nwpath/supportsipv6)
- [let supportsDNS: Bool](/documentation/network/nwpath/supportsdns)
- [var isConstrained: Bool](/documentation/network/nwpath/isconstrained)
- [let isExpensive: Bool](/documentation/network/nwpath/isexpensive)

### Inspecting Connected Paths

- [let localEndpoint: NWEndpoint?](/documentation/network/nwpath/localendpoint)
- [let remoteEndpoint: NWEndpoint?](/documentation/network/nwpath/remoteendpoint)

### Instance Properties

- [var isUltraConstrained: Bool](/documentation/network/nwpath/isultraconstrained)
- [var linkQuality: NWPath.LinkQuality](/documentation/network/nwpath/linkquality-swift.property)
- [var unsatisfiedReason: NWPath.UnsatisfiedReason](/documentation/network/nwpath/unsatisfiedreason-swift.property)
- [var wifiAware: WAPath?](/documentation/network/nwpath/wifiaware)

### Enumerations

- [NWPath.LinkQuality](/documentation/network/nwpath/linkquality-swift.enum)

#### Enumeration Cases

- [case good](/documentation/network/nwpath/linkquality-swift.enum/good)
- [case minimal](/documentation/network/nwpath/linkquality-swift.enum/minimal)
- [case moderate](/documentation/network/nwpath/linkquality-swift.enum/moderate)
- [case unknown](/documentation/network/nwpath/linkquality-swift.enum/unknown)
- [NWPath.UnsatisfiedReason](/documentation/network/nwpath/unsatisfiedreason-swift.enum)

#### Enumeration Cases

- [case cellularDenied](/documentation/network/nwpath/unsatisfiedreason-swift.enum/cellulardenied)
- [case localNetworkDenied](/documentation/network/nwpath/unsatisfiedreason-swift.enum/localnetworkdenied)
- [case notAvailable](/documentation/network/nwpath/unsatisfiedreason-swift.enum/notavailable)
- [case vpnInactive](/documentation/network/nwpath/unsatisfiedreason-swift.enum/vpninactive)
- [case wifiDenied](/documentation/network/nwpath/unsatisfiedreason-swift.enum/wifidenied)
- [NWPathMonitor](/documentation/network/nwpathmonitor)

### Creating Path Monitors

- [init()](/documentation/network/nwpathmonitor/init())
- [init(requiredInterfaceType: NWInterface.InterfaceType)](/documentation/network/nwpathmonitor/init(requiredinterfacetype:))
- [init(prohibitedInterfaceTypes: [NWInterface.InterfaceType])](/documentation/network/nwpathmonitor/init(prohibitedinterfacetypes:))
- [func start(queue: DispatchQueue)](/documentation/network/nwpathmonitor/start(queue:))
- [var queue: DispatchQueue?](/documentation/network/nwpathmonitor/queue)

### Handling Path Updates

- [var currentPath: NWPath](/documentation/network/nwpathmonitor/currentpath)
- [var pathUpdateHandler: ((NWPath) -> Void)?](/documentation/network/nwpathmonitor/pathupdatehandler)

### Canceling Path Monitors

- [func cancel()](/documentation/network/nwpathmonitor/cancel())

### Structures

- [NWPathMonitor.Iterator](/documentation/network/nwpathmonitor/iterator)

### Type Properties

- [static var ethernetChannel: NWPathMonitor](/documentation/network/nwpathmonitor/ethernetchannel)
- [NWInterface](/documentation/network/nwinterface)

### Inspecting Interfaces

- [var type: NWInterface.InterfaceType](/documentation/network/nwinterface/type)
- [NWInterface.InterfaceType](/documentation/network/nwinterface/interfacetype)

#### Interface Types

- [case wifi](/documentation/network/nwinterface/interfacetype/wifi)
- [case cellular](/documentation/network/nwinterface/interfacetype/cellular)
- [case wiredEthernet](/documentation/network/nwinterface/interfacetype/wiredethernet)
- [case loopback](/documentation/network/nwinterface/interfacetype/loopback)
- [case other](/documentation/network/nwinterface/interfacetype/other)
- [var name: String](/documentation/network/nwinterface/name)
- [var index: Int](/documentation/network/nwinterface/index)

### Enumerations

- [NWInterface.RadioType](/documentation/network/nwinterface/radiotype)

#### Enumeration Cases

- [case cell(NWInterface.RadioType.Cellular)](/documentation/network/nwinterface/radiotype/cell(_:))
- [case wifi(NWInterface.RadioType.WiFi)](/documentation/network/nwinterface/radiotype/wifi(_:))

#### Enumerations

- [NWInterface.RadioType.Cellular](/documentation/network/nwinterface/radiotype/cellular)

##### Enumeration Cases

- [case cdma](/documentation/network/nwinterface/radiotype/cellular/cdma)
- [case dualConnectivity5G(NWInterface.RadioType.Cellular.NewRadio5GVariant)](/documentation/network/nwinterface/radiotype/cellular/dualconnectivity5g(_:))
- [case evdo](/documentation/network/nwinterface/radiotype/cellular/evdo)
- [case gsm](/documentation/network/nwinterface/radiotype/cellular/gsm)
- [case lte](/documentation/network/nwinterface/radiotype/cellular/lte)
- [case standalone5G(NWInterface.RadioType.Cellular.NewRadio5GVariant)](/documentation/network/nwinterface/radiotype/cellular/standalone5g(_:))
- [case wcdma](/documentation/network/nwinterface/radiotype/cellular/wcdma)

##### Enumerations

- [NWInterface.RadioType.Cellular.NewRadio5GVariant](/documentation/network/nwinterface/radiotype/cellular/newradio5gvariant)

###### Enumeration Cases

- [case mmWave](/documentation/network/nwinterface/radiotype/cellular/newradio5gvariant/mmwave)
- [case sub6GHz](/documentation/network/nwinterface/radiotype/cellular/newradio5gvariant/sub6ghz)
- [NWInterface.RadioType.WiFi](/documentation/network/nwinterface/radiotype/wifi)

##### Enumeration Cases

- [case a](/documentation/network/nwinterface/radiotype/wifi/a)
- [case ac](/documentation/network/nwinterface/radiotype/wifi/ac)
- [case ax](/documentation/network/nwinterface/radiotype/wifi/ax)
- [case b](/documentation/network/nwinterface/radiotype/wifi/b)
- [case g](/documentation/network/nwinterface/radiotype/wifi/g)
- [case n](/documentation/network/nwinterface/radiotype/wifi/n)

## Errors

- [NWError](/documentation/network/nwerror)

### Checking Error Types

- [case posix(POSIXErrorCode)](/documentation/network/nwerror/posix(_:))
- [case dns(DNSServiceErrorType)](/documentation/network/nwerror/dns(_:))
- [case tls(OSStatus)](/documentation/network/nwerror/tls(_:))

### Enumeration Cases

- [case wifiAware(Int32)](/documentation/network/nwerror/wifiaware(_:))

### Instance Properties

- [var wifiAware: WAError?](/documentation/network/nwerror/wifiaware)

## Network Debugging

- [Choosing a Network Debugging Tool](/documentation/network/choosing-a-network-debugging-tool)
- [Debugging HTTP Server-Side Errors](/documentation/network/debugging-http-server-side-errors)
- [Debugging HTTPS Problems with CFNetwork Diagnostic Logging](/documentation/network/debugging-https-problems-with-cfnetwork-diagnostic-logging)
- [Recording a Packet Trace](/documentation/network/recording-a-packet-trace)

### Working with Packet Traces

- [Troubleshooting Packet Traces](/documentation/network/troubleshooting-packet-traces)
- [Recording a Wi-Fi Packet Trace](/documentation/network/recording-a-wi-fi-packet-trace)
- [Submitting a Packet Trace to Apple](/documentation/network/submitting-a-packet-trace-to-apple)
- [Taking Advantage of Third-Party Network Debugging Tools](/documentation/network/taking-advantage-of-third-party-network-debugging-tools)
- [Testing and Debugging L4S in Your App](/documentation/network/testing-and-debugging-l4s-in-your-app)

## C-Language Symbols

- [C-Language Symbols](/documentation/network/c-language-symbols)

### C Network Structures

- [nw_connection_group_state_t](/documentation/network/nw_connection_group_state_t)

#### States

- [var nw_connection_group_state_invalid: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_invalid)
- [var nw_connection_group_state_waiting: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_waiting)
- [var nw_connection_group_state_ready: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_ready)
- [var nw_connection_group_state_failed: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_failed)
- [var nw_connection_group_state_cancelled: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_cancelled)

#### Initializers

- [init(UInt32)](/documentation/network/nw_connection_group_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_connection_group_state_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_connection_group_state_t/rawvalue)
- [nw_browser_state_t](/documentation/network/nw_browser_state_t)

#### States

- [var nw_browser_state_invalid: nw_browser_state_t](/documentation/network/nw_browser_state_invalid)
- [var nw_browser_state_ready: nw_browser_state_t](/documentation/network/nw_browser_state_ready)
- [var nw_browser_state_failed: nw_browser_state_t](/documentation/network/nw_browser_state_failed)
- [var nw_browser_state_cancelled: nw_browser_state_t](/documentation/network/nw_browser_state_cancelled)

#### Initializers

- [init(UInt32)](/documentation/network/nw_browser_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_browser_state_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_browser_state_t/rawvalue)
- [nw_connection_state_t](/documentation/network/nw_connection_state_t)

#### Connection States

- [var nw_connection_state_invalid: nw_connection_state_t](/documentation/network/nw_connection_state_invalid)
- [var nw_connection_state_waiting: nw_connection_state_t](/documentation/network/nw_connection_state_waiting)
- [var nw_connection_state_preparing: nw_connection_state_t](/documentation/network/nw_connection_state_preparing)
- [var nw_connection_state_ready: nw_connection_state_t](/documentation/network/nw_connection_state_ready)
- [var nw_connection_state_failed: nw_connection_state_t](/documentation/network/nw_connection_state_failed)
- [var nw_connection_state_cancelled: nw_connection_state_t](/documentation/network/nw_connection_state_cancelled)

#### Initializers

- [init(UInt32)](/documentation/network/nw_connection_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_connection_state_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_connection_state_t/rawvalue)
- [nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_t)

#### Report States

- [var nw_data_transfer_report_state_collecting: nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_collecting)
- [var nw_data_transfer_report_state_collected: nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_collected)

#### Initializers

- [init(UInt32)](/documentation/network/nw_data_transfer_report_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_data_transfer_report_state_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_data_transfer_report_state_t/rawvalue)
- [nw_endpoint_type_t](/documentation/network/nw_endpoint_type_t)

#### Endpoint Types

- [var nw_endpoint_type_invalid: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_invalid)
- [var nw_endpoint_type_address: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_address)
- [var nw_endpoint_type_host: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_host)
- [var nw_endpoint_type_bonjour_service: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_bonjour_service)
- [var nw_endpoint_type_url: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_url)

#### Initializers

- [init(UInt32)](/documentation/network/nw_endpoint_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_endpoint_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_endpoint_type_t/rawvalue)
- [nw_error_domain_t](/documentation/network/nw_error_domain_t)

#### Error Domain Constants

- [var nw_error_domain_invalid: nw_error_domain_t](/documentation/network/nw_error_domain_invalid)
- [var nw_error_domain_posix: nw_error_domain_t](/documentation/network/nw_error_domain_posix)
- [var nw_error_domain_dns: nw_error_domain_t](/documentation/network/nw_error_domain_dns)
- [var nw_error_domain_tls: nw_error_domain_t](/documentation/network/nw_error_domain_tls)

#### CFError Domain Constants

- [let kNWErrorDomainPOSIX: CFString](/documentation/network/knwerrordomainposix)
- [let kNWErrorDomainDNS: CFString](/documentation/network/knwerrordomaindns)
- [let kNWErrorDomainTLS: CFString](/documentation/network/knwerrordomaintls)

#### Initializers

- [init(UInt32)](/documentation/network/nw_error_domain_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_error_domain_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_error_domain_t/rawvalue)
- [nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_t)

#### States

- [var nw_ethernet_channel_state_invalid: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_invalid)
- [var nw_ethernet_channel_state_waiting: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_waiting)
- [var nw_ethernet_channel_state_preparing: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_preparing)
- [var nw_ethernet_channel_state_ready: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_ready)
- [var nw_ethernet_channel_state_failed: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_failed)
- [var nw_ethernet_channel_state_cancelled: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_cancelled)

#### Initializers

- [init(UInt32)](/documentation/network/nw_ethernet_channel_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ethernet_channel_state_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ethernet_channel_state_t/rawvalue)
- [nw_framer_start_result_t](/documentation/network/nw_framer_start_result_t)

#### Start Results

- [var nw_framer_start_result_ready: nw_framer_start_result_t](/documentation/network/nw_framer_start_result_ready)
- [var nw_framer_start_result_will_mark_ready: nw_framer_start_result_t](/documentation/network/nw_framer_start_result_will_mark_ready)

#### Initializers

- [init(UInt32)](/documentation/network/nw_framer_start_result_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_framer_start_result_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_framer_start_result_t/rawvalue)
- [nw_interface_type_t](/documentation/network/nw_interface_type_t)

#### Creating an interface type instance

- [init(UInt32)](/documentation/network/nw_interface_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_interface_type_t/init(rawvalue:))

#### Interface types

- [var nw_interface_type_wifi: nw_interface_type_t](/documentation/network/nw_interface_type_wifi)
- [var nw_interface_type_cellular: nw_interface_type_t](/documentation/network/nw_interface_type_cellular)
- [var nw_interface_type_wired: nw_interface_type_t](/documentation/network/nw_interface_type_wired)
- [var nw_interface_type_loopback: nw_interface_type_t](/documentation/network/nw_interface_type_loopback)
- [var nw_interface_type_other: nw_interface_type_t](/documentation/network/nw_interface_type_other)

#### Accessing the raw value

- [var rawValue: UInt32](/documentation/network/nw_interface_type_t/rawvalue)
- [nw_ip_ecn_flag_t](/documentation/network/nw_ip_ecn_flag_t)

#### ECN Flags

- [var nw_ip_ecn_flag_non_ect: nw_ip_ecn_flag_t](/documentation/network/nw_ip_ecn_flag_non_ect)
- [var nw_ip_ecn_flag_ect_0: nw_ip_ecn_flag_t](/documentation/network/nw_ip_ecn_flag_ect_0)
- [var nw_ip_ecn_flag_ect_1: nw_ip_ecn_flag_t](/documentation/network/nw_ip_ecn_flag_ect_1)
- [var nw_ip_ecn_flag_ce: nw_ip_ecn_flag_t](/documentation/network/nw_ip_ecn_flag_ce)

#### Initializers

- [init(UInt32)](/documentation/network/nw_ip_ecn_flag_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ip_ecn_flag_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ip_ecn_flag_t/rawvalue)
- [nw_ip_local_address_preference_t](/documentation/network/nw_ip_local_address_preference_t)

#### Address Preferences

- [var nw_ip_local_address_preference_default: nw_ip_local_address_preference_t](/documentation/network/nw_ip_local_address_preference_default)
- [var nw_ip_local_address_preference_temporary: nw_ip_local_address_preference_t](/documentation/network/nw_ip_local_address_preference_temporary)
- [var nw_ip_local_address_preference_stable: nw_ip_local_address_preference_t](/documentation/network/nw_ip_local_address_preference_stable)

#### Initializers

- [init(UInt32)](/documentation/network/nw_ip_local_address_preference_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ip_local_address_preference_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ip_local_address_preference_t/rawvalue)
- [nw_ip_version_t](/documentation/network/nw_ip_version_t)

#### Versions

- [var nw_ip_version_any: nw_ip_version_t](/documentation/network/nw_ip_version_any)
- [var nw_ip_version_4: nw_ip_version_t](/documentation/network/nw_ip_version_4)
- [var nw_ip_version_6: nw_ip_version_t](/documentation/network/nw_ip_version_6)

#### Initializers

- [init(UInt32)](/documentation/network/nw_ip_version_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ip_version_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ip_version_t/rawvalue)
- [nw_listener_state_t](/documentation/network/nw_listener_state_t)

#### Listener States

- [var nw_listener_state_invalid: nw_listener_state_t](/documentation/network/nw_listener_state_invalid)
- [var nw_listener_state_waiting: nw_listener_state_t](/documentation/network/nw_listener_state_waiting)
- [var nw_listener_state_ready: nw_listener_state_t](/documentation/network/nw_listener_state_ready)
- [var nw_listener_state_failed: nw_listener_state_t](/documentation/network/nw_listener_state_failed)
- [var nw_listener_state_cancelled: nw_listener_state_t](/documentation/network/nw_listener_state_cancelled)

#### Initializers

- [init(UInt32)](/documentation/network/nw_listener_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_listener_state_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_listener_state_t/rawvalue)
- [nw_multipath_service_t](/documentation/network/nw_multipath_service_t)

#### Creating a multipath service type instance

- [init(UInt32)](/documentation/network/nw_multipath_service_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_multipath_service_t/init(rawvalue:))

#### Multipath service types

- [var nw_multipath_service_disabled: nw_multipath_service_t](/documentation/network/nw_multipath_service_disabled)
- [var nw_multipath_service_handover: nw_multipath_service_t](/documentation/network/nw_multipath_service_handover)
- [var nw_multipath_service_interactive: nw_multipath_service_t](/documentation/network/nw_multipath_service_interactive)
- [var nw_multipath_service_aggregate: nw_multipath_service_t](/documentation/network/nw_multipath_service_aggregate)

#### Accessing the raw value

- [var rawValue: UInt32](/documentation/network/nw_multipath_service_t/rawvalue)
- [nw_parameters_expired_dns_behavior_t](/documentation/network/nw_parameters_expired_dns_behavior_t)

#### Creating an expired DNS behavior instance

- [init(UInt32)](/documentation/network/nw_parameters_expired_dns_behavior_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_parameters_expired_dns_behavior_t/init(rawvalue:))

#### Expired DNS behaviors

- [var nw_parameters_expired_dns_behavior_default: nw_parameters_expired_dns_behavior_t](/documentation/network/nw_parameters_expired_dns_behavior_default)
- [var nw_parameters_expired_dns_behavior_allow: nw_parameters_expired_dns_behavior_t](/documentation/network/nw_parameters_expired_dns_behavior_allow)
- [var nw_parameters_expired_dns_behavior_prohibit: nw_parameters_expired_dns_behavior_t](/documentation/network/nw_parameters_expired_dns_behavior_prohibit)

#### Accessing the raw value

- [var rawValue: UInt32](/documentation/network/nw_parameters_expired_dns_behavior_t/rawvalue)
- [nw_path_status_t](/documentation/network/nw_path_status_t)

#### Status Values

- [var nw_path_status_invalid: nw_path_status_t](/documentation/network/nw_path_status_invalid)
- [var nw_path_status_unsatisfied: nw_path_status_t](/documentation/network/nw_path_status_unsatisfied)
- [var nw_path_status_satisfied: nw_path_status_t](/documentation/network/nw_path_status_satisfied)
- [var nw_path_status_satisfiable: nw_path_status_t](/documentation/network/nw_path_status_satisfiable)

#### Initializers

- [init(UInt32)](/documentation/network/nw_path_status_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_path_status_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_path_status_t/rawvalue)
- [nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_t)

#### Resolution Transports

- [var nw_report_resolution_protocol_unknown: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_unknown)
- [var nw_report_resolution_protocol_udp: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_udp)
- [var nw_report_resolution_protocol_tcp: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_tcp)
- [var nw_report_resolution_protocol_tls: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_tls)
- [var nw_report_resolution_protocol_https: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_https)

#### Initializers

- [init(UInt32)](/documentation/network/nw_report_resolution_protocol_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_report_resolution_protocol_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_report_resolution_protocol_t/rawvalue)
- [nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_t)

#### Resolution Sources

- [var nw_report_resolution_source_query: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_query)
- [var nw_report_resolution_source_cache: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_cache)
- [var nw_report_resolution_source_expired_cache: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_expired_cache)

#### Initializers

- [init(UInt32)](/documentation/network/nw_report_resolution_source_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_report_resolution_source_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_report_resolution_source_t/rawvalue)
- [nw_service_class_t](/documentation/network/nw_service_class_t)

#### Creating a service class instance

- [init(UInt32)](/documentation/network/nw_service_class_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_service_class_t/init(rawvalue:))

#### Service classes

- [var nw_service_class_best_effort: nw_service_class_t](/documentation/network/nw_service_class_best_effort)
- [var nw_service_class_background: nw_service_class_t](/documentation/network/nw_service_class_background)
- [var nw_service_class_interactive_video: nw_service_class_t](/documentation/network/nw_service_class_interactive_video)
- [var nw_service_class_interactive_voice: nw_service_class_t](/documentation/network/nw_service_class_interactive_voice)
- [var nw_service_class_responsive_data: nw_service_class_t](/documentation/network/nw_service_class_responsive_data)
- [var nw_service_class_signaling: nw_service_class_t](/documentation/network/nw_service_class_signaling)

#### Accessing the raw value

- [var rawValue: UInt32](/documentation/network/nw_service_class_t/rawvalue)
- [nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_t)

#### Key Value Status

- [var nw_txt_record_find_key_invalid: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_invalid)
- [var nw_txt_record_find_key_not_present: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_not_present)
- [var nw_txt_record_find_key_no_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_no_value)
- [var nw_txt_record_find_key_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_empty_value)
- [var nw_txt_record_find_key_non_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_non_empty_value)

#### Initializers

- [init(UInt32)](/documentation/network/nw_txt_record_find_key_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_txt_record_find_key_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_txt_record_find_key_t/rawvalue)
- [nw_ws_close_code_t](/documentation/network/nw_ws_close_code_t)

#### Defined Close Codes

- [var nw_ws_close_code_normal_closure: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_normal_closure)
- [var nw_ws_close_code_going_away: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_going_away)
- [var nw_ws_close_code_protocol_error: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_protocol_error)
- [var nw_ws_close_code_unsupported_data: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_unsupported_data)
- [var nw_ws_close_code_no_status_received: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_no_status_received)
- [var nw_ws_close_code_abnormal_closure: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_abnormal_closure)
- [var nw_ws_close_code_invalid_frame_payload_data: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_invalid_frame_payload_data)
- [var nw_ws_close_code_policy_violation: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_policy_violation)
- [var nw_ws_close_code_message_too_big: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_message_too_big)
- [var nw_ws_close_code_mandatory_extension: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_mandatory_extension)
- [var nw_ws_close_code_internal_server_error: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_internal_server_error)
- [var nw_ws_close_code_tls_handshake: nw_ws_close_code_t](/documentation/network/nw_ws_close_code_tls_handshake)

#### Initializers

- [init(UInt32)](/documentation/network/nw_ws_close_code_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ws_close_code_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ws_close_code_t/rawvalue)
- [nw_ws_opcode_t](/documentation/network/nw_ws_opcode_t)

#### Data Types

- [var nw_ws_opcode_binary: nw_ws_opcode_t](/documentation/network/nw_ws_opcode_binary)
- [var nw_ws_opcode_text: nw_ws_opcode_t](/documentation/network/nw_ws_opcode_text)
- [var nw_ws_opcode_cont: nw_ws_opcode_t](/documentation/network/nw_ws_opcode_cont)

#### Control Types

- [var nw_ws_opcode_ping: nw_ws_opcode_t](/documentation/network/nw_ws_opcode_ping)
- [var nw_ws_opcode_pong: nw_ws_opcode_t](/documentation/network/nw_ws_opcode_pong)
- [var nw_ws_opcode_close: nw_ws_opcode_t](/documentation/network/nw_ws_opcode_close)
- [var nw_ws_opcode_invalid: nw_ws_opcode_t](/documentation/network/nw_ws_opcode_invalid)

#### Initializers

- [init(Int32)](/documentation/network/nw_ws_opcode_t/init(_:))
- [init(rawValue: Int32)](/documentation/network/nw_ws_opcode_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: Int32](/documentation/network/nw_ws_opcode_t/rawvalue)
- [nw_ws_response_status_t](/documentation/network/nw_ws_response_status_t)

#### Handshake Status Values

- [var nw_ws_response_status_invalid: nw_ws_response_status_t](/documentation/network/nw_ws_response_status_invalid)
- [var nw_ws_response_status_accept: nw_ws_response_status_t](/documentation/network/nw_ws_response_status_accept)
- [var nw_ws_response_status_reject: nw_ws_response_status_t](/documentation/network/nw_ws_response_status_reject)

#### Initializers

- [init(UInt32)](/documentation/network/nw_ws_response_status_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ws_response_status_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ws_response_status_t/rawvalue)
- [nw_ws_version_t](/documentation/network/nw_ws_version_t)

#### Versions

- [var nw_ws_version_invalid: nw_ws_version_t](/documentation/network/nw_ws_version_invalid)
- [var nw_ws_version_13: nw_ws_version_t](/documentation/network/nw_ws_version_13)

#### Initializers

- [init(UInt32)](/documentation/network/nw_ws_version_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ws_version_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ws_version_t/rawvalue)

### C Network Protocols

- [OS_nw_advertise_descriptor](/documentation/network/os_nw_advertise_descriptor)
- [OS_nw_browse_descriptor](/documentation/network/os_nw_browse_descriptor)
- [OS_nw_browse_result](/documentation/network/os_nw_browse_result)
- [OS_nw_browser](/documentation/network/os_nw_browser)
- [OS_nw_connection](/documentation/network/os_nw_connection)
- [OS_nw_connection_group](/documentation/network/os_nw_connection_group)
- [OS_nw_content_context](/documentation/network/os_nw_content_context)
- [OS_nw_data_transfer_report](/documentation/network/os_nw_data_transfer_report)
- [OS_nw_endpoint](/documentation/network/os_nw_endpoint)
- [OS_nw_error](/documentation/network/os_nw_error)
- [OS_nw_establishment_report](/documentation/network/os_nw_establishment_report)
- [OS_nw_ethernet_channel](/documentation/network/os_nw_ethernet_channel)
- [OS_nw_framer](/documentation/network/os_nw_framer)
- [OS_nw_group_descriptor](/documentation/network/os_nw_group_descriptor)
- [OS_nw_interface](/documentation/network/os_nw_interface)
- [OS_nw_listener](/documentation/network/os_nw_listener)
- [OS_nw_object](/documentation/network/os_nw_object)
- [OS_nw_parameters](/documentation/network/os_nw_parameters)
- [OS_nw_path](/documentation/network/os_nw_path)
- [OS_nw_path_monitor](/documentation/network/os_nw_path_monitor)
- [OS_nw_privacy_context](/documentation/network/os_nw_privacy_context)
- [OS_nw_protocol_definition](/documentation/network/os_nw_protocol_definition)
- [OS_nw_protocol_metadata](/documentation/network/os_nw_protocol_metadata)
- [OS_nw_protocol_options](/documentation/network/os_nw_protocol_options)
- [OS_nw_protocol_stack](/documentation/network/os_nw_protocol_stack)
- [OS_nw_proxy_config](/documentation/network/os_nw_proxy_config)
- [OS_nw_relay_hop](/documentation/network/os_nw_relay_hop)
- [OS_nw_resolution_report](/documentation/network/os_nw_resolution_report)
- [OS_nw_resolver_config](/documentation/network/os_nw_resolver_config)
- [OS_nw_txt_record](/documentation/network/os_nw_txt_record)
- [OS_nw_ws_request](/documentation/network/os_nw_ws_request)
- [OS_nw_ws_response](/documentation/network/os_nw_ws_response)

## Structures

- [nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_t)

### Initializers

- [init(UInt32)](/documentation/network/nw_interface_radio_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_interface_radio_type_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_interface_radio_type_t/rawvalue)
- [nw_multipath_version_t](/documentation/network/nw_multipath_version_t)

### Initializers

- [init(Int32)](/documentation/network/nw_multipath_version_t/init(_:))
- [init(rawValue: Int32)](/documentation/network/nw_multipath_version_t/init(rawvalue:))

### Instance Properties

- [var rawValue: Int32](/documentation/network/nw_multipath_version_t/rawvalue)
- [nw_path_unsatisfied_reason_t](/documentation/network/nw_path_unsatisfied_reason_t)

### Initializers

- [init(UInt32)](/documentation/network/nw_path_unsatisfied_reason_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_path_unsatisfied_reason_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_path_unsatisfied_reason_t/rawvalue)
- [nw_quic_stream_type_t](/documentation/network/nw_quic_stream_type_t)

### Initializers

- [init(UInt32)](/documentation/network/nw_quic_stream_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_quic_stream_type_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_quic_stream_type_t/rawvalue)
- [Bonjour](/documentation/network/bonjour)

### Structures

- [Bonjour.Endpoint](/documentation/network/bonjour/endpoint)

#### Operators

- [static func == (Bonjour.Endpoint, Bonjour.Endpoint) -> Bool](/documentation/network/bonjour/endpoint/==(_:_:))

#### Instance Properties

- [var description: String](/documentation/network/bonjour/endpoint/description)
- [let domain: String](/documentation/network/bonjour/endpoint/domain)
- [var id: String](/documentation/network/bonjour/endpoint/id)
- [let name: String](/documentation/network/bonjour/endpoint/name)
- [var nwEndpoint: NWEndpoint](/documentation/network/bonjour/endpoint/nwendpoint)
- [let result: NWBrowser.Result](/documentation/network/bonjour/endpoint/result)
- [let txtRecord: NWTXTRecord](/documentation/network/bonjour/endpoint/txtrecord)
- [let type: String](/documentation/network/bonjour/endpoint/type)
- [BonjourListenerProvider](/documentation/network/bonjourlistenerprovider)

### Initializers

- [init(name: String?, type: String, domain: String?, txtRecord: NWTXTRecord?)](/documentation/network/bonjourlistenerprovider/init(name:type:domain:txtrecord:))

### Instance Properties

- [var service: NWListener.Service](/documentation/network/bonjourlistenerprovider/service)
- [Coder](/documentation/network/coder)

### Initializers

- [init<BelowProtocol>(Sending.Type, using: CoderType, () -> BelowProtocol)](/documentation/network/coder/init(_:using:_:)-61vdl)
- [init<BelowProtocol>(Sending.Type, using: CoderType, () -> BelowProtocol)](/documentation/network/coder/init(_:using:_:)-8o8kw)
- [init<BelowProtocol>(receiving: Receiving.Type, sending: Sending.Type, using: CoderType, () -> BelowProtocol)](/documentation/network/coder/init(receiving:sending:using:_:)-4mm04)
- [init<BelowProtocol>(receiving: Receiving.Type, sending: Sending.Type, using: CoderType, () -> BelowProtocol)](/documentation/network/coder/init(receiving:sending:using:_:)-7d2qd)
- [init<BelowProtocol>(sending: Sending.Type, receiving: Receiving.Type, using: CoderType, () -> BelowProtocol)](/documentation/network/coder/init(sending:receiving:using:_:)-1579q)
- [init<BelowProtocol>(sending: Sending.Type, receiving: Receiving.Type, using: CoderType, () -> BelowProtocol)](/documentation/network/coder/init(sending:receiving:using:_:)-7ox25)
- [DefaultProtocolStorage](/documentation/network/defaultprotocolstorage)
- [Framer](/documentation/network/framer)

### Initializers

- [init<BelowProtocol>(() -> BelowProtocol)](/documentation/network/framer/init(_:)-4jsj5)
- [init<BelowProtocol>(() -> BelowProtocol)](/documentation/network/framer/init(_:)-7946z)
- [init<BelowProtocol>(using: T.Type, () -> BelowProtocol)](/documentation/network/framer/init(using:_:)-16qam)
- [init<BelowProtocol>(using: T.Type, () -> BelowProtocol)](/documentation/network/framer/init(using:_:)-94t7p)

### Instance Properties

- [var options: NWProtocolFramer.Options](/documentation/network/framer/options)
- [IP](/documentation/network/ip)

### Initializers

- [init()](/documentation/network/ip/init())

### Instance Methods

- [func fragmentationDisabled(Bool) -> IP](/documentation/network/ip/fragmentationdisabled(_:))
- [func hopLimit(UInt8) -> IP](/documentation/network/ip/hoplimit(_:))
- [func localAddressPreference(NWProtocolIP.Options.AddressPreference) -> IP](/documentation/network/ip/localaddresspreference(_:))
- [func minimumMTU(Bool) -> IP](/documentation/network/ip/minimummtu(_:))
- [func multicastLoopbackDisabled(Bool) -> IP](/documentation/network/ip/multicastloopbackdisabled(_:))
- [func receiveTimeCalculated(Bool) -> IP](/documentation/network/ip/receivetimecalculated(_:))
- [func version(NWProtocolIP.Options.Version) -> IP](/documentation/network/ip/version(_:))
- [NWParametersBuilder](/documentation/network/nwparametersbuilder)

### Initializers

- [init(() -> (Top, repeat each P))](/documentation/network/nwparametersbuilder/init(_:))
- [init(auto: () -> (Top, repeat each P))](/documentation/network/nwparametersbuilder/init(auto:))

### Instance Methods

- [func wifiAware((inout WAParameters) -> Void) -> NWParametersBuilder<Top, repeat each P>](/documentation/network/nwparametersbuilder/wifiaware(_:))

### Type Methods

- [static func parameters(() -> (Top, repeat each P)) -> NWParametersBuilder<Top, repeat each P>](/documentation/network/nwparametersbuilder/parameters(_:))
- [static func parameters(initialParameters: NWParameters, () -> (Top, repeat each P)) -> NWParametersBuilder<Top, repeat each P>](/documentation/network/nwparametersbuilder/parameters(initialparameters:_:))
- [NWTXTRecord](/documentation/network/nwtxtrecord)

### Creating TXT Records

- [init([String : String])](/documentation/network/nwtxtrecord/init(_:)-566pd)
- [func removeEntry(key: String) -> Bool](/documentation/network/nwtxtrecord/removeentry(key:))
- [func setEntry(NWTXTRecord.Entry, for: String) -> Bool](/documentation/network/nwtxtrecord/setentry(_:for:))
- [NWTXTRecord.Entry](/documentation/network/nwtxtrecord/entry)

#### Entry Types

- [case none](/documentation/network/nwtxtrecord/entry/none)
- [case empty](/documentation/network/nwtxtrecord/entry/empty)
- [case string(String)](/documentation/network/nwtxtrecord/entry/string(_:))

#### Enumeration Cases

- [case data(Data)](/documentation/network/nwtxtrecord/entry/data(_:))

#### Initializers

- [init(Data?)](/documentation/network/nwtxtrecord/entry/init(_:))

#### Instance Properties

- [var data: Data?](/documentation/network/nwtxtrecord/entry/data)

### Examining TXT Records

- [func getEntry(for: String) -> NWTXTRecord.Entry?](/documentation/network/nwtxtrecord/getentry(for:))
- [subscript(String) -> String?](/documentation/network/nwtxtrecord/subscript(_:))
- [var dictionary: [String : String]](/documentation/network/nwtxtrecord/dictionary)

### Initializers

- [init(Data)](/documentation/network/nwtxtrecord/init(_:)-30jy4)

### Instance Properties

- [var data: Data](/documentation/network/nwtxtrecord/data)
- [NetworkJSONCoder](/documentation/network/networkjsoncoder)

### Instance Methods

- [func makeDecoder() -> JSONDecoder](/documentation/network/networkjsoncoder/makedecoder())
- [func makeEncoder() -> JSONEncoder](/documentation/network/networkjsoncoder/makeencoder())
- [NetworkPropertyListCoder](/documentation/network/networkpropertylistcoder)

### Instance Methods

- [func makeDecoder() -> PropertyListDecoder](/documentation/network/networkpropertylistcoder/makedecoder())
- [func makeEncoder() -> PropertyListEncoder](/documentation/network/networkpropertylistcoder/makeencoder())
- [ProtocolMetadataBuilder](/documentation/network/protocolmetadatabuilder)

### Type Methods

- [static func buildBlock(NWProtocolMetadata...) -> [NWProtocolMetadata]](/documentation/network/protocolmetadatabuilder/buildblock(_:))
- [ProtocolStackBuilder](/documentation/network/protocolstackbuilder)

### Type Methods

- [static func buildBlock(ApplicationProtocol, repeat each P) -> (ApplicationProtocol, repeat each P)](/documentation/network/protocolstackbuilder/buildblock(_:_:))
- [ProxyConfiguration](/documentation/network/proxyconfiguration)

### Creating Proxy Configurations

- [init(relayHops: [ProxyConfiguration.RelayHop])](/documentation/network/proxyconfiguration/init(relayhops:))
- [ProxyConfiguration.RelayHop](/documentation/network/proxyconfiguration/relayhop)

#### Creating Relay Hops

- [init(http3RelayEndpoint: NWEndpoint, http2RelayEndpoint: NWEndpoint?, tlsOptions: NWProtocolTLS.Options, additionalHTTPHeaderFields: [String : String])](/documentation/network/proxyconfiguration/relayhop/init(http3relayendpoint:http2relayendpoint:tlsoptions:additionalhttpheaderfields:))
- [init(http2RelayEndpoint: NWEndpoint, tlsOptions: NWProtocolTLS.Options, additionalHTTPHeaderFields: [String : String])](/documentation/network/proxyconfiguration/relayhop/init(http2relayendpoint:tlsoptions:additionalhttpheaderfields:))
- [init(httpCONNECTProxy: NWEndpoint, tlsOptions: NWProtocolTLS.Options?)](/documentation/network/proxyconfiguration/init(httpconnectproxy:tlsoptions:))
- [init(socksv5Proxy: NWEndpoint)](/documentation/network/proxyconfiguration/init(socksv5proxy:))

### Customizing Proxy Behavior

- [var allowFailover: Bool](/documentation/network/proxyconfiguration/allowfailover)
- [func applyCredential(username: String, password: String)](/documentation/network/proxyconfiguration/applycredential(username:password:))

### Initializers

- [init(obliviousHTTPRelay: ProxyConfiguration.RelayHop, relayResourcePath: String, gatewayKeyConfig: Data, matchDomains: [String])](/documentation/network/proxyconfiguration/init(oblivioushttprelay:relayresourcepath:gatewaykeyconfig:matchdomains:))

### Instance Properties

- [var excludedDomains: [String]](/documentation/network/proxyconfiguration/excludeddomains)
- [var matchDomains: [String]](/documentation/network/proxyconfiguration/matchdomains)
- [QUIC](/documentation/network/quic)

### Classes

- [QUIC.Datagrams](/documentation/network/quic/datagrams)

#### Instance Properties

- [let parent: NetworkConnection<QUIC>](/documentation/network/quic/datagrams/parent)
- [QUIC.Stream](/documentation/network/quic/stream)

#### Instance Properties

- [var directionality: QUICStream.Directionality](/documentation/network/quic/stream/directionality)
- [var initiator: QUICStream.Initiator](/documentation/network/quic/stream/initiator)
- [let parent: NetworkConnection<QUIC>](/documentation/network/quic/stream/parent)
- [var streamApplicationErrorCode: UInt64](/documentation/network/quic/stream/streamapplicationerrorcode)
- [var streamID: UInt64](/documentation/network/quic/stream/streamid)

### Structures

- [QUIC.TLS](/documentation/network/quic/tls-swift.struct)

#### Instance Methods

- [func certificateValidator((sec_protocol_metadata_t, sec_trust_t) async -> Bool) -> QUIC](/documentation/network/quic/tls-swift.struct/certificatevalidator(_:))
- [func cipherSuites([tls_ciphersuite_t]) -> QUIC](/documentation/network/quic/tls-swift.struct/ciphersuites(_:))
- [func ciphersuiteGroups([tls_ciphersuite_group_t]) -> QUIC](/documentation/network/quic/tls-swift.struct/ciphersuitegroups(_:))
- [func localIdentity(sec_identity_t) -> QUIC](/documentation/network/quic/tls-swift.struct/localidentity(_:))
- [func peerAuthentication(TLS.PeerAuthentication) -> QUIC](/documentation/network/quic/tls-swift.struct/peerauthentication(_:))

### Initializers

- [init(alpn: [String])](/documentation/network/quic/init(alpn:))
- [init(alpn: [String], () -> UDP)](/documentation/network/quic/init(alpn:_:))

### Instance Properties

- [var tls: QUIC.TLS](/documentation/network/quic/tls-swift.property)

### Instance Methods

- [func idleTimeout(Int) -> QUIC](/documentation/network/quic/idletimeout(_:))
- [func initialMaxBidirectionalStreams(Int) -> QUIC](/documentation/network/quic/initialmaxbidirectionalstreams(_:))
- [func initialMaxData(Int) -> QUIC](/documentation/network/quic/initialmaxdata(_:))
- [func initialMaxStreamDataBidirectionalLocal(Int) -> QUIC](/documentation/network/quic/initialmaxstreamdatabidirectionallocal(_:))
- [func initialMaxStreamDataBidirectionalRemote(Int) -> QUIC](/documentation/network/quic/initialmaxstreamdatabidirectionalremote(_:))
- [func initialMaxStreamDataUnidirectional(Int) -> QUIC](/documentation/network/quic/initialmaxstreamdataunidirectional(_:))
- [func initialMaxUnidirectionalStreams(Int) -> QUIC](/documentation/network/quic/initialmaxunidirectionalstreams(_:))
- [func maxDatagramFrameSize(Int) -> QUIC](/documentation/network/quic/maxdatagramframesize(_:))
- [func maxUDPPayloadSize(Int) -> QUIC](/documentation/network/quic/maxudppayloadsize(_:))
- [QUICDatagram](/documentation/network/quicdatagram)
- [QUICStream](/documentation/network/quicstream)

### Enumerations

- [QUICStream.Directionality](/documentation/network/quicstream/directionality)

#### Enumeration Cases

- [case bidirectional](/documentation/network/quicstream/directionality/bidirectional)
- [case unidirectional](/documentation/network/quicstream/directionality/unidirectional)
- [QUICStream.Initiator](/documentation/network/quicstream/initiator)

#### Enumeration Cases

- [case client](/documentation/network/quicstream/initiator/client)
- [case server](/documentation/network/quicstream/initiator/server)
- [TCP](/documentation/network/tcp)

### Initializers

- [init()](/documentation/network/tcp/init())
- [init(() -> IP)](/documentation/network/tcp/init(_:))

### Instance Methods

- [func ackStretchingDisabled(Bool) -> TCP](/documentation/network/tcp/ackstretchingdisabled(_:))
- [func connectionTimeout(UInt32) -> TCP](/documentation/network/tcp/connectiontimeout(_:))
- [func ecnDisabled(Bool) -> TCP](/documentation/network/tcp/ecndisabled(_:))
- [func fastOpenAllowed(Bool) -> TCP](/documentation/network/tcp/fastopenallowed(_:))
- [func keepalive(idleTimeInSeconds: UInt32, count: UInt32, intervalInSeconds: UInt32) -> TCP](/documentation/network/tcp/keepalive(idletimeinseconds:count:intervalinseconds:))
- [func maximumSegmentSize(UInt32) -> TCP](/documentation/network/tcp/maximumsegmentsize(_:))
- [func noDelay(Bool) -> TCP](/documentation/network/tcp/nodelay(_:))
- [func noOptions(Bool) -> TCP](/documentation/network/tcp/nooptions(_:))
- [func noPush(Bool) -> TCP](/documentation/network/tcp/nopush(_:))
- [func persistTimeout(UInt32) -> TCP](/documentation/network/tcp/persisttimeout(_:))
- [func retransmitConnectionDropTime(UInt32) -> TCP](/documentation/network/tcp/retransmitconnectiondroptime(_:))
- [func retransmitFinDrop(Bool) -> TCP](/documentation/network/tcp/retransmitfindrop(_:))
- [TLS](/documentation/network/tls)

### Initializers

- [init()](/documentation/network/tls/init())
- [init(() -> TCP)](/documentation/network/tls/init(_:))

### Instance Methods

- [func applicationProtocols([String]) -> TLS](/documentation/network/tls/applicationprotocols(_:))
- [func certificateValidator((sec_protocol_metadata_t, sec_trust_t) async -> Bool) -> TLS](/documentation/network/tls/certificatevalidator(_:))
- [func cipherSuiteGroups([tls_ciphersuite_group_t]) -> TLS](/documentation/network/tls/ciphersuitegroups(_:))
- [func cipherSuites([tls_ciphersuite_t]) -> TLS](/documentation/network/tls/ciphersuites(_:))
- [func earlyDataEnabled(Bool) -> TLS](/documentation/network/tls/earlydataenabled(_:))
- [func localIdentity(sec_identity_t) -> TLS](/documentation/network/tls/localidentity(_:))
- [func peerAuthentication(TLS.PeerAuthentication) -> TLS](/documentation/network/tls/peerauthentication(_:))
- [func ticketsEnabled(Bool) -> TLS](/documentation/network/tls/ticketsenabled(_:))
- [func version(min: tls_protocol_version_t?, max: tls_protocol_version_t?) -> TLS](/documentation/network/tls/version(min:max:))

### Enumerations

- [TLS.PeerAuthentication](/documentation/network/tls/peerauthentication)

#### Enumeration Cases

- [case none](/documentation/network/tls/peerauthentication/none)
- [case optional](/documentation/network/tls/peerauthentication/optional)
- [case required](/documentation/network/tls/peerauthentication/required)
- [TLV](/documentation/network/tlv)

### Initializers

- [init<BelowProtocol>(() -> BelowProtocol)](/documentation/network/tlv/init(_:)-8ka4w)
- [init<BelowProtocol>(() -> BelowProtocol)](/documentation/network/tlv/init(_:)-8qsbh)
- [init<T, L, BelowProtocol>(type: T.Type, length: L.Type, () -> BelowProtocol)](/documentation/network/tlv/init(type:length:_:)-7awe)
- [init<T, L, BelowProtocol>(type: T.Type, length: L.Type, () -> BelowProtocol)](/documentation/network/tlv/init(type:length:_:)-h8s)
- [TXTRecordDecoder](/documentation/network/txtrecorddecoder)

### Initializers

- [init()](/documentation/network/txtrecorddecoder/init())

### Instance Methods

- [func decode<T>(T.Type, from: NWTXTRecord) throws -> T](/documentation/network/txtrecorddecoder/decode(_:from:))
- [UDP](/documentation/network/udp)

### Initializers

- [init()](/documentation/network/udp/init())
- [init(() -> IP)](/documentation/network/udp/init(_:))

### Instance Methods

- [func noChecksumPreferred(Bool) -> UDP](/documentation/network/udp/nochecksumpreferred(_:))
- [UnexpectedEndpointType](/documentation/network/unexpectedendpointtype)

### Initializers

- [init(endpoint: NWEndpoint)](/documentation/network/unexpectedendpointtype/init(endpoint:))

### Instance Properties

- [let endpoint: NWEndpoint](/documentation/network/unexpectedendpointtype/endpoint)
- [WebSocket](/documentation/network/websocket)

### Initializers

- [init<BelowProtocol>(() -> BelowProtocol)](/documentation/network/websocket/init(_:)-5q53h)
- [init<BelowProtocol>(() -> BelowProtocol)](/documentation/network/websocket/init(_:)-7xsae)

### Instance Methods

- [func additionalHeaders([(name: String, value: String)]) -> WebSocket](/documentation/network/websocket/additionalheaders(_:))
- [func autoReplyPing(Bool) -> WebSocket](/documentation/network/websocket/autoreplyping(_:))
- [func maximumMessageSize(Int) -> WebSocket](/documentation/network/websocket/maximummessagesize(_:))
- [func skipHandshake(Bool) -> WebSocket](/documentation/network/websocket/skiphandshake(_:))
- [func subprotocols([String]) -> WebSocket](/documentation/network/websocket/subprotocols(_:))
- [nw_link_quality_t](/documentation/network/nw_link_quality_t)

### Initializers

- [init(UInt32)](/documentation/network/nw_link_quality_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_link_quality_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_link_quality_t/rawvalue)

## Classes

- [NWMultiplexGroup](/documentation/network/nwmultiplexgroup)

### Initializers

- [init(to: NWEndpoint)](/documentation/network/nwmultiplexgroup/init(to:))

### Instance Properties

- [var members: [NWEndpoint]](/documentation/network/nwmultiplexgroup/members)
- [NetworkBrowser](/documentation/network/networkbrowser)

### Initializers

- [init(for: Provider, using: NWParameters?)](/documentation/network/networkbrowser/init(for:using:))

### Instance Methods

- [func onStateUpdate((NetworkBrowser<Provider>, NetworkBrowser<Provider>.State) -> Void) -> Self](/documentation/network/networkbrowser/onstateupdate(_:))
- [func run(([Provider.Endpoint]) async throws -> Void) async throws](/documentation/network/networkbrowser/run(_:)-31x4b)
- [func run<Return>(([Provider.Endpoint]) async throws -> NetworkBrowser<Provider>.RunResult<Return>) async throws -> Return](/documentation/network/networkbrowser/run(_:)-wqyo)

### Type Aliases

- [NetworkBrowser.StateUpdateHandler](/documentation/network/networkbrowser/stateupdatehandler)

### Enumerations

- [NetworkBrowser.RunResult](/documentation/network/networkbrowser/runresult)

#### Enumeration Cases

- [case `continue`](/documentation/network/networkbrowser/runresult/continue)
- [case finish(T)](/documentation/network/networkbrowser/runresult/finish(_:))
- [NetworkBrowser.State](/documentation/network/networkbrowser/state)

#### Enumeration Cases

- [case cancelled](/documentation/network/networkbrowser/state/cancelled)
- [case failed(NWError)](/documentation/network/networkbrowser/state/failed(_:))
- [case ready](/documentation/network/networkbrowser/state/ready)
- [case setup](/documentation/network/networkbrowser/state/setup)
- [case waiting(NWError)](/documentation/network/networkbrowser/state/waiting(_:))
- [NetworkChannel](/documentation/network/networkchannel)

### Operators

- [static func == (NetworkChannel<ApplicationProtocol>, NetworkChannel<ApplicationProtocol>) -> Bool](/documentation/network/networkchannel/==(_:_:))

### Instance Properties

- [var debugDescription: String](/documentation/network/networkchannel/debugdescription)
- [var id: String](/documentation/network/networkchannel/id)
- [var maximumDatagramSize: Int](/documentation/network/networkchannel/maximumdatagramsize)
- [var messages: AsyncThrowingStream<ApplicationProtocol.Message<ApplicationProtocol.ContentType>, any Error>](/documentation/network/networkchannel/messages)
- [var parameters: NWParameters](/documentation/network/networkchannel/parameters)
- [var state: NetworkChannel<ApplicationProtocol>.State](/documentation/network/networkchannel/state-swift.property)

### Instance Methods

- [func close(code: NWProtocolWebSocket.CloseCode, reason: String?, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/close(code:reason:metadata:))
- [func dataTransferReport() async throws -> NWConnection.DataTransferReport](/documentation/network/networkchannel/datatransferreport())
- [func establishmentReport() async throws -> NWConnection.EstablishmentReport](/documentation/network/networkchannel/establishmentreport())
- [func metadata(definition: NWProtocolDefinition) -> NWProtocolMetadata?](/documentation/network/networkchannel/metadata(definition:))
- [func ping<Content>(Content?, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/ping(_:metadata:))
- [func pong<Content>(Content?, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/pong(_:metadata:))
- [func receive() async throws -> ApplicationProtocol.Message<Data>](/documentation/network/networkchannel/receive()-3a115)
- [func receive() async throws -> ApplicationProtocol.Message<Data>](/documentation/network/networkchannel/receive()-3atum)
- [func receive<Sending, Receiving, CoderType>() async throws -> ApplicationProtocol.Message<Receiving>](/documentation/network/networkchannel/receive()-5p11z)
- [func receive() async throws -> ApplicationProtocol.Message<Data>](/documentation/network/networkchannel/receive()-86md7)
- [func receive<T>() async throws -> ApplicationProtocol.Message<Data>](/documentation/network/networkchannel/receive()-8jbul)
- [func receive<Value>(as: Value.Type) async throws -> ApplicationProtocol.Message<Value>](/documentation/network/networkchannel/receive(as:))
- [func receive(atLeast: Int, atMost: Int) async throws -> ApplicationProtocol.Message<Data>](/documentation/network/networkchannel/receive(atleast:atmost:))
- [func receive(exactly: Int) async throws -> ApplicationProtocol.Message<Data>](/documentation/network/networkchannel/receive(exactly:))
- [func send<Value>(Value, endOfStream: Bool, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:endofstream:metadata:)-4f2l0)
- [func send<Content>(Content, endOfStream: Bool, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:endofstream:metadata:)-79bb6)
- [func send<T>(Data, lastMessage: Bool, metadata: NWProtocolFramer.Message?, other: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:lastmessage:metadata:other:))
- [func send<Content>(Content, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:metadata:)-3r1av)
- [func send<Content>(Content, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:metadata:)-42nkz)
- [func send<Sending, Receiving, CoderType>(Sending, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:metadata:)-4rxt1)
- [func send(String, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:metadata:)-5ec48)
- [func send<Content>(Content, type: Int, lastMessage: Bool, metadata: () -> [NWProtocolMetadata]) async throws](/documentation/network/networkchannel/send(_:type:lastmessage:metadata:))
- [func sendIdempotent<Content>(Content, endOfStream: Bool, metadata: () -> [NWProtocolMetadata])](/documentation/network/networkchannel/sendidempotent(_:endofstream:metadata:)-4bo5u)
- [func sendIdempotent<Value>(Value, endOfStream: Bool, metadata: () -> [NWProtocolMetadata])](/documentation/network/networkchannel/sendidempotent(_:endofstream:metadata:)-6cko0)
- [func sendIdempotent(String, metadata: () -> [NWProtocolMetadata])](/documentation/network/networkchannel/sendidempotent(_:metadata:)-37eiq)
- [func sendIdempotent<Content>(Content, metadata: () -> [NWProtocolMetadata])](/documentation/network/networkchannel/sendidempotent(_:metadata:)-6tubc)
- [func sendIdempotent<Content>(Content, type: Int, lastMessage: Bool, metadata: () -> [NWProtocolMetadata])](/documentation/network/networkchannel/sendidempotent(_:type:lastmessage:metadata:))
- [func startReceive(((Int, Int) async throws -> ApplicationProtocol.Message<Data>) async throws -> Void) async throws](/documentation/network/networkchannel/startreceive(_:))
- [func startSend(String, metadata: () -> [NWProtocolMetadata], handler: ((String, Bool) async throws -> Void) async throws -> Void) async throws](/documentation/network/networkchannel/startsend(_:metadata:handler:)-15tt3)
- [func startSend<Content>(Content, metadata: () -> [NWProtocolMetadata], handler: ((Content, Bool) async throws -> Void) async throws -> Void) async throws](/documentation/network/networkchannel/startsend(_:metadata:handler:)-5xhjv)

### Enumerations

- [NetworkChannel.State](/documentation/network/networkchannel/state-swift.enum)

#### Enumeration Cases

- [case cancelled](/documentation/network/networkchannel/state-swift.enum/cancelled)
- [case failed(NWError)](/documentation/network/networkchannel/state-swift.enum/failed(_:))
- [case preparing](/documentation/network/networkchannel/state-swift.enum/preparing)
- [case ready](/documentation/network/networkchannel/state-swift.enum/ready)
- [case setup](/documentation/network/networkchannel/state-swift.enum/setup)
- [case waiting(NWError)](/documentation/network/networkchannel/state-swift.enum/waiting(_:))
- [NetworkConnection](/documentation/network/networkconnection)

### Initializers

- [convenience init(to: NWEndpoint, using: () -> ApplicationProtocol)](/documentation/network/networkconnection/init(to:using:)-182om)
- [convenience init(to: any Connectable, using: () -> ApplicationProtocol)](/documentation/network/networkconnection/init(to:using:)-51aq2)
- [convenience init(to: NWEndpoint, using: NWParametersBuilder<ApplicationProtocol>)](/documentation/network/networkconnection/init(to:using:)-5e864)
- [convenience init(to: NWEndpoint, using: NWParametersBuilder<ApplicationProtocol>)](/documentation/network/networkconnection/init(to:using:)-69glf)
- [convenience init(to: any Connectable, using: NWParametersBuilder<ApplicationProtocol>)](/documentation/network/networkconnection/init(to:using:)-6yzx9)
- [convenience init(to: any Connectable, using: () -> ApplicationProtocol)](/documentation/network/networkconnection/init(to:using:)-7gprx)
- [convenience init(to: NWEndpoint, using: () -> ApplicationProtocol)](/documentation/network/networkconnection/init(to:using:)-907m0)
- [convenience init(to: any Connectable, using: NWParametersBuilder<ApplicationProtocol>)](/documentation/network/networkconnection/init(to:using:)-9kq3t)

### Instance Properties

- [var applicationError: NWProtocolQUIC.ApplicationError](/documentation/network/networkconnection/applicationerror)
- [var currentPath: NWPath?](/documentation/network/networkconnection/currentpath)
- [var datagrams: QUIC.Datagrams<QUICDatagram>](/documentation/network/networkconnection/datagrams)
- [var keepalive: NWProtocolQUIC.Metadata.KeepAliveBehavior](/documentation/network/networkconnection/keepalive)
- [var localEndpoint: NWEndpoint?](/documentation/network/networkconnection/localendpoint)
- [var negotiatedALPN: String?](/documentation/network/networkconnection/negotiatedalpn)
- [var remoteEndpoint: NWEndpoint?](/documentation/network/networkconnection/remoteendpoint)
- [var remoteIdleTimeout: Int](/documentation/network/networkconnection/remoteidletimeout)
- [var remoteMaxStreamsBidirectional: Int](/documentation/network/networkconnection/remotemaxstreamsbidirectional)
- [var remoteMaxStreamsUnidirectional: Int](/documentation/network/networkconnection/remotemaxstreamsunidirectional)
- [var securityProtocolMetadata: sec_protocol_metadata_t](/documentation/network/networkconnection/securityprotocolmetadata)
- [var usableDatagramFrameSize: Int](/documentation/network/networkconnection/usabledatagramframesize)

### Instance Methods

- [func inboundStreams((QUIC.Stream<QUICStream>) async throws -> Void) async throws](/documentation/network/networkconnection/inboundstreams(_:))
- [func inboundStreams<NewApplicationProtocol>(prepending: (QUICStream) -> NewApplicationProtocol, (QUIC.Stream<NewApplicationProtocol>) async throws -> Void) async throws](/documentation/network/networkconnection/inboundstreams(prepending:_:))
- [func onBetterPathUpdate((NetworkConnection<ApplicationProtocol>, Bool) -> Void) -> Self](/documentation/network/networkconnection/onbetterpathupdate(_:))
- [func onPathUpdate((NetworkConnection<ApplicationProtocol>, NWPath) -> Void) -> Self](/documentation/network/networkconnection/onpathupdate(_:))
- [func onStateUpdate((NetworkConnection<ApplicationProtocol>, NetworkChannel<ApplicationProtocol>.State) -> Void) -> Self](/documentation/network/networkconnection/onstateupdate(_:))
- [func onViabilityUpdate((NetworkConnection<ApplicationProtocol>, Bool) -> Void) -> Self](/documentation/network/networkconnection/onviabilityupdate(_:))
- [func openStream(directionality: QUICStream.Directionality) async throws -> QUIC.Stream<QUICStream>](/documentation/network/networkconnection/openstream(directionality:))
- [func openStream<NewApplicationProtocol>(directionality: QUICStream.Directionality, (QUICStream) -> NewApplicationProtocol) async throws -> QUIC.Stream<NewApplicationProtocol>](/documentation/network/networkconnection/openstream(directionality:_:))
- [func start() -> Self](/documentation/network/networkconnection/start())
- [func tryNextEndpoint()](/documentation/network/networkconnection/trynextendpoint())
- [NetworkListener](/documentation/network/networklistener)

### Initializers

- [convenience init(for: (any ListenerProvider)?, using: () -> ApplicationProtocol) throws](/documentation/network/networklistener/init(for:using:)-2hkg)
- [convenience init(for: (any ListenerProvider)?, using: NWParametersBuilder<ApplicationProtocol>) throws](/documentation/network/networklistener/init(for:using:)-2vh87)

### Instance Properties

- [var newConnectionLimit: Int](/documentation/network/networklistener/newconnectionlimit)
- [var port: NWEndpoint.Port?](/documentation/network/networklistener/port)
- [var service: NWListener.Service?](/documentation/network/networklistener/service)

### Instance Methods

- [func newConnectionLimit(Int) -> Self](/documentation/network/networklistener/newconnectionlimit(_:))
- [func onServiceRegistrationUpdate((NetworkListener<ApplicationProtocol>, NetworkListener<ApplicationProtocol>.ServiceRegistrationChange) -> Void) -> Self](/documentation/network/networklistener/onserviceregistrationupdate(_:))
- [func onStateUpdate((NetworkListener<ApplicationProtocol>, NetworkListener<ApplicationProtocol>.State) -> Void) -> Self](/documentation/network/networklistener/onstateupdate(_:))
- [func run((NetworkConnection<ApplicationProtocol>) async throws -> Void) async throws](/documentation/network/networklistener/run(_:)-42k25)
- [func run((NetworkConnection<ApplicationProtocol>) async throws -> Void) async throws](/documentation/network/networklistener/run(_:)-4iov3)

### Type Aliases

- [NetworkListener.ServiceRegistrationUpdateHandler](/documentation/network/networklistener/serviceregistrationupdatehandler)
- [NetworkListener.StateUpdateHandler](/documentation/network/networklistener/stateupdatehandler)

### Enumerations

- [NetworkListener.ServiceRegistrationChange](/documentation/network/networklistener/serviceregistrationchange)

#### Enumeration Cases

- [case add(NWEndpoint)](/documentation/network/networklistener/serviceregistrationchange/add(_:))
- [case remove(NWEndpoint)](/documentation/network/networklistener/serviceregistrationchange/remove(_:))
- [NetworkListener.State](/documentation/network/networklistener/state)

#### Enumeration Cases

- [case cancelled](/documentation/network/networklistener/state/cancelled)
- [case failed(NWError)](/documentation/network/networklistener/state/failed(_:))
- [case ready](/documentation/network/networklistener/state/ready)
- [case setup](/documentation/network/networklistener/state/setup)
- [case waiting(NWError)](/documentation/network/networklistener/state/waiting(_:))

## Reference

- [Network Constants](/documentation/network/network-constants)

### Constants

- [var NW_FRAMER_CREATE_FLAGS_DEFAULT: Int32](/documentation/network/nw_framer_create_flags_default)
- [var NW_FRAMER_WAKEUP_TIME_FOREVER: UInt64](/documentation/network/nw_framer_wakeup_time_forever)
- [var NW_LISTENER_INFINITE_CONNECTION_LIMIT: UInt32](/documentation/network/nw_listener_infinite_connection_limit)
- [var NW_QUIC_CONNECTION_DEFAULT_KEEPALIVE: Int32](/documentation/network/nw_quic_connection_default_keepalive)
- [var nw_browser_state_waiting: nw_browser_state_t](/documentation/network/nw_browser_state_waiting)
- [var nw_interface_radio_type_cell_cdma: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_cdma)
- [var nw_interface_radio_type_cell_endc_mmw: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_endc_mmw)
- [var nw_interface_radio_type_cell_endc_sub6: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_endc_sub6)
- [var nw_interface_radio_type_cell_evdo: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_evdo)
- [var nw_interface_radio_type_cell_gsm: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_gsm)
- [var nw_interface_radio_type_cell_lte: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_lte)
- [var nw_interface_radio_type_cell_nr_sa_mmw: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_nr_sa_mmw)
- [var nw_interface_radio_type_cell_nr_sa_sub6: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_nr_sa_sub6)
- [var nw_interface_radio_type_cell_wcdma: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_cell_wcdma)
- [var nw_interface_radio_type_unknown: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_unknown)
- [var nw_interface_radio_type_wifi_a: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_wifi_a)
- [var nw_interface_radio_type_wifi_ac: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_wifi_ac)
- [var nw_interface_radio_type_wifi_ax: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_wifi_ax)
- [var nw_interface_radio_type_wifi_b: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_wifi_b)
- [var nw_interface_radio_type_wifi_g: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_wifi_g)
- [var nw_interface_radio_type_wifi_n: nw_interface_radio_type_t](/documentation/network/nw_interface_radio_type_wifi_n)
- [var nw_multipath_version_0: nw_multipath_version_t](/documentation/network/nw_multipath_version_0)
- [var nw_multipath_version_1: nw_multipath_version_t](/documentation/network/nw_multipath_version_1)
- [var nw_multipath_version_unspecified: nw_multipath_version_t](/documentation/network/nw_multipath_version_unspecified)
- [var nw_parameters_expired_dns_behavior_persistent: nw_parameters_expired_dns_behavior_t](/documentation/network/nw_parameters_expired_dns_behavior_persistent)
- [var nw_path_unsatisfied_reason_cellular_denied: nw_path_unsatisfied_reason_t](/documentation/network/nw_path_unsatisfied_reason_cellular_denied)
- [var nw_path_unsatisfied_reason_local_network_denied: nw_path_unsatisfied_reason_t](/documentation/network/nw_path_unsatisfied_reason_local_network_denied)
- [var nw_path_unsatisfied_reason_not_available: nw_path_unsatisfied_reason_t](/documentation/network/nw_path_unsatisfied_reason_not_available)
- [var nw_path_unsatisfied_reason_vpn_inactive: nw_path_unsatisfied_reason_t](/documentation/network/nw_path_unsatisfied_reason_vpn_inactive)
- [var nw_path_unsatisfied_reason_wifi_denied: nw_path_unsatisfied_reason_t](/documentation/network/nw_path_unsatisfied_reason_wifi_denied)
- [var nw_quic_stream_type_bidirectional: nw_quic_stream_type_t](/documentation/network/nw_quic_stream_type_bidirectional)
- [var nw_quic_stream_type_datagram: nw_quic_stream_type_t](/documentation/network/nw_quic_stream_type_datagram)
- [var nw_quic_stream_type_unidirectional: nw_quic_stream_type_t](/documentation/network/nw_quic_stream_type_unidirectional)
- [var nw_quic_stream_type_unknown: nw_quic_stream_type_t](/documentation/network/nw_quic_stream_type_unknown)
- [Network Functions](/documentation/network/network-functions)

### Functions

- [func nw_advertise_descriptor_copy_txt_record_object(nw_advertise_descriptor_t) -> nw_txt_record_t?](/documentation/network/nw_advertise_descriptor_copy_txt_record_object(_:))
- [func nw_advertise_descriptor_create_application_service(UnsafePointer<CChar>) -> nw_advertise_descriptor_t](/documentation/network/nw_advertise_descriptor_create_application_service(_:))
- [func nw_advertise_descriptor_create_bonjour_service(UnsafePointer<CChar>?, UnsafePointer<CChar>, UnsafePointer<CChar>?) -> nw_advertise_descriptor_t?](/documentation/network/nw_advertise_descriptor_create_bonjour_service(_:_:_:))
- [func nw_advertise_descriptor_get_application_service_name(nw_advertise_descriptor_t) -> UnsafePointer<CChar>?](/documentation/network/nw_advertise_descriptor_get_application_service_name(_:))
- [func nw_advertise_descriptor_get_no_auto_rename(nw_advertise_descriptor_t) -> Bool](/documentation/network/nw_advertise_descriptor_get_no_auto_rename(_:))
- [func nw_advertise_descriptor_set_no_auto_rename(nw_advertise_descriptor_t, Bool)](/documentation/network/nw_advertise_descriptor_set_no_auto_rename(_:_:))
- [func nw_advertise_descriptor_set_txt_record(nw_advertise_descriptor_t, UnsafeRawPointer?, Int)](/documentation/network/nw_advertise_descriptor_set_txt_record(_:_:_:))
- [func nw_advertise_descriptor_set_txt_record_object(nw_advertise_descriptor_t, nw_txt_record_t?)](/documentation/network/nw_advertise_descriptor_set_txt_record_object(_:_:))
- [func nw_browse_descriptor_create_application_service(UnsafePointer<CChar>) -> nw_browse_descriptor_t](/documentation/network/nw_browse_descriptor_create_application_service(_:))
- [func nw_browse_descriptor_create_bonjour_service(UnsafePointer<CChar>, UnsafePointer<CChar>?) -> nw_browse_descriptor_t](/documentation/network/nw_browse_descriptor_create_bonjour_service(_:_:))
- [func nw_browse_descriptor_get_application_service_name(nw_browse_descriptor_t) -> UnsafePointer<CChar>?](/documentation/network/nw_browse_descriptor_get_application_service_name(_:))
- [func nw_browse_descriptor_get_bonjour_service_domain(nw_browse_descriptor_t) -> UnsafePointer<CChar>?](/documentation/network/nw_browse_descriptor_get_bonjour_service_domain(_:))
- [func nw_browse_descriptor_get_bonjour_service_type(nw_browse_descriptor_t) -> UnsafePointer<CChar>](/documentation/network/nw_browse_descriptor_get_bonjour_service_type(_:))
- [func nw_browse_descriptor_get_include_txt_record(nw_browse_descriptor_t) -> Bool](/documentation/network/nw_browse_descriptor_get_include_txt_record(_:))
- [func nw_browse_descriptor_set_include_txt_record(nw_browse_descriptor_t, Bool)](/documentation/network/nw_browse_descriptor_set_include_txt_record(_:_:))
- [func nw_browse_result_copy_endpoint(nw_browse_result_t) -> nw_endpoint_t](/documentation/network/nw_browse_result_copy_endpoint(_:))
- [func nw_browse_result_copy_txt_record_object(nw_browse_result_t) -> nw_txt_record_t?](/documentation/network/nw_browse_result_copy_txt_record_object(_:))
- [func nw_browse_result_enumerate_interfaces(nw_browse_result_t, (nw_interface_t) -> Bool)](/documentation/network/nw_browse_result_enumerate_interfaces(_:_:))
- [func nw_browse_result_get_changes(nw_browse_result_t?, nw_browse_result_t?) -> nw_browse_result_change_t](/documentation/network/nw_browse_result_get_changes(_:_:))
- [func nw_browse_result_get_interfaces_count(nw_browse_result_t) -> Int](/documentation/network/nw_browse_result_get_interfaces_count(_:))
- [func nw_browser_cancel(nw_browser_t)](/documentation/network/nw_browser_cancel(_:))
- [func nw_browser_copy_browse_descriptor(nw_browser_t) -> nw_browse_descriptor_t](/documentation/network/nw_browser_copy_browse_descriptor(_:))
- [func nw_browser_copy_parameters(nw_browser_t) -> nw_parameters_t](/documentation/network/nw_browser_copy_parameters(_:))
- [func nw_browser_create(nw_browse_descriptor_t, nw_parameters_t?) -> nw_browser_t](/documentation/network/nw_browser_create(_:_:))
- [func nw_browser_set_browse_results_changed_handler(nw_browser_t, nw_browser_browse_results_changed_handler_t?)](/documentation/network/nw_browser_set_browse_results_changed_handler(_:_:))
- [func nw_browser_set_queue(nw_browser_t, dispatch_queue_t)](/documentation/network/nw_browser_set_queue(_:_:))
- [func nw_browser_set_state_changed_handler(nw_browser_t, nw_browser_state_changed_handler_t?)](/documentation/network/nw_browser_set_state_changed_handler(_:_:))
- [func nw_browser_start(nw_browser_t)](/documentation/network/nw_browser_start(_:))
- [func nw_connection_access_establishment_report(nw_connection_t, dispatch_queue_t, nw_establishment_report_access_block_t)](/documentation/network/nw_connection_access_establishment_report(_:_:_:))
- [func nw_connection_batch(nw_connection_t, () -> Void)](/documentation/network/nw_connection_batch(_:_:))
- [func nw_connection_cancel(nw_connection_t)](/documentation/network/nw_connection_cancel(_:))
- [func nw_connection_cancel_current_endpoint(nw_connection_t)](/documentation/network/nw_connection_cancel_current_endpoint(_:))
- [func nw_connection_copy_current_path(nw_connection_t) -> nw_path_t?](/documentation/network/nw_connection_copy_current_path(_:))
- [func nw_connection_copy_description(nw_connection_t) -> UnsafeMutablePointer<CChar>](/documentation/network/nw_connection_copy_description(_:))
- [func nw_connection_copy_endpoint(nw_connection_t) -> nw_endpoint_t](/documentation/network/nw_connection_copy_endpoint(_:))
- [func nw_connection_copy_parameters(nw_connection_t) -> nw_parameters_t](/documentation/network/nw_connection_copy_parameters(_:))
- [func nw_connection_copy_protocol_metadata(nw_connection_t, nw_protocol_definition_t) -> nw_protocol_metadata_t?](/documentation/network/nw_connection_copy_protocol_metadata(_:_:))
- [func nw_connection_create(nw_endpoint_t, nw_parameters_t) -> nw_connection_t](/documentation/network/nw_connection_create(_:_:))
- [func nw_connection_create_new_data_transfer_report(nw_connection_t) -> nw_data_transfer_report_t](/documentation/network/nw_connection_create_new_data_transfer_report(_:))
- [func nw_connection_force_cancel(nw_connection_t)](/documentation/network/nw_connection_force_cancel(_:))
- [func nw_connection_get_maximum_datagram_size(nw_connection_t) -> UInt32](/documentation/network/nw_connection_get_maximum_datagram_size(_:))
- [func nw_connection_group_cancel(nw_connection_group_t)](/documentation/network/nw_connection_group_cancel(_:))
- [func nw_connection_group_copy_descriptor(nw_connection_group_t) -> nw_group_descriptor_t](/documentation/network/nw_connection_group_copy_descriptor(_:))
- [func nw_connection_group_copy_local_endpoint_for_message(nw_connection_group_t, nw_content_context_t) -> nw_endpoint_t?](/documentation/network/nw_connection_group_copy_local_endpoint_for_message(_:_:))
- [func nw_connection_group_copy_parameters(nw_connection_group_t) -> nw_parameters_t](/documentation/network/nw_connection_group_copy_parameters(_:))
- [func nw_connection_group_copy_path_for_message(nw_connection_group_t, nw_content_context_t) -> nw_path_t?](/documentation/network/nw_connection_group_copy_path_for_message(_:_:))
- [func nw_connection_group_copy_protocol_metadata(nw_connection_group_t, nw_protocol_definition_t) -> nw_protocol_metadata_t?](/documentation/network/nw_connection_group_copy_protocol_metadata(_:_:))
- [func nw_connection_group_copy_protocol_metadata_for_message(nw_connection_group_t, nw_content_context_t, nw_protocol_definition_t) -> nw_protocol_metadata_t?](/documentation/network/nw_connection_group_copy_protocol_metadata_for_message(_:_:_:))
- [func nw_connection_group_copy_remote_endpoint_for_message(nw_connection_group_t, nw_content_context_t) -> nw_endpoint_t?](/documentation/network/nw_connection_group_copy_remote_endpoint_for_message(_:_:))
- [func nw_connection_group_create(nw_group_descriptor_t, nw_parameters_t) -> nw_connection_group_t](/documentation/network/nw_connection_group_create(_:_:))
- [func nw_connection_group_extract_connection(nw_connection_group_t, nw_endpoint_t?, nw_protocol_options_t?) -> nw_connection_t?](/documentation/network/nw_connection_group_extract_connection(_:_:_:))
- [func nw_connection_group_extract_connection_for_message(nw_connection_group_t, nw_content_context_t) -> nw_connection_t?](/documentation/network/nw_connection_group_extract_connection_for_message(_:_:))
- [func nw_connection_group_reinsert_extracted_connection(nw_connection_group_t, nw_connection_t) -> Bool](/documentation/network/nw_connection_group_reinsert_extracted_connection(_:_:))
- [func nw_connection_group_reply(nw_connection_group_t, nw_content_context_t, nw_content_context_t, dispatch_data_t?)](/documentation/network/nw_connection_group_reply(_:_:_:_:))
- [func nw_connection_group_send_message(nw_connection_group_t, dispatch_data_t?, nw_endpoint_t?, nw_content_context_t, nw_connection_group_send_completion_t)](/documentation/network/nw_connection_group_send_message(_:_:_:_:_:))
- [func nw_connection_group_set_new_connection_handler(nw_connection_group_t, nw_connection_group_new_connection_handler_t?)](/documentation/network/nw_connection_group_set_new_connection_handler(_:_:))
- [func nw_connection_group_set_queue(nw_connection_group_t, dispatch_queue_t)](/documentation/network/nw_connection_group_set_queue(_:_:))
- [func nw_connection_group_set_receive_handler(nw_connection_group_t, UInt32, Bool, nw_connection_group_receive_handler_t?)](/documentation/network/nw_connection_group_set_receive_handler(_:_:_:_:))
- [func nw_connection_group_set_state_changed_handler(nw_connection_group_t, nw_connection_group_state_changed_handler_t?)](/documentation/network/nw_connection_group_set_state_changed_handler(_:_:))
- [func nw_connection_group_start(nw_connection_group_t)](/documentation/network/nw_connection_group_start(_:))
- [func nw_connection_receive(nw_connection_t, UInt32, UInt32, nw_connection_receive_completion_t)](/documentation/network/nw_connection_receive(_:_:_:_:))
- [func nw_connection_receive_message(nw_connection_t, nw_connection_receive_completion_t)](/documentation/network/nw_connection_receive_message(_:_:))
- [func nw_connection_restart(nw_connection_t)](/documentation/network/nw_connection_restart(_:))
- [func nw_connection_send(nw_connection_t, dispatch_data_t?, nw_content_context_t, Bool, nw_connection_send_completion_t)](/documentation/network/nw_connection_send(_:_:_:_:_:))
- [func nw_connection_set_better_path_available_handler(nw_connection_t, nw_connection_boolean_event_handler_t?)](/documentation/network/nw_connection_set_better_path_available_handler(_:_:))
- [func nw_connection_set_path_changed_handler(nw_connection_t, nw_connection_path_event_handler_t?)](/documentation/network/nw_connection_set_path_changed_handler(_:_:))
- [func nw_connection_set_queue(nw_connection_t, dispatch_queue_t)](/documentation/network/nw_connection_set_queue(_:_:))
- [func nw_connection_set_state_changed_handler(nw_connection_t, nw_connection_state_changed_handler_t?)](/documentation/network/nw_connection_set_state_changed_handler(_:_:))
- [func nw_connection_set_viability_changed_handler(nw_connection_t, nw_connection_boolean_event_handler_t?)](/documentation/network/nw_connection_set_viability_changed_handler(_:_:))
- [func nw_connection_start(nw_connection_t)](/documentation/network/nw_connection_start(_:))
- [func nw_content_context_copy_antecedent(nw_content_context_t) -> nw_content_context_t?](/documentation/network/nw_content_context_copy_antecedent(_:))
- [func nw_content_context_copy_protocol_metadata(nw_content_context_t, nw_protocol_definition_t) -> nw_protocol_metadata_t?](/documentation/network/nw_content_context_copy_protocol_metadata(_:_:))
- [func nw_content_context_create(UnsafePointer<CChar>) -> nw_content_context_t](/documentation/network/nw_content_context_create(_:))
- [func nw_content_context_foreach_protocol_metadata(nw_content_context_t, (nw_protocol_definition_t, nw_protocol_metadata_t) -> Void)](/documentation/network/nw_content_context_foreach_protocol_metadata(_:_:))
- [func nw_content_context_get_expiration_milliseconds(nw_content_context_t) -> UInt64](/documentation/network/nw_content_context_get_expiration_milliseconds(_:))
- [func nw_content_context_get_identifier(nw_content_context_t) -> UnsafePointer<CChar>](/documentation/network/nw_content_context_get_identifier(_:))
- [func nw_content_context_get_is_final(nw_content_context_t) -> Bool](/documentation/network/nw_content_context_get_is_final(_:))
- [func nw_content_context_get_relative_priority(nw_content_context_t) -> Double](/documentation/network/nw_content_context_get_relative_priority(_:))
- [func nw_content_context_set_antecedent(nw_content_context_t, nw_content_context_t?)](/documentation/network/nw_content_context_set_antecedent(_:_:))
- [func nw_content_context_set_expiration_milliseconds(nw_content_context_t, UInt64)](/documentation/network/nw_content_context_set_expiration_milliseconds(_:_:))
- [func nw_content_context_set_is_final(nw_content_context_t, Bool)](/documentation/network/nw_content_context_set_is_final(_:_:))
- [func nw_content_context_set_metadata_for_protocol(nw_content_context_t, nw_protocol_metadata_t)](/documentation/network/nw_content_context_set_metadata_for_protocol(_:_:))
- [func nw_content_context_set_relative_priority(nw_content_context_t, Double)](/documentation/network/nw_content_context_set_relative_priority(_:_:))
- [func nw_data_transfer_report_collect(nw_data_transfer_report_t, dispatch_queue_t, nw_data_transfer_report_collect_block_t)](/documentation/network/nw_data_transfer_report_collect(_:_:_:))
- [func nw_data_transfer_report_copy_path_interface(nw_data_transfer_report_t, UInt32) -> nw_interface_t](/documentation/network/nw_data_transfer_report_copy_path_interface(_:_:))
- [func nw_data_transfer_report_get_duration_milliseconds(nw_data_transfer_report_t) -> UInt64](/documentation/network/nw_data_transfer_report_get_duration_milliseconds(_:))
- [func nw_data_transfer_report_get_path_count(nw_data_transfer_report_t) -> UInt32](/documentation/network/nw_data_transfer_report_get_path_count(_:))
- [func nw_data_transfer_report_get_path_radio_type(nw_data_transfer_report_t, UInt32) -> nw_interface_radio_type_t](/documentation/network/nw_data_transfer_report_get_path_radio_type(_:_:))
- [func nw_data_transfer_report_get_received_application_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_application_byte_count(_:_:))
- [func nw_data_transfer_report_get_received_ip_packet_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_ip_packet_count(_:_:))
- [func nw_data_transfer_report_get_received_transport_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_byte_count(_:_:))
- [func nw_data_transfer_report_get_received_transport_duplicate_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_duplicate_byte_count(_:_:))
- [func nw_data_transfer_report_get_received_transport_out_of_order_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_out_of_order_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_application_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_application_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_ip_packet_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_ip_packet_count(_:_:))
- [func nw_data_transfer_report_get_sent_transport_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_transport_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_transport_retransmitted_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_transport_retransmitted_byte_count(_:_:))
- [func nw_data_transfer_report_get_state(nw_data_transfer_report_t) -> nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_get_state(_:))
- [func nw_data_transfer_report_get_transport_minimum_rtt_milliseconds(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_minimum_rtt_milliseconds(_:_:))
- [func nw_data_transfer_report_get_transport_rtt_variance(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_rtt_variance(_:_:))
- [func nw_data_transfer_report_get_transport_smoothed_rtt_milliseconds(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_smoothed_rtt_milliseconds(_:_:))
- [func nw_endpoint_copy_address_string(nw_endpoint_t) -> UnsafeMutablePointer<CChar>](/documentation/network/nw_endpoint_copy_address_string(_:))
- [func nw_endpoint_copy_port_string(nw_endpoint_t) -> UnsafeMutablePointer<CChar>](/documentation/network/nw_endpoint_copy_port_string(_:))
- [func nw_endpoint_copy_txt_record(nw_endpoint_t) -> nw_txt_record_t?](/documentation/network/nw_endpoint_copy_txt_record(_:))
- [func nw_endpoint_create_address(UnsafePointer<sockaddr>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_address(_:))
- [func nw_endpoint_create_bonjour_service(UnsafePointer<CChar>, UnsafePointer<CChar>, UnsafePointer<CChar>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_bonjour_service(_:_:_:))
- [func nw_endpoint_create_host(UnsafePointer<CChar>, UnsafePointer<CChar>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_host(_:_:))
- [func nw_endpoint_create_url(UnsafePointer<CChar>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_url(_:))
- [func nw_endpoint_get_address(nw_endpoint_t) -> UnsafePointer<sockaddr>](/documentation/network/nw_endpoint_get_address(_:))
- [func nw_endpoint_get_bonjour_service_domain(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_bonjour_service_domain(_:))
- [func nw_endpoint_get_bonjour_service_name(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_bonjour_service_name(_:))
- [func nw_endpoint_get_bonjour_service_type(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_bonjour_service_type(_:))
- [func nw_endpoint_get_hostname(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_hostname(_:))
- [func nw_endpoint_get_port(nw_endpoint_t) -> UInt16](/documentation/network/nw_endpoint_get_port(_:))
- [func nw_endpoint_get_signature(nw_endpoint_t, UnsafeMutablePointer<Int>) -> UnsafePointer<UInt8>?](/documentation/network/nw_endpoint_get_signature(_:_:))
- [func nw_endpoint_get_type(nw_endpoint_t) -> nw_endpoint_type_t](/documentation/network/nw_endpoint_get_type(_:))
- [func nw_endpoint_get_url(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_url(_:))
- [func nw_error_copy_cf_error(nw_error_t) -> Unmanaged<CFError>](/documentation/network/nw_error_copy_cf_error(_:))
- [func nw_error_get_error_code(nw_error_t) -> Int32](/documentation/network/nw_error_get_error_code(_:))
- [func nw_error_get_error_domain(nw_error_t) -> nw_error_domain_t](/documentation/network/nw_error_get_error_domain(_:))
- [func nw_establishment_report_copy_proxy_endpoint(nw_establishment_report_t) -> nw_endpoint_t?](/documentation/network/nw_establishment_report_copy_proxy_endpoint(_:))
- [func nw_establishment_report_enumerate_protocols(nw_establishment_report_t, (nw_protocol_definition_t, UInt64, UInt64) -> Bool)](/documentation/network/nw_establishment_report_enumerate_protocols(_:_:))
- [func nw_establishment_report_enumerate_resolution_reports(nw_establishment_report_t, (nw_resolution_report_t) -> Bool)](/documentation/network/nw_establishment_report_enumerate_resolution_reports(_:_:))
- [func nw_establishment_report_enumerate_resolutions(nw_establishment_report_t, (nw_report_resolution_source_t, UInt64, UInt32, nw_endpoint_t, nw_endpoint_t) -> Bool)](/documentation/network/nw_establishment_report_enumerate_resolutions(_:_:))
- [func nw_establishment_report_get_attempt_started_after_milliseconds(nw_establishment_report_t) -> UInt64](/documentation/network/nw_establishment_report_get_attempt_started_after_milliseconds(_:))
- [func nw_establishment_report_get_duration_milliseconds(nw_establishment_report_t) -> UInt64](/documentation/network/nw_establishment_report_get_duration_milliseconds(_:))
- [func nw_establishment_report_get_previous_attempt_count(nw_establishment_report_t) -> UInt32](/documentation/network/nw_establishment_report_get_previous_attempt_count(_:))
- [func nw_establishment_report_get_proxy_configured(nw_establishment_report_t) -> Bool](/documentation/network/nw_establishment_report_get_proxy_configured(_:))
- [func nw_establishment_report_get_used_proxy(nw_establishment_report_t) -> Bool](/documentation/network/nw_establishment_report_get_used_proxy(_:))
- [func nw_ethernet_channel_cancel(nw_ethernet_channel_t)](/documentation/network/nw_ethernet_channel_cancel(_:))
- [func nw_ethernet_channel_create(UInt16, nw_interface_t) -> nw_ethernet_channel_t](/documentation/network/nw_ethernet_channel_create(_:_:))
- [func nw_ethernet_channel_create_with_parameters(UInt16, nw_interface_t, nw_parameters_t) -> nw_ethernet_channel_t](/documentation/network/nw_ethernet_channel_create_with_parameters(_:_:_:))
- [func nw_ethernet_channel_get_maximum_payload_size(nw_ethernet_channel_t) -> UInt32](/documentation/network/nw_ethernet_channel_get_maximum_payload_size(_:))
- [func nw_ethernet_channel_send(nw_ethernet_channel_t, dispatch_data_t, UInt16, UnsafeMutablePointer<UInt8>, nw_ethernet_channel_send_completion_t)](/documentation/network/nw_ethernet_channel_send(_:_:_:_:_:))
- [func nw_ethernet_channel_set_queue(nw_ethernet_channel_t, dispatch_queue_t)](/documentation/network/nw_ethernet_channel_set_queue(_:_:))
- [func nw_ethernet_channel_set_receive_handler(nw_ethernet_channel_t, nw_ethernet_channel_receive_handler_t?)](/documentation/network/nw_ethernet_channel_set_receive_handler(_:_:))
- [func nw_ethernet_channel_set_state_changed_handler(nw_ethernet_channel_t, nw_ethernet_channel_state_changed_handler_t?)](/documentation/network/nw_ethernet_channel_set_state_changed_handler(_:_:))
- [func nw_ethernet_channel_start(nw_ethernet_channel_t)](/documentation/network/nw_ethernet_channel_start(_:))
- [func nw_framer_async(nw_framer_t, nw_framer_block_t)](/documentation/network/nw_framer_async(_:_:))
- [func nw_framer_copy_local_endpoint(nw_framer_t) -> nw_endpoint_t](/documentation/network/nw_framer_copy_local_endpoint(_:))
- [func nw_framer_copy_options(nw_framer_t) -> nw_protocol_options_t](/documentation/network/nw_framer_copy_options(_:))
- [func nw_framer_copy_parameters(nw_framer_t) -> nw_parameters_t](/documentation/network/nw_framer_copy_parameters(_:))
- [func nw_framer_copy_remote_endpoint(nw_framer_t) -> nw_endpoint_t](/documentation/network/nw_framer_copy_remote_endpoint(_:))
- [func nw_framer_create_definition(UnsafePointer<CChar>, UInt32, nw_framer_start_handler_t) -> nw_protocol_definition_t](/documentation/network/nw_framer_create_definition(_:_:_:))
- [func nw_framer_create_options(nw_protocol_definition_t) -> nw_protocol_options_t](/documentation/network/nw_framer_create_options(_:))
- [func nw_framer_deliver_input(nw_framer_t, UnsafePointer<UInt8>, Int, nw_framer_message_t, Bool)](/documentation/network/nw_framer_deliver_input(_:_:_:_:_:))
- [func nw_framer_deliver_input_no_copy(nw_framer_t, Int, nw_framer_message_t, Bool) -> Bool](/documentation/network/nw_framer_deliver_input_no_copy(_:_:_:_:))
- [func nw_framer_mark_failed_with_error(nw_framer_t, Int32)](/documentation/network/nw_framer_mark_failed_with_error(_:_:))
- [func nw_framer_mark_ready(nw_framer_t)](/documentation/network/nw_framer_mark_ready(_:))
- [func nw_framer_message_access_value(nw_framer_message_t, UnsafePointer<CChar>, (UnsafeRawPointer?) -> Bool) -> Bool](/documentation/network/nw_framer_message_access_value(_:_:_:))
- [func nw_framer_message_copy_object_value(nw_framer_message_t, UnsafePointer<CChar>) -> Any?](/documentation/network/nw_framer_message_copy_object_value(_:_:))
- [func nw_framer_message_create(nw_framer_t) -> nw_framer_message_t](/documentation/network/nw_framer_message_create(_:))
- [func nw_framer_message_set_object_value(nw_framer_message_t, UnsafePointer<CChar>, Any?)](/documentation/network/nw_framer_message_set_object_value(_:_:_:))
- [func nw_framer_message_set_value(nw_framer_message_t, UnsafePointer<CChar>, UnsafeMutableRawPointer?, nw_framer_message_dispose_value_t?)](/documentation/network/nw_framer_message_set_value(_:_:_:_:))
- [func nw_framer_options_copy_object_value(nw_protocol_options_t, UnsafePointer<CChar>) -> Any?](/documentation/network/nw_framer_options_copy_object_value(_:_:))
- [func nw_framer_options_set_object_value(nw_protocol_options_t, UnsafePointer<CChar>, Any?)](/documentation/network/nw_framer_options_set_object_value(_:_:_:))
- [func nw_framer_parse_input(nw_framer_t, Int, Int, UnsafeMutablePointer<UInt8>?, (UnsafeMutablePointer<UInt8>?, Int, Bool) -> Int) -> Bool](/documentation/network/nw_framer_parse_input(_:_:_:_:_:))
- [func nw_framer_parse_output(nw_framer_t, Int, Int, UnsafeMutablePointer<UInt8>?, (UnsafeMutablePointer<UInt8>?, Int, Bool) -> Int) -> Bool](/documentation/network/nw_framer_parse_output(_:_:_:_:_:))
- [func nw_framer_pass_through_input(nw_framer_t)](/documentation/network/nw_framer_pass_through_input(_:))
- [func nw_framer_pass_through_output(nw_framer_t)](/documentation/network/nw_framer_pass_through_output(_:))
- [func nw_framer_prepend_application_protocol(nw_framer_t, nw_protocol_options_t) -> Bool](/documentation/network/nw_framer_prepend_application_protocol(_:_:))
- [func nw_framer_protocol_create_message(nw_protocol_definition_t) -> nw_framer_message_t](/documentation/network/nw_framer_protocol_create_message(_:))
- [func nw_framer_schedule_wakeup(nw_framer_t, UInt64)](/documentation/network/nw_framer_schedule_wakeup(_:_:))
- [func nw_framer_set_cleanup_handler(nw_framer_t, nw_framer_cleanup_handler_t)](/documentation/network/nw_framer_set_cleanup_handler(_:_:))
- [func nw_framer_set_input_handler(nw_framer_t, nw_framer_input_handler_t)](/documentation/network/nw_framer_set_input_handler(_:_:))
- [func nw_framer_set_output_handler(nw_framer_t, nw_framer_output_handler_t)](/documentation/network/nw_framer_set_output_handler(_:_:))
- [func nw_framer_set_stop_handler(nw_framer_t, nw_framer_stop_handler_t)](/documentation/network/nw_framer_set_stop_handler(_:_:))
- [func nw_framer_set_wakeup_handler(nw_framer_t, nw_framer_wakeup_handler_t)](/documentation/network/nw_framer_set_wakeup_handler(_:_:))
- [func nw_framer_write_output(nw_framer_t, UnsafePointer<UInt8>, Int)](/documentation/network/nw_framer_write_output(_:_:_:))
- [func nw_framer_write_output_data(nw_framer_t, dispatch_data_t)](/documentation/network/nw_framer_write_output_data(_:_:))
- [func nw_framer_write_output_no_copy(nw_framer_t, Int) -> Bool](/documentation/network/nw_framer_write_output_no_copy(_:_:))
- [func nw_group_descriptor_add_endpoint(nw_group_descriptor_t, nw_endpoint_t) -> Bool](/documentation/network/nw_group_descriptor_add_endpoint(_:_:))
- [func nw_group_descriptor_create_multicast(nw_endpoint_t) -> nw_group_descriptor_t](/documentation/network/nw_group_descriptor_create_multicast(_:))

#### Customizing Multicast Behavior

- [func nw_multicast_group_descriptor_set_disable_unicast_traffic(nw_group_descriptor_t, Bool)](/documentation/network/nw_multicast_group_descriptor_set_disable_unicast_traffic(_:_:))
- [func nw_multicast_group_descriptor_get_disable_unicast_traffic(nw_group_descriptor_t) -> Bool](/documentation/network/nw_multicast_group_descriptor_get_disable_unicast_traffic(_:))
- [func nw_multicast_group_descriptor_set_specific_source(nw_group_descriptor_t, nw_endpoint_t)](/documentation/network/nw_multicast_group_descriptor_set_specific_source(_:_:))
- [func nw_group_descriptor_create_multiplex(nw_endpoint_t) -> nw_group_descriptor_t](/documentation/network/nw_group_descriptor_create_multiplex(_:))
- [func nw_group_descriptor_enumerate_endpoints(nw_group_descriptor_t, (nw_endpoint_t) -> Bool)](/documentation/network/nw_group_descriptor_enumerate_endpoints(_:_:))
- [func nw_interface_get_index(nw_interface_t) -> UInt32](/documentation/network/nw_interface_get_index(_:))
- [func nw_interface_get_name(nw_interface_t) -> UnsafePointer<CChar>](/documentation/network/nw_interface_get_name(_:))
- [func nw_interface_get_type(nw_interface_t) -> nw_interface_type_t](/documentation/network/nw_interface_get_type(_:))
- [func nw_ip_create_metadata() -> nw_protocol_metadata_t](/documentation/network/nw_ip_create_metadata())
- [func nw_ip_metadata_get_ecn_flag(nw_protocol_metadata_t) -> nw_ip_ecn_flag_t](/documentation/network/nw_ip_metadata_get_ecn_flag(_:))
- [func nw_ip_metadata_get_receive_time(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_ip_metadata_get_receive_time(_:))
- [func nw_ip_metadata_get_service_class(nw_protocol_metadata_t) -> nw_service_class_t](/documentation/network/nw_ip_metadata_get_service_class(_:))
- [func nw_ip_metadata_set_ecn_flag(nw_protocol_metadata_t, nw_ip_ecn_flag_t)](/documentation/network/nw_ip_metadata_set_ecn_flag(_:_:))
- [func nw_ip_metadata_set_service_class(nw_protocol_metadata_t, nw_service_class_t)](/documentation/network/nw_ip_metadata_set_service_class(_:_:))
- [func nw_ip_options_set_calculate_receive_time(nw_protocol_options_t, Bool)](/documentation/network/nw_ip_options_set_calculate_receive_time(_:_:))
- [func nw_ip_options_set_disable_fragmentation(nw_protocol_options_t, Bool)](/documentation/network/nw_ip_options_set_disable_fragmentation(_:_:))
- [func nw_ip_options_set_disable_multicast_loopback(nw_protocol_options_t, Bool)](/documentation/network/nw_ip_options_set_disable_multicast_loopback(_:_:))
- [func nw_ip_options_set_hop_limit(nw_protocol_options_t, UInt8)](/documentation/network/nw_ip_options_set_hop_limit(_:_:))
- [func nw_ip_options_set_local_address_preference(nw_protocol_options_t, nw_ip_local_address_preference_t)](/documentation/network/nw_ip_options_set_local_address_preference(_:_:))
- [func nw_ip_options_set_use_minimum_mtu(nw_protocol_options_t, Bool)](/documentation/network/nw_ip_options_set_use_minimum_mtu(_:_:))
- [func nw_ip_options_set_version(nw_protocol_options_t, nw_ip_version_t)](/documentation/network/nw_ip_options_set_version(_:_:))
- [func nw_listener_cancel(nw_listener_t)](/documentation/network/nw_listener_cancel(_:))
- [func nw_listener_create(nw_parameters_t) -> nw_listener_t?](/documentation/network/nw_listener_create(_:))
- [func nw_listener_create_with_connection(nw_connection_t, nw_parameters_t) -> nw_listener_t?](/documentation/network/nw_listener_create_with_connection(_:_:))
- [func nw_listener_create_with_launchd_key(nw_parameters_t, UnsafePointer<CChar>) -> nw_listener_t](/documentation/network/nw_listener_create_with_launchd_key(_:_:))
- [func nw_listener_create_with_port(UnsafePointer<CChar>, nw_parameters_t) -> nw_listener_t?](/documentation/network/nw_listener_create_with_port(_:_:))
- [func nw_listener_get_new_connection_limit(nw_listener_t) -> UInt32](/documentation/network/nw_listener_get_new_connection_limit(_:))
- [func nw_listener_get_port(nw_listener_t) -> UInt16](/documentation/network/nw_listener_get_port(_:))
- [func nw_listener_set_advertise_descriptor(nw_listener_t, nw_advertise_descriptor_t?)](/documentation/network/nw_listener_set_advertise_descriptor(_:_:))
- [func nw_listener_set_advertised_endpoint_changed_handler(nw_listener_t, nw_listener_advertised_endpoint_changed_handler_t?)](/documentation/network/nw_listener_set_advertised_endpoint_changed_handler(_:_:))
- [func nw_listener_set_new_connection_group_handler(nw_listener_t, nw_listener_new_connection_group_handler_t?)](/documentation/network/nw_listener_set_new_connection_group_handler(_:_:))
- [func nw_listener_set_new_connection_handler(nw_listener_t, nw_listener_new_connection_handler_t?)](/documentation/network/nw_listener_set_new_connection_handler(_:_:))
- [func nw_listener_set_new_connection_limit(nw_listener_t, UInt32)](/documentation/network/nw_listener_set_new_connection_limit(_:_:))
- [func nw_listener_set_queue(nw_listener_t, dispatch_queue_t)](/documentation/network/nw_listener_set_queue(_:_:))
- [func nw_listener_set_state_changed_handler(nw_listener_t, nw_listener_state_changed_handler_t?)](/documentation/network/nw_listener_set_state_changed_handler(_:_:))
- [func nw_listener_start(nw_listener_t)](/documentation/network/nw_listener_start(_:))
- [func nw_multicast_group_descriptor_get_disable_unicast_traffic(nw_group_descriptor_t) -> Bool](/documentation/network/nw_multicast_group_descriptor_get_disable_unicast_traffic(_:))
- [func nw_multicast_group_descriptor_set_disable_unicast_traffic(nw_group_descriptor_t, Bool)](/documentation/network/nw_multicast_group_descriptor_set_disable_unicast_traffic(_:_:))
- [func nw_multicast_group_descriptor_set_specific_source(nw_group_descriptor_t, nw_endpoint_t)](/documentation/network/nw_multicast_group_descriptor_set_specific_source(_:_:))
- [func nw_parameters_create_application_service() -> nw_parameters_t](/documentation/network/nw_parameters_create_application_service())
- [func nw_parameters_create_quic(nw_parameters_configure_protocol_block_t) -> nw_parameters_t](/documentation/network/nw_parameters_create_quic(_:))
- [func nw_parameters_requires_dnssec_validation(nw_parameters_t) -> Bool](/documentation/network/nw_parameters_requires_dnssec_validation(_:))
- [func nw_parameters_set_requires_dnssec_validation(nw_parameters_t, Bool)](/documentation/network/nw_parameters_set_requires_dnssec_validation(_:_:))
- [func nw_path_copy_effective_local_endpoint(nw_path_t) -> nw_endpoint_t?](/documentation/network/nw_path_copy_effective_local_endpoint(_:))
- [func nw_path_copy_effective_remote_endpoint(nw_path_t) -> nw_endpoint_t?](/documentation/network/nw_path_copy_effective_remote_endpoint(_:))
- [func nw_path_enumerate_gateways(nw_path_t, (nw_endpoint_t) -> Bool)](/documentation/network/nw_path_enumerate_gateways(_:_:))
- [func nw_path_enumerate_interfaces(nw_path_t, (nw_interface_t) -> Bool)](/documentation/network/nw_path_enumerate_interfaces(_:_:))
- [func nw_path_get_status(nw_path_t) -> nw_path_status_t](/documentation/network/nw_path_get_status(_:))
- [func nw_path_get_unsatisfied_reason(nw_path_t) -> nw_path_unsatisfied_reason_t](/documentation/network/nw_path_get_unsatisfied_reason(_:))
- [func nw_path_has_dns(nw_path_t) -> Bool](/documentation/network/nw_path_has_dns(_:))
- [func nw_path_has_ipv4(nw_path_t) -> Bool](/documentation/network/nw_path_has_ipv4(_:))
- [func nw_path_has_ipv6(nw_path_t) -> Bool](/documentation/network/nw_path_has_ipv6(_:))
- [func nw_path_is_constrained(nw_path_t) -> Bool](/documentation/network/nw_path_is_constrained(_:))
- [func nw_path_is_equal(nw_path_t, nw_path_t) -> Bool](/documentation/network/nw_path_is_equal(_:_:))
- [func nw_path_is_expensive(nw_path_t) -> Bool](/documentation/network/nw_path_is_expensive(_:))
- [func nw_path_monitor_cancel(nw_path_monitor_t)](/documentation/network/nw_path_monitor_cancel(_:))
- [func nw_path_monitor_create() -> nw_path_monitor_t](/documentation/network/nw_path_monitor_create())
- [func nw_path_monitor_create_for_ethernet_channel() -> nw_path_monitor_t](/documentation/network/nw_path_monitor_create_for_ethernet_channel())
- [func nw_path_monitor_create_with_type(nw_interface_type_t) -> nw_path_monitor_t](/documentation/network/nw_path_monitor_create_with_type(_:))
- [func nw_path_monitor_prohibit_interface_type(nw_path_monitor_t, nw_interface_type_t)](/documentation/network/nw_path_monitor_prohibit_interface_type(_:_:))
- [func nw_path_monitor_set_cancel_handler(nw_path_monitor_t, nw_path_monitor_cancel_handler_t)](/documentation/network/nw_path_monitor_set_cancel_handler(_:_:))
- [func nw_path_monitor_set_queue(nw_path_monitor_t, dispatch_queue_t)](/documentation/network/nw_path_monitor_set_queue(_:_:))
- [func nw_path_monitor_set_update_handler(nw_path_monitor_t, nw_path_monitor_update_handler_t)](/documentation/network/nw_path_monitor_set_update_handler(_:_:))
- [func nw_path_monitor_start(nw_path_monitor_t)](/documentation/network/nw_path_monitor_start(_:))
- [func nw_path_uses_interface_type(nw_path_t, nw_interface_type_t) -> Bool](/documentation/network/nw_path_uses_interface_type(_:_:))
- [func nw_protocol_copy_ip_definition() -> nw_protocol_definition_t](/documentation/network/nw_protocol_copy_ip_definition())
- [func nw_protocol_copy_quic_definition() -> nw_protocol_definition_t](/documentation/network/nw_protocol_copy_quic_definition())
- [func nw_protocol_copy_tcp_definition() -> nw_protocol_definition_t](/documentation/network/nw_protocol_copy_tcp_definition())
- [func nw_protocol_copy_tls_definition() -> nw_protocol_definition_t](/documentation/network/nw_protocol_copy_tls_definition())
- [func nw_protocol_copy_udp_definition() -> nw_protocol_definition_t](/documentation/network/nw_protocol_copy_udp_definition())
- [func nw_protocol_copy_ws_definition() -> nw_protocol_definition_t](/documentation/network/nw_protocol_copy_ws_definition())
- [func nw_protocol_metadata_copy_definition(nw_protocol_metadata_t) -> nw_protocol_definition_t](/documentation/network/nw_protocol_metadata_copy_definition(_:))
- [func nw_protocol_metadata_is_framer_message(nw_protocol_metadata_t) -> Bool](/documentation/network/nw_protocol_metadata_is_framer_message(_:))
- [func nw_protocol_metadata_is_ip(nw_protocol_metadata_t) -> Bool](/documentation/network/nw_protocol_metadata_is_ip(_:))
- [func nw_protocol_metadata_is_quic(nw_protocol_metadata_t) -> Bool](/documentation/network/nw_protocol_metadata_is_quic(_:))
- [func nw_protocol_metadata_is_tcp(nw_protocol_metadata_t) -> Bool](/documentation/network/nw_protocol_metadata_is_tcp(_:))
- [func nw_protocol_metadata_is_tls(nw_protocol_metadata_t) -> Bool](/documentation/network/nw_protocol_metadata_is_tls(_:))
- [func nw_protocol_metadata_is_udp(nw_protocol_metadata_t) -> Bool](/documentation/network/nw_protocol_metadata_is_udp(_:))
- [func nw_protocol_metadata_is_ws(nw_protocol_metadata_t) -> Bool](/documentation/network/nw_protocol_metadata_is_ws(_:))
- [func nw_protocol_options_is_quic(nw_protocol_options_t) -> Bool](/documentation/network/nw_protocol_options_is_quic(_:))
- [func nw_proxy_config_add_excluded_domain(nw_proxy_config_t, UnsafePointer<CChar>)](/documentation/network/nw_proxy_config_add_excluded_domain(_:_:))
- [func nw_proxy_config_add_match_domain(nw_proxy_config_t, UnsafePointer<CChar>)](/documentation/network/nw_proxy_config_add_match_domain(_:_:))
- [func nw_proxy_config_clear_excluded_domains(nw_proxy_config_t)](/documentation/network/nw_proxy_config_clear_excluded_domains(_:))
- [func nw_proxy_config_clear_match_domains(nw_proxy_config_t)](/documentation/network/nw_proxy_config_clear_match_domains(_:))
- [func nw_proxy_config_enumerate_excluded_domains(nw_proxy_config_t, (UnsafePointer<CChar>) -> Void)](/documentation/network/nw_proxy_config_enumerate_excluded_domains(_:_:))
- [func nw_proxy_config_enumerate_match_domains(nw_proxy_config_t, (UnsafePointer<CChar>) -> Void)](/documentation/network/nw_proxy_config_enumerate_match_domains(_:_:))
- [func nw_quic_add_tls_application_protocol(nw_protocol_options_t, UnsafePointer<CChar>)](/documentation/network/nw_quic_add_tls_application_protocol(_:_:))
- [func nw_quic_copy_sec_protocol_metadata(nw_protocol_metadata_t) -> sec_protocol_metadata_t](/documentation/network/nw_quic_copy_sec_protocol_metadata(_:))
- [func nw_quic_copy_sec_protocol_options(nw_protocol_options_t) -> sec_protocol_options_t](/documentation/network/nw_quic_copy_sec_protocol_options(_:))
- [func nw_quic_create_options() -> nw_protocol_options_t](/documentation/network/nw_quic_create_options())
- [func nw_quic_get_application_error(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_application_error(_:))
- [func nw_quic_get_application_error_reason(nw_protocol_metadata_t) -> UnsafePointer<CChar>?](/documentation/network/nw_quic_get_application_error_reason(_:))
- [func nw_quic_get_idle_timeout(nw_protocol_options_t) -> UInt32](/documentation/network/nw_quic_get_idle_timeout(_:))
- [func nw_quic_get_initial_max_data(nw_protocol_options_t) -> UInt64](/documentation/network/nw_quic_get_initial_max_data(_:))
- [func nw_quic_get_initial_max_stream_data_bidirectional_local(nw_protocol_options_t) -> UInt64](/documentation/network/nw_quic_get_initial_max_stream_data_bidirectional_local(_:))
- [func nw_quic_get_initial_max_stream_data_bidirectional_remote(nw_protocol_options_t) -> UInt64](/documentation/network/nw_quic_get_initial_max_stream_data_bidirectional_remote(_:))
- [func nw_quic_get_initial_max_stream_data_unidirectional(nw_protocol_options_t) -> UInt64](/documentation/network/nw_quic_get_initial_max_stream_data_unidirectional(_:))
- [func nw_quic_get_initial_max_streams_bidirectional(nw_protocol_options_t) -> UInt64](/documentation/network/nw_quic_get_initial_max_streams_bidirectional(_:))
- [func nw_quic_get_initial_max_streams_unidirectional(nw_protocol_options_t) -> UInt64](/documentation/network/nw_quic_get_initial_max_streams_unidirectional(_:))
- [func nw_quic_get_keepalive_interval(nw_protocol_metadata_t) -> UInt16](/documentation/network/nw_quic_get_keepalive_interval(_:))
- [func nw_quic_get_local_max_streams_bidirectional(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_local_max_streams_bidirectional(_:))
- [func nw_quic_get_local_max_streams_unidirectional(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_local_max_streams_unidirectional(_:))
- [func nw_quic_get_max_datagram_frame_size(nw_protocol_options_t) -> UInt16](/documentation/network/nw_quic_get_max_datagram_frame_size(_:))
- [func nw_quic_get_max_udp_payload_size(nw_protocol_options_t) -> UInt16](/documentation/network/nw_quic_get_max_udp_payload_size(_:))
- [func nw_quic_get_remote_idle_timeout(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_remote_idle_timeout(_:))
- [func nw_quic_get_remote_max_streams_bidirectional(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_remote_max_streams_bidirectional(_:))
- [func nw_quic_get_remote_max_streams_unidirectional(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_remote_max_streams_unidirectional(_:))
- [func nw_quic_get_stream_application_error(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_stream_application_error(_:))
- [func nw_quic_get_stream_id(nw_protocol_metadata_t) -> UInt64](/documentation/network/nw_quic_get_stream_id(_:))
- [func nw_quic_get_stream_is_datagram(nw_protocol_options_t) -> Bool](/documentation/network/nw_quic_get_stream_is_datagram(_:))
- [func nw_quic_get_stream_is_unidirectional(nw_protocol_options_t) -> Bool](/documentation/network/nw_quic_get_stream_is_unidirectional(_:))
- [func nw_quic_get_stream_type(nw_protocol_metadata_t) -> UInt8](/documentation/network/nw_quic_get_stream_type(_:))
- [func nw_quic_get_stream_usable_datagram_frame_size(nw_protocol_metadata_t) -> UInt16](/documentation/network/nw_quic_get_stream_usable_datagram_frame_size(_:))
- [func nw_quic_set_application_error(nw_protocol_metadata_t, UInt64, UnsafePointer<CChar>?)](/documentation/network/nw_quic_set_application_error(_:_:_:))
- [func nw_quic_set_idle_timeout(nw_protocol_options_t, UInt32)](/documentation/network/nw_quic_set_idle_timeout(_:_:))
- [func nw_quic_set_initial_max_data(nw_protocol_options_t, UInt64)](/documentation/network/nw_quic_set_initial_max_data(_:_:))
- [func nw_quic_set_initial_max_stream_data_bidirectional_local(nw_protocol_options_t, UInt64)](/documentation/network/nw_quic_set_initial_max_stream_data_bidirectional_local(_:_:))
- [func nw_quic_set_initial_max_stream_data_bidirectional_remote(nw_protocol_options_t, UInt64)](/documentation/network/nw_quic_set_initial_max_stream_data_bidirectional_remote(_:_:))
- [func nw_quic_set_initial_max_stream_data_unidirectional(nw_protocol_options_t, UInt64)](/documentation/network/nw_quic_set_initial_max_stream_data_unidirectional(_:_:))
- [func nw_quic_set_initial_max_streams_bidirectional(nw_protocol_options_t, UInt64)](/documentation/network/nw_quic_set_initial_max_streams_bidirectional(_:_:))
- [func nw_quic_set_initial_max_streams_unidirectional(nw_protocol_options_t, UInt64)](/documentation/network/nw_quic_set_initial_max_streams_unidirectional(_:_:))
- [func nw_quic_set_keepalive_interval(nw_protocol_metadata_t, UInt16)](/documentation/network/nw_quic_set_keepalive_interval(_:_:))
- [func nw_quic_set_local_max_streams_bidirectional(nw_protocol_metadata_t, UInt64)](/documentation/network/nw_quic_set_local_max_streams_bidirectional(_:_:))
- [func nw_quic_set_local_max_streams_unidirectional(nw_protocol_metadata_t, UInt64)](/documentation/network/nw_quic_set_local_max_streams_unidirectional(_:_:))
- [func nw_quic_set_max_datagram_frame_size(nw_protocol_options_t, UInt16)](/documentation/network/nw_quic_set_max_datagram_frame_size(_:_:))
- [func nw_quic_set_max_udp_payload_size(nw_protocol_options_t, UInt16)](/documentation/network/nw_quic_set_max_udp_payload_size(_:_:))
- [func nw_quic_set_stream_application_error(nw_protocol_metadata_t, UInt64)](/documentation/network/nw_quic_set_stream_application_error(_:_:))
- [func nw_quic_set_stream_is_datagram(nw_protocol_options_t, Bool)](/documentation/network/nw_quic_set_stream_is_datagram(_:_:))
- [func nw_quic_set_stream_is_unidirectional(nw_protocol_options_t, Bool)](/documentation/network/nw_quic_set_stream_is_unidirectional(_:_:))
- [func nw_resolution_report_copy_preferred_endpoint(nw_resolution_report_t) -> nw_endpoint_t](/documentation/network/nw_resolution_report_copy_preferred_endpoint(_:))
- [func nw_resolution_report_copy_successful_endpoint(nw_resolution_report_t) -> nw_endpoint_t](/documentation/network/nw_resolution_report_copy_successful_endpoint(_:))
- [func nw_resolution_report_get_endpoint_count(nw_resolution_report_t) -> UInt32](/documentation/network/nw_resolution_report_get_endpoint_count(_:))
- [func nw_resolution_report_get_milliseconds(nw_resolution_report_t) -> UInt64](/documentation/network/nw_resolution_report_get_milliseconds(_:))
- [func nw_resolution_report_get_protocol(nw_resolution_report_t) -> nw_report_resolution_protocol_t](/documentation/network/nw_resolution_report_get_protocol(_:))
- [func nw_resolution_report_get_source(nw_resolution_report_t) -> nw_report_resolution_source_t](/documentation/network/nw_resolution_report_get_source(_:))
- [func nw_tcp_create_options() -> nw_protocol_options_t](/documentation/network/nw_tcp_create_options())
- [func nw_tcp_get_available_receive_buffer(nw_protocol_metadata_t) -> UInt32](/documentation/network/nw_tcp_get_available_receive_buffer(_:))
- [func nw_tcp_get_available_send_buffer(nw_protocol_metadata_t) -> UInt32](/documentation/network/nw_tcp_get_available_send_buffer(_:))
- [func nw_tcp_options_set_connection_timeout(nw_protocol_options_t, UInt32)](/documentation/network/nw_tcp_options_set_connection_timeout(_:_:))
- [func nw_tcp_options_set_disable_ack_stretching(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_disable_ack_stretching(_:_:))
- [func nw_tcp_options_set_disable_ecn(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_disable_ecn(_:_:))
- [func nw_tcp_options_set_enable_fast_open(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_enable_fast_open(_:_:))
- [func nw_tcp_options_set_enable_keepalive(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_enable_keepalive(_:_:))
- [func nw_tcp_options_set_keepalive_count(nw_protocol_options_t, UInt32)](/documentation/network/nw_tcp_options_set_keepalive_count(_:_:))
- [func nw_tcp_options_set_keepalive_idle_time(nw_protocol_options_t, UInt32)](/documentation/network/nw_tcp_options_set_keepalive_idle_time(_:_:))
- [func nw_tcp_options_set_keepalive_interval(nw_protocol_options_t, UInt32)](/documentation/network/nw_tcp_options_set_keepalive_interval(_:_:))
- [func nw_tcp_options_set_maximum_segment_size(nw_protocol_options_t, UInt32)](/documentation/network/nw_tcp_options_set_maximum_segment_size(_:_:))
- [func nw_tcp_options_set_multipath_force_version(nw_protocol_options_t, nw_multipath_version_t)](/documentation/network/nw_tcp_options_set_multipath_force_version(_:_:))
- [func nw_tcp_options_set_no_delay(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_no_delay(_:_:))
- [func nw_tcp_options_set_no_options(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_no_options(_:_:))
- [func nw_tcp_options_set_no_push(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_no_push(_:_:))
- [func nw_tcp_options_set_persist_timeout(nw_protocol_options_t, UInt32)](/documentation/network/nw_tcp_options_set_persist_timeout(_:_:))
- [func nw_tcp_options_set_retransmit_connection_drop_time(nw_protocol_options_t, UInt32)](/documentation/network/nw_tcp_options_set_retransmit_connection_drop_time(_:_:))
- [func nw_tcp_options_set_retransmit_fin_drop(nw_protocol_options_t, Bool)](/documentation/network/nw_tcp_options_set_retransmit_fin_drop(_:_:))
- [func nw_tls_copy_sec_protocol_metadata(nw_protocol_metadata_t) -> sec_protocol_metadata_t](/documentation/network/nw_tls_copy_sec_protocol_metadata(_:))
- [func nw_tls_copy_sec_protocol_options(nw_protocol_options_t) -> sec_protocol_options_t](/documentation/network/nw_tls_copy_sec_protocol_options(_:))
- [func nw_tls_create_options() -> nw_protocol_options_t](/documentation/network/nw_tls_create_options())
- [func nw_txt_record_access_bytes(nw_txt_record_t, nw_txt_record_access_bytes_t) -> Bool](/documentation/network/nw_txt_record_access_bytes(_:_:))
- [func nw_txt_record_access_key(nw_txt_record_t, UnsafePointer<CChar>, nw_txt_record_access_key_t) -> Bool](/documentation/network/nw_txt_record_access_key(_:_:_:))
- [func nw_txt_record_apply(nw_txt_record_t, nw_txt_record_applier_t) -> Bool](/documentation/network/nw_txt_record_apply(_:_:))
- [func nw_txt_record_copy(nw_txt_record_t?) -> nw_txt_record_t?](/documentation/network/nw_txt_record_copy(_:))
- [func nw_txt_record_create_dictionary() -> nw_txt_record_t](/documentation/network/nw_txt_record_create_dictionary())
- [func nw_txt_record_create_with_bytes(UnsafePointer<UInt8>, Int) -> nw_txt_record_t](/documentation/network/nw_txt_record_create_with_bytes(_:_:))
- [func nw_txt_record_find_key(nw_txt_record_t, UnsafePointer<CChar>) -> nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key(_:_:))
- [func nw_txt_record_get_key_count(nw_txt_record_t?) -> Int](/documentation/network/nw_txt_record_get_key_count(_:))
- [func nw_txt_record_is_dictionary(nw_txt_record_t) -> Bool](/documentation/network/nw_txt_record_is_dictionary(_:))
- [func nw_txt_record_is_equal(nw_txt_record_t?, nw_txt_record_t?) -> Bool](/documentation/network/nw_txt_record_is_equal(_:_:))
- [func nw_txt_record_remove_key(nw_txt_record_t, UnsafePointer<CChar>) -> Bool](/documentation/network/nw_txt_record_remove_key(_:_:))
- [func nw_txt_record_set_key(nw_txt_record_t, UnsafePointer<CChar>, UnsafePointer<UInt8>?, Int) -> Bool](/documentation/network/nw_txt_record_set_key(_:_:_:_:))
- [func nw_udp_create_metadata() -> nw_protocol_metadata_t](/documentation/network/nw_udp_create_metadata())
- [func nw_udp_create_options() -> nw_protocol_options_t](/documentation/network/nw_udp_create_options())
- [func nw_udp_options_set_prefer_no_checksum(nw_protocol_options_t, Bool)](/documentation/network/nw_udp_options_set_prefer_no_checksum(_:_:))
- [func nw_ws_create_metadata(nw_ws_opcode_t) -> nw_protocol_metadata_t](/documentation/network/nw_ws_create_metadata(_:))
- [func nw_ws_create_options(nw_ws_version_t) -> nw_protocol_options_t](/documentation/network/nw_ws_create_options(_:))
- [func nw_ws_metadata_copy_server_response(nw_protocol_metadata_t) -> nw_ws_response_t](/documentation/network/nw_ws_metadata_copy_server_response(_:))
- [func nw_ws_metadata_get_close_code(nw_protocol_metadata_t) -> nw_ws_close_code_t](/documentation/network/nw_ws_metadata_get_close_code(_:))
- [func nw_ws_metadata_get_opcode(nw_protocol_metadata_t) -> nw_ws_opcode_t](/documentation/network/nw_ws_metadata_get_opcode(_:))
- [func nw_ws_metadata_set_close_code(nw_protocol_metadata_t, nw_ws_close_code_t)](/documentation/network/nw_ws_metadata_set_close_code(_:_:))
- [func nw_ws_metadata_set_pong_handler(nw_protocol_metadata_t, dispatch_queue_t, nw_ws_pong_handler_t)](/documentation/network/nw_ws_metadata_set_pong_handler(_:_:_:))
- [func nw_ws_options_add_additional_header(nw_protocol_options_t, UnsafePointer<CChar>, UnsafePointer<CChar>)](/documentation/network/nw_ws_options_add_additional_header(_:_:_:))
- [func nw_ws_options_add_subprotocol(nw_protocol_options_t, UnsafePointer<CChar>)](/documentation/network/nw_ws_options_add_subprotocol(_:_:))
- [func nw_ws_options_set_auto_reply_ping(nw_protocol_options_t, Bool)](/documentation/network/nw_ws_options_set_auto_reply_ping(_:_:))
- [func nw_ws_options_set_client_request_handler(nw_protocol_options_t, dispatch_queue_t, nw_ws_client_request_handler_t)](/documentation/network/nw_ws_options_set_client_request_handler(_:_:_:))
- [func nw_ws_options_set_maximum_message_size(nw_protocol_options_t, Int)](/documentation/network/nw_ws_options_set_maximum_message_size(_:_:))
- [func nw_ws_options_set_skip_handshake(nw_protocol_options_t, Bool)](/documentation/network/nw_ws_options_set_skip_handshake(_:_:))
- [func nw_ws_request_enumerate_additional_headers(nw_ws_request_t, (UnsafePointer<CChar>, UnsafePointer<CChar>) -> Bool) -> Bool](/documentation/network/nw_ws_request_enumerate_additional_headers(_:_:))
- [func nw_ws_request_enumerate_subprotocols(nw_ws_request_t, (UnsafePointer<CChar>) -> Bool) -> Bool](/documentation/network/nw_ws_request_enumerate_subprotocols(_:_:))
- [func nw_ws_response_add_additional_header(nw_ws_response_t, UnsafePointer<CChar>, UnsafePointer<CChar>)](/documentation/network/nw_ws_response_add_additional_header(_:_:_:))
- [func nw_ws_response_create(nw_ws_response_status_t, UnsafePointer<CChar>?) -> nw_ws_response_t](/documentation/network/nw_ws_response_create(_:_:))
- [func nw_ws_response_enumerate_additional_headers(nw_ws_response_t, (UnsafePointer<CChar>, UnsafePointer<CChar>) -> Bool) -> Bool](/documentation/network/nw_ws_response_enumerate_additional_headers(_:_:))
- [func nw_ws_response_get_selected_subprotocol(nw_ws_response_t) -> UnsafePointer<CChar>?](/documentation/network/nw_ws_response_get_selected_subprotocol(_:))
- [func nw_ws_response_get_status(nw_ws_response_t?) -> nw_ws_response_status_t](/documentation/network/nw_ws_response_get_status(_:))
- [Network Data Types](/documentation/network/network-data-types)

### Data Types

- [nw_advertise_descriptor_t](/documentation/network/nw_advertise_descriptor_t)

#### Advertising Bonjour Services

- [func nw_advertise_descriptor_create_bonjour_service(UnsafePointer<CChar>?, UnsafePointer<CChar>, UnsafePointer<CChar>?) -> nw_advertise_descriptor_t?](/documentation/network/nw_advertise_descriptor_create_bonjour_service(_:_:_:))
- [func nw_advertise_descriptor_set_no_auto_rename(nw_advertise_descriptor_t, Bool)](/documentation/network/nw_advertise_descriptor_set_no_auto_rename(_:_:))
- [func nw_advertise_descriptor_get_no_auto_rename(nw_advertise_descriptor_t) -> Bool](/documentation/network/nw_advertise_descriptor_get_no_auto_rename(_:))

#### Configuring TXT Records

- [func nw_advertise_descriptor_set_txt_record(nw_advertise_descriptor_t, UnsafeRawPointer?, Int)](/documentation/network/nw_advertise_descriptor_set_txt_record(_:_:_:))
- [func nw_advertise_descriptor_set_txt_record_object(nw_advertise_descriptor_t, nw_txt_record_t?)](/documentation/network/nw_advertise_descriptor_set_txt_record_object(_:_:))
- [func nw_advertise_descriptor_copy_txt_record_object(nw_advertise_descriptor_t) -> nw_txt_record_t?](/documentation/network/nw_advertise_descriptor_copy_txt_record_object(_:))
- [nw_browse_descriptor_t](/documentation/network/nw_browse_descriptor_t)

#### Creating Browse Descriptors

- [func nw_browse_descriptor_create_bonjour_service(UnsafePointer<CChar>, UnsafePointer<CChar>?) -> nw_browse_descriptor_t](/documentation/network/nw_browse_descriptor_create_bonjour_service(_:_:))
- [func nw_browse_descriptor_set_include_txt_record(nw_browse_descriptor_t, Bool)](/documentation/network/nw_browse_descriptor_set_include_txt_record(_:_:))

#### Inspecting Browse Descriptors

- [func nw_browse_descriptor_get_bonjour_service_type(nw_browse_descriptor_t) -> UnsafePointer<CChar>](/documentation/network/nw_browse_descriptor_get_bonjour_service_type(_:))
- [func nw_browse_descriptor_get_bonjour_service_domain(nw_browse_descriptor_t) -> UnsafePointer<CChar>?](/documentation/network/nw_browse_descriptor_get_bonjour_service_domain(_:))
- [func nw_browse_descriptor_get_include_txt_record(nw_browse_descriptor_t) -> Bool](/documentation/network/nw_browse_descriptor_get_include_txt_record(_:))
- [nw_browse_result_change_t](/documentation/network/nw_browse_result_change_t)

#### Browse Result Change Flags

- [var nw_browse_result_change_invalid: Int](/documentation/network/nw_browse_result_change_invalid)
- [var nw_browse_result_change_identical: Int](/documentation/network/nw_browse_result_change_identical)
- [var nw_browse_result_change_result_added: Int](/documentation/network/nw_browse_result_change_result_added)
- [var nw_browse_result_change_result_removed: Int](/documentation/network/nw_browse_result_change_result_removed)
- [var nw_browse_result_change_txt_record_changed: Int](/documentation/network/nw_browse_result_change_txt_record_changed)
- [var nw_browse_result_change_interface_added: Int](/documentation/network/nw_browse_result_change_interface_added)
- [var nw_browse_result_change_interface_removed: Int](/documentation/network/nw_browse_result_change_interface_removed)
- [nw_browse_result_enumerate_interface_t](/documentation/network/nw_browse_result_enumerate_interface_t)
- [nw_browse_result_t](/documentation/network/nw_browse_result_t)

#### Evaluating Browser Results

- [func nw_browse_result_copy_endpoint(nw_browse_result_t) -> nw_endpoint_t](/documentation/network/nw_browse_result_copy_endpoint(_:))
- [func nw_browse_result_enumerate_interfaces(nw_browse_result_t, (nw_interface_t) -> Bool)](/documentation/network/nw_browse_result_enumerate_interfaces(_:_:))
- [nw_browse_result_enumerate_interface_t](/documentation/network/nw_browse_result_enumerate_interface_t)
- [func nw_browse_result_get_interfaces_count(nw_browse_result_t) -> Int](/documentation/network/nw_browse_result_get_interfaces_count(_:))

#### Handling TXT Records

- [func nw_browse_result_copy_txt_record_object(nw_browse_result_t) -> nw_txt_record_t?](/documentation/network/nw_browse_result_copy_txt_record_object(_:))
- [nw_txt_record_t](/documentation/network/nw_txt_record_t)

##### Creating TXT Records

- [func nw_txt_record_create_dictionary() -> nw_txt_record_t](/documentation/network/nw_txt_record_create_dictionary())
- [func nw_txt_record_create_with_bytes(UnsafePointer<UInt8>, Int) -> nw_txt_record_t](/documentation/network/nw_txt_record_create_with_bytes(_:_:))
- [func nw_txt_record_copy(nw_txt_record_t?) -> nw_txt_record_t?](/documentation/network/nw_txt_record_copy(_:))
- [func nw_txt_record_set_key(nw_txt_record_t, UnsafePointer<CChar>, UnsafePointer<UInt8>?, Int) -> Bool](/documentation/network/nw_txt_record_set_key(_:_:_:_:))
- [func nw_txt_record_remove_key(nw_txt_record_t, UnsafePointer<CChar>) -> Bool](/documentation/network/nw_txt_record_remove_key(_:_:))

##### Examining TXT Records

- [func nw_txt_record_is_dictionary(nw_txt_record_t) -> Bool](/documentation/network/nw_txt_record_is_dictionary(_:))
- [func nw_txt_record_get_key_count(nw_txt_record_t?) -> Int](/documentation/network/nw_txt_record_get_key_count(_:))
- [func nw_txt_record_apply(nw_txt_record_t, nw_txt_record_applier_t) -> Bool](/documentation/network/nw_txt_record_apply(_:_:))
- [nw_txt_record_applier_t](/documentation/network/nw_txt_record_applier_t)
- [func nw_txt_record_access_key(nw_txt_record_t, UnsafePointer<CChar>, nw_txt_record_access_key_t) -> Bool](/documentation/network/nw_txt_record_access_key(_:_:_:))
- [nw_txt_record_access_key_t](/documentation/network/nw_txt_record_access_key_t)
- [func nw_txt_record_find_key(nw_txt_record_t, UnsafePointer<CChar>) -> nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key(_:_:))
- [nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_t)

###### Key Value Status

- [var nw_txt_record_find_key_invalid: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_invalid)
- [var nw_txt_record_find_key_not_present: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_not_present)
- [var nw_txt_record_find_key_no_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_no_value)
- [var nw_txt_record_find_key_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_empty_value)
- [var nw_txt_record_find_key_non_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_non_empty_value)

###### Initializers

- [init(UInt32)](/documentation/network/nw_txt_record_find_key_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_txt_record_find_key_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_txt_record_find_key_t/rawvalue)
- [func nw_txt_record_is_equal(nw_txt_record_t?, nw_txt_record_t?) -> Bool](/documentation/network/nw_txt_record_is_equal(_:_:))
- [func nw_txt_record_access_bytes(nw_txt_record_t, nw_txt_record_access_bytes_t) -> Bool](/documentation/network/nw_txt_record_access_bytes(_:_:))
- [nw_txt_record_access_bytes_t](/documentation/network/nw_txt_record_access_bytes_t)

#### Tracking Result Changes

- [func nw_browse_result_get_changes(nw_browse_result_t?, nw_browse_result_t?) -> nw_browse_result_change_t](/documentation/network/nw_browse_result_get_changes(_:_:))
- [nw_browse_result_change_t](/documentation/network/nw_browse_result_change_t)

##### Browse Result Change Flags

- [var nw_browse_result_change_invalid: Int](/documentation/network/nw_browse_result_change_invalid)
- [var nw_browse_result_change_identical: Int](/documentation/network/nw_browse_result_change_identical)
- [var nw_browse_result_change_result_added: Int](/documentation/network/nw_browse_result_change_result_added)
- [var nw_browse_result_change_result_removed: Int](/documentation/network/nw_browse_result_change_result_removed)
- [var nw_browse_result_change_txt_record_changed: Int](/documentation/network/nw_browse_result_change_txt_record_changed)
- [var nw_browse_result_change_interface_added: Int](/documentation/network/nw_browse_result_change_interface_added)
- [var nw_browse_result_change_interface_removed: Int](/documentation/network/nw_browse_result_change_interface_removed)
- [nw_browser_browse_results_changed_handler_t](/documentation/network/nw_browser_browse_results_changed_handler_t)
- [nw_browser_state_changed_handler_t](/documentation/network/nw_browser_state_changed_handler_t)
- [nw_browser_t](/documentation/network/nw_browser_t)

#### Essentials

- [NSBonjourServices](/documentation/bundleresources/information-property-list/nsbonjourservices)
- [NSLocalNetworkUsageDescription](/documentation/bundleresources/information-property-list/nslocalnetworkusagedescription)

#### Browsing for Services

- [func nw_browser_create(nw_browse_descriptor_t, nw_parameters_t?) -> nw_browser_t](/documentation/network/nw_browser_create(_:_:))
- [nw_browse_descriptor_t](/documentation/network/nw_browse_descriptor_t)

##### Creating Browse Descriptors

- [func nw_browse_descriptor_create_bonjour_service(UnsafePointer<CChar>, UnsafePointer<CChar>?) -> nw_browse_descriptor_t](/documentation/network/nw_browse_descriptor_create_bonjour_service(_:_:))
- [func nw_browse_descriptor_set_include_txt_record(nw_browse_descriptor_t, Bool)](/documentation/network/nw_browse_descriptor_set_include_txt_record(_:_:))

##### Inspecting Browse Descriptors

- [func nw_browse_descriptor_get_bonjour_service_type(nw_browse_descriptor_t) -> UnsafePointer<CChar>](/documentation/network/nw_browse_descriptor_get_bonjour_service_type(_:))
- [func nw_browse_descriptor_get_bonjour_service_domain(nw_browse_descriptor_t) -> UnsafePointer<CChar>?](/documentation/network/nw_browse_descriptor_get_bonjour_service_domain(_:))
- [func nw_browse_descriptor_get_include_txt_record(nw_browse_descriptor_t) -> Bool](/documentation/network/nw_browse_descriptor_get_include_txt_record(_:))
- [func nw_browser_set_queue(nw_browser_t, dispatch_queue_t)](/documentation/network/nw_browser_set_queue(_:_:))
- [func nw_browser_start(nw_browser_t)](/documentation/network/nw_browser_start(_:))
- [func nw_browser_set_browse_results_changed_handler(nw_browser_t, nw_browser_browse_results_changed_handler_t?)](/documentation/network/nw_browser_set_browse_results_changed_handler(_:_:))
- [nw_browser_browse_results_changed_handler_t](/documentation/network/nw_browser_browse_results_changed_handler_t)
- [nw_browse_result_t](/documentation/network/nw_browse_result_t)

##### Evaluating Browser Results

- [func nw_browse_result_copy_endpoint(nw_browse_result_t) -> nw_endpoint_t](/documentation/network/nw_browse_result_copy_endpoint(_:))
- [func nw_browse_result_enumerate_interfaces(nw_browse_result_t, (nw_interface_t) -> Bool)](/documentation/network/nw_browse_result_enumerate_interfaces(_:_:))
- [nw_browse_result_enumerate_interface_t](/documentation/network/nw_browse_result_enumerate_interface_t)
- [func nw_browse_result_get_interfaces_count(nw_browse_result_t) -> Int](/documentation/network/nw_browse_result_get_interfaces_count(_:))

##### Handling TXT Records

- [func nw_browse_result_copy_txt_record_object(nw_browse_result_t) -> nw_txt_record_t?](/documentation/network/nw_browse_result_copy_txt_record_object(_:))
- [nw_txt_record_t](/documentation/network/nw_txt_record_t)

###### Creating TXT Records

- [func nw_txt_record_create_dictionary() -> nw_txt_record_t](/documentation/network/nw_txt_record_create_dictionary())
- [func nw_txt_record_create_with_bytes(UnsafePointer<UInt8>, Int) -> nw_txt_record_t](/documentation/network/nw_txt_record_create_with_bytes(_:_:))
- [func nw_txt_record_copy(nw_txt_record_t?) -> nw_txt_record_t?](/documentation/network/nw_txt_record_copy(_:))
- [func nw_txt_record_set_key(nw_txt_record_t, UnsafePointer<CChar>, UnsafePointer<UInt8>?, Int) -> Bool](/documentation/network/nw_txt_record_set_key(_:_:_:_:))
- [func nw_txt_record_remove_key(nw_txt_record_t, UnsafePointer<CChar>) -> Bool](/documentation/network/nw_txt_record_remove_key(_:_:))

###### Examining TXT Records

- [func nw_txt_record_is_dictionary(nw_txt_record_t) -> Bool](/documentation/network/nw_txt_record_is_dictionary(_:))
- [func nw_txt_record_get_key_count(nw_txt_record_t?) -> Int](/documentation/network/nw_txt_record_get_key_count(_:))
- [func nw_txt_record_apply(nw_txt_record_t, nw_txt_record_applier_t) -> Bool](/documentation/network/nw_txt_record_apply(_:_:))
- [nw_txt_record_applier_t](/documentation/network/nw_txt_record_applier_t)
- [func nw_txt_record_access_key(nw_txt_record_t, UnsafePointer<CChar>, nw_txt_record_access_key_t) -> Bool](/documentation/network/nw_txt_record_access_key(_:_:_:))
- [nw_txt_record_access_key_t](/documentation/network/nw_txt_record_access_key_t)
- [func nw_txt_record_find_key(nw_txt_record_t, UnsafePointer<CChar>) -> nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key(_:_:))
- [nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_t)

###### Key Value Status

- [var nw_txt_record_find_key_invalid: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_invalid)
- [var nw_txt_record_find_key_not_present: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_not_present)
- [var nw_txt_record_find_key_no_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_no_value)
- [var nw_txt_record_find_key_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_empty_value)
- [var nw_txt_record_find_key_non_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_non_empty_value)

###### Initializers

- [init(UInt32)](/documentation/network/nw_txt_record_find_key_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_txt_record_find_key_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_txt_record_find_key_t/rawvalue)
- [func nw_txt_record_is_equal(nw_txt_record_t?, nw_txt_record_t?) -> Bool](/documentation/network/nw_txt_record_is_equal(_:_:))
- [func nw_txt_record_access_bytes(nw_txt_record_t, nw_txt_record_access_bytes_t) -> Bool](/documentation/network/nw_txt_record_access_bytes(_:_:))
- [nw_txt_record_access_bytes_t](/documentation/network/nw_txt_record_access_bytes_t)

##### Tracking Result Changes

- [func nw_browse_result_get_changes(nw_browse_result_t?, nw_browse_result_t?) -> nw_browse_result_change_t](/documentation/network/nw_browse_result_get_changes(_:_:))
- [nw_browse_result_change_t](/documentation/network/nw_browse_result_change_t)

###### Browse Result Change Flags

- [var nw_browse_result_change_invalid: Int](/documentation/network/nw_browse_result_change_invalid)
- [var nw_browse_result_change_identical: Int](/documentation/network/nw_browse_result_change_identical)
- [var nw_browse_result_change_result_added: Int](/documentation/network/nw_browse_result_change_result_added)
- [var nw_browse_result_change_result_removed: Int](/documentation/network/nw_browse_result_change_result_removed)
- [var nw_browse_result_change_txt_record_changed: Int](/documentation/network/nw_browse_result_change_txt_record_changed)
- [var nw_browse_result_change_interface_added: Int](/documentation/network/nw_browse_result_change_interface_added)
- [var nw_browse_result_change_interface_removed: Int](/documentation/network/nw_browse_result_change_interface_removed)

#### Managing Browsers

- [func nw_browser_set_state_changed_handler(nw_browser_t, nw_browser_state_changed_handler_t?)](/documentation/network/nw_browser_set_state_changed_handler(_:_:))
- [nw_browser_state_changed_handler_t](/documentation/network/nw_browser_state_changed_handler_t)
- [nw_browser_state_t](/documentation/network/nw_browser_state_t)

##### States

- [var nw_browser_state_invalid: nw_browser_state_t](/documentation/network/nw_browser_state_invalid)
- [var nw_browser_state_ready: nw_browser_state_t](/documentation/network/nw_browser_state_ready)
- [var nw_browser_state_failed: nw_browser_state_t](/documentation/network/nw_browser_state_failed)
- [var nw_browser_state_cancelled: nw_browser_state_t](/documentation/network/nw_browser_state_cancelled)

##### Initializers

- [init(UInt32)](/documentation/network/nw_browser_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_browser_state_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_browser_state_t/rawvalue)
- [func nw_browser_cancel(nw_browser_t)](/documentation/network/nw_browser_cancel(_:))

#### Inspecting Browsers

- [func nw_browser_copy_browse_descriptor(nw_browser_t) -> nw_browse_descriptor_t](/documentation/network/nw_browser_copy_browse_descriptor(_:))
- [func nw_browser_copy_parameters(nw_browser_t) -> nw_parameters_t](/documentation/network/nw_browser_copy_parameters(_:))
- [nw_connection_boolean_event_handler_t](/documentation/network/nw_connection_boolean_event_handler_t)
- [nw_connection_group_new_connection_handler_t](/documentation/network/nw_connection_group_new_connection_handler_t)
- [nw_connection_group_receive_handler_t](/documentation/network/nw_connection_group_receive_handler_t)
- [nw_connection_group_send_completion_t](/documentation/network/nw_connection_group_send_completion_t)
- [nw_connection_group_state_changed_handler_t](/documentation/network/nw_connection_group_state_changed_handler_t)
- [nw_connection_group_t](/documentation/network/nw_connection_group_t)

#### Establishing Group Connectivity

- [func nw_connection_group_create(nw_group_descriptor_t, nw_parameters_t) -> nw_connection_group_t](/documentation/network/nw_connection_group_create(_:_:))
- [func nw_group_descriptor_create_multicast(nw_endpoint_t) -> nw_group_descriptor_t](/documentation/network/nw_group_descriptor_create_multicast(_:))

##### Customizing Multicast Behavior

- [func nw_multicast_group_descriptor_set_disable_unicast_traffic(nw_group_descriptor_t, Bool)](/documentation/network/nw_multicast_group_descriptor_set_disable_unicast_traffic(_:_:))
- [func nw_multicast_group_descriptor_get_disable_unicast_traffic(nw_group_descriptor_t) -> Bool](/documentation/network/nw_multicast_group_descriptor_get_disable_unicast_traffic(_:))
- [func nw_multicast_group_descriptor_set_specific_source(nw_group_descriptor_t, nw_endpoint_t)](/documentation/network/nw_multicast_group_descriptor_set_specific_source(_:_:))
- [nw_group_descriptor_t](/documentation/network/nw_group_descriptor_t)
- [func nw_group_descriptor_add_endpoint(nw_group_descriptor_t, nw_endpoint_t) -> Bool](/documentation/network/nw_group_descriptor_add_endpoint(_:_:))
- [func nw_group_descriptor_enumerate_endpoints(nw_group_descriptor_t, (nw_endpoint_t) -> Bool)](/documentation/network/nw_group_descriptor_enumerate_endpoints(_:_:))
- [nw_group_descriptor_enumerate_endpoints_block_t](/documentation/network/nw_group_descriptor_enumerate_endpoints_block_t)
- [func nw_connection_group_set_queue(nw_connection_group_t, dispatch_queue_t)](/documentation/network/nw_connection_group_set_queue(_:_:))
- [func nw_connection_group_start(nw_connection_group_t)](/documentation/network/nw_connection_group_start(_:))

#### Sending and Receiving Group Messages

- [func nw_connection_group_set_receive_handler(nw_connection_group_t, UInt32, Bool, nw_connection_group_receive_handler_t?)](/documentation/network/nw_connection_group_set_receive_handler(_:_:_:_:))
- [nw_connection_group_receive_handler_t](/documentation/network/nw_connection_group_receive_handler_t)
- [func nw_connection_group_copy_remote_endpoint_for_message(nw_connection_group_t, nw_content_context_t) -> nw_endpoint_t?](/documentation/network/nw_connection_group_copy_remote_endpoint_for_message(_:_:))
- [func nw_connection_group_copy_local_endpoint_for_message(nw_connection_group_t, nw_content_context_t) -> nw_endpoint_t?](/documentation/network/nw_connection_group_copy_local_endpoint_for_message(_:_:))
- [func nw_connection_group_copy_path_for_message(nw_connection_group_t, nw_content_context_t) -> nw_path_t?](/documentation/network/nw_connection_group_copy_path_for_message(_:_:))
- [func nw_connection_group_reply(nw_connection_group_t, nw_content_context_t, nw_content_context_t, dispatch_data_t?)](/documentation/network/nw_connection_group_reply(_:_:_:_:))
- [func nw_connection_group_extract_connection_for_message(nw_connection_group_t, nw_content_context_t) -> nw_connection_t?](/documentation/network/nw_connection_group_extract_connection_for_message(_:_:))
- [func nw_connection_group_send_message(nw_connection_group_t, dispatch_data_t?, nw_endpoint_t?, nw_content_context_t, nw_connection_group_send_completion_t)](/documentation/network/nw_connection_group_send_message(_:_:_:_:_:))
- [nw_connection_group_send_completion_t](/documentation/network/nw_connection_group_send_completion_t)

#### Managing Groups

- [func nw_connection_group_set_state_changed_handler(nw_connection_group_t, nw_connection_group_state_changed_handler_t?)](/documentation/network/nw_connection_group_set_state_changed_handler(_:_:))
- [nw_connection_group_state_changed_handler_t](/documentation/network/nw_connection_group_state_changed_handler_t)
- [nw_connection_group_state_t](/documentation/network/nw_connection_group_state_t)

##### States

- [var nw_connection_group_state_invalid: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_invalid)
- [var nw_connection_group_state_waiting: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_waiting)
- [var nw_connection_group_state_ready: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_ready)
- [var nw_connection_group_state_failed: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_failed)
- [var nw_connection_group_state_cancelled: nw_connection_group_state_t](/documentation/network/nw_connection_group_state_cancelled)

##### Initializers

- [init(UInt32)](/documentation/network/nw_connection_group_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_connection_group_state_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_connection_group_state_t/rawvalue)
- [func nw_connection_group_cancel(nw_connection_group_t)](/documentation/network/nw_connection_group_cancel(_:))

#### Inspecting Groups

- [func nw_connection_group_copy_descriptor(nw_connection_group_t) -> nw_group_descriptor_t](/documentation/network/nw_connection_group_copy_descriptor(_:))
- [func nw_connection_group_copy_parameters(nw_connection_group_t) -> nw_parameters_t](/documentation/network/nw_connection_group_copy_parameters(_:))
- [nw_connection_path_event_handler_t](/documentation/network/nw_connection_path_event_handler_t)
- [nw_connection_receive_completion_t](/documentation/network/nw_connection_receive_completion_t)
- [nw_connection_send_completion_t](/documentation/network/nw_connection_send_completion_t)
- [nw_connection_state_changed_handler_t](/documentation/network/nw_connection_state_changed_handler_t)
- [nw_connection_t](/documentation/network/nw_connection_t)

#### Creating Connections

- [func nw_connection_create(nw_endpoint_t, nw_parameters_t) -> nw_connection_t](/documentation/network/nw_connection_create(_:_:))
- [func nw_connection_set_queue(nw_connection_t, dispatch_queue_t)](/documentation/network/nw_connection_set_queue(_:_:))
- [func nw_connection_start(nw_connection_t)](/documentation/network/nw_connection_start(_:))
- [func nw_connection_restart(nw_connection_t)](/documentation/network/nw_connection_restart(_:))

#### Handling State Updates

- [nw_connection_state_t](/documentation/network/nw_connection_state_t)

##### Connection States

- [var nw_connection_state_invalid: nw_connection_state_t](/documentation/network/nw_connection_state_invalid)
- [var nw_connection_state_waiting: nw_connection_state_t](/documentation/network/nw_connection_state_waiting)
- [var nw_connection_state_preparing: nw_connection_state_t](/documentation/network/nw_connection_state_preparing)
- [var nw_connection_state_ready: nw_connection_state_t](/documentation/network/nw_connection_state_ready)
- [var nw_connection_state_failed: nw_connection_state_t](/documentation/network/nw_connection_state_failed)
- [var nw_connection_state_cancelled: nw_connection_state_t](/documentation/network/nw_connection_state_cancelled)

##### Initializers

- [init(UInt32)](/documentation/network/nw_connection_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_connection_state_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_connection_state_t/rawvalue)
- [func nw_connection_set_state_changed_handler(nw_connection_t, nw_connection_state_changed_handler_t?)](/documentation/network/nw_connection_set_state_changed_handler(_:_:))
- [nw_connection_state_changed_handler_t](/documentation/network/nw_connection_state_changed_handler_t)

#### Sending and Receiving Data

- [func nw_connection_send(nw_connection_t, dispatch_data_t?, nw_content_context_t, Bool, nw_connection_send_completion_t)](/documentation/network/nw_connection_send(_:_:_:_:_:))
- [nw_connection_send_completion_t](/documentation/network/nw_connection_send_completion_t)
- [nw_content_context_t](/documentation/network/nw_content_context_t)

##### Creating Custom Send Contexts

- [func nw_content_context_create(UnsafePointer<CChar>) -> nw_content_context_t](/documentation/network/nw_content_context_create(_:))
- [func nw_content_context_set_metadata_for_protocol(nw_content_context_t, nw_protocol_metadata_t)](/documentation/network/nw_content_context_set_metadata_for_protocol(_:_:))
- [nw_protocol_metadata_t](/documentation/network/nw_protocol_metadata_t)

###### Inspecting Metadata

- [func nw_protocol_metadata_copy_definition(nw_protocol_metadata_t) -> nw_protocol_definition_t](/documentation/network/nw_protocol_metadata_copy_definition(_:))
- [func nw_content_context_set_antecedent(nw_content_context_t, nw_content_context_t?)](/documentation/network/nw_content_context_set_antecedent(_:_:))
- [func nw_content_context_copy_antecedent(nw_content_context_t) -> nw_content_context_t?](/documentation/network/nw_content_context_copy_antecedent(_:))
- [func nw_content_context_set_expiration_milliseconds(nw_content_context_t, UInt64)](/documentation/network/nw_content_context_set_expiration_milliseconds(_:_:))
- [func nw_content_context_get_expiration_milliseconds(nw_content_context_t) -> UInt64](/documentation/network/nw_content_context_get_expiration_milliseconds(_:))
- [func nw_content_context_set_relative_priority(nw_content_context_t, Double)](/documentation/network/nw_content_context_set_relative_priority(_:_:))
- [func nw_content_context_get_relative_priority(nw_content_context_t) -> Double](/documentation/network/nw_content_context_get_relative_priority(_:))
- [func nw_content_context_set_is_final(nw_content_context_t, Bool)](/documentation/network/nw_content_context_set_is_final(_:_:))
- [func nw_content_context_get_identifier(nw_content_context_t) -> UnsafePointer<CChar>](/documentation/network/nw_content_context_get_identifier(_:))

##### Inspecting Receive Contexts

- [func nw_content_context_get_is_final(nw_content_context_t) -> Bool](/documentation/network/nw_content_context_get_is_final(_:))
- [func nw_content_context_copy_protocol_metadata(nw_content_context_t, nw_protocol_definition_t) -> nw_protocol_metadata_t?](/documentation/network/nw_content_context_copy_protocol_metadata(_:_:))
- [func nw_content_context_foreach_protocol_metadata(nw_content_context_t, (nw_protocol_definition_t, nw_protocol_metadata_t) -> Void)](/documentation/network/nw_content_context_foreach_protocol_metadata(_:_:))
- [func nw_connection_receive(nw_connection_t, UInt32, UInt32, nw_connection_receive_completion_t)](/documentation/network/nw_connection_receive(_:_:_:_:))
- [nw_connection_receive_completion_t](/documentation/network/nw_connection_receive_completion_t)
- [func nw_connection_receive_message(nw_connection_t, nw_connection_receive_completion_t)](/documentation/network/nw_connection_receive_message(_:_:))
- [func nw_connection_batch(nw_connection_t, () -> Void)](/documentation/network/nw_connection_batch(_:_:))
- [func nw_connection_get_maximum_datagram_size(nw_connection_t) -> UInt32](/documentation/network/nw_connection_get_maximum_datagram_size(_:))

#### Canceling Connections

- [func nw_connection_cancel(nw_connection_t)](/documentation/network/nw_connection_cancel(_:))
- [func nw_connection_force_cancel(nw_connection_t)](/documentation/network/nw_connection_force_cancel(_:))
- [func nw_connection_cancel_current_endpoint(nw_connection_t)](/documentation/network/nw_connection_cancel_current_endpoint(_:))

#### Handling Path Updates

- [func nw_connection_copy_current_path(nw_connection_t) -> nw_path_t?](/documentation/network/nw_connection_copy_current_path(_:))
- [func nw_connection_set_path_changed_handler(nw_connection_t, nw_connection_path_event_handler_t?)](/documentation/network/nw_connection_set_path_changed_handler(_:_:))
- [nw_connection_path_event_handler_t](/documentation/network/nw_connection_path_event_handler_t)
- [func nw_connection_set_viability_changed_handler(nw_connection_t, nw_connection_boolean_event_handler_t?)](/documentation/network/nw_connection_set_viability_changed_handler(_:_:))
- [func nw_connection_set_better_path_available_handler(nw_connection_t, nw_connection_boolean_event_handler_t?)](/documentation/network/nw_connection_set_better_path_available_handler(_:_:))
- [nw_connection_boolean_event_handler_t](/documentation/network/nw_connection_boolean_event_handler_t)

#### Collecting Connection Metrics

- [nw_establishment_report_t](/documentation/network/nw_establishment_report_t)

##### Inspecting Connection Attempts

- [func nw_establishment_report_get_duration_milliseconds(nw_establishment_report_t) -> UInt64](/documentation/network/nw_establishment_report_get_duration_milliseconds(_:))
- [func nw_establishment_report_get_previous_attempt_count(nw_establishment_report_t) -> UInt32](/documentation/network/nw_establishment_report_get_previous_attempt_count(_:))
- [func nw_establishment_report_get_attempt_started_after_milliseconds(nw_establishment_report_t) -> UInt64](/documentation/network/nw_establishment_report_get_attempt_started_after_milliseconds(_:))

##### Inspecting Resolution

- [func nw_establishment_report_enumerate_resolution_reports(nw_establishment_report_t, (nw_resolution_report_t) -> Bool)](/documentation/network/nw_establishment_report_enumerate_resolution_reports(_:_:))
- [nw_report_resolution_report_enumerator_t](/documentation/network/nw_report_resolution_report_enumerator_t)
- [nw_resolution_report_t](/documentation/network/nw_resolution_report_t)
- [func nw_resolution_report_get_milliseconds(nw_resolution_report_t) -> UInt64](/documentation/network/nw_resolution_report_get_milliseconds(_:))
- [func nw_resolution_report_get_source(nw_resolution_report_t) -> nw_report_resolution_source_t](/documentation/network/nw_resolution_report_get_source(_:))
- [nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_t)

###### Resolution Sources

- [var nw_report_resolution_source_query: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_query)
- [var nw_report_resolution_source_cache: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_cache)
- [var nw_report_resolution_source_expired_cache: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_expired_cache)

###### Initializers

- [init(UInt32)](/documentation/network/nw_report_resolution_source_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_report_resolution_source_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_report_resolution_source_t/rawvalue)
- [func nw_resolution_report_get_protocol(nw_resolution_report_t) -> nw_report_resolution_protocol_t](/documentation/network/nw_resolution_report_get_protocol(_:))
- [nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_t)

###### Resolution Transports

- [var nw_report_resolution_protocol_unknown: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_unknown)
- [var nw_report_resolution_protocol_udp: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_udp)
- [var nw_report_resolution_protocol_tcp: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_tcp)
- [var nw_report_resolution_protocol_tls: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_tls)
- [var nw_report_resolution_protocol_https: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_https)

###### Initializers

- [init(UInt32)](/documentation/network/nw_report_resolution_protocol_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_report_resolution_protocol_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_report_resolution_protocol_t/rawvalue)
- [func nw_resolution_report_copy_successful_endpoint(nw_resolution_report_t) -> nw_endpoint_t](/documentation/network/nw_resolution_report_copy_successful_endpoint(_:))
- [func nw_resolution_report_copy_preferred_endpoint(nw_resolution_report_t) -> nw_endpoint_t](/documentation/network/nw_resolution_report_copy_preferred_endpoint(_:))
- [func nw_resolution_report_get_endpoint_count(nw_resolution_report_t) -> UInt32](/documentation/network/nw_resolution_report_get_endpoint_count(_:))
- [func nw_establishment_report_enumerate_resolutions(nw_establishment_report_t, (nw_report_resolution_source_t, UInt64, UInt32, nw_endpoint_t, nw_endpoint_t) -> Bool)](/documentation/network/nw_establishment_report_enumerate_resolutions(_:_:))
- [nw_report_resolution_enumerator_t](/documentation/network/nw_report_resolution_enumerator_t)

##### Inspecting Protocol Handshakes

- [func nw_establishment_report_enumerate_protocols(nw_establishment_report_t, (nw_protocol_definition_t, UInt64, UInt64) -> Bool)](/documentation/network/nw_establishment_report_enumerate_protocols(_:_:))
- [nw_report_protocol_enumerator_t](/documentation/network/nw_report_protocol_enumerator_t)

##### Checking for Proxies

- [func nw_establishment_report_get_proxy_configured(nw_establishment_report_t) -> Bool](/documentation/network/nw_establishment_report_get_proxy_configured(_:))
- [func nw_establishment_report_get_used_proxy(nw_establishment_report_t) -> Bool](/documentation/network/nw_establishment_report_get_used_proxy(_:))
- [func nw_establishment_report_copy_proxy_endpoint(nw_establishment_report_t) -> nw_endpoint_t?](/documentation/network/nw_establishment_report_copy_proxy_endpoint(_:))
- [func nw_connection_access_establishment_report(nw_connection_t, dispatch_queue_t, nw_establishment_report_access_block_t)](/documentation/network/nw_connection_access_establishment_report(_:_:_:))
- [nw_establishment_report_access_block_t](/documentation/network/nw_establishment_report_access_block_t)
- [nw_data_transfer_report_t](/documentation/network/nw_data_transfer_report_t)

##### Collecting Reports

- [func nw_data_transfer_report_collect(nw_data_transfer_report_t, dispatch_queue_t, nw_data_transfer_report_collect_block_t)](/documentation/network/nw_data_transfer_report_collect(_:_:_:))
- [nw_data_transfer_report_collect_block_t](/documentation/network/nw_data_transfer_report_collect_block_t)
- [func nw_data_transfer_report_get_state(nw_data_transfer_report_t) -> nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_get_state(_:))
- [nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_t)

###### Report States

- [var nw_data_transfer_report_state_collecting: nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_collecting)
- [var nw_data_transfer_report_state_collected: nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_collected)

###### Initializers

- [init(UInt32)](/documentation/network/nw_data_transfer_report_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_data_transfer_report_state_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_data_transfer_report_state_t/rawvalue)

##### Identifying Paths

- [func nw_data_transfer_report_get_path_count(nw_data_transfer_report_t) -> UInt32](/documentation/network/nw_data_transfer_report_get_path_count(_:))
- [func nw_data_transfer_report_get_duration_milliseconds(nw_data_transfer_report_t) -> UInt64](/documentation/network/nw_data_transfer_report_get_duration_milliseconds(_:))
- [func nw_data_transfer_report_copy_path_interface(nw_data_transfer_report_t, UInt32) -> nw_interface_t](/documentation/network/nw_data_transfer_report_copy_path_interface(_:_:))

##### Inspecting Application Metrics

- [func nw_data_transfer_report_get_received_application_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_application_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_application_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_application_byte_count(_:_:))

##### Inspecting Transport Metrics

- [func nw_data_transfer_report_get_received_transport_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_byte_count(_:_:))
- [func nw_data_transfer_report_get_received_transport_duplicate_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_duplicate_byte_count(_:_:))
- [func nw_data_transfer_report_get_received_transport_out_of_order_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_out_of_order_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_transport_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_transport_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_transport_retransmitted_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_transport_retransmitted_byte_count(_:_:))
- [func nw_data_transfer_report_get_transport_smoothed_rtt_milliseconds(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_smoothed_rtt_milliseconds(_:_:))
- [func nw_data_transfer_report_get_transport_minimum_rtt_milliseconds(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_minimum_rtt_milliseconds(_:_:))
- [func nw_data_transfer_report_get_transport_rtt_variance(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_rtt_variance(_:_:))

##### Inspecting Packet Metrics

- [func nw_data_transfer_report_get_received_ip_packet_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_ip_packet_count(_:_:))
- [func nw_data_transfer_report_get_sent_ip_packet_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_ip_packet_count(_:_:))
- [func nw_connection_create_new_data_transfer_report(nw_connection_t) -> nw_data_transfer_report_t](/documentation/network/nw_connection_create_new_data_transfer_report(_:))

#### Copying Connection State

- [func nw_connection_copy_protocol_metadata(nw_connection_t, nw_protocol_definition_t) -> nw_protocol_metadata_t?](/documentation/network/nw_connection_copy_protocol_metadata(_:_:))
- [func nw_connection_copy_endpoint(nw_connection_t) -> nw_endpoint_t](/documentation/network/nw_connection_copy_endpoint(_:))
- [func nw_connection_copy_parameters(nw_connection_t) -> nw_parameters_t](/documentation/network/nw_connection_copy_parameters(_:))
- [func nw_connection_copy_description(nw_connection_t) -> UnsafeMutablePointer<CChar>](/documentation/network/nw_connection_copy_description(_:))
- [nw_content_context_t](/documentation/network/nw_content_context_t)

#### Creating Custom Send Contexts

- [func nw_content_context_create(UnsafePointer<CChar>) -> nw_content_context_t](/documentation/network/nw_content_context_create(_:))
- [func nw_content_context_set_metadata_for_protocol(nw_content_context_t, nw_protocol_metadata_t)](/documentation/network/nw_content_context_set_metadata_for_protocol(_:_:))
- [nw_protocol_metadata_t](/documentation/network/nw_protocol_metadata_t)

##### Inspecting Metadata

- [func nw_protocol_metadata_copy_definition(nw_protocol_metadata_t) -> nw_protocol_definition_t](/documentation/network/nw_protocol_metadata_copy_definition(_:))
- [func nw_content_context_set_antecedent(nw_content_context_t, nw_content_context_t?)](/documentation/network/nw_content_context_set_antecedent(_:_:))
- [func nw_content_context_copy_antecedent(nw_content_context_t) -> nw_content_context_t?](/documentation/network/nw_content_context_copy_antecedent(_:))
- [func nw_content_context_set_expiration_milliseconds(nw_content_context_t, UInt64)](/documentation/network/nw_content_context_set_expiration_milliseconds(_:_:))
- [func nw_content_context_get_expiration_milliseconds(nw_content_context_t) -> UInt64](/documentation/network/nw_content_context_get_expiration_milliseconds(_:))
- [func nw_content_context_set_relative_priority(nw_content_context_t, Double)](/documentation/network/nw_content_context_set_relative_priority(_:_:))
- [func nw_content_context_get_relative_priority(nw_content_context_t) -> Double](/documentation/network/nw_content_context_get_relative_priority(_:))
- [func nw_content_context_set_is_final(nw_content_context_t, Bool)](/documentation/network/nw_content_context_set_is_final(_:_:))
- [func nw_content_context_get_identifier(nw_content_context_t) -> UnsafePointer<CChar>](/documentation/network/nw_content_context_get_identifier(_:))

#### Inspecting Receive Contexts

- [func nw_content_context_get_is_final(nw_content_context_t) -> Bool](/documentation/network/nw_content_context_get_is_final(_:))
- [func nw_content_context_copy_protocol_metadata(nw_content_context_t, nw_protocol_definition_t) -> nw_protocol_metadata_t?](/documentation/network/nw_content_context_copy_protocol_metadata(_:_:))
- [func nw_content_context_foreach_protocol_metadata(nw_content_context_t, (nw_protocol_definition_t, nw_protocol_metadata_t) -> Void)](/documentation/network/nw_content_context_foreach_protocol_metadata(_:_:))
- [nw_data_transfer_report_collect_block_t](/documentation/network/nw_data_transfer_report_collect_block_t)
- [nw_data_transfer_report_t](/documentation/network/nw_data_transfer_report_t)

#### Collecting Reports

- [func nw_data_transfer_report_collect(nw_data_transfer_report_t, dispatch_queue_t, nw_data_transfer_report_collect_block_t)](/documentation/network/nw_data_transfer_report_collect(_:_:_:))
- [nw_data_transfer_report_collect_block_t](/documentation/network/nw_data_transfer_report_collect_block_t)
- [func nw_data_transfer_report_get_state(nw_data_transfer_report_t) -> nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_get_state(_:))
- [nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_t)

##### Report States

- [var nw_data_transfer_report_state_collecting: nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_collecting)
- [var nw_data_transfer_report_state_collected: nw_data_transfer_report_state_t](/documentation/network/nw_data_transfer_report_state_collected)

##### Initializers

- [init(UInt32)](/documentation/network/nw_data_transfer_report_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_data_transfer_report_state_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_data_transfer_report_state_t/rawvalue)

#### Identifying Paths

- [func nw_data_transfer_report_get_path_count(nw_data_transfer_report_t) -> UInt32](/documentation/network/nw_data_transfer_report_get_path_count(_:))
- [func nw_data_transfer_report_get_duration_milliseconds(nw_data_transfer_report_t) -> UInt64](/documentation/network/nw_data_transfer_report_get_duration_milliseconds(_:))
- [func nw_data_transfer_report_copy_path_interface(nw_data_transfer_report_t, UInt32) -> nw_interface_t](/documentation/network/nw_data_transfer_report_copy_path_interface(_:_:))

#### Inspecting Application Metrics

- [func nw_data_transfer_report_get_received_application_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_application_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_application_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_application_byte_count(_:_:))

#### Inspecting Transport Metrics

- [func nw_data_transfer_report_get_received_transport_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_byte_count(_:_:))
- [func nw_data_transfer_report_get_received_transport_duplicate_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_duplicate_byte_count(_:_:))
- [func nw_data_transfer_report_get_received_transport_out_of_order_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_transport_out_of_order_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_transport_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_transport_byte_count(_:_:))
- [func nw_data_transfer_report_get_sent_transport_retransmitted_byte_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_transport_retransmitted_byte_count(_:_:))
- [func nw_data_transfer_report_get_transport_smoothed_rtt_milliseconds(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_smoothed_rtt_milliseconds(_:_:))
- [func nw_data_transfer_report_get_transport_minimum_rtt_milliseconds(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_minimum_rtt_milliseconds(_:_:))
- [func nw_data_transfer_report_get_transport_rtt_variance(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_transport_rtt_variance(_:_:))

#### Inspecting Packet Metrics

- [func nw_data_transfer_report_get_received_ip_packet_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_received_ip_packet_count(_:_:))
- [func nw_data_transfer_report_get_sent_ip_packet_count(nw_data_transfer_report_t, UInt32) -> UInt64](/documentation/network/nw_data_transfer_report_get_sent_ip_packet_count(_:_:))
- [nw_endpoint_t](/documentation/network/nw_endpoint_t)

#### Endpoint Types

- [nw_endpoint_type_t](/documentation/network/nw_endpoint_type_t)

##### Endpoint Types

- [var nw_endpoint_type_invalid: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_invalid)
- [var nw_endpoint_type_address: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_address)
- [var nw_endpoint_type_host: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_host)
- [var nw_endpoint_type_bonjour_service: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_bonjour_service)
- [var nw_endpoint_type_url: nw_endpoint_type_t](/documentation/network/nw_endpoint_type_url)

##### Initializers

- [init(UInt32)](/documentation/network/nw_endpoint_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_endpoint_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_endpoint_type_t/rawvalue)
- [func nw_endpoint_get_type(nw_endpoint_t) -> nw_endpoint_type_t](/documentation/network/nw_endpoint_get_type(_:))

#### Host Endpoints

- [func nw_endpoint_create_host(UnsafePointer<CChar>, UnsafePointer<CChar>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_host(_:_:))
- [func nw_endpoint_get_hostname(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_hostname(_:))
- [func nw_endpoint_get_port(nw_endpoint_t) -> UInt16](/documentation/network/nw_endpoint_get_port(_:))
- [func nw_endpoint_copy_port_string(nw_endpoint_t) -> UnsafeMutablePointer<CChar>](/documentation/network/nw_endpoint_copy_port_string(_:))

#### Address Endpoints

- [func nw_endpoint_create_address(UnsafePointer<sockaddr>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_address(_:))
- [func nw_endpoint_get_address(nw_endpoint_t) -> UnsafePointer<sockaddr>](/documentation/network/nw_endpoint_get_address(_:))
- [func nw_endpoint_copy_address_string(nw_endpoint_t) -> UnsafeMutablePointer<CChar>](/documentation/network/nw_endpoint_copy_address_string(_:))
- [func nw_endpoint_copy_port_string(nw_endpoint_t) -> UnsafeMutablePointer<CChar>](/documentation/network/nw_endpoint_copy_port_string(_:))

#### Bonjour Service Endpoints

- [func nw_endpoint_create_bonjour_service(UnsafePointer<CChar>, UnsafePointer<CChar>, UnsafePointer<CChar>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_bonjour_service(_:_:_:))
- [func nw_endpoint_get_bonjour_service_name(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_bonjour_service_name(_:))
- [func nw_endpoint_get_bonjour_service_type(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_bonjour_service_type(_:))
- [func nw_endpoint_get_bonjour_service_domain(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_bonjour_service_domain(_:))

#### URL Endpoints

- [func nw_endpoint_create_url(UnsafePointer<CChar>) -> nw_endpoint_t](/documentation/network/nw_endpoint_create_url(_:))
- [func nw_endpoint_get_url(nw_endpoint_t) -> UnsafePointer<CChar>](/documentation/network/nw_endpoint_get_url(_:))
- [nw_error_t](/documentation/network/nw_error_t)

#### Inspecting Errors

- [func nw_error_get_error_domain(nw_error_t) -> nw_error_domain_t](/documentation/network/nw_error_get_error_domain(_:))
- [nw_error_domain_t](/documentation/network/nw_error_domain_t)

##### Error Domain Constants

- [var nw_error_domain_invalid: nw_error_domain_t](/documentation/network/nw_error_domain_invalid)
- [var nw_error_domain_posix: nw_error_domain_t](/documentation/network/nw_error_domain_posix)
- [var nw_error_domain_dns: nw_error_domain_t](/documentation/network/nw_error_domain_dns)
- [var nw_error_domain_tls: nw_error_domain_t](/documentation/network/nw_error_domain_tls)

##### CFError Domain Constants

- [let kNWErrorDomainPOSIX: CFString](/documentation/network/knwerrordomainposix)
- [let kNWErrorDomainDNS: CFString](/documentation/network/knwerrordomaindns)
- [let kNWErrorDomainTLS: CFString](/documentation/network/knwerrordomaintls)

##### Initializers

- [init(UInt32)](/documentation/network/nw_error_domain_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_error_domain_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_error_domain_t/rawvalue)
- [func nw_error_get_error_code(nw_error_t) -> Int32](/documentation/network/nw_error_get_error_code(_:))
- [func nw_error_copy_cf_error(nw_error_t) -> Unmanaged<CFError>](/documentation/network/nw_error_copy_cf_error(_:))
- [nw_establishment_report_access_block_t](/documentation/network/nw_establishment_report_access_block_t)
- [nw_establishment_report_t](/documentation/network/nw_establishment_report_t)

#### Inspecting Connection Attempts

- [func nw_establishment_report_get_duration_milliseconds(nw_establishment_report_t) -> UInt64](/documentation/network/nw_establishment_report_get_duration_milliseconds(_:))
- [func nw_establishment_report_get_previous_attempt_count(nw_establishment_report_t) -> UInt32](/documentation/network/nw_establishment_report_get_previous_attempt_count(_:))
- [func nw_establishment_report_get_attempt_started_after_milliseconds(nw_establishment_report_t) -> UInt64](/documentation/network/nw_establishment_report_get_attempt_started_after_milliseconds(_:))

#### Inspecting Resolution

- [func nw_establishment_report_enumerate_resolution_reports(nw_establishment_report_t, (nw_resolution_report_t) -> Bool)](/documentation/network/nw_establishment_report_enumerate_resolution_reports(_:_:))
- [nw_report_resolution_report_enumerator_t](/documentation/network/nw_report_resolution_report_enumerator_t)
- [nw_resolution_report_t](/documentation/network/nw_resolution_report_t)
- [func nw_resolution_report_get_milliseconds(nw_resolution_report_t) -> UInt64](/documentation/network/nw_resolution_report_get_milliseconds(_:))
- [func nw_resolution_report_get_source(nw_resolution_report_t) -> nw_report_resolution_source_t](/documentation/network/nw_resolution_report_get_source(_:))
- [nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_t)

##### Resolution Sources

- [var nw_report_resolution_source_query: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_query)
- [var nw_report_resolution_source_cache: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_cache)
- [var nw_report_resolution_source_expired_cache: nw_report_resolution_source_t](/documentation/network/nw_report_resolution_source_expired_cache)

##### Initializers

- [init(UInt32)](/documentation/network/nw_report_resolution_source_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_report_resolution_source_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_report_resolution_source_t/rawvalue)
- [func nw_resolution_report_get_protocol(nw_resolution_report_t) -> nw_report_resolution_protocol_t](/documentation/network/nw_resolution_report_get_protocol(_:))
- [nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_t)

##### Resolution Transports

- [var nw_report_resolution_protocol_unknown: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_unknown)
- [var nw_report_resolution_protocol_udp: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_udp)
- [var nw_report_resolution_protocol_tcp: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_tcp)
- [var nw_report_resolution_protocol_tls: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_tls)
- [var nw_report_resolution_protocol_https: nw_report_resolution_protocol_t](/documentation/network/nw_report_resolution_protocol_https)

##### Initializers

- [init(UInt32)](/documentation/network/nw_report_resolution_protocol_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_report_resolution_protocol_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_report_resolution_protocol_t/rawvalue)
- [func nw_resolution_report_copy_successful_endpoint(nw_resolution_report_t) -> nw_endpoint_t](/documentation/network/nw_resolution_report_copy_successful_endpoint(_:))
- [func nw_resolution_report_copy_preferred_endpoint(nw_resolution_report_t) -> nw_endpoint_t](/documentation/network/nw_resolution_report_copy_preferred_endpoint(_:))
- [func nw_resolution_report_get_endpoint_count(nw_resolution_report_t) -> UInt32](/documentation/network/nw_resolution_report_get_endpoint_count(_:))
- [func nw_establishment_report_enumerate_resolutions(nw_establishment_report_t, (nw_report_resolution_source_t, UInt64, UInt32, nw_endpoint_t, nw_endpoint_t) -> Bool)](/documentation/network/nw_establishment_report_enumerate_resolutions(_:_:))
- [nw_report_resolution_enumerator_t](/documentation/network/nw_report_resolution_enumerator_t)

#### Inspecting Protocol Handshakes

- [func nw_establishment_report_enumerate_protocols(nw_establishment_report_t, (nw_protocol_definition_t, UInt64, UInt64) -> Bool)](/documentation/network/nw_establishment_report_enumerate_protocols(_:_:))
- [nw_report_protocol_enumerator_t](/documentation/network/nw_report_protocol_enumerator_t)

#### Checking for Proxies

- [func nw_establishment_report_get_proxy_configured(nw_establishment_report_t) -> Bool](/documentation/network/nw_establishment_report_get_proxy_configured(_:))
- [func nw_establishment_report_get_used_proxy(nw_establishment_report_t) -> Bool](/documentation/network/nw_establishment_report_get_used_proxy(_:))
- [func nw_establishment_report_copy_proxy_endpoint(nw_establishment_report_t) -> nw_endpoint_t?](/documentation/network/nw_establishment_report_copy_proxy_endpoint(_:))
- [nw_ethernet_address_t](/documentation/network/nw_ethernet_address_t)
- [nw_ethernet_channel_receive_handler_t](/documentation/network/nw_ethernet_channel_receive_handler_t)
- [nw_ethernet_channel_send_completion_t](/documentation/network/nw_ethernet_channel_send_completion_t)
- [nw_ethernet_channel_state_changed_handler_t](/documentation/network/nw_ethernet_channel_state_changed_handler_t)
- [nw_ethernet_channel_t](/documentation/network/nw_ethernet_channel_t)

#### Managing Ethernet Channels

- [func nw_ethernet_channel_create(UInt16, nw_interface_t) -> nw_ethernet_channel_t](/documentation/network/nw_ethernet_channel_create(_:_:))
- [func nw_ethernet_channel_set_queue(nw_ethernet_channel_t, dispatch_queue_t)](/documentation/network/nw_ethernet_channel_set_queue(_:_:))
- [func nw_ethernet_channel_start(nw_ethernet_channel_t)](/documentation/network/nw_ethernet_channel_start(_:))
- [func nw_ethernet_channel_cancel(nw_ethernet_channel_t)](/documentation/network/nw_ethernet_channel_cancel(_:))

#### Handling State Updates

- [func nw_ethernet_channel_set_state_changed_handler(nw_ethernet_channel_t, nw_ethernet_channel_state_changed_handler_t?)](/documentation/network/nw_ethernet_channel_set_state_changed_handler(_:_:))
- [nw_ethernet_channel_state_changed_handler_t](/documentation/network/nw_ethernet_channel_state_changed_handler_t)
- [nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_t)

##### States

- [var nw_ethernet_channel_state_invalid: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_invalid)
- [var nw_ethernet_channel_state_waiting: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_waiting)
- [var nw_ethernet_channel_state_preparing: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_preparing)
- [var nw_ethernet_channel_state_ready: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_ready)
- [var nw_ethernet_channel_state_failed: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_failed)
- [var nw_ethernet_channel_state_cancelled: nw_ethernet_channel_state_t](/documentation/network/nw_ethernet_channel_state_cancelled)

##### Initializers

- [init(UInt32)](/documentation/network/nw_ethernet_channel_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_ethernet_channel_state_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_ethernet_channel_state_t/rawvalue)

#### Sending and Receiving Ethernet Frames

- [func nw_ethernet_channel_send(nw_ethernet_channel_t, dispatch_data_t, UInt16, UnsafeMutablePointer<UInt8>, nw_ethernet_channel_send_completion_t)](/documentation/network/nw_ethernet_channel_send(_:_:_:_:_:))
- [nw_ethernet_channel_send_completion_t](/documentation/network/nw_ethernet_channel_send_completion_t)
- [func nw_ethernet_channel_set_receive_handler(nw_ethernet_channel_t, nw_ethernet_channel_receive_handler_t?)](/documentation/network/nw_ethernet_channel_set_receive_handler(_:_:))
- [nw_ethernet_channel_receive_handler_t](/documentation/network/nw_ethernet_channel_receive_handler_t)
- [nw_ethernet_address_t](/documentation/network/nw_ethernet_address_t)
- [nw_framer_block_t](/documentation/network/nw_framer_block_t)
- [nw_framer_cleanup_handler_t](/documentation/network/nw_framer_cleanup_handler_t)
- [nw_framer_input_handler_t](/documentation/network/nw_framer_input_handler_t)
- [nw_framer_message_dispose_value_t](/documentation/network/nw_framer_message_dispose_value_t)
- [nw_framer_message_t](/documentation/network/nw_framer_message_t)
- [nw_framer_output_handler_t](/documentation/network/nw_framer_output_handler_t)
- [nw_framer_parse_completion_t](/documentation/network/nw_framer_parse_completion_t)
- [nw_framer_start_handler_t](/documentation/network/nw_framer_start_handler_t)
- [nw_framer_stop_handler_t](/documentation/network/nw_framer_stop_handler_t)
- [nw_framer_t](/documentation/network/nw_framer_t)
- [nw_framer_wakeup_handler_t](/documentation/network/nw_framer_wakeup_handler_t)
- [nw_group_descriptor_enumerate_endpoints_block_t](/documentation/network/nw_group_descriptor_enumerate_endpoints_block_t)
- [nw_group_descriptor_t](/documentation/network/nw_group_descriptor_t)
- [nw_interface_t](/documentation/network/nw_interface_t)

#### Network Interface Types

- [nw_interface_type_t](/documentation/network/nw_interface_type_t)

##### Creating an interface type instance

- [init(UInt32)](/documentation/network/nw_interface_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_interface_type_t/init(rawvalue:))

##### Interface types

- [var nw_interface_type_wifi: nw_interface_type_t](/documentation/network/nw_interface_type_wifi)
- [var nw_interface_type_cellular: nw_interface_type_t](/documentation/network/nw_interface_type_cellular)
- [var nw_interface_type_wired: nw_interface_type_t](/documentation/network/nw_interface_type_wired)
- [var nw_interface_type_loopback: nw_interface_type_t](/documentation/network/nw_interface_type_loopback)
- [var nw_interface_type_other: nw_interface_type_t](/documentation/network/nw_interface_type_other)

##### Accessing the raw value

- [var rawValue: UInt32](/documentation/network/nw_interface_type_t/rawvalue)

#### Inspecting Interfaces

- [func nw_interface_get_type(nw_interface_t) -> nw_interface_type_t](/documentation/network/nw_interface_get_type(_:))
- [func nw_interface_get_name(nw_interface_t) -> UnsafePointer<CChar>](/documentation/network/nw_interface_get_name(_:))
- [func nw_interface_get_index(nw_interface_t) -> UInt32](/documentation/network/nw_interface_get_index(_:))
- [nw_listener_advertised_endpoint_changed_handler_t](/documentation/network/nw_listener_advertised_endpoint_changed_handler_t)
- [nw_listener_new_connection_group_handler_t](/documentation/network/nw_listener_new_connection_group_handler_t)
- [nw_listener_new_connection_handler_t](/documentation/network/nw_listener_new_connection_handler_t)
- [nw_listener_state_changed_handler_t](/documentation/network/nw_listener_state_changed_handler_t)
- [nw_listener_t](/documentation/network/nw_listener_t)

#### Creating Listeners

- [func nw_listener_create(nw_parameters_t) -> nw_listener_t?](/documentation/network/nw_listener_create(_:))
- [func nw_listener_create_with_port(UnsafePointer<CChar>, nw_parameters_t) -> nw_listener_t?](/documentation/network/nw_listener_create_with_port(_:_:))
- [func nw_listener_create_with_connection(nw_connection_t, nw_parameters_t) -> nw_listener_t?](/documentation/network/nw_listener_create_with_connection(_:_:))
- [func nw_listener_set_queue(nw_listener_t, dispatch_queue_t)](/documentation/network/nw_listener_set_queue(_:_:))
- [func nw_listener_start(nw_listener_t)](/documentation/network/nw_listener_start(_:))
- [func nw_listener_get_port(nw_listener_t) -> UInt16](/documentation/network/nw_listener_get_port(_:))
- [func nw_listener_cancel(nw_listener_t)](/documentation/network/nw_listener_cancel(_:))

#### Receiving Connections

- [func nw_listener_set_new_connection_handler(nw_listener_t, nw_listener_new_connection_handler_t?)](/documentation/network/nw_listener_set_new_connection_handler(_:_:))
- [nw_listener_new_connection_handler_t](/documentation/network/nw_listener_new_connection_handler_t)
- [func nw_listener_set_new_connection_limit(nw_listener_t, UInt32)](/documentation/network/nw_listener_set_new_connection_limit(_:_:))
- [func nw_listener_get_new_connection_limit(nw_listener_t) -> UInt32](/documentation/network/nw_listener_get_new_connection_limit(_:))
- [var NW_LISTENER_INFINITE_CONNECTION_LIMIT: UInt32](/documentation/network/nw_listener_infinite_connection_limit)

#### Advertising Bonjour Services

- [NSBonjourServices](/documentation/bundleresources/information-property-list/nsbonjourservices)
- [NSLocalNetworkUsageDescription](/documentation/bundleresources/information-property-list/nslocalnetworkusagedescription)
- [func nw_listener_set_advertise_descriptor(nw_listener_t, nw_advertise_descriptor_t?)](/documentation/network/nw_listener_set_advertise_descriptor(_:_:))
- [nw_advertise_descriptor_t](/documentation/network/nw_advertise_descriptor_t)

##### Advertising Bonjour Services

- [func nw_advertise_descriptor_create_bonjour_service(UnsafePointer<CChar>?, UnsafePointer<CChar>, UnsafePointer<CChar>?) -> nw_advertise_descriptor_t?](/documentation/network/nw_advertise_descriptor_create_bonjour_service(_:_:_:))
- [func nw_advertise_descriptor_set_no_auto_rename(nw_advertise_descriptor_t, Bool)](/documentation/network/nw_advertise_descriptor_set_no_auto_rename(_:_:))
- [func nw_advertise_descriptor_get_no_auto_rename(nw_advertise_descriptor_t) -> Bool](/documentation/network/nw_advertise_descriptor_get_no_auto_rename(_:))

##### Configuring TXT Records

- [func nw_advertise_descriptor_set_txt_record(nw_advertise_descriptor_t, UnsafeRawPointer?, Int)](/documentation/network/nw_advertise_descriptor_set_txt_record(_:_:_:))
- [func nw_advertise_descriptor_set_txt_record_object(nw_advertise_descriptor_t, nw_txt_record_t?)](/documentation/network/nw_advertise_descriptor_set_txt_record_object(_:_:))
- [func nw_advertise_descriptor_copy_txt_record_object(nw_advertise_descriptor_t) -> nw_txt_record_t?](/documentation/network/nw_advertise_descriptor_copy_txt_record_object(_:))
- [func nw_listener_set_advertised_endpoint_changed_handler(nw_listener_t, nw_listener_advertised_endpoint_changed_handler_t?)](/documentation/network/nw_listener_set_advertised_endpoint_changed_handler(_:_:))
- [nw_listener_advertised_endpoint_changed_handler_t](/documentation/network/nw_listener_advertised_endpoint_changed_handler_t)

#### Handling State Updates

- [func nw_listener_set_state_changed_handler(nw_listener_t, nw_listener_state_changed_handler_t?)](/documentation/network/nw_listener_set_state_changed_handler(_:_:))
- [nw_listener_state_changed_handler_t](/documentation/network/nw_listener_state_changed_handler_t)
- [nw_listener_state_t](/documentation/network/nw_listener_state_t)

##### Listener States

- [var nw_listener_state_invalid: nw_listener_state_t](/documentation/network/nw_listener_state_invalid)
- [var nw_listener_state_waiting: nw_listener_state_t](/documentation/network/nw_listener_state_waiting)
- [var nw_listener_state_ready: nw_listener_state_t](/documentation/network/nw_listener_state_ready)
- [var nw_listener_state_failed: nw_listener_state_t](/documentation/network/nw_listener_state_failed)
- [var nw_listener_state_cancelled: nw_listener_state_t](/documentation/network/nw_listener_state_cancelled)

##### Initializers

- [init(UInt32)](/documentation/network/nw_listener_state_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_listener_state_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_listener_state_t/rawvalue)
- [nw_object_t](/documentation/network/nw_object_t)
- [nw_path_enumerate_gateways_block_t](/documentation/network/nw_path_enumerate_gateways_block_t)
- [nw_path_enumerate_interfaces_block_t](/documentation/network/nw_path_enumerate_interfaces_block_t)
- [nw_path_monitor_cancel_handler_t](/documentation/network/nw_path_monitor_cancel_handler_t)
- [nw_path_monitor_t](/documentation/network/nw_path_monitor_t)

#### Creating Path Monitors

- [func nw_path_monitor_create() -> nw_path_monitor_t](/documentation/network/nw_path_monitor_create())
- [func nw_path_monitor_create_with_type(nw_interface_type_t) -> nw_path_monitor_t](/documentation/network/nw_path_monitor_create_with_type(_:))
- [func nw_path_monitor_prohibit_interface_type(nw_path_monitor_t, nw_interface_type_t)](/documentation/network/nw_path_monitor_prohibit_interface_type(_:_:))
- [func nw_path_monitor_set_queue(nw_path_monitor_t, dispatch_queue_t)](/documentation/network/nw_path_monitor_set_queue(_:_:))
- [func nw_path_monitor_start(nw_path_monitor_t)](/documentation/network/nw_path_monitor_start(_:))

#### Handling Path Updates

- [func nw_path_monitor_set_update_handler(nw_path_monitor_t, nw_path_monitor_update_handler_t)](/documentation/network/nw_path_monitor_set_update_handler(_:_:))
- [nw_path_monitor_update_handler_t](/documentation/network/nw_path_monitor_update_handler_t)

#### Canceling Path Monitors

- [func nw_path_monitor_cancel(nw_path_monitor_t)](/documentation/network/nw_path_monitor_cancel(_:))
- [func nw_path_monitor_set_cancel_handler(nw_path_monitor_t, nw_path_monitor_cancel_handler_t)](/documentation/network/nw_path_monitor_set_cancel_handler(_:_:))
- [nw_path_monitor_cancel_handler_t](/documentation/network/nw_path_monitor_cancel_handler_t)
- [nw_path_monitor_update_handler_t](/documentation/network/nw_path_monitor_update_handler_t)
- [nw_path_t](/documentation/network/nw_path_t)

#### Checking Path Availability

- [func nw_path_get_status(nw_path_t) -> nw_path_status_t](/documentation/network/nw_path_get_status(_:))
- [nw_path_status_t](/documentation/network/nw_path_status_t)

##### Status Values

- [var nw_path_status_invalid: nw_path_status_t](/documentation/network/nw_path_status_invalid)
- [var nw_path_status_unsatisfied: nw_path_status_t](/documentation/network/nw_path_status_unsatisfied)
- [var nw_path_status_satisfied: nw_path_status_t](/documentation/network/nw_path_status_satisfied)
- [var nw_path_status_satisfiable: nw_path_status_t](/documentation/network/nw_path_status_satisfiable)

##### Initializers

- [init(UInt32)](/documentation/network/nw_path_status_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_path_status_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_path_status_t/rawvalue)

#### Inspecting Interfaces

- [func nw_path_uses_interface_type(nw_path_t, nw_interface_type_t) -> Bool](/documentation/network/nw_path_uses_interface_type(_:_:))
- [func nw_path_enumerate_interfaces(nw_path_t, (nw_interface_t) -> Bool)](/documentation/network/nw_path_enumerate_interfaces(_:_:))
- [nw_path_enumerate_interfaces_block_t](/documentation/network/nw_path_enumerate_interfaces_block_t)
- [func nw_path_enumerate_gateways(nw_path_t, (nw_endpoint_t) -> Bool)](/documentation/network/nw_path_enumerate_gateways(_:_:))
- [nw_path_enumerate_gateways_block_t](/documentation/network/nw_path_enumerate_gateways_block_t)

#### Checking Path Capabilities

- [func nw_path_has_ipv4(nw_path_t) -> Bool](/documentation/network/nw_path_has_ipv4(_:))
- [func nw_path_has_ipv6(nw_path_t) -> Bool](/documentation/network/nw_path_has_ipv6(_:))
- [func nw_path_has_dns(nw_path_t) -> Bool](/documentation/network/nw_path_has_dns(_:))
- [func nw_path_is_constrained(nw_path_t) -> Bool](/documentation/network/nw_path_is_constrained(_:))
- [func nw_path_is_expensive(nw_path_t) -> Bool](/documentation/network/nw_path_is_expensive(_:))

#### Comparing Paths

- [func nw_path_is_equal(nw_path_t, nw_path_t) -> Bool](/documentation/network/nw_path_is_equal(_:_:))

#### Inspecting Connected Paths

- [func nw_path_copy_effective_local_endpoint(nw_path_t) -> nw_endpoint_t?](/documentation/network/nw_path_copy_effective_local_endpoint(_:))
- [func nw_path_copy_effective_remote_endpoint(nw_path_t) -> nw_endpoint_t?](/documentation/network/nw_path_copy_effective_remote_endpoint(_:))
- [nw_protocol_metadata_t](/documentation/network/nw_protocol_metadata_t)

#### Inspecting Metadata

- [func nw_protocol_metadata_copy_definition(nw_protocol_metadata_t) -> nw_protocol_definition_t](/documentation/network/nw_protocol_metadata_copy_definition(_:))
- [nw_proxy_domain_enumerator_t](/documentation/network/nw_proxy_domain_enumerator_t)
- [nw_report_protocol_enumerator_t](/documentation/network/nw_report_protocol_enumerator_t)
- [nw_report_resolution_enumerator_t](/documentation/network/nw_report_resolution_enumerator_t)
- [nw_report_resolution_report_enumerator_t](/documentation/network/nw_report_resolution_report_enumerator_t)
- [nw_resolution_report_t](/documentation/network/nw_resolution_report_t)
- [nw_txt_record_access_bytes_t](/documentation/network/nw_txt_record_access_bytes_t)
- [nw_txt_record_access_key_t](/documentation/network/nw_txt_record_access_key_t)
- [nw_txt_record_applier_t](/documentation/network/nw_txt_record_applier_t)
- [nw_txt_record_t](/documentation/network/nw_txt_record_t)

#### Creating TXT Records

- [func nw_txt_record_create_dictionary() -> nw_txt_record_t](/documentation/network/nw_txt_record_create_dictionary())
- [func nw_txt_record_create_with_bytes(UnsafePointer<UInt8>, Int) -> nw_txt_record_t](/documentation/network/nw_txt_record_create_with_bytes(_:_:))
- [func nw_txt_record_copy(nw_txt_record_t?) -> nw_txt_record_t?](/documentation/network/nw_txt_record_copy(_:))
- [func nw_txt_record_set_key(nw_txt_record_t, UnsafePointer<CChar>, UnsafePointer<UInt8>?, Int) -> Bool](/documentation/network/nw_txt_record_set_key(_:_:_:_:))
- [func nw_txt_record_remove_key(nw_txt_record_t, UnsafePointer<CChar>) -> Bool](/documentation/network/nw_txt_record_remove_key(_:_:))

#### Examining TXT Records

- [func nw_txt_record_is_dictionary(nw_txt_record_t) -> Bool](/documentation/network/nw_txt_record_is_dictionary(_:))
- [func nw_txt_record_get_key_count(nw_txt_record_t?) -> Int](/documentation/network/nw_txt_record_get_key_count(_:))
- [func nw_txt_record_apply(nw_txt_record_t, nw_txt_record_applier_t) -> Bool](/documentation/network/nw_txt_record_apply(_:_:))
- [nw_txt_record_applier_t](/documentation/network/nw_txt_record_applier_t)
- [func nw_txt_record_access_key(nw_txt_record_t, UnsafePointer<CChar>, nw_txt_record_access_key_t) -> Bool](/documentation/network/nw_txt_record_access_key(_:_:_:))
- [nw_txt_record_access_key_t](/documentation/network/nw_txt_record_access_key_t)
- [func nw_txt_record_find_key(nw_txt_record_t, UnsafePointer<CChar>) -> nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key(_:_:))
- [nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_t)

##### Key Value Status

- [var nw_txt_record_find_key_invalid: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_invalid)
- [var nw_txt_record_find_key_not_present: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_not_present)
- [var nw_txt_record_find_key_no_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_no_value)
- [var nw_txt_record_find_key_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_empty_value)
- [var nw_txt_record_find_key_non_empty_value: nw_txt_record_find_key_t](/documentation/network/nw_txt_record_find_key_non_empty_value)

##### Initializers

- [init(UInt32)](/documentation/network/nw_txt_record_find_key_t/init(_:))
- [init(rawValue: UInt32)](/documentation/network/nw_txt_record_find_key_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/network/nw_txt_record_find_key_t/rawvalue)
- [func nw_txt_record_is_equal(nw_txt_record_t?, nw_txt_record_t?) -> Bool](/documentation/network/nw_txt_record_is_equal(_:_:))
- [func nw_txt_record_access_bytes(nw_txt_record_t, nw_txt_record_access_bytes_t) -> Bool](/documentation/network/nw_txt_record_access_bytes(_:_:))
- [nw_txt_record_access_bytes_t](/documentation/network/nw_txt_record_access_bytes_t)
- [nw_ws_additional_header_enumerator_t](/documentation/network/nw_ws_additional_header_enumerator_t)
- [nw_ws_client_request_handler_t](/documentation/network/nw_ws_client_request_handler_t)
- [nw_ws_pong_handler_t](/documentation/network/nw_ws_pong_handler_t)
- [nw_ws_request_t](/documentation/network/nw_ws_request_t)
- [nw_ws_response_t](/documentation/network/nw_ws_response_t)
- [nw_ws_subprotocol_enumerator_t](/documentation/network/nw_ws_subprotocol_enumerator_t)

## Protocols

- [BrowserProvider](/documentation/network/browserprovider)

### Associated Types

- [Endpoint](/documentation/network/browserprovider/endpoint)

### Type Methods

- [static func bonjour(String, domain: String?, includeTxtRecord: Bool) -> Bonjour](/documentation/network/browserprovider/bonjour(_:domain:includetxtrecord:))
- [static func wifiAware(WASubscriberBrowser.Action, active: Duration?) -> Self](/documentation/network/browserprovider/wifiaware(_:active:))
- [Connectable](/documentation/network/connectable)
- [ConnectionStorage](/documentation/network/connectionstorage)

### Initializers

- [init()](/documentation/network/connectionstorage/init())
- [DatagramProtocol](/documentation/network/datagramprotocol)
- [FramerProtocol](/documentation/network/framerprotocol)

### Type Properties

- [static var definition: NWProtocolFramer.Definition](/documentation/network/framerprotocol/definition)
- [ListenerProvider](/documentation/network/listenerprovider)

### Instance Properties

- [var service: NWListener.Service](/documentation/network/listenerprovider/service)

### Type Methods

- [static func bonjour(name: String?, type: String, domain: String?, txtRecord: NWTXTRecord?) -> BonjourListenerProvider](/documentation/network/listenerprovider/bonjour(name:type:domain:txtrecord:))
- [static func wifiAware(WAPublisherListener.Action, active: Duration?) -> Self](/documentation/network/listenerprovider/wifiaware(_:active:))
- [MessageProtocol](/documentation/network/messageprotocol)

### Associated Types

- [ContentType](/documentation/network/messageprotocol/contenttype)
- [LegacyMessage](/documentation/network/messageprotocol/legacymessage)
- [MultiplexProtocol](/documentation/network/multiplexprotocol)
- [NWParametersProvider](/documentation/network/nwparametersprovider)

### Instance Properties

- [var parameters: NWParameters](/documentation/network/nwparametersprovider/parameters)

### Instance Methods

- [func constrainedPathsProhibited(Bool) -> Self](/documentation/network/nwparametersprovider/constrainedpathsprohibited(_:))
- [func dnssecValidationRequired(Bool) -> Self](/documentation/network/nwparametersprovider/dnssecvalidationrequired(_:))
- [func expensivePathsProhibited(Bool) -> Self](/documentation/network/nwparametersprovider/expensivepathsprohibited(_:))
- [func expiredDNSBehavior(NWParameters.ExpiredDNSBehavior) -> Self](/documentation/network/nwparametersprovider/expireddnsbehavior(_:))
- [func fastOpenAllowed(Bool) -> Self](/documentation/network/nwparametersprovider/fastopenallowed(_:))
- [func localEndpoint(NWEndpoint?) -> Self](/documentation/network/nwparametersprovider/localendpoint(_:))
- [func localEndpointReuseAllowed(Bool) -> Self](/documentation/network/nwparametersprovider/localendpointreuseallowed(_:))
- [func localOnly(Bool) -> Self](/documentation/network/nwparametersprovider/localonly(_:))
- [func localPort(NWEndpoint.Port) -> Self](/documentation/network/nwparametersprovider/localport(_:))
- [func multipathServiceType(NWParameters.MultipathServiceType) -> Self](/documentation/network/nwparametersprovider/multipathservicetype(_:))
- [func noProxiesPreferred(Bool) -> Self](/documentation/network/nwparametersprovider/noproxiespreferred(_:))
- [func peerToPeerIncluded(Bool) -> Self](/documentation/network/nwparametersprovider/peertopeerincluded(_:))
- [func prohibitedInterfaceTypes([NWInterface.InterfaceType]) -> Self](/documentation/network/nwparametersprovider/prohibitedinterfacetypes(_:))
- [func prohibitedInterfaces([NWInterface]) -> Self](/documentation/network/nwparametersprovider/prohibitedinterfaces(_:))
- [func requiredInterface(NWInterface) -> Self](/documentation/network/nwparametersprovider/requiredinterface(_:))
- [func requiredInterfaceType(NWInterface.InterfaceType) -> Self](/documentation/network/nwparametersprovider/requiredinterfacetype(_:))
- [func serviceClass(NWParameters.ServiceClass) -> Self](/documentation/network/nwparametersprovider/serviceclass(_:))
- [func ultraConstrainedPathsAllowed(Bool) -> Self](/documentation/network/nwparametersprovider/ultraconstrainedpathsallowed(_:))
- [NetworkCoder](/documentation/network/networkcoder)

### Associated Types

- [Decoder](/documentation/network/networkcoder/decoder)
- [Encoder](/documentation/network/networkcoder/encoder)

### Initializers

- [init()](/documentation/network/networkcoder/init())

### Instance Methods

- [func makeDecoder() -> Self.Decoder](/documentation/network/networkcoder/makedecoder())
- [func makeEncoder() -> Self.Encoder](/documentation/network/networkcoder/makeencoder())

### Type Properties

- [static var json: NetworkJSONCoder](/documentation/network/networkcoder/json)
- [static var propertyList: NetworkPropertyListCoder](/documentation/network/networkcoder/propertylist)
- [NetworkDecoder](/documentation/network/networkdecoder)

### Instance Methods

- [func decode<T>(T.Type, from: Data) throws -> T](/documentation/network/networkdecoder/decode(_:from:))
- [NetworkEncoder](/documentation/network/networkencoder)

### Instance Methods

- [func encode<T>(T) throws -> Data](/documentation/network/networkencoder/encode(_:))
- [NetworkFixedWidthInteger](/documentation/network/networkfixedwidthinteger)

### Initializers

- [init(bigEndian: Self)](/documentation/network/networkfixedwidthinteger/init(bigendian:))

### Instance Properties

- [var bigEndian: Self](/documentation/network/networkfixedwidthinteger/bigendian)
- [NetworkMetadataProtocol](/documentation/network/networkmetadataprotocol)
- [NetworkProtocolOptions](/documentation/network/networkprotocoloptions)

### Associated Types

- [BelowProtocol](/documentation/network/networkprotocoloptions/belowprotocol)
- [Metadata](/documentation/network/networkprotocoloptions/metadata)
- [ProtocolStorage](/documentation/network/networkprotocoloptions/protocolstorage)

### Type Aliases

- [NetworkProtocolOptions.Message](/documentation/network/networkprotocoloptions/message)
- [OneToOneProtocol](/documentation/network/onetooneprotocol)
- [StreamProtocol](/documentation/network/streamprotocol)

## Variables

- [let kNWErrorDomainWiFiAware: CFString](/documentation/network/knwerrordomainwifiaware)
- [var nw_error_domain_wifi_aware: nw_error_domain_t](/documentation/network/nw_error_domain_wifi_aware)
- [var nw_link_quality_good: nw_link_quality_t](/documentation/network/nw_link_quality_good)
- [var nw_link_quality_minimal: nw_link_quality_t](/documentation/network/nw_link_quality_minimal)
- [var nw_link_quality_moderate: nw_link_quality_t](/documentation/network/nw_link_quality_moderate)
- [var nw_link_quality_unknown: nw_link_quality_t](/documentation/network/nw_link_quality_unknown)

## Functions

- [func nw_parameters_get_allow_ultra_constrained(nw_parameters_t) -> Bool](/documentation/network/nw_parameters_get_allow_ultra_constrained(_:))
- [func nw_parameters_set_allow_ultra_constrained(nw_parameters_t, Bool)](/documentation/network/nw_parameters_set_allow_ultra_constrained(_:_:))
- [func nw_path_get_link_quality(nw_path_t) -> nw_link_quality_t](/documentation/network/nw_path_get_link_quality(_:))
- [func nw_path_is_ultra_constrained(nw_path_t) -> Bool](/documentation/network/nw_path_is_ultra_constrained(_:))
- [func withNetworkConnection<ApplicationProtocol>(to: NWEndpoint, using: () -> ApplicationProtocol, (NetworkConnection<ApplicationProtocol>) async throws -> Void) async throws](/documentation/network/withnetworkconnection(to:using:_:)-1sik8)
- [func withNetworkConnection<ApplicationProtocol>(to: NWEndpoint, using: () -> ApplicationProtocol, (NetworkConnection<ApplicationProtocol>) async throws -> Void) async throws](/documentation/network/withnetworkconnection(to:using:_:)-4wpc9)
- [func withNetworkConnection<ApplicationProtocol>(to: NWEndpoint, using: NWParametersBuilder<ApplicationProtocol>, (NetworkConnection<ApplicationProtocol>) async throws -> Void) async throws](/documentation/network/withnetworkconnection(to:using:_:)-7skhi)
- [func withNetworkConnection<ApplicationProtocol>(to: NWEndpoint, using: NWParametersBuilder<ApplicationProtocol>, (NetworkConnection<ApplicationProtocol>) async throws -> Void) async throws](/documentation/network/withnetworkconnection(to:using:_:)-887ho)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
