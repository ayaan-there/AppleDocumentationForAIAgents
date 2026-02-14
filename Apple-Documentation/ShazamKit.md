# ShazamKit Documentation

Source: https://sosumi.ai/documentation/shazamkit

---
title: ShazamKit
source: https://developer.apple.com/documentation/shazamkit
timestamp: 2026-02-13T19:02:11.808Z
---

## Match audio

- [SHSession](/documentation/shazamkit/shsession)

### Creating a session object

- [init()](/documentation/shazamkit/shsession/init())
- [init(catalog: SHCatalog)](/documentation/shazamkit/shsession/init(catalog:))

### Making a match

- [func match(SHSignature)](/documentation/shazamkit/shsession/match(_:))
- [func matchStreamingBuffer(AVAudioPCMBuffer, at: AVAudioTime?)](/documentation/shazamkit/shsession/matchstreamingbuffer(_:at:))
- [Matching audio using the built-in microphone](/documentation/shazamkit/matching-audio-using-the-built-in-microphone)

### Reading the session properties

- [var delegate: (any SHSessionDelegate)?](/documentation/shazamkit/shsession/delegate)
- [var catalog: SHCatalog](/documentation/shazamkit/shsession/catalog)
- [var results: SHSession.Results](/documentation/shazamkit/shsession/results-swift.property)
- [SHSession.Results](/documentation/shazamkit/shsession/results-swift.struct)

#### Creating an iterator

- [func makeAsyncIterator() -> SHSession.Results.Iterator](/documentation/shazamkit/shsession/results-swift.struct/makeasynciterator())
- [SHSession.Results.Iterator](/documentation/shazamkit/shsession/results-swift.struct/iterator)

##### Iterating over results

- [func next() async -> SHSession.Results.Element?](/documentation/shazamkit/shsession/results-swift.struct/iterator/next())
- [SHSession.Results.Element](/documentation/shazamkit/shsession/results-swift.struct/element)

### Returning queries

- [func result(from: SHSignature) async -> SHSession.Result](/documentation/shazamkit/shsession/result(from:))
- [SHSession.Result](/documentation/shazamkit/shsession/result)

#### Constants

- [case match(SHMatch)](/documentation/shazamkit/shsession/result/match(_:))
- [case noMatch(SHSignature)](/documentation/shazamkit/shsession/result/nomatch(_:))
- [case error(any Error, SHSignature)](/documentation/shazamkit/shsession/result/error(_:_:))
- [SHManagedSession](/documentation/shazamkit/shmanagedsession)

### Creating a managed session object

- [init()](/documentation/shazamkit/shmanagedsession/init())
- [init(catalog: SHCatalog)](/documentation/shazamkit/shmanagedsession/init(catalog:))

### Getting the session state

- [var state: SHManagedSession.State](/documentation/shazamkit/shmanagedsession/state-swift.property)
- [SHManagedSession.State](/documentation/shazamkit/shmanagedsession/state-swift.enum)

#### Getting session states

- [case idle](/documentation/shazamkit/shmanagedsession/state-swift.enum/idle)
- [case matching](/documentation/shazamkit/shmanagedsession/state-swift.enum/matching)
- [case prerecording](/documentation/shazamkit/shmanagedsession/state-swift.enum/prerecording)

### Returning queries

- [func result() async -> SHSession.Result](/documentation/shazamkit/shmanagedsession/result())
- [var results: SHSession.Results](/documentation/shazamkit/shmanagedsession/results)
- [func cancel()](/documentation/shazamkit/shmanagedsession/cancel())
- [func prepare() async](/documentation/shazamkit/shmanagedsession/prepare())
- [SHSessionDelegate](/documentation/shazamkit/shsessiondelegate)

### Handling matches

- [func session(SHSession, didFind: SHMatch)](/documentation/shazamkit/shsessiondelegate/session(_:didfind:))
- [func session(SHSession, didNotFindMatchFor: SHSignature, error: (any Error)?)](/documentation/shazamkit/shsessiondelegate/session(_:didnotfindmatchfor:error:))
- [SHMatch](/documentation/shazamkit/shmatch)

### Reading match information

- [var mediaItems: [SHMatchedMediaItem]](/documentation/shazamkit/shmatch/mediaitems)
- [var querySignature: SHSignature](/documentation/shazamkit/shmatch/querysignature)
- [SHMatchedMediaItem](/documentation/shazamkit/shmatchedmediaitem)

