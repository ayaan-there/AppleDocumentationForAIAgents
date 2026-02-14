# Natural Language Documentation

Source: https://sosumi.ai/documentation/naturallanguage

---
title: Natural Language
source: https://developer.apple.com/documentation/naturallanguage
timestamp: 2026-02-13T19:23:50.327Z
---

## Tokenization

- [Tokenizing natural language text](/documentation/naturallanguage/tokenizing-natural-language-text)
- [NLTokenizer](/documentation/naturallanguage/nltokenizer)

### Creating a tokenizer

- [init(unit: NLTokenUnit)](/documentation/naturallanguage/nltokenizer/init(unit:))

### Configuring a tokenizer

- [var string: String?](/documentation/naturallanguage/nltokenizer/string)
- [func setLanguage(NLLanguage)](/documentation/naturallanguage/nltokenizer/setlanguage(_:))
- [var unit: NLTokenUnit](/documentation/naturallanguage/nltokenizer/unit)
- [NLTokenizer.Attributes](/documentation/naturallanguage/nltokenizer/attributes)

#### Contents

- [static var emoji: NLTokenizer.Attributes](/documentation/naturallanguage/nltokenizer/attributes/emoji)
- [static var numeric: NLTokenizer.Attributes](/documentation/naturallanguage/nltokenizer/attributes/numeric)
- [static var symbolic: NLTokenizer.Attributes](/documentation/naturallanguage/nltokenizer/attributes/symbolic)

#### Initializers

- [init(rawValue: UInt)](/documentation/naturallanguage/nltokenizer/attributes/init(rawvalue:))

### Enumerating the tokens

- [func enumerateTokens(in: Range<String.Index>, using: (Range<String.Index>, NLTokenizer.Attributes) -> Bool)](/documentation/naturallanguage/nltokenizer/enumeratetokens(in:using:))
- [func tokens(for: Range<String.Index>) -> [Range<String.Index>]](/documentation/naturallanguage/nltokenizer/tokens(for:))
- [func tokenRange(at: String.Index) -> Range<String.Index>](/documentation/naturallanguage/nltokenizer/tokenrange(at:))
- [func tokenRange(for: Range<String.Index>) -> Range<String.Index>](/documentation/naturallanguage/nltokenizer/tokenrange(for:))

## Language identification

- [Identifying the language in text](/documentation/naturallanguage/identifying-the-language-in-text)
- [NLLanguageRecognizer](/documentation/naturallanguage/nllanguagerecognizer)

### Creating a recognizer

- [init()](/documentation/naturallanguage/nllanguagerecognizer/init())

### Determining the language

- [class func dominantLanguage(for: String) -> NLLanguage?](/documentation/naturallanguage/nllanguagerecognizer/dominantlanguage(for:))
- [func processString(String)](/documentation/naturallanguage/nllanguagerecognizer/processstring(_:))
- [var dominantLanguage: NLLanguage?](/documentation/naturallanguage/nllanguagerecognizer/dominantlanguage)
- [func languageHypotheses(withMaximum: Int) -> [NLLanguage : Double]](/documentation/naturallanguage/nllanguagerecognizer/languagehypotheses(withmaximum:))
- [func reset()](/documentation/naturallanguage/nllanguagerecognizer/reset())

### Guiding the recognizer

- [var languageHints: [NLLanguage : Double]](/documentation/naturallanguage/nllanguagerecognizer/languagehints-7dwgv)
- [var languageConstraints: [NLLanguage]](/documentation/naturallanguage/nllanguagerecognizer/languageconstraints)
- [NLLanguage](/documentation/naturallanguage/nllanguage)

### Getting standard languages

