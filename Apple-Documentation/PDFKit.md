# PDFKit Documentation

Source: https://sosumi.ai/documentation/pdfkit

---
title: PDFKit
source: https://developer.apple.com/documentation/pdfkit
timestamp: 2026-02-13T19:00:31.415Z
---

## Views

- [PDFView](/documentation/pdfkit/pdfview)

### Associating a Document with a View

- [var document: PDFDocument?](/documentation/pdfkit/pdfview/document)
- [func takePasswordFrom(Any)](/documentation/pdfkit/pdfview/takepasswordfrom(_:))

### Configuring Document View

- [Configurations](/documentation/pdfkit/configurations)

#### Working with Display Modes and Characteristics

- [var displayMode: PDFDisplayMode](/documentation/pdfkit/pdfview/displaymode)
- [PDFDisplayMode](/documentation/pdfkit/pdfdisplaymode)

##### Constants

- [case singlePage](/documentation/pdfkit/pdfdisplaymode/singlepage)
- [case singlePageContinuous](/documentation/pdfkit/pdfdisplaymode/singlepagecontinuous)
- [case twoUp](/documentation/pdfkit/pdfdisplaymode/twoup)
- [case twoUpContinuous](/documentation/pdfkit/pdfdisplaymode/twoupcontinuous)

##### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfdisplaymode/init(rawvalue:))
- [Additional Display Configurations](/documentation/pdfkit/additional-display-configurations)

##### Defining Display Box

- [var displayBox: PDFDisplayBox](/documentation/pdfkit/pdfview/displaybox)

##### Defining Page Breaks

- [var displaysPageBreaks: Bool](/documentation/pdfkit/pdfview/displayspagebreaks)
- [var pageBreakMargins: UIEdgeInsets](/documentation/pdfkit/pdfview/pagebreakmargins)

##### Defining Display Direction

- [var displayDirection: PDFDisplayDirection](/documentation/pdfkit/pdfview/displaydirection)
- [var displaysRTL: Bool](/documentation/pdfkit/pdfview/displaysrtl)
- [Book Display](/documentation/pdfkit/book-display)

##### Displaying as Book

- [var displaysAsBook: Bool](/documentation/pdfkit/pdfview/displaysasbook)
- [var isUsingPageViewController: Bool](/documentation/pdfkit/pdfview/isusingpageviewcontroller)
- [func usePageViewController(Bool, withViewOptions: [AnyHashable : Any]?)](/documentation/pdfkit/pdfview/usepageviewcontroller(_:withviewoptions:))
- [Graphics Properties](/documentation/pdfkit/graphics-properties)

##### Setting Background Color

- [func takeBackgroundColorFrom(Any)](/documentation/pdfkit/pdfview/takebackgroundcolorfrom(_:))
- [var backgroundColor: UIColor](/documentation/pdfkit/pdfview/backgroundcolor)

##### Antialiasing

- [var shouldAntiAlias: Bool](/documentation/pdfkit/pdfview/shouldantialias)
- [var interpolationQuality: PDFInterpolationQuality](/documentation/pdfkit/pdfview/interpolationquality)
- [PDFInterpolationQuality](/documentation/pdfkit/pdfinterpolationquality)

###### Enumeration Cases

- [case none](/documentation/pdfkit/pdfinterpolationquality/none)
- [case low](/documentation/pdfkit/pdfinterpolationquality/low)
- [case high](/documentation/pdfkit/pdfinterpolationquality/high)

###### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfinterpolationquality/init(rawvalue:))

##### Greeking

- [var greekingThreshold: CGFloat](/documentation/pdfkit/pdfview/greekingthreshold)

#### Scaling the View

- [var scaleFactor: CGFloat](/documentation/pdfkit/pdfview/scalefactor)
- [var scaleFactorForSizeToFit: CGFloat](/documentation/pdfkit/pdfview/scalefactorforsizetofit)
- [var maxScaleFactor: CGFloat](/documentation/pdfkit/pdfview/maxscalefactor)
- [var minScaleFactor: CGFloat](/documentation/pdfkit/pdfview/minscalefactor)
- [var autoScales: Bool](/documentation/pdfkit/pdfview/autoscales)
- [func rowSize(for: PDFPage) -> CGSize](/documentation/pdfkit/pdfview/rowsize(for:))
- [Zoom Operations](/documentation/pdfkit/zoom-operations)

##### Zooming in a PDF View

- [func zoomIn(Any?)](/documentation/pdfkit/pdfview/zoomin(_:))
- [var canZoomIn: Bool](/documentation/pdfkit/pdfview/canzoomin)
- [func zoomOut(Any?)](/documentation/pdfkit/pdfview/zoomout(_:))
- [var canZoomOut: Bool](/documentation/pdfkit/pdfview/canzoomout)

#### Rendering the View and Printing

- [func draw(PDFPage)](/documentation/pdfkit/pdfview/draw(_:))
- [func drawPagePost(PDFPage)](/documentation/pdfkit/pdfview/drawpagepost(_:))
- [func print(with: NSPrintInfo, autoRotate: Bool)](/documentation/pdfkit/pdfview/print(with:autorotate:))
- [func print(with: NSPrintInfo, autoRotate: Bool, pageScaling: PDFPrintScalingMode)](/documentation/pdfkit/pdfview/print(with:autorotate:pagescaling:))

#### Specializing the View

- [var documentView: UIView?](/documentation/pdfkit/pdfview/documentview)
- [func layoutDocumentView()](/documentation/pdfkit/pdfview/layoutdocumentview())
- [Draw Operations](/documentation/pdfkit/draw-operations)

##### Drawing in a PDF Page

- [func draw(PDFPage, to: CGContext)](/documentation/pdfkit/pdfview/draw(_:to:))
- [func drawPagePost(PDFPage, to: CGContext)](/documentation/pdfkit/pdfview/drawpagepost(_:to:))

### Interacting in a View

- [Document Interactions](/documentation/pdfkit/document-interactions)

#### Handling Selections

- [var currentSelection: PDFSelection?](/documentation/pdfkit/pdfview/currentselection)
- [func setCurrentSelection(PDFSelection?, animate: Bool)](/documentation/pdfkit/pdfview/setcurrentselection(_:animate:))
- [func selectAll(Any?)](/documentation/pdfkit/pdfview/selectall(_:))
- [func clearSelection()](/documentation/pdfkit/pdfview/clearselection())
- [func copy(Any?)](/documentation/pdfkit/pdfview/copy(_:))
- [func scrollSelectionToVisible(Any?)](/documentation/pdfkit/pdfview/scrollselectiontovisible(_:))
- [var highlightedSelections: [PDFSelection]?](/documentation/pdfkit/pdfview/highlightedselections)

#### Working with Annotation Actions

- [func annotationsChanged(on: PDFPage)](/documentation/pdfkit/pdfview/annotationschanged(on:))
- [Link Annotations](/documentation/pdfkit/link-annotations)

##### Linking in a View

- [var enableDataDetectors: Bool](/documentation/pdfkit/pdfview/enabledatadetectors)

#### Converting Page and View Points

- [func page(for: CGPoint, nearest: Bool) -> PDFPage?](/documentation/pdfkit/pdfview/page(for:nearest:))
- [func convert(CGPoint, to: PDFPage) -> CGPoint](/documentation/pdfkit/pdfview/convert(_:to:)-9twqk)
- [func convert(CGRect, to: PDFPage) -> CGRect](/documentation/pdfkit/pdfview/convert(_:to:)-8cp0c)
- [func convert(CGPoint, from: PDFPage) -> CGPoint](/documentation/pdfkit/pdfview/convert(_:from:)-4evlx)
- [func convert(CGRect, from: PDFPage) -> CGRect](/documentation/pdfkit/pdfview/convert(_:from:)-9xv1z)

#### Working with Mouse Position and Events

- [func areaOfInterest(forMouse: UIEvent) -> PDFAreaOfInterest](/documentation/pdfkit/pdfview/areaofinterest(formouse:))
- [func areaOfInterest(for: CGPoint) -> PDFAreaOfInterest](/documentation/pdfkit/pdfview/areaofinterest(for:))
- [PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest)

##### Constants

- [static var pageArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/pagearea)
- [static var textArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/textarea)
- [static var annotationArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/annotationarea)
- [static var linkArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/linkarea)
- [static var controlArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/controlarea)
- [static var textFieldArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/textfieldarea)
- [static var iconArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/iconarea)
- [static var popupArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/popuparea)
- [static var imageArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/imagearea)

##### Initializers

- [init(rawValue: Int)](/documentation/pdfkit/pdfareaofinterest/init(rawvalue:))

##### Type Properties

- [static var anyArea: PDFAreaOfInterest](/documentation/pdfkit/pdfareaofinterest/anyarea)
- [func setCursorFor(PDFAreaOfInterest)](/documentation/pdfkit/pdfview/setcursorfor(_:))
- [func perform(PDFAction)](/documentation/pdfkit/pdfview/perform(_:))
- [Drag Operations](/documentation/pdfkit/drag-operations)

##### Dragging in a View

- [var allowsDragging: Bool](/documentation/pdfkit/pdfview/allowsdragging)
- [var acceptsDraggedFiles: Bool](/documentation/pdfkit/pdfview/acceptsdraggedfiles)

### Navigating Within a Document

- [var currentPage: PDFPage?](/documentation/pdfkit/pdfview/currentpage)
- [var currentDestination: PDFDestination?](/documentation/pdfkit/pdfview/currentdestination)
- [var visiblePages: [PDFPage]](/documentation/pdfkit/pdfview/visiblepages)
- [Navigation](/documentation/pdfkit/navigation)

#### Determining Valid History Operations

