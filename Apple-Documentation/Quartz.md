# Quartz Documentation

Source: https://sosumi.ai/documentation/quartz

---
title: Quartz
source: https://developer.apple.com/documentation/quartz
timestamp: 2026-02-13T19:00:56.508Z
---

## Viewing and Transforming Images

- [ImageKit](/documentation/quartz/imagekit)

### Classes

- [IKCameraDeviceView](/documentation/quartz/ikcameradeviceview)

#### Getting and Setting the Camera Device

- [var cameraDevice: ICCameraDevice!](/documentation/quartz/ikcameradeviceview/cameradevice)

#### View Display Mode

- [var iconSize: Int](/documentation/quartz/ikcameradeviceview/iconsize)
- [var mode: IKCameraDeviceViewDisplayMode](/documentation/quartz/ikcameradeviceview/mode)
- [var hasDisplayModeIcon: Bool](/documentation/quartz/ikcameradeviceview/hasdisplaymodeicon)
- [var hasDisplayModeTable: Bool](/documentation/quartz/ikcameradeviceview/hasdisplaymodetable)

#### Selecting the File Transfer Mode

- [var transferMode: IKCameraDeviceViewTransferMode](/documentation/quartz/ikcameradeviceview/transfermode)

#### Configuring Download Interface and Downloading Files

- [var canDownloadSelectedItems: Bool](/documentation/quartz/ikcameradeviceview/candownloadselecteditems)
- [var downloadsDirectory: URL!](/documentation/quartz/ikcameradeviceview/downloadsdirectory)
- [func downloadSelectedItems(Any!)](/documentation/quartz/ikcameradeviceview/downloadselecteditems(_:))
- [func downloadAllItems(Any!)](/documentation/quartz/ikcameradeviceview/downloadallitems(_:))
- [var downloadSelectedControlLabel: String!](/documentation/quartz/ikcameradeviceview/downloadselectedcontrollabel)
- [var downloadAllControlLabel: String!](/documentation/quartz/ikcameradeviceview/downloadallcontrollabel)
- [var displaysDownloadsDirectoryControl: Bool](/documentation/quartz/ikcameradeviceview/displaysdownloadsdirectorycontrol)

#### Getting and Setting the Post Processing Application

- [var displaysPostProcessApplicationControl: Bool](/documentation/quartz/ikcameradeviceview/displayspostprocessapplicationcontrol)
- [var postProcessApplication: URL!](/documentation/quartz/ikcameradeviceview/postprocessapplication)

#### Deleting Selected Items

- [var canDeleteSelectedItems: Bool](/documentation/quartz/ikcameradeviceview/candeleteselecteditems)
- [func deleteSelectedItems(Any!)](/documentation/quartz/ikcameradeviceview/deleteselecteditems(_:))

#### Selection Management

- [func select(IndexSet!, byExtendingSelection: Bool)](/documentation/quartz/ikcameradeviceview/select(_:byextendingselection:))
- [func selectedIndexes() -> IndexSet!](/documentation/quartz/ikcameradeviceview/selectedindexes())

#### Getting and Setting the Delegate

- [var delegate: (any IKCameraDeviceViewDelegate)!](/documentation/quartz/ikcameradeviceview/delegate)

#### Selected Item Rotation

- [var canRotateSelectedItemsLeft: Bool](/documentation/quartz/ikcameradeviceview/canrotateselecteditemsleft)
- [var canRotateSelectedItemsRight: Bool](/documentation/quartz/ikcameradeviceview/canrotateselecteditemsright)
- [func rotateLeft(Any!)](/documentation/quartz/ikcameradeviceview/rotateleft(_:))
- [func rotateRight(Any!)](/documentation/quartz/ikcameradeviceview/rotateright(_:))

#### Constants

- [IKCameraDeviceViewDisplayMode](/documentation/quartz/ikcameradeviceviewdisplaymode)

##### Constants

- [case table](/documentation/quartz/ikcameradeviceviewdisplaymode/table)
- [case icon](/documentation/quartz/ikcameradeviceviewdisplaymode/icon)

##### Enumeration Cases

- [case none](/documentation/quartz/ikcameradeviceviewdisplaymode/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikcameradeviceviewdisplaymode/init(rawvalue:))
- [IKCameraDeviceViewTransferMode](/documentation/quartz/ikcameradeviceviewtransfermode)

##### Constants

- [case fileBased](/documentation/quartz/ikcameradeviceviewtransfermode/filebased)
- [case memoryBased](/documentation/quartz/ikcameradeviceviewtransfermode/memorybased)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikcameradeviceviewtransfermode/init(rawvalue:))

#### Instance Methods

- [func setCustomActionControl(NSSegmentedControl!)](/documentation/quartz/ikcameradeviceview/setcustomactioncontrol(_:))
- [func setCustomDelete(NSSegmentedControl!)](/documentation/quartz/ikcameradeviceview/setcustomdelete(_:))
- [func setCustomIconSizeSlider(NSSlider!)](/documentation/quartz/ikcameradeviceview/setcustomiconsizeslider(_:))
- [func setCustomModeControl(NSSegmentedControl!)](/documentation/quartz/ikcameradeviceview/setcustommodecontrol(_:))
- [func setCustomRotateControl(NSSegmentedControl!)](/documentation/quartz/ikcameradeviceview/setcustomrotatecontrol(_:))
- [func setShowStatusInfoAsWindowSubtitle(Bool)](/documentation/quartz/ikcameradeviceview/setshowstatusinfoaswindowsubtitle(_:))
- [IKDeviceBrowserView](/documentation/quartz/ikdevicebrowserview)

#### Getting the Selected Device

- [var selectedDevice: ICDevice!](/documentation/quartz/ikdevicebrowserview/selecteddevice)

#### Specifying the Device Types to Display

- [var displaysLocalCameras: Bool](/documentation/quartz/ikdevicebrowserview/displayslocalcameras)
- [var displaysNetworkCameras: Bool](/documentation/quartz/ikdevicebrowserview/displaysnetworkcameras)
- [var displaysLocalScanners: Bool](/documentation/quartz/ikdevicebrowserview/displayslocalscanners)
- [var displaysNetworkScanners: Bool](/documentation/quartz/ikdevicebrowserview/displaysnetworkscanners)

#### Specifying the Display Mode

- [var mode: IKDeviceBrowserViewDisplayMode](/documentation/quartz/ikdevicebrowserview/mode)

#### Getting and Setting the Delegate

- [var delegate: (any IKDeviceBrowserViewDelegate)!](/documentation/quartz/ikdevicebrowserview/delegate)

#### Constants

- [IKDeviceBrowserViewDisplayMode](/documentation/quartz/ikdevicebrowserviewdisplaymode)

##### Constants

- [case table](/documentation/quartz/ikdevicebrowserviewdisplaymode/table)
- [case outline](/documentation/quartz/ikdevicebrowserviewdisplaymode/outline)
- [case icon](/documentation/quartz/ikdevicebrowserviewdisplaymode/icon)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikdevicebrowserviewdisplaymode/init(rawvalue:))
- [IKFilterBrowserPanel](/documentation/quartz/ikfilterbrowserpanel)

#### Getting a Filter Name

- [func filterName() -> String!](/documentation/quartz/ikfilterbrowserpanel/filtername())

#### Displaying and Running the Panel

- [func filterBrowserView(options: [AnyHashable : Any]!) -> IKFilterBrowserView!](/documentation/quartz/ikfilterbrowserpanel/filterbrowserview(options:))
- [func begin(options: [AnyHashable : Any]!, modelessDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!)](/documentation/quartz/ikfilterbrowserpanel/begin(options:modelessdelegate:didend:contextinfo:))
- [func beginSheet(options: [AnyHashable : Any]!, modalFor: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!)](/documentation/quartz/ikfilterbrowserpanel/beginsheet(options:modalfor:modaldelegate:didend:contextinfo:))
- [func runModal(options: [AnyHashable : Any]!) -> Int32](/documentation/quartz/ikfilterbrowserpanel/runmodal(options:))
- [func finish(Any!)](/documentation/quartz/ikfilterbrowserpanel/finish(_:))

#### Creating a Filter Browser Panel

- [class func filterBrowserPanel(withStyleMask: UInt32) -> Any!](/documentation/quartz/ikfilterbrowserpanel/filterbrowserpanel(withstylemask:))

#### Constants

- [Filter Browser Option Keys](/documentation/quartz/filter-browser-option-keys)

##### Constants

- [let IKFilterBrowserDefaultInputImage: String](/documentation/quartz/ikfilterbrowserdefaultinputimage)
- [let IKFilterBrowserExcludeCategories: String](/documentation/quartz/ikfilterbrowserexcludecategories)
- [let IKFilterBrowserExcludeFilters: String](/documentation/quartz/ikfilterbrowserexcludefilters)
- [let IKFilterBrowserShowCategories: String](/documentation/quartz/ikfilterbrowsershowcategories)
- [let IKFilterBrowserShowPreview: String](/documentation/quartz/ikfilterbrowsershowpreview)
- [IKFilterBrowserView](/documentation/quartz/ikfilterbrowserview)

#### Setting the Preview State

- [func setPreviewState(Bool)](/documentation/quartz/ikfilterbrowserview/setpreviewstate(_:))

#### Getting the Filter Name

- [func filterName() -> String!](/documentation/quartz/ikfilterbrowserview/filtername())
- [IKFilterUIView](/documentation/quartz/ikfilteruiview)

#### Creating and Initializing a Filter UI View

- [class func view(withFrame: NSRect, filter: CIFilter!) -> Any!](/documentation/quartz/ikfilteruiview/view(withframe:filter:))
- [init!(frame: NSRect, filter: CIFilter!)](/documentation/quartz/ikfilteruiview/init(frame:filter:))

#### Getting Data from the Filter View

- [func filter() -> CIFilter!](/documentation/quartz/ikfilteruiview/filter())
- [func objectController() -> NSObjectController!](/documentation/quartz/ikfilteruiview/objectcontroller())
- [IKImageBrowserCell](/documentation/quartz/ikimagebrowsercell)

#### Cell Component Frames

- [func frame() -> NSRect](/documentation/quartz/ikimagebrowsercell/frame())
- [func imageFrame() -> NSRect](/documentation/quartz/ikimagebrowsercell/imageframe())
- [func subtitleFrame() -> NSRect](/documentation/quartz/ikimagebrowsercell/subtitleframe())
- [func titleFrame() -> NSRect](/documentation/quartz/ikimagebrowsercell/titleframe())
- [func imageContainerFrame() -> NSRect](/documentation/quartz/ikimagebrowsercell/imagecontainerframe())

#### Represented Item

- [func indexOfRepresentedItem() -> Int](/documentation/quartz/ikimagebrowsercell/indexofrepresenteditem())
- [func representedItem() -> Any!](/documentation/quartz/ikimagebrowsercell/representeditem())

#### Selection Handling

- [func isSelected() -> Bool](/documentation/quartz/ikimagebrowsercell/isselected())
- [func selectionFrame() -> NSRect](/documentation/quartz/ikimagebrowsercell/selectionframe())

#### Cell Content Display

- [func imageAlignment() -> NSImageAlignment](/documentation/quartz/ikimagebrowsercell/imagealignment())
- [func opacity() -> CGFloat](/documentation/quartz/ikimagebrowsercell/opacity())

#### Getting The Cell State

- [func cellState() -> IKImageBrowserCellState](/documentation/quartz/ikimagebrowsercell/cellstate())

#### Core Animation Integration

- [func layer(forType: String!) -> CALayer!](/documentation/quartz/ikimagebrowsercell/layer(fortype:))

#### Getting The Parent Browser View

- [func imageBrowserView() -> IKImageBrowserView!](/documentation/quartz/ikimagebrowsercell/imagebrowserview())

#### Constants

- [IKImageBrowserCellState](/documentation/quartz/ikimagebrowsercellstate)

##### Constants

- [var IKImageStateNoImage: IKImageBrowserCellState](/documentation/quartz/ikimagestatenoimage)
- [var IKImageStateInvalid: IKImageBrowserCellState](/documentation/quartz/ikimagestateinvalid)
- [var IKImageStateReady: IKImageBrowserCellState](/documentation/quartz/ikimagestateready)

##### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowsercellstate/rawvalue)
- [Cell Layer Positions](/documentation/quartz/cell-layer-positions)

##### Constants

- [let IKImageBrowserCellBackgroundLayer: String](/documentation/quartz/ikimagebrowsercellbackgroundlayer)
- [let IKImageBrowserCellForegroundLayer: String](/documentation/quartz/ikimagebrowsercellforegroundlayer)
- [let IKImageBrowserCellSelectionLayer: String](/documentation/quartz/ikimagebrowsercellselectionlayer)
- [let IKImageBrowserCellPlaceHolderLayer: String](/documentation/quartz/ikimagebrowsercellplaceholderlayer)
- [IKImageEditPanel](/documentation/quartz/ikimageeditpanel)

#### Creating an Image Editing Panel

- [class func shared() -> IKImageEditPanel!](/documentation/quartz/ikimageeditpanel/shared())

#### Getting the User Adjustments and Effects

- [var filterArray: [Any]!](/documentation/quartz/ikimageeditpanel/filterarray)

#### Getting, Setting, and Reloading Data

- [var dataSource: (any IKImageEditPanelDataSource)!](/documentation/quartz/ikimageeditpanel/datasource)
- [func reloadData()](/documentation/quartz/ikimageeditpanel/reloaddata())
- [IKImageView](/documentation/quartz/ikimageview)

#### Getting and Setting Image View Characteristics

- [var delegate: AnyObject!](/documentation/quartz/ikimageview/delegate)
- [var zoomFactor: CGFloat](/documentation/quartz/ikimageview/zoomfactor)
- [var rotationAngle: CGFloat](/documentation/quartz/ikimageview/rotationangle)
- [var currentToolMode: String!](/documentation/quartz/ikimageview/currenttoolmode)
- [var autoresizes: Bool](/documentation/quartz/ikimageview/autoresizes)
- [var hasHorizontalScroller: Bool](/documentation/quartz/ikimageview/hashorizontalscroller)
- [var hasVerticalScroller: Bool](/documentation/quartz/ikimageview/hasverticalscroller)
- [var autohidesScrollers: Bool](/documentation/quartz/ikimageview/autohidesscrollers)
- [var supportsDragAndDrop: Bool](/documentation/quartz/ikimageview/supportsdraganddrop)
- [var editable: Bool](/documentation/quartz/ikimageview/editable)
- [var doubleClickOpensImageEditPanel: Bool](/documentation/quartz/ikimageview/doubleclickopensimageeditpanel)
- [var imageCorrection: CIFilter!](/documentation/quartz/ikimageview/imagecorrection)
- [var backgroundColor: NSColor!](/documentation/quartz/ikimageview/backgroundcolor)
- [func imageSize() -> NSSize](/documentation/quartz/ikimageview/imagesize())
- [func imageProperties() -> [AnyHashable : Any]!](/documentation/quartz/ikimageview/imageproperties())

