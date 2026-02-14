# OSLog Documentation

Source: https://sosumi.ai/documentation/oslog

---
title: OSLog
source: https://developer.apple.com/documentation/oslog
timestamp: 2026-02-13T19:00:18.231Z
---

## Read Log Entries

- [OSLogStore](/documentation/oslog/oslogstore)

### Creating Log Stores

- [convenience init(url: URL) throws](/documentation/oslog/oslogstore/init(url:))
- [class func local() throws -> Self](/documentation/oslog/oslogstore/local())

### Accessing Position

- [func position(date: Date) -> OSLogPosition](/documentation/oslog/oslogstore/position(date:))
- [func position(timeIntervalSinceEnd: TimeInterval) -> OSLogPosition](/documentation/oslog/oslogstore/position(timeintervalsinceend:))
- [func position(timeIntervalSinceLatestBoot: TimeInterval) -> OSLogPosition](/documentation/oslog/oslogstore/position(timeintervalsincelatestboot:))

### Accessing Entries

- [func getEntries(with: OSLogEnumerator.Options, at: OSLogPosition?, matching: NSPredicate?) throws -> AnySequence<OSLogEntry>](/documentation/oslog/oslogstore/getentries(with:at:matching:))

### Initializers

- [init()](/documentation/oslog/oslogstore/init())
- [convenience init(scope: OSLogStore.Scope) throws](/documentation/oslog/oslogstore/init(scope:))

### Enumerations

- [OSLogStore.Scope](/documentation/oslog/oslogstore/scope)

#### Enumeration Cases

- [case currentProcessIdentifier](/documentation/oslog/oslogstore/scope/currentprocessidentifier)
- [case system](/documentation/oslog/oslogstore/scope/system)

#### Initializers

- [init?(rawValue: Int)](/documentation/oslog/oslogstore/scope/init(rawvalue:))
- [OSLogEnumerator](/documentation/oslog/oslogenumerator)

### Enumerator Options

- [OSLogEnumerator.Options](/documentation/oslog/oslogenumerator/options)

#### Changing Directions

- [static var reverse: OSLogEnumerator.Options](/documentation/oslog/oslogenumerator/options/reverse)

#### Initializers

- [init(rawValue: UInt)](/documentation/oslog/oslogenumerator/options/init(rawvalue:))

## Log Entries

- [OSLogEntry](/documentation/oslog/oslogentry)

### Accessing Log Entry Data

- [var composedMessage: String](/documentation/oslog/oslogentry/composedmessage)
- [var date: Date](/documentation/oslog/oslogentry/date)

### Accessing Store Categories

- [var storeCategory: OSLogEntry.StoreCategory](/documentation/oslog/oslogentry/storecategory-swift.property)
- [OSLogEntry.StoreCategory](/documentation/oslog/oslogentry/storecategory-swift.enum)

#### Constants

- [case undefined](/documentation/oslog/oslogentry/storecategory-swift.enum/undefined)
- [case metadata](/documentation/oslog/oslogentry/storecategory-swift.enum/metadata)
- [case shortTerm](/documentation/oslog/oslogentry/storecategory-swift.enum/shortterm)
- [case longTermAuto](/documentation/oslog/oslogentry/storecategory-swift.enum/longtermauto)
- [case longTerm1](/documentation/oslog/oslogentry/storecategory-swift.enum/longterm1)
- [case longTerm3](/documentation/oslog/oslogentry/storecategory-swift.enum/longterm3)
- [case longTerm7](/documentation/oslog/oslogentry/storecategory-swift.enum/longterm7)
- [case longTerm14](/documentation/oslog/oslogentry/storecategory-swift.enum/longterm14)
- [case longTerm30](/documentation/oslog/oslogentry/storecategory-swift.enum/longterm30)

#### Initializers

- [init?(rawValue: Int)](/documentation/oslog/oslogentry/storecategory-swift.enum/init(rawvalue:))
- [OSLogEntryActivity](/documentation/oslog/oslogentryactivity)

### Identifying the Parent

- [var parentActivityIdentifier: os_activity_id_t](/documentation/oslog/oslogentryactivity/parentactivityidentifier)
- [OSLogEntryBoundary](/documentation/oslog/oslogentryboundary)
- [OSLogEntryLog](/documentation/oslog/oslogentrylog)

### Accessing Log Levels

- [var level: OSLogEntryLog.Level](/documentation/oslog/oslogentrylog/level-swift.property)
- [OSLogEntryLog.Level](/documentation/oslog/oslogentrylog/level-swift.enum)

#### Log Levels

- [case undefined](/documentation/oslog/oslogentrylog/level-swift.enum/undefined)
- [case debug](/documentation/oslog/oslogentrylog/level-swift.enum/debug)
- [case info](/documentation/oslog/oslogentrylog/level-swift.enum/info)
- [case notice](/documentation/oslog/oslogentrylog/level-swift.enum/notice)
- [case error](/documentation/oslog/oslogentrylog/level-swift.enum/error)
- [case fault](/documentation/oslog/oslogentrylog/level-swift.enum/fault)

#### Initializers

- [init?(rawValue: Int)](/documentation/oslog/oslogentrylog/level-swift.enum/init(rawvalue:))
- [OSLogEntrySignpost](/documentation/oslog/oslogentrysignpost)

### Accessing Signpost Details

