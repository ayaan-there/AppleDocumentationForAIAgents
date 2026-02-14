# Network Extension Documentation

Source: https://sosumi.ai/documentation/networkextension

---
title: Network Extension
source: https://developer.apple.com/documentation/networkextension
timestamp: 2026-02-13T19:00:02.111Z
---

## Wi-Fi management

- [Wi-Fi configuration](/documentation/networkextension/wi-fi-configuration)

### Essentials

- [Hotspot Configuration Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.hotspotconfiguration)

### Wi-Fi network configuration

- [NEHotspotConfigurationManager](/documentation/networkextension/nehotspotconfigurationmanager)

#### Creating configurations

- [class var shared: NEHotspotConfigurationManager](/documentation/networkextension/nehotspotconfigurationmanager/shared)
- [func apply(NEHotspotConfiguration, completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nehotspotconfigurationmanager/apply(_:completionhandler:))

#### Getting a list of configurations

- [func getConfiguredSSIDs(completionHandler: ([String]) -> Void)](/documentation/networkextension/nehotspotconfigurationmanager/getconfiguredssids(completionhandler:))

#### Removing configuration

- [func removeConfiguration(forHS20DomainName: String)](/documentation/networkextension/nehotspotconfigurationmanager/removeconfiguration(forhs20domainname:))
- [func removeConfiguration(forSSID: String)](/documentation/networkextension/nehotspotconfigurationmanager/removeconfiguration(forssid:))

#### Errors

- [let NEHotspotConfigurationErrorDomain: String](/documentation/networkextension/nehotspotconfigurationerrordomain)
- [NEHotspotConfigurationError](/documentation/networkextension/nehotspotconfigurationerror)

##### Errors

- [case invalid](/documentation/networkextension/nehotspotconfigurationerror/invalid)
- [case invalidSSID](/documentation/networkextension/nehotspotconfigurationerror/invalidssid)
- [case invalidWPAPassphrase](/documentation/networkextension/nehotspotconfigurationerror/invalidwpapassphrase)
- [case invalidWEPPassphrase](/documentation/networkextension/nehotspotconfigurationerror/invalidweppassphrase)
- [case invalidEAPSettings](/documentation/networkextension/nehotspotconfigurationerror/invalideapsettings)
- [case invalidHS20Settings](/documentation/networkextension/nehotspotconfigurationerror/invalidhs20settings)
- [case invalidHS20DomainName](/documentation/networkextension/nehotspotconfigurationerror/invalidhs20domainname)
- [case invalidSSIDPrefix](/documentation/networkextension/nehotspotconfigurationerror/invalidssidprefix)
- [case userDenied](/documentation/networkextension/nehotspotconfigurationerror/userdenied)
- [case `internal`](/documentation/networkextension/nehotspotconfigurationerror/internal)
- [case pending](/documentation/networkextension/nehotspotconfigurationerror/pending)
- [case systemConfiguration](/documentation/networkextension/nehotspotconfigurationerror/systemconfiguration)
- [case unknown](/documentation/networkextension/nehotspotconfigurationerror/unknown)
- [case joinOnceNotSupported](/documentation/networkextension/nehotspotconfigurationerror/joinoncenotsupported)
- [case alreadyAssociated](/documentation/networkextension/nehotspotconfigurationerror/alreadyassociated)
- [case applicationIsNotInForeground](/documentation/networkextension/nehotspotconfigurationerror/applicationisnotinforeground)

##### Enumeration Cases

- [case systemDenied](/documentation/networkextension/nehotspotconfigurationerror/systemdenied)
- [case userUnauthorized](/documentation/networkextension/nehotspotconfigurationerror/userunauthorized)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspotconfigurationerror/init(rawvalue:))

#### Entitlements

- [Hotspot Configuration Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.hotspotconfiguration)

#### Instance Methods

- [func joinAccessoryHotspot(ASAccessory, passphrase: String, completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nehotspotconfigurationmanager/joinaccessoryhotspot(_:passphrase:completionhandler:))
- [func joinAccessoryHotspotWithoutSecurity(ASAccessory, completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nehotspotconfigurationmanager/joinaccessoryhotspotwithoutsecurity(_:completionhandler:))
- [NEHotspotConfiguration](/documentation/networkextension/nehotspotconfiguration)

#### Initializing a configuration

- [init(ssid: String)](/documentation/networkextension/nehotspotconfiguration/init(ssid:))
- [init(ssid: String, passphrase: String, isWEP: Bool)](/documentation/networkextension/nehotspotconfiguration/init(ssid:passphrase:iswep:))
- [init(ssid: String, eapSettings: NEHotspotEAPSettings)](/documentation/networkextension/nehotspotconfiguration/init(ssid:eapsettings:))
- [init(hs20Settings: NEHotspotHS20Settings, eapSettings: NEHotspotEAPSettings)](/documentation/networkextension/nehotspotconfiguration/init(hs20settings:eapsettings:))
- [init(ssidPrefix: String)](/documentation/networkextension/nehotspotconfiguration/init(ssidprefix:))
- [init(ssidPrefix: String, passphrase: String, isWEP: Bool)](/documentation/networkextension/nehotspotconfiguration/init(ssidprefix:passphrase:iswep:))

#### Accessing configuration properties

- [var ssid: String](/documentation/networkextension/nehotspotconfiguration/ssid)
- [var ssidPrefix: String](/documentation/networkextension/nehotspotconfiguration/ssidprefix)
- [var lifeTimeInDays: NSNumber](/documentation/networkextension/nehotspotconfiguration/lifetimeindays)
- [var joinOnce: Bool](/documentation/networkextension/nehotspotconfiguration/joinonce)
- [var hidden: Bool](/documentation/networkextension/nehotspotconfiguration/hidden)
- [NEHotspotEAPSettings](/documentation/networkextension/nehotspoteapsettings)

#### Accessing EAP properties

- [var isTLSClientCertificateRequired: Bool](/documentation/networkextension/nehotspoteapsettings/istlsclientcertificaterequired)
- [var trustedServerNames: [String]](/documentation/networkextension/nehotspoteapsettings/trustedservernames)
- [var supportedEAPTypes: [NSNumber]](/documentation/networkextension/nehotspoteapsettings/supportedeaptypes)
- [NEHotspotEAPSettings.EAPType](/documentation/networkextension/nehotspoteapsettings/eaptype)

##### Enumeration Cases

- [case EAPTLS](/documentation/networkextension/nehotspoteapsettings/eaptype/eaptls)
- [case EAPTTLS](/documentation/networkextension/nehotspoteapsettings/eaptype/eapttls)
- [case EAPPEAP](/documentation/networkextension/nehotspoteapsettings/eaptype/eappeap)
- [case EAPFAST](/documentation/networkextension/nehotspoteapsettings/eaptype/eapfast)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspoteapsettings/eaptype/init(rawvalue:))
- [var username: String](/documentation/networkextension/nehotspoteapsettings/username)
- [var password: String](/documentation/networkextension/nehotspoteapsettings/password)
- [var preferredTLSVersion: NEHotspotEAPSettings.TLSVersion](/documentation/networkextension/nehotspoteapsettings/preferredtlsversion)
- [NEHotspotEAPSettings.TLSVersion](/documentation/networkextension/nehotspoteapsettings/tlsversion)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspoteapsettings/tlsversion/init(rawvalue:))
- [var outerIdentity: String](/documentation/networkextension/nehotspoteapsettings/outeridentity)
- [var ttlsInnerAuthenticationType: NEHotspotEAPSettings.TTLSInnerAuthenticationType](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.property)
- [NEHotspotEAPSettings.TTLSInnerAuthenticationType](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.enum)

##### Enumeration Cases

- [case eapttlsInnerAuthenticationPAP](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.enum/eapttlsinnerauthenticationpap)
- [case eapttlsInnerAuthenticationCHAP](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.enum/eapttlsinnerauthenticationchap)
- [case eapttlsInnerAuthenticationMSCHAP](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.enum/eapttlsinnerauthenticationmschap)
- [case eapttlsInnerAuthenticationMSCHAPv2](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.enum/eapttlsinnerauthenticationmschapv2)
- [case eapttlsInnerAuthenticationEAP](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.enum/eapttlsinnerauthenticationeap)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspoteapsettings/ttlsinnerauthenticationtype-swift.enum/init(rawvalue:))

#### Setting Keychain-based EAP Properties

- [func setIdentity(SecIdentity) -> Bool](/documentation/networkextension/nehotspoteapsettings/setidentity(_:))
- [func setTrustedServerCertificates([Any]) -> Bool](/documentation/networkextension/nehotspoteapsettings/settrustedservercertificates(_:))
- [NEHotspotHS20Settings](/documentation/networkextension/nehotspoths20settings)

#### Initializing Hotspot 2.0 settings

- [init(domainName: String, roamingEnabled: Bool)](/documentation/networkextension/nehotspoths20settings/init(domainname:roamingenabled:))

#### Accessing Hotspot 2.0 properties

- [var domainName: String](/documentation/networkextension/nehotspoths20settings/domainname)
- [var isRoamingEnabled: Bool](/documentation/networkextension/nehotspoths20settings/isroamingenabled)
- [var mccAndMNCs: [String]](/documentation/networkextension/nehotspoths20settings/mccandmncs)
- [var naiRealmNames: [String]](/documentation/networkextension/nehotspoths20settings/nairealmnames)
- [var roamingConsortiumOIs: [String]](/documentation/networkextension/nehotspoths20settings/roamingconsortiumois)
- [Configuring a Wi-Fi accessory to join a network](/documentation/networkextension/configuring-a-wi-fi-accessory-to-join-a-network)
- [Hotspot helper](/documentation/networkextension/hotspot-helper)

### Registration

- [NEHotspotHelper](/documentation/networkextension/nehotspothelper)

#### Registering a hotspot helper

- [class func register(options: [String : NSObject]?, queue: dispatch_queue_t, handler: NEHotspotHelperHandler) -> Bool](/documentation/networkextension/nehotspothelper/register(options:queue:handler:))
- [let kNEHotspotHelperOptionDisplayName: String](/documentation/networkextension/knehotspothelperoptiondisplayname)
- [NEHotspotHelperHandler](/documentation/networkextension/nehotspothelperhandler)

#### Getting hotspot network status

- [class func supportedNetworkInterfaces() -> [Any]?](/documentation/networkextension/nehotspothelper/supportednetworkinterfaces())

#### Logging off

- [class func logoff(NEHotspotNetwork) -> Bool](/documentation/networkextension/nehotspothelper/logoff(_:))

### Commands

- [NEHotspotHelperCommand](/documentation/networkextension/nehotspothelpercommand)

#### Command information

- [var commandType: NEHotspotHelperCommandType](/documentation/networkextension/nehotspothelpercommand/commandtype)
- [NEHotspotHelperCommandType](/documentation/networkextension/nehotspothelpercommandtype)

##### Command Types

- [case none](/documentation/networkextension/nehotspothelpercommandtype/none)
- [case filterScanList](/documentation/networkextension/nehotspothelpercommandtype/filterscanlist)
- [case evaluate](/documentation/networkextension/nehotspothelpercommandtype/evaluate)
- [case authenticate](/documentation/networkextension/nehotspothelpercommandtype/authenticate)
- [case presentUI](/documentation/networkextension/nehotspothelpercommandtype/presentui)
- [case maintain](/documentation/networkextension/nehotspothelpercommandtype/maintain)
- [case logoff](/documentation/networkextension/nehotspothelpercommandtype/logoff)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspothelpercommandtype/init(rawvalue:))
- [var network: NEHotspotNetwork?](/documentation/networkextension/nehotspothelpercommand/network)
- [var networkList: [NEHotspotNetwork]?](/documentation/networkextension/nehotspothelpercommand/networklist)

#### Networking on the hotspot network

- [func bind(to: NEHotspotHelperCommand)](/documentation/foundation/nsmutableurlrequest/bind(to:))
- [func createTCPConnection(NWEndpoint) -> NWTCPConnection](/documentation/networkextension/nehotspothelpercommand/createtcpconnection(_:))
- [func createUDPSession(NWEndpoint) -> NWUDPSession](/documentation/networkextension/nehotspothelpercommand/createudpsession(_:))

#### Response creation

- [func createResponse(NEHotspotHelperResult) -> NEHotspotHelperResponse](/documentation/networkextension/nehotspothelpercommand/createresponse(_:))
- [NEHotspotHelperResult](/documentation/networkextension/nehotspothelperresult)

##### Results

- [case success](/documentation/networkextension/nehotspothelperresult/success)
- [case failure](/documentation/networkextension/nehotspothelperresult/failure)
- [case uiRequired](/documentation/networkextension/nehotspothelperresult/uirequired)
- [case commandNotRecognized](/documentation/networkextension/nehotspothelperresult/commandnotrecognized)
- [case authenticationRequired](/documentation/networkextension/nehotspothelperresult/authenticationrequired)
- [case unsupportedNetwork](/documentation/networkextension/nehotspothelperresult/unsupportednetwork)
- [case temporaryFailure](/documentation/networkextension/nehotspothelperresult/temporaryfailure)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspothelperresult/init(rawvalue:))

#### Instance Properties

- [var interface: NWInterface](/documentation/networkextension/nehotspothelpercommand/interface-46dq)
- [NEHotspotHelperResponse](/documentation/networkextension/nehotspothelperresponse)

#### Response properties

- [func setNetwork(NEHotspotNetwork)](/documentation/networkextension/nehotspothelperresponse/setnetwork(_:))
- [func setNetworkList([NEHotspotNetwork])](/documentation/networkextension/nehotspothelperresponse/setnetworklist(_:))

#### Response delivery

- [func deliver()](/documentation/networkextension/nehotspothelperresponse/deliver())
- [NEHotspotNetwork](/documentation/networkextension/nehotspotnetwork)

#### Network information

- [var ssid: String](/documentation/networkextension/nehotspotnetwork/ssid)
- [var bssid: String](/documentation/networkextension/nehotspotnetwork/bssid)
- [var signalStrength: Double](/documentation/networkextension/nehotspotnetwork/signalstrength)
- [var isSecure: Bool](/documentation/networkextension/nehotspotnetwork/issecure)
- [var didAutoJoin: Bool](/documentation/networkextension/nehotspotnetwork/didautojoin)
- [var didJustJoin: Bool](/documentation/networkextension/nehotspotnetwork/didjustjoin)
- [var isChosenHelper: Bool](/documentation/networkextension/nehotspotnetwork/ischosenhelper)
- [var securityType: NEHotspotNetworkSecurityType](/documentation/networkextension/nehotspotnetwork/securitytype)
- [NEHotspotNetworkSecurityType](/documentation/networkextension/nehotspotnetworksecuritytype)

##### Security types

- [case open](/documentation/networkextension/nehotspotnetworksecuritytype/open)
- [case WEP](/documentation/networkextension/nehotspotnetworksecuritytype/wep)
- [case personal](/documentation/networkextension/nehotspotnetworksecuritytype/personal)
- [case enterprise](/documentation/networkextension/nehotspotnetworksecuritytype/enterprise)
- [case unknown](/documentation/networkextension/nehotspotnetworksecuritytype/unknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspotnetworksecuritytype/init(rawvalue:))

#### Network annotation

- [func setConfidence(NEHotspotHelperConfidence)](/documentation/networkextension/nehotspotnetwork/setconfidence(_:))
- [NEHotspotHelperConfidence](/documentation/networkextension/nehotspothelperconfidence)

##### Confidence Levels

- [case high](/documentation/networkextension/nehotspothelperconfidence/high)
- [case low](/documentation/networkextension/nehotspothelperconfidence/low)
- [case none](/documentation/networkextension/nehotspothelperconfidence/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspothelperconfidence/init(rawvalue:))
- [func setPassword(String)](/documentation/networkextension/nehotspotnetwork/setpassword(_:))

#### Fetching VPN network information

- [class func fetchCurrent(completionHandler: (NEHotspotNetwork?) -> Void)](/documentation/networkextension/nehotspotnetwork/fetchcurrent(completionhandler:))

### Hotspot communication

- [func bind(to: NEHotspotHelperCommand)](/documentation/foundation/nsmutableurlrequest/bind(to:))
- [In-Provider Networking](/documentation/networkextension/in-provider-networking)

#### TCP connections

- [NWTCPConnection](/documentation/networkextension/nwtcpconnection)

##### Monitoring the connection status

- [var state: NWTCPConnectionState](/documentation/networkextension/nwtcpconnection/state)
- [NWTCPConnectionState](/documentation/networkextension/nwtcpconnectionstate)

###### Connection States

- [case invalid](/documentation/networkextension/nwtcpconnectionstate/invalid)
- [case connecting](/documentation/networkextension/nwtcpconnectionstate/connecting)
- [case waiting](/documentation/networkextension/nwtcpconnectionstate/waiting)
- [case connected](/documentation/networkextension/nwtcpconnectionstate/connected)
- [case disconnected](/documentation/networkextension/nwtcpconnectionstate/disconnected)
- [case cancelled](/documentation/networkextension/nwtcpconnectionstate/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwtcpconnectionstate/init(rawvalue:))
- [var isViable: Bool](/documentation/networkextension/nwtcpconnection/isviable)
- [var error: (any Error)?](/documentation/networkextension/nwtcpconnection/error)

##### Transferring data

