# IOKit Documentation

Source: https://sosumi.ai/documentation/iokit

---
title: IOKit
source: https://developer.apple.com/documentation/iokit
timestamp: 2026-02-13T18:58:20.758Z
---

## Serial Ports

- [Communicating with a Modem on a Serial Port](/documentation/iokit/communicating_with_a_modem_on_a_serial_port)

## Reference

- [IODataQueueClient.h](/documentation/iokit/iodataqueueclient_h)

### Miscellaneous

- [func IODataQueueAllocateNotificationPort() -> mach_port_t](/documentation/iokit/1514495-iodataqueueallocatenotificationp)
- [func IODataQueueDataAvailable(UnsafeMutablePointer<IODataQueueMemory>!) -> Bool](/documentation/iokit/1514386-iodataqueuedataavailable)
- [func IODataQueueDequeue(UnsafeMutablePointer<IODataQueueMemory>!, UnsafeMutableRawPointer!, UnsafeMutablePointer<UInt32>!) -> IOReturn](/documentation/iokit/1514287-iodataqueuedequeue)
- [func IODataQueueEnqueue(UnsafeMutablePointer<IODataQueueMemory>!, UnsafeMutableRawPointer!, UInt32) -> IOReturn](/documentation/iokit/1514482-iodataqueueenqueue)
- [func IODataQueuePeek(UnsafeMutablePointer<IODataQueueMemory>!) -> UnsafeMutablePointer<IODataQueueEntry>!](/documentation/iokit/1514649-iodataqueuepeek)
- [func IODataQueueSetNotificationPort(UnsafeMutablePointer<IODataQueueMemory>!, mach_port_t) -> IOReturn](/documentation/iokit/1514301-iodataqueuesetnotificationport)
- [func IODataQueueWaitForAvailableData(UnsafeMutablePointer<IODataQueueMemory>!, mach_port_t) -> IOReturn](/documentation/iokit/1514696-iodataqueuewaitforavailabledata)
- [IOKitLib.h](/documentation/iokit/iokitlib_h)

### Miscellaneous

