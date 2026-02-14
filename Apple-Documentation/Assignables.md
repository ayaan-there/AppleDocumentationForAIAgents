# Assignables Documentation

Source: https://sosumi.ai/documentation/assignables

---
title: Assignables
source: https://developer.apple.com/documentation/assignables
timestamp: 2026-02-13T18:53:56.355Z
---

## Assignable document

- [AssignableDocument](/documentation/assignables/assignabledocument)

### Creating an assignable document

- [init(pdfURL: URL, id: String?) throws](/documentation/assignables/assignabledocument/init(pdfurl:id:))
- [init(id: AssignableDocument.ID, partData: [AssignableDocument.PartID : MergeablePartData]) async throws](/documentation/assignables/assignabledocument/init(id:partdata:)-8gf6g)
- [MergeablePartData](/documentation/assignables/mergeablepartdata)

#### Enumeration Cases

- [case data(Data)](/documentation/assignables/mergeablepartdata/data(_:))
- [case fileURL(URL)](/documentation/assignables/mergeablepartdata/fileurl(_:))
- [init(id: AssignableDocument.ID, partData: [AssignableDocument.PartID : URL]) throws](/documentation/assignables/assignabledocument/init(id:partdata:)-4am19)
- [init(pdfURL: URL, authors: [some UserIdentity], id: String?) throws](/documentation/assignables/assignabledocument/init(pdfurl:authors:id:))

### Inspecting an assignable document

- [AssignableDocument.ID](/documentation/assignables/assignabledocument/id-swift.typealias)
- [var id: AssignableDocument.ID](/documentation/assignables/assignabledocument/id-swift.property)
- [var isMultiPageDocument: Bool](/documentation/assignables/assignabledocument/ismultipagedocument)
- [var isPartial: Bool](/documentation/assignables/assignabledocument/ispartial)
- [AssignableDocument.PartIDs](/documentation/assignables/assignabledocument/partids-swift.enum)

#### Layer types

- [static let all: [MergeablePartsContainerPartID]](/documentation/assignables/assignabledocument/partids-swift.enum/all)
- [static let authors: MergeablePartsContainerPartID](/documentation/assignables/assignabledocument/partids-swift.enum/authors)
- [static let base: MergeablePartsContainerPartID](/documentation/assignables/assignabledocument/partids-swift.enum/base)
- [static let instructionMarkup: MergeablePartsContainerPartID](/documentation/assignables/assignabledocument/partids-swift.enum/instructionmarkup)
- [static let questionBoxes: MergeablePartsContainerPartID](/documentation/assignables/assignabledocument/partids-swift.enum/questionboxes)

#### Getting the document type

- [AssignableDocument.PartIDs.Document](/documentation/assignables/assignabledocument/partids-swift.enum/document)
- [var partIDs: [AssignableDocument.PartID]](/documentation/assignables/assignabledocument/partids-swift.property)
- [AssignableDocument.Question](/documentation/assignables/assignabledocument/question)

#### Creating a question

- [init(pageID: AssignableDocument.Page.ID, boxes: [AssignableDocument.QuestionBox], maxScore: Double?)](/documentation/assignables/assignabledocument/question/init(pageid:boxes:maxscore:))

#### Inspecting a question

- [var boxes: [AssignableDocument.QuestionBox]](/documentation/assignables/assignabledocument/question/boxes)
- [AssignableDocument.Question.ID](/documentation/assignables/assignabledocument/question/id-swift.typealias)
- [var id: AssignableDocument.Question.ID](/documentation/assignables/assignabledocument/question/id-swift.property)
- [var maxScore: Double?](/documentation/assignables/assignabledocument/question/maxscore)
- [AssignableDocument.Question.Thumbnail](/documentation/assignables/assignabledocument/question/thumbnail)

##### Inspecting a thumbnail

- [AssignableDocument.Question.Thumbnail.Data](/documentation/assignables/assignabledocument/question/thumbnail/data-swift.struct)

###### Inspecting thumbnail data

- [var box: AssignableDocument.QuestionBox](/documentation/assignables/assignabledocument/question/thumbnail/data-swift.struct/box)
- [var image: UIImage](/documentation/assignables/assignabledocument/question/thumbnail/data-swift.struct/image)
- [var pageID: AssignableDocument.Page.ID](/documentation/assignables/assignabledocument/question/thumbnail/data-swift.struct/pageid)
- [var data: AssignableDocument.Question.Thumbnail.Data?](/documentation/assignables/assignabledocument/question/thumbnail/data-swift.property)
- [var questionID: AssignableDocument.Question.ID](/documentation/assignables/assignabledocument/question/thumbnail/questionid)
- [AssignableDocument.Question.Document](/documentation/assignables/assignabledocument/question/document)

