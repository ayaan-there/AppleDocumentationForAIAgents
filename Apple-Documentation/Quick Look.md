# Quick Look Documentation

Source: https://sosumi.ai/documentation/quicklook

---
title: Quick Look
source: https://developer.apple.com/documentation/quicklook
timestamp: 2026-02-13T19:00:57.958Z
---

## Previews

- [QLPreviewController](/documentation/quicklook/qlpreviewcontroller)

### Configuring a preview controller

- [var dataSource: (any QLPreviewControllerDataSource)?](/documentation/quicklook/qlpreviewcontroller/datasource)
- [QLPreviewControllerDataSource](/documentation/quicklook/qlpreviewcontrollerdatasource)

#### Providing data to a preview controller

- [func numberOfPreviewItems(in: QLPreviewController) -> Int](/documentation/quicklook/qlpreviewcontrollerdatasource/numberofpreviewitems(in:))
- [func previewController(QLPreviewController, previewItemAt: Int) -> any QLPreviewItem](/documentation/quicklook/qlpreviewcontrollerdatasource/previewcontroller(_:previewitemat:))
- [var delegate: (any QLPreviewControllerDelegate)?](/documentation/quicklook/qlpreviewcontroller/delegate)
- [QLPreviewControllerDelegate](/documentation/quicklook/qlpreviewcontrollerdelegate)

#### Responding to preview requests

- [func previewController(QLPreviewController, frameFor: any QLPreviewItem, inSourceView: AutoreleasingUnsafeMutablePointer<UIView?>) -> CGRect](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontroller(_:framefor:insourceview:))
- [func previewController(QLPreviewController, transitionImageFor: any QLPreviewItem, contentRect: UnsafeMutablePointer<CGRect>) -> UIImage?](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontroller(_:transitionimagefor:contentrect:))
- [func previewController(QLPreviewController, transitionViewFor: any QLPreviewItem) -> UIView?](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontroller(_:transitionviewfor:))
- [func previewControllerWillDismiss(QLPreviewController)](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontrollerwilldismiss(_:))
- [func previewControllerDidDismiss(QLPreviewController)](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontrollerdiddismiss(_:))

#### Responding to user actions

- [func previewController(QLPreviewController, shouldOpen: URL, for: any QLPreviewItem) -> Bool](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontroller(_:shouldopen:for:))

#### Editing the content of a preview

- [func previewController(QLPreviewController, editingModeFor: any QLPreviewItem) -> QLPreviewItemEditingMode](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontroller(_:editingmodefor:))
- [QLPreviewItemEditingMode](/documentation/quicklook/qlpreviewitemeditingmode)

##### Enumeration Cases

- [case createCopy](/documentation/quicklook/qlpreviewitemeditingmode/createcopy)
- [case disabled](/documentation/quicklook/qlpreviewitemeditingmode/disabled)
- [case updateContents](/documentation/quicklook/qlpreviewitemeditingmode/updatecontents)

##### Initializers

- [init?(rawValue: Int)](/documentation/quicklook/qlpreviewitemeditingmode/init(rawvalue:))
- [func previewController(QLPreviewController, didUpdateContentsOf: any QLPreviewItem)](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontroller(_:didupdatecontentsof:))
- [func previewController(QLPreviewController, didSaveEditedCopyOf: any QLPreviewItem, at: URL)](/documentation/quicklook/qlpreviewcontrollerdelegate/previewcontroller(_:didsaveeditedcopyof:at:))

### Managing item previews

- [class func canPreview(any QLPreviewItem) -> Bool](/documentation/quicklook/qlpreviewcontroller/canpreview(_:))
- [var currentPreviewItem: (any QLPreviewItem)?](/documentation/quicklook/qlpreviewcontroller/currentpreviewitem)
- [var currentPreviewItemIndex: Int](/documentation/quicklook/qlpreviewcontroller/currentpreviewitemindex)
- [func refreshCurrentPreviewItem()](/documentation/quicklook/qlpreviewcontroller/refreshcurrentpreviewitem())
- [func reloadData()](/documentation/quicklook/qlpreviewcontroller/reloaddata())
- [QLPreviewItem](/documentation/quicklookui/qlpreviewitem)
- [QLPreviewSceneActivationConfiguration](/documentation/quicklook/qlpreviewsceneactivationconfiguration)

