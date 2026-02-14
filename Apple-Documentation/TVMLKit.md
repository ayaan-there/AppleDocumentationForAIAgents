# TVMLKit Documentation

Source: https://sosumi.ai/documentation/tvmlkit

---
title: TVMLKit
source: https://developer.apple.com/documentation/tvmlkit
timestamp: 2026-02-13T19:04:41.405Z
---

## JavaScript Environment

- [Implementing a Hybrid TV App with TVMLKit](/documentation/tvmlkit/implementing-a-hybrid-tv-app-with-tvmlkit)
- [TVApplicationController](/documentation/tvmlkit/tvapplicationcontroller)

### Creating a New App Controller

- [init(context: TVApplicationControllerContext, window: UIWindow?, delegate: (any TVApplicationControllerDelegate)?)](/documentation/tvmlkit/tvapplicationcontroller/init(context:window:delegate:))

### Controlling and Handling Events

- [func evaluate(inJavaScriptContext: (JSContext) -> Void, completion: ((Bool) -> Void)?)](/documentation/tvmlkit/tvapplicationcontroller/evaluate(injavascriptcontext:completion:))
- [func stop()](/documentation/tvmlkit/tvapplicationcontroller/stop())

### Getting the Delegate

- [var delegate: (any TVApplicationControllerDelegate)?](/documentation/tvmlkit/tvapplicationcontroller/delegate)
- [TVApplicationControllerDelegate](/documentation/tvmlkit/tvapplicationcontrollerdelegate)

#### Managing the App Controller

- [func appController(TVApplicationController, didFail: any Error)](/documentation/tvmlkit/tvapplicationcontrollerdelegate/appcontroller(_:didfail:))
- [func appController(TVApplicationController, didFinishLaunching: [String : Any]?)](/documentation/tvmlkit/tvapplicationcontrollerdelegate/appcontroller(_:didfinishlaunching:))
- [func appController(TVApplicationController, didStop: [String : Any]?)](/documentation/tvmlkit/tvapplicationcontrollerdelegate/appcontroller(_:didstop:))
- [func appController(TVApplicationController, evaluateAppJavaScriptIn: JSContext)](/documentation/tvmlkit/tvapplicationcontrollerdelegate/appcontroller(_:evaluateappjavascriptin:))
- [func player(for: TVApplicationController) -> TVPlayer?](/documentation/tvmlkit/tvapplicationcontrollerdelegate/player(for:))

### Examining App Controller Properties

- [var context: TVApplicationControllerContext](/documentation/tvmlkit/tvapplicationcontroller/context)
- [var navigationController: UINavigationController](/documentation/tvmlkit/tvapplicationcontroller/navigationcontroller)
- [var window: UIWindow?](/documentation/tvmlkit/tvapplicationcontroller/window)
- [TVApplicationControllerContext](/documentation/tvmlkit/tvapplicationcontrollercontext)

### Providing Launch Information

- [var javaScriptApplicationURL: URL](/documentation/tvmlkit/tvapplicationcontrollercontext/javascriptapplicationurl)
- [var launchOptions: [String : Any]](/documentation/tvmlkit/tvapplicationcontrollercontext/launchoptions)
- [var storageIdentifier: String?](/documentation/tvmlkit/tvapplicationcontrollercontext/storageidentifier)
- [var supportsPictureInPicturePlayback: Bool](/documentation/tvmlkit/tvapplicationcontrollercontext/supportspictureinpictureplayback)

## Views and View Controllers

- [TVViewElement](/documentation/tvmlkit/tvviewelement)

### Inspecting a View Element

- [var autoHighlightIdentifier: String?](/documentation/tvmlkit/tvviewelement/autohighlightidentifier)
- [var attributes: [String : String]?](/documentation/tvmlkit/tvviewelement/attributes)
- [var children: [TVViewElement]?](/documentation/tvmlkit/tvviewelement/children)
- [var isDisabled: Bool](/documentation/tvmlkit/tvviewelement/isdisabled)
- [var identifier: String](/documentation/tvmlkit/tvviewelement/identifier)
- [var name: String](/documentation/tvmlkit/tvviewelement/name)
- [var parent: TVViewElement?](/documentation/tvmlkit/tvviewelement/parent)
- [var style: TVViewElementStyle?](/documentation/tvmlkit/tvviewelement/style)
- [var updateType: TVElementUpdateType](/documentation/tvmlkit/tvviewelement/updatetype)
- [TVElementUpdateType](/documentation/tvmlkit/tvelementupdatetype)

#### Constants

- [case none](/documentation/tvmlkit/tvelementupdatetype/none)
- [case subtree](/documentation/tvmlkit/tvelementupdatetype/subtree)
- [case children](/documentation/tvmlkit/tvelementupdatetype/children)
- [case node](/documentation/tvmlkit/tvelementupdatetype/node)

#### Enumeration Cases

- [case styles](/documentation/tvmlkit/tvelementupdatetype/styles)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvelementupdatetype/init(rawvalue:))