### Reading information about the match

- [var matchOffset: TimeInterval](/documentation/shazamkit/shmatchedmediaitem/matchoffset)
- [var predictedCurrentMatchOffset: TimeInterval](/documentation/shazamkit/shmatchedmediaitem/predictedcurrentmatchoffset)
- [var frequencySkew: Float](/documentation/shazamkit/shmatchedmediaitem/frequencyskew)

### Instance Properties

- [var confidence: Float](/documentation/shazamkit/shmatchedmediaitem/confidence)
- [SHMediaItem](/documentation/shazamkit/shmediaitem)

### Creating a new media item object

- [convenience init(properties: [SHMediaItemProperty : Any])](/documentation/shazamkit/shmediaitem/init(properties:))

### Working with media item properties

- [subscript(SHMediaItemProperty) -> Any](/documentation/shazamkit/shmediaitem/subscript(_:))
- [SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty)

#### Creating a property key

- [init(String)](/documentation/shazamkit/shmediaitemproperty/init(_:))
- [init(rawValue: String)](/documentation/shazamkit/shmediaitemproperty/init(rawvalue:))

#### General media item property keys

- [static let title: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/title)
- [static let subtitle: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/subtitle)
- [static let artist: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/artist)
- [static let artworkURL: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/artworkurl)
- [static let videoURL: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/videourl)
- [static let genres: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/genres)
- [static let explicitContent: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/explicitcontent)
- [static let ISRC: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/isrc)
- [static let frequencySkewRanges: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/frequencyskewranges)
- [static let creationDate: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/creationdate)
- [static let timeRanges: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/timeranges)

#### Apple Music property keys

- [static let appleMusicURL: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/applemusicurl)
- [static let appleMusicID: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/applemusicid)

#### Shazam music catalog property keys

- [static let webURL: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/weburl)
- [static let shazamID: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/shazamid)

#### Matched media item property keys

- [static let matchOffset: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/matchoffset)
- [static let frequencySkew: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/frequencyskew)

#### Type Properties

- [static let confidence: SHMediaItemProperty](/documentation/shazamkit/shmediaitemproperty/confidence)
- [var timeRanges: [Range<TimeInterval>]](/documentation/shazamkit/shmediaitem/timeranges-8msna)
- [var frequencySkewRanges: [Range<Float>]](/documentation/shazamkit/shmediaitem/frequencyskewranges-1j7d3)

### Reading general media item properties

- [var title: String?](/documentation/shazamkit/shmediaitem/title)
- [var subtitle: String?](/documentation/shazamkit/shmediaitem/subtitle)
- [var artist: String?](/documentation/shazamkit/shmediaitem/artist)
- [var artworkURL: URL?](/documentation/shazamkit/shmediaitem/artworkurl)
- [var videoURL: URL?](/documentation/shazamkit/shmediaitem/videourl)
- [var genres: [String]](/documentation/shazamkit/shmediaitem/genres)
- [var explicitContent: Bool](/documentation/shazamkit/shmediaitem/explicitcontent)
- [var creationDate: Date?](/documentation/shazamkit/shmediaitem/creationdate)
- [var isrc: String?](/documentation/shazamkit/shmediaitem/isrc)
- [var id: UUID](/documentation/shazamkit/shmediaitem/id)

### Reading Apple Music properties

- [var songs: [Song]](/documentation/shazamkit/shmediaitem/songs)
- [var appleMusicURL: URL?](/documentation/shazamkit/shmediaitem/applemusicurl)
- [var appleMusicID: String?](/documentation/shazamkit/shmediaitem/applemusicid)

### Working with Shazam music catalog media items

- [var webURL: URL?](/documentation/shazamkit/shmediaitem/weburl)
- [var shazamID: String?](/documentation/shazamkit/shmediaitem/shazamid)
- [class func fetch(shazamID: String, completionHandler: (SHMediaItem?, (any Error)?) -> Void)](/documentation/shazamkit/shmediaitem/fetch(shazamid:completionhandler:))

### Default Implementations

- [Identifiable Implementations](/documentation/shazamkit/shmediaitem/identifiable-implementations)

#### Instance Properties

- [var id: UUID](/documentation/shazamkit/shmediaitem/id)

## Create a signature from audio

- [SHSignature](/documentation/shazamkit/shsignature)

### Creating a signature object

- [init(dataRepresentation: Data) throws](/documentation/shazamkit/shsignature/init(datarepresentation:))

