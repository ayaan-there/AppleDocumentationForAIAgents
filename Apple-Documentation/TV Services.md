# TV Services Documentation

Source: https://sosumi.ai/documentation/tvservices

---
title: TV Services
source: https://developer.apple.com/documentation/tvservices
timestamp: 2026-02-13T19:03:17.322Z
---

## Top shelf app extensions

- [Building a Full Screen Top Shelf Extension](/documentation/tvservices/building-a-full-screen-top-shelf-extension)
- [TVTopShelfContentProvider](/documentation/tvservices/tvtopshelfcontentprovider)

### Providing the Top Shelf Content

- [func loadTopShelfContent(completionHandler: ((any TVTopShelfContent)?) -> Void)](/documentation/tvservices/tvtopshelfcontentprovider/loadtopshelfcontent(completionhandler:))

### Updating Your Content

- [class func topShelfContentDidChange()](/documentation/tvservices/tvtopshelfcontentprovider/topshelfcontentdidchange())
- [Legacy Extension](/documentation/tvservices/legacy-extension)

### Extension

- [TVTopShelfProvider](/documentation/tvservices/tvtopshelfprovider)

#### Implementing TV Services Extension Properties

- [var topShelfItems: [TVContentItem]](/documentation/tvservices/tvtopshelfprovider/topshelfitems)
- [var topShelfStyle: TVTopShelfContentStyle](/documentation/tvservices/tvtopshelfprovider/topshelfstyle)
- [TVTopShelfContentStyle](/documentation/tvservices/tvtopshelfcontentstyle)

##### Constants

- [case inset](/documentation/tvservices/tvtopshelfcontentstyle/inset)
- [case sectioned](/documentation/tvservices/tvtopshelfcontentstyle/sectioned)

##### Initializers

- [init?(rawValue: Int)](/documentation/tvservices/tvtopshelfcontentstyle/init(rawvalue:))

#### Notifying the System of Changes

- [static let TVTopShelfItemsDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/tvtopshelfitemsdidchange)

### Content

- [TVContentItem](/documentation/tvservices/tvcontentitem)

#### Initializing a Content Item

- [init(contentIdentifier: TVContentIdentifier)](/documentation/tvservices/tvcontentitem/init(contentidentifier:))
- [init?(coder: NSCoder)](/documentation/tvservices/tvcontentitem/init(coder:))

#### Reading a Content Item’s Identifier

- [var contentIdentifier: TVContentIdentifier](/documentation/tvservices/tvcontentitem/contentidentifier)

#### Inspecting the General Display Properties

- [var badgeCount: NSNumber?](/documentation/tvservices/tvcontentitem/badgecount)
- [var title: String?](/documentation/tvservices/tvcontentitem/title)
- [var topShelfItems: [TVContentItem]?](/documentation/tvservices/tvcontentitem/topshelfitems)

#### Accessing Image Resources

- [var imageURL: URL?](/documentation/tvservices/tvcontentitem/imageurl)
- [func imageURL(forTraits: TVContentItemImageTrait) -> URL?](/documentation/tvservices/tvcontentitem/imageurl(fortraits:))
- [func setImageURL(URL?, forTraits: TVContentItemImageTrait)](/documentation/tvservices/tvcontentitem/setimageurl(_:fortraits:))
- [TVContentItemImageTrait](/documentation/tvservices/tvcontentitemimagetrait)

##### Traits

- [static var screenScale1x: TVContentItemImageTrait](/documentation/tvservices/tvcontentitemimagetrait/screenscale1x)
- [static var screenScale2x: TVContentItemImageTrait](/documentation/tvservices/tvcontentitemimagetrait/screenscale2x)
- [static var userInterfaceStyleDark: TVContentItemImageTrait](/documentation/tvservices/tvcontentitemimagetrait/userinterfacestyledark)
- [static var userInterfaceStyleLight: TVContentItemImageTrait](/documentation/tvservices/tvcontentitemimagetrait/userinterfacestylelight)

##### Initializers

- [init(rawValue: UInt)](/documentation/tvservices/tvcontentitemimagetrait/init(rawvalue:))

#### Inspecting the Content Properties

- [var creationDate: Date?](/documentation/tvservices/tvcontentitem/creationdate)
- [var duration: NSNumber?](/documentation/tvservices/tvcontentitem/duration)
- [var expirationDate: Date?](/documentation/tvservices/tvcontentitem/expirationdate)
- [var imageShape: TVContentItemImageShape](/documentation/tvservices/tvcontentitem/imageshape)
- [TVContentItemImageShape](/documentation/tvservices/tvcontentitemimageshape)