- [func IOBSDNameMatching(mach_port_t, UInt32, UnsafePointer<CChar>!) -> CFMutableDictionary!](/documentation/iokit/1514486-iobsdnamematching)
- [func IOConnectAddClient(io_connect_t, io_connect_t) -> kern_return_t](/documentation/iokit/1514609-ioconnectaddclient)
- [func IOConnectAddRef(io_connect_t) -> kern_return_t](/documentation/iokit/1514739-ioconnectaddref)
- [func IOConnectGetService(io_connect_t, UnsafeMutablePointer<io_service_t>!) -> kern_return_t](/documentation/iokit/1514438-ioconnectgetservice)
- [func IOConnectMapMemory(io_connect_t, UInt32, task_port_t, UnsafeMutablePointer<mach_vm_address_t>!, UnsafeMutablePointer<mach_vm_size_t>!, IOOptionBits) -> kern_return_t](/documentation/iokit/1514377-ioconnectmapmemory)
- [func IOConnectMapMemory64(io_connect_t, UInt32, task_port_t, UnsafeMutablePointer<mach_vm_address_t>!, UnsafeMutablePointer<mach_vm_size_t>!, IOOptionBits) -> kern_return_t](/documentation/iokit/1514862-ioconnectmapmemory64)
- [func IOConnectRelease(io_connect_t) -> kern_return_t](/documentation/iokit/1514511-ioconnectrelease)
- [func IOConnectSetCFProperties(io_connect_t, CFTypeRef!) -> kern_return_t](/documentation/iokit/1514713-ioconnectsetcfproperties)
- [func IOConnectSetCFProperty(io_connect_t, CFString!, CFTypeRef!) -> kern_return_t](/documentation/iokit/1514796-ioconnectsetcfproperty)
- [func IOConnectSetNotificationPort(io_connect_t, UInt32, mach_port_t, UInt) -> kern_return_t](/documentation/iokit/1514541-ioconnectsetnotificationport)
- [func IOConnectUnmapMemory(io_connect_t, UInt32, task_port_t, mach_vm_address_t) -> kern_return_t](/documentation/iokit/1514527-ioconnectunmapmemory)
- [func IOConnectUnmapMemory64(io_connect_t, UInt32, task_port_t, mach_vm_address_t) -> kern_return_t](/documentation/iokit/1514760-ioconnectunmapmemory64)
- [func IOCreateReceivePort(UInt32, UnsafeMutablePointer<mach_port_t>!) -> kern_return_t](/documentation/iokit/1514698-iocreatereceiveport)
- [func IODispatchCalloutFromMessage(UnsafeMutableRawPointer!, UnsafeMutablePointer<mach_msg_header_t>!, UnsafeMutableRawPointer!)](/documentation/iokit/1514775-iodispatchcalloutfrommessage)
- [func IOIteratorIsValid(io_iterator_t) -> boolean_t](/documentation/iokit/1514556-ioiteratorisvalid)
- [func IOIteratorNext(io_iterator_t) -> io_object_t](/documentation/iokit/1514741-ioiteratornext)
- [func IOIteratorReset(io_iterator_t)](/documentation/iokit/1514379-ioiteratorreset)
- [func IOKitGetBusyState(mach_port_t, UnsafeMutablePointer<UInt32>!) -> kern_return_t](/documentation/iokit/1514460-iokitgetbusystate)
- [func IOKitWaitQuiet(mach_port_t, UnsafeMutablePointer<mach_timespec_t>!) -> kern_return_t](/documentation/iokit/1514440-iokitwaitquiet)
- [func IOMasterPort(mach_port_t, UnsafeMutablePointer<mach_port_t>!) -> kern_return_t](/documentation/iokit/1514652-iomasterport)
- [func IONotificationPortCreate(mach_port_t) -> IONotificationPortRef!](/documentation/iokit/1514480-ionotificationportcreate)
- [func IONotificationPortDestroy(IONotificationPortRef!)](/documentation/iokit/1514751-ionotificationportdestroy)
- [func IONotificationPortGetMachPort(IONotificationPortRef!) -> mach_port_t](/documentation/iokit/1514875-ionotificationportgetmachport)
- [func IONotificationPortGetRunLoopSource(IONotificationPortRef!) -> Unmanaged<CFRunLoopSource>!](/documentation/iokit/1514599-ionotificationportgetrunloopsour)
- [func IONotificationPortSetDispatchQueue(IONotificationPortRef!, dispatch_queue_t!)](/documentation/iokit/1514596-ionotificationportsetdispatchque)
- [func IOObjectConformsTo(io_object_t, UnsafePointer<CChar>!) -> boolean_t](/documentation/iokit/1514505-ioobjectconformsto)
- [func IOObjectCopyBundleIdentifierForClass(CFString!) -> Unmanaged<CFString>!](/documentation/iokit/1514375-ioobjectcopybundleidentifierforc)
- [func IOObjectCopyClass(io_object_t) -> Unmanaged<CFString>!](/documentation/iokit/1514781-ioobjectcopyclass)
- [func IOObjectCopySuperclassForClass(CFString!) -> Unmanaged<CFString>!](/documentation/iokit/1514635-ioobjectcopysuperclassforclass)
- [func IOObjectGetClass(io_object_t, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514756-ioobjectgetclass)
- [func IOObjectGetKernelRetainCount(io_object_t) -> UInt32](/documentation/iokit/1514325-ioobjectgetkernelretaincount)
- [func IOObjectGetRetainCount(io_object_t) -> UInt32](/documentation/iokit/1514824-ioobjectgetretaincount)
- [func IOObjectGetUserRetainCount(io_object_t) -> UInt32](/documentation/iokit/1514464-ioobjectgetuserretaincount)
- [func IOObjectIsEqualTo(io_object_t, io_object_t) -> boolean_t](/documentation/iokit/1514563-ioobjectisequalto)
- [func IOObjectRelease(io_object_t) -> kern_return_t](/documentation/iokit/1514627-ioobjectrelease)
- [func IOObjectRetain(io_object_t) -> kern_return_t](/documentation/iokit/1514769-ioobjectretain)
- [func IORegistryCreateIterator(mach_port_t, UnsafePointer<CChar>!, IOOptionBits, UnsafeMutablePointer<io_iterator_t>!) -> kern_return_t](/documentation/iokit/1514238-ioregistrycreateiterator)
- [func IORegistryEntryCreateCFProperties(io_registry_entry_t, UnsafeMutablePointer<Unmanaged<CFMutableDictionary>?>!, CFAllocator!, IOOptionBits) -> kern_return_t](/documentation/iokit/1514310-ioregistryentrycreatecfpropertie)
- [func IORegistryEntryCreateCFProperty(io_registry_entry_t, CFString!, CFAllocator!, IOOptionBits) -> Unmanaged<CFTypeRef>!](/documentation/iokit/1514293-ioregistryentrycreatecfproperty)
- [func IORegistryEntryCreateIterator(io_registry_entry_t, UnsafePointer<CChar>!, IOOptionBits, UnsafeMutablePointer<io_iterator_t>!) -> kern_return_t](/documentation/iokit/1514318-ioregistryentrycreateiterator)
- [func IORegistryEntryFromPath(mach_port_t, UnsafePointer<CChar>!) -> io_registry_entry_t](/documentation/iokit/1514802-ioregistryentryfrompath)
- [func IORegistryEntryGetChildEntry(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<io_registry_entry_t>!) -> kern_return_t](/documentation/iokit/1514496-ioregistryentrygetchildentry)
- [func IORegistryEntryGetChildIterator(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<io_iterator_t>!) -> kern_return_t](/documentation/iokit/1514703-ioregistryentrygetchilditerator)
- [func IORegistryEntryGetLocationInPlane(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514340-ioregistryentrygetlocationinplan)
- [func IORegistryEntryGetName(io_registry_entry_t, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514323-ioregistryentrygetname)
- [func IORegistryEntryGetNameInPlane(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514475-ioregistryentrygetnameinplane)
- [func IORegistryEntryGetParentEntry(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<io_registry_entry_t>!) -> kern_return_t](/documentation/iokit/1514454-ioregistryentrygetparententry)
- [func IORegistryEntryGetParentIterator(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<io_iterator_t>!) -> kern_return_t](/documentation/iokit/1514366-ioregistryentrygetparentiterator)
- [func IORegistryEntryGetPath(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514229-ioregistryentrygetpath)
- [func IORegistryEntryGetRegistryEntryID(io_registry_entry_t, UnsafeMutablePointer<UInt64>!) -> kern_return_t](/documentation/iokit/1514719-ioregistryentrygetregistryentryi)
- [func IORegistryEntryIDMatching(UInt64) -> CFMutableDictionary!](/documentation/iokit/1514880-ioregistryentryidmatching)
- [func IORegistryEntryInPlane(io_registry_entry_t, UnsafePointer<CChar>!) -> boolean_t](/documentation/iokit/1514668-ioregistryentryinplane)
- [func IORegistryEntrySearchCFProperty(io_registry_entry_t, UnsafePointer<CChar>!, CFString!, CFAllocator!, IOOptionBits) -> CFTypeRef!](/documentation/iokit/1514537-ioregistryentrysearchcfproperty)
- [func IORegistryEntrySetCFProperties(io_registry_entry_t, CFTypeRef!) -> kern_return_t](/documentation/iokit/1514414-ioregistryentrysetcfproperties)
- [func IORegistryEntrySetCFProperty(io_registry_entry_t, CFString!, CFTypeRef!) -> kern_return_t](/documentation/iokit/1514882-ioregistryentrysetcfproperty)
- [func IORegistryGetRootEntry(mach_port_t) -> io_registry_entry_t](/documentation/iokit/1514878-ioregistrygetrootentry)
- [func IORegistryIteratorEnterEntry(io_iterator_t) -> kern_return_t](/documentation/iokit/1514822-ioregistryiteratorenterentry)
- [func IORegistryIteratorExitEntry(io_iterator_t) -> kern_return_t](/documentation/iokit/1514334-ioregistryiteratorexitentry)
- [func IOServiceAddInterestNotification(IONotificationPortRef!, io_service_t, UnsafePointer<CChar>!, IOServiceInterestCallback!, UnsafeMutableRawPointer!, UnsafeMutablePointer<io_object_t>!) -> kern_return_t](/documentation/iokit/1514866-ioserviceaddinterestnotification)
- [func IOServiceAddMatchingNotification(IONotificationPortRef!, UnsafePointer<CChar>!, CFDictionary!, IOServiceMatchingCallback!, UnsafeMutableRawPointer!, UnsafeMutablePointer<io_iterator_t>!) -> kern_return_t](/documentation/iokit/1514362-ioserviceaddmatchingnotification)
- [func IOServiceClose(io_connect_t) -> kern_return_t](/documentation/iokit/1514646-ioserviceclose)
- [func IOServiceGetBusyState(io_service_t, UnsafeMutablePointer<UInt32>!) -> kern_return_t](/documentation/iokit/1514607-ioservicegetbusystate)
- [func IOServiceGetMatchingService(mach_port_t, CFDictionary!) -> io_service_t](/documentation/iokit/1514535-ioservicegetmatchingservice)
- [func IOServiceGetMatchingServices(mach_port_t, CFDictionary!, UnsafeMutablePointer<io_iterator_t>!) -> kern_return_t](/documentation/iokit/1514494-ioservicegetmatchingservices)
- [func IOServiceMatching(UnsafePointer<CChar>!) -> CFMutableDictionary!](/documentation/iokit/1514687-ioservicematching)
- [func IOServiceMatchPropertyTable(io_service_t, CFDictionary!, UnsafeMutablePointer<boolean_t>!) -> kern_return_t](/documentation/iokit/1514685-ioservicematchpropertytable)
- [func IOServiceNameMatching(UnsafePointer<CChar>!) -> CFMutableDictionary!](/documentation/iokit/1514416-ioservicenamematching)
- [func IOServiceOpen(io_service_t, task_port_t, UInt32, UnsafeMutablePointer<io_connect_t>!) -> kern_return_t](/documentation/iokit/1514515-ioserviceopen)
- [func IOServiceRequestProbe(io_service_t, UInt32) -> kern_return_t](/documentation/iokit/1514364-ioservicerequestprobe)
- [func IOServiceWaitQuiet(io_service_t, UnsafeMutablePointer<mach_timespec_t>!) -> kern_return_t](/documentation/iokit/1514573-ioservicewaitquiet)

### Callbacks

- [IOAsyncCallback](/documentation/iokit/ioasynccallback)
- [IOAsyncCallback0](/documentation/iokit/ioasynccallback0)
- [IOAsyncCallback1](/documentation/iokit/ioasynccallback1)
- [IOAsyncCallback2](/documentation/iokit/ioasynccallback2)
- [IOServiceInterestCallback](/documentation/iokit/ioserviceinterestcallback)
- [IOServiceMatchingCallback](/documentation/iokit/ioservicematchingcallback)

### Constants

- [Global Constants](/documentation/iokit/iokitlib_h/global_constants)

#### Constants

- [let kIOMasterPortDefault: mach_port_t](/documentation/iokit/kiomasterportdefault)
- [IOTypes.h User-Space](/documentation/iokit/iotypes_h_user-space)

### Constants

- [Scale Factors](/documentation/iokit/iotypes_h_user-space/1553154-scale_factors)

#### Constants

- [var kNanosecondScale: Int](/documentation/iokit/knanosecondscale)
- [var kMicrosecondScale: Int](/documentation/iokit/kmicrosecondscale)
- [var kMillisecondScale: Int](/documentation/iokit/kmillisecondscale)
- [var kTickScale: Int](/documentation/iokit/ktickscale)
- [var kSecondScale: Int](/documentation/iokit/ksecondscale)
- [IOKit Structures](/documentation/iokit/iokit_structures)

### Structures

- [IOAsyncCompletionContent](/documentation/iokit/ioasynccompletioncontent)

#### Initializers

- [init()](/documentation/iokit/ioasynccompletioncontent/1514427-init)

#### Instance Properties

- [var result: IOReturn](/documentation/iokit/ioasynccompletioncontent/1455594-result)
- [IOCFPlugInInterfaceStruct](/documentation/iokit/iocfplugininterfacestruct)

#### Initializers

- [init()](/documentation/iokit/iocfplugininterfacestruct/1514869-init)
- [init(_reserved: UnsafeMutableRawPointer!, QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!, AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!, Release: ((UnsafeMutableRawPointer?) -> ULONG)!, version: UInt16, revision: UInt16, Probe: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t, UnsafeMutablePointer<Int32>?) -> IOReturn)!, Start: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t) -> IOReturn)!, Stop: ((UnsafeMutableRawPointer?) -> IOReturn)!)](/documentation/iokit/iocfplugininterfacestruct/1792000-init)

#### Instance Properties

- [var AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/iokit/iocfplugininterfacestruct/1412440-addref)
- [var Probe: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t, UnsafeMutablePointer<Int32>?) -> IOReturn)!](/documentation/iokit/iocfplugininterfacestruct/1412435-probe)
- [var QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!](/documentation/iokit/iocfplugininterfacestruct/1412423-queryinterface)
- [var Release: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/iokit/iocfplugininterfacestruct/1412422-release)
- [var Start: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t) -> IOReturn)!](/documentation/iokit/iocfplugininterfacestruct/1412433-start)
- [var Stop: ((UnsafeMutableRawPointer?) -> IOReturn)!](/documentation/iokit/iocfplugininterfacestruct/1412438-stop)
- [var revision: UInt16](/documentation/iokit/iocfplugininterfacestruct/1412427-revision)
- [var version: UInt16](/documentation/iokit/iocfplugininterfacestruct/1412436-version)
- [IONamedValue](/documentation/iokit/ionamedvalue)

#### Initializers

- [init()](/documentation/iokit/ionamedvalue/1514639-init)
- [init(value: Int32, name: UnsafePointer<CChar>!)](/documentation/iokit/ionamedvalue/1514633-init)

#### Instance Properties

- [var name: UnsafePointer<CChar>!](/documentation/iokit/ionamedvalue/1514729-name)
- [var value: Int32](/documentation/iokit/ionamedvalue/1514501-value)
- [IOPhysicalRange](/documentation/iokit/iophysicalrange)

#### Initializers

- [init()](/documentation/iokit/iophysicalrange/1514810-init)
- [init(address: IOPhysicalAddress, length: IOByteCount)](/documentation/iokit/iophysicalrange/1514773-init)

#### Instance Properties

- [var address: IOPhysicalAddress](/documentation/iokit/iophysicalrange/1514285-address)
- [var length: IOByteCount](/documentation/iokit/iophysicalrange/1514289-length)
- [IOServiceInterestContent](/documentation/iokit/ioserviceinterestcontent)