### Creating a preview scene activation configuration

- [init(itemsAt: [URL], options: QLPreviewSceneActivationConfiguration.Options?)](/documentation/quicklook/qlpreviewsceneactivationconfiguration/init(itemsat:options:))

### Configuring a preview scene activation

- [QLPreviewSceneActivationConfiguration.Options](/documentation/quicklook/qlpreviewsceneactivationconfiguration/options)

#### Identifying the initial item to preview

- [var initialPreviewIndex: Int](/documentation/quicklook/qlpreviewsceneactivationconfiguration/options/initialpreviewindex)
- [var initialPreviewIndex: Int](/documentation/quicklook/qlpreviewsceneactivationconfiguration/options/initialpreviewindex)
- [Previews or thumbnail images for macOS 10.14 or earlier](/documentation/quicklook/previews-or-thumbnail-images-for-macos-10-14-or-earlier)

### Creating thumbnails

- [func QLThumbnailImageCreate(CFAllocator!, CFURL!, CGSize, CFDictionary!) -> Unmanaged<CGImage>!](/documentation/quicklook/qlthumbnailimagecreate(_:_:_:_:))
- [func QLThumbnailCreate(CFAllocator!, CFURL!, CGSize, CFDictionary!) -> Unmanaged<QLThumbnail>!](/documentation/quicklook/qlthumbnailcreate(_:_:_:_:))
- [func QLThumbnailDispatchAsync(QLThumbnail!, dispatch_queue_t!, (() -> Void)!)](/documentation/quicklook/qlthumbnaildispatchasync(_:_:_:))
- [func QLThumbnailCancel(QLThumbnail!)](/documentation/quicklook/qlthumbnailcancel(_:))
- [func QLThumbnailCopyDocumentURL(QLThumbnail!) -> Unmanaged<CFURL>!](/documentation/quicklook/qlthumbnailcopydocumenturl(_:))
- [func QLThumbnailCopyImage(QLThumbnail!) -> Unmanaged<CGImage>!](/documentation/quicklook/qlthumbnailcopyimage(_:))
- [func QLThumbnailCopyOptions(QLThumbnail!) -> Unmanaged<CFDictionary>!](/documentation/quicklook/qlthumbnailcopyoptions(_:))
- [func QLThumbnailGetContentRect(QLThumbnail!) -> CGRect](/documentation/quicklook/qlthumbnailgetcontentrect(_:))
- [func QLThumbnailGetMaximumSize(QLThumbnail!) -> CGSize](/documentation/quicklook/qlthumbnailgetmaximumsize(_:))
- [func QLThumbnailGetTypeID() -> CFTypeID](/documentation/quicklook/qlthumbnailgettypeid())
- [func QLThumbnailIsCancelled(QLThumbnail!) -> Bool](/documentation/quicklook/qlthumbnailiscancelled(_:))

### Handling thumbnail requests

