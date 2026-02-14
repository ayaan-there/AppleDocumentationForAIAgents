# Media Player Documentation

Source: https://sosumi.ai/documentation/mediaplayer

---
title: Media Player
source: https://developer.apple.com/documentation/mediaplayer
timestamp: 2026-02-13T18:59:24.994Z
---

## Essentials

- [NSAppleMusicUsageDescription](/documentation/bundleresources/information-property-list/nsapplemusicusagedescription)

## Built-in music playback

- [Playing audio using the built-in music player](/documentation/mediaplayer/playing-audio-using-the-built-in-music-player)
- [MPMusicPlayerController](/documentation/mediaplayer/mpmusicplayercontroller)

### Getting a music player

- [class var applicationMusicPlayer: MPMusicPlayerController](/documentation/mediaplayer/mpmusicplayercontroller/applicationmusicplayer)
- [class var applicationQueuePlayer: MPMusicPlayerApplicationController](/documentation/mediaplayer/mpmusicplayercontroller/applicationqueueplayer)
- [class var systemMusicPlayer: any MPMusicPlayerController & MPSystemMusicPlayerController](/documentation/mediaplayer/mpmusicplayercontroller/systemmusicplayer)

### Setting up a playback queue

- [func setQueue(with: MPMediaQuery)](/documentation/mediaplayer/mpmusicplayercontroller/setqueue(with:)-5rii3)
- [func setQueue(with: MPMediaItemCollection)](/documentation/mediaplayer/mpmusicplayercontroller/setqueue(with:)-xlwk)
- [func setQueue(with: [String])](/documentation/mediaplayer/mpmusicplayercontroller/setqueue(with:)-8x6xb)
- [func setQueue(with: MPMusicPlayerQueueDescriptor)](/documentation/mediaplayer/mpmusicplayercontroller/setqueue(with:)-1izmj)

### Playing a media item

- [func prepareToPlay(completionHandler: ((any Error)?) -> Void)](/documentation/mediaplayer/mpmusicplayercontroller/preparetoplay(completionhandler:))

### Managing playback mode and state

- [var nowPlayingItem: MPMediaItem?](/documentation/mediaplayer/mpmusicplayercontroller/nowplayingitem)
- [var indexOfNowPlayingItem: Int](/documentation/mediaplayer/mpmusicplayercontroller/indexofnowplayingitem)
- [var playbackState: MPMusicPlaybackState](/documentation/mediaplayer/mpmusicplayercontroller/playbackstate)
- [var repeatMode: MPMusicRepeatMode](/documentation/mediaplayer/mpmusicplayercontroller/repeatmode)
- [var shuffleMode: MPMusicShuffleMode](/documentation/mediaplayer/mpmusicplayercontroller/shufflemode)
- [MPMusicPlaybackState](/documentation/mediaplayer/mpmusicplaybackstate)

#### Constants

- [case stopped](/documentation/mediaplayer/mpmusicplaybackstate/stopped)
- [case playing](/documentation/mediaplayer/mpmusicplaybackstate/playing)
- [case paused](/documentation/mediaplayer/mpmusicplaybackstate/paused)
- [case interrupted](/documentation/mediaplayer/mpmusicplaybackstate/interrupted)
- [case seekingForward](/documentation/mediaplayer/mpmusicplaybackstate/seekingforward)
- [case seekingBackward](/documentation/mediaplayer/mpmusicplaybackstate/seekingbackward)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmusicplaybackstate/init(rawvalue:))
- [MPMusicRepeatMode](/documentation/mediaplayer/mpmusicrepeatmode)

#### Constants

- [case `default`](/documentation/mediaplayer/mpmusicrepeatmode/default)
- [case none](/documentation/mediaplayer/mpmusicrepeatmode/none)
- [case one](/documentation/mediaplayer/mpmusicrepeatmode/one)
- [case all](/documentation/mediaplayer/mpmusicrepeatmode/all)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmusicrepeatmode/init(rawvalue:))
- [MPMusicShuffleMode](/documentation/mediaplayer/mpmusicshufflemode)

#### Constants

- [case `default`](/documentation/mediaplayer/mpmusicshufflemode/default)
- [case off](/documentation/mediaplayer/mpmusicshufflemode/off)
- [case songs](/documentation/mediaplayer/mpmusicshufflemode/songs)
- [case albums](/documentation/mediaplayer/mpmusicshufflemode/albums)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmusicshufflemode/init(rawvalue:))
- [var volume: Float](/documentation/mediaplayer/mpmusicplayercontroller/volume)

### Controlling playback

- [func skipToNextItem()](/documentation/mediaplayer/mpmusicplayercontroller/skiptonextitem())
- [func skipToBeginning()](/documentation/mediaplayer/mpmusicplayercontroller/skiptobeginning())
- [func skipToPreviousItem()](/documentation/mediaplayer/mpmusicplayercontroller/skiptopreviousitem())
- [func append(MPMusicPlayerQueueDescriptor)](/documentation/mediaplayer/mpmusicplayercontroller/append(_:))
- [func prepend(MPMusicPlayerQueueDescriptor)](/documentation/mediaplayer/mpmusicplayercontroller/prepend(_:))

### Using music player notifications

- [func beginGeneratingPlaybackNotifications()](/documentation/mediaplayer/mpmusicplayercontroller/begingeneratingplaybacknotifications())
- [func endGeneratingPlaybackNotifications()](/documentation/mediaplayer/mpmusicplayercontroller/endgeneratingplaybacknotifications())

### Type Properties

- [class var iPodMusicPlayer: MPMusicPlayerController](/documentation/mediaplayer/mpmusicplayercontroller/ipodmusicplayer)
- [MPMediaPlayback](/documentation/mediaplayer/mpmediaplayback)

### Starting and stopping playback

- [func play()](/documentation/mediaplayer/mpmediaplayback/play())
- [func pause()](/documentation/mediaplayer/mpmediaplayback/pause())
- [func stop()](/documentation/mediaplayer/mpmediaplayback/stop())
- [func prepareToPlay()](/documentation/mediaplayer/mpmediaplayback/preparetoplay())
- [var isPreparedToPlay: Bool](/documentation/mediaplayer/mpmediaplayback/ispreparedtoplay)

### Seeking within media

- [func beginSeekingBackward()](/documentation/mediaplayer/mpmediaplayback/beginseekingbackward())
- [func beginSeekingForward()](/documentation/mediaplayer/mpmediaplayback/beginseekingforward())
- [func endSeeking()](/documentation/mediaplayer/mpmediaplayback/endseeking())

### Accessing playback attributes

- [var currentPlaybackRate: Float](/documentation/mediaplayer/mpmediaplayback/currentplaybackrate)
- [var currentPlaybackTime: TimeInterval](/documentation/mediaplayer/mpmediaplayback/currentplaybacktime)
- [MPSystemMusicPlayerController](/documentation/mediaplayer/mpsystemmusicplayercontroller)

### Playing video in the music app

- [func openToPlay(MPMusicPlayerQueueDescriptor)](/documentation/mediaplayer/mpsystemmusicplayercontroller/opentoplay(_:))

## Media library synchronization

- [MPMediaLibrary](/documentation/mediaplayer/mpmedialibrary)

### Getting the default media library

- [class func requestAuthorization((MPMediaLibraryAuthorizationStatus) -> Void)](/documentation/mediaplayer/mpmedialibrary/requestauthorization(_:))
- [class func authorizationStatus() -> MPMediaLibraryAuthorizationStatus](/documentation/mediaplayer/mpmedialibrary/authorizationstatus())
- [MPMediaLibraryAuthorizationStatus](/documentation/mediaplayer/mpmedialibraryauthorizationstatus)

#### Authorization statuses

- [case notDetermined](/documentation/mediaplayer/mpmedialibraryauthorizationstatus/notdetermined)
- [case denied](/documentation/mediaplayer/mpmedialibraryauthorizationstatus/denied)
- [case restricted](/documentation/mediaplayer/mpmedialibraryauthorizationstatus/restricted)
- [case authorized](/documentation/mediaplayer/mpmedialibraryauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmedialibraryauthorizationstatus/init(rawvalue:))
- [class func `default`() -> MPMediaLibrary](/documentation/mediaplayer/mpmedialibrary/default())

### Receiving notifications when the user’s library changes

- [func beginGeneratingLibraryChangeNotifications()](/documentation/mediaplayer/mpmedialibrary/begingeneratinglibrarychangenotifications())
- [func endGeneratingLibraryChangeNotifications()](/documentation/mediaplayer/mpmedialibrary/endgeneratinglibrarychangenotifications())
- [var lastModifiedDate: Date](/documentation/mediaplayer/mpmedialibrary/lastmodifieddate)

### Retrieving a playlist from the media library

- [func getPlaylist(with: UUID, creationMetadata: MPMediaPlaylistCreationMetadata?, completionHandler: (MPMediaPlaylist?, (any Error)?) -> Void)](/documentation/mediaplayer/mpmedialibrary/getplaylist(with:creationmetadata:completionhandler:))

### Adding an item to the media library

- [func addItem(withProductID: String, completionHandler: (([MPMediaEntity], (any Error)?) -> Void)?)](/documentation/mediaplayer/mpmedialibrary/additem(withproductid:completionhandler:))

## Media item queries

- [Using filters to create specialized queries](/documentation/mediaplayer/using-filters-to-create-specialized-queries)
- [MPMediaQuery](/documentation/mediaplayer/mpmediaquery)

### Creating media queries

- [class func albums() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/albums())
- [class func artists() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/artists())
- [class func songs() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/songs())
- [class func playlists() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/playlists())
- [class func podcasts() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/podcasts())
- [class func audiobooks() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/audiobooks())
- [class func compilations() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/compilations())
- [class func composers() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/composers())
- [class func genres() -> MPMediaQuery](/documentation/mediaplayer/mpmediaquery/genres())
- [init(filterPredicates: Set<MPMediaPredicate>?)](/documentation/mediaplayer/mpmediaquery/init(filterpredicates:))

### Configuring media queries

- [var filterPredicates: Set<MPMediaPredicate>?](/documentation/mediaplayer/mpmediaquery/filterpredicates)
- [func addFilterPredicate(MPMediaPredicate)](/documentation/mediaplayer/mpmediaquery/addfilterpredicate(_:))
- [func removeFilterPredicate(MPMediaPredicate)](/documentation/mediaplayer/mpmediaquery/removefilterpredicate(_:))
- [var groupingType: MPMediaGrouping](/documentation/mediaplayer/mpmediaquery/groupingtype)
- [var itemSections: [MPMediaQuerySection]?](/documentation/mediaplayer/mpmediaquery/itemsections)
- [var collectionSections: [MPMediaQuerySection]?](/documentation/mediaplayer/mpmediaquery/collectionsections)
- [MPMediaGrouping](/documentation/mediaplayer/mpmediagrouping)

#### Media query keys

- [case title](/documentation/mediaplayer/mpmediagrouping/title)
- [case album](/documentation/mediaplayer/mpmediagrouping/album)
- [case artist](/documentation/mediaplayer/mpmediagrouping/artist)
- [case albumArtist](/documentation/mediaplayer/mpmediagrouping/albumartist)
- [case composer](/documentation/mediaplayer/mpmediagrouping/composer)
- [case genre](/documentation/mediaplayer/mpmediagrouping/genre)
- [case playlist](/documentation/mediaplayer/mpmediagrouping/playlist)
- [case podcastTitle](/documentation/mediaplayer/mpmediagrouping/podcasttitle)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmediagrouping/init(rawvalue:))

