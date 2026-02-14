# PassKit Documentation

Source: https://sosumi.ai/documentation/passkit

---
title: PassKit (Apple Pay and Wallet)
source: https://developer.apple.com/documentation/passkit
timestamp: 2026-02-13T19:57:54.393Z
---

## Apple pay support

- [Apple Pay](/documentation/passkit/apple-pay)

### Apple Pay setup

- [Setting up Apple Pay](/documentation/passkit/setting-up-apple-pay)
- [Offering Apple Pay in Your App](/documentation/passkit/offering-apple-pay-in-your-app)
- [Complying with regional regulations](/documentation/passkit/complying-with-regional-regulations)

### Apple Pay availability

- [PKPaymentAuthorizationController](/documentation/passkit/pkpaymentauthorizationcontroller)

#### Creating a payment authorization controller

- [init(paymentRequest: PKPaymentRequest)](/documentation/passkit/pkpaymentauthorizationcontroller/init(paymentrequest:))
- [convenience init(disbursementRequest: PKDisbursementRequest)](/documentation/passkit/pkpaymentauthorizationcontroller/init(disbursementrequest:))

#### Determining whether the user can make payments or disbursements

- [class func canMakePayments() -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/canmakepayments())
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/canmakepayments(usingnetworks:))
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/canmakepayments(usingnetworks:capabilities:))
- [class func supportsDisbursements() -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/supportsdisbursements())
- [class func supportsDisbursements(using: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/supportsdisbursements(using:))
- [class func supportsDisbursements(using: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/supportsdisbursements(using:capabilities:))

#### Handling user interactions

- [var delegate: (any PKPaymentAuthorizationControllerDelegate)?](/documentation/passkit/pkpaymentauthorizationcontroller/delegate)
- [PKPaymentAuthorizationControllerDelegate](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate)

##### Handling user interactions

- [func presentationWindow(for: PKPaymentAuthorizationController) -> UIWindow?](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/presentationwindow(for:))

##### Handling user’s payment method selection

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectPaymentMethod: PKPaymentMethod, handler: (PKPaymentRequestPaymentMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectpaymentmethod:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectPaymentMethod: PKPaymentMethod, completion: ([PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectpaymentmethod:completion:))

##### Handling coupons

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didChangeCouponCode: String, handler: (PKPaymentRequestCouponCodeUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didchangecouponcode:handler:))

##### Handling shipping information

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingContact: PKContact, handler: (PKPaymentRequestShippingContactUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingcontact:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingContact: PKContact, completion: (PKPaymentAuthorizationStatus, [PKShippingMethod], [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingcontact:completion:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingMethod: PKShippingMethod, handler: (PKPaymentRequestShippingMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingmethod:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingMethod: PKShippingMethod, completion: (PKPaymentAuthorizationStatus, [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingmethod:completion:))

##### Handling user’s payment authorization

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didRequestMerchantSessionUpdate: (PKPaymentRequestMerchantSessionUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didrequestmerchantsessionupdate:))
- [func paymentAuthorizationControllerWillAuthorizePayment(PKPaymentAuthorizationController)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontrollerwillauthorizepayment(_:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didAuthorizePayment: PKPayment, handler: (PKPaymentAuthorizationResult) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didauthorizepayment:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didAuthorizePayment: PKPayment, completion: (PKPaymentAuthorizationStatus) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didauthorizepayment:completion:))
- [func paymentAuthorizationControllerDidFinish(PKPaymentAuthorizationController)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontrollerdidfinish(_:))
- [func present(completion: ((Bool) -> Void)?)](/documentation/passkit/pkpaymentauthorizationcontroller/present(completion:))
- [func dismiss(completion: (() -> Void)?)](/documentation/passkit/pkpaymentauthorizationcontroller/dismiss(completion:))
- [PKPaymentAuthorizationViewController](/documentation/passkit/pkpaymentauthorizationviewcontroller)

#### Determining whether the user can make payments

- [class func canMakePayments() -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/canmakepayments())
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/canmakepayments(usingnetworks:))
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/canmakepayments(usingnetworks:capabilities:))
- [class func supportsDisbursements() -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/supportsdisbursements())
- [class func supportsDisbursements(using: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/supportsdisbursements(using:))
- [class func supportsDisbursements(using: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/supportsdisbursements(using:capabilities:))

#### Handling user interactions

- [var delegate: (any PKPaymentAuthorizationViewControllerDelegate)?](/documentation/passkit/pkpaymentauthorizationviewcontroller/delegate)
- [PKPaymentAuthorizationViewControllerDelegate](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate)

##### Handling user’s payment authorization

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didRequestMerchantSessionUpdate: (PKPaymentRequestMerchantSessionUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didrequestmerchantsessionupdate:))
- [func paymentAuthorizationViewControllerWillAuthorizePayment(PKPaymentAuthorizationViewController)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontrollerwillauthorizepayment(_:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didAuthorizePayment: PKPayment, handler: (PKPaymentAuthorizationResult) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didauthorizepayment:handler:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didAuthorizePayment: PKPayment, completion: (PKPaymentAuthorizationStatus) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didauthorizepayment:completion:))
- [func paymentAuthorizationViewControllerDidFinish(PKPaymentAuthorizationViewController)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontrollerdidfinish(_:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKPaymentMethod, handler: (PKPaymentRequestPaymentMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:handler:)-3bex6)
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKPaymentMethod, completion: ([PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:completion:)-30s85)

##### Handling coupons

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didChangeCouponCode: String, handler: (PKPaymentRequestCouponCodeUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didchangecouponcode:handler:))

##### Handling shipping information

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelectShippingContact: PKContact, handler: (PKPaymentRequestShippingContactUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselectshippingcontact:handler:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelectShippingContact: PKContact, completion: (PKPaymentAuthorizationStatus, [PKShippingMethod], [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselectshippingcontact:completion:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKShippingMethod, handler: (PKPaymentRequestShippingMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:handler:)-5r0i7)
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKShippingMethod, completion: (PKPaymentAuthorizationStatus, [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:completion:)-9otrj)

##### Deprecated

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelectShippingAddress: ABRecord, completion: (PKPaymentAuthorizationStatus, [PKShippingMethod], [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselectshippingaddress:completion:))

#### Creating a payment authorization view controller

- [init?(paymentRequest: PKPaymentRequest)](/documentation/passkit/pkpaymentauthorizationviewcontroller/init(paymentrequest:))
- [convenience init(disbursementRequest: PKDisbursementRequest)](/documentation/passkit/pkpaymentauthorizationviewcontroller/init(disbursementrequest:))

### Apple Pay buttons

- [PKPaymentButton](/documentation/passkit/pkpaymentbutton)

#### Creating payment buttons

- [init(paymentButtonType: PKPaymentButtonType, paymentButtonStyle: PKPaymentButtonStyle)](/documentation/passkit/pkpaymentbutton/init(paymentbuttontype:paymentbuttonstyle:))

#### Configuring the appearance

- [PKPaymentButtonType](/documentation/passkit/pkpaymentbuttontype)

##### Payment button types

- [case plain](/documentation/passkit/pkpaymentbuttontype/plain)
- [case buy](/documentation/passkit/pkpaymentbuttontype/buy)
- [case addMoney](/documentation/passkit/pkpaymentbuttontype/addmoney)
- [case book](/documentation/passkit/pkpaymentbuttontype/book)
- [case checkout](/documentation/passkit/pkpaymentbuttontype/checkout)
- [case `continue`](/documentation/passkit/pkpaymentbuttontype/continue)
- [case contribute](/documentation/passkit/pkpaymentbuttontype/contribute)
- [case donate](/documentation/passkit/pkpaymentbuttontype/donate)
- [case inStore](/documentation/passkit/pkpaymentbuttontype/instore)
- [case order](/documentation/passkit/pkpaymentbuttontype/order)
- [case reload](/documentation/passkit/pkpaymentbuttontype/reload)
- [case rent](/documentation/passkit/pkpaymentbuttontype/rent)
- [case setUp](/documentation/passkit/pkpaymentbuttontype/setup)
- [case subscribe](/documentation/passkit/pkpaymentbuttontype/subscribe)
- [case support](/documentation/passkit/pkpaymentbuttontype/support)
- [case tip](/documentation/passkit/pkpaymentbuttontype/tip)
- [case topUp](/documentation/passkit/pkpaymentbuttontype/topup)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaymentbuttontype/init(rawvalue:))
- [PKPaymentButtonStyle](/documentation/passkit/pkpaymentbuttonstyle)

##### Payment button styles

- [case white](/documentation/passkit/pkpaymentbuttonstyle/white)
- [case whiteOutline](/documentation/passkit/pkpaymentbuttonstyle/whiteoutline)
- [case black](/documentation/passkit/pkpaymentbuttonstyle/black)
- [case automatic](/documentation/passkit/pkpaymentbuttonstyle/automatic)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaymentbuttonstyle/init(rawvalue:))
- [var cornerRadius: CGFloat](/documentation/passkit/pkpaymentbutton/cornerradius)

#### Initializers

- [convenience init(type: PKPaymentButtonType, style: PKPaymentButtonStyle, disableCardArt: Bool)](/documentation/passkit/pkpaymentbutton/init(type:style:disablecardart:))
- [PayWithApplePayButton](/documentation/passkit/paywithapplepaybutton)

#### Creating the button

- [init(PayWithApplePayButtonLabel, action: () -> Void)](/documentation/passkit/paywithapplepaybutton/init(_:action:))
- [init(PayWithApplePayButtonLabel, action: () -> Void, fallback: () -> Fallback)](/documentation/passkit/paywithapplepaybutton/init(_:action:fallback:))
- [init(PayWithApplePayButtonLabel, request: PKPaymentRequest, onPaymentAuthorizationChange: (PayWithApplePayButtonPaymentAuthorizationPhase) -> Void)](/documentation/passkit/paywithapplepaybutton/init(_:request:onpaymentauthorizationchange:))
- [init(PayWithApplePayButtonLabel, request: PKPaymentRequest, onPaymentAuthorizationChange: (PayWithApplePayButtonPaymentAuthorizationPhase) -> Void, fallback: () -> Fallback)](/documentation/passkit/paywithapplepaybutton/init(_:request:onpaymentauthorizationchange:fallback:))
- [init(PayWithApplePayButtonLabel, request: PKPaymentRequest, onPaymentAuthorizationChange: (PayWithApplePayButtonPaymentAuthorizationPhase) -> Void, onMerchantSessionRequested: () async -> PKPaymentRequestMerchantSessionUpdate)](/documentation/passkit/paywithapplepaybutton/init(_:request:onpaymentauthorizationchange:onmerchantsessionrequested:))
- [init(PayWithApplePayButtonLabel, request: PKPaymentRequest, onPaymentAuthorizationChange: (PayWithApplePayButtonPaymentAuthorizationPhase) -> Void, onMerchantSessionRequested: () async -> PKPaymentRequestMerchantSessionUpdate, fallback: () -> Fallback)](/documentation/passkit/paywithapplepaybutton/init(_:request:onpaymentauthorizationchange:onmerchantsessionrequested:fallback:))
- [PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel)

#### Type Properties

- [static let addMoney: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/addmoney)
- [static let book: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/book)
- [static let buy: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/buy)
- [static let checkout: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/checkout)
- [static let `continue`: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/continue)
- [static let contribute: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/contribute)
- [static let donate: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/donate)
- [static let inStore: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/instore)
- [static let order: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/order)
- [static let plain: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/plain)
- [static let reload: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/reload)
- [static let rent: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/rent)
- [static let setUp: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/setup)
- [static let subscribe: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/subscribe)
- [static let support: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/support)
- [static let tip: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/tip)
- [static let topUp: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/topup)
- [PayWithApplePayButtonStyle](/documentation/passkit/paywithapplepaybuttonstyle)

#### Type Properties

- [static let automatic: PayWithApplePayButtonStyle](/documentation/passkit/paywithapplepaybuttonstyle/automatic)
- [static let black: PayWithApplePayButtonStyle](/documentation/passkit/paywithapplepaybuttonstyle/black)
- [static let white: PayWithApplePayButtonStyle](/documentation/passkit/paywithapplepaybuttonstyle/white)
- [static let whiteOutline: PayWithApplePayButtonStyle](/documentation/passkit/paywithapplepaybuttonstyle/whiteoutline)
- [PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel)

#### Type Properties

- [static let addMoney: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/addmoney)
- [static let book: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/book)
- [static let buy: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/buy)
- [static let checkout: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/checkout)
- [static let `continue`: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/continue)
- [static let contribute: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/contribute)
- [static let donate: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/donate)
- [static let inStore: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/instore)
- [static let order: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/order)
- [static let plain: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/plain)
- [static let reload: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/reload)
- [static let rent: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/rent)
- [static let setUp: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/setup)
- [static let subscribe: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/subscribe)
- [static let support: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/support)
- [static let tip: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/tip)
- [static let topUp: PayWithApplePayButtonLabel](/documentation/passkit/paywithapplepaybuttonlabel/topup)

### Payment requests

- [PKPaymentRequest](/documentation/passkit/pkpaymentrequest)

#### Selecting the payment networks

- [class func availableNetworks() -> [PKPaymentNetwork]](/documentation/passkit/pkpaymentrequest/availablenetworks())
- [var supportedNetworks: [PKPaymentNetwork]](/documentation/passkit/pkpaymentrequest/supportednetworks)
- [PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork)

##### Payment networks

- [static let amex: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/amex)
- [static let bancomat: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/bancomat)
- [static let bancontact: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/bancontact)
- [static let bankAxept: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/bankaxept)
- [static let barcode: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/barcode)
- [static let carteBancaire: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/cartebancaire)
- [static let cartesBancaires: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/cartesbancaires)
- [static let chinaUnionPay: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/chinaunionpay)
- [static let dankort: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/dankort)
- [static let discover: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/discover)
- [static let eftpos: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/eftpos)
- [static let electron: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/electron)
- [static let elo: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/elo)
- [static let girocard: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/girocard)
- [static let idCredit: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/idcredit)
- [static let interac: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/interac)
- [static let JCB: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/jcb)
- [static let mada: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/mada)
- [static let maestro: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/maestro)
- [static let masterCard: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/mastercard)
- [static let meeza: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/meeza)
- [static let mir: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/mir)
- [static let nanaco: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/nanaco)
- [static let NAPAS: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/napas)
- [static let pagoBancomat: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/pagobancomat)
- [static let postFinance: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/postfinance)
- [static let privateLabel: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/privatelabel)
- [static let quicPay: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/quicpay)
- [static let suica: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/suica)
- [static let tmoney: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/tmoney)
- [static let visa: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/visa)
- [static let vPay: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/vpay)
- [static let waon: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/waon)
- [static let carteBancaires: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/cartebancaires)

##### Initializers

- [init(String)](/documentation/passkit/pkpaymentnetwork/init(_:))
- [init(rawValue: String)](/documentation/passkit/pkpaymentnetwork/init(rawvalue:))

##### Type Properties

- [static let conecs: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/conecs)
- [static let himyan: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/himyan)
- [static let jaywan: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/jaywan)
- [static let myDebit: PKPaymentNetwork](/documentation/passkit/pkpaymentnetwork/mydebit)

#### Setting merchant information

- [PKPaymentRequest.MerchantCategoryCode](/documentation/passkit/pkpaymentrequest/merchantcategorycode-swift.struct)
- [var merchantIdentifier: String](/documentation/passkit/pkpaymentrequest/merchantidentifier)
- [var merchantCapabilities: PKMerchantCapability](/documentation/passkit/pkpaymentrequest/merchantcapabilities)
- [PKMerchantCapability](/documentation/passkit/pkmerchantcapability)

##### Initializers

- [init(rawValue: UInt)](/documentation/passkit/pkmerchantcapability/init(rawvalue:))

##### Constants

- [static var instantFundsOut: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/instantfundsout)
- [static var threeDSecure: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/threedsecure)
- [static var emv: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/emv)
- [static var credit: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/credit)
- [static var debit: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/debit)

##### Type Properties

- [static var capability3DS: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/capability3ds)
- [static var capabilityCredit: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/capabilitycredit)
- [static var capabilityDebit: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/capabilitydebit)
- [static var capabilityEMV: PKMerchantCapability](/documentation/passkit/pkmerchantcapability/capabilityemv)

#### Setting currency and region information

- [var currencyCode: String](/documentation/passkit/pkpaymentrequest/currencycode)
- [var supportedCountries: Set<String>?](/documentation/passkit/pkpaymentrequest/supportedcountries)
- [var countryCode: String](/documentation/passkit/pkpaymentrequest/countrycode)

#### Setting the payment summary items

- [var paymentSummaryItems: [PKPaymentSummaryItem]](/documentation/passkit/pkpaymentrequest/paymentsummaryitems)
- [PKPaymentSummaryItem](/documentation/passkit/pkpaymentsummaryitem)

##### Creating  summary items

- [convenience init(label: String, amount: NSDecimalNumber)](/documentation/passkit/pkpaymentsummaryitem/init(label:amount:))
- [convenience init(label: String, amount: NSDecimalNumber, type: PKPaymentSummaryItemType)](/documentation/passkit/pkpaymentsummaryitem/init(label:amount:type:))

##### Describing summary items

- [var label: String](/documentation/passkit/pkpaymentsummaryitem/label)
- [var amount: NSDecimalNumber](/documentation/passkit/pkpaymentsummaryitem/amount)
- [var type: PKPaymentSummaryItemType](/documentation/passkit/pkpaymentsummaryitem/type)
- [PKPaymentSummaryItemType](/documentation/passkit/pkpaymentsummaryitemtype)

###### Payment summary item types

- [case final](/documentation/passkit/pkpaymentsummaryitemtype/final)
- [case pending](/documentation/passkit/pkpaymentsummaryitemtype/pending)

###### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkpaymentsummaryitemtype/init(rawvalue:))
- [PKRecurringPaymentSummaryItem](/documentation/passkit/pkrecurringpaymentsummaryitem)

##### Setting the payment period

- [var startDate: Date?](/documentation/passkit/pkrecurringpaymentsummaryitem/startdate)
- [var endDate: Date?](/documentation/passkit/pkrecurringpaymentsummaryitem/enddate)

##### Setting the payment interval

- [var intervalUnit: NSCalendar.Unit](/documentation/passkit/pkrecurringpaymentsummaryitem/intervalunit)
- [var intervalCount: Int](/documentation/passkit/pkrecurringpaymentsummaryitem/intervalcount)
- [PKDeferredPaymentSummaryItem](/documentation/passkit/pkdeferredpaymentsummaryitem)

##### Setting the payment date

- [var deferredDate: Date](/documentation/passkit/pkdeferredpaymentsummaryitem/deferreddate)

#### Requesting recurring, automatic, and deferred payments

- [var recurringPaymentRequest: PKRecurringPaymentRequest?](/documentation/passkit/pkpaymentrequest/recurringpaymentrequest)
- [PKRecurringPaymentRequest](/documentation/passkit/pkrecurringpaymentrequest)

##### Creating a recurring payment request

- [init(paymentDescription: String, regularBilling: PKRecurringPaymentSummaryItem, managementURL: URL)](/documentation/passkit/pkrecurringpaymentrequest/init(paymentdescription:regularbilling:managementurl:))

##### Describing a recurring payment

- [var paymentDescription: String](/documentation/passkit/pkrecurringpaymentrequest/paymentdescription)
- [var billingAgreement: String?](/documentation/passkit/pkrecurringpaymentrequest/billingagreement)

##### Setting payment summary items

- [var regularBilling: PKRecurringPaymentSummaryItem](/documentation/passkit/pkrecurringpaymentrequest/regularbilling)
- [var trialBilling: PKRecurringPaymentSummaryItem?](/documentation/passkit/pkrecurringpaymentrequest/trialbilling)
- [PKRecurringPaymentSummaryItem](/documentation/passkit/pkrecurringpaymentsummaryitem)

###### Setting the payment period

- [var startDate: Date?](/documentation/passkit/pkrecurringpaymentsummaryitem/startdate)
- [var endDate: Date?](/documentation/passkit/pkrecurringpaymentsummaryitem/enddate)

###### Setting the payment interval

- [var intervalUnit: NSCalendar.Unit](/documentation/passkit/pkrecurringpaymentsummaryitem/intervalunit)
- [var intervalCount: Int](/documentation/passkit/pkrecurringpaymentsummaryitem/intervalcount)

##### Managing payment tokens

- [var tokenNotificationURL: URL?](/documentation/passkit/pkrecurringpaymentrequest/tokennotificationurl)
- [var managementURL: URL](/documentation/passkit/pkrecurringpaymentrequest/managementurl)
- [var automaticReloadPaymentRequest: PKAutomaticReloadPaymentRequest?](/documentation/passkit/pkpaymentrequest/automaticreloadpaymentrequest)
- [PKAutomaticReloadPaymentRequest](/documentation/passkit/pkautomaticreloadpaymentrequest)

##### Creating an automatic reload payment request

- [init(paymentDescription: String, automaticReloadBilling: PKAutomaticReloadPaymentSummaryItem, managementURL: URL)](/documentation/passkit/pkautomaticreloadpaymentrequest/init(paymentdescription:automaticreloadbilling:managementurl:))

##### Describing an automatic reload payment

- [var paymentDescription: String](/documentation/passkit/pkautomaticreloadpaymentrequest/paymentdescription)
- [var billingAgreement: String?](/documentation/passkit/pkautomaticreloadpaymentrequest/billingagreement)

##### Setting the payment summary items

- [var automaticReloadBilling: PKAutomaticReloadPaymentSummaryItem](/documentation/passkit/pkautomaticreloadpaymentrequest/automaticreloadbilling)
- [PKAutomaticReloadPaymentSummaryItem](/documentation/passkit/pkautomaticreloadpaymentsummaryitem)

###### Setting the automatic reload threshold

- [var thresholdAmount: NSDecimalNumber](/documentation/passkit/pkautomaticreloadpaymentsummaryitem/thresholdamount)

##### Managing payment tokens

- [var managementURL: URL](/documentation/passkit/pkautomaticreloadpaymentrequest/managementurl)
- [var tokenNotificationURL: URL?](/documentation/passkit/pkautomaticreloadpaymentrequest/tokennotificationurl)
- [var deferredPaymentRequest: PKDeferredPaymentRequest?](/documentation/passkit/pkpaymentrequest/deferredpaymentrequest)
- [PKDeferredPaymentRequest](/documentation/passkit/pkdeferredpaymentrequest)

##### Creating a deferred payment request

- [init(paymentDescription: String, deferredBilling: PKDeferredPaymentSummaryItem, managementURL: URL)](/documentation/passkit/pkdeferredpaymentrequest/init(paymentdescription:deferredbilling:managementurl:))

##### Describing a deferred payment

- [var freeCancellationDate: Date?](/documentation/passkit/pkdeferredpaymentrequest/freecancellationdate)
- [var billingAgreement: String?](/documentation/passkit/pkdeferredpaymentrequest/billingagreement)
- [var paymentDescription: String](/documentation/passkit/pkdeferredpaymentrequest/paymentdescription)
- [var freeCancellationDateTimeZone: TimeZone?](/documentation/passkit/pkdeferredpaymentrequest/freecancellationdatetimezone)

##### Setting payment summary items

- [var deferredBilling: PKDeferredPaymentSummaryItem](/documentation/passkit/pkdeferredpaymentrequest/deferredbilling)
- [PKDeferredPaymentSummaryItem](/documentation/passkit/pkdeferredpaymentsummaryitem)

###### Setting the payment date

- [var deferredDate: Date](/documentation/passkit/pkdeferredpaymentsummaryitem/deferreddate)

##### Managing payment tokens

- [var managementURL: URL](/documentation/passkit/pkdeferredpaymentrequest/managementurl)
- [var tokenNotificationURL: URL?](/documentation/passkit/pkdeferredpaymentrequest/tokennotificationurl)

#### Requesting multitoken or multimerchant payments

- [var multiTokenContexts: [PKPaymentTokenContext]](/documentation/passkit/pkpaymentrequest/multitokencontexts)
- [PKPaymentTokenContext](/documentation/passkit/pkpaymenttokencontext)

##### Creating a payment token context

- [init(merchantIdentifier: String, externalIdentifier: String, merchantName: String, merchantDomain: String?, amount: NSDecimalNumber)](/documentation/passkit/pkpaymenttokencontext/init(merchantidentifier:externalidentifier:merchantname:merchantdomain:amount:))

##### Specifying the merchant

- [var merchantIdentifier: String](/documentation/passkit/pkpaymenttokencontext/merchantidentifier)
- [var merchantDomain: String?](/documentation/passkit/pkpaymenttokencontext/merchantdomain)
- [var merchantName: String](/documentation/passkit/pkpaymenttokencontext/merchantname)
- [var externalIdentifier: String](/documentation/passkit/pkpaymenttokencontext/externalidentifier)

##### Indicating a payment amount

- [var amount: NSDecimalNumber](/documentation/passkit/pkpaymenttokencontext/amount)

#### Requesting billing and shipping contact fields

- [var requiredBillingContactFields: Set<PKContactField>](/documentation/passkit/pkpaymentrequest/requiredbillingcontactfields)
- [var requiredShippingContactFields: Set<PKContactField>](/documentation/passkit/pkpaymentrequest/requiredshippingcontactfields)
- [PKContactField](/documentation/passkit/pkcontactfield)

##### Initializing a contact field

- [init(rawValue: String)](/documentation/passkit/pkcontactfield/init(rawvalue:))

##### Types of contact fields

- [static let emailAddress: PKContactField](/documentation/passkit/pkcontactfield/emailaddress)
- [static let name: PKContactField](/documentation/passkit/pkcontactfield/name)
- [static let phoneNumber: PKContactField](/documentation/passkit/pkcontactfield/phonenumber)
- [static let phoneticName: PKContactField](/documentation/passkit/pkcontactfield/phoneticname)
- [static let postalAddress: PKContactField](/documentation/passkit/pkcontactfield/postaladdress)

#### Providing known contact information

- [var billingContact: PKContact?](/documentation/passkit/pkpaymentrequest/billingcontact)
- [var shippingContact: PKContact?](/documentation/passkit/pkpaymentrequest/shippingcontact)
- [PKContact](/documentation/passkit/pkcontact)

##### Contact information

- [var emailAddress: String?](/documentation/passkit/pkcontact/emailaddress)
- [var name: PersonNameComponents?](/documentation/passkit/pkcontact/name)
- [var phoneNumber: CNPhoneNumber?](/documentation/passkit/pkcontact/phonenumber)
- [var postalAddress: CNPostalAddress?](/documentation/passkit/pkcontact/postaladdress)
- [var supplementarySubLocality: String?](/documentation/passkit/pkcontact/supplementarysublocality)

#### Setting the shipping methods and types

- [Displaying a Read-Only Pickup Address](/documentation/passkit/displaying-a-read-only-pickup-address)
- [var shippingMethods: [PKShippingMethod]?](/documentation/passkit/pkpaymentrequest/shippingmethods)
- [PKShippingMethod](/documentation/passkit/pkshippingmethod)

##### Working with shipping methods

- [var detail: String?](/documentation/passkit/pkshippingmethod/detail)
- [var dateComponentsRange: PKDateComponentsRange?](/documentation/passkit/pkshippingmethod/datecomponentsrange)
- [var identifier: String?](/documentation/passkit/pkshippingmethod/identifier)
- [PKDateComponentsRange](/documentation/passkit/pkdatecomponentsrange)

###### Creating a Date Range

- [init?(start: DateComponents, end: DateComponents)](/documentation/passkit/pkdatecomponentsrange/init(start:end:))

###### Reading the Start and End Dates

- [var startDateComponents: DateComponents](/documentation/passkit/pkdatecomponentsrange/startdatecomponents)
- [var endDateComponents: DateComponents](/documentation/passkit/pkdatecomponentsrange/enddatecomponents)
- [var shippingType: PKShippingType](/documentation/passkit/pkpaymentrequest/shippingtype)
- [var shippingContactEditingMode: PKShippingContactEditingMode](/documentation/passkit/pkpaymentrequest/shippingcontacteditingmode)
- [PKShippingType](/documentation/passkit/pkshippingtype)

##### Constants

- [case shipping](/documentation/passkit/pkshippingtype/shipping)
- [case delivery](/documentation/passkit/pkshippingtype/delivery)
- [case storePickup](/documentation/passkit/pkshippingtype/storepickup)
- [case servicePickup](/documentation/passkit/pkshippingtype/servicepickup)

##### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkshippingtype/init(rawvalue:))
- [PKShippingContactEditingMode](/documentation/passkit/pkshippingcontacteditingmode)

##### Reading the editing mode

- [case available](/documentation/passkit/pkshippingcontacteditingmode/available)
- [case storePickup](/documentation/passkit/pkshippingcontacteditingmode/storepickup)

##### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkshippingcontacteditingmode/init(rawvalue:))

##### Type Properties

- [static var enabled: PKShippingContactEditingMode](/documentation/passkit/pkshippingcontacteditingmode/enabled)

#### Working with coupon codes

- [var couponCode: String?](/documentation/passkit/pkpaymentrequest/couponcode)
- [var supportsCouponCode: Bool](/documentation/passkit/pkpaymentrequest/supportscouponcode)

#### Adding custom data

- [var applicationData: Data?](/documentation/passkit/pkpaymentrequest/applicationdata)

#### Providing error information

- [class func paymentBillingAddressInvalidError(withKey: String, localizedDescription: String?) -> any Error](/documentation/passkit/pkpaymentrequest/paymentbillingaddressinvaliderror(withkey:localizeddescription:))
- [class func paymentContactInvalidError(withContactField: PKContactField, localizedDescription: String?) -> any Error](/documentation/passkit/pkpaymentrequest/paymentcontactinvaliderror(withcontactfield:localizeddescription:))
- [class func paymentShippingAddressInvalidError(withKey: String, localizedDescription: String?) -> any Error](/documentation/passkit/pkpaymentrequest/paymentshippingaddressinvaliderror(withkey:localizeddescription:))
- [class func paymentShippingAddressUnserviceableError(withLocalizedDescription: String?) -> any Error](/documentation/passkit/pkpaymentrequest/paymentshippingaddressunserviceableerror(withlocalizeddescription:))
- [static func paymentCouponCodeInvalidError(localizedDescription: String?) -> any Error](/documentation/passkit/pkpaymentrequest/paymentcouponcodeinvaliderror(localizeddescription:))
- [static func paymentCouponCodeExpiredError(localizedDescription: String?) -> any Error](/documentation/passkit/pkpaymentrequest/paymentcouponcodeexpirederror(localizeddescription:))

#### Deprecated

- [static var enabled: PKShippingContactEditingMode](/documentation/passkit/pkshippingcontacteditingmode/enabled)
- [var requiredBillingAddressFields: PKAddressField](/documentation/passkit/pkpaymentrequest/requiredbillingaddressfields)
- [var requiredShippingAddressFields: PKAddressField](/documentation/passkit/pkpaymentrequest/requiredshippingaddressfields)
- [PKAddressField](/documentation/passkit/pkaddressfield)

##### Constants

- [static var postalAddress: PKAddressField](/documentation/passkit/pkaddressfield/postaladdress)
- [static var phone: PKAddressField](/documentation/passkit/pkaddressfield/phone)
- [static var email: PKAddressField](/documentation/passkit/pkaddressfield/email)
- [static var name: PKAddressField](/documentation/passkit/pkaddressfield/name)
- [static var all: PKAddressField](/documentation/passkit/pkaddressfield/all)

##### Initializers

- [init(rawValue: UInt)](/documentation/passkit/pkaddressfield/init(rawvalue:))
- [var billingAddress: ABRecord?](/documentation/passkit/pkpaymentrequest/billingaddress)
- [var shippingAddress: ABRecord?](/documentation/passkit/pkpaymentrequest/shippingaddress)

#### Enumerations

- [PKPaymentRequest.ApplePayLaterAvailability](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum)

##### Availability

- [case unavailable(PKPaymentRequest.ApplePayLaterAvailability.Reason)](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/unavailable(_:))
- [case available](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/available)

##### Transaction availability reasons

- [PKPaymentRequest.ApplePayLaterAvailability.Reason](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/reason)

###### Reasons

- [case itemIneligible](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/reason/itemineligible)
- [case recurringTransaction](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/reason/recurringtransaction)

#### Instance Properties

- [var applePayLaterAvailability: PKPaymentRequest.ApplePayLaterAvailability](/documentation/passkit/pkpaymentrequest/applepaylateravailability-3dxrt)
- [var attributionIdentifier: String?](/documentation/passkit/pkpaymentrequest/attributionidentifier)
- [var merchantCategoryCode: PKPaymentRequest.MerchantCategoryCode?](/documentation/passkit/pkpaymentrequest/merchantcategorycode-9kcn6)
- [PKRecurringPaymentRequest](/documentation/passkit/pkrecurringpaymentrequest)

#### Creating a recurring payment request

- [init(paymentDescription: String, regularBilling: PKRecurringPaymentSummaryItem, managementURL: URL)](/documentation/passkit/pkrecurringpaymentrequest/init(paymentdescription:regularbilling:managementurl:))

#### Describing a recurring payment

- [var paymentDescription: String](/documentation/passkit/pkrecurringpaymentrequest/paymentdescription)
- [var billingAgreement: String?](/documentation/passkit/pkrecurringpaymentrequest/billingagreement)

#### Setting payment summary items

- [var regularBilling: PKRecurringPaymentSummaryItem](/documentation/passkit/pkrecurringpaymentrequest/regularbilling)
- [var trialBilling: PKRecurringPaymentSummaryItem?](/documentation/passkit/pkrecurringpaymentrequest/trialbilling)
- [PKRecurringPaymentSummaryItem](/documentation/passkit/pkrecurringpaymentsummaryitem)

##### Setting the payment period

- [var startDate: Date?](/documentation/passkit/pkrecurringpaymentsummaryitem/startdate)
- [var endDate: Date?](/documentation/passkit/pkrecurringpaymentsummaryitem/enddate)

##### Setting the payment interval

- [var intervalUnit: NSCalendar.Unit](/documentation/passkit/pkrecurringpaymentsummaryitem/intervalunit)
- [var intervalCount: Int](/documentation/passkit/pkrecurringpaymentsummaryitem/intervalcount)

#### Managing payment tokens

- [var tokenNotificationURL: URL?](/documentation/passkit/pkrecurringpaymentrequest/tokennotificationurl)
- [var managementURL: URL](/documentation/passkit/pkrecurringpaymentrequest/managementurl)
- [PKAutomaticReloadPaymentRequest](/documentation/passkit/pkautomaticreloadpaymentrequest)

#### Creating an automatic reload payment request

- [init(paymentDescription: String, automaticReloadBilling: PKAutomaticReloadPaymentSummaryItem, managementURL: URL)](/documentation/passkit/pkautomaticreloadpaymentrequest/init(paymentdescription:automaticreloadbilling:managementurl:))

#### Describing an automatic reload payment

- [var paymentDescription: String](/documentation/passkit/pkautomaticreloadpaymentrequest/paymentdescription)
- [var billingAgreement: String?](/documentation/passkit/pkautomaticreloadpaymentrequest/billingagreement)

#### Setting the payment summary items

- [var automaticReloadBilling: PKAutomaticReloadPaymentSummaryItem](/documentation/passkit/pkautomaticreloadpaymentrequest/automaticreloadbilling)
- [PKAutomaticReloadPaymentSummaryItem](/documentation/passkit/pkautomaticreloadpaymentsummaryitem)

##### Setting the automatic reload threshold

- [var thresholdAmount: NSDecimalNumber](/documentation/passkit/pkautomaticreloadpaymentsummaryitem/thresholdamount)

#### Managing payment tokens

- [var managementURL: URL](/documentation/passkit/pkautomaticreloadpaymentrequest/managementurl)
- [var tokenNotificationURL: URL?](/documentation/passkit/pkautomaticreloadpaymentrequest/tokennotificationurl)
- [PKDeferredPaymentRequest](/documentation/passkit/pkdeferredpaymentrequest)

#### Creating a deferred payment request

- [init(paymentDescription: String, deferredBilling: PKDeferredPaymentSummaryItem, managementURL: URL)](/documentation/passkit/pkdeferredpaymentrequest/init(paymentdescription:deferredbilling:managementurl:))

#### Describing a deferred payment

- [var freeCancellationDate: Date?](/documentation/passkit/pkdeferredpaymentrequest/freecancellationdate)
- [var billingAgreement: String?](/documentation/passkit/pkdeferredpaymentrequest/billingagreement)
- [var paymentDescription: String](/documentation/passkit/pkdeferredpaymentrequest/paymentdescription)
- [var freeCancellationDateTimeZone: TimeZone?](/documentation/passkit/pkdeferredpaymentrequest/freecancellationdatetimezone)

#### Setting payment summary items

- [var deferredBilling: PKDeferredPaymentSummaryItem](/documentation/passkit/pkdeferredpaymentrequest/deferredbilling)
- [PKDeferredPaymentSummaryItem](/documentation/passkit/pkdeferredpaymentsummaryitem)

##### Setting the payment date

- [var deferredDate: Date](/documentation/passkit/pkdeferredpaymentsummaryitem/deferreddate)

#### Managing payment tokens

- [var managementURL: URL](/documentation/passkit/pkdeferredpaymentrequest/managementurl)
- [var tokenNotificationURL: URL?](/documentation/passkit/pkdeferredpaymentrequest/tokennotificationurl)
- [PKPaymentTokenContext](/documentation/passkit/pkpaymenttokencontext)

#### Creating a payment token context

- [init(merchantIdentifier: String, externalIdentifier: String, merchantName: String, merchantDomain: String?, amount: NSDecimalNumber)](/documentation/passkit/pkpaymenttokencontext/init(merchantidentifier:externalidentifier:merchantname:merchantdomain:amount:))

#### Specifying the merchant

- [var merchantIdentifier: String](/documentation/passkit/pkpaymenttokencontext/merchantidentifier)
- [var merchantDomain: String?](/documentation/passkit/pkpaymenttokencontext/merchantdomain)
- [var merchantName: String](/documentation/passkit/pkpaymenttokencontext/merchantname)
- [var externalIdentifier: String](/documentation/passkit/pkpaymenttokencontext/externalidentifier)

#### Indicating a payment amount

- [var amount: NSDecimalNumber](/documentation/passkit/pkpaymenttokencontext/amount)

### Disbursement requests

- [PKDisbursementRequest](/documentation/passkit/pkdisbursementrequest)

#### Initializers

- [convenience init(merchantIdentifier: String, currency: Locale.Currency, region: Locale.Region, supportedNetworks: [PKPaymentNetwork], merchantCapabilities: PKMerchantCapability, summaryItems: [PKPaymentSummaryItem])](/documentation/passkit/pkdisbursementrequest/init(merchantidentifier:currency:region:supportednetworks:merchantcapabilities:summaryitems:))

#### Setting currency and region information

- [var currency: Locale.Currency](/documentation/passkit/pkdisbursementrequest/currency)
- [var region: Locale.Region](/documentation/passkit/pkdisbursementrequest/region)
- [var supportedRegions: [Locale.Region]?](/documentation/passkit/pkdisbursementrequest/supportedregions-1cl0f)

#### Setting the summary items

- [var summaryItems: [PKPaymentSummaryItem]](/documentation/passkit/pkdisbursementrequest/summaryitems)
- [PKPaymentSummaryItem](/documentation/passkit/pkpaymentsummaryitem)

##### Creating  summary items

- [convenience init(label: String, amount: NSDecimalNumber)](/documentation/passkit/pkpaymentsummaryitem/init(label:amount:))
- [convenience init(label: String, amount: NSDecimalNumber, type: PKPaymentSummaryItemType)](/documentation/passkit/pkpaymentsummaryitem/init(label:amount:type:))

##### Describing summary items

- [var label: String](/documentation/passkit/pkpaymentsummaryitem/label)
- [var amount: NSDecimalNumber](/documentation/passkit/pkpaymentsummaryitem/amount)
- [var type: PKPaymentSummaryItemType](/documentation/passkit/pkpaymentsummaryitem/type)
- [PKPaymentSummaryItemType](/documentation/passkit/pkpaymentsummaryitemtype)

###### Payment summary item types

- [case final](/documentation/passkit/pkpaymentsummaryitemtype/final)
- [case pending](/documentation/passkit/pkpaymentsummaryitemtype/pending)

###### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkpaymentsummaryitemtype/init(rawvalue:))
- [PKDisbursementSummaryItem](/documentation/passkit/pkdisbursementsummaryitem)
- [PKInstantFundsOutFeeSummaryItem](/documentation/passkit/pkinstantfundsoutfeesummaryitem)

#### Setting custom application data

- [var applicationData: Data?](/documentation/passkit/pkdisbursementrequest/applicationdata)

#### Setting the merchant information

- [var merchantIdentifier: String](/documentation/passkit/pkdisbursementrequest/merchantidentifier)
- [var merchantCapabilities: PKMerchantCapability](/documentation/passkit/pkdisbursementrequest/merchantcapabilities)
- [var supportedNetworks: [PKPaymentNetwork]](/documentation/passkit/pkdisbursementrequest/supportednetworks)

#### Requesting recipient contact fields

- [var recipientContact: PKContact?](/documentation/passkit/pkdisbursementrequest/recipientcontact)
- [var requiredRecipientContactFields: [PKContactField]](/documentation/passkit/pkdisbursementrequest/requiredrecipientcontactfields)

#### Handling errors

- [class func disbursementCardUnsupportedError() -> any Error](/documentation/passkit/pkdisbursementrequest/disbursementcardunsupportederror())
- [class func disbursementContactInvalidError(withContactField: PKContactField, localizedDescription: String?) -> any Error](/documentation/passkit/pkdisbursementrequest/disbursementcontactinvaliderror(withcontactfield:localizeddescription:))

### Payment sheet interactions and authorization

- [PKPaymentAuthorizationResult](/documentation/passkit/pkpaymentauthorizationresult)

#### Initializing a payment authorization result

- [init(status: PKPaymentAuthorizationStatus, errors: [any Error]?)](/documentation/passkit/pkpaymentauthorizationresult/init(status:errors:))

#### Setting order details

- [var orderDetails: PKPaymentOrderDetails?](/documentation/passkit/pkpaymentauthorizationresult/orderdetails)
- [PKPaymentOrderDetails](/documentation/passkit/pkpaymentorderdetails)

##### Creating payment order details

- [init(orderTypeIdentifier: String, orderIdentifier: String, webServiceURL: URL, authenticationToken: String)](/documentation/passkit/pkpaymentorderdetails/init(ordertypeidentifier:orderidentifier:webserviceurl:authenticationtoken:))

##### Identifying and authenticating the order

- [var authenticationToken: String](/documentation/passkit/pkpaymentorderdetails/authenticationtoken)
- [var orderIdentifier: String](/documentation/passkit/pkpaymentorderdetails/orderidentifier)
- [var orderTypeIdentifier: String](/documentation/passkit/pkpaymentorderdetails/ordertypeidentifier)
- [var webServiceURL: URL](/documentation/passkit/pkpaymentorderdetails/webserviceurl)

#### Setting payment authorization status and errors

- [var errors: [any Error]!](/documentation/passkit/pkpaymentauthorizationresult/errors)
- [var status: PKPaymentAuthorizationStatus](/documentation/passkit/pkpaymentauthorizationresult/status)
- [PKPaymentAuthorizationStatus](/documentation/passkit/pkpaymentauthorizationstatus)

##### Payment authorization status constants

- [case success](/documentation/passkit/pkpaymentauthorizationstatus/success)
- [case failure](/documentation/passkit/pkpaymentauthorizationstatus/failure)
- [case invalidBillingPostalAddress](/documentation/passkit/pkpaymentauthorizationstatus/invalidbillingpostaladdress)
- [case invalidShippingPostalAddress](/documentation/passkit/pkpaymentauthorizationstatus/invalidshippingpostaladdress)
- [case invalidShippingContact](/documentation/passkit/pkpaymentauthorizationstatus/invalidshippingcontact)
- [case pinRequired](/documentation/passkit/pkpaymentauthorizationstatus/pinrequired)
- [case pinIncorrect](/documentation/passkit/pkpaymentauthorizationstatus/pinincorrect)
- [case pinLockout](/documentation/passkit/pkpaymentauthorizationstatus/pinlockout)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaymentauthorizationstatus/init(rawvalue:))
- [PKPaymentOrderDetails](/documentation/passkit/pkpaymentorderdetails)

#### Creating payment order details

- [init(orderTypeIdentifier: String, orderIdentifier: String, webServiceURL: URL, authenticationToken: String)](/documentation/passkit/pkpaymentorderdetails/init(ordertypeidentifier:orderidentifier:webserviceurl:authenticationtoken:))

#### Identifying and authenticating the order

- [var authenticationToken: String](/documentation/passkit/pkpaymentorderdetails/authenticationtoken)
- [var orderIdentifier: String](/documentation/passkit/pkpaymentorderdetails/orderidentifier)
- [var orderTypeIdentifier: String](/documentation/passkit/pkpaymentorderdetails/ordertypeidentifier)
- [var webServiceURL: URL](/documentation/passkit/pkpaymentorderdetails/webserviceurl)
- [PKPaymentAuthorizationController](/documentation/passkit/pkpaymentauthorizationcontroller)

#### Creating a payment authorization controller

- [init(paymentRequest: PKPaymentRequest)](/documentation/passkit/pkpaymentauthorizationcontroller/init(paymentrequest:))
- [convenience init(disbursementRequest: PKDisbursementRequest)](/documentation/passkit/pkpaymentauthorizationcontroller/init(disbursementrequest:))

#### Determining whether the user can make payments or disbursements

- [class func canMakePayments() -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/canmakepayments())
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/canmakepayments(usingnetworks:))
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/canmakepayments(usingnetworks:capabilities:))
- [class func supportsDisbursements() -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/supportsdisbursements())
- [class func supportsDisbursements(using: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/supportsdisbursements(using:))
- [class func supportsDisbursements(using: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationcontroller/supportsdisbursements(using:capabilities:))

#### Handling user interactions

- [var delegate: (any PKPaymentAuthorizationControllerDelegate)?](/documentation/passkit/pkpaymentauthorizationcontroller/delegate)
- [PKPaymentAuthorizationControllerDelegate](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate)

##### Handling user interactions

- [func presentationWindow(for: PKPaymentAuthorizationController) -> UIWindow?](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/presentationwindow(for:))

##### Handling user’s payment method selection

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectPaymentMethod: PKPaymentMethod, handler: (PKPaymentRequestPaymentMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectpaymentmethod:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectPaymentMethod: PKPaymentMethod, completion: ([PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectpaymentmethod:completion:))

##### Handling coupons

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didChangeCouponCode: String, handler: (PKPaymentRequestCouponCodeUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didchangecouponcode:handler:))

##### Handling shipping information

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingContact: PKContact, handler: (PKPaymentRequestShippingContactUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingcontact:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingContact: PKContact, completion: (PKPaymentAuthorizationStatus, [PKShippingMethod], [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingcontact:completion:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingMethod: PKShippingMethod, handler: (PKPaymentRequestShippingMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingmethod:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didSelectShippingMethod: PKShippingMethod, completion: (PKPaymentAuthorizationStatus, [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didselectshippingmethod:completion:))

##### Handling user’s payment authorization

- [func paymentAuthorizationController(PKPaymentAuthorizationController, didRequestMerchantSessionUpdate: (PKPaymentRequestMerchantSessionUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didrequestmerchantsessionupdate:))
- [func paymentAuthorizationControllerWillAuthorizePayment(PKPaymentAuthorizationController)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontrollerwillauthorizepayment(_:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didAuthorizePayment: PKPayment, handler: (PKPaymentAuthorizationResult) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didauthorizepayment:handler:))
- [func paymentAuthorizationController(PKPaymentAuthorizationController, didAuthorizePayment: PKPayment, completion: (PKPaymentAuthorizationStatus) -> Void)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontroller(_:didauthorizepayment:completion:))
- [func paymentAuthorizationControllerDidFinish(PKPaymentAuthorizationController)](/documentation/passkit/pkpaymentauthorizationcontrollerdelegate/paymentauthorizationcontrollerdidfinish(_:))
- [func present(completion: ((Bool) -> Void)?)](/documentation/passkit/pkpaymentauthorizationcontroller/present(completion:))
- [func dismiss(completion: (() -> Void)?)](/documentation/passkit/pkpaymentauthorizationcontroller/dismiss(completion:))
- [PKPaymentAuthorizationViewController](/documentation/passkit/pkpaymentauthorizationviewcontroller)

#### Determining whether the user can make payments

- [class func canMakePayments() -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/canmakepayments())
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/canmakepayments(usingnetworks:))
- [class func canMakePayments(usingNetworks: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/canmakepayments(usingnetworks:capabilities:))
- [class func supportsDisbursements() -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/supportsdisbursements())
- [class func supportsDisbursements(using: [PKPaymentNetwork]) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/supportsdisbursements(using:))
- [class func supportsDisbursements(using: [PKPaymentNetwork], capabilities: PKMerchantCapability) -> Bool](/documentation/passkit/pkpaymentauthorizationviewcontroller/supportsdisbursements(using:capabilities:))

#### Handling user interactions

- [var delegate: (any PKPaymentAuthorizationViewControllerDelegate)?](/documentation/passkit/pkpaymentauthorizationviewcontroller/delegate)
- [PKPaymentAuthorizationViewControllerDelegate](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate)

##### Handling user’s payment authorization

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didRequestMerchantSessionUpdate: (PKPaymentRequestMerchantSessionUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didrequestmerchantsessionupdate:))
- [func paymentAuthorizationViewControllerWillAuthorizePayment(PKPaymentAuthorizationViewController)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontrollerwillauthorizepayment(_:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didAuthorizePayment: PKPayment, handler: (PKPaymentAuthorizationResult) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didauthorizepayment:handler:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didAuthorizePayment: PKPayment, completion: (PKPaymentAuthorizationStatus) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didauthorizepayment:completion:))
- [func paymentAuthorizationViewControllerDidFinish(PKPaymentAuthorizationViewController)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontrollerdidfinish(_:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKPaymentMethod, handler: (PKPaymentRequestPaymentMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:handler:)-3bex6)
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKPaymentMethod, completion: ([PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:completion:)-30s85)

##### Handling coupons

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didChangeCouponCode: String, handler: (PKPaymentRequestCouponCodeUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didchangecouponcode:handler:))

##### Handling shipping information

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelectShippingContact: PKContact, handler: (PKPaymentRequestShippingContactUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselectshippingcontact:handler:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelectShippingContact: PKContact, completion: (PKPaymentAuthorizationStatus, [PKShippingMethod], [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselectshippingcontact:completion:))
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKShippingMethod, handler: (PKPaymentRequestShippingMethodUpdate) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:handler:)-5r0i7)
- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelect: PKShippingMethod, completion: (PKPaymentAuthorizationStatus, [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselect:completion:)-9otrj)

##### Deprecated

- [func paymentAuthorizationViewController(PKPaymentAuthorizationViewController, didSelectShippingAddress: ABRecord, completion: (PKPaymentAuthorizationStatus, [PKShippingMethod], [PKPaymentSummaryItem]) -> Void)](/documentation/passkit/pkpaymentauthorizationviewcontrollerdelegate/paymentauthorizationviewcontroller(_:didselectshippingaddress:completion:))

#### Creating a payment authorization view controller

- [init?(paymentRequest: PKPaymentRequest)](/documentation/passkit/pkpaymentauthorizationviewcontroller/init(paymentrequest:))
- [convenience init(disbursementRequest: PKDisbursementRequest)](/documentation/passkit/pkpaymentauthorizationviewcontroller/init(disbursementrequest:))
- [PKPayment](/documentation/passkit/pkpayment)

#### Working with the payment token

- [var token: PKPaymentToken](/documentation/passkit/pkpayment/token)
- [PKPaymentToken](/documentation/passkit/pkpaymenttoken)

##### Working with payment tokens

- [var paymentData: Data](/documentation/passkit/pkpaymenttoken/paymentdata)
- [var paymentMethod: PKPaymentMethod](/documentation/passkit/pkpaymenttoken/paymentmethod)
- [PKPaymentMethod](/documentation/passkit/pkpaymentmethod)

###### Getting the pass

- [var secureElementPass: PKSecureElementPass?](/documentation/passkit/pkpaymentmethod/secureelementpass)
- [var paymentPass: PKPaymentPass?](/documentation/passkit/pkpaymentmethod/paymentpass)

###### Getting the payment method’s attributes

- [var type: PKPaymentMethodType](/documentation/passkit/pkpaymentmethod/type)
- [PKPaymentMethodType](/documentation/passkit/pkpaymentmethodtype)

###### Payment Method Type Constants

- [case unknown](/documentation/passkit/pkpaymentmethodtype/unknown)
- [case debit](/documentation/passkit/pkpaymentmethodtype/debit)
- [case eMoney](/documentation/passkit/pkpaymentmethodtype/emoney)
- [case credit](/documentation/passkit/pkpaymentmethodtype/credit)
- [case prepaid](/documentation/passkit/pkpaymentmethodtype/prepaid)
- [case store](/documentation/passkit/pkpaymentmethodtype/store)

###### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkpaymentmethodtype/init(rawvalue:))
- [var displayName: String?](/documentation/passkit/pkpaymentmethod/displayname)
- [var network: PKPaymentNetwork?](/documentation/passkit/pkpaymentmethod/network)
- [var billingAddress: CNContact?](/documentation/passkit/pkpaymentmethod/billingaddress)
- [var transactionIdentifier: String](/documentation/passkit/pkpaymenttoken/transactionidentifier)

##### Deprecated

- [var paymentNetwork: String](/documentation/passkit/pkpaymenttoken/paymentnetwork)
- [var paymentInstrumentName: String](/documentation/passkit/pkpaymenttoken/paymentinstrumentname)

#### Working with billing and shipping information

- [var billingContact: PKContact?](/documentation/passkit/pkpayment/billingcontact)
- [var shippingContact: PKContact?](/documentation/passkit/pkpayment/shippingcontact)
- [var shippingMethod: PKShippingMethod?](/documentation/passkit/pkpayment/shippingmethod)
- [PKContact](/documentation/passkit/pkcontact)

##### Contact information

- [var emailAddress: String?](/documentation/passkit/pkcontact/emailaddress)
- [var name: PersonNameComponents?](/documentation/passkit/pkcontact/name)
- [var phoneNumber: CNPhoneNumber?](/documentation/passkit/pkcontact/phonenumber)
- [var postalAddress: CNPostalAddress?](/documentation/passkit/pkcontact/postaladdress)
- [var supplementarySubLocality: String?](/documentation/passkit/pkcontact/supplementarysublocality)
- [PKShippingMethod](/documentation/passkit/pkshippingmethod)

##### Working with shipping methods

- [var detail: String?](/documentation/passkit/pkshippingmethod/detail)
- [var dateComponentsRange: PKDateComponentsRange?](/documentation/passkit/pkshippingmethod/datecomponentsrange)
- [var identifier: String?](/documentation/passkit/pkshippingmethod/identifier)
- [PKDateComponentsRange](/documentation/passkit/pkdatecomponentsrange)

###### Creating a Date Range

- [init?(start: DateComponents, end: DateComponents)](/documentation/passkit/pkdatecomponentsrange/init(start:end:))

###### Reading the Start and End Dates

- [var startDateComponents: DateComponents](/documentation/passkit/pkdatecomponentsrange/startdatecomponents)
- [var endDateComponents: DateComponents](/documentation/passkit/pkdatecomponentsrange/enddatecomponents)

#### Deprecated

- [var billingAddress: ABRecord?](/documentation/passkit/pkpayment/billingaddress)
- [var shippingAddress: ABRecord?](/documentation/passkit/pkpayment/shippingaddress)

### Payment sheet updates

- [PKPaymentRequestMerchantSessionUpdate](/documentation/passkit/pkpaymentrequestmerchantsessionupdate)

#### Creating a merchant session update

- [init(status: PKPaymentAuthorizationStatus, merchantSession: PKPaymentMerchantSession?)](/documentation/passkit/pkpaymentrequestmerchantsessionupdate/init(status:merchantsession:))

#### Getting information for the merchant session update

- [var status: PKPaymentAuthorizationStatus](/documentation/passkit/pkpaymentrequestmerchantsessionupdate/status)
- [var session: PKPaymentMerchantSession?](/documentation/passkit/pkpaymentrequestmerchantsessionupdate/session)
- [PKPaymentMerchantSession](/documentation/passkit/pkpaymentmerchantsession)

##### Creating a merchant session

- [init(dictionary: [AnyHashable : Any])](/documentation/passkit/pkpaymentmerchantsession/init(dictionary:))
- [PKPaymentRequestPaymentMethodUpdate](/documentation/passkit/pkpaymentrequestpaymentmethodupdate)

#### Creating a payment request update

- [init(errors: [any Error]?, paymentSummaryItems: [PKPaymentSummaryItem])](/documentation/passkit/pkpaymentrequestpaymentmethodupdate/init(errors:paymentsummaryitems:))

#### Getting user errors

- [var errors: [any Error]!](/documentation/passkit/pkpaymentrequestpaymentmethodupdate/errors)
- [PKPaymentRequestShippingContactUpdate](/documentation/passkit/pkpaymentrequestshippingcontactupdate)

#### Creating a shipping contact update

- [init(errors: [any Error]?, paymentSummaryItems: [PKPaymentSummaryItem], shippingMethods: [PKShippingMethod])](/documentation/passkit/pkpaymentrequestshippingcontactupdate/init(errors:paymentsummaryitems:shippingmethods:))

#### Updating user errors and shipping methods

- [var errors: [any Error]!](/documentation/passkit/pkpaymentrequestshippingcontactupdate/errors)
- [var shippingMethods: [PKShippingMethod]](/documentation/passkit/pkpaymentrequestshippingcontactupdate/shippingmethods)
- [PKPaymentRequestShippingMethodUpdate](/documentation/passkit/pkpaymentrequestshippingmethodupdate)
- [PKPaymentRequestCouponCodeUpdate](/documentation/passkit/pkpaymentrequestcouponcodeupdate)

#### Creating a payment coupon update object

- [init(errors: [any Error]?, paymentSummaryItems: [PKPaymentSummaryItem], shippingMethods: [PKShippingMethod])](/documentation/passkit/pkpaymentrequestcouponcodeupdate/init(errors:paymentsummaryitems:shippingmethods:))

#### Reading errors

- [var errors: [any Error]!](/documentation/passkit/pkpaymentrequestcouponcodeupdate/errors)
- [PKPaymentRequestUpdate](/documentation/passkit/pkpaymentrequestupdate)

#### Creating a payment request update

- [init(paymentSummaryItems: [PKPaymentSummaryItem])](/documentation/passkit/pkpaymentrequestupdate/init(paymentsummaryitems:))

#### Updating authorization status

- [var status: PKPaymentAuthorizationStatus](/documentation/passkit/pkpaymentrequestupdate/status)
- [PKPaymentAuthorizationStatus](/documentation/passkit/pkpaymentauthorizationstatus)

##### Payment authorization status constants

- [case success](/documentation/passkit/pkpaymentauthorizationstatus/success)
- [case failure](/documentation/passkit/pkpaymentauthorizationstatus/failure)
- [case invalidBillingPostalAddress](/documentation/passkit/pkpaymentauthorizationstatus/invalidbillingpostaladdress)
- [case invalidShippingPostalAddress](/documentation/passkit/pkpaymentauthorizationstatus/invalidshippingpostaladdress)
- [case invalidShippingContact](/documentation/passkit/pkpaymentauthorizationstatus/invalidshippingcontact)
- [case pinRequired](/documentation/passkit/pkpaymentauthorizationstatus/pinrequired)
- [case pinIncorrect](/documentation/passkit/pkpaymentauthorizationstatus/pinincorrect)
- [case pinLockout](/documentation/passkit/pkpaymentauthorizationstatus/pinlockout)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaymentauthorizationstatus/init(rawvalue:))

#### Updating summary items

- [var paymentSummaryItems: [PKPaymentSummaryItem]](/documentation/passkit/pkpaymentrequestupdate/paymentsummaryitems)
- [PKPaymentSummaryItem](/documentation/passkit/pkpaymentsummaryitem)

##### Creating  summary items

- [convenience init(label: String, amount: NSDecimalNumber)](/documentation/passkit/pkpaymentsummaryitem/init(label:amount:))
- [convenience init(label: String, amount: NSDecimalNumber, type: PKPaymentSummaryItemType)](/documentation/passkit/pkpaymentsummaryitem/init(label:amount:type:))

##### Describing summary items

- [var label: String](/documentation/passkit/pkpaymentsummaryitem/label)
- [var amount: NSDecimalNumber](/documentation/passkit/pkpaymentsummaryitem/amount)
- [var type: PKPaymentSummaryItemType](/documentation/passkit/pkpaymentsummaryitem/type)
- [PKPaymentSummaryItemType](/documentation/passkit/pkpaymentsummaryitemtype)

###### Payment summary item types

- [case final](/documentation/passkit/pkpaymentsummaryitemtype/final)
- [case pending](/documentation/passkit/pkpaymentsummaryitemtype/pending)

###### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkpaymentsummaryitemtype/init(rawvalue:))

#### Updating shipping methods

- [var shippingMethods: [PKShippingMethod]](/documentation/passkit/pkpaymentrequestupdate/shippingmethods)

#### Updating automatic reload payments

- [var automaticReloadPaymentRequest: PKAutomaticReloadPaymentRequest?](/documentation/passkit/pkpaymentrequestupdate/automaticreloadpaymentrequest)

#### Updating multitoken or multimerchant payments

- [var multiTokenContexts: [PKPaymentTokenContext]?](/documentation/passkit/pkpaymentrequestupdate/multitokencontexts)

#### Updating recurring payments

- [var recurringPaymentRequest: PKRecurringPaymentRequest?](/documentation/passkit/pkpaymentrequestupdate/recurringpaymentrequest)

#### Setting up a deferred payment request

- [var deferredPaymentRequest: PKDeferredPaymentRequest?](/documentation/passkit/pkpaymentrequestupdate/deferredpaymentrequest)

### QR transaction information

- [PKPaymentInformationEventExtension](/documentation/passkit/pkpaymentinformationeventextension)
- [PKPaymentInformationRequestHandling](/documentation/passkit/pkpaymentinformationrequesthandling)

#### Getting the transaction information

- [func handle(PKBarcodeEventConfigurationRequest, completion: () -> Void)](/documentation/passkit/pkpaymentinformationrequesthandling/handle(_:completion:)-3cth8)
- [func handleInformationRequest(PKBarcodeEventMetadataRequest, completion: (PKBarcodeEventMetadataResponse) -> Void)](/documentation/passkit/pkpaymentinformationrequesthandling/handleinformationrequest(_:completion:))
- [PKBarcodeEventConfigurationRequest](/documentation/passkit/pkbarcodeeventconfigurationrequest)

##### Reading Configuration Information

- [var deviceAccountIdentifier: String](/documentation/passkit/pkbarcodeeventconfigurationrequest/deviceaccountidentifier)
- [var configurationDataType: PKBarcodeEventConfigurationDataType](/documentation/passkit/pkbarcodeeventconfigurationrequest/configurationdatatype)
- [var configurationData: Data](/documentation/passkit/pkbarcodeeventconfigurationrequest/configurationdata)
- [PKBarcodeEventConfigurationDataType](/documentation/passkit/pkbarcodeeventconfigurationdatatype)

###### QR Code Purchase Signing Types

- [case signingCertificate](/documentation/passkit/pkbarcodeeventconfigurationdatatype/signingcertificate)
- [case signingKeyMaterial](/documentation/passkit/pkbarcodeeventconfigurationdatatype/signingkeymaterial)
- [case unknown](/documentation/passkit/pkbarcodeeventconfigurationdatatype/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkbarcodeeventconfigurationdatatype/init(rawvalue:))
- [PKBarcodeEventMetadataRequest](/documentation/passkit/pkbarcodeeventmetadatarequest)

##### Getting QR Purchase Metadata

- [var deviceAccountIdentifier: String](/documentation/passkit/pkbarcodeeventmetadatarequest/deviceaccountidentifier)
- [var lastUsedBarcodeIdentifier: String](/documentation/passkit/pkbarcodeeventmetadatarequest/lastusedbarcodeidentifier)
- [PKBarcodeEventMetadataResponse](/documentation/passkit/pkbarcodeeventmetadataresponse)

##### Creating an Event Metadata Response

- [init(paymentInformation: Data)](/documentation/passkit/pkbarcodeeventmetadataresponse/init(paymentinformation:))

##### Getting QR Payment Information

- [var paymentInformation: Data](/documentation/passkit/pkbarcodeeventmetadataresponse/paymentinformation)
- [PKInformationRequestCompletionBlock](/documentation/passkit/pkinformationrequestcompletionblock)

#### Signing the transaction

- [func handle(PKBarcodeEventSignatureRequest, completion: (PKBarcodeEventSignatureResponse) -> Void)](/documentation/passkit/pkpaymentinformationrequesthandling/handle(_:completion:)-18x2y)
- [PKBarcodeEventSignatureRequest](/documentation/passkit/pkbarcodeeventsignaturerequest)

##### Getting Transaction Details

- [var amount: NSNumber](/documentation/passkit/pkbarcodeeventsignaturerequest/amount)
- [var currencyCode: String](/documentation/passkit/pkbarcodeeventsignaturerequest/currencycode)
- [var transactionDate: Date](/documentation/passkit/pkbarcodeeventsignaturerequest/transactiondate)
- [var transactionIdentifier: String](/documentation/passkit/pkbarcodeeventsignaturerequest/transactionidentifier)
- [var transactionStatus: String](/documentation/passkit/pkbarcodeeventsignaturerequest/transactionstatus)
- [var merchantName: String](/documentation/passkit/pkbarcodeeventsignaturerequest/merchantname)
- [var rawMerchantName: String](/documentation/passkit/pkbarcodeeventsignaturerequest/rawmerchantname)

##### Getting Signing Information

- [var partialSignature: Data](/documentation/passkit/pkbarcodeeventsignaturerequest/partialsignature)
- [var barcodeIdentifier: String](/documentation/passkit/pkbarcodeeventsignaturerequest/barcodeidentifier)
- [var deviceAccountIdentifier: String](/documentation/passkit/pkbarcodeeventsignaturerequest/deviceaccountidentifier)
- [PKBarcodeEventSignatureResponse](/documentation/passkit/pkbarcodeeventsignatureresponse)

##### Creating a Signature Response

- [init(signedData: Data)](/documentation/passkit/pkbarcodeeventsignatureresponse/init(signeddata:))

##### Returning the Signature

- [var signedData: Data](/documentation/passkit/pkbarcodeeventsignatureresponse/signeddata)
- [PKSignatureRequestCompletionBlock](/documentation/passkit/pksignaturerequestcompletionblock)

### Entitlements

- [Merchant IDs Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.in-app-payments)

### Payment token format

- [Payment token format reference](/documentation/passkit/payment-token-format-reference)

#### Symmetric keys

- [Restoring the symmetric key](/documentation/passkit/restoring-the-symmetric-key)

### Errors

- [PKDisbursementError](/documentation/passkit/pkdisbursementerror)

#### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/passkit_apple_pay_and_wallet/pkdisbursementerror/4156691-init)

#### Error details

- [PKDisbursementError.Code](/documentation/passkit/pkdisbursementerror/code)

##### Error codes

- [case recipientContactInvalidError](/documentation/passkit/pkdisbursementerror/code/recipientcontactinvaliderror)
- [case unsupportedCardError](/documentation/passkit/pkdisbursementerror/code/unsupportedcarderror)
- [case unknownError](/documentation/passkit/pkdisbursementerror/code/unknownerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkdisbursementerror/code/init(rawvalue:))
- [var errorCode: Int](/documentation/foundation/customnserror/errorcode-2opgi)
- [var errorUserInfo: [String : Any]](/documentation/foundation/customnserror/erroruserinfo-1aas5)
- [var hashValue: Int](/documentation/passkit_apple_pay_and_wallet/pkdisbursementerror/4156690-hashvalue)
- [var userInfo: [String : Any]](/documentation/passkit_apple_pay_and_wallet/pkdisbursementerror/4156696-userinfo)

#### Type properties

- [static var recipientContactInvalidError: PKDisbursementError.Code](/documentation/passkit/pkdisbursementerror/recipientcontactinvaliderror)
- [static var unknownError: PKDisbursementError.Code](/documentation/passkit/pkdisbursementerror/unknownerror)
- [static var unsupportedCardError: PKDisbursementError.Code](/documentation/passkit/pkdisbursementerror/unsupportedcarderror)

#### Utility methods

- [func hash(into: inout Hasher)](/documentation/passkit_apple_pay_and_wallet/pkdisbursementerror/4156689-hash)
- [static func == (PKDisbursementError, PKDisbursementError) -> Bool](/documentation/passkit_apple_pay_and_wallet/pkdisbursementerror/4156684)

#### Type Properties

- [static var errorDomain: String](/documentation/passkit/pkdisbursementerror/errordomain)
- [PKDisbursementErrorKey](/documentation/passkit/pkdisbursementerrorkey)

#### Initializers

- [init(rawValue: String)](/documentation/passkit/pkdisbursementerrorkey/init(rawvalue:))

#### Type properties

- [static let contactFieldUserInfoKey: PKDisbursementErrorKey](/documentation/passkit/pkdisbursementerrorkey/contactfielduserinfokey)
- [PKPaymentError](/documentation/passkit/pkpaymenterror)

#### Creating a payment error object

- [init(Code, userInfo: [String : Any])](/documentation/passkit_apple_pay_and_wallet/pkpaymenterror/3727675-init)

#### Describing the error

- [var errorCode: Int](/documentation/foundation/customnserror/errorcode-2opgi)
- [var userInfo: [String : Any]](/documentation/passkit_apple_pay_and_wallet/pkpaymenterror/3727676-userinfo)
- [var errorUserInfo: [String : Any]](/documentation/foundation/customnserror/erroruserinfo-1aas5)

#### Identifying the error

- [static var billingContactInvalidError: PKPaymentError.Code](/documentation/passkit/pkpaymenterror/billingcontactinvaliderror)
- [static var shippingContactInvalidError: PKPaymentError.Code](/documentation/passkit/pkpaymenterror/shippingcontactinvaliderror)
- [static var shippingAddressUnserviceableError: PKPaymentError.Code](/documentation/passkit/pkpaymenterror/shippingaddressunserviceableerror)
- [static var couponCodeExpiredError: PKPaymentError.Code](/documentation/passkit/pkpaymenterror/couponcodeexpirederror)
- [static var couponCodeInvalidError: PKPaymentError.Code](/documentation/passkit/pkpaymenterror/couponcodeinvaliderror)
- [static var unknownError: PKPaymentError.Code](/documentation/passkit/pkpaymenterror/unknownerror)
- [PKPaymentError.Code](/documentation/passkit/pkpaymenterror/code)

##### Error codes

- [case couponCodeExpiredError](/documentation/passkit/pkpaymenterror/code/couponcodeexpirederror)
- [case couponCodeInvalidError](/documentation/passkit/pkpaymenterror/code/couponcodeinvaliderror)
- [case billingContactInvalidError](/documentation/passkit/pkpaymenterror/code/billingcontactinvaliderror)
- [case shippingContactInvalidError](/documentation/passkit/pkpaymenterror/code/shippingcontactinvaliderror)
- [case shippingAddressUnserviceableError](/documentation/passkit/pkpaymenterror/code/shippingaddressunserviceableerror)
- [case unknownError](/documentation/passkit/pkpaymenterror/code/unknownerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaymenterror/code/init(rawvalue:))

#### Querying the error domain

- [let PKPaymentErrorDomain: String](/documentation/passkit/pkpaymenterrordomain)

#### Comparing errors

- [static func == (PKPaymentError, PKPaymentError) -> Bool](/documentation/passkit_apple_pay_and_wallet/pkpaymenterror/3727671)

#### Hashing

- [func hash(into: inout Hasher)](/documentation/passkit_apple_pay_and_wallet/pkpaymenterror/3727673-hash)
- [var hashValue: Int](/documentation/passkit_apple_pay_and_wallet/pkpaymenterror/3727674-hashvalue)

#### Type Properties

- [static var errorDomain: String](/documentation/passkit/pkpaymenterror/errordomain)
- [PKPaymentError.Code](/documentation/passkit/pkpaymenterror/code)

#### Error codes

- [case couponCodeExpiredError](/documentation/passkit/pkpaymenterror/code/couponcodeexpirederror)
- [case couponCodeInvalidError](/documentation/passkit/pkpaymenterror/code/couponcodeinvaliderror)
- [case billingContactInvalidError](/documentation/passkit/pkpaymenterror/code/billingcontactinvaliderror)
- [case shippingContactInvalidError](/documentation/passkit/pkpaymenterror/code/shippingcontactinvaliderror)
- [case shippingAddressUnserviceableError](/documentation/passkit/pkpaymenterror/code/shippingaddressunserviceableerror)
- [case unknownError](/documentation/passkit/pkpaymenterror/code/unknownerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaymenterror/code/init(rawvalue:))
- [PKPaymentErrorKey](/documentation/passkit/pkpaymenterrorkey)

#### Initializing a payment error key

- [init(rawValue: String)](/documentation/passkit/pkpaymenterrorkey/init(rawvalue:))

#### Error keys

- [static let postalAddressUserInfoKey: PKPaymentErrorKey](/documentation/passkit/pkpaymenterrorkey/postaladdressuserinfokey)
- [static let contactFieldUserInfoKey: PKPaymentErrorKey](/documentation/passkit/pkpaymenterrorkey/contactfielduserinfokey)
- [PKDisbursementError.Code](/documentation/passkit/pkdisbursementerror/code)

#### Error codes

- [case recipientContactInvalidError](/documentation/passkit/pkdisbursementerror/code/recipientcontactinvaliderror)
- [case unsupportedCardError](/documentation/passkit/pkdisbursementerror/code/unsupportedcarderror)
- [case unknownError](/documentation/passkit/pkdisbursementerror/code/unknownerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkdisbursementerror/code/init(rawvalue:))
- [let PKPaymentErrorDomain: String](/documentation/passkit/pkpaymenterrordomain)
- [let PKDisbursementErrorDomain: String](/documentation/passkit/pkdisbursementerrordomain)

### Deprecated

- [var applePayLaterAvailability: PKPaymentRequest.ApplePayLaterAvailability](/documentation/passkit/pkpaymentrequest/applepaylateravailability-3dxrt)
- [PKPaymentRequest.ApplePayLaterAvailability](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum)

#### Availability

- [case unavailable(PKPaymentRequest.ApplePayLaterAvailability.Reason)](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/unavailable(_:))
- [case available](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/available)

#### Transaction availability reasons

- [PKPaymentRequest.ApplePayLaterAvailability.Reason](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/reason)

##### Reasons

- [case itemIneligible](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/reason/itemineligible)
- [case recurringTransaction](/documentation/passkit/pkpaymentrequest/applepaylateravailability-swift.enum/reason/recurringtransaction)
- [PKAddressField](/documentation/passkit/pkaddressfield)

#### Constants

- [static var postalAddress: PKAddressField](/documentation/passkit/pkaddressfield/postaladdress)
- [static var phone: PKAddressField](/documentation/passkit/pkaddressfield/phone)
- [static var email: PKAddressField](/documentation/passkit/pkaddressfield/email)
- [static var name: PKAddressField](/documentation/passkit/pkaddressfield/name)
- [static var all: PKAddressField](/documentation/passkit/pkaddressfield/all)

#### Initializers

- [init(rawValue: UInt)](/documentation/passkit/pkaddressfield/init(rawvalue:))
- [PKApplePayLaterAvailability](/documentation/passkit/pkapplepaylateravailability)

#### Availability values

- [case available](/documentation/passkit/pkapplepaylateravailability/available)
- [case unavailableItemIneligible](/documentation/passkit/pkapplepaylateravailability/unavailableitemineligible)
- [case unavailableRecurringTransaction](/documentation/passkit/pkapplepaylateravailability/unavailablerecurringtransaction)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkapplepaylateravailability/init(rawvalue:))

## Wallet support

- [Wallet](/documentation/passkit/wallet)

### Essentials

- [Pass Type IDs Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.pass-type-identifiers)
- [Merchant IDs Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.in-app-payments)
- [com.apple.developer.in-app-identity-presentment](/documentation/bundleresources/entitlements/com.apple.developer.in-app-identity-presentment)
- [Requesting identity data from a Wallet pass](/documentation/passkit/requesting-identity-data-from-a-wallet-pass)
- [Verifying Wallet identity requests](/documentation/passkit/verifying-wallet-identity-requests)

### Wallet Passes

- [Wallet Passes](/documentation/walletpasses)

### Common data types

- [PKObject](/documentation/passkit/pkobject)
- [PKAddPassButton](/documentation/passkit/pkaddpassbutton)

#### Creating add pass buttons

- [init(addPassButtonStyle: PKAddPassButtonStyle)](/documentation/passkit/pkaddpassbutton/init(addpassbuttonstyle:))

#### Accessing the button’s style

- [var addPassButtonStyle: PKAddPassButtonStyle](/documentation/passkit/pkaddpassbutton/addpassbuttonstyle)

#### Button styles

- [PKAddPassButtonStyle](/documentation/passkit/pkaddpassbuttonstyle)

##### Constants

- [case black](/documentation/passkit/pkaddpassbuttonstyle/black)
- [case blackOutline](/documentation/passkit/pkaddpassbuttonstyle/blackoutline)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddpassbuttonstyle/init(rawvalue:))
- [PKLabeledValue](/documentation/passkit/pklabeledvalue)

#### Creating a labeled value

- [init(label: String, value: String)](/documentation/passkit/pklabeledvalue/init(label:value:))

#### Labeled value properties

- [var label: String](/documentation/passkit/pklabeledvalue/label)
- [var value: String](/documentation/passkit/pklabeledvalue/value)
- [AddPassToWalletButton](/documentation/passkit/addpasstowalletbutton)

#### Creating the button

- [init(PKEncryptionScheme, cardholderName: String, passStyle: PKAddPaymentPassStyle, primaryAccountSuffix: String?, cardDetails: [PKLabeledValue]?, description: String?, filters: [AddPassToWalletButtonFilter], onRequest: (AddPassToWalletButtonResponse) async -> PKAddPaymentPassRequest, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void)](/documentation/passkit/addpasstowalletbutton/init(_:cardholdername:passstyle:primaryaccountsuffix:carddetails:description:filters:onrequest:oncompletion:))
- [init(PKEncryptionScheme, cardholderName: String, passStyle: PKAddPaymentPassStyle, primaryAccountSuffix: String?, cardDetails: [PKLabeledValue]?, description: String?, filters: [AddPassToWalletButtonFilter], onRequest: (AddPassToWalletButtonResponse) async -> PKAddPaymentPassRequest, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void, fallback: () -> Fallback)](/documentation/passkit/addpasstowalletbutton/init(_:cardholdername:passstyle:primaryaccountsuffix:carddetails:description:filters:onrequest:oncompletion:fallback:))
- [init([PKPass], onCompletion: (Bool) -> Void)](/documentation/passkit/addpasstowalletbutton/init(_:oncompletion:)-1inhj)
- [init(PKAddSecureElementPassConfiguration, onCompletion: (Result<[PKSecureElementPass], any Error>) -> Void)](/documentation/passkit/addpasstowalletbutton/init(_:oncompletion:)-5wkyi)
- [init([PKPass], onCompletion: (Bool) -> Void, fallback: () -> Fallback)](/documentation/passkit/addpasstowalletbutton/init(_:oncompletion:fallback:)-77t5g)
- [init(PKAddSecureElementPassConfiguration, onCompletion: (Result<[PKSecureElementPass], any Error>) -> Void, fallback: () -> Fallback)](/documentation/passkit/addpasstowalletbutton/init(_:oncompletion:fallback:)-7adn5)
- [init(PKAddPaymentPassRequestConfiguration, onRequest: (AddPassToWalletButtonResponse) async -> PKAddPaymentPassRequest, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void)](/documentation/passkit/addpasstowalletbutton/init(_:onrequest:oncompletion:))
- [init(PKAddPaymentPassRequestConfiguration, onRequest: (AddPassToWalletButtonResponse) async -> PKAddPaymentPassRequest, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void, fallback: () -> Fallback)](/documentation/passkit/addpasstowalletbutton/init(_:onrequest:oncompletion:fallback:))
- [init(PKEncryptionScheme, primaryAccountSuffix: String, passStyle: PKAddPaymentPassStyle, cardDetails: [PKLabeledValue]?, description: String?, filters: [AddPassToWalletButtonFilter], onRequest: (AddPassToWalletButtonResponse) async -> PKAddPaymentPassRequest, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void)](/documentation/passkit/addpasstowalletbutton/init(_:primaryaccountsuffix:passstyle:carddetails:description:filters:onrequest:oncompletion:))
- [init(PKEncryptionScheme, primaryAccountSuffix: String, passStyle: PKAddPaymentPassStyle, cardDetails: [PKLabeledValue]?, description: String?, filters: [AddPassToWalletButtonFilter], onRequest: (AddPassToWalletButtonResponse) async -> PKAddPaymentPassRequest, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void, fallback: () -> Fallback)](/documentation/passkit/addpasstowalletbutton/init(_:primaryaccountsuffix:passstyle:carddetails:description:filters:onrequest:oncompletion:fallback:))
- [init(action: () -> Void)](/documentation/passkit/addpasstowalletbutton/init(action:))
- [init(carKeyPassword: String, supportedRadioTechnologies: PKRadioTechnology, issuerIdentifier: String, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void)](/documentation/passkit/addpasstowalletbutton/init(carkeypassword:supportedradiotechnologies:issueridentifier:oncompletion:))
- [init(carKeyPassword: String, supportedRadioTechnologies: PKRadioTechnology, issuerIdentifier: String, onCompletion: (Result<PKSecureElementPass, any Error>) -> Void, fallback: () -> Fallback)](/documentation/passkit/addpasstowalletbutton/init(carkeypassword:supportedradiotechnologies:issueridentifier:oncompletion:fallback:))
- [AddPassToWalletButtonFilter](/documentation/passkit/addpasstowalletbuttonfilter)

#### Type Methods

- [static func paymentNetwork(PKPaymentNetwork) -> AddPassToWalletButtonFilter](/documentation/passkit/addpasstowalletbuttonfilter/paymentnetwork(_:))
- [static func primaryAccountIdentifier(String) -> AddPassToWalletButtonFilter](/documentation/passkit/addpasstowalletbuttonfilter/primaryaccountidentifier(_:))
- [static func productIdentifier(String) -> AddPassToWalletButtonFilter](/documentation/passkit/addpasstowalletbuttonfilter/productidentifier(_:))
- [AddPassToWalletButtonResponse](/documentation/passkit/addpasstowalletbuttonresponse)

#### Instance Properties

- [var certificates: [Data]](/documentation/passkit/addpasstowalletbuttonresponse/certificates)
- [var nonce: Data](/documentation/passkit/addpasstowalletbuttonresponse/nonce)
- [var nonceSignature: Data](/documentation/passkit/addpasstowalletbuttonresponse/noncesignature)
- [AddPassToWalletButtonStyle](/documentation/passkit/addpasstowalletbuttonstyle)

#### Type Properties

- [static let black: AddPassToWalletButtonStyle](/documentation/passkit/addpasstowalletbuttonstyle/black)
- [static let blackOutline: AddPassToWalletButtonStyle](/documentation/passkit/addpasstowalletbuttonstyle/blackoutline)

### Pass library

- [PKPassLibrary](/documentation/passkit/pkpasslibrary)

#### Accessing passes

- [class func isPassLibraryAvailable() -> Bool](/documentation/passkit/pkpasslibrary/ispasslibraryavailable())
- [func passes() -> [PKPass]](/documentation/passkit/pkpasslibrary/passes())
- [func passes(of: PKPassType) -> [PKPass]](/documentation/passkit/pkpasslibrary/passes(of:))
- [func pass(withPassTypeIdentifier: String, serialNumber: String) -> PKPass?](/documentation/passkit/pkpasslibrary/pass(withpasstypeidentifier:serialnumber:))
- [func containsPass(PKPass) -> Bool](/documentation/passkit/pkpasslibrary/containspass(_:))
- [func serviceProviderData(for: PKSecureElementPass, completion: (Data?, (any Error)?) -> Void)](/documentation/passkit/pkpasslibrary/serviceproviderdata(for:completion:))
- [var remoteSecureElementPasses: [PKSecureElementPass]](/documentation/passkit/pkpasslibrary/remotesecureelementpasses)

#### Adding passes

- [func canAddSecureElementPass(primaryAccountIdentifier: String) -> Bool](/documentation/passkit/pkpasslibrary/canaddsecureelementpass(primaryaccountidentifier:))
- [func canAddFelicaPass() -> Bool](/documentation/passkit/pkpasslibrary/canaddfelicapass())
- [func addPasses([PKPass], withCompletionHandler: ((PKPassLibraryAddPassesStatus) -> Void)?)](/documentation/passkit/pkpasslibrary/addpasses(_:withcompletionhandler:))
- [PKPassLibraryAddPassesStatus](/documentation/passkit/pkpasslibraryaddpassesstatus)

##### Constants

- [case didAddPasses](/documentation/passkit/pkpasslibraryaddpassesstatus/didaddpasses)
- [case shouldReviewPasses](/documentation/passkit/pkpasslibraryaddpassesstatus/shouldreviewpasses)
- [case didCancelAddPasses](/documentation/passkit/pkpasslibraryaddpassesstatus/didcanceladdpasses)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpasslibraryaddpassesstatus/init(rawvalue:))

#### Managing passes

- [var isSecureElementPassActivationAvailable: Bool](/documentation/passkit/pkpasslibrary/issecureelementpassactivationavailable)
- [func activate(PKSecureElementPass, activationData: Data, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/passkit/pkpasslibrary/activate(_:activationdata:completion:))
- [func replacePass(with: PKPass) -> Bool](/documentation/passkit/pkpasslibrary/replacepass(with:))
- [func removePass(PKPass)](/documentation/passkit/pkpasslibrary/removepass(_:))

#### Presenting and suppressing passes

- [func present(PKSecureElementPass)](/documentation/passkit/pkpasslibrary/present(_:)-9467u)
- [class func isSuppressingAutomaticPassPresentation() -> Bool](/documentation/passkit/pkpasslibrary/issuppressingautomaticpasspresentation())
- [class func requestAutomaticPassPresentationSuppression(responseHandler: (PKAutomaticPassPresentationSuppressionResult) -> Void) -> PKSuppressionRequestToken](/documentation/passkit/pkpasslibrary/requestautomaticpasspresentationsuppression(responsehandler:))
- [PKAutomaticPassPresentationSuppressionResult](/documentation/passkit/pkautomaticpasspresentationsuppressionresult)

##### Constants

- [case notSupported](/documentation/passkit/pkautomaticpasspresentationsuppressionresult/notsupported)
- [case alreadyPresenting](/documentation/passkit/pkautomaticpasspresentationsuppressionresult/alreadypresenting)
- [case denied](/documentation/passkit/pkautomaticpasspresentationsuppressionresult/denied)
- [case cancelled](/documentation/passkit/pkautomaticpasspresentationsuppressionresult/cancelled)
- [case success](/documentation/passkit/pkautomaticpasspresentationsuppressionresult/success)

##### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkautomaticpasspresentationsuppressionresult/init(rawvalue:))
- [class func endAutomaticPassPresentationSuppression(withRequestToken: PKSuppressionRequestToken)](/documentation/passkit/pkpasslibrary/endautomaticpasspresentationsuppression(withrequesttoken:))
- [PKSuppressionRequestToken](/documentation/passkit/pksuppressionrequesttoken)

#### Setting up payments

- [func openPaymentSetup()](/documentation/passkit/pkpasslibrary/openpaymentsetup())

#### Signing data

- [func sign(Data, using: PKSecureElementPass, completion: (Data?, Data?, (any Error)?) -> Void)](/documentation/passkit/pkpasslibrary/sign(_:using:completion:))

#### Receiving notifications

- [PKPassLibraryNotificationKey](/documentation/passkit/pkpasslibrarynotificationkey)

##### Creating a pass library notification key

- [init(rawValue: String)](/documentation/passkit/pkpasslibrarynotificationkey/init(rawvalue:))

##### Notification keys

- [static let addedPassesUserInfoKey: PKPassLibraryNotificationKey](/documentation/passkit/pkpasslibrarynotificationkey/addedpassesuserinfokey)
- [static let passTypeIdentifierUserInfoKey: PKPassLibraryNotificationKey](/documentation/passkit/pkpasslibrarynotificationkey/passtypeidentifieruserinfokey)
- [static let recoveredPassesUserInfoKey: PKPassLibraryNotificationKey](/documentation/passkit/pkpasslibrarynotificationkey/recoveredpassesuserinfokey)
- [static let removedPassInfosUserInfoKey: PKPassLibraryNotificationKey](/documentation/passkit/pkpasslibrarynotificationkey/removedpassinfosuserinfokey)
- [static let replacementPassesUserInfoKey: PKPassLibraryNotificationKey](/documentation/passkit/pkpasslibrarynotificationkey/replacementpassesuserinfokey)
- [static let serialNumberUserInfoKey: PKPassLibraryNotificationKey](/documentation/passkit/pkpasslibrarynotificationkey/serialnumberuserinfokey)
- [PKPassLibraryNotificationName](/documentation/passkit/pkpasslibrarynotificationname)

##### Creating a pass library notification name

- [init(rawValue: String)](/documentation/passkit/pkpasslibrarynotificationname/init(rawvalue:))
- [init(String)](/documentation/passkit/pkpasslibrarynotificationname/init(_:))

##### Notification names

- [static let PKPassLibraryDidChange: PKPassLibraryNotificationName](/documentation/passkit/pkpasslibrarynotificationname/pkpasslibrarydidchange)
- [static let PKPassLibraryRemotePaymentPassesDidChange: PKPassLibraryNotificationName](/documentation/passkit/pkpasslibrarynotificationname/pkpasslibraryremotepaymentpassesdidchange)

#### Deprecated

- [Deprecated Symbols](/documentation/passkit/deprecated-symbols)

##### Deprecated Methods

- [func activate(PKPaymentPass, withActivationCode: String, completion: ((Bool, any Error) -> Void)?)](/documentation/passkit/pkpasslibrary/activate(_:withactivationcode:completion:))
- [func activate(PKPaymentPass, withActivationData: Data, completion: ((Bool, any Error) -> Void)?)](/documentation/passkit/pkpasslibrary/activate(_:withactivationdata:completion:))
- [func canAddPaymentPass(withPrimaryAccountIdentifier: String) -> Bool](/documentation/passkit/pkpasslibrary/canaddpaymentpass(withprimaryaccountidentifier:))
- [class func isPaymentPassActivationAvailable() -> Bool](/documentation/passkit/pkpasslibrary/ispaymentpassactivationavailable()-swift.type.method)
- [func isPaymentPassActivationAvailable() -> Bool](/documentation/passkit/pkpasslibrary/ispaymentpassactivationavailable()-swift.method)
- [func present(PKPaymentPass)](/documentation/passkit/pkpasslibrary/present(_:)-67jce)
- [func remotePaymentPasses() -> [PKPaymentPass]](/documentation/passkit/pkpasslibrary/remotepaymentpasses())

#### Instance Methods

- [func authorizationStatus(for: PKPassLibrary.Capability) -> PKPassLibrary.AuthorizationStatus](/documentation/passkit/pkpasslibrary/authorizationstatus(for:))
- [func encryptedServiceProviderData(for: PKSecureElementPass, completion: ([AnyHashable : Any]?, (any Error)?) -> Void)](/documentation/passkit/pkpasslibrary/encryptedserviceproviderdata(for:completion:))
- [func passes(withReaderIdentifier: String) -> Set<PKSecureElementPass>](/documentation/passkit/pkpasslibrary/passes(withreaderidentifier:))
- [func requestAuthorization(for: PKPassLibrary.Capability, completion: (PKPassLibrary.AuthorizationStatus) -> Void)](/documentation/passkit/pkpasslibrary/requestauthorization(for:completion:))

#### Enumerations

- [PKPassLibrary.AuthorizationStatus](/documentation/passkit/pkpasslibrary/authorizationstatus)

##### Enumeration Cases

- [case authorized](/documentation/passkit/pkpasslibrary/authorizationstatus/authorized)
- [case denied](/documentation/passkit/pkpasslibrary/authorizationstatus/denied)
- [case notDetermined](/documentation/passkit/pkpasslibrary/authorizationstatus/notdetermined)
- [case restricted](/documentation/passkit/pkpasslibrary/authorizationstatus/restricted)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpasslibrary/authorizationstatus/init(rawvalue:))
- [PKPassLibrary.Capability](/documentation/passkit/pkpasslibrary/capability)

##### Enumeration Cases

- [case backgroundAddPasses](/documentation/passkit/pkpasslibrary/capability/backgroundaddpasses)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpasslibrary/capability/init(rawvalue:))

### General purpose passes

- [PKSecureElementPass](/documentation/passkit/pksecureelementpass)

#### Getting the activation state

- [var passActivationState: PKSecureElementPass.PassActivationState](/documentation/passkit/pksecureelementpass/passactivationstate-swift.property)
- [PKSecureElementPass.PassActivationState](/documentation/passkit/pksecureelementpass/passactivationstate-swift.enum)

##### Activation states

- [case requiresActivation](/documentation/passkit/pksecureelementpass/passactivationstate-swift.enum/requiresactivation)
- [case activating](/documentation/passkit/pksecureelementpass/passactivationstate-swift.enum/activating)
- [case activated](/documentation/passkit/pksecureelementpass/passactivationstate-swift.enum/activated)
- [case suspended](/documentation/passkit/pksecureelementpass/passactivationstate-swift.enum/suspended)
- [case deactivated](/documentation/passkit/pksecureelementpass/passactivationstate-swift.enum/deactivated)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pksecureelementpass/passactivationstate-swift.enum/init(rawvalue:))

