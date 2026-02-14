# Speech Documentation

Source: https://sosumi.ai/documentation/speech

---
title: Speech
source: https://developer.apple.com/documentation/speech
timestamp: 2026-02-13T19:24:18.350Z
---

## Essentials

- [Bringing advanced speech-to-text capabilities to your app](/documentation/speech/bringing-advanced-speech-to-text-capabilities-to-your-app)
- [SpeechAnalyzer](/documentation/speech/speechanalyzer)

### Creating an analyzer

- [convenience init(modules: [any SpeechModule], options: SpeechAnalyzer.Options?)](/documentation/speech/speechanalyzer/init(modules:options:))
- [convenience init<InputSequence>(inputSequence: InputSequence, modules: [any SpeechModule], options: SpeechAnalyzer.Options?, analysisContext: AnalysisContext, volatileRangeChangedHandler: sending ((CMTimeRange, Bool, Bool) -> Void)?)](/documentation/speech/speechanalyzer/init(inputsequence:modules:options:analysiscontext:volatilerangechangedhandler:))
- [convenience init(inputAudioFile: AVAudioFile, modules: [any SpeechModule], options: SpeechAnalyzer.Options?, analysisContext: AnalysisContext, finishAfterFile: Bool, volatileRangeChangedHandler: sending ((CMTimeRange, Bool, Bool) -> Void)?) async throws](/documentation/speech/speechanalyzer/init(inputaudiofile:modules:options:analysiscontext:finishafterfile:volatilerangechangedhandler:))
- [SpeechAnalyzer.Options](/documentation/speech/speechanalyzer/options)

#### Creating an options object

- [init(priority: TaskPriority, modelRetention: SpeechAnalyzer.Options.ModelRetention)](/documentation/speech/speechanalyzer/options/init(priority:modelretention:))
- [SpeechAnalyzer.Options.ModelRetention](/documentation/speech/speechanalyzer/options/modelretention-swift.enum)

##### Retention options

- [case lingering](/documentation/speech/speechanalyzer/options/modelretention-swift.enum/lingering)
- [case processLifetime](/documentation/speech/speechanalyzer/options/modelretention-swift.enum/processlifetime)
- [case whileInUse](/documentation/speech/speechanalyzer/options/modelretention-swift.enum/whileinuse)

#### Inspecting options

- [let modelRetention: SpeechAnalyzer.Options.ModelRetention](/documentation/speech/speechanalyzer/options/modelretention-swift.property)
- [let priority: TaskPriority](/documentation/speech/speechanalyzer/options/priority)

### Managing modules

- [func setModules([any SpeechModule]) async throws](/documentation/speech/speechanalyzer/setmodules(_:))
- [var modules: [any SpeechModule]](/documentation/speech/speechanalyzer/modules)

### Performing analysis

- [func analyzeSequence<InputSequence>(InputSequence) async throws -> CMTime?](/documentation/speech/speechanalyzer/analyzesequence(_:))
- [func analyzeSequence(from: AVAudioFile) async throws -> CMTime?](/documentation/speech/speechanalyzer/analyzesequence(from:))

### Performing autonomous analysis

- [func start<InputSequence>(inputSequence: InputSequence) async throws](/documentation/speech/speechanalyzer/start(inputsequence:))
- [func start(inputAudioFile: AVAudioFile, finishAfterFile: Bool) async throws](/documentation/speech/speechanalyzer/start(inputaudiofile:finishafterfile:))

### Finalizing and cancelling results

- [func cancelAnalysis(before: CMTime)](/documentation/speech/speechanalyzer/cancelanalysis(before:))
- [func finalize(through: CMTime?) async throws](/documentation/speech/speechanalyzer/finalize(through:))

### Finishing analysis

- [func cancelAndFinishNow() async](/documentation/speech/speechanalyzer/cancelandfinishnow())
- [func finalizeAndFinishThroughEndOfInput() async throws](/documentation/speech/speechanalyzer/finalizeandfinishthroughendofinput())
- [func finalizeAndFinish(through: CMTime) async throws](/documentation/speech/speechanalyzer/finalizeandfinish(through:))
- [func finish(after: CMTime) async throws](/documentation/speech/speechanalyzer/finish(after:))

### Determining audio formats

- [static func bestAvailableAudioFormat(compatibleWith: [any SpeechModule]) async -> AVAudioFormat?](/documentation/speech/speechanalyzer/bestavailableaudioformat(compatiblewith:))
- [static func bestAvailableAudioFormat(compatibleWith: [any SpeechModule], considering: AVAudioFormat?) async -> AVAudioFormat?](/documentation/speech/speechanalyzer/bestavailableaudioformat(compatiblewith:considering:))

### Improving responsiveness

- [func prepareToAnalyze(in: AVAudioFormat?) async throws](/documentation/speech/speechanalyzer/preparetoanalyze(in:))
- [func prepareToAnalyze(in: AVAudioFormat?, withProgressReadyHandler: sending ((Progress) -> Void)?) async throws](/documentation/speech/speechanalyzer/preparetoanalyze(in:withprogressreadyhandler:))

### Monitoring analysis

- [func setVolatileRangeChangedHandler(sending ((CMTimeRange, Bool, Bool) -> Void)?)](/documentation/speech/speechanalyzer/setvolatilerangechangedhandler(_:))
- [var volatileRange: CMTimeRange?](/documentation/speech/speechanalyzer/volatilerange)

### Managing contexts

- [func setContext(AnalysisContext) async throws](/documentation/speech/speechanalyzer/setcontext(_:))
- [var context: AnalysisContext](/documentation/speech/speechanalyzer/context)
- [AssetInventory](/documentation/speech/assetinventory)

### Downloading and installing assets

- [static func assetInstallationRequest(supporting: [any SpeechModule]) async throws -> AssetInstallationRequest?](/documentation/speech/assetinventory/assetinstallationrequest(supporting:))

### Checking asset status

- [static func status(forModules: [any SpeechModule]) async -> AssetInventory.Status](/documentation/speech/assetinventory/status(formodules:))
- [AssetInventory.Status](/documentation/speech/assetinventory/status)

#### Asset status

- [case downloading](/documentation/speech/assetinventory/status/downloading)
- [case installed](/documentation/speech/assetinventory/status/installed)
- [case supported](/documentation/speech/assetinventory/status/supported)
- [case unsupported](/documentation/speech/assetinventory/status/unsupported)

### Type Properties

- [static var maximumReservedLocales: Int](/documentation/speech/assetinventory/maximumreservedlocales)
- [static var reservedLocales: [Locale]](/documentation/speech/assetinventory/reservedlocales)

### Type Methods

- [static func release(reservedLocale: Locale) async -> Bool](/documentation/speech/assetinventory/release(reservedlocale:))
- [static func reserve(locale: Locale) async throws -> Bool](/documentation/speech/assetinventory/reserve(locale:))

