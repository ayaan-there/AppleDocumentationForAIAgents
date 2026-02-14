# iTunes Library Documentation

Source: https://sosumi.ai/documentation/ituneslibrary

---
title: iTunes Library
source: https://developer.apple.com/documentation/ituneslibrary
timestamp: 2026-02-13T18:58:28.937Z
---

## Essentials

- [ITLibrary](/documentation/ituneslibrary/itlibrary)

### Essentials

- [convenience init(apiVersion: String) throws](/documentation/ituneslibrary/itlibrary/init(apiversion:))
- [init(apiVersion: String, options: ITLibInitOptions) throws](/documentation/ituneslibrary/itlibrary/init(apiversion:options:))
- [ITLibInitOptions](/documentation/ituneslibrary/itlibinitoptions)

#### Init Options

- [case none](/documentation/ituneslibrary/itlibinitoptions/none)
- [case lazyLoadData](/documentation/ituneslibrary/itlibinitoptions/lazyloaddata)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibinitoptions/init(rawvalue:))

### Getting iTunes Library Info

- [var allMediaItems: [ITLibMediaItem]](/documentation/ituneslibrary/itlibrary/allmediaitems)
- [var allPlaylists: [ITLibPlaylist]](/documentation/ituneslibrary/itlibrary/allplaylists)
- [var apiMajorVersion: Int](/documentation/ituneslibrary/itlibrary/apimajorversion)
- [var apiMinorVersion: Int](/documentation/ituneslibrary/itlibrary/apiminorversion)
- [var applicationVersion: String](/documentation/ituneslibrary/itlibrary/applicationversion)
- [var mediaFolderLocation: URL?](/documentation/ituneslibrary/itlibrary/mediafolderlocation)
- [var shouldShowContentRating: Bool](/documentation/ituneslibrary/itlibrary/shouldshowcontentrating)

### Loading and Unloading Data

- [func reloadData() -> Bool](/documentation/ituneslibrary/itlibrary/reloaddata())
- [func unloadData()](/documentation/ituneslibrary/itlibrary/unloaddata())

### Accessing Artwork

- [func artwork(forMediaFile: URL) -> ITLibArtwork?](/documentation/ituneslibrary/itlibrary/artwork(formediafile:))

### Deprecated

- [var features: ITLibExportFeature](/documentation/ituneslibrary/itlibrary/features)
- [ITLibExportFeature](/documentation/ituneslibrary/itlibexportfeature)

#### Export Features

- [case none](/documentation/ituneslibrary/itlibexportfeature/none)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibexportfeature/init(rawvalue:))
- [var musicFolderLocation: URL?](/documentation/ituneslibrary/itlibrary/musicfolderlocation)

## Albums and Playlists

- [ITLibAlbum](/documentation/ituneslibrary/itlibalbum)

### Getting Album Info

- [var trackCount: Int](/documentation/ituneslibrary/itlibalbum/trackcount)
- [var title: String?](/documentation/ituneslibrary/itlibalbum/title)
- [var sortTitle: String?](/documentation/ituneslibrary/itlibalbum/sorttitle)
- [var rating: Int](/documentation/ituneslibrary/itlibalbum/rating)
- [var isRatingComputed: Bool](/documentation/ituneslibrary/itlibalbum/isratingcomputed)
- [var isGapless: Bool](/documentation/ituneslibrary/itlibalbum/isgapless)
- [var discNumber: Int](/documentation/ituneslibrary/itlibalbum/discnumber)
- [var discCount: Int](/documentation/ituneslibrary/itlibalbum/disccount)
- [var isCompilation: Bool](/documentation/ituneslibrary/itlibalbum/iscompilation)
- [var albumArtist: String?](/documentation/ituneslibrary/itlibalbum/albumartist)
- [var sortAlbumArtist: String?](/documentation/ituneslibrary/itlibalbum/sortalbumartist)
- [var persistentID: NSNumber](/documentation/ituneslibrary/itlibalbum/persistentid)

### Deprecated

