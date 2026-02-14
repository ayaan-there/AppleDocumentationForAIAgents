# File Provider Documentation

Source: https://sosumi.ai/documentation/fileprovider

---
title: File Provider
source: https://developer.apple.com/documentation/fileprovider
timestamp: 2026-02-13T18:56:58.125Z
---

## Essentials

- [File Provider updates](/documentation/updates/fileprovider)

## Extension types

- [Replicated File Provider extension](/documentation/fileprovider/replicated-file-provider-extension)

### Essentials

- [Synchronizing the File Provider Extension](/documentation/fileprovider/synchronizing-the-file-provider-extension)
- [Synchronizing files using file provider extensions](/documentation/fileprovider/synchronizing-files-using-file-provider-extensions)
- [Setting the Finder Sidebar Icon](/documentation/fileprovider/setting-the-finder-sidebar-icon)

### File Provider protocols

- [NSFileProviderReplicatedExtension](/documentation/fileprovider/nsfileproviderreplicatedextension)

#### Creating and Removing File Providers

- [init(domain: NSFileProviderDomain)](/documentation/fileprovider/nsfileproviderreplicatedextension/init(domain:))
- [func invalidate()](/documentation/fileprovider/nsfileproviderreplicatedextension/invalidate())

#### Accessing Remote Content