### Performing media queries

- [var items: [MPMediaItem]?](/documentation/mediaplayer/mpmediaquery/items)
- [var collections: [MPMediaItemCollection]?](/documentation/mediaplayer/mpmediaquery/collections)
- [MPMediaQuerySection](/documentation/mediaplayer/mpmediaquerysection)

### Working with media query sections

- [var title: String](/documentation/mediaplayer/mpmediaquerysection/title)
- [var range: NSRange](/documentation/mediaplayer/mpmediaquerysection/range)
- [MPMediaPropertyPredicate](/documentation/mediaplayer/mpmediapropertypredicate)

### Creating media property predicates

- [init(value: Any?, forProperty: String)](/documentation/mediaplayer/mpmediapropertypredicate/init(value:forproperty:))
- [init(value: Any?, forProperty: String, comparisonType: MPMediaPredicateComparison)](/documentation/mediaplayer/mpmediapropertypredicate/init(value:forproperty:comparisontype:))

### Examining media property predicates

- [var property: String](/documentation/mediaplayer/mpmediapropertypredicate/property)
- [var value: Any?](/documentation/mediaplayer/mpmediapropertypredicate/value)
- [var comparisonType: MPMediaPredicateComparison](/documentation/mediaplayer/mpmediapropertypredicate/comparisontype)

### Supporting types

- [MPMediaPredicateComparison](/documentation/mediaplayer/mpmediapredicatecomparison)

#### Constants

- [case equalTo](/documentation/mediaplayer/mpmediapredicatecomparison/equalto)
- [case contains](/documentation/mediaplayer/mpmediapredicatecomparison/contains)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmediapredicatecomparison/init(rawvalue:))
- [MPMediaPredicate](/documentation/mediaplayer/mpmediapredicate)

## Media player queues

- [MPMusicPlayerControllerQueue](/documentation/mediaplayer/mpmusicplayercontrollerqueue)

### Inspecting queue media items

- [var items: [MPMediaItem]](/documentation/mediaplayer/mpmusicplayercontrollerqueue/items)
- [MPMusicPlayerControllerMutableQueue](/documentation/mediaplayer/mpmusicplayercontrollermutablequeue)

### Adding and removing items

- [func insert(MPMusicPlayerQueueDescriptor, after: MPMediaItem?)](/documentation/mediaplayer/mpmusicplayercontrollermutablequeue/insert(_:after:))
- [func remove(MPMediaItem)](/documentation/mediaplayer/mpmusicplayercontrollermutablequeue/remove(_:))
- [MPMusicPlayerApplicationController](/documentation/mediaplayer/mpmusicplayerapplicationcontroller)

### Changing the queue contents

- [func perform(queueTransaction: (MPMusicPlayerControllerMutableQueue) -> Void, completionHandler: (MPMusicPlayerControllerQueue, (any Error)?) -> Void)](/documentation/mediaplayer/mpmusicplayerapplicationcontroller/perform(queuetransaction:completionhandler:))
- [static let MPMusicPlayerControllerQueueDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/mpmusicplayercontrollerqueuedidchange)
- [MPMusicPlayerMediaItemQueueDescriptor](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor)

### Creating a new media item queue descriptor

- [init(itemCollection: MPMediaItemCollection)](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor/init(itemcollection:))
- [init(query: MPMediaQuery)](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor/init(query:))

### Media item queue descriptor properties

- [var itemCollection: MPMediaItemCollection](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor/itemcollection)
- [var query: MPMediaQuery](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor/query)
- [var startItem: MPMediaItem?](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor/startitem)

### Setting start and end times

- [func setStartTime(TimeInterval, for: MPMediaItem)](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor/setstarttime(_:for:))
- [func setEndTime(TimeInterval, for: MPMediaItem)](/documentation/mediaplayer/mpmusicplayermediaitemqueuedescriptor/setendtime(_:for:))
- [MPMusicPlayerStoreQueueDescriptor](/documentation/mediaplayer/mpmusicplayerstorequeuedescriptor)

### Creating a new store queue descriptor

- [init(storeIDs: [String])](/documentation/mediaplayer/mpmusicplayerstorequeuedescriptor/init(storeids:))

### Store identifier queue descriptor properties

- [var startItemID: String?](/documentation/mediaplayer/mpmusicplayerstorequeuedescriptor/startitemid)
- [var storeIDs: [String]?](/documentation/mediaplayer/mpmusicplayerstorequeuedescriptor/storeids)

### Setting start and end times

- [func setStartTime(TimeInterval, forItemWithStoreID: String)](/documentation/mediaplayer/mpmusicplayerstorequeuedescriptor/setstarttime(_:foritemwithstoreid:))
- [func setEndTime(TimeInterval, forItemWithStoreID: String)](/documentation/mediaplayer/mpmusicplayerstorequeuedescriptor/setendtime(_:foritemwithstoreid:))
- [MPMusicPlayerPlayParametersQueueDescriptor](/documentation/mediaplayer/mpmusicplayerplayparametersqueuedescriptor)

### Creating a new play parameters queue descriptor

- [init(playParametersQueue: [MPMusicPlayerPlayParameters])](/documentation/mediaplayer/mpmusicplayerplayparametersqueuedescriptor/init(playparametersqueue:))
- [MPMusicPlayerPlayParameters](/documentation/mediaplayer/mpmusicplayerplayparameters)

#### Creating the play parameters

- [init?(dictionary: [String : Any])](/documentation/mediaplayer/mpmusicplayerplayparameters/init(dictionary:))

#### Accessing the play parameters

- [var dictionary: [String : Any]](/documentation/mediaplayer/mpmusicplayerplayparameters/dictionary)

### Accessing the play parameters

- [var playParametersQueue: [MPMusicPlayerPlayParameters]](/documentation/mediaplayer/mpmusicplayerplayparametersqueuedescriptor/playparametersqueue)
- [var startItemPlayParameters: MPMusicPlayerPlayParameters?](/documentation/mediaplayer/mpmusicplayerplayparametersqueuedescriptor/startitemplayparameters)
- [MPMusicPlayerPlayParameters](/documentation/mediaplayer/mpmusicplayerplayparameters)

#### Creating the play parameters

- [init?(dictionary: [String : Any])](/documentation/mediaplayer/mpmusicplayerplayparameters/init(dictionary:))

#### Accessing the play parameters

- [var dictionary: [String : Any]](/documentation/mediaplayer/mpmusicplayerplayparameters/dictionary)

### Setting start and end times

- [func setStartTime(TimeInterval, forItemWith: MPMusicPlayerPlayParameters)](/documentation/mediaplayer/mpmusicplayerplayparametersqueuedescriptor/setstarttime(_:foritemwith:))
- [func setEndTime(TimeInterval, forItemWith: MPMusicPlayerPlayParameters)](/documentation/mediaplayer/mpmusicplayerplayparametersqueuedescriptor/setendtime(_:foritemwith:))
- [MPMusicPlayerQueueDescriptor](/documentation/mediaplayer/mpmusicplayerqueuedescriptor)

## Media items and playlists

- [Providing animated artwork for media items](/documentation/mediaplayer/providing-animated-artwork-for-media-items)
- [MPMediaItem](/documentation/mediaplayer/mpmediaitem)

### Media item properties

- [var albumArtist: String?](/documentation/mediaplayer/mpmediaitem/albumartist)
- [var albumArtistPersistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaitem/albumartistpersistentid)
- [var albumPersistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaitem/albumpersistentid)
- [var albumTitle: String?](/documentation/mediaplayer/mpmediaitem/albumtitle)
- [var albumTrackCount: Int](/documentation/mediaplayer/mpmediaitem/albumtrackcount)
- [var albumTrackNumber: Int](/documentation/mediaplayer/mpmediaitem/albumtracknumber)
- [var artist: String?](/documentation/mediaplayer/mpmediaitem/artist)
- [var artistPersistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaitem/artistpersistentid)
- [var artwork: MPMediaItemArtwork?](/documentation/mediaplayer/mpmediaitem/artwork)
- [var assetURL: URL?](/documentation/mediaplayer/mpmediaitem/asseturl)
- [var beatsPerMinute: Int](/documentation/mediaplayer/mpmediaitem/beatsperminute)
- [var bookmarkTime: TimeInterval](/documentation/mediaplayer/mpmediaitem/bookmarktime)
- [var isCloudItem: Bool](/documentation/mediaplayer/mpmediaitem/isclouditem)
- [var comments: String?](/documentation/mediaplayer/mpmediaitem/comments)
- [var isCompilation: Bool](/documentation/mediaplayer/mpmediaitem/iscompilation)
- [var isPreorder: Bool](/documentation/mediaplayer/mpmediaitem/ispreorder)
- [var composer: String?](/documentation/mediaplayer/mpmediaitem/composer)
- [var composerPersistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaitem/composerpersistentid)
- [var dateAdded: Date](/documentation/mediaplayer/mpmediaitem/dateadded)
- [var discCount: Int](/documentation/mediaplayer/mpmediaitem/disccount)
- [var discNumber: Int](/documentation/mediaplayer/mpmediaitem/discnumber)
- [var isExplicitItem: Bool](/documentation/mediaplayer/mpmediaitem/isexplicititem)
- [var genre: String?](/documentation/mediaplayer/mpmediaitem/genre)
- [var genrePersistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaitem/genrepersistentid)
- [var lastPlayedDate: Date?](/documentation/mediaplayer/mpmediaitem/lastplayeddate)
- [var lyrics: String?](/documentation/mediaplayer/mpmediaitem/lyrics)
- [var mediaType: MPMediaType](/documentation/mediaplayer/mpmediaitem/mediatype)
- [var persistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaitem/persistentid)
- [var playCount: Int](/documentation/mediaplayer/mpmediaitem/playcount)
- [var playbackDuration: TimeInterval](/documentation/mediaplayer/mpmediaitem/playbackduration)
- [var playbackStoreID: String](/documentation/mediaplayer/mpmediaitem/playbackstoreid)
- [var podcastPersistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaitem/podcastpersistentid)
- [var podcastTitle: String?](/documentation/mediaplayer/mpmediaitem/podcasttitle)
- [var hasProtectedAsset: Bool](/documentation/mediaplayer/mpmediaitem/hasprotectedasset)
- [var rating: Int](/documentation/mediaplayer/mpmediaitem/rating)
- [var releaseDate: Date?](/documentation/mediaplayer/mpmediaitem/releasedate)
- [var skipCount: Int](/documentation/mediaplayer/mpmediaitem/skipcount)
- [var title: String?](/documentation/mediaplayer/mpmediaitem/title)
- [var userGrouping: String?](/documentation/mediaplayer/mpmediaitem/usergrouping)

### Obtaining group properties

- [class func persistentIDProperty(forGroupingType: MPMediaGrouping) -> String](/documentation/mediaplayer/mpmediaitem/persistentidproperty(forgroupingtype:))
- [class func titleProperty(forGroupingType: MPMediaGrouping) -> String](/documentation/mediaplayer/mpmediaitem/titleproperty(forgroupingtype:))

### Media item types and keys

- [MPMediaType](/documentation/mediaplayer/mpmediatype)

#### Constants