- [var artist: ITLibArtist?](/documentation/ituneslibrary/itlibalbum/artist)
- [ITLibPlaylist](/documentation/ituneslibrary/itlibplaylist)

### Getting Playlist Info

- [var name: String](/documentation/ituneslibrary/itlibplaylist/name)
- [var items: [ITLibMediaItem]](/documentation/ituneslibrary/itlibplaylist/items)
- [var parentID: NSNumber?](/documentation/ituneslibrary/itlibplaylist/parentid)
- [var isPrimary: Bool](/documentation/ituneslibrary/itlibplaylist/isprimary)
- [var isVisible: Bool](/documentation/ituneslibrary/itlibplaylist/isvisible)
- [var distinguishedKind: ITLibDistinguishedPlaylistKind](/documentation/ituneslibrary/itlibplaylist/distinguishedkind)
- [var kind: ITLibPlaylistKind](/documentation/ituneslibrary/itlibplaylist/kind)
- [ITLibPlaylistKind](/documentation/ituneslibrary/itlibplaylistkind)

#### Playlist Kinds

- [case regular](/documentation/ituneslibrary/itlibplaylistkind/regular)
- [case smart](/documentation/ituneslibrary/itlibplaylistkind/smart)
- [case genius](/documentation/ituneslibrary/itlibplaylistkind/genius)
- [case folder](/documentation/ituneslibrary/itlibplaylistkind/folder)
- [case geniusMix](/documentation/ituneslibrary/itlibplaylistkind/geniusmix)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibplaylistkind/init(rawvalue:))
- [ITLibDistinguishedPlaylistKind](/documentation/ituneslibrary/itlibdistinguishedplaylistkind)

#### Distinguished Playlist Kinds

- [case kindNone](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindnone)
- [case kindMovies](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindmovies)
- [case kindTVShows](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindtvshows)
- [case kindMusic](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindmusic)
- [case kindAudiobooks](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindaudiobooks)
- [static var kindBooks: ITLibDistinguishedPlaylistKind](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindbooks)
- [case kindRingtones](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindringtones)
- [case kindPodcasts](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindpodcasts)
- [case kindVoiceMemos](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindvoicememos)
- [case kindPurchases](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindpurchases)
- [case kindiTunesU](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kinditunesu)
- [case kind90sMusic](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kind90smusic)
- [case kindMyTopRated](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindmytoprated)
- [case kindTop25MostPlayed](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindtop25mostplayed)
- [case kindRecentlyPlayed](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindrecentlyplayed)
- [case kindRecentlyAdded](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindrecentlyadded)
- [case kindMusicVideos](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindmusicvideos)
- [case kindClassicalMusic](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindclassicalmusic)
- [case kindLibraryMusicVideos](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindlibrarymusicvideos)
- [case kindHomeVideos](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindhomevideos)
- [case kindApplications](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindapplications)
- [case kindLovedSongs](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindlovedsongs)
- [case kindMusicShowsAndMovies](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/kindmusicshowsandmovies)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibdistinguishedplaylistkind/init(rawvalue:))

### Playlist Properties

- [let ITLibPlaylistPropertyAllItemsPlaylist: String](/documentation/ituneslibrary/itlibplaylistpropertyallitemsplaylist)

#### Related Documentation

- [var isAllItemsPlaylist: Bool](/documentation/ituneslibrary/itlibplaylist/isallitemsplaylist)
- [let ITLibPlaylistPropertyDistinguisedKind: String](/documentation/ituneslibrary/itlibplaylistpropertydistinguisedkind)

#### Related Documentation

- [var distinguishedKind: ITLibDistinguishedPlaylistKind](/documentation/ituneslibrary/itlibplaylist/distinguishedkind)
- [let ITLibPlaylistPropertyItems: String](/documentation/ituneslibrary/itlibplaylistpropertyitems)

#### Related Documentation

- [var items: [ITLibMediaItem]](/documentation/ituneslibrary/itlibplaylist/items)
- [let ITLibPlaylistPropertyKind: String](/documentation/ituneslibrary/itlibplaylistpropertykind)

#### Related Documentation

