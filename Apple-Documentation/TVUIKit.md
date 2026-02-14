# TVUIKit Documentation

Source: https://sosumi.ai/documentation/tvuikit

---
title: TVUIKit
source: https://developer.apple.com/documentation/tvuikit
timestamp: 2026-02-13T19:03:23.412Z
---

## Collections of content

- [Creating immersive experiences using a full-screen layout](/documentation/tvuikit/creating-immersive-experiences-using-a-full-screen-layout)
- [TVCollectionViewFullScreenLayout](/documentation/tvuikit/tvcollectionviewfullscreenlayout)

### Managing a collection view’s appearance

- [var interitemSpacing: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayout/interitemspacing)

### Accessing collection view items

- [var centerIndexPath: IndexPath?](/documentation/tvuikit/tvcollectionviewfullscreenlayout/centerindexpath)

### Configuring cell masks

- [var maskAmount: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayout/maskamount)
- [var maskInset: UIEdgeInsets](/documentation/tvuikit/tvcollectionviewfullscreenlayout/maskinset)

### Managing cell appearance

- [var cornerRadius: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayout/cornerradius)

### Managing transitions

- [var parallaxFactor: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayout/parallaxfactor)
- [var isTransitioningToCenterIndexPath: Bool](/documentation/tvuikit/tvcollectionviewfullscreenlayout/istransitioningtocenterindexpath)
- [TVCollectionViewDelegateFullScreenLayout](/documentation/tvuikit/tvcollectionviewdelegatefullscreenlayout)

### Managing Cell Transitions

- [func collectionView(UICollectionView, layout: UICollectionViewLayout, willCenterCellAt: IndexPath)](/documentation/tvuikit/tvcollectionviewdelegatefullscreenlayout/collectionview(_:layout:willcentercellat:))
- [func collectionView(UICollectionView, layout: UICollectionViewLayout, didCenterCellAt: IndexPath)](/documentation/tvuikit/tvcollectionviewdelegatefullscreenlayout/collectionview(_:layout:didcentercellat:))
- [TVCollectionViewFullScreenCell](/documentation/tvuikit/tvcollectionviewfullscreencell)

### Modifying Cell Appearance

- [var contentBleed: UIEdgeInsets](/documentation/tvuikit/tvcollectionviewfullscreencell/contentbleed)
- [var cornerRadius: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreencell/cornerradius)
- [var maskAmount: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreencell/maskamount)

### Accessing Cell Views

- [var maskedContentView: UIView](/documentation/tvuikit/tvcollectionviewfullscreencell/maskedcontentview)
- [var maskedBackgroundView: UIView](/documentation/tvuikit/tvcollectionviewfullscreencell/maskedbackgroundview)

### Accessing Cell Position

- [var normalizedPosition: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreencell/normalizedposition)

### Managing Cell Position

- [func normalizedPositionDidChange()](/documentation/tvuikit/tvcollectionviewfullscreencell/normalizedpositiondidchange())
- [func normalizedPositionWillChange(CGFloat)](/documentation/tvuikit/tvcollectionviewfullscreencell/normalizedpositionwillchange(_:))

### Managing Cell Mask

- [func maskAmountDidChange()](/documentation/tvuikit/tvcollectionviewfullscreencell/maskamountdidchange())
- [func maskAmountWillChange(CGFloat)](/documentation/tvuikit/tvcollectionviewfullscreencell/maskamountwillchange(_:))

### Managing the Parallax Effect

- [var parallaxOffset: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreencell/parallaxoffset)
- [TVCollectionViewFullScreenLayoutAttributes](/documentation/tvuikit/tvcollectionviewfullscreenlayoutattributes)

### Modifying Cell Appearance

- [var contentBleed: UIEdgeInsets](/documentation/tvuikit/tvcollectionviewfullscreenlayoutattributes/contentbleed)
- [var cornerRadius: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayoutattributes/cornerradius)
- [var maskAmount: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayoutattributes/maskamount)

### Modifying the Parallax Effect

- [var parallaxOffset: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayoutattributes/parallaxoffset)

### Managing Cell Position

- [var normalizedPosition: CGFloat](/documentation/tvuikit/tvcollectionviewfullscreenlayoutattributes/normalizedposition)

## Content views

- [TVMediaItemContentView](/documentation/tvuikit/tvmediaitemcontentview)

### Creating a Media Item Content View

- [convenience init(configuration: TVMediaItemContentConfiguration)](/documentation/tvuikit/tvmediaitemcontentview/init(configuration:))
- [TVMediaItemContentConfiguration](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct)

#### Creating Default Configurations