#### Getting the hardware attributes

- [var deviceAccountIdentifier: String](/documentation/passkit/pksecureelementpass/deviceaccountidentifier)
- [var deviceAccountNumberSuffix: String](/documentation/passkit/pksecureelementpass/deviceaccountnumbersuffix)
- [var devicePassIdentifier: String?](/documentation/passkit/pksecureelementpass/devicepassidentifier)
- [var pairedTerminalIdentifier: String?](/documentation/passkit/pksecureelementpass/pairedterminalidentifier)

#### Getting the account attributes

- [var primaryAccountIdentifier: String](/documentation/passkit/pksecureelementpass/primaryaccountidentifier)
- [var primaryAccountNumberSuffix: String](/documentation/passkit/pksecureelementpass/primaryaccountnumbersuffix)
- [PKAddSecureElementPassConfiguration](/documentation/passkit/pkaddsecureelementpassconfiguration)

#### Managing the issuer identity

- [var issuerIdentifier: String?](/documentation/passkit/pkaddsecureelementpassconfiguration/issueridentifier)
- [var localizedDescription: String?](/documentation/passkit/pkaddsecureelementpassconfiguration/localizeddescription)
- [PKAddSecureElementPassViewController](/documentation/passkit/pkaddsecureelementpassviewcontroller)

