# StoreKit Test Documentation

Source: https://sosumi.ai/documentation/storekittest

---
title: StoreKit Test
source: https://developer.apple.com/documentation/storekittest
timestamp: 2026-02-13T19:02:34.036Z
---

## StoreKit transaction testing

- [Setting up StoreKit Testing in Xcode](/documentation/xcode/setting-up-storekit-testing-in-xcode)
- [SKTestSession](/documentation/storekittest/sktestsession)

### Initializing test sessions

- [convenience init(configurationFileNamed: String) throws](/documentation/storekittest/sktestsession/init(configurationfilenamed:))
- [init(contentsOf: URL) throws](/documentation/storekittest/sktestsession/init(contentsof:))
- [func resetToDefaultState()](/documentation/storekittest/sktestsession/resettodefaultstate())

### Configuring the test environment

- [var storefront: String](/documentation/storekittest/sktestsession/storefront)
- [var locale: Locale](/documentation/storekittest/sktestsession/locale)
- [var disableDialogs: Bool](/documentation/storekittest/sktestsession/disabledialogs)

### Managing transactions in the test environment

- [func allTransactions() -> [SKTestTransaction]](/documentation/storekittest/sktestsession/alltransactions())
- [func deleteTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/deletetransaction(identifier:))
- [func clearTransactions()](/documentation/storekittest/sktestsession/cleartransactions())

### Forcing failed transactions

- [var failTransactionsEnabled: Bool](/documentation/storekittest/sktestsession/failtransactionsenabled)
- [var failureError: SKError.Code](/documentation/storekittest/sktestsession/failureerror)

### Testing interrupted purchases

- [var interruptedPurchasesEnabled: Bool](/documentation/storekittest/sktestsession/interruptedpurchasesenabled)
- [func resolveIssueForTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/resolveissuefortransaction(identifier:))

### Testing Ask To Buy transactions

- [var askToBuyEnabled: Bool](/documentation/storekittest/sktestsession/asktobuyenabled)
- [func approveAskToBuyTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/approveasktobuytransaction(identifier:))
- [func declineAskToBuyTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/declineasktobuytransaction(identifier:))

### Testing subscription renewals

- [var timeRate: SKTestSession.TimeRate](/documentation/storekittest/sktestsession/timerate-swift.property)
- [SKTestSession.TimeRate](/documentation/storekittest/sktestsession/timerate-swift.enum)

#### Fixed time rates for subscription renewals

- [case oneRenewalEveryFifteenMinutes](/documentation/storekittest/sktestsession/timerate-swift.enum/onerenewaleveryfifteenminutes)
- [case oneRenewalEveryFiveMinutes](/documentation/storekittest/sktestsession/timerate-swift.enum/onerenewaleveryfiveminutes)
- [case oneRenewalEveryMinute](/documentation/storekittest/sktestsession/timerate-swift.enum/onerenewaleveryminute)
- [case oneRenewalEveryThirtySeconds](/documentation/storekittest/sktestsession/timerate-swift.enum/onerenewaleverythirtyseconds)
- [case oneRenewalEveryTenSeconds](/documentation/storekittest/sktestsession/timerate-swift.enum/onerenewaleverytenseconds)
- [case oneRenewalEveryTwoSeconds](/documentation/storekittest/sktestsession/timerate-swift.enum/onerenewaleverytwoseconds)

#### Scaled time rates for subscription renewals

- [case realTime](/documentation/storekittest/sktestsession/timerate-swift.enum/realtime)
- [case monthlyRenewalEveryHour](/documentation/storekittest/sktestsession/timerate-swift.enum/monthlyrenewaleveryhour)
- [case monthlyRenewalEveryThirtyMinutes](/documentation/storekittest/sktestsession/timerate-swift.enum/monthlyrenewaleverythirtyminutes)
- [case monthlyRenewalEveryFifteenMinutes](/documentation/storekittest/sktestsession/timerate-swift.enum/monthlyrenewaleveryfifteenminutes)
- [case monthlyRenewalEveryFiveMinutes](/documentation/storekittest/sktestsession/timerate-swift.enum/monthlyrenewaleveryfiveminutes)
- [case monthlyRenewalEveryThirtySeconds](/documentation/storekittest/sktestsession/timerate-swift.enum/monthlyrenewaleverythirtyseconds)