#### Comparing questions

- [static func == (AssignableDocument.Question, AssignableDocument.Question) -> Bool](/documentation/assignables/assignabledocument/question/==(_:_:))

#### Hashing a question

- [func hash(into: inout Hasher)](/documentation/assignables/assignabledocument/question/hash(into:))

#### Initializers

- [init(boxes: [AssignableDocument.QuestionBox], maxScore: Double?)](/documentation/assignables/assignabledocument/question/init(boxes:maxscore:))
- [AssignableDocument.QuestionBox](/documentation/assignables/assignabledocument/questionbox)

#### Operators

- [static func == (AssignableDocument.QuestionBox, AssignableDocument.QuestionBox) -> Bool](/documentation/assignables/assignabledocument/questionbox/==(_:_:))

#### Initializers

- [init(id: AssignableDocument.QuestionBox.ID, pageID: AssignableDocument.Page.ID, bounds: CGRect)](/documentation/assignables/assignabledocument/questionbox/init(id:pageid:bounds:))

#### Instance Properties

- [var bounds: CGRect](/documentation/assignables/assignabledocument/questionbox/bounds)
- [var id: AssignableDocument.QuestionBox.ID](/documentation/assignables/assignabledocument/questionbox/id-swift.property)
- [var pageID: AssignableDocument.Page.ID?](/documentation/assignables/assignabledocument/questionbox/pageid)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/assignables/assignabledocument/questionbox/hash(into:))

#### Type Aliases

- [AssignableDocument.QuestionBox.Document](/documentation/assignables/assignabledocument/questionbox/document)
- [AssignableDocument.QuestionBox.ID](/documentation/assignables/assignabledocument/questionbox/id-swift.typealias)
- [var questions: [AssignableDocument.Question]](/documentation/assignables/assignabledocument/questions)
- [AssignableDocument.Element](/documentation/assignables/assignabledocument/element)
- [var pagesDebugDescription: String](/documentation/assignables/assignabledocument/pagesdebugdescription)
- [AssignableDocument.Error](/documentation/assignables/assignabledocument/error)

#### Document errors

- [case invalidURL](/documentation/assignables/assignabledocument/error/invalidurl)
- [case otherDocumentIsNotAVariant](/documentation/assignables/assignabledocument/error/otherdocumentisnotavariant)

#### Enumeration Cases

- [case exportFailed(partIDs: [AssignableDocument.PartID])](/documentation/assignables/assignabledocument/error/exportfailed(partids:))

### Getting and setting the questions

- [func appendQuestion(pageID: AssignableDocument.Page.ID, rect: CGRect, maxScore: Double?) -> AssignableDocument.Question.ID](/documentation/assignables/assignabledocument/appendquestion(pageid:rect:maxscore:))
- [func questions(on: AssignableDocument.Page.ID) -> [AssignableDocument.Question]](/documentation/assignables/assignabledocument/questions(on:))
- [func removeQuestion(AssignableDocument.Question.ID) -> AssignableDocument.Question?](/documentation/assignables/assignabledocument/removequestion(_:))

### Computing the max score

- [func computeMaxScore(defaultQuestionMaxScore: Double?) -> Double?](/documentation/assignables/assignabledocument/computemaxscore(defaultquestionmaxscore:))

### Getting the authors

- [var authors: [AnyUserIdentity]](/documentation/assignables/assignabledocument/authors)

### Getting the configuration

- [AssignableDocument.Configuration](/documentation/assignables/assignabledocument/configuration-swift.typealias)
- [var configuration: some AssignableDocumentConfiguration](/documentation/assignables/assignabledocument/configuration-swift.property)
- [AssignableDocument.CorrectMarkType](/documentation/assignables/assignabledocument/correctmarktype)

#### Mark types

- [case checkmark](/documentation/assignables/assignabledocument/correctmarktype/checkmark)
- [case numeric](/documentation/assignables/assignabledocument/correctmarktype/numeric)
- [case star](/documentation/assignables/assignabledocument/correctmarktype/star)
- [case unknown](/documentation/assignables/assignabledocument/correctmarktype/unknown)

#### Inspecting a type

- [var debugDescription: String](/documentation/assignables/assignabledocument/correctmarktype/debugdescription)
- [var id: AssignableDocument.CorrectMarkType](/documentation/assignables/assignabledocument/correctmarktype/id)

