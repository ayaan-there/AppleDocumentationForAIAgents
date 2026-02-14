# Family Controls Documentation

Source: https://sosumi.ai/documentation/familycontrols

---
title: Family Controls
source: https://developer.apple.com/documentation/familycontrols
timestamp: 2026-02-13T18:56:56.069Z
---

## Authorizations

- [AuthorizationCenter](/documentation/familycontrols/authorizationcenter)

### Accessing the shared center

- [static let shared: AuthorizationCenter](/documentation/familycontrols/authorizationcenter/shared)

### Requesting and revoking authorization

- [func requestAuthorization(for: FamilyControlsMember) async throws](/documentation/familycontrols/authorizationcenter/requestauthorization(for:))
- [func revokeAuthorization(completionHandler: (Result<Void, any Error>) -> Void)](/documentation/familycontrols/authorizationcenter/revokeauthorization(completionhandler:))

### Tracking authorization changes

- [var authorizationStatus: AuthorizationStatus](/documentation/familycontrols/authorizationcenter/authorizationstatus)
- [var $authorizationStatus: Published<AuthorizationStatus>.Publisher](/documentation/familycontrols/authorizationcenter/$authorizationstatus)

### Deprecated APIs

- [func requestAuthorization(completionHandler: (Result<Void, any Error>) -> Void)](/documentation/familycontrols/authorizationcenter/requestauthorization(completionhandler:))
- [AuthorizationStatus](/documentation/familycontrols/authorizationstatus)

### Determining the status

- [case notDetermined](/documentation/familycontrols/authorizationstatus/notdetermined)
- [case denied](/documentation/familycontrols/authorizationstatus/denied)
- [case approved](/documentation/familycontrols/authorizationstatus/approved)

### Debugging

- [var description: String](/documentation/familycontrols/authorizationstatus/description)
- [Family Controls](/documentation/bundleresources/entitlements/com.apple.developer.family-controls)
- [Requesting the Family Controls entitlement](/documentation/familycontrols/requesting-the-family-controls-entitlement)

## Account types

- [FamilyControlsMember](/documentation/familycontrols/familycontrolsmember)

### Enumeration Cases

- [case child](/documentation/familycontrols/familycontrolsmember/child)
- [case individual](/documentation/familycontrols/familycontrolsmember/individual)

### Instance Properties

- [var description: String](/documentation/familycontrols/familycontrolsmember/description)

## Activity selections

- [FamilyActivityPicker](/documentation/familycontrols/familyactivitypicker)

### Creating activity pickers

- [init(selection: Binding<FamilyActivitySelection>)](/documentation/familycontrols/familyactivitypicker/init(selection:))

### Accessing the content

- [var body: some View](/documentation/familycontrols/familyactivitypicker/body)

### Adding view modifiers

- [View Modifiers](/documentation/familycontrols/familyactivitypicker-view-modifiers)

### Initializers

- [init(headerText: String?, footerText: String?, selection: Binding<FamilyActivitySelection>)](/documentation/familycontrols/familyactivitypicker/init(headertext:footertext:selection:))
- [FamilyActivitySelection](/documentation/familycontrols/familyactivityselection)

### Accessing selected categories

- [var categories: Set<ActivityCategory>](/documentation/familycontrols/familyactivityselection/categories)
- [var categoryTokens: Set<ActivityCategoryToken>](/documentation/familycontrols/familyactivityselection/categorytokens)
- [init(includeEntireCategory: Bool)](/documentation/familycontrols/familyactivityselection/init(includeentirecategory:))

### Accessing selected applications

- [var applications: Set<Application>](/documentation/familycontrols/familyactivityselection/applications)
- [var applicationTokens: Set<ApplicationToken>](/documentation/familycontrols/familyactivityselection/applicationtokens)

### Accessing selected web domains

- [var webDomains: Set<WebDomain>](/documentation/familycontrols/familyactivityselection/webdomains)
- [var webDomainTokens: Set<WebDomainToken>](/documentation/familycontrols/familyactivityselection/webdomaintokens)

### Creating activity selections

- [init()](/documentation/familycontrols/familyactivityselection/init())

### Comparing activity selections

- [let includeEntireCategory: Bool](/documentation/familycontrols/familyactivityselection/includeentirecategory)

## Activity labels

- [Displaying Activity Labels](/documentation/familycontrols/displayingactivitylabels)

### Label constraints

- [FamilyActivityTitleView](/documentation/familycontrols/familyactivitytitleview)
- [FamilyActivityIconView](/documentation/familycontrols/familyactivityiconview)

## Errors

- [FamilyControlsError](/documentation/familycontrols/familycontrolserror)

### Error values

- [case invalidAccountType](/documentation/familycontrols/familycontrolserror/invalidaccounttype)
- [case authorizationConflict](/documentation/familycontrols/familycontrolserror/authorizationconflict)
- [case authorizationCanceled](/documentation/familycontrols/familycontrolserror/authorizationcanceled)
- [case invalidArgument](/documentation/familycontrols/familycontrolserror/invalidargument)
- [case unavailable](/documentation/familycontrols/familycontrolserror/unavailable)
- [case restricted](/documentation/familycontrols/familycontrolserror/restricted)
- [case networkError](/documentation/familycontrols/familycontrolserror/networkerror)
- [case authenticationMethodUnavailable](/documentation/familycontrols/familycontrolserror/authenticationmethodunavailable)

### Error data

- [var errorDescription: String?](/documentation/familycontrols/familycontrolserror/errordescription)
- [var errorDescription: String?](/documentation/familycontrols/familycontrolserror/errordescription)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
