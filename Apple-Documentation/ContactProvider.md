# ContactProvider Documentation

Source: https://sosumi.ai/documentation/contactprovider

---
title: ContactProvider
source: https://developer.apple.com/documentation/contactprovider
timestamp: 2026-02-13T18:55:05.933Z
---

## Creating a contact provider extension

- [ContactProviderExtension](/documentation/contactprovider/contactproviderextension)

### Configuring an extension

- [func configure(for: any ContactProviderDomain)](/documentation/contactprovider/contactproviderextension/configure(for:))

### Managing the extension life cycle

- [func invalidate() async throws](/documentation/contactprovider/contactproviderextension/invalidate())

## Managing an extension in an app

- [ContactProviderManager](/documentation/contactprovider/contactprovidermanager)

### Creating a contact provider manager

- [init(domainIdentifier: String) throws](/documentation/contactprovider/contactprovidermanager/init(domainidentifier:))

### Invoking the app extension

- [func signalEnumerator(for: ContactItem.Identifier) async throws](/documentation/contactprovider/contactprovidermanager/signalenumerator(for:))

### Managing the contact provider manager life cycle

- [func invalidate() async throws](/documentation/contactprovider/contactprovidermanager/invalidate())

### Managing the domain

- [var domain: any ContactProviderDomain](/documentation/contactprovider/contactprovidermanager/domain)
- [func enable() async throws](/documentation/contactprovider/contactprovidermanager/enable())
- [var isEnabled: Bool](/documentation/contactprovider/contactprovidermanager/isenabled)
- [func reset() async throws](/documentation/contactprovider/contactprovidermanager/reset())
- [func disable() async throws](/documentation/contactprovider/contactprovidermanager/disable())

## Working with domains

- [ContactProviderDomain](/documentation/contactprovider/contactproviderdomain)

### Identifying the domain

- [var displayName: String](/documentation/contactprovider/contactproviderdomain/displayname)
- [var identifier: String](/documentation/contactprovider/contactproviderdomain/identifier)

### Providing custom domain data

- [var userInfo: Dictionary<String, Any>](/documentation/contactprovider/contactproviderdomain/userinfo)
- [DefaultContactProviderDomain](/documentation/contactprovider/defaultcontactproviderdomain)

### Creating a default domain

- [init()](/documentation/contactprovider/defaultcontactproviderdomain/init())

### Identifying the domain

- [let displayName: String](/documentation/contactprovider/defaultcontactproviderdomain/displayname)

### Using the default domain identifier

- [static let identifier: String](/documentation/contactprovider/defaultcontactproviderdomain/identifier)

## Providing contacts

- [ContactItem](/documentation/contactprovider/contactitem)

### Handling item type

- [case contact(CNMutableContact, ContactItem.Identifier)](/documentation/contactprovider/contactitem/contact(_:_:))

### Identifying the item

- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

#### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

#### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

#### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)
- [ContactItemEnumerating](/documentation/contactprovider/contactitemenumerating)

### Providing an enumeration

- [func enumerator(for: ContactItem.Identifier) -> any ContactItemEnumerator](/documentation/contactprovider/contactitemenumerating/enumerator(for:))
- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

#### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

#### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

#### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)
- [ContactItemEnumerator](/documentation/contactprovider/contactitemenumerator)

#### Enumerating contact items

- [func enumerateContent(in: ContactItemPage, for: any ContactItemContentObserver) async](/documentation/contactprovider/contactitemenumerator/enumeratecontent(in:for:))
- [ContactItemPage](/documentation/contactprovider/contactitempage)

##### Creating a contact item page

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitempage/init(generationmarker:offset:))

##### Supporting paging

- [var generationMarker: Data](/documentation/contactprovider/contactitempage/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitempage/offset)
- [static let initialPage: ContactItemPage](/documentation/contactprovider/contactitempage/initialpage)
- [ContactItemContentObserver](/documentation/contactprovider/contactitemcontentobserver)

##### Providing contact items

- [func didEnumerate([ContactItem])](/documentation/contactprovider/contactitemcontentobserver/didenumerate(_:))
- [ContactItem](/documentation/contactprovider/contactitem)

