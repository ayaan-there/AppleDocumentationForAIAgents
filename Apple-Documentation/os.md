# os Documentation

Source: https://sosumi.ai/documentation/os

---
title: os
source: https://developer.apple.com/documentation/os
timestamp: 2026-02-13T19:00:16.227Z
---

## Essentials

- [Reading UNIX Manual Pages](/documentation/os/reading-unix-manual-pages)

## Logs

- [Logging](/documentation/os/logging)

### Essentials

- [Generating Log Messages from Your Code](/documentation/os/generating-log-messages-from-your-code)
- [Viewing Log Messages](/documentation/os/viewing-log-messages)
- [Customizing Logging Behavior While Debugging](/documentation/os/customizing-logging-behavior-while-debugging)

### Log Messages

- [Logger](/documentation/os/logger)

#### Creating a Logger

- [init()](/documentation/os/logger/init())
- [init(subsystem: String, category: String)](/documentation/os/logger/init(subsystem:category:))
- [init(OSLog)](/documentation/os/logger/init(_:))
- [OSLog](/documentation/os/oslog)

##### Creating a Log

- [convenience init(subsystem: String, category: String)](/documentation/os/oslog/init(subsystem:category:)-17gyy)
- [convenience init(subsystem: String, category: OSLog.Category)](/documentation/os/oslog/init(subsystem:category:)-72ghw)
- [OSLog.Category](/documentation/os/oslog/category)

###### Logging Signposts

- [static let pointsOfInterest: OSLog.Category](/documentation/os/oslog/category/pointsofinterest)
- [static let dynamicStackTracing: OSLog.Category](/documentation/os/oslog/category/dynamicstacktracing)
- [static let dynamicTracing: OSLog.Category](/documentation/os/oslog/category/dynamictracing)

###### Inspecting Log Categories

- [let rawValue: String](/documentation/os/oslog/category/rawvalue)

##### Getting the Shared Logs

- [static let `default`: OSLog](/documentation/os/oslog/default)
- [static let disabled: OSLog](/documentation/os/oslog/disabled)

##### Getting Log Configuration

- [func isEnabled(type: OSLogType) -> Bool](/documentation/os/oslog/isenabled(type:))
- [var signpostsEnabled: Bool](/documentation/os/oslog/signpostsenabled)

#### Logging a Message

- [func log(OSLogMessage)](/documentation/os/logger/log(_:))
- [func log(level: OSLogType, OSLogMessage)](/documentation/os/logger/log(level:_:))
- [OSLogType](/documentation/os/oslogtype)

##### Getting Log Types

- [static let debug: OSLogType](/documentation/os/oslogtype/debug)
- [static let info: OSLogType](/documentation/os/oslogtype/info)
- [static let `default`: OSLogType](/documentation/os/oslogtype/default)
- [static let error: OSLogType](/documentation/os/oslogtype/error)
- [static let fault: OSLogType](/documentation/os/oslogtype/fault)

##### Creating a Log Type

- [init(UInt8)](/documentation/os/oslogtype/init(_:))
- [init(rawValue: UInt8)](/documentation/os/oslogtype/init(rawvalue:))

##### Getting the Raw Value

- [var rawValue: UInt8](/documentation/os/oslogtype/rawvalue)
- [OSLogMessage](/documentation/os/oslogmessage)

##### Getting the Message Details

- [var bufferSize: Int](/documentation/os/oslogmessage/buffersize)
- [let interpolation: OSLogInterpolation](/documentation/os/oslogmessage/interpolation)
- [var maxOSLogArgumentCount: UInt8](/documentation/os/maxoslogargumentcount)

#### Logging a Scoped Message

- [func notice(OSLogMessage)](/documentation/os/logger/notice(_:))
- [func debug(OSLogMessage)](/documentation/os/logger/debug(_:))
- [func trace(OSLogMessage)](/documentation/os/logger/trace(_:))
- [func info(OSLogMessage)](/documentation/os/logger/info(_:))
- [func error(OSLogMessage)](/documentation/os/logger/error(_:))
- [func warning(OSLogMessage)](/documentation/os/logger/warning(_:))
- [func fault(OSLogMessage)](/documentation/os/logger/fault(_:))
- [func critical(OSLogMessage)](/documentation/os/logger/critical(_:))
- [Message Argument Formatters](/documentation/os/message-argument-formatters)

