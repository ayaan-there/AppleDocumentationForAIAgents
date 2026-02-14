# Safari Services Documentation

Source: https://sosumi.ai/documentation/safariservices

---
title: Safari Services
source: https://developer.apple.com/documentation/safariservices
timestamp: 2026-02-13T19:01:30.871Z
---

## Safari web extensions

- [Safari web extensions](/documentation/safariservices/safari-web-extensions)

### New extensions

- [Creating a Safari web extension](/documentation/safariservices/creating-a-safari-web-extension)
- [Modernizing Safari Web Extensions](/documentation/safariservices/modernizing-safari-web-extensions)
- [Developing a Safari Web Extension](/documentation/safariservices/developing-a-safari-web-extension)

### Extension conversions and packaging

- [Packaging a web extension for Safari](/documentation/safariservices/packaging-a-web-extension-for-safari)
- [Packaging and distributing Safari Web Extensions with App Store Connect](/documentation/safariservices/packaging-and-distributing-safari-web-extensions-with-app-store-connect)
- [Converting a Safari app extension to a Safari web extension](/documentation/safariservices/converting-a-safari-app-extension-to-a-safari-web-extension)

### Extension updates

- [Updating a Safari web extension](/documentation/safariservices/updating-a-safari-web-extension)
- [Managing Safari web extension permissions](/documentation/safariservices/managing-safari-web-extension-permissions)
- [Previewing Metadata using Open Graph](/documentation/safariservices/previewing-metadata-using-open-graph)

### Checking extension state

- [SFSafariExtensionManager](/documentation/safariservices/sfsafariextensionmanager)

#### Checking on the state of an extension

- [class func getStateOfSafariExtension(withIdentifier: String, completionHandler: (SFSafariExtensionState?, (any Error)?) -> Void)](/documentation/safariservices/sfsafariextensionmanager/getstateofsafariextension(withidentifier:completionhandler:))
- [class func getStateOfExtension(withIdentifier: String, completionHandler: (SFSafariExtensionState?, (any Error)?) -> Void)](/documentation/safariservices/sfsafariextensionmanager/getstateofextension(withidentifier:completionhandler:))
- [SFSafariExtensionState](/documentation/safariservices/sfsafariextensionstate)

#### Instance Properties

- [var isEnabled: Bool](/documentation/safariservices/sfsafariextensionstate/isenabled)

### Messaging

- [Messaging between the app and JavaScript in a Safari web extension](/documentation/safariservices/messaging-between-the-app-and-javascript-in-a-safari-web-extension)
- [let SFExtensionMessageKey: String](/documentation/safariservices/sfextensionmessagekey)
- [let SFExtensionProfileKey: String](/documentation/safariservices/sfextensionprofilekey)
- [Messaging a Web Extension’s Native App](/documentation/safariservices/messaging-a-web-extension-s-native-app)
- [Messaging between a webpage and your Safari web extension](/documentation/safariservices/messaging-between-a-webpage-and-your-safari-web-extension)

### Blocking content

- [Blocking content with your Safari web extension](/documentation/safariservices/blocking-content-with-your-safari-web-extension)
- [Adopting Declarative Content Blocking in Safari Web Extensions](/documentation/safariservices/adopting-declarative-content-blocking-in-safari-web-extensions)

### Adding Web Inspector tools

- [Adding a web development tool to Safari Web Inspector](/documentation/safariservices/adding-a-web-development-tool-to-safari-web-inspector)
- [Creating Safari Web Inspector extensions](/documentation/safariservices/creating-safari-web-inspector-extensions)

### Extension improvements

- [Optimizing your web extension for Safari](/documentation/safariservices/optimizing-your-web-extension-for-safari)
- [Adopting New Safari Web Extension APIs](/documentation/safariservices/adopting-new-safari-web-extension-apis)
- [Syncing Safari web extensions across devices and platforms](/documentation/safariservices/syncing-safari-web-extensions-across-devices-and-platforms)
- [Assessing your Safari web extension’s browser compatibility](/documentation/safariservices/assessing-your-safari-web-extension-s-browser-compatibility)
- [Troubleshooting your Safari web extension](/documentation/safariservices/troubleshooting-your-safari-web-extension)

### Installation and distribution