## Modules

- [SpeechTranscriber](/documentation/speech/speechtranscriber)

### Creating a transcriber

- [convenience init(locale: Locale, preset: SpeechTranscriber.Preset)](/documentation/speech/speechtranscriber/init(locale:preset:))
- [convenience init(locale: Locale, transcriptionOptions: Set<SpeechTranscriber.TranscriptionOption>, reportingOptions: Set<SpeechTranscriber.ReportingOption>, attributeOptions: Set<SpeechTranscriber.ResultAttributeOption>)](/documentation/speech/speechtranscriber/init(locale:transcriptionoptions:reportingoptions:attributeoptions:))
- [SpeechTranscriber.Preset](/documentation/speech/speechtranscriber/preset)

#### Standard presets

- [static let transcription: SpeechTranscriber.Preset](/documentation/speech/speechtranscriber/preset/transcription)
- [static let transcriptionWithAlternatives: SpeechTranscriber.Preset](/documentation/speech/speechtranscriber/preset/transcriptionwithalternatives)
- [static let timeIndexedTranscriptionWithAlternatives: SpeechTranscriber.Preset](/documentation/speech/speechtranscriber/preset/timeindexedtranscriptionwithalternatives)
- [static let progressiveTranscription: SpeechTranscriber.Preset](/documentation/speech/speechtranscriber/preset/progressivetranscription)
- [static let timeIndexedProgressiveTranscription: SpeechTranscriber.Preset](/documentation/speech/speechtranscriber/preset/timeindexedprogressivetranscription)

#### Creating a preset

- [init(transcriptionOptions: Set<SpeechTranscriber.TranscriptionOption>, reportingOptions: Set<SpeechTranscriber.ReportingOption>, attributeOptions: Set<SpeechTranscriber.ResultAttributeOption>)](/documentation/speech/speechtranscriber/preset/init(transcriptionoptions:reportingoptions:attributeoptions:))

#### Getting preset properties

- [var attributeOptions: Set<SpeechTranscriber.ResultAttributeOption>](/documentation/speech/speechtranscriber/preset/attributeoptions)
- [var reportingOptions: Set<SpeechTranscriber.ReportingOption>](/documentation/speech/speechtranscriber/preset/reportingoptions)
- [var transcriptionOptions: Set<SpeechTranscriber.TranscriptionOption>](/documentation/speech/speechtranscriber/preset/transcriptionoptions)

### Configuring transcription

- [SpeechTranscriber.ReportingOption](/documentation/speech/speechtranscriber/reportingoption)

#### Reporting options

- [case alternativeTranscriptions](/documentation/speech/speechtranscriber/reportingoption/alternativetranscriptions)
- [case fastResults](/documentation/speech/speechtranscriber/reportingoption/fastresults)
- [case volatileResults](/documentation/speech/speechtranscriber/reportingoption/volatileresults)
- [SpeechTranscriber.ResultAttributeOption](/documentation/speech/speechtranscriber/resultattributeoption)

#### Result attribute options

- [case audioTimeRange](/documentation/speech/speechtranscriber/resultattributeoption/audiotimerange)
- [case transcriptionConfidence](/documentation/speech/speechtranscriber/resultattributeoption/transcriptionconfidence)
- [SpeechTranscriber.TranscriptionOption](/documentation/speech/speechtranscriber/transcriptionoption)

#### Transcription options

- [case etiquetteReplacements](/documentation/speech/speechtranscriber/transcriptionoption/etiquettereplacements)

### Checking device support

- [static var isAvailable: Bool](/documentation/speech/speechtranscriber/isavailable)

### Checking locale support

- [static var installedLocales: [Locale]](/documentation/speech/speechtranscriber/installedlocales)
- [static var supportedLocales: [Locale]](/documentation/speech/speechtranscriber/supportedlocales)
- [static func supportedLocale(equivalentTo: Locale) async -> Locale?](/documentation/speech/speechtranscriber/supportedlocale(equivalentto:))

### Getting results

- [SpeechTranscriber.Result](/documentation/speech/speechtranscriber/result)

#### Getting transcriptions

- [let alternatives: [AttributedString]](/documentation/speech/speechtranscriber/result/alternatives)
- [var text: AttributedString](/documentation/speech/speechtranscriber/result/text)

#### Working with transcriptions

- [AttributeScopes.SpeechAttributes.TimeRangeAttribute](/documentation/foundation/attributescopes/speechattributes/timerangeattribute)
- [AttributeScopes.SpeechAttributes.ConfidenceAttribute](/documentation/foundation/attributescopes/speechattributes/confidenceattribute)
- [func rangeOfAudioTimeRangeAttributes(intersecting: CMTimeRange) -> Range<AttributedString.Index>?](/documentation/foundation/attributedstring/rangeofaudiotimerangeattributes(intersecting:))
- [DictationTranscriber](/documentation/speech/dictationtranscriber)

### Creating a transcriber

- [convenience init(locale: Locale, preset: DictationTranscriber.Preset)](/documentation/speech/dictationtranscriber/init(locale:preset:))
- [convenience init(locale: Locale, contentHints: Set<DictationTranscriber.ContentHint>, transcriptionOptions: Set<DictationTranscriber.TranscriptionOption>, reportingOptions: Set<DictationTranscriber.ReportingOption>, attributeOptions: Set<DictationTranscriber.ResultAttributeOption>)](/documentation/speech/dictationtranscriber/init(locale:contenthints:transcriptionoptions:reportingoptions:attributeoptions:))
- [DictationTranscriber.Preset](/documentation/speech/dictationtranscriber/preset)

#### Standard presets

- [static let phrase: DictationTranscriber.Preset](/documentation/speech/dictationtranscriber/preset/phrase)
- [static let shortDictation: DictationTranscriber.Preset](/documentation/speech/dictationtranscriber/preset/shortdictation)
- [static let progressiveShortDictation: DictationTranscriber.Preset](/documentation/speech/dictationtranscriber/preset/progressiveshortdictation)
- [static let longDictation: DictationTranscriber.Preset](/documentation/speech/dictationtranscriber/preset/longdictation)
- [static let progressiveLongDictation: DictationTranscriber.Preset](/documentation/speech/dictationtranscriber/preset/progressivelongdictation)
- [static let timeIndexedLongDictation: DictationTranscriber.Preset](/documentation/speech/dictationtranscriber/preset/timeindexedlongdictation)

#### Creating a preset

- [init(contentHints: Set<DictationTranscriber.ContentHint>, transcriptionOptions: Set<DictationTranscriber.TranscriptionOption>, reportingOptions: Set<DictationTranscriber.ReportingOption>, attributeOptions: Set<DictationTranscriber.ResultAttributeOption>)](/documentation/speech/dictationtranscriber/preset/init(contenthints:transcriptionoptions:reportingoptions:attributeoptions:))

