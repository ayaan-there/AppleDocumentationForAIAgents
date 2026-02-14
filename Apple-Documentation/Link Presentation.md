# Link Presentation Documentation

Source: https://sosumi.ai/documentation/linkpresentation

---
title: Link Presentation
source: https://developer.apple.com/documentation/linkpresentation
timestamp: 2026-02-13T18:58:42.787Z
---

## Link metadata

- [LPMetadataProvider](/documentation/linkpresentation/lpmetadataprovider)

### Fetching metadata

- [func startFetchingMetadata(for: URL, completionHandler: (LPLinkMetadata?, (any Error)?) -> Void)](/documentation/linkpresentation/lpmetadataprovider/startfetchingmetadata(for:completionhandler:)-54z5i)
- [func cancel()](/documentation/linkpresentation/lpmetadataprovider/cancel())
- [var shouldFetchSubresources: Bool](/documentation/linkpresentation/lpmetadataprovider/shouldfetchsubresources)
- [var timeout: TimeInterval](/documentation/linkpresentation/lpmetadataprovider/timeout)

### Instance Methods

- [func startFetchingMetadata(for: URLRequest, completionHandler: (LPLinkMetadata?, (any Error)?) -> Void)](/documentation/linkpresentation/lpmetadataprovider/startfetchingmetadata(for:completionhandler:)-9e6s8)
- [LPLinkMetadata](/documentation/linkpresentation/lplinkmetadata)

### Identifying the link

- [var url: URL?](/documentation/linkpresentation/lplinkmetadata/url)
- [var originalURL: URL?](/documentation/linkpresentation/lplinkmetadata/originalurl)

### Getting the link’s title

- [var title: String?](/documentation/linkpresentation/lplinkmetadata/title)

### Getting the link’s images

- [var iconProvider: NSItemProvider?](/documentation/linkpresentation/lplinkmetadata/iconprovider)
- [var imageProvider: NSItemProvider?](/documentation/linkpresentation/lplinkmetadata/imageprovider)

### Getting the link’s video

- [var remoteVideoURL: URL?](/documentation/linkpresentation/lplinkmetadata/remotevideourl)
- [var videoProvider: NSItemProvider?](/documentation/linkpresentation/lplinkmetadata/videoprovider)

## Rich links

- [LPLinkView](/documentation/linkpresentation/lplinkview)

### Creating a link view

- [init(metadata: LPLinkMetadata)](/documentation/linkpresentation/lplinkview/init(metadata:))
- [init(url: URL)](/documentation/linkpresentation/lplinkview/init(url:))

### Specifying metadata

- [var metadata: LPLinkMetadata](/documentation/linkpresentation/lplinkview/metadata)

## Reference

- [LinkPresentation Errors](/documentation/linkpresentation/errors)

### Errors

- [LPError](/documentation/linkpresentation/lperror)

#### Error details

- [var errorCode: Int](/documentation/linkpresentation/lperror/errorcode)
- [var errorUserInfo: [String : Any]](/documentation/linkpresentation/lperror/erroruserinfo)

#### Error domain

- [static var errorDomain: String](/documentation/linkpresentation/lperror/errordomain)
- [let LPErrorDomain: String](/documentation/linkpresentation/lperrordomain)

#### Error codes

- [static var metadataFetchCancelled: LPError.Code](/documentation/linkpresentation/lperror/metadatafetchcancelled)
- [static var metadataFetchFailed: LPError.Code](/documentation/linkpresentation/lperror/metadatafetchfailed)
- [static var metadataFetchTimedOut: LPError.Code](/documentation/linkpresentation/lperror/metadatafetchtimedout)
- [static var unknown: LPError.Code](/documentation/linkpresentation/lperror/unknown)
- [LPError.Code](/documentation/linkpresentation/lperror/code)

##### Error cases

- [case metadataFetchCancelled](/documentation/linkpresentation/lperror/code/metadatafetchcancelled)
- [case metadataFetchFailed](/documentation/linkpresentation/lperror/code/metadatafetchfailed)
- [case metadataFetchTimedOut](/documentation/linkpresentation/lperror/code/metadatafetchtimedout)
- [case unknown](/documentation/linkpresentation/lperror/code/unknown)

##### Enumeration Cases

- [case metadataFetchNotAllowed](/documentation/linkpresentation/lperror/code/metadatafetchnotallowed)

##### Initializers

- [init?(rawValue: Int)](/documentation/linkpresentation/lperror/code/init(rawvalue:))

#### Type Properties

- [static var metadataFetchNotAllowed: LPError.Code](/documentation/linkpresentation/lperror/metadatafetchnotallowed)
- [LPError.Code](/documentation/linkpresentation/lperror/code)

#### Error cases

- [case metadataFetchCancelled](/documentation/linkpresentation/lperror/code/metadatafetchcancelled)
- [case metadataFetchFailed](/documentation/linkpresentation/lperror/code/metadatafetchfailed)
- [case metadataFetchTimedOut](/documentation/linkpresentation/lperror/code/metadatafetchtimedout)
- [case unknown](/documentation/linkpresentation/lperror/code/unknown)

#### Enumeration Cases

- [case metadataFetchNotAllowed](/documentation/linkpresentation/lperror/code/metadatafetchnotallowed)

#### Initializers

- [init?(rawValue: Int)](/documentation/linkpresentation/lperror/code/init(rawvalue:))
- [let LPErrorDomain: String](/documentation/linkpresentation/lperrordomain)
- [LinkPresentation Macros](/documentation/linkpresentation/macros)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
