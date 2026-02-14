# CFNetwork Documentation

Source: https://sosumi.ai/documentation/cfnetwork

---
title: CFNetwork
source: https://developer.apple.com/documentation/cfnetwork
timestamp: 2026-02-13T18:54:43.411Z
---

## Errors

- [CFNetworkErrors](/documentation/cfnetwork/cfnetworkerrors)

### Constants

- [case cfHostErrorHostNotFound](/documentation/cfnetwork/cfnetworkerrors/cfhosterrorhostnotfound)
- [case cfHostErrorUnknown](/documentation/cfnetwork/cfnetworkerrors/cfhosterrorunknown)
- [case cfsocksErrorUnknownClientVersion](/documentation/cfnetwork/cfnetworkerrors/cfsockserrorunknownclientversion)
- [case cfsocksErrorUnsupportedServerVersion](/documentation/cfnetwork/cfnetworkerrors/cfsockserrorunsupportedserverversion)
- [case cfsocks4ErrorRequestFailed](/documentation/cfnetwork/cfnetworkerrors/cfsocks4errorrequestfailed)
- [case cfsocks4ErrorIdentdFailed](/documentation/cfnetwork/cfnetworkerrors/cfsocks4erroridentdfailed)
- [case cfsocks4ErrorIdConflict](/documentation/cfnetwork/cfnetworkerrors/cfsocks4erroridconflict)
- [case cfsocks4ErrorUnknownStatusCode](/documentation/cfnetwork/cfnetworkerrors/cfsocks4errorunknownstatuscode)
- [case cfsocks5ErrorBadState](/documentation/cfnetwork/cfnetworkerrors/cfsocks5errorbadstate)
- [case cfsocks5ErrorBadResponseAddr](/documentation/cfnetwork/cfnetworkerrors/cfsocks5errorbadresponseaddr)
- [case cfsocks5ErrorBadCredentials](/documentation/cfnetwork/cfnetworkerrors/cfsocks5errorbadcredentials)
- [case cfsocks5ErrorUnsupportedNegotiationMethod](/documentation/cfnetwork/cfnetworkerrors/cfsocks5errorunsupportednegotiationmethod)
- [case cfsocks5ErrorNoAcceptableMethod](/documentation/cfnetwork/cfnetworkerrors/cfsocks5errornoacceptablemethod)
- [case cfftpErrorUnexpectedStatusCode](/documentation/cfnetwork/cfnetworkerrors/cfftperrorunexpectedstatuscode)
- [case cfErrorHTTPAuthenticationTypeUnsupported](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpauthenticationtypeunsupported)
- [case cfErrorHTTPBadCredentials](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpbadcredentials)
- [case cfErrorHTTPConnectionLost](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpconnectionlost)
- [case cfErrorHTTPParseFailure](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpparsefailure)
- [case cfErrorHTTPRedirectionLoopDetected](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpredirectionloopdetected)
- [case cfErrorHTTPBadURL](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpbadurl)
- [case cfErrorHTTPProxyConnectionFailure](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpproxyconnectionfailure)
- [case cfErrorHTTPBadProxyCredentials](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpbadproxycredentials)
- [case cfErrorPACFileError](/documentation/cfnetwork/cfnetworkerrors/cferrorpacfileerror)
- [case cfErrorPACFileAuth](/documentation/cfnetwork/cfnetworkerrors/cferrorpacfileauth)
- [case cfErrorHTTPSProxyConnectionFailure](/documentation/cfnetwork/cfnetworkerrors/cferrorhttpsproxyconnectionfailure)
- [case cfStreamErrorHTTPSProxyFailureUnexpectedResponseToCONNECTMethod](/documentation/cfnetwork/cfnetworkerrors/cfstreamerrorhttpsproxyfailureunexpectedresponsetoconnectmethod)
- [case cfurlErrorUnknown](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorunknown)
- [case cfurlErrorCancelled](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcancelled)
- [case cfurlErrorBadURL](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorbadurl)
- [case cfurlErrorTimedOut](/documentation/cfnetwork/cfnetworkerrors/cfurlerrortimedout)
- [case cfurlErrorUnsupportedURL](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorunsupportedurl)
- [case cfurlErrorCannotFindHost](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotfindhost)
- [case cfurlErrorCannotConnectToHost](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotconnecttohost)
- [case cfurlErrorNetworkConnectionLost](/documentation/cfnetwork/cfnetworkerrors/cfurlerrornetworkconnectionlost)
- [case cfurlErrorDNSLookupFailed](/documentation/cfnetwork/cfnetworkerrors/cfurlerrordnslookupfailed)
- [case cfurlErrorHTTPTooManyRedirects](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorhttptoomanyredirects)
- [case cfurlErrorResourceUnavailable](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorresourceunavailable)
- [case cfurlErrorNotConnectedToInternet](/documentation/cfnetwork/cfnetworkerrors/cfurlerrornotconnectedtointernet)
- [case cfurlErrorRedirectToNonExistentLocation](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorredirecttononexistentlocation)
- [case cfurlErrorBadServerResponse](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorbadserverresponse)
- [case cfurlErrorUserCancelledAuthentication](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorusercancelledauthentication)
- [case cfurlErrorUserAuthenticationRequired](/documentation/cfnetwork/cfnetworkerrors/cfurlerroruserauthenticationrequired)
- [case cfurlErrorZeroByteResource](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorzerobyteresource)
- [case cfurlErrorCannotDecodeRawData](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotdecoderawdata)
- [case cfurlErrorCannotDecodeContentData](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotdecodecontentdata)
- [case cfurlErrorCannotParseResponse](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotparseresponse)
- [case cfurlErrorInternationalRoamingOff](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorinternationalroamingoff)
- [case cfurlErrorCallIsActive](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcallisactive)
- [case cfurlErrorDataNotAllowed](/documentation/cfnetwork/cfnetworkerrors/cfurlerrordatanotallowed)
- [case cfurlErrorRequestBodyStreamExhausted](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorrequestbodystreamexhausted)
- [case cfurlErrorFileDoesNotExist](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorfiledoesnotexist)
- [case cfurlErrorFileIsDirectory](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorfileisdirectory)
- [case cfurlErrorNoPermissionsToReadFile](/documentation/cfnetwork/cfnetworkerrors/cfurlerrornopermissionstoreadfile)
- [case cfurlErrorDataLengthExceedsMaximum](/documentation/cfnetwork/cfnetworkerrors/cfurlerrordatalengthexceedsmaximum)
- [case cfurlErrorSecureConnectionFailed](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorsecureconnectionfailed)
- [case cfurlErrorServerCertificateHasBadDate](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorservercertificatehasbaddate)
- [case cfurlErrorServerCertificateUntrusted](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorservercertificateuntrusted)
- [case cfurlErrorServerCertificateHasUnknownRoot](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorservercertificatehasunknownroot)
- [case cfurlErrorServerCertificateNotYetValid](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorservercertificatenotyetvalid)
- [case cfurlErrorClientCertificateRejected](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorclientcertificaterejected)
- [case cfurlErrorClientCertificateRequired](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorclientcertificaterequired)
- [case cfurlErrorCannotLoadFromNetwork](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotloadfromnetwork)
- [case cfurlErrorCannotCreateFile](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotcreatefile)
- [case cfurlErrorCannotOpenFile](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotopenfile)
- [case cfurlErrorCannotCloseFile](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotclosefile)
- [case cfurlErrorCannotWriteToFile](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotwritetofile)
- [case cfurlErrorCannotRemoveFile](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotremovefile)
- [case cfurlErrorCannotMoveFile](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorcannotmovefile)
- [case cfurlErrorDownloadDecodingFailedMidStream](/documentation/cfnetwork/cfnetworkerrors/cfurlerrordownloaddecodingfailedmidstream)
- [case cfurlErrorDownloadDecodingFailedToComplete](/documentation/cfnetwork/cfnetworkerrors/cfurlerrordownloaddecodingfailedtocomplete)
- [case cfhttpCookieCannotParseCookieFile](/documentation/cfnetwork/cfnetworkerrors/cfhttpcookiecannotparsecookiefile)
- [case cfNetServiceErrorUnknown](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrorunknown)
- [case cfNetServiceErrorCollision](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrorcollision)
- [case cfNetServiceErrorNotFound](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrornotfound)
- [case cfNetServiceErrorInProgress](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrorinprogress)
- [case cfNetServiceErrorBadArgument](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrorbadargument)
- [case cfNetServiceErrorCancel](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrorcancel)
- [case cfNetServiceErrorInvalid](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrorinvalid)
- [case cfNetServiceErrorTimeout](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrortimeout)
- [case cfNetServiceErrorDNSServiceFailure](/documentation/cfnetwork/cfnetworkerrors/cfnetserviceerrordnsservicefailure)
- [case cfurlErrorAppTransportSecurityRequiresSecureConnection](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorapptransportsecurityrequiressecureconnection)
- [case cfurlErrorBackgroundSessionInUseByAnotherProcess](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorbackgroundsessioninusebyanotherprocess)
- [case cfurlErrorBackgroundSessionWasDisconnected](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorbackgroundsessionwasdisconnected)

### Enumeration Cases

- [case cfurlErrorFileOutsideSafeArea](/documentation/cfnetwork/cfnetworkerrors/cfurlerrorfileoutsidesafearea)

### Initializers

- [init?(rawValue: Int32)](/documentation/cfnetwork/cfnetworkerrors/init(rawvalue:))
- [Error Dictionary Keys](/documentation/cfnetwork/error-dictionary-keys)

### Constants

- [let kCFURLErrorFailingURLErrorKey: CFString](/documentation/cfnetwork/kcfurlerrorfailingurlerrorkey)
- [let kCFURLErrorFailingURLStringErrorKey: CFString](/documentation/cfnetwork/kcfurlerrorfailingurlstringerrorkey)
- [let kCFGetAddrInfoFailureKey: CFString](/documentation/cfnetwork/kcfgetaddrinfofailurekey)
- [let kCFSOCKSStatusCodeKey: CFString](/documentation/cfnetwork/kcfsocksstatuscodekey)
- [let kCFSOCKSVersionKey: CFString](/documentation/cfnetwork/kcfsocksversionkey)
- [let kCFSOCKSNegotiationMethodKey: CFString](/documentation/cfnetwork/kcfsocksnegotiationmethodkey)
- [let kCFDNSServiceFailureKey: CFString](/documentation/cfnetwork/kcfdnsservicefailurekey)
- [let kCFFTPStatusCodeKey: CFString](/documentation/cfnetwork/kcfftpstatuscodekey)
- [Error Domains](/documentation/cfnetwork/error-domains)

### Constants

- [let kCFErrorDomainCFNetwork: CFString](/documentation/cfnetwork/kcferrordomaincfnetwork)
- [let kCFErrorDomainWinSock: CFString](/documentation/cfnetwork/kcferrordomainwinsock)

## Hosts

- [CFHost](/documentation/cfnetwork/cfhost)
- [CFHostInfoType](/documentation/cfnetwork/cfhostinfotype)

### Constants

- [case addresses](/documentation/cfnetwork/cfhostinfotype/addresses)
- [case names](/documentation/cfnetwork/cfhostinfotype/names)
- [case reachability](/documentation/cfnetwork/cfhostinfotype/reachability)

### Initializers

- [init?(rawValue: Int32)](/documentation/cfnetwork/cfhostinfotype/init(rawvalue:))
- [CFHostClientContext](/documentation/cfnetwork/cfhostclientcontext)

### Initializers

- [init()](/documentation/cfnetwork/cfhostclientcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer?, retain: CFAllocatorRetainCallBack?, release: CFAllocatorReleaseCallBack?, copyDescription: CFAllocatorCopyDescriptionCallBack?)](/documentation/cfnetwork/cfhostclientcontext/init(version:info:retain:release:copydescription:))

### Instance Properties