#### Creating a view controller

- [init?(configuration: PKAddSecureElementPassConfiguration, delegate: (any PKAddSecureElementPassViewControllerDelegate)?)](/documentation/passkit/pkaddsecureelementpassviewcontroller/init(configuration:delegate:))

#### Responding to the life cycle of a pass

- [var delegate: (any PKAddSecureElementPassViewControllerDelegate)?](/documentation/passkit/pkaddsecureelementpassviewcontroller/delegate)
- [PKAddSecureElementPassViewControllerDelegate](/documentation/passkit/pkaddsecureelementpassviewcontrollerdelegate)

##### Responding to pass addition

- [func addSecureElementPassViewController(PKAddSecureElementPassViewController, didFinishAddingSecureElementPasses: [PKSecureElementPass]?, error: (any Error)?)](/documentation/passkit/pkaddsecureelementpassviewcontrollerdelegate/addsecureelementpassviewcontroller(_:didfinishaddingsecureelementpasses:error:))
- [func addSecureElementPassViewController(PKAddSecureElementPassViewController, didFinishAdding: PKSecureElementPass?, error: (any Error)?)](/documentation/passkit/pkaddsecureelementpassviewcontrollerdelegate/addsecureelementpassviewcontroller(_:didfinishadding:error:))

#### Validating pass configuration