### Dispatching Events

- [func dispatchEvent(type: TVElementEventType, canBubble: Bool, cancellable: Bool, extraInfo: [String : Any]?, completion: ((Bool, Bool) -> Void)?)](/documentation/tvmlkit/tvviewelement/dispatchevent(type:canbubble:cancellable:extrainfo:completion:))
- [TVElementEventType](/documentation/tvmlkit/tvelementeventtype)

#### Enumeration Cases

- [case change](/documentation/tvmlkit/tvelementeventtype/change)
- [case highlight](/documentation/tvmlkit/tvelementeventtype/highlight)
- [case holdSelect](/documentation/tvmlkit/tvelementeventtype/holdselect)
- [case play](/documentation/tvmlkit/tvelementeventtype/play)
- [case select](/documentation/tvmlkit/tvelementeventtype/select)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvelementeventtype/init(rawvalue:))
- [func dispatchEvent(name: String, canBubble: Bool, cancellable: Bool, extraInfo: [String : Any]?, completion: ((Bool, Bool) -> Void)?)](/documentation/tvmlkit/tvviewelement/dispatchevent(name:canbubble:cancellable:extrainfo:completion:))

### Resetting a Property’s Value

- [func resetProperty(TVElementResettableProperty)](/documentation/tvmlkit/tvviewelement/resetproperty(_:))
- [TVElementResettableProperty](/documentation/tvmlkit/tvelementresettableproperty)

#### Constants

- [case updateType](/documentation/tvmlkit/tvelementresettableproperty/updatetype)
- [case autoHighlightIdentifier](/documentation/tvmlkit/tvelementresettableproperty/autohighlightidentifier)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvelementresettableproperty/init(rawvalue:))

### Instance Properties

- [var elementData: [String : Any]](/documentation/tvmlkit/tvviewelement/elementdata)
- [TVInterfaceCreating](/documentation/tvmlkit/tvinterfacecreating)

### Retrieving Resource Information

- [func resourceImage(name: String) -> UIImage?](/documentation/tvmlkit/tvinterfacecreating/resourceimage(name:))
- [func resourceURL(name: String) -> URL?](/documentation/tvmlkit/tvinterfacecreating/resourceurl(name:))

### Updating View Information

- [func makeViewController(element: TVViewElement, existingViewController: UIViewController?) -> UIViewController?](/documentation/tvmlkit/tvinterfacecreating/makeviewcontroller(element:existingviewcontroller:))
- [func makeView(element: TVViewElement, existingView: UIView?) -> UIView?](/documentation/tvmlkit/tvinterfacecreating/makeview(element:existingview:))
- [func collectionViewCellClass(for: TVViewElement) -> AnyClass?](/documentation/tvmlkit/tvinterfacecreating/collectionviewcellclass(for:))
- [func playerViewController(for: TVPlayer) -> UIViewController?](/documentation/tvmlkit/tvinterfacecreating/playerviewcontroller(for:))
- [TVInterfaceFactory](/documentation/tvmlkit/tvinterfacefactory)

### Extending an Interface

- [var extendedInterfaceCreator: (any TVInterfaceCreating)?](/documentation/tvmlkit/tvinterfacefactory/extendedinterfacecreator)
- [class func shared() -> Self](/documentation/tvmlkit/tvinterfacefactory/shared())
- [TVBrowserViewController](/documentation/tvmlkit/tvbrowserviewcontroller)

### Initializing the Browser View Controller

- [convenience init?(viewElement: TVViewElement)](/documentation/tvmlkit/tvbrowserviewcontroller/init(viewelement:))

### Providing the Browser’s Data

- [var dataSource: (any TVBrowserViewControllerDataSource)?](/documentation/tvmlkit/tvbrowserviewcontroller/datasource)
- [TVBrowserViewControllerDataSource](/documentation/tvmlkit/tvbrowserviewcontrollerdatasource)

#### Providing Data

- [func browserViewController(TVBrowserViewController, documentViewControllerFor: TVViewElement) -> TVDocumentViewController?](/documentation/tvmlkit/tvbrowserviewcontrollerdatasource/browserviewcontroller(_:documentviewcontrollerfor:))

### Managing Interactions with the Browser

- [var delegate: (any TVBrowserViewControllerDelegate)?](/documentation/tvmlkit/tvbrowserviewcontroller/delegate)
- [TVBrowserViewControllerDelegate](/documentation/tvmlkit/tvbrowserviewcontrollerdelegate)

#### Managing Focus

- [func browserViewController(TVBrowserViewController, didCenterOn: TVViewElement)](/documentation/tvmlkit/tvbrowserviewcontrollerdelegate/browserviewcontroller(_:didcenteron:))
- [func browserViewController(TVBrowserViewController, willCenterOn: TVViewElement)](/documentation/tvmlkit/tvbrowserviewcontrollerdelegate/browserviewcontroller(_:willcenteron:))

### Modifying the Browser Appearance

