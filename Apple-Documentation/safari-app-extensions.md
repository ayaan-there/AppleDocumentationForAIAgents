---
title: Safari app extensions
description: Learn how Safari app extensions extend the web-browsing experience in Safari by leveraging web technologies and native code.
source: https://developer.apple.com/documentation/SafariServices/safari-app-extensions
timestamp: 2026-02-13T20:01:22.811Z
---

**Navigation:** [SafariServices](/documentation/SafariServices)

**API Collection**

# Safari app extensions

> Learn how Safari app extensions extend the web-browsing experience in Safari by leveraging web technologies and native code.

## Overview

A Safari app extension can add new functionality to Safari by reading and modifying webpage content. These capabilities enhance the tools you use, the tasks you can accomplish, and the data you can access in your browser. A Safari app extension is uniquely useful because it can communicate with a native app. Sharing data between an app and Safari lets you integrate app content into Safari or send web data back to the app, enabling a unified experience for a web version and a native version of an app.

> [!NOTE]
> Previously, Safari extensions provided the communication between apps and Safari. To migrate a legacy Safari extension, see [converting-a-legacy-safari-extension-to-a-safari-app](/documentation/safariservices/converting-a-legacy-safari-extension-to-a-safari-app-extension).

Safari app extensions use a combination of JavaScript, CSS, and native code written in Objective-C or Swift. Because you build Safari app extensions on the standard app extension model, you get many native app benefits:

- You bundle Safari app extensions inside your app and distribute them through the App Store. You can distribute a Safari app extension with a Mac app or a [mac](/documentation/UIKit/mac-catalyst) app.
- Because you distribute your app and your Safari app extension together, you minimize the chances of installing mismatched versions.
- Your Safari app extension can securely communicate with your app using shared resources.

To become familiar with app extension concepts, see [](https://developer.apple.com/app-extensions/). If you're interested in deploying an extension you build for Chrome, Firefox, or Edge in Safari, or creating an extension that works in Safari and other browsers, see [safari-web](/documentation/safariservices/safari-web-extensions).

## Essentials

- [Building a Safari app extension](/documentation/safariservices/building-a-safari-app-extension) Add, build, and enable a Safari app extension.
- [Converting a legacy Safari extension to a Safari app extension](/documentation/safariservices/converting-a-legacy-safari-extension-to-a-safari-app-extension) Convert a legacy Safari extension to a Safari app extension, automatically with keys or manually.
- [Troubleshooting your Safari app extension](/documentation/safariservices/troubleshooting-your-safari-app-extension) Debug your Safari app extension with these techniques.

## Injected style sheets and scripts

- [Using injected style sheets and scripts](/documentation/safariservices/using-injected-style-sheets-and-scripts) Learn how you can affect the appearance or behavior of a webpage by using injected style sheets and scripts.
- [Injecting a script into a webpage](/documentation/safariservices/injecting-a-script-into-a-webpage) Inject a script that you write for a Safari app extension into a webpage.
- [Injecting CSS style sheets into a webpage](/documentation/safariservices/injecting-css-style-sheets-into-a-webpage) Add to or override styles by injecting CSS style sheets into webpages.
- [Passing messages between Safari app extensions and injected scripts](/documentation/safariservices/passing-messages-between-safari-app-extensions-and-injected-scripts) Communicate between your Safari app extension and injected scripts.
- [SFSafariExtensionHandler](/documentation/safariservices/sfsafariextensionhandler) A base class that you subclass to handle events in your Safari app extension.
- [SFSafariExtensionManager](/documentation/safariservices/sfsafariextensionmanager) A class that your app uses to find out the current state of a Safari extension.
- [SFSafariExtensionState](/documentation/safariservices/sfsafariextensionstate) The state of a Safari extension.
- [SFSafariPageProperties](/documentation/safariservices/sfsafaripageproperties) An object that captures information about a webpage.
- [SFSafariExtensionHandling](/documentation/safariservices/sfsafariextensionhandling) A protocol for implementing event handling in a Safari app extension.
- [SFExtensionProfileKey](/documentation/safariservices/sfextensionprofilekey) A string the system uses as a key in a user info dictionary to identify a profile identifier.

## Information property list keys

- [Safari app extension information property list keys](/documentation/safariservices/safari-app-extension-information-property-list-keys) Specify keys in your information property list file that provide information about your Safari app extension, UI, and permissions to the operating system.

## Related Documentation

- [Safari Extensions JS](/documentation/safariextensions)
- [Safari web extensions](/documentation/safariservices/safari-web-extensions)

## Safari app extensions

- [SFSafariExtension](/documentation/safariservices/sfsafariextension)
- [SFSafariApplication](/documentation/safariservices/sfsafariapplication)
- [SFSafariWindow](/documentation/safariservices/sfsafariwindow)
- [SFSafariPage](/documentation/safariservices/sfsafaripage)
- [SFSafariTab](/documentation/safariservices/sfsafaritab)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*