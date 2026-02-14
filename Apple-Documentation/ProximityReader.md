# ProximityReader Documentation

Source: https://sosumi.ai/documentation/proximityreader

---
title: ProximityReader
source: https://developer.apple.com/documentation/proximityreader
timestamp: 2026-02-13T19:00:50.000Z
---

## Payment card reader

- [Setting up Tap to Pay on iPhone](/documentation/proximityreader/setting-up-the-entitlement-for-tap-to-pay-on-iphone)
- [Adding support for Tap to Pay on iPhone to your app](/documentation/proximityreader/adding-support-for-tap-to-pay-on-iphone-to-your-app)
- [PaymentCardReader](/documentation/proximityreader/paymentcardreader)

### Creating a payment reader

- [init(options: PaymentCardReader.Options)](/documentation/proximityreader/paymentcardreader/init(options:))
- [PaymentCardReader.Options](/documentation/proximityreader/paymentcardreader/options-swift.struct)

#### Creating an options structure

- [init(vasMerchants: [VASRequest.Merchant])](/documentation/proximityreader/paymentcardreader/options-swift.struct/init(vasmerchants:))

#### Getting the list of merchants

- [var vasMerchants: [VASRequest.Merchant]](/documentation/proximityreader/paymentcardreader/options-swift.struct/vasmerchants)

#### Setting read behaviors

- [var includeErrorInReadResult: Bool](/documentation/proximityreader/paymentcardreader/options-swift.struct/includeerrorinreadresult)
- [var returnReadResultImmediately: Bool](/documentation/proximityreader/paymentcardreader/options-swift.struct/returnreadresultimmediately)

#### Initializers

- [init()](/documentation/proximityreader/paymentcardreader/options-swift.struct/init())

### Getting the feature availability

- [static let isSupported: Bool](/documentation/proximityreader/paymentcardreader/issupported)

### Configuring Tap to Pay on iPhone

- [func prepare(using: PaymentCardReader.Token) async throws -> PaymentCardReaderSession](/documentation/proximityreader/paymentcardreader/prepare(using:))

### Displaying the Tap to Pay on iPhone’s terms and conditions

- [func isAccountLinked(using: PaymentCardReader.Token) async throws -> Bool](/documentation/proximityreader/paymentcardreader/isaccountlinked(using:))
- [func linkAccount(using: PaymentCardReader.Token) async throws](/documentation/proximityreader/paymentcardreader/linkaccount(using:))
- [func relinkAccount(using: PaymentCardReader.Token) async throws](/documentation/proximityreader/paymentcardreader/relinkaccount(using:))
- [PaymentCardReader.Token](/documentation/proximityreader/paymentcardreader/token)

#### Creating a token

- [init(rawValue: String)](/documentation/proximityreader/paymentcardreader/token/init(rawvalue:))

#### Getting the token value

- [let rawValue: String](/documentation/proximityreader/paymentcardreader/token/rawvalue)

### Observing reader events

- [let events: AsyncStream<PaymentCardReader.Event>](/documentation/proximityreader/paymentcardreader/events)
- [PaymentCardReader.Event](/documentation/proximityreader/paymentcardreader/event)

#### Getting the event type

- [case cardDetected](/documentation/proximityreader/paymentcardreader/event/carddetected)
- [case pinEntryCompleted](/documentation/proximityreader/paymentcardreader/event/pinentrycompleted)
- [case pinEntryRequested](/documentation/proximityreader/paymentcardreader/event/pinentryrequested)
- [case readCancelled](/documentation/proximityreader/paymentcardreader/event/readcancelled)
- [case readCompleted](/documentation/proximityreader/paymentcardreader/event/readcompleted)
- [case readNotCompleted](/documentation/proximityreader/paymentcardreader/event/readnotcompleted)
- [case readRetry](/documentation/proximityreader/paymentcardreader/event/readretry)
- [case readyForTap](/documentation/proximityreader/paymentcardreader/event/readyfortap)
- [case removeCard](/documentation/proximityreader/paymentcardreader/event/removecard)
- [case updateProgress(Int)](/documentation/proximityreader/paymentcardreader/event/updateprogress(_:))
- [case userInterfaceDismissed](/documentation/proximityreader/paymentcardreader/event/userinterfacedismissed)
- [case notReady](/documentation/proximityreader/paymentcardreader/event/notready)

#### Getting the event name

- [var name: String](/documentation/proximityreader/paymentcardreader/event/name)

### Getting the configuration details

- [var readerIdentifier: String](/documentation/proximityreader/paymentcardreader/readeridentifier)
- [let options: PaymentCardReader.Options](/documentation/proximityreader/paymentcardreader/options-swift.property)

### Deprecated

- [let id: String](/documentation/proximityreader/paymentcardreader/id)
- [func prepare(using: PaymentCardReader.Token, updateHandler: ((PaymentCardReader.UpdateEvent) -> Void)?) async throws -> PaymentCardReaderSession](/documentation/proximityreader/paymentcardreader/prepare(using:updatehandler:))
- [PaymentCardReader.UpdateEvent](/documentation/proximityreader/paymentcardreader/updateevent)

#### Enumeration Cases

- [case notReady](/documentation/proximityreader/paymentcardreader/updateevent/notready)
- [case progress(Int)](/documentation/proximityreader/paymentcardreader/updateevent/progress(_:))

#### Instance Properties

- [var name: String](/documentation/proximityreader/paymentcardreader/updateevent/name)

### Instance Methods

- [func fetchPaymentCardReaderStore() throws -> PaymentCardReaderStore](/documentation/proximityreader/paymentcardreader/fetchpaymentcardreaderstore())
- [func prepareStoreAndForward() async throws -> StoreAndForwardPaymentCardReaderSession](/documentation/proximityreader/paymentcardreader/preparestoreandforward())
- [PaymentCardReaderSession](/documentation/proximityreader/paymentcardreadersession)

### Reading a payment card

- [func readPaymentCard(PaymentCardTransactionRequest) async throws -> PaymentCardReadResult](/documentation/proximityreader/paymentcardreadersession/readpaymentcard(_:)-8jol5)
- [func readPaymentCard(PaymentCardVerificationRequest) async throws -> PaymentCardReadResult](/documentation/proximityreader/paymentcardreadersession/readpaymentcard(_:)-hr97)

### Reading a loyalty card

- [func readPaymentCard(PaymentCardTransactionRequest, vasRequest: VASRequest, stopOnVASResult: Bool) async throws -> (PaymentCardReadResult?, VASReadResult?)](/documentation/proximityreader/paymentcardreadersession/readpaymentcard(_:vasrequest:stoponvasresult:))
- [func readVAS(VASRequest) async throws -> VASReadResult](/documentation/proximityreader/paymentcardreadersession/readvas(_:))

### Requesting the PIN

- [func capturePIN(using: PaymentCardReaderSession.PINToken, cardReaderTransactionID: String) async throws -> PaymentCardReadResult](/documentation/proximityreader/paymentcardreadersession/capturepin(using:cardreadertransactionid:))
- [PaymentCardReaderSession.PINToken](/documentation/proximityreader/paymentcardreadersession/pintoken)

#### Creating a token

- [init(rawValue: String)](/documentation/proximityreader/paymentcardreadersession/pintoken/init(rawvalue:))

#### Getting the token value

- [let rawValue: String](/documentation/proximityreader/paymentcardreadersession/pintoken/rawvalue)

### Canceling the reading process

- [func cancelRead() async throws -> Bool](/documentation/proximityreader/paymentcardreadersession/cancelread())

### Getting error information

- [PaymentCardReaderSession.ReadError](/documentation/proximityreader/paymentcardreadersession/readerror)

#### Getting the error

- [case cardReadFailed](/documentation/proximityreader/paymentcardreadersession/readerror/cardreadfailed)
- [case invalidAmount](/documentation/proximityreader/paymentcardreadersession/readerror/invalidamount)
- [case invalidCurrencyCode](/documentation/proximityreader/paymentcardreadersession/readerror/invalidcurrencycode)
- [case invalidPreferredAID](/documentation/proximityreader/paymentcardreadersession/readerror/invalidpreferredaid)
- [case invalidVASMerchants(String?)](/documentation/proximityreader/paymentcardreadersession/readerror/invalidvasmerchants(_:))
- [case invalidVASRequestParameters(String?)](/documentation/proximityreader/paymentcardreadersession/readerror/invalidvasrequestparameters(_:))
- [case nfcDisabled](/documentation/proximityreader/paymentcardreadersession/readerror/nfcdisabled)
- [case noReaderSession](/documentation/proximityreader/paymentcardreadersession/readerror/noreadersession)
- [case passcodeDisabled](/documentation/proximityreader/paymentcardreadersession/readerror/passcodedisabled)
- [case paymentCardDeclined](/documentation/proximityreader/paymentcardreadersession/readerror/paymentcarddeclined)
- [case paymentReadFailed](/documentation/proximityreader/paymentcardreadersession/readerror/paymentreadfailed)
- [case pinCancelled](/documentation/proximityreader/paymentcardreadersession/readerror/pincancelled)
- [case pinNotAllowed](/documentation/proximityreader/paymentcardreadersession/readerror/pinnotallowed)
- [case pinEntryFailed](/documentation/proximityreader/paymentcardreadersession/readerror/pinentryfailed)
- [case pinEntryTimeout](/documentation/proximityreader/paymentcardreadersession/readerror/pinentrytimeout)
- [case pinTokenInvalid](/documentation/proximityreader/paymentcardreadersession/readerror/pintokeninvalid)
- [case readCancelled](/documentation/proximityreader/paymentcardreadersession/readerror/readcancelled)
- [case readFromBackgroundError](/documentation/proximityreader/paymentcardreadersession/readerror/readfrombackgrounderror)
- [case readNotAllowed](/documentation/proximityreader/paymentcardreadersession/readerror/readnotallowed)
- [case readNotAllowedDuringCall](/documentation/proximityreader/paymentcardreadersession/readerror/readnotallowedduringcall)
- [case readerServiceConnectionError](/documentation/proximityreader/paymentcardreadersession/readerror/readerserviceconnectionerror)
- [case readerServiceError](/documentation/proximityreader/paymentcardreadersession/readerror/readerserviceerror)
- [case readerSessionAuthenticationError](/documentation/proximityreader/paymentcardreadersession/readerror/readersessionauthenticationerror)
- [case readerSessionBusy](/documentation/proximityreader/paymentcardreadersession/readerror/readersessionbusy)
- [case readerSessionExpired](/documentation/proximityreader/paymentcardreadersession/readerror/readersessionexpired)
- [case readerSessionNetworkError](/documentation/proximityreader/paymentcardreadersession/readerror/readersessionnetworkerror)
- [case readerTokenExpired](/documentation/proximityreader/paymentcardreadersession/readerror/readertokenexpired)
- [case vasReadFail](/documentation/proximityreader/paymentcardreadersession/readerror/vasreadfail)

#### Describing the error

- [var errorDescription: String](/documentation/proximityreader/paymentcardreadersession/readerror/errordescription)
- [var errorName: String](/documentation/proximityreader/paymentcardreadersession/readerror/errorname)