#### Getting and Setting Images

- [func image() -> Unmanaged<CGImage>!](/documentation/quartz/ikimageview/image())
- [func setImage(CGImage!, imageProperties: [AnyHashable : Any]!)](/documentation/quartz/ikimageview/setimage(_:imageproperties:))
- [func setImageWith(URL!)](/documentation/quartz/ikimageview/setimagewith(_:))

#### Manipulating the Image in a View

- [func setRotationAngle(CGFloat, center: NSPoint)](/documentation/quartz/ikimageview/setrotationangle(_:center:))
- [func setImageZoomFactor(CGFloat, center: NSPoint)](/documentation/quartz/ikimageview/setimagezoomfactor(_:center:))
- [func zoomImageToFit(Any!)](/documentation/quartz/ikimageview/zoomimagetofit(_:))
- [func zoomImageToActualSize(Any!)](/documentation/quartz/ikimageview/zoomimagetoactualsize(_:))
- [func zoomImage(to: NSRect)](/documentation/quartz/ikimageview/zoomimage(to:))
- [func zoomIn(Any!)](/documentation/quartz/ikimageview/zoomin(_:))
- [func zoomOut(Any!)](/documentation/quartz/ikimageview/zoomout(_:))
- [func crop(Any!)](/documentation/quartz/ikimageview/crop(_:))
- [func flipImageHorizontal(Any!)](/documentation/quartz/ikimageview/flipimagehorizontal(_:))
- [func flipImageVertical(Any!)](/documentation/quartz/ikimageview/flipimagevertical(_:))
- [func rotateImageLeft(Any!)](/documentation/quartz/ikimageview/rotateimageleft(_:))
- [func rotateImageRight(Any!)](/documentation/quartz/ikimageview/rotateimageright(_:))

#### Working With Core Animation

- [func setOverlay(CALayer!, forType: String!)](/documentation/quartz/ikimageview/setoverlay(_:fortype:))
- [func overlay(forType: String!) -> CALayer!](/documentation/quartz/ikimageview/overlay(fortype:))

#### Scrolling

- [func scroll(to: NSPoint)](/documentation/quartz/ikimageview/scroll(to:)-myqk)
- [func scroll(to: NSRect)](/documentation/quartz/ikimageview/scroll(to:)-535q6)

#### Converting Points and Rectangles

- [func convertPoint(toImagePoint: NSPoint) -> NSPoint](/documentation/quartz/ikimageview/convertpoint(toimagepoint:))
- [func convertRect(toImageRect: NSRect) -> NSRect](/documentation/quartz/ikimageview/convertrect(toimagerect:))
- [func convertImagePoint(toViewPoint: NSPoint) -> NSPoint](/documentation/quartz/ikimageview/convertimagepoint(toviewpoint:))
- [func convertImageRect(toViewRect: NSRect) -> NSRect](/documentation/quartz/ikimageview/convertimagerect(toviewrect:))

#### Constants

- [Tool Modes](/documentation/quartz/tool-modes)

##### Constants

- [let IKToolModeNone: String](/documentation/quartz/iktoolmodenone)
- [let IKToolModeMove: String](/documentation/quartz/iktoolmodemove)
- [let IKToolModeSelect: String](/documentation/quartz/iktoolmodeselect)
- [let IKToolModeSelectRect: String](/documentation/quartz/iktoolmodeselectrect)
- [let IKToolModeSelectEllipse: String](/documentation/quartz/iktoolmodeselectellipse)
- [let IKToolModeSelectLasso: String](/documentation/quartz/iktoolmodeselectlasso)
- [let IKToolModeCrop: String](/documentation/quartz/iktoolmodecrop)
- [let IKToolModeRotate: String](/documentation/quartz/iktoolmoderotate)
- [let IKToolModeAnnotate: String](/documentation/quartz/iktoolmodeannotate)
- [Overlay Types](/documentation/quartz/overlay-types)

##### Constants

- [let IKOverlayTypeBackground: String](/documentation/quartz/ikoverlaytypebackground)
- [let IKOverlayTypeImage: String](/documentation/quartz/ikoverlaytypeimage)
- [IKPictureTaker](/documentation/quartz/ikpicturetaker)

#### Creating And Displaying The Picture Taker

- [class func pictureTaker() -> IKPictureTaker!](/documentation/quartz/ikpicturetaker/picturetaker())
- [func beginSheet(for: NSWindow!, withDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!)](/documentation/quartz/ikpicturetaker/beginsheet(for:withdelegate:didend:contextinfo:))
- [func begin(withDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!)](/documentation/quartz/ikpicturetaker/begin(withdelegate:didend:contextinfo:))
- [func popUpRecentsMenu(for: NSView!, withDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!)](/documentation/quartz/ikpicturetaker/popuprecentsmenu(for:withdelegate:didend:contextinfo:))
- [func runModal() -> Int](/documentation/quartz/ikpicturetaker/runmodal())

#### Getting and Setting Images

- [func setInputImage(NSImage!)](/documentation/quartz/ikpicturetaker/setinputimage(_:))
- [func inputImage() -> NSImage!](/documentation/quartz/ikpicturetaker/inputimage())
- [func outputImage() -> NSImage!](/documentation/quartz/ikpicturetaker/outputimage())

#### Getting and Setting Mirroring

- [func setMirroring(Bool)](/documentation/quartz/ikpicturetaker/setmirroring(_:))
- [func mirroring() -> Bool](/documentation/quartz/ikpicturetaker/mirroring())

#### Constants

- [Picture Taker Keys](/documentation/quartz/picture-taker-keys)

##### Constants

- [let IKPictureTakerAllowsVideoCaptureKey: String](/documentation/quartz/ikpicturetakerallowsvideocapturekey)
- [let IKPictureTakerAllowsFileChoosingKey: String](/documentation/quartz/ikpicturetakerallowsfilechoosingkey)
- [let IKPictureTakerUpdateRecentPictureKey: String](/documentation/quartz/ikpicturetakerupdaterecentpicturekey)
- [let IKPictureTakerAllowsEditingKey: String](/documentation/quartz/ikpicturetakerallowseditingkey)
- [let IKPictureTakerShowEffectsKey: String](/documentation/quartz/ikpicturetakershoweffectskey)
- [let IKPictureTakerInformationalTextKey: String](/documentation/quartz/ikpicturetakerinformationaltextkey)
- [let IKPictureTakerImageTransformsKey: String](/documentation/quartz/ikpicturetakerimagetransformskey)
- [let IKPictureTakerOutputImageMaxSizeKey: String](/documentation/quartz/ikpicturetakeroutputimagemaxsizekey)
- [let IKPictureTakerCropAreaSizeKey: String](/documentation/quartz/ikpicturetakercropareasizekey)
- [let IKPictureTakerShowAddressBookPictureKey: String](/documentation/quartz/ikpicturetakershowaddressbookpicturekey)
- [let IKPictureTakerShowEmptyPictureKey: String](/documentation/quartz/ikpicturetakershowemptypicturekey)
- [let IKPictureTakerRemainOpenAfterValidateKey: String](/documentation/quartz/ikpicturetakerremainopenaftervalidatekey)
- [IKSaveOptions](/documentation/quartz/iksaveoptions)

#### Creating A Save Options Accessory View

- [init!(imageProperties: [AnyHashable : Any]!, imageUTType: String!)](/documentation/quartz/iksaveoptions/init(imageproperties:imageuttype:))
- [func addAccessoryView(to: NSSavePanel!)](/documentation/quartz/iksaveoptions/addaccessoryview(to:))

#### Retrieving User Responses

- [var imageProperties: [AnyHashable : Any]!](/documentation/quartz/iksaveoptions/imageproperties)
- [var imageUTType: String!](/documentation/quartz/iksaveoptions/imageuttype)
- [var userSelection: [AnyHashable : Any]!](/documentation/quartz/iksaveoptions/userselection)

#### Getting and Setting the delegate

- [var delegate: AnyObject!](/documentation/quartz/iksaveoptions/delegate)

#### File Type Filtering

- [func saveOptions(IKSaveOptions!, shouldShowUTType: String!) -> Bool](/documentation/objectivec/nsobject-swift.class/saveoptions(_:shouldshowuttype:))

#### Instance Properties

- [var rememberLastSetting: Bool](/documentation/quartz/iksaveoptions/rememberlastsetting)

#### Instance Methods

- [func add(to: NSView!)](/documentation/quartz/iksaveoptions/add(to:))
- [IKScannerDeviceView](/documentation/quartz/ikscannerdeviceview)

#### Setting the Scanner Device

- [var scannerDevice: ICScannerDevice!](/documentation/quartz/ikscannerdeviceview/scannerdevice)

#### Setting the Device View’s Display Mode

- [var mode: IKScannerDeviceViewDisplayMode](/documentation/quartz/ikscannerdeviceview/mode)
- [var hasDisplayModeAdvanced: Bool](/documentation/quartz/ikscannerdeviceview/hasdisplaymodeadvanced)
- [var hasDisplayModeSimple: Bool](/documentation/quartz/ikscannerdeviceview/hasdisplaymodesimple)

#### Configuring Downloading

- [var displaysDownloadsDirectoryControl: Bool](/documentation/quartz/ikscannerdeviceview/displaysdownloadsdirectorycontrol)
- [var downloadsDirectory: URL!](/documentation/quartz/ikscannerdeviceview/downloadsdirectory)
- [var transferMode: IKScannerDeviceViewTransferMode](/documentation/quartz/ikscannerdeviceview/transfermode)
- [var documentName: String!](/documentation/quartz/ikscannerdeviceview/documentname)

#### Specifying a Post Processing Application

- [var displaysPostProcessApplicationControl: Bool](/documentation/quartz/ikscannerdeviceview/displayspostprocessapplicationcontrol)
- [var postProcessApplication: URL!](/documentation/quartz/ikscannerdeviceview/postprocessapplication)

#### Getting and Setting the Delegate

- [var delegate: (any IKScannerDeviceViewDelegate)!](/documentation/quartz/ikscannerdeviceview/delegate)

#### Customizing Button Labels

- [var overviewControlLabel: String!](/documentation/quartz/ikscannerdeviceview/overviewcontrollabel)
- [var scanControlLabel: String!](/documentation/quartz/ikscannerdeviceview/scancontrollabel)

#### Constants

- [IKScannerDeviceViewTransferMode](/documentation/quartz/ikscannerdeviceviewtransfermode)

##### Constants

- [case fileBased](/documentation/quartz/ikscannerdeviceviewtransfermode/filebased)
- [case memoryBased](/documentation/quartz/ikscannerdeviceviewtransfermode/memorybased)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikscannerdeviceviewtransfermode/init(rawvalue:))
- [IKScannerDeviceViewDisplayMode](/documentation/quartz/ikscannerdeviceviewdisplaymode)

##### Constants

- [case simple](/documentation/quartz/ikscannerdeviceviewdisplaymode/simple)
- [case advanced](/documentation/quartz/ikscannerdeviceviewdisplaymode/advanced)

##### Enumeration Cases

- [case none](/documentation/quartz/ikscannerdeviceviewdisplaymode/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikscannerdeviceviewdisplaymode/init(rawvalue:))
- [IKSlideshow](/documentation/quartz/ikslideshow)

#### Creating a Shared Instance of a Slideshow

- [class func shared() -> IKSlideshow!](/documentation/quartz/ikslideshow/shared())

#### Running and Stopping a Slideshow

- [func run(with: (any IKSlideshowDataSource)!, inMode: String!, options: [AnyHashable : Any]!)](/documentation/quartz/ikslideshow/run(with:inmode:options:))
- [func stop(Any!)](/documentation/quartz/ikslideshow/stop(_:))
- [var autoPlayDelay: TimeInterval](/documentation/quartz/ikslideshow/autoplaydelay)

#### Getting Slideshow Data

- [func indexOfCurrentSlideshowItem() -> Int](/documentation/quartz/ikslideshow/indexofcurrentslideshowitem())

#### Reloading Data

- [func reloadData()](/documentation/quartz/ikslideshow/reloaddata())
- [func reloadItem(at: Int)](/documentation/quartz/ikslideshow/reloaditem(at:))

#### Exporting Slideshow Items

- [class func canExport(toApplication: String!) -> Bool](/documentation/quartz/ikslideshow/canexport(toapplication:))
- [class func exportItem(Any!, toApplication: String!)](/documentation/quartz/ikslideshow/exportitem(_:toapplication:))

#### Constants

- [Bundle Identifiers](/documentation/quartz/bundle-identifiers)

##### Constants

- [let IK_iPhotoBundleIdentifier: String](/documentation/quartz/ik_iphotobundleidentifier)
- [let IK_ApertureBundleIdentifier: String](/documentation/quartz/ik_aperturebundleidentifier)
- [let IK_MailBundleIdentifier: String](/documentation/quartz/ik_mailbundleidentifier)
- [Slideshow Modes](/documentation/quartz/slideshow-modes)

##### Constants

- [let IKSlideshowModeImages: String](/documentation/quartz/ikslideshowmodeimages)
- [let IKSlideshowModePDF: String](/documentation/quartz/ikslideshowmodepdf)
- [let IKSlideshowModeOther: String](/documentation/quartz/ikslideshowmodeother)
- [Slideshow Option Keys](/documentation/quartz/slideshow-option-keys)

##### Constants

- [let IKSlideshowWrapAround: String](/documentation/quartz/ikslideshowwraparound)
- [let IKSlideshowStartPaused: String](/documentation/quartz/ikslideshowstartpaused)
- [let IKSlideshowStartIndex: String](/documentation/quartz/ikslideshowstartindex)
- [let IKSlideshowPDFDisplayBox: String](/documentation/quartz/ikslideshowpdfdisplaybox)
- [let IKSlideshowPDFDisplayMode: String](/documentation/quartz/ikslideshowpdfdisplaymode)
- [let IKSlideshowPDFDisplaysAsBook: String](/documentation/quartz/ikslideshowpdfdisplaysasbook)
- [let IKSlideshowScreen: String](/documentation/quartz/ikslideshowscreen)
- [let IKSlideshowAudioFile: String](/documentation/quartz/ikslideshowaudiofile)

### Protocols

- [IKCameraDeviceViewDelegate](/documentation/quartz/ikcameradeviceviewdelegate)

#### Downloading Camera Content

- [func cameraDeviceView(IKCameraDeviceView!, didDownloadFile: ICCameraFile!, location: URL!, fileData: Data!, error: (any Error)!)](/documentation/quartz/ikcameradeviceviewdelegate/cameradeviceview(_:diddownloadfile:location:filedata:error:))

#### Detecting Selection Changes

- [func cameraDeviceViewSelectionDidChange(IKCameraDeviceView!)](/documentation/quartz/ikcameradeviceviewdelegate/cameradeviceviewselectiondidchange(_:))