#### Getting preset properties

- [var attributeOptions: Set<DictationTranscriber.ResultAttributeOption>](/documentation/speech/dictationtranscriber/preset/attributeoptions)
- [var contentHints: Set<DictationTranscriber.ContentHint>](/documentation/speech/dictationtranscriber/preset/contenthints)
- [var reportingOptions: Set<DictationTranscriber.ReportingOption>](/documentation/speech/dictationtranscriber/preset/reportingoptions)
- [var transcriptionOptions: Set<DictationTranscriber.TranscriptionOption>](/documentation/speech/dictationtranscriber/preset/transcriptionoptions)

### Configuring transcription

- [DictationTranscriber.ContentHint](/documentation/speech/dictationtranscriber/contenthint)

#### Content hints

- [static let shortForm: DictationTranscriber.ContentHint](/documentation/speech/dictationtranscriber/contenthint/shortform)
- [static let farField: DictationTranscriber.ContentHint](/documentation/speech/dictationtranscriber/contenthint/farfield)
- [static func customizedLanguage(modelConfiguration: SFSpeechLanguageModel.Configuration) -> DictationTranscriber.ContentHint](/documentation/speech/dictationtranscriber/contenthint/customizedlanguage(modelconfiguration:))
- [static let atypicalSpeech: DictationTranscriber.ContentHint](/documentation/speech/dictationtranscriber/contenthint/atypicalspeech)
- [DictationTranscriber.ReportingOption](/documentation/speech/dictationtranscriber/reportingoption)

#### Reporting options

- [case alternativeTranscriptions](/documentation/speech/dictationtranscriber/reportingoption/alternativetranscriptions)
- [case frequentFinalization](/documentation/speech/dictationtranscriber/reportingoption/frequentfinalization)
- [case volatileResults](/documentation/speech/dictationtranscriber/reportingoption/volatileresults)
- [DictationTranscriber.ResultAttributeOption](/documentation/speech/dictationtranscriber/resultattributeoption)

#### Result attribute options

- [case audioTimeRange](/documentation/speech/dictationtranscriber/resultattributeoption/audiotimerange)
- [case transcriptionConfidence](/documentation/speech/dictationtranscriber/resultattributeoption/transcriptionconfidence)
- [DictationTranscriber.TranscriptionOption](/documentation/speech/dictationtranscriber/transcriptionoption)

#### Transcription options

- [case emoji](/documentation/speech/dictationtranscriber/transcriptionoption/emoji)
- [case etiquetteReplacements](/documentation/speech/dictationtranscriber/transcriptionoption/etiquettereplacements)
- [case punctuation](/documentation/speech/dictationtranscriber/transcriptionoption/punctuation)

### Checking locale support

- [static var installedLocales: [Locale]](/documentation/speech/dictationtranscriber/installedlocales)
- [static var supportedLocales: [Locale]](/documentation/speech/dictationtranscriber/supportedlocales)
- [static func supportedLocale(equivalentTo: Locale) async -> Locale?](/documentation/speech/dictationtranscriber/supportedlocale(equivalentto:))

### Getting results

- [DictationTranscriber.Result](/documentation/speech/dictationtranscriber/result)

#### Getting transcriptions

- [let alternatives: [AttributedString]](/documentation/speech/dictationtranscriber/result/alternatives)
- [var text: AttributedString](/documentation/speech/dictationtranscriber/result/text)

#### Working with transcriptions

- [AttributeScopes.SpeechAttributes.TimeRangeAttribute](/documentation/foundation/attributescopes/speechattributes/timerangeattribute)
- [AttributeScopes.SpeechAttributes.ConfidenceAttribute](/documentation/foundation/attributescopes/speechattributes/confidenceattribute)
- [func rangeOfAudioTimeRangeAttributes(intersecting: CMTimeRange) -> Range<AttributedString.Index>?](/documentation/foundation/attributedstring/rangeofaudiotimerangeattributes(intersecting:))
- [SpeechDetector](/documentation/speech/speechdetector)

### Creating a detector

- [convenience init()](/documentation/speech/speechdetector/init())
- [init(detectionOptions: SpeechDetector.DetectionOptions, reportResults: Bool)](/documentation/speech/speechdetector/init(detectionoptions:reportresults:))
- [SpeechDetector.DetectionOptions](/documentation/speech/speechdetector/detectionoptions)

#### Creating an options object

- [init(sensitivityLevel: SpeechDetector.SensitivityLevel)](/documentation/speech/speechdetector/detectionoptions/init(sensitivitylevel:))

#### Inspecting options

- [let sensitivityLevel: SpeechDetector.SensitivityLevel](/documentation/speech/speechdetector/detectionoptions/sensitivitylevel)
- [SpeechDetector.SensitivityLevel](/documentation/speech/speechdetector/sensitivitylevel)

#### Sensitivity levels

- [case high](/documentation/speech/speechdetector/sensitivitylevel/high)
- [case low](/documentation/speech/speechdetector/sensitivitylevel/low)
- [case medium](/documentation/speech/speechdetector/sensitivitylevel/medium)

### Getting results

- [SpeechDetector.Result](/documentation/speech/speechdetector/result)

#### Getting detection results

- [let speechDetected: Bool](/documentation/speech/speechdetector/result/speechdetected)
- [SpeechModule](/documentation/speech/speechmodule)

### Checking audio format support

- [var availableCompatibleAudioFormats: [AVAudioFormat]](/documentation/speech/speechmodule/availablecompatibleaudioformats)

### Getting results

- [var results: Self.Results](/documentation/speech/speechmodule/results-swift.property)
- [Result](/documentation/speech/speechmodule/result)
- [Results](/documentation/speech/speechmodule/results-swift.associatedtype)
- [LocaleDependentSpeechModule](/documentation/speech/localedependentspeechmodule)

### Getting supported locales

- [static var supportedLocales: [Locale]](/documentation/speech/localedependentspeechmodule/supportedlocales)
- [static func supportedLocale(equivalentTo: Locale) async -> Locale?](/documentation/speech/localedependentspeechmodule/supportedlocale(equivalentto:))

### Inspecting an instance’s locales

- [var selectedLocales: [Locale]](/documentation/speech/localedependentspeechmodule/selectedlocales)

## Input and output

- [AnalyzerInput](/documentation/speech/analyzerinput)

### Creating an input element

- [init(buffer: AVAudioPCMBuffer)](/documentation/speech/analyzerinput/init(buffer:))
- [init(buffer: AVAudioPCMBuffer, bufferStartTime: CMTime?)](/documentation/speech/analyzerinput/init(buffer:bufferstarttime:))

### Inspecting an input element