- [ITLibPlaylistKind](/documentation/ituneslibrary/itlibplaylistkind)

##### Playlist Kinds

- [case regular](/documentation/ituneslibrary/itlibplaylistkind/regular)
- [case smart](/documentation/ituneslibrary/itlibplaylistkind/smart)
- [case genius](/documentation/ituneslibrary/itlibplaylistkind/genius)
- [case folder](/documentation/ituneslibrary/itlibplaylistkind/folder)
- [case geniusMix](/documentation/ituneslibrary/itlibplaylistkind/geniusmix)

##### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibplaylistkind/init(rawvalue:))
- [let ITLibPlaylistPropertyPrimary: String](/documentation/ituneslibrary/itlibplaylistpropertyprimary)

#### Related Documentation

- [var isPrimary: Bool](/documentation/ituneslibrary/itlibplaylist/isprimary)
- [let ITLibPlaylistPropertyName: String](/documentation/ituneslibrary/itlibplaylistpropertyname)

#### Related Documentation

- [var name: String](/documentation/ituneslibrary/itlibplaylist/name)
- [let ITLibPlaylistPropertyParentPersistentID: String](/documentation/ituneslibrary/itlibplaylistpropertyparentpersistentid)

#### Related Documentation

- [var parentID: NSNumber?](/documentation/ituneslibrary/itlibplaylist/parentid)
- [let ITLibPlaylistPropertyVisible: String](/documentation/ituneslibrary/itlibplaylistpropertyvisible)

#### Related Documentation

- [var isVisible: Bool](/documentation/ituneslibrary/itlibplaylist/isvisible)

### Deprecated

- [var isAllItemsPlaylist: Bool](/documentation/ituneslibrary/itlibplaylist/isallitemsplaylist)
- [var isMaster: Bool](/documentation/ituneslibrary/itlibplaylist/ismaster)
- [let ITLibPlaylistPropertyMaster: String](/documentation/ituneslibrary/itlibplaylistpropertymaster)

## Media Items

- [ITLibMediaItem](/documentation/ituneslibrary/itlibmediaitem)

### Getting Media Item Info

