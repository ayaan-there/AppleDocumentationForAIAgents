# Core Transferable Documentation

Source: https://sosumi.ai/documentation/coretransferable

---
title: Core Transferable
source: https://developer.apple.com/documentation/coretransferable
timestamp: 2026-02-13T18:55:48.287Z
---

## Essentials

- [Transferable](/documentation/coretransferable/transferable)

### Implementing a transfer representation

- [static var transferRepresentation: Self.Representation](/documentation/coretransferable/transferable/transferrepresentation)
- [Representation](/documentation/coretransferable/transferable/representation)

### Initializers

- [init(importing: URL, contentType: UTType?) async throws](/documentation/coretransferable/transferable/init(importing:contenttype:)-4pfpm)
- [init(importing: Data, contentType: UTType?) async throws](/documentation/coretransferable/transferable/init(importing:contenttype:)-74t08)

### Instance Properties

- [var suggestedFilename: String?](/documentation/coretransferable/transferable/suggestedfilename)

### Instance Methods

- [func export(to: URL, contentType: UTType?) async throws -> URL](/documentation/coretransferable/transferable/export(to:contenttype:))
- [func exported(as: UTType?) async throws -> Data](/documentation/coretransferable/transferable/exported(as:))
- [func exportedContentTypes(TransferRepresentationVisibility) -> [UTType]](/documentation/coretransferable/transferable/exportedcontenttypes(_:))
- [func importedContentTypes() -> [UTType]](/documentation/coretransferable/transferable/importedcontenttypes()-swift.method)
- [func withExportedFile<Result>(contentType: UTType?, fileHandler: (URL) async throws -> Result) async throws -> Result](/documentation/coretransferable/transferable/withexportedfile(contenttype:filehandler:))

### Type Methods

- [static func exportedContentTypes(visibility: TransferRepresentationVisibility) -> [UTType]](/documentation/coretransferable/transferable/exportedcontenttypes(visibility:))
- [static func importedContentTypes() -> [UTType]](/documentation/coretransferable/transferable/importedcontenttypes()-swift.type.method)
- [TransferRepresentation](/documentation/coretransferable/transferrepresentation)

### Implementing a transfer representation

- [var body: Self.Body](/documentation/coretransferable/transferrepresentation/body-swift.property)
- [Body](/documentation/coretransferable/transferrepresentation/body-swift.associatedtype)
- [Item](/documentation/coretransferable/transferrepresentation/item)

### Configuring exports

- [func exportingCondition((Self.Item) -> Bool) -> _ConditionalTransferRepresentation<Self>](/documentation/coretransferable/transferrepresentation/exportingcondition(_:))

### Controlling visibility

- [func visibility(TransferRepresentationVisibility) -> some TransferRepresentation<Self.Item>
](/documentation/coretransferable/transferrepresentation/visibility(_:))

### Instance Methods

- [func suggestedFileName(String) -> some TransferRepresentation<Self.Item>
](/documentation/coretransferable/transferrepresentation/suggestedfilename(_:)-2yln2)
- [func suggestedFileName((Self.Item) -> String?) -> some TransferRepresentation<Self.Item>
](/documentation/coretransferable/transferrepresentation/suggestedfilename(_:)-47rg0)
- [Choosing a transfer representation for a model type](/documentation/coretransferable/choosing-a-transfer-representation-for-a-model-type)

## Data transfer

- [CodableRepresentation](/documentation/coretransferable/codablerepresentation)

### Creating a transfer representation

- [init(for: Item.Type, contentType: UTType)](/documentation/coretransferable/codablerepresentation/init(for:contenttype:))
- [init(for: Item.Type, contentType: UTType, encoder: Encoder, decoder: Decoder)](/documentation/coretransferable/codablerepresentation/init(for:contenttype:encoder:decoder:))
- [DataRepresentation](/documentation/coretransferable/datarepresentation)

### Creating a transfer representation

- [init(contentType: UTType, exporting: (Item) async throws -> Data, importing: (Data) async throws -> Item)](/documentation/coretransferable/datarepresentation/init(contenttype:exporting:importing:))
- [init(importedContentType: UTType, importing: (Data) async throws -> Item)](/documentation/coretransferable/datarepresentation/init(importedcontenttype:importing:))
- [init(exportedContentType: UTType, exporting: (Item) async throws -> Data)](/documentation/coretransferable/datarepresentation/init(exportedcontenttype:exporting:))

## File transfer

- [FileRepresentation](/documentation/coretransferable/filerepresentation)

### Creating a transfer representation

- [init(contentType: UTType, shouldAttemptToOpenInPlace: Bool, exporting: (Item) async throws -> SentTransferredFile, importing: (ReceivedTransferredFile) async throws -> Item)](/documentation/coretransferable/filerepresentation/init(contenttype:shouldattempttoopeninplace:exporting:importing:))
- [init(importedContentType: UTType, shouldAttemptToOpenInPlace: Bool, importing: (ReceivedTransferredFile) async throws -> Item)](/documentation/coretransferable/filerepresentation/init(importedcontenttype:shouldattempttoopeninplace:importing:))
- [init(exportedContentType: UTType, shouldAllowToOpenInPlace: Bool, exporting: (Item) async throws -> SentTransferredFile)](/documentation/coretransferable/filerepresentation/init(exportedcontenttype:shouldallowtoopeninplace:exporting:))
- [SentTransferredFile](/documentation/coretransferable/senttransferredfile)