- [class func canAddSecureElementPass(configuration: PKAddSecureElementPassConfiguration) -> Bool](/documentation/passkit/pkaddsecureelementpassviewcontroller/canaddsecureelementpass(configuration:))
- [PKPass](/documentation/passkit/pkpass)

#### Creating a pass

- [init(data: Data) throws](/documentation/passkit/pkpass/init(data:))

#### Identifying a pass

- [var passType: PKPassType](/documentation/passkit/pkpass/passtype)
- [PKPassType](/documentation/passkit/pkpasstype)

##### Pass types

- [case any](/documentation/passkit/pkpasstype/any)
- [case barcode](/documentation/passkit/pkpasstype/barcode)
- [case secureElement](/documentation/passkit/pkpasstype/secureelement)
- [static var payment: PKPassType](/documentation/passkit/pkpasstype/payment)

##### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkpasstype/init(rawvalue:))
- [var secureElementPass: PKSecureElementPass?](/documentation/passkit/pkpass/secureelementpass)
- [var serialNumber: String](/documentation/passkit/pkpass/serialnumber)
- [var passTypeIdentifier: String](/documentation/passkit/pkpass/passtypeidentifier)
- [var deviceName: String](/documentation/passkit/pkpass/devicename)
- [var localizedName: String](/documentation/passkit/pkpass/localizedname)
- [var localizedDescription: String](/documentation/passkit/pkpass/localizeddescription)
- [var isRemotePass: Bool](/documentation/passkit/pkpass/isremotepass)
- [var paymentPass: PKPaymentPass?](/documentation/passkit/pkpass/paymentpass)

