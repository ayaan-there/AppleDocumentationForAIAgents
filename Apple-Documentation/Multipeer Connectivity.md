# Multipeer Connectivity Documentation

Source: https://sosumi.ai/documentation/multipeerconnectivity

---
title: Multipeer Connectivity
source: https://developer.apple.com/documentation/multipeerconnectivity
timestamp: 2026-02-13T18:59:53.484Z
---

## Classes

- [MCAdvertiserAssistant](/documentation/multipeerconnectivity/mcadvertiserassistant)

### Initializing and Configuring

- [init(serviceType: String, discoveryInfo: [String : String]?, session: MCSession)](/documentation/multipeerconnectivity/mcadvertiserassistant/init(servicetype:discoveryinfo:session:))
- [var session: MCSession](/documentation/multipeerconnectivity/mcadvertiserassistant/session)
- [var delegate: (any MCAdvertiserAssistantDelegate)?](/documentation/multipeerconnectivity/mcadvertiserassistant/delegate)
- [var discoveryInfo: [String : String]?](/documentation/multipeerconnectivity/mcadvertiserassistant/discoveryinfo)
- [var serviceType: String](/documentation/multipeerconnectivity/mcadvertiserassistant/servicetype)

### Starting and Stopping the Assistant

- [func start()](/documentation/multipeerconnectivity/mcadvertiserassistant/start())
- [func stop()](/documentation/multipeerconnectivity/mcadvertiserassistant/stop())
- [MCBrowserViewController](/documentation/multipeerconnectivity/mcbrowserviewcontroller)

### Initializing a Browser View Controller

- [convenience init(serviceType: String, session: MCSession)](/documentation/multipeerconnectivity/mcbrowserviewcontroller/init(servicetype:session:))
- [init(browser: MCNearbyServiceBrowser, session: MCSession)](/documentation/multipeerconnectivity/mcbrowserviewcontroller/init(browser:session:))
- [var delegate: (any MCBrowserViewControllerDelegate)?](/documentation/multipeerconnectivity/mcbrowserviewcontroller/delegate)
- [var browser: MCNearbyServiceBrowser?](/documentation/multipeerconnectivity/mcbrowserviewcontroller/browser)
- [var session: MCSession](/documentation/multipeerconnectivity/mcbrowserviewcontroller/session)

### Getting and Setting the Maximum and Minimum Number of Peers

- [var maximumNumberOfPeers: Int](/documentation/multipeerconnectivity/mcbrowserviewcontroller/maximumnumberofpeers)
- [var minimumNumberOfPeers: Int](/documentation/multipeerconnectivity/mcbrowserviewcontroller/minimumnumberofpeers)
- [MCNearbyServiceAdvertiser](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser)

### Configuring and Initialization

- [init(peer: MCPeerID, discoveryInfo: [String : String]?, serviceType: String)](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser/init(peer:discoveryinfo:servicetype:))
- [var delegate: (any MCNearbyServiceAdvertiserDelegate)?](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser/delegate)
- [var discoveryInfo: [String : String]?](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser/discoveryinfo)
- [var myPeerID: MCPeerID](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser/mypeerid)
- [var serviceType: String](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser/servicetype)

### Starting and Stopping Advertisement

- [func startAdvertisingPeer()](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser/startadvertisingpeer())
- [func stopAdvertisingPeer()](/documentation/multipeerconnectivity/mcnearbyserviceadvertiser/stopadvertisingpeer())
- [MCNearbyServiceBrowser](/documentation/multipeerconnectivity/mcnearbyservicebrowser)

### Initializing the Browser

- [init(peer: MCPeerID, serviceType: String)](/documentation/multipeerconnectivity/mcnearbyservicebrowser/init(peer:servicetype:))
- [var delegate: (any MCNearbyServiceBrowserDelegate)?](/documentation/multipeerconnectivity/mcnearbyservicebrowser/delegate)
- [var myPeerID: MCPeerID](/documentation/multipeerconnectivity/mcnearbyservicebrowser/mypeerid)
- [var serviceType: String](/documentation/multipeerconnectivity/mcnearbyservicebrowser/servicetype)

