# Foundation Models Documentation

Source: https://sosumi.ai/documentation/foundationmodels

---
title: Foundation Models
source: https://developer.apple.com/documentation/foundationmodels
timestamp: 2026-02-13T18:57:10.828Z
---

## Essentials

- [Generating content and performing tasks with Foundation Models](/documentation/foundationmodels/generating-content-and-performing-tasks-with-foundation-models)
- [Improving the safety of generative model output](/documentation/foundationmodels/improving-the-safety-of-generative-model-output)
- [Supporting languages and locales with Foundation Models](/documentation/foundationmodels/supporting-languages-and-locales-with-foundation-models)
- [Adding intelligent app features with generative models](/documentation/foundationmodels/adding-intelligent-app-features-with-generative-models)
- [SystemLanguageModel](/documentation/foundationmodels/systemlanguagemodel)

### Loading the model with a use case

- [convenience init(useCase: SystemLanguageModel.UseCase, guardrails: SystemLanguageModel.Guardrails)](/documentation/foundationmodels/systemlanguagemodel/init(usecase:guardrails:))
- [SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase)

#### Getting the general use case

- [Generating content and performing tasks with Foundation Models](/documentation/foundationmodels/generating-content-and-performing-tasks-with-foundation-models)
- [static let general: SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase/general)

#### Getting the content tagging use case

- [Categorizing and organizing data with content tags](/documentation/foundationmodels/categorizing-and-organizing-data-with-content-tags)
- [static let contentTagging: SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase/contenttagging)
- [SystemLanguageModel.Guardrails](/documentation/foundationmodels/systemlanguagemodel/guardrails)

#### Getting the guardrail types

- [static let `default`: SystemLanguageModel.Guardrails](/documentation/foundationmodels/systemlanguagemodel/guardrails/default)
- [static let permissiveContentTransformations: SystemLanguageModel.Guardrails](/documentation/foundationmodels/systemlanguagemodel/guardrails/permissivecontenttransformations)

#### Handling guardrail errors