- [let buffer: AVAudioPCMBuffer](/documentation/speech/analyzerinput/buffer)
- [let bufferStartTime: CMTime?](/documentation/speech/analyzerinput/bufferstarttime)
- [SpeechModuleResult](/documentation/speech/speechmoduleresult)

### Getting audio range

- [var range: CMTimeRange](/documentation/speech/speechmoduleresult/range)

### Getting finalization state

- [var isFinal: Bool](/documentation/speech/speechmoduleresult/isfinal)
- [var resultsFinalizationTime: CMTime](/documentation/speech/speechmoduleresult/resultsfinalizationtime)

## Custom vocabulary

- [AnalysisContext](/documentation/speech/analysiscontext)

### Creating a context

- [init()](/documentation/speech/analysiscontext/init())

### Providing textual context

- [var contextualStrings: [AnalysisContext.ContextualStringsTag : [String]]](/documentation/speech/analysiscontext/contextualstrings)
- [AnalysisContext.ContextualStringsTag](/documentation/speech/analysiscontext/contextualstringstag)

#### Creating a tag

- [init(AnalysisContext.ContextualStringsTag.RawValue)](/documentation/speech/analysiscontext/contextualstringstag/init(_:))

#### Predefined tags

- [static let general: AnalysisContext.ContextualStringsTag](/documentation/speech/analysiscontext/contextualstringstag/general)

### Preserving app-specific context

- [var userData: [AnalysisContext.UserDataTag : any Sendable]](/documentation/speech/analysiscontext/userdata)
- [AnalysisContext.UserDataTag](/documentation/speech/analysiscontext/userdatatag)

#### Creating a tag

- [init(AnalysisContext.UserDataTag.RawValue)](/documentation/speech/analysiscontext/userdatatag/init(_:))
- [SFSpeechLanguageModel](/documentation/speech/sfspeechlanguagemodel)

### Creating a custom language model

- [class func prepareCustomLanguageModel(for: URL, configuration: SFSpeechLanguageModel.Configuration, completion: ((any Error)?) -> Void)](/documentation/speech/sfspeechlanguagemodel/preparecustomlanguagemodel(for:configuration:completion:))
- [class func prepareCustomLanguageModel(for: URL, configuration: SFSpeechLanguageModel.Configuration, ignoresCache: Bool, completion: ((any Error)?) -> Void)](/documentation/speech/sfspeechlanguagemodel/preparecustomlanguagemodel(for:configuration:ignorescache:completion:))
- [SFSpeechLanguageModel.Configuration](/documentation/speech/sfspeechlanguagemodel/configuration)

#### Creating a language model configuration

- [init(languageModel: URL)](/documentation/speech/sfspeechlanguagemodel/configuration/init(languagemodel:))
- [init(languageModel: URL, vocabulary: URL?)](/documentation/speech/sfspeechlanguagemodel/configuration/init(languagemodel:vocabulary:))
- [init(languageModel: URL, vocabulary: URL?, weight: NSNumber?)](/documentation/speech/sfspeechlanguagemodel/configuration/init(languagemodel:vocabulary:weight:))

#### Inspecting a language model

- [var languageModel: URL](/documentation/speech/sfspeechlanguagemodel/configuration/languagemodel)
- [var vocabulary: URL?](/documentation/speech/sfspeechlanguagemodel/configuration/vocabulary)
- [var weight: NSNumber?](/documentation/speech/sfspeechlanguagemodel/configuration/weight)

### Type Methods

- [class func prepareCustomLanguageModel(for: URL, clientIdentifier: String, configuration: SFSpeechLanguageModel.Configuration, completion: ((any Error)?) -> Void)](/documentation/speech/sfspeechlanguagemodel/preparecustomlanguagemodel(for:clientidentifier:configuration:completion:))
- [class func prepareCustomLanguageModel(for: URL, clientIdentifier: String, configuration: SFSpeechLanguageModel.Configuration, ignoresCache: Bool, completion: ((any Error)?) -> Void)](/documentation/speech/sfspeechlanguagemodel/preparecustomlanguagemodel(for:clientidentifier:configuration:ignorescache:completion:))
- [SFSpeechLanguageModel.Configuration](/documentation/speech/sfspeechlanguagemodel/configuration)

### Creating a language model configuration

- [init(languageModel: URL)](/documentation/speech/sfspeechlanguagemodel/configuration/init(languagemodel:))
- [init(languageModel: URL, vocabulary: URL?)](/documentation/speech/sfspeechlanguagemodel/configuration/init(languagemodel:vocabulary:))
- [init(languageModel: URL, vocabulary: URL?, weight: NSNumber?)](/documentation/speech/sfspeechlanguagemodel/configuration/init(languagemodel:vocabulary:weight:))

### Inspecting a language model

- [var languageModel: URL](/documentation/speech/sfspeechlanguagemodel/configuration/languagemodel)
- [var vocabulary: URL?](/documentation/speech/sfspeechlanguagemodel/configuration/vocabulary)
- [var weight: NSNumber?](/documentation/speech/sfspeechlanguagemodel/configuration/weight)
- [SFCustomLanguageModelData](/documentation/speech/sfcustomlanguagemodeldata)

### Creating a model data container

- [convenience init(locale: Locale, identifier: String, version: String, builder: () -> any DataInsertable)](/documentation/speech/sfcustomlanguagemodeldata/init(locale:identifier:version:builder:))
- [init(locale: Locale, identifier: String, version: String)](/documentation/speech/sfcustomlanguagemodeldata/init(locale:identifier:version:))
- [SFCustomLanguageModelData.DataInsertableBuilder](/documentation/speech/sfcustomlanguagemodeldata/datainsertablebuilder)

#### Result builder methods

- [static func buildArray([any DataInsertable]) -> any DataInsertable](/documentation/speech/sfcustomlanguagemodeldata/datainsertablebuilder/buildarray(_:))
- [static func buildBlock(any DataInsertable...) -> any DataInsertable](/documentation/speech/sfcustomlanguagemodeldata/datainsertablebuilder/buildblock(_:))
- [static func buildEither(first: any DataInsertable) -> any DataInsertable](/documentation/speech/sfcustomlanguagemodeldata/datainsertablebuilder/buildeither(first:))
- [static func buildEither(second: any DataInsertable) -> any DataInsertable](/documentation/speech/sfcustomlanguagemodeldata/datainsertablebuilder/buildeither(second:))
- [static func buildOptional((any DataInsertable)?) -> any DataInsertable](/documentation/speech/sfcustomlanguagemodeldata/datainsertablebuilder/buildoptional(_:))

### Adding terms

- [func insert(term: SFCustomLanguageModelData.CustomPronunciation)](/documentation/speech/sfcustomlanguagemodeldata/insert(term:))
- [static func supportedPhonemes(locale: Locale) -> [String]](/documentation/speech/sfcustomlanguagemodeldata/supportedphonemes(locale:))
- [SFCustomLanguageModelData.CustomPronunciation](/documentation/speech/sfcustomlanguagemodeldata/custompronunciation)