#### Enumeration Cases

- [case cardNotSupported](/documentation/proximityreader/paymentcardreadersession/readerror/cardnotsupported)
- [case readerInitializationFailed](/documentation/proximityreader/paymentcardreadersession/readerror/readerinitializationfailed)
- [case readerNotAvailable](/documentation/proximityreader/paymentcardreadersession/readerror/readernotavailable)
- [case storeAndForwardDeclineFailed](/documentation/proximityreader/paymentcardreadersession/readerror/storeandforwarddeclinefailed)
- [case storeAndForwardResultNotFound](/documentation/proximityreader/paymentcardreadersession/readerror/storeandforwardresultnotfound)
- [case unknown(code: Int)](/documentation/proximityreader/paymentcardreadersession/readerror/unknown(code:))

### Deprecated

- [func readPaymentCard(PaymentCardTransactionRequest, eventHandler: ((PaymentCardReaderSession.Event) -> Void)?) async throws -> PaymentCardReadResult](/documentation/proximityreader/paymentcardreadersession/readpaymentcard(_:eventhandler:)-2zgwn)
- [func readPaymentCard(PaymentCardVerificationRequest, eventHandler: ((PaymentCardReaderSession.Event) -> Void)?) async throws -> PaymentCardReadResult](/documentation/proximityreader/paymentcardreadersession/readpaymentcard(_:eventhandler:)-20e1w)
- [func readPaymentCard(PaymentCardTransactionRequest, vasRequest: VASRequest, stopOnVASResult: Bool, eventHandler: ((PaymentCardReaderSession.Event) -> Void)?) async throws -> (PaymentCardReadResult?, VASReadResult?)](/documentation/proximityreader/paymentcardreadersession/readpaymentcard(_:vasrequest:stoponvasresult:eventhandler:))
- [func readVAS(VASRequest, eventHandler: ((PaymentCardReaderSession.Event) -> Void)?) async throws -> VASReadResult](/documentation/proximityreader/paymentcardreadersession/readvas(_:eventhandler:))
- [let id: String](/documentation/proximityreader/paymentcardreadersession/id)
- [PaymentCardReaderSession.Event](/documentation/proximityreader/paymentcardreadersession/event)

#### Getting the event type

- [case cardDetected](/documentation/proximityreader/paymentcardreadersession/event/carddetected)
- [case completed](/documentation/proximityreader/paymentcardreadersession/event/completed)
- [case readCancelled](/documentation/proximityreader/paymentcardreadersession/event/readcancelled)
- [case readNotCompleted](/documentation/proximityreader/paymentcardreadersession/event/readnotcompleted)
- [case readyForTap](/documentation/proximityreader/paymentcardreadersession/event/readyfortap)
- [case removeCard](/documentation/proximityreader/paymentcardreadersession/event/removecard)
- [case retry](/documentation/proximityreader/paymentcardreadersession/event/retry)

#### Getting the event name

- [var name: String](/documentation/proximityreader/paymentcardreadersession/event/name)

### Instance Properties

- [let currentOSVersionDeprecationDate: Date?](/documentation/proximityreader/paymentcardreadersession/currentosversiondeprecationdate)

## Payment requests

- [PaymentCardTransactionRequest](/documentation/proximityreader/paymentcardtransactionrequest)

### Creating a transaction request

- [init(amount: Decimal, currencyCode: String, for: PaymentCardTransactionRequest.TransactionType)](/documentation/proximityreader/paymentcardtransactionrequest/init(amount:currencycode:for:))

### Getting the transaction details

- [let amount: Decimal](/documentation/proximityreader/paymentcardtransactionrequest/amount)
- [let currencyCode: String](/documentation/proximityreader/paymentcardtransactionrequest/currencycode)
- [let type: PaymentCardTransactionRequest.TransactionType](/documentation/proximityreader/paymentcardtransactionrequest/type)
- [PaymentCardTransactionRequest.TransactionType](/documentation/proximityreader/paymentcardtransactionrequest/transactiontype)

#### Getting the transaction type

- [case purchase](/documentation/proximityreader/paymentcardtransactionrequest/transactiontype/purchase)
- [case refund](/documentation/proximityreader/paymentcardtransactionrequest/transactiontype/refund)
- [var transactionDescription: PaymentCardTransactionRequest.TransactionAmountDescription?](/documentation/proximityreader/paymentcardtransactionrequest/transactiondescription)
- [PaymentCardTransactionRequest.TransactionAmountDescription](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription)

#### Enumeration Cases

- [case installment(PaymentCardTransactionRequest.PaymentCycle, amount: Decimal, payments: Int)](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription/installment(_:amount:payments:))
- [case membership(PaymentCardTransactionRequest.PaymentCycle)](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription/membership(_:))
- [case preauthorization](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription/preauthorization)
- [case preauthorizationAmount(Decimal)](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription/preauthorizationamount(_:))
- [case preauthorizationRelease](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription/preauthorizationrelease)
- [case surchargeAmount(Decimal)](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription/surchargeamount(_:))
- [case surchargePercent(Double)](/documentation/proximityreader/paymentcardtransactionrequest/transactionamountdescription/surchargepercent(_:))

### Setting the preferred Application Identifier (AID) list

- [var preferredAIDList: [Data]](/documentation/proximityreader/paymentcardtransactionrequest/preferredaidlist)

### Setting the user interface language

- [var userInterfaceLanguage: Locale.Language?](/documentation/proximityreader/paymentcardtransactionrequest/userinterfacelanguage)

### Instance Properties

- [var useISOCurrencySymbol: Bool](/documentation/proximityreader/paymentcardtransactionrequest/useisocurrencysymbol)

### Enumerations

- [PaymentCardTransactionRequest.PaymentCycle](/documentation/proximityreader/paymentcardtransactionrequest/paymentcycle)

#### Enumeration Cases

- [case monthly](/documentation/proximityreader/paymentcardtransactionrequest/paymentcycle/monthly)
- [case weekly](/documentation/proximityreader/paymentcardtransactionrequest/paymentcycle/weekly)
- [case yearly](/documentation/proximityreader/paymentcardtransactionrequest/paymentcycle/yearly)
- [PaymentCardVerificationRequest](/documentation/proximityreader/paymentcardverificationrequest)

### Creating the verification request

- [init(currencyCode: String, for: PaymentCardVerificationRequest.Reason)](/documentation/proximityreader/paymentcardverificationrequest/init(currencycode:for:))

### Getting the request details

- [let currencyCode: String](/documentation/proximityreader/paymentcardverificationrequest/currencycode)
- [let verificationReason: PaymentCardVerificationRequest.Reason](/documentation/proximityreader/paymentcardverificationrequest/verificationreason)
- [PaymentCardVerificationRequest.Reason](/documentation/proximityreader/paymentcardverificationrequest/reason)

#### Getting the verification reason

- [case lookUp](/documentation/proximityreader/paymentcardverificationrequest/reason/lookup)
- [case openTab](/documentation/proximityreader/paymentcardverificationrequest/reason/opentab)
- [case saveCard](/documentation/proximityreader/paymentcardverificationrequest/reason/savecard)
- [case other](/documentation/proximityreader/paymentcardverificationrequest/reason/other)

### Setting the user interface language

- [var userInterfaceLanguage: Locale.Language?](/documentation/proximityreader/paymentcardverificationrequest/userinterfacelanguage)
- [PaymentCardReadResult](/documentation/proximityreader/paymentcardreadresult)

### Getting the result data

- [let generalCardData: String?](/documentation/proximityreader/paymentcardreadresult/generalcarddata)
- [let paymentCardData: String?](/documentation/proximityreader/paymentcardreadresult/paymentcarddata)

### Checking the read outcome

- [let outcome: PaymentCardReadResult.ReadOutcome](/documentation/proximityreader/paymentcardreadresult/outcome)
- [PaymentCardReadResult.ReadOutcome](/documentation/proximityreader/paymentcardreadresult/readoutcome)

#### Getting the read outcome

- [case success](/documentation/proximityreader/paymentcardreadresult/readoutcome/success)
- [case failure](/documentation/proximityreader/paymentcardreadresult/readoutcome/failure)
- [case cardDeclined](/documentation/proximityreader/paymentcardreadresult/readoutcome/carddeclined)

### Getting the result ID

- [let id: String](/documentation/proximityreader/paymentcardreadresult/id)

### Getting the PIN status

- [let isPINFallback: Bool](/documentation/proximityreader/paymentcardreadresult/ispinfallback)
- [let pinBypassed: Bool](/documentation/proximityreader/paymentcardreadresult/pinbypassed)

### Getting the kernel type

- [let applicationTypeIdentifier: String?](/documentation/proximityreader/paymentcardreadresult/applicationtypeidentifier)

### Instance Properties

- [let cardEffectiveState: PaymentCardReadResult.CardEffectiveState?](/documentation/proximityreader/paymentcardreadresult/cardeffectivestate-swift.property)
- [let cardExpirationState: PaymentCardReadResult.CardExpirationState?](/documentation/proximityreader/paymentcardreadresult/cardexpirationstate-swift.property)

### Enumerations

- [PaymentCardReadResult.CardEffectiveState](/documentation/proximityreader/paymentcardreadresult/cardeffectivestate-swift.enum)

#### Enumeration Cases

- [case active](/documentation/proximityreader/paymentcardreadresult/cardeffectivestate-swift.enum/active)
- [case inactive](/documentation/proximityreader/paymentcardreadresult/cardeffectivestate-swift.enum/inactive)
- [case invalid](/documentation/proximityreader/paymentcardreadresult/cardeffectivestate-swift.enum/invalid)
- [case unknown](/documentation/proximityreader/paymentcardreadresult/cardeffectivestate-swift.enum/unknown)
- [PaymentCardReadResult.CardExpirationState](/documentation/proximityreader/paymentcardreadresult/cardexpirationstate-swift.enum)

#### Enumeration Cases

- [case expired](/documentation/proximityreader/paymentcardreadresult/cardexpirationstate-swift.enum/expired)
- [case invalid](/documentation/proximityreader/paymentcardreadresult/cardexpirationstate-swift.enum/invalid)
- [case notExpired](/documentation/proximityreader/paymentcardreadresult/cardexpirationstate-swift.enum/notexpired)
- [case unknown](/documentation/proximityreader/paymentcardreadresult/cardexpirationstate-swift.enum/unknown)

## Store and Forward mode

- [StoreAndForwardBatch](/documentation/proximityreader/storeandforwardbatch)

### Getting the batch details

- [let id: String](/documentation/proximityreader/storeandforwardbatch/id)
- [let count: Int](/documentation/proximityreader/storeandforwardbatch/count)
- [let intermediateCertificate: [String]](/documentation/proximityreader/storeandforwardbatch/intermediatecertificate)
- [let leafCertificate: String](/documentation/proximityreader/storeandforwardbatch/leafcertificate)
- [let payments: [StoreAndForwardBatch.StoredPaymentCardReadResult]](/documentation/proximityreader/storeandforwardbatch/payments)
- [let signature: String](/documentation/proximityreader/storeandforwardbatch/signature)

### Getting the results

