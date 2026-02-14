# Developer Tools Support Documentation

Source: https://sosumi.ai/documentation/developertoolssupport

---
title: DeveloperToolsSupport
source: https://developer.apple.com/documentation/developertoolssupport
timestamp: 2026-02-13T18:56:08.754Z
---

## Library Customization

- [LibraryContentProvider](/documentation/developertoolssupport/librarycontentprovider)

### Adding Views

- [var views: [LibraryItem]](/documentation/developertoolssupport/librarycontentprovider/views)

### Adding Modifiers

- [func modifiers(base: Self.ModifierBase) -> [LibraryItem]](/documentation/developertoolssupport/librarycontentprovider/modifiers(base:))
- [ModifierBase](/documentation/developertoolssupport/librarycontentprovider/modifierbase)

### Building Arrays

- [LibraryContentBuilder](/documentation/developertoolssupport/librarycontentbuilder)

#### Type Methods

- [static func buildBlock([LibraryItem]...) -> [LibraryItem]](/documentation/developertoolssupport/librarycontentbuilder/buildblock(_:))
- [static func buildExpression(LibraryItem) -> [LibraryItem]](/documentation/developertoolssupport/librarycontentbuilder/buildexpression(_:)-8x2oz)
- [static func buildExpression([LibraryItem]) -> [LibraryItem]](/documentation/developertoolssupport/librarycontentbuilder/buildexpression(_:)-90ip4)
- [LibraryItem](/documentation/developertoolssupport/libraryitem)

### Creating a Library Item

- [init<SnippetExpressionType>(@autoclosure () -> SnippetExpressionType, visible: Bool, title: String?, category: LibraryItem.Category, matchingSignature: String?)](/documentation/developertoolssupport/libraryitem/init(_:visible:title:category:matchingsignature:))
- [LibraryItem.Category](/documentation/developertoolssupport/libraryitem/category)

#### Specifying a Category

- [static let control: LibraryItem.Category](/documentation/developertoolssupport/libraryitem/category/control)
- [static let effect: LibraryItem.Category](/documentation/developertoolssupport/libraryitem/category/effect)
- [static let layout: LibraryItem.Category](/documentation/developertoolssupport/libraryitem/category/layout)
- [static let other: LibraryItem.Category](/documentation/developertoolssupport/libraryitem/category/other)

## Preview Registration

- [PreviewRegistry](/documentation/developertoolssupport/previewregistry)

### Type Properties

- [static var column: Int](/documentation/developertoolssupport/previewregistry/column)
- [static var fileID: String](/documentation/developertoolssupport/previewregistry/fileid)
- [static var line: Int](/documentation/developertoolssupport/previewregistry/line)
- [static var preview: Preview](/documentation/developertoolssupport/previewregistry/preview)

### Type Methods

- [static func makePreview() throws -> Preview](/documentation/developertoolssupport/previewregistry/makepreview())
- [Preview](/documentation/developertoolssupport/preview)

### Initializers