- [static let amharic: NLLanguage](/documentation/naturallanguage/nllanguage/amharic)
- [static let arabic: NLLanguage](/documentation/naturallanguage/nllanguage/arabic)
- [static let armenian: NLLanguage](/documentation/naturallanguage/nllanguage/armenian)
- [static let bengali: NLLanguage](/documentation/naturallanguage/nllanguage/bengali)
- [static let bulgarian: NLLanguage](/documentation/naturallanguage/nllanguage/bulgarian)
- [static let burmese: NLLanguage](/documentation/naturallanguage/nllanguage/burmese)
- [static let catalan: NLLanguage](/documentation/naturallanguage/nllanguage/catalan)
- [static let cherokee: NLLanguage](/documentation/naturallanguage/nllanguage/cherokee)
- [static let croatian: NLLanguage](/documentation/naturallanguage/nllanguage/croatian)
- [static let czech: NLLanguage](/documentation/naturallanguage/nllanguage/czech)
- [static let danish: NLLanguage](/documentation/naturallanguage/nllanguage/danish)
- [static let dutch: NLLanguage](/documentation/naturallanguage/nllanguage/dutch)
- [static let english: NLLanguage](/documentation/naturallanguage/nllanguage/english)
- [static let finnish: NLLanguage](/documentation/naturallanguage/nllanguage/finnish)
- [static let french: NLLanguage](/documentation/naturallanguage/nllanguage/french)
- [static let georgian: NLLanguage](/documentation/naturallanguage/nllanguage/georgian)
- [static let german: NLLanguage](/documentation/naturallanguage/nllanguage/german)
- [static let greek: NLLanguage](/documentation/naturallanguage/nllanguage/greek)
- [static let gujarati: NLLanguage](/documentation/naturallanguage/nllanguage/gujarati)
- [static let hebrew: NLLanguage](/documentation/naturallanguage/nllanguage/hebrew)
- [static let hindi: NLLanguage](/documentation/naturallanguage/nllanguage/hindi)
- [static let hungarian: NLLanguage](/documentation/naturallanguage/nllanguage/hungarian)
- [static let icelandic: NLLanguage](/documentation/naturallanguage/nllanguage/icelandic)
- [static let indonesian: NLLanguage](/documentation/naturallanguage/nllanguage/indonesian)
- [static let italian: NLLanguage](/documentation/naturallanguage/nllanguage/italian)
- [static let japanese: NLLanguage](/documentation/naturallanguage/nllanguage/japanese)
- [static let kannada: NLLanguage](/documentation/naturallanguage/nllanguage/kannada)
- [static let kazakh: NLLanguage](/documentation/naturallanguage/nllanguage/kazakh)
- [static let khmer: NLLanguage](/documentation/naturallanguage/nllanguage/khmer)
- [static let korean: NLLanguage](/documentation/naturallanguage/nllanguage/korean)
- [static let lao: NLLanguage](/documentation/naturallanguage/nllanguage/lao)
- [static let malay: NLLanguage](/documentation/naturallanguage/nllanguage/malay)
- [static let malayalam: NLLanguage](/documentation/naturallanguage/nllanguage/malayalam)
- [static let marathi: NLLanguage](/documentation/naturallanguage/nllanguage/marathi)
- [static let mongolian: NLLanguage](/documentation/naturallanguage/nllanguage/mongolian)
- [static let norwegian: NLLanguage](/documentation/naturallanguage/nllanguage/norwegian)
- [static let oriya: NLLanguage](/documentation/naturallanguage/nllanguage/oriya)
- [static let persian: NLLanguage](/documentation/naturallanguage/nllanguage/persian)
- [static let polish: NLLanguage](/documentation/naturallanguage/nllanguage/polish)
- [static let portuguese: NLLanguage](/documentation/naturallanguage/nllanguage/portuguese)
- [static let punjabi: NLLanguage](/documentation/naturallanguage/nllanguage/punjabi)
- [static let romanian: NLLanguage](/documentation/naturallanguage/nllanguage/romanian)
- [static let russian: NLLanguage](/documentation/naturallanguage/nllanguage/russian)
- [static let simplifiedChinese: NLLanguage](/documentation/naturallanguage/nllanguage/simplifiedchinese)
- [static let sinhalese: NLLanguage](/documentation/naturallanguage/nllanguage/sinhalese)
- [static let slovak: NLLanguage](/documentation/naturallanguage/nllanguage/slovak)
- [static let spanish: NLLanguage](/documentation/naturallanguage/nllanguage/spanish)
- [static let swedish: NLLanguage](/documentation/naturallanguage/nllanguage/swedish)
- [static let tamil: NLLanguage](/documentation/naturallanguage/nllanguage/tamil)
- [static let telugu: NLLanguage](/documentation/naturallanguage/nllanguage/telugu)
- [static let thai: NLLanguage](/documentation/naturallanguage/nllanguage/thai)
- [static let tibetan: NLLanguage](/documentation/naturallanguage/nllanguage/tibetan)
- [static let traditionalChinese: NLLanguage](/documentation/naturallanguage/nllanguage/traditionalchinese)
- [static let turkish: NLLanguage](/documentation/naturallanguage/nllanguage/turkish)
- [static let ukrainian: NLLanguage](/documentation/naturallanguage/nllanguage/ukrainian)
- [static let urdu: NLLanguage](/documentation/naturallanguage/nllanguage/urdu)
- [static let vietnamese: NLLanguage](/documentation/naturallanguage/nllanguage/vietnamese)
- [static let undetermined: NLLanguage](/documentation/naturallanguage/nllanguage/undetermined)