- [var canGoBack: Bool](/documentation/pdfkit/pdfview/cangoback)
- [var canGoForward: Bool](/documentation/pdfkit/pdfview/cangoforward)
- [var canGoToFirstPage: Bool](/documentation/pdfkit/pdfview/cangotofirstpage)
- [var canGoToLastPage: Bool](/documentation/pdfkit/pdfview/cangotolastpage)
- [var canGoToNextPage: Bool](/documentation/pdfkit/pdfview/cangotonextpage)
- [var canGoToPreviousPage: Bool](/documentation/pdfkit/pdfview/cangotopreviouspage)

#### Navigating History for a Document

- [func goBack(Any?)](/documentation/pdfkit/pdfview/goback(_:))
- [func goForward(Any?)](/documentation/pdfkit/pdfview/goforward(_:))
- [func goToFirstPage(Any?)](/documentation/pdfkit/pdfview/gotofirstpage(_:))
- [func goToLastPage(Any?)](/documentation/pdfkit/pdfview/gotolastpage(_:))
- [func goToNextPage(Any?)](/documentation/pdfkit/pdfview/gotonextpage(_:))
- [func goToPreviousPage(Any?)](/documentation/pdfkit/pdfview/gotopreviouspage(_:))

#### Using Seek in a Document

- [func go(to: PDFPage)](/documentation/pdfkit/pdfview/go(to:)-6x8y2)
- [func go(to: PDFDestination)](/documentation/pdfkit/pdfview/go(to:)-5lh5d)
- [func go(to: PDFSelection)](/documentation/pdfkit/pdfview/go(to:)-3t5go)
- [func go(to: CGRect, on: PDFPage)](/documentation/pdfkit/pdfview/go(to:on:))

### Setting the Delegate

- [var delegate: (any PDFViewDelegate)?](/documentation/pdfkit/pdfview/delegate)
- [PDFViewDelegate](/documentation/pdfkit/pdfviewdelegate)

#### Working with Annotation Actions

- [func pdfViewPerformFind(PDFView)](/documentation/pdfkit/pdfviewdelegate/pdfviewperformfind(_:))
- [func pdfViewPerformGo(toPage: PDFView)](/documentation/pdfkit/pdfviewdelegate/pdfviewperformgo(topage:))
- [func pdfViewPerformPrint(PDFView)](/documentation/pdfkit/pdfviewdelegate/pdfviewperformprint(_:))
- [func pdfViewOpenPDF(PDFView, forRemoteGoToAction: PDFActionRemoteGoTo)](/documentation/pdfkit/pdfviewdelegate/pdfviewopenpdf(_:forremotegotoaction:))

#### Scaling the View

- [func pdfViewWillChangeScaleFactor(PDFView, toScale: CGFloat) -> CGFloat](/documentation/pdfkit/pdfviewdelegate/pdfviewwillchangescalefactor(_:toscale:))

#### Linking in a View

- [func pdfViewWillClick(onLink: PDFView, with: URL)](/documentation/pdfkit/pdfviewdelegate/pdfviewwillclick(onlink:with:))

#### Printing the View

- [func pdfViewPrintJobTitle(PDFView) -> String](/documentation/pdfkit/pdfviewdelegate/pdfviewprintjobtitle(_:))

#### Instance Methods

- [func pdfViewParentViewController() -> UIViewController](/documentation/pdfkit/pdfviewdelegate/pdfviewparentviewcontroller())

### Instance Properties

- [var findInteraction: UIFindInteraction](/documentation/pdfkit/pdfview/findinteraction)
- [var isFindInteractionEnabled: Bool](/documentation/pdfkit/pdfview/isfindinteractionenabled)
- [var isInMarkupMode: Bool](/documentation/pdfkit/pdfview/isinmarkupmode)
- [var pageOverlayViewProvider: (any PDFPageOverlayViewProvider)?](/documentation/pdfkit/pdfview/pageoverlayviewprovider)
- [var pageShadowsEnabled: Bool](/documentation/pdfkit/pdfview/pageshadowsenabled)
- [PDFThumbnailView](/documentation/pdfkit/pdfthumbnailview)

### Accessing the Associated PDF View

- [var pdfView: PDFView?](/documentation/pdfkit/pdfthumbnailview/pdfview)

### Managing the Size of a Thumbnail View

- [var thumbnailSize: CGSize](/documentation/pdfkit/pdfthumbnailview/thumbnailsize)

### Working with Thumbnail View Display Characteristics

- [var maximumNumberOfColumns: Int](/documentation/pdfkit/pdfthumbnailview/maximumnumberofcolumns)
- [var labelFont: NSFont?](/documentation/pdfkit/pdfthumbnailview/labelfont)
- [var backgroundColor: UIColor?](/documentation/pdfkit/pdfthumbnailview/backgroundcolor)

### Managing the Behavior of a Thumbnail View

- [var allowsDragging: Bool](/documentation/pdfkit/pdfthumbnailview/allowsdragging)
- [var allowsMultipleSelection: Bool](/documentation/pdfkit/pdfthumbnailview/allowsmultipleselection)
- [var selectedPages: [PDFPage]?](/documentation/pdfkit/pdfthumbnailview/selectedpages)

### Instance Properties

- [var contentInset: UIEdgeInsets](/documentation/pdfkit/pdfthumbnailview/contentinset)
- [var layoutMode: PDFThumbnailLayoutMode](/documentation/pdfkit/pdfthumbnailview/layoutmode)

## Content Model

- [PDFDocument](/documentation/pdfkit/pdfdocument)

### Initializing Documents

- [init?(url: URL)](/documentation/pdfkit/pdfdocument/init(url:))
- [init?(data: Data)](/documentation/pdfkit/pdfdocument/init(data:))
- [init()](/documentation/pdfkit/pdfdocument/init())

### Reading and Writing PDFs

- [Read Operations](/documentation/pdfkit/read-operations)

#### Accessing Document Information

- [var documentURL: URL?](/documentation/pdfkit/pdfdocument/documenturl)
- [var majorVersion: Int](/documentation/pdfkit/pdfdocument/majorversion)
- [var minorVersion: Int](/documentation/pdfkit/pdfdocument/minorversion)
- [var string: String?](/documentation/pdfkit/pdfdocument/string)
- [func outlineItem(for: PDFSelection) -> PDFOutline?](/documentation/pdfkit/pdfdocument/outlineitem(for:))
- [var outlineRoot: PDFOutline?](/documentation/pdfkit/pdfdocument/outlineroot)
- [var documentAttributes: [AnyHashable : Any]?](/documentation/pdfkit/pdfdocument/documentattributes)
- [var documentRef: CGPDFDocument?](/documentation/pdfkit/pdfdocument/documentref)

#### Managing Document Security

- [var isEncrypted: Bool](/documentation/pdfkit/pdfdocument/isencrypted)
- [var isLocked: Bool](/documentation/pdfkit/pdfdocument/islocked)
- [func unlock(withPassword: String) -> Bool](/documentation/pdfkit/pdfdocument/unlock(withpassword:))
- [var permissionsStatus: PDFDocumentPermissions](/documentation/pdfkit/pdfdocument/permissionsstatus)
- [Permission Properties](/documentation/pdfkit/permission-properties)

##### Getting Permissions

- [var allowsCopying: Bool](/documentation/pdfkit/pdfdocument/allowscopying)
- [var allowsPrinting: Bool](/documentation/pdfkit/pdfdocument/allowsprinting)
- [var allowsCommenting: Bool](/documentation/pdfkit/pdfdocument/allowscommenting)
- [var allowsContentAccessibility: Bool](/documentation/pdfkit/pdfdocument/allowscontentaccessibility)
- [var allowsDocumentAssembly: Bool](/documentation/pdfkit/pdfdocument/allowsdocumentassembly)
- [var allowsDocumentChanges: Bool](/documentation/pdfkit/pdfdocument/allowsdocumentchanges)
- [var allowsFormFieldEntry: Bool](/documentation/pdfkit/pdfdocument/allowsformfieldentry)

#### Working with Selections and Searches

- [func selection(from: PDFPage, atCharacterIndex: Int, to: PDFPage, atCharacterIndex: Int) -> PDFSelection?](/documentation/pdfkit/pdfdocument/selection(from:atcharacterindex:to:atcharacterindex:))
- [func selection(from: PDFPage, at: CGPoint, to: PDFPage, at: CGPoint) -> PDFSelection?](/documentation/pdfkit/pdfdocument/selection(from:at:to:at:))
- [var selectionForEntireDocument: PDFSelection?](/documentation/pdfkit/pdfdocument/selectionforentiredocument)
- [Search Operations](/documentation/pdfkit/search-operations)

##### Searching Documents

- [func findString(String, withOptions: NSString.CompareOptions) -> [PDFSelection]](/documentation/pdfkit/pdfdocument/findstring(_:withoptions:))
- [func beginFindString(String, withOptions: NSString.CompareOptions)](/documentation/pdfkit/pdfdocument/beginfindstring(_:withoptions:))
- [func beginFindStrings([String], withOptions: NSString.CompareOptions)](/documentation/pdfkit/pdfdocument/beginfindstrings(_:withoptions:))
- [func findString(String, fromSelection: PDFSelection?, withOptions: NSString.CompareOptions) -> PDFSelection?](/documentation/pdfkit/pdfdocument/findstring(_:fromselection:withoptions:))
- [var isFinding: Bool](/documentation/pdfkit/pdfdocument/isfinding)
- [func cancelFindString()](/documentation/pdfkit/pdfdocument/cancelfindstring())

#### Working with Pages

- [var pageCount: Int](/documentation/pdfkit/pdfdocument/pagecount)
- [func page(at: Int) -> PDFPage?](/documentation/pdfkit/pdfdocument/page(at:))
- [func index(for: PDFPage) -> Int](/documentation/pdfkit/pdfdocument/index(for:))
- [func insert(PDFPage, at: Int)](/documentation/pdfkit/pdfdocument/insert(_:at:))
- [func removePage(at: Int)](/documentation/pdfkit/pdfdocument/removepage(at:))
- [func exchangePage(at: Int, withPageAt: Int)](/documentation/pdfkit/pdfdocument/exchangepage(at:withpageat:))
- [var pageClass: AnyClass](/documentation/pdfkit/pdfdocument/pageclass)
- [Write Operations](/documentation/pdfkit/write-operations)

