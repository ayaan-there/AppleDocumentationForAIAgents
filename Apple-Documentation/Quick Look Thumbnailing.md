# Quick Look Thumbnailing Documentation

Source: https://sosumi.ai/documentation/quicklookthumbnailing

---
title: Quick Look Thumbnailing
source: https://developer.apple.com/documentation/quicklookthumbnailing
timestamp: 2026-02-13T19:00:59.986Z
---

## Thumbnail Generation

- [Creating Quick Look Thumbnails to Preview Files in Your App](/documentation/quicklookthumbnailing/creating-quick-look-thumbnails-to-preview-files-in-your-app)
- [QLThumbnailGenerator](/documentation/quicklookthumbnailing/qlthumbnailgenerator)

### Getting the Generator Instance

- [class var shared: QLThumbnailGenerator](/documentation/quicklookthumbnailing/qlthumbnailgenerator/shared)

### Generating a Thumbnail

- [func generateBestRepresentation(for: QLThumbnailGenerator.Request, completion: (QLThumbnailRepresentation?, (any Error)?) -> Void)](/documentation/quicklookthumbnailing/qlthumbnailgenerator/generatebestrepresentation(for:completion:))
- [func generateRepresentations(for: QLThumbnailGenerator.Request, update: ((QLThumbnailRepresentation?, QLThumbnailRepresentation.RepresentationType, (any Error)?) -> Void)?)](/documentation/quicklookthumbnailing/qlthumbnailgenerator/generaterepresentations(for:update:))
- [QLThumbnailGenerator.Request](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request)

#### Creating a Thumbail Request

- [init(fileAt: URL, size: CGSize, scale: CGFloat, representationTypes: QLThumbnailGenerator.Request.RepresentationTypes)](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/init(fileat:size:scale:representationtypes:))

#### Describing the Requested Thumbnail

- [var size: CGSize](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/size)
- [var scale: CGFloat](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/scale)
- [var contentType: UTType!](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/contenttype)
- [var representationTypes: QLThumbnailGenerator.Request.RepresentationTypes](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/representationtypes-swift.property)
- [var minimumDimension: CGFloat](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/minimumdimension)
- [var iconMode: Bool](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/iconmode)
- [QLThumbnailGenerator.Request.RepresentationTypes](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/representationtypes-swift.struct)

##### Creating a Thumbnail Type

- [init(rawValue: UInt)](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/representationtypes-swift.struct/init(rawvalue:))
- [static var all: QLThumbnailGenerator.Request.RepresentationTypes](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/representationtypes-swift.struct/all)
- [static var icon: QLThumbnailGenerator.Request.RepresentationTypes](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/representationtypes-swift.struct/icon)
- [static var lowQualityThumbnail: QLThumbnailGenerator.Request.RepresentationTypes](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/representationtypes-swift.struct/lowqualitythumbnail)
- [static var thumbnail: QLThumbnailGenerator.Request.RepresentationTypes](/documentation/quicklookthumbnailing/qlthumbnailgenerator/request/representationtypes-swift.struct/thumbnail)

### Saving a Thumbnail

- [func saveBestRepresentation(for: QLThumbnailGenerator.Request, to: URL, contentType: String, completion: ((any Error)?) -> Void)](/documentation/quicklookthumbnailing/qlthumbnailgenerator/savebestrepresentation(for:to:contenttype:completion:))

### Canceling

- [func cancel(QLThumbnailGenerator.Request)](/documentation/quicklookthumbnailing/qlthumbnailgenerator/cancel(_:))

### Instance Methods

- [func saveBestRepresentation(for: QLThumbnailGenerator.Request, to: URL, as: UTType, completion: ((any Error)?) -> Void)](/documentation/quicklookthumbnailing/qlthumbnailgenerator/savebestrepresentation(for:to:as:completion:))
- [QLThumbnailRepresentation](/documentation/quicklookthumbnailing/qlthumbnailrepresentation)

### Thumbnail Images

