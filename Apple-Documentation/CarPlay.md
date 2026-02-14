# CarPlay Documentation

Source: https://sosumi.ai/documentation/carplay

---
title: CarPlay
source: https://developer.apple.com/documentation/carplay
timestamp: 2026-02-13T18:54:41.138Z
---

## CarPlay Integration

- [Requesting CarPlay Entitlements](/documentation/carplay/requesting-carplay-entitlements)
- [Displaying Content in CarPlay](/documentation/carplay/displaying-content-in-carplay)
- [Supporting Previous Versions of iOS](/documentation/carplay/supporting-previous-versions-of-ios)
- [Using the CarPlay Simulator](/documentation/carplay/using-the-carplay-simulator)
- [CPTemplateApplicationScene](/documentation/carplay/cptemplateapplicationscene)

### Responding to the Scene Life Cycle

- [var delegate: (any CPTemplateApplicationSceneDelegate)?](/documentation/carplay/cptemplateapplicationscene/delegate)
- [CPTemplateApplicationSceneDelegate](/documentation/carplay/cptemplateapplicationscenedelegate)

#### Responding to the Scene Life Cycle

- [func templateApplicationScene(CPTemplateApplicationScene, didConnect: CPInterfaceController)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didconnect:))
- [func templateApplicationScene(CPTemplateApplicationScene, didConnect: CPInterfaceController, to: CPWindow)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didconnect:to:))
- [func templateApplicationScene(CPTemplateApplicationScene, didDisconnectInterfaceController: CPInterfaceController)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:diddisconnectinterfacecontroller:))
- [func templateApplicationScene(CPTemplateApplicationScene, didDisconnect: CPInterfaceController, from: CPWindow)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:diddisconnect:from:))

#### Responding to User Actions

- [func templateApplicationScene(CPTemplateApplicationScene, didSelect: CPManeuver)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didselect:)-5rf2h)
- [func templateApplicationScene(CPTemplateApplicationScene, didSelect: CPNavigationAlert)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didselect:)-7bie0)

#### Instance Methods

- [func contentStyleDidChange(UIUserInterfaceStyle)](/documentation/carplay/cptemplateapplicationscenedelegate/contentstyledidchange(_:))

### Accessing the Interface Controller

- [var interfaceController: CPInterfaceController](/documentation/carplay/cptemplateapplicationscene/interfacecontroller)
- [CPInterfaceController](/documentation/carplay/cpinterfacecontroller)

#### Configuring the Interface Controller

- [var delegate: (any CPInterfaceControllerDelegate)?](/documentation/carplay/cpinterfacecontroller/delegate)
- [CPInterfaceControllerDelegate](/documentation/carplay/cpinterfacecontrollerdelegate)

##### Handling Display Events