#### Managing Errors

- [func cameraDeviceView(IKCameraDeviceView!, didEncounterError: (any Error)!)](/documentation/quartz/ikcameradeviceviewdelegate/cameradeviceview(_:didencountererror:))
- [IKDeviceBrowserViewDelegate](/documentation/quartz/ikdevicebrowserviewdelegate)

#### Responding to Selection Changes

- [func deviceBrowserView(IKDeviceBrowserView!, selectionDidChange: ICDevice!)](/documentation/quartz/ikdevicebrowserviewdelegate/devicebrowserview(_:selectiondidchange:))

#### Responding to Errors

- [func deviceBrowserView(IKDeviceBrowserView!, didEncounterError: (any Error)!)](/documentation/quartz/ikdevicebrowserviewdelegate/devicebrowserview(_:didencountererror:))
- [IKFilterCustomUIProvider](/documentation/quartz/ikfiltercustomuiprovider)

#### Providing a Custom View

- [func provideView(forUIConfiguration: [AnyHashable : Any]!, excludedKeys: [Any]!) -> IKFilterUIView!](/documentation/quartz/ikfiltercustomuiprovider/provideview(foruiconfiguration:excludedkeys:))
- [IKImageBrowserDataSource Protocol](/documentation/quartz/ikimagebrowserdatasource-protocol)

#### Providing Information About Items (Required)

- [func numberOfItems(inImageBrowser: IKImageBrowserView!) -> Int](/documentation/objectivec/nsobject-swift.class/numberofitems(inimagebrowser:))
- [func imageBrowser(IKImageBrowserView!, itemAt: Int) -> Any!](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:itemat:))

#### Supporting Item Editing (Optional)

- [func imageBrowser(IKImageBrowserView!, removeItemsAt: IndexSet!)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:removeitemsat:))
- [func imageBrowser(IKImageBrowserView!, moveItemsAt: IndexSet!, to: Int) -> Bool](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:moveitemsat:to:))
- [func imageBrowser(IKImageBrowserView!, writeItemsAt: IndexSet!, to: NSPasteboard!) -> Int](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:writeitemsat:to:))

#### Providing Information About Groups (Optional)

- [func numberOfGroups(inImageBrowser: IKImageBrowserView!) -> Int](/documentation/objectivec/nsobject-swift.class/numberofgroups(inimagebrowser:))
- [func imageBrowser(IKImageBrowserView!, groupAt: Int) -> [AnyHashable : Any]!](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:groupat:))
- [IKImageBrowserDelegate Protocol](/documentation/quartz/ikimagebrowserdelegate-protocol)

#### Performing Custom Tasks in Response to User Events

- [func imageBrowser(IKImageBrowserView!, backgroundWasRightClickedWith: NSEvent!)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:backgroundwasrightclickedwith:))
- [func imageBrowser(IKImageBrowserView!, cellWasRightClickedAt: Int, with: NSEvent!)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:cellwasrightclickedat:with:))
- [func imageBrowser(IKImageBrowserView!, cellWasDoubleClickedAt: Int)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:cellwasdoubleclickedat:))
- [func imageBrowserSelectionDidChange(IKImageBrowserView!)](/documentation/objectivec/nsobject-swift.class/imagebrowserselectiondidchange(_:))
- [IKImageBrowserItem Protocol](/documentation/quartz/ikimagebrowseritem-protocol)

#### Providing Required Information for an Image

- [func imageUID() -> String!](/documentation/objectivec/nsobject-swift.class/imageuid())
- [func imageRepresentationType() -> String!](/documentation/objectivec/nsobject-swift.class/imagerepresentationtype())
- [func imageRepresentation() -> Any!](/documentation/objectivec/nsobject-swift.class/imagerepresentation())

#### Providing Optional Information for an Image

- [func imageVersion() -> Int](/documentation/objectivec/nsobject-swift.class/imageversion())
- [func imageTitle() -> String!](/documentation/objectivec/nsobject-swift.class/imagetitle())
- [func imageSubtitle() -> String!](/documentation/objectivec/nsobject-swift.class/imagesubtitle())

#### Constants

- [Image Representation Types](/documentation/quartz/image-representation-types)

##### Constants

- [let IKImageBrowserPathRepresentationType: String](/documentation/quartz/ikimagebrowserpathrepresentationtype)
- [let IKImageBrowserNSURLRepresentationType: String](/documentation/quartz/ikimagebrowsernsurlrepresentationtype)
- [let IKImageBrowserNSImageRepresentationType: String](/documentation/quartz/ikimagebrowsernsimagerepresentationtype)
- [let IKImageBrowserCGImageRepresentationType: String](/documentation/quartz/ikimagebrowsercgimagerepresentationtype)
- [let IKImageBrowserCGImageSourceRepresentationType: String](/documentation/quartz/ikimagebrowsercgimagesourcerepresentationtype)
- [let IKImageBrowserNSDataRepresentationType: String](/documentation/quartz/ikimagebrowsernsdatarepresentationtype)
- [let IKImageBrowserNSBitmapImageRepresentationType: String](/documentation/quartz/ikimagebrowsernsbitmapimagerepresentationtype)
- [let IKImageBrowserQTMovieRepresentationType: String](/documentation/quartz/ikimagebrowserqtmovierepresentationtype)
- [let IKImageBrowserQTMoviePathRepresentationType: String](/documentation/quartz/ikimagebrowserqtmoviepathrepresentationtype)
- [let IKImageBrowserQCCompositionRepresentationType: String](/documentation/quartz/ikimagebrowserqccompositionrepresentationtype)
- [let IKImageBrowserQCCompositionPathRepresentationType: String](/documentation/quartz/ikimagebrowserqccompositionpathrepresentationtype)
- [let IKImageBrowserQuickLookPathRepresentationType: String](/documentation/quartz/ikimagebrowserquicklookpathrepresentationtype)
- [let IKImageBrowserIconRefPathRepresentationType: String](/documentation/quartz/ikimagebrowsericonrefpathrepresentationtype)
- [let IKImageBrowserIconRefRepresentationType: String](/documentation/quartz/ikimagebrowsericonrefrepresentationtype)
- [let IKImageBrowserPDFPageRepresentationType: String](/documentation/quartz/ikimagebrowserpdfpagerepresentationtype)
- [IKImageEditPanelDataSource](/documentation/quartz/ikimageeditpaneldatasource)

#### Getting and Setting Image Properties

- [var imageProperties: [AnyHashable : Any]!](/documentation/quartz/ikimageeditpaneldatasource/imageproperties)
- [func setImage(CGImage!, imageProperties: [AnyHashable : Any]!)](/documentation/quartz/ikimageeditpaneldatasource/setimage(_:imageproperties:))

#### Getting Images From the Data Source

- [var image: CGImage!](/documentation/quartz/ikimageeditpaneldatasource/image)
- [func thumbnail(withMaximumSize: NSSize) -> Unmanaged<CGImage>!](/documentation/quartz/ikimageeditpaneldatasource/thumbnail(withmaximumsize:))

#### New Methods

- [var hasAdjustMode: Bool](/documentation/quartz/ikimageeditpaneldatasource/hasadjustmode)
- [var hasDetailsMode: Bool](/documentation/quartz/ikimageeditpaneldatasource/hasdetailsmode)
- [var hasEffectsMode: Bool](/documentation/quartz/ikimageeditpaneldatasource/haseffectsmode)
- [IKScannerDeviceViewDelegate](/documentation/quartz/ikscannerdeviceviewdelegate)

#### Scan Completed

- [func scannerDeviceView(IKScannerDeviceView!, didScanTo: URL!, fileData: Data!, error: (any Error)!)](/documentation/quartz/ikscannerdeviceviewdelegate/scannerdeviceview(_:didscanto:filedata:error:))

#### Scanner Encountered Error

- [func scannerDeviceView(IKScannerDeviceView!, didEncounterError: (any Error)!)](/documentation/quartz/ikscannerdeviceviewdelegate/scannerdeviceview(_:didencountererror:))

#### Instance Methods

- [func scannerDeviceView(IKScannerDeviceView!, didScanTo: URL!, error: (any Error)!)](/documentation/quartz/ikscannerdeviceviewdelegate/scannerdeviceview(_:didscanto:error:))
- [func scannerDeviceView(IKScannerDeviceView!, didScanTo: ICScannerBandData!, scanInfo: [AnyHashable : Any]!, error: (any Error)!)](/documentation/quartz/ikscannerdeviceviewdelegate/scannerdeviceview(_:didscanto:scaninfo:error:))
- [IKSlideshowDataSource](/documentation/quartz/ikslideshowdatasource)

#### Providing Slideshow Information

- [func numberOfSlideshowItems() -> Int](/documentation/quartz/ikslideshowdatasource/numberofslideshowitems())
- [func slideshowItem(at: Int) -> Any!](/documentation/quartz/ikslideshowdatasource/slideshowitem(at:))
- [func nameOfSlideshowItem(at: Int) -> String!](/documentation/quartz/ikslideshowdatasource/nameofslideshowitem(at:))
- [func canExportSlideshowItem(at: Int, toApplication: String!) -> Bool](/documentation/quartz/ikslideshowdatasource/canexportslideshowitem(at:toapplication:))

#### Performing Custom Tasks

- [func slideshowWillStart()](/documentation/quartz/ikslideshowdatasource/slideshowwillstart())
- [func slideshowDidStop()](/documentation/quartz/ikslideshowdatasource/slideshowdidstop())
- [func slideshowDidChangeCurrentIndex(Int)](/documentation/quartz/ikslideshowdatasource/slideshowdidchangecurrentindex(_:))

### Informal Protocols

- [IKImageBrowserCellState](/documentation/quartz/ikimagebrowsercellstate)

#### Constants

- [var IKImageStateNoImage: IKImageBrowserCellState](/documentation/quartz/ikimagestatenoimage)
- [var IKImageStateInvalid: IKImageBrowserCellState](/documentation/quartz/ikimagestateinvalid)
- [var IKImageStateReady: IKImageBrowserCellState](/documentation/quartz/ikimagestateready)

#### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowsercellstate/rawvalue)
- [IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropoperation)

#### Constants

- [var IKImageBrowserDropOn: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropon)
- [var IKImageBrowserDropBefore: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropbefore)

#### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowserdropoperation/rawvalue)

### Extended Types

- [CIFilter](/documentation/coreimage/cifilter-swift.class)

### Reference

- [ImageKit Constants](/documentation/quartz/imagekit-quartz-constants)

#### Constants

- [var IKImageBrowserDropOn: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropon)
- [var IKImageBrowserDropBefore: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropbefore)
- [let IKFilterBrowserDefaultInputImage: String](/documentation/quartz/ikfilterbrowserdefaultinputimage)
- [let IKFilterBrowserExcludeCategories: String](/documentation/quartz/ikfilterbrowserexcludecategories)
- [let IKFilterBrowserExcludeFilters: String](/documentation/quartz/ikfilterbrowserexcludefilters)
- [let IKFilterBrowserShowCategories: String](/documentation/quartz/ikfilterbrowsershowcategories)
- [let IKFilterBrowserShowPreview: String](/documentation/quartz/ikfilterbrowsershowpreview)
- [let IKImageBrowserBackgroundColorKey: String](/documentation/quartz/ikimagebrowserbackgroundcolorkey)
- [let IKImageBrowserCellBackgroundLayer: String](/documentation/quartz/ikimagebrowsercellbackgroundlayer)
- [let IKImageBrowserCellForegroundLayer: String](/documentation/quartz/ikimagebrowsercellforegroundlayer)
- [let IKImageBrowserCellPlaceHolderLayer: String](/documentation/quartz/ikimagebrowsercellplaceholderlayer)
- [let IKImageBrowserCellSelectionLayer: String](/documentation/quartz/ikimagebrowsercellselectionlayer)
- [let IKImageBrowserCellsHighlightedTitleAttributesKey: String](/documentation/quartz/ikimagebrowsercellshighlightedtitleattributeskey)
- [let IKImageBrowserCellsOutlineColorKey: String](/documentation/quartz/ikimagebrowsercellsoutlinecolorkey)
- [let IKImageBrowserCellsSubtitleAttributesKey: String](/documentation/quartz/ikimagebrowsercellssubtitleattributeskey)
- [let IKImageBrowserCellsTitleAttributesKey: String](/documentation/quartz/ikimagebrowsercellstitleattributeskey)
- [let IKImageBrowserGroupBackgroundColorKey: String](/documentation/quartz/ikimagebrowsergroupbackgroundcolorkey)
- [let IKImageBrowserGroupFooterLayer: String](/documentation/quartz/ikimagebrowsergroupfooterlayer)
- [let IKImageBrowserGroupHeaderLayer: String](/documentation/quartz/ikimagebrowsergroupheaderlayer)
- [let IKImageBrowserGroupRangeKey: String](/documentation/quartz/ikimagebrowsergrouprangekey)
- [let IKImageBrowserGroupStyleKey: String](/documentation/quartz/ikimagebrowsergroupstylekey)
- [let IKImageBrowserGroupTitleKey: String](/documentation/quartz/ikimagebrowsergrouptitlekey)
- [let IKImageBrowserSelectionColorKey: String](/documentation/quartz/ikimagebrowserselectioncolorkey)
- [var IKImageStateInvalid: IKImageBrowserCellState](/documentation/quartz/ikimagestateinvalid)
- [var IKImageStateNoImage: IKImageBrowserCellState](/documentation/quartz/ikimagestatenoimage)
- [var IKImageStateReady: IKImageBrowserCellState](/documentation/quartz/ikimagestateready)
- [let IKOverlayTypeBackground: String](/documentation/quartz/ikoverlaytypebackground)
- [let IKOverlayTypeImage: String](/documentation/quartz/ikoverlaytypeimage)
- [let IKPictureTakerAllowsEditingKey: String](/documentation/quartz/ikpicturetakerallowseditingkey)
- [let IKPictureTakerAllowsFileChoosingKey: String](/documentation/quartz/ikpicturetakerallowsfilechoosingkey)
- [let IKPictureTakerAllowsVideoCaptureKey: String](/documentation/quartz/ikpicturetakerallowsvideocapturekey)
- [let IKPictureTakerImageTransformsKey: String](/documentation/quartz/ikpicturetakerimagetransformskey)
- [let IKPictureTakerInformationalTextKey: String](/documentation/quartz/ikpicturetakerinformationaltextkey)
- [let IKPictureTakerOutputImageMaxSizeKey: String](/documentation/quartz/ikpicturetakeroutputimagemaxsizekey)
- [let IKPictureTakerRemainOpenAfterValidateKey: String](/documentation/quartz/ikpicturetakerremainopenaftervalidatekey)
- [let IKPictureTakerShowAddressBookPicture: String](/documentation/quartz/ikpicturetakershowaddressbookpicture)
- [let IKPictureTakerShowAddressBookPictureKey: String](/documentation/quartz/ikpicturetakershowaddressbookpicturekey)
- [let IKPictureTakerShowEffectsKey: String](/documentation/quartz/ikpicturetakershoweffectskey)
- [let IKPictureTakerShowEmptyPicture: String](/documentation/quartz/ikpicturetakershowemptypicture)
- [let IKPictureTakerShowEmptyPictureKey: String](/documentation/quartz/ikpicturetakershowemptypicturekey)
- [let IKPictureTakerShowRecentPictureKey: String](/documentation/quartz/ikpicturetakershowrecentpicturekey)
- [let IKPictureTakerUpdateRecentPictureKey: String](/documentation/quartz/ikpicturetakerupdaterecentpicturekey)
- [let IKSlideshowAudioFile: String](/documentation/quartz/ikslideshowaudiofile)
- [let IKSlideshowModeImages: String](/documentation/quartz/ikslideshowmodeimages)
- [let IKSlideshowModeOther: String](/documentation/quartz/ikslideshowmodeother)
- [let IKSlideshowModePDF: String](/documentation/quartz/ikslideshowmodepdf)
- [let IKSlideshowPDFDisplayBox: String](/documentation/quartz/ikslideshowpdfdisplaybox)
- [let IKSlideshowPDFDisplayMode: String](/documentation/quartz/ikslideshowpdfdisplaymode)
- [let IKSlideshowPDFDisplaysAsBook: String](/documentation/quartz/ikslideshowpdfdisplaysasbook)
- [let IKSlideshowScreen: String](/documentation/quartz/ikslideshowscreen)
- [let IKSlideshowStartIndex: String](/documentation/quartz/ikslideshowstartindex)
- [let IKSlideshowStartPaused: String](/documentation/quartz/ikslideshowstartpaused)
- [let IKSlideshowWrapAround: String](/documentation/quartz/ikslideshowwraparound)
- [let IKToolModeAnnotate: String](/documentation/quartz/iktoolmodeannotate)
- [let IKToolModeCrop: String](/documentation/quartz/iktoolmodecrop)
- [let IKToolModeMove: String](/documentation/quartz/iktoolmodemove)
- [let IKToolModeNone: String](/documentation/quartz/iktoolmodenone)
- [let IKToolModeRotate: String](/documentation/quartz/iktoolmoderotate)
- [let IKToolModeSelect: String](/documentation/quartz/iktoolmodeselect)
- [let IKToolModeSelectEllipse: String](/documentation/quartz/iktoolmodeselectellipse)
- [let IKToolModeSelectLasso: String](/documentation/quartz/iktoolmodeselectlasso)
- [let IKToolModeSelectRect: String](/documentation/quartz/iktoolmodeselectrect)
- [let IKUIFlavorAllowFallback: String](/documentation/quartz/ikuiflavorallowfallback)
- [let IKUISizeFlavor: String](/documentation/quartz/ikuisizeflavor)
- [let IKUISizeMini: String](/documentation/quartz/ikuisizemini)
- [let IKUISizeRegular: String](/documentation/quartz/ikuisizeregular)
- [let IKUISizeSmall: String](/documentation/quartz/ikuisizesmall)
- [let IKUImaxSize: String](/documentation/quartz/ikuimaxsize)
- [let IK_ApertureBundleIdentifier: String](/documentation/quartz/ik_aperturebundleidentifier)
- [let IK_MailBundleIdentifier: String](/documentation/quartz/ik_mailbundleidentifier)
- [let IK_PhotosBundleIdentifier: String](/documentation/quartz/ik_photosbundleidentifier)
- [let IK_iPhotoBundleIdentifier: String](/documentation/quartz/ik_iphotobundleidentifier)

