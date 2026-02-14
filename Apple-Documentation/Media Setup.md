# Media Setup Documentation

Source: https://sosumi.ai/documentation/mediasetup

---
title: Media Setup
source: https://developer.apple.com/documentation/mediasetup
timestamp: 2026-02-13T18:59:27.164Z
---

## HomePod Configuration

- [MSSetupSession](/documentation/mediasetup/mssetupsession)

### Preparing the Configuration View

- [init(serviceAccount: MSServiceAccount)](/documentation/mediasetup/mssetupsession/init(serviceaccount:))
- [var account: MSServiceAccount](/documentation/mediasetup/mssetupsession/account)

### Presenting the Configuration View

- [var presentationContext: (any MSAuthenticationPresentationContext)?](/documentation/mediasetup/mssetupsession/presentationcontext)
- [MSAuthenticationPresentationContext](/documentation/mediasetup/msauthenticationpresentationcontext)

#### Displaying the Media Setup View

- [func presentationAnchor() -> MSPresentationAnchor?](/documentation/mediasetup/msauthenticationpresentationcontext/presentationanchor())
- [MSPresentationAnchor](/documentation/mediasetup/mspresentationanchor)
- [func start() throws](/documentation/mediasetup/mssetupsession/start())
- [MSServiceAccount](/documentation/mediasetup/msserviceaccount)

### Presenting Account Information to the User

- [init(serviceName: String, accountName: String)](/documentation/mediasetup/msserviceaccount/init(servicename:accountname:))
- [var serviceName: String](/documentation/mediasetup/msserviceaccount/servicename)
- [var accountName: String](/documentation/mediasetup/msserviceaccount/accountname)

### Providing Parameters for an OAuth Request

- [var authorizationTokenURL: URL?](/documentation/mediasetup/msserviceaccount/authorizationtokenurl)
- [var authorizationScope: String?](/documentation/mediasetup/msserviceaccount/authorizationscope)
- [var clientID: String?](/documentation/mediasetup/msserviceaccount/clientid)
- [var clientSecret: String?](/documentation/mediasetup/msserviceaccount/clientsecret)
- [var configurationURL: URL?](/documentation/mediasetup/msserviceaccount/configurationurl)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
