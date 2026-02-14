# ImageIO Documentation

Source: https://sosumi.ai/documentation/imageio

---
title: Image I/O
source: https://developer.apple.com/documentation/imageio
timestamp: 2026-02-13T19:58:00.275Z
---

## Image Management

- [CGImageSource](/documentation/imageio/cgimagesource)

### Creating an Image Source

- [func CGImageSourceCreateWithURL(CFURL, CFDictionary?) -> CGImageSource?](/documentation/imageio/cgimagesourcecreatewithurl(_:_:))
- [func CGImageSourceCreateWithData(CFData, CFDictionary?) -> CGImageSource?](/documentation/imageio/cgimagesourcecreatewithdata(_:_:))
- [func CGImageSourceCreateWithDataProvider(CGDataProvider, CFDictionary?) -> CGImageSource?](/documentation/imageio/cgimagesourcecreatewithdataprovider(_:_:))
- [func CGImageSourceCreateIncremental(CFDictionary?) -> CGImageSource](/documentation/imageio/cgimagesourcecreateincremental(_:))

### Extracting Images From an Image Source

- [func CGImageSourceCreateImageAtIndex(CGImageSource, Int, CFDictionary?) -> CGImage?](/documentation/imageio/cgimagesourcecreateimageatindex(_:_:_:))
- [func CGImageSourceCreateThumbnailAtIndex(CGImageSource, Int, CFDictionary?) -> CGImage?](/documentation/imageio/cgimagesourcecreatethumbnailatindex(_:_:_:))
- [func CGImageSourceGetPrimaryImageIndex(CGImageSource) -> Int](/documentation/imageio/cgimagesourcegetprimaryimageindex(_:))

### Getting Information From an Image Source

- [func CGImageSourceGetTypeID() -> CFTypeID](/documentation/imageio/cgimagesourcegettypeid())
- [func CGImageSourceGetType(CGImageSource) -> CFString?](/documentation/imageio/cgimagesourcegettype(_:))
- [func CGImageSourceCopyTypeIdentifiers() -> CFArray](/documentation/imageio/cgimagesourcecopytypeidentifiers())
- [func CGImageSourceGetCount(CGImageSource) -> Int](/documentation/imageio/cgimagesourcegetcount(_:))
- [func CGImageSourceCopyProperties(CGImageSource, CFDictionary?) -> CFDictionary?](/documentation/imageio/cgimagesourcecopyproperties(_:_:))
- [func CGImageSourceCopyPropertiesAtIndex(CGImageSource, Int, CFDictionary?) -> CFDictionary?](/documentation/imageio/cgimagesourcecopypropertiesatindex(_:_:_:))
- [func CGImageSourceCopyAuxiliaryDataInfoAtIndex(CGImageSource, Int, CFString) -> CFDictionary?](/documentation/imageio/cgimagesourcecopyauxiliarydatainfoatindex(_:_:_:))

### Updating an Incremental Image

- [func CGImageSourceUpdateData(CGImageSource, CFData, Bool)](/documentation/imageio/cgimagesourceupdatedata(_:_:_:))
- [func CGImageSourceUpdateDataProvider(CGImageSource, CGDataProvider, Bool)](/documentation/imageio/cgimagesourceupdatedataprovider(_:_:_:))

### Getting the Image Status

- [func CGImageSourceGetStatus(CGImageSource) -> CGImageSourceStatus](/documentation/imageio/cgimagesourcegetstatus(_:))
- [func CGImageSourceGetStatusAtIndex(CGImageSource, Int) -> CGImageSourceStatus](/documentation/imageio/cgimagesourcegetstatusatindex(_:_:))
- [CGImageSourceStatus](/documentation/imageio/cgimagesourcestatus)

#### Status Values

- [case statusUnexpectedEOF](/documentation/imageio/cgimagesourcestatus/statusunexpectedeof)
- [case statusInvalidData](/documentation/imageio/cgimagesourcestatus/statusinvaliddata)
- [case statusUnknownType](/documentation/imageio/cgimagesourcestatus/statusunknowntype)
- [case statusReadingHeader](/documentation/imageio/cgimagesourcestatus/statusreadingheader)
- [case statusIncomplete](/documentation/imageio/cgimagesourcestatus/statusincomplete)
- [case statusComplete](/documentation/imageio/cgimagesourcestatus/statuscomplete)

#### Initializers

- [init?(rawValue: Int32)](/documentation/imageio/cgimagesourcestatus/init(rawvalue:))

### Specifying the Read Options

- [let kCGImageSourceTypeIdentifierHint: CFString](/documentation/imageio/kcgimagesourcetypeidentifierhint)
- [let kCGImageSourceShouldAllowFloat: CFString](/documentation/imageio/kcgimagesourceshouldallowfloat)
- [let kCGImageSourceShouldCache: CFString](/documentation/imageio/kcgimagesourceshouldcache)
- [let kCGImageSourceShouldCacheImmediately: CFString](/documentation/imageio/kcgimagesourceshouldcacheimmediately)
- [let kCGImageSourceCreateThumbnailFromImageIfAbsent: CFString](/documentation/imageio/kcgimagesourcecreatethumbnailfromimageifabsent)
- [let kCGImageSourceCreateThumbnailFromImageAlways: CFString](/documentation/imageio/kcgimagesourcecreatethumbnailfromimagealways)
- [let kCGImageSourceThumbnailMaxPixelSize: CFString](/documentation/imageio/kcgimagesourcethumbnailmaxpixelsize)
- [let kCGImageSourceCreateThumbnailWithTransform: CFString](/documentation/imageio/kcgimagesourcecreatethumbnailwithtransform)
- [let kCGImageSourceSubsampleFactor: CFString](/documentation/imageio/kcgimagesourcesubsamplefactor)
- [CGImageDestination](/documentation/imageio/cgimagedestination)

### Creating an Image Destination

- [func CGImageDestinationCreateWithURL(CFURL, CFString, Int, CFDictionary?) -> CGImageDestination?](/documentation/imageio/cgimagedestinationcreatewithurl(_:_:_:_:))
- [func CGImageDestinationCreateWithData(CFMutableData, CFString, Int, CFDictionary?) -> CGImageDestination?](/documentation/imageio/cgimagedestinationcreatewithdata(_:_:_:_:))
- [func CGImageDestinationCreateWithDataConsumer(CGDataConsumer, CFString, Int, CFDictionary?) -> CGImageDestination?](/documentation/imageio/cgimagedestinationcreatewithdataconsumer(_:_:_:_:))

### Adding Images to the Destination

- [func CGImageDestinationAddImage(CGImageDestination, CGImage, CFDictionary?)](/documentation/imageio/cgimagedestinationaddimage(_:_:_:))
- [func CGImageDestinationAddImageFromSource(CGImageDestination, CGImageSource, Int, CFDictionary?)](/documentation/imageio/cgimagedestinationaddimagefromsource(_:_:_:_:))

### Adding Metadata to the Image

- [func CGImageDestinationSetProperties(CGImageDestination, CFDictionary?)](/documentation/imageio/cgimagedestinationsetproperties(_:_:))
- [func CGImageDestinationAddAuxiliaryDataInfo(CGImageDestination, CFString, CFDictionary)](/documentation/imageio/cgimagedestinationaddauxiliarydatainfo(_:_:_:))

### Finalizing the Image Data

- [func CGImageDestinationFinalize(CGImageDestination) -> Bool](/documentation/imageio/cgimagedestinationfinalize(_:))

### Getting the Image Types

- [func CGImageDestinationCopyTypeIdentifiers() -> CFArray](/documentation/imageio/cgimagedestinationcopytypeidentifiers())
- [func CGImageDestinationGetTypeID() -> CFTypeID](/documentation/imageio/cgimagedestinationgettypeid())

### Configuring the Image Behaviors

- [let kCGImageDestinationLossyCompressionQuality: CFString](/documentation/imageio/kcgimagedestinationlossycompressionquality)
- [let kCGImageDestinationBackgroundColor: CFString](/documentation/imageio/kcgimagedestinationbackgroundcolor)
- [let kCGImageDestinationDateTime: CFString](/documentation/imageio/kcgimagedestinationdatetime)
- [let kCGImageDestinationEmbedThumbnail: CFString](/documentation/imageio/kcgimagedestinationembedthumbnail)
- [let kCGImageDestinationImageMaxPixelSize: CFString](/documentation/imageio/kcgimagedestinationimagemaxpixelsize)
- [let kCGImageDestinationMetadata: CFString](/documentation/imageio/kcgimagedestinationmetadata)
- [let kCGImageDestinationMergeMetadata: CFString](/documentation/imageio/kcgimagedestinationmergemetadata)
- [let kCGImageDestinationOptimizeColorForSharing: CFString](/documentation/imageio/kcgimagedestinationoptimizecolorforsharing)
- [let kCGImageDestinationOrientation: CFString](/documentation/imageio/kcgimagedestinationorientation)
- [let kCGImageDestinationPreserveGainMap: CFString](/documentation/imageio/kcgimagedestinationpreservegainmap)
- [let kCGImageMetadataShouldExcludeGPS: CFString](/documentation/imageio/kcgimagemetadatashouldexcludegps)
- [let kCGImageMetadataShouldExcludeXMP: CFString](/documentation/imageio/kcgimagemetadatashouldexcludexmp)

## XMP Metadata

- [CGImageMetadata](/documentation/imageio/cgimagemetadata)

### Creating an Image Metadata Type

- [func CGImageMetadataCreateFromXMPData(CFData) -> CGImageMetadata?](/documentation/imageio/cgimagemetadatacreatefromxmpdata(_:))

### Getting the Metadata Tags

- [func CGImageMetadataCopyTagWithPath(CGImageMetadata, CGImageMetadataTag?, CFString) -> CGImageMetadataTag?](/documentation/imageio/cgimagemetadatacopytagwithpath(_:_:_:))
- [func CGImageMetadataCopyTags(CGImageMetadata) -> CFArray?](/documentation/imageio/cgimagemetadatacopytags(_:))
- [func CGImageMetadataCopyTagMatchingImageProperty(CGImageMetadata, CFString, CFString) -> CGImageMetadataTag?](/documentation/imageio/cgimagemetadatacopytagmatchingimageproperty(_:_:_:))
- [func CGImageMetadataCopyStringValueWithPath(CGImageMetadata, CGImageMetadataTag?, CFString) -> CFString?](/documentation/imageio/cgimagemetadatacopystringvaluewithpath(_:_:_:))

### Enumerating the Metadata Tags

- [func CGImageMetadataEnumerateTagsUsingBlock(CGImageMetadata, CFString?, CFDictionary?, CGImageMetadataTagBlock)](/documentation/imageio/cgimagemetadataenumeratetagsusingblock(_:_:_:_:))
- [CGImageMetadataTagBlock](/documentation/imageio/cgimagemetadatatagblock)
- [let kCGImageMetadataEnumerateRecursively: CFString](/documentation/imageio/kcgimagemetadataenumeraterecursively)

### Generating XMP Data

- [func CGImageMetadataCreateXMPData(CGImageMetadata, CFDictionary?) -> CFData?](/documentation/imageio/cgimagemetadatacreatexmpdata(_:_:))

### Getting the Core Foundation Type

- [func CGImageMetadataGetTypeID() -> CFTypeID](/documentation/imageio/cgimagemetadatagettypeid())
- [CGMutableImageMetadata](/documentation/imageio/cgmutableimagemetadata)

### Creating a Mutable Metadata Type

- [func CGImageMetadataCreateMutable() -> CGMutableImageMetadata](/documentation/imageio/cgimagemetadatacreatemutable())
- [func CGImageMetadataCreateMutableCopy(CGImageMetadata) -> CGMutableImageMetadata?](/documentation/imageio/cgimagemetadatacreatemutablecopy(_:))

### Setting the Values of Tags

- [func CGImageMetadataSetValueWithPath(CGMutableImageMetadata, CGImageMetadataTag?, CFString, CFTypeRef) -> Bool](/documentation/imageio/cgimagemetadatasetvaluewithpath(_:_:_:_:))
- [func CGImageMetadataSetValueMatchingImageProperty(CGMutableImageMetadata, CFString, CFString, CFTypeRef) -> Bool](/documentation/imageio/cgimagemetadatasetvaluematchingimageproperty(_:_:_:_:))
- [func CGImageMetadataSetTagWithPath(CGMutableImageMetadata, CGImageMetadataTag?, CFString, CGImageMetadataTag) -> Bool](/documentation/imageio/cgimagemetadatasettagwithpath(_:_:_:_:))
- [func CGImageMetadataRemoveTagWithPath(CGMutableImageMetadata, CGImageMetadataTag?, CFString) -> Bool](/documentation/imageio/cgimagemetadataremovetagwithpath(_:_:_:))

### Registering a Custom Namespace