#### Creating a term

- [init(grapheme: String, phonemes: [String])](/documentation/speech/sfcustomlanguagemodeldata/custompronunciation/init(grapheme:phonemes:))

#### Inspecting a term

- [let grapheme: String](/documentation/speech/sfcustomlanguagemodeldata/custompronunciation/grapheme)
- [let phonemes: [String]](/documentation/speech/sfcustomlanguagemodeldata/custompronunciation/phonemes)

### Adding phrases

- [func insert(phraseCount: SFCustomLanguageModelData.PhraseCount)](/documentation/speech/sfcustomlanguagemodeldata/insert(phrasecount:))
- [SFCustomLanguageModelData.PhraseCount](/documentation/speech/sfcustomlanguagemodeldata/phrasecount)

#### Creating a weighted phrase

- [init(phrase: String, count: Int)](/documentation/speech/sfcustomlanguagemodeldata/phrasecount/init(phrase:count:))

#### Inspecting the weighted phrase

- [let count: Int](/documentation/speech/sfcustomlanguagemodeldata/phrasecount/count)
- [let phrase: String](/documentation/speech/sfcustomlanguagemodeldata/phrasecount/phrase)

### Adding parameterized sample data within a result builder

- [SFCustomLanguageModelData.PhraseCountsFromTemplates](/documentation/speech/sfcustomlanguagemodeldata/phrasecountsfromtemplates)

#### Creating weighted phrases from templates

- [init(classes: [String : [String]], builder: () -> any TemplateInsertable)](/documentation/speech/sfcustomlanguagemodeldata/phrasecountsfromtemplates/init(classes:builder:))
- [SFCustomLanguageModelData.TemplateInsertableBuilder](/documentation/speech/sfcustomlanguagemodeldata/templateinsertablebuilder)

#### Result builder methods

- [static func buildArray([any TemplateInsertable]) -> any TemplateInsertable](/documentation/speech/sfcustomlanguagemodeldata/templateinsertablebuilder/buildarray(_:))
- [static func buildBlock(any TemplateInsertable...) -> any TemplateInsertable](/documentation/speech/sfcustomlanguagemodeldata/templateinsertablebuilder/buildblock(_:))
- [static func buildEither(first: any TemplateInsertable) -> any TemplateInsertable](/documentation/speech/sfcustomlanguagemodeldata/templateinsertablebuilder/buildeither(first:))
- [static func buildEither(second: any TemplateInsertable) -> any TemplateInsertable](/documentation/speech/sfcustomlanguagemodeldata/templateinsertablebuilder/buildeither(second:))
- [static func buildOptional((any TemplateInsertable)?) -> any TemplateInsertable](/documentation/speech/sfcustomlanguagemodeldata/templateinsertablebuilder/buildoptional(_:))

### Adding parameterized sample data with a generator

- [func insert(phraseCountGenerator: SFCustomLanguageModelData.PhraseCountGenerator)](/documentation/speech/sfcustomlanguagemodeldata/insert(phrasecountgenerator:))
- [SFCustomLanguageModelData.TemplatePhraseCountGenerator](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator)

#### Defining template tokens

- [func define(className: String, values: [String])](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/define(classname:values:))

#### Adding a template

- [func insert(template: String, count: Int)](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/insert(template:count:))
- [SFCustomLanguageModelData.TemplatePhraseCountGenerator.Template](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/template)

##### Creating a template

- [init(String, count: Int)](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/template/init(_:count:))

##### Inspecting the template

- [let body: String](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/template/body)
- [let count: Int](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/template/count)

#### Classes

- [SFCustomLanguageModelData.TemplatePhraseCountGenerator.Iterator](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/iterator)

##### Initializers

- [init(templates: [SFCustomLanguageModelData.TemplatePhraseCountGenerator.Template], templateClasses: [String : [String]])](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/iterator/init(templates:templateclasses:))

##### Instance Methods

- [func next() async throws -> SFCustomLanguageModelData.PhraseCount?](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/iterator/next())

##### Type Aliases

- [SFCustomLanguageModelData.TemplatePhraseCountGenerator.Iterator.Element](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/iterator/element)

#### Operators

- [static func == (SFCustomLanguageModelData.TemplatePhraseCountGenerator, SFCustomLanguageModelData.TemplatePhraseCountGenerator) -> Bool](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/==(_:_:))

#### Initializers

- [init()](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/init())
- [init(from: any Decoder) throws](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/init(from:))

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/hash(into:))
- [func makeAsyncIterator() -> SFCustomLanguageModelData.PhraseCountGenerator.Iterator](/documentation/speech/sfcustomlanguagemodeldata/templatephrasecountgenerator/makeasynciterator())
- [SFCustomLanguageModelData.PhraseCountGenerator](/documentation/speech/sfcustomlanguagemodeldata/phrasecountgenerator)

#### Protocol requirements

- [init()](/documentation/speech/sfcustomlanguagemodeldata/phrasecountgenerator/init())
- [SFCustomLanguageModelData.PhraseCountGenerator.Iterator](/documentation/speech/sfcustomlanguagemodeldata/phrasecountgenerator/iterator)

### Exporting model data

- [func export(to: URL) async throws](/documentation/speech/sfcustomlanguagemodeldata/export(to:))

### Inspecting model data

- [let identifier: String](/documentation/speech/sfcustomlanguagemodeldata/identifier)
- [let locale: Locale](/documentation/speech/sfcustomlanguagemodeldata/locale)
- [let version: String](/documentation/speech/sfcustomlanguagemodeldata/version)

### Result builder support

- [SFCustomLanguageModelData.CompoundTemplate](/documentation/speech/sfcustomlanguagemodeldata/compoundtemplate)

#### Result builder methods

- [init([any TemplateInsertable])](/documentation/speech/sfcustomlanguagemodeldata/compoundtemplate/init(_:))
- [DataInsertable](/documentation/speech/datainsertable)

#### Protocol requirements

- [func insert(data: SFCustomLanguageModelData)](/documentation/speech/datainsertable/insert(data:))
- [TemplateInsertable](/documentation/speech/templateinsertable)

#### Protocol requirements

- [func insert(generator: SFCustomLanguageModelData.TemplatePhraseCountGenerator)](/documentation/speech/templateinsertable/insert(generator:))

## Asset and resource management

- [AssetInstallationRequest](/documentation/speech/assetinstallationrequest)

### Performing an installation request

- [func downloadAndInstall() async throws](/documentation/speech/assetinstallationrequest/downloadandinstall())
- [SpeechModels](/documentation/speech/speechmodels)

### Releasing cached models