### Browsing for Peers

- [func startBrowsingForPeers()](/documentation/multipeerconnectivity/mcnearbyservicebrowser/startbrowsingforpeers())
- [func stopBrowsingForPeers()](/documentation/multipeerconnectivity/mcnearbyservicebrowser/stopbrowsingforpeers())

### Inviting Peers

- [func invitePeer(MCPeerID, to: MCSession, withContext: Data?, timeout: TimeInterval)](/documentation/multipeerconnectivity/mcnearbyservicebrowser/invitepeer(_:to:withcontext:timeout:))
- [MCPeerID](/documentation/multipeerconnectivity/mcpeerid)

### Peer Methods

- [init(displayName: String)](/documentation/multipeerconnectivity/mcpeerid/init(displayname:))
- [var displayName: String](/documentation/multipeerconnectivity/mcpeerid/displayname)
- [MCSession](/documentation/multipeerconnectivity/mcsession)

### Creating a Session

- [convenience init(peer: MCPeerID)](/documentation/multipeerconnectivity/mcsession/init(peer:))
- [init(peer: MCPeerID, securityIdentity: [Any]?, encryptionPreference: MCEncryptionPreference)](/documentation/multipeerconnectivity/mcsession/init(peer:securityidentity:encryptionpreference:))
- [var delegate: (any MCSessionDelegate)?](/documentation/multipeerconnectivity/mcsession/delegate)
- [var encryptionPreference: MCEncryptionPreference](/documentation/multipeerconnectivity/mcsession/encryptionpreference)
- [var myPeerID: MCPeerID](/documentation/multipeerconnectivity/mcsession/mypeerid)
- [var securityIdentity: [Any]?](/documentation/multipeerconnectivity/mcsession/securityidentity)

### Managing Peers Manually

- [func connectPeer(MCPeerID, withNearbyConnectionData: Data)](/documentation/multipeerconnectivity/mcsession/connectpeer(_:withnearbyconnectiondata:))
- [func cancelConnectPeer(MCPeerID)](/documentation/multipeerconnectivity/mcsession/cancelconnectpeer(_:))
- [var connectedPeers: [MCPeerID]](/documentation/multipeerconnectivity/mcsession/connectedpeers)
- [func nearbyConnectionData(forPeer: MCPeerID, withCompletionHandler: (Data?, (any Error)?) -> Void)](/documentation/multipeerconnectivity/mcsession/nearbyconnectiondata(forpeer:withcompletionhandler:))

### Sending Data and Resources

- [func send(Data, toPeers: [MCPeerID], with: MCSessionSendDataMode) throws](/documentation/multipeerconnectivity/mcsession/send(_:topeers:with:))
- [func sendResource(at: URL, withName: String, toPeer: MCPeerID, withCompletionHandler: (((any Error)?) -> Void)?) -> Progress?](/documentation/multipeerconnectivity/mcsession/sendresource(at:withname:topeer:withcompletionhandler:))
- [func startStream(withName: String, toPeer: MCPeerID) throws -> OutputStream](/documentation/multipeerconnectivity/mcsession/startstream(withname:topeer:))

### Leaving a Session

- [func disconnect()](/documentation/multipeerconnectivity/mcsession/disconnect())

### Constants

- [MCSessionSendDataMode](/documentation/multipeerconnectivity/mcsessionsenddatamode)

#### Constants

- [case reliable](/documentation/multipeerconnectivity/mcsessionsenddatamode/reliable)
- [case unreliable](/documentation/multipeerconnectivity/mcsessionsenddatamode/unreliable)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcsessionsenddatamode/init(rawvalue:))
- [MCSessionState](/documentation/multipeerconnectivity/mcsessionstate)

#### Constants

- [case notConnected](/documentation/multipeerconnectivity/mcsessionstate/notconnected)
- [case connecting](/documentation/multipeerconnectivity/mcsessionstate/connecting)
- [case connected](/documentation/multipeerconnectivity/mcsessionstate/connected)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcsessionstate/init(rawvalue:))
- [MCEncryptionPreference](/documentation/multipeerconnectivity/mcencryptionpreference)

#### Constants

