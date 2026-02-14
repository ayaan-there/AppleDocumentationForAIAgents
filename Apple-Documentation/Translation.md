# Translation Documentation

Source: https://sosumi.ai/documentation/translation

---
title: Translation
source: https://developer.apple.com/documentation/translation
timestamp: 2026-02-13T19:03:13.511Z
---

## Essentials

- [Translating text within your app](/documentation/translation/translating-text-within-your-app)
- [func translationPresentation(isPresented: Binding<Bool>, text: String, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge, replacementAction: ((String) -> Void)?) -> some View](/documentation/swiftui/view/translationpresentation(ispresented:text:attachmentanchor:arrowedge:replacementaction:))
- [func translationTask(TranslationSession.Configuration?, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(_:action:))
- [func translationTask(source: Locale.Language?, target: Locale.Language?, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(source:target:action:))
- [TranslationSession](/documentation/translation/translationsession)

### Initalizing a translation session

- [convenience init(installedSource: Locale.Language, target: Locale.Language?)](/documentation/translation/translationsession/init(installedsource:target:))

### Preparing for translation

- [TranslationSession.Configuration](/documentation/translation/translationsession/configuration)

#### Initializers

- [init(source: Locale.Language?, target: Locale.Language?)](/documentation/translation/translationsession/configuration/init(source:target:))

#### Instance Properties

- [var source: Locale.Language?](/documentation/translation/translationsession/configuration/source)
- [var target: Locale.Language?](/documentation/translation/translationsession/configuration/target)
- [var version: Int](/documentation/translation/translationsession/configuration/version)

#### Instance Methods

- [func invalidate()](/documentation/translation/translationsession/configuration/invalidate())
- [func prepareTranslation() async throws](/documentation/translation/translationsession/preparetranslation())

### Getting the language configuration

- [let sourceLanguage: Locale.Language?](/documentation/translation/translationsession/sourcelanguage)
- [let targetLanguage: Locale.Language?](/documentation/translation/translationsession/targetlanguage)

### Translating the text

- [func translate(String) async throws -> TranslationSession.Response](/documentation/translation/translationsession/translate(_:))
- [func translate(batch: [TranslationSession.Request]) -> TranslationSession.BatchResponse](/documentation/translation/translationsession/translate(batch:))
- [func translations(from: [TranslationSession.Request]) async throws -> [TranslationSession.Response]](/documentation/translation/translationsession/translations(from:))
- [TranslationSession.Request](/documentation/translation/translationsession/request)

#### Initializers

- [init(sourceText: String, clientIdentifier: String?)](/documentation/translation/translationsession/request/init(sourcetext:clientidentifier:))

#### Instance Properties

- [var clientIdentifier: String?](/documentation/translation/translationsession/request/clientidentifier)
- [var sourceText: String](/documentation/translation/translationsession/request/sourcetext)
- [TranslationSession.Response](/documentation/translation/translationsession/response)

#### Initializers

- [init(sourceLanguage: Locale.Language, targetLanguage: Locale.Language, sourceText: String, targetText: String, clientIdentifier: String?)](/documentation/translation/translationsession/response/init(sourcelanguage:targetlanguage:sourcetext:targettext:clientidentifier:))

#### Instance Properties

- [let clientIdentifier: String?](/documentation/translation/translationsession/response/clientidentifier)
- [let sourceLanguage: Locale.Language](/documentation/translation/translationsession/response/sourcelanguage)
- [let sourceText: String](/documentation/translation/translationsession/response/sourcetext)
- [let targetLanguage: Locale.Language](/documentation/translation/translationsession/response/targetlanguage)
- [let targetText: String](/documentation/translation/translationsession/response/targettext)
- [TranslationSession.BatchResponse](/documentation/translation/translationsession/batchresponse)

#### Structures

- [TranslationSession.BatchResponse.AsyncIterator](/documentation/translation/translationsession/batchresponse/asynciterator)

#### Instance Methods

- [func makeAsyncIterator() -> TranslationSession.BatchResponse.AsyncIterator](/documentation/translation/translationsession/batchresponse/makeasynciterator())

#### Type Aliases

- [TranslationSession.BatchResponse.Element](/documentation/translation/translationsession/batchresponse/element)

### Accessing the session properties

- [var canRequestDownloads: Bool](/documentation/translation/translationsession/canrequestdownloads)
- [var isReady: Bool](/documentation/translation/translationsession/isready)

### Cancelling a translation session

- [func cancel()](/documentation/translation/translationsession/cancel())

## Availability

- [LanguageAvailability](/documentation/translation/languageavailability)

### Creating a language availability

- [init()](/documentation/translation/languageavailability/init())

### Getting supported languages

- [var supportedLanguages: [Locale.Language]](/documentation/translation/languageavailability/supportedlanguages)

### Checking language availability

- [func status(from: Locale.Language, to: Locale.Language?) async -> LanguageAvailability.Status](/documentation/translation/languageavailability/status(from:to:))
- [func status(for: String, to: Locale.Language?) async throws -> LanguageAvailability.Status](/documentation/translation/languageavailability/status(for:to:))
- [LanguageAvailability.Status](/documentation/translation/languageavailability/status)

#### Enumeration Cases

- [case installed](/documentation/translation/languageavailability/status/installed)
- [case supported](/documentation/translation/languageavailability/status/supported)
- [case unsupported](/documentation/translation/languageavailability/status/unsupported)

## Errors

- [TranslationError](/documentation/translation/translationerror)

### Handling general errors

- [static let nothingToTranslate: TranslationError](/documentation/translation/translationerror/nothingtotranslate)
- [static let unableToIdentifyLanguage: TranslationError](/documentation/translation/translationerror/unabletoidentifylanguage)
- [static let internalError: TranslationError](/documentation/translation/translationerror/internalerror)
- [static let alreadyCancelled: TranslationError](/documentation/translation/translationerror/alreadycancelled)
- [static let notInstalled: TranslationError](/documentation/translation/translationerror/notinstalled)

### Handling unsupported errors

- [static let unsupportedSourceLanguage: TranslationError](/documentation/translation/translationerror/unsupportedsourcelanguage)
- [static let unsupportedTargetLanguage: TranslationError](/documentation/translation/translationerror/unsupportedtargetlanguage)
- [static let unsupportedLanguagePairing: TranslationError](/documentation/translation/translationerror/unsupportedlanguagepairing)

### Describing errors

- [var errorDescription: String?](/documentation/translation/translationerror/errordescription)
- [var failureReason: String?](/documentation/translation/translationerror/failurereason)

### Comparing errors

- [static func ~= (TranslationError, any Error) -> Bool](/documentation/translation/translationerror/~=(_:_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