- [func CGImageMetadataRegisterNamespaceForPrefix(CGMutableImageMetadata, CFString, CFString, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/imageio/cgimagemetadataregisternamespaceforprefix(_:_:_:_:))
- [CGImageMetadataTag](/documentation/imageio/cgimagemetadatatag)

### Creating a Metadata Tag

- [func CGImageMetadataTagCreate(CFString, CFString?, CFString, CGImageMetadataType, CFTypeRef) -> CGImageMetadataTag?](/documentation/imageio/cgimagemetadatatagcreate(_:_:_:_:_:))

### Getting the Attributes of the Tag

- [func CGImageMetadataTagCopyNamespace(CGImageMetadataTag) -> CFString?](/documentation/imageio/cgimagemetadatatagcopynamespace(_:))
- [func CGImageMetadataTagCopyPrefix(CGImageMetadataTag) -> CFString?](/documentation/imageio/cgimagemetadatatagcopyprefix(_:))
- [func CGImageMetadataTagCopyName(CGImageMetadataTag) -> CFString?](/documentation/imageio/cgimagemetadatatagcopyname(_:))
- [func CGImageMetadataTagCopyValue(CGImageMetadataTag) -> CFTypeRef?](/documentation/imageio/cgimagemetadatatagcopyvalue(_:))
- [func CGImageMetadataTagCopyQualifiers(CGImageMetadataTag) -> CFArray?](/documentation/imageio/cgimagemetadatatagcopyqualifiers(_:))

### Getting the Tag Type

- [func CGImageMetadataTagGetType(CGImageMetadataTag) -> CGImageMetadataType](/documentation/imageio/cgimagemetadatataggettype(_:))
- [CGImageMetadataType](/documentation/imageio/cgimagemetadatatype)

#### Metadata Types

- [case invalid](/documentation/imageio/cgimagemetadatatype/invalid)
- [case `default`](/documentation/imageio/cgimagemetadatatype/default)
- [case string](/documentation/imageio/cgimagemetadatatype/string)
- [case arrayUnordered](/documentation/imageio/cgimagemetadatatype/arrayunordered)
- [case arrayOrdered](/documentation/imageio/cgimagemetadatatype/arrayordered)
- [case alternateArray](/documentation/imageio/cgimagemetadatatype/alternatearray)
- [case alternateText](/documentation/imageio/cgimagemetadatatype/alternatetext)
- [case structure](/documentation/imageio/cgimagemetadatatype/structure)

#### Initializers

- [init?(rawValue: Int32)](/documentation/imageio/cgimagemetadatatype/init(rawvalue:))

### Getting the Core Foundation Type

- [func CGImageMetadataTagGetTypeID() -> CFTypeID](/documentation/imageio/cgimagemetadatataggettypeid())
- [XMP Namespaces and Prefixes](/documentation/imageio/xmp-namespaces-and-prefixes)

### Public Namespaces

- [let kCGImageMetadataNamespaceDublinCore: CFString](/documentation/imageio/kcgimagemetadatanamespacedublincore)
- [let kCGImageMetadataNamespaceExif: CFString](/documentation/imageio/kcgimagemetadatanamespaceexif)
- [let kCGImageMetadataNamespaceExifAux: CFString](/documentation/imageio/kcgimagemetadatanamespaceexifaux)
- [let kCGImageMetadataNamespaceExifEX: CFString](/documentation/imageio/kcgimagemetadatanamespaceexifex)
- [let kCGImageMetadataNamespaceIPTCCore: CFString](/documentation/imageio/kcgimagemetadatanamespaceiptccore)
- [let kCGImageMetadataNamespacePhotoshop: CFString](/documentation/imageio/kcgimagemetadatanamespacephotoshop)
- [let kCGImageMetadataNamespaceTIFF: CFString](/documentation/imageio/kcgimagemetadatanamespacetiff)
- [let kCGImageMetadataNamespaceXMPBasic: CFString](/documentation/imageio/kcgimagemetadatanamespacexmpbasic)
- [let kCGImageMetadataNamespaceXMPRights: CFString](/documentation/imageio/kcgimagemetadatanamespacexmprights)

### Public Prefixes

- [let kCGImageMetadataPrefixDublinCore: CFString](/documentation/imageio/kcgimagemetadataprefixdublincore)
- [let kCGImageMetadataPrefixExif: CFString](/documentation/imageio/kcgimagemetadataprefixexif)
- [let kCGImageMetadataPrefixExifAux: CFString](/documentation/imageio/kcgimagemetadataprefixexifaux)
- [let kCGImageMetadataPrefixExifEX: CFString](/documentation/imageio/kcgimagemetadataprefixexifex)
- [let kCGImageMetadataPrefixIPTCCore: CFString](/documentation/imageio/kcgimagemetadataprefixiptccore)
- [let kCGImageMetadataPrefixPhotoshop: CFString](/documentation/imageio/kcgimagemetadataprefixphotoshop)
- [let kCGImageMetadataPrefixTIFF: CFString](/documentation/imageio/kcgimagemetadataprefixtiff)
- [let kCGImageMetadataPrefixXMPBasic: CFString](/documentation/imageio/kcgimagemetadataprefixxmpbasic)
- [let kCGImageMetadataPrefixXMPRights: CFString](/documentation/imageio/kcgimagemetadataprefixxmprights)
- [let kCFErrorDomainCGImageMetadata: CFString](/documentation/imageio/kcferrordomaincgimagemetadata)
- [CGImageMetadataErrors](/documentation/imageio/cgimagemetadataerrors)

### Error Codes

- [case unknown](/documentation/imageio/cgimagemetadataerrors/unknown)
- [case unsupportedFormat](/documentation/imageio/cgimagemetadataerrors/unsupportedformat)
- [case badArgument](/documentation/imageio/cgimagemetadataerrors/badargument)
- [case conflictingArguments](/documentation/imageio/cgimagemetadataerrors/conflictingarguments)
- [case prefixConflict](/documentation/imageio/cgimagemetadataerrors/prefixconflict)

### Initializers

- [init?(rawValue: Int32)](/documentation/imageio/cgimagemetadataerrors/init(rawvalue:))

## Common Image Properties

- [Image Properties](/documentation/imageio/image-properties)

### Dictionary

- [let kCGImagePropertyFileContentsDictionary: CFString](/documentation/imageio/kcgimagepropertyfilecontentsdictionary)

### Container File Size

- [let kCGImagePropertyFileSize: CFString](/documentation/imageio/kcgimagepropertyfilesize)

### Image Information

- [let kCGImagePropertyImageCount: CFString](/documentation/imageio/kcgimagepropertyimagecount)
- [let kCGImagePropertyIsIndexed: CFString](/documentation/imageio/kcgimagepropertyisindexed)
- [let kCGImagePropertyImages: CFString](/documentation/imageio/kcgimagepropertyimages)
- [let kCGImagePropertyThumbnailImages: CFString](/documentation/imageio/kcgimagepropertythumbnailimages)
- [let kCGImagePropertyPrimaryImage: CFString](/documentation/imageio/kcgimagepropertyprimaryimage)
- [let kCGImagePropertyIsFloat: CFString](/documentation/imageio/kcgimagepropertyisfloat)
- [let kCGImagePropertyOrientation: CFString](/documentation/imageio/kcgimagepropertyorientation)
- [Individual Image Properties](/documentation/imageio/individual-image-properties)

#### Image Size

- [let kCGImagePropertyHeight: CFString](/documentation/imageio/kcgimagepropertyheight)
- [let kCGImagePropertyWidth: CFString](/documentation/imageio/kcgimagepropertywidth)
- [let kCGImagePropertyBytesPerRow: CFString](/documentation/imageio/kcgimagepropertybytesperrow)

#### Auxiliary Data Types

- [let kCGImageAuxiliaryDataTypeDepth: CFString](/documentation/imageio/kcgimageauxiliarydatatypedepth)
- [let kCGImageAuxiliaryDataTypeDisparity: CFString](/documentation/imageio/kcgimageauxiliarydatatypedisparity)
- [let kCGImageAuxiliaryDataTypeHDRGainMap: CFString](/documentation/imageio/kcgimageauxiliarydatatypehdrgainmap)
- [let kCGImageAuxiliaryDataTypePortraitEffectsMatte: CFString](/documentation/imageio/kcgimageauxiliarydatatypeportraiteffectsmatte)
- [let kCGImageAuxiliaryDataTypeSemanticSegmentationGlassesMatte: CFString](/documentation/imageio/kcgimageauxiliarydatatypesemanticsegmentationglassesmatte)
- [let kCGImageAuxiliaryDataTypeSemanticSegmentationHairMatte: CFString](/documentation/imageio/kcgimageauxiliarydatatypesemanticsegmentationhairmatte)
- [let kCGImageAuxiliaryDataTypeSemanticSegmentationSkinMatte: CFString](/documentation/imageio/kcgimageauxiliarydatatypesemanticsegmentationskinmatte)
- [let kCGImageAuxiliaryDataTypeSemanticSegmentationSkyMatte: CFString](/documentation/imageio/kcgimageauxiliarydatatypesemanticsegmentationskymatte)
- [let kCGImageAuxiliaryDataTypeSemanticSegmentationTeethMatte: CFString](/documentation/imageio/kcgimageauxiliarydatatypesemanticsegmentationteethmatte)

#### Auxiliary Image Data

- [let kCGImagePropertyAuxiliaryData: CFString](/documentation/imageio/kcgimagepropertyauxiliarydata)
- [let kCGImagePropertyAuxiliaryDataType: CFString](/documentation/imageio/kcgimagepropertyauxiliarydatatype)
- [let kCGImageAuxiliaryDataInfoData: CFString](/documentation/imageio/kcgimageauxiliarydatainfodata)
- [let kCGImageAuxiliaryDataInfoDataDescription: CFString](/documentation/imageio/kcgimageauxiliarydatainfodatadescription)
- [let kCGImageAuxiliaryDataInfoMetadata: CFString](/documentation/imageio/kcgimageauxiliarydatainfometadata)

#### Open EXR Properties

- [let kCGImagePropertyOpenEXRDictionary: CFString](/documentation/imageio/kcgimagepropertyopenexrdictionary)
- [let kCGImagePropertyOpenEXRAspectRatio: CFString](/documentation/imageio/kcgimagepropertyopenexraspectratio)
- [CGImagePropertyOrientation](/documentation/imageio/cgimagepropertyorientation)

#### Image Orientations

- [case up](/documentation/imageio/cgimagepropertyorientation/up)
- [case upMirrored](/documentation/imageio/cgimagepropertyorientation/upmirrored)
- [case down](/documentation/imageio/cgimagepropertyorientation/down)
- [case downMirrored](/documentation/imageio/cgimagepropertyorientation/downmirrored)
- [case leftMirrored](/documentation/imageio/cgimagepropertyorientation/leftmirrored)
- [case right](/documentation/imageio/cgimagepropertyorientation/right)
- [case rightMirrored](/documentation/imageio/cgimagepropertyorientation/rightmirrored)
- [case left](/documentation/imageio/cgimagepropertyorientation/left)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/imageio/cgimagepropertyorientation/init(rawvalue:))

### Pixel Information

- [let kCGImagePropertyPixelFormat: CFString](/documentation/imageio/kcgimagepropertypixelformat)
- [let kCGImagePropertyPixelWidth: CFString](/documentation/imageio/kcgimagepropertypixelwidth)
- [let kCGImagePropertyPixelHeight: CFString](/documentation/imageio/kcgimagepropertypixelheight)
- [let kCGImagePropertyDPIHeight: CFString](/documentation/imageio/kcgimagepropertydpiheight)
- [let kCGImagePropertyDPIWidth: CFString](/documentation/imageio/kcgimagepropertydpiwidth)
- [let kCGImagePropertyDepth: CFString](/documentation/imageio/kcgimagepropertydepth)

### Color Information

- [let kCGImagePropertyHasAlpha: CFString](/documentation/imageio/kcgimagepropertyhasalpha)
- [let kCGImagePropertyNamedColorSpace: CFString](/documentation/imageio/kcgimagepropertynamedcolorspace)
- [let kCGImagePropertyProfileName: CFString](/documentation/imageio/kcgimagepropertyprofilename)
- [let kCGImagePropertyColorModel: CFString](/documentation/imageio/kcgimagepropertycolormodel)
- [let kCGImagePropertyColorModelRGB: CFString](/documentation/imageio/kcgimagepropertycolormodelrgb)
- [let kCGImagePropertyColorModelCMYK: CFString](/documentation/imageio/kcgimagepropertycolormodelcmyk)
- [let kCGImagePropertyColorModelGray: CFString](/documentation/imageio/kcgimagepropertycolormodelgray)
- [let kCGImagePropertyColorModelLab: CFString](/documentation/imageio/kcgimagepropertycolormodellab)
- [EXIF Dictionary Keys](/documentation/imageio/exif-dictionary-keys)

### Dictionaries

- [let kCGImagePropertyExifDictionary: CFString](/documentation/imageio/kcgimagepropertyexifdictionary)
- [let kCGImagePropertyExifAuxDictionary: CFString](/documentation/imageio/kcgimagepropertyexifauxdictionary)

### Camera Settings

- [let kCGImagePropertyExifDeviceSettingDescription: CFString](/documentation/imageio/kcgimagepropertyexifdevicesettingdescription)
- [let kCGImagePropertyExifFNumber: CFString](/documentation/imageio/kcgimagepropertyexiffnumber)
- [let kCGImagePropertyExifShutterSpeedValue: CFString](/documentation/imageio/kcgimagepropertyexifshutterspeedvalue)
- [let kCGImagePropertyExifApertureValue: CFString](/documentation/imageio/kcgimagepropertyexifaperturevalue)
- [let kCGImagePropertyExifMaxApertureValue: CFString](/documentation/imageio/kcgimagepropertyexifmaxaperturevalue)
- [let kCGImagePropertyExifFocalLength: CFString](/documentation/imageio/kcgimagepropertyexiffocallength)
- [let kCGImagePropertyExifSpectralSensitivity: CFString](/documentation/imageio/kcgimagepropertyexifspectralsensitivity)
- [let kCGImagePropertyExifISOSpeedRatings: CFString](/documentation/imageio/kcgimagepropertyexifisospeedratings)
- [let kCGImagePropertyExifSubjectDistance: CFString](/documentation/imageio/kcgimagepropertyexifsubjectdistance)
- [let kCGImagePropertyExifMeteringMode: CFString](/documentation/imageio/kcgimagepropertyexifmeteringmode)
- [let kCGImagePropertyExifSubjectArea: CFString](/documentation/imageio/kcgimagepropertyexifsubjectarea)
- [let kCGImagePropertyExifSubjectLocation: CFString](/documentation/imageio/kcgimagepropertyexifsubjectlocation)
- [let kCGImagePropertyExifSensingMethod: CFString](/documentation/imageio/kcgimagepropertyexifsensingmethod)
- [let kCGImagePropertyExifSceneType: CFString](/documentation/imageio/kcgimagepropertyexifscenetype)
- [let kCGImagePropertyExifDigitalZoomRatio: CFString](/documentation/imageio/kcgimagepropertyexifdigitalzoomratio)
- [let kCGImagePropertyExifFocalLenIn35mmFilm: CFString](/documentation/imageio/kcgimagepropertyexiffocallenin35mmfilm)
- [let kCGImagePropertyExifSceneCaptureType: CFString](/documentation/imageio/kcgimagepropertyexifscenecapturetype)
- [let kCGImagePropertyExifSubjectDistRange: CFString](/documentation/imageio/kcgimagepropertyexifsubjectdistrange)

### Exposure

- [let kCGImagePropertyExifExposureTime: CFString](/documentation/imageio/kcgimagepropertyexifexposuretime)
- [let kCGImagePropertyExifExposureProgram: CFString](/documentation/imageio/kcgimagepropertyexifexposureprogram)
- [let kCGImagePropertyExifExposureIndex: CFString](/documentation/imageio/kcgimagepropertyexifexposureindex)
- [let kCGImagePropertyExifExposureMode: CFString](/documentation/imageio/kcgimagepropertyexifexposuremode)
- [let kCGImagePropertyExifISOSpeed: CFString](/documentation/imageio/kcgimagepropertyexifisospeed)
- [let kCGImagePropertyExifISOSpeedLatitudeyyy: CFString](/documentation/imageio/kcgimagepropertyexifisospeedlatitudeyyy)
- [let kCGImagePropertyExifISOSpeedLatitudezzz: CFString](/documentation/imageio/kcgimagepropertyexifisospeedlatitudezzz)
- [let kCGImagePropertyExifRecommendedExposureIndex: CFString](/documentation/imageio/kcgimagepropertyexifrecommendedexposureindex)
- [let kCGImagePropertyExifExposureBiasValue: CFString](/documentation/imageio/kcgimagepropertyexifexposurebiasvalue)
- [let kCGImagePropertyExifSensitivityType: CFString](/documentation/imageio/kcgimagepropertyexifsensitivitytype)
- [let kCGImagePropertyExifStandardOutputSensitivity: CFString](/documentation/imageio/kcgimagepropertyexifstandardoutputsensitivity)
- [let kCGImagePropertyExifSourceExposureTimesOfCompositeImage: CFString](/documentation/imageio/kcgimagepropertyexifsourceexposuretimesofcompositeimage)

### Image Quality