- [func QLThumbnailRequestCopyContentUTI(QLThumbnailRequest!) -> Unmanaged<CFString>!](/documentation/quicklook/qlthumbnailrequestcopycontentuti(_:))
- [func QLThumbnailRequestCopyOptions(QLThumbnailRequest!) -> Unmanaged<CFDictionary>!](/documentation/quicklook/qlthumbnailrequestcopyoptions(_:))
- [func QLThumbnailRequestCopyURL(QLThumbnailRequest!) -> Unmanaged<CFURL>!](/documentation/quicklook/qlthumbnailrequestcopyurl(_:))
- [func QLThumbnailRequestCreateContext(QLThumbnailRequest!, CGSize, Bool, CFDictionary!) -> Unmanaged<CGContext>!](/documentation/quicklook/qlthumbnailrequestcreatecontext(_:_:_:_:))
- [func QLThumbnailRequestFlushContext(QLThumbnailRequest!, CGContext!)](/documentation/quicklook/qlthumbnailrequestflushcontext(_:_:))
- [func QLThumbnailRequestGetDocumentObject(QLThumbnailRequest!) -> UnsafeRawPointer!](/documentation/quicklook/qlthumbnailrequestgetdocumentobject(_:))
- [func QLThumbnailRequestGetGeneratorBundle(QLThumbnailRequest!) -> Unmanaged<CFBundle>!](/documentation/quicklook/qlthumbnailrequestgetgeneratorbundle(_:))
- [func QLThumbnailRequestGetMaximumSize(QLThumbnailRequest!) -> CGSize](/documentation/quicklook/qlthumbnailrequestgetmaximumsize(_:))
- [func QLThumbnailRequestGetTypeID() -> CFTypeID](/documentation/quicklook/qlthumbnailrequestgettypeid())
- [func QLThumbnailRequestIsCancelled(QLThumbnailRequest!) -> Bool](/documentation/quicklook/qlthumbnailrequestiscancelled(_:))
- [func QLThumbnailRequestSetDocumentObject(QLThumbnailRequest!, UnsafeRawPointer!, UnsafePointer<CFArrayCallBacks>!)](/documentation/quicklook/qlthumbnailrequestsetdocumentobject(_:_:_:))
- [func QLThumbnailRequestSetImage(QLThumbnailRequest!, CGImage!, CFDictionary!)](/documentation/quicklook/qlthumbnailrequestsetimage(_:_:_:))
- [func QLThumbnailRequestSetImageAtURL(QLThumbnailRequest!, CFURL!, CFDictionary!)](/documentation/quicklook/qlthumbnailrequestsetimageaturl(_:_:_:))
- [func QLThumbnailRequestSetImageWithData(QLThumbnailRequest!, CFData!, CFDictionary!)](/documentation/quicklook/qlthumbnailrequestsetimagewithdata(_:_:_:))
- [func QLThumbnailRequestSetThumbnailWithDataRepresentation(QLThumbnailRequest!, CFData!, CFString!, CFDictionary!, CFDictionary!)](/documentation/quicklook/qlthumbnailrequestsetthumbnailwithdatarepresentation(_:_:_:_:_:))
- [func QLThumbnailRequestSetThumbnailWithURLRepresentation(QLThumbnailRequest!, CFURL!, CFString!, CFDictionary!, CFDictionary!)](/documentation/quicklook/qlthumbnailrequestsetthumbnailwithurlrepresentation(_:_:_:_:_:))

### Requesting previews

- [func QLPreviewRequestCopyContentUTI(QLPreviewRequest!) -> Unmanaged<CFString>!](/documentation/quicklook/qlpreviewrequestcopycontentuti(_:))
- [func QLPreviewRequestCopyOptions(QLPreviewRequest!) -> Unmanaged<CFDictionary>!](/documentation/quicklook/qlpreviewrequestcopyoptions(_:))
- [func QLPreviewRequestCopyURL(QLPreviewRequest!) -> Unmanaged<CFURL>!](/documentation/quicklook/qlpreviewrequestcopyurl(_:))
- [func QLPreviewRequestCreateContext(QLPreviewRequest!, CGSize, Bool, CFDictionary!) -> Unmanaged<CGContext>!](/documentation/quicklook/qlpreviewrequestcreatecontext(_:_:_:_:))
- [func QLPreviewRequestCreatePDFContext(QLPreviewRequest!, UnsafePointer<CGRect>!, CFDictionary!, CFDictionary!) -> Unmanaged<CGContext>!](/documentation/quicklook/qlpreviewrequestcreatepdfcontext(_:_:_:_:))
- [func QLPreviewRequestFlushContext(QLPreviewRequest!, CGContext!)](/documentation/quicklook/qlpreviewrequestflushcontext(_:_:))
- [func QLPreviewRequestGetDocumentObject(QLPreviewRequest!) -> UnsafeRawPointer!](/documentation/quicklook/qlpreviewrequestgetdocumentobject(_:))
- [func QLPreviewRequestSetDocumentObject(QLPreviewRequest!, UnsafeRawPointer!, UnsafePointer<CFArrayCallBacks>!)](/documentation/quicklook/qlpreviewrequestsetdocumentobject(_:_:_:))
- [func QLPreviewRequestGetGeneratorBundle(QLPreviewRequest!) -> Unmanaged<CFBundle>!](/documentation/quicklook/qlpreviewrequestgetgeneratorbundle(_:))
- [func QLPreviewRequestGetTypeID() -> CFTypeID](/documentation/quicklook/qlpreviewrequestgettypeid())
- [func QLPreviewRequestIsCancelled(QLPreviewRequest!) -> Bool](/documentation/quicklook/qlpreviewrequestiscancelled(_:))
- [func QLPreviewRequestSetDataRepresentation(QLPreviewRequest!, CFData!, CFString!, CFDictionary!)](/documentation/quicklook/qlpreviewrequestsetdatarepresentation(_:_:_:_:))
- [func QLPreviewRequestSetURLRepresentation(QLPreviewRequest!, CFURL!, CFString!, CFDictionary!)](/documentation/quicklook/qlpreviewrequestseturlrepresentation(_:_:_:_:))