- [case guardrailViolation(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/guardrailviolation(_:))

### Loading the model with an adapter

- [Loading and using a custom adapter with Foundation Models](/documentation/foundationmodels/loading-and-using-a-custom-adapter-with-foundation-models)
- [com.apple.developer.foundation-model-adapter](/documentation/bundleresources/entitlements/com.apple.developer.foundation-model-adapter)
- [convenience init(adapter: SystemLanguageModel.Adapter, guardrails: SystemLanguageModel.Guardrails)](/documentation/foundationmodels/systemlanguagemodel/init(adapter:guardrails:))
- [SystemLanguageModel.Adapter](/documentation/foundationmodels/systemlanguagemodel/adapter)

#### Creating an adapter

- [Loading and using a custom adapter with Foundation Models](/documentation/foundationmodels/loading-and-using-a-custom-adapter-with-foundation-models)
- [com.apple.developer.foundation-model-adapter](/documentation/bundleresources/entitlements/com.apple.developer.foundation-model-adapter)
- [init(fileURL: URL) throws](/documentation/foundationmodels/systemlanguagemodel/adapter/init(fileurl:))
- [init(name: String) throws](/documentation/foundationmodels/systemlanguagemodel/adapter/init(name:))

#### Prepare the adapter

- [func compile() async throws](/documentation/foundationmodels/systemlanguagemodel/adapter/compile())

#### Getting the metadata

- [var creatorDefinedMetadata: [String : Any]](/documentation/foundationmodels/systemlanguagemodel/adapter/creatordefinedmetadata)

#### Removing obsolete adapters

- [static func removeObsoleteAdapters() throws](/documentation/foundationmodels/systemlanguagemodel/adapter/removeobsoleteadapters())

#### Checking compatibility

- [static func compatibleAdapterIdentifiers(name: String) -> [String]](/documentation/foundationmodels/systemlanguagemodel/adapter/compatibleadapteridentifiers(name:))
- [static func isCompatible(AssetPack) -> Bool](/documentation/foundationmodels/systemlanguagemodel/adapter/iscompatible(_:))

#### Getting the asset error

- [SystemLanguageModel.Adapter.AssetError](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror)

##### Getting the asset errors

- [case compatibleAdapterNotFound(SystemLanguageModel.Adapter.AssetError.Context)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/compatibleadapternotfound(_:))
- [case invalidAdapterName(SystemLanguageModel.Adapter.AssetError.Context)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/invalidadaptername(_:))
- [case invalidAsset(SystemLanguageModel.Adapter.AssetError.Context)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/invalidasset(_:))
- [SystemLanguageModel.Adapter.AssetError.Context](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/context)

###### Creating a context

- [init(debugDescription: String)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/context/init(debugdescription:))

###### Getting the debug description

- [let debugDescription: String](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/context/debugdescription)

##### Getting the error description

- [var errorDescription: String?](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/errordescription)

### Checking model availability

- [var isAvailable: Bool](/documentation/foundationmodels/systemlanguagemodel/isavailable)
- [var availability: SystemLanguageModel.Availability](/documentation/foundationmodels/systemlanguagemodel/availability-swift.property)
- [SystemLanguageModel.Availability](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum)

#### Checking for availability

- [case available](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/available)
- [case unavailable(SystemLanguageModel.Availability.UnavailableReason)](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailable(_:))
- [SystemLanguageModel.Availability.UnavailableReason](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason)

##### Getting the unavailable reasons

- [case appleIntelligenceNotEnabled](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason/appleintelligencenotenabled)
- [case deviceNotEligible](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason/devicenoteligible)
- [case modelNotReady](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason/modelnotready)

### Retrieving the supported languages

- [var supportedLanguages: Set<Locale.Language>](/documentation/foundationmodels/systemlanguagemodel/supportedlanguages)

### Determining whether the model supports a locale

- [func supportsLocale(Locale) -> Bool](/documentation/foundationmodels/systemlanguagemodel/supportslocale(_:))

### Getting the default model

- [static let `default`: SystemLanguageModel](/documentation/foundationmodels/systemlanguagemodel/default)
- [SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase)

### Getting the general use case

- [Generating content and performing tasks with Foundation Models](/documentation/foundationmodels/generating-content-and-performing-tasks-with-foundation-models)
- [static let general: SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase/general)

### Getting the content tagging use case

- [Categorizing and organizing data with content tags](/documentation/foundationmodels/categorizing-and-organizing-data-with-content-tags)
- [static let contentTagging: SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase/contenttagging)

## Prompting

- [Prompting an on-device foundation model](/documentation/foundationmodels/prompting-an-on-device-foundation-model)
- [Analyzing the runtime performance of your Foundation Models app](/documentation/foundationmodels/analyzing-the-runtime-performance-of-your-foundation-models-app)
- [LanguageModelSession](/documentation/foundationmodels/languagemodelsession)

### Creating a session

- [convenience(model:tools:instructions:)](/documentation/foundationmodels/languagemodelsession/init(model:tools:instructions:))
- [SystemLanguageModel](/documentation/foundationmodels/systemlanguagemodel)

#### Loading the model with a use case

- [convenience init(useCase: SystemLanguageModel.UseCase, guardrails: SystemLanguageModel.Guardrails)](/documentation/foundationmodels/systemlanguagemodel/init(usecase:guardrails:))
- [SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase)

##### Getting the general use case

- [Generating content and performing tasks with Foundation Models](/documentation/foundationmodels/generating-content-and-performing-tasks-with-foundation-models)
- [static let general: SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase/general)

##### Getting the content tagging use case

- [Categorizing and organizing data with content tags](/documentation/foundationmodels/categorizing-and-organizing-data-with-content-tags)
- [static let contentTagging: SystemLanguageModel.UseCase](/documentation/foundationmodels/systemlanguagemodel/usecase/contenttagging)
- [SystemLanguageModel.Guardrails](/documentation/foundationmodels/systemlanguagemodel/guardrails)

##### Getting the guardrail types

- [static let `default`: SystemLanguageModel.Guardrails](/documentation/foundationmodels/systemlanguagemodel/guardrails/default)
- [static let permissiveContentTransformations: SystemLanguageModel.Guardrails](/documentation/foundationmodels/systemlanguagemodel/guardrails/permissivecontenttransformations)

##### Handling guardrail errors

- [case guardrailViolation(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/guardrailviolation(_:))

#### Loading the model with an adapter

- [Loading and using a custom adapter with Foundation Models](/documentation/foundationmodels/loading-and-using-a-custom-adapter-with-foundation-models)
- [com.apple.developer.foundation-model-adapter](/documentation/bundleresources/entitlements/com.apple.developer.foundation-model-adapter)
- [convenience init(adapter: SystemLanguageModel.Adapter, guardrails: SystemLanguageModel.Guardrails)](/documentation/foundationmodels/systemlanguagemodel/init(adapter:guardrails:))
- [SystemLanguageModel.Adapter](/documentation/foundationmodels/systemlanguagemodel/adapter)

##### Creating an adapter

- [Loading and using a custom adapter with Foundation Models](/documentation/foundationmodels/loading-and-using-a-custom-adapter-with-foundation-models)
- [com.apple.developer.foundation-model-adapter](/documentation/bundleresources/entitlements/com.apple.developer.foundation-model-adapter)
- [init(fileURL: URL) throws](/documentation/foundationmodels/systemlanguagemodel/adapter/init(fileurl:))
- [init(name: String) throws](/documentation/foundationmodels/systemlanguagemodel/adapter/init(name:))

##### Prepare the adapter

- [func compile() async throws](/documentation/foundationmodels/systemlanguagemodel/adapter/compile())

##### Getting the metadata

- [var creatorDefinedMetadata: [String : Any]](/documentation/foundationmodels/systemlanguagemodel/adapter/creatordefinedmetadata)

##### Removing obsolete adapters

- [static func removeObsoleteAdapters() throws](/documentation/foundationmodels/systemlanguagemodel/adapter/removeobsoleteadapters())

##### Checking compatibility

- [static func compatibleAdapterIdentifiers(name: String) -> [String]](/documentation/foundationmodels/systemlanguagemodel/adapter/compatibleadapteridentifiers(name:))
- [static func isCompatible(AssetPack) -> Bool](/documentation/foundationmodels/systemlanguagemodel/adapter/iscompatible(_:))

##### Getting the asset error

- [SystemLanguageModel.Adapter.AssetError](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror)

###### Getting the asset errors

- [case compatibleAdapterNotFound(SystemLanguageModel.Adapter.AssetError.Context)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/compatibleadapternotfound(_:))
- [case invalidAdapterName(SystemLanguageModel.Adapter.AssetError.Context)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/invalidadaptername(_:))
- [case invalidAsset(SystemLanguageModel.Adapter.AssetError.Context)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/invalidasset(_:))
- [SystemLanguageModel.Adapter.AssetError.Context](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/context)

###### Creating a context

- [init(debugDescription: String)](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/context/init(debugdescription:))

###### Getting the debug description

- [let debugDescription: String](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/context/debugdescription)

###### Getting the error description

- [var errorDescription: String?](/documentation/foundationmodels/systemlanguagemodel/adapter/asseterror/errordescription)

#### Checking model availability

- [var isAvailable: Bool](/documentation/foundationmodels/systemlanguagemodel/isavailable)
- [var availability: SystemLanguageModel.Availability](/documentation/foundationmodels/systemlanguagemodel/availability-swift.property)
- [SystemLanguageModel.Availability](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum)

##### Checking for availability

- [case available](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/available)
- [case unavailable(SystemLanguageModel.Availability.UnavailableReason)](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailable(_:))
- [SystemLanguageModel.Availability.UnavailableReason](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason)

###### Getting the unavailable reasons

- [case appleIntelligenceNotEnabled](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason/appleintelligencenotenabled)
- [case deviceNotEligible](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason/devicenoteligible)
- [case modelNotReady](/documentation/foundationmodels/systemlanguagemodel/availability-swift.enum/unavailablereason/modelnotready)

#### Retrieving the supported languages

- [var supportedLanguages: Set<Locale.Language>](/documentation/foundationmodels/systemlanguagemodel/supportedlanguages)

#### Determining whether the model supports a locale

- [func supportsLocale(Locale) -> Bool](/documentation/foundationmodels/systemlanguagemodel/supportslocale(_:))

#### Getting the default model

- [static let `default`: SystemLanguageModel](/documentation/foundationmodels/systemlanguagemodel/default)
- [Tool](/documentation/foundationmodels/tool)

#### Invoking a tool

- [func call(arguments: Self.Arguments) async throws -> Self.Output](/documentation/foundationmodels/tool/call(arguments:))
- [Arguments](/documentation/foundationmodels/tool/arguments)
- [Output](/documentation/foundationmodels/tool/output)

#### Getting the tool properties

- [var description: String](/documentation/foundationmodels/tool/description)
- [var includesSchemaInInstructions: Bool](/documentation/foundationmodels/tool/includesschemaininstructions)
- [var name: String](/documentation/foundationmodels/tool/name)
- [var parameters: GenerationSchema](/documentation/foundationmodels/tool/parameters)
- [Instructions](/documentation/foundationmodels/instructions)

#### Creating instructions

- [init(_:)](/documentation/foundationmodels/instructions/init(_:))
- [InstructionsBuilder](/documentation/foundationmodels/instructionsbuilder)

##### Building instructions

- [static func buildArray([some InstructionsRepresentable]) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildarray(_:))
- [static func buildBlock<each I>(repeat each I) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildblock(_:))
- [static func buildEither(first: some InstructionsRepresentable) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildeither(first:))
- [static func buildEither(second: some InstructionsRepresentable) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildeither(second:))
- [static buildExpression(_:)](/documentation/foundationmodels/instructionsbuilder/buildexpression(_:))
- [static func buildLimitedAvailability(some InstructionsRepresentable) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildlimitedavailability(_:))
- [static func buildOptional(Instructions?) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildoptional(_:))
- [InstructionsRepresentable](/documentation/foundationmodels/instructionsrepresentable)

##### Getting the representation

- [var instructionsRepresentation: Instructions](/documentation/foundationmodels/instructionsrepresentable/instructionsrepresentation)

### Creating a session from a transcript

- [convenience init(model: SystemLanguageModel, tools: [any Tool], transcript: Transcript)](/documentation/foundationmodels/languagemodelsession/init(model:tools:transcript:))
- [Transcript](/documentation/foundationmodels/transcript)

#### Creating a transcript

- [init(entries: some Sequence<Transcript.Entry>)](/documentation/foundationmodels/transcript/init(entries:))
- [Transcript.Entry](/documentation/foundationmodels/transcript/entry)

##### Creating an entry

- [case instructions(Transcript.Instructions)](/documentation/foundationmodels/transcript/entry/instructions(_:))
- [case prompt(Transcript.Prompt)](/documentation/foundationmodels/transcript/entry/prompt(_:))
- [case response(Transcript.Response)](/documentation/foundationmodels/transcript/entry/response(_:))
- [case toolCalls(Transcript.ToolCalls)](/documentation/foundationmodels/transcript/entry/toolcalls(_:))
- [case toolOutput(Transcript.ToolOutput)](/documentation/foundationmodels/transcript/entry/tooloutput(_:))
- [Transcript.Segment](/documentation/foundationmodels/transcript/segment)

##### Creating a segment

- [case structure(Transcript.StructuredSegment)](/documentation/foundationmodels/transcript/segment/structure(_:))
- [case text(Transcript.TextSegment)](/documentation/foundationmodels/transcript/segment/text(_:))

#### Getting the transcript types

- [Transcript.Instructions](/documentation/foundationmodels/transcript/instructions)

##### Creating instructions

- [init(id: String, segments: [Transcript.Segment], toolDefinitions: [Transcript.ToolDefinition])](/documentation/foundationmodels/transcript/instructions/init(id:segments:tooldefinitions:))

##### Inspecting instructions

- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/instructions/segments)
- [var toolDefinitions: [Transcript.ToolDefinition]](/documentation/foundationmodels/transcript/instructions/tooldefinitions)
- [Transcript.Prompt](/documentation/foundationmodels/transcript/prompt)

##### Creating a prompt

- [init(id: String, segments: [Transcript.Segment], options: GenerationOptions, responseFormat: Transcript.ResponseFormat?)](/documentation/foundationmodels/transcript/prompt/init(id:segments:options:responseformat:))

##### Inspecting a prompt

- [var id: String](/documentation/foundationmodels/transcript/prompt/id)
- [var responseFormat: Transcript.ResponseFormat?](/documentation/foundationmodels/transcript/prompt/responseformat)
- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/prompt/segments)
- [var options: GenerationOptions](/documentation/foundationmodels/transcript/prompt/options)
- [Transcript.Response](/documentation/foundationmodels/transcript/response)