- [var title: String](/documentation/ituneslibrary/itlibmediaitem/title)
- [var sortTitle: String?](/documentation/ituneslibrary/itlibmediaitem/sorttitle)
- [var artist: ITLibArtist?](/documentation/ituneslibrary/itlibmediaitem/artist)
- [var composer: String](/documentation/ituneslibrary/itlibmediaitem/composer)
- [var sortComposer: String?](/documentation/ituneslibrary/itlibmediaitem/sortcomposer)
- [var rating: Int](/documentation/ituneslibrary/itlibmediaitem/rating)
- [var isRatingComputed: Bool](/documentation/ituneslibrary/itlibmediaitem/isratingcomputed)
- [var startTime: Int](/documentation/ituneslibrary/itlibmediaitem/starttime)
- [var stopTime: Int](/documentation/ituneslibrary/itlibmediaitem/stoptime)
- [var album: ITLibAlbum](/documentation/ituneslibrary/itlibmediaitem/album)
- [var genre: String](/documentation/ituneslibrary/itlibmediaitem/genre)
- [var kind: String?](/documentation/ituneslibrary/itlibmediaitem/kind)
- [var mediaKind: ITLibMediaItemMediaKind](/documentation/ituneslibrary/itlibmediaitem/mediakind)
- [var totalTime: Int](/documentation/ituneslibrary/itlibmediaitem/totaltime)
- [var trackNumber: Int](/documentation/ituneslibrary/itlibmediaitem/tracknumber)
- [var category: String?](/documentation/ituneslibrary/itlibmediaitem/category)
- [var description: String?](/documentation/ituneslibrary/itlibmediaitem/description)
- [var contentRating: String?](/documentation/ituneslibrary/itlibmediaitem/contentrating)
- [var lyricsContentRating: ITLibMediaItemLyricsContentRating](/documentation/ituneslibrary/itlibmediaitem/lyricscontentrating)
- [var addedDate: Date?](/documentation/ituneslibrary/itlibmediaitem/addeddate)
- [var modifiedDate: Date?](/documentation/ituneslibrary/itlibmediaitem/modifieddate)
- [var bitrate: Int](/documentation/ituneslibrary/itlibmediaitem/bitrate)
- [var sampleRate: Int](/documentation/ituneslibrary/itlibmediaitem/samplerate)
- [var beatsPerMinute: Int](/documentation/ituneslibrary/itlibmediaitem/beatsperminute)
- [var playCount: Int](/documentation/ituneslibrary/itlibmediaitem/playcount)
- [var lastPlayedDate: Date?](/documentation/ituneslibrary/itlibmediaitem/lastplayeddate)
- [var location: URL?](/documentation/ituneslibrary/itlibmediaitem/location)
- [var locationType: ITLibMediaItemLocationType](/documentation/ituneslibrary/itlibmediaitem/locationtype)
- [var hasArtworkAvailable: Bool](/documentation/ituneslibrary/itlibmediaitem/hasartworkavailable)
- [var artwork: ITLibArtwork?](/documentation/ituneslibrary/itlibmediaitem/artwork)
- [var comments: String?](/documentation/ituneslibrary/itlibmediaitem/comments)
- [var isPurchased: Bool](/documentation/ituneslibrary/itlibmediaitem/ispurchased)
- [var isDRMProtected: Bool](/documentation/ituneslibrary/itlibmediaitem/isdrmprotected)
- [var isVideo: Bool](/documentation/ituneslibrary/itlibmediaitem/isvideo)
- [var videoInfo: ITLibMediaItemVideoInfo?](/documentation/ituneslibrary/itlibmediaitem/videoinfo)
- [var releaseDate: Date?](/documentation/ituneslibrary/itlibmediaitem/releasedate)
- [var year: Int](/documentation/ituneslibrary/itlibmediaitem/year)
- [var skipCount: Int](/documentation/ituneslibrary/itlibmediaitem/skipcount)
- [var skipDate: Date?](/documentation/ituneslibrary/itlibmediaitem/skipdate)
- [var voiceOverLanguage: String?](/documentation/ituneslibrary/itlibmediaitem/voiceoverlanguage)
- [var volumeAdjustment: Int](/documentation/ituneslibrary/itlibmediaitem/volumeadjustment)
- [var volumeNormalizationEnergy: Int](/documentation/ituneslibrary/itlibmediaitem/volumenormalizationenergy)
- [var isUserDisabled: Bool](/documentation/ituneslibrary/itlibmediaitem/isuserdisabled)
- [var grouping: String?](/documentation/ituneslibrary/itlibmediaitem/grouping)
- [var fileSize: UInt64](/documentation/ituneslibrary/itlibmediaitem/filesize)
- [var isCloud: Bool](/documentation/ituneslibrary/itlibmediaitem/iscloud)
- [var playStatus: ITLibMediaItemPlayStatus](/documentation/ituneslibrary/itlibmediaitem/playstatus)
- [ITLibMediaItemMediaKind](/documentation/ituneslibrary/itlibmediaitemmediakind)

#### Media Kinds