#### Deprecated constants

- [let IKPictureTakerCropAreaSizeKey: String](/documentation/quartz/ikpicturetakercropareasizekey)
- [let IKPictureTakerShowAddressBookPicture: String](/documentation/quartz/ikpicturetakershowaddressbookpicture)
- [let IKPictureTakerShowEmptyPicture: String](/documentation/quartz/ikpicturetakershowemptypicture)
- [Quartz Enumerations](/documentation/quartz/quartz-enumerations)

#### Enumerations

- [Cell Appearance Style Masks](/documentation/quartz/1564248-cell-appearance-style-masks)

##### Constants

- [var IKCellsStyleNone: Int](/documentation/quartz/ikcellsstylenone)
- [var IKCellsStyleShadowed: Int](/documentation/quartz/ikcellsstyleshadowed)
- [var IKCellsStyleOutlined: Int](/documentation/quartz/ikcellsstyleoutlined)
- [var IKCellsStyleTitled: Int](/documentation/quartz/ikcellsstyletitled)
- [var IKCellsStyleSubtitled: Int](/documentation/quartz/ikcellsstylesubtitled)
- [Group Style Attributes](/documentation/quartz/1564247-group-style-attributes)

##### Constants

- [var IKGroupBezelStyle: Int](/documentation/quartz/ikgroupbezelstyle)
- [var IKGroupDisclosureStyle: Int](/documentation/quartz/ikgroupdisclosurestyle)
- [IKCameraDeviceViewDisplayMode](/documentation/quartz/ikcameradeviceviewdisplaymode)

##### Constants

- [case table](/documentation/quartz/ikcameradeviceviewdisplaymode/table)
- [case icon](/documentation/quartz/ikcameradeviceviewdisplaymode/icon)

##### Enumeration Cases

- [case none](/documentation/quartz/ikcameradeviceviewdisplaymode/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikcameradeviceviewdisplaymode/init(rawvalue:))
- [IKCameraDeviceViewTransferMode](/documentation/quartz/ikcameradeviceviewtransfermode)

##### Constants

- [case fileBased](/documentation/quartz/ikcameradeviceviewtransfermode/filebased)
- [case memoryBased](/documentation/quartz/ikcameradeviceviewtransfermode/memorybased)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikcameradeviceviewtransfermode/init(rawvalue:))
- [IKDeviceBrowserViewDisplayMode](/documentation/quartz/ikdevicebrowserviewdisplaymode)

##### Constants

- [case table](/documentation/quartz/ikdevicebrowserviewdisplaymode/table)
- [case outline](/documentation/quartz/ikdevicebrowserviewdisplaymode/outline)
- [case icon](/documentation/quartz/ikdevicebrowserviewdisplaymode/icon)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikdevicebrowserviewdisplaymode/init(rawvalue:))
- [IKImageBrowserCellState](/documentation/quartz/ikimagebrowsercellstate)

##### Constants

- [var IKImageStateNoImage: IKImageBrowserCellState](/documentation/quartz/ikimagestatenoimage)
- [var IKImageStateInvalid: IKImageBrowserCellState](/documentation/quartz/ikimagestateinvalid)
- [var IKImageStateReady: IKImageBrowserCellState](/documentation/quartz/ikimagestateready)

##### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowsercellstate/rawvalue)
- [IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropoperation)

##### Constants

- [var IKImageBrowserDropOn: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropon)
- [var IKImageBrowserDropBefore: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropbefore)

##### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowserdropoperation/rawvalue)
- [IKScannerDeviceViewDisplayMode](/documentation/quartz/ikscannerdeviceviewdisplaymode)

##### Constants

- [case simple](/documentation/quartz/ikscannerdeviceviewdisplaymode/simple)
- [case advanced](/documentation/quartz/ikscannerdeviceviewdisplaymode/advanced)

##### Enumeration Cases

- [case none](/documentation/quartz/ikscannerdeviceviewdisplaymode/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikscannerdeviceviewdisplaymode/init(rawvalue:))
- [IKScannerDeviceViewTransferMode](/documentation/quartz/ikscannerdeviceviewtransfermode)

##### Constants

- [case fileBased](/documentation/quartz/ikscannerdeviceviewtransfermode/filebased)
- [case memoryBased](/documentation/quartz/ikscannerdeviceviewtransfermode/memorybased)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikscannerdeviceviewtransfermode/init(rawvalue:))

### Deprecated symbols

- [IKImageBrowserView](/documentation/quartz/ikimagebrowserview)

#### Updating the Display of the Content

- [func reloadData()](/documentation/quartz/ikimagebrowserview/reloaddata())

#### Getting and Setting the Delegate

- [var delegate: AnyObject!](/documentation/quartz/ikimagebrowserview/delegate)

#### Getting and Setting the Data Source

- [var dataSource: AnyObject!](/documentation/quartz/ikimagebrowserview/datasource)

#### Setting the Appearance

- [func setCellsStyleMask(Int)](/documentation/quartz/ikimagebrowserview/setcellsstylemask(_:))
- [func cellsStyleMask() -> Int](/documentation/quartz/ikimagebrowserview/cellsstylemask())
- [func setConstrainsToOriginalSize(Bool)](/documentation/quartz/ikimagebrowserview/setconstrainstooriginalsize(_:))
- [func constrainsToOriginalSize() -> Bool](/documentation/quartz/ikimagebrowserview/constrainstooriginalsize())
- [func setIntercellSpacing(NSSize)](/documentation/quartz/ikimagebrowserview/setintercellspacing(_:))
- [func intercellSpacing() -> NSSize](/documentation/quartz/ikimagebrowserview/intercellspacing())

#### Creating a Custom Cell for an Item

- [func newCell(forRepresentedItem: Any!) -> IKImageBrowserCell!](/documentation/quartz/ikimagebrowserview/newcell(forrepresenteditem:))

#### Zooming and Resizing

- [func setZoomValue(Float)](/documentation/quartz/ikimagebrowserview/setzoomvalue(_:))
- [func zoomValue() -> Float](/documentation/quartz/ikimagebrowserview/zoomvalue())
- [func setContentResizingMask(Int)](/documentation/quartz/ikimagebrowserview/setcontentresizingmask(_:))
- [func contentResizingMask() -> Int](/documentation/quartz/ikimagebrowserview/contentresizingmask())

#### Scrolling

- [func scrollIndexToVisible(Int)](/documentation/quartz/ikimagebrowserview/scrollindextovisible(_:))

#### Setting and Getting Cell Size

- [func setCellSize(NSSize)](/documentation/quartz/ikimagebrowserview/setcellsize(_:))
- [func cellSize() -> NSSize](/documentation/quartz/ikimagebrowserview/cellsize())

#### Getting Item Information

- [func indexOfItem(at: NSPoint) -> Int](/documentation/quartz/ikimagebrowserview/indexofitem(at:))
- [func itemFrame(at: Int) -> NSRect](/documentation/quartz/ikimagebrowserview/itemframe(at:))
- [func visibleItemIndexes() -> IndexSet!](/documentation/quartz/ikimagebrowserview/visibleitemindexes())
- [func cellForItem(at: Int) -> IKImageBrowserCell!](/documentation/quartz/ikimagebrowserview/cellforitem(at:))

#### Reordering and Groups Items

- [func selectionIndexes() -> IndexSet!](/documentation/quartz/ikimagebrowserview/selectionindexes())
- [func setSelectionIndexes(IndexSet!, byExtendingSelection: Bool)](/documentation/quartz/ikimagebrowserview/setselectionindexes(_:byextendingselection:))
- [func setAllowsMultipleSelection(Bool)](/documentation/quartz/ikimagebrowserview/setallowsmultipleselection(_:))
- [func allowsMultipleSelection() -> Bool](/documentation/quartz/ikimagebrowserview/allowsmultipleselection())
- [func setAllowsEmptySelection(Bool)](/documentation/quartz/ikimagebrowserview/setallowsemptyselection(_:))
- [func allowsEmptySelection() -> Bool](/documentation/quartz/ikimagebrowserview/allowsemptyselection())
- [func setAllowsReordering(Bool)](/documentation/quartz/ikimagebrowserview/setallowsreordering(_:))
- [func allowsReordering() -> Bool](/documentation/quartz/ikimagebrowserview/allowsreordering())
- [func setAnimates(Bool)](/documentation/quartz/ikimagebrowserview/setanimates(_:))
- [func animates() -> Bool](/documentation/quartz/ikimagebrowserview/animates())
- [func expandGroup(at: Int)](/documentation/quartz/ikimagebrowserview/expandgroup(at:))
- [func collapseGroup(at: Int)](/documentation/quartz/ikimagebrowserview/collapsegroup(at:))
- [func isGroupExpanded(at: Int) -> Bool](/documentation/quartz/ikimagebrowserview/isgroupexpanded(at:))

#### Supporting Drag and Drop

- [func setDraggingDestinationDelegate(Any!)](/documentation/quartz/ikimagebrowserview/setdraggingdestinationdelegate(_:))
- [func draggingDestinationDelegate() -> Any!](/documentation/quartz/ikimagebrowserview/draggingdestinationdelegate())
- [func setDrop(Int, dropOperation: IKImageBrowserDropOperation)](/documentation/quartz/ikimagebrowserview/setdrop(_:dropoperation:))
- [func indexAtLocationOfDroppedItem() -> Int](/documentation/quartz/ikimagebrowserview/indexatlocationofdroppeditem())
- [func setAllowsDroppingOnItems(Bool)](/documentation/quartz/ikimagebrowserview/setallowsdroppingonitems(_:))
- [func allowsDroppingOnItems() -> Bool](/documentation/quartz/ikimagebrowserview/allowsdroppingonitems())
- [func dropOperation() -> IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserview/dropoperation())

#### Core Animation Layer Integration

- [func setForegroundLayer(CALayer!)](/documentation/quartz/ikimagebrowserview/setforegroundlayer(_:))
- [func foregroundLayer() -> CALayer!](/documentation/quartz/ikimagebrowserview/foregroundlayer())
- [func setBackgroundLayer(CALayer!)](/documentation/quartz/ikimagebrowserview/setbackgroundlayer(_:))
- [func backgroundLayer() -> CALayer!](/documentation/quartz/ikimagebrowserview/backgroundlayer())

#### QuickLook Support

- [func setCanControlQuickLookPanel(Bool)](/documentation/quartz/ikimagebrowserview/setcancontrolquicklookpanel(_:))
- [func canControlQuickLookPanel() -> Bool](/documentation/quartz/ikimagebrowserview/cancontrolquicklookpanel())

#### Getting Columns and Rows Information

- [func numberOfColumns() -> Int](/documentation/quartz/ikimagebrowserview/numberofcolumns())
- [func numberOfRows() -> Int](/documentation/quartz/ikimagebrowserview/numberofrows())
- [func rect(ofColumn: Int) -> NSRect](/documentation/quartz/ikimagebrowserview/rect(ofcolumn:))
- [func columnIndexes(in: NSRect) -> IndexSet!](/documentation/quartz/ikimagebrowserview/columnindexes(in:))
- [func rect(ofRow: Int) -> NSRect](/documentation/quartz/ikimagebrowserview/rect(ofrow:))
- [func rowIndexes(in: NSRect) -> IndexSet!](/documentation/quartz/ikimagebrowserview/rowindexes(in:))

