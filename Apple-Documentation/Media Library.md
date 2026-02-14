# Media Library Documentation

Source: https://sosumi.ai/documentation/medialibrary

---
title: Media Library
source: https://developer.apple.com/documentation/medialibrary
timestamp: 2026-02-13T18:59:22.941Z
---

## Classes

- [MLMediaGroup](/documentation/medialibrary/mlmediagroup)

### Identifying the Group

- [var identifier: String](/documentation/medialibrary/mlmediagroup/identifier)
- [var typeIdentifier: String](/documentation/medialibrary/mlmediagroup/typeidentifier)
- [var mediaSourceIdentifier: String](/documentation/medialibrary/mlmediagroup/mediasourceidentifier)
- [var mediaLibrary: MLMediaLibrary?](/documentation/medialibrary/mlmediagroup/medialibrary)

### Accessing Group Attributes

- [var attributes: [String : Any]](/documentation/medialibrary/mlmediagroup/attributes)
- [var name: String?](/documentation/medialibrary/mlmediagroup/name)
- [var iconImage: NSImage?](/documentation/medialibrary/mlmediagroup/iconimage)
- [var url: URL?](/documentation/medialibrary/mlmediagroup/url)
- [var modificationDate: Date?](/documentation/medialibrary/mlmediagroup/modificationdate)

### Accessing the Group Hierarchy

- [var parent: MLMediaGroup?](/documentation/medialibrary/mlmediagroup/parent)
- [var childGroups: [MLMediaGroup]?](/documentation/medialibrary/mlmediagroup/childgroups)
- [var mediaObjects: [MLMediaObject]?](/documentation/medialibrary/mlmediagroup/mediaobjects)
- [MLMediaLibrary](/documentation/medialibrary/mlmedialibrary)

### Initializing the Library

- [init(options: [String : Any])](/documentation/medialibrary/mlmedialibrary/init(options:))

### Accessing Media Sources

- [var mediaSources: [String : MLMediaSource]?](/documentation/medialibrary/mlmedialibrary/mediasources)

### Constants

- [Load Options Keys](/documentation/medialibrary/load-options-keys)

#### Constants

- [let MLMediaLoadSourceTypesKey: String](/documentation/medialibrary/mlmedialoadsourcetypeskey)
- [let MLMediaLoadIncludeSourcesKey: String](/documentation/medialibrary/mlmedialoadincludesourceskey)
- [let MLMediaLoadExcludeSourcesKey: String](/documentation/medialibrary/mlmedialoadexcludesourceskey)
- [let MLMediaLoadFoldersKey: String](/documentation/medialibrary/mlmedialoadfolderskey)
- [let MLMediaLoadAppFoldersKey: String](/documentation/medialibrary/mlmedialoadappfolderskey)
- [Media Source Identifiers](/documentation/medialibrary/media-source-identifiers)

#### Constants

- [let MLMediaSourceiPhotoIdentifier: String](/documentation/medialibrary/mlmediasourceiphotoidentifier)
- [let MLMediaSourceiTunesIdentifier: String](/documentation/medialibrary/mlmediasourceitunesidentifier)
- [let MLMediaSourceApertureIdentifier: String](/documentation/medialibrary/mlmediasourceapertureidentifier)
- [let MLMediaSourceiMovieIdentifier: String](/documentation/medialibrary/mlmediasourceimovieidentifier)
- [let MLMediaSourceFinalCutIdentifier: String](/documentation/medialibrary/mlmediasourcefinalcutidentifier)
- [let MLMediaSourceGarageBandIdentifier: String](/documentation/medialibrary/mlmediasourcegaragebandidentifier)
- [let MLMediaSourceLogicIdentifier: String](/documentation/medialibrary/mlmediasourcelogicidentifier)
- [let MLMediaSourcePhotoBoothIdentifier: String](/documentation/medialibrary/mlmediasourcephotoboothidentifier)
- [Non-App-Specific Media Source Identifiers](/documentation/medialibrary/non-app-specific-media-source-identifiers)

#### Constants

- [let MLMediaSourceMoviesFolderIdentifier: String](/documentation/medialibrary/mlmediasourcemoviesfolderidentifier)
- [let MLMediaSourceCustomFoldersIdentifier: String](/documentation/medialibrary/mlmediasourcecustomfoldersidentifier)
- [let MLMediaSourceAppDefinedFoldersIdentifier: String](/documentation/medialibrary/mlmediasourceappdefinedfoldersidentifier)
- [Well-Known Folder Identifiers](/documentation/medialibrary/well-known-folder-identifiers)

