# DataDetection Documentation

Source: https://sosumi.ai/documentation/datadetection

---
title: DataDetection
source: https://developer.apple.com/documentation/datadetection
timestamp: 2026-02-13T18:56:04.928Z
---

## Matched strings

- [DDMatch](/documentation/datadetection/ddmatch)

### Getting matches

- [var matchedString: String](/documentation/datadetection/ddmatch/matchedstring)
- [DataDetector](/documentation/datadetection/datadetector)

### Methods that scan strings for known content types

- [func dataDetectorMatches(DataDetector.MatchType, options: DataDetector.Options) -> some AsyncSequence<DataDetector.Match, Never>
](/documentation/swift/stringprotocol/datadetectormatches(_:options:))

### Structures

- [DataDetector.Match](/documentation/datadetection/datadetector/match)

#### Match details

- [let details: DataDetector.Match.SemanticDetails](/documentation/datadetection/datadetector/match/details)
- [let preferredHighlightStyle: DataDetector.Match.HighlightStyle](/documentation/datadetection/datadetector/match/preferredhighlightstyle)
- [let range: Range<String.Index>?](/documentation/datadetection/datadetector/match/range)

#### Values that describe highlighting and semantic details of matches

- [DataDetector.Match.HighlightStyle](/documentation/datadetection/datadetector/match/highlightstyle)

##### Enumeration Cases

- [case hidden](/documentation/datadetection/datadetector/match/highlightstyle/hidden)
- [case regular](/documentation/datadetection/datadetector/match/highlightstyle/regular)
- [case url](/documentation/datadetection/datadetector/match/highlightstyle/url)
- [DataDetector.Match.SemanticDetails](/documentation/datadetection/datadetector/match/semanticdetails)

##### Structures

- [DataDetector.Match.SemanticDetails.CalendarEvent](/documentation/datadetection/datadetector/match/semanticdetails/calendarevent)

###### Calendar event properties

- [let allDay: Bool](/documentation/datadetection/datadetector/match/semanticdetails/calendarevent/allday)
- [let startDate: Date?](/documentation/datadetection/datadetector/match/semanticdetails/calendarevent/startdate)
- [let endDate: Date?](/documentation/datadetection/datadetector/match/semanticdetails/calendarevent/enddate)
- [let startTimeZone: TimeZone?](/documentation/datadetection/datadetector/match/semanticdetails/calendarevent/starttimezone)
- [let endTimeZone: TimeZone?](/documentation/datadetection/datadetector/match/semanticdetails/calendarevent/endtimezone)
- [DataDetector.Match.SemanticDetails.EmailAddress](/documentation/datadetection/datadetector/match/semanticdetails/emailaddress)

###### Properties that describe an email address

- [let emailAddress: String](/documentation/datadetection/datadetector/match/semanticdetails/emailaddress/emailaddress)
- [let label: String?](/documentation/datadetection/datadetector/match/semanticdetails/emailaddress/label)
- [DataDetector.Match.SemanticDetails.FlightNumber](/documentation/datadetection/datadetector/match/semanticdetails/flightnumber)

###### Characteristics of a flight number

- [let airlineCode: String](/documentation/datadetection/datadetector/match/semanticdetails/flightnumber/airlinecode)
- [let flightNumber: Int](/documentation/datadetection/datadetector/match/semanticdetails/flightnumber/flightnumber)
- [DataDetector.Match.SemanticDetails.Link](/documentation/datadetection/datadetector/match/semanticdetails/link)

###### Getting the value of the original link

- [let url: URL](/documentation/datadetection/datadetector/match/semanticdetails/link/url)
- [DataDetector.Match.SemanticDetails.Measurement](/documentation/datadetection/datadetector/match/semanticdetails/measurement)

###### Values that describe the characteristics of the measurement

- [let possibleDimensions: [Dimension]](/documentation/datadetection/datadetector/match/semanticdetails/measurement/possibledimensions)
- [func measurement<D>(in: D) -> Measurement<D>](/documentation/datadetection/datadetector/match/semanticdetails/measurement/measurement(in:))
- [let value: Double](/documentation/datadetection/datadetector/match/semanticdetails/measurement/value)
- [DataDetector.Match.SemanticDetails.MoneyAmount](/documentation/datadetection/datadetector/match/semanticdetails/moneyamount)

###### Properties that describe elements of the amount

- [let amount: Decimal](/documentation/datadetection/datadetector/match/semanticdetails/moneyamount/amount)
- [let currency: Locale.Currency](/documentation/datadetection/datadetector/match/semanticdetails/moneyamount/currency)
- [DataDetector.Match.SemanticDetails.PaymentIdentifier](/documentation/datadetection/datadetector/match/semanticdetails/paymentidentifier)

###### null

- [let identifier: String](/documentation/datadetection/datadetector/match/semanticdetails/paymentidentifier/identifier)
- [let type: DataDetector.Match.SemanticDetails.PaymentIdentifier.PaymentSystem](/documentation/datadetection/datadetector/match/semanticdetails/paymentidentifier/type)

###### Enumerations

