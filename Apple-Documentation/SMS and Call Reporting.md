# IdentityLookup Documentation

Source: https://sosumi.ai/documentation/identitylookup

---
title: SMS and Call Reporting
source: https://developer.apple.com/documentation/identitylookup
timestamp: 2026-02-13T19:57:45.197Z
---

## Message filtering

- [SMS and MMS Message Filtering](/documentation/identitylookup/sms-and-mms-message-filtering)

### First Steps

- [Creating a Message Filter App Extension](/documentation/identitylookup/creating-a-message-filter-app-extension)

### App Extension

- [ILMessageFilterExtensionContext](/documentation/identitylookup/ilmessagefilterextensioncontext)

#### Deferring a Request to the Network

- [func deferQueryRequestToNetwork(completion: (ILNetworkResponse?, (any Error)?) -> Void)](/documentation/identitylookup/ilmessagefilterextensioncontext/deferqueryrequesttonetwork(completion:))
- [ILMessageFilterExtension](/documentation/identitylookup/ilmessagefilterextension)

### Queries

- [ILMessageFilterQueryRequest](/documentation/identitylookup/ilmessagefilterqueryrequest)

#### Getting Information About a Message

- [var sender: String?](/documentation/identitylookup/ilmessagefilterqueryrequest/sender)
- [var messageBody: String?](/documentation/identitylookup/ilmessagefilterqueryrequest/messagebody)
- [var receiverISOCountryCode: String?](/documentation/identitylookup/ilmessagefilterqueryrequest/receiverisocountrycode)
- [ILMessageFilterQueryHandling](/documentation/identitylookup/ilmessagefilterqueryhandling)

#### Handling a Query Request

- [func handle(ILMessageFilterQueryRequest, context: ILMessageFilterExtensionContext, completion: (ILMessageFilterQueryResponse) -> Void)](/documentation/identitylookup/ilmessagefilterqueryhandling/handle(_:context:completion:))

### Responses

- [ILMessageFilterQueryResponse](/documentation/identitylookup/ilmessagefilterqueryresponse)

#### Specifying the Action

- [var action: ILMessageFilterAction](/documentation/identitylookup/ilmessagefilterqueryresponse/action)
- [var subAction: ILMessageFilterSubAction](/documentation/identitylookup/ilmessagefilterqueryresponse/subaction)
- [ILNetworkResponse](/documentation/identitylookup/ilnetworkresponse)

#### Getting the Response

- [var urlResponse: HTTPURLResponse](/documentation/identitylookup/ilnetworkresponse/urlresponse)

#### Getting Data from the Response

- [var data: Data](/documentation/identitylookup/ilnetworkresponse/data)
- [ILMessageFilterAction](/documentation/identitylookup/ilmessagefilteraction)

#### Filter Actions

- [case none](/documentation/identitylookup/ilmessagefilteraction/none)
- [case allow](/documentation/identitylookup/ilmessagefilteraction/allow)
- [case junk](/documentation/identitylookup/ilmessagefilteraction/junk)
- [case promotion](/documentation/identitylookup/ilmessagefilteraction/promotion)
- [case transaction](/documentation/identitylookup/ilmessagefilteraction/transaction)

#### Deprecations

- [static var filter: ILMessageFilterAction](/documentation/identitylookup/ilmessagefilteraction/filter)

#### Initializers

- [init?(rawValue: Int)](/documentation/identitylookup/ilmessagefilteraction/init(rawvalue:))

### Errors

- [ILMessageFilterError](/documentation/identitylookup/ilmessagefiltererror-swift.struct)

#### Enumerations

- [ILMessageFilterError.Code](/documentation/identitylookup/ilmessagefiltererror-swift.struct/code)

##### Error Codes

- [case system](/documentation/identitylookup/ilmessagefiltererror-swift.struct/code/system)
- [case invalidNetworkURL](/documentation/identitylookup/ilmessagefiltererror-swift.struct/code/invalidnetworkurl)
- [case networkURLUnauthorized](/documentation/identitylookup/ilmessagefiltererror-swift.struct/code/networkurlunauthorized)
- [case networkRequestFailed](/documentation/identitylookup/ilmessagefiltererror-swift.struct/code/networkrequestfailed)
- [case redundantNetworkDeferral](/documentation/identitylookup/ilmessagefiltererror-swift.struct/code/redundantnetworkdeferral)

##### Initializers

- [init?(rawValue: Int)](/documentation/identitylookup/ilmessagefiltererror-swift.struct/code/init(rawvalue:))

#### Error Codes

- [static var invalidNetworkURL: ILMessageFilterError.Code](/documentation/identitylookup/ilmessagefiltererror-swift.struct/invalidnetworkurl)
- [static var networkRequestFailed: ILMessageFilterError.Code](/documentation/identitylookup/ilmessagefiltererror-swift.struct/networkrequestfailed)
- [static var networkURLUnauthorized: ILMessageFilterError.Code](/documentation/identitylookup/ilmessagefiltererror-swift.struct/networkurlunauthorized)
- [static var redundantNetworkDeferral: ILMessageFilterError.Code](/documentation/identitylookup/ilmessagefiltererror-swift.struct/redundantnetworkdeferral)
- [static var system: ILMessageFilterError.Code](/documentation/identitylookup/ilmessagefiltererror-swift.struct/system)