#### Constants

- [let MLMediaLoadAppleLoops: String](/documentation/medialibrary/mlmedialoadappleloops)
- [let MLMediaLoadMoviesFolder: String](/documentation/medialibrary/mlmedialoadmoviesfolder)
- [MLMediaObject](/documentation/medialibrary/mlmediaobject)

### Identifying the Object

- [var identifier: String](/documentation/medialibrary/mlmediaobject/identifier)
- [var mediaSourceIdentifier: String](/documentation/medialibrary/mlmediaobject/mediasourceidentifier)
- [var mediaLibrary: MLMediaLibrary?](/documentation/medialibrary/mlmediaobject/medialibrary)

### Accessing Object Attributes

- [var attributes: [String : Any]](/documentation/medialibrary/mlmediaobject/attributes)
- [var mediaType: MLMediaType](/documentation/medialibrary/mlmediaobject/mediatype)
- [var contentType: String?](/documentation/medialibrary/mlmediaobject/contenttype)
- [var name: String?](/documentation/medialibrary/mlmediaobject/name)
- [var url: URL?](/documentation/medialibrary/mlmediaobject/url)
- [var originalURL: URL?](/documentation/medialibrary/mlmediaobject/originalurl)
- [var fileSize: Int](/documentation/medialibrary/mlmediaobject/filesize)
- [var modificationDate: Date?](/documentation/medialibrary/mlmediaobject/modificationdate)
- [var thumbnailURL: URL?](/documentation/medialibrary/mlmediaobject/thumbnailurl)
- [var artworkImage: NSImage?](/documentation/medialibrary/mlmediaobject/artworkimage)
- [MLMediaSource](/documentation/medialibrary/mlmediasource)

### Identifying the Source

- [var mediaSourceIdentifier: String](/documentation/medialibrary/mlmediasource/mediasourceidentifier)
- [var mediaLibrary: MLMediaLibrary?](/documentation/medialibrary/mlmediasource/medialibrary)

### Accessing Source Attributes

- [var attributes: [String : Any]](/documentation/medialibrary/mlmediasource/attributes)

### Accessing the Root Media Group

- [var rootMediaGroup: MLMediaGroup?](/documentation/medialibrary/mlmediasource/rootmediagroup)

### Accessing Media

- [func mediaGroup(forIdentifier: String) -> MLMediaGroup?](/documentation/medialibrary/mlmediasource/mediagroup(foridentifier:))
- [func mediaGroups(forIdentifiers: [String]) -> [String : MLMediaGroup]](/documentation/medialibrary/mlmediasource/mediagroups(foridentifiers:))
- [func mediaObject(forIdentifier: String) -> MLMediaObject?](/documentation/medialibrary/mlmediasource/mediaobject(foridentifier:))
- [func mediaObjects(forIdentifiers: [String]) -> [String : MLMediaObject]](/documentation/medialibrary/mlmediasource/mediaobjects(foridentifiers:))

## Reference

- [MediaLibrary Constants](/documentation/medialibrary/medialibrary-constants)

### Constants

- [Aperture Media Group Type Identifiers](/documentation/medialibrary/aperture-media-group-type-identifiers)

#### Constants