- [static var music: MPMediaType](/documentation/mediaplayer/mpmediatype/music)
- [static var podcast: MPMediaType](/documentation/mediaplayer/mpmediatype/podcast)
- [static var audioBook: MPMediaType](/documentation/mediaplayer/mpmediatype/audiobook)
- [static var audioITunesU: MPMediaType](/documentation/mediaplayer/mpmediatype/audioitunesu)
- [static var anyAudio: MPMediaType](/documentation/mediaplayer/mpmediatype/anyaudio)
- [static var movie: MPMediaType](/documentation/mediaplayer/mpmediatype/movie)
- [static var tvShow: MPMediaType](/documentation/mediaplayer/mpmediatype/tvshow)
- [static var videoPodcast: MPMediaType](/documentation/mediaplayer/mpmediatype/videopodcast)
- [static var musicVideo: MPMediaType](/documentation/mediaplayer/mpmediatype/musicvideo)
- [static var videoITunesU: MPMediaType](/documentation/mediaplayer/mpmediatype/videoitunesu)
- [static var homeVideo: MPMediaType](/documentation/mediaplayer/mpmediatype/homevideo)
- [static var anyVideo: MPMediaType](/documentation/mediaplayer/mpmediatype/anyvideo)
- [static var any: MPMediaType](/documentation/mediaplayer/mpmediatype/any)

#### Initializers

- [init(rawValue: UInt)](/documentation/mediaplayer/mpmediatype/init(rawvalue:))
- [General media item property keys](/documentation/mediaplayer/general-media-item-property-keys)

#### Property keys

- [let MPMediaItemPropertyPlaybackDuration: String](/documentation/mediaplayer/mpmediaitempropertyplaybackduration)
- [let MPMediaItemPropertyAlbumTrackNumber: String](/documentation/mediaplayer/mpmediaitempropertyalbumtracknumber)
- [let MPMediaItemPropertyAlbumTrackCount: String](/documentation/mediaplayer/mpmediaitempropertyalbumtrackcount)
- [let MPMediaItemPropertyDiscNumber: String](/documentation/mediaplayer/mpmediaitempropertydiscnumber)
- [let MPMediaItemPropertyDiscCount: String](/documentation/mediaplayer/mpmediaitempropertydisccount)
- [let MPMediaItemPropertyArtwork: String](/documentation/mediaplayer/mpmediaitempropertyartwork)
- [let MPMediaItemPropertyLyrics: String](/documentation/mediaplayer/mpmediaitempropertylyrics)
- [let MPMediaItemPropertyReleaseDate: String](/documentation/mediaplayer/mpmediaitempropertyreleasedate)
- [let MPMediaItemPropertyBeatsPerMinute: String](/documentation/mediaplayer/mpmediaitempropertybeatsperminute)
- [let MPMediaItemPropertyComments: String](/documentation/mediaplayer/mpmediaitempropertycomments)
- [let MPMediaItemPropertyAssetURL: String](/documentation/mediaplayer/mpmediaitempropertyasseturl)
- [let MPMediaItemPropertyIsExplicit: String](/documentation/mediaplayer/mpmediaitempropertyisexplicit)
- [let MPMediaItemPropertyIsPreorder: String](/documentation/mediaplayer/mpmediaitempropertyispreorder)
- [let MPMediaItemPropertyPlaybackStoreID: String](/documentation/mediaplayer/mpmediaitempropertyplaybackstoreid)

#### Filterable property keys

- [let MPMediaItemPropertyAlbumArtist: String](/documentation/mediaplayer/mpmediaitempropertyalbumartist)
- [let MPMediaItemPropertyAlbumArtistPersistentID: String](/documentation/mediaplayer/mpmediaitempropertyalbumartistpersistentid)
- [let MPMediaItemPropertyAlbumPersistentID: String](/documentation/mediaplayer/mpmediaitempropertyalbumpersistentid)
- [let MPMediaItemPropertyAlbumTitle: String](/documentation/mediaplayer/mpmediaitempropertyalbumtitle)
- [let MPMediaItemPropertyArtist: String](/documentation/mediaplayer/mpmediaitempropertyartist)
- [let MPMediaItemPropertyArtistPersistentID: String](/documentation/mediaplayer/mpmediaitempropertyartistpersistentid)
- [let MPMediaItemPropertyComposer: String](/documentation/mediaplayer/mpmediaitempropertycomposer)
- [let MPMediaItemPropertyComposerPersistentID: String](/documentation/mediaplayer/mpmediaitempropertycomposerpersistentid)
- [let MPMediaItemPropertyGenre: String](/documentation/mediaplayer/mpmediaitempropertygenre)
- [let MPMediaItemPropertyGenrePersistentID: String](/documentation/mediaplayer/mpmediaitempropertygenrepersistentid)
- [let MPMediaItemPropertyHasProtectedAsset: String](/documentation/mediaplayer/mpmediaitempropertyhasprotectedasset)
- [let MPMediaItemPropertyIsCompilation: String](/documentation/mediaplayer/mpmediaitempropertyiscompilation)
- [let MPMediaItemPropertyIsCloudItem: String](/documentation/mediaplayer/mpmediaitempropertyisclouditem)
- [let MPMediaItemPropertyMediaType: String](/documentation/mediaplayer/mpmediaitempropertymediatype)
- [let MPMediaItemPropertyPersistentID: String](/documentation/mediaplayer/mpmediaitempropertypersistentid)
- [let MPMediaItemPropertyPlayCount: String](/documentation/mediaplayer/mpmediaitempropertyplaycount)
- [let MPMediaItemPropertyPodcastPersistentID: String](/documentation/mediaplayer/mpmediaitempropertypodcastpersistentid)
- [let MPMediaItemPropertyPodcastTitle: String](/documentation/mediaplayer/mpmediaitempropertypodcasttitle)
- [let MPMediaItemPropertyTitle: String](/documentation/mediaplayer/mpmediaitempropertytitle)
- [User-defined property keys](/documentation/mediaplayer/user-defined-property-keys)

#### User-defined property keys

- [let MPMediaItemPropertySkipCount: String](/documentation/mediaplayer/mpmediaitempropertyskipcount)
- [let MPMediaItemPropertyRating: String](/documentation/mediaplayer/mpmediaitempropertyrating)
- [let MPMediaItemPropertyLastPlayedDate: String](/documentation/mediaplayer/mpmediaitempropertylastplayeddate)
- [let MPMediaItemPropertyUserGrouping: String](/documentation/mediaplayer/mpmediaitempropertyusergrouping)
- [let MPMediaItemPropertyBookmarkTime: String](/documentation/mediaplayer/mpmediaitempropertybookmarktime)
- [let MPMediaItemPropertyDateAdded: String](/documentation/mediaplayer/mpmediaitempropertydateadded)
- [MPMediaItemArtwork](/documentation/mediaplayer/mpmediaitemartwork)

### Resizing existing artwork

- [init(boundsSize: CGSize, requestHandler: (CGSize) -> UIImage)](/documentation/mediaplayer/mpmediaitemartwork/init(boundssize:requesthandler:))

### Using a media item image

- [func image(at: CGSize) -> UIImage?](/documentation/mediaplayer/mpmediaitemartwork/image(at:))
- [var bounds: CGRect](/documentation/mediaplayer/mpmediaitemartwork/bounds)

### Initializers

- [convenience init(image: UIImage)](/documentation/mediaplayer/mpmediaitemartwork/init(image:))

### Instance Properties

- [var imageCropRect: CGRect](/documentation/mediaplayer/mpmediaitemartwork/imagecroprect)
- [MPMediaItemAnimatedArtwork](/documentation/mediaplayer/mpmediaitemanimatedartwork)

### Initializers

- [convenience init(artworkID: String, previewImageRequestHandler: (CGSize) async -> UIImage?, videoAssetFileURLRequestHandler: (CGSize) async -> URL?)](/documentation/mediaplayer/mpmediaitemanimatedartwork/init(artworkid:previewimagerequesthandler:videoassetfileurlrequesthandler:)-7bb3j)
- [convenience init(artworkID: String, previewImageRequestHandler: (CGSize) async -> NSImage?, videoAssetFileURLRequestHandler: (CGSize) async -> URL?)](/documentation/mediaplayer/mpmediaitemanimatedartwork/init(artworkid:previewimagerequesthandler:videoassetfileurlrequesthandler:)-7n23z)
- [init(artworkID: String, previewImageRequestHandler: (CGSize, (UIImage?) -> Void) -> Void, videoAssetFileURLRequestHandler: (CGSize, (URL?) -> Void) -> Void)](/documentation/mediaplayer/mpmediaitemanimatedartwork/init(artworkid:previewimagerequesthandler:videoassetfileurlrequesthandler:)-ieue)
- [MPMediaItemCollection](/documentation/mediaplayer/mpmediaitemcollection)

### Creating a media item collection

- [init(items: [MPMediaItem])](/documentation/mediaplayer/mpmediaitemcollection/init(items:))

### Using a media item collection

- [var items: [MPMediaItem]](/documentation/mediaplayer/mpmediaitemcollection/items)
- [var representativeItem: MPMediaItem?](/documentation/mediaplayer/mpmediaitemcollection/representativeitem)
- [var count: Int](/documentation/mediaplayer/mpmediaitemcollection/count)
- [var mediaTypes: MPMediaType](/documentation/mediaplayer/mpmediaitemcollection/mediatypes)
- [MPMediaPlaylist](/documentation/mediaplayer/mpmediaplaylist)

### Adding media items to a playlist

- [func addItem(withProductID: String, completionHandler: (((any Error)?) -> Void)?)](/documentation/mediaplayer/mpmediaplaylist/additem(withproductid:completionhandler:))
- [func add([MPMediaItem], completionHandler: (((any Error)?) -> Void)?)](/documentation/mediaplayer/mpmediaplaylist/add(_:completionhandler:))

### Retrieving information about a playlist

- [var authorDisplayName: String?](/documentation/mediaplayer/mpmediaplaylist/authordisplayname)
- [var descriptionText: String?](/documentation/mediaplayer/mpmediaplaylist/descriptiontext)
- [var name: String?](/documentation/mediaplayer/mpmediaplaylist/name)
- [var persistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaplaylist/persistentid)
- [var cloudGlobalID: String?](/documentation/mediaplayer/mpmediaplaylist/cloudglobalid)
- [var playlistAttributes: MPMediaPlaylistAttribute](/documentation/mediaplayer/mpmediaplaylist/playlistattributes)
- [MPMediaPlaylistAttribute](/documentation/mediaplayer/mpmediaplaylistattribute)

#### Constants

- [static var onTheGo: MPMediaPlaylistAttribute](/documentation/mediaplayer/mpmediaplaylistattribute/onthego)
- [static var smart: MPMediaPlaylistAttribute](/documentation/mediaplayer/mpmediaplaylistattribute/smart)
- [static var genius: MPMediaPlaylistAttribute](/documentation/mediaplayer/mpmediaplaylistattribute/genius)

#### Initializers

- [init(rawValue: UInt)](/documentation/mediaplayer/mpmediaplaylistattribute/init(rawvalue:))
- [var seedItems: [MPMediaItem]?](/documentation/mediaplayer/mpmediaplaylist/seeditems)

### Property keys

- [Playlist property keys](/documentation/mediaplayer/playlist-property-keys)

#### Property keys

