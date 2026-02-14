# Assets Library Documentation

Source: https://sosumi.ai/documentation/assetslibrary

---
title: Assets Library
source: https://developer.apple.com/documentation/assetslibrary
timestamp: 2026-02-13T18:53:54.460Z
---

## Classes

- [ALAsset](/documentation/assetslibrary/alasset)

### Asset Properties

- [func value(forProperty: String!) -> Any!](/documentation/assetslibrary/alasset/value(forproperty:))
- [var isEditable: Bool](/documentation/assetslibrary/alasset/iseditable)
- [var original: ALAsset!](/documentation/assetslibrary/alasset/original)

### Accessing Representations

- [func defaultRepresentation() -> ALAssetRepresentation!](/documentation/assetslibrary/alasset/defaultrepresentation())
- [func representation(forUTI: String!) -> ALAssetRepresentation!](/documentation/assetslibrary/alasset/representation(foruti:))
- [func thumbnail() -> Unmanaged<CGImage>!](/documentation/assetslibrary/alasset/thumbnail())
- [func aspectRatioThumbnail() -> Unmanaged<CGImage>!](/documentation/assetslibrary/alasset/aspectratiothumbnail())

### Setting New Image and Video Data

- [func setImageData(Data!, metadata: [AnyHashable : Any]!, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alasset/setimagedata(_:metadata:completionblock:))
- [func setVideoAtPath(URL!, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alasset/setvideoatpath(_:completionblock:))

### Saving to the Saved Photos Album

- [func writeModifiedImageData(toSavedPhotosAlbum: Data!, metadata: [AnyHashable : Any]!, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alasset/writemodifiedimagedata(tosavedphotosalbum:metadata:completionblock:))
- [func writeModifiedVideoAtPath(toSavedPhotosAlbum: URL!, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alasset/writemodifiedvideoatpath(tosavedphotosalbum:completionblock:))

### Constants

- [Property Keys](/documentation/assetslibrary/property-keys)

#### Constants

- [let ALAssetPropertyType: String](/documentation/assetslibrary/alassetpropertytype)
- [let ALAssetPropertyLocation: String](/documentation/assetslibrary/alassetpropertylocation)
- [let ALAssetPropertyDuration: String](/documentation/assetslibrary/alassetpropertyduration)
- [let ALAssetPropertyOrientation: String](/documentation/assetslibrary/alassetpropertyorientation)
- [let ALAssetPropertyDate: String](/documentation/assetslibrary/alassetpropertydate)
- [let ALAssetPropertyRepresentations: String](/documentation/assetslibrary/alassetpropertyrepresentations)
- [let ALAssetPropertyURLs: String](/documentation/assetslibrary/alassetpropertyurls)
- [let ALAssetPropertyAssetURL: String](/documentation/assetslibrary/alassetpropertyasseturl)
- [Invalid Property Value](/documentation/assetslibrary/invalid-property-value)

#### Constants

- [let ALErrorInvalidProperty: String](/documentation/assetslibrary/alerrorinvalidproperty)
- [Asset Types](/documentation/assetslibrary/asset-types)

#### Constants

- [let ALAssetTypePhoto: String](/documentation/assetslibrary/alassettypephoto)
- [let ALAssetTypeVideo: String](/documentation/assetslibrary/alassettypevideo)
- [let ALAssetTypeUnknown: String](/documentation/assetslibrary/alassettypeunknown)
- [ALAssetRepresentation](/documentation/assetslibrary/alassetrepresentation)

### Getting Image Representations

- [func cgImage(options: [AnyHashable : Any]!) -> Unmanaged<CGImage>!](/documentation/assetslibrary/alassetrepresentation/cgimage(options:))
- [func fullResolutionImage() -> Unmanaged<CGImage>!](/documentation/assetslibrary/alassetrepresentation/fullresolutionimage())
- [func fullScreenImage() -> Unmanaged<CGImage>!](/documentation/assetslibrary/alassetrepresentation/fullscreenimage())

### Getting Image Attributes

- [func orientation() -> ALAssetOrientation](/documentation/assetslibrary/alassetrepresentation/orientation())
- [func scale() -> Float](/documentation/assetslibrary/alassetrepresentation/scale())
- [func dimensions() -> CGSize](/documentation/assetslibrary/alassetrepresentation/dimensions())
- [func filename() -> String!](/documentation/assetslibrary/alassetrepresentation/filename())

### Getting Raw Data

- [func size() -> Int64](/documentation/assetslibrary/alassetrepresentation/size())
- [func getBytes(UnsafeMutablePointer<UInt8>!, fromOffset: Int64, length: Int, error: NSErrorPointer) -> Int](/documentation/assetslibrary/alassetrepresentation/getbytes(_:fromoffset:length:error:))

### Getting Metadata

- [func uti() -> String!](/documentation/assetslibrary/alassetrepresentation/uti())
- [func metadata() -> [AnyHashable : Any]!](/documentation/assetslibrary/alassetrepresentation/metadata())

### Getting an URL

- [func url() -> URL!](/documentation/assetslibrary/alassetrepresentation/url())
- [ALAssetsFilter](/documentation/assetslibrary/alassetsfilter)

### Creating Filters

- [class func allAssets() -> ALAssetsFilter!](/documentation/assetslibrary/alassetsfilter/allassets())
- [class func allPhotos() -> ALAssetsFilter!](/documentation/assetslibrary/alassetsfilter/allphotos())
- [class func allVideos() -> ALAssetsFilter!](/documentation/assetslibrary/alassetsfilter/allvideos())
- [ALAssetsGroup](/documentation/assetslibrary/alassetsgroup)

### Enumerating Assets

- [func enumerateAssets(ALAssetsGroupEnumerationResultsBlock!)](/documentation/assetslibrary/alassetsgroup/enumerateassets(_:))
- [func enumerateAssets(options: NSEnumerationOptions, using: ALAssetsGroupEnumerationResultsBlock!)](/documentation/assetslibrary/alassetsgroup/enumerateassets(options:using:))
- [func enumerateAssets(at: IndexSet!, options: NSEnumerationOptions, using: ALAssetsGroupEnumerationResultsBlock!)](/documentation/assetslibrary/alassetsgroup/enumerateassets(at:options:using:))

### Adding Assets

- [func add(ALAsset!) -> Bool](/documentation/assetslibrary/alassetsgroup/add(_:))
- [var isEditable: Bool](/documentation/assetslibrary/alassetsgroup/iseditable)

### Filtering

- [func numberOfAssets() -> Int](/documentation/assetslibrary/alassetsgroup/numberofassets())
- [func setAssetsFilter(ALAssetsFilter!)](/documentation/assetslibrary/alassetsgroup/setassetsfilter(_:))

### Accessing Properties

- [func value(forProperty: String!) -> Any!](/documentation/assetslibrary/alassetsgroup/value(forproperty:))
- [func posterImage() -> Unmanaged<CGImage>!](/documentation/assetslibrary/alassetsgroup/posterimage())

### Constants

- [ALAssetsGroupEnumerationResultsBlock](/documentation/assetslibrary/alassetsgroupenumerationresultsblock)
- [Group Property Names](/documentation/assetslibrary/group-property-names)

#### Constants

- [let ALAssetsGroupPropertyName: String](/documentation/assetslibrary/alassetsgrouppropertyname)
- [let ALAssetsGroupPropertyType: String](/documentation/assetslibrary/alassetsgrouppropertytype)
- [let ALAssetsGroupPropertyPersistentID: String](/documentation/assetslibrary/alassetsgrouppropertypersistentid)
- [let ALAssetsGroupPropertyURL: String](/documentation/assetslibrary/alassetsgrouppropertyurl)
- [ALAssetsLibrary](/documentation/assetslibrary/alassetslibrary)

### Accessing Assets

- [class func authorizationStatus() -> ALAuthorizationStatus](/documentation/assetslibrary/alassetslibrary/authorizationstatus())

### Managing Notifications

- [class func disableSharedPhotoStreamsSupport()](/documentation/assetslibrary/alassetslibrary/disablesharedphotostreamssupport())

### Finding Assets

- [func asset(for: URL!, resultBlock: ALAssetsLibraryAssetForURLResultBlock!, failureBlock: ALAssetsLibraryAccessFailureBlock!)](/documentation/assetslibrary/alassetslibrary/asset(for:resultblock:failureblock:))

### Enumerating Assets

- [func enumerateGroups(withTypes: ALAssetsGroupType, using: ALAssetsLibraryGroupsEnumerationResultsBlock!, failureBlock: ALAssetsLibraryAccessFailureBlock!)](/documentation/assetslibrary/alassetslibrary/enumerategroups(withtypes:using:failureblock:))

### Saving Assets

- [func writeVideoAtPath(toSavedPhotosAlbum: URL!, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alassetslibrary/writevideoatpath(tosavedphotosalbum:completionblock:))
- [func videoAtPathIs(compatibleWithSavedPhotosAlbum: URL!) -> Bool](/documentation/assetslibrary/alassetslibrary/videoatpathis(compatiblewithsavedphotosalbum:))
- [func writeImage(toSavedPhotosAlbum: CGImage!, orientation: ALAssetOrientation, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alassetslibrary/writeimage(tosavedphotosalbum:orientation:completionblock:))
- [func writeImageData(toSavedPhotosAlbum: Data!, metadata: [AnyHashable : Any]!, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alassetslibrary/writeimagedata(tosavedphotosalbum:metadata:completionblock:))
- [func writeImage(toSavedPhotosAlbum: CGImage!, metadata: [AnyHashable : Any]!, completionBlock: ((URL?, (any Error)?) -> Void)!)](/documentation/assetslibrary/alassetslibrary/writeimage(tosavedphotosalbum:metadata:completionblock:))

### Managing Asset Groups

- [func addAssetsGroupAlbum(withName: String!, resultBlock: ALAssetsLibraryGroupResultBlock!, failureBlock: ALAssetsLibraryAccessFailureBlock!)](/documentation/assetslibrary/alassetslibrary/addassetsgroupalbum(withname:resultblock:failureblock:))
- [func group(for: URL!, resultBlock: ALAssetsLibraryGroupResultBlock!, failureBlock: ALAssetsLibraryAccessFailureBlock!)](/documentation/assetslibrary/alassetslibrary/group(for:resultblock:failureblock:))

### Constants

- [ALAssetsGroupType](/documentation/assetslibrary/alassetsgrouptype)
- [Types of Asset](/documentation/assetslibrary/types-of-asset)

#### Constants

- [var ALAssetsGroupLibrary: UInt32](/documentation/assetslibrary/alassetsgrouplibrary)
- [var ALAssetsGroupAlbum: UInt32](/documentation/assetslibrary/alassetsgroupalbum)
- [var ALAssetsGroupEvent: UInt32](/documentation/assetslibrary/alassetsgroupevent)
- [var ALAssetsGroupFaces: UInt32](/documentation/assetslibrary/alassetsgroupfaces)
- [var ALAssetsGroupSavedPhotos: UInt32](/documentation/assetslibrary/alassetsgroupsavedphotos)
- [var ALAssetsGroupPhotoStream: UInt32](/documentation/assetslibrary/alassetsgroupphotostream)
- [var ALAssetsGroupAll: UInt32](/documentation/assetslibrary/alassetsgroupall)
- [ALAssetOrientation](/documentation/assetslibrary/alassetorientation)

#### Constants

- [case up](/documentation/assetslibrary/alassetorientation/up)
- [case down](/documentation/assetslibrary/alassetorientation/down)
- [case left](/documentation/assetslibrary/alassetorientation/left)
- [case right](/documentation/assetslibrary/alassetorientation/right)
- [case upMirrored](/documentation/assetslibrary/alassetorientation/upmirrored)
- [case downMirrored](/documentation/assetslibrary/alassetorientation/downmirrored)
- [case leftMirrored](/documentation/assetslibrary/alassetorientation/leftmirrored)
- [case rightMirrored](/documentation/assetslibrary/alassetorientation/rightmirrored)

#### Initializers

- [init?(rawValue: Int)](/documentation/assetslibrary/alassetorientation/init(rawvalue:))
- [ALAssetsLibraryGroupsEnumerationResultsBlock](/documentation/assetslibrary/alassetslibrarygroupsenumerationresultsblock)
- [ALAssetsLibraryAssetForURLResultBlock](/documentation/assetslibrary/alassetslibraryassetforurlresultblock)
- [ALAssetsLibraryWriteImageCompletionBlock](/documentation/assetslibrary/alassetslibrarywriteimagecompletionblock)
- [ALAssetsLibraryWriteVideoCompletionBlock](/documentation/assetslibrary/alassetslibrarywritevideocompletionblock)
- [ALAssetsLibraryAccessFailureBlock](/documentation/assetslibrary/alassetslibraryaccessfailureblock)
- [ALAssetsLibraryGroupResultBlock](/documentation/assetslibrary/alassetslibrarygroupresultblock)
- [ALAuthorizationStatus](/documentation/assetslibrary/alauthorizationstatus)

#### Constants

- [case notDetermined](/documentation/assetslibrary/alauthorizationstatus/notdetermined)
- [case restricted](/documentation/assetslibrary/alauthorizationstatus/restricted)
- [case denied](/documentation/assetslibrary/alauthorizationstatus/denied)
- [case authorized](/documentation/assetslibrary/alauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/assetslibrary/alauthorizationstatus/init(rawvalue:))
- [Notification Keys](/documentation/assetslibrary/notification-keys)

#### Constants

- [let ALAssetLibraryUpdatedAssetsKey: String](/documentation/assetslibrary/alassetlibraryupdatedassetskey)
- [let ALAssetLibraryInsertedAssetGroupsKey: String](/documentation/assetslibrary/alassetlibraryinsertedassetgroupskey)
- [let ALAssetLibraryUpdatedAssetGroupsKey: String](/documentation/assetslibrary/alassetlibraryupdatedassetgroupskey)
- [let ALAssetLibraryDeletedAssetGroupsKey: String](/documentation/assetslibrary/alassetlibrarydeletedassetgroupskey)
- [Error Domain](/documentation/assetslibrary/error-domain)

#### Constants

- [let ALAssetsLibraryErrorDomain: String](/documentation/assetslibrary/alassetslibraryerrordomain)
- [Error Codes](/documentation/assetslibrary/error-codes)

#### Constants

- [var ALAssetsLibraryUnknownError: Int](/documentation/assetslibrary/alassetslibraryunknownerror)
- [var ALAssetsLibraryWriteFailedError: Int](/documentation/assetslibrary/alassetslibrarywritefailederror)
- [var ALAssetsLibraryWriteBusyError: Int](/documentation/assetslibrary/alassetslibrarywritebusyerror)
- [var ALAssetsLibraryWriteInvalidDataError: Int](/documentation/assetslibrary/alassetslibrarywriteinvaliddataerror)
- [var ALAssetsLibraryWriteIncompatibleDataError: Int](/documentation/assetslibrary/alassetslibrarywriteincompatibledataerror)
- [var ALAssetsLibraryWriteDataEncodingError: Int](/documentation/assetslibrary/alassetslibrarywritedataencodingerror)
- [var ALAssetsLibraryWriteDiskSpaceError: Int](/documentation/assetslibrary/alassetslibrarywritediskspaceerror)
- [var ALAssetsLibraryDataUnavailableError: Int](/documentation/assetslibrary/alassetslibrarydataunavailableerror)
- [var ALAssetsLibraryAccessUserDeniedError: Int](/documentation/assetslibrary/alassetslibraryaccessuserdeniederror)
- [var ALAssetsLibraryAccessGloballyDeniedError: Int](/documentation/assetslibrary/alassetslibraryaccessgloballydeniederror)

### Notifications

- [static let ALAssetsLibraryChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/alassetslibrarychanged)

## Reference

- [AssetsLibrary Enumerations](/documentation/assetslibrary/assetslibrary-enumerations)

### Enumerations

- [ALAssetOrientation](/documentation/assetslibrary/alassetorientation)

#### Constants

- [case up](/documentation/assetslibrary/alassetorientation/up)
- [case down](/documentation/assetslibrary/alassetorientation/down)
- [case left](/documentation/assetslibrary/alassetorientation/left)
- [case right](/documentation/assetslibrary/alassetorientation/right)
- [case upMirrored](/documentation/assetslibrary/alassetorientation/upmirrored)
- [case downMirrored](/documentation/assetslibrary/alassetorientation/downmirrored)
- [case leftMirrored](/documentation/assetslibrary/alassetorientation/leftmirrored)
- [case rightMirrored](/documentation/assetslibrary/alassetorientation/rightmirrored)

#### Initializers

- [init?(rawValue: Int)](/documentation/assetslibrary/alassetorientation/init(rawvalue:))
- [ALAuthorizationStatus](/documentation/assetslibrary/alauthorizationstatus)

#### Constants

- [case notDetermined](/documentation/assetslibrary/alauthorizationstatus/notdetermined)
- [case restricted](/documentation/assetslibrary/alauthorizationstatus/restricted)
- [case denied](/documentation/assetslibrary/alauthorizationstatus/denied)
- [case authorized](/documentation/assetslibrary/alauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/assetslibrary/alauthorizationstatus/init(rawvalue:))
- [Error Codes](/documentation/assetslibrary/error-codes)

#### Constants

- [var ALAssetsLibraryUnknownError: Int](/documentation/assetslibrary/alassetslibraryunknownerror)
- [var ALAssetsLibraryWriteFailedError: Int](/documentation/assetslibrary/alassetslibrarywritefailederror)
- [var ALAssetsLibraryWriteBusyError: Int](/documentation/assetslibrary/alassetslibrarywritebusyerror)
- [var ALAssetsLibraryWriteInvalidDataError: Int](/documentation/assetslibrary/alassetslibrarywriteinvaliddataerror)
- [var ALAssetsLibraryWriteIncompatibleDataError: Int](/documentation/assetslibrary/alassetslibrarywriteincompatibledataerror)
- [var ALAssetsLibraryWriteDataEncodingError: Int](/documentation/assetslibrary/alassetslibrarywritedataencodingerror)
- [var ALAssetsLibraryWriteDiskSpaceError: Int](/documentation/assetslibrary/alassetslibrarywritediskspaceerror)
- [var ALAssetsLibraryDataUnavailableError: Int](/documentation/assetslibrary/alassetslibrarydataunavailableerror)
- [var ALAssetsLibraryAccessUserDeniedError: Int](/documentation/assetslibrary/alassetslibraryaccessuserdeniederror)
- [var ALAssetsLibraryAccessGloballyDeniedError: Int](/documentation/assetslibrary/alassetslibraryaccessgloballydeniederror)
- [Types of Asset](/documentation/assetslibrary/types-of-asset)

#### Constants

- [var ALAssetsGroupLibrary: UInt32](/documentation/assetslibrary/alassetsgrouplibrary)
- [var ALAssetsGroupAlbum: UInt32](/documentation/assetslibrary/alassetsgroupalbum)
- [var ALAssetsGroupEvent: UInt32](/documentation/assetslibrary/alassetsgroupevent)
- [var ALAssetsGroupFaces: UInt32](/documentation/assetslibrary/alassetsgroupfaces)
- [var ALAssetsGroupSavedPhotos: UInt32](/documentation/assetslibrary/alassetsgroupsavedphotos)
- [var ALAssetsGroupPhotoStream: UInt32](/documentation/assetslibrary/alassetsgroupphotostream)
- [var ALAssetsGroupAll: UInt32](/documentation/assetslibrary/alassetsgroupall)
- [AssetsLibrary Constants](/documentation/assetslibrary/assetslibrary-constants)

### Constants

- [let ALAssetLibraryDeletedAssetGroupsKey: String](/documentation/assetslibrary/alassetlibrarydeletedassetgroupskey)
- [let ALAssetLibraryInsertedAssetGroupsKey: String](/documentation/assetslibrary/alassetlibraryinsertedassetgroupskey)
- [let ALAssetLibraryUpdatedAssetGroupsKey: String](/documentation/assetslibrary/alassetlibraryupdatedassetgroupskey)
- [let ALAssetLibraryUpdatedAssetsKey: String](/documentation/assetslibrary/alassetlibraryupdatedassetskey)
- [let ALAssetPropertyAssetURL: String](/documentation/assetslibrary/alassetpropertyasseturl)
- [let ALAssetPropertyDate: String](/documentation/assetslibrary/alassetpropertydate)
- [let ALAssetPropertyDuration: String](/documentation/assetslibrary/alassetpropertyduration)
- [let ALAssetPropertyLocation: String](/documentation/assetslibrary/alassetpropertylocation)
- [let ALAssetPropertyOrientation: String](/documentation/assetslibrary/alassetpropertyorientation)
- [let ALAssetPropertyRepresentations: String](/documentation/assetslibrary/alassetpropertyrepresentations)
- [let ALAssetPropertyType: String](/documentation/assetslibrary/alassetpropertytype)
- [let ALAssetPropertyURLs: String](/documentation/assetslibrary/alassetpropertyurls)
- [let ALAssetTypePhoto: String](/documentation/assetslibrary/alassettypephoto)
- [let ALAssetTypeUnknown: String](/documentation/assetslibrary/alassettypeunknown)
- [let ALAssetTypeVideo: String](/documentation/assetslibrary/alassettypevideo)
- [let ALAssetsGroupPropertyName: String](/documentation/assetslibrary/alassetsgrouppropertyname)
- [let ALAssetsGroupPropertyPersistentID: String](/documentation/assetslibrary/alassetsgrouppropertypersistentid)
- [let ALAssetsGroupPropertyType: String](/documentation/assetslibrary/alassetsgrouppropertytype)
- [let ALAssetsGroupPropertyURL: String](/documentation/assetslibrary/alassetsgrouppropertyurl)
- [let ALAssetsLibraryErrorDomain: String](/documentation/assetslibrary/alassetslibraryerrordomain)
- [let ALErrorInvalidProperty: String](/documentation/assetslibrary/alerrorinvalidproperty)
- [AssetsLibrary Data Types](/documentation/assetslibrary/assetslibrary-data-types)

### Data Types

- [ALAssetsGroupEnumerationResultsBlock](/documentation/assetslibrary/alassetsgroupenumerationresultsblock)
- [ALAssetsGroupType](/documentation/assetslibrary/alassetsgrouptype)
- [ALAssetsLibraryAccessFailureBlock](/documentation/assetslibrary/alassetslibraryaccessfailureblock)
- [ALAssetsLibraryAssetForURLResultBlock](/documentation/assetslibrary/alassetslibraryassetforurlresultblock)
- [ALAssetsLibraryGroupResultBlock](/documentation/assetslibrary/alassetslibrarygroupresultblock)
- [ALAssetsLibraryGroupsEnumerationResultsBlock](/documentation/assetslibrary/alassetslibrarygroupsenumerationresultsblock)
- [ALAssetsLibraryWriteImageCompletionBlock](/documentation/assetslibrary/alassetslibrarywriteimagecompletionblock)
- [ALAssetsLibraryWriteVideoCompletionBlock](/documentation/assetslibrary/alassetslibrarywritevideocompletionblock)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