- [func readMinimumLength(Int, maximumLength: Int, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/readminimumlength(_:maximumlength:completionhandler:))
- [func readLength(Int, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/readlength(_:completionhandler:))
- [func write(Data, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/write(_:completionhandler:))
- [func writeClose()](/documentation/networkextension/nwtcpconnection/writeclose())

##### Canceling the connection

- [func cancel()](/documentation/networkextension/nwtcpconnection/cancel())

##### Responding to network changes

- [var hasBetterPath: Bool](/documentation/networkextension/nwtcpconnection/hasbetterpath)
- [init(upgradeFor: NWTCPConnection)](/documentation/networkextension/nwtcpconnection/init(upgradefor:))

##### Getting connection properties

- [var endpoint: NWEndpoint](/documentation/networkextension/nwtcpconnection/endpoint)
- [var localAddress: NWEndpoint?](/documentation/networkextension/nwtcpconnection/localaddress)
- [var remoteAddress: NWEndpoint?](/documentation/networkextension/nwtcpconnection/remoteaddress)
- [var connectedPath: NWPath?](/documentation/networkextension/nwtcpconnection/connectedpath)
- [var txtRecord: Data?](/documentation/networkextension/nwtcpconnection/txtrecord)
- [NWTLSParameters](/documentation/networkextension/nwtlsparameters)

##### Accessing TLS parameters

- [var tlsSessionID: Data?](/documentation/networkextension/nwtlsparameters/tlssessionid)
- [var sslCipherSuites: Set<NSNumber>?](/documentation/networkextension/nwtlsparameters/sslciphersuites)
- [var minimumSSLProtocolVersion: Int](/documentation/networkextension/nwtlsparameters/minimumsslprotocolversion)
- [var maximumSSLProtocolVersion: Int](/documentation/networkextension/nwtlsparameters/maximumsslprotocolversion)
- [NWTCPConnectionAuthenticationDelegate](/documentation/networkextension/nwtcpconnectionauthenticationdelegate)

##### Delegate methods

- [func shouldEvaluateTrust(for: NWTCPConnection) -> Bool](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/shouldevaluatetrust(for:))
- [func evaluateTrust(for: NWTCPConnection, peerCertificateChain: [Any], completionHandler: (SecTrust) -> Void)](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/evaluatetrust(for:peercertificatechain:completionhandler:))
- [func shouldProvideIdentity(for: NWTCPConnection) -> Bool](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/shouldprovideidentity(for:))
- [func provideIdentity(for: NWTCPConnection, completionHandler: (SecIdentity, [Any]) -> Void)](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/provideidentity(for:completionhandler:))

#### UDP sessions

- [NWUDPSession](/documentation/networkextension/nwudpsession)

##### Monitoring the session state

- [var state: NWUDPSessionState](/documentation/networkextension/nwudpsession/state)
- [NWUDPSessionState](/documentation/networkextension/nwudpsessionstate)

###### Session States

- [case invalid](/documentation/networkextension/nwudpsessionstate/invalid)
- [case waiting](/documentation/networkextension/nwudpsessionstate/waiting)
- [case preparing](/documentation/networkextension/nwudpsessionstate/preparing)
- [case ready](/documentation/networkextension/nwudpsessionstate/ready)
- [case failed](/documentation/networkextension/nwudpsessionstate/failed)
- [case cancelled](/documentation/networkextension/nwudpsessionstate/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwudpsessionstate/init(rawvalue:))
- [var isViable: Bool](/documentation/networkextension/nwudpsession/isviable)

##### Selecting remote endpoints

- [var resolvedEndpoint: NWEndpoint?](/documentation/networkextension/nwudpsession/resolvedendpoint)
- [func tryNextResolvedEndpoint()](/documentation/networkextension/nwudpsession/trynextresolvedendpoint())

##### Transferring data

- [func setReadHandler(([Data]?, (any Error)?) -> Void, maxDatagrams: Int)](/documentation/networkextension/nwudpsession/setreadhandler(_:maxdatagrams:))
- [func writeDatagram(Data, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwudpsession/writedatagram(_:completionhandler:))
- [func writeMultipleDatagrams([Data], completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwudpsession/writemultipledatagrams(_:completionhandler:))
- [var maximumDatagramLength: Int](/documentation/networkextension/nwudpsession/maximumdatagramlength)

##### Canceling the session

- [func cancel()](/documentation/networkextension/nwudpsession/cancel())

##### Responding to network changes

- [var hasBetterPath: Bool](/documentation/networkextension/nwudpsession/hasbetterpath)
- [init(upgradeFor: NWUDPSession)](/documentation/networkextension/nwudpsession/init(upgradefor:))

##### Getting session properties

- [var endpoint: NWEndpoint](/documentation/networkextension/nwudpsession/endpoint)
- [var currentPath: NWPath?](/documentation/networkextension/nwudpsession/currentpath)

#### Endpoints

- [NWHostEndpoint](/documentation/networkextension/nwhostendpoint)

##### Initializing host endpoints

- [convenience init(hostname: String, port: String)](/documentation/networkextension/nwhostendpoint/init(hostname:port:))

##### Getting endpoint properties

- [var hostname: String](/documentation/networkextension/nwhostendpoint/hostname)
- [var port: String](/documentation/networkextension/nwhostendpoint/port)
- [NWBonjourServiceEndpoint](/documentation/networkextension/nwbonjourserviceendpoint)

##### Initializing Bonjour service endpoints

- [convenience init(name: String, type: String, domain: String)](/documentation/networkextension/nwbonjourserviceendpoint/init(name:type:domain:))

##### Getting endpoint properties

- [var name: String](/documentation/networkextension/nwbonjourserviceendpoint/name)
- [var type: String](/documentation/networkextension/nwbonjourserviceendpoint/type)
- [var domain: String](/documentation/networkextension/nwbonjourserviceendpoint/domain)
- [NWEndpoint](/documentation/networkextension/nwendpoint)

#### Network path information

- [NWPath](/documentation/networkextension/nwpath)

##### Getting network path properties

- [var status: NWPathStatus](/documentation/networkextension/nwpath/status)
- [NWPathStatus](/documentation/networkextension/nwpathstatus)

###### Path Statuses

- [case invalid](/documentation/networkextension/nwpathstatus/invalid)
- [case satisfied](/documentation/networkextension/nwpathstatus/satisfied)
- [case unsatisfied](/documentation/networkextension/nwpathstatus/unsatisfied)
- [case satisfiable](/documentation/networkextension/nwpathstatus/satisfiable)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwpathstatus/init(rawvalue:))
- [var isExpensive: Bool](/documentation/networkextension/nwpath/isexpensive)
- [var isConstrained: Bool](/documentation/networkextension/nwpath/isconstrained)

##### Comparing network paths

- [func isEqual(to: NWPath) -> Bool](/documentation/networkextension/nwpath/isequal(to:))

### Hotspot helper extension

- [NEHotspotManager](/documentation/networkextension/nehotspotmanager)

#### Accessing the shared instance

- [static var shared: NEHotspotManager](/documentation/networkextension/nehotspotmanager/shared)

#### Accessing provider properties

- [var isEnabled: Bool](/documentation/networkextension/nehotspotmanager/isenabled)
- [var evaluationProviderBundleIdentifier: String?](/documentation/networkextension/nehotspotmanager/evaluationproviderbundleidentifier)
- [var authenticationProviderBundleIdentifier: String?](/documentation/networkextension/nehotspotmanager/authenticationproviderbundleidentifier)

#### Authenticating with Safari domains

- [var safariDomains: [String]](/documentation/networkextension/nehotspotmanager/safaridomains)

#### Identifying pre-evaluated Wi-Fi networks

- [var evaluatedSSIDs: [String]](/documentation/networkextension/nehotspotmanager/evaluatedssids)

#### Managing the saved configuration

- [func loadFromPreferences() async throws](/documentation/networkextension/nehotspotmanager/loadfrompreferences())
- [func saveToPreferences() async throws](/documentation/networkextension/nehotspotmanager/savetopreferences())
- [func removeFromPreferences() async throws](/documentation/networkextension/nehotspotmanager/removefrompreferences())

#### Identifying manager errors

- [NEHotspotManager.Error](/documentation/networkextension/nehotspotmanager/error)

##### Configuration errors

- [case configurationNotLoaded](/documentation/networkextension/nehotspotmanager/error/configurationnotloaded)
- [case configurationInvalid](/documentation/networkextension/nehotspotmanager/error/configurationinvalid)

##### Other errors

- [case internalError](/documentation/networkextension/nehotspotmanager/error/internalerror)
- [NEHotspotEvaluationProvider](/documentation/networkextension/nehotspotevaluationprovider)

#### Managing provider life cycle

- [func start() async -> Bool](/documentation/networkextension/nehotspotevaluationprovider/start())
- [func stop(reason: NEProviderStopReason) async](/documentation/networkextension/nehotspotevaluationprovider/stop(reason:))
- [NEProviderStopReason](/documentation/networkextension/neproviderstopreason)

##### Stop Reasons

- [case none](/documentation/networkextension/neproviderstopreason/none)
- [case userInitiated](/documentation/networkextension/neproviderstopreason/userinitiated)
- [case providerFailed](/documentation/networkextension/neproviderstopreason/providerfailed)
- [case noNetworkAvailable](/documentation/networkextension/neproviderstopreason/nonetworkavailable)
- [case unrecoverableNetworkChange](/documentation/networkextension/neproviderstopreason/unrecoverablenetworkchange)
- [case providerDisabled](/documentation/networkextension/neproviderstopreason/providerdisabled)
- [case authenticationCanceled](/documentation/networkextension/neproviderstopreason/authenticationcanceled)
- [case configurationFailed](/documentation/networkextension/neproviderstopreason/configurationfailed)
- [case idleTimeout](/documentation/networkextension/neproviderstopreason/idletimeout)
- [case configurationDisabled](/documentation/networkextension/neproviderstopreason/configurationdisabled)
- [case configurationRemoved](/documentation/networkextension/neproviderstopreason/configurationremoved)
- [case superceded](/documentation/networkextension/neproviderstopreason/superceded)
- [case userLogout](/documentation/networkextension/neproviderstopreason/userlogout)
- [case userSwitch](/documentation/networkextension/neproviderstopreason/userswitch)
- [case appUpdate](/documentation/networkextension/neproviderstopreason/appupdate)
- [case connectionFailed](/documentation/networkextension/neproviderstopreason/connectionfailed)
- [case sleep](/documentation/networkextension/neproviderstopreason/sleep)
- [case internalError](/documentation/networkextension/neproviderstopreason/internalerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neproviderstopreason/init(rawvalue:))

#### Sending commands to the provider

- [func handleCommand(NEHotspotHelperCommand) async -> NEHotspotHelperResponse](/documentation/networkextension/nehotspotevaluationprovider/handlecommand(_:))
- [NEHotspotHelperCommand](/documentation/networkextension/nehotspothelpercommand)

##### Command information

- [var commandType: NEHotspotHelperCommandType](/documentation/networkextension/nehotspothelpercommand/commandtype)
- [NEHotspotHelperCommandType](/documentation/networkextension/nehotspothelpercommandtype)

###### Command Types

- [case none](/documentation/networkextension/nehotspothelpercommandtype/none)
- [case filterScanList](/documentation/networkextension/nehotspothelpercommandtype/filterscanlist)
- [case evaluate](/documentation/networkextension/nehotspothelpercommandtype/evaluate)
- [case authenticate](/documentation/networkextension/nehotspothelpercommandtype/authenticate)
- [case presentUI](/documentation/networkextension/nehotspothelpercommandtype/presentui)
- [case maintain](/documentation/networkextension/nehotspothelpercommandtype/maintain)
- [case logoff](/documentation/networkextension/nehotspothelpercommandtype/logoff)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspothelpercommandtype/init(rawvalue:))
- [var network: NEHotspotNetwork?](/documentation/networkextension/nehotspothelpercommand/network)
- [var networkList: [NEHotspotNetwork]?](/documentation/networkextension/nehotspothelpercommand/networklist)

##### Networking on the hotspot network

- [func bind(to: NEHotspotHelperCommand)](/documentation/foundation/nsmutableurlrequest/bind(to:))
- [func createTCPConnection(NWEndpoint) -> NWTCPConnection](/documentation/networkextension/nehotspothelpercommand/createtcpconnection(_:))
- [func createUDPSession(NWEndpoint) -> NWUDPSession](/documentation/networkextension/nehotspothelpercommand/createudpsession(_:))

##### Response creation

- [func createResponse(NEHotspotHelperResult) -> NEHotspotHelperResponse](/documentation/networkextension/nehotspothelpercommand/createresponse(_:))
- [NEHotspotHelperResult](/documentation/networkextension/nehotspothelperresult)

###### Results

- [case success](/documentation/networkextension/nehotspothelperresult/success)
- [case failure](/documentation/networkextension/nehotspothelperresult/failure)
- [case uiRequired](/documentation/networkextension/nehotspothelperresult/uirequired)
- [case commandNotRecognized](/documentation/networkextension/nehotspothelperresult/commandnotrecognized)
- [case authenticationRequired](/documentation/networkextension/nehotspothelperresult/authenticationrequired)
- [case unsupportedNetwork](/documentation/networkextension/nehotspothelperresult/unsupportednetwork)
- [case temporaryFailure](/documentation/networkextension/nehotspothelperresult/temporaryfailure)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspothelperresult/init(rawvalue:))

##### Instance Properties

- [var interface: NWInterface](/documentation/networkextension/nehotspothelpercommand/interface-46dq)

#### Providing a network name

- [var localizedDisplayName: String](/documentation/networkextension/nehotspotevaluationprovider/localizeddisplayname)
- [NEHotspotAuthenticationProvider](/documentation/networkextension/nehotspotauthenticationprovider)

#### Managing provider life cycle

- [func start() async -> Bool](/documentation/networkextension/nehotspotauthenticationprovider/start())
- [func stop(reason: NEProviderStopReason) async](/documentation/networkextension/nehotspotauthenticationprovider/stop(reason:))
- [NEProviderStopReason](/documentation/networkextension/neproviderstopreason)

##### Stop Reasons

- [case none](/documentation/networkextension/neproviderstopreason/none)
- [case userInitiated](/documentation/networkextension/neproviderstopreason/userinitiated)
- [case providerFailed](/documentation/networkextension/neproviderstopreason/providerfailed)
- [case noNetworkAvailable](/documentation/networkextension/neproviderstopreason/nonetworkavailable)
- [case unrecoverableNetworkChange](/documentation/networkextension/neproviderstopreason/unrecoverablenetworkchange)
- [case providerDisabled](/documentation/networkextension/neproviderstopreason/providerdisabled)
- [case authenticationCanceled](/documentation/networkextension/neproviderstopreason/authenticationcanceled)
- [case configurationFailed](/documentation/networkextension/neproviderstopreason/configurationfailed)
- [case idleTimeout](/documentation/networkextension/neproviderstopreason/idletimeout)
- [case configurationDisabled](/documentation/networkextension/neproviderstopreason/configurationdisabled)
- [case configurationRemoved](/documentation/networkextension/neproviderstopreason/configurationremoved)
- [case superceded](/documentation/networkextension/neproviderstopreason/superceded)
- [case userLogout](/documentation/networkextension/neproviderstopreason/userlogout)
- [case userSwitch](/documentation/networkextension/neproviderstopreason/userswitch)
- [case appUpdate](/documentation/networkextension/neproviderstopreason/appupdate)
- [case connectionFailed](/documentation/networkextension/neproviderstopreason/connectionfailed)
- [case sleep](/documentation/networkextension/neproviderstopreason/sleep)
- [case internalError](/documentation/networkextension/neproviderstopreason/internalerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neproviderstopreason/init(rawvalue:))

#### Sending commands to the provider

- [func handleCommand(NEHotspotHelperCommand) async -> NEHotspotHelperResponse](/documentation/networkextension/nehotspotauthenticationprovider/handlecommand(_:))
- [NEHotspotHelperCommand](/documentation/networkextension/nehotspothelpercommand)

##### Command information

- [var commandType: NEHotspotHelperCommandType](/documentation/networkextension/nehotspothelpercommand/commandtype)
- [NEHotspotHelperCommandType](/documentation/networkextension/nehotspothelpercommandtype)

###### Command Types

- [case none](/documentation/networkextension/nehotspothelpercommandtype/none)
- [case filterScanList](/documentation/networkextension/nehotspothelpercommandtype/filterscanlist)
- [case evaluate](/documentation/networkextension/nehotspothelpercommandtype/evaluate)
- [case authenticate](/documentation/networkextension/nehotspothelpercommandtype/authenticate)
- [case presentUI](/documentation/networkextension/nehotspothelpercommandtype/presentui)
- [case maintain](/documentation/networkextension/nehotspothelpercommandtype/maintain)
- [case logoff](/documentation/networkextension/nehotspothelpercommandtype/logoff)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspothelpercommandtype/init(rawvalue:))
- [var network: NEHotspotNetwork?](/documentation/networkextension/nehotspothelpercommand/network)
- [var networkList: [NEHotspotNetwork]?](/documentation/networkextension/nehotspothelpercommand/networklist)

##### Networking on the hotspot network

- [func bind(to: NEHotspotHelperCommand)](/documentation/foundation/nsmutableurlrequest/bind(to:))
- [func createTCPConnection(NWEndpoint) -> NWTCPConnection](/documentation/networkextension/nehotspothelpercommand/createtcpconnection(_:))
- [func createUDPSession(NWEndpoint) -> NWUDPSession](/documentation/networkextension/nehotspothelpercommand/createudpsession(_:))

##### Response creation

- [func createResponse(NEHotspotHelperResult) -> NEHotspotHelperResponse](/documentation/networkextension/nehotspothelpercommand/createresponse(_:))
- [NEHotspotHelperResult](/documentation/networkextension/nehotspothelperresult)

###### Results

- [case success](/documentation/networkextension/nehotspothelperresult/success)
- [case failure](/documentation/networkextension/nehotspothelperresult/failure)
- [case uiRequired](/documentation/networkextension/nehotspothelperresult/uirequired)
- [case commandNotRecognized](/documentation/networkextension/nehotspothelperresult/commandnotrecognized)
- [case authenticationRequired](/documentation/networkextension/nehotspothelperresult/authenticationrequired)
- [case unsupportedNetwork](/documentation/networkextension/nehotspothelperresult/unsupportednetwork)
- [case temporaryFailure](/documentation/networkextension/nehotspothelperresult/temporaryfailure)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nehotspothelperresult/init(rawvalue:))

##### Instance Properties

- [var interface: NWInterface](/documentation/networkextension/nehotspothelpercommand/interface-46dq)
- [NEHotspotEvaluationProviderConfiguration](/documentation/networkextension/nehotspotevaluationproviderconfiguration)
- [NEHotspotAuthenticationProviderConfiguration](/documentation/networkextension/nehotspotauthenticationproviderconfiguration)

## Virtual private networks

- [Routing your VPN network traffic](/documentation/networkextension/routing-your-vpn-network-traffic)
- [Personal VPN](/documentation/networkextension/personal-vpn)

### Essentials

- [Personal VPN Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.vpn.api)

### VPN configuration

- [NEVPNManager](/documentation/networkextension/nevpnmanager)

#### Managing VPN configurations

- [class func shared() -> NEVPNManager](/documentation/networkextension/nevpnmanager/shared())
- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nevpnmanager/loadfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nevpnmanager/savetopreferences(completionhandler:))
- [func setAuthorization(AuthorizationRef)](/documentation/networkextension/nevpnmanager/setauthorization(_:))
- [func removeFromPreferences(completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nevpnmanager/removefrompreferences(completionhandler:))

#### Accessing VPN configuration properties

- [var isEnabled: Bool](/documentation/networkextension/nevpnmanager/isenabled)
- [var protocolConfiguration: NEVPNProtocol?](/documentation/networkextension/nevpnmanager/protocolconfiguration)
- [var `protocol`: NEVPNProtocol?](/documentation/networkextension/nevpnmanager/protocol)
- [var localizedDescription: String?](/documentation/networkextension/nevpnmanager/localizeddescription)
- [var isOnDemandEnabled: Bool](/documentation/networkextension/nevpnmanager/isondemandenabled)
- [var onDemandRules: [NEOnDemandRule]?](/documentation/networkextension/nevpnmanager/ondemandrules)

#### Connecting and disconnecting VPN

- [var connection: NEVPNConnection](/documentation/networkextension/nevpnmanager/connection)

#### Errors

- [NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/code)

##### Error codes

- [case configurationDisabled](/documentation/networkextension/nevpnerror-swift.struct/code/configurationdisabled)
- [case configurationInvalid](/documentation/networkextension/nevpnerror-swift.struct/code/configurationinvalid)
- [case connectionFailed](/documentation/networkextension/nevpnerror-swift.struct/code/connectionfailed)
- [case configurationStale](/documentation/networkextension/nevpnerror-swift.struct/code/configurationstale)
- [case configurationReadWriteFailed](/documentation/networkextension/nevpnerror-swift.struct/code/configurationreadwritefailed)
- [case configurationUnknown](/documentation/networkextension/nevpnerror-swift.struct/code/configurationunknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnerror-swift.struct/code/init(rawvalue:))
- [let NEVPNErrorDomain: String](/documentation/networkextension/nevpnerrordomain)
- [NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/code)

##### Error codes

- [case configurationDisabled](/documentation/networkextension/nevpnerror-swift.struct/code/configurationdisabled)
- [case configurationInvalid](/documentation/networkextension/nevpnerror-swift.struct/code/configurationinvalid)
- [case connectionFailed](/documentation/networkextension/nevpnerror-swift.struct/code/connectionfailed)
- [case configurationStale](/documentation/networkextension/nevpnerror-swift.struct/code/configurationstale)
- [case configurationReadWriteFailed](/documentation/networkextension/nevpnerror-swift.struct/code/configurationreadwritefailed)
- [case configurationUnknown](/documentation/networkextension/nevpnerror-swift.struct/code/configurationunknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnerror-swift.struct/code/init(rawvalue:))

#### Notifications

- [static let NEVPNConfigurationChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nevpnconfigurationchange)

#### Entitlements

- [Personal VPN Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.vpn.api)
- [NEVPNProtocolIKEv2](/documentation/networkextension/nevpnprotocolikev2)

#### Accessing IKEv2 Security Association parameters

- [var ikeSecurityAssociationParameters: NEVPNIKEv2SecurityAssociationParameters](/documentation/networkextension/nevpnprotocolikev2/ikesecurityassociationparameters)
- [var childSecurityAssociationParameters: NEVPNIKEv2SecurityAssociationParameters](/documentation/networkextension/nevpnprotocolikev2/childsecurityassociationparameters)
- [NEVPNIKEv2SecurityAssociationParameters](/documentation/networkextension/nevpnikev2securityassociationparameters)

##### IKEv2 Security Association parameters

- [var encryptionAlgorithm: NEVPNIKEv2EncryptionAlgorithm](/documentation/networkextension/nevpnikev2securityassociationparameters/encryptionalgorithm)
- [NEVPNIKEv2EncryptionAlgorithm](/documentation/networkextension/nevpnikev2encryptionalgorithm)

###### Encryption algorithms

- [case algorithmDES](/documentation/networkextension/nevpnikev2encryptionalgorithm/algorithmdes)
- [case algorithm3DES](/documentation/networkextension/nevpnikev2encryptionalgorithm/algorithm3des)
- [case algorithmAES128](/documentation/networkextension/nevpnikev2encryptionalgorithm/algorithmaes128)
- [case algorithmAES256](/documentation/networkextension/nevpnikev2encryptionalgorithm/algorithmaes256)
- [case algorithmAES128GCM](/documentation/networkextension/nevpnikev2encryptionalgorithm/algorithmaes128gcm)
- [case algorithmAES256GCM](/documentation/networkextension/nevpnikev2encryptionalgorithm/algorithmaes256gcm)
- [case algorithmChaCha20Poly1305](/documentation/networkextension/nevpnikev2encryptionalgorithm/algorithmchacha20poly1305)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikev2encryptionalgorithm/init(rawvalue:))
- [var integrityAlgorithm: NEVPNIKEv2IntegrityAlgorithm](/documentation/networkextension/nevpnikev2securityassociationparameters/integrityalgorithm)
- [NEVPNIKEv2IntegrityAlgorithm](/documentation/networkextension/nevpnikev2integrityalgorithm)

###### Integrity algorithms

- [case SHA96](/documentation/networkextension/nevpnikev2integrityalgorithm/sha96)
- [case SHA160](/documentation/networkextension/nevpnikev2integrityalgorithm/sha160)
- [case SHA256](/documentation/networkextension/nevpnikev2integrityalgorithm/sha256)
- [case SHA384](/documentation/networkextension/nevpnikev2integrityalgorithm/sha384)
- [case SHA512](/documentation/networkextension/nevpnikev2integrityalgorithm/sha512)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikev2integrityalgorithm/init(rawvalue:))
- [var diffieHellmanGroup: NEVPNIKEv2DiffieHellmanGroup](/documentation/networkextension/nevpnikev2securityassociationparameters/diffiehellmangroup)
- [NEVPNIKEv2DiffieHellmanGroup](/documentation/networkextension/nevpnikev2diffiehellmangroup)

###### Diffie-Hellman groups

- [case groupInvalid](/documentation/networkextension/nevpnikev2diffiehellmangroup/groupinvalid)
- [case group1](/documentation/networkextension/nevpnikev2diffiehellmangroup/group1)
- [case group2](/documentation/networkextension/nevpnikev2diffiehellmangroup/group2)
- [case group5](/documentation/networkextension/nevpnikev2diffiehellmangroup/group5)
- [case group14](/documentation/networkextension/nevpnikev2diffiehellmangroup/group14)
- [case group15](/documentation/networkextension/nevpnikev2diffiehellmangroup/group15)
- [case group16](/documentation/networkextension/nevpnikev2diffiehellmangroup/group16)
- [case group17](/documentation/networkextension/nevpnikev2diffiehellmangroup/group17)
- [case group18](/documentation/networkextension/nevpnikev2diffiehellmangroup/group18)
- [case group19](/documentation/networkextension/nevpnikev2diffiehellmangroup/group19)
- [case group20](/documentation/networkextension/nevpnikev2diffiehellmangroup/group20)
- [case group21](/documentation/networkextension/nevpnikev2diffiehellmangroup/group21)
- [case group31](/documentation/networkextension/nevpnikev2diffiehellmangroup/group31)
- [case group32](/documentation/networkextension/nevpnikev2diffiehellmangroup/group32)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikev2diffiehellmangroup/init(rawvalue:))
- [var lifetimeMinutes: Int32](/documentation/networkextension/nevpnikev2securityassociationparameters/lifetimeminutes)
- [var postQuantumKeyExchangeMethods: [NEVPNIKEv2PostQuantumKeyExchangeMethod]](/documentation/networkextension/nevpnikev2securityassociationparameters/postquantumkeyexchangemethods-3173s)
- [NEVPNIKEv2PostQuantumKeyExchangeMethod](/documentation/networkextension/nevpnikev2postquantumkeyexchangemethod)

###### Key exchange methods

- [case method36](/documentation/networkextension/nevpnikev2postquantumkeyexchangemethod/method36)
- [case method37](/documentation/networkextension/nevpnikev2postquantumkeyexchangemethod/method37)
- [case methodNone](/documentation/networkextension/nevpnikev2postquantumkeyexchangemethod/methodnone)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikev2postquantumkeyexchangemethod/init(rawvalue:))

#### Accessing certificate properties

- [var serverCertificateIssuerCommonName: String?](/documentation/networkextension/nevpnprotocolikev2/servercertificateissuercommonname)
- [var serverCertificateCommonName: String?](/documentation/networkextension/nevpnprotocolikev2/servercertificatecommonname)
- [var certificateType: NEVPNIKEv2CertificateType](/documentation/networkextension/nevpnprotocolikev2/certificatetype)
- [NEVPNIKEv2CertificateType](/documentation/networkextension/nevpnikev2certificatetype)

##### Certificate types

- [case RSA](/documentation/networkextension/nevpnikev2certificatetype/rsa)
- [case ECDSA256](/documentation/networkextension/nevpnikev2certificatetype/ecdsa256)
- [case ECDSA384](/documentation/networkextension/nevpnikev2certificatetype/ecdsa384)
- [case ECDSA521](/documentation/networkextension/nevpnikev2certificatetype/ecdsa521)
- [case ed25519](/documentation/networkextension/nevpnikev2certificatetype/ed25519)
- [case RSAPSS](/documentation/networkextension/nevpnikev2certificatetype/rsapss)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikev2certificatetype/init(rawvalue:))

#### Accessing TLS version properties

- [var minimumTLSVersion: NEVPNIKEv2TLSVersion](/documentation/networkextension/nevpnprotocolikev2/minimumtlsversion)
- [var maximumTLSVersion: NEVPNIKEv2TLSVersion](/documentation/networkextension/nevpnprotocolikev2/maximumtlsversion)
- [NEVPNIKEv2TLSVersion](/documentation/networkextension/nevpnikev2tlsversion)

##### TLS versions

- [case versionDefault](/documentation/networkextension/nevpnikev2tlsversion/versiondefault)
- [case version1_0](/documentation/networkextension/nevpnikev2tlsversion/version1_0)
- [case version1_1](/documentation/networkextension/nevpnikev2tlsversion/version1_1)
- [case version1_2](/documentation/networkextension/nevpnikev2tlsversion/version1_2)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikev2tlsversion/init(rawvalue:))

#### Accessing other IKEv2 properties

- [var deadPeerDetectionRate: NEVPNIKEv2DeadPeerDetectionRate](/documentation/networkextension/nevpnprotocolikev2/deadpeerdetectionrate)
- [NEVPNIKEv2DeadPeerDetectionRate](/documentation/networkextension/nevpnikev2deadpeerdetectionrate)

##### Detection rates

- [case none](/documentation/networkextension/nevpnikev2deadpeerdetectionrate/none)
- [case low](/documentation/networkextension/nevpnikev2deadpeerdetectionrate/low)
- [case medium](/documentation/networkextension/nevpnikev2deadpeerdetectionrate/medium)
- [case high](/documentation/networkextension/nevpnikev2deadpeerdetectionrate/high)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikev2deadpeerdetectionrate/init(rawvalue:))
- [var useConfigurationAttributeInternalIPSubnet: Bool](/documentation/networkextension/nevpnprotocolikev2/useconfigurationattributeinternalipsubnet)
- [var disableMOBIKE: Bool](/documentation/networkextension/nevpnprotocolikev2/disablemobike)
- [var disableRedirect: Bool](/documentation/networkextension/nevpnprotocolikev2/disableredirect)
- [var enablePFS: Bool](/documentation/networkextension/nevpnprotocolikev2/enablepfs)
- [var enableRevocationCheck: Bool](/documentation/networkextension/nevpnprotocolikev2/enablerevocationcheck)
- [var strictRevocationCheck: Bool](/documentation/networkextension/nevpnprotocolikev2/strictrevocationcheck)
- [var mtu: Int](/documentation/networkextension/nevpnprotocolikev2/mtu)

#### Supporting Wi-Fi assist

- [var enableFallback: Bool](/documentation/networkextension/nevpnprotocolikev2/enablefallback)

#### Supporting quantum-secure cryptography

- [var allowPostQuantumKeyExchangeFallback: Bool](/documentation/networkextension/nevpnprotocolikev2/allowpostquantumkeyexchangefallback)
- [var ppkConfiguration: NEVPNIKEv2PPKConfiguration?](/documentation/networkextension/nevpnprotocolikev2/ppkconfiguration)
- [NEVPNIKEv2PPKConfiguration](/documentation/networkextension/nevpnikev2ppkconfiguration)

##### Creating a PPK configuration

- [init(identifier: String, keychainReference: Data)](/documentation/networkextension/nevpnikev2ppkconfiguration/init(identifier:keychainreference:))

##### Accessing the configuration parameters

- [var identifier: String](/documentation/networkextension/nevpnikev2ppkconfiguration/identifier)
- [var keychainReference: Data](/documentation/networkextension/nevpnikev2ppkconfiguration/keychainreference)
- [var isMandatory: Bool](/documentation/networkextension/nevpnikev2ppkconfiguration/ismandatory)
- [NEVPNProtocolIPSec](/documentation/networkextension/nevpnprotocolipsec)

#### Accessing IPSec properties

- [var authenticationMethod: NEVPNIKEAuthenticationMethod](/documentation/networkextension/nevpnprotocolipsec/authenticationmethod)
- [NEVPNIKEAuthenticationMethod](/documentation/networkextension/nevpnikeauthenticationmethod)

##### Authentication methods

- [case none](/documentation/networkextension/nevpnikeauthenticationmethod/none)
- [case certificate](/documentation/networkextension/nevpnikeauthenticationmethod/certificate)
- [case sharedSecret](/documentation/networkextension/nevpnikeauthenticationmethod/sharedsecret)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnikeauthenticationmethod/init(rawvalue:))
- [var useExtendedAuthentication: Bool](/documentation/networkextension/nevpnprotocolipsec/useextendedauthentication)
- [var sharedSecretReference: Data?](/documentation/networkextension/nevpnprotocolipsec/sharedsecretreference)
- [var localIdentifier: String?](/documentation/networkextension/nevpnprotocolipsec/localidentifier)
- [var remoteIdentifier: String?](/documentation/networkextension/nevpnprotocolipsec/remoteidentifier)
- [NEVPNProtocol](/documentation/networkextension/nevpnprotocol)

#### Configuring the VPN

- [var serverAddress: String?](/documentation/networkextension/nevpnprotocol/serveraddress)
- [var disconnectOnSleep: Bool](/documentation/networkextension/nevpnprotocol/disconnectonsleep)
- [var proxySettings: NEProxySettings?](/documentation/networkextension/nevpnprotocol/proxysettings)

#### Authenticating the user