- [let kCGImagePropertyExifCFAPattern: CFString](/documentation/imageio/kcgimagepropertyexifcfapattern)
- [let kCGImagePropertyExifBrightnessValue: CFString](/documentation/imageio/kcgimagepropertyexifbrightnessvalue)
- [let kCGImagePropertyExifLightSource: CFString](/documentation/imageio/kcgimagepropertyexiflightsource)
- [let kCGImagePropertyExifFlash: CFString](/documentation/imageio/kcgimagepropertyexifflash)
- [let kCGImagePropertyExifSpatialFrequencyResponse: CFString](/documentation/imageio/kcgimagepropertyexifspatialfrequencyresponse)
- [let kCGImagePropertyExifContrast: CFString](/documentation/imageio/kcgimagepropertyexifcontrast)
- [let kCGImagePropertyExifSaturation: CFString](/documentation/imageio/kcgimagepropertyexifsaturation)
- [let kCGImagePropertyExifSharpness: CFString](/documentation/imageio/kcgimagepropertyexifsharpness)
- [let kCGImagePropertyExifGamma: CFString](/documentation/imageio/kcgimagepropertyexifgamma)
- [let kCGImagePropertyExifWhiteBalance: CFString](/documentation/imageio/kcgimagepropertyexifwhitebalance)

### Image Settings

- [let kCGImagePropertyExifGainControl: CFString](/documentation/imageio/kcgimagepropertyexifgaincontrol)
- [let kCGImagePropertyExifImageUniqueID: CFString](/documentation/imageio/kcgimagepropertyexifimageuniqueid)
- [let kCGImagePropertyExifCompressedBitsPerPixel: CFString](/documentation/imageio/kcgimagepropertyexifcompressedbitsperpixel)
- [let kCGImagePropertyExifColorSpace: CFString](/documentation/imageio/kcgimagepropertyexifcolorspace)
- [let kCGImagePropertyExifPixelXDimension: CFString](/documentation/imageio/kcgimagepropertyexifpixelxdimension)
- [let kCGImagePropertyExifPixelYDimension: CFString](/documentation/imageio/kcgimagepropertyexifpixelydimension)
- [let kCGImagePropertyExifRelatedSoundFile: CFString](/documentation/imageio/kcgimagepropertyexifrelatedsoundfile)
- [let kCGImagePropertyExifFocalPlaneXResolution: CFString](/documentation/imageio/kcgimagepropertyexiffocalplanexresolution)
- [let kCGImagePropertyExifFocalPlaneYResolution: CFString](/documentation/imageio/kcgimagepropertyexiffocalplaneyresolution)
- [let kCGImagePropertyExifFocalPlaneResolutionUnit: CFString](/documentation/imageio/kcgimagepropertyexiffocalplaneresolutionunit)
- [let kCGImagePropertyExifCustomRendered: CFString](/documentation/imageio/kcgimagepropertyexifcustomrendered)
- [let kCGImagePropertyExifCompositeImage: CFString](/documentation/imageio/kcgimagepropertyexifcompositeimage)
- [let kCGImagePropertyExifOECF: CFString](/documentation/imageio/kcgimagepropertyexifoecf)
- [let kCGImagePropertyExifComponentsConfiguration: CFString](/documentation/imageio/kcgimagepropertyexifcomponentsconfiguration)
- [let kCGImagePropertyExifSourceImageNumberOfCompositeImage: CFString](/documentation/imageio/kcgimagepropertyexifsourceimagenumberofcompositeimage)
- [let kCGImagePropertyExifFileSource: CFString](/documentation/imageio/kcgimagepropertyexiffilesource)

### Timestamp

- [let kCGImagePropertyExifDateTimeOriginal: CFString](/documentation/imageio/kcgimagepropertyexifdatetimeoriginal)
- [let kCGImagePropertyExifDateTimeDigitized: CFString](/documentation/imageio/kcgimagepropertyexifdatetimedigitized)
- [let kCGImagePropertyExifSubsecTime: CFString](/documentation/imageio/kcgimagepropertyexifsubsectime)
- [let kCGImagePropertyExifSubsecTimeOrginal: CFString](/documentation/imageio/kcgimagepropertyexifsubsectimeorginal)
- [let kCGImagePropertyExifSubsecTimeOriginal: CFString](/documentation/imageio/kcgimagepropertyexifsubsectimeoriginal)
- [let kCGImagePropertyExifSubsecTimeDigitized: CFString](/documentation/imageio/kcgimagepropertyexifsubsectimedigitized)
- [let kCGImagePropertyExifOffsetTime: CFString](/documentation/imageio/kcgimagepropertyexifoffsettime)
- [let kCGImagePropertyExifOffsetTimeOriginal: CFString](/documentation/imageio/kcgimagepropertyexifoffsettimeoriginal)
- [let kCGImagePropertyExifOffsetTimeDigitized: CFString](/documentation/imageio/kcgimagepropertyexifoffsettimedigitized)

### Lens Information

- [let kCGImagePropertyExifLensSpecification: CFString](/documentation/imageio/kcgimagepropertyexiflensspecification)
- [let kCGImagePropertyExifLensMake: CFString](/documentation/imageio/kcgimagepropertyexiflensmake)
- [let kCGImagePropertyExifLensModel: CFString](/documentation/imageio/kcgimagepropertyexiflensmodel)
- [let kCGImagePropertyExifLensSerialNumber: CFString](/documentation/imageio/kcgimagepropertyexiflensserialnumber)

### Camera Information

- [let kCGImagePropertyExifMakerNote: CFString](/documentation/imageio/kcgimagepropertyexifmakernote)
- [let kCGImagePropertyExifUserComment: CFString](/documentation/imageio/kcgimagepropertyexifusercomment)
- [let kCGImagePropertyExifCameraOwnerName: CFString](/documentation/imageio/kcgimagepropertyexifcameraownername)
- [let kCGImagePropertyExifBodySerialNumber: CFString](/documentation/imageio/kcgimagepropertyexifbodyserialnumber)

### Flash Information

- [let kCGImagePropertyExifFlashPixVersion: CFString](/documentation/imageio/kcgimagepropertyexifflashpixversion)
- [let kCGImagePropertyExifFlashEnergy: CFString](/documentation/imageio/kcgimagepropertyexifflashenergy)

### Auxiliary Keys

- [let kCGImagePropertyExifAuxLensInfo: CFString](/documentation/imageio/kcgimagepropertyexifauxlensinfo)
- [let kCGImagePropertyExifAuxLensModel: CFString](/documentation/imageio/kcgimagepropertyexifauxlensmodel)
- [let kCGImagePropertyExifAuxSerialNumber: CFString](/documentation/imageio/kcgimagepropertyexifauxserialnumber)
- [let kCGImagePropertyExifAuxLensID: CFString](/documentation/imageio/kcgimagepropertyexifauxlensid)
- [let kCGImagePropertyExifAuxLensSerialNumber: CFString](/documentation/imageio/kcgimagepropertyexifauxlensserialnumber)
- [let kCGImagePropertyExifAuxImageNumber: CFString](/documentation/imageio/kcgimagepropertyexifauximagenumber)
- [let kCGImagePropertyExifAuxFlashCompensation: CFString](/documentation/imageio/kcgimagepropertyexifauxflashcompensation)
- [let kCGImagePropertyExifAuxOwnerName: CFString](/documentation/imageio/kcgimagepropertyexifauxownername)
- [let kCGImagePropertyExifAuxFirmware: CFString](/documentation/imageio/kcgimagepropertyexifauxfirmware)

### EXIF Format

- [let kCGImagePropertyExifVersion: CFString](/documentation/imageio/kcgimagepropertyexifversion)
- [IPTC Dictionary Keys](/documentation/imageio/iptc-dictionary-keys)

### Dictionary

- [let kCGImagePropertyIPTCDictionary: CFString](/documentation/imageio/kcgimagepropertyiptcdictionary)

### Image Categorization

- [let kCGImagePropertyIPTCUrgency: CFString](/documentation/imageio/kcgimagepropertyiptcurgency)
- [let kCGImagePropertyIPTCSubjectReference: CFString](/documentation/imageio/kcgimagepropertyiptcsubjectreference)
- [let kCGImagePropertyIPTCCategory: CFString](/documentation/imageio/kcgimagepropertyiptccategory)
- [let kCGImagePropertyIPTCSupplementalCategory: CFString](/documentation/imageio/kcgimagepropertyiptcsupplementalcategory)
- [let kCGImagePropertyIPTCFixtureIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcfixtureidentifier)
- [let kCGImagePropertyIPTCKeywords: CFString](/documentation/imageio/kcgimagepropertyiptckeywords)
- [let kCGImagePropertyIPTCContentLocationCode: CFString](/documentation/imageio/kcgimagepropertyiptccontentlocationcode)
- [let kCGImagePropertyIPTCContentLocationName: CFString](/documentation/imageio/kcgimagepropertyiptccontentlocationname)
- [let kCGImagePropertyIPTCEditStatus: CFString](/documentation/imageio/kcgimagepropertyiptceditstatus)
- [let kCGImagePropertyIPTCEditorialUpdate: CFString](/documentation/imageio/kcgimagepropertyiptceditorialupdate)
- [let kCGImagePropertyIPTCObjectCycle: CFString](/documentation/imageio/kcgimagepropertyiptcobjectcycle)

### Image Information

- [let kCGImagePropertyIPTCImageType: CFString](/documentation/imageio/kcgimagepropertyiptcimagetype)
- [let kCGImagePropertyIPTCImageOrientation: CFString](/documentation/imageio/kcgimagepropertyiptcimageorientation)
- [let kCGImagePropertyIPTCLanguageIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptclanguageidentifier)
- [let kCGImagePropertyIPTCCaptionAbstract: CFString](/documentation/imageio/kcgimagepropertyiptccaptionabstract)
- [let kCGImagePropertyIPTCHeadline: CFString](/documentation/imageio/kcgimagepropertyiptcheadline)
- [let kCGImagePropertyIPTCCredit: CFString](/documentation/imageio/kcgimagepropertyiptccredit)
- [let kCGImagePropertyIPTCStarRating: CFString](/documentation/imageio/kcgimagepropertyiptcstarrating)
- [let kCGImagePropertyIPTCScene: CFString](/documentation/imageio/kcgimagepropertyiptcscene)

### Copyright

- [let kCGImagePropertyIPTCCopyrightNotice: CFString](/documentation/imageio/kcgimagepropertyiptccopyrightnotice)
- [let kCGImagePropertyIPTCRightsUsageTerms: CFString](/documentation/imageio/kcgimagepropertyiptcrightsusageterms)

### Release Information

- [let kCGImagePropertyIPTCReleaseDate: CFString](/documentation/imageio/kcgimagepropertyiptcreleasedate)
- [let kCGImagePropertyIPTCReleaseTime: CFString](/documentation/imageio/kcgimagepropertyiptcreleasetime)
- [let kCGImagePropertyIPTCExpirationDate: CFString](/documentation/imageio/kcgimagepropertyiptcexpirationdate)
- [let kCGImagePropertyIPTCExpirationTime: CFString](/documentation/imageio/kcgimagepropertyiptcexpirationtime)
- [let kCGImagePropertyIPTCSpecialInstructions: CFString](/documentation/imageio/kcgimagepropertyiptcspecialinstructions)
- [let kCGImagePropertyIPTCActionAdvised: CFString](/documentation/imageio/kcgimagepropertyiptcactionadvised)
- [let kCGImagePropertyIPTCReferenceService: CFString](/documentation/imageio/kcgimagepropertyiptcreferenceservice)
- [let kCGImagePropertyIPTCReferenceDate: CFString](/documentation/imageio/kcgimagepropertyiptcreferencedate)
- [let kCGImagePropertyIPTCReferenceNumber: CFString](/documentation/imageio/kcgimagepropertyiptcreferencenumber)
- [let kCGImagePropertyIPTCDateCreated: CFString](/documentation/imageio/kcgimagepropertyiptcdatecreated)
- [let kCGImagePropertyIPTCTimeCreated: CFString](/documentation/imageio/kcgimagepropertyiptctimecreated)
- [let kCGImagePropertyIPTCDigitalCreationDate: CFString](/documentation/imageio/kcgimagepropertyiptcdigitalcreationdate)
- [let kCGImagePropertyIPTCDigitalCreationTime: CFString](/documentation/imageio/kcgimagepropertyiptcdigitalcreationtime)

### Personnel

- [let kCGImagePropertyIPTCByline: CFString](/documentation/imageio/kcgimagepropertyiptcbyline)
- [let kCGImagePropertyIPTCBylineTitle: CFString](/documentation/imageio/kcgimagepropertyiptcbylinetitle)
- [let kCGImagePropertyIPTCSource: CFString](/documentation/imageio/kcgimagepropertyiptcsource)
- [let kCGImagePropertyIPTCContact: CFString](/documentation/imageio/kcgimagepropertyiptccontact)
- [let kCGImagePropertyIPTCWriterEditor: CFString](/documentation/imageio/kcgimagepropertyiptcwritereditor)
- [let kCGImagePropertyIPTCCreatorContactInfo: CFString](/documentation/imageio/kcgimagepropertyiptccreatorcontactinfo)
- [IPTC Creator Contact Info Dictionary Keys](/documentation/imageio/iptc-creator-contact-info-dictionary-keys)

#### Extended Properties