#### Deprecated

- [case oneHourIsOneDay](/documentation/storekittest/sktestsession/timerate-swift.enum/onehourisoneday)
- [case thirtyMinutesIsOneDay](/documentation/storekittest/sktestsession/timerate-swift.enum/thirtyminutesisoneday)
- [case fiveMinutesIsOneDay](/documentation/storekittest/sktestsession/timerate-swift.enum/fiveminutesisoneday)
- [case oneMinuteIsOneDay](/documentation/storekittest/sktestsession/timerate-swift.enum/oneminuteisoneday)
- [case thirtySecondsIsOneDay](/documentation/storekittest/sktestsession/timerate-swift.enum/thirtysecondsisoneday)
- [case oneSecondIsOneDay](/documentation/storekittest/sktestsession/timerate-swift.enum/onesecondisoneday)

#### Initializers

- [init?(rawValue: Int)](/documentation/storekittest/sktestsession/timerate-swift.enum/init(rawvalue:))
- [func enableAutoRenewForTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/enableautorenewfortransaction(identifier:))
- [func disableAutoRenewForTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/disableautorenewfortransaction(identifier:))
- [func forceRenewalOfSubscription(productIdentifier: String) throws](/documentation/storekittest/sktestsession/forcerenewalofsubscription(productidentifier:))
- [func expireSubscription(productIdentifier: String) throws](/documentation/storekittest/sktestsession/expiresubscription(productidentifier:))

### Testing billing retry and grace period

- [var billingGracePeriodIsEnabled: Bool](/documentation/storekittest/sktestsession/billinggraceperiodisenabled)
- [var shouldEnterBillingRetryOnRenewal: Bool](/documentation/storekittest/sktestsession/shouldenterbillingretryonrenewal)
- [func resolveIssueForTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/resolveissuefortransaction(identifier:))

### Testing price increase consent

- [func requestPriceIncreaseConsentForTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/requestpriceincreaseconsentfortransaction(identifier:))
- [func consentToPriceIncreaseForTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/consenttopriceincreasefortransaction(identifier:))
- [func declinePriceIncreaseForTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/declinepriceincreasefortransaction(identifier:))

### Testing externally performed transactions

- [func buyProduct(productIdentifier: String) throws](/documentation/storekittest/sktestsession/buyproduct(productidentifier:))
- [func refundTransaction(identifier: Int) throws](/documentation/storekittest/sktestsession/refundtransaction(identifier:))

### Instance Methods

- [func buyProduct(identifier: Product.ID, options: Set<Product.PurchaseOption>) async throws -> Transaction](/documentation/storekittest/sktestsession/buyproduct(identifier:options:))
- [func setSimulatedError<API>(API.Failure?, forAPI: API) async throws](/documentation/storekittest/sktestsession/setsimulatederror(_:forapi:))
- [func simulatedError<API>(forAPI: API) async -> API.Failure?](/documentation/storekittest/sktestsession/simulatederror(forapi:))
- [SKTestTransaction](/documentation/storekittest/sktesttransaction)

### Identifying Transactions and Products

- [var identifier: Int](/documentation/storekittest/sktesttransaction/identifier)
- [var originalTransactionIdentifier: Int](/documentation/storekittest/sktesttransaction/originaltransactionidentifier)
- [var productIdentifier: String](/documentation/storekittest/sktesttransaction/productidentifier)

### Getting Payment Transaction States

- [var state: SKPaymentTransactionState](/documentation/storekittest/sktesttransaction/state)

### Getting Dates

- [var purchaseDate: Date](/documentation/storekittest/sktesttransaction/purchasedate)
- [var cancelDate: Date?](/documentation/storekittest/sktesttransaction/canceldate)
- [var expirationDate: Date?](/documentation/storekittest/sktesttransaction/expirationdate)

### Getting Test Environment States

- [var autoRenewingEnabled: Bool](/documentation/storekittest/sktesttransaction/autorenewingenabled)
- [var hasPurchaseIssue: Bool](/documentation/storekittest/sktesttransaction/haspurchaseissue)
- [var isPendingPriceIncreaseConsent: Bool](/documentation/storekittest/sktesttransaction/ispendingpriceincreaseconsent)
- [var pendingAskToBuyConfirmation: Bool](/documentation/storekittest/sktesttransaction/pendingasktobuyconfirmation)

