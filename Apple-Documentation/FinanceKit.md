# FinanceKit Documentation

Source: https://sosumi.ai/documentation/financekit

---
title: FinanceKit
source: https://developer.apple.com/documentation/financekit
timestamp: 2026-02-13T18:57:02.560Z
---

## Essentials

- [Implementing a background delivery extension](/documentation/financekit/implementing-a-background-delivery-extension)
- [FinanceKit updates](/documentation/updates/financekit)

## Data storage

- [FinanceStore](/documentation/financekit/financestore)

### Retrieving the shared instance

- [static let shared: FinanceStore](/documentation/financekit/financestore/shared)

### Determining data availability

- [static func isDataAvailable(FinanceStore.DataType) -> Bool](/documentation/financekit/financestore/isdataavailable(_:))

### Checking authorization status and requesting authorization

- [func authorizationStatus() async throws -> AuthorizationStatus](/documentation/financekit/financestore/authorizationstatus())
- [func requestAuthorization() async throws -> AuthorizationStatus](/documentation/financekit/financestore/requestauthorization())

### Finding accounts

- [func accountHistory(since: FinanceStore.HistoryToken?, isMonitoring: Bool) -> FinanceStore.History<Account>](/documentation/financekit/financestore/accounthistory(since:ismonitoring:))
- [func accounts(query: AccountQuery) async throws -> [Account]](/documentation/financekit/financestore/accounts(query:))

### Getting account balances

- [func accountBalances(query: AccountBalanceQuery) async throws -> [AccountBalance]](/documentation/financekit/financestore/accountbalances(query:))
- [func accountBalanceHistory(forAccountID: UUID, since: FinanceStore.HistoryToken?, isMonitoring: Bool) -> FinanceStore.History<AccountBalance>](/documentation/financekit/financestore/accountbalancehistory(foraccountid:since:ismonitoring:))

### Searching for a specific order

- [func containsOrder(matching: FullyQualifiedOrderIdentifier, updatedDate: Date?) async throws -> FinanceStore.ContainsOrderResult](/documentation/financekit/financestore/containsorder(matching:updateddate:))

### Saving or updating orders

- [func saveOrder(signedArchive: Data) async throws -> FinanceStore.SaveOrderResult](/documentation/financekit/financestore/saveorder(signedarchive:))

### Monitoring transactions

- [func transactionHistory(forAccountID: UUID, since: FinanceStore.HistoryToken?, isMonitoring: Bool) -> FinanceStore.History<Transaction>](/documentation/financekit/financestore/transactionhistory(foraccountid:since:ismonitoring:))
- [func transactions(query: TransactionQuery) async throws -> [Transaction]](/documentation/financekit/financestore/transactions(query:))

### Enumerations

- [FinanceStore.ContainsOrderResult](/documentation/financekit/financestore/containsorderresult)

#### Enumeration Cases

- [case exists](/documentation/financekit/financestore/containsorderresult/exists)
- [case newerExists](/documentation/financekit/financestore/containsorderresult/newerexists)
- [case notFound](/documentation/financekit/financestore/containsorderresult/notfound)
- [case olderExists](/documentation/financekit/financestore/containsorderresult/olderexists)
- [FinanceStore.DataType](/documentation/financekit/financestore/datatype)

#### Enumeration Cases

- [case financialData](/documentation/financekit/financestore/datatype/financialdata)
- [case orders](/documentation/financekit/financestore/datatype/orders)
- [FinanceStore.SaveOrderResult](/documentation/financekit/financestore/saveorderresult)

#### Enumeration Cases

- [case added](/documentation/financekit/financestore/saveorderresult/added)
- [case cancelled](/documentation/financekit/financestore/saveorderresult/cancelled)
- [case newerExisting](/documentation/financekit/financestore/saveorderresult/newerexisting)
- [FinanceStore.BackgroundDataType](/documentation/financekit/financestore/backgrounddatatype)

#### Enumeration Cases

- [case accountBalances](/documentation/financekit/financestore/backgrounddatatype/accountbalances)
- [case accounts](/documentation/financekit/financestore/backgrounddatatype/accounts)
- [case transactions](/documentation/financekit/financestore/backgrounddatatype/transactions)
- [FinanceStore.UpdateFrequency](/documentation/financekit/financestore/updatefrequency)