#### Initializers

- [init()](/documentation/iokit/ioserviceinterestcontent/1514548-init)
- [init(messageType: natural_t, messageArgument: UnsafeMutableRawPointer?)](/documentation/iokit/ioserviceinterestcontent/1514388-init)

#### Instance Properties

- [var messageArgument: UnsafeMutableRawPointer?](/documentation/iokit/ioserviceinterestcontent/1455538-messageargument)
- [var messageType: natural_t](/documentation/iokit/ioserviceinterestcontent/1455584-messagetype)
- [IOServiceInterestContent64](/documentation/iokit/ioserviceinterestcontent64)

#### Instance Properties

- [var messageArgument: io_user_reference_t](/documentation/iokit/ioserviceinterestcontent64/1455540-messageargument)
- [var messageType: natural_t](/documentation/iokit/ioserviceinterestcontent64/1455516-messagetype)

#### Initializers

- [init()](/documentation/iokit/ioserviceinterestcontent64/1514849-init)
- [init(messageType: natural_t, messageArgument: io_user_reference_t)](/documentation/iokit/ioserviceinterestcontent64/1514569-init)
- [IOURLError](/documentation/iokit/iourlerror)

#### Initializers

- [init(Int32)](/documentation/iokit/iourlerror/1514691-init)
- [init(rawValue: Int32)](/documentation/iokit/iourlerror/1514762-init)

#### Instance Properties

- [var rawValue: Int32](/documentation/iokit/iourlerror/1514452-rawvalue)
- [IOVirtualRange](/documentation/iokit/iovirtualrange)

#### Initializers

- [init()](/documentation/iokit/iovirtualrange/1514435-init)
- [init(address: IOVirtualAddress, length: IOByteCount)](/documentation/iokit/iovirtualrange/1514575-init)

#### Instance Properties

- [var address: IOVirtualAddress](/documentation/iokit/iovirtualrange/1514871-address)
- [var length: IOByteCount](/documentation/iokit/iovirtualrange/1514469-length)
- [OSNotificationHeader](/documentation/iokit/osnotificationheader)

#### Initializers

- [init()](/documentation/iokit/osnotificationheader/1514872-init)

#### Instance Properties

- [var reference: OSAsyncReference](/documentation/iokit/osnotificationheader/1455523-reference)
- [var size: mach_msg_size_t](/documentation/iokit/osnotificationheader/1455560-size)
- [var type: natural_t](/documentation/iokit/osnotificationheader/1455562-type)
- [OSNotificationHeader64](/documentation/iokit/osnotificationheader64)

#### Instance Properties

- [var reference: OSAsyncReference64](/documentation/iokit/osnotificationheader64/1455547-reference)
- [var size: mach_msg_size_t](/documentation/iokit/osnotificationheader64/1455592-size)
- [var type: natural_t](/documentation/iokit/osnotificationheader64/1455613-type)

#### Initializers

- [init()](/documentation/iokit/osnotificationheader64/1514395-init)
- [IORPC](/documentation/iokit/iorpc)

#### Initializers

- [init()](/documentation/iokit/iorpc/3757883-init)
- [init(message: UnsafeMutablePointer<IORPCMessageMach>!, reply: UnsafeMutablePointer<IORPCMessageMach>!, sendSize: UInt32, replySize: UInt32)](/documentation/iokit/iorpc/3757884-init)

#### Instance Properties

- [var message: UnsafeMutablePointer<IORPCMessageMach>!](/documentation/iokit/iorpc/3074874-message)
- [var reply: UnsafeMutablePointer<IORPCMessageMach>!](/documentation/iokit/iorpc/3074875-reply)
- [var replySize: UInt32](/documentation/iokit/iorpc/3074876-replysize)
- [var sendSize: UInt32](/documentation/iokit/iorpc/3074877-sendsize)
- [IORPCMessage](/documentation/iokit/iorpcmessage)

#### Initializers

- [init()](/documentation/iokit/iorpcmessage/3757885-init)
- [init(msgid: UInt64, flags: UInt64, objectRefs: UInt64, objects: ())](/documentation/iokit/iorpcmessage/3757886-init)

#### Instance Properties

- [var flags: UInt64](/documentation/iokit/iorpcmessage/3074881-flags)
- [var msgid: UInt64](/documentation/iokit/iorpcmessage/3074882-msgid)
- [var objectRefs: UInt64](/documentation/iokit/iorpcmessage/3074884-objectrefs)
- [var objects: ()](/documentation/iokit/iorpcmessage/3353076-objects)
- [IORPCMessageErrorReturn](/documentation/iokit/iorpcmessageerrorreturn)

#### Initializers

- [init()](/documentation/iokit/iorpcmessageerrorreturn/3757887-init)
- [init(mach: IORPCMessageMach, content: IORPCMessageErrorReturnContent)](/documentation/iokit/iorpcmessageerrorreturn/3757888-init)

#### Instance Properties

- [var content: IORPCMessageErrorReturnContent](/documentation/iokit/iorpcmessageerrorreturn/3223191-content)
- [var mach: IORPCMessageMach](/documentation/iokit/iorpcmessageerrorreturn/3223192-mach)
- [IORPCMessageErrorReturnContent](/documentation/iokit/iorpcmessageerrorreturncontent)

#### Initializers

- [init()](/documentation/iokit/iorpcmessageerrorreturncontent/3757889-init)
- [init(hdr: IORPCMessage, result: kern_return_t, pad: UInt32)](/documentation/iokit/iorpcmessageerrorreturncontent/3757890-init)

#### Instance Properties

- [var hdr: IORPCMessage](/documentation/iokit/iorpcmessageerrorreturncontent/3223194-hdr)
- [var pad: UInt32](/documentation/iokit/iorpcmessageerrorreturncontent/3223195-pad)
- [var result: kern_return_t](/documentation/iokit/iorpcmessageerrorreturncontent/3325690-result)
- [IORPCMessageMach](/documentation/iokit/iorpcmessagemach)

#### Initializers

- [init()](/documentation/iokit/iorpcmessagemach/3757891-init)
- [init(msgh: mach_msg_header_t, msgh_body: mach_msg_body_t, objects: ())](/documentation/iokit/iorpcmessagemach/3757892-init)

#### Instance Properties

- [var msgh: mach_msg_header_t](/documentation/iokit/iorpcmessagemach/3074887-msgh)
- [var msgh_body: mach_msg_body_t](/documentation/iokit/iorpcmessagemach/3074888-msgh_body)
- [var objects: ()](/documentation/iokit/iorpcmessagemach/3074889-objects)
- [OSClassDescription](/documentation/iokit/osclassdescription)

#### Initializers

- [init()](/documentation/iokit/osclassdescription/3757893-init)
- [init(descriptionSize: UInt32, name: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar), superName: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar), methodOptionsSize: UInt32, methodOptionsOffset: UInt32, metaMethodOptionsSize: UInt32, metaMethodOptionsOffset: UInt32, queueNamesSize: UInt32, queueNamesOffset: UInt32, methodNamesSize: UInt32, methodNamesOffset: UInt32, metaMethodNamesSize: UInt32, metaMethodNamesOffset: UInt32, flags: UInt64, resv1: (UInt64, UInt64, UInt64, UInt64, UInt64, UInt64, UInt64, UInt64), methodOptions: (), metaMethodOptions: (), dispatchNames: (), methodNames: (), metaMethodNames: ())](/documentation/iokit/osclassdescription/3757894-init)

#### Instance Properties

- [var descriptionSize: UInt32](/documentation/iokit/osclassdescription/3074891-descriptionsize)
- [var dispatchNames: ()](/documentation/iokit/osclassdescription/3074892-dispatchnames)
- [var flags: UInt64](/documentation/iokit/osclassdescription/3074893-flags)
- [var metaMethodNames: ()](/documentation/iokit/osclassdescription/3074894-metamethodnames)
- [var metaMethodNamesOffset: UInt32](/documentation/iokit/osclassdescription/3074895-metamethodnamesoffset)
- [var metaMethodNamesSize: UInt32](/documentation/iokit/osclassdescription/3074896-metamethodnamessize)
- [var metaMethodOptions: ()](/documentation/iokit/osclassdescription/3074897-metamethodoptions)
- [var metaMethodOptionsOffset: UInt32](/documentation/iokit/osclassdescription/3074898-metamethodoptionsoffset)
- [var metaMethodOptionsSize: UInt32](/documentation/iokit/osclassdescription/3074899-metamethodoptionssize)
- [var methodNames: ()](/documentation/iokit/osclassdescription/3074900-methodnames)
- [var methodNamesOffset: UInt32](/documentation/iokit/osclassdescription/3074901-methodnamesoffset)
- [var methodNamesSize: UInt32](/documentation/iokit/osclassdescription/3074902-methodnamessize)
- [var methodOptions: ()](/documentation/iokit/osclassdescription/3074903-methodoptions)
- [var methodOptionsOffset: UInt32](/documentation/iokit/osclassdescription/3074904-methodoptionsoffset)
- [var methodOptionsSize: UInt32](/documentation/iokit/osclassdescription/3074905-methodoptionssize)
- [var name: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar)](/documentation/iokit/osclassdescription/3074906-name)
- [var queueNamesOffset: UInt32](/documentation/iokit/osclassdescription/3074907-queuenamesoffset)
- [var queueNamesSize: UInt32](/documentation/iokit/osclassdescription/3074908-queuenamessize)
- [var resv1: (UInt64, UInt64, UInt64, UInt64, UInt64, UInt64, UInt64, UInt64)](/documentation/iokit/osclassdescription/3074909-resv1)
- [var superName: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar)](/documentation/iokit/osclassdescription/3074910-supername)
- [IOKit Enumerations](/documentation/iokit/iokit_enumerations)