### Reading signature information

- [var dataRepresentation: Data](/documentation/shazamkit/shsignature/datarepresentation)
- [var duration: TimeInterval](/documentation/shazamkit/shsignature/duration)

### Slicing signature segments

- [func slices(from: TimeInterval, duration: TimeInterval, stride: TimeInterval?) throws -> SHSignature.Slices](/documentation/shazamkit/shsignature/slices(from:duration:stride:))
- [SHSignature.Slices](/documentation/shazamkit/shsignature/slices)

#### Supporting types

- [SHSignature.Slices.Iterator](/documentation/shazamkit/shsignature/slices/iterator)

### Getting the content type

- [static var shazamSignature: UTType](/documentation/uniformtypeidentifiers/uttype-swift.struct/shazamsignature)
- [SHSignatureGenerator](/documentation/shazamkit/shsignaturegenerator)

### Generating a signature from audio

- [func append(AVAudioPCMBuffer, at: AVAudioTime?) throws](/documentation/shazamkit/shsignaturegenerator/append(_:at:))
- [func signature() -> SHSignature](/documentation/shazamkit/shsignaturegenerator/signature())
- [Generating a signature from an audio buffer](/documentation/shazamkit/generating-a-signature-from-an-audio-buffer)

### Generate a signature from assets

- [class func generateSignature(from: AVAsset, completionHandler: (SHSignature?, (any Error)?) -> Void)](/documentation/shazamkit/shsignaturegenerator/generatesignature(from:completionhandler:))

## Create a custom audio catalog

- [Building a Custom Catalog and Matching Audio](/documentation/shazamkit/building-a-custom-catalog-and-matching-audio)
- [ShazamKit Dance Finder with Managed Session](/documentation/shazamkit/shazamkit-dance-finder-with-managed-session)
- [SHCustomCatalog](/documentation/shazamkit/shcustomcatalog)

### Creating a custom catalog object

- [init()](/documentation/shazamkit/shcustomcatalog/init())

### Adding a signature to the catalog

- [func addReferenceSignature(SHSignature, representing: [SHMediaItem]) throws](/documentation/shazamkit/shcustomcatalog/addreferencesignature(_:representing:))

### Loading and saving a custom catalog

- [func add(from: URL) throws](/documentation/shazamkit/shcustomcatalog/add(from:))
- [func write(to: URL) throws](/documentation/shazamkit/shcustomcatalog/write(to:))

### Getting the content type

- [static var shazamCustomCatalog: UTType](/documentation/uniformtypeidentifiers/uttype-swift.struct/shazamcustomcatalog)

### Initializers

- [init(dataRepresentation: Data) throws](/documentation/shazamkit/shcustomcatalog/init(datarepresentation:))

### Instance Properties

- [var dataRepresentation: Data](/documentation/shazamkit/shcustomcatalog/datarepresentation)
- [SHCatalog](/documentation/shazamkit/shcatalog)

### Accessing catalog properties

- [var maximumQuerySignatureDuration: TimeInterval](/documentation/shazamkit/shcatalog/maximumquerysignatureduration)
- [var minimumQuerySignatureDuration: TimeInterval](/documentation/shazamkit/shcatalog/minimumquerysignatureduration)

## Update the user’s Shazam library

- [SHLibrary](/documentation/shazamkit/shlibrary)

### Managing the items in the library

- [static let `default`: SHLibrary](/documentation/shazamkit/shlibrary/default)
- [func addItems([SHMediaItem]) async throws](/documentation/shazamkit/shlibrary/additems(_:))
- [func removeItems([SHMediaItem]) async throws](/documentation/shazamkit/shlibrary/removeitems(_:))
- [var items: [SHMediaItem]](/documentation/shazamkit/shlibrary/items)
- [SHMediaLibrary](/documentation/shazamkit/shmedialibrary)

### Adding a matched song to the library

- [class var `default`: SHMediaLibrary](/documentation/shazamkit/shmedialibrary/default)
- [func add([SHMediaItem], completionHandler: ((any Error)?) -> Void)](/documentation/shazamkit/shmedialibrary/add(_:completionhandler:))

## Shazam errors

- [SHError](/documentation/shazamkit/sherror)

### Inspecting an error

- [SHError.Code](/documentation/shazamkit/sherror/code)

#### Matching errors

- [case matchAttemptFailed](/documentation/shazamkit/sherror/code/matchattemptfailed)