- [case optional](/documentation/multipeerconnectivity/mcencryptionpreference/optional)
- [case required](/documentation/multipeerconnectivity/mcencryptionpreference/required)
- [case none](/documentation/multipeerconnectivity/mcencryptionpreference/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcencryptionpreference/init(rawvalue:))
- [MCError.Code](/documentation/multipeerconnectivity/mcerror/code)

#### Constants

- [case unknown](/documentation/multipeerconnectivity/mcerror/code/unknown)
- [case notConnected](/documentation/multipeerconnectivity/mcerror/code/notconnected)
- [case invalidParameter](/documentation/multipeerconnectivity/mcerror/code/invalidparameter)
- [case unsupported](/documentation/multipeerconnectivity/mcerror/code/unsupported)
- [case timedOut](/documentation/multipeerconnectivity/mcerror/code/timedout)
- [case cancelled](/documentation/multipeerconnectivity/mcerror/code/cancelled)
- [case unavailable](/documentation/multipeerconnectivity/mcerror/code/unavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcerror/code/init(rawvalue:))
- [Multipeer Connectivity Error Domain](/documentation/multipeerconnectivity/multipeer_connectivity_error_domain)

#### Constants

- [let MCErrorDomain: String](/documentation/multipeerconnectivity/mcerrordomain)
- [Minimum and Maximum Supported Peers](/documentation/multipeerconnectivity/minimum_and_maximum_supported_peers)

#### Constants

- [let kMCSessionMaximumNumberOfPeers: Int](/documentation/multipeerconnectivity/kmcsessionmaximumnumberofpeers)
- [let kMCSessionMinimumNumberOfPeers: Int](/documentation/multipeerconnectivity/kmcsessionminimumnumberofpeers)

## Protocols

- [MCAdvertiserAssistantDelegate](/documentation/multipeerconnectivity/mcadvertiserassistantdelegate)

### Advertiser Assistant Delegate Methods

- [func advertiserAssistantWillPresentInvitation(MCAdvertiserAssistant)](/documentation/multipeerconnectivity/mcadvertiserassistantdelegate/advertiserassistantwillpresentinvitation(_:))
- [func advertiserAssistantDidDismissInvitation(MCAdvertiserAssistant)](/documentation/multipeerconnectivity/mcadvertiserassistantdelegate/advertiserassistantdiddismissinvitation(_:))
- [MCBrowserViewControllerDelegate](/documentation/multipeerconnectivity/mcbrowserviewcontrollerdelegate)

### Peer Notifications

- [func browserViewController(MCBrowserViewController, shouldPresentNearbyPeer: MCPeerID, withDiscoveryInfo: [String : String]?) -> Bool](/documentation/multipeerconnectivity/mcbrowserviewcontrollerdelegate/browserviewcontroller(_:shouldpresentnearbypeer:withdiscoveryinfo:))

### User Action Notifications

- [func browserViewControllerDidFinish(MCBrowserViewController)](/documentation/multipeerconnectivity/mcbrowserviewcontrollerdelegate/browserviewcontrollerdidfinish(_:))
- [func browserViewControllerWasCancelled(MCBrowserViewController)](/documentation/multipeerconnectivity/mcbrowserviewcontrollerdelegate/browserviewcontrollerwascancelled(_:))
- [MCNearbyServiceAdvertiserDelegate](/documentation/multipeerconnectivity/mcnearbyserviceadvertiserdelegate)

### Error Handling Delegate Methods

- [func advertiser(MCNearbyServiceAdvertiser, didNotStartAdvertisingPeer: any Error)](/documentation/multipeerconnectivity/mcnearbyserviceadvertiserdelegate/advertiser(_:didnotstartadvertisingpeer:))

### Invitation Handling Delegate Methods

- [func advertiser(MCNearbyServiceAdvertiser, didReceiveInvitationFromPeer: MCPeerID, withContext: Data?, invitationHandler: (Bool, MCSession?) -> Void)](/documentation/multipeerconnectivity/mcnearbyserviceadvertiserdelegate/advertiser(_:didreceiveinvitationfrompeer:withcontext:invitationhandler:))
- [MCNearbyServiceBrowserDelegate](/documentation/multipeerconnectivity/mcnearbyservicebrowserdelegate)