- [static func wideCell() -> TVMediaItemContentConfiguration](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/widecell())

#### Customizing Content

- [var image: UIImage?](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/image)
- [var text: String?](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/text)
- [var secondaryText: String?](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/secondarytext)
- [var badgeText: String?](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgetext)
- [var badgeProperties: TVMediaItemContentConfiguration.BadgeProperties](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.property)
- [TVMediaItemContentConfiguration.BadgeProperties](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.struct)

##### Creating a Default Configuration

- [static func `default`() -> TVMediaItemContentConfiguration.BadgeProperties](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.struct/default())
- [static func liveContent() -> TVMediaItemContentConfiguration.BadgeProperties](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.struct/livecontent())

##### Customizing Content

- [var font: UIFont](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.struct/font)
- [var color: UIColor](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.struct/color)
- [var backgroundColor: UIColor](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.struct/backgroundcolor)
- [var transform: TVMediaItemContentConfiguration.TextProperties.TextTransform](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/badgeproperties-swift.struct/transform)
- [TVMediaItemContentConfiguration.TextProperties.TextTransform](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform)

###### Text Transforms

- [case none](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/none)
- [case capitalized](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/capitalized)
- [case lowercase](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/lowercase)
- [case uppercase](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/uppercase)
- [var overlayView: UIView?](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/overlayview)
- [var playbackProgress: Float](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/playbackprogress)

#### Customizing Appearance

- [TVMediaItemContentConfiguration.TextProperties](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct)

##### Configuring Text Properties

- [var font: UIFont](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/font)
- [var color: UIColor](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/color)
- [var transform: TVMediaItemContentConfiguration.TextProperties.TextTransform](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/transform)
- [TVMediaItemContentConfiguration.TextProperties.TextTransform](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform)

###### Text Transforms

- [case none](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/none)
- [case capitalized](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/capitalized)
- [case lowercase](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/lowercase)
- [case uppercase](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/uppercase)
- [var textProperties: TVMediaItemContentConfiguration.TextProperties](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/textproperties-swift.property)
- [var secondaryTextProperties: TVMediaItemContentConfiguration.TextProperties](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/secondarytextproperties)

#### Creating a Content View

- [func makeContentView() -> any UIView & UIContentView](/documentation/tvuikit/tvmediaitemcontentconfiguration-swift.struct/makecontentview())

### Managing the Content Layout

- [var focusedFrameGuide: UILayoutGuide](/documentation/tvuikit/tvmediaitemcontentview/focusedframeguide)
- [TVMonogramContentView](/documentation/tvuikit/tvmonogramcontentview)

### Creating a Monogram Content View

- [convenience init(configuration: TVMonogramContentConfiguration)](/documentation/tvuikit/tvmonogramcontentview/init(configuration:))
- [TVMonogramContentConfiguration](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct)

#### Creating Default Configurations

- [static func cell() -> TVMonogramContentConfiguration](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/cell())

#### Customizing Content

- [var image: UIImage?](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/image)
- [var text: String?](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/text)
- [var secondaryText: String?](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/secondarytext)
- [var personNameComponents: PersonNameComponents?](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/personnamecomponents)

#### Customizing Appearance

- [var textProperties: TVMonogramContentConfiguration.TextProperties](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.property)
- [var secondaryTextProperties: TVMonogramContentConfiguration.TextProperties](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/secondarytextproperties)
- [TVMonogramContentConfiguration.TextProperties](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct)

##### Configuring Text Properties

- [var font: UIFont](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct/font)
- [var color: UIColor](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct/color)
- [TVMonogramContentConfiguration.TextProperties.TextTransform](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform)

###### Text Transforms

- [case none](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/none)
- [case capitalized](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/capitalized)
- [case lowercase](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/lowercase)
- [case uppercase](/documentation/tvuikit/tvmonogramcontentconfiguration-swift.struct/textproperties-swift.struct/texttransform/uppercase)

### Managing the Content Layout

- [var focusedFrameGuide: UILayoutGuide](/documentation/tvuikit/tvmonogramcontentview/focusedframeguide)

## Numeric input

- [TVDigitEntryViewController](/documentation/tvuikit/tvdigitentryviewcontroller)

### Configuring the Digit Entry View

- [var numberOfDigits: Int](/documentation/tvuikit/tvdigitentryviewcontroller/numberofdigits)
- [var titleText: String?](/documentation/tvuikit/tvdigitentryviewcontroller/titletext)
- [var promptText: String?](/documentation/tvuikit/tvdigitentryviewcontroller/prompttext)
- [var isSecureDigitEntry: Bool](/documentation/tvuikit/tvdigitentryviewcontroller/issecuredigitentry)