- [var cornerRadius: CGFloat](/documentation/tvmlkit/tvbrowserviewcontroller/cornerradius)
- [var interitemSpacing: CGFloat](/documentation/tvmlkit/tvbrowserviewcontroller/interitemspacing)
- [var maskInset: UIEdgeInsets](/documentation/tvmlkit/tvbrowserviewcontroller/maskinset)

### Accessing Browser Elements

- [var centeredViewElement: TVViewElement](/documentation/tvmlkit/tvbrowserviewcontroller/centeredviewelement)
- [var viewElement: TVViewElement](/documentation/tvmlkit/tvbrowserviewcontroller/viewelement)

### Managing Browser Transitions

- [TVBrowserTransitionAnimator](/documentation/tvmlkit/tvbrowsertransitionanimator)
- [TVDocumentViewController](/documentation/tvmlkit/tvdocumentviewcontroller)

### Initializing the Document View Controller

- [convenience init(context: [String : Any], for: TVApplicationController)](/documentation/tvmlkit/tvdocumentviewcontroller/init(context:for:))

### Managing Interactions with the Document

- [var delegate: (any TVDocumentViewControllerDelegate)?](/documentation/tvmlkit/tvdocumentviewcontroller/delegate)
- [TVDocumentViewControllerDelegate](/documentation/tvmlkit/tvdocumentviewcontrollerdelegate)

#### Managing Document Updates

- [func documentViewControllerWillUpdate(TVDocumentViewController)](/documentation/tvmlkit/tvdocumentviewcontrollerdelegate/documentviewcontrollerwillupdate(_:))
- [func documentViewControllerDidUpdate(TVDocumentViewController)](/documentation/tvmlkit/tvdocumentviewcontrollerdelegate/documentviewcontrollerdidupdate(_:))
- [func documentViewController(TVDocumentViewController, didUpdateWithContext: [String : Any])](/documentation/tvmlkit/tvdocumentviewcontrollerdelegate/documentviewcontroller(_:didupdatewithcontext:))

#### Responding to Errors

- [func documentViewController(TVDocumentViewController, didFailUpdateWithError: any Error)](/documentation/tvmlkit/tvdocumentviewcontrollerdelegate/documentviewcontroller(_:didfailupdatewitherror:))

#### Handling Events

- [func documentViewController(TVDocumentViewController, handleEvent: TVDocumentViewController.Event, with: TVViewElement) -> Bool](/documentation/tvmlkit/tvdocumentviewcontrollerdelegate/documentviewcontroller(_:handleevent:with:))

### Handling Document Events

- [TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event)

#### Initializers for Document View Controller Events

- [init(String)](/documentation/tvmlkit/tvdocumentviewcontroller/event/init(_:))
- [init(rawValue: String)](/documentation/tvmlkit/tvdocumentviewcontroller/event/init(rawvalue:))

#### Event Types

- [static let appear: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/appear)
- [static let disappear: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/disappear)
- [static let highlight: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/highlight)
- [static let holdSelect: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/holdselect)
- [static let load: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/load)
- [static let play: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/play)
- [static let select: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/select)
- [static let unload: TVDocumentViewController.Event](/documentation/tvmlkit/tvdocumentviewcontroller/event/unload)

### Updating the Document View Controller

- [func update(using: [String : Any])](/documentation/tvmlkit/tvdocumentviewcontroller/update(using:))

### Accessing the Document’s Components

- [var appController: TVApplicationController?](/documentation/tvmlkit/tvdocumentviewcontroller/appcontroller)
- [var documentContext: [String : Any]](/documentation/tvmlkit/tvdocumentviewcontroller/documentcontext)

## Custom Elements

- [TVElementFactory](/documentation/tvmlkit/tvelementfactory)

### Registering New Elements

- [class func registerViewElementClass(AnyClass, elementName: String)](/documentation/tvmlkit/tvelementfactory/registerviewelementclass(_:elementname:))
- [TVImageElement](/documentation/tvmlkit/tvimageelement)

### Identifying an Image

- [var url: URL?](/documentation/tvmlkit/tvimageelement/url)
- [var imageType: TVImageType](/documentation/tvmlkit/tvimageelement/imagetype)
- [TVImageType](/documentation/tvmlkit/tvimagetype)

#### Constants

- [case image](/documentation/tvmlkit/tvimagetype/image)
- [case fullscreen](/documentation/tvmlkit/tvimagetype/fullscreen)
- [case decoration](/documentation/tvmlkit/tvimagetype/decoration)
- [case hero](/documentation/tvmlkit/tvimagetype/hero)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvimagetype/init(rawvalue:))
- [var srcset: [String : URL]?](/documentation/tvmlkit/tvimageelement/srcset)
- [TVTextElement](/documentation/tvmlkit/tvtextelement)

### Creating Attributed Strings

- [func makeAttributedString(font: UIFont) -> NSAttributedString](/documentation/tvmlkit/tvtextelement/makeattributedstring(font:))
- [func makeAttributedString(font: UIFont, foregroundColor: UIColor?, textAlignment: NSTextAlignment) -> NSAttributedString](/documentation/tvmlkit/tvtextelement/makeattributedstring(font:foregroundcolor:textalignment:))

