# TranslationUIProvider Documentation

Source: https://sosumi.ai/documentation/translationuiprovider

---
title: TranslationUIProvider
source: https://developer.apple.com/documentation/translationuiprovider
timestamp: 2026-02-13T19:03:15.423Z
---

## Essentials

- [Preparing your app to be the default translation app](/documentation/translationuiprovider/preparing-your-app-to-be-the-default-translation-app)

## Creating translation app extensions

- [TranslationUIProviderContext](/documentation/translationuiprovider/translationuiprovidercontext)

### Instance Properties

- [var allowsReplacement: Bool](/documentation/translationuiprovider/translationuiprovidercontext/allowsreplacement)
- [var inputText: AttributedString?](/documentation/translationuiprovider/translationuiprovidercontext/inputtext)

### Instance Methods

- [func expandSheet()](/documentation/translationuiprovider/translationuiprovidercontext/expandsheet())
- [func finish(translation: AttributedString?)](/documentation/translationuiprovider/translationuiprovidercontext/finish(translation:))
- [TranslationUIProviderExtension](/documentation/translationuiprovider/translationuiproviderextension)

### Associated Types

- [Body](/documentation/translationuiprovider/translationuiproviderextension/body-swift.associatedtype)

### Instance Properties

- [var body: Self.Body](/documentation/translationuiprovider/translationuiproviderextension/body-swift.property)
- [TranslationUIProviderExtensionScene](/documentation/translationuiprovider/translationuiproviderextensionscene)

## Configuration and text selection

- [TranslationProviderUIExtensionConfiguration](/documentation/translationuiprovider/translationprovideruiextensionconfiguration)

### Creating a configuration

- [init(any TranslationUIProviderExtension)](/documentation/translationuiprovider/translationprovideruiextensionconfiguration/init(_:))
- [TranslationUIProviderSelectedTextScene](/documentation/translationuiprovider/translationuiproviderselectedtextscene)

### Initializers

- [init(content: (any TranslationUIProviderContext) -> Content)](/documentation/translationuiprovider/translationuiproviderselectedtextscene/init(content:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
