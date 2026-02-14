# Core Telephony Documentation

Source: https://sosumi.ai/documentation/coretelephony

---
title: Core Telephony
source: https://developer.apple.com/documentation/coretelephony
timestamp: 2026-02-13T18:55:43.874Z
---

## Service Information

- [CTTelephonyNetworkInfo](/documentation/coretelephony/cttelephonynetworkinfo)

### Getting Information About the Cellular Service Provider

- [var dataServiceIdentifier: String?](/documentation/coretelephony/cttelephonynetworkinfo/dataserviceidentifier)
- [var delegate: (any CTTelephonyNetworkInfoDelegate)?](/documentation/coretelephony/cttelephonynetworkinfo/delegate)
- [CTTelephonyNetworkInfoDelegate](/documentation/coretelephony/cttelephonynetworkinfodelegate)

#### Responding to Data Service Changes

- [func dataServiceIdentifierDidChange(String)](/documentation/coretelephony/cttelephonynetworkinfodelegate/dataserviceidentifierdidchange(_:))
- [var serviceCurrentRadioAccessTechnology: [String : String]?](/documentation/coretelephony/cttelephonynetworkinfo/servicecurrentradioaccesstechnology)
- [Radio Access Technology Constants](/documentation/coretelephony/radio-access-technology-constants)

#### Constants

- [let CTRadioAccessTechnologyGPRS: String](/documentation/coretelephony/ctradioaccesstechnologygprs)
- [let CTRadioAccessTechnologyEdge: String](/documentation/coretelephony/ctradioaccesstechnologyedge)
- [let CTRadioAccessTechnologyWCDMA: String](/documentation/coretelephony/ctradioaccesstechnologywcdma)
- [let CTRadioAccessTechnologyHSDPA: String](/documentation/coretelephony/ctradioaccesstechnologyhsdpa)
- [let CTRadioAccessTechnologyHSUPA: String](/documentation/coretelephony/ctradioaccesstechnologyhsupa)
- [let CTRadioAccessTechnologyCDMA1x: String](/documentation/coretelephony/ctradioaccesstechnologycdma1x)
- [let CTRadioAccessTechnologyCDMAEVDORev0: String](/documentation/coretelephony/ctradioaccesstechnologycdmaevdorev0)
- [let CTRadioAccessTechnologyCDMAEVDORevA: String](/documentation/coretelephony/ctradioaccesstechnologycdmaevdoreva)
- [let CTRadioAccessTechnologyCDMAEVDORevB: String](/documentation/coretelephony/ctradioaccesstechnologycdmaevdorevb)
- [let CTRadioAccessTechnologyeHRPD: String](/documentation/coretelephony/ctradioaccesstechnologyehrpd)
- [let CTRadioAccessTechnologyLTE: String](/documentation/coretelephony/ctradioaccesstechnologylte)
- [let CTRadioAccessTechnologyNRNSA: String](/documentation/coretelephony/ctradioaccesstechnologynrnsa)
- [let CTRadioAccessTechnologyNR: String](/documentation/coretelephony/ctradioaccesstechnologynr)

### Deprecated

- [var currentRadioAccessTechnology: String?](/documentation/coretelephony/cttelephonynetworkinfo/currentradioaccesstechnology)
- [var subscriberCellularProvider: CTCarrier?](/documentation/coretelephony/cttelephonynetworkinfo/subscribercellularprovider)
- [var subscriberCellularProviderDidUpdateNotifier: ((CTCarrier) -> Void)?](/documentation/coretelephony/cttelephonynetworkinfo/subscribercellularproviderdidupdatenotifier)
- [var serviceSubscriberCellularProviders: [String : CTCarrier]?](/documentation/coretelephony/cttelephonynetworkinfo/servicesubscribercellularproviders)
- [var serviceSubscriberCellularProvidersDidUpdateNotifier: ((String) -> Void)?](/documentation/coretelephony/cttelephonynetworkinfo/servicesubscribercellularprovidersdidupdatenotifier)
- [static let CTRadioAccessTechnologyDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/ctradioaccesstechnologydidchange)

## eSIM

- [CTCellularPlanProvisioning](/documentation/coretelephony/ctcellularplanprovisioning)

### Provisioning an eSIM