###### Handling item type

- [case contact(CNMutableContact, ContactItem.Identifier)](/documentation/contactprovider/contactitem/contact(_:_:))

###### Identifying the item

- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

###### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

###### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

###### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)

##### Ending enumeration

- [func didFinishEnumeratingContent(upTo: Data)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingcontent(upto:))
- [func didFinishEnumeratingPage(upTo: ContactItemPage)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingpage(upto:))
- [ContactItemPage](/documentation/contactprovider/contactitempage)

###### Creating a contact item page

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitempage/init(generationmarker:offset:))

###### Supporting paging

- [var generationMarker: Data](/documentation/contactprovider/contactitempage/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitempage/offset)
- [static let initialPage: ContactItemPage](/documentation/contactprovider/contactitempage/initialpage)
- [func didFinishEnumeratingContentWithError(any Error)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingcontentwitherror(_:))

##### Optimizing enumeration

- [var suggestedPageSize: Int](/documentation/contactprovider/contactitemcontentobserver/suggestedpagesize)

#### Enumerating item changes

- [func enumerateChanges(startingAt: ContactItemSyncAnchor, for: any ContactItemChangeObserver) async](/documentation/contactprovider/contactitemenumerator/enumeratechanges(startingat:for:))
- [ContactItemSyncAnchor](/documentation/contactprovider/contactitemsyncanchor)

##### Creating a sync anchor

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitemsyncanchor/init(generationmarker:offset:))

##### Inspecting sync anchor properties

- [var generationMarker: Data](/documentation/contactprovider/contactitemsyncanchor/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitemsyncanchor/offset)
- [ContactItemChangeObserver](/documentation/contactprovider/contactitemchangeobserver)

##### Providing change data

- [func didUpdate([ContactItem])](/documentation/contactprovider/contactitemchangeobserver/didupdate(_:))
- [ContactItem](/documentation/contactprovider/contactitem)

###### Handling item type

- [case contact(CNMutableContact, ContactItem.Identifier)](/documentation/contactprovider/contactitem/contact(_:_:))

###### Identifying the item

- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

###### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

###### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

###### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)
- [func didDelete([ContactItem.Identifier])](/documentation/contactprovider/contactitemchangeobserver/diddelete(_:))
- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

###### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

###### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

###### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)

##### Ending enumeration

- [func didFinishEnumeratingChanges(upTo: ContactItemSyncAnchor, moreComing: Bool)](/documentation/contactprovider/contactitemchangeobserver/didfinishenumeratingchanges(upto:morecoming:))
- [ContactItemSyncAnchor](/documentation/contactprovider/contactitemsyncanchor)

###### Creating a sync anchor

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitemsyncanchor/init(generationmarker:offset:))

###### Inspecting sync anchor properties

- [var generationMarker: Data](/documentation/contactprovider/contactitemsyncanchor/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitemsyncanchor/offset)
- [func didFinishEnumeratingChangesWithError(any Error)](/documentation/contactprovider/contactitemchangeobserver/didfinishenumeratingchangeswitherror(_:))

##### Optimizing observer batching

- [var suggestedBatchSize: Int](/documentation/contactprovider/contactitemchangeobserver/suggestedbatchsize)

#### Managing enumerator life cycle

- [func invalidate() async](/documentation/contactprovider/contactitemenumerator/invalidate())
- [ContactItemEnumerator](/documentation/contactprovider/contactitemenumerator)

### Enumerating contact items

- [func enumerateContent(in: ContactItemPage, for: any ContactItemContentObserver) async](/documentation/contactprovider/contactitemenumerator/enumeratecontent(in:for:))
- [ContactItemPage](/documentation/contactprovider/contactitempage)

#### Creating a contact item page

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitempage/init(generationmarker:offset:))

#### Supporting paging

- [var generationMarker: Data](/documentation/contactprovider/contactitempage/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitempage/offset)
- [static let initialPage: ContactItemPage](/documentation/contactprovider/contactitempage/initialpage)
- [ContactItemContentObserver](/documentation/contactprovider/contactitemcontentobserver)

#### Providing contact items