### Creating custom language tags

- [init(String)](/documentation/naturallanguage/nllanguage/init(_:))
- [init(rawValue: String)](/documentation/naturallanguage/nllanguage/init(rawvalue:))

## Linguistic tags

- [Identifying parts of speech](/documentation/naturallanguage/identifying-parts-of-speech)
- [Identifying people, places, and organizations](/documentation/naturallanguage/identifying-people-places-and-organizations)
- [NLTagger](/documentation/naturallanguage/nltagger)

### Creating a tagger

- [init(tagSchemes: [NLTagScheme])](/documentation/naturallanguage/nltagger/init(tagschemes:))
- [var string: String?](/documentation/naturallanguage/nltagger/string)

### Getting the tag schemes

- [class func availableTagSchemes(for: NLTokenUnit, language: NLLanguage) -> [NLTagScheme]](/documentation/naturallanguage/nltagger/availabletagschemes(for:language:))
- [class func requestAssets(for: NLLanguage, tagScheme: NLTagScheme, completionHandler: (NLTagger.AssetsResult, (any Error)?) -> Void)](/documentation/naturallanguage/nltagger/requestassets(for:tagscheme:completionhandler:))
- [NLTagger.AssetsResult](/documentation/naturallanguage/nltagger/assetsresult)

#### Asset request responses

- [case available](/documentation/naturallanguage/nltagger/assetsresult/available)
- [case notAvailable](/documentation/naturallanguage/nltagger/assetsresult/notavailable)
- [case error](/documentation/naturallanguage/nltagger/assetsresult/error)

#### Initializers

- [init?(rawValue: Int)](/documentation/naturallanguage/nltagger/assetsresult/init(rawvalue:))
- [var tagSchemes: [NLTagScheme]](/documentation/naturallanguage/nltagger/tagschemes)
- [NLTagScheme](/documentation/naturallanguage/nltagscheme)

#### Schemes

- [static let tokenType: NLTagScheme](/documentation/naturallanguage/nltagscheme/tokentype)
- [static let lexicalClass: NLTagScheme](/documentation/naturallanguage/nltagscheme/lexicalclass)
- [static let nameType: NLTagScheme](/documentation/naturallanguage/nltagscheme/nametype)
- [static let nameTypeOrLexicalClass: NLTagScheme](/documentation/naturallanguage/nltagscheme/nametypeorlexicalclass)
- [static let lemma: NLTagScheme](/documentation/naturallanguage/nltagscheme/lemma)
- [static let language: NLTagScheme](/documentation/naturallanguage/nltagscheme/language)
- [static let script: NLTagScheme](/documentation/naturallanguage/nltagscheme/script)
- [static let sentimentScore: NLTagScheme](/documentation/naturallanguage/nltagscheme/sentimentscore)

#### Initializers

- [init(String)](/documentation/naturallanguage/nltagscheme/init(_:))
- [init(rawValue: String)](/documentation/naturallanguage/nltagscheme/init(rawvalue:))

### Determining the dominant language and orthography

- [var dominantLanguage: NLLanguage?](/documentation/naturallanguage/nltagger/dominantlanguage)
- [func setLanguage(NLLanguage, range: Range<String.Index>)](/documentation/naturallanguage/nltagger/setlanguage(_:range:))
- [func setOrthography(NSOrthography, range: Range<String.Index>)](/documentation/naturallanguage/nltagger/setorthography(_:range:))

### Enumerating linguistic tags

- [func enumerateTags(in: Range<String.Index>, unit: NLTokenUnit, scheme: NLTagScheme, options: NLTagger.Options, using: (NLTag?, Range<String.Index>) -> Bool)](/documentation/naturallanguage/nltagger/enumeratetags(in:unit:scheme:options:using:))
- [NLTagger.Options](/documentation/naturallanguage/nltagger/options)