### Error Handling Delegate Methods

- [func browser(MCNearbyServiceBrowser, didNotStartBrowsingForPeers: any Error)](/documentation/multipeerconnectivity/mcnearbyservicebrowserdelegate/browser(_:didnotstartbrowsingforpeers:))

### Peer Discovery Delegate Methods

- [func browser(MCNearbyServiceBrowser, foundPeer: MCPeerID, withDiscoveryInfo: [String : String]?)](/documentation/multipeerconnectivity/mcnearbyservicebrowserdelegate/browser(_:foundpeer:withdiscoveryinfo:))
- [func browser(MCNearbyServiceBrowser, lostPeer: MCPeerID)](/documentation/multipeerconnectivity/mcnearbyservicebrowserdelegate/browser(_:lostpeer:))
- [MCSessionDelegate](/documentation/multipeerconnectivity/mcsessiondelegate)

### MCSession Delegate Methods

- [func session(MCSession, didReceive: Data, fromPeer: MCPeerID)](/documentation/multipeerconnectivity/mcsessiondelegate/session(_:didreceive:frompeer:))
- [func session(MCSession, didStartReceivingResourceWithName: String, fromPeer: MCPeerID, with: Progress)](/documentation/multipeerconnectivity/mcsessiondelegate/session(_:didstartreceivingresourcewithname:frompeer:with:))
- [func session(MCSession, didFinishReceivingResourceWithName: String, fromPeer: MCPeerID, at: URL?, withError: (any Error)?)](/documentation/multipeerconnectivity/mcsessiondelegate/session(_:didfinishreceivingresourcewithname:frompeer:at:witherror:))
- [func session(MCSession, didReceive: InputStream, withName: String, fromPeer: MCPeerID)](/documentation/multipeerconnectivity/mcsessiondelegate/session(_:didreceive:withname:frompeer:))
- [func session(MCSession, peer: MCPeerID, didChange: MCSessionState)](/documentation/multipeerconnectivity/mcsessiondelegate/session(_:peer:didchange:))
- [func session(MCSession, didReceiveCertificate: [Any]?, fromPeer: MCPeerID, certificateHandler: (Bool) -> Void)](/documentation/multipeerconnectivity/mcsessiondelegate/session(_:didreceivecertificate:frompeer:certificatehandler:))

## Structures

- [MCError](/documentation/multipeerconnectivity/mcerror)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/multipeerconnectivity/mcerror/3726664-init)

### Instance Properties

- [MCError.Code](/documentation/multipeerconnectivity/mcerror/code)

#### Constants

- [case unknown](/documentation/multipeerconnectivity/mcerror/code/unknown)
- [case notConnected](/documentation/multipeerconnectivity/mcerror/code/notconnected)
- [case invalidParameter](/documentation/multipeerconnectivity/mcerror/code/invalidparameter)
- [case unsupported](/documentation/multipeerconnectivity/mcerror/code/unsupported)
- [case timedOut](/documentation/multipeerconnectivity/mcerror/code/timedout)
- [case cancelled](/documentation/multipeerconnectivity/mcerror/code/cancelled)
- [case unavailable](/documentation/multipeerconnectivity/mcerror/code/unavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcerror/code/init(rawvalue:))
- [var errorCode: Int](/documentation/foundation/customnserror/errorcode-2opgi)
- [var errorUserInfo: [String : Any]](/documentation/foundation/customnserror/erroruserinfo-1aas5)
- [var hashValue: Int](/documentation/multipeerconnectivity/mcerror/3726663-hashvalue)
- [var userInfo: [String : Any]](/documentation/multipeerconnectivity/mcerror/userinfo)

### Type Properties

