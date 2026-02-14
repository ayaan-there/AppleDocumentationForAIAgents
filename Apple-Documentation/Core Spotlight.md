# Core Spotlight Documentation

Source: https://sosumi.ai/documentation/corespotlight

---
title: Core Spotlight
source: https://developer.apple.com/documentation/corespotlight
timestamp: 2026-02-13T18:55:41.963Z
---

## Essentials

- [Adding your app’s content to Spotlight indexes](/documentation/corespotlight/adding-your-app-s-content-to-spotlight-indexes)
- [Enabling Apple Intelligence summarization and prioritization](/documentation/corespotlight/enable-apple-intelligence-summaries)

## Searchable items

- [CSSearchableItem](/documentation/corespotlight/cssearchableitem)

### Getting a searchable item

- [init(uniqueIdentifier: String?, domainIdentifier: String?, attributeSet: CSSearchableItemAttributeSet)](/documentation/corespotlight/cssearchableitem/init(uniqueidentifier:domainidentifier:attributeset:))

### Setting attributes on a searchable item

- [var uniqueIdentifier: String](/documentation/corespotlight/cssearchableitem/uniqueidentifier)
- [var domainIdentifier: String?](/documentation/corespotlight/cssearchableitem/domainidentifier)
- [var attributeSet: CSSearchableItemAttributeSet](/documentation/corespotlight/cssearchableitem/attributeset)
- [var expirationDate: Date!](/documentation/corespotlight/cssearchableitem/expirationdate)
- [var isUpdate: Bool](/documentation/corespotlight/cssearchableitem/isupdate)

### Continuing a search or activity

- [let CSSearchableItemActionType: String](/documentation/corespotlight/cssearchableitemactiontype)
- [let CSSearchableItemActivityIdentifier: String](/documentation/corespotlight/cssearchableitemactivityidentifier)
- [let CSQueryContinuationActionType: String](/documentation/corespotlight/csquerycontinuationactiontype)
- [let CSSearchQueryString: String](/documentation/corespotlight/cssearchquerystring)

### Comparing items

- [func compare(byRank: CSSearchableItem) -> ComparisonResult](/documentation/corespotlight/cssearchableitem/compare(byrank:))

### Structures

- [CSSearchableItem.UpdateListenerOptions](/documentation/corespotlight/cssearchableitem/updatelisteneroptions-swift.struct)

#### Getting the listener options structure

- [init(rawValue: UInt)](/documentation/corespotlight/cssearchableitem/updatelisteneroptions-swift.struct/init(rawvalue:))

#### Getting the listener options attributes

- [static var summarization: CSSearchableItem.UpdateListenerOptions](/documentation/corespotlight/cssearchableitem/updatelisteneroptions-swift.struct/summarization)
- [static var priority: CSSearchableItem.UpdateListenerOptions](/documentation/corespotlight/cssearchableitem/updatelisteneroptions-swift.struct/priority)

### Initializers

- [convenience init(appEntity: some IndexedEntity)](/documentation/corespotlight/cssearchableitem/init(appentity:))
- [convenience init<Entity>(appEntity: Entity, priority: Int)](/documentation/corespotlight/cssearchableitem/init(appentity:priority:))

### Instance Properties

- [var updateListenerOptions: CSSearchableItem.UpdateListenerOptions](/documentation/corespotlight/cssearchableitem/updatelisteneroptions-swift.property)

### Instance Methods

- [func associateAppEntity(some IndexedEntity, priority: Int)](/documentation/corespotlight/cssearchableitem/associateappentity(_:priority:))
- [CSSearchableItemAttributeSet](/documentation/corespotlight/cssearchableitemattributeset)

### Getting an attribute set

- [init(contentType: UTType)](/documentation/corespotlight/cssearchableitemattributeset/init(contenttype:))

### Working with custom attributes

- [func setValue((any NSSecureCoding)?, forCustomKey: CSCustomAttributeKey)](/documentation/corespotlight/cssearchableitemattributeset/setvalue(_:forcustomkey:))
- [func value(forCustomKey: CSCustomAttributeKey) -> (any NSSecureCoding)?](/documentation/corespotlight/cssearchableitemattributeset/value(forcustomkey:))

### Describing Apple Intelligence prioritization and summarization

- [var isPriority: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/ispriority)
- [var textContentSummary: String?](/documentation/corespotlight/cssearchableitemattributeset/textcontentsummary)
- [var transcribedTextContent: String?](/documentation/corespotlight/cssearchableitemattributeset/transcribedtextcontent)

### Describing documents

- [var audiences: [String]?](/documentation/corespotlight/cssearchableitemattributeset/audiences)
- [var contentDescription: String?](/documentation/corespotlight/cssearchableitemattributeset/contentdescription)
- [var creator: String?](/documentation/corespotlight/cssearchableitemattributeset/creator)
- [var encodingApplications: [String]?](/documentation/corespotlight/cssearchableitemattributeset/encodingapplications)
- [var fileSize: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/filesize)
- [var fontNames: [String]?](/documentation/corespotlight/cssearchableitemattributeset/fontnames)
- [var identifier: String?](/documentation/corespotlight/cssearchableitemattributeset/identifier)
- [var kind: String?](/documentation/corespotlight/cssearchableitemattributeset/kind)
- [var pageCount: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/pagecount)
- [var pageHeight: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/pageheight)
- [var pageWidth: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/pagewidth)
- [var securityMethod: String?](/documentation/corespotlight/cssearchableitemattributeset/securitymethod)
- [var subject: String?](/documentation/corespotlight/cssearchableitemattributeset/subject)
- [var theme: String?](/documentation/corespotlight/cssearchableitemattributeset/theme)

### Describing general attributes