- [Running your Safari web extension](/documentation/safariservices/running-your-safari-web-extension)
- [Distributing your Safari web extension](/documentation/safariservices/distributing-your-safari-web-extension)

## Content blockers

- [Creating a content blocker](/documentation/safariservices/creating-a-content-blocker)
- [SFContentBlockerManager](/documentation/safariservices/sfcontentblockermanager)

### Acting Based on the State of Your Content Blocker

- [class func getStateOfContentBlocker(withIdentifier: String, completionHandler: (SFContentBlockerState?, (any Error)?) -> Void)](/documentation/safariservices/sfcontentblockermanager/getstateofcontentblocker(withidentifier:completionhandler:))

### Reloading Your Content-Blocking Rules

- [class func reloadContentBlocker(withIdentifier: String, completionHandler: (((any Error)?) -> Void)?)](/documentation/safariservices/sfcontentblockermanager/reloadcontentblocker(withidentifier:completionhandler:))
- [SFContentBlockerState](/documentation/safariservices/sfcontentblockerstate)

### Identifying the Content Blocker’s State

- [var isEnabled: Bool](/documentation/safariservices/sfcontentblockerstate/isenabled)

## Safari app extensions

- [Safari app extensions](/documentation/safariservices/safari-app-extensions)

### Essentials

- [Building a Safari app extension](/documentation/safariservices/building-a-safari-app-extension)
- [Converting a legacy Safari extension to a Safari app extension](/documentation/safariservices/converting-a-legacy-safari-extension-to-a-safari-app-extension)
- [Troubleshooting your Safari app extension](/documentation/safariservices/troubleshooting-your-safari-app-extension)

### Injected style sheets and scripts

- [Using injected style sheets and scripts](/documentation/safariservices/using-injected-style-sheets-and-scripts)
- [Injecting a script into a webpage](/documentation/safariservices/injecting-a-script-into-a-webpage)
- [Injecting CSS style sheets into a webpage](/documentation/safariservices/injecting-css-style-sheets-into-a-webpage)
- [Passing messages between Safari app extensions and injected scripts](/documentation/safariservices/passing-messages-between-safari-app-extensions-and-injected-scripts)
- [SFSafariExtensionHandler](/documentation/safariservices/sfsafariextensionhandler)
- [SFSafariExtensionManager](/documentation/safariservices/sfsafariextensionmanager)

#### Checking on the state of an extension

- [class func getStateOfSafariExtension(withIdentifier: String, completionHandler: (SFSafariExtensionState?, (any Error)?) -> Void)](/documentation/safariservices/sfsafariextensionmanager/getstateofsafariextension(withidentifier:completionhandler:))
- [class func getStateOfExtension(withIdentifier: String, completionHandler: (SFSafariExtensionState?, (any Error)?) -> Void)](/documentation/safariservices/sfsafariextensionmanager/getstateofextension(withidentifier:completionhandler:))
- [SFSafariExtensionState](/documentation/safariservices/sfsafariextensionstate)

#### Instance Properties

- [var isEnabled: Bool](/documentation/safariservices/sfsafariextensionstate/isenabled)
- [SFSafariPageProperties](/documentation/safariservices/sfsafaripageproperties)

#### Getting the Safari Page Properties

- [var isActive: Bool](/documentation/safariservices/sfsafaripageproperties/isactive)
- [var title: String?](/documentation/safariservices/sfsafaripageproperties/title)
- [var url: URL?](/documentation/safariservices/sfsafaripageproperties/url)
- [var usesPrivateBrowsing: Bool](/documentation/safariservices/sfsafaripageproperties/usesprivatebrowsing)
- [SFSafariExtensionHandling](/documentation/safariservices/sfsafariextensionhandling)

#### Receiving Messages in Your App Extension

- [func messageReceived(withName: String, from: SFSafariPage, userInfo: [String : Any]?)](/documentation/safariservices/sfsafariextensionhandling/messagereceived(withname:from:userinfo:))
- [func messageReceivedFromContainingApp(withName: String, userInfo: [String : Any]?)](/documentation/safariservices/sfsafariextensionhandling/messagereceivedfromcontainingapp(withname:userinfo:))

#### Responding to Context Menu Selections