- [let MLApertureRootGroupTypeIdentifier: String](/documentation/medialibrary/mlaperturerootgrouptypeidentifier)
- [let MLApertureUserAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureuseralbumtypeidentifier)
- [let MLApertureUserSmartAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureusersmartalbumtypeidentifier)
- [let MLApertureProjectAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureprojectalbumtypeidentifier)
- [let MLApertureFolderAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturefolderalbumtypeidentifier)
- [let MLApertureProjectFolderAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureprojectfolderalbumtypeidentifier)
- [let MLApertureAllProjectsTypeIdentifier: String](/documentation/medialibrary/mlapertureallprojectstypeidentifier)
- [let MLApertureAllPhotosTypeIdentifier: String](/documentation/medialibrary/mlapertureallphotostypeidentifier)
- [let MLApertureLastViewedEventAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturelastviewedeventalbumtypeidentifier)
- [let MLApertureLastImportAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturelastimportalbumtypeidentifier)
- [let MLApertureLastNMonthsAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturelastnmonthsalbumtypeidentifier)
- [let MLApertureFlaggedTypeIdentifier: String](/documentation/medialibrary/mlapertureflaggedtypeidentifier)
- [let MLApertureLightTableTypeIdentifier: String](/documentation/medialibrary/mlaperturelighttabletypeidentifier)
- [let MLApertureSlideShowTypeIdentifier: String](/documentation/medialibrary/mlapertureslideshowtypeidentifier)
- [let MLAperturePhotoStreamAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturephotostreamalbumtypeidentifier)
- [let MLApertureFacesAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturefacesalbumtypeidentifier)
- [let MLAperturePlacesAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureplacesalbumtypeidentifier)
- [let MLAperturePlacesCountryAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureplacescountryalbumtypeidentifier)
- [let MLAperturePlacesProvinceAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureplacesprovincealbumtypeidentifier)
- [let MLAperturePlacesCityAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureplacescityalbumtypeidentifier)
- [let MLAperturePlacesPointOfInterestAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureplacespointofinterestalbumtypeidentifier)
- [let MLApertureFacebookAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturefacebookalbumtypeidentifier)
- [let MLApertureFacebookGroupTypeIdentifier: String](/documentation/medialibrary/mlaperturefacebookgrouptypeidentifier)
- [let MLApertureFlickrAlbumTypeIdentifier: String](/documentation/medialibrary/mlapertureflickralbumtypeidentifier)
- [let MLApertureFlickrGroupTypeIdentifier: String](/documentation/medialibrary/mlapertureflickrgrouptypeidentifier)
- [let MLApertureSmugMugAlbumTypeIdentifier: String](/documentation/medialibrary/mlaperturesmugmugalbumtypeidentifier)
- [let MLApertureSmugMugGroupTypeIdentifier: String](/documentation/medialibrary/mlaperturesmugmuggrouptypeidentifier)
- [Final Cut Pro Media Group Type Identifiers](/documentation/medialibrary/final-cut-pro-media-group-type-identifiers)

#### Constants

- [let MLFinalCutRootGroupTypeIdentifier: String](/documentation/medialibrary/mlfinalcutrootgrouptypeidentifier)
- [let MLFinalCutProjectGroupTypeIdentifier: String](/documentation/medialibrary/mlfinalcutprojectgrouptypeidentifier)
- [let MLFinalCutFolderGroupTypeIdentifier: String](/documentation/medialibrary/mlfinalcutfoldergrouptypeidentifier)
- [let MLFinalCutEventGroupTypeIdentifier: String](/documentation/medialibrary/mlfinalcuteventgrouptypeidentifier)
- [let MLFinalCutEventCalendarGroupTypeIdentifier: String](/documentation/medialibrary/mlfinalcuteventcalendargrouptypeidentifier)
- [let MLFinalCutEventLibraryGroupTypeIdentifier: String](/documentation/medialibrary/mlfinalcuteventlibrarygrouptypeidentifier)
- [Folders Media Group Type Identifiers](/documentation/medialibrary/folders-media-group-type-identifiers)

#### Constants

- [let MLFolderRootGroupTypeIdentifier: String](/documentation/medialibrary/mlfolderrootgrouptypeidentifier)
- [let MLFolderGroupTypeIdentifier: String](/documentation/medialibrary/mlfoldergrouptypeidentifier)
- [GarageBand Media Group Type Identifiers](/documentation/medialibrary/garageband-media-group-type-identifiers)

#### Constants

- [let MLGarageBandRootGroupTypeIdentifier: String](/documentation/medialibrary/mlgaragebandrootgrouptypeidentifier)
- [let MLGarageBandFolderGroupTypeIdentifier: String](/documentation/medialibrary/mlgaragebandfoldergrouptypeidentifier)
- [Logic Media Group Type Identifiers](/documentation/medialibrary/logic-media-group-type-identifiers)

#### Constants