#### Writing Out the PDF Data

- [func write(toFile: String) -> Bool](/documentation/pdfkit/pdfdocument/write(tofile:))
- [func write(toFile: String, withOptions: [PDFDocumentWriteOption : Any]?) -> Bool](/documentation/pdfkit/pdfdocument/write(tofile:withoptions:))
- [func write(to: URL) -> Bool](/documentation/pdfkit/pdfdocument/write(to:))
- [func write(to: URL, withOptions: [PDFDocumentWriteOption : Any]?) -> Bool](/documentation/pdfkit/pdfdocument/write(to:withoptions:))
- [Data Representations](/documentation/pdfkit/data-representations)

##### Creating Data Representations

- [func dataRepresentation() -> Data?](/documentation/pdfkit/pdfdocument/datarepresentation())
- [func dataRepresentation(options: [AnyHashable : Any]) -> Data?](/documentation/pdfkit/pdfdocument/datarepresentation(options:))

#### Printing Documents for macOS

- [func printOperation(for: NSPrintInfo?, scalingMode: PDFPrintScalingMode, autoRotate: Bool) -> NSPrintOperation?](/documentation/pdfkit/pdfdocument/printoperation(for:scalingmode:autorotate:))
- [PDFPrintScalingMode](/documentation/pdfkit/pdfprintscalingmode)

##### Enumeration Cases

- [case pageScaleDownToFit](/documentation/pdfkit/pdfprintscalingmode/pagescaledowntofit)
- [case pageScaleNone](/documentation/pdfkit/pdfprintscalingmode/pagescalenone)
- [case pageScaleToFit](/documentation/pdfkit/pdfprintscalingmode/pagescaletofit)

##### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfprintscalingmode/init(rawvalue:))

### Setting the Delegate

- [var delegate: (any PDFDocumentDelegate)?](/documentation/pdfkit/pdfdocument/delegate)
- [PDFDocumentDelegate](/documentation/pdfkit/pdfdocumentdelegate)

#### Managing Document Security

- [func documentDidUnlock(Notification)](/documentation/pdfkit/pdfdocumentdelegate/documentdidunlock(_:))

#### Getting Document Search Notifications

- [func didMatchString(PDFSelection)](/documentation/pdfkit/pdfdocumentdelegate/didmatchstring(_:))
- [func documentDidBeginDocumentFind(Notification)](/documentation/pdfkit/pdfdocumentdelegate/documentdidbegindocumentfind(_:))
- [func documentDidBeginPageFind(Notification)](/documentation/pdfkit/pdfdocumentdelegate/documentdidbeginpagefind(_:))
- [func documentDidEndDocumentFind(Notification)](/documentation/pdfkit/pdfdocumentdelegate/documentdidenddocumentfind(_:))
- [func documentDidEndPageFind(Notification)](/documentation/pdfkit/pdfdocumentdelegate/documentdidendpagefind(_:))
- [func documentDidFindMatch(Notification)](/documentation/pdfkit/pdfdocumentdelegate/documentdidfindmatch(_:))

#### Wrapping Document Elements

- [func classForPage() -> AnyClass](/documentation/pdfkit/pdfdocumentdelegate/classforpage())
- [func `class`(forAnnotationClass: AnyClass) -> AnyClass](/documentation/pdfkit/pdfdocumentdelegate/class(forannotationclass:))
- [func `class`(forAnnotationType: String) -> AnyClass](/documentation/pdfkit/pdfdocumentdelegate/class(forannotationtype:))

### Constants

- [PDFDocumentPermissions](/documentation/pdfkit/pdfdocumentpermissions)

#### Enumeration Cases

- [case none](/documentation/pdfkit/pdfdocumentpermissions/none)
- [case user](/documentation/pdfkit/pdfdocumentpermissions/user)
- [case owner](/documentation/pdfkit/pdfdocumentpermissions/owner)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfdocumentpermissions/init(rawvalue:))
- [PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute)

#### Creating Document Attributes

- [init(rawValue: String)](/documentation/pdfkit/pdfdocumentattribute/init(rawvalue:))

#### Getting Document Attributes

- [static let authorAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/authorattribute)
- [static let creationDateAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/creationdateattribute)
- [static let creatorAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/creatorattribute)
- [static let keywordsAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/keywordsattribute)
- [static let modificationDateAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/modificationdateattribute)
- [static let producerAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/producerattribute)
- [static let subjectAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/subjectattribute)
- [static let titleAttribute: PDFDocumentAttribute](/documentation/pdfkit/pdfdocumentattribute/titleattribute)
- [PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption)

#### Creating Write Options

- [init(rawValue: String)](/documentation/pdfkit/pdfdocumentwriteoption/init(rawvalue:))

#### Getting Write Option Properties

- [static let ownerPasswordOption: PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption/ownerpasswordoption)
- [static let userPasswordOption: PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption/userpasswordoption)

#### Type Properties

- [static let accessPermissionsOption: PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption/accesspermissionsoption)
- [static let burnInAnnotationsOption: PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption/burninannotationsoption)
- [static let optimizeImagesForScreenOption: PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption/optimizeimagesforscreenoption)
- [static let saveImagesAsJPEGOption: PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption/saveimagesasjpegoption)
- [static let saveTextFromOCROption: PDFDocumentWriteOption](/documentation/pdfkit/pdfdocumentwriteoption/savetextfromocroption)

### Instance Properties

- [var accessPermissions: PDFAccessPermissions](/documentation/pdfkit/pdfdocument/accesspermissions)

### Instance Methods

- [func selection(from: PDFPage, at: CGPoint, to: PDFPage, at: CGPoint, with: PDFSelectionGranularity) -> PDFSelection?](/documentation/pdfkit/pdfdocument/selection(from:at:to:at:with:))
- [PDFPage](/documentation/pdfkit/pdfpage)

### Initializing a Page

- [convenience init?(image: UIImage)](/documentation/pdfkit/pdfpage/init(image:))

### Getting Information About a Page

- [var document: PDFDocument?](/documentation/pdfkit/pdfpage/document)
- [var label: String?](/documentation/pdfkit/pdfpage/label)
- [func bounds(for: PDFDisplayBox) -> CGRect](/documentation/pdfkit/pdfpage/bounds(for:))
- [func setBounds(CGRect, for: PDFDisplayBox)](/documentation/pdfkit/pdfpage/setbounds(_:for:))
- [var rotation: Int](/documentation/pdfkit/pdfpage/rotation)

### Working with Annotations

- [var annotations: [PDFAnnotation]](/documentation/pdfkit/pdfpage/annotations)
- [var displaysAnnotations: Bool](/documentation/pdfkit/pdfpage/displaysannotations)
- [func addAnnotation(PDFAnnotation)](/documentation/pdfkit/pdfpage/addannotation(_:))
- [func removeAnnotation(PDFAnnotation)](/documentation/pdfkit/pdfpage/removeannotation(_:))
- [func annotation(at: CGPoint) -> PDFAnnotation?](/documentation/pdfkit/pdfpage/annotation(at:))

### Rendering Pages

- [func draw(with: PDFDisplayBox)](/documentation/pdfkit/pdfpage/draw(with:))
- [func transformContext(for: PDFDisplayBox)](/documentation/pdfkit/pdfpage/transformcontext(for:))

### Working with Textual Content

- [var numberOfCharacters: Int](/documentation/pdfkit/pdfpage/numberofcharacters)
- [var string: String?](/documentation/pdfkit/pdfpage/string)
- [var attributedString: NSAttributedString?](/documentation/pdfkit/pdfpage/attributedstring)
- [func characterBounds(at: Int) -> CGRect](/documentation/pdfkit/pdfpage/characterbounds(at:))
- [func characterIndex(at: CGPoint) -> Int](/documentation/pdfkit/pdfpage/characterindex(at:))

### Working with Selections

- [func selection(for: CGRect) -> PDFSelection?](/documentation/pdfkit/pdfpage/selection(for:)-2ckpi)
- [func selectionForWord(at: CGPoint) -> PDFSelection?](/documentation/pdfkit/pdfpage/selectionforword(at:))
- [func selectionForLine(at: CGPoint) -> PDFSelection?](/documentation/pdfkit/pdfpage/selectionforline(at:))
- [func selection(from: CGPoint, to: CGPoint) -> PDFSelection?](/documentation/pdfkit/pdfpage/selection(from:to:))
- [func selection(for: NSRange) -> PDFSelection?](/documentation/pdfkit/pdfpage/selection(for:)-20y9d)

### Supporting Types

- [PDFDisplayBox](/documentation/pdfkit/pdfdisplaybox)

#### Constants

- [case mediaBox](/documentation/pdfkit/pdfdisplaybox/mediabox)
- [case cropBox](/documentation/pdfkit/pdfdisplaybox/cropbox)
- [case bleedBox](/documentation/pdfkit/pdfdisplaybox/bleedbox)
- [case trimBox](/documentation/pdfkit/pdfdisplaybox/trimbox)
- [case artBox](/documentation/pdfkit/pdfdisplaybox/artbox)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfdisplaybox/init(rawvalue:))
- [PDFDisplayDirection](/documentation/pdfkit/pdfdisplaydirection)

#### Enumeration Cases

- [case horizontal](/documentation/pdfkit/pdfdisplaydirection/horizontal)
- [case vertical](/documentation/pdfkit/pdfdisplaydirection/vertical)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfdisplaydirection/init(rawvalue:))

### Type Aliases

- [PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption)

#### Initializers

- [init(rawValue: String)](/documentation/pdfkit/pdfpage/imageinitializationoption/init(rawvalue:))

#### Type Properties