- [init<Attributes>(String?, as: ActivityPreviewViewKind, using: Attributes, widget: () -> some Widget, contentStates: () async -> [Attributes.ContentState])](/documentation/developertoolssupport/preview/init(_:as:using:widget:contentstates:))
- [init<Provider>(String?, as: WidgetFamily, using: Provider.Intent, widget: () -> some Widget, timelineProvider: () -> Provider)](/documentation/developertoolssupport/preview/init(_:as:using:widget:timelineprovider:)-1if5u)
- [init<Provider>(String?, as: WidgetFamily, using: Provider.Intent, widget: () -> some Widget, timelineProvider: () -> Provider)](/documentation/developertoolssupport/preview/init(_:as:using:widget:timelineprovider:)-5335n)
- [init(String?, as: WidgetFamily, widget: () -> some Widget, timeline: () async -> [any TimelineEntry])](/documentation/developertoolssupport/preview/init(_:as:widget:timeline:))
- [init(String?, as: WidgetFamily, widget: () -> some Widget, timelineProvider: () -> some TimelineProvider)](/documentation/developertoolssupport/preview/init(_:as:widget:timelineprovider:))
- [init(String?, immersionStyle: some ImmersionStyle, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/developertoolssupport/preview/init(_:immersionstyle:traits:body:cameras:))
- [init(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> NSView)](/documentation/developertoolssupport/preview/init(_:traits:body:)-158mk)
- [init(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> NSViewController)](/documentation/developertoolssupport/preview/init(_:traits:body:)-2viaf)
- [init(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> UIView)](/documentation/developertoolssupport/preview/init(_:traits:body:)-3i54d)
- [init(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View)](/documentation/developertoolssupport/preview/init(_:traits:body:)-8pemr)
- [init(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> UIViewController)](/documentation/developertoolssupport/preview/init(_:traits:body:)-941vb)
- [init(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/developertoolssupport/preview/init(_:traits:body:cameras:))
- [init<Entry>(String?, widget: () -> some Widget, relevanceEntries: () async -> [Entry])](/documentation/developertoolssupport/preview/init(_:widget:relevanceentries:))
- [init<Provider>(String?, widget: () -> some Widget, relevanceProvider: () -> Provider)](/documentation/developertoolssupport/preview/init(_:widget:relevanceprovider:))
- [init<Provider>(String?, widget: () -> some Widget, relevanceProvider: () -> Provider, relevance: () async -> WidgetRelevance<Provider.Configuration>)](/documentation/developertoolssupport/preview/init(_:widget:relevanceprovider:relevance:))
- [init(String?, windowStyle: some WindowStyle, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/developertoolssupport/preview/init(_:windowstyle:traits:body:cameras:))

### Enumerations

- [Preview.ViewTraits](/documentation/developertoolssupport/preview/viewtraits)
- [PreviewLayout](/documentation/developertoolssupport/previewlayout)

### Enumeration Cases

- [case device](/documentation/developertoolssupport/previewlayout/device)
- [case fixed(width: CGFloat, height: CGFloat)](/documentation/developertoolssupport/previewlayout/fixed(width:height:))
- [case fixed3D(width: CGFloat, height: CGFloat, depth: CGFloat)](/documentation/developertoolssupport/previewlayout/fixed3d(width:height:depth:))
- [case sizeThatFits](/documentation/developertoolssupport/previewlayout/sizethatfits)
- [PreviewTrait](/documentation/developertoolssupport/previewtrait)

### Initializers

- [init(PreviewTrait<T>...)](/documentation/developertoolssupport/previewtrait/init(_:))

### Type Properties

- [static var assistiveAccess: PreviewTrait<Preview.ViewTraits>](/documentation/developertoolssupport/previewtrait/assistiveaccess)
- [static var defaultLayout: PreviewTrait<Preview.ViewTraits>](/documentation/developertoolssupport/previewtrait/defaultlayout)
- [static var landscapeLeft: PreviewTrait<Preview.ViewTraits>](/documentation/developertoolssupport/previewtrait/landscapeleft)
- [static var landscapeRight: PreviewTrait<Preview.ViewTraits>](/documentation/developertoolssupport/previewtrait/landscaperight)
- [static var portrait: PreviewTrait<Preview.ViewTraits>](/documentation/developertoolssupport/previewtrait/portrait)
- [static var portraitUpsideDown: PreviewTrait<Preview.ViewTraits>](/documentation/developertoolssupport/previewtrait/portraitupsidedown)
- [static var sizeThatFitsLayout: PreviewTrait<Preview.ViewTraits>](/documentation/developertoolssupport/previewtrait/sizethatfitslayout)

### Type Methods

- [static func fixedLayout(width: CGFloat, height: CGFloat) -> PreviewTrait<T>](/documentation/developertoolssupport/previewtrait/fixedlayout(width:height:))
- [static func fixedLayout(width: CGFloat, height: CGFloat, depth: CGFloat) -> PreviewTrait<T>](/documentation/developertoolssupport/previewtrait/fixedlayout(width:height:depth:))
- [static func modifier(some PreviewModifier) -> PreviewTrait<T>](/documentation/developertoolssupport/previewtrait/modifier(_:))

## Resource Definition

- [ColorResource](/documentation/developertoolssupport/colorresource)

### Initializers

- [init(name: String, bundle: Bundle)](/documentation/developertoolssupport/colorresource/init(name:bundle:))
- [ImageResource](/documentation/developertoolssupport/imageresource)

### Initializers

- [init(name: String, bundle: Bundle)](/documentation/developertoolssupport/imageresource/init(name:bundle:))

## Camera Management

- [PreviewCamera](/documentation/developertoolssupport/previewcamera)

### Initializers

- [init(from: UnitPoint3D, zoom: Double, name: String?)](/documentation/developertoolssupport/previewcamera/init(from:zoom:name:))
- [init(lookingAt: Point3D, from: Point3D, name: String?)](/documentation/developertoolssupport/previewcamera/init(lookingat:from:name:))
- [PreviewCameraBuilder](/documentation/developertoolssupport/previewcamerabuilder)

### Type Methods

- [static func buildArray([[PreviewCamera]]) -> [PreviewCamera]](/documentation/developertoolssupport/previewcamerabuilder/buildarray(_:))
- [static func buildExpression(PreviewCamera) -> [PreviewCamera]](/documentation/developertoolssupport/previewcamerabuilder/buildexpression(_:)-5okdh)
- [static func buildExpression([PreviewCamera]) -> [PreviewCamera]](/documentation/developertoolssupport/previewcamerabuilder/buildexpression(_:)-5t9d2)
- [static func buildPartialBlock(accumulated: [PreviewCamera], next: [PreviewCamera]) -> [PreviewCamera]](/documentation/developertoolssupport/previewcamerabuilder/buildpartialblock(accumulated:next:))
- [static func buildPartialBlock(first: [PreviewCamera]) -> [PreviewCamera]](/documentation/developertoolssupport/previewcamerabuilder/buildpartialblock(first:))

## Structures

- [PreviewBodyBuilder](/documentation/developertoolssupport/previewbodybuilder)

### Type Methods

- [static func buildBlock(Content) -> Content](/documentation/developertoolssupport/previewbodybuilder/buildblock(_:))
- [PreviewMacroBodyBuilder](/documentation/developertoolssupport/previewmacrobodybuilder)

### Type Methods

- [static func buildBlock(Content) -> Content](/documentation/developertoolssupport/previewmacrobodybuilder/buildblock(_:))
- [PreviewUnavailable](/documentation/developertoolssupport/previewunavailable)

### Initializers

- [init()](/documentation/developertoolssupport/previewunavailable/init())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