- [StoreAndForwardBatch.StoredPaymentCardReadResult](/documentation/proximityreader/storeandforwardbatch/storedpaymentcardreadresult)

#### Instance Properties

- [let generalCardData: String](/documentation/proximityreader/storeandforwardbatch/storedpaymentcardreadresult/generalcarddata)
- [let id: String](/documentation/proximityreader/storeandforwardbatch/storedpaymentcardreadresult/id)
- [let paymentCardData: String](/documentation/proximityreader/storeandforwardbatch/storedpaymentcardreadresult/paymentcarddata)
- [let signature: String](/documentation/proximityreader/storeandforwardbatch/storedpaymentcardreadresult/signature)
- [StoreAndForwardBatchDeletionToken](/documentation/proximityreader/storeandforwardbatchdeletiontoken)

### Creating a token

- [init(rawValue: String)](/documentation/proximityreader/storeandforwardbatchdeletiontoken/init(rawvalue:))

### Getting the token value

- [let rawValue: String](/documentation/proximityreader/storeandforwardbatchdeletiontoken/rawvalue)
- [StoreAndForwardPaymentCardReaderSession](/documentation/proximityreader/storeandforwardpaymentcardreadersession)

### Instance Methods

- [func decline() async throws](/documentation/proximityreader/storeandforwardpaymentcardreadersession/decline())
- [func status() async throws -> StoreAndForwardStatus](/documentation/proximityreader/storeandforwardpaymentcardreadersession/status())
- [StoreAndForwardStatus](/documentation/proximityreader/storeandforwardstatus)

### Getting the status

- [let expiration: Date](/documentation/proximityreader/storeandforwardstatus/expiration)
- [let readCount: Int](/documentation/proximityreader/storeandforwardstatus/readcount)
- [PaymentCardReaderStore](/documentation/proximityreader/paymentcardreaderstore)

### Instance Methods

- [func fetchStoredPaymentCardReadResultBatch(size: Int) async throws -> StoreAndForwardBatch](/documentation/proximityreader/paymentcardreaderstore/fetchstoredpaymentcardreadresultbatch(size:))
- [func fetchStoredPaymentCardReadResultCount() async throws -> Int](/documentation/proximityreader/paymentcardreaderstore/fetchstoredpaymentcardreadresultcount())
- [func resetBatchState() async throws](/documentation/proximityreader/paymentcardreaderstore/resetbatchstate())
- [func resolveBatch(batchDeletionToken: StoreAndForwardBatchDeletionToken) async throws -> Int](/documentation/proximityreader/paymentcardreaderstore/resolvebatch(batchdeletiontoken:))

### Enumerations

- [PaymentCardReaderStore.StoreError](/documentation/proximityreader/paymentcardreaderstore/storeerror)

#### Enumeration Cases

- [case busy](/documentation/proximityreader/paymentcardreaderstore/storeerror/busy)
- [case networkError](/documentation/proximityreader/paymentcardreaderstore/storeerror/networkerror)
- [case notAllowed](/documentation/proximityreader/paymentcardreaderstore/storeerror/notallowed)
- [case passcodeDisabled](/documentation/proximityreader/paymentcardreaderstore/storeerror/passcodedisabled)
- [case storeAndForwardBatchAlreadyExists](/documentation/proximityreader/paymentcardreaderstore/storeerror/storeandforwardbatchalreadyexists)
- [case storeAndForwardBatchNotFound](/documentation/proximityreader/paymentcardreaderstore/storeerror/storeandforwardbatchnotfound)
- [case storeAndForwardBatchSizeInvalid](/documentation/proximityreader/paymentcardreaderstore/storeerror/storeandforwardbatchsizeinvalid)
- [case storeAndForwardDeletionTokenExpired](/documentation/proximityreader/paymentcardreaderstore/storeerror/storeandforwarddeletiontokenexpired)
- [case storeAndForwardDeletionTokenInvalid](/documentation/proximityreader/paymentcardreaderstore/storeerror/storeandforwarddeletiontokeninvalid)
- [case storeAndForwardResultsNotFound](/documentation/proximityreader/paymentcardreaderstore/storeerror/storeandforwardresultsnotfound)
- [case unknown(code: Int)](/documentation/proximityreader/paymentcardreaderstore/storeerror/unknown(code:))

## Loyalty card requests

- [Accepting loyalty passes from Wallet](/documentation/proximityreader/accepting-loyalty-passes-from-wallet)
- [VASRequest](/documentation/proximityreader/vasrequest)

### Creating a loyalty card request

- [init(vasMerchants: [VASRequest.Merchant], localizedVASType: String)](/documentation/proximityreader/vasrequest/init(vasmerchants:localizedvastype:))

### Getting the loyalty card details

- [let localizedVASType: String](/documentation/proximityreader/vasrequest/localizedvastype)
- [let vasMerchants: [VASRequest.Merchant]](/documentation/proximityreader/vasrequest/vasmerchants)
- [VASRequest.Merchant](/documentation/proximityreader/vasrequest/merchant)

#### Creating a merchant structure

- [init(id: String, url: URL?, shouldSendURLOnly: Bool, localizedName: String?)](/documentation/proximityreader/vasrequest/merchant/init(id:url:shouldsendurlonly:localizedname:))

#### Getting the merchant name

- [var localizedName: String](/documentation/proximityreader/vasrequest/merchant/localizedname)

#### Getting the merchant URL details

- [let url: URL?](/documentation/proximityreader/vasrequest/merchant/url)
- [let shouldSendURLOnly: Bool](/documentation/proximityreader/vasrequest/merchant/shouldsendurlonly)

#### Getting the merchant ID

- [let id: String](/documentation/proximityreader/vasrequest/merchant/id)

#### Initializers

- [init(id: String, url: URL?, localizedName: String?)](/documentation/proximityreader/vasrequest/merchant/init(id:url:localizedname:))

### Setting the user interface language

- [var userInterfaceLanguage: Locale.Language?](/documentation/proximityreader/vasrequest/userinterfacelanguage)
- [VASReadResult](/documentation/proximityreader/vasreadresult)

### Creating a read result structure

- [init(id: String, entries: [VASReadResult.ReadEntry])](/documentation/proximityreader/vasreadresult/init(id:entries:))

### Getting the entry details

- [let entries: [VASReadResult.ReadEntry]](/documentation/proximityreader/vasreadresult/entries)
- [VASReadResult.ReadEntry](/documentation/proximityreader/vasreadresult/readentry)

#### Getting the customer data

- [let customerVASData: Data?](/documentation/proximityreader/vasreadresult/readentry/customervasdata)

#### Getting the status word

- [let status: VASReadResult.ReadEntry.Status](/documentation/proximityreader/vasreadresult/readentry/status-swift.property)
- [VASReadResult.ReadEntry.Status](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum)

##### Getting the status

- [case success](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/success)
- [case incorrectData](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/incorrectdata)
- [case unsupportedApplicationVersion](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/unsupportedapplicationversion)
- [case userInterventionRequired](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/userinterventionrequired)
- [case vasDataNotActivated](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/vasdatanotactivated)
- [case vasDataNotFound](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/vasdatanotfound)
- [case wrongCommandLength](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/wrongcommandlength)
- [case wrongP1P2](/documentation/proximityreader/vasreadresult/readentry/status-swift.enum/wrongp1p2)

#### Getting the entry ID

- [let id: String](/documentation/proximityreader/vasreadresult/readentry/id)

### Getting the result ID

- [let id: String](/documentation/proximityreader/vasreadresult/id)

## Merchant discovery

- [ProximityReaderDiscovery](/documentation/proximityreader/proximityreaderdiscovery)

### Creating a discovery object

- [init()](/documentation/proximityreader/proximityreaderdiscovery/init())

### Fetching the content to display

- [func content(for: ProximityReaderDiscovery.Topic) async throws -> ProximityReaderDiscovery.Content](/documentation/proximityreader/proximityreaderdiscovery/content(for:))
- [ProximityReaderDiscovery.Topic](/documentation/proximityreader/proximityreaderdiscovery/topic)

#### Creating a discovery object

- [case payment(ProximityReaderDiscovery.Topic.Payment)](/documentation/proximityreader/proximityreaderdiscovery/topic/payment(_:))
- [ProximityReaderDiscovery.Topic.Payment](/documentation/proximityreader/proximityreaderdiscovery/topic/payment)

##### Enumeration Cases

- [case howToTap](/documentation/proximityreader/proximityreaderdiscovery/topic/payment/howtotap)
- [ProximityReaderDiscovery.Content](/documentation/proximityreader/proximityreaderdiscovery/content)

#### Getting the content identifier

- [let id: String](/documentation/proximityreader/proximityreaderdiscovery/content/id)

#### Getting the content description

- [let description: String](/documentation/proximityreader/proximityreaderdiscovery/content/description)
- [var contentList: [ProximityReaderDiscovery.Content]](/documentation/proximityreader/proximityreaderdiscovery/contentlist)

### Displaying the information

- [func presentContent(ProximityReaderDiscovery.Content, from: UIViewController) async throws](/documentation/proximityreader/proximityreaderdiscovery/presentcontent(_:from:))

### Getting relevant errors

- [ProximityReaderDiscovery.ContentError](/documentation/proximityreader/proximityreaderdiscovery/contenterror)

#### Getting the errors

- [case contentNotFound](/documentation/proximityreader/proximityreaderdiscovery/contenterror/contentnotfound)
- [case contentDisplayFailed](/documentation/proximityreader/proximityreaderdiscovery/contenterror/contentdisplayfailed)
- [case notSupported](/documentation/proximityreader/proximityreaderdiscovery/contenterror/notsupported)
- [case networkUnavailable](/documentation/proximityreader/proximityreaderdiscovery/contenterror/networkunavailable)
- [case systemBusy](/documentation/proximityreader/proximityreaderdiscovery/contenterror/systembusy)
- [case unknown](/documentation/proximityreader/proximityreaderdiscovery/contenterror/unknown)

## Mobile document reader

- [Adopting the Verifier API in your iPhone app](/documentation/proximityreader/adopting-the-verifier-api-in-your-iphone-app)
- [Generating reader tokens for the Verifier API](/documentation/proximityreader/generating-reader-tokens-for-the-verifier-api)
- [Checking IDs with the Verifier API](/documentation/proximityreader/checking-ids-with-the-verifier-api)
- [MobileDocumentReader](/documentation/proximityreader/mobiledocumentreader)

### Creating a mobile document reader

- [init()](/documentation/proximityreader/mobiledocumentreader/init())

### Getting the feature availability

- [static var isSupported: Bool](/documentation/proximityreader/mobiledocumentreader/issupported)

### Preparing the device for reading mobile documents

- [func prepare(using: MobileDocumentReader.Token?) async throws -> MobileDocumentReaderSession](/documentation/proximityreader/mobiledocumentreader/prepare(using:))
- [MobileDocumentReader.Token](/documentation/proximityreader/mobiledocumentreader/token)

#### Initializers

- [init(String)](/documentation/proximityreader/mobiledocumentreader/token/init(_:))

#### Instance Properties

- [let tokenString: String](/documentation/proximityreader/mobiledocumentreader/token/tokenstring)