### Configuring the appearance of PDF previews

- [QLPreviewPDFStyle](/documentation/quicklook/qlpreviewpdfstyle)

#### Creating a Preview Style for PDF Files

- [init(UInt32)](/documentation/quicklook/qlpreviewpdfstyle/init(_:))
- [init(rawValue: UInt32)](/documentation/quicklook/qlpreviewpdfstyle/init(rawvalue:))
- [var rawValue: UInt32](/documentation/quicklook/qlpreviewpdfstyle/rawvalue)

#### Styles for PDF Previews

- [var kQLPreviewPDFStandardStyle: QLPreviewPDFStyle](/documentation/quicklook/kqlpreviewpdfstandardstyle)
- [var kQLPreviewPDFPagesWithThumbnailsOnLeftStyle: QLPreviewPDFStyle](/documentation/quicklook/kqlpreviewpdfpageswiththumbnailsonleftstyle)
- [var kQLPreviewPDFPagesWithThumbnailsOnRightStyle: QLPreviewPDFStyle](/documentation/quicklook/kqlpreviewpdfpageswiththumbnailsonrightstyle)

### Interfacing with a Quick Look plug-in

- [QLGeneratorInterfaceStruct](/documentation/quicklook/qlgeneratorinterfacestruct)

#### Creating a Quick Look Plug-In

- [init()](/documentation/quicklook/qlgeneratorinterfacestruct/init())
- [var QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!](/documentation/quicklook/qlgeneratorinterfacestruct/queryinterface)
- [var AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/quicklook/qlgeneratorinterfacestruct/addref)
- [var Release: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/quicklook/qlgeneratorinterfacestruct/release)
- [var GenerateThumbnailForURL: ((UnsafeMutableRawPointer?, QLThumbnailRequest?, CFURL?, CFString?, CFDictionary?, CGSize) -> OSStatus)!](/documentation/quicklook/qlgeneratorinterfacestruct/generatethumbnailforurl)
- [var CancelThumbnailGeneration: ((UnsafeMutableRawPointer?, QLThumbnailRequest?) -> Void)!](/documentation/quicklook/qlgeneratorinterfacestruct/cancelthumbnailgeneration)
- [var GeneratePreviewForURL: ((UnsafeMutableRawPointer?, QLPreviewRequest?, CFURL?, CFString?, CFDictionary?) -> OSStatus)!](/documentation/quicklook/qlgeneratorinterfacestruct/generatepreviewforurl)
- [var CancelPreviewGeneration: ((UnsafeMutableRawPointer?, QLPreviewRequest?) -> Void)!](/documentation/quicklook/qlgeneratorinterfacestruct/cancelpreviewgeneration)

### Opaque types

- [QLThumbnail](/documentation/quicklook/qlthumbnail)
- [QLThumbnailRequest](/documentation/quicklook/qlthumbnailrequest)
- [QLPreviewRequest](/documentation/quicklook/qlpreviewrequest)

### Constants

- [var kQLReturnMask: Int32](/documentation/quicklook/kqlreturnmask)
- [var kQLReturnHasMore: Int32](/documentation/quicklook/kqlreturnhasmore)
- [let kQLThumbnailOptionIconModeKey: CFString!](/documentation/quicklook/kqlthumbnailoptioniconmodekey)
- [let kQLThumbnailOptionScaleFactorKey: CFString!](/documentation/quicklook/kqlthumbnailoptionscalefactorkey)
- [var QUICKLOOK_VERSION: Int32](/documentation/quicklook/quicklook_version)