##### Constants

- [case none](/documentation/tvservices/tvcontentitemimageshape/none)
- [case poster](/documentation/tvservices/tvcontentitemimageshape/poster)
- [case square](/documentation/tvservices/tvcontentitemimageshape/square)
- [case SDTV](/documentation/tvservices/tvcontentitemimageshape/sdtv)
- [case HDTV](/documentation/tvservices/tvcontentitemimageshape/hdtv)
- [case wide](/documentation/tvservices/tvcontentitemimageshape/wide)
- [case extraWide](/documentation/tvservices/tvcontentitemimageshape/extrawide)

##### Initializers

- [init?(rawValue: Int)](/documentation/tvservices/tvcontentitemimageshape/init(rawvalue:))

#### Inspecting the Playback Properties

- [var currentPosition: NSNumber?](/documentation/tvservices/tvcontentitem/currentposition)
- [var hasPlayedToEnd: NSNumber?](/documentation/tvservices/tvcontentitem/hasplayedtoend)
- [var lastAccessedDate: Date?](/documentation/tvservices/tvcontentitem/lastaccesseddate)

#### Inspecting the Application Launch Properties

- [var displayURL: URL?](/documentation/tvservices/tvcontentitem/displayurl)
- [var playURL: URL?](/documentation/tvservices/tvcontentitem/playurl)
- [TVContentIdentifier](/documentation/tvservices/tvcontentidentifier)

#### Initializing a Content Identifier

- [init(identifier: String, container: TVContentIdentifier?)](/documentation/tvservices/tvcontentidentifier/init(identifier:container:))
- [init?(coder: NSCoder)](/documentation/tvservices/tvcontentidentifier/init(coder:))

#### Inspecting an Identifier’s Contents

- [var identifier: String](/documentation/tvservices/tvcontentidentifier/identifier)
- [var container: TVContentIdentifier?](/documentation/tvservices/tvcontentidentifier/container)
- [func TVTopShelfImageSize(shape: TVContentItemImageShape, style: TVTopShelfContentStyle) -> CGSize](/documentation/tvservices/tvtopshelfimagesize(shape:style:))

## Carousel content

- [TVTopShelfCarouselItem](/documentation/tvservices/tvtopshelfcarouselitem)

### Specifying the Item Details

- [var contextTitle: String?](/documentation/tvservices/tvtopshelfcarouselitem/contexttitle)
- [var summary: String?](/documentation/tvservices/tvtopshelfcarouselitem/summary)
- [var genre: String?](/documentation/tvservices/tvtopshelfcarouselitem/genre)
- [var duration: TimeInterval](/documentation/tvservices/tvtopshelfcarouselitem/duration)
- [var creationDate: Date?](/documentation/tvservices/tvtopshelfcarouselitem/creationdate)

### Specifying the Content Previews

- [var cinemagraphURL: URL?](/documentation/tvservices/tvtopshelfcarouselitem/cinemagraphurl)
- [var previewVideoURL: URL?](/documentation/tvservices/tvtopshelfcarouselitem/previewvideourl)

### Adding Media Badges

- [var mediaOptions: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.property)
- [TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct)

#### Media Options

- [static var videoResolutionHD: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/videoresolutionhd)
- [static var videoResolution4K: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/videoresolution4k)
- [static var videoColorSpaceHDR: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/videocolorspacehdr)
- [static var videoColorSpaceDolbyVision: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/videocolorspacedolbyvision)
- [static var audioDolbyAtmos: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/audiodolbyatmos)
- [static var audioTranscriptionClosedCaptioning: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/audiotranscriptionclosedcaptioning)
- [static var audioTranscriptionSDH: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/audiotranscriptionsdh)
- [static var audioDescription: TVTopShelfCarouselItem.MediaOptions](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/audiodescription)

#### Initializers

- [init(rawValue: UInt)](/documentation/tvservices/tvtopshelfcarouselitem/mediaoptions-swift.struct/init(rawvalue:))

### Adding Custom Attributes

- [var namedAttributes: [TVTopShelfNamedAttribute]](/documentation/tvservices/tvtopshelfcarouselitem/namedattributes)
- [TVTopShelfNamedAttribute](/documentation/tvservices/tvtopshelfnamedattribute)