- [func didEnumerate([ContactItem])](/documentation/contactprovider/contactitemcontentobserver/didenumerate(_:))
- [ContactItem](/documentation/contactprovider/contactitem)

##### Handling item type

- [case contact(CNMutableContact, ContactItem.Identifier)](/documentation/contactprovider/contactitem/contact(_:_:))

##### Identifying the item

- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

###### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

###### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

###### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)

#### Ending enumeration

- [func didFinishEnumeratingContent(upTo: Data)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingcontent(upto:))
- [func didFinishEnumeratingPage(upTo: ContactItemPage)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingpage(upto:))
- [ContactItemPage](/documentation/contactprovider/contactitempage)

##### Creating a contact item page

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitempage/init(generationmarker:offset:))

##### Supporting paging

- [var generationMarker: Data](/documentation/contactprovider/contactitempage/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitempage/offset)
- [static let initialPage: ContactItemPage](/documentation/contactprovider/contactitempage/initialpage)
- [func didFinishEnumeratingContentWithError(any Error)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingcontentwitherror(_:))

#### Optimizing enumeration

- [var suggestedPageSize: Int](/documentation/contactprovider/contactitemcontentobserver/suggestedpagesize)

### Enumerating item changes

- [func enumerateChanges(startingAt: ContactItemSyncAnchor, for: any ContactItemChangeObserver) async](/documentation/contactprovider/contactitemenumerator/enumeratechanges(startingat:for:))
- [ContactItemSyncAnchor](/documentation/contactprovider/contactitemsyncanchor)

#### Creating a sync anchor

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitemsyncanchor/init(generationmarker:offset:))

#### Inspecting sync anchor properties

- [var generationMarker: Data](/documentation/contactprovider/contactitemsyncanchor/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitemsyncanchor/offset)
- [ContactItemChangeObserver](/documentation/contactprovider/contactitemchangeobserver)

#### Providing change data

- [func didUpdate([ContactItem])](/documentation/contactprovider/contactitemchangeobserver/didupdate(_:))
- [ContactItem](/documentation/contactprovider/contactitem)

##### Handling item type

- [case contact(CNMutableContact, ContactItem.Identifier)](/documentation/contactprovider/contactitem/contact(_:_:))

##### Identifying the item

- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

###### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

###### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

###### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)
- [func didDelete([ContactItem.Identifier])](/documentation/contactprovider/contactitemchangeobserver/diddelete(_:))
- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

##### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

##### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

##### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)

#### Ending enumeration

- [func didFinishEnumeratingChanges(upTo: ContactItemSyncAnchor, moreComing: Bool)](/documentation/contactprovider/contactitemchangeobserver/didfinishenumeratingchanges(upto:morecoming:))
- [ContactItemSyncAnchor](/documentation/contactprovider/contactitemsyncanchor)

##### Creating a sync anchor

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitemsyncanchor/init(generationmarker:offset:))

##### Inspecting sync anchor properties

- [var generationMarker: Data](/documentation/contactprovider/contactitemsyncanchor/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitemsyncanchor/offset)
- [func didFinishEnumeratingChangesWithError(any Error)](/documentation/contactprovider/contactitemchangeobserver/didfinishenumeratingchangeswitherror(_:))

#### Optimizing observer batching

- [var suggestedBatchSize: Int](/documentation/contactprovider/contactitemchangeobserver/suggestedbatchsize)

### Managing enumerator life cycle

- [func invalidate() async](/documentation/contactprovider/contactitemenumerator/invalidate())

## Receiving contacts

- [ContactItemContentObserver](/documentation/contactprovider/contactitemcontentobserver)

### Providing contact items

- [func didEnumerate([ContactItem])](/documentation/contactprovider/contactitemcontentobserver/didenumerate(_:))
- [ContactItem](/documentation/contactprovider/contactitem)

#### Handling item type

- [case contact(CNMutableContact, ContactItem.Identifier)](/documentation/contactprovider/contactitem/contact(_:_:))

#### Identifying the item

- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

##### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

##### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

##### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)

### Ending enumeration

- [func didFinishEnumeratingContent(upTo: Data)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingcontent(upto:))
- [func didFinishEnumeratingPage(upTo: ContactItemPage)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingpage(upto:))
- [ContactItemPage](/documentation/contactprovider/contactitempage)