- [DataDetector.Match.SemanticDetails.PaymentIdentifier.PaymentSystem](/documentation/datadetection/datadetector/match/semanticdetails/paymentidentifier/paymentsystem)

###### Payment systems

- [case unifiedPaymentsInterface](/documentation/datadetection/datadetector/match/semanticdetails/paymentidentifier/paymentsystem/unifiedpaymentsinterface)
- [DataDetector.Match.SemanticDetails.PhoneNumber](/documentation/datadetection/datadetector/match/semanticdetails/phonenumber)

###### Components of a phone number

- [let phoneNumber: String](/documentation/datadetection/datadetector/match/semanticdetails/phonenumber/phonenumber)
- [let label: String?](/documentation/datadetection/datadetector/match/semanticdetails/phonenumber/label)
- [DataDetector.Match.SemanticDetails.PostalAddress](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress)

###### Properties that detail parts of a postal address

- [let fullAddress: String](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/fulladdress)
- [let street: String?](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/street)
- [let city: String?](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/city)
- [let state: String?](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/state)
- [let postalCode: String?](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/postalcode)
- [let region: String?](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/region)
- [let regionCode: Locale.Region?](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/regioncode)
- [let label: String?](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress/label)
- [DataDetector.Match.SemanticDetails.ShipmentTrackingNumber](/documentation/datadetection/datadetector/match/semanticdetails/shipmenttrackingnumber)

###### Properties that describe a shipment

- [let carrier: String](/documentation/datadetection/datadetector/match/semanticdetails/shipmenttrackingnumber/carrier)
- [let trackingNumber: String](/documentation/datadetection/datadetector/match/semanticdetails/shipmenttrackingnumber/trackingnumber)
- [let trackingURL: URL?](/documentation/datadetection/datadetector/match/semanticdetails/shipmenttrackingnumber/trackingurl)

##### Enumeration Cases

- [case calendarEvent(DataDetector.Match.SemanticDetails.CalendarEvent)](/documentation/datadetection/datadetector/match/semanticdetails/calendarevent(_:))
- [case emailAddress(DataDetector.Match.SemanticDetails.EmailAddress)](/documentation/datadetection/datadetector/match/semanticdetails/emailaddress(_:))
- [case flightNumber(DataDetector.Match.SemanticDetails.FlightNumber)](/documentation/datadetection/datadetector/match/semanticdetails/flightnumber(_:))
- [case link(DataDetector.Match.SemanticDetails.Link)](/documentation/datadetection/datadetector/match/semanticdetails/link(_:))
- [case measurement(DataDetector.Match.SemanticDetails.Measurement)](/documentation/datadetection/datadetector/match/semanticdetails/measurement(_:))
- [case moneyAmount(DataDetector.Match.SemanticDetails.MoneyAmount)](/documentation/datadetection/datadetector/match/semanticdetails/moneyamount(_:))
- [case paymentIdentifier(DataDetector.Match.SemanticDetails.PaymentIdentifier)](/documentation/datadetection/datadetector/match/semanticdetails/paymentidentifier(_:))
- [case phoneNumber(DataDetector.Match.SemanticDetails.PhoneNumber)](/documentation/datadetection/datadetector/match/semanticdetails/phonenumber(_:))
- [case postalAddress(DataDetector.Match.SemanticDetails.PostalAddress)](/documentation/datadetection/datadetector/match/semanticdetails/postaladdress(_:))
- [case shipmentTrackingNumber(DataDetector.Match.SemanticDetails.ShipmentTrackingNumber)](/documentation/datadetection/datadetector/match/semanticdetails/shipmenttrackingnumber(_:))
- [DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype)

#### Supported match types

- [static let all: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/all)
- [static let calendarEvent: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/calendarevent)
- [static let emailAddress: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/emailaddress)
- [static let flightNumber: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/flightnumber)
- [static let link: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/link)
- [static let measurement: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/measurement)
- [static let moneyAmount: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/moneyamount)
- [static let paymentIdentifier: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/paymentidentifier)
- [static let phoneNumber: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/phonenumber)
- [static let postalAddress: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/postaladdress)
- [static let shipmentTrackingNumber: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/shipmenttrackingnumber)
- [DataDetector.Options](/documentation/datadetection/datadetector/options)

#### Hints you can provide to add more context for the matching process

- [var documentDate: Date?](/documentation/datadetection/datadetector/options/documentdate)
- [var documentLanguageCode: Locale.LanguageCode?](/documentation/datadetection/datadetector/options/documentlanguagecode)
- [var documentRegion: Locale.Region?](/documentation/datadetection/datadetector/options/documentregion)
- [var documentTimeZone: TimeZone?](/documentation/datadetection/datadetector/options/documenttimezone)

#### Initializers

- [init()](/documentation/datadetection/datadetector/options/init())

### Known entity types