- [var username: String?](/documentation/networkextension/nevpnprotocol/username)
- [var passwordReference: Data?](/documentation/networkextension/nevpnprotocol/passwordreference)
- [var identityReference: Data?](/documentation/networkextension/nevpnprotocol/identityreference)
- [var identityData: Data?](/documentation/networkextension/nevpnprotocol/identitydata)
- [var identityDataPassword: String?](/documentation/networkextension/nevpnprotocol/identitydatapassword)

#### Routing network traffic

- [var includeAllNetworks: Bool](/documentation/networkextension/nevpnprotocol/includeallnetworks)
- [var excludeAPNs: Bool](/documentation/networkextension/nevpnprotocol/excludeapns)
- [var excludeCellularServices: Bool](/documentation/networkextension/nevpnprotocol/excludecellularservices)
- [var excludeLocalNetworks: Bool](/documentation/networkextension/nevpnprotocol/excludelocalnetworks)
- [var enforceRoutes: Bool](/documentation/networkextension/nevpnprotocol/enforceroutes)

#### Instance Properties

- [var excludeDeviceCommunication: Bool](/documentation/networkextension/nevpnprotocol/excludedevicecommunication)
- [var sliceUUID: String?](/documentation/networkextension/nevpnprotocol/sliceuuid)
- [VPN On Demand Rules](/documentation/networkextension/vpn-on-demand-rules)

#### Settings

- [NEOnDemandRuleConnect](/documentation/networkextension/neondemandruleconnect)
- [NEOnDemandRuleDisconnect](/documentation/networkextension/neondemandruledisconnect)
- [NEOnDemandRuleIgnore](/documentation/networkextension/neondemandruleignore)
- [NEOnDemandRuleEvaluateConnection](/documentation/networkextension/neondemandruleevaluateconnection)

##### Accessing connection rules

- [var connectionRules: [NEEvaluateConnectionRule]?](/documentation/networkextension/neondemandruleevaluateconnection/connectionrules)
- [NEEvaluateConnectionRule](/documentation/networkextension/neevaluateconnectionrule)

###### Initializing a Rule

- [init(matchDomains: [String], andAction: NEEvaluateConnectionRuleAction)](/documentation/networkextension/neevaluateconnectionrule/init(matchdomains:andaction:))

###### Accessing Rule Match Properties

- [var matchDomains: [String]](/documentation/networkextension/neevaluateconnectionrule/matchdomains)
- [var useDNSServers: [String]?](/documentation/networkextension/neevaluateconnectionrule/usednsservers)
- [var probeURL: URL?](/documentation/networkextension/neevaluateconnectionrule/probeurl)

###### Accessing the Rule Action

- [var action: NEEvaluateConnectionRuleAction](/documentation/networkextension/neevaluateconnectionrule/action)
- [NEEvaluateConnectionRuleAction](/documentation/networkextension/neevaluateconnectionruleaction)

###### Rule Actions

- [case connectIfNeeded](/documentation/networkextension/neevaluateconnectionruleaction/connectifneeded)
- [case neverConnect](/documentation/networkextension/neevaluateconnectionruleaction/neverconnect)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neevaluateconnectionruleaction/init(rawvalue:))
- [NEOnDemandRule](/documentation/networkextension/neondemandrule)

##### Accessing match parameters

- [var dnsSearchDomainMatch: [String]?](/documentation/networkextension/neondemandrule/dnssearchdomainmatch)
- [var dnsServerAddressMatch: [String]?](/documentation/networkextension/neondemandrule/dnsserveraddressmatch)
- [var interfaceTypeMatch: NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandrule/interfacetypematch)
- [NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandruleinterfacetype)

###### Interface Types

- [case any](/documentation/networkextension/neondemandruleinterfacetype/any)
- [case ethernet](/documentation/networkextension/neondemandruleinterfacetype/ethernet)
- [case wiFi](/documentation/networkextension/neondemandruleinterfacetype/wifi)
- [case cellular](/documentation/networkextension/neondemandruleinterfacetype/cellular)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleinterfacetype/init(rawvalue:))
- [var ssidMatch: [String]?](/documentation/networkextension/neondemandrule/ssidmatch)
- [var probeURL: URL?](/documentation/networkextension/neondemandrule/probeurl)

##### Accessing the rule action

- [var action: NEOnDemandRuleAction](/documentation/networkextension/neondemandrule/action)
- [NEOnDemandRuleAction](/documentation/networkextension/neondemandruleaction)

###### Rule Actions

- [case connect](/documentation/networkextension/neondemandruleaction/connect)
- [case disconnect](/documentation/networkextension/neondemandruleaction/disconnect)
- [case evaluateConnection](/documentation/networkextension/neondemandruleaction/evaluateconnection)
- [case ignore](/documentation/networkextension/neondemandruleaction/ignore)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleaction/init(rawvalue:))

### VPN control

- [NEVPNConnection](/documentation/networkextension/nevpnconnection)

#### Controlling the VPN connection

- [func startVPNTunnel() throws](/documentation/networkextension/nevpnconnection/startvpntunnel())
- [func startVPNTunnel(options: [String : NSObject]?) throws](/documentation/networkextension/nevpnconnection/startvpntunnel(options:))
- [let NEVPNConnectionStartOptionUsername: String](/documentation/networkextension/nevpnconnectionstartoptionusername)
- [let NEVPNConnectionStartOptionPassword: String](/documentation/networkextension/nevpnconnectionstartoptionpassword)
- [func stopVPNTunnel()](/documentation/networkextension/nevpnconnection/stopvpntunnel())

#### Getting VPN connection status

- [var manager: NEVPNManager](/documentation/networkextension/nevpnconnection/manager)
- [var status: NEVPNStatus](/documentation/networkextension/nevpnconnection/status)
- [NEVPNStatus](/documentation/networkextension/nevpnstatus)

##### Statuses

- [case disconnecting](/documentation/networkextension/nevpnstatus/disconnecting)
- [case reasserting](/documentation/networkextension/nevpnstatus/reasserting)
- [case connected](/documentation/networkextension/nevpnstatus/connected)
- [case connecting](/documentation/networkextension/nevpnstatus/connecting)
- [case disconnected](/documentation/networkextension/nevpnstatus/disconnected)
- [case invalid](/documentation/networkextension/nevpnstatus/invalid)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnstatus/init(rawvalue:))
- [var connectedDate: Date?](/documentation/networkextension/nevpnconnection/connecteddate)

#### Notifications

- [static let NEVPNStatusDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nevpnstatusdidchange)

#### Handling errors

- [func fetchLastDisconnectError(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nevpnconnection/fetchlastdisconnecterror(completionhandler:))
- [let NEVPNConnectionErrorDomain: String](/documentation/networkextension/nevpnconnectionerrordomain)
- [NEVPNConnectionError](/documentation/networkextension/nevpnconnectionerror)

##### General error codes

- [case overslept](/documentation/networkextension/nevpnconnectionerror/overslept)
- [case noNetworkAvailable](/documentation/networkextension/nevpnconnectionerror/nonetworkavailable)
- [case unrecoverableNetworkChange](/documentation/networkextension/nevpnconnectionerror/unrecoverablenetworkchange)
- [case configurationFailed](/documentation/networkextension/nevpnconnectionerror/configurationfailed)
- [case authenticationFailed](/documentation/networkextension/nevpnconnectionerror/authenticationfailed)
- [case configurationNotFound](/documentation/networkextension/nevpnconnectionerror/configurationnotfound)
- [case negotiationFailed](/documentation/networkextension/nevpnconnectionerror/negotiationfailed)

##### VPN server error codes

- [case serverAddressResolutionFailed](/documentation/networkextension/nevpnconnectionerror/serveraddressresolutionfailed)
- [case serverNotResponding](/documentation/networkextension/nevpnconnectionerror/servernotresponding)
- [case serverDead](/documentation/networkextension/nevpnconnectionerror/serverdead)
- [case serverDisconnected](/documentation/networkextension/nevpnconnectionerror/serverdisconnected)

##### Plugin error codes

- [case pluginFailed](/documentation/networkextension/nevpnconnectionerror/pluginfailed)
- [case pluginDisabled](/documentation/networkextension/nevpnconnectionerror/plugindisabled)

##### Client certificate error codes

- [case clientCertificateInvalid](/documentation/networkextension/nevpnconnectionerror/clientcertificateinvalid)
- [case clientCertificateNotYetValid](/documentation/networkextension/nevpnconnectionerror/clientcertificatenotyetvalid)
- [case clientCertificateExpired](/documentation/networkextension/nevpnconnectionerror/clientcertificateexpired)

##### Server certificate error codes

- [case serverCertificateInvalid](/documentation/networkextension/nevpnconnectionerror/servercertificateinvalid)
- [case serverCertificateNotYetValid](/documentation/networkextension/nevpnconnectionerror/servercertificatenotyetvalid)
- [case serverCertificateExpired](/documentation/networkextension/nevpnconnectionerror/servercertificateexpired)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnconnectionerror/init(rawvalue:))
- [Packet tunnel provider](/documentation/networkextension/packet-tunnel-provider)

### Essentials

- [Network Extensions Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.networkextension)

### Packet tunnel provider

- [NEPacketTunnelProvider](/documentation/networkextension/nepackettunnelprovider)

#### Managing the tunnel life cycle

- [func startTunnel(options: [String : NSObject]?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nepackettunnelprovider/starttunnel(options:completionhandler:))
- [func stopTunnel(with: NEProviderStopReason, completionHandler: () -> Void)](/documentation/networkextension/nepackettunnelprovider/stoptunnel(with:completionhandler:))
- [func cancelTunnelWithError((any Error)?)](/documentation/networkextension/nepackettunnelprovider/canceltunnelwitherror(_:))

#### Handling IP packets

- [var packetFlow: NEPacketTunnelFlow](/documentation/networkextension/nepackettunnelprovider/packetflow)

#### Creating network connections through the tunnel

- [func createTCPConnectionThroughTunnel(to: NWEndpoint, enableTLS: Bool, tlsParameters: NWTLSParameters?, delegate: Any?) -> NWTCPConnection](/documentation/networkextension/nepackettunnelprovider/createtcpconnectionthroughtunnel(to:enabletls:tlsparameters:delegate:))
- [func createUDPSessionThroughTunnel(to: NWEndpoint, from: NWHostEndpoint?) -> NWUDPSession](/documentation/networkextension/nepackettunnelprovider/createudpsessionthroughtunnel(to:from:))

#### Instance Properties

- [var virtualInterface: NWInterface?](/documentation/networkextension/nepackettunnelprovider/virtualinterface-7l3ol)
- [NETunnelProvider](/documentation/networkextension/netunnelprovider)

#### Getting the tunnel configuration

- [var protocolConfiguration: NEVPNProtocol](/documentation/networkextension/netunnelprovider/protocolconfiguration)
- [var routingMethod: NETunnelProviderRoutingMethod](/documentation/networkextension/netunnelprovider/routingmethod)
- [var appRules: [NEAppRule]?](/documentation/networkextension/netunnelprovider/apprules)

#### Configuring the tunnel interface

- [func setTunnelNetworkSettings(NETunnelNetworkSettings?, completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/netunnelprovider/settunnelnetworksettings(_:completionhandler:))

#### Communicating with the containing app

- [func handleAppMessage(Data, completionHandler: ((Data?) -> Void)?)](/documentation/networkextension/netunnelprovider/handleappmessage(_:completionhandler:))

#### Setting tunnel status

- [var reasserting: Bool](/documentation/networkextension/netunnelprovider/reasserting)

#### Errors

- [NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/code)

##### Error codes

- [case networkSettingsInvalid](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsinvalid)
- [case networkSettingsCanceled](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingscanceled)
- [case networkSettingsFailed](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netunnelprovidererror-swift.struct/code/init(rawvalue:))
- [let NETunnelProviderErrorDomain: String](/documentation/networkextension/netunnelprovidererrordomain)
- [NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/code)

##### Error codes

- [case networkSettingsInvalid](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsinvalid)
- [case networkSettingsCanceled](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingscanceled)
- [case networkSettingsFailed](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netunnelprovidererror-swift.struct/code/init(rawvalue:))
- [NEProvider](/documentation/networkextension/neprovider)

#### Handling sleep and wake

- [func sleep(completionHandler: () -> Void)](/documentation/networkextension/neprovider/sleep(completionhandler:))
- [func wake()](/documentation/networkextension/neprovider/wake())

#### Creating network connections

- [func createTCPConnection(to: NWEndpoint, enableTLS: Bool, tlsParameters: NWTLSParameters?, delegate: Any?) -> NWTCPConnection](/documentation/networkextension/neprovider/createtcpconnection(to:enabletls:tlsparameters:delegate:))
- [func createUDPSession(to: NWEndpoint, from: NWHostEndpoint?) -> NWUDPSession](/documentation/networkextension/neprovider/createudpsession(to:from:))

#### Monitoring the network state

- [var defaultPath: NWPath?](/documentation/networkextension/neprovider/defaultpath)

#### Supporting system extensions

- [class func startSystemExtensionMode()](/documentation/networkextension/neprovider/startsystemextensionmode())

#### Constants

- [NEProviderStopReason](/documentation/networkextension/neproviderstopreason)

##### Stop Reasons

- [case none](/documentation/networkextension/neproviderstopreason/none)
- [case userInitiated](/documentation/networkextension/neproviderstopreason/userinitiated)
- [case providerFailed](/documentation/networkextension/neproviderstopreason/providerfailed)
- [case noNetworkAvailable](/documentation/networkextension/neproviderstopreason/nonetworkavailable)
- [case unrecoverableNetworkChange](/documentation/networkextension/neproviderstopreason/unrecoverablenetworkchange)
- [case providerDisabled](/documentation/networkextension/neproviderstopreason/providerdisabled)
- [case authenticationCanceled](/documentation/networkextension/neproviderstopreason/authenticationcanceled)
- [case configurationFailed](/documentation/networkextension/neproviderstopreason/configurationfailed)
- [case idleTimeout](/documentation/networkextension/neproviderstopreason/idletimeout)
- [case configurationDisabled](/documentation/networkextension/neproviderstopreason/configurationdisabled)
- [case configurationRemoved](/documentation/networkextension/neproviderstopreason/configurationremoved)
- [case superceded](/documentation/networkextension/neproviderstopreason/superceded)
- [case userLogout](/documentation/networkextension/neproviderstopreason/userlogout)
- [case userSwitch](/documentation/networkextension/neproviderstopreason/userswitch)
- [case appUpdate](/documentation/networkextension/neproviderstopreason/appupdate)
- [case connectionFailed](/documentation/networkextension/neproviderstopreason/connectionfailed)
- [case sleep](/documentation/networkextension/neproviderstopreason/sleep)
- [case internalError](/documentation/networkextension/neproviderstopreason/internalerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neproviderstopreason/init(rawvalue:))

#### Displaying messages

- [func displayMessage(String, completionHandler: (Bool) -> Void)](/documentation/networkextension/neprovider/displaymessage(_:completionhandler:))
- [NEPacketTunnelNetworkSettings](/documentation/networkextension/nepackettunnelnetworksettings)

#### Accessing network properties

- [var ipv4Settings: NEIPv4Settings?](/documentation/networkextension/nepackettunnelnetworksettings/ipv4settings)
- [NEIPv4Settings](/documentation/networkextension/neipv4settings)

##### Initializing IPv4 settings

- [init(addresses: [String], subnetMasks: [String])](/documentation/networkextension/neipv4settings/init(addresses:subnetmasks:))

##### Accessing IPv4 properties

- [var addresses: [String]](/documentation/networkextension/neipv4settings/addresses)
- [var subnetMasks: [String]](/documentation/networkextension/neipv4settings/subnetmasks)
- [var router: String?](/documentation/networkextension/neipv4settings/router)

##### Routing network traffic

- [var includedRoutes: [NEIPv4Route]?](/documentation/networkextension/neipv4settings/includedroutes)
- [var excludedRoutes: [NEIPv4Route]?](/documentation/networkextension/neipv4settings/excludedroutes)
- [NEIPv4Route](/documentation/networkextension/neipv4route)

###### Creating an IPv4 Route

- [init(destinationAddress: String, subnetMask: String)](/documentation/networkextension/neipv4route/init(destinationaddress:subnetmask:))
- [class func `default`() -> NEIPv4Route](/documentation/networkextension/neipv4route/default())

###### Accessing IPv4 Route Properties

- [var destinationAddress: String](/documentation/networkextension/neipv4route/destinationaddress)
- [var destinationSubnetMask: String](/documentation/networkextension/neipv4route/destinationsubnetmask)
- [var gatewayAddress: String?](/documentation/networkextension/neipv4route/gatewayaddress)
- [var ipv6Settings: NEIPv6Settings?](/documentation/networkextension/nepackettunnelnetworksettings/ipv6settings)
- [NEIPv6Settings](/documentation/networkextension/neipv6settings)

##### Initializing IPv6 settings

- [init(addresses: [String], networkPrefixLengths: [NSNumber])](/documentation/networkextension/neipv6settings/init(addresses:networkprefixlengths:))

##### Accessing IPv6 properties

- [var addresses: [String]](/documentation/networkextension/neipv6settings/addresses)
- [var networkPrefixLengths: [NSNumber]](/documentation/networkextension/neipv6settings/networkprefixlengths)

##### Routing network traffic

- [var includedRoutes: [NEIPv6Route]?](/documentation/networkextension/neipv6settings/includedroutes)
- [var excludedRoutes: [NEIPv6Route]?](/documentation/networkextension/neipv6settings/excludedroutes)
- [NEIPv6Route](/documentation/networkextension/neipv6route)

###### Creating an IPv6 Route

- [init(destinationAddress: String, networkPrefixLength: NSNumber)](/documentation/networkextension/neipv6route/init(destinationaddress:networkprefixlength:))
- [class func `default`() -> NEIPv6Route](/documentation/networkextension/neipv6route/default())

###### Accessing IPv6 Route Properties

- [var destinationAddress: String](/documentation/networkextension/neipv6route/destinationaddress)
- [var destinationNetworkPrefixLength: NSNumber](/documentation/networkextension/neipv6route/destinationnetworkprefixlength)
- [var gatewayAddress: String?](/documentation/networkextension/neipv6route/gatewayaddress)
- [var tunnelOverheadBytes: NSNumber?](/documentation/networkextension/nepackettunnelnetworksettings/tunneloverheadbytes)
- [var mtu: NSNumber?](/documentation/networkextension/nepackettunnelnetworksettings/mtu)
- [NETunnelNetworkSettings](/documentation/networkextension/netunnelnetworksettings)

#### Initializing tunnel network settings

- [init(tunnelRemoteAddress: String)](/documentation/networkextension/netunnelnetworksettings/init(tunnelremoteaddress:))

#### Accessing tunnel network settings

- [var tunnelRemoteAddress: String](/documentation/networkextension/netunnelnetworksettings/tunnelremoteaddress)
- [var dnsSettings: NEDNSSettings?](/documentation/networkextension/netunnelnetworksettings/dnssettings)
- [NEDNSSettings](/documentation/networkextension/nednssettings)

##### Initializing DNS settings

- [init(servers: [String])](/documentation/networkextension/nednssettings/init(servers:))

##### Accessing DNS properties

- [var servers: [String]](/documentation/networkextension/nednssettings/servers)
- [var searchDomains: [String]?](/documentation/networkextension/nednssettings/searchdomains)
- [var domainName: String?](/documentation/networkextension/nednssettings/domainname)
- [var matchDomains: [String]?](/documentation/networkextension/nednssettings/matchdomains)
- [var matchDomainsNoSearch: Bool](/documentation/networkextension/nednssettings/matchdomainsnosearch)
- [var dnsProtocol: NEDNSProtocol](/documentation/networkextension/nednssettings/dnsprotocol)
- [NEDNSProtocol](/documentation/networkextension/nednsprotocol)

###### DNS protocols

- [case cleartext](/documentation/networkextension/nednsprotocol/cleartext)
- [case TLS](/documentation/networkextension/nednsprotocol/tls)
- [case HTTPS](/documentation/networkextension/nednsprotocol/https)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nednsprotocol/init(rawvalue:))

##### Instance Properties

- [var allowFailover: Bool](/documentation/networkextension/nednssettings/allowfailover)
- [var proxySettings: NEProxySettings?](/documentation/networkextension/netunnelnetworksettings/proxysettings)
- [NEProxySettings](/documentation/networkextension/neproxysettings)

##### Accessing Automatic Proxy Properties

- [var autoProxyConfigurationEnabled: Bool](/documentation/networkextension/neproxysettings/autoproxyconfigurationenabled)
- [var proxyAutoConfigurationURL: URL?](/documentation/networkextension/neproxysettings/proxyautoconfigurationurl)
- [var proxyAutoConfigurationJavaScript: String?](/documentation/networkextension/neproxysettings/proxyautoconfigurationjavascript)

##### Accessing Manual Proxy Properties

- [var httpEnabled: Bool](/documentation/networkextension/neproxysettings/httpenabled)
- [var httpServer: NEProxyServer?](/documentation/networkextension/neproxysettings/httpserver)
- [var httpsEnabled: Bool](/documentation/networkextension/neproxysettings/httpsenabled)
- [var httpsServer: NEProxyServer?](/documentation/networkextension/neproxysettings/httpsserver)
- [NEProxyServer](/documentation/networkextension/neproxyserver)

###### Initializing a Proxy Server

- [init(address: String, port: Int)](/documentation/networkextension/neproxyserver/init(address:port:))

###### Accessing Proxy Server Properties

- [var address: String](/documentation/networkextension/neproxyserver/address)
- [var port: Int](/documentation/networkextension/neproxyserver/port)
- [var authenticationRequired: Bool](/documentation/networkextension/neproxyserver/authenticationrequired)
- [var username: String?](/documentation/networkextension/neproxyserver/username)
- [var password: String?](/documentation/networkextension/neproxyserver/password)

##### Accessing General Proxy Properties

- [var excludeSimpleHostnames: Bool](/documentation/networkextension/neproxysettings/excludesimplehostnames)
- [var exceptionList: [String]?](/documentation/networkextension/neproxysettings/exceptionlist)
- [var matchDomains: [String]?](/documentation/networkextension/neproxysettings/matchdomains)
- [NEEthernetTunnelProvider](/documentation/networkextension/neethernettunnelprovider)
- [NEEthernetTunnelNetworkSettings](/documentation/networkextension/neethernettunnelnetworksettings)

#### Creating a settings instance

- [init(tunnelRemoteAddress: String, ethernetAddress: String, mtu: Int)](/documentation/networkextension/neethernettunnelnetworksettings/init(tunnelremoteaddress:ethernetaddress:mtu:))

#### Inspecting settings properties

- [var ethernetAddress: String](/documentation/networkextension/neethernettunnelnetworksettings/ethernetaddress)

### Packet handling

- [NEPacketTunnelFlow](/documentation/networkextension/nepackettunnelflow)

#### Handling IP packets

- [func readPacketObjects(completionHandler: ([NEPacket]) -> Void)](/documentation/networkextension/nepackettunnelflow/readpacketobjects(completionhandler:))
- [func writePacketObjects([NEPacket]) -> Bool](/documentation/networkextension/nepackettunnelflow/writepacketobjects(_:))
- [func readPackets(completionHandler: ([Data], [NSNumber]) -> Void)](/documentation/networkextension/nepackettunnelflow/readpackets(completionhandler:))
- [func writePackets([Data], withProtocols: [NSNumber]) -> Bool](/documentation/networkextension/nepackettunnelflow/writepackets(_:withprotocols:))
- [NEPacket](/documentation/networkextension/nepacket)

#### Initializing a packet

- [init(data: Data, protocolFamily: sa_family_t)](/documentation/networkextension/nepacket/init(data:protocolfamily:))

#### Accessing packet properties

- [var data: Data](/documentation/networkextension/nepacket/data)
- [var metadata: NEFlowMetaData?](/documentation/networkextension/nepacket/metadata)
- [var protocolFamily: sa_family_t](/documentation/networkextension/nepacket/protocolfamily)
- [var direction: NETrafficDirection](/documentation/networkextension/nepacket/direction)
- [NETrafficDirection](/documentation/networkextension/netrafficdirection)

##### Directions

- [case inbound](/documentation/networkextension/netrafficdirection/inbound)
- [case outbound](/documentation/networkextension/netrafficdirection/outbound)
- [case any](/documentation/networkextension/netrafficdirection/any)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netrafficdirection/init(rawvalue:))
- [In-Provider Networking](/documentation/networkextension/in-provider-networking)

#### TCP connections

- [NWTCPConnection](/documentation/networkextension/nwtcpconnection)

##### Monitoring the connection status

- [var state: NWTCPConnectionState](/documentation/networkextension/nwtcpconnection/state)
- [NWTCPConnectionState](/documentation/networkextension/nwtcpconnectionstate)

###### Connection States

- [case invalid](/documentation/networkextension/nwtcpconnectionstate/invalid)
- [case connecting](/documentation/networkextension/nwtcpconnectionstate/connecting)
- [case waiting](/documentation/networkextension/nwtcpconnectionstate/waiting)
- [case connected](/documentation/networkextension/nwtcpconnectionstate/connected)
- [case disconnected](/documentation/networkextension/nwtcpconnectionstate/disconnected)
- [case cancelled](/documentation/networkextension/nwtcpconnectionstate/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwtcpconnectionstate/init(rawvalue:))
- [var isViable: Bool](/documentation/networkextension/nwtcpconnection/isviable)
- [var error: (any Error)?](/documentation/networkextension/nwtcpconnection/error)

##### Transferring data

