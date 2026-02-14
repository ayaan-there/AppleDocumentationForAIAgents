# Image Playground Documentation

Source: https://sosumi.ai/documentation/imageplayground

---
title: Image Playground
source: https://developer.apple.com/documentation/imageplayground
timestamp: 2026-02-13T18:58:06.652Z
---

## SwiftUI presentation

- [func imagePlaygroundSheet(isPresented: Binding<Bool>, concept: String, sourceImage: Image?, onCompletion: (URL) -> Void, onCancellation: (() -> Void)?) -> some View](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concept:sourceimage:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented: Binding<Bool>, concepts: [ImagePlaygroundConcept], sourceImage: Image?, onCompletion: (URL) -> Void, onCancellation: (() -> Void)?) -> some View](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concepts:sourceimage:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented: Binding<Bool>, concepts: [ImagePlaygroundConcept], sourceImageURL: URL, onCompletion: (URL) -> Void, onCancellation: (() -> Void)?) -> some View](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concepts:sourceimageurl:oncompletion:oncancellation:))

## UIKit and AppKit presentation

- [ImagePlaygroundViewController](/documentation/imageplayground/imageplaygroundviewcontroller)

### Creating the view controller

- [convenience init()](/documentation/imageplayground/imageplaygroundviewcontroller/init())

### Processing a generated image

- [var delegate: (any ImagePlaygroundViewController.Delegate)?](/documentation/imageplayground/imageplaygroundviewcontroller/delegate-swift.property)
- [ImagePlaygroundViewController.Delegate](/documentation/imageplayground/imageplaygroundviewcontroller/delegate-swift.protocol)

#### Receiving the image

- [func imagePlaygroundViewController(ImagePlaygroundViewController, didCreateImageAt: URL)](/documentation/imageplayground/imageplaygroundviewcontroller/delegate-swift.protocol/imageplaygroundviewcontroller(_:didcreateimageat:))

#### Handling cancellation events

- [func imagePlaygroundViewControllerDidCancel(ImagePlaygroundViewController)](/documentation/imageplayground/imageplaygroundviewcontroller/delegate-swift.protocol/imageplaygroundviewcontrollerdidcancel(_:))

### Specifying the configuration of the playground

- [var selectedGenerationStyle: ImagePlaygroundStyle](/documentation/imageplayground/imageplaygroundviewcontroller/selectedgenerationstyle)
- [var allowedGenerationStyles: [ImagePlaygroundStyle]](/documentation/imageplayground/imageplaygroundviewcontroller/allowedgenerationstyles)
- [var personalizationPolicy: ImagePlaygroundPersonalizationPolicy](/documentation/imageplayground/imageplaygroundviewcontroller/personalizationpolicy)
- [ImagePlaygroundPersonalizationPolicy](/documentation/imageplayground/imageplaygroundpersonalizationpolicy)

#### Getting the policy

- [case automatic](/documentation/imageplayground/imageplaygroundpersonalizationpolicy/automatic)
- [case enabled](/documentation/imageplayground/imageplaygroundpersonalizationpolicy/enabled)
- [case disabled](/documentation/imageplayground/imageplaygroundpersonalizationpolicy/disabled)

### Specifying the source content

- [var concepts: [ImagePlaygroundConcept]](/documentation/imageplayground/imageplaygroundviewcontroller/concepts)
- [var sourceImage: UIImage?](/documentation/imageplayground/imageplaygroundviewcontroller/sourceimage)

### Getting the feature availability

- [class var isAvailable: Bool](/documentation/imageplayground/imageplaygroundviewcontroller/isavailable)

### Managing the view

- [func viewDidLoad()](/documentation/imageplayground/imageplaygroundviewcontroller/viewdidload())
- [func viewDidDisappear()](/documentation/imageplayground/imageplaygroundviewcontroller/viewdiddisappear())
- [func viewWillAppear()](/documentation/imageplayground/imageplaygroundviewcontroller/viewwillappear())

### Instance Properties