- [static let all: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/all)
- [static let link: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/link)
- [static let emailAddress: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/emailaddress)
- [static let phoneNumber: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/phonenumber)
- [static let postalAddress: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/postaladdress)
- [static let calendarEvent: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/calendarevent)
- [static let moneyAmount: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/moneyamount)
- [static let measurement: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/measurement)
- [static let flightNumber: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/flightnumber)
- [static let shipmentTrackingNumber: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/shipmenttrackingnumber)
- [static let paymentIdentifier: DataDetector.MatchType](/documentation/datadetection/datadetector/matchtype/paymentidentifier)

## Matched data types

- [DDMatchCalendarEvent](/documentation/datadetection/ddmatchcalendarevent)

### Getting event details

- [var isAllDay: Bool](/documentation/datadetection/ddmatchcalendarevent/isallday)
- [var endDate: Date?](/documentation/datadetection/ddmatchcalendarevent/enddate)
- [var endTimeZone: TimeZone?](/documentation/datadetection/ddmatchcalendarevent/endtimezone)
- [var startDate: Date?](/documentation/datadetection/ddmatchcalendarevent/startdate)
- [var startTimeZone: TimeZone?](/documentation/datadetection/ddmatchcalendarevent/starttimezone)
- [DDMatchEmailAddress](/documentation/datadetection/ddmatchemailaddress)

### Getting email information

- [var emailAddress: String](/documentation/datadetection/ddmatchemailaddress/emailaddress)
- [var label: String?](/documentation/datadetection/ddmatchemailaddress/label)
- [DDMatchFlightNumber](/documentation/datadetection/ddmatchflightnumber)

### Getting flight information

- [var airline: String](/documentation/datadetection/ddmatchflightnumber/airline)
- [var flightNumber: String](/documentation/datadetection/ddmatchflightnumber/flightnumber)
- [DDMatchLink](/documentation/datadetection/ddmatchlink)

### Getting link information

- [var url: URL](/documentation/datadetection/ddmatchlink/url)
- [DDMatchMoneyAmount](/documentation/datadetection/ddmatchmoneyamount)

### Getting money information

- [var amount: Double](/documentation/datadetection/ddmatchmoneyamount/amount)
- [var currency: String](/documentation/datadetection/ddmatchmoneyamount/currency)
- [DDMatchPhoneNumber](/documentation/datadetection/ddmatchphonenumber)

### Getting phone information

- [var phoneNumber: String](/documentation/datadetection/ddmatchphonenumber/phonenumber)
- [var label: String?](/documentation/datadetection/ddmatchphonenumber/label)
- [DDMatchPostalAddress](/documentation/datadetection/ddmatchpostaladdress)

### Getting postal address information

- [var street: String?](/documentation/datadetection/ddmatchpostaladdress/street)
- [var city: String?](/documentation/datadetection/ddmatchpostaladdress/city)
- [var state: String?](/documentation/datadetection/ddmatchpostaladdress/state)
- [var postalCode: String?](/documentation/datadetection/ddmatchpostaladdress/postalcode)
- [var country: String?](/documentation/datadetection/ddmatchpostaladdress/country)
- [DDMatchShipmentTrackingNumber](/documentation/datadetection/ddmatchshipmenttrackingnumber)

### Getting tracking information

- [var carrier: String](/documentation/datadetection/ddmatchshipmenttrackingnumber/carrier)
- [var trackingNumber: String](/documentation/datadetection/ddmatchshipmenttrackingnumber/trackingnumber)

## Pasteboard detectors

- [func detectPatterns(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>, completionHandler: (Result<Set<PartialKeyPath<UIPasteboard.DetectedValues>>, any Error>) -> ())](/documentation/uikit/uipasteboard/detectpatterns(for:completionhandler:)-23vwn)
- [func detectedPatterns(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>) async throws -> Set<PartialKeyPath<UIPasteboard.DetectedValues>>](/documentation/uikit/uipasteboard/detectedpatterns(for:))
- [func detectPatterns(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>, inItemSet: IndexSet?, completionHandler: (Result<[Set<PartialKeyPath<UIPasteboard.DetectedValues>>], any Error>) -> ())](/documentation/uikit/uipasteboard/detectpatterns(for:initemset:completionhandler:)-7ubl1)
- [func detectedPatterns(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>, inItemSet: IndexSet?) async throws -> [Set<PartialKeyPath<UIPasteboard.DetectedValues>>]](/documentation/uikit/uipasteboard/detectedpatterns(for:initemset:))
- [func detectValues(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>, completionHandler: (Result<UIPasteboard.DetectedValues, any Error>) -> ())](/documentation/uikit/uipasteboard/detectvalues(for:completionhandler:)-6adre)
- [func detectedValues(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>) async throws -> UIPasteboard.DetectedValues](/documentation/uikit/uipasteboard/detectedvalues(for:))
- [func detectValues(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>, inItemSet: IndexSet?, completionHandler: (Result<[UIPasteboard.DetectedValues], any Error>) -> ())](/documentation/uikit/uipasteboard/detectvalues(for:initemset:completionhandler:)-pm9l)
- [func detectedValues(for: Set<PartialKeyPath<UIPasteboard.DetectedValues>>, inItemSet: IndexSet?) async throws -> [UIPasteboard.DetectedValues]](/documentation/uikit/uipasteboard/detectedvalues(for:initemset:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