- [func readMinimumLength(Int, maximumLength: Int, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/readminimumlength(_:maximumlength:completionhandler:))
- [func readLength(Int, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/readlength(_:completionhandler:))
- [func write(Data, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/write(_:completionhandler:))
- [func writeClose()](/documentation/networkextension/nwtcpconnection/writeclose())

##### Canceling the connection

- [func cancel()](/documentation/networkextension/nwtcpconnection/cancel())

##### Responding to network changes

- [var hasBetterPath: Bool](/documentation/networkextension/nwtcpconnection/hasbetterpath)
- [init(upgradeFor: NWTCPConnection)](/documentation/networkextension/nwtcpconnection/init(upgradefor:))

##### Getting connection properties

- [var endpoint: NWEndpoint](/documentation/networkextension/nwtcpconnection/endpoint)
- [var localAddress: NWEndpoint?](/documentation/networkextension/nwtcpconnection/localaddress)
- [var remoteAddress: NWEndpoint?](/documentation/networkextension/nwtcpconnection/remoteaddress)
- [var connectedPath: NWPath?](/documentation/networkextension/nwtcpconnection/connectedpath)
- [var txtRecord: Data?](/documentation/networkextension/nwtcpconnection/txtrecord)
- [NWTLSParameters](/documentation/networkextension/nwtlsparameters)

##### Accessing TLS parameters

- [var tlsSessionID: Data?](/documentation/networkextension/nwtlsparameters/tlssessionid)
- [var sslCipherSuites: Set<NSNumber>?](/documentation/networkextension/nwtlsparameters/sslciphersuites)
- [var minimumSSLProtocolVersion: Int](/documentation/networkextension/nwtlsparameters/minimumsslprotocolversion)
- [var maximumSSLProtocolVersion: Int](/documentation/networkextension/nwtlsparameters/maximumsslprotocolversion)
- [NWTCPConnectionAuthenticationDelegate](/documentation/networkextension/nwtcpconnectionauthenticationdelegate)

##### Delegate methods

- [func shouldEvaluateTrust(for: NWTCPConnection) -> Bool](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/shouldevaluatetrust(for:))
- [func evaluateTrust(for: NWTCPConnection, peerCertificateChain: [Any], completionHandler: (SecTrust) -> Void)](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/evaluatetrust(for:peercertificatechain:completionhandler:))
- [func shouldProvideIdentity(for: NWTCPConnection) -> Bool](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/shouldprovideidentity(for:))
- [func provideIdentity(for: NWTCPConnection, completionHandler: (SecIdentity, [Any]) -> Void)](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/provideidentity(for:completionhandler:))

#### UDP sessions

- [NWUDPSession](/documentation/networkextension/nwudpsession)

##### Monitoring the session state

- [var state: NWUDPSessionState](/documentation/networkextension/nwudpsession/state)
- [NWUDPSessionState](/documentation/networkextension/nwudpsessionstate)

###### Session States

- [case invalid](/documentation/networkextension/nwudpsessionstate/invalid)
- [case waiting](/documentation/networkextension/nwudpsessionstate/waiting)
- [case preparing](/documentation/networkextension/nwudpsessionstate/preparing)
- [case ready](/documentation/networkextension/nwudpsessionstate/ready)
- [case failed](/documentation/networkextension/nwudpsessionstate/failed)
- [case cancelled](/documentation/networkextension/nwudpsessionstate/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwudpsessionstate/init(rawvalue:))
- [var isViable: Bool](/documentation/networkextension/nwudpsession/isviable)

##### Selecting remote endpoints

- [var resolvedEndpoint: NWEndpoint?](/documentation/networkextension/nwudpsession/resolvedendpoint)
- [func tryNextResolvedEndpoint()](/documentation/networkextension/nwudpsession/trynextresolvedendpoint())

##### Transferring data

- [func setReadHandler(([Data]?, (any Error)?) -> Void, maxDatagrams: Int)](/documentation/networkextension/nwudpsession/setreadhandler(_:maxdatagrams:))
- [func writeDatagram(Data, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwudpsession/writedatagram(_:completionhandler:))
- [func writeMultipleDatagrams([Data], completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwudpsession/writemultipledatagrams(_:completionhandler:))
- [var maximumDatagramLength: Int](/documentation/networkextension/nwudpsession/maximumdatagramlength)

##### Canceling the session

- [func cancel()](/documentation/networkextension/nwudpsession/cancel())

##### Responding to network changes

- [var hasBetterPath: Bool](/documentation/networkextension/nwudpsession/hasbetterpath)
- [init(upgradeFor: NWUDPSession)](/documentation/networkextension/nwudpsession/init(upgradefor:))

##### Getting session properties

- [var endpoint: NWEndpoint](/documentation/networkextension/nwudpsession/endpoint)
- [var currentPath: NWPath?](/documentation/networkextension/nwudpsession/currentpath)

#### Endpoints

- [NWHostEndpoint](/documentation/networkextension/nwhostendpoint)

##### Initializing host endpoints

- [convenience init(hostname: String, port: String)](/documentation/networkextension/nwhostendpoint/init(hostname:port:))

##### Getting endpoint properties

- [var hostname: String](/documentation/networkextension/nwhostendpoint/hostname)
- [var port: String](/documentation/networkextension/nwhostendpoint/port)
- [NWBonjourServiceEndpoint](/documentation/networkextension/nwbonjourserviceendpoint)

##### Initializing Bonjour service endpoints

- [convenience init(name: String, type: String, domain: String)](/documentation/networkextension/nwbonjourserviceendpoint/init(name:type:domain:))

##### Getting endpoint properties

- [var name: String](/documentation/networkextension/nwbonjourserviceendpoint/name)
- [var type: String](/documentation/networkextension/nwbonjourserviceendpoint/type)
- [var domain: String](/documentation/networkextension/nwbonjourserviceendpoint/domain)
- [NWEndpoint](/documentation/networkextension/nwendpoint)

#### Network path information

- [NWPath](/documentation/networkextension/nwpath)

##### Getting network path properties

- [var status: NWPathStatus](/documentation/networkextension/nwpath/status)
- [NWPathStatus](/documentation/networkextension/nwpathstatus)

###### Path Statuses

- [case invalid](/documentation/networkextension/nwpathstatus/invalid)
- [case satisfied](/documentation/networkextension/nwpathstatus/satisfied)
- [case unsatisfied](/documentation/networkextension/nwpathstatus/unsatisfied)
- [case satisfiable](/documentation/networkextension/nwpathstatus/satisfiable)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwpathstatus/init(rawvalue:))
- [var isExpensive: Bool](/documentation/networkextension/nwpath/isexpensive)
- [var isConstrained: Bool](/documentation/networkextension/nwpath/isconstrained)

##### Comparing network paths

- [func isEqual(to: NWPath) -> Bool](/documentation/networkextension/nwpath/isequal(to:))

### VPN configuration

- [NETunnelProviderManager](/documentation/networkextension/netunnelprovidermanager)

#### Managing tunnel configurations

- [class func loadAllFromPreferences(completionHandler: ([NETunnelProviderManager]?, (any Error)?) -> Void)](/documentation/networkextension/netunnelprovidermanager/loadallfrompreferences(completionhandler:))
- [func copyAppRules() -> [NEAppRule]?](/documentation/networkextension/netunnelprovidermanager/copyapprules())

#### Getting tunnel configuration properties

- [var routingMethod: NETunnelProviderRoutingMethod](/documentation/networkextension/netunnelprovidermanager/routingmethod)
- [NETunnelProviderRoutingMethod](/documentation/networkextension/netunnelproviderroutingmethod)

##### Routing Methods

- [case destinationIP](/documentation/networkextension/netunnelproviderroutingmethod/destinationip)
- [case sourceApplication](/documentation/networkextension/netunnelproviderroutingmethod/sourceapplication)
- [case networkRule](/documentation/networkextension/netunnelproviderroutingmethod/networkrule)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netunnelproviderroutingmethod/init(rawvalue:))

#### Configuring a per-app VPN

- [class func forPerAppVPN() -> Self](/documentation/networkextension/netunnelprovidermanager/forperappvpn())
- [var appRules: [NEAppRule]](/documentation/networkextension/netunnelprovidermanager/apprules)
- [var excludedDomains: [String]](/documentation/networkextension/netunnelprovidermanager/excludeddomains)
- [var associatedDomains: [String]](/documentation/networkextension/netunnelprovidermanager/associateddomains)
- [var calendarDomains: [String]](/documentation/networkextension/netunnelprovidermanager/calendardomains)
- [var contactsDomains: [String]](/documentation/networkextension/netunnelprovidermanager/contactsdomains)
- [var mailDomains: [String]](/documentation/networkextension/netunnelprovidermanager/maildomains)
- [var safariDomains: [String]](/documentation/networkextension/netunnelprovidermanager/safaridomains)
- [NEVPNManager](/documentation/networkextension/nevpnmanager)

#### Managing VPN configurations

- [class func shared() -> NEVPNManager](/documentation/networkextension/nevpnmanager/shared())
- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nevpnmanager/loadfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nevpnmanager/savetopreferences(completionhandler:))
- [func setAuthorization(AuthorizationRef)](/documentation/networkextension/nevpnmanager/setauthorization(_:))
- [func removeFromPreferences(completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nevpnmanager/removefrompreferences(completionhandler:))

#### Accessing VPN configuration properties

- [var isEnabled: Bool](/documentation/networkextension/nevpnmanager/isenabled)
- [var protocolConfiguration: NEVPNProtocol?](/documentation/networkextension/nevpnmanager/protocolconfiguration)
- [var `protocol`: NEVPNProtocol?](/documentation/networkextension/nevpnmanager/protocol)
- [var localizedDescription: String?](/documentation/networkextension/nevpnmanager/localizeddescription)
- [var isOnDemandEnabled: Bool](/documentation/networkextension/nevpnmanager/isondemandenabled)
- [var onDemandRules: [NEOnDemandRule]?](/documentation/networkextension/nevpnmanager/ondemandrules)

#### Connecting and disconnecting VPN

- [var connection: NEVPNConnection](/documentation/networkextension/nevpnmanager/connection)

#### Errors

- [NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/code)

##### Error codes

- [case configurationDisabled](/documentation/networkextension/nevpnerror-swift.struct/code/configurationdisabled)
- [case configurationInvalid](/documentation/networkextension/nevpnerror-swift.struct/code/configurationinvalid)
- [case connectionFailed](/documentation/networkextension/nevpnerror-swift.struct/code/connectionfailed)
- [case configurationStale](/documentation/networkextension/nevpnerror-swift.struct/code/configurationstale)
- [case configurationReadWriteFailed](/documentation/networkextension/nevpnerror-swift.struct/code/configurationreadwritefailed)
- [case configurationUnknown](/documentation/networkextension/nevpnerror-swift.struct/code/configurationunknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnerror-swift.struct/code/init(rawvalue:))
- [let NEVPNErrorDomain: String](/documentation/networkextension/nevpnerrordomain)
- [NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/code)

##### Error codes

- [case configurationDisabled](/documentation/networkextension/nevpnerror-swift.struct/code/configurationdisabled)
- [case configurationInvalid](/documentation/networkextension/nevpnerror-swift.struct/code/configurationinvalid)
- [case connectionFailed](/documentation/networkextension/nevpnerror-swift.struct/code/connectionfailed)
- [case configurationStale](/documentation/networkextension/nevpnerror-swift.struct/code/configurationstale)
- [case configurationReadWriteFailed](/documentation/networkextension/nevpnerror-swift.struct/code/configurationreadwritefailed)
- [case configurationUnknown](/documentation/networkextension/nevpnerror-swift.struct/code/configurationunknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnerror-swift.struct/code/init(rawvalue:))

#### Notifications

- [static let NEVPNConfigurationChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nevpnconfigurationchange)

#### Entitlements

- [Personal VPN Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.vpn.api)
- [NETunnelProviderProtocol](/documentation/networkextension/netunnelproviderprotocol)

#### Accessing the tunnel configuration

- [var providerConfiguration: [String : Any]?](/documentation/networkextension/netunnelproviderprotocol/providerconfiguration)
- [var providerBundleIdentifier: String?](/documentation/networkextension/netunnelproviderprotocol/providerbundleidentifier)
- [NEAppRule](/documentation/networkextension/neapprule)

#### Initializing an app rule

- [init(signingIdentifier: String)](/documentation/networkextension/neapprule/init(signingidentifier:))
- [init(signingIdentifier: String, designatedRequirement: String)](/documentation/networkextension/neapprule/init(signingidentifier:designatedrequirement:))

#### Accessing app rule properties

- [var matchSigningIdentifier: String](/documentation/networkextension/neapprule/matchsigningidentifier)
- [var matchDesignatedRequirement: String](/documentation/networkextension/neapprule/matchdesignatedrequirement)
- [var matchPath: String?](/documentation/networkextension/neapprule/matchpath)
- [var matchDomains: [Any]?](/documentation/networkextension/neapprule/matchdomains)
- [var matchTools: [NEAppRule]?](/documentation/networkextension/neapprule/matchtools)
- [VPN On Demand Rules](/documentation/networkextension/vpn-on-demand-rules)

#### Settings

- [NEOnDemandRuleConnect](/documentation/networkextension/neondemandruleconnect)
- [NEOnDemandRuleDisconnect](/documentation/networkextension/neondemandruledisconnect)
- [NEOnDemandRuleIgnore](/documentation/networkextension/neondemandruleignore)
- [NEOnDemandRuleEvaluateConnection](/documentation/networkextension/neondemandruleevaluateconnection)

##### Accessing connection rules

- [var connectionRules: [NEEvaluateConnectionRule]?](/documentation/networkextension/neondemandruleevaluateconnection/connectionrules)
- [NEEvaluateConnectionRule](/documentation/networkextension/neevaluateconnectionrule)

###### Initializing a Rule

- [init(matchDomains: [String], andAction: NEEvaluateConnectionRuleAction)](/documentation/networkextension/neevaluateconnectionrule/init(matchdomains:andaction:))

###### Accessing Rule Match Properties

- [var matchDomains: [String]](/documentation/networkextension/neevaluateconnectionrule/matchdomains)
- [var useDNSServers: [String]?](/documentation/networkextension/neevaluateconnectionrule/usednsservers)
- [var probeURL: URL?](/documentation/networkextension/neevaluateconnectionrule/probeurl)

###### Accessing the Rule Action

- [var action: NEEvaluateConnectionRuleAction](/documentation/networkextension/neevaluateconnectionrule/action)
- [NEEvaluateConnectionRuleAction](/documentation/networkextension/neevaluateconnectionruleaction)

###### Rule Actions

- [case connectIfNeeded](/documentation/networkextension/neevaluateconnectionruleaction/connectifneeded)
- [case neverConnect](/documentation/networkextension/neevaluateconnectionruleaction/neverconnect)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neevaluateconnectionruleaction/init(rawvalue:))
- [NEOnDemandRule](/documentation/networkextension/neondemandrule)

##### Accessing match parameters

- [var dnsSearchDomainMatch: [String]?](/documentation/networkextension/neondemandrule/dnssearchdomainmatch)
- [var dnsServerAddressMatch: [String]?](/documentation/networkextension/neondemandrule/dnsserveraddressmatch)
- [var interfaceTypeMatch: NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandrule/interfacetypematch)
- [NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandruleinterfacetype)

###### Interface Types

- [case any](/documentation/networkextension/neondemandruleinterfacetype/any)
- [case ethernet](/documentation/networkextension/neondemandruleinterfacetype/ethernet)
- [case wiFi](/documentation/networkextension/neondemandruleinterfacetype/wifi)
- [case cellular](/documentation/networkextension/neondemandruleinterfacetype/cellular)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleinterfacetype/init(rawvalue:))
- [var ssidMatch: [String]?](/documentation/networkextension/neondemandrule/ssidmatch)
- [var probeURL: URL?](/documentation/networkextension/neondemandrule/probeurl)

##### Accessing the rule action

- [var action: NEOnDemandRuleAction](/documentation/networkextension/neondemandrule/action)
- [NEOnDemandRuleAction](/documentation/networkextension/neondemandruleaction)

###### Rule Actions

- [case connect](/documentation/networkextension/neondemandruleaction/connect)
- [case disconnect](/documentation/networkextension/neondemandruleaction/disconnect)
- [case evaluateConnection](/documentation/networkextension/neondemandruleaction/evaluateconnection)
- [case ignore](/documentation/networkextension/neondemandruleaction/ignore)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleaction/init(rawvalue:))

### VPN control

- [NETunnelProviderSession](/documentation/networkextension/netunnelprovidersession)

#### Controlling the tunnel connection

- [func startTunnel(options: [String : Any]?) throws](/documentation/networkextension/netunnelprovidersession/starttunnel(options:))
- [func stopTunnel()](/documentation/networkextension/netunnelprovidersession/stoptunnel())

#### Communicating with the tunnel provider

- [func sendProviderMessage(Data, responseHandler: ((Data?) -> Void)?) throws](/documentation/networkextension/netunnelprovidersession/sendprovidermessage(_:responsehandler:))
- [NEVPNConnection](/documentation/networkextension/nevpnconnection)

#### Controlling the VPN connection

- [func startVPNTunnel() throws](/documentation/networkextension/nevpnconnection/startvpntunnel())
- [func startVPNTunnel(options: [String : NSObject]?) throws](/documentation/networkextension/nevpnconnection/startvpntunnel(options:))
- [let NEVPNConnectionStartOptionUsername: String](/documentation/networkextension/nevpnconnectionstartoptionusername)
- [let NEVPNConnectionStartOptionPassword: String](/documentation/networkextension/nevpnconnectionstartoptionpassword)
- [func stopVPNTunnel()](/documentation/networkextension/nevpnconnection/stopvpntunnel())

#### Getting VPN connection status

- [var manager: NEVPNManager](/documentation/networkextension/nevpnconnection/manager)
- [var status: NEVPNStatus](/documentation/networkextension/nevpnconnection/status)
- [NEVPNStatus](/documentation/networkextension/nevpnstatus)

##### Statuses

- [case disconnecting](/documentation/networkextension/nevpnstatus/disconnecting)
- [case reasserting](/documentation/networkextension/nevpnstatus/reasserting)
- [case connected](/documentation/networkextension/nevpnstatus/connected)
- [case connecting](/documentation/networkextension/nevpnstatus/connecting)
- [case disconnected](/documentation/networkextension/nevpnstatus/disconnected)
- [case invalid](/documentation/networkextension/nevpnstatus/invalid)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnstatus/init(rawvalue:))
- [var connectedDate: Date?](/documentation/networkextension/nevpnconnection/connecteddate)

#### Notifications

- [static let NEVPNStatusDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nevpnstatusdidchange)

#### Handling errors

- [func fetchLastDisconnectError(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nevpnconnection/fetchlastdisconnecterror(completionhandler:))
- [let NEVPNConnectionErrorDomain: String](/documentation/networkextension/nevpnconnectionerrordomain)
- [NEVPNConnectionError](/documentation/networkextension/nevpnconnectionerror)

##### General error codes

- [case overslept](/documentation/networkextension/nevpnconnectionerror/overslept)
- [case noNetworkAvailable](/documentation/networkextension/nevpnconnectionerror/nonetworkavailable)
- [case unrecoverableNetworkChange](/documentation/networkextension/nevpnconnectionerror/unrecoverablenetworkchange)
- [case configurationFailed](/documentation/networkextension/nevpnconnectionerror/configurationfailed)
- [case authenticationFailed](/documentation/networkextension/nevpnconnectionerror/authenticationfailed)
- [case configurationNotFound](/documentation/networkextension/nevpnconnectionerror/configurationnotfound)
- [case negotiationFailed](/documentation/networkextension/nevpnconnectionerror/negotiationfailed)

##### VPN server error codes

- [case serverAddressResolutionFailed](/documentation/networkextension/nevpnconnectionerror/serveraddressresolutionfailed)
- [case serverNotResponding](/documentation/networkextension/nevpnconnectionerror/servernotresponding)
- [case serverDead](/documentation/networkextension/nevpnconnectionerror/serverdead)
- [case serverDisconnected](/documentation/networkextension/nevpnconnectionerror/serverdisconnected)

##### Plugin error codes

- [case pluginFailed](/documentation/networkextension/nevpnconnectionerror/pluginfailed)
- [case pluginDisabled](/documentation/networkextension/nevpnconnectionerror/plugindisabled)

##### Client certificate error codes

- [case clientCertificateInvalid](/documentation/networkextension/nevpnconnectionerror/clientcertificateinvalid)
- [case clientCertificateNotYetValid](/documentation/networkextension/nevpnconnectionerror/clientcertificatenotyetvalid)
- [case clientCertificateExpired](/documentation/networkextension/nevpnconnectionerror/clientcertificateexpired)

##### Server certificate error codes

- [case serverCertificateInvalid](/documentation/networkextension/nevpnconnectionerror/servercertificateinvalid)
- [case serverCertificateNotYetValid](/documentation/networkextension/nevpnconnectionerror/servercertificatenotyetvalid)
- [case serverCertificateExpired](/documentation/networkextension/nevpnconnectionerror/servercertificateexpired)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnconnectionerror/init(rawvalue:))
- [App proxy provider](/documentation/networkextension/app-proxy-provider)

### Essentials

- [Network Extensions Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.networkextension)

### App proxy provider

- [NEAppProxyProvider](/documentation/networkextension/neappproxyprovider)

#### Managing the app proxy life cycle