- [var cgImage: CGImage](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/cgimage)
- [var nsImage: NSImage](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/nsimage)
- [var uiImage: UIImage](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/uiimage)
- [var type: QLThumbnailRepresentation.RepresentationType](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/type)
- [var contentRect: CGRect](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/contentrect)
- [QLThumbnailRepresentation.RepresentationType](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/representationtype)

#### Enumeration Cases

- [case icon](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/representationtype/icon)
- [case lowQualityThumbnail](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/representationtype/lowqualitythumbnail)
- [case thumbnail](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/representationtype/thumbnail)

#### Initializers

- [init?(rawValue: Int)](/documentation/quicklookthumbnailing/qlthumbnailrepresentation/representationtype/init(rawvalue:))

## Thumbnails for Custom File Types

- [Providing Thumbnails of Your Custom File Types](/documentation/quicklookthumbnailing/providing-thumbnails-of-your-custom-file-types)
- [QLThumbnailProvider](/documentation/quicklookthumbnailing/qlthumbnailprovider)

### Essentials

- [func provideThumbnail(for: QLFileThumbnailRequest, (QLThumbnailReply?, (any Error)?) -> Void)](/documentation/quicklookthumbnailing/qlthumbnailprovider/providethumbnail(for:_:))
- [QLFileThumbnailRequest](/documentation/quicklookthumbnailing/qlfilethumbnailrequest)

### Describing the Requested Thumbnail

- [var maximumSize: CGSize](/documentation/quicklookthumbnailing/qlfilethumbnailrequest/maximumsize)
- [var minimumSize: CGSize](/documentation/quicklookthumbnailing/qlfilethumbnailrequest/minimumsize)
- [var scale: CGFloat](/documentation/quicklookthumbnailing/qlfilethumbnailrequest/scale)
- [var fileURL: URL](/documentation/quicklookthumbnailing/qlfilethumbnailrequest/fileurl)
- [QLThumbnailReply](/documentation/quicklookthumbnailing/qlthumbnailreply)

### Creating a Thumbnail

- [convenience init(contextSize: CGSize, currentContextDrawing: () -> Bool)](/documentation/quicklookthumbnailing/qlthumbnailreply/init(contextsize:currentcontextdrawing:))
- [convenience init(contextSize: CGSize, drawing: (CGContext) -> Bool)](/documentation/quicklookthumbnailing/qlthumbnailreply/init(contextsize:drawing:))
- [convenience init(imageFileURL: URL)](/documentation/quicklookthumbnailing/qlthumbnailreply/init(imagefileurl:))

### Customizing a Thumbnail Reply

- [var extensionBadge: String](/documentation/quicklookthumbnailing/qlthumbnailreply/extensionbadge)

## Error Information

- [let QLThumbnailErrorDomain: String](/documentation/quicklookthumbnailing/qlthumbnailerrordomain)
- [QLThumbnailError](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct)

### Error Codes

- [static var generationFailed: QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/generationfailed)
- [static var noCachedThumbnail: QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/nocachedthumbnail)
- [static var noCloudThumbnail: QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/nocloudthumbnail)
- [static var requestCancelled: QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/requestcancelled)
- [static var requestInvalid: QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/requestinvalid)
- [static var savingToURLFailed: QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/savingtourlfailed)
- [QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code)

#### Error Codes

- [case generationFailed](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/generationfailed)
- [case noCachedThumbnail](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/nocachedthumbnail)
- [case noCloudThumbnail](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/nocloudthumbnail)
- [case requestCancelled](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/requestcancelled)
- [case requestInvalid](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/requestinvalid)
- [case savingToURLFailed](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/savingtourlfailed)

#### Initializers

- [init?(rawValue: Int)](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/errordomain)
- [QLThumbnailError.Code](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code)

### Error Codes

- [case generationFailed](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/generationfailed)
- [case noCachedThumbnail](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/nocachedthumbnail)
- [case noCloudThumbnail](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/nocloudthumbnail)
- [case requestCancelled](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/requestcancelled)
- [case requestInvalid](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/requestinvalid)
- [case savingToURLFailed](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/savingtourlfailed)

### Initializers

- [init?(rawValue: Int)](/documentation/quicklookthumbnailing/qlthumbnailerror-swift.struct/code/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