### Merging the parts

- [func merge(AssignableDocument) async throws -> Bool](/documentation/assignables/assignabledocument/merge(_:))
- [func merge(partData: MergeablePartData, into: AssignableDocument.PartID) async throws -> Bool](/documentation/assignables/assignabledocument/merge(partdata:into:))
- [func merge(other: AssignableDocument) throws -> Bool](/documentation/assignables/assignabledocument/merge(other:))
- [func merge(partID: AssignableDocument.PartID, partDataURL: URL) throws -> Bool](/documentation/assignables/assignabledocument/merge(partid:partdataurl:))

### Producing thumbnails

- [func questionThumbnails(visibleParts: [AssignableDocument.PartID]) async -> [AssignableDocument.Question.ID : [AssignableDocument.Question.Thumbnail]]](/documentation/assignables/assignabledocument/questionthumbnails(visibleparts:))

### Making the parts

- [func makePart(for: AssignableDocument.PartID) throws -> MergeablePartData?](/documentation/assignables/assignabledocument/makepart(for:))

### Exporting the parts

- [func exportBaseAsPDF() async -> PDFDocument](/documentation/assignables/assignabledocument/exportbaseaspdf())
- [func exportParts(identifiedBy: [AssignableDocument.PartID]) async throws -> [AssignableDocument.PartID : MergeablePartData]](/documentation/assignables/assignabledocument/exportparts(identifiedby:))
- [func export(partIDs: [AssignableDocument.PartID]) async throws -> [AssignableDocument.PartID : URL]](/documentation/assignables/assignabledocument/export(partids:))

### Accessing documents

- [subscript(AssignableDocument.Page.ID) -> AssignableDocument.Page?](/documentation/assignables/assignabledocument/subscript(_:)-8ou91)
- [subscript(AssignableDocument.QuestionBox.ID) -> AssignableDocument.QuestionBox?](/documentation/assignables/assignabledocument/subscript(_:)-68enn)
- [subscript(AssignableDocument.Question.ID) -> AssignableDocument.Question?](/documentation/assignables/assignabledocument/subscript(_:)-7fijz)

### Comparing assignable documents

- [static func == (AssignableDocument, AssignableDocument) -> Bool](/documentation/assignables/assignabledocument/==(_:_:))

### Hashing the assignable document

- [func hash(into: inout Hasher)](/documentation/assignables/assignabledocument/hash(into:))

### Default Implementations

- [Assignable Implementations](/documentation/assignables/assignabledocument/assignable-implementations)

#### Instance Methods

- [func assign(to: AnyUserIdentity) throws -> AssignedWorkDocument](/documentation/assignables/assignabledocument/assign(to:))
- [func makeAssignedWorkDocument() throws -> AssignedWorkDocument](/documentation/assignables/assignabledocument/makeassignedworkdocument())
- [func makeAssignedWorkDocument(id: String) throws -> AssignedWorkDocument](/documentation/assignables/assignabledocument/makeassignedworkdocument(id:))
- [MergeableDocument Implementations](/documentation/assignables/assignabledocument/mergeabledocument-implementations)

#### Structures

- [AssignableDocument.Page](/documentation/assignables/assignabledocument/page)

##### Inspecting a page

- [AssignableDocument.Page.ID](/documentation/assignables/assignabledocument/page/id-swift.struct)

###### Creating a page identifier

- [AssignableDocument.Element](/documentation/assignables/assignabledocument/element)
- [var id: AssignableDocument.Page.ID](/documentation/assignables/assignabledocument/page/id-swift.property)
- [var size: CGSize](/documentation/assignables/assignabledocument/page/size)
- [AssignableDocument.Page.Document](/documentation/assignables/assignabledocument/page/document)

##### Comparing pages

- [static func == (AssignableDocument.Page, AssignableDocument.Page) -> Bool](/documentation/assignables/assignabledocument/page/==(_:_:))

##### Hashing a page

- [func hash(into: inout Hasher)](/documentation/assignables/assignabledocument/page/hash(into:))

##### Instance Properties

- [var rotation: Measurement<UnitAngle>](/documentation/assignables/assignabledocument/page/rotation)

#### Instance Properties

- [var pages: [AssignableDocument.Page]](/documentation/assignables/assignabledocument/pages)

#### Instance Methods

- [func exportToPDF(visibleParts: [MergeablePartsContainerPartID]) async -> PDFDocument](/documentation/assignables/assignabledocument/exporttopdf(visibleparts:))
- [AssignedWorkDocument](/documentation/assignables/assignedworkdocument)