## StoreKit transaction testing errors

- [let SKTestErrorDomain: String](/documentation/storekittest/sktesterrordomain)
- [SKTestError](/documentation/storekittest/sktesterror)

### Error Domain

- [static var errorDomain: String](/documentation/storekittest/sktesterror/errordomain)

### Error Codes

- [static var fileNotFound: SKTestError.Code](/documentation/storekittest/sktesterror/filenotfound)
- [static var invalidAction: SKTestError.Code](/documentation/storekittest/sktesterror/invalidaction)
- [static var invalidProductIdentifier: SKTestError.Code](/documentation/storekittest/sktesterror/invalidproductidentifier)
- [static var invalidProductType: SKTestError.Code](/documentation/storekittest/sktesterror/invalidproducttype)
- [static var invalidURL: SKTestError.Code](/documentation/storekittest/sktesterror/invalidurl)
- [static var noSubscriptionFound: SKTestError.Code](/documentation/storekittest/sktesterror/nosubscriptionfound)
- [static var noTransactionFound: SKTestError.Code](/documentation/storekittest/sktesterror/notransactionfound)
- [static var serviceUnavailable: SKTestError.Code](/documentation/storekittest/sktesterror/serviceunavailable)
- [SKTestError.Code](/documentation/storekittest/sktesterror/code)

#### Error Codes

- [case fileNotFound](/documentation/storekittest/sktesterror/code/filenotfound)
- [case invalidAction](/documentation/storekittest/sktesterror/code/invalidaction)
- [case invalidProductIdentifier](/documentation/storekittest/sktesterror/code/invalidproductidentifier)
- [case invalidProductType](/documentation/storekittest/sktesterror/code/invalidproducttype)
- [case invalidURL](/documentation/storekittest/sktesterror/code/invalidurl)
- [case noSubscriptionFound](/documentation/storekittest/sktesterror/code/nosubscriptionfound)
- [case noTransactionFound](/documentation/storekittest/sktesterror/code/notransactionfound)
- [case serviceUnavailable](/documentation/storekittest/sktesterror/code/serviceunavailable)
- [case fileNotFound](/documentation/storekittest/sktesterror/code/filenotfound)
- [case invalidAction](/documentation/storekittest/sktesterror/code/invalidaction)
- [case invalidProductIdentifier](/documentation/storekittest/sktesterror/code/invalidproductidentifier)
- [case invalidProductType](/documentation/storekittest/sktesterror/code/invalidproducttype)
- [case invalidURL](/documentation/storekittest/sktesterror/code/invalidurl)
- [case noSubscriptionFound](/documentation/storekittest/sktesterror/code/nosubscriptionfound)
- [case noTransactionFound](/documentation/storekittest/sktesterror/code/notransactionfound)
- [case serviceUnavailable](/documentation/storekittest/sktesterror/code/serviceunavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/storekittest/sktesterror/code/init(rawvalue:))

## Ad impression and postback testing

- [Testing and validating ad impression signatures and postbacks for SKAdNetwork](/documentation/storekittest/testing-and-validating-ad-impression-signatures-and-postbacks-for-skadnetwork)
- [SKAdTestSession](/documentation/storekittest/skadtestsession)

### Validating impressions

- [func validate(SKAdImpression, publicKey: String) throws](/documentation/storekittest/skadtestsession/validate(_:publickey:))
- [func validateImpression(parameters: [String : Any], publicKey: String) throws](/documentation/storekittest/skadtestsession/validateimpression(parameters:publickey:))
- [func validateWebAdImpressionPayload(Data, publicKey: String) throws](/documentation/storekittest/skadtestsession/validatewebadimpressionpayload(_:publickey:))

### Adding and sending postbacks

- [func setPostbacks([SKAdTestPostback]) throws](/documentation/storekittest/skadtestsession/setpostbacks(_:))
- [var postbacks: [SKAdTestPostback]](/documentation/storekittest/skadtestsession/postbacks)
- [func flushPostbacks(responses: ([String : SKAdTestPostbackResponse]?, (any Error)?) -> Void)](/documentation/storekittest/skadtestsession/flushpostbacks(responses:))
- [SKANTestPostbackResponseHandler](/documentation/storekittest/skantestpostbackresponsehandler)