- [func supportsCellularPlan() -> Bool](/documentation/coretelephony/ctcellularplanprovisioning/supportscellularplan())
- [var supportsEmbeddedSIM: Bool](/documentation/coretelephony/ctcellularplanprovisioning/supportsembeddedsim)
- [func addPlan(request: CTCellularPlanProvisioningRequest, properties: CTCellularPlanProperties?, completionHandler: (CTCellularPlanProvisioningAddPlanResult) -> Void)](/documentation/coretelephony/ctcellularplanprovisioning/addplan(request:properties:completionhandler:))
- [func addPlan(with: CTCellularPlanProvisioningRequest, completionHandler: (CTCellularPlanProvisioningAddPlanResult) -> Void)](/documentation/coretelephony/ctcellularplanprovisioning/addplan(with:completionhandler:))
- [CTCellularPlanProvisioningAddPlanResult](/documentation/coretelephony/ctcellularplanprovisioningaddplanresult)

#### Results

- [case fail](/documentation/coretelephony/ctcellularplanprovisioningaddplanresult/fail)
- [case success](/documentation/coretelephony/ctcellularplanprovisioningaddplanresult/success)
- [case unknown](/documentation/coretelephony/ctcellularplanprovisioningaddplanresult/unknown)
- [case cancel](/documentation/coretelephony/ctcellularplanprovisioningaddplanresult/cancel)

#### Initializers

- [init?(rawValue: UInt)](/documentation/coretelephony/ctcellularplanprovisioningaddplanresult/init(rawvalue:))

### Updating eSIM information

- [func update(CTCellularPlanProperties, completionHandler: ((any Error)?) -> Void)](/documentation/coretelephony/ctcellularplanprovisioning/update(_:completionhandler:))
- [CTCellularPlanProvisioningRequest](/documentation/coretelephony/ctcellularplanprovisioningrequest)

### Specifying Request Properties

- [var address: String](/documentation/coretelephony/ctcellularplanprovisioningrequest/address)
- [var confirmationCode: String?](/documentation/coretelephony/ctcellularplanprovisioningrequest/confirmationcode)
- [var eid: String?](/documentation/coretelephony/ctcellularplanprovisioningrequest/eid)
- [var iccid: String?](/documentation/coretelephony/ctcellularplanprovisioningrequest/iccid)
- [var matchingID: String?](/documentation/coretelephony/ctcellularplanprovisioningrequest/matchingid)
- [var oid: String?](/documentation/coretelephony/ctcellularplanprovisioningrequest/oid)
- [CTCellularPlanProperties](/documentation/coretelephony/ctcellularplanproperties)

### Getting the eSIM properties

- [var associatedIccid: String?](/documentation/coretelephony/ctcellularplanproperties/associatediccid)
- [var simCapability: CTCellularPlanCapability](/documentation/coretelephony/ctcellularplanproperties/simcapability)
- [var supportedRegionCodes: [Locale.Region]](/documentation/coretelephony/ctcellularplanproperties/supportedregioncodes-yhu5)
- [CTCellularPlanCapability](/documentation/coretelephony/ctcellularplancapability)

### Defining cellular data plans

- [init?(rawValue: Int)](/documentation/coretelephony/ctcellularplancapability/init(rawvalue:))
- [case dataAndVoice](/documentation/coretelephony/ctcellularplancapability/dataandvoice)
- [case dataOnly](/documentation/coretelephony/ctcellularplancapability/dataonly)

## SIM

- [CTCellularPlanStatus](/documentation/coretelephony/ctcellularplanstatus)

### Get and store a token

- [class func getTokenWithCompletion((String?, (any Error)?) -> Void)](/documentation/coretelephony/ctcellularplanstatus/gettokenwithcompletion(_:))

### Check the validity of the ICCID associated with the token