- [let kCGImagePropertyIPTCExtAboutCvTerm: CFString](/documentation/imageio/kcgimagepropertyiptcextaboutcvterm)
- [let kCGImagePropertyIPTCExtAboutCvTermCvId: CFString](/documentation/imageio/kcgimagepropertyiptcextaboutcvtermcvid)
- [let kCGImagePropertyIPTCExtAboutCvTermId: CFString](/documentation/imageio/kcgimagepropertyiptcextaboutcvtermid)
- [let kCGImagePropertyIPTCExtAboutCvTermName: CFString](/documentation/imageio/kcgimagepropertyiptcextaboutcvtermname)
- [let kCGImagePropertyIPTCExtAboutCvTermRefinedAbout: CFString](/documentation/imageio/kcgimagepropertyiptcextaboutcvtermrefinedabout)
- [let kCGImagePropertyIPTCExtAddlModelInfo: CFString](/documentation/imageio/kcgimagepropertyiptcextaddlmodelinfo)
- [let kCGImagePropertyIPTCExtArtworkCircaDateCreated: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcircadatecreated)
- [let kCGImagePropertyIPTCExtArtworkContentDescription: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcontentdescription)
- [let kCGImagePropertyIPTCExtArtworkContributionDescription: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcontributiondescription)
- [let kCGImagePropertyIPTCExtArtworkCopyrightNotice: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcopyrightnotice)
- [let kCGImagePropertyIPTCExtArtworkCopyrightOwnerID: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcopyrightownerid)
- [let kCGImagePropertyIPTCExtArtworkCopyrightOwnerName: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcopyrightownername)
- [let kCGImagePropertyIPTCExtArtworkCreator: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcreator)
- [let kCGImagePropertyIPTCExtArtworkCreatorID: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkcreatorid)
- [let kCGImagePropertyIPTCExtArtworkDateCreated: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkdatecreated)
- [let kCGImagePropertyIPTCExtArtworkLicensorID: CFString](/documentation/imageio/kcgimagepropertyiptcextartworklicensorid)
- [let kCGImagePropertyIPTCExtArtworkLicensorName: CFString](/documentation/imageio/kcgimagepropertyiptcextartworklicensorname)
- [let kCGImagePropertyIPTCExtArtworkOrObject: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkorobject)
- [let kCGImagePropertyIPTCExtArtworkPhysicalDescription: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkphysicaldescription)
- [let kCGImagePropertyIPTCExtArtworkSource: CFString](/documentation/imageio/kcgimagepropertyiptcextartworksource)
- [let kCGImagePropertyIPTCExtArtworkSourceInvURL: CFString](/documentation/imageio/kcgimagepropertyiptcextartworksourceinvurl)
- [let kCGImagePropertyIPTCExtArtworkSourceInventoryNo: CFString](/documentation/imageio/kcgimagepropertyiptcextartworksourceinventoryno)
- [let kCGImagePropertyIPTCExtArtworkStylePeriod: CFString](/documentation/imageio/kcgimagepropertyiptcextartworkstyleperiod)
- [let kCGImagePropertyIPTCExtArtworkTitle: CFString](/documentation/imageio/kcgimagepropertyiptcextartworktitle)
- [let kCGImagePropertyIPTCExtAudioBitrate: CFString](/documentation/imageio/kcgimagepropertyiptcextaudiobitrate)
- [let kCGImagePropertyIPTCExtAudioBitrateMode: CFString](/documentation/imageio/kcgimagepropertyiptcextaudiobitratemode)
- [let kCGImagePropertyIPTCExtAudioChannelCount: CFString](/documentation/imageio/kcgimagepropertyiptcextaudiochannelcount)
- [let kCGImagePropertyIPTCExtCircaDateCreated: CFString](/documentation/imageio/kcgimagepropertyiptcextcircadatecreated)
- [let kCGImagePropertyIPTCExtContainerFormat: CFString](/documentation/imageio/kcgimagepropertyiptcextcontainerformat)
- [let kCGImagePropertyIPTCExtContainerFormatIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextcontainerformatidentifier)
- [let kCGImagePropertyIPTCExtContainerFormatName: CFString](/documentation/imageio/kcgimagepropertyiptcextcontainerformatname)
- [let kCGImagePropertyIPTCExtContributor: CFString](/documentation/imageio/kcgimagepropertyiptcextcontributor)
- [let kCGImagePropertyIPTCExtContributorIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextcontributoridentifier)
- [let kCGImagePropertyIPTCExtContributorName: CFString](/documentation/imageio/kcgimagepropertyiptcextcontributorname)
- [let kCGImagePropertyIPTCExtContributorRole: CFString](/documentation/imageio/kcgimagepropertyiptcextcontributorrole)
- [let kCGImagePropertyIPTCExtControlledVocabularyTerm: CFString](/documentation/imageio/kcgimagepropertyiptcextcontrolledvocabularyterm)
- [let kCGImagePropertyIPTCExtCopyrightYear: CFString](/documentation/imageio/kcgimagepropertyiptcextcopyrightyear)
- [let kCGImagePropertyIPTCExtCreator: CFString](/documentation/imageio/kcgimagepropertyiptcextcreator)
- [let kCGImagePropertyIPTCExtCreatorIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextcreatoridentifier)
- [let kCGImagePropertyIPTCExtCreatorName: CFString](/documentation/imageio/kcgimagepropertyiptcextcreatorname)
- [let kCGImagePropertyIPTCExtCreatorRole: CFString](/documentation/imageio/kcgimagepropertyiptcextcreatorrole)
- [let kCGImagePropertyIPTCExtDataOnScreen: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreen)
- [let kCGImagePropertyIPTCExtDataOnScreenRegion: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregion)
- [let kCGImagePropertyIPTCExtDataOnScreenRegionD: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregiond)
- [let kCGImagePropertyIPTCExtDataOnScreenRegionH: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregionh)
- [let kCGImagePropertyIPTCExtDataOnScreenRegionText: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregiontext)
- [let kCGImagePropertyIPTCExtDataOnScreenRegionUnit: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregionunit)
- [let kCGImagePropertyIPTCExtDataOnScreenRegionW: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregionw)
- [let kCGImagePropertyIPTCExtDataOnScreenRegionX: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregionx)
- [let kCGImagePropertyIPTCExtDataOnScreenRegionY: CFString](/documentation/imageio/kcgimagepropertyiptcextdataonscreenregiony)
- [let kCGImagePropertyIPTCExtDigitalImageGUID: CFString](/documentation/imageio/kcgimagepropertyiptcextdigitalimageguid)
- [let kCGImagePropertyIPTCExtDigitalSourceFileType: CFString](/documentation/imageio/kcgimagepropertyiptcextdigitalsourcefiletype)
- [let kCGImagePropertyIPTCExtDigitalSourceType: CFString](/documentation/imageio/kcgimagepropertyiptcextdigitalsourcetype)
- [let kCGImagePropertyIPTCExtDopesheet: CFString](/documentation/imageio/kcgimagepropertyiptcextdopesheet)
- [let kCGImagePropertyIPTCExtDopesheetLink: CFString](/documentation/imageio/kcgimagepropertyiptcextdopesheetlink)
- [let kCGImagePropertyIPTCExtDopesheetLinkLink: CFString](/documentation/imageio/kcgimagepropertyiptcextdopesheetlinklink)
- [let kCGImagePropertyIPTCExtDopesheetLinkLinkQualifier: CFString](/documentation/imageio/kcgimagepropertyiptcextdopesheetlinklinkqualifier)
- [let kCGImagePropertyIPTCExtEmbdEncRightsExpr: CFString](/documentation/imageio/kcgimagepropertyiptcextembdencrightsexpr)
- [let kCGImagePropertyIPTCExtEmbeddedEncodedRightsExpr: CFString](/documentation/imageio/kcgimagepropertyiptcextembeddedencodedrightsexpr)
- [let kCGImagePropertyIPTCExtEmbeddedEncodedRightsExprLangID: CFString](/documentation/imageio/kcgimagepropertyiptcextembeddedencodedrightsexprlangid)
- [let kCGImagePropertyIPTCExtEmbeddedEncodedRightsExprType: CFString](/documentation/imageio/kcgimagepropertyiptcextembeddedencodedrightsexprtype)
- [let kCGImagePropertyIPTCExtEpisode: CFString](/documentation/imageio/kcgimagepropertyiptcextepisode)
- [let kCGImagePropertyIPTCExtEpisodeIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextepisodeidentifier)
- [let kCGImagePropertyIPTCExtEpisodeName: CFString](/documentation/imageio/kcgimagepropertyiptcextepisodename)
- [let kCGImagePropertyIPTCExtEpisodeNumber: CFString](/documentation/imageio/kcgimagepropertyiptcextepisodenumber)
- [let kCGImagePropertyIPTCExtEvent: CFString](/documentation/imageio/kcgimagepropertyiptcextevent)
- [let kCGImagePropertyIPTCExtExternalMetadataLink: CFString](/documentation/imageio/kcgimagepropertyiptcextexternalmetadatalink)
- [let kCGImagePropertyIPTCExtFeedIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextfeedidentifier)
- [let kCGImagePropertyIPTCExtGenre: CFString](/documentation/imageio/kcgimagepropertyiptcextgenre)
- [let kCGImagePropertyIPTCExtGenreCvId: CFString](/documentation/imageio/kcgimagepropertyiptcextgenrecvid)
- [let kCGImagePropertyIPTCExtGenreCvTermId: CFString](/documentation/imageio/kcgimagepropertyiptcextgenrecvtermid)
- [let kCGImagePropertyIPTCExtGenreCvTermName: CFString](/documentation/imageio/kcgimagepropertyiptcextgenrecvtermname)
- [let kCGImagePropertyIPTCExtGenreCvTermRefinedAbout: CFString](/documentation/imageio/kcgimagepropertyiptcextgenrecvtermrefinedabout)
- [let kCGImagePropertyIPTCExtHeadline: CFString](/documentation/imageio/kcgimagepropertyiptcextheadline)
- [let kCGImagePropertyIPTCExtIPTCLastEdited: CFString](/documentation/imageio/kcgimagepropertyiptcextiptclastedited)
- [let kCGImagePropertyIPTCExtLinkedEncRightsExpr: CFString](/documentation/imageio/kcgimagepropertyiptcextlinkedencrightsexpr)
- [let kCGImagePropertyIPTCExtLinkedEncodedRightsExpr: CFString](/documentation/imageio/kcgimagepropertyiptcextlinkedencodedrightsexpr)
- [let kCGImagePropertyIPTCExtLinkedEncodedRightsExprLangID: CFString](/documentation/imageio/kcgimagepropertyiptcextlinkedencodedrightsexprlangid)
- [let kCGImagePropertyIPTCExtLinkedEncodedRightsExprType: CFString](/documentation/imageio/kcgimagepropertyiptcextlinkedencodedrightsexprtype)
- [let kCGImagePropertyIPTCExtLocationCity: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationcity)
- [let kCGImagePropertyIPTCExtLocationCountryCode: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationcountrycode)
- [let kCGImagePropertyIPTCExtLocationCountryName: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationcountryname)
- [let kCGImagePropertyIPTCExtLocationCreated: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationcreated)
- [let kCGImagePropertyIPTCExtLocationGPSAltitude: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationgpsaltitude)
- [let kCGImagePropertyIPTCExtLocationGPSLatitude: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationgpslatitude)
- [let kCGImagePropertyIPTCExtLocationGPSLongitude: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationgpslongitude)
- [let kCGImagePropertyIPTCExtLocationIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationidentifier)
- [let kCGImagePropertyIPTCExtLocationLocationId: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationlocationid)
- [let kCGImagePropertyIPTCExtLocationLocationName: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationlocationname)
- [let kCGImagePropertyIPTCExtLocationProvinceState: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationprovincestate)
- [let kCGImagePropertyIPTCExtLocationShown: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationshown)
- [let kCGImagePropertyIPTCExtLocationSublocation: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationsublocation)
- [let kCGImagePropertyIPTCExtLocationWorldRegion: CFString](/documentation/imageio/kcgimagepropertyiptcextlocationworldregion)
- [let kCGImagePropertyIPTCExtMaxAvailHeight: CFString](/documentation/imageio/kcgimagepropertyiptcextmaxavailheight)
- [let kCGImagePropertyIPTCExtMaxAvailWidth: CFString](/documentation/imageio/kcgimagepropertyiptcextmaxavailwidth)
- [let kCGImagePropertyIPTCExtModelAge: CFString](/documentation/imageio/kcgimagepropertyiptcextmodelage)
- [let kCGImagePropertyIPTCExtOrganisationInImageCode: CFString](/documentation/imageio/kcgimagepropertyiptcextorganisationinimagecode)
- [let kCGImagePropertyIPTCExtOrganisationInImageName: CFString](/documentation/imageio/kcgimagepropertyiptcextorganisationinimagename)
- [let kCGImagePropertyIPTCExtPersonHeard: CFString](/documentation/imageio/kcgimagepropertyiptcextpersonheard)
- [let kCGImagePropertyIPTCExtPersonHeardIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextpersonheardidentifier)
- [let kCGImagePropertyIPTCExtPersonHeardName: CFString](/documentation/imageio/kcgimagepropertyiptcextpersonheardname)
- [let kCGImagePropertyIPTCExtPersonInImage: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimage)
- [let kCGImagePropertyIPTCExtPersonInImageCharacteristic: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagecharacteristic)
- [let kCGImagePropertyIPTCExtPersonInImageCvTermCvId: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagecvtermcvid)
- [let kCGImagePropertyIPTCExtPersonInImageCvTermId: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagecvtermid)
- [let kCGImagePropertyIPTCExtPersonInImageCvTermName: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagecvtermname)
- [let kCGImagePropertyIPTCExtPersonInImageCvTermRefinedAbout: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagecvtermrefinedabout)
- [let kCGImagePropertyIPTCExtPersonInImageDescription: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagedescription)
- [let kCGImagePropertyIPTCExtPersonInImageId: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimageid)
- [let kCGImagePropertyIPTCExtPersonInImageName: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagename)
- [let kCGImagePropertyIPTCExtPersonInImageWDetails: CFString](/documentation/imageio/kcgimagepropertyiptcextpersoninimagewdetails)
- [let kCGImagePropertyIPTCExtProductInImage: CFString](/documentation/imageio/kcgimagepropertyiptcextproductinimage)
- [let kCGImagePropertyIPTCExtProductInImageDescription: CFString](/documentation/imageio/kcgimagepropertyiptcextproductinimagedescription)
- [let kCGImagePropertyIPTCExtProductInImageGTIN: CFString](/documentation/imageio/kcgimagepropertyiptcextproductinimagegtin)
- [let kCGImagePropertyIPTCExtProductInImageName: CFString](/documentation/imageio/kcgimagepropertyiptcextproductinimagename)
- [let kCGImagePropertyIPTCExtPublicationEvent: CFString](/documentation/imageio/kcgimagepropertyiptcextpublicationevent)
- [let kCGImagePropertyIPTCExtPublicationEventDate: CFString](/documentation/imageio/kcgimagepropertyiptcextpublicationeventdate)
- [let kCGImagePropertyIPTCExtPublicationEventIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextpublicationeventidentifier)
- [let kCGImagePropertyIPTCExtPublicationEventName: CFString](/documentation/imageio/kcgimagepropertyiptcextpublicationeventname)
- [let kCGImagePropertyIPTCExtRating: CFString](/documentation/imageio/kcgimagepropertyiptcextrating)
- [let kCGImagePropertyIPTCExtRatingRatingRegion: CFString](/documentation/imageio/kcgimagepropertyiptcextratingratingregion)
- [let kCGImagePropertyIPTCExtRatingRegionCity: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregioncity)
- [let kCGImagePropertyIPTCExtRatingRegionCountryCode: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregioncountrycode)
- [let kCGImagePropertyIPTCExtRatingRegionCountryName: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregioncountryname)
- [let kCGImagePropertyIPTCExtRatingRegionGPSAltitude: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregiongpsaltitude)
- [let kCGImagePropertyIPTCExtRatingRegionGPSLatitude: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregiongpslatitude)
- [let kCGImagePropertyIPTCExtRatingRegionGPSLongitude: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregiongpslongitude)
- [let kCGImagePropertyIPTCExtRatingRegionIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregionidentifier)
- [let kCGImagePropertyIPTCExtRatingRegionLocationId: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregionlocationid)
- [let kCGImagePropertyIPTCExtRatingRegionLocationName: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregionlocationname)
- [let kCGImagePropertyIPTCExtRatingRegionProvinceState: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregionprovincestate)
- [let kCGImagePropertyIPTCExtRatingRegionSublocation: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregionsublocation)
- [let kCGImagePropertyIPTCExtRatingRegionWorldRegion: CFString](/documentation/imageio/kcgimagepropertyiptcextratingregionworldregion)
- [let kCGImagePropertyIPTCExtRatingScaleMaxValue: CFString](/documentation/imageio/kcgimagepropertyiptcextratingscalemaxvalue)
- [let kCGImagePropertyIPTCExtRatingScaleMinValue: CFString](/documentation/imageio/kcgimagepropertyiptcextratingscaleminvalue)
- [let kCGImagePropertyIPTCExtRatingSourceLink: CFString](/documentation/imageio/kcgimagepropertyiptcextratingsourcelink)
- [let kCGImagePropertyIPTCExtRatingValue: CFString](/documentation/imageio/kcgimagepropertyiptcextratingvalue)
- [let kCGImagePropertyIPTCExtRatingValueLogoLink: CFString](/documentation/imageio/kcgimagepropertyiptcextratingvaluelogolink)
- [let kCGImagePropertyIPTCExtRegistryEntryRole: CFString](/documentation/imageio/kcgimagepropertyiptcextregistryentryrole)
- [let kCGImagePropertyIPTCExtRegistryID: CFString](/documentation/imageio/kcgimagepropertyiptcextregistryid)
- [let kCGImagePropertyIPTCExtRegistryItemID: CFString](/documentation/imageio/kcgimagepropertyiptcextregistryitemid)
- [let kCGImagePropertyIPTCExtRegistryOrganisationID: CFString](/documentation/imageio/kcgimagepropertyiptcextregistryorganisationid)
- [let kCGImagePropertyIPTCExtReleaseReady: CFString](/documentation/imageio/kcgimagepropertyiptcextreleaseready)
- [let kCGImagePropertyIPTCExtSeason: CFString](/documentation/imageio/kcgimagepropertyiptcextseason)
- [let kCGImagePropertyIPTCExtSeasonIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextseasonidentifier)
- [let kCGImagePropertyIPTCExtSeasonName: CFString](/documentation/imageio/kcgimagepropertyiptcextseasonname)
- [let kCGImagePropertyIPTCExtSeasonNumber: CFString](/documentation/imageio/kcgimagepropertyiptcextseasonnumber)
- [let kCGImagePropertyIPTCExtSeries: CFString](/documentation/imageio/kcgimagepropertyiptcextseries)
- [let kCGImagePropertyIPTCExtSeriesIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextseriesidentifier)
- [let kCGImagePropertyIPTCExtSeriesName: CFString](/documentation/imageio/kcgimagepropertyiptcextseriesname)
- [let kCGImagePropertyIPTCExtShownEvent: CFString](/documentation/imageio/kcgimagepropertyiptcextshownevent)
- [let kCGImagePropertyIPTCExtShownEventIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextshowneventidentifier)
- [let kCGImagePropertyIPTCExtShownEventName: CFString](/documentation/imageio/kcgimagepropertyiptcextshowneventname)
- [let kCGImagePropertyIPTCExtStorylineIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextstorylineidentifier)
- [let kCGImagePropertyIPTCExtStreamReady: CFString](/documentation/imageio/kcgimagepropertyiptcextstreamready)
- [let kCGImagePropertyIPTCExtStylePeriod: CFString](/documentation/imageio/kcgimagepropertyiptcextstyleperiod)
- [let kCGImagePropertyIPTCExtSupplyChainSource: CFString](/documentation/imageio/kcgimagepropertyiptcextsupplychainsource)
- [let kCGImagePropertyIPTCExtSupplyChainSourceIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextsupplychainsourceidentifier)
- [let kCGImagePropertyIPTCExtSupplyChainSourceName: CFString](/documentation/imageio/kcgimagepropertyiptcextsupplychainsourcename)
- [let kCGImagePropertyIPTCExtTemporalCoverage: CFString](/documentation/imageio/kcgimagepropertyiptcexttemporalcoverage)
- [let kCGImagePropertyIPTCExtTemporalCoverageFrom: CFString](/documentation/imageio/kcgimagepropertyiptcexttemporalcoveragefrom)
- [let kCGImagePropertyIPTCExtTemporalCoverageTo: CFString](/documentation/imageio/kcgimagepropertyiptcexttemporalcoverageto)
- [let kCGImagePropertyIPTCExtTranscript: CFString](/documentation/imageio/kcgimagepropertyiptcexttranscript)
- [let kCGImagePropertyIPTCExtTranscriptLink: CFString](/documentation/imageio/kcgimagepropertyiptcexttranscriptlink)
- [let kCGImagePropertyIPTCExtTranscriptLinkLink: CFString](/documentation/imageio/kcgimagepropertyiptcexttranscriptlinklink)
- [let kCGImagePropertyIPTCExtTranscriptLinkLinkQualifier: CFString](/documentation/imageio/kcgimagepropertyiptcexttranscriptlinklinkqualifier)
- [let kCGImagePropertyIPTCExtVideoBitrate: CFString](/documentation/imageio/kcgimagepropertyiptcextvideobitrate)
- [let kCGImagePropertyIPTCExtVideoBitrateMode: CFString](/documentation/imageio/kcgimagepropertyiptcextvideobitratemode)
- [let kCGImagePropertyIPTCExtVideoDisplayAspectRatio: CFString](/documentation/imageio/kcgimagepropertyiptcextvideodisplayaspectratio)
- [let kCGImagePropertyIPTCExtVideoEncodingProfile: CFString](/documentation/imageio/kcgimagepropertyiptcextvideoencodingprofile)
- [let kCGImagePropertyIPTCExtVideoShotType: CFString](/documentation/imageio/kcgimagepropertyiptcextvideoshottype)
- [let kCGImagePropertyIPTCExtVideoShotTypeIdentifier: CFString](/documentation/imageio/kcgimagepropertyiptcextvideoshottypeidentifier)
- [let kCGImagePropertyIPTCExtVideoShotTypeName: CFString](/documentation/imageio/kcgimagepropertyiptcextvideoshottypename)
- [let kCGImagePropertyIPTCExtVideoStreamsCount: CFString](/documentation/imageio/kcgimagepropertyiptcextvideostreamscount)
- [let kCGImagePropertyIPTCExtVisualColor: CFString](/documentation/imageio/kcgimagepropertyiptcextvisualcolor)
- [let kCGImagePropertyIPTCExtWorkflowTag: CFString](/documentation/imageio/kcgimagepropertyiptcextworkflowtag)
- [let kCGImagePropertyIPTCExtWorkflowTagCvId: CFString](/documentation/imageio/kcgimagepropertyiptcextworkflowtagcvid)
- [let kCGImagePropertyIPTCExtWorkflowTagCvTermId: CFString](/documentation/imageio/kcgimagepropertyiptcextworkflowtagcvtermid)
- [let kCGImagePropertyIPTCExtWorkflowTagCvTermName: CFString](/documentation/imageio/kcgimagepropertyiptcextworkflowtagcvtermname)
- [let kCGImagePropertyIPTCExtWorkflowTagCvTermRefinedAbout: CFString](/documentation/imageio/kcgimagepropertyiptcextworkflowtagcvtermrefinedabout)
- [let kCGImagePropertyIPTCContactInfoCity: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfocity)
- [let kCGImagePropertyIPTCContactInfoCountry: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfocountry)
- [let kCGImagePropertyIPTCContactInfoAddress: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfoaddress)
- [let kCGImagePropertyIPTCContactInfoPostalCode: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfopostalcode)
- [let kCGImagePropertyIPTCContactInfoStateProvince: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfostateprovince)
- [let kCGImagePropertyIPTCContactInfoEmails: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfoemails)
- [let kCGImagePropertyIPTCContactInfoPhones: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfophones)
- [let kCGImagePropertyIPTCContactInfoWebURLs: CFString](/documentation/imageio/kcgimagepropertyiptccontactinfoweburls)