#### Error Domain

- [let ILMessageFilterErrorDomain: String](/documentation/identitylookup/ilmessagefiltererrordomain)

#### Type Properties

- [static var errorDomain: String](/documentation/identitylookup/ilmessagefiltererror-swift.struct/errordomain)
- [let ILMessageFilterErrorDomain: String](/documentation/identitylookup/ilmessagefiltererrordomain)

## Spam reporting

- [SMS and Call Spam Reporting](/documentation/identitylookup/sms-and-call-spam-reporting)

### App Extension

- [ILClassificationUIExtensionViewController](/documentation/identitylookupui/ilclassificationuiextensionviewcontroller)

### Communications

- [ILCommunication](/documentation/identitylookup/ilcommunication)

#### Accessing Data

- [var sender: String?](/documentation/identitylookup/ilcommunication/sender)
- [var dateReceived: Date](/documentation/identitylookup/ilcommunication/datereceived)
- [ILMessageCommunication](/documentation/identitylookup/ilmessagecommunication)

#### Accessing Data

- [var messageBody: String?](/documentation/identitylookup/ilmessagecommunication/messagebody)
- [ILCallCommunication](/documentation/identitylookup/ilcallcommunication)

### Requests

- [ILClassificationRequest](/documentation/identitylookup/ilclassificationrequest)
- [ILMessageClassificationRequest](/documentation/identitylookup/ilmessageclassificationrequest)

#### Accessing Messages

- [var messageCommunications: [ILMessageCommunication]](/documentation/identitylookup/ilmessageclassificationrequest/messagecommunications)
- [ILCallClassificationRequest](/documentation/identitylookup/ilcallclassificationrequest)

#### Accessing Calls

- [var callCommunications: [ILCallCommunication]](/documentation/identitylookup/ilcallclassificationrequest/callcommunications)

### Responses

- [ILClassificationResponse](/documentation/identitylookup/ilclassificationresponse)

#### Creating Responses

- [init(action: ILClassificationAction)](/documentation/identitylookup/ilclassificationresponse/init(action:))

#### Accessing Data

- [var action: ILClassificationAction](/documentation/identitylookup/ilclassificationresponse/action)
- [var userInfo: [String : Any]?](/documentation/identitylookup/ilclassificationresponse/userinfo)
- [var userString: String?](/documentation/identitylookup/ilclassificationresponse/userstring)
- [ILClassificationAction](/documentation/identitylookup/ilclassificationaction)

#### Classifications

- [case none](/documentation/identitylookup/ilclassificationaction/none)
- [case reportJunk](/documentation/identitylookup/ilclassificationaction/reportjunk)
- [case reportJunkAndBlockSender](/documentation/identitylookup/ilclassificationaction/reportjunkandblocksender)
- [case reportNotJunk](/documentation/identitylookup/ilclassificationaction/reportnotjunk)

#### Initializers

- [init?(rawValue: Int)](/documentation/identitylookup/ilclassificationaction/init(rawvalue:))

### Queries

- [ILMessageFilterCapabilitiesQueryRequest](/documentation/identitylookup/ilmessagefiltercapabilitiesqueryrequest)
- [ILMessageFilterCapabilitiesQueryHandling](/documentation/identitylookup/ilmessagefiltercapabilitiesqueryhandling)

#### Handling a Capabilities Query Request

- [func handle(ILMessageFilterCapabilitiesQueryRequest, context: ILMessageFilterExtensionContext, completion: (ILMessageFilterCapabilitiesQueryResponse) -> Void)](/documentation/identitylookup/ilmessagefiltercapabilitiesqueryhandling/handle(_:context:completion:))

### Responses

- [ILMessageFilterCapabilitiesQueryResponse](/documentation/identitylookup/ilmessagefiltercapabilitiesqueryresponse)

#### Setting the Subactions

- [var promotionalSubActions: [ILMessageFilterSubAction]](/documentation/identitylookup/ilmessagefiltercapabilitiesqueryresponse/promotionalsubactions-98kzj)
- [var transactionalSubActions: [ILMessageFilterSubAction]](/documentation/identitylookup/ilmessagefiltercapabilitiesqueryresponse/transactionalsubactions-4bfqz)
- [ILMessageFilterSubAction](/documentation/identitylookup/ilmessagefiltersubaction)

#### Transactional Subactions