### Viewing the developer postback URL

- [var developerPostbackURL: URL?](/documentation/storekittest/skadtestsession/developerpostbackurl)

### Initializing test sessions

- [init()](/documentation/storekittest/skadtestsession/init())
- [SKAdTestPostback](/documentation/storekittest/skadtestpostback)

### Creating test postbacks

- [init?(version: SKAdTestPostbackVersion, adNetworkIdentifier: String, sourceIdentifier: String, appStoreItemIdentifier: Int, sourceAppStoreItemIdentifier: Int, sourceDomain: String?, fidelityType: Int, isRedownload: Bool, didWin: Bool, postbackURL: String)](/documentation/storekittest/skadtestpostback/init(version:adnetworkidentifier:sourceidentifier:appstoreitemidentifier:sourceappstoreitemidentifier:sourcedomain:fidelitytype:isredownload:didwin:postbackurl:))
- [class func winningPostbacks(withVersion: SKAdTestPostbackVersion, adNetworkIdentifier: String, sourceIdentifier: String, appStoreItemIdentifier: Int, sourceAppStoreItemIdentifier: Int, sourceDomain: String?, fidelityType: Int, isRedownload: Bool, postbackURL: String) -> [SKAdTestPostback]?](/documentation/storekittest/skadtestpostback/winningpostbacks(withversion:adnetworkidentifier:sourceidentifier:appstoreitemidentifier:sourceappstoreitemidentifier:sourcedomain:fidelitytype:isredownload:postbackurl:))
- [init?(version: SKAdTestPostbackVersion, adNetworkIdentifier: String, adCampaignIdentifier: Int, appStoreItemIdentifier: Int, sourceAppStoreItemIdentifier: Int, conversionValue: Int, fidelityType: Int, isRedownload: Bool, didWin: Bool, postbackURL: String)](/documentation/storekittest/skadtestpostback/init(version:adnetworkidentifier:adcampaignidentifier:appstoreitemidentifier:sourceappstoreitemidentifier:conversionvalue:fidelitytype:isredownload:didwin:postbackurl:))

### Getting the Postback Destination

- [var postbackURL: String](/documentation/storekittest/skadtestpostback/postbackurl)

### Getting general information

- [var version: SKAdTestPostbackVersion](/documentation/storekittest/skadtestpostback/version)
- [var transactionIdentifier: String](/documentation/storekittest/skadtestpostback/transactionidentifier)
- [var postbackSequenceIndex: Int](/documentation/storekittest/skadtestpostback/postbacksequenceindex)
- [var isRegistered: Bool](/documentation/storekittest/skadtestpostback/isregistered)
- [var isRedownload: Bool](/documentation/storekittest/skadtestpostback/isredownload)

### Getting advertisement information

- [var adNetworkIdentifier: String](/documentation/storekittest/skadtestpostback/adnetworkidentifier)
- [var appStoreItemIdentifier: Int](/documentation/storekittest/skadtestpostback/appstoreitemidentifier)
- [var sourceAppStoreItemIdentifier: Int](/documentation/storekittest/skadtestpostback/sourceappstoreitemidentifier)
- [var sourceDomain: String?](/documentation/storekittest/skadtestpostback/sourcedomain)
- [var sourceIdentifier: String?](/documentation/storekittest/skadtestpostback/sourceidentifier)

### Getting conversion information

- [var fidelityType: Int](/documentation/storekittest/skadtestpostback/fidelitytype)
- [var fineConversionValue: Int](/documentation/storekittest/skadtestpostback/fineconversionvalue)
- [var coarseConversionValue: SKAdNetwork.CoarseConversionValue?](/documentation/storekittest/skadtestpostback/coarseconversionvalue)
- [var didWin: Bool](/documentation/storekittest/skadtestpostback/didwin)

### Getting information in earlier versions

- [var adCampaignIdentifier: Int](/documentation/storekittest/skadtestpostback/adcampaignidentifier)
- [var conversionValue: Int](/documentation/storekittest/skadtestpostback/conversionvalue)
- [SKAdTestPostbackResponse](/documentation/storekittest/skadtestpostbackresponse)

### Getting Postback Responses