#### Getting the web service information

- [var webServiceURL: URL?](/documentation/passkit/pkpass/webserviceurl)
- [var authenticationToken: String?](/documentation/passkit/pkpass/authenticationtoken)

#### Getting the display attributes

- [var icon: UIImage](/documentation/passkit/pkpass/icon)
- [func localizedValue(forFieldKey: String) -> Any?](/documentation/passkit/pkpass/localizedvalue(forfieldkey:))
- [var organizationName: String](/documentation/passkit/pkpass/organizationname)
- [var relevantDate: Date?](/documentation/passkit/pkpass/relevantdate)
- [PKPassRelevantDate](/documentation/passkit/pkpassrelevantdate)

##### Instance Properties

- [var date: Date?](/documentation/passkit/pkpassrelevantdate/date)
- [var interval: DateInterval?](/documentation/passkit/pkpassrelevantdate/interval)

#### Getting the Wallet URL

- [var passURL: URL?](/documentation/passkit/pkpass/passurl)

#### Providing contextual information

- [var userInfo: [AnyHashable : Any]?](/documentation/passkit/pkpass/userinfo)

#### Instance Properties

- [var relevantDates: [PKPassRelevantDate]](/documentation/passkit/pkpass/relevantdates)
- [PKAddPassesViewController](/documentation/passkit/pkaddpassesviewcontroller)

#### Determining if the device supports adding passes

- [class func canAddPasses() -> Bool](/documentation/passkit/pkaddpassesviewcontroller/canaddpasses())

#### Creating an add-passes view controller

- [init?(pass: PKPass)](/documentation/passkit/pkaddpassesviewcontroller/init(pass:))
- [init?(passes: [PKPass])](/documentation/passkit/pkaddpassesviewcontroller/init(passes:))
- [init(issuerData: Data, signature: Data) throws](/documentation/passkit/pkaddpassesviewcontroller/init(issuerdata:signature:))

#### Adding passes

- [var delegate: (any PKAddPassesViewControllerDelegate)?](/documentation/passkit/pkaddpassesviewcontroller/delegate)
- [PKAddPassesViewControllerDelegate](/documentation/passkit/pkaddpassesviewcontrollerdelegate)

##### Delegate methods

- [func addPassesViewControllerDidFinish(PKAddPassesViewController)](/documentation/passkit/pkaddpassesviewcontrollerdelegate/addpassesviewcontrollerdidfinish(_:))
- [AsyncShareablePassConfiguration](/documentation/passkit/asyncshareablepassconfiguration)

#### Creating the configuration

- [init(metadata: [PKShareablePassMetadata], action: PKAddShareablePassConfigurationPrimaryAction, content: (AsyncShareablePassConfiguration<Content>.Result) -> Content)](/documentation/passkit/asyncshareablepassconfiguration/init(metadata:action:content:))
- [AsyncShareablePassConfiguration.Result](/documentation/passkit/asyncshareablepassconfiguration/result)

##### Enumeration Cases

- [case failure(any Error)](/documentation/passkit/asyncshareablepassconfiguration/result/failure(_:))
- [case loading](/documentation/passkit/asyncshareablepassconfiguration/result/loading)
- [case success(PKAddShareablePassConfiguration)](/documentation/passkit/asyncshareablepassconfiguration/result/success(_:))
- [PKShareSecureElementPassViewController](/documentation/passkit/pksharesecureelementpassviewcontroller)

#### Initializers

- [init(secureElementPass: PKSecureElementPass, delegate: (any PKShareSecureElementPassViewControllerDelegate)?)](/documentation/passkit/pksharesecureelementpassviewcontroller/init(secureelementpass:delegate:))

#### Instance Properties

- [var delegate: (any PKShareSecureElementPassViewControllerDelegate)?](/documentation/passkit/pksharesecureelementpassviewcontroller/delegate)
- [var promptToShareURL: Bool](/documentation/passkit/pksharesecureelementpassviewcontroller/prompttoshareurl)
- [PKShareSecureElementPassViewControllerDelegate](/documentation/passkit/pksharesecureelementpassviewcontrollerdelegate)

#### Instance Methods

- [func shareSecureElementPassViewController(PKShareSecureElementPassViewController, didCreateShare: URL?, activationCode: String?)](/documentation/passkit/pksharesecureelementpassviewcontrollerdelegate/sharesecureelementpassviewcontroller(_:didcreateshare:activationcode:))
- [func shareSecureElementPassViewController(PKShareSecureElementPassViewController, didFinishWith: PKShareSecureElementPassResult)](/documentation/passkit/pksharesecureelementpassviewcontrollerdelegate/sharesecureelementpassviewcontroller(_:didfinishwith:))
- [PKShareablePassMetadata.Preview](/documentation/passkit/pkshareablepassmetadata/preview-swift.class)

#### Initializers

- [init(templateIdentifier: String)](/documentation/passkit/pkshareablepassmetadata/preview-swift.class/init(templateidentifier:))

#### Instance Properties

- [var ownerDisplayName: String?](/documentation/passkit/pkshareablepassmetadata/preview-swift.class/ownerdisplayname)
- [var provisioningTemplateIdentifier: String?](/documentation/passkit/pkshareablepassmetadata/preview-swift.class/provisioningtemplateidentifier)
- [PKShareSecureElementPassResult](/documentation/passkit/pksharesecureelementpassresult)

#### Enumeration Cases

- [case canceled](/documentation/passkit/pksharesecureelementpassresult/canceled)
- [case failed](/documentation/passkit/pksharesecureelementpassresult/failed)
- [case shared](/documentation/passkit/pksharesecureelementpassresult/shared)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pksharesecureelementpassresult/init(rawvalue:))

### Identity passes and authorization

- [Requesting identity data from a Wallet pass](/documentation/passkit/requesting-identity-data-from-a-wallet-pass)
- [Configuring your environment for the Verify with Wallet API](/documentation/passkit/configuring-your-environment-for-the-verify-with-wallet-api)
- [Verifying Wallet identity requests](/documentation/passkit/verifying-wallet-identity-requests)
- [PKIdentityPhotoIDDescriptor](/documentation/passkit/pkidentityphotoiddescriptor)
- [PKIdentityAnyOfDescriptor](/documentation/passkit/pkidentityanyofdescriptor)

#### Identity documents

- [PKIdentityPhotoIDDescriptor](/documentation/passkit/pkidentityphotoiddescriptor)
- [PKIdentityDriversLicenseDescriptor](/documentation/passkit/pkidentitydriverslicensedescriptor)
- [PKIdentityNationalIDCardDescriptor](/documentation/passkit/pkidentitynationalidcarddescriptor)

##### Setting region information

- [var region: Locale.Region?](/documentation/passkit/pkidentitynationalidcarddescriptor/region)