#### Signature errors

- [case signatureInvalid](/documentation/shazamkit/sherror/code/signatureinvalid)
- [case signatureDurationInvalid](/documentation/shazamkit/sherror/code/signaturedurationinvalid)

#### Audio format errors

- [case invalidAudioFormat](/documentation/shazamkit/sherror/code/invalidaudioformat)
- [case audioDiscontinuity](/documentation/shazamkit/sherror/code/audiodiscontinuity)

#### Catalog errors

- [case customCatalogInvalidURL](/documentation/shazamkit/sherror/code/customcataloginvalidurl)
- [case customCatalogInvalid](/documentation/shazamkit/sherror/code/customcataloginvalid)

#### Library sync errors

- [case mediaItemFetchFailed](/documentation/shazamkit/sherror/code/mediaitemfetchfailed)
- [case mediaLibrarySyncFailed](/documentation/shazamkit/sherror/code/medialibrarysyncfailed)

#### Framework errors

- [case internalError](/documentation/shazamkit/sherror/code/internalerror)

#### Querying the error domain

- [let SHErrorDomain: String](/documentation/shazamkit/sherrordomain)

#### Initializers

- [init?(rawValue: Int)](/documentation/shazamkit/sherror/code/init(rawvalue:))
- [Error Constants](/documentation/shazamkit/error-constants)

#### Constants

- [static var matchAttemptFailed: SHError.Code](/documentation/shazamkit/sherror/matchattemptfailed)
- [static var signatureInvalid: SHError.Code](/documentation/shazamkit/sherror/signatureinvalid)
- [static var signatureDurationInvalid: SHError.Code](/documentation/shazamkit/sherror/signaturedurationinvalid)
- [static var invalidAudioFormat: SHError.Code](/documentation/shazamkit/sherror/invalidaudioformat)
- [static var internalError: SHError.Code](/documentation/shazamkit/sherror/internalerror)
- [static var audioDiscontinuity: SHError.Code](/documentation/shazamkit/sherror/audiodiscontinuity)
- [static var customCatalogInvalidURL: SHError.Code](/documentation/shazamkit/sherror/customcataloginvalidurl)
- [static var customCatalogInvalid: SHError.Code](/documentation/shazamkit/sherror/customcataloginvalid)
- [static var mediaItemFetchFailed: SHError.Code](/documentation/shazamkit/sherror/mediaitemfetchfailed)
- [static var mediaLibrarySyncFailed: SHError.Code](/documentation/shazamkit/sherror/medialibrarysyncfailed)

### Type Properties

- [static var errorDomain: String](/documentation/shazamkit/sherror/errordomain)

## Reference

- [ShazamKit Enumerations](/documentation/shazamkit/shazamkit-enumerations)

### Enumerations

- [SHError.Code](/documentation/shazamkit/sherror/code)

#### Matching errors

- [case matchAttemptFailed](/documentation/shazamkit/sherror/code/matchattemptfailed)

#### Signature errors

- [case signatureInvalid](/documentation/shazamkit/sherror/code/signatureinvalid)
- [case signatureDurationInvalid](/documentation/shazamkit/sherror/code/signaturedurationinvalid)

#### Audio format errors

- [case invalidAudioFormat](/documentation/shazamkit/sherror/code/invalidaudioformat)
- [case audioDiscontinuity](/documentation/shazamkit/sherror/code/audiodiscontinuity)

#### Catalog errors

- [case customCatalogInvalidURL](/documentation/shazamkit/sherror/code/customcataloginvalidurl)
- [case customCatalogInvalid](/documentation/shazamkit/sherror/code/customcataloginvalid)

#### Library sync errors

- [case mediaItemFetchFailed](/documentation/shazamkit/sherror/code/mediaitemfetchfailed)
- [case mediaLibrarySyncFailed](/documentation/shazamkit/sherror/code/medialibrarysyncfailed)

#### Framework errors

- [case internalError](/documentation/shazamkit/sherror/code/internalerror)

#### Querying the error domain

- [let SHErrorDomain: String](/documentation/shazamkit/sherrordomain)

#### Initializers

- [init?(rawValue: Int)](/documentation/shazamkit/sherror/code/init(rawvalue:))
- [ShazamKit Constants](/documentation/shazamkit/shazamkit-constants)

### Constants

- [let SHErrorDomain: String](/documentation/shazamkit/sherrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