### Enumerations

- [Anonymous](/documentation/iokit/iokit_enumerations/1550765-anonymous)

#### Constants

- [var kIORegistryIterateParents: Int](/documentation/iokit/kioregistryiterateparents)
- [var kIORegistryIterateRecursively: Int](/documentation/iokit/kioregistryiteraterecursively)
- [Anonymous](/documentation/iokit/iokit_enumerations/1550764-anonymous)

#### Constants

- [var kIOServiceInteractionAllowed: Int](/documentation/iokit/kioserviceinteractionallowed)
- [Anonymous](/documentation/iokit/iokit_enumerations/1455541-anonymous)

#### Constants

- [var kOSAsyncRefCount: Int](/documentation/iokit/kosasyncrefcount)
- [var kOSAsyncRefSize: Int](/documentation/iokit/kosasyncrefsize)
- [Anonymous](/documentation/iokit/iokit_enumerations/1455610-anonymous)

#### Constants

- [var kOSAsyncRef64Count: Int](/documentation/iokit/kosasyncref64count)
- [var kOSAsyncRef64Size: Int](/documentation/iokit/kosasyncref64size)
- [Anonymous](/documentation/iokit/iokit_enumerations/1455534-anonymous)

#### Constants

- [var kFirstIOKitNotificationType: Int](/documentation/iokit/kfirstiokitnotificationtype)
- [var kIOAsyncCompletionNotificationType: Int](/documentation/iokit/kioasynccompletionnotificationtype)
- [var kIOKitNoticationMsgSizeMask: Int](/documentation/iokit/kiokitnoticationmsgsizemask)
- [var kIOKitNoticationTypeMask: Int](/documentation/iokit/kiokitnoticationtypemask)
- [var kIOKitNoticationTypeSizeAdjShift: Int](/documentation/iokit/kiokitnoticationtypesizeadjshift)
- [var kIOServiceMatchedNotificationType: Int](/documentation/iokit/kioservicematchednotificationtype)
- [var kIOServiceMessageNotificationType: Int](/documentation/iokit/kioservicemessagenotificationtype)
- [var kIOServicePublishNotificationType: Int](/documentation/iokit/kioservicepublishnotificationtype)
- [var kIOServiceTerminatedNotificationType: Int](/documentation/iokit/kioserviceterminatednotificationtype)
- [var kLastIOKitNotificationType: Int](/documentation/iokit/klastiokitnotificationtype)
- [Anonymous](/documentation/iokit/iokit_enumerations/1455590-anonymous)

#### Constants

- [var kMaxAsyncArgs: Int](/documentation/iokit/kmaxasyncargs)
- [var kOSAsyncCompleteMessageID: Int](/documentation/iokit/kosasynccompletemessageid)
- [var kOSNotificationMessageID: Int](/documentation/iokit/kosnotificationmessageid)
- [Anonymous](/documentation/iokit/iokit_enumerations/1455563-anonymous)

#### Constants

- [var kIOAsyncCalloutCount: Int](/documentation/iokit/kioasynccalloutcount)
- [var kIOAsyncCalloutFuncIndex: Int](/documentation/iokit/kioasynccalloutfuncindex)
- [var kIOAsyncCalloutRefconIndex: Int](/documentation/iokit/kioasynccalloutrefconindex)
- [var kIOAsyncReservedCount: Int](/documentation/iokit/kioasyncreservedcount)
- [var kIOAsyncReservedIndex: Int](/documentation/iokit/kioasyncreservedindex)
- [var kIOInterestCalloutCount: Int](/documentation/iokit/kiointerestcalloutcount)
- [var kIOInterestCalloutFuncIndex: Int](/documentation/iokit/kiointerestcalloutfuncindex)
- [var kIOInterestCalloutRefconIndex: Int](/documentation/iokit/kiointerestcalloutrefconindex)
- [var kIOInterestCalloutServiceIndex: Int](/documentation/iokit/kiointerestcalloutserviceindex)
- [var kIOMatchingCalloutCount: Int](/documentation/iokit/kiomatchingcalloutcount)
- [var kIOMatchingCalloutFuncIndex: Int](/documentation/iokit/kiomatchingcalloutfuncindex)
- [var kIOMatchingCalloutRefconIndex: Int](/documentation/iokit/kiomatchingcalloutrefconindex)
- [Anonymous](/documentation/iokit/iokit_enumerations/1553157-anonymous)

#### Constants

- [var kIOMapAnywhere: UInt32](/documentation/iokit/kiomapanywhere)
- [var kIOMapCacheMask: UInt32](/documentation/iokit/kiomapcachemask)
- [var kIOMapCacheShift: UInt32](/documentation/iokit/kiomapcacheshift)
- [var kIOMapCopybackCache: UInt32](/documentation/iokit/kiomapcopybackcache)
- [var kIOMapCopybackInnerCache: UInt32](/documentation/iokit/kiomapcopybackinnercache)
- [var kIOMapDefaultCache: UInt32](/documentation/iokit/kiomapdefaultcache)
- [var kIOMapInhibitCache: UInt32](/documentation/iokit/kiomapinhibitcache)
- [var kIOMapOverwrite: UInt32](/documentation/iokit/kiomapoverwrite)
- [var kIOMapPrefault: UInt32](/documentation/iokit/kiomapprefault)
- [var kIOMapReadOnly: UInt32](/documentation/iokit/kiomapreadonly)
- [var kIOMapReference: UInt32](/documentation/iokit/kiomapreference)
- [var kIOMapStatic: UInt32](/documentation/iokit/kiomapstatic)
- [var kIOMapUnique: UInt32](/documentation/iokit/kiomapunique)
- [var kIOMapUserOptionsMask: UInt32](/documentation/iokit/kiomapuseroptionsmask)
- [var kIOMapWriteCombineCache: UInt32](/documentation/iokit/kiomapwritecombinecache)
- [var kIOMapWriteThruCache: UInt32](/documentation/iokit/kiomapwritethrucache)
- [Anonymous](/documentation/iokit/iokit_enumerations/1553153-anonymous)

#### Constants

- [var kIOConnectMethodVarOutputSize: Int](/documentation/iokit/kioconnectmethodvaroutputsize)
- [Anonymous](/documentation/iokit/iokit_enumerations/1553160-anonymous)

#### Constants

- [var kIODefaultMemoryType: Int](/documentation/iokit/kiodefaultmemorytype)
- [Anonymous](/documentation/iokit/iokit_enumerations/1553159-anonymous)

#### Constants

- [var kIOCopybackCache: Int](/documentation/iokit/kiocopybackcache)
- [var kIOCopybackInnerCache: Int](/documentation/iokit/kiocopybackinnercache)
- [var kIODefaultCache: Int](/documentation/iokit/kiodefaultcache)
- [var kIOInhibitCache: Int](/documentation/iokit/kioinhibitcache)
- [var kIOWriteCombineCache: Int](/documentation/iokit/kiowritecombinecache)
- [var kIOWriteThruCache: Int](/documentation/iokit/kiowritethrucache)
- [Anonymous](/documentation/iokit/iokit_enumerations/1403330-anonymous)

#### Constants

- [var kIOCFSerializeToBinary: Int](/documentation/iokit/kiocfserializetobinary)
- [Anonymous](/documentation/iokit/iokit_enumerations/3074862-anonymous)
- [Anonymous](/documentation/iokit/iokit_enumerations/3074863-anonymous)
- [Anonymous](/documentation/iokit/iokit_enumerations/3074864-anonymous)
- [Anonymous](/documentation/iokit/iokit_enumerations/3353072-anonymous)
- [Anonymous](/documentation/iokit/iokit_enumerations/3689522-anonymous)
- [Anonymous](/documentation/iokit/iokit_enumerations/4359589-anonymous)
- [IOKit Constants](/documentation/iokit/iokit_constants)

### Constants