#### Initializers

- [init(descriptors: [any PKIdentityDocumentDescriptor])](/documentation/passkit/pkidentityanyofdescriptor/init(descriptors:))

#### Instance Properties

- [var descriptors: [any PKIdentityDocumentDescriptor]](/documentation/passkit/pkidentityanyofdescriptor/descriptors)
- [PKIdentityDriversLicenseDescriptor](/documentation/passkit/pkidentitydriverslicensedescriptor)
- [PKAddIdentityDocumentMetadata](/documentation/passkit/pkaddidentitydocumentmetadata)

#### Creating metadata for identity documents

- [init(provisioningCredentialIdentifier: String, sharingInstanceIdentifier: String, cardTemplateIdentifier: String, issuingCountryCode: String, documentType: PKAddIdentityDocumentType, preview: PKAddPassMetadataPreview)](/documentation/passkit/pkaddidentitydocumentmetadata/init(provisioningcredentialidentifier:sharinginstanceidentifier:cardtemplateidentifier:issuingcountrycode:documenttype:preview:))

#### Checking identity document types

- [PKAddIdentityDocumentType](/documentation/passkit/pkaddidentitydocumenttype)

##### Types of identity documents

- [case idCard](/documentation/passkit/pkaddidentitydocumenttype/idcard)
- [case mDL](/documentation/passkit/pkaddidentitydocumenttype/mdl)
- [case photoID](/documentation/passkit/pkaddidentitydocumenttype/photoid)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddidentitydocumenttype/init(rawvalue:))

#### Previewing identity document metadata

- [var preview: PKAddPassMetadataPreview](/documentation/passkit/pkaddidentitydocumentmetadata/preview)
- [PKAddIdentityDocumentConfiguration](/documentation/passkit/pkaddidentitydocumentconfiguration)

#### Setting the metadata

- [var metadata: PKIdentityDocumentMetadata](/documentation/passkit/pkaddidentitydocumentconfiguration/metadata)
- [class func forMetadata(PKIdentityDocumentMetadata, completion: (PKAddIdentityDocumentConfiguration?, (any Error)?) -> Void)](/documentation/passkit/pkaddidentitydocumentconfiguration/formetadata(_:completion:))
- [JPKIPassContents](/documentation/passkit/jpkipasscontents)

#### Initializing the digital identity

- [init(PKPass) async throws](/documentation/passkit/jpkipasscontents/init(_:))

#### Defining access to the identity passes

- [JPKIPassContents.UserIdentity](/documentation/passkit/jpkipasscontents/useridentity-swift.struct)

##### Identifying the pass user

- [let userIdentity: JPKIPassContents.UserIdentity?](/documentation/passkit/jpkipasscontents/useridentity-swift.property)
- [func changePIN(from: String, to: String) async throws](/documentation/passkit/jpkipasscontents/useridentity-swift.struct/changepin(from:to:))
- [JPKIPassContents.UserIdentity.AuthenticationType](/documentation/passkit/jpkipasscontents/useridentity-swift.struct/authenticationtype)

###### Types of authentication

- [case pin(String)](/documentation/passkit/jpkipasscontents/useridentity-swift.struct/authenticationtype/pin(_:))
- [case systemBiometric](/documentation/passkit/jpkipasscontents/useridentity-swift.struct/authenticationtype/systembiometric)

##### Instance Properties

- [var authenticationTriesRemaining: Int](/documentation/passkit/jpkipasscontents/useridentity-swift.struct/authenticationtriesremaining)
- [JPKIPassContents.SigningIdentity](/documentation/passkit/jpkipasscontents/signingidentity-swift.struct)

##### Signing identity authentication

- [let signingIdentity: JPKIPassContents.SigningIdentity?](/documentation/passkit/jpkipasscontents/signingidentity-swift.property)
- [func changePassword(from: String, to: String) async throws](/documentation/passkit/jpkipasscontents/signingidentity-swift.struct/changepassword(from:to:))
- [JPKIPassContents.SigningIdentity.AuthenticationType](/documentation/passkit/jpkipasscontents/signingidentity-swift.struct/authenticationtype)

###### Case for authentication

- [case password(String)](/documentation/passkit/jpkipasscontents/signingidentity-swift.struct/authenticationtype/password(_:))
- [JPKIPassContents.Signature](/documentation/passkit/jpkipasscontents/signature)

##### Defining the certificate and signed data

- [let certificate: JPKIPassContents.Certificate<IdentityType>](/documentation/passkit/jpkipasscontents/signature/certificate)
- [let signatureData: Data](/documentation/passkit/jpkipasscontents/signature/signaturedata)
- [JPKIPassContents.Certificate](/documentation/passkit/jpkipasscontents/certificate)

##### Defining data

- [let data: Data](/documentation/passkit/jpkipasscontents/certificate/data)
- [JPKIPassContents.AuthenticationRequest](/documentation/passkit/jpkipasscontents/authenticationrequest)

##### Creating authentication request options

- [init(type: JPKIPassContents.UserIdentity.AuthenticationType)](/documentation/passkit/jpkipasscontents/authenticationrequest/init(type:)-hz9q)
- [init(type: JPKIPassContents.SigningIdentity.AuthenticationType)](/documentation/passkit/jpkipasscontents/authenticationrequest/init(type:)-25dbn)
- [JPKIPassContents.Identity](/documentation/passkit/jpkipasscontents/identity)

##### Data associated with the identity

- [IdentityType](/documentation/passkit/jpkipasscontents/identity/identitytype)
- [func certificate(using: JPKIPassContents.AuthenticationRequest<Self.IdentityType>) async throws -> JPKIPassContents.Certificate<Self.IdentityType>](/documentation/passkit/jpkipasscontents/identity/certificate(using:))

##### Instance Properties

- [var authenticationTriesRemaining: Int](/documentation/passkit/jpkipasscontents/identity/authenticationtriesremaining)

##### Instance Methods

- [func signature(for: [Data], using: JPKIPassContents.AuthenticationRequest<Self.IdentityType>) async throws -> [JPKIPassContents.Signature<Self.IdentityType>]](/documentation/passkit/jpkipasscontents/identity/signature(for:using:)-35arv)
- [func signature(for: Data, using: JPKIPassContents.AuthenticationRequest<Self.IdentityType>) async throws -> JPKIPassContents.Signature<Self.IdentityType>](/documentation/passkit/jpkipasscontents/identity/signature(for:using:)-4l8jw)

#### Error cases

- [JPKIPassContents.Error](/documentation/passkit/jpkipasscontents/error)

##### Error cases

- [case appNotForeground](/documentation/passkit/jpkipasscontents/error/appnotforeground)
- [case biometricUnavailable](/documentation/passkit/jpkipasscontents/error/biometricunavailable)
- [case incorrectUserAuthentication](/documentation/passkit/jpkipasscontents/error/incorrectuserauthentication)
- [case invalidInput](/documentation/passkit/jpkipasscontents/error/invalidinput)
- [case resourceNotAvailable](/documentation/passkit/jpkipasscontents/error/resourcenotavailable)

##### Enumeration Cases

- [case biometricAuthenticationFailed(laError: LAError)](/documentation/passkit/jpkipasscontents/error/biometricauthenticationfailed(laerror:))
- [case unknownError](/documentation/passkit/jpkipasscontents/error/unknownerror)
- [case userAuthenticationFailed(remainingRetryAttempts: Int)](/documentation/passkit/jpkipasscontents/error/userauthenticationfailed(remainingretryattempts:))

#### Instance Properties

- [let signingIdentity: JPKIPassContents.SigningIdentity?](/documentation/passkit/jpkipasscontents/signingidentity-swift.property)
- [let userIdentity: JPKIPassContents.UserIdentity?](/documentation/passkit/jpkipasscontents/useridentity-swift.property)
- [PKAddIdentityDocumentConfiguration](/documentation/passkit/pkaddidentitydocumentconfiguration)

#### Setting the metadata

- [var metadata: PKIdentityDocumentMetadata](/documentation/passkit/pkaddidentitydocumentconfiguration/metadata)
- [class func forMetadata(PKIdentityDocumentMetadata, completion: (PKAddIdentityDocumentConfiguration?, (any Error)?) -> Void)](/documentation/passkit/pkaddidentitydocumentconfiguration/formetadata(_:completion:))
- [PKAddPassMetadataPreview](/documentation/passkit/pkaddpassmetadatapreview)

#### Creating a preview of the pass

- [init(passThumbnail: CGImage, localizedDescription: String)](/documentation/passkit/pkaddpassmetadatapreview/init(passthumbnail:localizeddescription:))
- [var localizedDescription: String?](/documentation/passkit/pkaddpassmetadatapreview/localizeddescription)
- [var passThumbnailImage: CGImage?](/documentation/passkit/pkaddpassmetadatapreview/passthumbnailimage)
- [PKIdentityDocumentMetadata](/documentation/passkit/pkidentitydocumentmetadata)

#### Instance Properties

- [var cardConfigurationIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/cardconfigurationidentifier)
- [var cardTemplateIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/cardtemplateidentifier)
- [var credentialIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/credentialidentifier)
- [var serverEnvironmentIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/serverenvironmentidentifier)
- [var sharingInstanceIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/sharinginstanceidentifier)
- [var documentType: PKAddIdentityDocumentType](/documentation/passkit/pkidentitydocumentmetadata/documenttype)
- [var issuingCountryCode: String](/documentation/passkit/pkidentitydocumentmetadata/issuingcountrycode)
- [var cardConfigurationIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/cardconfigurationidentifier)
- [var cardTemplateIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/cardtemplateidentifier)
- [var credentialIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/credentialidentifier)
- [var documentType: PKAddIdentityDocumentType](/documentation/passkit/pkidentitydocumentmetadata/documenttype)
- [var issuingCountryCode: String](/documentation/passkit/pkidentitydocumentmetadata/issuingcountrycode)
- [var serverEnvironmentIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/serverenvironmentidentifier)
- [var sharingInstanceIdentifier: String](/documentation/passkit/pkidentitydocumentmetadata/sharinginstanceidentifier)
- [PKIdentityNationalIDCardDescriptor](/documentation/passkit/pkidentitynationalidcarddescriptor)

#### Setting region information

- [var region: Locale.Region?](/documentation/passkit/pkidentitynationalidcarddescriptor/region)
- [PKJapanIndividualNumberCardMetadata](/documentation/passkit/pkjapanindividualnumbercardmetadata)

#### Initializing the digital card metadata

- [init(provisioningCredentialIdentifier: String, sharingInstanceIdentifier: String, cardConfigurationIdentifier: String, preview: PKAddPassMetadataPreview)](/documentation/passkit/pkjapanindividualnumbercardmetadata/init(provisioningcredentialidentifier:sharinginstanceidentifier:cardconfigurationidentifier:preview:))
- [init(provisioningCredentialIdentifier: String, sharingInstanceIdentifier: String, cardTemplateIdentifier: String, preview: PKAddPassMetadataPreview)](/documentation/passkit/pkjapanindividualnumbercardmetadata/init(provisioningcredentialidentifier:sharinginstanceidentifier:cardtemplateidentifier:preview:))

#### Defining configuration

- [var authenticationPassword: String?](/documentation/passkit/pkjapanindividualnumbercardmetadata/authenticationpassword)
- [var preview: PKAddPassMetadataPreview](/documentation/passkit/pkjapanindividualnumbercardmetadata/preview)
- [var signingPassword: String?](/documentation/passkit/pkjapanindividualnumbercardmetadata/signingpassword)

### Identity sheet interactions and authorization

- [PKIdentityAuthorizationController](/documentation/passkit/pkidentityauthorizationcontroller)

#### Describing a document

- [PKIdentityDriversLicenseDescriptor](/documentation/passkit/pkidentitydriverslicensedescriptor)
- [PKIdentityIntentToStore](/documentation/passkit/pkidentityintenttostore)

##### Creating a default intent

- [class func mayStore(days: Int) -> Self](/documentation/passkit/pkidentityintenttostore/maystore(days:))

##### Getting default intents

- [class var mayStore: PKIdentityIntentToStore](/documentation/passkit/pkidentityintenttostore/maystore)
- [class var willNotStore: PKIdentityIntentToStore](/documentation/passkit/pkidentityintenttostore/willnotstore)
- [PKIdentityDocumentDescriptor](/documentation/passkit/pkidentitydocumentdescriptor)

##### Inspecting elements

- [var elements: [PKIdentityElement]](/documentation/passkit/pkidentitydocumentdescriptor/elements)
- [PKIdentityElement](/documentation/passkit/pkidentityelement)

###### Getting identity elements

- [class var address: PKIdentityElement](/documentation/passkit/pkidentityelement/address)
- [class var dateOfBirth: PKIdentityElement](/documentation/passkit/pkidentityelement/dateofbirth)
- [class var documentIssueDate: PKIdentityElement](/documentation/passkit/pkidentityelement/documentissuedate)
- [class var documentExpirationDate: PKIdentityElement](/documentation/passkit/pkidentityelement/documentexpirationdate)
- [class var documentNumber: PKIdentityElement](/documentation/passkit/pkidentityelement/documentnumber)
- [class var drivingPrivileges: PKIdentityElement](/documentation/passkit/pkidentityelement/drivingprivileges)
- [class var familyName: PKIdentityElement](/documentation/passkit/pkidentityelement/familyname)
- [class var givenName: PKIdentityElement](/documentation/passkit/pkidentityelement/givenname)
- [class var issuingAuthority: PKIdentityElement](/documentation/passkit/pkidentityelement/issuingauthority)
- [class var portrait: PKIdentityElement](/documentation/passkit/pkidentityelement/portrait)

###### Getting an age identity element

- [class var age: PKIdentityElement](/documentation/passkit/pkidentityelement/age)
- [class func age(atLeast: Int) -> Self](/documentation/passkit/pkidentityelement/age(atleast:))

###### Type Properties

- [class var documentDHSComplianceStatus: PKIdentityElement](/documentation/passkit/pkidentityelement/documentdhscompliancestatus)
- [class var eyeColor: PKIdentityElement](/documentation/passkit/pkidentityelement/eyecolor)
- [class var hairColor: PKIdentityElement](/documentation/passkit/pkidentityelement/haircolor)
- [class var height: PKIdentityElement](/documentation/passkit/pkidentityelement/height)
- [class var organDonorStatus: PKIdentityElement](/documentation/passkit/pkidentityelement/organdonorstatus)
- [class var sex: PKIdentityElement](/documentation/passkit/pkidentityelement/sex)
- [class var veteranStatus: PKIdentityElement](/documentation/passkit/pkidentityelement/veteranstatus)
- [class var weight: PKIdentityElement](/documentation/passkit/pkidentityelement/weight)

##### Adding an identity element

- [func addElements([PKIdentityElement], intentToStore: PKIdentityIntentToStore)](/documentation/passkit/pkidentitydocumentdescriptor/addelements(_:intenttostore:))
- [PKIdentityIntentToStore](/documentation/passkit/pkidentityintenttostore)

###### Creating a default intent

- [class func mayStore(days: Int) -> Self](/documentation/passkit/pkidentityintenttostore/maystore(days:))

###### Getting default intents

- [class var mayStore: PKIdentityIntentToStore](/documentation/passkit/pkidentityintenttostore/maystore)
- [class var willNotStore: PKIdentityIntentToStore](/documentation/passkit/pkidentityintenttostore/willnotstore)

##### Getting an elements intent

- [func intentToStore(element: PKIdentityElement) -> PKIdentityIntentToStore?](/documentation/passkit/pkidentitydocumentdescriptor/intenttostore(element:))

#### Requesting a document

- [func checkCanRequestDocument(any PKIdentityDocumentDescriptor, completion: (Bool) -> Void)](/documentation/passkit/pkidentityauthorizationcontroller/checkcanrequestdocument(_:completion:))
- [func requestDocument(PKIdentityRequest, completion: (PKIdentityDocument?, (any Error)?) -> Void)](/documentation/passkit/pkidentityauthorizationcontroller/requestdocument(_:completion:))

#### Cancelling a request

- [func cancelRequest()](/documentation/passkit/pkidentityauthorizationcontroller/cancelrequest())
- [PKIdentityRequest](/documentation/passkit/pkidentityrequest)

#### Configuring an identity request

- [var descriptor: (any PKIdentityDocumentDescriptor)?](/documentation/passkit/pkidentityrequest/descriptor)
- [var nonce: Data?](/documentation/passkit/pkidentityrequest/nonce)
- [var merchantIdentifier: String?](/documentation/passkit/pkidentityrequest/merchantidentifier)

#### Instance Properties

- [var usageDescriptionKey: String?](/documentation/passkit/pkidentityrequest/usagedescriptionkey)
- [PKIdentityDocument](/documentation/passkit/pkidentitydocument)

#### Configuring an identity document

- [var encryptedData: Data](/documentation/passkit/pkidentitydocument/encrypteddata)
- [PKIdentityElement](/documentation/passkit/pkidentityelement)

#### Getting identity elements

- [class var address: PKIdentityElement](/documentation/passkit/pkidentityelement/address)
- [class var dateOfBirth: PKIdentityElement](/documentation/passkit/pkidentityelement/dateofbirth)
- [class var documentIssueDate: PKIdentityElement](/documentation/passkit/pkidentityelement/documentissuedate)
- [class var documentExpirationDate: PKIdentityElement](/documentation/passkit/pkidentityelement/documentexpirationdate)
- [class var documentNumber: PKIdentityElement](/documentation/passkit/pkidentityelement/documentnumber)
- [class var drivingPrivileges: PKIdentityElement](/documentation/passkit/pkidentityelement/drivingprivileges)
- [class var familyName: PKIdentityElement](/documentation/passkit/pkidentityelement/familyname)
- [class var givenName: PKIdentityElement](/documentation/passkit/pkidentityelement/givenname)
- [class var issuingAuthority: PKIdentityElement](/documentation/passkit/pkidentityelement/issuingauthority)
- [class var portrait: PKIdentityElement](/documentation/passkit/pkidentityelement/portrait)

#### Getting an age identity element

- [class var age: PKIdentityElement](/documentation/passkit/pkidentityelement/age)
- [class func age(atLeast: Int) -> Self](/documentation/passkit/pkidentityelement/age(atleast:))

#### Type Properties

- [class var documentDHSComplianceStatus: PKIdentityElement](/documentation/passkit/pkidentityelement/documentdhscompliancestatus)
- [class var eyeColor: PKIdentityElement](/documentation/passkit/pkidentityelement/eyecolor)
- [class var hairColor: PKIdentityElement](/documentation/passkit/pkidentityelement/haircolor)
- [class var height: PKIdentityElement](/documentation/passkit/pkidentityelement/height)
- [class var organDonorStatus: PKIdentityElement](/documentation/passkit/pkidentityelement/organdonorstatus)
- [class var sex: PKIdentityElement](/documentation/passkit/pkidentityelement/sex)
- [class var veteranStatus: PKIdentityElement](/documentation/passkit/pkidentityelement/veteranstatus)
- [class var weight: PKIdentityElement](/documentation/passkit/pkidentityelement/weight)
- [PKIdentityButton](/documentation/passkit/pkidentitybutton)

#### Creating an identity button

- [init(label: PKIdentityButton.Label, style: PKIdentityButton.Style)](/documentation/passkit/pkidentitybutton/init(label:style:))

#### Configuring the appearance

- [PKIdentityButton.Label](/documentation/passkit/pkidentitybutton/label)

##### Labels

- [case verifyIdentity](/documentation/passkit/pkidentitybutton/label/verifyidentity)
- [case verify](/documentation/passkit/pkidentitybutton/label/verify)
- [case verifyAge](/documentation/passkit/pkidentitybutton/label/verifyage)
- [case `continue`](/documentation/passkit/pkidentitybutton/label/continue)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkidentitybutton/label/init(rawvalue:))
- [PKIdentityButton.Style](/documentation/passkit/pkidentitybutton/style)

##### Styles

- [case black](/documentation/passkit/pkidentitybutton/style/black)
- [case blackOutline](/documentation/passkit/pkidentitybutton/style/blackoutline)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkidentitybutton/style/init(rawvalue:))
- [var cornerRadius: CGFloat](/documentation/passkit/pkidentitybutton/cornerradius)
- [VerifyIdentityWithWalletButton](/documentation/passkit/verifyidentitywithwalletbutton)

#### Creating the button

- [init(VerifyIdentityWithWalletButtonLabel, action: () -> Void)](/documentation/passkit/verifyidentitywithwalletbutton/init(_:action:))
- [init(VerifyIdentityWithWalletButtonLabel, request: PKIdentityRequest, onCompletion: (Result<PKIdentityDocument, any Error>) -> Void)](/documentation/passkit/verifyidentitywithwalletbutton/init(_:request:oncompletion:))
- [init(VerifyIdentityWithWalletButtonLabel, request: PKIdentityRequest, onCompletion: (Result<PKIdentityDocument, any Error>) -> Void, fallback: () -> Fallback)](/documentation/passkit/verifyidentitywithwalletbutton/init(_:request:oncompletion:fallback:))
- [VerifyIdentityWithWalletButtonLabel](/documentation/passkit/verifyidentitywithwalletbuttonlabel)