- [let MLLogicRootGroupTypeIdentifier: String](/documentation/medialibrary/mllogicrootgrouptypeidentifier)
- [let MLLogicProjectTypeIdentifier: String](/documentation/medialibrary/mllogicprojecttypeidentifier)
- [let MLLogicProjectsGroupTypeIdentifier: String](/documentation/medialibrary/mllogicprojectsgrouptypeidentifier)
- [let MLLogicBouncesGroupTypeIdentifier: String](/documentation/medialibrary/mllogicbouncesgrouptypeidentifier)
- [let MLMediaLoadAppFoldersKey: String](/documentation/medialibrary/mlmedialoadappfolderskey)
- [let MLMediaLoadAppleLoops: String](/documentation/medialibrary/mlmedialoadappleloops)
- [let MLMediaLoadExcludeSourcesKey: String](/documentation/medialibrary/mlmedialoadexcludesourceskey)
- [let MLMediaLoadFoldersKey: String](/documentation/medialibrary/mlmedialoadfolderskey)
- [let MLMediaLoadIncludeSourcesKey: String](/documentation/medialibrary/mlmedialoadincludesourceskey)
- [let MLMediaLoadMoviesFolder: String](/documentation/medialibrary/mlmedialoadmoviesfolder)
- [let MLMediaLoadSourceTypesKey: String](/documentation/medialibrary/mlmedialoadsourcetypeskey)
- [let MLMediaSourceApertureIdentifier: String](/documentation/medialibrary/mlmediasourceapertureidentifier)
- [let MLMediaSourceAppDefinedFoldersIdentifier: String](/documentation/medialibrary/mlmediasourceappdefinedfoldersidentifier)
- [let MLMediaSourceCustomFoldersIdentifier: String](/documentation/medialibrary/mlmediasourcecustomfoldersidentifier)
- [let MLMediaSourceFinalCutIdentifier: String](/documentation/medialibrary/mlmediasourcefinalcutidentifier)
- [let MLMediaSourceGarageBandIdentifier: String](/documentation/medialibrary/mlmediasourcegaragebandidentifier)
- [let MLMediaSourceLogicIdentifier: String](/documentation/medialibrary/mlmediasourcelogicidentifier)
- [let MLMediaSourceMoviesFolderIdentifier: String](/documentation/medialibrary/mlmediasourcemoviesfolderidentifier)
- [let MLMediaSourcePhotoBoothIdentifier: String](/documentation/medialibrary/mlmediasourcephotoboothidentifier)
- [let MLMediaSourcePhotosIdentifier: String](/documentation/medialibrary/mlmediasourcephotosidentifier)
- [MLMediaSourceType](/documentation/medialibrary/mlmediasourcetype)

#### Constants

- [static var audio: MLMediaSourceType](/documentation/medialibrary/mlmediasourcetype/audio)
- [static var image: MLMediaSourceType](/documentation/medialibrary/mlmediasourcetype/image)
- [static var movie: MLMediaSourceType](/documentation/medialibrary/mlmediasourcetype/movie)

#### Initializers

- [init(rawValue: UInt)](/documentation/medialibrary/mlmediasourcetype/init(rawvalue:))
- [let MLMediaSourceiMovieIdentifier: String](/documentation/medialibrary/mlmediasourceimovieidentifier)
- [let MLMediaSourceiPhotoIdentifier: String](/documentation/medialibrary/mlmediasourceiphotoidentifier)
- [let MLMediaSourceiTunesIdentifier: String](/documentation/medialibrary/mlmediasourceitunesidentifier)
- [MLMediaType](/documentation/medialibrary/mlmediatype)

#### Constants

- [case audio](/documentation/medialibrary/mlmediatype/audio)
- [case image](/documentation/medialibrary/mlmediatype/image)
- [case movie](/documentation/medialibrary/mlmediatype/movie)

#### Initializers

