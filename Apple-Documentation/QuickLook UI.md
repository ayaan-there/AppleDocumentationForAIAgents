# QuickLook UI Documentation

Source: https://sosumi.ai/documentation/quicklookui

---
title: Quick Look UI
source: https://developer.apple.com/documentation/quicklookui
timestamp: 2026-02-13T19:01:01.917Z
---

## Previews

- [QLPreviewPanel](/documentation/quicklookui/qlpreviewpanel)

### Accessing the Shared Panel

- [class func shared() -> QLPreviewPanel!](/documentation/quicklookui/qlpreviewpanel/shared())
- [class func sharedPreviewPanelExists() -> Bool](/documentation/quicklookui/qlpreviewpanel/sharedpreviewpanelexists())

### Accessing the Preview Panel Controller

- [var currentController: Any!](/documentation/quicklookui/qlpreviewpanel/currentcontroller)
- [func updateController()](/documentation/quicklookui/qlpreviewpanel/updatecontroller())

### Managing the Preview Items

- [var dataSource: (any QLPreviewPanelDataSource)!](/documentation/quicklookui/qlpreviewpanel/datasource)
- [func reloadData()](/documentation/quicklookui/qlpreviewpanel/reloaddata())
- [func refreshCurrentPreviewItem()](/documentation/quicklookui/qlpreviewpanel/refreshcurrentpreviewitem())
- [var currentPreviewItemIndex: Int](/documentation/quicklookui/qlpreviewpanel/currentpreviewitemindex)
- [var currentPreviewItem: (any QLPreviewItem)!](/documentation/quicklookui/qlpreviewpanel/currentpreviewitem)
- [var displayState: Any!](/documentation/quicklookui/qlpreviewpanel/displaystate)

### The Panel’s Delegate

- [var delegate: AnyObject!](/documentation/quicklookui/qlpreviewpanel/delegate)

### Managing Full Screen Mode

- [func enterFullScreenMode(NSScreen!, withOptions: [AnyHashable : Any]!) -> Bool](/documentation/quicklookui/qlpreviewpanel/enterfullscreenmode(_:withoptions:))
- [func exitFullScreenMode(options: [AnyHashable : Any]!)](/documentation/quicklookui/qlpreviewpanel/exitfullscreenmode(options:))
- [var isInFullScreenMode: Bool](/documentation/quicklookui/qlpreviewpanel/isinfullscreenmode)
- [QLPreviewView](/documentation/quicklookui/qlpreviewview)

### Creating a Preview View

- [init!(frame: NSRect, style: QLPreviewViewStyle)](/documentation/quicklookui/qlpreviewview/init(frame:style:))
- [init!(frame: NSRect)](/documentation/quicklookui/qlpreviewview/init(frame:))
- [QLPreviewViewStyle](/documentation/quicklookui/qlpreviewviewstyle)

#### Choosing a Preview Style

- [case normal](/documentation/quicklookui/qlpreviewviewstyle/normal)
- [case compact](/documentation/quicklookui/qlpreviewviewstyle/compact)

#### Initializers

- [init?(rawValue: UInt)](/documentation/quicklookui/qlpreviewviewstyle/init(rawvalue:))

### Displaying a Preview

- [var previewItem: (any QLPreviewItem)!](/documentation/quicklookui/qlpreviewview/previewitem)
- [func refreshPreviewItem()](/documentation/quicklookui/qlpreviewview/refreshpreviewitem())
- [var displayState: Any!](/documentation/quicklookui/qlpreviewview/displaystate)
- [var autostarts: Bool](/documentation/quicklookui/qlpreviewview/autostarts)

### Closing a Preview

- [var shouldCloseWithWindow: Bool](/documentation/quicklookui/qlpreviewview/shouldclosewithwindow)
- [func close()](/documentation/quicklookui/qlpreviewview/close())
- [QLPreviewItem](/documentation/quicklookui/qlpreviewitem)

### Instance Properties

- [var previewItemDisplayState: Any!](/documentation/quicklookui/qlpreviewitem/previewitemdisplaystate)
- [var previewItemTitle: String!](/documentation/quicklookui/qlpreviewitem/previewitemtitle)
- [var previewItemURL: URL!](/documentation/quicklookui/qlpreviewitem/previewitemurl)
- [QLPreviewPanelDataSource](/documentation/quicklookui/qlpreviewpaneldatasource)

### Required Methods