### Inspecting Text Elements

- [var attributedString: NSAttributedString?](/documentation/tvmlkit/tvtextelement/attributedstring)
- [var textStyle: TVTextElementStyle](/documentation/tvmlkit/tvtextelement/textstyle)
- [TVTextElementStyle](/documentation/tvmlkit/tvtextelementstyle)

#### Constants

- [case none](/documentation/tvmlkit/tvtextelementstyle/none)
- [case title](/documentation/tvmlkit/tvtextelementstyle/title)
- [case subtitle](/documentation/tvmlkit/tvtextelementstyle/subtitle)
- [case description](/documentation/tvmlkit/tvtextelementstyle/description)
- [case decoration](/documentation/tvmlkit/tvtextelementstyle/decoration)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvtextelementstyle/init(rawvalue:))
- [Creating TVML Elements](/documentation/tvmlkit/creating-tvml-elements)

## Custom Styles

- [TVViewElementStyle](/documentation/tvmlkit/tvviewelementstyle)

### Retrieving the Style for an Element

- [func value(propertyName: String) -> Any?](/documentation/tvmlkit/tvviewelementstyle/value(propertyname:))

### Defining the Height and Width of an Element

- [var height: CGFloat](/documentation/tvmlkit/tvviewelementstyle/height)
- [var maxHeight: CGFloat](/documentation/tvmlkit/tvviewelementstyle/maxheight)
- [var maxWidth: CGFloat](/documentation/tvmlkit/tvviewelementstyle/maxwidth)
- [var minHeight: CGFloat](/documentation/tvmlkit/tvviewelementstyle/minheight)
- [var minWidth: CGFloat](/documentation/tvmlkit/tvviewelementstyle/minwidth)
- [var width: CGFloat](/documentation/tvmlkit/tvviewelementstyle/width)

### Aligning and Positioning an Element

- [var alignment: TVElementAlignment](/documentation/tvmlkit/tvviewelementstyle/alignment)
- [TVElementAlignment](/documentation/tvmlkit/tvelementalignment)

#### Constants

- [case undefined](/documentation/tvmlkit/tvelementalignment/undefined)
- [case left](/documentation/tvmlkit/tvelementalignment/left)
- [case center](/documentation/tvmlkit/tvelementalignment/center)
- [case right](/documentation/tvmlkit/tvelementalignment/right)
- [case leading](/documentation/tvmlkit/tvelementalignment/leading)
- [case trailing](/documentation/tvmlkit/tvelementalignment/trailing)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvelementalignment/init(rawvalue:))
- [var contentAlignment: TVElementContentAlignment](/documentation/tvmlkit/tvviewelementstyle/contentalignment)
- [TVElementContentAlignment](/documentation/tvmlkit/tvelementcontentalignment)

#### Constants

- [TVElementContentAlignmentUndefinded](/documentation/tvmlkit/tvelementcontentalignmentundefinded)
- [case top](/documentation/tvmlkit/tvelementcontentalignment/top)
- [case center](/documentation/tvmlkit/tvelementcontentalignment/center)
- [case bottom](/documentation/tvmlkit/tvelementcontentalignment/bottom)

#### Enumeration Cases

- [case undefined](/documentation/tvmlkit/tvelementcontentalignment/undefined)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvelementcontentalignment/init(rawvalue:))
- [var focusMargin: UIEdgeInsets](/documentation/tvmlkit/tvviewelementstyle/focusmargin)
- [var interitemSpacing: CGFloat](/documentation/tvmlkit/tvviewelementstyle/interitemspacing)
- [var margin: UIEdgeInsets](/documentation/tvmlkit/tvviewelementstyle/margin)
- [var padding: UIEdgeInsets](/documentation/tvmlkit/tvviewelementstyle/padding)
- [var position: TVElementPosition](/documentation/tvmlkit/tvviewelementstyle/position)
- [TVElementPosition](/documentation/tvmlkit/tvelementposition)

#### Constants

- [case undefined](/documentation/tvmlkit/tvelementposition/undefined)
- [case center](/documentation/tvmlkit/tvelementposition/center)
- [case top](/documentation/tvmlkit/tvelementposition/top)
- [case bottom](/documentation/tvmlkit/tvelementposition/bottom)
- [case left](/documentation/tvmlkit/tvelementposition/left)
- [case right](/documentation/tvmlkit/tvelementposition/right)
- [case topLeft](/documentation/tvmlkit/tvelementposition/topleft)
- [case topRight](/documentation/tvmlkit/tvelementposition/topright)
- [case bottomLeft](/documentation/tvmlkit/tvelementposition/bottomleft)
- [case bottomRight](/documentation/tvmlkit/tvelementposition/bottomright)
- [case header](/documentation/tvmlkit/tvelementposition/header)
- [case footer](/documentation/tvmlkit/tvelementposition/footer)
- [case leading](/documentation/tvmlkit/tvelementposition/leading)
- [case trailing](/documentation/tvmlkit/tvelementposition/trailing)
- [case topLeading](/documentation/tvmlkit/tvelementposition/topleading)
- [case topTrailing](/documentation/tvmlkit/tvelementposition/toptrailing)
- [case bottomLeading](/documentation/tvmlkit/tvelementposition/bottomleading)
- [case bottomTrailing](/documentation/tvmlkit/tvelementposition/bottomtrailing)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvelementposition/init(rawvalue:))