- [func contextMenuItemSelected(withCommand: String, in: SFSafariPage, userInfo: [String : Any]?)](/documentation/safariservices/sfsafariextensionhandling/contextmenuitemselected(withcommand:in:userinfo:))
- [func validateContextMenuItem(withCommand: String, in: SFSafariPage, userInfo: [String : Any]?, validationHandler: (Bool, String?) -> Void)](/documentation/safariservices/sfsafariextensionhandling/validatecontextmenuitem(withcommand:in:userinfo:validationhandler:))

#### Working with Toolbar Items

- [func toolbarItemClicked(in: SFSafariWindow)](/documentation/safariservices/sfsafariextensionhandling/toolbaritemclicked(in:))
- [func validateToolbarItem(in: SFSafariWindow, validationHandler: (Bool, String) -> Void)](/documentation/safariservices/sfsafariextensionhandling/validatetoolbaritem(in:validationhandler:))

#### Working with Popovers

- [func popoverViewController() -> SFSafariExtensionViewController](/documentation/safariservices/sfsafariextensionhandling/popoverviewcontroller())
- [func popoverWillShow(in: SFSafariWindow)](/documentation/safariservices/sfsafariextensionhandling/popoverwillshow(in:))
- [func popoverDidClose(in: SFSafariWindow)](/documentation/safariservices/sfsafariextensionhandling/popoverdidclose(in:))

#### Working with Content Blockers

- [func contentBlocker(withIdentifier: String, blockedResourcesWith: [URL], on: SFSafariPage)](/documentation/safariservices/sfsafariextensionhandling/contentblocker(withidentifier:blockedresourceswith:on:))

#### Responding to Page Navigation

- [func page(SFSafariPage, willNavigateTo: URL?)](/documentation/safariservices/sfsafariextensionhandling/page(_:willnavigateto:))

#### Instance Methods

- [func additionalRequestHeaders(for: URL, completionHandler: ([String : String]?) -> Void)](/documentation/safariservices/sfsafariextensionhandling/additionalrequestheaders(for:completionhandler:))
- [let SFExtensionProfileKey: String](/documentation/safariservices/sfextensionprofilekey)

### Information property list keys

- [Safari app extension information property list keys](/documentation/safariservices/safari-app-extension-information-property-list-keys)

#### First steps

- [Using Safari app extension default keys](/documentation/safariservices/using-safari-app-extension-default-keys)

#### Access and permissions

- [Setting Safari app extension feature keys](/documentation/safariservices/setting-safari-app-extension-feature-keys)
- [Adjusting website access permissions](/documentation/safariservices/adjusting-website-access-permissions)
- [Using permissions for scripts and style sheets](/documentation/safariservices/using-permissions-for-scripts-and-style-sheets)

#### Conditional scripts and style sheet injection

- [Using content script and style sheet keys](/documentation/safariservices/using-content-script-and-style-sheet-keys)

#### Contextual menu and toolbar items

- [Using contextual menu and toolbar item keys](/documentation/safariservices/using-contextual-menu-and-toolbar-item-keys)
- [Adjusting settings for a toolbar item](/documentation/safariservices/adjusting-settings-for-a-toolbar-item)
- [Adjusting settings for contextual menu items](/documentation/safariservices/adjusting-settings-for-contextual-menu-items)
- [SFSafariToolbarItem](/documentation/safariservices/sfsafaritoolbaritem)

##### Controlling Toolbar Items

- [func setEnabled(Bool, withBadgeText: String?)](/documentation/safariservices/sfsafaritoolbaritem/setenabled(_:withbadgetext:))
- [func setBadgeText(String?)](/documentation/safariservices/sfsafaritoolbaritem/setbadgetext(_:))
- [func setEnabled(Bool)](/documentation/safariservices/sfsafaritoolbaritem/setenabled(_:))
- [func setImage(NSImage?)](/documentation/safariservices/sfsafaritoolbaritem/setimage(_:))
- [func setLabel(String?)](/documentation/safariservices/sfsafaritoolbaritem/setlabel(_:))

##### Instance Methods

- [func showPopover()](/documentation/safariservices/sfsafaritoolbaritem/showpopover())
- [SFSafariExtensionViewController](/documentation/safariservices/sfsafariextensionviewcontroller)

##### Instance Methods

- [func dismissPopover()](/documentation/safariservices/sfsafariextensionviewcontroller/dismisspopover())
- [SFSafariExtension](/documentation/safariservices/sfsafariextension)