- [static func endRetention() async](/documentation/speech/speechmodels/endretention())

## Legacy API

- [Speech Recognition in Objective-C](/documentation/speech/speech-recognition-in-objc)

### Essentials

- [Asking Permission to Use Speech Recognition](/documentation/speech/asking-permission-to-use-speech-recognition)
- [SFSpeechRecognizer](/documentation/speech/sfspeechrecognizer)

#### Creating a speech recognizer

- [convenience init?()](/documentation/speech/sfspeechrecognizer/init())
- [init?(locale: Locale)](/documentation/speech/sfspeechrecognizer/init(locale:))

#### Monitoring speech recognition availability

- [var delegate: (any SFSpeechRecognizerDelegate)?](/documentation/speech/sfspeechrecognizer/delegate)
- [SFSpeechRecognizerDelegate](/documentation/speech/sfspeechrecognizerdelegate)

##### Monitoring speech recognizer availability

- [func speechRecognizer(SFSpeechRecognizer, availabilityDidChange: Bool)](/documentation/speech/sfspeechrecognizerdelegate/speechrecognizer(_:availabilitydidchange:))
- [var isAvailable: Bool](/documentation/speech/sfspeechrecognizer/isavailable)
- [var supportsOnDeviceRecognition: Bool](/documentation/speech/sfspeechrecognizer/supportsondevicerecognition)

#### Requesting user authorization

- [class func requestAuthorization((SFSpeechRecognizerAuthorizationStatus) -> Void)](/documentation/speech/sfspeechrecognizer/requestauthorization(_:))
- [class func authorizationStatus() -> SFSpeechRecognizerAuthorizationStatus](/documentation/speech/sfspeechrecognizer/authorizationstatus())
- [SFSpeechRecognizerAuthorizationStatus](/documentation/speech/sfspeechrecognizerauthorizationstatus)

##### Authorization statuses

- [case notDetermined](/documentation/speech/sfspeechrecognizerauthorizationstatus/notdetermined)
- [case denied](/documentation/speech/sfspeechrecognizerauthorizationstatus/denied)
- [case restricted](/documentation/speech/sfspeechrecognizerauthorizationstatus/restricted)
- [case authorized](/documentation/speech/sfspeechrecognizerauthorizationstatus/authorized)

##### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeechrecognizerauthorizationstatus/init(rawvalue:))

#### Configuring the speech recognizer

- [var defaultTaskHint: SFSpeechRecognitionTaskHint](/documentation/speech/sfspeechrecognizer/defaulttaskhint)
- [var queue: OperationQueue](/documentation/speech/sfspeechrecognizer/queue)

#### Performing speech recognition on audio

- [func recognitionTask(with: SFSpeechRecognitionRequest, resultHandler: (SFSpeechRecognitionResult?, (any Error)?) -> Void) -> SFSpeechRecognitionTask](/documentation/speech/sfspeechrecognizer/recognitiontask(with:resulthandler:))
- [func recognitionTask(with: SFSpeechRecognitionRequest, delegate: any SFSpeechRecognitionTaskDelegate) -> SFSpeechRecognitionTask](/documentation/speech/sfspeechrecognizer/recognitiontask(with:delegate:))
- [SFSpeechRecognitionTaskDelegate](/documentation/speech/sfspeechrecognitiontaskdelegate)

##### Tracking task progress

- [func speechRecognitionDidDetectSpeech(SFSpeechRecognitionTask)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiondiddetectspeech(_:))
- [func speechRecognitionTaskFinishedReadingAudio(SFSpeechRecognitionTask)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontaskfinishedreadingaudio(_:))

##### Getting transcriptions

- [func speechRecognitionTask(SFSpeechRecognitionTask, didHypothesizeTranscription: SFTranscription)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didhypothesizetranscription:))

##### Finishing a speech recognition task

- [func speechRecognitionTask(SFSpeechRecognitionTask, didFinishRecognition: SFSpeechRecognitionResult)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didfinishrecognition:))
- [func speechRecognitionTask(SFSpeechRecognitionTask, didFinishSuccessfully: Bool)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didfinishsuccessfully:))
- [func speechRecognitionTask(SFSpeechRecognitionTask, didProcessAudioDuration: TimeInterval)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didprocessaudioduration:))
- [func speechRecognitionTaskWasCancelled(SFSpeechRecognitionTask)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontaskwascancelled(_:))

#### Getting the current language

- [var locale: Locale](/documentation/speech/sfspeechrecognizer/locale)
- [class func supportedLocales() -> Set<Locale>](/documentation/speech/sfspeechrecognizer/supportedlocales())
- [SFSpeechRecognizerDelegate](/documentation/speech/sfspeechrecognizerdelegate)

#### Monitoring speech recognizer availability

- [func speechRecognizer(SFSpeechRecognizer, availabilityDidChange: Bool)](/documentation/speech/sfspeechrecognizerdelegate/speechrecognizer(_:availabilitydidchange:))
- [SFSpeechRecognitionTaskHint](/documentation/speech/sfspeechrecognitiontaskhint)

#### Hints

- [case unspecified](/documentation/speech/sfspeechrecognitiontaskhint/unspecified)
- [case dictation](/documentation/speech/sfspeechrecognitiontaskhint/dictation)
- [case search](/documentation/speech/sfspeechrecognitiontaskhint/search)
- [case confirmation](/documentation/speech/sfspeechrecognitiontaskhint/confirmation)

#### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeechrecognitiontaskhint/init(rawvalue:))
- [SFSpeechRecognizerAuthorizationStatus](/documentation/speech/sfspeechrecognizerauthorizationstatus)

#### Authorization statuses

- [case notDetermined](/documentation/speech/sfspeechrecognizerauthorizationstatus/notdetermined)
- [case denied](/documentation/speech/sfspeechrecognizerauthorizationstatus/denied)
- [case restricted](/documentation/speech/sfspeechrecognizerauthorizationstatus/restricted)
- [case authorized](/documentation/speech/sfspeechrecognizerauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeechrecognizerauthorizationstatus/init(rawvalue:))

### Audio sources

- [Recognizing speech in live audio](/documentation/speech/recognizing-speech-in-live-audio)
- [SFSpeechURLRecognitionRequest](/documentation/speech/sfspeechurlrecognitionrequest)

#### Creating a speech recognition request

- [init(url: URL)](/documentation/speech/sfspeechurlrecognitionrequest/init(url:))

#### Accessing the audio file URL

- [var url: URL](/documentation/speech/sfspeechurlrecognitionrequest/url)
- [SFSpeechAudioBufferRecognitionRequest](/documentation/speech/sfspeechaudiobufferrecognitionrequest)

#### Appending Audio Buffers