- [case none](/documentation/identitylookup/ilmessagefiltersubaction/none)
- [case transactionalOthers](/documentation/identitylookup/ilmessagefiltersubaction/transactionalothers)
- [case transactionalFinance](/documentation/identitylookup/ilmessagefiltersubaction/transactionalfinance)
- [case transactionalOrders](/documentation/identitylookup/ilmessagefiltersubaction/transactionalorders)
- [case transactionalReminders](/documentation/identitylookup/ilmessagefiltersubaction/transactionalreminders)
- [case transactionalHealth](/documentation/identitylookup/ilmessagefiltersubaction/transactionalhealth)
- [case transactionalWeather](/documentation/identitylookup/ilmessagefiltersubaction/transactionalweather)
- [case transactionalCarrier](/documentation/identitylookup/ilmessagefiltersubaction/transactionalcarrier)
- [case transactionalRewards](/documentation/identitylookup/ilmessagefiltersubaction/transactionalrewards)
- [case transactionalPublicServices](/documentation/identitylookup/ilmessagefiltersubaction/transactionalpublicservices)

#### Promotional Subactions

- [case promotionalOthers](/documentation/identitylookup/ilmessagefiltersubaction/promotionalothers)
- [case promotionalOffers](/documentation/identitylookup/ilmessagefiltersubaction/promotionaloffers)
- [case promotionalCoupons](/documentation/identitylookup/ilmessagefiltersubaction/promotionalcoupons)

#### Initializers

- [init?(rawValue: Int)](/documentation/identitylookup/ilmessagefiltersubaction/init(rawvalue:))

## Live Caller ID Lookup

- [Understanding how Live Caller ID Lookup preserves privacy](/documentation/identitylookup/understanding-how-live-caller-id-lookup-preserves-privacy)
- [Formatting data for blocking and identity information](/documentation/identitylookup/formatting-data-for-blocking-and-identity-information)
- [Setting up the HTTP endpoints for Live Caller ID Lookup](/documentation/identitylookup/setting-up-the-http-endpoints-for-live-caller-id-lookup)
- [Getting up-to-date calling and blocking information for your app](/documentation/identitylookup/getting-up-to-date-calling-and-blocking-information-for-your-app)
- [LiveCallerIDLookupProtocol](/documentation/identitylookup/livecalleridlookupprotocol)

### Setting extension context

- [var context: LiveCallerIDLookupExtensionContext](/documentation/identitylookup/livecalleridlookupprotocol/context)
- [LiveCallerIDLookupExtensionConfiguration](/documentation/identitylookup/livecalleridlookupextensionconfiguration)
- [LiveCallerIDLookupExtensionContext](/documentation/identitylookup/livecalleridlookupextensioncontext)

### Initializing the app extension context

- [init(serviceURL: URL, tokenIssuerURL: URL, userTierToken: Data)](/documentation/identitylookup/livecalleridlookupextensioncontext/init(serviceurl:tokenissuerurl:usertiertoken:))

### Configuring the system

- [let serviceURL: URL](/documentation/identitylookup/livecalleridlookupextensioncontext/serviceurl)
- [let tokenIssuerURL: URL](/documentation/identitylookup/livecalleridlookupextensioncontext/tokenissuerurl)
- [let userTierToken: Data](/documentation/identitylookup/livecalleridlookupextensioncontext/usertiertoken)
- [CallLookupExtensionStatus](/documentation/identitylookup/calllookupextensionstatus)

### Checking the state of the app extension

- [case disabled](/documentation/identitylookup/calllookupextensionstatus/disabled)
- [case enabled](/documentation/identitylookup/calllookupextensionstatus/enabled)
- [LiveCallerIDLookupManager](/documentation/identitylookup/livecalleridlookupmanager)

### Checking status and fetching data

- [let extensionPointName: String](/documentation/identitylookup/extensionpointname)
- [func openSettings() async throws](/documentation/identitylookup/livecalleridlookupmanager/opensettings())
- [func refreshPIRParameters(forExtensionWithIdentifier: String) async throws](/documentation/identitylookup/livecalleridlookupmanager/refreshpirparameters(forextensionwithidentifier:))
- [func reset(forExtensionWithIdentifier: String) async throws](/documentation/identitylookup/livecalleridlookupmanager/reset(forextensionwithidentifier:))
- [func status(forExtensionWithIdentifier: String) -> CallLookupExtensionStatus](/documentation/identitylookup/livecalleridlookupmanager/status(forextensionwithidentifier:))

### Sharing the instance

- [static let shared: LiveCallerIDLookupManager](/documentation/identitylookup/livecalleridlookupmanager/shared)

### Instance Methods

- [func refreshExtensionContext(forExtensionWithIdentifier: String) async throws](/documentation/identitylookup/livecalleridlookupmanager/refreshextensioncontext(forextensionwithidentifier:))

## Macros

- [Macros](/documentation/identitylookup/macros)

## Type Aliases

- [BlockingInfoCoreDataPropertiesSet](/documentation/identitylookup/blockinginfocoredatapropertiesset)
- [IdentityInfoCoreDataPropertiesSet](/documentation/identitylookup/identityinfocoredatapropertiesset)
- [LiveLookupDBExtensionCoreDataPropertiesSet](/documentation/identitylookup/livelookupdbextensioncoredatapropertiesset)
- [LiveLookupStoreCoreDataFrameworkManagedObject](/documentation/identitylookup/livelookupstorecoredataframeworkmanagedobject)
- [LiveLookupStoreFoundationFrameworkSet](/documentation/identitylookup/livelookupstorefoundationframeworkset)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