#### Constants

- [Cell Appearance Style Masks](/documentation/quartz/1564248-cell-appearance-style-masks)

##### Constants

- [var IKCellsStyleNone: Int](/documentation/quartz/ikcellsstylenone)
- [var IKCellsStyleShadowed: Int](/documentation/quartz/ikcellsstyleshadowed)
- [var IKCellsStyleOutlined: Int](/documentation/quartz/ikcellsstyleoutlined)
- [var IKCellsStyleTitled: Int](/documentation/quartz/ikcellsstyletitled)
- [var IKCellsStyleSubtitled: Int](/documentation/quartz/ikcellsstylesubtitled)
- [Group Style Attributes](/documentation/quartz/1564247-group-style-attributes)

##### Constants

- [var IKGroupBezelStyle: Int](/documentation/quartz/ikgroupbezelstyle)
- [var IKGroupDisclosureStyle: Int](/documentation/quartz/ikgroupdisclosurestyle)
- [View Options Keys](/documentation/quartz/view-options-keys)

##### Constants

- [let IKImageBrowserBackgroundColorKey: String](/documentation/quartz/ikimagebrowserbackgroundcolorkey)
- [let IKImageBrowserSelectionColorKey: String](/documentation/quartz/ikimagebrowserselectioncolorkey)
- [let IKImageBrowserCellsOutlineColorKey: String](/documentation/quartz/ikimagebrowsercellsoutlinecolorkey)
- [let IKImageBrowserCellsTitleAttributesKey: String](/documentation/quartz/ikimagebrowsercellstitleattributeskey)
- [let IKImageBrowserCellsHighlightedTitleAttributesKey: String](/documentation/quartz/ikimagebrowsercellshighlightedtitleattributeskey)
- [let IKImageBrowserCellsSubtitleAttributesKey: String](/documentation/quartz/ikimagebrowsercellssubtitleattributeskey)
- [Group Keys](/documentation/quartz/group-keys)

##### Constants

- [let IKImageBrowserGroupRangeKey: String](/documentation/quartz/ikimagebrowsergrouprangekey)
- [let IKImageBrowserGroupBackgroundColorKey: String](/documentation/quartz/ikimagebrowsergroupbackgroundcolorkey)
- [let IKImageBrowserGroupTitleKey: String](/documentation/quartz/ikimagebrowsergrouptitlekey)
- [let IKImageBrowserGroupStyleKey: String](/documentation/quartz/ikimagebrowsergroupstylekey)
- [let IKImageBrowserGroupHeaderLayer: String](/documentation/quartz/ikimagebrowsergroupheaderlayer)
- [let IKImageBrowserGroupFooterLayer: String](/documentation/quartz/ikimagebrowsergroupfooterlayer)
- [IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropoperation)

##### Constants

- [var IKImageBrowserDropOn: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropon)
- [var IKImageBrowserDropBefore: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropbefore)

##### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowserdropoperation/rawvalue)

## Displaying PDFs

- [PDFKit](/documentation/quartz/pdfkit)

### Views

- [PDFView](/documentation/pdfkit/pdfview)
- [PDFThumbnailView](/documentation/pdfkit/pdfthumbnailview)

### Content Model

- [PDFDocument](/documentation/pdfkit/pdfdocument)
- [PDFPage](/documentation/pdfkit/pdfpage)
- [PDFOutline](/documentation/pdfkit/pdfoutline)
- [PDFSelection](/documentation/pdfkit/pdfselection)

### Annotations

- [Adding Widgets to a PDF Document](/documentation/pdfkit/adding-widgets-to-a-pdf-document)
- [Adding Custom Graphics to a PDF](/documentation/pdfkit/adding-custom-graphics-to-a-pdf)
- [Custom Graphics](/documentation/pdfkit/custom-graphics)
- [PDF Widgets](/documentation/pdfkit/pdf-widgets)
- [PDFAnnotation](/documentation/pdfkit/pdfannotation)
- [PDFAction](/documentation/pdfkit/pdfaction)
- [PDFDestination](/documentation/pdfkit/pdfdestination)
- [PDFAppearanceCharacteristics](/documentation/pdfkit/pdfappearancecharacteristics)
- [PDFBorder](/documentation/pdfkit/pdfborder)
- [Deprecated Annotations](/documentation/quartz/deprecated-annotations)

#### Deprecated Annotation Types

- [PDFAnnotationButtonWidget](/documentation/pdfkit/pdfannotationbuttonwidget)
- [PDFAnnotationChoiceWidget](/documentation/pdfkit/pdfannotationchoicewidget)
- [PDFAnnotationCircle](/documentation/pdfkit/pdfannotationcircle)
- [PDFAnnotationFreeText](/documentation/pdfkit/pdfannotationfreetext)
- [PDFAnnotationInk](/documentation/pdfkit/pdfannotationink)
- [PDFAnnotationLine](/documentation/pdfkit/pdfannotationline)
- [PDFAnnotationLink](/documentation/pdfkit/pdfannotationlink)
- [PDFAnnotationMarkup](/documentation/pdfkit/pdfannotationmarkup)
- [PDFAnnotationPopup](/documentation/pdfkit/pdfannotationpopup)
- [PDFAnnotationSquare](/documentation/pdfkit/pdfannotationsquare)
- [PDFAnnotationStamp](/documentation/pdfkit/pdfannotationstamp)
- [PDFAnnotationText](/documentation/pdfkit/pdfannotationtext)
- [PDFAnnotationTextWidget](/documentation/pdfkit/pdfannotationtextwidget)

### PDFKit Documentation

- [Quartz PDFKit Symbols](/documentation/quartz/quartz-pdfkit)

## Quartz Composer

- [Quartz Composer](/documentation/quartz/quartz-composer)

### Classes

- [QCComposition](/documentation/quartz/qccomposition)

#### Creating a Composition

- [init!(file: String!)](/documentation/quartz/qccomposition/init(file:))
- [init!(data: Data!)](/documentation/quartz/qccomposition/init(data:))

#### Getting Information About a Composition

- [func attributes() -> [AnyHashable : Any]!](/documentation/quartz/qccomposition/attributes())
- [func protocols() -> [Any]!](/documentation/quartz/qccomposition/protocols())
- [func identifier() -> String!](/documentation/quartz/qccomposition/identifier())

#### Getting Port Keys

- [func inputKeys() -> [Any]!](/documentation/quartz/qccomposition/inputkeys())
- [func outputKeys() -> [Any]!](/documentation/quartz/qccomposition/outputkeys())

#### Constants

- [Attribute Keys](/documentation/quartz/attribute-keys)

##### Constants

- [let QCCompositionAttributeNameKey: String](/documentation/quartz/qccompositionattributenamekey)
- [let QCCompositionAttributeDescriptionKey: String](/documentation/quartz/qccompositionattributedescriptionkey)
- [let QCCompositionAttributeCopyrightKey: String](/documentation/quartz/qccompositionattributecopyrightkey)
- [let QCCompositionAttributeBuiltInKey: String](/documentation/quartz/qccompositionattributebuiltinkey)
- [let QCCompositionAttributeHasConsumersKey: String](/documentation/quartz/qccompositionattributehasconsumerskey)
- [let QCCompositionAttributeCategoryKey: String](/documentation/quartz/qccompositionattributecategorykey)
- [Composition Categories](/documentation/quartz/composition-categories)

##### Constants

- [let QCCompositionCategoryDistortion: String](/documentation/quartz/qccompositioncategorydistortion)
- [let QCCompositionCategoryStylize: String](/documentation/quartz/qccompositioncategorystylize)
- [let QCCompositionCategoryUtility: String](/documentation/quartz/qccompositioncategoryutility)
- [Standard Protocol Input Keys](/documentation/quartz/standard-protocol-input-keys)

##### Constants

- [let QCCompositionInputImageKey: String](/documentation/quartz/qccompositioninputimagekey)
- [let QCCompositionInputSourceImageKey: String](/documentation/quartz/qccompositioninputsourceimagekey)
- [let QCCompositionInputDestinationImageKey: String](/documentation/quartz/qccompositioninputdestinationimagekey)
- [let QCCompositionInputRSSFeedURLKey: String](/documentation/quartz/qccompositioninputrssfeedurlkey)
- [let QCCompositionInputRSSArticleDurationKey: String](/documentation/quartz/qccompositioninputrssarticledurationkey)
- [let QCCompositionInputPreviewModeKey: String](/documentation/quartz/qccompositioninputpreviewmodekey)
- [let QCCompositionInputXKey: String](/documentation/quartz/qccompositioninputxkey)
- [let QCCompositionInputYKey: String](/documentation/quartz/qccompositioninputykey)
- [let QCCompositionInputScreenImageKey: String](/documentation/quartz/qccompositioninputscreenimagekey)
- [let QCCompositionInputAudioPeakKey: String](/documentation/quartz/qccompositioninputaudiopeakkey)
- [let QCCompositionInputAudioSpectrumKey: String](/documentation/quartz/qccompositioninputaudiospectrumkey)
- [let QCCompositionInputTrackPositionKey: String](/documentation/quartz/qccompositioninputtrackpositionkey)
- [let QCCompositionInputTrackInfoKey: String](/documentation/quartz/qccompositioninputtrackinfokey)
- [let QCCompositionInputTrackSignalKey: String](/documentation/quartz/qccompositioninputtracksignalkey)
- [let QCCompositionInputPrimaryColorKey: String](/documentation/quartz/qccompositioninputprimarycolorkey)
- [let QCCompositionInputSecondaryColorKey: String](/documentation/quartz/qccompositioninputsecondarycolorkey)
- [let QCCompositionInputPaceKey: String](/documentation/quartz/qccompositioninputpacekey)
- [Standard Protocol Output Keys](/documentation/quartz/standard-protocol-output-keys)

##### Constants

- [let QCCompositionOutputImageKey: String](/documentation/quartz/qccompositionoutputimagekey)
- [let QCCompositionOutputWebPageURLKey: String](/documentation/quartz/qccompositionoutputwebpageurlkey)
- [Standard Protocols](/documentation/quartz/standard-protocols)

##### Constants

- [let QCCompositionProtocolGraphicAnimation: String](/documentation/quartz/qccompositionprotocolgraphicanimation)
- [let QCCompositionProtocolGraphicTransition: String](/documentation/quartz/qccompositionprotocolgraphictransition)
- [let QCCompositionProtocolImageFilter: String](/documentation/quartz/qccompositionprotocolimagefilter)
- [let QCCompositionProtocolScreenSaver: String](/documentation/quartz/qccompositionprotocolscreensaver)
- [let QCCompositionProtocolRSSVisualizer: String](/documentation/quartz/qccompositionprotocolrssvisualizer)
- [let QCCompositionProtocolMusicVisualizer: String](/documentation/quartz/qccompositionprotocolmusicvisualizer)
- [QCCompositionLayer](/documentation/quartz/qccompositionlayer)

#### Creating a Composition Layer

- [init!(file: String!)](/documentation/quartz/qccompositionlayer/init(file:))
- [init!(composition: QCComposition!)](/documentation/quartz/qccompositionlayer/init(composition:))

#### Getting the Composition

- [func composition() -> QCComposition!](/documentation/quartz/qccompositionlayer/composition())
- [QCCompositionParameterView](/documentation/quartz/qccompositionparameterview)

#### Getting and Setting the Renderer

- [func setCompositionRenderer((any QCCompositionRenderer)!)](/documentation/quartz/qccompositionparameterview/setcompositionrenderer(_:))
- [func compositionRenderer() -> (any QCCompositionRenderer)!](/documentation/quartz/qccompositionparameterview/compositionrenderer())

#### Checking for Input Parameters

- [func hasParameters() -> Bool](/documentation/quartz/qccompositionparameterview/hasparameters())

#### Setting and Retrieving the Delegate

- [func setDelegate(Any!)](/documentation/quartz/qccompositionparameterview/setdelegate(_:))
- [func delegate() -> Any!](/documentation/quartz/qccompositionparameterview/delegate())

#### Managing Background Drawing

- [func setDrawsBackground(Bool)](/documentation/quartz/qccompositionparameterview/setdrawsbackground(_:))
- [func drawsBackground() -> Bool](/documentation/quartz/qccompositionparameterview/drawsbackground())

#### Setting and Getting the Background Color

- [func setBackgroundColor(NSColor!)](/documentation/quartz/qccompositionparameterview/setbackgroundcolor(_:))
- [func backgroundColor() -> NSColor!](/documentation/quartz/qccompositionparameterview/backgroundcolor())
- [QCCompositionPickerPanel](/documentation/quartz/qccompositionpickerpanel)

#### Creating the Utility Window for Browsing Compositions

- [class func shared() -> QCCompositionPickerPanel!](/documentation/quartz/qccompositionpickerpanel/shared())

#### Getting the Picker Panel View

- [func compositionPickerView() -> QCCompositionPickerView!](/documentation/quartz/qccompositionpickerpanel/compositionpickerview())
- [QCCompositionPickerView](/documentation/quartz/qccompositionpickerview)

#### Setting and Getting the Background Color

- [func setBackgroundColor(NSColor!)](/documentation/quartz/qccompositionpickerview/setbackgroundcolor(_:))
- [func backgroundColor() -> NSColor!](/documentation/quartz/qccompositionpickerview/backgroundcolor())

#### Managing Background Drawing

- [func setDrawsBackground(Bool)](/documentation/quartz/qccompositionpickerview/setdrawsbackground(_:))
- [func drawsBackground() -> Bool](/documentation/quartz/qccompositionpickerview/drawsbackground())

#### Setting Composition Input Parameters

- [func setDefaultValue(Any!, forInputKey: String!)](/documentation/quartz/qccompositionpickerview/setdefaultvalue(_:forinputkey:))
- [func resetDefaultInputValues()](/documentation/quartz/qccompositionpickerview/resetdefaultinputvalues())

#### Managing Animation

- [func startAnimation(Any!)](/documentation/quartz/qccompositionpickerview/startanimation(_:))
- [func stopAnimation(Any!)](/documentation/quartz/qccompositionpickerview/stopanimation(_:))
- [func isAnimating() -> Bool](/documentation/quartz/qccompositionpickerview/isanimating())
- [func setMaxAnimationFrameRate(Float)](/documentation/quartz/qccompositionpickerview/setmaxanimationframerate(_:))
- [func maxAnimationFrameRate() -> Float](/documentation/quartz/qccompositionpickerview/maxanimationframerate())

#### Controlling Display of Composition Names

- [func setShowsCompositionNames(Bool)](/documentation/quartz/qccompositionpickerview/setshowscompositionnames(_:))
- [func showsCompositionNames() -> Bool](/documentation/quartz/qccompositionpickerview/showscompositionnames())

#### Setting and Retrieving the View Delegate

- [func setDelegate(Any!)](/documentation/quartz/qccompositionpickerview/setdelegate(_:))
- [func delegate() -> Any!](/documentation/quartz/qccompositionpickerview/delegate())