### Changing the Text of an Element

- [var fontSize: CGFloat](/documentation/tvmlkit/tvviewelementstyle/fontsize)
- [var fontWeight: String?](/documentation/tvmlkit/tvviewelementstyle/fontweight)
- [var maxTextLines: Int](/documentation/tvmlkit/tvviewelementstyle/maxtextlines)
- [var textAlignment: NSTextAlignment](/documentation/tvmlkit/tvviewelementstyle/textalignment)
- [var textHighlightStyle: String?](/documentation/tvmlkit/tvviewelementstyle/texthighlightstyle)
- [var textMinimumScaleFactor: CGFloat](/documentation/tvmlkit/tvviewelementstyle/textminimumscalefactor)
- [var textStyle: String?](/documentation/tvmlkit/tvviewelementstyle/textstyle)

### Modifying an Image

- [var imageTreatmentName: String?](/documentation/tvmlkit/tvviewelementstyle/imagetreatmentname)
- [var ratingStyle: String?](/documentation/tvmlkit/tvviewelementstyle/ratingstyle)

### Coloring an Element

- [var backgroundColor: TVColor?](/documentation/tvmlkit/tvviewelementstyle/backgroundcolor)
- [var color: TVColor?](/documentation/tvmlkit/tvviewelementstyle/color)
- [var highlightColor: TVColor?](/documentation/tvmlkit/tvviewelementstyle/highlightcolor)
- [var tintColor: TVColor?](/documentation/tvmlkit/tvviewelementstyle/tintcolor)

### Element Styles

- [Transition Style Values](/documentation/tvmlkit/transition-style-values)

#### Constants

- [TVTransitionDissolve](/documentation/tvmlkit/tvtransitiondissolve)
- [TVTransitionMagicMove](/documentation/tvmlkit/tvtransitionmagicmove)
- [TVTransitionNone](/documentation/tvmlkit/tvtransitionnone)
- [TVTransitionPush](/documentation/tvmlkit/tvtransitionpush)
- [TVTransitionWipe](/documentation/tvmlkit/tvtransitionwipe)
- [Rating Style Values](/documentation/tvmlkit/rating-style-values)

#### Constants

- [TVRatingStyleStarSmall](/documentation/tvmlkit/tvratingstylestarsmall)
- [TVRatingStyleStarMedium](/documentation/tvmlkit/tvratingstylestarmedium)
- [TVRatingStyleStarLarge](/documentation/tvmlkit/tvratingstylestarlarge)
- [Label State Values](/documentation/tvmlkit/label-state-values)

#### Constants

- [TVTextHighlightStyleShowOnHighlight](/documentation/tvmlkit/tvtexthighlightstyleshowonhighlight)
- [TVTextHighlightStyleMarqueeOnHighlight](/documentation/tvmlkit/tvtexthighlightstylemarqueeonhighlight)
- [TVTextHighlightStyleMarqueeAndShowOnHighlight](/documentation/tvmlkit/tvtexthighlightstylemarqueeandshowonhighlight)
- [Text Style Values](/documentation/tvmlkit/text-style-values)

#### Constants

- [TVTextStyleTitle1](/documentation/tvmlkit/tvtextstyletitle1)
- [TVTextStyleTitle2](/documentation/tvmlkit/tvtextstyletitle2)
- [TVTextStyleTitle3](/documentation/tvmlkit/tvtextstyletitle3)
- [TVTextStyleHeadline](/documentation/tvmlkit/tvtextstyleheadline)
- [TVTextStyleSubtitle1](/documentation/tvmlkit/tvtextstylesubtitle1)
- [TVTextStyleSubtitle2](/documentation/tvmlkit/tvtextstylesubtitle2)
- [TVTextStyleSubtitle3](/documentation/tvmlkit/tvtextstylesubtitle3)
- [TVTextStyleCallout](/documentation/tvmlkit/tvtextstylecallout)
- [TVTextStyleBody](/documentation/tvmlkit/tvtextstylebody)
- [TVTextStyleSubhead](/documentation/tvmlkit/tvtextstylesubhead)
- [TVTextStyleFootnote](/documentation/tvmlkit/tvtextstylefootnote)
- [TVTextStyleCaption1](/documentation/tvmlkit/tvtextstylecaption1)
- [TVTextStyleCaption2](/documentation/tvmlkit/tvtextstylecaption2)
- [TVStyleFactory](/documentation/tvmlkit/tvstylefactory)