- [func numberOfPreviewItems(in: QLPreviewPanel!) -> Int](/documentation/quicklookui/qlpreviewpaneldatasource/numberofpreviewitems(in:))
- [func previewPanel(QLPreviewPanel!, previewItemAt: Int) -> (any QLPreviewItem)!](/documentation/quicklookui/qlpreviewpaneldatasource/previewpanel(_:previewitemat:))
- [QLPreviewPanelDelegate](/documentation/quicklookui/qlpreviewpaneldelegate)

### Optional Methods

- [func previewPanel(QLPreviewPanel!, handle: NSEvent!) -> Bool](/documentation/quicklookui/qlpreviewpaneldelegate/previewpanel(_:handle:))
- [func previewPanel(QLPreviewPanel!, sourceFrameOnScreenFor: (any QLPreviewItem)!) -> NSRect](/documentation/quicklookui/qlpreviewpaneldelegate/previewpanel(_:sourceframeonscreenfor:))
- [func previewPanel(QLPreviewPanel!, transitionImageFor: (any QLPreviewItem)!, contentRect: UnsafeMutablePointer<NSRect>!) -> Any!](/documentation/quicklookui/qlpreviewpaneldelegate/previewpanel(_:transitionimagefor:contentrect:))
- [QLPreviewItemLoadingBlock](/documentation/quicklookui/qlpreviewitemloadingblock)

## Preview Extensions

- [QLPreviewingController](/documentation/quicklookui/qlpreviewingcontroller)

### Instance Methods

- [func preparePreviewOfFile(at: URL, completionHandler: ((any Error)?) -> Void)](/documentation/quicklookui/qlpreviewingcontroller/preparepreviewoffile(at:completionhandler:))
- [func preparePreviewOfSearchableItem(identifier: String, queryString: String?, completionHandler: ((any Error)?) -> Void)](/documentation/quicklookui/qlpreviewingcontroller/preparepreviewofsearchableitem(identifier:querystring:completionhandler:))
- [func providePreview(for: QLFilePreviewRequest, completionHandler: (QLPreviewReply?, (any Error)?) -> Void)](/documentation/quicklookui/qlpreviewingcontroller/providepreview(for:completionhandler:))

## Data-based Preview Extensions

- [QLPreviewProvider](/documentation/quicklookui/qlpreviewprovider)
- [QLFilePreviewRequest](/documentation/quicklookui/qlfilepreviewrequest)

### Inspecting the preview request

- [var fileURL: URL](/documentation/quicklookui/qlfilepreviewrequest/fileurl)
- [QLPreviewReply](/documentation/quicklookui/qlpreviewreply)

### Creating a preview reply

- [init(fileURL: URL)](/documentation/quicklookui/qlpreviewreply/init(fileurl:))

### Create a PDF preview reply

- [convenience init(forPDFWithPageSize: CGSize, createDocumentUsing: (QLPreviewReply) throws -> PDFDocument)](/documentation/quicklookui/qlpreviewreply/init(forpdfwithpagesize:createdocumentusing:))

### Generating a preview reply

- [convenience init(dataOfContentType: UTType, contentSize: CGSize, createDataUsing: (QLPreviewReply) throws -> Data)](/documentation/quicklookui/qlpreviewreply/init(dataofcontenttype:contentsize:createdatausing:))

### Drawing a preview reply

- [convenience init(contextSize: CGSize, isBitmap: Bool, drawUsing: (CGContext, QLPreviewReply) throws -> Void)](/documentation/quicklookui/qlpreviewreply/init(contextsize:isbitmap:drawusing:))

### Inspecting a preview reply

- [var title: String](/documentation/quicklookui/qlpreviewreply/title)
- [var attachments: [String : QLPreviewReplyAttachment]](/documentation/quicklookui/qlpreviewreply/attachments)
- [var stringEncoding: String.Encoding](/documentation/quicklookui/qlpreviewreply/stringencoding-8ahm8)
- [QLPreviewReplyAttachment](/documentation/quicklookui/qlpreviewreplyattachment)

### Creating a preview reply attachment

- [init(data: Data, contentType: UTType)](/documentation/quicklookui/qlpreviewreplyattachment/init(data:contenttype:))

### Inspecting a preview reply attachment

- [var contentType: UTType](/documentation/quicklookui/qlpreviewreplyattachment/contenttype)
- [var data: Data](/documentation/quicklookui/qlpreviewreplyattachment/data)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