#### Creating a contact item page

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitempage/init(generationmarker:offset:))

#### Supporting paging

- [var generationMarker: Data](/documentation/contactprovider/contactitempage/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitempage/offset)
- [static let initialPage: ContactItemPage](/documentation/contactprovider/contactitempage/initialpage)
- [func didFinishEnumeratingContentWithError(any Error)](/documentation/contactprovider/contactitemcontentobserver/didfinishenumeratingcontentwitherror(_:))

### Optimizing enumeration

- [var suggestedPageSize: Int](/documentation/contactprovider/contactitemcontentobserver/suggestedpagesize)
- [ContactItemChangeObserver](/documentation/contactprovider/contactitemchangeobserver)

### Providing change data

- [func didUpdate([ContactItem])](/documentation/contactprovider/contactitemchangeobserver/didupdate(_:))
- [ContactItem](/documentation/contactprovider/contactitem)

#### Handling item type

- [case contact(CNMutableContact, ContactItem.Identifier)](/documentation/contactprovider/contactitem/contact(_:_:))

#### Identifying the item

- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

##### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

##### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

##### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)
- [func didDelete([ContactItem.Identifier])](/documentation/contactprovider/contactitemchangeobserver/diddelete(_:))
- [ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier)

#### Creating a contact item identifier

- [init(String)](/documentation/contactprovider/contactitem/identifier/init(_:))

#### Inspecting identifier properties

- [let value: String](/documentation/contactprovider/contactitem/identifier/value)

#### Accessing the root container

- [static let rootContainer: ContactItem.Identifier](/documentation/contactprovider/contactitem/identifier/rootcontainer)

### Ending enumeration

- [func didFinishEnumeratingChanges(upTo: ContactItemSyncAnchor, moreComing: Bool)](/documentation/contactprovider/contactitemchangeobserver/didfinishenumeratingchanges(upto:morecoming:))
- [ContactItemSyncAnchor](/documentation/contactprovider/contactitemsyncanchor)

#### Creating a sync anchor

- [init(generationMarker: Data, offset: Int)](/documentation/contactprovider/contactitemsyncanchor/init(generationmarker:offset:))

#### Inspecting sync anchor properties

- [var generationMarker: Data](/documentation/contactprovider/contactitemsyncanchor/generationmarker)
- [var offset: Int](/documentation/contactprovider/contactitemsyncanchor/offset)
- [func didFinishEnumeratingChangesWithError(any Error)](/documentation/contactprovider/contactitemchangeobserver/didfinishenumeratingchangeswitherror(_:))

### Optimizing observer batching

- [var suggestedBatchSize: Int](/documentation/contactprovider/contactitemchangeobserver/suggestedbatchsize)

## Supporting types

- [ContactProviderError](/documentation/contactprovider/contactprovidererror)

### Availability errors

- [case featureNotAvailable](/documentation/contactprovider/contactprovidererror/featurenotavailable)
- [case deniedByUser](/documentation/contactprovider/contactprovidererror/deniedbyuser)

### Configuration errors

- [case extensionNotFound](/documentation/contactprovider/contactprovidererror/extensionnotfound)

### Capacity errors

- [case itemsLimitReached](/documentation/contactprovider/contactprovidererror/itemslimitreached)

### Enumeration errors

- [case cannotEnumerate](/documentation/contactprovider/contactprovidererror/cannotenumerate)
- [case enumerationTimeout](/documentation/contactprovider/contactprovidererror/enumerationtimeout)

### Expiration errors

- [case pageExpired](/documentation/contactprovider/contactprovidererror/pageexpired)
- [case changeAnchorExpired](/documentation/contactprovider/contactprovidererror/changeanchorexpired)

### Invalidation errors

- [case extensionInvalidated](/documentation/contactprovider/contactprovidererror/extensioninvalidated)
- [case extensionInvalidateTimeout](/documentation/contactprovider/contactprovidererror/extensioninvalidatetimeout)

### Enumeration Cases

- [case domainNotRegistered](/documentation/contactprovider/contactprovidererror/domainnotregistered)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