- [var IOKIT: Int32](/documentation/iokit/iokit)
- [var IOPhysSize: Int32](/documentation/iokit/iophyssize)
- [var IO_OBJECT_NULL: io_object_t](/documentation/iokit/io_object_null)
- [var kIOAppPowerStateInterest: String](/documentation/iokit/kioapppowerstateinterest)
- [var kIOAudioPlane: String](/documentation/iokit/kioaudioplane)
- [var kIOBSDKey: String](/documentation/iokit/kiobsdkey)
- [var kIOBSDMajorKey: String](/documentation/iokit/kiobsdmajorkey)
- [var kIOBSDMinorKey: String](/documentation/iokit/kiobsdminorkey)
- [var kIOBSDNameKey: String](/documentation/iokit/kiobsdnamekey)
- [var kIOBSDNamesKey: String](/documentation/iokit/kiobsdnameskey)
- [var kIOBSDUnitKey: String](/documentation/iokit/kiobsdunitkey)
- [var kIOBootDeviceKey: String](/documentation/iokit/kiobootdevicekey)
- [var kIOBootDevicePathKey: String](/documentation/iokit/kiobootdevicepathkey)
- [var kIOBootDeviceSizeKey: String](/documentation/iokit/kiobootdevicesizekey)
- [var kIOBundleDevelopmentRegionKey: String](/documentation/iokit/kiobundledevelopmentregionkey)
- [var kIOBundleExecutableKey: String](/documentation/iokit/kiobundleexecutablekey)
- [var kIOBundleIdentifierKey: String](/documentation/iokit/kiobundleidentifierkey)
- [var kIOBundleInfoDictionaryVersionKey: String](/documentation/iokit/kiobundleinfodictionaryversionkey)
- [var kIOBundleNameKey: String](/documentation/iokit/kiobundlenamekey)
- [var kIOBundleResourceFileKey: String](/documentation/iokit/kiobundleresourcefilekey)
- [var kIOBundleVersionKey: String](/documentation/iokit/kiobundleversionkey)
- [var kIOBusBadgeKey: String](/documentation/iokit/kiobusbadgekey)
- [var kIOBusyInterest: String](/documentation/iokit/kiobusyinterest)
- [var kIOCFPlugInTypesKey: String](/documentation/iokit/kiocfplugintypeskey)
- [var kIOCatalogueKey: String](/documentation/iokit/kiocataloguekey)
- [var kIOClassKey: String](/documentation/iokit/kioclasskey)
- [var kIOCommandPoolSizeKey: String](/documentation/iokit/kiocommandpoolsizekey)
- [var kIODTNVRAMPanicInfoKey: String](/documentation/iokit/kiodtnvrampanicinfokey)
- [var kIODefaultMatchCategoryKey: String](/documentation/iokit/kiodefaultmatchcategorykey)
- [var kIODeviceIconKey: String](/documentation/iokit/kiodeviceiconkey)
- [var kIODeviceTreePlane: String](/documentation/iokit/kiodevicetreeplane)
- [var kIOFireWirePlane: String](/documentation/iokit/kiofirewireplane)
- [var kIOFirstMatchNotification: String](/documentation/iokit/kiofirstmatchnotification)
- [var kIOFirstPublishNotification: String](/documentation/iokit/kiofirstpublishnotification)
- [var kIOGeneralInterest: String](/documentation/iokit/kiogeneralinterest)
- [var kIOIconKey: String](/documentation/iokit/kioiconkey)
- [var kIOKitBuildVersionKey: String](/documentation/iokit/kiokitbuildversionkey)
- [var kIOKitDebugKey: String](/documentation/iokit/kiokitdebugkey)
- [var kIOKitDiagnosticsKey: String](/documentation/iokit/kiokitdiagnosticskey)
- [var kIOLocationMatchKey: String](/documentation/iokit/kiolocationmatchkey)
- [var kIOMapperIDKey: String](/documentation/iokit/kiomapperidkey)
- [var kIOMatchCategoryKey: String](/documentation/iokit/kiomatchcategorykey)
- [var kIOMatchedNotification: String](/documentation/iokit/kiomatchednotification)
- [var kIOMatchedServiceCountKey: String](/documentation/iokit/kiomatchedservicecountkey)
- [var kIOMaximumBlockCountReadKey: String](/documentation/iokit/kiomaximumblockcountreadkey)
- [var kIOMaximumBlockCountWriteKey: String](/documentation/iokit/kiomaximumblockcountwritekey)
- [var kIOMaximumByteCountReadKey: String](/documentation/iokit/kiomaximumbytecountreadkey)
- [var kIOMaximumByteCountWriteKey: String](/documentation/iokit/kiomaximumbytecountwritekey)
- [var kIOMaximumPriorityCountKey: String](/documentation/iokit/kiomaximumprioritycountkey)
- [var kIOMaximumSegmentAddressableBitCountKey: String](/documentation/iokit/kiomaximumsegmentaddressablebitcountkey)
- [var kIOMaximumSegmentByteCountReadKey: String](/documentation/iokit/kiomaximumsegmentbytecountreadkey)
- [var kIOMaximumSegmentByteCountWriteKey: String](/documentation/iokit/kiomaximumsegmentbytecountwritekey)
- [var kIOMaximumSegmentCountReadKey: String](/documentation/iokit/kiomaximumsegmentcountreadkey)
- [var kIOMaximumSegmentCountWriteKey: String](/documentation/iokit/kiomaximumsegmentcountwritekey)
- [var kIOMinimumSaturationByteCountKey: String](/documentation/iokit/kiominimumsaturationbytecountkey)
- [var kIOMinimumSegmentAlignmentByteCountKey: String](/documentation/iokit/kiominimumsegmentalignmentbytecountkey)
- [var kIONVRAMActivateCSRConfigPropertyKey: String](/documentation/iokit/kionvramactivatecsrconfigpropertykey)
- [var kIONVRAMDeletePropertyKey: String](/documentation/iokit/kionvramdeletepropertykey)
- [var kIONVRAMSyncNowPropertyKey: String](/documentation/iokit/kionvramsyncnowpropertykey)
- [var kIONameMatchKey: String](/documentation/iokit/kionamematchkey)
- [var kIONameMatchedKey: String](/documentation/iokit/kionamematchedkey)
- [var kIOParentMatchKey: String](/documentation/iokit/kioparentmatchkey)
- [var kIOPathMatchKey: String](/documentation/iokit/kiopathmatchkey)
- [var kIOPlatformDeviceMessageKey: String](/documentation/iokit/kioplatformdevicemessagekey)
- [var kIOPlatformSerialNumberKey: String](/documentation/iokit/kioplatformserialnumberkey)
- [var kIOPlatformUUIDKey: String](/documentation/iokit/kioplatformuuidkey)
- [var kIOPowerPlane: String](/documentation/iokit/kiopowerplane)
- [var kIOPriorityPowerStateInterest: String](/documentation/iokit/kioprioritypowerstateinterest)
- [var kIOProbeScoreKey: String](/documentation/iokit/kioprobescorekey)
- [var kIOPropertyExistsMatchKey: String](/documentation/iokit/kiopropertyexistsmatchkey)
- [var kIOPropertyMatchKey: String](/documentation/iokit/kiopropertymatchkey)
- [var kIOProviderClassKey: String](/documentation/iokit/kioproviderclasskey)
- [var kIOPublishNotification: String](/documentation/iokit/kiopublishnotification)
- [var kIORegistryEntryIDKey: String](/documentation/iokit/kioregistryentryidkey)
- [var kIORegistryEntryPropertyKeysKey: String](/documentation/iokit/kioregistryentrypropertykeyskey)
- [var kIORegistryPlanesKey: String](/documentation/iokit/kioregistryplaneskey)
- [var kIOResourceMatchKey: String](/documentation/iokit/kioresourcematchkey)
- [var kIOResourceMatchedKey: String](/documentation/iokit/kioresourcematchedkey)
- [var kIOResourcesClass: String](/documentation/iokit/kioresourcesclass)
- [var kIOReturnAborted: IOReturn](/documentation/iokit/kioreturnaborted)
- [var kIOReturnBadArgument: IOReturn](/documentation/iokit/kioreturnbadargument)
- [var kIOReturnBadMedia: IOReturn](/documentation/iokit/kioreturnbadmedia)
- [var kIOReturnBadMessageID: IOReturn](/documentation/iokit/kioreturnbadmessageid)
- [var kIOReturnBusy: IOReturn](/documentation/iokit/kioreturnbusy)
- [var kIOReturnCannotLock: IOReturn](/documentation/iokit/kioreturncannotlock)
- [var kIOReturnCannotWire: IOReturn](/documentation/iokit/kioreturncannotwire)
- [var kIOReturnDMAError: IOReturn](/documentation/iokit/kioreturndmaerror)
- [var kIOReturnDeviceError: IOReturn](/documentation/iokit/kioreturndeviceerror)
- [var kIOReturnError: IOReturn](/documentation/iokit/kioreturnerror)
- [var kIOReturnExclusiveAccess: IOReturn](/documentation/iokit/kioreturnexclusiveaccess)
- [var kIOReturnIOError: IOReturn](/documentation/iokit/kioreturnioerror)
- [var kIOReturnIPCError: IOReturn](/documentation/iokit/kioreturnipcerror)
- [var kIOReturnInternalError: IOReturn](/documentation/iokit/kioreturninternalerror)
- [var kIOReturnInvalid: IOReturn](/documentation/iokit/kioreturninvalid)
- [var kIOReturnIsoTooNew: IOReturn](/documentation/iokit/kioreturnisotoonew)
- [var kIOReturnIsoTooOld: IOReturn](/documentation/iokit/kioreturnisotooold)
- [var kIOReturnLockedRead: IOReturn](/documentation/iokit/kioreturnlockedread)
- [var kIOReturnLockedWrite: IOReturn](/documentation/iokit/kioreturnlockedwrite)
- [var kIOReturnMessageTooLarge: IOReturn](/documentation/iokit/kioreturnmessagetoolarge)
- [var kIOReturnNoBandwidth: IOReturn](/documentation/iokit/kioreturnnobandwidth)
- [var kIOReturnNoChannels: IOReturn](/documentation/iokit/kioreturnnochannels)
- [var kIOReturnNoCompletion: IOReturn](/documentation/iokit/kioreturnnocompletion)
- [var kIOReturnNoDevice: IOReturn](/documentation/iokit/kioreturnnodevice)
- [var kIOReturnNoFrames: IOReturn](/documentation/iokit/kioreturnnoframes)
- [var kIOReturnNoInterrupt: IOReturn](/documentation/iokit/kioreturnnointerrupt)
- [var kIOReturnNoMedia: IOReturn](/documentation/iokit/kioreturnnomedia)
- [var kIOReturnNoMemory: IOReturn](/documentation/iokit/kioreturnnomemory)
- [var kIOReturnNoPower: IOReturn](/documentation/iokit/kioreturnnopower)
- [var kIOReturnNoResources: IOReturn](/documentation/iokit/kioreturnnoresources)
- [var kIOReturnNoSpace: IOReturn](/documentation/iokit/kioreturnnospace)
- [var kIOReturnNotAligned: IOReturn](/documentation/iokit/kioreturnnotaligned)
- [var kIOReturnNotAttached: IOReturn](/documentation/iokit/kioreturnnotattached)
- [var kIOReturnNotFound: IOReturn](/documentation/iokit/kioreturnnotfound)
- [var kIOReturnNotOpen: IOReturn](/documentation/iokit/kioreturnnotopen)
- [var kIOReturnNotPermitted: IOReturn](/documentation/iokit/kioreturnnotpermitted)
- [var kIOReturnNotPrivileged: IOReturn](/documentation/iokit/kioreturnnotprivileged)
- [var kIOReturnNotReadable: IOReturn](/documentation/iokit/kioreturnnotreadable)
- [var kIOReturnNotReady: IOReturn](/documentation/iokit/kioreturnnotready)
- [var kIOReturnNotResponding: IOReturn](/documentation/iokit/kioreturnnotresponding)
- [var kIOReturnNotWritable: IOReturn](/documentation/iokit/kioreturnnotwritable)
- [var kIOReturnOffline: IOReturn](/documentation/iokit/kioreturnoffline)
- [var kIOReturnOverrun: IOReturn](/documentation/iokit/kioreturnoverrun)
- [var kIOReturnPortExists: IOReturn](/documentation/iokit/kioreturnportexists)
- [var kIOReturnRLDError: IOReturn](/documentation/iokit/kioreturnrlderror)
- [var kIOReturnStillOpen: IOReturn](/documentation/iokit/kioreturnstillopen)
- [var kIOReturnSuccess: Int32](/documentation/iokit/kioreturnsuccess)
- [var kIOReturnTimeout: IOReturn](/documentation/iokit/kioreturntimeout)
- [var kIOReturnUnderrun: IOReturn](/documentation/iokit/kioreturnunderrun)
- [var kIOReturnUnformattedMedia: IOReturn](/documentation/iokit/kioreturnunformattedmedia)
- [var kIOReturnUnsupported: IOReturn](/documentation/iokit/kioreturnunsupported)
- [var kIOReturnUnsupportedMode: IOReturn](/documentation/iokit/kioreturnunsupportedmode)
- [var kIOReturnVMError: IOReturn](/documentation/iokit/kioreturnvmerror)
- [var kIOServiceClass: String](/documentation/iokit/kioserviceclass)
- [var kIOServicePlane: String](/documentation/iokit/kioserviceplane)
- [var kIOTerminatedNotification: String](/documentation/iokit/kioterminatednotification)
- [var kIOURLFileDirectoryContents: String](/documentation/iokit/kiourlfiledirectorycontents)
- [var kIOURLFileExists: String](/documentation/iokit/kiourlfileexists)
- [var kIOURLFileLastModificationTime: String](/documentation/iokit/kiourlfilelastmodificationtime)
- [var kIOURLFileLength: String](/documentation/iokit/kiourlfilelength)
- [var kIOURLFileOwnerID: String](/documentation/iokit/kiourlfileownerid)
- [var kIOURLFilePOSIXMode: String](/documentation/iokit/kiourlfileposixmode)
- [var kIOURLImproperArgumentsError: IOURLError](/documentation/iokit/kiourlimproperargumentserror)
- [var kIOURLPropertyKeyUnavailableError: IOURLError](/documentation/iokit/kiourlpropertykeyunavailableerror)
- [var kIOURLRemoteHostUnavailableError: IOURLError](/documentation/iokit/kiourlremotehostunavailableerror)
- [var kIOURLResourceAccessViolationError: IOURLError](/documentation/iokit/kiourlresourceaccessviolationerror)
- [var kIOURLResourceNotFoundError: IOURLError](/documentation/iokit/kiourlresourcenotfounderror)
- [var kIOURLTimeoutError: IOURLError](/documentation/iokit/kiourltimeouterror)
- [var kIOURLUnknownError: IOURLError](/documentation/iokit/kiourlunknownerror)
- [var kIOURLUnknownPropertyKeyError: IOURLError](/documentation/iokit/kiourlunknownpropertykeyerror)
- [var kIOURLUnknownSchemeError: IOURLError](/documentation/iokit/kiourlunknownschemeerror)
- [var kIOUSBPlane: String](/documentation/iokit/kiousbplane)
- [var kIOUserClientClassKey: String](/documentation/iokit/kiouserclientclasskey)
- [var kIOUserClientCreatorKey: String](/documentation/iokit/kiouserclientcreatorkey)
- [var kIOUserClientCrossEndianCompatibleKey: String](/documentation/iokit/kiouserclientcrossendiancompatiblekey)
- [var kIOUserClientCrossEndianKey: String](/documentation/iokit/kiouserclientcrossendiankey)
- [var kIOUserClientSharedInstanceKey: String](/documentation/iokit/kiouserclientsharedinstancekey)
- [var kOSBuildVersionKey: String](/documentation/iokit/kosbuildversionkey)
- [var PRIIOByteCount: String](/documentation/iokit/priiobytecount)
- [var kIOAllCPUInitializedKey: String](/documentation/iokit/kioallcpuinitializedkey)
- [var kIOCompatibilityMatchKey: String](/documentation/iokit/kiocompatibilitymatchkey)
- [var kIOCompatibilityPropertiesKey: String](/documentation/iokit/kiocompatibilitypropertieskey)
- [var kIODEXTMatchCountKey: String](/documentation/iokit/kiodextmatchcountkey)
- [var kIODriverKitEntitlementKey: String](/documentation/iokit/kiodriverkitentitlementkey)
- [var kIODriverKitHIDFamilyDeviceEntitlementKey: String](/documentation/iokit/kiodriverkithidfamilydeviceentitlementkey)
- [var kIODriverKitHIDFamilyEventServiceEntitlementKey: String](/documentation/iokit/kiodriverkithidfamilyeventserviceentitlementkey)
- [var kIODriverKitHIDTransportEntitlementKey: String](/documentation/iokit/kiodriverkithidtransportentitlementkey)
- [var kIODriverKitRequiredEntitlementsKey: String](/documentation/iokit/kiodriverkitrequiredentitlementskey)
- [var kIODriverKitTestDriverEntitlementKey: String](/documentation/iokit/kiodriverkittestdriverentitlementkey)
- [var kIODriverKitTransportBuiltinEntitlementKey: String](/documentation/iokit/kiodriverkittransportbuiltinentitlementkey)
- [var kIODriverKitUSBTransportEntitlementKey: String](/documentation/iokit/kiodriverkitusbtransportentitlementkey)
- [var kIODriverKitUserClientEntitlementAdministratorKey: String](/documentation/iokit/kiodriverkitusercliententitlementadministratorkey)
- [var kIODriverKitUserClientEntitlementAllowAnyKey: String](/documentation/iokit/kiodriverkitusercliententitlementallowanykey)
- [var kIODriverKitUserClientEntitlementAllowThirdPartyUserClientsKey: String](/documentation/iokit/kiodriverkitusercliententitlementallowthirdpartyuserclientskey)
- [var kIODriverKitUserClientEntitlementCommunicatesWithDriversKey: String](/documentation/iokit/kiodriverkitusercliententitlementcommunicateswithdriverskey)
- [var kIODriverKitUserClientEntitlementsKey: String](/documentation/iokit/kiodriverkitusercliententitlementskey)
- [let kIOMainPortDefault: mach_port_t](/documentation/iokit/kiomainportdefault)
- [var kIOMatchDeferKey: String](/documentation/iokit/kiomatchdeferkey)
- [var kIOMatchedPersonalityKey: String](/documentation/iokit/kiomatchedpersonalitykey)
- [var kIOMaximumSwapWriteKey: String](/documentation/iokit/kiomaximumswapwritekey)
- [var kIONVRAMBootArgsKey: String](/documentation/iokit/kionvrambootargskey)
- [var kIONVRAMDeletePropertyKeyWRet: String](/documentation/iokit/kionvramdeletepropertykeywret)
- [var kIONVRAMReadAccessKey: String](/documentation/iokit/kionvramreadaccesskey)
- [var kIONVRAMSystemAllowKey: String](/documentation/iokit/kionvramsystemallowkey)
- [var kIONVRAMWriteAccessKey: String](/documentation/iokit/kionvramwriteaccesskey)
- [var kIOPathKey: String](/documentation/iokit/kiopathkey)
- [var kIORegistryEntryAllowableSetPropertiesKey: String](/documentation/iokit/kioregistryentryallowablesetpropertieskey)
- [var kIORegistryEntryDefaultLockingSetPropertiesKey: String](/documentation/iokit/kioregistryentrydefaultlockingsetpropertieskey)
- [var kIORematchCountKey: String](/documentation/iokit/kiorematchcountkey)
- [var kIORematchPersonalityKey: String](/documentation/iokit/kiorematchpersonalitykey)
- [var kIOResourcesSetPropertyKey: String](/documentation/iokit/kioresourcessetpropertykey)
- [var kIOServiceDEXTEntitlementsKey: String](/documentation/iokit/kioservicedextentitlementskey)
- [var kIOStateNotificationEntitlementGetKey: String](/documentation/iokit/kiostatenotificationentitlementgetkey)
- [var kIOStateNotificationEntitlementSetKey: String](/documentation/iokit/kiostatenotificationentitlementsetkey)
- [var kIOStateNotificationItemCopyKey: String](/documentation/iokit/kiostatenotificationitemcopykey)
- [var kIOStateNotificationItemCreateKey: String](/documentation/iokit/kiostatenotificationitemcreatekey)
- [var kIOStateNotificationItemSetKey: String](/documentation/iokit/kiostatenotificationitemsetkey)
- [var kIOStateNotificationNameKey: String](/documentation/iokit/kiostatenotificationnamekey)
- [var kIOSupportedPropertiesKey: String](/documentation/iokit/kiosupportedpropertieskey)
- [var kIOSystemStateClamshellKey: String](/documentation/iokit/kiosystemstateclamshellkey)
- [var kIOSystemStateHaltDescriptionHaltStateKey: String](/documentation/iokit/kiosystemstatehaltdescriptionhaltstatekey)
- [var kIOSystemStateHaltDescriptionKey: String](/documentation/iokit/kiosystemstatehaltdescriptionkey)
- [var kIOSystemStatePowerSourceDescriptionACAttachedKey: String](/documentation/iokit/kiosystemstatepowersourcedescriptionacattachedkey)
- [var kIOSystemStatePowerSourceDescriptionKey: String](/documentation/iokit/kiosystemstatepowersourcedescriptionkey)
- [var kIOSystemStateSleepDescriptionHibernateStateKey: String](/documentation/iokit/kiosystemstatesleepdescriptionhibernatestatekey)
- [var kIOSystemStateSleepDescriptionKey: String](/documentation/iokit/kiosystemstatesleepdescriptionkey)
- [var kIOSystemStateSleepDescriptionReasonKey: String](/documentation/iokit/kiosystemstatesleepdescriptionreasonkey)
- [var kIOSystemStateWakeDescriptionContinuousTimeOffsetKey: String](/documentation/iokit/kiosystemstatewakedescriptioncontinuoustimeoffsetkey)
- [var kIOSystemStateWakeDescriptionKey: String](/documentation/iokit/kiosystemstatewakedescriptionkey)
- [var kIOSystemStateWakeDescriptionWakeReasonKey: String](/documentation/iokit/kiosystemstatewakedescriptionwakereasonkey)
- [var kIOUserClassKey: String](/documentation/iokit/kiouserclasskey)
- [var kIOUserClassesKey: String](/documentation/iokit/kiouserclasseskey)
- [var kIOUserClientDefaultLockingKey: String](/documentation/iokit/kiouserclientdefaultlockingkey)
- [var kIOUserClientDefaultLockingSetPropertiesKey: String](/documentation/iokit/kiouserclientdefaultlockingsetpropertieskey)
- [var kIOUserClientDefaultLockingSingleThreadExternalMethodKey: String](/documentation/iokit/kiouserclientdefaultlockingsinglethreadexternalmethodkey)
- [var kIOUserClientEntitlementsKey: String](/documentation/iokit/kiousercliententitlementskey)
- [var kIOUserServerCDHashKey: String](/documentation/iokit/kiouserservercdhashkey)
- [var kIOUserServerClassKey: String](/documentation/iokit/kiouserserverclasskey)
- [var kIOUserServerNameKey: String](/documentation/iokit/kiouserservernamekey)
- [var kIOUserServerOneProcessKey: String](/documentation/iokit/kiouserserveroneprocesskey)
- [var kIOUserServerPreserveUserspaceRebootKey: String](/documentation/iokit/kiouserserverpreserveuserspacerebootkey)
- [var kIOUserServerTagKey: String](/documentation/iokit/kiouserservertagkey)
- [var kIOUserServicePropertiesKey: String](/documentation/iokit/kiouserservicepropertieskey)
- [var kIOUserUserClientKey: String](/documentation/iokit/kiouseruserclientkey)
- [var kIOWillTerminateNotification: String](/documentation/iokit/kiowillterminatenotification)
- [IOKit Functions](/documentation/iokit/iokit_functions)