### Retrieving the reader configuration

- [var configuration: MobileDocumentReader.Configuration](/documentation/proximityreader/mobiledocumentreader/configuration-swift.property)
- [MobileDocumentReader.Configuration](/documentation/proximityreader/mobiledocumentreader/configuration-swift.struct)

#### Instance Properties

- [let readerInstanceIdentifier: String](/documentation/proximityreader/mobiledocumentreader/configuration-swift.struct/readerinstanceidentifier)
- [MobileDocumentReaderSession](/documentation/proximityreader/mobiledocumentreadersession)

### Performing a document request

- [func requestDocument<Request>(Request) async throws -> Request.Response](/documentation/proximityreader/mobiledocumentreadersession/requestdocument(_:))

## Mobile document requests

- [MobileDriversLicenseDisplayRequest](/documentation/proximityreader/mobiledriverslicensedisplayrequest)

### Creating a display request

- [init(elements: [MobileDriversLicenseDisplayRequest.Element], options: MobileDriversLicenseDisplayRequest.Options)](/documentation/proximityreader/mobiledriverslicensedisplayrequest/init(elements:options:))
- [var elements: [MobileDriversLicenseDisplayRequest.Element]](/documentation/proximityreader/mobiledriverslicensedisplayrequest/elements)
- [MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element)

#### Type Properties

- [static let age: MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/age)
- [static let familyName: MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/familyname)
- [static let givenName: MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/givenname)

#### Type Methods

- [static func ageAtLeast(Int) -> MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/ageatleast(_:))

### Configuring a display request

- [var options: MobileDriversLicenseDisplayRequest.Options](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.property)
- [MobileDriversLicenseDisplayRequest.Options](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct)

#### Structures

- [MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct)

##### Type Properties

- [static let check: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct/check)
- [static let checkMultiple: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct/checkmultiple)
- [static let confirm: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct/confirm)

#### Initializers

- [init(validationMode: MobileDriversLicenseDisplayRequest.Options.ValidationMode)](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/init(validationmode:))

#### Instance Properties

- [var validationMode: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.property)

### Handling the response

- [MobileDriversLicenseDisplayRequest.Response](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response)

#### Instance Properties

- [let validationOutcome: MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.property)

#### Enumerations

- [MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum)

##### Enumeration Cases

- [case approved](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/rejected)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledriverslicensedisplayrequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileDriversLicenseDisplayRequest.Response](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response)

##### Instance Properties

- [let validationOutcome: MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.property)

##### Enumerations

- [MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum)

###### Enumeration Cases

- [case approved](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/rejected)
- [MobileDriversLicenseDataRequest](/documentation/proximityreader/mobiledriverslicensedatarequest)

### Creating a data request

- [init(retainedElements: [MobileDriversLicenseDataRequest.Element], nonRetainedElements: [MobileDriversLicenseDataRequest.Element])](/documentation/proximityreader/mobiledriverslicensedatarequest/init(retainedelements:nonretainedelements:))
- [var retainedElements: [MobileDriversLicenseDataRequest.Element]](/documentation/proximityreader/mobiledriverslicensedatarequest/retainedelements)
- [var nonRetainedElements: [MobileDriversLicenseDataRequest.Element]](/documentation/proximityreader/mobiledriverslicensedatarequest/nonretainedelements)
- [MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element)

#### Type Properties

- [static let address: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/address)
- [static let age: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/age)
- [static let dateOfBirth: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/dateofbirth)
- [static let documentDHSComplianceStatus: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentdhscompliancestatus)
- [static let documentExpirationDate: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentexpirationdate)
- [static let documentIssueDate: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentissuedate)
- [static let documentNumber: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentnumber)
- [static let drivingPrivileges: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/drivingprivileges)
- [static let eyeColor: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/eyecolor)
- [static let familyName: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/familyname)
- [static let givenName: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/givenname)
- [static let hairColor: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/haircolor)
- [static let height: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/height)
- [static let issuingAuthority: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/issuingauthority)
- [static let organDonorStatus: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/organdonorstatus)
- [static let portrait: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/portrait)
- [static let sex: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/sex)
- [static let veteranStatus: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/veteranstatus)
- [static let weight: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/weight)

#### Type Methods

- [static func ageAtLeast(Int) -> MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/ageatleast(_:))

### Handling the Response

- [MobileDriversLicenseDataRequest.Response](/documentation/proximityreader/mobiledriverslicensedatarequest/response)

#### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct)

##### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/description)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/issuedate)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/description)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/description)

###### Instance Properties

- [let vehicleClass: MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.property)
- [let vehicleEndorsements: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsements)
- [let vehicleRestrictions: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestrictions)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/code)
- [let sign: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/sign)
- [let value: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/value)

###### Instance Properties

- [let codes: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/codes)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/issuedate)
- [let vehicleCategoryCode: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/vehiclecategorycode)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct)

###### Instance Properties

- [let isoCountryCode: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/isocountrycode)
- [let jurisdiction: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/jurisdiction)
- [let name: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/name)

##### Instance Properties

- [let aamvaDrivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivileges)
- [var address: CNPostalAddress?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/address)
- [let age: Int?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentDHSComplianceStatus: MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentdhscompliancestatus)
- [let documentExpirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentexpirationdate)
- [let documentIssueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentissuedate)
- [let documentNumber: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentnumber)
- [let drivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivileges)
- [let eyeColor: MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.property)
- [let hairColor: MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.property)
- [let height: Measurement<UnitLength>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/height)
- [let isOrganDonor: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isorgandonor)
- [let isVeteran: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isveteran)
- [let issuingAuthority: MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.property)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileDriversLicenseDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.property)
- [let weight: Measurement<UnitMass>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/weight)

##### Enumerations

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus)

###### Enumeration Cases

- [case compliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/compliant)
- [case noncompliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/noncompliant)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum)

###### Enumeration Cases

- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/black)
- [case blue](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/blue)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/brown)
- [case dichromatic](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/dichromatic)
- [case green](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/green)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/grey)
- [case hazel](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/hazel)
- [case maroon](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/maroon)
- [case pink](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/pink)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/unknown)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum)

###### Enumeration Cases

- [case auburn](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/auburn)
- [case bald](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/bald)
- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/black)
- [case blond](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/blond)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/brown)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/grey)
- [case red](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/red)
- [case sandy](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/sandy)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/unknown)
- [case white](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/white)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case notSpecified](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notspecified)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

#### Instance Properties

- [let documentElements: MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.property)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledriverslicensedatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileDriversLicenseDataRequest.Response](/documentation/proximityreader/mobiledriverslicensedatarequest/response)

##### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/description)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/issuedate)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/description)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/description)

###### Instance Properties

- [let vehicleClass: MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.property)
- [let vehicleEndorsements: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsements)
- [let vehicleRestrictions: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestrictions)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/code)
- [let sign: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/sign)
- [let value: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/value)

###### Instance Properties

- [let codes: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/codes)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/issuedate)
- [let vehicleCategoryCode: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/vehiclecategorycode)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct)

###### Instance Properties

- [let isoCountryCode: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/isocountrycode)
- [let jurisdiction: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/jurisdiction)
- [let name: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/name)

###### Instance Properties

- [let aamvaDrivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivileges)
- [var address: CNPostalAddress?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/address)
- [let age: Int?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentDHSComplianceStatus: MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentdhscompliancestatus)
- [let documentExpirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentexpirationdate)
- [let documentIssueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentissuedate)
- [let documentNumber: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentnumber)
- [let drivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivileges)
- [let eyeColor: MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.property)
- [let hairColor: MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.property)
- [let height: Measurement<UnitLength>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/height)
- [let isOrganDonor: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isorgandonor)
- [let isVeteran: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isveteran)
- [let issuingAuthority: MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.property)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileDriversLicenseDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.property)
- [let weight: Measurement<UnitMass>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/weight)

###### Enumerations

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus)

###### Enumeration Cases

- [case compliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/compliant)
- [case noncompliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/noncompliant)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum)

###### Enumeration Cases

- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/black)
- [case blue](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/blue)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/brown)
- [case dichromatic](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/dichromatic)
- [case green](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/green)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/grey)
- [case hazel](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/hazel)
- [case maroon](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/maroon)
- [case pink](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/pink)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/unknown)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum)

###### Enumeration Cases

- [case auburn](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/auburn)
- [case bald](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/bald)
- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/black)
- [case blond](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/blond)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/brown)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/grey)
- [case red](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/red)
- [case sandy](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/sandy)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/unknown)
- [case white](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/white)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case notSpecified](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notspecified)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

##### Instance Properties

- [let documentElements: MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.property)
- [MobileDriversLicenseRawDataRequest](/documentation/proximityreader/mobiledriverslicenserawdatarequest)

### Creating a raw data request

- [init(retainedElements: [MobileDriversLicenseRawDataRequest.Element], nonRetainedElements: [MobileDriversLicenseRawDataRequest.Element])](/documentation/proximityreader/mobiledriverslicenserawdatarequest/init(retainedelements:nonretainedelements:))
- [var retainedElements: [MobileDriversLicenseRawDataRequest.Element]](/documentation/proximityreader/mobiledriverslicenserawdatarequest/retainedelements)
- [var nonRetainedElements: [MobileDriversLicenseRawDataRequest.Element]](/documentation/proximityreader/mobiledriverslicenserawdatarequest/nonretainedelements)
- [MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element)

#### Type Properties

- [static let address: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/address)
- [static let age: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/age)
- [static let dateOfBirth: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/dateofbirth)
- [static let documentDHSComplianceStatus: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentdhscompliancestatus)
- [static let documentExpirationDate: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentexpirationdate)
- [static let documentIssueDate: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentissuedate)
- [static let documentNumber: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentnumber)
- [static let drivingPrivileges: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/drivingprivileges)
- [static let eyeColor: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/eyecolor)
- [static let familyName: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/familyname)
- [static let givenName: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/givenname)
- [static let hairColor: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/haircolor)
- [static let height: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/height)
- [static let issuingAuthority: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/issuingauthority)
- [static let organDonorStatus: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/organdonorstatus)
- [static let portrait: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/portrait)
- [static let sex: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/sex)
- [static let veteranStatus: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/veteranstatus)
- [static let weight: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/weight)

#### Type Methods

- [static func ageAtLeast(Int) -> MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/ageatleast(_:))

### Handling the response

- [MobileDriversLicenseRawDataRequest.Response](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response)

#### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/sessiontranscript)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledriverslicenserawdatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileDriversLicenseRawDataRequest.Response](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response)

##### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/sessiontranscript)
- [MobileNationalIDCardDisplayRequest](/documentation/proximityreader/mobilenationalidcarddisplayrequest)

### Creating a display request

- [init(region: Locale.Region, elements: [MobileNationalIDCardDisplayRequest.Element], options: MobileNationalIDCardDisplayRequest.Options)](/documentation/proximityreader/mobilenationalidcarddisplayrequest/init(region:elements:options:))

### Determining the region availability

- [static func isSupportedRegion(Locale.Region) -> Bool](/documentation/proximityreader/mobilenationalidcarddisplayrequest/issupportedregion(_:))