- [static let compressionQuality: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/compressionquality)
- [static let mediaBox: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/mediabox)
- [static let rotation: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/rotation)
- [static let upscaleIfSmaller: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/upscaleifsmaller)
- [static let compressionQuality: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/compressionquality)
- [static let mediaBox: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/mediabox)
- [static let rotation: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/rotation)
- [static let upscaleIfSmaller: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/upscaleifsmaller)

### Initializers

- [init()](/documentation/pdfkit/pdfpage/init())
- [init?(image: UIImage, options: [PDFPage.ImageInitializationOption : Any])](/documentation/pdfkit/pdfpage/init(image:options:))

### Instance Properties

- [var dataRepresentation: Data?](/documentation/pdfkit/pdfpage/datarepresentation)
- [var pageRef: CGPDFPage?](/documentation/pdfkit/pdfpage/pageref)

### Instance Methods

- [func draw(with: PDFDisplayBox, to: CGContext)](/documentation/pdfkit/pdfpage/draw(with:to:))
- [func thumbnail(of: CGSize, for: PDFDisplayBox) -> UIImage](/documentation/pdfkit/pdfpage/thumbnail(of:for:))
- [func transform(CGContext, for: PDFDisplayBox)](/documentation/pdfkit/pdfpage/transform(_:for:))
- [func transform(for: PDFDisplayBox) -> CGAffineTransform](/documentation/pdfkit/pdfpage/transform(for:))
- [PDFOutline](/documentation/pdfkit/pdfoutline)

### Initializing an Outline

- [init()](/documentation/pdfkit/pdfoutline/init())

### Getting Information About an Outline

- [var document: PDFDocument?](/documentation/pdfkit/pdfoutline/document)
- [var numberOfChildren: Int](/documentation/pdfkit/pdfoutline/numberofchildren)
- [var parent: PDFOutline?](/documentation/pdfkit/pdfoutline/parent)
- [func child(at: Int) -> PDFOutline?](/documentation/pdfkit/pdfoutline/child(at:))
- [var index: Int](/documentation/pdfkit/pdfoutline/index)

### Managing Outline Labels

- [var label: String?](/documentation/pdfkit/pdfoutline/label)

### Managing Actions and Destinations

- [var destination: PDFDestination?](/documentation/pdfkit/pdfoutline/destination)
- [var action: PDFAction?](/documentation/pdfkit/pdfoutline/action)

### Changing an Outline Hierarchy

- [func insertChild(PDFOutline, at: Int)](/documentation/pdfkit/pdfoutline/insertchild(_:at:))
- [func removeFromParent()](/documentation/pdfkit/pdfoutline/removefromparent())

### Managing the Disclosure of an Outline Object

- [var isOpen: Bool](/documentation/pdfkit/pdfoutline/isopen)
- [PDFSelection](/documentation/pdfkit/pdfselection)

### Initializing a Selection

- [init(document: PDFDocument)](/documentation/pdfkit/pdfselection/init(document:))

### Getting Information About a Selection

- [var pages: [PDFPage]](/documentation/pdfkit/pdfselection/pages)
- [var string: String?](/documentation/pdfkit/pdfselection/string)
- [var attributedString: NSAttributedString?](/documentation/pdfkit/pdfselection/attributedstring)
- [func bounds(for: PDFPage) -> CGRect](/documentation/pdfkit/pdfselection/bounds(for:))
- [func selectionsByLine() -> [PDFSelection]](/documentation/pdfkit/pdfselection/selectionsbyline())
- [var color: UIColor?](/documentation/pdfkit/pdfselection/color)

### Modifying a Selection

- [func add(PDFSelection)](/documentation/pdfkit/pdfselection/add(_:)-8c2r)
- [func add([PDFSelection])](/documentation/pdfkit/pdfselection/add(_:)-3fyld)
- [func extend(atEnd: Int)](/documentation/pdfkit/pdfselection/extend(atend:))
- [func extend(atStart: Int)](/documentation/pdfkit/pdfselection/extend(atstart:))

### Managing Selection Drawing

- [func draw(for: PDFPage, active: Bool)](/documentation/pdfkit/pdfselection/draw(for:active:))
- [func draw(for: PDFPage, with: PDFDisplayBox, active: Bool)](/documentation/pdfkit/pdfselection/draw(for:with:active:))
- [var color: UIColor?](/documentation/pdfkit/pdfselection/color)

### Instance Methods

- [func extendForLineBoundaries()](/documentation/pdfkit/pdfselection/extendforlineboundaries())
- [func numberOfTextRanges(on: PDFPage) -> Int](/documentation/pdfkit/pdfselection/numberoftextranges(on:))
- [func range(at: Int, on: PDFPage) -> NSRange](/documentation/pdfkit/pdfselection/range(at:on:))

## Annotations

- [Adding Widgets to a PDF Document](/documentation/pdfkit/adding-widgets-to-a-pdf-document)
- [Adding Custom Graphics to a PDF](/documentation/pdfkit/adding-custom-graphics-to-a-pdf)
- [Custom Graphics](/documentation/pdfkit/custom-graphics)
- [PDF Widgets](/documentation/pdfkit/pdf-widgets)
- [PDFAnnotation](/documentation/pdfkit/pdfannotation)

### Creating an Annotation

- [init(bounds: CGRect, forType: PDFAnnotationSubtype, withProperties: [AnyHashable : Any]?)](/documentation/pdfkit/pdfannotation/init(bounds:fortype:withproperties:))
- [PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype)

#### Choosing an Annotation Subtype

- [static let circle: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/circle)
- [static let freeText: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/freetext)
- [static let highlight: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/highlight)
- [static let ink: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/ink)
- [static let line: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/line)
- [static let link: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/link)
- [static let popup: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/popup)
- [static let square: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/square)
- [static let stamp: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/stamp)
- [static let strikeOut: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/strikeout)
- [static let text: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/text)
- [static let underline: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/underline)
- [static let widget: PDFAnnotationSubtype](/documentation/pdfkit/pdfannotationsubtype/widget)

#### Creating an Annotation Subtype

- [init(rawValue: String)](/documentation/pdfkit/pdfannotationsubtype/init(rawvalue:))

### Accessing Information About an Annotation

- [var page: PDFPage?](/documentation/pdfkit/pdfannotation/page)
- [var modificationDate: Date?](/documentation/pdfkit/pdfannotation/modificationdate)
- [var userName: String?](/documentation/pdfkit/pdfannotation/username)
- [var type: String?](/documentation/pdfkit/pdfannotation/type)
- [var action: PDFAction?](/documentation/pdfkit/pdfannotation/action)
- [PDFAction](/documentation/pdfkit/pdfaction)

#### Action Types

- [PDFActionGoTo](/documentation/pdfkit/pdfactiongoto)

##### Accessing the Destination

- [var destination: PDFDestination](/documentation/pdfkit/pdfactiongoto/destination)

##### Initializing the Action

- [init(destination: PDFDestination)](/documentation/pdfkit/pdfactiongoto/init(destination:))
- [PDFActionNamed](/documentation/pdfkit/pdfactionnamed)

##### Accessing the Name of the Action

- [var name: PDFActionNamedName](/documentation/pdfkit/pdfactionnamed/name)

##### Initializing the Action

- [init(name: PDFActionNamedName)](/documentation/pdfkit/pdfactionnamed/init(name:))
- [PDFActionRemoteGoTo](/documentation/pdfkit/pdfactionremotegoto)

##### Initializing the Remote Go-to Action

- [init(pageIndex: Int, at: CGPoint, fileURL: URL)](/documentation/pdfkit/pdfactionremotegoto/init(pageindex:at:fileurl:))

##### Accessing the Page Index of the Referenced Document

- [var pageIndex: Int](/documentation/pdfkit/pdfactionremotegoto/pageindex)

##### Accessing a Point on the Referenced Page

- [var point: CGPoint](/documentation/pdfkit/pdfactionremotegoto/point)

##### Accessing the URL of the Referenced Document

- [var url: URL](/documentation/pdfkit/pdfactionremotegoto/url)
- [PDFActionResetForm](/documentation/pdfkit/pdfactionresetform)

##### Initializing a Reset Form Action

- [init()](/documentation/pdfkit/pdfactionresetform/init())

##### Accessing and Changing Fields

- [var fields: [String]?](/documentation/pdfkit/pdfactionresetform/fields)

##### Determining Whether Fields are Cleared When the Action is Performed

- [var fieldsIncludedAreCleared: Bool](/documentation/pdfkit/pdfactionresetform/fieldsincludedarecleared)
- [PDFActionURL](/documentation/pdfkit/pdfactionurl)

##### Initializing a URL Action

- [init(url: URL)](/documentation/pdfkit/pdfactionurl/init(url:))

##### Accessing and Changing the URL

- [var url: URL?](/documentation/pdfkit/pdfactionurl/url)
- [PDFActionNamedName](/documentation/pdfkit/pdfactionnamedname)

##### Constants

- [case find](/documentation/pdfkit/pdfactionnamedname/find)
- [case firstPage](/documentation/pdfkit/pdfactionnamedname/firstpage)
- [case goBack](/documentation/pdfkit/pdfactionnamedname/goback)
- [case goForward](/documentation/pdfkit/pdfactionnamedname/goforward)
- [case goToPage](/documentation/pdfkit/pdfactionnamedname/gotopage)
- [case lastPage](/documentation/pdfkit/pdfactionnamedname/lastpage)
- [case nextPage](/documentation/pdfkit/pdfactionnamedname/nextpage)
- [case none](/documentation/pdfkit/pdfactionnamedname/none)
- [case previousPage](/documentation/pdfkit/pdfactionnamedname/previouspage)
- [case print](/documentation/pdfkit/pdfactionnamedname/print)
- [case zoomIn](/documentation/pdfkit/pdfactionnamedname/zoomin)
- [case zoomOut](/documentation/pdfkit/pdfactionnamedname/zoomout)

##### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfactionnamedname/init(rawvalue:))

#### Getting the Action Type

- [var type: String](/documentation/pdfkit/pdfaction/type)
- [PDFDestination](/documentation/pdfkit/pdfdestination)

#### Initializing a Destination