- [var didSucceed: Bool](/documentation/storekittest/skadtestpostbackresponse/didsucceed)
- [var httpResponse: HTTPURLResponse?](/documentation/storekittest/skadtestpostbackresponse/httpresponse)
- [var error: (any Error)?](/documentation/storekittest/skadtestpostbackresponse/error)
- [SKAdTestPostbackVersion](/documentation/storekittest/skadtestpostbackversion)

### Getting SKAdNetwork Versions

- [static let version4_0: SKAdTestPostbackVersion](/documentation/storekittest/skadtestpostbackversion/version4_0)
- [static let version3_0: SKAdTestPostbackVersion](/documentation/storekittest/skadtestpostbackversion/version3_0)
- [static let version2_2: SKAdTestPostbackVersion](/documentation/storekittest/skadtestpostbackversion/version2_2)
- [static let version2_1: SKAdTestPostbackVersion](/documentation/storekittest/skadtestpostbackversion/version2_1)

### Initializing the Postback Version

- [init(rawValue: String)](/documentation/storekittest/skadtestpostbackversion/init(rawvalue:))

## Ad impression and postback errors

- [let SKAdTestErrorDomain: String](/documentation/storekittest/skadtesterrordomain)
- [SKAdTestError](/documentation/storekittest/skadtesterror)

### Getting Signature Errors

- [static var missingSignature: SKAdTestError.Code](/documentation/storekittest/skadtesterror/missingsignature)
- [static var signatureInvalidKey: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signatureinvalidkey)
- [static var signatureInvalidOrder: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signatureinvalidorder)
- [static var signatureMissingAdNetworkId: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingadnetworkid)
- [static var signatureMissingAppAdamId: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingappadamid)
- [static var signatureMissingFidelityType: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingfidelitytype)
- [static var signatureMissingNonce: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingnonce)
- [static var signatureMissingSourceAppAdamId: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingsourceappadamid)
- [static var signatureMissingSourceDomain: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingsourcedomain)
- [static var signatureMissingSourceIdentifier: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingsourceidentifier)
- [static var signatureMissingTimestamp: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingtimestamp)
- [static var signatureUnknownError: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signatureunknownerror)
- [static var signatureVerificationFailed: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signatureverificationfailed)

### Getting Postback Errors

- [static var excessivePostbacks: SKAdTestError.Code](/documentation/storekittest/skadtesterror/excessivepostbacks)
- [static var invalidConversionValue: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidconversionvalue)
- [static var invalidPostbackURL: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidpostbackurl)
- [static var invalidRunnerUpPostback: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidrunneruppostback)
- [static var invalidWinningPostbackCount: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidwinningpostbackcount)
- [static var malformedPostbacks: SKAdTestError.Code](/documentation/storekittest/skadtesterror/malformedpostbacks)
- [static var missingPostbacks: SKAdTestError.Code](/documentation/storekittest/skadtesterror/missingpostbacks)
- [static var misplacedWinnerPostback: SKAdTestError.Code](/documentation/storekittest/skadtesterror/misplacedwinnerpostback)
- [static var missingWinningPostback: SKAdTestError.Code](/documentation/storekittest/skadtesterror/missingwinningpostback)
- [static var noPendingPostbacks: SKAdTestError.Code](/documentation/storekittest/skadtesterror/nopendingpostbacks)
- [static var unlinkedWinningPostbacks: SKAdTestError.Code](/documentation/storekittest/skadtesterror/unlinkedwinningpostbacks)

### Getting Other Errors

- [static var invalidVersion: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidversion)
- [static var invalidImpressionId: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidimpressionid)
- [static var invalidSourceAppAdamId: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidsourceappadamid)
- [static var invalidSourceDomain: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidsourcedomain)
- [static var invalidSourceIdentifier: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidsourceidentifier)
- [static var unknownError: SKAdTestError.Code](/documentation/storekittest/skadtesterror/unknownerror)

### Getting Older Errors

- [static var invalidCampaignId: SKAdTestError.Code](/documentation/storekittest/skadtesterror/invalidcampaignid)
- [static var signatureMissingCampaignId: SKAdTestError.Code](/documentation/storekittest/skadtesterror/signaturemissingcampaignid)
- [static var conflictingSource: SKAdTestError.Code](/documentation/storekittest/skadtesterror/conflictingsource)