- [init?(rawValue: UInt)](/documentation/medialibrary/mlmediatype/init(rawvalue:))
- [let MLPhotosAlbumTypeIdentifier: String](/documentation/medialibrary/mlphotosalbumtypeidentifier)
- [let MLPhotosAlbumsGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosalbumsgrouptypeidentifier)
- [let MLPhotosAllCollectionsGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosallcollectionsgrouptypeidentifier)
- [let MLPhotosAllMomentsGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosallmomentsgrouptypeidentifier)
- [let MLPhotosAllPhotosAlbumTypeIdentifier: String](/documentation/medialibrary/mlphotosallphotosalbumtypeidentifier)
- [let MLPhotosAllYearsGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosallyearsgrouptypeidentifier)
- [let MLPhotosBurstGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosburstgrouptypeidentifier)
- [let MLPhotosCollectionGroupTypeIdentifier: String](/documentation/medialibrary/mlphotoscollectiongrouptypeidentifier)
- [let MLPhotosDepthEffectGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosdeptheffectgrouptypeidentifier)
- [let MLPhotosFacesAlbumTypeIdentifier: String](/documentation/medialibrary/mlphotosfacesalbumtypeidentifier)
- [let MLPhotosFavoritesGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosfavoritesgrouptypeidentifier)
- [let MLPhotosFolderTypeIdentifier: String](/documentation/medialibrary/mlphotosfoldertypeidentifier)
- [let MLPhotosFrontCameraGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosfrontcameragrouptypeidentifier)
- [let MLPhotosLastImportGroupTypeIdentifier: String](/documentation/medialibrary/mlphotoslastimportgrouptypeidentifier)
- [let MLPhotosMomentGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosmomentgrouptypeidentifier)
- [let MLPhotosMyPhotoStreamTypeIdentifier: String](/documentation/medialibrary/mlphotosmyphotostreamtypeidentifier)
- [let MLPhotosPanoramasGroupTypeIdentifier: String](/documentation/medialibrary/mlphotospanoramasgrouptypeidentifier)
- [let MLPhotosPublishedAlbumTypeIdentifier: String](/documentation/medialibrary/mlphotospublishedalbumtypeidentifier)
- [let MLPhotosRootGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosrootgrouptypeidentifier)
- [let MLPhotosScreenshotGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosscreenshotgrouptypeidentifier)
- [let MLPhotosSharedGroupTypeIdentifier: String](/documentation/medialibrary/mlphotossharedgrouptypeidentifier)
- [let MLPhotosSharedPhotoStreamTypeIdentifier: String](/documentation/medialibrary/mlphotossharedphotostreamtypeidentifier)
- [let MLPhotosSloMoGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosslomogrouptypeidentifier)
- [let MLPhotosSmartAlbumTypeIdentifier: String](/documentation/medialibrary/mlphotossmartalbumtypeidentifier)
- [let MLPhotosTimelapseGroupTypeIdentifier: String](/documentation/medialibrary/mlphotostimelapsegrouptypeidentifier)
- [let MLPhotosVideosGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosvideosgrouptypeidentifier)
- [let MLPhotosYearGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosyeargrouptypeidentifier)
- [let MLiTunesMusicVideosPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesmusicvideosplaylisttypeidentifier)
- [let MLiTunesVideoPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesvideoplaylisttypeidentifier)
- [Media Object Attribute Keys](/documentation/medialibrary/media-object-attribute-keys)

#### Constants

- [let MLMediaObjectDurationKey: String](/documentation/medialibrary/mlmediaobjectdurationkey)
- [let MLMediaObjectArtistKey: String](/documentation/medialibrary/mlmediaobjectartistkey)
- [let MLMediaObjectAlbumKey: String](/documentation/medialibrary/mlmediaobjectalbumkey)
- [let MLMediaObjectGenreKey: String](/documentation/medialibrary/mlmediaobjectgenrekey)
- [let MLMediaObjectKindKey: String](/documentation/medialibrary/mlmediaobjectkindkey)
- [let MLMediaObjectTrackNumberKey: String](/documentation/medialibrary/mlmediaobjecttracknumberkey)
- [let MLMediaObjectBitRateKey: String](/documentation/medialibrary/mlmediaobjectbitratekey)
- [let MLMediaObjectSampleRateKey: String](/documentation/medialibrary/mlmediaobjectsampleratekey)
- [let MLMediaObjectChannelCountKey: String](/documentation/medialibrary/mlmediaobjectchannelcountkey)
- [let MLMediaObjectResolutionStringKey: String](/documentation/medialibrary/mlmediaobjectresolutionstringkey)
- [let MLMediaObjectCommentsKey: String](/documentation/medialibrary/mlmediaobjectcommentskey)
- [let MLMediaObjectKeywordsKey: String](/documentation/medialibrary/mlmediaobjectkeywordskey)
- [let MLMediaObjectProtectedKey: String](/documentation/medialibrary/mlmediaobjectprotectedkey)
- [iMovie Media Group Type Identifiers](/documentation/medialibrary/imovie-media-group-type-identifiers)

#### Constants

- [let MLiMovieRootGroupTypeIdentifier: String](/documentation/medialibrary/mlimovierootgrouptypeidentifier)
- [let MLiMovieProjectGroupTypeIdentifier: String](/documentation/medialibrary/mlimovieprojectgrouptypeidentifier)
- [let MLiMovieFolderGroupTypeIdentifier: String](/documentation/medialibrary/mlimoviefoldergrouptypeidentifier)
- [let MLiMovieEventGroupTypeIdentifier: String](/documentation/medialibrary/mlimovieeventgrouptypeidentifier)
- [let MLiMovieEventCalendarGroupTypeIdentifier: String](/documentation/medialibrary/mlimovieeventcalendargrouptypeidentifier)
- [let MLiMovieEventLibraryGroupTypeIdentifier: String](/documentation/medialibrary/mlimovieeventlibrarygrouptypeidentifier)
- [iPhoto Media Group Type Identifiers](/documentation/medialibrary/iphoto-media-group-type-identifiers)