- [init(page: PDFPage, at: CGPoint)](/documentation/pdfkit/pdfdestination/init(page:at:))

#### Getting Pages and Points

- [var page: PDFPage?](/documentation/pdfkit/pdfdestination/page)
- [var point: CGPoint](/documentation/pdfkit/pdfdestination/point)
- [let kPDFDestinationUnspecifiedValue: CGFloat](/documentation/pdfkit/kpdfdestinationunspecifiedvalue)

#### Getting a Relative Location

- [func compare(PDFDestination) -> ComparisonResult](/documentation/pdfkit/pdfdestination/compare(_:))

#### Instance Properties

- [var zoom: CGFloat](/documentation/pdfkit/pdfdestination/zoom)

### Managing Annotation Drawing and Output

- [func draw(with: PDFDisplayBox, in: CGContext)](/documentation/pdfkit/pdfannotation/draw(with:in:))
- [var shouldDisplay: Bool](/documentation/pdfkit/pdfannotation/shoulddisplay)
- [var shouldPrint: Bool](/documentation/pdfkit/pdfannotation/shouldprint)

### Modifying Annotation Attributes

- [var annotationKeyValues: [AnyHashable : Any]](/documentation/pdfkit/pdfannotation/annotationkeyvalues)
- [func value(forAnnotationKey: PDFAnnotationKey) -> Any?](/documentation/pdfkit/pdfannotation/value(forannotationkey:))
- [func setValue(Any, forAnnotationKey: PDFAnnotationKey) -> Bool](/documentation/pdfkit/pdfannotation/setvalue(_:forannotationkey:))
- [func setBoolean(Bool, forAnnotationKey: PDFAnnotationKey) -> Bool](/documentation/pdfkit/pdfannotation/setboolean(_:forannotationkey:))
- [func setRect(CGRect, forAnnotationKey: PDFAnnotationKey) -> Bool](/documentation/pdfkit/pdfannotation/setrect(_:forannotationkey:))
- [func removeValue(forAnnotationKey: PDFAnnotationKey)](/documentation/pdfkit/pdfannotation/removevalue(forannotationkey:))
- [PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey)

#### Configuring General Properties

- [static let contents: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/contents)
- [static let date: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/date)
- [static let flags: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/flags)
- [static let name: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/name)
- [static let page: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/page)
- [static let parent: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/parent)
- [static let quadPoints: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/quadpoints)
- [static let rect: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/rect)
- [static let subtype: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/subtype)
- [static let textLabel: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/textlabel)

#### Configuring Annotation Appearance

- [static let appearanceDictionary: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/appearancedictionary)
- [static let appearanceState: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/appearancestate)
- [static let border: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/border)
- [static let borderStyle: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/borderstyle)
- [static let color: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/color)
- [static let defaultAppearance: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/defaultappearance)
- [static let highlightingMode: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/highlightingmode)
- [PDFAnnotationHighlightingMode](/documentation/pdfkit/pdfannotationhighlightingmode)

##### Choosing a Highlight Mode

- [static let invert: PDFAnnotationHighlightingMode](/documentation/pdfkit/pdfannotationhighlightingmode/invert)
- [static let none: PDFAnnotationHighlightingMode](/documentation/pdfkit/pdfannotationhighlightingmode/none)
- [static let outline: PDFAnnotationHighlightingMode](/documentation/pdfkit/pdfannotationhighlightingmode/outline)
- [static let push: PDFAnnotationHighlightingMode](/documentation/pdfkit/pdfannotationhighlightingmode/push)

##### Creating an Annotation Highlight Mode

- [init(rawValue: String)](/documentation/pdfkit/pdfannotationhighlightingmode/init(rawvalue:))
- [static let iconName: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/iconname)
- [static let interiorColor: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/interiorcolor)
- [static let quadding: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/quadding)

#### Configuring Line Properties

- [static let lineEndingStyles: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/lineendingstyles)
- [PDFLineStyle](/documentation/pdfkit/pdflinestyle)

##### Constants

- [case none](/documentation/pdfkit/pdflinestyle/none)
- [case square](/documentation/pdfkit/pdflinestyle/square)
- [case circle](/documentation/pdfkit/pdflinestyle/circle)
- [case diamond](/documentation/pdfkit/pdflinestyle/diamond)
- [case openArrow](/documentation/pdfkit/pdflinestyle/openarrow)
- [case closedArrow](/documentation/pdfkit/pdflinestyle/closedarrow)

##### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdflinestyle/init(rawvalue:))
- [static let linePoints: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/linepoints)
- [PDFAnnotationLineEndingStyle](/documentation/pdfkit/pdfannotationlineendingstyle)

##### Choosing a Line-Ending Style

- [static let circle: PDFAnnotationLineEndingStyle](/documentation/pdfkit/pdfannotationlineendingstyle/circle)
- [static let closedArrow: PDFAnnotationLineEndingStyle](/documentation/pdfkit/pdfannotationlineendingstyle/closedarrow)
- [static let diamond: PDFAnnotationLineEndingStyle](/documentation/pdfkit/pdfannotationlineendingstyle/diamond)
- [static let none: PDFAnnotationLineEndingStyle](/documentation/pdfkit/pdfannotationlineendingstyle/none)
- [static let openArrow: PDFAnnotationLineEndingStyle](/documentation/pdfkit/pdfannotationlineendingstyle/openarrow)
- [static let square: PDFAnnotationLineEndingStyle](/documentation/pdfkit/pdfannotationlineendingstyle/square)

##### Creating a Line-Ending Style

- [init(rawValue: String)](/documentation/pdfkit/pdfannotationlineendingstyle/init(rawvalue:))

#### Configuring Pop-Up Annotations

- [static let popup: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/popup)
- [static let open: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/open)

#### Configuring Widget Annotations

- [static let widgetAppearanceDictionary: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetappearancedictionary)
- [static let widgetBackgroundColor: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetbackgroundcolor)
- [static let widgetBorderColor: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetbordercolor)
- [static let widgetCaption: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetcaption)
- [static let widgetDefaultValue: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetdefaultvalue)
- [static let widgetDownCaption: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetdowncaption)
- [static let widgetFieldFlags: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetfieldflags)
- [static let widgetFieldType: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetfieldtype)
- [static let widgetMaxLen: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetmaxlen)
- [static let widgetOptions: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetoptions)
- [static let widgetRolloverCaption: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetrollovercaption)
- [static let widgetRotation: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetrotation)
- [static let widgetTextLabelUI: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgettextlabelui)
- [static let widgetValue: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/widgetvalue)
- [PDFAnnotationWidgetSubtype](/documentation/pdfkit/pdfannotationwidgetsubtype)

##### Configuring a Widget Subtype

- [static let button: PDFAnnotationWidgetSubtype](/documentation/pdfkit/pdfannotationwidgetsubtype/button)
- [static let choice: PDFAnnotationWidgetSubtype](/documentation/pdfkit/pdfannotationwidgetsubtype/choice)
- [static let signature: PDFAnnotationWidgetSubtype](/documentation/pdfkit/pdfannotationwidgetsubtype/signature)
- [static let text: PDFAnnotationWidgetSubtype](/documentation/pdfkit/pdfannotationwidgetsubtype/text)

##### Creating a Widget Subtype

- [init(rawValue: String)](/documentation/pdfkit/pdfannotationwidgetsubtype/init(rawvalue:))

#### Configuring Actions

- [static let destination: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/destination)
- [static let action: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/action)
- [static let additionalActions: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/additionalactions)

#### Configuring Ink Annotations

- [static let inklist: PDFAnnotationKey](/documentation/pdfkit/pdfannotationkey/inklist)

#### Creating an Annotation Key

- [init(rawValue: String)](/documentation/pdfkit/pdfannotationkey/init(rawvalue:))

### Managing Annotation Display Characteristics

- [var alignment: NSTextAlignment](/documentation/pdfkit/pdfannotation/alignment)
- [var bounds: CGRect](/documentation/pdfkit/pdfannotation/bounds)
- [var contents: String?](/documentation/pdfkit/pdfannotation/contents)
- [var font: UIFont?](/documentation/pdfkit/pdfannotation/font)
- [var fontColor: UIColor?](/documentation/pdfkit/pdfannotation/fontcolor)
- [var border: PDFBorder?](/documentation/pdfkit/pdfannotation/border)
- [PDFBorder](/documentation/pdfkit/pdfborder)

#### Working with Border Styles and Characteristics

- [var style: PDFBorderStyle](/documentation/pdfkit/pdfborder/style)
- [PDFBorderStyle](/documentation/pdfkit/pdfborderstyle)

##### Constants

- [case solid](/documentation/pdfkit/pdfborderstyle/solid)
- [case dashed](/documentation/pdfkit/pdfborderstyle/dashed)
- [case beveled](/documentation/pdfkit/pdfborderstyle/beveled)
- [case inset](/documentation/pdfkit/pdfborderstyle/inset)
- [case underline](/documentation/pdfkit/pdfborderstyle/underline)

##### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfborderstyle/init(rawvalue:))
- [var lineWidth: CGFloat](/documentation/pdfkit/pdfborder/linewidth)
- [var dashPattern: [Any]?](/documentation/pdfkit/pdfborder/dashpattern)
- [var borderKeyValues: [AnyHashable : Any]](/documentation/pdfkit/pdfborder/borderkeyvalues)
- [PDFBorderKey](/documentation/pdfkit/pdfborderkey)

##### Initializers

- [init(rawValue: String)](/documentation/pdfkit/pdfborderkey/init(rawvalue:))

##### Type Properties

- [static let dashPattern: PDFBorderKey](/documentation/pdfkit/pdfborderkey/dashpattern)
- [static let lineWidth: PDFBorderKey](/documentation/pdfkit/pdfborderkey/linewidth)
- [static let style: PDFBorderKey](/documentation/pdfkit/pdfborderkey/style)

#### Drawing Borders