### Initializing the Error Objects

- [SKAdTestError.Code](/documentation/storekittest/skadtesterror/code)

#### Signature Errors

- [case missingSignature](/documentation/storekittest/skadtesterror/code/missingsignature)
- [case signatureInvalidKey](/documentation/storekittest/skadtesterror/code/signatureinvalidkey)
- [case signatureInvalidOrder](/documentation/storekittest/skadtesterror/code/signatureinvalidorder)
- [case signatureMissingAdNetworkId](/documentation/storekittest/skadtesterror/code/signaturemissingadnetworkid)
- [case signatureMissingAppAdamId](/documentation/storekittest/skadtesterror/code/signaturemissingappadamid)
- [case signatureMissingFidelityType](/documentation/storekittest/skadtesterror/code/signaturemissingfidelitytype)
- [case signatureMissingNonce](/documentation/storekittest/skadtesterror/code/signaturemissingnonce)
- [case signatureMissingSourceAppAdamId](/documentation/storekittest/skadtesterror/code/signaturemissingsourceappadamid)
- [case signatureMissingSourceDomain](/documentation/storekittest/skadtesterror/code/signaturemissingsourcedomain)
- [case signatureMissingSourceIdentifier](/documentation/storekittest/skadtesterror/code/signaturemissingsourceidentifier)
- [case signatureMissingTimestamp](/documentation/storekittest/skadtesterror/code/signaturemissingtimestamp)
- [case signatureUnknownError](/documentation/storekittest/skadtesterror/code/signatureunknownerror)
- [case signatureVerificationFailed](/documentation/storekittest/skadtesterror/code/signatureverificationfailed)
- [case missingSignature](/documentation/storekittest/skadtesterror/code/missingsignature)
- [case signatureInvalidKey](/documentation/storekittest/skadtesterror/code/signatureinvalidkey)
- [case signatureInvalidOrder](/documentation/storekittest/skadtesterror/code/signatureinvalidorder)
- [case signatureMissingAdNetworkId](/documentation/storekittest/skadtesterror/code/signaturemissingadnetworkid)
- [case signatureMissingAppAdamId](/documentation/storekittest/skadtesterror/code/signaturemissingappadamid)
- [case signatureMissingFidelityType](/documentation/storekittest/skadtesterror/code/signaturemissingfidelitytype)
- [case signatureMissingNonce](/documentation/storekittest/skadtesterror/code/signaturemissingnonce)
- [case signatureMissingSourceAppAdamId](/documentation/storekittest/skadtesterror/code/signaturemissingsourceappadamid)
- [case signatureMissingSourceDomain](/documentation/storekittest/skadtesterror/code/signaturemissingsourcedomain)
- [case signatureMissingSourceIdentifier](/documentation/storekittest/skadtesterror/code/signaturemissingsourceidentifier)
- [case signatureMissingTimestamp](/documentation/storekittest/skadtesterror/code/signaturemissingtimestamp)
- [case signatureUnknownError](/documentation/storekittest/skadtesterror/code/signatureunknownerror)
- [case signatureVerificationFailed](/documentation/storekittest/skadtesterror/code/signatureverificationfailed)

#### Postback Errors