- [var signpostIdentifier: os_signpost_id_t](/documentation/oslog/oslogentrysignpost/signpostidentifier)
- [var signpostName: String](/documentation/oslog/oslogentrysignpost/signpostname)

### Accessing Signpost Types

- [var signpostType: OSLogEntrySignpost.SignpostType](/documentation/oslog/oslogentrysignpost/signposttype-swift.property)
- [OSLogEntrySignpost.SignpostType](/documentation/oslog/oslogentrysignpost/signposttype-swift.enum)

#### Enumeration Cases

- [case undefined](/documentation/oslog/oslogentrysignpost/signposttype-swift.enum/undefined)
- [case intervalBegin](/documentation/oslog/oslogentrysignpost/signposttype-swift.enum/intervalbegin)
- [case intervalEnd](/documentation/oslog/oslogentrysignpost/signposttype-swift.enum/intervalend)
- [case event](/documentation/oslog/oslogentrysignpost/signposttype-swift.enum/event)

#### Initializers

- [init?(rawValue: Int)](/documentation/oslog/oslogentrysignpost/signposttype-swift.enum/init(rawvalue:))
- [OSLogEntryFromProcess](/documentation/oslog/oslogentryfromprocess)

### Identifying the Process Source

- [var activityIdentifier: os_activity_id_t](/documentation/oslog/oslogentryfromprocess/activityidentifier)
- [var process: String](/documentation/oslog/oslogentryfromprocess/process)
- [var processIdentifier: pid_t](/documentation/oslog/oslogentryfromprocess/processidentifier)
- [var sender: String](/documentation/oslog/oslogentryfromprocess/sender)
- [var threadIdentifier: UInt64](/documentation/oslog/oslogentryfromprocess/threadidentifier)
- [OSLogEntryWithPayload](/documentation/oslog/oslogentrywithpayload)

### Elements of a Payload

- [var category: String](/documentation/oslog/oslogentrywithpayload/category)
- [var components: [OSLogMessageComponent]](/documentation/oslog/oslogentrywithpayload/components)
- [var formatString: String](/documentation/oslog/oslogentrywithpayload/formatstring)
- [var subsystem: String](/documentation/oslog/oslogentrywithpayload/subsystem)

## Entry Data

- [OSLogMessageComponent](/documentation/oslog/oslogmessagecomponent)

### Reading the Argument

- [var argument: OSLogMessageComponent.Argument](/documentation/oslog/oslogmessagecomponent/argument-swift.property)
- [OSLogMessageComponent.Argument](/documentation/oslog/oslogmessagecomponent/argument-swift.enum)

#### Constants

- [case data(Data)](/documentation/oslog/oslogmessagecomponent/argument-swift.enum/data(_:))
- [case double(Double)](/documentation/oslog/oslogmessagecomponent/argument-swift.enum/double(_:))
- [case signed(Int64)](/documentation/oslog/oslogmessagecomponent/argument-swift.enum/signed(_:))
- [case string(String)](/documentation/oslog/oslogmessagecomponent/argument-swift.enum/string(_:))
- [case undefined](/documentation/oslog/oslogmessagecomponent/argument-swift.enum/undefined)
- [case unsigned(UInt64)](/documentation/oslog/oslogmessagecomponent/argument-swift.enum/unsigned(_:))
- [var argumentCategory: OSLogMessageComponent.ArgumentCategory](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.property)
- [OSLogMessageComponent.ArgumentCategory](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum)

#### Constants

- [case data](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum/data)
- [case double](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum/double)
- [case int64](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum/int64)
- [case string](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum/string)
- [case uInt64](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum/uint64)
- [case undefined](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum/undefined)

#### Initializers

- [init?(rawValue: Int)](/documentation/oslog/oslogmessagecomponent/argumentcategory-swift.enum/init(rawvalue:))

### Reading the Message Component

- [var formatSubstring: String](/documentation/oslog/oslogmessagecomponent/formatsubstring)
- [var placeholder: String](/documentation/oslog/oslogmessagecomponent/placeholder)

### Accessing the Argument

- [var argumentDataValue: Data?](/documentation/oslog/oslogmessagecomponent/argumentdatavalue)
- [var argumentDoubleValue: Double](/documentation/oslog/oslogmessagecomponent/argumentdoublevalue)
- [var argumentInt64Value: Int64](/documentation/oslog/oslogmessagecomponent/argumentint64value)
- [var argumentNumberValue: NSNumber?](/documentation/oslog/oslogmessagecomponent/argumentnumbervalue)
- [var argumentStringValue: String?](/documentation/oslog/oslogmessagecomponent/argumentstringvalue)
- [var argumentUInt64Value: UInt64](/documentation/oslog/oslogmessagecomponent/argumentuint64value)
- [OSLogPosition](/documentation/oslog/oslogposition)

## Reference

- [OSLog Enumerations](/documentation/oslog/oslog-enumerations)

### Enumerations

- [OSLogStore.Scope](/documentation/oslog/oslogstore/scope)

#### Enumeration Cases

- [case currentProcessIdentifier](/documentation/oslog/oslogstore/scope/currentprocessidentifier)
- [case system](/documentation/oslog/oslogstore/scope/system)

#### Initializers

- [init?(rawValue: Int)](/documentation/oslog/oslogstore/scope/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