- [func draw(in: CGRect)](/documentation/pdfkit/pdfborder/draw(in:))
- [var isHighlighted: Bool](/documentation/pdfkit/pdfannotation/ishighlighted)
- [var color: UIColor](/documentation/pdfkit/pdfannotation/color)
- [var hasAppearanceStream: Bool](/documentation/pdfkit/pdfannotation/hasappearancestream)

### Configuring Shape Annotations

- [var interiorColor: UIColor?](/documentation/pdfkit/pdfannotation/interiorcolor)

### Configuring Line Annotations

- [var startPoint: CGPoint](/documentation/pdfkit/pdfannotation/startpoint)
- [var endPoint: CGPoint](/documentation/pdfkit/pdfannotation/endpoint)
- [var startLineStyle: PDFLineStyle](/documentation/pdfkit/pdfannotation/startlinestyle)
- [var endLineStyle: PDFLineStyle](/documentation/pdfkit/pdfannotation/endlinestyle)
- [class func lineStyle(fromName: String) -> PDFLineStyle](/documentation/pdfkit/pdfannotation/linestyle(fromname:))
- [class func name(for: PDFLineStyle) -> String](/documentation/pdfkit/pdfannotation/name(for:))

### Configuring Link Annotations

- [var destination: PDFDestination?](/documentation/pdfkit/pdfannotation/destination)
- [var url: URL?](/documentation/pdfkit/pdfannotation/url)

### Configuring Text Annotations

- [var iconType: PDFTextAnnotationIconType](/documentation/pdfkit/pdfannotation/icontype)
- [PDFTextAnnotationIconType](/documentation/pdfkit/pdftextannotationicontype)

#### Constants

- [case comment](/documentation/pdfkit/pdftextannotationicontype/comment)
- [case key](/documentation/pdfkit/pdftextannotationicontype/key)
- [case note](/documentation/pdfkit/pdftextannotationicontype/note)
- [case help](/documentation/pdfkit/pdftextannotationicontype/help)
- [case newParagraph](/documentation/pdfkit/pdftextannotationicontype/newparagraph)
- [case paragraph](/documentation/pdfkit/pdftextannotationicontype/paragraph)
- [case insert](/documentation/pdfkit/pdftextannotationicontype/insert)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdftextannotationicontype/init(rawvalue:))
- [PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype)

#### Choosing a Text Icon Type

- [static let comment: PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype/comment)
- [static let key: PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype/key)
- [static let note: PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype/note)
- [static let help: PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype/help)
- [static let newParagraph: PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype/newparagraph)
- [static let paragraph: PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype/paragraph)
- [static let insert: PDFAnnotationTextIconType](/documentation/pdfkit/pdfannotationtexticontype/insert)

#### Creating a Text Icon Type

- [init(rawValue: String)](/documentation/pdfkit/pdfannotationtexticontype/init(rawvalue:))

### Configuring Pop-Up Annotations

- [var popup: PDFAnnotation?](/documentation/pdfkit/pdfannotation/popup)
- [var isOpen: Bool](/documentation/pdfkit/pdfannotation/isopen)

### Configuring Text Markup Annotations

- [var markupType: PDFMarkupType](/documentation/pdfkit/pdfannotation/markuptype)
- [PDFMarkupType](/documentation/pdfkit/pdfmarkuptype)

#### Constants

- [case highlight](/documentation/pdfkit/pdfmarkuptype/highlight)
- [case strikeOut](/documentation/pdfkit/pdfmarkuptype/strikeout)
- [case underline](/documentation/pdfkit/pdfmarkuptype/underline)
- [case redact](/documentation/pdfkit/pdfmarkuptype/redact)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfmarkuptype/init(rawvalue:))
- [var quadrilateralPoints: [NSValue]?](/documentation/pdfkit/pdfannotation/quadrilateralpoints)

### Configuring Widget Annotations

- [var widgetFieldType: PDFAnnotationWidgetSubtype](/documentation/pdfkit/pdfannotation/widgetfieldtype)
- [var widgetStringValue: String?](/documentation/pdfkit/pdfannotation/widgetstringvalue)
- [var widgetDefaultStringValue: String?](/documentation/pdfkit/pdfannotation/widgetdefaultstringvalue)
- [var fieldName: String?](/documentation/pdfkit/pdfannotation/fieldname)
- [var backgroundColor: UIColor?](/documentation/pdfkit/pdfannotation/backgroundcolor)
- [var isReadOnly: Bool](/documentation/pdfkit/pdfannotation/isreadonly)
- [PDFWidgetControlType](/documentation/pdfkit/pdfwidgetcontroltype)

#### Constants

- [case unknownControl](/documentation/pdfkit/pdfwidgetcontroltype/unknowncontrol)
- [case pushButtonControl](/documentation/pdfkit/pdfwidgetcontroltype/pushbuttoncontrol)
- [case radioButtonControl](/documentation/pdfkit/pdfwidgetcontroltype/radiobuttoncontrol)
- [case checkBoxControl](/documentation/pdfkit/pdfwidgetcontroltype/checkboxcontrol)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfwidgetcontroltype/init(rawvalue:))
- [PDFAppearanceCharacteristics](/documentation/pdfkit/pdfappearancecharacteristics)

#### Configuring a Widget’s Appearance

- [var backgroundColor: UIColor?](/documentation/pdfkit/pdfappearancecharacteristics/backgroundcolor)
- [var borderColor: UIColor?](/documentation/pdfkit/pdfappearancecharacteristics/bordercolor)
- [var caption: String?](/documentation/pdfkit/pdfappearancecharacteristics/caption)
- [var controlType: PDFWidgetControlType](/documentation/pdfkit/pdfappearancecharacteristics/controltype)
- [var downCaption: String?](/documentation/pdfkit/pdfappearancecharacteristics/downcaption)
- [var rolloverCaption: String?](/documentation/pdfkit/pdfappearancecharacteristics/rollovercaption)
- [var rotation: Int](/documentation/pdfkit/pdfappearancecharacteristics/rotation)
- [var appearanceCharacteristicsKeyValues: [AnyHashable : Any]](/documentation/pdfkit/pdfappearancecharacteristics/appearancecharacteristicskeyvalues)
- [PDFAppearanceCharacteristicsKey](/documentation/pdfkit/pdfappearancecharacteristicskey)

##### Modifying Widget Appearance

- [static let backgroundColor: PDFAppearanceCharacteristicsKey](/documentation/pdfkit/pdfappearancecharacteristicskey/backgroundcolor)
- [static let borderColor: PDFAppearanceCharacteristicsKey](/documentation/pdfkit/pdfappearancecharacteristicskey/bordercolor)
- [static let caption: PDFAppearanceCharacteristicsKey](/documentation/pdfkit/pdfappearancecharacteristicskey/caption)
- [static let downCaption: PDFAppearanceCharacteristicsKey](/documentation/pdfkit/pdfappearancecharacteristicskey/downcaption)
- [static let rolloverCaption: PDFAppearanceCharacteristicsKey](/documentation/pdfkit/pdfappearancecharacteristicskey/rollovercaption)
- [static let rotation: PDFAppearanceCharacteristicsKey](/documentation/pdfkit/pdfappearancecharacteristicskey/rotation)

##### Creating an Appearance Characteristic Key

- [init(rawValue: String)](/documentation/pdfkit/pdfappearancecharacteristicskey/init(rawvalue:))

### Configuring Text Widget Annotations

- [var isMultiline: Bool](/documentation/pdfkit/pdfannotation/ismultiline)
- [var isPasswordField: Bool](/documentation/pdfkit/pdfannotation/ispasswordfield)
- [var maximumLength: Int](/documentation/pdfkit/pdfannotation/maximumlength)
- [var hasComb: Bool](/documentation/pdfkit/pdfannotation/hascomb)

### Configuring Button Widget Annotations

- [var widgetControlType: PDFWidgetControlType](/documentation/pdfkit/pdfannotation/widgetcontroltype)
- [var buttonWidgetState: PDFWidgetCellState](/documentation/pdfkit/pdfannotation/buttonwidgetstate)
- [PDFWidgetCellState](/documentation/pdfkit/pdfwidgetcellstate)

#### Choosing a Cell State

- [case onState](/documentation/pdfkit/pdfwidgetcellstate/onstate)
- [case offState](/documentation/pdfkit/pdfwidgetcellstate/offstate)
- [case mixedState](/documentation/pdfkit/pdfwidgetcellstate/mixedstate)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfwidgetcellstate/init(rawvalue:))
- [var buttonWidgetStateString: String](/documentation/pdfkit/pdfannotation/buttonwidgetstatestring)
- [var caption: String?](/documentation/pdfkit/pdfannotation/caption)
- [var allowsToggleToOff: Bool](/documentation/pdfkit/pdfannotation/allowstoggletooff)
- [var radiosInUnison: Bool](/documentation/pdfkit/pdfannotation/radiosinunison)

### Configuring Choice Widget Annotations

- [var choices: [String]?](/documentation/pdfkit/pdfannotation/choices)
- [var isListChoice: Bool](/documentation/pdfkit/pdfannotation/islistchoice)
- [var values: [String]?](/documentation/pdfkit/pdfannotation/values)

### Configuring Ink Annotations

- [var paths: [UIBezierPath]?](/documentation/pdfkit/pdfannotation/paths)
- [func add(UIBezierPath)](/documentation/pdfkit/pdfannotation/add(_:))
- [func remove(UIBezierPath)](/documentation/pdfkit/pdfannotation/remove(_:))

### Configuring Stamp Annotations

- [var stampName: String?](/documentation/pdfkit/pdfannotation/stampname)

### Deprecated

- [Deprecated Symbols](/documentation/pdfkit/deprecated-symbols)

#### Deprecated Annotation Types

- [PDFAnnotationButtonWidget](/documentation/pdfkit/pdfannotationbuttonwidget)

##### Getting and Setting the Control Type