- [func append(AVAudioPCMBuffer)](/documentation/speech/sfspeechaudiobufferrecognitionrequest/append(_:))
- [func appendAudioSampleBuffer(CMSampleBuffer)](/documentation/speech/sfspeechaudiobufferrecognitionrequest/appendaudiosamplebuffer(_:))
- [func endAudio()](/documentation/speech/sfspeechaudiobufferrecognitionrequest/endaudio())

#### Getting the Audio Format

- [var nativeAudioFormat: AVAudioFormat](/documentation/speech/sfspeechaudiobufferrecognitionrequest/nativeaudioformat)
- [SFSpeechRecognitionRequest](/documentation/speech/sfspeechrecognitionrequest)

#### Configuring a recognition request

- [var requiresOnDeviceRecognition: Bool](/documentation/speech/sfspeechrecognitionrequest/requiresondevicerecognition)
- [var shouldReportPartialResults: Bool](/documentation/speech/sfspeechrecognitionrequest/shouldreportpartialresults)
- [var contextualStrings: [String]](/documentation/speech/sfspeechrecognitionrequest/contextualstrings)

#### Speech Type Classification

- [var taskHint: SFSpeechRecognitionTaskHint](/documentation/speech/sfspeechrecognitionrequest/taskhint)
- [SFSpeechRecognitionTaskHint](/documentation/speech/sfspeechrecognitiontaskhint)

##### Hints

- [case unspecified](/documentation/speech/sfspeechrecognitiontaskhint/unspecified)
- [case dictation](/documentation/speech/sfspeechrecognitiontaskhint/dictation)
- [case search](/documentation/speech/sfspeechrecognitiontaskhint/search)
- [case confirmation](/documentation/speech/sfspeechrecognitiontaskhint/confirmation)

##### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeechrecognitiontaskhint/init(rawvalue:))

#### Punctuation

- [var addsPunctuation: Bool](/documentation/speech/sfspeechrecognitionrequest/addspunctuation)

#### Deprecated

- [var interactionIdentifier: String?](/documentation/speech/sfspeechrecognitionrequest/interactionidentifier)

#### Instance Properties

- [var customizedLanguageModel: SFSpeechLanguageModel.Configuration?](/documentation/speech/sfspeechrecognitionrequest/customizedlanguagemodel)

### In-progress requests

- [SFSpeechRecognitionTask](/documentation/speech/sfspeechrecognitiontask)

#### Canceling a speech recognition task

- [func cancel()](/documentation/speech/sfspeechrecognitiontask/cancel())
- [var isCancelled: Bool](/documentation/speech/sfspeechrecognitiontask/iscancelled)

#### Finishing a speech recognition task

- [func finish()](/documentation/speech/sfspeechrecognitiontask/finish())
- [var isFinishing: Bool](/documentation/speech/sfspeechrecognitiontask/isfinishing)

#### Monitoring recognition progress

- [var state: SFSpeechRecognitionTaskState](/documentation/speech/sfspeechrecognitiontask/state)
- [SFSpeechRecognitionTaskState](/documentation/speech/sfspeechrecognitiontaskstate)

##### Task states

- [case canceling](/documentation/speech/sfspeechrecognitiontaskstate/canceling)
- [case completed](/documentation/speech/sfspeechrecognitiontaskstate/completed)
- [case finishing](/documentation/speech/sfspeechrecognitiontaskstate/finishing)
- [case running](/documentation/speech/sfspeechrecognitiontaskstate/running)
- [case starting](/documentation/speech/sfspeechrecognitiontaskstate/starting)

##### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeechrecognitiontaskstate/init(rawvalue:))
- [var error: (any Error)?](/documentation/speech/sfspeechrecognitiontask/error)
- [SFSpeechRecognitionTaskDelegate](/documentation/speech/sfspeechrecognitiontaskdelegate)

#### Tracking task progress

- [func speechRecognitionDidDetectSpeech(SFSpeechRecognitionTask)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiondiddetectspeech(_:))
- [func speechRecognitionTaskFinishedReadingAudio(SFSpeechRecognitionTask)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontaskfinishedreadingaudio(_:))

#### Getting transcriptions

- [func speechRecognitionTask(SFSpeechRecognitionTask, didHypothesizeTranscription: SFTranscription)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didhypothesizetranscription:))

#### Finishing a speech recognition task

- [func speechRecognitionTask(SFSpeechRecognitionTask, didFinishRecognition: SFSpeechRecognitionResult)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didfinishrecognition:))
- [func speechRecognitionTask(SFSpeechRecognitionTask, didFinishSuccessfully: Bool)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didfinishsuccessfully:))
- [func speechRecognitionTask(SFSpeechRecognitionTask, didProcessAudioDuration: TimeInterval)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontask(_:didprocessaudioduration:))
- [func speechRecognitionTaskWasCancelled(SFSpeechRecognitionTask)](/documentation/speech/sfspeechrecognitiontaskdelegate/speechrecognitiontaskwascancelled(_:))
- [SFSpeechRecognitionTaskState](/documentation/speech/sfspeechrecognitiontaskstate)

#### Task states

- [case canceling](/documentation/speech/sfspeechrecognitiontaskstate/canceling)
- [case completed](/documentation/speech/sfspeechrecognitiontaskstate/completed)
- [case finishing](/documentation/speech/sfspeechrecognitiontaskstate/finishing)
- [case running](/documentation/speech/sfspeechrecognitiontaskstate/running)
- [case starting](/documentation/speech/sfspeechrecognitiontaskstate/starting)

#### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeechrecognitiontaskstate/init(rawvalue:))

### Transcription results

- [SFSpeechRecognitionResult](/documentation/speech/sfspeechrecognitionresult)

#### Getting transcriptions

- [var bestTranscription: SFTranscription](/documentation/speech/sfspeechrecognitionresult/besttranscription)
- [var transcriptions: [SFTranscription]](/documentation/speech/sfspeechrecognitionresult/transcriptions)
- [var speechRecognitionMetadata: SFSpeechRecognitionMetadata?](/documentation/speech/sfspeechrecognitionresult/speechrecognitionmetadata)

#### Determining whether transcriptions are final

- [var isFinal: Bool](/documentation/speech/sfspeechrecognitionresult/isfinal)
- [SFSpeechRecognitionMetadata](/documentation/speech/sfspeechrecognitionmetadata)

#### Getting audio timing information

- [var averagePauseDuration: TimeInterval](/documentation/speech/sfspeechrecognitionmetadata/averagepauseduration)
- [var speakingRate: Double](/documentation/speech/sfspeechrecognitionmetadata/speakingrate)
- [var speechDuration: TimeInterval](/documentation/speech/sfspeechrecognitionmetadata/speechduration)
- [var speechStartTimestamp: TimeInterval](/documentation/speech/sfspeechrecognitionmetadata/speechstarttimestamp)

#### Analyzing voice