- [let MPMediaPlaylistPropertyAuthorDisplayName: String](/documentation/mediaplayer/mpmediaplaylistpropertyauthordisplayname)
- [let MPMediaPlaylistPropertyName: String](/documentation/mediaplayer/mpmediaplaylistpropertyname)
- [let MPMediaPlaylistPropertyDescriptionText: String](/documentation/mediaplayer/mpmediaplaylistpropertydescriptiontext)
- [let MPMediaPlaylistPropertyPersistentID: String](/documentation/mediaplayer/mpmediaplaylistpropertypersistentid)
- [let MPMediaPlaylistPropertyPlaylistAttributes: String](/documentation/mediaplayer/mpmediaplaylistpropertyplaylistattributes)
- [let MPMediaPlaylistPropertyCloudGlobalID: String](/documentation/mediaplayer/mpmediaplaylistpropertycloudglobalid)
- [let MPMediaPlaylistPropertySeedItems: String](/documentation/mediaplayer/mpmediaplaylistpropertyseeditems)
- [MPMediaPlaylistCreationMetadata](/documentation/mediaplayer/mpmediaplaylistcreationmetadata)

### Creating metadata for a playlist

- [init(name: String)](/documentation/mediaplayer/mpmediaplaylistcreationmetadata/init(name:))

### Metadata for a playlist

- [var authorDisplayName: String!](/documentation/mediaplayer/mpmediaplaylistcreationmetadata/authordisplayname)
- [var descriptionText: String](/documentation/mediaplayer/mpmediaplaylistcreationmetadata/descriptiontext)
- [var name: String](/documentation/mediaplayer/mpmediaplaylistcreationmetadata/name)
- [MPMediaEntity](/documentation/mediaplayer/mpmediaentity)

### Working with media properties