- [func controlType() -> PDFWidgetControlType](/documentation/pdfkit/pdfannotationbuttonwidget/controltype())
- [func setControlType(PDFWidgetControlType)](/documentation/pdfkit/pdfannotationbuttonwidget/setcontroltype(_:))

##### Getting and Setting the Control’s State

- [func state() -> Int](/documentation/pdfkit/pdfannotationbuttonwidget/state())
- [func setState(Int)](/documentation/pdfkit/pdfannotationbuttonwidget/setstate(_:))

##### Getting and Setting the Control’s Appearance

- [func backgroundColor() -> NSColor!](/documentation/pdfkit/pdfannotationbuttonwidget/backgroundcolor())
- [func setBackgroundColor(NSColor!)](/documentation/pdfkit/pdfannotationbuttonwidget/setbackgroundcolor(_:))

##### Getting and Setting the Control Label Font Attributes

- [func font() -> NSFont!](/documentation/pdfkit/pdfannotationbuttonwidget/font())
- [func setFont(NSFont!)](/documentation/pdfkit/pdfannotationbuttonwidget/setfont(_:))
- [func fontColor() -> NSColor!](/documentation/pdfkit/pdfannotationbuttonwidget/fontcolor())
- [func setFontColor(NSColor!)](/documentation/pdfkit/pdfannotationbuttonwidget/setfontcolor(_:))

##### Getting and Setting the Control Label Text

- [func caption() -> String!](/documentation/pdfkit/pdfannotationbuttonwidget/caption())
- [func setCaption(String!)](/documentation/pdfkit/pdfannotationbuttonwidget/setcaption(_:))

##### Managing Radio Button Behavior

- [func allowsToggleToOff() -> Bool](/documentation/pdfkit/pdfannotationbuttonwidget/allowstoggletooff())

##### Managing Control State Values and Form Fields

- [func onStateValue() -> String!](/documentation/pdfkit/pdfannotationbuttonwidget/onstatevalue())
- [func setOnStateValue(String!)](/documentation/pdfkit/pdfannotationbuttonwidget/setonstatevalue(_:))
- [func fieldName() -> String!](/documentation/pdfkit/pdfannotationbuttonwidget/fieldname())
- [func setFieldName(String!)](/documentation/pdfkit/pdfannotationbuttonwidget/setfieldname(_:))

##### Constants

- [PDFWidgetControlType](/documentation/pdfkit/pdfwidgetcontroltype)

###### Constants

- [case unknownControl](/documentation/pdfkit/pdfwidgetcontroltype/unknowncontrol)
- [case pushButtonControl](/documentation/pdfkit/pdfwidgetcontroltype/pushbuttoncontrol)
- [case radioButtonControl](/documentation/pdfkit/pdfwidgetcontroltype/radiobuttoncontrol)
- [case checkBoxControl](/documentation/pdfkit/pdfwidgetcontroltype/checkboxcontrol)

###### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfwidgetcontroltype/init(rawvalue:))

##### Instance Methods

- [func setAllowsToggleToOff(Bool)](/documentation/pdfkit/pdfannotationbuttonwidget/setallowstoggletooff(_:))
- [PDFAnnotationChoiceWidget](/documentation/pdfkit/pdfannotationchoicewidget)

##### Getting and Setting the String Value

- [func stringValue() -> String!](/documentation/pdfkit/pdfannotationchoicewidget/stringvalue())
- [func setStringValue(String!)](/documentation/pdfkit/pdfannotationchoicewidget/setstringvalue(_:))

##### Managing Font and Background Color Characteristics

- [func backgroundColor() -> NSColor!](/documentation/pdfkit/pdfannotationchoicewidget/backgroundcolor())
- [func setBackgroundColor(NSColor!)](/documentation/pdfkit/pdfannotationchoicewidget/setbackgroundcolor(_:))
- [func font() -> NSFont!](/documentation/pdfkit/pdfannotationchoicewidget/font())
- [func setFont(NSFont!)](/documentation/pdfkit/pdfannotationchoicewidget/setfont(_:))
- [func fontColor() -> NSColor!](/documentation/pdfkit/pdfannotationchoicewidget/fontcolor())
- [func setFontColor(NSColor!)](/documentation/pdfkit/pdfannotationchoicewidget/setfontcolor(_:))

##### Managing the Associated Field Name

- [func fieldName() -> String!](/documentation/pdfkit/pdfannotationchoicewidget/fieldname())
- [func setFieldName(String!)](/documentation/pdfkit/pdfannotationchoicewidget/setfieldname(_:))

##### Determining the Type of Choice Widget Annotation

- [func isListChoice() -> Bool](/documentation/pdfkit/pdfannotationchoicewidget/islistchoice())
- [func setIsListChoice(Bool)](/documentation/pdfkit/pdfannotationchoicewidget/setislistchoice(_:))

##### Accessing the Items in the Choice Widget Annotation

- [func choices() -> [Any]!](/documentation/pdfkit/pdfannotationchoicewidget/choices())
- [func setChoices([Any]!)](/documentation/pdfkit/pdfannotationchoicewidget/setchoices(_:))
- [PDFAnnotationCircle](/documentation/pdfkit/pdfannotationcircle)

##### Accessor methods

- [func interiorColor() -> NSColor!](/documentation/pdfkit/pdfannotationcircle/interiorcolor())
- [func setInteriorColor(NSColor!)](/documentation/pdfkit/pdfannotationcircle/setinteriorcolor(_:))
- [PDFAnnotationFreeText](/documentation/pdfkit/pdfannotationfreetext)

##### Managing Text Alignment

- [func alignment() -> NSTextAlignment](/documentation/pdfkit/pdfannotationfreetext/alignment())
- [func setAlignment(NSTextAlignment)](/documentation/pdfkit/pdfannotationfreetext/setalignment(_:))

##### Managing Font and Font Color

- [func font() -> NSFont!](/documentation/pdfkit/pdfannotationfreetext/font())
- [func setFont(NSFont!)](/documentation/pdfkit/pdfannotationfreetext/setfont(_:))
- [func fontColor() -> NSColor!](/documentation/pdfkit/pdfannotationfreetext/fontcolor())
- [func setFontColor(NSColor!)](/documentation/pdfkit/pdfannotationfreetext/setfontcolor(_:))
- [PDFAnnotationInk](/documentation/pdfkit/pdfannotationink)

##### Accessor methods

- [func paths() -> [Any]!](/documentation/pdfkit/pdfannotationink/paths())

##### Working with Bezier paths

- [func add(NSBezierPath!)](/documentation/pdfkit/pdfannotationink/add(_:))
- [func remove(NSBezierPath!)](/documentation/pdfkit/pdfannotationink/remove(_:))
- [PDFAnnotationLine](/documentation/pdfkit/pdfannotationline)

##### Specifying the Starting and Ending Points

- [func startPoint() -> NSPoint](/documentation/pdfkit/pdfannotationline/startpoint())
- [func setStart(NSPoint)](/documentation/pdfkit/pdfannotationline/setstart(_:)-86is0)
- [func endPoint() -> NSPoint](/documentation/pdfkit/pdfannotationline/endpoint())
- [func setEnd(NSPoint)](/documentation/pdfkit/pdfannotationline/setend(_:)-2qn58)

##### Specifying the Line Ending Styles

- [func startLineStyle() -> PDFLineStyle](/documentation/pdfkit/pdfannotationline/startlinestyle())
- [func setStart(PDFLineStyle)](/documentation/pdfkit/pdfannotationline/setstart(_:)-57pe0)
- [func endLineStyle() -> PDFLineStyle](/documentation/pdfkit/pdfannotationline/endlinestyle())
- [func setEnd(PDFLineStyle)](/documentation/pdfkit/pdfannotationline/setend(_:)-9cp0t)

##### Specifying the Color of Line-end Ornaments

- [func interiorColor() -> NSColor!](/documentation/pdfkit/pdfannotationline/interiorcolor())
- [func setInteriorColor(NSColor!)](/documentation/pdfkit/pdfannotationline/setinteriorcolor(_:))

##### Constants

- [PDFLineStyle](/documentation/pdfkit/pdflinestyle)

###### Constants

- [case none](/documentation/pdfkit/pdflinestyle/none)
- [case square](/documentation/pdfkit/pdflinestyle/square)
- [case circle](/documentation/pdfkit/pdflinestyle/circle)
- [case diamond](/documentation/pdfkit/pdflinestyle/diamond)
- [case openArrow](/documentation/pdfkit/pdflinestyle/openarrow)
- [case closedArrow](/documentation/pdfkit/pdflinestyle/closedarrow)

###### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdflinestyle/init(rawvalue:))
- [PDFAnnotationLink](/documentation/pdfkit/pdfannotationlink)

##### Working with link destinations

- [func destination() -> PDFDestination!](/documentation/pdfkit/pdfannotationlink/destination())
- [func setDestination(PDFDestination!)](/documentation/pdfkit/pdfannotationlink/setdestination(_:))
- [func url() -> URL!](/documentation/pdfkit/pdfannotationlink/url())
- [func setURL(URL!)](/documentation/pdfkit/pdfannotationlink/seturl(_:))
- [PDFAnnotationMarkup](/documentation/pdfkit/pdfannotationmarkup)

##### Working with Markup Boundaries

- [func quadrilateralPoints() -> [Any]!](/documentation/pdfkit/pdfannotationmarkup/quadrilateralpoints())
- [func setQuadrilateralPoints([Any]!)](/documentation/pdfkit/pdfannotationmarkup/setquadrilateralpoints(_:))

##### Working with Markup Style

- [func markupType() -> PDFMarkupType](/documentation/pdfkit/pdfannotationmarkup/markuptype())
- [func setMarkupType(PDFMarkupType)](/documentation/pdfkit/pdfannotationmarkup/setmarkuptype(_:))

##### Constants

- [PDFMarkupType](/documentation/pdfkit/pdfmarkuptype)

###### Constants