### Deprecated constants

- [let kQLPreviewContentIDScheme: CFString!](/documentation/quicklook/kqlpreviewcontentidscheme)
- [let kQLPreviewPropertyCursorKey: CFString!](/documentation/quicklook/kqlpreviewpropertycursorkey)
- [let kQLPreviewOptionCursorKey: CFString!](/documentation/quicklook/kqlpreviewoptioncursorkey)
- [let kQLPreviewPropertyAttachmentDataKey: CFString!](/documentation/quicklook/kqlpreviewpropertyattachmentdatakey)
- [let kQLPreviewPropertyAttachmentsKey: CFString!](/documentation/quicklook/kqlpreviewpropertyattachmentskey)
- [let kQLPreviewPropertyBaseBundlePathKey: CFString!](/documentation/quicklook/kqlpreviewpropertybasebundlepathkey)
- [let kQLPreviewPropertyDisplayNameKey: CFString!](/documentation/quicklook/kqlpreviewpropertydisplaynamekey)
- [let kQLPreviewPropertyHeightKey: CFString!](/documentation/quicklook/kqlpreviewpropertyheightkey)
- [let kQLPreviewPropertyMIMETypeKey: CFString!](/documentation/quicklook/kqlpreviewpropertymimetypekey)
- [let kQLPreviewPropertyPDFStyleKey: CFString!](/documentation/quicklook/kqlpreviewpropertypdfstylekey)
- [let kQLPreviewPropertyStringEncodingKey: CFString!](/documentation/quicklook/kqlpreviewpropertystringencodingkey)
- [let kQLPreviewPropertyTextEncodingNameKey: CFString!](/documentation/quicklook/kqlpreviewpropertytextencodingnamekey)
- [let kQLPreviewPropertyWidthKey: CFString!](/documentation/quicklook/kqlpreviewpropertywidthkey)
- [let kQLThumbnailPropertyBadgeImageKey: CFString!](/documentation/quicklook/kqlthumbnailpropertybadgeimagekey)
- [let kQLThumbnailPropertyBaseBundlePathKey: CFString!](/documentation/quicklook/kqlthumbnailpropertybasebundlepathkey)
- [let kQLThumbnailPropertyExtensionKey: CFString!](/documentation/quicklook/kqlthumbnailpropertyextensionkey)

### QuickLookUI symbols

- [QLFilePreviewRequest](/documentation/quicklook/qlfilepreviewrequest)

#### Instance Properties

- [var fileURL: URL](/documentation/quicklook/qlfilepreviewrequest/fileurl)
- [QLPreviewProvider](/documentation/quicklook/qlpreviewprovider)
- [QLPreviewReply](/documentation/quicklook/qlpreviewreply)

#### Initializers

- [convenience init(contextSize: CGSize, isBitmap: Bool, drawUsing: (CGContext, QLPreviewReply) throws -> Void)](/documentation/quicklook/qlpreviewreply/init(contextsize:isbitmap:drawusing:))
- [convenience init(dataOfContentType: UTType, contentSize: CGSize, createDataUsing: (QLPreviewReply) throws -> Data)](/documentation/quicklook/qlpreviewreply/init(dataofcontenttype:contentsize:createdatausing:))
- [init(fileURL: URL)](/documentation/quicklook/qlpreviewreply/init(fileurl:))
- [convenience init(forPDFWithPageSize: CGSize, createDocumentUsing: (QLPreviewReply) throws -> PDFDocument)](/documentation/quicklook/qlpreviewreply/init(forpdfwithpagesize:createdocumentusing:))

#### Instance Properties

- [var attachments: [String : QLPreviewReplyAttachment]](/documentation/quicklook/qlpreviewreply/attachments)
- [var stringEncoding: String.Encoding](/documentation/quicklook/qlpreviewreply/stringencoding-8rrio)
- [var title: String](/documentation/quicklook/qlpreviewreply/title)
- [QLPreviewReplyAttachment](/documentation/quicklook/qlpreviewreplyattachment)

#### Initializers

- [init(data: Data, contentType: UTType)](/documentation/quicklook/qlpreviewreplyattachment/init(data:contenttype:))