- [class func canFilter(byProperty: String) -> Bool](/documentation/mediaplayer/mpmediaentity/canfilter(byproperty:))
- [func enumerateValues(forProperties: Set<String>, using: (String, Any, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/mediaplayer/mpmediaentity/enumeratevalues(forproperties:using:))
- [var persistentID: MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaentity/persistentid)
- [subscript(Any) -> Any?](/documentation/mediaplayer/mpmediaentity/subscript(_:))
- [func value(forProperty: String) -> Any?](/documentation/mediaplayer/mpmediaentity/value(forproperty:))
- [MPMediaEntityPersistentID](/documentation/mediaplayer/mpmediaentitypersistentid)

### Media entity property keys

- [Media entity property keys](/documentation/mediaplayer/media-entity-property-keys)

#### Constants

- [let MPMediaEntityPropertyPersistentID: String](/documentation/mediaplayer/mpmediaentitypropertypersistentid)

## Media player user interface

- [Displaying a media picker from your app](/documentation/mediaplayer/displaying-a-media-picker-from-your-app)
- [MPMediaPickerController](/documentation/mediaplayer/mpmediapickercontroller)

### Initializing a media item picker

- [init(mediaTypes: MPMediaType)](/documentation/mediaplayer/mpmediapickercontroller/init(mediatypes:))

### Responding to media item picker selections

- [var delegate: (any MPMediaPickerControllerDelegate)?](/documentation/mediaplayer/mpmediapickercontroller/delegate)
- [MPMediaPickerControllerDelegate](/documentation/mediaplayer/mpmediapickercontrollerdelegate)

#### Responding to user actions

- [func mediaPicker(MPMediaPickerController, didPickMediaItems: MPMediaItemCollection)](/documentation/mediaplayer/mpmediapickercontrollerdelegate/mediapicker(_:didpickmediaitems:))
- [func mediaPickerDidCancel(MPMediaPickerController)](/documentation/mediaplayer/mpmediapickercontrollerdelegate/mediapickerdidcancel(_:))

### Using a media item picker

- [var allowsPickingMultipleItems: Bool](/documentation/mediaplayer/mpmediapickercontroller/allowspickingmultipleitems)
- [var showsCloudItems: Bool](/documentation/mediaplayer/mpmediapickercontroller/showsclouditems)
- [var mediaTypes: MPMediaType](/documentation/mediaplayer/mpmediapickercontroller/mediatypes)
- [var prompt: String?](/documentation/mediaplayer/mpmediapickercontroller/prompt)
- [var showsItemsWithProtectedAssets: Bool](/documentation/mediaplayer/mpmediapickercontroller/showsitemswithprotectedassets)
- [MPVolumeView](/documentation/mediaplayer/mpvolumeview)

### Managing visibility of controls

- [var showsVolumeSlider: Bool](/documentation/mediaplayer/mpvolumeview/showsvolumeslider)

### Customizing the volume slider

- [func maximumVolumeSliderImage(for: UIControl.State) -> UIImage?](/documentation/mediaplayer/mpvolumeview/maximumvolumesliderimage(for:))
- [func minimumVolumeSliderImage(for: UIControl.State) -> UIImage?](/documentation/mediaplayer/mpvolumeview/minimumvolumesliderimage(for:))
- [func setMaximumVolumeSliderImage(UIImage?, for: UIControl.State)](/documentation/mediaplayer/mpvolumeview/setmaximumvolumesliderimage(_:for:))
- [func setMinimumVolumeSliderImage(UIImage?, for: UIControl.State)](/documentation/mediaplayer/mpvolumeview/setminimumvolumesliderimage(_:for:))
- [func setVolumeThumbImage(UIImage?, for: UIControl.State)](/documentation/mediaplayer/mpvolumeview/setvolumethumbimage(_:for:))
- [func volumeSliderRect(forBounds: CGRect) -> CGRect](/documentation/mediaplayer/mpvolumeview/volumesliderrect(forbounds:))
- [func volumeThumbImage(for: UIControl.State) -> UIImage?](/documentation/mediaplayer/mpvolumeview/volumethumbimage(for:))
- [func volumeThumbRect(forBounds: CGRect, volumeSliderRect: CGRect, value: Float) -> CGRect](/documentation/mediaplayer/mpvolumeview/volumethumbrect(forbounds:volumesliderrect:value:))

### Deprecated

- [var volumeWarningSliderImage: UIImage?](/documentation/mediaplayer/mpvolumeview/volumewarningsliderimage)
- [var showsRouteButton: Bool](/documentation/mediaplayer/mpvolumeview/showsroutebutton)
- [var areWirelessRoutesAvailable: Bool](/documentation/mediaplayer/mpvolumeview/arewirelessroutesavailable)
- [var isWirelessRouteActive: Bool](/documentation/mediaplayer/mpvolumeview/iswirelessrouteactive)
- [func routeButtonImage(for: UIControl.State) -> UIImage?](/documentation/mediaplayer/mpvolumeview/routebuttonimage(for:))
- [func routeButtonRect(forBounds: CGRect) -> CGRect](/documentation/mediaplayer/mpvolumeview/routebuttonrect(forbounds:))
- [func setRouteButtonImage(UIImage?, for: UIControl.State)](/documentation/mediaplayer/mpvolumeview/setroutebuttonimage(_:for:))

## Now Playing information

- [Becoming a now playable app](/documentation/mediaplayer/becoming-a-now-playable-app)
- [MPNowPlayingSession](/documentation/mediaplayer/mpnowplayingsession)

### Creating a session

- [init(players: [AVPlayer])](/documentation/mediaplayer/mpnowplayingsession/init(players:))

### Accessing the delegate object

- [var delegate: (any MPNowPlayingSessionDelegate)?](/documentation/mediaplayer/mpnowplayingsession/delegate)
- [MPNowPlayingSessionDelegate](/documentation/mediaplayer/mpnowplayingsessiondelegate)

#### Responding to state changes

- [func nowPlayingSessionDidChangeActive(MPNowPlayingSession)](/documentation/mediaplayer/mpnowplayingsessiondelegate/nowplayingsessiondidchangeactive(_:))
- [func nowPlayingSessionDidChangeCanBecomeActive(MPNowPlayingSession)](/documentation/mediaplayer/mpnowplayingsessiondelegate/nowplayingsessiondidchangecanbecomeactive(_:))

### Managing players

- [var players: [AVPlayer]](/documentation/mediaplayer/mpnowplayingsession/players)
- [func addPlayer(AVPlayer)](/documentation/mediaplayer/mpnowplayingsession/addplayer(_:))
- [func removePlayer(AVPlayer)](/documentation/mediaplayer/mpnowplayingsession/removeplayer(_:))

### Managing the active state

- [var isActive: Bool](/documentation/mediaplayer/mpnowplayingsession/isactive)
- [var canBecomeActive: Bool](/documentation/mediaplayer/mpnowplayingsession/canbecomeactive)
- [func becomeActiveIfPossible(completion: ((Bool) -> Void)?)](/documentation/mediaplayer/mpnowplayingsession/becomeactiveifpossible(completion:))

### Configuring Now Playing information

- [var automaticallyPublishesNowPlayingInfo: Bool](/documentation/mediaplayer/mpnowplayingsession/automaticallypublishesnowplayinginfo)
- [var nowPlayingInfoCenter: MPNowPlayingInfoCenter](/documentation/mediaplayer/mpnowplayingsession/nowplayinginfocenter)

### Handling remote commands

- [var remoteCommandCenter: MPRemoteCommandCenter](/documentation/mediaplayer/mpnowplayingsession/remotecommandcenter)
- [MPNowPlayingInfoCenter](/documentation/mediaplayer/mpnowplayinginfocenter)

### Working with the default Now Playing info center

- [class func `default`() -> MPNowPlayingInfoCenter](/documentation/mediaplayer/mpnowplayinginfocenter/default())
- [var nowPlayingInfo: [String : Any]?](/documentation/mediaplayer/mpnowplayinginfocenter/nowplayinginfo)
- [MPNowPlayingInfoMediaType](/documentation/mediaplayer/mpnowplayinginfomediatype)

#### Media types

- [case none](/documentation/mediaplayer/mpnowplayinginfomediatype/none)
- [case audio](/documentation/mediaplayer/mpnowplayinginfomediatype/audio)
- [case video](/documentation/mediaplayer/mpnowplayinginfomediatype/video)

#### Initializers

- [init?(rawValue: UInt)](/documentation/mediaplayer/mpnowplayinginfomediatype/init(rawvalue:))
- [class var supportedAnimatedArtworkKeys: [String]](/documentation/mediaplayer/mpnowplayinginfocenter/supportedanimatedartworkkeys)

### Setting the playback state in macOS

- [var playbackState: MPNowPlayingPlaybackState](/documentation/mediaplayer/mpnowplayinginfocenter/playbackstate)
- [MPNowPlayingPlaybackState](/documentation/mediaplayer/mpnowplayingplaybackstate)

#### Playback states

- [case unknown](/documentation/mediaplayer/mpnowplayingplaybackstate/unknown)
- [case playing](/documentation/mediaplayer/mpnowplayingplaybackstate/playing)
- [case paused](/documentation/mediaplayer/mpnowplayingplaybackstate/paused)
- [case stopped](/documentation/mediaplayer/mpnowplayingplaybackstate/stopped)
- [case interrupted](/documentation/mediaplayer/mpnowplayingplaybackstate/interrupted)

#### Initializers

- [init?(rawValue: UInt)](/documentation/mediaplayer/mpnowplayingplaybackstate/init(rawvalue:))

### Accessing Now Playing metadata properties

- [let MPNowPlayingInfoCollectionIdentifier: String](/documentation/mediaplayer/mpnowplayinginfocollectionidentifier)
- [let MPNowPlayingInfoPropertyAdTimeRanges: String](/documentation/mediaplayer/mpnowplayinginfopropertyadtimeranges)

#### Ad time ranges

- [MPAdTimeRange](/documentation/mediaplayer/mpadtimerange)

##### Creating an Ad Time Range

- [init(CMTimeRange)](/documentation/mediaplayer/mpadtimerange/init(_:))

##### Inspecting an Ad Time Range

- [var timeRange: CMTimeRange](/documentation/mediaplayer/mpadtimerange/timerange)
- [let MPNowPlayingInfoPropertyAvailableLanguageOptions: String](/documentation/mediaplayer/mpnowplayinginfopropertyavailablelanguageoptions)
- [let MPNowPlayingInfoPropertyAssetURL: String](/documentation/mediaplayer/mpnowplayinginfopropertyasseturl)
- [let MPNowPlayingInfoPropertyChapterCount: String](/documentation/mediaplayer/mpnowplayinginfopropertychaptercount)
- [let MPNowPlayingInfoPropertyChapterNumber: String](/documentation/mediaplayer/mpnowplayinginfopropertychapternumber)
- [let MPNowPlayingInfoPropertyCreditsStartTime: String](/documentation/mediaplayer/mpnowplayinginfopropertycreditsstarttime)
- [let MPNowPlayingInfoPropertyCurrentLanguageOptions: String](/documentation/mediaplayer/mpnowplayinginfopropertycurrentlanguageoptions)
- [let MPNowPlayingInfoPropertyCurrentPlaybackDate: String](/documentation/mediaplayer/mpnowplayinginfopropertycurrentplaybackdate)
- [let MPNowPlayingInfoPropertyDefaultPlaybackRate: String](/documentation/mediaplayer/mpnowplayinginfopropertydefaultplaybackrate)
- [let MPNowPlayingInfoPropertyElapsedPlaybackTime: String](/documentation/mediaplayer/mpnowplayinginfopropertyelapsedplaybacktime)
- [let MPNowPlayingInfoPropertyExcludeFromSuggestions: String](/documentation/mediaplayer/mpnowplayinginfopropertyexcludefromsuggestions)
- [let MPNowPlayingInfoPropertyExternalContentIdentifier: String](/documentation/mediaplayer/mpnowplayinginfopropertyexternalcontentidentifier)
- [let MPNowPlayingInfoPropertyExternalUserProfileIdentifier: String](/documentation/mediaplayer/mpnowplayinginfopropertyexternaluserprofileidentifier)
- [let MPNowPlayingInfoPropertyInternationalStandardRecordingCode: String](/documentation/mediaplayer/mpnowplayinginfopropertyinternationalstandardrecordingcode)
- [let MPNowPlayingInfoPropertyIsLiveStream: String](/documentation/mediaplayer/mpnowplayinginfopropertyislivestream)
- [let MPNowPlayingInfoPropertyMediaType: String](/documentation/mediaplayer/mpnowplayinginfopropertymediatype)
- [let MPNowPlayingInfoPropertyPlaybackProgress: String](/documentation/mediaplayer/mpnowplayinginfopropertyplaybackprogress)
- [let MPNowPlayingInfoPropertyPlaybackRate: String](/documentation/mediaplayer/mpnowplayinginfopropertyplaybackrate)
- [let MPNowPlayingInfoPropertyPlaybackQueueCount: String](/documentation/mediaplayer/mpnowplayinginfopropertyplaybackqueuecount)
- [let MPNowPlayingInfoPropertyPlaybackQueueIndex: String](/documentation/mediaplayer/mpnowplayinginfopropertyplaybackqueueindex)
- [let MPNowPlayingInfoPropertyServiceIdentifier: String](/documentation/mediaplayer/mpnowplayinginfopropertyserviceidentifier)
- [let MPNowPlayingInfoProperty1x1AnimatedArtwork: String](/documentation/mediaplayer/mpnowplayinginfoproperty1x1animatedartwork)
- [let MPNowPlayingInfoProperty3x4AnimatedArtwork: String](/documentation/mediaplayer/mpnowplayinginfoproperty3x4animatedartwork)
- [MPNowPlayingInfoLanguageOption](/documentation/mediaplayer/mpnowplayinginfolanguageoption)

### Creating a new language option

- [init(type: MPNowPlayingInfoLanguageOptionType, languageTag: String, characteristics: [String]?, displayName: String, identifier: String)](/documentation/mediaplayer/mpnowplayinginfolanguageoption/init(type:languagetag:characteristics:displayname:identifier:))

### Retrieving language option properties

- [var displayName: String?](/documentation/mediaplayer/mpnowplayinginfolanguageoption/displayname)
- [var identifier: String?](/documentation/mediaplayer/mpnowplayinginfolanguageoption/identifier)
- [var languageOptionCharacteristics: [String]?](/documentation/mediaplayer/mpnowplayinginfolanguageoption/languageoptioncharacteristics)
- [var languageTag: String?](/documentation/mediaplayer/mpnowplayinginfolanguageoption/languagetag)
- [var languageOptionType: MPNowPlayingInfoLanguageOptionType](/documentation/mediaplayer/mpnowplayinginfolanguageoption/languageoptiontype)
- [MPNowPlayingInfoLanguageOptionType](/documentation/mediaplayer/mpnowplayinginfolanguageoptiontype)

#### Enumeration Cases

- [case audible](/documentation/mediaplayer/mpnowplayinginfolanguageoptiontype/audible)
- [case legible](/documentation/mediaplayer/mpnowplayinginfolanguageoptiontype/legible)

#### Initializers

- [init?(rawValue: UInt)](/documentation/mediaplayer/mpnowplayinginfolanguageoptiontype/init(rawvalue:))

### Retrieving a language option based on system preferences

- [func isAutomaticAudibleLanguageOption() -> Bool](/documentation/mediaplayer/mpnowplayinginfolanguageoption/isautomaticaudiblelanguageoption())
- [func isAutomaticLegibleLanguageOption() -> Bool](/documentation/mediaplayer/mpnowplayinginfolanguageoption/isautomaticlegiblelanguageoption())
- [MPNowPlayingInfoLanguageOptionGroup](/documentation/mediaplayer/mpnowplayinginfolanguageoptiongroup)

### Creating a new language option group

- [init(languageOptions: [MPNowPlayingInfoLanguageOption], defaultLanguageOption: MPNowPlayingInfoLanguageOption?, allowEmptySelection: Bool)](/documentation/mediaplayer/mpnowplayinginfolanguageoptiongroup/init(languageoptions:defaultlanguageoption:allowemptyselection:))

### Retrieving language option group information

- [var allowEmptySelection: Bool](/documentation/mediaplayer/mpnowplayinginfolanguageoptiongroup/allowemptyselection)
- [var defaultLanguageOption: MPNowPlayingInfoLanguageOption?](/documentation/mediaplayer/mpnowplayinginfolanguageoptiongroup/defaultlanguageoption)
- [var languageOptions: [MPNowPlayingInfoLanguageOption]](/documentation/mediaplayer/mpnowplayinginfolanguageoptiongroup/languageoptions)
- [Language option characteristic constants](/documentation/mediaplayer/language-option-characteristic-constants)

### Language option characteristic constants

- [let MPLanguageOptionCharacteristicContainsOnlyForcedSubtitles: String](/documentation/mediaplayer/mplanguageoptioncharacteristiccontainsonlyforcedsubtitles)
- [let MPLanguageOptionCharacteristicDescribesMusicAndSound: String](/documentation/mediaplayer/mplanguageoptioncharacteristicdescribesmusicandsound)
- [let MPLanguageOptionCharacteristicDescribesVideo: String](/documentation/mediaplayer/mplanguageoptioncharacteristicdescribesvideo)
- [let MPLanguageOptionCharacteristicDubbedTranslation: String](/documentation/mediaplayer/mplanguageoptioncharacteristicdubbedtranslation)
- [let MPLanguageOptionCharacteristicEasyToRead: String](/documentation/mediaplayer/mplanguageoptioncharacteristiceasytoread)
- [let MPLanguageOptionCharacteristicIsAuxiliaryContent: String](/documentation/mediaplayer/mplanguageoptioncharacteristicisauxiliarycontent)
- [let MPLanguageOptionCharacteristicIsMainProgramContent: String](/documentation/mediaplayer/mplanguageoptioncharacteristicismainprogramcontent)
- [let MPLanguageOptionCharacteristicLanguageTranslation: String](/documentation/mediaplayer/mplanguageoptioncharacteristiclanguagetranslation)
- [let MPLanguageOptionCharacteristicTranscribesSpokenDialog: String](/documentation/mediaplayer/mplanguageoptioncharacteristictranscribesspokendialog)
- [let MPLanguageOptionCharacteristicVoiceOverTranslation: String](/documentation/mediaplayer/mplanguageoptioncharacteristicvoiceovertranslation)

## External player and system event handling

- [Handling external player events notifications](/documentation/mediaplayer/handling-external-player-events-notifications)
- [Remote command center events](/documentation/mediaplayer/remote-command-center-events)

### Setting up the remote event handler

- [Becoming a now playable app](/documentation/mediaplayer/becoming-a-now-playable-app)
- [MPRemoteCommandCenter](/documentation/mediaplayer/mpremotecommandcenter)

#### Retrieving the shared instance

- [class func shared() -> MPRemoteCommandCenter](/documentation/mediaplayer/mpremotecommandcenter/shared())

#### Playback commands

- [var pauseCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/pausecommand)
- [var playCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/playcommand)
- [var stopCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/stopcommand)
- [var togglePlayPauseCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/toggleplaypausecommand)

#### Navigating between tracks

- [var nextTrackCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/nexttrackcommand)
- [var previousTrackCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/previoustrackcommand)
- [var changeRepeatModeCommand: MPChangeRepeatModeCommand](/documentation/mediaplayer/mpremotecommandcenter/changerepeatmodecommand)
- [var changeShuffleModeCommand: MPChangeShuffleModeCommand](/documentation/mediaplayer/mpremotecommandcenter/changeshufflemodecommand)

#### Navigating a track’s contents

- [var changePlaybackRateCommand: MPChangePlaybackRateCommand](/documentation/mediaplayer/mpremotecommandcenter/changeplaybackratecommand)
- [var seekBackwardCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/seekbackwardcommand)
- [var seekForwardCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/seekforwardcommand)
- [var skipBackwardCommand: MPSkipIntervalCommand](/documentation/mediaplayer/mpremotecommandcenter/skipbackwardcommand)
- [var skipForwardCommand: MPSkipIntervalCommand](/documentation/mediaplayer/mpremotecommandcenter/skipforwardcommand)
- [var changePlaybackPositionCommand: MPChangePlaybackPositionCommand](/documentation/mediaplayer/mpremotecommandcenter/changeplaybackpositioncommand)

#### Rating a media item

- [var ratingCommand: MPRatingCommand](/documentation/mediaplayer/mpremotecommandcenter/ratingcommand)
- [var likeCommand: MPFeedbackCommand](/documentation/mediaplayer/mpremotecommandcenter/likecommand)
- [var dislikeCommand: MPFeedbackCommand](/documentation/mediaplayer/mpremotecommandcenter/dislikecommand)

#### Bookmarking a media item

- [var bookmarkCommand: MPFeedbackCommand](/documentation/mediaplayer/mpremotecommandcenter/bookmarkcommand)

#### Enabling language options

- [var enableLanguageOptionCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/enablelanguageoptioncommand)
- [var disableLanguageOptionCommand: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandcenter/disablelanguageoptioncommand)
- [MPRemoteCommand](/documentation/mediaplayer/mpremotecommand)

#### Handling events

- [func addTarget(handler: (MPRemoteCommandEvent) -> MPRemoteCommandHandlerStatus) -> Any](/documentation/mediaplayer/mpremotecommand/addtarget(handler:))
- [func addTarget(Any, action: Selector)](/documentation/mediaplayer/mpremotecommand/addtarget(_:action:))
- [func removeTarget(Any?)](/documentation/mediaplayer/mpremotecommand/removetarget(_:))
- [func removeTarget(Any, action: Selector?)](/documentation/mediaplayer/mpremotecommand/removetarget(_:action:))
- [MPRemoteCommandHandlerStatus](/documentation/mediaplayer/mpremotecommandhandlerstatus)

##### Constants

- [case success](/documentation/mediaplayer/mpremotecommandhandlerstatus/success)
- [case noSuchContent](/documentation/mediaplayer/mpremotecommandhandlerstatus/nosuchcontent)
- [case noActionableNowPlayingItem](/documentation/mediaplayer/mpremotecommandhandlerstatus/noactionablenowplayingitem)
- [case deviceNotFound](/documentation/mediaplayer/mpremotecommandhandlerstatus/devicenotfound)
- [case commandFailed](/documentation/mediaplayer/mpremotecommandhandlerstatus/commandfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpremotecommandhandlerstatus/init(rawvalue:))

#### Enabling a command object

- [var isEnabled: Bool](/documentation/mediaplayer/mpremotecommand/isenabled)
- [MPRemoteCommandEvent](/documentation/mediaplayer/mpremotecommandevent)

#### Retrieving command information

- [var command: MPRemoteCommand](/documentation/mediaplayer/mpremotecommandevent/command)
- [var timestamp: TimeInterval](/documentation/mediaplayer/mpremotecommandevent/timestamp)
- [Track navigation events](/documentation/mediaplayer/track-navigation-events)

### Responding to track navigation events

- [MPChangePlaybackPositionCommand](/documentation/mediaplayer/mpchangeplaybackpositioncommand)
- [MPChangePlaybackPositionCommandEvent](/documentation/mediaplayer/mpchangeplaybackpositioncommandevent)

#### Retrieving the position time

- [var positionTime: TimeInterval](/documentation/mediaplayer/mpchangeplaybackpositioncommandevent/positiontime)
- [MPSeekCommandEvent](/documentation/mediaplayer/mpseekcommandevent)

#### Changing the current seek behavior

- [var type: MPSeekCommandEventType](/documentation/mediaplayer/mpseekcommandevent/type)

#### Constants

- [MPSeekCommandEventType](/documentation/mediaplayer/mpseekcommandeventtype)

##### Event types

- [case beginSeeking](/documentation/mediaplayer/mpseekcommandeventtype/beginseeking)
- [case endSeeking](/documentation/mediaplayer/mpseekcommandeventtype/endseeking)

##### Initializers

- [init?(rawValue: UInt)](/documentation/mediaplayer/mpseekcommandeventtype/init(rawvalue:))
- [MPSkipIntervalCommand](/documentation/mediaplayer/mpskipintervalcommand)

#### Retrieving skip intervals

- [var preferredIntervals: [NSNumber]](/documentation/mediaplayer/mpskipintervalcommand/preferredintervals)
- [MPSkipIntervalCommandEvent](/documentation/mediaplayer/mpskipintervalcommandevent)

#### Retrieving the skip interval

- [var interval: TimeInterval](/documentation/mediaplayer/mpskipintervalcommandevent/interval)
- [Media playback mode events](/documentation/mediaplayer/media-playback-mode-events)

### Responding to changes to media playback mode events

- [MPChangePlaybackRateCommand](/documentation/mediaplayer/mpchangeplaybackratecommand)

#### Retrieving playback rates

- [var supportedPlaybackRates: [NSNumber]](/documentation/mediaplayer/mpchangeplaybackratecommand/supportedplaybackrates)
- [MPChangePlaybackRateCommandEvent](/documentation/mediaplayer/mpchangeplaybackratecommandevent)

#### Retrieving the playback rate

- [var playbackRate: Float](/documentation/mediaplayer/mpchangeplaybackratecommandevent/playbackrate)
- [MPChangeLanguageOptionCommandEvent](/documentation/mediaplayer/mpchangelanguageoptioncommandevent)

#### Changing the language option

- [var languageOption: MPNowPlayingInfoLanguageOption](/documentation/mediaplayer/mpchangelanguageoptioncommandevent/languageoption)
- [var setting: MPChangeLanguageOptionSetting](/documentation/mediaplayer/mpchangelanguageoptioncommandevent/setting)
- [MPChangeLanguageOptionSetting](/documentation/mediaplayer/mpchangelanguageoptionsetting)

##### Enumeration Cases

- [case none](/documentation/mediaplayer/mpchangelanguageoptionsetting/none)
- [case nowPlayingItemOnly](/documentation/mediaplayer/mpchangelanguageoptionsetting/nowplayingitemonly)
- [case permanent](/documentation/mediaplayer/mpchangelanguageoptionsetting/permanent)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpchangelanguageoptionsetting/init(rawvalue:))
- [MPChangeRepeatModeCommand](/documentation/mediaplayer/mpchangerepeatmodecommand)

#### Retrieving the current repeat option

- [var currentRepeatType: MPRepeatType](/documentation/mediaplayer/mpchangerepeatmodecommand/currentrepeattype)
- [MPChangeRepeatModeCommandEvent](/documentation/mediaplayer/mpchangerepeatmodecommandevent)

#### Changing the repeat type

- [var repeatType: MPRepeatType](/documentation/mediaplayer/mpchangerepeatmodecommandevent/repeattype)
- [var preservesRepeatMode: Bool](/documentation/mediaplayer/mpchangerepeatmodecommandevent/preservesrepeatmode)
- [MPChangeShuffleModeCommand](/documentation/mediaplayer/mpchangeshufflemodecommand)

#### Retrieving the current shuffle mode

- [var currentShuffleType: MPShuffleType](/documentation/mediaplayer/mpchangeshufflemodecommand/currentshuffletype)
- [MPChangeShuffleModeCommandEvent](/documentation/mediaplayer/mpchangeshufflemodecommandevent)

#### Changing the shuffle mode

- [var shuffleType: MPShuffleType](/documentation/mediaplayer/mpchangeshufflemodecommandevent/shuffletype)
- [var preservesShuffleMode: Bool](/documentation/mediaplayer/mpchangeshufflemodecommandevent/preservesshufflemode)
- [MPRepeatType](/documentation/mediaplayer/mprepeattype)

#### Repeat types

- [case off](/documentation/mediaplayer/mprepeattype/off)
- [case one](/documentation/mediaplayer/mprepeattype/one)
- [case all](/documentation/mediaplayer/mprepeattype/all)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mprepeattype/init(rawvalue:))
- [MPShuffleType](/documentation/mediaplayer/mpshuffletype)