### Location Data

- [let kCGImagePropertyIPTCCity: CFString](/documentation/imageio/kcgimagepropertyiptccity)
- [let kCGImagePropertyIPTCSubLocation: CFString](/documentation/imageio/kcgimagepropertyiptcsublocation)
- [let kCGImagePropertyIPTCProvinceState: CFString](/documentation/imageio/kcgimagepropertyiptcprovincestate)
- [let kCGImagePropertyIPTCCountryPrimaryLocationCode: CFString](/documentation/imageio/kcgimagepropertyiptccountryprimarylocationcode)
- [let kCGImagePropertyIPTCCountryPrimaryLocationName: CFString](/documentation/imageio/kcgimagepropertyiptccountryprimarylocationname)
- [let kCGImagePropertyIPTCOriginalTransmissionReference: CFString](/documentation/imageio/kcgimagepropertyiptcoriginaltransmissionreference)

### Software Program

- [let kCGImagePropertyIPTCOriginatingProgram: CFString](/documentation/imageio/kcgimagepropertyiptcoriginatingprogram)
- [let kCGImagePropertyIPTCProgramVersion: CFString](/documentation/imageio/kcgimagepropertyiptcprogramversion)

### Object Details

- [let kCGImagePropertyIPTCObjectTypeReference: CFString](/documentation/imageio/kcgimagepropertyiptcobjecttypereference)
- [let kCGImagePropertyIPTCObjectAttributeReference: CFString](/documentation/imageio/kcgimagepropertyiptcobjectattributereference)
- [let kCGImagePropertyIPTCObjectName: CFString](/documentation/imageio/kcgimagepropertyiptcobjectname)

### IPTC Extension

- [let kCGImageMetadataNamespaceIPTCExtension: CFString](/documentation/imageio/kcgimagemetadatanamespaceiptcextension)
- [let kCGImageMetadataPrefixIPTCExtension: CFString](/documentation/imageio/kcgimagemetadataprefixiptcextension)
- [GPS Dictionary Keys](/documentation/imageio/gps-dictionary-keys)

### Dictionary

- [let kCGImagePropertyGPSDictionary: CFString](/documentation/imageio/kcgimagepropertygpsdictionary)

### GPS Coordinate

- [let kCGImagePropertyGPSLatitude: CFString](/documentation/imageio/kcgimagepropertygpslatitude)
- [let kCGImagePropertyGPSLongitude: CFString](/documentation/imageio/kcgimagepropertygpslongitude)
- [let kCGImagePropertyGPSAltitude: CFString](/documentation/imageio/kcgimagepropertygpsaltitude)
- [let kCGImagePropertyGPSLatitudeRef: CFString](/documentation/imageio/kcgimagepropertygpslatituderef)
- [let kCGImagePropertyGPSLongitudeRef: CFString](/documentation/imageio/kcgimagepropertygpslongituderef)
- [let kCGImagePropertyGPSAltitudeRef: CFString](/documentation/imageio/kcgimagepropertygpsaltituderef)
- [let kCGImagePropertyGPSHPositioningError: CFString](/documentation/imageio/kcgimagepropertygpshpositioningerror)

### Destinations

- [let kCGImagePropertyGPSDestLatitude: CFString](/documentation/imageio/kcgimagepropertygpsdestlatitude)
- [let kCGImagePropertyGPSDestLongitude: CFString](/documentation/imageio/kcgimagepropertygpsdestlongitude)
- [let kCGImagePropertyGPSDestBearing: CFString](/documentation/imageio/kcgimagepropertygpsdestbearing)
- [let kCGImagePropertyGPSDestDistance: CFString](/documentation/imageio/kcgimagepropertygpsdestdistance)
- [let kCGImagePropertyGPSDestLatitudeRef: CFString](/documentation/imageio/kcgimagepropertygpsdestlatituderef)
- [let kCGImagePropertyGPSDestLongitudeRef: CFString](/documentation/imageio/kcgimagepropertygpsdestlongituderef)
- [let kCGImagePropertyGPSDestBearingRef: CFString](/documentation/imageio/kcgimagepropertygpsdestbearingref)
- [let kCGImagePropertyGPSDestDistanceRef: CFString](/documentation/imageio/kcgimagepropertygpsdestdistanceref)

### Image Orientation

- [let kCGImagePropertyGPSImgDirectionRef: CFString](/documentation/imageio/kcgimagepropertygpsimgdirectionref)
- [let kCGImagePropertyGPSImgDirection: CFString](/documentation/imageio/kcgimagepropertygpsimgdirection)

### Measurement Details

- [let kCGImagePropertyGPSStatus: CFString](/documentation/imageio/kcgimagepropertygpsstatus)
- [let kCGImagePropertyGPSSatellites: CFString](/documentation/imageio/kcgimagepropertygpssatellites)
- [let kCGImagePropertyGPSMeasureMode: CFString](/documentation/imageio/kcgimagepropertygpsmeasuremode)
- [let kCGImagePropertyGPSDOP: CFString](/documentation/imageio/kcgimagepropertygpsdop)
- [let kCGImagePropertyGPSSpeedRef: CFString](/documentation/imageio/kcgimagepropertygpsspeedref)
- [let kCGImagePropertyGPSSpeed: CFString](/documentation/imageio/kcgimagepropertygpsspeed)
- [let kCGImagePropertyGPSTrackRef: CFString](/documentation/imageio/kcgimagepropertygpstrackref)
- [let kCGImagePropertyGPSTrack: CFString](/documentation/imageio/kcgimagepropertygpstrack)
- [let kCGImagePropertyGPSMapDatum: CFString](/documentation/imageio/kcgimagepropertygpsmapdatum)
- [let kCGImagePropertyGPSProcessingMethod: CFString](/documentation/imageio/kcgimagepropertygpsprocessingmethod)
- [let kCGImagePropertyGPSAreaInformation: CFString](/documentation/imageio/kcgimagepropertygpsareainformation)
- [let kCGImagePropertyGPSDifferental: CFString](/documentation/imageio/kcgimagepropertygpsdifferental)

### Timestamp Information

- [let kCGImagePropertyGPSTimeStamp: CFString](/documentation/imageio/kcgimagepropertygpstimestamp)
- [let kCGImagePropertyGPSDateStamp: CFString](/documentation/imageio/kcgimagepropertygpsdatestamp)

### GPS Version

- [let kCGImagePropertyGPSVersion: CFString](/documentation/imageio/kcgimagepropertygpsversion)
- [WebP Data](/documentation/imageio/webp-data)

### Dictionary

- [let kCGImagePropertyWebPDictionary: CFString](/documentation/imageio/kcgimagepropertywebpdictionary)

### Image Properties

- [let kCGImagePropertyWebPCanvasPixelHeight: CFString](/documentation/imageio/kcgimagepropertywebpcanvaspixelheight)
- [let kCGImagePropertyWebPCanvasPixelWidth: CFString](/documentation/imageio/kcgimagepropertywebpcanvaspixelwidth)

### Sequence Timing

- [let kCGImagePropertyWebPFrameInfoArray: CFString](/documentation/imageio/kcgimagepropertywebpframeinfoarray)
- [let kCGImagePropertyWebPDelayTime: CFString](/documentation/imageio/kcgimagepropertywebpdelaytime)
- [let kCGImagePropertyWebPUnclampedDelayTime: CFString](/documentation/imageio/kcgimagepropertywebpunclampeddelaytime)
- [let kCGImagePropertyWebPLoopCount: CFString](/documentation/imageio/kcgimagepropertywebploopcount)

## Format-Specific Properties

- [CIFF Image Properties](/documentation/imageio/ciff-image-properties)

### Dictionary

- [let kCGImagePropertyCIFFDictionary: CFString](/documentation/imageio/kcgimagepropertyciffdictionary)

### Image Details

- [let kCGImagePropertyCIFFDescription: CFString](/documentation/imageio/kcgimagepropertyciffdescription)
- [let kCGImagePropertyCIFFImageName: CFString](/documentation/imageio/kcgimagepropertyciffimagename)
- [let kCGImagePropertyCIFFImageFileName: CFString](/documentation/imageio/kcgimagepropertyciffimagefilename)
- [let kCGImagePropertyCIFFImageSerialNumber: CFString](/documentation/imageio/kcgimagepropertyciffimageserialnumber)