- [var copyDescription: CFAllocatorCopyDescriptionCallBack?](/documentation/cfnetwork/cfhostclientcontext/copydescription)
- [var info: UnsafeMutableRawPointer?](/documentation/cfnetwork/cfhostclientcontext/info)
- [var release: CFAllocatorReleaseCallBack?](/documentation/cfnetwork/cfhostclientcontext/release)
- [var retain: CFAllocatorRetainCallBack?](/documentation/cfnetwork/cfhostclientcontext/retain)
- [var version: CFIndex](/documentation/cfnetwork/cfhostclientcontext/version)
- [func CFHostCancelInfoResolution(CFHost, CFHostInfoType)](/documentation/cfnetwork/cfhostcancelinforesolution(_:_:))
- [func CFHostCreateCopy(CFAllocator?, CFHost) -> Unmanaged<CFHost>](/documentation/cfnetwork/cfhostcreatecopy(_:_:))
- [func CFHostCreateWithAddress(CFAllocator?, CFData) -> Unmanaged<CFHost>](/documentation/cfnetwork/cfhostcreatewithaddress(_:_:))
- [func CFHostCreateWithName(CFAllocator?, CFString) -> Unmanaged<CFHost>](/documentation/cfnetwork/cfhostcreatewithname(_:_:))
- [func CFHostGetAddressing(CFHost, UnsafeMutablePointer<DarwinBoolean>?) -> Unmanaged<CFArray>?](/documentation/cfnetwork/cfhostgetaddressing(_:_:))
- [func CFHostGetNames(CFHost, UnsafeMutablePointer<DarwinBoolean>?) -> Unmanaged<CFArray>?](/documentation/cfnetwork/cfhostgetnames(_:_:))
- [func CFHostGetReachability(CFHost, UnsafeMutablePointer<DarwinBoolean>?) -> Unmanaged<CFData>?](/documentation/cfnetwork/cfhostgetreachability(_:_:))
- [func CFHostGetTypeID() -> CFTypeID](/documentation/cfnetwork/cfhostgettypeid())
- [func CFHostScheduleWithRunLoop(CFHost, CFRunLoop, CFString)](/documentation/cfnetwork/cfhostschedulewithrunloop(_:_:_:))
- [func CFHostSetClient(CFHost, CFHostClientCallBack?, UnsafeMutablePointer<CFHostClientContext>?) -> Bool](/documentation/cfnetwork/cfhostsetclient(_:_:_:))
- [func CFHostStartInfoResolution(CFHost, CFHostInfoType, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfhoststartinforesolution(_:_:_:))
- [func CFHostUnscheduleFromRunLoop(CFHost, CFRunLoop, CFString)](/documentation/cfnetwork/cfhostunschedulefromrunloop(_:_:_:))

## Global Proxy Configuration

- [func CFNetworkCopyProxiesForURL(CFURL, CFDictionary) -> Unmanaged<CFArray>](/documentation/cfnetwork/cfnetworkcopyproxiesforurl(_:_:))
- [func CFNetworkCopyProxiesForAutoConfigurationScript(CFString, CFURL, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<CFArray>?](/documentation/cfnetwork/cfnetworkcopyproxiesforautoconfigurationscript(_:_:_:))
- [func CFNetworkExecuteProxyAutoConfigurationScript(CFString, CFURL, CFProxyAutoConfigurationResultCallback, UnsafeMutablePointer<CFStreamClientContext>) -> CFRunLoopSource](/documentation/cfnetwork/cfnetworkexecuteproxyautoconfigurationscript(_:_:_:_:))
- [func CFNetworkExecuteProxyAutoConfigurationURL(CFURL, CFURL, CFProxyAutoConfigurationResultCallback, UnsafeMutablePointer<CFStreamClientContext>) -> CFRunLoopSource](/documentation/cfnetwork/cfnetworkexecuteproxyautoconfigurationurl(_:_:_:_:))
- [func CFNetworkCopySystemProxySettings() -> Unmanaged<CFDictionary>?](/documentation/cfnetwork/cfnetworkcopysystemproxysettings())
- [CFProxyAutoConfigurationResultCallback](/documentation/cfnetwork/cfproxyautoconfigurationresultcallback)
- [Property Keys](/documentation/cfnetwork/property-keys)

### Constants

- [let kCFProxyAutoConfigurationHTTPResponseKey: CFString](/documentation/cfnetwork/kcfproxyautoconfigurationhttpresponsekey)
- [let kCFProxyAutoConfigurationJavaScriptKey: CFString](/documentation/cfnetwork/kcfproxyautoconfigurationjavascriptkey)
- [let kCFProxyAutoConfigurationURLKey: CFString](/documentation/cfnetwork/kcfproxyautoconfigurationurlkey)
- [let kCFProxyHostNameKey: CFString](/documentation/cfnetwork/kcfproxyhostnamekey)
- [let kCFProxyPasswordKey: CFString](/documentation/cfnetwork/kcfproxypasswordkey)
- [let kCFProxyPortNumberKey: CFString](/documentation/cfnetwork/kcfproxyportnumberkey)
- [let kCFProxyTypeKey: CFString](/documentation/cfnetwork/kcfproxytypekey)
- [let kCFProxyUsernameKey: CFString](/documentation/cfnetwork/kcfproxyusernamekey)
- [Proxy Types](/documentation/cfnetwork/proxy-types)

### Constants

- [let kCFProxyTypeNone: CFString](/documentation/cfnetwork/kcfproxytypenone)
- [let kCFProxyTypeAutoConfigurationURL: CFString](/documentation/cfnetwork/kcfproxytypeautoconfigurationurl)
- [let kCFProxyTypeAutoConfigurationJavaScript: CFString](/documentation/cfnetwork/kcfproxytypeautoconfigurationjavascript)
- [let kCFProxyTypeFTP: CFString](/documentation/cfnetwork/kcfproxytypeftp)
- [let kCFProxyTypeHTTP: CFString](/documentation/cfnetwork/kcfproxytypehttp)
- [let kCFProxyTypeHTTPS: CFString](/documentation/cfnetwork/kcfproxytypehttps)
- [let kCFProxyTypeSOCKS: CFString](/documentation/cfnetwork/kcfproxytypesocks)
- [Global Proxy Settings Constants](/documentation/cfnetwork/global-proxy-settings-constants)

### Constants

- [let kCFNetworkProxiesExceptionsList: CFString](/documentation/cfnetwork/kcfnetworkproxiesexceptionslist)
- [let kCFNetworkProxiesExcludeSimpleHostnames: CFString](/documentation/cfnetwork/kcfnetworkproxiesexcludesimplehostnames)
- [let kCFNetworkProxiesFTPEnable: CFString](/documentation/cfnetwork/kcfnetworkproxiesftpenable)
- [let kCFNetworkProxiesFTPPassive: CFString](/documentation/cfnetwork/kcfnetworkproxiesftppassive)
- [let kCFNetworkProxiesFTPPort: CFString](/documentation/cfnetwork/kcfnetworkproxiesftpport)
- [let kCFNetworkProxiesFTPProxy: CFString](/documentation/cfnetwork/kcfnetworkproxiesftpproxy)
- [let kCFNetworkProxiesGopherEnable: CFString](/documentation/cfnetwork/kcfnetworkproxiesgopherenable)
- [let kCFNetworkProxiesGopherPort: CFString](/documentation/cfnetwork/kcfnetworkproxiesgopherport)
- [let kCFNetworkProxiesGopherProxy: CFString](/documentation/cfnetwork/kcfnetworkproxiesgopherproxy)
- [let kCFNetworkProxiesHTTPEnable: CFString](/documentation/cfnetwork/kcfnetworkproxieshttpenable)
- [let kCFNetworkProxiesHTTPPort: CFString](/documentation/cfnetwork/kcfnetworkproxieshttpport)
- [let kCFNetworkProxiesHTTPProxy: CFString](/documentation/cfnetwork/kcfnetworkproxieshttpproxy)
- [let kCFNetworkProxiesHTTPSEnable: CFString](/documentation/cfnetwork/kcfnetworkproxieshttpsenable)
- [let kCFNetworkProxiesHTTPSPort: CFString](/documentation/cfnetwork/kcfnetworkproxieshttpsport)
- [let kCFNetworkProxiesHTTPSProxy: CFString](/documentation/cfnetwork/kcfnetworkproxieshttpsproxy)
- [let kCFNetworkProxiesRTSPEnable: CFString](/documentation/cfnetwork/kcfnetworkproxiesrtspenable)
- [let kCFNetworkProxiesRTSPPort: CFString](/documentation/cfnetwork/kcfnetworkproxiesrtspport)
- [let kCFNetworkProxiesRTSPProxy: CFString](/documentation/cfnetwork/kcfnetworkproxiesrtspproxy)
- [let kCFNetworkProxiesSOCKSEnable: CFString](/documentation/cfnetwork/kcfnetworkproxiessocksenable)
- [let kCFNetworkProxiesSOCKSPort: CFString](/documentation/cfnetwork/kcfnetworkproxiessocksport)
- [let kCFNetworkProxiesSOCKSProxy: CFString](/documentation/cfnetwork/kcfnetworkproxiessocksproxy)
- [let kCFNetworkProxiesProxyAutoConfigEnable: CFString](/documentation/cfnetwork/kcfnetworkproxiesproxyautoconfigenable)
- [let kCFNetworkProxiesProxyAutoConfigJavaScript: CFString](/documentation/cfnetwork/kcfnetworkproxiesproxyautoconfigjavascript)
- [let kCFNetworkProxiesProxyAutoConfigURLString: CFString](/documentation/cfnetwork/kcfnetworkproxiesproxyautoconfigurlstring)
- [let kCFNetworkProxiesProxyAutoDiscoveryEnable: CFString](/documentation/cfnetwork/kcfnetworkproxiesproxyautodiscoveryenable)

## HTTP Authentication

- [CFHTTPAuthentication](/documentation/cfnetwork/cfhttpauthentication)
- [func CFHTTPAuthenticationAppliesToRequest(CFHTTPAuthentication, CFHTTPMessage) -> Bool](/documentation/cfnetwork/cfhttpauthenticationappliestorequest(_:_:))
- [func CFHTTPAuthenticationCopyDomains(CFHTTPAuthentication) -> Unmanaged<CFArray>](/documentation/cfnetwork/cfhttpauthenticationcopydomains(_:))
- [func CFHTTPAuthenticationCopyMethod(CFHTTPAuthentication) -> Unmanaged<CFString>](/documentation/cfnetwork/cfhttpauthenticationcopymethod(_:))
- [func CFHTTPAuthenticationCopyRealm(CFHTTPAuthentication) -> Unmanaged<CFString>](/documentation/cfnetwork/cfhttpauthenticationcopyrealm(_:))
- [func CFHTTPAuthenticationCreateFromResponse(CFAllocator?, CFHTTPMessage) -> Unmanaged<CFHTTPAuthentication>](/documentation/cfnetwork/cfhttpauthenticationcreatefromresponse(_:_:))
- [func CFHTTPAuthenticationGetTypeID() -> CFTypeID](/documentation/cfnetwork/cfhttpauthenticationgettypeid())
- [func CFHTTPAuthenticationIsValid(CFHTTPAuthentication, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfhttpauthenticationisvalid(_:_:))
- [func CFHTTPAuthenticationRequiresAccountDomain(CFHTTPAuthentication) -> Bool](/documentation/cfnetwork/cfhttpauthenticationrequiresaccountdomain(_:))
- [func CFHTTPAuthenticationRequiresOrderedRequests(CFHTTPAuthentication) -> Bool](/documentation/cfnetwork/cfhttpauthenticationrequiresorderedrequests(_:))
- [func CFHTTPAuthenticationRequiresUserNameAndPassword(CFHTTPAuthentication) -> Bool](/documentation/cfnetwork/cfhttpauthenticationrequiresusernameandpassword(_:))
- [let kCFHTTPAuthenticationAccountDomain: CFString](/documentation/cfnetwork/kcfhttpauthenticationaccountdomain)
- [let kCFHTTPAuthenticationPassword: CFString](/documentation/cfnetwork/kcfhttpauthenticationpassword)
- [let kCFHTTPAuthenticationSchemeBasic: CFString](/documentation/cfnetwork/kcfhttpauthenticationschemebasic)
- [let kCFHTTPAuthenticationSchemeDigest: CFString](/documentation/cfnetwork/kcfhttpauthenticationschemedigest)
- [let kCFHTTPAuthenticationSchemeKerberos: CFString](/documentation/cfnetwork/kcfhttpauthenticationschemekerberos)
- [let kCFHTTPAuthenticationSchemeNTLM: CFString](/documentation/cfnetwork/kcfhttpauthenticationschementlm)
- [let kCFHTTPAuthenticationSchemeNegotiate: CFString](/documentation/cfnetwork/kcfhttpauthenticationschemenegotiate)
- [let kCFHTTPAuthenticationSchemeNegotiate2: CFString](/documentation/cfnetwork/kcfhttpauthenticationschemenegotiate2)
- [let kCFHTTPAuthenticationSchemeXMobileMeAuthToken: CFString](/documentation/cfnetwork/kcfhttpauthenticationschemexmobilemeauthtoken)
- [let kCFHTTPAuthenticationUsername: CFString](/documentation/cfnetwork/kcfhttpauthenticationusername)

## HTTP Messages

- [CFHTTPMessage](/documentation/cfnetwork/cfhttpmessage)
- [func CFHTTPMessageAddAuthentication(CFHTTPMessage, CFHTTPMessage?, CFString, CFString, CFString?, Bool) -> Bool](/documentation/cfnetwork/cfhttpmessageaddauthentication(_:_:_:_:_:_:))
- [func CFHTTPMessageAppendBytes(CFHTTPMessage, UnsafePointer<UInt8>, CFIndex) -> Bool](/documentation/cfnetwork/cfhttpmessageappendbytes(_:_:_:))
- [func CFHTTPMessageApplyCredentialDictionary(CFHTTPMessage, CFHTTPAuthentication, CFDictionary, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfhttpmessageapplycredentialdictionary(_:_:_:_:))
- [func CFHTTPMessageApplyCredentials(CFHTTPMessage, CFHTTPAuthentication, CFString?, CFString?, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfhttpmessageapplycredentials(_:_:_:_:_:))
- [func CFHTTPMessageCopyAllHeaderFields(CFHTTPMessage) -> Unmanaged<CFDictionary>?](/documentation/cfnetwork/cfhttpmessagecopyallheaderfields(_:))
- [func CFHTTPMessageCopyBody(CFHTTPMessage) -> Unmanaged<CFData>?](/documentation/cfnetwork/cfhttpmessagecopybody(_:))
- [func CFHTTPMessageCopyHeaderFieldValue(CFHTTPMessage, CFString) -> Unmanaged<CFString>?](/documentation/cfnetwork/cfhttpmessagecopyheaderfieldvalue(_:_:))
- [func CFHTTPMessageCopyRequestMethod(CFHTTPMessage) -> Unmanaged<CFString>?](/documentation/cfnetwork/cfhttpmessagecopyrequestmethod(_:))
- [func CFHTTPMessageCopyRequestURL(CFHTTPMessage) -> Unmanaged<CFURL>?](/documentation/cfnetwork/cfhttpmessagecopyrequesturl(_:))
- [func CFHTTPMessageCopyResponseStatusLine(CFHTTPMessage) -> Unmanaged<CFString>?](/documentation/cfnetwork/cfhttpmessagecopyresponsestatusline(_:))
- [func CFHTTPMessageCopySerializedMessage(CFHTTPMessage) -> Unmanaged<CFData>?](/documentation/cfnetwork/cfhttpmessagecopyserializedmessage(_:))
- [func CFHTTPMessageCopyVersion(CFHTTPMessage) -> Unmanaged<CFString>](/documentation/cfnetwork/cfhttpmessagecopyversion(_:))
- [func CFHTTPMessageCreateCopy(CFAllocator?, CFHTTPMessage) -> Unmanaged<CFHTTPMessage>](/documentation/cfnetwork/cfhttpmessagecreatecopy(_:_:))
- [func CFHTTPMessageCreateEmpty(CFAllocator?, Bool) -> Unmanaged<CFHTTPMessage>](/documentation/cfnetwork/cfhttpmessagecreateempty(_:_:))
- [func CFHTTPMessageCreateRequest(CFAllocator?, CFString, CFURL, CFString) -> Unmanaged<CFHTTPMessage>](/documentation/cfnetwork/cfhttpmessagecreaterequest(_:_:_:_:))
- [func CFHTTPMessageCreateResponse(CFAllocator?, CFIndex, CFString?, CFString) -> Unmanaged<CFHTTPMessage>](/documentation/cfnetwork/cfhttpmessagecreateresponse(_:_:_:_:))
- [func CFHTTPMessageGetResponseStatusCode(CFHTTPMessage) -> CFIndex](/documentation/cfnetwork/cfhttpmessagegetresponsestatuscode(_:))
- [func CFHTTPMessageGetTypeID() -> CFTypeID](/documentation/cfnetwork/cfhttpmessagegettypeid())
- [func CFHTTPMessageIsHeaderComplete(CFHTTPMessage) -> Bool](/documentation/cfnetwork/cfhttpmessageisheadercomplete(_:))
- [func CFHTTPMessageIsRequest(CFHTTPMessage) -> Bool](/documentation/cfnetwork/cfhttpmessageisrequest(_:))
- [func CFHTTPMessageSetBody(CFHTTPMessage, CFData)](/documentation/cfnetwork/cfhttpmessagesetbody(_:_:))
- [func CFHTTPMessageSetHeaderFieldValue(CFHTTPMessage, CFString, CFString?)](/documentation/cfnetwork/cfhttpmessagesetheaderfieldvalue(_:_:_:))
- [let kCFHTTPVersion1_0: CFString](/documentation/cfnetwork/kcfhttpversion1_0)
- [let kCFHTTPVersion1_1: CFString](/documentation/cfnetwork/kcfhttpversion1_1)
- [let kCFHTTPVersion2_0: CFString](/documentation/cfnetwork/kcfhttpversion2_0)

## FTP

- [func CFFTPCreateParsedResourceListing(CFAllocator?, UnsafePointer<UInt8>, CFIndex, UnsafeMutablePointer<Unmanaged<CFDictionary>?>?) -> CFIndex](/documentation/cfnetwork/cfftpcreateparsedresourcelisting(_:_:_:_:))
- [let kCFFTPResourceGroup: CFString](/documentation/cfnetwork/kcfftpresourcegroup)
- [let kCFFTPResourceLink: CFString](/documentation/cfnetwork/kcfftpresourcelink)
- [let kCFFTPResourceModDate: CFString](/documentation/cfnetwork/kcfftpresourcemoddate)
- [let kCFFTPResourceMode: CFString](/documentation/cfnetwork/kcfftpresourcemode)
- [let kCFFTPResourceName: CFString](/documentation/cfnetwork/kcfftpresourcename)
- [let kCFFTPResourceOwner: CFString](/documentation/cfnetwork/kcfftpresourceowner)
- [let kCFFTPResourceSize: CFString](/documentation/cfnetwork/kcfftpresourcesize)
- [let kCFFTPResourceType: CFString](/documentation/cfnetwork/kcfftpresourcetype)

## Network Diagnostics

- [CFNetDiagnostic](/documentation/cfnetwork/cfnetdiagnostic)
- [CFNetDiagnosticStatusValues](/documentation/cfnetwork/cfnetdiagnosticstatusvalues)

### Constants

- [case noErr](/documentation/cfnetwork/cfnetdiagnosticstatusvalues/noerr)
- [case err](/documentation/cfnetwork/cfnetdiagnosticstatusvalues/err)
- [case connectionUp](/documentation/cfnetwork/cfnetdiagnosticstatusvalues/connectionup)
- [case connectionIndeterminate](/documentation/cfnetwork/cfnetdiagnosticstatusvalues/connectionindeterminate)
- [case connectionDown](/documentation/cfnetwork/cfnetdiagnosticstatusvalues/connectiondown)

### Initializers

- [init?(rawValue: Int32)](/documentation/cfnetwork/cfnetdiagnosticstatusvalues/init(rawvalue:))
- [func CFNetDiagnosticCopyNetworkStatusPassively(CFNetDiagnostic, UnsafeMutablePointer<Unmanaged<CFString>?>?) -> CFNetDiagnosticStatus](/documentation/cfnetwork/cfnetdiagnosticcopynetworkstatuspassively(_:_:))
- [func CFNetDiagnosticCreateWithStreams(CFAllocator?, CFReadStream?, CFWriteStream?) -> Unmanaged<CFNetDiagnostic>](/documentation/cfnetwork/cfnetdiagnosticcreatewithstreams(_:_:_:))
- [func CFNetDiagnosticCreateWithURL(CFAllocator, CFURL) -> Unmanaged<CFNetDiagnostic>](/documentation/cfnetwork/cfnetdiagnosticcreatewithurl(_:_:))
- [func CFNetDiagnosticDiagnoseProblemInteractively(CFNetDiagnostic) -> CFNetDiagnosticStatus](/documentation/cfnetwork/cfnetdiagnosticdiagnoseprobleminteractively(_:))
- [func CFNetDiagnosticSetName(CFNetDiagnostic, CFString)](/documentation/cfnetwork/cfnetdiagnosticsetname(_:_:))

## Network Services

- [CFNetService](/documentation/cfnetwork/cfnetservice)
- [CFNetServiceBrowser](/documentation/cfnetwork/cfnetservicebrowser)
- [CFNetServiceBrowserFlags](/documentation/cfnetwork/cfnetservicebrowserflags)

### Constants

- [init(rawValue: CFOptionFlags)](/documentation/cfnetwork/cfnetservicebrowserflags/init(rawvalue:))

### Type Properties

- [static var isDefault: CFNetServiceBrowserFlags](/documentation/cfnetwork/cfnetservicebrowserflags/isdefault)
- [static var isDomain: CFNetServiceBrowserFlags](/documentation/cfnetwork/cfnetservicebrowserflags/isdomain)
- [static var isRegistrationDomain: CFNetServiceBrowserFlags](/documentation/cfnetwork/cfnetservicebrowserflags/isregistrationdomain)
- [static var moreComing: CFNetServiceBrowserFlags](/documentation/cfnetwork/cfnetservicebrowserflags/morecoming)
- [static var remove: CFNetServiceBrowserFlags](/documentation/cfnetwork/cfnetservicebrowserflags/remove)
- [static var isRegistrationDomain: CFNetServiceBrowserFlags](/documentation/cfnetwork/cfnetservicebrowserflags/isregistrationdomain)
- [CFNetServiceMonitor](/documentation/cfnetwork/cfnetservicemonitor)
- [CFNetServiceMonitorType](/documentation/cfnetwork/cfnetservicemonitortype)

### Constants

- [case TXT](/documentation/cfnetwork/cfnetservicemonitortype/txt)

### Initializers

- [init?(rawValue: Int32)](/documentation/cfnetwork/cfnetservicemonitortype/init(rawvalue:))
- [CFNetServiceClientContext](/documentation/cfnetwork/cfnetserviceclientcontext)

### Initializers

- [init()](/documentation/cfnetwork/cfnetserviceclientcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer?, retain: CFAllocatorRetainCallBack?, release: CFAllocatorReleaseCallBack?, copyDescription: CFAllocatorCopyDescriptionCallBack?)](/documentation/cfnetwork/cfnetserviceclientcontext/init(version:info:retain:release:copydescription:))

### Instance Properties

- [var copyDescription: CFAllocatorCopyDescriptionCallBack?](/documentation/cfnetwork/cfnetserviceclientcontext/copydescription)
- [var info: UnsafeMutableRawPointer?](/documentation/cfnetwork/cfnetserviceclientcontext/info)
- [var release: CFAllocatorReleaseCallBack?](/documentation/cfnetwork/cfnetserviceclientcontext/release)
- [var retain: CFAllocatorRetainCallBack?](/documentation/cfnetwork/cfnetserviceclientcontext/retain)
- [var version: CFIndex](/documentation/cfnetwork/cfnetserviceclientcontext/version)
- [CFNetServiceRegisterFlags](/documentation/cfnetwork/cfnetserviceregisterflags)

### Creating Register Flags

- [init(rawValue: CFOptionFlags)](/documentation/cfnetwork/cfnetserviceregisterflags/init(rawvalue:))

### Constants

- [static var noAutoRename: CFNetServiceRegisterFlags](/documentation/cfnetwork/cfnetserviceregisterflags/noautorename)
- [CFNetServicesError](/documentation/cfnetwork/cfnetserviceserror)

### Constants

- [case unknown](/documentation/cfnetwork/cfnetserviceserror/unknown)
- [case collision](/documentation/cfnetwork/cfnetserviceserror/collision)
- [case notFound](/documentation/cfnetwork/cfnetserviceserror/notfound)
- [case inProgress](/documentation/cfnetwork/cfnetserviceserror/inprogress)
- [case badArgument](/documentation/cfnetwork/cfnetserviceserror/badargument)
- [case cancel](/documentation/cfnetwork/cfnetserviceserror/cancel)
- [case invalid](/documentation/cfnetwork/cfnetserviceserror/invalid)
- [case timeout](/documentation/cfnetwork/cfnetserviceserror/timeout)

### Enumeration Cases

- [case missingRequiredConfiguration](/documentation/cfnetwork/cfnetserviceserror/missingrequiredconfiguration)

### Initializers

- [init?(rawValue: Int32)](/documentation/cfnetwork/cfnetserviceserror/init(rawvalue:))
- [func CFNetServiceBrowserInvalidate(CFNetServiceBrowser)](/documentation/cfnetwork/cfnetservicebrowserinvalidate(_:))
- [func CFNetServiceBrowserScheduleWithRunLoop(CFNetServiceBrowser, CFRunLoop, CFString)](/documentation/cfnetwork/cfnetservicebrowserschedulewithrunloop(_:_:_:))
- [func CFNetServiceBrowserCreate(CFAllocator?, CFNetServiceBrowserClientCallBack, UnsafeMutablePointer<CFNetServiceClientContext>) -> Unmanaged<CFNetServiceBrowser>](/documentation/cfnetwork/cfnetservicebrowsercreate(_:_:_:))
- [func CFNetServiceBrowserGetTypeID() -> CFTypeID](/documentation/cfnetwork/cfnetservicebrowsergettypeid())
- [func CFNetServiceBrowserSearchForDomains(CFNetServiceBrowser, Bool, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfnetservicebrowsersearchfordomains(_:_:_:))
- [func CFNetServiceBrowserSearchForServices(CFNetServiceBrowser, CFString, CFString, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfnetservicebrowsersearchforservices(_:_:_:_:))
- [func CFNetServiceBrowserStopSearch(CFNetServiceBrowser, UnsafeMutablePointer<CFStreamError>?)](/documentation/cfnetwork/cfnetservicebrowserstopsearch(_:_:))
- [func CFNetServiceBrowserUnscheduleFromRunLoop(CFNetServiceBrowser, CFRunLoop, CFString)](/documentation/cfnetwork/cfnetservicebrowserunschedulefromrunloop(_:_:_:))
- [func CFNetServiceCancel(CFNetService)](/documentation/cfnetwork/cfnetservicecancel(_:))
- [func CFNetServiceCreate(CFAllocator?, CFString, CFString, CFString, Int32) -> Unmanaged<CFNetService>](/documentation/cfnetwork/cfnetservicecreate(_:_:_:_:_:))
- [func CFNetServiceCreateCopy(CFAllocator?, CFNetService) -> Unmanaged<CFNetService>](/documentation/cfnetwork/cfnetservicecreatecopy(_:_:))
- [func CFNetServiceCreateDictionaryWithTXTData(CFAllocator?, CFData) -> Unmanaged<CFDictionary>?](/documentation/cfnetwork/cfnetservicecreatedictionarywithtxtdata(_:_:))
- [func CFNetServiceCreateTXTDataWithDictionary(CFAllocator?, CFDictionary) -> Unmanaged<CFData>?](/documentation/cfnetwork/cfnetservicecreatetxtdatawithdictionary(_:_:))
- [func CFNetServiceGetAddressing(CFNetService) -> Unmanaged<CFArray>?](/documentation/cfnetwork/cfnetservicegetaddressing(_:))
- [func CFNetServiceGetDomain(CFNetService) -> Unmanaged<CFString>](/documentation/cfnetwork/cfnetservicegetdomain(_:))
- [func CFNetServiceGetName(CFNetService) -> Unmanaged<CFString>](/documentation/cfnetwork/cfnetservicegetname(_:))
- [func CFNetServiceGetPortNumber(CFNetService) -> Int32](/documentation/cfnetwork/cfnetservicegetportnumber(_:))
- [func CFNetServiceGetTXTData(CFNetService) -> Unmanaged<CFData>?](/documentation/cfnetwork/cfnetservicegettxtdata(_:))
- [func CFNetServiceGetTargetHost(CFNetService) -> Unmanaged<CFString>?](/documentation/cfnetwork/cfnetservicegettargethost(_:))
- [func CFNetServiceGetType(CFNetService) -> Unmanaged<CFString>](/documentation/cfnetwork/cfnetservicegettype(_:))
- [func CFNetServiceGetTypeID() -> CFTypeID](/documentation/cfnetwork/cfnetservicegettypeid())
- [func CFNetServiceMonitorCreate(CFAllocator?, CFNetService, CFNetServiceMonitorClientCallBack, UnsafeMutablePointer<CFNetServiceClientContext>) -> Unmanaged<CFNetServiceMonitor>](/documentation/cfnetwork/cfnetservicemonitorcreate(_:_:_:_:))
- [func CFNetServiceMonitorGetTypeID() -> CFTypeID](/documentation/cfnetwork/cfnetservicemonitorgettypeid())
- [func CFNetServiceMonitorInvalidate(CFNetServiceMonitor)](/documentation/cfnetwork/cfnetservicemonitorinvalidate(_:))
- [func CFNetServiceMonitorScheduleWithRunLoop(CFNetServiceMonitor, CFRunLoop, CFString)](/documentation/cfnetwork/cfnetservicemonitorschedulewithrunloop(_:_:_:))
- [func CFNetServiceMonitorStart(CFNetServiceMonitor, CFNetServiceMonitorType, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfnetservicemonitorstart(_:_:_:))
- [func CFNetServiceMonitorStop(CFNetServiceMonitor, UnsafeMutablePointer<CFStreamError>?)](/documentation/cfnetwork/cfnetservicemonitorstop(_:_:))
- [func CFNetServiceMonitorUnscheduleFromRunLoop(CFNetServiceMonitor, CFRunLoop, CFString)](/documentation/cfnetwork/cfnetservicemonitorunschedulefromrunloop(_:_:_:))
- [func CFNetServiceRegisterWithOptions(CFNetService, CFOptionFlags, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfnetserviceregisterwithoptions(_:_:_:))
- [func CFNetServiceResolveWithTimeout(CFNetService, CFTimeInterval, UnsafeMutablePointer<CFStreamError>?) -> Bool](/documentation/cfnetwork/cfnetserviceresolvewithtimeout(_:_:_:))
- [func CFNetServiceSetClient(CFNetService, CFNetServiceClientCallBack?, UnsafeMutablePointer<CFNetServiceClientContext>?) -> Bool](/documentation/cfnetwork/cfnetservicesetclient(_:_:_:))
- [func CFNetServiceSetTXTData(CFNetService, CFData) -> Bool](/documentation/cfnetwork/cfnetservicesettxtdata(_:_:))
- [func CFNetServiceUnscheduleFromRunLoop(CFNetService, CFRunLoop, CFString)](/documentation/cfnetwork/cfnetserviceunschedulefromrunloop(_:_:_:))
- [func CFNetServiceScheduleWithRunLoop(CFNetService, CFRunLoop, CFString)](/documentation/cfnetwork/cfnetserviceschedulewithrunloop(_:_:_:))

## Streams

- [func CFReadStreamCreateForHTTPRequest(CFAllocator?, CFHTTPMessage) -> Unmanaged<CFReadStream>](/documentation/cfnetwork/cfreadstreamcreateforhttprequest(_:_:))
- [func CFReadStreamCreateForStreamedHTTPRequest(CFAllocator?, CFHTTPMessage, CFReadStream) -> Unmanaged<CFReadStream>](/documentation/cfnetwork/cfreadstreamcreateforstreamedhttprequest(_:_:_:))
- [let kCFStreamPropertyHTTPAttemptPersistentConnection: CFString](/documentation/cfnetwork/kcfstreampropertyhttpattemptpersistentconnection)
- [let kCFStreamPropertyHTTPFinalRequest: CFString](/documentation/cfnetwork/kcfstreampropertyhttpfinalrequest)
- [let kCFStreamPropertyHTTPFinalURL: CFString](/documentation/cfnetwork/kcfstreampropertyhttpfinalurl)
- [let kCFStreamPropertyHTTPProxy: CFString](/documentation/cfnetwork/kcfstreampropertyhttpproxy)
- [let kCFStreamPropertyHTTPProxyHost: CFString](/documentation/cfnetwork/kcfstreampropertyhttpproxyhost)
- [let kCFStreamPropertyHTTPProxyPort: CFString](/documentation/cfnetwork/kcfstreampropertyhttpproxyport)
- [let kCFStreamPropertyHTTPRequestBytesWrittenCount: CFString](/documentation/cfnetwork/kcfstreampropertyhttprequestbyteswrittencount)
- [let kCFStreamPropertyHTTPResponseHeader: CFString](/documentation/cfnetwork/kcfstreampropertyhttpresponseheader)
- [let kCFStreamPropertyHTTPSProxyHost: CFString](/documentation/cfnetwork/kcfstreampropertyhttpsproxyhost)
- [let kCFStreamPropertyHTTPSProxyPort: CFString](/documentation/cfnetwork/kcfstreampropertyhttpsproxyport)
- [let kCFStreamPropertyHTTPShouldAutoredirect: CFString](/documentation/cfnetwork/kcfstreampropertyhttpshouldautoredirect)
- [func CFWriteStreamCreateWithFTPURL(CFAllocator?, CFURL) -> Unmanaged<CFWriteStream>](/documentation/cfnetwork/cfwritestreamcreatewithftpurl(_:_:))
- [func CFReadStreamCreateWithFTPURL(CFAllocator?, CFURL) -> Unmanaged<CFReadStream>](/documentation/cfnetwork/cfreadstreamcreatewithftpurl(_:_:))
- [let kCFStreamPropertyFTPAttemptPersistentConnection: CFString](/documentation/cfnetwork/kcfstreampropertyftpattemptpersistentconnection)
- [let kCFStreamPropertyFTPFetchResourceInfo: CFString](/documentation/cfnetwork/kcfstreampropertyftpfetchresourceinfo)
- [let kCFStreamPropertyFTPFileTransferOffset: CFString](/documentation/cfnetwork/kcfstreampropertyftpfiletransferoffset)
- [let kCFStreamPropertyFTPPassword: CFString](/documentation/cfnetwork/kcfstreampropertyftppassword)
- [let kCFStreamPropertyFTPProxy: CFString](/documentation/cfnetwork/kcfstreampropertyftpproxy)
- [let kCFStreamPropertyFTPProxyHost: CFString](/documentation/cfnetwork/kcfstreampropertyftpproxyhost)
- [let kCFStreamPropertyFTPProxyPassword: CFString](/documentation/cfnetwork/kcfstreampropertyftpproxypassword)
- [let kCFStreamPropertyFTPProxyPort: CFString](/documentation/cfnetwork/kcfstreampropertyftpproxyport)
- [let kCFStreamPropertyFTPProxyUser: CFString](/documentation/cfnetwork/kcfstreampropertyftpproxyuser)
- [let kCFStreamPropertyFTPResourceSize: CFString](/documentation/cfnetwork/kcfstreampropertyftpresourcesize)
- [let kCFStreamPropertyFTPUsePassiveMode: CFString](/documentation/cfnetwork/kcfstreampropertyftpusepassivemode)
- [let kCFStreamPropertyFTPUserName: CFString](/documentation/cfnetwork/kcfstreampropertyftpusername)
- [func CFSocketStreamSOCKSGetError(UnsafePointer<CFStreamError>) -> Int32](/documentation/cfnetwork/cfsocketstreamsocksgeterror(_:))
- [func CFSocketStreamSOCKSGetErrorSubdomain(UnsafePointer<CFStreamError>) -> Int32](/documentation/cfnetwork/cfsocketstreamsocksgeterrorsubdomain(_:))
- [func CFStreamCreatePairWithSocketToCFHost(CFAllocator?, CFHost, Int32, UnsafeMutablePointer<Unmanaged<CFReadStream>?>?, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>?)](/documentation/cfnetwork/cfstreamcreatepairwithsockettocfhost(_:_:_:_:_:))
- [func CFStreamCreatePairWithSocketToNetService(CFAllocator?, CFNetService, UnsafeMutablePointer<Unmanaged<CFReadStream>?>?, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>?)](/documentation/cfnetwork/cfstreamcreatepairwithsockettonetservice(_:_:_:_:))
- [let kCFStreamNetworkServiceType: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetype)
- [let kCFStreamNetworkServiceTypeBackground: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypebackground)
- [let kCFStreamNetworkServiceTypeCallSignaling: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypecallsignaling)
- [let kCFStreamNetworkServiceTypeVideo: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypevideo)
- [let kCFStreamNetworkServiceTypeVoIP: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypevoip)
- [let kCFStreamNetworkServiceTypeVoice: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypevoice)
- [let kCFStreamErrorDomainFTP: Int32](/documentation/cfnetwork/kcfstreamerrordomainftp)
- [let kCFStreamErrorDomainHTTP: Int32](/documentation/cfnetwork/kcfstreamerrordomainhttp)
- [let kCFStreamErrorDomainMach: Int32](/documentation/cfnetwork/kcfstreamerrordomainmach)
- [let kCFStreamErrorDomainNetDB: Int32](/documentation/cfnetwork/kcfstreamerrordomainnetdb)
- [let kCFStreamErrorDomainNetServices: Int32](/documentation/cfnetwork/kcfstreamerrordomainnetservices)
- [let kCFStreamErrorDomainSOCKS: Int32](/documentation/corefoundation/kcfstreamerrordomainsocks)
- [let kCFStreamErrorDomainSSL: Int32](/documentation/corefoundation/kcfstreamerrordomainssl)
- [let kCFStreamErrorDomainSystemConfiguration: Int32](/documentation/cfnetwork/kcfstreamerrordomainsystemconfiguration)
- [let kCFStreamErrorDomainWinSock: CFIndex](/documentation/cfnetwork/kcfstreamerrordomainwinsock)
- [let kCFStreamPropertyConnectionIsCellular: CFString](/documentation/cfnetwork/kcfstreampropertyconnectioniscellular)
- [let kCFStreamPropertyNoCellular: CFString](/documentation/cfnetwork/kcfstreampropertynocellular)
- [let kCFStreamPropertyProxyLocalBypass: CFString](/documentation/cfnetwork/kcfstreampropertyproxylocalbypass)
- [let kCFStreamPropertySOCKSPassword: CFString](/documentation/corefoundation/kcfstreampropertysockspassword)
- [let kCFStreamPropertySOCKSProxy: CFString](/documentation/corefoundation/kcfstreampropertysocksproxy)
- [let kCFStreamPropertySOCKSProxyHost: CFString](/documentation/corefoundation/kcfstreampropertysocksproxyhost)
- [let kCFStreamPropertySOCKSProxyPort: CFString](/documentation/corefoundation/kcfstreampropertysocksproxyport)
- [let kCFStreamPropertySOCKSUser: CFString](/documentation/corefoundation/kcfstreampropertysocksuser)
- [let kCFStreamPropertySOCKSVersion: CFString](/documentation/corefoundation/kcfstreampropertysocksversion)
- [let kCFStreamPropertySSLContext: CFString](/documentation/cfnetwork/kcfstreampropertysslcontext)
- [let kCFStreamPropertySSLPeerCertificates: CFString](/documentation/cfnetwork/kcfstreampropertysslpeercertificates)
- [let kCFStreamPropertySSLPeerTrust: CFString](/documentation/cfnetwork/kcfstreampropertysslpeertrust)
- [let kCFStreamPropertySSLSettings: CFString](/documentation/cfnetwork/kcfstreampropertysslsettings)
- [let kCFStreamPropertyShouldCloseNativeSocket: CFString](/documentation/corefoundation/kcfstreampropertyshouldclosenativesocket)
- [let kCFStreamPropertySocketExtendedBackgroundIdleMode: CFString](/documentation/cfnetwork/kcfstreampropertysocketextendedbackgroundidlemode)
- [let kCFStreamPropertySocketRemoteHost: CFString](/documentation/cfnetwork/kcfstreampropertysocketremotehost)
- [let kCFStreamPropertySocketRemoteNetService: CFString](/documentation/cfnetwork/kcfstreampropertysocketremotenetservice)
- [let kCFStreamPropertySocketSecurityLevel: CFString](/documentation/corefoundation/kcfstreampropertysocketsecuritylevel)
- [let kCFStreamSSLAllowsAnyRoot: CFString](/documentation/cfnetwork/kcfstreamsslallowsanyroot)
- [let kCFStreamSSLAllowsExpiredCertificates: CFString](/documentation/cfnetwork/kcfstreamsslallowsexpiredcertificates)
- [let kCFStreamSSLAllowsExpiredRoots: CFString](/documentation/cfnetwork/kcfstreamsslallowsexpiredroots)
- [let kCFStreamSSLCertificates: CFString](/documentation/cfnetwork/kcfstreamsslcertificates)
- [let kCFStreamSSLIsServer: CFString](/documentation/cfnetwork/kcfstreamsslisserver)
- [let kCFStreamSSLLevel: CFString](/documentation/cfnetwork/kcfstreamssllevel)
- [let kCFStreamSSLPeerName: CFString](/documentation/cfnetwork/kcfstreamsslpeername)
- [let kCFStreamSSLValidatesCertificateChain: CFString](/documentation/cfnetwork/kcfstreamsslvalidatescertificatechain)
- [let kCFStreamSocketSOCKSVersion4: CFString](/documentation/corefoundation/kcfstreamsocketsocksversion4)
- [let kCFStreamSocketSOCKSVersion5: CFString](/documentation/corefoundation/kcfstreamsocketsocksversion5)
- [let kCFStreamSocketSecurityLevelNegotiatedSSL: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelnegotiatedssl)
- [let kCFStreamSocketSecurityLevelNone: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelnone)
- [let kCFStreamSocketSecurityLevelSSLv2: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelsslv2)
- [let kCFStreamSocketSecurityLevelSSLv3: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelsslv3)
- [let kCFStreamSocketSecurityLevelTLSv1: CFString](/documentation/corefoundation/kcfstreamsocketsecurityleveltlsv1)
- [CFStreamErrorHTTP](/documentation/cfnetwork/cfstreamerrorhttp)

### Constants

- [case parseFailure](/documentation/cfnetwork/cfstreamerrorhttp/parsefailure)
- [case redirectionLoop](/documentation/cfnetwork/cfstreamerrorhttp/redirectionloop)
- [case badURL](/documentation/cfnetwork/cfstreamerrorhttp/badurl)

### Initializers

- [init?(rawValue: Int32)](/documentation/cfnetwork/cfstreamerrorhttp/init(rawvalue:))
- [CFStreamErrorHTTPAuthentication](/documentation/cfnetwork/cfstreamerrorhttpauthentication)

### Constants

- [case typeUnsupported](/documentation/cfnetwork/cfstreamerrorhttpauthentication/typeunsupported)
- [case badUserName](/documentation/cfnetwork/cfstreamerrorhttpauthentication/badusername)
- [case badPassword](/documentation/cfnetwork/cfstreamerrorhttpauthentication/badpassword)

### Initializers

- [init?(rawValue: Int32)](/documentation/cfnetwork/cfstreamerrorhttpauthentication/init(rawvalue:))
- [Secure Sockets (SOCKS) Errors](/documentation/cfnetwork/1518266-secure-sockets-socks-errors)

### Constants

- [var kCFStreamErrorSOCKS4IdConflict: Int](/documentation/cfnetwork/kcfstreamerrorsocks4idconflict)
- [var kCFStreamErrorSOCKS4IdentdFailed: Int](/documentation/cfnetwork/kcfstreamerrorsocks4identdfailed)
- [var kCFStreamErrorSOCKS4RequestFailed: Int](/documentation/cfnetwork/kcfstreamerrorsocks4requestfailed)
- [var kCFStreamErrorSOCKS4SubDomainResponse: Int](/documentation/cfnetwork/kcfstreamerrorsocks4subdomainresponse)
- [var kCFStreamErrorSOCKS5SubDomainMethod: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainmethod)
- [var kCFStreamErrorSOCKS5SubDomainResponse: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainresponse)
- [var kCFStreamErrorSOCKS5SubDomainUserPass: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainuserpass)
- [var kCFStreamErrorSOCKSSubDomainNone: Int](/documentation/cfnetwork/kcfstreamerrorsockssubdomainnone)
- [var kCFStreamErrorSOCKSSubDomainVersionCode: Int](/documentation/cfnetwork/kcfstreamerrorsockssubdomainversioncode)
- [var kSOCKS5NoAcceptableMethod: Int](/documentation/cfnetwork/ksocks5noacceptablemethod)
- [var kCFStreamErrorSOCKS5BadResponseAddr: Int](/documentation/cfnetwork/kcfstreamerrorsocks5badresponseaddr)
- [var kCFStreamErrorSOCKS5BadState: Int](/documentation/cfnetwork/kcfstreamerrorsocks5badstate)
- [var kCFStreamErrorSOCKSUnknownClientVersion: Int](/documentation/cfnetwork/kcfstreamerrorsocksunknownclientversion)

## Reference

- [CFNetwork Data Types](/documentation/cfnetwork/cfnetwork-data-types)

### Data Types

- [CFHostClientCallBack](/documentation/cfnetwork/cfhostclientcallback)
- [CFNetServiceBrowserClientCallBack](/documentation/cfnetwork/cfnetservicebrowserclientcallback)
- [CFNetServiceClientCallBack](/documentation/cfnetwork/cfnetserviceclientcallback)
- [CFNetServiceMonitorClientCallBack](/documentation/cfnetwork/cfnetservicemonitorclientcallback)
- [CFNetDiagnosticStatus](/documentation/cfnetwork/cfnetdiagnosticstatus)
- [CFNetwork Enumerations](/documentation/cfnetwork/cfnetwork-enumerations)

### Enumerations

- [Anonymous](/documentation/cfnetwork/1518287-anonymous)

#### Constants

- [var kCFStreamErrorSOCKS4SubDomainResponse: Int](/documentation/cfnetwork/kcfstreamerrorsocks4subdomainresponse)
- [var kCFStreamErrorSOCKS5SubDomainMethod: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainmethod)
- [var kCFStreamErrorSOCKS5SubDomainResponse: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainresponse)
- [var kCFStreamErrorSOCKS5SubDomainUserPass: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainuserpass)
- [var kCFStreamErrorSOCKSSubDomainNone: Int](/documentation/cfnetwork/kcfstreamerrorsockssubdomainnone)
- [var kCFStreamErrorSOCKSSubDomainVersionCode: Int](/documentation/cfnetwork/kcfstreamerrorsockssubdomainversioncode)
- [Anonymous](/documentation/cfnetwork/1518276-anonymous)

#### Constants

- [var kSOCKS5NoAcceptableMethod: Int](/documentation/cfnetwork/ksocks5noacceptablemethod)
- [Anonymous](/documentation/cfnetwork/1518284-anonymous)

#### Constants

- [var kCFStreamErrorSOCKS4IdConflict: Int](/documentation/cfnetwork/kcfstreamerrorsocks4idconflict)
- [var kCFStreamErrorSOCKS4IdentdFailed: Int](/documentation/cfnetwork/kcfstreamerrorsocks4identdfailed)
- [var kCFStreamErrorSOCKS4RequestFailed: Int](/documentation/cfnetwork/kcfstreamerrorsocks4requestfailed)
- [CFNetwork Constants](/documentation/cfnetwork/cfnetwork-constants)

### Constants

- [let kCFHTTPVersion3_0: CFString](/documentation/cfnetwork/kcfhttpversion3_0)
- [let kCFStreamNetworkServiceTypeAVStreaming: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypeavstreaming)
- [let kCFStreamNetworkServiceTypeResponsiveAV: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetyperesponsiveav)
- [let kCFStreamNetworkServiceTypeResponsiveData: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetyperesponsivedata)
- [let kCFStreamPropertyAllowConstrainedNetworkAccess: CFString](/documentation/cfnetwork/kcfstreampropertyallowconstrainednetworkaccess)
- [let kCFStreamPropertyAllowExpensiveNetworkAccess: CFString](/documentation/cfnetwork/kcfstreampropertyallowexpensivenetworkaccess)
- [let kCFStreamPropertyConnectionIsExpensive: CFString](/documentation/cfnetwork/kcfstreampropertyconnectionisexpensive)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