##### Creating a response

- [init(id: String, assetIDs: [String], segments: [Transcript.Segment])](/documentation/foundationmodels/transcript/response/init(id:assetids:segments:))

##### Inspecting a response

- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/response/segments)
- [var assetIDs: [String]](/documentation/foundationmodels/transcript/response/assetids)
- [Transcript.ResponseFormat](/documentation/foundationmodels/transcript/responseformat)

##### Creating a response format

- [init(schema: GenerationSchema)](/documentation/foundationmodels/transcript/responseformat/init(schema:))
- [init<Content>(type: Content.Type)](/documentation/foundationmodels/transcript/responseformat/init(type:))

##### Inspecting a response format

- [var name: String](/documentation/foundationmodels/transcript/responseformat/name)
- [Transcript.StructuredSegment](/documentation/foundationmodels/transcript/structuredsegment)

##### Creating a structured segment

- [init(id: String, source: String, content: GeneratedContent)](/documentation/foundationmodels/transcript/structuredsegment/init(id:source:content:))

##### Inspecting a structured segment

- [var content: GeneratedContent](/documentation/foundationmodels/transcript/structuredsegment/content)
- [var source: String](/documentation/foundationmodels/transcript/structuredsegment/source)
- [Transcript.TextSegment](/documentation/foundationmodels/transcript/textsegment)

##### Creating a text segment

- [init(id: String, content: String)](/documentation/foundationmodels/transcript/textsegment/init(id:content:))

##### Inspecting a text segment

- [var content: String](/documentation/foundationmodels/transcript/textsegment/content)
- [Transcript.ToolCall](/documentation/foundationmodels/transcript/toolcall)

##### Creating a tool call

- [init(id: String, toolName: String, arguments: GeneratedContent)](/documentation/foundationmodels/transcript/toolcall/init(id:toolname:arguments:))

##### Inspecting a tool call

- [var arguments: GeneratedContent](/documentation/foundationmodels/transcript/toolcall/arguments)
- [var toolName: String](/documentation/foundationmodels/transcript/toolcall/toolname)
- [Transcript.ToolCalls](/documentation/foundationmodels/transcript/toolcalls)

##### Creating a tool calls

- [init<S>(id: String, S)](/documentation/foundationmodels/transcript/toolcalls/init(id:_:))
- [Transcript.ToolDefinition](/documentation/foundationmodels/transcript/tooldefinition)

##### Creating a tool definition

- [init(name: String, description: String, parameters: GenerationSchema)](/documentation/foundationmodels/transcript/tooldefinition/init(name:description:parameters:))
- [init(tool: some Tool)](/documentation/foundationmodels/transcript/tooldefinition/init(tool:))

##### Inspecting a tool definition

- [var description: String](/documentation/foundationmodels/transcript/tooldefinition/description)
- [var name: String](/documentation/foundationmodels/transcript/tooldefinition/name)
- [Transcript.ToolOutput](/documentation/foundationmodels/transcript/tooloutput)

##### Creating a tool output

- [init(id: String, toolName: String, segments: [Transcript.Segment])](/documentation/foundationmodels/transcript/tooloutput/init(id:toolname:segments:))

##### Inspecting a tool output