#### Instance Properties

- [var contentType: UTType](/documentation/quicklook/qlpreviewreplyattachment/contenttype)
- [var data: Data](/documentation/quicklook/qlpreviewreplyattachment/data)
- [QLPreviewItem](/documentation/quicklook/qlpreviewitem)

#### Instance Properties

- [var previewItemTitle: String?](/documentation/quicklook/qlpreviewitem/previewitemtitle)
- [var previewItemURL: URL?](/documentation/quicklook/qlpreviewitem/previewitemurl)
- [QLPreviewingController](/documentation/quicklook/qlpreviewingcontroller)

#### Instance Methods

- [func preparePreviewOfFile(at: URL, completionHandler: ((any Error)?) -> Void)](/documentation/quicklook/qlpreviewingcontroller/preparepreviewoffile(at:completionhandler:))
- [func preparePreviewOfSearchableItem(identifier: String, queryString: String?, completionHandler: ((any Error)?) -> Void)](/documentation/quicklook/qlpreviewingcontroller/preparepreviewofsearchableitem(identifier:querystring:completionhandler:))
- [func providePreview(for: QLFilePreviewRequest, completionHandler: (QLPreviewReply?, (any Error)?) -> Void)](/documentation/quicklook/qlpreviewingcontroller/providepreview(for:completionhandler:))

## Preview extensions

- [QLPreviewingController](/documentation/quicklookui/qlpreviewingcontroller)

## Data-based preview extensions

- [QLPreviewProvider](/documentation/quicklookui/qlpreviewprovider)
- [QLFilePreviewRequest](/documentation/quicklookui/qlfilepreviewrequest)
- [QLPreviewReply](/documentation/quicklookui/qlpreviewreply)
- [QLPreviewReplyAttachment](/documentation/quicklookui/qlpreviewreplyattachment)

## Classes

- [ARQuickLookPreviewItem](/documentation/quicklook/arquicklookpreviewitem)

### Initializers

- [init(fileAt: URL)](/documentation/quicklook/arquicklookpreviewitem/init(fileat:))

### Instance Properties

- [var allowsContentScaling: Bool](/documentation/quicklook/arquicklookpreviewitem/allowscontentscaling)
- [var canonicalWebPageURL: URL?](/documentation/quicklook/arquicklookpreviewitem/canonicalwebpageurl)
- [PreviewApplication](/documentation/quicklook/previewapplication)

### Type Methods

- [class func open(items: [PreviewItem], selectedItem: PreviewItem?) -> PreviewSession](/documentation/quicklook/previewapplication/open(items:selecteditem:))
- [class func open(urls: [URL], selectedURL: URL?) -> PreviewSession](/documentation/quicklook/previewapplication/open(urls:selectedurl:))

## Structures

- [PreviewItem](/documentation/quicklook/previewitem)

### Operators

- [static func == (PreviewItem, PreviewItem) -> Bool](/documentation/quicklook/previewitem/==(_:_:))

### Initializers

- [init(url: URL, displayName: String?, editingMode: EditingMode)](/documentation/quicklook/previewitem/init(url:displayname:editingmode:))

### Instance Properties

- [let displayName: String?](/documentation/quicklook/previewitem/displayname)
- [let editingMode: EditingMode](/documentation/quicklook/previewitem/editingmode)
- [let id: UUID](/documentation/quicklook/previewitem/id)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/quicklook/previewitem/hash(into:))
- [PreviewSession](/documentation/quicklook/previewsession)

### Instance Properties

- [var events: some AsyncSequence<PreviewSession.Event, Never>](/documentation/quicklook/previewsession/events)

### Instance Methods

- [func close() async throws](/documentation/quicklook/previewsession/close())

### Enumerations

- [PreviewSession.Event](/documentation/quicklook/previewsession/event)

#### Enumeration Cases

- [case didClose](/documentation/quicklook/previewsession/event/didclose)
- [case didFail(any Error)](/documentation/quicklook/previewsession/event/didfail(_:))
- [case didOpen](/documentation/quicklook/previewsession/event/didopen)

## Type Aliases

- [EditingMode](/documentation/quicklook/editingmode)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