#### Enumeration Cases

- [case daily](/documentation/financekit/financestore/updatefrequency/daily)
- [case hourly](/documentation/financekit/financestore/updatefrequency/hourly)
- [case weekly](/documentation/financekit/financestore/updatefrequency/weekly)

### Structures

- [FinanceStore.Changes](/documentation/financekit/financestore/changes)

#### Instance Properties

- [let deleted: [Model.ID]](/documentation/financekit/financestore/changes/deleted)
- [let inserted: [Model]](/documentation/financekit/financestore/changes/inserted)
- [let newToken: FinanceStore.HistoryToken](/documentation/financekit/financestore/changes/newtoken)
- [let updated: [Model]](/documentation/financekit/financestore/changes/updated)
- [FinanceStore.History](/documentation/financekit/financestore/history)

#### Structures

- [FinanceStore.History.Iterator](/documentation/financekit/financestore/history/iterator)

##### Instance Methods

- [func next() async throws -> FinanceStore.Changes<Model>?](/documentation/financekit/financestore/history/iterator/next())

#### Instance Methods

- [func makeAsyncIterator() -> FinanceStore.History<Model>.Iterator](/documentation/financekit/financestore/history/makeasynciterator())

#### Type Aliases

- [FinanceStore.History.AsyncIterator](/documentation/financekit/financestore/history/asynciterator)
- [FinanceStore.History.Element](/documentation/financekit/financestore/history/element)
- [FinanceStore.HistoryToken](/documentation/financekit/financestore/historytoken)

#### Initializers

- [init(from: any Decoder) throws](/documentation/financekit/financestore/historytoken/init(from:))

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/financekit/financestore/historytoken/encode(to:))

### Instance Methods

- [func disableAllBackgroundDelivery()](/documentation/financekit/financestore/disableallbackgrounddelivery())
- [func disableBackgroundDelivery(for: [FinanceStore.BackgroundDataType])](/documentation/financekit/financestore/disablebackgrounddelivery(for:))
- [func enableBackgroundDelivery(for: [FinanceStore.BackgroundDataType], frequency: FinanceStore.UpdateFrequency)](/documentation/financekit/financestore/enablebackgrounddelivery(for:frequency:))

## Authorization

- [func authorizationStatus() async throws -> AuthorizationStatus](/documentation/financekit/financestore/authorizationstatus())
- [func requestAuthorization() async throws -> AuthorizationStatus](/documentation/financekit/financestore/requestauthorization())
- [AuthorizationStatus](/documentation/financekit/authorizationstatus)

### Enumeration Cases

- [case authorized](/documentation/financekit/authorizationstatus/authorized)
- [case denied](/documentation/financekit/authorizationstatus/denied)
- [case notDetermined](/documentation/financekit/authorizationstatus/notdetermined)

## Accounts

- [func accounts(query: AccountQuery) async throws -> [Account]](/documentation/financekit/financestore/accounts(query:))
- [func accountHistory(since: FinanceStore.HistoryToken?, isMonitoring: Bool) -> FinanceStore.History<Account>](/documentation/financekit/financestore/accounthistory(since:ismonitoring:))
- [AssetAccount](/documentation/financekit/assetaccount)

### Instance Properties

- [let accountDescription: String?](/documentation/financekit/assetaccount/accountdescription)
- [let currencyCode: String](/documentation/financekit/assetaccount/currencycode)
- [let displayName: String](/documentation/financekit/assetaccount/displayname)
- [let id: UUID](/documentation/financekit/assetaccount/id)
- [let institutionName: String](/documentation/financekit/assetaccount/institutionname)
- [let openingDate: Date?](/documentation/financekit/assetaccount/openingdate)
- [LiabilityAccount](/documentation/financekit/liabilityaccount)

### Instance Properties

