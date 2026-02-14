# FinanceKitUI Documentation

Source: https://sosumi.ai/documentation/financekitui

---
title: FinanceKitUI
source: https://developer.apple.com/documentation/financekitui
timestamp: 2026-02-13T18:57:04.603Z
---

## Adding an order to Apple Wallet

- [AddOrderToWalletButton](/documentation/financekitui/addordertowalletbutton)

### Initializers

- [init(signedArchive: Data, onCompletion: (Result<FinanceStore.SaveOrderResult, any Error>) -> Void)](/documentation/financekitui/addordertowalletbutton/init(signedarchive:oncompletion:))
- [AddOrderToWalletButtonStyle](/documentation/financekitui/addordertowalletbuttonstyle)

### Type Properties

- [static let black: AddOrderToWalletButtonStyle](/documentation/financekitui/addordertowalletbuttonstyle/black)
- [static let blackOutline: AddOrderToWalletButtonStyle](/documentation/financekitui/addordertowalletbuttonstyle/blackoutline)

## Protocols

- [FinancialConnectionUIExtension](/documentation/financekitui/financialconnectionuiextension)

### Associated Types

- [Body](/documentation/financekitui/financialconnectionuiextension/body-swift.associatedtype)

### Instance Properties

- [var body: Self.Body](/documentation/financekitui/financialconnectionuiextension/body-swift.property)
- [FinancialConnectionUIExtensionProviding](/documentation/financekitui/financialconnectionuiextensionproviding)

### Instance Methods

- [func authorize(FinancialConnectionExtensionAuthorizationRequest)](/documentation/financekitui/financialconnectionuiextensionproviding/authorize(_:))
- [FinancialConnectionUIExtensionScene](/documentation/financekitui/financialconnectionuiextensionscene)

## Structures

- [FinancialConnectionExtensionAuthorizationRequest](/documentation/financekitui/financialconnectionextensionauthorizationrequest)

### Instance Properties

- [var params: FinancialConnectionExtensionAuthorizationParams](/documentation/financekitui/financialconnectionextensionauthorizationrequest/params)

### Instance Methods -

- [func complete(authorizationResult: FinancialConnectionExtensionAuthorizationResult)](/documentation/financekitui/financialconnectionextensionauthorizationrequest/complete(authorizationresult:))
- [func complete(error: any Error)](/documentation/financekitui/financialconnectionextensionauthorizationrequest/complete(error:))

### Type Aliases

- [FinancialConnectionExtensionAuthorizationRequest.CompletionHandler](/documentation/financekitui/financialconnectionextensionauthorizationrequest/completionhandler)
- [FinancialConnectionExtensionAuthorizationRequest.CompletionHandlerResult](/documentation/financekitui/financialconnectionextensionauthorizationrequest/completionhandlerresult)
- [FinancialConnectionExtensionAuthorizationResult](/documentation/financekitui/financialconnectionextensionauthorizationresult)

### Initializers

- [init(params: FinancialConnectionExtensionAuthorizationParams)](/documentation/financekitui/financialconnectionextensionauthorizationresult/init(params:))

### Instance Properties

- [let params: FinancialConnectionExtensionAuthorizationParams](/documentation/financekitui/financialconnectionextensionauthorizationresult/params)
- [FinancialConnectionUIExtensionAuthorizationScene](/documentation/financekitui/financialconnectionuiextensionauthorizationscene)

### Initializers

- [init(content: () -> Content)](/documentation/financekitui/financialconnectionuiextensionauthorizationscene/init(content:))
- [TransactionPicker](/documentation/financekitui/transactionpicker)

### Initializers

- [init(selection: Binding<[Transaction]>, label: () -> Label)](/documentation/financekitui/transactionpicker/init(selection:label:))

## Type Aliases

- [FinancialConnectionExtensionAuthorizationParams](/documentation/financekitui/financialconnectionextensionauthorizationparams)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