- [var alternateNames: [String]?](/documentation/corespotlight/cssearchableitemattributeset/alternatenames)
- [var contentType: String?](/documentation/corespotlight/cssearchableitemattributeset/contenttype)
- [var contentTypeTree: [String]?](/documentation/corespotlight/cssearchableitemattributeset/contenttypetree)
- [var contentURL: URL?](/documentation/corespotlight/cssearchableitemattributeset/contenturl)
- [var darkThumbnailURL: URL?](/documentation/corespotlight/cssearchableitemattributeset/darkthumbnailurl)
- [var displayName: String?](/documentation/corespotlight/cssearchableitemattributeset/displayname)
- [var keywords: [String]?](/documentation/corespotlight/cssearchableitemattributeset/keywords)
- [var metadataModificationDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/metadatamodificationdate)
- [var path: String?](/documentation/corespotlight/cssearchableitemattributeset/path)
- [var rankingHint: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/rankinghint)
- [var relatedUniqueIdentifier: String?](/documentation/corespotlight/cssearchableitemattributeset/relateduniqueidentifier)
- [var thumbnailData: Data?](/documentation/corespotlight/cssearchableitemattributeset/thumbnaildata)
- [var thumbnailURL: URL?](/documentation/corespotlight/cssearchableitemattributeset/thumbnailurl)
- [var title: String?](/documentation/corespotlight/cssearchableitemattributeset/title)
- [var domainIdentifier: String?](/documentation/corespotlight/cssearchableitemattributeset/domainidentifier)
- [var weakRelatedUniqueIdentifier: String?](/documentation/corespotlight/cssearchableitemattributeset/weakrelateduniqueidentifier)

### Describing user involvement

- [var userCreated: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/usercreated)
- [var userCurated: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/usercurated)
- [var userOwned: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/userowned)

### Describing events

- [var allDay: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/allday)
- [var completionDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/completiondate)
- [var dueDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/duedate)
- [var endDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/enddate)
- [var importantDates: [Date]?](/documentation/corespotlight/cssearchableitemattributeset/importantdates)
- [var startDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/startdate)

### Describing places

- [var altitude: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/altitude)
- [var city: String?](/documentation/corespotlight/cssearchableitemattributeset/city)
- [var country: String?](/documentation/corespotlight/cssearchableitemattributeset/country)
- [var gpsAreaInformation: String?](/documentation/corespotlight/cssearchableitemattributeset/gpsareainformation)
- [var gpsdop: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/gpsdop)
- [var gpsDateStamp: Date?](/documentation/corespotlight/cssearchableitemattributeset/gpsdatestamp)
- [var gpsDestBearing: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/gpsdestbearing)
- [var gpsDestDistance: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/gpsdestdistance)
- [var gpsDestLatitude: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/gpsdestlatitude)
- [var gpsDestLongitude: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/gpsdestlongitude)
- [var gpsDifferental: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/gpsdifferental)
- [var gpsMapDatum: String?](/documentation/corespotlight/cssearchableitemattributeset/gpsmapdatum)
- [var gpsMeasureMode: String?](/documentation/corespotlight/cssearchableitemattributeset/gpsmeasuremode)
- [var gpsProcessingMethod: String?](/documentation/corespotlight/cssearchableitemattributeset/gpsprocessingmethod)
- [var gpsStatus: String?](/documentation/corespotlight/cssearchableitemattributeset/gpsstatus)
- [var gpsTrack: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/gpstrack)
- [var headline: String?](/documentation/corespotlight/cssearchableitemattributeset/headline)
- [var imageDirection: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/imagedirection)
- [var instructions: String?](/documentation/corespotlight/cssearchableitemattributeset/instructions)
- [var latitude: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/latitude)
- [var longitude: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/longitude)
- [var namedLocation: String?](/documentation/corespotlight/cssearchableitemattributeset/namedlocation)
- [var speed: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/speed)
- [var stateOrProvince: String?](/documentation/corespotlight/cssearchableitemattributeset/stateorprovince)
- [var timestamp: Date?](/documentation/corespotlight/cssearchableitemattributeset/timestamp)
- [var fullyFormattedAddress: String?](/documentation/corespotlight/cssearchableitemattributeset/fullyformattedaddress)
- [var postalCode: String?](/documentation/corespotlight/cssearchableitemattributeset/postalcode)
- [var subThoroughfare: String?](/documentation/corespotlight/cssearchableitemattributeset/subthoroughfare)
- [var thoroughfare: String?](/documentation/corespotlight/cssearchableitemattributeset/thoroughfare)

### Describing media