### Type Methods

- [class func getBaseURI(completionHandler: (URL?) -> Void)](/documentation/safariservices/sfsafariextension/getbaseuri(completionhandler:))
- [SFSafariApplication](/documentation/safariservices/sfsafariapplication)

### Communicating With the App Extension

- [class func dispatchMessage(withName: String, toExtensionWithIdentifier: String, userInfo: [String : Any]?, completionHandler: (((any Error)?) -> Void)?)](/documentation/safariservices/sfsafariapplication/dispatchmessage(withname:toextensionwithidentifier:userinfo:completionhandler:))

### Working with Windows

- [class func getActiveWindow(completionHandler: (SFSafariWindow?) -> Void)](/documentation/safariservices/sfsafariapplication/getactivewindow(completionhandler:))
- [class func openWindow(with: URL, completionHandler: ((SFSafariWindow?) -> Void)?)](/documentation/safariservices/sfsafariapplication/openwindow(with:completionhandler:))
- [class func showPreferencesForExtension(withIdentifier: String, completionHandler: (((any Error)?) -> Void)?)](/documentation/safariservices/sfsafariapplication/showpreferencesforextension(withidentifier:completionhandler:))

### Updating Toolbar Items

- [class func setToolbarItemsNeedUpdate()](/documentation/safariservices/sfsafariapplication/settoolbaritemsneedupdate())

### Type Methods

- [class func getAllWindows(completionHandler: ([SFSafariWindow]) -> Void)](/documentation/safariservices/sfsafariapplication/getallwindows(completionhandler:))
- [class func getHostApplication(completionHandler: (NSRunningApplication) -> Void)](/documentation/safariservices/sfsafariapplication/gethostapplication(completionhandler:))
- [SFSafariWindow](/documentation/safariservices/sfsafariwindow)

### Working with Tabs

- [func getActiveTab(completionHandler: (SFSafariTab?) -> Void)](/documentation/safariservices/sfsafariwindow/getactivetab(completionhandler:))
- [func openTab(with: URL, makeActiveIfPossible: Bool, completionHandler: ((SFSafariTab?) -> Void)?)](/documentation/safariservices/sfsafariwindow/opentab(with:makeactiveifpossible:completionhandler:))

### Getting the Toolbar Item

- [func getToolbarItem(completionHandler: (SFSafariToolbarItem?) -> Void)](/documentation/safariservices/sfsafariwindow/gettoolbaritem(completionhandler:))

### Instance Methods

- [func close()](/documentation/safariservices/sfsafariwindow/close())
- [func getAllTabs(completionHandler: ([SFSafariTab]) -> Void)](/documentation/safariservices/sfsafariwindow/getalltabs(completionhandler:))
- [SFSafariPage](/documentation/safariservices/sfsafaripage)

### Messaging Injected Scripts

- [func dispatchMessageToScript(withName: String, userInfo: [String : Any]?)](/documentation/safariservices/sfsafaripage/dispatchmessagetoscript(withname:userinfo:))

### Getting Page Information

- [func getPropertiesWithCompletionHandler((SFSafariPageProperties?) -> Void)](/documentation/safariservices/sfsafaripage/getpropertieswithcompletionhandler(_:))

### Reloading the Page

- [func reload()](/documentation/safariservices/sfsafaripage/reload())

### Instance Methods

- [func getContainingTab(completionHandler: (SFSafariTab) -> Void)](/documentation/safariservices/sfsafaripage/getcontainingtab(completionhandler:))
- [func getScreenshotOfVisibleArea(completionHandler: (NSImage?) -> Void)](/documentation/safariservices/sfsafaripage/getscreenshotofvisiblearea(completionhandler:))
- [SFSafariTab](/documentation/safariservices/sfsafaritab)

### Accessing Pages

- [func getActivePage(completionHandler: (SFSafariPage?) -> Void)](/documentation/safariservices/sfsafaritab/getactivepage(completionhandler:))
- [func getPagesWithCompletionHandler(([SFSafariPage]?) -> Void)](/documentation/safariservices/sfsafaritab/getpageswithcompletionhandler(_:))

### Activating Tabs

- [func activate(completionHandler: (() -> Void)?)](/documentation/safariservices/sfsafaritab/activate(completionhandler:))

### Instance Methods