- [var voiceAnalytics: SFVoiceAnalytics?](/documentation/speech/sfspeechrecognitionmetadata/voiceanalytics)
- [SFTranscription](/documentation/speech/sftranscription)

#### Transcribing utterances

- [var formattedString: String](/documentation/speech/sftranscription/formattedstring)

#### Getting individual utterances

- [var segments: [SFTranscriptionSegment]](/documentation/speech/sftranscription/segments)

#### Deprecated

- [var averagePauseDuration: TimeInterval](/documentation/speech/sftranscription/averagepauseduration)
- [var speakingRate: Double](/documentation/speech/sftranscription/speakingrate)
- [SFTranscriptionSegment](/documentation/speech/sftranscriptionsegment)

#### Transcribing the segment

- [var substring: String](/documentation/speech/sftranscriptionsegment/substring)
- [var substringRange: NSRange](/documentation/speech/sftranscriptionsegment/substringrange)
- [var alternativeSubstrings: [String]](/documentation/speech/sftranscriptionsegment/alternativesubstrings)

#### Assessing the recognition confidence level

- [var confidence: Float](/documentation/speech/sftranscriptionsegment/confidence)

#### Getting audio timing information

- [var timestamp: TimeInterval](/documentation/speech/sftranscriptionsegment/timestamp)
- [var duration: TimeInterval](/documentation/speech/sftranscriptionsegment/duration)

#### Deprecated

- [var voiceAnalytics: SFVoiceAnalytics?](/documentation/speech/sftranscriptionsegment/voiceanalytics)

### Voice analytics

- [SFVoiceAnalytics](/documentation/speech/sfvoiceanalytics)

#### Analyzing voice

- [SFAcousticFeature](/documentation/speech/sfacousticfeature)

##### Inspecting a feature

- [var frameDuration: TimeInterval](/documentation/speech/sfacousticfeature/frameduration)
- [var acousticFeatureValuePerFrame: [Double]](/documentation/speech/sfacousticfeature/acousticfeaturevalueperframe-5krkk)
- [var voicing: SFAcousticFeature](/documentation/speech/sfvoiceanalytics/voicing)
- [var pitch: SFAcousticFeature](/documentation/speech/sfvoiceanalytics/pitch)
- [var jitter: SFAcousticFeature](/documentation/speech/sfvoiceanalytics/jitter)
- [var shimmer: SFAcousticFeature](/documentation/speech/sfvoiceanalytics/shimmer)
- [SFAcousticFeature](/documentation/speech/sfacousticfeature)

#### Inspecting a feature

- [var frameDuration: TimeInterval](/documentation/speech/sfacousticfeature/frameduration)
- [var acousticFeatureValuePerFrame: [Double]](/documentation/speech/sfacousticfeature/acousticfeaturevalueperframe-5krkk)

### Errors

- [let SFSpeechErrorDomain: String](/documentation/speech/sfspeecherrordomain)
- [SFSpeechError](/documentation/speech/sfspeecherror)

#### Error domain

- [static var errorDomain: String](/documentation/speech/sfspeecherror/errordomain)

#### Error codes

- [SFSpeechError.Code](/documentation/speech/sfspeecherror/code)

##### Audio input errors

- [static var audioDisordered: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/audiodisordered)
- [case audioReadFailed](/documentation/speech/sfspeecherror/code/audioreadfailed)

##### Audio format errors

- [static var incompatibleAudioFormats: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/incompatibleaudioformats)
- [static var unexpectedAudioFormat: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/unexpectedaudioformat)

##### Asset errors

- [static var assetLocaleNotAllocated: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/assetlocalenotallocated)
- [static var cannotAllocateUnsupportedLocale: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/cannotallocateunsupportedlocale)
- [static var noModel: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/nomodel)
- [case timeout](/documentation/speech/sfspeecherror/code/timeout)
- [static var tooManyAssetLocalesAllocated: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/toomanyassetlocalesallocated)

##### Custom language model errors

- [case malformedSupplementalModel](/documentation/speech/sfspeecherror/code/malformedsupplementalmodel)
- [case missingParameter](/documentation/speech/sfspeecherror/code/missingparameter)
- [case undefinedTemplateClassName](/documentation/speech/sfspeecherror/code/undefinedtemplateclassname)

##### Other errors

- [static var insufficientResources: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/insufficientresources)
- [case internalServiceError](/documentation/speech/sfspeecherror/code/internalserviceerror)
- [static var moduleOutputFailed: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/moduleoutputfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeecherror/code/init(rawvalue:))

#### Aliased error codes

- [static var audioReadFailed: SFSpeechError.Code](/documentation/speech/sfspeecherror/audioreadfailed)
- [static var internalServiceError: SFSpeechError.Code](/documentation/speech/sfspeecherror/internalserviceerror)
- [static var malformedSupplementalModel: SFSpeechError.Code](/documentation/speech/sfspeecherror/malformedsupplementalmodel)
- [static var missingParameter: SFSpeechError.Code](/documentation/speech/sfspeecherror/missingparameter)
- [static var timeout: SFSpeechError.Code](/documentation/speech/sfspeecherror/timeout)
- [static var undefinedTemplateClassName: SFSpeechError.Code](/documentation/speech/sfspeecherror/undefinedtemplateclassname)
- [SFSpeechError.Code](/documentation/speech/sfspeecherror/code)

#### Audio input errors

- [static var audioDisordered: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/audiodisordered)
- [case audioReadFailed](/documentation/speech/sfspeecherror/code/audioreadfailed)

#### Audio format errors

- [static var incompatibleAudioFormats: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/incompatibleaudioformats)
- [static var unexpectedAudioFormat: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/unexpectedaudioformat)

#### Asset errors

- [static var assetLocaleNotAllocated: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/assetlocalenotallocated)
- [static var cannotAllocateUnsupportedLocale: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/cannotallocateunsupportedlocale)
- [static var noModel: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/nomodel)
- [case timeout](/documentation/speech/sfspeecherror/code/timeout)
- [static var tooManyAssetLocalesAllocated: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/toomanyassetlocalesallocated)

#### Custom language model errors

- [case malformedSupplementalModel](/documentation/speech/sfspeecherror/code/malformedsupplementalmodel)
- [case missingParameter](/documentation/speech/sfspeecherror/code/missingparameter)
- [case undefinedTemplateClassName](/documentation/speech/sfspeecherror/code/undefinedtemplateclassname)

#### Other errors

- [static var insufficientResources: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/insufficientresources)
- [case internalServiceError](/documentation/speech/sfspeecherror/code/internalserviceerror)
- [static var moduleOutputFailed: SFSpeechError.Code](/documentation/speech/sfspeecherror/code/moduleoutputfailed)

#### Initializers

- [init?(rawValue: Int)](/documentation/speech/sfspeecherror/code/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