#### Constants

- [static var omitWords: NLTagger.Options](/documentation/naturallanguage/nltagger/options/omitwords)
- [static var omitPunctuation: NLTagger.Options](/documentation/naturallanguage/nltagger/options/omitpunctuation)
- [static var omitWhitespace: NLTagger.Options](/documentation/naturallanguage/nltagger/options/omitwhitespace)
- [static var omitOther: NLTagger.Options](/documentation/naturallanguage/nltagger/options/omitother)
- [static var joinNames: NLTagger.Options](/documentation/naturallanguage/nltagger/options/joinnames)
- [static var joinContractions: NLTagger.Options](/documentation/naturallanguage/nltagger/options/joincontractions)

#### Initializers

- [init(rawValue: UInt)](/documentation/naturallanguage/nltagger/options/init(rawvalue:))
- [NLTag](/documentation/naturallanguage/nltag)

#### Token types

- [static let word: NLTag](/documentation/naturallanguage/nltag/word)
- [static let punctuation: NLTag](/documentation/naturallanguage/nltag/punctuation)
- [static let whitespace: NLTag](/documentation/naturallanguage/nltag/whitespace)
- [static let other: NLTag](/documentation/naturallanguage/nltag/other)

#### Lexical classes

- [static let noun: NLTag](/documentation/naturallanguage/nltag/noun)
- [static let verb: NLTag](/documentation/naturallanguage/nltag/verb)
- [static let adjective: NLTag](/documentation/naturallanguage/nltag/adjective)
- [static let adverb: NLTag](/documentation/naturallanguage/nltag/adverb)
- [static let pronoun: NLTag](/documentation/naturallanguage/nltag/pronoun)
- [static let determiner: NLTag](/documentation/naturallanguage/nltag/determiner)
- [static let particle: NLTag](/documentation/naturallanguage/nltag/particle)
- [static let preposition: NLTag](/documentation/naturallanguage/nltag/preposition)
- [static let number: NLTag](/documentation/naturallanguage/nltag/number)
- [static let conjunction: NLTag](/documentation/naturallanguage/nltag/conjunction)
- [static let interjection: NLTag](/documentation/naturallanguage/nltag/interjection)
- [static let classifier: NLTag](/documentation/naturallanguage/nltag/classifier)
- [static let idiom: NLTag](/documentation/naturallanguage/nltag/idiom)
- [static let otherWord: NLTag](/documentation/naturallanguage/nltag/otherword)
- [static let sentenceTerminator: NLTag](/documentation/naturallanguage/nltag/sentenceterminator)
- [static let openQuote: NLTag](/documentation/naturallanguage/nltag/openquote)
- [static let closeQuote: NLTag](/documentation/naturallanguage/nltag/closequote)
- [static let openParenthesis: NLTag](/documentation/naturallanguage/nltag/openparenthesis)
- [static let closeParenthesis: NLTag](/documentation/naturallanguage/nltag/closeparenthesis)
- [static let wordJoiner: NLTag](/documentation/naturallanguage/nltag/wordjoiner)
- [static let dash: NLTag](/documentation/naturallanguage/nltag/dash)
- [static let otherPunctuation: NLTag](/documentation/naturallanguage/nltag/otherpunctuation)
- [static let paragraphBreak: NLTag](/documentation/naturallanguage/nltag/paragraphbreak)
- [static let otherWhitespace: NLTag](/documentation/naturallanguage/nltag/otherwhitespace)

#### Name types

- [static let personalName: NLTag](/documentation/naturallanguage/nltag/personalname)
- [static let organizationName: NLTag](/documentation/naturallanguage/nltag/organizationname)
- [static let placeName: NLTag](/documentation/naturallanguage/nltag/placename)

#### Initializers

- [init(String)](/documentation/naturallanguage/nltag/init(_:))
- [init(rawValue: String)](/documentation/naturallanguage/nltag/init(rawvalue:))

### Getting linguistic tags

