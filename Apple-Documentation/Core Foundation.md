# Core Foundation Documentation

Source: https://sosumi.ai/documentation/corefoundation

---
title: Core Foundation
source: https://developer.apple.com/documentation/corefoundation
timestamp: 2026-02-13T18:55:16.547Z
---

## Utilities

- [Base Utilities](/documentation/corefoundation/base-utilities)

### Core Foundation Base Utilities Miscellaneous Functions

- [func CFRangeMake(CFIndex, CFIndex) -> CFRange](/documentation/corefoundation/cfrangemake(_:_:))

### Callbacks

- [CFComparatorFunction](/documentation/corefoundation/cfcomparatorfunction)

### Data Types

- [CFIndex](/documentation/corefoundation/cfindex)
- [CFOptionFlags](/documentation/corefoundation/cfoptionflags)
- [CFRange](/documentation/corefoundation/cfrange)

#### Initializers

- [init()](/documentation/corefoundation/cfrange/init())
- [init(location: CFIndex, length: CFIndex)](/documentation/corefoundation/cfrange/init(location:length:))

#### Instance Properties

- [var length: CFIndex](/documentation/corefoundation/cfrange/length)
- [var location: CFIndex](/documentation/corefoundation/cfrange/location)

### Constants

- [CFComparisonResult](/documentation/corefoundation/cfcomparisonresult)

#### Constants

- [case compareLessThan](/documentation/corefoundation/cfcomparisonresult/comparelessthan)
- [case compareEqualTo](/documentation/corefoundation/cfcomparisonresult/compareequalto)
- [case compareGreaterThan](/documentation/corefoundation/cfcomparisonresult/comparegreaterthan)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfcomparisonresult/init(rawvalue:))
- [Value Not Found](/documentation/corefoundation/value-not-found)

#### Constants

- [let kCFNotFound: CFIndex](/documentation/corefoundation/kcfnotfound)
- [Current Framework Version Number](/documentation/corefoundation/current-framework-version-number)

#### Constants

- [var kCFCoreFoundationVersionNumber: Double](/documentation/corefoundation/kcfcorefoundationversionnumber)
- [Framework Version Numbers](/documentation/corefoundation/framework-version-numbers)

#### Constants

- [var kCFCoreFoundationVersionNumber10_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_0)
- [var kCFCoreFoundationVersionNumber10_0_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_0_3)
- [var kCFCoreFoundationVersionNumber10_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_1)
- [var kCFCoreFoundationVersionNumber10_1_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_1_1)
- [var kCFCoreFoundationVersionNumber10_1_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_1_2)
- [var kCFCoreFoundationVersionNumber10_1_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_1_3)
- [var kCFCoreFoundationVersionNumber10_1_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_1_4)
- [var kCFCoreFoundationVersionNumber10_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2)
- [var kCFCoreFoundationVersionNumber10_2_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_1)
- [var kCFCoreFoundationVersionNumber10_2_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_2)
- [var kCFCoreFoundationVersionNumber10_2_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_3)
- [var kCFCoreFoundationVersionNumber10_2_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_4)
- [var kCFCoreFoundationVersionNumber10_2_5: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_5)
- [var kCFCoreFoundationVersionNumber10_2_6: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_6)
- [var kCFCoreFoundationVersionNumber10_2_7: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_7)
- [var kCFCoreFoundationVersionNumber10_2_8: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_2_8)
- [var kCFCoreFoundationVersionNumber10_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3)
- [var kCFCoreFoundationVersionNumber10_3_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_1)
- [var kCFCoreFoundationVersionNumber10_3_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_2)
- [var kCFCoreFoundationVersionNumber10_3_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_3)
- [var kCFCoreFoundationVersionNumber10_3_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_4)
- [var kCFCoreFoundationVersionNumber10_3_5: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_5)
- [var kCFCoreFoundationVersionNumber10_3_6: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_6)
- [var kCFCoreFoundationVersionNumber10_3_7: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_7)
- [var kCFCoreFoundationVersionNumber10_3_8: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_8)
- [var kCFCoreFoundationVersionNumber10_3_9: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_3_9)
- [var kCFCoreFoundationVersionNumber10_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4)
- [var kCFCoreFoundationVersionNumber10_4_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_1)
- [var kCFCoreFoundationVersionNumber10_4_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_2)
- [var kCFCoreFoundationVersionNumber10_4_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_3)
- [var kCFCoreFoundationVersionNumber10_4_4_Intel: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_4_intel)
- [var kCFCoreFoundationVersionNumber10_4_4_PowerPC: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_4_powerpc)
- [var kCFCoreFoundationVersionNumber10_4_5_Intel: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_5_intel)
- [var kCFCoreFoundationVersionNumber10_4_5_PowerPC: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_5_powerpc)
- [var kCFCoreFoundationVersionNumber10_4_6_Intel: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_6_intel)
- [var kCFCoreFoundationVersionNumber10_4_6_PowerPC: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_6_powerpc)
- [var kCFCoreFoundationVersionNumber10_4_7: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_7)
- [var kCFCoreFoundationVersionNumber10_4_8: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_8)
- [var kCFCoreFoundationVersionNumber10_4_9: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_9)
- [var kCFCoreFoundationVersionNumber10_4_10: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_10)
- [var kCFCoreFoundationVersionNumber10_4_11: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_4_11)
- [var kCFCoreFoundationVersionNumber10_5: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5)
- [var kCFCoreFoundationVersionNumber10_5_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_1)
- [var kCFCoreFoundationVersionNumber10_5_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_2)
- [var kCFCoreFoundationVersionNumber10_5_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_3)
- [var kCFCoreFoundationVersionNumber10_5_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_4)
- [var kCFCoreFoundationVersionNumber10_5_5: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_5)
- [var kCFCoreFoundationVersionNumber10_5_6: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_6)
- [var kCFCoreFoundationVersionNumber10_5_7: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_7)
- [var kCFCoreFoundationVersionNumber10_5_8: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_5_8)
- [var kCFCoreFoundationVersionNumber10_6: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6)
- [var kCFCoreFoundationVersionNumber10_6_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_1)
- [var kCFCoreFoundationVersionNumber10_6_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_2)
- [var kCFCoreFoundationVersionNumber10_6_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_3)
- [var kCFCoreFoundationVersionNumber10_6_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_4)
- [var kCFCoreFoundationVersionNumber10_6_5: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_5)
- [var kCFCoreFoundationVersionNumber10_6_6: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_6)
- [var kCFCoreFoundationVersionNumber10_6_7: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_7)
- [var kCFCoreFoundationVersionNumber10_6_8: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_6_8)
- [var kCFCoreFoundationVersionNumber10_7: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_7)
- [var kCFCoreFoundationVersionNumber10_7_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_7_1)
- [var kCFCoreFoundationVersionNumber10_7_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_7_2)
- [var kCFCoreFoundationVersionNumber10_7_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_7_3)
- [var kCFCoreFoundationVersionNumber10_7_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_7_4)
- [var kCFCoreFoundationVersionNumber_iPhoneOS_2_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_iphoneos_2_0)
- [var kCFCoreFoundationVersionNumber_iPhoneOS_2_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_iphoneos_2_1)
- [var kCFCoreFoundationVersionNumber_iPhoneOS_2_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_iphoneos_2_2)
- [var kCFCoreFoundationVersionNumber_iPhoneOS_3_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_iphoneos_3_0)
- [var kCFCoreFoundationVersionNumber_iPhoneOS_3_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_iphoneos_3_1)
- [var kCFCoreFoundationVersionNumber_iPhoneOS_3_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_iphoneos_3_2)
- [var kCFCoreFoundationVersionNumber_iOS_4_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_4_0)
- [var kCFCoreFoundationVersionNumber_iOS_4_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_4_1)
- [var kCFCoreFoundationVersionNumber_iOS_4_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_4_2)
- [var kCFCoreFoundationVersionNumber_iOS_4_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_4_3)
- [var kCFCoreFoundationVersionNumber_iOS_5_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_5_0)
- [var kCFCoreFoundationVersionNumber_iOS_5_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_5_1)
- [Byte-Order Utilities](/documentation/corefoundation/byte-order-utilities)

### Core Foundation Byte Order Utilities Miscellaneous Functions

- [func CFByteOrderGetCurrent() -> CFByteOrder](/documentation/corefoundation/cfbyteordergetcurrent())
- [func CFConvertDoubleHostToSwapped(Double) -> CFSwappedFloat64](/documentation/corefoundation/cfconvertdoublehosttoswapped(_:))
- [func CFConvertDoubleSwappedToHost(CFSwappedFloat64) -> Double](/documentation/corefoundation/cfconvertdoubleswappedtohost(_:))
- [func CFConvertFloat32HostToSwapped(Float32) -> CFSwappedFloat32](/documentation/corefoundation/cfconvertfloat32hosttoswapped(_:))
- [func CFConvertFloat32SwappedToHost(CFSwappedFloat32) -> Float32](/documentation/corefoundation/cfconvertfloat32swappedtohost(_:))
- [func CFConvertFloat64HostToSwapped(Float64) -> CFSwappedFloat64](/documentation/corefoundation/cfconvertfloat64hosttoswapped(_:))
- [func CFConvertFloat64SwappedToHost(CFSwappedFloat64) -> Float64](/documentation/corefoundation/cfconvertfloat64swappedtohost(_:))
- [func CFConvertFloatHostToSwapped(Float) -> CFSwappedFloat32](/documentation/corefoundation/cfconvertfloathosttoswapped(_:))
- [func CFConvertFloatSwappedToHost(CFSwappedFloat32) -> Float](/documentation/corefoundation/cfconvertfloatswappedtohost(_:))
- [func CFSwapInt16(UInt16) -> UInt16](/documentation/corefoundation/cfswapint16(_:))
- [func CFSwapInt16BigToHost(UInt16) -> UInt16](/documentation/corefoundation/cfswapint16bigtohost(_:))
- [func CFSwapInt16HostToBig(UInt16) -> UInt16](/documentation/corefoundation/cfswapint16hosttobig(_:))
- [func CFSwapInt16HostToLittle(UInt16) -> UInt16](/documentation/corefoundation/cfswapint16hosttolittle(_:))
- [func CFSwapInt16LittleToHost(UInt16) -> UInt16](/documentation/corefoundation/cfswapint16littletohost(_:))
- [func CFSwapInt32(UInt32) -> UInt32](/documentation/corefoundation/cfswapint32(_:))
- [func CFSwapInt32BigToHost(UInt32) -> UInt32](/documentation/corefoundation/cfswapint32bigtohost(_:))
- [func CFSwapInt32HostToBig(UInt32) -> UInt32](/documentation/corefoundation/cfswapint32hosttobig(_:))
- [func CFSwapInt32HostToLittle(UInt32) -> UInt32](/documentation/corefoundation/cfswapint32hosttolittle(_:))
- [func CFSwapInt32LittleToHost(UInt32) -> UInt32](/documentation/corefoundation/cfswapint32littletohost(_:))
- [func CFSwapInt64(UInt64) -> UInt64](/documentation/corefoundation/cfswapint64(_:))
- [func CFSwapInt64BigToHost(UInt64) -> UInt64](/documentation/corefoundation/cfswapint64bigtohost(_:))
- [func CFSwapInt64HostToBig(UInt64) -> UInt64](/documentation/corefoundation/cfswapint64hosttobig(_:))
- [func CFSwapInt64HostToLittle(UInt64) -> UInt64](/documentation/corefoundation/cfswapint64hosttolittle(_:))
- [func CFSwapInt64LittleToHost(UInt64) -> UInt64](/documentation/corefoundation/cfswapint64littletohost(_:))

### Data Types

- [CFSwappedFloat32](/documentation/corefoundation/cfswappedfloat32)

#### Initializers

- [init()](/documentation/corefoundation/cfswappedfloat32/init())
- [init(v: UInt32)](/documentation/corefoundation/cfswappedfloat32/init(v:))

#### Instance Properties

- [var v: UInt32](/documentation/corefoundation/cfswappedfloat32/v)
- [CFSwappedFloat64](/documentation/corefoundation/cfswappedfloat64)

#### Initializers

- [init()](/documentation/corefoundation/cfswappedfloat64/init())
- [init(v: UInt64)](/documentation/corefoundation/cfswappedfloat64/init(v:))

#### Instance Properties

- [var v: UInt64](/documentation/corefoundation/cfswappedfloat64/v)

### Constants

- [CFByteOrder](/documentation/corefoundation/cfbyteorder)

#### Constants

- [var CFByteOrderUnknown: __CFByteOrder](/documentation/corefoundation/cfbyteorderunknown)
- [var CFByteOrderLittleEndian: __CFByteOrder](/documentation/corefoundation/cfbyteorderlittleendian)
- [var CFByteOrderBigEndian: __CFByteOrder](/documentation/corefoundation/cfbyteorderbigendian)
- [Core Foundation URL Access Utilities](/documentation/corefoundation/core-foundation-url-access-utilities)

### Core Foundation URL Access Utilities Miscellaneous Functions

- [func CFURLCreateDataAndPropertiesFromResource(CFAllocator!, CFURL!, UnsafeMutablePointer<Unmanaged<CFData>?>!, UnsafeMutablePointer<Unmanaged<CFDictionary>?>!, CFArray!, UnsafeMutablePointer<Int32>!) -> Bool](/documentation/corefoundation/cfurlcreatedataandpropertiesfromresource(_:_:_:_:_:_:))
- [func CFURLCreatePropertyFromResource(CFAllocator!, CFURL!, CFString!, UnsafeMutablePointer<Int32>!) -> CFTypeRef!](/documentation/corefoundation/cfurlcreatepropertyfromresource(_:_:_:_:))
- [func CFURLDestroyResource(CFURL!, UnsafeMutablePointer<Int32>!) -> Bool](/documentation/corefoundation/cfurldestroyresource(_:_:))
- [func CFURLWriteDataAndPropertiesToResource(CFURL!, CFData!, CFDictionary!, UnsafeMutablePointer<Int32>!) -> Bool](/documentation/corefoundation/cfurlwritedataandpropertiestoresource(_:_:_:_:))

### Constants

- [CFURLError](/documentation/corefoundation/cfurlerror)

#### Constants

- [case unknownError](/documentation/corefoundation/cfurlerror/unknownerror)
- [case unknownSchemeError](/documentation/corefoundation/cfurlerror/unknownschemeerror)
- [case resourceNotFoundError](/documentation/corefoundation/cfurlerror/resourcenotfounderror)
- [case resourceAccessViolationError](/documentation/corefoundation/cfurlerror/resourceaccessviolationerror)
- [case remoteHostUnavailableError](/documentation/corefoundation/cfurlerror/remotehostunavailableerror)
- [case improperArgumentsError](/documentation/corefoundation/cfurlerror/improperargumentserror)
- [case unknownPropertyKeyError](/documentation/corefoundation/cfurlerror/unknownpropertykeyerror)
- [case propertyKeyUnavailableError](/documentation/corefoundation/cfurlerror/propertykeyunavailableerror)
- [case timeoutError](/documentation/corefoundation/cfurlerror/timeouterror)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfurlerror/init(rawvalue:))
- [File URL Properties](/documentation/corefoundation/file-url-properties)

#### Constants

- [let kCFURLFileExists: CFString!](/documentation/corefoundation/kcfurlfileexists)
- [let kCFURLFileDirectoryContents: CFString!](/documentation/corefoundation/kcfurlfiledirectorycontents)
- [let kCFURLFileLength: CFString!](/documentation/corefoundation/kcfurlfilelength)
- [let kCFURLFileLastModificationTime: CFString!](/documentation/corefoundation/kcfurlfilelastmodificationtime)
- [let kCFURLFilePOSIXMode: CFString!](/documentation/corefoundation/kcfurlfileposixmode)
- [let kCFURLFileOwnerID: CFString!](/documentation/corefoundation/kcfurlfileownerid)
- [HTTP URL Properties](/documentation/corefoundation/http-url-properties)

#### Constants

- [let kCFURLHTTPStatusCode: CFString!](/documentation/corefoundation/kcfurlhttpstatuscode)
- [let kCFURLHTTPStatusLine: CFString!](/documentation/corefoundation/kcfurlhttpstatusline)
- [Preferences Utilities](/documentation/corefoundation/preferences-utilities)

### Getting Preference Values

- [func CFPreferencesCopyAppValue(CFString, CFString) -> CFPropertyList?](/documentation/corefoundation/cfpreferencescopyappvalue(_:_:))
- [func CFPreferencesCopyKeyList(CFString, CFString, CFString) -> CFArray?](/documentation/corefoundation/cfpreferencescopykeylist(_:_:_:))
- [func CFPreferencesCopyMultiple(CFArray?, CFString, CFString, CFString) -> CFDictionary](/documentation/corefoundation/cfpreferencescopymultiple(_:_:_:_:))
- [func CFPreferencesCopyValue(CFString, CFString, CFString, CFString) -> CFPropertyList?](/documentation/corefoundation/cfpreferencescopyvalue(_:_:_:_:))
- [func CFPreferencesGetAppBooleanValue(CFString, CFString, UnsafeMutablePointer<DarwinBoolean>?) -> Bool](/documentation/corefoundation/cfpreferencesgetappbooleanvalue(_:_:_:))
- [func CFPreferencesGetAppIntegerValue(CFString, CFString, UnsafeMutablePointer<DarwinBoolean>?) -> CFIndex](/documentation/corefoundation/cfpreferencesgetappintegervalue(_:_:_:))

### Setting Preference Values

- [func CFPreferencesSetAppValue(CFString, CFPropertyList?, CFString)](/documentation/corefoundation/cfpreferencessetappvalue(_:_:_:))
- [func CFPreferencesSetMultiple(CFDictionary?, CFArray?, CFString, CFString, CFString)](/documentation/corefoundation/cfpreferencessetmultiple(_:_:_:_:_:))
- [func CFPreferencesSetValue(CFString, CFPropertyList?, CFString, CFString, CFString)](/documentation/corefoundation/cfpreferencessetvalue(_:_:_:_:_:))

### Synchronizing Preferences

- [func CFPreferencesAppSynchronize(CFString) -> Bool](/documentation/corefoundation/cfpreferencesappsynchronize(_:))
- [func CFPreferencesSynchronize(CFString, CFString, CFString) -> Bool](/documentation/corefoundation/cfpreferencessynchronize(_:_:_:))

### Adding and Removing Suite Preferences

- [func CFPreferencesAddSuitePreferencesToApp(CFString, CFString)](/documentation/corefoundation/cfpreferencesaddsuitepreferencestoapp(_:_:))
- [func CFPreferencesRemoveSuitePreferencesFromApp(CFString, CFString)](/documentation/corefoundation/cfpreferencesremovesuitepreferencesfromapp(_:_:))

### Miscellaneous Functions

- [func CFPreferencesAppValueIsForced(CFString, CFString) -> Bool](/documentation/corefoundation/cfpreferencesappvalueisforced(_:_:))
- [func CFPreferencesCopyApplicationList(CFString, CFString) -> CFArray?](/documentation/corefoundation/cfpreferencescopyapplicationlist(_:_:))

### Constants

- [Application, Host, and User Keys](/documentation/corefoundation/application-host-and-user-keys)

#### Constants

- [let kCFPreferencesAnyApplication: CFString](/documentation/corefoundation/kcfpreferencesanyapplication)
- [let kCFPreferencesAnyHost: CFString](/documentation/corefoundation/kcfpreferencesanyhost)
- [let kCFPreferencesAnyUser: CFString](/documentation/corefoundation/kcfpreferencesanyuser)
- [let kCFPreferencesCurrentApplication: CFString](/documentation/corefoundation/kcfpreferencescurrentapplication)
- [let kCFPreferencesCurrentHost: CFString](/documentation/corefoundation/kcfpreferencescurrenthost)
- [let kCFPreferencesCurrentUser: CFString](/documentation/corefoundation/kcfpreferencescurrentuser)
- [Socket Name Server Utilities](/documentation/corefoundation/socket-name-server-utilities)

### Core Foundation Socket Name Server Utilities Miscellaneous Functions

- [func CFSocketCopyRegisteredSocketSignature(UnsafePointer<CFSocketSignature>!, CFTimeInterval, CFString!, UnsafeMutablePointer<CFSocketSignature>!, UnsafeMutablePointer<Unmanaged<CFData>?>!) -> CFSocketError](/documentation/corefoundation/cfsocketcopyregisteredsocketsignature(_:_:_:_:_:))
- [func CFSocketCopyRegisteredValue(UnsafePointer<CFSocketSignature>!, CFTimeInterval, CFString!, UnsafeMutablePointer<Unmanaged<CFPropertyList>?>!, UnsafeMutablePointer<Unmanaged<CFData>?>!) -> CFSocketError](/documentation/corefoundation/cfsocketcopyregisteredvalue(_:_:_:_:_:))
- [func CFSocketGetDefaultNameRegistryPortNumber() -> UInt16](/documentation/corefoundation/cfsocketgetdefaultnameregistryportnumber())
- [func CFSocketRegisterSocketSignature(UnsafePointer<CFSocketSignature>!, CFTimeInterval, CFString!, UnsafePointer<CFSocketSignature>!) -> CFSocketError](/documentation/corefoundation/cfsocketregistersocketsignature(_:_:_:_:))
- [func CFSocketRegisterValue(UnsafePointer<CFSocketSignature>!, CFTimeInterval, CFString!, CFPropertyList!) -> CFSocketError](/documentation/corefoundation/cfsocketregistervalue(_:_:_:_:))
- [func CFSocketSetDefaultNameRegistryPortNumber(UInt16)](/documentation/corefoundation/cfsocketsetdefaultnameregistryportnumber(_:))
- [func CFSocketUnregister(UnsafePointer<CFSocketSignature>!, CFTimeInterval, CFString!) -> CFSocketError](/documentation/corefoundation/cfsocketunregister(_:_:_:))

### Constants

- [CFSocket Name Server Keys](/documentation/corefoundation/cfsocket-name-server-keys)

#### Constants

- [let kCFSocketCommandKey: CFString!](/documentation/corefoundation/kcfsocketcommandkey)
- [let kCFSocketNameKey: CFString!](/documentation/corefoundation/kcfsocketnamekey)
- [let kCFSocketValueKey: CFString!](/documentation/corefoundation/kcfsocketvaluekey)
- [let kCFSocketResultKey: CFString!](/documentation/corefoundation/kcfsocketresultkey)
- [let kCFSocketErrorKey: CFString!](/documentation/corefoundation/kcfsocketerrorkey)
- [let kCFSocketRegisterCommand: CFString!](/documentation/corefoundation/kcfsocketregistercommand)
- [let kCFSocketRetrieveCommand: CFString!](/documentation/corefoundation/kcfsocketretrievecommand)
- [Time Utilities](/documentation/corefoundation/time-utilities)

### Core Foundation Time Utilities Miscellaneous Functions

- [func CFAbsoluteTimeAddGregorianUnits(CFAbsoluteTime, CFTimeZone!, CFGregorianUnits) -> CFAbsoluteTime](/documentation/corefoundation/cfabsolutetimeaddgregorianunits(_:_:_:))
- [func CFAbsoluteTimeGetCurrent() -> CFAbsoluteTime](/documentation/corefoundation/cfabsolutetimegetcurrent())
- [func CFAbsoluteTimeGetDayOfWeek(CFAbsoluteTime, CFTimeZone!) -> Int32](/documentation/corefoundation/cfabsolutetimegetdayofweek(_:_:))
- [func CFAbsoluteTimeGetDayOfYear(CFAbsoluteTime, CFTimeZone!) -> Int32](/documentation/corefoundation/cfabsolutetimegetdayofyear(_:_:))
- [func CFAbsoluteTimeGetDifferenceAsGregorianUnits(CFAbsoluteTime, CFAbsoluteTime, CFTimeZone!, CFOptionFlags) -> CFGregorianUnits](/documentation/corefoundation/cfabsolutetimegetdifferenceasgregorianunits(_:_:_:_:))
- [func CFAbsoluteTimeGetGregorianDate(CFAbsoluteTime, CFTimeZone!) -> CFGregorianDate](/documentation/corefoundation/cfabsolutetimegetgregoriandate(_:_:))
- [func CFAbsoluteTimeGetWeekOfYear(CFAbsoluteTime, CFTimeZone!) -> Int32](/documentation/corefoundation/cfabsolutetimegetweekofyear(_:_:))
- [func CFGregorianDateGetAbsoluteTime(CFGregorianDate, CFTimeZone!) -> CFAbsoluteTime](/documentation/corefoundation/cfgregoriandategetabsolutetime(_:_:))
- [func CFGregorianDateIsValid(CFGregorianDate, CFOptionFlags) -> Bool](/documentation/corefoundation/cfgregoriandateisvalid(_:_:))

### Data Types

- [CFAbsoluteTime](/documentation/corefoundation/cfabsolutetime)
- [CFGregorianDate](/documentation/corefoundation/cfgregoriandate)

#### Initializers

- [init()](/documentation/corefoundation/cfgregoriandate/init())
- [init(year: Int32, month: Int8, day: Int8, hour: Int8, minute: Int8, second: Double)](/documentation/corefoundation/cfgregoriandate/init(year:month:day:hour:minute:second:))

#### Instance Properties

- [var day: Int8](/documentation/corefoundation/cfgregoriandate/day)
- [var hour: Int8](/documentation/corefoundation/cfgregoriandate/hour)
- [var minute: Int8](/documentation/corefoundation/cfgregoriandate/minute)
- [var month: Int8](/documentation/corefoundation/cfgregoriandate/month)
- [var second: Double](/documentation/corefoundation/cfgregoriandate/second)
- [var year: Int32](/documentation/corefoundation/cfgregoriandate/year)
- [CFGregorianUnits](/documentation/corefoundation/cfgregorianunits)

#### Initializers

- [init()](/documentation/corefoundation/cfgregorianunits/init())
- [init(years: Int32, months: Int32, days: Int32, hours: Int32, minutes: Int32, seconds: Double)](/documentation/corefoundation/cfgregorianunits/init(years:months:days:hours:minutes:seconds:))

#### Instance Properties

- [var days: Int32](/documentation/corefoundation/cfgregorianunits/days)
- [var hours: Int32](/documentation/corefoundation/cfgregorianunits/hours)
- [var minutes: Int32](/documentation/corefoundation/cfgregorianunits/minutes)
- [var months: Int32](/documentation/corefoundation/cfgregorianunits/months)
- [var seconds: Double](/documentation/corefoundation/cfgregorianunits/seconds)
- [var years: Int32](/documentation/corefoundation/cfgregorianunits/years)
- [CFTimeInterval](/documentation/corefoundation/cftimeinterval)

### Constants

- [CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags)

#### Constants

- [static var unitsYears: CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags/unitsyears)
- [static var unitsMonths: CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags/unitsmonths)
- [static var unitsDays: CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags/unitsdays)
- [static var unitsHours: CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags/unitshours)
- [static var unitsMinutes: CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags/unitsminutes)
- [static var unitsSeconds: CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags/unitsseconds)
- [static var allUnits: CFGregorianUnitFlags](/documentation/corefoundation/cfgregorianunitflags/allunits)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfgregorianunitflags/init(rawvalue:))
- [Predefined Time Interval Values](/documentation/corefoundation/predefined-time-interval-values)

#### Constants

- [let kCFAbsoluteTimeIntervalSince1970: CFTimeInterval](/documentation/corefoundation/kcfabsolutetimeintervalsince1970)
- [let kCFAbsoluteTimeIntervalSince1904: CFTimeInterval](/documentation/corefoundation/kcfabsolutetimeintervalsince1904)

## Opaque Types

- [CFAllocator](/documentation/corefoundation/cfallocator)

### Creating an Allocator

- [func CFAllocatorCreate(CFAllocator!, UnsafeMutablePointer<CFAllocatorContext>!) -> Unmanaged<CFAllocator>!](/documentation/corefoundation/cfallocatorcreate(_:_:))

### Managing Memory with an Allocator

- [func CFAllocatorAllocate(CFAllocator!, CFIndex, CFOptionFlags) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfallocatorallocate(_:_:_:))
- [func CFAllocatorDeallocate(CFAllocator!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cfallocatordeallocate(_:_:))
- [func CFAllocatorGetPreferredSizeForSize(CFAllocator!, CFIndex, CFOptionFlags) -> CFIndex](/documentation/corefoundation/cfallocatorgetpreferredsizeforsize(_:_:_:))
- [func CFAllocatorReallocate(CFAllocator!, UnsafeMutableRawPointer!, CFIndex, CFOptionFlags) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfallocatorreallocate(_:_:_:_:))

### Getting and Setting the Default Allocator

- [func CFAllocatorGetDefault() -> Unmanaged<CFAllocator>!](/documentation/corefoundation/cfallocatorgetdefault())
- [func CFAllocatorSetDefault(CFAllocator!)](/documentation/corefoundation/cfallocatorsetdefault(_:))

### Getting an Allocator’s Context

- [func CFAllocatorGetContext(CFAllocator!, UnsafeMutablePointer<CFAllocatorContext>!)](/documentation/corefoundation/cfallocatorgetcontext(_:_:))

### Getting the CFAllocator Type ID

- [func CFAllocatorGetTypeID() -> CFTypeID](/documentation/corefoundation/cfallocatorgettypeid())

### Callbacks

- [CFAllocatorAllocateCallBack](/documentation/corefoundation/cfallocatorallocatecallback)
- [CFAllocatorCopyDescriptionCallBack](/documentation/corefoundation/cfallocatorcopydescriptioncallback)
- [CFAllocatorDeallocateCallBack](/documentation/corefoundation/cfallocatordeallocatecallback)
- [CFAllocatorPreferredSizeCallBack](/documentation/corefoundation/cfallocatorpreferredsizecallback)
- [CFAllocatorReallocateCallBack](/documentation/corefoundation/cfallocatorreallocatecallback)
- [CFAllocatorReleaseCallBack](/documentation/corefoundation/cfallocatorreleasecallback)
- [CFAllocatorRetainCallBack](/documentation/corefoundation/cfallocatorretaincallback)

### Data Types

- [CFAllocatorContext](/documentation/corefoundation/cfallocatorcontext)

#### Initializers

- [init()](/documentation/corefoundation/cfallocatorcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: CFAllocatorRetainCallBack!, release: CFAllocatorReleaseCallBack!, copyDescription: CFAllocatorCopyDescriptionCallBack!, allocate: CFAllocatorAllocateCallBack!, reallocate: CFAllocatorReallocateCallBack!, deallocate: CFAllocatorDeallocateCallBack!, preferredSize: CFAllocatorPreferredSizeCallBack!)](/documentation/corefoundation/cfallocatorcontext/init(version:info:retain:release:copydescription:allocate:reallocate:deallocate:preferredsize:))

#### Instance Properties

- [var allocate: CFAllocatorAllocateCallBack!](/documentation/corefoundation/cfallocatorcontext/allocate)
- [var copyDescription: CFAllocatorCopyDescriptionCallBack!](/documentation/corefoundation/cfallocatorcontext/copydescription)
- [var deallocate: CFAllocatorDeallocateCallBack!](/documentation/corefoundation/cfallocatorcontext/deallocate)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfallocatorcontext/info)
- [var preferredSize: CFAllocatorPreferredSizeCallBack!](/documentation/corefoundation/cfallocatorcontext/preferredsize)
- [var reallocate: CFAllocatorReallocateCallBack!](/documentation/corefoundation/cfallocatorcontext/reallocate)
- [var release: CFAllocatorReleaseCallBack!](/documentation/corefoundation/cfallocatorcontext/release)
- [var retain: CFAllocatorRetainCallBack!](/documentation/corefoundation/cfallocatorcontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfallocatorcontext/version)

### Constants

- [Predefined Allocators](/documentation/corefoundation/predefined-allocators)

#### Constants

- [let kCFAllocatorDefault: CFAllocator!](/documentation/corefoundation/kcfallocatordefault)
- [let kCFAllocatorSystemDefault: CFAllocator!](/documentation/corefoundation/kcfallocatorsystemdefault)
- [let kCFAllocatorMalloc: CFAllocator!](/documentation/corefoundation/kcfallocatormalloc)
- [let kCFAllocatorMallocZone: CFAllocator!](/documentation/corefoundation/kcfallocatormalloczone)
- [let kCFAllocatorNull: CFAllocator!](/documentation/corefoundation/kcfallocatornull)
- [let kCFAllocatorUseContext: CFAllocator!](/documentation/corefoundation/kcfallocatorusecontext)
- [CFArray](/documentation/corefoundation/cfarray)

### Creating an Array

- [func CFArrayCreate(CFAllocator!, UnsafeMutablePointer<UnsafeRawPointer?>!, CFIndex, UnsafePointer<CFArrayCallBacks>!) -> CFArray!](/documentation/corefoundation/cfarraycreate(_:_:_:_:))
- [func CFArrayCreateCopy(CFAllocator!, CFArray!) -> CFArray!](/documentation/corefoundation/cfarraycreatecopy(_:_:))

### Examining an Array

- [func CFArrayBSearchValues(CFArray!, CFRange, UnsafeRawPointer!, CFComparatorFunction!, UnsafeMutableRawPointer!) -> CFIndex](/documentation/corefoundation/cfarraybsearchvalues(_:_:_:_:_:))
- [func CFArrayContainsValue(CFArray!, CFRange, UnsafeRawPointer!) -> Bool](/documentation/corefoundation/cfarraycontainsvalue(_:_:_:))
- [func CFArrayGetCount(CFArray!) -> CFIndex](/documentation/corefoundation/cfarraygetcount(_:))
- [func CFArrayGetCountOfValue(CFArray!, CFRange, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfarraygetcountofvalue(_:_:_:))
- [func CFArrayGetFirstIndexOfValue(CFArray!, CFRange, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfarraygetfirstindexofvalue(_:_:_:))
- [func CFArrayGetLastIndexOfValue(CFArray!, CFRange, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfarraygetlastindexofvalue(_:_:_:))
- [func CFArrayGetValues(CFArray!, CFRange, UnsafeMutablePointer<UnsafeRawPointer?>!)](/documentation/corefoundation/cfarraygetvalues(_:_:_:))
- [func CFArrayGetValueAtIndex(CFArray!, CFIndex) -> UnsafeRawPointer!](/documentation/corefoundation/cfarraygetvalueatindex(_:_:))

### Applying a Function to Elements

- [func CFArrayApplyFunction(CFArray!, CFRange, ((UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void)!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cfarrayapplyfunction(_:_:_:_:))

### Getting the CFArray Type ID

- [func CFArrayGetTypeID() -> CFTypeID](/documentation/corefoundation/cfarraygettypeid())

### Callbacks

- [CFArrayApplierFunction](/documentation/corefoundation/cfarrayapplierfunction)
- [CFArrayCopyDescriptionCallBack](/documentation/corefoundation/cfarraycopydescriptioncallback)
- [CFArrayEqualCallBack](/documentation/corefoundation/cfarrayequalcallback)
- [CFArrayReleaseCallBack](/documentation/corefoundation/cfarrayreleasecallback)
- [CFArrayRetainCallBack](/documentation/corefoundation/cfarrayretaincallback)

### Data Types

- [CFArrayCallBacks](/documentation/corefoundation/cfarraycallbacks)

#### Initializers

- [init()](/documentation/corefoundation/cfarraycallbacks/init())
- [init(version: CFIndex, retain: CFArrayRetainCallBack!, release: CFArrayReleaseCallBack!, copyDescription: CFArrayCopyDescriptionCallBack!, equal: CFArrayEqualCallBack!)](/documentation/corefoundation/cfarraycallbacks/init(version:retain:release:copydescription:equal:))

#### Instance Properties

- [var copyDescription: CFArrayCopyDescriptionCallBack!](/documentation/corefoundation/cfarraycallbacks/copydescription)
- [var equal: CFArrayEqualCallBack!](/documentation/corefoundation/cfarraycallbacks/equal)
- [var release: CFArrayReleaseCallBack!](/documentation/corefoundation/cfarraycallbacks/release)
- [var retain: CFArrayRetainCallBack!](/documentation/corefoundation/cfarraycallbacks/retain)
- [var version: CFIndex](/documentation/corefoundation/cfarraycallbacks/version)

### Constants

- [Predefined Callback Structures](/documentation/corefoundation/predefined-callback-structures)

#### Constants

- [let kCFTypeArrayCallBacks: CFArrayCallBacks](/documentation/corefoundation/kcftypearraycallbacks)
- [CFAttributedString](/documentation/corefoundation/cfattributedstring)

### Creating a CFAttributedString

- [func CFAttributedStringCreate(CFAllocator!, CFString!, CFDictionary!) -> CFAttributedString!](/documentation/corefoundation/cfattributedstringcreate(_:_:_:))
- [func CFAttributedStringCreateCopy(CFAllocator!, CFAttributedString!) -> CFAttributedString!](/documentation/corefoundation/cfattributedstringcreatecopy(_:_:))
- [func CFAttributedStringCreateWithSubstring(CFAllocator!, CFAttributedString!, CFRange) -> CFAttributedString!](/documentation/corefoundation/cfattributedstringcreatewithsubstring(_:_:_:))
- [func CFAttributedStringGetLength(CFAttributedString!) -> CFIndex](/documentation/corefoundation/cfattributedstringgetlength(_:))
- [func CFAttributedStringGetString(CFAttributedString!) -> CFString!](/documentation/corefoundation/cfattributedstringgetstring(_:))

### Accessing Attributes

- [func CFAttributedStringGetAttribute(CFAttributedString!, CFIndex, CFString!, UnsafeMutablePointer<CFRange>!) -> CFTypeRef!](/documentation/corefoundation/cfattributedstringgetattribute(_:_:_:_:))
- [func CFAttributedStringGetAttributes(CFAttributedString!, CFIndex, UnsafeMutablePointer<CFRange>!) -> CFDictionary!](/documentation/corefoundation/cfattributedstringgetattributes(_:_:_:))
- [func CFAttributedStringGetAttributeAndLongestEffectiveRange(CFAttributedString!, CFIndex, CFString!, CFRange, UnsafeMutablePointer<CFRange>!) -> CFTypeRef!](/documentation/corefoundation/cfattributedstringgetattributeandlongesteffectiverange(_:_:_:_:_:))
- [func CFAttributedStringGetAttributesAndLongestEffectiveRange(CFAttributedString!, CFIndex, CFRange, UnsafeMutablePointer<CFRange>!) -> CFDictionary!](/documentation/corefoundation/cfattributedstringgetattributesandlongesteffectiverange(_:_:_:_:))

### Getting Attributed String Properties

- [func CFAttributedStringGetTypeID() -> CFTypeID](/documentation/corefoundation/cfattributedstringgettypeid())
- [CFBag](/documentation/corefoundation/cfbag)

### Creating a Bag

- [func CFBagCreate(CFAllocator!, UnsafeMutablePointer<UnsafeRawPointer?>!, CFIndex, UnsafePointer<CFBagCallBacks>!) -> CFBag!](/documentation/corefoundation/cfbagcreate(_:_:_:_:))
- [func CFBagCreateCopy(CFAllocator!, CFBag!) -> CFBag!](/documentation/corefoundation/cfbagcreatecopy(_:_:))

### Examining a Bag

- [func CFBagContainsValue(CFBag!, UnsafeRawPointer!) -> Bool](/documentation/corefoundation/cfbagcontainsvalue(_:_:))
- [func CFBagGetCount(CFBag!) -> CFIndex](/documentation/corefoundation/cfbaggetcount(_:))
- [func CFBagGetCountOfValue(CFBag!, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfbaggetcountofvalue(_:_:))
- [func CFBagGetValue(CFBag!, UnsafeRawPointer!) -> UnsafeRawPointer!](/documentation/corefoundation/cfbaggetvalue(_:_:))
- [func CFBagGetValueIfPresent(CFBag!, UnsafeRawPointer!, UnsafeMutablePointer<UnsafeRawPointer?>!) -> Bool](/documentation/corefoundation/cfbaggetvalueifpresent(_:_:_:))
- [func CFBagGetValues(CFBag!, UnsafeMutablePointer<UnsafeRawPointer?>!)](/documentation/corefoundation/cfbaggetvalues(_:_:))

### Applying a Function to the Contents of a Bag

- [func CFBagApplyFunction(CFBag!, ((UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void)!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cfbagapplyfunction(_:_:_:))

### Getting the CFBag Type ID

- [func CFBagGetTypeID() -> CFTypeID](/documentation/corefoundation/cfbaggettypeid())

### Callbacks

- [CFBagApplierFunction](/documentation/corefoundation/cfbagapplierfunction)
- [CFBagCopyDescriptionCallBack](/documentation/corefoundation/cfbagcopydescriptioncallback)
- [CFBagEqualCallBack](/documentation/corefoundation/cfbagequalcallback)
- [CFBagHashCallBack](/documentation/corefoundation/cfbaghashcallback)
- [CFBagReleaseCallBack](/documentation/corefoundation/cfbagreleasecallback)
- [CFBagRetainCallBack](/documentation/corefoundation/cfbagretaincallback)

### Data Types

- [CFBagCallBacks](/documentation/corefoundation/cfbagcallbacks)

#### Initializers

- [init()](/documentation/corefoundation/cfbagcallbacks/init())
- [init(version: CFIndex, retain: CFBagRetainCallBack!, release: CFBagReleaseCallBack!, copyDescription: CFBagCopyDescriptionCallBack!, equal: CFBagEqualCallBack!, hash: CFBagHashCallBack!)](/documentation/corefoundation/cfbagcallbacks/init(version:retain:release:copydescription:equal:hash:))

#### Instance Properties

- [var copyDescription: CFBagCopyDescriptionCallBack!](/documentation/corefoundation/cfbagcallbacks/copydescription)
- [var equal: CFBagEqualCallBack!](/documentation/corefoundation/cfbagcallbacks/equal)
- [var hash: CFBagHashCallBack!](/documentation/corefoundation/cfbagcallbacks/hash)
- [var release: CFBagReleaseCallBack!](/documentation/corefoundation/cfbagcallbacks/release)
- [var retain: CFBagRetainCallBack!](/documentation/corefoundation/cfbagcallbacks/retain)
- [var version: CFIndex](/documentation/corefoundation/cfbagcallbacks/version)

### Constants

- [Predefined Callback Structures](/documentation/corefoundation/cfbag-predefined-callback-structures)

#### Constants

- [let kCFTypeBagCallBacks: CFBagCallBacks](/documentation/corefoundation/kcftypebagcallbacks)
- [let kCFCopyStringBagCallBacks: CFBagCallBacks](/documentation/corefoundation/kcfcopystringbagcallbacks)
- [CFBinaryHeap](/documentation/corefoundation/cfbinaryheap)

### CFBinaryHeap Miscellaneous Functions

- [func CFBinaryHeapAddValue(CFBinaryHeap!, UnsafeRawPointer!)](/documentation/corefoundation/cfbinaryheapaddvalue(_:_:))
- [func CFBinaryHeapApplyFunction(CFBinaryHeap!, ((UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void)!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cfbinaryheapapplyfunction(_:_:_:))
- [func CFBinaryHeapContainsValue(CFBinaryHeap!, UnsafeRawPointer!) -> Bool](/documentation/corefoundation/cfbinaryheapcontainsvalue(_:_:))
- [func CFBinaryHeapCreate(CFAllocator!, CFIndex, UnsafePointer<CFBinaryHeapCallBacks>!, UnsafePointer<CFBinaryHeapCompareContext>!) -> CFBinaryHeap!](/documentation/corefoundation/cfbinaryheapcreate(_:_:_:_:))
- [func CFBinaryHeapCreateCopy(CFAllocator!, CFIndex, CFBinaryHeap!) -> CFBinaryHeap!](/documentation/corefoundation/cfbinaryheapcreatecopy(_:_:_:))
- [func CFBinaryHeapGetCount(CFBinaryHeap!) -> CFIndex](/documentation/corefoundation/cfbinaryheapgetcount(_:))
- [func CFBinaryHeapGetCountOfValue(CFBinaryHeap!, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfbinaryheapgetcountofvalue(_:_:))
- [func CFBinaryHeapGetMinimum(CFBinaryHeap!) -> UnsafeRawPointer!](/documentation/corefoundation/cfbinaryheapgetminimum(_:))
- [func CFBinaryHeapGetMinimumIfPresent(CFBinaryHeap!, UnsafeMutablePointer<UnsafeRawPointer?>!) -> Bool](/documentation/corefoundation/cfbinaryheapgetminimumifpresent(_:_:))
- [func CFBinaryHeapGetTypeID() -> CFTypeID](/documentation/corefoundation/cfbinaryheapgettypeid())
- [func CFBinaryHeapGetValues(CFBinaryHeap!, UnsafeMutablePointer<UnsafeRawPointer?>!)](/documentation/corefoundation/cfbinaryheapgetvalues(_:_:))
- [func CFBinaryHeapRemoveAllValues(CFBinaryHeap!)](/documentation/corefoundation/cfbinaryheapremoveallvalues(_:))
- [func CFBinaryHeapRemoveMinimumValue(CFBinaryHeap!)](/documentation/corefoundation/cfbinaryheapremoveminimumvalue(_:))

### Callbacks

- [CFBinaryHeapApplierFunction](/documentation/corefoundation/cfbinaryheapapplierfunction)
- [var compare: ((UnsafeRawPointer?, UnsafeRawPointer?, UnsafeMutableRawPointer?) -> CFComparisonResult)!](/documentation/corefoundation/cfbinaryheapcallbacks/compare)
- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfbinaryheapcallbacks/copydescription)
- [var release: ((CFAllocator?, UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfbinaryheapcallbacks/release)
- [var retain: ((CFAllocator?, UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfbinaryheapcallbacks/retain)
- [var version: CFIndex](/documentation/corefoundation/cfbinaryheapcallbacks/version)

### Data Types

- [CFBinaryHeapCallBacks](/documentation/corefoundation/cfbinaryheapcallbacks)

#### Initializers

- [init()](/documentation/corefoundation/cfbinaryheapcallbacks/init())
- [init(version: CFIndex, retain: ((CFAllocator?, UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((CFAllocator?, UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!, compare: ((UnsafeRawPointer?, UnsafeRawPointer?, UnsafeMutableRawPointer?) -> CFComparisonResult)!)](/documentation/corefoundation/cfbinaryheapcallbacks/init(version:retain:release:copydescription:compare:))

#### Instance Properties

- [var compare: ((UnsafeRawPointer?, UnsafeRawPointer?, UnsafeMutableRawPointer?) -> CFComparisonResult)!](/documentation/corefoundation/cfbinaryheapcallbacks/compare)
- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfbinaryheapcallbacks/copydescription)
- [var release: ((CFAllocator?, UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfbinaryheapcallbacks/release)
- [var retain: ((CFAllocator?, UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfbinaryheapcallbacks/retain)
- [var version: CFIndex](/documentation/corefoundation/cfbinaryheapcallbacks/version)
- [CFBinaryHeapCompareContext](/documentation/corefoundation/cfbinaryheapcomparecontext)

#### Initializers

- [init()](/documentation/corefoundation/cfbinaryheapcomparecontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfbinaryheapcomparecontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfbinaryheapcomparecontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfbinaryheapcomparecontext/info)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfbinaryheapcomparecontext/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfbinaryheapcomparecontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfbinaryheapcomparecontext/version)

### Constants

- [Predefined Callback Structures](/documentation/corefoundation/cfbinaryheap-predefined-callback-structures)

#### Constants

- [let kCFStringBinaryHeapCallBacks: CFBinaryHeapCallBacks](/documentation/corefoundation/kcfstringbinaryheapcallbacks)
- [CFBitVector](/documentation/corefoundation/cfbitvector)

### Creating a Bit Vector

- [func CFBitVectorCreate(CFAllocator!, UnsafePointer<UInt8>!, CFIndex) -> CFBitVector!](/documentation/corefoundation/cfbitvectorcreate(_:_:_:))
- [func CFBitVectorCreateCopy(CFAllocator!, CFBitVector!) -> CFBitVector!](/documentation/corefoundation/cfbitvectorcreatecopy(_:_:))

### Getting Information About a Bit Vector

- [func CFBitVectorContainsBit(CFBitVector!, CFRange, CFBit) -> Bool](/documentation/corefoundation/cfbitvectorcontainsbit(_:_:_:))
- [func CFBitVectorGetBitAtIndex(CFBitVector!, CFIndex) -> CFBit](/documentation/corefoundation/cfbitvectorgetbitatindex(_:_:))
- [func CFBitVectorGetBits(CFBitVector!, CFRange, UnsafeMutablePointer<UInt8>!)](/documentation/corefoundation/cfbitvectorgetbits(_:_:_:))
- [func CFBitVectorGetCount(CFBitVector!) -> CFIndex](/documentation/corefoundation/cfbitvectorgetcount(_:))
- [func CFBitVectorGetCountOfBit(CFBitVector!, CFRange, CFBit) -> CFIndex](/documentation/corefoundation/cfbitvectorgetcountofbit(_:_:_:))
- [func CFBitVectorGetFirstIndexOfBit(CFBitVector!, CFRange, CFBit) -> CFIndex](/documentation/corefoundation/cfbitvectorgetfirstindexofbit(_:_:_:))
- [func CFBitVectorGetLastIndexOfBit(CFBitVector!, CFRange, CFBit) -> CFIndex](/documentation/corefoundation/cfbitvectorgetlastindexofbit(_:_:_:))

### Getting the CFBitVector Type ID

- [func CFBitVectorGetTypeID() -> CFTypeID](/documentation/corefoundation/cfbitvectorgettypeid())

### Data Types

- [CFBit](/documentation/corefoundation/cfbit)
- [CFBoolean](/documentation/corefoundation/cfboolean)

### CFBoolean Miscellaneous Functions

- [func CFBooleanGetTypeID() -> CFTypeID](/documentation/corefoundation/cfbooleangettypeid())
- [func CFBooleanGetValue(CFBoolean!) -> Bool](/documentation/corefoundation/cfbooleangetvalue(_:))

### Constants

- [Boolean Values](/documentation/corefoundation/boolean-values)

#### Constants

- [let kCFBooleanTrue: CFBoolean!](/documentation/corefoundation/kcfbooleantrue)
- [let kCFBooleanFalse: CFBoolean!](/documentation/corefoundation/kcfbooleanfalse)
- [CFBundle](/documentation/corefoundation/cfbundle)

### Creating and Accessing Bundles

- [func CFBundleCreate(CFAllocator!, CFURL!) -> CFBundle!](/documentation/corefoundation/cfbundlecreate(_:_:))
- [func CFBundleCreateBundlesFromDirectory(CFAllocator!, CFURL!, CFString!) -> CFArray!](/documentation/corefoundation/cfbundlecreatebundlesfromdirectory(_:_:_:))
- [func CFBundleGetAllBundles() -> CFArray!](/documentation/corefoundation/cfbundlegetallbundles())
- [func CFBundleGetBundleWithIdentifier(CFString!) -> CFBundle!](/documentation/corefoundation/cfbundlegetbundlewithidentifier(_:))
- [func CFBundleGetMainBundle() -> CFBundle!](/documentation/corefoundation/cfbundlegetmainbundle())

### Loading and Unloading a Bundle

- [func CFBundleIsExecutableLoaded(CFBundle!) -> Bool](/documentation/corefoundation/cfbundleisexecutableloaded(_:))
- [func CFBundlePreflightExecutable(CFBundle!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/corefoundation/cfbundlepreflightexecutable(_:_:))
- [func CFBundleLoadExecutable(CFBundle!) -> Bool](/documentation/corefoundation/cfbundleloadexecutable(_:))
- [func CFBundleLoadExecutableAndReturnError(CFBundle!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/corefoundation/cfbundleloadexecutableandreturnerror(_:_:))
- [func CFBundleUnloadExecutable(CFBundle!)](/documentation/corefoundation/cfbundleunloadexecutable(_:))

### Finding Locations in a Bundle

- [func CFBundleCopyAuxiliaryExecutableURL(CFBundle!, CFString!) -> CFURL!](/documentation/corefoundation/cfbundlecopyauxiliaryexecutableurl(_:_:))
- [func CFBundleCopyBuiltInPlugInsURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopybuiltinpluginsurl(_:))
- [func CFBundleCopyExecutableURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopyexecutableurl(_:))
- [func CFBundleCopyPrivateFrameworksURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopyprivateframeworksurl(_:))
- [func CFBundleCopyResourcesDirectoryURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopyresourcesdirectoryurl(_:))
- [func CFBundleCopySharedFrameworksURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopysharedframeworksurl(_:))
- [func CFBundleCopySharedSupportURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopysharedsupporturl(_:))
- [func CFBundleCopySupportFilesDirectoryURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopysupportfilesdirectoryurl(_:))

### Locating Bundle Resources

- [func CFBundleCloseBundleResourceMap(CFBundle!, CFBundleRefNum)](/documentation/corefoundation/cfbundleclosebundleresourcemap(_:_:))
- [func CFBundleCopyResourceURL(CFBundle!, CFString!, CFString!, CFString!) -> CFURL!](/documentation/corefoundation/cfbundlecopyresourceurl(_:_:_:_:))
- [func CFBundleCopyResourceURLInDirectory(CFURL!, CFString!, CFString!, CFString!) -> CFURL!](/documentation/corefoundation/cfbundlecopyresourceurlindirectory(_:_:_:_:))
- [func CFBundleCopyResourceURLsOfType(CFBundle!, CFString!, CFString!) -> CFArray!](/documentation/corefoundation/cfbundlecopyresourceurlsoftype(_:_:_:))
- [func CFBundleCopyResourceURLsOfTypeInDirectory(CFURL!, CFString!, CFString!) -> CFArray!](/documentation/corefoundation/cfbundlecopyresourceurlsoftypeindirectory(_:_:_:))
- [func CFBundleCopyResourceURLForLocalization(CFBundle!, CFString!, CFString!, CFString!, CFString!) -> CFURL!](/documentation/corefoundation/cfbundlecopyresourceurlforlocalization(_:_:_:_:_:))
- [func CFBundleCopyResourceURLsOfTypeForLocalization(CFBundle!, CFString!, CFString!, CFString!) -> CFArray!](/documentation/corefoundation/cfbundlecopyresourceurlsoftypeforlocalization(_:_:_:_:))
- [func CFBundleOpenBundleResourceFiles(CFBundle!, UnsafeMutablePointer<CFBundleRefNum>!, UnsafeMutablePointer<CFBundleRefNum>!) -> Int32](/documentation/corefoundation/cfbundleopenbundleresourcefiles(_:_:_:))
- [func CFBundleOpenBundleResourceMap(CFBundle!) -> CFBundleRefNum](/documentation/corefoundation/cfbundleopenbundleresourcemap(_:))

### Managing Localizations

- [func CFBundleCopyBundleLocalizations(CFBundle!) -> CFArray!](/documentation/corefoundation/cfbundlecopybundlelocalizations(_:))
- [func CFBundleCopyLocalizedString(CFBundle!, CFString!, CFString!, CFString!) -> CFString!](/documentation/corefoundation/cfbundlecopylocalizedstring(_:_:_:_:))
- [func CFBundleCopyLocalizationsForPreferences(CFArray!, CFArray!) -> CFArray!](/documentation/corefoundation/cfbundlecopylocalizationsforpreferences(_:_:))
- [func CFBundleCopyLocalizationsForURL(CFURL!) -> CFArray!](/documentation/corefoundation/cfbundlecopylocalizationsforurl(_:))
- [func CFBundleCopyPreferredLocalizationsFromArray(CFArray!) -> CFArray!](/documentation/corefoundation/cfbundlecopypreferredlocalizationsfromarray(_:))

### Managing Executable Code

- [func CFBundleGetDataPointerForName(CFBundle!, CFString!) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfbundlegetdatapointerforname(_:_:))
- [func CFBundleGetDataPointersForNames(CFBundle!, CFArray!, UnsafeMutablePointer<UnsafeMutableRawPointer?>!)](/documentation/corefoundation/cfbundlegetdatapointersfornames(_:_:_:))
- [func CFBundleGetFunctionPointerForName(CFBundle!, CFString!) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfbundlegetfunctionpointerforname(_:_:))
- [func CFBundleGetFunctionPointersForNames(CFBundle!, CFArray!, UnsafeMutablePointer<UnsafeMutableRawPointer?>!)](/documentation/corefoundation/cfbundlegetfunctionpointersfornames(_:_:_:))
- [func CFBundleGetPlugIn(CFBundle!) -> CFPlugIn!](/documentation/corefoundation/cfbundlegetplugin(_:))

### Getting Bundle Properties

- [func CFBundleCopyBundleURL(CFBundle!) -> CFURL!](/documentation/corefoundation/cfbundlecopybundleurl(_:))
- [func CFBundleGetDevelopmentRegion(CFBundle!) -> CFString!](/documentation/corefoundation/cfbundlegetdevelopmentregion(_:))
- [func CFBundleGetIdentifier(CFBundle!) -> CFString!](/documentation/corefoundation/cfbundlegetidentifier(_:))
- [func CFBundleGetInfoDictionary(CFBundle!) -> CFDictionary!](/documentation/corefoundation/cfbundlegetinfodictionary(_:))
- [func CFBundleGetLocalInfoDictionary(CFBundle!) -> CFDictionary!](/documentation/corefoundation/cfbundlegetlocalinfodictionary(_:))
- [func CFBundleGetValueForInfoDictionaryKey(CFBundle!, CFString!) -> CFTypeRef!](/documentation/corefoundation/cfbundlegetvalueforinfodictionarykey(_:_:))
- [func CFBundleCopyInfoDictionaryInDirectory(CFURL!) -> CFDictionary!](/documentation/corefoundation/cfbundlecopyinfodictionaryindirectory(_:))
- [func CFBundleCopyInfoDictionaryForURL(CFURL!) -> CFDictionary!](/documentation/corefoundation/cfbundlecopyinfodictionaryforurl(_:))
- [func CFBundleGetPackageInfo(CFBundle!, UnsafeMutablePointer<UInt32>!, UnsafeMutablePointer<UInt32>!)](/documentation/corefoundation/cfbundlegetpackageinfo(_:_:_:))
- [func CFBundleGetPackageInfoInDirectory(CFURL!, UnsafeMutablePointer<UInt32>!, UnsafeMutablePointer<UInt32>!) -> Bool](/documentation/corefoundation/cfbundlegetpackageinfoindirectory(_:_:_:))
- [func CFBundleCopyExecutableArchitectures(CFBundle!) -> CFArray!](/documentation/corefoundation/cfbundlecopyexecutablearchitectures(_:))
- [func CFBundleCopyExecutableArchitecturesForURL(CFURL!) -> CFArray!](/documentation/corefoundation/cfbundlecopyexecutablearchitecturesforurl(_:))
- [func CFBundleGetVersionNumber(CFBundle!) -> UInt32](/documentation/corefoundation/cfbundlegetversionnumber(_:))

### Getting the CFBundle Type ID

- [func CFBundleGetTypeID() -> CFTypeID](/documentation/corefoundation/cfbundlegettypeid())

### Data Types

- [CFBundleRefNum](/documentation/corefoundation/cfbundlerefnum)

### Constants

- [Information Property List Keys](/documentation/corefoundation/information-property-list-keys)

#### Constants

- [let kCFBundleInfoDictionaryVersionKey: CFString!](/documentation/corefoundation/kcfbundleinfodictionaryversionkey)
- [let kCFBundleExecutableKey: CFString!](/documentation/corefoundation/kcfbundleexecutablekey)
- [let kCFBundleIdentifierKey: CFString!](/documentation/corefoundation/kcfbundleidentifierkey)
- [let kCFBundleVersionKey: CFString!](/documentation/corefoundation/kcfbundleversionkey)
- [let kCFBundleDevelopmentRegionKey: CFString!](/documentation/corefoundation/kcfbundledevelopmentregionkey)
- [let kCFBundleNameKey: CFString!](/documentation/corefoundation/kcfbundlenamekey)
- [let kCFBundleLocalizationsKey: CFString!](/documentation/corefoundation/kcfbundlelocalizationskey)
- [Architecture Types](/documentation/corefoundation/1537096-architecture-types)

#### Constants

- [var kCFBundleExecutableArchitectureI386: Int](/documentation/corefoundation/kcfbundleexecutablearchitecturei386)
- [var kCFBundleExecutableArchitecturePPC: Int](/documentation/corefoundation/kcfbundleexecutablearchitectureppc)
- [var kCFBundleExecutableArchitectureARM64: Int](/documentation/corefoundation/kcfbundleexecutablearchitecturearm64)
- [var kCFBundleExecutableArchitectureX86_64: Int](/documentation/corefoundation/kcfbundleexecutablearchitecturex86_64)
- [var kCFBundleExecutableArchitecturePPC64: Int](/documentation/corefoundation/kcfbundleexecutablearchitectureppc64)
- [CFCalendar](/documentation/corefoundation/cfcalendar)

### Creating a Calendar

- [func CFCalendarCopyCurrent() -> CFCalendar!](/documentation/corefoundation/cfcalendarcopycurrent())
- [func CFCalendarCreateWithIdentifier(CFAllocator!, CFCalendarIdentifier!) -> CFCalendar!](/documentation/corefoundation/cfcalendarcreatewithidentifier(_:_:))

### Getting Ranges of Units

- [func CFCalendarGetRangeOfUnit(CFCalendar!, CFCalendarUnit, CFCalendarUnit, CFAbsoluteTime) -> CFRange](/documentation/corefoundation/cfcalendargetrangeofunit(_:_:_:_:))
- [func CFCalendarGetOrdinalityOfUnit(CFCalendar!, CFCalendarUnit, CFCalendarUnit, CFAbsoluteTime) -> CFIndex](/documentation/corefoundation/cfcalendargetordinalityofunit(_:_:_:_:))
- [func CFCalendarGetTimeRangeOfUnit(CFCalendar!, CFCalendarUnit, CFAbsoluteTime, UnsafeMutablePointer<CFAbsoluteTime>!, UnsafeMutablePointer<CFTimeInterval>!) -> Bool](/documentation/corefoundation/cfcalendargettimerangeofunit(_:_:_:_:_:))
- [func CFCalendarGetMaximumRangeOfUnit(CFCalendar!, CFCalendarUnit) -> CFRange](/documentation/corefoundation/cfcalendargetmaximumrangeofunit(_:_:))
- [func CFCalendarGetMinimumRangeOfUnit(CFCalendar!, CFCalendarUnit) -> CFRange](/documentation/corefoundation/cfcalendargetminimumrangeofunit(_:_:))

### Getting and Setting the Time Zone

- [func CFCalendarCopyTimeZone(CFCalendar!) -> CFTimeZone!](/documentation/corefoundation/cfcalendarcopytimezone(_:))
- [func CFCalendarSetTimeZone(CFCalendar!, CFTimeZone!)](/documentation/corefoundation/cfcalendarsettimezone(_:_:))

### Getting the Identifier

- [func CFCalendarGetIdentifier(CFCalendar!) -> CFCalendarIdentifier!](/documentation/corefoundation/cfcalendargetidentifier(_:))

### Getting and Setting the Locale

- [func CFCalendarCopyLocale(CFCalendar!) -> CFLocale!](/documentation/corefoundation/cfcalendarcopylocale(_:))
- [func CFCalendarSetLocale(CFCalendar!, CFLocale!)](/documentation/corefoundation/cfcalendarsetlocale(_:_:))

### Getting and Setting Day Information

- [func CFCalendarGetFirstWeekday(CFCalendar!) -> CFIndex](/documentation/corefoundation/cfcalendargetfirstweekday(_:))
- [func CFCalendarSetFirstWeekday(CFCalendar!, CFIndex)](/documentation/corefoundation/cfcalendarsetfirstweekday(_:_:))
- [func CFCalendarGetMinimumDaysInFirstWeek(CFCalendar!) -> CFIndex](/documentation/corefoundation/cfcalendargetminimumdaysinfirstweek(_:))
- [func CFCalendarSetMinimumDaysInFirstWeek(CFCalendar!, CFIndex)](/documentation/corefoundation/cfcalendarsetminimumdaysinfirstweek(_:_:))

### Getting the Type ID

- [func CFCalendarGetTypeID() -> CFTypeID](/documentation/corefoundation/cfcalendargettypeid())

### Constants

- [CFCalendarUnit](/documentation/corefoundation/cfcalendarunit)

#### Constants

- [static var era: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/era)
- [static var year: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/year)
- [static var month: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/month)
- [static var day: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/day)
- [static var hour: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/hour)
- [static var minute: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/minute)
- [static var second: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/second)
- [static var week: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/week)
- [static var weekday: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/weekday)
- [static var weekdayOrdinal: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/weekdayordinal)
- [static var quarter: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/quarter)
- [static var weekOfMonth: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/weekofmonth)
- [static var weekOfYear: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/weekofyear)
- [static var yearForWeekOfYear: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/yearforweekofyear)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfcalendarunit/init(rawvalue:))

#### Type Properties

- [static var dayOfYear: CFCalendarUnit](/documentation/corefoundation/cfcalendarunit/dayofyear)
- [Component Wrapping Options](/documentation/corefoundation/1533520-component-wrapping-options)

#### Constants

- [var kCFCalendarComponentsWrap: CFOptionFlags](/documentation/corefoundation/kcfcalendarcomponentswrap)
- [CFCharacterSet](/documentation/corefoundation/cfcharacterset)

### Creating Character Sets

- [func CFCharacterSetCreateCopy(CFAllocator!, CFCharacterSet!) -> CFCharacterSet!](/documentation/corefoundation/cfcharactersetcreatecopy(_:_:))
- [func CFCharacterSetCreateInvertedSet(CFAllocator!, CFCharacterSet!) -> CFCharacterSet!](/documentation/corefoundation/cfcharactersetcreateinvertedset(_:_:))
- [func CFCharacterSetCreateWithCharactersInRange(CFAllocator!, CFRange) -> CFCharacterSet!](/documentation/corefoundation/cfcharactersetcreatewithcharactersinrange(_:_:))
- [func CFCharacterSetCreateWithCharactersInString(CFAllocator!, CFString!) -> CFCharacterSet!](/documentation/corefoundation/cfcharactersetcreatewithcharactersinstring(_:_:))
- [func CFCharacterSetCreateWithBitmapRepresentation(CFAllocator!, CFData!) -> CFCharacterSet!](/documentation/corefoundation/cfcharactersetcreatewithbitmaprepresentation(_:_:))

### Getting Predefined Character Sets

- [func CFCharacterSetGetPredefined(CFCharacterSetPredefinedSet) -> CFCharacterSet!](/documentation/corefoundation/cfcharactersetgetpredefined(_:))

### Querying Character Sets

- [func CFCharacterSetCreateBitmapRepresentation(CFAllocator!, CFCharacterSet!) -> CFData!](/documentation/corefoundation/cfcharactersetcreatebitmaprepresentation(_:_:))
- [func CFCharacterSetHasMemberInPlane(CFCharacterSet!, CFIndex) -> Bool](/documentation/corefoundation/cfcharactersethasmemberinplane(_:_:))
- [func CFCharacterSetIsCharacterMember(CFCharacterSet!, UniChar) -> Bool](/documentation/corefoundation/cfcharactersetischaractermember(_:_:))
- [func CFCharacterSetIsLongCharacterMember(CFCharacterSet!, UTF32Char) -> Bool](/documentation/corefoundation/cfcharactersetislongcharactermember(_:_:))
- [func CFCharacterSetIsSupersetOfSet(CFCharacterSet!, CFCharacterSet!) -> Bool](/documentation/corefoundation/cfcharactersetissupersetofset(_:_:))

### Getting the Character Set Type Identifier

- [func CFCharacterSetGetTypeID() -> CFTypeID](/documentation/corefoundation/cfcharactersetgettypeid())

### Data Types

- [CFCharacterSetPredefinedSet](/documentation/corefoundation/cfcharactersetpredefinedset)

#### Enumeration Cases

- [case alphaNumeric](/documentation/corefoundation/cfcharactersetpredefinedset/alphanumeric)
- [case capitalizedLetter](/documentation/corefoundation/cfcharactersetpredefinedset/capitalizedletter)
- [case control](/documentation/corefoundation/cfcharactersetpredefinedset/control)
- [case decimalDigit](/documentation/corefoundation/cfcharactersetpredefinedset/decimaldigit)
- [case decomposable](/documentation/corefoundation/cfcharactersetpredefinedset/decomposable)
- [case illegal](/documentation/corefoundation/cfcharactersetpredefinedset/illegal)
- [case letter](/documentation/corefoundation/cfcharactersetpredefinedset/letter)
- [case lowercaseLetter](/documentation/corefoundation/cfcharactersetpredefinedset/lowercaseletter)
- [case newline](/documentation/corefoundation/cfcharactersetpredefinedset/newline)
- [case nonBase](/documentation/corefoundation/cfcharactersetpredefinedset/nonbase)
- [case punctuation](/documentation/corefoundation/cfcharactersetpredefinedset/punctuation)
- [case symbol](/documentation/corefoundation/cfcharactersetpredefinedset/symbol)
- [case uppercaseLetter](/documentation/corefoundation/cfcharactersetpredefinedset/uppercaseletter)
- [case whitespace](/documentation/corefoundation/cfcharactersetpredefinedset/whitespace)
- [case whitespaceAndNewline](/documentation/corefoundation/cfcharactersetpredefinedset/whitespaceandnewline)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfcharactersetpredefinedset/init(rawvalue:))

### Constants

- [Predefined CFCharacterSet Selector Values](/documentation/corefoundation/predefined_cfcharacterset_selector_values)

#### Constants

- [case control](/documentation/corefoundation/cfcharactersetpredefinedset/control)
- [case whitespace](/documentation/corefoundation/cfcharactersetpredefinedset/whitespace)
- [case whitespaceAndNewline](/documentation/corefoundation/cfcharactersetpredefinedset/whitespaceandnewline)
- [case decimalDigit](/documentation/corefoundation/cfcharactersetpredefinedset/decimaldigit)
- [case letter](/documentation/corefoundation/cfcharactersetpredefinedset/letter)
- [case lowercaseLetter](/documentation/corefoundation/cfcharactersetpredefinedset/lowercaseletter)
- [case uppercaseLetter](/documentation/corefoundation/cfcharactersetpredefinedset/uppercaseletter)
- [case nonBase](/documentation/corefoundation/cfcharactersetpredefinedset/nonbase)
- [case decomposable](/documentation/corefoundation/cfcharactersetpredefinedset/decomposable)
- [case alphaNumeric](/documentation/corefoundation/cfcharactersetpredefinedset/alphanumeric)
- [case punctuation](/documentation/corefoundation/cfcharactersetpredefinedset/punctuation)
- [case capitalizedLetter](/documentation/corefoundation/cfcharactersetpredefinedset/capitalizedletter)
- [case symbol](/documentation/corefoundation/cfcharactersetpredefinedset/symbol)
- [case newline](/documentation/corefoundation/cfcharactersetpredefinedset/newline)
- [case illegal](/documentation/corefoundation/cfcharactersetpredefinedset/illegal)
- [CFData](/documentation/corefoundation/cfdata)

### Creating a CFData Object

- [func CFDataCreate(CFAllocator!, UnsafePointer<UInt8>!, CFIndex) -> CFData!](/documentation/corefoundation/cfdatacreate(_:_:_:))
- [func CFDataCreateCopy(CFAllocator!, CFData!) -> CFData!](/documentation/corefoundation/cfdatacreatecopy(_:_:))
- [func CFDataCreateWithBytesNoCopy(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, CFAllocator!) -> CFData!](/documentation/corefoundation/cfdatacreatewithbytesnocopy(_:_:_:_:))

### Examining a CFData Object

- [func CFDataGetBytePtr(CFData!) -> UnsafePointer<UInt8>!](/documentation/corefoundation/cfdatagetbyteptr(_:))
- [func CFDataGetBytes(CFData!, CFRange, UnsafeMutablePointer<UInt8>!)](/documentation/corefoundation/cfdatagetbytes(_:_:_:))
- [func CFDataGetLength(CFData!) -> CFIndex](/documentation/corefoundation/cfdatagetlength(_:))
- [func CFDataFind(CFData!, CFData!, CFRange, CFDataSearchFlags) -> CFRange](/documentation/corefoundation/cfdatafind(_:_:_:_:))

### Getting the CFData Type ID

- [func CFDataGetTypeID() -> CFTypeID](/documentation/corefoundation/cfdatagettypeid())

### Data Types

- [CFDataSearchFlags](/documentation/corefoundation/cfdatasearchflags)

#### Constants

- [static var backwards: CFDataSearchFlags](/documentation/corefoundation/cfdatasearchflags/backwards)
- [static var anchored: CFDataSearchFlags](/documentation/corefoundation/cfdatasearchflags/anchored)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfdatasearchflags/init(rawvalue:))
- [CFDate](/documentation/corefoundation/cfdate)

### CFDate Miscellaneous Functions

- [func CFDateCompare(CFDate!, CFDate!, UnsafeMutableRawPointer!) -> CFComparisonResult](/documentation/corefoundation/cfdatecompare(_:_:_:))
- [func CFDateCreate(CFAllocator!, CFAbsoluteTime) -> CFDate!](/documentation/corefoundation/cfdatecreate(_:_:))
- [func CFDateGetAbsoluteTime(CFDate!) -> CFAbsoluteTime](/documentation/corefoundation/cfdategetabsolutetime(_:))
- [func CFDateGetTimeIntervalSinceDate(CFDate!, CFDate!) -> CFTimeInterval](/documentation/corefoundation/cfdategettimeintervalsincedate(_:_:))
- [func CFDateGetTypeID() -> CFTypeID](/documentation/corefoundation/cfdategettypeid())
- [CFDateFormatter](/documentation/corefoundation/cfdateformatter)

### Creating a Date Formatter

- [func CFDateFormatterCreate(CFAllocator!, CFLocale!, CFDateFormatterStyle, CFDateFormatterStyle) -> CFDateFormatter!](/documentation/corefoundation/cfdateformattercreate(_:_:_:_:))

### Configuring a Date Formatter

- [func CFDateFormatterSetFormat(CFDateFormatter!, CFString!)](/documentation/corefoundation/cfdateformattersetformat(_:_:))
- [func CFDateFormatterSetProperty(CFDateFormatter!, CFString!, CFTypeRef!)](/documentation/corefoundation/cfdateformattersetproperty(_:_:_:))

### Parsing Strings

- [func CFDateFormatterCreateDateFromString(CFAllocator!, CFDateFormatter!, CFString!, UnsafeMutablePointer<CFRange>!) -> CFDate!](/documentation/corefoundation/cfdateformattercreatedatefromstring(_:_:_:_:))
- [func CFDateFormatterGetAbsoluteTimeFromString(CFDateFormatter!, CFString!, UnsafeMutablePointer<CFRange>!, UnsafeMutablePointer<CFAbsoluteTime>!) -> Bool](/documentation/corefoundation/cfdateformattergetabsolutetimefromstring(_:_:_:_:))

### Creating Strings From Data

- [func CFDateFormatterCreateStringWithAbsoluteTime(CFAllocator!, CFDateFormatter!, CFAbsoluteTime) -> CFString!](/documentation/corefoundation/cfdateformattercreatestringwithabsolutetime(_:_:_:))
- [func CFDateFormatterCreateStringWithDate(CFAllocator!, CFDateFormatter!, CFDate!) -> CFString!](/documentation/corefoundation/cfdateformattercreatestringwithdate(_:_:_:))
- [func CFDateFormatterCreateDateFormatFromTemplate(CFAllocator!, CFString!, CFOptionFlags, CFLocale!) -> CFString!](/documentation/corefoundation/cfdateformattercreatedateformatfromtemplate(_:_:_:_:))

### Getting Information About a Date Formatter

- [func CFDateFormatterCopyProperty(CFDateFormatter!, CFDateFormatterKey!) -> CFTypeRef!](/documentation/corefoundation/cfdateformattercopyproperty(_:_:))
- [func CFDateFormatterGetDateStyle(CFDateFormatter!) -> CFDateFormatterStyle](/documentation/corefoundation/cfdateformattergetdatestyle(_:))
- [func CFDateFormatterGetFormat(CFDateFormatter!) -> CFString!](/documentation/corefoundation/cfdateformattergetformat(_:))
- [func CFDateFormatterGetLocale(CFDateFormatter!) -> CFLocale!](/documentation/corefoundation/cfdateformattergetlocale(_:))
- [func CFDateFormatterGetTimeStyle(CFDateFormatter!) -> CFDateFormatterStyle](/documentation/corefoundation/cfdateformattergettimestyle(_:))

### Getting the CFDateFormatter Type ID

- [func CFDateFormatterGetTypeID() -> CFTypeID](/documentation/corefoundation/cfdateformattergettypeid())

### Data Types

- [CFDateFormatterStyle](/documentation/corefoundation/cfdateformatterstyle)

#### Enumeration Cases

- [case fullStyle](/documentation/corefoundation/cfdateformatterstyle/fullstyle)
- [case longStyle](/documentation/corefoundation/cfdateformatterstyle/longstyle)
- [case mediumStyle](/documentation/corefoundation/cfdateformatterstyle/mediumstyle)
- [case noStyle](/documentation/corefoundation/cfdateformatterstyle/nostyle)
- [case shortStyle](/documentation/corefoundation/cfdateformatterstyle/shortstyle)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfdateformatterstyle/init(rawvalue:))

### Constants

- [Date Formatter Styles](/documentation/corefoundation/date_formatter_styles)

#### Constants

- [case noStyle](/documentation/corefoundation/cfdateformatterstyle/nostyle)
- [case shortStyle](/documentation/corefoundation/cfdateformatterstyle/shortstyle)
- [case mediumStyle](/documentation/corefoundation/cfdateformatterstyle/mediumstyle)
- [case longStyle](/documentation/corefoundation/cfdateformatterstyle/longstyle)
- [case fullStyle](/documentation/corefoundation/cfdateformatterstyle/fullstyle)
- [Date Formatter Property Keys](/documentation/corefoundation/date-formatter-property-keys)

#### Constants

- [static let isLenient: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/islenient)
- [static let timeZone: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/timezone)
- [static let calendarName: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/calendarname)
- [static let defaultFormat: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/defaultformat)
- [static let twoDigitStartDate: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/twodigitstartdate)
- [static let defaultDate: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/defaultdate)
- [static let calendar: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/calendar)
- [static let eraSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/erasymbols)
- [static let monthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/monthsymbols)
- [static let shortMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortmonthsymbols)
- [static let weekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/weekdaysymbols)
- [static let shortWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortweekdaysymbols)
- [static let amSymbol: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/amsymbol)
- [static let pmSymbol: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/pmsymbol)
- [static let longEraSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/longerasymbols)
- [static let veryShortMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortmonthsymbols)
- [static let standaloneMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/standalonemonthsymbols)
- [static let shortStandaloneMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortstandalonemonthsymbols)
- [static let veryShortStandaloneMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortstandalonemonthsymbols)
- [static let veryShortWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortweekdaysymbols)
- [static let standaloneWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/standaloneweekdaysymbols)
- [static let shortStandaloneWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortstandaloneweekdaysymbols)
- [static let veryShortStandaloneWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortstandaloneweekdaysymbols)
- [static let quarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/quartersymbols)
- [static let shortQuarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortquartersymbols)
- [static let standaloneQuarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/standalonequartersymbols)
- [static let shortStandaloneQuarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortstandalonequartersymbols)
- [static let gregorianStartDate: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/gregorianstartdate)
- [static let doesRelativeDateFormattingKey: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/doesrelativedateformattingkey)
- [Calendar Names](/documentation/corefoundation/calendar-names)

#### Constants

- [static let gregorianCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/gregoriancalendar)
- [CFDictionary](/documentation/corefoundation/cfdictionary)

### Creating a dictionary

- [func CFDictionaryCreate(CFAllocator!, UnsafeMutablePointer<UnsafeRawPointer?>!, UnsafeMutablePointer<UnsafeRawPointer?>!, CFIndex, UnsafePointer<CFDictionaryKeyCallBacks>!, UnsafePointer<CFDictionaryValueCallBacks>!) -> CFDictionary!](/documentation/corefoundation/cfdictionarycreate(_:_:_:_:_:_:))
- [func CFDictionaryCreateCopy(CFAllocator!, CFDictionary!) -> CFDictionary!](/documentation/corefoundation/cfdictionarycreatecopy(_:_:))

### Examining a dictionary

- [func CFDictionaryContainsKey(CFDictionary!, UnsafeRawPointer!) -> Bool](/documentation/corefoundation/cfdictionarycontainskey(_:_:))
- [func CFDictionaryContainsValue(CFDictionary!, UnsafeRawPointer!) -> Bool](/documentation/corefoundation/cfdictionarycontainsvalue(_:_:))
- [func CFDictionaryGetCount(CFDictionary!) -> CFIndex](/documentation/corefoundation/cfdictionarygetcount(_:))
- [func CFDictionaryGetCountOfKey(CFDictionary!, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfdictionarygetcountofkey(_:_:))
- [func CFDictionaryGetCountOfValue(CFDictionary!, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfdictionarygetcountofvalue(_:_:))
- [func CFDictionaryGetKeysAndValues(CFDictionary!, UnsafeMutablePointer<UnsafeRawPointer?>!, UnsafeMutablePointer<UnsafeRawPointer?>!)](/documentation/corefoundation/cfdictionarygetkeysandvalues(_:_:_:))
- [func CFDictionaryGetValue(CFDictionary!, UnsafeRawPointer!) -> UnsafeRawPointer!](/documentation/corefoundation/cfdictionarygetvalue(_:_:))
- [func CFDictionaryGetValueIfPresent(CFDictionary!, UnsafeRawPointer!, UnsafeMutablePointer<UnsafeRawPointer?>!) -> Bool](/documentation/corefoundation/cfdictionarygetvalueifpresent(_:_:_:))

### Applying a function to a dictionary

- [func CFDictionaryApplyFunction(CFDictionary!, ((UnsafeRawPointer?, UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void)!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cfdictionaryapplyfunction(_:_:_:))

### Getting the CFDictionary type ID

- [func CFDictionaryGetTypeID() -> CFTypeID](/documentation/corefoundation/cfdictionarygettypeid())

### Callbacks

- [CFDictionaryApplierFunction](/documentation/corefoundation/cfdictionaryapplierfunction)
- [CFDictionaryCopyDescriptionCallBack](/documentation/corefoundation/cfdictionarycopydescriptioncallback)
- [CFDictionaryEqualCallBack](/documentation/corefoundation/cfdictionaryequalcallback)
- [CFDictionaryHashCallBack](/documentation/corefoundation/cfdictionaryhashcallback)
- [CFDictionaryReleaseCallBack](/documentation/corefoundation/cfdictionaryreleasecallback)
- [CFDictionaryRetainCallBack](/documentation/corefoundation/cfdictionaryretaincallback)

### Data Types

- [CFDictionaryKeyCallBacks](/documentation/corefoundation/cfdictionarykeycallbacks)

#### Initializers

- [init()](/documentation/corefoundation/cfdictionarykeycallbacks/init())
- [init(version: CFIndex, retain: CFDictionaryRetainCallBack!, release: CFDictionaryReleaseCallBack!, copyDescription: CFDictionaryCopyDescriptionCallBack!, equal: CFDictionaryEqualCallBack!, hash: CFDictionaryHashCallBack!)](/documentation/corefoundation/cfdictionarykeycallbacks/init(version:retain:release:copydescription:equal:hash:))

#### Instance Properties

- [var copyDescription: CFDictionaryCopyDescriptionCallBack!](/documentation/corefoundation/cfdictionarykeycallbacks/copydescription)
- [var equal: CFDictionaryEqualCallBack!](/documentation/corefoundation/cfdictionarykeycallbacks/equal)
- [var hash: CFDictionaryHashCallBack!](/documentation/corefoundation/cfdictionarykeycallbacks/hash)
- [var release: CFDictionaryReleaseCallBack!](/documentation/corefoundation/cfdictionarykeycallbacks/release)
- [var retain: CFDictionaryRetainCallBack!](/documentation/corefoundation/cfdictionarykeycallbacks/retain)
- [var version: CFIndex](/documentation/corefoundation/cfdictionarykeycallbacks/version)
- [CFDictionaryValueCallBacks](/documentation/corefoundation/cfdictionaryvaluecallbacks)

#### Initializers

- [init()](/documentation/corefoundation/cfdictionaryvaluecallbacks/init())
- [init(version: CFIndex, retain: CFDictionaryRetainCallBack!, release: CFDictionaryReleaseCallBack!, copyDescription: CFDictionaryCopyDescriptionCallBack!, equal: CFDictionaryEqualCallBack!)](/documentation/corefoundation/cfdictionaryvaluecallbacks/init(version:retain:release:copydescription:equal:))

#### Instance Properties

- [var copyDescription: CFDictionaryCopyDescriptionCallBack!](/documentation/corefoundation/cfdictionaryvaluecallbacks/copydescription)
- [var equal: CFDictionaryEqualCallBack!](/documentation/corefoundation/cfdictionaryvaluecallbacks/equal)
- [var release: CFDictionaryReleaseCallBack!](/documentation/corefoundation/cfdictionaryvaluecallbacks/release)
- [var retain: CFDictionaryRetainCallBack!](/documentation/corefoundation/cfdictionaryvaluecallbacks/retain)
- [var version: CFIndex](/documentation/corefoundation/cfdictionaryvaluecallbacks/version)

### Constants

- [Predefined Callback Structures](/documentation/corefoundation/cfdictionary-predefined-callback-structures)

#### Constants

- [let kCFCopyStringDictionaryKeyCallBacks: CFDictionaryKeyCallBacks](/documentation/corefoundation/kcfcopystringdictionarykeycallbacks)
- [let kCFTypeDictionaryKeyCallBacks: CFDictionaryKeyCallBacks](/documentation/corefoundation/kcftypedictionarykeycallbacks)
- [let kCFTypeDictionaryValueCallBacks: CFDictionaryValueCallBacks](/documentation/corefoundation/kcftypedictionaryvaluecallbacks)
- [CFError](/documentation/corefoundation/cferror)

### Creating a CFError

- [func CFErrorCreate(CFAllocator!, CFErrorDomain!, CFIndex, CFDictionary!) -> CFError!](/documentation/corefoundation/cferrorcreate(_:_:_:_:))
- [func CFErrorCreateWithUserInfoKeysAndValues(CFAllocator!, CFErrorDomain!, CFIndex, UnsafePointer<UnsafeRawPointer?>!, UnsafePointer<UnsafeRawPointer?>!, CFIndex) -> CFError!](/documentation/corefoundation/cferrorcreatewithuserinfokeysandvalues(_:_:_:_:_:_:))

### Getting Information About an Error

- [func CFErrorGetDomain(CFError!) -> CFErrorDomain!](/documentation/corefoundation/cferrorgetdomain(_:))
- [func CFErrorGetCode(CFError!) -> CFIndex](/documentation/corefoundation/cferrorgetcode(_:))
- [func CFErrorCopyUserInfo(CFError!) -> CFDictionary!](/documentation/corefoundation/cferrorcopyuserinfo(_:))
- [func CFErrorCopyDescription(CFError!) -> CFString!](/documentation/corefoundation/cferrorcopydescription(_:))
- [func CFErrorCopyFailureReason(CFError!) -> CFString!](/documentation/corefoundation/cferrorcopyfailurereason(_:))
- [func CFErrorCopyRecoverySuggestion(CFError!) -> CFString!](/documentation/corefoundation/cferrorcopyrecoverysuggestion(_:))

### Getting the CFError Type ID

- [func CFErrorGetTypeID() -> CFTypeID](/documentation/corefoundation/cferrorgettypeid())

### Constants

- [Error domains](/documentation/corefoundation/error-domains)

#### Constants

- [let kCFErrorDomainPOSIX: CFErrorDomain!](/documentation/corefoundation/kcferrordomainposix)
- [let kCFErrorDomainOSStatus: CFErrorDomain!](/documentation/corefoundation/kcferrordomainosstatus)
- [let kCFErrorDomainMach: CFErrorDomain!](/documentation/corefoundation/kcferrordomainmach)
- [let kCFErrorDomainCocoa: CFErrorDomain!](/documentation/corefoundation/kcferrordomaincocoa)
- [Keys for the user info dictionary](/documentation/corefoundation/keys-for-the-user-info-dictionary)

#### Constants

- [let kCFErrorLocalizedDescriptionKey: CFString!](/documentation/corefoundation/kcferrorlocalizeddescriptionkey)
- [let kCFErrorLocalizedFailureReasonKey: CFString!](/documentation/corefoundation/kcferrorlocalizedfailurereasonkey)
- [let kCFErrorLocalizedRecoverySuggestionKey: CFString!](/documentation/corefoundation/kcferrorlocalizedrecoverysuggestionkey)
- [let kCFErrorDescriptionKey: CFString!](/documentation/corefoundation/kcferrordescriptionkey)
- [let kCFErrorUnderlyingErrorKey: CFString!](/documentation/corefoundation/kcferrorunderlyingerrorkey)
- [let kCFErrorURLKey: CFString!](/documentation/corefoundation/kcferrorurlkey)
- [let kCFErrorFilePathKey: CFString!](/documentation/corefoundation/kcferrorfilepathkey)
- [CFFileDescriptor](/documentation/corefoundation/cffiledescriptor)

### Creating a CFFileDescriptor

- [func CFFileDescriptorCreate(CFAllocator!, CFFileDescriptorNativeDescriptor, Bool, CFFileDescriptorCallBack!, UnsafePointer<CFFileDescriptorContext>!) -> CFFileDescriptor!](/documentation/corefoundation/cffiledescriptorcreate(_:_:_:_:_:))

### Getting Information About a File Descriptor

- [func CFFileDescriptorGetNativeDescriptor(CFFileDescriptor!) -> CFFileDescriptorNativeDescriptor](/documentation/corefoundation/cffiledescriptorgetnativedescriptor(_:))
- [func CFFileDescriptorIsValid(CFFileDescriptor!) -> Bool](/documentation/corefoundation/cffiledescriptorisvalid(_:))
- [func CFFileDescriptorGetContext(CFFileDescriptor!, UnsafeMutablePointer<CFFileDescriptorContext>!)](/documentation/corefoundation/cffiledescriptorgetcontext(_:_:))

### Invalidating a File Descriptor

- [func CFFileDescriptorInvalidate(CFFileDescriptor!)](/documentation/corefoundation/cffiledescriptorinvalidate(_:))

### Managing Callbacks

- [func CFFileDescriptorEnableCallBacks(CFFileDescriptor!, CFOptionFlags)](/documentation/corefoundation/cffiledescriptorenablecallbacks(_:_:))
- [func CFFileDescriptorDisableCallBacks(CFFileDescriptor!, CFOptionFlags)](/documentation/corefoundation/cffiledescriptordisablecallbacks(_:_:))

### Creating a Run Loop Source

- [func CFFileDescriptorCreateRunLoopSource(CFAllocator!, CFFileDescriptor!, CFIndex) -> CFRunLoopSource!](/documentation/corefoundation/cffiledescriptorcreaterunloopsource(_:_:_:))

### Getting the CFFileDescriptor Type ID

- [func CFFileDescriptorGetTypeID() -> CFTypeID](/documentation/corefoundation/cffiledescriptorgettypeid())

### Data Types

- [CFFileDescriptorNativeDescriptor](/documentation/corefoundation/cffiledescriptornativedescriptor)
- [CFFileDescriptorCallBack](/documentation/corefoundation/cffiledescriptorcallback)
- [CFFileDescriptorContext](/documentation/corefoundation/cffiledescriptorcontext)

#### Initializers

- [init()](/documentation/corefoundation/cffiledescriptorcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!, release: ((UnsafeMutableRawPointer?) -> Void)!, copyDescription: ((UnsafeMutableRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cffiledescriptorcontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeMutableRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cffiledescriptorcontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cffiledescriptorcontext/info)
- [var release: ((UnsafeMutableRawPointer?) -> Void)!](/documentation/corefoundation/cffiledescriptorcontext/release)
- [var retain: ((UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!](/documentation/corefoundation/cffiledescriptorcontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cffiledescriptorcontext/version)

### Constants

- [Callback Identifiers](/documentation/corefoundation/1477595-callback-identifiers)

#### Constants

- [var kCFFileDescriptorReadCallBack: CFOptionFlags](/documentation/corefoundation/kcffiledescriptorreadcallback)
- [var kCFFileDescriptorWriteCallBack: CFOptionFlags](/documentation/corefoundation/kcffiledescriptorwritecallback)
- [CFFileSecurity](/documentation/corefoundation/cffilesecurity)
- [CFLocale](/documentation/corefoundation/cflocale)

### Creating a Locale

- [func CFLocaleCopyCurrent() -> CFLocale!](/documentation/corefoundation/cflocalecopycurrent())
- [func CFLocaleCreate(CFAllocator!, CFLocaleIdentifier!) -> CFLocale!](/documentation/corefoundation/cflocalecreate(_:_:))
- [func CFLocaleCreateCopy(CFAllocator!, CFLocale!) -> CFLocale!](/documentation/corefoundation/cflocalecreatecopy(_:_:))
- [func CFLocaleGetSystem() -> CFLocale!](/documentation/corefoundation/cflocalegetsystem())

### Getting System Locale Information

- [func CFLocaleCopyAvailableLocaleIdentifiers() -> CFArray!](/documentation/corefoundation/cflocalecopyavailablelocaleidentifiers())

### Getting ISO Information

- [func CFLocaleCopyISOCountryCodes() -> CFArray!](/documentation/corefoundation/cflocalecopyisocountrycodes())
- [func CFLocaleCopyISOLanguageCodes() -> CFArray!](/documentation/corefoundation/cflocalecopyisolanguagecodes())
- [func CFLocaleCopyISOCurrencyCodes() -> CFArray!](/documentation/corefoundation/cflocalecopyisocurrencycodes())
- [func CFLocaleCopyCommonISOCurrencyCodes() -> CFArray!](/documentation/corefoundation/cflocalecopycommonisocurrencycodes())

### Language Preferences

- [func CFLocaleCopyPreferredLanguages() -> CFArray!](/documentation/corefoundation/cflocalecopypreferredlanguages())

### Getting Information About a Locale

- [func CFLocaleCopyDisplayNameForPropertyValue(CFLocale!, CFLocaleKey!, CFString!) -> CFString!](/documentation/corefoundation/cflocalecopydisplaynameforpropertyvalue(_:_:_:))
- [func CFLocaleGetValue(CFLocale!, CFLocaleKey!) -> CFTypeRef!](/documentation/corefoundation/cflocalegetvalue(_:_:))
- [func CFLocaleGetIdentifier(CFLocale!) -> CFLocaleIdentifier!](/documentation/corefoundation/cflocalegetidentifier(_:))

### Getting and Creating Locale Identifiers

- [func CFLocaleCreateCanonicalLocaleIdentifierFromScriptManagerCodes(CFAllocator!, LangCode, RegionCode) -> CFLocaleIdentifier!](/documentation/corefoundation/cflocalecreatecanonicallocaleidentifierfromscriptmanagercodes(_:_:_:))
- [func CFLocaleCreateCanonicalLanguageIdentifierFromString(CFAllocator!, CFString!) -> CFLocaleIdentifier!](/documentation/corefoundation/cflocalecreatecanonicallanguageidentifierfromstring(_:_:))
- [func CFLocaleCreateCanonicalLocaleIdentifierFromString(CFAllocator!, CFString!) -> CFLocaleIdentifier!](/documentation/corefoundation/cflocalecreatecanonicallocaleidentifierfromstring(_:_:))
- [func CFLocaleCreateComponentsFromLocaleIdentifier(CFAllocator!, CFLocaleIdentifier!) -> CFDictionary!](/documentation/corefoundation/cflocalecreatecomponentsfromlocaleidentifier(_:_:))
- [func CFLocaleCreateLocaleIdentifierFromComponents(CFAllocator!, CFDictionary!) -> CFLocaleIdentifier!](/documentation/corefoundation/cflocalecreatelocaleidentifierfromcomponents(_:_:))
- [func CFLocaleCreateLocaleIdentifierFromWindowsLocaleCode(CFAllocator!, UInt32) -> CFLocaleIdentifier!](/documentation/corefoundation/cflocalecreatelocaleidentifierfromwindowslocalecode(_:_:))
- [func CFLocaleGetWindowsLocaleCodeFromLocaleIdentifier(CFLocaleIdentifier!) -> UInt32](/documentation/corefoundation/cflocalegetwindowslocalecodefromlocaleidentifier(_:))

### Getting Line and Character Direction for a Language

- [func CFLocaleGetLanguageCharacterDirection(CFString!) -> CFLocaleLanguageDirection](/documentation/corefoundation/cflocalegetlanguagecharacterdirection(_:))
- [func CFLocaleGetLanguageLineDirection(CFString!) -> CFLocaleLanguageDirection](/documentation/corefoundation/cflocalegetlanguagelinedirection(_:))

### Getting the CFLocale Type ID

- [func CFLocaleGetTypeID() -> CFTypeID](/documentation/corefoundation/cflocalegettypeid())

### Constants

- [CFLocaleLanguageDirection](/documentation/corefoundation/cflocalelanguagedirection)

#### Constants

- [case unknown](/documentation/corefoundation/cflocalelanguagedirection/unknown)
- [case leftToRight](/documentation/corefoundation/cflocalelanguagedirection/lefttoright)
- [case rightToLeft](/documentation/corefoundation/cflocalelanguagedirection/righttoleft)
- [case topToBottom](/documentation/corefoundation/cflocalelanguagedirection/toptobottom)
- [case bottomToTop](/documentation/corefoundation/cflocalelanguagedirection/bottomtotop)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cflocalelanguagedirection/init(rawvalue:))
- [Locale Property Keys](/documentation/corefoundation/locale-property-keys)

#### Constants

- [static let identifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/identifier)
- [static let languageCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/languagecode)
- [static let countryCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/countrycode)
- [static let scriptCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/scriptcode)
- [static let variantCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/variantcode)
- [static let exemplarCharacterSet: CFLocaleKey!](/documentation/corefoundation/cflocalekey/exemplarcharacterset)
- [static let calendarIdentifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/calendaridentifier)
- [static let calendar: CFLocaleKey!](/documentation/corefoundation/cflocalekey/calendar)
- [static let collationIdentifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/collationidentifier)
- [static let usesMetricSystem: CFLocaleKey!](/documentation/corefoundation/cflocalekey/usesmetricsystem)
- [static let measurementSystem: CFLocaleKey!](/documentation/corefoundation/cflocalekey/measurementsystem)
- [static let decimalSeparator: CFLocaleKey!](/documentation/corefoundation/cflocalekey/decimalseparator)
- [static let groupingSeparator: CFLocaleKey!](/documentation/corefoundation/cflocalekey/groupingseparator)
- [static let currencySymbol: CFLocaleKey!](/documentation/corefoundation/cflocalekey/currencysymbol)
- [static let currencyCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/currencycode)
- [static let collatorIdentifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/collatoridentifier)
- [static let quotationBeginDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/quotationbegindelimiterkey)
- [static let quotationEndDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/quotationenddelimiterkey)
- [static let alternateQuotationBeginDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/alternatequotationbegindelimiterkey)
- [static let alternateQuotationEndDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/alternatequotationenddelimiterkey)
- [Locale Calendar Identifiers](/documentation/corefoundation/locale-calendar-identifiers)

#### Constants

- [static let gregorianCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/gregoriancalendar)
- [static let buddhistCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/buddhistcalendar)
- [static let chineseCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/chinesecalendar)
- [static let hebrewCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/hebrewcalendar)
- [static let islamicCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamiccalendar)
- [static let islamicCivilCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamiccivilcalendar)
- [static let islamicTabularCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamictabularcalendar)
- [static let islamicUmmAlQuraCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamicummalquracalendar)
- [static let japaneseCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/japanesecalendar)
- [static let republicOfChinaCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/republicofchinacalendar)
- [static let persianCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/persiancalendar)
- [static let indianCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/indiancalendar)
- [static let cfiso8601Calendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/cfiso8601calendar)
- [Locale Change Notification](/documentation/corefoundation/locale-change-notification)

#### Constants

- [static let cfLocaleCurrentLocaleDidChange: CFNotificationName!](/documentation/corefoundation/cfnotificationname/cflocalecurrentlocaledidchange)
- [CFMachPort](/documentation/corefoundation/cfmachport)

### Creating a CFMachPort Object

- [func CFMachPortCreate(CFAllocator!, CFMachPortCallBack!, UnsafeMutablePointer<CFMachPortContext>!, UnsafeMutablePointer<DarwinBoolean>!) -> CFMachPort!](/documentation/corefoundation/cfmachportcreate(_:_:_:_:))
- [func CFMachPortCreateWithPort(CFAllocator!, mach_port_t, CFMachPortCallBack!, UnsafeMutablePointer<CFMachPortContext>!, UnsafeMutablePointer<DarwinBoolean>!) -> CFMachPort!](/documentation/corefoundation/cfmachportcreatewithport(_:_:_:_:_:))

### Configuring a CFMachPort Object

- [func CFMachPortInvalidate(CFMachPort!)](/documentation/corefoundation/cfmachportinvalidate(_:))
- [func CFMachPortCreateRunLoopSource(CFAllocator!, CFMachPort!, CFIndex) -> CFRunLoopSource!](/documentation/corefoundation/cfmachportcreaterunloopsource(_:_:_:))
- [func CFMachPortSetInvalidationCallBack(CFMachPort!, CFMachPortInvalidationCallBack!)](/documentation/corefoundation/cfmachportsetinvalidationcallback(_:_:))

### Examining a CFMachPort Object

- [func CFMachPortGetContext(CFMachPort!, UnsafeMutablePointer<CFMachPortContext>!)](/documentation/corefoundation/cfmachportgetcontext(_:_:))
- [func CFMachPortGetInvalidationCallBack(CFMachPort!) -> CFMachPortInvalidationCallBack!](/documentation/corefoundation/cfmachportgetinvalidationcallback(_:))
- [func CFMachPortGetPort(CFMachPort!) -> mach_port_t](/documentation/corefoundation/cfmachportgetport(_:))
- [func CFMachPortIsValid(CFMachPort!) -> Bool](/documentation/corefoundation/cfmachportisvalid(_:))

### Getting the CFMachPort Type ID

- [func CFMachPortGetTypeID() -> CFTypeID](/documentation/corefoundation/cfmachportgettypeid())

### Callbacks

- [CFMachPortCallBack](/documentation/corefoundation/cfmachportcallback)
- [CFMachPortInvalidationCallBack](/documentation/corefoundation/cfmachportinvalidationcallback)

### Data Types

- [CFMachPortContext](/documentation/corefoundation/cfmachportcontext)

#### Initializers

- [init()](/documentation/corefoundation/cfmachportcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfmachportcontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfmachportcontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfmachportcontext/info)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfmachportcontext/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfmachportcontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfmachportcontext/version)
- [CFMessagePort](/documentation/corefoundation/cfmessageport)

### Creating a CFMessagePort Object

- [func CFMessagePortCreateLocal(CFAllocator!, CFString!, CFMessagePortCallBack!, UnsafeMutablePointer<CFMessagePortContext>!, UnsafeMutablePointer<DarwinBoolean>!) -> CFMessagePort!](/documentation/corefoundation/cfmessageportcreatelocal(_:_:_:_:_:))
- [func CFMessagePortCreateRemote(CFAllocator!, CFString!) -> CFMessagePort!](/documentation/corefoundation/cfmessageportcreateremote(_:_:))

### Configuring a CFMessagePort Object

- [func CFMessagePortCreateRunLoopSource(CFAllocator!, CFMessagePort!, CFIndex) -> CFRunLoopSource!](/documentation/corefoundation/cfmessageportcreaterunloopsource(_:_:_:))
- [func CFMessagePortSetInvalidationCallBack(CFMessagePort!, CFMessagePortInvalidationCallBack!)](/documentation/corefoundation/cfmessageportsetinvalidationcallback(_:_:))
- [func CFMessagePortSetName(CFMessagePort!, CFString!) -> Bool](/documentation/corefoundation/cfmessageportsetname(_:_:))

### Using a Message Port

- [func CFMessagePortInvalidate(CFMessagePort!)](/documentation/corefoundation/cfmessageportinvalidate(_:))
- [func CFMessagePortSendRequest(CFMessagePort!, Int32, CFData!, CFTimeInterval, CFTimeInterval, CFString!, UnsafeMutablePointer<Unmanaged<CFData>?>!) -> Int32](/documentation/corefoundation/cfmessageportsendrequest(_:_:_:_:_:_:_:))
- [func CFMessagePortSetDispatchQueue(CFMessagePort!, dispatch_queue_t!)](/documentation/corefoundation/cfmessageportsetdispatchqueue(_:_:))

### Examining a Message Port

- [func CFMessagePortGetContext(CFMessagePort!, UnsafeMutablePointer<CFMessagePortContext>!)](/documentation/corefoundation/cfmessageportgetcontext(_:_:))
- [func CFMessagePortGetInvalidationCallBack(CFMessagePort!) -> CFMessagePortInvalidationCallBack!](/documentation/corefoundation/cfmessageportgetinvalidationcallback(_:))
- [func CFMessagePortGetName(CFMessagePort!) -> CFString!](/documentation/corefoundation/cfmessageportgetname(_:))
- [func CFMessagePortIsRemote(CFMessagePort!) -> Bool](/documentation/corefoundation/cfmessageportisremote(_:))
- [func CFMessagePortIsValid(CFMessagePort!) -> Bool](/documentation/corefoundation/cfmessageportisvalid(_:))

### Getting the CFMessagePort Type ID

- [func CFMessagePortGetTypeID() -> CFTypeID](/documentation/corefoundation/cfmessageportgettypeid())

### Callbacks

- [CFMessagePortCallBack](/documentation/corefoundation/cfmessageportcallback)
- [CFMessagePortInvalidationCallBack](/documentation/corefoundation/cfmessageportinvalidationcallback)

### Data Types

- [CFMessagePortContext](/documentation/corefoundation/cfmessageportcontext)

#### Initializers

- [init()](/documentation/corefoundation/cfmessageportcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfmessageportcontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfmessageportcontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfmessageportcontext/info)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfmessageportcontext/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfmessageportcontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfmessageportcontext/version)

### Constants

- [CFMessagePortSendRequest Error Codes](/documentation/corefoundation/1561514-cfmessageportsendrequest-error-c)

#### Constants

- [var kCFMessagePortSuccess: Int32](/documentation/corefoundation/kcfmessageportsuccess)
- [var kCFMessagePortSendTimeout: Int32](/documentation/corefoundation/kcfmessageportsendtimeout)
- [var kCFMessagePortReceiveTimeout: Int32](/documentation/corefoundation/kcfmessageportreceivetimeout)
- [var kCFMessagePortIsInvalid: Int32](/documentation/corefoundation/kcfmessageportisinvalid)
- [var kCFMessagePortTransportError: Int32](/documentation/corefoundation/kcfmessageporttransporterror)
- [var kCFMessagePortBecameInvalidError: Int32](/documentation/corefoundation/kcfmessageportbecameinvaliderror)
- [CFMutableArray](/documentation/corefoundation/cfmutablearray)

### CFMutableArray Miscellaneous Functions

- [func CFArrayAppendArray(CFMutableArray!, CFArray!, CFRange)](/documentation/corefoundation/cfarrayappendarray(_:_:_:))
- [func CFArrayAppendValue(CFMutableArray!, UnsafeRawPointer!)](/documentation/corefoundation/cfarrayappendvalue(_:_:))
- [func CFArrayCreateMutable(CFAllocator!, CFIndex, UnsafePointer<CFArrayCallBacks>!) -> CFMutableArray!](/documentation/corefoundation/cfarraycreatemutable(_:_:_:))
- [func CFArrayCreateMutableCopy(CFAllocator!, CFIndex, CFArray!) -> CFMutableArray!](/documentation/corefoundation/cfarraycreatemutablecopy(_:_:_:))
- [func CFArrayExchangeValuesAtIndices(CFMutableArray!, CFIndex, CFIndex)](/documentation/corefoundation/cfarrayexchangevaluesatindices(_:_:_:))
- [func CFArrayInsertValueAtIndex(CFMutableArray!, CFIndex, UnsafeRawPointer!)](/documentation/corefoundation/cfarrayinsertvalueatindex(_:_:_:))
- [func CFArrayRemoveAllValues(CFMutableArray!)](/documentation/corefoundation/cfarrayremoveallvalues(_:))
- [func CFArrayRemoveValueAtIndex(CFMutableArray!, CFIndex)](/documentation/corefoundation/cfarrayremovevalueatindex(_:_:))
- [func CFArrayReplaceValues(CFMutableArray!, CFRange, UnsafeMutablePointer<UnsafeRawPointer?>!, CFIndex)](/documentation/corefoundation/cfarrayreplacevalues(_:_:_:_:))
- [func CFArraySetValueAtIndex(CFMutableArray!, CFIndex, UnsafeRawPointer!)](/documentation/corefoundation/cfarraysetvalueatindex(_:_:_:))
- [func CFArraySortValues(CFMutableArray!, CFRange, CFComparatorFunction!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cfarraysortvalues(_:_:_:_:))
- [CFMutableAttributedString](/documentation/corefoundation/cfmutableattributedstring)

### Creating a CFMutableAttributedString

- [func CFAttributedStringCreateMutable(CFAllocator!, CFIndex) -> CFMutableAttributedString!](/documentation/corefoundation/cfattributedstringcreatemutable(_:_:))
- [func CFAttributedStringCreateMutableCopy(CFAllocator!, CFIndex, CFAttributedString!) -> CFMutableAttributedString!](/documentation/corefoundation/cfattributedstringcreatemutablecopy(_:_:_:))

### Modifying a CFMutableAttributedString

- [func CFAttributedStringBeginEditing(CFMutableAttributedString!)](/documentation/corefoundation/cfattributedstringbeginediting(_:))
- [func CFAttributedStringEndEditing(CFMutableAttributedString!)](/documentation/corefoundation/cfattributedstringendediting(_:))
- [func CFAttributedStringGetMutableString(CFMutableAttributedString!) -> CFMutableString!](/documentation/corefoundation/cfattributedstringgetmutablestring(_:))
- [func CFAttributedStringRemoveAttribute(CFMutableAttributedString!, CFRange, CFString!)](/documentation/corefoundation/cfattributedstringremoveattribute(_:_:_:))
- [func CFAttributedStringReplaceString(CFMutableAttributedString!, CFRange, CFString!)](/documentation/corefoundation/cfattributedstringreplacestring(_:_:_:))
- [func CFAttributedStringReplaceAttributedString(CFMutableAttributedString!, CFRange, CFAttributedString!)](/documentation/corefoundation/cfattributedstringreplaceattributedstring(_:_:_:))
- [func CFAttributedStringSetAttribute(CFMutableAttributedString!, CFRange, CFString!, CFTypeRef!)](/documentation/corefoundation/cfattributedstringsetattribute(_:_:_:_:))
- [func CFAttributedStringSetAttributes(CFMutableAttributedString!, CFRange, CFDictionary!, Bool)](/documentation/corefoundation/cfattributedstringsetattributes(_:_:_:_:))
- [CFMutableBag](/documentation/corefoundation/cfmutablebag)

### Creating a Mutable Bag

- [func CFBagCreateMutable(CFAllocator!, CFIndex, UnsafePointer<CFBagCallBacks>!) -> CFMutableBag!](/documentation/corefoundation/cfbagcreatemutable(_:_:_:))
- [func CFBagCreateMutableCopy(CFAllocator!, CFIndex, CFBag!) -> CFMutableBag!](/documentation/corefoundation/cfbagcreatemutablecopy(_:_:_:))

### Modifying a Mutable Bag

- [func CFBagAddValue(CFMutableBag!, UnsafeRawPointer!)](/documentation/corefoundation/cfbagaddvalue(_:_:))
- [func CFBagRemoveAllValues(CFMutableBag!)](/documentation/corefoundation/cfbagremoveallvalues(_:))
- [func CFBagRemoveValue(CFMutableBag!, UnsafeRawPointer!)](/documentation/corefoundation/cfbagremovevalue(_:_:))
- [func CFBagReplaceValue(CFMutableBag!, UnsafeRawPointer!)](/documentation/corefoundation/cfbagreplacevalue(_:_:))
- [func CFBagSetValue(CFMutableBag!, UnsafeRawPointer!)](/documentation/corefoundation/cfbagsetvalue(_:_:))
- [CFMutableBitVector](/documentation/corefoundation/cfmutablebitvector)

### Creating a CFMutableBitVector Object

- [func CFBitVectorCreateMutable(CFAllocator!, CFIndex) -> CFMutableBitVector!](/documentation/corefoundation/cfbitvectorcreatemutable(_:_:))
- [func CFBitVectorCreateMutableCopy(CFAllocator!, CFIndex, CFBitVector!) -> CFMutableBitVector!](/documentation/corefoundation/cfbitvectorcreatemutablecopy(_:_:_:))

### Modifying a Bit Vector

- [func CFBitVectorFlipBitAtIndex(CFMutableBitVector!, CFIndex)](/documentation/corefoundation/cfbitvectorflipbitatindex(_:_:))
- [func CFBitVectorFlipBits(CFMutableBitVector!, CFRange)](/documentation/corefoundation/cfbitvectorflipbits(_:_:))
- [func CFBitVectorSetAllBits(CFMutableBitVector!, CFBit)](/documentation/corefoundation/cfbitvectorsetallbits(_:_:))
- [func CFBitVectorSetBitAtIndex(CFMutableBitVector!, CFIndex, CFBit)](/documentation/corefoundation/cfbitvectorsetbitatindex(_:_:_:))
- [func CFBitVectorSetBits(CFMutableBitVector!, CFRange, CFBit)](/documentation/corefoundation/cfbitvectorsetbits(_:_:_:))
- [func CFBitVectorSetCount(CFMutableBitVector!, CFIndex)](/documentation/corefoundation/cfbitvectorsetcount(_:_:))
- [CFMutableCharacterSet](/documentation/corefoundation/cfmutablecharacterset)

### Creating a Mutable Character Set

- [func CFCharacterSetCreateMutable(CFAllocator!) -> CFMutableCharacterSet!](/documentation/corefoundation/cfcharactersetcreatemutable(_:))
- [func CFCharacterSetCreateMutableCopy(CFAllocator!, CFCharacterSet!) -> CFMutableCharacterSet!](/documentation/corefoundation/cfcharactersetcreatemutablecopy(_:_:))

### Adding Characters

- [func CFCharacterSetAddCharactersInRange(CFMutableCharacterSet!, CFRange)](/documentation/corefoundation/cfcharactersetaddcharactersinrange(_:_:))
- [func CFCharacterSetAddCharactersInString(CFMutableCharacterSet!, CFString!)](/documentation/corefoundation/cfcharactersetaddcharactersinstring(_:_:))

### Removing Characters

- [func CFCharacterSetRemoveCharactersInRange(CFMutableCharacterSet!, CFRange)](/documentation/corefoundation/cfcharactersetremovecharactersinrange(_:_:))
- [func CFCharacterSetRemoveCharactersInString(CFMutableCharacterSet!, CFString!)](/documentation/corefoundation/cfcharactersetremovecharactersinstring(_:_:))

### Logical Operations

- [func CFCharacterSetIntersect(CFMutableCharacterSet!, CFCharacterSet!)](/documentation/corefoundation/cfcharactersetintersect(_:_:))
- [func CFCharacterSetInvert(CFMutableCharacterSet!)](/documentation/corefoundation/cfcharactersetinvert(_:))
- [func CFCharacterSetUnion(CFMutableCharacterSet!, CFCharacterSet!)](/documentation/corefoundation/cfcharactersetunion(_:_:))
- [CFMutableData](/documentation/corefoundation/cfmutabledata)

### Creating a Mutable Data Object

- [func CFDataCreateMutable(CFAllocator!, CFIndex) -> CFMutableData!](/documentation/corefoundation/cfdatacreatemutable(_:_:))
- [func CFDataCreateMutableCopy(CFAllocator!, CFIndex, CFData!) -> CFMutableData!](/documentation/corefoundation/cfdatacreatemutablecopy(_:_:_:))

### Accessing Data

- [func CFDataGetMutableBytePtr(CFMutableData!) -> UnsafeMutablePointer<UInt8>!](/documentation/corefoundation/cfdatagetmutablebyteptr(_:))

### Modifying a Mutable Data Object

- [func CFDataAppendBytes(CFMutableData!, UnsafePointer<UInt8>!, CFIndex)](/documentation/corefoundation/cfdataappendbytes(_:_:_:))
- [func CFDataDeleteBytes(CFMutableData!, CFRange)](/documentation/corefoundation/cfdatadeletebytes(_:_:))
- [func CFDataReplaceBytes(CFMutableData!, CFRange, UnsafePointer<UInt8>!, CFIndex)](/documentation/corefoundation/cfdatareplacebytes(_:_:_:_:))
- [func CFDataIncreaseLength(CFMutableData!, CFIndex)](/documentation/corefoundation/cfdataincreaselength(_:_:))
- [func CFDataSetLength(CFMutableData!, CFIndex)](/documentation/corefoundation/cfdatasetlength(_:_:))
- [CFMutableDictionary](/documentation/corefoundation/cfmutabledictionary)

### Creating a Mutable Dictionary

- [func CFDictionaryCreateMutable(CFAllocator!, CFIndex, UnsafePointer<CFDictionaryKeyCallBacks>!, UnsafePointer<CFDictionaryValueCallBacks>!) -> CFMutableDictionary!](/documentation/corefoundation/cfdictionarycreatemutable(_:_:_:_:))
- [func CFDictionaryCreateMutableCopy(CFAllocator!, CFIndex, CFDictionary!) -> CFMutableDictionary!](/documentation/corefoundation/cfdictionarycreatemutablecopy(_:_:_:))

### Modifying a Dictionary

- [func CFDictionaryAddValue(CFMutableDictionary!, UnsafeRawPointer!, UnsafeRawPointer!)](/documentation/corefoundation/cfdictionaryaddvalue(_:_:_:))
- [func CFDictionaryRemoveAllValues(CFMutableDictionary!)](/documentation/corefoundation/cfdictionaryremoveallvalues(_:))
- [func CFDictionaryRemoveValue(CFMutableDictionary!, UnsafeRawPointer!)](/documentation/corefoundation/cfdictionaryremovevalue(_:_:))
- [func CFDictionaryReplaceValue(CFMutableDictionary!, UnsafeRawPointer!, UnsafeRawPointer!)](/documentation/corefoundation/cfdictionaryreplacevalue(_:_:_:))
- [func CFDictionarySetValue(CFMutableDictionary!, UnsafeRawPointer!, UnsafeRawPointer!)](/documentation/corefoundation/cfdictionarysetvalue(_:_:_:))
- [CFMutableSet](/documentation/corefoundation/cfmutableset)

### CFMutableSet Miscellaneous Functions

- [func CFSetAddValue(CFMutableSet!, UnsafeRawPointer!)](/documentation/corefoundation/cfsetaddvalue(_:_:))
- [func CFSetCreateMutable(CFAllocator!, CFIndex, UnsafePointer<CFSetCallBacks>!) -> CFMutableSet!](/documentation/corefoundation/cfsetcreatemutable(_:_:_:))
- [func CFSetCreateMutableCopy(CFAllocator!, CFIndex, CFSet!) -> CFMutableSet!](/documentation/corefoundation/cfsetcreatemutablecopy(_:_:_:))
- [func CFSetRemoveAllValues(CFMutableSet!)](/documentation/corefoundation/cfsetremoveallvalues(_:))
- [func CFSetRemoveValue(CFMutableSet!, UnsafeRawPointer!)](/documentation/corefoundation/cfsetremovevalue(_:_:))
- [func CFSetReplaceValue(CFMutableSet!, UnsafeRawPointer!)](/documentation/corefoundation/cfsetreplacevalue(_:_:))
- [func CFSetSetValue(CFMutableSet!, UnsafeRawPointer!)](/documentation/corefoundation/cfsetsetvalue(_:_:))
- [CFMutableString](/documentation/corefoundation/cfmutablestring)

### CFMutableString Miscellaneous Functions

- [func CFStringAppend(CFMutableString!, CFString!)](/documentation/corefoundation/cfstringappend(_:_:))
- [func CFStringAppendCharacters(CFMutableString!, UnsafePointer<UniChar>!, CFIndex)](/documentation/corefoundation/cfstringappendcharacters(_:_:_:))
- [func CFStringAppendCString(CFMutableString!, UnsafePointer<CChar>!, CFStringEncoding)](/documentation/corefoundation/cfstringappendcstring(_:_:_:))
- [func CFStringAppendFormatAndArguments(CFMutableString!, CFDictionary!, CFString!, CVaListPointer)](/documentation/corefoundation/cfstringappendformatandarguments(_:_:_:_:))
- [func CFStringAppendPascalString(CFMutableString!, ConstStr255Param!, CFStringEncoding)](/documentation/corefoundation/cfstringappendpascalstring(_:_:_:))
- [func CFStringCapitalize(CFMutableString!, CFLocale!)](/documentation/corefoundation/cfstringcapitalize(_:_:))
- [func CFStringCreateMutable(CFAllocator!, CFIndex) -> CFMutableString!](/documentation/corefoundation/cfstringcreatemutable(_:_:))
- [func CFStringCreateMutableCopy(CFAllocator!, CFIndex, CFString!) -> CFMutableString!](/documentation/corefoundation/cfstringcreatemutablecopy(_:_:_:))
- [func CFStringCreateMutableWithExternalCharactersNoCopy(CFAllocator!, UnsafeMutablePointer<UniChar>!, CFIndex, CFIndex, CFAllocator!) -> CFMutableString!](/documentation/corefoundation/cfstringcreatemutablewithexternalcharactersnocopy(_:_:_:_:_:))
- [func CFStringDelete(CFMutableString!, CFRange)](/documentation/corefoundation/cfstringdelete(_:_:))
- [func CFStringFindAndReplace(CFMutableString!, CFString!, CFString!, CFRange, CFStringCompareFlags) -> CFIndex](/documentation/corefoundation/cfstringfindandreplace(_:_:_:_:_:))
- [func CFStringFold(CFMutableString!, CFStringCompareFlags, CFLocale!)](/documentation/corefoundation/cfstringfold(_:_:_:))
- [func CFStringInsert(CFMutableString!, CFIndex, CFString!)](/documentation/corefoundation/cfstringinsert(_:_:_:))
- [func CFStringLowercase(CFMutableString!, CFLocale!)](/documentation/corefoundation/cfstringlowercase(_:_:))
- [func CFStringNormalize(CFMutableString!, CFStringNormalizationForm)](/documentation/corefoundation/cfstringnormalize(_:_:))
- [func CFStringPad(CFMutableString!, CFString!, CFIndex, CFIndex)](/documentation/corefoundation/cfstringpad(_:_:_:_:))
- [func CFStringReplace(CFMutableString!, CFRange, CFString!)](/documentation/corefoundation/cfstringreplace(_:_:_:))
- [func CFStringReplaceAll(CFMutableString!, CFString!)](/documentation/corefoundation/cfstringreplaceall(_:_:))
- [func CFStringSetExternalCharactersNoCopy(CFMutableString!, UnsafeMutablePointer<UniChar>!, CFIndex, CFIndex)](/documentation/corefoundation/cfstringsetexternalcharactersnocopy(_:_:_:_:))
- [func CFStringTransform(CFMutableString!, UnsafeMutablePointer<CFRange>!, CFString!, Bool) -> Bool](/documentation/corefoundation/cfstringtransform(_:_:_:_:))
- [func CFStringTrim(CFMutableString!, CFString!)](/documentation/corefoundation/cfstringtrim(_:_:))
- [func CFStringTrimWhitespace(CFMutableString!)](/documentation/corefoundation/cfstringtrimwhitespace(_:))
- [func CFStringUppercase(CFMutableString!, CFLocale!)](/documentation/corefoundation/cfstringuppercase(_:_:))

### Constants

- [CFStringNormalizationForm](/documentation/corefoundation/cfstringnormalizationform)

#### Constants

- [case D](/documentation/corefoundation/cfstringnormalizationform/d)
- [case KD](/documentation/corefoundation/cfstringnormalizationform/kd)
- [case C](/documentation/corefoundation/cfstringnormalizationform/c)
- [case KC](/documentation/corefoundation/cfstringnormalizationform/kc)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfstringnormalizationform/init(rawvalue:))
- [Transform Identifiers for CFStringTransform](/documentation/corefoundation/transform-identifiers-for-cfstringtransform)

#### Constants

- [let kCFStringTransformStripCombiningMarks: CFString!](/documentation/corefoundation/kcfstringtransformstripcombiningmarks)
- [let kCFStringTransformToLatin: CFString!](/documentation/corefoundation/kcfstringtransformtolatin)
- [let kCFStringTransformFullwidthHalfwidth: CFString!](/documentation/corefoundation/kcfstringtransformfullwidthhalfwidth)
- [let kCFStringTransformLatinKatakana: CFString!](/documentation/corefoundation/kcfstringtransformlatinkatakana)
- [let kCFStringTransformLatinHiragana: CFString!](/documentation/corefoundation/kcfstringtransformlatinhiragana)
- [let kCFStringTransformHiraganaKatakana: CFString!](/documentation/corefoundation/kcfstringtransformhiraganakatakana)
- [let kCFStringTransformMandarinLatin: CFString!](/documentation/corefoundation/kcfstringtransformmandarinlatin)
- [let kCFStringTransformLatinHangul: CFString!](/documentation/corefoundation/kcfstringtransformlatinhangul)
- [let kCFStringTransformLatinArabic: CFString!](/documentation/corefoundation/kcfstringtransformlatinarabic)
- [let kCFStringTransformLatinHebrew: CFString!](/documentation/corefoundation/kcfstringtransformlatinhebrew)
- [let kCFStringTransformLatinThai: CFString!](/documentation/corefoundation/kcfstringtransformlatinthai)
- [let kCFStringTransformLatinCyrillic: CFString!](/documentation/corefoundation/kcfstringtransformlatincyrillic)
- [let kCFStringTransformLatinGreek: CFString!](/documentation/corefoundation/kcfstringtransformlatingreek)
- [let kCFStringTransformToXMLHex: CFString!](/documentation/corefoundation/kcfstringtransformtoxmlhex)
- [let kCFStringTransformToUnicodeName: CFString!](/documentation/corefoundation/kcfstringtransformtounicodename)
- [let kCFStringTransformStripDiacritics: CFString!](/documentation/corefoundation/kcfstringtransformstripdiacritics)
- [CFNotificationCenter](/documentation/corefoundation/cfnotificationcenter)

### Accessing a Notification Center

- [func CFNotificationCenterGetDarwinNotifyCenter() -> CFNotificationCenter!](/documentation/corefoundation/cfnotificationcentergetdarwinnotifycenter())
- [func CFNotificationCenterGetDistributedCenter() -> CFNotificationCenter!](/documentation/corefoundation/cfnotificationcentergetdistributedcenter())
- [func CFNotificationCenterGetLocalCenter() -> CFNotificationCenter!](/documentation/corefoundation/cfnotificationcentergetlocalcenter())

### Posting a Notification

- [func CFNotificationCenterPostNotification(CFNotificationCenter!, CFNotificationName!, UnsafeRawPointer!, CFDictionary!, Bool)](/documentation/corefoundation/cfnotificationcenterpostnotification(_:_:_:_:_:))
- [func CFNotificationCenterPostNotificationWithOptions(CFNotificationCenter!, CFNotificationName!, UnsafeRawPointer!, CFDictionary!, CFOptionFlags)](/documentation/corefoundation/cfnotificationcenterpostnotificationwithoptions(_:_:_:_:_:))

### Adding and Removing Observers

- [func CFNotificationCenterAddObserver(CFNotificationCenter!, UnsafeRawPointer!, CFNotificationCallback!, CFString!, UnsafeRawPointer!, CFNotificationSuspensionBehavior)](/documentation/corefoundation/cfnotificationcenteraddobserver(_:_:_:_:_:_:))
- [func CFNotificationCenterRemoveEveryObserver(CFNotificationCenter!, UnsafeRawPointer!)](/documentation/corefoundation/cfnotificationcenterremoveeveryobserver(_:_:))
- [func CFNotificationCenterRemoveObserver(CFNotificationCenter!, UnsafeRawPointer!, CFNotificationName!, UnsafeRawPointer!)](/documentation/corefoundation/cfnotificationcenterremoveobserver(_:_:_:_:))

### Getting the CFNotificationCenter Type ID

- [func CFNotificationCenterGetTypeID() -> CFTypeID](/documentation/corefoundation/cfnotificationcentergettypeid())

### Callbacks

- [CFNotificationCallback](/documentation/corefoundation/cfnotificationcallback)

### Constants

- [CFNotificationSuspensionBehavior](/documentation/corefoundation/cfnotificationsuspensionbehavior)

#### Constants

- [case drop](/documentation/corefoundation/cfnotificationsuspensionbehavior/drop)
- [case coalesce](/documentation/corefoundation/cfnotificationsuspensionbehavior/coalesce)
- [case hold](/documentation/corefoundation/cfnotificationsuspensionbehavior/hold)
- [case deliverImmediately](/documentation/corefoundation/cfnotificationsuspensionbehavior/deliverimmediately)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfnotificationsuspensionbehavior/init(rawvalue:))
- [Notification Posting Options](/documentation/corefoundation/1569610-notification-posting-options)

#### Constants

- [var kCFNotificationDeliverImmediately: CFOptionFlags](/documentation/corefoundation/kcfnotificationdeliverimmediately)
- [var kCFNotificationPostToAllSessions: CFOptionFlags](/documentation/corefoundation/kcfnotificationposttoallsessions)
- [CFNull](/documentation/corefoundation/cfnull)

### CFNull Miscellaneous Functions

- [func CFNullGetTypeID() -> CFTypeID](/documentation/corefoundation/cfnullgettypeid())

### Constants

- [Predefined Value](/documentation/corefoundation/predefined-value)

#### Constants

- [let kCFNull: CFNull!](/documentation/corefoundation/kcfnull)
- [CFNumber](/documentation/corefoundation/cfnumber)

### Creating a Number

- [func CFNumberCreate(CFAllocator!, CFNumberType, UnsafeRawPointer!) -> CFNumber!](/documentation/corefoundation/cfnumbercreate(_:_:_:))

### Getting Information About Numbers

- [func CFNumberGetByteSize(CFNumber!) -> CFIndex](/documentation/corefoundation/cfnumbergetbytesize(_:))
- [func CFNumberGetType(CFNumber!) -> CFNumberType](/documentation/corefoundation/cfnumbergettype(_:))
- [func CFNumberGetValue(CFNumber!, CFNumberType, UnsafeMutableRawPointer!) -> Bool](/documentation/corefoundation/cfnumbergetvalue(_:_:_:))
- [func CFNumberIsFloatType(CFNumber!) -> Bool](/documentation/corefoundation/cfnumberisfloattype(_:))

### Comparing Numbers

- [func CFNumberCompare(CFNumber!, CFNumber!, UnsafeMutableRawPointer!) -> CFComparisonResult](/documentation/corefoundation/cfnumbercompare(_:_:_:))

### Getting the CFNumber Type ID

- [func CFNumberGetTypeID() -> CFTypeID](/documentation/corefoundation/cfnumbergettypeid())

### Constants

- [CFNumberType](/documentation/corefoundation/cfnumbertype)

#### Constants

- [case sInt8Type](/documentation/corefoundation/cfnumbertype/sint8type)
- [case sInt16Type](/documentation/corefoundation/cfnumbertype/sint16type)
- [case sInt32Type](/documentation/corefoundation/cfnumbertype/sint32type)
- [case sInt64Type](/documentation/corefoundation/cfnumbertype/sint64type)
- [case float32Type](/documentation/corefoundation/cfnumbertype/float32type)
- [case float64Type](/documentation/corefoundation/cfnumbertype/float64type)
- [case charType](/documentation/corefoundation/cfnumbertype/chartype)
- [case shortType](/documentation/corefoundation/cfnumbertype/shorttype)
- [case intType](/documentation/corefoundation/cfnumbertype/inttype)
- [case longType](/documentation/corefoundation/cfnumbertype/longtype)
- [case longLongType](/documentation/corefoundation/cfnumbertype/longlongtype)
- [case floatType](/documentation/corefoundation/cfnumbertype/floattype)
- [case doubleType](/documentation/corefoundation/cfnumbertype/doubletype)
- [case cfIndexType](/documentation/corefoundation/cfnumbertype/cfindextype)
- [case nsIntegerType](/documentation/corefoundation/cfnumbertype/nsintegertype)
- [case cgFloatType](/documentation/corefoundation/cfnumbertype/cgfloattype)
- [static var maxType: CFNumberType](/documentation/corefoundation/cfnumbertype/maxtype)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfnumbertype/init(rawvalue:))
- [Predefined Values](/documentation/corefoundation/predefined-values)

#### Constants

- [let kCFNumberNaN: CFNumber!](/documentation/corefoundation/kcfnumbernan)
- [let kCFNumberNegativeInfinity: CFNumber!](/documentation/corefoundation/kcfnumbernegativeinfinity)
- [let kCFNumberPositiveInfinity: CFNumber!](/documentation/corefoundation/kcfnumberpositiveinfinity)
- [CFNumberFormatter](/documentation/corefoundation/cfnumberformatter)

### Creating a Number Formatter

- [func CFNumberFormatterCreate(CFAllocator!, CFLocale!, CFNumberFormatterStyle) -> CFNumberFormatter!](/documentation/corefoundation/cfnumberformattercreate(_:_:_:))

### Configuring a Number Formatter

- [func CFNumberFormatterSetFormat(CFNumberFormatter!, CFString!)](/documentation/corefoundation/cfnumberformattersetformat(_:_:))
- [func CFNumberFormatterSetProperty(CFNumberFormatter!, CFNumberFormatterKey!, CFTypeRef!)](/documentation/corefoundation/cfnumberformattersetproperty(_:_:_:))

### Formatting Values

- [func CFNumberFormatterCreateNumberFromString(CFAllocator!, CFNumberFormatter!, CFString!, UnsafeMutablePointer<CFRange>!, CFOptionFlags) -> CFNumber!](/documentation/corefoundation/cfnumberformattercreatenumberfromstring(_:_:_:_:_:))
- [func CFNumberFormatterCreateStringWithNumber(CFAllocator!, CFNumberFormatter!, CFNumber!) -> CFString!](/documentation/corefoundation/cfnumberformattercreatestringwithnumber(_:_:_:))
- [func CFNumberFormatterCreateStringWithValue(CFAllocator!, CFNumberFormatter!, CFNumberType, UnsafeRawPointer!) -> CFString!](/documentation/corefoundation/cfnumberformattercreatestringwithvalue(_:_:_:_:))
- [func CFNumberFormatterGetDecimalInfoForCurrencyCode(CFString!, UnsafeMutablePointer<Int32>!, UnsafeMutablePointer<Double>!) -> Bool](/documentation/corefoundation/cfnumberformattergetdecimalinfoforcurrencycode(_:_:_:))
- [func CFNumberFormatterGetValueFromString(CFNumberFormatter!, CFString!, UnsafeMutablePointer<CFRange>!, CFNumberType, UnsafeMutableRawPointer!) -> Bool](/documentation/corefoundation/cfnumberformattergetvaluefromstring(_:_:_:_:_:))

### Examining a Number Formatter

- [func CFNumberFormatterCopyProperty(CFNumberFormatter!, CFNumberFormatterKey!) -> CFTypeRef!](/documentation/corefoundation/cfnumberformattercopyproperty(_:_:))
- [func CFNumberFormatterGetFormat(CFNumberFormatter!) -> CFString!](/documentation/corefoundation/cfnumberformattergetformat(_:))
- [func CFNumberFormatterGetLocale(CFNumberFormatter!) -> CFLocale!](/documentation/corefoundation/cfnumberformattergetlocale(_:))
- [func CFNumberFormatterGetStyle(CFNumberFormatter!) -> CFNumberFormatterStyle](/documentation/corefoundation/cfnumberformattergetstyle(_:))

### Getting the CFNumberFormatter Type ID

- [func CFNumberFormatterGetTypeID() -> CFTypeID](/documentation/corefoundation/cfnumberformattergettypeid())

### Data Types

- [CFNumberFormatterStyle](/documentation/corefoundation/cfnumberformatterstyle)

#### Enumeration Cases

- [case currencyAccountingStyle](/documentation/corefoundation/cfnumberformatterstyle/currencyaccountingstyle)
- [case currencyISOCodeStyle](/documentation/corefoundation/cfnumberformatterstyle/currencyisocodestyle)
- [case currencyPluralStyle](/documentation/corefoundation/cfnumberformatterstyle/currencypluralstyle)
- [case currencyStyle](/documentation/corefoundation/cfnumberformatterstyle/currencystyle)
- [case decimalStyle](/documentation/corefoundation/cfnumberformatterstyle/decimalstyle)
- [case noStyle](/documentation/corefoundation/cfnumberformatterstyle/nostyle)
- [case ordinalStyle](/documentation/corefoundation/cfnumberformatterstyle/ordinalstyle)
- [case percentStyle](/documentation/corefoundation/cfnumberformatterstyle/percentstyle)
- [case scientificStyle](/documentation/corefoundation/cfnumberformatterstyle/scientificstyle)
- [case spellOutStyle](/documentation/corefoundation/cfnumberformatterstyle/spelloutstyle)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfnumberformatterstyle/init(rawvalue:))
- [CFNumberFormatterOptionFlags](/documentation/corefoundation/cfnumberformatteroptionflags)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfnumberformatteroptionflags/init(rawvalue:))

#### Type Properties

- [static var parseIntegersOnly: CFNumberFormatterOptionFlags](/documentation/corefoundation/cfnumberformatteroptionflags/parseintegersonly)
- [CFNumberFormatterPadPosition](/documentation/corefoundation/cfnumberformatterpadposition)

#### Enumeration Cases

- [case afterPrefix](/documentation/corefoundation/cfnumberformatterpadposition/afterprefix)
- [case afterSuffix](/documentation/corefoundation/cfnumberformatterpadposition/aftersuffix)
- [case beforePrefix](/documentation/corefoundation/cfnumberformatterpadposition/beforeprefix)
- [case beforeSuffix](/documentation/corefoundation/cfnumberformatterpadposition/beforesuffix)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfnumberformatterpadposition/init(rawvalue:))

### Constants

- [Number Formatter Styles](/documentation/corefoundation/number-formatter-styles)

#### Constants

- [case noStyle](/documentation/corefoundation/cfnumberformatterstyle/nostyle)
- [case decimalStyle](/documentation/corefoundation/cfnumberformatterstyle/decimalstyle)
- [case currencyStyle](/documentation/corefoundation/cfnumberformatterstyle/currencystyle)
- [case percentStyle](/documentation/corefoundation/cfnumberformatterstyle/percentstyle)
- [case scientificStyle](/documentation/corefoundation/cfnumberformatterstyle/scientificstyle)
- [case spellOutStyle](/documentation/corefoundation/cfnumberformatterstyle/spelloutstyle)
- [Number Formatter Property Keys](/documentation/corefoundation/number-formatter-property-keys)

#### Constants

- [static let currencyCode: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencycode)
- [static let decimalSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/decimalseparator)
- [static let currencyDecimalSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencydecimalseparator)
- [static let alwaysShowDecimalSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/alwaysshowdecimalseparator)
- [static let groupingSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/groupingseparator)
- [static let useGroupingSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/usegroupingseparator)
- [static let percentSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/percentsymbol)
- [static let zeroSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/zerosymbol)
- [static let naNSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/nansymbol)
- [static let infinitySymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/infinitysymbol)
- [static let minusSign: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minussign)
- [static let plusSign: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/plussign)
- [static let currencySymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencysymbol)
- [static let exponentSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/exponentsymbol)
- [static let minIntegerDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minintegerdigits)
- [static let maxIntegerDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/maxintegerdigits)
- [static let minFractionDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minfractiondigits)
- [static let maxFractionDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/maxfractiondigits)
- [static let groupingSize: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/groupingsize)
- [static let secondaryGroupingSize: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/secondarygroupingsize)
- [static let roundingMode: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/roundingmode)
- [static let roundingIncrement: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/roundingincrement)
- [static let formatWidth: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/formatwidth)
- [static let paddingPosition: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/paddingposition)
- [static let paddingCharacter: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/paddingcharacter)
- [static let defaultFormat: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/defaultformat)
- [static let multiplier: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/multiplier)
- [static let positivePrefix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/positiveprefix)
- [static let positiveSuffix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/positivesuffix)
- [static let negativePrefix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/negativeprefix)
- [static let negativeSuffix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/negativesuffix)
- [static let perMillSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/permillsymbol)
- [static let internationalCurrencySymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/internationalcurrencysymbol)
- [static let currencyGroupingSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencygroupingseparator)
- [static let isLenient: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/islenient)
- [static let useSignificantDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/usesignificantdigits)
- [static let minSignificantDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minsignificantdigits)
- [static let maxSignificantDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/maxsignificantdigits)
- [Number Format Options](/documentation/corefoundation/number_format_options)

#### Constants

- [static var parseIntegersOnly: CFNumberFormatterOptionFlags](/documentation/corefoundation/cfnumberformatteroptionflags/parseintegersonly)
- [CFNumberFormatterRoundingMode](/documentation/corefoundation/cfnumberformatterroundingmode)

#### Constants

- [case roundCeiling](/documentation/corefoundation/cfnumberformatterroundingmode/roundceiling)
- [case roundFloor](/documentation/corefoundation/cfnumberformatterroundingmode/roundfloor)
- [case roundDown](/documentation/corefoundation/cfnumberformatterroundingmode/rounddown)
- [case roundUp](/documentation/corefoundation/cfnumberformatterroundingmode/roundup)
- [case roundHalfEven](/documentation/corefoundation/cfnumberformatterroundingmode/roundhalfeven)
- [case roundHalfDown](/documentation/corefoundation/cfnumberformatterroundingmode/roundhalfdown)
- [case roundHalfUp](/documentation/corefoundation/cfnumberformatterroundingmode/roundhalfup)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfnumberformatterroundingmode/init(rawvalue:))
- [Padding Positions](/documentation/corefoundation/padding-positions)

#### Constants

- [case beforePrefix](/documentation/corefoundation/cfnumberformatterpadposition/beforeprefix)
- [case afterPrefix](/documentation/corefoundation/cfnumberformatterpadposition/afterprefix)
- [case beforeSuffix](/documentation/corefoundation/cfnumberformatterpadposition/beforesuffix)
- [case afterSuffix](/documentation/corefoundation/cfnumberformatterpadposition/aftersuffix)
- [CFPlugIn](/documentation/corefoundation/cfplugin)

### Creating Plug-ins

- [func CFPlugInCreate(CFAllocator!, CFURL!) -> CFPlugIn!](/documentation/corefoundation/cfplugincreate(_:_:))
- [func CFPlugInInstanceCreate(CFAllocator!, CFUUID!, CFUUID!) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfplugininstancecreate(_:_:_:))

### Registration

- [func CFPlugInRegisterFactoryFunction(CFUUID!, CFPlugInFactoryFunction!) -> Bool](/documentation/corefoundation/cfpluginregisterfactoryfunction(_:_:))
- [func CFPlugInRegisterFactoryFunctionByName(CFUUID!, CFPlugIn!, CFString!) -> Bool](/documentation/corefoundation/cfpluginregisterfactoryfunctionbyname(_:_:_:))
- [func CFPlugInRegisterPlugInType(CFUUID!, CFUUID!) -> Bool](/documentation/corefoundation/cfpluginregisterplugintype(_:_:))
- [func CFPlugInUnregisterFactory(CFUUID!) -> Bool](/documentation/corefoundation/cfpluginunregisterfactory(_:))
- [func CFPlugInUnregisterPlugInType(CFUUID!, CFUUID!) -> Bool](/documentation/corefoundation/cfpluginunregisterplugintype(_:_:))

### CFPlugIn Miscellaneous Functions

- [func CFPlugInAddInstanceForFactory(CFUUID!)](/documentation/corefoundation/cfpluginaddinstanceforfactory(_:))
- [func CFPlugInFindFactoriesForPlugInType(CFUUID!) -> CFArray!](/documentation/corefoundation/cfpluginfindfactoriesforplugintype(_:))
- [func CFPlugInFindFactoriesForPlugInTypeInPlugIn(CFUUID!, CFPlugIn!) -> CFArray!](/documentation/corefoundation/cfpluginfindfactoriesforplugintypeinplugin(_:_:))
- [func CFPlugInGetBundle(CFPlugIn!) -> CFBundle!](/documentation/corefoundation/cfplugingetbundle(_:))
- [func CFPlugInGetTypeID() -> CFTypeID](/documentation/corefoundation/cfplugingettypeid())
- [func CFPlugInIsLoadOnDemand(CFPlugIn!) -> Bool](/documentation/corefoundation/cfpluginisloadondemand(_:))
- [func CFPlugInRemoveInstanceForFactory(CFUUID!)](/documentation/corefoundation/cfpluginremoveinstanceforfactory(_:))
- [func CFPlugInSetLoadOnDemand(CFPlugIn!, Bool)](/documentation/corefoundation/cfpluginsetloadondemand(_:_:))

### Callbacks

- [CFPlugInDynamicRegisterFunction](/documentation/corefoundation/cfplugindynamicregisterfunction)
- [CFPlugInFactoryFunction](/documentation/corefoundation/cfpluginfactoryfunction)
- [CFPlugInUnloadFunction](/documentation/corefoundation/cfpluginunloadfunction)

### Constants

- [Information Property List Keys](/documentation/corefoundation/cfplugin-information-property-list-keys)

#### Constants

- [let kCFPlugInDynamicRegistrationKey: CFString!](/documentation/corefoundation/kcfplugindynamicregistrationkey)
- [let kCFPlugInDynamicRegisterFunctionKey: CFString!](/documentation/corefoundation/kcfplugindynamicregisterfunctionkey)
- [let kCFPlugInUnloadFunctionKey: CFString!](/documentation/corefoundation/kcfpluginunloadfunctionkey)
- [let kCFPlugInFactoriesKey: CFString!](/documentation/corefoundation/kcfpluginfactorieskey)
- [let kCFPlugInTypesKey: CFString!](/documentation/corefoundation/kcfplugintypeskey)
- [CFPlugInInstance](/documentation/corefoundation/cfplugininstance)

### Deprecated

- [func CFPlugInInstanceCreateWithInstanceDataSize(CFAllocator!, CFIndex, CFPlugInInstanceDeallocateInstanceDataFunction!, CFString!, CFPlugInInstanceGetInterfaceFunction!) -> CFPlugInInstance!](/documentation/corefoundation/cfplugininstancecreatewithinstancedatasize(_:_:_:_:_:))
- [func CFPlugInInstanceGetFactoryName(CFPlugInInstance!) -> CFString!](/documentation/corefoundation/cfplugininstancegetfactoryname(_:))
- [func CFPlugInInstanceGetInstanceData(CFPlugInInstance!) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfplugininstancegetinstancedata(_:))
- [func CFPlugInInstanceGetInterfaceFunctionTable(CFPlugInInstance!, CFString!, UnsafeMutablePointer<UnsafeMutableRawPointer?>!) -> Bool](/documentation/corefoundation/cfplugininstancegetinterfacefunctiontable(_:_:_:))
- [func CFPlugInInstanceGetTypeID() -> CFTypeID](/documentation/corefoundation/cfplugininstancegettypeid())

### Callbacks

- [CFPlugInInstanceDeallocateInstanceDataFunction](/documentation/corefoundation/cfplugininstancedeallocateinstancedatafunction)
- [CFPlugInInstanceGetInterfaceFunction](/documentation/corefoundation/cfplugininstancegetinterfacefunction)
- [CFPropertyList](/documentation/corefoundation/cfpropertylist)

### Creating a Property List

- [func CFPropertyListCreateWithData(CFAllocator!, CFData!, CFOptionFlags, UnsafeMutablePointer<CFPropertyListFormat>!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFPropertyList>!](/documentation/corefoundation/cfpropertylistcreatewithdata(_:_:_:_:_:))
- [func CFPropertyListCreateWithStream(CFAllocator!, CFReadStream!, CFIndex, CFOptionFlags, UnsafeMutablePointer<CFPropertyListFormat>!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFPropertyList>!](/documentation/corefoundation/cfpropertylistcreatewithstream(_:_:_:_:_:_:))
- [func CFPropertyListCreateDeepCopy(CFAllocator!, CFPropertyList!, CFOptionFlags) -> CFPropertyList!](/documentation/corefoundation/cfpropertylistcreatedeepcopy(_:_:_:))
- [func CFPropertyListCreateFromXMLData(CFAllocator!, CFData!, CFOptionFlags, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> Unmanaged<CFPropertyList>!](/documentation/corefoundation/cfpropertylistcreatefromxmldata(_:_:_:_:))
- [func CFPropertyListCreateFromStream(CFAllocator!, CFReadStream!, CFIndex, CFOptionFlags, UnsafeMutablePointer<CFPropertyListFormat>!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> Unmanaged<CFPropertyList>!](/documentation/corefoundation/cfpropertylistcreatefromstream(_:_:_:_:_:_:))

### Exporting a Property List

- [func CFPropertyListCreateData(CFAllocator!, CFPropertyList!, CFPropertyListFormat, CFOptionFlags, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFData>!](/documentation/corefoundation/cfpropertylistcreatedata(_:_:_:_:_:))
- [func CFPropertyListWrite(CFPropertyList!, CFWriteStream!, CFPropertyListFormat, CFOptionFlags, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> CFIndex](/documentation/corefoundation/cfpropertylistwrite(_:_:_:_:_:))
- [func CFPropertyListCreateXMLData(CFAllocator!, CFPropertyList!) -> Unmanaged<CFData>!](/documentation/corefoundation/cfpropertylistcreatexmldata(_:_:))
- [func CFPropertyListWriteToStream(CFPropertyList!, CFWriteStream!, CFPropertyListFormat, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> CFIndex](/documentation/corefoundation/cfpropertylistwritetostream(_:_:_:_:))

### Validating a Property List

- [func CFPropertyListIsValid(CFPropertyList!, CFPropertyListFormat) -> Bool](/documentation/corefoundation/cfpropertylistisvalid(_:_:))

### Data Types

- [CFPropertyListMutabilityOptions](/documentation/corefoundation/cfpropertylistmutabilityoptions)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfpropertylistmutabilityoptions/init(rawvalue:))

#### Type Properties

- [static var mutableContainers: CFPropertyListMutabilityOptions](/documentation/corefoundation/cfpropertylistmutabilityoptions/mutablecontainers)
- [static var mutableContainersAndLeaves: CFPropertyListMutabilityOptions](/documentation/corefoundation/cfpropertylistmutabilityoptions/mutablecontainersandleaves)

### Constants

- [CFPropertyListFormat](/documentation/corefoundation/cfpropertylistformat)

#### Constants

- [case openStepFormat](/documentation/corefoundation/cfpropertylistformat/openstepformat)
- [case xmlFormat_v1_0](/documentation/corefoundation/cfpropertylistformat/xmlformat_v1_0)
- [case binaryFormat_v1_0](/documentation/corefoundation/cfpropertylistformat/binaryformat_v1_0)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfpropertylistformat/init(rawvalue:))
- [Property List Mutability Options](/documentation/corefoundation/property_list_mutability_options)

#### Constants

- [static var mutableContainers: CFPropertyListMutabilityOptions](/documentation/corefoundation/cfpropertylistmutabilityoptions/mutablecontainers)
- [static var mutableContainersAndLeaves: CFPropertyListMutabilityOptions](/documentation/corefoundation/cfpropertylistmutabilityoptions/mutablecontainersandleaves)
- [Reading and Writing Error Codes](/documentation/corefoundation/1429999-reading-and-writing-error-codes)

#### Constants

- [var kCFPropertyListReadCorruptError: CFIndex](/documentation/corefoundation/kcfpropertylistreadcorrupterror)
- [var kCFPropertyListReadUnknownVersionError: CFIndex](/documentation/corefoundation/kcfpropertylistreadunknownversionerror)
- [var kCFPropertyListReadStreamError: CFIndex](/documentation/corefoundation/kcfpropertylistreadstreamerror)
- [var kCFPropertyListWriteStreamError: CFIndex](/documentation/corefoundation/kcfpropertylistwritestreamerror)
- [CFReadStream](/documentation/corefoundation/cfreadstream)

### Creating a Read Stream

- [func CFReadStreamCreateWithBytesNoCopy(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, CFAllocator!) -> CFReadStream!](/documentation/corefoundation/cfreadstreamcreatewithbytesnocopy(_:_:_:_:))
- [func CFReadStreamCreateWithFile(CFAllocator!, CFURL!) -> CFReadStream!](/documentation/corefoundation/cfreadstreamcreatewithfile(_:_:))

### Opening and Closing a Read Stream

- [func CFReadStreamClose(CFReadStream!)](/documentation/corefoundation/cfreadstreamclose(_:))
- [func CFReadStreamOpen(CFReadStream!) -> Bool](/documentation/corefoundation/cfreadstreamopen(_:))

### Reading from a Stream

- [func CFReadStreamRead(CFReadStream!, UnsafeMutablePointer<UInt8>!, CFIndex) -> CFIndex](/documentation/corefoundation/cfreadstreamread(_:_:_:))

### Scheduling a Read Stream

- [func CFReadStreamScheduleWithRunLoop(CFReadStream!, CFRunLoop!, CFRunLoopMode!)](/documentation/corefoundation/cfreadstreamschedulewithrunloop(_:_:_:))
- [func CFReadStreamUnscheduleFromRunLoop(CFReadStream!, CFRunLoop!, CFRunLoopMode!)](/documentation/corefoundation/cfreadstreamunschedulefromrunloop(_:_:_:))

### Examining Stream Properties

- [func CFReadStreamCopyProperty(CFReadStream!, CFStreamPropertyKey!) -> CFTypeRef!](/documentation/corefoundation/cfreadstreamcopyproperty(_:_:))
- [func CFReadStreamGetBuffer(CFReadStream!, CFIndex, UnsafeMutablePointer<CFIndex>!) -> UnsafePointer<UInt8>!](/documentation/corefoundation/cfreadstreamgetbuffer(_:_:_:))
- [func CFReadStreamCopyError(CFReadStream!) -> CFError!](/documentation/corefoundation/cfreadstreamcopyerror(_:))
- [func CFReadStreamGetError(CFReadStream!) -> CFStreamError](/documentation/corefoundation/cfreadstreamgeterror(_:))
- [func CFReadStreamGetStatus(CFReadStream!) -> CFStreamStatus](/documentation/corefoundation/cfreadstreamgetstatus(_:))
- [func CFReadStreamHasBytesAvailable(CFReadStream!) -> Bool](/documentation/corefoundation/cfreadstreamhasbytesavailable(_:))

### Setting Stream Properties

- [func CFReadStreamSetClient(CFReadStream!, CFOptionFlags, CFReadStreamClientCallBack!, UnsafeMutablePointer<CFStreamClientContext>!) -> Bool](/documentation/corefoundation/cfreadstreamsetclient(_:_:_:_:))
- [func CFReadStreamSetProperty(CFReadStream!, CFStreamPropertyKey!, CFTypeRef!) -> Bool](/documentation/corefoundation/cfreadstreamsetproperty(_:_:_:))

### Getting the CFReadStream Type ID

- [func CFReadStreamGetTypeID() -> CFTypeID](/documentation/corefoundation/cfreadstreamgettypeid())

### Callbacks

- [CFReadStreamClientCallBack](/documentation/corefoundation/cfreadstreamclientcallback)

### Data Types

- [CFStreamClientContext](/documentation/corefoundation/cfstreamclientcontext)

#### Initializers

- [init()](/documentation/corefoundation/cfstreamclientcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!, release: ((UnsafeMutableRawPointer?) -> Void)!, copyDescription: ((UnsafeMutableRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfstreamclientcontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeMutableRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfstreamclientcontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfstreamclientcontext/info)
- [var release: ((UnsafeMutableRawPointer?) -> Void)!](/documentation/corefoundation/cfstreamclientcontext/release)
- [var retain: ((UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!](/documentation/corefoundation/cfstreamclientcontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfstreamclientcontext/version)
- [CFRunLoop](/documentation/corefoundation/cfrunloop)

### Getting a Run Loop

- [func CFRunLoopGetCurrent() -> CFRunLoop!](/documentation/corefoundation/cfrunloopgetcurrent())
- [func CFRunLoopGetMain() -> CFRunLoop!](/documentation/corefoundation/cfrunloopgetmain())

### Starting and Stopping a Run Loop

- [func CFRunLoopRun()](/documentation/corefoundation/cfrunlooprun())
- [func CFRunLoopRunInMode(CFRunLoopMode!, CFTimeInterval, Bool) -> CFRunLoopRunResult](/documentation/corefoundation/cfrunloopruninmode(_:_:_:))
- [func CFRunLoopWakeUp(CFRunLoop!)](/documentation/corefoundation/cfrunloopwakeup(_:))
- [func CFRunLoopStop(CFRunLoop!)](/documentation/corefoundation/cfrunloopstop(_:))
- [func CFRunLoopIsWaiting(CFRunLoop!) -> Bool](/documentation/corefoundation/cfrunloopiswaiting(_:))

### Managing Sources

- [func CFRunLoopAddSource(CFRunLoop!, CFRunLoopSource!, CFRunLoopMode!)](/documentation/corefoundation/cfrunloopaddsource(_:_:_:))
- [func CFRunLoopContainsSource(CFRunLoop!, CFRunLoopSource!, CFRunLoopMode!) -> Bool](/documentation/corefoundation/cfrunloopcontainssource(_:_:_:))
- [func CFRunLoopRemoveSource(CFRunLoop!, CFRunLoopSource!, CFRunLoopMode!)](/documentation/corefoundation/cfrunloopremovesource(_:_:_:))

### Managing Observers

- [func CFRunLoopAddObserver(CFRunLoop!, CFRunLoopObserver!, CFRunLoopMode!)](/documentation/corefoundation/cfrunloopaddobserver(_:_:_:))
- [func CFRunLoopContainsObserver(CFRunLoop!, CFRunLoopObserver!, CFRunLoopMode!) -> Bool](/documentation/corefoundation/cfrunloopcontainsobserver(_:_:_:))
- [func CFRunLoopRemoveObserver(CFRunLoop!, CFRunLoopObserver!, CFRunLoopMode!)](/documentation/corefoundation/cfrunloopremoveobserver(_:_:_:))

### Managing Run Loop Modes

- [func CFRunLoopAddCommonMode(CFRunLoop!, CFRunLoopMode!)](/documentation/corefoundation/cfrunloopaddcommonmode(_:_:))
- [func CFRunLoopCopyAllModes(CFRunLoop!) -> CFArray!](/documentation/corefoundation/cfrunloopcopyallmodes(_:))
- [func CFRunLoopCopyCurrentMode(CFRunLoop!) -> CFRunLoopMode!](/documentation/corefoundation/cfrunloopcopycurrentmode(_:))

### Managing Timers

- [func CFRunLoopAddTimer(CFRunLoop!, CFRunLoopTimer!, CFRunLoopMode!)](/documentation/corefoundation/cfrunloopaddtimer(_:_:_:))
- [func CFRunLoopGetNextTimerFireDate(CFRunLoop!, CFRunLoopMode!) -> CFAbsoluteTime](/documentation/corefoundation/cfrunloopgetnexttimerfiredate(_:_:))
- [func CFRunLoopRemoveTimer(CFRunLoop!, CFRunLoopTimer!, CFRunLoopMode!)](/documentation/corefoundation/cfrunloopremovetimer(_:_:_:))
- [func CFRunLoopContainsTimer(CFRunLoop!, CFRunLoopTimer!, CFRunLoopMode!) -> Bool](/documentation/corefoundation/cfrunloopcontainstimer(_:_:_:))

### Scheduling Blocks

- [func CFRunLoopPerformBlock(CFRunLoop!, CFTypeRef!, (() -> Void)!)](/documentation/corefoundation/cfrunloopperformblock(_:_:_:))

### Getting the CFRunLoop Type ID

- [func CFRunLoopGetTypeID() -> CFTypeID](/documentation/corefoundation/cfrunloopgettypeid())

### Constants

- [CFRunLoopRunInMode Exit Codes](/documentation/corefoundation/cfrunloopruninmode_exit_codes)

#### Constants

- [case finished](/documentation/corefoundation/cfrunlooprunresult/finished)
- [case stopped](/documentation/corefoundation/cfrunlooprunresult/stopped)
- [case timedOut](/documentation/corefoundation/cfrunlooprunresult/timedout)
- [case handledSource](/documentation/corefoundation/cfrunlooprunresult/handledsource)
- [Common Mode Flag](/documentation/corefoundation/common-mode-flag)

#### Constants

- [static let commonModes: CFRunLoopMode!](/documentation/corefoundation/cfrunloopmode/commonmodes)
- [Default Run Loop Mode](/documentation/corefoundation/default-run-loop-mode)

#### Constants

- [static let defaultMode: CFRunLoopMode!](/documentation/corefoundation/cfrunloopmode/defaultmode)
- [CFRunLoopObserver](/documentation/corefoundation/cfrunloopobserver)

### CFRunLoopObserver Miscellaneous Functions

- [func CFRunLoopObserverCreateWithHandler(CFAllocator!, CFOptionFlags, Bool, CFIndex, ((CFRunLoopObserver?, CFRunLoopActivity) -> Void)!) -> CFRunLoopObserver!](/documentation/corefoundation/cfrunloopobservercreatewithhandler(_:_:_:_:_:))
- [func CFRunLoopObserverCreate(CFAllocator!, CFOptionFlags, Bool, CFIndex, CFRunLoopObserverCallBack!, UnsafeMutablePointer<CFRunLoopObserverContext>!) -> CFRunLoopObserver!](/documentation/corefoundation/cfrunloopobservercreate(_:_:_:_:_:_:))
- [func CFRunLoopObserverDoesRepeat(CFRunLoopObserver!) -> Bool](/documentation/corefoundation/cfrunloopobserverdoesrepeat(_:))
- [func CFRunLoopObserverGetActivities(CFRunLoopObserver!) -> CFOptionFlags](/documentation/corefoundation/cfrunloopobservergetactivities(_:))
- [func CFRunLoopObserverGetContext(CFRunLoopObserver!, UnsafeMutablePointer<CFRunLoopObserverContext>!)](/documentation/corefoundation/cfrunloopobservergetcontext(_:_:))
- [func CFRunLoopObserverGetOrder(CFRunLoopObserver!) -> CFIndex](/documentation/corefoundation/cfrunloopobservergetorder(_:))
- [func CFRunLoopObserverGetTypeID() -> CFTypeID](/documentation/corefoundation/cfrunloopobservergettypeid())
- [func CFRunLoopObserverInvalidate(CFRunLoopObserver!)](/documentation/corefoundation/cfrunloopobserverinvalidate(_:))
- [func CFRunLoopObserverIsValid(CFRunLoopObserver!) -> Bool](/documentation/corefoundation/cfrunloopobserverisvalid(_:))

### Callbacks

- [CFRunLoopObserverCallBack](/documentation/corefoundation/cfrunloopobservercallback)

### Data Types

- [CFRunLoopObserverContext](/documentation/corefoundation/cfrunloopobservercontext)

#### Initializers

- [init()](/documentation/corefoundation/cfrunloopobservercontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfrunloopobservercontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfrunloopobservercontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfrunloopobservercontext/info)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfrunloopobservercontext/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfrunloopobservercontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfrunloopobservercontext/version)

### Constants

- [CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity)

#### Constants

- [static var entry: CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity/entry)
- [static var beforeTimers: CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity/beforetimers)
- [static var beforeSources: CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity/beforesources)
- [static var beforeWaiting: CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity/beforewaiting)
- [static var afterWaiting: CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity/afterwaiting)
- [static var exit: CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity/exit)
- [static var allActivities: CFRunLoopActivity](/documentation/corefoundation/cfrunloopactivity/allactivities)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfrunloopactivity/init(rawvalue:))
- [CFRunLoopSource](/documentation/corefoundation/cfrunloopsource)

### CFRunLoopSource Miscellaneous Functions

- [func CFRunLoopSourceCreate(CFAllocator!, CFIndex, UnsafeMutablePointer<CFRunLoopSourceContext>!) -> CFRunLoopSource!](/documentation/corefoundation/cfrunloopsourcecreate(_:_:_:))
- [func CFRunLoopSourceGetContext(CFRunLoopSource!, UnsafeMutablePointer<CFRunLoopSourceContext>!)](/documentation/corefoundation/cfrunloopsourcegetcontext(_:_:))
- [func CFRunLoopSourceGetOrder(CFRunLoopSource!) -> CFIndex](/documentation/corefoundation/cfrunloopsourcegetorder(_:))
- [func CFRunLoopSourceGetTypeID() -> CFTypeID](/documentation/corefoundation/cfrunloopsourcegettypeid())
- [func CFRunLoopSourceInvalidate(CFRunLoopSource!)](/documentation/corefoundation/cfrunloopsourceinvalidate(_:))
- [func CFRunLoopSourceIsValid(CFRunLoopSource!) -> Bool](/documentation/corefoundation/cfrunloopsourceisvalid(_:))
- [func CFRunLoopSourceSignal(CFRunLoopSource!)](/documentation/corefoundation/cfrunloopsourcesignal(_:))

### Callbacks

- [var cancel: ((UnsafeMutableRawPointer?, CFRunLoop?, CFRunLoopMode?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext/cancel)
- [var equal: ((UnsafeRawPointer?, UnsafeRawPointer?) -> DarwinBoolean)!](/documentation/corefoundation/cfrunloopsourcecontext/equal)
- [var hash: ((UnsafeRawPointer?) -> CFHashCode)!](/documentation/corefoundation/cfrunloopsourcecontext/hash)
- [var perform: ((UnsafeMutableRawPointer?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext/perform)
- [var schedule: ((UnsafeMutableRawPointer?, CFRunLoop?, CFRunLoopMode?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext/schedule)

### Data Types

- [CFRunLoopSourceContext](/documentation/corefoundation/cfrunloopsourcecontext)

#### Initializers

- [init()](/documentation/corefoundation/cfrunloopsourcecontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!, equal: ((UnsafeRawPointer?, UnsafeRawPointer?) -> DarwinBoolean)!, hash: ((UnsafeRawPointer?) -> CFHashCode)!, schedule: ((UnsafeMutableRawPointer?, CFRunLoop?, CFRunLoopMode?) -> Void)!, cancel: ((UnsafeMutableRawPointer?, CFRunLoop?, CFRunLoopMode?) -> Void)!, perform: ((UnsafeMutableRawPointer?) -> Void)!)](/documentation/corefoundation/cfrunloopsourcecontext/init(version:info:retain:release:copydescription:equal:hash:schedule:cancel:perform:))

#### Instance Properties

- [var cancel: ((UnsafeMutableRawPointer?, CFRunLoop?, CFRunLoopMode?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext/cancel)
- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfrunloopsourcecontext/copydescription)
- [var equal: ((UnsafeRawPointer?, UnsafeRawPointer?) -> DarwinBoolean)!](/documentation/corefoundation/cfrunloopsourcecontext/equal)
- [var hash: ((UnsafeRawPointer?) -> CFHashCode)!](/documentation/corefoundation/cfrunloopsourcecontext/hash)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfrunloopsourcecontext/info)
- [var perform: ((UnsafeMutableRawPointer?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext/perform)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfrunloopsourcecontext/retain)
- [var schedule: ((UnsafeMutableRawPointer?, CFRunLoop?, CFRunLoopMode?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext/schedule)
- [var version: CFIndex](/documentation/corefoundation/cfrunloopsourcecontext/version)
- [CFRunLoopSourceContext1](/documentation/corefoundation/cfrunloopsourcecontext1)

#### Initializers

- [init()](/documentation/corefoundation/cfrunloopsourcecontext1/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!, equal: ((UnsafeRawPointer?, UnsafeRawPointer?) -> DarwinBoolean)!, hash: ((UnsafeRawPointer?) -> CFHashCode)!, getPort: ((UnsafeMutableRawPointer?) -> mach_port_t)!, perform: ((UnsafeMutableRawPointer?, CFIndex, CFAllocator?, UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!)](/documentation/corefoundation/cfrunloopsourcecontext1/init(version:info:retain:release:copydescription:equal:hash:getport:perform:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfrunloopsourcecontext1/copydescription)
- [var equal: ((UnsafeRawPointer?, UnsafeRawPointer?) -> DarwinBoolean)!](/documentation/corefoundation/cfrunloopsourcecontext1/equal)
- [var getPort: ((UnsafeMutableRawPointer?) -> mach_port_t)!](/documentation/corefoundation/cfrunloopsourcecontext1/getport)
- [var hash: ((UnsafeRawPointer?) -> CFHashCode)!](/documentation/corefoundation/cfrunloopsourcecontext1/hash)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfrunloopsourcecontext1/info)
- [var perform: ((UnsafeMutableRawPointer?, CFIndex, CFAllocator?, UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!](/documentation/corefoundation/cfrunloopsourcecontext1/perform)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfrunloopsourcecontext1/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfrunloopsourcecontext1/retain)
- [var version: CFIndex](/documentation/corefoundation/cfrunloopsourcecontext1/version)
- [CFRunLoopTimer](/documentation/corefoundation/cfrunlooptimer)

### CFRunLoopTimer Miscellaneous Functions

- [func CFRunLoopTimerCreateWithHandler(CFAllocator!, CFAbsoluteTime, CFTimeInterval, CFOptionFlags, CFIndex, ((CFRunLoopTimer?) -> Void)!) -> CFRunLoopTimer!](/documentation/corefoundation/cfrunlooptimercreatewithhandler(_:_:_:_:_:_:))
- [func CFRunLoopTimerCreate(CFAllocator!, CFAbsoluteTime, CFTimeInterval, CFOptionFlags, CFIndex, CFRunLoopTimerCallBack!, UnsafeMutablePointer<CFRunLoopTimerContext>!) -> CFRunLoopTimer!](/documentation/corefoundation/cfrunlooptimercreate(_:_:_:_:_:_:_:))
- [func CFRunLoopTimerDoesRepeat(CFRunLoopTimer!) -> Bool](/documentation/corefoundation/cfrunlooptimerdoesrepeat(_:))
- [func CFRunLoopTimerGetContext(CFRunLoopTimer!, UnsafeMutablePointer<CFRunLoopTimerContext>!)](/documentation/corefoundation/cfrunlooptimergetcontext(_:_:))
- [func CFRunLoopTimerGetInterval(CFRunLoopTimer!) -> CFTimeInterval](/documentation/corefoundation/cfrunlooptimergetinterval(_:))
- [func CFRunLoopTimerGetNextFireDate(CFRunLoopTimer!) -> CFAbsoluteTime](/documentation/corefoundation/cfrunlooptimergetnextfiredate(_:))
- [func CFRunLoopTimerGetOrder(CFRunLoopTimer!) -> CFIndex](/documentation/corefoundation/cfrunlooptimergetorder(_:))
- [func CFRunLoopTimerGetTypeID() -> CFTypeID](/documentation/corefoundation/cfrunlooptimergettypeid())
- [func CFRunLoopTimerInvalidate(CFRunLoopTimer!)](/documentation/corefoundation/cfrunlooptimerinvalidate(_:))
- [func CFRunLoopTimerIsValid(CFRunLoopTimer!) -> Bool](/documentation/corefoundation/cfrunlooptimerisvalid(_:))
- [func CFRunLoopTimerSetNextFireDate(CFRunLoopTimer!, CFAbsoluteTime)](/documentation/corefoundation/cfrunlooptimersetnextfiredate(_:_:))

### Callbacks

- [CFRunLoopTimerCallBack](/documentation/corefoundation/cfrunlooptimercallback)

### Data Types

- [CFRunLoopTimerContext](/documentation/corefoundation/cfrunlooptimercontext)

#### Initializers

- [init()](/documentation/corefoundation/cfrunlooptimercontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfrunlooptimercontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfrunlooptimercontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfrunlooptimercontext/info)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfrunlooptimercontext/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfrunlooptimercontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfrunlooptimercontext/version)
- [CFSet](/documentation/corefoundation/cfset)

### Creating Sets

- [func CFSetCreate(CFAllocator!, UnsafeMutablePointer<UnsafeRawPointer?>!, CFIndex, UnsafePointer<CFSetCallBacks>!) -> CFSet!](/documentation/corefoundation/cfsetcreate(_:_:_:_:))
- [func CFSetCreateCopy(CFAllocator!, CFSet!) -> CFSet!](/documentation/corefoundation/cfsetcreatecopy(_:_:))

### Examining a Set

- [func CFSetContainsValue(CFSet!, UnsafeRawPointer!) -> Bool](/documentation/corefoundation/cfsetcontainsvalue(_:_:))
- [func CFSetGetCount(CFSet!) -> CFIndex](/documentation/corefoundation/cfsetgetcount(_:))
- [func CFSetGetCountOfValue(CFSet!, UnsafeRawPointer!) -> CFIndex](/documentation/corefoundation/cfsetgetcountofvalue(_:_:))
- [func CFSetGetValue(CFSet!, UnsafeRawPointer!) -> UnsafeRawPointer!](/documentation/corefoundation/cfsetgetvalue(_:_:))
- [func CFSetGetValueIfPresent(CFSet!, UnsafeRawPointer!, UnsafeMutablePointer<UnsafeRawPointer?>!) -> Bool](/documentation/corefoundation/cfsetgetvalueifpresent(_:_:_:))
- [func CFSetGetValues(CFSet!, UnsafeMutablePointer<UnsafeRawPointer?>!)](/documentation/corefoundation/cfsetgetvalues(_:_:))

### Applying a Function to Set Members

- [func CFSetApplyFunction(CFSet!, ((UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void)!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cfsetapplyfunction(_:_:_:))

### Getting the CFSet Type ID

- [func CFSetGetTypeID() -> CFTypeID](/documentation/corefoundation/cfsetgettypeid())

### Callbacks

- [CFSetApplierFunction](/documentation/corefoundation/cfsetapplierfunction)
- [CFSetCopyDescriptionCallBack](/documentation/corefoundation/cfsetcopydescriptioncallback)
- [CFSetEqualCallBack](/documentation/corefoundation/cfsetequalcallback)
- [CFSetHashCallBack](/documentation/corefoundation/cfsethashcallback)
- [CFSetReleaseCallBack](/documentation/corefoundation/cfsetreleasecallback)
- [CFSetRetainCallBack](/documentation/corefoundation/cfsetretaincallback)

### Data Types

- [CFSetCallBacks](/documentation/corefoundation/cfsetcallbacks)

#### Initializers

- [init()](/documentation/corefoundation/cfsetcallbacks/init())
- [init(version: CFIndex, retain: CFSetRetainCallBack!, release: CFSetReleaseCallBack!, copyDescription: CFSetCopyDescriptionCallBack!, equal: CFSetEqualCallBack!, hash: CFSetHashCallBack!)](/documentation/corefoundation/cfsetcallbacks/init(version:retain:release:copydescription:equal:hash:))

#### Instance Properties

- [var copyDescription: CFSetCopyDescriptionCallBack!](/documentation/corefoundation/cfsetcallbacks/copydescription)
- [var equal: CFSetEqualCallBack!](/documentation/corefoundation/cfsetcallbacks/equal)
- [var hash: CFSetHashCallBack!](/documentation/corefoundation/cfsetcallbacks/hash)
- [var release: CFSetReleaseCallBack!](/documentation/corefoundation/cfsetcallbacks/release)
- [var retain: CFSetRetainCallBack!](/documentation/corefoundation/cfsetcallbacks/retain)
- [var version: CFIndex](/documentation/corefoundation/cfsetcallbacks/version)

### Constants

- [Predefined Callback Structures](/documentation/corefoundation/cfset-predefined-callback-structures)

#### Constants

- [let kCFTypeSetCallBacks: CFSetCallBacks](/documentation/corefoundation/kcftypesetcallbacks)
- [let kCFCopyStringSetCallBacks: CFSetCallBacks](/documentation/corefoundation/kcfcopystringsetcallbacks)
- [CFSocket](/documentation/corefoundation/cfsocket)

### Creating Sockets

- [func CFSocketCreate(CFAllocator!, Int32, Int32, Int32, CFOptionFlags, CFSocketCallBack!, UnsafePointer<CFSocketContext>!) -> CFSocket!](/documentation/corefoundation/cfsocketcreate(_:_:_:_:_:_:_:))
- [func CFSocketCreateConnectedToSocketSignature(CFAllocator!, UnsafePointer<CFSocketSignature>!, CFOptionFlags, CFSocketCallBack!, UnsafePointer<CFSocketContext>!, CFTimeInterval) -> CFSocket!](/documentation/corefoundation/cfsocketcreateconnectedtosocketsignature(_:_:_:_:_:_:))
- [func CFSocketCreateWithNative(CFAllocator!, CFSocketNativeHandle, CFOptionFlags, CFSocketCallBack!, UnsafePointer<CFSocketContext>!) -> CFSocket!](/documentation/corefoundation/cfsocketcreatewithnative(_:_:_:_:_:))
- [func CFSocketCreateWithSocketSignature(CFAllocator!, UnsafePointer<CFSocketSignature>!, CFOptionFlags, CFSocketCallBack!, UnsafePointer<CFSocketContext>!) -> CFSocket!](/documentation/corefoundation/cfsocketcreatewithsocketsignature(_:_:_:_:_:))

### Configuring Sockets

- [func CFSocketCopyAddress(CFSocket!) -> CFData!](/documentation/corefoundation/cfsocketcopyaddress(_:))
- [func CFSocketCopyPeerAddress(CFSocket!) -> CFData!](/documentation/corefoundation/cfsocketcopypeeraddress(_:))
- [func CFSocketDisableCallBacks(CFSocket!, CFOptionFlags)](/documentation/corefoundation/cfsocketdisablecallbacks(_:_:))
- [func CFSocketEnableCallBacks(CFSocket!, CFOptionFlags)](/documentation/corefoundation/cfsocketenablecallbacks(_:_:))
- [func CFSocketGetContext(CFSocket!, UnsafeMutablePointer<CFSocketContext>!)](/documentation/corefoundation/cfsocketgetcontext(_:_:))
- [func CFSocketGetNative(CFSocket!) -> CFSocketNativeHandle](/documentation/corefoundation/cfsocketgetnative(_:))
- [func CFSocketGetSocketFlags(CFSocket!) -> CFOptionFlags](/documentation/corefoundation/cfsocketgetsocketflags(_:))
- [func CFSocketSetAddress(CFSocket!, CFData!) -> CFSocketError](/documentation/corefoundation/cfsocketsetaddress(_:_:))
- [func CFSocketSetSocketFlags(CFSocket!, CFOptionFlags)](/documentation/corefoundation/cfsocketsetsocketflags(_:_:))

### Using Sockets

- [func CFSocketConnectToAddress(CFSocket!, CFData!, CFTimeInterval) -> CFSocketError](/documentation/corefoundation/cfsocketconnecttoaddress(_:_:_:))
- [func CFSocketCreateRunLoopSource(CFAllocator!, CFSocket!, CFIndex) -> CFRunLoopSource!](/documentation/corefoundation/cfsocketcreaterunloopsource(_:_:_:))
- [func CFSocketGetTypeID() -> CFTypeID](/documentation/corefoundation/cfsocketgettypeid())
- [func CFSocketInvalidate(CFSocket!)](/documentation/corefoundation/cfsocketinvalidate(_:))
- [func CFSocketIsValid(CFSocket!) -> Bool](/documentation/corefoundation/cfsocketisvalid(_:))
- [func CFSocketSendData(CFSocket!, CFData!, CFData!, CFTimeInterval) -> CFSocketError](/documentation/corefoundation/cfsocketsenddata(_:_:_:_:))

### Callbacks

- [CFSocketCallBack](/documentation/corefoundation/cfsocketcallback)

### Data Types

- [CFSocketContext](/documentation/corefoundation/cfsocketcontext)

#### Initializers

- [init()](/documentation/corefoundation/cfsocketcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!, release: ((UnsafeRawPointer?) -> Void)!, copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfsocketcontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfsocketcontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfsocketcontext/info)
- [var release: ((UnsafeRawPointer?) -> Void)!](/documentation/corefoundation/cfsocketcontext/release)
- [var retain: ((UnsafeRawPointer?) -> UnsafeRawPointer?)!](/documentation/corefoundation/cfsocketcontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfsocketcontext/version)
- [CFSocketNativeHandle](/documentation/corefoundation/cfsocketnativehandle)
- [CFSocketSignature](/documentation/corefoundation/cfsocketsignature)

#### Initializers

- [init()](/documentation/corefoundation/cfsocketsignature/init())
- [init(protocolFamily: Int32, socketType: Int32, protocol: Int32, address: Unmanaged<CFData>!)](/documentation/corefoundation/cfsocketsignature/init(protocolfamily:sockettype:protocol:address:))

#### Instance Properties

- [var address: Unmanaged<CFData>!](/documentation/corefoundation/cfsocketsignature/address)
- [var `protocol`: Int32](/documentation/corefoundation/cfsocketsignature/protocol)
- [var protocolFamily: Int32](/documentation/corefoundation/cfsocketsignature/protocolfamily)
- [var socketType: Int32](/documentation/corefoundation/cfsocketsignature/sockettype)

### Constants

- [CFSocketCallBackType](/documentation/corefoundation/cfsocketcallbacktype)

#### Constants

- [static var readCallBack: CFSocketCallBackType](/documentation/corefoundation/cfsocketcallbacktype/readcallback)
- [static var acceptCallBack: CFSocketCallBackType](/documentation/corefoundation/cfsocketcallbacktype/acceptcallback)
- [static var dataCallBack: CFSocketCallBackType](/documentation/corefoundation/cfsocketcallbacktype/datacallback)
- [static var connectCallBack: CFSocketCallBackType](/documentation/corefoundation/cfsocketcallbacktype/connectcallback)
- [static var writeCallBack: CFSocketCallBackType](/documentation/corefoundation/cfsocketcallbacktype/writecallback)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfsocketcallbacktype/init(rawvalue:))
- [CFSocket Flags](/documentation/corefoundation/1560944-cfsocket-flags)

#### Constants

- [var kCFSocketAutomaticallyReenableReadCallBack: CFOptionFlags](/documentation/corefoundation/kcfsocketautomaticallyreenablereadcallback)
- [var kCFSocketAutomaticallyReenableAcceptCallBack: CFOptionFlags](/documentation/corefoundation/kcfsocketautomaticallyreenableacceptcallback)
- [var kCFSocketAutomaticallyReenableDataCallBack: CFOptionFlags](/documentation/corefoundation/kcfsocketautomaticallyreenabledatacallback)
- [var kCFSocketAutomaticallyReenableWriteCallBack: CFOptionFlags](/documentation/corefoundation/kcfsocketautomaticallyreenablewritecallback)
- [var kCFSocketLeaveErrors: CFOptionFlags](/documentation/corefoundation/kcfsocketleaveerrors)
- [var kCFSocketCloseOnInvalidate: CFOptionFlags](/documentation/corefoundation/kcfsocketcloseoninvalidate)
- [CFSocketError](/documentation/corefoundation/cfsocketerror)

#### Constants

- [case success](/documentation/corefoundation/cfsocketerror/success)
- [case error](/documentation/corefoundation/cfsocketerror/error)
- [case timeout](/documentation/corefoundation/cfsocketerror/timeout)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfsocketerror/init(rawvalue:))
- [CFString](/documentation/corefoundation/cfstring)

### Creating a CFString

- [func CFStringCreateArrayBySeparatingStrings(CFAllocator!, CFString!, CFString!) -> CFArray!](/documentation/corefoundation/cfstringcreatearraybyseparatingstrings(_:_:_:))
- [func CFStringCreateByCombiningStrings(CFAllocator!, CFArray!, CFString!) -> CFString!](/documentation/corefoundation/cfstringcreatebycombiningstrings(_:_:_:))
- [func CFStringCreateCopy(CFAllocator!, CFString!) -> CFString!](/documentation/corefoundation/cfstringcreatecopy(_:_:))
- [func CFStringCreateFromExternalRepresentation(CFAllocator!, CFData!, CFStringEncoding) -> CFString!](/documentation/corefoundation/cfstringcreatefromexternalrepresentation(_:_:_:))
- [func CFStringCreateWithBytes(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, CFStringEncoding, Bool) -> CFString!](/documentation/corefoundation/cfstringcreatewithbytes(_:_:_:_:_:))
- [func CFStringCreateWithBytesNoCopy(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, CFStringEncoding, Bool, CFAllocator!) -> CFString!](/documentation/corefoundation/cfstringcreatewithbytesnocopy(_:_:_:_:_:_:))
- [func CFStringCreateWithCharacters(CFAllocator!, UnsafePointer<UniChar>!, CFIndex) -> CFString!](/documentation/corefoundation/cfstringcreatewithcharacters(_:_:_:))
- [func CFStringCreateWithCharactersNoCopy(CFAllocator!, UnsafePointer<UniChar>!, CFIndex, CFAllocator!) -> CFString!](/documentation/corefoundation/cfstringcreatewithcharactersnocopy(_:_:_:_:))
- [func CFStringCreateWithCString(CFAllocator!, UnsafePointer<CChar>!, CFStringEncoding) -> CFString!](/documentation/corefoundation/cfstringcreatewithcstring(_:_:_:))
- [func CFStringCreateWithCStringNoCopy(CFAllocator!, UnsafePointer<CChar>!, CFStringEncoding, CFAllocator!) -> CFString!](/documentation/corefoundation/cfstringcreatewithcstringnocopy(_:_:_:_:))
- [func CFStringCreateWithFormatAndArguments(CFAllocator!, CFDictionary!, CFString!, CVaListPointer) -> CFString!](/documentation/corefoundation/cfstringcreatewithformatandarguments(_:_:_:_:))
- [func CFStringCreateWithPascalString(CFAllocator!, ConstStr255Param!, CFStringEncoding) -> CFString!](/documentation/corefoundation/cfstringcreatewithpascalstring(_:_:_:))
- [func CFStringCreateWithPascalStringNoCopy(CFAllocator!, ConstStr255Param!, CFStringEncoding, CFAllocator!) -> CFString!](/documentation/corefoundation/cfstringcreatewithpascalstringnocopy(_:_:_:_:))
- [func CFStringCreateWithSubstring(CFAllocator!, CFString!, CFRange) -> CFString!](/documentation/corefoundation/cfstringcreatewithsubstring(_:_:_:))

### Searching Strings

- [func CFStringCreateArrayWithFindResults(CFAllocator!, CFString!, CFString!, CFRange, CFStringCompareFlags) -> CFArray!](/documentation/corefoundation/cfstringcreatearraywithfindresults(_:_:_:_:_:))
- [func CFStringFind(CFString!, CFString!, CFStringCompareFlags) -> CFRange](/documentation/corefoundation/cfstringfind(_:_:_:))
- [func CFStringFindCharacterFromSet(CFString!, CFCharacterSet!, CFRange, CFStringCompareFlags, UnsafeMutablePointer<CFRange>!) -> Bool](/documentation/corefoundation/cfstringfindcharacterfromset(_:_:_:_:_:))
- [func CFStringFindWithOptions(CFString!, CFString!, CFRange, CFStringCompareFlags, UnsafeMutablePointer<CFRange>!) -> Bool](/documentation/corefoundation/cfstringfindwithoptions(_:_:_:_:_:))
- [func CFStringFindWithOptionsAndLocale(CFString!, CFString!, CFRange, CFStringCompareFlags, CFLocale!, UnsafeMutablePointer<CFRange>!) -> Bool](/documentation/corefoundation/cfstringfindwithoptionsandlocale(_:_:_:_:_:_:))
- [func CFStringGetLineBounds(CFString!, CFRange, UnsafeMutablePointer<CFIndex>!, UnsafeMutablePointer<CFIndex>!, UnsafeMutablePointer<CFIndex>!)](/documentation/corefoundation/cfstringgetlinebounds(_:_:_:_:_:))

### Comparing Strings

- [func CFStringCompare(CFString!, CFString!, CFStringCompareFlags) -> CFComparisonResult](/documentation/corefoundation/cfstringcompare(_:_:_:))
- [func CFStringCompareWithOptions(CFString!, CFString!, CFRange, CFStringCompareFlags) -> CFComparisonResult](/documentation/corefoundation/cfstringcomparewithoptions(_:_:_:_:))
- [func CFStringCompareWithOptionsAndLocale(CFString!, CFString!, CFRange, CFStringCompareFlags, CFLocale!) -> CFComparisonResult](/documentation/corefoundation/cfstringcomparewithoptionsandlocale(_:_:_:_:_:))
- [func CFStringHasPrefix(CFString!, CFString!) -> Bool](/documentation/corefoundation/cfstringhasprefix(_:_:))
- [func CFStringHasSuffix(CFString!, CFString!) -> Bool](/documentation/corefoundation/cfstringhassuffix(_:_:))

### Accessing Characters

- [func CFStringCreateExternalRepresentation(CFAllocator!, CFString!, CFStringEncoding, UInt8) -> CFData!](/documentation/corefoundation/cfstringcreateexternalrepresentation(_:_:_:_:))
- [func CFStringGetBytes(CFString!, CFRange, CFStringEncoding, UInt8, Bool, UnsafeMutablePointer<UInt8>!, CFIndex, UnsafeMutablePointer<CFIndex>!) -> CFIndex](/documentation/corefoundation/cfstringgetbytes(_:_:_:_:_:_:_:_:))
- [func CFStringGetCharacterAtIndex(CFString!, CFIndex) -> UniChar](/documentation/corefoundation/cfstringgetcharacteratindex(_:_:))
- [func CFStringGetCharacters(CFString!, CFRange, UnsafeMutablePointer<UniChar>!)](/documentation/corefoundation/cfstringgetcharacters(_:_:_:))
- [func CFStringGetCharactersPtr(CFString!) -> UnsafePointer<UniChar>!](/documentation/corefoundation/cfstringgetcharactersptr(_:))
- [func CFStringGetCharacterFromInlineBuffer(UnsafeMutablePointer<CFStringInlineBuffer>!, CFIndex) -> UniChar](/documentation/corefoundation/cfstringgetcharacterfrominlinebuffer(_:_:))
- [func CFStringGetCString(CFString!, UnsafeMutablePointer<CChar>!, CFIndex, CFStringEncoding) -> Bool](/documentation/corefoundation/cfstringgetcstring(_:_:_:_:))
- [func CFStringGetCStringPtr(CFString!, CFStringEncoding) -> UnsafePointer<CChar>!](/documentation/corefoundation/cfstringgetcstringptr(_:_:))
- [func CFStringGetLength(CFString!) -> CFIndex](/documentation/corefoundation/cfstringgetlength(_:))
- [func CFStringGetPascalString(CFString!, StringPtr!, CFIndex, CFStringEncoding) -> Bool](/documentation/corefoundation/cfstringgetpascalstring(_:_:_:_:))
- [func CFStringGetPascalStringPtr(CFString!, CFStringEncoding) -> ConstStringPtr!](/documentation/corefoundation/cfstringgetpascalstringptr(_:_:))
- [func CFStringGetRangeOfComposedCharactersAtIndex(CFString!, CFIndex) -> CFRange](/documentation/corefoundation/cfstringgetrangeofcomposedcharactersatindex(_:_:))
- [func CFStringInitInlineBuffer(CFString!, UnsafeMutablePointer<CFStringInlineBuffer>!, CFRange)](/documentation/corefoundation/cfstringinitinlinebuffer(_:_:_:))

### Working With Hyphenation

- [func CFStringGetHyphenationLocationBeforeIndex(CFString!, CFIndex, CFRange, CFOptionFlags, CFLocale!, UnsafeMutablePointer<UTF32Char>!) -> CFIndex](/documentation/corefoundation/cfstringgethyphenationlocationbeforeindex(_:_:_:_:_:_:))
- [func CFStringIsHyphenationAvailableForLocale(CFLocale!) -> Bool](/documentation/corefoundation/cfstringishyphenationavailableforlocale(_:))

### Working With Encodings

- [func CFStringConvertEncodingToIANACharSetName(CFStringEncoding) -> CFString!](/documentation/corefoundation/cfstringconvertencodingtoianacharsetname(_:))
- [func CFStringConvertEncodingToNSStringEncoding(CFStringEncoding) -> UInt](/documentation/corefoundation/cfstringconvertencodingtonsstringencoding(_:))
- [func CFStringConvertEncodingToWindowsCodepage(CFStringEncoding) -> UInt32](/documentation/corefoundation/cfstringconvertencodingtowindowscodepage(_:))
- [func CFStringConvertIANACharSetNameToEncoding(CFString!) -> CFStringEncoding](/documentation/corefoundation/cfstringconvertianacharsetnametoencoding(_:))
- [func CFStringConvertNSStringEncodingToEncoding(UInt) -> CFStringEncoding](/documentation/corefoundation/cfstringconvertnsstringencodingtoencoding(_:))
- [func CFStringConvertWindowsCodepageToEncoding(UInt32) -> CFStringEncoding](/documentation/corefoundation/cfstringconvertwindowscodepagetoencoding(_:))
- [func CFStringGetFastestEncoding(CFString!) -> CFStringEncoding](/documentation/corefoundation/cfstringgetfastestencoding(_:))
- [func CFStringGetListOfAvailableEncodings() -> UnsafePointer<CFStringEncoding>!](/documentation/corefoundation/cfstringgetlistofavailableencodings())
- [func CFStringGetMaximumSizeForEncoding(CFIndex, CFStringEncoding) -> CFIndex](/documentation/corefoundation/cfstringgetmaximumsizeforencoding(_:_:))
- [func CFStringGetMostCompatibleMacStringEncoding(CFStringEncoding) -> CFStringEncoding](/documentation/corefoundation/cfstringgetmostcompatiblemacstringencoding(_:))
- [func CFStringGetNameOfEncoding(CFStringEncoding) -> CFString!](/documentation/corefoundation/cfstringgetnameofencoding(_:))
- [func CFStringGetSmallestEncoding(CFString!) -> CFStringEncoding](/documentation/corefoundation/cfstringgetsmallestencoding(_:))
- [func CFStringGetSystemEncoding() -> CFStringEncoding](/documentation/corefoundation/cfstringgetsystemencoding())
- [func CFStringIsEncodingAvailable(CFStringEncoding) -> Bool](/documentation/corefoundation/cfstringisencodingavailable(_:))

### Getting Numeric Values

- [func CFStringGetDoubleValue(CFString!) -> Double](/documentation/corefoundation/cfstringgetdoublevalue(_:))
- [func CFStringGetIntValue(CFString!) -> Int32](/documentation/corefoundation/cfstringgetintvalue(_:))

### Getting String Properties

- [func CFShowStr(CFString!)](/documentation/corefoundation/cfshowstr(_:))
- [func CFStringGetTypeID() -> CFTypeID](/documentation/corefoundation/cfstringgettypeid())

### String File System Representations

- [func CFStringCreateWithFileSystemRepresentation(CFAllocator!, UnsafePointer<CChar>!) -> CFString!](/documentation/corefoundation/cfstringcreatewithfilesystemrepresentation(_:_:))
- [func CFStringGetFileSystemRepresentation(CFString!, UnsafeMutablePointer<CChar>!, CFIndex) -> Bool](/documentation/corefoundation/cfstringgetfilesystemrepresentation(_:_:_:))
- [func CFStringGetMaximumSizeOfFileSystemRepresentation(CFString!) -> CFIndex](/documentation/corefoundation/cfstringgetmaximumsizeoffilesystemrepresentation(_:))

### Getting Paragraph Bounds

- [func CFStringGetParagraphBounds(CFString!, CFRange, UnsafeMutablePointer<CFIndex>!, UnsafeMutablePointer<CFIndex>!, UnsafeMutablePointer<CFIndex>!)](/documentation/corefoundation/cfstringgetparagraphbounds(_:_:_:_:_:))

### Managing Surrogates

- [func CFStringGetLongCharacterForSurrogatePair(UniChar, UniChar) -> UTF32Char](/documentation/corefoundation/cfstringgetlongcharacterforsurrogatepair(_:_:))
- [func CFStringGetSurrogatePairForLongCharacter(UTF32Char, UnsafeMutablePointer<UniChar>!) -> Bool](/documentation/corefoundation/cfstringgetsurrogatepairforlongcharacter(_:_:))
- [func CFStringIsSurrogateHighCharacter(UniChar) -> Bool](/documentation/corefoundation/cfstringissurrogatehighcharacter(_:))
- [func CFStringIsSurrogateLowCharacter(UniChar) -> Bool](/documentation/corefoundation/cfstringissurrogatelowcharacter(_:))

### Data Types

- [CFStringEncoding](/documentation/corefoundation/cfstringencoding)
- [CFStringEncodings](/documentation/corefoundation/cfstringencodings)

#### Enumeration Cases

- [case ANSEL](/documentation/corefoundation/cfstringencodings/ansel)
- [case big5](/documentation/corefoundation/cfstringencodings/big5)
- [case big5_E](/documentation/corefoundation/cfstringencodings/big5_e)
- [case big5_HKSCS_1999](/documentation/corefoundation/cfstringencodings/big5_hkscs_1999)
- [case CNS_11643_92_P1](/documentation/corefoundation/cfstringencodings/cns_11643_92_p1)
- [case CNS_11643_92_P2](/documentation/corefoundation/cfstringencodings/cns_11643_92_p2)
- [case CNS_11643_92_P3](/documentation/corefoundation/cfstringencodings/cns_11643_92_p3)
- [case dosArabic](/documentation/corefoundation/cfstringencodings/dosarabic)
- [case dosBalticRim](/documentation/corefoundation/cfstringencodings/dosbalticrim)
- [case dosCanadianFrench](/documentation/corefoundation/cfstringencodings/doscanadianfrench)
- [case dosChineseSimplif](/documentation/corefoundation/cfstringencodings/doschinesesimplif)
- [case dosChineseTrad](/documentation/corefoundation/cfstringencodings/doschinesetrad)
- [case dosCyrillic](/documentation/corefoundation/cfstringencodings/doscyrillic)
- [case dosGreek](/documentation/corefoundation/cfstringencodings/dosgreek)
- [case dosGreek1](/documentation/corefoundation/cfstringencodings/dosgreek1)
- [case dosGreek2](/documentation/corefoundation/cfstringencodings/dosgreek2)
- [case dosHebrew](/documentation/corefoundation/cfstringencodings/doshebrew)
- [case dosIcelandic](/documentation/corefoundation/cfstringencodings/dosicelandic)
- [case dosJapanese](/documentation/corefoundation/cfstringencodings/dosjapanese)
- [case dosKorean](/documentation/corefoundation/cfstringencodings/doskorean)
- [case dosLatin1](/documentation/corefoundation/cfstringencodings/doslatin1)
- [case dosLatin2](/documentation/corefoundation/cfstringencodings/doslatin2)
- [case dosLatinUS](/documentation/corefoundation/cfstringencodings/doslatinus)
- [case dosNordic](/documentation/corefoundation/cfstringencodings/dosnordic)
- [case dosPortuguese](/documentation/corefoundation/cfstringencodings/dosportuguese)
- [case dosRussian](/documentation/corefoundation/cfstringencodings/dosrussian)
- [case dosThai](/documentation/corefoundation/cfstringencodings/dosthai)
- [case dosTurkish](/documentation/corefoundation/cfstringencodings/dosturkish)
- [case EBCDIC_CP037](/documentation/corefoundation/cfstringencodings/ebcdic_cp037)
- [case EBCDIC_US](/documentation/corefoundation/cfstringencodings/ebcdic_us)
- [case EUC_CN](/documentation/corefoundation/cfstringencodings/euc_cn)
- [case EUC_JP](/documentation/corefoundation/cfstringencodings/euc_jp)
- [case EUC_KR](/documentation/corefoundation/cfstringencodings/euc_kr)
- [case EUC_TW](/documentation/corefoundation/cfstringencodings/euc_tw)
- [case GBK_95](/documentation/corefoundation/cfstringencodings/gbk_95)
- [case GB_18030_2000](/documentation/corefoundation/cfstringencodings/gb_18030_2000)
- [case GB_2312_80](/documentation/corefoundation/cfstringencodings/gb_2312_80)
- [case HZ_GB_2312](/documentation/corefoundation/cfstringencodings/hz_gb_2312)
- [case isoLatin10](/documentation/corefoundation/cfstringencodings/isolatin10)
- [case isoLatin2](/documentation/corefoundation/cfstringencodings/isolatin2)
- [case isoLatin3](/documentation/corefoundation/cfstringencodings/isolatin3)
- [case isoLatin4](/documentation/corefoundation/cfstringencodings/isolatin4)
- [case isoLatin5](/documentation/corefoundation/cfstringencodings/isolatin5)
- [case isoLatin6](/documentation/corefoundation/cfstringencodings/isolatin6)
- [case isoLatin7](/documentation/corefoundation/cfstringencodings/isolatin7)
- [case isoLatin8](/documentation/corefoundation/cfstringencodings/isolatin8)
- [case isoLatin9](/documentation/corefoundation/cfstringencodings/isolatin9)
- [case isoLatinArabic](/documentation/corefoundation/cfstringencodings/isolatinarabic)
- [case isoLatinCyrillic](/documentation/corefoundation/cfstringencodings/isolatincyrillic)
- [case isoLatinGreek](/documentation/corefoundation/cfstringencodings/isolatingreek)
- [case isoLatinHebrew](/documentation/corefoundation/cfstringencodings/isolatinhebrew)
- [case isoLatinThai](/documentation/corefoundation/cfstringencodings/isolatinthai)
- [case ISO_2022_CN](/documentation/corefoundation/cfstringencodings/iso_2022_cn)
- [case ISO_2022_CN_EXT](/documentation/corefoundation/cfstringencodings/iso_2022_cn_ext)
- [case ISO_2022_JP](/documentation/corefoundation/cfstringencodings/iso_2022_jp)
- [case ISO_2022_JP_1](/documentation/corefoundation/cfstringencodings/iso_2022_jp_1)
- [case ISO_2022_JP_2](/documentation/corefoundation/cfstringencodings/iso_2022_jp_2)
- [case ISO_2022_JP_3](/documentation/corefoundation/cfstringencodings/iso_2022_jp_3)
- [case ISO_2022_KR](/documentation/corefoundation/cfstringencodings/iso_2022_kr)
- [case JIS_C6226_78](/documentation/corefoundation/cfstringencodings/jis_c6226_78)
- [case JIS_X0201_76](/documentation/corefoundation/cfstringencodings/jis_x0201_76)
- [case JIS_X0208_83](/documentation/corefoundation/cfstringencodings/jis_x0208_83)
- [case JIS_X0208_90](/documentation/corefoundation/cfstringencodings/jis_x0208_90)
- [case JIS_X0212_90](/documentation/corefoundation/cfstringencodings/jis_x0212_90)
- [case KOI8_R](/documentation/corefoundation/cfstringencodings/koi8_r)
- [case KOI8_U](/documentation/corefoundation/cfstringencodings/koi8_u)
- [case KSC_5601_87](/documentation/corefoundation/cfstringencodings/ksc_5601_87)
- [case ksc_5601_92_Johab](/documentation/corefoundation/cfstringencodings/ksc_5601_92_johab)
- [case macArabic](/documentation/corefoundation/cfstringencodings/macarabic)
- [case macArmenian](/documentation/corefoundation/cfstringencodings/macarmenian)
- [case macBengali](/documentation/corefoundation/cfstringencodings/macbengali)
- [case macBurmese](/documentation/corefoundation/cfstringencodings/macburmese)
- [case macCeltic](/documentation/corefoundation/cfstringencodings/macceltic)
- [case macCentralEurRoman](/documentation/corefoundation/cfstringencodings/maccentraleurroman)
- [case macChineseSimp](/documentation/corefoundation/cfstringencodings/macchinesesimp)
- [case macChineseTrad](/documentation/corefoundation/cfstringencodings/macchinesetrad)
- [case macCroatian](/documentation/corefoundation/cfstringencodings/maccroatian)
- [case macCyrillic](/documentation/corefoundation/cfstringencodings/maccyrillic)
- [case macDevanagari](/documentation/corefoundation/cfstringencodings/macdevanagari)
- [case macDingbats](/documentation/corefoundation/cfstringencodings/macdingbats)
- [case macEthiopic](/documentation/corefoundation/cfstringencodings/macethiopic)
- [case macExtArabic](/documentation/corefoundation/cfstringencodings/macextarabic)
- [case macFarsi](/documentation/corefoundation/cfstringencodings/macfarsi)
- [case macGaelic](/documentation/corefoundation/cfstringencodings/macgaelic)
- [case macGeorgian](/documentation/corefoundation/cfstringencodings/macgeorgian)
- [case macGreek](/documentation/corefoundation/cfstringencodings/macgreek)
- [case macGujarati](/documentation/corefoundation/cfstringencodings/macgujarati)
- [case macGurmukhi](/documentation/corefoundation/cfstringencodings/macgurmukhi)
- [case macHFS](/documentation/corefoundation/cfstringencodings/machfs)
- [case macHebrew](/documentation/corefoundation/cfstringencodings/machebrew)
- [case macIcelandic](/documentation/corefoundation/cfstringencodings/macicelandic)
- [case macInuit](/documentation/corefoundation/cfstringencodings/macinuit)
- [case macJapanese](/documentation/corefoundation/cfstringencodings/macjapanese)
- [case macKannada](/documentation/corefoundation/cfstringencodings/mackannada)
- [case macKhmer](/documentation/corefoundation/cfstringencodings/mackhmer)
- [case macKorean](/documentation/corefoundation/cfstringencodings/mackorean)
- [case macLaotian](/documentation/corefoundation/cfstringencodings/maclaotian)
- [case macMalayalam](/documentation/corefoundation/cfstringencodings/macmalayalam)
- [case macMongolian](/documentation/corefoundation/cfstringencodings/macmongolian)
- [case macOriya](/documentation/corefoundation/cfstringencodings/macoriya)
- [case macRomanLatin1](/documentation/corefoundation/cfstringencodings/macromanlatin1)
- [case macRomanian](/documentation/corefoundation/cfstringencodings/macromanian)
- [case macSinhalese](/documentation/corefoundation/cfstringencodings/macsinhalese)
- [case macSymbol](/documentation/corefoundation/cfstringencodings/macsymbol)
- [case macTamil](/documentation/corefoundation/cfstringencodings/mactamil)
- [case macTelugu](/documentation/corefoundation/cfstringencodings/mactelugu)
- [case macThai](/documentation/corefoundation/cfstringencodings/macthai)
- [case macTibetan](/documentation/corefoundation/cfstringencodings/mactibetan)
- [case macTurkish](/documentation/corefoundation/cfstringencodings/macturkish)
- [case macUkrainian](/documentation/corefoundation/cfstringencodings/macukrainian)
- [case macVT100](/documentation/corefoundation/cfstringencodings/macvt100)
- [case macVietnamese](/documentation/corefoundation/cfstringencodings/macvietnamese)
- [case nextStepJapanese](/documentation/corefoundation/cfstringencodings/nextstepjapanese)
- [case shiftJIS](/documentation/corefoundation/cfstringencodings/shiftjis)
- [case shiftJIS_X0213](/documentation/corefoundation/cfstringencodings/shiftjis_x0213)
- [case shiftJIS_X0213_MenKuTen](/documentation/corefoundation/cfstringencodings/shiftjis_x0213_menkuten)
- [case UTF7](/documentation/corefoundation/cfstringencodings/utf7)
- [case UTF7_IMAP](/documentation/corefoundation/cfstringencodings/utf7_imap)
- [case VISCII](/documentation/corefoundation/cfstringencodings/viscii)
- [case windowsArabic](/documentation/corefoundation/cfstringencodings/windowsarabic)
- [case windowsBalticRim](/documentation/corefoundation/cfstringencodings/windowsbalticrim)
- [case windowsCyrillic](/documentation/corefoundation/cfstringencodings/windowscyrillic)
- [case windowsGreek](/documentation/corefoundation/cfstringencodings/windowsgreek)
- [case windowsHebrew](/documentation/corefoundation/cfstringencodings/windowshebrew)
- [case windowsKoreanJohab](/documentation/corefoundation/cfstringencodings/windowskoreanjohab)
- [case windowsLatin2](/documentation/corefoundation/cfstringencodings/windowslatin2)
- [case windowsLatin5](/documentation/corefoundation/cfstringencodings/windowslatin5)
- [case windowsVietnamese](/documentation/corefoundation/cfstringencodings/windowsvietnamese)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfstringencodings/init(rawvalue:))

#### Type Properties

- [static var shiftJIS_X0213_00: CFStringEncodings](/documentation/corefoundation/cfstringencodings/shiftjis_x0213_00)
- [CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfstringcompareflags/init(rawvalue:))

#### Type Properties

- [static var compareAnchored: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/compareanchored)
- [static var compareBackwards: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparebackwards)
- [static var compareCaseInsensitive: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparecaseinsensitive)
- [static var compareDiacriticInsensitive: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparediacriticinsensitive)
- [static var compareForcedOrdering: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/compareforcedordering)
- [static var compareLocalized: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparelocalized)
- [static var compareNonliteral: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparenonliteral)
- [static var compareNumerically: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparenumerically)
- [static var compareWidthInsensitive: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparewidthinsensitive)
- [CFStringInlineBuffer](/documentation/corefoundation/cfstringinlinebuffer)

#### Initializers

- [init()](/documentation/corefoundation/cfstringinlinebuffer/init())
- [init(buffer: (UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar), theString: Unmanaged<CFString>!, directUniCharBuffer: UnsafePointer<UniChar>!, directCStringBuffer: UnsafePointer<CChar>!, rangeToBuffer: CFRange, bufferedRangeStart: CFIndex, bufferedRangeEnd: CFIndex)](/documentation/corefoundation/cfstringinlinebuffer/init(buffer:thestring:directunicharbuffer:directcstringbuffer:rangetobuffer:bufferedrangestart:bufferedrangeend:))

#### Instance Properties

- [var buffer: (UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar, UniChar)](/documentation/corefoundation/cfstringinlinebuffer/buffer)
- [var bufferedRangeEnd: CFIndex](/documentation/corefoundation/cfstringinlinebuffer/bufferedrangeend)
- [var bufferedRangeStart: CFIndex](/documentation/corefoundation/cfstringinlinebuffer/bufferedrangestart)
- [var directCStringBuffer: UnsafePointer<CChar>!](/documentation/corefoundation/cfstringinlinebuffer/directcstringbuffer)
- [var directUniCharBuffer: UnsafePointer<UniChar>!](/documentation/corefoundation/cfstringinlinebuffer/directunicharbuffer)
- [var rangeToBuffer: CFRange](/documentation/corefoundation/cfstringinlinebuffer/rangetobuffer)
- [var theString: Unmanaged<CFString>!](/documentation/corefoundation/cfstringinlinebuffer/thestring)

### Constants

- [String Comparison Flags](/documentation/corefoundation/string-comparison-flags)

#### Constants

- [static var compareCaseInsensitive: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparecaseinsensitive)
- [static var compareBackwards: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparebackwards)
- [static var compareAnchored: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/compareanchored)
- [static var compareNonliteral: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparenonliteral)
- [static var compareLocalized: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparelocalized)
- [static var compareNumerically: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparenumerically)
- [static var compareDiacriticInsensitive: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparediacriticinsensitive)
- [static var compareWidthInsensitive: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/comparewidthinsensitive)
- [static var compareForcedOrdering: CFStringCompareFlags](/documentation/corefoundation/cfstringcompareflags/compareforcedordering)
- [CFStringBuiltInEncodings](/documentation/corefoundation/cfstringbuiltinencodings)

#### Constants

- [case macRoman](/documentation/corefoundation/cfstringbuiltinencodings/macroman)
- [case windowsLatin1](/documentation/corefoundation/cfstringbuiltinencodings/windowslatin1)
- [case isoLatin1](/documentation/corefoundation/cfstringbuiltinencodings/isolatin1)
- [case nextStepLatin](/documentation/corefoundation/cfstringbuiltinencodings/nextsteplatin)
- [case ASCII](/documentation/corefoundation/cfstringbuiltinencodings/ascii)
- [case unicode](/documentation/corefoundation/cfstringbuiltinencodings/unicode)
- [case UTF8](/documentation/corefoundation/cfstringbuiltinencodings/utf8)
- [case nonLossyASCII](/documentation/corefoundation/cfstringbuiltinencodings/nonlossyascii)
- [static var UTF16: CFStringBuiltInEncodings](/documentation/corefoundation/cfstringbuiltinencodings/utf16)
- [case UTF16BE](/documentation/corefoundation/cfstringbuiltinencodings/utf16be)
- [case UTF16LE](/documentation/corefoundation/cfstringbuiltinencodings/utf16le)
- [case UTF32](/documentation/corefoundation/cfstringbuiltinencodings/utf32)
- [case UTF32BE](/documentation/corefoundation/cfstringbuiltinencodings/utf32be)
- [case UTF32LE](/documentation/corefoundation/cfstringbuiltinencodings/utf32le)

#### Initializers

- [init?(rawValue: CFStringEncoding)](/documentation/corefoundation/cfstringbuiltinencodings/init(rawvalue:))
- [Invalid String Encoding Flag](/documentation/corefoundation/invalid-string-encoding-flag)

#### Constants

- [var kCFStringEncodingInvalidId: UInt32](/documentation/corefoundation/kcfstringencodinginvalidid)
- [External String Encodings](/documentation/corefoundation/external-string-encodings)

#### Constants

- [case macJapanese](/documentation/corefoundation/cfstringencodings/macjapanese)
- [case macChineseTrad](/documentation/corefoundation/cfstringencodings/macchinesetrad)
- [case macKorean](/documentation/corefoundation/cfstringencodings/mackorean)
- [case macArabic](/documentation/corefoundation/cfstringencodings/macarabic)
- [case macHebrew](/documentation/corefoundation/cfstringencodings/machebrew)
- [case macGreek](/documentation/corefoundation/cfstringencodings/macgreek)
- [case macCyrillic](/documentation/corefoundation/cfstringencodings/maccyrillic)
- [case macDevanagari](/documentation/corefoundation/cfstringencodings/macdevanagari)
- [case macGurmukhi](/documentation/corefoundation/cfstringencodings/macgurmukhi)
- [case macGujarati](/documentation/corefoundation/cfstringencodings/macgujarati)
- [case macOriya](/documentation/corefoundation/cfstringencodings/macoriya)
- [case macBengali](/documentation/corefoundation/cfstringencodings/macbengali)
- [case macTamil](/documentation/corefoundation/cfstringencodings/mactamil)
- [case macTelugu](/documentation/corefoundation/cfstringencodings/mactelugu)
- [case macKannada](/documentation/corefoundation/cfstringencodings/mackannada)
- [case macMalayalam](/documentation/corefoundation/cfstringencodings/macmalayalam)
- [case macSinhalese](/documentation/corefoundation/cfstringencodings/macsinhalese)
- [case macBurmese](/documentation/corefoundation/cfstringencodings/macburmese)
- [case macKhmer](/documentation/corefoundation/cfstringencodings/mackhmer)
- [case macThai](/documentation/corefoundation/cfstringencodings/macthai)
- [case macLaotian](/documentation/corefoundation/cfstringencodings/maclaotian)
- [case macGeorgian](/documentation/corefoundation/cfstringencodings/macgeorgian)
- [case macArmenian](/documentation/corefoundation/cfstringencodings/macarmenian)
- [case macChineseSimp](/documentation/corefoundation/cfstringencodings/macchinesesimp)
- [case macTibetan](/documentation/corefoundation/cfstringencodings/mactibetan)
- [case macMongolian](/documentation/corefoundation/cfstringencodings/macmongolian)
- [case macEthiopic](/documentation/corefoundation/cfstringencodings/macethiopic)
- [case macCentralEurRoman](/documentation/corefoundation/cfstringencodings/maccentraleurroman)
- [case macVietnamese](/documentation/corefoundation/cfstringencodings/macvietnamese)
- [case macExtArabic](/documentation/corefoundation/cfstringencodings/macextarabic)
- [case macSymbol](/documentation/corefoundation/cfstringencodings/macsymbol)
- [case macDingbats](/documentation/corefoundation/cfstringencodings/macdingbats)
- [case macTurkish](/documentation/corefoundation/cfstringencodings/macturkish)
- [case macCroatian](/documentation/corefoundation/cfstringencodings/maccroatian)
- [case macIcelandic](/documentation/corefoundation/cfstringencodings/macicelandic)
- [case macRomanian](/documentation/corefoundation/cfstringencodings/macromanian)
- [case macCeltic](/documentation/corefoundation/cfstringencodings/macceltic)
- [case macGaelic](/documentation/corefoundation/cfstringencodings/macgaelic)
- [case macFarsi](/documentation/corefoundation/cfstringencodings/macfarsi)
- [case macUkrainian](/documentation/corefoundation/cfstringencodings/macukrainian)
- [case macInuit](/documentation/corefoundation/cfstringencodings/macinuit)
- [case macVT100](/documentation/corefoundation/cfstringencodings/macvt100)
- [case macHFS](/documentation/corefoundation/cfstringencodings/machfs)
- [case isoLatin2](/documentation/corefoundation/cfstringencodings/isolatin2)
- [case isoLatin3](/documentation/corefoundation/cfstringencodings/isolatin3)
- [case isoLatin4](/documentation/corefoundation/cfstringencodings/isolatin4)
- [case isoLatinCyrillic](/documentation/corefoundation/cfstringencodings/isolatincyrillic)
- [case isoLatinArabic](/documentation/corefoundation/cfstringencodings/isolatinarabic)
- [case isoLatinGreek](/documentation/corefoundation/cfstringencodings/isolatingreek)
- [case isoLatinHebrew](/documentation/corefoundation/cfstringencodings/isolatinhebrew)
- [case isoLatin5](/documentation/corefoundation/cfstringencodings/isolatin5)
- [case isoLatin6](/documentation/corefoundation/cfstringencodings/isolatin6)
- [case isoLatinThai](/documentation/corefoundation/cfstringencodings/isolatinthai)
- [case isoLatin7](/documentation/corefoundation/cfstringencodings/isolatin7)
- [case isoLatin8](/documentation/corefoundation/cfstringencodings/isolatin8)
- [case isoLatin9](/documentation/corefoundation/cfstringencodings/isolatin9)
- [case isoLatin10](/documentation/corefoundation/cfstringencodings/isolatin10)
- [case dosLatinUS](/documentation/corefoundation/cfstringencodings/doslatinus)
- [case dosGreek](/documentation/corefoundation/cfstringencodings/dosgreek)
- [case dosBalticRim](/documentation/corefoundation/cfstringencodings/dosbalticrim)
- [case dosLatin1](/documentation/corefoundation/cfstringencodings/doslatin1)
- [case dosGreek1](/documentation/corefoundation/cfstringencodings/dosgreek1)
- [case dosLatin2](/documentation/corefoundation/cfstringencodings/doslatin2)
- [case dosCyrillic](/documentation/corefoundation/cfstringencodings/doscyrillic)
- [case dosTurkish](/documentation/corefoundation/cfstringencodings/dosturkish)
- [case dosPortuguese](/documentation/corefoundation/cfstringencodings/dosportuguese)
- [case dosIcelandic](/documentation/corefoundation/cfstringencodings/dosicelandic)
- [case dosHebrew](/documentation/corefoundation/cfstringencodings/doshebrew)
- [case dosCanadianFrench](/documentation/corefoundation/cfstringencodings/doscanadianfrench)
- [case dosArabic](/documentation/corefoundation/cfstringencodings/dosarabic)
- [case dosNordic](/documentation/corefoundation/cfstringencodings/dosnordic)
- [case dosRussian](/documentation/corefoundation/cfstringencodings/dosrussian)
- [case dosGreek2](/documentation/corefoundation/cfstringencodings/dosgreek2)
- [case dosThai](/documentation/corefoundation/cfstringencodings/dosthai)
- [case dosJapanese](/documentation/corefoundation/cfstringencodings/dosjapanese)
- [case dosChineseSimplif](/documentation/corefoundation/cfstringencodings/doschinesesimplif)
- [case dosKorean](/documentation/corefoundation/cfstringencodings/doskorean)
- [case dosChineseTrad](/documentation/corefoundation/cfstringencodings/doschinesetrad)
- [case windowsLatin2](/documentation/corefoundation/cfstringencodings/windowslatin2)
- [case windowsCyrillic](/documentation/corefoundation/cfstringencodings/windowscyrillic)
- [case windowsGreek](/documentation/corefoundation/cfstringencodings/windowsgreek)
- [case windowsLatin5](/documentation/corefoundation/cfstringencodings/windowslatin5)
- [case windowsHebrew](/documentation/corefoundation/cfstringencodings/windowshebrew)
- [case windowsArabic](/documentation/corefoundation/cfstringencodings/windowsarabic)
- [case windowsBalticRim](/documentation/corefoundation/cfstringencodings/windowsbalticrim)
- [case windowsVietnamese](/documentation/corefoundation/cfstringencodings/windowsvietnamese)
- [case windowsKoreanJohab](/documentation/corefoundation/cfstringencodings/windowskoreanjohab)
- [case ANSEL](/documentation/corefoundation/cfstringencodings/ansel)
- [case JIS_X0201_76](/documentation/corefoundation/cfstringencodings/jis_x0201_76)
- [case JIS_X0208_83](/documentation/corefoundation/cfstringencodings/jis_x0208_83)
- [case JIS_X0208_90](/documentation/corefoundation/cfstringencodings/jis_x0208_90)
- [case JIS_X0212_90](/documentation/corefoundation/cfstringencodings/jis_x0212_90)
- [case JIS_C6226_78](/documentation/corefoundation/cfstringencodings/jis_c6226_78)
- [case shiftJIS_X0213](/documentation/corefoundation/cfstringencodings/shiftjis_x0213)
- [case shiftJIS_X0213_MenKuTen](/documentation/corefoundation/cfstringencodings/shiftjis_x0213_menkuten)
- [case GB_2312_80](/documentation/corefoundation/cfstringencodings/gb_2312_80)
- [case GBK_95](/documentation/corefoundation/cfstringencodings/gbk_95)
- [case GB_18030_2000](/documentation/corefoundation/cfstringencodings/gb_18030_2000)
- [case KSC_5601_87](/documentation/corefoundation/cfstringencodings/ksc_5601_87)
- [case ksc_5601_92_Johab](/documentation/corefoundation/cfstringencodings/ksc_5601_92_johab)
- [case CNS_11643_92_P1](/documentation/corefoundation/cfstringencodings/cns_11643_92_p1)
- [case CNS_11643_92_P2](/documentation/corefoundation/cfstringencodings/cns_11643_92_p2)
- [case CNS_11643_92_P3](/documentation/corefoundation/cfstringencodings/cns_11643_92_p3)
- [case ISO_2022_JP](/documentation/corefoundation/cfstringencodings/iso_2022_jp)
- [case ISO_2022_JP_2](/documentation/corefoundation/cfstringencodings/iso_2022_jp_2)
- [case ISO_2022_JP_1](/documentation/corefoundation/cfstringencodings/iso_2022_jp_1)
- [case ISO_2022_JP_3](/documentation/corefoundation/cfstringencodings/iso_2022_jp_3)
- [case ISO_2022_CN](/documentation/corefoundation/cfstringencodings/iso_2022_cn)
- [case ISO_2022_CN_EXT](/documentation/corefoundation/cfstringencodings/iso_2022_cn_ext)
- [case ISO_2022_KR](/documentation/corefoundation/cfstringencodings/iso_2022_kr)
- [case EUC_JP](/documentation/corefoundation/cfstringencodings/euc_jp)
- [case EUC_CN](/documentation/corefoundation/cfstringencodings/euc_cn)
- [case EUC_TW](/documentation/corefoundation/cfstringencodings/euc_tw)
- [case EUC_KR](/documentation/corefoundation/cfstringencodings/euc_kr)
- [case shiftJIS](/documentation/corefoundation/cfstringencodings/shiftjis)
- [case KOI8_R](/documentation/corefoundation/cfstringencodings/koi8_r)
- [case big5](/documentation/corefoundation/cfstringencodings/big5)
- [case macRomanLatin1](/documentation/corefoundation/cfstringencodings/macromanlatin1)
- [case HZ_GB_2312](/documentation/corefoundation/cfstringencodings/hz_gb_2312)
- [case big5_HKSCS_1999](/documentation/corefoundation/cfstringencodings/big5_hkscs_1999)
- [case VISCII](/documentation/corefoundation/cfstringencodings/viscii)
- [case KOI8_U](/documentation/corefoundation/cfstringencodings/koi8_u)
- [case big5_E](/documentation/corefoundation/cfstringencodings/big5_e)
- [case nextStepJapanese](/documentation/corefoundation/cfstringencodings/nextstepjapanese)
- [case EBCDIC_US](/documentation/corefoundation/cfstringencodings/ebcdic_us)
- [case EBCDIC_CP037](/documentation/corefoundation/cfstringencodings/ebcdic_cp037)
- [case UTF7](/documentation/corefoundation/cfstringencodings/utf7)
- [case UTF7_IMAP](/documentation/corefoundation/cfstringencodings/utf7_imap)
- [static var shiftJIS_X0213_00: CFStringEncodings](/documentation/corefoundation/cfstringencodings/shiftjis_x0213_00)
- [CFStringTokenizer](/documentation/corefoundation/cfstringtokenizer)

### Creating a Tokenizer

- [func CFStringTokenizerCreate(CFAllocator!, CFString!, CFRange, CFOptionFlags, CFLocale!) -> CFStringTokenizer!](/documentation/corefoundation/cfstringtokenizercreate(_:_:_:_:_:))

### Setting the String

- [func CFStringTokenizerSetString(CFStringTokenizer!, CFString!, CFRange)](/documentation/corefoundation/cfstringtokenizersetstring(_:_:_:))

### Changing the Location

- [func CFStringTokenizerAdvanceToNextToken(CFStringTokenizer!) -> CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizeradvancetonexttoken(_:))
- [func CFStringTokenizerGoToTokenAtIndex(CFStringTokenizer!, CFIndex) -> CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizergototokenatindex(_:_:))

### Getting Information About the Current Token

- [func CFStringTokenizerCopyCurrentTokenAttribute(CFStringTokenizer!, CFOptionFlags) -> CFTypeRef!](/documentation/corefoundation/cfstringtokenizercopycurrenttokenattribute(_:_:))
- [func CFStringTokenizerGetCurrentTokenRange(CFStringTokenizer!) -> CFRange](/documentation/corefoundation/cfstringtokenizergetcurrenttokenrange(_:))
- [func CFStringTokenizerGetCurrentSubTokens(CFStringTokenizer!, UnsafeMutablePointer<CFRange>!, CFIndex, CFMutableArray!) -> CFIndex](/documentation/corefoundation/cfstringtokenizergetcurrentsubtokens(_:_:_:_:))

### Identifying a Language

- [func CFStringTokenizerCopyBestStringLanguage(CFString!, CFRange) -> CFString!](/documentation/corefoundation/cfstringtokenizercopybeststringlanguage(_:_:))

### Getting the CFStringTokenizer Type ID

- [func CFStringTokenizerGetTypeID() -> CFTypeID](/documentation/corefoundation/cfstringtokenizergettypeid())

### Constants

- [Tokenization Modifiers](/documentation/corefoundation/1588024-tokenization-modifiers)

#### Constants

- [var kCFStringTokenizerUnitWord: CFOptionFlags](/documentation/corefoundation/kcfstringtokenizerunitword)
- [var kCFStringTokenizerUnitSentence: CFOptionFlags](/documentation/corefoundation/kcfstringtokenizerunitsentence)
- [var kCFStringTokenizerUnitParagraph: CFOptionFlags](/documentation/corefoundation/kcfstringtokenizerunitparagraph)
- [var kCFStringTokenizerUnitLineBreak: CFOptionFlags](/documentation/corefoundation/kcfstringtokenizerunitlinebreak)
- [var kCFStringTokenizerUnitWordBoundary: CFOptionFlags](/documentation/corefoundation/kcfstringtokenizerunitwordboundary)
- [var kCFStringTokenizerAttributeLatinTranscription: CFOptionFlags](/documentation/corefoundation/kcfstringtokenizerattributelatintranscription)
- [var kCFStringTokenizerAttributeLanguage: CFOptionFlags](/documentation/corefoundation/kcfstringtokenizerattributelanguage)
- [CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizertokentype)

#### Constants

- [static var normal: CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizertokentype/normal)
- [static var hasSubTokensMask: CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizertokentype/hassubtokensmask)
- [static var hasDerivedSubTokensMask: CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizertokentype/hasderivedsubtokensmask)
- [static var hasHasNumbersMask: CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizertokentype/hashasnumbersmask)
- [static var hasNonLettersMask: CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizertokentype/hasnonlettersmask)
- [static var isCJWordMask: CFStringTokenizerTokenType](/documentation/corefoundation/cfstringtokenizertokentype/iscjwordmask)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfstringtokenizertokentype/init(rawvalue:))
- [CFTimeZone](/documentation/corefoundation/cftimezone)

### Creating a Time Zone

- [func CFTimeZoneCreateWithName(CFAllocator!, CFString!, Bool) -> CFTimeZone!](/documentation/corefoundation/cftimezonecreatewithname(_:_:_:))
- [func CFTimeZoneCreateWithTimeIntervalFromGMT(CFAllocator!, CFTimeInterval) -> CFTimeZone!](/documentation/corefoundation/cftimezonecreatewithtimeintervalfromgmt(_:_:))
- [func CFTimeZoneCreate(CFAllocator!, CFString!, CFData!) -> CFTimeZone!](/documentation/corefoundation/cftimezonecreate(_:_:_:))

### System and Default Time Zones and Information

- [func CFTimeZoneCopyAbbreviationDictionary() -> CFDictionary!](/documentation/corefoundation/cftimezonecopyabbreviationdictionary())
- [func CFTimeZoneCopyAbbreviation(CFTimeZone!, CFAbsoluteTime) -> CFString!](/documentation/corefoundation/cftimezonecopyabbreviation(_:_:))
- [func CFTimeZoneCopyDefault() -> CFTimeZone!](/documentation/corefoundation/cftimezonecopydefault())
- [func CFTimeZoneCopySystem() -> CFTimeZone!](/documentation/corefoundation/cftimezonecopysystem())
- [func CFTimeZoneSetDefault(CFTimeZone!)](/documentation/corefoundation/cftimezonesetdefault(_:))
- [func CFTimeZoneCopyKnownNames() -> CFArray!](/documentation/corefoundation/cftimezonecopyknownnames())
- [func CFTimeZoneResetSystem()](/documentation/corefoundation/cftimezoneresetsystem())
- [func CFTimeZoneSetAbbreviationDictionary(CFDictionary!)](/documentation/corefoundation/cftimezonesetabbreviationdictionary(_:))

### Getting Information About Time Zones

- [func CFTimeZoneGetName(CFTimeZone!) -> CFString!](/documentation/corefoundation/cftimezonegetname(_:))
- [func CFTimeZoneCopyLocalizedName(CFTimeZone!, CFTimeZoneNameStyle, CFLocale!) -> CFString!](/documentation/corefoundation/cftimezonecopylocalizedname(_:_:_:))
- [func CFTimeZoneGetSecondsFromGMT(CFTimeZone!, CFAbsoluteTime) -> CFTimeInterval](/documentation/corefoundation/cftimezonegetsecondsfromgmt(_:_:))
- [func CFTimeZoneGetData(CFTimeZone!) -> CFData!](/documentation/corefoundation/cftimezonegetdata(_:))

### Getting Daylight Savings Time Information

- [func CFTimeZoneIsDaylightSavingTime(CFTimeZone!, CFAbsoluteTime) -> Bool](/documentation/corefoundation/cftimezoneisdaylightsavingtime(_:_:))
- [func CFTimeZoneGetDaylightSavingTimeOffset(CFTimeZone!, CFAbsoluteTime) -> CFTimeInterval](/documentation/corefoundation/cftimezonegetdaylightsavingtimeoffset(_:_:))
- [func CFTimeZoneGetNextDaylightSavingTimeTransition(CFTimeZone!, CFAbsoluteTime) -> CFAbsoluteTime](/documentation/corefoundation/cftimezonegetnextdaylightsavingtimetransition(_:_:))

### Getting the CFTimeZone Type ID

- [func CFTimeZoneGetTypeID() -> CFTypeID](/documentation/corefoundation/cftimezonegettypeid())

### Data Types

- [CFTimeZoneNameStyle](/documentation/corefoundation/cftimezonenamestyle)

#### Enumeration Cases

- [case daylightSaving](/documentation/corefoundation/cftimezonenamestyle/daylightsaving)
- [case generic](/documentation/corefoundation/cftimezonenamestyle/generic)
- [case shortDaylightSaving](/documentation/corefoundation/cftimezonenamestyle/shortdaylightsaving)
- [case shortGeneric](/documentation/corefoundation/cftimezonenamestyle/shortgeneric)
- [case shortStandard](/documentation/corefoundation/cftimezonenamestyle/shortstandard)
- [case standard](/documentation/corefoundation/cftimezonenamestyle/standard)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cftimezonenamestyle/init(rawvalue:))

### Constants

- [Notification Name](/documentation/corefoundation/notification-name)

#### Constants

- [static let cfTimeZoneSystemTimeZoneDidChange: CFNotificationName!](/documentation/corefoundation/cfnotificationname/cftimezonesystemtimezonedidchange)
- [Time Zone Name Styles](/documentation/corefoundation/time_zone_name_styles)

#### Constants

- [case standard](/documentation/corefoundation/cftimezonenamestyle/standard)
- [case shortStandard](/documentation/corefoundation/cftimezonenamestyle/shortstandard)
- [case daylightSaving](/documentation/corefoundation/cftimezonenamestyle/daylightsaving)
- [case shortDaylightSaving](/documentation/corefoundation/cftimezonenamestyle/shortdaylightsaving)
- [case generic](/documentation/corefoundation/cftimezonenamestyle/generic)
- [case shortGeneric](/documentation/corefoundation/cftimezonenamestyle/shortgeneric)
- [CFTree](/documentation/corefoundation/cftree)

### Creating Trees

- [func CFTreeCreate(CFAllocator!, UnsafePointer<CFTreeContext>!) -> CFTree!](/documentation/corefoundation/cftreecreate(_:_:))

### Modifying a Tree

- [func CFTreeAppendChild(CFTree!, CFTree!)](/documentation/corefoundation/cftreeappendchild(_:_:))
- [func CFTreeInsertSibling(CFTree!, CFTree!)](/documentation/corefoundation/cftreeinsertsibling(_:_:))
- [func CFTreeRemoveAllChildren(CFTree!)](/documentation/corefoundation/cftreeremoveallchildren(_:))
- [func CFTreePrependChild(CFTree!, CFTree!)](/documentation/corefoundation/cftreeprependchild(_:_:))
- [func CFTreeRemove(CFTree!)](/documentation/corefoundation/cftreeremove(_:))
- [func CFTreeSetContext(CFTree!, UnsafePointer<CFTreeContext>!)](/documentation/corefoundation/cftreesetcontext(_:_:))

### Sorting a Tree

- [func CFTreeSortChildren(CFTree!, CFComparatorFunction!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cftreesortchildren(_:_:_:))

### Examining a Tree

- [func CFTreeFindRoot(CFTree!) -> CFTree!](/documentation/corefoundation/cftreefindroot(_:))
- [func CFTreeGetChildAtIndex(CFTree!, CFIndex) -> CFTree!](/documentation/corefoundation/cftreegetchildatindex(_:_:))
- [func CFTreeGetChildCount(CFTree!) -> CFIndex](/documentation/corefoundation/cftreegetchildcount(_:))
- [func CFTreeGetChildren(CFTree!, UnsafeMutablePointer<Unmanaged<CFTree>?>!)](/documentation/corefoundation/cftreegetchildren(_:_:))
- [func CFTreeGetContext(CFTree!, UnsafeMutablePointer<CFTreeContext>!)](/documentation/corefoundation/cftreegetcontext(_:_:))
- [func CFTreeGetFirstChild(CFTree!) -> CFTree!](/documentation/corefoundation/cftreegetfirstchild(_:))
- [func CFTreeGetNextSibling(CFTree!) -> CFTree!](/documentation/corefoundation/cftreegetnextsibling(_:))
- [func CFTreeGetParent(CFTree!) -> CFTree!](/documentation/corefoundation/cftreegetparent(_:))

### Performing an Operation on Tree Elements

- [func CFTreeApplyFunctionToChildren(CFTree!, ((UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void)!, UnsafeMutableRawPointer!)](/documentation/corefoundation/cftreeapplyfunctiontochildren(_:_:_:))

### Getting the Tree Type ID

- [func CFTreeGetTypeID() -> CFTypeID](/documentation/corefoundation/cftreegettypeid())

### Callbacks

- [CFTreeApplierFunction](/documentation/corefoundation/cftreeapplierfunction)
- [CFTreeCopyDescriptionCallBack](/documentation/corefoundation/cftreecopydescriptioncallback)
- [CFTreeReleaseCallBack](/documentation/corefoundation/cftreereleasecallback)
- [CFTreeRetainCallBack](/documentation/corefoundation/cftreeretaincallback)

### Data Types

- [CFTreeContext](/documentation/corefoundation/cftreecontext)

#### Initializers

- [init()](/documentation/corefoundation/cftreecontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: CFTreeRetainCallBack!, release: CFTreeReleaseCallBack!, copyDescription: CFTreeCopyDescriptionCallBack!)](/documentation/corefoundation/cftreecontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: CFTreeCopyDescriptionCallBack!](/documentation/corefoundation/cftreecontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cftreecontext/info)
- [var release: CFTreeReleaseCallBack!](/documentation/corefoundation/cftreecontext/release)
- [var retain: CFTreeRetainCallBack!](/documentation/corefoundation/cftreecontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cftreecontext/version)
- [CFURL](/documentation/corefoundation/cfurl)

### Creating a CFURL

- [func CFURLCopyAbsoluteURL(CFURL!) -> CFURL!](/documentation/corefoundation/cfurlcopyabsoluteurl(_:))
- [func CFURLCreateAbsoluteURLWithBytes(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, CFStringEncoding, CFURL!, Bool) -> CFURL!](/documentation/corefoundation/cfurlcreateabsoluteurlwithbytes(_:_:_:_:_:_:))
- [func CFURLCreateByResolvingBookmarkData(CFAllocator!, CFData!, CFURLBookmarkResolutionOptions, CFURL!, CFArray!, UnsafeMutablePointer<DarwinBoolean>!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFURL>!](/documentation/corefoundation/cfurlcreatebyresolvingbookmarkdata(_:_:_:_:_:_:_:))
- [func CFURLCreateCopyAppendingPathComponent(CFAllocator!, CFURL!, CFString!, Bool) -> CFURL!](/documentation/corefoundation/cfurlcreatecopyappendingpathcomponent(_:_:_:_:))
- [func CFURLCreateCopyAppendingPathExtension(CFAllocator!, CFURL!, CFString!) -> CFURL!](/documentation/corefoundation/cfurlcreatecopyappendingpathextension(_:_:_:))
- [func CFURLCreateCopyDeletingLastPathComponent(CFAllocator!, CFURL!) -> CFURL!](/documentation/corefoundation/cfurlcreatecopydeletinglastpathcomponent(_:_:))
- [func CFURLCreateCopyDeletingPathExtension(CFAllocator!, CFURL!) -> CFURL!](/documentation/corefoundation/cfurlcreatecopydeletingpathextension(_:_:))
- [func CFURLCreateFilePathURL(CFAllocator!, CFURL!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFURL>!](/documentation/corefoundation/cfurlcreatefilepathurl(_:_:_:))
- [func CFURLCreateFileReferenceURL(CFAllocator!, CFURL!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFURL>!](/documentation/corefoundation/cfurlcreatefilereferenceurl(_:_:_:))
- [func CFURLCreateFromFileSystemRepresentation(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, Bool) -> CFURL!](/documentation/corefoundation/cfurlcreatefromfilesystemrepresentation(_:_:_:_:))
- [func CFURLCreateFromFileSystemRepresentationRelativeToBase(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, Bool, CFURL!) -> CFURL!](/documentation/corefoundation/cfurlcreatefromfilesystemrepresentationrelativetobase(_:_:_:_:_:))
- [func CFURLCreateFromFSRef(CFAllocator!, OpaquePointer!) -> CFURL!](/documentation/corefoundation/cfurlcreatefromfsref(_:_:))
- [func CFURLCreateWithBytes(CFAllocator!, UnsafePointer<UInt8>!, CFIndex, CFStringEncoding, CFURL!) -> CFURL!](/documentation/corefoundation/cfurlcreatewithbytes(_:_:_:_:_:))
- [func CFURLCreateWithFileSystemPath(CFAllocator!, CFString!, CFURLPathStyle, Bool) -> CFURL!](/documentation/corefoundation/cfurlcreatewithfilesystempath(_:_:_:_:))
- [func CFURLCreateWithFileSystemPathRelativeToBase(CFAllocator!, CFString!, CFURLPathStyle, Bool, CFURL!) -> CFURL!](/documentation/corefoundation/cfurlcreatewithfilesystempathrelativetobase(_:_:_:_:_:))
- [func CFURLCreateWithString(CFAllocator!, CFString!, CFURL!) -> CFURL!](/documentation/corefoundation/cfurlcreatewithstring(_:_:_:))

### Accessing the Parts of a URL

- [func CFURLCanBeDecomposed(CFURL!) -> Bool](/documentation/corefoundation/cfurlcanbedecomposed(_:))
- [func CFURLCopyFileSystemPath(CFURL!, CFURLPathStyle) -> CFString!](/documentation/corefoundation/cfurlcopyfilesystempath(_:_:))
- [func CFURLCopyFragment(CFURL!, CFString!) -> CFString!](/documentation/corefoundation/cfurlcopyfragment(_:_:))
- [func CFURLCopyHostName(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopyhostname(_:))
- [func CFURLCopyLastPathComponent(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopylastpathcomponent(_:))
- [func CFURLCopyNetLocation(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopynetlocation(_:))
- [func CFURLCopyParameterString(CFURL!, CFString!) -> CFString!](/documentation/corefoundation/cfurlcopyparameterstring(_:_:))
- [func CFURLCopyPassword(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopypassword(_:))
- [func CFURLCopyPath(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopypath(_:))
- [func CFURLCopyPathExtension(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopypathextension(_:))
- [func CFURLCopyQueryString(CFURL!, CFString!) -> CFString!](/documentation/corefoundation/cfurlcopyquerystring(_:_:))
- [func CFURLCopyResourceSpecifier(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopyresourcespecifier(_:))
- [func CFURLCopyScheme(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopyscheme(_:))
- [func CFURLCopyStrictPath(CFURL!, UnsafeMutablePointer<DarwinBoolean>!) -> CFString!](/documentation/corefoundation/cfurlcopystrictpath(_:_:))
- [func CFURLCopyUserName(CFURL!) -> CFString!](/documentation/corefoundation/cfurlcopyusername(_:))
- [func CFURLGetPortNumber(CFURL!) -> Int32](/documentation/corefoundation/cfurlgetportnumber(_:))
- [func CFURLHasDirectoryPath(CFURL!) -> Bool](/documentation/corefoundation/cfurlhasdirectorypath(_:))

### Converting URLs to Other Representations

- [func CFURLCreateData(CFAllocator!, CFURL!, CFStringEncoding, Bool) -> CFData!](/documentation/corefoundation/cfurlcreatedata(_:_:_:_:))
- [func CFURLCreateStringByAddingPercentEscapes(CFAllocator!, CFString!, CFString!, CFString!, CFStringEncoding) -> CFString!](/documentation/corefoundation/cfurlcreatestringbyaddingpercentescapes(_:_:_:_:_:))
- [func CFURLCreateStringByReplacingPercentEscapes(CFAllocator!, CFString!, CFString!) -> CFString!](/documentation/corefoundation/cfurlcreatestringbyreplacingpercentescapes(_:_:_:))
- [func CFURLCreateStringByReplacingPercentEscapesUsingEncoding(CFAllocator!, CFString!, CFString!, CFStringEncoding) -> CFString!](/documentation/corefoundation/cfurlcreatestringbyreplacingpercentescapesusingencoding(_:_:_:_:))
- [func CFURLGetFileSystemRepresentation(CFURL!, Bool, UnsafeMutablePointer<UInt8>!, CFIndex) -> Bool](/documentation/corefoundation/cfurlgetfilesystemrepresentation(_:_:_:_:))
- [func CFURLGetFSRef(CFURL!, OpaquePointer!) -> Bool](/documentation/corefoundation/cfurlgetfsref(_:_:))
- [func CFURLGetString(CFURL!) -> CFString!](/documentation/corefoundation/cfurlgetstring(_:))

### Getting URL Properties

- [func CFURLGetBaseURL(CFURL!) -> CFURL!](/documentation/corefoundation/cfurlgetbaseurl(_:))
- [func CFURLGetBytes(CFURL!, UnsafeMutablePointer<UInt8>!, CFIndex) -> CFIndex](/documentation/corefoundation/cfurlgetbytes(_:_:_:))
- [func CFURLGetByteRangeForComponent(CFURL!, CFURLComponentType, UnsafeMutablePointer<CFRange>!) -> CFRange](/documentation/corefoundation/cfurlgetbyterangeforcomponent(_:_:_:))
- [func CFURLGetTypeID() -> CFTypeID](/documentation/corefoundation/cfurlgettypeid())
- [func CFURLResourceIsReachable(CFURL!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/corefoundation/cfurlresourceisreachable(_:_:))

### Getting and Setting File System Resource Properties

- [func CFURLClearResourcePropertyCache(CFURL!)](/documentation/corefoundation/cfurlclearresourcepropertycache(_:))
- [func CFURLClearResourcePropertyCacheForKey(CFURL!, CFString!)](/documentation/corefoundation/cfurlclearresourcepropertycacheforkey(_:_:))
- [func CFURLCopyResourcePropertiesForKeys(CFURL!, CFArray!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFDictionary>!](/documentation/corefoundation/cfurlcopyresourcepropertiesforkeys(_:_:_:))
- [func CFURLCopyResourcePropertyForKey(CFURL!, CFString!, UnsafeMutableRawPointer!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/corefoundation/cfurlcopyresourcepropertyforkey(_:_:_:_:))
- [func CFURLCreateResourcePropertiesForKeysFromBookmarkData(CFAllocator!, CFArray!, CFData!) -> Unmanaged<CFDictionary>!](/documentation/corefoundation/cfurlcreateresourcepropertiesforkeysfrombookmarkdata(_:_:_:))
- [func CFURLCreateResourcePropertyForKeyFromBookmarkData(CFAllocator!, CFString!, CFData!) -> Unmanaged<CFTypeRef>!](/documentation/corefoundation/cfurlcreateresourcepropertyforkeyfrombookmarkdata(_:_:_:))
- [func CFURLSetResourcePropertiesForKeys(CFURL!, CFDictionary!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/corefoundation/cfurlsetresourcepropertiesforkeys(_:_:_:))
- [func CFURLSetResourcePropertyForKey(CFURL!, CFString!, CFTypeRef!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/corefoundation/cfurlsetresourcepropertyforkey(_:_:_:_:))
- [func CFURLSetTemporaryResourcePropertyForKey(CFURL!, CFString!, CFTypeRef!)](/documentation/corefoundation/cfurlsettemporaryresourcepropertyforkey(_:_:_:))

### Working with Bookmark Data

- [func CFURLCreateBookmarkData(CFAllocator!, CFURL!, CFURLBookmarkCreationOptions, CFArray!, CFURL!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFData>!](/documentation/corefoundation/cfurlcreatebookmarkdata(_:_:_:_:_:_:))
- [func CFURLCreateBookmarkDataFromAliasRecord(CFAllocator!, CFData!) -> Unmanaged<CFData>!](/documentation/corefoundation/cfurlcreatebookmarkdatafromaliasrecord(_:_:))
- [func CFURLCreateBookmarkDataFromFile(CFAllocator!, CFURL!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<CFData>!](/documentation/corefoundation/cfurlcreatebookmarkdatafromfile(_:_:_:))
- [func CFURLWriteBookmarkDataToFile(CFData!, CFURL!, CFURLBookmarkFileCreationOptions, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/corefoundation/cfurlwritebookmarkdatatofile(_:_:_:_:))
- [func CFURLStartAccessingSecurityScopedResource(CFURL!) -> Bool](/documentation/corefoundation/cfurlstartaccessingsecurityscopedresource(_:))
- [func CFURLStopAccessingSecurityScopedResource(CFURL!)](/documentation/corefoundation/cfurlstopaccessingsecurityscopedresource(_:))

### Bookmark Data Types

- [CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfurlbookmarkcreationoptions/init(rawvalue:))

#### Type Properties

- [static var minimalBookmarkMask: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/minimalbookmarkmask)
- [static var preferFileIDResolutionMask: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/preferfileidresolutionmask)
- [static var securityScopeAllowOnlyReadAccess: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/securityscopeallowonlyreadaccess)
- [static var suitableForBookmarkFile: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/suitableforbookmarkfile)
- [static var withSecurityScope: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/withsecurityscope)
- [static var withoutImplicitSecurityScope: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/withoutimplicitsecurityscope)
- [CFURLBookmarkFileCreationOptions](/documentation/corefoundation/cfurlbookmarkfilecreationoptions)
- [CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfurlbookmarkresolutionoptions/init(rawvalue:))

#### Type Properties

- [static var cfBookmarkResolutionWithoutMountingMask: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfbookmarkresolutionwithoutmountingmask)
- [static var cfBookmarkResolutionWithoutUIMask: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfbookmarkresolutionwithoutuimask)
- [static var cfurlBookmarkResolutionWithSecurityScope: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfurlbookmarkresolutionwithsecurityscope)
- [static var cfurlBookmarkResolutionWithoutImplicitStartAccessing: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfurlbookmarkresolutionwithoutimplicitstartaccessing)
- [static var cfurlBookmarkResolutionWithoutMountingMask: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfurlbookmarkresolutionwithoutmountingmask)
- [static var cfurlBookmarkResolutionWithoutUIMask: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfurlbookmarkresolutionwithoutuimask)

### Bookmark Data Constants

- [Bookmark Data Creation Options](/documentation/corefoundation/bookmark-data-creation-options)

#### Constants

- [static var preferFileIDResolutionMask: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/preferfileidresolutionmask)
- [static var minimalBookmarkMask: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/minimalbookmarkmask)
- [static var suitableForBookmarkFile: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/suitableforbookmarkfile)
- [static var withSecurityScope: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/withsecurityscope)
- [static var securityScopeAllowOnlyReadAccess: CFURLBookmarkCreationOptions](/documentation/corefoundation/cfurlbookmarkcreationoptions/securityscopeallowonlyreadaccess)
- [Bookmark Data Resolution Options](/documentation/corefoundation/bookmark-data-resolution-options)

#### Constants

- [static var cfBookmarkResolutionWithoutUIMask: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfbookmarkresolutionwithoutuimask)
- [static var cfBookmarkResolutionWithoutMountingMask: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfbookmarkresolutionwithoutmountingmask)
- [static var cfurlBookmarkResolutionWithSecurityScope: CFURLBookmarkResolutionOptions](/documentation/corefoundation/cfurlbookmarkresolutionoptions/cfurlbookmarkresolutionwithsecurityscope)

### File System Constants

- [Common File System Resource Keys](/documentation/corefoundation/common-file-system-resource-keys)

#### Constants

- [let kCFURLNameKey: CFString!](/documentation/corefoundation/kcfurlnamekey)
- [let kCFURLLocalizedNameKey: CFString!](/documentation/corefoundation/kcfurllocalizednamekey)
- [let kCFURLPathKey: CFString!](/documentation/corefoundation/kcfurlpathkey)
- [let kCFURLIsRegularFileKey: CFString!](/documentation/corefoundation/kcfurlisregularfilekey)
- [let kCFURLIsDirectoryKey: CFString!](/documentation/corefoundation/kcfurlisdirectorykey)
- [let kCFURLIsSymbolicLinkKey: CFString!](/documentation/corefoundation/kcfurlissymboliclinkkey)
- [let kCFURLIsVolumeKey: CFString!](/documentation/corefoundation/kcfurlisvolumekey)
- [let kCFURLIsPackageKey: CFString!](/documentation/corefoundation/kcfurlispackagekey)
- [let kCFURLIsSystemImmutableKey: CFString!](/documentation/corefoundation/kcfurlissystemimmutablekey)
- [let kCFURLIsUserImmutableKey: CFString!](/documentation/corefoundation/kcfurlisuserimmutablekey)
- [let kCFURLIsHiddenKey: CFString!](/documentation/corefoundation/kcfurlishiddenkey)
- [let kCFURLHasHiddenExtensionKey: CFString!](/documentation/corefoundation/kcfurlhashiddenextensionkey)
- [let kCFURLCreationDateKey: CFString!](/documentation/corefoundation/kcfurlcreationdatekey)
- [let kCFURLContentAccessDateKey: CFString!](/documentation/corefoundation/kcfurlcontentaccessdatekey)
- [let kCFURLContentModificationDateKey: CFString!](/documentation/corefoundation/kcfurlcontentmodificationdatekey)
- [let kCFURLAttributeModificationDateKey: CFString!](/documentation/corefoundation/kcfurlattributemodificationdatekey)
- [let kCFURLLinkCountKey: CFString!](/documentation/corefoundation/kcfurllinkcountkey)
- [let kCFURLParentDirectoryURLKey: CFString!](/documentation/corefoundation/kcfurlparentdirectoryurlkey)
- [let kCFURLVolumeURLKey: CFString!](/documentation/corefoundation/kcfurlvolumeurlkey)
- [let kCFURLTypeIdentifierKey: CFString!](/documentation/corefoundation/kcfurltypeidentifierkey)
- [let kCFURLLocalizedTypeDescriptionKey: CFString!](/documentation/corefoundation/kcfurllocalizedtypedescriptionkey)
- [let kCFURLLabelNumberKey: CFString!](/documentation/corefoundation/kcfurllabelnumberkey)
- [let kCFURLLabelColorKey: CFString!](/documentation/corefoundation/kcfurllabelcolorkey)
- [let kCFURLLocalizedLabelKey: CFString!](/documentation/corefoundation/kcfurllocalizedlabelkey)
- [let kCFURLEffectiveIconKey: CFString!](/documentation/corefoundation/kcfurleffectiveiconkey)
- [let kCFURLCustomIconKey: CFString!](/documentation/corefoundation/kcfurlcustomiconkey)
- [let kCFURLFileResourceIdentifierKey: CFString!](/documentation/corefoundation/kcfurlfileresourceidentifierkey)
- [let kCFURLVolumeIdentifierKey: CFString!](/documentation/corefoundation/kcfurlvolumeidentifierkey)
- [let kCFURLPreferredIOBlockSizeKey: CFString!](/documentation/corefoundation/kcfurlpreferredioblocksizekey)
- [let kCFURLIsReadableKey: CFString!](/documentation/corefoundation/kcfurlisreadablekey)
- [let kCFURLIsWritableKey: CFString!](/documentation/corefoundation/kcfurliswritablekey)
- [let kCFURLIsExecutableKey: CFString!](/documentation/corefoundation/kcfurlisexecutablekey)
- [let kCFURLFileSecurityKey: CFString!](/documentation/corefoundation/kcfurlfilesecuritykey)
- [let kCFURLIsExcludedFromBackupKey: CFString!](/documentation/corefoundation/kcfurlisexcludedfrombackupkey)
- [let kCFURLFileResourceTypeKey: CFString!](/documentation/corefoundation/kcfurlfileresourcetypekey)
- [File Resource Types](/documentation/corefoundation/file-resource-types)

#### Constants

- [let kCFURLFileResourceTypeBlockSpecial: CFString!](/documentation/corefoundation/kcfurlfileresourcetypeblockspecial)
- [let kCFURLFileResourceTypeCharacterSpecial: CFString!](/documentation/corefoundation/kcfurlfileresourcetypecharacterspecial)
- [let kCFURLFileResourceTypeDirectory: CFString!](/documentation/corefoundation/kcfurlfileresourcetypedirectory)
- [let kCFURLFileResourceTypeNamedPipe: CFString!](/documentation/corefoundation/kcfurlfileresourcetypenamedpipe)
- [let kCFURLFileResourceTypeRegular: CFString!](/documentation/corefoundation/kcfurlfileresourcetyperegular)
- [let kCFURLFileResourceTypeSocket: CFString!](/documentation/corefoundation/kcfurlfileresourcetypesocket)
- [let kCFURLFileResourceTypeSymbolicLink: CFString!](/documentation/corefoundation/kcfurlfileresourcetypesymboliclink)
- [let kCFURLFileResourceTypeUnknown: CFString!](/documentation/corefoundation/kcfurlfileresourcetypeunknown)
- [File Property Keys](/documentation/corefoundation/file-property-keys)

#### Constants

- [let kCFURLFileAllocatedSizeKey: CFString!](/documentation/corefoundation/kcfurlfileallocatedsizekey)
- [let kCFURLFileSizeKey: CFString!](/documentation/corefoundation/kcfurlfilesizekey)
- [let kCFURLIsAliasFileKey: CFString!](/documentation/corefoundation/kcfurlisaliasfilekey)
- [let kCFURLIsMountTriggerKey: CFString!](/documentation/corefoundation/kcfurlismounttriggerkey)
- [let kCFURLTotalFileAllocatedSizeKey: CFString!](/documentation/corefoundation/kcfurltotalfileallocatedsizekey)
- [let kCFURLTotalFileSizeKey: CFString!](/documentation/corefoundation/kcfurltotalfilesizekey)
- [iCloud Constants](/documentation/corefoundation/icloud-constants)

#### Constants

- [let kCFURLIsUbiquitousItemKey: CFString!](/documentation/corefoundation/kcfurlisubiquitousitemkey)
- [let kCFURLUbiquitousItemHasUnresolvedConflictsKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemhasunresolvedconflictskey)
- [let kCFURLUbiquitousItemIsDownloadedKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemisdownloadedkey)
- [let kCFURLUbiquitousItemIsDownloadingKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemisdownloadingkey)
- [let kCFURLUbiquitousItemIsUploadedKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemisuploadedkey)
- [let kCFURLUbiquitousItemIsUploadingKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemisuploadingkey)
- [let kCFURLUbiquitousItemPercentDownloadedKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitempercentdownloadedkey)
- [let kCFURLUbiquitousItemPercentUploadedKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitempercentuploadedkey)
- [Volume Property Keys](/documentation/corefoundation/volume-property-keys)

#### Constants

- [let kCFURLVolumeNameKey: CFString!](/documentation/corefoundation/kcfurlvolumenamekey)
- [let kCFURLVolumeLocalizedNameKey: CFString!](/documentation/corefoundation/kcfurlvolumelocalizednamekey)
- [let kCFURLVolumeLocalizedFormatDescriptionKey: CFString!](/documentation/corefoundation/kcfurlvolumelocalizedformatdescriptionkey)
- [let kCFURLVolumeTotalCapacityKey: CFString!](/documentation/corefoundation/kcfurlvolumetotalcapacitykey)
- [let kCFURLVolumeAvailableCapacityKey: CFString!](/documentation/corefoundation/kcfurlvolumeavailablecapacitykey)
- [let kCFURLVolumeResourceCountKey: CFString!](/documentation/corefoundation/kcfurlvolumeresourcecountkey)
- [let kCFURLVolumeSupportsPersistentIDsKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportspersistentidskey)
- [let kCFURLVolumeSupportsSymbolicLinksKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportssymboliclinkskey)
- [let kCFURLVolumeSupportsHardLinksKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportshardlinkskey)
- [let kCFURLVolumeSupportsJournalingKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsjournalingkey)
- [let kCFURLVolumeIsJournalingKey: CFString!](/documentation/corefoundation/kcfurlvolumeisjournalingkey)
- [let kCFURLVolumeSupportsSparseFilesKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportssparsefileskey)
- [let kCFURLVolumeSupportsZeroRunsKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportszerorunskey)
- [let kCFURLVolumeSupportsCaseSensitiveNamesKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportscasesensitivenameskey)
- [let kCFURLVolumeSupportsCasePreservedNamesKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportscasepreservednameskey)
- [let kCFURLVolumeSupportsRootDirectoryDatesKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsrootdirectorydateskey)
- [let kCFURLVolumeSupportsVolumeSizesKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsvolumesizeskey)
- [let kCFURLVolumeSupportsRenamingKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsrenamingkey)
- [let kCFURLVolumeSupportsAdvisoryFileLockingKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsadvisoryfilelockingkey)
- [let kCFURLVolumeSupportsExtendedSecurityKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsextendedsecuritykey)
- [let kCFURLVolumeIsBrowsableKey: CFString!](/documentation/corefoundation/kcfurlvolumeisbrowsablekey)
- [let kCFURLVolumeMaximumFileSizeKey: CFString!](/documentation/corefoundation/kcfurlvolumemaximumfilesizekey)
- [let kCFURLVolumeIsEjectableKey: CFString!](/documentation/corefoundation/kcfurlvolumeisejectablekey)
- [let kCFURLVolumeIsRemovableKey: CFString!](/documentation/corefoundation/kcfurlvolumeisremovablekey)
- [let kCFURLVolumeIsInternalKey: CFString!](/documentation/corefoundation/kcfurlvolumeisinternalkey)
- [let kCFURLVolumeIsAutomountedKey: CFString!](/documentation/corefoundation/kcfurlvolumeisautomountedkey)
- [let kCFURLVolumeIsLocalKey: CFString!](/documentation/corefoundation/kcfurlvolumeislocalkey)
- [let kCFURLVolumeIsReadOnlyKey: CFString!](/documentation/corefoundation/kcfurlvolumeisreadonlykey)
- [let kCFURLVolumeCreationDateKey: CFString!](/documentation/corefoundation/kcfurlvolumecreationdatekey)
- [let kCFURLVolumeURLForRemountingKey: CFString!](/documentation/corefoundation/kcfurlvolumeurlforremountingkey)
- [let kCFURLVolumeUUIDStringKey: CFString!](/documentation/corefoundation/kcfurlvolumeuuidstringkey)
- [CFError userInfo Dictionary Keys](/documentation/corefoundation/cferror-userinfo-dictionary-keys)

#### Constants

- [let kCFURLKeysOfUnsetValuesKey: CFString!](/documentation/corefoundation/kcfurlkeysofunsetvalueskey)

### Miscellaneous

- [CFURLComponentType](/documentation/corefoundation/cfurlcomponenttype)

#### Constants

- [case scheme](/documentation/corefoundation/cfurlcomponenttype/scheme)
- [case netLocation](/documentation/corefoundation/cfurlcomponenttype/netlocation)
- [case path](/documentation/corefoundation/cfurlcomponenttype/path)
- [case resourceSpecifier](/documentation/corefoundation/cfurlcomponenttype/resourcespecifier)
- [case user](/documentation/corefoundation/cfurlcomponenttype/user)
- [case password](/documentation/corefoundation/cfurlcomponenttype/password)
- [case userInfo](/documentation/corefoundation/cfurlcomponenttype/userinfo)
- [case host](/documentation/corefoundation/cfurlcomponenttype/host)
- [case port](/documentation/corefoundation/cfurlcomponenttype/port)
- [case parameterString](/documentation/corefoundation/cfurlcomponenttype/parameterstring)
- [case query](/documentation/corefoundation/cfurlcomponenttype/query)
- [case fragment](/documentation/corefoundation/cfurlcomponenttype/fragment)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfurlcomponenttype/init(rawvalue:))
- [CFURLPathStyle](/documentation/corefoundation/cfurlpathstyle)

#### Constants

- [case cfurlposixPathStyle](/documentation/corefoundation/cfurlpathstyle/cfurlposixpathstyle)
- [case cfurlhfsPathStyle](/documentation/corefoundation/cfurlpathstyle/cfurlhfspathstyle)
- [case cfurlWindowsPathStyle](/documentation/corefoundation/cfurlpathstyle/cfurlwindowspathstyle)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfurlpathstyle/init(rawvalue:))
- [CFUserNotification](/documentation/corefoundation/cfusernotification)

### CFUserNotification Miscellaneous Functions

- [func CFUserNotificationCancel(CFUserNotification!) -> Int32](/documentation/corefoundation/cfusernotificationcancel(_:))
- [func CFUserNotificationCheckBoxChecked(CFIndex) -> CFOptionFlags](/documentation/corefoundation/cfusernotificationcheckboxchecked(_:))
- [func CFUserNotificationCreate(CFAllocator!, CFTimeInterval, CFOptionFlags, UnsafeMutablePointer<Int32>!, CFDictionary!) -> CFUserNotification!](/documentation/corefoundation/cfusernotificationcreate(_:_:_:_:_:))
- [func CFUserNotificationCreateRunLoopSource(CFAllocator!, CFUserNotification!, CFUserNotificationCallBack!, CFIndex) -> CFRunLoopSource!](/documentation/corefoundation/cfusernotificationcreaterunloopsource(_:_:_:_:))
- [func CFUserNotificationDisplayAlert(CFTimeInterval, CFOptionFlags, CFURL!, CFURL!, CFURL!, CFString!, CFString!, CFString!, CFString!, CFString!, UnsafeMutablePointer<CFOptionFlags>!) -> Int32](/documentation/corefoundation/cfusernotificationdisplayalert(_:_:_:_:_:_:_:_:_:_:_:))
- [func CFUserNotificationDisplayNotice(CFTimeInterval, CFOptionFlags, CFURL!, CFURL!, CFURL!, CFString!, CFString!, CFString!) -> Int32](/documentation/corefoundation/cfusernotificationdisplaynotice(_:_:_:_:_:_:_:_:))
- [func CFUserNotificationGetResponseDictionary(CFUserNotification!) -> CFDictionary!](/documentation/corefoundation/cfusernotificationgetresponsedictionary(_:))
- [func CFUserNotificationGetResponseValue(CFUserNotification!, CFString!, CFIndex) -> CFString!](/documentation/corefoundation/cfusernotificationgetresponsevalue(_:_:_:))
- [func CFUserNotificationGetTypeID() -> CFTypeID](/documentation/corefoundation/cfusernotificationgettypeid())
- [func CFUserNotificationPopUpSelection(CFIndex) -> CFOptionFlags](/documentation/corefoundation/cfusernotificationpopupselection(_:))
- [func CFUserNotificationReceiveResponse(CFUserNotification!, CFTimeInterval, UnsafeMutablePointer<CFOptionFlags>!) -> Int32](/documentation/corefoundation/cfusernotificationreceiveresponse(_:_:_:))
- [func CFUserNotificationSecureTextField(CFIndex) -> CFOptionFlags](/documentation/corefoundation/cfusernotificationsecuretextfield(_:))
- [func CFUserNotificationUpdate(CFUserNotification!, CFTimeInterval, CFOptionFlags, CFDictionary!) -> Int32](/documentation/corefoundation/cfusernotificationupdate(_:_:_:_:))

### Callbacks

- [CFUserNotificationCallBack](/documentation/corefoundation/cfusernotificationcallback)

### Constants

- [Alert Levels](/documentation/corefoundation/1534483-alert-levels)

#### Constants

- [var kCFUserNotificationStopAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationstopalertlevel)
- [var kCFUserNotificationNoteAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationnotealertlevel)
- [var kCFUserNotificationCautionAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationcautionalertlevel)
- [var kCFUserNotificationPlainAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationplainalertlevel)
- [Response Codes](/documentation/corefoundation/1534504-response-codes)

#### Constants

- [var kCFUserNotificationDefaultResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationdefaultresponse)
- [var kCFUserNotificationAlternateResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationalternateresponse)
- [var kCFUserNotificationOtherResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationotherresponse)
- [var kCFUserNotificationCancelResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationcancelresponse)
- [Button Flags](/documentation/corefoundation/1534481-button-flags)

#### Constants

- [var kCFUserNotificationNoDefaultButtonFlag: CFOptionFlags](/documentation/corefoundation/kcfusernotificationnodefaultbuttonflag)
- [var kCFUserNotificationUseRadioButtonsFlag: CFOptionFlags](/documentation/corefoundation/kcfusernotificationuseradiobuttonsflag)
- [Alert Levels](/documentation/corefoundation/1534483-alert-levels)

#### Constants

- [var kCFUserNotificationStopAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationstopalertlevel)
- [var kCFUserNotificationNoteAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationnotealertlevel)
- [var kCFUserNotificationCautionAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationcautionalertlevel)
- [var kCFUserNotificationPlainAlertLevel: CFOptionFlags](/documentation/corefoundation/kcfusernotificationplainalertlevel)
- [Response Codes](/documentation/corefoundation/1534504-response-codes)

#### Constants

- [var kCFUserNotificationDefaultResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationdefaultresponse)
- [var kCFUserNotificationAlternateResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationalternateresponse)
- [var kCFUserNotificationOtherResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationotherresponse)
- [var kCFUserNotificationCancelResponse: CFOptionFlags](/documentation/corefoundation/kcfusernotificationcancelresponse)
- [Button Flags](/documentation/corefoundation/1534481-button-flags)

#### Constants

- [var kCFUserNotificationNoDefaultButtonFlag: CFOptionFlags](/documentation/corefoundation/kcfusernotificationnodefaultbuttonflag)
- [var kCFUserNotificationUseRadioButtonsFlag: CFOptionFlags](/documentation/corefoundation/kcfusernotificationuseradiobuttonsflag)
- [Dialog Description Keys](/documentation/corefoundation/dialog-description-keys)

#### Constants

- [let kCFUserNotificationIconURLKey: CFString!](/documentation/corefoundation/kcfusernotificationiconurlkey)
- [let kCFUserNotificationSoundURLKey: CFString!](/documentation/corefoundation/kcfusernotificationsoundurlkey)
- [let kCFUserNotificationLocalizationURLKey: CFString!](/documentation/corefoundation/kcfusernotificationlocalizationurlkey)
- [let kCFUserNotificationAlertHeaderKey: CFString!](/documentation/corefoundation/kcfusernotificationalertheaderkey)
- [let kCFUserNotificationAlertMessageKey: CFString!](/documentation/corefoundation/kcfusernotificationalertmessagekey)
- [let kCFUserNotificationDefaultButtonTitleKey: CFString!](/documentation/corefoundation/kcfusernotificationdefaultbuttontitlekey)
- [let kCFUserNotificationAlternateButtonTitleKey: CFString!](/documentation/corefoundation/kcfusernotificationalternatebuttontitlekey)
- [let kCFUserNotificationOtherButtonTitleKey: CFString!](/documentation/corefoundation/kcfusernotificationotherbuttontitlekey)
- [let kCFUserNotificationProgressIndicatorValueKey: CFString!](/documentation/corefoundation/kcfusernotificationprogressindicatorvaluekey)
- [let kCFUserNotificationPopUpTitlesKey: CFString!](/documentation/corefoundation/kcfusernotificationpopuptitleskey)
- [let kCFUserNotificationTextFieldTitlesKey: CFString!](/documentation/corefoundation/kcfusernotificationtextfieldtitleskey)
- [let kCFUserNotificationCheckBoxTitlesKey: CFString!](/documentation/corefoundation/kcfusernotificationcheckboxtitleskey)
- [let kCFUserNotificationTextFieldValuesKey: CFString!](/documentation/corefoundation/kcfusernotificationtextfieldvalueskey)
- [let kCFUserNotificationPopUpSelectionKey: CFString!](/documentation/corefoundation/kcfusernotificationpopupselectionkey)
- [CFURLEnumerator](/documentation/corefoundation/cfurlenumerator)
- [CFUUID](/documentation/corefoundation/cfuuid)

### Creating CFUUID Objects

- [func CFUUIDCreate(CFAllocator!) -> CFUUID!](/documentation/corefoundation/cfuuidcreate(_:))
- [func CFUUIDCreateFromString(CFAllocator!, CFString!) -> CFUUID!](/documentation/corefoundation/cfuuidcreatefromstring(_:_:))
- [func CFUUIDCreateFromUUIDBytes(CFAllocator!, CFUUIDBytes) -> CFUUID!](/documentation/corefoundation/cfuuidcreatefromuuidbytes(_:_:))
- [func CFUUIDCreateWithBytes(CFAllocator!, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8) -> CFUUID!](/documentation/corefoundation/cfuuidcreatewithbytes(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))

### Getting Information About CFUUID Objects

- [func CFUUIDCreateString(CFAllocator!, CFUUID!) -> CFString!](/documentation/corefoundation/cfuuidcreatestring(_:_:))
- [func CFUUIDGetConstantUUIDWithBytes(CFAllocator!, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8) -> CFUUID!](/documentation/corefoundation/cfuuidgetconstantuuidwithbytes(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func CFUUIDGetUUIDBytes(CFUUID!) -> CFUUIDBytes](/documentation/corefoundation/cfuuidgetuuidbytes(_:))

### Getting the CFUUID Type Identifier

- [func CFUUIDGetTypeID() -> CFTypeID](/documentation/corefoundation/cfuuidgettypeid())

### Data Types

- [CFUUIDBytes](/documentation/corefoundation/cfuuidbytes)

#### Initializers

- [init()](/documentation/corefoundation/cfuuidbytes/init())
- [init(byte0: UInt8, byte1: UInt8, byte2: UInt8, byte3: UInt8, byte4: UInt8, byte5: UInt8, byte6: UInt8, byte7: UInt8, byte8: UInt8, byte9: UInt8, byte10: UInt8, byte11: UInt8, byte12: UInt8, byte13: UInt8, byte14: UInt8, byte15: UInt8)](/documentation/corefoundation/cfuuidbytes/init(byte0:byte1:byte2:byte3:byte4:byte5:byte6:byte7:byte8:byte9:byte10:byte11:byte12:byte13:byte14:byte15:))

#### Instance Properties

- [var byte0: UInt8](/documentation/corefoundation/cfuuidbytes/byte0)
- [var byte1: UInt8](/documentation/corefoundation/cfuuidbytes/byte1)
- [var byte10: UInt8](/documentation/corefoundation/cfuuidbytes/byte10)
- [var byte11: UInt8](/documentation/corefoundation/cfuuidbytes/byte11)
- [var byte12: UInt8](/documentation/corefoundation/cfuuidbytes/byte12)
- [var byte13: UInt8](/documentation/corefoundation/cfuuidbytes/byte13)
- [var byte14: UInt8](/documentation/corefoundation/cfuuidbytes/byte14)
- [var byte15: UInt8](/documentation/corefoundation/cfuuidbytes/byte15)
- [var byte2: UInt8](/documentation/corefoundation/cfuuidbytes/byte2)
- [var byte3: UInt8](/documentation/corefoundation/cfuuidbytes/byte3)
- [var byte4: UInt8](/documentation/corefoundation/cfuuidbytes/byte4)
- [var byte5: UInt8](/documentation/corefoundation/cfuuidbytes/byte5)
- [var byte6: UInt8](/documentation/corefoundation/cfuuidbytes/byte6)
- [var byte7: UInt8](/documentation/corefoundation/cfuuidbytes/byte7)
- [var byte8: UInt8](/documentation/corefoundation/cfuuidbytes/byte8)
- [var byte9: UInt8](/documentation/corefoundation/cfuuidbytes/byte9)
- [CFWriteStream](/documentation/corefoundation/cfwritestream)

### Creating a Write Stream

- [func CFWriteStreamCreateWithAllocatedBuffers(CFAllocator!, CFAllocator!) -> CFWriteStream!](/documentation/corefoundation/cfwritestreamcreatewithallocatedbuffers(_:_:))
- [func CFWriteStreamCreateWithBuffer(CFAllocator!, UnsafeMutablePointer<UInt8>!, CFIndex) -> CFWriteStream!](/documentation/corefoundation/cfwritestreamcreatewithbuffer(_:_:_:))
- [func CFWriteStreamCreateWithFile(CFAllocator!, CFURL!) -> CFWriteStream!](/documentation/corefoundation/cfwritestreamcreatewithfile(_:_:))

### Opening and Closing a Stream

- [func CFWriteStreamClose(CFWriteStream!)](/documentation/corefoundation/cfwritestreamclose(_:))
- [func CFWriteStreamOpen(CFWriteStream!) -> Bool](/documentation/corefoundation/cfwritestreamopen(_:))

### Writing to a Stream

- [func CFWriteStreamWrite(CFWriteStream!, UnsafePointer<UInt8>!, CFIndex) -> CFIndex](/documentation/corefoundation/cfwritestreamwrite(_:_:_:))

### Scheduling a Write Stream

- [func CFWriteStreamScheduleWithRunLoop(CFWriteStream!, CFRunLoop!, CFRunLoopMode!)](/documentation/corefoundation/cfwritestreamschedulewithrunloop(_:_:_:))
- [func CFWriteStreamUnscheduleFromRunLoop(CFWriteStream!, CFRunLoop!, CFRunLoopMode!)](/documentation/corefoundation/cfwritestreamunschedulefromrunloop(_:_:_:))

### Examining Stream Properties

- [func CFWriteStreamCanAcceptBytes(CFWriteStream!) -> Bool](/documentation/corefoundation/cfwritestreamcanacceptbytes(_:))
- [func CFWriteStreamCopyProperty(CFWriteStream!, CFStreamPropertyKey!) -> CFTypeRef!](/documentation/corefoundation/cfwritestreamcopyproperty(_:_:))
- [func CFWriteStreamCopyError(CFWriteStream!) -> CFError!](/documentation/corefoundation/cfwritestreamcopyerror(_:))
- [func CFWriteStreamGetError(CFWriteStream!) -> CFStreamError](/documentation/corefoundation/cfwritestreamgeterror(_:))
- [func CFWriteStreamGetStatus(CFWriteStream!) -> CFStreamStatus](/documentation/corefoundation/cfwritestreamgetstatus(_:))

### Setting Stream Properties

- [func CFWriteStreamSetClient(CFWriteStream!, CFOptionFlags, CFWriteStreamClientCallBack!, UnsafeMutablePointer<CFStreamClientContext>!) -> Bool](/documentation/corefoundation/cfwritestreamsetclient(_:_:_:_:))
- [func CFWriteStreamSetProperty(CFWriteStream!, CFStreamPropertyKey!, CFTypeRef!) -> Bool](/documentation/corefoundation/cfwritestreamsetproperty(_:_:_:))

### Getting the CFWriteStream Type ID

- [func CFWriteStreamGetTypeID() -> CFTypeID](/documentation/corefoundation/cfwritestreamgettypeid())

### Callbacks

- [CFWriteStreamClientCallBack](/documentation/corefoundation/cfwritestreamclientcallback)
- [CFXMLNode](/documentation/corefoundation/cfxmlnode)

### Data Types

- [CFXMLAttributeDeclarationInfo](/documentation/corefoundation/cfxmlattributedeclarationinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlattributedeclarationinfo/init())
- [init(attributeName: Unmanaged<CFString>!, typeString: Unmanaged<CFString>!, defaultString: Unmanaged<CFString>!)](/documentation/corefoundation/cfxmlattributedeclarationinfo/init(attributename:typestring:defaultstring:))

#### Instance Properties

- [var attributeName: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlattributedeclarationinfo/attributename)
- [var defaultString: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlattributedeclarationinfo/defaultstring)
- [var typeString: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlattributedeclarationinfo/typestring)
- [CFXMLAttributeListDeclarationInfo](/documentation/corefoundation/cfxmlattributelistdeclarationinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlattributelistdeclarationinfo/init())
- [init(numberOfAttributes: CFIndex, attributes: UnsafeMutablePointer<CFXMLAttributeDeclarationInfo>!)](/documentation/corefoundation/cfxmlattributelistdeclarationinfo/init(numberofattributes:attributes:))

#### Instance Properties

- [var attributes: UnsafeMutablePointer<CFXMLAttributeDeclarationInfo>!](/documentation/corefoundation/cfxmlattributelistdeclarationinfo/attributes)
- [var numberOfAttributes: CFIndex](/documentation/corefoundation/cfxmlattributelistdeclarationinfo/numberofattributes)
- [CFXMLDocumentInfo](/documentation/corefoundation/cfxmldocumentinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmldocumentinfo/init())
- [init(sourceURL: Unmanaged<CFURL>!, encoding: CFStringEncoding)](/documentation/corefoundation/cfxmldocumentinfo/init(sourceurl:encoding:))

#### Instance Properties

- [var encoding: CFStringEncoding](/documentation/corefoundation/cfxmldocumentinfo/encoding)
- [var sourceURL: Unmanaged<CFURL>!](/documentation/corefoundation/cfxmldocumentinfo/sourceurl)
- [CFXMLDocumentTypeInfo](/documentation/corefoundation/cfxmldocumenttypeinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmldocumenttypeinfo/init())
- [init(externalID: CFXMLExternalID)](/documentation/corefoundation/cfxmldocumenttypeinfo/init(externalid:))

#### Instance Properties

- [var externalID: CFXMLExternalID](/documentation/corefoundation/cfxmldocumenttypeinfo/externalid)
- [CFXMLElementInfo](/documentation/corefoundation/cfxmlelementinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlelementinfo/init())

#### Instance Properties

- [var attributeOrder: Unmanaged<CFArray>!](/documentation/corefoundation/cfxmlelementinfo/attributeorder)
- [var attributes: Unmanaged<CFDictionary>!](/documentation/corefoundation/cfxmlelementinfo/attributes)
- [var isEmpty: DarwinBoolean](/documentation/corefoundation/cfxmlelementinfo/isempty)
- [CFXMLElementTypeDeclarationInfo](/documentation/corefoundation/cfxmlelementtypedeclarationinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlelementtypedeclarationinfo/init())
- [init(contentDescription: Unmanaged<CFString>!)](/documentation/corefoundation/cfxmlelementtypedeclarationinfo/init(contentdescription:))

#### Instance Properties

- [var contentDescription: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlelementtypedeclarationinfo/contentdescription)
- [CFXMLEntityInfo](/documentation/corefoundation/cfxmlentityinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlentityinfo/init())
- [init(entityType: CFXMLEntityTypeCode, replacementText: Unmanaged<CFString>!, entityID: CFXMLExternalID, notationName: Unmanaged<CFString>!)](/documentation/corefoundation/cfxmlentityinfo/init(entitytype:replacementtext:entityid:notationname:))

#### Instance Properties

- [var entityID: CFXMLExternalID](/documentation/corefoundation/cfxmlentityinfo/entityid)
- [var entityType: CFXMLEntityTypeCode](/documentation/corefoundation/cfxmlentityinfo/entitytype)
- [var notationName: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlentityinfo/notationname)
- [var replacementText: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlentityinfo/replacementtext)
- [CFXMLEntityReferenceInfo](/documentation/corefoundation/cfxmlentityreferenceinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlentityreferenceinfo/init())
- [init(entityType: CFXMLEntityTypeCode)](/documentation/corefoundation/cfxmlentityreferenceinfo/init(entitytype:))

#### Instance Properties

- [var entityType: CFXMLEntityTypeCode](/documentation/corefoundation/cfxmlentityreferenceinfo/entitytype)
- [CFXMLExternalID](/documentation/corefoundation/cfxmlexternalid)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlexternalid/init())
- [init(systemID: Unmanaged<CFURL>!, publicID: Unmanaged<CFString>!)](/documentation/corefoundation/cfxmlexternalid/init(systemid:publicid:))

#### Instance Properties

- [var publicID: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlexternalid/publicid)
- [var systemID: Unmanaged<CFURL>!](/documentation/corefoundation/cfxmlexternalid/systemid)
- [CFXMLNotationInfo](/documentation/corefoundation/cfxmlnotationinfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlnotationinfo/init())
- [init(externalID: CFXMLExternalID)](/documentation/corefoundation/cfxmlnotationinfo/init(externalid:))

#### Instance Properties

- [var externalID: CFXMLExternalID](/documentation/corefoundation/cfxmlnotationinfo/externalid)
- [CFXMLProcessingInstructionInfo](/documentation/corefoundation/cfxmlprocessinginstructioninfo)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlprocessinginstructioninfo/init())
- [init(dataString: Unmanaged<CFString>!)](/documentation/corefoundation/cfxmlprocessinginstructioninfo/init(datastring:))

#### Instance Properties

- [var dataString: Unmanaged<CFString>!](/documentation/corefoundation/cfxmlprocessinginstructioninfo/datastring)

### Constants

- [CFXMLEntityTypeCode](/documentation/corefoundation/cfxmlentitytypecode)

#### Constants

- [case parameter](/documentation/corefoundation/cfxmlentitytypecode/parameter)
- [case parsedInternal](/documentation/corefoundation/cfxmlentitytypecode/parsedinternal)
- [case parsedExternal](/documentation/corefoundation/cfxmlentitytypecode/parsedexternal)
- [case unparsed](/documentation/corefoundation/cfxmlentitytypecode/unparsed)
- [case character](/documentation/corefoundation/cfxmlentitytypecode/character)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfxmlentitytypecode/init(rawvalue:))
- [Node Current Version](/documentation/corefoundation/1443311-node-current-version)

#### Constants

- [var kCFXMLNodeCurrentVersion: CFIndex](/documentation/corefoundation/kcfxmlnodecurrentversion)
- [CFXMLNodeTypeCode](/documentation/corefoundation/cfxmlnodetypecode)

#### Constants

- [case document](/documentation/corefoundation/cfxmlnodetypecode/document)
- [case element](/documentation/corefoundation/cfxmlnodetypecode/element)
- [case attribute](/documentation/corefoundation/cfxmlnodetypecode/attribute)
- [case processingInstruction](/documentation/corefoundation/cfxmlnodetypecode/processinginstruction)
- [case comment](/documentation/corefoundation/cfxmlnodetypecode/comment)
- [case text](/documentation/corefoundation/cfxmlnodetypecode/text)
- [case cdataSection](/documentation/corefoundation/cfxmlnodetypecode/cdatasection)
- [case documentFragment](/documentation/corefoundation/cfxmlnodetypecode/documentfragment)
- [case entity](/documentation/corefoundation/cfxmlnodetypecode/entity)
- [case entityReference](/documentation/corefoundation/cfxmlnodetypecode/entityreference)
- [case documentType](/documentation/corefoundation/cfxmlnodetypecode/documenttype)
- [case whitespace](/documentation/corefoundation/cfxmlnodetypecode/whitespace)
- [case notation](/documentation/corefoundation/cfxmlnodetypecode/notation)
- [case elementTypeDeclaration](/documentation/corefoundation/cfxmlnodetypecode/elementtypedeclaration)
- [case attributeListDeclaration](/documentation/corefoundation/cfxmlnodetypecode/attributelistdeclaration)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfxmlnodetypecode/init(rawvalue:))
- [CFXMLParser](/documentation/corefoundation/cfxmlparser)

### Callbacks

- [CFXMLParserAddChildCallBack](/documentation/corefoundation/cfxmlparseraddchildcallback)
- [CFXMLParserCopyDescriptionCallBack](/documentation/corefoundation/cfxmlparsercopydescriptioncallback)
- [CFXMLParserCreateXMLStructureCallBack](/documentation/corefoundation/cfxmlparsercreatexmlstructurecallback)
- [CFXMLParserEndXMLStructureCallBack](/documentation/corefoundation/cfxmlparserendxmlstructurecallback)
- [CFXMLParserHandleErrorCallBack](/documentation/corefoundation/cfxmlparserhandleerrorcallback)
- [CFXMLParserReleaseCallBack](/documentation/corefoundation/cfxmlparserreleasecallback)
- [CFXMLParserResolveExternalEntityCallBack](/documentation/corefoundation/cfxmlparserresolveexternalentitycallback)
- [CFXMLParserRetainCallBack](/documentation/corefoundation/cfxmlparserretaincallback)

### Data Types

- [CFXMLParserCallBacks](/documentation/corefoundation/cfxmlparsercallbacks)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlparsercallbacks/init())
- [init(version: CFIndex, createXMLStructure: CFXMLParserCreateXMLStructureCallBack!, addChild: CFXMLParserAddChildCallBack!, endXMLStructure: CFXMLParserEndXMLStructureCallBack!, resolveExternalEntity: CFXMLParserResolveExternalEntityCallBack!, handleError: CFXMLParserHandleErrorCallBack!)](/documentation/corefoundation/cfxmlparsercallbacks/init(version:createxmlstructure:addchild:endxmlstructure:resolveexternalentity:handleerror:))

#### Instance Properties

- [var addChild: CFXMLParserAddChildCallBack!](/documentation/corefoundation/cfxmlparsercallbacks/addchild)
- [var createXMLStructure: CFXMLParserCreateXMLStructureCallBack!](/documentation/corefoundation/cfxmlparsercallbacks/createxmlstructure)
- [var endXMLStructure: CFXMLParserEndXMLStructureCallBack!](/documentation/corefoundation/cfxmlparsercallbacks/endxmlstructure)
- [var handleError: CFXMLParserHandleErrorCallBack!](/documentation/corefoundation/cfxmlparsercallbacks/handleerror)
- [var resolveExternalEntity: CFXMLParserResolveExternalEntityCallBack!](/documentation/corefoundation/cfxmlparsercallbacks/resolveexternalentity)
- [var version: CFIndex](/documentation/corefoundation/cfxmlparsercallbacks/version)
- [CFXMLParserContext](/documentation/corefoundation/cfxmlparsercontext)

#### Initializers

- [init()](/documentation/corefoundation/cfxmlparsercontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: CFXMLParserRetainCallBack!, release: CFXMLParserReleaseCallBack!, copyDescription: CFXMLParserCopyDescriptionCallBack!)](/documentation/corefoundation/cfxmlparsercontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: CFXMLParserCopyDescriptionCallBack!](/documentation/corefoundation/cfxmlparsercontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfxmlparsercontext/info)
- [var release: CFXMLParserReleaseCallBack!](/documentation/corefoundation/cfxmlparsercontext/release)
- [var retain: CFXMLParserRetainCallBack!](/documentation/corefoundation/cfxmlparsercontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfxmlparsercontext/version)

### Constants

- [CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode)

#### Constants

- [static var statusParseNotBegun: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/statusparsenotbegun)
- [static var statusParseInProgress: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/statusparseinprogress)
- [static var errorUnexpectedEOF: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errorunexpectedeof)
- [static var errorUnknownEncoding: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errorunknownencoding)
- [static var errorEncodingConversionFailure: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errorencodingconversionfailure)
- [static var errorMalformedProcessingInstruction: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedprocessinginstruction)
- [static var errorMalformedDTD: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformeddtd)
- [static var errorMalformedName: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedname)
- [static var errorMalformedCDSect: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedcdsect)
- [static var errorMalformedCloseTag: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedclosetag)
- [static var errorMalformedStartTag: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedstarttag)
- [static var errorMalformedDocument: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformeddocument)
- [static var errorElementlessDocument: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errorelementlessdocument)
- [static var errorMalformedComment: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedcomment)
- [static var errorMalformedCharacterReference: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedcharacterreference)
- [static var errorMalformedParsedCharacterData: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errormalformedparsedcharacterdata)
- [static var errorNoData: CFXMLParserStatusCode](/documentation/corefoundation/cfxmlparserstatuscode/errornodata)

#### Initializers

- [init(rawValue: CFIndex)](/documentation/corefoundation/cfxmlparserstatuscode/init(rawvalue:))
- [CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions)

#### Constants

- [static var validateDocument: CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions/validatedocument)
- [static var skipMetaData: CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions/skipmetadata)
- [static var replacePhysicalEntities: CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions/replacephysicalentities)
- [static var skipWhitespace: CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions/skipwhitespace)
- [static var resolveExternalEntities: CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions/resolveexternalentities)
- [static var addImpliedAttributes: CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions/addimpliedattributes)
- [static var allOptions: CFXMLParserOptions](/documentation/corefoundation/cfxmlparseroptions/alloptions)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfxmlparseroptions/init(rawvalue:))
- [CFXMLTree](/documentation/corefoundation/cfxmltree)

### CFXMLTree Miscellaneous Functions

- [func CFXMLCreateStringByEscapingEntities(CFAllocator!, CFString!, CFDictionary!) -> CFString!](/documentation/corefoundation/cfxmlcreatestringbyescapingentities(_:_:_:))
- [func CFXMLCreateStringByUnescapingEntities(CFAllocator!, CFString!, CFDictionary!) -> CFString!](/documentation/corefoundation/cfxmlcreatestringbyunescapingentities(_:_:_:))

### Constants

- [Error Dictionary Keys](/documentation/corefoundation/error-dictionary-keys)

#### Constants

- [let kCFXMLTreeErrorDescription: CFString!](/documentation/corefoundation/kcfxmltreeerrordescription)
- [let kCFXMLTreeErrorLineNumber: CFString!](/documentation/corefoundation/kcfxmltreeerrorlinenumber)
- [let kCFXMLTreeErrorLocation: CFString!](/documentation/corefoundation/kcfxmltreeerrorlocation)
- [let kCFXMLTreeErrorStatusCode: CFString!](/documentation/corefoundation/kcfxmltreeerrorstatuscode)

## Reference

- [CFStream](/documentation/corefoundation/cfstream)

### Creating Streams

- [func CFStreamCreatePairWithPeerSocketSignature(CFAllocator!, UnsafePointer<CFSocketSignature>!, UnsafeMutablePointer<Unmanaged<CFReadStream>?>!, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>!)](/documentation/corefoundation/cfstreamcreatepairwithpeersocketsignature(_:_:_:_:))
- [func CFStreamCreatePairWithSocketToHost(CFAllocator!, CFString!, UInt32, UnsafeMutablePointer<Unmanaged<CFReadStream>?>!, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>!)](/documentation/corefoundation/cfstreamcreatepairwithsockettohost(_:_:_:_:_:))
- [func CFStreamCreatePairWithSocket(CFAllocator!, CFSocketNativeHandle, UnsafeMutablePointer<Unmanaged<CFReadStream>?>!, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>!)](/documentation/corefoundation/cfstreamcreatepairwithsocket(_:_:_:_:))
- [func CFStreamCreateBoundPair(CFAllocator!, UnsafeMutablePointer<Unmanaged<CFReadStream>?>!, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>!, CFIndex)](/documentation/corefoundation/cfstreamcreateboundpair(_:_:_:_:))
- [func CFStreamCreatePairWithSocketToCFHost(CFAllocator?, CFHost, Int32, UnsafeMutablePointer<Unmanaged<CFReadStream>?>?, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>?)](/documentation/cfnetwork/cfstreamcreatepairwithsockettocfhost(_:_:_:_:_:))
- [func CFStreamCreatePairWithSocketToNetService(CFAllocator?, CFNetService, UnsafeMutablePointer<Unmanaged<CFReadStream>?>?, UnsafeMutablePointer<Unmanaged<CFWriteStream>?>?)](/documentation/cfnetwork/cfstreamcreatepairwithsockettonetservice(_:_:_:_:))

### Obtaining Errors

- [func CFSocketStreamSOCKSGetError(UnsafePointer<CFStreamError>) -> Int32](/documentation/cfnetwork/cfsocketstreamsocksgeterror(_:))
- [func CFSocketStreamSOCKSGetErrorSubdomain(UnsafePointer<CFStreamError>) -> Int32](/documentation/cfnetwork/cfsocketstreamsocksgeterrorsubdomain(_:))

### Setting the Security Protocol

- [func CFReadStreamSetProperty(CFReadStream!, CFStreamPropertyKey!, CFTypeRef!) -> Bool](/documentation/corefoundation/cfreadstreamsetproperty(_:_:_:))
- [func CFWriteStreamSetProperty(CFWriteStream!, CFStreamPropertyKey!, CFTypeRef!) -> Bool](/documentation/corefoundation/cfwritestreamsetproperty(_:_:_:))
- [CFStream Socket Security Level Constants](/documentation/corefoundation/cfstream-socket-security-level-constants)

#### Constants

- [let kCFStreamSocketSecurityLevelNone: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelnone)
- [let kCFStreamSocketSecurityLevelSSLv2: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelsslv2)
- [let kCFStreamSocketSecurityLevelSSLv3: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelsslv3)
- [let kCFStreamSocketSecurityLevelTLSv1: CFString](/documentation/corefoundation/kcfstreamsocketsecurityleveltlsv1)
- [let kCFStreamSocketSecurityLevelNegotiatedSSL: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelnegotiatedssl)

### Data Types

- [CFStreamError](/documentation/corefoundation/cfstreamerror)

#### Initializers

- [init()](/documentation/corefoundation/cfstreamerror/init())
- [init(domain: CFIndex, error: Int32)](/documentation/corefoundation/cfstreamerror/init(domain:error:))

#### Instance Properties

- [var domain: CFIndex](/documentation/corefoundation/cfstreamerror/domain)
- [var error: Int32](/documentation/corefoundation/cfstreamerror/error)
- [CFStreamClientContext](/documentation/corefoundation/cfstreamclientcontext)

#### Initializers

- [init()](/documentation/corefoundation/cfstreamclientcontext/init())
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: ((UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!, release: ((UnsafeMutableRawPointer?) -> Void)!, copyDescription: ((UnsafeMutableRawPointer?) -> Unmanaged<CFString>?)!)](/documentation/corefoundation/cfstreamclientcontext/init(version:info:retain:release:copydescription:))

#### Instance Properties

- [var copyDescription: ((UnsafeMutableRawPointer?) -> Unmanaged<CFString>?)!](/documentation/corefoundation/cfstreamclientcontext/copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/corefoundation/cfstreamclientcontext/info)
- [var release: ((UnsafeMutableRawPointer?) -> Void)!](/documentation/corefoundation/cfstreamclientcontext/release)
- [var retain: ((UnsafeMutableRawPointer?) -> UnsafeMutableRawPointer?)!](/documentation/corefoundation/cfstreamclientcontext/retain)
- [var version: CFIndex](/documentation/corefoundation/cfstreamclientcontext/version)

### Constants

- [CFStreamStatus](/documentation/corefoundation/cfstreamstatus)

#### Constants

- [case notOpen](/documentation/corefoundation/cfstreamstatus/notopen)
- [case opening](/documentation/corefoundation/cfstreamstatus/opening)
- [case open](/documentation/corefoundation/cfstreamstatus/open)
- [case reading](/documentation/corefoundation/cfstreamstatus/reading)
- [case writing](/documentation/corefoundation/cfstreamstatus/writing)
- [case atEnd](/documentation/corefoundation/cfstreamstatus/atend)
- [case closed](/documentation/corefoundation/cfstreamstatus/closed)
- [case error](/documentation/corefoundation/cfstreamstatus/error)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfstreamstatus/init(rawvalue:))
- [CFStreamErrorDomain](/documentation/corefoundation/cfstreamerrordomain)

#### Constants

- [case custom](/documentation/corefoundation/cfstreamerrordomain/custom)
- [case POSIX](/documentation/corefoundation/cfstreamerrordomain/posix)
- [case macOSStatus](/documentation/corefoundation/cfstreamerrordomain/macosstatus)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfstreamerrordomain/init(rawvalue:))
- [CFStream Error Domain Constants (CFHost)](/documentation/corefoundation/cfstream-error-domain-constants-cfhost)

#### Constants

- [let kCFStreamErrorDomainNetDB: Int32](/documentation/cfnetwork/kcfstreamerrordomainnetdb)
- [let kCFStreamErrorDomainNetServices: Int32](/documentation/cfnetwork/kcfstreamerrordomainnetservices)
- [let kCFStreamErrorDomainMach: Int32](/documentation/cfnetwork/kcfstreamerrordomainmach)
- [let kCFStreamErrorDomainFTP: Int32](/documentation/cfnetwork/kcfstreamerrordomainftp)
- [let kCFStreamErrorDomainHTTP: Int32](/documentation/cfnetwork/kcfstreamerrordomainhttp)
- [let kCFStreamErrorDomainSystemConfiguration: Int32](/documentation/cfnetwork/kcfstreamerrordomainsystemconfiguration)
- [let kCFStreamErrorDomainWinSock: CFIndex](/documentation/cfnetwork/kcfstreamerrordomainwinsock)
- [let kCFStreamErrorDomainSOCKS: Int32](/documentation/corefoundation/kcfstreamerrordomainsocks)
- [let kCFStreamErrorDomainSSL: Int32](/documentation/corefoundation/kcfstreamerrordomainssl)
- [Error Subdomains](/documentation/corefoundation/error-subdomains)

#### Constants

- [var kCFStreamErrorSOCKSSubDomainNone: Int](/documentation/cfnetwork/kcfstreamerrorsockssubdomainnone)
- [var kCFStreamErrorSOCKSSubDomainVersionCode: Int](/documentation/cfnetwork/kcfstreamerrorsockssubdomainversioncode)
- [var kCFStreamErrorSOCKS4SubDomainResponse: Int](/documentation/cfnetwork/kcfstreamerrorsocks4subdomainresponse)
- [var kCFStreamErrorSOCKS5SubDomainUserPass: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainuserpass)
- [var kCFStreamErrorSOCKS5SubDomainMethod: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainmethod)
- [var kCFStreamErrorSOCKS5SubDomainResponse: Int](/documentation/cfnetwork/kcfstreamerrorsocks5subdomainresponse)
- [Secure Sockets (SOCKS) Errors](/documentation/cfnetwork/1518266-secure-sockets-socks-errors)
- [CFStreamEventType](/documentation/corefoundation/cfstreameventtype)

#### Constants

- [static var openCompleted: CFStreamEventType](/documentation/corefoundation/cfstreameventtype/opencompleted)
- [static var hasBytesAvailable: CFStreamEventType](/documentation/corefoundation/cfstreameventtype/hasbytesavailable)
- [static var canAcceptBytes: CFStreamEventType](/documentation/corefoundation/cfstreameventtype/canacceptbytes)
- [static var errorOccurred: CFStreamEventType](/documentation/corefoundation/cfstreameventtype/erroroccurred)
- [static var endEncountered: CFStreamEventType](/documentation/corefoundation/cfstreameventtype/endencountered)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfstreameventtype/init(rawvalue:))
- [Stream Properties](/documentation/corefoundation/stream-properties)

#### Constants

- [static let appendToFile: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/appendtofile)
- [static let dataWritten: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/datawritten)
- [static let fileCurrentOffset: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/filecurrentoffset)
- [static let socketNativeHandle: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/socketnativehandle)
- [static let socketRemoteHostName: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/socketremotehostname)
- [static let socketRemotePortNumber: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/socketremoteportnumber)
- [let kCFStreamPropertyShouldCloseNativeSocket: CFString](/documentation/corefoundation/kcfstreampropertyshouldclosenativesocket)
- [let kCFStreamPropertySocketSecurityLevel: CFString](/documentation/corefoundation/kcfstreampropertysocketsecuritylevel)
- [let kCFStreamPropertySSLPeerCertificates: CFString](/documentation/cfnetwork/kcfstreampropertysslpeercertificates)
- [let kCFStreamPropertySSLPeerTrust: CFString](/documentation/cfnetwork/kcfstreampropertysslpeertrust)
- [let kCFStreamPropertySSLSettings: CFString](/documentation/cfnetwork/kcfstreampropertysslsettings)
- [let kCFStreamPropertySSLContext: CFString](/documentation/cfnetwork/kcfstreampropertysslcontext)
- [let kCFStreamPropertySOCKSProxy: CFString](/documentation/corefoundation/kcfstreampropertysocksproxy)
- [let kCFStreamPropertyProxyLocalBypass: CFString](/documentation/cfnetwork/kcfstreampropertyproxylocalbypass)
- [let kCFStreamPropertySocketRemoteHost: CFString](/documentation/cfnetwork/kcfstreampropertysocketremotehost)
- [let kCFStreamPropertySocketRemoteNetService: CFString](/documentation/cfnetwork/kcfstreampropertysocketremotenetservice)
- [let kCFStreamNetworkServiceType: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetype)
- [let kCFStreamPropertyConnectionIsCellular: CFString](/documentation/cfnetwork/kcfstreampropertyconnectioniscellular)
- [let kCFStreamPropertyNoCellular: CFString](/documentation/cfnetwork/kcfstreampropertynocellular)
- [CFStream Property SSL Settings Constants](/documentation/corefoundation/cfstream-property-ssl-settings-constants)

#### Constants

- [let kCFStreamSSLLevel: CFString](/documentation/cfnetwork/kcfstreamssllevel)
- [let kCFStreamSSLAllowsExpiredCertificates: CFString](/documentation/cfnetwork/kcfstreamsslallowsexpiredcertificates)
- [let kCFStreamSSLAllowsExpiredRoots: CFString](/documentation/cfnetwork/kcfstreamsslallowsexpiredroots)
- [let kCFStreamSSLAllowsAnyRoot: CFString](/documentation/cfnetwork/kcfstreamsslallowsanyroot)
- [let kCFStreamSSLValidatesCertificateChain: CFString](/documentation/cfnetwork/kcfstreamsslvalidatescertificatechain)
- [let kCFStreamSSLPeerName: CFString](/documentation/cfnetwork/kcfstreamsslpeername)
- [let kCFStreamSSLCertificates: CFString](/documentation/cfnetwork/kcfstreamsslcertificates)
- [let kCFStreamSSLIsServer: CFString](/documentation/cfnetwork/kcfstreamsslisserver)
- [CFStream Socket Security Level Constants](/documentation/corefoundation/cfstream-socket-security-level-constants)

#### Constants

- [let kCFStreamSocketSecurityLevelNone: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelnone)
- [let kCFStreamSocketSecurityLevelSSLv2: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelsslv2)
- [let kCFStreamSocketSecurityLevelSSLv3: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelsslv3)
- [let kCFStreamSocketSecurityLevelTLSv1: CFString](/documentation/corefoundation/kcfstreamsocketsecurityleveltlsv1)
- [let kCFStreamSocketSecurityLevelNegotiatedSSL: CFString](/documentation/corefoundation/kcfstreamsocketsecuritylevelnegotiatedssl)
- [CFStream SOCKS Proxy Key Constants](/documentation/corefoundation/cfstream-socks-proxy-key-constants)

#### Constants

- [let kCFStreamPropertySOCKSProxyHost: CFString](/documentation/corefoundation/kcfstreampropertysocksproxyhost)
- [let kCFStreamPropertySOCKSProxyPort: CFString](/documentation/corefoundation/kcfstreampropertysocksproxyport)
- [let kCFStreamPropertySOCKSVersion: CFString](/documentation/corefoundation/kcfstreampropertysocksversion)
- [let kCFStreamSocketSOCKSVersion4: CFString](/documentation/corefoundation/kcfstreamsocketsocksversion4)
- [let kCFStreamSocketSOCKSVersion5: CFString](/documentation/corefoundation/kcfstreamsocketsocksversion5)
- [let kCFStreamPropertySOCKSUser: CFString](/documentation/corefoundation/kcfstreampropertysocksuser)
- [let kCFStreamPropertySOCKSPassword: CFString](/documentation/corefoundation/kcfstreampropertysockspassword)
- [Stream Service Types](/documentation/corefoundation/stream-service-types)

#### Constants

- [let kCFStreamNetworkServiceTypeVoIP: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypevoip)
- [let kCFStreamNetworkServiceTypeVideo: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypevideo)
- [let kCFStreamNetworkServiceTypeBackground: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypebackground)
- [let kCFStreamNetworkServiceTypeVoice: CFString](/documentation/cfnetwork/kcfstreamnetworkservicetypevoice)
- [Core Foundation Structures](/documentation/corefoundation/core-foundation-structures)

### Structures

- [CGAffineTransform](/documentation/corefoundation/cgaffinetransform)

#### Initializers

- [init()](/documentation/corefoundation/cgaffinetransform/init())
- [init(CGAffineTransformComponents)](/documentation/corefoundation/cgaffinetransform/init(_:))
- [init(CGFloat, CGFloat, CGFloat, CGFloat, CGFloat, CGFloat)](/documentation/corefoundation/cgaffinetransform/init(_:_:_:_:_:_:))
- [init(a: Double, b: Double, c: Double, d: Double, tx: Double, ty: Double)](/documentation/corefoundation/cgaffinetransform/init(a:b:c:d:tx:ty:))
- [init(rotationAngle: CGFloat)](/documentation/corefoundation/cgaffinetransform/init(rotationangle:))
- [init(scaleX: CGFloat, y: CGFloat)](/documentation/corefoundation/cgaffinetransform/init(scalex:y:))
- [init(translationX: CGFloat, y: CGFloat)](/documentation/corefoundation/cgaffinetransform/init(translationx:y:))

#### Instance Properties

- [var a: Double](/documentation/corefoundation/cgaffinetransform/a)
- [var b: Double](/documentation/corefoundation/cgaffinetransform/b)
- [var c: Double](/documentation/corefoundation/cgaffinetransform/c)
- [var d: Double](/documentation/corefoundation/cgaffinetransform/d)
- [var isIdentity: Bool](/documentation/corefoundation/cgaffinetransform/isidentity)
- [var tx: Double](/documentation/corefoundation/cgaffinetransform/tx)
- [var ty: Double](/documentation/corefoundation/cgaffinetransform/ty)

#### Instance Methods

- [func concatenating(CGAffineTransform) -> CGAffineTransform](/documentation/corefoundation/cgaffinetransform/concatenating(_:))
- [func decomposed() -> CGAffineTransformComponents](/documentation/corefoundation/cgaffinetransform/decomposed())
- [func inverted() -> CGAffineTransform](/documentation/corefoundation/cgaffinetransform/inverted())
- [func rotated(by: CGFloat) -> CGAffineTransform](/documentation/corefoundation/cgaffinetransform/rotated(by:))
- [func scaledBy(x: CGFloat, y: CGFloat) -> CGAffineTransform](/documentation/corefoundation/cgaffinetransform/scaledby(x:y:))
- [func translatedBy(x: CGFloat, y: CGFloat) -> CGAffineTransform](/documentation/corefoundation/cgaffinetransform/translatedby(x:y:))

#### Type Properties

- [static var identity: CGAffineTransform](/documentation/corefoundation/cgaffinetransform/identity)
- [CGAffineTransformComponents](/documentation/corefoundation/cgaffinetransformcomponents)

#### Initializers

- [init()](/documentation/corefoundation/cgaffinetransformcomponents/init())
- [init(scale: CGSize, horizontalShear: CGFloat, rotation: CGFloat, translation: CGVector)](/documentation/corefoundation/cgaffinetransformcomponents/init(scale:horizontalshear:rotation:translation:)-4uvq2)
- [init(scale: CGSize, horizontalShear: Double, rotation: Double, translation: CGVector)](/documentation/corefoundation/cgaffinetransformcomponents/init(scale:horizontalshear:rotation:translation:)-xpnj)

#### Instance Properties

- [var horizontalShear: Double](/documentation/corefoundation/cgaffinetransformcomponents/horizontalshear)
- [var rotation: Double](/documentation/corefoundation/cgaffinetransformcomponents/rotation)
- [var scale: CGSize](/documentation/corefoundation/cgaffinetransformcomponents/scale)
- [var translation: CGVector](/documentation/corefoundation/cgaffinetransformcomponents/translation)
- [CGFloat](/documentation/corefoundation/cgfloat-swift.struct)

#### Initializers

- [init()](/documentation/corefoundation/cgfloat-swift.struct/init())
- [init(CGFloat)](/documentation/corefoundation/cgfloat-swift.struct/init(_:)-7dkuk)
- [init(NSNumber)](/documentation/corefoundation/cgfloat-swift.struct/init(_:)-99gmf)
- [init(bitPattern: UInt)](/documentation/corefoundation/cgfloat-swift.struct/init(bitpattern:))
- [init?(exactly: NSNumber)](/documentation/corefoundation/cgfloat-swift.struct/init(exactly:))
- [init(nan: CGFloat.RawSignificand, signaling: Bool)](/documentation/corefoundation/cgfloat-swift.struct/init(nan:signaling:))
- [init(truncating: NSNumber)](/documentation/corefoundation/cgfloat-swift.struct/init(truncating:))

#### Instance Properties

- [var bitPattern: UInt](/documentation/corefoundation/cgfloat-swift.struct/bitpattern)
- [var native: CGFloat.NativeType](/documentation/corefoundation/cgfloat-swift.struct/native)

#### Type Aliases

- [CGFloat.NativeType](/documentation/corefoundation/cgfloat-swift.struct/nativetype)

#### Default Implementations

- [CustomReflectable Implementations](/documentation/corefoundation/cgfloat-swift.struct/customreflectable-implementations)

##### Instance Properties

- [var customMirror: Mirror](/documentation/corefoundation/cgfloat-swift.struct/custommirror)
- [CustomStringConvertible Implementations](/documentation/corefoundation/cgfloat-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/corefoundation/cgfloat-swift.struct/description)
- [ExpressibleByFloatLiteral Implementations](/documentation/corefoundation/cgfloat-swift.struct/expressiblebyfloatliteral-implementations)

##### Initializers

- [init(floatLiteral: CGFloat.NativeType)](/documentation/corefoundation/cgfloat-swift.struct/init(floatliteral:))
- [ExpressibleByIntegerLiteral Implementations](/documentation/corefoundation/cgfloat-swift.struct/expressiblebyintegerliteral-implementations)

##### Initializers

- [init(integerLiteral: Int)](/documentation/corefoundation/cgfloat-swift.struct/init(integerliteral:))
- [Hashable Implementations](/documentation/corefoundation/cgfloat-swift.struct/hashable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/corefoundation/cgfloat-swift.struct/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/corefoundation/cgfloat-swift.struct/hash(into:))
- [Strideable Implementations](/documentation/corefoundation/cgfloat-swift.struct/strideable-implementations)

##### Instance Methods

- [func advanced(by: CGFloat) -> CGFloat](/documentation/corefoundation/cgfloat-swift.struct/advanced(by:))
- [func distance(to: CGFloat) -> CGFloat](/documentation/corefoundation/cgfloat-swift.struct/distance(to:))
- [CGPoint](/documentation/corefoundation/cgpoint)

#### Initializers

- [init()](/documentation/corefoundation/cgpoint/init())
- [init?(dictionaryRepresentation: CFDictionary)](/documentation/corefoundation/cgpoint/init(dictionaryrepresentation:))
- [init(x: Double, y: Double)](/documentation/corefoundation/cgpoint/init(x:y:)-4lkgz)
- [init(x: Double, y: Double)](/documentation/corefoundation/cgpoint/init(x:y:)-4tunm)
- [init(x: Int, y: Int)](/documentation/corefoundation/cgpoint/init(x:y:)-72awk)

#### Instance Properties

- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/corefoundation/cgpoint/customplaygroundquicklook)
- [var dictionaryRepresentation: CFDictionary](/documentation/corefoundation/cgpoint/dictionaryrepresentation)
- [var x: Double](/documentation/corefoundation/cgpoint/x)
- [var y: Double](/documentation/corefoundation/cgpoint/y)

#### Instance Methods

- [func applying(CGAffineTransform) -> CGPoint](/documentation/corefoundation/cgpoint/applying(_:)-2afxw)
- [func applying(ProjectionTransform) -> CGPoint](/documentation/corefoundation/cgpoint/applying(_:)-5nfkk)
- [func equalTo(CGPoint) -> Bool](/documentation/corefoundation/cgpoint/equalto(_:))

#### Type Properties

- [static var zero: CGPoint](/documentation/corefoundation/cgpoint/zero)
- [CGRect](/documentation/corefoundation/cgrect)

#### Initializers

- [init()](/documentation/corefoundation/cgrect/init())
- [init?(dictionaryRepresentation: CFDictionary)](/documentation/corefoundation/cgrect/init(dictionaryrepresentation:))
- [init(origin: CGPoint, size: CGSize)](/documentation/corefoundation/cgrect/init(origin:size:))
- [init(x: Double, y: Double, width: Double, height: Double)](/documentation/corefoundation/cgrect/init(x:y:width:height:)-27bxn)
- [init(x: Int, y: Int, width: Int, height: Int)](/documentation/corefoundation/cgrect/init(x:y:width:height:)-3kjh6)
- [init(x: CGFloat, y: CGFloat, width: CGFloat, height: CGFloat)](/documentation/corefoundation/cgrect/init(x:y:width:height:)-3xq19)

#### Instance Properties

- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/corefoundation/cgrect/customplaygroundquicklook)
- [var dictionaryRepresentation: CFDictionary](/documentation/corefoundation/cgrect/dictionaryrepresentation)
- [var height: CGFloat](/documentation/corefoundation/cgrect/height)
- [var integral: CGRect](/documentation/corefoundation/cgrect/integral)
- [var isEmpty: Bool](/documentation/corefoundation/cgrect/isempty)
- [var isInfinite: Bool](/documentation/corefoundation/cgrect/isinfinite)
- [var isNull: Bool](/documentation/corefoundation/cgrect/isnull)
- [var maxX: CGFloat](/documentation/corefoundation/cgrect/maxx)
- [var maxY: CGFloat](/documentation/corefoundation/cgrect/maxy)
- [var midX: CGFloat](/documentation/corefoundation/cgrect/midx)
- [var midY: CGFloat](/documentation/corefoundation/cgrect/midy)
- [var minX: CGFloat](/documentation/corefoundation/cgrect/minx)
- [var minY: CGFloat](/documentation/corefoundation/cgrect/miny)
- [var origin: CGPoint](/documentation/corefoundation/cgrect/origin)
- [var size: CGSize](/documentation/corefoundation/cgrect/size)
- [var standardized: CGRect](/documentation/corefoundation/cgrect/standardized)
- [var width: CGFloat](/documentation/corefoundation/cgrect/width)

#### Instance Methods

- [func applying(CGAffineTransform) -> CGRect](/documentation/corefoundation/cgrect/applying(_:))
- [func clip()](/documentation/corefoundation/cgrect/clip())
- [func contains(CGPoint) -> Bool](/documentation/corefoundation/cgrect/contains(_:)-6n2uh)
- [func contains(CGRect) -> Bool](/documentation/corefoundation/cgrect/contains(_:)-8fdse)
- [func divided(atDistance: CGFloat, from: CGRectEdge) -> (slice: CGRect, remainder: CGRect)](/documentation/corefoundation/cgrect/divided(atdistance:from:))
- [func equalTo(CGRect) -> Bool](/documentation/corefoundation/cgrect/equalto(_:))
- [func fill(using: NSCompositingOperation)](/documentation/corefoundation/cgrect/fill(using:))
- [func frame(withWidth: CGFloat, using: NSCompositingOperation)](/documentation/corefoundation/cgrect/frame(withwidth:using:))
- [func inset(by: UIEdgeInsets) -> CGRect](/documentation/corefoundation/cgrect/inset(by:))
- [func insetBy(dx: CGFloat, dy: CGFloat) -> CGRect](/documentation/corefoundation/cgrect/insetby(dx:dy:))
- [func intersection(CGRect) -> CGRect](/documentation/corefoundation/cgrect/intersection(_:))
- [func intersects(CGRect) -> Bool](/documentation/corefoundation/cgrect/intersects(_:))
- [func offsetBy(dx: CGFloat, dy: CGFloat) -> CGRect](/documentation/corefoundation/cgrect/offsetby(dx:dy:))
- [func union(CGRect) -> CGRect](/documentation/corefoundation/cgrect/union(_:))

#### Type Properties

- [static var infinite: CGRect](/documentation/corefoundation/cgrect/infinite)
- [static var null: CGRect](/documentation/corefoundation/cgrect/null)
- [static var zero: CGRect](/documentation/corefoundation/cgrect/zero)
- [CGSize](/documentation/corefoundation/cgsize)

#### Geometric Properties

- [var width: Double](/documentation/corefoundation/cgsize/width)
- [var height: Double](/documentation/corefoundation/cgsize/height)

#### Special Values

- [static var zero: CGSize](/documentation/corefoundation/cgsize/zero)
- [init()](/documentation/corefoundation/cgsize/init())

#### Transforming Sizes

- [func applying(CGAffineTransform) -> CGSize](/documentation/corefoundation/cgsize/applying(_:))

#### Alternate Representations

- [var dictionaryRepresentation: CFDictionary](/documentation/corefoundation/cgsize/dictionaryrepresentation)
- [init?(dictionaryRepresentation: CFDictionary)](/documentation/corefoundation/cgsize/init(dictionaryrepresentation:))
- [var debugDescription: String](/documentation/coregraphics/cgsize/1645822-debugdescription)
- [var customMirror: Mirror](/documentation/coregraphics/cgsize/1645828-custommirror)
- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/corefoundation/cgsize/customplaygroundquicklook)

#### Comparing Sizes

- [func CGSizeEqualToSize(CGSize, CGSize) -> Bool](/documentation/coregraphics/cgsizeequaltosize(_:_:))

#### Initializers

- [init(CVImageSize)](/documentation/corefoundation/cgsize/init(_:))
- [init?(dictionaryRepresentation: CFDictionary)](/documentation/corefoundation/cgsize/init(dictionaryrepresentation:))
- [init(width: Double, height: Double)](/documentation/corefoundation/cgsize/init(width:height:)-2du3k)
- [init(width: Double, height: Double)](/documentation/corefoundation/cgsize/init(width:height:)-63ffm)
- [init(width: Int, height: Int)](/documentation/corefoundation/cgsize/init(width:height:)-83b96)

#### Instance Properties

- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/corefoundation/cgsize/customplaygroundquicklook)
- [var dictionaryRepresentation: CFDictionary](/documentation/corefoundation/cgsize/dictionaryrepresentation)

#### Instance Methods

- [func applying(CGAffineTransform) -> CGSize](/documentation/corefoundation/cgsize/applying(_:))
- [func equalTo(CGSize) -> Bool](/documentation/corefoundation/cgsize/equalto(_:))

#### Type Properties

- [static var zero: CGSize](/documentation/corefoundation/cgsize/zero)
- [CGVector](/documentation/corefoundation/cgvector)

#### Special Values

- [static var zero: CGVector](/documentation/corefoundation/cgvector/zero)
- [init()](/documentation/corefoundation/cgvector/init())

#### Geometric Properties

- [var dx: Double](/documentation/corefoundation/cgvector/dx)
- [var dy: Double](/documentation/corefoundation/cgvector/dy)

#### Initializers

- [init(dx: Double, dy: Double)](/documentation/corefoundation/cgvector/init(dx:dy:)-1cr8k)
- [init(dx: Double, dy: Double)](/documentation/corefoundation/cgvector/init(dx:dy:)-57w7m)
- [init(dx: Int, dy: Int)](/documentation/corefoundation/cgvector/init(dx:dy:)-5dw92)

#### Type Properties

- [static var zero: CGVector](/documentation/corefoundation/cgvector/zero)
- [Core Foundation Enumerations](/documentation/corefoundation/core-foundation-enumerations)

### Enumerations

- [CFFileSecurityClearOptions](/documentation/corefoundation/cffilesecurityclearoptions)

#### Constants

- [static var accessControlList: CFFileSecurityClearOptions](/documentation/corefoundation/cffilesecurityclearoptions/accesscontrollist)
- [static var group: CFFileSecurityClearOptions](/documentation/corefoundation/cffilesecurityclearoptions/group)
- [static var groupUUID: CFFileSecurityClearOptions](/documentation/corefoundation/cffilesecurityclearoptions/groupuuid)
- [static var mode: CFFileSecurityClearOptions](/documentation/corefoundation/cffilesecurityclearoptions/mode)
- [static var owner: CFFileSecurityClearOptions](/documentation/corefoundation/cffilesecurityclearoptions/owner)
- [static var ownerUUID: CFFileSecurityClearOptions](/documentation/corefoundation/cffilesecurityclearoptions/owneruuid)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cffilesecurityclearoptions/init(rawvalue:))
- [CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions)

#### Constants

- [static var withColonSeparatorInTime: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withcolonseparatorintime)
- [static var withColonSeparatorInTimeZone: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withcolonseparatorintimezone)
- [static var withDashSeparatorInDate: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withdashseparatorindate)
- [static var withDay: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withday)
- [static var withFullDate: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withfulldate)
- [static var withFullTime: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withfulltime)
- [static var withInternetDateTime: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withinternetdatetime)
- [static var withMonth: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withmonth)
- [static var withSpaceBetweenDateAndTime: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withspacebetweendateandtime)
- [static var withTime: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withtime)
- [static var withTimeZone: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withtimezone)
- [static var withWeekOfYear: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withweekofyear)
- [static var withYear: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withyear)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfiso8601dateformatoptions/init(rawvalue:))

#### Type Properties

- [static var withFractionalSeconds: CFISO8601DateFormatOptions](/documentation/corefoundation/cfiso8601dateformatoptions/withfractionalseconds)
- [CFRunLoopRunResult](/documentation/corefoundation/cfrunlooprunresult)

#### Constants

- [case finished](/documentation/corefoundation/cfrunlooprunresult/finished)
- [case handledSource](/documentation/corefoundation/cfrunlooprunresult/handledsource)
- [case stopped](/documentation/corefoundation/cfrunlooprunresult/stopped)
- [case timedOut](/documentation/corefoundation/cfrunlooprunresult/timedout)

#### Initializers

- [init?(rawValue: Int32)](/documentation/corefoundation/cfrunlooprunresult/init(rawvalue:))
- [CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions)

#### Constants

- [static var descendRecursively: CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions/descendrecursively)
- [static var skipInvisibles: CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions/skipinvisibles)
- [static var generateFileReferenceURLs: CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions/generatefilereferenceurls)
- [static var skipPackageContents: CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions/skippackagecontents)
- [static var includeDirectoriesPreOrder: CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions/includedirectoriespreorder)
- [static var includeDirectoriesPostOrder: CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions/includedirectoriespostorder)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/corefoundation/cfurlenumeratoroptions/init(rawvalue:))

#### Type Properties

- [static var generateRelativePathURLs: CFURLEnumeratorOptions](/documentation/corefoundation/cfurlenumeratoroptions/generaterelativepathurls)
- [CFURLEnumeratorResult](/documentation/corefoundation/cfurlenumeratorresult)

#### Constants

- [case success](/documentation/corefoundation/cfurlenumeratorresult/success)
- [case end](/documentation/corefoundation/cfurlenumeratorresult/end)
- [case error](/documentation/corefoundation/cfurlenumeratorresult/error)
- [case directoryPostOrderSuccess](/documentation/corefoundation/cfurlenumeratorresult/directorypostordersuccess)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/corefoundation/cfurlenumeratorresult/init(rawvalue:))
- [CGRectEdge](/documentation/corefoundation/cgrectedge)

#### Enumeration Cases

- [case maxXEdge](/documentation/corefoundation/cgrectedge/maxxedge)
- [case maxYEdge](/documentation/corefoundation/cgrectedge/maxyedge)
- [case minXEdge](/documentation/corefoundation/cgrectedge/minxedge)
- [case minYEdge](/documentation/corefoundation/cgrectedge/minyedge)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/corefoundation/cgrectedge/init(rawvalue:))
- [init(rectEdge: NSRectEdge)](/documentation/corefoundation/cgrectedge/init(rectedge:))
- [Core Foundation Constants](/documentation/corefoundation/core-foundation-constants)

### Constants

- [var CFByteOrderBigEndian: __CFByteOrder](/documentation/corefoundation/cfbyteorderbigendian)
- [var CFByteOrderLittleEndian: __CFByteOrder](/documentation/corefoundation/cfbyteorderlittleendian)
- [var CFByteOrderUnknown: __CFByteOrder](/documentation/corefoundation/cfbyteorderunknown)
- [var kCFCoreFoundationVersionNumber10_10: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_10)
- [var kCFCoreFoundationVersionNumber10_10_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_10_1)
- [var kCFCoreFoundationVersionNumber10_10_2: Int32](/documentation/corefoundation/kcfcorefoundationversionnumber10_10_2)
- [var kCFCoreFoundationVersionNumber10_10_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_10_3)
- [var kCFCoreFoundationVersionNumber10_10_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_10_4)
- [var kCFCoreFoundationVersionNumber10_10_5: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_10_5)
- [var kCFCoreFoundationVersionNumber10_10_Max: Int32](/documentation/corefoundation/kcfcorefoundationversionnumber10_10_max)
- [var kCFCoreFoundationVersionNumber10_11: Int32](/documentation/corefoundation/kcfcorefoundationversionnumber10_11)
- [var kCFCoreFoundationVersionNumber10_11_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_11_1)
- [var kCFCoreFoundationVersionNumber10_11_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_11_2)
- [var kCFCoreFoundationVersionNumber10_11_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_11_3)
- [var kCFCoreFoundationVersionNumber10_11_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_11_4)
- [var kCFCoreFoundationVersionNumber10_11_Max: Int32](/documentation/corefoundation/kcfcorefoundationversionnumber10_11_max)
- [var kCFCoreFoundationVersionNumber10_7_5: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_7_5)
- [var kCFCoreFoundationVersionNumber10_8: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_8)
- [var kCFCoreFoundationVersionNumber10_8_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_8_1)
- [var kCFCoreFoundationVersionNumber10_8_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_8_2)
- [var kCFCoreFoundationVersionNumber10_8_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_8_3)
- [var kCFCoreFoundationVersionNumber10_8_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_8_4)
- [var kCFCoreFoundationVersionNumber10_9: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_9)
- [var kCFCoreFoundationVersionNumber10_9_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_9_1)
- [var kCFCoreFoundationVersionNumber10_9_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber10_9_2)
- [var kCFCoreFoundationVersionNumber_iOS_6_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_6_0)
- [var kCFCoreFoundationVersionNumber_iOS_6_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_6_1)
- [var kCFCoreFoundationVersionNumber_iOS_7_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_7_0)
- [var kCFCoreFoundationVersionNumber_iOS_7_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_7_1)
- [var kCFCoreFoundationVersionNumber_iOS_8_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_8_0)
- [var kCFCoreFoundationVersionNumber_iOS_8_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_8_1)
- [var kCFCoreFoundationVersionNumber_iOS_8_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_8_2)
- [var kCFCoreFoundationVersionNumber_iOS_8_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_8_3)
- [var kCFCoreFoundationVersionNumber_iOS_8_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_8_4)
- [var kCFCoreFoundationVersionNumber_iOS_8_x_Max: Int32](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_8_x_max)
- [var kCFCoreFoundationVersionNumber_iOS_9_0: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_9_0)
- [var kCFCoreFoundationVersionNumber_iOS_9_1: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_9_1)
- [var kCFCoreFoundationVersionNumber_iOS_9_2: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_9_2)
- [var kCFCoreFoundationVersionNumber_iOS_9_3: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_9_3)
- [var kCFCoreFoundationVersionNumber_iOS_9_4: Double](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_9_4)
- [var kCFCoreFoundationVersionNumber_iOS_9_x_Max: Int32](/documentation/corefoundation/kcfcorefoundationversionnumber_ios_9_x_max)
- [let kCFNotFound: CFIndex](/documentation/corefoundation/kcfnotfound)
- [let kCFURLAddedToDirectoryDateKey: CFString!](/documentation/corefoundation/kcfurladdedtodirectorydatekey)
- [let kCFURLApplicationIsScriptableKey: CFString!](/documentation/corefoundation/kcfurlapplicationisscriptablekey)
- [let kCFURLCanonicalPathKey: CFString!](/documentation/corefoundation/kcfurlcanonicalpathkey)
- [let kCFURLDocumentIdentifierKey: CFString!](/documentation/corefoundation/kcfurldocumentidentifierkey)
- [let kCFURLFileProtectionComplete: CFString!](/documentation/corefoundation/kcfurlfileprotectioncomplete)
- [let kCFURLFileProtectionCompleteUnlessOpen: CFString!](/documentation/corefoundation/kcfurlfileprotectioncompleteunlessopen)
- [let kCFURLFileProtectionCompleteUntilFirstUserAuthentication: CFString!](/documentation/corefoundation/kcfurlfileprotectioncompleteuntilfirstuserauthentication)
- [let kCFURLFileProtectionKey: CFString!](/documentation/corefoundation/kcfurlfileprotectionkey)
- [let kCFURLFileProtectionNone: CFString!](/documentation/corefoundation/kcfurlfileprotectionnone)
- [let kCFURLGenerationIdentifierKey: CFString!](/documentation/corefoundation/kcfurlgenerationidentifierkey)
- [let kCFURLIsApplicationKey: CFString!](/documentation/corefoundation/kcfurlisapplicationkey)
- [let kCFURLQuarantinePropertiesKey: CFString!](/documentation/corefoundation/kcfurlquarantinepropertieskey)
- [let kCFURLTagNamesKey: CFString!](/documentation/corefoundation/kcfurltagnameskey)
- [let kCFURLUbiquitousItemDownloadingErrorKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemdownloadingerrorkey)
- [let kCFURLUbiquitousItemDownloadingStatusCurrent: CFString!](/documentation/corefoundation/kcfurlubiquitousitemdownloadingstatuscurrent)
- [let kCFURLUbiquitousItemDownloadingStatusDownloaded: CFString!](/documentation/corefoundation/kcfurlubiquitousitemdownloadingstatusdownloaded)
- [let kCFURLUbiquitousItemDownloadingStatusKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemdownloadingstatuskey)
- [let kCFURLUbiquitousItemDownloadingStatusNotDownloaded: CFString!](/documentation/corefoundation/kcfurlubiquitousitemdownloadingstatusnotdownloaded)
- [let kCFURLUbiquitousItemUploadingErrorKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemuploadingerrorkey)
- [let kCFURLVolumeIsEncryptedKey: CFString!](/documentation/corefoundation/kcfurlvolumeisencryptedkey)
- [let kCFURLVolumeIsRootFileSystemKey: CFString!](/documentation/corefoundation/kcfurlvolumeisrootfilesystemkey)
- [let kCFURLVolumeSupportsCompressionKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportscompressionkey)
- [let kCFURLVolumeSupportsExclusiveRenamingKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsexclusiverenamingkey)
- [let kCFURLVolumeSupportsFileCloningKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsfilecloningkey)
- [let kCFURLVolumeSupportsSwapRenamingKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsswaprenamingkey)
- [var CGFLOAT_EPSILON: Double](/documentation/corefoundation/cgfloat_epsilon)
- [var CGFLOAT_IS_DOUBLE: Int32](/documentation/corefoundation/cgfloat_is_double)
- [var CGFLOAT_MAX: Double](/documentation/corefoundation/cgfloat_max)
- [var CGFLOAT_MIN: Double](/documentation/corefoundation/cgfloat_min)
- [var COREFOUNDATION_CFPLUGINCOM_SEPARATE: Int32](/documentation/corefoundation/corefoundation_cfplugincom_separate)
- [var ISA_PTRAUTH_DISCRIMINATOR: Int32](/documentation/corefoundation/isa_ptrauth_discriminator)
- [let kCFErrorLocalizedFailureKey: CFString!](/documentation/corefoundation/kcferrorlocalizedfailurekey)
- [let kCFURLDirectoryEntryCountKey: CFString!](/documentation/corefoundation/kcfurldirectoryentrycountkey)
- [let kCFURLFileContentIdentifierKey: CFString!](/documentation/corefoundation/kcfurlfilecontentidentifierkey)
- [let kCFURLFileIdentifierKey: CFString!](/documentation/corefoundation/kcfurlfileidentifierkey)
- [let kCFURLFileProtectionCompleteWhenUserInactive: CFString!](/documentation/corefoundation/kcfurlfileprotectioncompletewhenuserinactive)
- [let kCFURLIsPurgeableKey: CFString!](/documentation/corefoundation/kcfurlispurgeablekey)
- [let kCFURLIsSparseKey: CFString!](/documentation/corefoundation/kcfurlissparsekey)
- [let kCFURLMayHaveExtendedAttributesKey: CFString!](/documentation/corefoundation/kcfurlmayhaveextendedattributeskey)
- [let kCFURLMayShareFileContentKey: CFString!](/documentation/corefoundation/kcfurlmaysharefilecontentkey)
- [let kCFURLUbiquitousItemIsExcludedFromSyncKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemisexcludedfromsynckey)
- [let kCFURLVolumeAvailableCapacityForImportantUsageKey: CFString!](/documentation/corefoundation/kcfurlvolumeavailablecapacityforimportantusagekey)
- [let kCFURLVolumeAvailableCapacityForOpportunisticUsageKey: CFString!](/documentation/corefoundation/kcfurlvolumeavailablecapacityforopportunisticusagekey)
- [let kCFURLVolumeMountFromLocationKey: CFString!](/documentation/corefoundation/kcfurlvolumemountfromlocationkey)
- [let kCFURLVolumeSubtypeKey: CFString!](/documentation/corefoundation/kcfurlvolumesubtypekey)
- [let kCFURLVolumeSupportsAccessPermissionsKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsaccesspermissionskey)
- [let kCFURLVolumeSupportsFileProtectionKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsfileprotectionkey)
- [let kCFURLVolumeSupportsImmutableFilesKey: CFString!](/documentation/corefoundation/kcfurlvolumesupportsimmutablefileskey)
- [let kCFURLVolumeTypeNameKey: CFString!](/documentation/corefoundation/kcfurlvolumetypenamekey)
- [let kCFUserNotificationAlertTopMostKey: CFString!](/documentation/corefoundation/kcfusernotificationalerttopmostkey)
- [let kCFUserNotificationKeyboardTypesKey: CFString!](/documentation/corefoundation/kcfusernotificationkeyboardtypeskey)
- [Core Foundation Functions](/documentation/corefoundation/core-foundation-functions)

### Functions

- [func CFAllocatorAllocateBytes(CFAllocator!, CFIndex, CFOptionFlags) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfallocatorallocatebytes(_:_:_:))
- [func CFAllocatorAllocateTyped(CFAllocator!, CFIndex, CFAllocatorTypeID, CFOptionFlags) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfallocatorallocatetyped(_:_:_:_:))
- [func CFAllocatorReallocateBytes(CFAllocator!, UnsafeMutableRawPointer!, CFIndex, CFOptionFlags) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfallocatorreallocatebytes(_:_:_:_:))
- [func CFAllocatorReallocateTyped(CFAllocator!, UnsafeMutableRawPointer!, CFIndex, CFAllocatorTypeID, CFOptionFlags) -> UnsafeMutableRawPointer!](/documentation/corefoundation/cfallocatorreallocatetyped(_:_:_:_:_:))
- [func CFAttributedStringGetBidiLevelsAndResolvedDirections(CFAttributedString!, CFRange, Int8, UnsafeMutablePointer<UInt8>!, UnsafeMutablePointer<UInt8>!) -> Bool](/documentation/corefoundation/cfattributedstringgetbidilevelsandresolveddirections(_:_:_:_:_:))
- [func CFBundleCopyLocalizedStringForLocalizations(CFBundle!, CFString!, CFString!, CFString!, CFArray!) -> CFString!](/documentation/corefoundation/cfbundlecopylocalizedstringforlocalizations(_:_:_:_:_:))
- [func CFBundleIsArchitectureLoadable(cpu_type_t) -> Bool](/documentation/corefoundation/cfbundleisarchitectureloadable(_:))
- [func CFBundleIsExecutableLoadable(CFBundle!) -> Bool](/documentation/corefoundation/cfbundleisexecutableloadable(_:))
- [func CFBundleIsExecutableLoadableForURL(CFURL!) -> Bool](/documentation/corefoundation/cfbundleisexecutableloadableforurl(_:))
- [func CFCopyHomeDirectoryURL() -> CFURL!](/documentation/corefoundation/cfcopyhomedirectoryurl())
- [func CFDateFormatterCreateISO8601Formatter(CFAllocator!, CFISO8601DateFormatOptions) -> CFDateFormatter!](/documentation/corefoundation/cfdateformattercreateiso8601formatter(_:_:))
- [func CFFileSecurityClearProperties(CFFileSecurity!, CFFileSecurityClearOptions) -> Bool](/documentation/corefoundation/cffilesecurityclearproperties(_:_:))
- [func CFFileSecurityCopyAccessControlList(CFFileSecurity!, UnsafeMutablePointer<acl_t?>!) -> Bool](/documentation/corefoundation/cffilesecuritycopyaccesscontrollist(_:_:))
- [func CFFileSecurityCopyGroupUUID(CFFileSecurity!, UnsafeMutablePointer<Unmanaged<CFUUID>?>!) -> Bool](/documentation/corefoundation/cffilesecuritycopygroupuuid(_:_:))
- [func CFFileSecurityCopyOwnerUUID(CFFileSecurity!, UnsafeMutablePointer<Unmanaged<CFUUID>?>!) -> Bool](/documentation/corefoundation/cffilesecuritycopyowneruuid(_:_:))
- [func CFFileSecurityCreate(CFAllocator!) -> CFFileSecurity!](/documentation/corefoundation/cffilesecuritycreate(_:))
- [func CFFileSecurityCreateCopy(CFAllocator!, CFFileSecurity!) -> CFFileSecurity!](/documentation/corefoundation/cffilesecuritycreatecopy(_:_:))
- [func CFFileSecurityGetGroup(CFFileSecurity!, UnsafeMutablePointer<gid_t>!) -> Bool](/documentation/corefoundation/cffilesecuritygetgroup(_:_:))
- [func CFFileSecurityGetMode(CFFileSecurity!, UnsafeMutablePointer<mode_t>!) -> Bool](/documentation/corefoundation/cffilesecuritygetmode(_:_:))
- [func CFFileSecurityGetOwner(CFFileSecurity!, UnsafeMutablePointer<uid_t>!) -> Bool](/documentation/corefoundation/cffilesecuritygetowner(_:_:))
- [func CFFileSecurityGetTypeID() -> CFTypeID](/documentation/corefoundation/cffilesecuritygettypeid())
- [func CFFileSecuritySetAccessControlList(CFFileSecurity!, acl_t!) -> Bool](/documentation/corefoundation/cffilesecuritysetaccesscontrollist(_:_:))
- [func CFFileSecuritySetGroup(CFFileSecurity!, gid_t) -> Bool](/documentation/corefoundation/cffilesecuritysetgroup(_:_:))
- [func CFFileSecuritySetGroupUUID(CFFileSecurity!, CFUUID!) -> Bool](/documentation/corefoundation/cffilesecuritysetgroupuuid(_:_:))
- [func CFFileSecuritySetMode(CFFileSecurity!, mode_t) -> Bool](/documentation/corefoundation/cffilesecuritysetmode(_:_:))
- [func CFFileSecuritySetOwner(CFFileSecurity!, uid_t) -> Bool](/documentation/corefoundation/cffilesecuritysetowner(_:_:))
- [func CFFileSecuritySetOwnerUUID(CFFileSecurity!, CFUUID!) -> Bool](/documentation/corefoundation/cffilesecuritysetowneruuid(_:_:))
- [func CFReadStreamCopyDispatchQueue(CFReadStream!) -> dispatch_queue_t!](/documentation/corefoundation/cfreadstreamcopydispatchqueue(_:))
- [func CFReadStreamSetDispatchQueue(CFReadStream!, dispatch_queue_t!)](/documentation/corefoundation/cfreadstreamsetdispatchqueue(_:_:))
- [func CFRunLoopTimerGetTolerance(CFRunLoopTimer!) -> CFTimeInterval](/documentation/corefoundation/cfrunlooptimergettolerance(_:))
- [func CFRunLoopTimerSetTolerance(CFRunLoopTimer!, CFTimeInterval)](/documentation/corefoundation/cfrunlooptimersettolerance(_:_:))
- [func CFURLEnumeratorCreateForDirectoryURL(CFAllocator!, CFURL!, CFURLEnumeratorOptions, CFArray!) -> CFURLEnumerator!](/documentation/corefoundation/cfurlenumeratorcreatefordirectoryurl(_:_:_:_:))
- [func CFURLEnumeratorCreateForMountedVolumes(CFAllocator!, CFURLEnumeratorOptions, CFArray!) -> CFURLEnumerator!](/documentation/corefoundation/cfurlenumeratorcreateformountedvolumes(_:_:_:))
- [func CFURLEnumeratorGetDescendentLevel(CFURLEnumerator!) -> CFIndex](/documentation/corefoundation/cfurlenumeratorgetdescendentlevel(_:))
- [func CFURLEnumeratorGetNextURL(CFURLEnumerator!, UnsafeMutablePointer<Unmanaged<CFURL>?>!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> CFURLEnumeratorResult](/documentation/corefoundation/cfurlenumeratorgetnexturl(_:_:_:))
- [func CFURLEnumeratorGetSourceDidChange(CFURLEnumerator!) -> Bool](/documentation/corefoundation/cfurlenumeratorgetsourcedidchange(_:))
- [func CFURLEnumeratorGetTypeID() -> CFTypeID](/documentation/corefoundation/cfurlenumeratorgettypeid())
- [func CFURLEnumeratorSkipDescendents(CFURLEnumerator!)](/documentation/corefoundation/cfurlenumeratorskipdescendents(_:))
- [func CFURLIsFileReferenceURL(CFURL!) -> Bool](/documentation/corefoundation/cfurlisfilereferenceurl(_:))
- [func CFWriteStreamCopyDispatchQueue(CFWriteStream!) -> dispatch_queue_t!](/documentation/corefoundation/cfwritestreamcopydispatchqueue(_:))
- [func CFWriteStreamSetDispatchQueue(CFWriteStream!, dispatch_queue_t!)](/documentation/corefoundation/cfwritestreamsetdispatchqueue(_:_:))
- [Core Foundation Data Types](/documentation/corefoundation/core-foundation-data-types)

### Data Types

- [CFAllocatorTypeID](/documentation/corefoundation/cfallocatortypeid)
- [CFCalendarIdentifier](/documentation/corefoundation/cfcalendaridentifier)

#### Type Properties

- [static let buddhistCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/buddhistcalendar)
- [static let cfiso8601Calendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/cfiso8601calendar)
- [static let chineseCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/chinesecalendar)
- [static let gregorianCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/gregoriancalendar)
- [static let hebrewCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/hebrewcalendar)
- [static let indianCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/indiancalendar)
- [static let islamicCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamiccalendar)
- [static let islamicCivilCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamiccivilcalendar)
- [static let islamicTabularCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamictabularcalendar)
- [static let islamicUmmAlQuraCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/islamicummalquracalendar)
- [static let japaneseCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/japanesecalendar)
- [static let persianCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/persiancalendar)
- [static let republicOfChinaCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/republicofchinacalendar)
- [static let banglaCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/banglacalendar)
- [static let dangiCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/dangicalendar)
- [static let gujaratiCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/gujaraticalendar)
- [static let kannadaCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/kannadacalendar)
- [static let malayalamCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/malayalamcalendar)
- [static let marathiCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/marathicalendar)
- [static let odiaCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/odiacalendar)
- [static let tamilCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/tamilcalendar)
- [static let teluguCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/telugucalendar)
- [static let vietnameseCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/vietnamesecalendar)
- [static let vikramCalendar: CFCalendarIdentifier!](/documentation/corefoundation/cfcalendaridentifier/vikramcalendar)

#### Initializers

- [init(rawValue: CFString)](/documentation/corefoundation/cfcalendaridentifier/init(rawvalue:))
- [CFDateFormatterKey](/documentation/corefoundation/cfdateformatterkey)

#### Type Properties

- [static let amSymbol: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/amsymbol)
- [static let calendar: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/calendar)
- [static let calendarName: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/calendarname)
- [static let defaultDate: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/defaultdate)
- [static let defaultFormat: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/defaultformat)
- [static let doesRelativeDateFormattingKey: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/doesrelativedateformattingkey)
- [static let eraSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/erasymbols)
- [static let gregorianStartDate: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/gregorianstartdate)
- [static let isLenient: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/islenient)
- [static let longEraSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/longerasymbols)
- [static let monthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/monthsymbols)
- [static let pmSymbol: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/pmsymbol)
- [static let quarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/quartersymbols)
- [static let shortMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortmonthsymbols)
- [static let shortQuarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortquartersymbols)
- [static let shortStandaloneMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortstandalonemonthsymbols)
- [static let shortStandaloneQuarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortstandalonequartersymbols)
- [static let shortStandaloneWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortstandaloneweekdaysymbols)
- [static let shortWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/shortweekdaysymbols)
- [static let standaloneMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/standalonemonthsymbols)
- [static let standaloneQuarterSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/standalonequartersymbols)
- [static let standaloneWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/standaloneweekdaysymbols)
- [static let timeZone: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/timezone)
- [static let twoDigitStartDate: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/twodigitstartdate)
- [static let veryShortMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortmonthsymbols)
- [static let veryShortStandaloneMonthSymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortstandalonemonthsymbols)
- [static let veryShortStandaloneWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortstandaloneweekdaysymbols)
- [static let veryShortWeekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/veryshortweekdaysymbols)
- [static let weekdaySymbols: CFDateFormatterKey!](/documentation/corefoundation/cfdateformatterkey/weekdaysymbols)

#### Initializers

- [init(rawValue: CFString)](/documentation/corefoundation/cfdateformatterkey/init(rawvalue:))
- [CFErrorDomain](/documentation/corefoundation/cferrordomain)
- [CFLocaleIdentifier](/documentation/corefoundation/cflocaleidentifier)

#### Initializers

- [init(CFString)](/documentation/corefoundation/cflocaleidentifier/init(_:))
- [init(rawValue: CFString)](/documentation/corefoundation/cflocaleidentifier/init(rawvalue:))
- [CFLocaleKey](/documentation/corefoundation/cflocalekey)

#### Type Properties

- [static let alternateQuotationBeginDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/alternatequotationbegindelimiterkey)
- [static let alternateQuotationEndDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/alternatequotationenddelimiterkey)
- [static let calendar: CFLocaleKey!](/documentation/corefoundation/cflocalekey/calendar)
- [static let calendarIdentifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/calendaridentifier)
- [static let collationIdentifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/collationidentifier)
- [static let collatorIdentifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/collatoridentifier)
- [static let countryCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/countrycode)
- [static let currencyCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/currencycode)
- [static let currencySymbol: CFLocaleKey!](/documentation/corefoundation/cflocalekey/currencysymbol)
- [static let decimalSeparator: CFLocaleKey!](/documentation/corefoundation/cflocalekey/decimalseparator)
- [static let exemplarCharacterSet: CFLocaleKey!](/documentation/corefoundation/cflocalekey/exemplarcharacterset)
- [static let groupingSeparator: CFLocaleKey!](/documentation/corefoundation/cflocalekey/groupingseparator)
- [static let identifier: CFLocaleKey!](/documentation/corefoundation/cflocalekey/identifier)
- [static let languageCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/languagecode)
- [static let measurementSystem: CFLocaleKey!](/documentation/corefoundation/cflocalekey/measurementsystem)
- [static let quotationBeginDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/quotationbegindelimiterkey)
- [static let quotationEndDelimiterKey: CFLocaleKey!](/documentation/corefoundation/cflocalekey/quotationenddelimiterkey)
- [static let scriptCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/scriptcode)
- [static let usesMetricSystem: CFLocaleKey!](/documentation/corefoundation/cflocalekey/usesmetricsystem)
- [static let variantCode: CFLocaleKey!](/documentation/corefoundation/cflocalekey/variantcode)

#### Initializers

- [init(rawValue: CFString)](/documentation/corefoundation/cflocalekey/init(rawvalue:))
- [CFNotificationName](/documentation/corefoundation/cfnotificationname)

#### Type Properties

- [static let cfLocaleCurrentLocaleDidChange: CFNotificationName!](/documentation/corefoundation/cfnotificationname/cflocalecurrentlocaledidchange)
- [static let cfTimeZoneSystemTimeZoneDidChange: CFNotificationName!](/documentation/corefoundation/cfnotificationname/cftimezonesystemtimezonedidchange)

#### Initializers

- [init(CFString)](/documentation/corefoundation/cfnotificationname/init(_:))
- [init(rawValue: CFString)](/documentation/corefoundation/cfnotificationname/init(rawvalue:))
- [CFNumberFormatterKey](/documentation/corefoundation/cfnumberformatterkey)

#### Type Properties

- [static let alwaysShowDecimalSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/alwaysshowdecimalseparator)
- [static let currencyCode: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencycode)
- [static let currencyDecimalSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencydecimalseparator)
- [static let currencyGroupingSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencygroupingseparator)
- [static let currencySymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/currencysymbol)
- [static let decimalSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/decimalseparator)
- [static let defaultFormat: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/defaultformat)
- [static let exponentSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/exponentsymbol)
- [static let formatWidth: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/formatwidth)
- [static let groupingSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/groupingseparator)
- [static let groupingSize: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/groupingsize)
- [static let infinitySymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/infinitysymbol)
- [static let internationalCurrencySymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/internationalcurrencysymbol)
- [static let isLenient: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/islenient)
- [static let maxFractionDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/maxfractiondigits)
- [static let maxIntegerDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/maxintegerdigits)
- [static let maxSignificantDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/maxsignificantdigits)
- [static let minFractionDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minfractiondigits)
- [static let minIntegerDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minintegerdigits)
- [static let minSignificantDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minsignificantdigits)
- [static let minusSign: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/minussign)
- [static let multiplier: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/multiplier)
- [static let naNSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/nansymbol)
- [static let negativePrefix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/negativeprefix)
- [static let negativeSuffix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/negativesuffix)
- [static let paddingCharacter: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/paddingcharacter)
- [static let paddingPosition: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/paddingposition)
- [static let perMillSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/permillsymbol)
- [static let percentSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/percentsymbol)
- [static let plusSign: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/plussign)
- [static let positivePrefix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/positiveprefix)
- [static let positiveSuffix: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/positivesuffix)
- [static let roundingIncrement: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/roundingincrement)
- [static let roundingMode: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/roundingmode)
- [static let secondaryGroupingSize: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/secondarygroupingsize)
- [static let useGroupingSeparator: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/usegroupingseparator)
- [static let useSignificantDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/usesignificantdigits)
- [static let zeroSymbol: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/zerosymbol)
- [static let minGroupingDigits: CFNumberFormatterKey!](/documentation/corefoundation/cfnumberformatterkey/mingroupingdigits)

#### Initializers

- [init(rawValue: CFString)](/documentation/corefoundation/cfnumberformatterkey/init(rawvalue:))
- [CFRunLoopMode](/documentation/corefoundation/cfrunloopmode)

#### Type Properties

- [static let commonModes: CFRunLoopMode!](/documentation/corefoundation/cfrunloopmode/commonmodes)
- [static let defaultMode: CFRunLoopMode!](/documentation/corefoundation/cfrunloopmode/defaultmode)

#### Initializers

- [init(CFString)](/documentation/corefoundation/cfrunloopmode/init(_:))
- [init(rawValue: CFString)](/documentation/corefoundation/cfrunloopmode/init(rawvalue:))
- [CFStreamPropertyKey](/documentation/corefoundation/cfstreampropertykey)

#### Type Properties

- [static let appendToFile: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/appendtofile)
- [static let dataWritten: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/datawritten)
- [static let fileCurrentOffset: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/filecurrentoffset)
- [static let socketNativeHandle: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/socketnativehandle)
- [static let socketRemoteHostName: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/socketremotehostname)
- [static let socketRemotePortNumber: CFStreamPropertyKey!](/documentation/corefoundation/cfstreampropertykey/socketremoteportnumber)

#### Initializers

- [init(CFString)](/documentation/corefoundation/cfstreampropertykey/init(_:))
- [init(rawValue: CFString)](/documentation/corefoundation/cfstreampropertykey/init(rawvalue:))
- [CFTypeRef](/documentation/corefoundation/cftyperef)

#### Memory Management

- [func CFGetAllocator(CFTypeRef!) -> CFAllocator!](/documentation/corefoundation/cfgetallocator(_:))
- [func CFGetRetainCount(CFTypeRef!) -> CFIndex](/documentation/corefoundation/cfgetretaincount(_:))

#### Determining Equality

- [func CFEqual(CFTypeRef!, CFTypeRef!) -> Bool](/documentation/corefoundation/cfequal(_:_:))

#### Hashing

- [func CFHash(CFTypeRef!) -> CFHashCode](/documentation/corefoundation/cfhash(_:))

#### Miscellaneous Functions

- [func CFCopyDescription(CFTypeRef!) -> CFString!](/documentation/corefoundation/cfcopydescription(_:))
- [func CFCopyTypeIDDescription(CFTypeID) -> CFString!](/documentation/corefoundation/cfcopytypeiddescription(_:))
- [func CFGetTypeID(CFTypeRef!) -> CFTypeID](/documentation/corefoundation/cfgettypeid(_:))
- [func CFShow(CFTypeRef!)](/documentation/corefoundation/cfshow(_:))

#### Data Types

- [CFHashCode](/documentation/corefoundation/cfhashcode)
- [CFTypeID](/documentation/corefoundation/cftypeid)
- [Core Foundation Macros](/documentation/corefoundation/corefoundation-macros)

### Macros

- [var CF_HAS_TYPED_ALLOCATOR: Int32](/documentation/corefoundation/cf_has_typed_allocator)
- [var CGFLOAT_DEFINED: Int32](/documentation/corefoundation/cgfloat_defined)
- [var COREFOUNDATION_CFPLUGINCOM_SEPARATE: Int32](/documentation/corefoundation/corefoundation_cfplugincom_separate)

## Variables

- [let kCFURLUbiquitousItemIsSyncPausedKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemissyncpausedkey)
- [let kCFURLUbiquitousItemSupportedSyncControlsKey: CFString!](/documentation/corefoundation/kcfurlubiquitousitemsupportedsynccontrolskey)

## Functions

- [func CFAttributedStringGetStatisticalWritingDirections(CFAttributedString!, CFRange, Int8, UnsafeMutablePointer<UInt8>!, UnsafeMutablePointer<UInt8>!) -> Bool](/documentation/corefoundation/cfattributedstringgetstatisticalwritingdirections(_:_:_:_:_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