- [class func checkValidity(ofToken: String, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/coretelephony/ctcellularplanstatus/checkvalidity(oftoken:completionhandler:))

## Subscriber Information

- [CTSubscriber](/documentation/coretelephony/ctsubscriber)

### Identifying the subscriber

- [var identifier: String](/documentation/coretelephony/ctsubscriber/identifier)

### Working with a delegate

- [var delegate: (any CTSubscriberDelegate)?](/documentation/coretelephony/ctsubscriber/delegate)

### Managing the carrier token

- [var carrierToken: Data?](/documentation/coretelephony/ctsubscriber/carriertoken)
- [func refreshCarrierToken() -> Bool](/documentation/coretelephony/ctsubscriber/refreshcarriertoken())
- [let CTSubscriberTokenRefreshed: String](/documentation/coretelephony/ctsubscribertokenrefreshed)

### Detecting a SIM

- [var isSIMInserted: Bool](/documentation/coretelephony/ctsubscriber/issiminserted)
- [CTSubscriberDelegate](/documentation/coretelephony/ctsubscriberdelegate)

### Handling Token Updates

- [func subscriberTokenRefreshed(CTSubscriber)](/documentation/coretelephony/ctsubscriberdelegate/subscribertokenrefreshed(_:))
- [CTSubscriberInfo](/documentation/coretelephony/ctsubscriberinfo)

### Getting Subscriber Information

- [class func subscribers() -> [CTSubscriber]](/documentation/coretelephony/ctsubscriberinfo/subscribers())
- [class func subscriber() -> CTSubscriber](/documentation/coretelephony/ctsubscriberinfo/subscriber())

## Cellular Data Access

- [CTCellularData](/documentation/coretelephony/ctcellulardata)

### Determining the Cellular Data Restricted State

- [var restrictedState: CTCellularDataRestrictedState](/documentation/coretelephony/ctcellulardata/restrictedstate)
- [CTCellularDataRestrictedState](/documentation/coretelephony/ctcellulardatarestrictedstate)

#### Constants

- [case notRestricted](/documentation/coretelephony/ctcellulardatarestrictedstate/notrestricted)
- [case restricted](/documentation/coretelephony/ctcellulardatarestrictedstate/restricted)
- [case restrictedStateUnknown](/documentation/coretelephony/ctcellulardatarestrictedstate/restrictedstateunknown)

#### Initializers

- [init?(rawValue: UInt)](/documentation/coretelephony/ctcellulardatarestrictedstate/init(rawvalue:))

### Handling Policy Changes

- [var cellularDataRestrictionDidUpdateNotifier: CellularDataRestrictionDidUpdateNotifier?](/documentation/coretelephony/ctcellulardata/cellulardatarestrictiondidupdatenotifier)
- [CellularDataRestrictionDidUpdateNotifier](/documentation/coretelephony/cellulardatarestrictiondidupdatenotifier)

## Errors

- [CTError](/documentation/coretelephony/cterror)

### Getting Error Properties

- [var domain: Int32](/documentation/coretelephony/cterror/domain)
- [var error: Int32](/documentation/coretelephony/cterror/error)

### Identifying Error Domains

- [Error Domains](/documentation/coretelephony/error-domain-codes)

#### Error Domains

- [var kCTErrorDomainMach: Int](/documentation/coretelephony/kcterrordomainmach)
- [var kCTErrorDomainNoError: Int](/documentation/coretelephony/kcterrordomainnoerror)
- [var kCTErrorDomainPOSIX: Int](/documentation/coretelephony/kcterrordomainposix)

### Initializers

- [init()](/documentation/coretelephony/cterror/init())
- [init(domain: Int32, error: Int32)](/documentation/coretelephony/cterror/init(domain:error:))

## Deprecated

- [CTCarrier](/documentation/coretelephony/ctcarrier)

### Getting Information About the Cellular Service Provider

- [var allowsVOIP: Bool](/documentation/coretelephony/ctcarrier/allowsvoip)
- [var carrierName: String?](/documentation/coretelephony/ctcarrier/carriername)
- [var isoCountryCode: String?](/documentation/coretelephony/ctcarrier/isocountrycode)
- [var mobileCountryCode: String?](/documentation/coretelephony/ctcarrier/mobilecountrycode)
- [var mobileNetworkCode: String?](/documentation/coretelephony/ctcarrier/mobilenetworkcode)
- [CTCall](/documentation/coretelephony/ctcall)

### Obtaining Information About a Cellular Call

- [var callID: String](/documentation/coretelephony/ctcall/callid)
- [var callState: String](/documentation/coretelephony/ctcall/callstate)

### Getting Cellular Call State

- [Cellular Call States](/documentation/coretelephony/cellular-call-states)

#### Constants

- [let CTCallStateDialing: String](/documentation/coretelephony/ctcallstatedialing)
- [let CTCallStateIncoming: String](/documentation/coretelephony/ctcallstateincoming)
- [let CTCallStateConnected: String](/documentation/coretelephony/ctcallstateconnected)
- [let CTCallStateDisconnected: String](/documentation/coretelephony/ctcallstatedisconnected)
- [CTCallCenter](/documentation/coretelephony/ctcallcenter)

### Responding to Cellular Call Events

- [var callEventHandler: ((CTCall) -> Void)?](/documentation/coretelephony/ctcallcenter/calleventhandler)
- [var currentCalls: Set<CTCall>?](/documentation/coretelephony/ctcallcenter/currentcalls)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