- [func tags(in: Range<String.Index>, unit: NLTokenUnit, scheme: NLTagScheme, options: NLTagger.Options) -> [(NLTag?, Range<String.Index>)]](/documentation/naturallanguage/nltagger/tags(in:unit:scheme:options:))
- [func tag(at: String.Index, unit: NLTokenUnit, scheme: NLTagScheme) -> (NLTag?, Range<String.Index>)](/documentation/naturallanguage/nltagger/tag(at:unit:scheme:))
- [func tagHypotheses(at: String.Index, unit: NLTokenUnit, scheme: NLTagScheme, maximumCount: Int) -> ([String : Double], Range<String.Index>)](/documentation/naturallanguage/nltagger/taghypotheses(at:unit:scheme:maximumcount:))

### Determining the range of a unit token

- [func tokenRange(at: String.Index, unit: NLTokenUnit) -> Range<String.Index>](/documentation/naturallanguage/nltagger/tokenrange(at:unit:))
- [func tokenRange(for: Range<String.Index>, unit: NLTokenUnit) -> Range<String.Index>](/documentation/naturallanguage/nltagger/tokenrange(for:unit:))
- [NLTokenUnit](/documentation/naturallanguage/nltokenunit)

#### Constants

- [case word](/documentation/naturallanguage/nltokenunit/word)
- [case sentence](/documentation/naturallanguage/nltokenunit/sentence)
- [case paragraph](/documentation/naturallanguage/nltokenunit/paragraph)
- [case document](/documentation/naturallanguage/nltokenunit/document)

#### Initializers

- [init?(rawValue: Int)](/documentation/naturallanguage/nltokenunit/init(rawvalue:))

### Using models with a tagger

- [func setModels([NLModel], forTagScheme: NLTagScheme)](/documentation/naturallanguage/nltagger/setmodels(_:fortagscheme:))
- [func models(forTagScheme: NLTagScheme) -> [NLModel]](/documentation/naturallanguage/nltagger/models(fortagscheme:))

### Using gazetteers with a tagger

- [func setGazetteers([NLGazetteer], for: NLTagScheme)](/documentation/naturallanguage/nltagger/setgazetteers(_:for:))
- [func gazetteers(for: NLTagScheme) -> [NLGazetteer]](/documentation/naturallanguage/nltagger/gazetteers(for:))
- [NLGazetteer](/documentation/naturallanguage/nlgazetteer)

#### Creating a Gazetteer

- [init(contentsOf: URL) throws](/documentation/naturallanguage/nlgazetteer/init(contentsof:))
- [init(data: Data) throws](/documentation/naturallanguage/nlgazetteer/init(data:))
- [init(dictionary: [String : [String]], language: NLLanguage?) throws](/documentation/naturallanguage/nlgazetteer/init(dictionary:language:))
- [class func write([String : [String]], language: NLLanguage?, to: URL) throws](/documentation/naturallanguage/nlgazetteer/write(_:language:to:))

#### Looking Up Labels for Terms

- [func label(for: String) -> String?](/documentation/naturallanguage/nlgazetteer/label(for:))

#### Inspecting a Gazetteer

- [var data: Data](/documentation/naturallanguage/nlgazetteer/data)
- [var language: NLLanguage?](/documentation/naturallanguage/nlgazetteer/language)

## Text embedding

- [Finding similarities between pieces of text](/documentation/naturallanguage/finding-similarities-between-pieces-of-text)
- [NLEmbedding](/documentation/naturallanguage/nlembedding)

### Creating a word embedding

- [class func wordEmbedding(for: NLLanguage) -> NLEmbedding?](/documentation/naturallanguage/nlembedding/wordembedding(for:))
- [class func wordEmbedding(for: NLLanguage, revision: Int) -> NLEmbedding?](/documentation/naturallanguage/nlembedding/wordembedding(for:revision:))
- [convenience init(contentsOf: URL) throws](/documentation/naturallanguage/nlembedding/init(contentsof:))

### Creating a sentence embedding

- [class func sentenceEmbedding(for: NLLanguage) -> NLEmbedding?](/documentation/naturallanguage/nlembedding/sentenceembedding(for:))
- [class func sentenceEmbedding(for: NLLanguage, revision: Int) -> NLEmbedding?](/documentation/naturallanguage/nlembedding/sentenceembedding(for:revision:))

### Finding strings and their distances in an embedding