### Creating New Style Properties

- [class func registerStyleName(String, type: TVViewElementStyleType, inherited: Bool)](/documentation/tvmlkit/tvstylefactory/registerstylename(_:type:inherited:))
- [TVViewElementStyleType](/documentation/tvmlkit/tvviewelementstyletype)

#### Constants

- [case integer](/documentation/tvmlkit/tvviewelementstyletype/integer)
- [case double](/documentation/tvmlkit/tvviewelementstyletype/double)
- [case point](/documentation/tvmlkit/tvviewelementstyletype/point)
- [case string](/documentation/tvmlkit/tvviewelementstyletype/string)
- [case color](/documentation/tvmlkit/tvviewelementstyletype/color)
- [case URL](/documentation/tvmlkit/tvviewelementstyletype/url)
- [case edgeInsets](/documentation/tvmlkit/tvviewelementstyletype/edgeinsets)

#### Enumeration Cases

- [case transform](/documentation/tvmlkit/tvviewelementstyletype/transform)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvviewelementstyletype/init(rawvalue:))
- [TVColor](/documentation/tvmlkit/tvcolor)

### Getting Color Properties

- [var color: UIColor?](/documentation/tvmlkit/tvcolor/color)
- [var colorType: TVColorType](/documentation/tvmlkit/tvcolor/colortype)
- [TVColorType](/documentation/tvmlkit/tvcolortype)

#### Constants

- [case none](/documentation/tvmlkit/tvcolortype/none)
- [case plain](/documentation/tvmlkit/tvcolortype/plain)
- [case linearGradientTopToBottom](/documentation/tvmlkit/tvcolortype/lineargradienttoptobottom)
- [case linearGradientLeftToRight](/documentation/tvmlkit/tvcolortype/lineargradientlefttoright)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvcolortype/init(rawvalue:))
- [var gradientColors: [UIColor]?](/documentation/tvmlkit/tvcolor/gradientcolors)
- [var gradientPoints: [NSNumber]?](/documentation/tvmlkit/tvcolor/gradientpoints)

## Custom Player

- [TVMediaItem](/documentation/tvmlkit/tvmediaitem)

### Rating Media Content

- [var containsExplicitContent: Bool](/documentation/tvmlkit/tvmediaitem/containsexplicitcontent)
- [var contentRatingDomain: TVMediaItem.ContentRatingDomain?](/documentation/tvmlkit/tvmediaitem/contentratingdomain-swift.property)
- [TVMediaItem.ContentRatingDomain](/documentation/tvmlkit/tvmediaitem/contentratingdomain-swift.struct)

#### Rating Domains

- [static let movie: TVMediaItem.ContentRatingDomain](/documentation/tvmlkit/tvmediaitem/contentratingdomain-swift.struct/movie)
- [static let music: TVMediaItem.ContentRatingDomain](/documentation/tvmlkit/tvmediaitem/contentratingdomain-swift.struct/music)
- [static let tvShow: TVMediaItem.ContentRatingDomain](/documentation/tvmlkit/tvmediaitem/contentratingdomain-swift.struct/tvshow)

#### Initializers

- [init(String)](/documentation/tvmlkit/tvmediaitem/contentratingdomain-swift.struct/init(_:))
- [init(rawValue: String)](/documentation/tvmlkit/tvmediaitem/contentratingdomain-swift.struct/init(rawvalue:))
- [var contentRatingRanking: NSNumber?](/documentation/tvmlkit/tvmediaitem/contentratingranking)

### Identifying Media Items

- [var artworkImageURL: URL?](/documentation/tvmlkit/tvmediaitem/artworkimageurl)
- [var itemDescription: String?](/documentation/tvmlkit/tvmediaitem/itemdescription)
- [var subtitle: String?](/documentation/tvmlkit/tvmediaitem/subtitle)
- [var title: String?](/documentation/tvmlkit/tvmediaitem/title)
- [var type: TVMediaItem.MediaType?](/documentation/tvmlkit/tvmediaitem/type)
- [TVMediaItem.MediaType](/documentation/tvmlkit/tvmediaitem/mediatype)

#### Media Types

- [static let audio: TVMediaItem.MediaType](/documentation/tvmlkit/tvmediaitem/mediatype/audio)
- [static let video: TVMediaItem.MediaType](/documentation/tvmlkit/tvmediaitem/mediatype/video)

#### Initializers

- [init(String)](/documentation/tvmlkit/tvmediaitem/mediatype/init(_:))
- [init(rawValue: String)](/documentation/tvmlkit/tvmediaitem/mediatype/init(rawvalue:))
- [var url: URL?](/documentation/tvmlkit/tvmediaitem/url)
- [var userInfo: [String : Any]](/documentation/tvmlkit/tvmediaitem/userinfo)

### Setting Timing Options

- [var highlightGroups: [TVMediaItem.HighlightGroup]](/documentation/tvmlkit/tvmediaitem/highlightgroups)
- [TVMediaItem.HighlightGroup](/documentation/tvmlkit/tvmediaitem/highlightgroup)

