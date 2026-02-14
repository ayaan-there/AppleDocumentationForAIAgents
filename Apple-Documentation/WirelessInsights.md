# WirelessInsights Documentation

Source: https://sosumi.ai/documentation/wirelessinsights

---
title: WirelessInsights
source: https://developer.apple.com/documentation/wirelessinsights
timestamp: 2026-02-13T19:04:18.627Z
---

## Essentials

- [ServicePredictionProvider](/documentation/wirelessinsights/servicepredictionprovider)

### Creating a service prediction provider

- [init()](/documentation/wirelessinsights/servicepredictionprovider/init())

### Receiving service predictions

- [var servicePredictions: any AsyncSequence<[ServicePrediction], any Error>](/documentation/wirelessinsights/servicepredictionprovider/servicepredictions)
- [ServicePrediction](/documentation/wirelessinsights/serviceprediction)

#### Accessing prediction impact

- [let impact: ServicePrediction.Impact](/documentation/wirelessinsights/serviceprediction/impact-swift.property)
- [ServicePrediction.Impact](/documentation/wirelessinsights/serviceprediction/impact-swift.enum)

##### Working with impact values

- [case high](/documentation/wirelessinsights/serviceprediction/impact-swift.enum/high)
- [case medium](/documentation/wirelessinsights/serviceprediction/impact-swift.enum/medium)
- [case low](/documentation/wirelessinsights/serviceprediction/impact-swift.enum/low)

#### Accessing prediction timing

- [let predictedStartTime: Date](/documentation/wirelessinsights/serviceprediction/predictedstarttime)
- [let predictedInterval: TimeInterval](/documentation/wirelessinsights/serviceprediction/predictedinterval)
- [ServicePrediction.QuantizedInterval](/documentation/wirelessinsights/serviceprediction/quantizedinterval)

##### Working with interval values

- [static let long: Double](/documentation/wirelessinsights/serviceprediction/quantizedinterval/long)
- [static let medium: Double](/documentation/wirelessinsights/serviceprediction/quantizedinterval/medium)
- [static let short: Double](/documentation/wirelessinsights/serviceprediction/quantizedinterval/short)
- [static let minimal: Double](/documentation/wirelessinsights/serviceprediction/quantizedinterval/minimal)

#### Accessing prediction confidence

- [let confidenceScore: ServicePrediction.ConfidenceScore](/documentation/wirelessinsights/serviceprediction/confidencescore-swift.property)
- [ServicePrediction.ConfidenceScore](/documentation/wirelessinsights/serviceprediction/confidencescore-swift.struct)

##### Accessing prediction confidence scores

- [let prediction: ServicePrediction.Confidence](/documentation/wirelessinsights/serviceprediction/confidencescore-swift.struct/prediction)
- [let startTime: ServicePrediction.Confidence](/documentation/wirelessinsights/serviceprediction/confidencescore-swift.struct/starttime)
- [let duration: ServicePrediction.Confidence](/documentation/wirelessinsights/serviceprediction/confidencescore-swift.struct/duration)
- [ServicePrediction.Confidence](/documentation/wirelessinsights/serviceprediction/confidence)

###### Working with confidence values

- [case high](/documentation/wirelessinsights/serviceprediction/confidence/high)
- [case medium](/documentation/wirelessinsights/serviceprediction/confidence/medium)
- [case low](/documentation/wirelessinsights/serviceprediction/confidence/low)
- [ServicePrediction.Confidence](/documentation/wirelessinsights/serviceprediction/confidence)

##### Working with confidence values

- [case high](/documentation/wirelessinsights/serviceprediction/confidence/high)
- [case medium](/documentation/wirelessinsights/serviceprediction/confidence/medium)
- [case low](/documentation/wirelessinsights/serviceprediction/confidence/low)
- [ServicePredictionError](/documentation/wirelessinsights/servicepredictionerror)

#### Handling configuration errors

- [case unsupportedDevice](/documentation/wirelessinsights/servicepredictionerror/unsupporteddevice)

#### Handling connectivity errors

- [case connectionError](/documentation/wirelessinsights/servicepredictionerror/connectionerror)
- [Wireless Insights Service Predictions](/documentation/bundleresources/entitlements/com.apple.developer.wireless-insights.service-predictions)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