#### Shuffle types

- [case off](/documentation/mediaplayer/mpshuffletype/off)
- [case items](/documentation/mediaplayer/mpshuffletype/items)
- [case collections](/documentation/mediaplayer/mpshuffletype/collections)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpshuffletype/init(rawvalue:))
- [Feedback and rating events](/documentation/mediaplayer/feedback-and-rating-events)

### Responding to feedback and rating events

- [MPFeedbackCommand](/documentation/mediaplayer/mpfeedbackcommand)

#### Retrieving information about a feedback command

- [var isActive: Bool](/documentation/mediaplayer/mpfeedbackcommand/isactive)
- [var localizedTitle: String](/documentation/mediaplayer/mpfeedbackcommand/localizedtitle)
- [var localizedShortTitle: String](/documentation/mediaplayer/mpfeedbackcommand/localizedshorttitle)
- [MPFeedbackCommandEvent](/documentation/mediaplayer/mpfeedbackcommandevent)

#### Determining the type of feedback action

- [var isNegative: Bool](/documentation/mediaplayer/mpfeedbackcommandevent/isnegative)
- [MPRatingCommand](/documentation/mediaplayer/mpratingcommand)

#### Defining maximum and minimum ratings

- [var maximumRating: Float](/documentation/mediaplayer/mpratingcommand/maximumrating)
- [var minimumRating: Float](/documentation/mediaplayer/mpratingcommand/minimumrating)
- [MPRatingCommandEvent](/documentation/mediaplayer/mpratingcommandevent)

#### Rating a media item

- [var rating: Float](/documentation/mediaplayer/mpratingcommandevent/rating)

## External media player items

- [MPContentItem](/documentation/mediaplayer/mpcontentitem)

### Setting a unique identifier

- [init(identifier: String)](/documentation/mediaplayer/mpcontentitem/init(identifier:))

### Retrieving information about a media item

- [var artwork: MPMediaItemArtwork?](/documentation/mediaplayer/mpcontentitem/artwork)
- [var isContainer: Bool](/documentation/mediaplayer/mpcontentitem/iscontainer)
- [var isExplicitContent: Bool](/documentation/mediaplayer/mpcontentitem/isexplicitcontent)
- [var identifier: String](/documentation/mediaplayer/mpcontentitem/identifier)
- [var isPlayable: Bool](/documentation/mediaplayer/mpcontentitem/isplayable)
- [var isStreamingContent: Bool](/documentation/mediaplayer/mpcontentitem/isstreamingcontent)
- [var playbackProgress: Float](/documentation/mediaplayer/mpcontentitem/playbackprogress)
- [var subtitle: String?](/documentation/mediaplayer/mpcontentitem/subtitle)
- [var title: String?](/documentation/mediaplayer/mpcontentitem/title)

## Media player errors

- [MPError](/documentation/mediaplayer/mperror)

### Inspecting an error

- [static var errorDomain: String](/documentation/mediaplayer/mperror/errordomain)
- [let MPErrorDomain: String](/documentation/mediaplayer/mperrordomain)
- [MPError.Code](/documentation/mediaplayer/mperror/code)

#### Error codes

- [case cancelled](/documentation/mediaplayer/mperror/code/cancelled)
- [case cloudServiceCapabilityMissing](/documentation/mediaplayer/mperror/code/cloudservicecapabilitymissing)
- [case networkConnectionFailed](/documentation/mediaplayer/mperror/code/networkconnectionfailed)
- [case notFound](/documentation/mediaplayer/mperror/code/notfound)
- [case notSupported](/documentation/mediaplayer/mperror/code/notsupported)
- [case permissionDenied](/documentation/mediaplayer/mperror/code/permissiondenied)
- [case requestTimedOut](/documentation/mediaplayer/mperror/code/requesttimedout)
- [case unknown](/documentation/mediaplayer/mperror/code/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mperror/code/init(rawvalue:))
- [Error constants](/documentation/mediaplayer/error-constants)

#### Error code constants

