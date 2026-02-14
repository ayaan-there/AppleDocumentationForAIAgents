# MusicKit Documentation

Source: https://sosumi.ai/documentation/musickit

---
title: MusicKit
source: https://developer.apple.com/documentation/musickit
timestamp: 2026-02-13T19:23:48.157Z
---

## Essentials

- [Using Automatic Developer Token Generation for Apple Music API](/documentation/musickit/using-automatic-token-generation-for-apple-music-api)
- [Using MusicKit to Integrate with Apple Music](/documentation/musickit/using_musickit_to_integrate_with_apple_music)
- [NSAppleMusicUsageDescription](/documentation/bundleresources/information-property-list/nsapplemusicusagedescription)

## Music Items

- [Album](/documentation/musickit/album)

### Instance Properties

- [var appearsOn: MusicItemCollection<Playlist>?](/documentation/musickit/album/appearson)
- [var artistName: String](/documentation/musickit/album/artistname)
- [var artistURL: URL?](/documentation/musickit/album/artisturl)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/album/artists)
- [var artwork: Artwork?](/documentation/musickit/album/artwork)
- [var audioVariants: [AudioVariant]?](/documentation/musickit/album/audiovariants)
- [var contentRating: ContentRating?](/documentation/musickit/album/contentrating)
- [var copyright: String?](/documentation/musickit/album/copyright)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/album/editorialnotes)
- [var genreNames: [String]](/documentation/musickit/album/genrenames)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/album/genres)
- [let id: MusicItemID](/documentation/musickit/album/id)
- [var isAppleDigitalMaster: Bool?](/documentation/musickit/album/isappledigitalmaster)
- [var isCompilation: Bool?](/documentation/musickit/album/iscompilation)
- [var isComplete: Bool?](/documentation/musickit/album/iscomplete)
- [var isSingle: Bool?](/documentation/musickit/album/issingle)
- [var lastPlayedDate: Date?](/documentation/musickit/album/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/album/libraryaddeddate)
- [var otherVersions: MusicItemCollection<Album>?](/documentation/musickit/album/otherversions)
- [var playParameters: PlayParameters?](/documentation/musickit/album/playparameters)
- [var recordLabelName: String?](/documentation/musickit/album/recordlabelname)
- [var recordLabels: MusicItemCollection<RecordLabel>?](/documentation/musickit/album/recordlabels)
- [var relatedAlbums: MusicItemCollection<Album>?](/documentation/musickit/album/relatedalbums)
- [var relatedVideos: MusicItemCollection<MusicVideo>?](/documentation/musickit/album/relatedvideos)
- [var releaseDate: Date?](/documentation/musickit/album/releasedate)
- [var title: String](/documentation/musickit/album/title)
- [var trackCount: Int](/documentation/musickit/album/trackcount)
- [var tracks: MusicItemCollection<Track>?](/documentation/musickit/album/tracks)
- [var upc: String?](/documentation/musickit/album/upc)
- [var url: URL?](/documentation/musickit/album/url)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/album/filterablemusicitem-implementations)

#### Type Aliases

- [Album.FilterType](/documentation/musickit/album/filtertype)
- [MusicLibraryRequestable Implementations](/documentation/musickit/album/musiclibraryrequestable-implementations)

#### Type Aliases

- [Album.LibraryFilter](/documentation/musickit/album/libraryfilter)
- [Album.LibrarySortProperties](/documentation/musickit/album/librarysortproperties)
- [Artist](/documentation/musickit/artist)

### Instance Properties

- [var albums: MusicItemCollection<Album>?](/documentation/musickit/artist/albums)
- [var appearsOnAlbums: MusicItemCollection<Album>?](/documentation/musickit/artist/appearsonalbums)
- [var artwork: Artwork?](/documentation/musickit/artist/artwork)
- [var compilationAlbums: MusicItemCollection<Album>?](/documentation/musickit/artist/compilationalbums)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/artist/editorialnotes)
- [var featuredAlbums: MusicItemCollection<Album>?](/documentation/musickit/artist/featuredalbums)
- [var featuredPlaylists: MusicItemCollection<Playlist>?](/documentation/musickit/artist/featuredplaylists)
- [var fullAlbums: MusicItemCollection<Album>?](/documentation/musickit/artist/fullalbums)
- [var genreNames: [String]?](/documentation/musickit/artist/genrenames)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/artist/genres)
- [let id: MusicItemID](/documentation/musickit/artist/id)
- [var latestRelease: Album?](/documentation/musickit/artist/latestrelease)
- [var libraryAddedDate: Date?](/documentation/musickit/artist/libraryaddeddate)
- [var liveAlbums: MusicItemCollection<Album>?](/documentation/musickit/artist/livealbums)
- [var musicVideos: MusicItemCollection<MusicVideo>?](/documentation/musickit/artist/musicvideos)
- [var name: String](/documentation/musickit/artist/name)
- [var playlists: MusicItemCollection<Playlist>?](/documentation/musickit/artist/playlists)
- [var similarArtists: MusicItemCollection<Artist>?](/documentation/musickit/artist/similarartists)
- [var singles: MusicItemCollection<Album>?](/documentation/musickit/artist/singles)
- [var station: Station?](/documentation/musickit/artist/station)
- [var topMusicVideos: MusicItemCollection<MusicVideo>?](/documentation/musickit/artist/topmusicvideos)
- [var topSongs: MusicItemCollection<Song>?](/documentation/musickit/artist/topsongs)
- [var url: URL?](/documentation/musickit/artist/url)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/artist/filterablemusicitem-implementations)

#### Type Aliases

- [Artist.FilterType](/documentation/musickit/artist/filtertype)
- [MusicLibraryRequestable Implementations](/documentation/musickit/artist/musiclibraryrequestable-implementations)

#### Type Aliases

- [Artist.LibraryFilter](/documentation/musickit/artist/libraryfilter)
- [Artist.LibrarySortProperties](/documentation/musickit/artist/librarysortproperties)
- [Curator](/documentation/musickit/curator)

### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/curator/artwork)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/curator/editorialnotes)
- [let id: MusicItemID](/documentation/musickit/curator/id)
- [var kind: Curator.Kind](/documentation/musickit/curator/kind-swift.property)
- [var name: String](/documentation/musickit/curator/name)
- [var playlists: MusicItemCollection<Playlist>?](/documentation/musickit/curator/playlists)
- [var url: URL?](/documentation/musickit/curator/url)

### Enumerations

- [Curator.Kind](/documentation/musickit/curator/kind-swift.enum)

#### Enumeration Cases

- [case editorial](/documentation/musickit/curator/kind-swift.enum/editorial)
- [case external](/documentation/musickit/curator/kind-swift.enum/external)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/curator/filterablemusicitem-implementations)

#### Type Aliases

- [Curator.FilterType](/documentation/musickit/curator/filtertype)
- [Genre](/documentation/musickit/genre)

### Instance Properties

- [let id: MusicItemID](/documentation/musickit/genre/id)
- [var libraryAddedDate: Date?](/documentation/musickit/genre/libraryaddeddate)
- [var name: String](/documentation/musickit/genre/name)
- [var parent: Genre?](/documentation/musickit/genre/parent)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/genre/filterablemusicitem-implementations)

#### Type Aliases

- [Genre.FilterType](/documentation/musickit/genre/filtertype)
- [MusicLibraryRequestable Implementations](/documentation/musickit/genre/musiclibraryrequestable-implementations)

#### Type Aliases

- [Genre.LibraryFilter](/documentation/musickit/genre/libraryfilter)
- [Genre.LibrarySortProperties](/documentation/musickit/genre/librarysortproperties)
- [MusicVideo](/documentation/musickit/musicvideo)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/musicvideo/albumtitle)
- [var albums: MusicItemCollection<Album>?](/documentation/musickit/musicvideo/albums)
- [var artistName: String](/documentation/musickit/musicvideo/artistname)
- [var artistURL: URL?](/documentation/musickit/musicvideo/artisturl)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/musicvideo/artists)
- [var artwork: Artwork?](/documentation/musickit/musicvideo/artwork)
- [var contentRating: ContentRating?](/documentation/musickit/musicvideo/contentrating)
- [var duration: TimeInterval?](/documentation/musickit/musicvideo/duration)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/musicvideo/editorialnotes)
- [var genreNames: [String]](/documentation/musickit/musicvideo/genrenames)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/musicvideo/genres)
- [var has4K: Bool?](/documentation/musickit/musicvideo/has4k)
- [var hasHDR: Bool?](/documentation/musickit/musicvideo/hashdr)
- [let id: MusicItemID](/documentation/musickit/musicvideo/id)
- [var isPreview: Bool](/documentation/musickit/musicvideo/ispreview)
- [var isrc: String?](/documentation/musickit/musicvideo/isrc)
- [var lastPlayedDate: Date?](/documentation/musickit/musicvideo/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/musicvideo/libraryaddeddate)
- [var moreByArtist: MusicItemCollection<MusicVideo>?](/documentation/musickit/musicvideo/morebyartist)
- [var moreInGenre: MusicItemCollection<MusicVideo>?](/documentation/musickit/musicvideo/moreingenre)
- [var playCount: Int?](/documentation/musickit/musicvideo/playcount)
- [var playParameters: PlayParameters?](/documentation/musickit/musicvideo/playparameters)
- [var previewAssets: [PreviewAsset]?](/documentation/musickit/musicvideo/previewassets)
- [var releaseDate: Date?](/documentation/musickit/musicvideo/releasedate)
- [var songs: MusicItemCollection<Song>?](/documentation/musickit/musicvideo/songs)
- [var title: String](/documentation/musickit/musicvideo/title)
- [var trackNumber: Int?](/documentation/musickit/musicvideo/tracknumber)
- [var url: URL?](/documentation/musickit/musicvideo/url)
- [var workName: String?](/documentation/musickit/musicvideo/workname)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/musicvideo/filterablemusicitem-implementations)

#### Type Aliases

- [MusicVideo.FilterType](/documentation/musickit/musicvideo/filtertype)
- [MusicLibraryRequestable Implementations](/documentation/musickit/musicvideo/musiclibraryrequestable-implementations)

#### Type Aliases

- [MusicVideo.LibraryFilter](/documentation/musickit/musicvideo/libraryfilter)
- [MusicVideo.LibrarySortProperties](/documentation/musickit/musicvideo/librarysortproperties)
- [Playlist](/documentation/musickit/playlist)

### Structures

- [Playlist.Entry](/documentation/musickit/playlist/entry)

#### Instance Properties

- [var albumTitle: String?](/documentation/musickit/playlist/entry/albumtitle)
- [var artistName: String](/documentation/musickit/playlist/entry/artistname)
- [var artistURL: URL?](/documentation/musickit/playlist/entry/artisturl)
- [var artwork: Artwork?](/documentation/musickit/playlist/entry/artwork)
- [var contentRating: ContentRating?](/documentation/musickit/playlist/entry/contentrating)
- [var duration: TimeInterval?](/documentation/musickit/playlist/entry/duration)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/playlist/entry/editorialnotes)
- [var genreNames: [String]](/documentation/musickit/playlist/entry/genrenames)
- [let id: MusicItemID](/documentation/musickit/playlist/entry/id)
- [var isrc: String?](/documentation/musickit/playlist/entry/isrc)
- [var item: Playlist.Entry.Item?](/documentation/musickit/playlist/entry/item-swift.property)
- [var lastPlayedDate: Date?](/documentation/musickit/playlist/entry/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/playlist/entry/libraryaddeddate)
- [var playCount: Int?](/documentation/musickit/playlist/entry/playcount)
- [var playParameters: PlayParameters?](/documentation/musickit/playlist/entry/playparameters)
- [var position: Int](/documentation/musickit/playlist/entry/position)
- [var previewAssets: [PreviewAsset]?](/documentation/musickit/playlist/entry/previewassets)
- [var releaseDate: Date?](/documentation/musickit/playlist/entry/releasedate)
- [var title: String](/documentation/musickit/playlist/entry/title)
- [var url: URL?](/documentation/musickit/playlist/entry/url)