#### Managing the Composition Picker View

- [func setCompositionsFromRepositoryWithProtocol(String!, andAttributes: [AnyHashable : Any]!)](/documentation/quartz/qccompositionpickerview/setcompositionsfromrepositorywithprotocol(_:andattributes:))
- [func compositions() -> [Any]!](/documentation/quartz/qccompositionpickerview/compositions())
- [func setAllowsEmptySelection(Bool)](/documentation/quartz/qccompositionpickerview/setallowsemptyselection(_:))
- [func allowsEmptySelection() -> Bool](/documentation/quartz/qccompositionpickerview/allowsemptyselection())
- [func setCompositionAspectRatio(NSSize)](/documentation/quartz/qccompositionpickerview/setcompositionaspectratio(_:))
- [func compositionAspectRatio() -> NSSize](/documentation/quartz/qccompositionpickerview/compositionaspectratio())
- [func setSelectedComposition(QCComposition!)](/documentation/quartz/qccompositionpickerview/setselectedcomposition(_:))
- [func selectedComposition() -> QCComposition!](/documentation/quartz/qccompositionpickerview/selectedcomposition())

#### Working with Columns and Rows

- [func setNumberOfColumns(Int)](/documentation/quartz/qccompositionpickerview/setnumberofcolumns(_:))
- [func numberOfColumns() -> Int](/documentation/quartz/qccompositionpickerview/numberofcolumns())
- [func setNumberOfRows(Int)](/documentation/quartz/qccompositionpickerview/setnumberofrows(_:))
- [func numberOfRows() -> Int](/documentation/quartz/qccompositionpickerview/numberofrows())
- [QCCompositionRepository](/documentation/quartz/qccompositionrepository)

#### Getting the Composition Repository

- [class func shared() -> QCCompositionRepository!](/documentation/quartz/qccompositionrepository/shared())

#### Fetching Compositions

- [func composition(withIdentifier: String!) -> QCComposition!](/documentation/quartz/qccompositionrepository/composition(withidentifier:))
- [func compositions(withProtocols: [Any]!, andAttributes: [AnyHashable : Any]!) -> [Any]!](/documentation/quartz/qccompositionrepository/compositions(withprotocols:andattributes:))
- [func allCompositions() -> [Any]!](/documentation/quartz/qccompositionrepository/allcompositions())
- [QCPatchController](/documentation/quartz/qcpatchcontroller)
- [QCPlugIn](/documentation/quartz/qcplugin)

#### Defining the Characteristics of a Custom Patch

- [class func executionMode() -> QCPlugInExecutionMode](/documentation/quartz/qcplugin/executionmode())
- [class func timeMode() -> QCPlugInTimeMode](/documentation/quartz/qcplugin/timemode())

#### Executing a Custom Patch

- [func execute((any QCPlugInContext)!, atTime: TimeInterval, withArguments: [AnyHashable : Any]!) -> Bool](/documentation/quartz/qcplugin/execute(_:attime:witharguments:))

#### Performing Custom Tasks During Execution

- [func startExecution((any QCPlugInContext)!) -> Bool](/documentation/quartz/qcplugin/startexecution(_:))
- [func enableExecution((any QCPlugInContext)!)](/documentation/quartz/qcplugin/enableexecution(_:))
- [func disableExecution((any QCPlugInContext)!)](/documentation/quartz/qcplugin/disableexecution(_:))
- [func stopExecution((any QCPlugInContext)!)](/documentation/quartz/qcplugin/stopexecution(_:))

#### Defining Patch and Property Port Attributes

- [class func attributes() -> [AnyHashable : Any]!](/documentation/quartz/qcplugin/attributes())
- [class func attributesForPropertyPort(withKey: String!) -> [AnyHashable : Any]!](/documentation/quartz/qcplugin/attributesforpropertyport(withkey:))

#### Defining Internal Settings

- [func createViewController() -> QCPlugInViewController!](/documentation/quartz/qcplugin/createviewcontroller())
- [class func plugInKeys() -> [Any]!](/documentation/quartz/qcplugin/pluginkeys())

#### Supporting Saving and Retrieving Internal Settings

- [func serializedValue(forKey: String!) -> Any!](/documentation/quartz/qcplugin/serializedvalue(forkey:))
- [func setSerializedValue(Any!, forKey: String!)](/documentation/quartz/qcplugin/setserializedvalue(_:forkey:))

#### Adding Ports Dynamically

- [func addInputPort(withType: String!, forKey: String!, withAttributes: [AnyHashable : Any]!)](/documentation/quartz/qcplugin/addinputport(withtype:forkey:withattributes:))
- [func removeInputPort(forKey: String!)](/documentation/quartz/qcplugin/removeinputport(forkey:))
- [func addOutputPort(withType: String!, forKey: String!, withAttributes: [AnyHashable : Any]!)](/documentation/quartz/qcplugin/addoutputport(withtype:forkey:withattributes:))
- [func removeOutputPort(forKey: String!)](/documentation/quartz/qcplugin/removeoutputport(forkey:))

#### Getting and Setting Port Values

- [func didValue(forInputKeyChange: String!) -> Bool](/documentation/quartz/qcplugin/didvalue(forinputkeychange:))
- [func value(forInputKey: String!) -> Any!](/documentation/quartz/qcplugin/value(forinputkey:))
- [func setValue(Any!, forOutputKey: String!) -> Bool](/documentation/quartz/qcplugin/setvalue(_:foroutputkey:))

#### Loading Bundle and Custom Patches Manually

- [class func load(atPath: String!) -> Bool](/documentation/quartz/qcplugin/load(atpath:))
- [class func registerClass(AnyClass!)](/documentation/quartz/qcplugin/registerclass(_:))

#### Ordering Property Ports

- [class func sortedPropertyPortKeys() -> [Any]!](/documentation/quartz/qcplugin/sortedpropertyportkeys())

#### Constants

- [Patch Attributes](/documentation/quartz/patch-attributes)

##### Constants

- [let QCPlugInAttributeNameKey: String](/documentation/quartz/qcpluginattributenamekey)
- [let QCPlugInAttributeDescriptionKey: String](/documentation/quartz/qcpluginattributedescriptionkey)
- [Input and Output Port Attributes](/documentation/quartz/input-and-output-port-attributes)

##### Constants

- [let QCPortAttributeTypeKey: String](/documentation/quartz/qcportattributetypekey)
- [let QCPortAttributeNameKey: String](/documentation/quartz/qcportattributenamekey)
- [let QCPortAttributeMinimumValueKey: String](/documentation/quartz/qcportattributeminimumvaluekey)
- [let QCPortAttributeMaximumValueKey: String](/documentation/quartz/qcportattributemaximumvaluekey)
- [let QCPortAttributeDefaultValueKey: String](/documentation/quartz/qcportattributedefaultvaluekey)
- [let QCPortAttributeMenuItemsKey: String](/documentation/quartz/qcportattributemenuitemskey)
- [Port Input and Output Types](/documentation/quartz/port-input-and-output-types)

##### Constants

- [let QCPortTypeBoolean: String](/documentation/quartz/qcporttypeboolean)
- [let QCPortTypeIndex: String](/documentation/quartz/qcporttypeindex)
- [let QCPortTypeNumber: String](/documentation/quartz/qcporttypenumber)
- [let QCPortTypeString: String](/documentation/quartz/qcporttypestring)
- [let QCPortTypeColor: String](/documentation/quartz/qcporttypecolor)
- [let QCPortTypeImage: String](/documentation/quartz/qcporttypeimage)
- [let QCPortTypeStructure: String](/documentation/quartz/qcporttypestructure)
- [Pixel Formats](/documentation/quartz/pixel-formats)

##### Constants

- [let QCPlugInPixelFormatARGB8: String](/documentation/quartz/qcpluginpixelformatargb8)
- [let QCPlugInPixelFormatBGRA8: String](/documentation/quartz/qcpluginpixelformatbgra8)
- [let QCPlugInPixelFormatRGBAf: String](/documentation/quartz/qcpluginpixelformatrgbaf)
- [let QCPlugInPixelFormatI8: String](/documentation/quartz/qcpluginpixelformati8)
- [let QCPlugInPixelFormatIf: String](/documentation/quartz/qcpluginpixelformatif)
- [Execution Arguments](/documentation/quartz/execution-arguments)

##### Constants

- [let QCPlugInExecutionArgumentEventKey: String](/documentation/quartz/qcpluginexecutionargumenteventkey)
- [let QCPlugInExecutionArgumentMouseLocationKey: String](/documentation/quartz/qcpluginexecutionargumentmouselocationkey)
- [QCPlugInExecutionMode](/documentation/quartz/qcpluginexecutionmode)

##### Constants

- [var kQCPlugInExecutionModeProvider: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprovider)
- [var kQCPlugInExecutionModeProcessor: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprocessor)
- [var kQCPlugInExecutionModeConsumer: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeconsumer)

##### Initializers

- [init(UInt32)](/documentation/quartz/qcpluginexecutionmode/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/qcpluginexecutionmode/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/qcpluginexecutionmode/rawvalue)
- [QCPlugInTimeMode](/documentation/quartz/qcplugintimemode)

##### Constants

- [var kQCPlugInTimeModeNone: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodenone)
- [var kQCPlugInTimeModeIdle: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodeidle)
- [var kQCPlugInTimeModeTimeBase: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodetimebase)

##### Initializers

- [init(UInt32)](/documentation/quartz/qcplugintimemode/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/qcplugintimemode/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/qcplugintimemode/rawvalue)

#### Instance Methods

- [func executionTime(for: (any QCPlugInContext)!, atTime: TimeInterval, withArguments: [AnyHashable : Any]!) -> TimeInterval](/documentation/quartz/qcplugin/executiontime(for:attime:witharguments:))
- [QCPlugInViewController](/documentation/quartz/qcpluginviewcontroller)

#### Creating a Controller

- [init!(plugIn: QCPlugIn!, viewNibName: String!)](/documentation/quartz/qcpluginviewcontroller/init(plugin:viewnibname:))

#### Getting the QCPlugIn Object

- [func plugIn() -> QCPlugIn!](/documentation/quartz/qcpluginviewcontroller/plugin())
- [QCRenderer](/documentation/quartz/qcrenderer)

#### Creating and Initializing a Renderer

- [init!(composition: QCComposition!, colorSpace: CGColorSpace!)](/documentation/quartz/qcrenderer/init(composition:colorspace:))
- [init!(openGLContext: NSOpenGLContext!, pixelFormat: NSOpenGLPixelFormat!, file: String!)](/documentation/quartz/qcrenderer/init(openglcontext:pixelformat:file:))
- [init!(cglContext: CGLContextObj!, pixelFormat: CGLPixelFormatObj!, colorSpace: CGColorSpace!, composition: QCComposition!)](/documentation/quartz/qcrenderer/init(cglcontext:pixelformat:colorspace:composition:))
- [init!(offScreenWith: NSSize, colorSpace: CGColorSpace!, composition: QCComposition!)](/documentation/quartz/qcrenderer/init(offscreenwith:colorspace:composition:))

#### Rendering a Composition

- [func render(atTime: TimeInterval, arguments: [AnyHashable : Any]!) -> Bool](/documentation/quartz/qcrenderer/render(attime:arguments:))

#### Getting the Composition Object

- [func composition() -> QCComposition!](/documentation/quartz/qcrenderer/composition())

#### Taking Snapshot Images

- [func snapshotImage() -> NSImage!](/documentation/quartz/qcrenderer/snapshotimage())
- [func createSnapshotImage(ofType: String!) -> Any!](/documentation/quartz/qcrenderer/createsnapshotimage(oftype:))

#### Constants

- [Rendering Arguments](/documentation/quartz/rendering-arguments)

##### Constants

- [let QCRendererEventKey: String](/documentation/quartz/qcrenderereventkey)
- [let QCRendererMouseLocationKey: String](/documentation/quartz/qcrenderermouselocationkey)

#### Instance Methods

- [func renderingTime(forTime: TimeInterval, arguments: [AnyHashable : Any]!) -> TimeInterval](/documentation/quartz/qcrenderer/renderingtime(fortime:arguments:))
- [QCView](/documentation/quartz/qcview)

#### Performing Custom Operations During Rendering

- [func render(atTime: TimeInterval, arguments: [AnyHashable : Any]!) -> Bool](/documentation/quartz/qcview/render(attime:arguments:))

#### Loading a Composition

- [func loadComposition(fromFile: String!) -> Bool](/documentation/quartz/qcview/loadcomposition(fromfile:))
- [func load(QCComposition!) -> Bool](/documentation/quartz/qcview/load(_:))
- [func loadedComposition() -> QCComposition!](/documentation/quartz/qcview/loadedcomposition())
- [func unloadComposition()](/documentation/quartz/qcview/unloadcomposition())

#### Managing the Erase Color

- [func erase()](/documentation/quartz/qcview/erase())
- [func eraseColor() -> NSColor!](/documentation/quartz/qcview/erasecolor())
- [func setEraseColor(NSColor!)](/documentation/quartz/qcview/seterasecolor(_:))

#### Setting and Getting Event Masks

- [func eventForwardingMask() -> Int](/documentation/quartz/qcview/eventforwardingmask())
- [func setEventForwardingMask(Int)](/documentation/quartz/qcview/seteventforwardingmask(_:))

#### Setting and Getting the Maximum Frame Rate

- [func maxRenderingFrameRate() -> Float](/documentation/quartz/qcview/maxrenderingframerate())
- [func setMaxRenderingFrameRate(Float)](/documentation/quartz/qcview/setmaxrenderingframerate(_:))

#### Managing Rendering

- [func startRendering() -> Bool](/documentation/quartz/qcview/startrendering())
- [func isRendering() -> Bool](/documentation/quartz/qcview/isrendering())
- [func autostartsRendering() -> Bool](/documentation/quartz/qcview/autostartsrendering())
- [func setAutostartsRendering(Bool)](/documentation/quartz/qcview/setautostartsrendering(_:))
- [func stopRendering()](/documentation/quartz/qcview/stoprendering())
- [func pauseRendering()](/documentation/quartz/qcview/pauserendering())
- [func isPausedRendering() -> Bool](/documentation/quartz/qcview/ispausedrendering())
- [func resumeRendering()](/documentation/quartz/qcview/resumerendering())

#### Using Interface Builder

- [func play(Any!)](/documentation/quartz/qcview/play(_:))
- [func start(Any!)](/documentation/quartz/qcview/start(_:))
- [func stop(Any!)](/documentation/quartz/qcview/stop(_:))

#### Taking Snapshot Images

- [func snapshotImage() -> NSImage!](/documentation/quartz/qcview/snapshotimage())
- [func createSnapshotImage(ofType: String!) -> Any!](/documentation/quartz/qcview/createsnapshotimage(oftype:))

#### Working With OpenGL