### Configuring the request details

- [var region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddisplayrequest/region)
- [var elements: [MobileNationalIDCardDisplayRequest.Element]](/documentation/proximityreader/mobilenationalidcarddisplayrequest/elements)
- [MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element)

#### Type Properties

- [static let age: MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/age)
- [static let familyName: MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/familyname)
- [static let givenName: MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/givenname)

#### Type Methods

- [static func ageAtLeast(Int) -> MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/ageatleast(_:))
- [var options: MobileNationalIDCardDisplayRequest.Options](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.property)
- [MobileNationalIDCardDisplayRequest.Options](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct)

#### Structures

- [MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct)

##### Type Properties

- [static let check: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct/check)
- [static let checkMultiple: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct/checkmultiple)
- [static let confirm: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct/confirm)

#### Initializers

- [init(validationMode: MobileNationalIDCardDisplayRequest.Options.ValidationMode)](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/init(validationmode:))

#### Instance Properties

- [var validationMode: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.property)

### Handling the response

- [MobileNationalIDCardDisplayRequest.Response](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response)

#### Instance Properties

- [let validationOutcome: MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.property)

#### Enumerations

- [MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum)

##### Enumeration Cases

- [case approved](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/rejected)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilenationalidcarddisplayrequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileNationalIDCardDisplayRequest.Response](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response)

##### Instance Properties

- [let validationOutcome: MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.property)

##### Enumerations

- [MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum)

###### Enumeration Cases

- [case approved](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/rejected)
- [MobileNationalIDCardDataRequest](/documentation/proximityreader/mobilenationalidcarddatarequest)

### Creating a data request

- [init(region: Locale.Region, retainedElements: [MobileNationalIDCardDataRequest.Element], nonRetainedElements: [MobileNationalIDCardDataRequest.Element])](/documentation/proximityreader/mobilenationalidcarddatarequest/init(region:retainedelements:nonretainedelements:))

### Determining the region availability

- [static func isSupportedRegion(Locale.Region) -> Bool](/documentation/proximityreader/mobilenationalidcarddatarequest/issupportedregion(_:))

### Configuring the request details

- [var region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddatarequest/region)
- [var retainedElements: [MobileNationalIDCardDataRequest.Element]](/documentation/proximityreader/mobilenationalidcarddatarequest/retainedelements)
- [var nonRetainedElements: [MobileNationalIDCardDataRequest.Element]](/documentation/proximityreader/mobilenationalidcarddatarequest/nonretainedelements)
- [MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element)

#### Type Properties

- [static let age: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/age)
- [static let dateOfBirth: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/dateofbirth)
- [static let documentNumber: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/documentnumber)
- [static let familyName: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/familyname)
- [static let givenName: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/givenname)
- [static let portrait: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/portrait)
- [static let sex: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/sex)

#### Type Methods

- [static func ageAtLeast(Int) -> MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/ageatleast(_:))

### Handling the Response

- [MobileNationalIDCardDataRequest.Response](/documentation/proximityreader/mobilenationalidcarddatarequest/response)

#### Structures

- [MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct)

##### Instance Properties

- [let age: Int?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentNumber: String?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/documentnumber)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileNationalIDCardDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.property)

##### Enumerations

- [MobileNationalIDCardDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case unknown](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

#### Instance Properties

- [let documentElements: MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.property)
- [let region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddatarequest/response/region)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilenationalidcarddatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileNationalIDCardDataRequest.Response](/documentation/proximityreader/mobilenationalidcarddatarequest/response)

##### Structures

- [MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct)

###### Instance Properties

- [let age: Int?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentNumber: String?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/documentnumber)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileNationalIDCardDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.property)

###### Enumerations

- [MobileNationalIDCardDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case unknown](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

##### Instance Properties

- [let documentElements: MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.property)
- [let region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddatarequest/response/region)
- [MobileNationalIDCardRawDataRequest](/documentation/proximityreader/mobilenationalidcardrawdatarequest)

### Creating a raw data request

- [init(region: Locale.Region, retainedElements: [MobileNationalIDCardRawDataRequest.Element], nonRetainedElements: [MobileNationalIDCardRawDataRequest.Element])](/documentation/proximityreader/mobilenationalidcardrawdatarequest/init(region:retainedelements:nonretainedelements:))

### Determining the region availability

- [static func isSupportedRegion(Locale.Region) -> Bool](/documentation/proximityreader/mobilenationalidcardrawdatarequest/issupportedregion(_:))

### Configuring the request details

- [var region: Locale.Region](/documentation/proximityreader/mobilenationalidcardrawdatarequest/region)
- [var retainedElements: [MobileNationalIDCardRawDataRequest.Element]](/documentation/proximityreader/mobilenationalidcardrawdatarequest/retainedelements)
- [var nonRetainedElements: [MobileNationalIDCardRawDataRequest.Element]](/documentation/proximityreader/mobilenationalidcardrawdatarequest/nonretainedelements)
- [MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element)

#### Type Properties

- [static let address: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/address)
- [static let age: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/age)
- [static let dateOfBirth: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/dateofbirth)
- [static let documentNumber: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/documentnumber)
- [static let familyName: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/familyname)
- [static let givenName: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/givenname)
- [static let portrait: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/portrait)
- [static let sex: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/sex)

#### Type Methods

- [static func ageAtLeast(Int) -> MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/ageatleast(_:))

### Handling the response

- [MobileNationalIDCardRawDataRequest.Response](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response)

#### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/sessiontranscript)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilenationalidcardrawdatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileNationalIDCardRawDataRequest.Response](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response)

##### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/sessiontranscript)
- [MobileDocumentDisplayRequest](/documentation/proximityreader/mobiledocumentdisplayrequest)

### Creating a display request

- [init(elements: [MobileDocumentDisplayRequest.Element], options: MobileDocumentDisplayRequest.Options)](/documentation/proximityreader/mobiledocumentdisplayrequest/init(elements:options:))
- [MobileDocumentDisplayRequest.Element](/documentation/proximityreader/mobiledocumentdisplayrequest/element)

#### Type Properties

- [static let age: MobileDocumentDisplayRequest.Element](/documentation/proximityreader/mobiledocumentdisplayrequest/element/age)
- [static let familyName: MobileDocumentDisplayRequest.Element](/documentation/proximityreader/mobiledocumentdisplayrequest/element/familyname)
- [static let givenName: MobileDocumentDisplayRequest.Element](/documentation/proximityreader/mobiledocumentdisplayrequest/element/givenname)

#### Type Methods

- [static func ageAtLeast(Int) -> MobileDocumentDisplayRequest.Element](/documentation/proximityreader/mobiledocumentdisplayrequest/element/ageatleast(_:))

### Configuring a display request

- [MobileDocumentDisplayRequest.Options](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct)

#### Structures

- [MobileDocumentDisplayRequest.Options.DocumentType](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/documenttype)

##### Type Properties

- [static let driversLicense: MobileDocumentDisplayRequest.Options.DocumentType](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/documenttype/driverslicense)
- [static let photoID: MobileDocumentDisplayRequest.Options.DocumentType](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/documenttype/photoid)

##### Type Methods

- [static func nationalIDCard(region: Locale.Region) -> MobileDocumentDisplayRequest.Options.DocumentType](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/documenttype/nationalidcard(region:))
- [MobileDocumentDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/validationmode-swift.struct)

##### Type Properties

- [static let check: MobileDocumentDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/validationmode-swift.struct/check)
- [static let checkMultiple: MobileDocumentDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/validationmode-swift.struct/checkmultiple)
- [static let confirm: MobileDocumentDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/validationmode-swift.struct/confirm)

#### Initializers

- [init(allowedDocumentTypes: [MobileDocumentDisplayRequest.Options.DocumentType], validationMode: MobileDocumentDisplayRequest.Options.ValidationMode)](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/init(alloweddocumenttypes:validationmode:))

#### Instance Properties

- [var allowedDocumentTypes: [MobileDocumentDisplayRequest.Options.DocumentType]](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/alloweddocumenttypes)
- [var validationMode: MobileDocumentDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.struct/validationmode-swift.property)
- [var options: MobileDocumentDisplayRequest.Options](/documentation/proximityreader/mobiledocumentdisplayrequest/options-swift.property)

### Handling the response

- [MobileDocumentDisplayRequest.Response](/documentation/proximityreader/mobiledocumentdisplayrequest/response)

#### Getting the response

- [let validationOutcome: MobileDocumentDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.property)
- [MobileDocumentDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum)

##### Enumeration Cases

- [case approved](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum/rejected)

### Instance Properties

- [var elements: [MobileDocumentDisplayRequest.Element]](/documentation/proximityreader/mobiledocumentdisplayrequest/elements)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledocumentdisplayrequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileDocumentDisplayRequest.Response](/documentation/proximityreader/mobiledocumentdisplayrequest/response)

##### Getting the response

- [let validationOutcome: MobileDocumentDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.property)
- [MobileDocumentDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum)

###### Enumeration Cases

- [case approved](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobiledocumentdisplayrequest/response/validationoutcome-swift.enum/rejected)
- [MobileDocumentRequest](/documentation/proximityreader/mobiledocumentrequest)

### Mobile driver’s license display request

- [MobileDriversLicenseDisplayRequest](/documentation/proximityreader/mobiledriverslicensedisplayrequest)

#### Creating a display request

- [init(elements: [MobileDriversLicenseDisplayRequest.Element], options: MobileDriversLicenseDisplayRequest.Options)](/documentation/proximityreader/mobiledriverslicensedisplayrequest/init(elements:options:))
- [var elements: [MobileDriversLicenseDisplayRequest.Element]](/documentation/proximityreader/mobiledriverslicensedisplayrequest/elements)
- [MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element)

##### Type Properties

- [static let age: MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/age)
- [static let familyName: MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/familyname)
- [static let givenName: MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/givenname)

##### Type Methods

- [static func ageAtLeast(Int) -> MobileDriversLicenseDisplayRequest.Element](/documentation/proximityreader/mobiledriverslicensedisplayrequest/element/ageatleast(_:))

#### Configuring a display request

- [var options: MobileDriversLicenseDisplayRequest.Options](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.property)
- [MobileDriversLicenseDisplayRequest.Options](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct)

##### Structures

- [MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct)

###### Type Properties

- [static let check: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct/check)
- [static let checkMultiple: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct/checkmultiple)
- [static let confirm: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.struct/confirm)

##### Initializers

- [init(validationMode: MobileDriversLicenseDisplayRequest.Options.ValidationMode)](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/init(validationmode:))

##### Instance Properties

- [var validationMode: MobileDriversLicenseDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobiledriverslicensedisplayrequest/options-swift.struct/validationmode-swift.property)

#### Handling the response

- [MobileDriversLicenseDisplayRequest.Response](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response)

##### Instance Properties

- [let validationOutcome: MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.property)

##### Enumerations

- [MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum)

###### Enumeration Cases

- [case approved](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/rejected)

#### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledriverslicensedisplayrequest/mobiledocumentrequest-implementations)