- [var id: String](/documentation/foundationmodels/transcript/tooloutput/id)
- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/tooloutput/segments)
- [var toolName: String](/documentation/foundationmodels/transcript/tooloutput/toolname)

### Preloading the model

- [func prewarm(promptPrefix: Prompt?)](/documentation/foundationmodels/languagemodelsession/prewarm(promptprefix:))

### Inspecting session properties

- [var isResponding: Bool](/documentation/foundationmodels/languagemodelsession/isresponding)
- [var transcript: Transcript](/documentation/foundationmodels/languagemodelsession/transcript)

### Generating a request

- [func respond(options: GenerationOptions, prompt: () throws -> Prompt) async throws -> LanguageModelSession.Response<String>](/documentation/foundationmodels/languagemodelsession/respond(options:prompt:))
- [func respond<Content>(generating: Content.Type, includeSchemaInPrompt: Bool, options: GenerationOptions, prompt: () throws -> Prompt) async throws -> LanguageModelSession.Response<Content>](/documentation/foundationmodels/languagemodelsession/respond(generating:includeschemainprompt:options:prompt:))
- [func respond(schema: GenerationSchema, includeSchemaInPrompt: Bool, options: GenerationOptions, prompt: () throws -> Prompt) async throws -> LanguageModelSession.Response<GeneratedContent>](/documentation/foundationmodels/languagemodelsession/respond(schema:includeschemainprompt:options:prompt:))
- [func respond(to:options:)](/documentation/foundationmodels/languagemodelsession/respond(to:options:))
- [func respond(to:generating:includeSchemaInPrompt:options:)](/documentation/foundationmodels/languagemodelsession/respond(to:generating:includeschemainprompt:options:))
- [func respond(to:schema:includeSchemaInPrompt:options:)](/documentation/foundationmodels/languagemodelsession/respond(to:schema:includeschemainprompt:options:))
- [Prompt](/documentation/foundationmodels/prompt)

#### Creating a prompt

- [init(_:)](/documentation/foundationmodels/prompt/init(_:))
- [PromptBuilder](/documentation/foundationmodels/promptbuilder)

##### Building a prompt

- [static func buildArray([some PromptRepresentable]) -> Prompt](/documentation/foundationmodels/promptbuilder/buildarray(_:))
- [static func buildBlock<each P>(repeat each P) -> Prompt](/documentation/foundationmodels/promptbuilder/buildblock(_:))
- [static func buildEither(first: some PromptRepresentable) -> Prompt](/documentation/foundationmodels/promptbuilder/buildeither(first:))
- [static func buildEither(second: some PromptRepresentable) -> Prompt](/documentation/foundationmodels/promptbuilder/buildeither(second:))
- [static buildExpression(_:)](/documentation/foundationmodels/promptbuilder/buildexpression(_:))
- [static func buildLimitedAvailability(some PromptRepresentable) -> Prompt](/documentation/foundationmodels/promptbuilder/buildlimitedavailability(_:))
- [static func buildOptional(Prompt?) -> Prompt](/documentation/foundationmodels/promptbuilder/buildoptional(_:))
- [PromptRepresentable](/documentation/foundationmodels/promptrepresentable)

##### Getting the representation

- [var promptRepresentation: Prompt](/documentation/foundationmodels/promptrepresentable/promptrepresentation)
- [LanguageModelSession.Response](/documentation/foundationmodels/languagemodelsession/response)

#### Getting the response content

- [let content: Content](/documentation/foundationmodels/languagemodelsession/response/content)
- [let rawContent: GeneratedContent](/documentation/foundationmodels/languagemodelsession/response/rawcontent)

#### Getting the transcript entries

- [let transcriptEntries: ArraySlice<Transcript.Entry>](/documentation/foundationmodels/languagemodelsession/response/transcriptentries)
- [GenerationOptions](/documentation/foundationmodels/generationoptions)

#### Creating options

- [init(sampling: GenerationOptions.SamplingMode?, temperature: Double?, maximumResponseTokens: Int?)](/documentation/foundationmodels/generationoptions/init(sampling:temperature:maximumresponsetokens:))

#### Configuring the response tokens

- [var maximumResponseTokens: Int?](/documentation/foundationmodels/generationoptions/maximumresponsetokens)

#### Configuring the sampling mode

- [var sampling: GenerationOptions.SamplingMode?](/documentation/foundationmodels/generationoptions/sampling)
- [GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode)

##### Sampling options

- [static var greedy: GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode/greedy)
- [static func random(probabilityThreshold: Double, seed: UInt64?) -> GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode/random(probabilitythreshold:seed:))
- [static func random(top: Int, seed: UInt64?) -> GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode/random(top:seed:))

#### Configuring the temperature

- [var temperature: Double?](/documentation/foundationmodels/generationoptions/temperature)

### Streaming a response

- [func streamResponse(to:options:)](/documentation/foundationmodels/languagemodelsession/streamresponse(to:options:))
- [func streamResponse(to:generating:includeSchemaInPrompt:options:)](/documentation/foundationmodels/languagemodelsession/streamresponse(to:generating:includeschemainprompt:options:))
- [func streamResponse(to:schema:includeSchemaInPrompt:options:)](/documentation/foundationmodels/languagemodelsession/streamresponse(to:schema:includeschemainprompt:options:))
- [func streamResponse(options: GenerationOptions, prompt: () throws -> Prompt) rethrows -> sending LanguageModelSession.ResponseStream<String>](/documentation/foundationmodels/languagemodelsession/streamresponse(options:prompt:))
- [func streamResponse<Content>(generating: Content.Type, includeSchemaInPrompt: Bool, options: GenerationOptions, prompt: () throws -> Prompt) rethrows -> sending LanguageModelSession.ResponseStream<Content>](/documentation/foundationmodels/languagemodelsession/streamresponse(generating:includeschemainprompt:options:prompt:))
- [func streamResponse(schema: GenerationSchema, includeSchemaInPrompt: Bool, options: GenerationOptions, prompt: () throws -> Prompt) rethrows -> sending LanguageModelSession.ResponseStream<GeneratedContent>](/documentation/foundationmodels/languagemodelsession/streamresponse(schema:includeschemainprompt:options:prompt:))
- [LanguageModelSession.ResponseStream](/documentation/foundationmodels/languagemodelsession/responsestream)

#### Collecting the response stream

- [func collect() async throws -> sending LanguageModelSession.Response<Content>](/documentation/foundationmodels/languagemodelsession/responsestream/collect())

#### Getting a snapshot of a partial response

- [LanguageModelSession.ResponseStream.Snapshot](/documentation/foundationmodels/languagemodelsession/responsestream/snapshot)

##### Instance Properties