#### Enumerations

- [Playlist.Entry.Item](/documentation/musickit/playlist/entry/item-swift.enum)

##### Enumeration Cases

- [case musicVideo(MusicVideo)](/documentation/musickit/playlist/entry/item-swift.enum/musicvideo(_:))
- [case song(Song)](/documentation/musickit/playlist/entry/item-swift.enum/song(_:))

##### Instance Properties

- [var albumTitle: String?](/documentation/musickit/playlist/entry/item-swift.enum/albumtitle)
- [var artistName: String](/documentation/musickit/playlist/entry/item-swift.enum/artistname)
- [var artistURL: URL?](/documentation/musickit/playlist/entry/item-swift.enum/artisturl)
- [var artwork: Artwork?](/documentation/musickit/playlist/entry/item-swift.enum/artwork)
- [var contentRating: ContentRating?](/documentation/musickit/playlist/entry/item-swift.enum/contentrating)
- [var duration: TimeInterval?](/documentation/musickit/playlist/entry/item-swift.enum/duration)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/playlist/entry/item-swift.enum/editorialnotes)
- [var genreNames: [String]](/documentation/musickit/playlist/entry/item-swift.enum/genrenames)
- [var id: MusicItemID](/documentation/musickit/playlist/entry/item-swift.enum/id)
- [var isrc: String?](/documentation/musickit/playlist/entry/item-swift.enum/isrc)
- [var lastPlayedDate: Date?](/documentation/musickit/playlist/entry/item-swift.enum/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/playlist/entry/item-swift.enum/libraryaddeddate)
- [var playCount: Int?](/documentation/musickit/playlist/entry/item-swift.enum/playcount)
- [var playParameters: PlayParameters?](/documentation/musickit/playlist/entry/item-swift.enum/playparameters)
- [var previewAssets: [PreviewAsset]?](/documentation/musickit/playlist/entry/item-swift.enum/previewassets)
- [var releaseDate: Date?](/documentation/musickit/playlist/entry/item-swift.enum/releasedate)
- [var title: String](/documentation/musickit/playlist/entry/item-swift.enum/title)
- [var url: URL?](/documentation/musickit/playlist/entry/item-swift.enum/url)

#### Default Implementations

- [MusicLibraryRequestable Implementations](/documentation/musickit/playlist/entry/musiclibraryrequestable-implementations)

##### Type Aliases

- [Playlist.Entry.LibraryFilter](/documentation/musickit/playlist/entry/libraryfilter)
- [Playlist.Entry.LibrarySortProperties](/documentation/musickit/playlist/entry/librarysortproperties)

### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/playlist/artwork)
- [var curator: Curator?](/documentation/musickit/playlist/curator)
- [var curatorName: String?](/documentation/musickit/playlist/curatorname)
- [var entries: MusicItemCollection<Playlist.Entry>?](/documentation/musickit/playlist/entries)
- [var featuredArtists: MusicItemCollection<Artist>?](/documentation/musickit/playlist/featuredartists)
- [let id: MusicItemID](/documentation/musickit/playlist/id)
- [var isChart: Bool?](/documentation/musickit/playlist/ischart)
- [var kind: Playlist.Kind?](/documentation/musickit/playlist/kind-swift.property)
- [var lastModifiedDate: Date?](/documentation/musickit/playlist/lastmodifieddate)
- [var lastPlayedDate: Date?](/documentation/musickit/playlist/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/playlist/libraryaddeddate)
- [var moreByCurator: MusicItemCollection<Playlist>?](/documentation/musickit/playlist/morebycurator)
- [var name: String](/documentation/musickit/playlist/name)
- [var playParameters: PlayParameters?](/documentation/musickit/playlist/playparameters)
- [var radioShow: RadioShow?](/documentation/musickit/playlist/radioshow)
- [var shortDescription: String?](/documentation/musickit/playlist/shortdescription)
- [var standardDescription: String?](/documentation/musickit/playlist/standarddescription)
- [var tracks: MusicItemCollection<Track>?](/documentation/musickit/playlist/tracks)
- [var url: URL?](/documentation/musickit/playlist/url)

### Enumerations

- [Playlist.Kind](/documentation/musickit/playlist/kind-swift.enum)

#### Enumeration Cases

- [case editorial](/documentation/musickit/playlist/kind-swift.enum/editorial)
- [case external](/documentation/musickit/playlist/kind-swift.enum/external)
- [case personalMix](/documentation/musickit/playlist/kind-swift.enum/personalmix)
- [case replay](/documentation/musickit/playlist/kind-swift.enum/replay)
- [case userShared](/documentation/musickit/playlist/kind-swift.enum/usershared)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/playlist/filterablemusicitem-implementations)

#### Type Aliases

- [Playlist.FilterType](/documentation/musickit/playlist/filtertype)
- [MusicLibraryRequestable Implementations](/documentation/musickit/playlist/musiclibraryrequestable-implementations)

#### Type Aliases

- [Playlist.LibraryFilter](/documentation/musickit/playlist/libraryfilter)
- [Playlist.LibrarySortProperties](/documentation/musickit/playlist/librarysortproperties)
- [RadioShow](/documentation/musickit/radioshow)

### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/radioshow/artwork)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/radioshow/editorialnotes)
- [var hostName: String?](/documentation/musickit/radioshow/hostname)
- [let id: MusicItemID](/documentation/musickit/radioshow/id)
- [var name: String](/documentation/musickit/radioshow/name)
- [var playlists: MusicItemCollection<Playlist>?](/documentation/musickit/radioshow/playlists)
- [var url: URL?](/documentation/musickit/radioshow/url)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/radioshow/filterablemusicitem-implementations)

#### Type Aliases

- [RadioShow.FilterType](/documentation/musickit/radioshow/filtertype)
- [RecordLabel](/documentation/musickit/recordlabel)

### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/recordlabel/artwork)
- [let id: MusicItemID](/documentation/musickit/recordlabel/id)
- [var latestReleases: MusicItemCollection<Album>?](/documentation/musickit/recordlabel/latestreleases)
- [var name: String](/documentation/musickit/recordlabel/name)
- [var shortDescription: String?](/documentation/musickit/recordlabel/shortdescription)
- [var standardDescription: String?](/documentation/musickit/recordlabel/standarddescription)
- [var topReleases: MusicItemCollection<Album>?](/documentation/musickit/recordlabel/topreleases)
- [var url: URL?](/documentation/musickit/recordlabel/url)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/recordlabel/filterablemusicitem-implementations)

#### Type Aliases

- [RecordLabel.FilterType](/documentation/musickit/recordlabel/filtertype)
- [Song](/documentation/musickit/song)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/song/albumtitle)
- [var albums: MusicItemCollection<Album>?](/documentation/musickit/song/albums)
- [var artistName: String](/documentation/musickit/song/artistname)
- [var artistURL: URL?](/documentation/musickit/song/artisturl)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/song/artists)
- [var artwork: Artwork?](/documentation/musickit/song/artwork)
- [var attribution: String?](/documentation/musickit/song/attribution)
- [var audioVariants: [AudioVariant]?](/documentation/musickit/song/audiovariants)
- [var composerName: String?](/documentation/musickit/song/composername)
- [var composers: MusicItemCollection<Artist>?](/documentation/musickit/song/composers)
- [var contentRating: ContentRating?](/documentation/musickit/song/contentrating)
- [var discNumber: Int?](/documentation/musickit/song/discnumber)
- [var duration: TimeInterval?](/documentation/musickit/song/duration)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/song/editorialnotes)
- [var genreNames: [String]](/documentation/musickit/song/genrenames)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/song/genres)
- [var hasLyrics: Bool](/documentation/musickit/song/haslyrics)
- [let id: MusicItemID](/documentation/musickit/song/id)
- [var isAppleDigitalMaster: Bool?](/documentation/musickit/song/isappledigitalmaster)
- [var isrc: String?](/documentation/musickit/song/isrc)
- [var lastPlayedDate: Date?](/documentation/musickit/song/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/song/libraryaddeddate)
- [var movementCount: Int?](/documentation/musickit/song/movementcount)
- [var movementName: String?](/documentation/musickit/song/movementname)
- [var movementNumber: Int?](/documentation/musickit/song/movementnumber)
- [var musicVideos: MusicItemCollection<MusicVideo>?](/documentation/musickit/song/musicvideos)
- [var playCount: Int?](/documentation/musickit/song/playcount)
- [var playParameters: PlayParameters?](/documentation/musickit/song/playparameters)
- [var previewAssets: [PreviewAsset]?](/documentation/musickit/song/previewassets)
- [var releaseDate: Date?](/documentation/musickit/song/releasedate)
- [var station: Station?](/documentation/musickit/song/station)
- [var title: String](/documentation/musickit/song/title)
- [var trackNumber: Int?](/documentation/musickit/song/tracknumber)
- [var url: URL?](/documentation/musickit/song/url)
- [var workName: String?](/documentation/musickit/song/workname)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/song/filterablemusicitem-implementations)

#### Type Aliases

- [Song.FilterType](/documentation/musickit/song/filtertype)
- [MusicLibraryRequestable Implementations](/documentation/musickit/song/musiclibraryrequestable-implementations)

#### Type Aliases

- [Song.LibraryFilter](/documentation/musickit/song/libraryfilter)
- [Song.LibrarySortProperties](/documentation/musickit/song/librarysortproperties)
- [Station](/documentation/musickit/station)

### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/station/artwork)
- [var contentRating: ContentRating?](/documentation/musickit/station/contentrating)
- [var duration: TimeInterval?](/documentation/musickit/station/duration)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/station/editorialnotes)
- [var episodeNumber: Int?](/documentation/musickit/station/episodenumber)
- [let id: MusicItemID](/documentation/musickit/station/id)
- [var isLive: Bool](/documentation/musickit/station/islive)
- [var name: String](/documentation/musickit/station/name)
- [var playParameters: PlayParameters?](/documentation/musickit/station/playparameters)
- [var stationProviderName: String?](/documentation/musickit/station/stationprovidername)
- [var url: URL?](/documentation/musickit/station/url)

### Default Implementations

- [FilterableMusicItem Implementations](/documentation/musickit/station/filterablemusicitem-implementations)

#### Type Aliases

- [Station.FilterType](/documentation/musickit/station/filtertype)
- [Track](/documentation/musickit/track)

### Enumeration Cases

- [case musicVideo(MusicVideo)](/documentation/musickit/track/musicvideo(_:))
- [case song(Song)](/documentation/musickit/track/song(_:))

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/track/albumtitle)
- [var albums: MusicItemCollection<Album>?](/documentation/musickit/track/albums)
- [var artistName: String](/documentation/musickit/track/artistname)
- [var artistURL: URL?](/documentation/musickit/track/artisturl)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/track/artists)
- [var artwork: Artwork?](/documentation/musickit/track/artwork)
- [var contentRating: ContentRating?](/documentation/musickit/track/contentrating)
- [var discNumber: Int?](/documentation/musickit/track/discnumber)
- [var duration: TimeInterval?](/documentation/musickit/track/duration)
- [var editorialNotes: EditorialNotes?](/documentation/musickit/track/editorialnotes)
- [var genreNames: [String]](/documentation/musickit/track/genrenames)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/track/genres)
- [var id: MusicItemID](/documentation/musickit/track/id)
- [var isrc: String?](/documentation/musickit/track/isrc)
- [var lastPlayedDate: Date?](/documentation/musickit/track/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/track/libraryaddeddate)
- [var playCount: Int?](/documentation/musickit/track/playcount)
- [var playParameters: PlayParameters?](/documentation/musickit/track/playparameters)
- [var previewAssets: [PreviewAsset]?](/documentation/musickit/track/previewassets)
- [var releaseDate: Date?](/documentation/musickit/track/releasedate)
- [var title: String](/documentation/musickit/track/title)
- [var trackNumber: Int?](/documentation/musickit/track/tracknumber)
- [var url: URL?](/documentation/musickit/track/url)
- [var workName: String?](/documentation/musickit/track/workname)