- [let accountDescription: String?](/documentation/financekit/liabilityaccount/accountdescription)
- [let creditInformation: AccountCreditInformation](/documentation/financekit/liabilityaccount/creditinformation)
- [let currencyCode: String](/documentation/financekit/liabilityaccount/currencycode)
- [let displayName: String](/documentation/financekit/liabilityaccount/displayname)
- [let id: UUID](/documentation/financekit/liabilityaccount/id)
- [let institutionName: String](/documentation/financekit/liabilityaccount/institutionname)
- [let openingDate: Date?](/documentation/financekit/liabilityaccount/openingdate)
- [Account](/documentation/financekit/account)

### Enumeration Casess

- [case asset(AssetAccount)](/documentation/financekit/account/asset(_:))
- [case liability(LiabilityAccount)](/documentation/financekit/account/liability(_:))

### Instance Properties

- [var accountDescription: String?](/documentation/financekit/account/accountdescription)
- [var assetAccount: AssetAccount?](/documentation/financekit/account/assetaccount)
- [var currencyCode: String](/documentation/financekit/account/currencycode)
- [var displayName: String](/documentation/financekit/account/displayname)
- [var id: UUID](/documentation/financekit/account/id)
- [var institutionName: String](/documentation/financekit/account/institutionname)
- [var liabilityAccount: LiabilityAccount?](/documentation/financekit/account/liabilityaccount)
- [var openingDate: Date?](/documentation/financekit/account/openingdate)

## Balances

- [func accountBalances(query: AccountBalanceQuery) async throws -> [AccountBalance]](/documentation/financekit/financestore/accountbalances(query:))
- [func accountBalanceHistory(forAccountID: UUID, since: FinanceStore.HistoryToken?, isMonitoring: Bool) -> FinanceStore.History<AccountBalance>](/documentation/financekit/financestore/accountbalancehistory(foraccountid:since:ismonitoring:))
- [AccountBalance](/documentation/financekit/accountbalance)

### Instance Properties

- [let accountID: UUID](/documentation/financekit/accountbalance/accountid)
- [var available: Balance?](/documentation/financekit/accountbalance/available)
- [var booked: Balance?](/documentation/financekit/accountbalance/booked)
- [var currencyCode: String](/documentation/financekit/accountbalance/currencycode)
- [let currentBalance: CurrentBalance](/documentation/financekit/accountbalance/currentbalance)
- [let id: UUID](/documentation/financekit/accountbalance/id)
- [AccountBalanceQuery](/documentation/financekit/accountbalancequery)

### Initializers

- [init(sortDescriptors: [SortDescriptor<AccountBalance>], predicate: Predicate<AccountBalance>?, limit: Int?, offset: Int?)](/documentation/financekit/accountbalancequery/init(sortdescriptors:predicate:limit:offset:))

### Type Methods

- [static func predicate(availableSince: Date, until: Date?) -> Predicate<AccountBalance>](/documentation/financekit/accountbalancequery/predicate(availablesince:until:))
- [static func predicate(bookedSince: Date, until: Date?) -> Predicate<AccountBalance>](/documentation/financekit/accountbalancequery/predicate(bookedsince:until:))
- [Balance](/documentation/financekit/balance)

### Instance Properties

- [let amount: CurrencyAmount](/documentation/financekit/balance/amount)
- [let asOfDate: Date](/documentation/financekit/balance/asofdate)
- [let creditDebitIndicator: CreditDebitIndicator](/documentation/financekit/balance/creditdebitindicator)
- [CreditDebitIndicator](/documentation/financekit/creditdebitindicator)

### Enumeration Cases

- [case credit](/documentation/financekit/creditdebitindicator/credit)
- [case debit](/documentation/financekit/creditdebitindicator/debit)
- [CurrentBalance](/documentation/financekit/currentbalance)

### Enumeration Cases

- [case available(Balance)](/documentation/financekit/currentbalance/available(_:))
- [case availableAndBooked(available: Balance, booked: Balance)](/documentation/financekit/currentbalance/availableandbooked(available:booked:))
- [case booked(Balance)](/documentation/financekit/currentbalance/booked(_:))

## Orders

- [FullyQualifiedOrderIdentifier](/documentation/financekit/fullyqualifiedorderidentifier)

### Initializers