### Exposure

- [let kCGImagePropertyCIFFWhiteBalanceIndex: CFString](/documentation/imageio/kcgimagepropertyciffwhitebalanceindex)
- [let kCGImagePropertyCIFFFlashExposureComp: CFString](/documentation/imageio/kcgimagepropertyciffflashexposurecomp)
- [let kCGImagePropertyCIFFMeasuredEV: CFString](/documentation/imageio/kcgimagepropertyciffmeasuredev)
- [let kCGImagePropertyCIFFMeteringMode: CFString](/documentation/imageio/kcgimagepropertyciffmeteringmode)

### Shutter Information

- [let kCGImagePropertyCIFFReleaseTiming: CFString](/documentation/imageio/kcgimagepropertyciffreleasetiming)
- [let kCGImagePropertyCIFFSelfTimingTime: CFString](/documentation/imageio/kcgimagepropertyciffselftimingtime)
- [let kCGImagePropertyCIFFReleaseMethod: CFString](/documentation/imageio/kcgimagepropertyciffreleasemethod)
- [let kCGImagePropertyCIFFContinuousDrive: CFString](/documentation/imageio/kcgimagepropertyciffcontinuousdrive)
- [let kCGImagePropertyCIFFShootingMode: CFString](/documentation/imageio/kcgimagepropertyciffshootingmode)

### Lens and Focus

- [let kCGImagePropertyCIFFFocusMode: CFString](/documentation/imageio/kcgimagepropertycifffocusmode)
- [let kCGImagePropertyCIFFLensMaxMM: CFString](/documentation/imageio/kcgimagepropertycifflensmaxmm)
- [let kCGImagePropertyCIFFLensMinMM: CFString](/documentation/imageio/kcgimagepropertycifflensminmm)
- [let kCGImagePropertyCIFFLensModel: CFString](/documentation/imageio/kcgimagepropertycifflensmodel)

### Camera Information

- [let kCGImagePropertyCIFFFirmware: CFString](/documentation/imageio/kcgimagepropertycifffirmware)
- [let kCGImagePropertyCIFFOwnerName: CFString](/documentation/imageio/kcgimagepropertyciffownername)
- [let kCGImagePropertyCIFFCameraSerialNumber: CFString](/documentation/imageio/kcgimagepropertyciffcameraserialnumber)
- [let kCGImagePropertyCIFFRecordID: CFString](/documentation/imageio/kcgimagepropertyciffrecordid)
- [DNG Image Properties](/documentation/imageio/dng-image-properties)

### Dictionary

- [let kCGImagePropertyDNGDictionary: CFString](/documentation/imageio/kcgimagepropertydngdictionary)

### Quality

- [let kCGImagePropertyDNGBaselineSharpness: CFString](/documentation/imageio/kcgimagepropertydngbaselinesharpness)
- [let kCGImagePropertyDNGLinearResponseLimit: CFString](/documentation/imageio/kcgimagepropertydnglinearresponselimit)
- [let kCGImagePropertyDNGChromaBlurRadius: CFString](/documentation/imageio/kcgimagepropertydngchromablurradius)
- [let kCGImagePropertyDNGAntiAliasStrength: CFString](/documentation/imageio/kcgimagepropertydngantialiasstrength)
- [let kCGImagePropertyDNGShadowScale: CFString](/documentation/imageio/kcgimagepropertydngshadowscale)
- [let kCGImagePropertyDNGBestQualityScale: CFString](/documentation/imageio/kcgimagepropertydngbestqualityscale)
- [let kCGImagePropertyDNGDefaultScale: CFString](/documentation/imageio/kcgimagepropertydngdefaultscale)
- [let kCGImagePropertyDNGLinearizationTable: CFString](/documentation/imageio/kcgimagepropertydnglinearizationtable)

### Exposure

- [let kCGImagePropertyDNGBaselineExposure: CFString](/documentation/imageio/kcgimagepropertydngbaselineexposure)
- [let kCGImagePropertyDNGBaselineNoise: CFString](/documentation/imageio/kcgimagepropertydngbaselinenoise)
- [let kCGImagePropertyDNGBaselineExposureOffset: CFString](/documentation/imageio/kcgimagepropertydngbaselineexposureoffset)

### Color Balance

- [let kCGImagePropertyDNGAnalogBalance: CFString](/documentation/imageio/kcgimagepropertydnganalogbalance)
- [let kCGImagePropertyDNGAsShotNeutral: CFString](/documentation/imageio/kcgimagepropertydngasshotneutral)
- [let kCGImagePropertyDNGAsShotWhiteXY: CFString](/documentation/imageio/kcgimagepropertydngasshotwhitexy)
- [let kCGImagePropertyDNGBayerGreenSplit: CFString](/documentation/imageio/kcgimagepropertydngbayergreensplit)
- [let kCGImagePropertyDNGForwardMatrix1: CFString](/documentation/imageio/kcgimagepropertydngforwardmatrix1)
- [let kCGImagePropertyDNGForwardMatrix2: CFString](/documentation/imageio/kcgimagepropertydngforwardmatrix2)
- [let kCGImagePropertyDNGDefaultBlackRender: CFString](/documentation/imageio/kcgimagepropertydngdefaultblackrender)

### Color Calibration

- [let kCGImagePropertyDNGBlackLevelRepeatDim: CFString](/documentation/imageio/kcgimagepropertydngblacklevelrepeatdim)
- [let kCGImagePropertyDNGBlackLevel: CFString](/documentation/imageio/kcgimagepropertydngblacklevel)
- [let kCGImagePropertyDNGBlackLevelDeltaH: CFString](/documentation/imageio/kcgimagepropertydngblackleveldeltah)
- [let kCGImagePropertyDNGBlackLevelDeltaV: CFString](/documentation/imageio/kcgimagepropertydngblackleveldeltav)
- [let kCGImagePropertyDNGWhiteLevel: CFString](/documentation/imageio/kcgimagepropertydngwhitelevel)
- [let kCGImagePropertyDNGCalibrationIlluminant1: CFString](/documentation/imageio/kcgimagepropertydngcalibrationilluminant1)
- [let kCGImagePropertyDNGCalibrationIlluminant2: CFString](/documentation/imageio/kcgimagepropertydngcalibrationilluminant2)
- [let kCGImagePropertyDNGColorMatrix1: CFString](/documentation/imageio/kcgimagepropertydngcolormatrix1)
- [let kCGImagePropertyDNGColorMatrix2: CFString](/documentation/imageio/kcgimagepropertydngcolormatrix2)
- [let kCGImagePropertyDNGCameraCalibration1: CFString](/documentation/imageio/kcgimagepropertydngcameracalibration1)
- [let kCGImagePropertyDNGCameraCalibration2: CFString](/documentation/imageio/kcgimagepropertydngcameracalibration2)
- [let kCGImagePropertyDNGReductionMatrix1: CFString](/documentation/imageio/kcgimagepropertydngreductionmatrix1)
- [let kCGImagePropertyDNGReductionMatrix2: CFString](/documentation/imageio/kcgimagepropertydngreductionmatrix2)
- [let kCGImagePropertyDNGAsShotICCProfile: CFString](/documentation/imageio/kcgimagepropertydngasshoticcprofile)
- [let kCGImagePropertyDNGAsShotPreProfileMatrix: CFString](/documentation/imageio/kcgimagepropertydngasshotpreprofilematrix)
- [let kCGImagePropertyDNGCurrentICCProfile: CFString](/documentation/imageio/kcgimagepropertydngcurrenticcprofile)
- [let kCGImagePropertyDNGCurrentPreProfileMatrix: CFString](/documentation/imageio/kcgimagepropertydngcurrentpreprofilematrix)
- [let kCGImagePropertyDNGColorimetricReference: CFString](/documentation/imageio/kcgimagepropertydngcolorimetricreference)
- [let kCGImagePropertyDNGCameraCalibrationSignature: CFString](/documentation/imageio/kcgimagepropertydngcameracalibrationsignature)
- [let kCGImagePropertyDNGProfileCalibrationSignature: CFString](/documentation/imageio/kcgimagepropertydngprofilecalibrationsignature)

### Crop Data

- [let kCGImagePropertyDNGActiveArea: CFString](/documentation/imageio/kcgimagepropertydngactivearea)
- [let kCGImagePropertyDNGMaskedAreas: CFString](/documentation/imageio/kcgimagepropertydngmaskedareas)
- [let kCGImagePropertyDNGDefaultCropOrigin: CFString](/documentation/imageio/kcgimagepropertydngdefaultcroporigin)
- [let kCGImagePropertyDNGDefaultCropSize: CFString](/documentation/imageio/kcgimagepropertydngdefaultcropsize)
- [let kCGImagePropertyDNGDefaultUserCrop: CFString](/documentation/imageio/kcgimagepropertydngdefaultusercrop)

### RAW Data

- [let kCGImagePropertyDNGOriginalRawFileName: CFString](/documentation/imageio/kcgimagepropertydngoriginalrawfilename)
- [let kCGImagePropertyDNGOriginalRawFileData: CFString](/documentation/imageio/kcgimagepropertydngoriginalrawfiledata)
- [let kCGImagePropertyDNGNoiseReductionApplied: CFString](/documentation/imageio/kcgimagepropertydngnoisereductionapplied)
- [let kCGImagePropertyDNGNewRawImageDigest: CFString](/documentation/imageio/kcgimagepropertydngnewrawimagedigest)
- [let kCGImagePropertyDNGOriginalRawFileDigest: CFString](/documentation/imageio/kcgimagepropertydngoriginalrawfiledigest)
- [let kCGImagePropertyDNGRawImageDigest: CFString](/documentation/imageio/kcgimagepropertydngrawimagedigest)
- [let kCGImagePropertyDNGOriginalDefaultFinalSize: CFString](/documentation/imageio/kcgimagepropertydngoriginaldefaultfinalsize)
- [let kCGImagePropertyDNGOriginalBestQualityFinalSize: CFString](/documentation/imageio/kcgimagepropertydngoriginalbestqualityfinalsize)
- [let kCGImagePropertyDNGOriginalDefaultCropSize: CFString](/documentation/imageio/kcgimagepropertydngoriginaldefaultcropsize)
- [let kCGImagePropertyDNGRawToPreviewGain: CFString](/documentation/imageio/kcgimagepropertydngrawtopreviewgain)
- [let kCGImagePropertyDNGNoiseProfile: CFString](/documentation/imageio/kcgimagepropertydngnoiseprofile)
- [let kCGImagePropertyDNGCFALayout: CFString](/documentation/imageio/kcgimagepropertydngcfalayout)
- [let kCGImagePropertyDNGCFAPlaneColor: CFString](/documentation/imageio/kcgimagepropertydngcfaplanecolor)
- [let kCGImagePropertyDNGOpcodeList1: CFString](/documentation/imageio/kcgimagepropertydngopcodelist1)
- [let kCGImagePropertyDNGOpcodeList2: CFString](/documentation/imageio/kcgimagepropertydngopcodelist2)
- [let kCGImagePropertyDNGOpcodeList3: CFString](/documentation/imageio/kcgimagepropertydngopcodelist3)
- [let kCGImagePropertyDNGWarpRectilinear: CFString](/documentation/imageio/kcgimagepropertydngwarprectilinear)
- [let kCGImagePropertyDNGWarpFisheye: CFString](/documentation/imageio/kcgimagepropertydngwarpfisheye)
- [let kCGImagePropertyDNGFixVignetteRadial: CFString](/documentation/imageio/kcgimagepropertydngfixvignetteradial)

### Image File Data

- [let kCGImagePropertyDNGPrivateData: CFString](/documentation/imageio/kcgimagepropertydngprivatedata)
- [let kCGImagePropertyDNGMakerNoteSafety: CFString](/documentation/imageio/kcgimagepropertydngmakernotesafety)
- [let kCGImagePropertyDNGRawDataUniqueID: CFString](/documentation/imageio/kcgimagepropertydngrawdatauniqueid)
- [let kCGImagePropertyDNGSubTileBlockSize: CFString](/documentation/imageio/kcgimagepropertydngsubtileblocksize)
- [let kCGImagePropertyDNGRowInterleaveFactor: CFString](/documentation/imageio/kcgimagepropertydngrowinterleavefactor)
- [let kCGImagePropertyDNGBackwardVersion: CFString](/documentation/imageio/kcgimagepropertydngbackwardversion)
- [let kCGImagePropertyDNGVersion: CFString](/documentation/imageio/kcgimagepropertydngversion)

### Profile Data

- [let kCGImagePropertyDNGExtraCameraProfiles: CFString](/documentation/imageio/kcgimagepropertydngextracameraprofiles)
- [let kCGImagePropertyDNGAsShotProfileName: CFString](/documentation/imageio/kcgimagepropertydngasshotprofilename)
- [let kCGImagePropertyDNGProfileHueSatMapDims: CFString](/documentation/imageio/kcgimagepropertydngprofilehuesatmapdims)
- [let kCGImagePropertyDNGProfileHueSatMapData1: CFString](/documentation/imageio/kcgimagepropertydngprofilehuesatmapdata1)
- [let kCGImagePropertyDNGProfileHueSatMapData2: CFString](/documentation/imageio/kcgimagepropertydngprofilehuesatmapdata2)
- [let kCGImagePropertyDNGProfileHueSatMapEncoding: CFString](/documentation/imageio/kcgimagepropertydngprofilehuesatmapencoding)
- [let kCGImagePropertyDNGProfileToneCurve: CFString](/documentation/imageio/kcgimagepropertydngprofiletonecurve)
- [let kCGImagePropertyDNGProfileName: CFString](/documentation/imageio/kcgimagepropertydngprofilename)
- [let kCGImagePropertyDNGProfileEmbedPolicy: CFString](/documentation/imageio/kcgimagepropertydngprofileembedpolicy)
- [let kCGImagePropertyDNGProfileCopyright: CFString](/documentation/imageio/kcgimagepropertydngprofilecopyright)
- [let kCGImagePropertyDNGProfileLookTableDims: CFString](/documentation/imageio/kcgimagepropertydngprofilelooktabledims)
- [let kCGImagePropertyDNGProfileLookTableData: CFString](/documentation/imageio/kcgimagepropertydngprofilelooktabledata)
- [let kCGImagePropertyDNGProfileLookTableEncoding: CFString](/documentation/imageio/kcgimagepropertydngprofilelooktableencoding)

### Preview

- [let kCGImagePropertyDNGPreviewApplicationName: CFString](/documentation/imageio/kcgimagepropertydngpreviewapplicationname)
- [let kCGImagePropertyDNGPreviewApplicationVersion: CFString](/documentation/imageio/kcgimagepropertydngpreviewapplicationversion)
- [let kCGImagePropertyDNGPreviewSettingsName: CFString](/documentation/imageio/kcgimagepropertydngpreviewsettingsname)
- [let kCGImagePropertyDNGPreviewSettingsDigest: CFString](/documentation/imageio/kcgimagepropertydngpreviewsettingsdigest)
- [let kCGImagePropertyDNGPreviewColorSpace: CFString](/documentation/imageio/kcgimagepropertydngpreviewcolorspace)
- [let kCGImagePropertyDNGPreviewDateTime: CFString](/documentation/imageio/kcgimagepropertydngpreviewdatetime)