- [var comment: String?](/documentation/corespotlight/cssearchableitemattributeset/comment)
- [var contentCreationDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/contentcreationdate)
- [var contentModificationDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/contentmodificationdate)
- [var contentSources: [String]?](/documentation/corespotlight/cssearchableitemattributeset/contentsources)
- [var copyright: String?](/documentation/corespotlight/cssearchableitemattributeset/copyright)
- [var downloadedDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/downloadeddate)
- [var editors: [String]?](/documentation/corespotlight/cssearchableitemattributeset/editors)
- [var lastUsedDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/lastuseddate)
- [var participants: [String]?](/documentation/corespotlight/cssearchableitemattributeset/participants)
- [var projects: [String]?](/documentation/corespotlight/cssearchableitemattributeset/projects)
- [var addedDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/addeddate)
- [var codecs: [String]?](/documentation/corespotlight/cssearchableitemattributeset/codecs)
- [var contactKeywords: [String]?](/documentation/corespotlight/cssearchableitemattributeset/contactkeywords)
- [var deliveryType: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/deliverytype)
- [var duration: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/duration)
- [var mediaTypes: [String]?](/documentation/corespotlight/cssearchableitemattributeset/mediatypes)
- [var organizations: [String]?](/documentation/corespotlight/cssearchableitemattributeset/organizations)
- [var streamable: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/streamable)
- [var totalBitRate: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/totalbitrate)
- [var audioBitRate: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/audiobitrate)
- [var version: String?](/documentation/corespotlight/cssearchableitemattributeset/version)
- [var videoBitRate: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/videobitrate)
- [var contributors: [String]?](/documentation/corespotlight/cssearchableitemattributeset/contributors)
- [var languages: [String]?](/documentation/corespotlight/cssearchableitemattributeset/languages)
- [var publishers: [String]?](/documentation/corespotlight/cssearchableitemattributeset/publishers)
- [var rights: String?](/documentation/corespotlight/cssearchableitemattributeset/rights)
- [var role: String?](/documentation/corespotlight/cssearchableitemattributeset/role)
- [var contentRating: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/contentrating)
- [var coverage: [String]?](/documentation/corespotlight/cssearchableitemattributeset/coverage)
- [var director: String?](/documentation/corespotlight/cssearchableitemattributeset/director)
- [var genre: String?](/documentation/corespotlight/cssearchableitemattributeset/genre)
- [var information: String?](/documentation/corespotlight/cssearchableitemattributeset/information)
- [var local: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/local)
- [var originalFormat: String?](/documentation/corespotlight/cssearchableitemattributeset/originalformat)
- [var originalSource: String?](/documentation/corespotlight/cssearchableitemattributeset/originalsource)
- [var performers: [String]?](/documentation/corespotlight/cssearchableitemattributeset/performers)
- [var playCount: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/playcount)
- [var producer: String?](/documentation/corespotlight/cssearchableitemattributeset/producer)
- [var rating: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/rating)
- [var ratingDescription: String?](/documentation/corespotlight/cssearchableitemattributeset/ratingdescription)
- [var url: URL?](/documentation/corespotlight/cssearchableitemattributeset/url)

### Describing music

- [var album: String?](/documentation/corespotlight/cssearchableitemattributeset/album)
- [var artist: String?](/documentation/corespotlight/cssearchableitemattributeset/artist)
- [var audioChannelCount: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/audiochannelcount)
- [var audioEncodingApplication: String?](/documentation/corespotlight/cssearchableitemattributeset/audioencodingapplication)
- [var audioSampleRate: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/audiosamplerate)
- [var audioTrackNumber: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/audiotracknumber)
- [var composer: String?](/documentation/corespotlight/cssearchableitemattributeset/composer)
- [var keySignature: String?](/documentation/corespotlight/cssearchableitemattributeset/keysignature)
- [var lyricist: String?](/documentation/corespotlight/cssearchableitemattributeset/lyricist)
- [var musicalGenre: String?](/documentation/corespotlight/cssearchableitemattributeset/musicalgenre)
- [var recordingDate: Date?](/documentation/corespotlight/cssearchableitemattributeset/recordingdate)
- [var tempo: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/tempo)
- [var timeSignature: String?](/documentation/corespotlight/cssearchableitemattributeset/timesignature)
- [var generalMIDISequence: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/generalmidisequence)
- [var musicalInstrumentCategory: String?](/documentation/corespotlight/cssearchableitemattributeset/musicalinstrumentcategory)
- [var musicalInstrumentName: String?](/documentation/corespotlight/cssearchableitemattributeset/musicalinstrumentname)

### Describing images

- [var isoSpeed: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/isospeed)
- [var acquisitionMake: String?](/documentation/corespotlight/cssearchableitemattributeset/acquisitionmake)
- [var acquisitionModel: String?](/documentation/corespotlight/cssearchableitemattributeset/acquisitionmodel)
- [var aperture: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/aperture)
- [var bitsPerSample: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/bitspersample)
- [var cameraOwner: String?](/documentation/corespotlight/cssearchableitemattributeset/cameraowner)
- [var colorSpace: String?](/documentation/corespotlight/cssearchableitemattributeset/colorspace)
- [var flashOn: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/flashon)
- [var focalLength: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/focallength)
- [var focalLength35mm: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/focallength35mm)
- [var layerNames: [String]?](/documentation/corespotlight/cssearchableitemattributeset/layernames)
- [var lensModel: String?](/documentation/corespotlight/cssearchableitemattributeset/lensmodel)
- [var orientation: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/orientation)
- [var pixelCount: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/pixelcount)
- [var pixelHeight: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/pixelheight)
- [var pixelWidth: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/pixelwidth)
- [var whiteBalance: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/whitebalance)
- [var exifgpsVersion: String?](/documentation/corespotlight/cssearchableitemattributeset/exifgpsversion)
- [var exifVersion: String?](/documentation/corespotlight/cssearchableitemattributeset/exifversion)
- [var exposureMode: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/exposuremode)
- [var exposureProgram: String?](/documentation/corespotlight/cssearchableitemattributeset/exposureprogram)
- [var exposureTime: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/exposuretime)
- [var exposureTimeString: String?](/documentation/corespotlight/cssearchableitemattributeset/exposuretimestring)
- [var fNumber: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/fnumber)
- [var hasAlphaChannel: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/hasalphachannel)
- [var maxAperture: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/maxaperture)
- [var meteringMode: String?](/documentation/corespotlight/cssearchableitemattributeset/meteringmode)
- [var profileName: String?](/documentation/corespotlight/cssearchableitemattributeset/profilename)
- [var redEyeOn: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/redeyeon)
- [var resolutionHeightDPI: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/resolutionheightdpi)
- [var resolutionWidthDPI: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/resolutionwidthdpi)

### Describing messages

- [Common Mailbox Identifiers](/documentation/corespotlight/common-mailbox-identifiers)

#### Constants