- [init(orderTypeIdentifier: String, orderIdentifier: String)](/documentation/financekit/fullyqualifiedorderidentifier/init(ordertypeidentifier:orderidentifier:))

### Instance Properties

- [var orderIdentifier: String](/documentation/financekit/fullyqualifiedorderidentifier/orderidentifier)
- [var orderTypeIdentifier: String](/documentation/financekit/fullyqualifiedorderidentifier/ordertypeidentifier)
- [func saveOrder(signedArchive: Data) async throws -> FinanceStore.SaveOrderResult](/documentation/financekit/financestore/saveorder(signedarchive:))

## Transactions

- [func transactionHistory(forAccountID: UUID, since: FinanceStore.HistoryToken?, isMonitoring: Bool) -> FinanceStore.History<Transaction>](/documentation/financekit/financestore/transactionhistory(foraccountid:since:ismonitoring:))
- [func transactions(query: TransactionQuery) async throws -> [Transaction]](/documentation/financekit/financestore/transactions(query:))
- [AccountQuery](/documentation/financekit/accountquery)

### Initializers

- [init(sortDescriptors: [SortDescriptor<Account>], predicate: Predicate<Account>?, limit: Int?, offset: Int?)](/documentation/financekit/accountquery/init(sortdescriptors:predicate:limit:offset:))
- [AccountCreditInformation](/documentation/financekit/accountcreditinformation)

### Instance Properties

- [let creditLimit: CurrencyAmount?](/documentation/financekit/accountcreditinformation/creditlimit)
- [let minimumNextPaymentAmount: CurrencyAmount?](/documentation/financekit/accountcreditinformation/minimumnextpaymentamount)
- [let nextPaymentDueDate: Date?](/documentation/financekit/accountcreditinformation/nextpaymentduedate)
- [let overduePaymentAmount: CurrencyAmount?](/documentation/financekit/accountcreditinformation/overduepaymentamount)
- [CurrencyAmount](/documentation/financekit/currencyamount)

### Instance Properties

- [let amount: Decimal](/documentation/financekit/currencyamount/amount)
- [let currencyCode: String](/documentation/financekit/currencyamount/currencycode)
- [Transaction](/documentation/financekit/transaction)

### Instance Properties

- [let accountID: UUID](/documentation/financekit/transaction/accountid)
- [let creditDebitIndicator: CreditDebitIndicator](/documentation/financekit/transaction/creditdebitindicator)
- [let foreignCurrencyAmount: CurrencyAmount?](/documentation/financekit/transaction/foreigncurrencyamount)
- [let foreignCurrencyExchangeRate: Decimal?](/documentation/financekit/transaction/foreigncurrencyexchangerate)
- [let id: UUID](/documentation/financekit/transaction/id)
- [let merchantCategoryCode: MerchantCategoryCode?](/documentation/financekit/transaction/merchantcategorycode)
- [let merchantName: String?](/documentation/financekit/transaction/merchantname)
- [let originalTransactionDescription: String](/documentation/financekit/transaction/originaltransactiondescription)
- [let postedDate: Date?](/documentation/financekit/transaction/posteddate)
- [let status: TransactionStatus](/documentation/financekit/transaction/status)
- [let transactionAmount: CurrencyAmount](/documentation/financekit/transaction/transactionamount)
- [let transactionDate: Date](/documentation/financekit/transaction/transactiondate)
- [let transactionDescription: String](/documentation/financekit/transaction/transactiondescription)
- [let transactionType: TransactionType](/documentation/financekit/transaction/transactiontype)
- [TransactionQuery](/documentation/financekit/transactionquery)

### Initializers

- [init(sortDescriptors: [SortDescriptor<Transaction>], predicate: Predicate<Transaction>?, limit: Int?, offset: Int?)](/documentation/financekit/transactionquery/init(sortdescriptors:predicate:limit:offset:))

### Type Methods

- [static func predicate(forMerchantCategoryCodes: [MerchantCategoryCode]) -> Predicate<Transaction>](/documentation/financekit/transactionquery/predicate(formerchantcategorycodes:))
- [static func predicate(forStatuses: [TransactionStatus]) -> Predicate<Transaction>](/documentation/financekit/transactionquery/predicate(forstatuses:))
- [static func predicate(forTransactionTypes: [TransactionType]) -> Predicate<Transaction>](/documentation/financekit/transactionquery/predicate(fortransactiontypes:))
- [TransactionType](/documentation/financekit/transactiontype)