- [case excessivePostbacks](/documentation/storekittest/skadtesterror/code/excessivepostbacks)
- [case invalidConversionValue](/documentation/storekittest/skadtesterror/code/invalidconversionvalue)
- [case invalidPostbackURL](/documentation/storekittest/skadtesterror/code/invalidpostbackurl)
- [case invalidRunnerUpPostback](/documentation/storekittest/skadtesterror/code/invalidrunneruppostback)
- [case invalidWinningPostbackCount](/documentation/storekittest/skadtesterror/code/invalidwinningpostbackcount)
- [case malformedPostbacks](/documentation/storekittest/skadtesterror/code/malformedpostbacks)
- [case missingPostbacks](/documentation/storekittest/skadtesterror/code/missingpostbacks)
- [case misplacedWinnerPostback](/documentation/storekittest/skadtesterror/code/misplacedwinnerpostback)
- [case missingWinningPostback](/documentation/storekittest/skadtesterror/code/missingwinningpostback)
- [case noPendingPostbacks](/documentation/storekittest/skadtesterror/code/nopendingpostbacks)
- [case unlinkedWinningPostbacks](/documentation/storekittest/skadtesterror/code/unlinkedwinningpostbacks)
- [case excessivePostbacks](/documentation/storekittest/skadtesterror/code/excessivepostbacks)
- [case invalidConversionValue](/documentation/storekittest/skadtesterror/code/invalidconversionvalue)
- [case invalidPostbackURL](/documentation/storekittest/skadtesterror/code/invalidpostbackurl)
- [case invalidRunnerUpPostback](/documentation/storekittest/skadtesterror/code/invalidrunneruppostback)
- [case invalidWinningPostbackCount](/documentation/storekittest/skadtesterror/code/invalidwinningpostbackcount)
- [case malformedPostbacks](/documentation/storekittest/skadtesterror/code/malformedpostbacks)
- [case missingPostbacks](/documentation/storekittest/skadtesterror/code/missingpostbacks)
- [case misplacedWinnerPostback](/documentation/storekittest/skadtesterror/code/misplacedwinnerpostback)
- [case missingWinningPostback](/documentation/storekittest/skadtesterror/code/missingwinningpostback)
- [case noPendingPostbacks](/documentation/storekittest/skadtesterror/code/nopendingpostbacks)
- [case unlinkedWinningPostbacks](/documentation/storekittest/skadtesterror/code/unlinkedwinningpostbacks)

#### Other Errors

- [case invalidVersion](/documentation/storekittest/skadtesterror/code/invalidversion)
- [case invalidImpressionId](/documentation/storekittest/skadtesterror/code/invalidimpressionid)
- [case invalidSourceAppAdamId](/documentation/storekittest/skadtesterror/code/invalidsourceappadamid)
- [case invalidSourceDomain](/documentation/storekittest/skadtesterror/code/invalidsourcedomain)
- [case invalidSourceIdentifier](/documentation/storekittest/skadtesterror/code/invalidsourceidentifier)
- [case unknownError](/documentation/storekittest/skadtesterror/code/unknownerror)
- [case invalidVersion](/documentation/storekittest/skadtesterror/code/invalidversion)
- [case invalidImpressionId](/documentation/storekittest/skadtesterror/code/invalidimpressionid)
- [case invalidSourceAppAdamId](/documentation/storekittest/skadtesterror/code/invalidsourceappadamid)
- [case invalidSourceDomain](/documentation/storekittest/skadtesterror/code/invalidsourcedomain)
- [case invalidSourceIdentifier](/documentation/storekittest/skadtesterror/code/invalidsourceidentifier)
- [case unknownError](/documentation/storekittest/skadtesterror/code/unknownerror)

#### Older Errors

- [case invalidCampaignId](/documentation/storekittest/skadtesterror/code/invalidcampaignid)
- [case signatureMissingCampaignId](/documentation/storekittest/skadtesterror/code/signaturemissingcampaignid)
- [case conflictingSource](/documentation/storekittest/skadtesterror/code/conflictingsource)
- [case invalidCampaignId](/documentation/storekittest/skadtesterror/code/invalidcampaignid)
- [case signatureMissingCampaignId](/documentation/storekittest/skadtesterror/code/signaturemissingcampaignid)
- [case conflictingSource](/documentation/storekittest/skadtesterror/code/conflictingsource)

#### Initializers

- [init?(rawValue: Int)](/documentation/storekittest/skadtesterror/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/storekittest/skadtesterror/errordomain)

## Structures

- [StoreKitAppStoreSyncAPI](/documentation/storekittest/storekitappstoresyncapi)

### Initializers

- [init()](/documentation/storekittest/storekitappstoresyncapi/init())
- [StoreKitAppTransactionAPI](/documentation/storekittest/storekitapptransactionapi)

### Initializers

- [init()](/documentation/storekittest/storekitapptransactionapi/init())
- [StoreKitLoadProductsAPI](/documentation/storekittest/storekitloadproductsapi)

### Initializers

- [init()](/documentation/storekittest/storekitloadproductsapi/init())
- [StoreKitManageSubscriptionsAPI](/documentation/storekittest/storekitmanagesubscriptionsapi)

### Initializers

- [init()](/documentation/storekittest/storekitmanagesubscriptionsapi/init())
- [StoreKitOfferCodeRedeemAPI](/documentation/storekittest/storekitoffercoderedeemapi)