- [let CSMailboxInbox: String](/documentation/corespotlight/csmailboxinbox)
- [let CSMailboxDrafts: String](/documentation/corespotlight/csmailboxdrafts)
- [let CSMailboxSent: String](/documentation/corespotlight/csmailboxsent)
- [let CSMailboxJunk: String](/documentation/corespotlight/csmailboxjunk)
- [let CSMailboxTrash: String](/documentation/corespotlight/csmailboxtrash)
- [let CSMailboxArchive: String](/documentation/corespotlight/csmailboxarchive)
- [var htmlContentData: Data?](/documentation/corespotlight/cssearchableitemattributeset/htmlcontentdata)
- [var accountHandles: [String]?](/documentation/corespotlight/cssearchableitemattributeset/accounthandles)
- [var accountIdentifier: String?](/documentation/corespotlight/cssearchableitemattributeset/accountidentifier)
- [var additionalRecipients: [CSPerson]?](/documentation/corespotlight/cssearchableitemattributeset/additionalrecipients)
- [var authorAddresses: [String]?](/documentation/corespotlight/cssearchableitemattributeset/authoraddresses)
- [var authorEmailAddresses: [String]?](/documentation/corespotlight/cssearchableitemattributeset/authoremailaddresses)
- [var authorNames: [String]?](/documentation/corespotlight/cssearchableitemattributeset/authornames)
- [var authors: [CSPerson]?](/documentation/corespotlight/cssearchableitemattributeset/authors)
- [var emailAddresses: [String]?](/documentation/corespotlight/cssearchableitemattributeset/emailaddresses)
- [var emailHeaders: [String : [Any]]?](/documentation/corespotlight/cssearchableitemattributeset/emailheaders)
- [var hiddenAdditionalRecipients: [CSPerson]?](/documentation/corespotlight/cssearchableitemattributeset/hiddenadditionalrecipients)
- [var instantMessageAddresses: [String]?](/documentation/corespotlight/cssearchableitemattributeset/instantmessageaddresses)
- [var likelyJunk: NSNumber](/documentation/corespotlight/cssearchableitemattributeset/likelyjunk)
- [var mailboxIdentifiers: [String]?](/documentation/corespotlight/cssearchableitemattributeset/mailboxidentifiers)
- [var phoneNumbers: [String]?](/documentation/corespotlight/cssearchableitemattributeset/phonenumbers)
- [var primaryRecipients: [CSPerson]?](/documentation/corespotlight/cssearchableitemattributeset/primaryrecipients)
- [var recipientAddresses: [String]?](/documentation/corespotlight/cssearchableitemattributeset/recipientaddresses)
- [var recipientEmailAddresses: [String]?](/documentation/corespotlight/cssearchableitemattributeset/recipientemailaddresses)
- [var recipientNames: [String]?](/documentation/corespotlight/cssearchableitemattributeset/recipientnames)
- [var textContent: String?](/documentation/corespotlight/cssearchableitemattributeset/textcontent)

### Describing containment

- [var containerDisplayName: String?](/documentation/corespotlight/cssearchableitemattributeset/containerdisplayname)
- [var containerIdentifier: String?](/documentation/corespotlight/cssearchableitemattributeset/containeridentifier)
- [var containerOrder: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/containerorder)
- [var containerTitle: String?](/documentation/corespotlight/cssearchableitemattributeset/containertitle)

### Supporting actions

- [var actionIdentifiers: [String]](/documentation/corespotlight/cssearchableitemattributeset/actionidentifiers)
- [var supportsNavigation: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/supportsnavigation)
- [var supportsPhoneCall: NSNumber?](/documentation/corespotlight/cssearchableitemattributeset/supportsphonecall)
- [var sharedItemContentType: UTType?](/documentation/corespotlight/cssearchableitemattributeset/shareditemcontenttype)
- [let CSActionIdentifier: String](/documentation/corespotlight/csactionidentifier)

### Providing item representations

- [var providerDataTypeIdentifiers: [String]?](/documentation/corespotlight/cssearchableitemattributeset/providerdatatypeidentifiers)
- [var providerFileTypeIdentifiers: [String]?](/documentation/corespotlight/cssearchableitemattributeset/providerfiletypeidentifiers)
- [var providerInPlaceFileTypeIdentifiers: [String]?](/documentation/corespotlight/cssearchableitemattributeset/providerinplacefiletypeidentifiers)

### Deprecated

- [init(itemContentType: String)](/documentation/corespotlight/cssearchableitemattributeset/init(itemcontenttype:))

### Instance Methods

- [func associateAppEntity<Entity>(Entity, priority: Int)](/documentation/corespotlight/cssearchableitemattributeset/associateappentity(_:priority:))
- [func move(from: CSSearchableItemAttributeSet)](/documentation/corespotlight/cssearchableitemattributeset/move(from:))
- [CSCustomAttributeKey](/documentation/corespotlight/cscustomattributekey)

### Creating a custom attribute

- [convenience init?(keyName: String)](/documentation/corespotlight/cscustomattributekey/init(keyname:))
- [init?(keyName: String, searchable: Bool, searchableByDefault: Bool, unique: Bool, multiValued: Bool)](/documentation/corespotlight/cscustomattributekey/init(keyname:searchable:searchablebydefault:unique:multivalued:))

### Getting the attribute details

- [var keyName: String](/documentation/corespotlight/cscustomattributekey/keyname)
- [var isMultiValued: Bool](/documentation/corespotlight/cscustomattributekey/ismultivalued)
- [var isSearchable: Bool](/documentation/corespotlight/cscustomattributekey/issearchable)
- [var isSearchableByDefault: Bool](/documentation/corespotlight/cscustomattributekey/issearchablebydefault)
- [var isUnique: Bool](/documentation/corespotlight/cscustomattributekey/isunique)
- [CSLocalizedString](/documentation/corespotlight/cslocalizedstring)

### Specifying localized strings

- [init(localizedStrings: [AnyHashable : Any])](/documentation/corespotlight/cslocalizedstring/init(localizedstrings:))