- [case kindUnknown](/documentation/ituneslibrary/itlibmediaitemmediakind/kindunknown)
- [case kindSong](/documentation/ituneslibrary/itlibmediaitemmediakind/kindsong)
- [case kindMovie](/documentation/ituneslibrary/itlibmediaitemmediakind/kindmovie)
- [case kindPodcast](/documentation/ituneslibrary/itlibmediaitemmediakind/kindpodcast)
- [case kindAudiobook](/documentation/ituneslibrary/itlibmediaitemmediakind/kindaudiobook)
- [case kindPDFBooklet](/documentation/ituneslibrary/itlibmediaitemmediakind/kindpdfbooklet)
- [case kindMusicVideo](/documentation/ituneslibrary/itlibmediaitemmediakind/kindmusicvideo)
- [case kindTVShow](/documentation/ituneslibrary/itlibmediaitemmediakind/kindtvshow)
- [case kindInteractiveBooklet](/documentation/ituneslibrary/itlibmediaitemmediakind/kindinteractivebooklet)
- [case kindHomeVideo](/documentation/ituneslibrary/itlibmediaitemmediakind/kindhomevideo)
- [case kindRingtone](/documentation/ituneslibrary/itlibmediaitemmediakind/kindringtone)
- [case kindDigitalBooklet](/documentation/ituneslibrary/itlibmediaitemmediakind/kinddigitalbooklet)
- [case kindIOSApplication](/documentation/ituneslibrary/itlibmediaitemmediakind/kindiosapplication)
- [case kindVoiceMemo](/documentation/ituneslibrary/itlibmediaitemmediakind/kindvoicememo)
- [case kindiTunesU](/documentation/ituneslibrary/itlibmediaitemmediakind/kinditunesu)
- [case kindBook](/documentation/ituneslibrary/itlibmediaitemmediakind/kindbook)
- [case kindPDFBook](/documentation/ituneslibrary/itlibmediaitemmediakind/kindpdfbook)
- [case kindAlertTone](/documentation/ituneslibrary/itlibmediaitemmediakind/kindalerttone)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibmediaitemmediakind/init(rawvalue:))
- [ITLibMediaItemLocationType](/documentation/ituneslibrary/itlibmediaitemlocationtype)

#### Media Item Location Types

- [case unknown](/documentation/ituneslibrary/itlibmediaitemlocationtype/unknown)
- [case file](/documentation/ituneslibrary/itlibmediaitemlocationtype/file)
- [case URL](/documentation/ituneslibrary/itlibmediaitemlocationtype/url)
- [case remote](/documentation/ituneslibrary/itlibmediaitemlocationtype/remote)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibmediaitemlocationtype/init(rawvalue:))
- [ITLibMediaItemLyricsContentRating](/documentation/ituneslibrary/itlibmediaitemlyricscontentrating)

#### Media Item Lyric Content Ratings

- [case none](/documentation/ituneslibrary/itlibmediaitemlyricscontentrating/none)
- [case explicit](/documentation/ituneslibrary/itlibmediaitemlyricscontentrating/explicit)
- [case clean](/documentation/ituneslibrary/itlibmediaitemlyricscontentrating/clean)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibmediaitemlyricscontentrating/init(rawvalue:))
- [ITLibMediaItemPlayStatus](/documentation/ituneslibrary/itlibmediaitemplaystatus)

#### Media Item Play Statuses

- [case none](/documentation/ituneslibrary/itlibmediaitemplaystatus/none)

##### Related Documentation

- [var playCount: Int](/documentation/ituneslibrary/itlibmediaitem/playcount)
- [case partiallyPlayed](/documentation/ituneslibrary/itlibmediaitemplaystatus/partiallyplayed)
- [case unplayed](/documentation/ituneslibrary/itlibmediaitemplaystatus/unplayed)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibmediaitemplaystatus/init(rawvalue:))

### Media Item Properties