- [var isModalInPresentation: Bool](/documentation/imageplayground/imageplaygroundviewcontroller/ismodalinpresentation)
- [var modalPresentationStyle: UIModalPresentationStyle](/documentation/imageplayground/imageplaygroundviewcontroller/modalpresentationstyle)
- [var preferredContentSize: CGSize](/documentation/imageplayground/imageplaygroundviewcontroller/preferredcontentsize)
- [var supportedInterfaceOrientations: UIInterfaceOrientationMask](/documentation/imageplayground/imageplaygroundviewcontroller/supportedinterfaceorientations)

### Instance Methods

- [func viewDidDisappear(Bool)](/documentation/imageplayground/imageplaygroundviewcontroller/viewdiddisappear(_:))

## Programmatic creation

- [ImageCreator](/documentation/imageplayground/imagecreator)

### Creating the object

- [init() async throws](/documentation/imageplayground/imagecreator/init())

### Generating images

- [func images(for: [ImagePlaygroundConcept], style: ImagePlaygroundStyle, limit: Int) -> some AsyncSequence<ImageCreator.CreatedImage, any Error>
](/documentation/imageplayground/imagecreator/images(for:style:limit:))
- [let availableStyles: [ImagePlaygroundStyle]](/documentation/imageplayground/imagecreator/availablestyles)
- [ImageCreator.CreatedImage](/documentation/imageplayground/imagecreator/createdimage)

#### Getting the image

- [let cgImage: CGImage](/documentation/imageplayground/imagecreator/createdimage/cgimage)
- [ImageCreator.Error](/documentation/imageplayground/imagecreator/error)

#### Getting the error codes

- [case notSupported](/documentation/imageplayground/imagecreator/error/notsupported)
- [case unavailable](/documentation/imageplayground/imagecreator/error/unavailable)
- [case creationCancelled](/documentation/imageplayground/imagecreator/error/creationcancelled)
- [case faceInImageTooSmall](/documentation/imageplayground/imagecreator/error/faceinimagetoosmall)
- [case unsupportedLanguage](/documentation/imageplayground/imagecreator/error/unsupportedlanguage)
- [case unsupportedInputImage](/documentation/imageplayground/imagecreator/error/unsupportedinputimage)
- [case backgroundCreationForbidden](/documentation/imageplayground/imagecreator/error/backgroundcreationforbidden)
- [case creationFailed](/documentation/imageplayground/imagecreator/error/creationfailed)

#### Enumeration Cases

- [case conceptsRequirePersonIdentity](/documentation/imageplayground/imagecreator/error/conceptsrequirepersonidentity)

## Platform support

- [ImagePlaygroundConcept](/documentation/imageplayground/imageplaygroundconcept)

### Describing the image

- [static func text(String) -> ImagePlaygroundConcept](/documentation/imageplayground/imageplaygroundconcept/text(_:))
- [static func extracted(from: String, title: String?) -> ImagePlaygroundConcept](/documentation/imageplayground/imageplaygroundconcept/extracted(from:title:))
- [static func drawing(PKDrawing) -> ImagePlaygroundConcept](/documentation/imageplayground/imageplaygroundconcept/drawing(_:))
- [static func image(CGImage) -> ImagePlaygroundConcept](/documentation/imageplayground/imageplaygroundconcept/image(_:)-29ora)
- [static func image(URL) -> ImagePlaygroundConcept?](/documentation/imageplayground/imageplaygroundconcept/image(_:)-2s44c)
- [ImagePlaygroundStyle](/documentation/imageplayground/imageplaygroundstyle)

### Getting the style options

- [static let animation: ImagePlaygroundStyle](/documentation/imageplayground/imageplaygroundstyle/animation)
- [static let illustration: ImagePlaygroundStyle](/documentation/imageplayground/imageplaygroundstyle/illustration)
- [static let sketch: ImagePlaygroundStyle](/documentation/imageplayground/imageplaygroundstyle/sketch)
- [static var all: [ImagePlaygroundStyle]](/documentation/imageplayground/imageplaygroundstyle/all)

### Getting the style identifier

- [let id: String](/documentation/imageplayground/imageplaygroundstyle/id)

### Type Properties

- [static let externalProvider: ImagePlaygroundStyle](/documentation/imageplayground/imageplaygroundstyle/externalprovider)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
