# AppClip Documentation

Source: https://sosumi.ai/documentation/appclip

---
title: App Clips
source: https://developer.apple.com/documentation/appclip
timestamp: 2026-02-13T19:58:16.012Z
---

## Essentials

- [Choosing the right functionality for your App Clip](/documentation/appclip/choosing-the-right-functionality-for-your-app-clip)
- [Configuring App Clip experiences](/documentation/appclip/configuring-the-launch-experience-of-your-app-clip)
- [App Clips updates](/documentation/updates/appclips)

## Creation

- [Creating an App Clip with Xcode](/documentation/appclip/creating-an-app-clip-with-xcode)
- [Fruta: Building a feature-rich app with SwiftUI](/documentation/appclip/fruta-building-a-feature-rich-app-with-swiftui)
- [Parent Application Identifiers Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.parent-application-identifiers)
- [com.apple.developer.associated-appclip-app-identifiers](/documentation/bundleresources/entitlements/com.apple.developer.associated-appclip-app-identifiers)
- [com.apple.developer.on-demand-install-capable](/documentation/bundleresources/entitlements/com.apple.developer.on-demand-install-capable)

## Launch

- [Responding to invocations](/documentation/appclip/responding-to-invocations)
- [Associating your App Clip with your website](/documentation/appclip/associating-your-app-clip-with-your-website)
- [Supporting invocations from your website and the Messages app](/documentation/appclip/supporting-invocations-from-your-website-and-the-messages-app)
- [Confirming a person’s physical location](/documentation/appclip/confirming-a-person-s-physical-location)
- [Launching another app’s App Clip from your app](/documentation/appclip/launching-another-app-s-app-clip-from-your-app)
- [APActivationPayload](/documentation/appclip/apactivationpayload)

### Passing data to the App Clip

- [var url: URL?](/documentation/appclip/apactivationpayload/url)

### Confirming a person’s physical location

- [func confirmAcquired(in: CLRegion, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/appclip/apactivationpayload/confirmacquired(in:completionhandler:))

### Understanding errors

- [let APActivationPayloadErrorDomain: String](/documentation/appclip/apactivationpayloaderrordomain)
- [APActivationPayloadError](/documentation/appclip/apactivationpayloaderror)

#### Getting information about the error

- [static var errorDomain: String](/documentation/appclip/apactivationpayloaderror/errordomain)

#### Interpreting errors

- [static var doesNotMatch: APActivationPayloadError.Code](/documentation/appclip/apactivationpayloaderror/doesnotmatch)
- [static var disallowed: APActivationPayloadError.Code](/documentation/appclip/apactivationpayloaderror/disallowed)
- [APActivationPayloadError.Code](/documentation/appclip/apactivationpayloaderror/code)

##### Error types

- [case doesNotMatch](/documentation/appclip/apactivationpayloaderror/code/doesnotmatch)
- [case disallowed](/documentation/appclip/apactivationpayloaderror/code/disallowed)

##### Initializers

- [init?(rawValue: Int)](/documentation/appclip/apactivationpayloaderror/code/init(rawvalue:))
- [APActivationPayloadError.Code](/documentation/appclip/apactivationpayloaderror/code)

#### Error types

- [case doesNotMatch](/documentation/appclip/apactivationpayloaderror/code/doesnotmatch)
- [case disallowed](/documentation/appclip/apactivationpayloaderror/code/disallowed)

#### Initializers

- [init?(rawValue: Int)](/documentation/appclip/apactivationpayloaderror/code/init(rawvalue:))
- [NSAppClip](/documentation/bundleresources/information-property-list/nsappclip)

## App Clip Codes

- [Creating App Clip Codes](/documentation/appclip/creating-app-clip-codes)

### App Clip Code creation

- [Creating App Clip Codes with App Store Connect](/documentation/appclip/creating-app-clip-codes-with-app-store-connect)
- [Creating App Clip Codes with the App Clip Code Generator](/documentation/appclip/creating-app-clip-codes-with-the-app-clip-code-generator)
- [Encoding a URL in an App Clip Code](/documentation/appclip/encoding-a-url-in-an-app-clip-code)
- [Preparing multiple App Clip Codes for production](/documentation/appclip/preparing-multiple-app-clip-codes-for-production)
- [Interacting with App Clip Codes in AR](/documentation/appclip/interacting-with-app-clip-codes-in-ar)

## App Clip to full app transition

- [Recommending your app to App Clip users](/documentation/appclip/recommending-your-app-to-app-clip-users)
- [Sharing data between your App Clip and your full app](/documentation/appclip/sharing-data-between-your-app-clip-and-your-full-app)

## Notifications

- [Enabling notifications in App Clips](/documentation/appclip/enabling-notifications-in-app-clips)

## Live Activities

- [Offering Live Activities with your App Clip](/documentation/appclip/offering-live-activities-with-your-app-clip)

## Testing

- [Testing the launch experience of your App Clip](/documentation/appclip/testing-the-launch-experience-of-your-app-clip)

## Distribution

- [Distributing your App Clip](/documentation/appclip/distributing-your-app-clip)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
