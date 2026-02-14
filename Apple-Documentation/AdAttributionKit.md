# AdAttributionKit Documentation

Source: https://sosumi.ai/documentation/adattributionkit

---
title: AdAttributionKit
source: https://developer.apple.com/documentation/adattributionkit
timestamp: 2026-02-13T19:06:38.255Z
---

## Essentials

- [Understanding AdAttributionKit and SKAdNetwork interoperability](/documentation/adattributionkit/adattributionkit-skadnetwork-interoperability)
- [Presenting ads in your app](/documentation/adattributionkit/presenting-ads-in-your-app)
- [Receiving ad attributions and postbacks](/documentation/adattributionkit/receiving-ad-attributions-and-postbacks)
- [Identifying conversion values with conversion tags](/documentation/adattributionkit/conversion-tags)

## Ad network registration and configuration

- [Registering an ad network](/documentation/adattributionkit/registering-an-ad-network)
- [Configuring a publisher app](/documentation/adattributionkit/configuring-a-publisher-app)
- [Configuring an advertised app](/documentation/adattributionkit/configuring-an-advertised-app)
- [Configuring attribution rules for your app](/documentation/adattributionkit/configuring-attribution-rules-for-your-app)

## Ad attribution testing

- [Testing ad attributions with Developer Mode](/documentation/adattributionkit/testing-adattributionkit-with-developer-mode)
- [Creating postbacks in developer settings](/documentation/adattributionkit/creating-postbacks-in-developer-settings)
- [Testing ad attributions with a downloaded profile](/documentation/adattributionkit/testing-ad-attributions-with-a-downloaded-profile)

## Signatures

- [Generating JWS impressions](/documentation/adattributionkit/generating-jws-impressions)

## App impressions

- [AppImpression](/documentation/adattributionkit/appimpression)

### Creating an ad impression

- [init(compactJWS: String) async throws](/documentation/adattributionkit/appimpression/init(compactjws:))

### Displaying view-through ads

- [func beginView() async throws](/documentation/adattributionkit/appimpression/beginview())
- [func endView() async throws](/documentation/adattributionkit/appimpression/endview())
- [func handleView() async throws](/documentation/adattributionkit/appimpression/handleview())

### Processing interactions with click-through ads

- [func handleTap() async throws](/documentation/adattributionkit/appimpression/handletap())
- [func handleTap(reengagementURL: URL) async throws](/documentation/adattributionkit/appimpression/handletap(reengagementurl:))

### Accessing ad impression properties

- [var adNetworkID: String](/documentation/adattributionkit/appimpression/adnetworkid)
- [var advertisedItemID: UInt64](/documentation/adattributionkit/appimpression/advertiseditemid)
- [var compactJWSRepresentation: String](/documentation/adattributionkit/appimpression/compactjwsrepresentation)
- [var eligibleForReengagement: Bool](/documentation/adattributionkit/appimpression/eligibleforreengagement)
- [var id: UUID](/documentation/adattributionkit/appimpression/id)
- [var keyID: String](/documentation/adattributionkit/appimpression/keyid)
- [var publisherItemID: UInt64](/documentation/adattributionkit/appimpression/publisheritemid)
- [var sourceID: Int](/documentation/adattributionkit/appimpression/sourceid)
- [var timestamp: Date](/documentation/adattributionkit/appimpression/timestamp)

### Checking device support

- [static var isSupported: Bool](/documentation/adattributionkit/appimpression/issupported)

### Comparing and hashing ad impressions

- [static func == (AppImpression, AppImpression) -> Bool](/documentation/adattributionkit/appimpression/==(_:_:))
- [func hash(into: inout Hasher)](/documentation/adattributionkit/appimpression/hash(into:))

## Postbacks

- [Postback](/documentation/adattributionkit/postback)

### Type Properties

- [static var isSupported: Bool](/documentation/adattributionkit/postback/issupported)
- [static var reengagementOpenURLParameter: String](/documentation/adattributionkit/postback/reengagementopenurlparameter)

### Type Methods