- [func openGLContext() -> NSOpenGLContext!](/documentation/quartz/qcview/openglcontext())
- [func openGLPixelFormat() -> NSOpenGLPixelFormat!](/documentation/quartz/qcview/openglpixelformat())

### Protocols

- [QCCompositionParameterViewDelegate](/documentation/quartz/qccompositionparameterviewdelegate)

#### Responding to Composition Selections

- [func compositionParameterView(QCCompositionParameterView!, shouldDisplayParameterWithKey: String!, attributes: [AnyHashable : Any]!) -> Bool](/documentation/objectivec/nsobject-swift.class/compositionparameterview(_:shoulddisplayparameterwithkey:attributes:))

#### Responding when an Input Parameter Changes

- [func compositionParameterView(QCCompositionParameterView!, didChangeParameterWithKey: String!)](/documentation/objectivec/nsobject-swift.class/compositionparameterview(_:didchangeparameterwithkey:))
- [QCCompositionPickerViewDelegate](/documentation/quartz/qccompositionpickerviewdelegate)

#### Responding to Composition Selections

- [func compositionPickerView(QCCompositionPickerView!, didSelect: QCComposition!)](/documentation/objectivec/nsobject-swift.class/compositionpickerview(_:didselect:))

#### Responding to Animation State Changes

- [func compositionPickerViewDidStartAnimating(QCCompositionPickerView!)](/documentation/objectivec/nsobject-swift.class/compositionpickerviewdidstartanimating(_:))
- [func compositionPickerViewWillStopAnimating(QCCompositionPickerView!)](/documentation/objectivec/nsobject-swift.class/compositionpickerviewwillstopanimating(_:))
- [QCCompositionRenderer](/documentation/quartz/qccompositionrenderer)

#### Passing and Retrieving Values From a Composition

- [func setValue(Any!, forInputKey: String!) -> Bool](/documentation/quartz/qccompositionrenderer/setvalue(_:forinputkey:))
- [func value(forInputKey: String!) -> Any!](/documentation/quartz/qccompositionrenderer/value(forinputkey:))
- [func value(forOutputKey: String!) -> Any!](/documentation/quartz/qccompositionrenderer/value(foroutputkey:))
- [func value(forOutputKey: String!, ofType: String!) -> Any!](/documentation/quartz/qccompositionrenderer/value(foroutputkey:oftype:))

#### Getting Input and Output Keys

- [func inputKeys() -> [Any]!](/documentation/quartz/qccompositionrenderer/inputkeys())
- [func outputKeys() -> [Any]!](/documentation/quartz/qccompositionrenderer/outputkeys())

#### Getting Attributes

- [func attributes() -> [AnyHashable : Any]!](/documentation/quartz/qccompositionrenderer/attributes())

#### Storing Arbitrary Information

- [func userInfo() -> NSMutableDictionary!](/documentation/quartz/qccompositionrenderer/userinfo())

#### Saving and Restoring Input Values

- [func propertyListFromInputValues() -> Any!](/documentation/quartz/qccompositionrenderer/propertylistfrominputvalues())
- [func setInputValuesWithPropertyList(Any!)](/documentation/quartz/qccompositionrenderer/setinputvalueswithpropertylist(_:))
- [QCPlugInContext](/documentation/quartz/qcplugincontext)

#### Getting the OpenGL Context

- [func cglContextObj() -> CGLContextObj!](/documentation/quartz/qcplugincontext/cglcontextobj())

#### Getting Execution Context Information

- [func userInfo() -> NSMutableDictionary!](/documentation/quartz/qcplugincontext/userinfo())
- [func bounds() -> NSRect](/documentation/quartz/qcplugincontext/bounds())
- [func colorSpace() -> Unmanaged<CGColorSpace>!](/documentation/quartz/qcplugincontext/colorspace())

#### Getting an Image Provider

- [func outputImageProviderFromBuffer(withPixelFormat: String!, pixelsWide: Int, pixelsHigh: Int, baseAddress: UnsafeRawPointer!, bytesPerRow: Int, releaseCallback: QCPlugInBufferReleaseCallback!, releaseContext: UnsafeMutableRawPointer!, colorSpace: CGColorSpace!, shouldColorMatch: Bool) -> Any!](/documentation/quartz/qcplugincontext/outputimageproviderfrombuffer(withpixelformat:pixelswide:pixelshigh:baseaddress:bytesperrow:releasecallback:releasecontext:colorspace:shouldcolormatch:))
- [func outputImageProviderFromTexture(withPixelFormat: String!, pixelsWide: Int, pixelsHigh: Int, name: GLuint, flipped: Bool, releaseCallback: QCPlugInTextureReleaseCallback!, releaseContext: UnsafeMutableRawPointer!, colorSpace: CGColorSpace!, shouldColorMatch: Bool) -> Any!](/documentation/quartz/qcplugincontext/outputimageproviderfromtexture(withpixelformat:pixelswide:pixelshigh:name:flipped:releasecallback:releasecontext:colorspace:shouldcolormatch:))

#### Instance Methods

- [func compositionURL() -> URL!](/documentation/quartz/qcplugincontext/compositionurl())
- [QCPlugInInputImageSource](/documentation/quartz/qcplugininputimagesource)

#### Converting an Image to a Representation

- [func lockTextureRepresentation(with: CGColorSpace!, forBounds: NSRect) -> Bool](/documentation/quartz/qcplugininputimagesource/locktexturerepresentation(with:forbounds:))
- [func unlockTextureRepresentation()](/documentation/quartz/qcplugininputimagesource/unlocktexturerepresentation())
- [func lockBufferRepresentation(withPixelFormat: String!, colorSpace: CGColorSpace!, forBounds: NSRect) -> Bool](/documentation/quartz/qcplugininputimagesource/lockbufferrepresentation(withpixelformat:colorspace:forbounds:))
- [func bindTextureRepresentation(toCGLContext: CGLContextObj!, textureUnit: GLenum, normalizeCoordinates: Bool)](/documentation/quartz/qcplugininputimagesource/bindtexturerepresentation(tocglcontext:textureunit:normalizecoordinates:))
- [func unbindTextureRepresentation(fromCGLContext: CGLContextObj!, textureUnit: GLenum)](/documentation/quartz/qcplugininputimagesource/unbindtexturerepresentation(fromcglcontext:textureunit:))
- [func unlockBufferRepresentation()](/documentation/quartz/qcplugininputimagesource/unlockbufferrepresentation())

#### Getting Color Space Information

- [func imageColorSpace() -> Unmanaged<CGColorSpace>!](/documentation/quartz/qcplugininputimagesource/imagecolorspace())
- [func shouldColorMatch() -> Bool](/documentation/quartz/qcplugininputimagesource/shouldcolormatch())

#### Getting Texture Information

- [func texturePixelsWide() -> Int](/documentation/quartz/qcplugininputimagesource/texturepixelswide())
- [func texturePixelsHigh() -> Int](/documentation/quartz/qcplugininputimagesource/texturepixelshigh())
- [func textureTarget() -> GLenum](/documentation/quartz/qcplugininputimagesource/texturetarget())
- [func textureName() -> GLuint](/documentation/quartz/qcplugininputimagesource/texturename())
- [func textureColorSpace() -> Unmanaged<CGColorSpace>!](/documentation/quartz/qcplugininputimagesource/texturecolorspace())
- [func textureFlipped() -> Bool](/documentation/quartz/qcplugininputimagesource/textureflipped())
- [func textureMatrix() -> UnsafePointer<GLfloat>!](/documentation/quartz/qcplugininputimagesource/texturematrix())

#### Getting Image Buffer Information

- [func imageBounds() -> NSRect](/documentation/quartz/qcplugininputimagesource/imagebounds())
- [func bufferPixelsWide() -> Int](/documentation/quartz/qcplugininputimagesource/bufferpixelswide())
- [func bufferPixelsHigh() -> Int](/documentation/quartz/qcplugininputimagesource/bufferpixelshigh())
- [func bufferPixelFormat() -> String!](/documentation/quartz/qcplugininputimagesource/bufferpixelformat())
- [func bufferColorSpace() -> Unmanaged<CGColorSpace>!](/documentation/quartz/qcplugininputimagesource/buffercolorspace())
- [func bufferBaseAddress() -> UnsafeRawPointer!](/documentation/quartz/qcplugininputimagesource/bufferbaseaddress())
- [func bufferBytesPerRow() -> Int](/documentation/quartz/qcplugininputimagesource/bufferbytesperrow())
- [QCPlugInOutputImageProvider](/documentation/quartz/qcpluginoutputimageprovider)

#### Rendering an Image to a Destination

- [func render(toBuffer: UnsafeMutableRawPointer!, withBytesPerRow: Int, pixelFormat: String!, forBounds: NSRect) -> Bool](/documentation/quartz/qcpluginoutputimageprovider/render(tobuffer:withbytesperrow:pixelformat:forbounds:))
- [func copyRenderedTexture(forCGLContext: CGLContextObj!, pixelFormat: String!, bounds: NSRect, isFlipped: UnsafeMutablePointer<ObjCBool>!) -> GLuint](/documentation/quartz/qcpluginoutputimageprovider/copyrenderedtexture(forcglcontext:pixelformat:bounds:isflipped:))
- [func render(withCGLContext: CGLContextObj!, forBounds: NSRect) -> Bool](/documentation/quartz/qcpluginoutputimageprovider/render(withcglcontext:forbounds:))
- [func releaseRenderedTexture(GLuint, forCGLContext: CGLContextObj!)](/documentation/quartz/qcpluginoutputimageprovider/releaserenderedtexture(_:forcglcontext:))

#### Providing Information About the Image

- [func imageBounds() -> NSRect](/documentation/quartz/qcpluginoutputimageprovider/imagebounds())
- [func imageColorSpace() -> Unmanaged<CGColorSpace>!](/documentation/quartz/qcpluginoutputimageprovider/imagecolorspace())
- [func shouldColorMatch() -> Bool](/documentation/quartz/qcpluginoutputimageprovider/shouldcolormatch())

#### Providing Information About the Rendering Destination

- [func supportedBufferPixelFormats() -> [Any]!](/documentation/quartz/qcpluginoutputimageprovider/supportedbufferpixelformats())
- [func supportedRenderedTexturePixelFormats() -> [Any]!](/documentation/quartz/qcpluginoutputimageprovider/supportedrenderedtexturepixelformats())
- [func canRender(withCGLContext: CGLContextObj!) -> Bool](/documentation/quartz/qcpluginoutputimageprovider/canrender(withcglcontext:))

### Structures

- [QCPlugInExecutionMode](/documentation/quartz/qcpluginexecutionmode)

#### Constants

- [var kQCPlugInExecutionModeProvider: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprovider)
- [var kQCPlugInExecutionModeProcessor: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprocessor)
- [var kQCPlugInExecutionModeConsumer: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeconsumer)

#### Initializers

- [init(UInt32)](/documentation/quartz/qcpluginexecutionmode/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/qcpluginexecutionmode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/qcpluginexecutionmode/rawvalue)
- [QCPlugInTimeMode](/documentation/quartz/qcplugintimemode)

#### Constants

- [var kQCPlugInTimeModeNone: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodenone)
- [var kQCPlugInTimeModeIdle: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodeidle)
- [var kQCPlugInTimeModeTimeBase: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodetimebase)

#### Initializers

- [init(UInt32)](/documentation/quartz/qcplugintimemode/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/qcplugintimemode/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/qcplugintimemode/rawvalue)

### Reference

- [Quartz Data Types](/documentation/quartz/quartz-data-types)

#### Data Types

- [QCPlugInBufferReleaseCallback](/documentation/quartz/qcpluginbufferreleasecallback)
- [QCPlugInTextureReleaseCallback](/documentation/quartz/qcplugintexturereleasecallback)
- [Quartz Constants](/documentation/quartz/quartz-constants)

#### Constants

- [var globalUpdateOK: DarwinBoolean](/documentation/quartz/globalupdateok)
- [let kQuartzFilterApplicationDomain: String](/documentation/quartz/kquartzfilterapplicationdomain)
- [let kQuartzFilterPDFWorkflowDomain: String](/documentation/quartz/kquartzfilterpdfworkflowdomain)
- [let kQuartzFilterPrintingDomain: String](/documentation/quartz/kquartzfilterprintingdomain)

#### Deprecated constants

- [let QCCompositionAttributeIsTimeDependentKey: String](/documentation/quartz/qccompositionattributeistimedependentkey)
- [let QCPlugInAttributeCategoriesKey: String](/documentation/quartz/qcpluginattributecategorieskey)
- [let QCPlugInAttributeCopyrightKey: String](/documentation/quartz/qcpluginattributecopyrightkey)
- [let QCPlugInAttributeExamplesKey: String](/documentation/quartz/qcpluginattributeexampleskey)
- [Quartz Enumerations](/documentation/quartz/quartz-enumerations)

#### Enumerations

- [Cell Appearance Style Masks](/documentation/quartz/1564248-cell-appearance-style-masks)

##### Constants

- [var IKCellsStyleNone: Int](/documentation/quartz/ikcellsstylenone)
- [var IKCellsStyleShadowed: Int](/documentation/quartz/ikcellsstyleshadowed)
- [var IKCellsStyleOutlined: Int](/documentation/quartz/ikcellsstyleoutlined)
- [var IKCellsStyleTitled: Int](/documentation/quartz/ikcellsstyletitled)
- [var IKCellsStyleSubtitled: Int](/documentation/quartz/ikcellsstylesubtitled)
- [Group Style Attributes](/documentation/quartz/1564247-group-style-attributes)

##### Constants

- [var IKGroupBezelStyle: Int](/documentation/quartz/ikgroupbezelstyle)
- [var IKGroupDisclosureStyle: Int](/documentation/quartz/ikgroupdisclosurestyle)
- [IKCameraDeviceViewDisplayMode](/documentation/quartz/ikcameradeviceviewdisplaymode)

##### Constants

- [case table](/documentation/quartz/ikcameradeviceviewdisplaymode/table)
- [case icon](/documentation/quartz/ikcameradeviceviewdisplaymode/icon)

##### Enumeration Cases

- [case none](/documentation/quartz/ikcameradeviceviewdisplaymode/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikcameradeviceviewdisplaymode/init(rawvalue:))
- [IKCameraDeviceViewTransferMode](/documentation/quartz/ikcameradeviceviewtransfermode)

##### Constants

- [case fileBased](/documentation/quartz/ikcameradeviceviewtransfermode/filebased)
- [case memoryBased](/documentation/quartz/ikcameradeviceviewtransfermode/memorybased)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikcameradeviceviewtransfermode/init(rawvalue:))
- [IKDeviceBrowserViewDisplayMode](/documentation/quartz/ikdevicebrowserviewdisplaymode)

##### Constants

