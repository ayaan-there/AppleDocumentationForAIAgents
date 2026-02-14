# Tabular Data Documentation

Source: https://sosumi.ai/documentation/tabulardata

---
title: TabularData
source: https://developer.apple.com/documentation/tabulardata
timestamp: 2026-02-13T19:02:58.329Z
---

## Data Tables

- [DataFrame](/documentation/tabulardata/dataframe)

### Creating a Data Frame

- [init()](/documentation/tabulardata/dataframe/init())
- [init<S>(columns: S)](/documentation/tabulardata/dataframe/init(columns:))
- [init(dictionaryLiteral: (String, [Any?])...)](/documentation/tabulardata/dataframe/init(dictionaryliteral:))

### Creating a Data Frame from Other Data Frames

- [init(DataFrame.Slice)](/documentation/tabulardata/dataframe/init(_:))
- [DataFrame.Slice](/documentation/tabulardata/dataframe/slice)

#### Inspecting a Slice

- [var shape: (rows: Int, columns: Int)](/documentation/tabulardata/dataframe/slice/shape)
- [var columns: [AnyColumnSlice]](/documentation/tabulardata/dataframe/slice/columns)
- [var rows: DataFrame.Rows](/documentation/tabulardata/dataframe/slice/rows)
- [var base: DataFrame](/documentation/tabulardata/dataframe/slice/base)

#### Creating a Slice by Selecting a Column

- [subscript<T>(ColumnID<T>) -> DiscontiguousColumnSlice<T>](/documentation/tabulardata/dataframe/slice/subscript(_:)-32h9z)
- [subscript<T>(column _: Int, T.Type) -> DiscontiguousColumnSlice<T>](/documentation/tabulardata/dataframe/slice/subscript(column:_:))
- [subscript<T>(String, T.Type) -> DiscontiguousColumnSlice<T>](/documentation/tabulardata/dataframe/slice/subscript(_:_:))
- [subscript(String) -> AnyColumnSlice](/documentation/tabulardata/dataframe/slice/subscript(_:)-18kdy)
- [subscript(dynamicMember _: String) -> AnyColumnSlice](/documentation/tabulardata/dataframe/slice/subscript(dynamicmember:))

#### Creating a Slice by Selecting Multiple Columns

- [subscript<S>(S) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/subscript(_:)-5y42o)
- [func selecting<S>(columnNames: S) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/selecting(columnnames:)-9l8oe)
- [func selecting(columnNames: String...) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/selecting(columnnames:)-48kji)

#### Creating a Slice by Selecting Rows

- [func prefix(Int) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/prefix(_:))
- [func prefix(upTo: Int) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/prefix(upto:))
- [func prefix(through: Int) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/prefix(through:))
- [func suffix(Int) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/suffix(_:))
- [func suffix(from: Int) -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/suffix(from:))

#### Creating a Slice by Filtering Rows

- [func filter<T>(on: ColumnID<T>, (T?) throws -> Bool) rethrows -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/filter(on:_:))
- [func filter<T>(on: String, T.Type, (T?) throws -> Bool) rethrows -> DataFrame.Slice](/documentation/tabulardata/dataframe/slice/filter(on:_:_:))

#### Grouping Rows

- [RowGrouping](/documentation/tabulardata/rowgrouping)

##### Creating a Row Grouping

- [init<D>(frame: D, columnName: String, timeUnit: Calendar.Component)](/documentation/tabulardata/rowgrouping/init(frame:columnname:timeunit:))
- [init<D>(groups: [(GroupingKey?, D)], groupKeysColumnName: String)](/documentation/tabulardata/rowgrouping/init(groups:groupkeyscolumnname:))

##### Inspecting a Row Grouping

- [var count: Int](/documentation/tabulardata/rowgrouping/count)
- [subscript(Int) -> (key: GroupingKey?, group: DataFrame.Slice)](/documentation/tabulardata/rowgrouping/subscript(_:)-5z2eg)

##### Transforming a Row Grouping

- [func mapGroups((DataFrame.Slice) throws -> DataFrame) rethrows -> RowGrouping<GroupingKey>](/documentation/tabulardata/rowgrouping/mapgroups(_:))

##### Splitting a Row Grouping

- [func randomSplit(by: Double, seed: Int?) -> (RowGrouping<GroupingKey>, RowGrouping<GroupingKey>)](/documentation/tabulardata/rowgrouping/randomsplit(by:seed:))

##### Aggregating a Row Grouping

- [func counts(order: Order?) -> DataFrame](/documentation/tabulardata/rowgrouping/counts(order:))
- [func aggregated<Element, Result>(on: [String], naming: (String) -> String, transform: (DiscontiguousColumnSlice<Element>) throws -> Result?) rethrows -> DataFrame](/documentation/tabulardata/rowgrouping/aggregated(on:naming:transform:))

##### Flattening a Row Grouping

- [func ungrouped() -> DataFrame](/documentation/tabulardata/rowgrouping/ungrouped())

##### Summarizing a Row Grouping

- [func summary() -> any GroupSummaries](/documentation/tabulardata/rowgrouping/summary())
- [func summary(of: [String]) -> any GroupSummaries](/documentation/tabulardata/rowgrouping/summary(of:))
- [GroupSummaries](/documentation/tabulardata/groupsummaries)

###### Instance Properties

- [var description: String](/documentation/tabulardata/groupsummaries/description)

###### Instance Methods

- [func description(options: FormattingOptions) -> String](/documentation/tabulardata/groupsummaries/description(options:))

###### Subscripts

- [subscript(Any?...) -> DataFrame?](/documentation/tabulardata/groupsummaries/subscript(_:))

##### Describing a Row Grouping

- [var description: String](/documentation/tabulardata/rowgrouping/description)

##### Subscripts

- [subscript(Any?...) -> DataFrame.Slice?](/documentation/tabulardata/rowgrouping/subscript(_:)-2xxs8)

##### Default Implementations

- [Collection Implementations](/documentation/tabulardata/rowgrouping/collection-implementations)

###### Instance Properties

- [var count: Int](/documentation/tabulardata/rowgrouping/count)
- [RandomAccessCollection Implementations](/documentation/tabulardata/rowgrouping/randomaccesscollection-implementations)

###### Instance Properties

- [var endIndex: Int](/documentation/tabulardata/rowgrouping/endindex)
- [var startIndex: Int](/documentation/tabulardata/rowgrouping/startindex)

###### Instance Methods

- [func index(after: Int) -> Int](/documentation/tabulardata/rowgrouping/index(after:))
- [func index(before: Int) -> Int](/documentation/tabulardata/rowgrouping/index(before:))

###### Subscripts

- [subscript(Int) -> (key: GroupingKey?, group: DataFrame.Slice)](/documentation/tabulardata/rowgrouping/subscript(_:)-5z2eg)
- [RowGroupingProtocol Implementations](/documentation/tabulardata/rowgrouping/rowgroupingprotocol-implementations)

###### Instance Methods

- [func randomSplit(by: Double, seed: Int?) -> (RowGrouping<GroupingKey>, RowGrouping<GroupingKey>)](/documentation/tabulardata/rowgrouping/randomsplit(by:seed:))
- [func summary() -> any GroupSummaries](/documentation/tabulardata/rowgrouping/summary())
- [func summary(of: [String]) -> any GroupSummaries](/documentation/tabulardata/rowgrouping/summary(of:))
- [func grouped(by: String) -> any RowGroupingProtocol](/documentation/tabulardata/dataframe/slice/grouped(by:))
- [RowGroupingProtocol](/documentation/tabulardata/rowgroupingprotocol)

##### Inspecting a Row Grouping

- [var count: Int](/documentation/tabulardata/rowgroupingprotocol/count)

##### Transforming a Row Grouping

- [func mapGroups((DataFrame.Slice) throws -> DataFrame) rethrows -> Self](/documentation/tabulardata/rowgroupingprotocol/mapgroups(_:))

##### Splitting a Row Grouping

- [func randomSplit(by: Double) -> (Self, Self)](/documentation/tabulardata/rowgroupingprotocol/randomsplit(by:))
- [func randomSplit(by: Double, seed: Int?) -> (Self, Self)](/documentation/tabulardata/rowgroupingprotocol/randomsplit(by:seed:))

##### Aggregating a Row Grouping