- [func templateWillAppear(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontrollerdelegate/templatewillappear(_:animated:))
- [func templateDidAppear(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontrollerdelegate/templatedidappear(_:animated:))
- [func templateWillDisappear(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontrollerdelegate/templatewilldisappear(_:animated:))
- [func templateDidDisappear(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontrollerdelegate/templatediddisappear(_:animated:))
- [var prefersDarkUserInterfaceStyle: Bool](/documentation/carplay/cpinterfacecontroller/prefersdarkuserinterfacestyle)
- [func setRootTemplate(CPTemplate, animated: Bool, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/carplay/cpinterfacecontroller/setroottemplate(_:animated:completion:))

#### Accessing the Trait Collection

- [var carTraitCollection: UITraitCollection](/documentation/carplay/cpinterfacecontroller/cartraitcollection)

#### Accessing Templates

- [var rootTemplate: CPTemplate](/documentation/carplay/cpinterfacecontroller/roottemplate)
- [var topTemplate: CPTemplate?](/documentation/carplay/cpinterfacecontroller/toptemplate)
- [var templates: [CPTemplate]](/documentation/carplay/cpinterfacecontroller/templates)

#### Adding and Removing Templates

- [func pushTemplate(CPTemplate, animated: Bool, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/carplay/cpinterfacecontroller/pushtemplate(_:animated:completion:))
- [func popTemplate(animated: Bool, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/carplay/cpinterfacecontroller/poptemplate(animated:completion:))
- [func popToRootTemplate(animated: Bool, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/carplay/cpinterfacecontroller/poptoroottemplate(animated:completion:))
- [func pop(to: CPTemplate, animated: Bool, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/carplay/cpinterfacecontroller/pop(to:animated:completion:))

#### Displaying Templates Modally

- [func presentTemplate(CPTemplate, animated: Bool, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/carplay/cpinterfacecontroller/presenttemplate(_:animated:completion:))
- [func dismissTemplate(animated: Bool, completion: ((Bool, (any Error)?) -> Void)?)](/documentation/carplay/cpinterfacecontroller/dismisstemplate(animated:completion:))
- [var presentedTemplate: CPTemplate?](/documentation/carplay/cpinterfacecontroller/presentedtemplate)

#### Deprecated

- [Deprecated Symbols](/documentation/carplay/cpinterfacecontroller-deprecated-symbols)

##### Deprecated Methods

- [func setRootTemplate(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/setroottemplate(_:animated:))
- [func pushTemplate(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/pushtemplate(_:animated:))
- [func popTemplate(animated: Bool)](/documentation/carplay/cpinterfacecontroller/poptemplate(animated:))
- [func popToRootTemplate(animated: Bool)](/documentation/carplay/cpinterfacecontroller/poptoroottemplate(animated:))
- [func pop(to: CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/pop(to:animated:))
- [func presentTemplate(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/presenttemplate(_:animated:))
- [func dismissTemplate(animated: Bool)](/documentation/carplay/cpinterfacecontroller/dismisstemplate(animated:))

### Accessing the Window

- [var carWindow: CPWindow](/documentation/carplay/cptemplateapplicationscene/carwindow)
- [CPWindow](/documentation/carplay/cpwindow)

#### Accessing the Scene

- [var templateApplicationScene: CPTemplateApplicationScene?](/documentation/carplay/cpwindow/templateapplicationscene)

#### Layout

- [var mapButtonSafeAreaLayoutGuide: UILayoutGuide](/documentation/carplay/cpwindow/mapbuttonsafearealayoutguide)

### Instance Properties

- [var contentStyle: UIUserInterfaceStyle](/documentation/carplay/cptemplateapplicationscene/contentstyle)
- [CPTemplateApplicationSceneDelegate](/documentation/carplay/cptemplateapplicationscenedelegate)

### Responding to the Scene Life Cycle

- [func templateApplicationScene(CPTemplateApplicationScene, didConnect: CPInterfaceController)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didconnect:))
- [func templateApplicationScene(CPTemplateApplicationScene, didConnect: CPInterfaceController, to: CPWindow)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didconnect:to:))
- [func templateApplicationScene(CPTemplateApplicationScene, didDisconnectInterfaceController: CPInterfaceController)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:diddisconnectinterfacecontroller:))
- [func templateApplicationScene(CPTemplateApplicationScene, didDisconnect: CPInterfaceController, from: CPWindow)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:diddisconnect:from:))

### Responding to User Actions

- [func templateApplicationScene(CPTemplateApplicationScene, didSelect: CPManeuver)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didselect:)-5rf2h)
- [func templateApplicationScene(CPTemplateApplicationScene, didSelect: CPNavigationAlert)](/documentation/carplay/cptemplateapplicationscenedelegate/templateapplicationscene(_:didselect:)-7bie0)

### Instance Methods

- [func contentStyleDidChange(UIUserInterfaceStyle)](/documentation/carplay/cptemplateapplicationscenedelegate/contentstyledidchange(_:))
- [CPSessionConfiguration](/documentation/carplay/cpsessionconfiguration)

### Creating a Session Configuration

- [init(delegate: any CPSessionConfigurationDelegate)](/documentation/carplay/cpsessionconfiguration/init(delegate:))
- [CPSessionConfigurationDelegate](/documentation/carplay/cpsessionconfigurationdelegate)

#### Handling Content Style Changes

- [func sessionConfiguration(CPSessionConfiguration, contentStyleChanged: CPContentStyle)](/documentation/carplay/cpsessionconfigurationdelegate/sessionconfiguration(_:contentstylechanged:))

#### Handling Limit Changes

- [func sessionConfiguration(CPSessionConfiguration, limitedUserInterfacesChanged: CPLimitableUserInterface)](/documentation/carplay/cpsessionconfigurationdelegate/sessionconfiguration(_:limiteduserinterfaceschanged:))

### Managing the Delegate

- [var delegate: (any CPSessionConfigurationDelegate)?](/documentation/carplay/cpsessionconfiguration/delegate)

### Getting the Content Style

- [var contentStyle: CPContentStyle](/documentation/carplay/cpsessionconfiguration/contentstyle)
- [CPContentStyle](/documentation/carplay/cpcontentstyle)

#### Creating a Content Style

- [init(rawValue: UInt)](/documentation/carplay/cpcontentstyle/init(rawvalue:))

#### Content Styles

- [static var dark: CPContentStyle](/documentation/carplay/cpcontentstyle/dark)
- [static var light: CPContentStyle](/documentation/carplay/cpcontentstyle/light)

### Getting the Limits

- [var limitedUserInterfaces: CPLimitableUserInterface](/documentation/carplay/cpsessionconfiguration/limiteduserinterfaces)
- [CPLimitableUserInterface](/documentation/carplay/cplimitableuserinterface)

#### User Interface Limits

- [static var keyboard: CPLimitableUserInterface](/documentation/carplay/cplimitableuserinterface/keyboard)
- [static var lists: CPLimitableUserInterface](/documentation/carplay/cplimitableuserinterface/lists)

#### Initializers

- [init(rawValue: UInt)](/documentation/carplay/cplimitableuserinterface/init(rawvalue:))

## General Purpose Templates

- [CPListTemplate](/documentation/carplay/cplisttemplate)

### Creating a List Template

- [init(title: String?, sections: [CPListSection])](/documentation/carplay/cplisttemplate/init(title:sections:))
- [init(title: String?, sections: [CPListSection], assistantCellConfiguration: CPAssistantCellConfiguration?)](/documentation/carplay/cplisttemplate/init(title:sections:assistantcellconfiguration:))

### Managing Sections

- [class var maximumSectionCount: Int](/documentation/carplay/cplisttemplate/maximumsectioncount)
- [var sectionCount: Int](/documentation/carplay/cplisttemplate/sectioncount)
- [var sections: [CPListSection]](/documentation/carplay/cplisttemplate/sections)
- [func updateSections([CPListSection])](/documentation/carplay/cplisttemplate/updatesections(_:))
- [CPListSection](/documentation/carplay/cplistsection)

#### Creating a Section

- [init(items: [any CPListTemplateItem], header: String, headerSubtitle: String?, headerImage: UIImage?, headerButton: CPButton?, sectionIndexTitle: String?)](/documentation/carplay/cplistsection/init(items:header:headersubtitle:headerimage:headerbutton:sectionindextitle:))
- [CPListTemplateItem](/documentation/carplay/cplisttemplateitem)

##### Managing Content

- [var text: String?](/documentation/carplay/cplisttemplateitem/text)
- [var userInfo: Any?](/documentation/carplay/cplisttemplateitem/userinfo)

##### Enabling Items

- [var isEnabled: Bool](/documentation/carplay/cplisttemplateitem/isenabled)
- [CPSelectableListItem](/documentation/carplay/cpselectablelistitem)

##### Managing Selection

- [var handler: ((any CPSelectableListItem, () -> Void) -> Void)?](/documentation/carplay/cpselectablelistitem/handler)
- [CPListItem](/documentation/carplay/cplistitem)

##### Creating a List Item

- [init(text: String?, detailText: String?)](/documentation/carplay/cplistitem/init(text:detailtext:))
- [init(text: String?, detailText: String?, image: UIImage?)](/documentation/carplay/cplistitem/init(text:detailtext:image:))
- [init(text: String?, detailText: String?, image: UIImage?, accessoryImage: UIImage?, accessoryType: CPListItemAccessoryType)](/documentation/carplay/cplistitem/init(text:detailtext:image:accessoryimage:accessorytype:))

##### Managing Configuration

- [var isEnabled: Bool](/documentation/carplay/cplistitem/isenabled)
- [var handler: ((any CPSelectableListItem, () -> Void) -> Void)?](/documentation/carplay/cplistitem/handler)
- [var userInfo: Any?](/documentation/carplay/cplistitem/userinfo)

##### Managing Accessories

- [var accessoryType: CPListItemAccessoryType](/documentation/carplay/cplistitem/accessorytype)
- [CPListItemAccessoryType](/documentation/carplay/cplistitemaccessorytype)

###### Accessory Types

- [case none](/documentation/carplay/cplistitemaccessorytype/none)
- [case disclosureIndicator](/documentation/carplay/cplistitemaccessorytype/disclosureindicator)
- [case cloud](/documentation/carplay/cplistitemaccessorytype/cloud)

###### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplistitemaccessorytype/init(rawvalue:))
- [var accessoryImage: UIImage?](/documentation/carplay/cplistitem/accessoryimage)
- [func setAccessoryImage(UIImage?)](/documentation/carplay/cplistitem/setaccessoryimage(_:))

##### Managing Content

- [var text: String?](/documentation/carplay/cplistitem/text)
- [func setText(String)](/documentation/carplay/cplistitem/settext(_:))
- [var detailText: String?](/documentation/carplay/cplistitem/detailtext)
- [func setDetailText(String?)](/documentation/carplay/cplistitem/setdetailtext(_:))
- [var image: UIImage?](/documentation/carplay/cplistitem/image)
- [func setImage(UIImage?)](/documentation/carplay/cplistitem/setimage(_:))
- [class var maximumImageSize: CGSize](/documentation/carplay/cplistitem/maximumimagesize)

##### Managing Playback Information

- [var isExplicitContent: Bool](/documentation/carplay/cplistitem/isexplicitcontent)
- [var isPlaying: Bool](/documentation/carplay/cplistitem/isplaying)
- [var playingIndicatorLocation: CPListItemPlayingIndicatorLocation](/documentation/carplay/cplistitem/playingindicatorlocation)
- [CPListItemPlayingIndicatorLocation](/documentation/carplay/cplistitemplayingindicatorlocation)

###### Now Playing Indicator Locations

- [case leading](/documentation/carplay/cplistitemplayingindicatorlocation/leading)
- [case trailing](/documentation/carplay/cplistitemplayingindicatorlocation/trailing)

###### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplistitemplayingindicatorlocation/init(rawvalue:))
- [var playbackProgress: CGFloat](/documentation/carplay/cplistitem/playbackprogress)

##### Managing the Assistant Cell

- [CPListItem.AssistantCellPosition](/documentation/carplay/cplistitem/assistantcellposition)

###### Controlling the Assistant Cell Position

- [case bottom](/documentation/carplay/cplistitem/assistantcellposition/bottom)
- [case top](/documentation/carplay/cplistitem/assistantcellposition/top)

###### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplistitem/assistantcellposition/init(rawvalue:))
- [CPListItem.AssistantCellVisibility](/documentation/carplay/cplistitem/assistantcellvisibility)

###### Controlling the Assistant Cell Visibility

- [case off](/documentation/carplay/cplistitem/assistantcellvisibility/off)
- [case always](/documentation/carplay/cplistitem/assistantcellvisibility/always)
- [case whileLimitedUIActive](/documentation/carplay/cplistitem/assistantcellvisibility/whilelimiteduiactive)

###### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplistitem/assistantcellvisibility/init(rawvalue:))

##### Deprecated

- [Deprecated Symbols](/documentation/carplay/cplistitem-deprecated-symbols)

###### Deprecated Methods

- [init(text: String?, detailText: String?, image: UIImage?, showsDisclosureIndicator: Bool)](/documentation/carplay/cplistitem/init(text:detailtext:image:showsdisclosureindicator:))

###### Deprecated Properties

- [var showsDisclosureIndicator: Bool](/documentation/carplay/cplistitem/showsdisclosureindicator)
- [var showsExplicitLabel: Bool](/documentation/carplay/cplistitem/showsexplicitlabel)
- [func setRootTemplate(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/setroottemplate(_:animated:))
- [func pushTemplate(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/pushtemplate(_:animated:))
- [func popTemplate(animated: Bool)](/documentation/carplay/cpinterfacecontroller/poptemplate(animated:))
- [func popToRootTemplate(animated: Bool)](/documentation/carplay/cpinterfacecontroller/poptoroottemplate(animated:))
- [func pop(to: CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/pop(to:animated:))
- [func presentTemplate(CPTemplate, animated: Bool)](/documentation/carplay/cpinterfacecontroller/presenttemplate(_:animated:))
- [func dismissTemplate(animated: Bool)](/documentation/carplay/cpinterfacecontroller/dismisstemplate(animated:))
- [CPListImageRowItem](/documentation/carplay/cplistimagerowitem)

##### Creating a List Image Row Item

- [init(text: String, images: [UIImage])](/documentation/carplay/cplistimagerowitem/init(text:images:))
- [init(text: String, images: [UIImage], imageTitles: [String])](/documentation/carplay/cplistimagerowitem/init(text:images:imagetitles:))

##### Managing Content

- [var text: String?](/documentation/carplay/cplistimagerowitem/text)
- [var gridImages: [UIImage]](/documentation/carplay/cplistimagerowitem/gridimages)
- [func update([UIImage])](/documentation/carplay/cplistimagerowitem/update(_:))
- [class var maximumImageSize: CGSize](/documentation/carplay/cplistimagerowitem/maximumimagesize)
- [let CPMaximumNumberOfGridImages: Int](/documentation/carplay/cpmaximumnumberofgridimages)

##### Managing Selection

- [var listImageRowHandler: ((CPListImageRowItem, Int, () -> Void) -> Void)?](/documentation/carplay/cplistimagerowitem/listimagerowhandler)
- [var handler: ((any CPSelectableListItem, () -> Void) -> Void)?](/documentation/carplay/cplistimagerowitem/handler)

##### Managing Supplementary Information

- [var userInfo: Any?](/documentation/carplay/cplistimagerowitem/userinfo)

##### Enabling Items

- [var isEnabled: Bool](/documentation/carplay/cplistimagerowitem/isenabled)

##### Initializers

- [init(text: String?, cardElements: [CPListImageRowItemCardElement], allowsMultipleLines: Bool)](/documentation/carplay/cplistimagerowitem/init(text:cardelements:allowsmultiplelines:))
- [init(text: String?, condensedElements: [CPListImageRowItemCondensedElement], allowsMultipleLines: Bool)](/documentation/carplay/cplistimagerowitem/init(text:condensedelements:allowsmultiplelines:))
- [init(text: String?, elements: [CPListImageRowItemRowElement], allowsMultipleLines: Bool)](/documentation/carplay/cplistimagerowitem/init(text:elements:allowsmultiplelines:))
- [init(text: String?, gridElements: [CPListImageRowItemGridElement], allowsMultipleLines: Bool)](/documentation/carplay/cplistimagerowitem/init(text:gridelements:allowsmultiplelines:))
- [init(text: String?, imageGridElements: [CPListImageRowItemImageGridElement], allowsMultipleLines: Bool)](/documentation/carplay/cplistimagerowitem/init(text:imagegridelements:allowsmultiplelines:))

##### Instance Properties

- [var allowsMultipleLines: Bool](/documentation/carplay/cplistimagerowitem/allowsmultiplelines)
- [var elements: [CPListImageRowItemElement]](/documentation/carplay/cplistimagerowitem/elements)
- [var imageTitles: [String]](/documentation/carplay/cplistimagerowitem/imagetitles)
- [CPMessageListItem](/documentation/carplay/cpmessagelistitem)

##### Creating a Message List Item

- [init(conversationIdentifier: String, text: String, leadingConfiguration: CPMessageListItemLeadingConfiguration, trailingConfiguration: CPMessageListItemTrailingConfiguration?, detailText: String?, trailingText: String?)](/documentation/carplay/cpmessagelistitem/init(conversationidentifier:text:leadingconfiguration:trailingconfiguration:detailtext:trailingtext:))
- [init(fullName: String, phoneOrEmailAddress: String, leadingConfiguration: CPMessageListItemLeadingConfiguration, trailingConfiguration: CPMessageListItemTrailingConfiguration?, detailText: String?, trailingText: String?)](/documentation/carplay/cpmessagelistitem/init(fullname:phoneoremailaddress:leadingconfiguration:trailingconfiguration:detailtext:trailingtext:))

##### Managing the Message Context

- [var conversationIdentifier: String?](/documentation/carplay/cpmessagelistitem/conversationidentifier)
- [var phoneOrEmailAddress: String?](/documentation/carplay/cpmessagelistitem/phoneoremailaddress)

##### Managing Content

- [var text: String?](/documentation/carplay/cpmessagelistitem/text)
- [var detailText: String?](/documentation/carplay/cpmessagelistitem/detailtext)
- [var trailingText: String?](/documentation/carplay/cpmessagelistitem/trailingtext)

##### Managing Leading and Trailing Configurations

- [var leadingConfiguration: CPMessageListItemLeadingConfiguration](/documentation/carplay/cpmessagelistitem/leadingconfiguration)
- [CPMessageListItemLeadingConfiguration](/documentation/carplay/cpmessagelistitemleadingconfiguration)

###### Creating a Configuration

- [init(leadingItem: CPMessageLeadingItem, leadingImage: UIImage?, unread: Bool)](/documentation/carplay/cpmessagelistitemleadingconfiguration/init(leadingitem:leadingimage:unread:))
- [let CPMaximumMessageItemImageSize: CGSize](/documentation/carplay/cpmaximummessageitemimagesize)

###### Getting the Leading Item

- [var leadingItem: CPMessageLeadingItem](/documentation/carplay/cpmessagelistitemleadingconfiguration/leadingitem)
- [CPMessageLeadingItem](/documentation/carplay/cpmessageleadingitem)

###### Leading Items

- [case none](/documentation/carplay/cpmessageleadingitem/none)
- [case pin](/documentation/carplay/cpmessageleadingitem/pin)
- [case star](/documentation/carplay/cpmessageleadingitem/star)

###### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cpmessageleadingitem/init(rawvalue:))

###### Getting the Configuration’s State

- [var leadingImage: UIImage?](/documentation/carplay/cpmessagelistitemleadingconfiguration/leadingimage)
- [var isUnread: Bool](/documentation/carplay/cpmessagelistitemleadingconfiguration/isunread)
- [var trailingConfiguration: CPMessageListItemTrailingConfiguration?](/documentation/carplay/cpmessagelistitem/trailingconfiguration)
- [CPMessageListItemTrailingConfiguration](/documentation/carplay/cpmessagelistitemtrailingconfiguration)

###### Creating a Configuration

- [init(trailingItem: CPMessageTrailingItem, trailingImage: UIImage?)](/documentation/carplay/cpmessagelistitemtrailingconfiguration/init(trailingitem:trailingimage:))
- [let CPMaximumMessageItemImageSize: CGSize](/documentation/carplay/cpmaximummessageitemimagesize)

###### Getting the Trailing Item

- [var trailingItem: CPMessageTrailingItem](/documentation/carplay/cpmessagelistitemtrailingconfiguration/trailingitem)
- [CPMessageTrailingItem](/documentation/carplay/cpmessagetrailingitem)

###### Trailing Items

- [case none](/documentation/carplay/cpmessagetrailingitem/none)
- [case mute](/documentation/carplay/cpmessagetrailingitem/mute)

###### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cpmessagetrailingitem/init(rawvalue:))

###### Getting the Trailing Image

- [var trailingImage: UIImage?](/documentation/carplay/cpmessagelistitemtrailingconfiguration/trailingimage)

##### Managing Supplementary Information

- [var userInfo: Any?](/documentation/carplay/cpmessagelistitem/userinfo)

##### Enabling Items

- [var isEnabled: Bool](/documentation/carplay/cpmessagelistitem/isenabled)

##### Instance Properties

- [var leadingDetailTextImage: UIImage?](/documentation/carplay/cpmessagelistitem/leadingdetailtextimage)

#### Getting Supplementary Information

- [var header: String?](/documentation/carplay/cplistsection/header)
- [var sectionIndexTitle: String?](/documentation/carplay/cplistsection/sectionindextitle)

#### Getting Items

- [var items: [any CPListTemplateItem]](/documentation/carplay/cplistsection/items)
- [func index(of: any CPListTemplateItem) -> Int](/documentation/carplay/cplistsection/index(of:))
- [func item(at: Int) -> any CPListTemplateItem](/documentation/carplay/cplistsection/item(at:))

#### Configuring Section Headers

- [var headerButton: CPButton?](/documentation/carplay/cplistsection/headerbutton)
- [var headerImage: UIImage?](/documentation/carplay/cplistsection/headerimage)
- [var headerSubtitle: String?](/documentation/carplay/cplistsection/headersubtitle)

#### Initializers

- [convenience init(items: [CPListItem])](/documentation/carplay/cplistsection/init(items:)-32d0q)
- [convenience init(items: [CPListItem], header: String?, sectionIndexTitle: String?)](/documentation/carplay/cplistsection/init(items:header:sectionindextitle:)-743we)
- [convenience init(items: [any CPListTemplateItem])](/documentation/carplay/cplistsection/init(items:)-6ksy3)
- [convenience init(items: [any CPListTemplateItem], header: String?, sectionIndexTitle: String?)](/documentation/carplay/cplistsection/init(items:header:sectionindextitle:)-6xewg)

### Managing the Assistant Cell

- [var assistantCellConfiguration: CPAssistantCellConfiguration?](/documentation/carplay/cplisttemplate/assistantcellconfiguration)
- [CPAssistantCellConfiguration](/documentation/carplay/cpassistantcellconfiguration)

#### Creating an Assistant Cell Configuration

- [init(position: CPListItem.AssistantCellPosition, visibility: CPListItem.AssistantCellVisibility, assistantAction: CPAssistantCellActionType)](/documentation/carplay/cpassistantcellconfiguration/init(position:visibility:assistantaction:))

#### Getting the Configuration Attributes

- [var position: CPListItem.AssistantCellPosition](/documentation/carplay/cpassistantcellconfiguration/position)
- [var visibility: CPListItem.AssistantCellVisibility](/documentation/carplay/cpassistantcellconfiguration/visibility)
- [var assistantAction: CPAssistantCellActionType](/documentation/carplay/cpassistantcellconfiguration/assistantaction)
- [CPAssistantCellActionType](/documentation/carplay/cpassistantcellactiontype)

##### Siri Actions

- [case playMedia](/documentation/carplay/cpassistantcellactiontype/playmedia)
- [case startCall](/documentation/carplay/cpassistantcellactiontype/startcall)

##### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cpassistantcellactiontype/init(rawvalue:))

### Managing an Empty List

- [var emptyViewTitleVariants: [String]](/documentation/carplay/cplisttemplate/emptyviewtitlevariants)
- [var emptyViewSubtitleVariants: [String]](/documentation/carplay/cplisttemplate/emptyviewsubtitlevariants)

### Getting Supplementary Information

- [class var maximumItemCount: Int](/documentation/carplay/cplisttemplate/maximumitemcount)
- [var itemCount: Int](/documentation/carplay/cplisttemplate/itemcount)
- [func indexPath(for: any CPListTemplateItem) -> IndexPath?](/documentation/carplay/cplisttemplate/indexpath(for:))
- [var title: String?](/documentation/carplay/cplisttemplate/title)

### Responding to List Events

- [var delegate: (any CPListTemplateDelegate)?](/documentation/carplay/cplisttemplate/delegate)
- [CPListTemplateDelegate](/documentation/carplay/cplisttemplatedelegate)

#### Getting the Selected Item

- [func listTemplate(CPListTemplate, didSelect: CPListItem, completionHandler: () -> Void)](/documentation/carplay/cplisttemplatedelegate/listtemplate(_:didselect:completionhandler:))

### Initializers

- [init(title: String?, sections: [CPListSection], assistantCellConfiguration: CPAssistantCellConfiguration?, headerGridButtons: [CPGridButton]?)](/documentation/carplay/cplisttemplate/init(title:sections:assistantcellconfiguration:headergridbuttons:))

### Instance Properties

- [var headerGridButtons: [CPGridButton]?](/documentation/carplay/cplisttemplate/headergridbuttons)
- [var showsSpinnerWhileEmpty: Bool](/documentation/carplay/cplisttemplate/showsspinnerwhileempty)

### Type Properties

- [class var maximumGridButtonImageSize: CGSize](/documentation/carplay/cplisttemplate/maximumgridbuttonimagesize)
- [class var maximumHeaderGridButtonCount: Int](/documentation/carplay/cplisttemplate/maximumheadergridbuttoncount)
- [CPGridTemplate](/documentation/carplay/cpgridtemplate)

### Creating a Grid Template

- [init(title: String?, gridButtons: [CPGridButton])](/documentation/carplay/cpgridtemplate/init(title:gridbuttons:))
- [CPGridButton](/documentation/carplay/cpgridbutton)

#### Creating a Grid Button

- [convenience init(titleVariants: [String], image: UIImage, handler: ((CPGridButton) -> Void)?)](/documentation/carplay/cpgridbutton/init(titlevariants:image:handler:))

#### Controlling the Grid Button

- [var isEnabled: Bool](/documentation/carplay/cpgridbutton/isenabled)

#### Obtaining Grid Button Information

- [var titleVariants: [String]](/documentation/carplay/cpgridbutton/titlevariants)
- [var image: UIImage](/documentation/carplay/cpgridbutton/image)

#### Initializers

- [init(titleVariants: [String], image: UIImage, messageConfiguration: CPMessageGridItemConfiguration?, handler: ((CPGridButton) -> Void)?)](/documentation/carplay/cpgridbutton/init(titlevariants:image:messageconfiguration:handler:))

#### Instance Properties

- [var messageConfiguration: CPMessageGridItemConfiguration?](/documentation/carplay/cpgridbutton/messageconfiguration)

#### Instance Methods

- [func updateImage(UIImage)](/documentation/carplay/cpgridbutton/updateimage(_:))
- [func updateTitleVariants([String])](/documentation/carplay/cpgridbutton/updatetitlevariants(_:))

### Getting the Grid Title

- [var title: String](/documentation/carplay/cpgridtemplate/title)

### Getting the Grid Buttons

- [var gridButtons: [CPGridButton]](/documentation/carplay/cpgridtemplate/gridbuttons)

### Instance Methods

- [func updateGridButtons([CPGridButton])](/documentation/carplay/cpgridtemplate/updategridbuttons(_:))
- [func updateTitle(String)](/documentation/carplay/cpgridtemplate/updatetitle(_:))

### Type Properties

- [class var maximumGridButtonImageSize: CGSize](/documentation/carplay/cpgridtemplate/maximumgridbuttonimagesize)
- [CPTabBarTemplate](/documentation/carplay/cptabbartemplate)

### Creating a Tab Bar Template

- [init(templates: [CPTemplate])](/documentation/carplay/cptabbartemplate/init(templates:))

### Managing Tab Bar Interactions

- [var delegate: (any CPTabBarTemplateDelegate)?](/documentation/carplay/cptabbartemplate/delegate)
- [CPTabBarTemplateDelegate](/documentation/carplay/cptabbartemplatedelegate)

#### Managing the Selected Template

- [func tabBarTemplate(CPTabBarTemplate, didSelect: CPTemplate)](/documentation/carplay/cptabbartemplatedelegate/tabbartemplate(_:didselect:))

### Managing the Templates

- [var templates: [CPTemplate]](/documentation/carplay/cptabbartemplate/templates)
- [func updateTemplates([CPTemplate])](/documentation/carplay/cptabbartemplate/updatetemplates(_:))
- [class var maximumTabCount: Int](/documentation/carplay/cptabbartemplate/maximumtabcount)

### Getting the Selected Template

- [var selectedTemplate: CPTemplate?](/documentation/carplay/cptabbartemplate/selectedtemplate)

### Instance Methods

- [func select(CPTemplate)](/documentation/carplay/cptabbartemplate/select(_:))
- [func selectTemplate(at: Int)](/documentation/carplay/cptabbartemplate/selecttemplate(at:))
- [CPTemplate](/documentation/carplay/cptemplate)

### Accessing Template Information

- [var userInfo: Any?](/documentation/carplay/cptemplate/userinfo)

### Accessing Tab Information

- [var tabTitle: String?](/documentation/carplay/cptemplate/tabtitle)
- [var tabImage: UIImage?](/documentation/carplay/cptemplate/tabimage)
- [var tabSystemItem: UITabBarItem.SystemItem](/documentation/carplay/cptemplate/tabsystemitem)
- [var showsTabBadge: Bool](/documentation/carplay/cptemplate/showstabbadge)
- [CPBarButtonProviding](/documentation/carplay/cpbarbuttonproviding)

### Providing Navigation Bar Buttons

- [var backButton: CPBarButton?](/documentation/carplay/cpbarbuttonproviding/backbutton)
- [var leadingNavigationBarButtons: [CPBarButton]](/documentation/carplay/cpbarbuttonproviding/leadingnavigationbarbuttons)
- [var trailingNavigationBarButtons: [CPBarButton]](/documentation/carplay/cpbarbuttonproviding/trailingnavigationbarbuttons)
- [CPBarButton](/documentation/carplay/cpbarbutton)

#### Creating a CarPlay Bar Button

- [init?(coder: NSCoder)](/documentation/carplay/cpbarbutton/init(coder:))
- [init(type: CPBarButton.Type, handler: CPBarButtonHandler?)](/documentation/carplay/cpbarbutton/init(type:handler:))
- [init(image: UIImage, handler: CPBarButtonHandler?)](/documentation/carplay/cpbarbutton/init(image:handler:))
- [init(title: String, handler: CPBarButtonHandler?)](/documentation/carplay/cpbarbutton/init(title:handler:))
- [CPBarButton.Type](/documentation/carplay/cpbarbutton/type)

##### Button Types

- [case text](/documentation/carplay/cpbarbutton/type/text)
- [case image](/documentation/carplay/cpbarbutton/type/image)

##### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpbarbutton/type/init(rawvalue:))
- [CPBarButtonHandler](/documentation/carplay/cpbarbuttonhandler)

#### Configuring the Button

- [var isEnabled: Bool](/documentation/carplay/cpbarbutton/isenabled)
- [var image: UIImage?](/documentation/carplay/cpbarbutton/image)
- [var title: String?](/documentation/carplay/cpbarbutton/title)

#### Getting the Button Style

- [var buttonType: CPBarButton.Type](/documentation/carplay/cpbarbutton/buttontype)
- [var buttonStyle: CPBarButtonStyle](/documentation/carplay/cpbarbutton/buttonstyle)
- [CPBarButtonStyle](/documentation/carplay/cpbarbuttonstyle)

##### Button Styles

- [case none](/documentation/carplay/cpbarbuttonstyle/none)
- [case rounded](/documentation/carplay/cpbarbuttonstyle/rounded)

##### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cpbarbuttonstyle/init(rawvalue:))
- [CPMessageComposeBarButton](/documentation/carplay/cpmessagecomposebarbutton)

#### Creating a Message Compose Bar Button

- [init()](/documentation/carplay/cpmessagecomposebarbutton/init())
- [init(image: UIImage)](/documentation/carplay/cpmessagecomposebarbutton/init(image:))

## Audio

- [Integrating CarPlay with Your Music App](/documentation/carplay/integrating-carplay-with-your-music-app)
- [CPNowPlayingTemplate](/documentation/carplay/cpnowplayingtemplate)

### Managing the Shared Template

- [class var shared: CPNowPlayingTemplate](/documentation/carplay/cpnowplayingtemplate/shared)

### Managing the Template’s Buttons

- [var nowPlayingButtons: [CPNowPlayingButton]](/documentation/carplay/cpnowplayingtemplate/nowplayingbuttons)
- [func updateNowPlayingButtons([CPNowPlayingButton])](/documentation/carplay/cpnowplayingtemplate/updatenowplayingbuttons(_:))
- [CPNowPlayingButton](/documentation/carplay/cpnowplayingbutton)

#### Creating a Button

- [init(handler: ((CPNowPlayingButton) -> Void)?)](/documentation/carplay/cpnowplayingbutton/init(handler:))

#### Managing the Button State

- [var isEnabled: Bool](/documentation/carplay/cpnowplayingbutton/isenabled)
- [var isSelected: Bool](/documentation/carplay/cpnowplayingbutton/isselected)
- [CPNowPlayingImageButton](/documentation/carplay/cpnowplayingimagebutton)

#### Creating a Button

- [init(image: UIImage, handler: ((CPNowPlayingButton) -> Void)?)](/documentation/carplay/cpnowplayingimagebutton/init(image:handler:))
- [let CPNowPlayingButtonMaximumImageSize: CGSize](/documentation/carplay/cpnowplayingbuttonmaximumimagesize)

#### Getting the Button’s Image

- [var image: UIImage?](/documentation/carplay/cpnowplayingimagebutton/image)
- [CPNowPlayingAddToLibraryButton](/documentation/carplay/cpnowplayingaddtolibrarybutton)
- [CPNowPlayingMoreButton](/documentation/carplay/cpnowplayingmorebutton)
- [CPNowPlayingPlaybackRateButton](/documentation/carplay/cpnowplayingplaybackratebutton)
- [CPNowPlayingRepeatButton](/documentation/carplay/cpnowplayingrepeatbutton)
- [CPNowPlayingShuffleButton](/documentation/carplay/cpnowplayingshufflebutton)

### Managing Albums, Artists, and Up Next

- [var isAlbumArtistButtonEnabled: Bool](/documentation/carplay/cpnowplayingtemplate/isalbumartistbuttonenabled)
- [var isUpNextButtonEnabled: Bool](/documentation/carplay/cpnowplayingtemplate/isupnextbuttonenabled)
- [var upNextTitle: String](/documentation/carplay/cpnowplayingtemplate/upnexttitle)

### Observing Now Playing Events

- [func add(any CPNowPlayingTemplateObserver)](/documentation/carplay/cpnowplayingtemplate/add(_:))
- [func remove(any CPNowPlayingTemplateObserver)](/documentation/carplay/cpnowplayingtemplate/remove(_:))
- [CPNowPlayingTemplateObserver](/documentation/carplay/cpnowplayingtemplateobserver)

#### Responding to User Interactions

- [func nowPlayingTemplateAlbumArtistButtonTapped(CPNowPlayingTemplate)](/documentation/carplay/cpnowplayingtemplateobserver/nowplayingtemplatealbumartistbuttontapped(_:))
- [func nowPlayingTemplateUpNextButtonTapped(CPNowPlayingTemplate)](/documentation/carplay/cpnowplayingtemplateobserver/nowplayingtemplateupnextbuttontapped(_:))

### Instance Properties

- [var nowPlayingMode: CPNowPlayingMode?](/documentation/carplay/cpnowplayingtemplate/nowplayingmode)

## Instrument cluster

- [CPInstrumentClusterController](/documentation/carplay/cpinstrumentclustercontroller)

### Instance Properties

- [var attributedInactiveDescriptionVariants: [NSAttributedString]](/documentation/carplay/cpinstrumentclustercontroller/attributedinactivedescriptionvariants)
- [var compassSetting: CPInstrumentClusterSetting](/documentation/carplay/cpinstrumentclustercontroller/compasssetting)
- [var delegate: (any CPInstrumentClusterControllerDelegate)?](/documentation/carplay/cpinstrumentclustercontroller/delegate)
- [var inactiveDescriptionVariants: [String]](/documentation/carplay/cpinstrumentclustercontroller/inactivedescriptionvariants)
- [var instrumentClusterWindow: UIWindow?](/documentation/carplay/cpinstrumentclustercontroller/instrumentclusterwindow)
- [var speedLimitSetting: CPInstrumentClusterSetting](/documentation/carplay/cpinstrumentclustercontroller/speedlimitsetting)
- [CPInstrumentClusterControllerDelegate](/documentation/carplay/cpinstrumentclustercontrollerdelegate)

### Instance Methods

- [func instrumentClusterController(CPInstrumentClusterController, didChangeCompassSetting: CPInstrumentClusterSetting)](/documentation/carplay/cpinstrumentclustercontrollerdelegate/instrumentclustercontroller(_:didchangecompasssetting:))
- [func instrumentClusterController(CPInstrumentClusterController, didChangeSpeedLimitSetting: CPInstrumentClusterSetting)](/documentation/carplay/cpinstrumentclustercontrollerdelegate/instrumentclustercontroller(_:didchangespeedlimitsetting:))
- [func instrumentClusterControllerDidConnect(UIWindow)](/documentation/carplay/cpinstrumentclustercontrollerdelegate/instrumentclustercontrollerdidconnect(_:))
- [func instrumentClusterControllerDidDisconnectWindow(UIWindow)](/documentation/carplay/cpinstrumentclustercontrollerdelegate/instrumentclustercontrollerdiddisconnectwindow(_:))
- [func instrumentClusterControllerDidZoom(in: CPInstrumentClusterController)](/documentation/carplay/cpinstrumentclustercontrollerdelegate/instrumentclustercontrollerdidzoom(in:))
- [func instrumentClusterControllerDidZoomOut(CPInstrumentClusterController)](/documentation/carplay/cpinstrumentclustercontrollerdelegate/instrumentclustercontrollerdidzoomout(_:))
- [CPTemplateApplicationInstrumentClusterScene](/documentation/carplay/cptemplateapplicationinstrumentclusterscene)

### Instance Properties

- [var contentStyle: UIUserInterfaceStyle](/documentation/carplay/cptemplateapplicationinstrumentclusterscene/contentstyle)
- [var delegate: (any CPTemplateApplicationInstrumentClusterSceneDelegate)?](/documentation/carplay/cptemplateapplicationinstrumentclusterscene/delegate)
- [var instrumentClusterController: CPInstrumentClusterController](/documentation/carplay/cptemplateapplicationinstrumentclusterscene/instrumentclustercontroller)
- [CPTemplateApplicationInstrumentClusterSceneDelegate](/documentation/carplay/cptemplateapplicationinstrumentclusterscenedelegate)

### Instance Methods

- [func contentStyleDidChange(UIUserInterfaceStyle)](/documentation/carplay/cptemplateapplicationinstrumentclusterscenedelegate/contentstyledidchange(_:))
- [func templateApplicationInstrumentClusterScene(CPTemplateApplicationInstrumentClusterScene, didConnect: CPInstrumentClusterController)](/documentation/carplay/cptemplateapplicationinstrumentclusterscenedelegate/templateapplicationinstrumentclusterscene(_:didconnect:))
- [func templateApplicationInstrumentClusterScene(CPTemplateApplicationInstrumentClusterScene, didDisconnectInstrumentClusterController: CPInstrumentClusterController)](/documentation/carplay/cptemplateapplicationinstrumentclusterscenedelegate/templateapplicationinstrumentclusterscene(_:diddisconnectinstrumentclustercontroller:))

## Navigation

- [Integrating CarPlay with Your Navigation App](/documentation/carplay/integrating-carplay-with-your-navigation-app)
- [CPTemplateApplicationDashboardScene](/documentation/carplay/cptemplateapplicationdashboardscene)

### Responding to the Dashboard Scene Life Cycle

- [var delegate: (any CPTemplateApplicationDashboardSceneDelegate)?](/documentation/carplay/cptemplateapplicationdashboardscene/delegate)
- [CPTemplateApplicationDashboardSceneDelegate](/documentation/carplay/cptemplateapplicationdashboardscenedelegate)

#### Responding to the Scene Life Cycle

- [func templateApplicationDashboardScene(CPTemplateApplicationDashboardScene, didConnect: CPDashboardController, to: UIWindow)](/documentation/carplay/cptemplateapplicationdashboardscenedelegate/templateapplicationdashboardscene(_:didconnect:to:))
- [func templateApplicationDashboardScene(CPTemplateApplicationDashboardScene, didDisconnect: CPDashboardController, from: UIWindow)](/documentation/carplay/cptemplateapplicationdashboardscenedelegate/templateapplicationdashboardscene(_:diddisconnect:from:))

### Accessing the Dashboard Controller

- [var dashboardController: CPDashboardController](/documentation/carplay/cptemplateapplicationdashboardscene/dashboardcontroller)
- [CPDashboardController](/documentation/carplay/cpdashboardcontroller)

#### Providing Dashboard Buttons

- [var shortcutButtons: [CPDashboardButton]](/documentation/carplay/cpdashboardcontroller/shortcutbuttons)
- [CPDashboardButton](/documentation/carplay/cpdashboardbutton)

##### Creating a Dashboard Button

- [init(titleVariants: [String], subtitleVariants: [String], image: UIImage, handler: ((CPDashboardButton) -> Void)?)](/documentation/carplay/cpdashboardbutton/init(titlevariants:subtitlevariants:image:handler:))

##### Accessing the Button Configuration

- [var titleVariants: [String]](/documentation/carplay/cpdashboardbutton/titlevariants)
- [var subtitleVariants: [String]](/documentation/carplay/cpdashboardbutton/subtitlevariants)
- [var image: UIImage](/documentation/carplay/cpdashboardbutton/image)

### Accessing the Dashboard Window

- [var dashboardWindow: UIWindow](/documentation/carplay/cptemplateapplicationdashboardscene/dashboardwindow)
- [CPTemplateApplicationDashboardSceneDelegate](/documentation/carplay/cptemplateapplicationdashboardscenedelegate)

### Responding to the Scene Life Cycle

- [func templateApplicationDashboardScene(CPTemplateApplicationDashboardScene, didConnect: CPDashboardController, to: UIWindow)](/documentation/carplay/cptemplateapplicationdashboardscenedelegate/templateapplicationdashboardscene(_:didconnect:to:))
- [func templateApplicationDashboardScene(CPTemplateApplicationDashboardScene, didDisconnect: CPDashboardController, from: UIWindow)](/documentation/carplay/cptemplateapplicationdashboardscenedelegate/templateapplicationdashboardscene(_:diddisconnect:from:))
- [CPMapTemplate](/documentation/carplay/cpmaptemplate)

### Configuring Map Templates

- [var automaticallyHidesNavigationBar: Bool](/documentation/carplay/cpmaptemplate/automaticallyhidesnavigationbar)
- [var hidesButtonsWithNavigationBar: Bool](/documentation/carplay/cpmaptemplate/hidesbuttonswithnavigationbar)
- [var guidanceBackgroundColor: UIColor](/documentation/carplay/cpmaptemplate/guidancebackgroundcolor)

### Handling Map Template Events

- [var mapDelegate: (any CPMapTemplateDelegate)?](/documentation/carplay/cpmaptemplate/mapdelegate)
- [CPMapTemplateDelegate](/documentation/carplay/cpmaptemplatedelegate)

#### Setting the Display Style

- [func mapTemplate(CPMapTemplate, displayStyleFor: CPManeuver) -> CPManeuverDisplayStyle](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:displaystylefor:))
- [CPManeuverDisplayStyle](/documentation/carplay/cpmaneuverdisplaystyle)

##### Display Styles

- [static var leadingSymbol: CPManeuverDisplayStyle](/documentation/carplay/cpmaneuverdisplaystyle/leadingsymbol)
- [static var trailingSymbol: CPManeuverDisplayStyle](/documentation/carplay/cpmaneuverdisplaystyle/trailingsymbol)
- [static var instructionOnly: CPManeuverDisplayStyle](/documentation/carplay/cpmaneuverdisplaystyle/instructiononly)
- [static var symbolOnly: CPManeuverDisplayStyle](/documentation/carplay/cpmaneuverdisplaystyle/symbolonly)

##### Initializers

- [init(rawValue: Int)](/documentation/carplay/cpmaneuverdisplaystyle/init(rawvalue:))

#### Handling Navigation Events

- [func mapTemplate(CPMapTemplate, selectedPreviewFor: CPTrip, using: CPRouteChoice)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:selectedpreviewfor:using:))
- [func mapTemplate(CPMapTemplate, startedTrip: CPTrip, using: CPRouteChoice)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:startedtrip:using:))
- [func mapTemplateDidCancelNavigation(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatedidcancelnavigation(_:))
- [func mapTemplateShouldProvideNavigationMetadata(CPMapTemplate) -> Bool](/documentation/carplay/cpmaptemplatedelegate/maptemplateshouldprovidenavigationmetadata(_:))

#### Displaying Notifications

- [func mapTemplate(CPMapTemplate, shouldShowNotificationFor: CPManeuver) -> Bool](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:shouldshownotificationfor:)-4mnm1)
- [func mapTemplate(CPMapTemplate, shouldUpdateNotificationFor: CPManeuver, with: CPTravelEstimates) -> Bool](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:shouldupdatenotificationfor:with:))
- [func mapTemplate(CPMapTemplate, shouldShowNotificationFor: CPNavigationAlert) -> Bool](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:shouldshownotificationfor:)-5lu8a)

#### Handling Navigation Alerts

- [func mapTemplate(CPMapTemplate, willShow: CPNavigationAlert)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:willshow:))
- [func mapTemplate(CPMapTemplate, didShow: CPNavigationAlert)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:didshow:))
- [func mapTemplate(CPMapTemplate, willDismiss: CPNavigationAlert, dismissalContext: CPNavigationAlert.DismissalContext)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:willdismiss:dismissalcontext:))
- [func mapTemplate(CPMapTemplate, didDismiss: CPNavigationAlert, dismissalContext: CPNavigationAlert.DismissalContext)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:diddismiss:dismissalcontext:))
- [CPNavigationAlert.DismissalContext](/documentation/carplay/cpnavigationalert/dismissalcontext)

##### Dismissal Reasons

- [case timeout](/documentation/carplay/cpnavigationalert/dismissalcontext/timeout)
- [case systemDismissed](/documentation/carplay/cpnavigationalert/dismissalcontext/systemdismissed)
- [case userDismissed](/documentation/carplay/cpnavigationalert/dismissalcontext/userdismissed)

##### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpnavigationalert/dismissalcontext/init(rawvalue:))

#### Panning the Map

- [func mapTemplateDidShowPanningInterface(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatedidshowpanninginterface(_:))
- [func mapTemplateWillDismissPanningInterface(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatewilldismisspanninginterface(_:))
- [func mapTemplateDidDismissPanningInterface(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatediddismisspanninginterface(_:))
- [func mapTemplateDidBeginPanGesture(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatedidbeginpangesture(_:))
- [func mapTemplate(CPMapTemplate, panBeganWith: CPMapTemplate.PanDirection)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:panbeganwith:))
- [func mapTemplate(CPMapTemplate, panWith: CPMapTemplate.PanDirection)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:panwith:))
- [func mapTemplate(CPMapTemplate, panEndedWith: CPMapTemplate.PanDirection)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:panendedwith:))
- [CPMapTemplate.PanDirection](/documentation/carplay/cpmaptemplate/pandirection)

##### Pan Directions

- [static var down: CPMapTemplate.PanDirection](/documentation/carplay/cpmaptemplate/pandirection/down)
- [static var left: CPMapTemplate.PanDirection](/documentation/carplay/cpmaptemplate/pandirection/left)
- [static var right: CPMapTemplate.PanDirection](/documentation/carplay/cpmaptemplate/pandirection/right)
- [static var up: CPMapTemplate.PanDirection](/documentation/carplay/cpmaptemplate/pandirection/up)

##### Initializers

- [init(rawValue: Int)](/documentation/carplay/cpmaptemplate/pandirection/init(rawvalue:))
- [func mapTemplate(CPMapTemplate, didEndPanGestureWithVelocity: CGPoint)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:didendpangesturewithvelocity:))
- [func mapTemplate(CPMapTemplate, didUpdatePanGestureWithTranslation: CGPoint, velocity: CGPoint)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:didupdatepangesturewithtranslation:velocity:))

#### Instance Methods

- [func mapTemplate(CPMapTemplate, didEndZoomGestureWithVelocity: CGFloat)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:didendzoomgesturewithvelocity:))
- [func mapTemplate(CPMapTemplate, didRotateWithCenter: CGPoint, rotation: CGFloat, velocity: CGFloat)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:didrotatewithcenter:rotation:velocity:))
- [func mapTemplate(CPMapTemplate, didUpdateZoomGestureWithCenter: CGPoint, scale: CGFloat, velocity: CGFloat)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:didupdatezoomgesturewithcenter:scale:velocity:))
- [func mapTemplate(CPMapTemplate, pitchEndedWithCenter: CGPoint)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:pitchendedwithcenter:))
- [func mapTemplate(CPMapTemplate, pitchWithCenter: CGPoint)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:pitchwithcenter:))
- [func mapTemplate(CPMapTemplate, rotationDidEndWithVelocity: CGFloat)](/documentation/carplay/cpmaptemplatedelegate/maptemplate(_:rotationdidendwithvelocity:))
- [func mapTemplateDidBeginPitchGesture(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatedidbeginpitchgesture(_:))
- [func mapTemplateDidBeginRotationGesture(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatedidbeginrotationgesture(_:))
- [func mapTemplateDidBeginZoomGesture(CPMapTemplate)](/documentation/carplay/cpmaptemplatedelegate/maptemplatedidbeginzoomgesture(_:))

### Managing Map Buttons

- [var mapButtons: [CPMapButton]](/documentation/carplay/cpmaptemplate/mapbuttons)
- [CPMapButton](/documentation/carplay/cpmapbutton)

#### Creating a Map Button

- [init(handler: ((CPMapButton) -> Void)?)](/documentation/carplay/cpmapbutton/init(handler:))

#### Providing Button Images

- [var image: UIImage?](/documentation/carplay/cpmapbutton/image)
- [var focusedImage: UIImage?](/documentation/carplay/cpmapbutton/focusedimage)

#### Controlling the Button

- [var isEnabled: Bool](/documentation/carplay/cpmapbutton/isenabled)
- [var isHidden: Bool](/documentation/carplay/cpmapbutton/ishidden)

### Displaying Trip Previews

- [func showTripPreviews([CPTrip], textConfiguration: CPTripPreviewTextConfiguration?)](/documentation/carplay/cpmaptemplate/showtrippreviews(_:textconfiguration:))
- [func showTripPreviews([CPTrip], selectedTrip: CPTrip?, textConfiguration: CPTripPreviewTextConfiguration?)](/documentation/carplay/cpmaptemplate/showtrippreviews(_:selectedtrip:textconfiguration:))
- [func hideTripPreviews()](/documentation/carplay/cpmaptemplate/hidetrippreviews())
- [func showRouteChoicesPreview(for: CPTrip, textConfiguration: CPTripPreviewTextConfiguration?)](/documentation/carplay/cpmaptemplate/showroutechoicespreview(for:textconfiguration:))
- [CPTripPreviewTextConfiguration](/documentation/carplay/cptrippreviewtextconfiguration)

#### Creating a Text Configuration Object

- [init(startButtonTitle: String?, additionalRoutesButtonTitle: String?, overviewButtonTitle: String?)](/documentation/carplay/cptrippreviewtextconfiguration/init(startbuttontitle:additionalroutesbuttontitle:overviewbuttontitle:))

#### Setting Button Titles

- [var startButtonTitle: String?](/documentation/carplay/cptrippreviewtextconfiguration/startbuttontitle)
- [var additionalRoutesButtonTitle: String?](/documentation/carplay/cptrippreviewtextconfiguration/additionalroutesbuttontitle)
- [var overviewButtonTitle: String?](/documentation/carplay/cptrippreviewtextconfiguration/overviewbuttontitle)

### Navigating a Trip

- [func startNavigationSession(for: CPTrip) -> CPNavigationSession](/documentation/carplay/cpmaptemplate/startnavigationsession(for:))
- [CPNavigationSession](/documentation/carplay/cpnavigationsession)

#### Getting the Trip

- [var trip: CPTrip](/documentation/carplay/cpnavigationsession/trip)
- [CPTrip](/documentation/carplay/cptrip)

##### Creating a Trip

- [init(origin: MKMapItem, destination: MKMapItem, routeChoices: [CPRouteChoice])](/documentation/carplay/cptrip/init(origin:destination:routechoices:))
- [CPRouteChoice](/documentation/carplay/cproutechoice)

###### Creating a Route Choice

- [init(summaryVariants: [String], additionalInformationVariants: [String], selectionSummaryVariants: [String])](/documentation/carplay/cproutechoice/init(summaryvariants:additionalinformationvariants:selectionsummaryvariants:))

###### Getting Variants

- [var summaryVariants: [String]](/documentation/carplay/cproutechoice/summaryvariants)
- [var additionalInformationVariants: [String]?](/documentation/carplay/cproutechoice/additionalinformationvariants)
- [var selectionSummaryVariants: [String]?](/documentation/carplay/cproutechoice/selectionsummaryvariants)

###### Providing Additional Information

- [var userInfo: Any?](/documentation/carplay/cproutechoice/userinfo)

##### Getting the Trip’s Origin and Destination

- [var origin: MKMapItem](/documentation/carplay/cptrip/origin)
- [var destination: MKMapItem](/documentation/carplay/cptrip/destination)

##### Getting Route Choices

- [var routeChoices: [CPRouteChoice]](/documentation/carplay/cptrip/routechoices)
- [var destinationNameVariants: [String]?](/documentation/carplay/cptrip/destinationnamevariants)

##### Providing Additional Information

- [var userInfo: Any?](/documentation/carplay/cptrip/userinfo)

#### Managing Trip Navigation

- [func cancelTrip()](/documentation/carplay/cpnavigationsession/canceltrip())
- [func finishTrip()](/documentation/carplay/cpnavigationsession/finishtrip())
- [func pauseTrip(for: CPNavigationSession.PauseReason, description: String?)](/documentation/carplay/cpnavigationsession/pausetrip(for:description:))
- [func pauseTrip(for: CPNavigationSession.PauseReason, description: String?, turnCardColor: UIColor?)](/documentation/carplay/cpnavigationsession/pausetrip(for:description:turncardcolor:))
- [CPNavigationSession.PauseReason](/documentation/carplay/cpnavigationsession/pausereason)

##### Reasons

- [case arrived](/documentation/carplay/cpnavigationsession/pausereason/arrived)
- [case loading](/documentation/carplay/cpnavigationsession/pausereason/loading)
- [case locating](/documentation/carplay/cpnavigationsession/pausereason/locating)
- [case proceedToRoute](/documentation/carplay/cpnavigationsession/pausereason/proceedtoroute)
- [case rerouting](/documentation/carplay/cpnavigationsession/pausereason/rerouting)

##### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpnavigationsession/pausereason/init(rawvalue:))
- [func resumeTrip(updatedRouteInformation: CPRouteInformation)](/documentation/carplay/cpnavigationsession/resumetrip(updatedrouteinformation:))

#### Managing Upcoming Maneuvers

- [var upcomingManeuvers: [CPManeuver]](/documentation/carplay/cpnavigationsession/upcomingmaneuvers)
- [var maneuverState: CPManeuverState](/documentation/carplay/cpnavigationsession/maneuverstate)
- [var currentRoadNameVariants: [String]](/documentation/carplay/cpnavigationsession/currentroadnamevariants)
- [var currentLaneGuidance: CPLaneGuidance?](/documentation/carplay/cpnavigationsession/currentlaneguidance)
- [func add([CPManeuver])](/documentation/carplay/cpnavigationsession/add(_:)-17l62)
- [func add([CPLaneGuidance])](/documentation/carplay/cpnavigationsession/add(_:)-93qpu)
- [CPManeuver](/documentation/carplay/cpmaneuver)

##### Providing instructions

- [var dashboardInstructionVariants: [String]](/documentation/carplay/cpmaneuver/dashboardinstructionvariants)
- [var notificationInstructionVariants: [String]](/documentation/carplay/cpmaneuver/notificationinstructionvariants)

##### Providing attributed instructions

- [var attributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/attributedinstructionvariants)
- [var dashboardAttributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/dashboardattributedinstructionvariants)
- [var notificationAttributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/notificationattributedinstructionvariants)

##### Providing travel estimates

- [var initialTravelEstimates: CPTravelEstimates?](/documentation/carplay/cpmaneuver/initialtravelestimates)

##### Providing symbol images

- [var symbolImage: UIImage?](/documentation/carplay/cpmaneuver/symbolimage)
- [var dashboardSymbolImage: UIImage?](/documentation/carplay/cpmaneuver/dashboardsymbolimage)
- [var notificationSymbolImage: UIImage?](/documentation/carplay/cpmaneuver/notificationsymbolimage)
- [var symbolSet: CPImageSet?](/documentation/carplay/cpmaneuver/symbolset)

##### Providing junction images

- [var junctionImage: UIImage?](/documentation/carplay/cpmaneuver/junctionimage)
- [var dashboardJunctionImage: UIImage?](/documentation/carplay/cpmaneuver/dashboardjunctionimage)

##### Providing junction information

- [var junctionType: CPJunctionType](/documentation/carplay/cpmaneuver/junctiontype)
- [var junctionExitAngle: Measurement<UnitAngle>?](/documentation/carplay/cpmaneuver/junctionexitangle)
- [var junctionElementAngles: Set<Measurement<UnitAngle>>?](/documentation/carplay/cpmaneuver/junctionelementangles)

##### Providing maneuver information

- [var maneuverType: CPManeuverType](/documentation/carplay/cpmaneuver/maneuvertype)
- [var roadFollowingManeuverVariants: [String]?](/documentation/carplay/cpmaneuver/roadfollowingmaneuvervariants)
- [var linkedLaneGuidance: CPLaneGuidance](/documentation/carplay/cpmaneuver/linkedlaneguidance)
- [var highwayExitLabel: String](/documentation/carplay/cpmaneuver/highwayexitlabel)
- [var trafficSide: CPTrafficSide](/documentation/carplay/cpmaneuver/trafficside)

##### Providing additional information

- [var userInfo: Any?](/documentation/carplay/cpmaneuver/userinfo)

##### Instance properties

- [var cardBackgroundColor: UIColor?](/documentation/carplay/cpmaneuver/cardbackgroundcolor)

##### Instance Properties

- [var instructionVariants: [String]](/documentation/carplay/cpmaneuver/instructionvariants)

#### Updating Travel Estimates

- [func updateEstimates(CPTravelEstimates, for: CPManeuver)](/documentation/carplay/cpnavigationsession/updateestimates(_:for:))
- [CPTravelEstimates](/documentation/carplay/cptravelestimates)

##### Getting the trip

- [CPTrip](/documentation/carplay/cptrip)

###### Creating a Trip

- [init(origin: MKMapItem, destination: MKMapItem, routeChoices: [CPRouteChoice])](/documentation/carplay/cptrip/init(origin:destination:routechoices:))
- [CPRouteChoice](/documentation/carplay/cproutechoice)

###### Creating a Route Choice

- [init(summaryVariants: [String], additionalInformationVariants: [String], selectionSummaryVariants: [String])](/documentation/carplay/cproutechoice/init(summaryvariants:additionalinformationvariants:selectionsummaryvariants:))

###### Getting Variants

- [var summaryVariants: [String]](/documentation/carplay/cproutechoice/summaryvariants)
- [var additionalInformationVariants: [String]?](/documentation/carplay/cproutechoice/additionalinformationvariants)
- [var selectionSummaryVariants: [String]?](/documentation/carplay/cproutechoice/selectionsummaryvariants)

###### Providing Additional Information

- [var userInfo: Any?](/documentation/carplay/cproutechoice/userinfo)

###### Getting the Trip’s Origin and Destination

- [var origin: MKMapItem](/documentation/carplay/cptrip/origin)
- [var destination: MKMapItem](/documentation/carplay/cptrip/destination)

###### Getting Route Choices

- [var routeChoices: [CPRouteChoice]](/documentation/carplay/cptrip/routechoices)
- [var destinationNameVariants: [String]?](/documentation/carplay/cptrip/destinationnamevariants)

###### Providing Additional Information

- [var userInfo: Any?](/documentation/carplay/cptrip/userinfo)

##### Managing upcoming maneuvers

- [func add([CPManeuver])](/documentation/carplay/cpnavigationsession/add(_:)-17l62)
- [func add([CPLaneGuidance])](/documentation/carplay/cpnavigationsession/add(_:)-93qpu)
- [CPManeuver](/documentation/carplay/cpmaneuver)

###### Providing instructions

- [var dashboardInstructionVariants: [String]](/documentation/carplay/cpmaneuver/dashboardinstructionvariants)
- [var notificationInstructionVariants: [String]](/documentation/carplay/cpmaneuver/notificationinstructionvariants)

###### Providing attributed instructions

- [var attributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/attributedinstructionvariants)
- [var dashboardAttributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/dashboardattributedinstructionvariants)
- [var notificationAttributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/notificationattributedinstructionvariants)

###### Providing travel estimates

- [var initialTravelEstimates: CPTravelEstimates?](/documentation/carplay/cpmaneuver/initialtravelestimates)

###### Providing symbol images

- [var symbolImage: UIImage?](/documentation/carplay/cpmaneuver/symbolimage)
- [var dashboardSymbolImage: UIImage?](/documentation/carplay/cpmaneuver/dashboardsymbolimage)
- [var notificationSymbolImage: UIImage?](/documentation/carplay/cpmaneuver/notificationsymbolimage)
- [var symbolSet: CPImageSet?](/documentation/carplay/cpmaneuver/symbolset)

###### Providing junction images

- [var junctionImage: UIImage?](/documentation/carplay/cpmaneuver/junctionimage)
- [var dashboardJunctionImage: UIImage?](/documentation/carplay/cpmaneuver/dashboardjunctionimage)

###### Providing junction information

- [var junctionType: CPJunctionType](/documentation/carplay/cpmaneuver/junctiontype)
- [var junctionExitAngle: Measurement<UnitAngle>?](/documentation/carplay/cpmaneuver/junctionexitangle)
- [var junctionElementAngles: Set<Measurement<UnitAngle>>?](/documentation/carplay/cpmaneuver/junctionelementangles)

###### Providing maneuver information

- [var maneuverType: CPManeuverType](/documentation/carplay/cpmaneuver/maneuvertype)
- [var roadFollowingManeuverVariants: [String]?](/documentation/carplay/cpmaneuver/roadfollowingmaneuvervariants)
- [var linkedLaneGuidance: CPLaneGuidance](/documentation/carplay/cpmaneuver/linkedlaneguidance)
- [var highwayExitLabel: String](/documentation/carplay/cpmaneuver/highwayexitlabel)
- [var trafficSide: CPTrafficSide](/documentation/carplay/cpmaneuver/trafficside)

###### Providing additional information

- [var userInfo: Any?](/documentation/carplay/cpmaneuver/userinfo)

###### Instance properties

- [var cardBackgroundColor: UIColor?](/documentation/carplay/cpmaneuver/cardbackgroundcolor)

###### Instance Properties

- [var instructionVariants: [String]](/documentation/carplay/cpmaneuver/instructionvariants)

##### Creating a Travel Estimates Object

- [init(distanceRemaining: Measurement<UnitLength>, timeRemaining: TimeInterval)](/documentation/carplay/cptravelestimates/init(distanceremaining:timeremaining:))
- [init(distanceRemaining: Measurement<UnitLength>, distanceRemainingToDisplay: Measurement<UnitLength>, timeRemaining: TimeInterval)](/documentation/carplay/cptravelestimates/init(distanceremaining:distanceremainingtodisplay:timeremaining:))

##### Updating travel estimates

- [func updateEstimates(CPTravelEstimates, for: CPManeuver)](/documentation/carplay/cpnavigationsession/updateestimates(_:for:))

##### Managing trip navigation

- [func cancelTrip()](/documentation/carplay/cpnavigationsession/canceltrip())
- [func finishTrip()](/documentation/carplay/cpnavigationsession/finishtrip())
- [func pauseTrip(for: CPNavigationSession.PauseReason, description: String?)](/documentation/carplay/cpnavigationsession/pausetrip(for:description:))
- [func pauseTrip(for: CPNavigationSession.PauseReason, description: String?, turnCardColor: UIColor?)](/documentation/carplay/cpnavigationsession/pausetrip(for:description:turncardcolor:))
- [func resumeTrip(updatedRouteInformation: CPRouteInformation)](/documentation/carplay/cpnavigationsession/resumetrip(updatedrouteinformation:))
- [CPNavigationSession.PauseReason](/documentation/carplay/cpnavigationsession/pausereason)

###### Reasons

- [case arrived](/documentation/carplay/cpnavigationsession/pausereason/arrived)
- [case loading](/documentation/carplay/cpnavigationsession/pausereason/loading)
- [case locating](/documentation/carplay/cpnavigationsession/pausereason/locating)
- [case proceedToRoute](/documentation/carplay/cpnavigationsession/pausereason/proceedtoroute)
- [case rerouting](/documentation/carplay/cpnavigationsession/pausereason/rerouting)

###### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpnavigationsession/pausereason/init(rawvalue:))

##### Getting Travel Estimates

- [var distanceRemaining: Measurement<UnitLength>](/documentation/carplay/cptravelestimates/distanceremaining)
- [var distanceRemainingToDisplay: Measurement<UnitLength>](/documentation/carplay/cptravelestimates/distanceremainingtodisplay)
- [var timeRemaining: TimeInterval](/documentation/carplay/cptravelestimates/timeremaining)

### Providing Trip Estimates

- [func updateEstimates(CPTravelEstimates, for: CPTrip)](/documentation/carplay/cpmaptemplate/updateestimates(_:for:))
- [func update(CPTravelEstimates, for: CPTrip, with: CPTimeRemainingColor)](/documentation/carplay/cpmaptemplate/update(_:for:with:))
- [CPTimeRemainingColor](/documentation/carplay/cptimeremainingcolor)

#### Colors

- [case `default`](/documentation/carplay/cptimeremainingcolor/default)
- [case green](/documentation/carplay/cptimeremainingcolor/green)
- [case orange](/documentation/carplay/cptimeremainingcolor/orange)
- [case red](/documentation/carplay/cptimeremainingcolor/red)

#### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cptimeremainingcolor/init(rawvalue:))
- [var tripEstimateStyle: CPTripEstimateStyle](/documentation/carplay/cpmaptemplate/tripestimatestyle)
- [CPTripEstimateStyle](/documentation/carplay/cptripestimatestyle)

#### Styles

- [case light](/documentation/carplay/cptripestimatestyle/light)
- [case dark](/documentation/carplay/cptripestimatestyle/dark)

#### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cptripestimatestyle/init(rawvalue:))

### Displaying a Navigation Alert

- [func present(navigationAlert: CPNavigationAlert, animated: Bool)](/documentation/carplay/cpmaptemplate/present(navigationalert:animated:))
- [func dismissNavigationAlert(animated: Bool, completion: (Bool) -> Void)](/documentation/carplay/cpmaptemplate/dismissnavigationalert(animated:completion:))
- [var currentNavigationAlert: CPNavigationAlert?](/documentation/carplay/cpmaptemplate/currentnavigationalert)
- [CPNavigationAlert](/documentation/carplay/cpnavigationalert)

#### Creating a Navigation Alert

- [init(titleVariants: [String], subtitleVariants: [String]?, image: UIImage?, primaryAction: CPAlertAction, secondaryAction: CPAlertAction?, duration: TimeInterval)](/documentation/carplay/cpnavigationalert/init(titlevariants:subtitlevariants:image:primaryaction:secondaryaction:duration:))
- [init(titleVariants: [String], subtitleVariants: [String]?, imageSet: CPImageSet?, primaryAction: CPAlertAction, secondaryAction: CPAlertAction?, duration: TimeInterval)](/documentation/carplay/cpnavigationalert/init(titlevariants:subtitlevariants:imageset:primaryaction:secondaryaction:duration:))

#### Getting Titles

- [var titleVariants: [String]](/documentation/carplay/cpnavigationalert/titlevariants)
- [var subtitleVariants: [String]](/documentation/carplay/cpnavigationalert/subtitlevariants)
- [func updateTitleVariants([String], subtitleVariants: [String])](/documentation/carplay/cpnavigationalert/updatetitlevariants(_:subtitlevariants:))

#### Getting the Alert Image

- [var image: UIImage?](/documentation/carplay/cpnavigationalert/image)
- [var imageSet: CPImageSet?](/documentation/carplay/cpnavigationalert/imageset)

#### Getting the Actions

- [var primaryAction: CPAlertAction](/documentation/carplay/cpnavigationalert/primaryaction)
- [var secondaryAction: CPAlertAction?](/documentation/carplay/cpnavigationalert/secondaryaction)

#### Getting the Alert Duration

- [var duration: TimeInterval](/documentation/carplay/cpnavigationalert/duration)
- [let CPNavigationAlertMinimumDuration: TimeInterval](/documentation/carplay/cpnavigationalertminimumduration)

#### Enumerations

- [CPNavigationAlert.DismissalContext](/documentation/carplay/cpnavigationalert/dismissalcontext)

##### Dismissal Reasons

- [case timeout](/documentation/carplay/cpnavigationalert/dismissalcontext/timeout)
- [case systemDismissed](/documentation/carplay/cpnavigationalert/dismissalcontext/systemdismissed)
- [case userDismissed](/documentation/carplay/cpnavigationalert/dismissalcontext/userdismissed)

##### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpnavigationalert/dismissalcontext/init(rawvalue:))

### Panning the Map

- [func showPanningInterface(animated: Bool)](/documentation/carplay/cpmaptemplate/showpanninginterface(animated:))
- [func dismissPanningInterface(animated: Bool)](/documentation/carplay/cpmaptemplate/dismisspanninginterface(animated:))
- [var isPanningInterfaceVisible: Bool](/documentation/carplay/cpmaptemplate/ispanninginterfacevisible)
- [CPSearchTemplate](/documentation/carplay/cpsearchtemplate)

### Providing a Search Template Delegate

- [var delegate: (any CPSearchTemplateDelegate)?](/documentation/carplay/cpsearchtemplate/delegate)
- [CPSearchTemplateDelegate](/documentation/carplay/cpsearchtemplatedelegate)

#### Updating Search Text

- [func searchTemplate(CPSearchTemplate, updatedSearchText: String, completionHandler: ([CPListItem]) -> Void)](/documentation/carplay/cpsearchtemplatedelegate/searchtemplate(_:updatedsearchtext:completionhandler:))

#### Selecting a Search Result Item

- [func searchTemplate(CPSearchTemplate, selectedResult: CPListItem, completionHandler: () -> Void)](/documentation/carplay/cpsearchtemplatedelegate/searchtemplate(_:selectedresult:completionhandler:))

#### Pressing the Search Button

- [func searchTemplateSearchButtonPressed(CPSearchTemplate)](/documentation/carplay/cpsearchtemplatedelegate/searchtemplatesearchbuttonpressed(_:))
- [CPVoiceControlTemplate](/documentation/carplay/cpvoicecontroltemplate)

### Creating a Voice Control Template

- [init(voiceControlStates: [CPVoiceControlState])](/documentation/carplay/cpvoicecontroltemplate/init(voicecontrolstates:))
- [CPVoiceControlState](/documentation/carplay/cpvoicecontrolstate)

#### Creating a Voice Control State

- [init(identifier: String, titleVariants: [String]?, image: UIImage?, repeats: Bool)](/documentation/carplay/cpvoicecontrolstate/init(identifier:titlevariants:image:repeats:))

#### Getting State Information

- [var identifier: String](/documentation/carplay/cpvoicecontrolstate/identifier)
- [var titleVariants: [String]?](/documentation/carplay/cpvoicecontrolstate/titlevariants)
- [var image: UIImage?](/documentation/carplay/cpvoicecontrolstate/image)
- [var repeats: Bool](/documentation/carplay/cpvoicecontrolstate/repeats)

### Activating a State

- [func activateVoiceControlState(withIdentifier: String)](/documentation/carplay/cpvoicecontroltemplate/activatevoicecontrolstate(withidentifier:))
- [var activeStateIdentifier: String?](/documentation/carplay/cpvoicecontroltemplate/activestateidentifier)

### Getting Available States

- [var voiceControlStates: [CPVoiceControlState]](/documentation/carplay/cpvoicecontroltemplate/voicecontrolstates)

## Location and Information

- [CPPointOfInterestTemplate](/documentation/carplay/cppointofinteresttemplate)

### Creating a Point of Interest Template

- [init(title: String, pointsOfInterest: [CPPointOfInterest], selectedIndex: Int)](/documentation/carplay/cppointofinteresttemplate/init(title:pointsofinterest:selectedindex:))
- [CPPointOfInterest](/documentation/carplay/cppointofinterest)

#### Creating a Point of Interest

- [convenience init(location: MKMapItem, title: String, subtitle: String?, summary: String?, detailTitle: String?, detailSubtitle: String?, detailSummary: String?, pinImage: UIImage?)](/documentation/carplay/cppointofinterest/init(location:title:subtitle:summary:detailtitle:detailsubtitle:detailsummary:pinimage:))

#### Managing the Map Annotation

- [var location: MKMapItem](/documentation/carplay/cppointofinterest/location)
- [var pinImage: UIImage?](/documentation/carplay/cppointofinterest/pinimage)

#### Managing the Picker Item’s Data

- [var title: String](/documentation/carplay/cppointofinterest/title)
- [var subtitle: String?](/documentation/carplay/cppointofinterest/subtitle)
- [var summary: String?](/documentation/carplay/cppointofinterest/summary)

#### Managing the Detail Card’s Data

- [var detailTitle: String?](/documentation/carplay/cppointofinterest/detailtitle)
- [var detailSubtitle: String?](/documentation/carplay/cppointofinterest/detailsubtitle)
- [var detailSummary: String?](/documentation/carplay/cppointofinterest/detailsummary)

#### Managing the Detail Card’s Buttons

- [var primaryButton: CPTextButton?](/documentation/carplay/cppointofinterest/primarybutton)
- [var secondaryButton: CPTextButton?](/documentation/carplay/cppointofinterest/secondarybutton)

#### Attaching Additional Context

- [var userInfo: Any?](/documentation/carplay/cppointofinterest/userinfo)

#### Initializers

- [init(location: MKMapItem, title: String, subtitle: String?, summary: String?, detailTitle: String?, detailSubtitle: String?, detailSummary: String?, pinImage: UIImage?, selectedPinImage: UIImage?)](/documentation/carplay/cppointofinterest/init(location:title:subtitle:summary:detailtitle:detailsubtitle:detailsummary:pinimage:selectedpinimage:))

#### Instance Properties

- [var selectedPinImage: UIImage?](/documentation/carplay/cppointofinterest/selectedpinimage)

#### Type Properties

- [class var pinImageSize: CGSize](/documentation/carplay/cppointofinterest/pinimagesize)
- [class var selectedPinImageSize: CGSize](/documentation/carplay/cppointofinterest/selectedpinimagesize)

### Handling Template Events

- [var pointOfInterestDelegate: (any CPPointOfInterestTemplateDelegate)?](/documentation/carplay/cppointofinteresttemplate/pointofinterestdelegate)
- [CPPointOfInterestTemplateDelegate](/documentation/carplay/cppointofinteresttemplatedelegate)

#### Responding to Map Region Changes

- [func pointOfInterestTemplate(CPPointOfInterestTemplate, didChangeMapRegion: MKCoordinateRegion)](/documentation/carplay/cppointofinteresttemplatedelegate/pointofinteresttemplate(_:didchangemapregion:))

#### Responding to Point of Interest Selection

- [func pointOfInterestTemplate(CPPointOfInterestTemplate, didSelectPointOfInterest: CPPointOfInterest)](/documentation/carplay/cppointofinteresttemplatedelegate/pointofinteresttemplate(_:didselectpointofinterest:))

### Managing the Picker’s Title

- [var title: String](/documentation/carplay/cppointofinteresttemplate/title)

### Managing the Points of Interest

- [var pointsOfInterest: [CPPointOfInterest]](/documentation/carplay/cppointofinteresttemplate/pointsofinterest)
- [func setPointsOfInterest([CPPointOfInterest], selectedIndex: Int)](/documentation/carplay/cppointofinteresttemplate/setpointsofinterest(_:selectedindex:))
- [var selectedIndex: Int](/documentation/carplay/cppointofinteresttemplate/selectedindex)
- [CPInformationTemplate](/documentation/carplay/cpinformationtemplate)

### Creating an Information Template

- [init(title: String, layout: CPInformationTemplateLayout, items: [CPInformationItem], actions: [CPTextButton])](/documentation/carplay/cpinformationtemplate/init(title:layout:items:actions:))

### Accessing the Layout

- [var layout: CPInformationTemplateLayout](/documentation/carplay/cpinformationtemplate/layout)
- [CPInformationTemplateLayout](/documentation/carplay/cpinformationtemplatelayout)

#### Template Layout Styles

- [case leading](/documentation/carplay/cpinformationtemplatelayout/leading)
- [case twoColumn](/documentation/carplay/cpinformationtemplatelayout/twocolumn)

#### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cpinformationtemplatelayout/init(rawvalue:))

### Managing the Title

- [var title: String](/documentation/carplay/cpinformationtemplate/title)

### Managing the Items

- [var items: [CPInformationItem]](/documentation/carplay/cpinformationtemplate/items)
- [CPInformationItem](/documentation/carplay/cpinformationitem)

#### Creating an Information Item

- [init(title: String?, detail: String?)](/documentation/carplay/cpinformationitem/init(title:detail:))

#### Accessing the Item’s Attributes

- [var title: String?](/documentation/carplay/cpinformationitem/title)
- [var detail: String?](/documentation/carplay/cpinformationitem/detail)
- [CPInformationRatingItem](/documentation/carplay/cpinformationratingitem)

#### Creating a Rating Item

- [init(rating: NSNumber?, maximumRating: NSNumber?, title: String?, detail: String?)](/documentation/carplay/cpinformationratingitem/init(rating:maximumrating:title:detail:))

#### Accessing the Item’s Attributes

- [var rating: NSNumber?](/documentation/carplay/cpinformationratingitem/rating)
- [var maximumRating: NSNumber?](/documentation/carplay/cpinformationratingitem/maximumrating)

### Managing the Actions

- [var actions: [CPTextButton]](/documentation/carplay/cpinformationtemplate/actions)
- [CPTextButton](/documentation/carplay/cptextbutton)

### Creating a Text Button

- [init(title: String, textStyle: CPTextButtonStyle, handler: ((CPTextButton) -> Void)?)](/documentation/carplay/cptextbutton/init(title:textstyle:handler:))

### Managing the Title

- [var title: String](/documentation/carplay/cptextbutton/title)

### Managing the Button Style

- [var textStyle: CPTextButtonStyle](/documentation/carplay/cptextbutton/textstyle)
- [CPTextButtonStyle](/documentation/carplay/cptextbuttonstyle)

#### Button Text Styles

- [case normal](/documentation/carplay/cptextbuttonstyle/normal)
- [case confirm](/documentation/carplay/cptextbuttonstyle/confirm)
- [case cancel](/documentation/carplay/cptextbuttonstyle/cancel)

#### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cptextbuttonstyle/init(rawvalue:))
- [Integrating CarPlay with your quick-ordering app](/documentation/carplay/integrating-carplay-with-your-quick-ordering-app)

## Maneuvers

- [CPManeuver](/documentation/carplay/cpmaneuver)

### Providing instructions

- [var dashboardInstructionVariants: [String]](/documentation/carplay/cpmaneuver/dashboardinstructionvariants)
- [var notificationInstructionVariants: [String]](/documentation/carplay/cpmaneuver/notificationinstructionvariants)

### Providing attributed instructions

- [var attributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/attributedinstructionvariants)
- [var dashboardAttributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/dashboardattributedinstructionvariants)
- [var notificationAttributedInstructionVariants: [NSAttributedString]](/documentation/carplay/cpmaneuver/notificationattributedinstructionvariants)

### Providing travel estimates

- [var initialTravelEstimates: CPTravelEstimates?](/documentation/carplay/cpmaneuver/initialtravelestimates)

### Providing symbol images

- [var symbolImage: UIImage?](/documentation/carplay/cpmaneuver/symbolimage)
- [var dashboardSymbolImage: UIImage?](/documentation/carplay/cpmaneuver/dashboardsymbolimage)
- [var notificationSymbolImage: UIImage?](/documentation/carplay/cpmaneuver/notificationsymbolimage)
- [var symbolSet: CPImageSet?](/documentation/carplay/cpmaneuver/symbolset)

### Providing junction images

- [var junctionImage: UIImage?](/documentation/carplay/cpmaneuver/junctionimage)
- [var dashboardJunctionImage: UIImage?](/documentation/carplay/cpmaneuver/dashboardjunctionimage)

### Providing junction information

- [var junctionType: CPJunctionType](/documentation/carplay/cpmaneuver/junctiontype)
- [var junctionExitAngle: Measurement<UnitAngle>?](/documentation/carplay/cpmaneuver/junctionexitangle)
- [var junctionElementAngles: Set<Measurement<UnitAngle>>?](/documentation/carplay/cpmaneuver/junctionelementangles)

### Providing maneuver information

- [var maneuverType: CPManeuverType](/documentation/carplay/cpmaneuver/maneuvertype)
- [var roadFollowingManeuverVariants: [String]?](/documentation/carplay/cpmaneuver/roadfollowingmaneuvervariants)
- [var linkedLaneGuidance: CPLaneGuidance](/documentation/carplay/cpmaneuver/linkedlaneguidance)
- [var highwayExitLabel: String](/documentation/carplay/cpmaneuver/highwayexitlabel)
- [var trafficSide: CPTrafficSide](/documentation/carplay/cpmaneuver/trafficside)

### Providing additional information

- [var userInfo: Any?](/documentation/carplay/cpmaneuver/userinfo)

### Instance properties

- [var cardBackgroundColor: UIColor?](/documentation/carplay/cpmaneuver/cardbackgroundcolor)

### Instance Properties

- [var instructionVariants: [String]](/documentation/carplay/cpmaneuver/instructionvariants)
- [CPManeuverState](/documentation/carplay/cpmaneuverstate)

### Enumeration Cases

- [case prepare](/documentation/carplay/cpmaneuverstate/prepare)
- [case initial](/documentation/carplay/cpmaneuverstate/initial)
- [case execute](/documentation/carplay/cpmaneuverstate/execute)
- [case `continue`](/documentation/carplay/cpmaneuverstate/continue)

### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cpmaneuverstate/init(rawvalue:))
- [CPManeuverType](/documentation/carplay/cpmaneuvertype)

### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpmaneuvertype/init(rawvalue:))

### Maneuver types

- [case arriveAtDestination](/documentation/carplay/cpmaneuvertype/arriveatdestination)
- [case arriveAtDestinationLeft](/documentation/carplay/cpmaneuvertype/arriveatdestinationleft)
- [case arriveAtDestinationRight](/documentation/carplay/cpmaneuvertype/arriveatdestinationright)
- [case arriveEndOfDirections](/documentation/carplay/cpmaneuvertype/arriveendofdirections)
- [case arriveEndOfNavigation](/documentation/carplay/cpmaneuvertype/arriveendofnavigation)
- [case changeFerry](/documentation/carplay/cpmaneuvertype/changeferry)
- [case changeHighway](/documentation/carplay/cpmaneuvertype/changehighway)
- [case changeHighwayLeft](/documentation/carplay/cpmaneuvertype/changehighwayleft)
- [case changeHighwayRight](/documentation/carplay/cpmaneuvertype/changehighwayright)
- [case enterRoundabout](/documentation/carplay/cpmaneuvertype/enterroundabout)
- [case enter_Ferry](/documentation/carplay/cpmaneuvertype/enter_ferry)
- [case exitFerry](/documentation/carplay/cpmaneuvertype/exitferry)
- [case exitRoundabout](/documentation/carplay/cpmaneuvertype/exitroundabout)
- [case followRoad](/documentation/carplay/cpmaneuvertype/followroad)
- [case highwayOffRampLeft](/documentation/carplay/cpmaneuvertype/highwayofframpleft)
- [case highwayOffRampRight](/documentation/carplay/cpmaneuvertype/highwayofframpright)
- [case keepLeft](/documentation/carplay/cpmaneuvertype/keepleft)
- [case keepRight](/documentation/carplay/cpmaneuvertype/keepright)
- [case leftTurn](/documentation/carplay/cpmaneuvertype/leftturn)
- [case leftTurnAtEnd](/documentation/carplay/cpmaneuvertype/leftturnatend)
- [case noTurn](/documentation/carplay/cpmaneuvertype/noturn)
- [case offRamp](/documentation/carplay/cpmaneuvertype/offramp)
- [case onRamp](/documentation/carplay/cpmaneuvertype/onramp)
- [case rightTurn](/documentation/carplay/cpmaneuvertype/rightturn)
- [case rightTurnAtEnd](/documentation/carplay/cpmaneuvertype/rightturnatend)
- [case roundaboutExit1](/documentation/carplay/cpmaneuvertype/roundaboutexit1)
- [case roundaboutExit10](/documentation/carplay/cpmaneuvertype/roundaboutexit10)
- [case roundaboutExit11](/documentation/carplay/cpmaneuvertype/roundaboutexit11)
- [case roundaboutExit12](/documentation/carplay/cpmaneuvertype/roundaboutexit12)
- [case roundaboutExit13](/documentation/carplay/cpmaneuvertype/roundaboutexit13)
- [case roundaboutExit14](/documentation/carplay/cpmaneuvertype/roundaboutexit14)
- [case roundaboutExit15](/documentation/carplay/cpmaneuvertype/roundaboutexit15)
- [case roundaboutExit16](/documentation/carplay/cpmaneuvertype/roundaboutexit16)
- [case roundaboutExit17](/documentation/carplay/cpmaneuvertype/roundaboutexit17)
- [case roundaboutExit18](/documentation/carplay/cpmaneuvertype/roundaboutexit18)
- [case roundaboutExit19](/documentation/carplay/cpmaneuvertype/roundaboutexit19)
- [case roundaboutExit2](/documentation/carplay/cpmaneuvertype/roundaboutexit2)
- [case roundaboutExit3](/documentation/carplay/cpmaneuvertype/roundaboutexit3)
- [case roundaboutExit4](/documentation/carplay/cpmaneuvertype/roundaboutexit4)
- [case roundaboutExit5](/documentation/carplay/cpmaneuvertype/roundaboutexit5)
- [case roundaboutExit6](/documentation/carplay/cpmaneuvertype/roundaboutexit6)
- [case roundaboutExit7](/documentation/carplay/cpmaneuvertype/roundaboutexit7)
- [case roundaboutExit8](/documentation/carplay/cpmaneuvertype/roundaboutexit8)
- [case roundaboutExit9](/documentation/carplay/cpmaneuvertype/roundaboutexit9)
- [case sharpLeftTurn](/documentation/carplay/cpmaneuvertype/sharpleftturn)
- [case sharpRightTurn](/documentation/carplay/cpmaneuvertype/sharprightturn)
- [case slightLeftTurn](/documentation/carplay/cpmaneuvertype/slightleftturn)
- [case slightRightTurn](/documentation/carplay/cpmaneuvertype/slightrightturn)
- [case startRoute](/documentation/carplay/cpmaneuvertype/startroute)
- [case startRouteWithUTurn](/documentation/carplay/cpmaneuvertype/startroutewithuturn)
- [case straightAhead](/documentation/carplay/cpmaneuvertype/straightahead)
- [case uTurn](/documentation/carplay/cpmaneuvertype/uturn)
- [case uTurnAtRoundabout](/documentation/carplay/cpmaneuvertype/uturnatroundabout)
- [case uTurnWhenPossible](/documentation/carplay/cpmaneuvertype/uturnwhenpossible)

## Routes, lanes and junctions

- [CPRouteInformation](/documentation/carplay/cprouteinformation)

### Initializers

- [init(maneuvers: [CPManeuver], laneGuidances: [CPLaneGuidance], currentManeuvers: [CPManeuver], currentLaneGuidance: CPLaneGuidance, trip: CPTravelEstimates, maneuverTravelEstimates: CPTravelEstimates)](/documentation/carplay/cprouteinformation/init(maneuvers:laneguidances:currentmaneuvers:currentlaneguidance:trip:maneuvertravelestimates:))

### Properties

- [var currentLaneGuidance: CPLaneGuidance](/documentation/carplay/cprouteinformation/currentlaneguidance)
- [var currentManeuvers: [CPManeuver]](/documentation/carplay/cprouteinformation/currentmaneuvers)
- [var laneGuidances: [CPLaneGuidance]](/documentation/carplay/cprouteinformation/laneguidances)
- [var maneuverTravelEstimates: CPTravelEstimates](/documentation/carplay/cprouteinformation/maneuvertravelestimates)
- [var maneuvers: [CPManeuver]](/documentation/carplay/cprouteinformation/maneuvers)
- [var tripTravelEstimates: CPTravelEstimates](/documentation/carplay/cprouteinformation/triptravelestimates)
- [CPLane](/documentation/carplay/cplane)

### Properties

- [var primaryAngle: Measurement<UnitAngle>](/documentation/carplay/cplane/primaryangle)
- [var secondaryAngles: [Measurement<UnitAngle>]](/documentation/carplay/cplane/secondaryangles)
- [var status: CPLaneStatus](/documentation/carplay/cplane/status)

### Lane status

- [CPLaneStatus](/documentation/carplay/cplanestatus)

#### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplanestatus/init(rawvalue:))

#### Lane statuses

- [case notGood](/documentation/carplay/cplanestatus/notgood)
- [case good](/documentation/carplay/cplanestatus/good)
- [case preferred](/documentation/carplay/cplanestatus/preferred)

### Initializers

- [init()](/documentation/carplay/cplane/init())
- [init(angles: [Measurement<UnitAngle>])](/documentation/carplay/cplane/init(angles:))
- [init(angles: [Measurement<UnitAngle>], highlightedAngle: Measurement<UnitAngle>, isPreferred: Bool)](/documentation/carplay/cplane/init(angles:highlightedangle:ispreferred:))

### Instance Properties

- [var angles: [Measurement<UnitAngle>]](/documentation/carplay/cplane/angles)
- [var highlightedAngle: Measurement<UnitAngle>?](/documentation/carplay/cplane/highlightedangle)
- [CPLaneGuidance](/documentation/carplay/cplaneguidance)

### Properties

- [var instructionVariants: [String]](/documentation/carplay/cplaneguidance/instructionvariants)
- [var lanes: [CPLane]](/documentation/carplay/cplaneguidance/lanes)
- [CPLaneStatus](/documentation/carplay/cplanestatus)

### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplanestatus/init(rawvalue:))

### Lane statuses

- [case notGood](/documentation/carplay/cplanestatus/notgood)
- [case good](/documentation/carplay/cplanestatus/good)
- [case preferred](/documentation/carplay/cplanestatus/preferred)
- [CPJunctionType](/documentation/carplay/cpjunctiontype)

### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpjunctiontype/init(rawvalue:))

### Junction types

- [case intersection](/documentation/carplay/cpjunctiontype/intersection)
- [case roundabout](/documentation/carplay/cpjunctiontype/roundabout)

## Communication

- [CPContactTemplate](/documentation/carplay/cpcontacttemplate)

### Creating a Contact Template

- [init(contact: CPContact)](/documentation/carplay/cpcontacttemplate/init(contact:))

### Configuring the Contact

- [var contact: CPContact](/documentation/carplay/cpcontacttemplate/contact)
- [CPContact](/documentation/carplay/cpcontact)

#### Creating a Contact

- [init(name: String, image: UIImage)](/documentation/carplay/cpcontact/init(name:image:))

#### Configuring the Contact’s Attributes

- [var image: UIImage](/documentation/carplay/cpcontact/image)
- [var name: String](/documentation/carplay/cpcontact/name)
- [var subtitle: String?](/documentation/carplay/cpcontact/subtitle)
- [var informativeText: String?](/documentation/carplay/cpcontact/informativetext)

#### Managing Interactions with the Contact

- [var actions: [CPButton]?](/documentation/carplay/cpcontact/actions)
- [CPContactCallButton](/documentation/carplay/cpcontactcallbutton)

##### Creating a Contact Call Button

- [init(handler: ((CPButton) -> Void)?)](/documentation/carplay/cpcontactcallbutton/init(handler:))
- [CPContactDirectionsButton](/documentation/carplay/cpcontactdirectionsbutton)

##### Creating a Contact Directions Button

- [init(handler: ((CPButton) -> Void)?)](/documentation/carplay/cpcontactdirectionsbutton/init(handler:))
- [CPContactMessageButton](/documentation/carplay/cpcontactmessagebutton)

##### Creating a Contact Message Button

- [init(phoneOrEmail: String)](/documentation/carplay/cpcontactmessagebutton/init(phoneoremail:))

##### Getting the Contact Information

- [var phoneOrEmail: String](/documentation/carplay/cpcontactmessagebutton/phoneoremail)

## Actions and Alerts

- [CPActionSheetTemplate](/documentation/carplay/cpactionsheettemplate)

### Creating an Action Sheet Template

- [init(title: String?, message: String?, actions: [CPAlertAction])](/documentation/carplay/cpactionsheettemplate/init(title:message:actions:))

### Getting Action Sheet Template Information

- [var title: String?](/documentation/carplay/cpactionsheettemplate/title)
- [var message: String?](/documentation/carplay/cpactionsheettemplate/message)
- [var actions: [CPAlertAction]](/documentation/carplay/cpactionsheettemplate/actions)
- [CPAlertTemplate](/documentation/carplay/cpalerttemplate)

### Creating an Alert Template

- [init(titleVariants: [String], actions: [CPAlertAction])](/documentation/carplay/cpalerttemplate/init(titlevariants:actions:))
- [class var maximumActionCount: Int](/documentation/carplay/cpalerttemplate/maximumactioncount)

### Getting the Alert Information

- [var titleVariants: [String]](/documentation/carplay/cpalerttemplate/titlevariants)
- [var actions: [CPAlertAction]](/documentation/carplay/cpalerttemplate/actions)
- [CPAlertAction](/documentation/carplay/cpalertaction)

### Creating an Alert Action

- [init(title: String, style: CPAlertAction.Style, handler: CPAlertActionHandler)](/documentation/carplay/cpalertaction/init(title:style:handler:))

### Getting the Title

- [var title: String](/documentation/carplay/cpalertaction/title)

### Getting the Action Style

- [var style: CPAlertAction.Style](/documentation/carplay/cpalertaction/style-swift.property)
- [CPAlertAction.Style](/documentation/carplay/cpalertaction/style-swift.enum)

#### Styles

- [case `default`](/documentation/carplay/cpalertaction/style-swift.enum/default)
- [case cancel](/documentation/carplay/cpalertaction/style-swift.enum/cancel)
- [case destructive](/documentation/carplay/cpalertaction/style-swift.enum/destructive)

#### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpalertaction/style-swift.enum/init(rawvalue:))

### Getting the Action Handler

- [var handler: CPAlertActionHandler](/documentation/carplay/cpalertaction/handler)
- [CPAlertActionHandler](/documentation/carplay/cpalertactionhandler)

### Initializers

- [init(title: String, color: UIColor, handler: CPAlertActionHandler)](/documentation/carplay/cpalertaction/init(title:color:handler:))

### Instance Properties

- [var color: UIColor?](/documentation/carplay/cpalertaction/color)

## Related Types

- [CPButton](/documentation/carplay/cpbutton)

### Creating a Button

- [init(image: UIImage, handler: ((CPButton) -> Void)?)](/documentation/carplay/cpbutton/init(image:handler:))
- [let CPButtonMaximumImageSize: CGSize](/documentation/carplay/cpbuttonmaximumimagesize)

### Getting the Button’s Image

- [var image: UIImage?](/documentation/carplay/cpbutton/image)

### Configuring the Button’s Attributes

- [var title: String?](/documentation/carplay/cpbutton/title)
- [var isEnabled: Bool](/documentation/carplay/cpbutton/isenabled)
- [CPImageSet](/documentation/carplay/cpimageset)

### Creating an Image Set

- [init(lightContentImage: UIImage, darkContentImage: UIImage)](/documentation/carplay/cpimageset/init(lightcontentimage:darkcontentimage:))

### Getting Content Images

- [var lightContentImage: UIImage](/documentation/carplay/cpimageset/lightcontentimage)
- [var darkContentImage: UIImage](/documentation/carplay/cpimageset/darkcontentimage)
- [let CarPlayErrorDomain: String](/documentation/carplay/carplayerrordomain)

## Deprecated

- [Deprecated Symbols](/documentation/carplay/deprecated-symbols)

### Application Life Cycle

- [CPApplicationDelegate](/documentation/carplay/cpapplicationdelegate)

#### Connecting to the CarPlay Interface

- [func application(UIApplication, didConnectCarInterfaceController: CPInterfaceController, to: CPWindow)](/documentation/carplay/cpapplicationdelegate/application(_:didconnectcarinterfacecontroller:to:))
- [func application(UIApplication, didDisconnectCarInterfaceController: CPInterfaceController, from: CPWindow)](/documentation/carplay/cpapplicationdelegate/application(_:diddisconnectcarinterfacecontroller:from:))

#### Receiving the Selected Maneuver

- [func application(UIApplication, didSelect: CPManeuver)](/documentation/carplay/cpapplicationdelegate/application(_:didselect:)-6ybyy)

#### Handling Navigation Alert Actions

- [func application(UIApplication, didSelect: CPNavigationAlert)](/documentation/carplay/cpapplicationdelegate/application(_:didselect:)-478jb)

## Reference

- [CarPlay Enumerations](/documentation/carplay/carplay-enumerations)

### Enumerations

- [CPInstrumentClusterSetting](/documentation/carplay/cpinstrumentclustersetting)

#### Enumeration Cases

- [case disabled](/documentation/carplay/cpinstrumentclustersetting/disabled)
- [case enabled](/documentation/carplay/cpinstrumentclustersetting/enabled)
- [case unspecified](/documentation/carplay/cpinstrumentclustersetting/unspecified)
- [case userPreference](/documentation/carplay/cpinstrumentclustersetting/userpreference)

#### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpinstrumentclustersetting/init(rawvalue:))
- [CPJunctionType](/documentation/carplay/cpjunctiontype)

#### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpjunctiontype/init(rawvalue:))

#### Junction types

- [case intersection](/documentation/carplay/cpjunctiontype/intersection)
- [case roundabout](/documentation/carplay/cpjunctiontype/roundabout)
- [CPManeuverState](/documentation/carplay/cpmaneuverstate)

#### Enumeration Cases

- [case prepare](/documentation/carplay/cpmaneuverstate/prepare)
- [case initial](/documentation/carplay/cpmaneuverstate/initial)
- [case execute](/documentation/carplay/cpmaneuverstate/execute)
- [case `continue`](/documentation/carplay/cpmaneuverstate/continue)

#### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cpmaneuverstate/init(rawvalue:))
- [CPManeuverType](/documentation/carplay/cpmaneuvertype)

#### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cpmaneuvertype/init(rawvalue:))

#### Maneuver types

- [case arriveAtDestination](/documentation/carplay/cpmaneuvertype/arriveatdestination)
- [case arriveAtDestinationLeft](/documentation/carplay/cpmaneuvertype/arriveatdestinationleft)
- [case arriveAtDestinationRight](/documentation/carplay/cpmaneuvertype/arriveatdestinationright)
- [case arriveEndOfDirections](/documentation/carplay/cpmaneuvertype/arriveendofdirections)
- [case arriveEndOfNavigation](/documentation/carplay/cpmaneuvertype/arriveendofnavigation)
- [case changeFerry](/documentation/carplay/cpmaneuvertype/changeferry)
- [case changeHighway](/documentation/carplay/cpmaneuvertype/changehighway)
- [case changeHighwayLeft](/documentation/carplay/cpmaneuvertype/changehighwayleft)
- [case changeHighwayRight](/documentation/carplay/cpmaneuvertype/changehighwayright)
- [case enterRoundabout](/documentation/carplay/cpmaneuvertype/enterroundabout)
- [case enter_Ferry](/documentation/carplay/cpmaneuvertype/enter_ferry)
- [case exitFerry](/documentation/carplay/cpmaneuvertype/exitferry)
- [case exitRoundabout](/documentation/carplay/cpmaneuvertype/exitroundabout)
- [case followRoad](/documentation/carplay/cpmaneuvertype/followroad)
- [case highwayOffRampLeft](/documentation/carplay/cpmaneuvertype/highwayofframpleft)
- [case highwayOffRampRight](/documentation/carplay/cpmaneuvertype/highwayofframpright)
- [case keepLeft](/documentation/carplay/cpmaneuvertype/keepleft)
- [case keepRight](/documentation/carplay/cpmaneuvertype/keepright)
- [case leftTurn](/documentation/carplay/cpmaneuvertype/leftturn)
- [case leftTurnAtEnd](/documentation/carplay/cpmaneuvertype/leftturnatend)
- [case noTurn](/documentation/carplay/cpmaneuvertype/noturn)
- [case offRamp](/documentation/carplay/cpmaneuvertype/offramp)
- [case onRamp](/documentation/carplay/cpmaneuvertype/onramp)
- [case rightTurn](/documentation/carplay/cpmaneuvertype/rightturn)
- [case rightTurnAtEnd](/documentation/carplay/cpmaneuvertype/rightturnatend)
- [case roundaboutExit1](/documentation/carplay/cpmaneuvertype/roundaboutexit1)
- [case roundaboutExit10](/documentation/carplay/cpmaneuvertype/roundaboutexit10)
- [case roundaboutExit11](/documentation/carplay/cpmaneuvertype/roundaboutexit11)
- [case roundaboutExit12](/documentation/carplay/cpmaneuvertype/roundaboutexit12)
- [case roundaboutExit13](/documentation/carplay/cpmaneuvertype/roundaboutexit13)
- [case roundaboutExit14](/documentation/carplay/cpmaneuvertype/roundaboutexit14)
- [case roundaboutExit15](/documentation/carplay/cpmaneuvertype/roundaboutexit15)
- [case roundaboutExit16](/documentation/carplay/cpmaneuvertype/roundaboutexit16)
- [case roundaboutExit17](/documentation/carplay/cpmaneuvertype/roundaboutexit17)
- [case roundaboutExit18](/documentation/carplay/cpmaneuvertype/roundaboutexit18)
- [case roundaboutExit19](/documentation/carplay/cpmaneuvertype/roundaboutexit19)
- [case roundaboutExit2](/documentation/carplay/cpmaneuvertype/roundaboutexit2)
- [case roundaboutExit3](/documentation/carplay/cpmaneuvertype/roundaboutexit3)
- [case roundaboutExit4](/documentation/carplay/cpmaneuvertype/roundaboutexit4)
- [case roundaboutExit5](/documentation/carplay/cpmaneuvertype/roundaboutexit5)
- [case roundaboutExit6](/documentation/carplay/cpmaneuvertype/roundaboutexit6)
- [case roundaboutExit7](/documentation/carplay/cpmaneuvertype/roundaboutexit7)
- [case roundaboutExit8](/documentation/carplay/cpmaneuvertype/roundaboutexit8)
- [case roundaboutExit9](/documentation/carplay/cpmaneuvertype/roundaboutexit9)
- [case sharpLeftTurn](/documentation/carplay/cpmaneuvertype/sharpleftturn)
- [case sharpRightTurn](/documentation/carplay/cpmaneuvertype/sharprightturn)
- [case slightLeftTurn](/documentation/carplay/cpmaneuvertype/slightleftturn)
- [case slightRightTurn](/documentation/carplay/cpmaneuvertype/slightrightturn)
- [case startRoute](/documentation/carplay/cpmaneuvertype/startroute)
- [case startRouteWithUTurn](/documentation/carplay/cpmaneuvertype/startroutewithuturn)
- [case straightAhead](/documentation/carplay/cpmaneuvertype/straightahead)
- [case uTurn](/documentation/carplay/cpmaneuvertype/uturn)
- [case uTurnAtRoundabout](/documentation/carplay/cpmaneuvertype/uturnatroundabout)
- [case uTurnWhenPossible](/documentation/carplay/cpmaneuvertype/uturnwhenpossible)
- [CPLaneStatus](/documentation/carplay/cplanestatus)

#### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplanestatus/init(rawvalue:))

#### Lane statuses

- [case notGood](/documentation/carplay/cplanestatus/notgood)
- [case good](/documentation/carplay/cplanestatus/good)
- [case preferred](/documentation/carplay/cplanestatus/preferred)
- [CPTrafficSide](/documentation/carplay/cptrafficside)

#### Initializers

- [init?(rawValue: UInt)](/documentation/carplay/cptrafficside/init(rawvalue:))

#### Lane statuses

- [case right](/documentation/carplay/cptrafficside/right)
- [case left](/documentation/carplay/cptrafficside/left)
- [CarPlay Constants](/documentation/carplay/carplay-constants)

### Constants

- [let CPGridTemplateMaximumItems: Int](/documentation/carplay/cpgridtemplatemaximumitems)
- [let CPMaximumListSectionImageSize: CGSize](/documentation/carplay/cpmaximumlistsectionimagesize)

## Classes

- [CPListImageRowItemCardElement](/documentation/carplay/cplistimagerowitemcardelement)

### Initializers

- [init(image: UIImage, showsImageFullHeight: Bool, title: String?, subtitle: String?, tintColor: UIColor?)](/documentation/carplay/cplistimagerowitemcardelement/init(image:showsimagefullheight:title:subtitle:tintcolor:))

### Instance Properties

- [var showsImageFullHeight: Bool](/documentation/carplay/cplistimagerowitemcardelement/showsimagefullheight)
- [var subtitle: String?](/documentation/carplay/cplistimagerowitemcardelement/subtitle)
- [var tintColor: UIColor?](/documentation/carplay/cplistimagerowitemcardelement/tintcolor)
- [var title: String](/documentation/carplay/cplistimagerowitemcardelement/title)

### Type Properties

- [class var maximumFullHeightImageSize: CGSize](/documentation/carplay/cplistimagerowitemcardelement/maximumfullheightimagesize)
- [class var maximumImageSize: CGSize](/documentation/carplay/cplistimagerowitemcardelement/maximumimagesize)
- [CPListImageRowItemCondensedElement](/documentation/carplay/cplistimagerowitemcondensedelement)

### Initializers

- [init(image: UIImage, imageShape: CPListImageRowItemCondensedElement.Shape, title: String, subtitle: String?, accessorySymbolName: String?)](/documentation/carplay/cplistimagerowitemcondensedelement/init(image:imageshape:title:subtitle:accessorysymbolname:))

### Instance Properties

- [var accessorySymbolName: String?](/documentation/carplay/cplistimagerowitemcondensedelement/accessorysymbolname)
- [var imageShape: CPListImageRowItemCondensedElement.Shape](/documentation/carplay/cplistimagerowitemcondensedelement/imageshape)
- [var subtitle: String?](/documentation/carplay/cplistimagerowitemcondensedelement/subtitle)
- [var title: String](/documentation/carplay/cplistimagerowitemcondensedelement/title)

### Enumerations

- [CPListImageRowItemCondensedElement.Shape](/documentation/carplay/cplistimagerowitemcondensedelement/shape)

#### Enumeration Cases

- [case circular](/documentation/carplay/cplistimagerowitemcondensedelement/shape/circular)
- [case roundedRectangle](/documentation/carplay/cplistimagerowitemcondensedelement/shape/roundedrectangle)

#### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplistimagerowitemcondensedelement/shape/init(rawvalue:))
- [CPListImageRowItemElement](/documentation/carplay/cplistimagerowitemelement)

### Instance Properties

- [var image: UIImage](/documentation/carplay/cplistimagerowitemelement/image)
- [var isEnabled: Bool](/documentation/carplay/cplistimagerowitemelement/isenabled)

### Type Properties

- [class var maximumImageSize: CGSize](/documentation/carplay/cplistimagerowitemelement/maximumimagesize)
- [CPListImageRowItemGridElement](/documentation/carplay/cplistimagerowitemgridelement)

### Initializers

- [init(image: UIImage)](/documentation/carplay/cplistimagerowitemgridelement/init(image:))
- [CPListImageRowItemImageGridElement](/documentation/carplay/cplistimagerowitemimagegridelement)

### Initializers

- [init(image: UIImage, imageShape: CPListImageRowItemImageGridElement.Shape, title: String, accessorySymbolName: String?)](/documentation/carplay/cplistimagerowitemimagegridelement/init(image:imageshape:title:accessorysymbolname:))

### Instance Properties

- [var accessorySymbolName: String?](/documentation/carplay/cplistimagerowitemimagegridelement/accessorysymbolname)
- [var imageShape: CPListImageRowItemImageGridElement.Shape](/documentation/carplay/cplistimagerowitemimagegridelement/imageshape)
- [var title: String](/documentation/carplay/cplistimagerowitemimagegridelement/title)

### Enumerations

- [CPListImageRowItemImageGridElement.Shape](/documentation/carplay/cplistimagerowitemimagegridelement/shape)

#### Enumeration Cases

- [case circular](/documentation/carplay/cplistimagerowitemimagegridelement/shape/circular)
- [case roundedRectangle](/documentation/carplay/cplistimagerowitemimagegridelement/shape/roundedrectangle)

#### Initializers

- [init?(rawValue: Int)](/documentation/carplay/cplistimagerowitemimagegridelement/shape/init(rawvalue:))
- [CPListImageRowItemRowElement](/documentation/carplay/cplistimagerowitemrowelement)

### Initializers

- [init(image: UIImage, title: String?, subtitle: String?)](/documentation/carplay/cplistimagerowitemrowelement/init(image:title:subtitle:))

### Instance Properties

- [var subtitle: String?](/documentation/carplay/cplistimagerowitemrowelement/subtitle)
- [var title: String?](/documentation/carplay/cplistimagerowitemrowelement/title)
- [CPMessageGridItemConfiguration](/documentation/carplay/cpmessagegriditemconfiguration)

### Initializers

- [init(conversationIdentifier: String, unread: Bool)](/documentation/carplay/cpmessagegriditemconfiguration/init(conversationidentifier:unread:))

### Instance Properties

- [var conversationIdentifier: String](/documentation/carplay/cpmessagegriditemconfiguration/conversationidentifier)
- [var isUnread: Bool](/documentation/carplay/cpmessagegriditemconfiguration/isunread)
- [CPNowPlayingMode](/documentation/carplay/cpnowplayingmode)

### Type Properties

- [class var `default`: CPNowPlayingMode](/documentation/carplay/cpnowplayingmode/default)
- [CPNowPlayingModeSports](/documentation/carplay/cpnowplayingmodesports)

### Initializers

- [init(leftTeam: CPNowPlayingSportsTeam, rightTeam: CPNowPlayingSportsTeam, eventStatus: CPNowPlayingSportsEventStatus?, backgroundArtwork: UIImage?)](/documentation/carplay/cpnowplayingmodesports/init(leftteam:rightteam:eventstatus:backgroundartwork:))

### Instance Properties

- [var backgroundArtwork: UIImage?](/documentation/carplay/cpnowplayingmodesports/backgroundartwork)
- [var eventStatus: CPNowPlayingSportsEventStatus?](/documentation/carplay/cpnowplayingmodesports/eventstatus)
- [var leftTeam: CPNowPlayingSportsTeam](/documentation/carplay/cpnowplayingmodesports/leftteam)
- [var rightTeam: CPNowPlayingSportsTeam](/documentation/carplay/cpnowplayingmodesports/rightteam)
- [CPNowPlayingSportsClock](/documentation/carplay/cpnowplayingsportsclock)

### Initializers

- [init(elapsedTime: TimeInterval, paused: Bool)](/documentation/carplay/cpnowplayingsportsclock/init(elapsedtime:paused:))
- [init(timeRemaining: TimeInterval, paused: Bool)](/documentation/carplay/cpnowplayingsportsclock/init(timeremaining:paused:))

### Instance Properties

- [var countsUp: Bool](/documentation/carplay/cpnowplayingsportsclock/countsup)
- [var isPaused: Bool](/documentation/carplay/cpnowplayingsportsclock/ispaused)
- [var timeValue: TimeInterval](/documentation/carplay/cpnowplayingsportsclock/timevalue)
- [CPNowPlayingSportsEventStatus](/documentation/carplay/cpnowplayingsportseventstatus)

### Initializers

- [init(eventStatusText: [String]?, eventStatusImage: UIImage?, eventClock: CPNowPlayingSportsClock?)](/documentation/carplay/cpnowplayingsportseventstatus/init(eventstatustext:eventstatusimage:eventclock:))

### Instance Properties

- [var eventClock: CPNowPlayingSportsClock?](/documentation/carplay/cpnowplayingsportseventstatus/eventclock)
- [var eventStatusImage: UIImage?](/documentation/carplay/cpnowplayingsportseventstatus/eventstatusimage)
- [var eventStatusText: [String]?](/documentation/carplay/cpnowplayingsportseventstatus/eventstatustext)
- [CPNowPlayingSportsTeam](/documentation/carplay/cpnowplayingsportsteam)

### Initializers

- [init(name: String, logo: CPNowPlayingSportsTeamLogo, teamStandings: String?, eventScore: String, possessionIndicator: UIImage?, favorite: Bool)](/documentation/carplay/cpnowplayingsportsteam/init(name:logo:teamstandings:eventscore:possessionindicator:favorite:))

### Instance Properties

- [var eventScore: String](/documentation/carplay/cpnowplayingsportsteam/eventscore)
- [var isFavorite: Bool](/documentation/carplay/cpnowplayingsportsteam/isfavorite)
- [var logo: CPNowPlayingSportsTeamLogo](/documentation/carplay/cpnowplayingsportsteam/logo)
- [var name: String](/documentation/carplay/cpnowplayingsportsteam/name)
- [var possessionIndicator: UIImage?](/documentation/carplay/cpnowplayingsportsteam/possessionindicator)
- [var teamStandings: String?](/documentation/carplay/cpnowplayingsportsteam/teamstandings)
- [CPNowPlayingSportsTeamLogo](/documentation/carplay/cpnowplayingsportsteamlogo)

### Initializers

- [init(teamInitials: String)](/documentation/carplay/cpnowplayingsportsteamlogo/init(teaminitials:))
- [init(teamLogo: UIImage)](/documentation/carplay/cpnowplayingsportsteamlogo/init(teamlogo:))

### Instance Properties

- [var initials: String?](/documentation/carplay/cpnowplayingsportsteamlogo/initials)
- [var logo: UIImage?](/documentation/carplay/cpnowplayingsportsteamlogo/logo)

## Variables

- [let CPMaximumMessageItemLeadingDetailTextImageSize: CGSize](/documentation/carplay/cpmaximummessageitemleadingdetailtextimagesize)

## Functions

- [func NSStringFromCPJunctionType(CPJunctionType) -> String!](/documentation/carplay/nsstringfromcpjunctiontype(_:))
- [func NSStringFromCPLaneStatus(CPLaneStatus) -> String!](/documentation/carplay/nsstringfromcplanestatus(_:))
- [func NSStringFromCPManeuverType(CPManeuverType) -> String!](/documentation/carplay/nsstringfromcpmaneuvertype(_:))
- [func NSStringFromCPTrafficSide(CPTrafficSide) -> String!](/documentation/carplay/nsstringfromcptrafficside(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
