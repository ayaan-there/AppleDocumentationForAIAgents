# Preference Panes Documentation

Source: https://sosumi.ai/documentation/preferencepanes

---
title: Preference Panes
source: https://developer.apple.com/documentation/preferencepanes
timestamp: 2026-02-13T19:00:45.824Z
---

## Preference Pane Interface

- [NSPreferencePane](/documentation/preferencepanes/nspreferencepane)

### Initializing the Preference Pane

- [init(bundle: Bundle)](/documentation/preferencepanes/nspreferencepane/init(bundle:))

### Loading the Main View

- [func loadMainView() -> NSView](/documentation/preferencepanes/nspreferencepane/loadmainview())
- [func assignMainView()](/documentation/preferencepanes/nspreferencepane/assignmainview())
- [func mainViewDidLoad()](/documentation/preferencepanes/nspreferencepane/mainviewdidload())

### Getting the Bundle Information

- [var bundle: Bundle](/documentation/preferencepanes/nspreferencepane/bundle)
- [var mainNibName: String](/documentation/preferencepanes/nspreferencepane/mainnibname)
- [var mainView: NSView](/documentation/preferencepanes/nspreferencepane/mainview)

### Selecting and Deselecting the Preference Pane

- [func willSelect()](/documentation/preferencepanes/nspreferencepane/willselect())
- [func didSelect()](/documentation/preferencepanes/nspreferencepane/didselect())
- [func willUnselect()](/documentation/preferencepanes/nspreferencepane/willunselect())
- [func didUnselect()](/documentation/preferencepanes/nspreferencepane/didunselect())
- [var isSelected: Bool](/documentation/preferencepanes/nspreferencepane/isselected)
- [var shouldUnselect: NSPreferencePaneUnselectReply](/documentation/preferencepanes/nspreferencepane/shouldunselect)
- [NSPreferencePaneUnselectReply](/documentation/preferencepanes/nspreferencepaneunselectreply)

#### Replies

- [case unselectCancel](/documentation/preferencepanes/nspreferencepaneunselectreply/unselectcancel)
- [case unselectNow](/documentation/preferencepanes/nspreferencepaneunselectreply/unselectnow)
- [case unselectLater](/documentation/preferencepanes/nspreferencepaneunselectreply/unselectlater)

#### Initializers

- [init?(rawValue: UInt)](/documentation/preferencepanes/nspreferencepaneunselectreply/init(rawvalue:))
- [func reply(toShouldUnselect: Bool)](/documentation/preferencepanes/nspreferencepane/reply(toshouldunselect:))

### Handling keyboard focus

- [var firstKeyView: NSView?](/documentation/preferencepanes/nspreferencepane/firstkeyview)
- [var initialKeyView: NSView?](/documentation/preferencepanes/nspreferencepane/initialkeyview)
- [var lastKeyView: NSView?](/documentation/preferencepanes/nspreferencepane/lastkeyview)
- [var autoSaveTextFields: Bool](/documentation/preferencepanes/nspreferencepane/autosavetextfields)

### Help Menu support

- [func updateHelpMenu(with: [[String : String]]?)](/documentation/preferencepanes/nspreferencepane/updatehelpmenu(with:))

## Notifications

- [static let NSPreferencePrefPaneIsAvailable: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspreferenceprefpaneisavailable)
- [static let NSPreferencePaneDoUnselect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspreferencepanedounselect)
- [static let NSPreferencePaneCancelUnselect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspreferencepanecancelunselect)
- [static let NSPreferencePaneSwitchToPane: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspreferencepaneswitchtopane)
- [static let NSPreferencePaneUpdateHelpMenu: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspreferencepaneupdatehelpmenu)

## Help Menu Keys

- [let NSPrefPaneHelpMenuInfoPListKey: String](/documentation/preferencepanes/nsprefpanehelpmenuinfoplistkey)
- [let NSPrefPaneHelpMenuTitleKey: String](/documentation/preferencepanes/nsprefpanehelpmenutitlekey)
- [let NSPrefPaneHelpMenuAnchorKey: String](/documentation/preferencepanes/nsprefpanehelpmenuanchorkey)

## Reference

- [PreferencePanes Constants](/documentation/preferencepanes/preferencepanes-constants)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