- [var content: Content.PartiallyGenerated](/documentation/foundationmodels/languagemodelsession/responsestream/snapshot/content)
- [var rawContent: GeneratedContent](/documentation/foundationmodels/languagemodelsession/responsestream/snapshot/rawcontent)
- [GeneratedContent](/documentation/foundationmodels/generatedcontent)

#### Creating generated content

- [init(_:)](/documentation/foundationmodels/generatedcontent/init(_:))
- [init(some ConvertibleToGeneratedContent, id: GenerationID)](/documentation/foundationmodels/generatedcontent/init(_:id:))
- [init<S>(elements: S, id: GenerationID?)](/documentation/foundationmodels/generatedcontent/init(elements:id:))
- [init(kind: GeneratedContent.Kind, id: GenerationID?)](/documentation/foundationmodels/generatedcontent/init(kind:id:))

#### Creating content from properties

- [init(properties: KeyValuePairs<String, any ConvertibleToGeneratedContent>, id: GenerationID?)](/documentation/foundationmodels/generatedcontent/init(properties:id:))
- [init<S>(properties: S, id: GenerationID?, uniquingKeysWith: (GeneratedContent, GeneratedContent) throws -> some ConvertibleToGeneratedContent) rethrows](/documentation/foundationmodels/generatedcontent/init(properties:id:uniquingkeyswith:))

#### Creating content from JSON

- [init(json: String) throws](/documentation/foundationmodels/generatedcontent/init(json:))

#### Creating content from kind

- [init(kind: GeneratedContent.Kind, id: GenerationID?)](/documentation/foundationmodels/generatedcontent/init(kind:id:))
- [GeneratedContent.Kind](/documentation/foundationmodels/generatedcontent/kind-swift.enum)

##### Getting the kind of content

- [case array([GeneratedContent])](/documentation/foundationmodels/generatedcontent/kind-swift.enum/array(_:))
- [case bool(Bool)](/documentation/foundationmodels/generatedcontent/kind-swift.enum/bool(_:))
- [case null](/documentation/foundationmodels/generatedcontent/kind-swift.enum/null)
- [case number(Double)](/documentation/foundationmodels/generatedcontent/kind-swift.enum/number(_:))
- [case string(String)](/documentation/foundationmodels/generatedcontent/kind-swift.enum/string(_:))
- [case structure(properties: [String : GeneratedContent], orderedKeys: [String])](/documentation/foundationmodels/generatedcontent/kind-swift.enum/structure(properties:orderedkeys:))

#### Accessing instance properties

- [var kind: GeneratedContent.Kind](/documentation/foundationmodels/generatedcontent/kind-swift.property)
- [var isComplete: Bool](/documentation/foundationmodels/generatedcontent/iscomplete)
- [var jsonString: String](/documentation/foundationmodels/generatedcontent/jsonstring)

#### Getting the debug description

- [var debugDescription: String](/documentation/foundationmodels/generatedcontent/debugdescription)

#### Reads a value from the concrete type

- [func value<Value>(Value.Type) throws -> Value](/documentation/foundationmodels/generatedcontent/value(_:))
- [func value(_:forProperty:)](/documentation/foundationmodels/generatedcontent/value(_:forproperty:))

#### Retrieving the schema and content

- [var generatedContent: GeneratedContent](/documentation/foundationmodels/generatedcontent/generatedcontent)

#### Getting the unique generation id

- [var id: GenerationID?](/documentation/foundationmodels/generatedcontent/id)
- [ConvertibleFromGeneratedContent](/documentation/foundationmodels/convertiblefromgeneratedcontent)

#### Creating a convertable

- [init(GeneratedContent) throws](/documentation/foundationmodels/convertiblefromgeneratedcontent/init(_:))
- [ConvertibleToGeneratedContent](/documentation/foundationmodels/convertibletogeneratedcontent)

#### Getting the generated content

- [var generatedContent: GeneratedContent](/documentation/foundationmodels/convertibletogeneratedcontent/generatedcontent)

### Generating feedback

- [func logFeedbackAttachment(sentiment: LanguageModelFeedback.Sentiment?, issues: [LanguageModelFeedback.Issue], desiredOutput: Transcript.Entry?) -> Data](/documentation/foundationmodels/languagemodelsession/logfeedbackattachment(sentiment:issues:desiredoutput:))
- [func logFeedbackAttachment(sentiment: LanguageModelFeedback.Sentiment?, issues: [LanguageModelFeedback.Issue], desiredResponseContent: (any ConvertibleToGeneratedContent)?) -> Data](/documentation/foundationmodels/languagemodelsession/logfeedbackattachment(sentiment:issues:desiredresponsecontent:))
- [func logFeedbackAttachment(sentiment: LanguageModelFeedback.Sentiment?, issues: [LanguageModelFeedback.Issue], desiredResponseText: String?) -> Data](/documentation/foundationmodels/languagemodelsession/logfeedbackattachment(sentiment:issues:desiredresponsetext:))

### Getting the error types

- [LanguageModelSession.GenerationError](/documentation/foundationmodels/languagemodelsession/generationerror)

#### Generation errors