- [let ITLibMediaEntityPropertyPersistentID: String](/documentation/ituneslibrary/itlibmediaentitypropertypersistentid)
- [let ITLibMediaItemPropertyAddedDate: String](/documentation/ituneslibrary/itlibmediaitempropertyaddeddate)
- [let ITLibMediaItemPropertyAlbumArtist: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumartist)
- [let ITLibMediaItemPropertyAlbumDiscCount: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumdisccount)
- [let ITLibMediaItemPropertyAlbumDiscNumber: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumdiscnumber)
- [let ITLibMediaItemPropertyAlbumIsCompilation: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumiscompilation)
- [let ITLibMediaItemPropertyAlbumIsGapless: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumisgapless)
- [let ITLibMediaItemPropertyAlbumRating: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumrating)
- [let ITLibMediaItemPropertyAlbumRatingComputed: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumratingcomputed)
- [let ITLibMediaItemPropertyAlbumTitle: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumtitle)
- [let ITLibMediaItemPropertyAlbumTrackCount: String](/documentation/ituneslibrary/itlibmediaitempropertyalbumtrackcount)
- [let ITLibMediaItemPropertyArtistName: String](/documentation/ituneslibrary/itlibmediaitempropertyartistname)
- [let ITLibMediaItemPropertyArtwork: String](/documentation/ituneslibrary/itlibmediaitempropertyartwork)
- [let ITLibMediaItemPropertyBeatsPerMinute: String](/documentation/ituneslibrary/itlibmediaitempropertybeatsperminute)
- [let ITLibMediaItemPropertyBitRate: String](/documentation/ituneslibrary/itlibmediaitempropertybitrate)
- [let ITLibMediaItemPropertyCategory: String](/documentation/ituneslibrary/itlibmediaitempropertycategory)
- [let ITLibMediaItemPropertyComments: String](/documentation/ituneslibrary/itlibmediaitempropertycomments)
- [let ITLibMediaItemPropertyComposer: String](/documentation/ituneslibrary/itlibmediaitempropertycomposer)
- [let ITLibMediaItemPropertyContentRating: String](/documentation/ituneslibrary/itlibmediaitempropertycontentrating)
- [let ITLibMediaItemPropertyDescription: String](/documentation/ituneslibrary/itlibmediaitempropertydescription)
- [let ITLibMediaItemPropertyFileSize: String](/documentation/ituneslibrary/itlibmediaitempropertyfilesize)
- [let ITLibMediaItemPropertyGenre: String](/documentation/ituneslibrary/itlibmediaitempropertygenre)
- [let ITLibMediaItemPropertyGrouping: String](/documentation/ituneslibrary/itlibmediaitempropertygrouping)
- [let ITLibMediaItemPropertyHasArtwork: String](/documentation/ituneslibrary/itlibmediaitempropertyhasartwork)
- [let ITLibMediaItemPropertyIsDRMProtected: String](/documentation/ituneslibrary/itlibmediaitempropertyisdrmprotected)
- [let ITLibMediaItemPropertyIsPurchased: String](/documentation/ituneslibrary/itlibmediaitempropertyispurchased)
- [let ITLibMediaItemPropertyIsUserDisabled: String](/documentation/ituneslibrary/itlibmediaitempropertyisuserdisabled)
- [let ITLibMediaItemPropertyIsVideo: String](/documentation/ituneslibrary/itlibmediaitempropertyisvideo)
- [let ITLibMediaItemPropertyKind: String](/documentation/ituneslibrary/itlibmediaitempropertykind)
- [let ITLibMediaItemPropertyLastPlayDate: String](/documentation/ituneslibrary/itlibmediaitempropertylastplaydate)
- [let ITLibMediaItemPropertyLocation: String](/documentation/ituneslibrary/itlibmediaitempropertylocation)
- [let ITLibMediaItemPropertyLocationType: String](/documentation/ituneslibrary/itlibmediaitempropertylocationtype)
- [let ITLibMediaItemPropertyLyricsContentRating: String](/documentation/ituneslibrary/itlibmediaitempropertylyricscontentrating)
- [let ITLibMediaItemPropertyMediaKind: String](/documentation/ituneslibrary/itlibmediaitempropertymediakind)
- [let ITLibMediaItemPropertyModifiedDate: String](/documentation/ituneslibrary/itlibmediaitempropertymodifieddate)
- [let ITLibMediaItemPropertyMovementCount: String](/documentation/ituneslibrary/itlibmediaitempropertymovementcount)
- [let ITLibMediaItemPropertyMovementName: String](/documentation/ituneslibrary/itlibmediaitempropertymovementname)
- [let ITLibMediaItemPropertyMovementNumber: String](/documentation/ituneslibrary/itlibmediaitempropertymovementnumber)
- [let ITLibMediaItemPropertyPlayCount: String](/documentation/ituneslibrary/itlibmediaitempropertyplaycount)
- [let ITLibMediaItemPropertyPlayStatus: String](/documentation/ituneslibrary/itlibmediaitempropertyplaystatus)
- [let ITLibMediaItemPropertyRating: String](/documentation/ituneslibrary/itlibmediaitempropertyrating)
- [let ITLibMediaItemPropertyRatingComputed: String](/documentation/ituneslibrary/itlibmediaitempropertyratingcomputed)
- [let ITLibMediaItemPropertyReleaseDate: String](/documentation/ituneslibrary/itlibmediaitempropertyreleasedate)
- [let ITLibMediaItemPropertySampleRate: String](/documentation/ituneslibrary/itlibmediaitempropertysamplerate)
- [let ITLibMediaItemPropertySize: String](/documentation/ituneslibrary/itlibmediaitempropertysize)
- [let ITLibMediaItemPropertySkipDate: String](/documentation/ituneslibrary/itlibmediaitempropertyskipdate)
- [let ITLibMediaItemPropertySortAlbumArtist: String](/documentation/ituneslibrary/itlibmediaitempropertysortalbumartist)
- [let ITLibMediaItemPropertySortAlbumTitle: String](/documentation/ituneslibrary/itlibmediaitempropertysortalbumtitle)
- [let ITLibMediaItemPropertySortArtistName: String](/documentation/ituneslibrary/itlibmediaitempropertysortartistname)
- [let ITLibMediaItemPropertySortComposer: String](/documentation/ituneslibrary/itlibmediaitempropertysortcomposer)
- [let ITLibMediaItemPropertySortTitle: String](/documentation/ituneslibrary/itlibmediaitempropertysorttitle)
- [let ITLibMediaItemPropertyStartTime: String](/documentation/ituneslibrary/itlibmediaitempropertystarttime)
- [let ITLibMediaItemPropertyStopTime: String](/documentation/ituneslibrary/itlibmediaitempropertystoptime)
- [let ITLibMediaItemPropertyTitle: String](/documentation/ituneslibrary/itlibmediaitempropertytitle)
- [let ITLibMediaItemPropertyTotalTime: String](/documentation/ituneslibrary/itlibmediaitempropertytotaltime)
- [let ITLibMediaItemPropertyTrackNumber: String](/documentation/ituneslibrary/itlibmediaitempropertytracknumber)
- [let ITLibMediaItemPropertyUserSkipCount: String](/documentation/ituneslibrary/itlibmediaitempropertyuserskipcount)
- [let ITLibMediaItemPropertyVideoEpisode: String](/documentation/ituneslibrary/itlibmediaitempropertyvideoepisode)
- [let ITLibMediaItemPropertyVideoEpisodeOrder: String](/documentation/ituneslibrary/itlibmediaitempropertyvideoepisodeorder)
- [let ITLibMediaItemPropertyVideoHeight: String](/documentation/ituneslibrary/itlibmediaitempropertyvideoheight)
- [let ITLibMediaItemPropertyVideoIsHD: String](/documentation/ituneslibrary/itlibmediaitempropertyvideoishd)
- [let ITLibMediaItemPropertyVideoSeason: String](/documentation/ituneslibrary/itlibmediaitempropertyvideoseason)
- [let ITLibMediaItemPropertyVideoSeries: String](/documentation/ituneslibrary/itlibmediaitempropertyvideoseries)
- [let ITLibMediaItemPropertyVideoSortSeries: String](/documentation/ituneslibrary/itlibmediaitempropertyvideosortseries)
- [let ITLibMediaItemPropertyVideoWidth: String](/documentation/ituneslibrary/itlibmediaitempropertyvideowidth)
- [let ITLibMediaItemPropertyVoiceOverLanguage: String](/documentation/ituneslibrary/itlibmediaitempropertyvoiceoverlanguage)
- [let ITLibMediaItemPropertyVolumeAdjustment: String](/documentation/ituneslibrary/itlibmediaitempropertyvolumeadjustment)
- [let ITLibMediaItemPropertyVolumeNormalizationEnergy: String](/documentation/ituneslibrary/itlibmediaitempropertyvolumenormalizationenergy)
- [let ITLibMediaItemPropertyWork: String](/documentation/ituneslibrary/itlibmediaitempropertywork)
- [let ITLibMediaItemPropertyYear: String](/documentation/ituneslibrary/itlibmediaitempropertyyear)