### Creating an assigned work document

- [init(id: AssignedWorkDocument.ID, assignableDocument: AssignableDocument, partData: [AssignedWorkDocument.PartID : MergeablePartData]) async throws](/documentation/assignables/assignedworkdocument/init(id:assignabledocument:partdata:)-8eh38)
- [init(id: AssignedWorkDocument.ID, assignableDocument: AssignableDocument, partData: [AssignedWorkDocument.PartID : URL]) throws](/documentation/assignables/assignedworkdocument/init(id:assignabledocument:partdata:)-54yg5)

### Inspecting a work document

- [AssignedWorkDocument.ID](/documentation/assignables/assignedworkdocument/id-swift.typealias)
- [var id: AssignedWorkDocument.ID](/documentation/assignables/assignedworkdocument/id-swift.property)
- [var isMultiPageDocument: Bool](/documentation/assignables/assignedworkdocument/ismultipagedocument)
- [var isPartial: Bool](/documentation/assignables/assignedworkdocument/ispartial)
- [AssignedWorkDocument.PartIDs](/documentation/assignables/assignedworkdocument/partids-swift.enum)

#### Layer types

- [static let all: [MergeablePartsContainerPartID]](/documentation/assignables/assignedworkdocument/partids-swift.enum/all)
- [static let assignableDocumentAuthors: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/assignabledocumentauthors)
- [static let assignableDocumentBase: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/assignabledocumentbase)
- [static let assignableDocumentInstructionMarkup: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/assignabledocumentinstructionmarkup)
- [static let assignableDocumentQuestionBoxes: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/assignabledocumentquestionboxes)
- [static let assignees: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/assignees)
- [static let scoreAnnotations: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/scoreannotations)
- [static let scorerMarkup: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/scorermarkup)
- [static let scorers: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/scorers)
- [static let takerMarkup: MergeablePartsContainerPartID](/documentation/assignables/assignedworkdocument/partids-swift.enum/takermarkup)

#### Getting the document type

- [AssignedWorkDocument.PartIDs.Document](/documentation/assignables/assignedworkdocument/partids-swift.enum/document)
- [var partIDs: [MergeablePartsContainerPartID]](/documentation/assignables/assignedworkdocument/partids-swift.property)
- [var scoreAnnotations: [AssignedWorkDocument.ScoreAnnotation]](/documentation/assignables/assignedworkdocument/scoreannotations)
- [var scorers: [AnyUserIdentity]](/documentation/assignables/assignedworkdocument/scorers)
- [var pagesDebugDescription: String](/documentation/assignables/assignedworkdocument/pagesdebugdescription)
- [AssignedWorkDocument.Error](/documentation/assignables/assignedworkdocument/error)

#### Variant error

- [case otherDocumentIsNotAVariant](/documentation/assignables/assignedworkdocument/error/otherdocumentisnotavariant)

#### Enumeration Cases

- [case exportFailed(partIDs: [AssignedWorkDocument.PartID])](/documentation/assignables/assignedworkdocument/error/exportfailed(partids:))

### Getting the assignable document

- [var assignableDocument: AssignableDocument](/documentation/assignables/assignedworkdocument/assignabledocument)

### Getting the assignees

- [var assignees: [AnyUserIdentity]](/documentation/assignables/assignedworkdocument/assignees)

### Getting the configuration

- [AssignedWorkDocument.Configuration](/documentation/assignables/assignedworkdocument/configuration-swift.typealias)
- [var configuration: any AssignedWorkDocumentConfiguration](/documentation/assignables/assignedworkdocument/configuration-swift.property)

### Merging the parts

- [func merge(AssignedWorkDocument) async throws -> Bool](/documentation/assignables/assignedworkdocument/merge(_:))
- [func merge(partData: MergeablePartData, into: AssignedWorkDocument.PartID) async throws -> Bool](/documentation/assignables/assignedworkdocument/merge(partdata:into:))
- [func merge(other: AssignedWorkDocument) throws -> Bool](/documentation/assignables/assignedworkdocument/merge(other:))
- [func merge(partID: AssignedWorkDocument.PartID, partDataURL: URL) throws -> Bool](/documentation/assignables/assignedworkdocument/merge(partid:partdataurl:))

### Producing thumbnails

- [func questionThumbnails(visibleParts: [AssignedWorkDocument.PartID]) async -> [AssignableDocument.Question.ID : [AssignableDocument.Question.Thumbnail]]](/documentation/assignables/assignedworkdocument/questionthumbnails(visibleparts:))

### Computing the score