- [func neighbors(for: String, maximumCount: Int, distanceType: NLDistanceType) -> [(String, NLDistance)]](/documentation/naturallanguage/nlembedding/neighbors(for:maximumcount:distancetype:)-8f1jc)
- [func neighbors(for: [Double], maximumCount: Int, distanceType: NLDistanceType) -> [(String, NLDistance)]](/documentation/naturallanguage/nlembedding/neighbors(for:maximumcount:distancetype:)-8lp4z)
- [func enumerateNeighbors(for: String, maximumCount: Int, distanceType: NLDistanceType, using: (String, NLDistance) -> Bool)](/documentation/naturallanguage/nlembedding/enumerateneighbors(for:maximumcount:distancetype:using:)-72jda)
- [func enumerateNeighbors(for: [Double], maximumCount: Int, distanceType: NLDistanceType, using: (String, NLDistance) -> Bool)](/documentation/naturallanguage/nlembedding/enumerateneighbors(for:maximumcount:distancetype:using:)-6dy4x)
- [func distance(between: String, and: String, distanceType: NLDistanceType) -> NLDistance](/documentation/naturallanguage/nlembedding/distance(between:and:distancetype:))
- [NLDistance](/documentation/naturallanguage/nldistance)

#### Calculating Distance

- [NLDistanceType](/documentation/naturallanguage/nldistancetype)

##### Distance Types

- [case cosine](/documentation/naturallanguage/nldistancetype/cosine)

##### Initializers

- [init?(rawValue: Int)](/documentation/naturallanguage/nldistancetype/init(rawvalue:))

### Inspecting the vocabulary of an embedding

- [var dimension: Int](/documentation/naturallanguage/nlembedding/dimension)
- [var vocabularySize: Int](/documentation/naturallanguage/nlembedding/vocabularysize)
- [var language: NLLanguage?](/documentation/naturallanguage/nlembedding/language)
- [func contains(String) -> Bool](/documentation/naturallanguage/nlembedding/contains(_:))
- [func vector(for: String) -> [Double]?](/documentation/naturallanguage/nlembedding/vector(for:))
- [var revision: Int](/documentation/naturallanguage/nlembedding/revision)

### Saving an embedding

- [class func write([String : [Double]], language: NLLanguage?, revision: Int, to: URL) throws](/documentation/naturallanguage/nlembedding/write(_:language:revision:to:))

### Checking for Natural Language support

- [class func currentRevision(for: NLLanguage) -> Int](/documentation/naturallanguage/nlembedding/currentrevision(for:))
- [class func supportedRevisions(for: NLLanguage) -> IndexSet](/documentation/naturallanguage/nlembedding/supportedrevisions(for:))
- [class func currentSentenceEmbeddingRevision(for: NLLanguage) -> Int](/documentation/naturallanguage/nlembedding/currentsentenceembeddingrevision(for:))
- [class func supportedSentenceEmbeddingRevisions(for: NLLanguage) -> IndexSet](/documentation/naturallanguage/nlembedding/supportedsentenceembeddingrevisions(for:))

## Contextual embedding

- [NLContextualEmbedding](/documentation/naturallanguage/nlcontextualembedding)

### Creating a contextual embedding

- [convenience init?(modelIdentifier: String)](/documentation/naturallanguage/nlcontextualembedding/init(modelidentifier:))
- [init?(language: NLLanguage)](/documentation/naturallanguage/nlcontextualembedding/init(language:))
- [init?(script: NLScript)](/documentation/naturallanguage/nlcontextualembedding/init(script:))

### Inspecting the contextual embedding

- [var dimension: Int](/documentation/naturallanguage/nlcontextualembedding/dimension)
- [var hasAvailableAssets: Bool](/documentation/naturallanguage/nlcontextualembedding/hasavailableassets)
- [var languages: [NLLanguage]](/documentation/naturallanguage/nlcontextualembedding/languages)
- [var maximumSequenceLength: Int](/documentation/naturallanguage/nlcontextualembedding/maximumsequencelength)
- [var modelIdentifier: String](/documentation/naturallanguage/nlcontextualembedding/modelidentifier)
- [var revision: Int](/documentation/naturallanguage/nlcontextualembedding/revision)
- [var scripts: [NLScript]](/documentation/naturallanguage/nlcontextualembedding/scripts)

### Requesting assets

- [func requestAssets(completionHandler: (NLContextualEmbedding.AssetsResult, (any Error)?) -> Void)](/documentation/naturallanguage/nlcontextualembedding/requestassets(completionhandler:))
- [NLContextualEmbedding.AssetsResult](/documentation/naturallanguage/nlcontextualembedding/assetsresult)