#### Creating a Named Attribute

- [init(name: String, values: [String])](/documentation/tvservices/tvtopshelfnamedattribute/init(name:values:))

#### Getting the Name and Value

- [var name: String](/documentation/tvservices/tvtopshelfnamedattribute/name)
- [var values: [String]](/documentation/tvservices/tvtopshelfnamedattribute/values)
- [TVTopShelfCarouselContent](/documentation/tvservices/tvtopshelfcarouselcontent)

### Creating a Carousel Content Object

- [init(style: TVTopShelfCarouselContent.Style, items: [TVTopShelfCarouselItem])](/documentation/tvservices/tvtopshelfcarouselcontent/init(style:items:))

### Accessing the Carousel Items

- [var items: [TVTopShelfCarouselItem]](/documentation/tvservices/tvtopshelfcarouselcontent/items)

### Getting the Item Style

- [var style: TVTopShelfCarouselContent.Style](/documentation/tvservices/tvtopshelfcarouselcontent/style-swift.property)
- [TVTopShelfCarouselContent.Style](/documentation/tvservices/tvtopshelfcarouselcontent/style-swift.enum)

#### Styles

- [case actions](/documentation/tvservices/tvtopshelfcarouselcontent/style-swift.enum/actions)
- [case details](/documentation/tvservices/tvtopshelfcarouselcontent/style-swift.enum/details)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvservices/tvtopshelfcarouselcontent/style-swift.enum/init(rawvalue:))

## Sectioned and inset content

- [TVTopShelfSectionedItem](/documentation/tvservices/tvtopshelfsectioneditem)

### Setting the Image Shape

- [var imageShape: TVTopShelfSectionedItem.ImageShape](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.property)
- [TVTopShelfSectionedItem.ImageShape](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum)

#### Image Shapes

- [case square](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/square)
- [case poster](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/poster)
- [case hdtv](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/hdtv)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/init(rawvalue:))

### Setting the Playback Progress

- [var playbackProgress: Double](/documentation/tvservices/tvtopshelfsectioneditem/playbackprogress)
- [TVTopShelfItemCollection](/documentation/tvservices/tvtopshelfitemcollection)

### Creating an Item Collection

- [init(items: [Item])](/documentation/tvservices/tvtopshelfitemcollection/init(items:))

### Getting the Items

- [var items: [Item]](/documentation/tvservices/tvtopshelfitemcollection/items)
- [TVTopShelfSectionedContent](/documentation/tvservices/tvtopshelfsectionedcontent)

### Creating a Sectioned Content Object

- [init(sections: [TVTopShelfItemCollection<TVTopShelfSectionedItem>])](/documentation/tvservices/tvtopshelfsectionedcontent/init(sections:))

### Getting the Sections

- [var sections: [TVTopShelfItemCollection<TVTopShelfSectionedItem>]](/documentation/tvservices/tvtopshelfsectionedcontent/sections)

### Getting the Image Size Information

- [class func imageSize(for: TVTopShelfSectionedItem.ImageShape) -> CGSize](/documentation/tvservices/tvtopshelfsectionedcontent/imagesize(for:))
- [TVTopShelfSectionedItem.ImageShape](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum)

#### Image Shapes

- [case square](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/square)
- [case poster](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/poster)
- [case hdtv](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/hdtv)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvservices/tvtopshelfsectioneditem/imageshape-swift.enum/init(rawvalue:))
- [TVTopShelfInsetContent](/documentation/tvservices/tvtopshelfinsetcontent)

### Creating an Inset Content Object

- [init(items: [TVTopShelfItem])](/documentation/tvservices/tvtopshelfinsetcontent/init(items:))

### Getting the Items

- [var items: [TVTopShelfItem]](/documentation/tvservices/tvtopshelfinsetcontent/items)

### Getting the Image Size

- [class var imageSize: CGSize](/documentation/tvservices/tvtopshelfinsetcontent/imagesize)

## Multiple users

- [Personalizing Your App for Each User on Apple TV](/documentation/tvservices/personalizing-your-app-for-each-user-on-apple-tv)
- [Supporting Multiple Users in Your tvOS App](/documentation/tvservices/supporting-multiple-users-in-your-tvos-app)
- [Mapping Apple TV users to app profiles](/documentation/tvservices/mapping-apple-tv-users-to-app-profiles)
- [TVUserManager](/documentation/tvservices/tvusermanager)