### Getting a localized string

- [func localizedString() -> String](/documentation/corespotlight/cslocalizedstring/localizedstring())
- [CSPerson](/documentation/corespotlight/csperson)

### Initializing a person object

- [init(displayName: String?, handles: [String], handleIdentifier: String)](/documentation/corespotlight/csperson/init(displayname:handles:handleidentifier:))

### Accessing person properties

- [var contactIdentifier: String?](/documentation/corespotlight/csperson/contactidentifier)
- [var displayName: String?](/documentation/corespotlight/csperson/displayname)
- [var handleIdentifier: String](/documentation/corespotlight/csperson/handleidentifier)
- [var handles: [String]](/documentation/corespotlight/csperson/handles)

## Indexes

- [CSSearchableIndex](/documentation/corespotlight/cssearchableindex)

### Creating an index

- [class func `default`() -> Self](/documentation/corespotlight/cssearchableindex/default())
- [init(name: String)](/documentation/corespotlight/cssearchableindex/init(name:))
- [init(name: String, protectionClass: FileProtectionType?)](/documentation/corespotlight/cssearchableindex/init(name:protectionclass:))

### Determining if indexing is available

- [class func isIndexingAvailable() -> Bool](/documentation/corespotlight/cssearchableindex/isindexingavailable())

### Responding to index-related changes

- [CSSearchableIndexDelegate](/documentation/corespotlight/cssearchableindexdelegate)

#### Getting item-related details

- [func data(for: CSSearchableIndex, itemIdentifier: String, typeIdentifier: String) throws -> Data](/documentation/corespotlight/cssearchableindexdelegate/data(for:itemidentifier:typeidentifier:))
- [func fileURL(for: CSSearchableIndex, itemIdentifier: String, typeIdentifier: String, inPlace: Bool) throws -> URL](/documentation/corespotlight/cssearchableindexdelegate/fileurl(for:itemidentifier:typeidentifier:inplace:))

#### Updating the index

- [func searchableIndex(CSSearchableIndex, reindexAllSearchableItemsWithAcknowledgementHandler: () -> Void)](/documentation/corespotlight/cssearchableindexdelegate/searchableindex(_:reindexallsearchableitemswithacknowledgementhandler:))
- [func searchableIndex(CSSearchableIndex, reindexSearchableItemsWithIdentifiers: [String], acknowledgementHandler: () -> Void)](/documentation/corespotlight/cssearchableindexdelegate/searchableindex(_:reindexsearchableitemswithidentifiers:acknowledgementhandler:))

#### Getting information about indexing

- [func searchableIndexDidThrottle(CSSearchableIndex)](/documentation/corespotlight/cssearchableindexdelegate/searchableindexdidthrottle(_:))
- [func searchableIndexDidFinishThrottle(CSSearchableIndex)](/documentation/corespotlight/cssearchableindexdelegate/searchableindexdidfinishthrottle(_:))

#### Instance Methods

- [func searchableItems(forIdentifiers: [String], searchableItemsHandler: ([CSSearchableItem]) -> Void)](/documentation/corespotlight/cssearchableindexdelegate/searchableitems(foridentifiers:searchableitemshandler:))
- [func searchableItemsDidUpdate([CSSearchableItem])](/documentation/corespotlight/cssearchableindexdelegate/searchableitemsdidupdate(_:))
- [var indexDelegate: (any CSSearchableIndexDelegate)?](/documentation/corespotlight/cssearchableindex/indexdelegate)

### Managing items in an index

- [func indexSearchableItems([CSSearchableItem], completionHandler: (((any Error)?) -> Void)?)](/documentation/corespotlight/cssearchableindex/indexsearchableitems(_:completionhandler:))
- [func deleteAllSearchableItems(completionHandler: (((any Error)?) -> Void)?)](/documentation/corespotlight/cssearchableindex/deleteallsearchableitems(completionhandler:))
- [func deleteSearchableItems(withDomainIdentifiers: [String], completionHandler: (((any Error)?) -> Void)?)](/documentation/corespotlight/cssearchableindex/deletesearchableitems(withdomainidentifiers:completionhandler:))
- [func deleteSearchableItems(withIdentifiers: [String], completionHandler: (((any Error)?) -> Void)?)](/documentation/corespotlight/cssearchableindex/deletesearchableitems(withidentifiers:completionhandler:))

### Batching index updates