### Initializers

- [init()](/documentation/storekittest/storekitoffercoderedeemapi/init())
- [StoreKitPurchaseAPI](/documentation/storekittest/storekitpurchaseapi)

### Initializers

- [init()](/documentation/storekittest/storekitpurchaseapi/init())
- [StoreKitRefundRequestAPI](/documentation/storekittest/storekitrefundrequestapi)

### Initializers

- [init()](/documentation/storekittest/storekitrefundrequestapi/init())
- [StoreKitSubscriptionStatusAPI](/documentation/storekittest/storekitsubscriptionstatusapi)

### Initializers

- [init()](/documentation/storekittest/storekitsubscriptionstatusapi/init())
- [StoreKitVerificationAPI](/documentation/storekittest/storekitverificationapi)

### Initializers

- [init()](/documentation/storekittest/storekitverificationapi/init())

## Enumerations

- [SKTestFailures](/documentation/storekittest/sktestfailures)

### Enumerations

- [SKTestFailures.AppStoreSync](/documentation/storekittest/sktestfailures/appstoresync)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/appstoresync/generic(_:))
- [SKTestFailures.AppTransaction](/documentation/storekittest/sktestfailures/apptransaction)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/apptransaction/generic(_:))
- [SKTestFailures.LoadProducts](/documentation/storekittest/sktestfailures/loadproducts)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/loadproducts/generic(_:))
- [SKTestFailures.ManageSubscriptions](/documentation/storekittest/sktestfailures/managesubscriptions)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/managesubscriptions/generic(_:))
- [SKTestFailures.OfferCodeRedeem](/documentation/storekittest/sktestfailures/offercoderedeem)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/offercoderedeem/generic(_:))
- [SKTestFailures.Purchase](/documentation/storekittest/sktestfailures/purchase)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/purchase/generic(_:))
- [case purchase(Product.PurchaseError)](/documentation/storekittest/sktestfailures/purchase/purchase(_:))
- [SKTestFailures.RefundRequest](/documentation/storekittest/sktestfailures/refundrequest)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/refundrequest/generic(_:))
- [case refundRequest(Transaction.RefundRequestError)](/documentation/storekittest/sktestfailures/refundrequest/refundrequest(_:))
- [SKTestFailures.SubscriptionStatus](/documentation/storekittest/sktestfailures/subscriptionstatus)

#### Enumeration Cases

- [case generic(StoreKitError)](/documentation/storekittest/sktestfailures/subscriptionstatus/generic(_:))
- [SKTestFailures.Verification](/documentation/storekittest/sktestfailures/verification)

#### Enumeration Cases

- [case verification(VerificationResult<Any>.VerificationError)](/documentation/storekittest/sktestfailures/verification/verification(_:))

## Protocols

- [FailableStoreKitAPI](/documentation/storekittest/failablestorekitapi)

### Associated Types

- [Failure](/documentation/storekittest/failablestorekitapi/failure)

### Type Properties

- [static var appStoreSync: StoreKitAppStoreSyncAPI](/documentation/storekittest/failablestorekitapi/appstoresync)
- [static var appTransaction: StoreKitAppTransactionAPI](/documentation/storekittest/failablestorekitapi/apptransaction)
- [static var loadProducts: StoreKitLoadProductsAPI](/documentation/storekittest/failablestorekitapi/loadproducts)
- [static var manageSubscriptions: StoreKitManageSubscriptionsAPI](/documentation/storekittest/failablestorekitapi/managesubscriptions)
- [static var offerCodeRedeem: StoreKitOfferCodeRedeemAPI](/documentation/storekittest/failablestorekitapi/offercoderedeem)
- [static var purchase: StoreKitPurchaseAPI](/documentation/storekittest/failablestorekitapi/purchase)
- [static var refundRequest: StoreKitRefundRequestAPI](/documentation/storekittest/failablestorekitapi/refundrequest)
- [static var subscriptionStatus: StoreKitSubscriptionStatusAPI](/documentation/storekittest/failablestorekitapi/subscriptionstatus)
- [static var verification: StoreKitVerificationAPI](/documentation/storekittest/failablestorekitapi/verification)
- [SKTestFailure](/documentation/storekittest/sktestfailure)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