### Default Implementations

- [MusicLibraryRequestable Implementations](/documentation/musickit/track/musiclibraryrequestable-implementations)

#### Type Aliases

- [Track.LibraryFilter](/documentation/musickit/track/libraryfilter)
- [Track.LibrarySortProperties](/documentation/musickit/track/librarysortproperties)

## Music Item Attributes

- [ContentRating](/documentation/musickit/contentrating)

### Enumeration Cases

- [case clean](/documentation/musickit/contentrating/clean)
- [case explicit](/documentation/musickit/contentrating/explicit)
- [EditorialNotes](/documentation/musickit/editorialnotes)

### Instance Properties

- [let name: String?](/documentation/musickit/editorialnotes/name)
- [let short: String?](/documentation/musickit/editorialnotes/short)
- [let standard: String?](/documentation/musickit/editorialnotes/standard)
- [let tagline: String?](/documentation/musickit/editorialnotes/tagline)
- [PreviewAsset](/documentation/musickit/previewasset)

### Instance Properties

- [let artwork: Artwork?](/documentation/musickit/previewasset/artwork)
- [let hlsURL: URL?](/documentation/musickit/previewasset/hlsurl)
- [let url: URL?](/documentation/musickit/previewasset/url)

## Catalog Search

- [MusicCatalogSearchRequest](/documentation/musickit/musiccatalogsearchrequest)

### Initializers

- [init(term: String, types: [any MusicCatalogSearchable.Type])](/documentation/musickit/musiccatalogsearchrequest/init(term:types:))

### Instance Properties

- [var includeTopResults: Bool](/documentation/musickit/musiccatalogsearchrequest/includetopresults)
- [var limit: Int?](/documentation/musickit/musiccatalogsearchrequest/limit)
- [var offset: Int?](/documentation/musickit/musiccatalogsearchrequest/offset)
- [let term: String](/documentation/musickit/musiccatalogsearchrequest/term)
- [var types: [any MusicCatalogSearchable.Type]](/documentation/musickit/musiccatalogsearchrequest/types)

### Instance Methods

- [func response() async throws -> MusicCatalogSearchResponse](/documentation/musickit/musiccatalogsearchrequest/response())
- [MusicCatalogSearchResponse](/documentation/musickit/musiccatalogsearchresponse)

### Instance Properties

- [let albums: MusicItemCollection<Album>](/documentation/musickit/musiccatalogsearchresponse/albums)
- [let artists: MusicItemCollection<Artist>](/documentation/musickit/musiccatalogsearchresponse/artists)
- [let curators: MusicItemCollection<Curator>](/documentation/musickit/musiccatalogsearchresponse/curators)
- [let musicVideos: MusicItemCollection<MusicVideo>](/documentation/musickit/musiccatalogsearchresponse/musicvideos)
- [let playlists: MusicItemCollection<Playlist>](/documentation/musickit/musiccatalogsearchresponse/playlists)
- [let radioShows: MusicItemCollection<RadioShow>](/documentation/musickit/musiccatalogsearchresponse/radioshows)
- [let recordLabels: MusicItemCollection<RecordLabel>](/documentation/musickit/musiccatalogsearchresponse/recordlabels)
- [let songs: MusicItemCollection<Song>](/documentation/musickit/musiccatalogsearchresponse/songs)
- [let stations: MusicItemCollection<Station>](/documentation/musickit/musiccatalogsearchresponse/stations)
- [let topResults: MusicItemCollection<MusicCatalogSearchResponse.TopResult>](/documentation/musickit/musiccatalogsearchresponse/topresults)

### Enumerations

- [MusicCatalogSearchResponse.TopResult](/documentation/musickit/musiccatalogsearchresponse/topresult)

#### Enumeration Cases

- [case album(Album)](/documentation/musickit/musiccatalogsearchresponse/topresult/album(_:))
- [case artist(Artist)](/documentation/musickit/musiccatalogsearchresponse/topresult/artist(_:))
- [case curator(Curator)](/documentation/musickit/musiccatalogsearchresponse/topresult/curator(_:))
- [case musicVideo(MusicVideo)](/documentation/musickit/musiccatalogsearchresponse/topresult/musicvideo(_:))
- [case playlist(Playlist)](/documentation/musickit/musiccatalogsearchresponse/topresult/playlist(_:))
- [case radioShow(RadioShow)](/documentation/musickit/musiccatalogsearchresponse/topresult/radioshow(_:))
- [case recordLabel(RecordLabel)](/documentation/musickit/musiccatalogsearchresponse/topresult/recordlabel(_:))
- [case song(Song)](/documentation/musickit/musiccatalogsearchresponse/topresult/song(_:))
- [case station(Station)](/documentation/musickit/musiccatalogsearchresponse/topresult/station(_:))

#### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/musiccatalogsearchresponse/topresult/artwork)
- [var id: MusicItemID](/documentation/musickit/musiccatalogsearchresponse/topresult/id)
- [var title: String](/documentation/musickit/musiccatalogsearchresponse/topresult/title)
- [MusicCatalogSearchable](/documentation/musickit/musiccatalogsearchable)

## Resource Loading Using Filters

- [MusicCatalogResourceRequest](/documentation/musickit/musiccatalogresourcerequest)

### Initializers

- [init()](/documentation/musickit/musiccatalogresourcerequest/init())
- [init<Value>(matching: KeyPath<MusicItemType.FilterType, Value>, equalTo: Value)](/documentation/musickit/musiccatalogresourcerequest/init(matching:equalto:))
- [init<Value>(matching: KeyPath<MusicItemType.FilterType, Value>, memberOf: [Value])](/documentation/musickit/musiccatalogresourcerequest/init(matching:memberof:))

### Instance Properties

- [var limit: Int?](/documentation/musickit/musiccatalogresourcerequest/limit)
- [var properties: [PartialMusicAsyncProperty<MusicItemType>]](/documentation/musickit/musiccatalogresourcerequest/properties)

### Instance Methods

- [func response() async throws -> MusicCatalogResourceResponse<MusicItemType>](/documentation/musickit/musiccatalogresourcerequest/response())
- [MusicCatalogResourceResponse](/documentation/musickit/musiccatalogresourceresponse)

### Instance Properties

- [let items: MusicItemCollection<MusicItemType>](/documentation/musickit/musiccatalogresourceresponse/items)
- [AlbumFilter](/documentation/musickit/albumfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/albumfilter/id)
- [var upc: String?](/documentation/musickit/albumfilter/upc)
- [ArtistFilter](/documentation/musickit/artistfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/artistfilter/id)
- [CuratorFilter](/documentation/musickit/curatorfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/curatorfilter/id)
- [GenreFilter](/documentation/musickit/genrefilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/genrefilter/id)
- [MusicVideoFilter](/documentation/musickit/musicvideofilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/musicvideofilter/id)
- [var isrc: String?](/documentation/musickit/musicvideofilter/isrc)
- [PlaylistFilter](/documentation/musickit/playlistfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/playlistfilter/id)
- [RadioShowFilter](/documentation/musickit/radioshowfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/radioshowfilter/id)
- [RecordLabelFilter](/documentation/musickit/recordlabelfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/recordlabelfilter/id)
- [SongFilter](/documentation/musickit/songfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/songfilter/id)
- [var isrc: String?](/documentation/musickit/songfilter/isrc)
- [StationFilter](/documentation/musickit/stationfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/stationfilter/id)
- [FilterableMusicItem](/documentation/musickit/filterablemusicitem)

### Associated Types

- [FilterType](/documentation/musickit/filterablemusicitem/filtertype)

## General Purpose Data Request

- [MusicDataRequest](/documentation/musickit/musicdatarequest)

### Structures

- [MusicDataRequest.Error](/documentation/musickit/musicdatarequest/error)

#### Instance Properties

- [let code: Int](/documentation/musickit/musicdatarequest/error/code)
- [let detailText: String](/documentation/musickit/musicdatarequest/error/detailtext)
- [let id: String](/documentation/musickit/musicdatarequest/error/id)
- [let originalResponse: MusicDataResponse](/documentation/musickit/musicdatarequest/error/originalresponse)
- [let source: MusicDataRequest.Error.Source?](/documentation/musickit/musicdatarequest/error/source-swift.property)
- [let status: Int](/documentation/musickit/musicdatarequest/error/status)
- [let title: String](/documentation/musickit/musicdatarequest/error/title)

#### Enumerations

- [MusicDataRequest.Error.Source](/documentation/musickit/musicdatarequest/error/source-swift.enum)

##### Enumeration Cases

- [case parameter(String)](/documentation/musickit/musicdatarequest/error/source-swift.enum/parameter(_:))

### Initializers

- [init(urlRequest: URLRequest)](/documentation/musickit/musicdatarequest/init(urlrequest:))

### Instance Properties

- [let urlRequest: URLRequest](/documentation/musickit/musicdatarequest/urlrequest)

### Instance Methods

- [func response() async throws -> MusicDataResponse](/documentation/musickit/musicdatarequest/response())

### Type Properties

- [static var currentCountryCode: String](/documentation/musickit/musicdatarequest/currentcountrycode)
- [static var tokenProvider: any MusicUserTokenProvider & MusicDeveloperTokenProvider](/documentation/musickit/musicdatarequest/tokenprovider)
- [MusicDataResponse](/documentation/musickit/musicdataresponse)

### Instance Properties

- [let data: Data](/documentation/musickit/musicdataresponse/data)
- [let urlResponse: HTTPURLResponse](/documentation/musickit/musicdataresponse/urlresponse)

## Playback

- [ApplicationMusicPlayer](/documentation/musickit/applicationmusicplayer)

### Classes

- [ApplicationMusicPlayer.Queue](/documentation/musickit/applicationmusicplayer/queue-swift.class)

#### Structures

- [ApplicationMusicPlayer.Queue.Entries](/documentation/musickit/applicationmusicplayer/queue-swift.class/entries-swift.struct)

##### Initializers

- [init()](/documentation/musickit/applicationmusicplayer/queue-swift.class/entries-swift.struct/init())

#### Initializers

- [init<S>(S, startingAt: S.Element?)](/documentation/musickit/applicationmusicplayer/queue-swift.class/init(_:startingat:))
- [init(album: Album, startingAt: Track)](/documentation/musickit/applicationmusicplayer/queue-swift.class/init(album:startingat:))
- [init(arrayLiteral: any PlayableMusicItem...)](/documentation/musickit/applicationmusicplayer/queue-swift.class/init(arrayliteral:))
- [init<S, PlayableMusicItemType>(for: S, startingAt: S.Element?)](/documentation/musickit/applicationmusicplayer/queue-swift.class/init(for:startingat:))
- [init(playlist: Playlist, startingAt: Playlist.Entry)](/documentation/musickit/applicationmusicplayer/queue-swift.class/init(playlist:startingat:))

#### Instance Properties