- [func beginBatch()](/documentation/corespotlight/cssearchableindex/beginbatch())
- [func endBatch(withClientState: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/corespotlight/cssearchableindex/endbatch(withclientstate:completionhandler:))
- [func endIndexBatch(expectedClientState: Data?, newClientState: Data, completionHandler: (((any Error)?) -> Void)?)](/documentation/corespotlight/cssearchableindex/endindexbatch(expectedclientstate:newclientstate:completionhandler:))
- [func fetchLastClientState(completionHandler: (Data?, (any Error)?) -> Void)](/documentation/corespotlight/cssearchableindex/fetchlastclientstate(completionhandler:))

### Handling drag and drop content

- [func fetchData(forBundleIdentifier: String, itemIdentifier: String, contentType: UTType, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/corespotlight/cssearchableindex/fetchdata(forbundleidentifier:itemidentifier:contenttype:completionhandler:))

### Instance Methods

- [func deleteAppEntities<Entity>(identifiedBy: [Entity.ID], ofType: Entity.Type) async throws](/documentation/corespotlight/cssearchableindex/deleteappentities(identifiedby:oftype:))
- [func deleteAppEntities<Entity>(ofType: Entity.Type) async throws](/documentation/corespotlight/cssearchableindex/deleteappentities(oftype:))
- [func indexAppEntities([some IndexedEntity], priority: Int) async throws](/documentation/corespotlight/cssearchableindex/indexappentities(_:priority:))
- [CSSearchableIndexDelegate](/documentation/corespotlight/cssearchableindexdelegate)

### Getting item-related details

- [func data(for: CSSearchableIndex, itemIdentifier: String, typeIdentifier: String) throws -> Data](/documentation/corespotlight/cssearchableindexdelegate/data(for:itemidentifier:typeidentifier:))
- [func fileURL(for: CSSearchableIndex, itemIdentifier: String, typeIdentifier: String, inPlace: Bool) throws -> URL](/documentation/corespotlight/cssearchableindexdelegate/fileurl(for:itemidentifier:typeidentifier:inplace:))

### Updating the index

- [func searchableIndex(CSSearchableIndex, reindexAllSearchableItemsWithAcknowledgementHandler: () -> Void)](/documentation/corespotlight/cssearchableindexdelegate/searchableindex(_:reindexallsearchableitemswithacknowledgementhandler:))
- [func searchableIndex(CSSearchableIndex, reindexSearchableItemsWithIdentifiers: [String], acknowledgementHandler: () -> Void)](/documentation/corespotlight/cssearchableindexdelegate/searchableindex(_:reindexsearchableitemswithidentifiers:acknowledgementhandler:))

### Getting information about indexing

- [func searchableIndexDidThrottle(CSSearchableIndex)](/documentation/corespotlight/cssearchableindexdelegate/searchableindexdidthrottle(_:))
- [func searchableIndexDidFinishThrottle(CSSearchableIndex)](/documentation/corespotlight/cssearchableindexdelegate/searchableindexdidfinishthrottle(_:))

### Instance Methods

- [func searchableItems(forIdentifiers: [String], searchableItemsHandler: ([CSSearchableItem]) -> Void)](/documentation/corespotlight/cssearchableindexdelegate/searchableitems(foridentifiers:searchableitemshandler:))
- [func searchableItemsDidUpdate([CSSearchableItem])](/documentation/corespotlight/cssearchableindexdelegate/searchableitemsdidupdate(_:))

## Spotlight app extensions

- [Regenerating your app’s indexes on demand](/documentation/corespotlight/regenerating-your-app-s-indexes-on-demand)
- [CSIndexExtensionRequestHandler](/documentation/corespotlight/csindexextensionrequesthandler)
- [CSImportExtension](/documentation/corespotlight/csimportextension)

### Providing searchable attributes

- [func update(CSSearchableItemAttributeSet, forFileAt: URL) throws](/documentation/corespotlight/csimportextension/update(_:forfileat:))

## Queries

- [Building a search interface for your app](/documentation/corespotlight/building-a-search-interface-for-your-app)
- [Searching for information in your app](/documentation/corespotlight/searching-for-information-in-your-app)
- [CSUserQuery](/documentation/corespotlight/csuserquery)

### Creating a user query

- [init(userQueryString: String?, userQueryContext: CSUserQueryContext?)](/documentation/corespotlight/csuserquery/init(userquerystring:userquerycontext:))

### Preparing to search

- [class func prepare()](/documentation/corespotlight/csuserquery/prepare())
- [class func prepareProtectionClasses([FileProtectionType])](/documentation/corespotlight/csuserquery/prepareprotectionclasses(_:))

### Executing the query automatically

- [var responses: CSUserQuery.Responses](/documentation/corespotlight/csuserquery/responses-swift.property)
- [var suggestions: CSUserQuery.Suggestions](/documentation/corespotlight/csuserquery/suggestions-swift.property)
- [CSUserQuery.Responses](/documentation/corespotlight/csuserquery/responses-swift.struct)

#### Getting the response type

- [CSUserQuery.Responses.Response](/documentation/corespotlight/csuserquery/responses-swift.struct/response)

##### Enumeration Cases

- [case item(CSUserQuery.Item)](/documentation/corespotlight/csuserquery/responses-swift.struct/response/item(_:))
- [case suggestion(CSUserQuery.Suggestion)](/documentation/corespotlight/csuserquery/responses-swift.struct/response/suggestion(_:))

#### Iterating over the responses

- [CSUserQuery.Responses.Iterator](/documentation/corespotlight/csuserquery/responses-swift.struct/iterator)
- [CSUserQuery.Suggestions](/documentation/corespotlight/csuserquery/suggestions-swift.struct)

#### Structures

- [CSUserQuery.Suggestions.Iterator](/documentation/corespotlight/csuserquery/suggestions-swift.struct/iterator)
- [CSUserQuery.Item](/documentation/corespotlight/csuserquery/item)

#### Instance Properties

- [var item: CSSearchableItem](/documentation/corespotlight/csuserquery/item/item)
- [CSUserQuery.Suggestion](/documentation/corespotlight/csuserquery/suggestion)

#### Instance Properties

- [var suggestion: CSSuggestion](/documentation/corespotlight/csuserquery/suggestion/suggestion)

### Executing the query with handler blocks

- [func start()](/documentation/corespotlight/csuserquery/start())
- [func cancel()](/documentation/corespotlight/csuserquery/cancel())
- [var foundSuggestionsHandler: (([CSSuggestion]) -> Void)?](/documentation/corespotlight/csuserquery/foundsuggestionshandler)
- [var foundSuggestionCount: Int](/documentation/corespotlight/csuserquery/foundsuggestioncount)

### Improving the quality of ranked results

- [func userEngaged(CSUserQuery.Item, visibleItems: [CSUserQuery.Item], interaction: CSUserQuery.UserInteractionKind)](/documentation/corespotlight/csuserquery/userengaged(_:visibleitems:interaction:))
- [func userEngaged(CSUserQuery.Suggestion, visibleSuggestions: [CSUserQuery.Suggestion], interaction: CSUserQuery.UserInteractionKind)](/documentation/corespotlight/csuserquery/userengaged(_:visiblesuggestions:interaction:))
- [CSUserQuery.UserInteractionKind](/documentation/corespotlight/csuserquery/userinteractionkind)

#### Getting the interaction types

- [static var `default`: CSUserQuery.UserInteractionKind](/documentation/corespotlight/csuserquery/userinteractionkind/default)
- [case select](/documentation/corespotlight/csuserquery/userinteractionkind/select)
- [case focus](/documentation/corespotlight/csuserquery/userinteractionkind/focus)

#### Creating an interaction kind

- [init?(rawValue: Int)](/documentation/corespotlight/csuserquery/userinteractionkind/init(rawvalue:))
- [CSUserQueryContext](/documentation/corespotlight/csuserquerycontext)

### Creating a query context

- [init(currentSuggestion: CSSuggestion?)](/documentation/corespotlight/csuserquerycontext/init(currentsuggestion:))

### Configuring search options

- [var maxResultCount: Int](/documentation/corespotlight/csuserquerycontext/maxresultcount)
- [var maxSuggestionCount: Int](/documentation/corespotlight/csuserquerycontext/maxsuggestioncount)
- [var disableSemanticSearch: Bool](/documentation/corespotlight/csuserquerycontext/disablesemanticsearch)

### Configuring the ranked results behavior

- [var enableRankedResults: Bool](/documentation/corespotlight/csuserquerycontext/enablerankedresults)
- [var maxRankedResultCount: Int](/documentation/corespotlight/csuserquerycontext/maxrankedresultcount)
- [CSSearchQuery](/documentation/corespotlight/cssearchquery)

### Creating a query object

- [convenience init(queryString: String, attributes: [String]?)](/documentation/corespotlight/cssearchquery/init(querystring:attributes:))
- [init(queryString: String, queryContext: CSSearchQueryContext?)](/documentation/corespotlight/cssearchquery/init(querystring:querycontext:))

### Continuing an activity

- [let CSSearchQueryString: String](/documentation/corespotlight/cssearchquerystring)
- [let CSQueryContinuationActionType: String](/documentation/corespotlight/csquerycontinuationactiontype)

### Specifying the indexes to search

- [var protectionClasses: [FileProtectionType]](/documentation/corespotlight/cssearchquery/protectionclasses)

### Executing the query automatically

- [var results: CSSearchQuery.Results](/documentation/corespotlight/cssearchquery/results-swift.property)
- [CSSearchQuery.Results](/documentation/corespotlight/cssearchquery/results-swift.struct)

#### Structures

- [CSSearchQuery.Results.Item](/documentation/corespotlight/cssearchquery/results-swift.struct/item)

##### Instance Properties

- [var item: CSSearchableItem](/documentation/corespotlight/cssearchquery/results-swift.struct/item/item)
- [CSSearchQuery.Results.Iterator](/documentation/corespotlight/cssearchquery/results-swift.struct/iterator)

### Executing the query with handler blocks

- [func start()](/documentation/corespotlight/cssearchquery/start())
- [func cancel()](/documentation/corespotlight/cssearchquery/cancel())
- [var isCancelled: Bool](/documentation/corespotlight/cssearchquery/iscancelled)
- [var foundItemCount: Int](/documentation/corespotlight/cssearchquery/founditemcount)
- [var foundItemsHandler: (([CSSearchableItem]) -> Void)?](/documentation/corespotlight/cssearchquery/founditemshandler)
- [var completionHandler: (((any Error)?) -> Void)?](/documentation/corespotlight/cssearchquery/completionhandler)
- [CSSearchQueryContext](/documentation/corespotlight/cssearchquerycontext)

### Configuring search behavior

- [var fetchAttributes: [String]](/documentation/corespotlight/cssearchquerycontext/fetchattributes)
- [var keyboardLanguage: String?](/documentation/corespotlight/cssearchquerycontext/keyboardlanguage)
- [var sourceOptions: CSSearchQueryContext.SourceOptions](/documentation/corespotlight/cssearchquerycontext/sourceoptions-swift.property)
- [CSSearchQueryContext.SourceOptions](/documentation/corespotlight/cssearchquerycontext/sourceoptions-swift.struct)

#### Search options

- [static var allowMail: CSSearchQueryContext.SourceOptions](/documentation/corespotlight/cssearchquerycontext/sourceoptions-swift.struct/allowmail)

#### Initializers

- [init(rawValue: UInt)](/documentation/corespotlight/cssearchquerycontext/sourceoptions-swift.struct/init(rawvalue:))

### Filtering the results

- [var filterQueries: [String]](/documentation/corespotlight/cssearchquerycontext/filterqueries)
- [CSSuggestion](/documentation/corespotlight/cssuggestion)

### Setting suggestion attributes

- [var localizedAttributedSuggestion: AttributedString](/documentation/corespotlight/cssuggestion/localizedattributedsuggestion-3ssly)
- [var suggestionKind: CSSuggestion.SuggestionKind](/documentation/corespotlight/cssuggestion/suggestionkind-swift.property)
- [CSSuggestion.SuggestionKind](/documentation/corespotlight/cssuggestion/suggestionkind-swift.enum)

#### Suggestion types

- [case none](/documentation/corespotlight/cssuggestion/suggestionkind-swift.enum/none)
- [case custom](/documentation/corespotlight/cssuggestion/suggestionkind-swift.enum/custom)
- [case `default`](/documentation/corespotlight/cssuggestion/suggestionkind-swift.enum/default)

#### Initializers

- [init?(rawValue: Int)](/documentation/corespotlight/cssuggestion/suggestionkind-swift.enum/init(rawvalue:))

### Comparing suggestions

- [func compare(CSSuggestion) -> ComparisonResult](/documentation/corespotlight/cssuggestion/compare(_:))
- [func compare(byRank: CSSuggestion) -> ComparisonResult](/documentation/corespotlight/cssuggestion/compare(byrank:))

## Errors

- [CSIndexError](/documentation/corespotlight/csindexerror)

### Getting the error codes

- [static var indexUnavailableError: CSIndexError.Code](/documentation/corespotlight/csindexerror/indexunavailableerror)
- [static var indexingUnsupported: CSIndexError.Code](/documentation/corespotlight/csindexerror/indexingunsupported)
- [static var invalidClientStateError: CSIndexError.Code](/documentation/corespotlight/csindexerror/invalidclientstateerror)
- [static var invalidItemError: CSIndexError.Code](/documentation/corespotlight/csindexerror/invaliditemerror)
- [static var mismatchedClientState: CSIndexError.Code](/documentation/corespotlight/csindexerror/mismatchedclientstate)
- [static var quotaExceeded: CSIndexError.Code](/documentation/corespotlight/csindexerror/quotaexceeded)
- [static var remoteConnectionError: CSIndexError.Code](/documentation/corespotlight/csindexerror/remoteconnectionerror)
- [static var unknownError: CSIndexError.Code](/documentation/corespotlight/csindexerror/unknownerror)

### Getting codes for indexing errors

- [CSIndexError.Code](/documentation/corespotlight/csindexerror/code)

#### Getting the indexing error codes

- [case indexUnavailableError](/documentation/corespotlight/csindexerror/code/indexunavailableerror)
- [case indexingUnsupported](/documentation/corespotlight/csindexerror/code/indexingunsupported)
- [case invalidClientStateError](/documentation/corespotlight/csindexerror/code/invalidclientstateerror)
- [case invalidItemError](/documentation/corespotlight/csindexerror/code/invaliditemerror)
- [case mismatchedClientState](/documentation/corespotlight/csindexerror/code/mismatchedclientstate)
- [case quotaExceeded](/documentation/corespotlight/csindexerror/code/quotaexceeded)
- [case remoteConnectionError](/documentation/corespotlight/csindexerror/code/remoteconnectionerror)
- [case unknownError](/documentation/corespotlight/csindexerror/code/unknownerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/corespotlight/csindexerror/code/init(rawvalue:))

### Getting the error description

- [static var errorDomain: String](/documentation/corespotlight/csindexerror/errordomain)
- [CSSearchQueryError](/documentation/corespotlight/cssearchqueryerror)

### Getting the error codes

- [static var cancelled: CSSearchQueryError.Code](/documentation/corespotlight/cssearchqueryerror/cancelled)
- [static var indexUnreachable: CSSearchQueryError.Code](/documentation/corespotlight/cssearchqueryerror/indexunreachable)
- [static var invalidQuery: CSSearchQueryError.Code](/documentation/corespotlight/cssearchqueryerror/invalidquery)
- [static var unknown: CSSearchQueryError.Code](/documentation/corespotlight/cssearchqueryerror/unknown)

### Getting codes for query-related errors

- [CSSearchQueryError.Code](/documentation/corespotlight/cssearchqueryerror/code)

#### Getting the error codes

- [case cancelled](/documentation/corespotlight/cssearchqueryerror/code/cancelled)
- [case indexUnreachable](/documentation/corespotlight/cssearchqueryerror/code/indexunreachable)
- [case invalidQuery](/documentation/corespotlight/cssearchqueryerror/code/invalidquery)
- [case unknown](/documentation/corespotlight/cssearchqueryerror/code/unknown)

#### Creating a query error

- [init?(rawValue: Int)](/documentation/corespotlight/cssearchqueryerror/code/init(rawvalue:))

### Getting the error description

- [static var errorDomain: String](/documentation/corespotlight/cssearchqueryerror/errordomain)
- [CSIndex Errors](/documentation/corespotlight/csindex-errors)

### Index Errors

- [CSIndexError.Code](/documentation/corespotlight/csindexerror/code)

#### Getting the indexing error codes

- [case indexUnavailableError](/documentation/corespotlight/csindexerror/code/indexunavailableerror)
- [case indexingUnsupported](/documentation/corespotlight/csindexerror/code/indexingunsupported)
- [case invalidClientStateError](/documentation/corespotlight/csindexerror/code/invalidclientstateerror)
- [case invalidItemError](/documentation/corespotlight/csindexerror/code/invaliditemerror)
- [case mismatchedClientState](/documentation/corespotlight/csindexerror/code/mismatchedclientstate)
- [case quotaExceeded](/documentation/corespotlight/csindexerror/code/quotaexceeded)
- [case remoteConnectionError](/documentation/corespotlight/csindexerror/code/remoteconnectionerror)
- [case unknownError](/documentation/corespotlight/csindexerror/code/unknownerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/corespotlight/csindexerror/code/init(rawvalue:))
- [let CSIndexErrorDomain: String](/documentation/corespotlight/csindexerrordomain)
- [CSSearchQuery Errors](/documentation/corespotlight/cssearchquery-errors)

### Query Errors

- [CSSearchQueryError.Code](/documentation/corespotlight/cssearchqueryerror/code)

#### Getting the error codes

- [case cancelled](/documentation/corespotlight/cssearchqueryerror/code/cancelled)
- [case indexUnreachable](/documentation/corespotlight/cssearchqueryerror/code/indexunreachable)
- [case invalidQuery](/documentation/corespotlight/cssearchqueryerror/code/invalidquery)
- [case unknown](/documentation/corespotlight/cssearchqueryerror/code/unknown)

#### Creating a query error

- [init?(rawValue: Int)](/documentation/corespotlight/cssearchqueryerror/code/init(rawvalue:))
- [let CSSearchQueryErrorDomain: String](/documentation/corespotlight/cssearchqueryerrordomain)

## Version

- [var CoreSpotlightAPIVersion: Int32](/documentation/corespotlight/corespotlightapiversion)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