### Enumeration Cases

- [case adjustment](/documentation/financekit/transactiontype/adjustment)
- [case atm](/documentation/financekit/transactiontype/atm)
- [case billPayment](/documentation/financekit/transactiontype/billpayment)
- [case check](/documentation/financekit/transactiontype/check)
- [case deposit](/documentation/financekit/transactiontype/deposit)
- [case directDebit](/documentation/financekit/transactiontype/directdebit)
- [case directDeposit](/documentation/financekit/transactiontype/directdeposit)
- [case dividend](/documentation/financekit/transactiontype/dividend)
- [case fee](/documentation/financekit/transactiontype/fee)
- [case interest](/documentation/financekit/transactiontype/interest)
- [case loan](/documentation/financekit/transactiontype/loan)
- [case pointOfSale](/documentation/financekit/transactiontype/pointofsale)
- [case refund](/documentation/financekit/transactiontype/refund)
- [case standingOrder](/documentation/financekit/transactiontype/standingorder)
- [case transfer](/documentation/financekit/transactiontype/transfer)
- [case unknown](/documentation/financekit/transactiontype/unknown)
- [case withdrawal](/documentation/financekit/transactiontype/withdrawal)
- [TransactionStatus](/documentation/financekit/transactionstatus)

### Enumeration Cases

- [case authorized](/documentation/financekit/transactionstatus/authorized)
- [case booked](/documentation/financekit/transactionstatus/booked)
- [case memo](/documentation/financekit/transactionstatus/memo)
- [case pending](/documentation/financekit/transactionstatus/pending)
- [case rejected](/documentation/financekit/transactionstatus/rejected)

## Queries

- [FinanceStore.HistoryToken](/documentation/financekit/financestore/historytoken)

### Initializers

- [init(from: any Decoder) throws](/documentation/financekit/financestore/historytoken/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/financekit/financestore/historytoken/encode(to:))

## Merchant categories

- [MerchantCategoryCode](/documentation/financekit/merchantcategorycode)

### Initializers

- [init(rawValue: Int16)](/documentation/financekit/merchantcategorycode/init(rawvalue:))

### Instance Properties

- [let rawValue: Int16](/documentation/financekit/merchantcategorycode/rawvalue)

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/financekit/merchantcategorycode/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/financekit/merchantcategorycode/description)
- [LosslessStringConvertible Implementations](/documentation/financekit/merchantcategorycode/losslessstringconvertible-implementations)

#### Initializers

- [init?(String)](/documentation/financekit/merchantcategorycode/init(_:))

## Errors

- [FinanceError](/documentation/financekit/financeerror)

### Enumeration Cases

- [case dataRestricted(FinanceStore.DataType)](/documentation/financekit/financeerror/datarestricted(_:))
- [case historyTokenInvalid](/documentation/financekit/financeerror/historytokeninvalid)
- [case unknown](/documentation/financekit/financeerror/unknown)

### Instance Properties

- [var errorCode: Int](/documentation/financekit/financeerror/errorcode)
- [var errorDescription: String?](/documentation/financekit/financeerror/errordescription)
- [var errorUserInfo: [String : Any]](/documentation/financekit/financeerror/erroruserinfo)
- [var failureReason: String?](/documentation/financekit/financeerror/failurereason)

### Type Properties

- [static var errorDomain: String](/documentation/financekit/financeerror/errordomain)

## Protocols

- [BackgroundDeliveryExtension](/documentation/financekit/backgrounddeliveryextension)
- [BackgroundDeliveryExtensionProviding](/documentation/financekit/backgrounddeliveryextensionproviding)

### Instance Methods

- [func didReceiveData(for: [FinanceStore.BackgroundDataType]) async](/documentation/financekit/backgrounddeliveryextensionproviding/didreceivedata(for:))
- [func willTerminate() async](/documentation/financekit/backgrounddeliveryextensionproviding/willterminate())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