- [static var cancelled: MCError.Code](/documentation/multipeerconnectivity/mcerror/cancelled)
- [static var errorDomain: String](/documentation/multipeerconnectivity/mcerror/errordomain)
- [static var invalidParameter: MCError.Code](/documentation/multipeerconnectivity/mcerror/invalidparameter)
- [static var notConnected: MCError.Code](/documentation/multipeerconnectivity/mcerror/notconnected)
- [static var timedOut: MCError.Code](/documentation/multipeerconnectivity/mcerror/timedout)
- [static var unavailable: MCError.Code](/documentation/multipeerconnectivity/mcerror/unavailable)
- [static var unknown: MCError.Code](/documentation/multipeerconnectivity/mcerror/unknown)
- [static var unsupported: MCError.Code](/documentation/multipeerconnectivity/mcerror/unsupported)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/multipeerconnectivity/mcerror/3726662-hash)

### Operator Functions

- [static func == (MCError, MCError) -> Bool](/documentation/multipeerconnectivity/mcerror/3726660)

### Enumerations

- [MCError.Code](/documentation/multipeerconnectivity/mcerror/code)

#### Constants

- [case unknown](/documentation/multipeerconnectivity/mcerror/code/unknown)
- [case notConnected](/documentation/multipeerconnectivity/mcerror/code/notconnected)
- [case invalidParameter](/documentation/multipeerconnectivity/mcerror/code/invalidparameter)
- [case unsupported](/documentation/multipeerconnectivity/mcerror/code/unsupported)
- [case timedOut](/documentation/multipeerconnectivity/mcerror/code/timedout)
- [case cancelled](/documentation/multipeerconnectivity/mcerror/code/cancelled)
- [case unavailable](/documentation/multipeerconnectivity/mcerror/code/unavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcerror/code/init(rawvalue:))

## Reference

- [MultipeerConnectivity Enumerations](/documentation/multipeerconnectivity/multipeerconnectivity_enumerations)

### Enumerations

- [MCEncryptionPreference](/documentation/multipeerconnectivity/mcencryptionpreference)

#### Constants

- [case optional](/documentation/multipeerconnectivity/mcencryptionpreference/optional)
- [case required](/documentation/multipeerconnectivity/mcencryptionpreference/required)
- [case none](/documentation/multipeerconnectivity/mcencryptionpreference/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcencryptionpreference/init(rawvalue:))
- [MCError.Code](/documentation/multipeerconnectivity/mcerror/code)

#### Constants

- [case unknown](/documentation/multipeerconnectivity/mcerror/code/unknown)
- [case notConnected](/documentation/multipeerconnectivity/mcerror/code/notconnected)
- [case invalidParameter](/documentation/multipeerconnectivity/mcerror/code/invalidparameter)
- [case unsupported](/documentation/multipeerconnectivity/mcerror/code/unsupported)
- [case timedOut](/documentation/multipeerconnectivity/mcerror/code/timedout)
- [case cancelled](/documentation/multipeerconnectivity/mcerror/code/cancelled)
- [case unavailable](/documentation/multipeerconnectivity/mcerror/code/unavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcerror/code/init(rawvalue:))
- [MCSessionSendDataMode](/documentation/multipeerconnectivity/mcsessionsenddatamode)

#### Constants

- [case reliable](/documentation/multipeerconnectivity/mcsessionsenddatamode/reliable)
- [case unreliable](/documentation/multipeerconnectivity/mcsessionsenddatamode/unreliable)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcsessionsenddatamode/init(rawvalue:))
- [MCSessionState](/documentation/multipeerconnectivity/mcsessionstate)

#### Constants

- [case notConnected](/documentation/multipeerconnectivity/mcsessionstate/notconnected)
- [case connecting](/documentation/multipeerconnectivity/mcsessionstate/connecting)
- [case connected](/documentation/multipeerconnectivity/mcsessionstate/connected)

#### Initializers

- [init?(rawValue: Int)](/documentation/multipeerconnectivity/mcsessionstate/init(rawvalue:))
- [MultipeerConnectivity Constants](/documentation/multipeerconnectivity/multipeerconnectivity_constants)

### Constants

- [let MCErrorDomain: String](/documentation/multipeerconnectivity/mcerrordomain)
- [let kMCSessionMaximumNumberOfPeers: Int](/documentation/multipeerconnectivity/kmcsessionmaximumnumberofpeers)
- [let kMCSessionMinimumNumberOfPeers: Int](/documentation/multipeerconnectivity/kmcsessionminimumnumberofpeers)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