- [var entries: ApplicationMusicPlayer.Queue.Entries](/documentation/musickit/applicationmusicplayer/queue-swift.class/entries-swift.property)

### Instance Properties

- [var queue: ApplicationMusicPlayer.Queue](/documentation/musickit/applicationmusicplayer/queue-swift.property)
- [var transition: MusicPlayer.Transition](/documentation/musickit/applicationmusicplayer/transition)

### Type Properties

- [static let shared: ApplicationMusicPlayer](/documentation/musickit/applicationmusicplayer/shared)
- [SystemMusicPlayer](/documentation/musickit/systemmusicplayer)

### Instance Properties

- [var queue: MusicPlayer.Queue](/documentation/musickit/systemmusicplayer/queue)

### Type Properties

- [static let shared: SystemMusicPlayer](/documentation/musickit/systemmusicplayer/shared)
- [MusicPlayer](/documentation/musickit/musicplayer)

### Classes

- [MusicPlayer.Queue](/documentation/musickit/musicplayer/queue)

#### Structures

- [MusicPlayer.Queue.Entry](/documentation/musickit/musicplayer/queue/entry)

##### Initializers

- [init(any PlayableMusicItem, startTime: TimeInterval?, endTime: TimeInterval?)](/documentation/musickit/musicplayer/queue/entry/init(_:starttime:endtime:))

##### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/musicplayer/queue/entry/artwork)
- [var endTime: TimeInterval?](/documentation/musickit/musicplayer/queue/entry/endtime)
- [let id: String](/documentation/musickit/musicplayer/queue/entry/id)
- [var isTransient: Bool](/documentation/musickit/musicplayer/queue/entry/istransient)
- [var item: MusicPlayer.Queue.Entry.Item?](/documentation/musickit/musicplayer/queue/entry/item-swift.property)
- [var startTime: TimeInterval?](/documentation/musickit/musicplayer/queue/entry/starttime)
- [var subtitle: String?](/documentation/musickit/musicplayer/queue/entry/subtitle)
- [var title: String](/documentation/musickit/musicplayer/queue/entry/title)
- [var transientItem: (any PlayableMusicItem)?](/documentation/musickit/musicplayer/queue/entry/transientitem)

##### Enumerations

- [MusicPlayer.Queue.Entry.Item](/documentation/musickit/musicplayer/queue/entry/item-swift.enum)

###### Enumeration Cases

- [case musicVideo(MusicVideo)](/documentation/musickit/musicplayer/queue/entry/item-swift.enum/musicvideo(_:))
- [case song(Song)](/documentation/musickit/musicplayer/queue/entry/item-swift.enum/song(_:))

###### Instance Properties

- [var id: MusicItemID](/documentation/musickit/musicplayer/queue/entry/item-swift.enum/id)
- [var playParameters: PlayParameters?](/documentation/musickit/musicplayer/queue/entry/item-swift.enum/playparameters)

#### Initializers

- [init<S>(S, startingAt: S.Element?)](/documentation/musickit/musicplayer/queue/init(_:startingat:))
- [init(album: Album, startingAt: Track)](/documentation/musickit/musicplayer/queue/init(album:startingat:))
- [init<S, PlayableMusicItemType>(for: S, startingAt: S.Element?)](/documentation/musickit/musicplayer/queue/init(for:startingat:))
- [init(playlist: Playlist, startingAt: Playlist.Entry)](/documentation/musickit/musicplayer/queue/init(playlist:startingat:))

#### Instance Properties

- [var currentEntry: MusicPlayer.Queue.Entry?](/documentation/musickit/musicplayer/queue/currententry)

#### Instance Methods

- [func insert<PlayableMusicItemType>(PlayableMusicItemType, position: MusicPlayer.Queue.EntryInsertionPosition) async throws](/documentation/musickit/musicplayer/queue/insert(_:position:)-186ue)
- [func insert<S, PlayableMusicItemType>(S, position: MusicPlayer.Queue.EntryInsertionPosition) async throws](/documentation/musickit/musicplayer/queue/insert(_:position:)-228pb)
- [func insert(MusicPlayer.Queue.Entry, position: MusicPlayer.Queue.EntryInsertionPosition) async throws](/documentation/musickit/musicplayer/queue/insert(_:position:)-3lv7k)
- [func insert<S>(S, position: MusicPlayer.Queue.EntryInsertionPosition) async throws](/documentation/musickit/musicplayer/queue/insert(_:position:)-58ohm)

#### Enumerations

- [MusicPlayer.Queue.EntryInsertionPosition](/documentation/musickit/musicplayer/queue/entryinsertionposition)

##### Enumeration Cases

- [case afterCurrentEntry](/documentation/musickit/musicplayer/queue/entryinsertionposition/aftercurrententry)
- [case tail](/documentation/musickit/musicplayer/queue/entryinsertionposition/tail)
- [MusicPlayer.State](/documentation/musickit/musicplayer/state-swift.class)

#### Instance Properties

- [var audioVariant: AudioVariant?](/documentation/musickit/musicplayer/state-swift.class/audiovariant)
- [var playbackRate: Float](/documentation/musickit/musicplayer/state-swift.class/playbackrate)
- [var playbackStatus: MusicPlayer.PlaybackStatus](/documentation/musickit/musicplayer/state-swift.class/playbackstatus)
- [var repeatMode: MusicPlayer.RepeatMode?](/documentation/musickit/musicplayer/state-swift.class/repeatmode)
- [var shuffleMode: MusicPlayer.ShuffleMode?](/documentation/musickit/musicplayer/state-swift.class/shufflemode)

### Instance Properties

- [var isPreparedToPlay: Bool](/documentation/musickit/musicplayer/ispreparedtoplay)
- [var playbackTime: TimeInterval](/documentation/musickit/musicplayer/playbacktime)
- [let state: MusicPlayer.State](/documentation/musickit/musicplayer/state-swift.property)

### Instance Methods

- [func beginSeekingBackward()](/documentation/musickit/musicplayer/beginseekingbackward())
- [func beginSeekingForward()](/documentation/musickit/musicplayer/beginseekingforward())
- [func endSeeking()](/documentation/musickit/musicplayer/endseeking())
- [func pause()](/documentation/musickit/musicplayer/pause())
- [func play() async throws](/documentation/musickit/musicplayer/play())
- [func prepareToPlay() async throws](/documentation/musickit/musicplayer/preparetoplay())
- [func restartCurrentEntry()](/documentation/musickit/musicplayer/restartcurrententry())
- [func skipToNextEntry() async throws](/documentation/musickit/musicplayer/skiptonextentry())
- [func skipToPreviousEntry() async throws](/documentation/musickit/musicplayer/skiptopreviousentry())
- [func stop()](/documentation/musickit/musicplayer/stop())

### Enumerations

- [MusicPlayer.PlaybackStatus](/documentation/musickit/musicplayer/playbackstatus)

#### Enumeration Cases

- [case interrupted](/documentation/musickit/musicplayer/playbackstatus/interrupted)
- [case paused](/documentation/musickit/musicplayer/playbackstatus/paused)
- [case playing](/documentation/musickit/musicplayer/playbackstatus/playing)
- [case seekingBackward](/documentation/musickit/musicplayer/playbackstatus/seekingbackward)
- [case seekingForward](/documentation/musickit/musicplayer/playbackstatus/seekingforward)
- [case stopped](/documentation/musickit/musicplayer/playbackstatus/stopped)
- [MusicPlayer.RepeatMode](/documentation/musickit/musicplayer/repeatmode)

#### Enumeration Cases

- [case all](/documentation/musickit/musicplayer/repeatmode/all)
- [case none](/documentation/musickit/musicplayer/repeatmode/none)
- [case one](/documentation/musickit/musicplayer/repeatmode/one)
- [MusicPlayer.ShuffleMode](/documentation/musickit/musicplayer/shufflemode)

#### Enumeration Cases

- [case off](/documentation/musickit/musicplayer/shufflemode/off)
- [case songs](/documentation/musickit/musicplayer/shufflemode/songs)
- [MusicPlayer.Transition](/documentation/musickit/musicplayer/transition)

#### Structures

- [MusicPlayer.Transition.CrossfadeOptions](/documentation/musickit/musicplayer/transition/crossfadeoptions)

##### Initializers

- [init(duration: TimeInterval?)](/documentation/musickit/musicplayer/transition/crossfadeoptions/init(duration:))

#### Enumeration Cases

- [case crossfade(options: MusicPlayer.Transition.CrossfadeOptions)](/documentation/musickit/musicplayer/transition/crossfade(options:))
- [case none](/documentation/musickit/musicplayer/transition/none)

#### Type Properties

- [static let crossfade: MusicPlayer.Transition](/documentation/musickit/musicplayer/transition/crossfade)

#### Type Methods

- [static func crossfade(duration: TimeInterval?) -> MusicPlayer.Transition](/documentation/musickit/musicplayer/transition/crossfade(duration:))
- [PlayableMusicItem](/documentation/musickit/playablemusicitem)

### Instance Properties

- [var playParameters: PlayParameters?](/documentation/musickit/playablemusicitem/playparameters)
- [PlayParameters](/documentation/musickit/playparameters)

## Artwork

- [Artwork](/documentation/musickit/artwork)

### Instance Properties

- [let alternateText: String?](/documentation/musickit/artwork/alternatetext)
- [let backgroundColor: CGColor?](/documentation/musickit/artwork/backgroundcolor)
- [let maximumHeight: Int](/documentation/musickit/artwork/maximumheight)
- [let maximumWidth: Int](/documentation/musickit/artwork/maximumwidth)
- [let primaryTextColor: CGColor?](/documentation/musickit/artwork/primarytextcolor)
- [let quaternaryTextColor: CGColor?](/documentation/musickit/artwork/quaternarytextcolor)
- [let secondaryTextColor: CGColor?](/documentation/musickit/artwork/secondarytextcolor)
- [let tertiaryTextColor: CGColor?](/documentation/musickit/artwork/tertiarytextcolor)

### Instance Methods

- [func url(width: Int, height: Int) -> URL?](/documentation/musickit/artwork/url(width:height:))
- [ArtworkImage](/documentation/musickit/artworkimage)

### Initializers

- [init(Artwork, height: CGFloat)](/documentation/musickit/artworkimage/init(_:height:))
- [init(Artwork, width: CGFloat)](/documentation/musickit/artworkimage/init(_:width:))
- [init(Artwork, width: CGFloat, height: CGFloat)](/documentation/musickit/artworkimage/init(_:width:height:))

## Authorization

- [MusicAuthorization](/documentation/musickit/musicauthorization)

### Type Properties

- [static var currentStatus: MusicAuthorization.Status](/documentation/musickit/musicauthorization/currentstatus)

### Type Methods

- [static func request() async -> MusicAuthorization.Status](/documentation/musickit/musicauthorization/request())

### Enumerations

- [MusicAuthorization.Status](/documentation/musickit/musicauthorization/status)

#### Enumeration Cases

- [case authorized](/documentation/musickit/musicauthorization/status/authorized)
- [case denied](/documentation/musickit/musicauthorization/status/denied)
- [case notDetermined](/documentation/musickit/musicauthorization/status/notdetermined)
- [case restricted](/documentation/musickit/musicauthorization/status/restricted)

## Apple Music Subscription

- [MusicSubscription](/documentation/musickit/musicsubscription)

### Structures

- [MusicSubscription.Updates](/documentation/musickit/musicsubscription/updates)

#### Structures

- [MusicSubscription.Updates.Iterator](/documentation/musickit/musicsubscription/updates/iterator)

#### Type Aliases

- [MusicSubscription.Updates.Element](/documentation/musickit/musicsubscription/updates/element)

