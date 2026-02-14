# AVFoundation Documentation

Source: https://sosumi.ai/documentation/avfoundation

---
title: AVFoundation
source: https://developer.apple.com/documentation/avfoundation
timestamp: 2026-02-13T19:22:54.581Z
---

## Essentials

- [AVFoundation updates](/documentation/updates/avfoundation)

## Common

- [Media assets](/documentation/avfoundation/media-assets)

### Essentials

- [Loading media data asynchronously](/documentation/avfoundation/loading-media-data-asynchronously)

### Assets

- [AVAsset](/documentation/avfoundation/avasset)

#### Creating an asset

- [convenience init(url: URL)](/documentation/avfoundation/avasset/init(url:))

#### Loading duration and timing

- [static var duration: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/duration)
- [static var providesPreciseDurationAndTiming: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/providesprecisedurationandtiming)
- [static var minimumTimeOffsetFromLive: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/minimumtimeoffsetfromlive)

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVAssetTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-48zyw)
- [func loadTrack(withTrackID: CMPersistentTrackID, completionHandler: (AVAssetTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avasset/loadtrack(withtrackid:completionhandler:))
- [func loadTracks(withMediaType: AVMediaType, completionHandler: ([AVAssetTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avasset/loadtracks(withmediatype:completionhandler:))
- [func loadTracks(withMediaCharacteristic: AVMediaCharacteristic, completionHandler: ([AVAssetTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avasset/loadtracks(withmediacharacteristic:completionhandler:))
- [func findUnusedTrackID(completionHandler: (CMPersistentTrackID, (any Error)?) -> Void)](/documentation/avfoundation/avasset/findunusedtrackid(completionhandler:))

#### Loading track groups

- [static var trackGroups: AVAsyncProperty<Root, [AVAssetTrackGroup]>](/documentation/avfoundation/avpartialasyncproperty/trackgroups)

#### Loading metadata

- [static var metadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/metadata-16qej)
- [static var commonMetadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/commonmetadata-3j3n4)
- [static var availableMetadataFormats: AVAsyncProperty<Root, [AVMetadataFormat]>](/documentation/avfoundation/avpartialasyncproperty/availablemetadataformats-4yiq8)
- [func loadMetadata(for: AVMetadataFormat, completionHandler: ([AVMetadataItem]?, (any Error)?) -> Void)](/documentation/avfoundation/avasset/loadmetadata(for:completionhandler:))
- [static var creationDate: AVAsyncProperty<Root, AVMetadataItem?>](/documentation/avfoundation/avpartialasyncproperty/creationdate)
- [static var lyrics: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/lyrics)

#### Loading suitability

- [static var isPlayable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isplayable-45h5v)
- [static var isExportable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isexportable)
- [static var isReadable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isreadable)
- [static var isComposable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/iscomposable)
- [static var isCompatibleWithAirPlayVideo: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/iscompatiblewithairplayvideo)
- [static var isCompatibleWithSavedPhotosAlbum: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/iscompatiblewithsavedphotosalbum)

#### Loading asset preferences

- [static var preferredRate: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/preferredrate)
- [static var preferredVolume: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/preferredvolume-20mb3)
- [static var preferredTransform: AVAsyncProperty<Root, CGAffineTransform>](/documentation/avfoundation/avpartialasyncproperty/preferredtransform-80d13)
- [static var preferredDisplayCriteria: AVAsyncProperty<Root, AVDisplayCriteria>](/documentation/avfoundation/avpartialasyncproperty/preferreddisplaycriteria)
- [AVDisplayCriteria](/documentation/avfoundation/avdisplaycriteria)

##### Create a display criteria

- [init(refreshRate: Float, formatDescription: CMFormatDescription)](/documentation/avfoundation/avdisplaycriteria/init(refreshrate:formatdescription:))

#### Loading media selections

- [static var allMediaSelections: AVAsyncProperty<Root, [AVMediaSelection]>](/documentation/avfoundation/avpartialasyncproperty/allmediaselections)
- [static var preferredMediaSelection: AVAsyncProperty<Root, AVMediaSelection>](/documentation/avfoundation/avpartialasyncproperty/preferredmediaselection)
- [static var availableMediaCharacteristicsWithMediaSelectionOptions: AVAsyncProperty<Root, [AVMediaCharacteristic]>](/documentation/avfoundation/avpartialasyncproperty/availablemediacharacteristicswithmediaselectionoptions)
- [func loadMediaSelectionGroup(for: AVMediaCharacteristic, completionHandler: (AVMediaSelectionGroup?, (any Error)?) -> Void)](/documentation/avfoundation/avasset/loadmediaselectiongroup(for:completionhandler:))

#### Loading chapter metadata

- [static var availableChapterLocales: AVAsyncProperty<Root, [Locale]>](/documentation/avfoundation/avpartialasyncproperty/availablechapterlocales)
- [func loadChapterMetadataGroups(withTitleLocale: Locale, containingItemsWithCommonKeys: [AVMetadataKey]) async throws -> [AVTimedMetadataGroup]](/documentation/avfoundation/avasset/loadchaptermetadatagroups(withtitlelocale:containingitemswithcommonkeys:))
- [func loadChapterMetadataGroups(bestMatchingPreferredLanguages: [String], completionHandler: ([AVTimedMetadataGroup]?, (any Error)?) -> Void)](/documentation/avfoundation/avasset/loadchaptermetadatagroups(bestmatchingpreferredlanguages:completionhandler:))

#### Loading content protections

- [static var hasProtectedContent: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/hasprotectedcontent)

#### Loading fragment support

- [static var canContainFragments: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/cancontainfragments)
- [static var containsFragments: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/containsfragments)
- [static var overallDurationHint: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/overalldurationhint)

#### Canceling property loading

- [func cancelLoading()](/documentation/avfoundation/avasset/cancelloading())

#### Retrieving reference restrictions

- [var referenceRestrictions: AVAssetReferenceRestrictions](/documentation/avfoundation/avasset/referencerestrictions)
- [AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions)

##### Reference restrictions

- [static var forbidAll: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidall)
- [static var forbidRemoteReferenceToLocal: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidremotereferencetolocal)
- [static var forbidLocalReferenceToRemote: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidlocalreferencetoremote)
- [static var forbidCrossSiteReference: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidcrosssitereference)
- [static var forbidLocalReferenceToLocal: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidlocalreferencetolocal)
- [static var defaultPolicy: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/defaultpolicy)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avassetreferencerestrictions/init(rawvalue:))

#### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avasset-deprecated-symbols)

##### Accessing duration and timing

- [var duration: CMTime](/documentation/avfoundation/avasset/duration)
- [var providesPreciseDurationAndTiming: Bool](/documentation/avfoundation/avasset/providesprecisedurationandtiming)
- [var minimumTimeOffsetFromLive: CMTime](/documentation/avfoundation/avasset/minimumtimeoffsetfromlive)

##### Accessing tracks

- [var tracks: [AVAssetTrack]](/documentation/avfoundation/avasset/tracks)
- [func track(withTrackID: CMPersistentTrackID) -> AVAssetTrack?](/documentation/avfoundation/avasset/track(withtrackid:))
- [func tracks(withMediaType: AVMediaType) -> [AVAssetTrack]](/documentation/avfoundation/avasset/tracks(withmediatype:))
- [func tracks(withMediaCharacteristic: AVMediaCharacteristic) -> [AVAssetTrack]](/documentation/avfoundation/avasset/tracks(withmediacharacteristic:))
- [func unusedTrackID() -> CMPersistentTrackID](/documentation/avfoundation/avasset/unusedtrackid())

##### Accessing track groups

- [var trackGroups: [AVAssetTrackGroup]](/documentation/avfoundation/avasset/trackgroups)

##### Accessing metadata

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avasset/metadata)
- [var commonMetadata: [AVMetadataItem]](/documentation/avfoundation/avasset/commonmetadata)
- [var availableMetadataFormats: [AVMetadataFormat]](/documentation/avfoundation/avasset/availablemetadataformats)
- [func metadata(forFormat: AVMetadataFormat) -> [AVMetadataItem]](/documentation/avfoundation/avasset/metadata(forformat:))
- [var creationDate: AVMetadataItem?](/documentation/avfoundation/avasset/creationdate)
- [var lyrics: String?](/documentation/avfoundation/avasset/lyrics)

##### Accessing suitability

- [var isPlayable: Bool](/documentation/avfoundation/avasset/isplayable)
- [var isExportable: Bool](/documentation/avfoundation/avasset/isexportable)
- [var isReadable: Bool](/documentation/avfoundation/avasset/isreadable)
- [var isComposable: Bool](/documentation/avfoundation/avasset/iscomposable)
- [var isCompatibleWithAirPlayVideo: Bool](/documentation/avfoundation/avasset/iscompatiblewithairplayvideo)
- [var isCompatibleWithSavedPhotosAlbum: Bool](/documentation/avfoundation/avasset/iscompatiblewithsavedphotosalbum)

##### Accessing asset preferences

- [var preferredRate: Float](/documentation/avfoundation/avasset/preferredrate)
- [var preferredVolume: Float](/documentation/avfoundation/avasset/preferredvolume)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avasset/preferredtransform)
- [var preferredDisplayCriteria: AVDisplayCriteria](/documentation/avfoundation/avasset/preferreddisplaycriteria)
- [var preferredMediaSelection: AVMediaSelection](/documentation/avfoundation/avasset/preferredmediaselection)

##### Accessing media selections

- [var allMediaSelections: [AVMediaSelection]](/documentation/avfoundation/avasset/allmediaselections)
- [var availableMediaCharacteristicsWithMediaSelectionOptions: [AVMediaCharacteristic]](/documentation/avfoundation/avasset/availablemediacharacteristicswithmediaselectionoptions)
- [func mediaSelectionGroup(forMediaCharacteristic: AVMediaCharacteristic) -> AVMediaSelectionGroup?](/documentation/avfoundation/avasset/mediaselectiongroup(formediacharacteristic:))

##### Accessing chapter metadata

- [var availableChapterLocales: [Locale]](/documentation/avfoundation/avasset/availablechapterlocales)
- [func chapterMetadataGroups(withTitleLocale: Locale, containingItemsWithCommonKeys: [AVMetadataKey]?) -> [AVTimedMetadataGroup]](/documentation/avfoundation/avasset/chaptermetadatagroups(withtitlelocale:containingitemswithcommonkeys:))
- [func chapterMetadataGroups(bestMatchingPreferredLanguages: [String]) -> [AVTimedMetadataGroup]](/documentation/avfoundation/avasset/chaptermetadatagroups(bestmatchingpreferredlanguages:))

##### Accessing content protections

- [var hasProtectedContent: Bool](/documentation/avfoundation/avasset/hasprotectedcontent)

##### Accessing fragment support

- [var canContainFragments: Bool](/documentation/avfoundation/avasset/cancontainfragments)
- [var containsFragments: Bool](/documentation/avfoundation/avasset/containsfragments)
- [var overallDurationHint: CMTime](/documentation/avfoundation/avasset/overalldurationhint)

##### Inspecting visual attributes

- [var naturalSize: CGSize](/documentation/avfoundation/avasset/naturalsize)
- [AVURLAsset](/documentation/avfoundation/avurlasset)

#### Creating an asset

- [convenience init(url: URL)](/documentation/avfoundation/avurlasset/init(url:))
- [init(url: URL, options: [String : Any]?)](/documentation/avfoundation/avurlasset/init(url:options:))
- [Initialization options](/documentation/avfoundation/avurlasset-initialization-options)

##### Options

- [let AVURLAssetAllowsCellularAccessKey: String](/documentation/avfoundation/avurlassetallowscellularaccesskey)
- [let AVURLAssetAllowsConstrainedNetworkAccessKey: String](/documentation/avfoundation/avurlassetallowsconstrainednetworkaccesskey)
- [let AVURLAssetAllowsExpensiveNetworkAccessKey: String](/documentation/avfoundation/avurlassetallowsexpensivenetworkaccesskey)
- [let AVURLAssetHTTPCookiesKey: String](/documentation/avfoundation/avurlassethttpcookieskey)
- [let AVURLAssetHTTPUserAgentKey: String](/documentation/avfoundation/avurlassethttpuseragentkey)
- [let AVURLAssetOverrideMIMETypeKey: String](/documentation/avfoundation/avurlassetoverridemimetypekey)
- [let AVURLAssetPreferPreciseDurationAndTimingKey: String](/documentation/avfoundation/avurlassetpreferprecisedurationandtimingkey)
- [let AVURLAssetPrimarySessionIdentifierKey: String](/documentation/avfoundation/avurlassetprimarysessionidentifierkey)
- [let AVURLAssetReferenceRestrictionsKey: String](/documentation/avfoundation/avurlassetreferencerestrictionskey)

###### Data types

- [AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions)

###### Reference restrictions

- [static var forbidAll: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidall)
- [static var forbidRemoteReferenceToLocal: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidremotereferencetolocal)
- [static var forbidLocalReferenceToRemote: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidlocalreferencetoremote)
- [static var forbidCrossSiteReference: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidcrosssitereference)
- [static var forbidLocalReferenceToLocal: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/forbidlocalreferencetolocal)
- [static var defaultPolicy: AVAssetReferenceRestrictions](/documentation/avfoundation/avassetreferencerestrictions/defaultpolicy)

###### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avassetreferencerestrictions/init(rawvalue:))
- [let AVURLAssetShouldSupportAliasDataReferencesKey: String](/documentation/avfoundation/avurlassetshouldsupportaliasdatareferenceskey)
- [let AVURLAssetURLRequestAttributionKey: String](/documentation/avfoundation/avurlasseturlrequestattributionkey)
- [let AVURLAssetShouldParseExternalSphericalTagsKey: String](/documentation/avfoundation/avurlassetshouldparseexternalsphericaltagskey)

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVAssetTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-44ptx)
- [func findCompatibleTrack(for: AVCompositionTrack, completionHandler: (AVAssetTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avurlasset/findcompatibletrack(for:completionhandler:))

#### Loading variants

- [static var variants: AVAsyncProperty<Root, [AVAssetVariant]>](/documentation/avfoundation/avpartialasyncproperty/variants)

#### Determining supported media types

- [class func audiovisualTypes() -> [AVFileType]](/documentation/avfoundation/avurlasset/audiovisualtypes())
- [class func audiovisualMIMETypes() -> [String]](/documentation/avfoundation/avurlasset/audiovisualmimetypes())
- [class func isPlayableExtendedMIMEType(String) -> Bool](/documentation/avfoundation/avurlasset/isplayableextendedmimetype(_:))
- [class var audiovisualContentTypes: [UTType]](/documentation/avfoundation/avurlasset/audiovisualcontenttypes)

#### Assisting with resource loading

- [var resourceLoader: AVAssetResourceLoader](/documentation/avfoundation/avurlasset/resourceloader)
- [var mayRequireContentKeysForMediaDataProcessing: Bool](/documentation/avfoundation/avurlasset/mayrequirecontentkeysformediadataprocessing)

#### Working with offline assets

- [var assetCache: AVAssetCache?](/documentation/avfoundation/avurlasset/assetcache)

#### Accessing the media URL

- [var url: URL](/documentation/avfoundation/avurlasset/url)

#### Accessing asset variants

- [var variants: [AVAssetVariant]](/documentation/avfoundation/avurlasset/variants)

#### Accessing compatible tracks

- [func compatibleTrack(for: AVCompositionTrack) -> AVAssetTrack?](/documentation/avfoundation/avurlasset/compatibletrack(for:))

#### Accessing the session identifier

- [var httpSessionIdentifier: UUID](/documentation/avfoundation/avurlasset/httpsessionidentifier)

#### Accessing Media Extension properties

- [var mediaExtensionProperties: AVMediaExtensionProperties?](/documentation/avfoundation/avurlasset/mediaextensionproperties)
- [AVMediaExtensionProperties](/documentation/avfoundation/avmediaextensionproperties)

##### Inspecting the extension

- [var extensionName: String](/documentation/avfoundation/avmediaextensionproperties/extensionname)
- [var containingBundleName: String](/documentation/avfoundation/avmediaextensionproperties/containingbundlename)
- [var extensionIdentifier: String](/documentation/avfoundation/avmediaextensionproperties/extensionidentifier)
- [var extensionURL: URL](/documentation/avfoundation/avmediaextensionproperties/extensionurl)
- [var containingBundleURL: URL](/documentation/avfoundation/avmediaextensionproperties/containingbundleurl)
- [AVAssetTrack](/documentation/avfoundation/avassettrack)

#### Identifying an asset track

- [var trackID: CMPersistentTrackID](/documentation/avfoundation/avassettrack/trackid)
- [var mediaType: AVMediaType](/documentation/avfoundation/avassettrack/mediatype)
- [var asset: AVAsset?](/documentation/avfoundation/avassettrack/asset)

#### Loading track information

- [static var formatDescriptions: AVAsyncProperty<Root, [CMFormatDescription]>](/documentation/avfoundation/avpartialasyncproperty/formatdescriptions)
- [static var isPlayable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isplayable-6txa5)
- [static var isDecodable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isdecodable)
- [static var isEnabled: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isenabled)
- [static var isSelfContained: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isselfcontained)
- [static var totalSampleDataLength: AVAsyncProperty<Root, Int64>](/documentation/avfoundation/avpartialasyncproperty/totalsampledatalength)
- [static var mediaCharacteristics: AVAsyncProperty<Root, [AVMediaCharacteristic]>](/documentation/avfoundation/avpartialasyncproperty/mediacharacteristics)

#### Loading temporal information

- [static var timeRange: AVAsyncProperty<Root, CMTimeRange>](/documentation/avfoundation/avpartialasyncproperty/timerange)
- [static var naturalTimeScale: AVAsyncProperty<Root, CMTimeScale>](/documentation/avfoundation/avpartialasyncproperty/naturaltimescale)
- [static var estimatedDataRate: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/estimateddatarate)

#### Loading language support

- [static var languageCode: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/languagecode)
- [static var extendedLanguageTag: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/extendedlanguagetag)

#### Loading visual characteristics

- [static var naturalSize: AVAsyncProperty<Root, CGSize>](/documentation/avfoundation/avpartialasyncproperty/naturalsize)
- [static var preferredTransform: AVAsyncProperty<Root, CGAffineTransform>](/documentation/avfoundation/avpartialasyncproperty/preferredtransform-90jdn)

#### Loading audible characteristics

- [static var preferredVolume: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/preferredvolume-8q2yt)
- [static var hasAudioSampleDependencies: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/hasaudiosampledependencies)

#### Loading frame-based characteristics

- [static var nominalFrameRate: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/nominalframerate)
- [static var minFrameDuration: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/minframeduration)
- [static var requiresFrameReordering: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/requiresframereordering)

#### Loading metadata

- [static var metadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/metadata-6e14c)
- [static var commonMetadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/commonmetadata-73m58)
- [static var availableMetadataFormats: AVAsyncProperty<Root, [AVMetadataFormat]>](/documentation/avfoundation/avpartialasyncproperty/availablemetadataformats-5p9xg)
- [func loadMetadata(for: AVMetadataFormat, completionHandler: ([AVMetadataItem]?, (any Error)?) -> Void)](/documentation/avfoundation/avassettrack/loadmetadata(for:completionhandler:))

#### Loading track segments

- [static var segments: AVAsyncProperty<Root, [AVAssetTrackSegment]>](/documentation/avfoundation/avpartialasyncproperty/segments)
- [func loadSegment(forTrackTime: CMTime, completionHandler: (AVAssetTrackSegment?, (any Error)?) -> Void)](/documentation/avfoundation/avassettrack/loadsegment(fortracktime:completionhandler:))
- [func loadSamplePresentationTime(forTrackTime: CMTime, completionHandler: (CMTime, (any Error)?) -> Void)](/documentation/avfoundation/avassettrack/loadsamplepresentationtime(fortracktime:completionhandler:))
- [AVAssetTrackSegment](/documentation/avfoundation/avassettracksegment)

##### Retrieving segment information

- [var timeMapping: CMTimeMapping](/documentation/avfoundation/avassettracksegment/timemapping)
- [var isEmpty: Bool](/documentation/avfoundation/avassettracksegment/isempty)

#### Loading track associations

- [static var availableTrackAssociationTypes: AVAsyncProperty<Root, [AVAssetTrack.AssociationType]>](/documentation/avfoundation/avpartialasyncproperty/availabletrackassociationtypes)
- [func loadAssociatedTracks(ofType: AVAssetTrack.AssociationType, completionHandler: ([AVAssetTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avassettrack/loadassociatedtracks(oftype:completionhandler:))

#### Creating sample cursors

- [func makeSampleCursor(presentationTimeStamp: CMTime) -> AVSampleCursor?](/documentation/avfoundation/avassettrack/makesamplecursor(presentationtimestamp:))
- [func makeSampleCursorAtFirstSampleInDecodeOrder() -> AVSampleCursor?](/documentation/avfoundation/avassettrack/makesamplecursoratfirstsampleindecodeorder())
- [func makeSampleCursorAtLastSampleInDecodeOrder() -> AVSampleCursor?](/documentation/avfoundation/avassettrack/makesamplecursoratlastsampleindecodeorder())

#### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avassettrack-deprecated-symbols)

##### Accessing track information

- [var formatDescriptions: [Any]](/documentation/avfoundation/avassettrack/formatdescriptions)
- [var isPlayable: Bool](/documentation/avfoundation/avassettrack/isplayable)
- [var isDecodable: Bool](/documentation/avfoundation/avassettrack/isdecodable)
- [var isEnabled: Bool](/documentation/avfoundation/avassettrack/isenabled)
- [var isSelfContained: Bool](/documentation/avfoundation/avassettrack/isselfcontained)
- [var totalSampleDataLength: Int64](/documentation/avfoundation/avassettrack/totalsampledatalength)
- [func hasMediaCharacteristic(AVMediaCharacteristic) -> Bool](/documentation/avfoundation/avassettrack/hasmediacharacteristic(_:))

##### Accessing temporal information

- [var timeRange: CMTimeRange](/documentation/avfoundation/avassettrack/timerange)
- [var naturalTimeScale: CMTimeScale](/documentation/avfoundation/avassettrack/naturaltimescale)
- [var estimatedDataRate: Float](/documentation/avfoundation/avassettrack/estimateddatarate)

##### Accessing language support

- [var languageCode: String?](/documentation/avfoundation/avassettrack/languagecode)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avassettrack/extendedlanguagetag)

##### Accessing visual characteristics

- [var naturalSize: CGSize](/documentation/avfoundation/avassettrack/naturalsize)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avassettrack/preferredtransform)

##### Accessing audible characteristics

- [var preferredVolume: Float](/documentation/avfoundation/avassettrack/preferredvolume)
- [var hasAudioSampleDependencies: Bool](/documentation/avfoundation/avassettrack/hasaudiosampledependencies)

##### Accessing frame-based characteristics

- [var nominalFrameRate: Float](/documentation/avfoundation/avassettrack/nominalframerate)
- [var minFrameDuration: CMTime](/documentation/avfoundation/avassettrack/minframeduration)
- [var requiresFrameReordering: Bool](/documentation/avfoundation/avassettrack/requiresframereordering)

##### Accessing metadata

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avassettrack/metadata)
- [var commonMetadata: [AVMetadataItem]](/documentation/avfoundation/avassettrack/commonmetadata)
- [var availableMetadataFormats: [AVMetadataFormat]](/documentation/avfoundation/avassettrack/availablemetadataformats)
- [func metadata(forFormat: AVMetadataFormat) -> [AVMetadataItem]](/documentation/avfoundation/avassettrack/metadata(forformat:))

##### Accessing track segments

- [var segments: [AVAssetTrackSegment]](/documentation/avfoundation/avassettrack/segments)
- [func segment(forTrackTime: CMTime) -> AVAssetTrackSegment?](/documentation/avfoundation/avassettrack/segment(fortracktime:))
- [func samplePresentationTime(forTrackTime: CMTime) -> CMTime](/documentation/avfoundation/avassettrack/samplepresentationtime(fortracktime:))

##### Accessing track associations

- [var availableTrackAssociationTypes: [AVAssetTrack.AssociationType]](/documentation/avfoundation/avassettrack/availabletrackassociationtypes)
- [func associatedTracks(ofType: AVAssetTrack.AssociationType) -> [AVAssetTrack]](/documentation/avfoundation/avassettrack/associatedtracks(oftype:))

##### Creating sample cursors

- [var canProvideSampleCursors: Bool](/documentation/avfoundation/avassettrack/canprovidesamplecursors)
- [AVAssetTrackSegment](/documentation/avfoundation/avassettracksegment)

#### Retrieving segment information

- [var timeMapping: CMTimeMapping](/documentation/avfoundation/avassettracksegment/timemapping)
- [var isEmpty: Bool](/documentation/avfoundation/avassettracksegment/isempty)
- [AVAssetTrackGroup](/documentation/avfoundation/avassettrackgroup)

#### Getting track ID values

- [var trackIDs: [NSNumber]](/documentation/avfoundation/avassettrackgroup/trackids)

### Metadata

- [Retrieving media metadata](/documentation/avfoundation/retrieving-media-metadata)
- [AVMetadataItem](/documentation/avfoundation/avmetadataitem)

#### Creating a metadata item

- [init(propertiesOfMetadataItem: AVMetadataItem, valueLoadingHandler: (AVMetadataItemValueRequest) -> Void)](/documentation/avfoundation/avmetadataitem/init(propertiesofmetadataitem:valueloadinghandler:))
- [AVMetadataItemValueRequest](/documentation/avfoundation/avmetadataitemvaluerequest)

##### Handling the response

- [func respond(value: any NSCopying & NSObjectProtocol)](/documentation/avfoundation/avmetadataitemvaluerequest/respond(value:))
- [func respond(error: any Error)](/documentation/avfoundation/avmetadataitemvaluerequest/respond(error:))
- [var metadataItem: AVMetadataItem?](/documentation/avfoundation/avmetadataitemvaluerequest/metadataitem)

#### Identifying metadata items

- [var identifier: AVMetadataIdentifier?](/documentation/avfoundation/avmetadataitem/identifier)

#### Loading values

- [var dataType: String?](/documentation/avfoundation/avmetadataitem/datatype)
- [static var value: AVAsyncProperty<Root, (any NSCopying & NSObjectProtocol)?>](/documentation/avfoundation/avpartialasyncproperty/value)
- [static var stringValue: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/stringvalue)
- [static var numberValue: AVAsyncProperty<Root, NSNumber?>](/documentation/avfoundation/avpartialasyncproperty/numbervalue)
- [static var dateValue: AVAsyncProperty<Root, Date?>](/documentation/avfoundation/avpartialasyncproperty/datevalue)
- [static var dataValue: AVAsyncProperty<Root, Data?>](/documentation/avfoundation/avpartialasyncproperty/datavalue)
- [static var extraAttributes: AVAsyncProperty<Root, [AVMetadataExtraAttributeKey : Any]?>](/documentation/avfoundation/avpartialasyncproperty/extraattributes)

#### Accessing keys and key spaces

- [var key: (any NSCopying & NSObjectProtocol)?](/documentation/avfoundation/avmetadataitem/key)
- [var commonKey: AVMetadataKey?](/documentation/avfoundation/avmetadataitem/commonkey)
- [var keySpace: AVMetadataKeySpace?](/documentation/avfoundation/avmetadataitem/keyspace)

#### Accessing timing

- [var time: CMTime](/documentation/avfoundation/avmetadataitem/time)
- [var startDate: Date?](/documentation/avfoundation/avmetadataitem/startdate)
- [var duration: CMTime](/documentation/avfoundation/avmetadataitem/duration)

#### Accessing language support

- [var locale: Locale?](/documentation/avfoundation/avmetadataitem/locale)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avmetadataitem/extendedlanguagetag)

#### Filtering arrays of metadata items

- [class func metadataItems(from: [AVMetadataItem], filteredByIdentifier: AVMetadataIdentifier) -> [AVMetadataItem]](/documentation/avfoundation/avmetadataitem/metadataitems(from:filteredbyidentifier:))
- [class func metadataItems(from: [AVMetadataItem], withKey: Any?, keySpace: AVMetadataKeySpace?) -> [AVMetadataItem]](/documentation/avfoundation/avmetadataitem/metadataitems(from:withkey:keyspace:))
- [class func metadataItems(from: [AVMetadataItem], with: Locale) -> [AVMetadataItem]](/documentation/avfoundation/avmetadataitem/metadataitems(from:with:))
- [class func metadataItems(from: [AVMetadataItem], filteredAndSortedAccordingToPreferredLanguages: [String]) -> [AVMetadataItem]](/documentation/avfoundation/avmetadataitem/metadataitems(from:filteredandsortedaccordingtopreferredlanguages:))
- [class func metadataItems(from: [AVMetadataItem], filteredBy: AVMetadataItemFilter) -> [AVMetadataItem]](/documentation/avfoundation/avmetadataitem/metadataitems(from:filteredby:))

#### Translating metadata items

- [class func identifier(forKey: Any, keySpace: AVMetadataKeySpace) -> AVMetadataIdentifier?](/documentation/avfoundation/avmetadataitem/identifier(forkey:keyspace:))
- [class func key(forIdentifier: AVMetadataIdentifier) -> Any?](/documentation/avfoundation/avmetadataitem/key(foridentifier:))
- [class func keySpace(forIdentifier: AVMetadataIdentifier) -> AVMetadataKeySpace?](/documentation/avfoundation/avmetadataitem/keyspace(foridentifier:))

#### Accessing values

- [var value: (any NSCopying & NSObjectProtocol)?](/documentation/avfoundation/avmetadataitem/value)
- [var extraAttributes: [AVMetadataExtraAttributeKey : Any]?](/documentation/avfoundation/avmetadataitem/extraattributes)
- [var stringValue: String?](/documentation/avfoundation/avmetadataitem/stringvalue)
- [var numberValue: NSNumber?](/documentation/avfoundation/avmetadataitem/numbervalue)
- [var dateValue: Date?](/documentation/avfoundation/avmetadataitem/datevalue)
- [var dataValue: Data?](/documentation/avfoundation/avmetadataitem/datavalue)
- [AVMutableMetadataItem](/documentation/avfoundation/avmutablemetadataitem)

#### Identifying metadata items

- [var identifier: AVMetadataIdentifier?](/documentation/avfoundation/avmutablemetadataitem/identifier)

#### Accessing keys and key spaces

- [var key: (any NSCopying & NSObjectProtocol)?](/documentation/avfoundation/avmutablemetadataitem/key)
- [var keySpace: AVMetadataKeySpace?](/documentation/avfoundation/avmutablemetadataitem/keyspace)

#### Accessing values

- [var value: (any NSCopying & NSObjectProtocol)?](/documentation/avfoundation/avmutablemetadataitem/value)
- [var extraAttributes: [AVMetadataExtraAttributeKey : Any]?](/documentation/avfoundation/avmutablemetadataitem/extraattributes)
- [var dataType: String?](/documentation/avfoundation/avmutablemetadataitem/datatype)
- [var stringValue: String?](/documentation/avfoundation/avmutablemetadataitem/stringvalue)
- [var numberValue: NSNumber?](/documentation/avfoundation/avmutablemetadataitem/numbervalue)
- [var dateValue: Date?](/documentation/avfoundation/avmutablemetadataitem/datevalue)
- [var dataValue: Data?](/documentation/avfoundation/avmutablemetadataitem/datavalue)

#### Accessing timing

- [var time: CMTime](/documentation/avfoundation/avmutablemetadataitem/time)
- [var startDate: Date?](/documentation/avfoundation/avmutablemetadataitem/startdate)
- [var duration: CMTime](/documentation/avfoundation/avmutablemetadataitem/duration)

#### Accessing language support

- [var locale: Locale?](/documentation/avfoundation/avmutablemetadataitem/locale)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avmutablemetadataitem/extendedlanguagetag)
- [AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier)

#### Common metadata identifiers

- [static let commonIdentifierAccessibilityDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifieraccessibilitydescription)
- [static let commonIdentifierAlbumName: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifieralbumname)
- [static let commonIdentifierArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierartist)
- [static let commonIdentifierArtwork: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierartwork)
- [static let commonIdentifierAssetIdentifier: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierassetidentifier)
- [static let commonIdentifierAuthor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierauthor)
- [static let commonIdentifierContributor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiercontributor)
- [static let commonIdentifierCopyrights: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiercopyrights)
- [static let commonIdentifierCreationDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiercreationdate)
- [static let commonIdentifierCreator: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiercreator)
- [static let commonIdentifierDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierdescription)
- [static let commonIdentifierFormat: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierformat)
- [static let commonIdentifierLanguage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierlanguage)
- [static let commonIdentifierLastModifiedDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierlastmodifieddate)
- [static let commonIdentifierLocation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierlocation)
- [static let commonIdentifierMake: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiermake)
- [static let commonIdentifierModel: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiermodel)
- [static let commonIdentifierPublisher: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierpublisher)
- [static let commonIdentifierRelation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifierrelation)
- [static let commonIdentifierSoftware: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiersoftware)
- [static let commonIdentifierSource: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiersource)
- [static let commonIdentifierSubject: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiersubject)
- [static let commonIdentifierTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiertitle)
- [static let commonIdentifierType: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/commonidentifiertype)

#### iTunes metadata identifiers

- [static let iTunesMetadataAccountKind: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataaccountkind)
- [static let iTunesMetadataAcknowledgement: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataacknowledgement)
- [static let iTunesMetadataAlbum: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataalbum)
- [static let iTunesMetadataAlbumArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataalbumartist)
- [static let iTunesMetadataAppleID: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataappleid)
- [static let iTunesMetadataArranger: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataarranger)
- [static let iTunesMetadataArtDirector: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataartdirector)
- [static let iTunesMetadataArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataartist)
- [static let iTunesMetadataArtistID: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataartistid)
- [static let iTunesMetadataAuthor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataauthor)
- [static let iTunesMetadataBeatsPerMin: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatabeatspermin)
- [static let iTunesMetadataComposer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatacomposer)
- [static let iTunesMetadataConductor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataconductor)
- [static let iTunesMetadataContentRating: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatacontentrating)
- [static let iTunesMetadataCopyright: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatacopyright)
- [static let iTunesMetadataCoverArt: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatacoverart)
- [static let iTunesMetadataCredits: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatacredits)
- [static let iTunesMetadataDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatadescription)
- [static let iTunesMetadataDirector: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatadirector)
- [static let iTunesMetadataDiscCompilation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatadisccompilation)
- [static let iTunesMetadataDiscNumber: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatadiscnumber)
- [static let iTunesMetadataEncodedBy: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataencodedby)
- [static let iTunesMetadataEncodingTool: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataencodingtool)
- [static let iTunesMetadataEQ: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataeq)
- [static let iTunesMetadataExecProducer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataexecproducer)
- [static let iTunesMetadataGenreID: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatagenreid)
- [static let iTunesMetadataGrouping: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatagrouping)
- [static let iTunesMetadataLinerNotes: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatalinernotes)
- [static let iTunesMetadataLyrics: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatalyrics)
- [static let iTunesMetadataOnlineExtras: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataonlineextras)
- [static let iTunesMetadataOriginalArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataoriginalartist)
- [static let iTunesMetadataPerformer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataperformer)
- [static let iTunesMetadataPhonogramRights: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataphonogramrights)
- [static let iTunesMetadataPlaylistID: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataplaylistid)
- [static let iTunesMetadataPredefinedGenre: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatapredefinedgenre)
- [static let iTunesMetadataProducer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadataproducer)
- [static let iTunesMetadataPublisher: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatapublisher)
- [static let iTunesMetadataRecordCompany: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatarecordcompany)
- [static let iTunesMetadataReleaseDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatareleasedate)
- [static let iTunesMetadataSoloist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatasoloist)
- [static let iTunesMetadataSongID: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatasongid)
- [static let iTunesMetadataSongName: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatasongname)
- [static let iTunesMetadataSoundEngineer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatasoundengineer)
- [static let iTunesMetadataThanks: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatathanks)
- [static let iTunesMetadataTrackNumber: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatatracknumber)
- [static let iTunesMetadataTrackSubTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatatracksubtitle)
- [static let iTunesMetadataUserComment: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatausercomment)
- [static let iTunesMetadataUserGenre: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/itunesmetadatausergenre)

#### QuickTime metadata identifiers

- [static let quickTimeMetadataAIMEData: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataaimedata)
- [static let quickTimeMetadataAccessibilityDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataaccessibilitydescription)
- [static let quickTimeMetadataAlbum: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataalbum)
- [static let quickTimeMetadataArranger: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataarranger)
- [static let quickTimeMetadataArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataartist)
- [static let quickTimeMetadataArtwork: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataartwork)
- [static let quickTimeMetadataAuthor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataauthor)
- [static let quickTimeMetadataAutoLivePhoto: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataautolivephoto)
- [static let quickTimeMetadataCameraFocalLength35mmEquivalent: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacamerafocallength35mmequivalent)
- [static let quickTimeMetadataCameraFrameReadoutTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacameraframereadouttime)
- [static let quickTimeMetadataCameraISOSensitivity: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacameraisosensitivity)
- [static let quickTimeMetadataCameraIdentifier: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacameraidentifier)
- [static let quickTimeMetadataCameraLensIrisFNumber: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacameralensirisfnumber)
- [static let quickTimeMetadataCameraLensModel: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacameralensmodel)
- [static let quickTimeMetadataCameraShutterSpeedAngle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacamerashutterspeedangle)
- [static let quickTimeMetadataCameraShutterSpeedTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacamerashutterspeedtime)
- [static let quickTimeMetadataCameraWhiteBalance: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacamerawhitebalance)
- [static let quickTimeMetadataCinematicVideoIntent: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacinematicvideointent)
- [static let quickTimeMetadataCollectionUser: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacollectionuser)
- [static let quickTimeMetadataComment: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacomment)
- [static let quickTimeMetadataComposer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacomposer)
- [static let quickTimeMetadataContentIdentifier: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacontentidentifier)
- [static let quickTimeMetadataCopyright: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacopyright)
- [static let quickTimeMetadataCreationDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacreationdate)
- [static let quickTimeMetadataCredits: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatacredits)
- [static let quickTimeMetadataDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadescription)
- [static let quickTimeMetadataDetectedCatBody: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadetectedcatbody)
- [static let quickTimeMetadataDetectedDogBody: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadetecteddogbody)
- [static let quickTimeMetadataDetectedFace: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadetectedface)
- [static let quickTimeMetadataDetectedHumanBody: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadetectedhumanbody)
- [static let quickTimeMetadataDetectedSalientObject: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadetectedsalientobject)
- [static let quickTimeMetadataDirectionFacing: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadirectionfacing)
- [static let quickTimeMetadataDirectionMotion: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadirectionmotion)
- [static let quickTimeMetadataDirector: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadirector)
- [static let quickTimeMetadataDisplayName: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatadisplayname)
- [static let quickTimeMetadataEncodedBy: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataencodedby)
- [static let quickTimeMetadataFullFrameRatePlaybackIntent: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatafullframerateplaybackintent)
- [static let quickTimeMetadataGenre: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatagenre)
- [static let quickTimeMetadataInformation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatainformation)
- [static let quickTimeMetadataIsMontage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataismontage)
- [static let quickTimeMetadataKeywords: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatakeywords)
- [static let quickTimeMetadataLivePhotoVitalityScore: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalivephotovitalityscore)
- [static let quickTimeMetadataLivePhotoVitalityScoringVersion: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalivephotovitalityscoringversion)
- [static let quickTimeMetadataLocationBody: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalocationbody)
- [static let quickTimeMetadataLocationDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalocationdate)
- [static let quickTimeMetadataLocationHorizontalAccuracyInMeters: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalocationhorizontalaccuracyinmeters)
- [static let quickTimeMetadataLocationISO6709: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalocationiso6709)
- [static let quickTimeMetadataLocationName: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalocationname)
- [static let quickTimeMetadataLocationNote: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalocationnote)
- [static let quickTimeMetadataLocationRole: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatalocationrole)
- [static let quickTimeMetadataMake: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatamake)
- [static let quickTimeMetadataModel: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatamodel)
- [static let quickTimeMetadataOriginalArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataoriginalartist)
- [static let quickTimeMetadataPerformer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataperformer)
- [static let quickTimeMetadataPhonogramRights: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataphonogramrights)
- [static let quickTimeMetadataPreferredAffineTransform: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatapreferredaffinetransform)
- [static let quickTimeMetadataPresentationImmersiveMedia: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatapresentationimmersivemedia)
- [static let quickTimeMetadataProducer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataproducer)
- [static let quickTimeMetadataPublisher: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatapublisher)
- [static let quickTimeMetadataRatingUser: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataratinguser)
- [static let quickTimeMetadataSoftware: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatasoftware)
- [static let quickTimeMetadataSpatialOverCaptureQualityScore: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataspatialovercapturequalityscore)
- [static let quickTimeMetadataSpatialOverCaptureQualityScoringVersion: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataspatialovercapturequalityscoringversion)
- [static let quickTimeMetadataTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatatitle)
- [static let quickTimeMetadataVideoOrientation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatavideoorientation)
- [static let quickTimeMetadataWhiteBalanceByCCTColorMatrices: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatawhitebalancebycctcolormatrices)
- [static let quickTimeMetadataWhiteBalanceByCCTWhiteBalanceFactors: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatawhitebalancebycctwhitebalancefactors)
- [static let quickTimeMetadataYear: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadatayear)
- [static let quickTimeMetadataiXML: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimemetadataixml)

#### QuickTime user metadata identifiers

- [static let quickTimeUserDataAccessibilityDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataaccessibilitydescription)
- [static let quickTimeUserDataAlbum: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataalbum)
- [static let quickTimeUserDataArranger: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataarranger)
- [static let quickTimeUserDataArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataartist)
- [static let quickTimeUserDataAuthor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataauthor)
- [static let quickTimeUserDataChapter: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatachapter)
- [static let quickTimeUserDataComment: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatacomment)
- [static let quickTimeUserDataComposer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatacomposer)
- [static let quickTimeUserDataCopyright: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatacopyright)
- [static let quickTimeUserDataCreationDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatacreationdate)
- [static let quickTimeUserDataCredits: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatacredits)
- [static let quickTimeUserDataDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatadescription)
- [static let quickTimeUserDataDirector: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatadirector)
- [static let quickTimeUserDataDisclaimer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatadisclaimer)
- [static let quickTimeUserDataEncodedBy: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataencodedby)
- [static let quickTimeUserDataFullName: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatafullname)
- [static let quickTimeUserDataGenre: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatagenre)
- [static let quickTimeUserDataHostComputer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatahostcomputer)
- [static let quickTimeUserDataInformation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatainformation)
- [static let quickTimeUserDataKeywords: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatakeywords)
- [static let quickTimeUserDataLocationISO6709: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatalocationiso6709)
- [static let quickTimeUserDataMake: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatamake)
- [static let quickTimeUserDataModel: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatamodel)
- [static let quickTimeUserDataOriginalArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataoriginalartist)
- [static let quickTimeUserDataOriginalFormat: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataoriginalformat)
- [static let quickTimeUserDataOriginalSource: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataoriginalsource)
- [static let quickTimeUserDataPerformers: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataperformers)
- [static let quickTimeUserDataPhonogramRights: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataphonogramrights)
- [static let quickTimeUserDataProducer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataproducer)
- [static let quickTimeUserDataProduct: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataproduct)
- [static let quickTimeUserDataPublisher: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatapublisher)
- [static let quickTimeUserDataSoftware: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatasoftware)
- [static let quickTimeUserDataSpecialPlaybackRequirements: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataspecialplaybackrequirements)
- [static let quickTimeUserDataTaggedCharacteristic: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatataggedcharacteristic)
- [static let quickTimeUserDataTrackName: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatatrackname)
- [static let quickTimeUserDataTrack: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatatrack)
- [static let quickTimeUserDataURLLink: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdataurllink)
- [static let quickTimeUserDataWarning: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatawarning)
- [static let quickTimeUserDataWriter: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/quicktimeuserdatawriter)

#### ID3 metadata identifiers

- [static let id3MetadataAlbumSortOrder: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataalbumsortorder)
- [static let id3MetadataAlbumTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataalbumtitle)
- [static let id3MetadataAttachedPicture: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataattachedpicture)
- [static let id3MetadataAudioEncryption: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataaudioencryption)
- [static let id3MetadataAudioSeekPointIndex: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataaudioseekpointindex)
- [static let id3MetadataBand: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataband)
- [static let id3MetadataBeatsPerMinute: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatabeatsperminute)
- [static let id3MetadataComments: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacomments)
- [static let id3MetadataCommercial: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacommercial)
- [static let id3MetadataCommercialInformation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacommercialinformation)
- [static let id3MetadataComposer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacomposer)
- [static let id3MetadataConductor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataconductor)
- [static let id3MetadataContentGroupDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacontentgroupdescription)
- [static let id3MetadataContentType: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacontenttype)
- [static let id3MetadataCopyright: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacopyright)
- [static let id3MetadataCopyrightInformation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacopyrightinformation)
- [static let id3MetadataDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatadate)
- [static let id3MetadataEncodedBy: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataencodedby)
- [static let id3MetadataEncodedWith: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataencodedwith)
- [static let id3MetadataEncodingTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataencodingtime)
- [static let id3MetadataEncryption: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataencryption)
- [static let id3MetadataEqualization: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataequalization)
- [static let id3MetadataEqualization2: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataequalization2)
- [static let id3MetadataEventTimingCodes: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataeventtimingcodes)
- [static let id3MetadataFileOwner: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatafileowner)
- [static let id3MetadataFileType: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatafiletype)
- [static let id3MetadataGeneralEncapsulatedObject: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatageneralencapsulatedobject)
- [static let id3MetadataGroupIdentifier: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatagroupidentifier)
- [static let id3MetadataInitialKey: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatainitialkey)
- [static let id3MetadataInternationalStandardRecordingCode: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatainternationalstandardrecordingcode)
- [static let id3MetadataInternetRadioStationName: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatainternetradiostationname)
- [static let id3MetadataInternetRadioStationOwner: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatainternetradiostationowner)
- [static let id3MetadataInvolvedPeopleList_v23: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatainvolvedpeoplelist_v23)
- [static let id3MetadataInvolvedPeopleList_v24: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatainvolvedpeoplelist_v24)
- [static let id3MetadataLanguage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatalanguage)
- [static let id3MetadataLeadPerformer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataleadperformer)
- [static let id3MetadataLength: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatalength)
- [static let id3MetadataLink: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatalink)
- [static let id3MetadataLyricist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatalyricist)
- [static let id3MetadataMediaType: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatamediatype)
- [static let id3MetadataModifiedBy: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatamodifiedby)
- [static let id3MetadataMood: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatamood)
- [static let id3MetadataMPEGLocationLookupTable: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatampeglocationlookuptable)
- [static let id3MetadataMusicCDIdentifier: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatamusiccdidentifier)
- [static let id3MetadataMusicianCreditsList: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatamusiciancreditslist)
- [static let id3MetadataOfficialArtistWebpage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataofficialartistwebpage)
- [static let id3MetadataOfficialAudioFileWebpage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataofficialaudiofilewebpage)
- [static let id3MetadataOfficialAudioSourceWebpage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataofficialaudiosourcewebpage)
- [static let id3MetadataOfficialInternetRadioStationHomepage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataofficialinternetradiostationhomepage)
- [static let id3MetadataOfficialPublisherWebpage: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataofficialpublisherwebpage)
- [static let id3MetadataOriginalAlbumTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataoriginalalbumtitle)
- [static let id3MetadataOriginalArtist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataoriginalartist)
- [static let id3MetadataOriginalFilename: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataoriginalfilename)
- [static let id3MetadataOriginalLyricist: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataoriginallyricist)
- [static let id3MetadataOriginalReleaseTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataoriginalreleasetime)
- [static let id3MetadataOriginalReleaseYear: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataoriginalreleaseyear)
- [static let id3MetadataOwnership: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataownership)
- [static let id3MetadataPartOfASet: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatapartofaset)
- [static let id3MetadataPayment: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatapayment)
- [static let id3MetadataPerformerSortOrder: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataperformersortorder)
- [static let id3MetadataPlayCounter: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataplaycounter)
- [static let id3MetadataPlaylistDelay: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataplaylistdelay)
- [static let id3MetadataPopularimeter: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatapopularimeter)
- [static let id3MetadataPositionSynchronization: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatapositionsynchronization)
- [static let id3MetadataPrivate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataprivate)
- [static let id3MetadataProducedNotice: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataproducednotice)
- [static let id3MetadataPublisher: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatapublisher)
- [static let id3MetadataRecommendedBufferSize: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatarecommendedbuffersize)
- [static let id3MetadataRecordingDates: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatarecordingdates)
- [static let id3MetadataRecordingTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatarecordingtime)
- [static let id3MetadataRelativeVolumeAdjustment: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatarelativevolumeadjustment)
- [static let id3MetadataRelativeVolumeAdjustment2: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatarelativevolumeadjustment2)
- [static let id3MetadataReleaseTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatareleasetime)
- [static let id3MetadataReverb: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatareverb)
- [static let id3MetadataSeek: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataseek)
- [static let id3MetadataSetSubtitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatasetsubtitle)
- [static let id3MetadataSignature: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatasignature)
- [static let id3MetadataSize: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatasize)
- [static let id3MetadataSubTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatasubtitle)
- [static let id3MetadataSynchronizedLyric: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatasynchronizedlyric)
- [static let id3MetadataSynchronizedTempoCodes: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatasynchronizedtempocodes)
- [static let id3MetadataTaggingTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatataggingtime)
- [static let id3MetadataTermsOfUse: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatatermsofuse)
- [static let id3MetadataTime: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatatime)
- [static let id3MetadataTitleDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatatitledescription)
- [static let id3MetadataTitleSortOrder: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatatitlesortorder)
- [static let id3MetadataTrackNumber: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatatracknumber)
- [static let id3MetadataUniqueFileIdentifier: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatauniquefileidentifier)
- [static let id3MetadataUnsynchronizedLyric: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadataunsynchronizedlyric)
- [static let id3MetadataUserText: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatausertext)
- [static let id3MetadataUserURL: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatauserurl)
- [static let id3MetadataYear: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatayear)
- [static let id3MetadataCommerical: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/id3metadatacommerical)

#### 3GP user metadata identifiers

- [static let identifier3GPUserDataAlbumAndTrack: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdataalbumandtrack)
- [static let identifier3GPUserDataAuthor: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdataauthor)
- [static let identifier3GPUserDataCollection: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatacollection)
- [static let identifier3GPUserDataCopyright: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatacopyright)
- [static let identifier3GPUserDataDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatadescription)
- [static let identifier3GPUserDataGenre: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatagenre)
- [static let identifier3GPUserDataKeywordList: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatakeywordlist)
- [static let identifier3GPUserDataLocation: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatalocation)
- [static let identifier3GPUserDataMediaClassification: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatamediaclassification)
- [static let identifier3GPUserDataMediaRating: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatamediarating)
- [static let identifier3GPUserDataPerformer: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdataperformer)
- [static let identifier3GPUserDataRecordingYear: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatarecordingyear)
- [static let identifier3GPUserDataThumbnail: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatathumbnail)
- [static let identifier3GPUserDataTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatatitle)
- [static let identifier3GPUserDataUserRating: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/identifier3gpuserdatauserrating)

#### ISO metadata identifiers

- [static let isoUserDataAccessibilityDescription: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/isouserdataaccessibilitydescription)
- [static let isoUserDataCopyright: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/isouserdatacopyright)
- [static let isoUserDataDate: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/isouserdatadate)
- [static let isoUserDataTaggedCharacteristic: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/isouserdatataggedcharacteristic)

#### ICY metadata identifiers

- [static let icyMetadataStreamTitle: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/icymetadatastreamtitle)
- [static let icyMetadataStreamURL: AVMetadataIdentifier](/documentation/avfoundation/avmetadataidentifier/icymetadatastreamurl)

#### Initializers

- [init(String)](/documentation/avfoundation/avmetadataidentifier/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avmetadataidentifier/init(rawvalue:))
- [AVMetadataKey](/documentation/avfoundation/avmetadatakey)

#### Common metadata keys

- [static let commonKeyAccessibilityDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyaccessibilitydescription)
- [static let commonKeyAlbumName: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyalbumname)
- [static let commonKeyArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyartist)
- [static let commonKeyArtwork: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyartwork)
- [static let commonKeyAuthor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyauthor)
- [static let commonKeyContributor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeycontributor)
- [static let commonKeyCopyrights: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeycopyrights)
- [static let commonKeyCreationDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeycreationdate)
- [static let commonKeyCreator: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeycreator)
- [static let commonKeyDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeydescription)
- [static let commonKeyFormat: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyformat)
- [static let commonKeyIdentifier: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyidentifier)
- [static let commonKeyLanguage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeylanguage)
- [static let commonKeyLastModifiedDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeylastmodifieddate)
- [static let commonKeyLocation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeylocation)
- [static let commonKeyMake: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeymake)
- [static let commonKeyModel: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeymodel)
- [static let commonKeyPublisher: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeypublisher)
- [static let commonKeyRelation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeyrelation)
- [static let commonKeySoftware: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeysoftware)
- [static let commonKeySource: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeysource)
- [static let commonKeySubject: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeysubject)
- [static let commonKeyTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeytitle)
- [static let commonKeyType: AVMetadataKey](/documentation/avfoundation/avmetadatakey/commonkeytype)

#### iTunes metadata keys

- [static let iTunesMetadataKeyAccountKind: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyaccountkind)
- [static let iTunesMetadataKeyAcknowledgement: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyacknowledgement)
- [static let iTunesMetadataKeyAlbum: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyalbum)
- [static let iTunesMetadataKeyAlbumArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyalbumartist)
- [static let iTunesMetadataKeyAppleID: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyappleid)
- [static let iTunesMetadataKeyArranger: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyarranger)
- [static let iTunesMetadataKeyArtDirector: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyartdirector)
- [static let iTunesMetadataKeyArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyartist)
- [static let iTunesMetadataKeyArtistID: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyartistid)
- [static let iTunesMetadataKeyAuthor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyauthor)
- [static let iTunesMetadataKeyBeatsPerMin: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeybeatspermin)
- [static let iTunesMetadataKeyComposer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeycomposer)
- [static let iTunesMetadataKeyConductor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyconductor)
- [static let iTunesMetadataKeyContentRating: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeycontentrating)
- [static let iTunesMetadataKeyCopyright: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeycopyright)
- [static let iTunesMetadataKeyCoverArt: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeycoverart)
- [static let iTunesMetadataKeyCredits: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeycredits)
- [static let iTunesMetadataKeyDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeydescription)
- [static let iTunesMetadataKeyDirector: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeydirector)
- [static let iTunesMetadataKeyDiscCompilation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeydisccompilation)
- [static let iTunesMetadataKeyDiscNumber: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeydiscnumber)
- [static let iTunesMetadataKeyEncodedBy: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyencodedby)
- [static let iTunesMetadataKeyEncodingTool: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyencodingtool)
- [static let iTunesMetadataKeyEQ: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyeq)
- [static let iTunesMetadataKeyExecProducer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyexecproducer)
- [static let iTunesMetadataKeyGenreID: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeygenreid)
- [static let iTunesMetadataKeyGrouping: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeygrouping)
- [static let iTunesMetadataKeyLinerNotes: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeylinernotes)
- [static let iTunesMetadataKeyLyrics: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeylyrics)
- [static let iTunesMetadataKeyOnlineExtras: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyonlineextras)
- [static let iTunesMetadataKeyOriginalArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyoriginalartist)
- [static let iTunesMetadataKeyPerformer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyperformer)
- [static let iTunesMetadataKeyPhonogramRights: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyphonogramrights)
- [static let iTunesMetadataKeyPlaylistID: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyplaylistid)
- [static let iTunesMetadataKeyPredefinedGenre: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeypredefinedgenre)
- [static let iTunesMetadataKeyProducer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyproducer)
- [static let iTunesMetadataKeyPublisher: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeypublisher)
- [static let iTunesMetadataKeyRecordCompany: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyrecordcompany)
- [static let iTunesMetadataKeyReleaseDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyreleasedate)
- [static let iTunesMetadataKeySoloist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeysoloist)
- [static let iTunesMetadataKeySongID: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeysongid)
- [static let iTunesMetadataKeySongName: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeysongname)
- [static let iTunesMetadataKeySoundEngineer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeysoundengineer)
- [static let iTunesMetadataKeyThanks: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeythanks)
- [static let iTunesMetadataKeyTrackNumber: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeytracknumber)
- [static let iTunesMetadataKeyTrackSubTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeytracksubtitle)
- [static let iTunesMetadataKeyUserComment: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyusercomment)
- [static let iTunesMetadataKeyUserGenre: AVMetadataKey](/documentation/avfoundation/avmetadatakey/itunesmetadatakeyusergenre)

#### QuickTime metadata keys

- [static let quickTimeMetadataKeyAccessibilityDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyaccessibilitydescription)
- [static let quickTimeMetadataKeyAlbum: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyalbum)
- [static let quickTimeMetadataKeyArranger: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyarranger)
- [static let quickTimeMetadataKeyArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyartist)
- [static let quickTimeMetadataKeyArtwork: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyartwork)
- [static let quickTimeMetadataKeyAuthor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyauthor)
- [static let quickTimeMetadataKeyCameraFocalLength35mmEquivalent: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycamerafocallength35mmequivalent)
- [static let quickTimeMetadataKeyCameraFrameReadoutTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycameraframereadouttime)
- [static let quickTimeMetadataKeyCameraISOSensitivity: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycameraisosensitivity)
- [static let quickTimeMetadataKeyCameraIdentifier: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycameraidentifier)
- [static let quickTimeMetadataKeyCameraLensIrisFNumber: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycameralensirisfnumber)
- [static let quickTimeMetadataKeyCameraLensModel: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycameralensmodel)
- [static let quickTimeMetadataKeyCameraShutterSpeedAngle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycamerashutterspeedangle)
- [static let quickTimeMetadataKeyCameraShutterSpeedTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycamerashutterspeedtime)
- [static let quickTimeMetadataKeyCameraWhiteBalance: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycamerawhitebalance)
- [static let quickTimeMetadataKeyCinematicVideoIntent: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycinematicvideointent)
- [static let quickTimeMetadataKeyCollectionUser: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycollectionuser)
- [static let quickTimeMetadataKeyComment: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycomment)
- [static let quickTimeMetadataKeyComposer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycomposer)
- [static let quickTimeMetadataKeyContentIdentifier: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycontentidentifier)
- [static let quickTimeMetadataKeyCopyright: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycopyright)
- [static let quickTimeMetadataKeyCreationDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycreationdate)
- [static let quickTimeMetadataKeyCredits: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeycredits)
- [static let quickTimeMetadataKeyDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeydescription)
- [static let quickTimeMetadataKeyDirectionFacing: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeydirectionfacing)
- [static let quickTimeMetadataKeyDirectionMotion: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeydirectionmotion)
- [static let quickTimeMetadataKeyDirector: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeydirector)
- [static let quickTimeMetadataKeyDisplayName: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeydisplayname)
- [static let quickTimeMetadataKeyEncodedBy: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyencodedby)
- [static let quickTimeMetadataKeyFullFrameRatePlaybackIntent: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyfullframerateplaybackintent)
- [static let quickTimeMetadataKeyGenre: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeygenre)
- [static let quickTimeMetadataKeyInformation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyinformation)
- [static let quickTimeMetadataKeyIsMontage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyismontage)
- [static let quickTimeMetadataKeyKeywords: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeykeywords)
- [static let quickTimeMetadataKeyLocationBody: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeylocationbody)
- [static let quickTimeMetadataKeyLocationDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeylocationdate)
- [static let quickTimeMetadataKeyLocationISO6709: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeylocationiso6709)
- [static let quickTimeMetadataKeyLocationName: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeylocationname)
- [static let quickTimeMetadataKeyLocationNote: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeylocationnote)
- [static let quickTimeMetadataKeyLocationRole: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeylocationrole)
- [static let quickTimeMetadataKeyMake: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeymake)
- [static let quickTimeMetadataKeyModel: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeymodel)
- [static let quickTimeMetadataKeyOriginalArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyoriginalartist)
- [static let quickTimeMetadataKeyPerformer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyperformer)
- [static let quickTimeMetadataKeyPhonogramRights: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyphonogramrights)
- [static let quickTimeMetadataKeyProducer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyproducer)
- [static let quickTimeMetadataKeyPublisher: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeypublisher)
- [static let quickTimeMetadataKeyRatingUser: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyratinguser)
- [static let quickTimeMetadataKeySoftware: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeysoftware)
- [static let quickTimeMetadataKeyTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeytitle)
- [static let quickTimeMetadataKeyWhiteBalanceByCCTColorMatrices: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeywhitebalancebycctcolormatrices)
- [static let quickTimeMetadataKeyWhiteBalanceByCCTWhiteBalanceFactors: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeywhitebalancebycctwhitebalancefactors)
- [static let quickTimeMetadataKeyYear: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyyear)
- [static let quickTimeMetadataKeyiXML: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimemetadatakeyixml)

#### QuickTime user metadata keys

- [static let quickTimeUserDataKeyAccessibilityDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyaccessibilitydescription)
- [static let quickTimeUserDataKeyAlbum: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyalbum)
- [static let quickTimeUserDataKeyArranger: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyarranger)
- [static let quickTimeUserDataKeyArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyartist)
- [static let quickTimeUserDataKeyAuthor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyauthor)
- [static let quickTimeUserDataKeyChapter: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeychapter)
- [static let quickTimeUserDataKeyComment: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeycomment)
- [static let quickTimeUserDataKeyComposer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeycomposer)
- [static let quickTimeUserDataKeyCopyright: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeycopyright)
- [static let quickTimeUserDataKeyCreationDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeycreationdate)
- [static let quickTimeUserDataKeyCredits: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeycredits)
- [static let quickTimeUserDataKeyDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeydescription)
- [static let quickTimeUserDataKeyDirector: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeydirector)
- [static let quickTimeUserDataKeyDisclaimer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeydisclaimer)
- [static let quickTimeUserDataKeyEncodedBy: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyencodedby)
- [static let quickTimeUserDataKeyFullName: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyfullname)
- [static let quickTimeUserDataKeyGenre: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeygenre)
- [static let quickTimeUserDataKeyHostComputer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyhostcomputer)
- [static let quickTimeUserDataKeyInformation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyinformation)
- [static let quickTimeUserDataKeyKeywords: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeykeywords)
- [static let quickTimeUserDataKeyLocationISO6709: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeylocationiso6709)
- [static let quickTimeUserDataKeyMake: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeymake)
- [static let quickTimeUserDataKeyModel: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeymodel)
- [static let quickTimeUserDataKeyOriginalArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyoriginalartist)
- [static let quickTimeUserDataKeyOriginalFormat: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyoriginalformat)
- [static let quickTimeUserDataKeyOriginalSource: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyoriginalsource)
- [static let quickTimeUserDataKeyPerformers: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyperformers)
- [static let quickTimeUserDataKeyPhonogramRights: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyphonogramrights)
- [static let quickTimeUserDataKeyProducer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyproducer)
- [static let quickTimeUserDataKeyProduct: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyproduct)
- [static let quickTimeUserDataKeyPublisher: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeypublisher)
- [static let quickTimeUserDataKeySoftware: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeysoftware)
- [static let quickTimeUserDataKeySpecialPlaybackRequirements: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyspecialplaybackrequirements)
- [static let quickTimeUserDataKeyTaggedCharacteristic: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeytaggedcharacteristic)
- [static let quickTimeUserDataKeyTrack: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeytrack)
- [static let quickTimeUserDataKeyTrackName: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeytrackname)
- [static let quickTimeUserDataKeyURLLink: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeyurllink)
- [static let quickTimeUserDataKeyWarning: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeywarning)
- [static let quickTimeUserDataKeyWriter: AVMetadataKey](/documentation/avfoundation/avmetadatakey/quicktimeuserdatakeywriter)

#### ID3 metadata keys

- [static let id3MetadataKeyAlbumSortOrder: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyalbumsortorder)
- [static let id3MetadataKeyAlbumTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyalbumtitle)
- [static let id3MetadataKeyAttachedPicture: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyattachedpicture)
- [static let id3MetadataKeyAudioEncryption: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyaudioencryption)
- [static let id3MetadataKeyAudioSeekPointIndex: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyaudioseekpointindex)
- [static let id3MetadataKeyBand: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyband)
- [static let id3MetadataKeyBeatsPerMinute: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeybeatsperminute)
- [static let id3MetadataKeyComments: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycomments)
- [static let id3MetadataKeyCommercial: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycommercial)
- [static let id3MetadataKeyCommercialInformation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycommercialinformation)
- [static let id3MetadataKeyComposer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycomposer)
- [static let id3MetadataKeyConductor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyconductor)
- [static let id3MetadataKeyContentGroupDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycontentgroupdescription)
- [static let id3MetadataKeyContentType: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycontenttype)
- [static let id3MetadataKeyCopyright: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycopyright)
- [static let id3MetadataKeyCopyrightInformation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycopyrightinformation)
- [static let id3MetadataKeyDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeydate)
- [static let id3MetadataKeyEncodedBy: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyencodedby)
- [static let id3MetadataKeyEncodedWith: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyencodedwith)
- [static let id3MetadataKeyEncodingTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyencodingtime)
- [static let id3MetadataKeyEncryption: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyencryption)
- [static let id3MetadataKeyEqualization: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyequalization)
- [static let id3MetadataKeyEqualization2: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyequalization2)
- [static let id3MetadataKeyEventTimingCodes: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyeventtimingcodes)
- [static let id3MetadataKeyFileOwner: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyfileowner)
- [static let id3MetadataKeyFileType: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyfiletype)
- [static let id3MetadataKeyGeneralEncapsulatedObject: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeygeneralencapsulatedobject)
- [static let id3MetadataKeyGroupIdentifier: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeygroupidentifier)
- [static let id3MetadataKeyInitialKey: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyinitialkey)
- [static let id3MetadataKeyInternationalStandardRecordingCode: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyinternationalstandardrecordingcode)
- [static let id3MetadataKeyInternetRadioStationName: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyinternetradiostationname)
- [static let id3MetadataKeyInternetRadioStationOwner: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyinternetradiostationowner)
- [static let id3MetadataKeyInvolvedPeopleList_v23: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyinvolvedpeoplelist_v23)
- [static let id3MetadataKeyInvolvedPeopleList_v24: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyinvolvedpeoplelist_v24)
- [static let id3MetadataKeyLanguage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeylanguage)
- [static let id3MetadataKeyLeadPerformer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyleadperformer)
- [static let id3MetadataKeyLength: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeylength)
- [static let id3MetadataKeyLink: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeylink)
- [static let id3MetadataKeyLyricist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeylyricist)
- [static let id3MetadataKeyMediaType: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeymediatype)
- [static let id3MetadataKeyModifiedBy: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeymodifiedby)
- [static let id3MetadataKeyMood: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeymood)
- [static let id3MetadataKeyMPEGLocationLookupTable: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeympeglocationlookuptable)
- [static let id3MetadataKeyMusicCDIdentifier: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeymusiccdidentifier)
- [static let id3MetadataKeyMusicianCreditsList: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeymusiciancreditslist)
- [static let id3MetadataKeyOfficialArtistWebpage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyofficialartistwebpage)
- [static let id3MetadataKeyOfficialAudioFileWebpage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyofficialaudiofilewebpage)
- [static let id3MetadataKeyOfficialAudioSourceWebpage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyofficialaudiosourcewebpage)
- [static let id3MetadataKeyOfficialInternetRadioStationHomepage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyofficialinternetradiostationhomepage)
- [static let id3MetadataKeyOfficialPublisherWebpage: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyofficialpublisherwebpage)
- [static let id3MetadataKeyOriginalAlbumTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyoriginalalbumtitle)
- [static let id3MetadataKeyOriginalArtist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyoriginalartist)
- [static let id3MetadataKeyOriginalFilename: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyoriginalfilename)
- [static let id3MetadataKeyOriginalLyricist: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyoriginallyricist)
- [static let id3MetadataKeyOriginalReleaseTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyoriginalreleasetime)
- [static let id3MetadataKeyOriginalReleaseYear: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyoriginalreleaseyear)
- [static let id3MetadataKeyOwnership: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyownership)
- [static let id3MetadataKeyPartOfASet: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeypartofaset)
- [static let id3MetadataKeyPayment: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeypayment)
- [static let id3MetadataKeyPerformerSortOrder: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyperformersortorder)
- [static let id3MetadataKeyPlayCounter: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyplaycounter)
- [static let id3MetadataKeyPlaylistDelay: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyplaylistdelay)
- [static let id3MetadataKeyPopularimeter: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeypopularimeter)
- [static let id3MetadataKeyPositionSynchronization: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeypositionsynchronization)
- [static let id3MetadataKeyPrivate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyprivate)
- [static let id3MetadataKeyProducedNotice: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyproducednotice)
- [static let id3MetadataKeyPublisher: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeypublisher)
- [static let id3MetadataKeyRecommendedBufferSize: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyrecommendedbuffersize)
- [static let id3MetadataKeyRecordingDates: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyrecordingdates)
- [static let id3MetadataKeyRecordingTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyrecordingtime)
- [static let id3MetadataKeyRelativeVolumeAdjustment: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyrelativevolumeadjustment)
- [static let id3MetadataKeyRelativeVolumeAdjustment2: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyrelativevolumeadjustment2)
- [static let id3MetadataKeyReleaseTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyreleasetime)
- [static let id3MetadataKeyReverb: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyreverb)
- [static let id3MetadataKeySeek: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyseek)
- [static let id3MetadataKeySetSubtitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeysetsubtitle)
- [static let id3MetadataKeySignature: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeysignature)
- [static let id3MetadataKeySize: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeysize)
- [static let id3MetadataKeySubTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeysubtitle)
- [static let id3MetadataKeySynchronizedLyric: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeysynchronizedlyric)
- [static let id3MetadataKeySynchronizedTempoCodes: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeysynchronizedtempocodes)
- [static let id3MetadataKeyTaggingTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeytaggingtime)
- [static let id3MetadataKeyTermsOfUse: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeytermsofuse)
- [static let id3MetadataKeyTime: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeytime)
- [static let id3MetadataKeyTitleDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeytitledescription)
- [static let id3MetadataKeyTitleSortOrder: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeytitlesortorder)
- [static let id3MetadataKeyTrackNumber: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeytracknumber)
- [static let id3MetadataKeyUniqueFileIdentifier: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyuniquefileidentifier)
- [static let id3MetadataKeyUnsynchronizedLyric: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyunsynchronizedlyric)
- [static let id3MetadataKeyUserText: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyusertext)
- [static let id3MetadataKeyUserURL: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyuserurl)
- [static let id3MetadataKeyYear: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeyyear)
- [static let id3MetadataKeyCommerical: AVMetadataKey](/documentation/avfoundation/avmetadatakey/id3metadatakeycommerical)

#### 3GP user metadata keys

- [static let metadata3GPUserDataKeyAlbumAndTrack: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeyalbumandtrack)
- [static let metadata3GPUserDataKeyAuthor: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeyauthor)
- [static let metadata3GPUserDataKeyCollection: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeycollection)
- [static let metadata3GPUserDataKeyCopyright: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeycopyright)
- [static let metadata3GPUserDataKeyDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeydescription)
- [static let metadata3GPUserDataKeyGenre: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeygenre)
- [static let metadata3GPUserDataKeyKeywordList: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeykeywordlist)
- [static let metadata3GPUserDataKeyLocation: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeylocation)
- [static let metadata3GPUserDataKeyMediaClassification: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeymediaclassification)
- [static let metadata3GPUserDataKeyMediaRating: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeymediarating)
- [static let metadata3GPUserDataKeyPerformer: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeyperformer)
- [static let metadata3GPUserDataKeyRecordingYear: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeyrecordingyear)
- [static let metadata3GPUserDataKeyThumbnail: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeythumbnail)
- [static let metadata3GPUserDataKeyTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeytitle)
- [static let metadata3GPUserDataKeyUserRating: AVMetadataKey](/documentation/avfoundation/avmetadatakey/metadata3gpuserdatakeyuserrating)

#### ISO user metadata keys

- [static let isoUserDataKeyAccessibilityDescription: AVMetadataKey](/documentation/avfoundation/avmetadatakey/isouserdatakeyaccessibilitydescription)
- [static let isoUserDataKeyCopyright: AVMetadataKey](/documentation/avfoundation/avmetadatakey/isouserdatakeycopyright)
- [static let isoUserDataKeyDate: AVMetadataKey](/documentation/avfoundation/avmetadatakey/isouserdatakeydate)
- [static let isoUserDataKeyTaggedCharacteristic: AVMetadataKey](/documentation/avfoundation/avmetadatakey/isouserdatakeytaggedcharacteristic)

#### ICY metadata keys

- [static let icyMetadataKeyStreamTitle: AVMetadataKey](/documentation/avfoundation/avmetadatakey/icymetadatakeystreamtitle)
- [static let icyMetadataKeyStreamURL: AVMetadataKey](/documentation/avfoundation/avmetadatakey/icymetadatakeystreamurl)

#### Initializers

- [init(String)](/documentation/avfoundation/avmetadatakey/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avmetadatakey/init(rawvalue:))
- [AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace)

#### Common key space

- [static let common: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/common)

#### Format-specific key spaces

- [static let audioFile: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/audiofile)
- [static let hlsDateRange: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/hlsdaterange)
- [static let iTunes: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/itunes)
- [static let icy: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/icy)
- [static let id3: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/id3)
- [static let isoUserData: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/isouserdata)
- [static let quickTimeMetadata: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/quicktimemetadata)
- [static let quickTimeUserData: AVMetadataKeySpace](/documentation/avfoundation/avmetadatakeyspace/quicktimeuserdata)

#### Initializers

- [init(String)](/documentation/avfoundation/avmetadatakeyspace/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avmetadatakeyspace/init(rawvalue:))
- [AVMetadataExtraAttributeKey](/documentation/avfoundation/avmetadataextraattributekey)

#### Extra attribute keys

- [static let valueURI: AVMetadataExtraAttributeKey](/documentation/avfoundation/avmetadataextraattributekey/valueuri)
- [static let baseURI: AVMetadataExtraAttributeKey](/documentation/avfoundation/avmetadataextraattributekey/baseuri)
- [static let info: AVMetadataExtraAttributeKey](/documentation/avfoundation/avmetadataextraattributekey/info)

#### Initializers

- [init(String)](/documentation/avfoundation/avmetadataextraattributekey/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avmetadataextraattributekey/init(rawvalue:))
- [AVMetadataFormat](/documentation/avfoundation/avmetadataformat)

#### Metadata formats

- [static let hlsMetadata: AVMetadataFormat](/documentation/avfoundation/avmetadataformat/hlsmetadata)
- [static let iTunesMetadata: AVMetadataFormat](/documentation/avfoundation/avmetadataformat/itunesmetadata)
- [static let id3Metadata: AVMetadataFormat](/documentation/avfoundation/avmetadataformat/id3metadata)
- [static let isoUserData: AVMetadataFormat](/documentation/avfoundation/avmetadataformat/isouserdata)
- [static let quickTimeMetadata: AVMetadataFormat](/documentation/avfoundation/avmetadataformat/quicktimemetadata)
- [static let quickTimeUserData: AVMetadataFormat](/documentation/avfoundation/avmetadataformat/quicktimeuserdata)
- [static let unknown: AVMetadataFormat](/documentation/avfoundation/avmetadataformat/unknown)

#### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avmetadataformat/init(rawvalue:))
- [AVMetadataItemFilter](/documentation/avfoundation/avmetadataitemfilter)

#### Creating a metadata item filter

- [class func forSharing() -> AVMetadataItemFilter](/documentation/avfoundation/avmetadataitemfilter/forsharing())

### Property loading

- [AVAsynchronousKeyValueLoading](/documentation/avfoundation/avasynchronouskeyvalueloading)

#### Loading property values

- [func load<T>(AVAsyncProperty<Self, T>, isolation: isolated (any Actor)?) async throws -> T](/documentation/avfoundation/avasynchronouskeyvalueloading/load(_:isolation:))
- [func load<A, B, each C>(AVAsyncProperty<Self, A>, AVAsyncProperty<Self, B>, repeat AVAsyncProperty<Self, each C>, isolation: isolated (any Actor)?) async throws -> (A, B, repeat each C)](/documentation/avfoundation/avasynchronouskeyvalueloading/load(_:_:_:isolation:))

#### Determining the loaded status

- [func status<T>(of: AVAsyncProperty<Self, T>) -> AVAsyncProperty<Self, T>.Status](/documentation/avfoundation/avasynchronouskeyvalueloading/status(of:))

#### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avasynchronouskeyvalueloading-deprecated-symbols)

##### Loading property values

- [func loadValuesAsynchronously(forKeys: [String], completionHandler: (() -> Void)?)](/documentation/avfoundation/avasynchronouskeyvalueloading/loadvaluesasynchronously(forkeys:completionhandler:))
- [func statusOfValue(forKey: String, error: NSErrorPointer) -> AVKeyValueStatus](/documentation/avfoundation/avasynchronouskeyvalueloading/statusofvalue(forkey:error:))
- [AVKeyValueStatus](/documentation/avfoundation/avkeyvaluestatus)

###### Status values

- [case unknown](/documentation/avfoundation/avkeyvaluestatus/unknown)
- [case loading](/documentation/avfoundation/avkeyvaluestatus/loading)
- [case loaded](/documentation/avfoundation/avkeyvaluestatus/loaded)
- [case failed](/documentation/avfoundation/avkeyvaluestatus/failed)
- [case cancelled](/documentation/avfoundation/avkeyvaluestatus/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avkeyvaluestatus/init(rawvalue:))
- [func loadValuesAsynchronously(forKeys: [String], completionHandler: (() -> Void)?)](/documentation/avfoundation/avasynchronouskeyvalueloading/loadvaluesasynchronously(forkeys:completionhandler:))
- [func statusOfValue(forKey: String, error: NSErrorPointer) -> AVKeyValueStatus](/documentation/avfoundation/avasynchronouskeyvalueloading/statusofvalue(forkey:error:))
- [AVKeyValueStatus](/documentation/avfoundation/avkeyvaluestatus)

##### Status values

- [case unknown](/documentation/avfoundation/avkeyvaluestatus/unknown)
- [case loading](/documentation/avfoundation/avkeyvaluestatus/loading)
- [case loaded](/documentation/avfoundation/avkeyvaluestatus/loaded)
- [case failed](/documentation/avfoundation/avkeyvaluestatus/failed)
- [case cancelled](/documentation/avfoundation/avkeyvaluestatus/cancelled)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avkeyvaluestatus/init(rawvalue:))
- [AVAsyncProperty](/documentation/avfoundation/avasyncproperty)

#### Accessing the status

- [AVAsyncProperty.Status](/documentation/avfoundation/avasyncproperty/status)

##### Status values

- [case notYetLoaded](/documentation/avfoundation/avasyncproperty/status/notyetloaded)
- [case loading](/documentation/avfoundation/avasyncproperty/status/loading)
- [case loaded(Value)](/documentation/avfoundation/avasyncproperty/status/loaded(_:))
- [case failed(NSError)](/documentation/avfoundation/avasyncproperty/status/failed(_:))
- [AVPartialAsyncProperty](/documentation/avfoundation/avpartialasyncproperty)

#### Loading properties

- [AVAsset](/documentation/avfoundation/avasset-async-properties)

##### Loading duration and timing

- [static var duration: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/duration)
- [static var providesPreciseDurationAndTiming: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/providesprecisedurationandtiming)
- [static var minimumTimeOffsetFromLive: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/minimumtimeoffsetfromlive)

##### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVAssetTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-48zyw)

##### Loading track groups

- [static var trackGroups: AVAsyncProperty<Root, [AVAssetTrackGroup]>](/documentation/avfoundation/avpartialasyncproperty/trackgroups)

##### Loading metadata

- [static var metadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/metadata-16qej)
- [static var commonMetadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/commonmetadata-3j3n4)
- [static var availableMetadataFormats: AVAsyncProperty<Root, [AVMetadataFormat]>](/documentation/avfoundation/avpartialasyncproperty/availablemetadataformats-4yiq8)
- [static var creationDate: AVAsyncProperty<Root, AVMetadataItem?>](/documentation/avfoundation/avpartialasyncproperty/creationdate)
- [static var lyrics: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/lyrics)

##### Loading suitability

- [static var isPlayable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isplayable-45h5v)
- [static var isExportable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isexportable)
- [static var isReadable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isreadable)
- [static var isComposable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/iscomposable)
- [static var isCompatibleWithSavedPhotosAlbum: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/iscompatiblewithsavedphotosalbum)
- [static var isCompatibleWithAirPlayVideo: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/iscompatiblewithairplayvideo)

##### Loading asset preferences

- [static var preferredRate: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/preferredrate)
- [static var preferredTransform: AVAsyncProperty<Root, CGAffineTransform>](/documentation/avfoundation/avpartialasyncproperty/preferredtransform-80d13)
- [static var preferredVolume: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/preferredvolume-20mb3)
- [static var preferredDisplayCriteria: AVAsyncProperty<Root, AVDisplayCriteria>](/documentation/avfoundation/avpartialasyncproperty/preferreddisplaycriteria)

##### Loading media selections

- [static var allMediaSelections: AVAsyncProperty<Root, [AVMediaSelection]>](/documentation/avfoundation/avpartialasyncproperty/allmediaselections)
- [static var preferredMediaSelection: AVAsyncProperty<Root, AVMediaSelection>](/documentation/avfoundation/avpartialasyncproperty/preferredmediaselection)
- [static var availableMediaCharacteristicsWithMediaSelectionOptions: AVAsyncProperty<Root, [AVMediaCharacteristic]>](/documentation/avfoundation/avpartialasyncproperty/availablemediacharacteristicswithmediaselectionoptions)

##### Loading chapter metadata

- [static var availableChapterLocales: AVAsyncProperty<Root, [Locale]>](/documentation/avfoundation/avpartialasyncproperty/availablechapterlocales)

##### Loading content protections

- [static var hasProtectedContent: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/hasprotectedcontent)

##### Loading fragment support

- [static var canContainFragments: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/cancontainfragments)
- [static var containsFragments: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/containsfragments)
- [static var overallDurationHint: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/overalldurationhint)
- [AVAssetTrack](/documentation/avfoundation/avassettrack-async-properties)

##### Loading track information

- [static var totalSampleDataLength: AVAsyncProperty<Root, Int64>](/documentation/avfoundation/avpartialasyncproperty/totalsampledatalength)
- [static var formatDescriptions: AVAsyncProperty<Root, [CMFormatDescription]>](/documentation/avfoundation/avpartialasyncproperty/formatdescriptions)
- [static var isDecodable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isdecodable)
- [static var isEnabled: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isenabled)
- [static var isPlayable: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isplayable-6txa5)
- [static var mediaCharacteristics: AVAsyncProperty<Root, [AVMediaCharacteristic]>](/documentation/avfoundation/avpartialasyncproperty/mediacharacteristics)
- [static var isSelfContained: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/isselfcontained)

##### Loading temporal information

- [static var timeRange: AVAsyncProperty<Root, CMTimeRange>](/documentation/avfoundation/avpartialasyncproperty/timerange)
- [static var naturalTimeScale: AVAsyncProperty<Root, CMTimeScale>](/documentation/avfoundation/avpartialasyncproperty/naturaltimescale)
- [static var estimatedDataRate: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/estimateddatarate)

##### Loading language support

- [static var languageCode: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/languagecode)
- [static var extendedLanguageTag: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/extendedlanguagetag)

##### Loading visual characteristics

- [static var naturalSize: AVAsyncProperty<Root, CGSize>](/documentation/avfoundation/avpartialasyncproperty/naturalsize)
- [static var preferredTransform: AVAsyncProperty<Root, CGAffineTransform>](/documentation/avfoundation/avpartialasyncproperty/preferredtransform-90jdn)

##### Loading audible characteristics

- [static var preferredVolume: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/preferredvolume-8q2yt)
- [static var hasAudioSampleDependencies: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/hasaudiosampledependencies)

##### Loading frame-based characteristics

- [static var nominalFrameRate: AVAsyncProperty<Root, Float>](/documentation/avfoundation/avpartialasyncproperty/nominalframerate)
- [static var minFrameDuration: AVAsyncProperty<Root, CMTime>](/documentation/avfoundation/avpartialasyncproperty/minframeduration)
- [static var requiresFrameReordering: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/requiresframereordering)

##### Loading metadata

- [static var metadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/metadata-6e14c)
- [static var availableMetadataFormats: AVAsyncProperty<Root, [AVMetadataFormat]>](/documentation/avfoundation/avpartialasyncproperty/availablemetadataformats-5p9xg)
- [static var commonMetadata: AVAsyncProperty<Root, [AVMetadataItem]>](/documentation/avfoundation/avpartialasyncproperty/commonmetadata-73m58)

##### Loading track segments

- [static var segments: AVAsyncProperty<Root, [AVAssetTrackSegment]>](/documentation/avfoundation/avpartialasyncproperty/segments)

##### Loading track associations

- [static var availableTrackAssociationTypes: AVAsyncProperty<Root, [AVAssetTrack.AssociationType]>](/documentation/avfoundation/avpartialasyncproperty/availabletrackassociationtypes)

##### Creating sample cursors

- [static var canProvideSampleCursors: AVAsyncProperty<Root, Bool>](/documentation/avfoundation/avpartialasyncproperty/canprovidesamplecursors)
- [AVURLAsset](/documentation/avfoundation/avurlasset-async-properties)

##### Loading tracks and variants

- [static var tracks: AVAsyncProperty<Root, [AVAssetTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-44ptx)
- [static var variants: AVAsyncProperty<Root, [AVAssetVariant]>](/documentation/avfoundation/avpartialasyncproperty/variants)
- [AVFragmentedAsset](/documentation/avfoundation/avfragmentedasset-async-properties)

##### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVFragmentedAssetTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-9z3j9)
- [AVMetadataItem](/documentation/avfoundation/avmetadataitem-async-properties)

##### Loading values

- [static var value: AVAsyncProperty<Root, (any NSCopying & NSObjectProtocol)?>](/documentation/avfoundation/avpartialasyncproperty/value)
- [static var extraAttributes: AVAsyncProperty<Root, [AVMetadataExtraAttributeKey : Any]?>](/documentation/avfoundation/avpartialasyncproperty/extraattributes)
- [static var stringValue: AVAsyncProperty<Root, String?>](/documentation/avfoundation/avpartialasyncproperty/stringvalue)
- [static var numberValue: AVAsyncProperty<Root, NSNumber?>](/documentation/avfoundation/avpartialasyncproperty/numbervalue)
- [static var dateValue: AVAsyncProperty<Root, Date?>](/documentation/avfoundation/avpartialasyncproperty/datevalue)
- [static var dataValue: AVAsyncProperty<Root, Data?>](/documentation/avfoundation/avpartialasyncproperty/datavalue)
- [AVComposition](/documentation/avfoundation/avcomposition-async-properties)

##### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVCompositionTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-9eows)
- [AVMutableComposition](/documentation/avfoundation/avmutablecomposition-async-properties)

##### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVMutableCompositionTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-92p4a)
- [AVMovie](/documentation/avfoundation/avmovie-async-properties)

##### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVMovieTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-80a83)
- [AVMutableMovie](/documentation/avfoundation/avmutablemovie-async-properties)

##### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVMutableMovieTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-2lj40)
- [AVFragmentedMovie](/documentation/avfoundation/avfragmentedmovie-async-properties)

##### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVFragmentedMovieTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-7fr6q)

#### Describing a property

- [var description: String](/documentation/avfoundation/avpartialasyncproperty/description)
- [static var sidecarURL: AVAsyncProperty<Root, URL?>](/documentation/avfoundation/avpartialasyncproperty/sidecarurl)
- [AVAnyAsyncProperty](/documentation/avfoundation/avanyasyncproperty)

### Fragmented assets

- [AVFragmentedAsset](/documentation/avfoundation/avfragmentedasset)

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVFragmentedAssetTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-9z3j9)
- [func loadTrack(withTrackID: CMPersistentTrackID, completionHandler: (AVFragmentedAssetTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avfragmentedasset/loadtrack(withtrackid:completionhandler:))
- [func loadTracks(withMediaType: AVMediaType, completionHandler: ([AVFragmentedAssetTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avfragmentedasset/loadtracks(withmediatype:completionhandler:))
- [func loadTracks(withMediaCharacteristic: AVMediaCharacteristic, completionHandler: ([AVFragmentedAssetTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avfragmentedasset/loadtracks(withmediacharacteristic:completionhandler:))

#### Accessing tracks

- [var tracks: [AVFragmentedAssetTrack]](/documentation/avfoundation/avfragmentedasset/tracks)
- [func track(withTrackID: CMPersistentTrackID) -> AVFragmentedAssetTrack?](/documentation/avfoundation/avfragmentedasset/track(withtrackid:))
- [func tracks(withMediaType: AVMediaType) -> [AVFragmentedAssetTrack]](/documentation/avfoundation/avfragmentedasset/tracks(withmediatype:))
- [func tracks(withMediaCharacteristic: AVMediaCharacteristic) -> [AVFragmentedAssetTrack]](/documentation/avfoundation/avfragmentedasset/tracks(withmediacharacteristic:))
- [AVFragmentedAssetTrack](/documentation/avfoundation/avfragmentedassettrack)
- [AVFragmentedAssetMinder](/documentation/avfoundation/avfragmentedassetminder)

#### Creating an asset minder

- [init(asset: any AVAsset & AVFragmentMinding, mindingInterval: TimeInterval)](/documentation/avfoundation/avfragmentedassetminder/init(asset:mindinginterval:))

#### Configuring the minding interval

- [var mindingInterval: TimeInterval](/documentation/avfoundation/avfragmentedassetminder/mindinginterval)

#### Inspecting a fragment asset

- [var assets: [any AVAsset & AVFragmentMinding]](/documentation/avfoundation/avfragmentedassetminder/assets)

#### Adding and removing fragmented assets

- [func addFragmentedAsset(any AVAsset & AVFragmentMinding)](/documentation/avfoundation/avfragmentedassetminder/addfragmentedasset(_:))
- [func removeFragmentedAsset(any AVAsset & AVFragmentMinding)](/documentation/avfoundation/avfragmentedassetminder/removefragmentedasset(_:))
- [AVFragmentMinding](/documentation/avfoundation/avfragmentminding)

#### Fragment minder association

- [var isAssociatedWithFragmentMinder: Bool](/documentation/avfoundation/avfragmentminding/isassociatedwithfragmentminder)
- [Media reading and writing](/documentation/avfoundation/media-reading-and-writing)

### Media export

- [Exporting video to alternative formats](/documentation/avfoundation/exporting-video-to-alternative-formats)
- [AVAssetExportSession](/documentation/avfoundation/avassetexportsession)

#### Creating an export session

- [init?(asset: AVAsset, presetName: String)](/documentation/avfoundation/avassetexportsession/init(asset:presetname:))
- [Export presets](/documentation/avfoundation/export-presets)

##### Quality presets

- [let AVAssetExportPresetLowQuality: String](/documentation/avfoundation/avassetexportpresetlowquality)
- [let AVAssetExportPresetMediumQuality: String](/documentation/avfoundation/avassetexportpresetmediumquality)
- [let AVAssetExportPresetHighestQuality: String](/documentation/avfoundation/avassetexportpresethighestquality)
- [let AVAssetExportPresetHEVCHighestQuality: String](/documentation/avfoundation/avassetexportpresethevchighestquality)
- [let AVAssetExportPresetHEVCHighestQualityWithAlpha: String](/documentation/avfoundation/avassetexportpresethevchighestqualitywithalpha)

##### Size presets

- [let AVAssetExportPreset640x480: String](/documentation/avfoundation/avassetexportpreset640x480)
- [let AVAssetExportPreset960x540: String](/documentation/avfoundation/avassetexportpreset960x540)
- [let AVAssetExportPreset1280x720: String](/documentation/avfoundation/avassetexportpreset1280x720)
- [let AVAssetExportPreset1920x1080: String](/documentation/avfoundation/avassetexportpreset1920x1080)
- [let AVAssetExportPreset3840x2160: String](/documentation/avfoundation/avassetexportpreset3840x2160)

##### HEVC size presets

- [let AVAssetExportPresetHEVC1920x1080: String](/documentation/avfoundation/avassetexportpresethevc1920x1080)
- [let AVAssetExportPresetHEVC3840x2160: String](/documentation/avfoundation/avassetexportpresethevc3840x2160)
- [let AVAssetExportPresetHEVC1920x1080WithAlpha: String](/documentation/avfoundation/avassetexportpresethevc1920x1080withalpha)
- [let AVAssetExportPresetHEVC3840x2160WithAlpha: String](/documentation/avfoundation/avassetexportpresethevc3840x2160withalpha)
- [let AVAssetExportPresetHEVC4320x2160: String](/documentation/avfoundation/avassetexportpresethevc4320x2160)
- [let AVAssetExportPresetHEVC7680x4320: String](/documentation/avfoundation/avassetexportpresethevc7680x4320)

##### MV-HEVC presets

- [let AVAssetExportPresetMVHEVC960x960: String](/documentation/avfoundation/avassetexportpresetmvhevc960x960)
- [let AVAssetExportPresetMVHEVC1440x1440: String](/documentation/avfoundation/avassetexportpresetmvhevc1440x1440)
- [let AVAssetExportPresetMVHEVC4320x4320: String](/documentation/avfoundation/avassetexportpresetmvhevc4320x4320)
- [let AVAssetExportPresetMVHEVC7680x7680: String](/documentation/avfoundation/avassetexportpresetmvhevc7680x7680)

##### M4V presets

- [let AVAssetExportPresetAppleM4V480pSD: String](/documentation/avfoundation/avassetexportpresetapplem4v480psd)
- [let AVAssetExportPresetAppleM4V720pHD: String](/documentation/avfoundation/avassetexportpresetapplem4v720phd)
- [let AVAssetExportPresetAppleM4V1080pHD: String](/documentation/avfoundation/avassetexportpresetapplem4v1080phd)
- [let AVAssetExportPresetAppleM4ViPod: String](/documentation/avfoundation/avassetexportpresetapplem4vipod)
- [let AVAssetExportPresetAppleM4VAppleTV: String](/documentation/avfoundation/avassetexportpresetapplem4vappletv)
- [let AVAssetExportPresetAppleM4VCellular: String](/documentation/avfoundation/avassetexportpresetapplem4vcellular)
- [let AVAssetExportPresetAppleM4VWiFi: String](/documentation/avfoundation/avassetexportpresetapplem4vwifi)

##### Apple ProRes presets

- [let AVAssetExportPresetAppleProRes422LPCM: String](/documentation/avfoundation/avassetexportpresetappleprores422lpcm)
- [let AVAssetExportPresetAppleProRes4444LPCM: String](/documentation/avfoundation/avassetexportpresetappleprores4444lpcm)

##### Passthrough presets

- [let AVAssetExportPresetPassthrough: String](/documentation/avfoundation/avassetexportpresetpassthrough)

##### Audio-only presets

- [let AVAssetExportPresetAppleM4A: String](/documentation/avfoundation/avassetexportpresetapplem4a)

#### Accessing export presets

- [var presetName: String](/documentation/avfoundation/avassetexportsession/presetname)
- [func determineCompatibleFileTypes(completionHandler: ([AVFileType]) -> Void)](/documentation/avfoundation/avassetexportsession/determinecompatiblefiletypes(completionhandler:))
- [class func allExportPresets() -> [String]](/documentation/avfoundation/avassetexportsession/allexportpresets())
- [class func determineCompatibility(ofExportPreset: String, with: AVAsset, outputFileType: AVFileType?, completionHandler: (Bool) -> Void)](/documentation/avfoundation/avassetexportsession/determinecompatibility(ofexportpreset:with:outputfiletype:completionhandler:))
- [class func exportPresets(compatibleWith: AVAsset) -> [String]](/documentation/avfoundation/avassetexportsession/exportpresets(compatiblewith:))

#### Configuring output

- [var outputURL: URL?](/documentation/avfoundation/avassetexportsession/outputurl)
- [var outputFileType: AVFileType?](/documentation/avfoundation/avassetexportsession/outputfiletype)
- [var supportedFileTypes: [AVFileType]](/documentation/avfoundation/avassetexportsession/supportedfiletypes)
- [var allowsParallelizedExport: Bool](/documentation/avfoundation/avassetexportsession/allowsparallelizedexport)
- [var shouldOptimizeForNetworkUse: Bool](/documentation/avfoundation/avassetexportsession/shouldoptimizefornetworkuse)
- [var canPerformMultiplePassesOverSourceMediaData: Bool](/documentation/avfoundation/avassetexportsession/canperformmultiplepassesoversourcemediadata)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avassetexportsession/timerange)
- [var fileLengthLimit: Int64](/documentation/avfoundation/avassetexportsession/filelengthlimit)
- [var directoryForTemporaryFiles: URL?](/documentation/avfoundation/avassetexportsession/directoryfortemporaryfiles)

#### Configuring metadata

- [var metadata: [AVMetadataItem]?](/documentation/avfoundation/avassetexportsession/metadata)
- [var metadataItemFilter: AVMetadataItemFilter?](/documentation/avfoundation/avassetexportsession/metadataitemfilter)

#### Configuring video output

- [var videoComposition: AVVideoComposition?](/documentation/avfoundation/avassetexportsession/videocomposition)
- [var customVideoCompositor: (any AVVideoCompositing)?](/documentation/avfoundation/avassetexportsession/customvideocompositor)

#### Configuring track groups

- [var audioTrackGroupHandling: AVAssetTrackGroupOutputHandling](/documentation/avfoundation/avassetexportsession/audiotrackgrouphandling)
- [AVAssetTrackGroupOutputHandling](/documentation/avfoundation/avassettrackgroupoutputhandling)

##### Policies

- [static var preserveAlternateTracks: AVAssetTrackGroupOutputHandling](/documentation/avfoundation/avassettrackgroupoutputhandling/preservealternatetracks)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avassettrackgroupoutputhandling/init(rawvalue:))

#### Configuring audio output

- [var audioMix: AVAudioMix?](/documentation/avfoundation/avassetexportsession/audiomix)
- [var audioTimePitchAlgorithm: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avassetexportsession/audiotimepitchalgorithm)

#### Exporting media

- [func export(to: URL, as: AVFileType, isolation: isolated (any Actor)?) async throws](/documentation/avfoundation/avassetexportsession/export(to:as:isolation:))
- [func cancelExport()](/documentation/avfoundation/avassetexportsession/cancelexport())
- [func exportAsynchronously(completionHandler: () -> Void)](/documentation/avfoundation/avassetexportsession/exportasynchronously(completionhandler:))

#### Monitoring export progress

- [func states(updateInterval: TimeInterval) -> some Sendable & AsyncSequence<AVAssetExportSession.State, Never>
](/documentation/avfoundation/avassetexportsession/states(updateinterval:))
- [AVAssetExportSession.State](/documentation/avfoundation/avassetexportsession/state)

##### States

- [case pending](/documentation/avfoundation/avassetexportsession/state/pending)
- [case exporting(progress: Progress)](/documentation/avfoundation/avassetexportsession/state/exporting(progress:))
- [case waiting](/documentation/avfoundation/avassetexportsession/state/waiting)
- [var status: AVAssetExportSession.Status](/documentation/avfoundation/avassetexportsession/status-swift.property)
- [AVAssetExportSession.Status](/documentation/avfoundation/avassetexportsession/status-swift.enum)

##### Status values

- [case unknown](/documentation/avfoundation/avassetexportsession/status-swift.enum/unknown)
- [case waiting](/documentation/avfoundation/avassetexportsession/status-swift.enum/waiting)
- [case exporting](/documentation/avfoundation/avassetexportsession/status-swift.enum/exporting)
- [case completed](/documentation/avfoundation/avassetexportsession/status-swift.enum/completed)
- [case failed](/documentation/avfoundation/avassetexportsession/status-swift.enum/failed)
- [case cancelled](/documentation/avfoundation/avassetexportsession/status-swift.enum/cancelled)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avassetexportsession/status-swift.enum/init(rawvalue:))
- [var progress: Float](/documentation/avfoundation/avassetexportsession/progress)
- [var error: (any Error)?](/documentation/avfoundation/avassetexportsession/error)

#### Estimating file length and duration

- [func estimateOutputFileLength(completionHandler: (Int64, (any Error)?) -> Void)](/documentation/avfoundation/avassetexportsession/estimateoutputfilelength(completionhandler:))
- [var estimatedOutputFileLength: Int64](/documentation/avfoundation/avassetexportsession/estimatedoutputfilelength)

#### Estimating duration

- [func estimateMaximumDuration(completionHandler: (CMTime, (any Error)?) -> Void)](/documentation/avfoundation/avassetexportsession/estimatemaximumduration(completionhandler:))
- [var maxDuration: CMTime](/documentation/avfoundation/avassetexportsession/maxduration)

#### Accessing the asset

- [var asset: AVAsset](/documentation/avfoundation/avassetexportsession/asset)

### Image generation

- [Creating images from a video asset](/documentation/avfoundation/creating-images-from-a-video-asset)
- [AVAssetImageGenerator](/documentation/avfoundation/avassetimagegenerator)

#### Creating an image generator

- [init(asset: AVAsset)](/documentation/avfoundation/avassetimagegenerator/init(asset:))

#### Configuring image generation

- [var maximumSize: CGSize](/documentation/avfoundation/avassetimagegenerator/maximumsize)
- [var requestedTimeToleranceBefore: CMTime](/documentation/avfoundation/avassetimagegenerator/requestedtimetolerancebefore)
- [var requestedTimeToleranceAfter: CMTime](/documentation/avfoundation/avassetimagegenerator/requestedtimetoleranceafter)
- [var dynamicRangePolicy: AVAssetImageGenerator.DynamicRangePolicy](/documentation/avfoundation/avassetimagegenerator/dynamicrangepolicy-swift.property)
- [AVAssetImageGenerator.DynamicRangePolicy](/documentation/avfoundation/avassetimagegenerator/dynamicrangepolicy-swift.struct)

##### Policies

- [static let forceSDR: AVAssetImageGenerator.DynamicRangePolicy](/documentation/avfoundation/avassetimagegenerator/dynamicrangepolicy-swift.struct/forcesdr)
- [static let matchSource: AVAssetImageGenerator.DynamicRangePolicy](/documentation/avfoundation/avassetimagegenerator/dynamicrangepolicy-swift.struct/matchsource)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avassetimagegenerator/dynamicrangepolicy-swift.struct/init(rawvalue:))
- [var appliesPreferredTrackTransform: Bool](/documentation/avfoundation/avassetimagegenerator/appliespreferredtracktransform)
- [var apertureMode: AVAssetImageGenerator.ApertureMode?](/documentation/avfoundation/avassetimagegenerator/aperturemode-swift.property)
- [AVAssetImageGenerator.ApertureMode](/documentation/avfoundation/avassetimagegenerator/aperturemode-swift.struct)

##### Aperture modes

- [static let cleanAperture: AVAssetImageGenerator.ApertureMode](/documentation/avfoundation/avassetimagegenerator/aperturemode-swift.struct/cleanaperture)
- [static let encodedPixels: AVAssetImageGenerator.ApertureMode](/documentation/avfoundation/avassetimagegenerator/aperturemode-swift.struct/encodedpixels)
- [static let productionAperture: AVAssetImageGenerator.ApertureMode](/documentation/avfoundation/avassetimagegenerator/aperturemode-swift.struct/productionaperture)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avassetimagegenerator/aperturemode-swift.struct/init(rawvalue:))

#### Configuring compositing

- [var videoComposition: AVVideoComposition?](/documentation/avfoundation/avassetimagegenerator/videocomposition)
- [var customVideoCompositor: (any AVVideoCompositing)?](/documentation/avfoundation/avassetimagegenerator/customvideocompositor)

#### Generating images

- [func image(at: CMTime) async throws -> (image: CGImage, actualTime: CMTime)](/documentation/avfoundation/avassetimagegenerator/image(at:))
- [func images(for: [CMTime]) -> sending AVAssetImageGenerator.Images](/documentation/avfoundation/avassetimagegenerator/images(for:))

##### Generated image sequence

- [AVAssetImageGenerator.Images](/documentation/avfoundation/avassetimagegenerator/images)

###### Creating an iterator

- [func makeAsyncIterator() -> AVAssetImageGenerator.Images](/documentation/avfoundation/avassetimagegenerator/images/makeasynciterator())

###### Iterating elements

- [func next() async -> AVAssetImageGenerator.Images.Element?](/documentation/avfoundation/avassetimagegenerator/images/next())
- [AVAssetImageGenerator.Images.Element](/documentation/avfoundation/avassetimagegenerator/images/element)

###### Cases

- [case success(requestedTime: CMTime, image: CGImage, actualTime: CMTime)](/documentation/avfoundation/avassetimagegenerator/images/element/success(requestedtime:image:actualtime:))
- [case failure(requestedTime: CMTime, error: any Error)](/documentation/avfoundation/avassetimagegenerator/images/element/failure(requestedtime:error:))

###### Accessing image data

- [var image: CGImage](/documentation/avfoundation/avassetimagegenerator/images/element/image)
- [var requestedTime: CMTime](/documentation/avfoundation/avassetimagegenerator/images/element/requestedtime)
- [var actualTime: CMTime](/documentation/avfoundation/avassetimagegenerator/images/element/actualtime)
- [AVAssetImageGenerator.Images](/documentation/avfoundation/avassetimagegenerator/images)

##### Creating an iterator

- [func makeAsyncIterator() -> AVAssetImageGenerator.Images](/documentation/avfoundation/avassetimagegenerator/images/makeasynciterator())

##### Iterating elements

- [func next() async -> AVAssetImageGenerator.Images.Element?](/documentation/avfoundation/avassetimagegenerator/images/next())
- [AVAssetImageGenerator.Images.Element](/documentation/avfoundation/avassetimagegenerator/images/element)

###### Cases

- [case success(requestedTime: CMTime, image: CGImage, actualTime: CMTime)](/documentation/avfoundation/avassetimagegenerator/images/element/success(requestedtime:image:actualtime:))
- [case failure(requestedTime: CMTime, error: any Error)](/documentation/avfoundation/avassetimagegenerator/images/element/failure(requestedtime:error:))

###### Accessing image data

- [var image: CGImage](/documentation/avfoundation/avassetimagegenerator/images/element/image)
- [var requestedTime: CMTime](/documentation/avfoundation/avassetimagegenerator/images/element/requestedtime)
- [var actualTime: CMTime](/documentation/avfoundation/avassetimagegenerator/images/element/actualtime)
- [func generateCGImageAsynchronously(for: CMTime, completionHandler: (CGImage?, CMTime, (any Error)?) -> Void)](/documentation/avfoundation/avassetimagegenerator/generatecgimageasynchronously(for:completionhandler:))

##### Data types

- [AVAssetImageGeneratorCompletionHandler](/documentation/avfoundation/avassetimagegeneratorcompletionhandler)
- [AVAssetImageGenerator.Result](/documentation/avfoundation/avassetimagegenerator/result)

###### Results

- [case succeeded](/documentation/avfoundation/avassetimagegenerator/result/succeeded)
- [case failed](/documentation/avfoundation/avassetimagegenerator/result/failed)
- [case cancelled](/documentation/avfoundation/avassetimagegenerator/result/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avassetimagegenerator/result/init(rawvalue:))
- [func generateCGImagesAsynchronously(forTimes: [NSValue], completionHandler: AVAssetImageGeneratorCompletionHandler)](/documentation/avfoundation/avassetimagegenerator/generatecgimagesasynchronously(fortimes:completionhandler:))

##### Data types

- [AVAssetImageGeneratorCompletionHandler](/documentation/avfoundation/avassetimagegeneratorcompletionhandler)
- [AVAssetImageGenerator.Result](/documentation/avfoundation/avassetimagegenerator/result)

###### Results

- [case succeeded](/documentation/avfoundation/avassetimagegenerator/result/succeeded)
- [case failed](/documentation/avfoundation/avassetimagegenerator/result/failed)
- [case cancelled](/documentation/avfoundation/avassetimagegenerator/result/cancelled)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avassetimagegenerator/result/init(rawvalue:))
- [AVAssetImageGeneratorCompletionHandler](/documentation/avfoundation/avassetimagegeneratorcompletionhandler)
- [func cancelAllCGImageGeneration()](/documentation/avfoundation/avassetimagegenerator/cancelallcgimagegeneration())
- [func copyCGImage(at: CMTime, actualTime: UnsafeMutablePointer<CMTime>?) throws -> CGImage](/documentation/avfoundation/avassetimagegenerator/copycgimage(at:actualtime:))

#### Accessing the asset

- [var asset: AVAsset](/documentation/avfoundation/avassetimagegenerator/asset)

### Media reading

- [Reading multiview 3D video files](/documentation/avfoundation/reading-multiview-3d-video-files)
- [AVAssetReader](/documentation/avfoundation/avassetreader)

#### Creating an asset reader

- [init(asset: AVAsset) throws](/documentation/avfoundation/avassetreader/init(asset:))

#### Managing outputs

- [func canAdd(AVAssetReaderOutput) -> Bool](/documentation/avfoundation/avassetreader/canadd(_:))
- [func add(AVAssetReaderOutput)](/documentation/avfoundation/avassetreader/add(_:))
- [var outputs: [AVAssetReaderOutput]](/documentation/avfoundation/avassetreader/outputs)

#### Accessing output providers

- [func outputProvider(for: AVAssetReaderOutput) -> sending AVAssetReaderOutput.Provider<CMReadySampleBuffer<CMSampleBuffer.DynamicContent>>](/documentation/avfoundation/avassetreader/outputprovider(for:))
- [func outputProviderWithRandomAccess(for: AVAssetReaderOutput) -> sending (AVAssetReaderOutput.Provider<CMReadySampleBuffer<CMSampleBuffer.DynamicContent>>, AVAssetReaderOutput.RandomAccessController)](/documentation/avfoundation/avassetreader/outputproviderwithrandomaccess(for:))
- [func outputCaptionProvider(for: AVAssetReaderTrackOutput, validationDelegate: (any AVAssetReaderCaptionValidationHandling)?) -> sending AVAssetReaderOutput.Provider<AVCaptionGroup>](/documentation/avfoundation/avassetreader/outputcaptionprovider(for:validationdelegate:))
- [func outputCaptionProviderWithRandomAccess(for: AVAssetReaderTrackOutput, validationDelegate: (any AVAssetReaderCaptionValidationHandling)?) -> sending (AVAssetReaderOutput.Provider<AVCaptionGroup>, AVAssetReaderOutput.RandomAccessController)](/documentation/avfoundation/avassetreader/outputcaptionproviderwithrandomaccess(for:validationdelegate:))
- [func outputMetadataProvider(for: AVAssetReaderTrackOutput) -> sending AVAssetReaderOutput.Provider<AVTimedMetadataGroup>](/documentation/avfoundation/avassetreader/outputmetadataprovider(for:))
- [func outputMetadataProviderWithRandomAccess(for: AVAssetReaderTrackOutput) -> sending (AVAssetReaderOutput.Provider<AVTimedMetadataGroup>, AVAssetReaderOutput.RandomAccessController)](/documentation/avfoundation/avassetreader/outputmetadataproviderwithrandomaccess(for:))

#### Configuring reading

- [var timeRange: CMTimeRange](/documentation/avfoundation/avassetreader/timerange)
- [var status: AVAssetReader.Status](/documentation/avfoundation/avassetreader/status-swift.property)
- [AVAssetReader.Status](/documentation/avfoundation/avassetreader/status-swift.enum)

##### Status values

- [case unknown](/documentation/avfoundation/avassetreader/status-swift.enum/unknown)
- [case reading](/documentation/avfoundation/avassetreader/status-swift.enum/reading)
- [case completed](/documentation/avfoundation/avassetreader/status-swift.enum/completed)
- [case failed](/documentation/avfoundation/avassetreader/status-swift.enum/failed)
- [case cancelled](/documentation/avfoundation/avassetreader/status-swift.enum/cancelled)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avassetreader/status-swift.enum/init(rawvalue:))
- [var error: (any Error)?](/documentation/avfoundation/avassetreader/error)

#### Controlling reading

- [func start() throws](/documentation/avfoundation/avassetreader/start())
- [func startReading() -> Bool](/documentation/avfoundation/avassetreader/startreading())
- [func cancelReading()](/documentation/avfoundation/avassetreader/cancelreading())

#### Inspecting the asset

- [var asset: AVAsset](/documentation/avfoundation/avassetreader/asset)
- [AVAssetReaderOutput](/documentation/avfoundation/avassetreaderoutput)

#### Configuring reading

- [var alwaysCopiesSampleData: Bool](/documentation/avfoundation/avassetreaderoutput/alwayscopiessampledata)
- [var supportsRandomAccess: Bool](/documentation/avfoundation/avassetreaderoutput/supportsrandomaccess)
- [func reset(forReadingTimeRanges: [NSValue])](/documentation/avfoundation/avassetreaderoutput/reset(forreadingtimeranges:))
- [func markConfigurationAsFinal()](/documentation/avfoundation/avassetreaderoutput/markconfigurationasfinal())

#### Copying sample buffers

- [func copyNextSampleBuffer() -> CMSampleBuffer?](/documentation/avfoundation/avassetreaderoutput/copynextsamplebuffer())
- [AVAssetReaderOutput.Provider](/documentation/avfoundation/avassetreaderoutput/provider)

##### Reading media data

- [func captionsNotPresentInPreviousGroups(in: AVCaptionGroup) -> [AVCaption]](/documentation/avfoundation/avassetreaderoutput/provider/captionsnotpresentinpreviousgroups(in:))
- [func next() async throws -> Payload?](/documentation/avfoundation/avassetreaderoutput/provider/next())
- [AVAssetReaderOutput.RandomAccessController](/documentation/avfoundation/avassetreaderoutput/randomaccesscontroller)

##### Configuring a controller

- [func markConfigurationAsFinal()](/documentation/avfoundation/avassetreaderoutput/randomaccesscontroller/markconfigurationasfinal())
- [func resetForReading(timeRanges: [CMTimeRange])](/documentation/avfoundation/avassetreaderoutput/randomaccesscontroller/resetforreading(timeranges:))
- [AVAssetReaderOutput.SupportedPayload](/documentation/avfoundation/avassetreaderoutput/supportedpayload)

#### Inspecting the media type

- [var mediaType: AVMediaType](/documentation/avfoundation/avassetreaderoutput/mediatype)
- [AVAssetReaderTrackOutput](/documentation/avfoundation/avassetreadertrackoutput)

#### Creating a track output

- [init(track: AVAssetTrack, outputSettings: [String : Any]?)](/documentation/avfoundation/avassetreadertrackoutput/init(track:outputsettings:))
- [Video settings](/documentation/avfoundation/video-settings)

##### Clean aperture

- [let AVVideoCleanApertureKey: String](/documentation/avfoundation/avvideocleanaperturekey)
- [let AVVideoCleanApertureWidthKey: String](/documentation/avfoundation/avvideocleanaperturewidthkey)
- [let AVVideoCleanApertureHeightKey: String](/documentation/avfoundation/avvideocleanapertureheightkey)
- [let AVVideoCleanApertureVerticalOffsetKey: String](/documentation/avfoundation/avvideocleanapertureverticaloffsetkey)
- [let AVVideoCleanApertureHorizontalOffsetKey: String](/documentation/avfoundation/avvideocleanaperturehorizontaloffsetkey)

##### Video codecs

- [let AVVideoCodecKey: String](/documentation/avfoundation/avvideocodeckey)
- [AVVideoCodecType](/documentation/avfoundation/avvideocodectype)

###### Video codecs

- [static let h264: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/h264)
- [static let hevc: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevc)
- [static let hevcWithAlpha: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevcwithalpha)
- [static let jpeg: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpeg)
- [static let JPEGXL: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpegxl)
- [static let proRes422: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422)
- [static let proRes422LT: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422lt)
- [static let proRes422HQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422hq)
- [static let proRes422Proxy: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422proxy)
- [static let proRes4444: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores4444)
- [static let proResRAW: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresraw)
- [static let proResRAWHQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresrawhq)
- [static let appleProRes4444XQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/appleprores4444xq)

###### Deprecated

- [let AVVideoCodecH264: String](/documentation/avfoundation/avvideocodech264)
- [let AVVideoCodecHEVC: String](/documentation/avfoundation/avvideocodechevc)
- [let AVVideoCodecJPEG: String](/documentation/avfoundation/avvideocodecjpeg)
- [let AVVideoCodecAppleProRes422: String](/documentation/avfoundation/avvideocodecappleprores422)
- [let AVVideoCodecAppleProRes4444: String](/documentation/avfoundation/avvideocodecappleprores4444)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideocodectype/init(rawvalue:))

##### Color properties

- [Setting color properties for a specific resolution](/documentation/avfoundation/setting-color-properties-for-a-specific-resolution)
- [let AVVideoAllowWideColorKey: String](/documentation/avfoundation/avvideoallowwidecolorkey)
- [let AVVideoColorPrimariesKey: String](/documentation/avfoundation/avvideocolorprimarieskey)
- [let AVVideoColorPrimaries_EBU_3213: String](/documentation/avfoundation/avvideocolorprimaries_ebu_3213)
- [let AVVideoColorPrimaries_ITU_R_2020: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_2020)
- [let AVVideoColorPrimaries_ITU_R_709_2: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_709_2)
- [let AVVideoColorPrimaries_P3_D65: String](/documentation/avfoundation/avvideocolorprimaries_p3_d65)
- [let AVVideoColorPrimaries_SMPTE_C: String](/documentation/avfoundation/avvideocolorprimaries_smpte_c)
- [let AVVideoColorPropertiesKey: String](/documentation/avfoundation/avvideocolorpropertieskey)
- [let AVVideoTransferFunctionKey: String](/documentation/avfoundation/avvideotransferfunctionkey)
- [let AVVideoTransferFunction_IEC_sRGB: String](/documentation/avfoundation/avvideotransferfunction_iec_srgb)
- [let AVVideoTransferFunction_ITU_R_2100_HLG: String](/documentation/avfoundation/avvideotransferfunction_itu_r_2100_hlg)
- [let AVVideoTransferFunction_ITU_R_709_2: String](/documentation/avfoundation/avvideotransferfunction_itu_r_709_2)
- [let AVVideoTransferFunction_Linear: String](/documentation/avfoundation/avvideotransferfunction_linear)
- [let AVVideoTransferFunction_SMPTE_240M_1995: String](/documentation/avfoundation/avvideotransferfunction_smpte_240m_1995)
- [let AVVideoTransferFunction_SMPTE_ST_2084_PQ: String](/documentation/avfoundation/avvideotransferfunction_smpte_st_2084_pq)
- [let AVVideoYCbCrMatrixKey: String](/documentation/avfoundation/avvideoycbcrmatrixkey)
- [let AVVideoYCbCrMatrix_ITU_R_2020: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_2020)
- [let AVVideoYCbCrMatrix_ITU_R_601_4: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_601_4)
- [let AVVideoYCbCrMatrix_ITU_R_709_2: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_709_2)
- [let AVVideoYCbCrMatrix_SMPTE_240M_1995: String](/documentation/avfoundation/avvideoycbcrmatrix_smpte_240m_1995)

##### Compression

- [let AVVideoCompressionPropertiesKey: String](/documentation/avfoundation/avvideocompressionpropertieskey)
- [let AVVideoDecompressionPropertiesKey: String](/documentation/avfoundation/avvideodecompressionpropertieskey)
- [let AVVideoAverageBitRateKey: String](/documentation/avfoundation/avvideoaveragebitratekey)
- [let AVVideoQualityKey: String](/documentation/avfoundation/avvideoqualitykey)
- [let AVVideoMaxKeyFrameIntervalKey: String](/documentation/avfoundation/avvideomaxkeyframeintervalkey)
- [let AVVideoMaxKeyFrameIntervalDurationKey: String](/documentation/avfoundation/avvideomaxkeyframeintervaldurationkey)
- [let AVVideoAllowFrameReorderingKey: String](/documentation/avfoundation/avvideoallowframereorderingkey)
- [let AVVideoAppleProRAWBitDepthKey: String](/documentation/avfoundation/avvideoappleprorawbitdepthkey)

##### Entropy mode

- [let AVVideoH264EntropyModeKey: String](/documentation/avfoundation/avvideoh264entropymodekey)
- [let AVVideoH264EntropyModeCABAC: String](/documentation/avfoundation/avvideoh264entropymodecabac)
- [let AVVideoH264EntropyModeCAVLC: String](/documentation/avfoundation/avvideoh264entropymodecavlc)

##### FairPlay

- [let AVStreamingKeyDeliveryContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverycontentkeytype)
- [let AVStreamingKeyDeliveryPersistentContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverypersistentcontentkeytype)

##### Frame rate

- [let AVVideoExpectedSourceFrameRateKey: String](/documentation/avfoundation/avvideoexpectedsourceframeratekey)
- [let AVVideoAverageNonDroppableFrameRateKey: String](/documentation/avfoundation/avvideoaveragenondroppableframeratekey)

##### Geometry

- [let AVVideoWidthKey: String](/documentation/avfoundation/avvideowidthkey)
- [let AVVideoHeightKey: String](/documentation/avfoundation/avvideoheightkey)
- [let AVVideoPixelAspectRatioKey: String](/documentation/avfoundation/avvideopixelaspectratiokey)
- [let AVVideoPixelAspectRatioVerticalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratioverticalspacingkey)
- [let AVVideoPixelAspectRatioHorizontalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratiohorizontalspacingkey)

##### Profile level

- [let AVVideoProfileLevelKey: String](/documentation/avfoundation/avvideoprofilelevelkey)
- [let AVVideoProfileLevelH264High40: String](/documentation/avfoundation/avvideoprofilelevelh264high40)
- [let AVVideoProfileLevelH264High41: String](/documentation/avfoundation/avvideoprofilelevelh264high41)
- [let AVVideoProfileLevelH264Main30: String](/documentation/avfoundation/avvideoprofilelevelh264main30)
- [let AVVideoProfileLevelH264Main31: String](/documentation/avfoundation/avvideoprofilelevelh264main31)
- [let AVVideoProfileLevelH264Main32: String](/documentation/avfoundation/avvideoprofilelevelh264main32)
- [let AVVideoProfileLevelH264Main41: String](/documentation/avfoundation/avvideoprofilelevelh264main41)
- [let AVVideoProfileLevelH264Baseline30: String](/documentation/avfoundation/avvideoprofilelevelh264baseline30)
- [let AVVideoProfileLevelH264Baseline31: String](/documentation/avfoundation/avvideoprofilelevelh264baseline31)
- [let AVVideoProfileLevelH264Baseline41: String](/documentation/avfoundation/avvideoprofilelevelh264baseline41)
- [let AVVideoProfileLevelH264HighAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264highautolevel)
- [let AVVideoProfileLevelH264MainAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264mainautolevel)
- [let AVVideoProfileLevelH264BaselineAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264baselineautolevel)

##### Scaling mode

- [let AVVideoScalingModeFit: String](/documentation/avfoundation/avvideoscalingmodefit)
- [let AVVideoScalingModeKey: String](/documentation/avfoundation/avvideoscalingmodekey)
- [let AVVideoScalingModeResize: String](/documentation/avfoundation/avvideoscalingmoderesize)
- [let AVVideoScalingModeResizeAspect: String](/documentation/avfoundation/avvideoscalingmoderesizeaspect)
- [let AVVideoScalingModeResizeAspectFill: String](/documentation/avfoundation/avvideoscalingmoderesizeaspectfill)

##### VideoToolbox options

- [let AVVideoEncoderSpecificationKey: String](/documentation/avfoundation/avvideoencoderspecificationkey)

#### Configuring audio settings

- [var audioTimePitchAlgorithm: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avassetreadertrackoutput/audiotimepitchalgorithm)

#### Inspecting an output

- [var outputSettings: [String : Any]?](/documentation/avfoundation/avassetreadertrackoutput/outputsettings)
- [var track: AVAssetTrack](/documentation/avfoundation/avassetreadertrackoutput/track)
- [AVAssetReaderAudioMixOutput](/documentation/avfoundation/avassetreaderaudiomixoutput)

#### Creating an audio mix output

- [init(audioTracks: [AVAssetTrack], audioSettings: [String : Any]?)](/documentation/avfoundation/avassetreaderaudiomixoutput/init(audiotracks:audiosettings:))

#### Configuring audio settings

- [var audioMix: AVAudioMix?](/documentation/avfoundation/avassetreaderaudiomixoutput/audiomix)
- [var audioTimePitchAlgorithm: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avassetreaderaudiomixoutput/audiotimepitchalgorithm)

#### Inspecting an output

- [var audioTracks: [AVAssetTrack]](/documentation/avfoundation/avassetreaderaudiomixoutput/audiotracks)
- [var audioSettings: [String : Any]?](/documentation/avfoundation/avassetreaderaudiomixoutput/audiosettings)
- [AVAssetReaderVideoCompositionOutput](/documentation/avfoundation/avassetreadervideocompositionoutput)

#### Creating a video composition output

- [init(videoTracks: [AVAssetTrack], videoSettings: [String : Any]?)](/documentation/avfoundation/avassetreadervideocompositionoutput/init(videotracks:videosettings:))

#### Configuring video settings

- [var videoComposition: AVVideoComposition?](/documentation/avfoundation/avassetreadervideocompositionoutput/videocomposition)
- [var customVideoCompositor: (any AVVideoCompositing)?](/documentation/avfoundation/avassetreadervideocompositionoutput/customvideocompositor)

#### Inspecting an output

- [var videoTracks: [AVAssetTrack]](/documentation/avfoundation/avassetreadervideocompositionoutput/videotracks)
- [var videoSettings: [String : Any]?](/documentation/avfoundation/avassetreadervideocompositionoutput/videosettings)
- [AVAssetReaderSampleReferenceOutput](/documentation/avfoundation/avassetreadersamplereferenceoutput)

#### Creating a sample reference output

- [init(track: AVAssetTrack)](/documentation/avfoundation/avassetreadersamplereferenceoutput/init(track:))

#### Inspecting the track

- [var track: AVAssetTrack](/documentation/avfoundation/avassetreadersamplereferenceoutput/track)
- [AVAssetReaderOutputMetadataAdaptor](/documentation/avfoundation/avassetreaderoutputmetadataadaptor)

#### Creating a metadata adaptor

- [init(assetReaderTrackOutput: AVAssetReaderTrackOutput)](/documentation/avfoundation/avassetreaderoutputmetadataadaptor/init(assetreadertrackoutput:))

#### Retrieving timed metadata groups

- [func nextTimedMetadataGroup() -> AVTimedMetadataGroup?](/documentation/avfoundation/avassetreaderoutputmetadataadaptor/nexttimedmetadatagroup())

#### Inspecting the track output

- [var assetReaderTrackOutput: AVAssetReaderTrackOutput](/documentation/avfoundation/avassetreaderoutputmetadataadaptor/assetreadertrackoutput)

### Media writing

- [Converting projected video to Apple Projected Media Profile](/documentation/avfoundation/converting-projected-video-to-apple-projected-media-profile)
- [Converting side-by-side 3D video to multiview HEVC and spatial video](/documentation/avfoundation/converting-side-by-side-3d-video-to-multiview-hevc-and-spatial-video)
- [Adding a display mask rectangle metadata track to a movie file](/documentation/avfoundation/adding-a-display-mask-rectangle-metadata-track-to-a-movie-file)
- [Writing fragmented MPEG-4 files for HTTP Live Streaming](/documentation/avfoundation/writing-fragmented-mpeg-4-files-for-http-live-streaming)
- [Creating spatial photos and videos with spatial metadata](/documentation/imageio/creating-spatial-photos-and-videos-with-spatial-metadata)
- [Tagging media with video color information](/documentation/avfoundation/tagging-media-with-video-color-information)
- [Evaluating an app’s video color](/documentation/avfoundation/evaluating-an-app-s-video-color)

#### Video evaluation

- [Evaluating video using QuickTime test pattern files](/documentation/avfoundation/evaluating-video-using-quicktime-test-pattern-files)
- [Evaluating an app’s video color using video test equipment](/documentation/avfoundation/evaluating-an-app-s-video-color-using-video-test-equipment)
- [Evaluating an app’s video color using light-measurement Instruments](/documentation/avfoundation/evaluating-an-app-s-video-color-using-light-measurement-instruments)
- [AVOutputSettingsAssistant](/documentation/avfoundation/avoutputsettingsassistant)

#### Creating an assistant

- [convenience init?(preset: AVOutputSettingsPreset)](/documentation/avfoundation/avoutputsettingsassistant/init(preset:))
- [AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset)

##### Presets

- [static let preset640x480: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/preset640x480)
- [static let preset960x540: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/preset960x540)
- [static let preset1280x720: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/preset1280x720)
- [static let preset1920x1080: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/preset1920x1080)
- [static let preset3840x2160: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/preset3840x2160)
- [static let hevc1920x1080WithAlpha: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/hevc1920x1080withalpha)
- [static let hevc1920x1080: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/hevc1920x1080)
- [static let hevc3840x2160WithAlpha: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/hevc3840x2160withalpha)
- [static let hevc3840x2160: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/hevc3840x2160)
- [static let hevc4320x2160: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/hevc4320x2160)
- [static let hevc7680x4320: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/hevc7680x4320)
- [static let mvhevc1440x1440: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/mvhevc1440x1440)
- [static let mvhevc4320x4320: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/mvhevc4320x4320)
- [static let mvhevc7680x7680: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/mvhevc7680x7680)
- [static let mvhevc960x960: AVOutputSettingsPreset](/documentation/avfoundation/avoutputsettingspreset/mvhevc960x960)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avoutputsettingspreset/init(rawvalue:))
- [class func availableOutputSettingsPresets() -> [AVOutputSettingsPreset]](/documentation/avfoundation/avoutputsettingsassistant/availableoutputsettingspresets())

#### Configuring output settings

- [var outputFileType: AVFileType](/documentation/avfoundation/avoutputsettingsassistant/outputfiletype)
- [var audioSettings: [String : Any]?](/documentation/avfoundation/avoutputsettingsassistant/audiosettings)
- [var sourceAudioFormat: CMAudioFormatDescription?](/documentation/avfoundation/avoutputsettingsassistant/sourceaudioformat)
- [var videoSettings: [String : Any]?](/documentation/avfoundation/avoutputsettingsassistant/videosettings)
- [var sourceVideoFormat: CMVideoFormatDescription?](/documentation/avfoundation/avoutputsettingsassistant/sourcevideoformat)
- [var sourceVideoMinFrameDuration: CMTime](/documentation/avfoundation/avoutputsettingsassistant/sourcevideominframeduration)
- [var sourceVideoAverageFrameDuration: CMTime](/documentation/avfoundation/avoutputsettingsassistant/sourcevideoaverageframeduration)
- [AVAssetWriter](/documentation/avfoundation/avassetwriter)

#### Creating an asset writer

- [convenience init(url: URL, fileType: AVFileType) throws](/documentation/avfoundation/avassetwriter/init(url:filetype:))
- [init(outputURL: URL, fileType: AVFileType) throws](/documentation/avfoundation/avassetwriter/init(outputurl:filetype:))
- [init(contentType: UTType)](/documentation/avfoundation/avassetwriter/init(contenttype:))

#### Configuring inputs

- [var inputs: [AVAssetWriterInput]](/documentation/avfoundation/avassetwriter/inputs)
- [var availableMediaTypes: [AVMediaType]](/documentation/avfoundation/avassetwriter/availablemediatypes)
- [func canApply(outputSettings: [String : Any]?, forMediaType: AVMediaType) -> Bool](/documentation/avfoundation/avassetwriter/canapply(outputsettings:formediatype:))
- [func canAdd(AVAssetWriterInput) -> Bool](/documentation/avfoundation/avassetwriter/canadd(_:)-6al7j)
- [func add(AVAssetWriterInput)](/documentation/avfoundation/avassetwriter/add(_:)-4c4d0)

#### Configuring input receivers

- [func inputReceiver(for: AVAssetWriterInput) -> sending AVAssetWriterInput.SampleBufferReceiver](/documentation/avfoundation/avassetwriter/inputreceiver(for:))
- [func inputCaptionReceiver(for: AVAssetWriterInput) -> sending AVAssetWriterInput.CaptionReceiver](/documentation/avfoundation/avassetwriter/inputcaptionreceiver(for:))
- [func inputCaptionReceiverRequestingMultiPass(for: AVAssetWriterInput) -> sending (AVAssetWriterInput.CaptionReceiver, AVAssetWriterInput.MultiPassController)](/documentation/avfoundation/avassetwriter/inputcaptionreceiverrequestingmultipass(for:))
- [func inputMetadataReceiver(for: AVAssetWriterInput) -> sending AVAssetWriterInput.MetadataReceiver](/documentation/avfoundation/avassetwriter/inputmetadatareceiver(for:))
- [func inputMetadataReceiverRequestingMultiPass(for: AVAssetWriterInput) -> sending (AVAssetWriterInput.MetadataReceiver, AVAssetWriterInput.MultiPassController)](/documentation/avfoundation/avassetwriter/inputmetadatareceiverrequestingmultipass(for:))
- [func inputPixelBufferReceiver(for: AVAssetWriterInput, pixelBufferAttributes: CVPixelBufferCreationAttributes?) -> sending AVAssetWriterInput.PixelBufferReceiver](/documentation/avfoundation/avassetwriter/inputpixelbufferreceiver(for:pixelbufferattributes:))
- [func inputPixelBufferReceiverRequestingMultiPass(for: AVAssetWriterInput, pixelBufferAttributes: CVPixelBufferCreationAttributes?) -> sending (AVAssetWriterInput.PixelBufferReceiver, AVAssetWriterInput.MultiPassController)](/documentation/avfoundation/avassetwriter/inputpixelbufferreceiverrequestingmultipass(for:pixelbufferattributes:))
- [func inputReceiverRequestingMultiPass(for: AVAssetWriterInput) -> sending (AVAssetWriterInput.SampleBufferReceiver, AVAssetWriterInput.MultiPassController)](/documentation/avfoundation/avassetwriter/inputreceiverrequestingmultipass(for:))
- [func inputTaggedPixelBufferGroupReceiver(for: AVAssetWriterInput, pixelBufferAttributes: CVPixelBufferCreationAttributes?) -> sending AVAssetWriterInput.TaggedPixelBufferGroupReceiver](/documentation/avfoundation/avassetwriter/inputtaggedpixelbuffergroupreceiver(for:pixelbufferattributes:))
- [func inputTaggedPixelBufferGroupReceiverRequestingMultiPass(for: AVAssetWriterInput, pixelBufferAttributes: CVPixelBufferCreationAttributes?) -> sending (AVAssetWriterInput.TaggedPixelBufferGroupReceiver, AVAssetWriterInput.MultiPassController)](/documentation/avfoundation/avassetwriter/inputtaggedpixelbuffergroupreceiverrequestingmultipass(for:pixelbufferattributes:))

#### Configuring input groups

- [var inputGroups: [AVAssetWriterInputGroup]](/documentation/avfoundation/avassetwriter/inputgroups)
- [func canAdd(AVAssetWriterInputGroup) -> Bool](/documentation/avfoundation/avassetwriter/canadd(_:)-8s1oh)
- [func add(AVAssetWriterInputGroup)](/documentation/avfoundation/avassetwriter/add(_:)-3san4)

#### Configuring output

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avassetwriter/metadata)
- [var shouldOptimizeForNetworkUse: Bool](/documentation/avfoundation/avassetwriter/shouldoptimizefornetworkuse)
- [var directoryForTemporaryFiles: URL?](/documentation/avfoundation/avassetwriter/directoryfortemporaryfiles)

#### Configuring fragment output

- [var movieFragmentInterval: CMTime](/documentation/avfoundation/avassetwriter/moviefragmentinterval)
- [var initialMovieFragmentInterval: CMTime](/documentation/avfoundation/avassetwriter/initialmoviefragmentinterval)
- [var initialMovieFragmentSequenceNumber: Int](/documentation/avfoundation/avassetwriter/initialmoviefragmentsequencenumber)
- [var producesCombinableFragments: Bool](/documentation/avfoundation/avassetwriter/producescombinablefragments)
- [var overallDurationHint: CMTime](/documentation/avfoundation/avassetwriter/overalldurationhint)
- [var movieTimeScale: CMTimeScale](/documentation/avfoundation/avassetwriter/movietimescale)

#### Managing writing sessions

- [func start() throws](/documentation/avfoundation/avassetwriter/start())
- [func startWriting() -> Bool](/documentation/avfoundation/avassetwriter/startwriting())
- [func startSession(atSourceTime: CMTime)](/documentation/avfoundation/avassetwriter/startsession(atsourcetime:))
- [func endSession(atSourceTime: CMTime)](/documentation/avfoundation/avassetwriter/endsession(atsourcetime:))
- [func finishWriting(completionHandler: () -> Void)](/documentation/avfoundation/avassetwriter/finishwriting(completionhandler:))
- [func cancelWriting()](/documentation/avfoundation/avassetwriter/cancelwriting())
- [func finishWriting() -> Bool](/documentation/avfoundation/avassetwriter/finishwriting())

#### Inspecting writing status

- [var status: AVAssetWriter.Status](/documentation/avfoundation/avassetwriter/status-swift.property)
- [AVAssetWriter.Status](/documentation/avfoundation/avassetwriter/status-swift.enum)

##### Status values

- [case unknown](/documentation/avfoundation/avassetwriter/status-swift.enum/unknown)
- [case writing](/documentation/avfoundation/avassetwriter/status-swift.enum/writing)
- [case completed](/documentation/avfoundation/avassetwriter/status-swift.enum/completed)
- [case failed](/documentation/avfoundation/avassetwriter/status-swift.enum/failed)
- [case cancelled](/documentation/avfoundation/avassetwriter/status-swift.enum/cancelled)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avassetwriter/status-swift.enum/init(rawvalue:))
- [var error: (any Error)?](/documentation/avfoundation/avassetwriter/error)

#### Configuring segment writing

- [var delegate: (any AVAssetWriterDelegate)?](/documentation/avfoundation/avassetwriter/delegate)
- [AVAssetWriterDelegate](/documentation/avfoundation/avassetwriterdelegate)

##### Responding to segment output

- [func assetWriter(AVAssetWriter, didOutputSegmentData: Data, segmentType: AVAssetSegmentType)](/documentation/avfoundation/avassetwriterdelegate/assetwriter(_:didoutputsegmentdata:segmenttype:))
- [func assetWriter(AVAssetWriter, didOutputSegmentData: Data, segmentType: AVAssetSegmentType, segmentReport: AVAssetSegmentReport?)](/documentation/avfoundation/avassetwriterdelegate/assetwriter(_:didoutputsegmentdata:segmenttype:segmentreport:))
- [AVAssetSegmentReport](/documentation/avfoundation/avassetsegmentreport)

###### Inspecting a report

- [var segmentType: AVAssetSegmentType](/documentation/avfoundation/avassetsegmentreport/segmenttype)
- [AVAssetSegmentType](/documentation/avfoundation/avassetsegmenttype)

###### Segment types

- [case initialization](/documentation/avfoundation/avassetsegmenttype/initialization)
- [case separable](/documentation/avfoundation/avassetsegmenttype/separable)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avassetsegmenttype/init(rawvalue:))
- [var trackReports: [AVAssetSegmentTrackReport]](/documentation/avfoundation/avassetsegmentreport/trackreports)
- [AVAssetSegmentTrackReport](/documentation/avfoundation/avassetsegmenttrackreport)

###### Inspecting a report

- [var trackID: CMPersistentTrackID](/documentation/avfoundation/avassetsegmenttrackreport/trackid)
- [var mediaType: AVMediaType](/documentation/avfoundation/avassetsegmenttrackreport/mediatype)
- [var duration: CMTime](/documentation/avfoundation/avassetsegmenttrackreport/duration)
- [var earliestPresentationTimeStamp: CMTime](/documentation/avfoundation/avassetsegmenttrackreport/earliestpresentationtimestamp)
- [var firstVideoSampleInformation: AVAssetSegmentReportSampleInformation?](/documentation/avfoundation/avassetsegmenttrackreport/firstvideosampleinformation)
- [AVAssetSegmentReportSampleInformation](/documentation/avfoundation/avassetsegmentreportsampleinformation)

###### Inspecting the information

- [var presentationTimeStamp: CMTime](/documentation/avfoundation/avassetsegmentreportsampleinformation/presentationtimestamp)
- [var offset: Int](/documentation/avfoundation/avassetsegmentreportsampleinformation/offset)
- [var length: Int](/documentation/avfoundation/avassetsegmentreportsampleinformation/length)
- [var isSyncSample: Bool](/documentation/avfoundation/avassetsegmentreportsampleinformation/issyncsample)
- [var preferredOutputSegmentInterval: CMTime](/documentation/avfoundation/avassetwriter/preferredoutputsegmentinterval)
- [var initialSegmentStartTime: CMTime](/documentation/avfoundation/avassetwriter/initialsegmentstarttime)
- [var outputFileTypeProfile: AVFileTypeProfile?](/documentation/avfoundation/avassetwriter/outputfiletypeprofile)
- [func flushSegment()](/documentation/avfoundation/avassetwriter/flushsegment())

#### Accessing output settings

- [var outputURL: URL](/documentation/avfoundation/avassetwriter/outputurl)
- [var outputFileType: AVFileType](/documentation/avfoundation/avassetwriter/outputfiletype)
- [AVAssetWriterInput](/documentation/avfoundation/avassetwriterinput)

#### Creating an input

- [convenience init(mediaType: AVMediaType, outputSettings: [String : Any]?)](/documentation/avfoundation/avassetwriterinput/init(mediatype:outputsettings:))
- [init(mediaType: AVMediaType, outputSettings: [String : Any]?, sourceFormatHint: CMFormatDescription?)](/documentation/avfoundation/avassetwriterinput/init(mediatype:outputsettings:sourceformathint:))

#### Configuring presentation

- [var naturalSize: CGSize](/documentation/avfoundation/avassetwriterinput/naturalsize)
- [var transform: CGAffineTransform](/documentation/avfoundation/avassetwriterinput/transform)
- [var preferredVolume: Float](/documentation/avfoundation/avassetwriterinput/preferredvolume)
- [var mediaTimeScale: CMTimeScale](/documentation/avfoundation/avassetwriterinput/mediatimescale)
- [var marksOutputTrackAsEnabled: Bool](/documentation/avfoundation/avassetwriterinput/marksoutputtrackasenabled)

#### Configuring language support

- [var languageCode: String?](/documentation/avfoundation/avassetwriterinput/languagecode)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avassetwriterinput/extendedlanguagetag)

#### Configuring metadata

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avassetwriterinput/metadata)

#### Configuring media data layout

- [var preferredMediaChunkAlignment: Int](/documentation/avfoundation/avassetwriterinput/preferredmediachunkalignment)
- [var preferredMediaChunkDuration: CMTime](/documentation/avfoundation/avassetwriterinput/preferredmediachunkduration)
- [var sampleReferenceBaseURL: URL?](/documentation/avfoundation/avassetwriterinput/samplereferencebaseurl)
- [var mediaDataLocation: AVAssetWriterInput.MediaDataLocation](/documentation/avfoundation/avassetwriterinput/mediadatalocation-swift.property)
- [AVAssetWriterInput.MediaDataLocation](/documentation/avfoundation/avassetwriterinput/mediadatalocation-swift.struct)

##### Media data locations

- [static let interleavedWithMainMediaData: AVAssetWriterInput.MediaDataLocation](/documentation/avfoundation/avassetwriterinput/mediadatalocation-swift.struct/interleavedwithmainmediadata)
- [static let beforeMainMediaDataNotInterleaved: AVAssetWriterInput.MediaDataLocation](/documentation/avfoundation/avassetwriterinput/mediadatalocation-swift.struct/beforemainmediadatanotinterleaved)
- [static let sparselyInterleavedWithMainMediaData: AVAssetWriterInput.MediaDataLocation](/documentation/avfoundation/avassetwriterinput/mediadatalocation-swift.struct/sparselyinterleavedwithmainmediadata)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avassetwriterinput/mediadatalocation-swift.struct/init(rawvalue:))

#### Configuring track associations

- [func canAddTrackAssociation(withTrackOf: AVAssetWriterInput, type: String) -> Bool](/documentation/avfoundation/avassetwriterinput/canaddtrackassociation(withtrackof:type:))
- [func addTrackAssociation(withTrackOf: AVAssetWriterInput, type: String)](/documentation/avfoundation/avassetwriterinput/addtrackassociation(withtrackof:type:))

#### Appending media samples

- [var expectsMediaDataInRealTime: Bool](/documentation/avfoundation/avassetwriterinput/expectsmediadatainrealtime)
- [var isReadyForMoreMediaData: Bool](/documentation/avfoundation/avassetwriterinput/isreadyformoremediadata)
- [func requestMediaDataWhenReady(on: dispatch_queue_t, using: () -> Void)](/documentation/avfoundation/avassetwriterinput/requestmediadatawhenready(on:using:))
- [func append(CMSampleBuffer) -> Bool](/documentation/avfoundation/avassetwriterinput/append(_:))
- [func markAsFinished()](/documentation/avfoundation/avassetwriterinput/markasfinished())
- [AVAssetWriterInput.SampleBufferReceiver](/documentation/avfoundation/avassetwriterinput/samplebufferreceiver)

##### Appending samples

- [func append(CMReadySampleBuffer<CMSampleBuffer.DynamicContent>) async throws](/documentation/avfoundation/avassetwriterinput/samplebufferreceiver/append(_:))
- [func appendImmediately(CMReadySampleBuffer<CMSampleBuffer.DynamicContent>) throws -> Bool](/documentation/avfoundation/avassetwriterinput/samplebufferreceiver/appendimmediately(_:))
- [func finish()](/documentation/avfoundation/avassetwriterinput/samplebufferreceiver/finish())
- [AVAssetWriterInput.PixelBufferReceiver](/documentation/avfoundation/avassetwriterinput/pixelbufferreceiver)

##### Appending pixel buffers

- [func append(CVReadOnlyPixelBuffer, with: CMTime) async throws](/documentation/avfoundation/avassetwriterinput/pixelbufferreceiver/append(_:with:))
- [func appendImmediately(CVReadOnlyPixelBuffer, with: CMTime) throws -> Bool](/documentation/avfoundation/avassetwriterinput/pixelbufferreceiver/appendimmediately(_:with:))
- [func finish()](/documentation/avfoundation/avassetwriterinput/pixelbufferreceiver/finish())

##### Accessing the pixel buffer pool

- [var pixelBufferPool: CVMutablePixelBuffer.Pool?](/documentation/avfoundation/avassetwriterinput/pixelbufferreceiver/pixelbufferpool)
- [var sourcePixelBufferAttributes: CVPixelBufferCreationAttributes?](/documentation/avfoundation/avassetwriterinput/pixelbufferreceiver/sourcepixelbufferattributes)
- [AVAssetWriterInput.TaggedPixelBufferGroupReceiver](/documentation/avfoundation/avassetwriterinput/taggedpixelbuffergroupreceiver)

##### Appending tagged buffers

- [func append([CMTaggedDynamicBuffer], with: CMTime) async throws](/documentation/avfoundation/avassetwriterinput/taggedpixelbuffergroupreceiver/append(_:with:))
- [func appendImmediately([CMTaggedDynamicBuffer], with: CMTime) throws -> Bool](/documentation/avfoundation/avassetwriterinput/taggedpixelbuffergroupreceiver/appendimmediately(_:with:))
- [func finish()](/documentation/avfoundation/avassetwriterinput/taggedpixelbuffergroupreceiver/finish())

##### Accessing the pixel buffer pool

- [var pixelBufferPool: CVMutablePixelBuffer.Pool?](/documentation/avfoundation/avassetwriterinput/taggedpixelbuffergroupreceiver/pixelbufferpool)
- [var sourcePixelBufferAttributes: CVPixelBufferCreationAttributes?](/documentation/avfoundation/avassetwriterinput/taggedpixelbuffergroupreceiver/sourcepixelbufferattributes)
- [AVAssetWriterInput.MetadataReceiver](/documentation/avfoundation/avassetwriterinput/metadatareceiver)

##### Appending metadata

- [func append(AVTimedMetadataGroup) async throws](/documentation/avfoundation/avassetwriterinput/metadatareceiver/append(_:))
- [func appendImmediately(AVTimedMetadataGroup) throws -> Bool](/documentation/avfoundation/avassetwriterinput/metadatareceiver/appendimmediately(_:))
- [func finish()](/documentation/avfoundation/avassetwriterinput/metadatareceiver/finish())
- [AVAssetWriterInput.CaptionReceiver](/documentation/avfoundation/avassetwriterinput/captionreceiver)

##### Appending captions

- [func append(AVCaptionGroup) async throws](/documentation/avfoundation/avassetwriterinput/captionreceiver/append(_:)-4opbd)
- [func append(AVCaption) async throws](/documentation/avfoundation/avassetwriterinput/captionreceiver/append(_:)-4wpi2)
- [func appendImmediately(AVCaptionGroup) throws -> Bool](/documentation/avfoundation/avassetwriterinput/captionreceiver/appendimmediately(_:)-7q21r)
- [func appendImmediately(AVCaption) throws -> Bool](/documentation/avfoundation/avassetwriterinput/captionreceiver/appendimmediately(_:)-9uy14)
- [func finish()](/documentation/avfoundation/avassetwriterinput/captionreceiver/finish())

#### Performing multiple-pass encoding

- [var canPerformMultiplePasses: Bool](/documentation/avfoundation/avassetwriterinput/canperformmultiplepasses)
- [var currentPassDescription: AVAssetWriterInputPassDescription?](/documentation/avfoundation/avassetwriterinput/currentpassdescription)
- [AVAssetWriterInputPassDescription](/documentation/avfoundation/avassetwriterinputpassdescription)

##### Getting source time ranges

- [var sourceTimeRanges: [NSValue]](/documentation/avfoundation/avassetwriterinputpassdescription/sourcetimeranges)
- [func markCurrentPassAsFinished()](/documentation/avfoundation/avassetwriterinput/markcurrentpassasfinished())
- [var performsMultiPassEncodingIfSupported: Bool](/documentation/avfoundation/avassetwriterinput/performsmultipassencodingifsupported)
- [func respondToEachPassDescription(on: dispatch_queue_t, using: () -> Void)](/documentation/avfoundation/avassetwriterinput/respondtoeachpassdescription(on:using:))
- [AVAssetWriterInput.MultiPassController](/documentation/avfoundation/avassetwriterinput/multipasscontroller)

##### Accessing pass descriptions

- [var passDescriptions: (some AsyncSequence<AVAssetWriterInputPassDescription, Never>)?](/documentation/avfoundation/avassetwriterinput/multipasscontroller/passdescriptions)

#### Inspecting an input

- [var mediaType: AVMediaType](/documentation/avfoundation/avassetwriterinput/mediatype)
- [var outputSettings: [String : Any]?](/documentation/avfoundation/avassetwriterinput/outputsettings)
- [var sourceFormatHint: CMFormatDescription?](/documentation/avfoundation/avassetwriterinput/sourceformathint)
- [AVAssetWriterInputPixelBufferAdaptor](/documentation/avfoundation/avassetwriterinputpixelbufferadaptor)

#### Creating an adaptor

- [init(assetWriterInput: AVAssetWriterInput, sourcePixelBufferAttributes: [String : Any]?)](/documentation/avfoundation/avassetwriterinputpixelbufferadaptor/init(assetwriterinput:sourcepixelbufferattributes:))

#### Appending pixel buffers

- [func append(CVPixelBuffer, withPresentationTime: CMTime) -> Bool](/documentation/avfoundation/avassetwriterinputpixelbufferadaptor/append(_:withpresentationtime:))

#### Accessing the pool

- [var pixelBufferPool: CVPixelBufferPool?](/documentation/avfoundation/avassetwriterinputpixelbufferadaptor/pixelbufferpool)
- [var sourcePixelBufferAttributes: [String : any Sendable]?](/documentation/avfoundation/avassetwriterinputpixelbufferadaptor/sourcepixelbufferattributes)

#### Inspecting a pixel buffer adaptor

- [var assetWriterInput: AVAssetWriterInput](/documentation/avfoundation/avassetwriterinputpixelbufferadaptor/assetwriterinput)
- [AVAssetWriterInputTaggedPixelBufferGroupAdaptor](/documentation/avfoundation/avassetwriterinputtaggedpixelbuffergroupadaptor)

#### Creating an adaptor

- [init(assetWriterInput: AVAssetWriterInput, sourcePixelBufferAttributes: [String : Any]?)](/documentation/avfoundation/avassetwriterinputtaggedpixelbuffergroupadaptor/init(assetwriterinput:sourcepixelbufferattributes:))

#### Configuring the buffer pool

- [var sourcePixelBufferAttributes: [String : any Sendable]?](/documentation/avfoundation/avassetwriterinputtaggedpixelbuffergroupadaptor/sourcepixelbufferattributes)
- [var pixelBufferPool: CVPixelBufferPool?](/documentation/avfoundation/avassetwriterinputtaggedpixelbuffergroupadaptor/pixelbufferpool)

#### Appending pixel buffers

- [func appendTaggedBuffers([CMTaggedBuffer], withPresentationTime: CMTime) -> Bool](/documentation/avfoundation/avassetwriterinputtaggedpixelbuffergroupadaptor/appendtaggedbuffers(_:withpresentationtime:))
- [func appendTaggedPixelBufferGroup(__CMTaggedBufferGroup, withPresentationTime: CMTime) -> Bool](/documentation/avfoundation/avassetwriterinputtaggedpixelbuffergroupadaptor/appendtaggedpixelbuffergroup(_:withpresentationtime:))

#### Accessing the writer input

- [var assetWriterInput: AVAssetWriterInput](/documentation/avfoundation/avassetwriterinputtaggedpixelbuffergroupadaptor/assetwriterinput)
- [AVAssetWriterInputMetadataAdaptor](/documentation/avfoundation/avassetwriterinputmetadataadaptor)

#### Creating an input metadata adaptor

- [init(assetWriterInput: AVAssetWriterInput)](/documentation/avfoundation/avassetwriterinputmetadataadaptor/init(assetwriterinput:))

#### Appending timed metadata

- [func append(AVTimedMetadataGroup) -> Bool](/documentation/avfoundation/avassetwriterinputmetadataadaptor/append(_:))

#### Accessing the input

- [var assetWriterInput: AVAssetWriterInput](/documentation/avfoundation/avassetwriterinputmetadataadaptor/assetwriterinput)
- [AVAssetWriterInputGroup](/documentation/avfoundation/avassetwriterinputgroup)

#### Creating an input group

- [init(inputs: [AVAssetWriterInput], defaultInput: AVAssetWriterInput?)](/documentation/avfoundation/avassetwriterinputgroup/init(inputs:defaultinput:))

#### Accessing the inputs

- [var inputs: [AVAssetWriterInput]](/documentation/avfoundation/avassetwriterinputgroup/inputs)
- [var defaultInput: AVAssetWriterInput?](/documentation/avfoundation/avassetwriterinputgroup/defaultinput)

### Captions

- [Caption authoring](/documentation/avfoundation/caption-authoring)

#### Captions

- [AVCaption](/documentation/avfoundation/avcaption)

##### Creating a caption

- [init(String, timeRange: CMTimeRange)](/documentation/avfoundation/avcaption/init(_:timerange:))

##### Accessing text and timing

- [var text: String](/documentation/avfoundation/avcaption/text)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avcaption/timerange)

##### Accessing the region

- [var region: AVCaptionRegion?](/documentation/avfoundation/avcaption/region)

##### Accessing font styles

- [func fontStyle(at: String.Index) -> (AVCaption.FontStyle, Range<String.Index>)](/documentation/avfoundation/avcaption/fontstyle(at:))
- [AVCaption.FontStyle](/documentation/avfoundation/avcaption/fontstyle)

###### Font styles

- [case unknown](/documentation/avfoundation/avcaption/fontstyle/unknown)
- [case normal](/documentation/avfoundation/avcaption/fontstyle/normal)
- [case italic](/documentation/avfoundation/avcaption/fontstyle/italic)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/fontstyle/init(rawvalue:))
- [func fontWeight(at: String.Index) -> (AVCaption.FontWeight, Range<String.Index>)](/documentation/avfoundation/avcaption/fontweight(at:))
- [AVCaption.FontWeight](/documentation/avfoundation/avcaption/fontweight)

###### Font weights

- [case unknown](/documentation/avfoundation/avcaption/fontweight/unknown)
- [case normal](/documentation/avfoundation/avcaption/fontweight/normal)
- [case bold](/documentation/avfoundation/avcaption/fontweight/bold)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/fontweight/init(rawvalue:))
- [func decoration(at: String.Index) -> (AVCaption.Decoration, Range<String.Index>)](/documentation/avfoundation/avcaption/decoration(at:))
- [AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration)

###### Decorations

- [static var underline: AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration/underline)
- [static var lineThrough: AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration/linethrough)
- [static var overline: AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration/overline)

###### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avcaption/decoration/init(rawvalue:))

##### Accessing colors

- [func textColor(at: String.Index) -> (CGColor?, Range<String.Index>)](/documentation/avfoundation/avcaption/textcolor(at:))
- [func backgroundColor(at: String.Index) -> (CGColor?, Range<String.Index>)](/documentation/avfoundation/avcaption/backgroundcolor(at:))

##### Accessing alignment

- [var textAlignment: AVCaption.TextAlignment](/documentation/avfoundation/avcaption/textalignment-swift.property)
- [AVCaption.TextAlignment](/documentation/avfoundation/avcaption/textalignment-swift.enum)

###### Text alignments

- [case start](/documentation/avfoundation/avcaption/textalignment-swift.enum/start)
- [case end](/documentation/avfoundation/avcaption/textalignment-swift.enum/end)
- [case center](/documentation/avfoundation/avcaption/textalignment-swift.enum/center)
- [case left](/documentation/avfoundation/avcaption/textalignment-swift.enum/left)
- [case right](/documentation/avfoundation/avcaption/textalignment-swift.enum/right)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/textalignment-swift.enum/init(rawvalue:))

##### Accessing animation

- [var animation: AVCaption.Animation](/documentation/avfoundation/avcaption/animation-swift.property)
- [AVCaption.Animation](/documentation/avfoundation/avcaption/animation-swift.enum)

###### Animations

- [case none](/documentation/avfoundation/avcaption/animation-swift.enum/none)
- [case characterReveal](/documentation/avfoundation/avcaption/animation-swift.enum/characterreveal)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/animation-swift.enum/init(rawvalue:))

##### Accessing advanced typography

- [func ruby(at: String.Index) -> (AVCaption.Ruby?, Range<String.Index>)](/documentation/avfoundation/avcaption/ruby(at:))
- [AVCaption.Ruby](/documentation/avfoundation/avcaption/ruby)

###### Creating Ruby text

- [init(text: String)](/documentation/avfoundation/avcaption/ruby/init(text:))
- [convenience init(text: String, position: AVCaptionRubyPosition, alignment: AVCaptionRubyAlignment)](/documentation/avfoundation/avcaption/ruby/init(text:position:alignment:))

###### Accessing text properties

- [var text: String](/documentation/avfoundation/avcaption/ruby/text)
- [var position: AVCaptionRubyPosition](/documentation/avfoundation/avcaption/ruby/position)
- [AVCaptionRubyPosition](/documentation/avfoundation/avcaptionrubyposition)

###### Ruby positions

- [case before](/documentation/avfoundation/avcaptionrubyposition/before)
- [case after](/documentation/avfoundation/avcaptionrubyposition/after)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionrubyposition/init(rawvalue:))
- [var alignment: AVCaptionRubyAlignment](/documentation/avfoundation/avcaption/ruby/alignment)
- [AVCaptionRubyAlignment](/documentation/avfoundation/avcaptionrubyalignment)

###### Text alignments

- [case start](/documentation/avfoundation/avcaptionrubyalignment/start)
- [case center](/documentation/avfoundation/avcaptionrubyalignment/center)
- [case distributeSpaceBetween](/documentation/avfoundation/avcaptionrubyalignment/distributespacebetween)
- [case distributeSpaceAround](/documentation/avfoundation/avcaptionrubyalignment/distributespacearound)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionrubyalignment/init(rawvalue:))
- [func textCombine(at: String.Index) -> (AVCaption.TextCombine, Range<String.Index>)](/documentation/avfoundation/avcaption/textcombine(at:))
- [AVCaption.TextCombine](/documentation/avfoundation/avcaption/textcombine)

###### Text combine options

- [case all](/documentation/avfoundation/avcaption/textcombine/all)
- [case none](/documentation/avfoundation/avcaption/textcombine/none)
- [case oneDigit](/documentation/avfoundation/avcaption/textcombine/onedigit)
- [case twoDigits](/documentation/avfoundation/avcaption/textcombine/twodigits)
- [case threeDigits](/documentation/avfoundation/avcaption/textcombine/threedigits)
- [case fourDigits](/documentation/avfoundation/avcaption/textcombine/fourdigits)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/textcombine/init(rawvalue:))
- [AVMutableCaption](/documentation/avfoundation/avmutablecaption)

##### Configuring text and timing

- [var text: String](/documentation/avfoundation/avmutablecaption/text)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avmutablecaption/timerange)

##### Configuring the region

- [var region: AVCaptionRegion](/documentation/avfoundation/avmutablecaption/region)

##### Configuring font styles

- [AVCaption.FontStyle](/documentation/avfoundation/avcaption/fontstyle)

###### Font styles

- [case unknown](/documentation/avfoundation/avcaption/fontstyle/unknown)
- [case normal](/documentation/avfoundation/avcaption/fontstyle/normal)
- [case italic](/documentation/avfoundation/avcaption/fontstyle/italic)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/fontstyle/init(rawvalue:))
- [func setFontStyle(AVCaption.FontStyle, in: NSRange)](/documentation/avfoundation/avmutablecaption/setfontstyle(_:in:))
- [func removeFontStyle(in: NSRange)](/documentation/avfoundation/avmutablecaption/removefontstyle(in:))
- [AVCaption.FontWeight](/documentation/avfoundation/avcaption/fontweight)

###### Font weights

- [case unknown](/documentation/avfoundation/avcaption/fontweight/unknown)
- [case normal](/documentation/avfoundation/avcaption/fontweight/normal)
- [case bold](/documentation/avfoundation/avcaption/fontweight/bold)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/fontweight/init(rawvalue:))
- [func setFontWeight(AVCaption.FontWeight, in: NSRange)](/documentation/avfoundation/avmutablecaption/setfontweight(_:in:))
- [func removeFontWeight(in: NSRange)](/documentation/avfoundation/avmutablecaption/removefontweight(in:))
- [AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration)

###### Decorations

- [static var underline: AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration/underline)
- [static var lineThrough: AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration/linethrough)
- [static var overline: AVCaption.Decoration](/documentation/avfoundation/avcaption/decoration/overline)

###### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avcaption/decoration/init(rawvalue:))
- [func setDecoration(AVCaption.Decoration, in: NSRange)](/documentation/avfoundation/avmutablecaption/setdecoration(_:in:))
- [func removeDecoration(in: NSRange)](/documentation/avfoundation/avmutablecaption/removedecoration(in:))

##### Configuring colors

- [func setTextColor(CGColor, in: NSRange)](/documentation/avfoundation/avmutablecaption/settextcolor(_:in:))
- [func removeTextColor(in: NSRange)](/documentation/avfoundation/avmutablecaption/removetextcolor(in:))
- [func setBackgroundColor(CGColor, in: NSRange)](/documentation/avfoundation/avmutablecaption/setbackgroundcolor(_:in:))
- [func removeBackgroundColor(in: NSRange)](/documentation/avfoundation/avmutablecaption/removebackgroundcolor(in:))

##### Configuring alignment

- [var textAlignment: AVCaption.TextAlignment](/documentation/avfoundation/avmutablecaption/textalignment)
- [AVCaption.TextAlignment](/documentation/avfoundation/avcaption/textalignment-swift.enum)

###### Text alignments

- [case start](/documentation/avfoundation/avcaption/textalignment-swift.enum/start)
- [case end](/documentation/avfoundation/avcaption/textalignment-swift.enum/end)
- [case center](/documentation/avfoundation/avcaption/textalignment-swift.enum/center)
- [case left](/documentation/avfoundation/avcaption/textalignment-swift.enum/left)
- [case right](/documentation/avfoundation/avcaption/textalignment-swift.enum/right)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/textalignment-swift.enum/init(rawvalue:))

##### Configuring animation

- [var animation: AVCaption.Animation](/documentation/avfoundation/avmutablecaption/animation)
- [AVCaption.Animation](/documentation/avfoundation/avcaption/animation-swift.enum)

###### Animations

- [case none](/documentation/avfoundation/avcaption/animation-swift.enum/none)
- [case characterReveal](/documentation/avfoundation/avcaption/animation-swift.enum/characterreveal)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/animation-swift.enum/init(rawvalue:))

##### Configuring advanced typography

- [AVCaption.Ruby](/documentation/avfoundation/avcaption/ruby)

###### Creating Ruby text

- [init(text: String)](/documentation/avfoundation/avcaption/ruby/init(text:))
- [convenience init(text: String, position: AVCaptionRubyPosition, alignment: AVCaptionRubyAlignment)](/documentation/avfoundation/avcaption/ruby/init(text:position:alignment:))

###### Accessing text properties

- [var text: String](/documentation/avfoundation/avcaption/ruby/text)
- [var position: AVCaptionRubyPosition](/documentation/avfoundation/avcaption/ruby/position)
- [AVCaptionRubyPosition](/documentation/avfoundation/avcaptionrubyposition)

###### Ruby positions

- [case before](/documentation/avfoundation/avcaptionrubyposition/before)
- [case after](/documentation/avfoundation/avcaptionrubyposition/after)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionrubyposition/init(rawvalue:))
- [var alignment: AVCaptionRubyAlignment](/documentation/avfoundation/avcaption/ruby/alignment)
- [AVCaptionRubyAlignment](/documentation/avfoundation/avcaptionrubyalignment)

###### Text alignments

- [case start](/documentation/avfoundation/avcaptionrubyalignment/start)
- [case center](/documentation/avfoundation/avcaptionrubyalignment/center)
- [case distributeSpaceBetween](/documentation/avfoundation/avcaptionrubyalignment/distributespacebetween)
- [case distributeSpaceAround](/documentation/avfoundation/avcaptionrubyalignment/distributespacearound)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionrubyalignment/init(rawvalue:))
- [func setRuby(AVCaption.Ruby, in: NSRange)](/documentation/avfoundation/avmutablecaption/setruby(_:in:))
- [func removeRuby(in: NSRange)](/documentation/avfoundation/avmutablecaption/removeruby(in:))
- [AVCaption.TextCombine](/documentation/avfoundation/avcaption/textcombine)

###### Text combine options

- [case all](/documentation/avfoundation/avcaption/textcombine/all)
- [case none](/documentation/avfoundation/avcaption/textcombine/none)
- [case oneDigit](/documentation/avfoundation/avcaption/textcombine/onedigit)
- [case twoDigits](/documentation/avfoundation/avcaption/textcombine/twodigits)
- [case threeDigits](/documentation/avfoundation/avcaption/textcombine/threedigits)
- [case fourDigits](/documentation/avfoundation/avcaption/textcombine/fourdigits)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaption/textcombine/init(rawvalue:))
- [func setTextCombine(AVCaption.TextCombine, in: NSRange)](/documentation/avfoundation/avmutablecaption/settextcombine(_:in:))
- [func removeTextCombine(in: NSRange)](/documentation/avfoundation/avmutablecaption/removetextcombine(in:))

#### Regions

- [AVCaptionRegion](/documentation/avfoundation/avcaptionregion)

##### Accessing defined regions

- [class var appleITTTop: AVCaptionRegion](/documentation/avfoundation/avcaptionregion/appleitttop)
- [class var appleITTBottom: AVCaptionRegion](/documentation/avfoundation/avcaptionregion/appleittbottom)
- [class var appleITTLeft: AVCaptionRegion](/documentation/avfoundation/avcaptionregion/appleittleft)
- [class var appleITTRight: AVCaptionRegion](/documentation/avfoundation/avcaptionregion/appleittright)
- [class var subRipTextBottom: AVCaptionRegion](/documentation/avfoundation/avcaptionregion/subriptextbottom)

##### Identifying a region

- [var identifier: String?](/documentation/avfoundation/avcaptionregion/identifier)

##### Accessing dimensions

- [AVCaptionDimension](/documentation/avfoundation/avcaptiondimension)

###### Inspecting the dimensions

- [var value: CGFloat](/documentation/avfoundation/avcaptiondimension/value)
- [var units: AVCaptionUnitsType](/documentation/avfoundation/avcaptiondimension/units)
- [AVCaptionUnitsType](/documentation/avfoundation/avcaptionunitstype)

###### Unit types

- [case cells](/documentation/avfoundation/avcaptionunitstype/cells)
- [case percent](/documentation/avfoundation/avcaptionunitstype/percent)
- [case unspecified](/documentation/avfoundation/avcaptionunitstype/unspecified)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionunitstype/init(rawvalue:))

###### Initializers

- [init()](/documentation/avfoundation/avcaptiondimension/init())
- [init(value: CGFloat, units: AVCaptionUnitsType)](/documentation/avfoundation/avcaptiondimension/init(value:units:))

##### Accessing the location

- [var origin: AVCaptionPoint](/documentation/avfoundation/avcaptionregion/origin)
- [AVCaptionPoint](/documentation/avfoundation/avcaptionpoint)

###### Inspecting the point

- [var x: AVCaptionDimension](/documentation/avfoundation/avcaptionpoint/x)
- [var y: AVCaptionDimension](/documentation/avfoundation/avcaptionpoint/y)

###### Initializers

- [init()](/documentation/avfoundation/avcaptionpoint/init())
- [init(x: AVCaptionDimension, y: AVCaptionDimension)](/documentation/avfoundation/avcaptionpoint/init(x:y:))

##### Accessing the size

- [var size: AVCaptionSize](/documentation/avfoundation/avcaptionregion/size)
- [AVCaptionSize](/documentation/avfoundation/avcaptionsize)

###### Inspecting the size

- [var height: AVCaptionDimension](/documentation/avfoundation/avcaptionsize/height)
- [var width: AVCaptionDimension](/documentation/avfoundation/avcaptionsize/width)

###### Initializers

- [init()](/documentation/avfoundation/avcaptionsize/init())
- [init(width: AVCaptionDimension, height: AVCaptionDimension)](/documentation/avfoundation/avcaptionsize/init(width:height:))

##### Accessing the display alignment

- [var displayAlignment: AVCaptionRegion.DisplayAlignment](/documentation/avfoundation/avcaptionregion/displayalignment-swift.property)
- [AVCaptionRegion.DisplayAlignment](/documentation/avfoundation/avcaptionregion/displayalignment-swift.enum)

###### Display alignments

- [case before](/documentation/avfoundation/avcaptionregion/displayalignment-swift.enum/before)
- [case center](/documentation/avfoundation/avcaptionregion/displayalignment-swift.enum/center)
- [case after](/documentation/avfoundation/avcaptionregion/displayalignment-swift.enum/after)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionregion/displayalignment-swift.enum/init(rawvalue:))

##### Accessing the scroll mode

- [var scroll: AVCaptionRegion.Scroll](/documentation/avfoundation/avcaptionregion/scroll-swift.property)
- [AVCaptionRegion.Scroll](/documentation/avfoundation/avcaptionregion/scroll-swift.enum)

###### Scroll values

- [case none](/documentation/avfoundation/avcaptionregion/scroll-swift.enum/none)
- [case rollUp](/documentation/avfoundation/avcaptionregion/scroll-swift.enum/rollup)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionregion/scroll-swift.enum/init(rawvalue:))

##### Accessing the writing mode

- [var writingMode: AVCaptionRegion.WritingMode](/documentation/avfoundation/avcaptionregion/writingmode-swift.property)
- [AVCaptionRegion.WritingMode](/documentation/avfoundation/avcaptionregion/writingmode-swift.enum)

###### Writing modes

- [case leftToRightAndTopToBottom](/documentation/avfoundation/avcaptionregion/writingmode-swift.enum/lefttorightandtoptobottom)
- [case topToBottomAndRightToLeft](/documentation/avfoundation/avcaptionregion/writingmode-swift.enum/toptobottomandrighttoleft)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionregion/writingmode-swift.enum/init(rawvalue:))

##### Processing regions

- [func mutableCopy(with: NSZone?) -> Any](/documentation/avfoundation/avcaptionregion/mutablecopy(with:))
- [func encode(with: NSCoder)](/documentation/avfoundation/avcaptionregion/encode(with:))
- [func isEqual(Any) -> Bool](/documentation/avfoundation/avcaptionregion/isequal(_:))
- [AVMutableCaptionRegion](/documentation/avfoundation/avmutablecaptionregion)

##### Creating a caption region

- [init()](/documentation/avfoundation/avmutablecaptionregion/init())
- [init(identifier: String)](/documentation/avfoundation/avmutablecaptionregion/init(identifier:))

##### Configuring the region

- [var origin: AVCaptionPoint](/documentation/avfoundation/avmutablecaptionregion/origin)
- [var size: AVCaptionSize](/documentation/avfoundation/avmutablecaptionregion/size)
- [var displayAlignment: AVCaptionRegion.DisplayAlignment](/documentation/avfoundation/avmutablecaptionregion/displayalignment)
- [var scroll: AVCaptionRegion.Scroll](/documentation/avfoundation/avmutablecaptionregion/scroll)
- [var writingMode: AVCaptionRegion.WritingMode](/documentation/avfoundation/avmutablecaptionregion/writingmode)

#### Groups

- [AVCaptionGroup](/documentation/avfoundation/avcaptiongroup)

##### Creating a caption group

- [init(timeRange: CMTimeRange)](/documentation/avfoundation/avcaptiongroup/init(timerange:))
- [init(captions: [AVCaption], timeRange: CMTimeRange)](/documentation/avfoundation/avcaptiongroup/init(captions:timerange:))

##### Inspecting the caption group

- [var captions: [AVCaption]](/documentation/avfoundation/avcaptiongroup/captions)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avcaptiongroup/timerange)
- [AVCaptionGrouper](/documentation/avfoundation/avcaptiongrouper)

##### Adding captions

- [func add(AVCaption)](/documentation/avfoundation/avcaptiongrouper/add(_:))

##### Generating captions groups

- [func flushAddedCaptions(upTo: CMTime) -> [AVCaptionGroup]](/documentation/avfoundation/avcaptiongrouper/flushaddedcaptions(upto:))

#### Presentation

- [AVCaptionRenderer](/documentation/avfoundation/avcaptionrenderer)

##### Configuring the renderer

- [var captions: [AVCaption]](/documentation/avfoundation/avcaptionrenderer/captions)
- [var bounds: CGRect](/documentation/avfoundation/avcaptionrenderer/bounds)

##### Determining scene changes

- [func captionSceneChanges(in: CMTimeRange) -> [AVCaptionRenderer.Scene]](/documentation/avfoundation/avcaptionrenderer/captionscenechanges(in:))
- [AVCaptionRenderer.Scene](/documentation/avfoundation/avcaptionrenderer/scene)

###### Inspecting the scene

- [var timeRange: CMTimeRange](/documentation/avfoundation/avcaptionrenderer/scene/timerange)
- [var hasActiveCaptions: Bool](/documentation/avfoundation/avcaptionrenderer/scene/hasactivecaptions)
- [var needsPeriodicRefresh: Bool](/documentation/avfoundation/avcaptionrenderer/scene/needsperiodicrefresh)

##### Rendering a caption

- [func render(in: CGContext, for: CMTime)](/documentation/avfoundation/avcaptionrenderer/render(in:for:))

#### Reading and writing

- [AVAssetReaderOutputCaptionAdaptor](/documentation/avfoundation/avassetreaderoutputcaptionadaptor)

##### Creating a caption adaptor

- [init(assetReaderTrackOutput: AVAssetReaderTrackOutput)](/documentation/avfoundation/avassetreaderoutputcaptionadaptor/init(assetreadertrackoutput:))

##### Accessing the track output

- [var assetReaderTrackOutput: AVAssetReaderTrackOutput](/documentation/avfoundation/avassetreaderoutputcaptionadaptor/assetreadertrackoutput)

##### Managing the validation delegate

- [var validationDelegate: (any AVAssetReaderCaptionValidationHandling)?](/documentation/avfoundation/avassetreaderoutputcaptionadaptor/validationdelegate)
- [AVAssetReaderCaptionValidationHandling](/documentation/avfoundation/avassetreadercaptionvalidationhandling)

###### Validating captions

- [func captionAdaptor(AVAssetReaderOutputCaptionAdaptor, didVendCaption: AVCaption, skippingUnsupportedSourceSyntaxElements: [String])](/documentation/avfoundation/avassetreadercaptionvalidationhandling/captionadaptor(_:didvendcaption:skippingunsupportedsourcesyntaxelements:))

##### Reading caption groups

- [func nextCaptionGroup() -> AVCaptionGroup?](/documentation/avfoundation/avassetreaderoutputcaptionadaptor/nextcaptiongroup())
- [func captionsNotPresentInPreviousGroups(in: AVCaptionGroup) -> [AVCaption]](/documentation/avfoundation/avassetreaderoutputcaptionadaptor/captionsnotpresentinpreviousgroups(in:))
- [AVAssetWriterInputCaptionAdaptor](/documentation/avfoundation/avassetwriterinputcaptionadaptor)

##### Creating a caption adaptor

- [init(assetWriterInput: AVAssetWriterInput)](/documentation/avfoundation/avassetwriterinputcaptionadaptor/init(assetwriterinput:))

##### Accessing the writer input

- [var assetWriterInput: AVAssetWriterInput](/documentation/avfoundation/avassetwriterinputcaptionadaptor/assetwriterinput)

##### Appending captions

- [func append(AVCaption) -> Bool](/documentation/avfoundation/avassetwriterinputcaptionadaptor/append(_:)-910lp)
- [func append(AVCaptionGroup) -> Bool](/documentation/avfoundation/avassetwriterinputcaptionadaptor/append(_:)-4ils8)

#### Conversion and validation

- [AVCaptionSettingsKey](/documentation/avfoundation/avcaptionsettingskey)

##### Keys

- [static let mediaType: AVCaptionSettingsKey](/documentation/avfoundation/avcaptionsettingskey/mediatype)
- [static let mediaSubType: AVCaptionSettingsKey](/documentation/avfoundation/avcaptionsettingskey/mediasubtype)
- [static let timeCodeFrameDuration: AVCaptionSettingsKey](/documentation/avfoundation/avcaptionsettingskey/timecodeframeduration)
- [static let useDropFrameTimeCode: AVCaptionSettingsKey](/documentation/avfoundation/avcaptionsettingskey/usedropframetimecode)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcaptionsettingskey/init(rawvalue:))
- [AVCaptionFormatConformer](/documentation/avfoundation/avcaptionformatconformer)

##### Creating a format conformer

- [init(conversionSettings: [AVCaptionSettingsKey : Any])](/documentation/avfoundation/avcaptionformatconformer/init(conversionsettings:))

##### Conforming captions

- [var conformsCaptionsToTimeRange: Bool](/documentation/avfoundation/avcaptionformatconformer/conformscaptionstotimerange)
- [func conformedCaption(for: AVCaption) throws -> AVCaption](/documentation/avfoundation/avcaptionformatconformer/conformedcaption(for:))
- [AVCaptionConversionValidator](/documentation/avfoundation/avcaptionconversionvalidator)

##### Creating a validator

- [init(captions: [AVCaption], timeRange: CMTimeRange, conversionSettings: [AVCaptionSettingsKey : Any])](/documentation/avfoundation/avcaptionconversionvalidator/init(captions:timerange:conversionsettings:))

##### Inspecting the validator

- [var captions: [AVCaption]](/documentation/avfoundation/avcaptionconversionvalidator/captions)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avcaptionconversionvalidator/timerange)

##### Validating captions

- [func validateCaptionConversion(warningHandler: (AVCaptionConversionWarning?) -> Void)](/documentation/avfoundation/avcaptionconversionvalidator/validatecaptionconversion(warninghandler:))
- [var warnings: [AVCaptionConversionWarning]](/documentation/avfoundation/avcaptionconversionvalidator/warnings)
- [AVCaptionConversionWarning](/documentation/avfoundation/avcaptionconversionwarning)

###### Inspecting the warning

- [var warningType: AVCaptionConversionWarning.WarningType](/documentation/avfoundation/avcaptionconversionwarning/warningtype-swift.property)
- [var rangeOfCaptions: NSRange](/documentation/avfoundation/avcaptionconversionwarning/rangeofcaptions)
- [var adjustment: AVCaptionConversionAdjustment?](/documentation/avfoundation/avcaptionconversionwarning/adjustment)
- [AVCaptionConversionAdjustment](/documentation/avfoundation/avcaptionconversionadjustment)

###### Accessing the adjustment type

- [var adjustmentType: AVCaptionConversionAdjustment.AdjustmentType](/documentation/avfoundation/avcaptionconversionadjustment/adjustmenttype-swift.property)
- [AVCaptionConversionAdjustment.AdjustmentType](/documentation/avfoundation/avcaptionconversionadjustment/adjustmenttype-swift.struct)

###### Adjustment types

- [static let timeRange: AVCaptionConversionAdjustment.AdjustmentType](/documentation/avfoundation/avcaptionconversionadjustment/adjustmenttype-swift.struct/timerange)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcaptionconversionadjustment/adjustmenttype-swift.struct/init(rawvalue:))
- [AVCaptionConversionTimeRangeAdjustment](/documentation/avfoundation/avcaptionconversiontimerangeadjustment)

###### Accessing time offsets

- [var startTimeOffset: CMTime](/documentation/avfoundation/avcaptionconversiontimerangeadjustment/starttimeoffset)
- [var durationOffset: CMTime](/documentation/avfoundation/avcaptionconversiontimerangeadjustment/durationoffset)
- [AVCaptionConversionWarning.WarningType](/documentation/avfoundation/avcaptionconversionwarning/warningtype-swift.struct)

###### Warning types

- [static let excessMediaData: AVCaptionConversionWarning.WarningType](/documentation/avfoundation/avcaptionconversionwarning/warningtype-swift.struct/excessmediadata)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcaptionconversionwarning/warningtype-swift.struct/init(rawvalue:))
- [func stopValidating()](/documentation/avfoundation/avcaptionconversionvalidator/stopvalidating())

##### Checking the status

- [var status: AVCaptionConversionValidator.Status](/documentation/avfoundation/avcaptionconversionvalidator/status-swift.property)
- [AVCaptionConversionValidator.Status](/documentation/avfoundation/avcaptionconversionvalidator/status-swift.enum)

###### Validation statuses

- [case unknown](/documentation/avfoundation/avcaptionconversionvalidator/status-swift.enum/unknown)
- [case validating](/documentation/avfoundation/avcaptionconversionvalidator/status-swift.enum/validating)
- [case completed](/documentation/avfoundation/avcaptionconversionvalidator/status-swift.enum/completed)
- [case stopped](/documentation/avfoundation/avcaptionconversionvalidator/status-swift.enum/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptionconversionvalidator/status-swift.enum/init(rawvalue:))
- [Media types and utilities](/documentation/avfoundation/media-types-and-utilities)

### Media types

- [AVMediaType](/documentation/avfoundation/avmediatype)

#### Media types

- [static let audio: AVMediaType](/documentation/avfoundation/avmediatype/audio)
- [static let auxiliaryPicture: AVMediaType](/documentation/avfoundation/avmediatype/auxiliarypicture)
- [static let closedCaption: AVMediaType](/documentation/avfoundation/avmediatype/closedcaption)
- [static let depthData: AVMediaType](/documentation/avfoundation/avmediatype/depthdata)
- [static let haptic: AVMediaType](/documentation/avfoundation/avmediatype/haptic)
- [static let metadata: AVMediaType](/documentation/avfoundation/avmediatype/metadata)
- [static let metadataObject: AVMediaType](/documentation/avfoundation/avmediatype/metadataobject)
- [static let muxed: AVMediaType](/documentation/avfoundation/avmediatype/muxed)
- [static let subtitle: AVMediaType](/documentation/avfoundation/avmediatype/subtitle)
- [static let text: AVMediaType](/documentation/avfoundation/avmediatype/text)
- [static let timecode: AVMediaType](/documentation/avfoundation/avmediatype/timecode)
- [static let video: AVMediaType](/documentation/avfoundation/avmediatype/video)

#### Initializers

- [init(String)](/documentation/avfoundation/avmediatype/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avmediatype/init(rawvalue:))
- [AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic)

#### Visual

- [static let visual: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/visual)
- [static let containsAlphaChannel: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/containsalphachannel)
- [static let containsHDRVideo: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/containshdrvideo)
- [static let frameBased: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/framebased)
- [static let usesWideGamutColorSpace: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/useswidegamutcolorspace)
- [static let containsStereoMultiviewVideo: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/containsstereomultiviewvideo)
- [static let carriesVideoStereoMetadata: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/carriesvideostereometadata)
- [static let indicatesHorizontalFieldOfView: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/indicateshorizontalfieldofview)
- [static let indicatesNonRectilinearProjection: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/indicatesnonrectilinearprojection)

#### Audible

- [static let audible: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/audible)
- [static let dubbedTranslation: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/dubbedtranslation)
- [static let voiceOverTranslation: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/voiceovertranslation)
- [static let enhancesSpeechIntelligibility: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/enhancesspeechintelligibility)
- [static let describesMusicAndSoundForAccessibility: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/describesmusicandsoundforaccessibility)
- [static let tactileMinimal: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/tactileminimal)

#### Legible

- [static let legible: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/legible)
- [static let easyToRead: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/easytoread)
- [static let describesVideoForAccessibility: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/describesvideoforaccessibility)
- [static let containsOnlyForcedSubtitles: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/containsonlyforcedsubtitles)
- [static let languageTranslation: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/languagetranslation)
- [static let transcribesSpokenDialogForAccessibility: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/transcribesspokendialogforaccessibility)

#### Content

- [static let isOriginalContent: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/isoriginalcontent)
- [static let isMainProgramContent: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/ismainprogramcontent)
- [static let isAuxiliaryContent: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/isauxiliarycontent)
- [static let machineGenerated: AVMediaCharacteristic](/documentation/avfoundation/avmediacharacteristic/machinegenerated)

#### Initializers

- [init(String)](/documentation/avfoundation/avmediacharacteristic/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avmediacharacteristic/init(rawvalue:))

### File types

- [AVFileType](/documentation/avfoundation/avfiletype)

#### File types

- [static let AHAP: AVFileType](/documentation/avfoundation/avfiletype/ahap)
- [static let SCC: AVFileType](/documentation/avfoundation/avfiletype/scc)
- [static let ac3: AVFileType](/documentation/avfoundation/avfiletype/ac3)
- [static let aifc: AVFileType](/documentation/avfoundation/avfiletype/aifc)
- [static let aiff: AVFileType](/documentation/avfoundation/avfiletype/aiff)
- [static let amr: AVFileType](/documentation/avfoundation/avfiletype/amr)
- [static let appleiTT: AVFileType](/documentation/avfoundation/avfiletype/appleitt)
- [static let au: AVFileType](/documentation/avfoundation/avfiletype/au)
- [static let avci: AVFileType](/documentation/avfoundation/avfiletype/avci)
- [static let caf: AVFileType](/documentation/avfoundation/avfiletype/caf)
- [static let dcm: AVFileType](/documentation/avfoundation/avfiletype/dcm)
- [static let dng: AVFileType](/documentation/avfoundation/avfiletype/dng)
- [static let eac3: AVFileType](/documentation/avfoundation/avfiletype/eac3)
- [static let heic: AVFileType](/documentation/avfoundation/avfiletype/heic)
- [static let heif: AVFileType](/documentation/avfoundation/avfiletype/heif)
- [static let jpg: AVFileType](/documentation/avfoundation/avfiletype/jpg)
- [static let m4a: AVFileType](/documentation/avfoundation/avfiletype/m4a)
- [static let m4v: AVFileType](/documentation/avfoundation/avfiletype/m4v)
- [static let mobile3GPP2: AVFileType](/documentation/avfoundation/avfiletype/mobile3gpp2)
- [static let mobile3GPP: AVFileType](/documentation/avfoundation/avfiletype/mobile3gpp)
- [static let mov: AVFileType](/documentation/avfoundation/avfiletype/mov)
- [static let mp3: AVFileType](/documentation/avfoundation/avfiletype/mp3)
- [static let mp4: AVFileType](/documentation/avfoundation/avfiletype/mp4)
- [static let qta: AVFileType](/documentation/avfoundation/avfiletype/qta)
- [static let tif: AVFileType](/documentation/avfoundation/avfiletype/tif)
- [static let wav: AVFileType](/documentation/avfoundation/avfiletype/wav)

#### Initializers

- [init(String)](/documentation/avfoundation/avfiletype/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avfiletype/init(rawvalue:))
- [AVFileTypeProfile](/documentation/avfoundation/avfiletypeprofile)

#### File type profiles

- [static let mpeg4AppleHLS: AVFileTypeProfile](/documentation/avfoundation/avfiletypeprofile/mpeg4applehls)
- [static let mpeg4CMAFCompliant: AVFileTypeProfile](/documentation/avfoundation/avfiletypeprofile/mpeg4cmafcompliant)

#### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avfiletypeprofile/init(rawvalue:))

### Utilities

- [func AVMakeRect(aspectRatio: CGSize, insideRect: CGRect) -> CGRect](/documentation/avfoundation/avmakerect(aspectratio:insiderect:))
- [Video settings](/documentation/avfoundation/video-settings)

### Clean aperture

- [let AVVideoCleanApertureKey: String](/documentation/avfoundation/avvideocleanaperturekey)
- [let AVVideoCleanApertureWidthKey: String](/documentation/avfoundation/avvideocleanaperturewidthkey)
- [let AVVideoCleanApertureHeightKey: String](/documentation/avfoundation/avvideocleanapertureheightkey)
- [let AVVideoCleanApertureVerticalOffsetKey: String](/documentation/avfoundation/avvideocleanapertureverticaloffsetkey)
- [let AVVideoCleanApertureHorizontalOffsetKey: String](/documentation/avfoundation/avvideocleanaperturehorizontaloffsetkey)

### Video codecs

- [let AVVideoCodecKey: String](/documentation/avfoundation/avvideocodeckey)
- [AVVideoCodecType](/documentation/avfoundation/avvideocodectype)

#### Video codecs

- [static let h264: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/h264)
- [static let hevc: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevc)
- [static let hevcWithAlpha: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevcwithalpha)
- [static let jpeg: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpeg)
- [static let JPEGXL: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpegxl)
- [static let proRes422: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422)
- [static let proRes422LT: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422lt)
- [static let proRes422HQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422hq)
- [static let proRes422Proxy: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422proxy)
- [static let proRes4444: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores4444)
- [static let proResRAW: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresraw)
- [static let proResRAWHQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresrawhq)
- [static let appleProRes4444XQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/appleprores4444xq)

#### Deprecated

- [let AVVideoCodecH264: String](/documentation/avfoundation/avvideocodech264)
- [let AVVideoCodecHEVC: String](/documentation/avfoundation/avvideocodechevc)
- [let AVVideoCodecJPEG: String](/documentation/avfoundation/avvideocodecjpeg)
- [let AVVideoCodecAppleProRes422: String](/documentation/avfoundation/avvideocodecappleprores422)
- [let AVVideoCodecAppleProRes4444: String](/documentation/avfoundation/avvideocodecappleprores4444)

#### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideocodectype/init(rawvalue:))

### Color properties

- [Setting color properties for a specific resolution](/documentation/avfoundation/setting-color-properties-for-a-specific-resolution)
- [let AVVideoAllowWideColorKey: String](/documentation/avfoundation/avvideoallowwidecolorkey)
- [let AVVideoColorPrimariesKey: String](/documentation/avfoundation/avvideocolorprimarieskey)
- [let AVVideoColorPrimaries_EBU_3213: String](/documentation/avfoundation/avvideocolorprimaries_ebu_3213)
- [let AVVideoColorPrimaries_ITU_R_2020: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_2020)
- [let AVVideoColorPrimaries_ITU_R_709_2: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_709_2)
- [let AVVideoColorPrimaries_P3_D65: String](/documentation/avfoundation/avvideocolorprimaries_p3_d65)
- [let AVVideoColorPrimaries_SMPTE_C: String](/documentation/avfoundation/avvideocolorprimaries_smpte_c)
- [let AVVideoColorPropertiesKey: String](/documentation/avfoundation/avvideocolorpropertieskey)
- [let AVVideoTransferFunctionKey: String](/documentation/avfoundation/avvideotransferfunctionkey)
- [let AVVideoTransferFunction_IEC_sRGB: String](/documentation/avfoundation/avvideotransferfunction_iec_srgb)
- [let AVVideoTransferFunction_ITU_R_2100_HLG: String](/documentation/avfoundation/avvideotransferfunction_itu_r_2100_hlg)
- [let AVVideoTransferFunction_ITU_R_709_2: String](/documentation/avfoundation/avvideotransferfunction_itu_r_709_2)
- [let AVVideoTransferFunction_Linear: String](/documentation/avfoundation/avvideotransferfunction_linear)
- [let AVVideoTransferFunction_SMPTE_240M_1995: String](/documentation/avfoundation/avvideotransferfunction_smpte_240m_1995)
- [let AVVideoTransferFunction_SMPTE_ST_2084_PQ: String](/documentation/avfoundation/avvideotransferfunction_smpte_st_2084_pq)
- [let AVVideoYCbCrMatrixKey: String](/documentation/avfoundation/avvideoycbcrmatrixkey)
- [let AVVideoYCbCrMatrix_ITU_R_2020: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_2020)
- [let AVVideoYCbCrMatrix_ITU_R_601_4: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_601_4)
- [let AVVideoYCbCrMatrix_ITU_R_709_2: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_709_2)
- [let AVVideoYCbCrMatrix_SMPTE_240M_1995: String](/documentation/avfoundation/avvideoycbcrmatrix_smpte_240m_1995)

### Compression

- [let AVVideoCompressionPropertiesKey: String](/documentation/avfoundation/avvideocompressionpropertieskey)
- [let AVVideoDecompressionPropertiesKey: String](/documentation/avfoundation/avvideodecompressionpropertieskey)
- [let AVVideoAverageBitRateKey: String](/documentation/avfoundation/avvideoaveragebitratekey)
- [let AVVideoQualityKey: String](/documentation/avfoundation/avvideoqualitykey)
- [let AVVideoMaxKeyFrameIntervalKey: String](/documentation/avfoundation/avvideomaxkeyframeintervalkey)
- [let AVVideoMaxKeyFrameIntervalDurationKey: String](/documentation/avfoundation/avvideomaxkeyframeintervaldurationkey)
- [let AVVideoAllowFrameReorderingKey: String](/documentation/avfoundation/avvideoallowframereorderingkey)
- [let AVVideoAppleProRAWBitDepthKey: String](/documentation/avfoundation/avvideoappleprorawbitdepthkey)

### Entropy mode

- [let AVVideoH264EntropyModeKey: String](/documentation/avfoundation/avvideoh264entropymodekey)
- [let AVVideoH264EntropyModeCABAC: String](/documentation/avfoundation/avvideoh264entropymodecabac)
- [let AVVideoH264EntropyModeCAVLC: String](/documentation/avfoundation/avvideoh264entropymodecavlc)

### FairPlay

- [let AVStreamingKeyDeliveryContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverycontentkeytype)
- [let AVStreamingKeyDeliveryPersistentContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverypersistentcontentkeytype)

### Frame rate

- [let AVVideoExpectedSourceFrameRateKey: String](/documentation/avfoundation/avvideoexpectedsourceframeratekey)
- [let AVVideoAverageNonDroppableFrameRateKey: String](/documentation/avfoundation/avvideoaveragenondroppableframeratekey)

### Geometry

- [let AVVideoWidthKey: String](/documentation/avfoundation/avvideowidthkey)
- [let AVVideoHeightKey: String](/documentation/avfoundation/avvideoheightkey)
- [let AVVideoPixelAspectRatioKey: String](/documentation/avfoundation/avvideopixelaspectratiokey)
- [let AVVideoPixelAspectRatioVerticalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratioverticalspacingkey)
- [let AVVideoPixelAspectRatioHorizontalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratiohorizontalspacingkey)

### Profile level

- [let AVVideoProfileLevelKey: String](/documentation/avfoundation/avvideoprofilelevelkey)
- [let AVVideoProfileLevelH264High40: String](/documentation/avfoundation/avvideoprofilelevelh264high40)
- [let AVVideoProfileLevelH264High41: String](/documentation/avfoundation/avvideoprofilelevelh264high41)
- [let AVVideoProfileLevelH264Main30: String](/documentation/avfoundation/avvideoprofilelevelh264main30)
- [let AVVideoProfileLevelH264Main31: String](/documentation/avfoundation/avvideoprofilelevelh264main31)
- [let AVVideoProfileLevelH264Main32: String](/documentation/avfoundation/avvideoprofilelevelh264main32)
- [let AVVideoProfileLevelH264Main41: String](/documentation/avfoundation/avvideoprofilelevelh264main41)
- [let AVVideoProfileLevelH264Baseline30: String](/documentation/avfoundation/avvideoprofilelevelh264baseline30)
- [let AVVideoProfileLevelH264Baseline31: String](/documentation/avfoundation/avvideoprofilelevelh264baseline31)
- [let AVVideoProfileLevelH264Baseline41: String](/documentation/avfoundation/avvideoprofilelevelh264baseline41)
- [let AVVideoProfileLevelH264HighAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264highautolevel)
- [let AVVideoProfileLevelH264MainAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264mainautolevel)
- [let AVVideoProfileLevelH264BaselineAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264baselineautolevel)

### Scaling mode

- [let AVVideoScalingModeFit: String](/documentation/avfoundation/avvideoscalingmodefit)
- [let AVVideoScalingModeKey: String](/documentation/avfoundation/avvideoscalingmodekey)
- [let AVVideoScalingModeResize: String](/documentation/avfoundation/avvideoscalingmoderesize)
- [let AVVideoScalingModeResizeAspect: String](/documentation/avfoundation/avvideoscalingmoderesizeaspect)
- [let AVVideoScalingModeResizeAspectFill: String](/documentation/avfoundation/avvideoscalingmoderesizeaspectfill)

### VideoToolbox options

- [let AVVideoEncoderSpecificationKey: String](/documentation/avfoundation/avvideoencoderspecificationkey)
- [Audio settings](/documentation/avfoundation/audio-settings)

### Formats

- [AVAudioFormat](/documentation/avfaudio/avaudioformat)
- [AVAudioChannelLayout](/documentation/avfaudio/avaudiochannellayout)
- [let AVChannelLayoutKey: String](/documentation/avfaudio/avchannellayoutkey)
- [Linear PCM format settings](/documentation/avfoundation/linear-pcm-format-settings)

#### Settings

- [let AVLinearPCMBitDepthKey: String](/documentation/avfaudio/avlinearpcmbitdepthkey)
- [let AVLinearPCMIsBigEndianKey: String](/documentation/avfaudio/avlinearpcmisbigendiankey)
- [let AVLinearPCMIsFloatKey: String](/documentation/avfaudio/avlinearpcmisfloatkey)
- [let AVLinearPCMIsNonInterleaved: String](/documentation/avfaudio/avlinearpcmisnoninterleaved)
- [Format settings](/documentation/avfoundation/format-settings)

#### Settings

- [let AVFormatIDKey: String](/documentation/avfaudio/avformatidkey)
- [let AVSampleRateKey: String](/documentation/avfaudio/avsampleratekey)
- [let AVNumberOfChannelsKey: String](/documentation/avfaudio/avnumberofchannelskey)

### Settings

- [Sample rate conversion settings](/documentation/avfoundation/sample-rate-conversion-settings)

#### Constants

- [let AVSampleRateConverterAudioQualityKey: String](/documentation/avfaudio/avsamplerateconverteraudioqualitykey)
- [let AVEncoderAudioQualityForVBRKey: String](/documentation/avfaudio/avencoderaudioqualityforvbrkey)
- [let AVSampleRateConverterAlgorithmKey: String](/documentation/avfaudio/avsamplerateconverteralgorithmkey)
- [AVAudioQuality](/documentation/avfaudio/avaudioquality)
- [Encoder settings](/documentation/avfoundation/encoder-settings)

#### Settings

- [let AVEncoderAudioQualityKey: String](/documentation/avfaudio/avencoderaudioqualitykey)
- [let AVEncoderBitRateKey: String](/documentation/avfaudio/avencoderbitratekey)
- [let AVEncoderBitRatePerChannelKey: String](/documentation/avfaudio/avencoderbitrateperchannelkey)
- [let AVEncoderBitRateStrategyKey: String](/documentation/avfaudio/avencoderbitratestrategykey)
- [let AVEncoderBitDepthHintKey: String](/documentation/avfaudio/avencoderbitdepthhintkey)
- [Time pitch algorithm settings](/documentation/avfoundation/time-pitch-algorithm-settings)

#### Constants

- [static let timeDomain: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/timedomain)
- [static let varispeed: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/varispeed)
- [static let spectral: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/spectral)
- [static let lowQualityZeroLatency: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/lowqualityzerolatency)

### Constants

- [Encoder bit rate strategy values](/documentation/avfoundation/encoder-bit-rate-strategy-values)

#### Strategies

- [let AVAudioBitRateStrategy_Constant: String](/documentation/avfaudio/avaudiobitratestrategy_constant)
- [let AVAudioBitRateStrategy_LongTermAverage: String](/documentation/avfaudio/avaudiobitratestrategy_longtermaverage)
- [let AVAudioBitRateStrategy_VariableConstrained: String](/documentation/avfaudio/avaudiobitratestrategy_variableconstrained)
- [let AVAudioBitRateStrategy_Variable: String](/documentation/avfaudio/avaudiobitratestrategy_variable)
- [var AVAUDIOENGINE_HAVE_AUAUDIOUNIT: Int32](/documentation/avfaudio/avaudioengine_have_auaudiounit)

## Playback

- [Media playback](/documentation/avfoundation/media-playback)

### Essentials

- [Configuring your app for media playback](/documentation/avfoundation/configuring-your-app-for-media-playback)

### Playback control

- [Observing playback state in SwiftUI](/documentation/avfoundation/observing-playback-state-in-swiftui)
- [Controlling the transport behavior of a player](/documentation/avfoundation/controlling-the-transport-behavior-of-a-player)
- [Creating a seamless multiview playback experience](/documentation/avfoundation/creating-a-seamless-multiview-playback-experience)
- [AVPlayer](/documentation/avfoundation/avplayer)

#### Creating a player

- [init(url: URL)](/documentation/avfoundation/avplayer/init(url:))
- [init(playerItem: AVPlayerItem?)](/documentation/avfoundation/avplayer/init(playeritem:))
- [init()](/documentation/avfoundation/avplayer/init())

#### Managing the player item

- [var currentItem: AVPlayerItem?](/documentation/avfoundation/avplayer/currentitem)
- [func replaceCurrentItem(with: AVPlayerItem?)](/documentation/avfoundation/avplayer/replacecurrentitem(with:))

#### Determining player readiness

- [var status: AVPlayer.Status](/documentation/avfoundation/avplayer/status-swift.property)
- [AVPlayer.Status](/documentation/avfoundation/avplayer/status-swift.enum)

##### Status values

- [case unknown](/documentation/avfoundation/avplayer/status-swift.enum/unknown)
- [case readyToPlay](/documentation/avfoundation/avplayer/status-swift.enum/readytoplay)
- [case failed](/documentation/avfoundation/avplayer/status-swift.enum/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayer/status-swift.enum/init(rawvalue:))
- [var error: (any Error)?](/documentation/avfoundation/avplayer/error)

#### Controlling playback

- [var defaultRate: Float](/documentation/avfoundation/avplayer/defaultrate)
- [func play()](/documentation/avfoundation/avplayer/play())
- [func pause()](/documentation/avfoundation/avplayer/pause())
- [var rate: Float](/documentation/avfoundation/avplayer/rate)
- [class let rateDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayer/ratedidchangenotification)

##### User information keys

- [class let rateDidChangeOriginatingParticipantKey: String](/documentation/avfoundation/avplayer/ratedidchangeoriginatingparticipantkey)
- [class let rateDidChangeReasonKey: String](/documentation/avfoundation/avplayer/ratedidchangereasonkey)
- [AVPlayer.RateDidChangeReason](/documentation/avfoundation/avplayer/ratedidchangereason)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avplayer/ratedidchangereason/init(rawvalue:))

###### Rate change reasons

- [static let appBackgrounded: AVPlayer.RateDidChangeReason](/documentation/avfoundation/avplayer/ratedidchangereason/appbackgrounded)
- [static let audioSessionInterrupted: AVPlayer.RateDidChangeReason](/documentation/avfoundation/avplayer/ratedidchangereason/audiosessioninterrupted)
- [static let setRateCalled: AVPlayer.RateDidChangeReason](/documentation/avfoundation/avplayer/ratedidchangereason/setratecalled)
- [static let setRateFailed: AVPlayer.RateDidChangeReason](/documentation/avfoundation/avplayer/ratedidchangereason/setratefailed)

#### Observing playback time

- [func currentTime() -> CMTime](/documentation/avfoundation/avplayer/currenttime())
- [func addPeriodicTimeObserver(forInterval: CMTime, queue: dispatch_queue_t?, using: (CMTime) -> Void) -> Any](/documentation/avfoundation/avplayer/addperiodictimeobserver(forinterval:queue:using:))
- [func addBoundaryTimeObserver(forTimes: [NSValue], queue: dispatch_queue_t?, using: () -> Void) -> Any](/documentation/avfoundation/avplayer/addboundarytimeobserver(fortimes:queue:using:))
- [func removeTimeObserver(Any)](/documentation/avfoundation/avplayer/removetimeobserver(_:))

#### Seeking through media

- [func seek(to: CMTime)](/documentation/avfoundation/avplayer/seek(to:)-87h2r)
- [func seek(to: CMTime, completionHandler: (Bool) -> Void)](/documentation/avfoundation/avplayer/seek(to:completionhandler:)-75bls)
- [func seek(to: CMTime, toleranceBefore: CMTime, toleranceAfter: CMTime)](/documentation/avfoundation/avplayer/seek(to:tolerancebefore:toleranceafter:))
- [func seek(to: CMTime, toleranceBefore: CMTime, toleranceAfter: CMTime, completionHandler: (Bool) -> Void)](/documentation/avfoundation/avplayer/seek(to:tolerancebefore:toleranceafter:completionhandler:))
- [func seek(to: Date)](/documentation/avfoundation/avplayer/seek(to:)-9h9qr)
- [func seek(to: Date, completionHandler: (Bool) -> Void)](/documentation/avfoundation/avplayer/seek(to:completionhandler:)-wr1l)

#### Configuring waiting behavior

- [var automaticallyWaitsToMinimizeStalling: Bool](/documentation/avfoundation/avplayer/automaticallywaitstominimizestalling)
- [var reasonForWaitingToPlay: AVPlayer.WaitingReason?](/documentation/avfoundation/avplayer/reasonforwaitingtoplay)
- [AVPlayer.WaitingReason](/documentation/avfoundation/avplayer/waitingreason)

##### Player waiting reasons

- [static let evaluatingBufferingRate: AVPlayer.WaitingReason](/documentation/avfoundation/avplayer/waitingreason/evaluatingbufferingrate)
- [static let noItemToPlay: AVPlayer.WaitingReason](/documentation/avfoundation/avplayer/waitingreason/noitemtoplay)
- [static let toMinimizeStalls: AVPlayer.WaitingReason](/documentation/avfoundation/avplayer/waitingreason/tominimizestalls)
- [static let interstitialEvent: AVPlayer.WaitingReason](/documentation/avfoundation/avplayer/waitingreason/interstitialevent)
- [static let waitingForCoordinatedPlayback: AVPlayer.WaitingReason](/documentation/avfoundation/avplayer/waitingreason/waitingforcoordinatedplayback)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avplayer/waitingreason/init(rawvalue:))
- [var timeControlStatus: AVPlayer.TimeControlStatus](/documentation/avfoundation/avplayer/timecontrolstatus-swift.property)
- [AVPlayer.TimeControlStatus](/documentation/avfoundation/avplayer/timecontrolstatus-swift.enum)

##### Status values

- [case paused](/documentation/avfoundation/avplayer/timecontrolstatus-swift.enum/paused)
- [case waitingToPlayAtSpecifiedRate](/documentation/avfoundation/avplayer/timecontrolstatus-swift.enum/waitingtoplayatspecifiedrate)
- [case playing](/documentation/avfoundation/avplayer/timecontrolstatus-swift.enum/playing)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayer/timecontrolstatus-swift.enum/init(rawvalue:))
- [func playImmediately(atRate: Float)](/documentation/avfoundation/avplayer/playimmediately(atrate:))

#### Responding when playback ends

- [var actionAtItemEnd: AVPlayer.ActionAtItemEnd](/documentation/avfoundation/avplayer/actionatitemend-swift.property)
- [AVPlayer.ActionAtItemEnd](/documentation/avfoundation/avplayer/actionatitemend-swift.enum)

##### Actions

- [case advance](/documentation/avfoundation/avplayer/actionatitemend-swift.enum/advance)
- [case pause](/documentation/avfoundation/avplayer/actionatitemend-swift.enum/pause)
- [case none](/documentation/avfoundation/avplayer/actionatitemend-swift.enum/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayer/actionatitemend-swift.enum/init(rawvalue:))

#### Configuring media selection criteria

- [var appliesMediaSelectionCriteriaAutomatically: Bool](/documentation/avfoundation/avplayer/appliesmediaselectioncriteriaautomatically)
- [func mediaSelectionCriteria(forMediaCharacteristic: AVMediaCharacteristic) -> AVPlayerMediaSelectionCriteria?](/documentation/avfoundation/avplayer/mediaselectioncriteria(formediacharacteristic:))
- [func setMediaSelectionCriteria(AVPlayerMediaSelectionCriteria?, forMediaCharacteristic: AVMediaCharacteristic)](/documentation/avfoundation/avplayer/setmediaselectioncriteria(_:formediacharacteristic:))

#### Accessing player output

- [var videoOutput: AVPlayerVideoOutput?](/documentation/avfoundation/avplayer/videooutput)

#### Configuring audio behavior

- [var volume: Float](/documentation/avfoundation/avplayer/volume)
- [var isMuted: Bool](/documentation/avfoundation/avplayer/ismuted)
- [var allowedAudioSpatializationFormats: AVAudioSpatializationFormats](/documentation/avfoundation/avplayeritem/allowedaudiospatializationformats)
- [var isAudioSpatializationAllowed: Bool](/documentation/avfoundation/avplayeritem/isaudiospatializationallowed)
- [var audioOutputSuppressedDueToNonMixableAudioRoute: Bool](/documentation/avfoundation/avplayer/audiooutputsuppressedduetononmixableaudioroute)
- [var intendedSpatialAudioExperience: any SpatialAudioExperience](/documentation/avfoundation/avplayer/intendedspatialaudioexperience-1bd87)

#### Configuring background playback

- [var audiovisualBackgroundPlaybackPolicy: AVPlayerAudiovisualBackgroundPlaybackPolicy](/documentation/avfoundation/avplayer/audiovisualbackgroundplaybackpolicy)
- [AVPlayerAudiovisualBackgroundPlaybackPolicy](/documentation/avfoundation/avplayeraudiovisualbackgroundplaybackpolicy)

##### Policies

- [case automatic](/documentation/avfoundation/avplayeraudiovisualbackgroundplaybackpolicy/automatic)
- [case continuesIfPossible](/documentation/avfoundation/avplayeraudiovisualbackgroundplaybackpolicy/continuesifpossible)
- [case pauses](/documentation/avfoundation/avplayeraudiovisualbackgroundplaybackpolicy/pauses)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayeraudiovisualbackgroundplaybackpolicy/init(rawvalue:))

#### Managing external playback

- [var allowsExternalPlayback: Bool](/documentation/avfoundation/avplayer/allowsexternalplayback)
- [var isExternalPlaybackActive: Bool](/documentation/avfoundation/avplayer/isexternalplaybackactive)
- [var usesExternalPlaybackWhileExternalScreenIsActive: Bool](/documentation/avfoundation/avplayer/usesexternalplaybackwhileexternalscreenisactive)
- [var externalPlaybackVideoGravity: AVLayerVideoGravity](/documentation/avfoundation/avplayer/externalplaybackvideogravity)

#### Determining HDR playback eligibility

- [class var eligibleForHDRPlayback: Bool](/documentation/avfoundation/avplayer/eligibleforhdrplayback)
- [class var availableHDRModes: AVPlayer.HDRMode](/documentation/avfoundation/avplayer/availablehdrmodes)
- [AVPlayer.HDRMode](/documentation/avfoundation/avplayer/hdrmode)

##### HDR modes

- [static var hlg: AVPlayer.HDRMode](/documentation/avfoundation/avplayer/hdrmode/hlg)
- [static var hdr10: AVPlayer.HDRMode](/documentation/avfoundation/avplayer/hdrmode/hdr10)
- [static var dolbyVision: AVPlayer.HDRMode](/documentation/avfoundation/avplayer/hdrmode/dolbyvision)

##### Initializers

- [init(rawValue: Int)](/documentation/avfoundation/avplayer/hdrmode/init(rawvalue:))
- [class let eligibleForHDRPlaybackDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayer/eligibleforhdrplaybackdidchangenotification)

#### Coordinating playback

- [var playbackCoordinator: AVPlayerPlaybackCoordinator](/documentation/avfoundation/avplayer/playbackcoordinator)

#### Synchronizing multiple players

- [func setRate(Float, time: CMTime, atHostTime: CMTime)](/documentation/avfoundation/avplayer/setrate(_:time:athosttime:))
- [func preroll(atRate: Float, completionHandler: ((Bool) -> Void)?)](/documentation/avfoundation/avplayer/preroll(atrate:completionhandler:))
- [func cancelPendingPrerolls()](/documentation/avfoundation/avplayer/cancelpendingprerolls())
- [var sourceClock: CMClock?](/documentation/avfoundation/avplayer/sourceclock)
- [var masterClock: CMClock?](/documentation/avfoundation/avplayer/masterclock)

#### Preventing sleep and backgrounding

- [var preventsDisplaySleepDuringVideoPlayback: Bool](/documentation/avfoundation/avplayer/preventsdisplaysleepduringvideoplayback)
- [var preventsAutomaticBackgroundingDuringVideoPlayback: Bool](/documentation/avfoundation/avplayer/preventsautomaticbackgroundingduringvideoplayback)

#### Determining content protections

- [var isOutputObscuredDueToInsufficientExternalProtection: Bool](/documentation/avfoundation/avplayer/isoutputobscuredduetoinsufficientexternalprotection)

#### Configuring audio and video devices

- [var audioOutputDeviceUniqueID: String?](/documentation/avfoundation/avplayer/audiooutputdeviceuniqueid)
- [var preferredVideoDecoderGPURegistryID: UInt64](/documentation/avfoundation/avplayer/preferredvideodecodergpuregistryid)

#### Configuring the network resource priority

- [var networkResourcePriority: AVPlayer.NetworkResourcePriority](/documentation/avfoundation/avplayer/networkresourcepriority-swift.property)
- [AVPlayer.NetworkResourcePriority](/documentation/avfoundation/avplayer/networkresourcepriority-swift.enum)

##### Priorities

- [case `default`](/documentation/avfoundation/avplayer/networkresourcepriority-swift.enum/default)
- [case high](/documentation/avfoundation/avplayer/networkresourcepriority-swift.enum/high)
- [case low](/documentation/avfoundation/avplayer/networkresourcepriority-swift.enum/low)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayer/networkresourcepriority-swift.enum/init(rawvalue:))

#### Configuring observation

- [class var isObservationEnabled: Bool](/documentation/avfoundation/avplayer/isobservationenabled)

#### Configuring AirPlay behavior

- [var allowsAirPlayVideo: Bool](/documentation/avfoundation/avplayer/allowsairplayvideo)
- [var isAirPlayVideoActive: Bool](/documentation/avfoundation/avplayer/isairplayvideoactive)
- [var usesAirPlayVideoWhileAirPlayScreenIsActive: Bool](/documentation/avfoundation/avplayer/usesairplayvideowhileairplayscreenisactive)

#### Displaying closed captions

- [var isClosedCaptionDisplayEnabled: Bool](/documentation/avfoundation/avplayer/isclosedcaptiondisplayenabled)
- [AVPlayerItem](/documentation/avfoundation/avplayeritem)

#### Creating a player item

- [convenience init(url: URL)](/documentation/avfoundation/avplayeritem/init(url:))
- [convenience init(asset: AVAsset)](/documentation/avfoundation/avplayeritem/init(asset:)-87rjl)
- [convenience init(asset: any AVAsset & Sendable)](/documentation/avfoundation/avplayeritem/init(asset:)-1nme9)
- [convenience init(asset: AVAsset, automaticallyLoadedAssetKeys: [AVPartialAsyncProperty<AVAsset>])](/documentation/avfoundation/avplayeritem/init(asset:automaticallyloadedassetkeys:)-5czjh)
- [convenience init(asset: any AVAsset & Sendable, automaticallyLoadedAssetKeys: [AVPartialAsyncProperty<AVAsset>])](/documentation/avfoundation/avplayeritem/init(asset:automaticallyloadedassetkeys:)-85hal)
- [init(asset: AVAsset, automaticallyLoadedAssetKeys: [String]?)](/documentation/avfoundation/avplayeritem/init(asset:automaticallyloadedassetkeys:)-8x4)

#### Accessing tracks

- [var tracks: [AVPlayerItemTrack]](/documentation/avfoundation/avplayeritem/tracks)

#### Accessing metadata

- [var externalMetadata: [AVMetadataItem]](/documentation/avfoundation/avplayeritem/externalmetadata)

#### Determining readiness

- [var status: AVPlayerItem.Status](/documentation/avfoundation/avplayeritem/status-swift.property)
- [AVPlayerItem.Status](/documentation/avfoundation/avplayeritem/status-swift.enum)

##### Player item statuses

- [case unknown](/documentation/avfoundation/avplayeritem/status-swift.enum/unknown)
- [case readyToPlay](/documentation/avfoundation/avplayeritem/status-swift.enum/readytoplay)
- [case failed](/documentation/avfoundation/avplayeritem/status-swift.enum/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayeritem/status-swift.enum/init(rawvalue:))
- [var error: (any Error)?](/documentation/avfoundation/avplayeritem/error)

#### Determining playback capabilities

- [var canPlayReverse: Bool](/documentation/avfoundation/avplayeritem/canplayreverse)
- [var canPlayFastForward: Bool](/documentation/avfoundation/avplayeritem/canplayfastforward)
- [var canPlayFastReverse: Bool](/documentation/avfoundation/avplayeritem/canplayfastreverse)
- [var canPlaySlowForward: Bool](/documentation/avfoundation/avplayeritem/canplayslowforward)
- [var canPlaySlowReverse: Bool](/documentation/avfoundation/avplayeritem/canplayslowreverse)

#### Setting playback boundaries

- [var forwardPlaybackEndTime: CMTime](/documentation/avfoundation/avplayeritem/forwardplaybackendtime)
- [var reversePlaybackEndTime: CMTime](/documentation/avfoundation/avplayeritem/reverseplaybackendtime)

#### Stepping through media

- [var canStepForward: Bool](/documentation/avfoundation/avplayeritem/canstepforward)
- [var canStepBackward: Bool](/documentation/avfoundation/avplayeritem/canstepbackward)
- [func step(byCount: Int)](/documentation/avfoundation/avplayeritem/step(bycount:))

#### Seeking through media

- [func seek(to: CMTime, completionHandler: ((Bool) -> Void)?)](/documentation/avfoundation/avplayeritem/seek(to:completionhandler:)-91gnw)
- [func seek(to: CMTime, toleranceBefore: CMTime, toleranceAfter: CMTime, completionHandler: ((Bool) -> Void)?)](/documentation/avfoundation/avplayeritem/seek(to:tolerancebefore:toleranceafter:completionhandler:))
- [func seek(to: Date, completionHandler: ((Bool) -> Void)?) -> Bool](/documentation/avfoundation/avplayeritem/seek(to:completionhandler:)-1dibq)
- [func cancelPendingSeeks()](/documentation/avfoundation/avplayeritem/cancelpendingseeks())

#### Selecting media options

- [func select(AVMediaPresentationSetting, for: AVMediaSelectionGroup)](/documentation/avfoundation/avplayeritem/select(_:for:))
- [var preferredCustomMediaSelectionSchemes: [AVCustomMediaSelectionScheme]](/documentation/avfoundation/avplayeritem/preferredcustommediaselectionschemes)
- [func effectiveMediaPresentationSettings(for: AVMediaSelectionGroup) -> [AVMediaPresentationSelector : Any]](/documentation/avfoundation/avplayeritem/effectivemediapresentationsettings(for:))
- [func selectMediaPresentationLanguage(String, for: AVMediaSelectionGroup)](/documentation/avfoundation/avplayeritem/selectmediapresentationlanguage(_:for:))
- [func selectedMediaPresentationLanguage(for: AVMediaSelectionGroup) -> String?](/documentation/avfoundation/avplayeritem/selectedmediapresentationlanguage(for:))
- [func selectedMediaPresentationSettings(for: AVMediaSelectionGroup) -> [AVMediaPresentationSelector : Any]](/documentation/avfoundation/avplayeritem/selectedmediapresentationsettings(for:))
- [var currentMediaSelection: AVMediaSelection](/documentation/avfoundation/avplayeritem/currentmediaselection)
- [func select(AVMediaSelectionOption?, in: AVMediaSelectionGroup)](/documentation/avfoundation/avplayeritem/select(_:in:))
- [func selectMediaOptionAutomatically(in: AVMediaSelectionGroup)](/documentation/avfoundation/avplayeritem/selectmediaoptionautomatically(in:))

#### Setting variant behavior

- [var variantPreferences: AVVariantPreferences](/documentation/avfoundation/avplayeritem/variantpreferences)
- [AVVariantPreferences](/documentation/avfoundation/avvariantpreferences)

##### Preference settings

- [static var scalabilityToLosslessAudio: AVVariantPreferences](/documentation/avfoundation/avvariantpreferences/scalabilitytolosslessaudio)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avvariantpreferences/init(rawvalue:))
- [var startsOnFirstEligibleVariant: Bool](/documentation/avfoundation/avplayeritem/startsonfirsteligiblevariant)

#### Configuring interstitial events

- [var integratedTimeline: AVPlayerItemIntegratedTimeline](/documentation/avfoundation/avplayeritem/integratedtimeline)
- [var automaticallyHandlesInterstitialEvents: Bool](/documentation/avfoundation/avplayeritem/automaticallyhandlesinterstitialevents)
- [var translatesPlayerInterstitialEvents: Bool](/documentation/avfoundation/avplayeritem/translatesplayerinterstitialevents)
- [var interstitialTimeRanges: [AVInterstitialTimeRange]](/documentation/avfoundation/avplayeritem/interstitialtimeranges)
- [var template: AVPlayerItem?](/documentation/avfoundation/avplayeritem/template)

#### Accessing timing information

- [func currentTime() -> CMTime](/documentation/avfoundation/avplayeritem/currenttime())
- [func currentDate() -> Date?](/documentation/avfoundation/avplayeritem/currentdate())
- [var duration: CMTime](/documentation/avfoundation/avplayeritem/duration)
- [var timebase: CMTimebase?](/documentation/avfoundation/avplayeritem/timebase)

#### Determining available time ranges

- [var loadedTimeRanges: [NSValue]](/documentation/avfoundation/avplayeritem/loadedtimeranges)
- [var seekableTimeRanges: [NSValue]](/documentation/avfoundation/avplayeritem/seekabletimeranges)

#### Determining buffering status

- [var isPlaybackLikelyToKeepUp: Bool](/documentation/avfoundation/avplayeritem/isplaybacklikelytokeepup)
- [var isPlaybackBufferFull: Bool](/documentation/avfoundation/avplayeritem/isplaybackbufferfull)
- [var isPlaybackBufferEmpty: Bool](/documentation/avfoundation/avplayeritem/isplaybackbufferempty)

#### Configuring expensive network behavior

- [var preferredPeakBitRateForExpensiveNetworks: Double](/documentation/avfoundation/avplayeritem/preferredpeakbitrateforexpensivenetworks)
- [var preferredMaximumResolutionForExpensiveNetworks: CGSize](/documentation/avfoundation/avplayeritem/preferredmaximumresolutionforexpensivenetworks)

#### Accessing text style rules

- [var textStyleRules: [AVTextStyleRule]?](/documentation/avfoundation/avplayeritem/textstylerules)
- [AVTextStyleRule](/documentation/avfoundation/avtextstylerule)

##### Creating and initializing style rules

- [class func textStyleRules(fromPropertyList: Any) -> [AVTextStyleRule]?](/documentation/avfoundation/avtextstylerule/textstylerules(frompropertylist:))
- [convenience init?(textMarkupAttributes: [String : Any])](/documentation/avfoundation/avtextstylerule/init(textmarkupattributes:))
- [init?(textMarkupAttributes: [String : Any], textSelector: String?)](/documentation/avfoundation/avtextstylerule/init(textmarkupattributes:textselector:))

##### Accessing the style attributes

- [var textMarkupAttributes: [String : Any]](/documentation/avfoundation/avtextstylerule/textmarkupattributes)
- [var textSelector: String?](/documentation/avfoundation/avtextstylerule/textselector)

##### Exporting the style rules

- [class func propertyList(for: [AVTextStyleRule]) -> Any](/documentation/avfoundation/avtextstylerule/propertylist(for:))

#### Accessing logging information

- [func accessLog() -> AVPlayerItemAccessLog?](/documentation/avfoundation/avplayeritem/accesslog())
- [AVPlayerItemAccessLog](/documentation/avfoundation/avplayeritemaccesslog)

##### Accessing log data

- [var events: [AVPlayerItemAccessLogEvent]](/documentation/avfoundation/avplayeritemaccesslog/events)
- [func extendedLogData() -> Data?](/documentation/avfoundation/avplayeritemaccesslog/extendedlogdata())
- [var extendedLogDataStringEncoding: UInt](/documentation/avfoundation/avplayeritemaccesslog/extendedlogdatastringencoding)
- [AVPlayerItemAccessLogEvent](/documentation/avfoundation/avplayeritemaccesslogevent)

##### Getting server-related log events

- [var uri: String?](/documentation/avfoundation/avplayeritemaccesslogevent/uri)
- [var serverAddress: String?](/documentation/avfoundation/avplayeritemaccesslogevent/serveraddress)
- [var numberOfServerAddressChanges: Int](/documentation/avfoundation/avplayeritemaccesslogevent/numberofserveraddresschanges)
- [var mediaRequestsWWAN: Int](/documentation/avfoundation/avplayeritemaccesslogevent/mediarequestswwan)
- [var transferDuration: TimeInterval](/documentation/avfoundation/avplayeritemaccesslogevent/transferduration)
- [var numberOfBytesTransferred: Int64](/documentation/avfoundation/avplayeritemaccesslogevent/numberofbytestransferred)
- [var numberOfMediaRequests: Int](/documentation/avfoundation/avplayeritemaccesslogevent/numberofmediarequests)

##### Getting playback-related log events

- [var playbackStartDate: Date?](/documentation/avfoundation/avplayeritemaccesslogevent/playbackstartdate)
- [var playbackSessionID: String?](/documentation/avfoundation/avplayeritemaccesslogevent/playbacksessionid)
- [var playbackStartOffset: TimeInterval](/documentation/avfoundation/avplayeritemaccesslogevent/playbackstartoffset)
- [var playbackType: String?](/documentation/avfoundation/avplayeritemaccesslogevent/playbacktype)
- [var startupTime: TimeInterval](/documentation/avfoundation/avplayeritemaccesslogevent/startuptime)
- [var durationWatched: TimeInterval](/documentation/avfoundation/avplayeritemaccesslogevent/durationwatched)
- [var numberOfDroppedVideoFrames: Int](/documentation/avfoundation/avplayeritemaccesslogevent/numberofdroppedvideoframes)
- [var numberOfStalls: Int](/documentation/avfoundation/avplayeritemaccesslogevent/numberofstalls)
- [var numberOfSegmentsDownloaded: Int](/documentation/avfoundation/avplayeritemaccesslogevent/numberofsegmentsdownloaded)
- [var segmentsDownloadedDuration: TimeInterval](/documentation/avfoundation/avplayeritemaccesslogevent/segmentsdownloadedduration)
- [var downloadOverdue: Int](/documentation/avfoundation/avplayeritemaccesslogevent/downloadoverdue)

##### Getting bit rate log events

- [var observedBitrateStandardDeviation: Double](/documentation/avfoundation/avplayeritemaccesslogevent/observedbitratestandarddeviation)
- [var observedMaxBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/observedmaxbitrate)
- [var observedMinBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/observedminbitrate)
- [var switchBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/switchbitrate)
- [var indicatedBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/indicatedbitrate)
- [var observedBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/observedbitrate)
- [var averageAudioBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/averageaudiobitrate)
- [var averageVideoBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/averagevideobitrate)
- [var indicatedAverageBitrate: Double](/documentation/avfoundation/avplayeritemaccesslogevent/indicatedaveragebitrate)
- [func errorLog() -> AVPlayerItemErrorLog?](/documentation/avfoundation/avplayeritem/errorlog())
- [AVPlayerItemErrorLog](/documentation/avfoundation/avplayeritemerrorlog)

##### Accessing error data

- [var events: [AVPlayerItemErrorLogEvent]](/documentation/avfoundation/avplayeritemerrorlog/events)
- [func extendedLogData() -> Data?](/documentation/avfoundation/avplayeritemerrorlog/extendedlogdata())
- [var extendedLogDataStringEncoding: UInt](/documentation/avfoundation/avplayeritemerrorlog/extendedlogdatastringencoding)
- [AVPlayerItemErrorLogEvent](/documentation/avfoundation/avplayeritemerrorlogevent)

##### Getting information about the event

- [var date: Date?](/documentation/avfoundation/avplayeritemerrorlogevent/date)
- [var uri: String?](/documentation/avfoundation/avplayeritemerrorlogevent/uri)
- [var serverAddress: String?](/documentation/avfoundation/avplayeritemerrorlogevent/serveraddress)
- [var playbackSessionID: String?](/documentation/avfoundation/avplayeritemerrorlogevent/playbacksessionid)
- [var errorStatusCode: Int](/documentation/avfoundation/avplayeritemerrorlogevent/errorstatuscode)
- [var errorDomain: String](/documentation/avfoundation/avplayeritemerrorlogevent/errordomain)
- [var errorComment: String?](/documentation/avfoundation/avplayeritemerrorlogevent/errorcomment)
- [var allHTTPResponseHeaderFields: [String : String]?](/documentation/avfoundation/avplayeritemerrorlogevent/allhttpresponseheaderfields)

#### Observing notifications

- [class let didPlayToEndTimeNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/didplaytoendtimenotification)
- [class let failedToPlayToEndTimeNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/failedtoplaytoendtimenotification)

##### Error keys

- [let AVPlayerItemFailedToPlayToEndTimeErrorKey: String](/documentation/avfoundation/avplayeritemfailedtoplaytoendtimeerrorkey)
- [class let timeJumpedNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/timejumpednotification)

##### User information keys

- [class let timeJumpedOriginatingParticipantKey: String](/documentation/avfoundation/avplayeritem/timejumpedoriginatingparticipantkey)
- [class let playbackStalledNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/playbackstallednotification)
- [class let mediaSelectionDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/mediaselectiondidchangenotification)
- [class let recommendedTimeOffsetFromLiveDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/recommendedtimeoffsetfromlivedidchangenotification)
- [class let newAccessLogEntryNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/newaccesslogentrynotification)
- [class let newErrorLogEntryNotification: NSNotification.Name](/documentation/avfoundation/avplayeritem/newerrorlogentrynotification)

#### Managing time offsets

- [var automaticallyPreservesTimeOffsetFromLive: Bool](/documentation/avfoundation/avplayeritem/automaticallypreservestimeoffsetfromlive)
- [var recommendedTimeOffsetFromLive: CMTime](/documentation/avfoundation/avplayeritem/recommendedtimeoffsetfromlive)
- [var configuredTimeOffsetFromLive: CMTime](/documentation/avfoundation/avplayeritem/configuredtimeoffsetfromlive)

#### Configuring presentation

- [var presentationSize: CGSize](/documentation/avfoundation/avplayeritem/presentationsize)
- [var preferredMaximumResolution: CGSize](/documentation/avfoundation/avplayeritem/preferredmaximumresolution)
- [var videoApertureMode: AVVideoApertureMode](/documentation/avfoundation/avplayeritem/videoaperturemode)
- [AVVideoApertureMode](/documentation/avfoundation/avvideoaperturemode)

##### Aperture modes

- [static let cleanAperture: AVVideoApertureMode](/documentation/avfoundation/avvideoaperturemode/cleanaperture)
- [static let encodedPixels: AVVideoApertureMode](/documentation/avfoundation/avvideoaperturemode/encodedpixels)
- [static let productionAperture: AVVideoApertureMode](/documentation/avfoundation/avvideoaperturemode/productionaperture)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideoaperturemode/init(rawvalue:))

#### Accessing Now Playing information

- [var nowPlayingInfo: [String : Any]?](/documentation/avfoundation/avplayeritem/nowplayinginfo)

#### Configuring HDR settings

- [var appliesPerFrameHDRDisplayMetadata: Bool](/documentation/avfoundation/avplayeritem/appliesperframehdrdisplaymetadata)

#### Configuring video compositing

- [var videoComposition: AVVideoComposition?](/documentation/avfoundation/avplayeritem/videocomposition)
- [var customVideoCompositor: (any AVVideoCompositing)?](/documentation/avfoundation/avplayeritem/customvideocompositor)
- [var seekingWaitsForVideoCompositionRendering: Bool](/documentation/avfoundation/avplayeritem/seekingwaitsforvideocompositionrendering)

#### Configuring audio

- [var audioMix: AVAudioMix?](/documentation/avfoundation/avplayeritem/audiomix)
- [var audioTimePitchAlgorithm: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avplayeritem/audiotimepitchalgorithm)
- [var allowedAudioSpatializationFormats: AVAudioSpatializationFormats](/documentation/avfoundation/avplayeritem/allowedaudiospatializationformats)
- [AVAudioSpatializationFormats](/documentation/avfoundation/avaudiospatializationformats)

##### Spatialization formats

- [static var monoAndStereo: AVAudioSpatializationFormats](/documentation/avfoundation/avaudiospatializationformats/monoandstereo)
- [static var multichannel: AVAudioSpatializationFormats](/documentation/avfoundation/avaudiospatializationformats/multichannel)
- [static var monoStereoAndMultichannel: AVAudioSpatializationFormats](/documentation/avfoundation/avaudiospatializationformats/monostereoandmultichannel)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avaudiospatializationformats/init(rawvalue:))
- [var isAudioSpatializationAllowed: Bool](/documentation/avfoundation/avplayeritem/isaudiospatializationallowed)

#### Managing player item outputs

- [var outputs: [AVPlayerItemOutput]](/documentation/avfoundation/avplayeritem/outputs)
- [func add(AVPlayerItemOutput)](/documentation/avfoundation/avplayeritem/add(_:)-16ctk)
- [func remove(AVPlayerItemOutput)](/documentation/avfoundation/avplayeritem/remove(_:)-46b1r)

#### Managing player item data collectors

- [var mediaDataCollectors: [AVPlayerItemMediaDataCollector]](/documentation/avfoundation/avplayeritem/mediadatacollectors)
- [func add(AVPlayerItemMediaDataCollector)](/documentation/avfoundation/avplayeritem/add(_:)-9l3to)
- [func remove(AVPlayerItemMediaDataCollector)](/documentation/avfoundation/avplayeritem/remove(_:)-29iuz)

#### Configuring network behavior

- [var preferredPeakBitRate: Double](/documentation/avfoundation/avplayeritem/preferredpeakbitrate)
- [var preferredForwardBufferDuration: TimeInterval](/documentation/avfoundation/avplayeritem/preferredforwardbufferduration)
- [var canUseNetworkResourcesForLiveStreamingWhilePaused: Bool](/documentation/avfoundation/avplayeritem/canusenetworkresourcesforlivestreamingwhilepaused)

#### Configuring player items for AVKit

- [var navigationMarkerGroups: [AVNavigationMarkersGroup]](/documentation/avfoundation/avplayeritem/navigationmarkergroups)
- [var nextContentProposal: AVContentProposal?](/documentation/avfoundation/avplayeritem/nextcontentproposal)

#### Requesting playback authorization in tvOS

- [func requestPlaybackRestrictionsAuthorization((Bool, (any Error)?) -> Void)](/documentation/avfoundation/avplayeritem/requestplaybackrestrictionsauthorization(_:))
- [func cancelPlaybackRestrictionsAuthorizationRequest()](/documentation/avfoundation/avplayeritem/cancelplaybackrestrictionsauthorizationrequest())

#### Managing playback authorization in macOS

- [var isContentAuthorizedForPlayback: Bool](/documentation/avfoundation/avplayeritem/iscontentauthorizedforplayback)
- [var isAuthorizationRequiredForPlayback: Bool](/documentation/avfoundation/avplayeritem/isauthorizationrequiredforplayback)
- [var isApplicationAuthorizedForPlayback: Bool](/documentation/avfoundation/avplayeritem/isapplicationauthorizedforplayback)
- [func requestContentAuthorizationAsynchronously(withTimeoutInterval: TimeInterval, completionHandler: () -> Void)](/documentation/avfoundation/avplayeritem/requestcontentauthorizationasynchronously(withtimeoutinterval:completionhandler:))
- [var contentAuthorizationRequestStatus: AVContentAuthorizationStatus](/documentation/avfoundation/avplayeritem/contentauthorizationrequeststatus)
- [AVContentAuthorizationStatus](/documentation/avfoundation/avcontentauthorizationstatus)

##### Content authorization statuses

- [case unknown](/documentation/avfoundation/avcontentauthorizationstatus/unknown)
- [case completed](/documentation/avfoundation/avcontentauthorizationstatus/completed)
- [case cancelled](/documentation/avfoundation/avcontentauthorizationstatus/cancelled)
- [case timedOut](/documentation/avfoundation/avcontentauthorizationstatus/timedout)
- [case busy](/documentation/avfoundation/avcontentauthorizationstatus/busy)
- [case notAvailable](/documentation/avfoundation/avcontentauthorizationstatus/notavailable)
- [case notPossible](/documentation/avfoundation/avcontentauthorizationstatus/notpossible)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcontentauthorizationstatus/init(rawvalue:))
- [func cancelContentAuthorizationRequest()](/documentation/avfoundation/avplayeritem/cancelcontentauthorizationrequest())

#### Accessing initialization parameters

- [var asset: AVAsset](/documentation/avfoundation/avplayeritem/asset)
- [var automaticallyLoadedAssetKeys: [String]](/documentation/avfoundation/avplayeritem/automaticallyloadedassetkeys)

#### Copying an player item

- [func copy() -> Any](/documentation/avfoundation/avplayeritem/copy())
- [func copy(with: NSZone?) -> Any](/documentation/avfoundation/avplayeritem/copy(with:))

#### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avplayeritem-deprecated-symbols)

##### Accessing metadata

- [var timedMetadata: [AVMetadataItem]?](/documentation/avfoundation/avplayeritem/timedmetadata)

##### Seeking through media

- [func seek(to: CMTime)](/documentation/avfoundation/avplayeritem/seek(to:)-1dpto)
- [func seek(to: CMTime, toleranceBefore: CMTime, toleranceAfter: CMTime)](/documentation/avfoundation/avplayeritem/seek(to:tolerancebefore:toleranceafter:))
- [func seek(to: Date) async -> Bool](/documentation/avfoundation/avplayeritem/seek(to:)-5rt4x)
- [func seek(to: Date) -> Bool](/documentation/avfoundation/avplayeritem/seek(to:)-3s9d8)

##### Selecting media options

- [func selectedMediaOption(in: AVMediaSelectionGroup) -> AVMediaSelectionOption?](/documentation/avfoundation/avplayeritem/selectedmediaoption(in:))
- [AVPlayerItemTrack](/documentation/avfoundation/avplayeritemtrack)

#### Setting the enabled state

- [var isEnabled: Bool](/documentation/avfoundation/avplayeritemtrack/isenabled)

#### Configuring video properties

- [var currentVideoFrameRate: Float](/documentation/avfoundation/avplayeritemtrack/currentvideoframerate)
- [var videoFieldMode: String?](/documentation/avfoundation/avplayeritemtrack/videofieldmode)
- [let AVPlayerItemTrackVideoFieldModeDeinterlaceFields: String](/documentation/avfoundation/avplayeritemtrackvideofieldmodedeinterlacefields)

#### Accessing the asset track

- [var assetTrack: AVAssetTrack?](/documentation/avfoundation/avplayeritemtrack/assettrack)
- [AVQueuePlayer](/documentation/avfoundation/avqueueplayer)

#### Creating a queue player

- [init(items: [AVPlayerItem])](/documentation/avfoundation/avqueueplayer/init(items:))

#### Managing the player queue

- [func items() -> [AVPlayerItem]](/documentation/avfoundation/avqueueplayer/items())
- [func advanceToNextItem()](/documentation/avfoundation/avqueueplayer/advancetonextitem())
- [func canInsert(AVPlayerItem, after: AVPlayerItem?) -> Bool](/documentation/avfoundation/avqueueplayer/caninsert(_:after:))
- [func insert(AVPlayerItem, after: AVPlayerItem?)](/documentation/avfoundation/avqueueplayer/insert(_:after:))
- [func remove(AVPlayerItem)](/documentation/avfoundation/avqueueplayer/remove(_:))
- [func removeAllItems()](/documentation/avfoundation/avqueueplayer/removeallitems())
- [AVPlayerLooper](/documentation/avfoundation/avplayerlooper)

#### Creating a player looper

- [init(player: AVQueuePlayer, templateItem: AVPlayerItem, timeRange: CMTimeRange, existingItemsOrdering: AVPlayerLooper.ItemOrdering)](/documentation/avfoundation/avplayerlooper/init(player:templateitem:timerange:existingitemsordering:))

##### Item ordering

- [AVPlayerLooper.ItemOrdering](/documentation/avfoundation/avplayerlooper/itemordering)

###### Ordering

- [case loopingItemsPrecedeExistingItems](/documentation/avfoundation/avplayerlooper/itemordering/loopingitemsprecedeexistingitems)
- [case loopingItemsFollowExistingItems](/documentation/avfoundation/avplayerlooper/itemordering/loopingitemsfollowexistingitems)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayerlooper/itemordering/init(rawvalue:))
- [convenience init(player: AVQueuePlayer, templateItem: AVPlayerItem)](/documentation/avfoundation/avplayerlooper/init(player:templateitem:))
- [convenience init(player: AVQueuePlayer, templateItem: AVPlayerItem, timeRange: CMTimeRange)](/documentation/avfoundation/avplayerlooper/init(player:templateitem:timerange:))

#### Configuring looping

- [var loopingPlayerItems: [AVPlayerItem]](/documentation/avfoundation/avplayerlooper/loopingplayeritems)
- [func disableLooping()](/documentation/avfoundation/avplayerlooper/disablelooping())

#### Observing looping state

- [var loopCount: Int](/documentation/avfoundation/avplayerlooper/loopcount)
- [var status: AVPlayerLooper.Status](/documentation/avfoundation/avplayerlooper/status-swift.property)
- [AVPlayerLooper.Status](/documentation/avfoundation/avplayerlooper/status-swift.enum)

##### Status values

- [case unknown](/documentation/avfoundation/avplayerlooper/status-swift.enum/unknown)
- [case ready](/documentation/avfoundation/avplayerlooper/status-swift.enum/ready)
- [case failed](/documentation/avfoundation/avplayerlooper/status-swift.enum/failed)
- [case cancelled](/documentation/avfoundation/avplayerlooper/status-swift.enum/cancelled)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayerlooper/status-swift.enum/init(rawvalue:))

#### Monitoring errors

- [var error: (any Error)?](/documentation/avfoundation/avplayerlooper/error)

### SharePlay

- [Destination Video](/documentation/visionos/destination-video)
- [Supporting coordinated media playback](/documentation/avfoundation/supporting-coordinated-media-playback)
- [AVPlaybackCoordinator](/documentation/avfoundation/avplaybackcoordinator)

#### Configuring playback policies

- [func participantLimitForWaitingOutSuspensions(withReason: AVCoordinatedPlaybackSuspension.Reason) -> Int](/documentation/avfoundation/avplaybackcoordinator/participantlimitforwaitingoutsuspensions(withreason:))
- [func setParticipantLimit(Int, forWaitingOutSuspensionsWithReason: AVCoordinatedPlaybackSuspension.Reason)](/documentation/avfoundation/avplaybackcoordinator/setparticipantlimit(_:forwaitingoutsuspensionswithreason:))
- [var suspensionReasonsThatTriggerWaiting: [AVCoordinatedPlaybackSuspension.Reason]](/documentation/avfoundation/avplaybackcoordinator/suspensionreasonsthattriggerwaiting)
- [var pauseSnapsToMediaTimeOfOriginator: Bool](/documentation/avfoundation/avplaybackcoordinator/pausesnapstomediatimeoforiginator)

#### Suspending state coordination

- [func beginSuspension(for: AVCoordinatedPlaybackSuspension.Reason) -> AVCoordinatedPlaybackSuspension](/documentation/avfoundation/avplaybackcoordinator/beginsuspension(for:))
- [AVCoordinatedPlaybackSuspension](/documentation/avfoundation/avcoordinatedplaybacksuspension)

##### Inspecting a suspension

- [var beginDate: Date](/documentation/avfoundation/avcoordinatedplaybacksuspension/begindate)
- [var reason: AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.property)
- [AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct)

###### Suspension reasons

- [static let audioSessionInterrupted: AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/audiosessioninterrupted)
- [static let coordinatedPlaybackNotPossible: AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/coordinatedplaybacknotpossible)
- [static let playingInterstitial: AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/playinginterstitial)
- [static let stallRecovery: AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/stallrecovery)
- [static let userActionRequired: AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/useractionrequired)
- [static let userIsChangingCurrentTime: AVCoordinatedPlaybackSuspension.Reason](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/userischangingcurrenttime)

###### Initializers

- [init(String)](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/init(rawvalue:))

##### Ending a suspension

- [func end()](/documentation/avfoundation/avcoordinatedplaybacksuspension/end())
- [func end(proposingNewTime: CMTime)](/documentation/avfoundation/avcoordinatedplaybacksuspension/end(proposingnewtime:))

##### Initializers

- [init(String)](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/init(_:))
- [init(rawValue: String)](/documentation/avfoundation/avcoordinatedplaybacksuspension/reason-swift.struct/init(rawvalue:))
- [func expectedItemTime(atHostTime: CMTime) -> CMTime](/documentation/avfoundation/avplaybackcoordinator/expecteditemtime(athosttime:))

#### Observing suspension reasons

- [var suspensionReasons: [AVCoordinatedPlaybackSuspension.Reason]](/documentation/avfoundation/avplaybackcoordinator/suspensionreasons)
- [class let suspensionReasonsDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplaybackcoordinator/suspensionreasonsdidchangenotification)

#### Observing other participants

- [var otherParticipants: [AVCoordinatedPlaybackParticipant]](/documentation/avfoundation/avplaybackcoordinator/otherparticipants)
- [AVCoordinatedPlaybackParticipant](/documentation/avfoundation/avcoordinatedplaybackparticipant)

##### Accessing participant status

- [var identifier: UUID](/documentation/avfoundation/avcoordinatedplaybackparticipant/identifier)
- [var isReadyToPlay: Bool](/documentation/avfoundation/avcoordinatedplaybackparticipant/isreadytoplay)
- [var suspensionReasons: [AVCoordinatedPlaybackSuspension.Reason]](/documentation/avfoundation/avcoordinatedplaybackparticipant/suspensionreasons)
- [class let otherParticipantsDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplaybackcoordinator/otherparticipantsdidchangenotification)

#### Coordinating with group sessions

- [func coordinateWithSession<T>(GroupSession<T>)](/documentation/avfoundation/avplaybackcoordinator/coordinatewithsession(_:))
- [AVPlayerPlaybackCoordinator](/documentation/avfoundation/avplayerplaybackcoordinator)

#### Accessing the player

- [var player: AVPlayer?](/documentation/avfoundation/avplayerplaybackcoordinator/player)

#### Configuring the delegate

- [var delegate: (any AVPlayerPlaybackCoordinatorDelegate)?](/documentation/avfoundation/avplayerplaybackcoordinator/delegate)
- [AVPlayerPlaybackCoordinatorDelegate](/documentation/avfoundation/avplayerplaybackcoordinatordelegate)

##### Identifying items

- [func playbackCoordinator(AVPlayerPlaybackCoordinator, identifierFor: AVPlayerItem) -> String](/documentation/avfoundation/avplayerplaybackcoordinatordelegate/playbackcoordinator(_:identifierfor:))

##### Retrieving interstitial time ranges

- [func playbackCoordinator(AVPlayerPlaybackCoordinator, interstitialTimeRangesFor: AVPlayerItem) -> [NSValue]](/documentation/avfoundation/avplayerplaybackcoordinatordelegate/playbackcoordinator(_:interstitialtimerangesfor:))

#### Managing coordination

- [func coordinate(using: AVPlaybackCoordinationMedium?) throws](/documentation/avfoundation/avplayerplaybackcoordinator/coordinate(using:))
- [var playbackCoordinationMedium: AVPlaybackCoordinationMedium?](/documentation/avfoundation/avplayerplaybackcoordinator/playbackcoordinationmedium)
- [AVDelegatingPlaybackCoordinator](/documentation/avfoundation/avdelegatingplaybackcoordinator)

#### Creating a coordinator

- [init(playbackControlDelegate: any AVPlaybackCoordinatorPlaybackControlDelegate)](/documentation/avfoundation/avdelegatingplaybackcoordinator/init(playbackcontroldelegate:))
- [AVPlaybackCoordinatorPlaybackControlDelegate](/documentation/avfoundation/avplaybackcoordinatorplaybackcontroldelegate)

##### Responding to commands

- [func playbackCoordinator(AVDelegatingPlaybackCoordinator, didIssue: AVDelegatingPlaybackCoordinatorPlayCommand, completionHandler: () -> Void)](/documentation/avfoundation/avplaybackcoordinatorplaybackcontroldelegate/playbackcoordinator(_:didissue:completionhandler:)-73p3a)
- [func playbackCoordinator(AVDelegatingPlaybackCoordinator, didIssue: AVDelegatingPlaybackCoordinatorPauseCommand, completionHandler: () -> Void)](/documentation/avfoundation/avplaybackcoordinatorplaybackcontroldelegate/playbackcoordinator(_:didissue:completionhandler:)-56t01)
- [func playbackCoordinator(AVDelegatingPlaybackCoordinator, didIssue: AVDelegatingPlaybackCoordinatorSeekCommand, completionHandler: () -> Void)](/documentation/avfoundation/avplaybackcoordinatorplaybackcontroldelegate/playbackcoordinator(_:didissue:completionhandler:)-4fk8y)
- [func playbackCoordinator(AVDelegatingPlaybackCoordinator, didIssue: AVDelegatingPlaybackCoordinatorBufferingCommand, completionHandler: () -> Void)](/documentation/avfoundation/avplaybackcoordinatorplaybackcontroldelegate/playbackcoordinator(_:didissue:completionhandler:)-btle)

#### Identifying items

- [var currentItemIdentifier: String?](/documentation/avfoundation/avdelegatingplaybackcoordinator/currentitemidentifier)

#### Accessing the delegate

- [var playbackControlDelegate: (any AVPlaybackCoordinatorPlaybackControlDelegate)?](/documentation/avfoundation/avdelegatingplaybackcoordinator/playbackcontroldelegate)

#### Coordinating state changes

- [func coordinateRateChange(to: Float, options: AVDelegatingPlaybackCoordinatorRateChangeOptions)](/documentation/avfoundation/avdelegatingplaybackcoordinator/coordinateratechange(to:options:))
- [func coordinateSeek(to: CMTime, options: AVDelegatingPlaybackCoordinatorSeekOptions)](/documentation/avfoundation/avdelegatingplaybackcoordinator/coordinateseek(to:options:))
- [func transitionToItem(withIdentifier: String?, proposingInitialTimingBasedOn: CMTimebase?)](/documentation/avfoundation/avdelegatingplaybackcoordinator/transitiontoitem(withidentifier:proposinginitialtimingbasedon:))
- [func reapplyCurrentItemStateToPlaybackControlDelegate()](/documentation/avfoundation/avdelegatingplaybackcoordinator/reapplycurrentitemstatetoplaybackcontroldelegate())
- [AVDelegatingPlaybackCoordinatorSeekOptions](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekoptions)

##### Seek options

- [static var resumeImmediately: AVDelegatingPlaybackCoordinatorSeekOptions](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekoptions/resumeimmediately)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekoptions/init(rawvalue:))
- [AVDelegatingPlaybackCoordinatorRateChangeOptions](/documentation/avfoundation/avdelegatingplaybackcoordinatorratechangeoptions)

##### Rate change options

- [static var playImmediately: AVDelegatingPlaybackCoordinatorRateChangeOptions](/documentation/avfoundation/avdelegatingplaybackcoordinatorratechangeoptions/playimmediately)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avdelegatingplaybackcoordinatorratechangeoptions/init(rawvalue:))

#### Playback commands

- [AVDelegatingPlaybackCoordinatorPlaybackControlCommand](/documentation/avfoundation/avdelegatingplaybackcoordinatorplaybackcontrolcommand)

##### Accessing command details

- [var expectedCurrentItemIdentifier: String](/documentation/avfoundation/avdelegatingplaybackcoordinatorplaybackcontrolcommand/expectedcurrentitemidentifier)
- [var originator: AVCoordinatedPlaybackParticipant?](/documentation/avfoundation/avdelegatingplaybackcoordinatorplaybackcontrolcommand/originator)
- [AVDelegatingPlaybackCoordinatorPlayCommand](/documentation/avfoundation/avdelegatingplaybackcoordinatorplaycommand)

##### Accessing command details

- [var rate: Float](/documentation/avfoundation/avdelegatingplaybackcoordinatorplaycommand/rate)
- [var itemTime: CMTime](/documentation/avfoundation/avdelegatingplaybackcoordinatorplaycommand/itemtime)
- [var hostClockTime: CMTime](/documentation/avfoundation/avdelegatingplaybackcoordinatorplaycommand/hostclocktime)
- [AVDelegatingPlaybackCoordinatorPauseCommand](/documentation/avfoundation/avdelegatingplaybackcoordinatorpausecommand)

##### Accessing command details

- [var shouldBufferInAnticipationOfPlayback: Bool](/documentation/avfoundation/avdelegatingplaybackcoordinatorpausecommand/shouldbufferinanticipationofplayback)
- [var anticipatedPlaybackRate: Float](/documentation/avfoundation/avdelegatingplaybackcoordinatorpausecommand/anticipatedplaybackrate)
- [AVDelegatingPlaybackCoordinatorSeekCommand](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekcommand)

##### Accessing command details

- [var shouldBufferInAnticipationOfPlayback: Bool](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekcommand/shouldbufferinanticipationofplayback)
- [var anticipatedPlaybackRate: Float](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekcommand/anticipatedplaybackrate)
- [var itemTime: CMTime](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekcommand/itemtime)
- [var completionDueDate: Date?](/documentation/avfoundation/avdelegatingplaybackcoordinatorseekcommand/completionduedate)
- [AVDelegatingPlaybackCoordinatorBufferingCommand](/documentation/avfoundation/avdelegatingplaybackcoordinatorbufferingcommand)

##### Accessing command details

- [var anticipatedPlaybackRate: Float](/documentation/avfoundation/avdelegatingplaybackcoordinatorbufferingcommand/anticipatedplaybackrate)
- [var completionDueDate: Date?](/documentation/avfoundation/avdelegatingplaybackcoordinatorbufferingcommand/completionduedate)
- [AVPlaybackCoordinationMedium](/documentation/avfoundation/avplaybackcoordinationmedium)

#### Creating a coordination medium

- [init()](/documentation/avfoundation/avplaybackcoordinationmedium/init())

#### Managing playback coordinators

- [var connectedPlaybackCoordinators: [AVPlayerPlaybackCoordinator]](/documentation/avfoundation/avplaybackcoordinationmedium/connectedplaybackcoordinators)

### Presentation

- [Monitoring playback progress in your app](/documentation/avfoundation/monitoring-playback-progress-in-your-app)
- [Using HEVC video with alpha](/documentation/avfoundation/using-hevc-video-with-alpha)
- [AVPlayerLayer](/documentation/avfoundation/avplayerlayer)

#### Creating a player layer

- [init(player: AVPlayer?)](/documentation/avfoundation/avplayerlayer/init(player:))

#### Configuring the presentation

- [var videoRect: CGRect](/documentation/avfoundation/avplayerlayer/videorect)
- [var videoGravity: AVLayerVideoGravity](/documentation/avfoundation/avplayerlayer/videogravity)
- [AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity)

##### Video gravities

- [static let resize: AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity/resize)
- [static let resizeAspect: AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity/resizeaspect)
- [static let resizeAspectFill: AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity/resizeaspectfill)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avlayervideogravity/init(rawvalue:))

#### Determining display readiness

- [var isReadyForDisplay: Bool](/documentation/avfoundation/avplayerlayer/isreadyfordisplay)

#### Accessing the player

- [var player: AVPlayer?](/documentation/avfoundation/avplayerlayer/player)

#### Processing pixel buffers

- [var pixelBufferAttributes: [String : Any]?](/documentation/avfoundation/avplayerlayer/pixelbufferattributes)
- [func displayedPixelBuffer() -> CVPixelBuffer?](/documentation/avfoundation/avplayerlayer/displayedpixelbuffer())
- [func displayedReadOnlyPixelBuffer() -> CVReadOnlyPixelBuffer?](/documentation/avfoundation/avplayerlayer/displayedreadonlypixelbuffer())
- [AVSynchronizedLayer](/documentation/avfoundation/avsynchronizedlayer)

#### Creating a synchronized layer

- [init(playerItem: AVPlayerItem)](/documentation/avfoundation/avsynchronizedlayer/init(playeritem:))

#### Managing the player item

- [var playerItem: AVPlayerItem?](/documentation/avfoundation/avsynchronizedlayer/playeritem)

#### Supporting types

- [let AVCoreAnimationBeginTimeAtZero: CFTimeInterval](/documentation/avfoundation/avcoreanimationbegintimeatzero)

### Media selection

- [Selecting subtitles and alternative audio tracks](/documentation/avfoundation/selecting-subtitles-and-alternative-audio-tracks)
- [AVMediaSelection](/documentation/avfoundation/avmediaselection)

#### Inspecting the media selection

- [func selectedMediaOption(in: AVMediaSelectionGroup) -> AVMediaSelectionOption?](/documentation/avfoundation/avmediaselection/selectedmediaoption(in:))
- [func mediaSelectionCriteriaCanBeAppliedAutomatically(to: AVMediaSelectionGroup) -> Bool](/documentation/avfoundation/avmediaselection/mediaselectioncriteriacanbeappliedautomatically(to:))

#### Accessing the asset

- [var asset: AVAsset?](/documentation/avfoundation/avmediaselection/asset)
- [AVMediaSelectionGroup](/documentation/avfoundation/avmediaselectiongroup)

#### Accessing media selection options

- [var options: [AVMediaSelectionOption]](/documentation/avfoundation/avmediaselectiongroup/options)
- [func mediaSelectionOption(withPropertyList: Any) -> AVMediaSelectionOption?](/documentation/avfoundation/avmediaselectiongroup/mediaselectionoption(withpropertylist:))
- [var defaultOption: AVMediaSelectionOption?](/documentation/avfoundation/avmediaselectiongroup/defaultoption)

#### Configuring empty selection behavior

- [var allowsEmptySelection: Bool](/documentation/avfoundation/avmediaselectiongroup/allowsemptyselection)

#### Filtering selection options

- [class func playableMediaSelectionOptions(from: [AVMediaSelectionOption]) -> [AVMediaSelectionOption]](/documentation/avfoundation/avmediaselectiongroup/playablemediaselectionoptions(from:))
- [class func mediaSelectionOptions(from: [AVMediaSelectionOption], with: Locale) -> [AVMediaSelectionOption]](/documentation/avfoundation/avmediaselectiongroup/mediaselectionoptions(from:with:))
- [class func mediaSelectionOptions(from: [AVMediaSelectionOption], withMediaCharacteristics: [AVMediaCharacteristic]) -> [AVMediaSelectionOption]](/documentation/avfoundation/avmediaselectiongroup/mediaselectionoptions(from:withmediacharacteristics:))
- [class func mediaSelectionOptions(from: [AVMediaSelectionOption], withoutMediaCharacteristics: [AVMediaCharacteristic]) -> [AVMediaSelectionOption]](/documentation/avfoundation/avmediaselectiongroup/mediaselectionoptions(from:withoutmediacharacteristics:))
- [class func mediaSelectionOptions(from: [AVMediaSelectionOption], filteredAndSortedAccordingToPreferredLanguages: [String]) -> [AVMediaSelectionOption]](/documentation/avfoundation/avmediaselectiongroup/mediaselectionoptions(from:filteredandsortedaccordingtopreferredlanguages:))
- [var customMediaSelectionScheme: AVCustomMediaSelectionScheme?](/documentation/avfoundation/avmediaselectiongroup/custommediaselectionscheme)

#### Creating a Now Playing language option group

- [func makeNowPlayingInfoLanguageOptionGroup() -> MPNowPlayingInfoLanguageOptionGroup](/documentation/avfoundation/avmediaselectiongroup/makenowplayinginfolanguageoptiongroup())
- [AVMediaSelectionOption](/documentation/avfoundation/avmediaselectionoption)

#### Accessing media information

- [var mediaType: AVMediaType](/documentation/avfoundation/avmediaselectionoption/mediatype)
- [var mediaSubTypes: [NSNumber]](/documentation/avfoundation/avmediaselectionoption/mediasubtypes)
- [func hasMediaCharacteristic(AVMediaCharacteristic) -> Bool](/documentation/avfoundation/avmediaselectionoption/hasmediacharacteristic(_:))

#### Managing metadata

- [var commonMetadata: [AVMetadataItem]](/documentation/avfoundation/avmediaselectionoption/commonmetadata)
- [var availableMetadataFormats: [String]](/documentation/avfoundation/avmediaselectionoption/availablemetadataformats)
- [func metadata(forFormat: String) -> [AVMetadataItem]](/documentation/avfoundation/avmediaselectionoption/metadata(forformat:))

#### Determining playability

- [var isPlayable: Bool](/documentation/avfoundation/avmediaselectionoption/isplayable)

#### Getting the language and locale settings

- [var displayName: String](/documentation/avfoundation/avmediaselectionoption/displayname)
- [func displayName(with: Locale) -> String](/documentation/avfoundation/avmediaselectionoption/displayname(with:))
- [var locale: Locale?](/documentation/avfoundation/avmediaselectionoption/locale)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avmediaselectionoption/extendedlanguagetag)

#### Getting the associated media selection option

- [func associatedMediaSelectionOption(in: AVMediaSelectionGroup) -> AVMediaSelectionOption?](/documentation/avfoundation/avmediaselectionoption/associatedmediaselectionoption(in:))

#### Creating a Now Playing language option

- [func makeNowPlayingInfoLanguageOption() -> MPNowPlayingInfoLanguageOption?](/documentation/avfoundation/avmediaselectionoption/makenowplayinginfolanguageoption())

#### Creating a property list representation

- [func propertyList() -> Any](/documentation/avfoundation/avmediaselectionoption/propertylist())
- [AVMutableMediaSelection](/documentation/avfoundation/avmutablemediaselection)

#### Selecting media options

- [func select(AVMediaSelectionOption?, in: AVMediaSelectionGroup)](/documentation/avfoundation/avmutablemediaselection/select(_:in:))
- [AVPlayerMediaSelectionCriteria](/documentation/avfoundation/avplayermediaselectioncriteria)

#### Creating media selection criteria

- [init(preferredLanguages: [String]?, preferredMediaCharacteristics: [AVMediaCharacteristic]?)](/documentation/avfoundation/avplayermediaselectioncriteria/init(preferredlanguages:preferredmediacharacteristics:))
- [init(principalMediaCharacteristics: [AVMediaCharacteristic]?, preferredLanguages: [String]?, preferredMediaCharacteristics: [AVMediaCharacteristic]?)](/documentation/avfoundation/avplayermediaselectioncriteria/init(principalmediacharacteristics:preferredlanguages:preferredmediacharacteristics:))

#### Retrieving selection criteria settings

- [var preferredLanguages: [String]?](/documentation/avfoundation/avplayermediaselectioncriteria/preferredlanguages)
- [var preferredMediaCharacteristics: [AVMediaCharacteristic]?](/documentation/avfoundation/avplayermediaselectioncriteria/preferredmediacharacteristics)
- [var principalMediaCharacteristics: [AVMediaCharacteristic]?](/documentation/avfoundation/avplayermediaselectioncriteria/principalmediacharacteristics)
- [AVCustomMediaSelectionScheme](/documentation/avfoundation/avcustommediaselectionscheme)

#### Inspecting the scheme

- [var availableLanguages: [String]](/documentation/avfoundation/avcustommediaselectionscheme/availablelanguages)
- [var selectors: [AVMediaPresentationSelector]](/documentation/avfoundation/avcustommediaselectionscheme/selectors)
- [var shouldOfferLanguageSelection: Bool](/documentation/avfoundation/avcustommediaselectionscheme/shouldofferlanguageselection)
- [func mediaPresentationSettings(for: AVMediaPresentationSelector, complementaryToLanguage: String?, settings: [AVMediaPresentationSetting]) -> [AVMediaPresentationSetting]](/documentation/avfoundation/avcustommediaselectionscheme/mediapresentationsettings(for:complementarytolanguage:settings:))
- [AVMediaPresentationSelector](/documentation/avfoundation/avmediapresentationselector)

#### Instance Properties

- [var identifier: String](/documentation/avfoundation/avmediapresentationselector/identifier)
- [var settings: [AVMediaPresentationSetting]](/documentation/avfoundation/avmediapresentationselector/settings)

#### Instance Methods

- [func displayName(forLocaleIdentifier: String) -> String](/documentation/avfoundation/avmediapresentationselector/displayname(forlocaleidentifier:))
- [AVMediaPresentationSetting](/documentation/avfoundation/avmediapresentationsetting)

#### Instance Properties

- [var mediaCharacteristic: AVMediaCharacteristic](/documentation/avfoundation/avmediapresentationsetting/mediacharacteristic)

#### Instance Methods

- [func displayName(forLocaleIdentifier: String) -> String](/documentation/avfoundation/avmediapresentationsetting/displayname(forlocaleidentifier:))

### Interstitials

- [Providing an integrated view of your timeline when playing HLS interstitials](/documentation/avfoundation/providing-an-integrated-view-of-your-timeline-when-playing-hls-interstitials)
- [AVPlayerInterstitialEvent](/documentation/avfoundation/avplayerinterstitialevent)

#### Creating an event

- [convenience init(primaryItem: AVPlayerItem, time: CMTime)](/documentation/avfoundation/avplayerinterstitialevent/init(primaryitem:time:))
- [convenience init(primaryItem: AVPlayerItem, date: Date)](/documentation/avfoundation/avplayerinterstitialevent/init(primaryitem:date:))
- [convenience init(primaryItem: AVPlayerItem, identifier: String?, time: CMTime, templateItems: [AVPlayerItem], restrictions: AVPlayerInterstitialEvent.Restrictions, resumptionOffset: CMTime, playoutLimit: CMTime, userDefinedAttributes: [String : Any])](/documentation/avfoundation/avplayerinterstitialevent/init(primaryitem:identifier:time:templateitems:restrictions:resumptionoffset:playoutlimit:userdefinedattributes:))
- [convenience init(primaryItem: AVPlayerItem, identifier: String?, date: Date, templateItems: [AVPlayerItem], restrictions: AVPlayerInterstitialEvent.Restrictions, resumptionOffset: CMTime, playoutLimit: CMTime, userDefinedAttributes: [String : Any])](/documentation/avfoundation/avplayerinterstitialevent/init(primaryitem:identifier:date:templateitems:restrictions:resumptionoffset:playoutlimit:userdefinedattributes:))

#### Identifying events

- [var identifier: String](/documentation/avfoundation/avplayerinterstitialevent/identifier)

#### Accessing player items

- [var primaryItem: AVPlayerItem?](/documentation/avfoundation/avplayerinterstitialevent/primaryitem)
- [var templateItems: [AVPlayerItem]](/documentation/avfoundation/avplayerinterstitialevent/templateitems)

#### Configuring cues

- [var cue: AVPlayerInterstitialEvent.Cue](/documentation/avfoundation/avplayerinterstitialevent/cue-swift.property)
- [AVPlayerInterstitialEvent.Cue](/documentation/avfoundation/avplayerinterstitialevent/cue-swift.struct)

##### Cues

- [static let noCue: AVPlayerInterstitialEvent.Cue](/documentation/avfoundation/avplayerinterstitialevent/cue-swift.struct/nocue)
- [static let joinCue: AVPlayerInterstitialEvent.Cue](/documentation/avfoundation/avplayerinterstitialevent/cue-swift.struct/joincue)
- [static let leaveCue: AVPlayerInterstitialEvent.Cue](/documentation/avfoundation/avplayerinterstitialevent/cue-swift.struct/leavecue)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avplayerinterstitialevent/cue-swift.struct/init(rawvalue:))

#### Inspecting timing

- [var time: CMTime](/documentation/avfoundation/avplayerinterstitialevent/time)
- [var date: Date?](/documentation/avfoundation/avplayerinterstitialevent/date)
- [var willPlayOnce: Bool](/documentation/avfoundation/avplayerinterstitialevent/willplayonce)
- [var resumptionOffset: CMTime](/documentation/avfoundation/avplayerinterstitialevent/resumptionoffset)
- [var playoutLimit: CMTime](/documentation/avfoundation/avplayerinterstitialevent/playoutlimit)
- [var alignsStartWithPrimarySegmentBoundary: Bool](/documentation/avfoundation/avplayerinterstitialevent/alignsstartwithprimarysegmentboundary)
- [var alignsResumptionWithPrimarySegmentBoundary: Bool](/documentation/avfoundation/avplayerinterstitialevent/alignsresumptionwithprimarysegmentboundary)

#### Managing restrictions

- [var restrictions: AVPlayerInterstitialEvent.Restrictions](/documentation/avfoundation/avplayerinterstitialevent/restrictions-swift.property)
- [AVPlayerInterstitialEvent.Restrictions](/documentation/avfoundation/avplayerinterstitialevent/restrictions-swift.struct)

##### Configure

- [static var constrainsSeekingForwardInPrimaryContent: AVPlayerInterstitialEvent.Restrictions](/documentation/avfoundation/avplayerinterstitialevent/restrictions-swift.struct/constrainsseekingforwardinprimarycontent)
- [static var requiresPlaybackAtPreferredRateForAdvancement: AVPlayerInterstitialEvent.Restrictions](/documentation/avfoundation/avplayerinterstitialevent/restrictions-swift.struct/requiresplaybackatpreferredrateforadvancement)

##### Initializing a restriction

- [init(rawValue: UInt)](/documentation/avfoundation/avplayerinterstitialevent/restrictions-swift.struct/init(rawvalue:))

#### Accessing asset lists

- [var assetListResponse: [AnyHashable : any Sendable]?](/documentation/avfoundation/avplayerinterstitialevent/assetlistresponse)

#### Accessing attributes

- [var userDefinedAttributes: [AnyHashable : any Sendable]](/documentation/avfoundation/avplayerinterstitialevent/userdefinedattributes)

#### Inspecting timeline occupancy

- [var timelineOccupancy: AVPlayerInterstitialEvent.TimelineOccupancy](/documentation/avfoundation/avplayerinterstitialevent/timelineoccupancy-swift.property)
- [AVPlayerInterstitialEvent.TimelineOccupancy](/documentation/avfoundation/avplayerinterstitialevent/timelineoccupancy-swift.enum)

##### Values

- [case singlePoint](/documentation/avfoundation/avplayerinterstitialevent/timelineoccupancy-swift.enum/singlepoint)
- [case fill](/documentation/avfoundation/avplayerinterstitialevent/timelineoccupancy-swift.enum/fill)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayerinterstitialevent/timelineoccupancy-swift.enum/init(rawvalue:))
- [var supplementsPrimaryContent: Bool](/documentation/avfoundation/avplayerinterstitialevent/supplementsprimarycontent)
- [var contentMayVary: Bool](/documentation/avfoundation/avplayerinterstitialevent/contentmayvary)
- [var plannedDuration: CMTime](/documentation/avfoundation/avplayerinterstitialevent/plannedduration)

#### Managing skipping behavior

- [var skipControlLocalizedLabelBundleKey: String?](/documentation/avfoundation/avplayerinterstitialevent/skipcontrollocalizedlabelbundlekey)
- [var skipControlTimeRange: CMTimeRange](/documentation/avfoundation/avplayerinterstitialevent/skipcontroltimerange)
- [AVPlayerInterstitialEvent.SkippableEventState](/documentation/avfoundation/avplayerinterstitialevent/skippableeventstate)

##### Event states

- [case eligible](/documentation/avfoundation/avplayerinterstitialevent/skippableeventstate/eligible)
- [case noLongerEligible](/documentation/avfoundation/avplayerinterstitialevent/skippableeventstate/nolongereligible)
- [case notSkippable](/documentation/avfoundation/avplayerinterstitialevent/skippableeventstate/notskippable)
- [case notYetEligible](/documentation/avfoundation/avplayerinterstitialevent/skippableeventstate/notyeteligible)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayerinterstitialevent/skippableeventstate/init(rawvalue:))
- [AVPlayerInterstitialEventController](/documentation/avfoundation/avplayerinterstitialeventcontroller)

#### Creating an event controller

- [init(primaryPlayer: AVPlayer)](/documentation/avfoundation/avplayerinterstitialeventcontroller/init(primaryplayer:))

#### Configuring the event schedule

- [var events: [AVPlayerInterstitialEvent]!](/documentation/avfoundation/avplayerinterstitialeventcontroller/events)
- [func cancelCurrentEvent(withResumptionOffset: CMTime)](/documentation/avfoundation/avplayerinterstitialeventcontroller/cancelcurrentevent(withresumptionoffset:))
- [func skipCurrentEvent()](/documentation/avfoundation/avplayerinterstitialeventcontroller/skipcurrentevent())

#### Accessing strings

- [var localizedStringsBundle: Bundle?](/documentation/avfoundation/avplayerinterstitialeventcontroller/localizedstringsbundle)
- [var localizedStringsTableName: String?](/documentation/avfoundation/avplayerinterstitialeventcontroller/localizedstringstablename)
- [AVPlayerInterstitialEventMonitor](/documentation/avfoundation/avplayerinterstitialeventmonitor)

#### Creating a monitor

- [init(primaryPlayer: AVPlayer)](/documentation/avfoundation/avplayerinterstitialeventmonitor/init(primaryplayer:))

#### Monitoring the current event

- [var currentEvent: AVPlayerInterstitialEvent?](/documentation/avfoundation/avplayerinterstitialeventmonitor/currentevent)
- [class let currentEventDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventdidchangenotification)

#### Monitoring the event schedule

- [var events: [AVPlayerInterstitialEvent]](/documentation/avfoundation/avplayerinterstitialeventmonitor/events)
- [class let eventsDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayerinterstitialeventmonitor/eventsdidchangenotification)
- [class let interstitialEventWasUnscheduledNotification: NSNotification.Name](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialeventwasunschedulednotification)
- [class let interstitialEventWasUnscheduledEventKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialeventwasunscheduledeventkey)
- [class let interstitialEventWasUnscheduledErrorKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialeventwasunschedulederrorkey)
- [class let interstitialEventDidFinishNotification: NSNotification.Name](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialeventdidfinishnotification)
- [class let interstitialEventDidFinishEventKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialeventdidfinisheventkey)
- [class let interstitialEventDidFinishPlayoutTimeKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialeventdidfinishplayouttimekey)
- [class let interstitialEventDidFinishDidPlayEntireEventKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialeventdidfinishdidplayentireeventkey)

#### Monitoring the asset list response

- [class let assetListResponseStatusDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayerinterstitialeventmonitor/assetlistresponsestatusdidchangenotification)

##### User information keys

- [class let assetListResponseStatusDidChangeEventKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/assetlistresponsestatusdidchangeeventkey)
- [class let assetListResponseStatusDidChangeStatusKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/assetlistresponsestatusdidchangestatuskey)
- [class let assetListResponseStatusDidChangeErrorKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/assetlistresponsestatusdidchangeerrorkey)
- [AVPlayerInterstitialEventAssetListResponseStatus](/documentation/avfoundation/avplayerinterstitialeventassetlistresponsestatus)

##### Status values

- [case available](/documentation/avfoundation/avplayerinterstitialeventassetlistresponsestatus/available)
- [case cleared](/documentation/avfoundation/avplayerinterstitialeventassetlistresponsestatus/cleared)
- [case unavailable](/documentation/avfoundation/avplayerinterstitialeventassetlistresponsestatus/unavailable)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayerinterstitialeventassetlistresponsestatus/init(rawvalue:))

#### Monitoring skipping

- [class let currentEventSkippableStateDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskippablestatedidchangenotification)
- [class let currentEventSkippableStateDidChangeEventKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskippablestatedidchangeeventkey)
- [class let currentEventSkippableStateDidChangeStateKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskippablestatedidchangestatekey)
- [class let currentEventSkippableStateDidChangeSkipControlLabelKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskippablestatedidchangeskipcontrollabelkey)
- [class let currentEventSkippedNotification: NSNotification.Name](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskippednotification)
- [class let currentEventSkippedEventKey: String](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskippedeventkey)
- [var currentEventSkipControlLabel: String?](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskipcontrollabel)
- [var currentEventSkippableState: AVPlayerInterstitialEvent.SkippableEventState](/documentation/avfoundation/avplayerinterstitialeventmonitor/currenteventskippablestate)

#### Accessing the players

- [var primaryPlayer: AVPlayer?](/documentation/avfoundation/avplayerinterstitialeventmonitor/primaryplayer)
- [var interstitialPlayer: AVQueuePlayer](/documentation/avfoundation/avplayerinterstitialeventmonitor/interstitialplayer)
- [AVPlayerItemIntegratedTimeline](/documentation/avfoundation/avplayeritemintegratedtimeline)

#### Inspecting snapshots

- [var currentSnapshot: AVPlayerItemIntegratedTimelineSnapshot](/documentation/avfoundation/avplayeritemintegratedtimeline/currentsnapshot)
- [AVPlayerItemIntegratedTimelineSnapshot](/documentation/avfoundation/avplayeritemintegratedtimelinesnapshot)

##### Inspecting the snapshot

- [var duration: CMTime](/documentation/avfoundation/avplayeritemintegratedtimelinesnapshot/duration)
- [var currentSegment: AVPlayerItemSegment?](/documentation/avfoundation/avplayeritemintegratedtimelinesnapshot/currentsegment)
- [var segments: [AVPlayerItemSegment]](/documentation/avfoundation/avplayeritemintegratedtimelinesnapshot/segments)
- [AVPlayerItemSegment](/documentation/avfoundation/avplayeritemsegment)

###### Identifying the type

- [var segmentType: AVPlayerItemSegment.SegmentType](/documentation/avfoundation/avplayeritemsegment/segmenttype-swift.property)
- [AVPlayerItemSegment.SegmentType](/documentation/avfoundation/avplayeritemsegment/segmenttype-swift.enum)

###### Segment types

- [case primary](/documentation/avfoundation/avplayeritemsegment/segmenttype-swift.enum/primary)
- [case interstitial](/documentation/avfoundation/avplayeritemsegment/segmenttype-swift.enum/interstitial)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avplayeritemsegment/segmenttype-swift.enum/init(rawvalue:))

###### Inspecting the segment

- [var timeMapping: CMTimeMapping](/documentation/avfoundation/avplayeritemsegment/timemapping)
- [var loadedTimeRanges: [CMTimeRange]](/documentation/avfoundation/avplayeritemsegment/loadedtimeranges-879hc)
- [var startDate: Date?](/documentation/avfoundation/avplayeritemsegment/startdate)
- [var interstitialEvent: AVPlayerInterstitialEvent?](/documentation/avfoundation/avplayeritemsegment/interstitialevent)
- [var currentTime: CMTime](/documentation/avfoundation/avplayeritemintegratedtimelinesnapshot/currenttime)
- [var currentDate: Date?](/documentation/avfoundation/avplayeritemintegratedtimelinesnapshot/currentdate)

##### Time mapping

- [func segmentAndOffsetIntoSegment(forTimelineTime: CMTime) -> (AVPlayerItemSegment, CMTime)](/documentation/avfoundation/avplayeritemintegratedtimelinesnapshot/segmentandoffsetintosegment(fortimelinetime:))
- [class let snapshotsOutOfSyncNotification: NSNotification.Name](/documentation/avfoundation/avplayeritemintegratedtimeline/snapshotsoutofsyncnotification)

##### User-information keys

- [class let snapshotsOutOfSyncReasonKey: String](/documentation/avfoundation/avplayeritemintegratedtimeline/snapshotsoutofsyncreasonkey)
- [AVPlayerIntegratedTimelineSnapshotsOutOfSyncReason](/documentation/avfoundation/avplayerintegratedtimelinesnapshotsoutofsyncreason)

###### Getting the reasons

- [static let segmentsChanged: AVPlayerIntegratedTimelineSnapshotsOutOfSyncReason](/documentation/avfoundation/avplayerintegratedtimelinesnapshotsoutofsyncreason/segmentschanged)
- [static let currentSegmentChanged: AVPlayerIntegratedTimelineSnapshotsOutOfSyncReason](/documentation/avfoundation/avplayerintegratedtimelinesnapshotsoutofsyncreason/currentsegmentchanged)
- [static let loadedTimeRangesChanged: AVPlayerIntegratedTimelineSnapshotsOutOfSyncReason](/documentation/avfoundation/avplayerintegratedtimelinesnapshotsoutofsyncreason/loadedtimerangeschanged)

###### Creating a reason

- [init(rawValue: String)](/documentation/avfoundation/avplayerintegratedtimelinesnapshotsoutofsyncreason/init(rawvalue:))

#### Inspecting the time and date

- [var currentTime: CMTime](/documentation/avfoundation/avplayeritemintegratedtimeline/currenttime)
- [var currentDate: Date?](/documentation/avfoundation/avplayeritemintegratedtimeline/currentdate)

#### Seeking

- [func seek(to: CMTime, toleranceBefore: CMTime, toleranceAfter: CMTime, completionHandler: ((Bool) -> Void)?)](/documentation/avfoundation/avplayeritemintegratedtimeline/seek(to:tolerancebefore:toleranceafter:completionhandler:))
- [func seek(to: Date, completionHandler: ((Bool) -> Void)?)](/documentation/avfoundation/avplayeritemintegratedtimeline/seek(to:completionhandler:))

#### Observing time changes

- [func periodicTimes(forInterval: CMTime) -> AVPlayerItemIntegratedTimeline.PeriodicTimes](/documentation/avfoundation/avplayeritemintegratedtimeline/periodictimes(forinterval:))
- [func boundaryTimes(for: AVPlayerItemSegment, offsetsIntoSegment: [CMTime]) -> AVPlayerItemIntegratedTimeline.BoundaryTimes](/documentation/avfoundation/avplayeritemintegratedtimeline/boundarytimes(for:offsetsintosegment:))
- [AVPlayerItemIntegratedTimeline.BoundaryTimes](/documentation/avfoundation/avplayeritemintegratedtimeline/boundarytimes)

##### Iterating elements

- [AVPlayerItemIntegratedTimeline.BoundaryTimes.Iterator](/documentation/avfoundation/avplayeritemintegratedtimeline/boundarytimes/iterator)
- [AVPlayerItemIntegratedTimeline.PeriodicTimes](/documentation/avfoundation/avplayeritemintegratedtimeline/periodictimes)

##### Iterating elements

- [AVPlayerItemIntegratedTimeline.PeriodicTimes.Iterator](/documentation/avfoundation/avplayeritemintegratedtimeline/periodictimes/iterator)
- [AVPlayerItemIntegratedTimelineObserver](/documentation/avfoundation/avplayeritemintegratedtimelineobserver)

### Metrics

- [AVMetrics](/documentation/avfoundation/avmetrics)

#### Merging metrics

- [func chronologicalMerge<OtherSecondMetric, each MetricEventPack>(with: AVMetrics<OtherSecondMetric>, repeat AVMetrics<each MetricEventPack>) -> AVMergedMetrics<MetricEvent, OtherSecondMetric, repeat each MetricEventPack>](/documentation/avfoundation/avmetrics/chronologicalmerge(with:_:))
- [AVMergedMetrics](/documentation/avfoundation/avmergedmetrics)
- [AVVideoPerformanceMetrics](/documentation/avfoundation/avvideoperformancemetrics)

#### Inspecting metrics

- [var numberOfCorruptedFrames: Int](/documentation/avfoundation/avvideoperformancemetrics/numberofcorruptedframes)
- [var numberOfDroppedFrames: Int](/documentation/avfoundation/avvideoperformancemetrics/numberofdroppedframes)
- [var numberOfFramesDisplayedUsingOptimizedCompositing: Int](/documentation/avfoundation/avvideoperformancemetrics/numberofframesdisplayedusingoptimizedcompositing)
- [var totalAccumulatedFrameDelay: TimeInterval](/documentation/avfoundation/avvideoperformancemetrics/totalaccumulatedframedelay)
- [var totalNumberOfFrames: Int](/documentation/avfoundation/avvideoperformancemetrics/totalnumberofframes)
- [AVMetricEventStreamPublisher](/documentation/avfoundation/avmetriceventstreampublisher)

#### Getting the metrics

- [func allMetrics() -> AVMetrics<AVMetricEvent>](/documentation/avfoundation/avmetriceventstreampublisher/allmetrics())
- [func metrics<MetricEvent>(forType: MetricEvent.Type) -> AVMetrics<MetricEvent>](/documentation/avfoundation/avmetriceventstreampublisher/metrics(fortype:))
- [AVMetricEvent](/documentation/avfoundation/avmetricevent)

#### Inspecting an event

- [var date: Date](/documentation/avfoundation/avmetricevent/date)
- [var mediaTime: CMTime](/documentation/avfoundation/avmetricevent/mediatime)
- [var sessionID: String?](/documentation/avfoundation/avmetricevent/sessionid)
- [AVMetricErrorEvent](/documentation/avfoundation/avmetricerrorevent)

#### Getting the error

- [var error: any Error](/documentation/avfoundation/avmetricerrorevent/error)
- [var didRecover: Bool](/documentation/avfoundation/avmetricerrorevent/didrecover)
- [Metric event types](/documentation/avfoundation/metric-event-types)

#### HTTP Live Streaming

- [AVMetricMediaResourceRequestEvent](/documentation/avfoundation/avmetricmediaresourcerequestevent)

##### Inspecting the event

- [var byteRange: NSRange](/documentation/avfoundation/avmetricmediaresourcerequestevent/byterange)
- [var errorEvent: AVMetricErrorEvent?](/documentation/avfoundation/avmetricmediaresourcerequestevent/errorevent)
- [var networkTransactionMetrics: URLSessionTaskMetrics?](/documentation/avfoundation/avmetricmediaresourcerequestevent/networktransactionmetrics)
- [var requestEndTime: Date](/documentation/avfoundation/avmetricmediaresourcerequestevent/requestendtime)
- [var requestStartTime: Date](/documentation/avfoundation/avmetricmediaresourcerequestevent/requeststarttime)
- [var responseEndTime: Date](/documentation/avfoundation/avmetricmediaresourcerequestevent/responseendtime)
- [var responseStartTime: Date](/documentation/avfoundation/avmetricmediaresourcerequestevent/responsestarttime)
- [var serverAddress: String?](/documentation/avfoundation/avmetricmediaresourcerequestevent/serveraddress)
- [var url: URL?](/documentation/avfoundation/avmetricmediaresourcerequestevent/url)
- [var wasReadFromCache: Bool](/documentation/avfoundation/avmetricmediaresourcerequestevent/wasreadfromcache)
- [AVMetricContentKeyRequestEvent](/documentation/avfoundation/avmetriccontentkeyrequestevent)

##### Inspecting the event

- [var contentKeySpecifier: AVContentKeySpecifier](/documentation/avfoundation/avmetriccontentkeyrequestevent/contentkeyspecifier)
- [var isClientInitiated: Bool](/documentation/avfoundation/avmetriccontentkeyrequestevent/isclientinitiated)
- [var mediaResourceRequestEvent: AVMetricMediaResourceRequestEvent?](/documentation/avfoundation/avmetriccontentkeyrequestevent/mediaresourcerequestevent)
- [var mediaType: AVMediaType](/documentation/avfoundation/avmetriccontentkeyrequestevent/mediatype)
- [AVMetricHLSMediaSegmentRequestEvent](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent)

##### Inspecting the event

- [var byteRange: NSRange](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent/byterange)
- [var indexFileURL: URL](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent/indexfileurl)
- [var isMapSegment: Bool](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent/ismapsegment)
- [var mediaResourceRequestEvent: AVMetricMediaResourceRequestEvent?](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent/mediaresourcerequestevent)
- [var mediaType: AVMediaType](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent/mediatype)
- [var segmentDuration: TimeInterval](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent/segmentduration)
- [var url: URL?](/documentation/avfoundation/avmetrichlsmediasegmentrequestevent/url)
- [AVMetricHLSPlaylistRequestEvent](/documentation/avfoundation/avmetrichlsplaylistrequestevent)

##### Inspecting the event

- [var isMultivariantPlaylist: Bool](/documentation/avfoundation/avmetrichlsplaylistrequestevent/ismultivariantplaylist)
- [var mediaResourceRequestEvent: AVMetricMediaResourceRequestEvent?](/documentation/avfoundation/avmetrichlsplaylistrequestevent/mediaresourcerequestevent)
- [var mediaType: AVMediaType](/documentation/avfoundation/avmetrichlsplaylistrequestevent/mediatype)
- [var url: URL?](/documentation/avfoundation/avmetrichlsplaylistrequestevent/url)
- [AVMetricPlayerItemVariantSwitchStartEvent](/documentation/avfoundation/avmetricplayeritemvariantswitchstartevent)

##### Inspecting the event

- [var fromVariant: AVAssetVariant?](/documentation/avfoundation/avmetricplayeritemvariantswitchstartevent/fromvariant)
- [var loadedTimeRanges: [CMTimeRange]](/documentation/avfoundation/avmetricplayeritemvariantswitchstartevent/loadedtimeranges-2mbm7)
- [var toVariant: AVAssetVariant](/documentation/avfoundation/avmetricplayeritemvariantswitchstartevent/tovariant)
- [var audioRendition: AVMetricMediaRendition](/documentation/avfoundation/avmetricplayeritemvariantswitchstartevent/audiorendition)
- [var videoRendition: AVMetricMediaRendition](/documentation/avfoundation/avmetricplayeritemvariantswitchstartevent/videorendition)
- [var subtitleRendition: AVMetricMediaRendition](/documentation/avfoundation/avmetricplayeritemvariantswitchstartevent/subtitlerendition)
- [AVMetricPlayerItemVariantSwitchEvent](/documentation/avfoundation/avmetricplayeritemvariantswitchevent)

##### Inspecting the event

- [var didSucceed: Bool](/documentation/avfoundation/avmetricplayeritemvariantswitchevent/didsucceed)
- [var fromVariant: AVAssetVariant?](/documentation/avfoundation/avmetricplayeritemvariantswitchevent/fromvariant)
- [var loadedTimeRanges: [CMTimeRange]](/documentation/avfoundation/avmetricplayeritemvariantswitchevent/loadedtimeranges-5lkmg)
- [var toVariant: AVAssetVariant](/documentation/avfoundation/avmetricplayeritemvariantswitchevent/tovariant)
- [var audioRendition: AVMetricMediaRendition](/documentation/avfoundation/avmetricplayeritemvariantswitchevent/audiorendition)
- [var videoRendition: AVMetricMediaRendition](/documentation/avfoundation/avmetricplayeritemvariantswitchevent/videorendition)
- [var subtitleRendition: AVMetricMediaRendition](/documentation/avfoundation/avmetricplayeritemvariantswitchevent/subtitlerendition)
- [AVMetricMediaRendition](/documentation/avfoundation/avmetricmediarendition)

##### Inspecting the rendition

- [var stableID: String?](/documentation/avfoundation/avmetricmediarendition/stableid)
- [var url: URL?](/documentation/avfoundation/avmetricmediarendition/url)

#### Buffering

- [AVMetricPlayerItemStallEvent](/documentation/avfoundation/avmetricplayeritemstallevent)
- [AVMetricPlayerItemLikelyToKeepUpEvent](/documentation/avfoundation/avmetricplayeritemlikelytokeepupevent)

##### Inspecting the event

- [var loadedTimeRanges: [CMTimeRange]](/documentation/avfoundation/avmetricplayeritemlikelytokeepupevent/loadedtimeranges-8yzws)
- [var timeTaken: TimeInterval](/documentation/avfoundation/avmetricplayeritemlikelytokeepupevent/timetaken)
- [var variant: AVAssetVariant?](/documentation/avfoundation/avmetricplayeritemlikelytokeepupevent/variant)
- [AVMetricPlayerItemInitialLikelyToKeepUpEvent](/documentation/avfoundation/avmetricplayeriteminitiallikelytokeepupevent)

##### Inspecting the event

- [var contentKeyRequestEvents: [AVMetricContentKeyRequestEvent]](/documentation/avfoundation/avmetricplayeriteminitiallikelytokeepupevent/contentkeyrequestevents)
- [var mediaSegmentRequestEvents: [AVMetricHLSMediaSegmentRequestEvent]](/documentation/avfoundation/avmetricplayeriteminitiallikelytokeepupevent/mediasegmentrequestevents)
- [var playlistRequestEvents: [AVMetricHLSPlaylistRequestEvent]](/documentation/avfoundation/avmetricplayeriteminitiallikelytokeepupevent/playlistrequestevents)

#### Transport control

- [AVMetricPlayerItemPlaybackSummaryEvent](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent)

##### Inspecting the event

- [var errorEvent: AVMetricErrorEvent?](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/errorevent)
- [var mediaResourceRequestCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/mediaresourcerequestcount)
- [var playbackDuration: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/playbackduration)
- [var recoverableErrorCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/recoverableerrorcount)
- [var stallCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/stallcount)
- [var timeSpentInInitialStartup: TimeInterval](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timespentininitialstartup)
- [var timeSpentRecoveringFromStall: TimeInterval](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timespentrecoveringfromstall)
- [var timeWeightedAverageBitrate: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timeweightedaveragebitrate)
- [var timeWeightedPeakBitrate: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timeweightedpeakbitrate)
- [var variantSwitchCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/variantswitchcount)
- [AVMetricPlayerItemRateChangeEvent](/documentation/avfoundation/avmetricplayeritemratechangeevent)

##### Inspecting the event

- [var previousRate: Double](/documentation/avfoundation/avmetricplayeritemratechangeevent/previousrate)
- [var rate: Double](/documentation/avfoundation/avmetricplayeritemratechangeevent/rate)
- [var variant: AVAssetVariant?](/documentation/avfoundation/avmetricplayeritemratechangeevent/variant)
- [AVMetricPlayerItemSeekDidCompleteEvent](/documentation/avfoundation/avmetricplayeritemseekdidcompleteevent)

##### Inspecting the event

- [var didSeekInBuffer: Bool](/documentation/avfoundation/avmetricplayeritemseekdidcompleteevent/didseekinbuffer)
- [AVMetricPlayerItemSeekEvent](/documentation/avfoundation/avmetricplayeritemseekevent)

#### Summary

- [AVMetricPlayerItemPlaybackSummaryEvent](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent)

##### Inspecting the event

- [var errorEvent: AVMetricErrorEvent?](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/errorevent)
- [var mediaResourceRequestCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/mediaresourcerequestcount)
- [var playbackDuration: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/playbackduration)
- [var recoverableErrorCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/recoverableerrorcount)
- [var stallCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/stallcount)
- [var timeSpentInInitialStartup: TimeInterval](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timespentininitialstartup)
- [var timeSpentRecoveringFromStall: TimeInterval](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timespentrecoveringfromstall)
- [var timeWeightedAverageBitrate: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timeweightedaveragebitrate)
- [var timeWeightedPeakBitrate: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/timeweightedpeakbitrate)
- [var variantSwitchCount: Int](/documentation/avfoundation/avmetricplayeritemplaybacksummaryevent/variantswitchcount)
- [AVMetricDownloadSummaryEvent](/documentation/avfoundation/avmetricdownloadsummaryevent)

##### Instance Properties

- [var bytesDownloadedCount: Int](/documentation/avfoundation/avmetricdownloadsummaryevent/bytesdownloadedcount)
- [var downloadDuration: TimeInterval](/documentation/avfoundation/avmetricdownloadsummaryevent/downloadduration)
- [var errorEvent: AVMetricErrorEvent?](/documentation/avfoundation/avmetricdownloadsummaryevent/errorevent)
- [var mediaResourceRequestCount: Int](/documentation/avfoundation/avmetricdownloadsummaryevent/mediaresourcerequestcount)
- [var recoverableErrorCount: Int](/documentation/avfoundation/avmetricdownloadsummaryevent/recoverableerrorcount)
- [var variants: [AVAssetVariant]](/documentation/avfoundation/avmetricdownloadsummaryevent/variants)

### Remote controls

- [Supporting remote interactions in tvOS](/documentation/avfoundation/supporting-remote-interactions-in-tvos)

### Timed metadata

- [Presenting chapter markers](/documentation/avfoundation/presenting-chapter-markers)
- [AVMetadataGroup](/documentation/avfoundation/avmetadatagroup)

#### Inspecting the metadata group

- [var items: [AVMetadataItem]](/documentation/avfoundation/avmetadatagroup/items)
- [var uniqueID: String?](/documentation/avfoundation/avmetadatagroup/uniqueid)
- [var classifyingLabel: String?](/documentation/avfoundation/avmetadatagroup/classifyinglabel)
- [AVTimedMetadataGroup](/documentation/avfoundation/avtimedmetadatagroup)

#### Creating a timed metadata group

- [convenience init?(sampleBuffer: CMReadySampleBuffer<CMSampleBuffer.DynamicContent>)](/documentation/avfoundation/avtimedmetadatagroup/init(samplebuffer:)-6atlv)
- [init(items: [AVMetadataItem], timeRange: CMTimeRange)](/documentation/avfoundation/avtimedmetadatagroup/init(items:timerange:))
- [init?(sampleBuffer: CMSampleBuffer)](/documentation/avfoundation/avtimedmetadatagroup/init(samplebuffer:)-bjuo)

#### Accessing group attributes

- [var items: [AVMetadataItem]](/documentation/avfoundation/avtimedmetadatagroup/items)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avtimedmetadatagroup/timerange)

#### Creating a format description

- [func copyFormatDescription() -> CMMetadataFormatDescription?](/documentation/avfoundation/avtimedmetadatagroup/copyformatdescription())
- [AVMutableTimedMetadataGroup](/documentation/avfoundation/avmutabletimedmetadatagroup)

#### Configuring the group

- [var items: [AVMetadataItem]](/documentation/avfoundation/avmutabletimedmetadatagroup/items)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avmutabletimedmetadatagroup/timerange)
- [AVDateRangeMetadataGroup](/documentation/avfoundation/avdaterangemetadatagroup)

#### Creating a date range group

- [init(items: [AVMetadataItem], start: Date, end: Date?)](/documentation/avfoundation/avdaterangemetadatagroup/init(items:start:end:))

#### Accessing the metadata

- [var items: [AVMetadataItem]](/documentation/avfoundation/avdaterangemetadatagroup/items)

#### Accessing the date range

- [var startDate: Date](/documentation/avfoundation/avdaterangemetadatagroup/startdate)
- [var endDate: Date?](/documentation/avfoundation/avdaterangemetadatagroup/enddate)
- [AVMutableDateRangeMetadataGroup](/documentation/avfoundation/avmutabledaterangemetadatagroup)

#### Configuring the metadata

- [var items: [AVMetadataItem]](/documentation/avfoundation/avmutabledaterangemetadatagroup/items)

#### Configuring the date range

- [var startDate: Date](/documentation/avfoundation/avmutabledaterangemetadatagroup/startdate)
- [var endDate: Date?](/documentation/avfoundation/avmutabledaterangemetadatagroup/enddate)
- [AVPlayerItemMediaDataCollector](/documentation/avfoundation/avplayeritemmediadatacollector)
- [AVPlayerItemMetadataCollector](/documentation/avfoundation/avplayeritemmetadatacollector)

#### Creating a metadata collector

- [init(identifiers: [String]?, classifyingLabels: [String]?)](/documentation/avfoundation/avplayeritemmetadatacollector/init(identifiers:classifyinglabels:))

#### Accessing the delegate and callback queue

- [func setDelegate((any AVPlayerItemMetadataCollectorPushDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avplayeritemmetadatacollector/setdelegate(_:queue:))
- [var delegate: (any AVPlayerItemMetadataCollectorPushDelegate)?](/documentation/avfoundation/avplayeritemmetadatacollector/delegate)
- [AVPlayerItemMetadataCollectorPushDelegate](/documentation/avfoundation/avplayeritemmetadatacollectorpushdelegate)

##### Accessing HLS date range metadata

- [func metadataCollector(AVPlayerItemMetadataCollector, didCollect: sending [AVDateRangeMetadataGroup], indexesOfNewGroups: IndexSet, indexesOfModifiedGroups: IndexSet)](/documentation/avfoundation/avplayeritemmetadatacollectorpushdelegate/metadatacollector(_:didcollect:indexesofnewgroups:indexesofmodifiedgroups:))
- [var delegateQueue: dispatch_queue_t?](/documentation/avfoundation/avplayeritemmetadatacollector/delegatequeue)

### Media output

- [AVPlayerVideoOutput](/documentation/avfoundation/avplayervideooutput)

#### Creating an output

- [init(specification: AVVideoOutputSpecification)](/documentation/avfoundation/avplayervideooutput/init(specification:))

#### Accessing video data

- [func sample(forHostTime: CMTime) -> AVPlayerVideoOutput.Sample?](/documentation/avfoundation/avplayervideooutput/sample(forhosttime:))
- [AVPlayerVideoOutput.Sample](/documentation/avfoundation/avplayervideooutput/sample)

##### Inspecting a sample

- [let activeConfiguration: AVPlayerVideoOutput.Configuration](/documentation/avfoundation/avplayervideooutput/sample/activeconfiguration)
- [let presentationTime: CMTime](/documentation/avfoundation/avplayervideooutput/sample/presentationtime)
- [let taggedBuffers: [CMTaggedDynamicBuffer]](/documentation/avfoundation/avplayervideooutput/sample/taggedbuffers)
- [func taggedBuffers(forHostTime: CMTime) -> (taggedBufferGroup: [CMTaggedBuffer], presentationTime: CMTime, activeConfiguration: AVPlayerVideoOutput.Configuration)?](/documentation/avfoundation/avplayervideooutput/taggedbuffers(forhosttime:))
- [AVPlayerVideoOutput.Configuration](/documentation/avfoundation/avplayervideooutput/configuration)

##### Inspecting the configuration

- [var sourcePlayerItem: AVPlayerItem?](/documentation/avfoundation/avplayervideooutput/configuration/sourceplayeritem)
- [var dataChannelDescription: [[CMTag]]](/documentation/avfoundation/avplayervideooutput/configuration/datachanneldescription)
- [var activationTime: CMTime](/documentation/avfoundation/avplayervideooutput/configuration/activationtime)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avplayervideooutput/configuration/preferredtransform)
- [AVVideoOutputSpecification](/documentation/avfoundation/avvideooutputspecification)

#### Creating a specification

- [convenience init(tagCollections: [[CMTag]])](/documentation/avfoundation/avvideooutputspecification/init(tagcollections:))

#### Configuring the specification

- [var defaultOutputSettings: [String : any Sendable]?](/documentation/avfoundation/avvideooutputspecification/defaultoutputsettings)
- [func setOutputSettings([String : any Sendable]?, for: [CMTag])](/documentation/avfoundation/avvideooutputspecification/setoutputsettings(_:for:))
- [var defaultPixelBufferAttributes: [String : Any]?](/documentation/avfoundation/avvideooutputspecification/defaultpixelbufferattributes)
- [func setOutputPixelBufferAttributes([String : Any]?, for: [CMTag])](/documentation/avfoundation/avvideooutputspecification/setoutputpixelbufferattributes(_:for:))
- [var preferredTagCollections: [[CMTag]]](/documentation/avfoundation/avvideooutputspecification/preferredtagcollections-3gdo7)
- [AVPlayerItemOutput](/documentation/avfoundation/avplayeritemoutput)

#### Time conversion

- [func itemTime(forHostTime: CFTimeInterval) -> CMTime](/documentation/avfoundation/avplayeritemoutput/itemtime(forhosttime:))
- [func itemTime(forMachAbsoluteTime: Int64) -> CMTime](/documentation/avfoundation/avplayeritemoutput/itemtime(formachabsolutetime:))
- [func itemTime(for: CVTimeStamp) -> CMTime](/documentation/avfoundation/avplayeritemoutput/itemtime(for:))

#### Configuring the playback options

- [var suppressesPlayerRendering: Bool](/documentation/avfoundation/avplayeritemoutput/suppressesplayerrendering)
- [AVPlayerItemVideoOutput](/documentation/avfoundation/avplayeritemvideooutput)

#### Creating a video output

- [init(pixelBufferAttributes: [String : any Sendable]?)](/documentation/avfoundation/avplayeritemvideooutput/init(pixelbufferattributes:)-7n7v8)
- [convenience init(pixelBufferAttributes: CVPixelBufferAttributes)](/documentation/avfoundation/avplayeritemvideooutput/init(pixelbufferattributes:)-18izh)
- [init(outputSettings: [String : any Sendable]?)](/documentation/avfoundation/avplayeritemvideooutput/init(outputsettings:))

#### Configuring the delegate

- [func setDelegate((any AVPlayerItemOutputPullDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avplayeritemvideooutput/setdelegate(_:queue:))
- [var delegate: (any AVPlayerItemOutputPullDelegate)?](/documentation/avfoundation/avplayeritemvideooutput/delegate)
- [AVPlayerItemOutputPullDelegate](/documentation/avfoundation/avplayeritemoutputpulldelegate)

##### Responding to pixel buffer changes

- [func outputMediaDataWillChange(AVPlayerItemOutput)](/documentation/avfoundation/avplayeritemoutputpulldelegate/outputmediadatawillchange(_:))
- [func outputSequenceWasFlushed(AVPlayerItemOutput)](/documentation/avfoundation/avplayeritemoutputpulldelegate/outputsequencewasflushed(_:))
- [var delegateQueue: dispatch_queue_t?](/documentation/avfoundation/avplayeritemvideooutput/delegatequeue)

#### Notifying the delegate of changes

- [func requestNotificationOfMediaDataChange(withAdvanceInterval: TimeInterval)](/documentation/avfoundation/avplayeritemvideooutput/requestnotificationofmediadatachange(withadvanceinterval:))

#### Getting pixel buffer data

- [func hasNewPixelBuffer(forItemTime: CMTime) -> Bool](/documentation/avfoundation/avplayeritemvideooutput/hasnewpixelbuffer(foritemtime:))
- [func copyPixelBuffer(forItemTime: CMTime, itemTimeForDisplay: UnsafeMutablePointer<CMTime>?) -> CVPixelBuffer?](/documentation/avfoundation/avplayeritemvideooutput/copypixelbuffer(foritemtime:itemtimefordisplay:))
- [func pixelBufferAndDisplayTime(forItemTime: CMTime) -> (pixelBuffer: CVReadOnlyPixelBuffer?, itemTimeForDisplay: CMTime)](/documentation/avfoundation/avplayeritemvideooutput/pixelbufferanddisplaytime(foritemtime:))
- [AVPlayerItemLegibleOutput](/documentation/avfoundation/avplayeritemlegibleoutput)

#### Creating a legible output

- [init(mediaSubtypesForNativeRepresentation: [NSNumber])](/documentation/avfoundation/avplayeritemlegibleoutput/init(mediasubtypesfornativerepresentation:))

#### Configuring text styling

- [var textStylingResolution: AVPlayerItemLegibleOutput.TextStylingResolution](/documentation/avfoundation/avplayeritemlegibleoutput/textstylingresolution-swift.property)
- [AVPlayerItemLegibleOutput.TextStylingResolution](/documentation/avfoundation/avplayeritemlegibleoutput/textstylingresolution-swift.struct)

##### Text styling options

- [static let `default`: AVPlayerItemLegibleOutput.TextStylingResolution](/documentation/avfoundation/avplayeritemlegibleoutput/textstylingresolution-swift.struct/default)
- [static let sourceAndRulesOnly: AVPlayerItemLegibleOutput.TextStylingResolution](/documentation/avfoundation/avplayeritemlegibleoutput/textstylingresolution-swift.struct/sourceandrulesonly)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avplayeritemlegibleoutput/textstylingresolution-swift.struct/init(rawvalue:))

#### Configuring the delegate

- [var delegate: (any AVPlayerItemLegibleOutputPushDelegate)?](/documentation/avfoundation/avplayeritemlegibleoutput/delegate)
- [func setDelegate((any AVPlayerItemLegibleOutputPushDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avplayeritemlegibleoutput/setdelegate(_:queue:))
- [AVPlayerItemLegibleOutputPushDelegate](/documentation/avfoundation/avplayeritemlegibleoutputpushdelegate)

##### Providing alternative attributed-string output

- [func legibleOutput(AVPlayerItemLegibleOutput, didOutputAttributedStrings: [NSAttributedString], nativeSampleBuffers: [Any], forItemTime: CMTime)](/documentation/avfoundation/avplayeritemlegibleoutputpushdelegate/legibleoutput(_:didoutputattributedstrings:nativesamplebuffers:foritemtime:))
- [var advanceIntervalForDelegateInvocation: TimeInterval](/documentation/avfoundation/avplayeritemlegibleoutput/advanceintervalfordelegateinvocation)
- [var delegateQueue: dispatch_queue_t?](/documentation/avfoundation/avplayeritemlegibleoutput/delegatequeue)
- [AVPlayerItemRenderedLegibleOutput](/documentation/avfoundation/avplayeritemrenderedlegibleoutput)

#### Creating an output

- [init(videoDisplay: CGSize)](/documentation/avfoundation/avplayeritemrenderedlegibleoutput/init(videodisplay:))

#### Configuring an output

- [var advanceIntervalForDelegateInvocation: TimeInterval](/documentation/avfoundation/avplayeritemrenderedlegibleoutput/advanceintervalfordelegateinvocation)
- [var videoDisplaySize: CGSize](/documentation/avfoundation/avplayeritemrenderedlegibleoutput/videodisplaysize)

#### Setting a delegate

- [var delegate: (any AVPlayerItemRenderedLegibleOutputPushDelegate)?](/documentation/avfoundation/avplayeritemrenderedlegibleoutput/delegate)
- [func setDelegate((any AVPlayerItemRenderedLegibleOutputPushDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avplayeritemrenderedlegibleoutput/setdelegate(_:queue:))
- [var delegateQueue: dispatch_queue_t?](/documentation/avfoundation/avplayeritemrenderedlegibleoutput/delegatequeue)
- [AVPlayerItemRenderedLegibleOutputPushDelegate](/documentation/avfoundation/avplayeritemrenderedlegibleoutputpushdelegate)

##### Handling rendered pixel buffers

- [func renderedLegibleOutput(AVPlayerItemRenderedLegibleOutput, didOutputRenderedCaptionImages: [AVRenderedCaptionImage], forItemTime: CMTime)](/documentation/avfoundation/avplayeritemrenderedlegibleoutputpushdelegate/renderedlegibleoutput(_:didoutputrenderedcaptionimages:foritemtime:))
- [AVRenderedCaptionImage](/documentation/avfoundation/avrenderedcaptionimage)

#### Inspecting the image

- [var pixelBuffer: CVPixelBuffer](/documentation/avfoundation/avrenderedcaptionimage/pixelbuffer)
- [var readOnlyPixelBuffer: CVReadOnlyPixelBuffer](/documentation/avfoundation/avrenderedcaptionimage/readonlypixelbuffer)
- [var position: CGPoint](/documentation/avfoundation/avrenderedcaptionimage/position)
- [AVPlayerItemMetadataOutput](/documentation/avfoundation/avplayeritemmetadataoutput)

#### Creating a metadata output

- [init(identifiers: [String]?)](/documentation/avfoundation/avplayeritemmetadataoutput/init(identifiers:))

#### Configuring the delegate

- [var advanceIntervalForDelegateInvocation: TimeInterval](/documentation/avfoundation/avplayeritemmetadataoutput/advanceintervalfordelegateinvocation)
- [var delegate: (any AVPlayerItemMetadataOutputPushDelegate)?](/documentation/avfoundation/avplayeritemmetadataoutput/delegate)
- [AVPlayerItemMetadataOutputPushDelegate](/documentation/avfoundation/avplayeritemmetadataoutputpushdelegate)

##### Combining timed metadata groups

- [func metadataOutput(AVPlayerItemMetadataOutput, didOutputTimedMetadataGroups: sending [AVTimedMetadataGroup], from: AVPlayerItemTrack?)](/documentation/avfoundation/avplayeritemmetadataoutputpushdelegate/metadataoutput(_:didoutputtimedmetadatagroups:from:))
- [var delegateQueue: dispatch_queue_t?](/documentation/avfoundation/avplayeritemmetadataoutput/delegatequeue)
- [func setDelegate((any AVPlayerItemMetadataOutputPushDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avplayeritemmetadataoutput/setdelegate(_:queue:))
- [AVPlayerItemOutputPushDelegate](/documentation/avfoundation/avplayeritemoutputpushdelegate)

#### Flushing sequence state

- [func outputSequenceWasFlushed(AVPlayerItemOutput)](/documentation/avfoundation/avplayeritemoutputpushdelegate/outputsequencewasflushed(_:))

### Utilities

- [AVAssetPlaybackAssistant](/documentation/avfoundation/avassetplaybackassistant)

#### Creating a playback assistant

- [convenience init(asset: AVAsset)](/documentation/avfoundation/avassetplaybackassistant/init(asset:))

#### Loading playback configuration options

- [func loadPlaybackConfigurationOptions(completionHandler: ([AVAssetPlaybackConfigurationOption]) -> Void)](/documentation/avfoundation/avassetplaybackassistant/loadplaybackconfigurationoptions(completionhandler:))
- [AVAssetPlaybackConfigurationOption](/documentation/avfoundation/avassetplaybackconfigurationoption)

#### Configuration options

- [static let stereoVideo: AVAssetPlaybackConfigurationOption](/documentation/avfoundation/avassetplaybackconfigurationoption/stereovideo)
- [static let stereoMultiviewVideo: AVAssetPlaybackConfigurationOption](/documentation/avfoundation/avassetplaybackconfigurationoption/stereomultiviewvideo)
- [static let spatialVideo: AVAssetPlaybackConfigurationOption](/documentation/avfoundation/avassetplaybackconfigurationoption/spatialvideo)
- [static let appleImmersiveVideo: AVAssetPlaybackConfigurationOption](/documentation/avfoundation/avassetplaybackconfigurationoption/appleimmersivevideo)
- [static let nonRectilinearProjection: AVAssetPlaybackConfigurationOption](/documentation/avfoundation/avassetplaybackconfigurationoption/nonrectilinearprojection)

#### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avassetplaybackconfigurationoption/init(rawvalue:))
- [Offline playback and storage](/documentation/avfoundation/offline-playback-and-storage)

### Asset downloading

- [Using AVFoundation to play and persist HTTP live streams](/documentation/avfoundation/using-avfoundation-to-play-and-persist-http-live-streams)
- [AVAssetDownloadURLSession](/documentation/avfoundation/avassetdownloadurlsession)

#### Creating a download session

- [init(configuration: URLSessionConfiguration, assetDownloadDelegate: (any AVAssetDownloadDelegate)?, delegateQueue: OperationQueue?)](/documentation/avfoundation/avassetdownloadurlsession/init(configuration:assetdownloaddelegate:delegatequeue:))
- [AVAssetDownloadDelegate](/documentation/avfoundation/avassetdownloaddelegate)

##### Responding to download events

- [func urlSession(URLSession, assetDownloadTask: AVAssetDownloadTask, didResolve: AVMediaSelection)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:assetdownloadtask:didresolve:))
- [func urlSession(URLSession, assetDownloadTask: AVAssetDownloadTask, didLoad: CMTimeRange, totalTimeRangesLoaded: [NSValue], timeRangeExpectedToLoad: CMTimeRange)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:assetdownloadtask:didload:totaltimerangesloaded:timerangeexpectedtoload:))
- [func urlSession(URLSession, assetDownloadTask: AVAssetDownloadTask, didFinishDownloadingTo: URL)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:assetdownloadtask:didfinishdownloadingto:))
- [func urlSession(URLSession, assetDownloadTask: AVAssetDownloadTask, willDownloadVariants: [AVAssetVariant])](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:assetdownloadtask:willdownloadvariants:))
- [func urlSession(URLSession, assetDownloadTask: AVAssetDownloadTask, willDownloadTo: URL)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:assetdownloadtask:willdownloadto:))
- [func urlSession(URLSession, assetDownloadTask: AVAssetDownloadTask, didReceive: AVMetricEvent)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:assetdownloadtask:didreceive:))

##### Responding to aggregate download events

- [func urlSession(URLSession, aggregateAssetDownloadTask: AVAggregateAssetDownloadTask, willDownloadTo: URL)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:aggregateassetdownloadtask:willdownloadto:))
- [func urlSession(URLSession, aggregateAssetDownloadTask: AVAggregateAssetDownloadTask, didLoad: CMTimeRange, totalTimeRangesLoaded: [NSValue], timeRangeExpectedToLoad: CMTimeRange, for: AVMediaSelection)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:aggregateassetdownloadtask:didload:totaltimerangesloaded:timerangeexpectedtoload:for:))
- [func urlSession(URLSession, aggregateAssetDownloadTask: AVAggregateAssetDownloadTask, didCompleteFor: AVMediaSelection)](/documentation/avfoundation/avassetdownloaddelegate/urlsession(_:aggregateassetdownloadtask:didcompletefor:))

#### Creating download tasks

- [func makeAssetDownloadTask(downloadConfiguration: AVAssetDownloadConfiguration) -> AVAssetDownloadTask](/documentation/avfoundation/avassetdownloadurlsession/makeassetdownloadtask(downloadconfiguration:))
- [AVAssetDownloadConfiguration](/documentation/avfoundation/avassetdownloadconfiguration)

##### Creating a configuration

- [convenience init(asset: AVURLAsset, title: String)](/documentation/avfoundation/avassetdownloadconfiguration/init(asset:title:))

##### Accessing configuration details

- [var artworkData: Data?](/documentation/avfoundation/avassetdownloadconfiguration/artworkdata)
- [var primaryContentConfiguration: AVAssetDownloadContentConfiguration](/documentation/avfoundation/avassetdownloadconfiguration/primarycontentconfiguration)
- [var auxiliaryContentConfigurations: [AVAssetDownloadContentConfiguration]](/documentation/avfoundation/avassetdownloadconfiguration/auxiliarycontentconfigurations)
- [AVAssetDownloadContentConfiguration](/documentation/avfoundation/avassetdownloadcontentconfiguration)

###### Accessing configuration details

- [var variantQualifiers: [AVAssetVariantQualifier]](/documentation/avfoundation/avassetdownloadcontentconfiguration/variantqualifiers)
- [AVAssetVariantQualifier](/documentation/avfoundation/avassetvariantqualifier)

###### Creating a variant qualifier

- [convenience init(variant: AVAssetVariant)](/documentation/avfoundation/avassetvariantqualifier/init(variant:))
- [AVAssetVariant](/documentation/avfoundation/avassetvariant)

###### Configuring attributes

- [var audioAttributes: AVAssetVariant.AudioAttributes?](/documentation/avfoundation/avassetvariant/audioattributes-swift.property)
- [AVAssetVariant.AudioAttributes](/documentation/avfoundation/avassetvariant/audioattributes-swift.class)

###### Inspecting audio attributes

- [var formatIDs: [AudioFormatID]](/documentation/avfoundation/avassetvariant/audioattributes-swift.class/formatids)
- [func renditionSpecificAttributes(for: AVMediaSelectionOption) -> AVAssetVariant.AudioAttributes.RenditionSpecificAttributes?](/documentation/avfoundation/avassetvariant/audioattributes-swift.class/renditionspecificattributes(for:))
- [AVAssetVariant.AudioAttributes.RenditionSpecificAttributes](/documentation/avfoundation/avassetvariant/audioattributes-swift.class/renditionspecificattributes)

###### Accessing attributes

- [var channelCount: Int?](/documentation/avfoundation/avassetvariant/audioattributes-swift.class/renditionspecificattributes/channelcount)
- [var isBinaural: Bool](/documentation/avfoundation/avassetvariant/audioattributes-swift.class/renditionspecificattributes/isbinaural)
- [var isImmersive: Bool](/documentation/avfoundation/avassetvariant/audioattributes-swift.class/renditionspecificattributes/isimmersive)
- [var isDownmix: Bool](/documentation/avfoundation/avassetvariant/audioattributes-swift.class/renditionspecificattributes/isdownmix)
- [var videoAttributes: AVAssetVariant.VideoAttributes?](/documentation/avfoundation/avassetvariant/videoattributes-swift.property)
- [AVAssetVariant.VideoAttributes](/documentation/avfoundation/avassetvariant/videoattributes-swift.class)

###### Inspecting the attributes

- [var codecTypes: [CMVideoCodecType]](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/codectypes)
- [var nominalFrameRate: Double?](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/nominalframerate)
- [var presentationSize: CGSize](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/presentationsize)
- [var videoRange: AVVideoRange](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/videorange)
- [AVVideoRange](/documentation/avfoundation/avvideorange)

###### Video ranges

- [static let pq: AVVideoRange](/documentation/avfoundation/avvideorange/pq)
- [static let hlg: AVVideoRange](/documentation/avfoundation/avvideorange/hlg)
- [static let sdr: AVVideoRange](/documentation/avfoundation/avvideorange/sdr)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideorange/init(rawvalue:))
- [var videoLayoutAttributes: [AVAssetVariant.VideoAttributes.LayoutAttributes]](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/videolayoutattributes)
- [AVAssetVariant.VideoAttributes.LayoutAttributes](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/layoutattributes)

###### Accessing attributes

- [var stereoViewComponents: CMStereoViewComponents](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/layoutattributes/stereoviewcomponents)
- [var projectionType: CMProjectionType](/documentation/avfoundation/avassetvariant/videoattributes-swift.class/layoutattributes/projectiontype)

###### Configuring bit rate

- [var averageBitRate: Double?](/documentation/avfoundation/avassetvariant/averagebitrate-5p1oh)
- [var peakBitRate: Double?](/documentation/avfoundation/avassetvariant/peakbitrate-9hzpi)

###### Accessing the URL

- [var url: URL](/documentation/avfoundation/avassetvariant/url)
- [convenience init(predicate: NSPredicate)](/documentation/avfoundation/avassetvariantqualifier/init(predicate:))

###### Building predicates

- [class func predicate(forAudioSampleRate: Double, mediaSelectionOption: AVMediaSelectionOption?, operatorType: NSComparisonPredicate.Operator) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(foraudiosamplerate:mediaselectionoption:operatortype:))
- [class func predicate(forAudioSampleRate: Double, operatorType: NSComparisonPredicate.Operator) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(foraudiosamplerate:operatortype:))
- [class func predicate(forBinauralAudio: Bool) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forbinauralaudio:))
- [class func predicate(forBinauralAudio: Bool, mediaSelectionOption: AVMediaSelectionOption?) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forbinauralaudio:mediaselectionoption:))
- [class func predicate(forChannelCount: Int, mediaSelectionOption: AVMediaSelectionOption?, operatorType: NSComparisonPredicate.Operator) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forchannelcount:mediaselectionoption:operatortype:))
- [class func predicate(forChannelCount: Int, operatorType: NSComparisonPredicate.Operator) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forchannelcount:operatortype:))
- [class func predicate(forDownmixAudio: Bool) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(fordownmixaudio:))
- [class func predicate(forDownmixAudio: Bool, mediaSelectionOption: AVMediaSelectionOption?) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(fordownmixaudio:mediaselectionoption:))
- [class func predicate(forImmersiveAudio: Bool) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forimmersiveaudio:))
- [class func predicate(forImmersiveAudio: Bool, mediaSelectionOption: AVMediaSelectionOption?) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forimmersiveaudio:mediaselectionoption:))
- [class func predicate(forPresentationHeight: CGFloat, operatorType: NSComparisonPredicate.Operator) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forpresentationheight:operatortype:))
- [class func predicate(forPresentationWidth: CGFloat, operatorType: NSComparisonPredicate.Operator) -> NSPredicate](/documentation/avfoundation/avassetvariantqualifier/predicate(forpresentationwidth:operatortype:))
- [var mediaSelections: [AVMediaSelection]](/documentation/avfoundation/avassetdownloadcontentconfiguration/mediaselections)
- [var optimizesAuxiliaryContentConfigurations: Bool](/documentation/avfoundation/avassetdownloadconfiguration/optimizesauxiliarycontentconfigurations)
- [func setInterstitialMediaSelectionCriteria([AVPlayerMediaSelectionCriteria], forMediaCharacteristic: AVMediaCharacteristic)](/documentation/avfoundation/avassetdownloadconfiguration/setinterstitialmediaselectioncriteria(_:formediacharacteristic:))
- [func makeAssetDownloadTask(asset: AVURLAsset, assetTitle: String, assetArtworkData: Data?, options: [String : Any]?) -> AVAssetDownloadTask?](/documentation/avfoundation/avassetdownloadurlsession/makeassetdownloadtask(asset:assettitle:assetartworkdata:options:))

##### Download option keys

- [let AVAssetDownloadTaskMinimumRequiredMediaBitrateKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredmediabitratekey)
- [let AVAssetDownloadTaskMinimumRequiredPresentationSizeKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredpresentationsizekey)
- [let AVAssetDownloadTaskMediaSelectionKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionkey)
- [let AVAssetDownloadTaskMediaSelectionPrefersMultichannelKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionprefersmultichannelkey)
- [let AVAssetDownloadTaskPrefersHDRKey: String](/documentation/avfoundation/avassetdownloadtaskprefershdrkey)
- [let AVAssetDownloadTaskPrefersLosslessAudioKey: String](/documentation/avfoundation/avassetdownloadtaskpreferslosslessaudiokey)
- [func aggregateAssetDownloadTask(with: AVURLAsset, mediaSelections: [AVMediaSelection], assetTitle: String, assetArtworkData: Data?, options: [String : Any]?) -> AVAggregateAssetDownloadTask?](/documentation/avfoundation/avassetdownloadurlsession/aggregateassetdownloadtask(with:mediaselections:assettitle:assetartworkdata:options:))

##### Download option keys

- [let AVAssetDownloadTaskMinimumRequiredMediaBitrateKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredmediabitratekey)
- [let AVAssetDownloadTaskMinimumRequiredPresentationSizeKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredpresentationsizekey)
- [let AVAssetDownloadTaskMediaSelectionKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionkey)
- [let AVAssetDownloadTaskMediaSelectionPrefersMultichannelKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionprefersmultichannelkey)
- [let AVAssetDownloadTaskPrefersHDRKey: String](/documentation/avfoundation/avassetdownloadtaskprefershdrkey)
- [let AVAssetDownloadTaskPrefersLosslessAudioKey: String](/documentation/avfoundation/avassetdownloadtaskpreferslosslessaudiokey)
- [func makeAssetDownloadTask(asset: AVURLAsset, destinationURL: URL, options: [String : Any]?) -> AVAssetDownloadTask?](/documentation/avfoundation/avassetdownloadurlsession/makeassetdownloadtask(asset:destinationurl:options:))

##### Download option keys

- [let AVAssetDownloadTaskMinimumRequiredMediaBitrateKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredmediabitratekey)
- [let AVAssetDownloadTaskMinimumRequiredPresentationSizeKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredpresentationsizekey)
- [let AVAssetDownloadTaskMediaSelectionKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionkey)
- [let AVAssetDownloadTaskMediaSelectionPrefersMultichannelKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionprefersmultichannelkey)
- [let AVAssetDownloadTaskPrefersHDRKey: String](/documentation/avfoundation/avassetdownloadtaskprefershdrkey)
- [let AVAssetDownloadTaskPrefersLosslessAudioKey: String](/documentation/avfoundation/avassetdownloadtaskpreferslosslessaudiokey)

#### Download option keys

- [let AVAssetDownloadTaskMinimumRequiredMediaBitrateKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredmediabitratekey)
- [let AVAssetDownloadTaskMinimumRequiredPresentationSizeKey: String](/documentation/avfoundation/avassetdownloadtaskminimumrequiredpresentationsizekey)
- [let AVAssetDownloadTaskMediaSelectionKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionkey)
- [let AVAssetDownloadTaskMediaSelectionPrefersMultichannelKey: String](/documentation/avfoundation/avassetdownloadtaskmediaselectionprefersmultichannelkey)
- [let AVAssetDownloadTaskPrefersHDRKey: String](/documentation/avfoundation/avassetdownloadtaskprefershdrkey)
- [let AVAssetDownloadTaskPrefersLosslessAudioKey: String](/documentation/avfoundation/avassetdownloadtaskpreferslosslessaudiokey)
- [AVAssetDownloadTask](/documentation/avfoundation/avassetdownloadtask)

#### Accessing task information

- [var urlAsset: AVURLAsset](/documentation/avfoundation/avassetdownloadtask/urlasset)
- [var loadedTimeRanges: [NSValue]](/documentation/avfoundation/avassetdownloadtask/loadedtimeranges)
- [var options: [String : Any]?](/documentation/avfoundation/avassetdownloadtask/options)
- [var destinationURL: URL](/documentation/avfoundation/avassetdownloadtask/destinationurl)
- [AVAggregateAssetDownloadTask](/documentation/avfoundation/avaggregateassetdownloadtask)

#### Accessing the asset

- [var urlAsset: AVURLAsset](/documentation/avfoundation/avaggregateassetdownloadtask/urlasset)

### Offline storage management

- [AVAssetDownloadStorageManager](/documentation/avfoundation/avassetdownloadstoragemanager)

#### Accessing the shared manager

- [class func shared() -> AVAssetDownloadStorageManager](/documentation/avfoundation/avassetdownloadstoragemanager/shared())

#### Setting the storage policy

- [func storageManagementPolicy(for: URL) -> AVAssetDownloadStorageManagementPolicy?](/documentation/avfoundation/avassetdownloadstoragemanager/storagemanagementpolicy(for:))
- [func setStorageManagementPolicy(AVAssetDownloadStorageManagementPolicy, for: URL)](/documentation/avfoundation/avassetdownloadstoragemanager/setstoragemanagementpolicy(_:for:))
- [AVAssetDownloadStorageManagementPolicy](/documentation/avfoundation/avassetdownloadstoragemanagementpolicy)

#### Inspecting a policy

- [var expirationDate: Date](/documentation/avfoundation/avassetdownloadstoragemanagementpolicy/expirationdate)
- [var priority: AVAssetDownloadedAssetEvictionPriority](/documentation/avfoundation/avassetdownloadstoragemanagementpolicy/priority)
- [AVMutableAssetDownloadStorageManagementPolicy](/documentation/avfoundation/avmutableassetdownloadstoragemanagementpolicy)

#### Managing storage

- [var expirationDate: Date](/documentation/avfoundation/avmutableassetdownloadstoragemanagementpolicy/expirationdate)
- [var priority: AVAssetDownloadedAssetEvictionPriority](/documentation/avfoundation/avmutableassetdownloadstoragemanagementpolicy/priority)
- [AVAssetDownloadedAssetEvictionPriority](/documentation/avfoundation/avassetdownloadedassetevictionpriority)

##### Eviction priorities

- [static let `default`: AVAssetDownloadedAssetEvictionPriority](/documentation/avfoundation/avassetdownloadedassetevictionpriority/default)
- [static let important: AVAssetDownloadedAssetEvictionPriority](/documentation/avfoundation/avassetdownloadedassetevictionpriority/important)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avassetdownloadedassetevictionpriority/init(rawvalue:))

### Cache monitoring

- [AVAssetCache](/documentation/avfoundation/avassetcache)

#### Inspecting the cached media

- [var isPlayableOffline: Bool](/documentation/avfoundation/avassetcache/isplayableoffline)
- [func mediaSelectionOptions(in: AVMediaSelectionGroup) -> [AVMediaSelectionOption]](/documentation/avfoundation/avassetcache/mediaselectionoptions(in:))
- [func mediaPresentationLanguages(for: AVMediaSelectionGroup) -> [String]](/documentation/avfoundation/avassetcache/mediapresentationlanguages(for:))
- [func mediaPresentationSettings(for: AVMediaSelectionGroup) -> [AVMediaPresentationSelector : [AVMediaPresentationSetting]]](/documentation/avfoundation/avassetcache/mediapresentationsettings(for:))
- [Streaming and AirPlay](/documentation/avfoundation/streaming-and-airplay)

### Essentials

- [Supporting AirPlay in your app](/documentation/avfoundation/supporting-airplay-in-your-app)

### Route selection

- [AVRouteDetector](/documentation/avfoundation/avroutedetector)

#### Detecting routes

- [var detectsCustomRoutes: Bool](/documentation/avfoundation/avroutedetector/detectscustomroutes)
- [var isRouteDetectionEnabled: Bool](/documentation/avfoundation/avroutedetector/isroutedetectionenabled)
- [var multipleRoutesDetected: Bool](/documentation/avfoundation/avroutedetector/multipleroutesdetected)
- [static let AVRouteDetectorMultipleRoutesDetectedDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/avroutedetectormultipleroutesdetecteddidchange)

### Buffered playback

- [Implementing simple enhanced buffering for your content](/documentation/avfoundation/implementing-simple-enhanced-buffering-for-your-content)
- [Implementing flexible enhanced buffering for your content](/documentation/avfoundation/implementing-flexible-enhanced-buffering-for-your-content)
- [Integrating AirPlay for long-form video apps](/documentation/avfoundation/integrating-airplay-for-long-form-video-apps)

### Resource loading

- [AVAssetResourceLoader](/documentation/avfoundation/avassetresourceloader)

#### Accessing the delegate

- [func setDelegate((any AVAssetResourceLoaderDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avassetresourceloader/setdelegate(_:queue:))
- [var delegate: (any AVAssetResourceLoaderDelegate)?](/documentation/avfoundation/avassetresourceloader/delegate)
- [AVAssetResourceLoaderDelegate](/documentation/avfoundation/avassetresourceloaderdelegate)

##### Processing resource requests

- [func resourceLoader(AVAssetResourceLoader, shouldWaitForLoadingOfRequestedResource: AVAssetResourceLoadingRequest) -> Bool](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:shouldwaitforloadingofrequestedresource:))
- [func resourceLoader(AVAssetResourceLoader, shouldWaitForRenewalOfRequestedResource: AVAssetResourceRenewalRequest) -> Bool](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:shouldwaitforrenewalofrequestedresource:))
- [func resourceLoader(AVAssetResourceLoader, didCancel: AVAssetResourceLoadingRequest)](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:didcancel:)-3nl51)

##### Processing authentication challenges

- [func resourceLoader(AVAssetResourceLoader, shouldWaitForResponseTo: URLAuthenticationChallenge) -> Bool](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:shouldwaitforresponseto:))
- [func resourceLoader(AVAssetResourceLoader, didCancel: URLAuthenticationChallenge)](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:didcancel:)-1wqin)
- [var delegateQueue: dispatch_queue_t?](/documentation/avfoundation/avassetresourceloader/delegatequeue)

#### Loading content keys

- [var preloadsEligibleContentKeys: Bool](/documentation/avfoundation/avassetresourceloader/preloadseligiblecontentkeys)

#### Supporting Common Media Client Data

- [var sendsCommonMediaClientDataAsHTTPHeaders: Bool](/documentation/avfoundation/avassetresourceloader/sendscommonmediaclientdataashttpheaders)
- [AVAssetResourceLoaderDelegate](/documentation/avfoundation/avassetresourceloaderdelegate)

#### Processing resource requests

- [func resourceLoader(AVAssetResourceLoader, shouldWaitForLoadingOfRequestedResource: AVAssetResourceLoadingRequest) -> Bool](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:shouldwaitforloadingofrequestedresource:))
- [func resourceLoader(AVAssetResourceLoader, shouldWaitForRenewalOfRequestedResource: AVAssetResourceRenewalRequest) -> Bool](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:shouldwaitforrenewalofrequestedresource:))
- [func resourceLoader(AVAssetResourceLoader, didCancel: AVAssetResourceLoadingRequest)](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:didcancel:)-3nl51)

#### Processing authentication challenges

- [func resourceLoader(AVAssetResourceLoader, shouldWaitForResponseTo: URLAuthenticationChallenge) -> Bool](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:shouldwaitforresponseto:))
- [func resourceLoader(AVAssetResourceLoader, didCancel: URLAuthenticationChallenge)](/documentation/avfoundation/avassetresourceloaderdelegate/resourceloader(_:didcancel:)-1wqin)
- [AVAssetResourceLoadingRequest](/documentation/avfoundation/avassetresourceloadingrequest)

#### Accessing the request data

- [var request: URLRequest](/documentation/avfoundation/avassetresourceloadingrequest/request)
- [var requestor: AVAssetResourceLoadingRequestor](/documentation/avfoundation/avassetresourceloadingrequest/requestor)
- [var contentInformationRequest: AVAssetResourceLoadingContentInformationRequest?](/documentation/avfoundation/avassetresourceloadingrequest/contentinformationrequest)
- [var dataRequest: AVAssetResourceLoadingDataRequest?](/documentation/avfoundation/avassetresourceloadingrequest/datarequest)
- [var redirect: URLRequest?](/documentation/avfoundation/avassetresourceloadingrequest/redirect)
- [func streamingContentKeyRequestData(forApp: Data, contentIdentifier: Data, options: [String : Any]?) throws -> Data](/documentation/avfoundation/avassetresourceloadingrequest/streamingcontentkeyrequestdata(forapp:contentidentifier:options:))

##### Configuration options

- [let AVAssetResourceLoadingRequestStreamingContentKeyRequestRequiresPersistentKey: String](/documentation/avfoundation/avassetresourceloadingrequeststreamingcontentkeyrequestrequirespersistentkey)
- [func persistentContentKey(fromKeyVendorResponse: Data, options: [String : Any]?) throws -> Data](/documentation/avfoundation/avassetresourceloadingrequest/persistentcontentkey(fromkeyvendorresponse:options:))
- [let AVAssetResourceLoadingRequestStreamingContentKeyRequestRequiresPersistentKey: String](/documentation/avfoundation/avassetresourceloadingrequeststreamingcontentkeyrequestrequirespersistentkey)

#### Reporting the result of the request

- [var response: URLResponse?](/documentation/avfoundation/avassetresourceloadingrequest/response)
- [func finishLoading()](/documentation/avfoundation/avassetresourceloadingrequest/finishloading())
- [var isCancelled: Bool](/documentation/avfoundation/avassetresourceloadingrequest/iscancelled)
- [func finishLoading(with: (any Error)?)](/documentation/avfoundation/avassetresourceloadingrequest/finishloading(with:))
- [var isFinished: Bool](/documentation/avfoundation/avassetresourceloadingrequest/isfinished)
- [func finishLoading(with: URLResponse?, data: Data?, redirect: URLRequest?)](/documentation/avfoundation/avassetresourceloadingrequest/finishloading(with:data:redirect:))
- [AVAssetResourceRenewalRequest](/documentation/avfoundation/avassetresourcerenewalrequest)
- [AVAssetResourceLoadingRequestor](/documentation/avfoundation/avassetresourceloadingrequestor)

#### Retrieving expired session reports

- [var providesExpiredSessionReports: Bool](/documentation/avfoundation/avassetresourceloadingrequestor/providesexpiredsessionreports)
- [AVAssetResourceLoadingDataRequest](/documentation/avfoundation/avassetresourceloadingdatarequest)

#### Providing data to a request

- [func respond(with: Data)](/documentation/avfoundation/avassetresourceloadingdatarequest/respond(with:))
- [var requestedLength: Int](/documentation/avfoundation/avassetresourceloadingdatarequest/requestedlength)
- [var requestedOffset: Int64](/documentation/avfoundation/avassetresourceloadingdatarequest/requestedoffset)
- [var currentOffset: Int64](/documentation/avfoundation/avassetresourceloadingdatarequest/currentoffset)
- [var requestsAllDataToEndOfResource: Bool](/documentation/avfoundation/avassetresourceloadingdatarequest/requestsalldatatoendofresource)
- [AVAssetResourceLoadingContentInformationRequest](/documentation/avfoundation/avassetresourceloadingcontentinformationrequest)

#### Configuring content information

- [var allowedContentTypes: [String]?](/documentation/avfoundation/avassetresourceloadingcontentinformationrequest/allowedcontenttypes)
- [var contentType: String?](/documentation/avfoundation/avassetresourceloadingcontentinformationrequest/contenttype)
- [var contentLength: Int64](/documentation/avfoundation/avassetresourceloadingcontentinformationrequest/contentlength)
- [var isByteRangeAccessSupported: Bool](/documentation/avfoundation/avassetresourceloadingcontentinformationrequest/isbyterangeaccesssupported)
- [var renewalDate: Date?](/documentation/avfoundation/avassetresourceloadingcontentinformationrequest/renewaldate)
- [var isEntireLengthAvailableOnDemand: Bool](/documentation/avfoundation/avassetresourceloadingcontentinformationrequest/isentirelengthavailableondemand)

### FairPlay streaming

- [AVContentKeySession](/documentation/avfoundation/avcontentkeysession)

#### Creating a session

- [convenience init(keySystem: AVContentKeySystem)](/documentation/avfoundation/avcontentkeysession/init(keysystem:))
- [convenience init(keySystem: AVContentKeySystem, storageDirectoryAt: URL)](/documentation/avfoundation/avcontentkeysession/init(keysystem:storagedirectoryat:))

#### Inspecting the session

- [var keySystem: AVContentKeySystem](/documentation/avfoundation/avcontentkeysession/keysystem)
- [AVContentKeySystem](/documentation/avfoundation/avcontentkeysystem)

##### Key-delivery methods

- [static let fairPlayStreaming: AVContentKeySystem](/documentation/avfoundation/avcontentkeysystem/fairplaystreaming)
- [static let clearKey: AVContentKeySystem](/documentation/avfoundation/avcontentkeysystem/clearkey)
- [static let authorizationToken: AVContentKeySystem](/documentation/avfoundation/avcontentkeysystem/authorizationtoken)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcontentkeysystem/init(rawvalue:))
- [var storageURL: URL?](/documentation/avfoundation/avcontentkeysession/storageurl)

#### Managing the delegate object

- [func setDelegate((any AVContentKeySessionDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avcontentkeysession/setdelegate(_:queue:))
- [var delegate: (any AVContentKeySessionDelegate)?](/documentation/avfoundation/avcontentkeysession/delegate)
- [var delegateQueue: dispatch_queue_t?](/documentation/avfoundation/avcontentkeysession/delegatequeue)

#### Managing content key recipients

- [var contentKeyRecipients: [any AVContentKeyRecipient]](/documentation/avfoundation/avcontentkeysession/contentkeyrecipients)
- [AVContentKeyRecipient](/documentation/avfoundation/avcontentkeyrecipient)

##### Verifying decryption key requirements

- [var mayRequireContentKeysForMediaDataProcessing: Bool](/documentation/avfoundation/avcontentkeyrecipient/mayrequirecontentkeysformediadataprocessing)
- [func contentKeySession(AVContentKeySession, didProvide: AVContentKey)](/documentation/avfoundation/avcontentkeyrecipient/contentkeysession(_:didprovide:))
- [func addContentKeyRecipient(any AVContentKeyRecipient)](/documentation/avfoundation/avcontentkeysession/addcontentkeyrecipient(_:))
- [func removeContentKeyRecipient(any AVContentKeyRecipient)](/documentation/avfoundation/avcontentkeysession/removecontentkeyrecipient(_:))

#### Processing requests

- [func processContentKeyRequest(withIdentifier: (any Sendable)?, initializationData: Data?, options: [String : any Sendable]?)](/documentation/avfoundation/avcontentkeysession/processcontentkeyrequest(withidentifier:initializationdata:options:))

#### Managing expiration

- [func expire()](/documentation/avfoundation/avcontentkeysession/expire())
- [func makeSecureTokenForExpirationDate(ofPersistableContentKey: Data, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/avfoundation/avcontentkeysession/makesecuretokenforexpirationdate(ofpersistablecontentkey:completionhandler:))
- [func renewExpiringResponseData(for: AVContentKeyRequest)](/documentation/avfoundation/avcontentkeysession/renewexpiringresponsedata(for:))
- [var contentProtectionSessionIdentifier: Data?](/documentation/avfoundation/avcontentkeysession/contentprotectionsessionidentifier)

#### Invalidating content keys

- [func invalidatePersistableContentKey(Data, options: [AVContentKeySessionServerPlaybackContextOption : Any]?, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/avfoundation/avcontentkeysession/invalidatepersistablecontentkey(_:options:completionhandler:))
- [func invalidateAllPersistableContentKeys(forApp: Data, options: [AVContentKeySessionServerPlaybackContextOption : Any]?, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/avfoundation/avcontentkeysession/invalidateallpersistablecontentkeys(forapp:options:completionhandler:))
- [AVContentKeySessionServerPlaybackContextOption](/documentation/avfoundation/avcontentkeysessionserverplaybackcontextoption)

##### Server playback context options

- [static let protocolVersions: AVContentKeySessionServerPlaybackContextOption](/documentation/avfoundation/avcontentkeysessionserverplaybackcontextoption/protocolversions)
- [static let serverChallenge: AVContentKeySessionServerPlaybackContextOption](/documentation/avfoundation/avcontentkeysessionserverplaybackcontextoption/serverchallenge)

##### Initializing an options structure

- [init(rawValue: String)](/documentation/avfoundation/avcontentkeysessionserverplaybackcontextoption/init(rawvalue:))

#### Handling expired session reports

- [class func pendingExpiredSessionReports(withAppIdentifier: Data, storageDirectoryAt: URL) -> [Data]](/documentation/avfoundation/avcontentkeysession/pendingexpiredsessionreports(withappidentifier:storagedirectoryat:))
- [class func removePendingExpiredSessionReports([Data], withAppIdentifier: Data, storageDirectoryAt: URL)](/documentation/avfoundation/avcontentkeysession/removependingexpiredsessionreports(_:withappidentifier:storagedirectoryat:))
- [AVContentKeySessionDelegate](/documentation/avfoundation/avcontentkeysessiondelegate)

#### Providing new content key requests

- [func contentKeySession(AVContentKeySession, didProvide: AVContentKeyRequest)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:didprovide:)-3coq5)
- [func contentKeySession(AVContentKeySession, didProvideRenewingContentKeyRequest: AVContentKeyRequest)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:didproviderenewingcontentkeyrequest:))
- [func contentKeySession(AVContentKeySession, didProvide: AVPersistableContentKeyRequest)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:didprovide:)-2wdgz)

#### Updating and retrying content key requests

- [func contentKeySession(AVContentKeySession, didProvide: [AVContentKeyRequest], forInitializationData: Data?)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:didprovide:forinitializationdata:))
- [func contentKeySession(AVContentKeySession, externalProtectionStatusDidChangeFor: AVContentKey)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:externalprotectionstatusdidchangefor:))
- [func contentKeySession(AVContentKeySession, didUpdatePersistableContentKey: Data, forContentKeyIdentifier: Any)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:didupdatepersistablecontentkey:forcontentkeyidentifier:))
- [func contentKeySession(AVContentKeySession, shouldRetry: AVContentKeyRequest, reason: AVContentKeyRequest.RetryReason) -> Bool](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:shouldretry:reason:))
- [AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason)

##### Reasons for content key request retry

- [static let receivedObsoleteContentKey: AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason/receivedobsoletecontentkey)
- [static let receivedResponseWithExpiredLease: AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason/receivedresponsewithexpiredlease)
- [static let timedOut: AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason/timedout)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcontentkeyrequest/retryreason/init(rawvalue:))
- [func contentKeySessionContentProtectionSessionIdentifierDidChange(AVContentKeySession)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysessioncontentprotectionsessionidentifierdidchange(_:))
- [func contentKeySession(AVContentKeySession, contentKeyRequest: AVContentKeyRequest, didFailWithError: any Error)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:contentkeyrequest:didfailwitherror:))
- [func contentKeySession(AVContentKeySession, contentKeyRequestDidSucceed: AVContentKeyRequest)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysession(_:contentkeyrequestdidsucceed:))
- [func contentKeySessionDidGenerateExpiredSessionReport(AVContentKeySession)](/documentation/avfoundation/avcontentkeysessiondelegate/contentkeysessiondidgenerateexpiredsessionreport(_:))
- [AVContentKey](/documentation/avfoundation/avcontentkey)

#### Accessing the specifier

- [var contentKeySpecifier: AVContentKeySpecifier](/documentation/avfoundation/avcontentkey/contentkeyspecifier)

#### Inspecting protection status

- [var externalContentProtectionStatus: AVExternalContentProtectionStatus](/documentation/avfoundation/avcontentkey/externalcontentprotectionstatus)
- [func revoke()](/documentation/avfoundation/avcontentkey/revoke())
- [AVContentKeySpecifier](/documentation/avfoundation/avcontentkeyspecifier)

#### Creating a specifier

- [init(forKeySystem: AVContentKeySystem, identifier: Any, options: [String : Any])](/documentation/avfoundation/avcontentkeyspecifier/init(forkeysystem:identifier:options:))

#### Inspecting a specifier

- [var identifier: any Sendable](/documentation/avfoundation/avcontentkeyspecifier/identifier)
- [var keySystem: AVContentKeySystem](/documentation/avfoundation/avcontentkeyspecifier/keysystem)
- [var options: [String : any Sendable]](/documentation/avfoundation/avcontentkeyspecifier/options)
- [AVContentKeyRequest](/documentation/avfoundation/avcontentkeyrequest)

#### Getting content key request data

- [func makeStreamingContentKeyRequestData(forApp: Data, contentIdentifier: Data?, options: [String : Any]?, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/avfoundation/avcontentkeyrequest/makestreamingcontentkeyrequestdata(forapp:contentidentifier:options:completionhandler:))
- [let AVContentKeyRequestProtocolVersionsKey: String](/documentation/avfoundation/avcontentkeyrequestprotocolversionskey)
- [let AVContentKeyRequestRequiresValidationDataInSecureTokenKey: String](/documentation/avfoundation/avcontentkeyrequestrequiresvalidationdatainsecuretokenkey)
- [let AVContentKeyRequestRandomDeviceIdentifierSeedKey: String](/documentation/avfoundation/avcontentkeyrequestrandomdeviceidentifierseedkey)
- [let AVContentKeyRequestShouldRandomizeDeviceIdentifierKey: String](/documentation/avfoundation/avcontentkeyrequestshouldrandomizedeviceidentifierkey)

#### Responding to the content key request

- [func processContentKeyResponse(AVContentKeyResponse)](/documentation/avfoundation/avcontentkeyrequest/processcontentkeyresponse(_:))
- [func processContentKeyResponseError(any Error)](/documentation/avfoundation/avcontentkeyrequest/processcontentkeyresponseerror(_:))

#### Getting content key request properties

- [var identifier: (any Sendable)?](/documentation/avfoundation/avcontentkeyrequest/identifier)
- [var originatingRecipient: (any AVContentKeyRecipient)?](/documentation/avfoundation/avcontentkeyrequest/originatingrecipient)
- [var canProvidePersistableContentKey: Bool](/documentation/avfoundation/avcontentkeyrequest/canprovidepersistablecontentkey)
- [var error: (any Error)?](/documentation/avfoundation/avcontentkeyrequest/error)
- [var initializationData: Data?](/documentation/avfoundation/avcontentkeyrequest/initializationdata)
- [var renewsExpiringResponseData: Bool](/documentation/avfoundation/avcontentkeyrequest/renewsexpiringresponsedata)
- [var status: AVContentKeyRequest.Status](/documentation/avfoundation/avcontentkeyrequest/status-swift.property)
- [AVContentKeyRequest.Status](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum)

##### Request status

- [case cancelled](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum/cancelled)
- [case failed](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum/failed)
- [case receivedResponse](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum/receivedresponse)
- [case renewed](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum/renewed)
- [case requestingResponse](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum/requestingresponse)
- [case retried](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum/retried)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcontentkeyrequest/status-swift.enum/init(rawvalue:))

#### Inspecting a request

- [var contentKey: AVContentKey?](/documentation/avfoundation/avcontentkeyrequest/contentkey)
- [var contentKeySpecifier: AVContentKeySpecifier](/documentation/avfoundation/avcontentkeyrequest/contentkeyspecifier)
- [var options: [String : any Sendable]](/documentation/avfoundation/avcontentkeyrequest/options)
- [AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason)

##### Reasons for content key request retry

- [static let receivedObsoleteContentKey: AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason/receivedobsoletecontentkey)
- [static let receivedResponseWithExpiredLease: AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason/receivedresponsewithexpiredlease)
- [static let timedOut: AVContentKeyRequest.RetryReason](/documentation/avfoundation/avcontentkeyrequest/retryreason/timedout)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcontentkeyrequest/retryreason/init(rawvalue:))

#### Instance Methods

- [func respondByRequestingPersistableContentKeyRequest()](/documentation/avfoundation/avcontentkeyrequest/respondbyrequestingpersistablecontentkeyrequest()-1ci4q)
- [func respondByRequestingPersistableContentKeyRequestAndReturnError() throws](/documentation/avfoundation/avcontentkeyrequest/respondbyrequestingpersistablecontentkeyrequest()-7i2pw)
- [AVPersistableContentKeyRequest](/documentation/avfoundation/avpersistablecontentkeyrequest)

#### Requesting persistable content key data

- [func persistableContentKey(fromKeyVendorResponse: Data, options: [String : Any]?) throws -> Data](/documentation/avfoundation/avpersistablecontentkeyrequest/persistablecontentkey(fromkeyvendorresponse:options:))
- [AVContentKeyResponse](/documentation/avfoundation/avcontentkeyresponse)

#### Creating new content key responses

- [convenience init(clearKeyData: Data, initializationVector: Data?)](/documentation/avfoundation/avcontentkeyresponse/init(clearkeydata:initializationvector:))
- [convenience init(fairPlayStreamingKeyResponseData: Data)](/documentation/avfoundation/avcontentkeyresponse/init(fairplaystreamingkeyresponsedata:))
- [convenience init(authorizationTokenData: Data)](/documentation/avfoundation/avcontentkeyresponse/init(authorizationtokendata:))
- [AVExternalContentProtectionStatus](/documentation/avfoundation/avexternalcontentprotectionstatus)

#### Status values

- [case pending](/documentation/avfoundation/avexternalcontentprotectionstatus/pending)
- [case sufficient](/documentation/avfoundation/avexternalcontentprotectionstatus/sufficient)
- [case insufficient](/documentation/avfoundation/avexternalcontentprotectionstatus/insufficient)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avexternalcontentprotectionstatus/init(rawvalue:))
- [func AVSampleBufferAttachContentKey(CMSampleBuffer, AVContentKey, NSErrorPointer) -> Bool](/documentation/avfoundation/avsamplebufferattachcontentkey(_:_:_:))
- [Sample buffer playback](/documentation/avfoundation/sample-buffer-playback)

### Sample buffer generation

- [Playing custom audio with your own player](/documentation/avfaudio/playing-custom-audio-with-your-own-player)
- [AVSampleBufferRequest](/documentation/avfoundation/avsamplebufferrequest)

#### Creating a request

- [init(start: AVSampleCursor)](/documentation/avfoundation/avsamplebufferrequest/init(start:))

#### Configuring sample buffer request parameters

- [var direction: AVSampleBufferRequest.Direction](/documentation/avfoundation/avsamplebufferrequest/direction-swift.property)
- [AVSampleBufferRequest.Direction](/documentation/avfoundation/avsamplebufferrequest/direction-swift.enum)

##### Buffer direction

- [case forward](/documentation/avfoundation/avsamplebufferrequest/direction-swift.enum/forward)
- [case none](/documentation/avfoundation/avsamplebufferrequest/direction-swift.enum/none)
- [case reverse](/documentation/avfoundation/avsamplebufferrequest/direction-swift.enum/reverse)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avsamplebufferrequest/direction-swift.enum/init(rawvalue:))
- [var limitCursor: AVSampleCursor?](/documentation/avfoundation/avsamplebufferrequest/limitcursor)
- [var maxSampleCount: Int](/documentation/avfoundation/avsamplebufferrequest/maxsamplecount)
- [var mode: AVSampleBufferRequest.Mode](/documentation/avfoundation/avsamplebufferrequest/mode-swift.property)
- [AVSampleBufferRequest.Mode](/documentation/avfoundation/avsamplebufferrequest/mode-swift.enum)

##### Mode scheduling

- [case immediate](/documentation/avfoundation/avsamplebufferrequest/mode-swift.enum/immediate)
- [case scheduled](/documentation/avfoundation/avsamplebufferrequest/mode-swift.enum/scheduled)
- [case opportunistic](/documentation/avfoundation/avsamplebufferrequest/mode-swift.enum/opportunistic)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avsamplebufferrequest/mode-swift.enum/init(rawvalue:))
- [var overrideTime: CMTime](/documentation/avfoundation/avsamplebufferrequest/overridetime)
- [var preferredMinSampleCount: Int](/documentation/avfoundation/avsamplebufferrequest/preferredminsamplecount)
- [var startCursor: AVSampleCursor](/documentation/avfoundation/avsamplebufferrequest/startcursor)
- [AVSampleBufferGenerator](/documentation/avfoundation/avsamplebuffergenerator)

#### Creating sample buffer generators

- [init(asset: AVAsset, timebase: CMTimebase?)](/documentation/avfoundation/avsamplebuffergenerator/init(asset:timebase:))

#### Creating a sample buffer

- [func makeSampleBuffer(for: AVSampleBufferRequest) throws -> sending CMSampleBuffer](/documentation/avfoundation/avsamplebuffergenerator/makesamplebuffer(for:))
- [func makeBatch() -> AVSampleBufferGeneratorBatch](/documentation/avfoundation/avsamplebuffergenerator/makebatch())
- [func makeSampleBuffer(for: AVSampleBufferRequest, addTo: AVSampleBufferGeneratorBatch) throws -> CMSampleBuffer](/documentation/avfoundation/avsamplebuffergenerator/makesamplebuffer(for:addto:))
- [func createSampleBuffer(for: AVSampleBufferRequest) -> CMSampleBuffer?](/documentation/avfoundation/avsamplebuffergenerator/createsamplebuffer(for:))

#### Retrieving sample buffer data

- [class func notifyOfDataReady(for: CMSampleBuffer, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/avfoundation/avsamplebuffergenerator/notifyofdataready(for:completionhandler:))
- [AVSampleBufferGeneratorBatch](/documentation/avfoundation/avsamplebuffergeneratorbatch)

#### Preparing a batch

- [func makeDataReady(completionHandler: ((any Error)?) -> Void)](/documentation/avfoundation/avsamplebuffergeneratorbatch/makedataready(completionhandler:))

#### Canceling a batch

- [func cancel()](/documentation/avfoundation/avsamplebuffergeneratorbatch/cancel())

### Presentation

- [AVQueuedSampleBufferRendering](/documentation/avfoundation/avqueuedsamplebufferrendering)

#### Requesting media

- [var isReadyForMoreMediaData: Bool](/documentation/avfoundation/avqueuedsamplebufferrendering/isreadyformoremediadata)
- [func enqueue(CMSampleBuffer)](/documentation/avfoundation/avqueuedsamplebufferrendering/enqueue(_:))
- [func requestMediaDataWhenReady(on: dispatch_queue_t, using: () -> Void)](/documentation/avfoundation/avqueuedsamplebufferrendering/requestmediadatawhenready(on:using:))
- [func stopRequestingMediaData()](/documentation/avfoundation/avqueuedsamplebufferrendering/stoprequestingmediadata())

#### Determining playback readiness

- [var hasSufficientMediaDataForReliablePlaybackStart: Bool](/documentation/avfoundation/avqueuedsamplebufferrendering/hassufficientmediadataforreliableplaybackstart)

#### Clearing queued sample buffers

- [func flush()](/documentation/avfoundation/avqueuedsamplebufferrendering/flush())

#### Indentifying the timebase

- [var timebase: CMTimebase](/documentation/avfoundation/avqueuedsamplebufferrendering/timebase)
- [AVSampleBufferRenderSynchronizer](/documentation/avfoundation/avsamplebufferrendersynchronizer)

#### Managing renderers

- [var renderers: [any AVQueuedSampleBufferRendering]](/documentation/avfoundation/avsamplebufferrendersynchronizer/renderers)
- [func addRenderer(any AVQueuedSampleBufferRendering)](/documentation/avfoundation/avsamplebufferrendersynchronizer/addrenderer(_:))
- [func removeRenderer(any AVQueuedSampleBufferRendering, at: CMTime, completionHandler: ((Bool) -> Void)?)](/documentation/avfoundation/avsamplebufferrendersynchronizer/removerenderer(_:at:completionhandler:))

#### Accessing time information

- [func currentTime() -> CMTime](/documentation/avfoundation/avsamplebufferrendersynchronizer/currenttime())
- [var timebase: CMTimebase](/documentation/avfoundation/avsamplebufferrendersynchronizer/timebase)
- [var rate: Float](/documentation/avfoundation/avsamplebufferrendersynchronizer/rate)
- [func setRate(Float, time: CMTime)](/documentation/avfoundation/avsamplebufferrendersynchronizer/setrate(_:time:))
- [func setRate(Float, time: CMTime, atHostTime: CMTime)](/documentation/avfoundation/avsamplebufferrendersynchronizer/setrate(_:time:athosttime:))
- [class let rateDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avsamplebufferrendersynchronizer/ratedidchangenotification)
- [var delaysRateChangeUntilHasSufficientMediaData: Bool](/documentation/avfoundation/avsamplebufferrendersynchronizer/delaysratechangeuntilhassufficientmediadata)

#### Observing time

- [func addPeriodicTimeObserver(forInterval: CMTime, queue: dispatch_queue_t?, using: (CMTime) -> Void) -> Any](/documentation/avfoundation/avsamplebufferrendersynchronizer/addperiodictimeobserver(forinterval:queue:using:))
- [func addBoundaryTimeObserver(forTimes: [NSValue], queue: dispatch_queue_t?, using: () -> Void) -> Any](/documentation/avfoundation/avsamplebufferrendersynchronizer/addboundarytimeobserver(fortimes:queue:using:))
- [func removeTimeObserver(Any)](/documentation/avfoundation/avsamplebufferrendersynchronizer/removetimeobserver(_:))

#### Configuring audio behavior

- [var intendedSpatialAudioExperience: any SpatialAudioExperience](/documentation/avfoundation/avsamplebufferrendersynchronizer/intendedspatialaudioexperience-3z7d3)
- [AVSampleBufferDisplayLayer](/documentation/avfoundation/avsamplebufferdisplaylayer)

#### Accessing the video renderer

- [var sampleBufferRenderer: AVSampleBufferVideoRenderer](/documentation/avfoundation/avsamplebufferdisplaylayer/samplebufferrenderer)

#### Configuring the layer

- [var isReadyForDisplay: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/isreadyfordisplay)
- [var controlTimebase: CMTimebase?](/documentation/avfoundation/avsamplebufferdisplaylayer/controltimebase)
- [var videoGravity: AVLayerVideoGravity](/documentation/avfoundation/avsamplebufferdisplaylayer/videogravity)
- [AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity)

##### Video gravities

- [static let resize: AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity/resize)
- [static let resizeAspect: AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity/resizeaspect)
- [static let resizeAspectFill: AVLayerVideoGravity](/documentation/avfoundation/avlayervideogravity/resizeaspectfill)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avlayervideogravity/init(rawvalue:))

#### Protecting content

- [var preventsCapture: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/preventscapture)
- [var isOutputObscuredDueToInsufficientExternalProtection: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/isoutputobscuredduetoinsufficientexternalprotection)

#### Preventing backgrounding

- [var preventsDisplaySleepDuringVideoPlayback: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/preventsdisplaysleepduringvideoplayback)
- [var preventsAutomaticBackgroundingDuringVideoPlayback: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/preventsautomaticbackgroundingduringvideoplayback)

#### Handling errors

- [static let AVSampleBufferDisplayLayerFailedToDecode: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/avsamplebufferdisplaylayerfailedtodecode)
- [let AVSampleBufferDisplayLayerFailedToDecodeNotificationErrorKey: String](/documentation/avfoundation/avsamplebufferdisplaylayerfailedtodecodenotificationerrorkey)

#### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avsamplebufferdisplaylayer-deprecated-symbols)

##### Initiating media data requests

- [func requestMediaDataWhenReady(on: dispatch_queue_t, using: () -> Void)](/documentation/avfoundation/avsamplebufferdisplaylayer/requestmediadatawhenready(on:using:))
- [var isReadyForMoreMediaData: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/isreadyformoremediadata)
- [var requiresFlushToResumeDecoding: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/requiresflushtoresumedecoding)
- [func stopRequestingMediaData()](/documentation/avfoundation/avsamplebufferdisplaylayer/stoprequestingmediadata())
- [var hasSufficientMediaDataForReliablePlaybackStart: Bool](/documentation/avfoundation/avsamplebufferdisplaylayer/hassufficientmediadataforreliableplaybackstart)

##### Flushing sample buffers

- [func flush()](/documentation/avfoundation/avsamplebufferdisplaylayer/flush())
- [func flushAndRemoveImage()](/documentation/avfoundation/avsamplebufferdisplaylayer/flushandremoveimage())

##### Configuring the timebase

- [var timebase: CMTimebase](/documentation/avfoundation/avsamplebufferdisplaylayer/timebase)

##### Enqueuing the sample buffer

- [func enqueue(CMSampleBuffer)](/documentation/avfoundation/avsamplebufferdisplaylayer/enqueue(_:))

##### Getting display layer settings

- [var status: AVQueuedSampleBufferRenderingStatus](/documentation/avfoundation/avsamplebufferdisplaylayer/status)
- [AVQueuedSampleBufferRenderingStatus](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus)

###### Status values

- [case unknown](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/unknown)
- [case rendering](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/rendering)
- [case failed](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/failed)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/init(rawvalue:))

##### Handling errors

- [var error: (any Error)?](/documentation/avfoundation/avsamplebufferdisplaylayer/error)
- [AVSampleBufferVideoRenderer](/documentation/avfoundation/avsamplebuffervideorenderer)

#### Flushing the renderer

- [var requiresFlushToResumeDecoding: Bool](/documentation/avfoundation/avsamplebuffervideorenderer/requiresflushtoresumedecoding)
- [class let requiresFlushToResumeDecodingDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avsamplebuffervideorenderer/requiresflushtoresumedecodingdidchangenotification)
- [func flush(removingDisplayedImage: Bool, completionHandler: (() -> Void)?)](/documentation/avfoundation/avsamplebuffervideorenderer/flush(removingdisplayedimage:completionhandler:))

#### Setting presentation time expectations

- [var presentationTimeExpectation: AVSampleBufferVideoRenderer.PresentationTimeExpectation](/documentation/avfoundation/avsamplebuffervideorenderer/presentationtimeexpectation-swift.property)
- [AVSampleBufferVideoRenderer.PresentationTimeExpectation](/documentation/avfoundation/avsamplebuffervideorenderer/presentationtimeexpectation-swift.enum)

##### Expectations

- [case minimumUpcoming(CMTime)](/documentation/avfoundation/avsamplebuffervideorenderer/presentationtimeexpectation-swift.enum/minimumupcoming(_:))
- [case monotonicallyIncreasing](/documentation/avfoundation/avsamplebuffervideorenderer/presentationtimeexpectation-swift.enum/monotonicallyincreasing)
- [case none](/documentation/avfoundation/avsamplebuffervideorenderer/presentationtimeexpectation-swift.enum/none)

#### Inspecting the status

- [var status: AVQueuedSampleBufferRenderingStatus](/documentation/avfoundation/avsamplebuffervideorenderer/status)
- [var error: (any Error)?](/documentation/avfoundation/avsamplebuffervideorenderer/error)

#### Accessing the pixel buffer

- [func displayedPixelBuffer() -> CVPixelBuffer?](/documentation/avfoundation/avsamplebuffervideorenderer/displayedpixelbuffer())
- [var recommendedPixelBufferAttributes: CVPixelBufferAttributes](/documentation/avfoundation/avsamplebuffervideorenderer/recommendedpixelbufferattributes-6zrqb)

#### Handling decode failures

- [class let didFailToDecodeNotification: NSNotification.Name](/documentation/avfoundation/avsamplebuffervideorenderer/didfailtodecodenotification)
- [class let didFailToDecodeNotificationErrorKey: String](/documentation/avfoundation/avsamplebuffervideorenderer/didfailtodecodenotificationerrorkey)

#### Capturing performance metrics

- [func loadVideoPerformanceMetrics(completionHandler: (AVVideoPerformanceMetrics?) -> Void)](/documentation/avfoundation/avsamplebuffervideorenderer/loadvideoperformancemetrics(completionhandler:))
- [AVSampleBufferAudioRenderer](/documentation/avfoundation/avsamplebufferaudiorenderer)

#### Determining rendering status

- [var status: AVQueuedSampleBufferRenderingStatus](/documentation/avfoundation/avsamplebufferaudiorenderer/status)
- [AVQueuedSampleBufferRenderingStatus](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus)

##### Status values

- [case unknown](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/unknown)
- [case rendering](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/rendering)
- [case failed](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avqueuedsamplebufferrenderingstatus/init(rawvalue:))

#### Removing queued buffers

- [func flush(fromSourceTime: CMTime, completionHandler: (Bool) -> Void)](/documentation/avfoundation/avsamplebufferaudiorenderer/flush(fromsourcetime:completionhandler:))
- [let AVSampleBufferAudioRendererFlushTimeKey: String](/documentation/avfoundation/avsamplebufferaudiorendererflushtimekey)

#### Configuring time and pitch

- [var audioTimePitchAlgorithm: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avsamplebufferaudiorenderer/audiotimepitchalgorithm)
- [AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm)

##### Type properties

- [static let lowQualityZeroLatency: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/lowqualityzerolatency)
- [static let spectral: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/spectral)
- [static let timeDomain: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/timedomain)
- [static let varispeed: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/varispeed)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avaudiotimepitchalgorithm/init(rawvalue:))

#### Configuring audio spatialization

- [var allowedAudioSpatializationFormats: AVAudioSpatializationFormats](/documentation/avfoundation/avsamplebufferaudiorenderer/allowedaudiospatializationformats)

#### Managing audio output

- [var volume: Float](/documentation/avfoundation/avsamplebufferaudiorenderer/volume)
- [var isMuted: Bool](/documentation/avfoundation/avsamplebufferaudiorenderer/ismuted)
- [var audioOutputDeviceUniqueID: String?](/documentation/avfoundation/avsamplebufferaudiorenderer/audiooutputdeviceuniqueid)

#### Responding to errors

- [var error: (any Error)?](/documentation/avfoundation/avsamplebufferaudiorenderer/error)

## Capture

- [Capture setup](/documentation/avfoundation/capture-setup)

### Essentials

- [Requesting authorization to capture and save media](/documentation/avfoundation/requesting-authorization-to-capture-and-save-media)

### Capture sessions

- [Setting up a capture session](/documentation/avfoundation/setting-up-a-capture-session)
- [Accessing the camera while multitasking on iPad](/documentation/avkit/accessing-the-camera-while-multitasking-on-ipad)
- [AVCam: Building a camera app](/documentation/avfoundation/avcam-building-a-camera-app)
- [Capturing Cinematic video](/documentation/avfoundation/capturing-cinematic-video)
- [AVMultiCamPiP: Capturing from Multiple Cameras](/documentation/avfoundation/avmulticampip-capturing-from-multiple-cameras)
- [AVCamBarcode: detecting barcodes and faces](/documentation/avfoundation/avcambarcode-detecting-barcodes-and-faces)
- [AVCaptureSession](/documentation/avfoundation/avcapturesession)

#### Configuring a session

- [func beginConfiguration()](/documentation/avfoundation/avcapturesession/beginconfiguration())
- [func commitConfiguration()](/documentation/avfoundation/avcapturesession/commitconfiguration())

#### Setting a session preset

- [AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset)

##### Quality levels

- [static let high: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/high)
- [static let medium: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/medium)
- [static let low: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/low)

##### Photo

- [static let photo: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/photo)

##### Manual configuration

- [static let inputPriority: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/inputpriority)

##### High definition

- [static let qHD960x540: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/qhd960x540)
- [static let hd1280x720: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/hd1280x720)
- [static let hd1920x1080: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/hd1920x1080)
- [static let hd4K3840x2160: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/hd4k3840x2160)

##### VGA

- [static let qvga320x240: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/qvga320x240)
- [static let vga640x480: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/vga640x480)

##### iFrame

- [static let iFrame960x540: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/iframe960x540)
- [static let iFrame1280x720: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/iframe1280x720)

##### CIF

- [static let cif352x288: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/preset/cif352x288)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcapturesession/preset/init(rawvalue:))
- [func canSetSessionPreset(AVCaptureSession.Preset) -> Bool](/documentation/avfoundation/avcapturesession/cansetsessionpreset(_:))
- [var sessionPreset: AVCaptureSession.Preset](/documentation/avfoundation/avcapturesession/sessionpreset)

#### Configuring inputs

- [var inputs: [AVCaptureInput]](/documentation/avfoundation/avcapturesession/inputs)
- [func canAddInput(AVCaptureInput) -> Bool](/documentation/avfoundation/avcapturesession/canaddinput(_:))
- [func addInput(AVCaptureInput)](/documentation/avfoundation/avcapturesession/addinput(_:))
- [func removeInput(AVCaptureInput)](/documentation/avfoundation/avcapturesession/removeinput(_:))

#### Configuring outputs

- [var outputs: [AVCaptureOutput]](/documentation/avfoundation/avcapturesession/outputs)
- [func canAddOutput(AVCaptureOutput) -> Bool](/documentation/avfoundation/avcapturesession/canaddoutput(_:))
- [func addOutput(AVCaptureOutput)](/documentation/avfoundation/avcapturesession/addoutput(_:))
- [func removeOutput(AVCaptureOutput)](/documentation/avfoundation/avcapturesession/removeoutput(_:))

#### Connecting inputs and outputs

- [var connections: [AVCaptureConnection]](/documentation/avfoundation/avcapturesession/connections)
- [func addConnection(AVCaptureConnection)](/documentation/avfoundation/avcapturesession/addconnection(_:))
- [func canAddConnection(AVCaptureConnection) -> Bool](/documentation/avfoundation/avcapturesession/canaddconnection(_:))
- [func addInputWithNoConnections(AVCaptureInput)](/documentation/avfoundation/avcapturesession/addinputwithnoconnections(_:))
- [func addOutputWithNoConnections(AVCaptureOutput)](/documentation/avfoundation/avcapturesession/addoutputwithnoconnections(_:))
- [func removeConnection(AVCaptureConnection)](/documentation/avfoundation/avcapturesession/removeconnection(_:))
- [AVCaptureAudioChannel](/documentation/avfoundation/avcaptureaudiochannel)

##### Configuring a channel

- [var isEnabled: Bool](/documentation/avfoundation/avcaptureaudiochannel/isenabled)
- [var volume: Float](/documentation/avfoundation/avcaptureaudiochannel/volume)

##### Accessing power levels

- [var averagePowerLevel: Float](/documentation/avfoundation/avcaptureaudiochannel/averagepowerlevel)
- [var peakHoldLevel: Float](/documentation/avfoundation/avcaptureaudiochannel/peakholdlevel)

#### Configuring deferred start

- [var isManualDeferredStartSupported: Bool](/documentation/avfoundation/avcapturesession/ismanualdeferredstartsupported)
- [var automaticallyRunsDeferredStart: Bool](/documentation/avfoundation/avcapturesession/automaticallyrunsdeferredstart)
- [func runDeferredStartWhenNeeded()](/documentation/avfoundation/avcapturesession/rundeferredstartwhenneeded())
- [var deferredStartDelegate: (any AVCaptureSessionDeferredStartDelegate)?](/documentation/avfoundation/avcapturesession/deferredstartdelegate)
- [var deferredStartDelegateCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcapturesession/deferredstartdelegatecallbackqueue)
- [func setDeferredStartDelegate((any AVCaptureSessionDeferredStartDelegate)?, deferredStartDelegateCallbackQueue: dispatch_queue_t?)](/documentation/avfoundation/avcapturesession/setdeferredstartdelegate(_:deferredstartdelegatecallbackqueue:))
- [AVCaptureSessionDeferredStartDelegate](/documentation/avfoundation/avcapturesessiondeferredstartdelegate)

##### Responding to deferred start events

- [func sessionDidRunDeferredStart(AVCaptureSession)](/documentation/avfoundation/avcapturesessiondeferredstartdelegate/sessiondidrundeferredstart(_:))
- [func sessionWillRunDeferredStart(AVCaptureSession)](/documentation/avfoundation/avcapturesessiondeferredstartdelegate/sessionwillrundeferredstart(_:))

#### Configuring capture controls

- [var supportsControls: Bool](/documentation/avfoundation/avcapturesession/supportscontrols)
- [var maxControlsCount: Int](/documentation/avfoundation/avcapturesession/maxcontrolscount)
- [var controls: [AVCaptureControl]](/documentation/avfoundation/avcapturesession/controls)
- [func canAddControl(AVCaptureControl) -> Bool](/documentation/avfoundation/avcapturesession/canaddcontrol(_:))
- [func addControl(AVCaptureControl)](/documentation/avfoundation/avcapturesession/addcontrol(_:))
- [func removeControl(AVCaptureControl)](/documentation/avfoundation/avcapturesession/removecontrol(_:))
- [func setControlsDelegate((any AVCaptureSessionControlsDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avcapturesession/setcontrolsdelegate(_:queue:))
- [AVCaptureSessionControlsDelegate](/documentation/avfoundation/avcapturesessioncontrolsdelegate)

##### Responding to control events

- [func sessionControlsDidBecomeActive(AVCaptureSession)](/documentation/avfoundation/avcapturesessioncontrolsdelegate/sessioncontrolsdidbecomeactive(_:))
- [func sessionControlsWillEnterFullscreenAppearance(AVCaptureSession)](/documentation/avfoundation/avcapturesessioncontrolsdelegate/sessioncontrolswillenterfullscreenappearance(_:))
- [func sessionControlsWillExitFullscreenAppearance(AVCaptureSession)](/documentation/avfoundation/avcapturesessioncontrolsdelegate/sessioncontrolswillexitfullscreenappearance(_:))
- [func sessionControlsDidBecomeInactive(AVCaptureSession)](/documentation/avfoundation/avcapturesessioncontrolsdelegate/sessioncontrolsdidbecomeinactive(_:))
- [var controlsDelegate: (any AVCaptureSessionControlsDelegate)?](/documentation/avfoundation/avcapturesession/controlsdelegate)
- [var controlsDelegateCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcapturesession/controlsdelegatecallbackqueue)

#### Managing the session life cycle

- [func startRunning()](/documentation/avfoundation/avcapturesession/startrunning())
- [func stopRunning()](/documentation/avfoundation/avcapturesession/stoprunning())

#### Observing session state

- [var isRunning: Bool](/documentation/avfoundation/avcapturesession/isrunning)
- [var isInterrupted: Bool](/documentation/avfoundation/avcapturesession/isinterrupted)
- [class let didStartRunningNotification: NSNotification.Name](/documentation/avfoundation/avcapturesession/didstartrunningnotification)
- [class let didStopRunningNotification: NSNotification.Name](/documentation/avfoundation/avcapturesession/didstoprunningnotification)
- [class let wasInterruptedNotification: NSNotification.Name](/documentation/avfoundation/avcapturesession/wasinterruptednotification)

##### User-infomation keys

- [let AVCaptureSessionInterruptionSystemPressureStateKey: String](/documentation/avfoundation/avcapturesessioninterruptionsystempressurestatekey)
- [let AVCaptureSessionInterruptionReasonKey: String](/documentation/avfoundation/avcapturesessioninterruptionreasonkey)
- [AVCaptureSession.InterruptionReason](/documentation/avfoundation/avcapturesession/interruptionreason)

###### Constants

- [case videoDeviceNotAvailableInBackground](/documentation/avfoundation/avcapturesession/interruptionreason/videodevicenotavailableinbackground)
- [case audioDeviceInUseByAnotherClient](/documentation/avfoundation/avcapturesession/interruptionreason/audiodeviceinusebyanotherclient)
- [case videoDeviceInUseByAnotherClient](/documentation/avfoundation/avcapturesession/interruptionreason/videodeviceinusebyanotherclient)
- [case videoDeviceNotAvailableWithMultipleForegroundApps](/documentation/avfoundation/avcapturesession/interruptionreason/videodevicenotavailablewithmultipleforegroundapps)
- [case videoDeviceNotAvailableDueToSystemPressure](/documentation/avfoundation/avcapturesession/interruptionreason/videodevicenotavailableduetosystempressure)
- [case sensitiveContentMitigationActivated](/documentation/avfoundation/avcapturesession/interruptionreason/sensitivecontentmitigationactivated)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturesession/interruptionreason/init(rawvalue:))
- [class let interruptionEndedNotification: NSNotification.Name](/documentation/avfoundation/avcapturesession/interruptionendednotification)
- [class let runtimeErrorNotification: NSNotification.Name](/documentation/avfoundation/avcapturesession/runtimeerrornotification)

##### User info keys

- [let AVCaptureSessionErrorKey: String](/documentation/avfoundation/avcapturesessionerrorkey)

#### Configuring multitasking

- [var isMultitaskingCameraAccessSupported: Bool](/documentation/avfoundation/avcapturesession/ismultitaskingcameraaccesssupported)
- [var isMultitaskingCameraAccessEnabled: Bool](/documentation/avfoundation/avcapturesession/ismultitaskingcameraaccessenabled)

#### Monitoring performance

- [var hardwareCost: Float](/documentation/avfoundation/avcapturesession/hardwarecost)

#### Configuring the app’s audio session

- [var usesApplicationAudioSession: Bool](/documentation/avfoundation/avcapturesession/usesapplicationaudiosession)
- [var automaticallyConfiguresApplicationAudioSession: Bool](/documentation/avfoundation/avcapturesession/automaticallyconfiguresapplicationaudiosession)
- [var configuresApplicationAudioSessionToMixWithOthers: Bool](/documentation/avfoundation/avcapturesession/configuresapplicationaudiosessiontomixwithothers)
- [var configuresApplicationAudioSessionForBluetoothHighQualityRecording: Bool](/documentation/avfoundation/avcapturesession/configuresapplicationaudiosessionforbluetoothhighqualityrecording)

#### Managing color spaces

- [var automaticallyConfiguresCaptureDeviceForWideColor: Bool](/documentation/avfoundation/avcapturesession/automaticallyconfigurescapturedeviceforwidecolor)

#### Synchronizing output

- [var synchronizationClock: CMClock?](/documentation/avfoundation/avcapturesession/synchronizationclock)
- [var masterClock: CMClock?](/documentation/avfoundation/avcapturesession/masterclock)
- [AVCaptureMultiCamSession](/documentation/avfoundation/avcapturemulticamsession)

#### Determining multi-camera support

- [class var isMultiCamSupported: Bool](/documentation/avfoundation/avcapturemulticamsession/ismulticamsupported)

#### Managing resources

- [var hardwareCost: Float](/documentation/avfoundation/avcapturemulticamsession/hardwarecost)
- [var systemPressureCost: Float](/documentation/avfoundation/avcapturemulticamsession/systempressurecost)
- [AVCaptureInput](/documentation/avfoundation/avcaptureinput)

#### Accessing ports

- [var ports: [AVCaptureInput.Port]](/documentation/avfoundation/avcaptureinput/ports)
- [AVCaptureInput.Port](/documentation/avfoundation/avcaptureinput/port)

##### Inspecting an input port

- [var isEnabled: Bool](/documentation/avfoundation/avcaptureinput/port/isenabled)
- [var mediaType: AVMediaType](/documentation/avfoundation/avcaptureinput/port/mediatype)
- [var formatDescription: CMFormatDescription?](/documentation/avfoundation/avcaptureinput/port/formatdescription)
- [var sourceDeviceType: AVCaptureDevice.DeviceType?](/documentation/avfoundation/avcaptureinput/port/sourcedevicetype)
- [var sourceDevicePosition: AVCaptureDevice.Position](/documentation/avfoundation/avcaptureinput/port/sourcedeviceposition)
- [var clock: CMClock?](/documentation/avfoundation/avcaptureinput/port/clock)

##### Observing format changes

- [class let formatDescriptionDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avcaptureinput/port/formatdescriptiondidchangenotification)

##### Accessing the input

- [var input: AVCaptureInput](/documentation/avfoundation/avcaptureinput/port/input)
- [AVCaptureOutput](/documentation/avfoundation/avcaptureoutput)

#### Accessing connections

- [var connections: [AVCaptureConnection]](/documentation/avfoundation/avcaptureoutput/connections)
- [func connection(with: AVMediaType) -> AVCaptureConnection?](/documentation/avfoundation/avcaptureoutput/connection(with:))
- [AVCaptureOutput.DataDroppedReason](/documentation/avfoundation/avcaptureoutput/datadroppedreason)

##### Reasons

- [case none](/documentation/avfoundation/avcaptureoutput/datadroppedreason/none)
- [case lateData](/documentation/avfoundation/avcaptureoutput/datadroppedreason/latedata)
- [case outOfBuffers](/documentation/avfoundation/avcaptureoutput/datadroppedreason/outofbuffers)
- [case discontinuity](/documentation/avfoundation/avcaptureoutput/datadroppedreason/discontinuity)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptureoutput/datadroppedreason/init(rawvalue:))

#### Managing deferred start

- [var isDeferredStartEnabled: Bool](/documentation/avfoundation/avcaptureoutput/isdeferredstartenabled)
- [var isDeferredStartSupported: Bool](/documentation/avfoundation/avcaptureoutput/isdeferredstartsupported)

#### Converting between coordinate systems

- [func transformedMetadataObject(for: AVMetadataObject, connection: AVCaptureConnection) -> AVMetadataObject?](/documentation/avfoundation/avcaptureoutput/transformedmetadataobject(for:connection:))
- [func metadataOutputRectConverted(fromOutputRect: CGRect) -> CGRect](/documentation/avfoundation/avcaptureoutput/metadataoutputrectconverted(fromoutputrect:))
- [func outputRectConverted(fromMetadataOutputRect: CGRect) -> CGRect](/documentation/avfoundation/avcaptureoutput/outputrectconverted(frommetadataoutputrect:))
- [AVCaptureConnection](/documentation/avfoundation/avcaptureconnection)

#### Creating a connection

- [init(inputPorts: [AVCaptureInput.Port], output: AVCaptureOutput)](/documentation/avfoundation/avcaptureconnection/init(inputports:output:))
- [init(inputPort: AVCaptureInput.Port, videoPreviewLayer: AVCaptureVideoPreviewLayer)](/documentation/avfoundation/avcaptureconnection/init(inputport:videopreviewlayer:))

#### Enabling a connection

- [var isEnabled: Bool](/documentation/avfoundation/avcaptureconnection/isenabled)
- [var isActive: Bool](/documentation/avfoundation/avcaptureconnection/isactive)

#### Inspecting a connection

- [var inputPorts: [AVCaptureInput.Port]](/documentation/avfoundation/avcaptureconnection/inputports)
- [var output: AVCaptureOutput?](/documentation/avfoundation/avcaptureconnection/output)
- [var videoPreviewLayer: AVCaptureVideoPreviewLayer?](/documentation/avfoundation/avcaptureconnection/videopreviewlayer)
- [var audioChannels: [AVCaptureAudioChannel]](/documentation/avfoundation/avcaptureconnection/audiochannels)

#### Rotating a video

- [func isVideoRotationAngleSupported(CGFloat) -> Bool](/documentation/avfoundation/avcaptureconnection/isvideorotationanglesupported(_:))
- [var videoRotationAngle: CGFloat](/documentation/avfoundation/avcaptureconnection/videorotationangle)

#### Mirroring a video

- [var isVideoMirroringSupported: Bool](/documentation/avfoundation/avcaptureconnection/isvideomirroringsupported)
- [var isVideoMirrored: Bool](/documentation/avfoundation/avcaptureconnection/isvideomirrored)
- [var automaticallyAdjustsVideoMirroring: Bool](/documentation/avfoundation/avcaptureconnection/automaticallyadjustsvideomirroring)

#### Stabilizing video

- [var isVideoStabilizationSupported: Bool](/documentation/avfoundation/avcaptureconnection/isvideostabilizationsupported)
- [var activeVideoStabilizationMode: AVCaptureVideoStabilizationMode](/documentation/avfoundation/avcaptureconnection/activevideostabilizationmode)
- [var preferredVideoStabilizationMode: AVCaptureVideoStabilizationMode](/documentation/avfoundation/avcaptureconnection/preferredvideostabilizationmode)

#### Delivering camera calibration settings

- [var isCameraIntrinsicMatrixDeliverySupported: Bool](/documentation/avfoundation/avcaptureconnection/iscameraintrinsicmatrixdeliverysupported)
- [var isCameraIntrinsicMatrixDeliveryEnabled: Bool](/documentation/avfoundation/avcaptureconnection/iscameraintrinsicmatrixdeliveryenabled)

#### Configuring a video’s frame rate

- [var isVideoMinFrameDurationSupported: Bool](/documentation/avfoundation/avcaptureconnection/isvideominframedurationsupported)
- [var videoMinFrameDuration: CMTime](/documentation/avfoundation/avcaptureconnection/videominframeduration)
- [var isVideoMaxFrameDurationSupported: Bool](/documentation/avfoundation/avcaptureconnection/isvideomaxframedurationsupported)
- [var videoMaxFrameDuration: CMTime](/documentation/avfoundation/avcaptureconnection/videomaxframeduration)

#### Scaling a video

- [var videoMaxScaleAndCropFactor: CGFloat](/documentation/avfoundation/avcaptureconnection/videomaxscaleandcropfactor)
- [var videoScaleAndCropFactor: CGFloat](/documentation/avfoundation/avcaptureconnection/videoscaleandcropfactor)

#### Interlacing video

- [var isVideoFieldModeSupported: Bool](/documentation/avfoundation/avcaptureconnection/isvideofieldmodesupported)
- [var videoFieldMode: AVVideoFieldMode](/documentation/avfoundation/avcaptureconnection/videofieldmode)
- [AVVideoFieldMode](/documentation/avfoundation/avvideofieldmode)

##### Constants

- [case both](/documentation/avfoundation/avvideofieldmode/both)
- [case topOnly](/documentation/avfoundation/avvideofieldmode/toponly)
- [case bottomOnly](/documentation/avfoundation/avvideofieldmode/bottomonly)
- [case deinterlace](/documentation/avfoundation/avvideofieldmode/deinterlace)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avvideofieldmode/init(rawvalue:))

#### Deprecated

- [var isVideoStabilizationEnabled: Bool](/documentation/avfoundation/avcaptureconnection/isvideostabilizationenabled)
- [var enablesVideoStabilizationWhenAvailable: Bool](/documentation/avfoundation/avcaptureconnection/enablesvideostabilizationwhenavailable)
- [var isVideoOrientationSupported: Bool](/documentation/avfoundation/avcaptureconnection/isvideoorientationsupported)
- [var videoOrientation: AVCaptureVideoOrientation](/documentation/avfoundation/avcaptureconnection/videoorientation)
- [AVCaptureVideoOrientation](/documentation/avfoundation/avcapturevideoorientation)

##### Constants

- [case portrait](/documentation/avfoundation/avcapturevideoorientation/portrait)
- [case portraitUpsideDown](/documentation/avfoundation/avcapturevideoorientation/portraitupsidedown)
- [case landscapeRight](/documentation/avfoundation/avcapturevideoorientation/landscaperight)
- [case landscapeLeft](/documentation/avfoundation/avcapturevideoorientation/landscapeleft)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturevideoorientation/init(rawvalue:))

### Capture devices

- [Choosing a capture device](/documentation/avfoundation/choosing-a-capture-device)
- [Adopting smart framing in your camera app](/documentation/avfoundation/adopting-smart-framing-in-your-camera-app)
- [AVCaptureDevice](/documentation/avfoundation/avcapturedevice)

#### Finding and monitoring devices

- [AVCaptureDevice.DiscoverySession](/documentation/avfoundation/avcapturedevice/discoverysession)

##### Creating a session

- [convenience init(deviceTypes: [AVCaptureDevice.DeviceType], mediaType: AVMediaType?, position: AVCaptureDevice.Position)](/documentation/avfoundation/avcapturedevice/discoverysession/init(devicetypes:mediatype:position:))

##### Finding devices

- [var devices: [AVCaptureDevice]](/documentation/avfoundation/avcapturedevice/discoverysession/devices)
- [var supportedMultiCamDeviceSets: [Set<AVCaptureDevice>]](/documentation/avfoundation/avcapturedevice/discoverysession/supportedmulticamdevicesets)
- [class func `default`(AVCaptureDevice.DeviceType, for: AVMediaType?, position: AVCaptureDevice.Position) -> AVCaptureDevice?](/documentation/avfoundation/avcapturedevice/default(_:for:position:))
- [class func `default`(for: AVMediaType) -> AVCaptureDevice?](/documentation/avfoundation/avcapturedevice/default(for:))
- [init?(uniqueID: String)](/documentation/avfoundation/avcapturedevice/init(uniqueid:))
- [class let wasConnectedNotification: NSNotification.Name](/documentation/avfoundation/avcapturedevice/wasconnectednotification)
- [class let wasDisconnectedNotification: NSNotification.Name](/documentation/avfoundation/avcapturedevice/wasdisconnectednotification)
- [class func devices(for: AVMediaType) -> [AVCaptureDevice]](/documentation/avfoundation/avcapturedevice/devices(for:))
- [class func devices() -> [AVCaptureDevice]](/documentation/avfoundation/avcapturedevice/devices())

#### Authorizing device access

- [class func requestAccess(for: AVMediaType, completionHandler: (Bool) -> Void)](/documentation/avfoundation/avcapturedevice/requestaccess(for:completionhandler:))
- [class func authorizationStatus(for: AVMediaType) -> AVAuthorizationStatus](/documentation/avfoundation/avcapturedevice/authorizationstatus(for:))
- [AVAuthorizationStatus](/documentation/avfoundation/avauthorizationstatus)

##### Status values

- [case notDetermined](/documentation/avfoundation/avauthorizationstatus/notdetermined)
- [case restricted](/documentation/avfoundation/avauthorizationstatus/restricted)
- [case denied](/documentation/avfoundation/avauthorizationstatus/denied)
- [case authorized](/documentation/avfoundation/avauthorizationstatus/authorized)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avauthorizationstatus/init(rawvalue:))

#### Identifying a device

- [var uniqueID: String](/documentation/avfoundation/avcapturedevice/uniqueid)
- [var modelID: String](/documentation/avfoundation/avcapturedevice/modelid)
- [var localizedName: String](/documentation/avfoundation/avcapturedevice/localizedname)
- [var manufacturer: String](/documentation/avfoundation/avcapturedevice/manufacturer)
- [var deviceType: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.property)
- [AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct)

##### Cameras

- [static let builtInWideAngleCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtinwideanglecamera)
- [static let builtInUltraWideCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtinultrawidecamera)
- [static let builtInTelephotoCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtintelephotocamera)
- [static let builtInDualCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtindualcamera)
- [static let builtInDualWideCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtindualwidecamera)
- [static let builtInTripleCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtintriplecamera)
- [static let continuityCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/continuitycamera)
- [static let builtInDuoCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtinduocamera)

##### Microphones

- [static let microphone: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/microphone)
- [static let builtInMicrophone: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtinmicrophone)

##### External devices

- [static let external: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/external)
- [static let externalUnknown: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/externalunknown)

##### Desk View

- [static let deskViewCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/deskviewcamera)

##### Depth sensing

- [static let builtInLiDARDepthCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtinlidardepthcamera)
- [static let builtInTrueDepthCamera: AVCaptureDevice.DeviceType](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/builtintruedepthcamera)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcapturedevice/devicetype-swift.struct/init(rawvalue:))
- [var position: AVCaptureDevice.Position](/documentation/avfoundation/avcapturedevice/position-swift.property)
- [AVCaptureDevice.Position](/documentation/avfoundation/avcapturedevice/position-swift.enum)

##### Positions

- [case front](/documentation/avfoundation/avcapturedevice/position-swift.enum/front)
- [case back](/documentation/avfoundation/avcapturedevice/position-swift.enum/back)
- [case unspecified](/documentation/avfoundation/avcapturedevice/position-swift.enum/unspecified)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/position-swift.enum/init(rawvalue:))

#### Accessing device state

- [var isConnected: Bool](/documentation/avfoundation/avcapturedevice/isconnected)
- [var isSuspended: Bool](/documentation/avfoundation/avcapturedevice/issuspended)
- [var isInUseByAnotherApplication: Bool](/documentation/avfoundation/avcapturedevice/isinusebyanotherapplication)

#### Inspecting device characteristics

- [var isVirtualDevice: Bool](/documentation/avfoundation/avcapturedevice/isvirtualdevice)
- [var constituentDevices: [AVCaptureDevice]](/documentation/avfoundation/avcapturedevice/constituentdevices)
- [func hasMediaType(AVMediaType) -> Bool](/documentation/avfoundation/avcapturedevice/hasmediatype(_:))
- [var transportType: Int32](/documentation/avfoundation/avcapturedevice/transporttype)
- [func supportsSessionPreset(AVCaptureSession.Preset) -> Bool](/documentation/avfoundation/avcapturedevice/supportssessionpreset(_:))

#### Monitoring device rotation

- [AVCaptureDevice.RotationCoordinator](/documentation/avfoundation/avcapturedevice/rotationcoordinator)

##### Creating a rotation coordinator

- [init(device: AVCaptureDevice, previewLayer: CALayer?)](/documentation/avfoundation/avcapturedevice/rotationcoordinator/init(device:previewlayer:))

##### Compensating for a device’s rotation

- [var videoRotationAngleForHorizonLevelCapture: CGFloat](/documentation/avfoundation/avcapturedevice/rotationcoordinator/videorotationangleforhorizonlevelcapture)
- [var videoRotationAngleForHorizonLevelPreview: CGFloat](/documentation/avfoundation/avcapturedevice/rotationcoordinator/videorotationangleforhorizonlevelpreview)

##### Inspecting a coordinator’s configuration

- [var device: AVCaptureDevice?](/documentation/avfoundation/avcapturedevice/rotationcoordinator/device)
- [var previewLayer: CALayer?](/documentation/avfoundation/avcapturedevice/rotationcoordinator/previewlayer)

#### Configuring camera hardware

- [func lockForConfiguration() throws](/documentation/avfoundation/avcapturedevice/lockforconfiguration())
- [func unlockForConfiguration()](/documentation/avfoundation/avcapturedevice/unlockforconfiguration())
- [var isSubjectAreaChangeMonitoringEnabled: Bool](/documentation/avfoundation/avcapturedevice/issubjectareachangemonitoringenabled)
- [class let subjectAreaDidChangeNotification: NSNotification.Name](/documentation/avfoundation/avcapturedevice/subjectareadidchangenotification)
- [Formats](/documentation/avfoundation/capture-device-formats)

##### Configuring capture formats

- [var formats: [AVCaptureDevice.Format]](/documentation/avfoundation/avcapturedevice/formats)
- [var activeFormat: AVCaptureDevice.Format](/documentation/avfoundation/avcapturedevice/activeformat)
- [var activeDepthDataFormat: AVCaptureDevice.Format?](/documentation/avfoundation/avcapturedevice/activedepthdataformat)
- [AVCaptureDevice.Format](/documentation/avfoundation/avcapturedevice/format)

###### Determining spatial capture support

- [var isSpatialVideoCaptureSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isspatialvideocapturesupported)

###### Determining background replacement support

- [var isBackgroundReplacementSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isbackgroundreplacementsupported)
- [var videoFrameRateRangeForBackgroundReplacement: AVFrameRateRange?](/documentation/avfoundation/avcapturedevice/format/videoframeraterangeforbackgroundreplacement)

###### Determining video capture support

- [var isAutoVideoFrameRateSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isautovideoframeratesupported)
- [var videoSupportedFrameRateRanges: [AVFrameRateRange]](/documentation/avfoundation/avcapturedevice/format/videosupportedframerateranges)
- [AVFrameRateRange](/documentation/avfoundation/avframeraterange)

###### Accessing properties

- [var maxFrameDuration: CMTime](/documentation/avfoundation/avframeraterange/maxframeduration)
- [var maxFrameRate: Float64](/documentation/avfoundation/avframeraterange/maxframerate)
- [var minFrameDuration: CMTime](/documentation/avfoundation/avframeraterange/minframeduration)
- [var minFrameRate: Float64](/documentation/avfoundation/avframeraterange/minframerate)
- [var isVideoBinned: Bool](/documentation/avfoundation/avcapturedevice/format/isvideobinned)
- [var isVideoHDRSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isvideohdrsupported)
- [var isMultiCamSupported: Bool](/documentation/avfoundation/avcapturedevice/format/ismulticamsupported)

###### Determining reaction effects support

- [var reactionEffectsSupported: Bool](/documentation/avfoundation/avcapturedevice/format/reactioneffectssupported)
- [var videoFrameRateRangeForReactionEffectsInProgress: AVFrameRateRange?](/documentation/avfoundation/avcapturedevice/format/videoframeraterangeforreactioneffectsinprogress)

###### Determining supported media formats

- [var mediaType: AVMediaType](/documentation/avfoundation/avcapturedevice/format/mediatype)
- [var formatDescription: CMFormatDescription](/documentation/avfoundation/avcapturedevice/format/formatdescription)

###### Determining output support

- [var unsupportedCaptureOutputClasses: [AnyClass]](/documentation/avfoundation/avcapturedevice/format/unsupportedcaptureoutputclasses)

###### Determining field of view

- [var videoFieldOfView: Float](/documentation/avfoundation/avcapturedevice/format/videofieldofview)
- [var geometricDistortionCorrectedVideoFieldOfView: Float](/documentation/avfoundation/avcapturedevice/format/geometricdistortioncorrectedvideofieldofview)

###### Determining video stabilization support

- [func isVideoStabilizationModeSupported(AVCaptureVideoStabilizationMode) -> Bool](/documentation/avfoundation/avcapturedevice/format/isvideostabilizationmodesupported(_:))
- [AVCaptureVideoStabilizationMode](/documentation/avfoundation/avcapturevideostabilizationmode)

###### Stabilization modes

- [case off](/documentation/avfoundation/avcapturevideostabilizationmode/off)
- [case standard](/documentation/avfoundation/avcapturevideostabilizationmode/standard)
- [case cinematic](/documentation/avfoundation/avcapturevideostabilizationmode/cinematic)
- [case cinematicExtended](/documentation/avfoundation/avcapturevideostabilizationmode/cinematicextended)
- [case previewOptimized](/documentation/avfoundation/avcapturevideostabilizationmode/previewoptimized)
- [case cinematicExtendedEnhanced](/documentation/avfoundation/avcapturevideostabilizationmode/cinematicextendedenhanced)
- [case auto](/documentation/avfoundation/avcapturevideostabilizationmode/auto)
- [case lowLatency](/documentation/avfoundation/avcapturevideostabilizationmode/lowlatency)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturevideostabilizationmode/init(rawvalue:))

###### Determining photo quality

- [var supportedMaxPhotoDimensions: [CMVideoDimensions]](/documentation/avfoundation/avcapturedevice/format/supportedmaxphotodimensions)
- [var isHighPhotoQualitySupported: Bool](/documentation/avfoundation/avcapturedevice/format/ishighphotoqualitysupported)
- [var isHighestPhotoQualitySupported: Bool](/documentation/avfoundation/avcapturedevice/format/ishighestphotoqualitysupported)

###### Determining color support

- [var isGlobalToneMappingSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isglobaltonemappingsupported)
- [var supportedColorSpaces: [AVCaptureColorSpace]](/documentation/avfoundation/avcapturedevice/format/supportedcolorspaces)

###### Determining exposure support

- [var systemRecommendedExposureBiasRange: ClosedRange<Float>?](/documentation/avfoundation/avcapturedevice/format/systemrecommendedexposurebiasrange)
- [var minISO: Float](/documentation/avfoundation/avcapturedevice/format/miniso)
- [var maxISO: Float](/documentation/avfoundation/avcapturedevice/format/maxiso)
- [var minExposureDuration: CMTime](/documentation/avfoundation/avcapturedevice/format/minexposureduration)
- [var maxExposureDuration: CMTime](/documentation/avfoundation/avcapturedevice/format/maxexposureduration)

###### Determining zoom capabilities

- [var systemRecommendedVideoZoomRange: ClosedRange<CGFloat>?](/documentation/avfoundation/avcapturedevice/format/systemrecommendedvideozoomrange)
- [var videoMaxZoomFactor: CGFloat](/documentation/avfoundation/avcapturedevice/format/videomaxzoomfactor)
- [var videoZoomFactorUpscaleThreshold: CGFloat](/documentation/avfoundation/avcapturedevice/format/videozoomfactorupscalethreshold)
- [var secondaryNativeResolutionZoomFactors: [CGFloat]](/documentation/avfoundation/avcapturedevice/format/secondarynativeresolutionzoomfactors)
- [var supportedVideoZoomRangesForDepthDataDelivery: [ClosedRange<CGFloat>]](/documentation/avfoundation/avcapturedevice/format/supportedvideozoomrangesfordepthdatadelivery)
- [var zoomFactorsOutsideOfVideoZoomRangesForDepthDeliverySupported: Bool](/documentation/avfoundation/avcapturedevice/format/zoomfactorsoutsideofvideozoomrangesfordepthdeliverysupported)

###### Determining the auto focus system

- [var autoFocusSystem: AVCaptureDevice.Format.AutoFocusSystem](/documentation/avfoundation/avcapturedevice/format/autofocussystem-swift.property)
- [AVCaptureDevice.Format.AutoFocusSystem](/documentation/avfoundation/avcapturedevice/format/autofocussystem-swift.enum)

###### Systems

- [case none](/documentation/avfoundation/avcapturedevice/format/autofocussystem-swift.enum/none)
- [case contrastDetection](/documentation/avfoundation/avcapturedevice/format/autofocussystem-swift.enum/contrastdetection)
- [case phaseDetection](/documentation/avfoundation/avcapturedevice/format/autofocussystem-swift.enum/phasedetection)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/format/autofocussystem-swift.enum/init(rawvalue:))

###### Determining Cinematic video support

- [var isCinematicVideoCaptureSupported: Bool](/documentation/avfoundation/avcapturedevice/format/iscinematicvideocapturesupported)
- [var defaultSimulatedAperture: Float](/documentation/avfoundation/avcapturedevice/format/defaultsimulatedaperture)
- [var minSimulatedAperture: Float](/documentation/avfoundation/avcapturedevice/format/minsimulatedaperture)
- [var maxSimulatedAperture: Float](/documentation/avfoundation/avcapturedevice/format/maxsimulatedaperture)
- [var videoMaxZoomFactorForCinematicVideo: CGFloat](/documentation/avfoundation/avcapturedevice/format/videomaxzoomfactorforcinematicvideo)
- [var videoMinZoomFactorForCinematicVideo: CGFloat](/documentation/avfoundation/avcapturedevice/format/videominzoomfactorforcinematicvideo)
- [var videoFrameRateRangeForCinematicVideo: AVFrameRateRange?](/documentation/avfoundation/avcapturedevice/format/videoframeraterangeforcinematicvideo)

###### Determining lens smudge detection support

- [var isCameraLensSmudgeDetectionSupported: Bool](/documentation/avfoundation/avcapturedevice/format/iscameralenssmudgedetectionsupported)

###### Determining smart framing support

- [var isSmartFramingSupported: Bool](/documentation/avfoundation/avcapturedevice/format/issmartframingsupported)

###### Determining dynamic aspect ratio support

- [var supportedDynamicAspectRatios: [AVCaptureDevice.AspectRatio]](/documentation/avfoundation/avcapturedevice/format/supporteddynamicaspectratios)
- [func videoFieldOfView(for: AVCaptureDevice.AspectRatio, geometricDistortionCorrected: Bool) -> Float](/documentation/avfoundation/avcapturedevice/format/videofieldofview(for:geometricdistortioncorrected:))

###### Determining Center Stage support

- [var isCenterStageSupported: Bool](/documentation/avfoundation/avcapturedevice/format/iscenterstagesupported)
- [var videoFrameRateRangeForCenterStage: AVFrameRateRange?](/documentation/avfoundation/avcapturedevice/format/videoframeraterangeforcenterstage)
- [var videoMinZoomFactorForCenterStage: CGFloat](/documentation/avfoundation/avcapturedevice/format/videominzoomfactorforcenterstage)
- [var videoMaxZoomFactorForCenterStage: CGFloat](/documentation/avfoundation/avcapturedevice/format/videomaxzoomfactorforcenterstage)

###### Determining Portrait Effects support

- [var isPortraitEffectSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isportraiteffectsupported)
- [var isPortraitEffectsMatteStillImageDeliverySupported: Bool](/documentation/avfoundation/avcapturedevice/format/isportraiteffectsmattestillimagedeliverysupported)
- [var videoFrameRateRangeForPortraitEffect: AVFrameRateRange?](/documentation/avfoundation/avcapturedevice/format/videoframeraterangeforportraiteffect)

###### Determining Studio Light support

- [var isStudioLightSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isstudiolightsupported)
- [var videoFrameRateRangeForStudioLight: AVFrameRateRange?](/documentation/avfoundation/avcapturedevice/format/videoframeraterangeforstudiolight)

###### Determining depth capture support

- [var supportedDepthDataFormats: [AVCaptureDevice.Format]](/documentation/avfoundation/avcapturedevice/format/supporteddepthdataformats)
- [var supportedVideoZoomFactorsForDepthDataDelivery: [CGFloat]](/documentation/avfoundation/avcapturedevice/format/supportedvideozoomfactorsfordepthdatadelivery)

###### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avcapturedevice-format-deprecated-symbols)

###### Determining video stabilization support

- [var isVideoStabilizationSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isvideostabilizationsupported)

###### Determining photo quality

- [var highResolutionStillImageDimensions: CMVideoDimensions](/documentation/avfoundation/avcapturedevice/format/highresolutionstillimagedimensions)

###### Determining zoom capabilities

- [var supportedVideoZoomFactorsForDepthDataDelivery: [CGFloat]](/documentation/avfoundation/avcapturedevice/format/supportedvideozoomfactorsfordepthdatadelivery)
- [var videoMinZoomFactorForDepthDataDelivery: CGFloat](/documentation/avfoundation/avcapturedevice/format/videominzoomfactorfordepthdatadelivery)
- [var videoMaxZoomFactorForDepthDataDelivery: CGFloat](/documentation/avfoundation/avcapturedevice/format/videomaxzoomfactorfordepthdatadelivery)

###### Instance Properties

- [var isEdgeLightSupported: Bool](/documentation/avfoundation/avcapturedevice/format/isedgelightsupported)

##### Configuring frame durations

- [var activeVideoMinFrameDuration: CMTime](/documentation/avfoundation/avcapturedevice/activevideominframeduration)
- [var activeVideoMaxFrameDuration: CMTime](/documentation/avfoundation/avcapturedevice/activevideomaxframeduration)
- [var activeDepthDataMinFrameDuration: CMTime](/documentation/avfoundation/avcapturedevice/activedepthdataminframeduration)
- [Focus](/documentation/avfoundation/capture-device-focus)

##### Configuring automatic focus

- [func isFocusModeSupported(AVCaptureDevice.FocusMode) -> Bool](/documentation/avfoundation/avcapturedevice/isfocusmodesupported(_:))
- [var focusMode: AVCaptureDevice.FocusMode](/documentation/avfoundation/avcapturedevice/focusmode-swift.property)
- [AVCaptureDevice.FocusMode](/documentation/avfoundation/avcapturedevice/focusmode-swift.enum)

###### Focus modes

- [case locked](/documentation/avfoundation/avcapturedevice/focusmode-swift.enum/locked)
- [case autoFocus](/documentation/avfoundation/avcapturedevice/focusmode-swift.enum/autofocus)
- [case continuousAutoFocus](/documentation/avfoundation/avcapturedevice/focusmode-swift.enum/continuousautofocus)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/focusmode-swift.enum/init(rawvalue:))
- [var isSmoothAutoFocusSupported: Bool](/documentation/avfoundation/avcapturedevice/issmoothautofocussupported)
- [var isSmoothAutoFocusEnabled: Bool](/documentation/avfoundation/avcapturedevice/issmoothautofocusenabled)
- [var isFaceDrivenAutoFocusEnabled: Bool](/documentation/avfoundation/avcapturedevice/isfacedrivenautofocusenabled)
- [var automaticallyAdjustsFaceDrivenAutoFocusEnabled: Bool](/documentation/avfoundation/avcapturedevice/automaticallyadjustsfacedrivenautofocusenabled)
- [var isAutoFocusRangeRestrictionSupported: Bool](/documentation/avfoundation/avcapturedevice/isautofocusrangerestrictionsupported)
- [var autoFocusRangeRestriction: AVCaptureDevice.AutoFocusRangeRestriction](/documentation/avfoundation/avcapturedevice/autofocusrangerestriction-swift.property)
- [AVCaptureDevice.AutoFocusRangeRestriction](/documentation/avfoundation/avcapturedevice/autofocusrangerestriction-swift.enum)

###### Constants

- [case none](/documentation/avfoundation/avcapturedevice/autofocusrangerestriction-swift.enum/none)
- [case near](/documentation/avfoundation/avcapturedevice/autofocusrangerestriction-swift.enum/near)
- [case far](/documentation/avfoundation/avcapturedevice/autofocusrangerestriction-swift.enum/far)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/autofocusrangerestriction-swift.enum/init(rawvalue:))

##### Setting a focus point of interest

- [var isFocusPointOfInterestSupported: Bool](/documentation/avfoundation/avcapturedevice/isfocuspointofinterestsupported)
- [var focusPointOfInterest: CGPoint](/documentation/avfoundation/avcapturedevice/focuspointofinterest)

##### Setting a focus rectangle of interest

- [var isFocusRectOfInterestSupported: Bool](/documentation/avfoundation/avcapturedevice/isfocusrectofinterestsupported)
- [var focusRectOfInterest: CGRect](/documentation/avfoundation/avcapturedevice/focusrectofinterest)
- [var minFocusRectOfInterestSize: CGSize](/documentation/avfoundation/avcapturedevice/minfocusrectofinterestsize)
- [func defaultRectForFocusPoint(ofInterest: CGPoint) -> CGRect](/documentation/avfoundation/avcapturedevice/defaultrectforfocuspoint(ofinterest:))

##### Monitoring focus changes

- [var isAdjustingFocus: Bool](/documentation/avfoundation/avcapturedevice/isadjustingfocus)

##### Setting focus manually

- [var isLockingFocusWithCustomLensPositionSupported: Bool](/documentation/avfoundation/avcapturedevice/islockingfocuswithcustomlenspositionsupported)
- [var lensPosition: Float](/documentation/avfoundation/avcapturedevice/lensposition)
- [class let currentLensPosition: Float](/documentation/avfoundation/avcapturedevice/currentlensposition)
- [func setFocusModeLocked(lensPosition: Float, completionHandler: ((CMTime) -> Void)?)](/documentation/avfoundation/avcapturedevice/setfocusmodelocked(lensposition:completionhandler:))

##### Inspecting the focus distance

- [var minimumFocusDistance: Int](/documentation/avfoundation/avcapturedevice/minimumfocusdistance)
- [Exposure](/documentation/avfoundation/capture-device-exposure)

##### Managing the exposure mode

- [func isExposureModeSupported(AVCaptureDevice.ExposureMode) -> Bool](/documentation/avfoundation/avcapturedevice/isexposuremodesupported(_:))
- [var exposureMode: AVCaptureDevice.ExposureMode](/documentation/avfoundation/avcapturedevice/exposuremode-swift.property)
- [AVCaptureDevice.ExposureMode](/documentation/avfoundation/avcapturedevice/exposuremode-swift.enum)

###### Exposure modes

- [case locked](/documentation/avfoundation/avcapturedevice/exposuremode-swift.enum/locked)
- [case autoExpose](/documentation/avfoundation/avcapturedevice/exposuremode-swift.enum/autoexpose)
- [case continuousAutoExposure](/documentation/avfoundation/avcapturedevice/exposuremode-swift.enum/continuousautoexposure)
- [case custom](/documentation/avfoundation/avcapturedevice/exposuremode-swift.enum/custom)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/exposuremode-swift.enum/init(rawvalue:))

##### Setting an exposure point of interest

- [var isExposurePointOfInterestSupported: Bool](/documentation/avfoundation/avcapturedevice/isexposurepointofinterestsupported)
- [var exposurePointOfInterest: CGPoint](/documentation/avfoundation/avcapturedevice/exposurepointofinterest)

##### Setting an exposure rectangle of interest

- [var isExposureRectOfInterestSupported: Bool](/documentation/avfoundation/avcapturedevice/isexposurerectofinterestsupported)
- [var exposureRectOfInterest: CGRect](/documentation/avfoundation/avcapturedevice/exposurerectofinterest)
- [var minExposureRectOfInterestSize: CGSize](/documentation/avfoundation/avcapturedevice/minexposurerectofinterestsize)
- [func defaultRectForExposurePoint(ofInterest: CGPoint) -> CGRect](/documentation/avfoundation/avcapturedevice/defaultrectforexposurepoint(ofinterest:))

##### Configuring face-driven automatic exposure

- [var isFaceDrivenAutoExposureEnabled: Bool](/documentation/avfoundation/avcapturedevice/isfacedrivenautoexposureenabled)
- [var automaticallyAdjustsFaceDrivenAutoExposureEnabled: Bool](/documentation/avfoundation/avcapturedevice/automaticallyadjustsfacedrivenautoexposureenabled)

##### Monitoring exposure changes

- [var isAdjustingExposure: Bool](/documentation/avfoundation/avcapturedevice/isadjustingexposure)

##### Adjusting exposure compensation

- [var exposureTargetOffset: Float](/documentation/avfoundation/avcapturedevice/exposuretargetoffset)
- [var exposureTargetBias: Float](/documentation/avfoundation/avcapturedevice/exposuretargetbias)
- [var minExposureTargetBias: Float](/documentation/avfoundation/avcapturedevice/minexposuretargetbias)
- [var maxExposureTargetBias: Float](/documentation/avfoundation/avcapturedevice/maxexposuretargetbias)
- [class let currentExposureTargetBias: Float](/documentation/avfoundation/avcapturedevice/currentexposuretargetbias)
- [func setExposureTargetBias(Float, completionHandler: ((CMTime) -> Void)?)](/documentation/avfoundation/avcapturedevice/setexposuretargetbias(_:completionhandler:))

##### Configuring exposure manually

- [var exposureDuration: CMTime](/documentation/avfoundation/avcapturedevice/exposureduration)
- [var activeMaxExposureDuration: CMTime](/documentation/avfoundation/avcapturedevice/activemaxexposureduration)
- [var iso: Float](/documentation/avfoundation/avcapturedevice/iso)
- [var lensAperture: Float](/documentation/avfoundation/avcapturedevice/lensaperture)
- [func setExposureModeCustom(duration: CMTime, iso: Float, completionHandler: ((CMTime) -> Void)?)](/documentation/avfoundation/avcapturedevice/setexposuremodecustom(duration:iso:completionhandler:))

###### Exposure constants

- [class let currentExposureDuration: CMTime](/documentation/avfoundation/avcapturedevice/currentexposureduration)
- [class let currentISO: Float](/documentation/avfoundation/avcapturedevice/currentiso)
- [White balance](/documentation/avfoundation/capture-device-white-balance)

##### Configuring automatic white balance

- [func isWhiteBalanceModeSupported(AVCaptureDevice.WhiteBalanceMode) -> Bool](/documentation/avfoundation/avcapturedevice/iswhitebalancemodesupported(_:))
- [var whiteBalanceMode: AVCaptureDevice.WhiteBalanceMode](/documentation/avfoundation/avcapturedevice/whitebalancemode-swift.property)
- [AVCaptureDevice.WhiteBalanceMode](/documentation/avfoundation/avcapturedevice/whitebalancemode-swift.enum)

###### White balance modes

- [case locked](/documentation/avfoundation/avcapturedevice/whitebalancemode-swift.enum/locked)
- [case autoWhiteBalance](/documentation/avfoundation/avcapturedevice/whitebalancemode-swift.enum/autowhitebalance)
- [case continuousAutoWhiteBalance](/documentation/avfoundation/avcapturedevice/whitebalancemode-swift.enum/continuousautowhitebalance)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/whitebalancemode-swift.enum/init(rawvalue:))

##### Monitoring white balance changes

- [var isAdjustingWhiteBalance: Bool](/documentation/avfoundation/avcapturedevice/isadjustingwhitebalance)

##### Inspecting gain levels

- [var deviceWhiteBalanceGains: AVCaptureDevice.WhiteBalanceGains](/documentation/avfoundation/avcapturedevice/devicewhitebalancegains)
- [var grayWorldDeviceWhiteBalanceGains: AVCaptureDevice.WhiteBalanceGains](/documentation/avfoundation/avcapturedevice/grayworlddevicewhitebalancegains)
- [var maxWhiteBalanceGain: Float](/documentation/avfoundation/avcapturedevice/maxwhitebalancegain)

##### Performing conversions

- [func chromaticityValues(for: AVCaptureDevice.WhiteBalanceGains) -> AVCaptureDevice.WhiteBalanceChromaticityValues](/documentation/avfoundation/avcapturedevice/chromaticityvalues(for:))
- [func temperatureAndTintValues(for: AVCaptureDevice.WhiteBalanceGains) -> AVCaptureDevice.WhiteBalanceTemperatureAndTintValues](/documentation/avfoundation/avcapturedevice/temperatureandtintvalues(for:))
- [func deviceWhiteBalanceGains(for: AVCaptureDevice.WhiteBalanceChromaticityValues) -> AVCaptureDevice.WhiteBalanceGains](/documentation/avfoundation/avcapturedevice/devicewhitebalancegains(for:)-9gdtw)
- [func deviceWhiteBalanceGains(for: AVCaptureDevice.WhiteBalanceTemperatureAndTintValues) -> AVCaptureDevice.WhiteBalanceGains](/documentation/avfoundation/avcapturedevice/devicewhitebalancegains(for:)-3wtsa)
- [AVCaptureDevice.WhiteBalanceGains](/documentation/avfoundation/avcapturedevice/whitebalancegains)

###### Creating white balance gains

- [init()](/documentation/avfoundation/avcapturedevice/whitebalancegains/init())
- [init(redGain: Float, greenGain: Float, blueGain: Float)](/documentation/avfoundation/avcapturedevice/whitebalancegains/init(redgain:greengain:bluegain:))

###### Isolating gain by color channel

- [var blueGain: Float](/documentation/avfoundation/avcapturedevice/whitebalancegains/bluegain)
- [var greenGain: Float](/documentation/avfoundation/avcapturedevice/whitebalancegains/greengain)
- [var redGain: Float](/documentation/avfoundation/avcapturedevice/whitebalancegains/redgain)
- [AVCaptureDevice.WhiteBalanceChromaticityValues](/documentation/avfoundation/avcapturedevice/whitebalancechromaticityvalues)

###### Creating chromaticity values

- [init()](/documentation/avfoundation/avcapturedevice/whitebalancechromaticityvalues/init())
- [init(x: Float, y: Float)](/documentation/avfoundation/avcapturedevice/whitebalancechromaticityvalues/init(x:y:))

###### Inspecting the values

- [var x: Float](/documentation/avfoundation/avcapturedevice/whitebalancechromaticityvalues/x)
- [var y: Float](/documentation/avfoundation/avcapturedevice/whitebalancechromaticityvalues/y)
- [AVCaptureDevice.WhiteBalanceTemperatureAndTintValues](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues)

###### Accessing standard values

- [static let cloudy: AVCaptureDevice.WhiteBalanceTemperatureAndTintValues](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/cloudy)
- [static let daylight: AVCaptureDevice.WhiteBalanceTemperatureAndTintValues](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/daylight)
- [static let fluorescent: AVCaptureDevice.WhiteBalanceTemperatureAndTintValues](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/fluorescent)
- [static let shadow: AVCaptureDevice.WhiteBalanceTemperatureAndTintValues](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/shadow)
- [static let tungsten: AVCaptureDevice.WhiteBalanceTemperatureAndTintValues](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/tungsten)

###### Creating temperature and tint values

- [init()](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/init())
- [init(temperature: Float, tint: Float)](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/init(temperature:tint:))

###### Inspecting the values

- [var temperature: Float](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/temperature)
- [var tint: Float](/documentation/avfoundation/avcapturedevice/whitebalancetemperatureandtintvalues/tint)

##### Setting white balance manually

- [var isLockingWhiteBalanceWithCustomDeviceGainsSupported: Bool](/documentation/avfoundation/avcapturedevice/islockingwhitebalancewithcustomdevicegainssupported)
- [func setWhiteBalanceModeLocked(with: AVCaptureDevice.WhiteBalanceGains, completionHandler: ((CMTime) -> Void)?)](/documentation/avfoundation/avcapturedevice/setwhitebalancemodelocked(with:completionhandler:))

###### White balance constants

- [class let currentWhiteBalanceGains: AVCaptureDevice.WhiteBalanceGains](/documentation/avfoundation/avcapturedevice/currentwhitebalancegains)
- [func setWhiteBalanceModeLocked(whiteBalanceTemperatureAndTintValues: AVCaptureDevice.WhiteBalanceTemperatureAndTintValues, handler: ((CMTime) -> Void)?)](/documentation/avfoundation/avcapturedevice/setwhitebalancemodelocked(whitebalancetemperatureandtintvalues:handler:))
- [Lighting](/documentation/avfoundation/capture-device-lighting)

##### Configuring flash settings

- [var hasFlash: Bool](/documentation/avfoundation/avcapturedevice/hasflash)
- [var isFlashAvailable: Bool](/documentation/avfoundation/avcapturedevice/isflashavailable)
- [var isFlashActive: Bool](/documentation/avfoundation/avcapturedevice/isflashactive)
- [var flashMode: AVCaptureDevice.FlashMode](/documentation/avfoundation/avcapturedevice/flashmode-swift.property)
- [func isFlashModeSupported(AVCaptureDevice.FlashMode) -> Bool](/documentation/avfoundation/avcapturedevice/isflashmodesupported(_:))
- [AVCaptureDevice.FlashMode](/documentation/avfoundation/avcapturedevice/flashmode-swift.enum)

###### Flash modes

- [case off](/documentation/avfoundation/avcapturedevice/flashmode-swift.enum/off)
- [case on](/documentation/avfoundation/avcapturedevice/flashmode-swift.enum/on)
- [case auto](/documentation/avfoundation/avcapturedevice/flashmode-swift.enum/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/flashmode-swift.enum/init(rawvalue:))

##### Configuring torch settings

- [var hasTorch: Bool](/documentation/avfoundation/avcapturedevice/hastorch)
- [var isTorchAvailable: Bool](/documentation/avfoundation/avcapturedevice/istorchavailable)
- [var isTorchActive: Bool](/documentation/avfoundation/avcapturedevice/istorchactive)
- [var torchLevel: Float](/documentation/avfoundation/avcapturedevice/torchlevel)
- [var torchMode: AVCaptureDevice.TorchMode](/documentation/avfoundation/avcapturedevice/torchmode-swift.property)
- [AVCaptureDevice.TorchMode](/documentation/avfoundation/avcapturedevice/torchmode-swift.enum)

###### Torch modes

- [case off](/documentation/avfoundation/avcapturedevice/torchmode-swift.enum/off)
- [case on](/documentation/avfoundation/avcapturedevice/torchmode-swift.enum/on)
- [case auto](/documentation/avfoundation/avcapturedevice/torchmode-swift.enum/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/torchmode-swift.enum/init(rawvalue:))
- [func isTorchModeSupported(AVCaptureDevice.TorchMode) -> Bool](/documentation/avfoundation/avcapturedevice/istorchmodesupported(_:))
- [func setTorchModeOn(level: Float) throws](/documentation/avfoundation/avcapturedevice/settorchmodeon(level:))
- [class let maxAvailableTorchLevel: Float](/documentation/avfoundation/avcapturedevice/maxavailabletorchlevel)

##### Configuring low light settings

- [var isLowLightBoostSupported: Bool](/documentation/avfoundation/avcapturedevice/islowlightboostsupported)
- [var isLowLightBoostEnabled: Bool](/documentation/avfoundation/avcapturedevice/islowlightboostenabled)
- [var automaticallyEnablesLowLightBoostWhenAvailable: Bool](/documentation/avfoundation/avcapturedevice/automaticallyenableslowlightboostwhenavailable)
- [Color](/documentation/avfoundation/capture-device-color)

##### Configuring HDR settings

- [var automaticallyAdjustsVideoHDREnabled: Bool](/documentation/avfoundation/avcapturedevice/automaticallyadjustsvideohdrenabled)
- [var isVideoHDREnabled: Bool](/documentation/avfoundation/avcapturedevice/isvideohdrenabled)

##### Enabling global tone mapping

- [var isGlobalToneMappingEnabled: Bool](/documentation/avfoundation/avcapturedevice/isglobaltonemappingenabled)

##### Configuring color space settings

- [var activeColorSpace: AVCaptureColorSpace](/documentation/avfoundation/avcapturedevice/activecolorspace)
- [AVCaptureColorSpace](/documentation/avfoundation/avcapturecolorspace)

###### Color spaces

- [case sRGB](/documentation/avfoundation/avcapturecolorspace/srgb)
- [case P3_D65](/documentation/avfoundation/avcapturecolorspace/p3_d65)
- [case HLG_BT2020](/documentation/avfoundation/avcapturecolorspace/hlg_bt2020)
- [case appleLog](/documentation/avfoundation/avcapturecolorspace/applelog)
- [case appleLog2](/documentation/avfoundation/avcapturecolorspace/applelog2)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturecolorspace/init(rawvalue:))
- [Zoom](/documentation/avfoundation/capture-device-zoom)

##### Adjusting zoom

- [var videoZoomFactor: CGFloat](/documentation/avfoundation/avcapturedevice/videozoomfactor)
- [func ramp(toVideoZoomFactor: CGFloat, withRate: Float)](/documentation/avfoundation/avcapturedevice/ramp(tovideozoomfactor:withrate:))
- [func cancelVideoZoomRamp()](/documentation/avfoundation/avcapturedevice/cancelvideozoomramp())

##### Observing zoom

- [var isRampingVideoZoom: Bool](/documentation/avfoundation/avcapturedevice/isrampingvideozoom)

##### Inspecting zoom factors

- [var minAvailableVideoZoomFactor: CGFloat](/documentation/avfoundation/avcapturedevice/minavailablevideozoomfactor)
- [var maxAvailableVideoZoomFactor: CGFloat](/documentation/avfoundation/avcapturedevice/maxavailablevideozoomfactor)
- [var virtualDeviceSwitchOverVideoZoomFactors: [NSNumber]](/documentation/avfoundation/avcapturedevice/virtualdeviceswitchovervideozoomfactors)
- [var dualCameraSwitchOverVideoZoomFactor: CGFloat](/documentation/avfoundation/avcapturedevice/dualcameraswitchovervideozoomfactor)
- [var displayVideoZoomFactorMultiplier: CGFloat](/documentation/avfoundation/avcapturedevice/displayvideozoomfactormultiplier)

##### Enabling geometric distortion correction

- [var isGeometricDistortionCorrectionSupported: Bool](/documentation/avfoundation/avcapturedevice/isgeometricdistortioncorrectionsupported)
- [var isGeometricDistortionCorrectionEnabled: Bool](/documentation/avfoundation/avcapturedevice/isgeometricdistortioncorrectionenabled)

#### Configuring Cinematic video

- [func setCinematicVideoFixedFocus(at: CGPoint, focusMode: AVCaptureDevice.CinematicVideoFocusMode)](/documentation/avfoundation/avcapturedevice/setcinematicvideofixedfocus(at:focusmode:))
- [func setCinematicVideoTrackingFocus(at: CGPoint, focusMode: AVCaptureDevice.CinematicVideoFocusMode)](/documentation/avfoundation/avcapturedevice/setcinematicvideotrackingfocus(at:focusmode:))
- [func setCinematicVideoTrackingFocus(detectedObjectID: Int, focusMode: AVCaptureDevice.CinematicVideoFocusMode)](/documentation/avfoundation/avcapturedevice/setcinematicvideotrackingfocus(detectedobjectid:focusmode:))
- [AVCaptureDevice.CinematicVideoFocusMode](/documentation/avfoundation/avcapturedevice/cinematicvideofocusmode)

##### Focus modes

- [case none](/documentation/avfoundation/avcapturedevice/cinematicvideofocusmode/none)
- [case strong](/documentation/avfoundation/avcapturedevice/cinematicvideofocusmode/strong)
- [case weak](/documentation/avfoundation/avcapturedevice/cinematicvideofocusmode/weak)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/cinematicvideofocusmode/init(rawvalue:))
- [AVCaptureSceneMonitoringStatus](/documentation/avfoundation/avcapturescenemonitoringstatus)

##### Status values

- [static let notEnoughLight: AVCaptureSceneMonitoringStatus](/documentation/avfoundation/avcapturescenemonitoringstatus/notenoughlight)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcapturescenemonitoringstatus/init(rawvalue:))
- [static let notEnoughLight: AVCaptureSceneMonitoringStatus](/documentation/avfoundation/avcapturescenemonitoringstatus/notenoughlight)
- [var cinematicVideoCaptureSceneMonitoringStatuses: Set<AVCaptureSceneMonitoringStatus>](/documentation/avfoundation/avcapturedevice/cinematicvideocapturescenemonitoringstatuses)

#### Configuring smart framing

- [var smartFramingMonitor: AVCaptureSmartFramingMonitor?](/documentation/avfoundation/avcapturedevice/smartframingmonitor)
- [AVCaptureSmartFramingMonitor](/documentation/avfoundation/avcapturesmartframingmonitor)

##### Configuring framings

- [var supportedFramings: [AVCaptureFraming]](/documentation/avfoundation/avcapturesmartframingmonitor/supportedframings)
- [var enabledFramings: [AVCaptureFraming]](/documentation/avfoundation/avcapturesmartframingmonitor/enabledframings)
- [var recommendedFraming: AVCaptureFraming?](/documentation/avfoundation/avcapturesmartframingmonitor/recommendedframing)

##### Managing the life cycle

- [var isMonitoring: Bool](/documentation/avfoundation/avcapturesmartframingmonitor/ismonitoring)
- [func startMonitoring() throws](/documentation/avfoundation/avcapturesmartframingmonitor/startmonitoring())
- [func stopMonitoring()](/documentation/avfoundation/avcapturesmartframingmonitor/stopmonitoring())
- [AVCaptureFraming](/documentation/avfoundation/avcaptureframing)

##### Inspecting a framing

- [var aspectRatio: AVCaptureDevice.AspectRatio](/documentation/avfoundation/avcaptureframing/aspectratio)
- [var zoomFactor: Float](/documentation/avfoundation/avcaptureframing/zoomfactor)

#### Configuring dynamic aspect ratio

- [func setDynamicAspectRatio(AVCaptureDevice.AspectRatio, completionHandler: ((CMTime, (any Error)?) -> Void)?)](/documentation/avfoundation/avcapturedevice/setdynamicaspectratio(_:completionhandler:))
- [AVCaptureDevice.AspectRatio](/documentation/avfoundation/avcapturedevice/aspectratio)

##### Aspect ratios

- [static let ratio16x9: AVCaptureDevice.AspectRatio](/documentation/avfoundation/avcapturedevice/aspectratio/ratio16x9)
- [static let ratio1x1: AVCaptureDevice.AspectRatio](/documentation/avfoundation/avcapturedevice/aspectratio/ratio1x1)
- [static let ratio3x4: AVCaptureDevice.AspectRatio](/documentation/avfoundation/avcapturedevice/aspectratio/ratio3x4)
- [static let ratio4x3: AVCaptureDevice.AspectRatio](/documentation/avfoundation/avcapturedevice/aspectratio/ratio4x3)
- [static let ratio9x16: AVCaptureDevice.AspectRatio](/documentation/avfoundation/avcapturedevice/aspectratio/ratio9x16)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcapturedevice/aspectratio/init(rawvalue:))
- [var dynamicAspectRatio: AVCaptureDevice.AspectRatio?](/documentation/avfoundation/avcapturedevice/dynamicaspectratio)
- [var dynamicDimensions: CMVideoDimensions](/documentation/avfoundation/avcapturedevice/dynamicdimensions)

#### Enabling automatic frame rate

- [var isAutoVideoFrameRateEnabled: Bool](/documentation/avfoundation/avcapturedevice/isautovideoframerateenabled)

#### Supporting spatial capture

- [var spatialCaptureDiscomfortReasons: Set<AVSpatialCaptureDiscomfortReason>](/documentation/avfoundation/avcapturedevice/spatialcapturediscomfortreasons)
- [AVSpatialCaptureDiscomfortReason](/documentation/avfoundation/avspatialcapturediscomfortreason)

##### Discomfort reasons

- [static let notEnoughLight: AVSpatialCaptureDiscomfortReason](/documentation/avfoundation/avspatialcapturediscomfortreason/notenoughlight)
- [static let subjectTooClose: AVSpatialCaptureDiscomfortReason](/documentation/avfoundation/avspatialcapturediscomfortreason/subjecttooclose)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avspatialcapturediscomfortreason/init(rawvalue:))

#### Supporting Continuity Camera

- [class var systemPreferredCamera: AVCaptureDevice?](/documentation/avfoundation/avcapturedevice/systempreferredcamera)
- [class var userPreferredCamera: AVCaptureDevice?](/documentation/avfoundation/avcapturedevice/userpreferredcamera)
- [var isContinuityCamera: Bool](/documentation/avfoundation/avcapturedevice/iscontinuitycamera)
- [var companionDeskViewCamera: AVCaptureDevice?](/documentation/avfoundation/avcapturedevice/companiondeskviewcamera)

#### Supporting system features

- [System video effects and microphone modes](/documentation/avfoundation/system-video-effects-and-microphone-modes)

##### Performing reaction effects

- [class var reactionEffectsEnabled: Bool](/documentation/avfoundation/avcapturedevice/reactioneffectsenabled)
- [var canPerformReactionEffects: Bool](/documentation/avfoundation/avcapturedevice/canperformreactioneffects)
- [var availableReactionTypes: Set<AVCaptureReactionType>](/documentation/avfoundation/avcapturedevice/availablereactiontypes)
- [class var reactionEffectGesturesEnabled: Bool](/documentation/avfoundation/avcapturedevice/reactioneffectgesturesenabled)
- [func performEffect(for: AVCaptureReactionType)](/documentation/avfoundation/avcapturedevice/performeffect(for:))
- [var reactionEffectsInProgress: [AVCaptureReactionEffectState]](/documentation/avfoundation/avcapturedevice/reactioneffectsinprogress)
- [AVCaptureReactionEffectState](/documentation/avfoundation/avcapturereactioneffectstate)

###### Configuring the effect state

- [var reactionType: AVCaptureReactionType](/documentation/avfoundation/avcapturereactioneffectstate/reactiontype)
- [AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype)

###### Reaction types

- [static let balloons: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/balloons)
- [static let confetti: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/confetti)
- [static let fireworks: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/fireworks)
- [static let heart: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/heart)
- [static let lasers: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/lasers)
- [static let rain: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/rain)
- [static let thumbsUp: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/thumbsup)
- [static let thumbsDown: AVCaptureReactionType](/documentation/avfoundation/avcapturereactiontype/thumbsdown)

###### Accessing the system image name

- [var systemImageName: String](/documentation/avfoundation/avcapturereactiontype/systemimagename)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcapturereactiontype/init(rawvalue:))
- [var startTime: CMTime](/documentation/avfoundation/avcapturereactioneffectstate/starttime)
- [var endTime: CMTime](/documentation/avfoundation/avcapturereactioneffectstate/endtime)

##### Configuring Center Stage

- [var isCenterStageActive: Bool](/documentation/avfoundation/avcapturedevice/iscenterstageactive)
- [class var isCenterStageEnabled: Bool](/documentation/avfoundation/avcapturedevice/iscenterstageenabled)
- [var centerStageRectOfInterest: CGRect](/documentation/avfoundation/avcapturedevice/centerstagerectofinterest)
- [class var centerStageControlMode: AVCaptureDevice.CenterStageControlMode](/documentation/avfoundation/avcapturedevice/centerstagecontrolmode-swift.type.property)
- [AVCaptureDevice.CenterStageControlMode](/documentation/avfoundation/avcapturedevice/centerstagecontrolmode-swift.enum)

###### Control modes

- [case user](/documentation/avfoundation/avcapturedevice/centerstagecontrolmode-swift.enum/user)
- [case app](/documentation/avfoundation/avcapturedevice/centerstagecontrolmode-swift.enum/app)
- [case cooperative](/documentation/avfoundation/avcapturedevice/centerstagecontrolmode-swift.enum/cooperative)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/centerstagecontrolmode-swift.enum/init(rawvalue:))

##### Configuring Studio Light

- [var isStudioLightActive: Bool](/documentation/avfoundation/avcapturedevice/isstudiolightactive)
- [class var isStudioLightEnabled: Bool](/documentation/avfoundation/avcapturedevice/isstudiolightenabled)

##### Inspecting the Portrait Effect settings

- [var isPortraitEffectActive: Bool](/documentation/avfoundation/avcapturedevice/isportraiteffectactive)
- [class var isPortraitEffectEnabled: Bool](/documentation/avfoundation/avcapturedevice/isportraiteffectenabled)

##### Inspecting the microphone mode

- [class var activeMicrophoneMode: AVCaptureDevice.MicrophoneMode](/documentation/avfoundation/avcapturedevice/activemicrophonemode)
- [class var preferredMicrophoneMode: AVCaptureDevice.MicrophoneMode](/documentation/avfoundation/avcapturedevice/preferredmicrophonemode)
- [AVCaptureDevice.MicrophoneMode](/documentation/avfoundation/avcapturedevice/microphonemode)

###### Microphone modes

- [case standard](/documentation/avfoundation/avcapturedevice/microphonemode/standard)
- [case wideSpectrum](/documentation/avfoundation/avcapturedevice/microphonemode/widespectrum)
- [case voiceIsolation](/documentation/avfoundation/avcapturedevice/microphonemode/voiceisolation)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/microphonemode/init(rawvalue:))

##### Presenting the configuration user interface

- [class func showSystemUserInterface(AVCaptureDevice.SystemUserInterface)](/documentation/avfoundation/avcapturedevice/showsystemuserinterface(_:))
- [AVCaptureDevice.SystemUserInterface](/documentation/avfoundation/avcapturedevice/systemuserinterface)

###### User interfaces

- [case videoEffects](/documentation/avfoundation/avcapturedevice/systemuserinterface/videoeffects)
- [case microphoneModes](/documentation/avfoundation/avcapturedevice/systemuserinterface/microphonemodes)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/systemuserinterface/init(rawvalue:))

##### Configuring background replacement

- [var isBackgroundReplacementActive: Bool](/documentation/avfoundation/avcapturedevice/isbackgroundreplacementactive)
- [class var isBackgroundReplacementEnabled: Bool](/documentation/avfoundation/avcapturedevice/isbackgroundreplacementenabled)

#### Monitoring system pressure

- [var systemPressureState: AVCaptureDevice.SystemPressureState](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.property)
- [AVCaptureDevice.SystemPressureState](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class)

##### Overall level

- [var level: AVCaptureDevice.SystemPressureState.Level](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.property)
- [AVCaptureDevice.SystemPressureState.Level](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.struct)

###### System pressure levels

- [static let nominal: AVCaptureDevice.SystemPressureState.Level](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.struct/nominal)
- [static let fair: AVCaptureDevice.SystemPressureState.Level](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.struct/fair)
- [static let serious: AVCaptureDevice.SystemPressureState.Level](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.struct/serious)
- [static let critical: AVCaptureDevice.SystemPressureState.Level](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.struct/critical)
- [static let shutdown: AVCaptureDevice.SystemPressureState.Level](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.struct/shutdown)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/level-swift.struct/init(rawvalue:))

##### Contributing factors

- [var factors: AVCaptureDevice.SystemPressureState.Factors](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/factors-swift.property)
- [AVCaptureDevice.SystemPressureState.Factors](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/factors-swift.struct)

###### System pressure factors

- [static var systemTemperature: AVCaptureDevice.SystemPressureState.Factors](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/factors-swift.struct/systemtemperature)
- [static var peakPower: AVCaptureDevice.SystemPressureState.Factors](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/factors-swift.struct/peakpower)
- [static var depthModuleTemperature: AVCaptureDevice.SystemPressureState.Factors](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/factors-swift.struct/depthmoduletemperature)
- [static var cameraTemperature: AVCaptureDevice.SystemPressureState.Factors](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/factors-swift.struct/cameratemperature)

###### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avcapturedevice/systempressurestate-swift.class/factors-swift.struct/init(rawvalue:))
- [let AVCaptureSessionInterruptionSystemPressureStateKey: String](/documentation/avfoundation/avcapturesessioninterruptionsystempressurestatekey)

#### Restricting camera switching

- [func setPrimaryConstituentDeviceSwitchingBehavior(AVCaptureDevice.PrimaryConstituentDeviceSwitchingBehavior, restrictedSwitchingBehaviorConditions: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions)](/documentation/avfoundation/avcapturedevice/setprimaryconstituentdeviceswitchingbehavior(_:restrictedswitchingbehaviorconditions:))
- [var primaryConstituentDeviceSwitchingBehavior: AVCaptureDevice.PrimaryConstituentDeviceSwitchingBehavior](/documentation/avfoundation/avcapturedevice/primaryconstituentdeviceswitchingbehavior-swift.property)
- [var primaryConstituentDeviceRestrictedSwitchingBehaviorConditions: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions](/documentation/avfoundation/avcapturedevice/primaryconstituentdevicerestrictedswitchingbehaviorconditions-swift.property)
- [var activePrimaryConstituentDeviceSwitchingBehavior: AVCaptureDevice.PrimaryConstituentDeviceSwitchingBehavior](/documentation/avfoundation/avcapturedevice/activeprimaryconstituentdeviceswitchingbehavior)
- [var activePrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions](/documentation/avfoundation/avcapturedevice/activeprimaryconstituentdevicerestrictedswitchingbehaviorconditions)
- [var activePrimaryConstituent: AVCaptureDevice?](/documentation/avfoundation/avcapturedevice/activeprimaryconstituent)
- [AVCaptureDevice.PrimaryConstituentDeviceSwitchingBehavior](/documentation/avfoundation/avcapturedevice/primaryconstituentdeviceswitchingbehavior-swift.enum)

##### Switching behaviors

- [case unsupported](/documentation/avfoundation/avcapturedevice/primaryconstituentdeviceswitchingbehavior-swift.enum/unsupported)
- [case auto](/documentation/avfoundation/avcapturedevice/primaryconstituentdeviceswitchingbehavior-swift.enum/auto)
- [case restricted](/documentation/avfoundation/avcapturedevice/primaryconstituentdeviceswitchingbehavior-swift.enum/restricted)
- [case locked](/documentation/avfoundation/avcapturedevice/primaryconstituentdeviceswitchingbehavior-swift.enum/locked)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/primaryconstituentdeviceswitchingbehavior-swift.enum/init(rawvalue:))
- [AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions](/documentation/avfoundation/avcapturedevice/primaryconstituentdevicerestrictedswitchingbehaviorconditions-swift.struct)

##### Switching behavior conditions

- [static var exposureModeChanged: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions](/documentation/avfoundation/avcapturedevice/primaryconstituentdevicerestrictedswitchingbehaviorconditions-swift.struct/exposuremodechanged)
- [static var focusModeChanged: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions](/documentation/avfoundation/avcapturedevice/primaryconstituentdevicerestrictedswitchingbehaviorconditions-swift.struct/focusmodechanged)
- [static var videoZoomChanged: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions](/documentation/avfoundation/avcapturedevice/primaryconstituentdevicerestrictedswitchingbehaviorconditions-swift.struct/videozoomchanged)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avcapturedevice/primaryconstituentdevicerestrictedswitchingbehaviorconditions-swift.struct/init(rawvalue:))
- [var supportedFallbackPrimaryConstituentDevices: [AVCaptureDevice]](/documentation/avfoundation/avcapturedevice/supportedfallbackprimaryconstituentdevices)
- [var fallbackPrimaryConstituentDevices: [AVCaptureDevice]](/documentation/avfoundation/avcapturedevice/fallbackprimaryconstituentdevices)

#### Configuring macOS features

- [macOS capture features](/documentation/avfoundation/macos-capture-features)

##### Controlling transport behavior

- [var transportControlsSupported: Bool](/documentation/avfoundation/avcapturedevice/transportcontrolssupported)
- [var transportControlsPlaybackMode: AVCaptureDevice.TransportControlsPlaybackMode](/documentation/avfoundation/avcapturedevice/transportcontrolsplaybackmode-swift.property)
- [func setTransportControlsPlaybackMode(AVCaptureDevice.TransportControlsPlaybackMode, speed: AVCaptureDevice.TransportControlsSpeed)](/documentation/avfoundation/avcapturedevice/settransportcontrolsplaybackmode(_:speed:))
- [AVCaptureDevice.TransportControlsPlaybackMode](/documentation/avfoundation/avcapturedevice/transportcontrolsplaybackmode-swift.enum)

###### Playback modes

- [case notPlaying](/documentation/avfoundation/avcapturedevice/transportcontrolsplaybackmode-swift.enum/notplaying)
- [case playing](/documentation/avfoundation/avcapturedevice/transportcontrolsplaybackmode-swift.enum/playing)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/transportcontrolsplaybackmode-swift.enum/init(rawvalue:))
- [var transportControlsSpeed: AVCaptureDevice.TransportControlsSpeed](/documentation/avfoundation/avcapturedevice/transportcontrolsspeed-swift.property)
- [AVCaptureDevice.TransportControlsSpeed](/documentation/avfoundation/avcapturedevice/transportcontrolsspeed-swift.typealias)

##### Configuring input sources

- [var inputSources: [AVCaptureDevice.InputSource]](/documentation/avfoundation/avcapturedevice/inputsources)
- [var activeInputSource: AVCaptureDevice.InputSource?](/documentation/avfoundation/avcapturedevice/activeinputsource)
- [AVCaptureDevice.InputSource](/documentation/avfoundation/avcapturedevice/inputsource)

###### Accessing properties

- [var inputSourceID: String](/documentation/avfoundation/avcapturedevice/inputsource/inputsourceid)
- [var localizedName: String](/documentation/avfoundation/avcapturedevice/inputsource/localizedname)

##### Accessing linked devices

- [var linkedDevices: [AVCaptureDevice]](/documentation/avfoundation/avcapturedevice/linkeddevices)

#### Accessing camera extrinsics

- [class func extrinsicMatrix(from: AVCaptureDevice, to: AVCaptureDevice) -> Data?](/documentation/avfoundation/avcapturedevice/extrinsicmatrix(from:to:))

#### Accessing the focal length

- [var nominalFocalLengthIn35mmFilm: Float](/documentation/avfoundation/avcapturedevice/nominalfocallengthin35mmfilm)

#### Determining lens stabilization

- [AVCaptureDevice.LensStabilizationStatus](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus)

##### Lens stabilization values

- [case unsupported](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/unsupported)
- [case off](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/off)
- [case active](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/active)
- [case outOfRange](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/outofrange)
- [case unavailable](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/unavailable)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/init(rawvalue:))

#### Configuring lens smudge detection

- [var isCameraLensSmudgeDetectionEnabled: Bool](/documentation/avfoundation/avcapturedevice/iscameralenssmudgedetectionenabled)
- [func setCameraLensSmudgeDetectionEnabled(Bool, detectionInterval: CMTime)](/documentation/avfoundation/avcapturedevice/setcameralenssmudgedetectionenabled(_:detectioninterval:))
- [var cameraLensSmudgeDetectionInterval: CMTime](/documentation/avfoundation/avcapturedevice/cameralenssmudgedetectioninterval)
- [var cameraLensSmudgeDetectionStatus: AVCaptureCameraLensSmudgeDetectionStatus](/documentation/avfoundation/avcapturedevice/cameralenssmudgedetectionstatus)
- [AVCaptureCameraLensSmudgeDetectionStatus](/documentation/avfoundation/avcapturecameralenssmudgedetectionstatus)

##### Status values

- [case disabled](/documentation/avfoundation/avcapturecameralenssmudgedetectionstatus/disabled)
- [case smudgeNotDetected](/documentation/avfoundation/avcapturecameralenssmudgedetectionstatus/smudgenotdetected)
- [case smudged](/documentation/avfoundation/avcapturecameralenssmudgedetectionstatus/smudged)
- [case unknown](/documentation/avfoundation/avcapturecameralenssmudgedetectionstatus/unknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturecameralenssmudgedetectionstatus/init(rawvalue:))

#### Synchronizing with external devices

- [var isFollowingExternalSyncDevice: Bool](/documentation/avfoundation/avcapturedevice/isfollowingexternalsyncdevice)
- [var minSupportedExternalSyncFrameDuration: CMTime](/documentation/avfoundation/avcapturedevice/minsupportedexternalsyncframeduration)
- [var isVideoFrameDurationLocked: Bool](/documentation/avfoundation/avcapturedevice/isvideoframedurationlocked)
- [var minSupportedLockedVideoFrameDuration: CMTime](/documentation/avfoundation/avcapturedevice/minsupportedlockedvideoframeduration)

#### Type Properties

- [class var isEdgeLightActive: Bool](/documentation/avfoundation/avcapturedevice/isedgelightactive)
- [class var isEdgeLightEnabled: Bool](/documentation/avfoundation/avcapturedevice/isedgelightenabled)
- [AVCaptureDeviceInput](/documentation/avfoundation/avcapturedeviceinput)

#### Creating an input

- [init(device: AVCaptureDevice) throws](/documentation/avfoundation/avcapturedeviceinput/init(device:))

#### Configuring video properties

- [var unifiedAutoExposureDefaultsEnabled: Bool](/documentation/avfoundation/avcapturedeviceinput/unifiedautoexposuredefaultsenabled)
- [var videoMinFrameDurationOverride: CMTime](/documentation/avfoundation/avcapturedeviceinput/videominframedurationoverride)

#### Configuring audio properties

- [func isMultichannelAudioModeSupported(AVCaptureMultichannelAudioMode) -> Bool](/documentation/avfoundation/avcapturedeviceinput/ismultichannelaudiomodesupported(_:))
- [var multichannelAudioMode: AVCaptureMultichannelAudioMode](/documentation/avfoundation/avcapturedeviceinput/multichannelaudiomode)
- [AVCaptureMultichannelAudioMode](/documentation/avfoundation/avcapturemultichannelaudiomode)

##### Modes

- [case none](/documentation/avfoundation/avcapturemultichannelaudiomode/none)
- [case stereo](/documentation/avfoundation/avcapturemultichannelaudiomode/stereo)
- [case firstOrderAmbisonics](/documentation/avfoundation/avcapturemultichannelaudiomode/firstorderambisonics)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturemultichannelaudiomode/init(rawvalue:))
- [var isWindNoiseRemovalSupported: Bool](/documentation/avfoundation/avcapturedeviceinput/iswindnoiseremovalsupported)
- [var isWindNoiseRemovalEnabled: Bool](/documentation/avfoundation/avcapturedeviceinput/iswindnoiseremovalenabled)

#### Configuring Cinematic video capture

- [var isCinematicVideoCaptureSupported: Bool](/documentation/avfoundation/avcapturedeviceinput/iscinematicvideocapturesupported)
- [var isCinematicVideoCaptureEnabled: Bool](/documentation/avfoundation/avcapturedeviceinput/iscinematicvideocaptureenabled)
- [var simulatedAperture: Float](/documentation/avfoundation/avcapturedeviceinput/simulatedaperture)

#### Locking frame duration

- [var activeLockedVideoFrameDuration: CMTime](/documentation/avfoundation/avcapturedeviceinput/activelockedvideoframeduration)
- [var isLockedVideoFrameDurationSupported: Bool](/documentation/avfoundation/avcapturedeviceinput/islockedvideoframedurationsupported)

#### Synchronizing with external devices

- [var isExternalSyncSupported: Bool](/documentation/avfoundation/avcapturedeviceinput/isexternalsyncsupported)
- [func follow(AVExternalSyncDevice, videoFrameDuration: CMTime, delegate: (any AVExternalSyncDeviceDelegate)?)](/documentation/avfoundation/avcapturedeviceinput/follow(_:videoframeduration:delegate:))
- [func unfollowExternalSyncDevice()](/documentation/avfoundation/avcapturedeviceinput/unfollowexternalsyncdevice())
- [var activeExternalSyncVideoFrameDuration: CMTime](/documentation/avfoundation/avcapturedeviceinput/activeexternalsyncvideoframeduration)
- [var externalSyncDevice: AVExternalSyncDevice?](/documentation/avfoundation/avcapturedeviceinput/externalsyncdevice)

#### Accessing the device

- [var device: AVCaptureDevice](/documentation/avfoundation/avcapturedeviceinput/device)
- [func ports(for: AVMediaType?, sourceDeviceType: AVCaptureDevice.DeviceType?, sourceDevicePosition: AVCaptureDevice.Position) -> [AVCaptureInput.Port]](/documentation/avfoundation/avcapturedeviceinput/ports(for:sourcedevicetype:sourcedeviceposition:))
- [AVContinuityDevice](/documentation/avfoundation/avcontinuitydevice)

#### Checking a continuity device’s availability

- [var isConnected: Bool](/documentation/avfoundation/avcontinuitydevice/isconnected)

#### Retrieving video devices from a continuity device

- [var videoDevices: [AVCaptureDevice]](/documentation/avfoundation/avcontinuitydevice/videodevices)

#### Retrieving audio ports from a continuity device

- [var audioSessionInputs: [AVAudioSessionPortDescription]](/documentation/avfoundation/avcontinuitydevice/audiosessioninputs)

#### Identifying a continuity device

- [var connectionID: UUID](/documentation/avfoundation/avcontinuitydevice/connectionid)
- [AVExternalStorageDevice](/documentation/avfoundation/avexternalstoragedevice)

#### Checking permission to generate URLs

- [class var authorizationStatus: AVAuthorizationStatus](/documentation/avfoundation/avexternalstoragedevice/authorizationstatus)

#### Requesting permission to generate URLs

- [class func requestAccess(completionHandler: (Bool) -> Void)](/documentation/avfoundation/avexternalstoragedevice/requestaccess(completionhandler:))

#### Generating URLs for image assets

- [func nextAvailableURLs(withPathExtensions: [String]) throws -> [URL]](/documentation/avfoundation/avexternalstoragedevice/nextavailableurls(withpathextensions:))

#### Inspecting a storage device

- [var isConnected: Bool](/documentation/avfoundation/avexternalstoragedevice/isconnected)
- [var displayName: String?](/documentation/avfoundation/avexternalstoragedevice/displayname)
- [var uuid: UUID?](/documentation/avfoundation/avexternalstoragedevice/uuid)
- [var freeSize: Int](/documentation/avfoundation/avexternalstoragedevice/freesize)
- [var totalSize: Int](/documentation/avfoundation/avexternalstoragedevice/totalsize)
- [var isNotRecommendedForCaptureUse: Bool](/documentation/avfoundation/avexternalstoragedevice/isnotrecommendedforcaptureuse)
- [AVExternalStorageDeviceDiscoverySession](/documentation/avfoundation/avexternalstoragedevicediscoverysession)

#### Checking for session support on a device

- [class var isSupported: Bool](/documentation/avfoundation/avexternalstoragedevicediscoverysession/issupported)

#### Retrieving the shared device discovery session instance

- [class var shared: AVExternalStorageDeviceDiscoverySession?](/documentation/avfoundation/avexternalstoragedevicediscoverysession/shared)

#### Monitoring for storage device updates

- [var externalStorageDevices: [AVExternalStorageDevice]](/documentation/avfoundation/avexternalstoragedevicediscoverysession/externalstoragedevices)

### Capture preview

- [AVCaptureVideoPreviewLayer](/documentation/avfoundation/avcapturevideopreviewlayer)

#### Creating a preview layer

- [init(session: AVCaptureSession)](/documentation/avfoundation/avcapturevideopreviewlayer/init(session:))
- [init(sessionWithNoConnection: AVCaptureSession)](/documentation/avfoundation/avcapturevideopreviewlayer/init(sessionwithnoconnection:))

#### Layer configuration

- [var isPreviewing: Bool](/documentation/avfoundation/avcapturevideopreviewlayer/ispreviewing)
- [var videoGravity: AVLayerVideoGravity](/documentation/avfoundation/avcapturevideopreviewlayer/videogravity)

#### Configuring deferred start

- [var isDeferredStartSupported: Bool](/documentation/avfoundation/avcapturevideopreviewlayer/isdeferredstartsupported)
- [var isDeferredStartEnabled: Bool](/documentation/avfoundation/avcapturevideopreviewlayer/isdeferredstartenabled)

#### Session configuration

- [var session: AVCaptureSession?](/documentation/avfoundation/avcapturevideopreviewlayer/session)
- [var connection: AVCaptureConnection?](/documentation/avfoundation/avcapturevideopreviewlayer/connection)
- [func setSessionWithNoConnection(AVCaptureSession)](/documentation/avfoundation/avcapturevideopreviewlayer/setsessionwithnoconnection(_:))

#### Converting between coordinate spaces

- [func layerPointConverted(fromCaptureDevicePoint: CGPoint) -> CGPoint](/documentation/avfoundation/avcapturevideopreviewlayer/layerpointconverted(fromcapturedevicepoint:))
- [func captureDevicePointConverted(fromLayerPoint: CGPoint) -> CGPoint](/documentation/avfoundation/avcapturevideopreviewlayer/capturedevicepointconverted(fromlayerpoint:))
- [func layerRectConverted(fromMetadataOutputRect: CGRect) -> CGRect](/documentation/avfoundation/avcapturevideopreviewlayer/layerrectconverted(frommetadataoutputrect:))
- [func metadataOutputRectConverted(fromLayerRect: CGRect) -> CGRect](/documentation/avfoundation/avcapturevideopreviewlayer/metadataoutputrectconverted(fromlayerrect:))
- [func transformedMetadataObject(for: AVMetadataObject) -> AVMetadataObject?](/documentation/avfoundation/avcapturevideopreviewlayer/transformedmetadataobject(for:))

#### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avcapturevideopreviewlayer-deprecated-symbols)
- [AVCaptureAudioPreviewOutput](/documentation/avfoundation/avcaptureaudiopreviewoutput)

#### Creating preview output

- [init()](/documentation/avfoundation/avcaptureaudiopreviewoutput/init())

#### Configuring the output

- [var volume: Float](/documentation/avfoundation/avcaptureaudiopreviewoutput/volume)
- [var outputDeviceUniqueID: String?](/documentation/avfoundation/avcaptureaudiopreviewoutput/outputdeviceuniqueid)

### Continuity Camera

- [Supporting Continuity Camera in your tvOS app](/documentation/avkit/supporting-continuity-camera-in-your-tvos-app)
- [Supporting Continuity Camera in your macOS app](/documentation/avfoundation/supporting-continuity-camera-in-your-macos-app)
- [AVCaptureDeskViewApplication](/documentation/avfoundation/avcapturedeskviewapplication)

#### Presenting the Desk View app

- [func present(completionHandler: (((any Error)?) -> Void)?)](/documentation/avfoundation/avcapturedeskviewapplication/present(completionhandler:))
- [func present(launchConfiguration: AVCaptureDeskViewApplication.LaunchConfiguration, completionHandler: (((any Error)?) -> Void)?)](/documentation/avfoundation/avcapturedeskviewapplication/present(launchconfiguration:completionhandler:))
- [AVCaptureDeskViewApplication.LaunchConfiguration](/documentation/avfoundation/avcapturedeskviewapplication/launchconfiguration)

##### Customizing the presentation

- [var mainWindowFrame: CGRect](/documentation/avfoundation/avcapturedeskviewapplication/launchconfiguration/mainwindowframe)
- [var requiresSetUpModeCompletion: Bool](/documentation/avfoundation/avcapturedeskviewapplication/launchconfiguration/requiressetupmodecompletion)

### Capture controls

- [Enhancing your app experience with the Camera Control](/documentation/avfoundation/enhancing-your-app-experience-with-the-camera-control)
- [AVCaptureControl](/documentation/avfoundation/avcapturecontrol)

#### Setting the enabled state

- [var isEnabled: Bool](/documentation/avfoundation/avcapturecontrol/isenabled)
- [AVCaptureSystemZoomSlider](/documentation/avfoundation/avcapturesystemzoomslider)

#### Creating a zoom slider

- [init(device: AVCaptureDevice)](/documentation/avfoundation/avcapturesystemzoomslider/init(device:))
- [init(device: AVCaptureDevice, action: (CGFloat) -> Void)](/documentation/avfoundation/avcapturesystemzoomslider/init(device:action:))
- [AVCaptureSystemExposureBiasSlider](/documentation/avfoundation/avcapturesystemexposurebiasslider)

#### Creating an exposure bias slider

- [init(device: AVCaptureDevice)](/documentation/avfoundation/avcapturesystemexposurebiasslider/init(device:))
- [init(device: AVCaptureDevice, action: (Float) -> Void)](/documentation/avfoundation/avcapturesystemexposurebiasslider/init(device:action:))
- [AVCaptureSlider](/documentation/avfoundation/avcaptureslider)

#### Creating a slider

- [convenience init(String, symbolName: String, in: ClosedRange<Float>)](/documentation/avfoundation/avcaptureslider/init(_:symbolname:in:))
- [convenience init(String, symbolName: String, in: ClosedRange<Float>, step: Float)](/documentation/avfoundation/avcaptureslider/init(_:symbolname:in:step:))
- [convenience init(String, symbolName: String, values: [Float])](/documentation/avfoundation/avcaptureslider/init(_:symbolname:values:))

#### Handling interaction

- [func setActionQueue(DispatchQueue, action: (Float) -> ())](/documentation/avfoundation/avcaptureslider/setactionqueue(_:action:))

#### Accessing the control value

- [var value: Float](/documentation/avfoundation/avcaptureslider/value)
- [var prominentValues: [Float]](/documentation/avfoundation/avcaptureslider/prominentvalues-199dz)
- [var localizedValueFormat: String?](/documentation/avfoundation/avcaptureslider/localizedvalueformat)

#### Setting an accessibility identifier

- [var accessibilityIdentifier: String?](/documentation/avfoundation/avcaptureslider/accessibilityidentifier)

#### Inspecting presentation attributes

- [var symbolName: String](/documentation/avfoundation/avcaptureslider/symbolname)
- [var localizedTitle: String](/documentation/avfoundation/avcaptureslider/localizedtitle)
- [AVCaptureIndexPicker](/documentation/avfoundation/avcaptureindexpicker)

#### Creating an index picker

- [init(String, symbolName: String, numberOfIndexes: Int)](/documentation/avfoundation/avcaptureindexpicker/init(_:symbolname:numberofindexes:))
- [init(String, symbolName: String, numberOfIndexes: Int, localizedTitleTransform: (Int) -> String)](/documentation/avfoundation/avcaptureindexpicker/init(_:symbolname:numberofindexes:localizedtitletransform:))
- [init(String, symbolName: String, localizedIndexTitles: [String])](/documentation/avfoundation/avcaptureindexpicker/init(_:symbolname:localizedindextitles:))

#### Handling interaction

- [func setActionQueue(DispatchQueue, action: (Int) -> ())](/documentation/avfoundation/avcaptureindexpicker/setactionqueue(_:action:))

#### Accessing the control value

- [var selectedIndex: Int](/documentation/avfoundation/avcaptureindexpicker/selectedindex)
- [var numberOfIndexes: Int](/documentation/avfoundation/avcaptureindexpicker/numberofindexes)

#### Setting an accessibility identifier

- [var accessibilityIdentifier: String?](/documentation/avfoundation/avcaptureindexpicker/accessibilityidentifier)

#### Inspecting presentation attributes

- [var symbolName: String](/documentation/avfoundation/avcaptureindexpicker/symbolname)
- [var localizedTitle: String](/documentation/avfoundation/avcaptureindexpicker/localizedtitle)
- [var localizedIndexTitles: [String]](/documentation/avfoundation/avcaptureindexpicker/localizedindextitles)

### External display output

- [AVCaptureExternalDisplayConfiguration](/documentation/avfoundation/avcaptureexternaldisplayconfiguration)

#### Modifying the configuration

- [var bypassColorSpaceConversion: Bool](/documentation/avfoundation/avcaptureexternaldisplayconfiguration/bypasscolorspaceconversion)
- [var preferredResolution: CMVideoDimensions](/documentation/avfoundation/avcaptureexternaldisplayconfiguration/preferredresolution)
- [var shouldMatchFrameRate: Bool](/documentation/avfoundation/avcaptureexternaldisplayconfiguration/shouldmatchframerate)
- [AVCaptureExternalDisplayConfigurator](/documentation/avfoundation/avcaptureexternaldisplayconfigurator)

#### Determining configuration support

- [class var isMatchingFrameRateSupported: Bool](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/ismatchingframeratesupported)
- [class var isPreferredResolutionSupported: Bool](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/ispreferredresolutionsupported)
- [class var isBypassingColorSpaceConversionSupported: Bool](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/isbypassingcolorspaceconversionsupported)

#### Creating an external display configurator

- [init(device: AVCaptureDevice, previewLayer: CALayer, configuration: AVCaptureExternalDisplayConfiguration)](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/init(device:previewlayer:configuration:))

#### Inspecting the configurator

- [var activeExternalDisplayFrameRate: Double](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/activeexternaldisplayframerate)
- [var device: AVCaptureDevice?](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/device)
- [var isActive: Bool](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/isactive)
- [var previewLayer: CALayer?](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/previewlayer)

#### Stopping configuration

- [func stop()](/documentation/avfoundation/avcaptureexternaldisplayconfigurator/stop())

### Timecode generation

- [AVCaptureTimecodeGenerator](/documentation/avfoundation/avcapturetimecodegenerator)

#### Generating timecode

- [func generateInitialTimecode() -> AVCaptureTimecode](/documentation/avfoundation/avcapturetimecodegenerator/generateinitialtimecode())

#### Managing sources

- [var currentSource: AVCaptureTimecode.Source](/documentation/avfoundation/avcapturetimecodegenerator/currentsource)
- [var availableSources: [AVCaptureTimecode.Source]](/documentation/avfoundation/avcapturetimecodegenerator/availablesources)
- [class var frameCountSource: AVCaptureTimecode.Source](/documentation/avfoundation/avcapturetimecodegenerator/framecountsource)
- [class var realTimeClockSource: AVCaptureTimecode.Source](/documentation/avfoundation/avcapturetimecodegenerator/realtimeclocksource)
- [func startSynchronization(source: AVCaptureTimecode.Source)](/documentation/avfoundation/avcapturetimecodegenerator/startsynchronization(source:))

#### Configuring the generator

- [var synchronizationTimeout: TimeInterval](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationtimeout)
- [var timecodeAlignmentOffset: TimeInterval](/documentation/avfoundation/avcapturetimecodegenerator/timecodealignmentoffset)
- [var timecodeFrameDuration: CMTime](/documentation/avfoundation/avcapturetimecodegenerator/timecodeframeduration)
- [func setDelegate((any AVCaptureTimecodeGeneratorDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avcapturetimecodegenerator/setdelegate(_:queue:))

#### Handling delegate callbacks

- [var delegate: (any AVCaptureTimecodeGeneratorDelegate)?](/documentation/avfoundation/avcapturetimecodegenerator/delegate)
- [var delegateCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcapturetimecodegenerator/delegatecallbackqueue)
- [AVCaptureTimecodeGeneratorDelegate](/documentation/avfoundation/avcapturetimecodegeneratordelegate)

#### Responding to timecode events

- [func timecodeGenerator(AVCaptureTimecodeGenerator, didReceiveUpdate: AVCaptureTimecode, from: AVCaptureTimecode.Source)](/documentation/avfoundation/avcapturetimecodegeneratordelegate/timecodegenerator(_:didreceiveupdate:from:))
- [func timecodeGenerator(AVCaptureTimecodeGenerator, didUpdateAvailableSources: [AVCaptureTimecode.Source])](/documentation/avfoundation/avcapturetimecodegeneratordelegate/timecodegenerator(_:didupdateavailablesources:))
- [func timecodeGenerator(AVCaptureTimecodeGenerator, transitionedTo: AVCaptureTimecodeGenerator.SynchronizationStatus, for: AVCaptureTimecode.Source)](/documentation/avfoundation/avcapturetimecodegeneratordelegate/timecodegenerator(_:transitionedto:for:))
- [AVCaptureTimecodeGenerator.SynchronizationStatus](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus)

##### Status values

- [case notRequired](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/notrequired)
- [case sourceSelected](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/sourceselected)
- [case sourceUnavailable](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/sourceunavailable)
- [case sourceUnsupported](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/sourceunsupported)
- [case synchronized](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/synchronized)
- [case synchronizing](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/synchronizing)
- [case timedOut](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/timedout)
- [case unknown](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/unknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/init(rawvalue:))
- [AVCaptureTimecodeGenerator.SynchronizationStatus](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus)

#### Status values

- [case notRequired](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/notrequired)
- [case sourceSelected](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/sourceselected)
- [case sourceUnavailable](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/sourceunavailable)
- [case sourceUnsupported](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/sourceunsupported)
- [case synchronized](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/synchronized)
- [case synchronizing](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/synchronizing)
- [case timedOut](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/timedout)
- [case unknown](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturetimecodegenerator/synchronizationstatus/init(rawvalue:))
- [AVCaptureTimecode.Source](/documentation/avfoundation/avcapturetimecode/source)

#### Inspecting the source

- [var displayName: String](/documentation/avfoundation/avcapturetimecode/source/displayname)
- [var type: AVCaptureTimecode.SourceType](/documentation/avfoundation/avcapturetimecode/source/type)
- [var uuid: UUID](/documentation/avfoundation/avcapturetimecode/source/uuid)
- [AVCaptureTimecode.SourceType](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum)

#### Source types

- [case external](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/external)
- [case frameCount](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/framecount)
- [case realTimeClock](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/realtimeclock)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/init(rawvalue:))
- [AVCaptureTimecode](/documentation/avfoundation/avcapturetimecode)

#### Accessing timecode components

- [var frameDuration: CMTime](/documentation/avfoundation/avcapturetimecode/frameduration)
- [var frames: UInt8](/documentation/avfoundation/avcapturetimecode/frames)
- [var hours: UInt8](/documentation/avfoundation/avcapturetimecode/hours)
- [var minutes: UInt8](/documentation/avfoundation/avcapturetimecode/minutes)
- [var seconds: UInt8](/documentation/avfoundation/avcapturetimecode/seconds)
- [var userBits: UInt32](/documentation/avfoundation/avcapturetimecode/userbits)

#### Working with sources

- [var sourceType: AVCaptureTimecode.SourceType](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.property)
- [AVCaptureTimecode.SourceType](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum)

##### Source types

- [case external](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/external)
- [case frameCount](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/framecount)
- [case realTimeClock](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/realtimeclock)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturetimecode/sourcetype-swift.enum/init(rawvalue:))
- [AVCaptureTimecode.Source](/documentation/avfoundation/avcapturetimecode/source)

##### Inspecting the source

- [var displayName: String](/documentation/avfoundation/avcapturetimecode/source/displayname)
- [var type: AVCaptureTimecode.SourceType](/documentation/avfoundation/avcapturetimecode/source/type)
- [var uuid: UUID](/documentation/avfoundation/avcapturetimecode/source/uuid)

#### Manipulating timecodes

- [static func advanced(AVCaptureTimecode, by: Int64) -> AVCaptureTimecode](/documentation/avfoundation/avcapturetimecode/advanced(_:by:))

#### Creating metadata sample buffers

- [static func createMetadataSampleBuffer(from: AVCaptureTimecode, associatedWithPresentationTimeStamp: CMTime) -> Unmanaged<CMSampleBuffer>?](/documentation/avfoundation/avcapturetimecode/createmetadatasamplebuffer(from:associatedwithpresentationtimestamp:))
- [static func createMetadataSampleBuffer(from: AVCaptureTimecode, forDuration: CMTime) -> Unmanaged<CMSampleBuffer>?](/documentation/avfoundation/avcapturetimecode/createmetadatasamplebuffer(from:forduration:))

#### Initializers

- [init()](/documentation/avfoundation/avcapturetimecode/init())
- [init(hours: UInt8, minutes: UInt8, seconds: UInt8, frames: UInt8, userBits: UInt32, frameDuration: CMTime, sourceType: AVCaptureTimecode.SourceType)](/documentation/avfoundation/avcapturetimecode/init(hours:minutes:seconds:frames:userbits:frameduration:sourcetype:))
- [static func advanced(AVCaptureTimecode, by: Int64) -> AVCaptureTimecode](/documentation/avfoundation/avcapturetimecode/advanced(_:by:))
- [static func createMetadataSampleBuffer(from: AVCaptureTimecode, associatedWithPresentationTimeStamp: CMTime) -> Unmanaged<CMSampleBuffer>?](/documentation/avfoundation/avcapturetimecode/createmetadatasamplebuffer(from:associatedwithpresentationtimestamp:))
- [static func createMetadataSampleBuffer(from: AVCaptureTimecode, forDuration: CMTime) -> Unmanaged<CMSampleBuffer>?](/documentation/avfoundation/avcapturetimecode/createmetadatasamplebuffer(from:forduration:))

### External synchronization

- [AVExternalSyncDevice](/documentation/avfoundation/avexternalsyncdevice)

#### Finding and monitoring devices

- [AVExternalSyncDevice.DiscoverySession](/documentation/avfoundation/avexternalsyncdevice/discoverysession)

##### Accessing the shared instance

- [class var shared: AVExternalSyncDevice.DiscoverySession?](/documentation/avfoundation/avexternalsyncdevice/discoverysession/shared)
- [class var isSupported: Bool](/documentation/avfoundation/avexternalsyncdevice/discoverysession/issupported)

##### Finding devices

- [var devices: [AVExternalSyncDevice]](/documentation/avfoundation/avexternalsyncdevice/discoverysession/devices)

#### Inspecting a device

- [var clock: CMClock?](/documentation/avfoundation/avexternalsyncdevice/clock)
- [var productID: UInt32](/documentation/avfoundation/avexternalsyncdevice/productid)
- [var signalCompensationDelay: CMTime](/documentation/avfoundation/avexternalsyncdevice/signalcompensationdelay)
- [var status: AVExternalSyncDeviceStatus](/documentation/avfoundation/avexternalsyncdevice/status)
- [var uuid: UUID](/documentation/avfoundation/avexternalsyncdevice/uuid)
- [var vendorID: UInt32](/documentation/avfoundation/avexternalsyncdevice/vendorid)
- [AVExternalSyncDeviceDelegate](/documentation/avfoundation/avexternalsyncdevicedelegate)

#### Responding to device events

- [func externalSyncDevice(AVExternalSyncDevice, failedWithError: (any Error)?)](/documentation/avfoundation/avexternalsyncdevicedelegate/externalsyncdevice(_:failedwitherror:))
- [func externalSyncDeviceStatusDidChange(AVExternalSyncDevice)](/documentation/avfoundation/avexternalsyncdevicedelegate/externalsyncdevicestatusdidchange(_:))
- [AVExternalSyncDeviceStatus](/documentation/avfoundation/avexternalsyncdevicestatus)

#### Status values

- [case activeSync](/documentation/avfoundation/avexternalsyncdevicestatus/activesync)
- [case calibrating](/documentation/avfoundation/avexternalsyncdevicestatus/calibrating)
- [case freeRunSync](/documentation/avfoundation/avexternalsyncdevicestatus/freerunsync)
- [case ready](/documentation/avfoundation/avexternalsyncdevicestatus/ready)
- [case unavailable](/documentation/avfoundation/avexternalsyncdevicestatus/unavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avexternalsyncdevicestatus/init(rawvalue:))
- [AVExternalSyncDevice.DiscoverySession](/documentation/avfoundation/avexternalsyncdevice/discoverysession)

#### Accessing the shared instance

- [class var shared: AVExternalSyncDevice.DiscoverySession?](/documentation/avfoundation/avexternalsyncdevice/discoverysession/shared)
- [class var isSupported: Bool](/documentation/avfoundation/avexternalsyncdevice/discoverysession/issupported)

#### Finding devices

- [var devices: [AVExternalSyncDevice]](/documentation/avfoundation/avexternalsyncdevice/discoverysession/devices)
- [Photo capture](/documentation/avfoundation/photo-capture)

### Photo capture

- [Capturing consistent color images](/documentation/avfoundation/capturing-consistent-color-images)
- [Capturing still and Live Photos](/documentation/avfoundation/capturing-still-and-live-photos)

#### Next steps

- [Saving captured photos](/documentation/avfoundation/saving-captured-photos)
- [Tracking photo capture progress](/documentation/avfoundation/tracking-photo-capture-progress)
- [Capturing and saving Live Photos](/documentation/avfoundation/capturing-and-saving-live-photos)

#### More capture options

- [Capturing photos with depth](/documentation/avfoundation/capturing-photos-with-depth)
- [Capturing a bracketed photo sequence](/documentation/avfoundation/capturing-a-bracketed-photo-sequence)
- [Capturing uncompressed image data](/documentation/avfoundation/capturing-uncompressed-image-data)
- [Capturing thumbnail and preview images](/documentation/avfoundation/capturing-thumbnail-and-preview-images)
- [Capturing photos in RAW and Apple ProRAW formats](/documentation/avfoundation/capturing-photos-in-raw-and-apple-proraw-formats)
- [Supporting Continuity Camera in Your Mac App](/documentation/appkit/supporting-continuity-camera-in-your-mac-app)
- [AVCapturePhoto](/documentation/avfoundation/avcapturephoto)

#### Resolving photo capture requests

- [var resolvedSettings: AVCaptureResolvedPhotoSettings](/documentation/avfoundation/avcapturephoto/resolvedsettings)
- [var photoCount: Int](/documentation/avfoundation/avcapturephoto/photocount)
- [var timestamp: CMTime](/documentation/avfoundation/avcapturephoto/timestamp)

#### Accessing photo pixel data

- [var isRawPhoto: Bool](/documentation/avfoundation/avcapturephoto/israwphoto)
- [var pixelBuffer: CVPixelBuffer?](/documentation/avfoundation/avcapturephoto/pixelbuffer)

#### Accessing preview photo data

- [var embeddedThumbnailPhotoFormat: [String : Any]?](/documentation/avfoundation/avcapturephoto/embeddedthumbnailphotoformat)
- [var previewPixelBuffer: CVPixelBuffer?](/documentation/avfoundation/avcapturephoto/previewpixelbuffer)

#### Accessing photo metadata

- [var depthData: AVDepthData?](/documentation/avfoundation/avcapturephoto/depthdata)
- [var cameraCalibrationData: AVCameraCalibrationData?](/documentation/avfoundation/avcapturephoto/cameracalibrationdata)
- [var sourceDeviceType: AVCaptureDevice.DeviceType?](/documentation/avfoundation/avcapturephoto/sourcedevicetype)
- [var metadata: [String : Any]](/documentation/avfoundation/avcapturephoto/metadata)
- [var portraitEffectsMatte: AVPortraitEffectsMatte?](/documentation/avfoundation/avcapturephoto/portraiteffectsmatte)

#### Packaging data for file output

- [func fileDataRepresentation(with: any AVCapturePhotoFileDataRepresentationCustomizer) -> Data?](/documentation/avfoundation/avcapturephoto/filedatarepresentation(with:))
- [AVCapturePhotoFileDataRepresentationCustomizer](/documentation/avfoundation/avcapturephotofiledatarepresentationcustomizer)

##### Replacing or removing metadata

- [func replacementMetadata(for: AVCapturePhoto) -> [String : Any]?](/documentation/avfoundation/avcapturephotofiledatarepresentationcustomizer/replacementmetadata(for:))
- [func replacementEmbeddedThumbnailPixelBuffer(withPhotoFormat: AutoreleasingUnsafeMutablePointer<NSDictionary?>, for: AVCapturePhoto) -> Unmanaged<CVPixelBuffer>?](/documentation/avfoundation/avcapturephotofiledatarepresentationcustomizer/replacementembeddedthumbnailpixelbuffer(withphotoformat:for:))
- [func replacementDepthData(for: AVCapturePhoto) -> AVDepthData?](/documentation/avfoundation/avcapturephotofiledatarepresentationcustomizer/replacementdepthdata(for:))
- [func replacementPortraitEffectsMatte(for: AVCapturePhoto) -> AVPortraitEffectsMatte?](/documentation/avfoundation/avcapturephotofiledatarepresentationcustomizer/replacementportraiteffectsmatte(for:))
- [func replacementSemanticSegmentationMatte(ofType: AVSemanticSegmentationMatte.MatteType, for: AVCapturePhoto) -> AVSemanticSegmentationMatte?](/documentation/avfoundation/avcapturephotofiledatarepresentationcustomizer/replacementsemanticsegmentationmatte(oftype:for:))
- [func replacementAppleProRAWCompressionSettings(for: AVCapturePhoto, defaultSettings: [String : Any], maximumBitDepth: Int) -> [String : Any]](/documentation/avfoundation/avcapturephotofiledatarepresentationcustomizer/replacementappleprorawcompressionsettings(for:defaultsettings:maximumbitdepth:))
- [func fileDataRepresentation() -> Data?](/documentation/avfoundation/avcapturephoto/filedatarepresentation())
- [func cgImageRepresentation() -> CGImage?](/documentation/avfoundation/avcapturephoto/cgimagerepresentation())
- [func previewCGImageRepresentation() -> CGImage?](/documentation/avfoundation/avcapturephoto/previewcgimagerepresentation())
- [func fileDataRepresentation(withReplacementMetadata: [String : Any]?, replacementEmbeddedThumbnailPhotoFormat: [String : Any]?, replacementEmbeddedThumbnailPixelBuffer: CVPixelBuffer?, replacementDepthData: AVDepthData?) -> Data?](/documentation/avfoundation/avcapturephoto/filedatarepresentation(withreplacementmetadata:replacementembeddedthumbnailphotoformat:replacementembeddedthumbnailpixelbuffer:replacementdepthdata:))

#### Enabling constant color

- [var constantColorCenterWeightedMeanConfidenceLevel: Float](/documentation/avfoundation/avcapturephoto/constantcolorcenterweightedmeanconfidencelevel)
- [var constantColorConfidenceMap: CVPixelBuffer?](/documentation/avfoundation/avcapturephoto/constantcolorconfidencemap)
- [var isConstantColorFallbackPhoto: Bool](/documentation/avfoundation/avcapturephoto/isconstantcolorfallbackphoto)

#### Examining bracketed capture information

- [var bracketSettings: AVCaptureBracketedStillImageSettings?](/documentation/avfoundation/avcapturephoto/bracketsettings)
- [var sequenceCount: Int](/documentation/avfoundation/avcapturephoto/sequencecount)
- [var lensStabilizationStatus: AVCaptureDevice.LensStabilizationStatus](/documentation/avfoundation/avcapturephoto/lensstabilizationstatus)
- [AVCaptureDevice.LensStabilizationStatus](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus)

##### Lens stabilization values

- [case unsupported](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/unsupported)
- [case off](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/off)
- [case active](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/active)
- [case outOfRange](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/outofrange)
- [case unavailable](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/unavailable)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturedevice/lensstabilizationstatus/init(rawvalue:))

#### Accessing segmentation mattes

- [func semanticSegmentationMatte(for: AVSemanticSegmentationMatte.MatteType) -> AVSemanticSegmentationMatte?](/documentation/avfoundation/avcapturephoto/semanticsegmentationmatte(for:))
- [AVCaptureDeferredPhotoProxy](/documentation/avfoundation/avcapturedeferredphotoproxy)
- [AVCapturePhotoOutput](/documentation/avfoundation/avcapturephotooutput)

#### Creating a photo output

- [init()](/documentation/avfoundation/avcapturephotooutput/init())

#### Capturing a photo

- [func capturePhoto(with: AVCapturePhotoSettings, delegate: any AVCapturePhotoCaptureDelegate)](/documentation/avfoundation/avcapturephotooutput/capturephoto(with:delegate:))

#### Managing responsive capture

- [var captureReadiness: AVCapturePhotoOutput.CaptureReadiness](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.property)
- [AVCapturePhotoOutput.CaptureReadiness](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.enum)

##### Readiness states

- [case sessionNotRunning](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.enum/sessionnotrunning)
- [case notReadyMomentarily](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.enum/notreadymomentarily)
- [case notReadyWaitingForCapture](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.enum/notreadywaitingforcapture)
- [case notReadyWaitingForProcessing](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.enum/notreadywaitingforprocessing)
- [case ready](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.enum/ready)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturephotooutput/capturereadiness-swift.enum/init(rawvalue:))
- [var isAutoDeferredPhotoDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isautodeferredphotodeliveryenabled)
- [var isAutoDeferredPhotoDeliverySupported: Bool](/documentation/avfoundation/avcapturephotooutput/isautodeferredphotodeliverysupported)
- [var isFastCapturePrioritizationSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isfastcaptureprioritizationsupported)
- [var isFastCapturePrioritizationEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isfastcaptureprioritizationenabled)
- [var isResponsiveCaptureSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isresponsivecapturesupported)
- [var isResponsiveCaptureEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isresponsivecaptureenabled)
- [var isZeroShutterLagSupported: Bool](/documentation/avfoundation/avcapturephotooutput/iszeroshutterlagsupported)
- [var isZeroShutterLagEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/iszeroshutterlagenabled)

#### Determining supported pixel formats

- [var availablePhotoPixelFormatTypes: [OSType]](/documentation/avfoundation/avcapturephotooutput/availablephotopixelformattypes-3ydgm)
- [var availableRawPhotoPixelFormatTypes: [OSType]](/documentation/avfoundation/avcapturephotooutput/availablerawphotopixelformattypes-9t9k5)
- [func supportedPhotoPixelFormatTypes(for: AVFileType) -> [OSType]](/documentation/avfoundation/avcapturephotooutput/supportedphotopixelformattypes(for:))
- [func supportedRawPhotoPixelFormatTypes(for: AVFileType) -> [OSType]](/documentation/avfoundation/avcapturephotooutput/supportedrawphotopixelformattypes(for:))
- [class func isAppleProRAWPixelFormat(OSType) -> Bool](/documentation/avfoundation/avcapturephotooutput/isappleprorawpixelformat(_:))
- [class func isBayerRAWPixelFormat(OSType) -> Bool](/documentation/avfoundation/avcapturephotooutput/isbayerrawpixelformat(_:))

#### Determining supported codec types

- [var availablePhotoCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturephotooutput/availablephotocodectypes)
- [func supportedPhotoCodecTypes(for: AVFileType) -> [AVVideoCodecType]](/documentation/avfoundation/avcapturephotooutput/supportedphotocodectypes(for:))

#### Determining supported file types

- [var availablePhotoFileTypes: [AVFileType]](/documentation/avfoundation/avcapturephotooutput/availablephotofiletypes)
- [var availableRawPhotoFileTypes: [AVFileType]](/documentation/avfoundation/avcapturephotooutput/availablerawphotofiletypes)

#### Suppressing the shutter sound

- [var isShutterSoundSuppressionSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isshuttersoundsuppressionsupported)

#### Configuring ProRAW support

- [var isAppleProRAWSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isappleprorawsupported)
- [var isAppleProRAWEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isappleprorawenabled)

#### Determining available settings

- [var isContentAwareDistortionCorrectionSupported: Bool](/documentation/avfoundation/avcapturephotooutput/iscontentawaredistortioncorrectionsupported)
- [var isContentAwareDistortionCorrectionEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/iscontentawaredistortioncorrectionenabled)
- [var isLensStabilizationDuringBracketedCaptureSupported: Bool](/documentation/avfoundation/avcapturephotooutput/islensstabilizationduringbracketedcapturesupported)
- [var maxBracketedCapturePhotoCount: Int](/documentation/avfoundation/avcapturephotooutput/maxbracketedcapturephotocount)
- [var supportedFlashModes: [AVCaptureDevice.FlashMode]](/documentation/avfoundation/avcapturephotooutput/supportedflashmodes-1n6nm)
- [var isAutoRedEyeReductionSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isautoredeyereductionsupported)

#### Monitoring the visible scene

- [var isFlashScene: Bool](/documentation/avfoundation/avcapturephotooutput/isflashscene)
- [var photoSettingsForSceneMonitoring: AVCapturePhotoSettings?](/documentation/avfoundation/avcapturephotooutput/photosettingsforscenemonitoring)

#### Configuring high-resolution still capture

- [var maxPhotoDimensions: CMVideoDimensions](/documentation/avfoundation/avcapturephotooutput/maxphotodimensions)

#### Configuring Live Photo capture

- [var isLivePhotoCaptureSupported: Bool](/documentation/avfoundation/avcapturephotooutput/islivephotocapturesupported)
- [var isLivePhotoCaptureEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/islivephotocaptureenabled)
- [var isLivePhotoCaptureSuspended: Bool](/documentation/avfoundation/avcapturephotooutput/islivephotocapturesuspended)
- [var preservesLivePhotoCaptureSuspendedOnSessionStop: Bool](/documentation/avfoundation/avcapturephotooutput/preserveslivephotocapturesuspendedonsessionstop)
- [var isLivePhotoAutoTrimmingEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/islivephotoautotrimmingenabled)
- [var availableLivePhotoVideoCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturephotooutput/availablelivephotovideocodectypes)

#### Configuring depth data capture

- [var isDepthDataDeliverySupported: Bool](/documentation/avfoundation/avcapturephotooutput/isdepthdatadeliverysupported)
- [var isDepthDataDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isdepthdatadeliveryenabled)

#### Configuring Portrait Effects matte capture

- [var isPortraitEffectsMatteDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isportraiteffectsmattedeliveryenabled)
- [var isPortraitEffectsMatteDeliverySupported: Bool](/documentation/avfoundation/avcapturephotooutput/isportraiteffectsmattedeliverysupported)
- [var portraitEffectsMatte: AVPortraitEffectsMatte?](/documentation/avfoundation/avcapturephoto/portraiteffectsmatte)

#### Configuring constant color

- [var isConstantColorSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isconstantcolorsupported)
- [var isConstantColorEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isconstantcolorenabled)

#### Configuring orientation compensation

- [var isCameraSensorOrientationCompensationSupported: Bool](/documentation/avfoundation/avcapturephotooutput/iscamerasensororientationcompensationsupported)
- [var isCameraSensorOrientationCompensationEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/iscamerasensororientationcompensationenabled)

#### Configuring virtual device capture

- [var isVirtualDeviceFusionSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isvirtualdevicefusionsupported)
- [var isVirtualDeviceConstituentPhotoDeliverySupported: Bool](/documentation/avfoundation/avcapturephotooutput/isvirtualdeviceconstituentphotodeliverysupported)
- [var isVirtualDeviceConstituentPhotoDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isvirtualdeviceconstituentphotodeliveryenabled)

#### Preparing for resource-intensive captures

- [var preparedPhotoSettingsArray: [AVCapturePhotoSettings]](/documentation/avfoundation/avcapturephotooutput/preparedphotosettingsarray)
- [func setPreparedPhotoSettingsArray([AVCapturePhotoSettings], completionHandler: ((Bool, (any Error)?) -> Void)?)](/documentation/avfoundation/avcapturephotooutput/setpreparedphotosettingsarray(_:completionhandler:))

#### Getting segmentation mattes

- [var availableSemanticSegmentationMatteTypes: [AVSemanticSegmentationMatte.MatteType]](/documentation/avfoundation/avcapturephotooutput/availablesemanticsegmentationmattetypes)
- [var enabledSemanticSegmentationMatteTypes: [AVSemanticSegmentationMatte.MatteType]](/documentation/avfoundation/avcapturephotooutput/enabledsemanticsegmentationmattetypes)

#### Setting the capture prioritization

- [var maxPhotoQualityPrioritization: AVCapturePhotoOutput.QualityPrioritization](/documentation/avfoundation/avcapturephotooutput/maxphotoqualityprioritization)
- [AVCapturePhotoOutput.QualityPrioritization](/documentation/avfoundation/avcapturephotooutput/qualityprioritization)

##### Specifying priority

- [case speed](/documentation/avfoundation/avcapturephotooutput/qualityprioritization/speed)
- [case quality](/documentation/avfoundation/avcapturephotooutput/qualityprioritization/quality)
- [case balanced](/documentation/avfoundation/avcapturephotooutput/qualityprioritization/balanced)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcapturephotooutput/qualityprioritization/init(rawvalue:))

#### Determining calibration data delivery support

- [var isCameraCalibrationDataDeliverySupported: Bool](/documentation/avfoundation/avcapturephotooutput/iscameracalibrationdatadeliverysupported)

#### Deprecated

- [Deprecated symbols](/documentation/avfoundation/avcapturephotooutput-deprecated-symbols)

##### Getting formatted output

- [class func jpegPhotoDataRepresentation(forJPEGSampleBuffer: CMSampleBuffer, previewPhotoSampleBuffer: CMSampleBuffer?) -> Data?](/documentation/avfoundation/avcapturephotooutput/jpegphotodatarepresentation(forjpegsamplebuffer:previewphotosamplebuffer:))
- [class func dngPhotoDataRepresentation(forRawSampleBuffer: CMSampleBuffer, previewPhotoSampleBuffer: CMSampleBuffer?) -> Data?](/documentation/avfoundation/avcapturephotooutput/dngphotodatarepresentation(forrawsamplebuffer:previewphotosamplebuffer:))

##### Configuring dual camera capture

- [var isDualCameraFusionSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isdualcamerafusionsupported)
- [var isDualCameraDualPhotoDeliverySupported: Bool](/documentation/avfoundation/avcapturephotooutput/isdualcameradualphotodeliverysupported)
- [var isDualCameraDualPhotoDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/isdualcameradualphotodeliveryenabled)

##### Configuring high-resolution still capture

- [var isHighResolutionCaptureEnabled: Bool](/documentation/avfoundation/avcapturephotooutput/ishighresolutioncaptureenabled)

##### Monitoring the visible scene

- [var isStillImageStabilizationScene: Bool](/documentation/avfoundation/avcapturephotooutput/isstillimagestabilizationscene)

##### Determining available settings

- [var isStillImageStabilizationSupported: Bool](/documentation/avfoundation/avcapturephotooutput/isstillimagestabilizationsupported)

#### Instance properties

- [var availableRawPhotoCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturephotooutput/availablerawphotocodectypes)

#### Instance methods

- [func supportedRawPhotoCodecTypes(forRawPhotoPixelFormatType: OSType, fileType: AVFileType) -> [AVVideoCodecType]](/documentation/avfoundation/avcapturephotooutput/supportedrawphotocodectypes(forrawphotopixelformattype:filetype:))
- [AVCapturePhotoCaptureDelegate](/documentation/avfoundation/avcapturephotocapturedelegate)

#### Monitoring capture progress

- [func photoOutput(AVCapturePhotoOutput, willBeginCaptureFor: AVCaptureResolvedPhotoSettings)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:willbegincapturefor:))
- [func photoOutput(AVCapturePhotoOutput, willCapturePhotoFor: AVCaptureResolvedPhotoSettings)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:willcapturephotofor:))
- [func photoOutput(AVCapturePhotoOutput, didCapturePhotoFor: AVCaptureResolvedPhotoSettings)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didcapturephotofor:))
- [func photoOutput(AVCapturePhotoOutput, didFinishCaptureFor: AVCaptureResolvedPhotoSettings, error: (any Error)?)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didfinishcapturefor:error:))

#### Receiving capture results

- [func photoOutput(AVCapturePhotoOutput, didFinishProcessingPhoto: AVCapturePhoto, error: (any Error)?)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didfinishprocessingphoto:error:))
- [func photoOutput(AVCapturePhotoOutput, didFinishRecordingLivePhotoMovieForEventualFileAt: URL, resolvedSettings: AVCaptureResolvedPhotoSettings)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didfinishrecordinglivephotomovieforeventualfileat:resolvedsettings:))
- [func photoOutput(AVCapturePhotoOutput, didFinishProcessingLivePhotoToMovieFileAt: URL, duration: CMTime, photoDisplayTime: CMTime, resolvedSettings: AVCaptureResolvedPhotoSettings, error: (any Error)?)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didfinishprocessinglivephototomoviefileat:duration:photodisplaytime:resolvedsettings:error:))
- [func photoOutput(AVCapturePhotoOutput, didFinishCapturingDeferredPhotoProxy: AVCaptureDeferredPhotoProxy?, error: (any Error)?)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didfinishcapturingdeferredphotoproxy:error:))
- [func photoOutput(AVCapturePhotoOutput, didFinishProcessingPhoto: CMSampleBuffer?, previewPhoto: CMSampleBuffer?, resolvedSettings: AVCaptureResolvedPhotoSettings, bracketSettings: AVCaptureBracketedStillImageSettings?, error: (any Error)?)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didfinishprocessingphoto:previewphoto:resolvedsettings:bracketsettings:error:))
- [func photoOutput(AVCapturePhotoOutput, didFinishProcessingRawPhoto: CMSampleBuffer?, previewPhoto: CMSampleBuffer?, resolvedSettings: AVCaptureResolvedPhotoSettings, bracketSettings: AVCaptureBracketedStillImageSettings?, error: (any Error)?)](/documentation/avfoundation/avcapturephotocapturedelegate/photooutput(_:didfinishprocessingrawphoto:previewphoto:resolvedsettings:bracketsettings:error:))
- [AVCapturePhotoOutputReadinessCoordinator](/documentation/avfoundation/avcapturephotooutputreadinesscoordinator)

#### Creating a coordinator

- [init(photoOutput: AVCapturePhotoOutput)](/documentation/avfoundation/avcapturephotooutputreadinesscoordinator/init(photooutput:))

#### Setting the delegate object

- [var delegate: (any AVCapturePhotoOutputReadinessCoordinatorDelegate)?](/documentation/avfoundation/avcapturephotooutputreadinesscoordinator/delegate)

#### Performing tracking requests

- [func startTrackingCaptureRequest(using: AVCapturePhotoSettings)](/documentation/avfoundation/avcapturephotooutputreadinesscoordinator/starttrackingcapturerequest(using:))
- [func stopTrackingCaptureRequest(using: Int64)](/documentation/avfoundation/avcapturephotooutputreadinesscoordinator/stoptrackingcapturerequest(using:))

#### Determining readiness for capture

- [var captureReadiness: AVCapturePhotoOutput.CaptureReadiness](/documentation/avfoundation/avcapturephotooutputreadinesscoordinator/capturereadiness)
- [AVCapturePhotoOutputReadinessCoordinatorDelegate](/documentation/avfoundation/avcapturephotooutputreadinesscoordinatordelegate)

#### Monitoring capture readiness

- [func readinessCoordinator(AVCapturePhotoOutputReadinessCoordinator, captureReadinessDidChange: AVCapturePhotoOutput.CaptureReadiness)](/documentation/avfoundation/avcapturephotooutputreadinesscoordinatordelegate/readinesscoordinator(_:capturereadinessdidchange:))
- [AVCaptureStillImageOutput](/documentation/avfoundation/avcapturestillimageoutput)

#### Capturing an image

- [func captureStillImageAsynchronously(from: AVCaptureConnection, completionHandler: (CMSampleBuffer?, (any Error)?) -> Void)](/documentation/avfoundation/avcapturestillimageoutput/capturestillimageasynchronously(from:completionhandler:))
- [var isCapturingStillImage: Bool](/documentation/avfoundation/avcapturestillimageoutput/iscapturingstillimage)

#### Getting and setting image stabilization settings

- [var isStillImageStabilizationActive: Bool](/documentation/avfoundation/avcapturestillimageoutput/isstillimagestabilizationactive)
- [var automaticallyEnablesStillImageStabilizationWhenAvailable: Bool](/documentation/avfoundation/avcapturestillimageoutput/automaticallyenablesstillimagestabilizationwhenavailable)
- [var isStillImageStabilizationSupported: Bool](/documentation/avfoundation/avcapturestillimageoutput/isstillimagestabilizationsupported)

#### Configuring orientation compensation

- [var isCameraSensorOrientationCompensationSupported: Bool](/documentation/avfoundation/avcapturestillimageoutput/iscamerasensororientationcompensationsupported)
- [var isCameraSensorOrientationCompensationEnabled: Bool](/documentation/avfoundation/avcapturestillimageoutput/iscamerasensororientationcompensationenabled)

#### Configuring image settings

- [var isHighResolutionStillImageOutputEnabled: Bool](/documentation/avfoundation/avcapturestillimageoutput/ishighresolutionstillimageoutputenabled)
- [var availableImageDataCVPixelFormatTypes: [NSNumber]](/documentation/avfoundation/avcapturestillimageoutput/availableimagedatacvpixelformattypes)
- [var availableImageDataCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturestillimageoutput/availableimagedatacodectypes)
- [var outputSettings: [String : Any]](/documentation/avfoundation/avcapturestillimageoutput/outputsettings)
- [Video settings](/documentation/avfoundation/video-settings)

##### Clean aperture

- [let AVVideoCleanApertureKey: String](/documentation/avfoundation/avvideocleanaperturekey)
- [let AVVideoCleanApertureWidthKey: String](/documentation/avfoundation/avvideocleanaperturewidthkey)
- [let AVVideoCleanApertureHeightKey: String](/documentation/avfoundation/avvideocleanapertureheightkey)
- [let AVVideoCleanApertureVerticalOffsetKey: String](/documentation/avfoundation/avvideocleanapertureverticaloffsetkey)
- [let AVVideoCleanApertureHorizontalOffsetKey: String](/documentation/avfoundation/avvideocleanaperturehorizontaloffsetkey)

##### Video codecs

- [let AVVideoCodecKey: String](/documentation/avfoundation/avvideocodeckey)
- [AVVideoCodecType](/documentation/avfoundation/avvideocodectype)

###### Video codecs

- [static let h264: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/h264)
- [static let hevc: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevc)
- [static let hevcWithAlpha: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevcwithalpha)
- [static let jpeg: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpeg)
- [static let JPEGXL: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpegxl)
- [static let proRes422: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422)
- [static let proRes422LT: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422lt)
- [static let proRes422HQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422hq)
- [static let proRes422Proxy: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422proxy)
- [static let proRes4444: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores4444)
- [static let proResRAW: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresraw)
- [static let proResRAWHQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresrawhq)
- [static let appleProRes4444XQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/appleprores4444xq)

###### Deprecated

- [let AVVideoCodecH264: String](/documentation/avfoundation/avvideocodech264)
- [let AVVideoCodecHEVC: String](/documentation/avfoundation/avvideocodechevc)
- [let AVVideoCodecJPEG: String](/documentation/avfoundation/avvideocodecjpeg)
- [let AVVideoCodecAppleProRes422: String](/documentation/avfoundation/avvideocodecappleprores422)
- [let AVVideoCodecAppleProRes4444: String](/documentation/avfoundation/avvideocodecappleprores4444)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideocodectype/init(rawvalue:))

##### Color properties

- [Setting color properties for a specific resolution](/documentation/avfoundation/setting-color-properties-for-a-specific-resolution)
- [let AVVideoAllowWideColorKey: String](/documentation/avfoundation/avvideoallowwidecolorkey)
- [let AVVideoColorPrimariesKey: String](/documentation/avfoundation/avvideocolorprimarieskey)
- [let AVVideoColorPrimaries_EBU_3213: String](/documentation/avfoundation/avvideocolorprimaries_ebu_3213)
- [let AVVideoColorPrimaries_ITU_R_2020: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_2020)
- [let AVVideoColorPrimaries_ITU_R_709_2: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_709_2)
- [let AVVideoColorPrimaries_P3_D65: String](/documentation/avfoundation/avvideocolorprimaries_p3_d65)
- [let AVVideoColorPrimaries_SMPTE_C: String](/documentation/avfoundation/avvideocolorprimaries_smpte_c)
- [let AVVideoColorPropertiesKey: String](/documentation/avfoundation/avvideocolorpropertieskey)
- [let AVVideoTransferFunctionKey: String](/documentation/avfoundation/avvideotransferfunctionkey)
- [let AVVideoTransferFunction_IEC_sRGB: String](/documentation/avfoundation/avvideotransferfunction_iec_srgb)
- [let AVVideoTransferFunction_ITU_R_2100_HLG: String](/documentation/avfoundation/avvideotransferfunction_itu_r_2100_hlg)
- [let AVVideoTransferFunction_ITU_R_709_2: String](/documentation/avfoundation/avvideotransferfunction_itu_r_709_2)
- [let AVVideoTransferFunction_Linear: String](/documentation/avfoundation/avvideotransferfunction_linear)
- [let AVVideoTransferFunction_SMPTE_240M_1995: String](/documentation/avfoundation/avvideotransferfunction_smpte_240m_1995)
- [let AVVideoTransferFunction_SMPTE_ST_2084_PQ: String](/documentation/avfoundation/avvideotransferfunction_smpte_st_2084_pq)
- [let AVVideoYCbCrMatrixKey: String](/documentation/avfoundation/avvideoycbcrmatrixkey)
- [let AVVideoYCbCrMatrix_ITU_R_2020: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_2020)
- [let AVVideoYCbCrMatrix_ITU_R_601_4: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_601_4)
- [let AVVideoYCbCrMatrix_ITU_R_709_2: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_709_2)
- [let AVVideoYCbCrMatrix_SMPTE_240M_1995: String](/documentation/avfoundation/avvideoycbcrmatrix_smpte_240m_1995)

##### Compression

- [let AVVideoCompressionPropertiesKey: String](/documentation/avfoundation/avvideocompressionpropertieskey)
- [let AVVideoDecompressionPropertiesKey: String](/documentation/avfoundation/avvideodecompressionpropertieskey)
- [let AVVideoAverageBitRateKey: String](/documentation/avfoundation/avvideoaveragebitratekey)
- [let AVVideoQualityKey: String](/documentation/avfoundation/avvideoqualitykey)
- [let AVVideoMaxKeyFrameIntervalKey: String](/documentation/avfoundation/avvideomaxkeyframeintervalkey)
- [let AVVideoMaxKeyFrameIntervalDurationKey: String](/documentation/avfoundation/avvideomaxkeyframeintervaldurationkey)
- [let AVVideoAllowFrameReorderingKey: String](/documentation/avfoundation/avvideoallowframereorderingkey)
- [let AVVideoAppleProRAWBitDepthKey: String](/documentation/avfoundation/avvideoappleprorawbitdepthkey)

##### Entropy mode

- [let AVVideoH264EntropyModeKey: String](/documentation/avfoundation/avvideoh264entropymodekey)
- [let AVVideoH264EntropyModeCABAC: String](/documentation/avfoundation/avvideoh264entropymodecabac)
- [let AVVideoH264EntropyModeCAVLC: String](/documentation/avfoundation/avvideoh264entropymodecavlc)

##### FairPlay

- [let AVStreamingKeyDeliveryContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverycontentkeytype)
- [let AVStreamingKeyDeliveryPersistentContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverypersistentcontentkeytype)

##### Frame rate

- [let AVVideoExpectedSourceFrameRateKey: String](/documentation/avfoundation/avvideoexpectedsourceframeratekey)
- [let AVVideoAverageNonDroppableFrameRateKey: String](/documentation/avfoundation/avvideoaveragenondroppableframeratekey)

##### Geometry

- [let AVVideoWidthKey: String](/documentation/avfoundation/avvideowidthkey)
- [let AVVideoHeightKey: String](/documentation/avfoundation/avvideoheightkey)
- [let AVVideoPixelAspectRatioKey: String](/documentation/avfoundation/avvideopixelaspectratiokey)
- [let AVVideoPixelAspectRatioVerticalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratioverticalspacingkey)
- [let AVVideoPixelAspectRatioHorizontalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratiohorizontalspacingkey)

##### Profile level

- [let AVVideoProfileLevelKey: String](/documentation/avfoundation/avvideoprofilelevelkey)
- [let AVVideoProfileLevelH264High40: String](/documentation/avfoundation/avvideoprofilelevelh264high40)
- [let AVVideoProfileLevelH264High41: String](/documentation/avfoundation/avvideoprofilelevelh264high41)
- [let AVVideoProfileLevelH264Main30: String](/documentation/avfoundation/avvideoprofilelevelh264main30)
- [let AVVideoProfileLevelH264Main31: String](/documentation/avfoundation/avvideoprofilelevelh264main31)
- [let AVVideoProfileLevelH264Main32: String](/documentation/avfoundation/avvideoprofilelevelh264main32)
- [let AVVideoProfileLevelH264Main41: String](/documentation/avfoundation/avvideoprofilelevelh264main41)
- [let AVVideoProfileLevelH264Baseline30: String](/documentation/avfoundation/avvideoprofilelevelh264baseline30)
- [let AVVideoProfileLevelH264Baseline31: String](/documentation/avfoundation/avvideoprofilelevelh264baseline31)
- [let AVVideoProfileLevelH264Baseline41: String](/documentation/avfoundation/avvideoprofilelevelh264baseline41)
- [let AVVideoProfileLevelH264HighAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264highautolevel)
- [let AVVideoProfileLevelH264MainAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264mainautolevel)
- [let AVVideoProfileLevelH264BaselineAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264baselineautolevel)

##### Scaling mode

- [let AVVideoScalingModeFit: String](/documentation/avfoundation/avvideoscalingmodefit)
- [let AVVideoScalingModeKey: String](/documentation/avfoundation/avvideoscalingmodekey)
- [let AVVideoScalingModeResize: String](/documentation/avfoundation/avvideoscalingmoderesize)
- [let AVVideoScalingModeResizeAspect: String](/documentation/avfoundation/avvideoscalingmoderesizeaspect)
- [let AVVideoScalingModeResizeAspectFill: String](/documentation/avfoundation/avvideoscalingmoderesizeaspectfill)

##### VideoToolbox options

- [let AVVideoEncoderSpecificationKey: String](/documentation/avfoundation/avvideoencoderspecificationkey)

#### Image format conversion

- [class func jpegStillImageNSDataRepresentation(CMSampleBuffer) -> Data?](/documentation/avfoundation/avcapturestillimageoutput/jpegstillimagensdatarepresentation(_:))

#### Still image bracketed capture

- [func captureStillImageBracketAsynchronously(from: AVCaptureConnection, withSettingsArray: [AVCaptureBracketedStillImageSettings], completionHandler: (CMSampleBuffer?, AVCaptureBracketedStillImageSettings?, (any Error)?) -> Void)](/documentation/avfoundation/avcapturestillimageoutput/capturestillimagebracketasynchronously(from:withsettingsarray:completionhandler:))
- [var maxBracketedCaptureStillImageCount: Int](/documentation/avfoundation/avcapturestillimageoutput/maxbracketedcapturestillimagecount)
- [func prepareToCaptureStillImageBracket(from: AVCaptureConnection, withSettingsArray: [AVCaptureBracketedStillImageSettings], completionHandler: (Bool, (any Error)?) -> Void)](/documentation/avfoundation/avcapturestillimageoutput/preparetocapturestillimagebracket(from:withsettingsarray:completionhandler:))
- [var isLensStabilizationDuringBracketedCaptureSupported: Bool](/documentation/avfoundation/avcapturestillimageoutput/islensstabilizationduringbracketedcapturesupported)
- [var isLensStabilizationDuringBracketedCaptureEnabled: Bool](/documentation/avfoundation/avcapturestillimageoutput/islensstabilizationduringbracketedcaptureenabled)

#### Creating still image output

- [init()](/documentation/avfoundation/avcapturestillimageoutput/init())

### Photo settings

- [AVCapturePhotoSettings](/documentation/avfoundation/avcapturephotosettings)

#### Creating photo settings

- [convenience init(format: [String : Any]?)](/documentation/avfoundation/avcapturephotosettings/init(format:))
- [convenience init(rawPixelFormatType: OSType)](/documentation/avfoundation/avcapturephotosettings/init(rawpixelformattype:))
- [convenience init(rawPixelFormatType: OSType, processedFormat: [String : Any]?)](/documentation/avfoundation/avcapturephotosettings/init(rawpixelformattype:processedformat:))
- [convenience init(rawPixelFormatType: OSType, rawFileType: AVFileType?, processedFormat: [String : Any]?, processedFileType: AVFileType?)](/documentation/avfoundation/avcapturephotosettings/init(rawpixelformattype:rawfiletype:processedformat:processedfiletype:))
- [convenience init(from: AVCapturePhotoSettings)](/documentation/avfoundation/avcapturephotosettings/init(from:))

#### Inspecting settings

- [var uniqueID: Int64](/documentation/avfoundation/avcapturephotosettings/uniqueid)
- [var format: [String : Any]?](/documentation/avfoundation/avcapturephotosettings/format)
- [var processedFileType: AVFileType?](/documentation/avfoundation/avcapturephotosettings/processedfiletype)
- [var rawFileType: AVFileType?](/documentation/avfoundation/avcapturephotosettings/rawfiletype)
- [var rawPhotoPixelFormatType: OSType](/documentation/avfoundation/avcapturephotosettings/rawphotopixelformattype)

#### Configuring photo settings

- [var flashMode: AVCaptureDevice.FlashMode](/documentation/avfoundation/avcapturephotosettings/flashmode)
- [var isAutoRedEyeReductionEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isautoredeyereductionenabled)
- [var maxPhotoDimensions: CMVideoDimensions](/documentation/avfoundation/avcapturephotosettings/maxphotodimensions)
- [var photoQualityPrioritization: AVCapturePhotoOutput.QualityPrioritization](/documentation/avfoundation/avcapturephotosettings/photoqualityprioritization)
- [var isCameraCalibrationDataDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/iscameracalibrationdatadeliveryenabled)
- [var isAutoContentAwareDistortionCorrectionEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isautocontentawaredistortioncorrectionenabled)
- [var isAutoVirtualDeviceFusionEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isautovirtualdevicefusionenabled)
- [var virtualDeviceConstituentPhotoDeliveryEnabledDevices: [AVCaptureDevice]](/documentation/avfoundation/avcapturephotosettings/virtualdeviceconstituentphotodeliveryenableddevices)
- [var isDualCameraDualPhotoDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isdualcameradualphotodeliveryenabled)
- [var isAutoDualCameraFusionEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isautodualcamerafusionenabled)
- [var isAutoStillImageStabilizationEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isautostillimagestabilizationenabled)
- [var isHighResolutionPhotoEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/ishighresolutionphotoenabled)

#### Suppressing the shutter sound

- [var isShutterSoundSuppressionEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isshuttersoundsuppressionenabled)

#### Enabling preview and thumbnail delivery

- [var previewPhotoFormat: [String : Any]?](/documentation/avfoundation/avcapturephotosettings/previewphotoformat)
- [var availablePreviewPhotoPixelFormatTypes: [OSType]](/documentation/avfoundation/avcapturephotosettings/availablepreviewphotopixelformattypes-30d9)
- [var embeddedThumbnailPhotoFormat: [String : Any]?](/documentation/avfoundation/avcapturephotosettings/embeddedthumbnailphotoformat)
- [var availableRawEmbeddedThumbnailPhotoCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturephotosettings/availablerawembeddedthumbnailphotocodectypes)
- [var rawEmbeddedThumbnailPhotoFormat: [String : Any]?](/documentation/avfoundation/avcapturephotosettings/rawembeddedthumbnailphotoformat)
- [var availableEmbeddedThumbnailPhotoCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturephotosettings/availableembeddedthumbnailphotocodectypes)

#### Configuring Live Photo settings

- [var livePhotoMovieFileURL: URL?](/documentation/avfoundation/avcapturephotosettings/livephotomoviefileurl)
- [var livePhotoMovieMetadata: [AVMetadataItem]!](/documentation/avfoundation/avcapturephotosettings/livephotomoviemetadata)
- [var livePhotoVideoCodecType: AVVideoCodecType](/documentation/avfoundation/avcapturephotosettings/livephotovideocodectype)

#### Configuring constant color

- [var isConstantColorEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isconstantcolorenabled)
- [var isConstantColorFallbackPhotoDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isconstantcolorfallbackphotodeliveryenabled)

#### Capturing depth data

- [var isDepthDataDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isdepthdatadeliveryenabled)
- [var embedsDepthDataInPhoto: Bool](/documentation/avfoundation/avcapturephotosettings/embedsdepthdatainphoto)
- [var isDepthDataFiltered: Bool](/documentation/avfoundation/avcapturephotosettings/isdepthdatafiltered)

#### Capturing Portrait Effects matte

- [var isPortraitEffectsMatteDeliveryEnabled: Bool](/documentation/avfoundation/avcapturephotosettings/isportraiteffectsmattedeliveryenabled)
- [var embedsPortraitEffectsMatteInPhoto: Bool](/documentation/avfoundation/avcapturephotosettings/embedsportraiteffectsmatteinphoto)

#### Capturing semantic segmentation mattes

- [var embedsSemanticSegmentationMattesInPhoto: Bool](/documentation/avfoundation/avcapturephotosettings/embedssemanticsegmentationmattesinphoto)
- [var enabledSemanticSegmentationMatteTypes: [AVSemanticSegmentationMatte.MatteType]](/documentation/avfoundation/avcapturephotosettings/enabledsemanticsegmentationmattetypes)

#### Embedding metadata

- [var metadata: [String : Any]](/documentation/avfoundation/avcapturephotosettings/metadata)

#### Instance properties

- [var rawFileFormat: [String : Any]?](/documentation/avfoundation/avcapturephotosettings/rawfileformat)
- [AVCapturePhotoBracketSettings](/documentation/avfoundation/avcapturephotobracketsettings)

#### Creating a bracket settings object

- [convenience init(rawPixelFormatType: OSType, rawFileType: AVFileType?, processedFormat: [String : Any]?, processedFileType: AVFileType?, bracketedSettings: [AVCaptureBracketedStillImageSettings])](/documentation/avfoundation/avcapturephotobracketsettings/init(rawpixelformattype:rawfiletype:processedformat:processedfiletype:bracketedsettings:))
- [convenience init(rawPixelFormatType: OSType, processedFormat: [String : Any]?, bracketedSettings: [AVCaptureBracketedStillImageSettings])](/documentation/avfoundation/avcapturephotobracketsettings/init(rawpixelformattype:processedformat:bracketedsettings:))

#### Working with bracketed settings

- [var bracketedSettings: [AVCaptureBracketedStillImageSettings]](/documentation/avfoundation/avcapturephotobracketsettings/bracketedsettings)
- [var isLensStabilizationEnabled: Bool](/documentation/avfoundation/avcapturephotobracketsettings/islensstabilizationenabled)

#### Bracketed settings types

- [AVCaptureAutoExposureBracketedStillImageSettings](/documentation/avfoundation/avcaptureautoexposurebracketedstillimagesettings)

##### Creating an auto exposure settings instance

- [class func autoExposureSettings(exposureTargetBias: Float) -> Self](/documentation/avfoundation/avcaptureautoexposurebracketedstillimagesettings/autoexposuresettings(exposuretargetbias:))

##### Getting the exposure target bias

- [var exposureTargetBias: Float](/documentation/avfoundation/avcaptureautoexposurebracketedstillimagesettings/exposuretargetbias)
- [AVCaptureManualExposureBracketedStillImageSettings](/documentation/avfoundation/avcapturemanualexposurebracketedstillimagesettings)

##### Creating a manual bracketed exposure settings instance

- [class func manualExposureSettings(exposureDuration: CMTime, iso: Float) -> Self](/documentation/avfoundation/avcapturemanualexposurebracketedstillimagesettings/manualexposuresettings(exposureduration:iso:))

##### Getting manual exposure setting values

- [var iso: Float](/documentation/avfoundation/avcapturemanualexposurebracketedstillimagesettings/iso)
- [var exposureDuration: CMTime](/documentation/avfoundation/avcapturemanualexposurebracketedstillimagesettings/exposureduration)
- [AVCaptureBracketedStillImageSettings](/documentation/avfoundation/avcapturebracketedstillimagesettings)
- [AVCaptureResolvedPhotoSettings](/documentation/avfoundation/avcaptureresolvedphotosettings)

#### Resolving photo capture requests

- [var uniqueID: Int64](/documentation/avfoundation/avcaptureresolvedphotosettings/uniqueid)
- [var expectedPhotoCount: Int](/documentation/avfoundation/avcaptureresolvedphotosettings/expectedphotocount)

#### Examining photo capture settings

- [var isFlashEnabled: Bool](/documentation/avfoundation/avcaptureresolvedphotosettings/isflashenabled)
- [var isRedEyeReductionEnabled: Bool](/documentation/avfoundation/avcaptureresolvedphotosettings/isredeyereductionenabled)
- [var isVirtualDeviceFusionEnabled: Bool](/documentation/avfoundation/avcaptureresolvedphotosettings/isvirtualdevicefusionenabled)
- [var isFastCapturePrioritizationEnabled: Bool](/documentation/avfoundation/avcaptureresolvedphotosettings/isfastcaptureprioritizationenabled)
- [var isContentAwareDistortionCorrectionEnabled: Bool](/documentation/avfoundation/avcaptureresolvedphotosettings/iscontentawaredistortioncorrectionenabled)
- [var isStillImageStabilizationEnabled: Bool](/documentation/avfoundation/avcaptureresolvedphotosettings/isstillimagestabilizationenabled)
- [var isDualCameraFusionEnabled: Bool](/documentation/avfoundation/avcaptureresolvedphotosettings/isdualcamerafusionenabled)

#### Examining output dimensions

- [var photoDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/photodimensions)
- [var deferredPhotoProxyDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/deferredphotoproxydimensions)
- [var rawPhotoDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/rawphotodimensions)
- [var previewDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/previewdimensions)
- [var embeddedThumbnailDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/embeddedthumbnaildimensions)
- [var rawEmbeddedThumbnailDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/rawembeddedthumbnaildimensions)
- [var livePhotoMovieDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/livephotomoviedimensions)
- [var portraitEffectsMatteDimensions: CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/portraiteffectsmattedimensions)
- [func dimensionsForSemanticSegmentationMatte(ofType: AVSemanticSegmentationMatte.MatteType) -> CMVideoDimensions](/documentation/avfoundation/avcaptureresolvedphotosettings/dimensionsforsemanticsegmentationmatte(oftype:))
- [var photoProcessingTimeRange: CMTimeRange](/documentation/avfoundation/avcaptureresolvedphotosettings/photoprocessingtimerange)

### Matte data

- [AVPortraitEffectsMatte](/documentation/avfoundation/avportraiteffectsmatte)

#### Creating a Portrait Effects matte

- [Configuring camera capture to collect a Portrait Effects matte](/documentation/avfoundation/configuring-camera-capture-to-collect-a-portrait-effects-matte)
- [convenience init(fromDictionaryRepresentation: [AnyHashable : Any]) throws](/documentation/avfoundation/avportraiteffectsmatte/init(fromdictionaryrepresentation:))
- [func applyingExifOrientation(CGImagePropertyOrientation) -> Self](/documentation/avfoundation/avportraiteffectsmatte/applyingexiforientation(_:))
- [func replacingPortraitEffectsMatte(with: CVPixelBuffer) throws -> Self](/documentation/avfoundation/avportraiteffectsmatte/replacingportraiteffectsmatte(with:))

#### Examining a Portrait Effects matte

- [Extracting Portrait Effects matte image data from a photo](/documentation/avfoundation/extracting-portrait-effects-matte-image-data-from-a-photo)
- [var mattingImage: CVPixelBuffer](/documentation/avfoundation/avportraiteffectsmatte/mattingimage)
- [var pixelFormatType: OSType](/documentation/avfoundation/avportraiteffectsmatte/pixelformattype)
- [func dictionaryRepresentation(forAuxiliaryDataType: AutoreleasingUnsafeMutablePointer<NSString?>?) -> [AnyHashable : Any]?](/documentation/avfoundation/avportraiteffectsmatte/dictionaryrepresentation(forauxiliarydatatype:))
- [AVSemanticSegmentationMatte](/documentation/avfoundation/avsemanticsegmentationmatte)

#### Creating a segmentation matte

- [convenience init(fromImageSourceAuxiliaryDataType: CFString, dictionaryRepresentation: [AnyHashable : Any]) throws](/documentation/avfoundation/avsemanticsegmentationmatte/init(fromimagesourceauxiliarydatatype:dictionaryrepresentation:))
- [func replacingSemanticSegmentationMatte(with: CVPixelBuffer) throws -> Self](/documentation/avfoundation/avsemanticsegmentationmatte/replacingsemanticsegmentationmatte(with:))
- [func applyingExifOrientation(CGImagePropertyOrientation) -> Self](/documentation/avfoundation/avsemanticsegmentationmatte/applyingexiforientation(_:))
- [func dictionaryRepresentation(forAuxiliaryDataType: AutoreleasingUnsafeMutablePointer<NSString?>?) -> [AnyHashable : Any]?](/documentation/avfoundation/avsemanticsegmentationmatte/dictionaryrepresentation(forauxiliarydatatype:))

#### Inspecting a segmentation matte

- [var matteType: AVSemanticSegmentationMatte.MatteType](/documentation/avfoundation/avsemanticsegmentationmatte/mattetype-swift.property)
- [AVSemanticSegmentationMatte.MatteType](/documentation/avfoundation/avsemanticsegmentationmatte/mattetype-swift.struct)

##### Matte types

- [static let hair: AVSemanticSegmentationMatte.MatteType](/documentation/avfoundation/avsemanticsegmentationmatte/mattetype-swift.struct/hair)
- [static let skin: AVSemanticSegmentationMatte.MatteType](/documentation/avfoundation/avsemanticsegmentationmatte/mattetype-swift.struct/skin)
- [static let teeth: AVSemanticSegmentationMatte.MatteType](/documentation/avfoundation/avsemanticsegmentationmatte/mattetype-swift.struct/teeth)
- [static let glasses: AVSemanticSegmentationMatte.MatteType](/documentation/avfoundation/avsemanticsegmentationmatte/mattetype-swift.struct/glasses)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avsemanticsegmentationmatte/mattetype-swift.struct/init(rawvalue:))
- [var mattingImage: CVPixelBuffer](/documentation/avfoundation/avsemanticsegmentationmatte/mattingimage)
- [var pixelFormatType: OSType](/documentation/avfoundation/avsemanticsegmentationmatte/pixelformattype)
- [Audio and video capture](/documentation/avfoundation/audio-and-video-capture)

### File capture

- [Recording movies in alternative formats](/documentation/avfoundation/recording-movies-in-alternative-formats)
- [AVCaptureMovieFileOutput](/documentation/avfoundation/avcapturemoviefileoutput)

#### Creating a movie file output

- [init()](/documentation/avfoundation/avcapturemoviefileoutput/init())

#### Configuring movies

- [var movieFragmentInterval: CMTime](/documentation/avfoundation/avcapturemoviefileoutput/moviefragmentinterval)
- [var metadata: [AVMetadataItem]?](/documentation/avfoundation/avcapturemoviefileoutput/metadata)

#### Managing output settings

- [func supportedOutputSettingsKeys(for: AVCaptureConnection) -> [String]](/documentation/avfoundation/avcapturemoviefileoutput/supportedoutputsettingskeys(for:))
- [func outputSettings(for: AVCaptureConnection) -> [String : Any]](/documentation/avfoundation/avcapturemoviefileoutput/outputsettings(for:))
- [func setOutputSettings([String : Any]?, for: AVCaptureConnection)](/documentation/avfoundation/avcapturemoviefileoutput/setoutputsettings(_:for:))
- [var availableVideoCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturemoviefileoutput/availablevideocodectypes)

#### Enabling spatial capture

- [var isSpatialVideoCaptureSupported: Bool](/documentation/avfoundation/avcapturemoviefileoutput/isspatialvideocapturesupported)
- [var isSpatialVideoCaptureEnabled: Bool](/documentation/avfoundation/avcapturemoviefileoutput/isspatialvideocaptureenabled)

#### Setting orientation

- [func recordsVideoOrientationAndMirroringChangesAsMetadataTrack(for: AVCaptureConnection) -> Bool](/documentation/avfoundation/avcapturemoviefileoutput/recordsvideoorientationandmirroringchangesasmetadatatrack(for:))
- [func setRecordsVideoOrientationAndMirroringChangesAsMetadataTrack(Bool, for: AVCaptureConnection)](/documentation/avfoundation/avcapturemoviefileoutput/setrecordsvideoorientationandmirroringchangesasmetadatatrack(_:for:))

#### Restricting camera switching

- [var isPrimaryConstituentDeviceSwitchingBehaviorForRecordingEnabled: Bool](/documentation/avfoundation/avcapturemoviefileoutput/isprimaryconstituentdeviceswitchingbehaviorforrecordingenabled)
- [func setPrimaryConstituentDeviceSwitchingBehaviorForRecording(AVCaptureDevice.PrimaryConstituentDeviceSwitchingBehavior, restrictedSwitchingBehaviorConditions: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions)](/documentation/avfoundation/avcapturemoviefileoutput/setprimaryconstituentdeviceswitchingbehaviorforrecording(_:restrictedswitchingbehaviorconditions:))
- [var primaryConstituentDeviceSwitchingBehaviorForRecording: AVCaptureDevice.PrimaryConstituentDeviceSwitchingBehavior](/documentation/avfoundation/avcapturemoviefileoutput/primaryconstituentdeviceswitchingbehaviorforrecording)
- [var primaryConstituentDeviceRestrictedSwitchingBehaviorConditionsForRecording: AVCaptureDevice.PrimaryConstituentDeviceRestrictedSwitchingBehaviorConditions](/documentation/avfoundation/avcapturemoviefileoutput/primaryconstituentdevicerestrictedswitchingbehaviorconditionsforrecording)
- [AVCaptureAudioFileOutput](/documentation/avfoundation/avcaptureaudiofileoutput)

#### Discovering supported types

- [class func availableOutputFileTypes() -> [AVFileType]](/documentation/avfoundation/avcaptureaudiofileoutput/availableoutputfiletypes())

#### Starting a recording

- [func startRecording(to: URL, outputFileType: AVFileType, recordingDelegate: any AVCaptureFileOutputRecordingDelegate)](/documentation/avfoundation/avcaptureaudiofileoutput/startrecording(to:outputfiletype:recordingdelegate:))

#### Configuring output

- [var audioSettings: [String : Any]?](/documentation/avfoundation/avcaptureaudiofileoutput/audiosettings)
- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avcaptureaudiofileoutput/metadata)

#### Creating output

- [init()](/documentation/avfoundation/avcaptureaudiofileoutput/init())
- [AVCaptureFileOutput](/documentation/avfoundation/avcapturefileoutput)

#### Setting file output properties

- [var delegate: (any AVCaptureFileOutputDelegate)?](/documentation/avfoundation/avcapturefileoutput/delegate)
- [var maxRecordedDuration: CMTime](/documentation/avfoundation/avcapturefileoutput/maxrecordedduration)
- [var maxRecordedFileSize: Int64](/documentation/avfoundation/avcapturefileoutput/maxrecordedfilesize)
- [var minFreeDiskSpaceLimit: Int64](/documentation/avfoundation/avcapturefileoutput/minfreediskspacelimit)
- [var outputFileURL: URL?](/documentation/avfoundation/avcapturefileoutput/outputfileurl)
- [var recordedDuration: CMTime](/documentation/avfoundation/avcapturefileoutput/recordedduration)
- [var recordedFileSize: Int64](/documentation/avfoundation/avcapturefileoutput/recordedfilesize)
- [var isRecording: Bool](/documentation/avfoundation/avcapturefileoutput/isrecording)
- [var isRecordingPaused: Bool](/documentation/avfoundation/avcapturefileoutput/isrecordingpaused)

#### Managing recording

- [func startRecording(to: URL, recordingDelegate: any AVCaptureFileOutputRecordingDelegate)](/documentation/avfoundation/avcapturefileoutput/startrecording(to:recordingdelegate:))
- [func stopRecording()](/documentation/avfoundation/avcapturefileoutput/stoprecording())
- [func pauseRecording()](/documentation/avfoundation/avcapturefileoutput/pauserecording())
- [func resumeRecording()](/documentation/avfoundation/avcapturefileoutput/resumerecording())
- [AVCaptureFileOutputDelegate](/documentation/avfoundation/avcapturefileoutputdelegate)

#### Sample processing

- [func fileOutputShouldProvideSampleAccurateRecordingStart(AVCaptureFileOutput) -> Bool](/documentation/avfoundation/avcapturefileoutputdelegate/fileoutputshouldprovidesampleaccuraterecordingstart(_:))
- [func fileOutput(AVCaptureFileOutput, didOutputSampleBuffer: CMSampleBuffer, from: AVCaptureConnection)](/documentation/avfoundation/avcapturefileoutputdelegate/fileoutput(_:didoutputsamplebuffer:from:))
- [AVCaptureFileOutputRecordingDelegate](/documentation/avfoundation/avcapturefileoutputrecordingdelegate)

#### Delegate methods

- [func fileOutput(AVCaptureFileOutput, didStartRecordingTo: URL, from: [AVCaptureConnection])](/documentation/avfoundation/avcapturefileoutputrecordingdelegate/fileoutput(_:didstartrecordingto:from:))
- [func fileOutput(AVCaptureFileOutput, didStartRecordingTo: URL, startPTS: CMTime, from: [AVCaptureConnection])](/documentation/avfoundation/avcapturefileoutputrecordingdelegate/fileoutput(_:didstartrecordingto:startpts:from:))
- [func fileOutput(AVCaptureFileOutput, willFinishRecordingTo: URL, from: [AVCaptureConnection], error: (any Error)?)](/documentation/avfoundation/avcapturefileoutputrecordingdelegate/fileoutput(_:willfinishrecordingto:from:error:))
- [func fileOutput(AVCaptureFileOutput, didFinishRecordingTo: URL, from: [AVCaptureConnection], error: (any Error)?)](/documentation/avfoundation/avcapturefileoutputrecordingdelegate/fileoutput(_:didfinishrecordingto:from:error:))
- [func fileOutput(AVCaptureFileOutput, didPauseRecordingTo: URL, from: [AVCaptureConnection])](/documentation/avfoundation/avcapturefileoutputrecordingdelegate/fileoutput(_:didpauserecordingto:from:))
- [func fileOutput(AVCaptureFileOutput, didResumeRecordingTo: URL, from: [AVCaptureConnection])](/documentation/avfoundation/avcapturefileoutputrecordingdelegate/fileoutput(_:didresumerecordingto:from:))

### Stream capture

- [Capturing Spatial Audio in your iOS app](/documentation/avfoundation/capturing-spatial-audio-in-your-ios-app)
- [AVCaptureVideoDataOutput](/documentation/avfoundation/avcapturevideodataoutput)

#### Configuring video capture

- [var videoSettings: [String : Any]!](/documentation/avfoundation/avcapturevideodataoutput/videosettings)
- [Video settings](/documentation/avfoundation/video-settings)

##### Clean aperture

- [let AVVideoCleanApertureKey: String](/documentation/avfoundation/avvideocleanaperturekey)
- [let AVVideoCleanApertureWidthKey: String](/documentation/avfoundation/avvideocleanaperturewidthkey)
- [let AVVideoCleanApertureHeightKey: String](/documentation/avfoundation/avvideocleanapertureheightkey)
- [let AVVideoCleanApertureVerticalOffsetKey: String](/documentation/avfoundation/avvideocleanapertureverticaloffsetkey)
- [let AVVideoCleanApertureHorizontalOffsetKey: String](/documentation/avfoundation/avvideocleanaperturehorizontaloffsetkey)

##### Video codecs

- [let AVVideoCodecKey: String](/documentation/avfoundation/avvideocodeckey)
- [AVVideoCodecType](/documentation/avfoundation/avvideocodectype)

###### Video codecs

- [static let h264: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/h264)
- [static let hevc: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevc)
- [static let hevcWithAlpha: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevcwithalpha)
- [static let jpeg: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpeg)
- [static let JPEGXL: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpegxl)
- [static let proRes422: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422)
- [static let proRes422LT: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422lt)
- [static let proRes422HQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422hq)
- [static let proRes422Proxy: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422proxy)
- [static let proRes4444: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores4444)
- [static let proResRAW: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresraw)
- [static let proResRAWHQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresrawhq)
- [static let appleProRes4444XQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/appleprores4444xq)

###### Deprecated

- [let AVVideoCodecH264: String](/documentation/avfoundation/avvideocodech264)
- [let AVVideoCodecHEVC: String](/documentation/avfoundation/avvideocodechevc)
- [let AVVideoCodecJPEG: String](/documentation/avfoundation/avvideocodecjpeg)
- [let AVVideoCodecAppleProRes422: String](/documentation/avfoundation/avvideocodecappleprores422)
- [let AVVideoCodecAppleProRes4444: String](/documentation/avfoundation/avvideocodecappleprores4444)

###### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideocodectype/init(rawvalue:))

##### Color properties

- [Setting color properties for a specific resolution](/documentation/avfoundation/setting-color-properties-for-a-specific-resolution)
- [let AVVideoAllowWideColorKey: String](/documentation/avfoundation/avvideoallowwidecolorkey)
- [let AVVideoColorPrimariesKey: String](/documentation/avfoundation/avvideocolorprimarieskey)
- [let AVVideoColorPrimaries_EBU_3213: String](/documentation/avfoundation/avvideocolorprimaries_ebu_3213)
- [let AVVideoColorPrimaries_ITU_R_2020: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_2020)
- [let AVVideoColorPrimaries_ITU_R_709_2: String](/documentation/avfoundation/avvideocolorprimaries_itu_r_709_2)
- [let AVVideoColorPrimaries_P3_D65: String](/documentation/avfoundation/avvideocolorprimaries_p3_d65)
- [let AVVideoColorPrimaries_SMPTE_C: String](/documentation/avfoundation/avvideocolorprimaries_smpte_c)
- [let AVVideoColorPropertiesKey: String](/documentation/avfoundation/avvideocolorpropertieskey)
- [let AVVideoTransferFunctionKey: String](/documentation/avfoundation/avvideotransferfunctionkey)
- [let AVVideoTransferFunction_IEC_sRGB: String](/documentation/avfoundation/avvideotransferfunction_iec_srgb)
- [let AVVideoTransferFunction_ITU_R_2100_HLG: String](/documentation/avfoundation/avvideotransferfunction_itu_r_2100_hlg)
- [let AVVideoTransferFunction_ITU_R_709_2: String](/documentation/avfoundation/avvideotransferfunction_itu_r_709_2)
- [let AVVideoTransferFunction_Linear: String](/documentation/avfoundation/avvideotransferfunction_linear)
- [let AVVideoTransferFunction_SMPTE_240M_1995: String](/documentation/avfoundation/avvideotransferfunction_smpte_240m_1995)
- [let AVVideoTransferFunction_SMPTE_ST_2084_PQ: String](/documentation/avfoundation/avvideotransferfunction_smpte_st_2084_pq)
- [let AVVideoYCbCrMatrixKey: String](/documentation/avfoundation/avvideoycbcrmatrixkey)
- [let AVVideoYCbCrMatrix_ITU_R_2020: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_2020)
- [let AVVideoYCbCrMatrix_ITU_R_601_4: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_601_4)
- [let AVVideoYCbCrMatrix_ITU_R_709_2: String](/documentation/avfoundation/avvideoycbcrmatrix_itu_r_709_2)
- [let AVVideoYCbCrMatrix_SMPTE_240M_1995: String](/documentation/avfoundation/avvideoycbcrmatrix_smpte_240m_1995)

##### Compression

- [let AVVideoCompressionPropertiesKey: String](/documentation/avfoundation/avvideocompressionpropertieskey)
- [let AVVideoDecompressionPropertiesKey: String](/documentation/avfoundation/avvideodecompressionpropertieskey)
- [let AVVideoAverageBitRateKey: String](/documentation/avfoundation/avvideoaveragebitratekey)
- [let AVVideoQualityKey: String](/documentation/avfoundation/avvideoqualitykey)
- [let AVVideoMaxKeyFrameIntervalKey: String](/documentation/avfoundation/avvideomaxkeyframeintervalkey)
- [let AVVideoMaxKeyFrameIntervalDurationKey: String](/documentation/avfoundation/avvideomaxkeyframeintervaldurationkey)
- [let AVVideoAllowFrameReorderingKey: String](/documentation/avfoundation/avvideoallowframereorderingkey)
- [let AVVideoAppleProRAWBitDepthKey: String](/documentation/avfoundation/avvideoappleprorawbitdepthkey)

##### Entropy mode

- [let AVVideoH264EntropyModeKey: String](/documentation/avfoundation/avvideoh264entropymodekey)
- [let AVVideoH264EntropyModeCABAC: String](/documentation/avfoundation/avvideoh264entropymodecabac)
- [let AVVideoH264EntropyModeCAVLC: String](/documentation/avfoundation/avvideoh264entropymodecavlc)

##### FairPlay

- [let AVStreamingKeyDeliveryContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverycontentkeytype)
- [let AVStreamingKeyDeliveryPersistentContentKeyType: String](/documentation/avfoundation/avstreamingkeydeliverypersistentcontentkeytype)

##### Frame rate

- [let AVVideoExpectedSourceFrameRateKey: String](/documentation/avfoundation/avvideoexpectedsourceframeratekey)
- [let AVVideoAverageNonDroppableFrameRateKey: String](/documentation/avfoundation/avvideoaveragenondroppableframeratekey)

##### Geometry

- [let AVVideoWidthKey: String](/documentation/avfoundation/avvideowidthkey)
- [let AVVideoHeightKey: String](/documentation/avfoundation/avvideoheightkey)
- [let AVVideoPixelAspectRatioKey: String](/documentation/avfoundation/avvideopixelaspectratiokey)
- [let AVVideoPixelAspectRatioVerticalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratioverticalspacingkey)
- [let AVVideoPixelAspectRatioHorizontalSpacingKey: String](/documentation/avfoundation/avvideopixelaspectratiohorizontalspacingkey)

##### Profile level

- [let AVVideoProfileLevelKey: String](/documentation/avfoundation/avvideoprofilelevelkey)
- [let AVVideoProfileLevelH264High40: String](/documentation/avfoundation/avvideoprofilelevelh264high40)
- [let AVVideoProfileLevelH264High41: String](/documentation/avfoundation/avvideoprofilelevelh264high41)
- [let AVVideoProfileLevelH264Main30: String](/documentation/avfoundation/avvideoprofilelevelh264main30)
- [let AVVideoProfileLevelH264Main31: String](/documentation/avfoundation/avvideoprofilelevelh264main31)
- [let AVVideoProfileLevelH264Main32: String](/documentation/avfoundation/avvideoprofilelevelh264main32)
- [let AVVideoProfileLevelH264Main41: String](/documentation/avfoundation/avvideoprofilelevelh264main41)
- [let AVVideoProfileLevelH264Baseline30: String](/documentation/avfoundation/avvideoprofilelevelh264baseline30)
- [let AVVideoProfileLevelH264Baseline31: String](/documentation/avfoundation/avvideoprofilelevelh264baseline31)
- [let AVVideoProfileLevelH264Baseline41: String](/documentation/avfoundation/avvideoprofilelevelh264baseline41)
- [let AVVideoProfileLevelH264HighAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264highautolevel)
- [let AVVideoProfileLevelH264MainAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264mainautolevel)
- [let AVVideoProfileLevelH264BaselineAutoLevel: String](/documentation/avfoundation/avvideoprofilelevelh264baselineautolevel)

##### Scaling mode

- [let AVVideoScalingModeFit: String](/documentation/avfoundation/avvideoscalingmodefit)
- [let AVVideoScalingModeKey: String](/documentation/avfoundation/avvideoscalingmodekey)
- [let AVVideoScalingModeResize: String](/documentation/avfoundation/avvideoscalingmoderesize)
- [let AVVideoScalingModeResizeAspect: String](/documentation/avfoundation/avvideoscalingmoderesizeaspect)
- [let AVVideoScalingModeResizeAspectFill: String](/documentation/avfoundation/avvideoscalingmoderesizeaspectfill)

##### VideoToolbox options

- [let AVVideoEncoderSpecificationKey: String](/documentation/avfoundation/avvideoencoderspecificationkey)
- [var alwaysDiscardsLateVideoFrames: Bool](/documentation/avfoundation/avcapturevideodataoutput/alwaysdiscardslatevideoframes)
- [var automaticallyConfiguresOutputBufferDimensions: Bool](/documentation/avfoundation/avcapturevideodataoutput/automaticallyconfiguresoutputbufferdimensions)
- [var deliversPreviewSizedOutputBuffers: Bool](/documentation/avfoundation/avcapturevideodataoutput/deliverspreviewsizedoutputbuffers)
- [var preparesCellularRadioForNetworkConnection: Bool](/documentation/avfoundation/avcapturevideodataoutput/preparescellularradiofornetworkconnection)
- [var preservesDynamicHDRMetadata: Bool](/documentation/avfoundation/avcapturevideodataoutput/preservesdynamichdrmetadata)
- [var recommendedMediaTimeScaleForAssetWriter: CMTimeScale](/documentation/avfoundation/avcapturevideodataoutput/recommendedmediatimescaleforassetwriter)
- [func recommendedMovieMetadata(forVideoCodecType: AVVideoCodecType, assetWriterOutputFileType: AVFileType) -> [AVMetadataItem]?](/documentation/avfoundation/avcapturevideodataoutput/recommendedmoviemetadata(forvideocodectype:assetwriteroutputfiletype:))
- [func recommendedVideoSettings(forVideoCodecType: AVVideoCodecType, assetWriterOutputFileType: AVFileType) -> [String : Any]?](/documentation/avfoundation/avcapturevideodataoutput/recommendedvideosettings(forvideocodectype:assetwriteroutputfiletype:))
- [func recommendedVideoSettings(forVideoCodecType: AVVideoCodecType, assetWriterOutputFileType: AVFileType, outputFileURL: URL?) -> [String : Any]?](/documentation/avfoundation/avcapturevideodataoutput/recommendedvideosettings(forvideocodectype:assetwriteroutputfiletype:outputfileurl:))
- [func recommendedVideoSettingsForAssetWriter(writingTo: AVFileType) -> [String : Any]?](/documentation/avfoundation/avcapturevideodataoutput/recommendedvideosettingsforassetwriter(writingto:))

#### Retrieving supported video types

- [var availableVideoPixelFormatTypes: [OSType]](/documentation/avfoundation/avcapturevideodataoutput/availablevideopixelformattypes)
- [var availableVideoCodecTypes: [AVVideoCodecType]](/documentation/avfoundation/avcapturevideodataoutput/availablevideocodectypes)
- [func availableVideoCodecTypesForAssetWriter(writingTo: AVFileType) -> [AVVideoCodecType]](/documentation/avfoundation/avcapturevideodataoutput/availablevideocodectypesforassetwriter(writingto:))
- [AVVideoCodecType](/documentation/avfoundation/avvideocodectype)

##### Video codecs

- [static let h264: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/h264)
- [static let hevc: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevc)
- [static let hevcWithAlpha: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/hevcwithalpha)
- [static let jpeg: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpeg)
- [static let JPEGXL: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/jpegxl)
- [static let proRes422: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422)
- [static let proRes422LT: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422lt)
- [static let proRes422HQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422hq)
- [static let proRes422Proxy: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores422proxy)
- [static let proRes4444: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/prores4444)
- [static let proResRAW: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresraw)
- [static let proResRAWHQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/proresrawhq)
- [static let appleProRes4444XQ: AVVideoCodecType](/documentation/avfoundation/avvideocodectype/appleprores4444xq)

##### Deprecated

- [let AVVideoCodecH264: String](/documentation/avfoundation/avvideocodech264)
- [let AVVideoCodecHEVC: String](/documentation/avfoundation/avvideocodechevc)
- [let AVVideoCodecJPEG: String](/documentation/avfoundation/avvideocodecjpeg)
- [let AVVideoCodecAppleProRes422: String](/documentation/avfoundation/avvideocodecappleprores422)
- [let AVVideoCodecAppleProRes4444: String](/documentation/avfoundation/avvideocodecappleprores4444)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideocodectype/init(rawvalue:))

#### Receiving captured video data

- [func setSampleBufferDelegate((any AVCaptureVideoDataOutputSampleBufferDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avcapturevideodataoutput/setsamplebufferdelegate(_:queue:))
- [var sampleBufferDelegate: (any AVCaptureVideoDataOutputSampleBufferDelegate)?](/documentation/avfoundation/avcapturevideodataoutput/samplebufferdelegate)
- [var sampleBufferCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcapturevideodataoutput/samplebuffercallbackqueue)
- [AVCaptureVideoDataOutputSampleBufferDelegate](/documentation/avfoundation/avcapturevideodataoutputsamplebufferdelegate)

##### Managing sample buffer behavior

- [func captureOutput(AVCaptureOutput, didOutput: CMSampleBuffer, from: AVCaptureConnection)](/documentation/avfoundation/avcapturevideodataoutputsamplebufferdelegate/captureoutput(_:didoutput:from:))
- [func captureOutput(AVCaptureOutput, didDrop: CMSampleBuffer, from: AVCaptureConnection)](/documentation/avfoundation/avcapturevideodataoutputsamplebufferdelegate/captureoutput(_:diddrop:from:))

#### Creating video capture output

- [init()](/documentation/avfoundation/avcapturevideodataoutput/init())
- [AVCaptureAudioDataOutput](/documentation/avfoundation/avcaptureaudiodataoutput)

#### Creating an audio capture output

- [init()](/documentation/avfoundation/avcaptureaudiodataoutput/init())

#### Configuring audio capture

- [var audioSettings: [String : Any]!](/documentation/avfoundation/avcaptureaudiodataoutput/audiosettings)
- [func recommendedAudioSettingsForAssetWriter(writingTo: AVFileType) -> [String : Any]?](/documentation/avfoundation/avcaptureaudiodataoutput/recommendedaudiosettingsforassetwriter(writingto:))
- [var spatialAudioChannelLayoutTag: AudioChannelLayoutTag](/documentation/avfoundation/avcaptureaudiodataoutput/spatialaudiochannellayouttag)

#### Receiving captured audio data

- [func setSampleBufferDelegate((any AVCaptureAudioDataOutputSampleBufferDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avcaptureaudiodataoutput/setsamplebufferdelegate(_:queue:))
- [var sampleBufferDelegate: (any AVCaptureAudioDataOutputSampleBufferDelegate)?](/documentation/avfoundation/avcaptureaudiodataoutput/samplebufferdelegate)
- [var sampleBufferCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcaptureaudiodataoutput/samplebuffercallbackqueue)
- [AVCaptureAudioDataOutputSampleBufferDelegate](/documentation/avfoundation/avcaptureaudiodataoutputsamplebufferdelegate)

##### Managing sample buffer behavior

- [func captureOutput(AVCaptureOutput, didOutput: CMSampleBuffer, from: AVCaptureConnection)](/documentation/avfoundation/avcaptureaudiodataoutputsamplebufferdelegate/captureoutput(_:didoutput:from:))
- [AVCaptureSpatialAudioMetadataSampleGenerator](/documentation/avfoundation/avcapturespatialaudiometadatasamplegenerator)

#### Analyzing audio samples

- [func analyzeAudioSample(CMSampleBuffer) -> OSStatus](/documentation/avfoundation/avcapturespatialaudiometadatasamplegenerator/analyzeaudiosample(_:))
- [func newTimedMetadataSampleBufferAndResetAnalyzer() -> Unmanaged<CMSampleBuffer>?](/documentation/avfoundation/avcapturespatialaudiometadatasamplegenerator/newtimedmetadatasamplebufferandresetanalyzer())
- [var timedMetadataSampleBufferFormatDescription: CMFormatDescription](/documentation/avfoundation/avcapturespatialaudiometadatasamplegenerator/timedmetadatasamplebufferformatdescription)
- [func resetAnalyzer()](/documentation/avfoundation/avcapturespatialaudiometadatasamplegenerator/resetanalyzer())

### Mac screen capture

- [AVCaptureScreenInput](/documentation/avfoundation/avcapturescreeninput)

#### Initializing a capture screen input

- [init?(displayID: CGDirectDisplayID)](/documentation/avfoundation/avcapturescreeninput/init(displayid:))
- [init()](/documentation/avfoundation/avcapturescreeninput/init())

#### Setting video capture options

- [var minFrameDuration: CMTime](/documentation/avfoundation/avcapturescreeninput/minframeduration)
- [var cropRect: CGRect](/documentation/avfoundation/avcapturescreeninput/croprect)
- [var scaleFactor: CGFloat](/documentation/avfoundation/avcapturescreeninput/scalefactor)

#### Capturing mouse activity

- [var capturesCursor: Bool](/documentation/avfoundation/avcapturescreeninput/capturescursor)
- [var capturesMouseClicks: Bool](/documentation/avfoundation/avcapturescreeninput/capturesmouseclicks)

#### Deprecated

- [var removesDuplicateFrames: Bool](/documentation/avfoundation/avcapturescreeninput/removesduplicateframes)
- [Additional data capture](/documentation/avfoundation/additional-data-capture)

### Depth data capture

- [Capturing photos with depth](/documentation/avfoundation/capturing-photos-with-depth)
- [Creating auxiliary depth data manually](/documentation/avfoundation/creating-auxiliary-depth-data-manually)
- [Capturing depth using the LiDAR camera](/documentation/avfoundation/capturing-depth-using-the-lidar-camera)
- [AVCamFilter: Applying filters to a capture stream](/documentation/avfoundation/avcamfilter-applying-filters-to-a-capture-stream)
- [Streaming depth data from the TrueDepth camera](/documentation/avfoundation/streaming-depth-data-from-the-truedepth-camera)
- [Enhancing live video by leveraging TrueDepth camera data](/documentation/avfoundation/enhancing-live-video-by-leveraging-truedepth-camera-data)
- [AVCaptureDepthDataOutput](/documentation/avfoundation/avcapturedepthdataoutput)

#### Creating a depth data output

- [init()](/documentation/avfoundation/avcapturedepthdataoutput/init())

#### Configuring depth data capture

- [var alwaysDiscardsLateDepthData: Bool](/documentation/avfoundation/avcapturedepthdataoutput/alwaysdiscardslatedepthdata)
- [var isFilteringEnabled: Bool](/documentation/avfoundation/avcapturedepthdataoutput/isfilteringenabled)

#### Receiving captured depth data

- [func setDelegate((any AVCaptureDepthDataOutputDelegate)?, callbackQueue: dispatch_queue_t?)](/documentation/avfoundation/avcapturedepthdataoutput/setdelegate(_:callbackqueue:))
- [var delegate: (any AVCaptureDepthDataOutputDelegate)?](/documentation/avfoundation/avcapturedepthdataoutput/delegate)
- [var delegateCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcapturedepthdataoutput/delegatecallbackqueue)
- [AVCaptureDepthDataOutputDelegate](/documentation/avfoundation/avcapturedepthdataoutputdelegate)

##### Receiving depth data

- [func depthDataOutput(AVCaptureDepthDataOutput, didOutput: AVDepthData, timestamp: CMTime, connection: AVCaptureConnection)](/documentation/avfoundation/avcapturedepthdataoutputdelegate/depthdataoutput(_:didoutput:timestamp:connection:))
- [func depthDataOutput(AVCaptureDepthDataOutput, didDrop: AVDepthData, timestamp: CMTime, connection: AVCaptureConnection, reason: AVCaptureOutput.DataDroppedReason)](/documentation/avfoundation/avcapturedepthdataoutputdelegate/depthdataoutput(_:diddrop:timestamp:connection:reason:))
- [AVCaptureOutput.DataDroppedReason](/documentation/avfoundation/avcaptureoutput/datadroppedreason)

###### Reasons

- [case none](/documentation/avfoundation/avcaptureoutput/datadroppedreason/none)
- [case lateData](/documentation/avfoundation/avcaptureoutput/datadroppedreason/latedata)
- [case outOfBuffers](/documentation/avfoundation/avcaptureoutput/datadroppedreason/outofbuffers)
- [case discontinuity](/documentation/avfoundation/avcaptureoutput/datadroppedreason/discontinuity)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avcaptureoutput/datadroppedreason/init(rawvalue:))
- [AVDepthData](/documentation/avfoundation/avdepthdata)

#### Creating depth data

- [convenience init(fromDictionaryRepresentation: [AnyHashable : Any]) throws](/documentation/avfoundation/avdepthdata/init(fromdictionaryrepresentation:))
- [func dictionaryRepresentation(forAuxiliaryDataType: AutoreleasingUnsafeMutablePointer<NSString?>?) -> [AnyHashable : Any]?](/documentation/avfoundation/avdepthdata/dictionaryrepresentation(forauxiliarydatatype:))

#### Reading pixel depth information

- [var depthDataMap: CVPixelBuffer](/documentation/avfoundation/avdepthdata/depthdatamap)
- [var depthDataType: OSType](/documentation/avfoundation/avdepthdata/depthdatatype)

#### Evaluating depth data

- [var isDepthDataFiltered: Bool](/documentation/avfoundation/avdepthdata/isdepthdatafiltered)
- [var depthDataAccuracy: AVDepthData.Accuracy](/documentation/avfoundation/avdepthdata/depthdataaccuracy)
- [AVDepthData.Accuracy](/documentation/avfoundation/avdepthdata/accuracy)

##### Accuracy values

- [case relative](/documentation/avfoundation/avdepthdata/accuracy/relative)
- [case absolute](/documentation/avfoundation/avdepthdata/accuracy/absolute)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avdepthdata/accuracy/init(rawvalue:))
- [var depthDataQuality: AVDepthData.Quality](/documentation/avfoundation/avdepthdata/depthdataquality)
- [AVDepthData.Quality](/documentation/avfoundation/avdepthdata/quality)

##### Depth quality values

- [case low](/documentation/avfoundation/avdepthdata/quality/low)
- [case high](/documentation/avfoundation/avdepthdata/quality/high)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/avdepthdata/quality/init(rawvalue:))

#### Transforming and processing

- [func applyingExifOrientation(CGImagePropertyOrientation) -> Self](/documentation/avfoundation/avdepthdata/applyingexiforientation(_:))
- [func converting(toDepthDataType: OSType) -> Self](/documentation/avfoundation/avdepthdata/converting(todepthdatatype:))
- [var availableDepthDataTypes: [OSType]](/documentation/avfoundation/avdepthdata/availabledepthdatatypes-3ifx1)
- [func replacingDepthDataMap(with: CVPixelBuffer) throws -> Self](/documentation/avfoundation/avdepthdata/replacingdepthdatamap(with:))

#### Using calibration data

- [var cameraCalibrationData: AVCameraCalibrationData?](/documentation/avfoundation/avdepthdata/cameracalibrationdata)
- [AVCameraCalibrationData](/documentation/avfoundation/avcameracalibrationdata)

#### Mapping pixels to scene geometry

- [var intrinsicMatrix: matrix_float3x3](/documentation/avfoundation/avcameracalibrationdata/intrinsicmatrix)
- [var intrinsicMatrixReferenceDimensions: CGSize](/documentation/avfoundation/avcameracalibrationdata/intrinsicmatrixreferencedimensions)
- [var extrinsicMatrix: matrix_float4x3](/documentation/avfoundation/avcameracalibrationdata/extrinsicmatrix)
- [var pixelSize: Float](/documentation/avfoundation/avcameracalibrationdata/pixelsize)

#### Correcting for lens distortion

- [var lensDistortionLookupTable: Data?](/documentation/avfoundation/avcameracalibrationdata/lensdistortionlookuptable)
- [var inverseLensDistortionLookupTable: Data?](/documentation/avfoundation/avcameracalibrationdata/inverselensdistortionlookuptable)
- [var lensDistortionCenter: CGPoint](/documentation/avfoundation/avcameracalibrationdata/lensdistortioncenter)

### Metadata capture

- [AVCaptureMetadataInput](/documentation/avfoundation/avcapturemetadatainput)

#### Creating metadata input

- [init(formatDescription: CMMetadataFormatDescription, clock: CMClock)](/documentation/avfoundation/avcapturemetadatainput/init(formatdescription:clock:))

#### Providing metadata

- [func append(AVTimedMetadataGroup) throws](/documentation/avfoundation/avcapturemetadatainput/append(_:))
- [AVCaptureMetadataOutput](/documentation/avfoundation/avcapturemetadataoutput)

#### Creating metadata output

- [init()](/documentation/avfoundation/avcapturemetadataoutput/init())

#### Configuring metadata capture

- [var availableMetadataObjectTypes: [AVMetadataObject.ObjectType]](/documentation/avfoundation/avcapturemetadataoutput/availablemetadataobjecttypes)
- [var metadataObjectTypes: [AVMetadataObject.ObjectType]!](/documentation/avfoundation/avcapturemetadataoutput/metadataobjecttypes)
- [var rectOfInterest: CGRect](/documentation/avfoundation/avcapturemetadataoutput/rectofinterest)
- [var requiredMetadataObjectTypesForCinematicVideoCapture: [AVMetadataObject.ObjectType]](/documentation/avfoundation/avcapturemetadataoutput/requiredmetadataobjecttypesforcinematicvideocapture)

#### Receiving captured metadata objects

- [func setMetadataObjectsDelegate((any AVCaptureMetadataOutputObjectsDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avcapturemetadataoutput/setmetadataobjectsdelegate(_:queue:))
- [var metadataObjectsDelegate: (any AVCaptureMetadataOutputObjectsDelegate)?](/documentation/avfoundation/avcapturemetadataoutput/metadataobjectsdelegate)
- [var metadataObjectsCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcapturemetadataoutput/metadataobjectscallbackqueue)
- [AVCaptureMetadataOutputObjectsDelegate](/documentation/avfoundation/avcapturemetadataoutputobjectsdelegate)

##### Processing emitted metadata objects

- [func metadataOutput(AVCaptureMetadataOutput, didOutput: [AVMetadataObject], from: AVCaptureConnection)](/documentation/avfoundation/avcapturemetadataoutputobjectsdelegate/metadataoutput(_:didoutput:from:))
- [AVMetadataObject](/documentation/avfoundation/avmetadataobject)

#### Inspecting the metadata

- [var bounds: CGRect](/documentation/avfoundation/avmetadataobject/bounds)
- [var duration: CMTime](/documentation/avfoundation/avmetadataobject/duration)
- [var time: CMTime](/documentation/avfoundation/avmetadataobject/time)
- [var type: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/type)
- [AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype)

##### Barcodes

- [static let codabar: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/codabar)
- [static let code39: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code39)
- [static let code39Mod43: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code39mod43)
- [static let code93: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code93)
- [static let code128: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code128)
- [static let ean8: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/ean8)
- [static let ean13: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/ean13)
- [static let gs1DataBar: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/gs1databar)
- [static let gs1DataBarExpanded: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/gs1databarexpanded)
- [static let gs1DataBarLimited: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/gs1databarlimited)
- [static let interleaved2of5: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/interleaved2of5)
- [static let itf14: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/itf14)
- [static let upce: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/upce)

##### 2D codes

- [static let aztec: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/aztec)
- [static let dataMatrix: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/datamatrix)
- [static let microPDF417: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/micropdf417)
- [static let microQR: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/microqr)
- [static let pdf417: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/pdf417)
- [static let qr: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/qr)

##### Bodies

- [static let humanBody: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/humanbody)
- [static let humanFullBody: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/humanfullbody)
- [static let dogHead: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/doghead)
- [static let dogBody: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/dogbody)
- [static let catHead: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/cathead)
- [static let catBody: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/catbody)

##### Faces

- [static let face: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/face)

##### Saliency

- [static let salientObject: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/salientobject)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avmetadataobject/objecttype/init(rawvalue:))
- [var isFixedFocus: Bool](/documentation/avfoundation/avmetadataobject/isfixedfocus)
- [var cinematicVideoFocusMode: AVCaptureDevice.CinematicVideoFocusMode](/documentation/avfoundation/avmetadataobject/cinematicvideofocusmode)
- [var groupID: Int](/documentation/avfoundation/avmetadataobject/groupid)
- [var objectID: Int](/documentation/avfoundation/avmetadataobject/objectid)
- [Metadata types](/documentation/avfoundation/metadata-types)

#### 2D and 3D codes

- [AVMetadataMachineReadableCodeObject](/documentation/avfoundation/avmetadatamachinereadablecodeobject)

##### Getting machine-readable code values

- [var corners: [CGPoint]](/documentation/avfoundation/avmetadatamachinereadablecodeobject/corners-58qbe)
- [var descriptor: CIBarcodeDescriptor?](/documentation/avfoundation/avmetadatamachinereadablecodeobject/descriptor)
- [var stringValue: String?](/documentation/avfoundation/avmetadatamachinereadablecodeobject/stringvalue)

##### Constants

- [Machine-readable object types](/documentation/avfoundation/machine-readable-object-types)

###### Constants

- [static let upce: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/upce)
- [static let code39: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code39)
- [static let code39Mod43: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code39mod43)
- [static let ean13: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/ean13)
- [static let ean8: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/ean8)
- [static let code93: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code93)
- [static let code128: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/code128)
- [static let pdf417: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/pdf417)
- [static let qr: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/qr)
- [static let aztec: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/aztec)
- [static let interleaved2of5: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/interleaved2of5)
- [static let itf14: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/itf14)
- [static let dataMatrix: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/datamatrix)

#### Faces

- [AVMetadataFaceObject](/documentation/avfoundation/avmetadatafaceobject)

##### Getting the face identifier

- [var faceID: Int](/documentation/avfoundation/avmetadatafaceobject/faceid)

##### Accessing the face detection data

- [var hasRollAngle: Bool](/documentation/avfoundation/avmetadatafaceobject/hasrollangle)
- [var rollAngle: CGFloat](/documentation/avfoundation/avmetadatafaceobject/rollangle)
- [var hasYawAngle: Bool](/documentation/avfoundation/avmetadatafaceobject/hasyawangle)
- [var yawAngle: CGFloat](/documentation/avfoundation/avmetadatafaceobject/yawangle)

##### Constants

- [Face metadata type](/documentation/avfoundation/face-metadata-type)

###### Constants

- [static let face: AVMetadataObject.ObjectType](/documentation/avfoundation/avmetadataobject/objecttype/face)

#### Heads

- [AVMetadataCatHeadObject](/documentation/avfoundation/avmetadatacatheadobject)
- [AVMetadataDogHeadObject](/documentation/avfoundation/avmetadatadogheadobject)

#### Bodies

- [AVMetadataBodyObject](/documentation/avfoundation/avmetadatabodyobject)

##### Inspecting metadata

- [var bodyID: Int](/documentation/avfoundation/avmetadatabodyobject/bodyid)
- [AVMetadataCatBodyObject](/documentation/avfoundation/avmetadatacatbodyobject)
- [AVMetadataDogBodyObject](/documentation/avfoundation/avmetadatadogbodyobject)
- [AVMetadataHumanBodyObject](/documentation/avfoundation/avmetadatahumanbodyobject)
- [AVMetadataHumanFullBodyObject](/documentation/avfoundation/avmetadatahumanfullbodyobject)

#### Saliency

- [AVMetadataSalientObject](/documentation/avfoundation/avmetadatasalientobject)

##### Inspecting metadata

- [var objectID: Int](/documentation/avfoundation/avmetadatasalientobject/objectid)

### Synchronized capture

- [AVCaptureDataOutputSynchronizer](/documentation/avfoundation/avcapturedataoutputsynchronizer)

#### Configuring synchronized capture

- [init(dataOutputs: [AVCaptureOutput])](/documentation/avfoundation/avcapturedataoutputsynchronizer/init(dataoutputs:))
- [var dataOutputs: [AVCaptureOutput]](/documentation/avfoundation/avcapturedataoutputsynchronizer/dataoutputs)

#### Receiving synchronized capture data

- [func setDelegate((any AVCaptureDataOutputSynchronizerDelegate)?, queue: dispatch_queue_t?)](/documentation/avfoundation/avcapturedataoutputsynchronizer/setdelegate(_:queue:))
- [var delegate: (any AVCaptureDataOutputSynchronizerDelegate)?](/documentation/avfoundation/avcapturedataoutputsynchronizer/delegate)
- [var delegateCallbackQueue: dispatch_queue_t?](/documentation/avfoundation/avcapturedataoutputsynchronizer/delegatecallbackqueue)
- [AVCaptureDataOutputSynchronizerDelegate](/documentation/avfoundation/avcapturedataoutputsynchronizerdelegate)

##### Receiving synchronized capture data

- [func dataOutputSynchronizer(AVCaptureDataOutputSynchronizer, didOutput: AVCaptureSynchronizedDataCollection)](/documentation/avfoundation/avcapturedataoutputsynchronizerdelegate/dataoutputsynchronizer(_:didoutput:))
- [AVCaptureSynchronizedDataCollection](/documentation/avfoundation/avcapturesynchronizeddatacollection)

#### Accessing synchronized data

- [var count: Int](/documentation/avfoundation/avcapturesynchronizeddatacollection/count)
- [func synchronizedData(for: AVCaptureOutput) -> AVCaptureSynchronizedData?](/documentation/avfoundation/avcapturesynchronizeddatacollection/synchronizeddata(for:))
- [subscript(AVCaptureOutput) -> AVCaptureSynchronizedData?](/documentation/avfoundation/avcapturesynchronizeddatacollection/subscript(_:))
- [AVCaptureSynchronizedSampleBufferData](/documentation/avfoundation/avcapturesynchronizedsamplebufferdata)

#### Accessing synchronized data

- [var sampleBuffer: CMSampleBuffer](/documentation/avfoundation/avcapturesynchronizedsamplebufferdata/samplebuffer)

#### Handling dropped data

- [var sampleBufferWasDropped: Bool](/documentation/avfoundation/avcapturesynchronizedsamplebufferdata/samplebufferwasdropped)
- [var droppedReason: AVCaptureOutput.DataDroppedReason](/documentation/avfoundation/avcapturesynchronizedsamplebufferdata/droppedreason)
- [AVCaptureSynchronizedMetadataObjectData](/documentation/avfoundation/avcapturesynchronizedmetadataobjectdata)

#### Accessing synchronized data

- [var metadataObjects: [AVMetadataObject]](/documentation/avfoundation/avcapturesynchronizedmetadataobjectdata/metadataobjects)
- [AVCaptureSynchronizedDepthData](/documentation/avfoundation/avcapturesynchronizeddepthdata)

#### Accessing synchronized data

- [var depthData: AVDepthData](/documentation/avfoundation/avcapturesynchronizeddepthdata/depthdata)

#### Handling dropped data

- [var depthDataWasDropped: Bool](/documentation/avfoundation/avcapturesynchronizeddepthdata/depthdatawasdropped)
- [var droppedReason: AVCaptureOutput.DataDroppedReason](/documentation/avfoundation/avcapturesynchronizeddepthdata/droppedreason)
- [AVCaptureSynchronizedData](/documentation/avfoundation/avcapturesynchronizeddata)

#### Correlating synchronized data

- [var timestamp: CMTime](/documentation/avfoundation/avcapturesynchronizeddata/timestamp)

## Editing

- [Composite assets](/documentation/avfoundation/composite-assets)

### Compositions

- [AVComposition](/documentation/avfoundation/avcomposition)

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVCompositionTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-9eows)
- [func loadTrack(withTrackID: CMPersistentTrackID, completionHandler: (AVCompositionTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avcomposition/loadtrack(withtrackid:completionhandler:))
- [func loadTracks(withMediaType: AVMediaType, completionHandler: ([AVCompositionTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avcomposition/loadtracks(withmediatype:completionhandler:))
- [func loadTracks(withMediaCharacteristic: AVMediaCharacteristic, completionHandler: ([AVCompositionTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avcomposition/loadtracks(withmediacharacteristic:completionhandler:))

#### Accessing tracks

- [var tracks: [AVCompositionTrack]](/documentation/avfoundation/avcomposition/tracks)
- [func track(withTrackID: CMPersistentTrackID) -> AVCompositionTrack?](/documentation/avfoundation/avcomposition/track(withtrackid:))
- [func tracks(withMediaType: AVMediaType) -> [AVCompositionTrack]](/documentation/avfoundation/avcomposition/tracks(withmediatype:))
- [func tracks(withMediaCharacteristic: AVMediaCharacteristic) -> [AVCompositionTrack]](/documentation/avfoundation/avcomposition/tracks(withmediacharacteristic:))
- [func unusedTrackID() -> CMPersistentTrackID](/documentation/avfoundation/avcomposition/unusedtrackid())

#### Accessing track groups

- [var trackGroups: [AVAssetTrackGroup]](/documentation/avfoundation/avcomposition/trackgroups)

#### Accessing duration and timing

- [var duration: CMTime](/documentation/avfoundation/avcomposition/duration)
- [var providesPreciseDurationAndTiming: Bool](/documentation/avfoundation/avcomposition/providesprecisedurationandtiming)
- [var minimumTimeOffsetFromLive: CMTime](/documentation/avfoundation/avcomposition/minimumtimeoffsetfromlive)

#### Accessing metadata

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avcomposition/metadata)
- [var commonMetadata: [AVMetadataItem]](/documentation/avfoundation/avcomposition/commonmetadata)
- [var availableMetadataFormats: [AVMetadataFormat]](/documentation/avfoundation/avcomposition/availablemetadataformats)
- [func metadata(forFormat: AVMetadataFormat) -> [AVMetadataItem]](/documentation/avfoundation/avcomposition/metadata(forformat:))
- [var creationDate: AVMetadataItem?](/documentation/avfoundation/avcomposition/creationdate)
- [var lyrics: String?](/documentation/avfoundation/avcomposition/lyrics)

#### Determining suitability

- [var isPlayable: Bool](/documentation/avfoundation/avcomposition/isplayable)
- [var isReadable: Bool](/documentation/avfoundation/avcomposition/isreadable)
- [var isExportable: Bool](/documentation/avfoundation/avcomposition/isexportable)
- [var isComposable: Bool](/documentation/avfoundation/avcomposition/iscomposable)
- [var isCompatibleWithAirPlayVideo: Bool](/documentation/avfoundation/avcomposition/iscompatiblewithairplayvideo)
- [var isCompatibleWithSavedPhotosAlbum: Bool](/documentation/avfoundation/avcomposition/iscompatiblewithsavedphotosalbum)

#### Inspecting preferences

- [var preferredRate: Float](/documentation/avfoundation/avcomposition/preferredrate)
- [var preferredVolume: Float](/documentation/avfoundation/avcomposition/preferredvolume)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avcomposition/preferredtransform)
- [var preferredMediaSelection: AVMediaSelection](/documentation/avfoundation/avcomposition/preferredmediaselection)
- [var preferredDisplayCriteria: AVDisplayCriteria](/documentation/avfoundation/avcomposition/preferreddisplaycriteria)

#### Accessing media selections

- [var allMediaSelections: [AVMediaSelection]](/documentation/avfoundation/avcomposition/allmediaselections)
- [var availableMediaCharacteristicsWithMediaSelectionOptions: [AVMediaCharacteristic]](/documentation/avfoundation/avcomposition/availablemediacharacteristicswithmediaselectionoptions)
- [func mediaSelectionGroup(forMediaCharacteristic: AVMediaCharacteristic) -> AVMediaSelectionGroup?](/documentation/avfoundation/avcomposition/mediaselectiongroup(formediacharacteristic:))

#### Accessing chapter metadata

- [var availableChapterLocales: [Locale]](/documentation/avfoundation/avcomposition/availablechapterlocales)
- [func chapterMetadataGroups(bestMatchingPreferredLanguages: [String]) -> [AVTimedMetadataGroup]](/documentation/avfoundation/avcomposition/chaptermetadatagroups(bestmatchingpreferredlanguages:))
- [func chapterMetadataGroups(withTitleLocale: Locale, containingItemsWithCommonKeys: [AVMetadataKey]?) -> [AVTimedMetadataGroup]](/documentation/avfoundation/avcomposition/chaptermetadatagroups(withtitlelocale:containingitemswithcommonkeys:))

#### Accessing visual dimensions

- [var naturalSize: CGSize](/documentation/avfoundation/avcomposition/naturalsize)

#### Accessing initialization options

- [var urlAssetInitializationOptions: [String : Any]](/documentation/avfoundation/avcomposition/urlassetinitializationoptions)

#### Determining content protections

- [var hasProtectedContent: Bool](/documentation/avfoundation/avcomposition/hasprotectedcontent)

#### Determining fragment support

- [var canContainFragments: Bool](/documentation/avfoundation/avcomposition/cancontainfragments)
- [var containsFragments: Bool](/documentation/avfoundation/avcomposition/containsfragments)
- [var overallDurationHint: CMTime](/documentation/avfoundation/avcomposition/overalldurationhint)
- [AVCompositionTrack](/documentation/avfoundation/avcompositiontrack)

#### Accessing track information

- [var isPlayable: Bool](/documentation/avfoundation/avcompositiontrack/isplayable)
- [var isDecodable: Bool](/documentation/avfoundation/avcompositiontrack/isdecodable)
- [var isEnabled: Bool](/documentation/avfoundation/avcompositiontrack/isenabled)
- [var isSelfContained: Bool](/documentation/avfoundation/avcompositiontrack/isselfcontained)
- [var totalSampleDataLength: Int64](/documentation/avfoundation/avcompositiontrack/totalsampledatalength)
- [func hasMediaCharacteristic(AVMediaCharacteristic) -> Bool](/documentation/avfoundation/avcompositiontrack/hasmediacharacteristic(_:))

#### Accessing temporal information

- [var timeRange: CMTimeRange](/documentation/avfoundation/avcompositiontrack/timerange)
- [var naturalTimeScale: CMTimeScale](/documentation/avfoundation/avcompositiontrack/naturaltimescale)
- [var estimatedDataRate: Float](/documentation/avfoundation/avcompositiontrack/estimateddatarate)
- [func samplePresentationTime(forTrackTime: CMTime) -> CMTime](/documentation/avfoundation/avcompositiontrack/samplepresentationtime(fortracktime:))

#### Accessing language support

- [var languageCode: String?](/documentation/avfoundation/avcompositiontrack/languagecode)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avcompositiontrack/extendedlanguagetag)

#### Managing format descriptions

- [var formatDescriptions: [Any]](/documentation/avfoundation/avcompositiontrack/formatdescriptions)
- [var formatDescriptionReplacements: [AVCompositionTrackFormatDescriptionReplacement]](/documentation/avfoundation/avcompositiontrack/formatdescriptionreplacements)
- [AVCompositionTrackFormatDescriptionReplacement](/documentation/avfoundation/avcompositiontrackformatdescriptionreplacement)

##### Managing format descriptions

- [var originalFormatDescription: CMFormatDescription](/documentation/avfoundation/avcompositiontrackformatdescriptionreplacement/originalformatdescription)
- [var replacementFormatDescription: CMFormatDescription](/documentation/avfoundation/avcompositiontrackformatdescriptionreplacement/replacementformatdescription)

#### Accessing visual characteristics

- [var naturalSize: CGSize](/documentation/avfoundation/avcompositiontrack/naturalsize)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avcompositiontrack/preferredtransform)

#### Accessing audible characteristics

- [var preferredVolume: Float](/documentation/avfoundation/avcompositiontrack/preferredvolume)
- [var hasAudioSampleDependencies: Bool](/documentation/avfoundation/avcompositiontrack/hasaudiosampledependencies)

#### Accessing frame-based characteristics

- [var nominalFrameRate: Float](/documentation/avfoundation/avcompositiontrack/nominalframerate)
- [var minFrameDuration: CMTime](/documentation/avfoundation/avcompositiontrack/minframeduration)
- [var requiresFrameReordering: Bool](/documentation/avfoundation/avcompositiontrack/requiresframereordering)

#### Accessing metadata

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avcompositiontrack/metadata)
- [var commonMetadata: [AVMetadataItem]](/documentation/avfoundation/avcompositiontrack/commonmetadata)
- [var availableMetadataFormats: [AVMetadataFormat]](/documentation/avfoundation/avcompositiontrack/availablemetadataformats)
- [func metadata(forFormat: AVMetadataFormat) -> [AVMetadataItem]](/documentation/avfoundation/avcompositiontrack/metadata(forformat:))

#### Accessing track segments

- [var segments: [AVCompositionTrackSegment]](/documentation/avfoundation/avcompositiontrack/segments)
- [func segment(forTrackTime: CMTime) -> AVCompositionTrackSegment?](/documentation/avfoundation/avcompositiontrack/segment(fortracktime:))

#### Accessing track associations

- [var availableTrackAssociationTypes: [AVAssetTrack.AssociationType]](/documentation/avfoundation/avcompositiontrack/availabletrackassociationtypes)
- [func associatedTracks(ofType: AVAssetTrack.AssociationType) -> [AVAssetTrack]](/documentation/avfoundation/avcompositiontrack/associatedtracks(oftype:))

#### Determining sample cursor support

- [var canProvideSampleCursors: Bool](/documentation/avfoundation/avcompositiontrack/canprovidesamplecursors)
- [AVCompositionTrackSegment](/documentation/avfoundation/avcompositiontracksegment)

#### Creating a segment

- [init(timeRange: CMTimeRange)](/documentation/avfoundation/avcompositiontracksegment/init(timerange:))
- [init(url: URL, trackID: CMPersistentTrackID, sourceTimeRange: CMTimeRange, targetTimeRange: CMTimeRange)](/documentation/avfoundation/avcompositiontracksegment/init(url:trackid:sourcetimerange:targettimerange:))

#### Accessing segment properties

- [var sourceURL: URL?](/documentation/avfoundation/avcompositiontracksegment/sourceurl)
- [var sourceTrackID: CMPersistentTrackID](/documentation/avfoundation/avcompositiontracksegment/sourcetrackid)
- [var isEmpty: Bool](/documentation/avfoundation/avcompositiontracksegment/isempty)

### Mutable compositions

- [AVMutableComposition](/documentation/avfoundation/avmutablecomposition)

#### Creating a composition

- [convenience init(urlAssetInitializationOptions: [String : Any]?)](/documentation/avfoundation/avmutablecomposition/init(urlassetinitializationoptions:))

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVMutableCompositionTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-92p4a)
- [func loadTrack(withTrackID: CMPersistentTrackID, completionHandler: (AVMutableCompositionTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablecomposition/loadtrack(withtrackid:completionhandler:))
- [func loadTracks(withMediaType: AVMediaType, completionHandler: ([AVMutableCompositionTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablecomposition/loadtracks(withmediatype:completionhandler:))
- [func loadTracks(withMediaCharacteristic: AVMediaCharacteristic, completionHandler: ([AVMutableCompositionTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablecomposition/loadtracks(withmediacharacteristic:completionhandler:))

#### Accessing tracks

- [var tracks: [AVMutableCompositionTrack]](/documentation/avfoundation/avmutablecomposition/tracks)
- [func track(withTrackID: CMPersistentTrackID) -> AVMutableCompositionTrack?](/documentation/avfoundation/avmutablecomposition/track(withtrackid:))
- [func tracks(withMediaType: AVMediaType) -> [AVMutableCompositionTrack]](/documentation/avfoundation/avmutablecomposition/tracks(withmediatype:))
- [func tracks(withMediaCharacteristic: AVMediaCharacteristic) -> [AVMutableCompositionTrack]](/documentation/avfoundation/avmutablecomposition/tracks(withmediacharacteristic:))

#### Managing composition tracks

- [func mutableTrack(compatibleWith: AVAssetTrack) -> AVMutableCompositionTrack?](/documentation/avfoundation/avmutablecomposition/mutabletrack(compatiblewith:))
- [func addMutableTrack(withMediaType: AVMediaType, preferredTrackID: CMPersistentTrackID) -> AVMutableCompositionTrack?](/documentation/avfoundation/avmutablecomposition/addmutabletrack(withmediatype:preferredtrackid:))
- [func removeTrack(AVCompositionTrack)](/documentation/avfoundation/avmutablecomposition/removetrack(_:))

#### Managing Cinematic tracks

- [func addTracks(for: CNAssetInfo, preferredStartingTrackID: CMPersistentTrackID) -> CNCompositionInfo](/documentation/avfoundation/avmutablecomposition/addtracks(for:preferredstartingtrackid:))

#### Managing time ranges

- [func removeTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablecomposition/removetimerange(_:))
- [func scaleTimeRange(CMTimeRange, toDuration: CMTime)](/documentation/avfoundation/avmutablecomposition/scaletimerange(_:toduration:))
- [func insertEmptyTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablecomposition/insertemptytimerange(_:))
- [func insertTimeRange(CMTimeRange, of: AVAsset, at: CMTime, completionHandler: ((any Error)?) -> Void)](/documentation/avfoundation/avmutablecomposition/inserttimerange(_:of:at:completionhandler:))
- [func insertTimeRange(CMTimeRange, of: AVAsset, at: CMTime) throws](/documentation/avfoundation/avmutablecomposition/inserttimerange(_:of:at:))

#### Configuring video size

- [var naturalSize: CGSize](/documentation/avfoundation/avmutablecomposition/naturalsize)

#### Instance methods

- [func insertTimeRange(CMTimeRange, of: AVAsset, at: CMTime, isolation: isolated (any Actor)?) async throws](/documentation/avfoundation/avmutablecomposition/inserttimerange(_:of:at:isolation:))
- [AVMutableCompositionTrack](/documentation/avfoundation/avmutablecompositiontrack)

#### Configuring track properties

- [var isEnabled: Bool](/documentation/avfoundation/avmutablecompositiontrack/isenabled)
- [var naturalTimeScale: CMTimeScale](/documentation/avfoundation/avmutablecompositiontrack/naturaltimescale)
- [var languageCode: String?](/documentation/avfoundation/avmutablecompositiontrack/languagecode)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avmutablecompositiontrack/extendedlanguagetag)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avmutablecompositiontrack/preferredtransform)
- [var preferredVolume: Float](/documentation/avfoundation/avmutablecompositiontrack/preferredvolume)

#### Managing time ranges

- [var segments: [AVCompositionTrackSegment]!](/documentation/avfoundation/avmutablecompositiontrack/segments)
- [func insertEmptyTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablecompositiontrack/insertemptytimerange(_:))
- [func insertTimeRange(CMTimeRange, of: AVAssetTrack, at: CMTime) throws](/documentation/avfoundation/avmutablecompositiontrack/inserttimerange(_:of:at:))
- [func insertTimeRanges([NSValue], of: [AVAssetTrack], at: CMTime) throws](/documentation/avfoundation/avmutablecompositiontrack/inserttimeranges(_:of:at:))
- [func removeTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablecompositiontrack/removetimerange(_:))
- [func scaleTimeRange(CMTimeRange, toDuration: CMTime)](/documentation/avfoundation/avmutablecompositiontrack/scaletimerange(_:toduration:))

#### Associating tracks

- [func addTrackAssociation(to: AVCompositionTrack, type: AVAssetTrack.AssociationType)](/documentation/avfoundation/avmutablecompositiontrack/addtrackassociation(to:type:))
- [func removeTrackAssociation(to: AVCompositionTrack, type: AVAssetTrack.AssociationType)](/documentation/avfoundation/avmutablecompositiontrack/removetrackassociation(to:type:))

#### Replacing format descriptions

- [func replaceFormatDescription(CMFormatDescription, with: CMFormatDescription?)](/documentation/avfoundation/avmutablecompositiontrack/replaceformatdescription(_:with:))

#### Validating segments

- [func validateSegments([AVCompositionTrackSegment]) throws](/documentation/avfoundation/avmutablecompositiontrack/validatesegments(_:))
- [QuickTime movies](/documentation/avfoundation/quicktime-movies)

### Movies

- [AVMovie](/documentation/avfoundation/avmovie)

#### Creating a movie

- [convenience init(url: URL)](/documentation/avfoundation/avmovie/init(url:))
- [init(url: URL, options: [String : Any]?)](/documentation/avfoundation/avmovie/init(url:options:))
- [init(data: Data, options: [String : Any]?)](/documentation/avfoundation/avmovie/init(data:options:))
- [Initialization options](/documentation/avfoundation/initialization-options)

##### Options

- [let AVMovieReferenceRestrictionsKey: String](/documentation/avfoundation/avmoviereferencerestrictionskey)
- [let AVMovieShouldSupportAliasDataReferencesKey: String](/documentation/avfoundation/avmovieshouldsupportaliasdatareferenceskey)

#### Determining supported file types

- [class func movieTypes() -> [AVFileType]](/documentation/avfoundation/avmovie/movietypes())

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVMovieTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-80a83)
- [func loadTrack(withTrackID: CMPersistentTrackID, completionHandler: (AVMovieTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avmovie/loadtrack(withtrackid:completionhandler:))
- [func loadTracks(withMediaType: AVMediaType, completionHandler: ([AVMovieTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avmovie/loadtracks(withmediatype:completionhandler:))
- [func loadTracks(withMediaCharacteristic: AVMediaCharacteristic, completionHandler: ([AVMovieTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avmovie/loadtracks(withmediacharacteristic:completionhandler:))

#### Creating and writing headers

- [func `is`(compatibleWithFileType: AVFileType) -> Bool](/documentation/avfoundation/avmovie/is(compatiblewithfiletype:))
- [func makeMovieHeader(fileType: AVFileType) throws -> Data](/documentation/avfoundation/avmovie/makemovieheader(filetype:))
- [func writeHeader(to: URL, fileType: AVFileType, options: AVMovieWritingOptions) throws](/documentation/avfoundation/avmovie/writeheader(to:filetype:options:))
- [AVMovieWritingOptions](/documentation/avfoundation/avmoviewritingoptions)

##### Writing options

- [static var addMovieHeaderToDestination: AVMovieWritingOptions](/documentation/avfoundation/avmoviewritingoptions/addmovieheadertodestination)
- [static var truncateDestinationToMovieHeaderOnly: AVMovieWritingOptions](/documentation/avfoundation/avmoviewritingoptions/truncatedestinationtomovieheaderonly)

##### Initializers

- [init(rawValue: UInt)](/documentation/avfoundation/avmoviewritingoptions/init(rawvalue:))

#### Determining fragment support

- [var canContainMovieFragments: Bool](/documentation/avfoundation/avmovie/cancontainmoviefragments)
- [var containsMovieFragments: Bool](/documentation/avfoundation/avmovie/containsmoviefragments)

#### Accessing movie information

- [var url: URL?](/documentation/avfoundation/avmovie/url)
- [var data: Data?](/documentation/avfoundation/avmovie/data)

#### Accessing tracks

- [var tracks: [AVMovieTrack]](/documentation/avfoundation/avmovie/tracks)
- [func track(withTrackID: CMPersistentTrackID) -> AVMovieTrack?](/documentation/avfoundation/avmovie/track(withtrackid:))
- [func tracks(withMediaType: AVMediaType) -> [AVMovieTrack]](/documentation/avfoundation/avmovie/tracks(withmediatype:))
- [func tracks(withMediaCharacteristic: AVMediaCharacteristic) -> [AVMovieTrack]](/documentation/avfoundation/avmovie/tracks(withmediacharacteristic:))

#### Accessing data storage

- [var defaultMediaDataStorage: AVMediaDataStorage?](/documentation/avfoundation/avmovie/defaultmediadatastorage)
- [AVMovieTrack](/documentation/avfoundation/avmovietrack)

#### Retrieving track information

- [var alternateGroupID: Int](/documentation/avfoundation/avmovietrack/alternategroupid)
- [var mediaDataStorage: AVMediaDataStorage?](/documentation/avfoundation/avmovietrack/mediadatastorage)
- [var mediaDecodeTimeRange: CMTimeRange](/documentation/avfoundation/avmovietrack/mediadecodetimerange)
- [var mediaPresentationTimeRange: CMTimeRange](/documentation/avfoundation/avmovietrack/mediapresentationtimerange)

### Mutable movies

- [AVMutableMovie](/documentation/avfoundation/avmutablemovie)

#### Creating a movie

- [init(url: URL, options: [String : Any]?, error: ()) throws](/documentation/avfoundation/avmutablemovie/init(url:options:error:))
- [init(data: Data, options: [String : Any]?, error: ()) throws](/documentation/avfoundation/avmutablemovie/init(data:options:error:))
- [init(settingsFrom: AVMovie?, options: [String : Any]?) throws](/documentation/avfoundation/avmutablemovie/init(settingsfrom:options:))

#### Configuring a movie

- [var isModified: Bool](/documentation/avfoundation/avmutablemovie/ismodified)
- [var timescale: CMTimeScale](/documentation/avfoundation/avmutablemovie/timescale)
- [var interleavingPeriod: CMTime](/documentation/avfoundation/avmutablemovie/interleavingperiod)
- [var defaultMediaDataStorage: AVMediaDataStorage?](/documentation/avfoundation/avmutablemovie/defaultmediadatastorage)

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVMutableMovieTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-2lj40)
- [func loadTrack(withTrackID: CMPersistentTrackID, completionHandler: (AVMutableMovieTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablemovie/loadtrack(withtrackid:completionhandler:))
- [func loadTracks(withMediaType: AVMediaType, completionHandler: ([AVMutableMovieTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablemovie/loadtracks(withmediatype:completionhandler:))
- [func loadTracks(withMediaCharacteristic: AVMediaCharacteristic, completionHandler: ([AVMutableMovieTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablemovie/loadtracks(withmediacharacteristic:completionhandler:))

#### Accessing tracks

- [var tracks: [AVMutableMovieTrack]](/documentation/avfoundation/avmutablemovie/tracks)
- [func track(withTrackID: CMPersistentTrackID) -> AVMutableMovieTrack?](/documentation/avfoundation/avmutablemovie/track(withtrackid:))
- [func tracks(withMediaType: AVMediaType) -> [AVMutableMovieTrack]](/documentation/avfoundation/avmutablemovie/tracks(withmediatype:))
- [func tracks(withMediaCharacteristic: AVMediaCharacteristic) -> [AVMutableMovieTrack]](/documentation/avfoundation/avmutablemovie/tracks(withmediacharacteristic:))
- [func unusedTrackID() -> CMPersistentTrackID](/documentation/avfoundation/avmutablemovie/unusedtrackid())

#### Accessing track groups

- [var trackGroups: [AVAssetTrackGroup]](/documentation/avfoundation/avmutablemovie/trackgroups)

#### Managing tracks

- [func mutableTrack(compatibleWith: AVAssetTrack) -> AVMutableMovieTrack?](/documentation/avfoundation/avmutablemovie/mutabletrack(compatiblewith:))
- [func addMutableTrack(withMediaType: AVMediaType, copySettingsFrom: AVAssetTrack?, options: [String : Any]?) -> AVMutableMovieTrack?](/documentation/avfoundation/avmutablemovie/addmutabletrack(withmediatype:copysettingsfrom:options:))
- [func addMutableTracksCopyingSettings(from: [AVAssetTrack], options: [String : Any]?) -> [AVMutableMovieTrack]](/documentation/avfoundation/avmutablemovie/addmutabletrackscopyingsettings(from:options:))
- [func removeTrack(AVMovieTrack)](/documentation/avfoundation/avmutablemovie/removetrack(_:))

#### Managing time ranges

- [func insertEmptyTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablemovie/insertemptytimerange(_:))
- [func insertTimeRange(CMTimeRange, of: AVAsset, at: CMTime, copySampleData: Bool) throws](/documentation/avfoundation/avmutablemovie/inserttimerange(_:of:at:copysampledata:))
- [func scale(CMTimeRange, toDuration: CMTime)](/documentation/avfoundation/avmutablemovie/scale(_:toduration:))
- [func removeTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablemovie/removetimerange(_:))

#### Accessing duration and timing

- [var duration: CMTime](/documentation/avfoundation/avmutablemovie/duration)
- [var providesPreciseDurationAndTiming: Bool](/documentation/avfoundation/avmutablemovie/providesprecisedurationandtiming)
- [var minimumTimeOffsetFromLive: CMTime](/documentation/avfoundation/avmutablemovie/minimumtimeoffsetfromlive)

#### Accessing metadata

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avmutablemovie/metadata)
- [var commonMetadata: [AVMetadataItem]](/documentation/avfoundation/avmutablemovie/commonmetadata)
- [var availableMetadataFormats: [AVMetadataFormat]](/documentation/avfoundation/avmutablemovie/availablemetadataformats)
- [func metadata(forFormat: AVMetadataFormat) -> [AVMetadataItem]](/documentation/avfoundation/avmutablemovie/metadata(forformat:))
- [var creationDate: AVMetadataItem?](/documentation/avfoundation/avmutablemovie/creationdate)
- [var lyrics: String?](/documentation/avfoundation/avmutablemovie/lyrics)

#### Determining suitability

- [var isPlayable: Bool](/documentation/avfoundation/avmutablemovie/isplayable)
- [var isReadable: Bool](/documentation/avfoundation/avmutablemovie/isreadable)
- [var isExportable: Bool](/documentation/avfoundation/avmutablemovie/isexportable)
- [var isComposable: Bool](/documentation/avfoundation/avmutablemovie/iscomposable)
- [var isCompatibleWithAirPlayVideo: Bool](/documentation/avfoundation/avmutablemovie/iscompatiblewithairplayvideo)
- [var isCompatibleWithSavedPhotosAlbum: Bool](/documentation/avfoundation/avmutablemovie/iscompatiblewithsavedphotosalbum)

#### Inspecting preferences

- [var preferredRate: Float](/documentation/avfoundation/avmutablemovie/preferredrate)
- [var preferredVolume: Float](/documentation/avfoundation/avmutablemovie/preferredvolume)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avmutablemovie/preferredtransform)
- [var preferredMediaSelection: AVMediaSelection](/documentation/avfoundation/avmutablemovie/preferredmediaselection)

#### Accessing media selections

- [var allMediaSelections: [AVMediaSelection]](/documentation/avfoundation/avmutablemovie/allmediaselections)
- [var availableMediaCharacteristicsWithMediaSelectionOptions: [AVMediaCharacteristic]](/documentation/avfoundation/avmutablemovie/availablemediacharacteristicswithmediaselectionoptions)
- [func mediaSelectionGroup(forMediaCharacteristic: AVMediaCharacteristic) -> AVMediaSelectionGroup?](/documentation/avfoundation/avmutablemovie/mediaselectiongroup(formediacharacteristic:))

#### Accessing chapter metadata

- [var availableChapterLocales: [Locale]](/documentation/avfoundation/avmutablemovie/availablechapterlocales)
- [func chapterMetadataGroups(bestMatchingPreferredLanguages: [String]) -> [AVTimedMetadataGroup]](/documentation/avfoundation/avmutablemovie/chaptermetadatagroups(bestmatchingpreferredlanguages:))
- [func chapterMetadataGroups(withTitleLocale: Locale, containingItemsWithCommonKeys: [AVMetadataKey]?) -> [AVTimedMetadataGroup]](/documentation/avfoundation/avmutablemovie/chaptermetadatagroups(withtitlelocale:containingitemswithcommonkeys:))

#### Determining content protections

- [var hasProtectedContent: Bool](/documentation/avfoundation/avmutablemovie/hasprotectedcontent)

#### Determining fragment support

- [var canContainFragments: Bool](/documentation/avfoundation/avmutablemovie/cancontainfragments)
- [var containsFragments: Bool](/documentation/avfoundation/avmutablemovie/containsfragments)
- [var overallDurationHint: CMTime](/documentation/avfoundation/avmutablemovie/overalldurationhint)
- [AVMutableMovieTrack](/documentation/avfoundation/avmutablemovietrack)

#### Managing time ranges

- [func insertTimeRange(CMTimeRange, of: AVAssetTrack, at: CMTime, copySampleData: Bool) throws](/documentation/avfoundation/avmutablemovietrack/inserttimerange(_:of:at:copysampledata:))
- [func insertEmptyTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablemovietrack/insertemptytimerange(_:))
- [func removeTimeRange(CMTimeRange)](/documentation/avfoundation/avmutablemovietrack/removetimerange(_:))
- [func scaleTimeRange(CMTimeRange, toDuration: CMTime)](/documentation/avfoundation/avmutablemovietrack/scaletimerange(_:toduration:))

#### Appending sample data

- [func append(CMReadySampleBuffer<CMSampleBuffer.DynamicContent>) throws -> (decodeTime: CMTime, presentationTime: CMTime)](/documentation/avfoundation/avmutablemovietrack/append(_:))
- [func append(CMSampleBuffer, decodeTime: UnsafeMutablePointer<CMTime>?, presentationTime: UnsafeMutablePointer<CMTime>?) throws](/documentation/avfoundation/avmutablemovietrack/append(_:decodetime:presentationtime:))
- [func insertMediaTimeRange(CMTimeRange, into: CMTimeRange) -> Bool](/documentation/avfoundation/avmutablemovietrack/insertmediatimerange(_:into:))

#### Accessing media chunks

- [var preferredMediaChunkAlignment: Int](/documentation/avfoundation/avmutablemovietrack/preferredmediachunkalignment)
- [var preferredMediaChunkDuration: CMTime](/documentation/avfoundation/avmutablemovietrack/preferredmediachunkduration)
- [var preferredMediaChunkSize: Int](/documentation/avfoundation/avmutablemovietrack/preferredmediachunksize)

#### Changing format descriptions

- [var formatDescriptions: [Any]](/documentation/avfoundation/avmutablemovietrack/formatdescriptions)
- [func replaceFormatDescription(CMFormatDescription, with: CMFormatDescription)](/documentation/avfoundation/avmutablemovietrack/replaceformatdescription(_:with:))

#### Configuring track information

- [var isModified: Bool](/documentation/avfoundation/avmutablemovietrack/ismodified)
- [var alternateGroupID: Int](/documentation/avfoundation/avmutablemovietrack/alternategroupid)
- [var mediaDataStorage: AVMediaDataStorage?](/documentation/avfoundation/avmutablemovietrack/mediadatastorage)
- [var sampleReferenceBaseURL: URL?](/documentation/avfoundation/avmutablemovietrack/samplereferencebaseurl)

#### Accessing track information

- [var isPlayable: Bool](/documentation/avfoundation/avmutablemovietrack/isplayable)
- [var isDecodable: Bool](/documentation/avfoundation/avmutablemovietrack/isdecodable)
- [var isEnabled: Bool](/documentation/avfoundation/avmutablemovietrack/isenabled)
- [var isSelfContained: Bool](/documentation/avfoundation/avmutablemovietrack/isselfcontained)
- [var hasProtectedContent: Bool](/documentation/avfoundation/avmutablemovietrack/hasprotectedcontent)
- [var totalSampleDataLength: Int64](/documentation/avfoundation/avmutablemovietrack/totalsampledatalength)
- [func hasMediaCharacteristic(AVMediaCharacteristic) -> Bool](/documentation/avfoundation/avmutablemovietrack/hasmediacharacteristic(_:))

#### Accessing temporal information

- [var timeRange: CMTimeRange](/documentation/avfoundation/avmutablemovietrack/timerange)
- [var timescale: CMTimeScale](/documentation/avfoundation/avmutablemovietrack/timescale)
- [var naturalTimeScale: CMTimeScale](/documentation/avfoundation/avmutablemovietrack/naturaltimescale)
- [var estimatedDataRate: Float](/documentation/avfoundation/avmutablemovietrack/estimateddatarate)
- [func samplePresentationTime(forTrackTime: CMTime) -> CMTime](/documentation/avfoundation/avmutablemovietrack/samplepresentationtime(fortracktime:))

#### Accessing language support

- [var languageCode: String?](/documentation/avfoundation/avmutablemovietrack/languagecode)
- [var extendedLanguageTag: String?](/documentation/avfoundation/avmutablemovietrack/extendedlanguagetag)

#### Accessing visual characteristics

- [var naturalSize: CGSize](/documentation/avfoundation/avmutablemovietrack/naturalsize)
- [var preferredTransform: CGAffineTransform](/documentation/avfoundation/avmutablemovietrack/preferredtransform)
- [var layer: Int](/documentation/avfoundation/avmutablemovietrack/layer)
- [var cleanApertureDimensions: CGSize](/documentation/avfoundation/avmutablemovietrack/cleanaperturedimensions)
- [var productionApertureDimensions: CGSize](/documentation/avfoundation/avmutablemovietrack/productionaperturedimensions)
- [var encodedPixelsDimensions: CGSize](/documentation/avfoundation/avmutablemovietrack/encodedpixelsdimensions)

#### Accessing audible characteristics

- [var preferredVolume: Float](/documentation/avfoundation/avmutablemovietrack/preferredvolume)
- [var hasAudioSampleDependencies: Bool](/documentation/avfoundation/avmutablemovietrack/hasaudiosampledependencies)

#### Accessing frame-based characteristics

- [var nominalFrameRate: Float](/documentation/avfoundation/avmutablemovietrack/nominalframerate)
- [var minFrameDuration: CMTime](/documentation/avfoundation/avmutablemovietrack/minframeduration)
- [var requiresFrameReordering: Bool](/documentation/avfoundation/avmutablemovietrack/requiresframereordering)

#### Accessing metadata

- [var metadata: [AVMetadataItem]](/documentation/avfoundation/avmutablemovietrack/metadata)
- [var commonMetadata: [AVMetadataItem]](/documentation/avfoundation/avmutablemovietrack/commonmetadata)
- [var availableMetadataFormats: [AVMetadataFormat]](/documentation/avfoundation/avmutablemovietrack/availablemetadataformats)
- [func metadata(forFormat: AVMetadataFormat) -> [AVMetadataItem]](/documentation/avfoundation/avmutablemovietrack/metadata(forformat:))

#### Accessing track segments

- [var segments: [AVAssetTrackSegment]](/documentation/avfoundation/avmutablemovietrack/segments)
- [func segment(forTrackTime: CMTime) -> AVAssetTrackSegment?](/documentation/avfoundation/avmutablemovietrack/segment(fortracktime:))

#### Managing track associations

- [var availableTrackAssociationTypes: [AVAssetTrack.AssociationType]](/documentation/avfoundation/avmutablemovietrack/availabletrackassociationtypes)
- [func associatedTracks(ofType: AVAssetTrack.AssociationType) -> [AVAssetTrack]](/documentation/avfoundation/avmutablemovietrack/associatedtracks(oftype:))
- [func addTrackAssociation(to: AVMovieTrack, type: AVAssetTrack.AssociationType)](/documentation/avfoundation/avmutablemovietrack/addtrackassociation(to:type:))
- [func removeTrackAssociation(to: AVMovieTrack, type: AVAssetTrack.AssociationType)](/documentation/avfoundation/avmutablemovietrack/removetrackassociation(to:type:))

#### Determining sample cursor support

- [var canProvideSampleCursors: Bool](/documentation/avfoundation/avmutablemovietrack/canprovidesamplecursors)

### Fragmented movies

- [AVFragmentedMovie](/documentation/avfoundation/avfragmentedmovie)

#### Loading tracks

- [static var tracks: AVAsyncProperty<Root, [AVFragmentedMovieTrack]>](/documentation/avfoundation/avpartialasyncproperty/tracks-7fr6q)
- [func loadTrack(withTrackID: CMPersistentTrackID, completionHandler: (AVFragmentedMovieTrack?, (any Error)?) -> Void)](/documentation/avfoundation/avfragmentedmovie/loadtrack(withtrackid:completionhandler:))
- [func loadTracks(withMediaType: AVMediaType, completionHandler: ([AVFragmentedMovieTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avfragmentedmovie/loadtracks(withmediatype:completionhandler:))
- [func loadTracks(withMediaCharacteristic: AVMediaCharacteristic, completionHandler: ([AVFragmentedMovieTrack]?, (any Error)?) -> Void)](/documentation/avfoundation/avfragmentedmovie/loadtracks(withmediacharacteristic:completionhandler:))

#### Accessing tracks

- [var tracks: [AVFragmentedMovieTrack]](/documentation/avfoundation/avfragmentedmovie/tracks)
- [func track(withTrackID: CMPersistentTrackID) -> AVFragmentedMovieTrack?](/documentation/avfoundation/avfragmentedmovie/track(withtrackid:))
- [func tracks(withMediaType: AVMediaType) -> [AVFragmentedMovieTrack]](/documentation/avfoundation/avfragmentedmovie/tracks(withmediatype:))
- [func tracks(withMediaCharacteristic: AVMediaCharacteristic) -> [AVFragmentedMovieTrack]](/documentation/avfoundation/avfragmentedmovie/tracks(withmediacharacteristic:))
- [AVFragmentedMovieTrack](/documentation/avfoundation/avfragmentedmovietrack)
- [AVFragmentedMovieMinder](/documentation/avfoundation/avfragmentedmovieminder)

#### Creating a movie minder

- [init(movie: AVFragmentedMovie, mindingInterval: TimeInterval)](/documentation/avfoundation/avfragmentedmovieminder/init(movie:mindinginterval:))

#### Adding and removing movies

- [var movies: [AVFragmentedMovie]](/documentation/avfoundation/avfragmentedmovieminder/movies)
- [func add(AVFragmentedMovie)](/documentation/avfoundation/avfragmentedmovieminder/add(_:))
- [func remove(AVFragmentedMovie)](/documentation/avfoundation/avfragmentedmovieminder/remove(_:))

#### Accessing minder information

- [var mindingInterval: TimeInterval](/documentation/avfoundation/avfragmentedmovieminder/mindinginterval)
- [AVFragmentMinding](/documentation/avfoundation/avfragmentminding)

#### Fragment minder association

- [var isAssociatedWithFragmentMinder: Bool](/documentation/avfoundation/avfragmentminding/isassociatedwithfragmentminder)

### Sample cursors

- [AVSampleCursor](/documentation/avfoundation/avsamplecursor)

#### Navigating samples

- [func step(byDecodeTime: CMTime, wasPinned: UnsafeMutablePointer<ObjCBool>?) -> CMTime](/documentation/avfoundation/avsamplecursor/step(bydecodetime:waspinned:))
- [func step(byPresentationTime: CMTime, wasPinned: UnsafeMutablePointer<ObjCBool>?) -> CMTime](/documentation/avfoundation/avsamplecursor/step(bypresentationtime:waspinned:))
- [func stepInDecodeOrder(byCount: Int64) -> Int64](/documentation/avfoundation/avsamplecursor/stepindecodeorder(bycount:))
- [func stepInPresentationOrder(byCount: Int64) -> Int64](/documentation/avfoundation/avsamplecursor/stepinpresentationorder(bycount:))

#### Getting timestamps

- [var decodeTimeStamp: CMTime](/documentation/avfoundation/avsamplecursor/decodetimestamp)
- [var presentationTimeStamp: CMTime](/documentation/avfoundation/avsamplecursor/presentationtimestamp)

#### Getting sample information

- [var currentChunkInfo: AVSampleCursorChunkInfo](/documentation/avfoundation/avsamplecursor/currentchunkinfo)
- [AVSampleCursorChunkInfo](/documentation/avfoundation/avsamplecursorchunkinfo)

##### Chunk information

- [var chunkSampleCount: Int64](/documentation/avfoundation/avsamplecursorchunkinfo/chunksamplecount)
- [var chunkHasUniformSampleSizes: ObjCBool](/documentation/avfoundation/avsamplecursorchunkinfo/chunkhasuniformsamplesizes)
- [var chunkHasUniformSampleDurations: ObjCBool](/documentation/avfoundation/avsamplecursorchunkinfo/chunkhasuniformsampledurations)
- [var chunkHasUniformFormatDescriptions: ObjCBool](/documentation/avfoundation/avsamplecursorchunkinfo/chunkhasuniformformatdescriptions)

##### Initializers

- [init()](/documentation/avfoundation/avsamplecursorchunkinfo/init())
- [init(chunkSampleCount: Int64, chunkHasUniformSampleSizes: ObjCBool, chunkHasUniformSampleDurations: ObjCBool, chunkHasUniformFormatDescriptions: ObjCBool)](/documentation/avfoundation/avsamplecursorchunkinfo/init(chunksamplecount:chunkhasuniformsamplesizes:chunkhasuniformsampledurations:chunkhasuniformformatdescriptions:))
- [var currentChunkStorageRange: AVSampleCursorStorageRange](/documentation/avfoundation/avsamplecursor/currentchunkstoragerange)
- [AVSampleCursorStorageRange](/documentation/avfoundation/avsamplecursorstoragerange)

##### Storage range

- [var offset: Int64](/documentation/avfoundation/avsamplecursorstoragerange/offset)
- [var length: Int64](/documentation/avfoundation/avsamplecursorstoragerange/length)

##### Initializers

- [init()](/documentation/avfoundation/avsamplecursorstoragerange/init())
- [init(offset: Int64, length: Int64)](/documentation/avfoundation/avsamplecursorstoragerange/init(offset:length:))
- [var currentChunkStorageURL: URL?](/documentation/avfoundation/avsamplecursor/currentchunkstorageurl)
- [var currentSampleDependencyInfo: AVSampleCursorDependencyInfo](/documentation/avfoundation/avsamplecursor/currentsampledependencyinfo)
- [AVSampleCursorDependencyInfo](/documentation/avfoundation/avsamplecursordependencyinfo)

##### Dependency information

- [var sampleIndicatesWhetherItHasDependentSamples: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampleindicateswhetherithasdependentsamples)
- [var sampleHasDependentSamples: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/samplehasdependentsamples)
- [var sampleIndicatesWhetherItDependsOnOthers: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampleindicateswhetheritdependsonothers)
- [var sampleDependsOnOthers: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampledependsonothers)
- [var sampleIndicatesWhetherItHasRedundantCoding: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampleindicateswhetherithasredundantcoding)
- [var sampleHasRedundantCoding: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/samplehasredundantcoding)

##### Initializers

- [init()](/documentation/avfoundation/avsamplecursordependencyinfo/init())
- [init(sampleIndicatesWhetherItHasDependentSamples: ObjCBool, sampleHasDependentSamples: ObjCBool, sampleIndicatesWhetherItDependsOnOthers: ObjCBool, sampleDependsOnOthers: ObjCBool, sampleIndicatesWhetherItHasRedundantCoding: ObjCBool, sampleHasRedundantCoding: ObjCBool)](/documentation/avfoundation/avsamplecursordependencyinfo/init(sampleindicateswhetherithasdependentsamples:samplehasdependentsamples:sampleindicateswhetheritdependsonothers:sampledependsonothers:sampleindicateswhetherithasredundantcoding:samplehasredundantcoding:))
- [var currentSampleDuration: CMTime](/documentation/avfoundation/avsamplecursor/currentsampleduration)
- [var currentSampleIndexInChunk: Int64](/documentation/avfoundation/avsamplecursor/currentsampleindexinchunk)
- [var currentSampleStorageRange: AVSampleCursorStorageRange](/documentation/avfoundation/avsamplecursor/currentsamplestoragerange)
- [var currentSampleSyncInfo: AVSampleCursorSyncInfo](/documentation/avfoundation/avsamplecursor/currentsamplesyncinfo)
- [AVSampleCursorSyncInfo](/documentation/avfoundation/avsamplecursorsyncinfo)

##### Sync information

- [var sampleIsFullSync: ObjCBool](/documentation/avfoundation/avsamplecursorsyncinfo/sampleisfullsync)
- [var sampleIsPartialSync: ObjCBool](/documentation/avfoundation/avsamplecursorsyncinfo/sampleispartialsync)
- [var sampleIsDroppable: ObjCBool](/documentation/avfoundation/avsamplecursorsyncinfo/sampleisdroppable)

##### Initializers

- [init()](/documentation/avfoundation/avsamplecursorsyncinfo/init())
- [init(sampleIsFullSync: ObjCBool, sampleIsPartialSync: ObjCBool, sampleIsDroppable: ObjCBool)](/documentation/avfoundation/avsamplecursorsyncinfo/init(sampleisfullsync:sampleispartialsync:sampleisdroppable:))
- [func copyCurrentSampleFormatDescription() -> CMFormatDescription](/documentation/avfoundation/avsamplecursor/copycurrentsampleformatdescription())
- [var currentSampleAudioDependencyInfo: AVSampleCursorAudioDependencyInfo](/documentation/avfoundation/avsamplecursor/currentsampleaudiodependencyinfo)
- [var currentSampleDependencyAttachments: [AnyHashable : Any]?](/documentation/avfoundation/avsamplecursor/currentsampledependencyattachments)

#### Accessing samples

- [func maySamplesWithEarlierDecodeTimeStampsHavePresentationTimeStamps(laterThan: AVSampleCursor) -> Bool](/documentation/avfoundation/avsamplecursor/maysampleswithearlierdecodetimestampshavepresentationtimestamps(laterthan:))
- [func maySamplesWithLaterDecodeTimeStampsHavePresentationTimeStamps(earlierThan: AVSampleCursor) -> Bool](/documentation/avfoundation/avsamplecursor/maysampleswithlaterdecodetimestampshavepresentationtimestamps(earlierthan:))
- [var samplesRequiredForDecoderRefresh: Int](/documentation/avfoundation/avsamplecursor/samplesrequiredfordecoderrefresh)

#### Comparing sample cursors

- [func comparePositionInDecodeOrder(withPositionOf: AVSampleCursor) -> ComparisonResult](/documentation/avfoundation/avsamplecursor/comparepositionindecodeorder(withpositionof:))
- [AVSampleCursorSyncInfo](/documentation/avfoundation/avsamplecursorsyncinfo)

#### Sync information

- [var sampleIsFullSync: ObjCBool](/documentation/avfoundation/avsamplecursorsyncinfo/sampleisfullsync)
- [var sampleIsPartialSync: ObjCBool](/documentation/avfoundation/avsamplecursorsyncinfo/sampleispartialsync)
- [var sampleIsDroppable: ObjCBool](/documentation/avfoundation/avsamplecursorsyncinfo/sampleisdroppable)

#### Initializers

- [init()](/documentation/avfoundation/avsamplecursorsyncinfo/init())
- [init(sampleIsFullSync: ObjCBool, sampleIsPartialSync: ObjCBool, sampleIsDroppable: ObjCBool)](/documentation/avfoundation/avsamplecursorsyncinfo/init(sampleisfullsync:sampleispartialsync:sampleisdroppable:))
- [AVSampleCursorDependencyInfo](/documentation/avfoundation/avsamplecursordependencyinfo)

#### Dependency information

- [var sampleIndicatesWhetherItHasDependentSamples: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampleindicateswhetherithasdependentsamples)
- [var sampleHasDependentSamples: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/samplehasdependentsamples)
- [var sampleIndicatesWhetherItDependsOnOthers: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampleindicateswhetheritdependsonothers)
- [var sampleDependsOnOthers: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampledependsonothers)
- [var sampleIndicatesWhetherItHasRedundantCoding: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/sampleindicateswhetherithasredundantcoding)
- [var sampleHasRedundantCoding: ObjCBool](/documentation/avfoundation/avsamplecursordependencyinfo/samplehasredundantcoding)

#### Initializers

- [init()](/documentation/avfoundation/avsamplecursordependencyinfo/init())
- [init(sampleIndicatesWhetherItHasDependentSamples: ObjCBool, sampleHasDependentSamples: ObjCBool, sampleIndicatesWhetherItDependsOnOthers: ObjCBool, sampleDependsOnOthers: ObjCBool, sampleIndicatesWhetherItHasRedundantCoding: ObjCBool, sampleHasRedundantCoding: ObjCBool)](/documentation/avfoundation/avsamplecursordependencyinfo/init(sampleindicateswhetherithasdependentsamples:samplehasdependentsamples:sampleindicateswhetheritdependsonothers:sampledependsonothers:sampleindicateswhetherithasredundantcoding:samplehasredundantcoding:))
- [AVSampleCursorAudioDependencyInfo](/documentation/avfoundation/avsamplecursoraudiodependencyinfo)

#### Querying independent decodability

- [var audioSampleIsIndependentlyDecodable: ObjCBool](/documentation/avfoundation/avsamplecursoraudiodependencyinfo/audiosampleisindependentlydecodable)
- [var audioSamplePacketRefreshCount: Int](/documentation/avfoundation/avsamplecursoraudiodependencyinfo/audiosamplepacketrefreshcount)

#### Initializers

- [init()](/documentation/avfoundation/avsamplecursoraudiodependencyinfo/init())
- [init(audioSampleIsIndependentlyDecodable: ObjCBool, audioSamplePacketRefreshCount: Int)](/documentation/avfoundation/avsamplecursoraudiodependencyinfo/init(audiosampleisindependentlydecodable:audiosamplepacketrefreshcount:))
- [AVSampleCursorStorageRange](/documentation/avfoundation/avsamplecursorstoragerange)

#### Storage range

- [var offset: Int64](/documentation/avfoundation/avsamplecursorstoragerange/offset)
- [var length: Int64](/documentation/avfoundation/avsamplecursorstoragerange/length)

#### Initializers

- [init()](/documentation/avfoundation/avsamplecursorstoragerange/init())
- [init(offset: Int64, length: Int64)](/documentation/avfoundation/avsamplecursorstoragerange/init(offset:length:))
- [AVSampleCursorChunkInfo](/documentation/avfoundation/avsamplecursorchunkinfo)

#### Chunk information

- [var chunkSampleCount: Int64](/documentation/avfoundation/avsamplecursorchunkinfo/chunksamplecount)
- [var chunkHasUniformSampleSizes: ObjCBool](/documentation/avfoundation/avsamplecursorchunkinfo/chunkhasuniformsamplesizes)
- [var chunkHasUniformSampleDurations: ObjCBool](/documentation/avfoundation/avsamplecursorchunkinfo/chunkhasuniformsampledurations)
- [var chunkHasUniformFormatDescriptions: ObjCBool](/documentation/avfoundation/avsamplecursorchunkinfo/chunkhasuniformformatdescriptions)

#### Initializers

- [init()](/documentation/avfoundation/avsamplecursorchunkinfo/init())
- [init(chunkSampleCount: Int64, chunkHasUniformSampleSizes: ObjCBool, chunkHasUniformSampleDurations: ObjCBool, chunkHasUniformFormatDescriptions: ObjCBool)](/documentation/avfoundation/avsamplecursorchunkinfo/init(chunksamplecount:chunkhasuniformsamplesizes:chunkhasuniformsampledurations:chunkhasuniformformatdescriptions:))

### Media data storage

- [AVMediaDataStorage](/documentation/avfoundation/avmediadatastorage)

#### Creating media data storage

- [init(url: URL, options: [String : Any]?)](/documentation/avfoundation/avmediadatastorage/init(url:options:))

#### Accessing the URL

- [func url() -> URL?](/documentation/avfoundation/avmediadatastorage/url())
- [Video effects](/documentation/avfoundation/video-effects)

### Core Animation integration

- [AVVideoCompositionCoreAnimationTool](/documentation/avfoundation/avvideocompositioncoreanimationtool)

#### Creating a composition tool

- [convenience init(additionalLayer: sending CALayer, asTrackID: CMPersistentTrackID)](/documentation/avfoundation/avvideocompositioncoreanimationtool/init(additionallayer:astrackid:))
- [convenience init(postProcessingAsVideoLayer: CALayer, in: CALayer)](/documentation/avfoundation/avvideocompositioncoreanimationtool/init(postprocessingasvideolayer:in:))
- [convenience init(postProcessingAsVideoLayers: [CALayer], in: CALayer)](/documentation/avfoundation/avvideocompositioncoreanimationtool/init(postprocessingasvideolayers:in:))
- [convenience init(configuration: sending AVVideoCompositionCoreAnimationTool.Configuration)](/documentation/avfoundation/avvideocompositioncoreanimationtool/init(configuration:))
- [AVVideoCompositionCoreAnimationTool.Configuration](/documentation/avfoundation/avvideocompositioncoreanimationtool/configuration)

##### Creating a configuration

- [init(postProcessingAsVideoLayer: CALayer, containingLayer: CALayer)](/documentation/avfoundation/avvideocompositioncoreanimationtool/configuration/init(postprocessingasvideolayer:containinglayer:))
- [init(postProcessingAsVideoLayers: [CALayer], containingLayer: CALayer)](/documentation/avfoundation/avvideocompositioncoreanimationtool/configuration/init(postprocessingasvideolayers:containinglayer:))

##### Inspecting the configuration

- [var containingLayer: CALayer](/documentation/avfoundation/avvideocompositioncoreanimationtool/configuration/containinglayer)
- [var layers: [CALayer]](/documentation/avfoundation/avvideocompositioncoreanimationtool/configuration/layers)

### Built-in video compositing

- [Editing and playing HDR video](/documentation/avfoundation/editing-and-playing-hdr-video)
- [Debugging AVFoundation audio mixes, compositions, and video compositions](/documentation/avfoundation/debugging-avfoundation-audio-mixes-compositions-and-video-compositions)
- [AVVideoComposition](/documentation/avfoundation/avvideocomposition)

#### Creating a video composition

- [convenience init(configuration: AVVideoComposition.Configuration)](/documentation/avfoundation/avvideocomposition/init(configuration:))
- [AVVideoComposition.Configuration](/documentation/avfoundation/avvideocomposition/configuration)

##### Creating a configuration

- [init(for: AVAsset, prototypeInstruction: AVVideoCompositionInstruction?) async throws](/documentation/avfoundation/avvideocomposition/configuration/init(for:prototypeinstruction:))
- [init(animationTool: AVVideoCompositionCoreAnimationTool?, colorPrimaries: String?, colorTransferFunction: String?, colorYCbCrMatrix: String?, customVideoCompositorClass: (any AVVideoCompositing.Type)?, frameDuration: CMTime, instructions: [any AVVideoCompositionInstructionProtocol], outputBufferDescription: [[CMTag]]?, perFrameHDRDisplayMetadataPolicy: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy, renderScale: Float, renderSize: CGSize, sourceSampleDataTrackIDs: [CMPersistentTrackID], sourceTrackIDForFrameTiming: Int32, spatialVideoConfigurations: [AVSpatialVideoConfiguration])](/documentation/avfoundation/avvideocomposition/configuration/init(animationtool:colorprimaries:colortransferfunction:colorycbcrmatrix:customvideocompositorclass:frameduration:instructions:outputbufferdescription:perframehdrdisplaymetadatapolicy:renderscale:rendersize:sourcesampledatatrackids:sourcetr-2lwnx)
- [init(animationTool: AVVideoCompositionCoreAnimationTool?, colorPrimaries: String?, colorTransferFunction: String?, colorYCbCrMatrix: String?, customVideoCompositorClass: (any AVVideoCompositing.Type)?, frameDuration: CMTime, instructions: [any AVVideoCompositionInstructionProtocol], outputBufferDescription: [[CMTag]]?, renderScale: Float, renderSize: CGSize, sourceSampleDataTrackIDs: [CMPersistentTrackID], sourceTrackIDForFrameTiming: Int32, spatialVideoConfigurations: [AVSpatialVideoConfiguration])](/documentation/avfoundation/avvideocomposition/configuration/init(animationtool:colorprimaries:colortransferfunction:colorycbcrmatrix:customvideocompositorclass:frameduration:instructions:outputbufferdescription:renderscale:rendersize:sourcesampledatatrackids:sourcetrackidforframetiming:spatialvideoc-j1vm)

##### Inspecting the configuration

- [var renderSize: CGSize](/documentation/avfoundation/avvideocomposition/configuration/rendersize)
- [var renderScale: Float](/documentation/avfoundation/avvideocomposition/configuration/renderscale)
- [var frameDuration: CMTime](/documentation/avfoundation/avvideocomposition/configuration/frameduration)
- [var animationTool: AVVideoCompositionCoreAnimationTool?](/documentation/avfoundation/avvideocomposition/configuration/animationtool)
- [var colorPrimaries: String?](/documentation/avfoundation/avvideocomposition/configuration/colorprimaries)
- [var colorTransferFunction: String?](/documentation/avfoundation/avvideocomposition/configuration/colortransferfunction)
- [var colorYCbCrMatrix: String?](/documentation/avfoundation/avvideocomposition/configuration/colorycbcrmatrix)
- [var customVideoCompositorClass: (any AVVideoCompositing.Type)?](/documentation/avfoundation/avvideocomposition/configuration/customvideocompositorclass)
- [var outputBufferDescription: [[CMTag]]?](/documentation/avfoundation/avvideocomposition/configuration/outputbufferdescription)
- [var instructions: [any AVVideoCompositionInstructionProtocol]](/documentation/avfoundation/avvideocomposition/configuration/instructions)
- [var spatialVideoConfigurations: [AVSpatialVideoConfiguration]](/documentation/avfoundation/avvideocomposition/configuration/spatialvideoconfigurations)
- [var perFrameHDRDisplayMetadataPolicy: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/configuration/perframehdrdisplaymetadatapolicy)
- [var sourceSampleDataTrackIDs: [CMPersistentTrackID]](/documentation/avfoundation/avvideocomposition/configuration/sourcesampledatatrackids)
- [var sourceTrackIDForFrameTiming: CMPersistentTrackID](/documentation/avfoundation/avvideocomposition/configuration/sourcetrackidforframetiming)
- [convenience init(applyingFiltersTo: AVAsset, applier: (AVCIImageFilteringParameters) async throws -> AVCIImageFilteringResult) async throws](/documentation/avfoundation/avvideocomposition/init(applyingfiltersto:applier:))
- [class func videoComposition(with: AVAsset, applyingCIFiltersWithHandler: (AVAsynchronousCIImageFilteringRequest) -> Void, completionHandler: (AVVideoComposition?, (any Error)?) -> Void)](/documentation/avfoundation/avvideocomposition/videocomposition(with:applyingcifilterswithhandler:completionhandler:))
- [AVAsynchronousCIImageFilteringRequest](/documentation/avfoundation/avasynchronousciimagefilteringrequest)

##### Getting the image to be filtered

- [var sourceImage: CIImage](/documentation/avfoundation/avasynchronousciimagefilteringrequest/sourceimage)

##### Getting contextual information for filtering

- [var compositionTime: CMTime](/documentation/avfoundation/avasynchronousciimagefilteringrequest/compositiontime)
- [var renderSize: CGSize](/documentation/avfoundation/avasynchronousciimagefilteringrequest/rendersize)

##### Returning the filtered image

- [func finish(with: CIImage, context: CIContext?)](/documentation/avfoundation/avasynchronousciimagefilteringrequest/finish(with:context:))
- [func finish(with: any Error)](/documentation/avfoundation/avasynchronousciimagefilteringrequest/finish(with:))
- [AVCIImageFilteringParameters](/documentation/avfoundation/avciimagefilteringparameters)

##### Inspecting the parameters

- [let compositionTime: CMTime](/documentation/avfoundation/avciimagefilteringparameters/compositiontime)
- [let renderSize: CGSize](/documentation/avfoundation/avciimagefilteringparameters/rendersize)
- [let sourceImage: CIImage](/documentation/avfoundation/avciimagefilteringparameters/sourceimage)
- [AVCIImageFilteringResult](/documentation/avfoundation/avciimagefilteringresult)

##### Creating a result

- [init(resultImage: CIImage, ciContext: CIContext?)](/documentation/avfoundation/avciimagefilteringresult/init(resultimage:cicontext:))

##### Inspecting the result

- [let ciContext: CIContext?](/documentation/avfoundation/avciimagefilteringresult/cicontext)
- [let resultImage: CIImage](/documentation/avfoundation/avciimagefilteringresult/resultimage)
- [class func videoComposition(withPropertiesOf: AVAsset, completionHandler: (AVVideoComposition?, (any Error)?) -> Void)](/documentation/avfoundation/avvideocomposition/videocomposition(withpropertiesof:completionhandler:))
- [init(propertiesOf: AVAsset)](/documentation/avfoundation/avvideocomposition/init(propertiesof:))
- [init(asset: AVAsset, applyingCIFiltersWithHandler: (AVAsynchronousCIImageFilteringRequest) -> Void)](/documentation/avfoundation/avvideocomposition/init(asset:applyingcifilterswithhandler:))

#### Inspecting the video composition

- [var renderSize: CGSize](/documentation/avfoundation/avvideocomposition/rendersize)
- [var renderScale: Float](/documentation/avfoundation/avvideocomposition/renderscale)
- [var frameDuration: CMTime](/documentation/avfoundation/avvideocomposition/frameduration)
- [var animationTool: AVVideoCompositionCoreAnimationTool?](/documentation/avfoundation/avvideocomposition/animationtool)
- [var colorPrimaries: String?](/documentation/avfoundation/avvideocomposition/colorprimaries)
- [var colorTransferFunction: String?](/documentation/avfoundation/avvideocomposition/colortransferfunction)
- [var colorYCbCrMatrix: String?](/documentation/avfoundation/avvideocomposition/colorycbcrmatrix)
- [var customVideoCompositorClass: (any AVVideoCompositing.Type)?](/documentation/avfoundation/avvideocomposition/customvideocompositorclass)
- [var outputBufferDescription: [[CMTag]]?](/documentation/avfoundation/avvideocomposition/outputbufferdescription-3ayt8)
- [var spatialVideoConfigurations: [AVSpatialVideoConfiguration]](/documentation/avfoundation/avvideocomposition/spatialvideoconfigurations-80iab)
- [AVSpatialVideoConfiguration](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct)

##### Creating a configuration

- [init()](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct/init())
- [init(formatDescription: CMFormatDescription)](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct/init(formatdescription:))
- [static var nonSpatial: AVSpatialVideoConfiguration](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct/nonspatial)

##### Modifying the configuration

- [var cameraCalibrationDataLensCollection: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection?](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct/cameracalibrationdatalenscollection)
- [var cameraSystemBaseline: UInt32?](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct/camerasystembaseline)
- [var disparityAdjustment: Int32?](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct/disparityadjustment)
- [var horizontalFieldOfView: UInt32?](/documentation/avfoundation/avspatialvideoconfiguration-swift.struct/horizontalfieldofview)

#### Validating the time range

- [func isValid(for: [AVAssetTrack], assetDuration: CMTime, timeRange: CMTimeRange, validationDelegate: (any AVVideoCompositionValidationHandling)?) -> Bool](/documentation/avfoundation/avvideocomposition/isvalid(for:assetduration:timerange:validationdelegate:))
- [AVVideoCompositionValidationHandling](/documentation/avfoundation/avvideocompositionvalidationhandling)

##### Configuring validation methods

- [func videoComposition(AVVideoComposition, shouldContinueValidatingAfterFindingInvalidValueForKey: String) -> Bool](/documentation/avfoundation/avvideocompositionvalidationhandling/videocomposition(_:shouldcontinuevalidatingafterfindinginvalidvalueforkey:))
- [func videoComposition(AVVideoComposition, shouldContinueValidatingAfterFindingEmptyTimeRange: CMTimeRange) -> Bool](/documentation/avfoundation/avvideocompositionvalidationhandling/videocomposition(_:shouldcontinuevalidatingafterfindingemptytimerange:))
- [func videoComposition(AVVideoComposition, shouldContinueValidatingAfterFindingInvalidTimeRangeIn: any AVVideoCompositionInstructionProtocol) -> Bool](/documentation/avfoundation/avvideocompositionvalidationhandling/videocomposition(_:shouldcontinuevalidatingafterfindinginvalidtimerangein:))
- [func videoComposition(AVVideoComposition, shouldContinueValidatingAfterFindingInvalidTrackIDIn: any AVVideoCompositionInstructionProtocol, layerInstruction: AVVideoCompositionLayerInstruction, asset: AVAsset) -> Bool](/documentation/avfoundation/avvideocompositionvalidationhandling/videocomposition(_:shouldcontinuevalidatingafterfindinginvalidtrackidin:layerinstruction:asset:))
- [func determineValidity(for: AVAsset?, timeRange: CMTimeRange, validationDelegate: (any AVVideoCompositionValidationHandling)?, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/avfoundation/avvideocomposition/determinevalidity(for:timerange:validationdelegate:completionhandler:))
- [func isValid(for: AVAsset?, timeRange: CMTimeRange, validationDelegate: (any AVVideoCompositionValidationHandling)?) -> Bool](/documentation/avfoundation/avvideocomposition/isvalid(for:timerange:validationdelegate:))

#### Reading instructions

- [var instructions: [any AVVideoCompositionInstructionProtocol]](/documentation/avfoundation/avvideocomposition/instructions)
- [AVVideoCompositionInstructionProtocol](/documentation/avfoundation/avvideocompositioninstructionprotocol)

##### Getting track ID settings

- [var passthroughTrackID: CMPersistentTrackID](/documentation/avfoundation/avvideocompositioninstructionprotocol/passthroughtrackid)
- [var requiredSourceTrackIDs: [NSValue]?](/documentation/avfoundation/avvideocompositioninstructionprotocol/requiredsourcetrackids)
- [var requiredSourceSampleDataTrackIDs: [NSNumber]](/documentation/avfoundation/avvideocompositioninstructionprotocol/requiredsourcesampledatatrackids)

##### Getting tweening settings

- [var containsTweening: Bool](/documentation/avfoundation/avvideocompositioninstructionprotocol/containstweening)

##### Getting post-processing status

- [var enablePostProcessing: Bool](/documentation/avfoundation/avvideocompositioninstructionprotocol/enablepostprocessing)

##### Getting timing settings

- [var timeRange: CMTimeRange](/documentation/avfoundation/avvideocompositioninstructionprotocol/timerange)

#### Identifying source tracks

- [var sourceTrackIDForFrameTiming: CMPersistentTrackID](/documentation/avfoundation/avvideocomposition/sourcetrackidforframetiming)
- [var sourceSampleDataTrackIDs: [CMPersistentTrackID]](/documentation/avfoundation/avvideocomposition/sourcesampledatatrackids-2hgue)

#### Configuring HDR metadata

- [var perFrameHDRDisplayMetadataPolicy: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.property)
- [AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct)

##### Policies

- [static let propagate: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct/propagate)
- [static let generate: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct/generate)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct/init(rawvalue:))
- [AVVideoCompositionInstruction](/documentation/avfoundation/avvideocompositioninstruction-swift.class)

#### Creating an instruction

- [convenience init(configuration: AVVideoCompositionInstruction.Configuration)](/documentation/avfoundation/avvideocompositioninstruction-swift.class/init(configuration:))
- [AVVideoCompositionInstruction.Configuration](/documentation/avfoundation/avvideocompositioninstruction-swift.class/configuration)

##### Creating a configuration

- [init(backgroundColor: CGColor?, enablePostProcessing: Bool, layerInstructions: [AVVideoCompositionLayerInstruction], requiredSourceSampleDataTrackIDs: [CMPersistentTrackID], timeRange: CMTimeRange)](/documentation/avfoundation/avvideocompositioninstruction-swift.class/configuration/init(backgroundcolor:enablepostprocessing:layerinstructions:requiredsourcesampledatatrackids:timerange:))

##### Inspecting the configuration

- [var backgroundColor: CGColor?](/documentation/avfoundation/avvideocompositioninstruction-swift.class/configuration/backgroundcolor)
- [var enablePostProcessing: Bool](/documentation/avfoundation/avvideocompositioninstruction-swift.class/configuration/enablepostprocessing)
- [var layerInstructions: [AVVideoCompositionLayerInstruction]](/documentation/avfoundation/avvideocompositioninstruction-swift.class/configuration/layerinstructions)
- [var requiredSourceSampleDataTrackIDs: [CMPersistentTrackID]](/documentation/avfoundation/avvideocompositioninstruction-swift.class/configuration/requiredsourcesampledatatrackids)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avvideocompositioninstruction-swift.class/configuration/timerange)

#### Inspecting the instruction

- [var backgroundColor: CGColor?](/documentation/avfoundation/avvideocompositioninstruction-swift.class/backgroundcolor)
- [var layerInstructions: [AVVideoCompositionLayerInstruction]](/documentation/avfoundation/avvideocompositioninstruction-swift.class/layerinstructions)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avvideocompositioninstruction-swift.class/timerange)
- [var enablePostProcessing: Bool](/documentation/avfoundation/avvideocompositioninstruction-swift.class/enablepostprocessing)

#### Identifying source tracks

- [var requiredSourceTrackIDs: [NSValue]](/documentation/avfoundation/avvideocompositioninstruction-swift.class/requiredsourcetrackids)
- [var requiredSourceSampleDataTrackIDs: [NSNumber]](/documentation/avfoundation/avvideocompositioninstruction-swift.class/requiredsourcesampledatatrackids)
- [var passthroughTrackID: CMPersistentTrackID](/documentation/avfoundation/avvideocompositioninstruction-swift.class/passthroughtrackid)
- [AVVideoCompositionLayerInstruction](/documentation/avfoundation/avvideocompositionlayerinstruction)

#### Creating a layer instruction

- [convenience init(configuration: AVVideoCompositionLayerInstruction.Configuration)](/documentation/avfoundation/avvideocompositionlayerinstruction/init(configuration:))
- [AVVideoCompositionLayerInstruction.Configuration](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration)

##### Creating a configuration

- [init(assetTrack: AVAssetTrack)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/init(assettrack:))
- [init(trackID: CMPersistentTrackID)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/init(trackid:))

##### Configuring the crop rectangle

- [func setCropRectangle(CGRect, at: CMTime)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/setcroprectangle(_:at:))
- [func addCropRectangleRamp(AVVideoCompositionLayerInstruction.CropRectangleRamp)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/addcroprectangleramp(_:))
- [func cropRectangleRamp(at: CMTime) -> AVVideoCompositionLayerInstruction.CropRectangleRamp?](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/croprectangleramp(at:))

##### Configuring the opacity

- [func setOpacity(Float, at: CMTime)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/setopacity(_:at:))
- [func addOpacityRamp(AVVideoCompositionLayerInstruction.OpacityRamp)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/addopacityramp(_:))
- [func opacityRamp(at: CMTime) -> AVVideoCompositionLayerInstruction.OpacityRamp?](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/opacityramp(at:))

##### Configuring the transform

- [func setTransform(CGAffineTransform, at: CMTime)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/settransform(_:at:))
- [func addTransformRamp(AVVideoCompositionLayerInstruction.TransformRamp)](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/addtransformramp(_:))
- [func transformRamp(at: CMTime) -> AVVideoCompositionLayerInstruction.TransformRamp?](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/transformramp(at:))

##### Inspecting the configuration

- [var trackID: CMPersistentTrackID](/documentation/avfoundation/avvideocompositionlayerinstruction/configuration/trackid)

#### Getting the track ID

- [var trackID: CMPersistentTrackID](/documentation/avfoundation/avvideocompositionlayerinstruction/trackid)

#### Getting opacity, transform, and cropping ramps

- [func cropRectangleRamp(at: CMTime) -> AVVideoCompositionLayerInstruction.CropRectangleRamp?](/documentation/avfoundation/avvideocompositionlayerinstruction/croprectangleramp(at:))
- [AVVideoCompositionLayerInstruction.CropRectangleRamp](/documentation/avfoundation/avvideocompositionlayerinstruction/croprectangleramp)

##### Creating a crop rectangle ramp

- [init(timeRange: CMTimeRange, start: CGRect, end: CGRect)](/documentation/avfoundation/avvideocompositionlayerinstruction/croprectangleramp/init(timerange:start:end:))

##### Inspecting the crop rectangle ramp

- [var end: CGRect](/documentation/avfoundation/avvideocompositionlayerinstruction/croprectangleramp/end)
- [var start: CGRect](/documentation/avfoundation/avvideocompositionlayerinstruction/croprectangleramp/start)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avvideocompositionlayerinstruction/croprectangleramp/timerange)
- [func getCropRectangleRamp(for: CMTime, startCropRectangle: UnsafeMutablePointer<CGRect>?, endCropRectangle: UnsafeMutablePointer<CGRect>?, timeRange: UnsafeMutablePointer<CMTimeRange>?) -> Bool](/documentation/avfoundation/avvideocompositionlayerinstruction/getcroprectangleramp(for:startcroprectangle:endcroprectangle:timerange:))
- [func opacityRamp(at: CMTime) -> AVVideoCompositionLayerInstruction.OpacityRamp?](/documentation/avfoundation/avvideocompositionlayerinstruction/opacityramp(at:))
- [AVVideoCompositionLayerInstruction.OpacityRamp](/documentation/avfoundation/avvideocompositionlayerinstruction/opacityramp)

##### Creating an opacity ramp

- [init(timeRange: CMTimeRange, start: Float, end: Float)](/documentation/avfoundation/avvideocompositionlayerinstruction/opacityramp/init(timerange:start:end:))

##### Inspecting the opacity ramp

- [var end: Float](/documentation/avfoundation/avvideocompositionlayerinstruction/opacityramp/end)
- [var start: Float](/documentation/avfoundation/avvideocompositionlayerinstruction/opacityramp/start)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avvideocompositionlayerinstruction/opacityramp/timerange)
- [func getOpacityRamp(for: CMTime, startOpacity: UnsafeMutablePointer<Float>?, endOpacity: UnsafeMutablePointer<Float>?, timeRange: UnsafeMutablePointer<CMTimeRange>?) -> Bool](/documentation/avfoundation/avvideocompositionlayerinstruction/getopacityramp(for:startopacity:endopacity:timerange:))
- [func transformRamp(at: CMTime) -> AVVideoCompositionLayerInstruction.TransformRamp?](/documentation/avfoundation/avvideocompositionlayerinstruction/transformramp(at:))
- [AVVideoCompositionLayerInstruction.TransformRamp](/documentation/avfoundation/avvideocompositionlayerinstruction/transformramp)

##### Creating a transform ramp

- [init(timeRange: CMTimeRange, start: CGAffineTransform, end: CGAffineTransform)](/documentation/avfoundation/avvideocompositionlayerinstruction/transformramp/init(timerange:start:end:))

##### Inspecting the transform ramp

- [var end: CGAffineTransform](/documentation/avfoundation/avvideocompositionlayerinstruction/transformramp/end)
- [var start: CGAffineTransform](/documentation/avfoundation/avvideocompositionlayerinstruction/transformramp/start)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avvideocompositionlayerinstruction/transformramp/timerange)
- [func getTransformRamp(for: CMTime, start: UnsafeMutablePointer<CGAffineTransform>?, end: UnsafeMutablePointer<CGAffineTransform>?, timeRange: UnsafeMutablePointer<CMTimeRange>?) -> Bool](/documentation/avfoundation/avvideocompositionlayerinstruction/gettransformramp(for:start:end:timerange:))
- [AVMutableVideoComposition](/documentation/avfoundation/avmutablevideocomposition)

#### Creating a video composition

- [class func videoComposition(withPropertiesOf: AVAsset, completionHandler: (AVMutableVideoComposition?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablevideocomposition/videocomposition(withpropertiesof:completionhandler:))
- [class func videoComposition(withPropertiesOf: AVAsset, prototypeInstruction: AVVideoCompositionInstruction, completionHandler: (AVMutableVideoComposition?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablevideocomposition/videocomposition(withpropertiesof:prototypeinstruction:completionhandler:))
- [class func videoComposition(with: AVAsset, applyingCIFiltersWithHandler: (AVAsynchronousCIImageFilteringRequest) -> Void, completionHandler: (AVMutableVideoComposition?, (any Error)?) -> Void)](/documentation/avfoundation/avmutablevideocomposition/videocomposition(with:applyingcifilterswithhandler:completionhandler:))
- [init(propertiesOf: AVAsset)](/documentation/avfoundation/avmutablevideocomposition/init(propertiesof:))
- [init(propertiesOf: AVAsset, prototypeInstruction: AVVideoCompositionInstruction)](/documentation/avfoundation/avmutablevideocomposition/init(propertiesof:prototypeinstruction:))
- [init(asset: AVAsset, applyingCIFiltersWithHandler: (AVAsynchronousCIImageFilteringRequest) -> Void)](/documentation/avfoundation/avmutablevideocomposition/init(asset:applyingcifilterswithhandler:))

#### Configuring video composition properties

- [var frameDuration: CMTime](/documentation/avfoundation/avmutablevideocomposition/frameduration)
- [var renderSize: CGSize](/documentation/avfoundation/avmutablevideocomposition/rendersize)
- [var renderScale: Float](/documentation/avfoundation/avmutablevideocomposition/renderscale)
- [var animationTool: AVVideoCompositionCoreAnimationTool?](/documentation/avfoundation/avmutablevideocomposition/animationtool)

#### Specifying composition instructions

- [var instructions: [any AVVideoCompositionInstructionProtocol]](/documentation/avfoundation/avmutablevideocomposition/instructions)
- [AVVideoCompositionInstructionProtocol](/documentation/avfoundation/avvideocompositioninstructionprotocol)

##### Getting track ID settings

- [var passthroughTrackID: CMPersistentTrackID](/documentation/avfoundation/avvideocompositioninstructionprotocol/passthroughtrackid)
- [var requiredSourceTrackIDs: [NSValue]?](/documentation/avfoundation/avvideocompositioninstructionprotocol/requiredsourcetrackids)
- [var requiredSourceSampleDataTrackIDs: [NSNumber]](/documentation/avfoundation/avvideocompositioninstructionprotocol/requiredsourcesampledatatrackids)

##### Getting tweening settings

- [var containsTweening: Bool](/documentation/avfoundation/avvideocompositioninstructionprotocol/containstweening)

##### Getting post-processing status

- [var enablePostProcessing: Bool](/documentation/avfoundation/avvideocompositioninstructionprotocol/enablepostprocessing)

##### Getting timing settings

- [var timeRange: CMTimeRange](/documentation/avfoundation/avvideocompositioninstructionprotocol/timerange)

#### Configuring HDR metadata

- [var perFrameHDRDisplayMetadataPolicy: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avmutablevideocomposition/perframehdrdisplaymetadatapolicy)
- [AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct)

##### Policies

- [static let propagate: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct/propagate)
- [static let generate: AVVideoComposition.PerFrameHDRDisplayMetadataPolicy](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct/generate)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avvideocomposition/perframehdrdisplaymetadatapolicy-swift.struct/init(rawvalue:))

#### Configuring color

- [var colorPrimaries: String?](/documentation/avfoundation/avmutablevideocomposition/colorprimaries)
- [var colorTransferFunction: String?](/documentation/avfoundation/avmutablevideocomposition/colortransferfunction)
- [var colorYCbCrMatrix: String?](/documentation/avfoundation/avmutablevideocomposition/colorycbcrmatrix)

#### Identifying source tracks

- [var sourceTrackIDForFrameTiming: CMPersistentTrackID](/documentation/avfoundation/avmutablevideocomposition/sourcetrackidforframetiming)
- [var sourceSampleDataTrackIDs: [CMPersistentTrackID]](/documentation/avfoundation/avmutablevideocomposition/sourcesampledatatrackids-7i02t)

#### Specifying a custom compositor

- [var customVideoCompositorClass: (any AVVideoCompositing.Type)?](/documentation/avfoundation/avmutablevideocomposition/customvideocompositorclass)
- [AVMutableVideoCompositionInstruction](/documentation/avfoundation/avmutablevideocompositioninstruction)

#### Configuring the instructions

- [var backgroundColor: CGColor?](/documentation/avfoundation/avmutablevideocompositioninstruction/backgroundcolor)
- [var layerInstructions: [AVVideoCompositionLayerInstruction]](/documentation/avfoundation/avmutablevideocompositioninstruction/layerinstructions)
- [var timeRange: CMTimeRange](/documentation/avfoundation/avmutablevideocompositioninstruction/timerange)
- [var enablePostProcessing: Bool](/documentation/avfoundation/avmutablevideocompositioninstruction/enablepostprocessing)

#### Configuring source tracks

- [var requiredSourceSampleDataTrackIDs: [NSNumber]](/documentation/avfoundation/avmutablevideocompositioninstruction/requiredsourcesampledatatrackids)
- [AVMutableVideoCompositionLayerInstruction](/documentation/avfoundation/avmutablevideocompositionlayerinstruction)

#### Creating an instruction

- [convenience init(assetTrack: AVAssetTrack)](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/init(assettrack:))

#### Configuring a track ID

- [var trackID: CMPersistentTrackID](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/trackid)

#### Managing properties

- [func setOpacity(Float, at: CMTime)](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/setopacity(_:at:))
- [func setOpacityRamp(fromStartOpacity: Float, toEndOpacity: Float, timeRange: CMTimeRange)](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/setopacityramp(fromstartopacity:toendopacity:timerange:))
- [func setTransform(CGAffineTransform, at: CMTime)](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/settransform(_:at:))
- [func setTransformRamp(fromStart: CGAffineTransform, toEnd: CGAffineTransform, timeRange: CMTimeRange)](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/settransformramp(fromstart:toend:timerange:))

#### Setting crop rectangle values

- [func setCropRectangle(CGRect, at: CMTime)](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/setcroprectangle(_:at:))
- [func setCropRectangleRamp(fromStartCropRectangle: CGRect, toEndCropRectangle: CGRect, timeRange: CMTimeRange)](/documentation/avfoundation/avmutablevideocompositionlayerinstruction/setcroprectangleramp(fromstartcroprectangle:toendcroprectangle:timerange:))

### Custom video compositing

- [Processing spatial video with a custom video compositor](/documentation/avfoundation/processing-spatial-video-with-a-custom-video-compositor)
- [AVVideoCompositing](/documentation/avfoundation/avvideocompositing)

#### Inspecting processing requirements

- [var sourcePixelBufferAttributes: [String : any Sendable]?](/documentation/avfoundation/avvideocompositing/sourcepixelbufferattributes)
- [var requiredPixelBufferAttributesForRenderContext: [String : any Sendable]](/documentation/avfoundation/avvideocompositing/requiredpixelbufferattributesforrendercontext)
- [var supportsHDRSourceFrames: Bool](/documentation/avfoundation/avvideocompositing/supportshdrsourceframes)
- [var supportsWideColorSourceFrames: Bool](/documentation/avfoundation/avvideocompositing/supportswidecolorsourceframes)
- [var canConformColorOfSourceFrames: Bool](/documentation/avfoundation/avvideocompositing/canconformcolorofsourceframes)
- [var supportsSourceTaggedBuffers: Bool](/documentation/avfoundation/avvideocompositing/supportssourcetaggedbuffers)

#### Observing render context changes

- [func renderContextChanged(AVVideoCompositionRenderContext)](/documentation/avfoundation/avvideocompositing/rendercontextchanged(_:))
- [AVVideoCompositionRenderContext](/documentation/avfoundation/avvideocompositionrendercontext)

##### Creating the pixel buffer

- [func newPixelBuffer() -> CVPixelBuffer?](/documentation/avfoundation/avvideocompositionrendercontext/newpixelbuffer())
- [func makeMutablePixelBuffer() throws -> CVMutablePixelBuffer](/documentation/avfoundation/avvideocompositionrendercontext/makemutablepixelbuffer())

##### Getting the render settings

- [var videoComposition: AVVideoComposition](/documentation/avfoundation/avvideocompositionrendercontext/videocomposition)
- [var highQualityRendering: Bool](/documentation/avfoundation/avvideocompositionrendercontext/highqualityrendering)
- [var renderScale: Float](/documentation/avfoundation/avvideocompositionrendercontext/renderscale)
- [var renderTransform: CGAffineTransform](/documentation/avfoundation/avvideocompositionrendercontext/rendertransform)
- [var size: CGSize](/documentation/avfoundation/avvideocompositionrendercontext/size)

##### Getting pixel and edge width information

- [var edgeWidths: AVEdgeWidths](/documentation/avfoundation/avvideocompositionrendercontext/edgewidths)
- [AVEdgeWidths](/documentation/avfoundation/avedgewidths)

###### Edge widths

- [var left: CGFloat](/documentation/avfoundation/avedgewidths/left)
- [var top: CGFloat](/documentation/avfoundation/avedgewidths/top)
- [var right: CGFloat](/documentation/avfoundation/avedgewidths/right)
- [var bottom: CGFloat](/documentation/avfoundation/avedgewidths/bottom)

###### Initializers

- [init()](/documentation/avfoundation/avedgewidths/init())
- [init(left: CGFloat, top: CGFloat, right: CGFloat, bottom: CGFloat)](/documentation/avfoundation/avedgewidths/init(left:top:right:bottom:))
- [var pixelAspectRatio: AVPixelAspectRatio](/documentation/avfoundation/avvideocompositionrendercontext/pixelaspectratio)
- [AVPixelAspectRatio](/documentation/avfoundation/avpixelaspectratio)

###### Spacing

- [var horizontalSpacing: Int](/documentation/avfoundation/avpixelaspectratio/horizontalspacing)
- [var verticalSpacing: Int](/documentation/avfoundation/avpixelaspectratio/verticalspacing)

###### Initializers

- [init()](/documentation/avfoundation/avpixelaspectratio/init())
- [init(horizontalSpacing: Int, verticalSpacing: Int)](/documentation/avfoundation/avpixelaspectratio/init(horizontalspacing:verticalspacing:))

#### Preparing to render frames

- [func anticipateRendering(using: AVVideoCompositionRenderHint)](/documentation/avfoundation/avvideocompositing/anticipaterendering(using:))
- [func prerollForRendering(using: AVVideoCompositionRenderHint)](/documentation/avfoundation/avvideocompositing/prerollforrendering(using:))
- [AVVideoCompositionRenderHint](/documentation/avfoundation/avvideocompositionrenderhint)

##### Managing composition timing

- [var startCompositionTime: CMTime](/documentation/avfoundation/avvideocompositionrenderhint/startcompositiontime)
- [var endCompositionTime: CMTime](/documentation/avfoundation/avvideocompositionrenderhint/endcompositiontime)

#### Rendering the composition

- [func startRequest(AVAsynchronousVideoCompositionRequest)](/documentation/avfoundation/avvideocompositing/startrequest(_:))
- [AVAsynchronousVideoCompositionRequest](/documentation/avfoundation/avasynchronousvideocompositionrequest)

##### Inspecting the request

- [var compositionTime: CMTime](/documentation/avfoundation/avasynchronousvideocompositionrequest/compositiontime)
- [var renderContext: AVVideoCompositionRenderContext](/documentation/avfoundation/avasynchronousvideocompositionrequest/rendercontext)
- [var videoCompositionInstruction: any AVVideoCompositionInstructionProtocol](/documentation/avfoundation/avasynchronousvideocompositionrequest/videocompositioninstruction)

##### Accessing source data

- [func attach(AVSpatialVideoConfiguration, to: inout CVMutablePixelBuffer) throws](/documentation/avfoundation/avasynchronousvideocompositionrequest/attach(_:to:))
- [func sourceFrame(byTrackID: CMPersistentTrackID) -> CVPixelBuffer?](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourceframe(bytrackid:))
- [func sourceReadOnlyPixelBuffer(byTrackID: CMPersistentTrackID) -> CVReadOnlyPixelBuffer?](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourcereadonlypixelbuffer(bytrackid:))
- [func sourceReadySampleBuffer(byTrackID: CMPersistentTrackID) -> CMReadySampleBuffer<CMSampleBuffer.DynamicContent>?](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourcereadysamplebuffer(bytrackid:))
- [func sourceSampleBuffer(byTrackID: CMPersistentTrackID) -> CMSampleBuffer?](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourcesamplebuffer(bytrackid:))
- [var sourceSampleDataTrackIDs: [CMPersistentTrackID]](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourcesampledatatrackids-3yiab)
- [func sourceTaggedDynamicBuffers(byTrackID: CMPersistentTrackID) -> [CMTaggedDynamicBuffer]?](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourcetaggeddynamicbuffers(bytrackid:))
- [func sourceTimedMetadata(byTrackID: CMPersistentTrackID) -> AVTimedMetadataGroup?](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourcetimedmetadata(bytrackid:))
- [var sourceTrackIDs: [NSNumber]](/documentation/avfoundation/avasynchronousvideocompositionrequest/sourcetrackids)

##### Finishing the request

- [func finish(withComposedVideoFrame: CVPixelBuffer)](/documentation/avfoundation/avasynchronousvideocompositionrequest/finish(withcomposedvideoframe:))
- [func finish(withComposedPixelBuffer: CVReadOnlyPixelBuffer)](/documentation/avfoundation/avasynchronousvideocompositionrequest/finish(withcomposedpixelbuffer:))
- [func finish(withComposedTaggedBuffers: [CMTaggedDynamicBuffer])](/documentation/avfoundation/avasynchronousvideocompositionrequest/finish(withcomposedtaggedbuffers:))
- [func finish(with: any Error)](/documentation/avfoundation/avasynchronousvideocompositionrequest/finish(with:))
- [func finishCancelledRequest()](/documentation/avfoundation/avasynchronousvideocompositionrequest/finishcancelledrequest())
- [func cancelAllPendingVideoCompositionRequests()](/documentation/avfoundation/avvideocompositing/cancelallpendingvideocompositionrequests())
- [Audio mixing](/documentation/avfoundation/audio-mixing)

### Mixing

- [AVAudioMix](/documentation/avfoundation/avaudiomix)

#### Retrieving input parameters

- [var inputParameters: [AVAudioMixInputParameters]](/documentation/avfoundation/avaudiomix/inputparameters)
- [AVMutableAudioMix](/documentation/avfoundation/avmutableaudiomix)

#### Input parameters

- [var inputParameters: [AVAudioMixInputParameters]](/documentation/avfoundation/avmutableaudiomix/inputparameters)
- [AVAudioMixInputParameters](/documentation/avfoundation/avaudiomixinputparameters)

#### Getting the track ID

- [var trackID: CMPersistentTrackID](/documentation/avfoundation/avaudiomixinputparameters/trackid)

#### Getting volume ramps

- [func getVolumeRamp(for: CMTime, startVolume: UnsafeMutablePointer<Float>?, endVolume: UnsafeMutablePointer<Float>?, timeRange: UnsafeMutablePointer<CMTimeRange>?) -> Bool](/documentation/avfoundation/avaudiomixinputparameters/getvolumeramp(for:startvolume:endvolume:timerange:))

#### Getting an audio tap

- [var audioTapProcessor: MTAudioProcessingTap?](/documentation/avfoundation/avaudiomixinputparameters/audiotapprocessor)

#### Getting the time pitch algorithm setting

- [var audioTimePitchAlgorithm: AVAudioTimePitchAlgorithm?](/documentation/avfoundation/avaudiomixinputparameters/audiotimepitchalgorithm)
- [AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm)

##### Type properties

- [static let lowQualityZeroLatency: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/lowqualityzerolatency)
- [static let spectral: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/spectral)
- [static let timeDomain: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/timedomain)
- [static let varispeed: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/varispeed)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avaudiotimepitchalgorithm/init(rawvalue:))
- [AVMutableAudioMixInputParameters](/documentation/avfoundation/avmutableaudiomixinputparameters)

#### Creating input parameters

- [convenience init(track: AVAssetTrack?)](/documentation/avfoundation/avmutableaudiomixinputparameters/init(track:))

#### Managing the track ID

- [var trackID: CMPersistentTrackID](/documentation/avfoundation/avmutableaudiomixinputparameters/trackid)

#### Setting the volume

- [func setVolume(Float, at: CMTime)](/documentation/avfoundation/avmutableaudiomixinputparameters/setvolume(_:at:))
- [func setVolumeRamp(fromStartVolume: Float, toEndVolume: Float, timeRange: CMTimeRange)](/documentation/avfoundation/avmutableaudiomixinputparameters/setvolumeramp(fromstartvolume:toendvolume:timerange:))

#### Getting an audio tap

- [var audioTapProcessor: MTAudioProcessingTap?](/documentation/avfoundation/avmutableaudiomixinputparameters/audiotapprocessor)

#### Time pitch settings

- [var audioTimePitchAlgorithm: AVAudioTimePitchAlgorithm?](/documentation/avfoundation/avmutableaudiomixinputparameters/audiotimepitchalgorithm)
- [AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm)

##### Type properties

- [static let lowQualityZeroLatency: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/lowqualityzerolatency)
- [static let spectral: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/spectral)
- [static let timeDomain: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/timedomain)
- [static let varispeed: AVAudioTimePitchAlgorithm](/documentation/avfoundation/avaudiotimepitchalgorithm/varispeed)

##### Initializers

- [init(rawValue: String)](/documentation/avfoundation/avaudiotimepitchalgorithm/init(rawvalue:))

## Audio

- [Audio playback, recording, and processing](/documentation/avfoundation/audio-playback-recording-and-processing)

### System audio

- [Handling audio interruptions](/documentation/avfaudio/handling-audio-interruptions)
- [Responding to audio route changes](/documentation/avfaudio/responding-to-audio-route-changes)
- [Capturing stereo audio from built-In microphones](/documentation/avfaudio/capturing-stereo-audio-from-built-in-microphones)
- [AVAudioSession](/documentation/avfaudio/avaudiosession)
- [AVAudioApplication](/documentation/avfaudio/avaudioapplication)
- [AVAudioRoutingArbiter](/documentation/avfaudio/avaudioroutingarbiter)

### Basic playback and recording

- [AVAudioPlayer](/documentation/avfaudio/avaudioplayer)
- [AVAudioRecorder](/documentation/avfaudio/avaudiorecorder)
- [AVMIDIPlayer](/documentation/avfaudio/avmidiplayer)

### Advanced audio processing

- [Audio Engine](/documentation/avfaudio/audio-engine)
- [Speech synthesis](/documentation/avfoundation/speech-synthesis)

### Spoken text attributes

- [AVSpeechUtterance](/documentation/avfaudio/avspeechutterance)
- [AVSpeechSynthesisVoice](/documentation/avfaudio/avspeechsynthesisvoice)

### Speech synthesis controls

- [AVSpeechSynthesizer](/documentation/avfaudio/avspeechsynthesizer)

### Speech synthesis audio unit

- [AVSpeechSynthesisProviderAudioUnit](/documentation/avfaudio/avspeechsynthesisprovideraudiounit)

## Errors

- [let AVFoundationErrorDomain: String](/documentation/avfoundation/avfoundationerrordomain)
- [AVError](/documentation/avfoundation/averror-swift.struct)

### Error domain

- [static var errorDomain: String](/documentation/avfoundation/averror-swift.struct/errordomain)

### Error codes

- [AVError.Code](/documentation/avfoundation/averror-swift.struct/code)

#### Error codes

- [case airPlayControllerRequiresInternet](/documentation/avfoundation/averror-swift.struct/code/airplaycontrollerrequiresinternet)
- [case airPlayReceiverRequiresInternet](/documentation/avfoundation/averror-swift.struct/code/airplayreceiverrequiresinternet)
- [case airPlayReceiverTemporarilyUnavailable](/documentation/avfoundation/averror-swift.struct/code/airplayreceivertemporarilyunavailable)
- [case applicationIsNotAuthorized](/documentation/avfoundation/averror-swift.struct/code/applicationisnotauthorized)
- [case applicationIsNotAuthorizedToUseDevice](/documentation/avfoundation/averror-swift.struct/code/applicationisnotauthorizedtousedevice)
- [case autoWhiteBalanceNotLocked](/documentation/avfoundation/averror-swift.struct/code/autowhitebalancenotlocked)
- [case compositionTrackSegmentsNotContiguous](/documentation/avfoundation/averror-swift.struct/code/compositiontracksegmentsnotcontiguous)
- [case contentIsNotAuthorized](/documentation/avfoundation/averror-swift.struct/code/contentisnotauthorized)
- [case contentIsProtected](/documentation/avfoundation/averror-swift.struct/code/contentisprotected)
- [case contentIsUnavailable](/documentation/avfoundation/averror-swift.struct/code/contentisunavailable)
- [case contentKeyRequestCancelled](/documentation/avfoundation/averror-swift.struct/code/contentkeyrequestcancelled)
- [case contentNotUpdated](/documentation/avfoundation/averror-swift.struct/code/contentnotupdated)
- [case createContentKeyRequestFailed](/documentation/avfoundation/averror-swift.struct/code/createcontentkeyrequestfailed)
- [case decodeFailed](/documentation/avfoundation/averror-swift.struct/code/decodefailed)
- [case decoderNotFound](/documentation/avfoundation/averror-swift.struct/code/decodernotfound)
- [case decoderTemporarilyUnavailable](/documentation/avfoundation/averror-swift.struct/code/decodertemporarilyunavailable)
- [case deviceAlreadyUsedByAnotherSession](/documentation/avfoundation/averror-swift.struct/code/devicealreadyusedbyanothersession)
- [case deviceInUseByAnotherApplication](/documentation/avfoundation/averror-swift.struct/code/deviceinusebyanotherapplication)
- [case deviceIsNotAvailableInBackground](/documentation/avfoundation/averror-swift.struct/code/deviceisnotavailableinbackground)
- [case deviceLockedForConfigurationByAnotherProcess](/documentation/avfoundation/averror-swift.struct/code/devicelockedforconfigurationbyanotherprocess)
- [case deviceNotConnected](/documentation/avfoundation/averror-swift.struct/code/devicenotconnected)
- [case deviceWasDisconnected](/documentation/avfoundation/averror-swift.struct/code/devicewasdisconnected)
- [case diskFull](/documentation/avfoundation/averror-swift.struct/code/diskfull)
- [case displayWasDisabled](/documentation/avfoundation/averror-swift.struct/code/displaywasdisabled)
- [case encodeFailed](/documentation/avfoundation/averror-swift.struct/code/encodefailed)
- [case encoderNotFound](/documentation/avfoundation/averror-swift.struct/code/encodernotfound)
- [case encoderTemporarilyUnavailable](/documentation/avfoundation/averror-swift.struct/code/encodertemporarilyunavailable)
- [case exportFailed](/documentation/avfoundation/averror-swift.struct/code/exportfailed)
- [case externalPlaybackNotSupportedForAsset](/documentation/avfoundation/averror-swift.struct/code/externalplaybacknotsupportedforasset)
- [case failedToLoadMediaData](/documentation/avfoundation/averror-swift.struct/code/failedtoloadmediadata)
- [case failedToLoadSampleData](/documentation/avfoundation/averror-swift.struct/code/failedtoloadsampledata)
- [case failedToParse](/documentation/avfoundation/averror-swift.struct/code/failedtoparse)
- [case fileAlreadyExists](/documentation/avfoundation/averror-swift.struct/code/filealreadyexists)
- [case fileFailedToParse](/documentation/avfoundation/averror-swift.struct/code/filefailedtoparse)
- [case fileFormatNotRecognized](/documentation/avfoundation/averror-swift.struct/code/fileformatnotrecognized)
- [case fileTypeDoesNotSupportSampleReferences](/documentation/avfoundation/averror-swift.struct/code/filetypedoesnotsupportsamplereferences)
- [case followExternalSyncDeviceTimedOut](/documentation/avfoundation/averror-swift.struct/code/followexternalsyncdevicetimedout)
- [case formatUnsupported](/documentation/avfoundation/averror-swift.struct/code/formatunsupported)
- [case incompatibleAsset](/documentation/avfoundation/averror-swift.struct/code/incompatibleasset)
- [case incorrectlyConfigured](/documentation/avfoundation/averror-swift.struct/code/incorrectlyconfigured)
- [case invalidCompositionTrackSegmentDuration](/documentation/avfoundation/averror-swift.struct/code/invalidcompositiontracksegmentduration)
- [case invalidCompositionTrackSegmentSourceDuration](/documentation/avfoundation/averror-swift.struct/code/invalidcompositiontracksegmentsourceduration)
- [case invalidCompositionTrackSegmentSourceStartTime](/documentation/avfoundation/averror-swift.struct/code/invalidcompositiontracksegmentsourcestarttime)
- [case invalidOutputURLPathExtension](/documentation/avfoundation/averror-swift.struct/code/invalidoutputurlpathextension)
- [case invalidSampleCursor](/documentation/avfoundation/averror-swift.struct/code/invalidsamplecursor)
- [case invalidSourceMedia](/documentation/avfoundation/averror-swift.struct/code/invalidsourcemedia)
- [case invalidVideoComposition](/documentation/avfoundation/averror-swift.struct/code/invalidvideocomposition)
- [case malformedDepth](/documentation/avfoundation/averror-swift.struct/code/malformeddepth)
- [case maximumDurationReached](/documentation/avfoundation/averror-swift.struct/code/maximumdurationreached)
- [case maximumFileSizeReached](/documentation/avfoundation/averror-swift.struct/code/maximumfilesizereached)
- [case maximumNumberOfSamplesForFileFormatReached](/documentation/avfoundation/averror-swift.struct/code/maximumnumberofsamplesforfileformatreached)
- [case maximumStillImageCaptureRequestsExceeded](/documentation/avfoundation/averror-swift.struct/code/maximumstillimagecapturerequestsexceeded)
- [case mediaChanged](/documentation/avfoundation/averror-swift.struct/code/mediachanged)
- [case mediaDiscontinuity](/documentation/avfoundation/averror-swift.struct/code/mediadiscontinuity)
- [case mediaExtensionConflict](/documentation/avfoundation/averror-swift.struct/code/mediaextensionconflict)
- [case mediaExtensionDisabled](/documentation/avfoundation/averror-swift.struct/code/mediaextensiondisabled)
- [case mediaServicesWereReset](/documentation/avfoundation/averror-swift.struct/code/mediaserviceswerereset)
- [case noCompatibleAlternatesForExternalDisplay](/documentation/avfoundation/averror-swift.struct/code/nocompatiblealternatesforexternaldisplay)
- [case noDataCaptured](/documentation/avfoundation/averror-swift.struct/code/nodatacaptured)
- [case noImageAtTime](/documentation/avfoundation/averror-swift.struct/code/noimageattime)
- [case noLongerPlayable](/documentation/avfoundation/averror-swift.struct/code/nolongerplayable)
- [case noSmartFramingsEnabled](/documentation/avfoundation/averror-swift.struct/code/nosmartframingsenabled)
- [case noSourceTrack](/documentation/avfoundation/averror-swift.struct/code/nosourcetrack)
- [case operationCancelled](/documentation/avfoundation/averror-swift.struct/code/operationcancelled)
- [case operationInterrupted](/documentation/avfoundation/averror-swift.struct/code/operationinterrupted)
- [case operationNotAllowed](/documentation/avfoundation/averror-swift.struct/code/operationnotallowed)
- [case operationNotSupportedForAsset](/documentation/avfoundation/averror-swift.struct/code/operationnotsupportedforasset)
- [case operationNotSupportedForPreset](/documentation/avfoundation/averror-swift.struct/code/operationnotsupportedforpreset)
- [case outOfMemory](/documentation/avfoundation/averror-swift.struct/code/outofmemory)
- [case recordingAlreadyInProgress](/documentation/avfoundation/averror-swift.struct/code/recordingalreadyinprogress)
- [case referenceForbiddenByReferencePolicy](/documentation/avfoundation/averror-swift.struct/code/referenceforbiddenbyreferencepolicy)
- [case rosettaNotInstalled](/documentation/avfoundation/averror-swift.struct/code/rosettanotinstalled)
- [case sandboxExtensionDenied](/documentation/avfoundation/averror-swift.struct/code/sandboxextensiondenied)
- [case screenCaptureFailed](/documentation/avfoundation/averror-swift.struct/code/screencapturefailed)
- [case segmentStartedWithNonSyncSample](/documentation/avfoundation/averror-swift.struct/code/segmentstartedwithnonsyncsample)
- [case serverIncorrectlyConfigured](/documentation/avfoundation/averror-swift.struct/code/serverincorrectlyconfigured)
- [case sessionConfigurationChanged](/documentation/avfoundation/averror-swift.struct/code/sessionconfigurationchanged)
- [case sessionHardwareCostOverage](/documentation/avfoundation/averror-swift.struct/code/sessionhardwarecostoverage)
- [case sessionNotRunning](/documentation/avfoundation/averror-swift.struct/code/sessionnotrunning)
- [case sessionWasInterrupted](/documentation/avfoundation/averror-swift.struct/code/sessionwasinterrupted)
- [case toneMappingFailed](/documentation/avfoundation/averror-swift.struct/code/tonemappingfailed)
- [case torchLevelUnavailable](/documentation/avfoundation/averror-swift.struct/code/torchlevelunavailable)
- [case undecodableMediaData](/documentation/avfoundation/averror-swift.struct/code/undecodablemediadata)
- [case unknown](/documentation/avfoundation/averror-swift.struct/code/unknown)
- [case unsupportedDeviceActiveFormat](/documentation/avfoundation/averror-swift.struct/code/unsupporteddeviceactiveformat)
- [case unsupportedOutputSettings](/documentation/avfoundation/averror-swift.struct/code/unsupportedoutputsettings)
- [case videoCompositorFailed](/documentation/avfoundation/averror-swift.struct/code/videocompositorfailed)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfoundation/averror-swift.struct/code/init(rawvalue:))
- [static var airPlayControllerRequiresInternet: AVError.Code](/documentation/avfoundation/averror-swift.struct/airplaycontrollerrequiresinternet)
- [static var airPlayReceiverRequiresInternet: AVError.Code](/documentation/avfoundation/averror-swift.struct/airplayreceiverrequiresinternet)
- [static var airPlayReceiverTemporarilyUnavailable: AVError.Code](/documentation/avfoundation/averror-swift.struct/airplayreceivertemporarilyunavailable)
- [static var applicationIsNotAuthorizedToUseDevice: AVError.Code](/documentation/avfoundation/averror-swift.struct/applicationisnotauthorizedtousedevice)
- [static var applicationIsNotAuthorized: AVError.Code](/documentation/avfoundation/averror-swift.struct/applicationisnotauthorized)
- [static var autoWhiteBalanceNotLocked: AVError.Code](/documentation/avfoundation/averror-swift.struct/autowhitebalancenotlocked)
- [static var compositionTrackSegmentsNotContiguous: AVError.Code](/documentation/avfoundation/averror-swift.struct/compositiontracksegmentsnotcontiguous)
- [static var contentIsNotAuthorized: AVError.Code](/documentation/avfoundation/averror-swift.struct/contentisnotauthorized)
- [static var contentIsProtected: AVError.Code](/documentation/avfoundation/averror-swift.struct/contentisprotected)
- [static var contentIsUnavailable: AVError.Code](/documentation/avfoundation/averror-swift.struct/contentisunavailable)
- [static var contentKeyRequestCancelled: AVError.Code](/documentation/avfoundation/averror-swift.struct/contentkeyrequestcancelled)
- [static var contentNotUpdated: AVError.Code](/documentation/avfoundation/averror-swift.struct/contentnotupdated)
- [static var createContentKeyRequestFailed: AVError.Code](/documentation/avfoundation/averror-swift.struct/createcontentkeyrequestfailed)
- [static var decodeFailed: AVError.Code](/documentation/avfoundation/averror-swift.struct/decodefailed)
- [static var decoderNotFound: AVError.Code](/documentation/avfoundation/averror-swift.struct/decodernotfound)
- [static var decoderTemporarilyUnavailable: AVError.Code](/documentation/avfoundation/averror-swift.struct/decodertemporarilyunavailable)
- [static var deviceAlreadyUsedByAnotherSession: AVError.Code](/documentation/avfoundation/averror-swift.struct/devicealreadyusedbyanothersession)
- [static var deviceInUseByAnotherApplication: AVError.Code](/documentation/avfoundation/averror-swift.struct/deviceinusebyanotherapplication)
- [static var deviceLockedForConfigurationByAnotherProcess: AVError.Code](/documentation/avfoundation/averror-swift.struct/devicelockedforconfigurationbyanotherprocess)
- [static var deviceNotConnected: AVError.Code](/documentation/avfoundation/averror-swift.struct/devicenotconnected)
- [static var deviceWasDisconnected: AVError.Code](/documentation/avfoundation/averror-swift.struct/devicewasdisconnected)
- [static var diskFull: AVError.Code](/documentation/avfoundation/averror-swift.struct/diskfull)
- [static var displayWasDisabled: AVError.Code](/documentation/avfoundation/averror-swift.struct/displaywasdisabled)
- [static var encodeFailed: AVError.Code](/documentation/avfoundation/averror-swift.struct/encodefailed)
- [static var encoderNotFound: AVError.Code](/documentation/avfoundation/averror-swift.struct/encodernotfound)
- [static var encoderTemporarilyUnavailable: AVError.Code](/documentation/avfoundation/averror-swift.struct/encodertemporarilyunavailable)
- [static var exportFailed: AVError.Code](/documentation/avfoundation/averror-swift.struct/exportfailed)
- [static var externalPlaybackNotSupportedForAsset: AVError.Code](/documentation/avfoundation/averror-swift.struct/externalplaybacknotsupportedforasset)
- [static var failedToLoadMediaData: AVError.Code](/documentation/avfoundation/averror-swift.struct/failedtoloadmediadata)
- [static var failedToLoadSampleData: AVError.Code](/documentation/avfoundation/averror-swift.struct/failedtoloadsampledata)
- [static var failedToParse: AVError.Code](/documentation/avfoundation/averror-swift.struct/failedtoparse)
- [static var fileAlreadyExists: AVError.Code](/documentation/avfoundation/averror-swift.struct/filealreadyexists)
- [static var fileFailedToParse: AVError.Code](/documentation/avfoundation/averror-swift.struct/filefailedtoparse)
- [static var fileFormatNotRecognized: AVError.Code](/documentation/avfoundation/averror-swift.struct/fileformatnotrecognized)
- [static var fileTypeDoesNotSupportSampleReferences: AVError.Code](/documentation/avfoundation/averror-swift.struct/filetypedoesnotsupportsamplereferences)
- [static var followExternalSyncDeviceTimedOut: AVError.Code](/documentation/avfoundation/averror-swift.struct/followexternalsyncdevicetimedout)
- [static var formatUnsupported: AVError.Code](/documentation/avfoundation/averror-swift.struct/formatunsupported)
- [static var incompatibleAsset: AVError.Code](/documentation/avfoundation/averror-swift.struct/incompatibleasset)
- [static var incorrectlyConfigured: AVError.Code](/documentation/avfoundation/averror-swift.struct/incorrectlyconfigured)
- [static var invalidCompositionTrackSegmentDuration: AVError.Code](/documentation/avfoundation/averror-swift.struct/invalidcompositiontracksegmentduration)
- [static var invalidCompositionTrackSegmentSourceDuration: AVError.Code](/documentation/avfoundation/averror-swift.struct/invalidcompositiontracksegmentsourceduration)
- [static var invalidCompositionTrackSegmentSourceStartTime: AVError.Code](/documentation/avfoundation/averror-swift.struct/invalidcompositiontracksegmentsourcestarttime)
- [static var invalidOutputURLPathExtension: AVError.Code](/documentation/avfoundation/averror-swift.struct/invalidoutputurlpathextension)
- [static var invalidSampleCursor: AVError.Code](/documentation/avfoundation/averror-swift.struct/invalidsamplecursor)
- [static var invalidSourceMedia: AVError.Code](/documentation/avfoundation/averror-swift.struct/invalidsourcemedia)
- [static var invalidVideoComposition: AVError.Code](/documentation/avfoundation/averror-swift.struct/invalidvideocomposition)
- [static var malformedDepth: AVError.Code](/documentation/avfoundation/averror-swift.struct/malformeddepth)
- [static var maximumDurationReached: AVError.Code](/documentation/avfoundation/averror-swift.struct/maximumdurationreached)
- [static var maximumFileSizeReached: AVError.Code](/documentation/avfoundation/averror-swift.struct/maximumfilesizereached)
- [static var maximumNumberOfSamplesForFileFormatReached: AVError.Code](/documentation/avfoundation/averror-swift.struct/maximumnumberofsamplesforfileformatreached)
- [static var maximumStillImageCaptureRequestsExceeded: AVError.Code](/documentation/avfoundation/averror-swift.struct/maximumstillimagecapturerequestsexceeded)
- [static var mediaChanged: AVError.Code](/documentation/avfoundation/averror-swift.struct/mediachanged)
- [static var mediaDiscontinuity: AVError.Code](/documentation/avfoundation/averror-swift.struct/mediadiscontinuity)
- [static var mediaExtensionConflict: AVError.Code](/documentation/avfoundation/averror-swift.struct/mediaextensionconflict)
- [static var mediaExtensionDisabled: AVError.Code](/documentation/avfoundation/averror-swift.struct/mediaextensiondisabled)
- [static var mediaServicesWereReset: AVError.Code](/documentation/avfoundation/averror-swift.struct/mediaserviceswerereset)
- [static var noCompatibleAlternatesForExternalDisplay: AVError.Code](/documentation/avfoundation/averror-swift.struct/nocompatiblealternatesforexternaldisplay)
- [static var noDataCaptured: AVError.Code](/documentation/avfoundation/averror-swift.struct/nodatacaptured)
- [static var noImageAtTime: AVError.Code](/documentation/avfoundation/averror-swift.struct/noimageattime)
- [static var noLongerPlayable: AVError.Code](/documentation/avfoundation/averror-swift.struct/nolongerplayable)
- [static var noSmartFramingsEnabled: AVError.Code](/documentation/avfoundation/averror-swift.struct/nosmartframingsenabled)
- [static var noSourceTrack: AVError.Code](/documentation/avfoundation/averror-swift.struct/nosourcetrack)
- [static var operationCancelled: AVError.Code](/documentation/avfoundation/averror-swift.struct/operationcancelled)
- [static var operationInterrupted: AVError.Code](/documentation/avfoundation/averror-swift.struct/operationinterrupted)
- [static var operationNotAllowed: AVError.Code](/documentation/avfoundation/averror-swift.struct/operationnotallowed)
- [static var operationNotSupportedForAsset: AVError.Code](/documentation/avfoundation/averror-swift.struct/operationnotsupportedforasset)
- [static var operationNotSupportedForPreset: AVError.Code](/documentation/avfoundation/averror-swift.struct/operationnotsupportedforpreset)
- [static var outOfMemory: AVError.Code](/documentation/avfoundation/averror-swift.struct/outofmemory)
- [static var recordingAlreadyInProgress: AVError.Code](/documentation/avfoundation/averror-swift.struct/recordingalreadyinprogress)
- [static var referenceForbiddenByReferencePolicy: AVError.Code](/documentation/avfoundation/averror-swift.struct/referenceforbiddenbyreferencepolicy)
- [static var rosettaNotInstalled: AVError.Code](/documentation/avfoundation/averror-swift.struct/rosettanotinstalled)
- [static var sandboxExtensionDenied: AVError.Code](/documentation/avfoundation/averror-swift.struct/sandboxextensiondenied)
- [static var screenCaptureFailed: AVError.Code](/documentation/avfoundation/averror-swift.struct/screencapturefailed)
- [static var segmentStartedWithNonSyncSample: AVError.Code](/documentation/avfoundation/averror-swift.struct/segmentstartedwithnonsyncsample)
- [static var serverIncorrectlyConfigured: AVError.Code](/documentation/avfoundation/averror-swift.struct/serverincorrectlyconfigured)
- [static var sessionConfigurationChanged: AVError.Code](/documentation/avfoundation/averror-swift.struct/sessionconfigurationchanged)
- [static var sessionHardwareCostOverage: AVError.Code](/documentation/avfoundation/averror-swift.struct/sessionhardwarecostoverage)
- [static var sessionNotRunning: AVError.Code](/documentation/avfoundation/averror-swift.struct/sessionnotrunning)
- [static var sessionWasInterrupted: AVError.Code](/documentation/avfoundation/averror-swift.struct/sessionwasinterrupted)
- [static var toneMappingFailed: AVError.Code](/documentation/avfoundation/averror-swift.struct/tonemappingfailed)
- [static var torchLevelUnavailable: AVError.Code](/documentation/avfoundation/averror-swift.struct/torchlevelunavailable)
- [static var undecodableMediaData: AVError.Code](/documentation/avfoundation/averror-swift.struct/undecodablemediadata)
- [static var unknown: AVError.Code](/documentation/avfoundation/averror-swift.struct/unknown)
- [static var unsupportedDeviceActiveFormat: AVError.Code](/documentation/avfoundation/averror-swift.struct/unsupporteddeviceactiveformat)
- [static var unsupportedOutputSettings: AVError.Code](/documentation/avfoundation/averror-swift.struct/unsupportedoutputsettings)
- [static var videoCompositorFailed: AVError.Code](/documentation/avfoundation/averror-swift.struct/videocompositorfailed)
- [static var deviceIsNotAvailableInBackground: AVError.Code](/documentation/avfoundation/averror-swift.struct/deviceisnotavailableinbackground)

### Error properties

- [var device: AVCaptureDevice?](/documentation/avfoundation/averror-swift.struct/device-5iio4)
- [var device: String?](/documentation/avfoundation/averror-swift.struct/device-1qfzr)
- [var fileSize: Int64?](/documentation/avfoundation/averror-swift.struct/filesize)
- [var fileType: AVFileType?](/documentation/avfoundation/averror-swift.struct/filetype)
- [var mediaSubtypes: [Int]?](/documentation/avfoundation/averror-swift.struct/mediasubtypes)
- [var mediaType: AVMediaType?](/documentation/avfoundation/averror-swift.struct/mediatype-7ksjb)
- [var mediaType: String?](/documentation/avfoundation/averror-swift.struct/mediatype-5d8ie)
- [var persistentTrackID: CMPersistentTrackID?](/documentation/avfoundation/averror-swift.struct/persistenttrackid)
- [var presentationTimeStamp: CMTime?](/documentation/avfoundation/averror-swift.struct/presentationtimestamp)
- [var processID: Int?](/documentation/avfoundation/averror-swift.struct/processid)
- [var recordingSuccessfullyFinished: Bool?](/documentation/avfoundation/averror-swift.struct/recordingsuccessfullyfinished)
- [var time: CMTime?](/documentation/avfoundation/averror-swift.struct/time)

### User info keys

- [let AVErrorDeviceKey: String](/documentation/avfoundation/averrordevicekey)
- [let AVErrorDiscontinuityFlagsKey: String](/documentation/avfoundation/averrordiscontinuityflagskey)
- [let AVErrorFileSizeKey: String](/documentation/avfoundation/averrorfilesizekey)
- [let AVErrorFileTypeKey: String](/documentation/avfoundation/averrorfiletypekey)
- [let AVErrorMediaTypeKey: String](/documentation/avfoundation/averrormediatypekey)
- [let AVErrorMediaSubTypeKey: String](/documentation/avfoundation/averrormediasubtypekey)
- [let AVErrorPersistentTrackIDKey: String](/documentation/avfoundation/averrorpersistenttrackidkey)
- [let AVErrorPIDKey: String](/documentation/avfoundation/averrorpidkey)
- [let AVErrorPresentationTimeStampKey: String](/documentation/avfoundation/averrorpresentationtimestampkey)
- [let AVErrorRecordingSuccessfullyFinishedKey: String](/documentation/avfoundation/averrorrecordingsuccessfullyfinishedkey)
- [let AVErrorTimeKey: String](/documentation/avfoundation/averrortimekey)

## Macros

- [Macros](/documentation/avfoundation/avfoundation-macros)

### Macros

- [var AVF_DEPLOYING_TO_2022_RELEASES_AND_LATER: Int32](/documentation/avfoundation/avf_deploying_to_2022_releases_and_later)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