- [func startProxy(options: [String : Any]?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyprovider/startproxy(options:completionhandler:))
- [func stopProxy(with: NEProviderStopReason, completionHandler: () -> Void)](/documentation/networkextension/neappproxyprovider/stopproxy(with:completionhandler:))
- [func cancelProxyWithError((any Error)?)](/documentation/networkextension/neappproxyprovider/cancelproxywitherror(_:))

#### Handling proxied flows

- [func handleNewFlow(NEAppProxyFlow) -> Bool](/documentation/networkextension/neappproxyprovider/handlenewflow(_:))
- [func handleNewUDPFlow(NEAppProxyUDPFlow, initialRemoteEndpoint: NWEndpoint) -> Bool](/documentation/networkextension/neappproxyprovider/handlenewudpflow(_:initialremoteendpoint:))
- [NETunnelProvider](/documentation/networkextension/netunnelprovider)

#### Getting the tunnel configuration

- [var protocolConfiguration: NEVPNProtocol](/documentation/networkextension/netunnelprovider/protocolconfiguration)
- [var routingMethod: NETunnelProviderRoutingMethod](/documentation/networkextension/netunnelprovider/routingmethod)
- [var appRules: [NEAppRule]?](/documentation/networkextension/netunnelprovider/apprules)

#### Configuring the tunnel interface

- [func setTunnelNetworkSettings(NETunnelNetworkSettings?, completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/netunnelprovider/settunnelnetworksettings(_:completionhandler:))

#### Communicating with the containing app

- [func handleAppMessage(Data, completionHandler: ((Data?) -> Void)?)](/documentation/networkextension/netunnelprovider/handleappmessage(_:completionhandler:))

#### Setting tunnel status

- [var reasserting: Bool](/documentation/networkextension/netunnelprovider/reasserting)

#### Errors

- [NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/code)

##### Error codes

- [case networkSettingsInvalid](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsinvalid)
- [case networkSettingsCanceled](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingscanceled)
- [case networkSettingsFailed](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netunnelprovidererror-swift.struct/code/init(rawvalue:))
- [let NETunnelProviderErrorDomain: String](/documentation/networkextension/netunnelprovidererrordomain)
- [NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/code)

##### Error codes

- [case networkSettingsInvalid](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsinvalid)
- [case networkSettingsCanceled](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingscanceled)
- [case networkSettingsFailed](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netunnelprovidererror-swift.struct/code/init(rawvalue:))
- [NEProvider](/documentation/networkextension/neprovider)

#### Handling sleep and wake

- [func sleep(completionHandler: () -> Void)](/documentation/networkextension/neprovider/sleep(completionhandler:))
- [func wake()](/documentation/networkextension/neprovider/wake())

#### Creating network connections

- [func createTCPConnection(to: NWEndpoint, enableTLS: Bool, tlsParameters: NWTLSParameters?, delegate: Any?) -> NWTCPConnection](/documentation/networkextension/neprovider/createtcpconnection(to:enabletls:tlsparameters:delegate:))
- [func createUDPSession(to: NWEndpoint, from: NWHostEndpoint?) -> NWUDPSession](/documentation/networkextension/neprovider/createudpsession(to:from:))

#### Monitoring the network state

- [var defaultPath: NWPath?](/documentation/networkextension/neprovider/defaultpath)

#### Supporting system extensions

- [class func startSystemExtensionMode()](/documentation/networkextension/neprovider/startsystemextensionmode())

#### Constants

- [NEProviderStopReason](/documentation/networkextension/neproviderstopreason)

##### Stop Reasons

- [case none](/documentation/networkextension/neproviderstopreason/none)
- [case userInitiated](/documentation/networkextension/neproviderstopreason/userinitiated)
- [case providerFailed](/documentation/networkextension/neproviderstopreason/providerfailed)
- [case noNetworkAvailable](/documentation/networkextension/neproviderstopreason/nonetworkavailable)
- [case unrecoverableNetworkChange](/documentation/networkextension/neproviderstopreason/unrecoverablenetworkchange)
- [case providerDisabled](/documentation/networkextension/neproviderstopreason/providerdisabled)
- [case authenticationCanceled](/documentation/networkextension/neproviderstopreason/authenticationcanceled)
- [case configurationFailed](/documentation/networkextension/neproviderstopreason/configurationfailed)
- [case idleTimeout](/documentation/networkextension/neproviderstopreason/idletimeout)
- [case configurationDisabled](/documentation/networkextension/neproviderstopreason/configurationdisabled)
- [case configurationRemoved](/documentation/networkextension/neproviderstopreason/configurationremoved)
- [case superceded](/documentation/networkextension/neproviderstopreason/superceded)
- [case userLogout](/documentation/networkextension/neproviderstopreason/userlogout)
- [case userSwitch](/documentation/networkextension/neproviderstopreason/userswitch)
- [case appUpdate](/documentation/networkextension/neproviderstopreason/appupdate)
- [case connectionFailed](/documentation/networkextension/neproviderstopreason/connectionfailed)
- [case sleep](/documentation/networkextension/neproviderstopreason/sleep)
- [case internalError](/documentation/networkextension/neproviderstopreason/internalerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neproviderstopreason/init(rawvalue:))

#### Displaying messages

- [func displayMessage(String, completionHandler: (Bool) -> Void)](/documentation/networkextension/neprovider/displaymessage(_:completionhandler:))
- [NETunnelNetworkSettings](/documentation/networkextension/netunnelnetworksettings)

#### Initializing tunnel network settings

- [init(tunnelRemoteAddress: String)](/documentation/networkextension/netunnelnetworksettings/init(tunnelremoteaddress:))

#### Accessing tunnel network settings

- [var tunnelRemoteAddress: String](/documentation/networkextension/netunnelnetworksettings/tunnelremoteaddress)
- [var dnsSettings: NEDNSSettings?](/documentation/networkextension/netunnelnetworksettings/dnssettings)
- [NEDNSSettings](/documentation/networkextension/nednssettings)

##### Initializing DNS settings

- [init(servers: [String])](/documentation/networkextension/nednssettings/init(servers:))

##### Accessing DNS properties

- [var servers: [String]](/documentation/networkextension/nednssettings/servers)
- [var searchDomains: [String]?](/documentation/networkextension/nednssettings/searchdomains)
- [var domainName: String?](/documentation/networkextension/nednssettings/domainname)
- [var matchDomains: [String]?](/documentation/networkextension/nednssettings/matchdomains)
- [var matchDomainsNoSearch: Bool](/documentation/networkextension/nednssettings/matchdomainsnosearch)
- [var dnsProtocol: NEDNSProtocol](/documentation/networkextension/nednssettings/dnsprotocol)
- [NEDNSProtocol](/documentation/networkextension/nednsprotocol)

###### DNS protocols

- [case cleartext](/documentation/networkextension/nednsprotocol/cleartext)
- [case TLS](/documentation/networkextension/nednsprotocol/tls)
- [case HTTPS](/documentation/networkextension/nednsprotocol/https)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nednsprotocol/init(rawvalue:))

##### Instance Properties

- [var allowFailover: Bool](/documentation/networkextension/nednssettings/allowfailover)
- [var proxySettings: NEProxySettings?](/documentation/networkextension/netunnelnetworksettings/proxysettings)
- [NEProxySettings](/documentation/networkextension/neproxysettings)

##### Accessing Automatic Proxy Properties

- [var autoProxyConfigurationEnabled: Bool](/documentation/networkextension/neproxysettings/autoproxyconfigurationenabled)
- [var proxyAutoConfigurationURL: URL?](/documentation/networkextension/neproxysettings/proxyautoconfigurationurl)
- [var proxyAutoConfigurationJavaScript: String?](/documentation/networkextension/neproxysettings/proxyautoconfigurationjavascript)

##### Accessing Manual Proxy Properties

- [var httpEnabled: Bool](/documentation/networkextension/neproxysettings/httpenabled)
- [var httpServer: NEProxyServer?](/documentation/networkextension/neproxysettings/httpserver)
- [var httpsEnabled: Bool](/documentation/networkextension/neproxysettings/httpsenabled)
- [var httpsServer: NEProxyServer?](/documentation/networkextension/neproxysettings/httpsserver)
- [NEProxyServer](/documentation/networkextension/neproxyserver)

###### Initializing a Proxy Server

- [init(address: String, port: Int)](/documentation/networkextension/neproxyserver/init(address:port:))

###### Accessing Proxy Server Properties

- [var address: String](/documentation/networkextension/neproxyserver/address)
- [var port: Int](/documentation/networkextension/neproxyserver/port)
- [var authenticationRequired: Bool](/documentation/networkextension/neproxyserver/authenticationrequired)
- [var username: String?](/documentation/networkextension/neproxyserver/username)
- [var password: String?](/documentation/networkextension/neproxyserver/password)

##### Accessing General Proxy Properties

- [var excludeSimpleHostnames: Bool](/documentation/networkextension/neproxysettings/excludesimplehostnames)
- [var exceptionList: [String]?](/documentation/networkextension/neproxysettings/exceptionlist)
- [var matchDomains: [String]?](/documentation/networkextension/neproxysettings/matchdomains)

### Flow handling

- [NEAppProxyTCPFlow](/documentation/networkextension/neappproxytcpflow)

#### Handling flow data

- [func write(Data, withCompletionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxytcpflow/write(_:withcompletionhandler:))
- [func readData(completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/neappproxytcpflow/readdata(completionhandler:))

#### Getting flow information

- [var remoteEndpoint: NWEndpoint](/documentation/networkextension/neappproxytcpflow/remoteendpoint)

#### Instance Properties

- [var remoteFlowEndpoint: NWEndpoint](/documentation/networkextension/neappproxytcpflow/remoteflowendpoint-4r7v1)
- [NEAppProxyUDPFlow](/documentation/networkextension/neappproxyudpflow)

#### Handling flow data

- [func readDatagrams(completionHandler: ([Data]?, [NWEndpoint]?, (any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/readdatagrams(completionhandler:)-9z8gw)
- [func writeDatagrams([Data], sentBy: [NWEndpoint], completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/writedatagrams(_:sentby:completionhandler:))

#### Getting flow information

- [var localEndpoint: NWEndpoint?](/documentation/networkextension/neappproxyudpflow/localendpoint)

#### Instance Properties

- [var localFlowEndpoint: NWEndpoint?](/documentation/networkextension/neappproxyudpflow/localflowendpoint-7ukb6)

#### Instance Methods

- [func readDatagrams() async -> ([(Data, NWEndpoint)]?, (any Error)?)](/documentation/networkextension/neappproxyudpflow/readdatagrams())
- [func readDatagrams(completionHandler: ([(Data, NWEndpoint)]?, (any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/readdatagrams(completionhandler:)-71k28)
- [func writeDatagrams([(Data, NWEndpoint)]) async throws](/documentation/networkextension/neappproxyudpflow/writedatagrams(_:))
- [func writeDatagrams([(Data, NWEndpoint)], completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/writedatagrams(_:completionhandler:))
- [NEAppProxyFlow](/documentation/networkextension/neappproxyflow)

#### Managing the flow life cycle

- [func open(withLocalEndpoint: NWHostEndpoint?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyflow/open(withlocalendpoint:completionhandler:))
- [func closeReadWithError((any Error)?)](/documentation/networkextension/neappproxyflow/closereadwitherror(_:))
- [func closeWriteWithError((any Error)?)](/documentation/networkextension/neappproxyflow/closewritewitherror(_:))

#### Accessing flow information

- [var metaData: NEFlowMetaData](/documentation/networkextension/neappproxyflow/metadata)
- [func setMetadata(nw_parameters_t)](/documentation/networkextension/neappproxyflow/setmetadata(_:))
- [nw_parameters_t](/documentation/network/nw_parameters_t)
- [var isBound: Bool](/documentation/networkextension/neappproxyflow/isbound)
- [var networkInterface: nw_interface_t?](/documentation/networkextension/neappproxyflow/networkinterface)
- [nw_interface_type_t](/documentation/network/nw_interface_type_t)
- [var remoteHostname: String?](/documentation/networkextension/neappproxyflow/remotehostname)

#### Errors

- [NEAppProxyFlowError](/documentation/networkextension/neappproxyflowerror-swift.struct)

##### Accessing error properties

- [NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/code)

###### Error Codes

- [case notConnected](/documentation/networkextension/neappproxyflowerror-swift.struct/code/notconnected)
- [case peerReset](/documentation/networkextension/neappproxyflowerror-swift.struct/code/peerreset)
- [case hostUnreachable](/documentation/networkextension/neappproxyflowerror-swift.struct/code/hostunreachable)
- [case invalidArgument](/documentation/networkextension/neappproxyflowerror-swift.struct/code/invalidargument)
- [case aborted](/documentation/networkextension/neappproxyflowerror-swift.struct/code/aborted)
- [case refused](/documentation/networkextension/neappproxyflowerror-swift.struct/code/refused)
- [case timedOut](/documentation/networkextension/neappproxyflowerror-swift.struct/code/timedout)
- [case `internal`](/documentation/networkextension/neappproxyflowerror-swift.struct/code/internal)
- [case datagramTooLarge](/documentation/networkextension/neappproxyflowerror-swift.struct/code/datagramtoolarge)
- [case readAlreadyPending](/documentation/networkextension/neappproxyflowerror-swift.struct/code/readalreadypending)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neappproxyflowerror-swift.struct/code/init(rawvalue:))

##### Error codes

- [static var notConnected: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/notconnected)
- [static var peerReset: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/peerreset)
- [static var hostUnreachable: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/hostunreachable)
- [static var invalidArgument: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/invalidargument)
- [static var aborted: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/aborted)
- [static var refused: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/refused)
- [static var timedOut: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/timedout)
- [static var `internal`: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/internal)
- [static var datagramTooLarge: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/datagramtoolarge)
- [static var readAlreadyPending: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/readalreadypending)

##### Type Properties

- [static var errorDomain: String](/documentation/networkextension/neappproxyflowerror-swift.struct/errordomain)
- [let NEAppProxyErrorDomain: String](/documentation/networkextension/neappproxyerrordomain)
- [NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/code)

##### Error Codes

- [case notConnected](/documentation/networkextension/neappproxyflowerror-swift.struct/code/notconnected)
- [case peerReset](/documentation/networkextension/neappproxyflowerror-swift.struct/code/peerreset)
- [case hostUnreachable](/documentation/networkextension/neappproxyflowerror-swift.struct/code/hostunreachable)
- [case invalidArgument](/documentation/networkextension/neappproxyflowerror-swift.struct/code/invalidargument)
- [case aborted](/documentation/networkextension/neappproxyflowerror-swift.struct/code/aborted)
- [case refused](/documentation/networkextension/neappproxyflowerror-swift.struct/code/refused)
- [case timedOut](/documentation/networkextension/neappproxyflowerror-swift.struct/code/timedout)
- [case `internal`](/documentation/networkextension/neappproxyflowerror-swift.struct/code/internal)
- [case datagramTooLarge](/documentation/networkextension/neappproxyflowerror-swift.struct/code/datagramtoolarge)
- [case readAlreadyPending](/documentation/networkextension/neappproxyflowerror-swift.struct/code/readalreadypending)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neappproxyflowerror-swift.struct/code/init(rawvalue:))
- [NEAppProxyFlowError](/documentation/networkextension/neappproxyflowerror-swift.struct)

##### Accessing error properties

- [NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/code)

###### Error Codes

- [case notConnected](/documentation/networkextension/neappproxyflowerror-swift.struct/code/notconnected)
- [case peerReset](/documentation/networkextension/neappproxyflowerror-swift.struct/code/peerreset)
- [case hostUnreachable](/documentation/networkextension/neappproxyflowerror-swift.struct/code/hostunreachable)
- [case invalidArgument](/documentation/networkextension/neappproxyflowerror-swift.struct/code/invalidargument)
- [case aborted](/documentation/networkextension/neappproxyflowerror-swift.struct/code/aborted)
- [case refused](/documentation/networkextension/neappproxyflowerror-swift.struct/code/refused)
- [case timedOut](/documentation/networkextension/neappproxyflowerror-swift.struct/code/timedout)
- [case `internal`](/documentation/networkextension/neappproxyflowerror-swift.struct/code/internal)
- [case datagramTooLarge](/documentation/networkextension/neappproxyflowerror-swift.struct/code/datagramtoolarge)
- [case readAlreadyPending](/documentation/networkextension/neappproxyflowerror-swift.struct/code/readalreadypending)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neappproxyflowerror-swift.struct/code/init(rawvalue:))

##### Error codes

- [static var notConnected: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/notconnected)
- [static var peerReset: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/peerreset)
- [static var hostUnreachable: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/hostunreachable)
- [static var invalidArgument: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/invalidargument)
- [static var aborted: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/aborted)
- [static var refused: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/refused)
- [static var timedOut: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/timedout)
- [static var `internal`: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/internal)
- [static var datagramTooLarge: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/datagramtoolarge)
- [static var readAlreadyPending: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/readalreadypending)

##### Type Properties

- [static var errorDomain: String](/documentation/networkextension/neappproxyflowerror-swift.struct/errordomain)

#### Instance Properties

- [var interface: NWInterface?](/documentation/networkextension/neappproxyflow/interface)

#### Instance Methods

- [func open(withLocalFlowEndpoint: NWEndpoint?) async throws](/documentation/networkextension/neappproxyflow/open(withlocalflowendpoint:))
- [func open(withLocalFlowEndpoint: NWEndpoint?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyflow/open(withlocalflowendpoint:completionhandler:))
- [func setMetadata(on: NWParameters)](/documentation/networkextension/neappproxyflow/setmetadata(on:))
- [NEFlowMetaData](/documentation/networkextension/neflowmetadata)

#### Getting source app information

- [var sourceAppUniqueIdentifier: Data](/documentation/networkextension/neflowmetadata/sourceappuniqueidentifier)
- [var sourceAppSigningIdentifier: String](/documentation/networkextension/neflowmetadata/sourceappsigningidentifier)
- [var sourceAppAuditToken: Data?](/documentation/networkextension/neflowmetadata/sourceappaudittoken)

#### Getting flow information

- [var filterFlowIdentifier: UUID?](/documentation/networkextension/neflowmetadata/filterflowidentifier)
- [In-Provider Networking](/documentation/networkextension/in-provider-networking)

#### TCP connections

- [NWTCPConnection](/documentation/networkextension/nwtcpconnection)

##### Monitoring the connection status

- [var state: NWTCPConnectionState](/documentation/networkextension/nwtcpconnection/state)
- [NWTCPConnectionState](/documentation/networkextension/nwtcpconnectionstate)

###### Connection States

- [case invalid](/documentation/networkextension/nwtcpconnectionstate/invalid)
- [case connecting](/documentation/networkextension/nwtcpconnectionstate/connecting)
- [case waiting](/documentation/networkextension/nwtcpconnectionstate/waiting)
- [case connected](/documentation/networkextension/nwtcpconnectionstate/connected)
- [case disconnected](/documentation/networkextension/nwtcpconnectionstate/disconnected)
- [case cancelled](/documentation/networkextension/nwtcpconnectionstate/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwtcpconnectionstate/init(rawvalue:))
- [var isViable: Bool](/documentation/networkextension/nwtcpconnection/isviable)
- [var error: (any Error)?](/documentation/networkextension/nwtcpconnection/error)

##### Transferring data

- [func readMinimumLength(Int, maximumLength: Int, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/readminimumlength(_:maximumlength:completionhandler:))
- [func readLength(Int, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/readlength(_:completionhandler:))
- [func write(Data, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwtcpconnection/write(_:completionhandler:))
- [func writeClose()](/documentation/networkextension/nwtcpconnection/writeclose())

##### Canceling the connection

- [func cancel()](/documentation/networkextension/nwtcpconnection/cancel())

##### Responding to network changes

- [var hasBetterPath: Bool](/documentation/networkextension/nwtcpconnection/hasbetterpath)
- [init(upgradeFor: NWTCPConnection)](/documentation/networkextension/nwtcpconnection/init(upgradefor:))

##### Getting connection properties

- [var endpoint: NWEndpoint](/documentation/networkextension/nwtcpconnection/endpoint)
- [var localAddress: NWEndpoint?](/documentation/networkextension/nwtcpconnection/localaddress)
- [var remoteAddress: NWEndpoint?](/documentation/networkextension/nwtcpconnection/remoteaddress)
- [var connectedPath: NWPath?](/documentation/networkextension/nwtcpconnection/connectedpath)
- [var txtRecord: Data?](/documentation/networkextension/nwtcpconnection/txtrecord)
- [NWTLSParameters](/documentation/networkextension/nwtlsparameters)

##### Accessing TLS parameters

- [var tlsSessionID: Data?](/documentation/networkextension/nwtlsparameters/tlssessionid)
- [var sslCipherSuites: Set<NSNumber>?](/documentation/networkextension/nwtlsparameters/sslciphersuites)
- [var minimumSSLProtocolVersion: Int](/documentation/networkextension/nwtlsparameters/minimumsslprotocolversion)
- [var maximumSSLProtocolVersion: Int](/documentation/networkextension/nwtlsparameters/maximumsslprotocolversion)
- [NWTCPConnectionAuthenticationDelegate](/documentation/networkextension/nwtcpconnectionauthenticationdelegate)

##### Delegate methods

- [func shouldEvaluateTrust(for: NWTCPConnection) -> Bool](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/shouldevaluatetrust(for:))
- [func evaluateTrust(for: NWTCPConnection, peerCertificateChain: [Any], completionHandler: (SecTrust) -> Void)](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/evaluatetrust(for:peercertificatechain:completionhandler:))
- [func shouldProvideIdentity(for: NWTCPConnection) -> Bool](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/shouldprovideidentity(for:))
- [func provideIdentity(for: NWTCPConnection, completionHandler: (SecIdentity, [Any]) -> Void)](/documentation/networkextension/nwtcpconnectionauthenticationdelegate/provideidentity(for:completionhandler:))

#### UDP sessions

- [NWUDPSession](/documentation/networkextension/nwudpsession)

##### Monitoring the session state

- [var state: NWUDPSessionState](/documentation/networkextension/nwudpsession/state)
- [NWUDPSessionState](/documentation/networkextension/nwudpsessionstate)

###### Session States

- [case invalid](/documentation/networkextension/nwudpsessionstate/invalid)
- [case waiting](/documentation/networkextension/nwudpsessionstate/waiting)
- [case preparing](/documentation/networkextension/nwudpsessionstate/preparing)
- [case ready](/documentation/networkextension/nwudpsessionstate/ready)
- [case failed](/documentation/networkextension/nwudpsessionstate/failed)
- [case cancelled](/documentation/networkextension/nwudpsessionstate/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwudpsessionstate/init(rawvalue:))
- [var isViable: Bool](/documentation/networkextension/nwudpsession/isviable)

##### Selecting remote endpoints

- [var resolvedEndpoint: NWEndpoint?](/documentation/networkextension/nwudpsession/resolvedendpoint)
- [func tryNextResolvedEndpoint()](/documentation/networkextension/nwudpsession/trynextresolvedendpoint())

##### Transferring data

- [func setReadHandler(([Data]?, (any Error)?) -> Void, maxDatagrams: Int)](/documentation/networkextension/nwudpsession/setreadhandler(_:maxdatagrams:))
- [func writeDatagram(Data, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwudpsession/writedatagram(_:completionhandler:))
- [func writeMultipleDatagrams([Data], completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nwudpsession/writemultipledatagrams(_:completionhandler:))
- [var maximumDatagramLength: Int](/documentation/networkextension/nwudpsession/maximumdatagramlength)

##### Canceling the session

- [func cancel()](/documentation/networkextension/nwudpsession/cancel())

##### Responding to network changes

- [var hasBetterPath: Bool](/documentation/networkextension/nwudpsession/hasbetterpath)
- [init(upgradeFor: NWUDPSession)](/documentation/networkextension/nwudpsession/init(upgradefor:))

##### Getting session properties

- [var endpoint: NWEndpoint](/documentation/networkextension/nwudpsession/endpoint)
- [var currentPath: NWPath?](/documentation/networkextension/nwudpsession/currentpath)

#### Endpoints

- [NWHostEndpoint](/documentation/networkextension/nwhostendpoint)

##### Initializing host endpoints

- [convenience init(hostname: String, port: String)](/documentation/networkextension/nwhostendpoint/init(hostname:port:))

##### Getting endpoint properties

- [var hostname: String](/documentation/networkextension/nwhostendpoint/hostname)
- [var port: String](/documentation/networkextension/nwhostendpoint/port)
- [NWBonjourServiceEndpoint](/documentation/networkextension/nwbonjourserviceendpoint)

##### Initializing Bonjour service endpoints

- [convenience init(name: String, type: String, domain: String)](/documentation/networkextension/nwbonjourserviceendpoint/init(name:type:domain:))

##### Getting endpoint properties

- [var name: String](/documentation/networkextension/nwbonjourserviceendpoint/name)
- [var type: String](/documentation/networkextension/nwbonjourserviceendpoint/type)
- [var domain: String](/documentation/networkextension/nwbonjourserviceendpoint/domain)
- [NWEndpoint](/documentation/networkextension/nwendpoint)

#### Network path information

- [NWPath](/documentation/networkextension/nwpath)

##### Getting network path properties

- [var status: NWPathStatus](/documentation/networkextension/nwpath/status)
- [NWPathStatus](/documentation/networkextension/nwpathstatus)

###### Path Statuses

- [case invalid](/documentation/networkextension/nwpathstatus/invalid)
- [case satisfied](/documentation/networkextension/nwpathstatus/satisfied)
- [case unsatisfied](/documentation/networkextension/nwpathstatus/unsatisfied)
- [case satisfiable](/documentation/networkextension/nwpathstatus/satisfiable)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nwpathstatus/init(rawvalue:))
- [var isExpensive: Bool](/documentation/networkextension/nwpath/isexpensive)
- [var isConstrained: Bool](/documentation/networkextension/nwpath/isconstrained)

##### Comparing network paths

- [func isEqual(to: NWPath) -> Bool](/documentation/networkextension/nwpath/isequal(to:))
- [Handling Flow Copying](/documentation/networkextension/handling-flow-copying)

### VPN configuration

- [NEAppProxyProviderManager](/documentation/networkextension/neappproxyprovidermanager)

#### Loading the app proxy configuration

- [class func loadAllFromPreferences(completionHandler: ([NEAppProxyProviderManager]?, (any Error)?) -> Void)](/documentation/networkextension/neappproxyprovidermanager/loadallfrompreferences(completionhandler:))
- [NETunnelProviderManager](/documentation/networkextension/netunnelprovidermanager)

#### Managing tunnel configurations

- [class func loadAllFromPreferences(completionHandler: ([NETunnelProviderManager]?, (any Error)?) -> Void)](/documentation/networkextension/netunnelprovidermanager/loadallfrompreferences(completionhandler:))
- [func copyAppRules() -> [NEAppRule]?](/documentation/networkextension/netunnelprovidermanager/copyapprules())

#### Getting tunnel configuration properties

- [var routingMethod: NETunnelProviderRoutingMethod](/documentation/networkextension/netunnelprovidermanager/routingmethod)
- [NETunnelProviderRoutingMethod](/documentation/networkextension/netunnelproviderroutingmethod)

##### Routing Methods

- [case destinationIP](/documentation/networkextension/netunnelproviderroutingmethod/destinationip)
- [case sourceApplication](/documentation/networkextension/netunnelproviderroutingmethod/sourceapplication)
- [case networkRule](/documentation/networkextension/netunnelproviderroutingmethod/networkrule)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netunnelproviderroutingmethod/init(rawvalue:))

#### Configuring a per-app VPN

- [class func forPerAppVPN() -> Self](/documentation/networkextension/netunnelprovidermanager/forperappvpn())
- [var appRules: [NEAppRule]](/documentation/networkextension/netunnelprovidermanager/apprules)
- [var excludedDomains: [String]](/documentation/networkextension/netunnelprovidermanager/excludeddomains)
- [var associatedDomains: [String]](/documentation/networkextension/netunnelprovidermanager/associateddomains)
- [var calendarDomains: [String]](/documentation/networkextension/netunnelprovidermanager/calendardomains)
- [var contactsDomains: [String]](/documentation/networkextension/netunnelprovidermanager/contactsdomains)
- [var mailDomains: [String]](/documentation/networkextension/netunnelprovidermanager/maildomains)
- [var safariDomains: [String]](/documentation/networkextension/netunnelprovidermanager/safaridomains)
- [NEVPNManager](/documentation/networkextension/nevpnmanager)

#### Managing VPN configurations

- [class func shared() -> NEVPNManager](/documentation/networkextension/nevpnmanager/shared())
- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nevpnmanager/loadfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nevpnmanager/savetopreferences(completionhandler:))
- [func setAuthorization(AuthorizationRef)](/documentation/networkextension/nevpnmanager/setauthorization(_:))
- [func removeFromPreferences(completionHandler: (((any Error)?) -> Void)?)](/documentation/networkextension/nevpnmanager/removefrompreferences(completionhandler:))

#### Accessing VPN configuration properties

- [var isEnabled: Bool](/documentation/networkextension/nevpnmanager/isenabled)
- [var protocolConfiguration: NEVPNProtocol?](/documentation/networkextension/nevpnmanager/protocolconfiguration)
- [var `protocol`: NEVPNProtocol?](/documentation/networkextension/nevpnmanager/protocol)
- [var localizedDescription: String?](/documentation/networkextension/nevpnmanager/localizeddescription)
- [var isOnDemandEnabled: Bool](/documentation/networkextension/nevpnmanager/isondemandenabled)
- [var onDemandRules: [NEOnDemandRule]?](/documentation/networkextension/nevpnmanager/ondemandrules)

#### Connecting and disconnecting VPN

- [var connection: NEVPNConnection](/documentation/networkextension/nevpnmanager/connection)

#### Errors

- [NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/code)

##### Error codes

- [case configurationDisabled](/documentation/networkextension/nevpnerror-swift.struct/code/configurationdisabled)
- [case configurationInvalid](/documentation/networkextension/nevpnerror-swift.struct/code/configurationinvalid)
- [case connectionFailed](/documentation/networkextension/nevpnerror-swift.struct/code/connectionfailed)
- [case configurationStale](/documentation/networkextension/nevpnerror-swift.struct/code/configurationstale)
- [case configurationReadWriteFailed](/documentation/networkextension/nevpnerror-swift.struct/code/configurationreadwritefailed)
- [case configurationUnknown](/documentation/networkextension/nevpnerror-swift.struct/code/configurationunknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnerror-swift.struct/code/init(rawvalue:))
- [let NEVPNErrorDomain: String](/documentation/networkextension/nevpnerrordomain)
- [NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/code)

##### Error codes

- [case configurationDisabled](/documentation/networkextension/nevpnerror-swift.struct/code/configurationdisabled)
- [case configurationInvalid](/documentation/networkextension/nevpnerror-swift.struct/code/configurationinvalid)
- [case connectionFailed](/documentation/networkextension/nevpnerror-swift.struct/code/connectionfailed)
- [case configurationStale](/documentation/networkextension/nevpnerror-swift.struct/code/configurationstale)
- [case configurationReadWriteFailed](/documentation/networkextension/nevpnerror-swift.struct/code/configurationreadwritefailed)
- [case configurationUnknown](/documentation/networkextension/nevpnerror-swift.struct/code/configurationunknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnerror-swift.struct/code/init(rawvalue:))

#### Notifications

- [static let NEVPNConfigurationChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nevpnconfigurationchange)

#### Entitlements

- [Personal VPN Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.vpn.api)
- [NETunnelProviderProtocol](/documentation/networkextension/netunnelproviderprotocol)

#### Accessing the tunnel configuration

- [var providerConfiguration: [String : Any]?](/documentation/networkextension/netunnelproviderprotocol/providerconfiguration)
- [var providerBundleIdentifier: String?](/documentation/networkextension/netunnelproviderprotocol/providerbundleidentifier)
- [NEAppRule](/documentation/networkextension/neapprule)

#### Initializing an app rule

- [init(signingIdentifier: String)](/documentation/networkextension/neapprule/init(signingidentifier:))
- [init(signingIdentifier: String, designatedRequirement: String)](/documentation/networkextension/neapprule/init(signingidentifier:designatedrequirement:))

#### Accessing app rule properties

- [var matchSigningIdentifier: String](/documentation/networkextension/neapprule/matchsigningidentifier)
- [var matchDesignatedRequirement: String](/documentation/networkextension/neapprule/matchdesignatedrequirement)
- [var matchPath: String?](/documentation/networkextension/neapprule/matchpath)
- [var matchDomains: [Any]?](/documentation/networkextension/neapprule/matchdomains)
- [var matchTools: [NEAppRule]?](/documentation/networkextension/neapprule/matchtools)
- [VPN On Demand Rules](/documentation/networkextension/vpn-on-demand-rules)

#### Settings

- [NEOnDemandRuleConnect](/documentation/networkextension/neondemandruleconnect)
- [NEOnDemandRuleDisconnect](/documentation/networkextension/neondemandruledisconnect)
- [NEOnDemandRuleIgnore](/documentation/networkextension/neondemandruleignore)
- [NEOnDemandRuleEvaluateConnection](/documentation/networkextension/neondemandruleevaluateconnection)

##### Accessing connection rules

- [var connectionRules: [NEEvaluateConnectionRule]?](/documentation/networkextension/neondemandruleevaluateconnection/connectionrules)
- [NEEvaluateConnectionRule](/documentation/networkextension/neevaluateconnectionrule)

###### Initializing a Rule

- [init(matchDomains: [String], andAction: NEEvaluateConnectionRuleAction)](/documentation/networkextension/neevaluateconnectionrule/init(matchdomains:andaction:))

###### Accessing Rule Match Properties

- [var matchDomains: [String]](/documentation/networkextension/neevaluateconnectionrule/matchdomains)
- [var useDNSServers: [String]?](/documentation/networkextension/neevaluateconnectionrule/usednsservers)
- [var probeURL: URL?](/documentation/networkextension/neevaluateconnectionrule/probeurl)

###### Accessing the Rule Action

- [var action: NEEvaluateConnectionRuleAction](/documentation/networkextension/neevaluateconnectionrule/action)
- [NEEvaluateConnectionRuleAction](/documentation/networkextension/neevaluateconnectionruleaction)

###### Rule Actions

- [case connectIfNeeded](/documentation/networkextension/neevaluateconnectionruleaction/connectifneeded)
- [case neverConnect](/documentation/networkextension/neevaluateconnectionruleaction/neverconnect)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neevaluateconnectionruleaction/init(rawvalue:))
- [NEOnDemandRule](/documentation/networkextension/neondemandrule)

##### Accessing match parameters

- [var dnsSearchDomainMatch: [String]?](/documentation/networkextension/neondemandrule/dnssearchdomainmatch)
- [var dnsServerAddressMatch: [String]?](/documentation/networkextension/neondemandrule/dnsserveraddressmatch)
- [var interfaceTypeMatch: NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandrule/interfacetypematch)
- [NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandruleinterfacetype)

###### Interface Types

- [case any](/documentation/networkextension/neondemandruleinterfacetype/any)
- [case ethernet](/documentation/networkextension/neondemandruleinterfacetype/ethernet)
- [case wiFi](/documentation/networkextension/neondemandruleinterfacetype/wifi)
- [case cellular](/documentation/networkextension/neondemandruleinterfacetype/cellular)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleinterfacetype/init(rawvalue:))
- [var ssidMatch: [String]?](/documentation/networkextension/neondemandrule/ssidmatch)
- [var probeURL: URL?](/documentation/networkextension/neondemandrule/probeurl)

##### Accessing the rule action

- [var action: NEOnDemandRuleAction](/documentation/networkextension/neondemandrule/action)
- [NEOnDemandRuleAction](/documentation/networkextension/neondemandruleaction)

###### Rule Actions

- [case connect](/documentation/networkextension/neondemandruleaction/connect)
- [case disconnect](/documentation/networkextension/neondemandruleaction/disconnect)
- [case evaluateConnection](/documentation/networkextension/neondemandruleaction/evaluateconnection)
- [case ignore](/documentation/networkextension/neondemandruleaction/ignore)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleaction/init(rawvalue:))

### VPN control

- [NETunnelProviderSession](/documentation/networkextension/netunnelprovidersession)

#### Controlling the tunnel connection

- [func startTunnel(options: [String : Any]?) throws](/documentation/networkextension/netunnelprovidersession/starttunnel(options:))
- [func stopTunnel()](/documentation/networkextension/netunnelprovidersession/stoptunnel())

#### Communicating with the tunnel provider

- [func sendProviderMessage(Data, responseHandler: ((Data?) -> Void)?) throws](/documentation/networkextension/netunnelprovidersession/sendprovidermessage(_:responsehandler:))
- [NEVPNConnection](/documentation/networkextension/nevpnconnection)

#### Controlling the VPN connection

- [func startVPNTunnel() throws](/documentation/networkextension/nevpnconnection/startvpntunnel())
- [func startVPNTunnel(options: [String : NSObject]?) throws](/documentation/networkextension/nevpnconnection/startvpntunnel(options:))
- [let NEVPNConnectionStartOptionUsername: String](/documentation/networkextension/nevpnconnectionstartoptionusername)
- [let NEVPNConnectionStartOptionPassword: String](/documentation/networkextension/nevpnconnectionstartoptionpassword)
- [func stopVPNTunnel()](/documentation/networkextension/nevpnconnection/stopvpntunnel())

#### Getting VPN connection status

- [var manager: NEVPNManager](/documentation/networkextension/nevpnconnection/manager)
- [var status: NEVPNStatus](/documentation/networkextension/nevpnconnection/status)
- [NEVPNStatus](/documentation/networkextension/nevpnstatus)

##### Statuses

- [case disconnecting](/documentation/networkextension/nevpnstatus/disconnecting)
- [case reasserting](/documentation/networkextension/nevpnstatus/reasserting)
- [case connected](/documentation/networkextension/nevpnstatus/connected)
- [case connecting](/documentation/networkextension/nevpnstatus/connecting)
- [case disconnected](/documentation/networkextension/nevpnstatus/disconnected)
- [case invalid](/documentation/networkextension/nevpnstatus/invalid)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnstatus/init(rawvalue:))
- [var connectedDate: Date?](/documentation/networkextension/nevpnconnection/connecteddate)

#### Notifications

- [static let NEVPNStatusDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nevpnstatusdidchange)

#### Handling errors

- [func fetchLastDisconnectError(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nevpnconnection/fetchlastdisconnecterror(completionhandler:))
- [let NEVPNConnectionErrorDomain: String](/documentation/networkextension/nevpnconnectionerrordomain)
- [NEVPNConnectionError](/documentation/networkextension/nevpnconnectionerror)

##### General error codes

- [case overslept](/documentation/networkextension/nevpnconnectionerror/overslept)
- [case noNetworkAvailable](/documentation/networkextension/nevpnconnectionerror/nonetworkavailable)
- [case unrecoverableNetworkChange](/documentation/networkextension/nevpnconnectionerror/unrecoverablenetworkchange)
- [case configurationFailed](/documentation/networkextension/nevpnconnectionerror/configurationfailed)
- [case authenticationFailed](/documentation/networkextension/nevpnconnectionerror/authenticationfailed)
- [case configurationNotFound](/documentation/networkextension/nevpnconnectionerror/configurationnotfound)
- [case negotiationFailed](/documentation/networkextension/nevpnconnectionerror/negotiationfailed)

##### VPN server error codes

- [case serverAddressResolutionFailed](/documentation/networkextension/nevpnconnectionerror/serveraddressresolutionfailed)
- [case serverNotResponding](/documentation/networkextension/nevpnconnectionerror/servernotresponding)
- [case serverDead](/documentation/networkextension/nevpnconnectionerror/serverdead)
- [case serverDisconnected](/documentation/networkextension/nevpnconnectionerror/serverdisconnected)

##### Plugin error codes

- [case pluginFailed](/documentation/networkextension/nevpnconnectionerror/pluginfailed)
- [case pluginDisabled](/documentation/networkextension/nevpnconnectionerror/plugindisabled)

##### Client certificate error codes

- [case clientCertificateInvalid](/documentation/networkextension/nevpnconnectionerror/clientcertificateinvalid)
- [case clientCertificateNotYetValid](/documentation/networkextension/nevpnconnectionerror/clientcertificatenotyetvalid)
- [case clientCertificateExpired](/documentation/networkextension/nevpnconnectionerror/clientcertificateexpired)

##### Server certificate error codes

- [case serverCertificateInvalid](/documentation/networkextension/nevpnconnectionerror/servercertificateinvalid)
- [case serverCertificateNotYetValid](/documentation/networkextension/nevpnconnectionerror/servercertificatenotyetvalid)
- [case serverCertificateExpired](/documentation/networkextension/nevpnconnectionerror/servercertificateexpired)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnconnectionerror/init(rawvalue:))

### Transparent proxy configuration

- [NETransparentProxyManager](/documentation/networkextension/netransparentproxymanager)

#### Loading proxy configurations

- [class func loadAllFromPreferences(completionHandler: ([NETransparentProxyManager]?, (any Error)?) -> Void)](/documentation/networkextension/netransparentproxymanager/loadallfrompreferences(completionhandler:))
- [NETransparentProxyProvider](/documentation/networkextension/netransparentproxyprovider)
- [NETransparentProxyNetworkSettings](/documentation/networkextension/netransparentproxynetworksettings)

#### Traffic routing rules

- [var includedNetworkRules: [NENetworkRule]?](/documentation/networkextension/netransparentproxynetworksettings/includednetworkrules)
- [var excludedNetworkRules: [NENetworkRule]?](/documentation/networkextension/netransparentproxynetworksettings/excludednetworkrules)
- [NENetworkRule](/documentation/networkextension/nenetworkrule)

#### Creating a network rule

- [init(destinationNetwork: NWHostEndpoint, prefix: Int, protocol: NENetworkRule.Protocol)](/documentation/networkextension/nenetworkrule/init(destinationnetwork:prefix:protocol:))
- [init(destinationHost: NWHostEndpoint, protocol: NENetworkRule.Protocol)](/documentation/networkextension/nenetworkrule/init(destinationhost:protocol:))
- [init(remoteNetwork: NWHostEndpoint?, remotePrefix: Int, localNetwork: NWHostEndpoint?, localPrefix: Int, protocol: NENetworkRule.Protocol, direction: NETrafficDirection)](/documentation/networkextension/nenetworkrule/init(remotenetwork:remoteprefix:localnetwork:localprefix:protocol:direction:))

#### Matching network traffic characteristics

- [var matchRemoteEndpoint: NWHostEndpoint?](/documentation/networkextension/nenetworkrule/matchremoteendpoint)
- [var matchRemotePrefix: Int](/documentation/networkextension/nenetworkrule/matchremoteprefix)
- [var matchLocalNetwork: NWHostEndpoint?](/documentation/networkextension/nenetworkrule/matchlocalnetwork)
- [var matchLocalPrefix: Int](/documentation/networkextension/nenetworkrule/matchlocalprefix)
- [var matchProtocol: NENetworkRule.Protocol](/documentation/networkextension/nenetworkrule/matchprotocol)
- [NENetworkRule.Protocol](/documentation/networkextension/nenetworkrule/protocol)

##### Protocols

- [case TCP](/documentation/networkextension/nenetworkrule/protocol/tcp)
- [case UDP](/documentation/networkextension/nenetworkrule/protocol/udp)
- [case any](/documentation/networkextension/nenetworkrule/protocol/any)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nenetworkrule/protocol/init(rawvalue:))
- [var matchDirection: NETrafficDirection](/documentation/networkextension/nenetworkrule/matchdirection)
- [NETrafficDirection](/documentation/networkextension/netrafficdirection)

##### Directions

- [case inbound](/documentation/networkextension/netrafficdirection/inbound)
- [case outbound](/documentation/networkextension/netrafficdirection/outbound)
- [case any](/documentation/networkextension/netrafficdirection/any)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netrafficdirection/init(rawvalue:))

#### Initializers

- [convenience init(destinationHostEndpoint: NWEndpoint, protocol: NENetworkRule.Protocol)](/documentation/networkextension/nenetworkrule/init(destinationhostendpoint:protocol:))
- [convenience init(destinationNetworkEndpoint: NWEndpoint, prefix: Int, protocol: NENetworkRule.Protocol)](/documentation/networkextension/nenetworkrule/init(destinationnetworkendpoint:prefix:protocol:))
- [convenience init(remoteNetworkEndpoint: NWEndpoint?, remotePrefix: Int, localNetworkEndpoint: NWEndpoint?, localPrefix: Int, protocol: NENetworkRule.Protocol, direction: NETrafficDirection)](/documentation/networkextension/nenetworkrule/init(remotenetworkendpoint:remoteprefix:localnetworkendpoint:localprefix:protocol:direction:))

#### Instance Properties

- [var matchLocalNetworkEndpoint: NWEndpoint?](/documentation/networkextension/nenetworkrule/matchlocalnetworkendpoint-62ttv)
- [var matchRemoteHostOrNetworkEndpoint: NWEndpoint?](/documentation/networkextension/nenetworkrule/matchremotehostornetworkendpoint-4a5ht)

## Network relays

- [Relays](/documentation/networkextension/relays)

### Essentials

- [Network Extensions Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.networkextension)

### Relay configuration

- [NERelayManager](/documentation/networkextension/nerelaymanager)

#### Managing relay configurations

- [class func shared() -> NERelayManager](/documentation/networkextension/nerelaymanager/shared())
- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nerelaymanager/loadfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nerelaymanager/savetopreferences(completionhandler:))
- [func removeFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nerelaymanager/removefrompreferences(completionhandler:))

#### Accessing relay configuration properties

- [var isEnabled: Bool](/documentation/networkextension/nerelaymanager/isenabled)
- [var relays: [NERelay]?](/documentation/networkextension/nerelaymanager/relays)
- [var matchDomains: [String]?](/documentation/networkextension/nerelaymanager/matchdomains)
- [var excludedDomains: [String]?](/documentation/networkextension/nerelaymanager/excludeddomains)
- [var localizedDescription: String?](/documentation/networkextension/nerelaymanager/localizeddescription)
- [var onDemandRules: [NEOnDemandRule]?](/documentation/networkextension/nerelaymanager/ondemandrules)
- [NEOnDemandRule](/documentation/networkextension/neondemandrule)

##### Accessing match parameters

- [var dnsSearchDomainMatch: [String]?](/documentation/networkextension/neondemandrule/dnssearchdomainmatch)
- [var dnsServerAddressMatch: [String]?](/documentation/networkextension/neondemandrule/dnsserveraddressmatch)
- [var interfaceTypeMatch: NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandrule/interfacetypematch)
- [NEOnDemandRuleInterfaceType](/documentation/networkextension/neondemandruleinterfacetype)

###### Interface Types

- [case any](/documentation/networkextension/neondemandruleinterfacetype/any)
- [case ethernet](/documentation/networkextension/neondemandruleinterfacetype/ethernet)
- [case wiFi](/documentation/networkextension/neondemandruleinterfacetype/wifi)
- [case cellular](/documentation/networkextension/neondemandruleinterfacetype/cellular)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleinterfacetype/init(rawvalue:))
- [var ssidMatch: [String]?](/documentation/networkextension/neondemandrule/ssidmatch)
- [var probeURL: URL?](/documentation/networkextension/neondemandrule/probeurl)

##### Accessing the rule action

- [var action: NEOnDemandRuleAction](/documentation/networkextension/neondemandrule/action)
- [NEOnDemandRuleAction](/documentation/networkextension/neondemandruleaction)

###### Rule Actions

- [case connect](/documentation/networkextension/neondemandruleaction/connect)
- [case disconnect](/documentation/networkextension/neondemandruleaction/disconnect)
- [case evaluateConnection](/documentation/networkextension/neondemandruleaction/evaluateconnection)
- [case ignore](/documentation/networkextension/neondemandruleaction/ignore)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neondemandruleaction/init(rawvalue:))

#### Loading previously-used managers

- [class func loadAllManagersFromPreferences(completionHandler: ([NERelayManager], (any Error)?) -> Void)](/documentation/networkextension/nerelaymanager/loadallmanagersfrompreferences(completionhandler:))

#### Handling errors

- [let NERelayErrorDomain: String](/documentation/networkextension/nerelayerrordomain)
- [NERelayManagerError](/documentation/networkextension/nerelaymanagererror)

##### Error codes

- [case configurationInvalid](/documentation/networkextension/nerelaymanagererror/configurationinvalid)
- [case configurationDisabled](/documentation/networkextension/nerelaymanagererror/configurationdisabled)
- [case configurationStale](/documentation/networkextension/nerelaymanagererror/configurationstale)
- [case configurationCannotBeRemoved](/documentation/networkextension/nerelaymanagererror/configurationcannotberemoved)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nerelaymanagererror/init(rawvalue:))

#### Instance Properties

- [var excludedFQDNs: [String]?](/documentation/networkextension/nerelaymanager/excludedfqdns)
- [var isDNSFailoverAllowed: Bool](/documentation/networkextension/nerelaymanager/isdnsfailoverallowed)
- [var isUIToggleEnabled: Bool](/documentation/networkextension/nerelaymanager/isuitoggleenabled)
- [var matchFQDNs: [String]?](/documentation/networkextension/nerelaymanager/matchfqdns)

#### Instance Methods

- [func getLastClientErrors(TimeInterval, completionHandler: ([any Error]?) -> Void)](/documentation/networkextension/nerelaymanager/getlastclienterrors(_:completionhandler:))
- [NERelay](/documentation/networkextension/nerelay)

#### Configuring server properties

- [var http3RelayURL: URL?](/documentation/networkextension/nerelay/http3relayurl)
- [var http2RelayURL: URL?](/documentation/networkextension/nerelay/http2relayurl)
- [var dnsOverHTTPSURL: URL?](/documentation/networkextension/nerelay/dnsoverhttpsurl)
- [var rawPublicKeys: [Data]?](/documentation/networkextension/nerelay/rawpublickeys)

#### Configuring client properties

- [var additionalHTTPHeaderFields: [String : String]](/documentation/networkextension/nerelay/additionalhttpheaderfields)
- [var identityData: Data?](/documentation/networkextension/nerelay/identitydata)
- [var identityDataPassword: String?](/documentation/networkextension/nerelay/identitydatapassword)
- [var syntheticDNSAnswerIPv4Prefix: String?](/documentation/networkextension/nerelay/syntheticdnsansweripv4prefix)
- [var syntheticDNSAnswerIPv6Prefix: String?](/documentation/networkextension/nerelay/syntheticdnsansweripv6prefix)

## Content filters

- [Content filter providers](/documentation/networkextension/content-filter-providers)

### Essentials

- [Network Extensions Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.networkextension)

### Data and control providers

- [NEFilterDataProvider](/documentation/networkextension/nefilterdataprovider)

#### Filtering network content

- [func handleNewFlow(NEFilterFlow) -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilterdataprovider/handlenewflow(_:))
- [func handleInboundData(from: NEFilterFlow, readBytesStartOffset: Int, readBytes: Data) -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataprovider/handleinbounddata(from:readbytesstartoffset:readbytes:))
- [NEFilterDataAttribute](/documentation/networkextension/nefilterdataattribute)

##### Attributes

- [case hasIPHeader](/documentation/networkextension/nefilterdataattribute/hasipheader)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefilterdataattribute/init(rawvalue:))
- [func handleOutboundData(from: NEFilterFlow, readBytesStartOffset: Int, readBytes: Data) -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataprovider/handleoutbounddata(from:readbytesstartoffset:readbytes:))
- [func handleInboundDataComplete(for: NEFilterFlow) -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataprovider/handleinbounddatacomplete(for:))
- [func handleOutboundDataComplete(for: NEFilterFlow) -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataprovider/handleoutbounddatacomplete(for:))

#### Handling remediation

- [func handleRemediation(for: NEFilterFlow) -> NEFilterRemediationVerdict](/documentation/networkextension/nefilterdataprovider/handleremediation(for:))

#### Handling rule updates

- [func handleRulesChanged()](/documentation/networkextension/nefilterdataprovider/handleruleschanged())

#### Changing filter settings

- [func apply(NEFilterSettings?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nefilterdataprovider/apply(_:completionhandler:))
- [NEFilterSettings](/documentation/networkextension/nefiltersettings)

##### Creating Filter Settings

- [init(rules: [NEFilterRule], defaultAction: NEFilterAction)](/documentation/networkextension/nefiltersettings/init(rules:defaultaction:))
- [NEFilterRule](/documentation/networkextension/nefilterrule)

###### Creating a Filter Rule

- [init(networkRule: NENetworkRule, action: NEFilterAction)](/documentation/networkextension/nefilterrule/init(networkrule:action:))

###### Inspecting Filter Rule Properties

- [var networkRule: NENetworkRule](/documentation/networkextension/nefilterrule/networkrule)
- [var action: NEFilterAction](/documentation/networkextension/nefilterrule/action)

##### Inspecting Filter Settings

- [var rules: [NEFilterRule]](/documentation/networkextension/nefiltersettings/rules)
- [var defaultAction: NEFilterAction](/documentation/networkextension/nefiltersettings/defaultaction)

#### Resuming data flows

- [func resumeFlow(NEFilterFlow, with: NEFilterVerdict)](/documentation/networkextension/nefilterdataprovider/resumeflow(_:with:))

#### Updating filter verdicts

- [func update(NEFilterSocketFlow, using: NEFilterDataVerdict, for: NETrafficDirection)](/documentation/networkextension/nefilterdataprovider/update(_:using:for:))
- [NEFilterControlProvider](/documentation/networkextension/nefiltercontrolprovider)

#### Handling requests for new rules

- [func handleNewFlow(NEFilterFlow, completionHandler: (NEFilterControlVerdict) -> Void)](/documentation/networkextension/nefiltercontrolprovider/handlenewflow(_:completionhandler:))
- [func notifyRulesChanged()](/documentation/networkextension/nefiltercontrolprovider/notifyruleschanged())

#### Handling remediation

- [func handleRemediation(for: NEFilterFlow, completionHandler: (NEFilterControlVerdict) -> Void)](/documentation/networkextension/nefiltercontrolprovider/handleremediation(for:completionhandler:))
- [var remediationMap: [String : [String : NSObject]]?](/documentation/networkextension/nefiltercontrolprovider/remediationmap)
- [let NEFilterProviderRemediationMapRemediationButtonTexts: String](/documentation/networkextension/nefilterproviderremediationmapremediationbuttontexts)
- [let NEFilterProviderRemediationMapRemediationURLs: String](/documentation/networkextension/nefilterproviderremediationmapremediationurls)
- [var NEFilterProviderRemediationURLFlowURL: String](/documentation/networkextension/nefilterproviderremediationurlflowurl)
- [var NEFilterProviderRemediationURLFlowURLHostname: String](/documentation/networkextension/nefilterproviderremediationurlflowurlhostname)
- [var NEFilterProviderRemediationURLOrganization: String](/documentation/networkextension/nefilterproviderremediationurlorganization)
- [var NEFilterProviderRemediationURLUsername: String](/documentation/networkextension/nefilterproviderremediationurlusername)
- [var urlAppendStringMap: [String : String]?](/documentation/networkextension/nefiltercontrolprovider/urlappendstringmap)
- [NEFilterPacketProvider](/documentation/networkextension/nefilterpacketprovider)

#### Filtering packets

- [var packetHandler: NEFilterPacketHandler?](/documentation/networkextension/nefilterpacketprovider/packethandler)
- [NEFilterPacketHandler](/documentation/networkextension/nefilterpackethandler)
- [NEFilterPacketContext](/documentation/networkextension/nefilterpacketcontext)
- [NETrafficDirection](/documentation/networkextension/netrafficdirection)

##### Directions

- [case inbound](/documentation/networkextension/netrafficdirection/inbound)
- [case outbound](/documentation/networkextension/netrafficdirection/outbound)
- [case any](/documentation/networkextension/netrafficdirection/any)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netrafficdirection/init(rawvalue:))
- [NEFilterPacketProvider.Verdict](/documentation/networkextension/nefilterpacketprovider/verdict)

##### Verdicts

- [case allow](/documentation/networkextension/nefilterpacketprovider/verdict/allow)
- [case drop](/documentation/networkextension/nefilterpacketprovider/verdict/drop)
- [case delay](/documentation/networkextension/nefilterpacketprovider/verdict/delay)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefilterpacketprovider/verdict/init(rawvalue:))

