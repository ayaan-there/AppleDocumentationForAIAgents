# Finder Sync Documentation

Source: https://sosumi.ai/documentation/findersync

---
title: Finder Sync
source: https://developer.apple.com/documentation/findersync
timestamp: 2026-02-13T18:57:06.692Z
---

## Classes

- [FIFinderSync](/documentation/findersync/fifindersync-swift.class)
- [FIFinderSyncController](/documentation/findersync/fifindersynccontroller)

### Managing the Finder Sync Controller

- [class func `default`() -> Self](/documentation/findersync/fifindersynccontroller/default())
- [var directoryURLs: Set<URL>!](/documentation/findersync/fifindersynccontroller/directoryurls)
- [func selectedItemURLs() -> [URL]?](/documentation/findersync/fifindersynccontroller/selecteditemurls())
- [func setBadgeIdentifier(String, for: URL)](/documentation/findersync/fifindersynccontroller/setbadgeidentifier(_:for:))
- [func setBadgeImage(NSImage, label: String?, forBadgeIdentifier: String)](/documentation/findersync/fifindersynccontroller/setbadgeimage(_:label:forbadgeidentifier:))
- [func targetedURL() -> URL?](/documentation/findersync/fifindersynccontroller/targetedurl())

### Instance Methods

- [func lastUsedDateForItem(with: URL) -> Date?](/documentation/findersync/fifindersynccontroller/lastuseddateforitem(with:))
- [func setLastUsedDate(Date, forItemWith: URL, completion: (any Error) -> Void)](/documentation/findersync/fifindersynccontroller/setlastuseddate(_:foritemwith:completion:))
- [func setTagData(Data?, forItemWith: URL, completion: (any Error) -> Void)](/documentation/findersync/fifindersynccontroller/settagdata(_:foritemwith:completion:))
- [func tagDataForItem(with: URL) -> Data?](/documentation/findersync/fifindersynccontroller/tagdataforitem(with:))

### Type Properties

- [class var isExtensionEnabled: Bool](/documentation/findersync/fifindersynccontroller/isextensionenabled)

### Type Methods

- [class func showExtensionManagementInterface()](/documentation/findersync/fifindersynccontroller/showextensionmanagementinterface())

## Protocols

- [FIFinderSyncProtocol](/documentation/findersync/fifindersyncprotocol)

### Managing Badges, Shortcut Menus, and Toolbar Buttons

- [func beginObservingDirectory(at: URL)](/documentation/findersync/fifindersyncprotocol/beginobservingdirectory(at:))
- [func endObservingDirectory(at: URL)](/documentation/findersync/fifindersyncprotocol/endobservingdirectory(at:))
- [func menu(for: FIMenuKind) -> NSMenu?](/documentation/findersync/fifindersyncprotocol/menu(for:))
- [func requestBadgeIdentifier(for: URL)](/documentation/findersync/fifindersyncprotocol/requestbadgeidentifier(for:))
- [var toolbarItemImage: NSImage](/documentation/findersync/fifindersyncprotocol/toolbaritemimage)
- [var toolbarItemName: String](/documentation/findersync/fifindersyncprotocol/toolbaritemname)
- [var toolbarItemToolTip: String](/documentation/findersync/fifindersyncprotocol/toolbaritemtooltip)

### Constants

- [FIMenuKind](/documentation/findersync/fimenukind)

#### Constants

- [case contextualMenuForItems](/documentation/findersync/fimenukind/contextualmenuforitems)
- [case contextualMenuForContainer](/documentation/findersync/fimenukind/contextualmenuforcontainer)
- [case contextualMenuForSidebar](/documentation/findersync/fimenukind/contextualmenuforsidebar)
- [case toolbarItemMenu](/documentation/findersync/fimenukind/toolbaritemmenu)

#### Initializers

- [init?(rawValue: UInt)](/documentation/findersync/fimenukind/init(rawvalue:))

### Instance Methods

- [func makeListenerEndpoint(forServiceName: NSFileProviderServiceName, itemURL: URL) throws -> NSXPCListenerEndpoint](/documentation/findersync/fifindersyncprotocol/makelistenerendpoint(forservicename:itemurl:))
- [func supportedServiceNamesForItem(with: URL) -> [NSFileProviderServiceName]](/documentation/findersync/fifindersyncprotocol/supportedservicenamesforitem(with:))
- [func values(forAttributes: [URLResourceKey], forItemWith: URL, completion: ([URLResourceKey : Any], (any Error)?) -> Void)](/documentation/findersync/fifindersyncprotocol/values(forattributes:foritemwith:completion:))

## Reference

- [FinderSync Enumerations](/documentation/findersync/findersyncenumerations)

### Enumerations

- [FIMenuKind](/documentation/findersync/fimenukind)

#### Constants

- [case contextualMenuForItems](/documentation/findersync/fimenukind/contextualmenuforitems)
- [case contextualMenuForContainer](/documentation/findersync/fimenukind/contextualmenuforcontainer)
- [case contextualMenuForSidebar](/documentation/findersync/fimenukind/contextualmenuforsidebar)
- [case toolbarItemMenu](/documentation/findersync/fimenukind/toolbaritemmenu)

#### Initializers

- [init?(rawValue: UInt)](/documentation/findersync/fimenukind/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