### Instance Properties

- [let canBecomeSubscriber: Bool](/documentation/musickit/musicsubscription/canbecomesubscriber)
- [let canPlayCatalogContent: Bool](/documentation/musickit/musicsubscription/canplaycatalogcontent)
- [let hasCloudLibraryEnabled: Bool](/documentation/musickit/musicsubscription/hascloudlibraryenabled)

### Type Properties

- [static var current: MusicSubscription](/documentation/musickit/musicsubscription/current)
- [static var subscriptionUpdates: MusicSubscription.Updates](/documentation/musickit/musicsubscription/subscriptionupdates)

### Enumerations

- [MusicSubscription.Error](/documentation/musickit/musicsubscription/error)

#### Enumeration Cases

- [case permissionDenied](/documentation/musickit/musicsubscription/error/permissiondenied)
- [case privacyAcknowledgementRequired](/documentation/musickit/musicsubscription/error/privacyacknowledgementrequired)
- [case unknown](/documentation/musickit/musicsubscription/error/unknown)
- [MusicSubscriptionOffer](/documentation/musickit/musicsubscriptionoffer)

### Structures

- [MusicSubscriptionOffer.Action](/documentation/musickit/musicsubscriptionoffer/action)

#### Initializers

- [init(String)](/documentation/musickit/musicsubscriptionoffer/action/init(_:))
- [init(rawValue: String)](/documentation/musickit/musicsubscriptionoffer/action/init(rawvalue:))

#### Type Properties

- [static let subscribe: MusicSubscriptionOffer.Action](/documentation/musickit/musicsubscriptionoffer/action/subscribe)
- [MusicSubscriptionOffer.MessageIdentifier](/documentation/musickit/musicsubscriptionoffer/messageidentifier)

#### Initializers

- [init(String)](/documentation/musickit/musicsubscriptionoffer/messageidentifier/init(_:))
- [init(rawValue: String)](/documentation/musickit/musicsubscriptionoffer/messageidentifier/init(rawvalue:))

#### Type Properties

- [static let addMusic: MusicSubscriptionOffer.MessageIdentifier](/documentation/musickit/musicsubscriptionoffer/messageidentifier/addmusic)
- [static let join: MusicSubscriptionOffer.MessageIdentifier](/documentation/musickit/musicsubscriptionoffer/messageidentifier/join)
- [static let playMusic: MusicSubscriptionOffer.MessageIdentifier](/documentation/musickit/musicsubscriptionoffer/messageidentifier/playmusic)
- [MusicSubscriptionOffer.Options](/documentation/musickit/musicsubscriptionoffer/options)

#### Initializers

- [init(action: MusicSubscriptionOffer.Action, messageIdentifier: MusicSubscriptionOffer.MessageIdentifier, itemID: MusicItemID?, affiliateToken: String?, campaignToken: String?)](/documentation/musickit/musicsubscriptionoffer/options/init(action:messageidentifier:itemid:affiliatetoken:campaigntoken:))

#### Instance Properties

- [var action: MusicSubscriptionOffer.Action](/documentation/musickit/musicsubscriptionoffer/options/action)
- [var affiliateToken: String?](/documentation/musickit/musicsubscriptionoffer/options/affiliatetoken)
- [var campaignToken: String?](/documentation/musickit/musicsubscriptionoffer/options/campaigntoken)
- [var itemID: MusicItemID?](/documentation/musickit/musicsubscriptionoffer/options/itemid)
- [var messageIdentifier: MusicSubscriptionOffer.MessageIdentifier](/documentation/musickit/musicsubscriptionoffer/options/messageidentifier)

#### Type Properties

- [static let `default`: MusicSubscriptionOffer.Options](/documentation/musickit/musicsubscriptionoffer/options/default)

## Token management

- [MusicTokenProvider](/documentation/musickit/musictokenprovider)
- [MusicDeveloperTokenProvider](/documentation/musickit/musicdevelopertokenprovider)

### Instance Methods

- [func developerToken(options: MusicTokenRequestOptions) async throws -> String](/documentation/musickit/musicdevelopertokenprovider/developertoken(options:))
- [MusicUserTokenProvider](/documentation/musickit/musicusertokenprovider)

### Initializers

- [init()](/documentation/musickit/musicusertokenprovider/init())

### Instance Methods

- [func userToken(for: String, options: MusicTokenRequestOptions) async throws -> String](/documentation/musickit/musicusertokenprovider/usertoken(for:options:))
- [MusicTokenRequestOptions](/documentation/musickit/musictokenrequestoptions)

### Type Properties

- [static let ignoreCache: MusicTokenRequestOptions](/documentation/musickit/musictokenrequestoptions/ignorecache)
- [MusicTokenRequestError](/documentation/musickit/musictokenrequesterror)

### Enumeration Cases

- [case developerTokenRequestFailed](/documentation/musickit/musictokenrequesterror/developertokenrequestfailed)
- [case permissionDenied](/documentation/musickit/musictokenrequesterror/permissiondenied)
- [case privacyAcknowledgementRequired](/documentation/musickit/musictokenrequesterror/privacyacknowledgementrequired)
- [case unknown](/documentation/musickit/musictokenrequesterror/unknown)
- [case userNotSignedIn](/documentation/musickit/musictokenrequesterror/usernotsignedin)
- [case userTokenRequestFailed](/documentation/musickit/musictokenrequesterror/usertokenrequestfailed)
- [case userTokenRevoked](/documentation/musickit/musictokenrequesterror/usertokenrevoked)
- [DefaultMusicTokenProvider](/documentation/musickit/defaultmusictokenprovider)

### Initializers

- [init()](/documentation/musickit/defaultmusictokenprovider/init())

## Utility

- [MusicItem](/documentation/musickit/musicitem)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/musicitem/id)

### Instance Methods

- [func with([PartialMusicAsyncProperty<Self>]) async throws -> Self](/documentation/musickit/musicitem/with(_:))
- [func with(PartialMusicAsyncProperty<Self>..., preferredSource: MusicPropertySource) async throws -> Self](/documentation/musickit/musicitem/with(_:preferredsource:)-2hn42)
- [func with([PartialMusicAsyncProperty<Self>], preferredSource: MusicPropertySource) async throws -> Self](/documentation/musickit/musicitem/with(_:preferredsource:)-416sk)
- [MusicItemID](/documentation/musickit/musicitemid)

### Initializers

- [init(String)](/documentation/musickit/musicitemid/init(_:))
- [MusicItemCollection](/documentation/musickit/musicitemcollection)

### Operators

- [static func += (inout MusicItemCollection<MusicItemType>, MusicItemCollection<MusicItemType>)](/documentation/musickit/musicitemcollection/+=(_:_:))

### Initializers

- [init<S>(S)](/documentation/musickit/musicitemcollection/init(_:))

### Instance Properties

- [var hasNextBatch: Bool](/documentation/musickit/musicitemcollection/hasnextbatch)
- [var title: String?](/documentation/musickit/musicitemcollection/title)

### Instance Methods

- [func nextBatch(limit: Int?) async throws -> MusicItemCollection<MusicItemType>?](/documentation/musickit/musicitemcollection/nextbatch(limit:)-432i0)
- [func nextBatch(limit: Int?) async throws -> MusicItemCollection<MusicItemType>?](/documentation/musickit/musicitemcollection/nextbatch(limit:)-ywue)
- [MusicPropertyContainer](/documentation/musickit/musicpropertycontainer)

### Instance Methods

- [func with([PartialMusicAsyncProperty<Self>]) async throws -> Self](/documentation/musickit/musicpropertycontainer/with(_:))
- [func with([PartialMusicAsyncProperty<Self>], preferredSource: MusicPropertySource) async throws -> Self](/documentation/musickit/musicpropertycontainer/with(_:preferredsource:)-8ec7p)
- [func with(PartialMusicAsyncProperty<Self>..., preferredSource: MusicPropertySource) async throws -> Self](/documentation/musickit/musicpropertycontainer/with(_:preferredsource:)-9wqhc)
- [MusicRelationshipProperty](/documentation/musickit/musicrelationshipproperty)
- [MusicExtendedAttributeProperty](/documentation/musickit/musicextendedattributeproperty)
- [MusicAttributeProperty](/documentation/musickit/musicattributeproperty)
- [PartialMusicAsyncProperty](/documentation/musickit/partialmusicasyncproperty)
- [PartialMusicProperty](/documentation/musickit/partialmusicproperty)

### Type Properties