- [static var cancelled: MPError.Code](/documentation/mediaplayer/mperror/cancelled)
- [static var cloudServiceCapabilityMissing: MPError.Code](/documentation/mediaplayer/mperror/cloudservicecapabilitymissing)
- [static var unknown: MPError.Code](/documentation/mediaplayer/mperror/unknown)
- [static var networkConnectionFailed: MPError.Code](/documentation/mediaplayer/mperror/networkconnectionfailed)
- [static var notFound: MPError.Code](/documentation/mediaplayer/mperror/notfound)
- [static var notSupported: MPError.Code](/documentation/mediaplayer/mperror/notsupported)
- [static var permissionDenied: MPError.Code](/documentation/mediaplayer/mperror/permissiondenied)
- [static var requestTimedOut: MPError.Code](/documentation/mediaplayer/mperror/requesttimedout)

## Deprecated

- [Deprecated types](/documentation/mediaplayer/deprecated-types)

### Deprecated symbols

- [MPMovieAccessLog](/documentation/mediaplayer/mpmovieaccesslog)

#### Movie access log properties

- [var extendedLogData: Data!](/documentation/mediaplayer/mpmovieaccesslog/extendedlogdata)
- [var extendedLogDataStringEncoding: UInt](/documentation/mediaplayer/mpmovieaccesslog/extendedlogdatastringencoding)
- [var events: [Any]!](/documentation/mediaplayer/mpmovieaccesslog/events)
- [MPMovieAccessLogEvent](/documentation/mediaplayer/mpmovieaccesslogevent)

#### Movie access log event properties

- [var numberOfSegmentsDownloaded: Int](/documentation/mediaplayer/mpmovieaccesslogevent/numberofsegmentsdownloaded)
- [var playbackStartDate: Date!](/documentation/mediaplayer/mpmovieaccesslogevent/playbackstartdate)
- [var uri: String!](/documentation/mediaplayer/mpmovieaccesslogevent/uri)
- [var serverAddress: String!](/documentation/mediaplayer/mpmovieaccesslogevent/serveraddress)
- [var numberOfServerAddressChanges: Int](/documentation/mediaplayer/mpmovieaccesslogevent/numberofserveraddresschanges)
- [var playbackSessionID: String!](/documentation/mediaplayer/mpmovieaccesslogevent/playbacksessionid)
- [var playbackStartOffset: TimeInterval](/documentation/mediaplayer/mpmovieaccesslogevent/playbackstartoffset)
- [var segmentsDownloadedDuration: TimeInterval](/documentation/mediaplayer/mpmovieaccesslogevent/segmentsdownloadedduration)
- [var durationWatched: TimeInterval](/documentation/mediaplayer/mpmovieaccesslogevent/durationwatched)
- [var numberOfStalls: Int](/documentation/mediaplayer/mpmovieaccesslogevent/numberofstalls)
- [var numberOfBytesTransferred: Int64](/documentation/mediaplayer/mpmovieaccesslogevent/numberofbytestransferred)
- [var observedBitrate: Double](/documentation/mediaplayer/mpmovieaccesslogevent/observedbitrate)
- [var indicatedBitrate: Double](/documentation/mediaplayer/mpmovieaccesslogevent/indicatedbitrate)
- [var numberOfDroppedVideoFrames: Int](/documentation/mediaplayer/mpmovieaccesslogevent/numberofdroppedvideoframes)
- [MPMovieErrorLog](/documentation/mediaplayer/mpmovieerrorlog)

#### Movie error log properties

- [var extendedLogData: Data!](/documentation/mediaplayer/mpmovieerrorlog/extendedlogdata)
- [var extendedLogDataStringEncoding: UInt](/documentation/mediaplayer/mpmovieerrorlog/extendedlogdatastringencoding)
- [var events: [Any]!](/documentation/mediaplayer/mpmovieerrorlog/events)
- [MPMovieErrorLogEvent](/documentation/mediaplayer/mpmovieerrorlogevent)

#### Movie error log event properties

- [var date: Date!](/documentation/mediaplayer/mpmovieerrorlogevent/date)
- [var uri: String!](/documentation/mediaplayer/mpmovieerrorlogevent/uri)
- [var serverAddress: String!](/documentation/mediaplayer/mpmovieerrorlogevent/serveraddress)
- [var playbackSessionID: String!](/documentation/mediaplayer/mpmovieerrorlogevent/playbacksessionid)
- [var errorStatusCode: Int](/documentation/mediaplayer/mpmovieerrorlogevent/errorstatuscode)
- [var errorDomain: String!](/documentation/mediaplayer/mpmovieerrorlogevent/errordomain)
- [var errorComment: String!](/documentation/mediaplayer/mpmovieerrorlogevent/errorcomment)
- [MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate)

#### Constants

- [static var playable: MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate/playable)
- [static var playthroughOK: MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate/playthroughok)
- [static var stalled: MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate/stalled)

#### Initializers

- [init(rawValue: UInt)](/documentation/mediaplayer/mpmovieloadstate/init(rawvalue:))
- [MPMovieMediaTypeMask](/documentation/mediaplayer/mpmoviemediatypemask)

#### Constants

- [static var video: MPMovieMediaTypeMask](/documentation/mediaplayer/mpmoviemediatypemask/video)
- [static var audio: MPMovieMediaTypeMask](/documentation/mediaplayer/mpmoviemediatypemask/audio)

#### Initializers

- [init(rawValue: UInt)](/documentation/mediaplayer/mpmoviemediatypemask/init(rawvalue:))
- [MPMoviePlayerController](/documentation/mediaplayer/mpmovieplayercontroller)

#### Creating and initializing the object

- [init!(contentURL: URL!)](/documentation/mediaplayer/mpmovieplayercontroller/init(contenturl:))

#### Accessing movie properties

- [var contentURL: URL!](/documentation/mediaplayer/mpmovieplayercontroller/contenturl)
- [var movieSourceType: MPMovieSourceType](/documentation/mediaplayer/mpmovieplayercontroller/moviesourcetype)
- [var movieMediaTypes: MPMovieMediaTypeMask](/documentation/mediaplayer/mpmovieplayercontroller/moviemediatypes)
- [var allowsAirPlay: Bool](/documentation/mediaplayer/mpmovieplayercontroller/allowsairplay)
- [var isAirPlayVideoActive: Bool](/documentation/mediaplayer/mpmovieplayercontroller/isairplayvideoactive)
- [var naturalSize: CGSize](/documentation/mediaplayer/mpmovieplayercontroller/naturalsize)
- [var isFullscreen: Bool](/documentation/mediaplayer/mpmovieplayercontroller/isfullscreen)
- [func setFullscreen(Bool, animated: Bool)](/documentation/mediaplayer/mpmovieplayercontroller/setfullscreen(_:animated:))
- [var scalingMode: MPMovieScalingMode](/documentation/mediaplayer/mpmovieplayercontroller/scalingmode)
- [var controlStyle: MPMovieControlStyle](/documentation/mediaplayer/mpmovieplayercontroller/controlstyle)
- [var useApplicationAudioSession: Bool](/documentation/mediaplayer/mpmovieplayercontroller/useapplicationaudiosession)

#### Accessing the movie duration

- [var duration: TimeInterval](/documentation/mediaplayer/mpmovieplayercontroller/duration)
- [var playableDuration: TimeInterval](/documentation/mediaplayer/mpmovieplayercontroller/playableduration)

#### Accessing the view

- [var view: UIView!](/documentation/mediaplayer/mpmovieplayercontroller/view)
- [var backgroundView: UIView!](/documentation/mediaplayer/mpmovieplayercontroller/backgroundview)

#### Controlling and monitoring playback

- [var loadState: MPMovieLoadState](/documentation/mediaplayer/mpmovieplayercontroller/loadstate)
- [var playbackState: MPMoviePlaybackState](/documentation/mediaplayer/mpmovieplayercontroller/playbackstate)
- [var initialPlaybackTime: TimeInterval](/documentation/mediaplayer/mpmovieplayercontroller/initialplaybacktime)
- [var endPlaybackTime: TimeInterval](/documentation/mediaplayer/mpmovieplayercontroller/endplaybacktime)
- [var shouldAutoplay: Bool](/documentation/mediaplayer/mpmovieplayercontroller/shouldautoplay)
- [var readyForDisplay: Bool](/documentation/mediaplayer/mpmovieplayercontroller/readyfordisplay)
- [var repeatMode: MPMovieRepeatMode](/documentation/mediaplayer/mpmovieplayercontroller/repeatmode)
- [var timedMetadata: [Any]!](/documentation/mediaplayer/mpmovieplayercontroller/timedmetadata)

#### Generating thumbnail images

- [func thumbnailImage(atTime: TimeInterval, timeOption: MPMovieTimeOption) -> UIImage!](/documentation/mediaplayer/mpmovieplayercontroller/thumbnailimage(attime:timeoption:))
- [func requestThumbnailImages(atTimes: [Any]!, timeOption: MPMovieTimeOption)](/documentation/mediaplayer/mpmovieplayercontroller/requestthumbnailimages(attimes:timeoption:))
- [func cancelAllThumbnailImageRequests()](/documentation/mediaplayer/mpmovieplayercontroller/cancelallthumbnailimagerequests())

#### Retrieving movie logs

- [var accessLog: MPMovieAccessLog!](/documentation/mediaplayer/mpmovieplayercontroller/accesslog)
- [var errorLog: MPMovieErrorLog!](/documentation/mediaplayer/mpmovieplayercontroller/errorlog)

#### Constants

- [MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate)

##### Constants

- [static var playable: MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate/playable)
- [static var playthroughOK: MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate/playthroughok)
- [static var stalled: MPMovieLoadState](/documentation/mediaplayer/mpmovieloadstate/stalled)

##### Initializers

- [init(rawValue: UInt)](/documentation/mediaplayer/mpmovieloadstate/init(rawvalue:))
- [MPMovieControlStyle](/documentation/mediaplayer/mpmoviecontrolstyle)

##### Constants

- [case none](/documentation/mediaplayer/mpmoviecontrolstyle/none)
- [case embedded](/documentation/mediaplayer/mpmoviecontrolstyle/embedded)
- [case fullscreen](/documentation/mediaplayer/mpmoviecontrolstyle/fullscreen)
- [static var `default`: MPMovieControlStyle](/documentation/mediaplayer/mpmoviecontrolstyle/default)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmoviecontrolstyle/init(rawvalue:))
- [MPMovieFinishReason](/documentation/mediaplayer/mpmoviefinishreason)

##### Constants

- [case playbackEnded](/documentation/mediaplayer/mpmoviefinishreason/playbackended)
- [case playbackError](/documentation/mediaplayer/mpmoviefinishreason/playbackerror)
- [case userExited](/documentation/mediaplayer/mpmoviefinishreason/userexited)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmoviefinishreason/init(rawvalue:))
- [MPMoviePlaybackState](/documentation/mediaplayer/mpmovieplaybackstate)

##### Constants

- [case stopped](/documentation/mediaplayer/mpmovieplaybackstate/stopped)
- [case playing](/documentation/mediaplayer/mpmovieplaybackstate/playing)
- [case paused](/documentation/mediaplayer/mpmovieplaybackstate/paused)
- [case interrupted](/documentation/mediaplayer/mpmovieplaybackstate/interrupted)
- [case seekingForward](/documentation/mediaplayer/mpmovieplaybackstate/seekingforward)
- [case seekingBackward](/documentation/mediaplayer/mpmovieplaybackstate/seekingbackward)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmovieplaybackstate/init(rawvalue:))
- [MPMovieRepeatMode](/documentation/mediaplayer/mpmovierepeatmode)

##### Constants