#### Privacy Options

- [OSLogPrivacy](/documentation/os/oslogprivacy)

##### Getting the Privacy Options

- [static var auto: OSLogPrivacy](/documentation/os/oslogprivacy/auto)
- [static var `private`: OSLogPrivacy](/documentation/os/oslogprivacy/private)
- [static var `public`: OSLogPrivacy](/documentation/os/oslogprivacy/public)
- [static var sensitive: OSLogPrivacy](/documentation/os/oslogprivacy/sensitive)

##### Creating a Custom Privacy Mask

- [static func auto(mask: OSLogPrivacy.Mask) -> OSLogPrivacy](/documentation/os/oslogprivacy/auto(mask:))
- [static func `private`(mask: OSLogPrivacy.Mask) -> OSLogPrivacy](/documentation/os/oslogprivacy/private(mask:))
- [static func sensitive(mask: OSLogPrivacy.Mask) -> OSLogPrivacy](/documentation/os/oslogprivacy/sensitive(mask:))
- [OSLogPrivacy.Mask](/documentation/os/oslogprivacy/mask)

###### Privacy Mask Options

- [case hash](/documentation/os/oslogprivacy/mask/hash)
- [case none](/documentation/os/oslogprivacy/mask/none)

#### Value Formatters

- [OSLogBoolFormat](/documentation/os/oslogboolformat)

##### Getting the Boolean Format Options

- [case truth](/documentation/os/oslogboolformat/truth)
- [case answer](/documentation/os/oslogboolformat/answer)
- [OSLogIntegerFormatting](/documentation/os/oslogintegerformatting)

##### Getting the Standard Formats

- [static var decimal: OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/decimal)
- [static var hex: OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/hex)
- [static var octal: OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/octal)

##### Creating a Custom Integer Format

- [static func decimal(explicitPositiveSign: Bool) -> OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/decimal(explicitpositivesign:))
- [static func decimal(explicitPositiveSign: Bool, minDigits: @autoclosure () -> Int) -> OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/decimal(explicitpositivesign:mindigits:))
- [static func hex(explicitPositiveSign: Bool, includePrefix: Bool, uppercase: Bool) -> OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/hex(explicitpositivesign:includeprefix:uppercase:))
- [static func hex(explicitPositiveSign: Bool, includePrefix: Bool, uppercase: Bool, minDigits: @autoclosure () -> Int) -> OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/hex(explicitpositivesign:includeprefix:uppercase:mindigits:))
- [static func octal(explicitPositiveSign: Bool, includePrefix: Bool, uppercase: Bool) -> OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/octal(explicitpositivesign:includeprefix:uppercase:))
- [static func octal(explicitPositiveSign: Bool, includePrefix: Bool, uppercase: Bool, minDigits: @autoclosure () -> Int) -> OSLogIntegerFormatting](/documentation/os/oslogintegerformatting/octal(explicitpositivesign:includeprefix:uppercase:mindigits:))
- [OSLogInt32ExtendedFormat](/documentation/os/oslogint32extendedformat)

##### Getting the Formats

- [case ipv4Address](/documentation/os/oslogint32extendedformat/ipv4address)
- [case secondsSince1970](/documentation/os/oslogint32extendedformat/secondssince1970)
- [case darwinErrno](/documentation/os/oslogint32extendedformat/darwinerrno)
- [case darwinMode](/documentation/os/oslogint32extendedformat/darwinmode)
- [case darwinSignal](/documentation/os/oslogint32extendedformat/darwinsignal)
- [case bitrate](/documentation/os/oslogint32extendedformat/bitrate)
- [case bitrateIEC](/documentation/os/oslogint32extendedformat/bitrateiec)
- [case byteCount](/documentation/os/oslogint32extendedformat/bytecount)
- [case byteCountIEC](/documentation/os/oslogint32extendedformat/bytecountiec)
- [case truth](/documentation/os/oslogint32extendedformat/truth)
- [case answer](/documentation/os/oslogint32extendedformat/answer)

##### Enumeration Cases

- [case machErrno](/documentation/os/oslogint32extendedformat/macherrno)
- [OSLogFloatFormatting](/documentation/os/oslogfloatformatting)

##### Getting the Standard Formats