##### Structures

- [MobileDriversLicenseDisplayRequest.Response](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response)

###### Instance Properties

- [let validationOutcome: MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.property)

###### Enumerations

- [MobileDriversLicenseDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum)

###### Enumeration Cases

- [case approved](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobiledriverslicensedisplayrequest/response/validationoutcome-swift.enum/rejected)
- [static func displayDriversLicense([MobileDriversLicenseDisplayRequest.Element], options: MobileDriversLicenseDisplayRequest.Options) -> Self](/documentation/proximityreader/mobiledocumentrequest/displaydriverslicense(_:options:))

### Mobile driver’s license data request

- [MobileDriversLicenseDataRequest](/documentation/proximityreader/mobiledriverslicensedatarequest)

#### Creating a data request

- [init(retainedElements: [MobileDriversLicenseDataRequest.Element], nonRetainedElements: [MobileDriversLicenseDataRequest.Element])](/documentation/proximityreader/mobiledriverslicensedatarequest/init(retainedelements:nonretainedelements:))
- [var retainedElements: [MobileDriversLicenseDataRequest.Element]](/documentation/proximityreader/mobiledriverslicensedatarequest/retainedelements)
- [var nonRetainedElements: [MobileDriversLicenseDataRequest.Element]](/documentation/proximityreader/mobiledriverslicensedatarequest/nonretainedelements)
- [MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element)

##### Type Properties

- [static let address: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/address)
- [static let age: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/age)
- [static let dateOfBirth: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/dateofbirth)
- [static let documentDHSComplianceStatus: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentdhscompliancestatus)
- [static let documentExpirationDate: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentexpirationdate)
- [static let documentIssueDate: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentissuedate)
- [static let documentNumber: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/documentnumber)
- [static let drivingPrivileges: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/drivingprivileges)
- [static let eyeColor: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/eyecolor)
- [static let familyName: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/familyname)
- [static let givenName: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/givenname)
- [static let hairColor: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/haircolor)
- [static let height: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/height)
- [static let issuingAuthority: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/issuingauthority)
- [static let organDonorStatus: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/organdonorstatus)
- [static let portrait: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/portrait)
- [static let sex: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/sex)
- [static let veteranStatus: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/veteranstatus)
- [static let weight: MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/weight)

##### Type Methods

- [static func ageAtLeast(Int) -> MobileDriversLicenseDataRequest.Element](/documentation/proximityreader/mobiledriverslicensedatarequest/element/ageatleast(_:))

#### Handling the Response

- [MobileDriversLicenseDataRequest.Response](/documentation/proximityreader/mobiledriverslicensedatarequest/response)

##### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/description)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/issuedate)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/description)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/description)

###### Instance Properties

- [let vehicleClass: MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.property)
- [let vehicleEndorsements: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsements)
- [let vehicleRestrictions: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestrictions)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/code)
- [let sign: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/sign)
- [let value: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/value)

###### Instance Properties

- [let codes: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/codes)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/issuedate)
- [let vehicleCategoryCode: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/vehiclecategorycode)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct)

###### Instance Properties

- [let isoCountryCode: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/isocountrycode)
- [let jurisdiction: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/jurisdiction)
- [let name: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/name)

###### Instance Properties

- [let aamvaDrivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivileges)
- [var address: CNPostalAddress?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/address)
- [let age: Int?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentDHSComplianceStatus: MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentdhscompliancestatus)
- [let documentExpirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentexpirationdate)
- [let documentIssueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentissuedate)
- [let documentNumber: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentnumber)
- [let drivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivileges)
- [let eyeColor: MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.property)
- [let hairColor: MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.property)
- [let height: Measurement<UnitLength>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/height)
- [let isOrganDonor: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isorgandonor)
- [let isVeteran: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isveteran)
- [let issuingAuthority: MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.property)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileDriversLicenseDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.property)
- [let weight: Measurement<UnitMass>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/weight)

###### Enumerations

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus)

###### Enumeration Cases

- [case compliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/compliant)
- [case noncompliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/noncompliant)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum)

###### Enumeration Cases

- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/black)
- [case blue](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/blue)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/brown)
- [case dichromatic](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/dichromatic)
- [case green](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/green)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/grey)
- [case hazel](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/hazel)
- [case maroon](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/maroon)
- [case pink](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/pink)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/unknown)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum)

###### Enumeration Cases

- [case auburn](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/auburn)
- [case bald](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/bald)
- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/black)
- [case blond](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/blond)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/brown)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/grey)
- [case red](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/red)
- [case sandy](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/sandy)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/unknown)
- [case white](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/white)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case notSpecified](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notspecified)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

##### Instance Properties

- [let documentElements: MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.property)

#### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledriverslicensedatarequest/mobiledocumentrequest-implementations)

##### Structures

- [MobileDriversLicenseDataRequest.Response](/documentation/proximityreader/mobiledriverslicensedatarequest/response)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/description)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.struct/issuedate)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsement/description)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction)

###### Instance Properties

- [let code: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/code)
- [let description: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestriction/description)

###### Instance Properties

- [let vehicleClass: MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleClass?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleclass-swift.property)
- [let vehicleEndorsements: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleEndorsement]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehicleendorsements)
- [let vehicleRestrictions: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege.VehicleRestriction]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivilege/vehiclerestrictions)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege)

###### Structures

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code)

###### Instance Properties

- [let code: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/code)
- [let sign: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/sign)
- [let value: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/code/value)

###### Instance Properties

- [let codes: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege.Code]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/codes)
- [let expirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/expirationdate)
- [let issueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/issuedate)
- [let vehicleCategoryCode: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivilege/vehiclecategorycode)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct)

###### Instance Properties

- [let isoCountryCode: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/isocountrycode)
- [let jurisdiction: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/jurisdiction)
- [let name: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/name)

###### Instance Properties

- [let aamvaDrivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.AAMVADrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/aamvadrivingprivileges)
- [var address: CNPostalAddress?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/address)
- [let age: Int?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentDHSComplianceStatus: MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentdhscompliancestatus)
- [let documentExpirationDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentexpirationdate)
- [let documentIssueDate: DateComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentissuedate)
- [let documentNumber: String?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/documentnumber)
- [let drivingPrivileges: [MobileDriversLicenseDataRequest.Response.DocumentElements.DrivingPrivilege]](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/drivingprivileges)
- [let eyeColor: MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.property)
- [let hairColor: MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.property)
- [let height: Measurement<UnitLength>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/height)
- [let isOrganDonor: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isorgandonor)
- [let isVeteran: Bool?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/isveteran)
- [let issuingAuthority: MobileDriversLicenseDataRequest.Response.DocumentElements.IssuingAuthority?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/issuingauthority-swift.property)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileDriversLicenseDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.property)
- [let weight: Measurement<UnitMass>?](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/weight)

###### Enumerations

- [MobileDriversLicenseDataRequest.Response.DocumentElements.DHSComplianceStatus](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus)

###### Enumeration Cases

- [case compliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/compliant)
- [case noncompliant](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/dhscompliancestatus/noncompliant)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.EyeColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum)

###### Enumeration Cases

- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/black)
- [case blue](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/blue)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/brown)
- [case dichromatic](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/dichromatic)
- [case green](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/green)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/grey)
- [case hazel](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/hazel)
- [case maroon](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/maroon)
- [case pink](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/pink)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/eyecolor-swift.enum/unknown)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.HairColor](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum)

###### Enumeration Cases