- [func counts() -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/counts())
- [func counts(order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/counts(order:))
- [func sums<N>(String, N.Type, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/sums(_:_:order:))
- [func sums<N>(ColumnID<N>, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/sums(_:order:))
- [func means<N>(String, N.Type, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/means(_:_:order:))
- [func means<N>(ColumnID<N>, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/means(_:order:))
- [func minimums<N>(String, N.Type, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/minimums(_:_:order:))
- [func minimums<N>(ColumnID<N>, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/minimums(_:order:))
- [func maximums<N>(String, N.Type, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/maximums(_:_:order:))
- [func maximums<N>(ColumnID<N>, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/maximums(_:order:))
- [func aggregated<Element, Result>(on: ColumnID<Element>, into: String?, transform: (DiscontiguousColumnSlice<Element>) throws -> Result) rethrows -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/aggregated(on:into:transform:))
- [func aggregated<Element, Result>(on: [String], naming: (String) -> String, transform: (DiscontiguousColumnSlice<Element>) throws -> Result?) rethrows -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/aggregated(on:naming:transform:))

##### Flattening a Row Grouping

- [func ungrouped() -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/ungrouped())

##### Summarizing a Row Grouping

- [func summary() -> any GroupSummaries](/documentation/tabulardata/rowgroupingprotocol/summary())
- [func summary(of: [String]) -> any GroupSummaries](/documentation/tabulardata/rowgroupingprotocol/summary(of:))
- [GroupSummaries](/documentation/tabulardata/groupsummaries)

###### Instance Properties

- [var description: String](/documentation/tabulardata/groupsummaries/description)

###### Instance Methods

- [func description(options: FormattingOptions) -> String](/documentation/tabulardata/groupsummaries/description(options:))

###### Subscripts

- [subscript(Any?...) -> DataFrame?](/documentation/tabulardata/groupsummaries/subscript(_:))

##### Instance Methods

- [func filter((DataFrame.Slice) throws -> Bool) rethrows -> Self](/documentation/tabulardata/rowgroupingprotocol/filter(_:))
- [func quantiles<N>(String, N.Type, quantile: N, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/quantiles(_:_:quantile:order:))
- [func quantiles<N>(ColumnID<N>, quantile: N, order: Order?) -> DataFrame](/documentation/tabulardata/rowgroupingprotocol/quantiles(_:quantile:order:))

##### Subscripts

- [subscript(Any?...) -> DataFrame.Slice?](/documentation/tabulardata/rowgroupingprotocol/subscript(_:))

#### Summarizing a Slice

- [func summary() -> DataFrame](/documentation/tabulardata/dataframe/slice/summary())
- [func summary(of: String...) -> DataFrame](/documentation/tabulardata/dataframe/slice/summary(of:))
- [func summary(ofColumns: Int...) -> DataFrame](/documentation/tabulardata/dataframe/slice/summary(ofcolumns:))
- [SummaryColumnIDs](/documentation/tabulardata/summarycolumnids)

##### Type Properties

- [static let columnName: ColumnID<String>](/documentation/tabulardata/summarycolumnids/columnname)
- [static let firstQuartile: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/firstquartile)
- [static let maximum: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/maximum)
- [static let mean: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/mean)
- [static let median: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/median)
- [static let minimum: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/minimum)
- [static let mode: ColumnID<[Any]>](/documentation/tabulardata/summarycolumnids/mode)
- [static let noneCount: ColumnID<Int>](/documentation/tabulardata/summarycolumnids/nonecount)
- [static let someCount: ColumnID<Int>](/documentation/tabulardata/summarycolumnids/somecount)
- [static let standardDeviation: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/standarddeviation)
- [static let thirdQuartile: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/thirdquartile)
- [static let uniqueCount: ColumnID<Int>](/documentation/tabulardata/summarycolumnids/uniquecount)

#### Comparing Slices

- [static func == (DataFrame.Slice, DataFrame.Slice) -> Bool](/documentation/tabulardata/dataframe/slice/==(_:_:))

#### Describing a Slice

- [var description: String](/documentation/tabulardata/dataframe/slice/description)
- [var debugDescription: String](/documentation/tabulardata/dataframe/slice/debugdescription)
- [var customMirror: Mirror](/documentation/tabulardata/dataframe/slice/custommirror)

#### Hashing a Slice

- [func hash(into: inout Hasher)](/documentation/tabulardata/dataframe/slice/hash(into:))

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/tabulardata/dataframe/slice/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/tabulardata/dataframe/slice/debugdescription)
- [CustomReflectable Implementations](/documentation/tabulardata/dataframe/slice/customreflectable-implementations)

##### Instance Properties

- [var customMirror: Mirror](/documentation/tabulardata/dataframe/slice/custommirror)
- [CustomStringConvertible Implementations](/documentation/tabulardata/dataframe/slice/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/tabulardata/dataframe/slice/description)
- [Equatable Implementations](/documentation/tabulardata/dataframe/slice/equatable-implementations)

##### Operators

- [static func == (DataFrame.Slice, DataFrame.Slice) -> Bool](/documentation/tabulardata/dataframe/slice/==(_:_:))
- [Hashable Implementations](/documentation/tabulardata/dataframe/slice/hashable-implementations)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/tabulardata/dataframe/slice/hash(into:))

### Creating a Data Frame from a JSON File

- [init(contentsOfJSONFile: URL, columns: [String]?, types: [String : JSONType], options: JSONReadingOptions) throws](/documentation/tabulardata/dataframe/init(contentsofjsonfile:columns:types:options:))
- [init(jsonData: Data, columns: [String]?, types: [String : JSONType], options: JSONReadingOptions) throws](/documentation/tabulardata/dataframe/init(jsondata:columns:types:options:))
- [JSONType](/documentation/tabulardata/jsontype)

#### Enumeration Cases

- [case array](/documentation/tabulardata/jsontype/array)
- [case boolean](/documentation/tabulardata/jsontype/boolean)
- [case date](/documentation/tabulardata/jsontype/date)
- [case double](/documentation/tabulardata/jsontype/double)
- [case integer](/documentation/tabulardata/jsontype/integer)
- [case object](/documentation/tabulardata/jsontype/object)
- [case string](/documentation/tabulardata/jsontype/string)
- [JSONReadingOptions](/documentation/tabulardata/jsonreadingoptions)

#### Initializers

- [init()](/documentation/tabulardata/jsonreadingoptions/init())

#### Instance Properties

- [var dateParsers: [(String) -> Date?]](/documentation/tabulardata/jsonreadingoptions/dateparsers)

#### Instance Methods

- [func addDateParseStrategy<T>(T)](/documentation/tabulardata/jsonreadingoptions/adddateparsestrategy(_:))

### Creating a Data Frame from a CSV

- [init(contentsOfCSVFile: URL, columns: [String]?, rows: Range<Int>?, types: [String : CSVType], options: CSVReadingOptions) throws](/documentation/tabulardata/dataframe/init(contentsofcsvfile:columns:rows:types:options:))
- [init(csvData: Data, columns: [String]?, rows: Range<Int>?, types: [String : CSVType], options: CSVReadingOptions) throws](/documentation/tabulardata/dataframe/init(csvdata:columns:rows:types:options:))
- [CSVType](/documentation/tabulardata/csvtype)

#### Enumeration Cases

- [case boolean](/documentation/tabulardata/csvtype/boolean)
- [case data](/documentation/tabulardata/csvtype/data)
- [case date](/documentation/tabulardata/csvtype/date)
- [case double](/documentation/tabulardata/csvtype/double)
- [case float](/documentation/tabulardata/csvtype/float)
- [case integer](/documentation/tabulardata/csvtype/integer)
- [case string](/documentation/tabulardata/csvtype/string)
- [CSVReadingOptions](/documentation/tabulardata/csvreadingoptions)

#### Initializers

- [init(hasHeaderRow: Bool, nilEncodings: Set<String>, trueEncodings: Set<String>, falseEncodings: Set<String>, floatingPointType: CSVType, ignoresEmptyLines: Bool, usesQuoting: Bool, usesEscaping: Bool, delimiter: Character, escapeCharacter: Character)](/documentation/tabulardata/csvreadingoptions/init(hasheaderrow:nilencodings:trueencodings:falseencodings:floatingpointtype:ignoresemptylines:usesquoting:usesescaping:delimiter:escapecharacter:))

#### Instance Properties

- [var dateParsers: [(String) -> Date?]](/documentation/tabulardata/csvreadingoptions/dateparsers)
- [var delimiter: Character](/documentation/tabulardata/csvreadingoptions/delimiter)
- [var escapeCharacter: Character](/documentation/tabulardata/csvreadingoptions/escapecharacter)
- [var falseEncodings: Set<String>](/documentation/tabulardata/csvreadingoptions/falseencodings)
- [var floatingPointType: CSVType](/documentation/tabulardata/csvreadingoptions/floatingpointtype)
- [var hasHeaderRow: Bool](/documentation/tabulardata/csvreadingoptions/hasheaderrow)
- [var ignoresEmptyLines: Bool](/documentation/tabulardata/csvreadingoptions/ignoresemptylines)
- [var nilEncodings: Set<String>](/documentation/tabulardata/csvreadingoptions/nilencodings)
- [var trueEncodings: Set<String>](/documentation/tabulardata/csvreadingoptions/trueencodings)
- [var usesEscaping: Bool](/documentation/tabulardata/csvreadingoptions/usesescaping)
- [var usesQuoting: Bool](/documentation/tabulardata/csvreadingoptions/usesquoting)

#### Instance Methods

- [func addDateParseStrategy<T>(T)](/documentation/tabulardata/csvreadingoptions/adddateparsestrategy(_:))

### Creating a Data Frame from Turi Create Types

- [init(contentsOfSFrameDirectory: URL, columns: [String]?, rows: Range<Int>?) throws](/documentation/tabulardata/dataframe/init(contentsofsframedirectory:columns:rows:))
- [ShapedData](/documentation/tabulardata/shapeddata)

#### Initializers

- [init(shape: [Int], strides: [Int], contents: [Element])](/documentation/tabulardata/shapeddata/init(shape:strides:contents:))

#### Instance Properties

- [let contents: [Element]](/documentation/tabulardata/shapeddata/contents)
- [let shape: [Int]](/documentation/tabulardata/shapeddata/shape)
- [let strides: [Int]](/documentation/tabulardata/shapeddata/strides)

#### Subscripts

- [subscript(Int...) -> Element](/documentation/tabulardata/shapeddata/subscript(_:))

### Inspecting a Data Frame

- [var shape: (rows: Int, columns: Int)](/documentation/tabulardata/dataframe/shape)
- [var columns: [AnyColumn]](/documentation/tabulardata/dataframe/columns)
- [var rows: DataFrame.Rows](/documentation/tabulardata/dataframe/rows-swift.property)
- [DataFrame.Rows](/documentation/tabulardata/dataframe/rows-swift.struct)

#### Inspecting a Row Collection

- [var count: Int](/documentation/tabulardata/dataframe/rows-swift.struct/count)

#### Accessing Elements

- [subscript(Int) -> DataFrame.Row](/documentation/tabulardata/dataframe/rows-swift.struct/subscript(_:)-3f938)
- [subscript(Range<Int>) -> DataFrame.Rows](/documentation/tabulardata/dataframe/rows-swift.struct/subscript(_:)-2qzx7)
- [var base: DataFrame](/documentation/tabulardata/dataframe/base)
- [func containsColumn<T>(String, T.Type) -> Bool](/documentation/tabulardata/dataframe/containscolumn(_:_:))

### Sorting a Data Frame

- [func sort(on: String, order: Order)](/documentation/tabulardata/dataframe/sort(on:order:)-4vns7)
- [func sort<T>(on: String, T.Type, order: Order)](/documentation/tabulardata/dataframe/sort(on:_:order:)-78avw)
- [func sort<T>(on: String, T.Type, by: (T, T) throws -> Bool) rethrows](/documentation/tabulardata/dataframe/sort(on:_:by:))
- [func sort<T>(on: ColumnID<T>, by: (T, T) throws -> Bool) rethrows](/documentation/tabulardata/dataframe/sort(on:by:))
- [func sort<T>(on: ColumnID<T>, order: Order)](/documentation/tabulardata/dataframe/sort(on:order:)-5ep7w)
- [func sort<T0, T1>(on: ColumnID<T0>, ColumnID<T1>, order: Order)](/documentation/tabulardata/dataframe/sort(on:_:order:)-8wrkl)
- [func sort<T0, T1, T2>(on: ColumnID<T0>, ColumnID<T1>, ColumnID<T2>, order: Order)](/documentation/tabulardata/dataframe/sort(on:_:_:order:))

### Summarizing a Data Frame

- [func summary() -> DataFrame](/documentation/tabulardata/dataframe/summary())
- [func summary(of: String...) -> DataFrame](/documentation/tabulardata/dataframe/summary(of:))
- [func summary(ofColumns: Int...) -> DataFrame](/documentation/tabulardata/dataframe/summary(ofcolumns:))
- [SummaryColumnIDs](/documentation/tabulardata/summarycolumnids)

#### Type Properties

- [static let columnName: ColumnID<String>](/documentation/tabulardata/summarycolumnids/columnname)
- [static let firstQuartile: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/firstquartile)
- [static let maximum: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/maximum)
- [static let mean: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/mean)
- [static let median: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/median)
- [static let minimum: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/minimum)
- [static let mode: ColumnID<[Any]>](/documentation/tabulardata/summarycolumnids/mode)
- [static let noneCount: ColumnID<Int>](/documentation/tabulardata/summarycolumnids/nonecount)
- [static let someCount: ColumnID<Int>](/documentation/tabulardata/summarycolumnids/somecount)
- [static let standardDeviation: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/standarddeviation)
- [static let thirdQuartile: ColumnID<Double>](/documentation/tabulardata/summarycolumnids/thirdquartile)
- [static let uniqueCount: ColumnID<Int>](/documentation/tabulardata/summarycolumnids/uniquecount)

### Saving a Data Frame to a CSV Format

- [CSVWritingOptions](/documentation/tabulardata/csvwritingoptions)

#### Initializers

- [init()](/documentation/tabulardata/csvwritingoptions/init())
- [init(includesHeader: Bool, dateFormat: String?, nilEncoding: String, trueEncoding: String, falseEncoding: String, newline: String, delimiter: Character)](/documentation/tabulardata/csvwritingoptions/init(includesheader:dateformat:nilencoding:trueencoding:falseencoding:newline:delimiter:))
- [init(includesHeader: Bool, nilEncoding: String, trueEncoding: String, falseEncoding: String, newline: String, delimiter: Character)](/documentation/tabulardata/csvwritingoptions/init(includesheader:nilencoding:trueencoding:falseencoding:newline:delimiter:))

#### Instance Properties

- [var dateFormat: String?](/documentation/tabulardata/csvwritingoptions/dateformat)
- [var dateFormatter: (Date) -> String](/documentation/tabulardata/csvwritingoptions/dateformatter)
- [var delimiter: Character](/documentation/tabulardata/csvwritingoptions/delimiter)
- [var falseEncoding: String](/documentation/tabulardata/csvwritingoptions/falseencoding)
- [var includesHeader: Bool](/documentation/tabulardata/csvwritingoptions/includesheader)
- [var newline: String](/documentation/tabulardata/csvwritingoptions/newline)
- [var nilEncoding: String](/documentation/tabulardata/csvwritingoptions/nilencoding)
- [var trueEncoding: String](/documentation/tabulardata/csvwritingoptions/trueencoding)

### Describing a Data Frame

- [var description: String](/documentation/tabulardata/dataframe/description)
- [var debugDescription: String](/documentation/tabulardata/dataframe/debugdescription)
- [var customMirror: Mirror](/documentation/tabulardata/dataframe/custommirror)

### Comparing Data Frames

- [static func == (DataFrame, DataFrame) -> Bool](/documentation/tabulardata/dataframe/==(_:_:))

### Hashing a Data Frame

- [func hash(into: inout Hasher)](/documentation/tabulardata/dataframe/hash(into:))

### Initializers

- [init<S, Feature, Annotation>(S, featuresColumnID: ColumnID<Feature>, annotationsColumnID: ColumnID<Annotation>) throws](/documentation/tabulardata/dataframe/init(_:featurescolumnid:annotationscolumnid:))
- [init<each T>(contentsOfCSVFile: URL, columns: repeat ColumnID<each T>, rows: Range<Int>?, options: CSVReadingOptions) throws](/documentation/tabulardata/dataframe/init(contentsofcsvfile:columns:rows:options:))
- [init<each T>(csvData: Data, columns: repeat ColumnID<each T>, rows: Range<Int>?, options: CSVReadingOptions) throws](/documentation/tabulardata/dataframe/init(csvdata:columns:rows:options:))

### Instance Methods

- [func containsColumn<T>(ColumnID<T>) -> Bool](/documentation/tabulardata/dataframe/containscolumn(_:)-6nqfs)
- [func containsColumn(String) -> Bool](/documentation/tabulardata/dataframe/containscolumn(_:)-8spst)
- [func loadRangedAnnotations<Annotation>(parameters: DataFrameTemporalAnnotationParameters<Annotation>, continueOnFailure: Bool) throws -> [AnnotatedFeature<TemporalFileSegment, Annotation>]](/documentation/tabulardata/dataframe/loadrangedannotations(parameters:continueonfailure:))
- [func selecting(ColumnSelection) -> DataFrame](/documentation/tabulardata/dataframe/selecting(_:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/tabulardata/dataframe/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/tabulardata/dataframe/debugdescription)
- [CustomReflectable Implementations](/documentation/tabulardata/dataframe/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/tabulardata/dataframe/custommirror)
- [CustomStringConvertible Implementations](/documentation/tabulardata/dataframe/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/dataframe/description)
- [DataFrameProtocol Implementations](/documentation/tabulardata/dataframe/dataframeprotocol-implementations)

#### Instance Properties

- [var base: DataFrame](/documentation/tabulardata/dataframe/base)
- [Equatable Implementations](/documentation/tabulardata/dataframe/equatable-implementations)

#### Operators

- [static func == (DataFrame, DataFrame) -> Bool](/documentation/tabulardata/dataframe/==(_:_:))
- [ExpressibleByDictionaryLiteral Implementations](/documentation/tabulardata/dataframe/expressiblebydictionaryliteral-implementations)

#### Initializers

- [init(dictionaryLiteral: (String, [Any?])...)](/documentation/tabulardata/dataframe/init(dictionaryliteral:))
- [Hashable Implementations](/documentation/tabulardata/dataframe/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/tabulardata/dataframe/hash(into:))
- [DataFrameProtocol](/documentation/tabulardata/dataframeprotocol)

### Inspecting a Data Frame Type

- [var isEmpty: Bool](/documentation/tabulardata/dataframeprotocol/isempty)
- [var shape: (rows: Int, columns: Int)](/documentation/tabulardata/dataframeprotocol/shape)
- [var columns: [Self.ColumnType]](/documentation/tabulardata/dataframeprotocol/columns)
- [ColumnType](/documentation/tabulardata/dataframeprotocol/columntype)
- [var rows: DataFrame.Rows](/documentation/tabulardata/dataframeprotocol/rows)
- [DataFrame.Rows](/documentation/tabulardata/dataframe/rows-swift.struct)

#### Inspecting a Row Collection

- [var count: Int](/documentation/tabulardata/dataframe/rows-swift.struct/count)

#### Accessing Elements

- [subscript(Int) -> DataFrame.Row](/documentation/tabulardata/dataframe/rows-swift.struct/subscript(_:)-3f938)
- [subscript(Range<Int>) -> DataFrame.Rows](/documentation/tabulardata/dataframe/rows-swift.struct/subscript(_:)-2qzx7)
- [var base: DataFrame](/documentation/tabulardata/dataframeprotocol/base)

### Accessing Rows

- [subscript(Range<Int>) -> DataFrame.Slice](/documentation/tabulardata/dataframeprotocol/subscript(_:))
- [subscript<R>(R) -> DataFrame.Slice](/documentation/tabulardata/dataframeprotocol/subscript(_:)-8hly3)

### Creating Two Slices by Splitting Rows

- [func randomSplit(by: Double, seed: Int?) -> (DataFrame.Slice, DataFrame.Slice)](/documentation/tabulardata/dataframeprotocol/randomsplit(by:seed:))
- [func randomSplit<G>(by: Double, using: inout G) -> (DataFrame.Slice, DataFrame.Slice)](/documentation/tabulardata/dataframeprotocol/randomsplit(by:using:))

### Creating Two Data Frames by Splitting Rows

- [func stratifiedSplit(on: String, by: Double, randomSeed: Int?) -> (DataFrame, DataFrame)](/documentation/tabulardata/dataframeprotocol/stratifiedsplit(on:by:randomseed:)-9iauf)
- [func stratifiedSplit(on: String..., by: Double, randomSeed: Int?) -> (DataFrame, DataFrame)](/documentation/tabulardata/dataframeprotocol/stratifiedsplit(on:by:randomseed:)-8szu1)
- [func stratifiedSplit<T>(on: ColumnID<T>, by: Double, randomSeed: Int?) -> (DataFrame, DataFrame)](/documentation/tabulardata/dataframeprotocol/stratifiedsplit(on:by:randomseed:)-714jk)
- [func stratifiedSplit<T0, T1>(on: ColumnID<T0>, ColumnID<T1>, by: Double, randomSeed: Int?) -> (DataFrame, DataFrame)](/documentation/tabulardata/dataframeprotocol/stratifiedsplit(on:_:by:randomseed:))
- [func stratifiedSplit<T0, T1, T2>(on: ColumnID<T0>, ColumnID<T1>, ColumnID<T2>, by: Double, randomSeed: Int?) -> (DataFrame, DataFrame)](/documentation/tabulardata/dataframeprotocol/stratifiedsplit(on:_:_:by:randomseed:))

### Creating a Data Frame by Sorting a Column

- [func sorted(on: String, order: Order) -> DataFrame](/documentation/tabulardata/dataframeprotocol/sorted(on:order:)-818u5)
- [func sorted<T>(on: String, T.Type, order: Order) -> DataFrame](/documentation/tabulardata/dataframeprotocol/sorted(on:_:order:)-8d7rr)
- [func sorted<T>(on: String, T.Type, by: (T, T) throws -> Bool) rethrows -> DataFrame](/documentation/tabulardata/dataframeprotocol/sorted(on:_:by:))
- [func sorted<T>(on: ColumnID<T>, order: Order) -> DataFrame](/documentation/tabulardata/dataframeprotocol/sorted(on:order:)-5nl5c)
- [func sorted<T>(on: ColumnID<T>, by: (T, T) throws -> Bool) rethrows -> DataFrame](/documentation/tabulardata/dataframeprotocol/sorted(on:by:))

### Creating a Data Frame by Sorting Multiple Columns

- [func sorted<T0, T1>(on: ColumnID<T0>, ColumnID<T1>, order: Order) -> DataFrame](/documentation/tabulardata/dataframeprotocol/sorted(on:_:order:)-79los)
- [func sorted<T0, T1, T2>(on: ColumnID<T0>, ColumnID<T1>, ColumnID<T2>, order: Order) -> DataFrame](/documentation/tabulardata/dataframeprotocol/sorted(on:_:_:order:))

### Creating a Data Frame by Joining Another Data Frame

- [func joined<R>(R, on: String, kind: JoinKind) -> DataFrame](/documentation/tabulardata/dataframeprotocol/joined(_:on:kind:)-1gp6k)
- [func joined<R>(R, on: (left: String, right: String), kind: JoinKind) -> DataFrame](/documentation/tabulardata/dataframeprotocol/joined(_:on:kind:)-7u2tw)
- [func joined<R, T>(R, on: (left: ColumnID<T>, right: ColumnID<T>), kind: JoinKind) -> DataFrame](/documentation/tabulardata/dataframeprotocol/joined(_:on:kind:)-9629e)
- [func joined<R, T>(R, on: ColumnID<T>, kind: JoinKind) -> DataFrame](/documentation/tabulardata/dataframeprotocol/joined(_:on:kind:)-mvic)
- [JoinKind](/documentation/tabulardata/joinkind)

#### Enumeration Cases

- [case full](/documentation/tabulardata/joinkind/full)
- [case inner](/documentation/tabulardata/joinkind/inner)
- [case left](/documentation/tabulardata/joinkind/left)
- [case right](/documentation/tabulardata/joinkind/right)

### Creating a Row Grouping by a Column

- [func grouped<GroupingKey>(by: ColumnID<GroupingKey>) -> RowGrouping<GroupingKey>](/documentation/tabulardata/dataframeprotocol/grouped(by:)-77mq2)
- [func grouped(by: String, timeUnit: Calendar.Component) -> RowGrouping<Int>](/documentation/tabulardata/dataframeprotocol/grouped(by:timeunit:)-7s782)
- [func grouped(by: ColumnID<Date>, timeUnit: Calendar.Component) -> RowGrouping<Int>](/documentation/tabulardata/dataframeprotocol/grouped(by:timeunit:)-78cy)
- [func grouped<InputKey, GroupingKey>(by: String, transform: (InputKey?) -> GroupingKey?) -> RowGrouping<GroupingKey>](/documentation/tabulardata/dataframeprotocol/grouped(by:transform:)-3cr4p)
- [func grouped<InputKey, GroupingKey>(by: ColumnID<InputKey>, transform: (InputKey?) -> GroupingKey?) -> RowGrouping<GroupingKey>](/documentation/tabulardata/dataframeprotocol/grouped(by:transform:)-3aade)

### Creating a Row Grouping by Multiple Columns

- [func grouped(by: String...) -> some RowGroupingProtocol](/documentation/tabulardata/dataframeprotocol/grouped(by:)-4wcw6)
- [func grouped<T>(by: ColumnID<T>...) -> some RowGroupingProtocol](/documentation/tabulardata/dataframeprotocol/grouped(by:)-6m6to)
- [func grouped<T0, T1>(by: ColumnID<T0>, ColumnID<T1>) -> some RowGroupingProtocol](/documentation/tabulardata/dataframeprotocol/grouped(by:_:))
- [func grouped<T0, T1, T2>(by: ColumnID<T0>, ColumnID<T1>, ColumnID<T2>) -> some RowGroupingProtocol](/documentation/tabulardata/dataframeprotocol/grouped(by:_:_:))

### Saving a Data Frame Type to a CSV Format

- [func writeCSV(to: URL, options: CSVWritingOptions) throws](/documentation/tabulardata/dataframeprotocol/writecsv(to:options:))
- [func csvRepresentation(options: CSVWritingOptions) throws -> Data](/documentation/tabulardata/dataframeprotocol/csvrepresentation(options:))

### Describing a Data Frame Type

- [func description(options: FormattingOptions) -> String](/documentation/tabulardata/dataframeprotocol/description(options:))

### Instance Methods

- [func jsonRepresentation(options: JSONWritingOptions) throws -> Data](/documentation/tabulardata/dataframeprotocol/jsonrepresentation(options:))
- [func writeJSON(to: URL, options: JSONWritingOptions) throws](/documentation/tabulardata/dataframeprotocol/writejson(to:options:))

## Typed Columns

- [Column](/documentation/tabulardata/column)

### Creating a Column

- [init(name: String, capacity: Int)](/documentation/tabulardata/column/init(name:capacity:))
- [init(ColumnID<WrappedElement>, capacity: Int)](/documentation/tabulardata/column/init(_:capacity:))
- [init<S>(name: String, contents: S)](/documentation/tabulardata/column/init(name:contents:)-6okx3)
- [init<S>(name: String, contents: S)](/documentation/tabulardata/column/init(name:contents:)-8nxtj)
- [init<S>(ColumnID<S.Element>, contents: S)](/documentation/tabulardata/column/init(_:contents:)-1871a)
- [init<S>(ColumnID<S.Element>, contents: S)](/documentation/tabulardata/column/init(_:contents:)-7z5ji)
- [init(ColumnSlice<WrappedElement>)](/documentation/tabulardata/column/init(_:))

### Creating a Column of the Same Type

- [var prototype: any AnyColumnPrototype](/documentation/tabulardata/column/prototype)

### Creating a Type-Erased Column

- [func eraseToAnyColumn() -> AnyColumn](/documentation/tabulardata/column/erasetoanycolumn())

### Creating Transformed Columns

- [func map<T>((Column<WrappedElement>.Element) throws -> T?) rethrows -> Column<T>](/documentation/tabulardata/column/map(_:))
- [func mapNonNil<T>((WrappedElement) throws -> T?) rethrows -> Column<T>](/documentation/tabulardata/column/mapnonnil(_:))

### Inspecting a Column

- [var name: String](/documentation/tabulardata/column/name)
- [var count: Int](/documentation/tabulardata/column/count)
- [var missingCount: Int](/documentation/tabulardata/column/missingcount)
- [Column.Element](/documentation/tabulardata/column/element)
- [var wrappedElementType: any Any.Type](/documentation/tabulardata/column/wrappedelementtype)

### Transforming a Column

- [func transform((WrappedElement) throws -> WrappedElement) rethrows](/documentation/tabulardata/column/transform(_:)-271dd)
- [func transform((Column<WrappedElement>.Element) throws -> Column<WrappedElement>.Element) rethrows](/documentation/tabulardata/column/transform(_:)-6mrwg)

### Adding Elements

- [func append(WrappedElement)](/documentation/tabulardata/column/append(_:)-qycj)
- [func append(Column<WrappedElement>.Element)](/documentation/tabulardata/column/append(_:)-4t2pt)
- [func append<S>(contentsOf: S)](/documentation/tabulardata/column/append(contentsof:)-qb4p)
- [func append<S>(contentsOf: S)](/documentation/tabulardata/column/append(contentsof:)-42y1d)

### Finding an Element Index

- [func argmin() -> Int?](/documentation/tabulardata/column/argmin())
- [func argmax() -> Int?](/documentation/tabulardata/column/argmax())

### Removing an Element

- [func remove(at: Int)](/documentation/tabulardata/column/remove(at:))

### Accessing Elements

- [subscript(Int) -> Column<WrappedElement>.Element](/documentation/tabulardata/column/subscript(_:)-qm4d)
- [subscript<R>(R) -> ColumnSlice<WrappedElement>](/documentation/tabulardata/column/subscript(_:)-52xy1)
- [subscript(Range<Int>) -> ColumnSlice<WrappedElement>](/documentation/tabulardata/column/subscript(_:)-gne9)

### Creating a Slice of Unique Elements

- [func distinct() -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/column/distinct())

### Creating a Slice by Masking Elements

- [subscript<C>(C) -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/column/subscript(_:)-56i2s)

### Encoding a Column

- [func encoded<Encoder>(using: Encoder) throws -> Column<Encoder.Output>](/documentation/tabulardata/column/encoded(using:))

### Decoding a Column

- [func decoded<T, Decoder>(T.Type, using: Decoder) throws -> Column<T>](/documentation/tabulardata/column/decoded(_:using:))

### Summarizing a Column

- [func summary() -> CategoricalSummary<WrappedElement>](/documentation/tabulardata/column/summary())
- [func numericSummary() -> NumericSummary<Double>](/documentation/tabulardata/column/numericsummary()-2m0sr)
- [func numericSummary() -> NumericSummary<WrappedElement>](/documentation/tabulardata/column/numericsummary()-8laeo)

### Getting Statistical Values

- [func sum() -> WrappedElement](/documentation/tabulardata/column/sum())
- [func min() -> Column<WrappedElement>.Element](/documentation/tabulardata/column/min())
- [func max() -> Column<WrappedElement>.Element](/documentation/tabulardata/column/max())
- [func mean() -> Double?](/documentation/tabulardata/column/mean()-2si7j)
- [func mean() -> Column<WrappedElement>.Element](/documentation/tabulardata/column/mean()-ic5z)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> Double?](/documentation/tabulardata/column/standarddeviation(deltadegreesoffreedom:)-9ffqu)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> Column<WrappedElement>.Element](/documentation/tabulardata/column/standarddeviation(deltadegreesoffreedom:)-4kc16)

### Describing a Column

- [var description: String](/documentation/tabulardata/column/description)
- [var debugDescription: String](/documentation/tabulardata/column/debugdescription)
- [var customMirror: Mirror](/documentation/tabulardata/column/custommirror)

### Modifying a Column with a Value

- [static func += (inout Column<WrappedElement>, WrappedElement)](/documentation/tabulardata/column/+=(_:_:)-94q8g)
- [static func -= (inout Column<WrappedElement>, WrappedElement)](/documentation/tabulardata/column/-=(_:_:)-8arlr)
- [static func *= (inout Column<WrappedElement>, WrappedElement)](/documentation/tabulardata/column/*=(_:_:)-4rraw)
- [static func /= (inout Column<WrappedElement>, WrappedElement)](/documentation/tabulardata/column/_=(_:_:)-8jmir)
- [static func /= (inout Column<WrappedElement>, WrappedElement)](/documentation/tabulardata/column/_=(_:_:)-3hfr5)

### Modifying a Column with a Collection of Values

- [static func += <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/+=(_:_:)-2w5o4)
- [static func += <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/+=(_:_:)-2scuy)
- [static func -= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/-=(_:_:)-8rgjq)
- [static func -= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/-=(_:_:)-3v0hh)
- [static func *= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/*=(_:_:)-8mmnn)
- [static func *= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/*=(_:_:)-6kp11)
- [static func /= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/_=(_:_:)-dnma)
- [static func /= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/_=(_:_:)-8xhzg)
- [static func /= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/_=(_:_:)-86t1j)
- [static func /= <C>(inout Column<WrappedElement>, C)](/documentation/tabulardata/column/_=(_:_:)-3acz8)

### Instance Methods

- [func withContiguousMutableStorageIfAvailable<R>((inout UnsafeMutableBufferPointer<WrappedElement>) throws -> R) rethrows -> R?](/documentation/tabulardata/column/withcontiguousmutablestorageifavailable(_:)-9j9p8)
- [func withContiguousStorageIfAvailable<R>((UnsafeBufferPointer<WrappedElement>) throws -> R) rethrows -> R?](/documentation/tabulardata/column/withcontiguousstorageifavailable(_:)-6nbz3)

### Default Implementations

- [BidirectionalCollection Implementations](/documentation/tabulardata/column/bidirectionalcollection-implementations)

#### Instance Properties

- [var endIndex: Int](/documentation/tabulardata/column/endindex)
- [var startIndex: Int](/documentation/tabulardata/column/startindex)

#### Instance Methods

- [func index(after: Int) -> Int](/documentation/tabulardata/column/index(after:))
- [func index(before: Int) -> Int](/documentation/tabulardata/column/index(before:))

#### Subscripts

- [subscript(Range<Int>) -> ColumnSlice<WrappedElement>](/documentation/tabulardata/column/subscript(_:)-gne9)
- [subscript(Int) -> Column<WrappedElement>.Element](/documentation/tabulardata/column/subscript(_:)-qm4d)
- [CustomDebugStringConvertible Implementations](/documentation/tabulardata/column/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/tabulardata/column/debugdescription)
- [CustomReflectable Implementations](/documentation/tabulardata/column/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/tabulardata/column/custommirror)
- [CustomStringConvertible Implementations](/documentation/tabulardata/column/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/column/description)
- [MutableCollection Implementations](/documentation/tabulardata/column/mutablecollection-implementations)

#### Instance Methods

- [func withContiguousMutableStorageIfAvailable<R>((inout UnsafeMutableBufferPointer<WrappedElement?>) throws -> R) rethrows -> R?](/documentation/tabulardata/column/withcontiguousmutablestorageifavailable(_:)-77itz)
- [Sequence Implementations](/documentation/tabulardata/column/sequence-implementations)

#### Instance Methods

- [func withContiguousStorageIfAvailable<R>((UnsafeBufferPointer<WrappedElement?>) throws -> R) rethrows -> R?](/documentation/tabulardata/column/withcontiguousstorageifavailable(_:)-539v3)
- [ColumnSlice](/documentation/tabulardata/columnslice)

### Creating a Column Slice

- [init(Column<WrappedElement>)](/documentation/tabulardata/columnslice/init(_:))

### Creating a Slice of Unique Elements

- [func distinct() -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/columnslice/distinct())

### Creating a Type-Erased Slice

- [func eraseToAnyColumn() -> AnyColumnSlice](/documentation/tabulardata/columnslice/erasetoanycolumn())

### Creating a Column of the Same Type

- [var prototype: any AnyColumnPrototype](/documentation/tabulardata/columnslice/prototype)

### Creating Transformed Columns

- [func map<T>((ColumnSlice<WrappedElement>.Element) throws -> T?) rethrows -> Column<T>](/documentation/tabulardata/columnslice/map(_:))

### Inspecting a Column Slice

- [var name: String](/documentation/tabulardata/columnslice/name)
- [var count: Int](/documentation/tabulardata/columnslice/count)
- [var wrappedElementType: any Any.Type](/documentation/tabulardata/columnslice/wrappedelementtype)
- [func argmin() -> Int?](/documentation/tabulardata/columnslice/argmin())
- [func argmax() -> Int?](/documentation/tabulardata/columnslice/argmax())
- [func isNil(at: Int) -> Bool](/documentation/tabulardata/columnslice/isnil(at:))

### Accessing Elements

- [subscript(Int) -> ColumnSlice<WrappedElement>.Element](/documentation/tabulardata/columnslice/subscript(_:)-38hn8)
- [subscript(Range<Int>) -> ColumnSlice<WrappedElement>](/documentation/tabulardata/columnslice/subscript(_:)-7lrhk)

### Summarizing a Column Slice

- [func summary() -> CategoricalSummary<WrappedElement>](/documentation/tabulardata/columnslice/summary())
- [func numericSummary() -> NumericSummary<Double>](/documentation/tabulardata/columnslice/numericsummary()-68ohj)
- [func numericSummary() -> NumericSummary<WrappedElement>](/documentation/tabulardata/columnslice/numericsummary()-5swa5)

### Getting Statistical Values

- [func sum() -> WrappedElement](/documentation/tabulardata/columnslice/sum())
- [func min() -> ColumnSlice<WrappedElement>.Element](/documentation/tabulardata/columnslice/min())
- [func max() -> ColumnSlice<WrappedElement>.Element](/documentation/tabulardata/columnslice/max())
- [func mean() -> Double?](/documentation/tabulardata/columnslice/mean()-3inzf)
- [func mean() -> ColumnSlice<WrappedElement>.Element](/documentation/tabulardata/columnslice/mean()-7u3i0)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> Double?](/documentation/tabulardata/columnslice/standarddeviation(deltadegreesoffreedom:)-1i05i)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> ColumnSlice<WrappedElement>.Element](/documentation/tabulardata/columnslice/standarddeviation(deltadegreesoffreedom:)-3d6vo)

### Describing a Column Slice

- [var description: String](/documentation/tabulardata/columnslice/description)
- [var debugDescription: String](/documentation/tabulardata/columnslice/debugdescription)
- [var customMirror: Mirror](/documentation/tabulardata/columnslice/custommirror)

### Comparing Two Column Slices

- [static func == (ColumnSlice<WrappedElement>, ColumnSlice<WrappedElement>) -> Bool](/documentation/tabulardata/columnslice/==(_:_:))

### Modifying a Column Slice with a Value

- [static func += (inout ColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/columnslice/+=(_:_:)-950qi)
- [static func -= (inout ColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/columnslice/-=(_:_:)-1n1gh)
- [static func *= (inout ColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/columnslice/*=(_:_:)-i6qs)
- [static func /= (inout ColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/columnslice/_=(_:_:)-8oi36)
- [static func /= (inout ColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/columnslice/_=(_:_:)-8pl3f)

### Modifying a Column Slice with a Collection of Values

- [static func += <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/+=(_:_:)-47cwm)
- [static func += <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/+=(_:_:)-4bgdt)
- [static func -= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/-=(_:_:)-3kauw)
- [static func -= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/-=(_:_:)-1bqy4)
- [static func *= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/*=(_:_:)-7lz8l)
- [static func *= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/*=(_:_:)-3v2q0)
- [static func /= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/_=(_:_:)-46jci)
- [static func /= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/_=(_:_:)-8frqe)
- [static func /= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/_=(_:_:)-1fciw)
- [static func /= <C>(inout ColumnSlice<WrappedElement>, C)](/documentation/tabulardata/columnslice/_=(_:_:)-6ujes)

### Hashing a Column Slice

- [func hash(into: inout Hasher)](/documentation/tabulardata/columnslice/hash(into:))

### Supporting Types

- [ColumnSlice.Element](/documentation/tabulardata/columnslice/element)
- [ColumnSlice.Index](/documentation/tabulardata/columnslice/index)

### Instance Properties

- [var missingCount: Int](/documentation/tabulardata/columnslice/missingcount)

### Default Implementations

- [BidirectionalCollection Implementations](/documentation/tabulardata/columnslice/bidirectionalcollection-implementations)

#### Instance Properties

- [var endIndex: Int](/documentation/tabulardata/columnslice/endindex)
- [var startIndex: Int](/documentation/tabulardata/columnslice/startindex)

#### Instance Methods

- [func index(after: Int) -> Int](/documentation/tabulardata/columnslice/index(after:))
- [func index(before: Int) -> Int](/documentation/tabulardata/columnslice/index(before:))

#### Subscripts

- [subscript(Int) -> ColumnSlice<WrappedElement>.Element](/documentation/tabulardata/columnslice/subscript(_:)-38hn8)
- [subscript(Range<Int>) -> ColumnSlice<WrappedElement>](/documentation/tabulardata/columnslice/subscript(_:)-7lrhk)
- [Collection Implementations](/documentation/tabulardata/columnslice/collection-implementations)

#### Instance Properties

- [var count: Int](/documentation/tabulardata/columnslice/count)
- [CustomDebugStringConvertible Implementations](/documentation/tabulardata/columnslice/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/tabulardata/columnslice/debugdescription)
- [CustomReflectable Implementations](/documentation/tabulardata/columnslice/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/tabulardata/columnslice/custommirror)
- [CustomStringConvertible Implementations](/documentation/tabulardata/columnslice/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/columnslice/description)
- [Equatable Implementations](/documentation/tabulardata/columnslice/equatable-implementations)

#### Operators

- [static func == (ColumnSlice<WrappedElement>, ColumnSlice<WrappedElement>) -> Bool](/documentation/tabulardata/columnslice/==(_:_:))
- [Hashable Implementations](/documentation/tabulardata/columnslice/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/tabulardata/columnslice/hash(into:))
- [FilledColumn](/documentation/tabulardata/filledcolumn)

### Inspecting a Column

- [var name: String](/documentation/tabulardata/filledcolumn/name)

### Finding an Element Index

- [func argmin() -> Base.Index?](/documentation/tabulardata/filledcolumn/argmin())
- [func argmax() -> FilledColumn<Base>.Index?](/documentation/tabulardata/filledcolumn/argmax())

### Accessing Elements

- [subscript(Base.Index) -> Base.WrappedElement](/documentation/tabulardata/filledcolumn/subscript(_:))

### Summarizing a Column

- [func summary() -> CategoricalSummary<FilledColumn<Base>.WrappedElement>](/documentation/tabulardata/filledcolumn/summary())
- [func numericSummary() -> NumericSummary<Double>](/documentation/tabulardata/filledcolumn/numericsummary()-3ao8s)
- [func numericSummary() -> NumericSummary<Base.WrappedElement>](/documentation/tabulardata/filledcolumn/numericsummary()-86mgh)

### Getting Statistical Values

- [func sum() -> FilledColumn<Base>.Element](/documentation/tabulardata/filledcolumn/sum()-5836l)
- [func sum() -> FilledColumn<Base>.Element](/documentation/tabulardata/filledcolumn/sum()-2805h)
- [func min() -> FilledColumn<Base>.Element?](/documentation/tabulardata/filledcolumn/min())
- [func max() -> FilledColumn<Base>.Element?](/documentation/tabulardata/filledcolumn/max())
- [func mean() -> Double?](/documentation/tabulardata/filledcolumn/mean()-8xs60)
- [func mean() -> FilledColumn<Base>.Element?](/documentation/tabulardata/filledcolumn/mean()-jd3v)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> Double?](/documentation/tabulardata/filledcolumn/standarddeviation(deltadegreesoffreedom:)-4cofd)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> FilledColumn<Base>.Element?](/documentation/tabulardata/filledcolumn/standarddeviation(deltadegreesoffreedom:)-27xnl)

### Describing a Column

- [var description: String](/documentation/tabulardata/filledcolumn/description)
- [var debugDescription: String](/documentation/tabulardata/filledcolumn/debugdescription)
- [func description(options: FormattingOptions) -> String](/documentation/tabulardata/filledcolumn/description(options:))

### Supporting Types

- [FilledColumn.Element](/documentation/tabulardata/filledcolumn/element)
- [FilledColumn.WrappedElement](/documentation/tabulardata/filledcolumn/wrappedelement)

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/tabulardata/filledcolumn/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/filledcolumn/description)
- [DiscontiguousColumnSlice](/documentation/tabulardata/discontiguouscolumnslice)

### Creating a Column Slice

- [init(Column<WrappedElement>)](/documentation/tabulardata/discontiguouscolumnslice/init(_:))
- [init(column: Column<WrappedElement>, ranges: [Range<Int>])](/documentation/tabulardata/discontiguouscolumnslice/init(column:ranges:))

### Creating a Slice of Unique Elements

- [func distinct() -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/discontiguouscolumnslice/distinct())

### Creating a Type-Erased Slice

- [func eraseToAnyColumn() -> AnyColumnSlice](/documentation/tabulardata/discontiguouscolumnslice/erasetoanycolumn())

### Creating a Column of the Same Type

- [var prototype: any AnyColumnPrototype](/documentation/tabulardata/discontiguouscolumnslice/prototype)

### Creating Transformed Columns

- [func map<T>((DiscontiguousColumnSlice<WrappedElement>.Element) throws -> T?) rethrows -> Column<T>](/documentation/tabulardata/discontiguouscolumnslice/map(_:))

### Inspecting a Column Slice

- [var name: String](/documentation/tabulardata/discontiguouscolumnslice/name)
- [var count: Int](/documentation/tabulardata/discontiguouscolumnslice/count)
- [var wrappedElementType: any Any.Type](/documentation/tabulardata/discontiguouscolumnslice/wrappedelementtype)
- [func argmin() -> Int?](/documentation/tabulardata/discontiguouscolumnslice/argmin())
- [func argmax() -> Int?](/documentation/tabulardata/discontiguouscolumnslice/argmax())
- [func isNil(at: Int) -> Bool](/documentation/tabulardata/discontiguouscolumnslice/isnil(at:))

### Accessing Elements

- [subscript(Int) -> DiscontiguousColumnSlice<WrappedElement>.Element](/documentation/tabulardata/discontiguouscolumnslice/subscript(_:)-9y37v)
- [subscript(Range<Int>) -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/discontiguouscolumnslice/subscript(_:)-8rd2f)
- [subscript<R>(R) -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/discontiguouscolumnslice/subscript(_:)-4k2lh)
- [subscript((UnboundedRange_) -> ()) -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/discontiguouscolumnslice/subscript(_:)-5xvit)

### Summarizing a Column Slice

- [func summary() -> CategoricalSummary<WrappedElement>](/documentation/tabulardata/discontiguouscolumnslice/summary())
- [func numericSummary() -> NumericSummary<Double>](/documentation/tabulardata/discontiguouscolumnslice/numericsummary()-3r7pn)
- [func numericSummary() -> NumericSummary<WrappedElement>](/documentation/tabulardata/discontiguouscolumnslice/numericsummary()-4b7m0)

### Getting Statistical Values

- [func sum() -> WrappedElement](/documentation/tabulardata/discontiguouscolumnslice/sum())
- [func min() -> DiscontiguousColumnSlice<WrappedElement>.Element](/documentation/tabulardata/discontiguouscolumnslice/min())
- [func max() -> DiscontiguousColumnSlice<WrappedElement>.Element](/documentation/tabulardata/discontiguouscolumnslice/max())
- [func mean() -> DiscontiguousColumnSlice<WrappedElement>.Element](/documentation/tabulardata/discontiguouscolumnslice/mean()-3y11c)
- [func mean() -> Double?](/documentation/tabulardata/discontiguouscolumnslice/mean()-49u93)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> Double?](/documentation/tabulardata/discontiguouscolumnslice/standarddeviation(deltadegreesoffreedom:)-36nx2)
- [func standardDeviation(deltaDegreesOfFreedom: Int) -> DiscontiguousColumnSlice<WrappedElement>.Element](/documentation/tabulardata/discontiguouscolumnslice/standarddeviation(deltadegreesoffreedom:)-5vd4r)

### Describing a Column Slice

- [var description: String](/documentation/tabulardata/discontiguouscolumnslice/description)
- [var debugDescription: String](/documentation/tabulardata/discontiguouscolumnslice/debugdescription)
- [var customMirror: Mirror](/documentation/tabulardata/discontiguouscolumnslice/custommirror)

### Comparing Two Column Slices

- [static func == (DiscontiguousColumnSlice<WrappedElement>, DiscontiguousColumnSlice<WrappedElement>) -> Bool](/documentation/tabulardata/discontiguouscolumnslice/==(_:_:))

### Modifying a Column Slice with a Value

- [static func += (inout DiscontiguousColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/discontiguouscolumnslice/+=(_:_:)-1mzz0)
- [static func -= (inout DiscontiguousColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/discontiguouscolumnslice/-=(_:_:)-2yrui)
- [static func *= (inout DiscontiguousColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/discontiguouscolumnslice/*=(_:_:)-7gcqc)
- [static func /= (inout DiscontiguousColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/discontiguouscolumnslice/_=(_:_:)-1g0yb)
- [static func /= (inout DiscontiguousColumnSlice<WrappedElement>, WrappedElement)](/documentation/tabulardata/discontiguouscolumnslice/_=(_:_:)-6i7hx)

### Modifying a Column Slice with a Collection of Values

- [static func += <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/+=(_:_:)-2jxz1)
- [static func += <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/+=(_:_:)-lpai)
- [static func -= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/-=(_:_:)-9nkq6)
- [static func -= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/-=(_:_:)-8a20q)
- [static func *= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/*=(_:_:)-9jg9h)
- [static func *= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/*=(_:_:)-18nlr)
- [static func /= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/_=(_:_:)-6xf9s)
- [static func /= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/_=(_:_:)-1mzcg)
- [static func /= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/_=(_:_:)-39wsi)
- [static func /= <C>(inout DiscontiguousColumnSlice<WrappedElement>, C)](/documentation/tabulardata/discontiguouscolumnslice/_=(_:_:)-6lzj)

### Hashing a Column Slice

- [func hash(into: inout Hasher)](/documentation/tabulardata/discontiguouscolumnslice/hash(into:))

### Supporting Types

- [DiscontiguousColumnSlice.Element](/documentation/tabulardata/discontiguouscolumnslice/element)
- [DiscontiguousColumnSlice.Index](/documentation/tabulardata/discontiguouscolumnslice/index)

### Instance Properties

- [var missingCount: Int](/documentation/tabulardata/discontiguouscolumnslice/missingcount)

### Default Implementations

- [BidirectionalCollection Implementations](/documentation/tabulardata/discontiguouscolumnslice/bidirectionalcollection-implementations)

#### Instance Properties

- [var endIndex: Int](/documentation/tabulardata/discontiguouscolumnslice/endindex)
- [var startIndex: Int](/documentation/tabulardata/discontiguouscolumnslice/startindex)

#### Instance Methods

- [func index(after: Int) -> Int](/documentation/tabulardata/discontiguouscolumnslice/index(after:))
- [func index(before: Int) -> Int](/documentation/tabulardata/discontiguouscolumnslice/index(before:))

#### Subscripts

- [subscript(Range<Int>) -> DiscontiguousColumnSlice<WrappedElement>](/documentation/tabulardata/discontiguouscolumnslice/subscript(_:)-8rd2f)
- [subscript(Int) -> DiscontiguousColumnSlice<WrappedElement>.Element](/documentation/tabulardata/discontiguouscolumnslice/subscript(_:)-9y37v)
- [Collection Implementations](/documentation/tabulardata/discontiguouscolumnslice/collection-implementations)

#### Instance Properties

- [var count: Int](/documentation/tabulardata/discontiguouscolumnslice/count)
- [CustomDebugStringConvertible Implementations](/documentation/tabulardata/discontiguouscolumnslice/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/tabulardata/discontiguouscolumnslice/debugdescription)
- [CustomReflectable Implementations](/documentation/tabulardata/discontiguouscolumnslice/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/tabulardata/discontiguouscolumnslice/custommirror)
- [CustomStringConvertible Implementations](/documentation/tabulardata/discontiguouscolumnslice/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/discontiguouscolumnslice/description)
- [Equatable Implementations](/documentation/tabulardata/discontiguouscolumnslice/equatable-implementations)

#### Operators

- [static func == (DiscontiguousColumnSlice<WrappedElement>, DiscontiguousColumnSlice<WrappedElement>) -> Bool](/documentation/tabulardata/discontiguouscolumnslice/==(_:_:))
- [Hashable Implementations](/documentation/tabulardata/discontiguouscolumnslice/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/tabulardata/discontiguouscolumnslice/hash(into:))
- [ColumnProtocol](/documentation/tabulardata/columnprotocol)

### Inspecting a Column Type

- [var name: String](/documentation/tabulardata/columnprotocol/name)

### Generating a Column by Adding Two Columns

- [static func + (Self, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/+(_:_:)-yc11)
- [func + <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/+(_:_:)-1i7oh)
- [func + <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/+(_:_:)-3exmp)

### Generating a Column by Subtracting Two Columns

- [static func - (Self, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/-(_:_:)-36zol)
- [func - <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/-(_:_:)-25cs6)
- [func - <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/-(_:_:)-95yoe)

### Generating a Column by Multiplying Two Columns

- [static func * (Self, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/*(_:_:)-9db1q)
- [func * <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/*(_:_:)-l9r3)
- [func * <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/*(_:_:)-2toor)

### Generating a Column by Dividing Two Columns

- [static func / (Self, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/_(_:_:)-922ku)
- [func / <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/_(_:_:)-9v3nw)
- [func / <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/_(_:_:)-4igyw)
- [static func / (Self, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/_(_:_:)-2urf0)
- [func / <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/_(_:_:)-4pr65)
- [func / <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/_(_:_:)-58kg6)

### Generating a Column by Combining a Value

- [static func + (Self, Self.Element) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/+(_:_:)-39k8v)
- [static func + (Self.Element, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/+(_:_:)-94kiv)
- [static func - (Self.Element, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/-(_:_:)-4fynh)
- [static func - (Self, Self.Element) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/-(_:_:)-6up21)
- [static func * (Self, Self.Element) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/*(_:_:)-17vqd)
- [static func * (Self.Element, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/*(_:_:)-3d6lu)
- [static func / (Self, Self.Element) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/_(_:_:)-4a632)
- [static func / (Self.Element, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/_(_:_:)-7pe3t)
- [static func / (Self, Self.Element) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/_(_:_:)-6zigz)
- [static func / (Self.Element, Self) -> Column<Self.Element>](/documentation/tabulardata/columnprotocol/_(_:_:)-4iv15)

### Comparing a Column with a Value

- [static func == (Self, Self.Element) -> [Bool]](/documentation/tabulardata/columnprotocol/==(_:_:)-5jc0x)
- [static func == (Self.Element, Self) -> [Bool]](/documentation/tabulardata/columnprotocol/==(_:_:)-4hx04)
- [static func != (Self, Self.Element) -> [Bool]](/documentation/tabulardata/columnprotocol/!=(_:_:)-557vb)
- [static func != (Self.Element, Self) -> [Bool]](/documentation/tabulardata/columnprotocol/!=(_:_:)-72ddh)

### Operators

- [static func > (Self.Element, Self) -> [Bool]](/documentation/tabulardata/columnprotocol/_(_:_:)-68any)
- [static func < (Self.Element, Self) -> [Bool]](/documentation/tabulardata/columnprotocol/_(_:_:)-70vl1)
- [static func < (Self, Self.Element) -> [Bool]](/documentation/tabulardata/columnprotocol/_(_:_:)-7gy2j)
- [static func > (Self, Self.Element) -> [Bool]](/documentation/tabulardata/columnprotocol/_(_:_:)-9rct2)
- [static func <= (Self.Element, Self) -> [Bool]](/documentation/tabulardata/columnprotocol/_=(_:_:)-17m6l)
- [static func >= (Self, Self.Element) -> [Bool]](/documentation/tabulardata/columnprotocol/_=(_:_:)-2w8gt)
- [static func >= (Self.Element, Self) -> [Bool]](/documentation/tabulardata/columnprotocol/_=(_:_:)-8jak4)
- [static func <= (Self, Self.Element) -> [Bool]](/documentation/tabulardata/columnprotocol/_=(_:_:)-9wr8s)
- [OptionalColumnProtocol](/documentation/tabulardata/optionalcolumnprotocol)

### Filling an Optional Column

- [func filled(with: Self.WrappedElement) -> FilledColumn<Self>](/documentation/tabulardata/optionalcolumnprotocol/filled(with:))

### Generating an Optional Column by Adding Two Columns

- [static func + (Self, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/+(_:_:)-2qex0)
- [func + <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/+(_:_:)-1i7oh)
- [func + <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/+(_:_:)-3exmp)

### Generating an Optional Column by Subtracting Two Columns

- [static func - (Self, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/-(_:_:)-5xfkx)
- [func - <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/-(_:_:)-25cs6)
- [func - <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/-(_:_:)-95yoe)

### Generating an Optional Column by Multiplying Two Columns

- [static func * (Self, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/*(_:_:)-5f5kx)
- [func * <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/*(_:_:)-2toor)
- [func * <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/*(_:_:)-l9r3)

### Generating an Optional Column by Dividing Two Columns

- [static func / (Self, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/_(_:_:)-4nmnl)
- [func / <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/_(_:_:)-9v3nw)
- [func / <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/_(_:_:)-4igyw)
- [static func / (Self, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/_(_:_:)-3rlo3)
- [func / <L, R>(L, R) -> Column<L.Element>](/documentation/tabulardata/_(_:_:)-4pr65)
- [func / <L, R>(L, R) -> Column<R.Element>](/documentation/tabulardata/_(_:_:)-58kg6)

### Generating an Optional Column by Combining a Value

- [static func + (Self, Self.WrappedElement) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/+(_:_:)-501gg)
- [static func + (Self.WrappedElement, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/+(_:_:)-6ko8x)
- [static func - (Self, Self.WrappedElement) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/-(_:_:)-9mejf)
- [static func - (Self.WrappedElement, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/-(_:_:)-5vffa)
- [static func * (Self, Self.WrappedElement) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/*(_:_:)-orkq)
- [static func * (Self.WrappedElement, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/*(_:_:)-5vorv)
- [static func / (Self, Self.WrappedElement) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/_(_:_:)-7tbmq)
- [static func / (Self.WrappedElement, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/_(_:_:)-56h1d)
- [static func / (Self, Self.WrappedElement) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/_(_:_:)-5qhxr)
- [static func / (Self.WrappedElement, Self) -> Column<Self.WrappedElement>](/documentation/tabulardata/optionalcolumnprotocol/_(_:_:)-2xfqa)

### Describing an Optional Column

- [func description(options: FormattingOptions) -> String](/documentation/tabulardata/optionalcolumnprotocol/description(options:))

### Supporting Types

- [WrappedElement](/documentation/tabulardata/optionalcolumnprotocol/wrappedelement)

## Type-Erased Columns

- [AnyColumn](/documentation/tabulardata/anycolumn)

### Inspecting a Type-Erased Column

- [var name: String](/documentation/tabulardata/anycolumn/name)
- [var count: Int](/documentation/tabulardata/anycolumn/count)
- [var missingCount: Int](/documentation/tabulardata/anycolumn/missingcount)
- [var wrappedElementType: any Any.Type](/documentation/tabulardata/anycolumn/wrappedelementtype)
- [func isNil(at: Int) -> Bool](/documentation/tabulardata/anycolumn/isnil(at:))

### Creating a Column of the Same Type

- [var prototype: any AnyColumnPrototype](/documentation/tabulardata/anycolumn/prototype)

### Creating a Typed Column

- [func assumingType<T>(T.Type) -> Column<T>](/documentation/tabulardata/anycolumn/assumingtype(_:))

### Adding Elements

- [func append(Any?)](/documentation/tabulardata/anycolumn/append(_:))
- [func append(contentsOf: AnyColumn)](/documentation/tabulardata/anycolumn/append(contentsof:)-2in58)
- [func append(contentsOf: AnyColumnSlice)](/documentation/tabulardata/anycolumn/append(contentsof:)-az5b)

### Removing an Element

- [func remove(at: Int)](/documentation/tabulardata/anycolumn/remove(at:))

### Accessing Elements

- [subscript(Int) -> Any?](/documentation/tabulardata/anycolumn/subscript(_:)-6z1b5)
- [subscript(Range<Int>) -> AnyColumnSlice](/documentation/tabulardata/anycolumn/subscript(_:)-1n9t9)

### Creating a Slice of Unique Elements

- [func distinct() -> AnyColumnSlice](/documentation/tabulardata/anycolumn/distinct())

### Creating a Slice by Masking Elements

- [subscript<C>(C) -> AnyColumnSlice](/documentation/tabulardata/anycolumn/subscript(_:)-3658g)

### Encoding a Column

- [func encode<T, Encoder>(T.Type, using: Encoder) throws](/documentation/tabulardata/anycolumn/encode(_:using:))
- [func encoded<T, Encoder>(T.Type, using: Encoder) throws -> AnyColumn](/documentation/tabulardata/anycolumn/encoded(_:using:))

### Decoding a Column

- [func decode<T, Decoder>(T.Type, using: Decoder) throws](/documentation/tabulardata/anycolumn/decode(_:using:))
- [func decoded<T, Decoder>(T.Type, using: Decoder) throws -> AnyColumn](/documentation/tabulardata/anycolumn/decoded(_:using:))

### Describing a Column

- [var description: String](/documentation/tabulardata/anycolumn/description)
- [var debugDescription: String](/documentation/tabulardata/anycolumn/debugdescription)
- [var customMirror: Mirror](/documentation/tabulardata/anycolumn/custommirror)

### Comparing Two Columns

- [static func == (AnyColumn, AnyColumn) -> Bool](/documentation/tabulardata/anycolumn/==(_:_:))

### Hashing a Column

- [func hash(into: inout Hasher)](/documentation/tabulardata/anycolumn/hash(into:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/tabulardata/anycolumn/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/tabulardata/anycolumn/debugdescription)
- [CustomReflectable Implementations](/documentation/tabulardata/anycolumn/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/tabulardata/anycolumn/custommirror)
- [CustomStringConvertible Implementations](/documentation/tabulardata/anycolumn/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/anycolumn/description)
- [Equatable Implementations](/documentation/tabulardata/anycolumn/equatable-implementations)

#### Operators

- [static func == (AnyColumn, AnyColumn) -> Bool](/documentation/tabulardata/anycolumn/==(_:_:))
- [Hashable Implementations](/documentation/tabulardata/anycolumn/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/tabulardata/anycolumn/hash(into:))
- [RandomAccessCollection Implementations](/documentation/tabulardata/anycolumn/randomaccesscollection-implementations)

#### Instance Properties

- [var endIndex: Int](/documentation/tabulardata/anycolumn/endindex)
- [var startIndex: Int](/documentation/tabulardata/anycolumn/startindex)

#### Instance Methods

- [func index(after: Int) -> Int](/documentation/tabulardata/anycolumn/index(after:))
- [func index(before: Int) -> Int](/documentation/tabulardata/anycolumn/index(before:))

#### Subscripts

- [subscript(Range<Int>) -> AnyColumnSlice](/documentation/tabulardata/anycolumn/subscript(_:)-1n9t9)
- [subscript(Int) -> Any?](/documentation/tabulardata/anycolumn/subscript(_:)-6z1b5)
- [AnyColumnSlice](/documentation/tabulardata/anycolumnslice)

### Inspecting a Type-Erased Column Slice

- [var name: String](/documentation/tabulardata/anycolumnslice/name)
- [var count: Int](/documentation/tabulardata/anycolumnslice/count)
- [var missingCount: Int](/documentation/tabulardata/anycolumnslice/missingcount)
- [var wrappedElementType: any Any.Type](/documentation/tabulardata/anycolumnslice/wrappedelementtype)
- [func isNil(at: Int) -> Bool](/documentation/tabulardata/anycolumnslice/isnil(at:))

### Converting to a Typed Column Slice

- [func assumingType<T>(T.Type) -> DiscontiguousColumnSlice<T>](/documentation/tabulardata/anycolumnslice/assumingtype(_:))

### Accessing Elements

- [subscript(Int) -> Any?](/documentation/tabulardata/anycolumnslice/subscript(_:)-g0gb)
- [subscript(Range<Int>) -> AnyColumnSlice](/documentation/tabulardata/anycolumnslice/subscript(_:)-3qisq)

### Creating a Slice of Unique Elements

- [func distinct() -> AnyColumnSlice](/documentation/tabulardata/anycolumnslice/distinct())

### Summarizing a Column Slice

- [func summary() -> AnyCategoricalSummary](/documentation/tabulardata/anycolumnslice/summary())

### Describing a Column Slice

- [var description: String](/documentation/tabulardata/anycolumnslice/description)
- [var debugDescription: String](/documentation/tabulardata/anycolumnslice/debugdescription)
- [var customMirror: Mirror](/documentation/tabulardata/anycolumnslice/custommirror)

### Comparing Two Column Slices

- [static func == (AnyColumnSlice, AnyColumnSlice) -> Bool](/documentation/tabulardata/anycolumnslice/==(_:_:))

### Hashing a Column Slice

- [func hash(into: inout Hasher)](/documentation/tabulardata/anycolumnslice/hash(into:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/tabulardata/anycolumnslice/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/tabulardata/anycolumnslice/debugdescription)
- [CustomReflectable Implementations](/documentation/tabulardata/anycolumnslice/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/tabulardata/anycolumnslice/custommirror)
- [CustomStringConvertible Implementations](/documentation/tabulardata/anycolumnslice/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/anycolumnslice/description)
- [Equatable Implementations](/documentation/tabulardata/anycolumnslice/equatable-implementations)

#### Operators

- [static func == (AnyColumnSlice, AnyColumnSlice) -> Bool](/documentation/tabulardata/anycolumnslice/==(_:_:))
- [Hashable Implementations](/documentation/tabulardata/anycolumnslice/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/tabulardata/anycolumnslice/hash(into:))
- [RandomAccessCollection Implementations](/documentation/tabulardata/anycolumnslice/randomaccesscollection-implementations)

#### Instance Properties

- [var endIndex: Int](/documentation/tabulardata/anycolumnslice/endindex)
- [var startIndex: Int](/documentation/tabulardata/anycolumnslice/startindex)

#### Instance Methods

- [func index(after: Int) -> Int](/documentation/tabulardata/anycolumnslice/index(after:))
- [func index(before: Int) -> Int](/documentation/tabulardata/anycolumnslice/index(before:))

#### Subscripts

- [subscript(Range<Int>) -> AnyColumnSlice](/documentation/tabulardata/anycolumnslice/subscript(_:)-3qisq)
- [subscript(Int) -> Any?](/documentation/tabulardata/anycolumnslice/subscript(_:)-g0gb)
- [AnyColumnProtocol](/documentation/tabulardata/anycolumnprotocol)

### Inspecting a Type-Erased Column Type

- [var name: String](/documentation/tabulardata/anycolumnprotocol/name)
- [var count: Int](/documentation/tabulardata/anycolumnprotocol/count)
- [var wrappedElementType: any Any.Type](/documentation/tabulardata/anycolumnprotocol/wrappedelementtype)

### Retrieving Elements

- [subscript(Int) -> Any?](/documentation/tabulardata/anycolumnprotocol/subscript(_:)-1dl8y)
- [subscript(Range<Int>) -> AnyColumnSlice](/documentation/tabulardata/anycolumnprotocol/subscript(_:)-81v4q)
- [AnyColumnPrototype](/documentation/tabulardata/anycolumnprototype)

### Naming a Prototype Column

- [var name: String](/documentation/tabulardata/anycolumnprototype/name)

### Creating Columns

- [func makeColumn(capacity: Int) -> AnyColumn](/documentation/tabulardata/anycolumnprototype/makecolumn(capacity:))

## Statistical Summaries

- [NumericSummary](/documentation/tabulardata/numericsummary)

### Creating a Summary

- [init()](/documentation/tabulardata/numericsummary/init())
- [init(someCount: Int, noneCount: Int, mean: Element, standardDeviation: Element, min: Element, max: Element, median: Element, firstQuartile: Element, thirdQuartile: Element)](/documentation/tabulardata/numericsummary/init(somecount:nonecount:mean:standarddeviation:min:max:median:firstquartile:thirdquartile:))

### Inspecting a Summary

- [var debugDescription: String](/documentation/tabulardata/numericsummary/debugdescription)
- [var someCount: Int](/documentation/tabulardata/numericsummary/somecount)
- [var noneCount: Int](/documentation/tabulardata/numericsummary/nonecount)
- [var totalCount: Int](/documentation/tabulardata/numericsummary/totalcount)

### Getting Statistical Values

- [var max: Element](/documentation/tabulardata/numericsummary/max)
- [var mean: Element](/documentation/tabulardata/numericsummary/mean)
- [var median: Element](/documentation/tabulardata/numericsummary/median)
- [var min: Element](/documentation/tabulardata/numericsummary/min)
- [var standardDeviation: Element](/documentation/tabulardata/numericsummary/standarddeviation)
- [var firstQuartile: Element](/documentation/tabulardata/numericsummary/firstquartile)
- [var thirdQuartile: Element](/documentation/tabulardata/numericsummary/thirdquartile)
- [CategoricalSummary](/documentation/tabulardata/categoricalsummary)

### Creating a Summary

- [init()](/documentation/tabulardata/categoricalsummary/init())
- [init(someCount: Int, noneCount: Int, uniqueCount: Int, mode: [Element])](/documentation/tabulardata/categoricalsummary/init(somecount:nonecount:uniquecount:mode:))

### Inspecting a Summary

- [var debugDescription: String](/documentation/tabulardata/categoricalsummary/debugdescription)
- [var mode: [Element]](/documentation/tabulardata/categoricalsummary/mode)
- [var uniqueCount: Int](/documentation/tabulardata/categoricalsummary/uniquecount)
- [var someCount: Int](/documentation/tabulardata/categoricalsummary/somecount)
- [var noneCount: Int](/documentation/tabulardata/categoricalsummary/nonecount)
- [var totalCount: Int](/documentation/tabulardata/categoricalsummary/totalcount)
- [AnyCategoricalSummary](/documentation/tabulardata/anycategoricalsummary)

### Getting Statistical Information

- [var noneCount: Int](/documentation/tabulardata/anycategoricalsummary/nonecount)
- [var someCount: Int](/documentation/tabulardata/anycategoricalsummary/somecount)
- [var totalCount: Int](/documentation/tabulardata/anycategoricalsummary/totalcount)
- [var uniqueCount: Int](/documentation/tabulardata/anycategoricalsummary/uniquecount)

### Getting Mode Information

- [var mode: [Any]](/documentation/tabulardata/anycategoricalsummary/mode)
- [var modeType: any Any.Type](/documentation/tabulardata/anycategoricalsummary/modetype)

### Operators

- [static func == (AnyCategoricalSummary, AnyCategoricalSummary) -> Bool](/documentation/tabulardata/anycategoricalsummary/==(_:_:))

### Initializers

- [init(CategoricalSummary<AnyHashable>)](/documentation/tabulardata/anycategoricalsummary/init(_:)-7p9bv)
- [init<T>(CategoricalSummary<T>)](/documentation/tabulardata/anycategoricalsummary/init(_:)-8innt)

## Errors

- [JSONReadingError](/documentation/tabulardata/jsonreadingerror)

### Getting Error Information

- [case failedToParse(row: Int, column: String, type: JSONType, contents: String)](/documentation/tabulardata/jsonreadingerror/failedtoparse(row:column:type:contents:))
- [case incompatibleValues(column: String)](/documentation/tabulardata/jsonreadingerror/incompatiblevalues(column:))
- [case unsupportedStructure](/documentation/tabulardata/jsonreadingerror/unsupportedstructure)
- [case wrongType(row: Int, column: String, expectedType: JSONType, value: any Sendable)](/documentation/tabulardata/jsonreadingerror/wrongtype(row:column:expectedtype:value:))

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/tabulardata/jsonreadingerror/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/jsonreadingerror/description)
- [LocalizedError Implementations](/documentation/tabulardata/jsonreadingerror/localizederror-implementations)

#### Instance Properties

- [var errorDescription: String?](/documentation/tabulardata/jsonreadingerror/errordescription)
- [CSVReadingError](/documentation/tabulardata/csvreadingerror)

### Getting Error Information

- [var column: Int?](/documentation/tabulardata/csvreadingerror/column)
- [var row: Int](/documentation/tabulardata/csvreadingerror/row)
- [case badEncoding(row: Int, column: Int, cellContents: Data)](/documentation/tabulardata/csvreadingerror/badencoding(row:column:cellcontents:))
- [case failedToParse(row: Int, column: Int, type: CSVType, cellContents: Data)](/documentation/tabulardata/csvreadingerror/failedtoparse(row:column:type:cellcontents:))
- [case misplacedQuote(row: Int, column: Int)](/documentation/tabulardata/csvreadingerror/misplacedquote(row:column:))
- [case missingColumn(columnName: String)](/documentation/tabulardata/csvreadingerror/missingcolumn(columnname:))
- [case unsupportedEncoding(String)](/documentation/tabulardata/csvreadingerror/unsupportedencoding(_:))
- [case wrongNumberOfColumns(row: Int, columns: Int, expected: Int)](/documentation/tabulardata/csvreadingerror/wrongnumberofcolumns(row:columns:expected:))

### Enumeration Cases

- [case outOfBounds(requested: Int, actual: Int)](/documentation/tabulardata/csvreadingerror/outofbounds(requested:actual:))
- [case unsupportedColumnType(columnIndex: Int, columnName: String, type: String)](/documentation/tabulardata/csvreadingerror/unsupportedcolumntype(columnindex:columnname:type:))

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/tabulardata/csvreadingerror/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/csvreadingerror/description)
- [LocalizedError Implementations](/documentation/tabulardata/csvreadingerror/localizederror-implementations)

#### Instance Properties

- [var errorDescription: String?](/documentation/tabulardata/csvreadingerror/errordescription)
- [CSVWritingError](/documentation/tabulardata/csvwritingerror)

### Getting Error Information

- [var column: String?](/documentation/tabulardata/csvwritingerror/column)
- [var row: Int](/documentation/tabulardata/csvwritingerror/row)
- [case badEncoding(row: Int, column: String, Data)](/documentation/tabulardata/csvwritingerror/badencoding(row:column:_:))

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/tabulardata/csvwritingerror/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/csvwritingerror/description)
- [ColumnDecodingError](/documentation/tabulardata/columndecodingerror)

### Creating a Decoding Error

- [init(columnName: String, rowIndex: Int, decodingError: DecodingError)](/documentation/tabulardata/columndecodingerror/init(columnname:rowindex:decodingerror:))

### Getting Error Information

- [var columnName: String](/documentation/tabulardata/columndecodingerror/columnname)
- [var debugDescription: String](/documentation/tabulardata/columndecodingerror/debugdescription)
- [var decodingError: DecodingError](/documentation/tabulardata/columndecodingerror/decodingerror)
- [var rowIndex: Int](/documentation/tabulardata/columndecodingerror/rowindex)
- [ColumnEncodingError](/documentation/tabulardata/columnencodingerror)

### Creating an Encoding Error

- [init(columnName: String, rowIndex: Int, encodingError: EncodingError)](/documentation/tabulardata/columnencodingerror/init(columnname:rowindex:encodingerror:))

### Getting Error Information

- [var columnName: String](/documentation/tabulardata/columnencodingerror/columnname)
- [var debugDescription: String](/documentation/tabulardata/columnencodingerror/debugdescription)
- [var encodingError: EncodingError](/documentation/tabulardata/columnencodingerror/encodingerror)
- [var rowIndex: Int](/documentation/tabulardata/columnencodingerror/rowindex)
- [SFrameReadingError](/documentation/tabulardata/sframereadingerror)

### Getting Error Information

- [case badArchive(String)](/documentation/tabulardata/sframereadingerror/badarchive(_:))
- [case badEncoding(String)](/documentation/tabulardata/sframereadingerror/badencoding(_:))
- [case missingArchive](/documentation/tabulardata/sframereadingerror/missingarchive)
- [case missingColumn(String)](/documentation/tabulardata/sframereadingerror/missingcolumn(_:))
- [case unsupportedArchive(String)](/documentation/tabulardata/sframereadingerror/unsupportedarchive(_:))
- [case unsupportedLayout(String)](/documentation/tabulardata/sframereadingerror/unsupportedlayout(_:))
- [case unsupportedType(Int)](/documentation/tabulardata/sframereadingerror/unsupportedtype(_:))

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/tabulardata/sframereadingerror/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/sframereadingerror/description)
- [LocalizedError Implementations](/documentation/tabulardata/sframereadingerror/localizederror-implementations)

#### Instance Properties

- [var errorDescription: String?](/documentation/tabulardata/sframereadingerror/errordescription)

## Supporting Types

- [Order](/documentation/tabulardata/order)

### Getting the Properties

- [case ascending](/documentation/tabulardata/order/ascending)
- [case descending](/documentation/tabulardata/order/descending)
- [func areOrdered<T>(T, T) -> Bool](/documentation/tabulardata/order/areordered(_:_:))
- [ColumnID](/documentation/tabulardata/columnid)

### Creating a Column ID

- [init(String, T.Type)](/documentation/tabulardata/columnid/init(_:_:))

### Getting the Properties

- [var name: String](/documentation/tabulardata/columnid/name)

### Instance Properties

- [var type: any Any.Type](/documentation/tabulardata/columnid/type)

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/tabulardata/columnid/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/tabulardata/columnid/description)
- [FormattingOptions](/documentation/tabulardata/formattingoptions)

### Creating the Options Object

- [init()](/documentation/tabulardata/formattingoptions/init())
- [init(locale: Locale)](/documentation/tabulardata/formattingoptions/init(locale:))
- [init(maximumLineWidth: Int, maximumCellWidth: Int, maximumRowCount: Int, includesColumnTypes: Bool)](/documentation/tabulardata/formattingoptions/init(maximumlinewidth:maximumcellwidth:maximumrowcount:includescolumntypes:))

### Getting the Properties

- [var dateFormatStyle: Date.FormatStyle](/documentation/tabulardata/formattingoptions/dateformatstyle)
- [var floatingPointFormatStyle: FloatingPointFormatStyle<Double>](/documentation/tabulardata/formattingoptions/floatingpointformatstyle)
- [var includesColumnTypes: Bool](/documentation/tabulardata/formattingoptions/includescolumntypes)
- [var integerFormatStyle: IntegerFormatStyle<Int>](/documentation/tabulardata/formattingoptions/integerformatstyle)
- [var locale: Locale](/documentation/tabulardata/formattingoptions/locale)
- [var maximumCellWidth: Int](/documentation/tabulardata/formattingoptions/maximumcellwidth)
- [var maximumLineWidth: Int](/documentation/tabulardata/formattingoptions/maximumlinewidth)
- [var maximumRowCount: Int](/documentation/tabulardata/formattingoptions/maximumrowcount)

### Instance Properties

- [var includesRowAndColumnCounts: Bool](/documentation/tabulardata/formattingoptions/includesrowandcolumncounts)
- [var includesRowIndices: Bool](/documentation/tabulardata/formattingoptions/includesrowindices)

## Structures

- [JSONWritingOptions](/documentation/tabulardata/jsonwritingoptions)

### Initializers

- [init()](/documentation/tabulardata/jsonwritingoptions/init())

### Instance Properties

- [var dateFormatter: (Date) -> String](/documentation/tabulardata/jsonwritingoptions/dateformatter)
- [var prettyPrint: Bool](/documentation/tabulardata/jsonwritingoptions/prettyprint)
- [var sortKeys: Bool](/documentation/tabulardata/jsonwritingoptions/sortkeys)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