- [static let albums: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/albums-2huns)
- [static let albums: MusicRelationshipProperty<Song, Album>](/documentation/musickit/partialmusicproperty/albums-5kqf6)
- [static let albums: MusicRelationshipProperty<MusicVideo, Album>](/documentation/musickit/partialmusicproperty/albums-6v0rp)
- [static let appearsOn: MusicRelationshipProperty<Album, Playlist>](/documentation/musickit/partialmusicproperty/appearson)
- [static let appearsOnAlbums: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/appearsonalbums)
- [static var artistURL: MusicExtendedAttributeProperty<MusicVideo, URL>](/documentation/musickit/partialmusicproperty/artisturl-7j56f)
- [static var artistURL: MusicExtendedAttributeProperty<Song, URL>](/documentation/musickit/partialmusicproperty/artisturl-81r7i)
- [static var artistURL: MusicExtendedAttributeProperty<Album, URL>](/documentation/musickit/partialmusicproperty/artisturl-msvj)
- [static let artists: MusicRelationshipProperty<Album, Artist>](/documentation/musickit/partialmusicproperty/artists-1bm4c)
- [static let artists: MusicRelationshipProperty<Song, Artist>](/documentation/musickit/partialmusicproperty/artists-3x8cx)
- [static let artists: MusicRelationshipProperty<MusicVideo, Artist>](/documentation/musickit/partialmusicproperty/artists-6myll)
- [static let audioVariants: MusicExtendedAttributeProperty<Song, [AudioVariant]>](/documentation/musickit/partialmusicproperty/audiovariants-60v28)
- [static let audioVariants: MusicExtendedAttributeProperty<Album, [AudioVariant]>](/documentation/musickit/partialmusicproperty/audiovariants-8zkt2)
- [static let compilationAlbums: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/compilationalbums)
- [static let composers: MusicRelationshipProperty<Song, Artist>](/documentation/musickit/partialmusicproperty/composers)
- [static let curator: MusicRelationshipProperty<Playlist, Curator>](/documentation/musickit/partialmusicproperty/curator)
- [static let entries: MusicRelationshipProperty<Playlist, Playlist.Entry>](/documentation/musickit/partialmusicproperty/entries)
- [static let featuredAlbums: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/featuredalbums)
- [static let featuredArtists: MusicRelationshipProperty<Playlist, Artist>](/documentation/musickit/partialmusicproperty/featuredartists)
- [static let featuredPlaylists: MusicRelationshipProperty<Artist, Playlist>](/documentation/musickit/partialmusicproperty/featuredplaylists)
- [static let fullAlbums: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/fullalbums)
- [static let genres: MusicRelationshipProperty<MusicVideo, Genre>](/documentation/musickit/partialmusicproperty/genres-2y2ss)
- [static let genres: MusicRelationshipProperty<Artist, Genre>](/documentation/musickit/partialmusicproperty/genres-3jsli)
- [static let genres: MusicRelationshipProperty<Song, Genre>](/documentation/musickit/partialmusicproperty/genres-5w9nm)
- [static let genres: MusicRelationshipProperty<Album, Genre>](/documentation/musickit/partialmusicproperty/genres-7el74)
- [static let latestRelease: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/latestrelease)
- [static var latestReleases: MusicRelationshipProperty<RecordLabel, Album>](/documentation/musickit/partialmusicproperty/latestreleases)
- [static let liveAlbums: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/livealbums)
- [static let moreByArtist: MusicRelationshipProperty<MusicVideo, MusicVideo>](/documentation/musickit/partialmusicproperty/morebyartist)
- [static let moreByCurator: MusicRelationshipProperty<Playlist, Playlist>](/documentation/musickit/partialmusicproperty/morebycurator)
- [static let moreInGenre: MusicRelationshipProperty<MusicVideo, MusicVideo>](/documentation/musickit/partialmusicproperty/moreingenre)
- [static let musicVideos: MusicRelationshipProperty<Artist, MusicVideo>](/documentation/musickit/partialmusicproperty/musicvideos-6hip3)
- [static let musicVideos: MusicRelationshipProperty<Song, MusicVideo>](/documentation/musickit/partialmusicproperty/musicvideos-89mym)
- [static let otherVersions: MusicRelationshipProperty<Album, Album>](/documentation/musickit/partialmusicproperty/otherversions)
- [static let playlists: MusicRelationshipProperty<Artist, Playlist>](/documentation/musickit/partialmusicproperty/playlists-1j0l9)
- [static let playlists: MusicRelationshipProperty<Curator, Playlist>](/documentation/musickit/partialmusicproperty/playlists-9quj1)
- [static let playlists: MusicRelationshipProperty<RadioShow, Playlist>](/documentation/musickit/partialmusicproperty/playlists-wgt7)
- [static let radioShow: MusicRelationshipProperty<Playlist, RadioShow>](/documentation/musickit/partialmusicproperty/radioshow)
- [static let recordLabels: MusicRelationshipProperty<Album, RecordLabel>](/documentation/musickit/partialmusicproperty/recordlabels)
- [static let relatedAlbums: MusicRelationshipProperty<Album, Album>](/documentation/musickit/partialmusicproperty/relatedalbums)
- [static let relatedVideos: MusicRelationshipProperty<Album, MusicVideo>](/documentation/musickit/partialmusicproperty/relatedvideos)
- [static let similarArtists: MusicRelationshipProperty<Artist, Artist>](/documentation/musickit/partialmusicproperty/similarartists)
- [static let singles: MusicRelationshipProperty<Artist, Album>](/documentation/musickit/partialmusicproperty/singles)
- [static let songs: MusicRelationshipProperty<MusicVideo, Song>](/documentation/musickit/partialmusicproperty/songs)
- [static let station: MusicRelationshipProperty<Song, Station>](/documentation/musickit/partialmusicproperty/station-8u1rf)
- [static let station: MusicRelationshipProperty<Artist, Station>](/documentation/musickit/partialmusicproperty/station-8zftf)
- [static let topMusicVideos: MusicRelationshipProperty<Artist, MusicVideo>](/documentation/musickit/partialmusicproperty/topmusicvideos)
- [static var topReleases: MusicRelationshipProperty<RecordLabel, Album>](/documentation/musickit/partialmusicproperty/topreleases)
- [static let topSongs: MusicRelationshipProperty<Artist, Song>](/documentation/musickit/partialmusicproperty/topsongs)
- [static let tracks: MusicRelationshipProperty<Playlist, Track>](/documentation/musickit/partialmusicproperty/tracks-8mq2j)
- [static let tracks: MusicRelationshipProperty<Album, Track>](/documentation/musickit/partialmusicproperty/tracks-9mk2l)
- [AnyMusicProperty](/documentation/musickit/anymusicproperty)

## Classes

- [MusicLibrary](/documentation/musickit/musiclibrary)

### Instance Methods

- [func add<MusicItemType>(MusicItemType) async throws](/documentation/musickit/musiclibrary/add(_:))
- [func add<MusicItemType>(MusicItemType, to: Playlist) async throws -> Playlist](/documentation/musickit/musiclibrary/add(_:to:))
- [func createPlaylist(name: String, description: String?, authorDisplayName: String?) async throws -> Playlist](/documentation/musickit/musiclibrary/createplaylist(name:description:authordisplayname:))
- [func createPlaylist<S, MusicPlaylistAddableType>(name: String, description: String?, authorDisplayName: String?, items: S) async throws -> Playlist](/documentation/musickit/musiclibrary/createplaylist(name:description:authordisplayname:items:))
- [func edit(Playlist, name: String?, description: String?, authorDisplayName: String?) async throws -> Playlist](/documentation/musickit/musiclibrary/edit(_:name:description:authordisplayname:))
- [func edit<S, MusicPlaylistAddableType>(Playlist, name: String?, description: String?, authorDisplayName: String?, items: S) async throws -> Playlist](/documentation/musickit/musiclibrary/edit(_:name:description:authordisplayname:items:))

### Type Properties

- [static let shared: MusicLibrary](/documentation/musickit/musiclibrary/shared)

### Enumerations

- [MusicLibrary.Error](/documentation/musickit/musiclibrary/error)

#### Enumeration Cases

- [case addToPlaylistFailed](/documentation/musickit/musiclibrary/error/addtoplaylistfailed)
- [case createPlaylistFailed](/documentation/musickit/musiclibrary/error/createplaylistfailed)
- [case editPlaylistFailed](/documentation/musickit/musiclibrary/error/editplaylistfailed)
- [case itemAlreadyAdded](/documentation/musickit/musiclibrary/error/itemalreadyadded)
- [case permissionDenied](/documentation/musickit/musiclibrary/error/permissiondenied)
- [case playlistNotInLibrary](/documentation/musickit/musiclibrary/error/playlistnotinlibrary)
- [case unableToAddItem](/documentation/musickit/musiclibrary/error/unabletoadditem)
- [case unknown](/documentation/musickit/musiclibrary/error/unknown)

## Protocols

- [LibraryAlbumFilter](/documentation/musickit/libraryalbumfilter)

### Instance Properties

- [var artistName: String](/documentation/musickit/libraryalbumfilter/artistname)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/libraryalbumfilter/artists)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/libraryalbumfilter/genres)
- [var id: MusicItemID](/documentation/musickit/libraryalbumfilter/id)
- [var isCompilation: Bool?](/documentation/musickit/libraryalbumfilter/iscompilation)
- [var title: String](/documentation/musickit/libraryalbumfilter/title)
- [LibraryAlbumSortProperties](/documentation/musickit/libraryalbumsortproperties)

### Instance Properties

- [var artistName: String](/documentation/musickit/libraryalbumsortproperties/artistname)
- [var lastPlayedDate: Date?](/documentation/musickit/libraryalbumsortproperties/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/libraryalbumsortproperties/libraryaddeddate)
- [var releaseDate: Date?](/documentation/musickit/libraryalbumsortproperties/releasedate)
- [var title: String](/documentation/musickit/libraryalbumsortproperties/title)
- [var trackCount: Int](/documentation/musickit/libraryalbumsortproperties/trackcount)
- [LibraryArtistFilter](/documentation/musickit/libraryartistfilter)

### Instance Properties

- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/libraryartistfilter/genres)
- [var id: MusicItemID](/documentation/musickit/libraryartistfilter/id)
- [var name: String](/documentation/musickit/libraryartistfilter/name)
- [var playlists: MusicItemCollection<Playlist>?](/documentation/musickit/libraryartistfilter/playlists)
- [LibraryArtistSortProperties](/documentation/musickit/libraryartistsortproperties)

### Instance Properties

- [var albumCount: Int?](/documentation/musickit/libraryartistsortproperties/albumcount)
- [var libraryAddedDate: Date?](/documentation/musickit/libraryartistsortproperties/libraryaddeddate)
- [var name: String](/documentation/musickit/libraryartistsortproperties/name)
- [LibraryGenreFilter](/documentation/musickit/librarygenrefilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/librarygenrefilter/id)
- [var name: String](/documentation/musickit/librarygenrefilter/name)
- [LibraryGenreSortProperties](/documentation/musickit/librarygenresortproperties)

### Instance Properties

- [var libraryAddedDate: Date?](/documentation/musickit/librarygenresortproperties/libraryaddeddate)
- [var name: String](/documentation/musickit/librarygenresortproperties/name)
- [LibraryMusicVideoFilter](/documentation/musickit/librarymusicvideofilter)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/librarymusicvideofilter/albumtitle)
- [var albums: MusicItemCollection<Album>?](/documentation/musickit/librarymusicvideofilter/albums)
- [var artistName: String?](/documentation/musickit/librarymusicvideofilter/artistname)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/librarymusicvideofilter/artists)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/librarymusicvideofilter/genres)
- [var id: MusicItemID](/documentation/musickit/librarymusicvideofilter/id)
- [var title: String](/documentation/musickit/librarymusicvideofilter/title)
- [LibraryMusicVideoSortProperties](/documentation/musickit/librarymusicvideosortproperties)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/librarymusicvideosortproperties/albumtitle)
- [var artistName: String?](/documentation/musickit/librarymusicvideosortproperties/artistname)
- [var duration: TimeInterval?](/documentation/musickit/librarymusicvideosortproperties/duration)
- [var lastPlayedDate: Date?](/documentation/musickit/librarymusicvideosortproperties/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/librarymusicvideosortproperties/libraryaddeddate)
- [var playCount: Int?](/documentation/musickit/librarymusicvideosortproperties/playcount)
- [var title: String](/documentation/musickit/librarymusicvideosortproperties/title)
- [var trackNumber: Int?](/documentation/musickit/librarymusicvideosortproperties/tracknumber)
- [LibraryPlaylistEntryFilter](/documentation/musickit/libraryplaylistentryfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/libraryplaylistentryfilter/id)
- [LibraryPlaylistEntrySortProperties](/documentation/musickit/libraryplaylistentrysortproperties)
- [LibraryPlaylistFilter](/documentation/musickit/libraryplaylistfilter)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/libraryplaylistfilter/id)
- [var name: String](/documentation/musickit/libraryplaylistfilter/name)
- [LibraryPlaylistSortProperties](/documentation/musickit/libraryplaylistsortproperties)

### Instance Properties

- [var lastPlayedDate: Date?](/documentation/musickit/libraryplaylistsortproperties/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/libraryplaylistsortproperties/libraryaddeddate)
- [var name: String](/documentation/musickit/libraryplaylistsortproperties/name)
- [LibrarySongFilter](/documentation/musickit/librarysongfilter)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/librarysongfilter/albumtitle)
- [var albums: MusicItemCollection<Album>?](/documentation/musickit/librarysongfilter/albums)
- [var artistName: String?](/documentation/musickit/librarysongfilter/artistname)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/librarysongfilter/artists)
- [var composerName: String?](/documentation/musickit/librarysongfilter/composername)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/librarysongfilter/genres)
- [var id: MusicItemID](/documentation/musickit/librarysongfilter/id)
- [var title: String](/documentation/musickit/librarysongfilter/title)
- [LibrarySongSortProperties](/documentation/musickit/librarysongsortproperties)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/librarysongsortproperties/albumtitle)
- [var artistName: String?](/documentation/musickit/librarysongsortproperties/artistname)
- [var composerName: String?](/documentation/musickit/librarysongsortproperties/composername)
- [var discNumber: Int?](/documentation/musickit/librarysongsortproperties/discnumber)
- [var duration: TimeInterval?](/documentation/musickit/librarysongsortproperties/duration)
- [var lastPlayedDate: Date?](/documentation/musickit/librarysongsortproperties/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/librarysongsortproperties/libraryaddeddate)
- [var playCount: Int?](/documentation/musickit/librarysongsortproperties/playcount)
- [var title: String](/documentation/musickit/librarysongsortproperties/title)
- [var trackNumber: Int?](/documentation/musickit/librarysongsortproperties/tracknumber)
- [LibraryTrackFilter](/documentation/musickit/librarytrackfilter)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/librarytrackfilter/albumtitle)
- [var albums: MusicItemCollection<Album>?](/documentation/musickit/librarytrackfilter/albums)
- [var artistName: String?](/documentation/musickit/librarytrackfilter/artistname)
- [var artists: MusicItemCollection<Artist>?](/documentation/musickit/librarytrackfilter/artists)
- [var genres: MusicItemCollection<Genre>?](/documentation/musickit/librarytrackfilter/genres)
- [var id: MusicItemID](/documentation/musickit/librarytrackfilter/id)
- [var title: String](/documentation/musickit/librarytrackfilter/title)
- [LibraryTrackSortProperties](/documentation/musickit/librarytracksortproperties)