#### Delaying packets

- [func delayCurrentPacket(NEFilterPacketContext) -> NEPacket](/documentation/networkextension/nefilterpacketprovider/delaycurrentpacket(_:))
- [func allow(NEPacket)](/documentation/networkextension/nefilterpacketprovider/allow(_:))

#### Instance Properties

- [var handler: ((NEFilterPacketContext, NWInterface, NETrafficDirection, UnsafeRawBufferPointer) -> NEFilterPacketProvider.Verdict)?](/documentation/networkextension/nefilterpacketprovider/handler)
- [NEFilterProvider](/documentation/networkextension/nefilterprovider)

#### Managing the filter life cycle

- [func startFilter(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nefilterprovider/startfilter(completionhandler:))
- [func stopFilter(with: NEProviderStopReason, completionHandler: () -> Void)](/documentation/networkextension/nefilterprovider/stopfilter(with:completionhandler:))

#### Getting the filter configuration

- [var filterConfiguration: NEFilterProviderConfiguration](/documentation/networkextension/nefilterprovider/filterconfiguration)

#### Receiving reports

- [func handle(NEFilterReport)](/documentation/networkextension/nefilterprovider/handle(_:))

#### Handling errors

- [let NEFilterErrorDomain: String](/documentation/networkextension/nefiltererrordomain)
- [NEFilterManagerError](/documentation/networkextension/nefiltermanagererror)

##### Error codes

- [case configurationInvalid](/documentation/networkextension/nefiltermanagererror/configurationinvalid)
- [case configurationDisabled](/documentation/networkextension/nefiltermanagererror/configurationdisabled)
- [case configurationStale](/documentation/networkextension/nefiltermanagererror/configurationstale)
- [case configurationCannotBeRemoved](/documentation/networkextension/nefiltermanagererror/configurationcannotberemoved)
- [case configurationPermissionDenied](/documentation/networkextension/nefiltermanagererror/configurationpermissiondenied)
- [case configurationInternalError](/documentation/networkextension/nefiltermanagererror/configurationinternalerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefiltermanagererror/init(rawvalue:))

### Flow handling

- [NEFilterFlow](/documentation/networkextension/nefilterflow)

#### Inspecting flow properties

- [var url: URL?](/documentation/networkextension/nefilterflow/url)
- [var identifier: UUID](/documentation/networkextension/nefilterflow/identifier)
- [var direction: NETrafficDirection](/documentation/networkextension/nefilterflow/direction)
- [NETrafficDirection](/documentation/networkextension/netrafficdirection)

##### Directions

- [case inbound](/documentation/networkextension/netrafficdirection/inbound)
- [case outbound](/documentation/networkextension/netrafficdirection/outbound)
- [case any](/documentation/networkextension/netrafficdirection/any)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netrafficdirection/init(rawvalue:))
- [var NEFilterFlowBytesMax: UInt64](/documentation/networkextension/nefilterflowbytesmax)