- [func close()](/documentation/safariservices/sfsafaritab/close())
- [func getContainingWindow(completionHandler: (SFSafariWindow?) -> Void)](/documentation/safariservices/sfsafaritab/getcontainingwindow(completionhandler:))
- [func navigate(to: URL)](/documentation/safariservices/sfsafaritab/navigate(to:))

## Safari Settings

- [SFSafariSettings](/documentation/safariservices/sfsafarisettings)

### Opening Settings for Safari extensions

- [class func openExtensionsSettings(forIdentifiers: [String], completionHandler: (((any Error)?) -> Void)?)](/documentation/safariservices/sfsafarisettings/openextensionssettings(foridentifiers:completionhandler:))

### Opening Settings to export browsing data

- [class func openExportBrowsingDataSettings(completionHandler: (((any Error)?) -> Void)?)](/documentation/safariservices/sfsafarisettings/openexportbrowsingdatasettings(completionhandler:))

## Safari content in your app

- [SFSafariViewController](/documentation/safariservices/sfsafariviewcontroller)

### Creating a View Controller

- [init(url: URL, configuration: SFSafariViewController.Configuration)](/documentation/safariservices/sfsafariviewcontroller/init(url:configuration:))
- [SFSafariViewController.Configuration](/documentation/safariservices/sfsafariviewcontroller/configuration-swift.class)

#### Configuring a Safari View Controller

- [var entersReaderIfAvailable: Bool](/documentation/safariservices/sfsafariviewcontroller/configuration-swift.class/entersreaderifavailable)
- [var barCollapsingEnabled: Bool](/documentation/safariservices/sfsafariviewcontroller/configuration-swift.class/barcollapsingenabled)
- [var eventAttribution: UIEventAttribution?](/documentation/safariservices/sfsafariviewcontroller/configuration-swift.class/eventattribution)

#### Instance Properties

- [var activityButton: SFSafariViewController.ActivityButton?](/documentation/safariservices/sfsafariviewcontroller/configuration-swift.class/activitybutton)
- [convenience init(url: URL)](/documentation/safariservices/sfsafariviewcontroller/init(url:))
- [init(url: URL, entersReaderIfAvailable: Bool)](/documentation/safariservices/sfsafariviewcontroller/init(url:entersreaderifavailable:))

### Responding to View Controller Interaction

- [var delegate: (any SFSafariViewControllerDelegate)?](/documentation/safariservices/sfsafariviewcontroller/delegate)
- [SFSafariViewControllerDelegate](/documentation/safariservices/sfsafariviewcontrollerdelegate)

#### Working with the View Controller

- [func safariViewController(SFSafariViewController, didCompleteInitialLoad: Bool)](/documentation/safariservices/sfsafariviewcontrollerdelegate/safariviewcontroller(_:didcompleteinitialload:))
- [func safariViewController(SFSafariViewController, activityItemsFor: URL, title: String?) -> [UIActivity]](/documentation/safariservices/sfsafariviewcontrollerdelegate/safariviewcontroller(_:activityitemsfor:title:))
- [func safariViewControllerDidFinish(SFSafariViewController)](/documentation/safariservices/sfsafariviewcontrollerdelegate/safariviewcontrollerdidfinish(_:))
- [func safariViewController(SFSafariViewController, excludedActivityTypesFor: URL, title: String?) -> [UIActivity.ActivityType]](/documentation/safariservices/sfsafariviewcontrollerdelegate/safariviewcontroller(_:excludedactivitytypesfor:title:))

#### Instance Methods

- [func safariViewController(SFSafariViewController, initialLoadDidRedirectTo: URL)](/documentation/safariservices/sfsafariviewcontrollerdelegate/safariviewcontroller(_:initialloaddidredirectto:))
- [func safariViewControllerWillOpenInBrowser(SFSafariViewController)](/documentation/safariservices/sfsafariviewcontrollerdelegate/safariviewcontrollerwillopeninbrowser(_:))

### Configuring the View Controller

- [var configuration: SFSafariViewController.Configuration](/documentation/safariservices/sfsafariviewcontroller/configuration-swift.property)
- [var dismissButtonStyle: SFSafariViewController.DismissButtonStyle](/documentation/safariservices/sfsafariviewcontroller/dismissbuttonstyle-swift.property)
- [SFSafariViewController.DismissButtonStyle](/documentation/safariservices/sfsafariviewcontroller/dismissbuttonstyle-swift.enum)