- [static var fixed: OSLogFloatFormatting](/documentation/os/oslogfloatformatting/fixed)
- [static var hex: OSLogFloatFormatting](/documentation/os/oslogfloatformatting/hex)
- [static var exponential: OSLogFloatFormatting](/documentation/os/oslogfloatformatting/exponential)
- [static var hybrid: OSLogFloatFormatting](/documentation/os/oslogfloatformatting/hybrid)

##### Creating a Custom Formatting Object

- [static func exponential(explicitPositiveSign: Bool, uppercase: Bool) -> OSLogFloatFormatting](/documentation/os/oslogfloatformatting/exponential(explicitpositivesign:uppercase:))
- [static func exponential(precision: @autoclosure () -> Int, explicitPositiveSign: Bool, uppercase: Bool) -> OSLogFloatFormatting](/documentation/os/oslogfloatformatting/exponential(precision:explicitpositivesign:uppercase:))
- [static func fixed(explicitPositiveSign: Bool, uppercase: Bool) -> OSLogFloatFormatting](/documentation/os/oslogfloatformatting/fixed(explicitpositivesign:uppercase:))
- [static func fixed(precision: @autoclosure () -> Int, explicitPositiveSign: Bool, uppercase: Bool) -> OSLogFloatFormatting](/documentation/os/oslogfloatformatting/fixed(precision:explicitpositivesign:uppercase:))
- [static func hex(explicitPositiveSign: Bool, uppercase: Bool) -> OSLogFloatFormatting](/documentation/os/oslogfloatformatting/hex(explicitpositivesign:uppercase:))
- [static func hybrid(explicitPositiveSign: Bool, uppercase: Bool) -> OSLogFloatFormatting](/documentation/os/oslogfloatformatting/hybrid(explicitpositivesign:uppercase:))
- [static func hybrid(precision: @autoclosure () -> Int, explicitPositiveSign: Bool, uppercase: Bool) -> OSLogFloatFormatting](/documentation/os/oslogfloatformatting/hybrid(precision:explicitpositivesign:uppercase:))
- [OSLogPointerFormat](/documentation/os/oslogpointerformat)

##### Getting the Format Options

- [case none](/documentation/os/oslogpointerformat/none)
- [case ipv6Address](/documentation/os/oslogpointerformat/ipv6address)
- [case sockaddr](/documentation/os/oslogpointerformat/sockaddr)
- [case timespec](/documentation/os/oslogpointerformat/timespec)
- [case timeval](/documentation/os/oslogpointerformat/timeval)
- [case uuid](/documentation/os/oslogpointerformat/uuid)

#### Value Interpolation

- [OSLogInterpolation](/documentation/os/osloginterpolation)

##### Appending Strings

- [func appendInterpolation(@autoclosure () -> String, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:align:privacy:)-6tazr)
- [func appendInterpolation(@autoclosure () -> String, align: OSLogStringAlignment, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:align:privacy:attributes:)-7g68v)

##### Appending Signed Integers