#### Source app identification

- [var sourceAppUniqueIdentifier: Data?](/documentation/networkextension/nefilterflow/sourceappuniqueidentifier)
- [var sourceAppIdentifier: String?](/documentation/networkextension/nefilterflow/sourceappidentifier)
- [var sourceAppVersion: String?](/documentation/networkextension/nefilterflow/sourceappversion)
- [var sourceAppAuditToken: Data?](/documentation/networkextension/nefilterflow/sourceappaudittoken)
- [var sourceProcessAuditToken: Data?](/documentation/networkextension/nefilterflow/sourceprocessaudittoken)
- [NEFilterBrowserFlow](/documentation/networkextension/nefilterbrowserflow)

#### Getting browser flow properties

- [var parentURL: URL?](/documentation/networkextension/nefilterbrowserflow/parenturl)
- [var request: URLRequest?](/documentation/networkextension/nefilterbrowserflow/request)
- [var response: URLResponse?](/documentation/networkextension/nefilterbrowserflow/response)
- [NEFilterSocketFlow](/documentation/networkextension/nefiltersocketflow)

#### Getting socket flow properties

- [var remoteEndpoint: NWEndpoint?](/documentation/networkextension/nefiltersocketflow/remoteendpoint)
- [var remoteHostname: String?](/documentation/networkextension/nefiltersocketflow/remotehostname)
- [NEFilterFlow](/documentation/networkextension/nefilterflow)

##### Inspecting flow properties

- [var url: URL?](/documentation/networkextension/nefilterflow/url)
- [var identifier: UUID](/documentation/networkextension/nefilterflow/identifier)
- [var direction: NETrafficDirection](/documentation/networkextension/nefilterflow/direction)
- [NETrafficDirection](/documentation/networkextension/netrafficdirection)

###### Directions

- [case inbound](/documentation/networkextension/netrafficdirection/inbound)
- [case outbound](/documentation/networkextension/netrafficdirection/outbound)
- [case any](/documentation/networkextension/netrafficdirection/any)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netrafficdirection/init(rawvalue:))
- [var NEFilterFlowBytesMax: UInt64](/documentation/networkextension/nefilterflowbytesmax)

##### Source app identification

- [var sourceAppUniqueIdentifier: Data?](/documentation/networkextension/nefilterflow/sourceappuniqueidentifier)
- [var sourceAppIdentifier: String?](/documentation/networkextension/nefilterflow/sourceappidentifier)
- [var sourceAppVersion: String?](/documentation/networkextension/nefilterflow/sourceappversion)
- [var sourceAppAuditToken: Data?](/documentation/networkextension/nefilterflow/sourceappaudittoken)
- [var sourceProcessAuditToken: Data?](/documentation/networkextension/nefilterflow/sourceprocessaudittoken)
- [var localEndpoint: NWEndpoint?](/documentation/networkextension/nefiltersocketflow/localendpoint)
- [var socketFamily: Int32](/documentation/networkextension/nefiltersocketflow/socketfamily)
- [var socketType: Int32](/documentation/networkextension/nefiltersocketflow/sockettype)
- [var socketProtocol: Int32](/documentation/networkextension/nefiltersocketflow/socketprotocol)

#### Instance Properties

- [var localFlowEndpoint: NWEndpoint?](/documentation/networkextension/nefiltersocketflow/localflowendpoint-89z3l)
- [var remoteFlowEndpoint: NWEndpoint?](/documentation/networkextension/nefiltersocketflow/remoteflowendpoint-6bnas)
- [NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict)

#### Creating new flow verdicts

- [class func allow() -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict/allow())
- [class func drop() -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict/drop())
- [class func pause() -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict/pause())
- [class func filterDataVerdict(withFilterInbound: Bool, peekInboundBytes: Int, filterOutbound: Bool, peekOutboundBytes: Int) -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict/filterdataverdict(withfilterinbound:peekinboundbytes:filteroutbound:peekoutboundbytes:))
- [class func remediateVerdict(withRemediationURLMapKey: String, remediationButtonTextMapKey: String) -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict/remediateverdict(withremediationurlmapkey:remediationbuttontextmapkey:))
- [class func needRules() -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict/needrules())
- [class func urlAppendStringVerdict(withMapKey: String) -> NEFilterNewFlowVerdict](/documentation/networkextension/nefilternewflowverdict/urlappendstringverdict(withmapkey:))

#### Inspecting new flow verdict properties

- [var statisticsReportFrequency: NEFilterReport.Frequency](/documentation/networkextension/nefilternewflowverdict/statisticsreportfrequency)
- [NEFilterReport.Frequency](/documentation/networkextension/nefilterreport/frequency)

##### Report frequencies

- [case none](/documentation/networkextension/nefilterreport/frequency/none)
- [case low](/documentation/networkextension/nefilterreport/frequency/low)
- [case medium](/documentation/networkextension/nefilterreport/frequency/medium)
- [case high](/documentation/networkextension/nefilterreport/frequency/high)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefilterreport/frequency/init(rawvalue:))
- [NEFilterDataVerdict](/documentation/networkextension/nefilterdataverdict)

#### Creating data verdicts

- [class func allow() -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataverdict/allow())
- [class func drop() -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataverdict/drop())
- [class func pause() -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataverdict/pause())
- [class func remediateVerdict(withRemediationURLMapKey: String?, remediationButtonTextMapKey: String?) -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataverdict/remediateverdict(withremediationurlmapkey:remediationbuttontextmapkey:))
- [class func needRules() -> NEFilterDataVerdict](/documentation/networkextension/nefilterdataverdict/needrules())
- [init(passBytes: Int, peekBytes: Int)](/documentation/networkextension/nefilterdataverdict/init(passbytes:peekbytes:))

#### Reporting statistics

- [var statisticsReportFrequency: NEFilterReport.Frequency](/documentation/networkextension/nefilterdataverdict/statisticsreportfrequency)
- [NEFilterControlVerdict](/documentation/networkextension/nefiltercontrolverdict)

#### Creating control verdicts

- [class func allow(withUpdateRules: Bool) -> NEFilterControlVerdict](/documentation/networkextension/nefiltercontrolverdict/allow(withupdaterules:))
- [class func drop(withUpdateRules: Bool) -> NEFilterControlVerdict](/documentation/networkextension/nefiltercontrolverdict/drop(withupdaterules:))
- [class func updateRules() -> NEFilterControlVerdict](/documentation/networkextension/nefiltercontrolverdict/updaterules())
- [NEFilterRemediationVerdict](/documentation/networkextension/nefilterremediationverdict)

#### Creating remediation verdicts

- [class func allow() -> NEFilterRemediationVerdict](/documentation/networkextension/nefilterremediationverdict/allow())
- [class func drop() -> NEFilterRemediationVerdict](/documentation/networkextension/nefilterremediationverdict/drop())
- [class func needRules() -> NEFilterRemediationVerdict](/documentation/networkextension/nefilterremediationverdict/needrules())
- [NEFilterVerdict](/documentation/networkextension/nefilterverdict)

#### Configuring report generation

- [var shouldReport: Bool](/documentation/networkextension/nefilterverdict/shouldreport)
- [NEFilterReport](/documentation/networkextension/nefilterreport)

#### Getting report properties

- [var flow: NEFilterFlow?](/documentation/networkextension/nefilterreport/flow)
- [var action: NEFilterAction](/documentation/networkextension/nefilterreport/action)
- [NEFilterAction](/documentation/networkextension/nefilteraction)

##### Enumeration Cases

- [case invalid](/documentation/networkextension/nefilteraction/invalid)
- [case allow](/documentation/networkextension/nefilteraction/allow)
- [case drop](/documentation/networkextension/nefilteraction/drop)
- [case remediate](/documentation/networkextension/nefilteraction/remediate)
- [case filterData](/documentation/networkextension/nefilteraction/filterdata)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefilteraction/init(rawvalue:))
- [var event: NEFilterReport.Event](/documentation/networkextension/nefilterreport/event-swift.property)
- [NEFilterReport.Event](/documentation/networkextension/nefilterreport/event-swift.enum)

##### Event Types

- [case newFlow](/documentation/networkextension/nefilterreport/event-swift.enum/newflow)
- [case dataDecision](/documentation/networkextension/nefilterreport/event-swift.enum/datadecision)
- [case flowClosed](/documentation/networkextension/nefilterreport/event-swift.enum/flowclosed)
- [case statistics](/documentation/networkextension/nefilterreport/event-swift.enum/statistics)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefilterreport/event-swift.enum/init(rawvalue:))
- [var bytesInboundCount: Int](/documentation/networkextension/nefilterreport/bytesinboundcount)
- [var bytesOutboundCount: Int](/documentation/networkextension/nefilterreport/bytesoutboundcount)

### Filter configuration

- [NEFilterManager](/documentation/networkextension/nefiltermanager)

#### Managing the filter configuration

- [class func shared() -> NEFilterManager](/documentation/networkextension/nefiltermanager/shared())
- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nefiltermanager/loadfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nefiltermanager/savetopreferences(completionhandler:))
- [func removeFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nefiltermanager/removefrompreferences(completionhandler:))

#### Accessing filter configuration properties

- [var isEnabled: Bool](/documentation/networkextension/nefiltermanager/isenabled)
- [var providerConfiguration: NEFilterProviderConfiguration?](/documentation/networkextension/nefiltermanager/providerconfiguration)
- [var localizedDescription: String?](/documentation/networkextension/nefiltermanager/localizeddescription)

#### Prioritizing filters

- [var grade: NEFilterManager.Grade](/documentation/networkextension/nefiltermanager/grade-swift.property)
- [NEFilterManager.Grade](/documentation/networkextension/nefiltermanager/grade-swift.enum)

##### Grades

- [case firewall](/documentation/networkextension/nefiltermanager/grade-swift.enum/firewall)
- [case inspector](/documentation/networkextension/nefiltermanager/grade-swift.enum/inspector)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefiltermanager/grade-swift.enum/init(rawvalue:))

#### Errors

- [let NEFilterErrorDomain: String](/documentation/networkextension/nefiltererrordomain)
- [NEFilterManagerError](/documentation/networkextension/nefiltermanagererror)

##### Error codes

- [case configurationInvalid](/documentation/networkextension/nefiltermanagererror/configurationinvalid)
- [case configurationDisabled](/documentation/networkextension/nefiltermanagererror/configurationdisabled)
- [case configurationStale](/documentation/networkextension/nefiltermanagererror/configurationstale)
- [case configurationCannotBeRemoved](/documentation/networkextension/nefiltermanagererror/configurationcannotberemoved)
- [case configurationPermissionDenied](/documentation/networkextension/nefiltermanagererror/configurationpermissiondenied)
- [case configurationInternalError](/documentation/networkextension/nefiltermanagererror/configurationinternalerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nefiltermanagererror/init(rawvalue:))

#### Notifications

- [static let NEFilterConfigurationDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nefilterconfigurationdidchange)

#### Instance Properties

- [var disableEncryptedDNSSettings: Bool](/documentation/networkextension/nefiltermanager/disableencrypteddnssettings)
- [NEFilterProviderConfiguration](/documentation/networkextension/nefilterproviderconfiguration)

#### Configuring filter behavior

- [var filterBrowsers: Bool](/documentation/networkextension/nefilterproviderconfiguration/filterbrowsers)
- [var filterSockets: Bool](/documentation/networkextension/nefilterproviderconfiguration/filtersockets)
- [var filterPackets: Bool](/documentation/networkextension/nefilterproviderconfiguration/filterpackets)

#### Accessing the filter configuration

- [var vendorConfiguration: [String : Any]?](/documentation/networkextension/nefilterproviderconfiguration/vendorconfiguration)
- [var serverAddress: String?](/documentation/networkextension/nefilterproviderconfiguration/serveraddress)
- [var username: String?](/documentation/networkextension/nefilterproviderconfiguration/username)
- [var organization: String?](/documentation/networkextension/nefilterproviderconfiguration/organization)
- [var passwordReference: Data?](/documentation/networkextension/nefilterproviderconfiguration/passwordreference)
- [var identityReference: Data?](/documentation/networkextension/nefilterproviderconfiguration/identityreference)

#### Accessing bundle identifiers

- [var filterDataProviderBundleIdentifier: String?](/documentation/networkextension/nefilterproviderconfiguration/filterdataproviderbundleidentifier)
- [var filterPacketProviderBundleIdentifier: String?](/documentation/networkextension/nefilterproviderconfiguration/filterpacketproviderbundleidentifier)
- [Filtering Network Traffic](/documentation/networkextension/filtering-network-traffic)

## URL filters

- [URL filters](/documentation/networkextension/url-filters)

### URL filters

- [NEURLFilterManager](/documentation/networkextension/neurlfiltermanager)

#### Obtaining the shared instance

- [static var shared: NEURLFilterManager](/documentation/networkextension/neurlfiltermanager/shared)

#### Working with a Private Information Retrieval server

- [var pirServerURL: URL?](/documentation/networkextension/neurlfiltermanager/pirserverurl)
- [var pirPrivacyPassIssuerURL: URL?](/documentation/networkextension/neurlfiltermanager/pirprivacypassissuerurl)
- [var pirAuthenticationToken: String?](/documentation/networkextension/neurlfiltermanager/pirauthenticationtoken)
- [func refreshPIRParameters() async throws](/documentation/networkextension/neurlfiltermanager/refreshpirparameters())
- [func resetPIRCache() async throws](/documentation/networkextension/neurlfiltermanager/resetpircache())

#### Working with the filter configuration

- [func setConfiguration(pirServerURL: URL, pirPrivacyPassIssuerURL: URL?, pirAuthenticationToken: String, controlProviderBundleIdentifier: String) throws](/documentation/networkextension/neurlfiltermanager/setconfiguration(pirserverurl:pirprivacypassissuerurl:pirauthenticationtoken:controlproviderbundleidentifier:))
- [func loadFromPreferences() async throws](/documentation/networkextension/neurlfiltermanager/loadfrompreferences())
- [func saveToPreferences() async throws](/documentation/networkextension/neurlfiltermanager/savetopreferences())
- [func removeFromPreferences() async throws](/documentation/networkextension/neurlfiltermanager/removefrompreferences())
- [func handleConfigChange() -> any AsyncSequence<Bool, Never>](/documentation/networkextension/neurlfiltermanager/handleconfigchange())

#### Working with filter status

- [var status: NEURLFilterManager.Status](/documentation/networkextension/neurlfiltermanager/status-swift.property)
- [func handleStatusChange() -> any AsyncSequence<NEURLFilterManager.Status, Never>](/documentation/networkextension/neurlfiltermanager/handlestatuschange())
- [NEURLFilterManager.Status](/documentation/networkextension/neurlfiltermanager/status-swift.enum)

##### URL filter statuses

- [case invalid](/documentation/networkextension/neurlfiltermanager/status-swift.enum/invalid)
- [case stopped](/documentation/networkextension/neurlfiltermanager/status-swift.enum/stopped)
- [case starting](/documentation/networkextension/neurlfiltermanager/status-swift.enum/starting)
- [case running](/documentation/networkextension/neurlfiltermanager/status-swift.enum/running)
- [case stopping](/documentation/networkextension/neurlfiltermanager/status-swift.enum/stopping)

#### Managing filter life cycle

- [var isEnabled: Bool](/documentation/networkextension/neurlfiltermanager/isenabled)
- [var shouldFailClosed: Bool](/documentation/networkextension/neurlfiltermanager/shouldfailclosed)
- [var prefilterFetchInterval: TimeInterval](/documentation/networkextension/neurlfiltermanager/prefilterfetchinterval)

#### Identifying app and extension bundles

- [var appBundleIdentifier: String?](/documentation/networkextension/neurlfiltermanager/appbundleidentifier)
- [var controlProviderBundleIdentifier: String?](/documentation/networkextension/neurlfiltermanager/controlproviderbundleidentifier)

#### Handling errors

- [var lastDisconnectError: NEURLFilterManager.Error?](/documentation/networkextension/neurlfiltermanager/lastdisconnecterror)
- [NEURLFilterManager.Error](/documentation/networkextension/neurlfiltermanager/error)

##### Configuration errors

- [case configurationUnchanged](/documentation/networkextension/neurlfiltermanager/error/configurationunchanged)
- [case configurationInvalid](/documentation/networkextension/neurlfiltermanager/error/configurationinvalid)
- [case configurationDisabled](/documentation/networkextension/neurlfiltermanager/error/configurationdisabled)
- [case configurationStale](/documentation/networkextension/neurlfiltermanager/error/configurationstale)
- [case configurationCannotBeRemoved](/documentation/networkextension/neurlfiltermanager/error/configurationcannotberemoved)
- [case configurationPermissionDenied](/documentation/networkextension/neurlfiltermanager/error/configurationpermissiondenied)
- [case configurationInternalError](/documentation/networkextension/neurlfiltermanager/error/configurationinternalerror)
- [case configurationNotLoaded](/documentation/networkextension/neurlfiltermanager/error/configurationnotloaded)

##### Server errors

- [case serverSetupIncomplete](/documentation/networkextension/neurlfiltermanager/error/serversetupincomplete)

##### Extension errors

- [case extensionCancelled](/documentation/networkextension/neurlfiltermanager/error/extensioncancelled)
- [case extensionNotFound](/documentation/networkextension/neurlfiltermanager/error/extensionnotfound)
- [case extensionFailedToLoad](/documentation/networkextension/neurlfiltermanager/error/extensionfailedtoload)

##### Other errors

- [case internalError](/documentation/networkextension/neurlfiltermanager/error/internalerror)
- [case unknown](/documentation/networkextension/neurlfiltermanager/error/unknown)

#### Describing the filter

- [var localizedDescription: LocalizedStringResource?](/documentation/networkextension/neurlfiltermanager/localizeddescription)
- [NEURLFilterControlProvider](/documentation/networkextension/neurlfiltercontrolprovider)

#### Starting and stopping the provider

- [func start() async throws](/documentation/networkextension/neurlfiltercontrolprovider/start())
- [func stop(reason: NEProviderStopReason) async throws](/documentation/networkextension/neurlfiltercontrolprovider/stop(reason:))

#### Fetching a prefilter

- [func fetchPrefilter(existingPrefilterTag: String?) async throws -> NEURLFilterPrefilter?](/documentation/networkextension/neurlfiltercontrolprovider/fetchprefilter(existingprefiltertag:))
- [NEURLFilterPrefilter](/documentation/networkextension/neurlfilterprefilter)

##### Creating a prefilter

- [init(data: NEURLFilterPrefilter.PrefilterData, tag: String, bitCount: Int, hashCount: Int, murmurSeed: UInt32)](/documentation/networkextension/neurlfilterprefilter/init(data:tag:bitcount:hashcount:murmurseed:))

##### Working with prefilter properties

- [let data: NEURLFilterPrefilter.PrefilterData](/documentation/networkextension/neurlfilterprefilter/data)
- [NEURLFilterPrefilter.PrefilterData](/documentation/networkextension/neurlfilterprefilter/prefilterdata)

###### Accessing prefilter data

- [case smallFilter(Data)](/documentation/networkextension/neurlfilterprefilter/prefilterdata/smallfilter(_:))
- [case temporaryFilepath(URL)](/documentation/networkextension/neurlfilterprefilter/prefilterdata/temporaryfilepath(_:))
- [let tag: String](/documentation/networkextension/neurlfilterprefilter/tag)
- [let bitCount: Int](/documentation/networkextension/neurlfilterprefilter/bitcount)
- [let hashCount: Int](/documentation/networkextension/neurlfilterprefilter/hashcount)
- [let murmurSeed: UInt32](/documentation/networkextension/neurlfilterprefilter/murmurseed)
- [NEURLFilterControlProviderConfiguration](/documentation/networkextension/neurlfiltercontrolproviderconfiguration)
- [NEURLFilter](/documentation/networkextension/neurlfilter)

#### Evaluating a URL

- [class func verdict(for: URL) async -> NEURLFilter.Verdict](/documentation/networkextension/neurlfilter/verdict(for:))
- [NEURLFilter.Verdict](/documentation/networkextension/neurlfilter/verdict)

##### Verdicts

- [case allow](/documentation/networkextension/neurlfilter/verdict/allow)
- [case deny](/documentation/networkextension/neurlfilter/verdict/deny)
- [case unknown](/documentation/networkextension/neurlfilter/verdict/unknown)

##### Working with raw values

- [init?(rawValue: Int)](/documentation/networkextension/neurlfilter/verdict/init(rawvalue:))

### Sample code projects

- [Filtering traffic by URL](/documentation/networkextension/filtering-traffic-by-url)
- [Setting up a PIR server for URL filtering](/documentation/networkextension/setting-up-a-pir-server-for-url-filtering)
- [Using the Bloom filter tool to configure a URL filter](/documentation/networkextension/using-the-bloom-filter-tool)

## DNS configurations

- [DNS settings](/documentation/networkextension/dns-settings)

### Essentials

- [Network Extensions Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.networkextension)

### DNS configuration

- [NEDNSSettingsManager](/documentation/networkextension/nednssettingsmanager)

#### Managing DNS configurations

- [class func shared() -> NEDNSSettingsManager](/documentation/networkextension/nednssettingsmanager/shared())
- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nednssettingsmanager/loadfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nednssettingsmanager/savetopreferences(completionhandler:))
- [func removeFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nednssettingsmanager/removefrompreferences(completionhandler:))

#### Accessing DNS configuration properties

- [var isEnabled: Bool](/documentation/networkextension/nednssettingsmanager/isenabled)
- [var dnsSettings: NEDNSSettings?](/documentation/networkextension/nednssettingsmanager/dnssettings)
- [var localizedDescription: String?](/documentation/networkextension/nednssettingsmanager/localizeddescription)
- [var onDemandRules: [NEOnDemandRule]?](/documentation/networkextension/nednssettingsmanager/ondemandrules)

