# User Notifications UI Documentation

Source: https://sosumi.ai/documentation/usernotificationsui

---
title: User Notifications UI
source: https://developer.apple.com/documentation/usernotificationsui
timestamp: 2026-02-13T19:03:34.878Z
---

## Notification Content App Extension

- [Customizing the Appearance of Notifications](/documentation/usernotificationsui/customizing-the-appearance-of-notifications)
- [UNNotificationContentExtension](/documentation/usernotificationsui/unnotificationcontentextension)

### Processing Notifications

- [func didReceive(UNNotification)](/documentation/usernotificationsui/unnotificationcontentextension/didreceive(_:))

### Handling Custom Actions

- [func didReceive(UNNotificationResponse, completionHandler: (UNNotificationContentExtensionResponseOption) -> Void)](/documentation/usernotificationsui/unnotificationcontentextension/didreceive(_:completionhandler:))
- [UNNotificationContentExtensionResponseOption](/documentation/usernotificationsui/unnotificationcontentextensionresponseoption)

#### Response Options

- [case doNotDismiss](/documentation/usernotificationsui/unnotificationcontentextensionresponseoption/donotdismiss)
- [case dismiss](/documentation/usernotificationsui/unnotificationcontentextensionresponseoption/dismiss)
- [case dismissAndForwardAction](/documentation/usernotificationsui/unnotificationcontentextensionresponseoption/dismissandforwardaction)

#### Initializers

- [init?(rawValue: UInt)](/documentation/usernotificationsui/unnotificationcontentextensionresponseoption/init(rawvalue:))

### Supporting Media Playback

- [var mediaPlayPauseButtonType: UNNotificationContentExtensionMediaPlayPauseButtonType](/documentation/usernotificationsui/unnotificationcontentextension/mediaplaypausebuttontype)
- [UNNotificationContentExtensionMediaPlayPauseButtonType](/documentation/usernotificationsui/unnotificationcontentextensionmediaplaypausebuttontype)

#### Button Types

- [case none](/documentation/usernotificationsui/unnotificationcontentextensionmediaplaypausebuttontype/none)
- [case `default`](/documentation/usernotificationsui/unnotificationcontentextensionmediaplaypausebuttontype/default)
- [case overlay](/documentation/usernotificationsui/unnotificationcontentextensionmediaplaypausebuttontype/overlay)

#### Initializers

- [init?(rawValue: UInt)](/documentation/usernotificationsui/unnotificationcontentextensionmediaplaypausebuttontype/init(rawvalue:))
- [var mediaPlayPauseButtonFrame: CGRect](/documentation/usernotificationsui/unnotificationcontentextension/mediaplaypausebuttonframe)
- [var mediaPlayPauseButtonTintColor: UIColor](/documentation/usernotificationsui/unnotificationcontentextension/mediaplaypausebuttontintcolor)
- [func mediaPlay()](/documentation/usernotificationsui/unnotificationcontentextension/mediaplay())
- [func mediaPause()](/documentation/usernotificationsui/unnotificationcontentextension/mediapause())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