#### Getting standard labels

- [static let `continue`: VerifyIdentityWithWalletButtonLabel](/documentation/passkit/verifyidentitywithwalletbuttonlabel/continue)
- [static let verify: VerifyIdentityWithWalletButtonLabel](/documentation/passkit/verifyidentitywithwalletbuttonlabel/verify)
- [static let verifyAge: VerifyIdentityWithWalletButtonLabel](/documentation/passkit/verifyidentitywithwalletbuttonlabel/verifyage)
- [static let verifyIdentity: VerifyIdentityWithWalletButtonLabel](/documentation/passkit/verifyidentitywithwalletbuttonlabel/verifyidentity)
- [VerifyIdentityWithWalletButtonStyle](/documentation/passkit/verifyidentitywithwalletbuttonstyle)

#### Getting the standard styles

- [static let black: VerifyIdentityWithWalletButtonStyle](/documentation/passkit/verifyidentitywithwalletbuttonstyle/black)
- [static let blackOutline: VerifyIdentityWithWalletButtonStyle](/documentation/passkit/verifyidentitywithwalletbuttonstyle/blackoutline)

### Payment passes

- [PKPaymentPass](/documentation/passkit/pkpaymentpass)

#### Determining activation state

- [var activationState: PKPaymentPassActivationState](/documentation/passkit/pkpaymentpass/activationstate)
- [PKPaymentPassActivationState](/documentation/passkit/pkpaymentpassactivationstate)

##### Activation states

- [case activated](/documentation/passkit/pkpaymentpassactivationstate/activated)
- [case requiresActivation](/documentation/passkit/pkpaymentpassactivationstate/requiresactivation)
- [case activating](/documentation/passkit/pkpaymentpassactivationstate/activating)
- [case suspended](/documentation/passkit/pkpaymentpassactivationstate/suspended)
- [case deactivated](/documentation/passkit/pkpaymentpassactivationstate/deactivated)

##### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkpaymentpassactivationstate/init(rawvalue:))
- [PKAddPaymentPassViewController](/documentation/passkit/pkaddpaymentpassviewcontroller)

#### Determining if payment passes can be added

- [class func canAddPaymentPass() -> Bool](/documentation/passkit/pkaddpaymentpassviewcontroller/canaddpaymentpass())

#### Working with add payment view controllers

- [var delegate: (any PKAddPaymentPassViewControllerDelegate)?](/documentation/passkit/pkaddpaymentpassviewcontroller/delegate)
- [PKAddPaymentPassViewControllerDelegate](/documentation/passkit/pkaddpaymentpassviewcontrollerdelegate)

##### Requesting to add payment cards to Apple Pay

- [func addPaymentPassViewController(PKAddPaymentPassViewController, generateRequestWithCertificateChain: [Data], nonce: Data, nonceSignature: Data, completionHandler: (PKAddPaymentPassRequest) -> Void)](/documentation/passkit/pkaddpaymentpassviewcontrollerdelegate/addpaymentpassviewcontroller(_:generaterequestwithcertificatechain:nonce:noncesignature:completionhandler:))
- [PKAddPaymentPassRequest](/documentation/passkit/pkaddpaymentpassrequest)

###### Creating an add payment pass request

- [init()](/documentation/passkit/pkaddpaymentpassrequest/init())

###### Accessing request data

- [var activationData: Data?](/documentation/passkit/pkaddpaymentpassrequest/activationdata)
- [var encryptedPassData: Data?](/documentation/passkit/pkaddpaymentpassrequest/encryptedpassdata)
- [var ephemeralPublicKey: Data?](/documentation/passkit/pkaddpaymentpassrequest/ephemeralpublickey)
- [var wrappedKey: Data?](/documentation/passkit/pkaddpaymentpassrequest/wrappedkey)
- [func addPaymentPassViewController(PKAddPaymentPassViewController, didFinishAdding: PKPaymentPass?, error: (any Error)?)](/documentation/passkit/pkaddpaymentpassviewcontrollerdelegate/addpaymentpassviewcontroller(_:didfinishadding:error:))

##### Payment pass errors

- [PKAddPaymentPassError](/documentation/passkit/pkaddpaymentpasserror)

###### Error codes

- [case unsupported](/documentation/passkit/pkaddpaymentpasserror/unsupported)
- [case userCancelled](/documentation/passkit/pkaddpaymentpasserror/usercancelled)
- [case systemCancelled](/documentation/passkit/pkaddpaymentpasserror/systemcancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddpaymentpasserror/init(rawvalue:))

#### Creating an add-payment-pass view controller

- [init?(requestConfiguration: PKAddPaymentPassRequestConfiguration, delegate: (any PKAddPaymentPassViewControllerDelegate)?)](/documentation/passkit/pkaddpaymentpassviewcontroller/init(requestconfiguration:delegate:))
- [PKAddPaymentPassRequestConfiguration](/documentation/passkit/pkaddpaymentpassrequestconfiguration)

##### Creating a request configuration

- [init?(encryptionScheme: PKEncryptionScheme)](/documentation/passkit/pkaddpaymentpassrequestconfiguration/init(encryptionscheme:))
- [PKEncryptionScheme](/documentation/passkit/pkencryptionscheme)

###### Creating an encryption scheme

- [init(rawValue: String)](/documentation/passkit/pkencryptionscheme/init(rawvalue:))

###### Encryption schemes

- [static let ECC_V2: PKEncryptionScheme](/documentation/passkit/pkencryptionscheme/ecc_v2)
- [static let RSA_V2: PKEncryptionScheme](/documentation/passkit/pkencryptionscheme/rsa_v2)

##### Filtering pass libraries

- [var paymentNetwork: PKPaymentNetwork?](/documentation/passkit/pkaddpaymentpassrequestconfiguration/paymentnetwork)
- [var primaryAccountIdentifier: String?](/documentation/passkit/pkaddpaymentpassrequestconfiguration/primaryaccountidentifier)
- [var requiresFelicaSecureElement: Bool](/documentation/passkit/pkaddpaymentpassrequestconfiguration/requiresfelicasecureelement)

##### Payment pass request properties

- [var cardholderName: String?](/documentation/passkit/pkaddpaymentpassrequestconfiguration/cardholdername)
- [var encryptionScheme: PKEncryptionScheme](/documentation/passkit/pkaddpaymentpassrequestconfiguration/encryptionscheme)
- [PKEncryptionScheme](/documentation/passkit/pkencryptionscheme)

###### Creating an encryption scheme

- [init(rawValue: String)](/documentation/passkit/pkencryptionscheme/init(rawvalue:))

###### Encryption schemes

- [static let ECC_V2: PKEncryptionScheme](/documentation/passkit/pkencryptionscheme/ecc_v2)
- [static let RSA_V2: PKEncryptionScheme](/documentation/passkit/pkencryptionscheme/rsa_v2)
- [var localizedDescription: String?](/documentation/passkit/pkaddpaymentpassrequestconfiguration/localizeddescription)
- [var primaryAccountSuffix: String?](/documentation/passkit/pkaddpaymentpassrequestconfiguration/primaryaccountsuffix)
- [var cardDetails: [PKLabeledValue]](/documentation/passkit/pkaddpaymentpassrequestconfiguration/carddetails)
- [PKLabeledValue](/documentation/passkit/pklabeledvalue)

###### Creating a labeled value

- [init(label: String, value: String)](/documentation/passkit/pklabeledvalue/init(label:value:))

###### Labeled value properties

- [var label: String](/documentation/passkit/pklabeledvalue/label)
- [var value: String](/documentation/passkit/pklabeledvalue/value)
- [var productIdentifiers: Set<String>](/documentation/passkit/pkaddpaymentpassrequestconfiguration/productidentifiers)
- [var style: PKAddPaymentPassStyle](/documentation/passkit/pkaddpaymentpassrequestconfiguration/style)
- [PKAddPaymentPassStyle](/documentation/passkit/pkaddpaymentpassstyle)

###### Payment pass styles

- [case access](/documentation/passkit/pkaddpaymentpassstyle/access)
- [case payment](/documentation/passkit/pkaddpaymentpassstyle/payment)

###### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddpaymentpassstyle/init(rawvalue:))

### Stored-value passes

- [PKTransitPassProperties](/documentation/passkit/pktransitpassproperties)

#### Getting pass status

- [var expirationDate: Date?](/documentation/passkit/pktransitpassproperties/expirationdate)
- [var isInStation: Bool](/documentation/passkit/pktransitpassproperties/isinstation)
- [var isBlocked: Bool](/documentation/passkit/pktransitpassproperties/isblocked)
- [var isBlacklisted: Bool](/documentation/passkit/pktransitpassproperties/isblacklisted)

#### Getting balance information

- [var transitBalance: NSDecimalNumber](/documentation/passkit/pktransitpassproperties/transitbalance)
- [var transitBalanceCurrencyCode: String](/documentation/passkit/pktransitpassproperties/transitbalancecurrencycode)
- [PKSuicaPassProperties](/documentation/passkit/pksuicapassproperties)

#### Initializing suica pass properties

- [convenience init?(for: PKPass)](/documentation/passkit/pksuicapassproperties/init(for:))

#### Getting pass status

- [var isBlocked: Bool](/documentation/passkit/pksuicapassproperties/isblocked)
- [var isBlacklisted: Bool](/documentation/passkit/pksuicapassproperties/isblacklisted)
- [var isGreenCarTicketUsed: Bool](/documentation/passkit/pksuicapassproperties/isgreencarticketused)
- [var isInShinkansenStation: Bool](/documentation/passkit/pksuicapassproperties/isinshinkansenstation)
- [var isInStation: Bool](/documentation/passkit/pksuicapassproperties/isinstation)

#### Getting suica balance information

- [var transitBalance: NSDecimalNumber](/documentation/passkit/pksuicapassproperties/transitbalance)
- [var transitBalanceCurrencyCode: String](/documentation/passkit/pksuicapassproperties/transitbalancecurrencycode)
- [var isBalanceAllowedForCommute: Bool](/documentation/passkit/pksuicapassproperties/isbalanceallowedforcommute)
- [var isLowBalanceGateNotificationEnabled: Bool](/documentation/passkit/pksuicapassproperties/islowbalancegatenotificationenabled)
- [PKStoredValuePassProperties](/documentation/passkit/pkstoredvaluepassproperties)

#### Creating a stored-value pass properties object

- [convenience init?(for: PKPass)](/documentation/passkit/pkstoredvaluepassproperties/init(for:))

#### Reading the stored-value pass properties

- [var balances: [PKStoredValuePassBalance]](/documentation/passkit/pkstoredvaluepassproperties/balances)
- [var expirationDate: Date?](/documentation/passkit/pkstoredvaluepassproperties/expirationdate)
- [var isBlocked: Bool](/documentation/passkit/pkstoredvaluepassproperties/isblocked)
- [var isBlacklisted: Bool](/documentation/passkit/pkstoredvaluepassproperties/isblacklisted)
- [PKStoredValuePassBalance](/documentation/passkit/pkstoredvaluepassbalance)

#### Getting the pass status

- [var expiryDate: Date?](/documentation/passkit/pkstoredvaluepassbalance/expirydate)
- [var amount: Decimal](/documentation/passkit/pkstoredvaluepassbalance/amount-2nwf5)
- [var balanceType: PKStoredValuePassBalance.BalanceType](/documentation/passkit/pkstoredvaluepassbalance/balancetype-swift.property)
- [var currencyCode: String?](/documentation/passkit/pkstoredvaluepassbalance/currencycode)
- [PKStoredValuePassBalance.BalanceType](/documentation/passkit/pkstoredvaluepassbalance/balancetype-swift.struct)

##### Creating a balance type

- [init(rawValue: String)](/documentation/passkit/pkstoredvaluepassbalance/balancetype-swift.struct/init(rawvalue:))

##### Reading the balance type

- [static let cash: PKStoredValuePassBalance.BalanceType](/documentation/passkit/pkstoredvaluepassbalance/balancetype-swift.struct/cash)
- [static let loyaltyPoints: PKStoredValuePassBalance.BalanceType](/documentation/passkit/pkstoredvaluepassbalance/balancetype-swift.struct/loyaltypoints)

#### Comparing pass balance objects

- [static func == (PKStoredValuePassBalance, PKStoredValuePassBalance) -> Bool](/documentation/passkit/pkstoredvaluepassbalance/==(_:_:))

### Shareable passes

- [PKAddShareablePassConfiguration](/documentation/passkit/pkaddshareablepassconfiguration)

#### Creating a pass configuration

- [class func forPassMetaData([PKShareablePassMetadata], provisioningPolicyIdentifier: String, action: PKAddShareablePassConfigurationPrimaryAction, completion: (PKAddShareablePassConfiguration?, (any Error)?) -> Void)](/documentation/passkit/pkaddshareablepassconfiguration/forpassmetadata(_:provisioningpolicyidentifier:action:completion:))
- [var primaryAction: PKAddShareablePassConfigurationPrimaryAction](/documentation/passkit/pkaddshareablepassconfiguration/primaryaction)
- [var credentialsMetadata: [PKShareablePassMetadata]](/documentation/passkit/pkaddshareablepassconfiguration/credentialsmetadata)
- [var provisioningPolicyIdentifier: String](/documentation/passkit/pkaddshareablepassconfiguration/provisioningpolicyidentifier)

#### Type Methods

- [class func forPassMetadata([PKShareablePassMetadata], action: PKAddShareablePassConfigurationPrimaryAction, completion: (PKAddShareablePassConfiguration?, (any Error)?) -> Void)](/documentation/passkit/pkaddshareablepassconfiguration/forpassmetadata(_:action:completion:))
- [PKShareablePassMetadata](/documentation/passkit/pkshareablepassmetadata)

#### Creating a shareable pass metadata object

- [init?(provisioningCredentialIdentifier: String, cardConfigurationIdentifier: String, sharingInstanceIdentifier: String, passThumbnailImage: CGImage, ownerDisplayName: String, localizedDescription: String)](/documentation/passkit/pkshareablepassmetadata/init(provisioningcredentialidentifier:cardconfigurationidentifier:sharinginstanceidentifier:passthumbnailimage:ownerdisplayname:localizeddescription:))
- [init(provisioningCredentialIdentifier: String, sharingInstanceIdentifier: String, passThumbnailImage: CGImage, ownerDisplayName: String, localizedDescription: String, accountHash: String, templateIdentifier: String, relyingPartyIdentifier: String, requiresUnifiedAccessCapableDevice: Bool)](/documentation/passkit/pkshareablepassmetadata/init(provisioningcredentialidentifier:sharinginstanceidentifier:passthumbnailimage:ownerdisplayname:localizeddescription:accounthash:templateidentifier:relyingpartyidentifier:requiresunifiedaccesscapabledevice:))

#### Displaying information on the share sheet

- [var ownerDisplayName: String](/documentation/passkit/pkshareablepassmetadata/ownerdisplayname)
- [var passThumbnailImage: CGImage](/documentation/passkit/pkshareablepassmetadata/passthumbnailimage)
- [var localizedDescription: String](/documentation/passkit/pkshareablepassmetadata/localizeddescription)

#### Reading notification properties

- [var accountHash: String](/documentation/passkit/pkshareablepassmetadata/accounthash)
- [var relyingPartyIdentifier: String](/documentation/passkit/pkshareablepassmetadata/relyingpartyidentifier)
- [var templateIdentifier: String](/documentation/passkit/pkshareablepassmetadata/templateidentifier)
- [var cardTemplateIdentifier: String](/documentation/passkit/pkshareablepassmetadata/cardtemplateidentifier)

#### Requiring a unified access capable device

- [var requiresUnifiedAccessCapableDevice: Bool](/documentation/passkit/pkshareablepassmetadata/requiresunifiedaccesscapabledevice)

#### Initializers

- [init(provisioningCredentialIdentifier: String, sharingInstanceIdentifier: String, cardConfigurationIdentifier: String, preview: PKShareablePassMetadata.Preview)](/documentation/passkit/pkshareablepassmetadata/init(provisioningcredentialidentifier:sharinginstanceidentifier:cardconfigurationidentifier:preview:))
- [init(provisioningCredentialIdentifier: String, sharingInstanceIdentifier: String, cardTemplateIdentifier: String, preview: PKShareablePassMetadata.Preview)](/documentation/passkit/pkshareablepassmetadata/init(provisioningcredentialidentifier:sharinginstanceidentifier:cardtemplateidentifier:preview:))

#### Instance Properties

- [var cardConfigurationIdentifier: String](/documentation/passkit/pkshareablepassmetadata/cardconfigurationidentifier)
- [var credentialIdentifier: String](/documentation/passkit/pkshareablepassmetadata/credentialidentifier)
- [var preview: PKShareablePassMetadata.Preview](/documentation/passkit/pkshareablepassmetadata/preview-swift.property)
- [var serverEnvironmentIdentifier: String](/documentation/passkit/pkshareablepassmetadata/serverenvironmentidentifier)
- [var sharingInstanceIdentifier: String](/documentation/passkit/pkshareablepassmetadata/sharinginstanceidentifier)
- [PKAddShareablePassConfigurationPrimaryAction](/documentation/passkit/pkaddshareablepassconfigurationprimaryaction)

#### Shareable pass configuration actions

- [case add](/documentation/passkit/pkaddshareablepassconfigurationprimaryaction/add)
- [case share](/documentation/passkit/pkaddshareablepassconfigurationprimaryaction/share)

#### Initializers

- [init?(rawValue: UInt)](/documentation/passkit/pkaddshareablepassconfigurationprimaryaction/init(rawvalue:))

### Digital car keys

- [PKAddCarKeyPassConfiguration](/documentation/passkit/pkaddcarkeypassconfiguration)

#### Creating a pass configuration

- [init()](/documentation/passkit/pkaddcarkeypassconfiguration/init())

#### Setting the wireless radio technology

- [var supportedRadioTechnologies: PKRadioTechnology](/documentation/passkit/pkaddcarkeypassconfiguration/supportedradiotechnologies)
- [PKRadioTechnology](/documentation/passkit/pkradiotechnology)

##### Reading the radio technology type

- [static var NFC: PKRadioTechnology](/documentation/passkit/pkradiotechnology/nfc)
- [static var bluetooth: PKRadioTechnology](/documentation/passkit/pkradiotechnology/bluetooth)

##### Creating a radio technology object

- [init(rawValue: UInt)](/documentation/passkit/pkradiotechnology/init(rawvalue:))

#### Managing the password

- [var password: String](/documentation/passkit/pkaddcarkeypassconfiguration/password)

#### Setting the provisioning template

- [var provisioningTemplateIdentifier: String?](/documentation/passkit/pkaddcarkeypassconfiguration/provisioningtemplateidentifier)

#### Instance Properties

- [var manufacturerIdentifier: String](/documentation/passkit/pkaddcarkeypassconfiguration/manufactureridentifier)
- [PKVehicleConnectionSession](/documentation/passkit/pkvehicleconnectionsession)

#### Instance Properties

- [var connectionStatus: PKVehicleConnectionSessionConnectionState](/documentation/passkit/pkvehicleconnectionsession/connectionstatus)
- [var delegate: (any PKVehicleConnectionDelegate)?](/documentation/passkit/pkvehicleconnectionsession/delegate)

#### Instance Methods

- [func invalidate()](/documentation/passkit/pkvehicleconnectionsession/invalidate())
- [func send(Data) throws](/documentation/passkit/pkvehicleconnectionsession/send(_:))

#### Type Methods

- [class func session(for: PKSecureElementPass, delegate: any PKVehicleConnectionDelegate, completion: (PKVehicleConnectionSession?, (any Error)?) -> Void)](/documentation/passkit/pkvehicleconnectionsession/session(for:delegate:completion:))
- [PKVehicleConnectionDelegate](/documentation/passkit/pkvehicleconnectiondelegate)

#### Instance Methods

- [func sessionDidChange(PKVehicleConnectionSessionConnectionState)](/documentation/passkit/pkvehicleconnectiondelegate/sessiondidchange(_:))
- [func sessionDidReceive(Data)](/documentation/passkit/pkvehicleconnectiondelegate/sessiondidreceive(_:))
- [PKVehicleConnectionSessionConnectionState](/documentation/passkit/pkvehicleconnectionsessionconnectionstate)

#### Enumeration Cases

- [case connected](/documentation/passkit/pkvehicleconnectionsessionconnectionstate/connected)
- [case connecting](/documentation/passkit/pkvehicleconnectionsessionconnectionstate/connecting)
- [case disconnected](/documentation/passkit/pkvehicleconnectionsessionconnectionstate/disconnected)
- [case failedToConnect](/documentation/passkit/pkvehicleconnectionsessionconnectionstate/failedtoconnect)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkvehicleconnectionsessionconnectionstate/init(rawvalue:))

### Issuer cards

- [Implementing Wallet Extensions](/documentation/passkit/implementing-wallet-extensions)
- [PKIssuerProvisioningExtensionHandler](/documentation/passkit/pkissuerprovisioningextensionhandler)

#### Returning extension status