- [func computeScore() -> Double](/documentation/assignables/assignedworkdocument/computescore())
- [AssignedWorkDocument.ScoreAnnotation](/documentation/assignables/assignedworkdocument/scoreannotation)

#### Creating a score annotation

- [init(id: AssignedWorkDocument.ScoreAnnotation.ID, pageID: AssignedWorkDocument.Page.ID?, location: CGPoint, kind: AssignedWorkDocument.ScoreAnnotation.Kind)](/documentation/assignables/assignedworkdocument/scoreannotation/init(id:pageid:location:kind:))

#### Inspecting a score annotation

- [AssignedWorkDocument.ScoreAnnotation.ID](/documentation/assignables/assignedworkdocument/scoreannotation/id-swift.typealias)
- [var id: AssignedWorkDocument.ScoreAnnotation.ID](/documentation/assignables/assignedworkdocument/scoreannotation/id-swift.property)
- [AssignedWorkDocument.ScoreAnnotation.Kind](/documentation/assignables/assignedworkdocument/scoreannotation/kind-swift.enum)

##### Score annotations

- [case bonus](/documentation/assignables/assignedworkdocument/scoreannotation/kind-swift.enum/bonus)
- [case correct](/documentation/assignables/assignedworkdocument/scoreannotation/kind-swift.enum/correct)
- [case incorrect](/documentation/assignables/assignedworkdocument/scoreannotation/kind-swift.enum/incorrect)
- [case unknown](/documentation/assignables/assignedworkdocument/scoreannotation/kind-swift.enum/unknown)

##### Instance Properties

- [var debugDescription: String](/documentation/assignables/assignedworkdocument/scoreannotation/kind-swift.enum/debugdescription)
- [var kind: AssignedWorkDocument.ScoreAnnotation.Kind](/documentation/assignables/assignedworkdocument/scoreannotation/kind-swift.property)
- [var location: CGPoint](/documentation/assignables/assignedworkdocument/scoreannotation/location)
- [var pageID: AssignedWorkDocument.Page.ID?](/documentation/assignables/assignedworkdocument/scoreannotation/pageid)
- [AssignedWorkDocument.ScoreAnnotation.Document](/documentation/assignables/assignedworkdocument/scoreannotation/document)

#### Comparing score annotations

- [static func == (AssignedWorkDocument.ScoreAnnotation, AssignedWorkDocument.ScoreAnnotation) -> Bool](/documentation/assignables/assignedworkdocument/scoreannotation/==(_:_:))

#### Hashing the score annotation

- [func hash(into: inout Hasher)](/documentation/assignables/assignedworkdocument/scoreannotation/hash(into:))

### Making the parts

- [func makePart(for: AssignedWorkDocument.PartID) throws -> MergeablePartData?](/documentation/assignables/assignedworkdocument/makepart(for:))

### Exporting the parts

- [func exportParts(identifiedBy: [AssignedWorkDocument.PartID]) async throws -> [AssignedWorkDocument.PartID : MergeablePartData]](/documentation/assignables/assignedworkdocument/exportparts(identifiedby:))
- [func export(partIDs: [AssignedWorkDocument.PartID]) async throws -> [AssignedWorkDocument.PartID : URL]](/documentation/assignables/assignedworkdocument/export(partids:))

### Comparing work documents

- [static func == (AssignedWorkDocument, AssignedWorkDocument) -> Bool](/documentation/assignables/assignedworkdocument/==(_:_:))

### Hashing the work document

- [func hash(into: inout Hasher)](/documentation/assignables/assignedworkdocument/hash(into:))

### Accessing work documents

- [subscript(AssignedWorkDocument.Page.ID) -> AssignedWorkDocument.Page?](/documentation/assignables/assignedworkdocument/subscript(_:)-4srtw)
- [subscript(AssignedWorkDocument.ScoreAnnotation.ID) -> AssignedWorkDocument.ScoreAnnotation?](/documentation/assignables/assignedworkdocument/subscript(_:)-5h89c)

### Default Implementations

- [MergeableDocument Implementations](/documentation/assignables/assignedworkdocument/mergeabledocument-implementations)

#### Structures

- [AssignedWorkDocument.Page](/documentation/assignables/assignedworkdocument/page)

##### Inspecting the properties

- [var assignableDocumentPageID: AssignableDocument.Page.ID](/documentation/assignables/assignedworkdocument/page/assignabledocumentpageid)
- [AssignedWorkDocument.Page.ID](/documentation/assignables/assignedworkdocument/page/id-swift.struct)