#### Handling errors

- [let NEDNSSettingsErrorDomain: String](/documentation/networkextension/nednssettingserrordomain)
- [NEDNSSettingsManagerError](/documentation/networkextension/nednssettingsmanagererror)

##### Error codes

- [case configurationInvalid](/documentation/networkextension/nednssettingsmanagererror/configurationinvalid)
- [case configurationDisabled](/documentation/networkextension/nednssettingsmanagererror/configurationdisabled)
- [case configurationStale](/documentation/networkextension/nednssettingsmanagererror/configurationstale)
- [case configurationCannotBeRemoved](/documentation/networkextension/nednssettingsmanagererror/configurationcannotberemoved)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nednssettingsmanagererror/init(rawvalue:))
- [NEDNSOverHTTPSSettings](/documentation/networkextension/nednsoverhttpssettings)

#### Configuring server properties

- [var serverURL: URL?](/documentation/networkextension/nednsoverhttpssettings/serverurl)
- [init(servers: [String])](/documentation/networkextension/nednssettings/init(servers:))
- [var matchDomains: [String]?](/documentation/networkextension/nednssettings/matchdomains)

#### Configuring client properties

- [var identityReference: Data?](/documentation/networkextension/nednsoverhttpssettings/identityreference)
- [NEDNSOverTLSSettings](/documentation/networkextension/nednsovertlssettings)

#### Configuring server properties

- [var serverName: String?](/documentation/networkextension/nednsovertlssettings/servername)
- [init(servers: [String])](/documentation/networkextension/nednssettings/init(servers:))
- [var matchDomains: [String]?](/documentation/networkextension/nednssettings/matchdomains)

#### Configuring client properties

- [var identityReference: Data?](/documentation/networkextension/nednsovertlssettings/identityreference)
- [DNS proxy provider](/documentation/networkextension/dns-proxy-provider)

### Essentials

- [Network Extensions Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.networking.networkextension)

### Provider

- [NEDNSProxyProvider](/documentation/networkextension/nednsproxyprovider)

#### Managing the DNS proxy life cycle

- [func startProxy(options: [String : Any]?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nednsproxyprovider/startproxy(options:completionhandler:))
- [func stopProxy(with: NEProviderStopReason, completionHandler: () -> Void)](/documentation/networkextension/nednsproxyprovider/stopproxy(with:completionhandler:))
- [func cancelProxyWithError((any Error)?)](/documentation/networkextension/nednsproxyprovider/cancelproxywitherror(_:))

#### Handling proxied DNS flow

- [func handleNewFlow(NEAppProxyFlow) -> Bool](/documentation/networkextension/nednsproxyprovider/handlenewflow(_:))
- [func handleNewUDPFlow(NEAppProxyUDPFlow, initialRemoteEndpoint: NWEndpoint) -> Bool](/documentation/networkextension/nednsproxyprovider/handlenewudpflow(_:initialremoteendpoint:))

#### Getting system DNS settings

- [var systemDNSSettings: [NEDNSSettings]?](/documentation/networkextension/nednsproxyprovider/systemdnssettings)
- [NEDNSSettings](/documentation/networkextension/nednssettings)

#### Initializing DNS settings

- [init(servers: [String])](/documentation/networkextension/nednssettings/init(servers:))

#### Accessing DNS properties

- [var servers: [String]](/documentation/networkextension/nednssettings/servers)
- [var searchDomains: [String]?](/documentation/networkextension/nednssettings/searchdomains)
- [var domainName: String?](/documentation/networkextension/nednssettings/domainname)
- [var matchDomains: [String]?](/documentation/networkextension/nednssettings/matchdomains)
- [var matchDomainsNoSearch: Bool](/documentation/networkextension/nednssettings/matchdomainsnosearch)
- [var dnsProtocol: NEDNSProtocol](/documentation/networkextension/nednssettings/dnsprotocol)
- [NEDNSProtocol](/documentation/networkextension/nednsprotocol)

##### DNS protocols

- [case cleartext](/documentation/networkextension/nednsprotocol/cleartext)
- [case TLS](/documentation/networkextension/nednsprotocol/tls)
- [case HTTPS](/documentation/networkextension/nednsprotocol/https)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nednsprotocol/init(rawvalue:))

#### Instance Properties

- [var allowFailover: Bool](/documentation/networkextension/nednssettings/allowfailover)

### Handling flows

- [NEAppProxyTCPFlow](/documentation/networkextension/neappproxytcpflow)

#### Handling flow data

- [func write(Data, withCompletionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxytcpflow/write(_:withcompletionhandler:))
- [func readData(completionHandler: (Data?, (any Error)?) -> Void)](/documentation/networkextension/neappproxytcpflow/readdata(completionhandler:))

#### Getting flow information

- [var remoteEndpoint: NWEndpoint](/documentation/networkextension/neappproxytcpflow/remoteendpoint)

#### Instance Properties

- [var remoteFlowEndpoint: NWEndpoint](/documentation/networkextension/neappproxytcpflow/remoteflowendpoint-4r7v1)
- [NEAppProxyUDPFlow](/documentation/networkextension/neappproxyudpflow)

#### Handling flow data

- [func readDatagrams(completionHandler: ([Data]?, [NWEndpoint]?, (any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/readdatagrams(completionhandler:)-9z8gw)
- [func writeDatagrams([Data], sentBy: [NWEndpoint], completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/writedatagrams(_:sentby:completionhandler:))

#### Getting flow information

- [var localEndpoint: NWEndpoint?](/documentation/networkextension/neappproxyudpflow/localendpoint)

#### Instance Properties

- [var localFlowEndpoint: NWEndpoint?](/documentation/networkextension/neappproxyudpflow/localflowendpoint-7ukb6)

#### Instance Methods

- [func readDatagrams() async -> ([(Data, NWEndpoint)]?, (any Error)?)](/documentation/networkextension/neappproxyudpflow/readdatagrams())
- [func readDatagrams(completionHandler: ([(Data, NWEndpoint)]?, (any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/readdatagrams(completionhandler:)-71k28)
- [func writeDatagrams([(Data, NWEndpoint)]) async throws](/documentation/networkextension/neappproxyudpflow/writedatagrams(_:))
- [func writeDatagrams([(Data, NWEndpoint)], completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyudpflow/writedatagrams(_:completionhandler:))
- [NEAppProxyFlow](/documentation/networkextension/neappproxyflow)

#### Managing the flow life cycle

- [func open(withLocalEndpoint: NWHostEndpoint?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyflow/open(withlocalendpoint:completionhandler:))
- [func closeReadWithError((any Error)?)](/documentation/networkextension/neappproxyflow/closereadwitherror(_:))
- [func closeWriteWithError((any Error)?)](/documentation/networkextension/neappproxyflow/closewritewitherror(_:))

#### Accessing flow information

- [var metaData: NEFlowMetaData](/documentation/networkextension/neappproxyflow/metadata)
- [func setMetadata(nw_parameters_t)](/documentation/networkextension/neappproxyflow/setmetadata(_:))
- [nw_parameters_t](/documentation/network/nw_parameters_t)
- [var isBound: Bool](/documentation/networkextension/neappproxyflow/isbound)
- [var networkInterface: nw_interface_t?](/documentation/networkextension/neappproxyflow/networkinterface)
- [nw_interface_type_t](/documentation/network/nw_interface_type_t)
- [var remoteHostname: String?](/documentation/networkextension/neappproxyflow/remotehostname)

#### Errors

- [NEAppProxyFlowError](/documentation/networkextension/neappproxyflowerror-swift.struct)

##### Accessing error properties

- [NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/code)

###### Error Codes

- [case notConnected](/documentation/networkextension/neappproxyflowerror-swift.struct/code/notconnected)
- [case peerReset](/documentation/networkextension/neappproxyflowerror-swift.struct/code/peerreset)
- [case hostUnreachable](/documentation/networkextension/neappproxyflowerror-swift.struct/code/hostunreachable)
- [case invalidArgument](/documentation/networkextension/neappproxyflowerror-swift.struct/code/invalidargument)
- [case aborted](/documentation/networkextension/neappproxyflowerror-swift.struct/code/aborted)
- [case refused](/documentation/networkextension/neappproxyflowerror-swift.struct/code/refused)
- [case timedOut](/documentation/networkextension/neappproxyflowerror-swift.struct/code/timedout)
- [case `internal`](/documentation/networkextension/neappproxyflowerror-swift.struct/code/internal)
- [case datagramTooLarge](/documentation/networkextension/neappproxyflowerror-swift.struct/code/datagramtoolarge)
- [case readAlreadyPending](/documentation/networkextension/neappproxyflowerror-swift.struct/code/readalreadypending)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neappproxyflowerror-swift.struct/code/init(rawvalue:))

##### Error codes

- [static var notConnected: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/notconnected)
- [static var peerReset: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/peerreset)
- [static var hostUnreachable: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/hostunreachable)
- [static var invalidArgument: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/invalidargument)
- [static var aborted: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/aborted)
- [static var refused: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/refused)
- [static var timedOut: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/timedout)
- [static var `internal`: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/internal)
- [static var datagramTooLarge: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/datagramtoolarge)
- [static var readAlreadyPending: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/readalreadypending)

##### Type Properties

- [static var errorDomain: String](/documentation/networkextension/neappproxyflowerror-swift.struct/errordomain)
- [let NEAppProxyErrorDomain: String](/documentation/networkextension/neappproxyerrordomain)
- [NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/code)

##### Error Codes

- [case notConnected](/documentation/networkextension/neappproxyflowerror-swift.struct/code/notconnected)
- [case peerReset](/documentation/networkextension/neappproxyflowerror-swift.struct/code/peerreset)
- [case hostUnreachable](/documentation/networkextension/neappproxyflowerror-swift.struct/code/hostunreachable)
- [case invalidArgument](/documentation/networkextension/neappproxyflowerror-swift.struct/code/invalidargument)
- [case aborted](/documentation/networkextension/neappproxyflowerror-swift.struct/code/aborted)
- [case refused](/documentation/networkextension/neappproxyflowerror-swift.struct/code/refused)
- [case timedOut](/documentation/networkextension/neappproxyflowerror-swift.struct/code/timedout)
- [case `internal`](/documentation/networkextension/neappproxyflowerror-swift.struct/code/internal)
- [case datagramTooLarge](/documentation/networkextension/neappproxyflowerror-swift.struct/code/datagramtoolarge)
- [case readAlreadyPending](/documentation/networkextension/neappproxyflowerror-swift.struct/code/readalreadypending)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neappproxyflowerror-swift.struct/code/init(rawvalue:))
- [NEAppProxyFlowError](/documentation/networkextension/neappproxyflowerror-swift.struct)

##### Accessing error properties

- [NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/code)

###### Error Codes

- [case notConnected](/documentation/networkextension/neappproxyflowerror-swift.struct/code/notconnected)
- [case peerReset](/documentation/networkextension/neappproxyflowerror-swift.struct/code/peerreset)
- [case hostUnreachable](/documentation/networkextension/neappproxyflowerror-swift.struct/code/hostunreachable)
- [case invalidArgument](/documentation/networkextension/neappproxyflowerror-swift.struct/code/invalidargument)
- [case aborted](/documentation/networkextension/neappproxyflowerror-swift.struct/code/aborted)
- [case refused](/documentation/networkextension/neappproxyflowerror-swift.struct/code/refused)
- [case timedOut](/documentation/networkextension/neappproxyflowerror-swift.struct/code/timedout)
- [case `internal`](/documentation/networkextension/neappproxyflowerror-swift.struct/code/internal)
- [case datagramTooLarge](/documentation/networkextension/neappproxyflowerror-swift.struct/code/datagramtoolarge)
- [case readAlreadyPending](/documentation/networkextension/neappproxyflowerror-swift.struct/code/readalreadypending)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neappproxyflowerror-swift.struct/code/init(rawvalue:))

##### Error codes

- [static var notConnected: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/notconnected)
- [static var peerReset: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/peerreset)
- [static var hostUnreachable: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/hostunreachable)
- [static var invalidArgument: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/invalidargument)
- [static var aborted: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/aborted)
- [static var refused: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/refused)
- [static var timedOut: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/timedout)
- [static var `internal`: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/internal)
- [static var datagramTooLarge: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/datagramtoolarge)
- [static var readAlreadyPending: NEAppProxyFlowError.Code](/documentation/networkextension/neappproxyflowerror-swift.struct/readalreadypending)

##### Type Properties

- [static var errorDomain: String](/documentation/networkextension/neappproxyflowerror-swift.struct/errordomain)

#### Instance Properties

- [var interface: NWInterface?](/documentation/networkextension/neappproxyflow/interface)

#### Instance Methods

- [func open(withLocalFlowEndpoint: NWEndpoint?) async throws](/documentation/networkextension/neappproxyflow/open(withlocalflowendpoint:))
- [func open(withLocalFlowEndpoint: NWEndpoint?, completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neappproxyflow/open(withlocalflowendpoint:completionhandler:))
- [func setMetadata(on: NWParameters)](/documentation/networkextension/neappproxyflow/setmetadata(on:))

### Configuration

- [NEDNSProxyManager](/documentation/networkextension/nednsproxymanager)

#### Managing the DNS proxy configuration

- [class func shared() -> NEDNSProxyManager](/documentation/networkextension/nednsproxymanager/shared())
- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nednsproxymanager/loadfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nednsproxymanager/savetopreferences(completionhandler:))
- [func removeFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/nednsproxymanager/removefrompreferences(completionhandler:))

#### Accessing DNS proxy configuration properties

- [var isEnabled: Bool](/documentation/networkextension/nednsproxymanager/isenabled)
- [var providerProtocol: NEDNSProxyProviderProtocol?](/documentation/networkextension/nednsproxymanager/providerprotocol)
- [var localizedDescription: String?](/documentation/networkextension/nednsproxymanager/localizeddescription)

#### Notifications

- [static let NEDNSProxyConfigurationDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nednsproxyconfigurationdidchange)

#### Errors

- [let NEDNSProxyErrorDomain: String](/documentation/networkextension/nednsproxyerrordomain)
- [NEDNSProxyManagerError](/documentation/networkextension/nednsproxymanagererror)

##### Enumeration Cases

- [case configurationInvalid](/documentation/networkextension/nednsproxymanagererror/configurationinvalid)
- [case configurationDisabled](/documentation/networkextension/nednsproxymanagererror/configurationdisabled)
- [case configurationStale](/documentation/networkextension/nednsproxymanagererror/configurationstale)
- [case configurationCannotBeRemoved](/documentation/networkextension/nednsproxymanagererror/configurationcannotberemoved)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nednsproxymanagererror/init(rawvalue:))
- [NEDNSProxyProviderProtocol](/documentation/networkextension/nednsproxyproviderprotocol)

#### Accessing the DNS proxy configuration

- [var providerConfiguration: [String : Any]?](/documentation/networkextension/nednsproxyproviderprotocol/providerconfiguration)
- [var providerBundleIdentifier: String?](/documentation/networkextension/nednsproxyproviderprotocol/providerbundleidentifier)

## Local networking

- [Local push connectivity](/documentation/networkextension/local-push-connectivity)

### Essentials

- [NEAppPushManager](/documentation/networkextension/neapppushmanager)

#### Matching Wi-Fi networks

- [var matchSSIDs: [String]](/documentation/networkextension/neapppushmanager/matchssids)
- [var matchPrivateLTENetworks: [NEPrivateLTENetwork]](/documentation/networkextension/neapppushmanager/matchprivateltenetworks)
- [NEPrivateLTENetwork](/documentation/networkextension/neprivateltenetwork)

##### Accessing network properties

- [var mobileCountryCode: String](/documentation/networkextension/neprivateltenetwork/mobilecountrycode)
- [var mobileNetworkCode: String](/documentation/networkextension/neprivateltenetwork/mobilenetworkcode)
- [var trackingAreaCode: String?](/documentation/networkextension/neprivateltenetwork/trackingareacode)

#### Persisting manager settings

- [func loadFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neapppushmanager/loadfrompreferences(completionhandler:))
- [class func loadAllFromPreferences(completionHandler: ([NEAppPushManager]?, (any Error)?) -> Void)](/documentation/networkextension/neapppushmanager/loadallfrompreferences(completionhandler:))
- [func saveToPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neapppushmanager/savetopreferences(completionhandler:))
- [func removeFromPreferences(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neapppushmanager/removefrompreferences(completionhandler:))

#### Working with a delegate

- [var delegate: (any NEAppPushDelegate)?](/documentation/networkextension/neapppushmanager/delegate)
- [NEAppPushDelegate](/documentation/networkextension/neapppushdelegate)

##### Receiving calls

- [func appPushManager(NEAppPushManager, didReceiveIncomingCallWithUserInfo: [AnyHashable : Any])](/documentation/networkextension/neapppushdelegate/apppushmanager(_:didreceiveincomingcallwithuserinfo:))

#### Inspecting manager properties

- [var isActive: Bool](/documentation/networkextension/neapppushmanager/isactive)
- [var isEnabled: Bool](/documentation/networkextension/neapppushmanager/isenabled)
- [var localizedDescription: String?](/documentation/networkextension/neapppushmanager/localizeddescription)

#### Inspecting provider properties

- [var providerConfiguration: [String : Any]](/documentation/networkextension/neapppushmanager/providerconfiguration)
- [var providerBundleIdentifier: String?](/documentation/networkextension/neapppushmanager/providerbundleidentifier)

#### Operating over Ethernet

- [var matchEthernet: Bool](/documentation/networkextension/neapppushmanager/matchethernet)

#### Handling errors

- [NEAppPushManagerError](/documentation/networkextension/neapppushmanagererror-swift.struct)

##### Inspecting error properties

- [NEAppPushManagerError.Code](/documentation/networkextension/neapppushmanagererror-swift.struct/code)

###### Error codes

- [case configurationInvalid](/documentation/networkextension/neapppushmanagererror-swift.struct/code/configurationinvalid)
- [case configurationNotLoaded](/documentation/networkextension/neapppushmanagererror-swift.struct/code/configurationnotloaded)
- [case inactiveSession](/documentation/networkextension/neapppushmanagererror-swift.struct/code/inactivesession)
- [case internalError](/documentation/networkextension/neapppushmanagererror-swift.struct/code/internalerror)

###### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neapppushmanagererror-swift.struct/code/init(rawvalue:))

##### Error constants

- [static var configurationInvalid: NEAppPushManagerError.Code](/documentation/networkextension/neapppushmanagererror-swift.struct/configurationinvalid)
- [static var configurationNotLoaded: NEAppPushManagerError.Code](/documentation/networkextension/neapppushmanagererror-swift.struct/configurationnotloaded)
- [static var inactiveSession: NEAppPushManagerError.Code](/documentation/networkextension/neapppushmanagererror-swift.struct/inactivesession)
- [static var internalError: NEAppPushManagerError.Code](/documentation/networkextension/neapppushmanagererror-swift.struct/internalerror)

##### Type Properties

- [static var errorDomain: String](/documentation/networkextension/neapppushmanagererror-swift.struct/errordomain)
- [let NEAppPushErrorDomain: String](/documentation/networkextension/neapppusherrordomain)
- [NEAppPushManagerError.Code](/documentation/networkextension/neapppushmanagererror-swift.struct/code)

##### Error codes

- [case configurationInvalid](/documentation/networkextension/neapppushmanagererror-swift.struct/code/configurationinvalid)
- [case configurationNotLoaded](/documentation/networkextension/neapppushmanagererror-swift.struct/code/configurationnotloaded)
- [case inactiveSession](/documentation/networkextension/neapppushmanagererror-swift.struct/code/inactivesession)
- [case internalError](/documentation/networkextension/neapppushmanagererror-swift.struct/code/internalerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/neapppushmanagererror-swift.struct/code/init(rawvalue:))
- [NEAppPushProvider](/documentation/networkextension/neapppushprovider)

#### Inspecting provider properties

- [var providerConfiguration: [String : Any]?](/documentation/networkextension/neapppushprovider/providerconfiguration)

#### Implementing provider life cycle

- [func start()](/documentation/networkextension/neapppushprovider/start())
- [func start(completionHandler: ((any Error)?) -> Void)](/documentation/networkextension/neapppushprovider/start(completionhandler:))
- [func stop(with: NEProviderStopReason, completionHandler: () -> Void)](/documentation/networkextension/neapppushprovider/stop(with:completionhandler:))
- [func handleTimerEvent()](/documentation/networkextension/neapppushprovider/handletimerevent())

#### Receiving local events

- [func reportIncomingCall(userInfo: [AnyHashable : Any])](/documentation/networkextension/neapppushprovider/reportincomingcall(userinfo:))
- [func reportPushToTalkMessage(userInfo: [AnyHashable : Any])](/documentation/networkextension/neapppushprovider/reportpushtotalkmessage(userinfo:))

#### Operating over Ethernet

- [func unmatchEthernet()](/documentation/networkextension/neapppushprovider/unmatchethernet())
- [Maintaining a Reliable Network Connection](/documentation/networkextension/maintaining-a-reliable-network-connection)
- [Receiving Voice and Text Communications on a Local Network](/documentation/networkextension/receiving-voice-and-text-communications-on-a-local-network)

## App extensions

- [NEAppExtensionConfiguration](/documentation/networkextension/neappextensionconfiguration)

### Communicating over XPC

- [func accept(connection: NSXPCConnection) -> Bool](/documentation/networkextension/neappextensionconfiguration/accept(connection:))

## Protocols

- [NEAppProxyUDPFlowHandling](/documentation/networkextension/neappproxyudpflowhandling)

### Instance Methods

- [func handleNewUDPFlow(NEAppProxyUDPFlow, initialRemoteFlowEndpoint: NWEndpoint) -> Bool](/documentation/networkextension/neappproxyudpflowhandling/handlenewudpflow(_:initialremoteflowendpoint:))

## Structures

- [NETunnelProviderError](/documentation/networkextension/netunnelprovidererror-swift.struct)

### Error information

- [NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/code)

#### Error codes

- [case networkSettingsInvalid](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsinvalid)
- [case networkSettingsCanceled](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingscanceled)
- [case networkSettingsFailed](/documentation/networkextension/netunnelprovidererror-swift.struct/code/networksettingsfailed)

#### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/netunnelprovidererror-swift.struct/code/init(rawvalue:))

### Error codes

- [static var networkSettingsInvalid: NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/networksettingsinvalid)
- [static var networkSettingsCanceled: NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/networksettingscanceled)
- [static var networkSettingsFailed: NETunnelProviderError.Code](/documentation/networkextension/netunnelprovidererror-swift.struct/networksettingsfailed)

### Type Properties

- [static var errorDomain: String](/documentation/networkextension/netunnelprovidererror-swift.struct/errordomain)
- [NEVPNError](/documentation/networkextension/nevpnerror-swift.struct)

### Inspecting error properties

- [NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/code)

#### Error codes

- [case configurationDisabled](/documentation/networkextension/nevpnerror-swift.struct/code/configurationdisabled)
- [case configurationInvalid](/documentation/networkextension/nevpnerror-swift.struct/code/configurationinvalid)
- [case connectionFailed](/documentation/networkextension/nevpnerror-swift.struct/code/connectionfailed)
- [case configurationStale](/documentation/networkextension/nevpnerror-swift.struct/code/configurationstale)
- [case configurationReadWriteFailed](/documentation/networkextension/nevpnerror-swift.struct/code/configurationreadwritefailed)
- [case configurationUnknown](/documentation/networkextension/nevpnerror-swift.struct/code/configurationunknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nevpnerror-swift.struct/code/init(rawvalue:))

### Error codes

- [static var configurationDisabled: NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/configurationdisabled)
- [static var configurationInvalid: NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/configurationinvalid)
- [static var connectionFailed: NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/connectionfailed)
- [static var configurationStale: NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/configurationstale)
- [static var configurationReadWriteFailed: NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/configurationreadwritefailed)
- [static var configurationUnknown: NEVPNError.Code](/documentation/networkextension/nevpnerror-swift.struct/configurationunknown)

### Type Properties

- [static var errorDomain: String](/documentation/networkextension/nevpnerror-swift.struct/errordomain)

## Variables

- [let NERelayClientErrorDomain: String](/documentation/networkextension/nerelayclienterrordomain)

## Enumerations

- [NERelayManagerClientError](/documentation/networkextension/nerelaymanagerclienterror)

### Enumeration Cases

- [case certificateExpired](/documentation/networkextension/nerelaymanagerclienterror/certificateexpired)
- [case certificateInvalid](/documentation/networkextension/nerelaymanagerclienterror/certificateinvalid)
- [case certificateMissing](/documentation/networkextension/nerelaymanagerclienterror/certificatemissing)
- [case dnsFailed](/documentation/networkextension/nerelaymanagerclienterror/dnsfailed)
- [case none](/documentation/networkextension/nerelaymanagerclienterror/none)
- [case other](/documentation/networkextension/nerelaymanagerclienterror/other)
- [case serverCertificateExpired](/documentation/networkextension/nerelaymanagerclienterror/servercertificateexpired)
- [case serverCertificateInvalid](/documentation/networkextension/nerelaymanagerclienterror/servercertificateinvalid)
- [case serverDisconnected](/documentation/networkextension/nerelaymanagerclienterror/serverdisconnected)
- [case serverUnreachable](/documentation/networkextension/nerelaymanagerclienterror/serverunreachable)

### Initializers

- [init?(rawValue: Int)](/documentation/networkextension/nerelaymanagerclienterror/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