- [func item(for: NSFileProviderItemIdentifier, request: NSFileProviderRequest, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderreplicatedextension/item(for:request:completionhandler:))
- [func fetchContents(for: NSFileProviderItemIdentifier, version: NSFileProviderItemVersion?, request: NSFileProviderRequest, completionHandler: (URL?, NSFileProviderItem?, (any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderreplicatedextension/fetchcontents(for:version:request:completionhandler:))

#### Managing Items

- [func createItem(basedOn: NSFileProviderItem, fields: NSFileProviderItemFields, contents: URL?, options: NSFileProviderCreateItemOptions, request: NSFileProviderRequest, completionHandler: (NSFileProviderItem?, NSFileProviderItemFields, Bool, (any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderreplicatedextension/createitem(basedon:fields:contents:options:request:completionhandler:))
- [NSFileProviderCreateItemOptions](/documentation/fileprovider/nsfileprovidercreateitemoptions)

##### Choosing Create Item Options

- [static var mayAlreadyExist: NSFileProviderCreateItemOptions](/documentation/fileprovider/nsfileprovidercreateitemoptions/mayalreadyexist)
- [static var deletionConflicted: NSFileProviderCreateItemOptions](/documentation/fileprovider/nsfileprovidercreateitemoptions/deletionconflicted)

##### Creating Options

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovidercreateitemoptions/init(rawvalue:))
- [func modifyItem(NSFileProviderItem, baseVersion: NSFileProviderItemVersion, changedFields: NSFileProviderItemFields, contents: URL?, options: NSFileProviderModifyItemOptions, request: NSFileProviderRequest, completionHandler: (NSFileProviderItem?, NSFileProviderItemFields, Bool, (any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderreplicatedextension/modifyitem(_:baseversion:changedfields:contents:options:request:completionhandler:))
- [NSFileProviderModifyItemOptions](/documentation/fileprovider/nsfileprovidermodifyitemoptions)

##### Choosing Modify Item Options

- [static var mayAlreadyExist: NSFileProviderModifyItemOptions](/documentation/fileprovider/nsfileprovidermodifyitemoptions/mayalreadyexist)
- [static var failOnConflict: NSFileProviderModifyItemOptions](/documentation/fileprovider/nsfileprovidermodifyitemoptions/failonconflict)

##### Creating Modify Options

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovidermodifyitemoptions/init(rawvalue:))

##### Type Properties

- [static var isImmediateUploadRequestByPresentingApplication: NSFileProviderModifyItemOptions](/documentation/fileprovider/nsfileprovidermodifyitemoptions/isimmediateuploadrequestbypresentingapplication)
- [func deleteItem(identifier: NSFileProviderItemIdentifier, baseVersion: NSFileProviderItemVersion, options: NSFileProviderDeleteItemOptions, request: NSFileProviderRequest, completionHandler: ((any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderreplicatedextension/deleteitem(identifier:baseversion:options:request:completionhandler:))
- [NSFileProviderDeleteItemOptions](/documentation/fileprovider/nsfileproviderdeleteitemoptions)

##### Choosing Delete Options

- [static var recursive: NSFileProviderDeleteItemOptions](/documentation/fileprovider/nsfileproviderdeleteitemoptions/recursive)

##### Creating Delete Options

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileproviderdeleteitemoptions/init(rawvalue:))

#### Tracking Materialized Items

- [func materializedItemsDidChange(completionHandler: () -> Void)](/documentation/fileprovider/nsfileproviderreplicatedextension/materializeditemsdidchange(completionhandler:))

#### Tracking Pending Items

- [func pendingItemsDidChange(completionHandler: () -> Void)](/documentation/fileprovider/nsfileproviderreplicatedextension/pendingitemsdidchange(completionhandler:))

#### Importing Domains

- [func importDidFinish(completionHandler: () -> Void)](/documentation/fileprovider/nsfileproviderreplicatedextension/importdidfinish(completionhandler:))
- [NSFileProviderEnumerating](/documentation/fileprovider/nsfileproviderenumerating)

#### Accessing Enumerators

- [func enumerator(for: NSFileProviderItemIdentifier, request: NSFileProviderRequest) throws -> any NSFileProviderEnumerator](/documentation/fileprovider/nsfileproviderenumerating/enumerator(for:request:))
- [NSFileProviderIncrementalContentFetching](/documentation/fileprovider/nsfileproviderincrementalcontentfetching)

#### Incrementally Fetching Contents

- [func fetchContents(for: NSFileProviderItemIdentifier, version: NSFileProviderItemVersion?, usingExistingContentsAt: URL, existingVersion: NSFileProviderItemVersion, request: NSFileProviderRequest, completionHandler: (URL?, NSFileProviderItem?, (any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderincrementalcontentfetching/fetchcontents(for:version:usingexistingcontentsat:existingversion:request:completionhandler:))
- [NSFileProviderPartialContentFetching](/documentation/fileprovider/nsfileproviderpartialcontentfetching)

#### Fetching Ranges from a File

- [func fetchPartialContents(for: NSFileProviderItemIdentifier, version: NSFileProviderItemVersion, request: NSFileProviderRequest, minimalRange: NSRange, aligningTo: Int, options: NSFileProviderFetchContentsOptions, completionHandler: (URL?, NSFileProviderItem?, NSRange, NSFileProviderMaterializationFlags, (any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderpartialcontentfetching/fetchpartialcontents(for:version:request:minimalrange:aligningto:options:completionhandler:))
- [NSFileProviderFetchContentsOptions](/documentation/fileprovider/nsfileproviderfetchcontentsoptions)

##### Accessing Options

- [static var strictVersioning: NSFileProviderFetchContentsOptions](/documentation/fileprovider/nsfileproviderfetchcontentsoptions/strictversioning)

##### Creating Options

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileproviderfetchcontentsoptions/init(rawvalue:))
- [NSFileProviderMaterializationFlags](/documentation/fileprovider/nsfileprovidermaterializationflags)

##### Accessing Flags

- [static var knownSparseRanges: NSFileProviderMaterializationFlags](/documentation/fileprovider/nsfileprovidermaterializationflags/knownsparseranges)

##### Creating Flags

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovidermaterializationflags/init(rawvalue:))
- [NSFileProviderServicing](/documentation/fileprovider/nsfileproviderservicing)

#### Providing a Service Source

- [func supportedServiceSources(for: NSFileProviderItemIdentifier, completionHandler: ([any NSFileProviderServiceSource]?, (any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderservicing/supportedservicesources(for:completionhandler:))
- [NSFileProviderCustomAction](/documentation/fileprovider/nsfileprovidercustomaction)

#### Performing Custom Actions

- [func performAction(identifier: NSFileProviderExtensionActionIdentifier, onItemsWithIdentifiers: [NSFileProviderItemIdentifier], completionHandler: ((any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileprovidercustomaction/performaction(identifier:onitemswithidentifiers:completionhandler:))
- [NSFileProviderExtensionActionIdentifier](/documentation/fileprovider/nsfileproviderextensionactionidentifier)

#### Creating Identifiers

- [init(String)](/documentation/fileprovider/nsfileproviderextensionactionidentifier/init(_:))
- [init(rawValue: String)](/documentation/fileprovider/nsfileproviderextensionactionidentifier/init(rawvalue:))
- [NSFileProviderThumbnailing](/documentation/fileprovider/nsfileproviderthumbnailing)

#### Providing Thumbnails

- [func fetchThumbnails(for: [NSFileProviderItemIdentifier], requestedSize: CGSize, perThumbnailCompletionHandler: (NSFileProviderItemIdentifier, Data?, (any Error)?) -> Void, completionHandler: ((any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderthumbnailing/fetchthumbnails(for:requestedsize:perthumbnailcompletionhandler:completionhandler:))
- [NSFileProviderPendingSetEnumerator](/documentation/fileprovider/nsfileproviderpendingsetenumerator)

#### Accessing Refresh Data

- [var domainVersion: NSFileProviderDomainVersion?](/documentation/fileprovider/nsfileproviderpendingsetenumerator/domainversion)
- [var refreshInterval: TimeInterval](/documentation/fileprovider/nsfileproviderpendingsetenumerator/refreshinterval)

#### Instance Properties

- [var isMaximumSizeReached: Bool](/documentation/fileprovider/nsfileproviderpendingsetenumerator/ismaximumsizereached)

### Items and metadata

- [NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields)

#### Specifying the Required Fields

- [static var filename: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/filename)
- [static var contents: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/contents)

#### Specifying Content Location

- [static var parentItemIdentifier: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/parentitemidentifier)

#### Tracking Usage

- [static var contentModificationDate: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/contentmodificationdate)
- [static var creationDate: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/creationdate)
- [static var lastUsedDate: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/lastuseddate)

#### Working with Metadata

- [static var extendedAttributes: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/extendedattributes)
- [static var fileSystemFlags: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/filesystemflags)
- [static var tagData: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/tagdata)
- [static var favoriteRank: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/favoriterank)
- [static var typeAndCreator: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovideritemfields/typeandcreator)

#### Initializers

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovideritemfields/init(rawvalue:))
- [NSFileProviderItemVersion](/documentation/fileprovider/nsfileprovideritemversion)

#### Creating Version Instances

- [init(contentVersion: Data, metadataVersion: Data)](/documentation/fileprovider/nsfileprovideritemversion/init(contentversion:metadataversion:))

#### Accessing Version Data

- [class var beforeFirstSyncComponent: Data](/documentation/fileprovider/nsfileprovideritemversion/beforefirstsynccomponent)
- [var contentVersion: Data](/documentation/fileprovider/nsfileprovideritemversion/contentversion)
- [var metadataVersion: Data](/documentation/fileprovider/nsfileprovideritemversion/metadataversion)
- [NSFileProviderRequest](/documentation/fileprovider/nsfileproviderrequest)

#### Accessing Application Information

- [var domainVersion: NSFileProviderDomainVersion?](/documentation/fileprovider/nsfileproviderrequest/domainversion)
- [var requestingExecutable: URL?](/documentation/fileprovider/nsfileproviderrequest/requestingexecutable)
- [var isFileViewerRequest: Bool](/documentation/fileprovider/nsfileproviderrequest/isfileviewerrequest)
- [var isSystemRequest: Bool](/documentation/fileprovider/nsfileproviderrequest/issystemrequest)
- [NSFileProviderItemDecorating](/documentation/fileprovider/nsfileprovideritemdecorating)

#### Providing Decorations

- [var decorations: [NSFileProviderItemDecorationIdentifier]?](/documentation/fileprovider/nsfileprovideritemdecorating/decorations)
- [NSFileProviderItemDecorationIdentifier](/documentation/fileprovider/nsfileprovideritemdecorationidentifier)

#### Creating Decoration Identifiers

- [init(String)](/documentation/fileprovider/nsfileprovideritemdecorationidentifier/init(_:))
- [init(rawValue: String)](/documentation/fileprovider/nsfileprovideritemdecorationidentifier/init(rawvalue:))

### Domains

- [NSFileProviderDomainVersion](/documentation/fileprovider/nsfileproviderdomainversion)

#### Creating Versions

- [func next() -> NSFileProviderDomainVersion](/documentation/fileprovider/nsfileproviderdomainversion/next())
- [NSFileProviderDomainState](/documentation/fileprovider/nsfileproviderdomainstate)

#### Accessing State Data

- [var domainVersion: NSFileProviderDomainVersion](/documentation/fileprovider/nsfileproviderdomainstate/domainversion)
- [var userInfo: [AnyHashable : Any]](/documentation/fileprovider/nsfileproviderdomainstate/userinfo)

### Testing protocols

- [NSFileProviderTestingChildrenEnumeration](/documentation/fileprovider/nsfileprovidertestingchildrenenumeration)

#### Accessing The Operation’s Data

- [var itemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidertestingchildrenenumeration/itemidentifier)
- [var side: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingchildrenenumeration/side)
- [NSFileProviderTestingCollisionResolution](/documentation/fileprovider/nsfileprovidertestingcollisionresolution)

#### Accessing the Operation’s Data

- [var renamedItem: NSFileProviderItem](/documentation/fileprovider/nsfileprovidertestingcollisionresolution/renameditem)
- [var side: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingcollisionresolution/side)
- [NSFileProviderTestingContentFetch](/documentation/fileprovider/nsfileprovidertestingcontentfetch)

#### Accessing the Operation’s Data

- [var itemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidertestingcontentfetch/itemidentifier)
- [var side: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingcontentfetch/side)
- [NSFileProviderTestingCreation](/documentation/fileprovider/nsfileprovidertestingcreation)

#### Accessing the Operation’s Data

- [var sourceItem: NSFileProviderItem](/documentation/fileprovider/nsfileprovidertestingcreation/sourceitem)
- [var targetSide: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingcreation/targetside)
- [var domainVersion: NSFileProviderDomainVersion?](/documentation/fileprovider/nsfileprovidertestingcreation/domainversion)
- [NSFileProviderTestingDeletion](/documentation/fileprovider/nsfileprovidertestingdeletion)

#### Accessing the Operation’s Data

- [var sourceItemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidertestingdeletion/sourceitemidentifier)
- [var targetSide: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingdeletion/targetside)
- [var targetItemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidertestingdeletion/targetitemidentifier)
- [var targetItemBaseVersion: NSFileProviderItemVersion](/documentation/fileprovider/nsfileprovidertestingdeletion/targetitembaseversion)
- [var domainVersion: NSFileProviderDomainVersion?](/documentation/fileprovider/nsfileprovidertestingdeletion/domainversion)
- [NSFileProviderTestingIngestion](/documentation/fileprovider/nsfileprovidertestingingestion)

#### Accessing the Operation’s Data

- [var itemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidertestingingestion/itemidentifier)
- [var item: NSFileProviderItem?](/documentation/fileprovider/nsfileprovidertestingingestion/item)
- [var side: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingingestion/side)
- [NSFileProviderTestingLookup](/documentation/fileprovider/nsfileprovidertestinglookup)

#### Accessing the Operation’s Data

- [var itemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidertestinglookup/itemidentifier)
- [var side: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestinglookup/side)
- [NSFileProviderTestingModification](/documentation/fileprovider/nsfileprovidertestingmodification)

#### Accessing the Operation’s Data

- [var sourceItem: NSFileProviderItem](/documentation/fileprovider/nsfileprovidertestingmodification/sourceitem)
- [var changedFields: NSFileProviderItemFields](/documentation/fileprovider/nsfileprovidertestingmodification/changedfields)
- [var targetSide: NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingmodification/targetside)
- [var targetItemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidertestingmodification/targetitemidentifier)
- [var targetItemBaseVersion: NSFileProviderItemVersion](/documentation/fileprovider/nsfileprovidertestingmodification/targetitembaseversion)
- [var domainVersion: NSFileProviderDomainVersion?](/documentation/fileprovider/nsfileprovidertestingmodification/domainversion)
- [NSFileProviderTestingOperation](/documentation/fileprovider/nsfileprovidertestingoperation)

#### Access the Operation Type

- [var type: NSFileProviderTestingOperationType](/documentation/fileprovider/nsfileprovidertestingoperation/type)
- [NSFileProviderUserInteractionSuppressing](/documentation/fileprovider/nsfileprovideruserinteractionsuppressing)

#### Supressing Interactions

- [func isInteractionSuppressed(forIdentifier: String) -> Bool](/documentation/fileprovider/nsfileprovideruserinteractionsuppressing/isinteractionsuppressed(foridentifier:))
- [func setInteractionSuppressed(Bool, forIdentifier: String)](/documentation/fileprovider/nsfileprovideruserinteractionsuppressing/setinteractionsuppressed(_:foridentifier:))
- [NSFileProviderTestingOperationSide](/documentation/fileprovider/nsfileprovidertestingoperationside)

#### Locations

- [case disk](/documentation/fileprovider/nsfileprovidertestingoperationside/disk)
- [case fileProvider](/documentation/fileprovider/nsfileprovidertestingoperationside/fileprovider)

#### Initializers

- [init?(rawValue: UInt)](/documentation/fileprovider/nsfileprovidertestingoperationside/init(rawvalue:))
- [NSFileProviderTestingOperationType](/documentation/fileprovider/nsfileprovidertestingoperationtype)

#### Types

- [case childrenEnumeration](/documentation/fileprovider/nsfileprovidertestingoperationtype/childrenenumeration)
- [case collisionResolution](/documentation/fileprovider/nsfileprovidertestingoperationtype/collisionresolution)
- [case contentFetch](/documentation/fileprovider/nsfileprovidertestingoperationtype/contentfetch)
- [case creation](/documentation/fileprovider/nsfileprovidertestingoperationtype/creation)
- [case deletion](/documentation/fileprovider/nsfileprovidertestingoperationtype/deletion)
- [case ingestion](/documentation/fileprovider/nsfileprovidertestingoperationtype/ingestion)
- [case lookup](/documentation/fileprovider/nsfileprovidertestingoperationtype/lookup)
- [case modification](/documentation/fileprovider/nsfileprovidertestingoperationtype/modification)

#### Initializers

- [init?(rawValue: Int)](/documentation/fileprovider/nsfileprovidertestingoperationtype/init(rawvalue:))
- [com.apple.developer.fileprovider.testing-mode](/documentation/bundleresources/entitlements/com.apple.developer.fileprovider.testing-mode)

### Information property list keys

- [NSDownloadsUbiquitousContents](/documentation/bundleresources/information-property-list/nsdownloadsubiquitouscontents)
- [com.apple.developer.fileprovider.testing-mode](/documentation/bundleresources/entitlements/com.apple.developer.fileprovider.testing-mode)
- [CFBundleSymbolName](/documentation/bundleresources/information-property-list/cfbundleicons/cfbundleprimaryicon/cfbundlesymbolname)
- [Nonreplicated File Provider extension](/documentation/fileprovider/nonreplicated-file-provider-extension)

### Nonreplicated extension

- [NSFileProviderExtension](/documentation/fileprovider/nsfileproviderextension)

#### Working with items and persistent identifiers

- [func persistentIdentifierForItem(at: URL) -> NSFileProviderItemIdentifier?](/documentation/fileprovider/nsfileproviderextension/persistentidentifierforitem(at:))
- [func urlForItem(withPersistentIdentifier: NSFileProviderItemIdentifier) -> URL?](/documentation/fileprovider/nsfileproviderextension/urlforitem(withpersistentidentifier:))
- [func item(for: NSFileProviderItemIdentifier) throws -> NSFileProviderItem](/documentation/fileprovider/nsfileproviderextension/item(for:))
- [func enumerator(for: NSFileProviderItemIdentifier) throws -> any NSFileProviderEnumerator](/documentation/fileprovider/nsfileproviderextension/enumerator(for:))
- [NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier)

##### Constants

- [static let rootContainer: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/rootcontainer)
- [static let workingSet: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/workingset)
- [static let trashContainer: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/trashcontainer)

##### Initializers

- [init(String)](/documentation/fileprovider/nsfileprovideritemidentifier/init(_:))
- [init(rawValue: String)](/documentation/fileprovider/nsfileprovideritemidentifier/init(rawvalue:))

#### Managing shared files

- [func itemChanged(at: URL)](/documentation/fileprovider/nsfileproviderextension/itemchanged(at:))
- [func providePlaceholder(at: URL, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/provideplaceholder(at:completionhandler:))
- [func startProvidingItem(at: URL, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/startprovidingitem(at:completionhandler:))
- [func stopProvidingItem(at: URL)](/documentation/fileprovider/nsfileproviderextension/stopprovidingitem(at:))

#### Handling actions

- [Providing support for user-driven actions](/documentation/fileprovider/providing-support-for-user-driven-actions)

##### Signaling Changes

- [Signaling Changes for User-Driven Actions](/documentation/fileprovider/signaling-changes-for-user-driven-actions)

##### Handling Errors

- [Handling Errors with User-Driven Actions](/documentation/fileprovider/handling-errors-with-user-driven-actions)
- [func createDirectory(withName: String, inParentItemIdentifier: NSFileProviderItemIdentifier, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/createdirectory(withname:inparentitemidentifier:completionhandler:))
- [func deleteItem(withIdentifier: NSFileProviderItemIdentifier, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/deleteitem(withidentifier:completionhandler:))
- [func importDocument(at: URL, toParentItemIdentifier: NSFileProviderItemIdentifier, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/importdocument(at:toparentitemidentifier:completionhandler:))
- [func renameItem(withIdentifier: NSFileProviderItemIdentifier, toName: String, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/renameitem(withidentifier:toname:completionhandler:))
- [func reparentItem(withIdentifier: NSFileProviderItemIdentifier, toParentItemWithIdentifier: NSFileProviderItemIdentifier, newName: String?, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/reparentitem(withidentifier:toparentitemwithidentifier:newname:completionhandler:))
- [func setFavoriteRank(NSNumber?, forItemIdentifier: NSFileProviderItemIdentifier, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/setfavoriterank(_:foritemidentifier:completionhandler:))
- [func setLastUsedDate(Date?, forItemIdentifier: NSFileProviderItemIdentifier, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/setlastuseddate(_:foritemidentifier:completionhandler:))
- [func setTagData(Data?, forItemIdentifier: NSFileProviderItemIdentifier, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/settagdata(_:foritemidentifier:completionhandler:))
- [func trashItem(withIdentifier: NSFileProviderItemIdentifier, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/trashitem(withidentifier:completionhandler:))
- [func untrashItem(withIdentifier: NSFileProviderItemIdentifier, toParentItemIdentifier: NSFileProviderItemIdentifier?, completionHandler: (NSFileProviderItem?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderextension/untrashitem(withidentifier:toparentitemidentifier:completionhandler:))

#### Managing domains

- [var domain: NSFileProviderDomain?](/documentation/fileprovider/nsfileproviderextension/domain)

#### Accessing thumbnails

- [func fetchThumbnails(for: [NSFileProviderItemIdentifier], requestedSize: CGSize, perThumbnailCompletionHandler: (NSFileProviderItemIdentifier, Data?, (any Error)?) -> Void, completionHandler: ((any Error)?) -> Void) -> Progress](/documentation/fileprovider/nsfileproviderextension/fetchthumbnails(for:requestedsize:perthumbnailcompletionhandler:completionhandler:))

#### Working with services

- [func supportedServiceSources(for: NSFileProviderItemIdentifier) throws -> [any NSFileProviderServiceSource]](/documentation/fileprovider/nsfileproviderextension/supportedservicesources(for:))
- [NSFileProviderServiceSource](/documentation/fileprovider/nsfileproviderservicesource)

##### Accessing the Service

- [var serviceName: NSFileProviderServiceName](/documentation/fileprovider/nsfileproviderservicesource/servicename)
- [func makeListenerEndpoint() throws -> NSXPCListenerEndpoint](/documentation/fileprovider/nsfileproviderservicesource/makelistenerendpoint())
- [var isRestricted: Bool](/documentation/fileprovider/nsfileproviderservicesource/isrestricted)

#### Managing placeholders

- [class func placeholderURL(for: URL) -> URL](/documentation/fileprovider/nsfileproviderextension/placeholderurl(for:))
- [class func writePlaceholder(at: URL, withMetadata: [URLResourceKey : Any]) throws](/documentation/fileprovider/nsfileproviderextension/writeplaceholder(at:withmetadata:))

#### Accessing the document storage

- [var documentStorageURL: URL](/documentation/fileprovider/nsfileproviderextension/documentstorageurl)
- [var providerIdentifier: String](/documentation/fileprovider/nsfileproviderextension/provideridentifier)
- [Content and Change Tracking](/documentation/fileprovider/content-and-change-tracking)

#### Essentials

- [NSFileProviderEnumerator](/documentation/fileprovider/nsfileproviderenumerator)

##### Enumerating Items and Changes

- [func enumerateItems(for: any NSFileProviderEnumerationObserver, startingAt: NSFileProviderPage)](/documentation/fileprovider/nsfileproviderenumerator/enumerateitems(for:startingat:))
- [func enumerateChanges(for: any NSFileProviderChangeObserver, from: NSFileProviderSyncAnchor)](/documentation/fileprovider/nsfileproviderenumerator/enumeratechanges(for:from:))
- [func currentSyncAnchor(completionHandler: (NSFileProviderSyncAnchor?) -> Void)](/documentation/fileprovider/nsfileproviderenumerator/currentsyncanchor(completionhandler:))
- [func invalidate()](/documentation/fileprovider/nsfileproviderenumerator/invalidate())

#### Content

- [Defining Your File Provider’s Content](/documentation/fileprovider/defining-your-file-provider-s-content)
- [NSFileProviderEnumerationObserver](/documentation/fileprovider/nsfileproviderenumerationobserver)

##### Observing Item Enumeration

- [func didEnumerate([any NSFileProviderItemProtocol])](/documentation/fileprovider/nsfileproviderenumerationobserver/didenumerate(_:))
- [func finishEnumerating(upTo: NSFileProviderPage?)](/documentation/fileprovider/nsfileproviderenumerationobserver/finishenumerating(upto:))
- [func finishEnumeratingWithError(any Error)](/documentation/fileprovider/nsfileproviderenumerationobserver/finishenumeratingwitherror(_:))
- [var suggestedPageSize: Int](/documentation/fileprovider/nsfileproviderenumerationobserver/suggestedpagesize)
- [NSFileProviderPage](/documentation/fileprovider/nsfileproviderpage)

##### Page Constants

- [static let initialPageSortedByName: NSData](/documentation/fileprovider/nsfileproviderpage/initialpagesortedbyname)
- [static let initialPageSortedByDate: NSData](/documentation/fileprovider/nsfileproviderpage/initialpagesortedbydate)

##### Initializers

- [init(Data)](/documentation/fileprovider/nsfileproviderpage/init(_:))
- [init(rawValue: Data)](/documentation/fileprovider/nsfileproviderpage/init(rawvalue:))

#### Change Tracking

- [Tracking Your File Provider’s Changes](/documentation/fileprovider/tracking-your-file-provider-s-changes)

##### Tracking Document Changes

- [Tracking Changes to Documents](/documentation/fileprovider/tracking-changes-to-documents)

##### Signaling Changes with Push Notifications

- [Using push notifications to signal changes](/documentation/fileprovider/using-push-notifications-to-signal-changes)
- [NSFileProviderChangeObserver](/documentation/fileprovider/nsfileproviderchangeobserver)

##### Observing Changes

- [func didDeleteItems(withIdentifiers: [NSFileProviderItemIdentifier])](/documentation/fileprovider/nsfileproviderchangeobserver/diddeleteitems(withidentifiers:))
- [func didUpdate([any NSFileProviderItemProtocol])](/documentation/fileprovider/nsfileproviderchangeobserver/didupdate(_:))
- [func finishEnumeratingChanges(upTo: NSFileProviderSyncAnchor, moreComing: Bool)](/documentation/fileprovider/nsfileproviderchangeobserver/finishenumeratingchanges(upto:morecoming:))
- [func finishEnumeratingWithError(any Error)](/documentation/fileprovider/nsfileproviderchangeobserver/finishenumeratingwitherror(_:))
- [var suggestedBatchSize: Int](/documentation/fileprovider/nsfileproviderchangeobserver/suggestedbatchsize)
- [NSFileProviderSyncAnchor](/documentation/fileprovider/nsfileprovidersyncanchor)

##### Creating Sync Anchors

- [init(Data)](/documentation/fileprovider/nsfileprovidersyncanchor/init(_:))
- [init(rawValue: Data)](/documentation/fileprovider/nsfileprovidersyncanchor/init(rawvalue:))

## Extension management

- [NSFileProviderManager](/documentation/fileprovider/nsfileprovidermanager)

### Accessing File Provider data

- [class var `default`: NSFileProviderManager](/documentation/fileprovider/nsfileprovidermanager/default)
- [var documentStorageURL: URL](/documentation/fileprovider/nsfileprovidermanager/documentstorageurl)
- [var providerIdentifier: String](/documentation/fileprovider/nsfileprovidermanager/provideridentifier)

### Translating user-visible URLs

- [func getUserVisibleURL(for: NSFileProviderItemIdentifier, completionHandler: (URL?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/getuservisibleurl(for:completionhandler:))
- [class func getIdentifierForUserVisibleFile(at: URL, completionHandler: (NSFileProviderItemIdentifier?, NSFileProviderDomainIdentifier?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/getidentifierforuservisiblefile(at:completionhandler:))

### Working with items

- [func reimportItems(below: NSFileProviderItemIdentifier, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/reimportitems(below:completionhandler:))
- [func evictItem(identifier: NSFileProviderItemIdentifier, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/evictitem(identifier:completionhandler:))
- [func requestDownloadForItem(withIdentifier: NSFileProviderItemIdentifier, requestedRange: NSRange?) async throws](/documentation/fileprovider/nsfileprovidermanager/requestdownloadforitem(withidentifier:requestedrange:))
- [func requestDownloadForItem(withIdentifier: NSFileProviderItemIdentifier, requestedRange: NSRange?, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/requestdownloadforitem(withidentifier:requestedrange:completionhandler:))
- [func requestModification(of: NSFileProviderItemFields, forItemWithIdentifier: NSFileProviderItemIdentifier, options: NSFileProviderModifyItemOptions, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/requestmodification(of:foritemwithidentifier:options:completionhandler:))
- [func enumeratorForMaterializedItems() -> any NSFileProviderEnumerator](/documentation/fileprovider/nsfileprovidermanager/enumeratorformaterializeditems())
- [func enumeratorForPendingItems() -> any NSFileProviderPendingSetEnumerator](/documentation/fileprovider/nsfileprovidermanager/enumeratorforpendingitems())

### Performing actions

- [class func placeholderURL(for: URL) -> URL](/documentation/fileprovider/nsfileprovidermanager/placeholderurl(for:))
- [class func writePlaceholder(at: URL, withMetadata: NSFileProviderItem) throws](/documentation/fileprovider/nsfileprovidermanager/writeplaceholder(at:withmetadata:))
- [func register(URLSessionTask, forItemWithIdentifier: NSFileProviderItemIdentifier, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/register(_:foritemwithidentifier:completionhandler:))
- [func signalEnumerator(for: NSFileProviderItemIdentifier, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/signalenumerator(for:completionhandler:))
- [func waitForChanges(below: NSFileProviderItemIdentifier, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/waitforchanges(below:completionhandler:))
- [func globalProgress(for: Progress.FileOperationKind) -> Progress](/documentation/fileprovider/nsfileprovidermanager/globalprogress(for:))

### Working with domains

- [convenience init?(for: NSFileProviderDomain)](/documentation/fileprovider/nsfileprovidermanager/init(for:))
- [class func `import`(NSFileProviderDomain, fromDirectoryAt: URL, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/import(_:fromdirectoryat:completionhandler:))
- [class func add(NSFileProviderDomain, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/add(_:completionhandler:))
- [class func getDomainsWithCompletionHandler(([NSFileProviderDomain], (any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/getdomainswithcompletionhandler(_:))
- [class func remove(NSFileProviderDomain, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/remove(_:completionhandler:))
- [class func remove(NSFileProviderDomain, mode: NSFileProviderManager.DomainRemovalMode, completionHandler: (URL?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/remove(_:mode:completionhandler:))
- [class func removeAllDomains(completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/removealldomains(completionhandler:))
- [NSFileProviderManager.DomainRemovalMode](/documentation/fileprovider/nsfileprovidermanager/domainremovalmode)

#### Options

- [case removeAll](/documentation/fileprovider/nsfileprovidermanager/domainremovalmode/removeall)
- [case preserveDirtyUserData](/documentation/fileprovider/nsfileprovidermanager/domainremovalmode/preservedirtyuserdata)
- [case preserveDownloadedUserData](/documentation/fileprovider/nsfileprovidermanager/domainremovalmode/preservedownloadeduserdata)

#### Initializers

- [init?(rawValue: Int)](/documentation/fileprovider/nsfileprovidermanager/domainremovalmode/init(rawvalue:))
- [func disconnect(reason: String, options: NSFileProviderManager.DisconnectionOptions, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/disconnect(reason:options:completionhandler:))
- [NSFileProviderManager.DisconnectionOptions](/documentation/fileprovider/nsfileprovidermanager/disconnectionoptions)

#### Choosing Disconnection Options

- [static var temporary: NSFileProviderManager.DisconnectionOptions](/documentation/fileprovider/nsfileprovidermanager/disconnectionoptions/temporary)

#### Creating Disconnection Options

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovidermanager/disconnectionoptions/init(rawvalue:))
- [func reconnect(completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/reconnect(completionhandler:))
- [func waitForStabilization(completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/waitforstabilization(completionhandler:))
- [func temporaryDirectoryURL() throws -> URL](/documentation/fileprovider/nsfileprovidermanager/temporarydirectoryurl())

### Syncing Desktop and Documents folders

- [func claimKnownFolders(NSFileProviderKnownFolderLocations, localizedReason: String, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/claimknownfolders(_:localizedreason:completionhandler:))
- [func releaseKnownFolders(NSFileProviderKnownFolders, localizedReason: String, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/releaseknownfolders(_:localizedreason:completionhandler:))
- [NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderknownfolders)

#### Identifying known folders

- [static var desktop: NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderknownfolders/desktop)
- [static var documents: NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderknownfolders/documents)

#### Creating a known-folder identifier

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileproviderknownfolders/init(rawvalue:))
- [NSFileProviderKnownFolderLocations](/documentation/fileprovider/nsfileproviderknownfolderlocations)

#### Identifying known-folder locations

- [var desktopLocation: NSFileProviderKnownFolderLocations.Location?](/documentation/fileprovider/nsfileproviderknownfolderlocations/desktoplocation)
- [var documentsLocation: NSFileProviderKnownFolderLocations.Location?](/documentation/fileprovider/nsfileproviderknownfolderlocations/documentslocation)
- [NSFileProviderKnownFolderLocations.Location](/documentation/fileprovider/nsfileproviderknownfolderlocations/location)

##### Initializers

- [init(existingItemIdentifier: NSFileProviderItemIdentifier)](/documentation/fileprovider/nsfileproviderknownfolderlocations/location/init(existingitemidentifier:))
- [init(parentItemIdentifier: NSFileProviderItemIdentifier, filename: String)](/documentation/fileprovider/nsfileproviderknownfolderlocations/location/init(parentitemidentifier:filename:))

#### Configuring folder options

- [var shouldCreateBinaryCompatibilitySymlink: Bool](/documentation/fileprovider/nsfileproviderknownfolderlocations/shouldcreatebinarycompatibilitysymlink)

#### Creating a known-folder locations object

- [init()](/documentation/fileprovider/nsfileproviderknownfolderlocations/init())
- [NSFileProviderKnownFolderSupporting](/documentation/fileprovider/nsfileproviderknownfoldersupporting)

#### Providing known-folder locations to the system

- [func getKnownFolderLocations(NSFileProviderKnownFolders, completionHandler: (NSFileProviderKnownFolderLocations?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderknownfoldersupporting/getknownfolderlocations(_:completionhandler:))

### Working with external volumes

- [func stateDirectoryURL() throws -> URL](/documentation/fileprovider/nsfileprovidermanager/statedirectoryurl())
- [class func checkDomainsCanBeStoredOnVolume(at: URL) throws -> NSFileProviderManager.EligibilityResult](/documentation/fileprovider/nsfileprovidermanager/checkdomainscanbestoredonvolume(at:))
- [NSFileProviderManager.EligibilityResult](/documentation/fileprovider/nsfileprovidermanager/eligibilityresult)

#### Determining eligibility

- [case eligible](/documentation/fileprovider/nsfileprovidermanager/eligibilityresult/eligible)
- [case ineligible(NSFileProviderVolumeUnsupportedReason)](/documentation/fileprovider/nsfileprovidermanager/eligibilityresult/ineligible(_:))
- [NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason)

##### Reasons

- [static var unknown: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/unknown)
- [static var nonEncrypted: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/nonencrypted)
- [static var readOnly: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/readonly)
- [static var network: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/network)
- [static var quarantined: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/quarantined)

##### Initializers

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/init(rawvalue:))

##### Type Properties

- [static var nonAPFS: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/nonapfs)
- [NSFileProviderExternalVolumeHandling](/documentation/fileprovider/nsfileproviderexternalvolumehandling)

#### Connecting to external domains

- [func shouldConnectExternalDomain(completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileproviderexternalvolumehandling/shouldconnectexternaldomain(completionhandler:))

### Using services

- [func getService(named: NSFileProviderServiceName, for: NSFileProviderItemIdentifier, completionHandler: (NSFileProviderService?, (any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/getservice(named:for:completionhandler:))

### Testing

- [func listAvailableTestingOperations() throws -> [any NSFileProviderTestingOperation]](/documentation/fileprovider/nsfileprovidermanager/listavailabletestingoperations())
- [func run([any NSFileProviderTestingOperation]) throws -> [AnyHashable : any Error]](/documentation/fileprovider/nsfileprovidermanager/run(_:))

### Handling errors

- [func signalErrorResolved(any Error, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/signalerrorresolved(_:completionhandler:))

### Collecting diagnostic reports

- [func requestDiagnosticCollection(for: NSFileProviderItemIdentifier, errorReason: any Error, completionHandler: ((any Error)?) -> Void)](/documentation/fileprovider/nsfileprovidermanager/requestdiagnosticcollection(for:errorreason:completionhandler:))

## Provided items

- [NSFileProviderItem](/documentation/fileprovider/nsfileprovideritem-swift.typealias)
- [NSFileProviderItemProtocol](/documentation/fileprovider/nsfileprovideritemprotocol)

### Providing Required Properties

- [var itemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemprotocol/itemidentifier)
- [var filename: String](/documentation/fileprovider/nsfileprovideritemprotocol/filename)
- [var typeIdentifier: String](/documentation/fileprovider/nsfileprovideritemprotocol/typeidentifier)
- [var contentType: UTType](/documentation/fileprovider/nsfileprovideritemprotocol/contenttype)
- [var capabilities: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemprotocol/capabilities)

### Managing Content

- [var childItemCount: NSNumber?](/documentation/fileprovider/nsfileprovideritemprotocol/childitemcount)
- [var documentSize: NSNumber?](/documentation/fileprovider/nsfileprovideritemprotocol/documentsize)
- [var contentPolicy: NSFileProviderContentPolicy](/documentation/fileprovider/nsfileprovideritemprotocol/contentpolicy)
- [NSFileProviderContentPolicy](/documentation/fileprovider/nsfileprovidercontentpolicy)

#### Policies

- [case downloadEagerlyAndKeepDownloaded](/documentation/fileprovider/nsfileprovidercontentpolicy/downloadeagerlyandkeepdownloaded)
- [case downloadLazily](/documentation/fileprovider/nsfileprovidercontentpolicy/downloadlazily)
- [case downloadLazilyAndEvictOnRemoteUpdate](/documentation/fileprovider/nsfileprovidercontentpolicy/downloadlazilyandevictonremoteupdate)
- [case inherited](/documentation/fileprovider/nsfileprovidercontentpolicy/inherited)

#### Initializers

- [init?(rawValue: Int)](/documentation/fileprovider/nsfileprovidercontentpolicy/init(rawvalue:))

### Specifying Content Location

- [var parentItemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemprotocol/parentitemidentifier)
- [var isTrashed: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/istrashed)
- [var symlinkTargetPath: String?](/documentation/fileprovider/nsfileprovideritemprotocol/symlinktargetpath)

### Tracking Usage

- [var contentModificationDate: Date?](/documentation/fileprovider/nsfileprovideritemprotocol/contentmodificationdate)
- [var creationDate: Date?](/documentation/fileprovider/nsfileprovideritemprotocol/creationdate)
- [var lastUsedDate: Date?](/documentation/fileprovider/nsfileprovideritemprotocol/lastuseddate)

### Tracking Versions

- [var itemVersion: NSFileProviderItemVersion](/documentation/fileprovider/nsfileprovideritemprotocol/itemversion)
- [var versionIdentifier: Data?](/documentation/fileprovider/nsfileprovideritemprotocol/versionidentifier)
- [var isMostRecentVersionDownloaded: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/ismostrecentversiondownloaded)

### Monitoring File Transfers

- [var isUploading: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/isuploading)
- [var isUploaded: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/isuploaded)
- [var uploadingError: (any Error)?](/documentation/fileprovider/nsfileprovideritemprotocol/uploadingerror)
- [var isDownloading: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/isdownloading)
- [var isDownloaded: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/isdownloaded)
- [var downloadingError: (any Error)?](/documentation/fileprovider/nsfileprovideritemprotocol/downloadingerror)

### Sharing

- [var isShared: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/isshared)
- [var isSharedByCurrentUser: Bool](/documentation/fileprovider/nsfileprovideritemprotocol/issharedbycurrentuser)
- [var mostRecentEditorNameComponents: PersonNameComponents?](/documentation/fileprovider/nsfileprovideritemprotocol/mostrecenteditornamecomponents)
- [var ownerNameComponents: PersonNameComponents?](/documentation/fileprovider/nsfileprovideritemprotocol/ownernamecomponents)

### Managing Metadata

- [var extendedAttributes: [String : Data]](/documentation/fileprovider/nsfileprovideritemprotocol/extendedattributes)
- [var fileSystemFlags: NSFileProviderFileSystemFlags](/documentation/fileprovider/nsfileprovideritemprotocol/filesystemflags)
- [NSFileProviderFileSystemFlags](/documentation/fileprovider/nsfileproviderfilesystemflags)

#### Flags

- [static var userReadable: NSFileProviderFileSystemFlags](/documentation/fileprovider/nsfileproviderfilesystemflags/userreadable)
- [static var userWritable: NSFileProviderFileSystemFlags](/documentation/fileprovider/nsfileproviderfilesystemflags/userwritable)
- [static var userExecutable: NSFileProviderFileSystemFlags](/documentation/fileprovider/nsfileproviderfilesystemflags/userexecutable)
- [static var hidden: NSFileProviderFileSystemFlags](/documentation/fileprovider/nsfileproviderfilesystemflags/hidden)
- [static var pathExtensionHidden: NSFileProviderFileSystemFlags](/documentation/fileprovider/nsfileproviderfilesystemflags/pathextensionhidden)

#### Initializers

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileproviderfilesystemflags/init(rawvalue:))
- [var tagData: Data?](/documentation/fileprovider/nsfileprovideritemprotocol/tagdata)
- [var userInfo: [AnyHashable : Any]?](/documentation/fileprovider/nsfileprovideritemprotocol/userinfo)
- [var favoriteRank: NSNumber?](/documentation/fileprovider/nsfileprovideritemprotocol/favoriterank)
- [let NSFileProviderFavoriteRankUnranked: UInt64](/documentation/fileprovider/nsfileproviderfavoriterankunranked)
- [var typeAndCreator: NSFileProviderTypeAndCreator](/documentation/fileprovider/nsfileprovideritemprotocol/typeandcreator)
- [NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier)

### Constants

- [static let rootContainer: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/rootcontainer)
- [static let workingSet: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/workingset)
- [static let trashContainer: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/trashcontainer)

### Initializers

- [init(String)](/documentation/fileprovider/nsfileprovideritemidentifier/init(_:))
- [init(rawValue: String)](/documentation/fileprovider/nsfileprovideritemidentifier/init(rawvalue:))
- [NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities)

### Initializers

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovideritemcapabilities/init(rawvalue:))

### Constants

- [static var allowsAddingSubItems: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsaddingsubitems)
- [static var allowsContentEnumerating: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowscontentenumerating)
- [static var allowsDeleting: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsdeleting)
- [static var allowsEvicting: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsevicting)
- [static var allowsReading: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsreading)
- [static var allowsRenaming: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsrenaming)
- [static var allowsReparenting: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsreparenting)
- [static var allowsTrashing: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowstrashing)
- [static var allowsWriting: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowswriting)
- [static var allowsExcludingFromSync: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsexcludingfromsync)
- [static var allowsAll: NSFileProviderItemCapabilities](/documentation/fileprovider/nsfileprovideritemcapabilities/allowsall)
- [NSFileProviderTypeAndCreator](/documentation/fileprovider/nsfileprovidertypeandcreator)

### Creating Type and Creator Structures

- [init()](/documentation/fileprovider/nsfileprovidertypeandcreator/init())
- [init(type: OSType, creator: OSType)](/documentation/fileprovider/nsfileprovidertypeandcreator/init(type:creator:))

### Accessing Type and Creator Codes

- [var creator: OSType](/documentation/fileprovider/nsfileprovidertypeandcreator/creator)
- [var type: OSType](/documentation/fileprovider/nsfileprovidertypeandcreator/type)

## Cloud search

- [NSFileProviderSearching](/documentation/fileprovider/nsfileprovidersearching)

### Implementing search

- [func searchEnumerator(for: NSFileProviderStringSearchRequest) -> any NSFileProviderSearchEnumerator](/documentation/fileprovider/nsfileprovidersearching/searchenumerator(for:))
- [NSFileProviderStringSearchRequest](/documentation/fileprovider/nsfileproviderstringsearchrequest)

#### Working with request properties

- [var query: String](/documentation/fileprovider/nsfileproviderstringsearchrequest/query)

#### Instance Properties

- [var desiredNumberOfResults: Int](/documentation/fileprovider/nsfileproviderstringsearchrequest/desirednumberofresults)
- [NSFileProviderSearchEnumerator](/documentation/fileprovider/nsfileprovidersearchenumerator)

#### Providing search results

- [func enumerateSearchResults(for: any NSFileProviderSearchEnumerationObserver, startingAt: NSFileProviderPage?)](/documentation/fileprovider/nsfileprovidersearchenumerator/enumeratesearchresults(for:startingat:))
- [NSFileProviderSearchEnumerationObserver](/documentation/fileprovider/nsfileprovidersearchenumerationobserver)

##### Providing search results

- [func didEnumerate([any NSFileProviderSearchResult])](/documentation/fileprovider/nsfileprovidersearchenumerationobserver/didenumerate(_:))
- [NSFileProviderSearchResult](/documentation/fileprovider/nsfileprovidersearchresult)

###### Identifying the item

- [var itemIdentifier: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovidersearchresult/itemidentifier)
- [NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier)

###### Constants

- [static let rootContainer: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/rootcontainer)
- [static let workingSet: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/workingset)
- [static let trashContainer: NSFileProviderItemIdentifier](/documentation/fileprovider/nsfileprovideritemidentifier/trashcontainer)

###### Initializers

- [init(String)](/documentation/fileprovider/nsfileprovideritemidentifier/init(_:))
- [init(rawValue: String)](/documentation/fileprovider/nsfileprovideritemidentifier/init(rawvalue:))
- [var filename: String](/documentation/fileprovider/nsfileprovidersearchresult/filename)

###### Accessing file metadata

- [var creationDate: Date?](/documentation/fileprovider/nsfileprovidersearchresult/creationdate)
- [var contentModificationDate: Date?](/documentation/fileprovider/nsfileprovidersearchresult/contentmodificationdate)
- [var lastUsedDate: Date?](/documentation/fileprovider/nsfileprovidersearchresult/lastuseddate)
- [var contentType: UTType](/documentation/fileprovider/nsfileprovidersearchresult/contenttype)
- [var documentSize: NSNumber?](/documentation/fileprovider/nsfileprovidersearchresult/documentsize)

##### Ending enumeration

- [func finishEnumerating(upTo: NSFileProviderPage?)](/documentation/fileprovider/nsfileprovidersearchenumerationobserver/finishenumerating(upto:))
- [func finishEnumeratingWithError(any Error)](/documentation/fileprovider/nsfileprovidersearchenumerationobserver/finishenumeratingwitherror(_:))

##### Instance Properties

- [var maximumNumberOfResultsPerPage: Int](/documentation/fileprovider/nsfileprovidersearchenumerationobserver/maximumnumberofresultsperpage)
- [NSFileProviderPage](/documentation/fileprovider/nsfileproviderpage)

##### Page Constants

- [static let initialPageSortedByName: NSData](/documentation/fileprovider/nsfileproviderpage/initialpagesortedbyname)
- [static let initialPageSortedByDate: NSData](/documentation/fileprovider/nsfileproviderpage/initialpagesortedbydate)

##### Initializers

- [init(Data)](/documentation/fileprovider/nsfileproviderpage/init(_:))
- [init(rawValue: Data)](/documentation/fileprovider/nsfileproviderpage/init(rawvalue:))

#### Canceling a search

- [func invalidate()](/documentation/fileprovider/nsfileprovidersearchenumerator/invalidate())

## Domains

- [NSFileProviderDomain](/documentation/fileprovider/nsfileproviderdomain)

### Creating domains

- [init(identifier: NSFileProviderDomainIdentifier, displayName: String, pathRelativeToDocumentStorage: String)](/documentation/fileprovider/nsfileproviderdomain/init(identifier:displayname:pathrelativetodocumentstorage:))
- [init(identifier: NSFileProviderDomainIdentifier, displayName: String)](/documentation/fileprovider/nsfileproviderdomain/init(identifier:displayname:))
- [NSFileProviderDomainIdentifier](/documentation/fileprovider/nsfileproviderdomainidentifier)

#### Initializers

- [init(String)](/documentation/fileprovider/nsfileproviderdomainidentifier/init(_:))
- [init(rawValue: String)](/documentation/fileprovider/nsfileproviderdomainidentifier/init(rawvalue:))
- [init(displayName: String, userInfo: [AnyHashable : Any], volumeURL: URL?)](/documentation/fileprovider/nsfileproviderdomain/init(displayname:userinfo:volumeurl:))

### Accessing data

- [var displayName: String](/documentation/fileprovider/nsfileproviderdomain/displayname)
- [var identifier: NSFileProviderDomainIdentifier](/documentation/fileprovider/nsfileproviderdomain/identifier)
- [var isReplicated: Bool](/documentation/fileprovider/nsfileproviderdomain/isreplicated)
- [var backingStoreIdentity: Data?](/documentation/fileprovider/nsfileproviderdomain/backingstoreidentity)
- [var pathRelativeToDocumentStorage: String](/documentation/fileprovider/nsfileproviderdomain/pathrelativetodocumentstorage)
- [var isHidden: Bool](/documentation/fileprovider/nsfileproviderdomain/ishidden)
- [var userEnabled: Bool](/documentation/fileprovider/nsfileproviderdomain/userenabled)
- [var isDisconnected: Bool](/documentation/fileprovider/nsfileproviderdomain/isdisconnected)
- [var supportsSyncingTrash: Bool](/documentation/fileprovider/nsfileproviderdomain/supportssyncingtrash)
- [var userInfo: [AnyHashable : Any]?](/documentation/fileprovider/nsfileproviderdomain/userinfo)
- [var volumeUUID: UUID?](/documentation/fileprovider/nsfileproviderdomain/volumeuuid)

### Syncing Desktop and Documents folders

- [var replicatedKnownFolders: NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderdomain/replicatedknownfolders)
- [var supportedKnownFolders: NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderdomain/supportedknownfolders)
- [NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderknownfolders)

#### Identifying known folders

- [static var desktop: NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderknownfolders/desktop)
- [static var documents: NSFileProviderKnownFolders](/documentation/fileprovider/nsfileproviderknownfolders/documents)

#### Creating a known-folder identifier

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileproviderknownfolders/init(rawvalue:))

### Supporting search

- [var supportsStringSearchRequest: Bool](/documentation/fileprovider/nsfileproviderdomain/supportsstringsearchrequest)

### Testing

- [var testingModes: NSFileProviderDomain.TestingModes](/documentation/fileprovider/nsfileproviderdomain/testingmodes-swift.property)
- [NSFileProviderDomain.TestingModes](/documentation/fileprovider/nsfileproviderdomain/testingmodes-swift.struct)

#### Accessing Modes

- [static var alwaysEnabled: NSFileProviderDomain.TestingModes](/documentation/fileprovider/nsfileproviderdomain/testingmodes-swift.struct/alwaysenabled)
- [static var interactive: NSFileProviderDomain.TestingModes](/documentation/fileprovider/nsfileproviderdomain/testingmodes-swift.struct/interactive)

#### Creating Modes

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileproviderdomain/testingmodes-swift.struct/init(rawvalue:))

## Errors

- [NSFileProviderError](/documentation/fileprovider/nsfileprovidererror)

### Accessing error codes

- [NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/code)

#### Error codes

- [case filenameCollision](/documentation/fileprovider/nsfileprovidererror/code/filenamecollision)
- [case insufficientQuota](/documentation/fileprovider/nsfileprovidererror/code/insufficientquota)
- [case noSuchItem](/documentation/fileprovider/nsfileprovidererror/code/nosuchitem)
- [case notAuthenticated](/documentation/fileprovider/nsfileprovidererror/code/notauthenticated)
- [case serverUnreachable](/documentation/fileprovider/nsfileprovidererror/code/serverunreachable)
- [case syncAnchorExpired](/documentation/fileprovider/nsfileprovidererror/code/syncanchorexpired)
- [static var pageExpired: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/code/pageexpired)
- [case directoryNotEmpty](/documentation/fileprovider/nsfileprovidererror/code/directorynotempty)
- [case providerNotFound](/documentation/fileprovider/nsfileprovidererror/code/providernotfound)
- [case providerTranslocated](/documentation/fileprovider/nsfileprovidererror/code/providertranslocated)
- [case olderExtensionVersionRunning](/documentation/fileprovider/nsfileprovidererror/code/olderextensionversionrunning)
- [case newerExtensionVersionFound](/documentation/fileprovider/nsfileprovidererror/code/newerextensionversionfound)
- [case nonEvictable](/documentation/fileprovider/nsfileprovidererror/code/nonevictable)
- [case nonEvictableChildren](/documentation/fileprovider/nsfileprovidererror/code/nonevictablechildren)
- [case unsyncedEdits](/documentation/fileprovider/nsfileprovidererror/code/unsyncededits)
- [case cannotSynchronize](/documentation/fileprovider/nsfileprovidererror/code/cannotsynchronize)
- [case deletionRejected](/documentation/fileprovider/nsfileprovidererror/code/deletionrejected)
- [case versionNoLongerAvailable](/documentation/fileprovider/nsfileprovidererror/code/versionnolongeravailable)
- [case domainDisabled](/documentation/fileprovider/nsfileprovidererror/code/domaindisabled)
- [case excludedFromSync](/documentation/fileprovider/nsfileprovidererror/code/excludedfromsync)
- [case applicationExtensionNotFound](/documentation/fileprovider/nsfileprovidererror/code/applicationextensionnotfound)
- [case providerDomainNotFound](/documentation/fileprovider/nsfileprovidererror/code/providerdomainnotfound)
- [case providerDomainTemporarilyUnavailable](/documentation/fileprovider/nsfileprovidererror/code/providerdomaintemporarilyunavailable)

#### Enumeration Cases

- [case localVersionConflictingWithServer](/documentation/fileprovider/nsfileprovidererror/code/localversionconflictingwithserver)

#### Initializers

- [init?(rawValue: Int)](/documentation/fileprovider/nsfileprovidererror/code/init(rawvalue:))
- [static var filenameCollision: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/filenamecollision)
- [static var insufficientQuota: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/insufficientquota)
- [static var noSuchItem: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/nosuchitem)
- [static var notAuthenticated: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/notauthenticated)
- [static var pageExpired: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/pageexpired)
- [static var serverUnreachable: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/serverunreachable)
- [static var syncAnchorExpired: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/syncanchorexpired)
- [static var directoryNotEmpty: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/directorynotempty)
- [static var providerNotFound: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/providernotfound)
- [static var providerTranslocated: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/providertranslocated)
- [static var olderExtensionVersionRunning: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/olderextensionversionrunning)
- [static var newerExtensionVersionFound: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/newerextensionversionfound)
- [static var nonEvictable: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/nonevictable)
- [static var nonEvictableChildren: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/nonevictablechildren)
- [static var unsyncedEdits: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/unsyncededits)
- [static var cannotSynchronize: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/cannotsynchronize)
- [static var deletionRejected: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/deletionrejected)
- [static var versionNoLongerAvailable: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/versionnolongeravailable)
- [static var domainDisabled: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/domaindisabled)
- [static var excludedFromSync: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/excludedfromsync)
- [static var applicationExtensionNotFound: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/applicationextensionnotfound)
- [static var providerDomainNotFound: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/providerdomainnotfound)
- [static var providerDomainTemporarilyUnavailable: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/providerdomaintemporarilyunavailable)

### Type Properties

- [static var errorDomain: String](/documentation/fileprovider/nsfileprovidererror/errordomain)
- [static var localVersionConflictingWithServer: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/localversionconflictingwithserver)
- [NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/code)

### Error codes

- [case filenameCollision](/documentation/fileprovider/nsfileprovidererror/code/filenamecollision)
- [case insufficientQuota](/documentation/fileprovider/nsfileprovidererror/code/insufficientquota)
- [case noSuchItem](/documentation/fileprovider/nsfileprovidererror/code/nosuchitem)
- [case notAuthenticated](/documentation/fileprovider/nsfileprovidererror/code/notauthenticated)
- [case serverUnreachable](/documentation/fileprovider/nsfileprovidererror/code/serverunreachable)
- [case syncAnchorExpired](/documentation/fileprovider/nsfileprovidererror/code/syncanchorexpired)
- [static var pageExpired: NSFileProviderError.Code](/documentation/fileprovider/nsfileprovidererror/code/pageexpired)
- [case directoryNotEmpty](/documentation/fileprovider/nsfileprovidererror/code/directorynotempty)
- [case providerNotFound](/documentation/fileprovider/nsfileprovidererror/code/providernotfound)
- [case providerTranslocated](/documentation/fileprovider/nsfileprovidererror/code/providertranslocated)
- [case olderExtensionVersionRunning](/documentation/fileprovider/nsfileprovidererror/code/olderextensionversionrunning)
- [case newerExtensionVersionFound](/documentation/fileprovider/nsfileprovidererror/code/newerextensionversionfound)
- [case nonEvictable](/documentation/fileprovider/nsfileprovidererror/code/nonevictable)
- [case nonEvictableChildren](/documentation/fileprovider/nsfileprovidererror/code/nonevictablechildren)
- [case unsyncedEdits](/documentation/fileprovider/nsfileprovidererror/code/unsyncededits)
- [case cannotSynchronize](/documentation/fileprovider/nsfileprovidererror/code/cannotsynchronize)
- [case deletionRejected](/documentation/fileprovider/nsfileprovidererror/code/deletionrejected)
- [case versionNoLongerAvailable](/documentation/fileprovider/nsfileprovidererror/code/versionnolongeravailable)
- [case domainDisabled](/documentation/fileprovider/nsfileprovidererror/code/domaindisabled)
- [case excludedFromSync](/documentation/fileprovider/nsfileprovidererror/code/excludedfromsync)
- [case applicationExtensionNotFound](/documentation/fileprovider/nsfileprovidererror/code/applicationextensionnotfound)
- [case providerDomainNotFound](/documentation/fileprovider/nsfileprovidererror/code/providerdomainnotfound)
- [case providerDomainTemporarilyUnavailable](/documentation/fileprovider/nsfileprovidererror/code/providerdomaintemporarilyunavailable)

### Enumeration Cases

- [case localVersionConflictingWithServer](/documentation/fileprovider/nsfileprovidererror/code/localversionconflictingwithserver)

### Initializers

- [init?(rawValue: Int)](/documentation/fileprovider/nsfileprovidererror/code/init(rawvalue:))
- [let NSFileProviderErrorDomain: String](/documentation/fileprovider/nsfileprovidererrordomain)
- [let NSFileProviderErrorItemKey: String](/documentation/fileprovider/nsfileprovidererroritemkey)
- [let NSFileProviderErrorNonExistentItemIdentifierKey: String](/documentation/fileprovider/nsfileprovidererrornonexistentitemidentifierkey)
- [let NSFileProviderErrorCollidingItemKey: String](/documentation/fileprovider/nsfileprovidererrorcollidingitemkey)

## Data export

- [Exporting file provider metrics data](/documentation/fileprovider/exporting-file-provider-metrics-data)

## Structures

- [NSFileProviderUserInfoKey](/documentation/fileprovider/nsfileprovideruserinfokey)

### Initializers

- [init(String)](/documentation/fileprovider/nsfileprovideruserinfokey/init(_:))
- [init(rawValue: String)](/documentation/fileprovider/nsfileprovideruserinfokey/init(rawvalue:))

### Type Properties

- [static let experimentID: NSFileProviderUserInfoKey](/documentation/fileprovider/nsfileprovideruserinfokey/experimentid)
- [NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason)

### Reasons

- [static var unknown: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/unknown)
- [static var nonEncrypted: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/nonencrypted)
- [static var readOnly: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/readonly)
- [static var network: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/network)
- [static var quarantined: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/quarantined)

### Initializers

- [init(rawValue: UInt)](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/init(rawvalue:))

### Type Properties

- [static var nonAPFS: NSFileProviderVolumeUnsupportedReason](/documentation/fileprovider/nsfileprovidervolumeunsupportedreason/nonapfs)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