- [case auburn](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/auburn)
- [case bald](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/bald)
- [case black](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/black)
- [case blond](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/blond)
- [case brown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/brown)
- [case grey](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/grey)
- [case red](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/red)
- [case sandy](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/sandy)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/unknown)
- [case white](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/haircolor-swift.enum/white)
- [MobileDriversLicenseDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case notSpecified](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/notspecified)
- [case unknown](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

###### Instance Properties

- [let documentElements: MobileDriversLicenseDataRequest.Response.DocumentElements](/documentation/proximityreader/mobiledriverslicensedatarequest/response/documentelements-swift.property)
- [static func driversLicenseData(retaining: [MobileDriversLicenseDataRequest.Element], notRetaining: [MobileDriversLicenseDataRequest.Element]) -> Self](/documentation/proximityreader/mobiledocumentrequest/driverslicensedata(retaining:notretaining:))

### Mobile driver’s license raw data request

- [MobileDriversLicenseRawDataRequest](/documentation/proximityreader/mobiledriverslicenserawdatarequest)

#### Creating a raw data request

- [init(retainedElements: [MobileDriversLicenseRawDataRequest.Element], nonRetainedElements: [MobileDriversLicenseRawDataRequest.Element])](/documentation/proximityreader/mobiledriverslicenserawdatarequest/init(retainedelements:nonretainedelements:))
- [var retainedElements: [MobileDriversLicenseRawDataRequest.Element]](/documentation/proximityreader/mobiledriverslicenserawdatarequest/retainedelements)
- [var nonRetainedElements: [MobileDriversLicenseRawDataRequest.Element]](/documentation/proximityreader/mobiledriverslicenserawdatarequest/nonretainedelements)
- [MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element)

##### Type Properties

- [static let address: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/address)
- [static let age: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/age)
- [static let dateOfBirth: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/dateofbirth)
- [static let documentDHSComplianceStatus: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentdhscompliancestatus)
- [static let documentExpirationDate: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentexpirationdate)
- [static let documentIssueDate: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentissuedate)
- [static let documentNumber: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/documentnumber)
- [static let drivingPrivileges: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/drivingprivileges)
- [static let eyeColor: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/eyecolor)
- [static let familyName: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/familyname)
- [static let givenName: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/givenname)
- [static let hairColor: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/haircolor)
- [static let height: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/height)
- [static let issuingAuthority: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/issuingauthority)
- [static let organDonorStatus: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/organdonorstatus)
- [static let portrait: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/portrait)
- [static let sex: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/sex)
- [static let veteranStatus: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/veteranstatus)
- [static let weight: MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/weight)

##### Type Methods

- [static func ageAtLeast(Int) -> MobileDriversLicenseRawDataRequest.Element](/documentation/proximityreader/mobiledriverslicenserawdatarequest/element/ageatleast(_:))

#### Handling the response

- [MobileDriversLicenseRawDataRequest.Response](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response)

##### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/sessiontranscript)

#### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledriverslicenserawdatarequest/mobiledocumentrequest-implementations)

##### Structures

- [MobileDriversLicenseRawDataRequest.Response](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response)

###### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobiledriverslicenserawdatarequest/response/sessiontranscript)
- [static func driversLicenseRawData(retaining: [MobileDriversLicenseRawDataRequest.Element], notRetaining: [MobileDriversLicenseRawDataRequest.Element]) -> Self](/documentation/proximityreader/mobiledocumentrequest/driverslicenserawdata(retaining:notretaining:))

### National ID card display request

- [MobileNationalIDCardDisplayRequest](/documentation/proximityreader/mobilenationalidcarddisplayrequest)

#### Creating a display request

- [init(region: Locale.Region, elements: [MobileNationalIDCardDisplayRequest.Element], options: MobileNationalIDCardDisplayRequest.Options)](/documentation/proximityreader/mobilenationalidcarddisplayrequest/init(region:elements:options:))

#### Determining the region availability

- [static func isSupportedRegion(Locale.Region) -> Bool](/documentation/proximityreader/mobilenationalidcarddisplayrequest/issupportedregion(_:))

#### Configuring the request details

- [var region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddisplayrequest/region)
- [var elements: [MobileNationalIDCardDisplayRequest.Element]](/documentation/proximityreader/mobilenationalidcarddisplayrequest/elements)
- [MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element)

##### Type Properties

- [static let age: MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/age)
- [static let familyName: MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/familyname)
- [static let givenName: MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/givenname)

##### Type Methods

- [static func ageAtLeast(Int) -> MobileNationalIDCardDisplayRequest.Element](/documentation/proximityreader/mobilenationalidcarddisplayrequest/element/ageatleast(_:))
- [var options: MobileNationalIDCardDisplayRequest.Options](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.property)
- [MobileNationalIDCardDisplayRequest.Options](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct)

##### Structures

- [MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct)

###### Type Properties

- [static let check: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct/check)
- [static let checkMultiple: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct/checkmultiple)
- [static let confirm: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.struct/confirm)

##### Initializers

- [init(validationMode: MobileNationalIDCardDisplayRequest.Options.ValidationMode)](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/init(validationmode:))

##### Instance Properties

- [var validationMode: MobileNationalIDCardDisplayRequest.Options.ValidationMode](/documentation/proximityreader/mobilenationalidcarddisplayrequest/options-swift.struct/validationmode-swift.property)

#### Handling the response

- [MobileNationalIDCardDisplayRequest.Response](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response)

##### Instance Properties

- [let validationOutcome: MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.property)

##### Enumerations

- [MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum)

###### Enumeration Cases

- [case approved](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/rejected)

#### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilenationalidcarddisplayrequest/mobiledocumentrequest-implementations)

##### Structures

- [MobileNationalIDCardDisplayRequest.Response](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response)

###### Instance Properties

- [let validationOutcome: MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.property)

###### Enumerations

- [MobileNationalIDCardDisplayRequest.Response.ValidationOutcome](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum)

###### Enumeration Cases

- [case approved](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/approved)
- [case dismissed](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/dismissed)
- [case rejected](/documentation/proximityreader/mobilenationalidcarddisplayrequest/response/validationoutcome-swift.enum/rejected)
- [static func nationalIDCard(region: Locale.Region, [MobileNationalIDCardDisplayRequest.Element], options: MobileNationalIDCardDisplayRequest.Options) -> Self](/documentation/proximityreader/mobiledocumentrequest/nationalidcard(region:_:options:))

### National ID card license data request

- [MobileNationalIDCardDataRequest](/documentation/proximityreader/mobilenationalidcarddatarequest)

#### Creating a data request

- [init(region: Locale.Region, retainedElements: [MobileNationalIDCardDataRequest.Element], nonRetainedElements: [MobileNationalIDCardDataRequest.Element])](/documentation/proximityreader/mobilenationalidcarddatarequest/init(region:retainedelements:nonretainedelements:))

#### Determining the region availability

- [static func isSupportedRegion(Locale.Region) -> Bool](/documentation/proximityreader/mobilenationalidcarddatarequest/issupportedregion(_:))

#### Configuring the request details

- [var region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddatarequest/region)
- [var retainedElements: [MobileNationalIDCardDataRequest.Element]](/documentation/proximityreader/mobilenationalidcarddatarequest/retainedelements)
- [var nonRetainedElements: [MobileNationalIDCardDataRequest.Element]](/documentation/proximityreader/mobilenationalidcarddatarequest/nonretainedelements)
- [MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element)

##### Type Properties

- [static let age: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/age)
- [static let dateOfBirth: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/dateofbirth)
- [static let documentNumber: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/documentnumber)
- [static let familyName: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/familyname)
- [static let givenName: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/givenname)
- [static let portrait: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/portrait)
- [static let sex: MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/sex)

##### Type Methods

- [static func ageAtLeast(Int) -> MobileNationalIDCardDataRequest.Element](/documentation/proximityreader/mobilenationalidcarddatarequest/element/ageatleast(_:))

#### Handling the Response

- [MobileNationalIDCardDataRequest.Response](/documentation/proximityreader/mobilenationalidcarddatarequest/response)

##### Structures

- [MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct)

###### Instance Properties

- [let age: Int?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentNumber: String?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/documentnumber)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileNationalIDCardDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.property)

###### Enumerations

- [MobileNationalIDCardDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case unknown](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

##### Instance Properties

- [let documentElements: MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.property)
- [let region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddatarequest/response/region)

#### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilenationalidcarddatarequest/mobiledocumentrequest-implementations)

##### Structures

- [MobileNationalIDCardDataRequest.Response](/documentation/proximityreader/mobilenationalidcarddatarequest/response)

###### Structures

- [MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct)

###### Instance Properties

- [let age: Int?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentNumber: String?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/documentnumber)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobileNationalIDCardDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.property)

###### Enumerations

- [MobileNationalIDCardDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case unknown](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

###### Instance Properties

- [let documentElements: MobileNationalIDCardDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilenationalidcarddatarequest/response/documentelements-swift.property)
- [let region: Locale.Region](/documentation/proximityreader/mobilenationalidcarddatarequest/response/region)
- [static func nationalIDCardData(region: Locale.Region, retaining: [MobileNationalIDCardDataRequest.Element], notRetaining: [MobileNationalIDCardDataRequest.Element]) -> Self](/documentation/proximityreader/mobiledocumentrequest/nationalidcarddata(region:retaining:notretaining:))

### National ID card license raw data request

- [MobileNationalIDCardRawDataRequest](/documentation/proximityreader/mobilenationalidcardrawdatarequest)

#### Creating a raw data request

- [init(region: Locale.Region, retainedElements: [MobileNationalIDCardRawDataRequest.Element], nonRetainedElements: [MobileNationalIDCardRawDataRequest.Element])](/documentation/proximityreader/mobilenationalidcardrawdatarequest/init(region:retainedelements:nonretainedelements:))

#### Determining the region availability

- [static func isSupportedRegion(Locale.Region) -> Bool](/documentation/proximityreader/mobilenationalidcardrawdatarequest/issupportedregion(_:))

#### Configuring the request details

- [var region: Locale.Region](/documentation/proximityreader/mobilenationalidcardrawdatarequest/region)
- [var retainedElements: [MobileNationalIDCardRawDataRequest.Element]](/documentation/proximityreader/mobilenationalidcardrawdatarequest/retainedelements)
- [var nonRetainedElements: [MobileNationalIDCardRawDataRequest.Element]](/documentation/proximityreader/mobilenationalidcardrawdatarequest/nonretainedelements)
- [MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element)

##### Type Properties

- [static let address: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/address)
- [static let age: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/age)
- [static let dateOfBirth: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/dateofbirth)
- [static let documentNumber: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/documentnumber)
- [static let familyName: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/familyname)
- [static let givenName: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/givenname)
- [static let portrait: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/portrait)
- [static let sex: MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/sex)

##### Type Methods

- [static func ageAtLeast(Int) -> MobileNationalIDCardRawDataRequest.Element](/documentation/proximityreader/mobilenationalidcardrawdatarequest/element/ageatleast(_:))

#### Handling the response

- [MobileNationalIDCardRawDataRequest.Response](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response)

##### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/sessiontranscript)

#### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilenationalidcardrawdatarequest/mobiledocumentrequest-implementations)

##### Structures

- [MobileNationalIDCardRawDataRequest.Response](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response)

###### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobilenationalidcardrawdatarequest/response/sessiontranscript)
- [static func nationalIDCardRawData(region: Locale.Region, retaining: [MobileNationalIDCardRawDataRequest.Element], notRetaining: [MobileNationalIDCardRawDataRequest.Element]) -> Self](/documentation/proximityreader/mobiledocumentrequest/nationalidcardrawdata(region:retaining:notretaining:))

### Associated Types

- [Response](/documentation/proximityreader/mobiledocumentrequest/response)

### Type Methods

- [static func displayDocument([MobileDocumentDisplayRequest.Element], options: MobileDocumentDisplayRequest.Options) -> Self](/documentation/proximityreader/mobiledocumentrequest/displaydocument(_:options:))
- [static func photoIDData(retaining: [MobilePhotoIDDataRequest.Element], notRetaining: [MobilePhotoIDDataRequest.Element]) -> Self](/documentation/proximityreader/mobiledocumentrequest/photoiddata(retaining:notretaining:))
- [static func photoIDRawData(retaining: [MobilePhotoIDRawDataRequest.Element], notRetaining: [MobilePhotoIDRawDataRequest.Element]) -> Self](/documentation/proximityreader/mobiledocumentrequest/photoidrawdata(retaining:notretaining:))
- [MobileDocumentDataRequest](/documentation/proximityreader/mobiledocumentdatarequest)

### Handling the response

- [MobileDocumentDataResponse](/documentation/proximityreader/mobiledocumentdataresponse)
- [MobileDocumentRawDataRequest](/documentation/proximityreader/mobiledocumentrawdatarequest)
- [MobilePhotoIDDataRequest](/documentation/proximityreader/mobilephotoiddatarequest)

### Creating a data request

- [init(retainedElements: [MobilePhotoIDDataRequest.Element], nonRetainedElements: [MobilePhotoIDDataRequest.Element])](/documentation/proximityreader/mobilephotoiddatarequest/init(retainedelements:nonretainedelements:))
- [MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element)

#### Type Properties

- [static let address: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/address)
- [static let age: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/age)
- [static let dateOfBirth: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/dateofbirth)
- [static let documentExpirationDate: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/documentexpirationdate)
- [static let documentIssueDate: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/documentissuedate)
- [static let documentNumber: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/documentnumber)
- [static let familyName: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/familyname)
- [static let givenName: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/givenname)
- [static let issuingAuthority: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/issuingauthority)
- [static let portrait: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/portrait)
- [static let sex: MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/sex)

#### Type Methods

- [static func ageAtLeast(Int) -> MobilePhotoIDDataRequest.Element](/documentation/proximityreader/mobilephotoiddatarequest/element/ageatleast(_:))
- [var nonRetainedElements: [MobilePhotoIDDataRequest.Element]](/documentation/proximityreader/mobilephotoiddatarequest/nonretainedelements)
- [var retainedElements: [MobilePhotoIDDataRequest.Element]](/documentation/proximityreader/mobilephotoiddatarequest/retainedelements)

### Handling the response

- [MobilePhotoIDDataRequest.Response](/documentation/proximityreader/mobilephotoiddatarequest/response)

#### Structures

- [MobilePhotoIDDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct)

##### Structures

- [MobilePhotoIDDataRequest.Response.DocumentElements.IssuingAuthority](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct)

###### Instance Properties

- [let isoCountryCode: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/isocountrycode)
- [let jurisdiction: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/jurisdiction)
- [let name: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/name)

##### Instance Properties

- [var address: CNPostalAddress?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/address)
- [let age: Int?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentExpirationDate: DateComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/documentexpirationdate)
- [let documentIssueDate: DateComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/documentissuedate)
- [let documentNumber: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/documentnumber)
- [let issuingAuthority: MobilePhotoIDDataRequest.Response.DocumentElements.IssuingAuthority?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.property)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobilePhotoIDDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.property)