#### Enumeration Cases

- [case done](/documentation/safariservices/sfsafariviewcontroller/dismissbuttonstyle-swift.enum/done)
- [case close](/documentation/safariservices/sfsafariviewcontroller/dismissbuttonstyle-swift.enum/close)
- [case cancel](/documentation/safariservices/sfsafariviewcontroller/dismissbuttonstyle-swift.enum/cancel)

#### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/sfsafariviewcontroller/dismissbuttonstyle-swift.enum/init(rawvalue:))
- [var preferredBarTintColor: UIColor?](/documentation/safariservices/sfsafariviewcontroller/preferredbartintcolor)
- [var preferredControlTintColor: UIColor?](/documentation/safariservices/sfsafariviewcontroller/preferredcontroltintcolor)

### Type Methods

- [class func prewarmConnections(to: [URL]) -> SFSafariViewController.PrewarmingToken](/documentation/safariservices/sfsafariviewcontroller/prewarmconnections(to:))

### Classes

- [SFSafariViewController.ActivityButton](/documentation/safariservices/sfsafariviewcontroller/activitybutton)

#### Initializers

- [init(templateImage: UIImage, extensionIdentifier: String)](/documentation/safariservices/sfsafariviewcontroller/activitybutton/init(templateimage:extensionidentifier:))

#### Instance Properties

- [var extensionIdentifier: String?](/documentation/safariservices/sfsafariviewcontroller/activitybutton/extensionidentifier)
- [var templateImage: UIImage?](/documentation/safariservices/sfsafariviewcontroller/activitybutton/templateimage)
- [SFSafariViewController.DataStore](/documentation/safariservices/sfsafariviewcontroller/datastore)

#### Type Properties

- [class var `default`: SFSafariViewController.DataStore](/documentation/safariservices/sfsafariviewcontroller/datastore/default)

#### Instance Methods

- [func clearWebsiteData(completionHandler: (() -> Void)?)](/documentation/safariservices/sfsafariviewcontroller/datastore/clearwebsitedata(completionhandler:))
- [SFSafariViewController.PrewarmingToken](/documentation/safariservices/sfsafariviewcontroller/prewarmingtoken)

#### Instance Methods

- [func invalidate()](/documentation/safariservices/sfsafariviewcontroller/prewarmingtoken/invalidate())
- [SFAuthenticationSession.CompletionHandler](/documentation/safariservices/sfauthenticationsession/completionhandler)
- [Importing data exported from Safari](/documentation/safariservices/importing-data-exported-from-safari)

## Associated domains

- [Supporting associated domains](/documentation/xcode/supporting-associated-domains)
- [SFUniversalLink](/documentation/safariservices/sfuniversallink)

### Initializing a Link

- [init?(webpageURL: URL)](/documentation/safariservices/sfuniversallink/init(webpageurl:))

### Configuring Universal Links

- [var applicationURL: URL](/documentation/safariservices/sfuniversallink/applicationurl)
- [var isEnabled: Bool](/documentation/safariservices/sfuniversallink/isenabled)
- [var webpageURL: URL](/documentation/safariservices/sfuniversallink/webpageurl)
- [Associated Domains Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.associated-domains)

## Availability

- [func SFSafariServicesAvailable(SFSafariServicesVersion) -> Bool](/documentation/safariservices/sfsafariservicesavailable(_:))
- [SFSafariServicesVersion](/documentation/safariservices/sfsafariservicesversion)

### Enumeration Cases

- [case version10_0](/documentation/safariservices/sfsafariservicesversion/version10_0)
- [case version10_1](/documentation/safariservices/sfsafariservicesversion/version10_1)
- [case version11_0](/documentation/safariservices/sfsafariservicesversion/version11_0)
- [case version12_0](/documentation/safariservices/sfsafariservicesversion/version12_0)
- [case version12_1](/documentation/safariservices/sfsafariservicesversion/version12_1)
- [case version13_0](/documentation/safariservices/sfsafariservicesversion/version13_0)

### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/sfsafariservicesversion/init(rawvalue:))

## Safari Reading List

- [SSReadingList](/documentation/safariservices/ssreadinglist)

### Getting the Reading List Singleton Object