### Functions

- [func IOCFSerialize(CFTypeRef!, CFOptionFlags) -> CFData!](/documentation/iokit/1403329-iocfserialize)
- [func IOCFUnserialize(UnsafePointer<CChar>!, CFAllocator!, CFOptionFlags, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> CFTypeRef!](/documentation/iokit/1514265-iocfunserialize)
- [func IOCFUnserializeBinary(UnsafePointer<CChar>!, Int, CFAllocator!, CFOptionFlags, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> CFTypeRef!](/documentation/iokit/1514876-iocfunserializebinary)
- [func IOCFUnserializeWithSize(UnsafePointer<CChar>!, Int, CFAllocator!, CFOptionFlags, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> CFTypeRef!](/documentation/iokit/1514745-iocfunserializewithsize)
- [func IOCatalogueGetData(mach_port_t, UInt32, UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>!, UnsafeMutablePointer<UInt32>!) -> kern_return_t](/documentation/iokit/1514233-iocataloguegetdata)
- [func IOCatalogueModuleLoaded(mach_port_t, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514886-iocataloguemoduleloaded)
- [func IOCatalogueReset(mach_port_t, UInt32) -> kern_return_t](/documentation/iokit/1514702-iocataloguereset)
- [func IOCatalogueSendData(mach_port_t, UInt32, UnsafePointer<CChar>!, UInt32) -> kern_return_t](/documentation/iokit/1514405-iocataloguesenddata)
- [func IOCatalogueTerminate(mach_port_t, UInt32, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514665-iocatalogueterminate)
- [func IOConnectCallAsyncMethod(mach_port_t, UInt32, mach_port_t, UnsafeMutablePointer<UInt64>!, UInt32, UnsafePointer<UInt64>!, UInt32, UnsafeRawPointer!, Int, UnsafeMutablePointer<UInt64>!, UnsafeMutablePointer<UInt32>!, UnsafeMutableRawPointer!, UnsafeMutablePointer<Int>!) -> kern_return_t](/documentation/iokit/1514418-ioconnectcallasyncmethod)
- [func IOConnectCallAsyncScalarMethod(mach_port_t, UInt32, mach_port_t, UnsafeMutablePointer<UInt64>!, UInt32, UnsafePointer<UInt64>!, UInt32, UnsafeMutablePointer<UInt64>!, UnsafeMutablePointer<UInt32>!) -> kern_return_t](/documentation/iokit/1514884-ioconnectcallasyncscalarmethod)
- [func IOConnectCallAsyncStructMethod(mach_port_t, UInt32, mach_port_t, UnsafeMutablePointer<UInt64>!, UInt32, UnsafeRawPointer!, Int, UnsafeMutableRawPointer!, UnsafeMutablePointer<Int>!) -> kern_return_t](/documentation/iokit/1514403-ioconnectcallasyncstructmethod)
- [func IOConnectCallMethod(mach_port_t, UInt32, UnsafePointer<UInt64>!, UInt32, UnsafeRawPointer!, Int, UnsafeMutablePointer<UInt64>!, UnsafeMutablePointer<UInt32>!, UnsafeMutableRawPointer!, UnsafeMutablePointer<Int>!) -> kern_return_t](/documentation/iokit/1514240-ioconnectcallmethod)
- [func IOConnectCallScalarMethod(mach_port_t, UInt32, UnsafePointer<UInt64>!, UInt32, UnsafeMutablePointer<UInt64>!, UnsafeMutablePointer<UInt32>!) -> kern_return_t](/documentation/iokit/1514793-ioconnectcallscalarmethod)
- [func IOConnectCallStructMethod(mach_port_t, UInt32, UnsafeRawPointer!, Int, UnsafeMutableRawPointer!, UnsafeMutablePointer<Int>!) -> kern_return_t](/documentation/iokit/1514274-ioconnectcallstructmethod)
- [func IOConnectTrap0(io_connect_t, UInt32) -> kern_return_t](/documentation/iokit/1514674-ioconnecttrap0)
- [func IOConnectTrap1(io_connect_t, UInt32, UInt) -> kern_return_t](/documentation/iokit/1514816-ioconnecttrap1)
- [func IOConnectTrap2(io_connect_t, UInt32, UInt, UInt) -> kern_return_t](/documentation/iokit/1514354-ioconnecttrap2)
- [func IOConnectTrap3(io_connect_t, UInt32, UInt, UInt, UInt) -> kern_return_t](/documentation/iokit/1514833-ioconnecttrap3)
- [func IOConnectTrap4(io_connect_t, UInt32, UInt, UInt, UInt, UInt) -> kern_return_t](/documentation/iokit/1514410-ioconnecttrap4)
- [func IOConnectTrap5(io_connect_t, UInt32, UInt, UInt, UInt, UInt, UInt) -> kern_return_t](/documentation/iokit/1514346-ioconnecttrap5)
- [func IOConnectTrap6(io_connect_t, UInt32, UInt, UInt, UInt, UInt, UInt, UInt) -> kern_return_t](/documentation/iokit/1514493-ioconnecttrap6)
- [func IOCreatePlugInInterfaceForService(io_service_t, CFUUID!, CFUUID!, UnsafeMutablePointer<UnsafeMutablePointer<UnsafeMutablePointer<IOCFPlugInInterface>?>?>!, UnsafeMutablePointer<Int32>!) -> kern_return_t](/documentation/iokit/1412429-iocreateplugininterfaceforservic)
- [func IODestroyPlugInInterface(UnsafeMutablePointer<UnsafeMutablePointer<IOCFPlugInInterface>?>!) -> kern_return_t](/documentation/iokit/1412425-iodestroyplugininterface)
- [func IOOpenFirmwarePathMatching(mach_port_t, UInt32, UnsafePointer<CChar>!) -> Unmanaged<CFMutableDictionary>!](/documentation/iokit/1514715-ioopenfirmwarepathmatching)
- [func IORegistryEntryCopyFromPath(mach_port_t, CFString!) -> io_registry_entry_t](/documentation/iokit/1514248-ioregistryentrycopyfrompath)
- [func IORegistryEntryCopyPath(io_registry_entry_t, UnsafePointer<CChar>!) -> Unmanaged<CFString>!](/documentation/iokit/1514853-ioregistryentrycopypath)
- [func IORegistryEntryGetProperty(io_registry_entry_t, UnsafePointer<CChar>!, UnsafeMutablePointer<CChar>!, UnsafeMutablePointer<UInt32>!) -> kern_return_t](/documentation/iokit/1514254-ioregistryentrygetproperty)
- [func IOServiceAddNotification(mach_port_t, UnsafePointer<CChar>!, CFDictionary!, mach_port_t, UInt, UnsafeMutablePointer<io_iterator_t>!) -> kern_return_t](/documentation/iokit/1514382-ioserviceaddnotification)
- [func IOServiceAuthorize(io_service_t, UInt32) -> kern_return_t](/documentation/iokit/1514533-ioserviceauthorize)
- [func IOServiceOFPathToBSDName(mach_port_t, UnsafePointer<CChar>!, UnsafeMutablePointer<CChar>!) -> kern_return_t](/documentation/iokit/1514661-ioserviceofpathtobsdname)
- [func IOServiceOpenAsFileDescriptor(io_service_t, Int32) -> Int32](/documentation/iokit/1514879-ioserviceopenasfiledescriptor)
- [func IOURLCreateDataAndPropertiesFromResource(CFAllocator!, CFURL!, UnsafeMutablePointer<Unmanaged<CFData>?>!, UnsafeMutablePointer<Unmanaged<CFDictionary>?>!, CFArray!, UnsafeMutablePointer<Int32>!) -> Bool](/documentation/iokit/1514836-iourlcreatedataandpropertiesfrom)
- [func IOURLCreatePropertyFromResource(CFAllocator!, CFURL!, CFString!, UnsafeMutablePointer<Int32>!) -> Unmanaged<CFTypeRef>!](/documentation/iokit/1514499-iourlcreatepropertyfromresource)
- [func IOURLWriteDataAndPropertiesToResource(CFURL!, CFData!, CFDictionary!, UnsafeMutablePointer<Int32>!) -> Bool](/documentation/iokit/1514272-iourlwritedataandpropertiestores)
- [func OSGetNotificationFromMessage(UnsafeMutablePointer<mach_msg_header_t>!, UInt32, UnsafeMutablePointer<UInt32>!, UnsafeMutablePointer<UInt>!, UnsafeMutablePointer<UnsafeMutableRawPointer?>!, UnsafeMutablePointer<vm_size_t>!) -> kern_return_t](/documentation/iokit/1514263-osgetnotificationfrommessage)
- [func IOMainPort(mach_port_t, UnsafeMutablePointer<mach_port_t>!) -> kern_return_t](/documentation/iokit/3753260-iomainport)
- [func IONotificationPortSetImportanceReceiver(IONotificationPortRef!) -> kern_return_t](/documentation/iokit/2870065-ionotificationportsetimportancer)
- [func IORPCMessageFromMach(UnsafeMutablePointer<IORPCMessageMach>!, Bool) -> UnsafeMutablePointer<IORPCMessage>!](/documentation/iokit/3325691-iorpcmessagefrommach)
- [IOKit Data Types](/documentation/iokit/iokit_data_types)

### Data Types

- [IOAddressRange](/documentation/iokit/ioaddressrange)
- [IOAlignment](/documentation/iokit/ioalignment)
- [IOByteCount](/documentation/iokit/iobytecount)
- [IOByteCount32](/documentation/iokit/iobytecount32)
- [IOByteCount64](/documentation/iokit/iobytecount64)
- [IOCFPlugInInterfaceStruct](/documentation/iokit/iocfplugininterfacestruct)

#### Initializers

- [init()](/documentation/iokit/iocfplugininterfacestruct/1514869-init)
- [init(_reserved: UnsafeMutableRawPointer!, QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!, AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!, Release: ((UnsafeMutableRawPointer?) -> ULONG)!, version: UInt16, revision: UInt16, Probe: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t, UnsafeMutablePointer<Int32>?) -> IOReturn)!, Start: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t) -> IOReturn)!, Stop: ((UnsafeMutableRawPointer?) -> IOReturn)!)](/documentation/iokit/iocfplugininterfacestruct/1792000-init)

#### Instance Properties

- [var AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/iokit/iocfplugininterfacestruct/1412440-addref)
- [var Probe: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t, UnsafeMutablePointer<Int32>?) -> IOReturn)!](/documentation/iokit/iocfplugininterfacestruct/1412435-probe)
- [var QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!](/documentation/iokit/iocfplugininterfacestruct/1412423-queryinterface)
- [var Release: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/iokit/iocfplugininterfacestruct/1412422-release)
- [var Start: ((UnsafeMutableRawPointer?, CFDictionary?, io_service_t) -> IOReturn)!](/documentation/iokit/iocfplugininterfacestruct/1412433-start)
- [var Stop: ((UnsafeMutableRawPointer?) -> IOReturn)!](/documentation/iokit/iocfplugininterfacestruct/1412438-stop)
- [var revision: UInt16](/documentation/iokit/iocfplugininterfacestruct/1412427-revision)
- [var version: UInt16](/documentation/iokit/iocfplugininterfacestruct/1412436-version)
- [IOCacheMode](/documentation/iokit/iocachemode)
- [IODataQueueAppendix](/documentation/iokit/iodataqueueappendix)
- [IODataQueueEntry](/documentation/iokit/iodataqueueentry)
- [IODataQueueMemory](/documentation/iokit/iodataqueuememory)
- [IODeviceNumber](/documentation/iokit/iodevicenumber)
- [IOFixed](/documentation/iokit/iofixed)
- [IOItemCount](/documentation/iokit/ioitemcount)
- [IOLogicalAddress](/documentation/iokit/iologicaladdress)
- [IOMessage](/documentation/iokit/iomessage)
- [IONotificationPortRef](/documentation/iokit/ionotificationportref)
- [IOOptionBits](/documentation/iokit/iooptionbits)
- [IOPhysicalAddress](/documentation/iokit/iophysicaladdress)
- [IOPhysicalAddress32](/documentation/iokit/iophysicaladdress32)
- [IOPhysicalAddress64](/documentation/iokit/iophysicaladdress64)
- [IOPhysicalLength](/documentation/iokit/iophysicallength)
- [IOPhysicalLength32](/documentation/iokit/iophysicallength32)
- [IOPhysicalLength64](/documentation/iokit/iophysicallength64)
- [IOReturn](/documentation/iokit/ioreturn)
- [IOServiceInterestContent64](/documentation/iokit/ioserviceinterestcontent64)