##### Enumerations

- [MobilePhotoIDDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case unknown](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

#### Instance Properties

- [let documentElements: MobilePhotoIDDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.property)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilephotoiddatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobilePhotoIDDataRequest.Response](/documentation/proximityreader/mobilephotoiddatarequest/response)

##### Structures

- [MobilePhotoIDDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct)

###### Structures

- [MobilePhotoIDDataRequest.Response.DocumentElements.IssuingAuthority](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct)

###### Instance Properties

- [let isoCountryCode: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/isocountrycode)
- [let jurisdiction: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/jurisdiction)
- [let name: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.struct/name)

###### Instance Properties

- [var address: CNPostalAddress?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/address)
- [let age: Int?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/age)
- [let ageAtLeastElements: [Int : Bool]](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/ageatleastelements)
- [let dateOfBirth: DateComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/dateofbirth)
- [let documentExpirationDate: DateComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/documentexpirationdate)
- [let documentIssueDate: DateComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/documentissuedate)
- [let documentNumber: String?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/documentnumber)
- [let issuingAuthority: MobilePhotoIDDataRequest.Response.DocumentElements.IssuingAuthority?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/issuingauthority-swift.property)
- [let nameComponents: PersonNameComponents?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/namecomponents)
- [let portraitData: Data?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/portraitdata)
- [let sex: MobilePhotoIDDataRequest.Response.DocumentElements.Sex?](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.property)

###### Enumerations

- [MobilePhotoIDDataRequest.Response.DocumentElements.Sex](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum)

###### Enumeration Cases

- [case female](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/female)
- [case male](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/male)
- [case notApplicable](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/notapplicable)
- [case unknown](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/unknown)

###### Instance Properties

- [var localizedName: String](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.struct/sex-swift.enum/localizedname)

##### Instance Properties

- [let documentElements: MobilePhotoIDDataRequest.Response.DocumentElements](/documentation/proximityreader/mobilephotoiddatarequest/response/documentelements-swift.property)
- [MobilePhotoIDRawDataRequest](/documentation/proximityreader/mobilephotoidrawdatarequest)

### Creating a raw data request

- [init(retainedElements: [MobilePhotoIDRawDataRequest.Element], nonRetainedElements: [MobilePhotoIDRawDataRequest.Element])](/documentation/proximityreader/mobilephotoidrawdatarequest/init(retainedelements:nonretainedelements:))
- [MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element)

#### Type Properties

- [static let address: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/address)
- [static let age: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/age)
- [static let dateOfBirth: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/dateofbirth)
- [static let documentExpirationDate: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/documentexpirationdate)
- [static let documentIssueDate: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/documentissuedate)
- [static let documentNumber: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/documentnumber)
- [static let familyName: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/familyname)
- [static let givenName: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/givenname)
- [static let issuingAuthority: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/issuingauthority)
- [static let portrait: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/portrait)
- [static let sex: MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/sex)

#### Type Methods

- [static func ageAtLeast(Int) -> MobilePhotoIDRawDataRequest.Element](/documentation/proximityreader/mobilephotoidrawdatarequest/element/ageatleast(_:))
- [var nonRetainedElements: [MobilePhotoIDRawDataRequest.Element]](/documentation/proximityreader/mobilephotoidrawdatarequest/nonretainedelements)
- [var retainedElements: [MobilePhotoIDRawDataRequest.Element]](/documentation/proximityreader/mobilephotoidrawdatarequest/retainedelements)

### Handling the response

- [MobilePhotoIDRawDataRequest.Response](/documentation/proximityreader/mobilephotoidrawdatarequest/response)

#### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobilephotoidrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobilephotoidrawdatarequest/response/sessiontranscript)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobilephotoidrawdatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobilePhotoIDRawDataRequest.Response](/documentation/proximityreader/mobilephotoidrawdatarequest/response)

##### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobilephotoidrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobilephotoidrawdatarequest/response/sessiontranscript)
- [MobileDocumentAnyOfDataRequest](/documentation/proximityreader/mobiledocumentanyofdatarequest)

### Initializing a request

- [init()](/documentation/proximityreader/mobiledocumentanyofdatarequest/init())

### Handling the response

- [MobileDocumentAnyOfDataRequest.Response](/documentation/proximityreader/mobiledocumentanyofdatarequest/response)

#### Instance Properties

- [var documentResponse: any MobileDocumentDataResponse](/documentation/proximityreader/mobiledocumentanyofdatarequest/response/documentresponse)

### Instance Methods

- [func addRequest(any MobileDocumentDataRequest)](/documentation/proximityreader/mobiledocumentanyofdatarequest/addrequest(_:))

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledocumentanyofdatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileDocumentAnyOfDataRequest.Response](/documentation/proximityreader/mobiledocumentanyofdatarequest/response)

##### Instance Properties

- [var documentResponse: any MobileDocumentDataResponse](/documentation/proximityreader/mobiledocumentanyofdatarequest/response/documentresponse)
- [MobileDocumentAnyOfRawDataRequest](/documentation/proximityreader/mobiledocumentanyofrawdatarequest)

### Initializing a raw data request

- [init()](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/init())
- [func addRequest(any MobileDocumentRawDataRequest)](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/addrequest(_:))

### Handling the response

- [MobileDocumentAnyOfRawDataRequest.Response](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/response)

#### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/response/sessiontranscript)

### Default Implementations

- [MobileDocumentRequest Implementations](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/mobiledocumentrequest-implementations)

#### Structures

- [MobileDocumentAnyOfRawDataRequest.Response](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/response)

##### Instance Properties

- [let responseData: Data](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/response/responsedata)
- [let sessionTranscript: Data](/documentation/proximityreader/mobiledocumentanyofrawdatarequest/response/sessiontranscript)

## Errors

- [PaymentCardReaderError](/documentation/proximityreader/paymentcardreadererror)

### Getting the error code

- [case accountAlreadyLinked](/documentation/proximityreader/paymentcardreadererror/accountalreadylinked)
- [case accountDeactivated](/documentation/proximityreader/paymentcardreadererror/accountdeactivated)
- [case accountLinkingCancelled](/documentation/proximityreader/paymentcardreadererror/accountlinkingcancelled)
- [case accountLinkingCheckFailed](/documentation/proximityreader/paymentcardreadererror/accountlinkingcheckfailed)
- [case accountLinkingFailed](/documentation/proximityreader/paymentcardreadererror/accountlinkingfailed)
- [case accountLinkingRequiresiCloudSignIn](/documentation/proximityreader/paymentcardreadererror/accountlinkingrequiresicloudsignin)
- [case accountNotLinked](/documentation/proximityreader/paymentcardreadererror/accountnotlinked)
- [case backgroundRequestNotAllowed](/documentation/proximityreader/paymentcardreadererror/backgroundrequestnotallowed)
- [case deviceBanned(Date?)](/documentation/proximityreader/paymentcardreadererror/devicebanned(_:))
- [case emptyReaderToken](/documentation/proximityreader/paymentcardreadererror/emptyreadertoken)
- [case invalidMerchant](/documentation/proximityreader/paymentcardreadererror/invalidmerchant)
- [case invalidReaderToken(String?)](/documentation/proximityreader/paymentcardreadererror/invalidreadertoken(_:))
- [case merchantBlocked](/documentation/proximityreader/paymentcardreadererror/merchantblocked)
- [case modelNotSupported](/documentation/proximityreader/paymentcardreadererror/modelnotsupported)
- [case networkAuthenticationError](/documentation/proximityreader/paymentcardreadererror/networkauthenticationerror)
- [case networkError](/documentation/proximityreader/paymentcardreadererror/networkerror)
- [case notAllowed](/documentation/proximityreader/paymentcardreadererror/notallowed)
- [case notReady](/documentation/proximityreader/paymentcardreadererror/notready)
- [case osVersionNotSupported](/documentation/proximityreader/paymentcardreadererror/osversionnotsupported)
- [case passcodeDisabled](/documentation/proximityreader/paymentcardreadererror/passcodedisabled)
- [case prepareExpired](/documentation/proximityreader/paymentcardreadererror/prepareexpired)
- [case prepareFailed(String?)](/documentation/proximityreader/paymentcardreadererror/preparefailed(_:))
- [case readerBusy](/documentation/proximityreader/paymentcardreadererror/readerbusy)
- [case readerMemoryFull](/documentation/proximityreader/paymentcardreadererror/readermemoryfull)
- [case serviceConnectionError](/documentation/proximityreader/paymentcardreadererror/serviceconnectionerror)
- [case tokenExpired](/documentation/proximityreader/paymentcardreadererror/tokenexpired)
- [case unsupported](/documentation/proximityreader/paymentcardreadererror/unsupported)
- [case unknown(code: Int)](/documentation/proximityreader/paymentcardreadererror/unknown(code:))

### Getting the error details

- [var errorDescription: String](/documentation/proximityreader/paymentcardreadererror/errordescription)
- [var errorName: String](/documentation/proximityreader/paymentcardreadererror/errorname)

### Enumeration Cases

- [case requestInterrupted](/documentation/proximityreader/paymentcardreadererror/requestinterrupted)
- [case storeAndForwardNotAllowed](/documentation/proximityreader/paymentcardreadererror/storeandforwardnotallowed)
- [case storeAndForwardSessionExpired](/documentation/proximityreader/paymentcardreadererror/storeandforwardsessionexpired)
- [case storeAndForwardSessionInvalidated](/documentation/proximityreader/paymentcardreadererror/storeandforwardsessioninvalidated)
- [case storeAndForwardTokenIssuerChanged](/documentation/proximityreader/paymentcardreadererror/storeandforwardtokenissuerchanged)
- [MobileDocumentReaderError](/documentation/proximityreader/mobiledocumentreadererror)

### Getting the error code

- [case cancelled](/documentation/proximityreader/mobiledocumentreadererror/cancelled)
- [case invalidRequest](/documentation/proximityreader/mobiledocumentreadererror/invalidrequest)
- [case invalidResponse](/documentation/proximityreader/mobiledocumentreadererror/invalidresponse)
- [case invalidToken](/documentation/proximityreader/mobiledocumentreadererror/invalidtoken)
- [case networkUnavailable](/documentation/proximityreader/mobiledocumentreadererror/networkunavailable)
- [case notAllowed](/documentation/proximityreader/mobiledocumentreadererror/notallowed)
- [case notSupported](/documentation/proximityreader/mobiledocumentreadererror/notsupported)
- [case serviceUnavailable](/documentation/proximityreader/mobiledocumentreadererror/serviceunavailable)
- [case sessionExpired](/documentation/proximityreader/mobiledocumentreadererror/sessionexpired)
- [case systemBusy](/documentation/proximityreader/mobiledocumentreadererror/systembusy)
- [case unknown](/documentation/proximityreader/mobiledocumentreadererror/unknown)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