### Entering Information

- [var entryCompletionHandler: (String) -> Void](/documentation/tvuikit/tvdigitentryviewcontroller/entrycompletionhandler)
- [func clearEntry(animated: Bool)](/documentation/tvuikit/tvdigitentryviewcontroller/clearentry(animated:))

## Lockup views

- [TVLockupView](/documentation/tvuikit/tvlockupview)

### Setting view size

- [var contentSize: CGSize](/documentation/tvuikit/tvlockupview/contentsize)
- [var contentViewInsets: NSDirectionalEdgeInsets](/documentation/tvuikit/tvlockupview/contentviewinsets)
- [var focusSizeIncrease: NSDirectionalEdgeInsets](/documentation/tvuikit/tvlockupview/focussizeincrease)

### Adding subviews

- [var contentView: UIView](/documentation/tvuikit/tvlockupview/contentview)
- [var headerView: TVLockupHeaderFooterView?](/documentation/tvuikit/tvlockupview/headerview)
- [var footerView: TVLockupHeaderFooterView?](/documentation/tvuikit/tvlockupview/footerview)
- [TVLockupViewComponent](/documentation/tvuikit/tvlockupviewcomponent)

### Updating the Lockup View Appearance

- [func updateAppearance(forLockupViewState: UIControl.State)](/documentation/tvuikit/tvlockupviewcomponent/updateappearance(forlockupviewstate:))
- [TVLockupHeaderFooterView](/documentation/tvuikit/tvlockupheaderfooterview)

### Adding Titles

- [var titleLabel: UILabel?](/documentation/tvuikit/tvlockupheaderfooterview/titlelabel)
- [var subtitleLabel: UILabel?](/documentation/tvuikit/tvlockupheaderfooterview/subtitlelabel)

### Configuring Focus Behavior

- [var showsOnlyWhenAncestorFocused: Bool](/documentation/tvuikit/tvlockupheaderfooterview/showsonlywhenancestorfocused)
- [TVCardView](/documentation/tvuikit/tvcardview)

### Setting the Background Color

- [var cardBackgroundColor: UIColor?](/documentation/tvuikit/tvcardview/cardbackgroundcolor)
- [TVPosterView](/documentation/tvuikit/tvposterview)

### Creating a Poster View

- [init(image: UIImage?)](/documentation/tvuikit/tvposterview/init(image:))

### Configuring a Poster View

- [var image: UIImage?](/documentation/tvuikit/tvposterview/image)
- [var imageView: UIImageView](/documentation/tvuikit/tvposterview/imageview)
- [var title: String?](/documentation/tvuikit/tvposterview/title)
- [var subtitle: String?](/documentation/tvuikit/tvposterview/subtitle)
- [TVCaptionButtonView](/documentation/tvuikit/tvcaptionbuttonview)

### Setting the Motion Direction

- [var motionDirection: TVCaptionButtonViewMotionDirection](/documentation/tvuikit/tvcaptionbuttonview/motiondirection)
- [TVCaptionButtonViewMotionDirection](/documentation/tvuikit/tvcaptionbuttonviewmotiondirection)

#### Tilt Directions

- [case all](/documentation/tvuikit/tvcaptionbuttonviewmotiondirection/all)
- [case horizontal](/documentation/tvuikit/tvcaptionbuttonviewmotiondirection/horizontal)
- [case none](/documentation/tvuikit/tvcaptionbuttonviewmotiondirection/none)
- [case vertical](/documentation/tvuikit/tvcaptionbuttonviewmotiondirection/vertical)

#### Initializers

- [init?(rawValue: Int)](/documentation/tvuikit/tvcaptionbuttonviewmotiondirection/init(rawvalue:))

### Configuring the Caption Button

- [var contentImage: UIImage?](/documentation/tvuikit/tvcaptionbuttonview/contentimage)
- [var contentText: String?](/documentation/tvuikit/tvcaptionbuttonview/contenttext)
- [var title: String?](/documentation/tvuikit/tvcaptionbuttonview/title)
- [var subtitle: String?](/documentation/tvuikit/tvcaptionbuttonview/subtitle)
- [TVMonogramView](/documentation/tvuikit/tvmonogramview)

### Configuring a Monogram

- [var personNameComponents: PersonNameComponents?](/documentation/tvuikit/tvmonogramview/personnamecomponents)
- [var image: UIImage?](/documentation/tvuikit/tvmonogramview/image)
- [var title: String?](/documentation/tvuikit/tvmonogramview/title)
- [var subtitle: String?](/documentation/tvuikit/tvmonogramview/subtitle)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