- [case highlight](/documentation/pdfkit/pdfmarkuptype/highlight)
- [case strikeOut](/documentation/pdfkit/pdfmarkuptype/strikeout)
- [case underline](/documentation/pdfkit/pdfmarkuptype/underline)
- [case redact](/documentation/pdfkit/pdfmarkuptype/redact)

###### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfmarkuptype/init(rawvalue:))
- [PDFAnnotationPopup](/documentation/pdfkit/pdfannotationpopup)

##### Accessing and Setting the Open State

- [func isOpen() -> Bool](/documentation/pdfkit/pdfannotationpopup/isopen())
- [func setIsOpen(Bool)](/documentation/pdfkit/pdfannotationpopup/setisopen(_:))
- [PDFAnnotationSquare](/documentation/pdfkit/pdfannotationsquare)

##### Accessor methods

- [func interiorColor() -> NSColor!](/documentation/pdfkit/pdfannotationsquare/interiorcolor())
- [func setInteriorColor(NSColor!)](/documentation/pdfkit/pdfannotationsquare/setinteriorcolor(_:))
- [PDFAnnotationStamp](/documentation/pdfkit/pdfannotationstamp)

##### Accessing and setting the stamp annotation

- [func name() -> String!](/documentation/pdfkit/pdfannotationstamp/name())
- [func setName(String!)](/documentation/pdfkit/pdfannotationstamp/setname(_:))
- [PDFAnnotationText](/documentation/pdfkit/pdfannotationtext)

##### Managing the Annotation Icon’s Type

- [func iconType() -> PDFTextAnnotationIconType](/documentation/pdfkit/pdfannotationtext/icontype())
- [func setIconType(PDFTextAnnotationIconType)](/documentation/pdfkit/pdfannotationtext/seticontype(_:))

##### Constants

- [PDFTextAnnotationIconType](/documentation/pdfkit/pdftextannotationicontype)

###### Constants

- [case comment](/documentation/pdfkit/pdftextannotationicontype/comment)
- [case key](/documentation/pdfkit/pdftextannotationicontype/key)
- [case note](/documentation/pdfkit/pdftextannotationicontype/note)
- [case help](/documentation/pdfkit/pdftextannotationicontype/help)
- [case newParagraph](/documentation/pdfkit/pdftextannotationicontype/newparagraph)
- [case paragraph](/documentation/pdfkit/pdftextannotationicontype/paragraph)
- [case insert](/documentation/pdfkit/pdftextannotationicontype/insert)

###### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdftextannotationicontype/init(rawvalue:))
- [PDFAnnotationTextWidget](/documentation/pdfkit/pdfannotationtextwidget)

##### Working with Annotation Strings

- [func stringValue() -> String!](/documentation/pdfkit/pdfannotationtextwidget/stringvalue())
- [func setStringValue(String!)](/documentation/pdfkit/pdfannotationtextwidget/setstringvalue(_:))
- [func maximumLength() -> Int](/documentation/pdfkit/pdfannotationtextwidget/maximumlength())
- [func setMaximumLength(Int)](/documentation/pdfkit/pdfannotationtextwidget/setmaximumlength(_:))

##### Managing the Font and Font Color

- [func font() -> NSFont!](/documentation/pdfkit/pdfannotationtextwidget/font())
- [func setFont(NSFont!)](/documentation/pdfkit/pdfannotationtextwidget/setfont(_:))
- [func fontColor() -> NSColor!](/documentation/pdfkit/pdfannotationtextwidget/fontcolor())
- [func setFontColor(NSColor!)](/documentation/pdfkit/pdfannotationtextwidget/setfontcolor(_:))

##### Managing Background Color, Alignment, and Rotation

- [func backgroundColor() -> NSColor!](/documentation/pdfkit/pdfannotationtextwidget/backgroundcolor())
- [func setBackgroundColor(NSColor!)](/documentation/pdfkit/pdfannotationtextwidget/setbackgroundcolor(_:))
- [func alignment() -> NSTextAlignment](/documentation/pdfkit/pdfannotationtextwidget/alignment())
- [func setAlignment(NSTextAlignment)](/documentation/pdfkit/pdfannotationtextwidget/setalignment(_:))
- [func rotation() -> Int](/documentation/pdfkit/pdfannotationtextwidget/rotation())
- [func setRotation(Int32)](/documentation/pdfkit/pdfannotationtextwidget/setrotation(_:))

##### Working with Field Names

- [func fieldName() -> String!](/documentation/pdfkit/pdfannotationtextwidget/fieldname())
- [func setFieldName(String!)](/documentation/pdfkit/pdfannotationtextwidget/setfieldname(_:))

##### Instance Methods

- [func attributedStringValue() -> NSAttributedString!](/documentation/pdfkit/pdfannotationtextwidget/attributedstringvalue())
- [func isMultiline() -> Bool](/documentation/pdfkit/pdfannotationtextwidget/ismultiline())
- [func setAttributedStringValue(NSAttributedString!)](/documentation/pdfkit/pdfannotationtextwidget/setattributedstringvalue(_:))
- [func setIsMultiline(Bool)](/documentation/pdfkit/pdfannotationtextwidget/setismultiline(_:))

#### Deprecated Methods

- [convenience init(bounds: NSRect)](/documentation/pdfkit/pdfannotation/init(bounds:))
- [convenience init(dictionary: [AnyHashable : Any], forPage: PDFPage?)](/documentation/pdfkit/pdfannotation/init(dictionary:forpage:))
- [func removeAllAppearanceStreams()](/documentation/pdfkit/pdfannotation/removeallappearancestreams())
- [func draw(with: PDFDisplayBox)](/documentation/pdfkit/pdfannotation/draw(with:))

#### Deprecated Properties

- [var mouseUpAction: PDFAction?](/documentation/pdfkit/pdfannotation/mouseupaction)
- [var toolTip: String?](/documentation/pdfkit/pdfannotation/tooltip)

### Instance Properties

- [var isActivatableTextField: Bool](/documentation/pdfkit/pdfannotation/isactivatabletextfield)

## Protocols

- [PDFPageOverlayViewProvider](/documentation/pdfkit/pdfpageoverlayviewprovider)

### Instance Methods

- [func pdfView(PDFView, overlayViewFor: PDFPage) -> UIView?](/documentation/pdfkit/pdfpageoverlayviewprovider/pdfview(_:overlayviewfor:))
- [func pdfView(PDFView, willDisplayOverlayView: UIView, for: PDFPage)](/documentation/pdfkit/pdfpageoverlayviewprovider/pdfview(_:willdisplayoverlayview:for:))
- [func pdfView(PDFView, willEndDisplayingOverlayView: UIView, for: PDFPage)](/documentation/pdfkit/pdfpageoverlayviewprovider/pdfview(_:willenddisplayingoverlayview:for:))

## Reference

- [PDFKit Enumerations](/documentation/pdfkit/enumerations)

### Enumerations

- [PDFAccessPermissions](/documentation/pdfkit/pdfaccesspermissions)

#### Enumeration Cases

- [case allowsCommenting](/documentation/pdfkit/pdfaccesspermissions/allowscommenting)
- [case allowsContentAccessibility](/documentation/pdfkit/pdfaccesspermissions/allowscontentaccessibility)
- [case allowsContentCopying](/documentation/pdfkit/pdfaccesspermissions/allowscontentcopying)
- [case allowsDocumentAssembly](/documentation/pdfkit/pdfaccesspermissions/allowsdocumentassembly)
- [case allowsDocumentChanges](/documentation/pdfkit/pdfaccesspermissions/allowsdocumentchanges)
- [case allowsFormFieldEntry](/documentation/pdfkit/pdfaccesspermissions/allowsformfieldentry)
- [case allowsHighQualityPrinting](/documentation/pdfkit/pdfaccesspermissions/allowshighqualityprinting)
- [case allowsLowQualityPrinting](/documentation/pdfkit/pdfaccesspermissions/allowslowqualityprinting)

#### Initializers

- [init?(rawValue: UInt)](/documentation/pdfkit/pdfaccesspermissions/init(rawvalue:))
- [PDFSelectionGranularity](/documentation/pdfkit/pdfselectiongranularity)

#### Enumeration Cases

- [case character](/documentation/pdfkit/pdfselectiongranularity/character)
- [case line](/documentation/pdfkit/pdfselectiongranularity/line)
- [case word](/documentation/pdfkit/pdfselectiongranularity/word)

#### Initializers

- [init?(rawValue: UInt)](/documentation/pdfkit/pdfselectiongranularity/init(rawvalue:))
- [PDFThumbnailLayoutMode](/documentation/pdfkit/pdfthumbnaillayoutmode)

#### Enumeration Cases

- [case horizontal](/documentation/pdfkit/pdfthumbnaillayoutmode/horizontal)
- [case vertical](/documentation/pdfkit/pdfthumbnaillayoutmode/vertical)

#### Initializers

- [init?(rawValue: Int)](/documentation/pdfkit/pdfthumbnaillayoutmode/init(rawvalue:))
- [PDFKit Constants](/documentation/pdfkit/constants)

### Constants

- [let PDFDocumentFoundSelectionKey: String](/documentation/pdfkit/pdfdocumentfoundselectionkey)
- [let PDFDocumentPageIndexKey: String](/documentation/pdfkit/pdfdocumentpageindexkey)
- [PDFKit Data Types](/documentation/pdfkit/data-types)

### Data Types

- [PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption)

#### Initializers

- [init(rawValue: String)](/documentation/pdfkit/pdfpage/imageinitializationoption/init(rawvalue:))

#### Type Properties

- [static let compressionQuality: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/compressionquality)
- [static let mediaBox: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/mediabox)
- [static let rotation: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/rotation)
- [static let upscaleIfSmaller: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/upscaleifsmaller)
- [static let compressionQuality: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/compressionquality)
- [static let mediaBox: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/mediabox)
- [static let rotation: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/rotation)
- [static let upscaleIfSmaller: PDFPage.ImageInitializationOption](/documentation/pdfkit/pdfpage/imageinitializationoption/upscaleifsmaller)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