#### Getting the result status

- [case available](/documentation/naturallanguage/nlcontextualembedding/assetsresult/available)
- [case notAvailable](/documentation/naturallanguage/nlcontextualembedding/assetsresult/notavailable)
- [case error](/documentation/naturallanguage/nlcontextualembedding/assetsresult/error)

#### Initializers

- [init?(rawValue: Int)](/documentation/naturallanguage/nlcontextualembedding/assetsresult/init(rawvalue:))

### Loading and unloading assets

- [func load() throws](/documentation/naturallanguage/nlcontextualembedding/load())
- [func unload()](/documentation/naturallanguage/nlcontextualembedding/unload())

### Applying an embedding

- [func embeddingResult(for: String, language: NLLanguage?) throws -> NLContextualEmbeddingResult](/documentation/naturallanguage/nlcontextualembedding/embeddingresult(for:language:))
- [NLContextualEmbeddingResult](/documentation/naturallanguage/nlcontextualembeddingresult)

#### Inspecting the result

- [var language: NLLanguage](/documentation/naturallanguage/nlcontextualembeddingresult/language)
- [var sequenceLength: Int](/documentation/naturallanguage/nlcontextualembeddingresult/sequencelength)
- [var string: String](/documentation/naturallanguage/nlcontextualembeddingresult/string)

#### Enumerating the vectors

- [func enumerateTokenVectors(in: Range<String.Index>, using: ([Double], Range<String.Index>) -> Bool)](/documentation/naturallanguage/nlcontextualembeddingresult/enumeratetokenvectors(in:using:))
- [func tokenVector(at: String.Index) -> ([Double], Range<String.Index>)?](/documentation/naturallanguage/nlcontextualembeddingresult/tokenvector(at:))

### Type Methods

- [class func contextualEmbeddings(forValues: [NLContextualEmbeddingKey : Any]) -> [NLContextualEmbedding]](/documentation/naturallanguage/nlcontextualembedding/contextualembeddings(forvalues:))
- [NLContextualEmbeddingKey](/documentation/naturallanguage/nlcontextualembeddingkey)

### Getting embedding keys

- [static let languages: NLContextualEmbeddingKey](/documentation/naturallanguage/nlcontextualembeddingkey/languages)
- [static let revision: NLContextualEmbeddingKey](/documentation/naturallanguage/nlcontextualembeddingkey/revision)
- [static let scripts: NLContextualEmbeddingKey](/documentation/naturallanguage/nlcontextualembeddingkey/scripts)

### Creating embedding keys

- [init(String)](/documentation/naturallanguage/nlcontextualembeddingkey/init(_:))
- [init(rawValue: String)](/documentation/naturallanguage/nlcontextualembeddingkey/init(rawvalue:))
- [NLScript](/documentation/naturallanguage/nlscript)

### Getting standard scripts

