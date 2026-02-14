# Declared Age Range Documentation

Source: https://sosumi.ai/documentation/declaredagerange

---
title: Declared Age Range
source: https://developer.apple.com/documentation/declaredagerange
timestamp: 2026-02-13T18:56:06.896Z
---

## Essentials

- [com.apple.developer.declared-age-range](/documentation/bundleresources/entitlements/com.apple.developer.declared-age-range)

## Age range requests

- [AgeRangeService](/documentation/declaredagerange/agerangeservice)

### Retrieving the shared instance

- [static let shared: AgeRangeService](/documentation/declaredagerange/agerangeservice/shared)

### Getting the age range

- [AgeRangeService.AgeRangeDeclaration](/documentation/declaredagerange/agerangeservice/agerangedeclaration)

#### Determining the age set method

- [case selfDeclared](/documentation/declaredagerange/agerangeservice/agerangedeclaration/selfdeclared)
- [case paymentChecked](/documentation/declaredagerange/agerangeservice/agerangedeclaration/paymentchecked)
- [case governmentIDChecked](/documentation/declaredagerange/agerangeservice/agerangedeclaration/governmentidchecked)
- [case checkedByOtherMethod](/documentation/declaredagerange/agerangeservice/agerangedeclaration/checkedbyothermethod)
- [case guardianDeclared](/documentation/declaredagerange/agerangeservice/agerangedeclaration/guardiandeclared)
- [case guardianPaymentChecked](/documentation/declaredagerange/agerangeservice/agerangedeclaration/guardianpaymentchecked)
- [case guardianGovernmentIDChecked](/documentation/declaredagerange/agerangeservice/agerangedeclaration/guardiangovernmentidchecked)
- [case guardianCheckedByOtherMethod](/documentation/declaredagerange/agerangeservice/agerangedeclaration/guardiancheckedbyothermethod)
- [AgeRangeService.AgeRange](/documentation/declaredagerange/agerangeservice/agerange)

#### Fetching the age range

- [var lowerBound: Int?](/documentation/declaredagerange/agerangeservice/agerange/lowerbound)
- [var upperBound: Int?](/documentation/declaredagerange/agerangeservice/agerange/upperbound)
- [var ageRangeDeclaration: AgeRangeService.AgeRangeDeclaration?](/documentation/declaredagerange/agerangeservice/agerange/agerangedeclaration)
- [var activeParentalControls: AgeRangeService.ParentalControls](/documentation/declaredagerange/agerangeservice/agerange/activeparentalcontrols)
- [func requestAgeRange(ageGates: Int, Int?, Int?, in: UIViewController) async throws -> AgeRangeService.Response](/documentation/declaredagerange/agerangeservice/requestagerange(agegates:_:_:in:)-2go8c)
- [func requestAgeRange(ageGates: Int, Int?, Int?, in: NSWindow) async throws -> AgeRangeService.Response](/documentation/declaredagerange/agerangeservice/requestagerange(agegates:_:_:in:)-4yo3r)
- [AgeRangeService.Response](/documentation/declaredagerange/agerangeservice/response)

#### Getting the age range response

- [case declinedSharing](/documentation/declaredagerange/agerangeservice/response/declinedsharing)
- [case sharing(range: AgeRangeService.AgeRange)](/documentation/declaredagerange/agerangeservice/response/sharing(range:))
- [AgeRangeService.ParentalControls](/documentation/declaredagerange/agerangeservice/parentalcontrols)

#### Creating a value

- [init(rawValue: Int)](/documentation/declaredagerange/agerangeservice/parentalcontrols/init(rawvalue:))

#### Accessing the raw value

- [var description: String](/documentation/declaredagerange/agerangeservice/parentalcontrols/description)
- [let rawValue: Int](/documentation/declaredagerange/agerangeservice/parentalcontrols/rawvalue)

#### Defining parental control options

- [static let communicationLimits: AgeRangeService.ParentalControls](/documentation/declaredagerange/agerangeservice/parentalcontrols/communicationlimits)
- [static let significantAppChangeApprovalRequired: AgeRangeService.ParentalControls](/documentation/declaredagerange/agerangeservice/parentalcontrols/significantappchangeapprovalrequired)

### Handling errors

- [AgeRangeService.Error](/documentation/declaredagerange/agerangeservice/error)

#### Interpreting error responses

- [case notAvailable](/documentation/declaredagerange/agerangeservice/error/notavailable)
- [case invalidRequest](/documentation/declaredagerange/agerangeservice/error/invalidrequest)

### Instance Properties

- [var isEligibleForAgeFeatures: Bool](/documentation/declaredagerange/agerangeservice/iseligibleforagefeatures)
- [DeclaredAgeRangeAction](/documentation/declaredagerange/declaredagerangeaction)

### Requesting the age range

- [func callAsFunction(ageGates: Int, Int?, Int?) async throws -> AgeRangeService.Response](/documentation/declaredagerange/declaredagerangeaction/callasfunction(agegates:_:_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