- [case table](/documentation/quartz/ikdevicebrowserviewdisplaymode/table)
- [case outline](/documentation/quartz/ikdevicebrowserviewdisplaymode/outline)
- [case icon](/documentation/quartz/ikdevicebrowserviewdisplaymode/icon)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikdevicebrowserviewdisplaymode/init(rawvalue:))
- [IKImageBrowserCellState](/documentation/quartz/ikimagebrowsercellstate)

##### Constants

- [var IKImageStateNoImage: IKImageBrowserCellState](/documentation/quartz/ikimagestatenoimage)
- [var IKImageStateInvalid: IKImageBrowserCellState](/documentation/quartz/ikimagestateinvalid)
- [var IKImageStateReady: IKImageBrowserCellState](/documentation/quartz/ikimagestateready)

##### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowsercellstate/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowsercellstate/rawvalue)
- [IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropoperation)

##### Constants

- [var IKImageBrowserDropOn: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropon)
- [var IKImageBrowserDropBefore: IKImageBrowserDropOperation](/documentation/quartz/ikimagebrowserdropbefore)

##### Initializers

- [init(UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/ikimagebrowserdropoperation/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/ikimagebrowserdropoperation/rawvalue)
- [IKScannerDeviceViewDisplayMode](/documentation/quartz/ikscannerdeviceviewdisplaymode)

##### Constants

- [case simple](/documentation/quartz/ikscannerdeviceviewdisplaymode/simple)
- [case advanced](/documentation/quartz/ikscannerdeviceviewdisplaymode/advanced)

##### Enumeration Cases

- [case none](/documentation/quartz/ikscannerdeviceviewdisplaymode/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikscannerdeviceviewdisplaymode/init(rawvalue:))
- [IKScannerDeviceViewTransferMode](/documentation/quartz/ikscannerdeviceviewtransfermode)

##### Constants

- [case fileBased](/documentation/quartz/ikscannerdeviceviewtransfermode/filebased)
- [case memoryBased](/documentation/quartz/ikscannerdeviceviewtransfermode/memorybased)

##### Initializers

- [init?(rawValue: Int)](/documentation/quartz/ikscannerdeviceviewtransfermode/init(rawvalue:))
- [Quartz Composer Constants](/documentation/quartz/quartz-composer-constants)

#### Constants

- [let QCCompositionAttributeBuiltInKey: String](/documentation/quartz/qccompositionattributebuiltinkey)
- [let QCCompositionAttributeCategoryKey: String](/documentation/quartz/qccompositionattributecategorykey)
- [let QCCompositionAttributeCopyrightKey: String](/documentation/quartz/qccompositionattributecopyrightkey)
- [let QCCompositionAttributeDescriptionKey: String](/documentation/quartz/qccompositionattributedescriptionkey)
- [let QCCompositionAttributeHasConsumersKey: String](/documentation/quartz/qccompositionattributehasconsumerskey)
- [let QCCompositionAttributeIsTimeDependentKey: String](/documentation/quartz/qccompositionattributeistimedependentkey)
- [let QCCompositionAttributeNameKey: String](/documentation/quartz/qccompositionattributenamekey)
- [let QCCompositionCategoryDistortion: String](/documentation/quartz/qccompositioncategorydistortion)
- [let QCCompositionCategoryStylize: String](/documentation/quartz/qccompositioncategorystylize)
- [let QCCompositionCategoryUtility: String](/documentation/quartz/qccompositioncategoryutility)
- [let QCCompositionInputAudioPeakKey: String](/documentation/quartz/qccompositioninputaudiopeakkey)
- [let QCCompositionInputAudioSpectrumKey: String](/documentation/quartz/qccompositioninputaudiospectrumkey)
- [let QCCompositionInputDestinationImageKey: String](/documentation/quartz/qccompositioninputdestinationimagekey)
- [let QCCompositionInputImageKey: String](/documentation/quartz/qccompositioninputimagekey)
- [let QCCompositionInputPaceKey: String](/documentation/quartz/qccompositioninputpacekey)
- [let QCCompositionInputPreviewModeKey: String](/documentation/quartz/qccompositioninputpreviewmodekey)
- [let QCCompositionInputPrimaryColorKey: String](/documentation/quartz/qccompositioninputprimarycolorkey)
- [let QCCompositionInputRSSArticleDurationKey: String](/documentation/quartz/qccompositioninputrssarticledurationkey)
- [let QCCompositionInputRSSFeedURLKey: String](/documentation/quartz/qccompositioninputrssfeedurlkey)
- [let QCCompositionInputScreenImageKey: String](/documentation/quartz/qccompositioninputscreenimagekey)
- [let QCCompositionInputSecondaryColorKey: String](/documentation/quartz/qccompositioninputsecondarycolorkey)
- [let QCCompositionInputSourceImageKey: String](/documentation/quartz/qccompositioninputsourceimagekey)
- [let QCCompositionInputTrackInfoKey: String](/documentation/quartz/qccompositioninputtrackinfokey)
- [let QCCompositionInputTrackPositionKey: String](/documentation/quartz/qccompositioninputtrackpositionkey)
- [let QCCompositionInputTrackSignalKey: String](/documentation/quartz/qccompositioninputtracksignalkey)
- [let QCCompositionInputXKey: String](/documentation/quartz/qccompositioninputxkey)
- [let QCCompositionInputYKey: String](/documentation/quartz/qccompositioninputykey)
- [let QCCompositionOutputImageKey: String](/documentation/quartz/qccompositionoutputimagekey)
- [let QCCompositionOutputWebPageURLKey: String](/documentation/quartz/qccompositionoutputwebpageurlkey)
- [let QCCompositionProtocolGraphicAnimation: String](/documentation/quartz/qccompositionprotocolgraphicanimation)
- [let QCCompositionProtocolGraphicTransition: String](/documentation/quartz/qccompositionprotocolgraphictransition)
- [let QCCompositionProtocolImageFilter: String](/documentation/quartz/qccompositionprotocolimagefilter)
- [let QCCompositionProtocolMusicVisualizer: String](/documentation/quartz/qccompositionprotocolmusicvisualizer)
- [let QCCompositionProtocolRSSVisualizer: String](/documentation/quartz/qccompositionprotocolrssvisualizer)
- [let QCCompositionProtocolScreenSaver: String](/documentation/quartz/qccompositionprotocolscreensaver)
- [let QCPlugInAttributeCategoriesKey: String](/documentation/quartz/qcpluginattributecategorieskey)
- [let QCPlugInAttributeCopyrightKey: String](/documentation/quartz/qcpluginattributecopyrightkey)
- [let QCPlugInAttributeDescriptionKey: String](/documentation/quartz/qcpluginattributedescriptionkey)
- [let QCPlugInAttributeExamplesKey: String](/documentation/quartz/qcpluginattributeexampleskey)
- [let QCPlugInAttributeNameKey: String](/documentation/quartz/qcpluginattributenamekey)
- [let QCPlugInExecutionArgumentEventKey: String](/documentation/quartz/qcpluginexecutionargumenteventkey)
- [let QCPlugInExecutionArgumentMouseLocationKey: String](/documentation/quartz/qcpluginexecutionargumentmouselocationkey)
- [let QCPlugInPixelFormatARGB8: String](/documentation/quartz/qcpluginpixelformatargb8)
- [let QCPlugInPixelFormatBGRA8: String](/documentation/quartz/qcpluginpixelformatbgra8)
- [let QCPlugInPixelFormatI8: String](/documentation/quartz/qcpluginpixelformati8)
- [let QCPlugInPixelFormatIf: String](/documentation/quartz/qcpluginpixelformatif)
- [let QCPlugInPixelFormatRGBAf: String](/documentation/quartz/qcpluginpixelformatrgbaf)
- [let QCPortAttributeDefaultValueKey: String](/documentation/quartz/qcportattributedefaultvaluekey)
- [let QCPortAttributeMaximumValueKey: String](/documentation/quartz/qcportattributemaximumvaluekey)
- [let QCPortAttributeMenuItemsKey: String](/documentation/quartz/qcportattributemenuitemskey)
- [let QCPortAttributeMinimumValueKey: String](/documentation/quartz/qcportattributeminimumvaluekey)
- [let QCPortAttributeNameKey: String](/documentation/quartz/qcportattributenamekey)
- [let QCPortAttributeTypeKey: String](/documentation/quartz/qcportattributetypekey)
- [let QCPortTypeBoolean: String](/documentation/quartz/qcporttypeboolean)
- [let QCPortTypeColor: String](/documentation/quartz/qcporttypecolor)
- [let QCPortTypeImage: String](/documentation/quartz/qcporttypeimage)
- [let QCPortTypeIndex: String](/documentation/quartz/qcporttypeindex)
- [let QCPortTypeNumber: String](/documentation/quartz/qcporttypenumber)
- [let QCPortTypeString: String](/documentation/quartz/qcporttypestring)
- [let QCPortTypeStructure: String](/documentation/quartz/qcporttypestructure)
- [let QCRendererEventKey: String](/documentation/quartz/qcrenderereventkey)
- [let QCRendererMouseLocationKey: String](/documentation/quartz/qcrenderermouselocationkey)
- [var kQCPlugInExecutionModeConsumer: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeconsumer)
- [var kQCPlugInExecutionModeProcessor: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprocessor)
- [var kQCPlugInExecutionModeProvider: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprovider)
- [var kQCPlugInTimeModeIdle: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodeidle)
- [var kQCPlugInTimeModeNone: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodenone)
- [var kQCPlugInTimeModeTimeBase: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodetimebase)
- [Quartz Composer Enumerations](/documentation/quartz/quartz-composer-enumerations)

#### Enumerations

- [QCPlugInExecutionMode](/documentation/quartz/qcpluginexecutionmode)

##### Constants

- [var kQCPlugInExecutionModeProvider: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprovider)
- [var kQCPlugInExecutionModeProcessor: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeprocessor)
- [var kQCPlugInExecutionModeConsumer: QCPlugInExecutionMode](/documentation/quartz/kqcpluginexecutionmodeconsumer)

##### Initializers

- [init(UInt32)](/documentation/quartz/qcpluginexecutionmode/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/qcpluginexecutionmode/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/qcpluginexecutionmode/rawvalue)
- [QCPlugInTimeMode](/documentation/quartz/qcplugintimemode)

##### Constants

- [var kQCPlugInTimeModeNone: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodenone)
- [var kQCPlugInTimeModeIdle: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodeidle)
- [var kQCPlugInTimeModeTimeBase: QCPlugInTimeMode](/documentation/quartz/kqcplugintimemodetimebase)

##### Initializers

- [init(UInt32)](/documentation/quartz/qcplugintimemode/init(_:))
- [init(rawValue: UInt32)](/documentation/quartz/qcplugintimemode/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/quartz/qcplugintimemode/rawvalue)

## Using Quick Look

- [Quick Look](/documentation/quartz/quick-look)

### Classes

- [QLPreviewView](/documentation/quicklookui/qlpreviewview)
- [QLPreviewViewStyle](/documentation/quicklookui/qlpreviewviewstyle)

### Protocols

- [QLPreviewItem](/documentation/quicklook/qlpreviewitem)
- [QLPreviewPanelDataSource](/documentation/quicklookui/qlpreviewpaneldatasource)
- [QLPreviewPanelDelegate](/documentation/quicklookui/qlpreviewpaneldelegate)

## Conversion Filters

- [Quartz Filter](/documentation/quartz/quartz-filter)

### Classes

- [QuartzFilter](/documentation/quartz/quartzfilter)

#### Initializers

- [init!(outputIntents: [Any]!)](/documentation/quartz/quartzfilter/init(outputintents:))
- [init!(properties: [AnyHashable : Any]!)](/documentation/quartz/quartzfilter/init(properties:))
- [init!(url: URL!)](/documentation/quartz/quartzfilter/init(url:))

#### Instance Methods

- [func apply(to: CGContext!) -> Bool](/documentation/quartz/quartzfilter/apply(to:))
- [func localizedName() -> String!](/documentation/quartz/quartzfilter/localizedname())
- [func properties() -> [AnyHashable : Any]!](/documentation/quartz/quartzfilter/properties())
- [func remove(from: CGContext!)](/documentation/quartz/quartzfilter/remove(from:))
- [func url() -> URL!](/documentation/quartz/quartzfilter/url())
- [QuartzFilterManager](/documentation/quartz/quartzfiltermanager)

#### Instance Methods

- [func delegate() -> Any!](/documentation/quartz/quartzfiltermanager/delegate())
- [func filterPanel() -> NSPanel!](/documentation/quartz/quartzfiltermanager/filterpanel())
- [func filterView() -> QuartzFilterView!](/documentation/quartz/quartzfiltermanager/filterview())
- [func importFilter([AnyHashable : Any]!) -> QuartzFilter!](/documentation/quartz/quartzfiltermanager/importfilter(_:))
- [func select(QuartzFilter!) -> Bool](/documentation/quartz/quartzfiltermanager/select(_:))
- [func selectedFilter() -> QuartzFilter!](/documentation/quartz/quartzfiltermanager/selectedfilter())
- [func setDelegate(Any!)](/documentation/quartz/quartzfiltermanager/setdelegate(_:))

#### Type Methods

- [class func filters(inDomains: [Any]!) -> [Any]!](/documentation/quartz/quartzfiltermanager/filters(indomains:))
- [QuartzFilterView](/documentation/quartz/quartzfilterview)

#### Instance Methods

- [func sizeToFit()](/documentation/quartz/quartzfilterview/sizetofit())

### Reference

- [Quartz Filter Constants](/documentation/quartz/quartz-filter-constants)

#### Constants

- [let kQuartzFilterApplicationDomain: String](/documentation/quartz/kquartzfilterapplicationdomain)
- [let kQuartzFilterPDFWorkflowDomain: String](/documentation/quartz/kquartzfilterpdfworkflowdomain)
- [let kQuartzFilterPrintingDomain: String](/documentation/quartz/kquartzfilterprintingdomain)

## Constants

- [Quartz Constants](/documentation/quartz/quartz-constants)

### Constants

- [var globalUpdateOK: DarwinBoolean](/documentation/quartz/globalupdateok)
- [let kQuartzFilterApplicationDomain: String](/documentation/quartz/kquartzfilterapplicationdomain)
- [let kQuartzFilterPDFWorkflowDomain: String](/documentation/quartz/kquartzfilterpdfworkflowdomain)
- [let kQuartzFilterPrintingDomain: String](/documentation/quartz/kquartzfilterprintingdomain)

### Deprecated constants

- [let QCCompositionAttributeIsTimeDependentKey: String](/documentation/quartz/qccompositionattributeistimedependentkey)
- [let QCPlugInAttributeCategoriesKey: String](/documentation/quartz/qcpluginattributecategorieskey)
- [let QCPlugInAttributeCopyrightKey: String](/documentation/quartz/qcpluginattributecopyrightkey)
- [let QCPlugInAttributeExamplesKey: String](/documentation/quartz/qcpluginattributeexampleskey)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