### Instance Properties

- [var albumTitle: String?](/documentation/musickit/librarytracksortproperties/albumtitle)
- [var artistName: String?](/documentation/musickit/librarytracksortproperties/artistname)
- [var discNumber: Int?](/documentation/musickit/librarytracksortproperties/discnumber)
- [var duration: TimeInterval?](/documentation/musickit/librarytracksortproperties/duration)
- [var lastPlayedDate: Date?](/documentation/musickit/librarytracksortproperties/lastplayeddate)
- [var libraryAddedDate: Date?](/documentation/musickit/librarytracksortproperties/libraryaddeddate)
- [var playCount: Int?](/documentation/musickit/librarytracksortproperties/playcount)
- [var title: String](/documentation/musickit/librarytracksortproperties/title)
- [var trackNumber: Int?](/documentation/musickit/librarytracksortproperties/tracknumber)
- [MusicCatalogChartRequestable](/documentation/musickit/musiccatalogchartrequestable)
- [MusicCatalogTopLevelResourceRequesting](/documentation/musickit/musiccatalogtoplevelresourcerequesting)
- [MusicLibraryAddable](/documentation/musickit/musiclibraryaddable)
- [MusicLibraryRequestFilterValueEquatable](/documentation/musickit/musiclibraryrequestfiltervalueequatable)
- [MusicLibraryRequestFilterValueMembershipComparable](/documentation/musickit/musiclibraryrequestfiltervaluemembershipcomparable)
- [MusicLibraryRequestable](/documentation/musickit/musiclibraryrequestable)

### Associated Types

- [LibraryFilter](/documentation/musickit/musiclibraryrequestable/libraryfilter)
- [LibrarySortProperties](/documentation/musickit/musiclibraryrequestable/librarysortproperties)
- [MusicLibrarySearchable](/documentation/musickit/musiclibrarysearchable)
- [MusicLibrarySectionRequestable](/documentation/musickit/musiclibrarysectionrequestable)
- [MusicPersonalRecommendationItem](/documentation/musickit/musicpersonalrecommendationitem)
- [MusicPlaylistAddable](/documentation/musickit/musicplaylistaddable)
- [MusicRecentlyPlayedRequestable](/documentation/musickit/musicrecentlyplayedrequestable)

## Structures

- [MusicCatalogChart](/documentation/musickit/musiccatalogchart)

### Instance Properties

- [let id: String](/documentation/musickit/musiccatalogchart/id)
- [let items: MusicItemCollection<MusicItemType>](/documentation/musickit/musiccatalogchart/items)
- [let kind: MusicCatalogChartKind](/documentation/musickit/musiccatalogchart/kind)
- [let title: String](/documentation/musickit/musiccatalogchart/title)
- [MusicCatalogChartsRequest](/documentation/musickit/musiccatalogchartsrequest)

### Initializers

- [init(genre: Genre?, kinds: [MusicCatalogChartKind], types: [any MusicCatalogChartRequestable.Type])](/documentation/musickit/musiccatalogchartsrequest/init(genre:kinds:types:))

### Instance Properties

- [var genre: Genre?](/documentation/musickit/musiccatalogchartsrequest/genre)
- [var kinds: [MusicCatalogChartKind]](/documentation/musickit/musiccatalogchartsrequest/kinds)
- [var limit: Int?](/documentation/musickit/musiccatalogchartsrequest/limit)
- [var offset: Int?](/documentation/musickit/musiccatalogchartsrequest/offset)
- [var types: [any MusicCatalogChartRequestable.Type]](/documentation/musickit/musiccatalogchartsrequest/types)

### Instance Methods

- [func response() async throws -> MusicCatalogChartsResponse](/documentation/musickit/musiccatalogchartsrequest/response())
- [MusicCatalogChartsResponse](/documentation/musickit/musiccatalogchartsresponse)

### Instance Properties

- [let albumCharts: [MusicCatalogChart<Album>]](/documentation/musickit/musiccatalogchartsresponse/albumcharts)
- [let musicVideoCharts: [MusicCatalogChart<MusicVideo>]](/documentation/musickit/musiccatalogchartsresponse/musicvideocharts)
- [let playlistCharts: [MusicCatalogChart<Playlist>]](/documentation/musickit/musiccatalogchartsresponse/playlistcharts)
- [let songCharts: [MusicCatalogChart<Song>]](/documentation/musickit/musiccatalogchartsresponse/songcharts)
- [MusicCatalogSearchSuggestionsRequest](/documentation/musickit/musiccatalogsearchsuggestionsrequest)

### Initializers

- [init(term: String, includingTopResultsOfTypes: [any MusicCatalogSearchable.Type])](/documentation/musickit/musiccatalogsearchsuggestionsrequest/init(term:includingtopresultsoftypes:))

### Instance Properties

- [var limit: Int?](/documentation/musickit/musiccatalogsearchsuggestionsrequest/limit)
- [let term: String](/documentation/musickit/musiccatalogsearchsuggestionsrequest/term)
- [var typesForTopResults: [any MusicCatalogSearchable.Type]](/documentation/musickit/musiccatalogsearchsuggestionsrequest/typesfortopresults)

### Instance Methods

- [func response() async throws -> MusicCatalogSearchSuggestionsResponse](/documentation/musickit/musiccatalogsearchsuggestionsrequest/response())
- [MusicCatalogSearchSuggestionsResponse](/documentation/musickit/musiccatalogsearchsuggestionsresponse)

### Structures

- [MusicCatalogSearchSuggestionsResponse.Suggestion](/documentation/musickit/musiccatalogsearchsuggestionsresponse/suggestion)

#### Instance Properties

- [let displayTerm: String](/documentation/musickit/musiccatalogsearchsuggestionsresponse/suggestion/displayterm)
- [var id: String](/documentation/musickit/musiccatalogsearchsuggestionsresponse/suggestion/id)
- [let searchTerm: String](/documentation/musickit/musiccatalogsearchsuggestionsresponse/suggestion/searchterm)

### Instance Properties

- [let suggestions: [MusicCatalogSearchSuggestionsResponse.Suggestion]](/documentation/musickit/musiccatalogsearchsuggestionsresponse/suggestions)
- [let topResults: MusicItemCollection<MusicCatalogSearchSuggestionsResponse.TopResult>](/documentation/musickit/musiccatalogsearchsuggestionsresponse/topresults)

### Type Aliases

- [MusicCatalogSearchSuggestionsResponse.TopResult](/documentation/musickit/musiccatalogsearchsuggestionsresponse/topresult)
- [MusicLibraryRequest](/documentation/musickit/musiclibraryrequest)

### Initializers

- [init()](/documentation/musickit/musiclibraryrequest/init())

### Instance Properties

- [var includeOnlyDownloadedContent: Bool](/documentation/musickit/musiclibraryrequest/includeonlydownloadedcontent)
- [var limit: Int](/documentation/musickit/musiclibraryrequest/limit)
- [var offset: Int](/documentation/musickit/musiclibraryrequest/offset)

### Instance Methods

- [func filter(matching: KeyPath<MusicItemType.LibraryFilter, String?>, contains: String)](/documentation/musickit/musiclibraryrequest/filter(matching:contains:)-4q231)
- [func filter(matching: KeyPath<MusicItemType.LibraryFilter, String>, contains: String)](/documentation/musickit/musiclibraryrequest/filter(matching:contains:)-8wwn3)
- [func filter<RelatedMusicItemType>(matching: KeyPath<MusicItemType.LibraryFilter, MusicItemCollection<RelatedMusicItemType>?>, contains: RelatedMusicItemType)](/documentation/musickit/musiclibraryrequest/filter(matching:contains:)-9756l)
- [func filter<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value>, equalTo: Value)](/documentation/musickit/musiclibraryrequest/filter(matching:equalto:)-5jgfj)
- [func filter<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value?>, equalTo: Value?)](/documentation/musickit/musiclibraryrequest/filter(matching:equalto:)-8efya)
- [func filter<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value?>, memberOf: [Value?])](/documentation/musickit/musiclibraryrequest/filter(matching:memberof:)-2u2ia)
- [func filter<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value>, memberOf: [Value])](/documentation/musickit/musiclibraryrequest/filter(matching:memberof:)-3e2ab)
- [func filter(text: String)](/documentation/musickit/musiclibraryrequest/filter(text:))
- [func response() async throws -> MusicLibraryResponse<MusicItemType>](/documentation/musickit/musiclibraryrequest/response())
- [func sort<Value>(by: KeyPath<MusicItemType.LibrarySortProperties, Value>, ascending: Bool)](/documentation/musickit/musiclibraryrequest/sort(by:ascending:))
- [MusicLibraryResponse](/documentation/musickit/musiclibraryresponse)

### Instance Properties

- [let items: MusicItemCollection<MusicItemType>](/documentation/musickit/musiclibraryresponse/items)
- [MusicLibrarySearchRequest](/documentation/musickit/musiclibrarysearchrequest)

### Initializers

- [init(term: String, types: [any MusicLibrarySearchable.Type])](/documentation/musickit/musiclibrarysearchrequest/init(term:types:))

### Instance Properties

- [var includeTopResults: Bool](/documentation/musickit/musiclibrarysearchrequest/includetopresults)
- [var limit: Int](/documentation/musickit/musiclibrarysearchrequest/limit)
- [let term: String](/documentation/musickit/musiclibrarysearchrequest/term)
- [var types: [any MusicLibrarySearchable.Type]](/documentation/musickit/musiclibrarysearchrequest/types)

### Instance Methods

- [func response() async throws -> MusicLibrarySearchResponse](/documentation/musickit/musiclibrarysearchrequest/response())
- [MusicLibrarySearchResponse](/documentation/musickit/musiclibrarysearchresponse)

### Instance Properties

- [let albums: MusicItemCollection<Album>](/documentation/musickit/musiclibrarysearchresponse/albums)
- [let artists: MusicItemCollection<Artist>](/documentation/musickit/musiclibrarysearchresponse/artists)
- [let musicVideos: MusicItemCollection<MusicVideo>](/documentation/musickit/musiclibrarysearchresponse/musicvideos)
- [let playlists: MusicItemCollection<Playlist>](/documentation/musickit/musiclibrarysearchresponse/playlists)
- [let songs: MusicItemCollection<Song>](/documentation/musickit/musiclibrarysearchresponse/songs)
- [let topResults: MusicItemCollection<MusicLibrarySearchResponse.TopResult>](/documentation/musickit/musiclibrarysearchresponse/topresults)

### Enumerations

- [MusicLibrarySearchResponse.TopResult](/documentation/musickit/musiclibrarysearchresponse/topresult)

#### Enumeration Cases