#### Accessing the Highlights

- [var localizedName: String?](/documentation/tvmlkit/tvmediaitem/highlightgroup/localizedname)
- [var highlights: [TVMediaItem.Highlight]](/documentation/tvmlkit/tvmediaitem/highlightgroup/highlights)
- [TVMediaItem.Highlight](/documentation/tvmlkit/tvmediaitem/highlight)

##### Accessing a Highlight

- [var highlightDescription: String?](/documentation/tvmlkit/tvmediaitem/highlight/highlightdescription)
- [var imageURL: URL?](/documentation/tvmlkit/tvmediaitem/highlight/imageurl)
- [var localizedName: String?](/documentation/tvmlkit/tvmediaitem/highlight/localizedname)
- [var timeRange: TVMediaItem.TimeRange](/documentation/tvmlkit/tvmediaitem/highlight/timerange)
- [var interstitials: [TVMediaItem.TimeRange]](/documentation/tvmlkit/tvmediaitem/interstitials)
- [TVMediaItem.TimeRange](/documentation/tvmlkit/tvmediaitem/timerange)

#### Defining the Time Range

- [var startTime: TimeInterval](/documentation/tvmlkit/tvmediaitem/timerange/starttime)
- [var endTime: TimeInterval](/documentation/tvmlkit/tvmediaitem/timerange/endtime)
- [var duration: TimeInterval](/documentation/tvmlkit/tvmediaitem/timerange/duration)
- [var resumeTime: TimeInterval](/documentation/tvmlkit/tvmediaitem/resumetime)
- [TVPlaylist](/documentation/tvmlkit/tvplaylist)

### Retrieving Playlist Information

- [var mediaItems: [TVMediaItem]](/documentation/tvmlkit/tvplaylist/mediaitems)
- [var userInfo: [String : Any]?](/documentation/tvmlkit/tvplaylist/userinfo)
- [var repeatMode: TVPlaylist.RepeatMode](/documentation/tvmlkit/tvplaylist/repeatmode-swift.property)
- [TVPlaylist.RepeatMode](/documentation/tvmlkit/tvplaylist/repeatmode-swift.enum)

#### Replay Modes

- [case all](/documentation/tvmlkit/tvplaylist/repeatmode-swift.enum/all)
- [case one](/documentation/tvmlkit/tvplaylist/repeatmode-swift.enum/one)
- [case none](/documentation/tvmlkit/tvplaylist/repeatmode-swift.enum/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvplaylist/repeatmode-swift.enum/init(rawvalue:))
- [var endAction: TVPlaylist.EndAction](/documentation/tvmlkit/tvplaylist/endaction-swift.property)
- [TVPlaylist.EndAction](/documentation/tvmlkit/tvplaylist/endaction-swift.enum)

#### End Playback Reasons

- [case stop](/documentation/tvmlkit/tvplaylist/endaction-swift.enum/stop)
- [case pause](/documentation/tvmlkit/tvplaylist/endaction-swift.enum/pause)
- [case waitForMoreItems](/documentation/tvmlkit/tvplaylist/endaction-swift.enum/waitformoreitems)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvplaylist/endaction-swift.enum/init(rawvalue:))
- [TVPlayer](/documentation/tvmlkit/tvplayer)

### Setting Up the Player

- [init(player: AVPlayer)](/documentation/tvmlkit/tvplayer/init(player:))
- [var player: AVPlayer](/documentation/tvmlkit/tvplayer/player)
- [var playlist: TVPlaylist?](/documentation/tvmlkit/tvplayer/playlist)

### Controlling Playback

- [func next()](/documentation/tvmlkit/tvplayer/next())
- [func pause()](/documentation/tvmlkit/tvplayer/pause())
- [func previous()](/documentation/tvmlkit/tvplayer/previous())
- [var state: TVPlaybackState](/documentation/tvmlkit/tvplayer/state)
- [TVPlaybackState](/documentation/tvmlkit/tvplaybackstate)

#### Playback States

- [case undefined](/documentation/tvmlkit/tvplaybackstate/undefined)
- [case begin](/documentation/tvmlkit/tvplaybackstate/begin)
- [case loading](/documentation/tvmlkit/tvplaybackstate/loading)
- [case playing](/documentation/tvmlkit/tvplaybackstate/playing)
- [case paused](/documentation/tvmlkit/tvplaybackstate/paused)
- [case scanning](/documentation/tvmlkit/tvplaybackstate/scanning)
- [case fastForwarding](/documentation/tvmlkit/tvplaybackstate/fastforwarding)
- [case rewinding](/documentation/tvmlkit/tvplaybackstate/rewinding)
- [case end](/documentation/tvmlkit/tvplaybackstate/end)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvplaybackstate/init(rawvalue:))
- [func dispatch(event: TVPlaybackEvent, userInfo: (any TVPlaybackEventMarshaling)?, completion: ((Bool) -> Void)?)](/documentation/tvmlkit/tvplayer/dispatch(event:userinfo:completion:))
- [TVPlaybackEvent](/documentation/tvmlkit/tvplaybackevent)