#### Instance Properties

- [var messageArgument: io_user_reference_t](/documentation/iokit/ioserviceinterestcontent64/1455540-messageargument)
- [var messageType: natural_t](/documentation/iokit/ioserviceinterestcontent64/1455516-messagetype)

#### Initializers

- [init()](/documentation/iokit/ioserviceinterestcontent64/1514849-init)
- [init(messageType: natural_t, messageArgument: io_user_reference_t)](/documentation/iokit/ioserviceinterestcontent64/1514569-init)
- [IOVersion](/documentation/iokit/ioversion)
- [IOVirtualAddress](/documentation/iokit/iovirtualaddress)
- [OSAsyncReference](/documentation/iokit/osasyncreference)
- [OSAsyncReference64](/documentation/iokit/osasyncreference64)
- [OSNotificationHeader64](/documentation/iokit/osnotificationheader64)

#### Instance Properties

- [var reference: OSAsyncReference64](/documentation/iokit/osnotificationheader64/1455547-reference)
- [var size: mach_msg_size_t](/documentation/iokit/osnotificationheader64/1455592-size)
- [var type: natural_t](/documentation/iokit/osnotificationheader64/1455613-type)

#### Initializers

- [init()](/documentation/iokit/osnotificationheader64/1514395-init)
- [io_connect_t](/documentation/iokit/io_connect_t)
- [io_enumerator_t](/documentation/iokit/io_enumerator_t)
- [io_iterator_t](/documentation/iokit/io_iterator_t)
- [io_object_t](/documentation/iokit/io_object_t)
- [io_registry_entry_t](/documentation/iokit/io_registry_entry_t)
- [io_service_t](/documentation/iokit/io_service_t)
- [OSObjectRef](/documentation/iokit/osobjectref)
- [io_ident_t](/documentation/iokit/io_ident_t)
- [uext_object_t](/documentation/iokit/uext_object_t)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