- [case album(Album)](/documentation/musickit/musiclibrarysearchresponse/topresult/album(_:))
- [case artist(Artist)](/documentation/musickit/musiclibrarysearchresponse/topresult/artist(_:))
- [case musicVideo(MusicVideo)](/documentation/musickit/musiclibrarysearchresponse/topresult/musicvideo(_:))
- [case playlist(Playlist)](/documentation/musickit/musiclibrarysearchresponse/topresult/playlist(_:))
- [case song(Song)](/documentation/musickit/musiclibrarysearchresponse/topresult/song(_:))

#### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/musiclibrarysearchresponse/topresult/artwork)
- [var id: MusicItemID](/documentation/musickit/musiclibrarysearchresponse/topresult/id)
- [var title: String](/documentation/musickit/musiclibrarysearchresponse/topresult/title)
- [MusicLibrarySection](/documentation/musickit/musiclibrarysection)

### Instance Properties

- [let items: MusicItemCollection<MusicItemType>](/documentation/musickit/musiclibrarysection/items)

### Subscripts

- [subscript<T>(dynamicMember _: KeyPath<SectionType, T>) -> T](/documentation/musickit/musiclibrarysection/subscript(dynamicmember:))
- [MusicLibrarySectionedRequest](/documentation/musickit/musiclibrarysectionedrequest)

### Initializers

- [init()](/documentation/musickit/musiclibrarysectionedrequest/init())

### Instance Properties

- [var includeOnlyDownloadedContent: Bool](/documentation/musickit/musiclibrarysectionedrequest/includeonlydownloadedcontent)
- [var limit: Int](/documentation/musickit/musiclibrarysectionedrequest/limit)
- [var offset: Int](/documentation/musickit/musiclibrarysectionedrequest/offset)

### Instance Methods

- [func filterItems<RelatedMusicItemType>(matching: KeyPath<MusicItemType.LibraryFilter, MusicItemCollection<RelatedMusicItemType>?>, contains: RelatedMusicItemType)](/documentation/musickit/musiclibrarysectionedrequest/filteritems(matching:contains:)-3s88f)
- [func filterItems(matching: KeyPath<MusicItemType.LibraryFilter, String>, contains: String)](/documentation/musickit/musiclibrarysectionedrequest/filteritems(matching:contains:)-8rbsc)
- [func filterItems(matching: KeyPath<MusicItemType.LibraryFilter, String?>, contains: String)](/documentation/musickit/musiclibrarysectionedrequest/filteritems(matching:contains:)-9hpfh)
- [func filterItems<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value>, equalTo: Value)](/documentation/musickit/musiclibrarysectionedrequest/filteritems(matching:equalto:)-3zn4r)
- [func filterItems<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value?>, equalTo: Value?)](/documentation/musickit/musiclibrarysectionedrequest/filteritems(matching:equalto:)-5ybaa)
- [func filterItems<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value>, memberOf: [Value])](/documentation/musickit/musiclibrarysectionedrequest/filteritems(matching:memberof:)-49h2x)
- [func filterItems<Value>(matching: KeyPath<MusicItemType.LibraryFilter, Value?>, memberOf: [Value?])](/documentation/musickit/musiclibrarysectionedrequest/filteritems(matching:memberof:)-zmb0)
- [func filterItems(text: String)](/documentation/musickit/musiclibrarysectionedrequest/filteritems(text:))
- [func filterSections(matching: KeyPath<SectionType.LibraryFilter, String?>, contains: String)](/documentation/musickit/musiclibrarysectionedrequest/filtersections(matching:contains:)-3jf7b)
- [func filterSections(matching: KeyPath<SectionType.LibraryFilter, String>, contains: String)](/documentation/musickit/musiclibrarysectionedrequest/filtersections(matching:contains:)-5ptoy)
- [func filterSections<Value>(matching: KeyPath<SectionType.LibraryFilter, Value?>, equalTo: Value?)](/documentation/musickit/musiclibrarysectionedrequest/filtersections(matching:equalto:)-5nop7)
- [func filterSections<Value>(matching: KeyPath<SectionType.LibraryFilter, Value>, equalTo: Value)](/documentation/musickit/musiclibrarysectionedrequest/filtersections(matching:equalto:)-7v8tr)
- [func filterSections<Value>(matching: KeyPath<SectionType.LibraryFilter, Value>, memberOf: [Value])](/documentation/musickit/musiclibrarysectionedrequest/filtersections(matching:memberof:)-4l0z8)
- [func filterSections<Value>(matching: KeyPath<SectionType.LibraryFilter, Value?>, memberOf: [Value?])](/documentation/musickit/musiclibrarysectionedrequest/filtersections(matching:memberof:)-746mb)
- [func filterSections(text: String)](/documentation/musickit/musiclibrarysectionedrequest/filtersections(text:))
- [func response() async throws -> MusicLibrarySectionedResponse<SectionType, MusicItemType>](/documentation/musickit/musiclibrarysectionedrequest/response())
- [func sortItems<Value>(by: KeyPath<MusicItemType.LibrarySortProperties, Value>, ascending: Bool)](/documentation/musickit/musiclibrarysectionedrequest/sortitems(by:ascending:))
- [func sortSections<Value>(by: KeyPath<SectionType.LibrarySortProperties, Value>, ascending: Bool)](/documentation/musickit/musiclibrarysectionedrequest/sortsections(by:ascending:))
- [MusicLibrarySectionedResponse](/documentation/musickit/musiclibrarysectionedresponse)

### Instance Properties

- [let sections: [MusicLibrarySection<SectionType, MusicItemType>]](/documentation/musickit/musiclibrarysectionedresponse/sections)
- [MusicPersonalRecommendation](/documentation/musickit/musicpersonalrecommendation)

### Instance Properties

- [var albums: MusicItemCollection<Album>](/documentation/musickit/musicpersonalrecommendation/albums)
- [let id: MusicItemID](/documentation/musickit/musicpersonalrecommendation/id)
- [var items: MusicItemCollection<MusicPersonalRecommendation.Item>](/documentation/musickit/musicpersonalrecommendation/items)
- [let nextRefreshDate: Date?](/documentation/musickit/musicpersonalrecommendation/nextrefreshdate)
- [var playlists: MusicItemCollection<Playlist>](/documentation/musickit/musicpersonalrecommendation/playlists)
- [let reason: String?](/documentation/musickit/musicpersonalrecommendation/reason)
- [var stations: MusicItemCollection<Station>](/documentation/musickit/musicpersonalrecommendation/stations)
- [let title: String?](/documentation/musickit/musicpersonalrecommendation/title)
- [var types: [any MusicPersonalRecommendationItem.Type]](/documentation/musickit/musicpersonalrecommendation/types)

### Enumerations

- [MusicPersonalRecommendation.Item](/documentation/musickit/musicpersonalrecommendation/item)

#### Enumeration Cases

- [case album(Album)](/documentation/musickit/musicpersonalrecommendation/item/album(_:))
- [case playlist(Playlist)](/documentation/musickit/musicpersonalrecommendation/item/playlist(_:))
- [case station(Station)](/documentation/musickit/musicpersonalrecommendation/item/station(_:))

#### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/musicpersonalrecommendation/item/artwork)
- [var id: MusicItemID](/documentation/musickit/musicpersonalrecommendation/item/id)
- [var subtitle: String?](/documentation/musickit/musicpersonalrecommendation/item/subtitle)
- [var title: String](/documentation/musickit/musicpersonalrecommendation/item/title)
- [MusicPersonalRecommendationsRequest](/documentation/musickit/musicpersonalrecommendationsrequest)

### Initializers

- [init()](/documentation/musickit/musicpersonalrecommendationsrequest/init())
- [init<S>(refreshing: S)](/documentation/musickit/musicpersonalrecommendationsrequest/init(refreshing:))

### Instance Properties

- [var limit: Int?](/documentation/musickit/musicpersonalrecommendationsrequest/limit)
- [var offset: Int?](/documentation/musickit/musicpersonalrecommendationsrequest/offset)

### Instance Methods

- [func response() async throws -> MusicPersonalRecommendationsResponse](/documentation/musickit/musicpersonalrecommendationsrequest/response())
- [MusicPersonalRecommendationsResponse](/documentation/musickit/musicpersonalrecommendationsresponse)

### Instance Properties

- [let recommendations: MusicItemCollection<MusicPersonalRecommendation>](/documentation/musickit/musicpersonalrecommendationsresponse/recommendations)
- [MusicRecentlyPlayedRequest](/documentation/musickit/musicrecentlyplayedrequest)

### Initializers

- [init()](/documentation/musickit/musicrecentlyplayedrequest/init())

### Instance Properties

- [var limit: Int?](/documentation/musickit/musicrecentlyplayedrequest/limit)
- [var offset: Int?](/documentation/musickit/musicrecentlyplayedrequest/offset)

### Instance Methods

- [func response() async throws -> MusicRecentlyPlayedResponse<MusicItemType>](/documentation/musickit/musicrecentlyplayedrequest/response())
- [MusicRecentlyPlayedResponse](/documentation/musickit/musicrecentlyplayedresponse)

### Instance Properties

- [let items: MusicItemCollection<MusicItemType>](/documentation/musickit/musicrecentlyplayedresponse/items)
- [TitledSection](/documentation/musickit/titledsection)

### Instance Properties

- [var id: MusicItemID](/documentation/musickit/titledsection/id)
- [let title: String](/documentation/musickit/titledsection/title)

## Type Aliases

- [MusicRecentlyPlayedContainerRequest](/documentation/musickit/musicrecentlyplayedcontainerrequest)
- [MusicRecentlyPlayedContainerResponse](/documentation/musickit/musicrecentlyplayedcontainerresponse)

## Enumerations

- [AudioVariant](/documentation/musickit/audiovariant)

### Enumeration Cases

- [case dolbyAtmos](/documentation/musickit/audiovariant/dolbyatmos)
- [case dolbyAudio](/documentation/musickit/audiovariant/dolbyaudio)
- [case highResolutionLossless](/documentation/musickit/audiovariant/highresolutionlossless)
- [case lossless](/documentation/musickit/audiovariant/lossless)
- [case lossyStereo](/documentation/musickit/audiovariant/lossystereo)
- [case spatialAudio](/documentation/musickit/audiovariant/spatialaudio)
- [MusicCatalogChartKind](/documentation/musickit/musiccatalogchartkind)

### Enumeration Cases

- [case cityTop](/documentation/musickit/musiccatalogchartkind/citytop)
- [case dailyGlobalTop](/documentation/musickit/musiccatalogchartkind/dailyglobaltop)
- [case mostPlayed](/documentation/musickit/musiccatalogchartkind/mostplayed)
- [MusicPropertySource](/documentation/musickit/musicpropertysource)

### Enumeration Cases

- [case catalog](/documentation/musickit/musicpropertysource/catalog)
- [case library](/documentation/musickit/musicpropertysource/library)
- [RecentlyPlayedMusicItem](/documentation/musickit/recentlyplayedmusicitem)

### Enumeration Cases

- [case album(Album)](/documentation/musickit/recentlyplayedmusicitem/album(_:))
- [case playlist(Playlist)](/documentation/musickit/recentlyplayedmusicitem/playlist(_:))
- [case station(Station)](/documentation/musickit/recentlyplayedmusicitem/station(_:))

### Instance Properties

- [var artwork: Artwork?](/documentation/musickit/recentlyplayedmusicitem/artwork)
- [var id: MusicItemID](/documentation/musickit/recentlyplayedmusicitem/id)
- [var playParameters: PlayParameters?](/documentation/musickit/recentlyplayedmusicitem/playparameters)
- [var subtitle: String?](/documentation/musickit/recentlyplayedmusicitem/subtitle)
- [var title: String](/documentation/musickit/recentlyplayedmusicitem/title)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