###### Getting the page identifier

- [var assignableDocumentPageID: AssignableDocument.Page.ID](/documentation/assignables/assignedworkdocument/page/id-swift.struct/assignabledocumentpageid)
- [var id: AssignedWorkDocument.Page.ID](/documentation/assignables/assignedworkdocument/page/id-swift.property)
- [AssignedWorkDocument.Page.Document](/documentation/assignables/assignedworkdocument/page/document)

##### Hashing the page

- [func hash(into: inout Hasher)](/documentation/assignables/assignedworkdocument/page/hash(into:))

##### Comparing pages

- [static func == (AssignedWorkDocument.Page, AssignedWorkDocument.Page) -> Bool](/documentation/assignables/assignedworkdocument/page/==(_:_:))

##### Instance Properties

- [var rotation: Measurement<UnitAngle>](/documentation/assignables/assignedworkdocument/page/rotation)

#### Instance Properties

- [var pages: [AssignedWorkDocument.Page]](/documentation/assignables/assignedworkdocument/pages)

#### Instance Methods

- [func exportToPDF(visibleParts: [MergeablePartsContainerPartID]) async -> PDFDocument](/documentation/assignables/assignedworkdocument/exporttopdf(visibleparts:))
- [Assignable](/documentation/assignables/assignable)

### Assigning a document

- [func assign(to: AnyUserIdentity) throws -> AssignedWorkDocument](/documentation/assignables/assignable/assign(to:)-4jnsl)
- [func assign(to: some UserIdentity) throws -> AssignedWorkDocument](/documentation/assignables/assignable/assign(to:)-4mit8)

### Instance Methods

- [func makeAssignedWorkDocument() throws -> AssignedWorkDocument](/documentation/assignables/assignable/makeassignedworkdocument())
- [func makeAssignedWorkDocument(id: String) throws -> AssignedWorkDocument](/documentation/assignables/assignable/makeassignedworkdocument(id:))

## Configuration

- [AssignableDocumentConfiguration](/documentation/assignables/assignabledocumentconfiguration)

### Configuring a document

- [var maxScore: Double?](/documentation/assignables/assignabledocumentconfiguration/maxscore)
- [var correctScoreMarkType: AssignableDocument.CorrectMarkType](/documentation/assignables/assignabledocumentconfiguration/correctscoremarktype)
- [var pointsPerBonusScoreMark: Double](/documentation/assignables/assignabledocumentconfiguration/pointsperbonusscoremark)
- [var pointsPerCorrectScoreMark: Double](/documentation/assignables/assignabledocumentconfiguration/pointspercorrectscoremark)
- [var pointsPerIncorrectScoreMark: Double](/documentation/assignables/assignabledocumentconfiguration/pointsperincorrectscoremark)
- [AssignedWorkDocumentConfiguration](/documentation/assignables/assignedworkdocumentconfiguration)

### Configuring the score

- [var manualScore: Double?](/documentation/assignables/assignedworkdocumentconfiguration/manualscore)

## Presentation

- [AssignableDocumentView](/documentation/assignables/assignabledocumentview)

### Creating a document view

- [init(document: Binding<AssignableDocumentView.Document>, activePartID: MergeablePartsContainerPartID?, hiddenPartIDs: [MergeablePartsContainerPartID], selectedPageID: Binding<AssignableDocumentView.Document.Page.ID?>?, selectedQuestionID: Binding<AssignableDocumentView.Document.Question.ID?>?, showsPageThumbnails: Bool, isStructureEditingEnabled: Bool)](/documentation/assignables/assignabledocumentview/init(document:activepartid:hiddenpartids:selectedpageid:selectedquestionid:showspagethumbnails:isstructureeditingenabled:))

### Customizing the view

- [AssignableDocumentView.Document](/documentation/assignables/assignabledocumentview/document)

### Initializers

- [init(document: Binding<AssignableDocumentView.Document>, activePartID: MergeablePartsContainerPartID?, hiddenPartIDs: [MergeablePartsContainerPartID], selectedPageID: Binding<AssignableDocumentView.Document.Page.ID?>?, selectedQuestionID: Binding<AssignableDocumentView.Document.Question.ID?>?, showsPageThumbnails: Bool, isStructureEditingEnabled: Bool, allowsPencilDrawing: Bool, onMarkupActivation: (Bool) -> Void)](/documentation/assignables/assignabledocumentview/init(document:activepartid:hiddenpartids:selectedpageid:selectedquestionid:showspagethumbnails:isstructureeditingenabled:allowspencildrawing:onmarkupactivation:))
- [AssignedWorkDocumentView](/documentation/assignables/assignedworkdocumentview)