- [static let arabic: NLScript](/documentation/naturallanguage/nlscript/arabic)
- [static let armenian: NLScript](/documentation/naturallanguage/nlscript/armenian)
- [static let bengali: NLScript](/documentation/naturallanguage/nlscript/bengali)
- [static let canadianAboriginalSyllabics: NLScript](/documentation/naturallanguage/nlscript/canadianaboriginalsyllabics)
- [static let cherokee: NLScript](/documentation/naturallanguage/nlscript/cherokee)
- [static let cyrillic: NLScript](/documentation/naturallanguage/nlscript/cyrillic)
- [static let devanagari: NLScript](/documentation/naturallanguage/nlscript/devanagari)
- [static let ethiopic: NLScript](/documentation/naturallanguage/nlscript/ethiopic)
- [static let georgian: NLScript](/documentation/naturallanguage/nlscript/georgian)
- [static let greek: NLScript](/documentation/naturallanguage/nlscript/greek)
- [static let gujarati: NLScript](/documentation/naturallanguage/nlscript/gujarati)
- [static let gurmukhi: NLScript](/documentation/naturallanguage/nlscript/gurmukhi)
- [static let hebrew: NLScript](/documentation/naturallanguage/nlscript/hebrew)
- [static let japanese: NLScript](/documentation/naturallanguage/nlscript/japanese)
- [static let kannada: NLScript](/documentation/naturallanguage/nlscript/kannada)
- [static let khmer: NLScript](/documentation/naturallanguage/nlscript/khmer)
- [static let korean: NLScript](/documentation/naturallanguage/nlscript/korean)
- [static let lao: NLScript](/documentation/naturallanguage/nlscript/lao)
- [static let latin: NLScript](/documentation/naturallanguage/nlscript/latin)
- [static let malayalam: NLScript](/documentation/naturallanguage/nlscript/malayalam)
- [static let mongolian: NLScript](/documentation/naturallanguage/nlscript/mongolian)
- [static let myanmar: NLScript](/documentation/naturallanguage/nlscript/myanmar)
- [static let oriya: NLScript](/documentation/naturallanguage/nlscript/oriya)
- [static let simplifiedChinese: NLScript](/documentation/naturallanguage/nlscript/simplifiedchinese)
- [static let sinhala: NLScript](/documentation/naturallanguage/nlscript/sinhala)
- [static let tamil: NLScript](/documentation/naturallanguage/nlscript/tamil)
- [static let telugu: NLScript](/documentation/naturallanguage/nlscript/telugu)
- [static let thai: NLScript](/documentation/naturallanguage/nlscript/thai)
- [static let tibetan: NLScript](/documentation/naturallanguage/nlscript/tibetan)
- [static let traditionalChinese: NLScript](/documentation/naturallanguage/nlscript/traditionalchinese)
- [static let undetermined: NLScript](/documentation/naturallanguage/nlscript/undetermined)

### Creating custom script tags

- [init(String)](/documentation/naturallanguage/nlscript/init(_:))
- [init(rawValue: String)](/documentation/naturallanguage/nlscript/init(rawvalue:))

## Natural language models

- [Creating a text classifier model](/documentation/createml/creating-a-text-classifier-model)
- [Creating a word tagger model](/documentation/createml/creating-a-word-tagger-model)
- [NLModel](/documentation/naturallanguage/nlmodel)

### Creating a model

- [convenience init(mlModel: MLModel) throws](/documentation/naturallanguage/nlmodel/init(mlmodel:))
- [convenience init(contentsOf: URL) throws](/documentation/naturallanguage/nlmodel/init(contentsof:))

### Making predictions

- [func predictedLabel(for: String) -> String?](/documentation/naturallanguage/nlmodel/predictedlabel(for:))
- [func predictedLabels(forTokens: [String]) -> [String]](/documentation/naturallanguage/nlmodel/predictedlabels(fortokens:))
- [func predictedLabelHypotheses(for: String, maximumCount: Int) -> [String : Double]](/documentation/naturallanguage/nlmodel/predictedlabelhypotheses(for:maximumcount:))
- [func predictedLabelHypotheses(forTokens: [String], maximumCount: Int) -> [[String : Double]]](/documentation/naturallanguage/nlmodel/predictedlabelhypotheses(fortokens:maximumcount:))

### Inspecting a model

- [var configuration: NLModelConfiguration](/documentation/naturallanguage/nlmodel/configuration)
- [NLModelConfiguration](/documentation/naturallanguage/nlmodelconfiguration)

#### Accessing the configuration

- [var language: NLLanguage?](/documentation/naturallanguage/nlmodelconfiguration/language)
- [var revision: Int](/documentation/naturallanguage/nlmodelconfiguration/revision)
- [class func supportedRevisions(for: NLModel.ModelType) -> IndexSet](/documentation/naturallanguage/nlmodelconfiguration/supportedrevisions(for:))
- [class func currentRevision(for: NLModel.ModelType) -> Int](/documentation/naturallanguage/nlmodelconfiguration/currentrevision(for:))
- [var type: NLModel.ModelType](/documentation/naturallanguage/nlmodelconfiguration/type)
- [NLModel.ModelType](/documentation/naturallanguage/nlmodel/modeltype)

##### Model types

- [case sequence](/documentation/naturallanguage/nlmodel/modeltype/sequence)
- [case classifier](/documentation/naturallanguage/nlmodel/modeltype/classifier)

##### Initializers

- [init?(rawValue: Int)](/documentation/naturallanguage/nlmodel/modeltype/init(rawvalue:))

### Related Documentation

- [MLTextClassifier](/documentation/createml/mltextclassifier)
- [MLWordTagger](/documentation/createml/mlwordtagger)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