- [case none](/documentation/mediaplayer/mpmovierepeatmode/none)
- [case one](/documentation/mediaplayer/mpmovierepeatmode/one)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmovierepeatmode/init(rawvalue:))
- [MPMovieScalingMode](/documentation/mediaplayer/mpmoviescalingmode)

##### Constants

- [case none](/documentation/mediaplayer/mpmoviescalingmode/none)
- [case aspectFit](/documentation/mediaplayer/mpmoviescalingmode/aspectfit)
- [case aspectFill](/documentation/mediaplayer/mpmoviescalingmode/aspectfill)
- [case fill](/documentation/mediaplayer/mpmoviescalingmode/fill)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmoviescalingmode/init(rawvalue:))
- [MPMovieTimeOption](/documentation/mediaplayer/mpmovietimeoption)

##### Constants

- [case nearestKeyFrame](/documentation/mediaplayer/mpmovietimeoption/nearestkeyframe)
- [case exact](/documentation/mediaplayer/mpmovietimeoption/exact)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmovietimeoption/init(rawvalue:))
- [MPMovieMediaTypeMask](/documentation/mediaplayer/mpmoviemediatypemask)

##### Constants

- [static var video: MPMovieMediaTypeMask](/documentation/mediaplayer/mpmoviemediatypemask/video)
- [static var audio: MPMovieMediaTypeMask](/documentation/mediaplayer/mpmoviemediatypemask/audio)

##### Initializers

- [init(rawValue: UInt)](/documentation/mediaplayer/mpmoviemediatypemask/init(rawvalue:))
- [MPMovieSourceType](/documentation/mediaplayer/mpmoviesourcetype)

##### Constants

- [case unknown](/documentation/mediaplayer/mpmoviesourcetype/unknown)
- [case file](/documentation/mediaplayer/mpmoviesourcetype/file)
- [case streaming](/documentation/mediaplayer/mpmoviesourcetype/streaming)

##### Initializers

- [init?(rawValue: Int)](/documentation/mediaplayer/mpmoviesourcetype/init(rawvalue:))
- [Thumbnail notification user info keys](/documentation/mediaplayer/thumbnail-notification-user-info-keys)

##### Constants

- [let MPMoviePlayerThumbnailImageKey: String](/documentation/mediaplayer/mpmovieplayerthumbnailimagekey)
- [let MPMoviePlayerThumbnailTimeKey: String](/documentation/mediaplayer/mpmovieplayerthumbnailtimekey)
- [let MPMoviePlayerThumbnailErrorKey: String](/documentation/mediaplayer/mpmovieplayerthumbnailerrorkey)
- [Fullscreen notification keys](/documentation/mediaplayer/fullscreen-notification-keys)

##### Constants

- [let MPMoviePlayerFullscreenAnimationDurationUserInfoKey: String](/documentation/mediaplayer/mpmovieplayerfullscreenanimationdurationuserinfokey)
- [let MPMoviePlayerFullscreenAnimationCurveUserInfoKey: String](/documentation/mediaplayer/mpmovieplayerfullscreenanimationcurveuserinfokey)
- [Playback finished notification key](/documentation/mediaplayer/playback-finished-notification-key)

##### Constants

- [let MPMoviePlayerPlaybackDidFinishReasonUserInfoKey: String](/documentation/mediaplayer/mpmovieplayerplaybackdidfinishreasonuserinfokey)
- [MPMoviePlayerViewController](/documentation/mediaplayer/mpmovieplayerviewcontroller)

#### New methods

- [init!(contentURL: URL!)](/documentation/mediaplayer/mpmovieplayerviewcontroller/init(contenturl:))
- [var moviePlayer: MPMoviePlayerController!](/documentation/mediaplayer/mpmovieplayerviewcontroller/movieplayer)
- [MPTimedMetadata](/documentation/mediaplayer/mptimedmetadata)

#### Extracting timed metadata from a stream

- [var allMetadata: [AnyHashable : Any]!](/documentation/mediaplayer/mptimedmetadata/allmetadata)
- [var key: String!](/documentation/mediaplayer/mptimedmetadata/key)
- [var keyspace: String!](/documentation/mediaplayer/mptimedmetadata/keyspace)
- [var timestamp: TimeInterval](/documentation/mediaplayer/mptimedmetadata/timestamp)
- [var value: Any!](/documentation/mediaplayer/mptimedmetadata/value)

#### Constants

- [Timed metadata dictionary keys](/documentation/mediaplayer/timed-metadata-dictionary-keys)

##### Constants

- [let MPMoviePlayerTimedMetadataKeyName: String](/documentation/mediaplayer/mpmovieplayertimedmetadatakeyname)
- [let MPMoviePlayerTimedMetadataKeyInfo: String](/documentation/mediaplayer/mpmovieplayertimedmetadatakeyinfo)
- [let MPMoviePlayerTimedMetadataKeyMIMEType: String](/documentation/mediaplayer/mpmovieplayertimedmetadatakeymimetype)
- [let MPMoviePlayerTimedMetadataKeyDataType: String](/documentation/mediaplayer/mpmovieplayertimedmetadatakeydatatype)
- [let MPMoviePlayerTimedMetadataKeyLanguageCode: String](/documentation/mediaplayer/mpmovieplayertimedmetadatakeylanguagecode)

#### Notifications

- [let MPMoviePlayerTimedMetadataUserInfoKey: String](/documentation/mediaplayer/mpmovieplayertimedmetadatauserinfokey)
- [MPPlayableContentManager](/documentation/mediaplayer/mpplayablecontentmanager)

#### Providing playable content

- [var dataSource: (any MPPlayableContentDataSource)?](/documentation/mediaplayer/mpplayablecontentmanager/datasource)
- [MPPlayableContentDataSource](/documentation/mediaplayer/mpplayablecontentdatasource)

##### Retrieving a media item

- [func contentItem(at: IndexPath) -> MPContentItem?](/documentation/mediaplayer/mpplayablecontentdatasource/contentitem(at:))
- [func contentItem(forIdentifier: String, completionHandler: (MPContentItem?, (any Error)?) -> Void)](/documentation/mediaplayer/mpplayablecontentdatasource/contentitem(foridentifier:completionhandler:))

##### Working with child nodes

- [func beginLoadingChildItems(at: IndexPath, completionHandler: ((any Error)?) -> Void)](/documentation/mediaplayer/mpplayablecontentdatasource/beginloadingchilditems(at:completionhandler:))
- [func childItemsDisplayPlaybackProgress(at: IndexPath) -> Bool](/documentation/mediaplayer/mpplayablecontentdatasource/childitemsdisplayplaybackprogress(at:))
- [func numberOfChildItems(at: IndexPath) -> Int](/documentation/mediaplayer/mpplayablecontentdatasource/numberofchilditems(at:))

#### Responding to playback events

- [var delegate: (any MPPlayableContentDelegate)?](/documentation/mediaplayer/mpplayablecontentmanager/delegate)
- [MPPlayableContentDelegate](/documentation/mediaplayer/mpplayablecontentdelegate)

##### Playing a specific media item

- [func playableContentManager(MPPlayableContentManager, initiatePlaybackOfContentItemAt: IndexPath, completionHandler: ((any Error)?) -> Void)](/documentation/mediaplayer/mpplayablecontentdelegate/playablecontentmanager(_:initiateplaybackofcontentitemat:completionhandler:))

##### Suggesting content for playback

- [func playableContentManager(MPPlayableContentManager, initializePlaybackQueueWithContentItems: [Any]?, completionHandler: ((any Error)?) -> Void)](/documentation/mediaplayer/mpplayablecontentdelegate/playablecontentmanager(_:initializeplaybackqueuewithcontentitems:completionhandler:))
- [func playableContentManager(MPPlayableContentManager, initializePlaybackQueueWithCompletionHandler: ((any Error)?) -> Void)](/documentation/mediaplayer/mpplayablecontentdelegate/playablecontentmanager(_:initializeplaybackqueuewithcompletionhandler:))

##### Responding to context changes

- [func playableContentManager(MPPlayableContentManager, didUpdate: MPPlayableContentManagerContext)](/documentation/mediaplayer/mpplayablecontentdelegate/playablecontentmanager(_:didupdate:))

#### Setting the content manager

- [class func shared() -> Self](/documentation/mediaplayer/mpplayablecontentmanager/shared())

#### Updating data

- [func beginUpdates()](/documentation/mediaplayer/mpplayablecontentmanager/beginupdates())
- [func endUpdates()](/documentation/mediaplayer/mpplayablecontentmanager/endupdates())
- [func reloadData()](/documentation/mediaplayer/mpplayablecontentmanager/reloaddata())

#### Retrieving information on currently playing items

- [var context: MPPlayableContentManagerContext](/documentation/mediaplayer/mpplayablecontentmanager/context)
- [var nowPlayingIdentifiers: [String]](/documentation/mediaplayer/mpplayablecontentmanager/nowplayingidentifiers)
- [MPPlayableContentManagerContext](/documentation/mediaplayer/mpplayablecontentmanagercontext)

#### Inspecting content manager properties

- [var contentLimitsEnforced: Bool](/documentation/mediaplayer/mpplayablecontentmanagercontext/contentlimitsenforced)
- [var endpointAvailable: Bool](/documentation/mediaplayer/mpplayablecontentmanagercontext/endpointavailable)
- [var enforcedContentItemsCount: Int](/documentation/mediaplayer/mpplayablecontentmanagercontext/enforcedcontentitemscount)
- [var enforcedContentTreeDepth: Int](/documentation/mediaplayer/mpplayablecontentmanagercontext/enforcedcontenttreedepth)
- [var contentLimitsEnabled: Bool](/documentation/mediaplayer/mpplayablecontentmanagercontext/contentlimitsenabled)
- [class var iPodMusicPlayer: MPMusicPlayerController](/documentation/mediaplayer/mpmusicplayercontroller/ipodmusicplayer)
- [convenience init(image: UIImage)](/documentation/mediaplayer/mpmediaitemartwork/init(image:))
- [var imageCropRect: CGRect](/documentation/mediaplayer/mpmediaitemartwork/imagecroprect)
- [var showsRouteButton: Bool](/documentation/mediaplayer/mpvolumeview/showsroutebutton)
- [func routeButtonImage(for: UIControl.State) -> UIImage?](/documentation/mediaplayer/mpvolumeview/routebuttonimage(for:))
- [func routeButtonRect(forBounds: CGRect) -> CGRect](/documentation/mediaplayer/mpvolumeview/routebuttonrect(forbounds:))
- [func setRouteButtonImage(UIImage?, for: UIControl.State)](/documentation/mediaplayer/mpvolumeview/setroutebuttonimage(_:for:))
- [var areWirelessRoutesAvailable: Bool](/documentation/mediaplayer/mpvolumeview/arewirelessroutesavailable)
- [var isWirelessRouteActive: Bool](/documentation/mediaplayer/mpvolumeview/iswirelessrouteactive)
- [Global volume setting methods](/documentation/mediaplayer/global-volume-setting-methods)

#### Global volume setting methods

- [func MPVolumeSettingsAlertShow()](/documentation/mediaplayer/mpvolumesettingsalertshow())
- [func MPVolumeSettingsAlertHide()](/documentation/mediaplayer/mpvolumesettingsalerthide())
- [func MPVolumeSettingsAlertIsVisible() -> Bool](/documentation/mediaplayer/mpvolumesettingsalertisvisible())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