### Camera Details

- [let kCGImagePropertyDNGLensInfo: CFString](/documentation/imageio/kcgimagepropertydnglensinfo)
- [let kCGImagePropertyDNGUniqueCameraModel: CFString](/documentation/imageio/kcgimagepropertydnguniquecameramodel)
- [let kCGImagePropertyDNGLocalizedCameraModel: CFString](/documentation/imageio/kcgimagepropertydnglocalizedcameramodel)
- [let kCGImagePropertyDNGCameraSerialNumber: CFString](/documentation/imageio/kcgimagepropertydngcameraserialnumber)
- [GIF Image Properties](/documentation/imageio/gif-image-properties)

### Dictionary

- [let kCGImagePropertyGIFDictionary: CFString](/documentation/imageio/kcgimagepropertygifdictionary)

### Image Properties

- [let kCGImagePropertyGIFCanvasPixelHeight: CFString](/documentation/imageio/kcgimagepropertygifcanvaspixelheight)
- [let kCGImagePropertyGIFCanvasPixelWidth: CFString](/documentation/imageio/kcgimagepropertygifcanvaspixelwidth)
- [let kCGImagePropertyGIFHasGlobalColorMap: CFString](/documentation/imageio/kcgimagepropertygifhasglobalcolormap)
- [let kCGImagePropertyGIFImageColorMap: CFString](/documentation/imageio/kcgimagepropertygifimagecolormap)

### Sequence Timing

- [let kCGImagePropertyGIFFrameInfoArray: CFString](/documentation/imageio/kcgimagepropertygifframeinfoarray)
- [let kCGImagePropertyGIFDelayTime: CFString](/documentation/imageio/kcgimagepropertygifdelaytime)
- [let kCGImagePropertyGIFUnclampedDelayTime: CFString](/documentation/imageio/kcgimagepropertygifunclampeddelaytime)
- [let kCGImagePropertyGIFLoopCount: CFString](/documentation/imageio/kcgimagepropertygifloopcount)
- [HEIC Image Properties](/documentation/imageio/heic-image-properties)

### Dictionary

- [let kCGImagePropertyHEICSDictionary: CFString](/documentation/imageio/kcgimagepropertyheicsdictionary)

### Image Properties

- [let kCGImagePropertyHEICSCanvasPixelHeight: CFString](/documentation/imageio/kcgimagepropertyheicscanvaspixelheight)
- [let kCGImagePropertyHEICSCanvasPixelWidth: CFString](/documentation/imageio/kcgimagepropertyheicscanvaspixelwidth)
- [let kCGImagePropertyNamedColorSpace: CFString](/documentation/imageio/kcgimagepropertynamedcolorspace)

### Sequence Timing

- [let kCGImagePropertyHEICSFrameInfoArray: CFString](/documentation/imageio/kcgimagepropertyheicsframeinfoarray)
- [let kCGImagePropertyHEICSDelayTime: CFString](/documentation/imageio/kcgimagepropertyheicsdelaytime)
- [let kCGImagePropertyHEICSUnclampedDelayTime: CFString](/documentation/imageio/kcgimagepropertyheicsunclampeddelaytime)
- [let kCGImagePropertyHEICSLoopCount: CFString](/documentation/imageio/kcgimagepropertyheicsloopcount)
- [JFIF Image Properties](/documentation/imageio/jfif-image-properties)

### Dictionary

- [let kCGImagePropertyJFIFDictionary: CFString](/documentation/imageio/kcgimagepropertyjfifdictionary)

### Quality Information

- [let kCGImagePropertyJFIFXDensity: CFString](/documentation/imageio/kcgimagepropertyjfifxdensity)
- [let kCGImagePropertyJFIFYDensity: CFString](/documentation/imageio/kcgimagepropertyjfifydensity)
- [let kCGImagePropertyJFIFDensityUnit: CFString](/documentation/imageio/kcgimagepropertyjfifdensityunit)
- [let kCGImagePropertyJFIFIsProgressive: CFString](/documentation/imageio/kcgimagepropertyjfifisprogressive)

### Version Information

- [let kCGImagePropertyJFIFVersion: CFString](/documentation/imageio/kcgimagepropertyjfifversion)
- [PNG Image Properties](/documentation/imageio/png-image-properties)

### Dictionary

- [let kCGImagePropertyPNGDictionary: CFString](/documentation/imageio/kcgimagepropertypngdictionary)

### Properties

- [let kCGImagePropertyPNGSource: CFString](/documentation/imageio/kcgimagepropertypngsource)

### Image Properties

- [let kCGImagePropertyAPNGCanvasPixelHeight: CFString](/documentation/imageio/kcgimagepropertyapngcanvaspixelheight)
- [let kCGImagePropertyAPNGCanvasPixelWidth: CFString](/documentation/imageio/kcgimagepropertyapngcanvaspixelwidth)
- [let kCGImagePropertyPNGXPixelsPerMeter: CFString](/documentation/imageio/kcgimagepropertypngxpixelspermeter)
- [let kCGImagePropertyPNGYPixelsPerMeter: CFString](/documentation/imageio/kcgimagepropertypngypixelspermeter)
- [let kCGImagePropertyPNGGamma: CFString](/documentation/imageio/kcgimagepropertypnggamma)
- [let kCGImagePropertyPNGInterlaceType: CFString](/documentation/imageio/kcgimagepropertypnginterlacetype)
- [let kCGImagePropertyPNGsRGBIntent: CFString](/documentation/imageio/kcgimagepropertypngsrgbintent)
- [let kCGImagePropertyPNGChromaticities: CFString](/documentation/imageio/kcgimagepropertypngchromaticities)

### Sequence Timing

- [let kCGImagePropertyAPNGFrameInfoArray: CFString](/documentation/imageio/kcgimagepropertyapngframeinfoarray)
- [let kCGImagePropertyAPNGDelayTime: CFString](/documentation/imageio/kcgimagepropertyapngdelaytime)
- [let kCGImagePropertyAPNGUnclampedDelayTime: CFString](/documentation/imageio/kcgimagepropertyapngunclampeddelaytime)
- [let kCGImagePropertyAPNGLoopCount: CFString](/documentation/imageio/kcgimagepropertyapngloopcount)

### Descriptive Information

- [let kCGImagePropertyPNGTitle: CFString](/documentation/imageio/kcgimagepropertypngtitle)
- [let kCGImagePropertyPNGDescription: CFString](/documentation/imageio/kcgimagepropertypngdescription)
- [let kCGImagePropertyPNGComment: CFString](/documentation/imageio/kcgimagepropertypngcomment)
- [let kCGImagePropertyPNGDisclaimer: CFString](/documentation/imageio/kcgimagepropertypngdisclaimer)
- [let kCGImagePropertyPNGWarning: CFString](/documentation/imageio/kcgimagepropertypngwarning)
- [let kCGImagePropertyPNGAuthor: CFString](/documentation/imageio/kcgimagepropertypngauthor)
- [let kCGImagePropertyPNGCopyright: CFString](/documentation/imageio/kcgimagepropertypngcopyright)
- [let kCGImagePropertyPNGCreationTime: CFString](/documentation/imageio/kcgimagepropertypngcreationtime)
- [let kCGImagePropertyPNGModificationTime: CFString](/documentation/imageio/kcgimagepropertypngmodificationtime)
- [let kCGImagePropertyPNGSoftware: CFString](/documentation/imageio/kcgimagepropertypngsoftware)

### Pre-Compression Filters

- [let kCGImagePropertyPNGCompressionFilter: CFString](/documentation/imageio/kcgimagepropertypngcompressionfilter)
- [var IMAGEIO_PNG_NO_FILTERS: Int32](/documentation/imageio/imageio_png_no_filters)
- [var IMAGEIO_PNG_FILTER_NONE: Int32](/documentation/imageio/imageio_png_filter_none)
- [var IMAGEIO_PNG_FILTER_SUB: Int32](/documentation/imageio/imageio_png_filter_sub)
- [var IMAGEIO_PNG_FILTER_UP: Int32](/documentation/imageio/imageio_png_filter_up)
- [var IMAGEIO_PNG_FILTER_AVG: Int32](/documentation/imageio/imageio_png_filter_avg)
- [var IMAGEIO_PNG_FILTER_PAETH: Int32](/documentation/imageio/imageio_png_filter_paeth)
- [TGA Image Properties](/documentation/imageio/tga-image-properties)

### Dictionary Key

- [let kCGImagePropertyTGADictionary: CFString](/documentation/imageio/kcgimagepropertytgadictionary)

### Compression

- [let kCGImagePropertyTGACompression: CFString](/documentation/imageio/kcgimagepropertytgacompression)
- [CGImagePropertyTGACompression](/documentation/imageio/cgimagepropertytgacompression)

#### Compression Options

- [case tgaCompressionNone](/documentation/imageio/cgimagepropertytgacompression/tgacompressionnone)
- [case tgaCompressionRLE](/documentation/imageio/cgimagepropertytgacompression/tgacompressionrle)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/imageio/cgimagepropertytgacompression/init(rawvalue:))
- [TIFF Image Properties](/documentation/imageio/tiff-image-properties)

### Dictionary

- [let kCGImagePropertyTIFFDictionary: CFString](/documentation/imageio/kcgimagepropertytiffdictionary)

### Image Quality

- [let kCGImagePropertyTIFFCompression: CFString](/documentation/imageio/kcgimagepropertytiffcompression)
- [let kCGImagePropertyTIFFPhotometricInterpretation: CFString](/documentation/imageio/kcgimagepropertytiffphotometricinterpretation)
- [let kCGImagePropertyTIFFTransferFunction: CFString](/documentation/imageio/kcgimagepropertytifftransferfunction)

### Canvas Details

- [let kCGImagePropertyTIFFOrientation: CFString](/documentation/imageio/kcgimagepropertytifforientation)
- [let kCGImagePropertyTIFFXResolution: CFString](/documentation/imageio/kcgimagepropertytiffxresolution)
- [let kCGImagePropertyTIFFYResolution: CFString](/documentation/imageio/kcgimagepropertytiffyresolution)
- [let kCGImagePropertyTIFFResolutionUnit: CFString](/documentation/imageio/kcgimagepropertytiffresolutionunit)
- [let kCGImagePropertyTIFFWhitePoint: CFString](/documentation/imageio/kcgimagepropertytiffwhitepoint)
- [let kCGImagePropertyTIFFPrimaryChromaticities: CFString](/documentation/imageio/kcgimagepropertytiffprimarychromaticities)
- [let kCGImagePropertyTIFFTileLength: CFString](/documentation/imageio/kcgimagepropertytifftilelength)
- [let kCGImagePropertyTIFFTileWidth: CFString](/documentation/imageio/kcgimagepropertytifftilewidth)

### Descriptive Information

- [let kCGImagePropertyTIFFDocumentName: CFString](/documentation/imageio/kcgimagepropertytiffdocumentname)
- [let kCGImagePropertyTIFFImageDescription: CFString](/documentation/imageio/kcgimagepropertytiffimagedescription)
- [let kCGImagePropertyTIFFArtist: CFString](/documentation/imageio/kcgimagepropertytiffartist)
- [let kCGImagePropertyTIFFCopyright: CFString](/documentation/imageio/kcgimagepropertytiffcopyright)
- [let kCGImagePropertyTIFFDateTime: CFString](/documentation/imageio/kcgimagepropertytiffdatetime)
- [let kCGImagePropertyTIFFMake: CFString](/documentation/imageio/kcgimagepropertytiffmake)
- [let kCGImagePropertyTIFFModel: CFString](/documentation/imageio/kcgimagepropertytiffmodel)
- [let kCGImagePropertyTIFFSoftware: CFString](/documentation/imageio/kcgimagepropertytiffsoftware)
- [let kCGImagePropertyTIFFHostComputer: CFString](/documentation/imageio/kcgimagepropertytiffhostcomputer)
- [8BIM Image Properties](/documentation/imageio/8bim-image-properties)

### Dictionary

- [let kCGImageProperty8BIMDictionary: CFString](/documentation/imageio/kcgimageproperty8bimdictionary)

### File Information

- [let kCGImageProperty8BIMLayerNames: CFString](/documentation/imageio/kcgimageproperty8bimlayernames)
- [let kCGImageProperty8BIMVersion: CFString](/documentation/imageio/kcgimageproperty8bimversion)

## Manufacturer-Specific Properties

- [Nikon Camera Dictionary Keys](/documentation/imageio/nikon-camera-dictionary-keys)

### Dictionary

- [let kCGImagePropertyMakerNikonDictionary: CFString](/documentation/imageio/kcgimagepropertymakernikondictionary)

### Program Settings

- [let kCGImagePropertyMakerNikonISOSetting: CFString](/documentation/imageio/kcgimagepropertymakernikonisosetting)
- [let kCGImagePropertyMakerNikonISOSelection: CFString](/documentation/imageio/kcgimagepropertymakernikonisoselection)
- [let kCGImagePropertyMakerNikonColorMode: CFString](/documentation/imageio/kcgimagepropertymakernikoncolormode)
- [let kCGImagePropertyMakerNikonQuality: CFString](/documentation/imageio/kcgimagepropertymakernikonquality)
- [let kCGImagePropertyMakerNikonWhiteBalanceMode: CFString](/documentation/imageio/kcgimagepropertymakernikonwhitebalancemode)
- [let kCGImagePropertyMakerNikonSharpenMode: CFString](/documentation/imageio/kcgimagepropertymakernikonsharpenmode)
- [let kCGImagePropertyMakerNikonFocusMode: CFString](/documentation/imageio/kcgimagepropertymakernikonfocusmode)
- [let kCGImagePropertyMakerNikonFlashSetting: CFString](/documentation/imageio/kcgimagepropertymakernikonflashsetting)
- [let kCGImagePropertyMakerNikonImageAdjustment: CFString](/documentation/imageio/kcgimagepropertymakernikonimageadjustment)
- [let kCGImagePropertyMakerNikonShootingMode: CFString](/documentation/imageio/kcgimagepropertymakernikonshootingmode)
- [let kCGImagePropertyMakerNikonDigitalZoom: CFString](/documentation/imageio/kcgimagepropertymakernikondigitalzoom)
- [let kCGImagePropertyMakerNikonShutterCount: CFString](/documentation/imageio/kcgimagepropertymakernikonshuttercount)
- [let kCGImagePropertyMakerNikonFlashExposureComp: CFString](/documentation/imageio/kcgimagepropertymakernikonflashexposurecomp)
- [let kCGImagePropertyMakerNikonFocusDistance: CFString](/documentation/imageio/kcgimagepropertymakernikonfocusdistance)

### Camera Details

- [let kCGImagePropertyMakerNikonLensAdapter: CFString](/documentation/imageio/kcgimagepropertymakernikonlensadapter)
- [let kCGImagePropertyMakerNikonLensType: CFString](/documentation/imageio/kcgimagepropertymakernikonlenstype)
- [let kCGImagePropertyMakerNikonLensInfo: CFString](/documentation/imageio/kcgimagepropertymakernikonlensinfo)
- [let kCGImagePropertyMakerNikonCameraSerialNumber: CFString](/documentation/imageio/kcgimagepropertymakernikoncameraserialnumber)
- [Canon Camera Dictionary Keys](/documentation/imageio/canon-camera-dictionary-keys)