### Configuring a file transfer

- [init(URL, allowAccessingOriginalFile: Bool)](/documentation/coretransferable/senttransferredfile/init(_:allowaccessingoriginalfile:))
- [let file: URL](/documentation/coretransferable/senttransferredfile/file)
- [let allowAccessingOriginalFile: Bool](/documentation/coretransferable/senttransferredfile/allowaccessingoriginalfile)
- [ReceivedTransferredFile](/documentation/coretransferable/receivedtransferredfile)

### Configuring a file transfer

- [let file: URL](/documentation/coretransferable/receivedtransferredfile/file)
- [let isOriginalFile: Bool](/documentation/coretransferable/receivedtransferredfile/isoriginalfile)

## Transfer customization

- [ProxyRepresentation](/documentation/coretransferable/proxyrepresentation)

### Initializers

- [init(exporting: (Item) async throws -> ProxyRepresentation)](/documentation/coretransferable/proxyrepresentation/init(exporting:)-6gjdh)
- [init(exporting: (Item) throws -> ProxyRepresentation)](/documentation/coretransferable/proxyrepresentation/init(exporting:)-q3qp)
- [init(exporting: (Item) throws -> ProxyRepresentation, importing: (ProxyRepresentation) throws -> Item)](/documentation/coretransferable/proxyrepresentation/init(exporting:importing:)-4aiur)
- [init(exporting: (Item) async throws -> ProxyRepresentation, importing: (ProxyRepresentation) async throws -> Item)](/documentation/coretransferable/proxyrepresentation/init(exporting:importing:)-8q8zv)
- [init(exporting: (Item) throws -> ProxyRepresentation, importing: (ProxyRepresentation) async throws -> Item)](/documentation/coretransferable/proxyrepresentation/init(exporting:importing:)-h69f)
- [init(importing: (ProxyRepresentation) async throws -> Item)](/documentation/coretransferable/proxyrepresentation/init(importing:)-4w9l5)
- [init(importing: (ProxyRepresentation) throws -> Item)](/documentation/coretransferable/proxyrepresentation/init(importing:)-pq40)
- [TransferRepresentationVisibility](/documentation/coretransferable/transferrepresentationvisibility)

### Specifying transfer visibility

- [static let all: TransferRepresentationVisibility](/documentation/coretransferable/transferrepresentationvisibility/all)
- [static let team: TransferRepresentationVisibility](/documentation/coretransferable/transferrepresentationvisibility/team)
- [static let group: TransferRepresentationVisibility](/documentation/coretransferable/transferrepresentationvisibility/group)
- [static let ownProcess: TransferRepresentationVisibility](/documentation/coretransferable/transferrepresentationvisibility/ownprocess)

## Supporting types

- [TransferRepresentationBuilder](/documentation/coretransferable/transferrepresentationbuilder)

### Building a transfer representation

- [static func buildBlock<Content>(Content) -> Content](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:))
- [static func buildExpression<R>(R) -> R](/documentation/coretransferable/transferrepresentationbuilder/buildexpression(_:)-3z8sl)
- [static func buildExpression<Encoder, Decoder>(CodableRepresentation<Item, Encoder, Decoder>) -> CodableRepresentation<Item, Encoder, Decoder>](/documentation/coretransferable/transferrepresentationbuilder/buildexpression(_:)-6qtdp)

### Combining transfer representations

- [static func buildBlock<C1, C2>(C1, C2) -> TupleTransferRepresentation<Item, (C1, C2)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:))
- [static func buildBlock<C1, C2, C3>(C1, C2, C3) -> TupleTransferRepresentation<Item, (C1, C2, C3)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:))
- [static func buildBlock<C1, C2, C3, C4>(C1, C2, C3, C4) -> TupleTransferRepresentation<Item, (C1, C2, C3, C4)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:_:))
- [static func buildBlock<C1, C2, C3, C4, C5>(C1, C2, C3, C4, C5) -> TupleTransferRepresentation<Item, (C1, C2, C3, C4, C5)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:_:_:))
- [static func buildBlock<C1, C2, C3, C4, C5, C6>(C1, C2, C3, C4, C5, C6) -> TupleTransferRepresentation<Item, (C1, C2, C3, C4, C5, C6)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:_:_:_:))
- [static func buildBlock<C1, C2, C3, C4, C5, C6, C7>(C1, C2, C3, C4, C5, C6, C7) -> TupleTransferRepresentation<Item, (C1, C2, C3, C4, C5, C6, C7)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:_:_:_:_:))
- [static func buildBlock<C1, C2, C3, C4, C5, C6, C7, C8>(C1, C2, C3, C4, C5, C6, C7, C8) -> TupleTransferRepresentation<Item, (C1, C2, C3, C4, C5, C6, C7, C8)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static func buildBlock<C1, C2, C3, C4, C5, C6, C7, C8, C9>(C1, C2, C3, C4, C5, C6, C7, C8, C9) -> TupleTransferRepresentation<Item, (C1, C2, C3, C4, C5, C6, C7, C8, C9)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<C1, C2, C3, C4, C5, C6, C7, C8, C9, C10>(C1, C2, C3, C4, C5, C6, C7, C8, C9, C10) -> TupleTransferRepresentation<Item, (C1, C2, C3, C4, C5, C6, C7, C8, C9, C10)>](/documentation/coretransferable/transferrepresentationbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))
- [TupleTransferRepresentation](/documentation/coretransferable/tupletransferrepresentation)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