### Deprecated

- [var fileType: Int](/documentation/ituneslibrary/itlibmediaitem/filetype)
- [var size: Int](/documentation/ituneslibrary/itlibmediaitem/size)
- [let ITLibMediaItemPropertyFileType: String](/documentation/ituneslibrary/itlibmediaitempropertyfiletype)
- [ITLibMediaEntity](/documentation/ituneslibrary/itlibmediaentity)

### Essentials

- [var persistentID: NSNumber](/documentation/ituneslibrary/itlibmediaentity/persistentid)

### Getting Media Item Properties

- [func enumerateValues(forProperties: Set<String>?, using: (String, Any, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/ituneslibrary/itlibmediaentity/enumeratevalues(forproperties:using:))
- [func enumerateValuesExcept(forProperties: Set<String>?, using: (String, Any, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/ituneslibrary/itlibmediaentity/enumeratevaluesexcept(forproperties:using:))
- [func value(forProperty: String) -> Any?](/documentation/ituneslibrary/itlibmediaentity/value(forproperty:))
- [ITLibArtist](/documentation/ituneslibrary/itlibartist)

### Getting Artist Info

- [var name: String?](/documentation/ituneslibrary/itlibartist/name)
- [var persistentID: NSNumber](/documentation/ituneslibrary/itlibartist/persistentid)
- [var sortName: String?](/documentation/ituneslibrary/itlibartist/sortname)
- [ITLibArtwork](/documentation/ituneslibrary/itlibartwork)

### Getting Artwork Info

- [var image: NSImage?](/documentation/ituneslibrary/itlibartwork/image)
- [var imageData: Data?](/documentation/ituneslibrary/itlibartwork/imagedata)
- [var imageDataFormat: ITLibArtworkFormat](/documentation/ituneslibrary/itlibartwork/imagedataformat)

### Artwork Formats

- [ITLibArtworkFormat](/documentation/ituneslibrary/itlibartworkformat)

#### Artwork Formats

- [case none](/documentation/ituneslibrary/itlibartworkformat/none)
- [case bitmap](/documentation/ituneslibrary/itlibartworkformat/bitmap)
- [case JPEG](/documentation/ituneslibrary/itlibartworkformat/jpeg)
- [case JPEG2000](/documentation/ituneslibrary/itlibartworkformat/jpeg2000)
- [case GIF](/documentation/ituneslibrary/itlibartworkformat/gif)
- [case PNG](/documentation/ituneslibrary/itlibartworkformat/png)
- [case BMP](/documentation/ituneslibrary/itlibartworkformat/bmp)
- [case TIFF](/documentation/ituneslibrary/itlibartworkformat/tiff)
- [case PICT](/documentation/ituneslibrary/itlibartworkformat/pict)

#### Initializers

- [init?(rawValue: UInt)](/documentation/ituneslibrary/itlibartworkformat/init(rawvalue:))
- [ITLibMediaItemVideoInfo](/documentation/ituneslibrary/itlibmediaitemvideoinfo)

### Getting Video Information

- [var videoWidth: Int](/documentation/ituneslibrary/itlibmediaitemvideoinfo/videowidth)
- [var videoHeight: Int](/documentation/ituneslibrary/itlibmediaitemvideoinfo/videoheight)
- [var series: String?](/documentation/ituneslibrary/itlibmediaitemvideoinfo/series)
- [var sortSeries: String?](/documentation/ituneslibrary/itlibmediaitemvideoinfo/sortseries)
- [var season: Int](/documentation/ituneslibrary/itlibmediaitemvideoinfo/season)
- [var isHD: Bool](/documentation/ituneslibrary/itlibmediaitemvideoinfo/ishd)
- [var episode: String?](/documentation/ituneslibrary/itlibmediaitemvideoinfo/episode)
- [var episodeOrder: Int](/documentation/ituneslibrary/itlibmediaitemvideoinfo/episodeorder)

## Structures

- [DidChangeLibraryMessage](/documentation/ituneslibrary/didchangelibrarymessage)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