### Dictionary

- [let kCGImagePropertyMakerCanonDictionary: CFString](/documentation/imageio/kcgimagepropertymakercanondictionary)

### Program Settings

- [let kCGImagePropertyMakerCanonFlashExposureComp: CFString](/documentation/imageio/kcgimagepropertymakercanonflashexposurecomp)
- [let kCGImagePropertyMakerCanonContinuousDrive: CFString](/documentation/imageio/kcgimagepropertymakercanoncontinuousdrive)
- [let kCGImagePropertyMakerCanonAspectRatioInfo: CFString](/documentation/imageio/kcgimagepropertymakercanonaspectratioinfo)

### Camera Details

- [let kCGImagePropertyMakerCanonOwnerName: CFString](/documentation/imageio/kcgimagepropertymakercanonownername)
- [let kCGImagePropertyMakerCanonCameraSerialNumber: CFString](/documentation/imageio/kcgimagepropertymakercanoncameraserialnumber)
- [let kCGImagePropertyMakerCanonImageSerialNumber: CFString](/documentation/imageio/kcgimagepropertymakercanonimageserialnumber)
- [let kCGImagePropertyMakerCanonLensModel: CFString](/documentation/imageio/kcgimagepropertymakercanonlensmodel)
- [let kCGImagePropertyMakerCanonFirmware: CFString](/documentation/imageio/kcgimagepropertymakercanonfirmware)
- [let kCGImagePropertyMakerAppleDictionary: CFString](/documentation/imageio/kcgimagepropertymakerappledictionary)
- [let kCGImagePropertyMakerMinoltaDictionary: CFString](/documentation/imageio/kcgimagepropertymakerminoltadictionary)
- [let kCGImagePropertyMakerFujiDictionary: CFString](/documentation/imageio/kcgimagepropertymakerfujidictionary)
- [let kCGImagePropertyMakerOlympusDictionary: CFString](/documentation/imageio/kcgimagepropertymakerolympusdictionary)
- [let kCGImagePropertyMakerPentaxDictionary: CFString](/documentation/imageio/kcgimagepropertymakerpentaxdictionary)
- [let kCGImagePropertyRawDictionary: CFString](/documentation/imageio/kcgimagepropertyrawdictionary)

## Spatial Photos

- [Writing spatial photos](/documentation/imageio/writing-spatial-photos)
- [Creating spatial photos and videos with spatial metadata](/documentation/imageio/creating-spatial-photos-and-videos-with-spatial-metadata)

## Animations

- [func CGAnimateImageAtURLWithBlock(CFURL, CFDictionary?, CGImageSourceAnimationBlock) -> OSStatus](/documentation/imageio/cganimateimageaturlwithblock(_:_:_:))
- [func CGAnimateImageDataWithBlock(CFData, CFDictionary?, CGImageSourceAnimationBlock) -> OSStatus](/documentation/imageio/cganimateimagedatawithblock(_:_:_:))
- [CGImageSourceAnimationBlock](/documentation/imageio/cgimagesourceanimationblock)
- [let kCGImageAnimationStartIndex: CFString](/documentation/imageio/kcgimageanimationstartindex)
- [let kCGImageAnimationDelayTime: CFString](/documentation/imageio/kcgimageanimationdelaytime)
- [let kCGImageAnimationLoopCount: CFString](/documentation/imageio/kcgimageanimationloopcount)
- [CGImageAnimationStatus](/documentation/imageio/cgimageanimationstatus)

### Animation Status

- [case allocationFailure](/documentation/imageio/cgimageanimationstatus/allocationfailure)
- [case corruptInputImage](/documentation/imageio/cgimageanimationstatus/corruptinputimage)
- [case incompleteInputImage](/documentation/imageio/cgimageanimationstatus/incompleteinputimage)
- [case parameterError](/documentation/imageio/cgimageanimationstatus/parametererror)
- [case unsupportedFormat](/documentation/imageio/cgimageanimationstatus/unsupportedformat)

### Initializers

- [init?(rawValue: OSStatus)](/documentation/imageio/cgimageanimationstatus/init(rawvalue:))

## Reference

- [Image I/O Constants](/documentation/imageio/image-i-o-constants)

### Constants

- [let kCGImageAuxiliaryDataInfoColorSpace: CFString](/documentation/imageio/kcgimageauxiliarydatainfocolorspace)
- [let kCGImageAuxiliaryDataTypeISOGainMap: CFString](/documentation/imageio/kcgimageauxiliarydatatypeisogainmap)
- [let kCGImagePropertyGroupMonoscopicImageLocation: CFString](/documentation/imageio/kcgimagepropertygroupmonoscopicimagelocation)
- [let kCGImagePropertyAVISDictionary: CFString](/documentation/imageio/kcgimagepropertyavisdictionary)
- [let kCGImagePropertyGroupImageBaseline: CFString](/documentation/imageio/kcgimagepropertygroupimagebaseline)
- [let kCGImagePropertyGroupImageDisparityAdjustment: CFString](/documentation/imageio/kcgimagepropertygroupimagedisparityadjustment)
- [let kCGImagePropertyGroupImageIndexLeft: CFString](/documentation/imageio/kcgimagepropertygroupimageindexleft)
- [let kCGImagePropertyGroupImageIndexRight: CFString](/documentation/imageio/kcgimagepropertygroupimageindexright)
- [let kCGImagePropertyGroupImageIndexMonoscopic: CFString](/documentation/imageio/kcgimagepropertygroupimageindexmonoscopic)
- [let kCGImagePropertyGroupImageIsAlternateImage: CFString](/documentation/imageio/kcgimagepropertygroupimageisalternateimage)
- [let kCGImagePropertyGroupImageIsLeftImage: CFString](/documentation/imageio/kcgimagepropertygroupimageisleftimage)
- [let kCGImagePropertyGroupImageIsRightImage: CFString](/documentation/imageio/kcgimagepropertygroupimageisrightimage)
- [let kCGImagePropertyGroupImageIsMonoscopicImage: CFString](/documentation/imageio/kcgimagepropertygroupimageismonoscopicimage)
- [let kCGImagePropertyGroupImageStereoAggressors: CFString](/documentation/imageio/kcgimagepropertygroupimagestereoaggressors)
- [let kCGImagePropertyGroupImagesAlternate: CFString](/documentation/imageio/kcgimagepropertygroupimagesalternate)
- [let kCGImagePropertyGroupIndex: CFString](/documentation/imageio/kcgimagepropertygroupindex)
- [let kCGImagePropertyGroupType: CFString](/documentation/imageio/kcgimagepropertygrouptype)
- [let kCGImagePropertyGroupTypeAlternate: CFString](/documentation/imageio/kcgimagepropertygrouptypealternate)
- [let kCGImagePropertyGroupTypeStereoPair: CFString](/documentation/imageio/kcgimagepropertygrouptypestereopair)
- [let kCGImagePropertyGroups: CFString](/documentation/imageio/kcgimagepropertygroups)
- [let kCGImagePropertyHEIFDictionary: CFString](/documentation/imageio/kcgimagepropertyheifdictionary)
- [let kCGImagePropertyImageIndex: CFString](/documentation/imageio/kcgimagepropertyimageindex)
- [let kCGImagePropertyPNGPixelsAspectRatio: CFString](/documentation/imageio/kcgimagepropertypngpixelsaspectratio)
- [let kCGImagePropertyPNGTransparency: CFString](/documentation/imageio/kcgimagepropertypngtransparency)
- [let kCGImagePropertyTIFFXPosition: CFString](/documentation/imageio/kcgimagepropertytiffxposition)
- [let kCGImagePropertyTIFFYPosition: CFString](/documentation/imageio/kcgimagepropertytiffyposition)
- [let kCGImageSourceDecodeRequest: CFString](/documentation/imageio/kcgimagesourcedecoderequest)
- [let kCGImageSourceDecodeRequestOptions: CFString](/documentation/imageio/kcgimagesourcedecoderequestoptions)
- [let kCGImageSourceDecodeToHDR: CFString](/documentation/imageio/kcgimagesourcedecodetohdr)
- [let kCGImageSourceDecodeToSDR: CFString](/documentation/imageio/kcgimagesourcedecodetosdr)
- [let kIIOCameraExtrinsics_CoordinateSystemID: CFString](/documentation/imageio/kiiocameraextrinsics_coordinatesystemid)
- [let kIIOCameraExtrinsics_Position: CFString](/documentation/imageio/kiiocameraextrinsics_position)
- [let kIIOCameraExtrinsics_Rotation: CFString](/documentation/imageio/kiiocameraextrinsics_rotation)
- [let kIIOCameraModelType_GenericPinhole: CFString](/documentation/imageio/kiiocameramodeltype_genericpinhole)
- [let kIIOCameraModelType_SimplifiedPinhole: CFString](/documentation/imageio/kiiocameramodeltype_simplifiedpinhole)
- [let kIIOCameraModel_Intrinsics: CFString](/documentation/imageio/kiiocameramodel_intrinsics)
- [let kIIOCameraModel_ModelType: CFString](/documentation/imageio/kiiocameramodel_modeltype)
- [let kIIOMetadata_CameraExtrinsicsKey: CFString](/documentation/imageio/kiiometadata_cameraextrinsicskey)
- [let kIIOMetadata_CameraModelKey: CFString](/documentation/imageio/kiiometadata_cameramodelkey)
- [let kIIOMonoscopicImageLocation_Center: CFString](/documentation/imageio/kiiomonoscopicimagelocation_center)
- [let kIIOMonoscopicImageLocation_Left: CFString](/documentation/imageio/kiiomonoscopicimagelocation_left)
- [let kIIOMonoscopicImageLocation_Right: CFString](/documentation/imageio/kiiomonoscopicimagelocation_right)
- [let kIIOMonoscopicImageLocation_Unspecified: CFString](/documentation/imageio/kiiomonoscopicimagelocation_unspecified)
- [let kIIOStereoAggressors_Severity: CFString](/documentation/imageio/kiiostereoaggressors_severity)
- [let kIIOStereoAggressors_SubTypeURI: CFString](/documentation/imageio/kiiostereoaggressors_subtypeuri)
- [let kIIOStereoAggressors_Type: CFString](/documentation/imageio/kiiostereoaggressors_type)
- [Image I/O Functions](/documentation/imageio/image-i-o-functions)

### Functions

- [func CGImageDestinationAddImageAndMetadata(CGImageDestination, CGImage, CGImageMetadata?, CFDictionary?)](/documentation/imageio/cgimagedestinationaddimageandmetadata(_:_:_:_:))
- [func CGImageDestinationCopyImageSource(CGImageDestination, CGImageSource, CFDictionary?, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/imageio/cgimagedestinationcopyimagesource(_:_:_:_:))
- [func CGImageSourceCopyMetadataAtIndex(CGImageSource, Int, CFDictionary?) -> CGImageMetadata?](/documentation/imageio/cgimagesourcecopymetadataatindex(_:_:_:))
- [func CGImageSourceRemoveCacheAtIndex(CGImageSource, Int)](/documentation/imageio/cgimagesourceremovecacheatindex(_:_:))
- [func CGImageSourceSetAllowableTypes(CFArray) -> OSStatus](/documentation/imageio/cgimagesourcesetallowabletypes(_:))
- [Image I/O Macros](/documentation/imageio/image-i-o-macros)

### Macros

- [var IIO_HAS_IOSURFACE: Int32](/documentation/imageio/iio_has_iosurface)

## Variables

- [let kCGComputeHDRStats: CFString](/documentation/imageio/kcgcomputehdrstats)
- [let kCGImageDestinationEncodeAlternateColorSpace: CFString](/documentation/imageio/kcgimagedestinationencodealternatecolorspace)
- [let kCGImageDestinationEncodeBaseColorSpace: CFString](/documentation/imageio/kcgimagedestinationencodebasecolorspace)
- [let kCGImageDestinationEncodeBaseIsSDR: CFString](/documentation/imageio/kcgimagedestinationencodebaseissdr)
- [let kCGImageDestinationEncodeBasePixelFormatRequest: CFString](/documentation/imageio/kcgimagedestinationencodebasepixelformatrequest)
- [let kCGImageDestinationEncodeGainMapPixelFormatRequest: CFString](/documentation/imageio/kcgimagedestinationencodegainmappixelformatrequest)
- [let kCGImageDestinationEncodeGainMapSubsampleFactor: CFString](/documentation/imageio/kcgimagedestinationencodegainmapsubsamplefactor)
- [let kCGImageDestinationEncodeGenerateGainMapWithBaseImage: CFString](/documentation/imageio/kcgimagedestinationencodegenerategainmapwithbaseimage)
- [let kCGImageDestinationEncodeIsBaseImage: CFString](/documentation/imageio/kcgimagedestinationencodeisbaseimage)
- [let kCGImageDestinationEncodeRequest: CFString](/documentation/imageio/kcgimagedestinationencoderequest)
- [let kCGImageDestinationEncodeRequestOptions: CFString](/documentation/imageio/kcgimagedestinationencoderequestoptions)
- [let kCGImageDestinationEncodeToISOGainmap: CFString](/documentation/imageio/kcgimagedestinationencodetoisogainmap)
- [let kCGImageDestinationEncodeToISOHDR: CFString](/documentation/imageio/kcgimagedestinationencodetoisohdr)
- [let kCGImageDestinationEncodeToSDR: CFString](/documentation/imageio/kcgimagedestinationencodetosdr)
- [let kCGImageDestinationEncodeTonemapMode: CFString](/documentation/imageio/kcgimagedestinationencodetonemapmode)
- [let kCGImagePropertyASTCBlockSize: CFString](/documentation/imageio/kcgimagepropertyastcblocksize)
- [let kCGImagePropertyASTCBlockSize4x4: CFString](/documentation/imageio/kcgimagepropertyastcblocksize4x4)
- [let kCGImagePropertyASTCBlockSize8x8: CFString](/documentation/imageio/kcgimagepropertyastcblocksize8x8)
- [let kCGImagePropertyASTCEncoder: CFString](/documentation/imageio/kcgimagepropertyastcencoder)
- [let kCGImagePropertyBCEncoder: CFString](/documentation/imageio/kcgimagepropertybcencoder)
- [let kCGImagePropertyBCFormat: CFString](/documentation/imageio/kcgimagepropertybcformat)
- [let kCGImagePropertyEncoder: CFString](/documentation/imageio/kcgimagepropertyencoder)
- [let kCGImagePropertyOpenEXRCompression: CFString](/documentation/imageio/kcgimagepropertyopenexrcompression)
- [let kCGImagePropertyPVREncoder: CFString](/documentation/imageio/kcgimagepropertypvrencoder)
- [let kCGImageProviderPreferredTileHeight: CFString](/documentation/imageio/kcgimageproviderpreferredtileheight)
- [let kCGImageProviderPreferredTileWidth: CFString](/documentation/imageio/kcgimageproviderpreferredtilewidth)
- [let kCGImageSourceGenerateImageSpecificLumaScaling: CFString](/documentation/imageio/kcgimagesourcegenerateimagespecificlumascaling)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