- [case assetsUnavailable(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/assetsunavailable(_:))
- [case decodingFailure(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/decodingfailure(_:))
- [case exceededContextWindowSize(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/exceededcontextwindowsize(_:))
- [case guardrailViolation(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/guardrailviolation(_:))
- [case rateLimited(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/ratelimited(_:))
- [case refusal(LanguageModelSession.GenerationError.Refusal, LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/refusal(_:_:))
- [case concurrentRequests(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/concurrentrequests(_:))
- [case unsupportedGuide(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/unsupportedguide(_:))
- [case unsupportedLanguageOrLocale(LanguageModelSession.GenerationError.Context)](/documentation/foundationmodels/languagemodelsession/generationerror/unsupportedlanguageorlocale(_:))
- [LanguageModelSession.GenerationError.Context](/documentation/foundationmodels/languagemodelsession/generationerror/context)

##### Creating a context

- [init(debugDescription: String)](/documentation/foundationmodels/languagemodelsession/generationerror/context/init(debugdescription:))

##### Getting the debug description

- [let debugDescription: String](/documentation/foundationmodels/languagemodelsession/generationerror/context/debugdescription)
- [LanguageModelSession.GenerationError.Refusal](/documentation/foundationmodels/languagemodelsession/generationerror/refusal)

##### Creating a generation error refusal

- [init(transcriptEntries: [Transcript.Entry])](/documentation/foundationmodels/languagemodelsession/generationerror/refusal/init(transcriptentries:))

##### Getting the explanation

- [var explanation: LanguageModelSession.Response<String>](/documentation/foundationmodels/languagemodelsession/generationerror/refusal/explanation)
- [var explanationStream: LanguageModelSession.ResponseStream<String>](/documentation/foundationmodels/languagemodelsession/generationerror/refusal/explanationstream)

#### Getting the error description

- [var errorDescription: String?](/documentation/foundationmodels/languagemodelsession/generationerror/errordescription)

#### Getting the failure reason

- [var failureReason: String?](/documentation/foundationmodels/languagemodelsession/generationerror/failurereason)

#### Getting the recovery suggestion

- [var recoverySuggestion: String?](/documentation/foundationmodels/languagemodelsession/generationerror/recoverysuggestion)
- [LanguageModelSession.ToolCallError](/documentation/foundationmodels/languagemodelsession/toolcallerror)

#### Creating a tool call error

- [init(tool: any Tool, underlyingError: any Error)](/documentation/foundationmodels/languagemodelsession/toolcallerror/init(tool:underlyingerror:))

#### Getting the tool

- [var tool: any Tool](/documentation/foundationmodels/languagemodelsession/toolcallerror/tool)

#### Getting the error description

- [var errorDescription: String?](/documentation/foundationmodels/languagemodelsession/toolcallerror/errordescription)

#### Getting the underlying error

- [var underlyingError: any Error](/documentation/foundationmodels/languagemodelsession/toolcallerror/underlyingerror)
- [Instructions](/documentation/foundationmodels/instructions)

### Creating instructions

- [init(_:)](/documentation/foundationmodels/instructions/init(_:))
- [InstructionsBuilder](/documentation/foundationmodels/instructionsbuilder)

#### Building instructions

- [static func buildArray([some InstructionsRepresentable]) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildarray(_:))
- [static func buildBlock<each I>(repeat each I) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildblock(_:))
- [static func buildEither(first: some InstructionsRepresentable) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildeither(first:))
- [static func buildEither(second: some InstructionsRepresentable) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildeither(second:))
- [static buildExpression(_:)](/documentation/foundationmodels/instructionsbuilder/buildexpression(_:))
- [static func buildLimitedAvailability(some InstructionsRepresentable) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildlimitedavailability(_:))
- [static func buildOptional(Instructions?) -> Instructions](/documentation/foundationmodels/instructionsbuilder/buildoptional(_:))
- [InstructionsRepresentable](/documentation/foundationmodels/instructionsrepresentable)

#### Getting the representation

- [var instructionsRepresentation: Instructions](/documentation/foundationmodels/instructionsrepresentable/instructionsrepresentation)
- [Prompt](/documentation/foundationmodels/prompt)

### Creating a prompt

- [init(_:)](/documentation/foundationmodels/prompt/init(_:))
- [PromptBuilder](/documentation/foundationmodels/promptbuilder)

#### Building a prompt

- [static func buildArray([some PromptRepresentable]) -> Prompt](/documentation/foundationmodels/promptbuilder/buildarray(_:))
- [static func buildBlock<each P>(repeat each P) -> Prompt](/documentation/foundationmodels/promptbuilder/buildblock(_:))
- [static func buildEither(first: some PromptRepresentable) -> Prompt](/documentation/foundationmodels/promptbuilder/buildeither(first:))
- [static func buildEither(second: some PromptRepresentable) -> Prompt](/documentation/foundationmodels/promptbuilder/buildeither(second:))
- [static buildExpression(_:)](/documentation/foundationmodels/promptbuilder/buildexpression(_:))
- [static func buildLimitedAvailability(some PromptRepresentable) -> Prompt](/documentation/foundationmodels/promptbuilder/buildlimitedavailability(_:))
- [static func buildOptional(Prompt?) -> Prompt](/documentation/foundationmodels/promptbuilder/buildoptional(_:))
- [PromptRepresentable](/documentation/foundationmodels/promptrepresentable)

#### Getting the representation

- [var promptRepresentation: Prompt](/documentation/foundationmodels/promptrepresentable/promptrepresentation)
- [Transcript](/documentation/foundationmodels/transcript)

### Creating a transcript

- [init(entries: some Sequence<Transcript.Entry>)](/documentation/foundationmodels/transcript/init(entries:))
- [Transcript.Entry](/documentation/foundationmodels/transcript/entry)

#### Creating an entry

- [case instructions(Transcript.Instructions)](/documentation/foundationmodels/transcript/entry/instructions(_:))
- [case prompt(Transcript.Prompt)](/documentation/foundationmodels/transcript/entry/prompt(_:))
- [case response(Transcript.Response)](/documentation/foundationmodels/transcript/entry/response(_:))
- [case toolCalls(Transcript.ToolCalls)](/documentation/foundationmodels/transcript/entry/toolcalls(_:))
- [case toolOutput(Transcript.ToolOutput)](/documentation/foundationmodels/transcript/entry/tooloutput(_:))
- [Transcript.Segment](/documentation/foundationmodels/transcript/segment)

#### Creating a segment

- [case structure(Transcript.StructuredSegment)](/documentation/foundationmodels/transcript/segment/structure(_:))
- [case text(Transcript.TextSegment)](/documentation/foundationmodels/transcript/segment/text(_:))

### Getting the transcript types

- [Transcript.Instructions](/documentation/foundationmodels/transcript/instructions)

#### Creating instructions

- [init(id: String, segments: [Transcript.Segment], toolDefinitions: [Transcript.ToolDefinition])](/documentation/foundationmodels/transcript/instructions/init(id:segments:tooldefinitions:))

#### Inspecting instructions

- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/instructions/segments)
- [var toolDefinitions: [Transcript.ToolDefinition]](/documentation/foundationmodels/transcript/instructions/tooldefinitions)
- [Transcript.Prompt](/documentation/foundationmodels/transcript/prompt)

#### Creating a prompt

- [init(id: String, segments: [Transcript.Segment], options: GenerationOptions, responseFormat: Transcript.ResponseFormat?)](/documentation/foundationmodels/transcript/prompt/init(id:segments:options:responseformat:))

#### Inspecting a prompt

- [var id: String](/documentation/foundationmodels/transcript/prompt/id)
- [var responseFormat: Transcript.ResponseFormat?](/documentation/foundationmodels/transcript/prompt/responseformat)
- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/prompt/segments)
- [var options: GenerationOptions](/documentation/foundationmodels/transcript/prompt/options)
- [Transcript.Response](/documentation/foundationmodels/transcript/response)

#### Creating a response

- [init(id: String, assetIDs: [String], segments: [Transcript.Segment])](/documentation/foundationmodels/transcript/response/init(id:assetids:segments:))

#### Inspecting a response

- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/response/segments)
- [var assetIDs: [String]](/documentation/foundationmodels/transcript/response/assetids)
- [Transcript.ResponseFormat](/documentation/foundationmodels/transcript/responseformat)

#### Creating a response format

- [init(schema: GenerationSchema)](/documentation/foundationmodels/transcript/responseformat/init(schema:))
- [init<Content>(type: Content.Type)](/documentation/foundationmodels/transcript/responseformat/init(type:))

#### Inspecting a response format

- [var name: String](/documentation/foundationmodels/transcript/responseformat/name)
- [Transcript.StructuredSegment](/documentation/foundationmodels/transcript/structuredsegment)

#### Creating a structured segment

- [init(id: String, source: String, content: GeneratedContent)](/documentation/foundationmodels/transcript/structuredsegment/init(id:source:content:))

#### Inspecting a structured segment

- [var content: GeneratedContent](/documentation/foundationmodels/transcript/structuredsegment/content)
- [var source: String](/documentation/foundationmodels/transcript/structuredsegment/source)
- [Transcript.TextSegment](/documentation/foundationmodels/transcript/textsegment)

#### Creating a text segment

- [init(id: String, content: String)](/documentation/foundationmodels/transcript/textsegment/init(id:content:))

#### Inspecting a text segment

- [var content: String](/documentation/foundationmodels/transcript/textsegment/content)
- [Transcript.ToolCall](/documentation/foundationmodels/transcript/toolcall)

#### Creating a tool call

- [init(id: String, toolName: String, arguments: GeneratedContent)](/documentation/foundationmodels/transcript/toolcall/init(id:toolname:arguments:))

#### Inspecting a tool call

- [var arguments: GeneratedContent](/documentation/foundationmodels/transcript/toolcall/arguments)
- [var toolName: String](/documentation/foundationmodels/transcript/toolcall/toolname)
- [Transcript.ToolCalls](/documentation/foundationmodels/transcript/toolcalls)

#### Creating a tool calls

- [init<S>(id: String, S)](/documentation/foundationmodels/transcript/toolcalls/init(id:_:))
- [Transcript.ToolDefinition](/documentation/foundationmodels/transcript/tooldefinition)

#### Creating a tool definition

- [init(name: String, description: String, parameters: GenerationSchema)](/documentation/foundationmodels/transcript/tooldefinition/init(name:description:parameters:))
- [init(tool: some Tool)](/documentation/foundationmodels/transcript/tooldefinition/init(tool:))

#### Inspecting a tool definition

- [var description: String](/documentation/foundationmodels/transcript/tooldefinition/description)
- [var name: String](/documentation/foundationmodels/transcript/tooldefinition/name)
- [Transcript.ToolOutput](/documentation/foundationmodels/transcript/tooloutput)

#### Creating a tool output

- [init(id: String, toolName: String, segments: [Transcript.Segment])](/documentation/foundationmodels/transcript/tooloutput/init(id:toolname:segments:))

#### Inspecting a tool output

- [var id: String](/documentation/foundationmodels/transcript/tooloutput/id)
- [var segments: [Transcript.Segment]](/documentation/foundationmodels/transcript/tooloutput/segments)
- [var toolName: String](/documentation/foundationmodels/transcript/tooloutput/toolname)
- [GenerationOptions](/documentation/foundationmodels/generationoptions)

### Creating options

- [init(sampling: GenerationOptions.SamplingMode?, temperature: Double?, maximumResponseTokens: Int?)](/documentation/foundationmodels/generationoptions/init(sampling:temperature:maximumresponsetokens:))

### Configuring the response tokens

- [var maximumResponseTokens: Int?](/documentation/foundationmodels/generationoptions/maximumresponsetokens)

### Configuring the sampling mode

- [var sampling: GenerationOptions.SamplingMode?](/documentation/foundationmodels/generationoptions/sampling)
- [GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode)

#### Sampling options

- [static var greedy: GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode/greedy)
- [static func random(probabilityThreshold: Double, seed: UInt64?) -> GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode/random(probabilitythreshold:seed:))
- [static func random(top: Int, seed: UInt64?) -> GenerationOptions.SamplingMode](/documentation/foundationmodels/generationoptions/samplingmode/random(top:seed:))

### Configuring the temperature

- [var temperature: Double?](/documentation/foundationmodels/generationoptions/temperature)

## Guided generation

- [Generating Swift data structures with guided generation](/documentation/foundationmodels/generating-swift-data-structures-with-guided-generation)
- [Generable](/documentation/foundationmodels/generable)

### Defining a generable type

- [macro Generable(description: String?)](/documentation/foundationmodels/generable(description:))

### Creating a guide

- [macro Guide(description: String)](/documentation/foundationmodels/guide(description:))
- [macro Guide(description:_:)](/documentation/foundationmodels/guide(description:_:))
- [GenerationGuide](/documentation/foundationmodels/generationguide)

#### Getting the pattern

- [static func pattern<Output>(Regex<Output>) -> GenerationGuide<String>](/documentation/foundationmodels/generationguide/pattern(_:))

#### Getting the element

- [static func element<Element>(GenerationGuide<Element>) -> GenerationGuide<[Element]>](/documentation/foundationmodels/generationguide/element(_:))

#### Getting the count

- [static count(_:)](/documentation/foundationmodels/generationguide/count(_:))

#### Getting the constant

- [static func constant(String) -> GenerationGuide<String>](/documentation/foundationmodels/generationguide/constant(_:))
- [static func anyOf([String]) -> GenerationGuide<String>](/documentation/foundationmodels/generationguide/anyof(_:))

#### Getting a range

- [static range(_:)](/documentation/foundationmodels/generationguide/range(_:))

#### Getting the minimum value

- [static minimum(_:)](/documentation/foundationmodels/generationguide/minimum(_:))
- [static func minimumCount<Element>(Int) -> GenerationGuide<[Element]>](/documentation/foundationmodels/generationguide/minimumcount(_:))

#### Getting the maximum value

- [static maximum(_:)](/documentation/foundationmodels/generationguide/maximum(_:))
- [static func maximumCount<Element>(Int) -> GenerationGuide<[Element]>](/documentation/foundationmodels/generationguide/maximumcount(_:))

### Getting the schema

- [static var generationSchema: GenerationSchema](/documentation/foundationmodels/generable/generationschema)
- [GenerationSchema](/documentation/foundationmodels/generationschema)

#### Creating a generation schema

- [init(root: DynamicGenerationSchema, dependencies: [DynamicGenerationSchema]) throws](/documentation/foundationmodels/generationschema/init(root:dependencies:))
- [init(type:description:anyOf:)](/documentation/foundationmodels/generationschema/init(type:description:anyof:))
- [init(type: any Generable.Type, description: String?, properties: [GenerationSchema.Property])](/documentation/foundationmodels/generationschema/init(type:description:properties:))
- [GenerationSchema.Property](/documentation/foundationmodels/generationschema/property)

##### Creating a property

- [init(name:description:type:guides:)](/documentation/foundationmodels/generationschema/property/init(name:description:type:guides:))

#### Getting the debug description

- [var debugDescription: String](/documentation/foundationmodels/generationschema/debugdescription)

#### Getting the generation schema error types

- [GenerationSchema.SchemaError](/documentation/foundationmodels/generationschema/schemaerror)

##### Getting schema errors

- [case duplicateProperty(schema: String, property: String, context: GenerationSchema.SchemaError.Context)](/documentation/foundationmodels/generationschema/schemaerror/duplicateproperty(schema:property:context:))
- [case duplicateType(schema: String?, type: String, context: GenerationSchema.SchemaError.Context)](/documentation/foundationmodels/generationschema/schemaerror/duplicatetype(schema:type:context:))
- [case emptyTypeChoices(schema: String, context: GenerationSchema.SchemaError.Context)](/documentation/foundationmodels/generationschema/schemaerror/emptytypechoices(schema:context:))
- [case undefinedReferences(schema: String?, references: [String], context: GenerationSchema.SchemaError.Context)](/documentation/foundationmodels/generationschema/schemaerror/undefinedreferences(schema:references:context:))
- [GenerationSchema.SchemaError.Context](/documentation/foundationmodels/generationschema/schemaerror/context)

###### Creating a schema error context

- [init(debugDescription: String)](/documentation/foundationmodels/generationschema/schemaerror/context/init(debugdescription:))

###### Getting the debug description

- [let debugDescription: String](/documentation/foundationmodels/generationschema/schemaerror/context/debugdescription)

##### Getting the error description

- [var errorDescription: String?](/documentation/foundationmodels/generationschema/schemaerror/errordescription)

##### Getting the recovery suggestion

- [var recoverySuggestion: String?](/documentation/foundationmodels/generationschema/schemaerror/recoverysuggestion)

### Generating a unique identifier

- [GenerationID](/documentation/foundationmodels/generationid)

#### Creating an identifier

- [init()](/documentation/foundationmodels/generationid/init())

### Converting to partially generated

- [func asPartiallyGenerated() -> Self.PartiallyGenerated](/documentation/foundationmodels/generable/aspartiallygenerated())
- [PartiallyGenerated](/documentation/foundationmodels/generable/partiallygenerated)

### Generate dynamic shemas

- [DynamicGenerationSchema](/documentation/foundationmodels/dynamicgenerationschema)

#### Creating a dynamic schema

- [init(arrayOf: DynamicGenerationSchema, minimumElements: Int?, maximumElements: Int?)](/documentation/foundationmodels/dynamicgenerationschema/init(arrayof:minimumelements:maximumelements:))
- [init(name:description:anyOf:)](/documentation/foundationmodels/dynamicgenerationschema/init(name:description:anyof:))
- [init(name: String, description: String?, properties: [DynamicGenerationSchema.Property])](/documentation/foundationmodels/dynamicgenerationschema/init(name:description:properties:))
- [init(referenceTo: String)](/documentation/foundationmodels/dynamicgenerationschema/init(referenceto:))
- [init<Value>(type: Value.Type, guides: [GenerationGuide<Value>])](/documentation/foundationmodels/dynamicgenerationschema/init(type:guides:))
- [DynamicGenerationSchema.Property](/documentation/foundationmodels/dynamicgenerationschema/property)

##### Creating a property

- [init(name: String, description: String?, schema: DynamicGenerationSchema, isOptional: Bool)](/documentation/foundationmodels/dynamicgenerationschema/property/init(name:description:schema:isoptional:))

## Tool calling

- [Expanding generation with tool calling](/documentation/foundationmodels/expanding-generation-with-tool-calling)
- [Generate dynamic game content with guided generation and tools](/documentation/foundationmodels/generate-dynamic-game-content-with-guided-generation-and-tools)
- [Tool](/documentation/foundationmodels/tool)

### Invoking a tool

- [func call(arguments: Self.Arguments) async throws -> Self.Output](/documentation/foundationmodels/tool/call(arguments:))
- [Arguments](/documentation/foundationmodels/tool/arguments)
- [Output](/documentation/foundationmodels/tool/output)

### Getting the tool properties

- [var description: String](/documentation/foundationmodels/tool/description)
- [var includesSchemaInInstructions: Bool](/documentation/foundationmodels/tool/includesschemaininstructions)
- [var name: String](/documentation/foundationmodels/tool/name)
- [var parameters: GenerationSchema](/documentation/foundationmodels/tool/parameters)

## Feedback

- [LanguageModelFeedback](/documentation/foundationmodels/languagemodelfeedback)

### Creating feedback

- [LanguageModelFeedback.Issue](/documentation/foundationmodels/languagemodelfeedback/issue)

#### Initializing an issue

- [init(category: LanguageModelFeedback.Issue.Category, explanation: String?)](/documentation/foundationmodels/languagemodelfeedback/issue/init(category:explanation:))
- [LanguageModelFeedback.Issue.Category](/documentation/foundationmodels/languagemodelfeedback/issue/category)

##### Getting the issue category

- [case didNotFollowInstructions](/documentation/foundationmodels/languagemodelfeedback/issue/category/didnotfollowinstructions)
- [case incorrect](/documentation/foundationmodels/languagemodelfeedback/issue/category/incorrect)
- [case stereotypeOrBias](/documentation/foundationmodels/languagemodelfeedback/issue/category/stereotypeorbias)
- [case suggestiveOrSexual](/documentation/foundationmodels/languagemodelfeedback/issue/category/suggestiveorsexual)
- [case tooVerbose](/documentation/foundationmodels/languagemodelfeedback/issue/category/tooverbose)
- [case triggeredGuardrailUnexpectedly](/documentation/foundationmodels/languagemodelfeedback/issue/category/triggeredguardrailunexpectedly)
- [case unhelpful](/documentation/foundationmodels/languagemodelfeedback/issue/category/unhelpful)
- [case vulgarOrOffensive](/documentation/foundationmodels/languagemodelfeedback/issue/category/vulgaroroffensive)
- [LanguageModelFeedback.Sentiment](/documentation/foundationmodels/languagemodelfeedback/sentiment)

#### Getting sentiment

- [case negative](/documentation/foundationmodels/languagemodelfeedback/sentiment/negative)
- [case neutral](/documentation/foundationmodels/languagemodelfeedback/sentiment/neutral)
- [case positive](/documentation/foundationmodels/languagemodelfeedback/sentiment/positive)
- [func logFeedbackAttachment(sentiment: LanguageModelFeedback.Sentiment?, issues: [LanguageModelFeedback.Issue], desiredOutput: Transcript.Entry?) -> Data](/documentation/foundationmodels/languagemodelsession/logfeedbackattachment(sentiment:issues:desiredoutput:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