#### Constants

- [let MLiPhotoRootGroupTypeIdentifier: String](/documentation/medialibrary/mliphotorootgrouptypeidentifier)
- [let MLiPhotoAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoalbumtypeidentifier)
- [let MLiPhotoSmartAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotosmartalbumtypeidentifier)
- [let MLiPhotoLibraryAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotolibraryalbumtypeidentifier)
- [let MLiPhotoFolderAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotofolderalbumtypeidentifier)
- [let MLiPhotoEventAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoeventalbumtypeidentifier)
- [let MLiPhotoEventsFolderTypeIdentifier: String](/documentation/medialibrary/mliphotoeventsfoldertypeidentifier)
- [let MLiPhotoLastViewedEventAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotolastviewedeventalbumtypeidentifier)
- [let MLiPhotoLastImportAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotolastimportalbumtypeidentifier)
- [let MLiPhotoLastNMonthsAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotolastnmonthsalbumtypeidentifier)
- [let MLiPhotoFlaggedAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoflaggedalbumtypeidentifier)
- [let MLiPhotoSubscribedAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotosubscribedalbumtypeidentifier)
- [let MLiPhotoSlideShowAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoslideshowalbumtypeidentifier)
- [let MLiPhotoPhotoStreamAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotophotostreamalbumtypeidentifier)
- [let MLiPhotoFacesAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotofacesalbumtypeidentifier)
- [let MLiPhotoPlacesAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoplacesalbumtypeidentifier)
- [let MLiPhotoPlacesCountryAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoplacescountryalbumtypeidentifier)
- [let MLiPhotoPlacesProvinceAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoplacesprovincealbumtypeidentifier)
- [let MLiPhotoPlacesCityAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoplacescityalbumtypeidentifier)
- [let MLiPhotoPlacesPointOfInterestAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoplacespointofinterestalbumtypeidentifier)
- [let MLiPhotoFacebookAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotofacebookalbumtypeidentifier)
- [let MLiPhotoFacebookGroupTypeIdentifier: String](/documentation/medialibrary/mliphotofacebookgrouptypeidentifier)
- [let MLiPhotoFlickrAlbumTypeIdentifier: String](/documentation/medialibrary/mliphotoflickralbumtypeidentifier)
- [let MLiPhotoFlickrGroupTypeIdentifier: String](/documentation/medialibrary/mliphotoflickrgrouptypeidentifier)
- [iTunes Media Group Type Identifiers](/documentation/medialibrary/itunes-media-group-type-identifiers)

#### Constants

- [let MLiTunesRootGroupTypeIdentifier: String](/documentation/medialibrary/mlitunesrootgrouptypeidentifier)
- [let MLiTunesPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesplaylisttypeidentifier)
- [let MLiTunesSmartPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunessmartplaylisttypeidentifier)
- [let MLiTunesGeniusPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesgeniusplaylisttypeidentifier)
- [let MLiTunesSavedGeniusPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunessavedgeniusplaylisttypeidentifier)
- [let MLiTunesFolderPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesfolderplaylisttypeidentifier)
- [let MLiTunesAudioBooksPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesaudiobooksplaylisttypeidentifier)
- [let MLiTunesiTunesUPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesitunesuplaylisttypeidentifier)
- [let MLiTunesMoviesPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesmoviesplaylisttypeidentifier)
- [let MLiTunesMusicPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunesmusicplaylisttypeidentifier)
- [let MLiTunesPodcastPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunespodcastplaylisttypeidentifier)
- [let MLiTunesPurchasedPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunespurchasedplaylisttypeidentifier)
- [let MLiTunesTVShowsPlaylistTypeIdentifier: String](/documentation/medialibrary/mlitunestvshowsplaylisttypeidentifier)
- [let MLPhotosAnimatedGroupTypeIdentifier: String](/documentation/medialibrary/mlphotosanimatedgrouptypeidentifier)
- [let MLPhotosLivePhotosGroupTypeIdentifier: String](/documentation/medialibrary/mlphotoslivephotosgrouptypeidentifier)
- [let MLPhotosLongExposureGroupTypeIdentifier: String](/documentation/medialibrary/mlphotoslongexposuregrouptypeidentifier)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