- [class func `default`() -> SSReadingList?](/documentation/safariservices/ssreadinglist/default())

### Checking Whether a URL is Supported by Reading List

- [class func supportsURL(URL) -> Bool](/documentation/safariservices/ssreadinglist/supportsurl(_:))

### Adding an Item to the Reading List

- [func addItem(with: URL, title: String?, previewText: String?) throws](/documentation/safariservices/ssreadinglist/additem(with:title:previewtext:))

### Constants

- [Reading List Error Domain](/documentation/safariservices/reading-list-error-domain)

#### Constants

- [let SSReadingListErrorDomain: String](/documentation/safariservices/ssreadinglisterrordomain)
- [SSReadingListError.Code](/documentation/safariservices/ssreadinglisterror/code)

#### Constants

- [case urlSchemeNotAllowed](/documentation/safariservices/ssreadinglisterror/code/urlschemenotallowed)

#### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/ssreadinglisterror/code/init(rawvalue:))
- [let SSReadingListErrorDomain: String](/documentation/safariservices/ssreadinglisterrordomain)
- [SSReadingListError.Code](/documentation/safariservices/ssreadinglisterror/code)

### Constants

- [case urlSchemeNotAllowed](/documentation/safariservices/ssreadinglisterror/code/urlschemenotallowed)

### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/ssreadinglisterror/code/init(rawvalue:))
- [SSReadingListError](/documentation/safariservices/ssreadinglisterror)

### Type Properties

- [static var urlSchemeNotAllowed: SSReadingListError.Code](/documentation/safariservices/ssreadinglisterror/urlschemenotallowed)
- [static var errorDomain: String](/documentation/safariservices/ssreadinglisterror/errordomain)

### Enumerations

- [SSReadingListError.Code](/documentation/safariservices/ssreadinglisterror/code)

#### Constants

- [case urlSchemeNotAllowed](/documentation/safariservices/ssreadinglisterror/code/urlschemenotallowed)

#### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/ssreadinglisterror/code/init(rawvalue:))

## Home Screen bookmarks

- [SFAddToHomeScreenActivityItem](/documentation/safariservices/sfaddtohomescreenactivityitem)

### Describing a bookmark or web app

- [var iconItemProvider: NSItemProvider?](/documentation/safariservices/sfaddtohomescreenactivityitem/iconitemprovider)
- [var title: String](/documentation/safariservices/sfaddtohomescreenactivityitem/title)
- [var url: URL](/documentation/safariservices/sfaddtohomescreenactivityitem/url)

### Providing information about a web app to the system

- [func getHomeScreenWebAppInfo(completionHandler: (SFAddToHomeScreenInfo?) -> Void)](/documentation/safariservices/sfaddtohomescreenactivityitem/gethomescreenwebappinfo(completionhandler:))
- [SFAddToHomeScreenInfo](/documentation/safariservices/sfaddtohomescreeninfo)

#### Creating an information object

- [init(manifest: BEWebAppManifest)](/documentation/safariservices/sfaddtohomescreeninfo/init(manifest:))

#### Information about a web app

- [var manifest: BEWebAppManifest](/documentation/safariservices/sfaddtohomescreeninfo/manifest)
- [var websiteCookies: [HTTPCookie]](/documentation/safariservices/sfaddtohomescreeninfo/websitecookies)
- [func getWebAppManifest(completionHandler: (BEWebAppManifest?) -> Void)](/documentation/safariservices/sfaddtohomescreenactivityitem/getwebappmanifest(completionhandler:))

## Miscellaneous errors

- [SFError](/documentation/safariservices/sferror)

### Error Codes

- [static var loadingInterrupted: SFError.Code](/documentation/safariservices/sferror/loadinginterrupted)
- [static var noAttachmentFound: SFError.Code](/documentation/safariservices/sferror/noattachmentfound)
- [static var noExtensionFound: SFError.Code](/documentation/safariservices/sferror/noextensionfound)
- [SFError.Code](/documentation/safariservices/sferror/code)

#### Error Codes

- [case loadingInterrupted](/documentation/safariservices/sferror/code/loadinginterrupted)
- [case noAttachmentFound](/documentation/safariservices/sferror/code/noattachmentfound)
- [case noExtensionFound](/documentation/safariservices/sferror/code/noextensionfound)