- [func appendInterpolation(@autoclosure () -> Int, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-8kli1)
- [func appendInterpolation(@autoclosure () -> Int8, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-5ihzf)
- [func appendInterpolation(@autoclosure () -> Int16, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-190d0)
- [func appendInterpolation(@autoclosure () -> Int32, format: OSLogInt32ExtendedFormat, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:privacy:)-3ji02)
- [func appendInterpolation(@autoclosure () -> Int32, format: OSLogInt32ExtendedFormat, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:format:privacy:attributes:)-4i2ir)
- [func appendInterpolation(@autoclosure () -> Int32, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-2sb1i)
- [func appendInterpolation(@autoclosure () -> Int64, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-802m9)

##### Appending Unsigned Integers

- [func appendInterpolation(@autoclosure () -> UInt, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-20jin)
- [func appendInterpolation(@autoclosure () -> UInt8, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-4qvu9)
- [func appendInterpolation(@autoclosure () -> UInt16, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-7k91g)
- [func appendInterpolation(@autoclosure () -> UInt32, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-2i3qh)
- [func appendInterpolation(@autoclosure () -> UInt64, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-81jbm)

##### Appending Doubles

- [func appendInterpolation(@autoclosure () -> Double, format: OSLogFloatFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-6mu00)
- [func appendInterpolation(@autoclosure () -> Double, format: OSLogFloatFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:attributes:)-8bi90)

##### Appending Floats

- [func appendInterpolation(@autoclosure () -> Float, format: OSLogFloatFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:)-7z1jd)
- [func appendInterpolation(@autoclosure () -> Float, format: OSLogFloatFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:attributes:)-78sek)

##### Appending Boolean Values

- [func appendInterpolation(@autoclosure () -> Bool, format: OSLogBoolFormat, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:privacy:)-686xc)

##### Appending Generic Types

- [func appendInterpolation<T>(@autoclosure () -> T, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:align:privacy:)-84m60)
- [func appendInterpolation<T>(@autoclosure () -> T, align: OSLogStringAlignment, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:align:privacy:attributes:)-xyum)
- [func appendInterpolation<T>(@autoclosure () -> T, format: OSLogIntegerFormatting, align: OSLogStringAlignment, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:format:align:privacy:attributes:)-8107a)
- [func appendInterpolation(@autoclosure () -> any Any.Type, align: OSLogStringAlignment, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:align:privacy:)-8hwmt)
- [func appendInterpolation(@autoclosure () -> any Any.Type, align: OSLogStringAlignment, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:align:privacy:attributes:)-9hehv)

##### Appending Pointer Data

- [func appendInterpolation(@autoclosure () -> UnsafeRawPointer, bytes: @autoclosure () -> Int, format: OSLogPointerFormat, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:bytes:format:privacy:))
- [func appendInterpolation(@autoclosure () -> UnsafeRawPointer, bytes: @autoclosure () -> Int, format: OSLogPointerFormat, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:bytes:format:privacy:attributes:))
- [func appendInterpolation(@autoclosure () -> UnsafeRawBufferPointer, format: OSLogPointerFormat, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:format:privacy:)-5qaau)
- [func appendInterpolation(@autoclosure () -> UnsafeRawBufferPointer, format: OSLogPointerFormat, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:format:privacy:attributes:)-93lbs)

##### Appending Objects

- [func appendInterpolation(@autoclosure () -> NSObject, privacy: OSLogPrivacy)](/documentation/os/osloginterpolation/appendinterpolation(_:privacy:))
- [func appendInterpolation(@autoclosure () -> NSObject, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:privacy:attributes:)-3czd2)

##### Instance Methods

- [func appendInterpolation(@autoclosure () -> Int, format: OSLogIntExtendedFormat, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:format:privacy:attributes:)-6le5w)
- [func appendInterpolation(@autoclosure () -> any Error, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:privacy:attributes:)-4o74h)
- [func appendInterpolation(@autoclosure () -> (any Error)?, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:privacy:attributes:)-6vtcc)
- [func appendInterpolation(@autoclosure () -> NSObject?, privacy: OSLogPrivacy, attributes: String)](/documentation/os/osloginterpolation/appendinterpolation(_:privacy:attributes:)-9eafm)
- [OSLogIntExtendedFormat](/documentation/os/oslogintextendedformat)

##### Expansion Options

- [case bitrate](/documentation/os/oslogintextendedformat/bitrate)
- [case bitrateIEC](/documentation/os/oslogintextendedformat/bitrateiec)
- [case byteCount](/documentation/os/oslogintextendedformat/bytecount)
- [case byteCountIEC](/documentation/os/oslogintextendedformat/bytecountiec)

##### Enumeration Cases

- [case secondsSince1970](/documentation/os/oslogintextendedformat/secondssince1970)

#### String Alignment

- [OSLogStringAlignment](/documentation/os/oslogstringalignment)

##### Getting the Standard Alignment

- [static var none: OSLogStringAlignment](/documentation/os/oslogstringalignment/none)

##### Getting a Custom String Alignment

- [static func left(columns: @autoclosure () -> Int) -> OSLogStringAlignment](/documentation/os/oslogstringalignment/left(columns:))
- [static func right(columns: @autoclosure () -> Int) -> OSLogStringAlignment](/documentation/os/oslogstringalignment/right(columns:))
- [OSLogType](/documentation/os/oslogtype)

#### Getting Log Types

- [static let debug: OSLogType](/documentation/os/oslogtype/debug)
- [static let info: OSLogType](/documentation/os/oslogtype/info)
- [static let `default`: OSLogType](/documentation/os/oslogtype/default)
- [static let error: OSLogType](/documentation/os/oslogtype/error)
- [static let fault: OSLogType](/documentation/os/oslogtype/fault)

#### Creating a Log Type

- [init(UInt8)](/documentation/os/oslogtype/init(_:))
- [init(rawValue: UInt8)](/documentation/os/oslogtype/init(rawvalue:))

#### Getting the Raw Value

- [var rawValue: UInt8](/documentation/os/oslogtype/rawvalue)

### Measure Events

- [Recording Performance Data](/documentation/os/recording-performance-data)
- [OSSignposter](/documentation/os/ossignposter)

#### Creating a Signposter

- [init()](/documentation/os/ossignposter/init())
- [init(subsystem: String, category: String)](/documentation/os/ossignposter/init(subsystem:category:)-94xpb)
- [init(subsystem: String, category: OSLog.Category)](/documentation/os/ossignposter/init(subsystem:category:)-4vdri)
- [init(logger: Logger)](/documentation/os/ossignposter/init(logger:))
- [init(logHandle: OSLog)](/documentation/os/ossignposter/init(loghandle:))
- [static var disabled: OSSignposter](/documentation/os/ossignposter/disabled)

#### Getting State

- [var isEnabled: Bool](/documentation/os/ossignposter/isenabled)

#### Generating Signpost IDs

- [func makeSignpostID() -> OSSignpostID](/documentation/os/ossignposter/makesignpostid())
- [func makeSignpostID(from: AnyObject) -> OSSignpostID](/documentation/os/ossignposter/makesignpostid(from:))
- [OSSignpostID](/documentation/os/ossignpostid)

##### Getting Signpost Identifiers

- [static let exclusive: OSSignpostID](/documentation/os/ossignpostid/exclusive)
- [static let invalid: OSSignpostID](/documentation/os/ossignpostid/invalid)
- [static let null: OSSignpostID](/documentation/os/ossignpostid/null)

##### Creating a Signpost Identifier

- [init(UInt64)](/documentation/os/ossignpostid/init(_:))
- [init(log: OSLog)](/documentation/os/ossignpostid/init(log:))
- [init(log: OSLog, object: AnyObject)](/documentation/os/ossignpostid/init(log:object:))

##### Getting an Identifier’s Raw Value

- [let rawValue: os_signpost_id_t](/documentation/os/ossignpostid/rawvalue)

#### Starting a Signposted Interval

- [func beginInterval(StaticString, id: OSSignpostID) -> OSSignpostIntervalState](/documentation/os/ossignposter/begininterval(_:id:))
- [func beginInterval(StaticString, id: OSSignpostID, SignpostMetadata) -> OSSignpostIntervalState](/documentation/os/ossignposter/begininterval(_:id:_:))
- [func beginAnimationInterval(StaticString, id: OSSignpostID) -> OSSignpostIntervalState](/documentation/os/ossignposter/beginanimationinterval(_:id:))
- [func beginAnimationInterval(StaticString, id: OSSignpostID, SignpostMetadata) -> OSSignpostIntervalState](/documentation/os/ossignposter/beginanimationinterval(_:id:_:))
- [OSSignpostIntervalState](/documentation/os/ossignpostintervalstate)

##### Creating Interval State

- [init(from: any Decoder) throws](/documentation/os/ossignpostintervalstate/init(from:))

##### Recreating Interval State

- [static func beginState(id: OSSignpostID) -> OSSignpostIntervalState](/documentation/os/ossignpostintervalstate/beginstate(id:))

##### Encoding Interval State

- [func encode(to: any Encoder) throws](/documentation/os/ossignpostintervalstate/encode(to:))
- [SignpostMetadata](/documentation/os/signpostmetadata)

#### Stopping a Signposted Interval

- [func endInterval(StaticString, OSSignpostIntervalState)](/documentation/os/ossignposter/endinterval(_:_:))
- [func endInterval(StaticString, OSSignpostIntervalState, SignpostMetadata)](/documentation/os/ossignposter/endinterval(_:_:_:))

#### Measuring a Closure

- [func withIntervalSignpost<T>(StaticString, id: OSSignpostID, around: () throws -> T) rethrows -> T](/documentation/os/ossignposter/withintervalsignpost(_:id:around:))
- [func withIntervalSignpost<T>(StaticString, id: OSSignpostID, SignpostMetadata, around: () throws -> T) rethrows -> T](/documentation/os/ossignposter/withintervalsignpost(_:id:_:around:))

#### Emitting Individual Signposts

- [func emitEvent(StaticString, id: OSSignpostID)](/documentation/os/ossignposter/emitevent(_:id:))
- [func emitEvent(StaticString, id: OSSignpostID, SignpostMetadata)](/documentation/os/ossignposter/emitevent(_:id:_:))
- [Legacy Signpost Symbols](/documentation/os/legacy-signpost-symbols)

#### Measure Events

- [func os_signpost(OSSignpostType, dso: UnsafeRawPointer, log: OSLog, name: StaticString, signpostID: OSSignpostID)](/documentation/os/os_signpost(_:dso:log:name:signpostid:)-2oz8u)
- [func os_signpost(OSSignpostType, dso: UnsafeRawPointer, log: OSLog, name: StaticString, signpostID: OSSignpostID, StaticString, any CVarArg...)](/documentation/os/os_signpost(_:dso:log:name:signpostid:_:_:)-2om9b)
- [OSSignpostType](/documentation/os/ossignposttype)

##### Specifying Signpost Types

- [static let begin: OSSignpostType](/documentation/os/ossignposttype/begin)
- [static let end: OSSignpostType](/documentation/os/ossignposttype/end)
- [static let event: OSSignpostType](/documentation/os/ossignposttype/event)

##### Creating Signpost Types

- [init(rawValue: UInt8)](/documentation/os/ossignposttype/init(rawvalue:))
- [init(UInt8)](/documentation/os/ossignposttype/init(_:))

##### Inspecting Signpost Types

- [var rawValue: UInt8](/documentation/os/ossignposttype/rawvalue)
- [func os_signpost(OSSignpostAnimationBegin, dso: UnsafeRawPointer, log: OSLog, name: StaticString, signpostID: OSSignpostID)](/documentation/os/os_signpost(_:dso:log:name:signpostid:)-12m3v)
- [func os_signpost(OSSignpostAnimationBegin, dso: UnsafeRawPointer, log: OSLog, name: StaticString, signpostID: OSSignpostID, AnimationFormatString.OSLogMessage, any CVarArg...)](/documentation/os/os_signpost(_:dso:log:name:signpostid:_:_:)-nez5)
- [OSSignpostAnimationBegin](/documentation/os/ossignpostanimationbegin)

##### Getting the Animation Options

- [case animationBegin](/documentation/os/ossignpostanimationbegin/animationbegin)
- [AnimationFormatString](/documentation/os/animationformatstring)

##### Getting an Animation-Related Log Message

- [AnimationFormatString.OSLogMessage](/documentation/os/animationformatstring/oslogmessage)

###### Creating a Format String

- [init(stringLiteral: String)](/documentation/os/animationformatstring/oslogmessage/init(stringliteral:))
- [os_signpost_id_t](/documentation/os/os_signpost_id_t)
- [OSSignpostType](/documentation/os/ossignposttype)

#### Specifying Signpost Types

- [static let begin: OSSignpostType](/documentation/os/ossignposttype/begin)
- [static let end: OSSignpostType](/documentation/os/ossignposttype/end)
- [static let event: OSSignpostType](/documentation/os/ossignposttype/event)

#### Creating Signpost Types

- [init(rawValue: UInt8)](/documentation/os/ossignposttype/init(rawvalue:))
- [init(UInt8)](/documentation/os/ossignposttype/init(_:))

#### Inspecting Signpost Types

- [var rawValue: UInt8](/documentation/os/ossignposttype/rawvalue)
- [os_signpost_id_t](/documentation/os/os_signpost_id_t)

## Task Management

- [Synchronization](/documentation/os/synchronization)

### Swift Wrappers

- [OSAllocatedUnfairLock](/documentation/os/osallocatedunfairlock)

#### Creating a lock object

- [init()](/documentation/os/osallocatedunfairlock/init())
- [init(initialState: State)](/documentation/os/osallocatedunfairlock/init(initialstate:))

#### Using locks

- [func lock()](/documentation/os/osallocatedunfairlock/lock())
- [func lockIfAvailable() -> Bool](/documentation/os/osallocatedunfairlock/lockifavailable())
- [func unlock()](/documentation/os/osallocatedunfairlock/unlock())

#### Determining lock ownership

- [OSAllocatedUnfairLock.Ownership](/documentation/os/osallocatedunfairlock/ownership)

##### Specifying ownership

- [case owner](/documentation/os/osallocatedunfairlock/ownership/owner)
- [case notOwner](/documentation/os/osallocatedunfairlock/ownership/notowner)
- [func precondition(OSAllocatedUnfairLock<State>.Ownership)](/documentation/os/osallocatedunfairlock/precondition(_:))

#### Initializers

- [init(uncheckedState: State)](/documentation/os/osallocatedunfairlock/init(uncheckedstate:))

#### Instance Methods

- [func lock(flags: OSAllocatedUnfairLockFlags)](/documentation/os/osallocatedunfairlock/lock(flags:))
- [func withLock<R>((inout State) throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlock(_:)-1uy7m)
- [func withLock<R>(() throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlock(_:)-hple)
- [func withLock<R>(flags: OSAllocatedUnfairLockFlags, (inout State) throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlock(flags:_:)-1ub4c)
- [func withLock<R>(flags: OSAllocatedUnfairLockFlags, () throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlock(flags:_:)-u2xj)
- [func withLockIfAvailable<R>(() throws -> R) rethrows -> R?](/documentation/os/osallocatedunfairlock/withlockifavailable(_:)-1rp3w)
- [func withLockIfAvailable<R>((inout State) throws -> R) rethrows -> R?](/documentation/os/osallocatedunfairlock/withlockifavailable(_:)-3kw0o)
- [func withLockIfAvailableUnchecked<R>((inout State) throws -> R) rethrows -> R?](/documentation/os/osallocatedunfairlock/withlockifavailableunchecked(_:)-15q0y)
- [func withLockIfAvailableUnchecked<R>(() throws -> R) rethrows -> R?](/documentation/os/osallocatedunfairlock/withlockifavailableunchecked(_:)-6gji7)
- [func withLockUnchecked<R>((inout State) throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlockunchecked(_:)-7qywq)
- [func withLockUnchecked<R>(() throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlockunchecked(_:)-9v03m)
- [func withLockUnchecked<R>(flags: OSAllocatedUnfairLockFlags, (inout State) throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlockunchecked(flags:_:)-8cv64)
- [func withLockUnchecked<R>(flags: OSAllocatedUnfairLockFlags, () throws -> R) rethrows -> R](/documentation/os/osallocatedunfairlock/withlockunchecked(flags:_:)-9iq8s)
- [OSAllocatedUnfairLockFlags](/documentation/os/osallocatedunfairlockflags)

#### Type Properties

- [static let adaptiveSpin: OSAllocatedUnfairLockFlags](/documentation/os/osallocatedunfairlockflags/adaptivespin)

## Deprecated

- [Deprecated Symbols](/documentation/os/deprecated-symbols)

### Deprecated Functions

- [func os_trace_debug_enabled() -> Bool](/documentation/os/os_trace_debug_enabled())
- [func os_trace_info_enabled() -> Bool](/documentation/os/os_trace_info_enabled())
- [func os_trace_type_enabled(UInt8) -> Bool](/documentation/os/os_trace_type_enabled(_:))

### Deprecated Macros

- [var OS_TRACE_TYPE_DEBUG: UInt32](/documentation/os/os_trace_type_debug)
- [var OS_TRACE_TYPE_INFO: UInt32](/documentation/os/os_trace_type_info)
- [var OS_TRACE_TYPE_RELEASE: UInt32](/documentation/os/os_trace_type_release)

### Deprecated Type Aliases

- [os_trace_payload_object_t](/documentation/os/os_trace_payload_object_t)

## Reference

- [os Constants](/documentation/os/os-constants)

### Constants

- [var OS_ATOMIC_USES_CXX: Int32](/documentation/os/os_atomic_uses_cxx)
- [var OS_LOG_TARGET_HAS_10_12_FEATURES: Int32](/documentation/os/os_log_target_has_10_12_features)
- [var OS_LOG_TARGET_HAS_10_13_FEATURES: Int32](/documentation/os/os_log_target_has_10_13_features)
- [var OS_LOG_TARGET_HAS_10_14_FEATURES: Int32](/documentation/os/os_log_target_has_10_14_features)
- [var OS_LOG_TARGET_HAS_10_15_FEATURES: Int32](/documentation/os/os_log_target_has_10_15_features)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