- [func status(completion: (PKIssuerProvisioningExtensionStatus) -> Void)](/documentation/passkit/pkissuerprovisioningextensionhandler/status(completion:))
- [PKIssuerProvisioningExtensionStatus](/documentation/passkit/pkissuerprovisioningextensionstatus)

##### Creating an issuer extension provisioning status

- [init()](/documentation/passkit/pkissuerprovisioningextensionstatus/init())

##### Reporting pass availability

- [var passEntriesAvailable: Bool](/documentation/passkit/pkissuerprovisioningextensionstatus/passentriesavailable)
- [var remotePassEntriesAvailable: Bool](/documentation/passkit/pkissuerprovisioningextensionstatus/remotepassentriesavailable)

##### Reporting requirements for authentication

- [var requiresAuthentication: Bool](/documentation/passkit/pkissuerprovisioningextensionstatus/requiresauthentication)

#### Returning available passes

- [func passEntries(completion: ([PKIssuerProvisioningExtensionPassEntry]) -> Void)](/documentation/passkit/pkissuerprovisioningextensionhandler/passentries(completion:))
- [func remotePassEntries(completion: ([PKIssuerProvisioningExtensionPassEntry]) -> Void)](/documentation/passkit/pkissuerprovisioningextensionhandler/remotepassentries(completion:))
- [PKIssuerProvisioningExtensionPassEntry](/documentation/passkit/pkissuerprovisioningextensionpassentry)

##### Information for displaying an addable card

- [var art: CGImage](/documentation/passkit/pkissuerprovisioningextensionpassentry/art)
- [var title: String](/documentation/passkit/pkissuerprovisioningextensionpassentry/title)
- [var identifier: String](/documentation/passkit/pkissuerprovisioningextensionpassentry/identifier)
- [PKIssuerProvisioningExtensionPaymentPassEntry](/documentation/passkit/pkissuerprovisioningextensionpaymentpassentry)

##### Creating a payment pass entry

- [init?(identifier: String, title: String, art: CGImage, addRequestConfiguration: PKAddPaymentPassRequestConfiguration)](/documentation/passkit/pkissuerprovisioningextensionpaymentpassentry/init(identifier:title:art:addrequestconfiguration:))

##### Getting the pass entry configuration

- [var addRequestConfiguration: PKAddPaymentPassRequestConfiguration](/documentation/passkit/pkissuerprovisioningextensionpaymentpassentry/addrequestconfiguration)

#### Returning information for adding a pass

- [func generateAddPaymentPassRequestForPassEntryWithIdentifier(String, configuration: PKAddPaymentPassRequestConfiguration, certificateChain: [Data], nonce: Data, nonceSignature: Data, completionHandler: (PKAddPaymentPassRequest?) -> Void)](/documentation/passkit/pkissuerprovisioningextensionhandler/generateaddpaymentpassrequestforpassentrywithidentifier(_:configuration:certificatechain:nonce:noncesignature:completionhandler:))
- [PKIssuerProvisioningExtensionAuthorizationProviding](/documentation/passkit/pkissuerprovisioningextensionauthorizationproviding)

#### Providing the result of authorization

- [var completionHandler: ((PKIssuerProvisioningExtensionAuthorizationResult) -> Void)?](/documentation/passkit/pkissuerprovisioningextensionauthorizationproviding/completionhandler)
- [PKIssuerProvisioningExtensionAuthorizationResult](/documentation/passkit/pkissuerprovisioningextensionauthorizationresult)

##### Authorization results

- [case authorized](/documentation/passkit/pkissuerprovisioningextensionauthorizationresult/authorized)
- [case canceled](/documentation/passkit/pkissuerprovisioningextensionauthorizationresult/canceled)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkissuerprovisioningextensionauthorizationresult/init(rawvalue:))

### Errors

- [PKPassKitError](/documentation/passkit/pkpasskiterror)

#### Creating a pass error object

- [init(Code, userInfo: [String : Any])](/documentation/passkit_apple_pay_and_wallet/pkpasskiterror/3727669-init)

#### Error information

- [var errorCode: Int](/documentation/foundation/customnserror/errorcode-2opgi)
- [var userInfo: [String : Any]](/documentation/passkit_apple_pay_and_wallet/pkpasskiterror/3727670-userinfo)
- [var errorUserInfo: [String : Any]](/documentation/foundation/customnserror/erroruserinfo-1aas5)

#### Error codes

- [static var invalidDataError: PKPassKitError.Code](/documentation/passkit/pkpasskiterror/invaliddataerror)
- [static var invalidSignature: PKPassKitError.Code](/documentation/passkit/pkpasskiterror/invalidsignature)
- [static var notEntitledError: PKPassKitError.Code](/documentation/passkit/pkpasskiterror/notentitlederror)
- [static var unknownError: PKPassKitError.Code](/documentation/passkit/pkpasskiterror/unknownerror)
- [static var unsupportedVersionError: PKPassKitError.Code](/documentation/passkit/pkpasskiterror/unsupportedversionerror)
- [PKPassKitError.Code](/documentation/passkit/pkpasskiterror/code)

##### Error codes

- [case unknownError](/documentation/passkit/pkpasskiterror/code/unknownerror)
- [case invalidDataError](/documentation/passkit/pkpasskiterror/code/invaliddataerror)
- [case unsupportedVersionError](/documentation/passkit/pkpasskiterror/code/unsupportedversionerror)
- [case invalidSignature](/documentation/passkit/pkpasskiterror/code/invalidsignature)
- [case notEntitledError](/documentation/passkit/pkpasskiterror/code/notentitlederror)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpasskiterror/code/init(rawvalue:))
- [PKAddPaymentPassError](/documentation/passkit/pkaddpaymentpasserror)

##### Error codes

- [case unsupported](/documentation/passkit/pkaddpaymentpasserror/unsupported)
- [case userCancelled](/documentation/passkit/pkaddpaymentpasserror/usercancelled)
- [case systemCancelled](/documentation/passkit/pkaddpaymentpasserror/systemcancelled)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddpaymentpasserror/init(rawvalue:))

#### Error domain

- [let PKPassKitErrorDomain: String](/documentation/passkit/pkpasskiterrordomain)

#### Comparison operator

- [static func == (PKPassKitError, PKPassKitError) -> Bool](/documentation/passkit_apple_pay_and_wallet/pkpasskiterror/3727665)

#### Hashing

- [func hash(into: inout Hasher)](/documentation/passkit_apple_pay_and_wallet/pkpasskiterror/3727667-hash)
- [var hashValue: Int](/documentation/passkit_apple_pay_and_wallet/pkpasskiterror/3727668-hashvalue)

#### Type Properties

- [static var errorDomain: String](/documentation/passkit/pkpasskiterror/errordomain)
- [PKAddSecureElementPassError](/documentation/passkit/pkaddsecureelementpasserror)

#### Creating a secure element pass error object

- [init(Code, userInfo: [String : Any])](/documentation/passkit_apple_pay_and_wallet/pkaddsecureelementpasserror/3727663-init)

#### Identifying errors

- [static var deviceNotReadyError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/devicenotreadyerror)
- [static var deviceNotSupportedError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/devicenotsupportederror)
- [static var invalidConfigurationError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/invalidconfigurationerror)
- [static var unavailableError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/unavailableerror)
- [static var unknownError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/unknownerror)
- [static var userCanceledError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/usercancelederror)
- [PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/code)

##### Error codes

- [case deviceNotReadyError](/documentation/passkit/pkaddsecureelementpasserror/code/devicenotreadyerror)
- [case deviceNotSupportedError](/documentation/passkit/pkaddsecureelementpasserror/code/devicenotsupportederror)
- [case genericError](/documentation/passkit/pkaddsecureelementpasserror/code/genericerror)
- [case invalidConfigurationError](/documentation/passkit/pkaddsecureelementpasserror/code/invalidconfigurationerror)
- [case osVersionNotSupportedError](/documentation/passkit/pkaddsecureelementpasserror/code/osversionnotsupportederror)
- [case unavailableError](/documentation/passkit/pkaddsecureelementpasserror/code/unavailableerror)
- [case userCanceledError](/documentation/passkit/pkaddsecureelementpasserror/code/usercancelederror)
- [static var unknownError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/code/unknownerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddsecureelementpasserror/code/init(rawvalue:))

#### Getting error information

- [var errorCode: Int](/documentation/foundation/customnserror/errorcode-2opgi)
- [var userInfo: [String : Any]](/documentation/passkit_apple_pay_and_wallet/pkaddsecureelementpasserror/3727664-userinfo)
- [var errorUserInfo: [String : Any]](/documentation/foundation/customnserror/erroruserinfo-1aas5)
- [let PKAddSecureElementPassErrorDomain: String](/documentation/passkit/pkaddsecureelementpasserrordomain)

#### Comparing errors

- [static func == (PKAddSecureElementPassError, PKAddSecureElementPassError) -> Bool](/documentation/passkit_apple_pay_and_wallet/pkaddsecureelementpasserror/3727659)

#### Hashing

- [func hash(into: inout Hasher)](/documentation/passkit_apple_pay_and_wallet/pkaddsecureelementpasserror/3727661-hash)
- [var hashValue: Int](/documentation/passkit_apple_pay_and_wallet/pkaddsecureelementpasserror/3727662-hashvalue)

#### Type Properties

- [static var errorDomain: String](/documentation/passkit/pkaddsecureelementpasserror/errordomain)
- [static var genericError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/genericerror)
- [static var osVersionNotSupportedError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/osversionnotsupportederror)
- [PKPassKitError.Code](/documentation/passkit/pkpasskiterror/code)

#### Error codes

- [case unknownError](/documentation/passkit/pkpasskiterror/code/unknownerror)
- [case invalidDataError](/documentation/passkit/pkpasskiterror/code/invaliddataerror)
- [case unsupportedVersionError](/documentation/passkit/pkpasskiterror/code/unsupportedversionerror)
- [case invalidSignature](/documentation/passkit/pkpasskiterror/code/invalidsignature)
- [case notEntitledError](/documentation/passkit/pkpasskiterror/code/notentitlederror)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpasskiterror/code/init(rawvalue:))
- [PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/code)

#### Error codes

- [case deviceNotReadyError](/documentation/passkit/pkaddsecureelementpasserror/code/devicenotreadyerror)
- [case deviceNotSupportedError](/documentation/passkit/pkaddsecureelementpasserror/code/devicenotsupportederror)
- [case genericError](/documentation/passkit/pkaddsecureelementpasserror/code/genericerror)
- [case invalidConfigurationError](/documentation/passkit/pkaddsecureelementpasserror/code/invalidconfigurationerror)
- [case osVersionNotSupportedError](/documentation/passkit/pkaddsecureelementpasserror/code/osversionnotsupportederror)
- [case unavailableError](/documentation/passkit/pkaddsecureelementpasserror/code/unavailableerror)
- [case userCanceledError](/documentation/passkit/pkaddsecureelementpasserror/code/usercancelederror)
- [static var unknownError: PKAddSecureElementPassError.Code](/documentation/passkit/pkaddsecureelementpasserror/code/unknownerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddsecureelementpasserror/code/init(rawvalue:))
- [PKAddPaymentPassError](/documentation/passkit/pkaddpaymentpasserror)

#### Error codes

- [case unsupported](/documentation/passkit/pkaddpaymentpasserror/unsupported)
- [case userCancelled](/documentation/passkit/pkaddpaymentpasserror/usercancelled)
- [case systemCancelled](/documentation/passkit/pkaddpaymentpasserror/systemcancelled)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkaddpaymentpasserror/init(rawvalue:))
- [PKIdentityError](/documentation/passkit/pkidentityerror-swift.struct)

#### Inspecting an error

- [PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/code)

##### Error codes

- [case cancelled](/documentation/passkit/pkidentityerror-swift.struct/code/cancelled)
- [case invalidElement](/documentation/passkit/pkidentityerror-swift.struct/code/invalidelement)
- [case invalidNonce](/documentation/passkit/pkidentityerror-swift.struct/code/invalidnonce)
- [case notSupported](/documentation/passkit/pkidentityerror-swift.struct/code/notsupported)
- [case networkUnavailable](/documentation/passkit/pkidentityerror-swift.struct/code/networkunavailable)
- [case noElementsRequested](/documentation/passkit/pkidentityerror-swift.struct/code/noelementsrequested)
- [case requestAlreadyInProgress](/documentation/passkit/pkidentityerror-swift.struct/code/requestalreadyinprogress)
- [case unknown](/documentation/passkit/pkidentityerror-swift.struct/code/unknown)

##### Enumeration Cases

- [case regionNotSupported](/documentation/passkit/pkidentityerror-swift.struct/code/regionnotsupported)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkidentityerror-swift.struct/code/init(rawvalue:))
- [Error constants](/documentation/passkit/error-constants)

##### Constants

- [static var cancelled: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/cancelled)
- [static var invalidElement: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/invalidelement)
- [static var invalidNonce: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/invalidnonce)
- [static var notSupported: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/notsupported)
- [static var networkUnavailable: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/networkunavailable)
- [static var noElementsRequested: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/noelementsrequested)
- [static var requestAlreadyInProgress: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/requestalreadyinprogress)
- [static var unknown: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/unknown)
- [var errorCode: Int](/documentation/foundation/customnserror/errorcode-2opgi)
- [var userInfo: [String : Any]](/documentation/passkit_apple_pay_and_wallet/pkidentityerror/3931651-userinfo)
- [var errorUserInfo: [String : Any]](/documentation/foundation/customnserror/erroruserinfo-1aas5)

#### Comparing errors

- [static func == (PKIdentityError, PKIdentityError) -> Bool](/documentation/passkit_apple_pay_and_wallet/pkidentityerror/3931635)

#### Accessing the hash value

- [func hash(into: inout Hasher)](/documentation/passkit_apple_pay_and_wallet/pkidentityerror/3931641-hash)
- [var hashValue: Int](/documentation/passkit_apple_pay_and_wallet/pkidentityerror/3931642-hashvalue)

#### Creating an identity error

- [init(Code, userInfo: [String : Any])](/documentation/passkit_apple_pay_and_wallet/pkidentityerror/3931643-init)

#### Type Properties

- [static var errorDomain: String](/documentation/passkit/pkidentityerror-swift.struct/errordomain)
- [static var regionNotSupported: PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/regionnotsupported)
- [PKIdentityError.Code](/documentation/passkit/pkidentityerror-swift.struct/code)

#### Error codes

- [case cancelled](/documentation/passkit/pkidentityerror-swift.struct/code/cancelled)
- [case invalidElement](/documentation/passkit/pkidentityerror-swift.struct/code/invalidelement)
- [case invalidNonce](/documentation/passkit/pkidentityerror-swift.struct/code/invalidnonce)
- [case notSupported](/documentation/passkit/pkidentityerror-swift.struct/code/notsupported)
- [case networkUnavailable](/documentation/passkit/pkidentityerror-swift.struct/code/networkunavailable)
- [case noElementsRequested](/documentation/passkit/pkidentityerror-swift.struct/code/noelementsrequested)
- [case requestAlreadyInProgress](/documentation/passkit/pkidentityerror-swift.struct/code/requestalreadyinprogress)
- [case unknown](/documentation/passkit/pkidentityerror-swift.struct/code/unknown)

#### Enumeration Cases

- [case regionNotSupported](/documentation/passkit/pkidentityerror-swift.struct/code/regionnotsupported)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkidentityerror-swift.struct/code/init(rawvalue:))
- [PKShareSecureElementPassError](/documentation/passkit/pksharesecureelementpasserror)

#### Type Properties

- [static var errorDomain: String](/documentation/passkit/pksharesecureelementpasserror/errordomain)
- [static var setupError: PKShareSecureElementPassError.Code](/documentation/passkit/pksharesecureelementpasserror/setuperror)
- [static var unknownError: PKShareSecureElementPassError.Code](/documentation/passkit/pksharesecureelementpasserror/unknownerror)
- [PKShareSecureElementPassError.Code](/documentation/passkit/pksharesecureelementpasserror/code)

#### Enumeration Cases

- [case setupError](/documentation/passkit/pksharesecureelementpasserror/code/setuperror)
- [case unknownError](/documentation/passkit/pksharesecureelementpasserror/code/unknownerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pksharesecureelementpasserror/code/init(rawvalue:))
- [PKVehicleConnectionErrorCode](/documentation/passkit/pkvehicleconnectionerrorcode)

#### Enumeration Cases

- [case sessionNotActive](/documentation/passkit/pkvehicleconnectionerrorcode/sessionnotactive)
- [case sessionUnableToStart](/documentation/passkit/pkvehicleconnectionerrorcode/sessionunabletostart)
- [case unknown](/documentation/passkit/pkvehicleconnectionerrorcode/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkvehicleconnectionerrorcode/init(rawvalue:))
- [PayWithApplePayButtonPaymentAuthorizationPhase](/documentation/passkit/paywithapplepaybuttonpaymentauthorizationphase)

#### Enumeration Cases

- [case didAuthorize(payment: PKPayment, resultHandler: (PKPaymentAuthorizationResult) -> Void)](/documentation/passkit/paywithapplepaybuttonpaymentauthorizationphase/didauthorize(payment:resulthandler:))
- [case didFinish](/documentation/passkit/paywithapplepaybuttonpaymentauthorizationphase/didfinish)
- [case willAuthorize](/documentation/passkit/paywithapplepaybuttonpaymentauthorizationphase/willauthorize)
- [let PKPassKitErrorDomain: String](/documentation/passkit/pkpasskiterrordomain)
- [let PKIdentityErrorDomain: String](/documentation/passkit/pkidentityerrordomain)
- [let PKAddSecureElementPassErrorDomain: String](/documentation/passkit/pkaddsecureelementpasserrordomain)
- [let PKShareSecureElementPassErrorDomain: String](/documentation/passkit/pksharesecureelementpasserrordomain)

### Deprecated

- [PayLaterView](/documentation/passkit/paylaterview)

#### Setting the view’s action

- [PayLaterViewAction](/documentation/passkit/paylaterviewaction)

##### Pay Later actions

- [static let calculator: PayLaterViewAction](/documentation/passkit/paylaterviewaction/calculator)
- [static let learnMore: PayLaterViewAction](/documentation/passkit/paylaterviewaction/learnmore)

#### Styling the view

- [PayLaterViewDisplayStyle](/documentation/passkit/paylaterviewdisplaystyle)

##### Payment display styles

- [static let standard: PayLaterViewDisplayStyle](/documentation/passkit/paylaterviewdisplaystyle/standard)
- [static let badge: PayLaterViewDisplayStyle](/documentation/passkit/paylaterviewdisplaystyle/badge)
- [static let checkout: PayLaterViewDisplayStyle](/documentation/passkit/paylaterviewdisplaystyle/checkout)
- [static let price: PayLaterViewDisplayStyle](/documentation/passkit/paylaterviewdisplaystyle/price)

#### Initializers

- [init(amount: Decimal, currency: Locale.Currency)](/documentation/passkit/paylaterview/init(amount:currency:))
- [PKPayLaterView](/documentation/passkit/pkpaylaterview)

#### Creating the widget

- [convenience init(amount: Decimal, currency: Locale.Currency)](/documentation/passkit/pkpaylaterview/init(amount:currency:))

#### Accessing information about the transaction

- [var amount: Decimal](/documentation/passkit/pkpaylaterview/amount-f3gs)
- [var currency: Locale.Currency](/documentation/passkit/pkpaylaterview/currency)

#### Responding to changes in the view’s height

- [var delegate: any PKPayLaterViewDelegate](/documentation/passkit/pkpaylaterview/delegate)
- [PKPayLaterViewDelegate](/documentation/passkit/pkpaylaterviewdelegate)

##### Responding to view size changes

- [func payLaterViewDidUpdateHeight(PKPayLaterView)](/documentation/passkit/pkpaylaterviewdelegate/paylaterviewdidupdateheight(_:))

#### Setting the user action

- [var action: PKPayLaterAction](/documentation/passkit/pkpaylaterview/action)
- [PKPayLaterAction](/documentation/passkit/pkpaylateraction)

##### Widget behaviors

- [case calculator](/documentation/passkit/pkpaylateraction/calculator)
- [case learnMore](/documentation/passkit/pkpaylateraction/learnmore)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaylateraction/init(rawvalue:))

#### Styling the view

- [var displayStyle: PKPayLaterDisplayStyle](/documentation/passkit/pkpaylaterview/displaystyle)
- [PKPayLaterDisplayStyle](/documentation/passkit/pkpaylaterdisplaystyle)

##### Payment view display styles

- [case standard](/documentation/passkit/pkpaylaterdisplaystyle/standard)
- [case badge](/documentation/passkit/pkpaylaterdisplaystyle/badge)
- [case checkout](/documentation/passkit/pkpaylaterdisplaystyle/checkout)
- [case price](/documentation/passkit/pkpaylaterdisplaystyle/price)

##### Initializers

- [init?(rawValue: Int)](/documentation/passkit/pkpaylaterdisplaystyle/init(rawvalue:))

#### Validating transactions

- [PKPayLater](/documentation/passkit/pkpaylater)

##### Utilities

- [static func validate(amount: Decimal, currency: Locale.Currency) async -> Bool](/documentation/passkit/pkpaylater/validate(amount:currency:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