- [static func updateConversionValue(PostbackUpdate) async throws](/documentation/adattributionkit/postback/updateconversionvalue(_:))
- [static func updateConversionValue(Int, coarseConversionValue: CoarseConversionValue, lockPostback: Bool) async throws](/documentation/adattributionkit/postback/updateconversionvalue(_:coarseconversionvalue:lockpostback:))
- [static func updateConversionValue(Int, lockPostback: Bool) async throws](/documentation/adattributionkit/postback/updateconversionvalue(_:lockpostback:))
- [PostbackUpdate](/documentation/adattributionkit/postbackupdate)

### Initializers

- [init(fineConversionValue: Int, lockPostback: Bool, coarseConversionValue: CoarseConversionValue?, conversionTypes: [PostbackUpdate.ConversionType]?)](/documentation/adattributionkit/postbackupdate/init(fineconversionvalue:lockpostback:coarseconversionvalue:conversiontypes:))
- [init(fineConversionValue: Int, lockPostback: Bool, conversionTag: String, coarseConversionValue: CoarseConversionValue?, conversionTypes: [PostbackUpdate.ConversionType]?)](/documentation/adattributionkit/postbackupdate/init(fineconversionvalue:lockpostback:conversiontag:coarseconversionvalue:conversiontypes:))

### Instance Properties

- [let coarseConversionValue: CoarseConversionValue?](/documentation/adattributionkit/postbackupdate/coarseconversionvalue)
- [let conversionTag: String?](/documentation/adattributionkit/postbackupdate/conversiontag)
- [let conversionTypes: [PostbackUpdate.ConversionType]?](/documentation/adattributionkit/postbackupdate/conversiontypes)
- [let fineConversionValue: Int](/documentation/adattributionkit/postbackupdate/fineconversionvalue)
- [let lockPostback: Bool](/documentation/adattributionkit/postbackupdate/lockpostback)

### Enumerations

- [PostbackUpdate.ConversionType](/documentation/adattributionkit/postbackupdate/conversiontype)

#### Enumeration Cases

- [case install](/documentation/adattributionkit/postbackupdate/conversiontype/install)
- [case reengagement](/documentation/adattributionkit/postbackupdate/conversiontype/reengagement)
- [CoarseConversionValue](/documentation/adattributionkit/coarseconversionvalue)

### Enumeration Cases

- [case high](/documentation/adattributionkit/coarseconversionvalue/high)
- [case low](/documentation/adattributionkit/coarseconversionvalue/low)
- [case medium](/documentation/adattributionkit/coarseconversionvalue/medium)

## Postback verification and parameter identification

- [Verifying a postback](/documentation/adattributionkit/verifying-a-postback)
- [Identifying the parameters in a postback](/documentation/adattributionkit/identifying-the-parameters-in-a-postback)

## Errors

- [AdAttributionKitError](/documentation/adattributionkit/adattributionkiterror)

### Enumeration Cases

- [case conversionTagNotSupported](/documentation/adattributionkit/adattributionkiterror/conversiontagnotsupported)
- [case impressionExpired](/documentation/adattributionkit/adattributionkiterror/impressionexpired)
- [case invalidConversionTag](/documentation/adattributionkit/adattributionkiterror/invalidconversiontag)
- [case invalidImpressionJWSComponents](/documentation/adattributionkit/adattributionkiterror/invalidimpressionjwscomponents)
- [case invalidImpressionJWSHeader](/documentation/adattributionkit/adattributionkiterror/invalidimpressionjwsheader)
- [case invalidImpressionJWSPayload](/documentation/adattributionkit/adattributionkiterror/invalidimpressionjwspayload)
- [case invalidImpressionJWSSignature](/documentation/adattributionkit/adattributionkiterror/invalidimpressionjwssignature)
- [case missingAttributionView](/documentation/adattributionkit/adattributionkiterror/missingattributionview)
- [case unknown](/documentation/adattributionkit/adattributionkiterror/unknown)

### Instance Properties

- [var description: String](/documentation/adattributionkit/adattributionkiterror/description)

## Articles

- [Receiving postbacks in multiple conversion windows](/documentation/adattributionkit/receiving-postbacks-in-multiple-conversion-windows)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