### Retaining profile selection for the current Apple TV account

- [var shouldStorePreferencesForCurrentUser: Bool](/documentation/tvservices/tvusermanager/shouldstorepreferencesforcurrentuser)

### Deprecated symbols

- [var currentUserIdentifier: TVUserIdentifier?](/documentation/tvservices/tvusermanager/currentuseridentifier)
- [class let currentUserIdentifierDidChangeNotification: NSNotification.Name](/documentation/tvservices/tvusermanager/currentuseridentifierdidchangenotification)
- [func presentProfilePreferencePanel(currentSettings: [TVUserIdentifier : TVAppProfileDescriptor], availableProfiles: [TVAppProfileDescriptor], completion: ([TVUserIdentifier : TVAppProfileDescriptor]) -> Void)](/documentation/tvservices/tvusermanager/presentprofilepreferencepanel(currentsettings:availableprofiles:completion:))
- [func shouldStorePreferenceForCurrentUser(to: TVAppProfileDescriptor, completion: (Bool) -> Void)](/documentation/tvservices/tvusermanager/shouldstorepreferenceforcurrentuser(to:completion:))
- [TVAppProfileDescriptor](/documentation/tvservices/tvappprofiledescriptor)

#### Creating a Profile Descriptor

- [init(name: String)](/documentation/tvservices/tvappprofiledescriptor/init(name:))

#### Getting the Profile Name

- [var name: String](/documentation/tvservices/tvappprofiledescriptor/name)
- [TVUserIdentifier](/documentation/tvservices/tvuseridentifier)
- [var userIdentifiersForCurrentProfile: [TVUserIdentifier]](/documentation/tvservices/tvusermanager/useridentifiersforcurrentprofile)

## Channel guide

- [Providing Channel Navigation](/documentation/tvservices/providing-channel-navigation)
- [let TVUserActivityTypeBrowsingChannelGuide: String](/documentation/tvservices/tvuseractivitytypebrowsingchannelguide)

## Common types

- [TVTopShelfItem](/documentation/tvservices/tvtopshelfitem)

### Creating a Top Shelf Item

- [init(identifier: String)](/documentation/tvservices/tvtopshelfitem/init(identifier:))

### Assigning Actions to the Item

- [var playAction: TVTopShelfAction?](/documentation/tvservices/tvtopshelfitem/playaction)
- [var displayAction: TVTopShelfAction?](/documentation/tvservices/tvtopshelfitem/displayaction)

### Providing an Image for the Item

- [func imageURL(for: TVTopShelfItem.ImageTraits) -> URL?](/documentation/tvservices/tvtopshelfitem/imageurl(for:))
- [func setImageURL(URL?, for: TVTopShelfItem.ImageTraits)](/documentation/tvservices/tvtopshelfitem/setimageurl(_:for:))
- [TVTopShelfItem.ImageTraits](/documentation/tvservices/tvtopshelfitem/imagetraits)

#### Image Traits

- [static var screenScale1x: TVTopShelfItem.ImageTraits](/documentation/tvservices/tvtopshelfitem/imagetraits/screenscale1x)
- [static var screenScale2x: TVTopShelfItem.ImageTraits](/documentation/tvservices/tvtopshelfitem/imagetraits/screenscale2x)

#### Initializers

- [init(rawValue: UInt)](/documentation/tvservices/tvtopshelfitem/imagetraits/init(rawvalue:))

### Getting the Item Attributes

- [var identifier: String](/documentation/tvservices/tvtopshelfitem/identifier)
- [var expirationDate: Date?](/documentation/tvservices/tvtopshelfitem/expirationdate)
- [TVTopShelfAction](/documentation/tvservices/tvtopshelfaction)

### Creating an Action Object

- [init(url: URL)](/documentation/tvservices/tvtopshelfaction/init(url:))

### Getting the URL

- [var url: URL](/documentation/tvservices/tvtopshelfaction/url)
- [TVTopShelfContent](/documentation/tvservices/tvtopshelfcontent)
- [TVTopShelfObject](/documentation/tvservices/tvtopshelfobject)

### Getting the Object Attributes

- [var title: String?](/documentation/tvservices/tvtopshelfobject/title)

## Variables

- [let TVUserActivityTypeBrowsingEntertainmentContent: String](/documentation/tvservices/tvuseractivitytypebrowsingentertainmentcontent)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