### Creating a document view

- [init(document: Binding<AssignedWorkDocumentView.Document>, activePartID: MergeablePartsContainerPartID?, hiddenPartIDs: [MergeablePartsContainerPartID], selectedPageID: Binding<AssignedWorkDocumentView.Document.Page.ID?>?, selectedQuestionID: Binding<AssignableDocument.Question.ID?>?, showsPageThumbnails: Bool, isStructureEditingEnabled: Bool)](/documentation/assignables/assignedworkdocumentview/init(document:activepartid:hiddenpartids:selectedpageid:selectedquestionid:showspagethumbnails:isstructureeditingenabled:))

### Implementing a view

- [AssignedWorkDocumentView.Document](/documentation/assignables/assignedworkdocumentview/document)

### Initializers

- [init(document: Binding<AssignedWorkDocumentView.Document>, activePartID: MergeablePartsContainerPartID?, hiddenPartIDs: [MergeablePartsContainerPartID], selectedPageID: Binding<AssignedWorkDocumentView.Document.Page.ID?>?, selectedQuestionID: Binding<AssignableDocument.Question.ID?>?, showsPageThumbnails: Bool, isStructureEditingEnabled: Bool, onMarkupActivation: (Bool) -> Void)](/documentation/assignables/assignedworkdocumentview/init(document:activepartid:hiddenpartids:selectedpageid:selectedquestionid:showspagethumbnails:isstructureeditingenabled:onmarkupactivation:))

## Document elements

- [DocumentElement](/documentation/assignables/documentelement)

### Implementing a document element

- [Document](/documentation/assignables/documentelement/document)
- [BasicDocumentElementID](/documentation/assignables/basicdocumentelementid)
- [DocumentElementID](/documentation/assignables/documentelementid)

### Implementing an element identifier

- [Element](/documentation/assignables/documentelementid/element)
- [AssignableDocumentElement](/documentation/assignables/assignabledocumentelement)
- [AssignedWorkDocumentElement](/documentation/assignables/assignedworkdocumentelement)

## Mergeable document

- [MergeableDocument](/documentation/assignables/mergeabledocument)

### Getting the pages

- [var pages: [Self.Page]](/documentation/assignables/mergeabledocument/pages)
- [Page](/documentation/assignables/mergeabledocument/page)

### Exporting the layers

- [func exportToPDF(visibleParts: [Self.PartID]) async -> PDFDocument](/documentation/assignables/mergeabledocument/exporttopdf(visibleparts:))

### Exporting the thumbnails

- [func pageThumbnails(visibleParts: [Self.PartID]) async -> [Self.Page.ID : Self.Page.Thumbnail]](/documentation/assignables/mergeabledocument/pagethumbnails(visibleparts:))

### Getting the error type

- [Error](/documentation/assignables/mergeabledocument/error)
- [MergeablePartsContainerPartID](/documentation/assignables/mergeablepartscontainerpartid)

### Initializers

- [init(String)](/documentation/assignables/mergeablepartscontainerpartid/init(_:))

### Instance Properties

- [var rawValue: String](/documentation/assignables/mergeablepartscontainerpartid/rawvalue)
- [MergeableDocumentPage](/documentation/assignables/mergeabledocumentpage)

### Implementing a mergeable page

- [Document](/documentation/assignables/mergeabledocumentpage/document)
- [MergeableDocumentPage.Thumbnail](/documentation/assignables/mergeabledocumentpage/thumbnail)
- [MergeablePartsContainer](/documentation/assignables/mergeablepartscontainer)

### Merging the parts

- [func merge(other: Self) throws -> Bool](/documentation/assignables/mergeablepartscontainer/merge(other:))
- [func merge(partID: Self.PartID, partDataURL: URL) throws -> Bool](/documentation/assignables/mergeablepartscontainer/merge(partid:partdataurl:))

### Exporting the parts

- [func export(partIDs: [Self.PartID]) async throws -> [Self.PartID : URL]](/documentation/assignables/mergeablepartscontainer/export(partids:))

### Getting the part identifiers

- [var partIDs: [Self.PartID]](/documentation/assignables/mergeablepartscontainer/partids)
- [MergeablePartsContainer.PartID](/documentation/assignables/mergeablepartscontainer/partid)

### Inspecting the parts

- [var isPartial: Bool](/documentation/assignables/mergeablepartscontainer/ispartial)

### Instance Methods