#### Enumeration Cases

- [case internalError](/documentation/safariservices/sferror/code/internalerror)
- [case maximumAttemptsExceeded](/documentation/safariservices/sferror/code/maximumattemptsexceeded)
- [case missingEntitlement](/documentation/safariservices/sferror/code/missingentitlement)

#### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/sferror/code/init(rawvalue:))

### Error Domain

- [let SFErrorDomain: String](/documentation/safariservices/sferrordomain)

### Type Properties

- [static var errorDomain: String](/documentation/safariservices/sferror/errordomain)
- [static var internalError: SFError.Code](/documentation/safariservices/sferror/internalerror)
- [static var maximumAttemptsExceeded: SFError.Code](/documentation/safariservices/sferror/maximumattemptsexceeded)
- [static var missingEntitlement: SFError.Code](/documentation/safariservices/sferror/missingentitlement)
- [SFError.Code](/documentation/safariservices/sferror/code)

### Error Codes

- [case loadingInterrupted](/documentation/safariservices/sferror/code/loadinginterrupted)
- [case noAttachmentFound](/documentation/safariservices/sferror/code/noattachmentfound)
- [case noExtensionFound](/documentation/safariservices/sferror/code/noextensionfound)

### Enumeration Cases

- [case internalError](/documentation/safariservices/sferror/code/internalerror)
- [case maximumAttemptsExceeded](/documentation/safariservices/sferror/code/maximumattemptsexceeded)
- [case missingEntitlement](/documentation/safariservices/sferror/code/missingentitlement)

### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/sferror/code/init(rawvalue:))
- [let SFErrorDomain: String](/documentation/safariservices/sferrordomain)

## Deprecated

- [Deprecated symbols](/documentation/safariservices/deprecated-symbols)

### Deprecated

- [let SFContentBlockerErrorDomain: String](/documentation/safariservices/sfcontentblockererrordomain)
- [SFContentBlockerErrorCode](/documentation/safariservices/sfcontentblockererrorcode)

#### Constants

- [case noExtensionFound](/documentation/safariservices/sfcontentblockererrorcode/noextensionfound)
- [case noAttachmentFound](/documentation/safariservices/sfcontentblockererrorcode/noattachmentfound)
- [case loadingInterrupted](/documentation/safariservices/sfcontentblockererrorcode/loadinginterrupted)

#### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/sfcontentblockererrorcode/init(rawvalue:))
- [SFAuthenticationSession](/documentation/safariservices/sfauthenticationsession)

#### Type Aliases

- [SFAuthenticationSession.CompletionHandler](/documentation/safariservices/sfauthenticationsession/completionhandler)

#### Initializers

- [init(url: URL, callbackURLScheme: String?, completionHandler: SFAuthenticationSession.CompletionHandler)](/documentation/safariservices/sfauthenticationsession/init(url:callbackurlscheme:completionhandler:))

#### Instance Methods

- [func cancel()](/documentation/safariservices/sfauthenticationsession/cancel())
- [func start() -> Bool](/documentation/safariservices/sfauthenticationsession/start())
- [SFAuthenticationError](/documentation/safariservices/sfauthenticationerror-swift.struct)

#### Type Properties

- [static var canceledLogin: SFAuthenticationError.Code](/documentation/safariservices/sfauthenticationerror-swift.struct/canceledlogin)
- [static var errorDomain: String](/documentation/safariservices/sfauthenticationerror-swift.struct/errordomain)

#### Enumerations

- [SFAuthenticationError.Code](/documentation/safariservices/sfauthenticationerror-swift.struct/code)

##### Enumeration Cases

- [case canceledLogin](/documentation/safariservices/sfauthenticationerror-swift.struct/code/canceledlogin)

##### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/sfauthenticationerror-swift.struct/code/init(rawvalue:))
- [SFAuthenticationError.Code](/documentation/safariservices/sfauthenticationerror-swift.struct/code)

#### Enumeration Cases

- [case canceledLogin](/documentation/safariservices/sfauthenticationerror-swift.struct/code/canceledlogin)

#### Initializers

- [init?(rawValue: Int)](/documentation/safariservices/sfauthenticationerror-swift.struct/code/init(rawvalue:))
- [let SFAuthenticationErrorDomain: String](/documentation/safariservices/sfauthenticationerrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