#### Initializers

- [init(String)](/documentation/tvmlkit/tvplaybackevent/init(_:))
- [init(rawValue: String)](/documentation/tvmlkit/tvplaybackevent/init(rawvalue:))
- [TVPlaybackEventMarshaling](/documentation/tvmlkit/tvplaybackeventmarshaling)

#### Processing Playback Events

- [func processReturnValue(value: JSValue, in: JSContext)](/documentation/tvmlkit/tvplaybackeventmarshaling/processreturnvalue(value:in:))
- [var properties: [TVPlaybackEventProperty : Any]?](/documentation/tvmlkit/tvplaybackeventmarshaling/properties)
- [TVPlaybackEventProperty](/documentation/tvmlkit/tvplaybackeventproperty)

##### Initializers

- [init(String)](/documentation/tvmlkit/tvplaybackeventproperty/init(_:))
- [init(rawValue: String)](/documentation/tvmlkit/tvplaybackeventproperty/init(rawvalue:))
- [TVPlaybackCustomEventUserInfo](/documentation/tvmlkit/tvplaybackcustomeventuserinfo)

#### Creating User Info for Custom Playback Events

- [init(properties: [TVPlaybackEventProperty : Any]?, expectsReturnValue: Bool)](/documentation/tvmlkit/tvplaybackcustomeventuserinfo/init(properties:expectsreturnvalue:))
- [TVPlaybackEventProperty](/documentation/tvmlkit/tvplaybackeventproperty)

##### Initializers

- [init(String)](/documentation/tvmlkit/tvplaybackeventproperty/init(_:))
- [init(rawValue: String)](/documentation/tvmlkit/tvplaybackeventproperty/init(rawvalue:))
- [var expectsReturnValue: Bool](/documentation/tvmlkit/tvplaybackcustomeventuserinfo/expectsreturnvalue)
- [var returnValue: Any?](/documentation/tvmlkit/tvplaybackcustomeventuserinfo/returnvalue)

### Inspecting Media Items

- [func setCurrentMediaItem(toItemAtIndex: Int)](/documentation/tvmlkit/tvplayer/setcurrentmediaitem(toitematindex:))
- [var previousMediaItem: TVMediaItem?](/documentation/tvmlkit/tvplayer/previousmediaitem)
- [var currentMediaItem: TVMediaItem?](/documentation/tvmlkit/tvplayer/currentmediaitem)
- [var nextMediaItem: TVMediaItem?](/documentation/tvmlkit/tvplayer/nextmediaitem)

### Instance Methods

- [func present(animated: Bool)](/documentation/tvmlkit/tvplayer/present(animated:))

## Errors

- [let TVMLKitErrorDomain: String](/documentation/tvmlkit/tvmlkiterrordomain)
- [TVMLKitError](/documentation/tvmlkit/tvmlkiterror)

### Errors

- [case failedToLaunch](/documentation/tvmlkit/tvmlkiterror/failedtolaunch)
- [case internetUnavailable](/documentation/tvmlkit/tvmlkiterror/internetunavailable)
- [case last](/documentation/tvmlkit/tvmlkiterror/last)
- [case unknown](/documentation/tvmlkit/tvmlkiterror/unknown)

### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvmlkiterror/init(rawvalue:))
- [TVDocumentError](/documentation/tvmlkit/tvdocumenterror-swift.struct)

### Error Types

- [static var cancelled: TVDocumentError.Code](/documentation/tvmlkit/tvdocumenterror-swift.struct/cancelled)
- [static var failed: TVDocumentError.Code](/documentation/tvmlkit/tvdocumenterror-swift.struct/failed)
- [TVDocumentError.Code](/documentation/tvmlkit/tvdocumenterror-swift.struct/code)

#### Enumeration Cases

- [case cancelled](/documentation/tvmlkit/tvdocumenterror-swift.struct/code/cancelled)
- [case failed](/documentation/tvmlkit/tvdocumenterror-swift.struct/code/failed)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvdocumenterror-swift.struct/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/tvmlkit/tvdocumenterror-swift.struct/errordomain)

## Reference

- [TVMLKit Enumerations](/documentation/tvmlkit/tvmlkit-enumerations)

### Enumerations

- [TVDocumentError.Code](/documentation/tvmlkit/tvdocumenterror-swift.struct/code)

#### Enumeration Cases

- [case cancelled](/documentation/tvmlkit/tvdocumenterror-swift.struct/code/cancelled)
- [case failed](/documentation/tvmlkit/tvdocumenterror-swift.struct/code/failed)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvmlkit/tvdocumenterror-swift.struct/code/init(rawvalue:))
- [TVMLKit Constants](/documentation/tvmlkit/tvmlkit-constants)

### Constants

- [let TVDocumentErrorDomain: String](/documentation/tvmlkit/tvdocumenterrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