- [func exportParts(identifiedBy: [Self.PartID]) async throws -> [Self.PartID : MergeablePartData]](/documentation/assignables/mergeablepartscontainer/exportparts(identifiedby:))
- [func makePart(for: Self.PartID) throws -> MergeablePartData?](/documentation/assignables/mergeablepartscontainer/makepart(for:))
- [func merge(Self) async throws -> Bool](/documentation/assignables/mergeablepartscontainer/merge(_:))
- [func merge(partData: MergeablePartData, into: Self.PartID) async throws -> Bool](/documentation/assignables/mergeablepartscontainer/merge(partdata:into:))
- [DocumentThumbnail](/documentation/assignables/documentthumbnail)

### Getting the page identifier

- [var pageID: Document.Page.ID](/documentation/assignables/documentthumbnail/pageid)

## Identity

- [UserIdentity](/documentation/assignables/useridentity)

### Inspecting an identity

- [var stringRepresentation: String](/documentation/assignables/useridentity/stringrepresentation)
- [var typeID: String](/documentation/assignables/useridentity/typeid)

### Setting the scope

- [func scope<R>(() throws -> R) rethrows -> R](/documentation/assignables/useridentity/scope(_:)-esta)
- [func scope<R>(() async throws -> R) async rethrows -> R](/documentation/assignables/useridentity/scope(_:)-j2jq)

### Getting a type eraser

- [func eraseToAnyUserIdentity() -> AnyUserIdentity](/documentation/assignables/useridentity/erasetoanyuseridentity())
- [UserIdentity.As](/documentation/assignables/useridentity/as)
- [AnonymousUserIdentity](/documentation/assignables/anonymoususeridentity)

### Creating an anonymous identity

- [init()](/documentation/assignables/anonymoususeridentity/init())

### Inspecting an identity

- [var stringRepresentation: String](/documentation/assignables/anonymoususeridentity/stringrepresentation)
- [var typeID: String](/documentation/assignables/anonymoususeridentity/typeid-swift.property)
- [static var typeID: String](/documentation/assignables/anonymoususeridentity/typeid-swift.type.property)
- [AnyUserIdentity](/documentation/assignables/anyuseridentity)

### Creating a user identity

- [init<T>(T)](/documentation/assignables/anyuseridentity/init(_:))
- [init(from: any Decoder) throws](/documentation/assignables/anyuseridentity/init(from:))

### Setting the scope

- [func scope<R>(() throws -> R) rethrows -> R](/documentation/assignables/anyuseridentity/scope(_:)-1wfwz)
- [func scope<R>(() async throws -> R) async rethrows -> R](/documentation/assignables/anyuseridentity/scope(_:)-76dnq)

### Inspecting an identity

- [var stringRepresentation: String](/documentation/assignables/anyuseridentity/stringrepresentation)
- [var typeID: String](/documentation/assignables/anyuseridentity/typeid)
- [AnyUserIdentity.Error](/documentation/assignables/anyuseridentity/error)

#### Decode error

- [case cannotDecode](/documentation/assignables/anyuseridentity/error/cannotdecode)

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/assignables/anyuseridentity/encode(to:))
- [func hash(into: inout Hasher)](/documentation/assignables/anyuseridentity/hash(into:))

### Comparing identities

- [static func == (AnyUserIdentity, AnyUserIdentity) -> Bool](/documentation/assignables/anyuseridentity/==(_:_:))
- [StringUserIdentity](/documentation/assignables/stringuseridentity)

### Creating a user identity

- [init(value: String)](/documentation/assignables/stringuseridentity/init(value:))

### Inspecting an identity

- [var stringRepresentation: String](/documentation/assignables/stringuseridentity/stringrepresentation)
- [var typeID: String](/documentation/assignables/stringuseridentity/typeid-swift.property)
- [static var typeID: String](/documentation/assignables/stringuseridentity/typeid-swift.type.property)
- [var value: String](/documentation/assignables/stringuseridentity/value)
- [UserIdentityTypeRegistry](/documentation/assignables/useridentitytyperegistry)

### Registering an identity

- [static func registerUserIdentityType<UI>(typeID: String, type: UI.Type)](/documentation/assignables/useridentitytyperegistry/registeruseridentitytype(typeid:type:))
- [UserIdentityFactory](/documentation/assignables/useridentityfactory)

### Getting the anonymous identity

- [static var anonymous: AnonymousUserIdentity](/documentation/assignables/useridentityfactory/anonymous)

### Creating an identity

- [static func string(String) -> StringUserIdentity](/documentation/assignables/useridentityfactory/string(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
