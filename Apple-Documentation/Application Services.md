# Application Services Documentation

Source: https://sosumi.ai/documentation/applicationservices

---
title: Application Services
source: https://developer.apple.com/documentation/applicationservices
timestamp: 2026-02-13T18:53:50.206Z
---

## Managers

- [Apple Event Manager](/documentation/applicationservices/apple_event_manager)

### Adding Items to Descriptor Lists

- [func AEPutArray(UnsafeMutablePointer<AEDescList>!, AEArrayType, UnsafePointer<AEArrayData>!, DescType, Size, Int) -> OSErr](/documentation/coreservices/1442535-aeputarray)
- [func AEPutDesc(UnsafeMutablePointer<AEDescList>!, Int, UnsafePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1450093-aeputdesc)
- [func AEPutPtr(UnsafeMutablePointer<AEDescList>!, Int, DescType, UnsafeRawPointer!, Size) -> OSErr](/documentation/coreservices/1445287-aeputptr)

### Adding Parameters and Attributes to Apple Events and Apple Event Records

- [func AEPutAttributeDesc(UnsafeMutablePointer<AppleEvent>!, AEKeyword, UnsafePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1441790-aeputattributedesc)
- [func AEPutAttributePtr(UnsafeMutablePointer<AppleEvent>!, AEKeyword, DescType, UnsafeRawPointer!, Size) -> OSErr](/documentation/coreservices/1445940-aeputattributeptr)
- [func AEPutParamDesc(UnsafeMutablePointer<AppleEvent>!, AEKeyword, UnsafePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1447576-aeputparamdesc)
- [func AEPutParamPtr(UnsafeMutablePointer<AppleEvent>!, AEKeyword, DescType, UnsafeRawPointer!, Size) -> OSErr](/documentation/coreservices/1449263-aeputparamptr)

### Coercing Descriptor Types

- [func AECoerceDesc(UnsafePointer<AEDesc>!, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1446519-aecoercedesc)
- [func AECoercePtr(DescType, UnsafeRawPointer!, Size, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1441846-aecoerceptr)

### Counting the Items in Descriptor Lists

- [func AECountItems(UnsafePointer<AEDescList>!, UnsafeMutablePointer<Int>!) -> OSErr](/documentation/coreservices/1449533-aecountitems)

### Creating an Apple Event

- [func AECreateAppleEvent(AEEventClass, AEEventID, UnsafePointer<AEAddressDesc>!, AEReturnID, AETransactionID, UnsafeMutablePointer<AppleEvent>!) -> OSErr](/documentation/coreservices/1448525-aecreateappleevent)

### Creating and Duplicating Descriptors

- [func AECreateDesc(DescType, UnsafeRawPointer!, Size, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1448535-aecreatedesc)
- [func AECreateDescFromExternalPtr(OSType, UnsafeRawPointer!, Size, AEDisposeExternalUPP!, SRefCon!, UnsafeMutablePointer<AEDesc>!) -> OSStatus](/documentation/coreservices/1446239-aecreatedescfromexternalptr)
- [func AEDuplicateDesc(UnsafePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1442661-aeduplicatedesc)

### Creating, Calling, and Deleting Universal Procedure Pointers

- [func DisposeAECoerceDescUPP(AECoerceDescUPP!)](/documentation/coreservices/1448721-disposeaecoercedescupp)
- [func DisposeAECoercePtrUPP(AECoercePtrUPP!)](/documentation/coreservices/1450664-disposeaecoerceptrupp)
- [func DisposeAEDisposeExternalUPP(AEDisposeExternalUPP!)](/documentation/coreservices/1447284-disposeaedisposeexternalupp)
- [func DisposeAEEventHandlerUPP(AEEventHandlerUPP!)](/documentation/coreservices/1442066-disposeaeeventhandlerupp)
- [func DisposeOSLAccessorUPP(OSLAccessorUPP!)](/documentation/coreservices/1444684-disposeoslaccessorupp)
- [func DisposeOSLAdjustMarksUPP(OSLAdjustMarksUPP!)](/documentation/coreservices/1443940-disposeosladjustmarksupp)
- [func DisposeOSLCompareUPP(OSLCompareUPP!)](/documentation/coreservices/1448398-disposeoslcompareupp)
- [func DisposeOSLCountUPP(OSLCountUPP!)](/documentation/coreservices/1443984-disposeoslcountupp)
- [func DisposeOSLDisposeTokenUPP(OSLDisposeTokenUPP!)](/documentation/coreservices/1442670-disposeosldisposetokenupp)
- [func DisposeOSLGetErrDescUPP(OSLGetErrDescUPP!)](/documentation/coreservices/1446061-disposeoslgeterrdescupp)
- [func DisposeOSLGetMarkTokenUPP(OSLGetMarkTokenUPP!)](/documentation/coreservices/1442377-disposeoslgetmarktokenupp)
- [func DisposeOSLMarkUPP(OSLMarkUPP!)](/documentation/coreservices/1449253-disposeoslmarkupp)
- [func InvokeAECoerceDescUPP(UnsafePointer<AEDesc>!, DescType, SRefCon!, UnsafeMutablePointer<AEDesc>!, AECoerceDescUPP!) -> OSErr](/documentation/coreservices/1445450-invokeaecoercedescupp)
- [func InvokeAECoercePtrUPP(DescType, UnsafeRawPointer!, Size, DescType, SRefCon!, UnsafeMutablePointer<AEDesc>!, AECoercePtrUPP!) -> OSErr](/documentation/coreservices/1447079-invokeaecoerceptrupp)
- [func InvokeAEDisposeExternalUPP(UnsafeRawPointer!, Size, SRefCon!, AEDisposeExternalUPP!)](/documentation/coreservices/1441717-invokeaedisposeexternalupp)
- [func InvokeAEEventHandlerUPP(UnsafePointer<AppleEvent>!, UnsafeMutablePointer<AppleEvent>!, SRefCon!, AEEventHandlerUPP!) -> OSErr](/documentation/coreservices/1446585-invokeaeeventhandlerupp)
- [func InvokeOSLAccessorUPP(DescType, UnsafePointer<AEDesc>!, DescType, DescType, UnsafePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!, SRefCon!, OSLAccessorUPP!) -> OSErr](/documentation/coreservices/1448978-invokeoslaccessorupp)
- [func InvokeOSLAdjustMarksUPP(Int, Int, UnsafePointer<AEDesc>!, OSLAdjustMarksUPP!) -> OSErr](/documentation/coreservices/1448506-invokeosladjustmarksupp)
- [func InvokeOSLCompareUPP(DescType, UnsafePointer<AEDesc>!, UnsafePointer<AEDesc>!, UnsafeMutablePointer<DarwinBoolean>!, OSLCompareUPP!) -> OSErr](/documentation/coreservices/1443110-invokeoslcompareupp)
- [func InvokeOSLCountUPP(DescType, DescType, UnsafePointer<AEDesc>!, UnsafeMutablePointer<Int>!, OSLCountUPP!) -> OSErr](/documentation/coreservices/1448030-invokeoslcountupp)
- [func InvokeOSLDisposeTokenUPP(UnsafeMutablePointer<AEDesc>!, OSLDisposeTokenUPP!) -> OSErr](/documentation/coreservices/1443963-invokeosldisposetokenupp)
- [func InvokeOSLGetErrDescUPP(UnsafeMutablePointer<UnsafeMutablePointer<AEDesc>?>!, OSLGetErrDescUPP!) -> OSErr](/documentation/coreservices/1448420-invokeoslgeterrdescupp)
- [func InvokeOSLGetMarkTokenUPP(UnsafePointer<AEDesc>!, DescType, UnsafeMutablePointer<AEDesc>!, OSLGetMarkTokenUPP!) -> OSErr](/documentation/coreservices/1441894-invokeoslgetmarktokenupp)
- [func InvokeOSLMarkUPP(UnsafePointer<AEDesc>!, UnsafePointer<AEDesc>!, Int, OSLMarkUPP!) -> OSErr](/documentation/coreservices/1447444-invokeoslmarkupp)
- [func NewAECoerceDescUPP(AECoerceDescProcPtr!) -> AECoerceDescUPP!](/documentation/coreservices/1445885-newaecoercedescupp)
- [func NewAECoercePtrUPP(AECoercePtrProcPtr!) -> AECoercePtrUPP!](/documentation/coreservices/1449962-newaecoerceptrupp)
- [func NewAEDisposeExternalUPP(AEDisposeExternalProcPtr!) -> AEDisposeExternalUPP!](/documentation/coreservices/1447774-newaedisposeexternalupp)
- [func NewAEEventHandlerUPP(AEEventHandlerProcPtr!) -> AEEventHandlerUPP!](/documentation/coreservices/1446862-newaeeventhandlerupp)
- [func NewOSLAccessorUPP(OSLAccessorProcPtr!) -> OSLAccessorUPP!](/documentation/coreservices/1449584-newoslaccessorupp)
- [func NewOSLAdjustMarksUPP(OSLAdjustMarksProcPtr!) -> OSLAdjustMarksUPP!](/documentation/coreservices/1443347-newosladjustmarksupp)
- [func NewOSLCompareUPP(OSLCompareProcPtr!) -> OSLCompareUPP!](/documentation/coreservices/1444603-newoslcompareupp)
- [func NewOSLCountUPP(OSLCountProcPtr!) -> OSLCountUPP!](/documentation/coreservices/1448156-newoslcountupp)
- [func NewOSLDisposeTokenUPP(OSLDisposeTokenProcPtr!) -> OSLDisposeTokenUPP!](/documentation/coreservices/1450027-newosldisposetokenupp)
- [func NewOSLGetErrDescUPP(OSLGetErrDescProcPtr!) -> OSLGetErrDescUPP!](/documentation/coreservices/1447934-newoslgeterrdescupp)
- [func NewOSLGetMarkTokenUPP(OSLGetMarkTokenProcPtr!) -> OSLGetMarkTokenUPP!](/documentation/coreservices/1445166-newoslgetmarktokenupp)
- [func NewOSLMarkUPP(OSLMarkProcPtr!) -> OSLMarkUPP!](/documentation/coreservices/1446942-newoslmarkupp)

### Creating Descriptor Lists and Apple Event Records

- [func AECreateList(UnsafeRawPointer!, Size, Bool, UnsafeMutablePointer<AEDescList>!) -> OSErr](/documentation/coreservices/1448643-aecreatelist)

### Creating Object Specifiers

- [func CreateCompDescriptor(DescType, UnsafeMutablePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1449155-createcompdescriptor)
- [func CreateLogicalDescriptor(UnsafeMutablePointer<AEDescList>!, DescType, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1445212-createlogicaldescriptor)
- [func CreateObjSpecifier(DescType, UnsafeMutablePointer<AEDesc>!, DescType, UnsafeMutablePointer<AEDesc>!, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1450244-createobjspecifier)
- [func CreateOffsetDescriptor(Int, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1444957-createoffsetdescriptor)
- [func CreateRangeDescriptor(UnsafeMutablePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1444087-createrangedescriptor)

### Deallocating Memory for Descriptors

- [func AEDisposeDesc(UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1444208-aedisposedesc)

### Deallocating Memory for Tokens

- [func AEDisposeToken(UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1446783-aedisposetoken)

### Deleting Descriptors

- [func AEDeleteItem(UnsafeMutablePointer<AEDescList>!, Int) -> OSErr](/documentation/coreservices/1447164-aedeleteitem)
- [func AEDeleteParam(UnsafeMutablePointer<AppleEvent>!, AEKeyword) -> OSErr](/documentation/coreservices/1444338-aedeleteparam)

### Getting, Calling, and Removing Object Accessor Functions

- [func AECallObjectAccessor(DescType, UnsafePointer<AEDesc>!, DescType, DescType, UnsafePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1447059-aecallobjectaccessor)
- [func AEGetObjectAccessor(DescType, DescType, UnsafeMutablePointer<OSLAccessorUPP?>!, UnsafeMutablePointer<SRefCon?>!, Bool) -> OSErr](/documentation/coreservices/1449054-aegetobjectaccessor)
- [func AEInstallObjectAccessor(DescType, DescType, OSLAccessorUPP!, SRefCon!, Bool) -> OSErr](/documentation/coreservices/1447905-aeinstallobjectaccessor)
- [func AERemoveObjectAccessor(DescType, DescType, OSLAccessorUPP!, Bool) -> OSErr](/documentation/coreservices/1442552-aeremoveobjectaccessor)

### Getting Data or Descriptors From Apple Events and Apple Event Records

- [func AEGetAttributeDesc(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1450314-aegetattributedesc)
- [func AEGetAttributePtr(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<DescType>!, UnsafeMutableRawPointer!, Size, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1445109-aegetattributeptr)
- [func AEGetParamDesc(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1449233-aegetparamdesc)
- [func AEGetParamPtr(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<DescType>!, UnsafeMutableRawPointer!, Size, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1444069-aegetparamptr)

### Getting Information About the Apple Event Manager

- [func AEManagerInfo(AEKeyword, UnsafeMutablePointer<Int>!) -> OSErr](/documentation/coreservices/1449373-aemanagerinfo)

### Getting Items From Descriptor Lists

- [func AEGetArray(UnsafePointer<AEDescList>!, AEArrayType, AEArrayDataPointer!, Size, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!, UnsafeMutablePointer<Int>!) -> OSErr](/documentation/coreservices/1445720-aegetarray)
- [func AEGetNthDesc(UnsafePointer<AEDescList>!, Int, DescType, UnsafeMutablePointer<AEKeyword>!, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1448326-aegetnthdesc)
- [func AEGetNthPtr(UnsafePointer<AEDescList>!, Int, DescType, UnsafeMutablePointer<AEKeyword>!, UnsafeMutablePointer<DescType>!, UnsafeMutableRawPointer!, Size, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1447539-aegetnthptr)

### Getting the Sizes and Descriptor Types of Descriptors

- [func AESizeOfAttribute(UnsafePointer<AppleEvent>!, AEKeyword, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1445764-aesizeofattribute)
- [func AESizeOfNthItem(UnsafePointer<AEDescList>!, Int, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1447307-aesizeofnthitem)
- [func AESizeOfParam(UnsafePointer<AppleEvent>!, AEKeyword, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1449998-aesizeofparam)

### Initializing the Object Support Library

- [func AEObjectInit() -> OSErr](/documentation/coreservices/1447372-aeobjectinit)
- [func AESetObjectCallbacks(OSLCompareUPP!, OSLCountUPP!, OSLDisposeTokenUPP!, OSLGetMarkTokenUPP!, OSLMarkUPP!, OSLAdjustMarksUPP!, OSLGetErrDescUPP!) -> OSErr](/documentation/coreservices/1447756-aesetobjectcallbacks)

### Locating Processes on Remote Computers

- [func AECreateRemoteProcessResolver(CFAllocator!, CFURL!) -> AERemoteProcessResolverRef!](/documentation/coreservices/1445692-aecreateremoteprocessresolver)
- [func AEDisposeRemoteProcessResolver(AERemoteProcessResolverRef!)](/documentation/coreservices/1442572-aedisposeremoteprocessresolver)
- [func AERemoteProcessResolverGetProcesses(AERemoteProcessResolverRef!, UnsafeMutablePointer<CFStreamError>!) -> Unmanaged<CFArray>!](/documentation/coreservices/1444456-aeremoteprocessresolvergetproces)
- [func AERemoteProcessResolverScheduleWithRunLoop(AERemoteProcessResolverRef!, CFRunLoop!, CFString!, AERemoteProcessResolverCallback!, UnsafePointer<AERemoteProcessResolverContext>!)](/documentation/coreservices/1447259-aeremoteprocessresolverschedulew)

### Managing Apple Event Dispatch Tables

- [func AEGetEventHandler(AEEventClass, AEEventID, UnsafeMutablePointer<AEEventHandlerUPP?>!, UnsafeMutablePointer<SRefCon?>!, Bool) -> OSErr](/documentation/coreservices/1445631-aegeteventhandler)
- [func AEInstallEventHandler(AEEventClass, AEEventID, AEEventHandlerUPP!, SRefCon!, Bool) -> OSErr](/documentation/coreservices/1448596-aeinstalleventhandler)
- [func AERemoveEventHandler(AEEventClass, AEEventID, AEEventHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1445239-aeremoveeventhandler)

### Managing Coercion Handler Dispatch Tables

- [func AEGetCoercionHandler(DescType, DescType, UnsafeMutablePointer<AECoercionHandlerUPP?>!, UnsafeMutablePointer<SRefCon?>!, UnsafeMutablePointer<DarwinBoolean>!, Bool) -> OSErr](/documentation/coreservices/1445348-aegetcoercionhandler)
- [func AEInstallCoercionHandler(DescType, DescType, AECoercionHandlerUPP!, SRefCon!, Bool, Bool) -> OSErr](/documentation/coreservices/1445548-aeinstallcoercionhandler)
- [func AERemoveCoercionHandler(DescType, DescType, AECoercionHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1441907-aeremovecoercionhandler)

### Managing Special Handler Dispatch Tables

- [func AEGetSpecialHandler(AEKeyword, UnsafeMutablePointer<AEEventHandlerUPP?>!, Bool) -> OSErr](/documentation/coreservices/1444274-aegetspecialhandler)
- [func AEInstallSpecialHandler(AEKeyword, AEEventHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1445532-aeinstallspecialhandler)
- [func AERemoveSpecialHandler(AEKeyword, AEEventHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1447960-aeremovespecialhandler)

### Operating On Descriptor Data

- [func AEGetDescData(UnsafePointer<AEDesc>!, UnsafeMutableRawPointer!, Size) -> OSErr](/documentation/coreservices/1444427-aegetdescdata)
- [func AEGetDescDataSize(UnsafePointer<AEDesc>!) -> Size](/documentation/coreservices/1450119-aegetdescdatasize)
- [func AEGetDescDataRange(UnsafePointer<AEDesc>!, UnsafeMutableRawPointer!, Size, Size) -> OSStatus](/documentation/coreservices/1446560-aegetdescdatarange)
- [func AEReplaceDescData(DescType, UnsafeRawPointer!, Size, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1446695-aereplacedescdata)

### Resolving Object Specifiers

- [func AEResolve(UnsafePointer<AEDesc>!, Int16, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1449720-aeresolve)

### Creating Apple Event Structures in Memory

- [func AEPrintDescToHandle(UnsafePointer<AEDesc>!, UnsafeMutablePointer<Handle?>!) -> OSStatus](/documentation/coreservices/1445158-aeprintdesctohandle)
- [func vAEBuildAppleEvent(AEEventClass, AEEventID, DescType, UnsafeRawPointer!, Size, Int16, Int32, UnsafeMutablePointer<AppleEvent>!, UnsafeMutablePointer<AEBuildError>!, UnsafePointer<CChar>!, CVaListPointer) -> OSStatus](/documentation/coreservices/1441729-vaebuildappleevent)
- [func vAEBuildDesc(UnsafeMutablePointer<AEDesc>!, UnsafeMutablePointer<AEBuildError>!, UnsafePointer<CChar>!, CVaListPointer) -> OSStatus](/documentation/coreservices/1446775-vaebuilddesc)
- [func vAEBuildParameters(UnsafeMutablePointer<AppleEvent>!, UnsafeMutablePointer<AEBuildError>!, UnsafePointer<CChar>!, CVaListPointer) -> OSStatus](/documentation/coreservices/1448040-vaebuildparameters)

### Creating Apple Event Structures Using Streams

- [func AEStreamClose(AEStreamRef!, UnsafeMutablePointer<AEDesc>!) -> OSStatus](/documentation/coreservices/1449821-aestreamclose)
- [func AEStreamCloseDesc(AEStreamRef!) -> OSStatus](/documentation/coreservices/1449272-aestreamclosedesc)
- [func AEStreamCloseList(AEStreamRef!) -> OSStatus](/documentation/coreservices/1448185-aestreamcloselist)
- [func AEStreamCloseRecord(AEStreamRef!) -> OSStatus](/documentation/coreservices/1449522-aestreamcloserecord)
- [func AEStreamCreateEvent(AEEventClass, AEEventID, DescType, UnsafeRawPointer!, Size, Int16, Int32) -> AEStreamRef!](/documentation/coreservices/1446562-aestreamcreateevent)
- [func AEStreamOpen() -> AEStreamRef!](/documentation/coreservices/1447732-aestreamopen)
- [func AEStreamOpenDesc(AEStreamRef!, DescType) -> OSStatus](/documentation/coreservices/1446544-aestreamopendesc)
- [func AEStreamOpenEvent(UnsafeMutablePointer<AppleEvent>!) -> AEStreamRef!](/documentation/coreservices/1445366-aestreamopenevent)
- [func AEStreamOpenKeyDesc(AEStreamRef!, AEKeyword, DescType) -> OSStatus](/documentation/coreservices/1442897-aestreamopenkeydesc)
- [func AEStreamOpenList(AEStreamRef!) -> OSStatus](/documentation/coreservices/1448594-aestreamopenlist)
- [func AEStreamOpenRecord(AEStreamRef!, DescType) -> OSStatus](/documentation/coreservices/1447141-aestreamopenrecord)
- [func AEStreamOptionalParam(AEStreamRef!, AEKeyword) -> OSStatus](/documentation/coreservices/1444481-aestreamoptionalparam)
- [func AEStreamSetRecordType(AEStreamRef!, DescType) -> OSStatus](/documentation/coreservices/1447704-aestreamsetrecordtype)
- [func AEStreamWriteAEDesc(AEStreamRef!, UnsafePointer<AEDesc>!) -> OSStatus](/documentation/coreservices/1448487-aestreamwriteaedesc)
- [func AEStreamWriteData(AEStreamRef!, UnsafeRawPointer!, Size) -> OSStatus](/documentation/coreservices/1442610-aestreamwritedata)
- [func AEStreamWriteDesc(AEStreamRef!, DescType, UnsafeRawPointer!, Size) -> OSStatus](/documentation/coreservices/1450387-aestreamwritedesc)
- [func AEStreamWriteKey(AEStreamRef!, AEKeyword) -> OSStatus](/documentation/coreservices/1448750-aestreamwritekey)
- [func AEStreamWriteKeyDesc(AEStreamRef!, AEKeyword, DescType, UnsafeRawPointer!, Size) -> OSStatus](/documentation/coreservices/1442568-aestreamwritekeydesc)

### Working With Lower Level Apple Event Functions

- [func AEGetRegisteredMachPort() -> mach_port_t](/documentation/coreservices/1449736-aegetregisteredmachport)
- [func AEDecodeMessage(UnsafeMutablePointer<mach_msg_header_t>!, UnsafeMutablePointer<AppleEvent>!, UnsafeMutablePointer<AppleEvent>!) -> OSStatus](/documentation/coreservices/1447827-aedecodemessage)
- [func AESendMessage(UnsafePointer<AppleEvent>!, UnsafeMutablePointer<AppleEvent>!, AESendMode, Int) -> OSStatus](/documentation/coreservices/1442994-aesendmessage)
- [func AEProcessMessage(UnsafeMutablePointer<mach_msg_header_t>!) -> OSStatus](/documentation/coreservices/1444387-aeprocessmessage)

### Serializing Apple Event Data

- [func AESizeOfFlattenedDesc(UnsafePointer<AEDesc>!) -> Size](/documentation/coreservices/1447305-aesizeofflatteneddesc)
- [func AEFlattenDesc(UnsafePointer<AEDesc>!, Ptr!, Size, UnsafeMutablePointer<Size>!) -> OSStatus](/documentation/coreservices/1441808-aeflattendesc)
- [func AEUnflattenDesc(UnsafeRawPointer!, UnsafeMutablePointer<AEDesc>!) -> OSStatus](/documentation/coreservices/1448997-aeunflattendesc)

### Miscellaneous

- [func AECheckIsRecord(UnsafePointer<AEDesc>!) -> Bool](/documentation/coreservices/1444011-aecheckisrecord)
- [func AEInitializeDesc(UnsafeMutablePointer<AEDesc>!)](/documentation/coreservices/1446047-aeinitializedesc)

### Callbacks

- [AERemoteProcessResolverCallback](/documentation/coreservices/aeremoteprocessresolvercallback)
- [AEDisposeExternalProcPtr](/documentation/coreservices/aedisposeexternalprocptr)
- [AECoerceDescProcPtr](/documentation/coreservices/aecoercedescprocptr)
- [AECoercePtrProcPtr](/documentation/coreservices/aecoerceptrprocptr)
- [AEEventHandlerProcPtr](/documentation/coreservices/aeeventhandlerprocptr)
- [OSLAccessorProcPtr](/documentation/coreservices/oslaccessorprocptr)
- [OSLAdjustMarksProcPtr](/documentation/coreservices/osladjustmarksprocptr)
- [OSLCompareProcPtr](/documentation/coreservices/oslcompareprocptr)
- [OSLCountProcPtr](/documentation/coreservices/oslcountprocptr)
- [OSLDisposeTokenProcPtr](/documentation/coreservices/osldisposetokenprocptr)
- [OSLGetErrDescProcPtr](/documentation/coreservices/oslgeterrdescprocptr)
- [OSLGetMarkTokenProcPtr](/documentation/coreservices/oslgetmarktokenprocptr)
- [OSLMarkProcPtr](/documentation/coreservices/oslmarkprocptr)

### Data Types

- [AEArrayData](/documentation/coreservices/aearraydata)
- [AEBuildError](/documentation/coreservices/aebuilderror)
- [AEDesc](/documentation/coreservices/aedesc)
- [AEKeyDesc](/documentation/coreservices/aekeydesc)
- [AERemoteProcessResolverContext](/documentation/coreservices/aeremoteprocessresolvercontext)
- [ccntTokenRecord](/documentation/coreservices/ccnttokenrecord)
- [IntlText](/documentation/coreservices/intltext)
- [OffsetArray](/documentation/coreservices/offsetarray)
- [TextRange](/documentation/coreservices/textrange)
- [TextRangeArray](/documentation/coreservices/textrangearray)
- [TScriptingSizeResource](/documentation/coreservices/tscriptingsizeresource)
- [WritingCode](/documentation/coreservices/writingcode)
- [AEAddressDesc](/documentation/coreservices/aeaddressdesc)
- [AEArrayDataPointer](/documentation/coreservices/aearraydatapointer)
- [AEArrayType](/documentation/coreservices/aearraytype)
- [AECoerceDescUPP](/documentation/coreservices/aecoercedescupp)
- [AECoercePtrUPP](/documentation/coreservices/aecoerceptrupp)
- [AECoercionHandlerUPP](/documentation/coreservices/aecoercionhandlerupp)
- [AEDataStorage](/documentation/coreservices/aedatastorage)
- [AEDataStorageType](/documentation/coreservices/aedatastoragetype)
- [AEDescList](/documentation/coreservices/aedesclist)
- [AEEventSource](/documentation/coreservices/aeeventsource)
- [AEDisposeExternalUPP](/documentation/coreservices/aedisposeexternalupp)
- [AEEventClass](/documentation/coreservices/aeeventclass)
- [AEEventHandlerUPP](/documentation/coreservices/aeeventhandlerupp)
- [AEEventID](/documentation/coreservices/aeeventid)
- [AEKeyword](/documentation/coreservices/aekeyword)
- [AERecord](/documentation/coreservices/aerecord)
- [AERemoteProcessResolverRef](/documentation/coreservices/aeremoteprocessresolverref)
- [AEReturnID](/documentation/coreservices/aereturnid)
- [AESendPriority](/documentation/coreservices/aesendpriority)
- [AEStreamRef](/documentation/coreservices/aestreamref)
- [AETransactionID](/documentation/coreservices/aetransactionid)
- [AppleEvent](/documentation/coreservices/appleevent)
- [DescType](/documentation/coreservices/desctype)
- [OffsetArrayHandle](/documentation/coreservices/offsetarrayhandle)
- [OSLAccessorUPP](/documentation/coreservices/oslaccessorupp)
- [OSLAdjustMarksUPP](/documentation/coreservices/osladjustmarksupp)
- [OSLCompareUPP](/documentation/coreservices/oslcompareupp)
- [OSLCountUPP](/documentation/coreservices/oslcountupp)
- [OSLDisposeTokenUPP](/documentation/coreservices/osldisposetokenupp)
- [OSLGetErrDescUPP](/documentation/coreservices/oslgeterrdescupp)
- [OSLGetMarkTokenUPP](/documentation/coreservices/oslgetmarktokenupp)
- [OSLMarkUPP](/documentation/coreservices/oslmarkupp)

### Constants

- [AEBuildErrorCode](/documentation/coreservices/aebuilderrorcode)
- [AESendMode](/documentation/coreservices/aesendmode)
- [Apple Event Recording Event ID Constants](/documentation/coreservices/apple_events/1527224-apple_event_recording_event_id_c)
- [cAEList](/documentation/applicationservices/apple_event_manager/1556411-caelist)

#### Constants

- [var cAEList: OSType](/documentation/coreservices/caelist)
- [var cApplication: OSType](/documentation/coreservices/capplication)
- [var cArc: OSType](/documentation/coreservices/carc)
- [var cBoolean: OSType](/documentation/coreservices/cboolean)
- [var cCell: OSType](/documentation/coreservices/ccell)
- [var cChar: OSType](/documentation/coreservices/cchar)
- [var cColorTable: OSType](/documentation/coreservices/ccolortable)
- [var cColumn: OSType](/documentation/coreservices/ccolumn)
- [var cDocument: OSType](/documentation/coreservices/cdocument)
- [var cDrawingArea: OSType](/documentation/coreservices/cdrawingarea)
- [var cEnumeration: OSType](/documentation/coreservices/cenumeration)
- [var cFile: OSType](/documentation/coreservices/cfile)
- [var cFixed: OSType](/documentation/coreservices/cfixed)
- [var cFixedPoint: OSType](/documentation/coreservices/cfixedpoint)
- [var cFixedRectangle: OSType](/documentation/coreservices/cfixedrectangle)
- [var cGraphicLine: OSType](/documentation/coreservices/cgraphicline)
- [var cGraphicObject: OSType](/documentation/coreservices/cgraphicobject)
- [var cGraphicShape: OSType](/documentation/coreservices/cgraphicshape)
- [var cGraphicText: OSType](/documentation/coreservices/cgraphictext)
- [var cGroupedGraphic: OSType](/documentation/coreservices/cgroupedgraphic)
- [Callback Constants for the AEResolve Function](/documentation/coreservices/apple_events/1572741-callback_constants_for_the_aeres)
- [cInsertionLoc](/documentation/applicationservices/apple_event_manager/1556389-cinsertionloc)

#### Constants

- [var cInsertionLoc: OSType](/documentation/coreservices/cinsertionloc)
- [var cInsertionPoint: OSType](/documentation/coreservices/cinsertionpoint)
- [var cIntlText: OSType](/documentation/coreservices/cintltext)
- [var cIntlWritingCode: OSType](/documentation/coreservices/cintlwritingcode)
- [var cItem: OSType](/documentation/coreservices/citem)
- [var cLine: OSType](/documentation/coreservices/cline)
- [var cLongDateTime: OSType](/documentation/coreservices/clongdatetime)
- [var cLongFixed: OSType](/documentation/coreservices/clongfixed)
- [var cLongFixedPoint: OSType](/documentation/coreservices/clongfixedpoint)
- [var cLongFixedRectangle: OSType](/documentation/coreservices/clongfixedrectangle)
- [var cLongInteger: OSType](/documentation/coreservices/clonginteger)
- [var cLongPoint: OSType](/documentation/coreservices/clongpoint)
- [var cLongRectangle: OSType](/documentation/coreservices/clongrectangle)
- [var cMachineLoc: OSType](/documentation/coreservices/cmachineloc)
- [var cMenu: OSType](/documentation/coreservices/cmenu)
- [var cMenuItem: OSType](/documentation/coreservices/cmenuitem)
- [var cObject: OSType](/documentation/coreservices/cobject)
- [var cObjectSpecifier: OSType](/documentation/coreservices/cobjectspecifier)
- [var cOpenableObject: OSType](/documentation/coreservices/copenableobject)
- [var cOval: OSType](/documentation/coreservices/coval)
- [cKeystroke](/documentation/applicationservices/apple_event_manager/1556385-ckeystroke)

#### Constants

- [var cKeystroke: OSType](/documentation/coreservices/ckeystroke)
- [var eCapsLockDown: OSType](/documentation/coreservices/ecapslockdown)
- [var eClearKey: OSType](/documentation/coreservices/eclearkey)
- [var eCommandDown: OSType](/documentation/coreservices/ecommanddown)
- [var eControlDown: OSType](/documentation/coreservices/econtroldown)
- [var eDeleteKey: OSType](/documentation/coreservices/edeletekey)
- [var eDownArrowKey: OSType](/documentation/coreservices/edownarrowkey)
- [var eEndKey: OSType](/documentation/coreservices/eendkey)
- [var eEnterKey: OSType](/documentation/coreservices/eenterkey)
- [var eEscapeKey: OSType](/documentation/coreservices/eescapekey)
- [var eF10Key: OSType](/documentation/coreservices/ef10key)
- [var eF11Key: OSType](/documentation/coreservices/ef11key)
- [var eF12Key: OSType](/documentation/coreservices/ef12key)
- [var eF13Key: OSType](/documentation/coreservices/ef13key)
- [var eF14Key: OSType](/documentation/coreservices/ef14key)
- [var eF15Key: OSType](/documentation/coreservices/ef15key)
- [var eF1Key: OSType](/documentation/coreservices/ef1key)
- [var eF2Key: OSType](/documentation/coreservices/ef2key)
- [var eF3Key: OSType](/documentation/coreservices/ef3key)
- [var eF4Key: OSType](/documentation/coreservices/ef4key)
- [var eF5Key: OSType](/documentation/coreservices/ef5key)
- [var eF6Key: OSType](/documentation/coreservices/ef6key)
- [var eF7Key: OSType](/documentation/coreservices/ef7key)
- [var eF8Key: OSType](/documentation/coreservices/ef8key)
- [var eF9Key: OSType](/documentation/coreservices/ef9key)
- [var eForwardDelKey: OSType](/documentation/coreservices/eforwarddelkey)
- [var eHelpKey: OSType](/documentation/coreservices/ehelpkey)
- [var eHomeKey: OSType](/documentation/coreservices/ehomekey)
- [var eKeyKind: OSType](/documentation/coreservices/ekeykind)
- [var eLeftArrowKey: OSType](/documentation/coreservices/eleftarrowkey)
- [var eModifiers: OSType](/documentation/coreservices/emodifiers)
- [var eOptionDown: OSType](/documentation/coreservices/eoptiondown)
- [var ePageDownKey: OSType](/documentation/coreservices/epagedownkey)
- [var ePageUpKey: OSType](/documentation/coreservices/epageupkey)
- [var eReturnKey: OSType](/documentation/coreservices/ereturnkey)
- [var eRightArrowKey: OSType](/documentation/coreservices/erightarrowkey)
- [var eShiftDown: OSType](/documentation/coreservices/eshiftdown)
- [var eTabKey: OSType](/documentation/coreservices/etabkey)
- [var eUpArrowKey: OSType](/documentation/coreservices/euparrowkey)
- [var pKeyKind: OSType](/documentation/coreservices/pkeykind)
- [var pKeystrokeKey: OSType](/documentation/coreservices/pkeystrokekey)
- [var pModifiers: OSType](/documentation/coreservices/pmodifiers)
- [Comparison Operator Constants](/documentation/applicationservices/apple_event_manager/comparison_operator_constants)

#### Constants

- [var kAEBeginsWith: OSType](/documentation/coreservices/kaebeginswith)
- [var kAEContains: OSType](/documentation/coreservices/kaecontains)
- [var kAECoreSuite: OSType](/documentation/coreservices/kaecoresuite)
- [Constants for Object Specifiers, Positions, and Logical and Comparison Operations](/documentation/coreservices/apple_events/1572744-constants_for_object_specifiers_)
- [cURL](/documentation/applicationservices/apple_event_manager/1556375-curl)

#### Constants

- [var cURL: OSType](/documentation/coreservices/curl)
- [var cInternetAddress: OSType](/documentation/coreservices/cinternetaddress)
- [var cHTML: OSType](/documentation/coreservices/chtml)
- [var cFTPItem: OSType](/documentation/coreservices/cftpitem)
- [cVersion](/documentation/applicationservices/apple_event_manager/cversion)

#### Constants

- [var formUniqueID: Int](/documentation/coreservices/formuniqueid)
- [Data Array Constants](/documentation/coreservices/apple_events/1542848-data_array_constants)
- [Descriptor Type Constants](/documentation/coreservices/apple_events/1542788-descriptor_type_constants)
- [eScheme](/documentation/applicationservices/apple_event_manager/1556397-escheme)

#### Constants

- [var eScheme: OSType](/documentation/coreservices/escheme)
- [var eurlAFP: OSType](/documentation/coreservices/eurlafp)
- [var eurlAT: OSType](/documentation/coreservices/eurlat)
- [var eurlEPPC: OSType](/documentation/coreservices/eurleppc)
- [var eurlFTP: OSType](/documentation/coreservices/eurlftp)
- [var eurlFile: OSType](/documentation/coreservices/eurlfile)
- [var eurlGopher: OSType](/documentation/coreservices/eurlgopher)
- [var eurlHTTP: OSType](/documentation/coreservices/eurlhttp)
- [var eurlHTTPS: OSType](/documentation/coreservices/eurlhttps)
- [var eurlIMAP: OSType](/documentation/coreservices/eurlimap)
- [var eurlLDAP: OSType](/documentation/coreservices/eurlldap)
- [var eurlLaunch: OSType](/documentation/coreservices/eurllaunch)
- [var eurlMail: OSType](/documentation/coreservices/eurlmail)
- [var eurlMailbox: OSType](/documentation/coreservices/eurlmailbox)
- [var eurlMessage: OSType](/documentation/coreservices/eurlmessage)
- [var eurlMulti: OSType](/documentation/coreservices/eurlmulti)
- [var eurlNFS: OSType](/documentation/coreservices/eurlnfs)
- [var eurlNNTP: OSType](/documentation/coreservices/eurlnntp)
- [var eurlNews: OSType](/documentation/coreservices/eurlnews)
- [var eurlPOP: OSType](/documentation/coreservices/eurlpop)
- [var eurlRTSP: OSType](/documentation/coreservices/eurlrtsp)
- [var eurlSNews: OSType](/documentation/coreservices/eurlsnews)
- [var eurlTelnet: OSType](/documentation/coreservices/eurltelnet)
- [var eurlUnknown: OSType](/documentation/coreservices/eurlunknown)
- [Event Class Constants](/documentation/coreservices/apple_events/1527210-event_class_constants)
- [Event ID Constants](/documentation/coreservices/apple_events/1527223-event_id_constants)
- [Event Source Constants](/documentation/coreservices/apple_events/1527201-event_source_constants)
- [Factoring Constants](/documentation/coreservices/apple_events/1542928-factoring_constants)
- [ID Constants for the AECreateAppleEvent Function](/documentation/coreservices/apple_events/1542799-id_constants_for_the_aecreateapp)
- [Key Form and Descriptor Type Object Specifier Constants](/documentation/coreservices/apple_events/1572731-key_form_and_descriptor_type_obj)
- [Keyword Attribute Constants](/documentation/coreservices/apple_events/1542920-keyword_attribute_constants)
- [Keyword Parameter Constants](/documentation/coreservices/apple_events/1527206-keyword_parameter_constants)
- [Launch Apple Event Constants](/documentation/coreservices/apple_events/1556410-launch_apple_event_constants)
- [Numeric Descriptor Type Constants](/documentation/coreservices/apple_events/1542872-numeric_descriptor_type_constant)
- [Object Class ID Constants](/documentation/coreservices/apple_events/1556368-object_class_id_constants)
- [Other Descriptor Type Constants](/documentation/coreservices/apple_events/1542760-other_descriptor_type_constants)
- [Priority Constants for the AESend Function (Deprecated in macOS)](/documentation/coreservices/apple_events/1542840-priority_constants_for_the_aesen)
- [Remote Process Dictionary Keys](/documentation/applicationservices/apple_event_manager/remote_process_dictionary_keys)

#### Constants

- [let kAERemoteProcessURLKey: CFString!](/documentation/coreservices/kaeremoteprocessurlkey)
- [let kAERemoteProcessNameKey: CFString!](/documentation/coreservices/kaeremoteprocessnamekey)
- [let kAERemoteProcessUserIDKey: CFString!](/documentation/coreservices/kaeremoteprocessuseridkey)
- [let kAERemoteProcessProcessIDKey: CFString!](/documentation/coreservices/kaeremoteprocessprocessidkey)
- [Special Handler Callback Constants](/documentation/coreservices/apple_events/1572726-special_handler_callback_constan)
- [Timeout Constants](/documentation/coreservices/apple_events/1542814-timeout_constants)
- [Whose Test Constants](/documentation/applicationservices/apple_event_manager/whose_test_constants)

#### Constants

- [var formWhose: Int](/documentation/coreservices/formwhose)
- [kAEDoObjectsExist](/documentation/applicationservices/apple_event_manager/kaedoobjectsexist)

#### Constants

- [var kAEEndsWith: OSType](/documentation/coreservices/kaeendswith)
- [var kAEEquals: OSType](/documentation/coreservices/kaeequals)
- [var kAEFinderEvents: OSType](/documentation/coreservices/kaefinderevents)
- [kAEDebugPOSTHeader](/documentation/coreservices/apple_events/1542854-kaedebugpostheader)
- [kAEGetPrivilegeSelection](/documentation/applicationservices/apple_event_manager/kaegetprivilegeselection)

#### Constants

- [var kAEGreaterThan: OSType](/documentation/coreservices/kaegreaterthan)
- [var kAEGreaterThanEquals: OSType](/documentation/coreservices/kaegreaterthanequals)
- [var kAELessThanEquals: OSType](/documentation/coreservices/kaelessthanequals)
- [kAEHandleArray](/documentation/coreservices/apple_events/1542886-kaehandlearray)
- [kAEInfo](/documentation/coreservices/apple_events/1556393-kaeinfo)
- [kAEInternetSuite](/documentation/coreservices/apple_events/1556388-kaeinternetsuite)
- [kAEISGetURL](/documentation/coreservices/apple_events/1556362-kaeisgeturl)
- [kAEISHTTPSearchArgs](/documentation/coreservices/apple_events/1556404-kaeishttpsearchargs)
- [kAELogOut](/documentation/coreservices/apple_events/1556395-kaelogout)
- [kAEMenuClass](/documentation/coreservices/apple_events/1556392-kaemenuclass)
- [kAEMouseClass](/documentation/coreservices/apple_events/1556409-kaemouseclass)
- [kAENonmodifiable](/documentation/coreservices/apple_events/1556386-kaenonmodifiable)
- [kAEQDNotOr](/documentation/coreservices/apple_events/1556377-kaeqdnotor)
- [kAESetPosition](/documentation/coreservices/apple_events/1556407-kaesetposition)
- [kAESocks4Protocol](/documentation/coreservices/apple_events/1542847-kaesocks4protocol)
- [kAEUseHTTPProxyAttr](/documentation/coreservices/apple_events/1542824-kaeusehttpproxyattr)
- [kAEUserTerminology](/documentation/coreservices/apple_events/1457902-kaeuserterminology)
- [kAEUseSocksAttr](/documentation/coreservices/apple_events/1542933-kaeusesocksattr)
- [kAEUTHasReturningParam](/documentation/coreservices/apple_events/1457911-kaeuthasreturningparam)
- [kAEZoomIn](/documentation/coreservices/apple_events/1556365-kaezoomin)
- [kBySmallIcon](/documentation/applicationservices/apple_event_manager/1556391-kbysmallicon)

#### Constants

- [var kByCommentView: Int](/documentation/coreservices/kbycommentview)
- [var kByDateView: Int](/documentation/coreservices/kbydateview)
- [var kByIconView: Int](/documentation/coreservices/kbyiconview)
- [var kByKindView: Int](/documentation/coreservices/kbykindview)
- [var kByLabelView: Int](/documentation/coreservices/kbylabelview)
- [var kByNameView: Int](/documentation/coreservices/kbynameview)
- [var kBySizeView: Int](/documentation/coreservices/kbysizeview)
- [var kBySmallIcon: Int](/documentation/coreservices/kbysmallicon)
- [var kByVersionView: Int](/documentation/coreservices/kbyversionview)
- [kConnSuite](/documentation/applicationservices/apple_event_manager/1556369-kconnsuite)

#### Constants

- [var cADBAddress: OSType](/documentation/coreservices/cadbaddress)
- [var cAddressSpec: OSType](/documentation/coreservices/caddressspec)
- [var cAppleTalkAddress: OSType](/documentation/coreservices/cappletalkaddress)
- [var cBusAddress: OSType](/documentation/coreservices/cbusaddress)
- [var cDevSpec: OSType](/documentation/coreservices/cdevspec)
- [var cEthernetAddress: OSType](/documentation/coreservices/cethernetaddress)
- [var cFireWireAddress: OSType](/documentation/coreservices/cfirewireaddress)
- [var cIPAddress: OSType](/documentation/coreservices/cipaddress)
- [var cLocalTalkAddress: OSType](/documentation/coreservices/clocaltalkaddress)
- [var cSCSIAddress: OSType](/documentation/coreservices/cscsiaddress)
- [var cTokenRingAddress: OSType](/documentation/coreservices/ctokenringaddress)
- [var cUSBAddress: OSType](/documentation/coreservices/cusbaddress)
- [var eADB: OSType](/documentation/coreservices/eadb)
- [var eAddressSpec: OSType](/documentation/coreservices/eaddressspec)
- [var eAnalogAudio: OSType](/documentation/coreservices/eanalogaudio)
- [var eAppleTalk: OSType](/documentation/coreservices/eappletalk)
- [var eAudioLineIn: OSType](/documentation/coreservices/eaudiolinein)
- [var eAudioLineOut: OSType](/documentation/coreservices/eaudiolineout)
- [var eAudioOut: OSType](/documentation/coreservices/eaudioout)
- [var eBus: OSType](/documentation/coreservices/ebus)
- [var eCDROM: OSType](/documentation/coreservices/ecdrom)
- [var eCommSlot: OSType](/documentation/coreservices/ecommslot)
- [var eConduit: OSType](/documentation/coreservices/econduit)
- [var eDVD: OSType](/documentation/coreservices/edvd)
- [var eDeviceType: OSType](/documentation/coreservices/edevicetype)
- [var eDigitalAudio: OSType](/documentation/coreservices/edigitalaudio)
- [var eDisplay: OSType](/documentation/coreservices/edisplay)
- [var eEthernet: OSType](/documentation/coreservices/eethernet)
- [var eFireWire: OSType](/documentation/coreservices/efirewire)
- [var eFloppy: OSType](/documentation/coreservices/efloppy)
- [var eHD: OSType](/documentation/coreservices/ehd)
- [var eIP: OSType](/documentation/coreservices/eip)
- [var eIRTalk: OSType](/documentation/coreservices/eirtalk)
- [var eInfrared: OSType](/documentation/coreservices/einfrared)
- [var eIrDA: OSType](/documentation/coreservices/eirda)
- [var eKeyboard: OSType](/documentation/coreservices/ekeyboard)
- [var eLCD: OSType](/documentation/coreservices/elcd)
- [var eLocalTalk: OSType](/documentation/coreservices/elocaltalk)
- [var eMacIP: OSType](/documentation/coreservices/emacip)
- [var eMacVideo: OSType](/documentation/coreservices/emacvideo)
- [var eMicrophone: OSType](/documentation/coreservices/emicrophone)
- [var eModem: OSType](/documentation/coreservices/emodem)
- [var eModemPort: OSType](/documentation/coreservices/emodemport)
- [var eModemPrinterPort: OSType](/documentation/coreservices/emodemprinterport)
- [var eMonitorOut: OSType](/documentation/coreservices/emonitorout)
- [var eMouse: OSType](/documentation/coreservices/emouse)
- [var eNuBus: OSType](/documentation/coreservices/enubus)
- [var eNuBusCard: OSType](/documentation/coreservices/enubuscard)
- [var ePCIbus: OSType](/documentation/coreservices/epcibus)
- [var ePCIcard: OSType](/documentation/coreservices/epcicard)
- [var ePCcard: OSType](/documentation/coreservices/epccard)
- [var ePDScard: OSType](/documentation/coreservices/epdscard)
- [var ePDSslot: OSType](/documentation/coreservices/epdsslot)
- [var ePPP: OSType](/documentation/coreservices/eppp)
- [var ePointingDevice: OSType](/documentation/coreservices/epointingdevice)
- [var ePostScript: OSType](/documentation/coreservices/epostscript)
- [var ePrinter: OSType](/documentation/coreservices/eprinter)
- [var ePrinterPort: OSType](/documentation/coreservices/eprinterport)
- [var eProtocol: OSType](/documentation/coreservices/eprotocol)
- [var eSCSI: OSType](/documentation/coreservices/escsi)
- [var eSVGA: OSType](/documentation/coreservices/esvga)
- [var eSerial: OSType](/documentation/coreservices/eserial)
- [var eSpeakers: OSType](/documentation/coreservices/espeakers)
- [var eStorageDevice: OSType](/documentation/coreservices/estoragedevice)
- [var eSvideo: OSType](/documentation/coreservices/esvideo)
- [var eTokenRing: OSType](/documentation/coreservices/etokenring)
- [var eTrackball: OSType](/documentation/coreservices/etrackball)
- [var eTrackpad: OSType](/documentation/coreservices/etrackpad)
- [var eUSB: OSType](/documentation/coreservices/eusb)
- [var eVideoIn: OSType](/documentation/coreservices/evideoin)
- [var eVideoMonitor: OSType](/documentation/coreservices/evideomonitor)
- [var eVideoOut: OSType](/documentation/coreservices/evideoout)
- [var kConnSuite: OSType](/documentation/coreservices/kconnsuite)
- [var pATMachine: OSType](/documentation/coreservices/patmachine)
- [var pATType: OSType](/documentation/coreservices/pattype)
- [var pATZone: OSType](/documentation/coreservices/patzone)
- [var pConduit: OSType](/documentation/coreservices/pconduit)
- [var pDNS: OSType](/documentation/coreservices/pdns)
- [var pDeviceAddress: OSType](/documentation/coreservices/pdeviceaddress)
- [var pDeviceType: OSType](/documentation/coreservices/pdevicetype)
- [var pDottedDecimal: OSType](/documentation/coreservices/pdotteddecimal)
- [var pNetwork: OSType](/documentation/coreservices/pnetwork)
- [var pNode: OSType](/documentation/coreservices/pnode)
- [var pPort: OSType](/documentation/coreservices/pport)
- [var pProtocol: OSType](/documentation/coreservices/pprotocol)
- [var pSCSIBus: OSType](/documentation/coreservices/pscsibus)
- [var pSCSILUN: OSType](/documentation/coreservices/pscsilun)
- [var pSocket: OSType](/documentation/coreservices/psocket)
- [keyAEAngle](/documentation/coreservices/apple_events/1556380-keyaeangle)
- [keyAEBaseAddr](/documentation/coreservices/apple_events/1556383-keyaebaseaddr)
- [keyAEDoScale](/documentation/coreservices/apple_events/1556387-keyaedoscale)
- [keyAEHiliteRange](/documentation/coreservices/apple_events/1556379-keyaehiliterange)
- [keyAEKeyword](/documentation/coreservices/apple_events/1556374-keyaekeyword)
- [keyAEPropData](/documentation/applicationservices/apple_event_manager/keyaepropdata)

#### Constants

- [var keyAESearchText: AEKeyword](/documentation/coreservices/keyaesearchtext)
- [keyAESuiteID](/documentation/coreservices/apple_events/1556370-keyaesuiteid)
- [keyMenuID](/documentation/coreservices/apple_events/1556381-keymenuid)
- [keyMiscellaneous](/documentation/coreservices/apple_events/1556399-keymiscellaneous)
- [keyReplyPortAttr](/documentation/coreservices/apple_events/1571648-keyreplyportattr)
- [keySOAPStructureMetaData](/documentation/coreservices/apple_events/1542797-keysoapstructuremetadata)
- [keyUserNameAttr](/documentation/coreservices/apple_events/1542780-keyusernameattr)
- [kFAServerApp](/documentation/applicationservices/apple_event_manager/1556384-kfaserverapp)

#### Constants

- [var kDoFolderActionEvent: OSType](/documentation/coreservices/kdofolderactionevent)
- [var kFAAttachCommand: OSType](/documentation/coreservices/kfaattachcommand)
- [var kFAEditCommand: OSType](/documentation/coreservices/kfaeditcommand)
- [var kFAFileParam: OSType](/documentation/coreservices/kfafileparam)
- [var kFAIndexParam: OSType](/documentation/coreservices/kfaindexparam)
- [var kFARemoveCommand: OSType](/documentation/coreservices/kfaremovecommand)
- [var kFAServerApp: OSType](/documentation/coreservices/kfaserverapp)
- [var kFASuiteCode: OSType](/documentation/coreservices/kfasuitecode)
- [var kFolderActionCode: OSType](/documentation/coreservices/kfolderactioncode)
- [var kFolderClosedEvent: OSType](/documentation/coreservices/kfolderclosedevent)
- [var kFolderItemsAddedEvent: OSType](/documentation/coreservices/kfolderitemsaddedevent)
- [var kFolderItemsRemovedEvent: OSType](/documentation/coreservices/kfolderitemsremovedevent)
- [var kFolderOpenedEvent: OSType](/documentation/coreservices/kfolderopenedevent)
- [var kFolderWindowMovedEvent: OSType](/documentation/coreservices/kfolderwindowmovedevent)
- [var kItemList: OSType](/documentation/coreservices/kitemlist)
- [var kNewSizeParameter: OSType](/documentation/coreservices/knewsizeparameter)
- [kLaunchToGetTerminology](/documentation/applicationservices/apple_event_manager/1457909-klaunchtogetterminology)

#### Constants

- [var kAlwaysSendSubject: Int](/documentation/coreservices/kalwayssendsubject)
- [var kDontFindAppBySignature: Int](/documentation/coreservices/kdontfindappbysignature)
- [var kLaunchToGetTerminology: Int](/documentation/coreservices/klaunchtogetterminology)
- [kNextBody](/documentation/applicationservices/apple_event_manager/1556402-knextbody)

#### Constants

- [var kNextBody: Int](/documentation/coreservices/knextbody)
- [var kPreviousBody: Int](/documentation/coreservices/kpreviousbody)
- [kOSIZDontOpenResourceFile](/documentation/applicationservices/apple_event_manager/1457903-kosizdontopenresourcefile)

#### Constants

- [var kOSIZCodeInSharedLibraries: Int](/documentation/coreservices/kosizcodeinsharedlibraries)
- [var kOSIZDontOpenResourceFile: Int](/documentation/coreservices/kosizdontopenresourcefile)
- [var kOSIZOpenWithReadPermission: Int](/documentation/coreservices/kosizopenwithreadpermission)
- [var kOSIZdontAcceptRemoteEvents: Int](/documentation/coreservices/kosizdontacceptremoteevents)
- [kReadExtensionTermsMask](/documentation/applicationservices/apple_event_manager/1457896-kreadextensiontermsmask)

#### Constants

- [var kReadExtensionTermsMask: Int](/documentation/coreservices/kreadextensiontermsmask)
- [kSOAP1999Schema](/documentation/applicationservices/apple_event_manager/1542943-ksoap1999schema)

#### Constants

- [var kSOAP1999Schema: Int](/documentation/coreservices/ksoap1999schema)
- [var kSOAP2001Schema: Int](/documentation/coreservices/ksoap2001schema)
- [kTextServiceClass](/documentation/applicationservices/apple_event_manager/1556406-ktextserviceclass)

#### Constants

- [var kGetSelectedText: OSType](/documentation/coreservices/kgetselectedtext)
- [var kOffset2Pos: OSType](/documentation/coreservices/koffset2pos)
- [var kPos2Offset: OSType](/documentation/coreservices/kpos2offset)
- [var kShowHideInputWindow: OSType](/documentation/coreservices/kshowhideinputwindow)
- [var kTextServiceClass: OSType](/documentation/coreservices/ktextserviceclass)
- [var kUnicodeNotFromInputMethod: OSType](/documentation/coreservices/kunicodenotfrominputmethod)
- [var kUpdateActiveInputArea: OSType](/documentation/coreservices/kupdateactiveinputarea)
- [var keyAEBufferSize: OSType](/documentation/coreservices/keyaebuffersize)
- [var keyAECurrentPoint: OSType](/documentation/coreservices/keyaecurrentpoint)
- [var keyAEFixLength: OSType](/documentation/coreservices/keyaefixlength)
- [var keyAEMoveView: OSType](/documentation/coreservices/keyaemoveview)
- [var keyAENextBody: OSType](/documentation/coreservices/keyaenextbody)
- [var keyAEServerInstance: OSType](/documentation/coreservices/keyaeserverinstance)
- [var keyAETSMDocumentRefcon: OSType](/documentation/coreservices/keyaetsmdocumentrefcon)
- [var keyAETSMEventRecord: OSType](/documentation/coreservices/keyaetsmeventrecord)
- [var keyAETSMEventRef: OSType](/documentation/coreservices/keyaetsmeventref)
- [var keyAETSMGlyphInfoArray: OSType](/documentation/coreservices/keyaetsmglyphinfoarray)
- [var keyAETSMScriptTag: OSType](/documentation/coreservices/keyaetsmscripttag)
- [var keyAETSMTextFMFont: OSType](/documentation/coreservices/keyaetsmtextfmfont)
- [var keyAETSMTextFont: OSType](/documentation/coreservices/keyaetsmtextfont)
- [var keyAETSMTextPointSize: OSType](/documentation/coreservices/keyaetsmtextpointsize)
- [var keyAETextServiceEncoding: OSType](/documentation/coreservices/keyaetextserviceencoding)
- [var keyAETextServiceMacEncoding: OSType](/documentation/coreservices/keyaetextservicemacencoding)
- [var keyAETheData: OSType](/documentation/coreservices/keyaethedata)
- [var keyAEUpdateRange: OSType](/documentation/coreservices/keyaeupdaterange)
- [var typeComponentInstance: OSType](/documentation/coreservices/typecomponentinstance)
- [var typeEventRef: OSType](/documentation/coreservices/typeeventref)
- [var typeGlyphInfoArray: OSType](/documentation/coreservices/typeglyphinfoarray)
- [var typeLowLevelEventRecord: OSType](/documentation/coreservices/typelowleveleventrecord)
- [var typeOffsetArray: OSType](/documentation/coreservices/typeoffsetarray)
- [var typeText: OSType](/documentation/coreservices/typetext)
- [var typeTextRange: OSType](/documentation/coreservices/typetextrange)
- [var typeTextRangeArray: OSType](/documentation/coreservices/typetextrangearray)
- [kTSMHiliteCaretPosition](/documentation/applicationservices/apple_event_manager/1556398-ktsmhilitecaretposition)

#### Constants

- [var kTSMHiliteCaretPosition: Int](/documentation/coreservices/ktsmhilitecaretposition)
- [var kTSMHiliteRawText: Int](/documentation/coreservices/ktsmhiliterawtext)
- [var kTSMHiliteSelectedRawText: Int](/documentation/coreservices/ktsmhiliteselectedrawtext)
- [var kTSMHiliteConvertedText: Int](/documentation/coreservices/ktsmhiliteconvertedtext)
- [var kTSMHiliteSelectedConvertedText: Int](/documentation/coreservices/ktsmhiliteselectedconvertedtext)
- [var kTSMHiliteBlockFillText: Int](/documentation/coreservices/ktsmhiliteblockfilltext)
- [var kTSMHiliteOutlineText: Int](/documentation/coreservices/ktsmhiliteoutlinetext)
- [var kTSMHiliteSelectedText: Int](/documentation/coreservices/ktsmhiliteselectedtext)
- [var kTSMHiliteNoHilite: Int](/documentation/coreservices/ktsmhilitenohilite)
- [kTSMOutsideOfBody](/documentation/applicationservices/apple_event_manager/1556371-ktsmoutsideofbody)

#### Constants

- [var kTSMInsideOfActiveInputArea: Int](/documentation/coreservices/ktsminsideofactiveinputarea)
- [var kTSMInsideOfBody: Int](/documentation/coreservices/ktsminsideofbody)
- [var kTSMOutsideOfBody: Int](/documentation/coreservices/ktsmoutsideofbody)
- [pArcAngle](/documentation/applicationservices/apple_event_manager/1556376-parcangle)

#### Constants

- [var pArcAngle: OSType](/documentation/coreservices/parcangle)
- [var pBackgroundColor: OSType](/documentation/coreservices/pbackgroundcolor)
- [var pBackgroundPattern: OSType](/documentation/coreservices/pbackgroundpattern)
- [var pBestType: OSType](/documentation/coreservices/pbesttype)
- [var pBounds: OSType](/documentation/coreservices/pbounds)
- [var pClass: OSType](/documentation/coreservices/pclass)
- [var pClipboard: OSType](/documentation/coreservices/pclipboard)
- [var pColor: OSType](/documentation/coreservices/pcolor)
- [var pColorTable: OSType](/documentation/coreservices/pcolortable)
- [var pContents: OSType](/documentation/coreservices/pcontents)
- [var pCornerCurveHeight: OSType](/documentation/coreservices/pcornercurveheight)
- [var pCornerCurveWidth: OSType](/documentation/coreservices/pcornercurvewidth)
- [var pDashStyle: OSType](/documentation/coreservices/pdashstyle)
- [var pDefaultType: OSType](/documentation/coreservices/pdefaulttype)
- [var pDefinitionRect: OSType](/documentation/coreservices/pdefinitionrect)
- [var pEnabled: OSType](/documentation/coreservices/penabled)
- [var pEndPoint: OSType](/documentation/coreservices/pendpoint)
- [var pFillColor: OSType](/documentation/coreservices/pfillcolor)
- [var pFillPattern: OSType](/documentation/coreservices/pfillpattern)
- [var pFont: OSType](/documentation/coreservices/pfont)
- [pFormula](/documentation/applicationservices/apple_event_manager/1556373-pformula)

#### Constants

- [var pFormula: OSType](/documentation/coreservices/pformula)
- [var pGraphicObjects: OSType](/documentation/coreservices/pgraphicobjects)
- [var pHasCloseBox: OSType](/documentation/coreservices/phasclosebox)
- [var pHasTitleBar: OSType](/documentation/coreservices/phastitlebar)
- [var pID: OSType](/documentation/coreservices/pid)
- [var pIndex: OSType](/documentation/coreservices/pindex)
- [var pInsertionLoc: OSType](/documentation/coreservices/pinsertionloc)
- [var pIsFloating: OSType](/documentation/coreservices/pisfloating)
- [var pIsFrontProcess: OSType](/documentation/coreservices/pisfrontprocess)
- [var pIsModal: OSType](/documentation/coreservices/pismodal)
- [var pIsModified: OSType](/documentation/coreservices/pismodified)
- [var pIsResizable: OSType](/documentation/coreservices/pisresizable)
- [var pIsStationeryPad: OSType](/documentation/coreservices/pisstationerypad)
- [var pIsZoomable: OSType](/documentation/coreservices/piszoomable)
- [var pIsZoomed: OSType](/documentation/coreservices/piszoomed)
- [var pItemNumber: OSType](/documentation/coreservices/pitemnumber)
- [var pJustification: OSType](/documentation/coreservices/pjustification)
- [var pLineArrow: OSType](/documentation/coreservices/plinearrow)
- [var pMenuID: OSType](/documentation/coreservices/pmenuid)
- [var pName: OSType](/documentation/coreservices/pname)
- [pNewElementLoc](/documentation/applicationservices/apple_event_manager/1556400-pnewelementloc)

#### Constants

- [var pNewElementLoc: OSType](/documentation/coreservices/pnewelementloc)
- [var pPenColor: OSType](/documentation/coreservices/ppencolor)
- [var pPenPattern: OSType](/documentation/coreservices/ppenpattern)
- [var pPenWidth: OSType](/documentation/coreservices/ppenwidth)
- [var pPixelDepth: OSType](/documentation/coreservices/ppixeldepth)
- [var pPointList: OSType](/documentation/coreservices/ppointlist)
- [var pPointSize: OSType](/documentation/coreservices/ppointsize)
- [var pProtection: OSType](/documentation/coreservices/pprotection)
- [var pRotation: OSType](/documentation/coreservices/protation)
- [var pScale: OSType](/documentation/coreservices/pscale)
- [var pScript: OSType](/documentation/coreservices/pscript)
- [var pScriptTag: OSType](/documentation/coreservices/pscripttag)
- [var pSelected: OSType](/documentation/coreservices/pselected)
- [var pSelection: OSType](/documentation/coreservices/pselection)
- [var pStartAngle: OSType](/documentation/coreservices/pstartangle)
- [var pStartPoint: OSType](/documentation/coreservices/pstartpoint)
- [var pTextColor: OSType](/documentation/coreservices/ptextcolor)
- [var pTextFont: OSType](/documentation/coreservices/ptextfont)
- [var pTextItemDelimiters: OSType](/documentation/coreservices/ptextitemdelimiters)
- [var pTextPointSize: OSType](/documentation/coreservices/ptextpointsize)
- [pScheme](/documentation/applicationservices/apple_event_manager/1556408-pscheme)

#### Constants

- [var pDNSForm: OSType](/documentation/coreservices/pdnsform)
- [var pFTPKind: OSType](/documentation/coreservices/pftpkind)
- [var pHost: OSType](/documentation/coreservices/phost)
- [var pPath: OSType](/documentation/coreservices/ppath)
- [var pScheme: OSType](/documentation/coreservices/pscheme)
- [var pTextEncoding: OSType](/documentation/coreservices/ptextencoding)
- [var pURL: OSType](/documentation/coreservices/purl)
- [var pUserName: OSType](/documentation/coreservices/pusername)
- [var pUserPassword: OSType](/documentation/coreservices/puserpassword)
- [pTextStyles](/documentation/applicationservices/apple_event_manager/1556367-ptextstyles)

#### Constants

- [var pTextStyles: OSType](/documentation/coreservices/ptextstyles)
- [var pTransferMode: OSType](/documentation/coreservices/ptransfermode)
- [var pTranslation: OSType](/documentation/coreservices/ptranslation)
- [var pUniformStyles: OSType](/documentation/coreservices/puniformstyles)
- [var pUpdateOn: OSType](/documentation/coreservices/pupdateon)
- [var pUserSelection: OSType](/documentation/coreservices/puserselection)
- [var pVersion: OSType](/documentation/coreservices/pversion)
- [var pVisible: OSType](/documentation/coreservices/pvisible)
- [typeAEText](/documentation/applicationservices/apple_event_manager/1556366-typeaetext)

#### Constants

- [var typeAEText: DescType](/documentation/coreservices/typeaetext)
- [var typeArc: DescType](/documentation/coreservices/typearc)
- [var typeBest: DescType](/documentation/coreservices/typebest)
- [var typeCell: DescType](/documentation/coreservices/typecell)
- [var typeClassInfo: DescType](/documentation/coreservices/typeclassinfo)
- [var typeColorTable: DescType](/documentation/coreservices/typecolortable)
- [var typeColumn: DescType](/documentation/coreservices/typecolumn)
- [var typeDashStyle: DescType](/documentation/coreservices/typedashstyle)
- [var typeData: DescType](/documentation/coreservices/typedata)
- [var typeDrawingArea: DescType](/documentation/coreservices/typedrawingarea)
- [var typeEPS: DescType](/documentation/coreservices/typeeps)
- [var typeElemInfo: DescType](/documentation/coreservices/typeeleminfo)
- [var typeEnumeration: DescType](/documentation/coreservices/typeenumeration)
- [var typeEventInfo: DescType](/documentation/coreservices/typeeventinfo)
- [typeApplicationBundleID](/documentation/applicationservices/apple_event_manager/1542896-typeapplicationbundleid)

#### Constants

- [var typeApplicationBundleID: DescType](/documentation/coreservices/typeapplicationbundleid)
- [typeFinderWindow](/documentation/applicationservices/apple_event_manager/typefinderwindow)

#### Constants

- [var typeIntlText: DescType](/documentation/coreservices/typeintltext)
- [typeHIMenu](/documentation/applicationservices/apple_event_manager/1556372-typehimenu)

#### Constants

- [var typeHIMenu: DescType](/documentation/coreservices/typehimenu)
- [var typeHIWindow: DescType](/documentation/coreservices/typehiwindow)
- [typeKernelProcessID](/documentation/applicationservices/apple_event_manager/1542936-typekernelprocessid)

#### Constants

- [var typeKernelProcessID: DescType](/documentation/coreservices/typekernelprocessid)
- [var typeMachPort: DescType](/documentation/coreservices/typemachport)
- [typeMachPort](/documentation/applicationservices/apple_event_manager/typemachport)

#### Constants

- [var typeMachPort: DescType](/documentation/coreservices/typemachport)
- [typeMeters](/documentation/applicationservices/apple_event_manager/1556382-typemeters)

#### Constants

- [var typeCentimeters: DescType](/documentation/coreservices/typecentimeters)
- [var typeCubicCentimeter: DescType](/documentation/coreservices/typecubiccentimeter)
- [var typeCubicFeet: DescType](/documentation/coreservices/typecubicfeet)
- [var typeCubicInches: DescType](/documentation/coreservices/typecubicinches)
- [var typeCubicMeters: DescType](/documentation/coreservices/typecubicmeters)
- [var typeCubicYards: DescType](/documentation/coreservices/typecubicyards)
- [var typeDegreesC: DescType](/documentation/coreservices/typedegreesc)
- [var typeDegreesF: DescType](/documentation/coreservices/typedegreesf)
- [var typeDegreesK: DescType](/documentation/coreservices/typedegreesk)
- [var typeFeet: DescType](/documentation/coreservices/typefeet)
- [var typeGallons: DescType](/documentation/coreservices/typegallons)
- [var typeGrams: DescType](/documentation/coreservices/typegrams)
- [var typeInches: DescType](/documentation/coreservices/typeinches)
- [var typeKilograms: DescType](/documentation/coreservices/typekilograms)
- [var typeKilometers: DescType](/documentation/coreservices/typekilometers)
- [var typeLiters: DescType](/documentation/coreservices/typeliters)
- [var typeMeters: DescType](/documentation/coreservices/typemeters)
- [var typeMiles: DescType](/documentation/coreservices/typemiles)
- [var typeOunces: DescType](/documentation/coreservices/typeounces)
- [var typePounds: DescType](/documentation/coreservices/typepounds)
- [var typeQuarts: DescType](/documentation/coreservices/typequarts)
- [var typeSquareFeet: DescType](/documentation/coreservices/typesquarefeet)
- [var typeSquareKilometers: DescType](/documentation/coreservices/typesquarekilometers)
- [var typeSquareMeters: DescType](/documentation/coreservices/typesquaremeters)
- [var typeSquareMiles: DescType](/documentation/coreservices/typesquaremiles)
- [var typeSquareYards: DescType](/documentation/coreservices/typesquareyards)
- [var typeYards: DescType](/documentation/coreservices/typeyards)
- [typePixelMap](/documentation/applicationservices/apple_event_manager/typepixelmap)

#### Constants

- [var typeStyledText: DescType](/documentation/coreservices/typestyledtext)
- [typeReplyPortAttr](/documentation/applicationservices/apple_event_manager/1571649-typereplyportattr)

#### Constants

- [var typeReplyPortAttr: DescType](/documentation/coreservices/typereplyportattr)
- [typeTIFF](/documentation/applicationservices/apple_event_manager/1556405-typetiff)

#### Constants

- [var typeGIF: DescType](/documentation/coreservices/typegif)
- [var typeJPEG: DescType](/documentation/coreservices/typejpeg)
- [var typeTIFF: DescType](/documentation/coreservices/typetiff)
- [var typeVersion: DescType](/documentation/coreservices/typeversion)
- [typeUnicodeText](/documentation/applicationservices/apple_event_manager/1542918-typeunicodetext)

#### Constants

- [var typeUTF16ExternalRepresentation: DescType](/documentation/coreservices/typeutf16externalrepresentation)
- [var typeUnicodeText: DescType](/documentation/coreservices/typeunicodetext)
- [var typeStyledUnicodeText: DescType](/documentation/coreservices/typestyledunicodetext)
- [var typeUTF8Text: DescType](/documentation/coreservices/typeutf8text)
- [var typeEncodedString: DescType](/documentation/coreservices/typeencodedstring)
- [var typeCString: DescType](/documentation/coreservices/typecstring)
- [var typePString: DescType](/documentation/coreservices/typepstring)

### Result Codes

- [var noPortErr: Int](/documentation/coreservices/noporterr)
- [var destPortErr: Int](/documentation/coreservices/destporterr)
- [var sessClosedErr: Int](/documentation/coreservices/sessclosederr)
- [var errAECoercionFail: Int](/documentation/coreservices/erraecoercionfail)
- [var errAEDescNotFound: Int](/documentation/coreservices/erraedescnotfound)
- [var errAECorruptData: Int](/documentation/coreservices/erraecorruptdata)
- [var errAEWrongDataType: Int](/documentation/coreservices/erraewrongdatatype)
- [var errAENotAEDesc: Int](/documentation/coreservices/erraenotaedesc)
- [var errAEBadListItem: Int](/documentation/coreservices/erraebadlistitem)
- [var errAENewerVersion: Int](/documentation/coreservices/erraenewerversion)
- [var errAENotAppleEvent: Int](/documentation/coreservices/erraenotappleevent)
- [var errAEEventNotHandled: Int](/documentation/coreservices/erraeeventnothandled)
- [var errAEReplyNotValid: Int](/documentation/coreservices/erraereplynotvalid)
- [var errAEUnknownSendMode: Int](/documentation/coreservices/erraeunknownsendmode)
- [var errAEWaitCanceled: Int](/documentation/coreservices/erraewaitcanceled)
- [var errAETimeout: Int](/documentation/coreservices/erraetimeout)
- [var errAENoUserInteraction: Int](/documentation/coreservices/erraenouserinteraction)
- [var errAENotASpecialFunction: Int](/documentation/coreservices/erraenotaspecialfunction)
- [var errAEParamMissed: Int](/documentation/coreservices/erraeparammissed)
- [var errAEUnknownAddressType: Int](/documentation/coreservices/erraeunknownaddresstype)
- [var errAEHandlerNotFound: Int](/documentation/coreservices/erraehandlernotfound)
- [var errAEReplyNotArrived: Int](/documentation/coreservices/erraereplynotarrived)
- [var errAEIllegalIndex: Int](/documentation/coreservices/erraeillegalindex)
- [var errAEImpossibleRange: Int](/documentation/coreservices/erraeimpossiblerange)
- [var errAEWrongNumberArgs: Int](/documentation/coreservices/erraewrongnumberargs)
- [var errAEAccessorNotFound: Int](/documentation/coreservices/erraeaccessornotfound)
- [var errAENoSuchLogical: Int](/documentation/coreservices/erraenosuchlogical)
- [var errAEBadTestKey: Int](/documentation/coreservices/erraebadtestkey)
- [var errAENoSuchObject: Int](/documentation/coreservices/erraenosuchobject)
- [var errAENegativeCount: Int](/documentation/coreservices/erraenegativecount)
- [var errAEEmptyListContainer: Int](/documentation/coreservices/erraeemptylistcontainer)
- [var errAEUnknownObjectType: Int](/documentation/coreservices/erraeunknownobjecttype)
- [var errAERecordingIsAlreadyOn: Int](/documentation/coreservices/erraerecordingisalreadyon)
- [var errAEReceiveTerminate: Int](/documentation/coreservices/erraereceiveterminate)
- [var errAEReceiveEscapeCurrent: Int](/documentation/coreservices/erraereceiveescapecurrent)
- [var errAEEventFiltered: Int](/documentation/coreservices/erraeeventfiltered)
- [var errAEDuplicateHandler: Int](/documentation/coreservices/erraeduplicatehandler)
- [var errAEStreamBadNesting: Int](/documentation/coreservices/erraestreambadnesting)
- [var errAEStreamAlreadyConverted: Int](/documentation/coreservices/erraestreamalreadyconverted)
- [var errAEDescIsNull: Int](/documentation/coreservices/erraedescisnull)
- [var errAEBuildSyntaxError: Int](/documentation/coreservices/erraebuildsyntaxerror)
- [var errAEBufferTooSmall: Int](/documentation/coreservices/erraebuffertoosmall)
- [var errASCantConsiderAndIgnore: Int](/documentation/coreservices/errascantconsiderandignore)
- [var errASCantCompareMoreThan32k: Int](/documentation/coreservices/errascantcomparemorethan32k)
- [var errASTerminologyNestingTooDeep: Int](/documentation/coreservices/errasterminologynestingtoodeep)
- [var errASIllegalFormalParameter: Int](/documentation/coreservices/errasillegalformalparameter)
- [var errASParameterNotForEvent: Int](/documentation/coreservices/errasparameternotforevent)
- [var errASNoResultReturned: Int](/documentation/coreservices/errasnoresultreturned)
- [var errAEEventFailed: Int](/documentation/coreservices/erraeeventfailed)
- [var errAETypeError: Int](/documentation/coreservices/erraetypeerror)
- [var errAEBadKeyForm: Int](/documentation/coreservices/erraebadkeyform)
- [var errAENotModifiable: Int](/documentation/coreservices/erraenotmodifiable)
- [var errAEPrivilegeError: Int](/documentation/coreservices/erraeprivilegeerror)
- [var errAEReadDenied: Int](/documentation/coreservices/erraereaddenied)
- [var errAEWriteDenied: Int](/documentation/coreservices/erraewritedenied)
- [var errAEIndexTooLarge: Int](/documentation/coreservices/erraeindextoolarge)
- [var errAENotAnElement: Int](/documentation/coreservices/erraenotanelement)
- [var errAECantSupplyType: Int](/documentation/coreservices/erraecantsupplytype)
- [var errAECantHandleClass: Int](/documentation/coreservices/erraecanthandleclass)
- [var errAEInTransaction: Int](/documentation/coreservices/erraeintransaction)
- [var errAENoSuchTransaction: Int](/documentation/coreservices/erraenosuchtransaction)
- [var errAENoUserSelection: Int](/documentation/coreservices/erraenouserselection)
- [var errAENotASingleObject: Int](/documentation/coreservices/erraenotasingleobject)
- [var errAECantUndo: Int](/documentation/coreservices/erraecantundo)
- [var errAENotAnEnumMember: Int](/documentation/coreservices/erraenotanenummember)
- [var errAECantPutThatThere: Int](/documentation/coreservices/erraecantputthatthere)
- [var errAEPropertiesClash: Int](/documentation/coreservices/erraepropertiesclash)
- [ColorSync Manager](/documentation/applicationservices/colorsync_manager)

### Working With Universal Procedure Pointers

- [NewCMBitmapCallBackUPP](/documentation/applicationservices/colorsync_manager/1805297-newcmbitmapcallbackupp)
- [DisposeCMBitmapCallBackUPP](/documentation/applicationservices/colorsync_manager/1805300-disposecmbitmapcallbackupp)
- [InvokeCMBitmapCallBackUPP](/documentation/applicationservices/colorsync_manager/1805303-invokecmbitmapcallbackupp)
- [NewCMConcatCallBackUPP](/documentation/applicationservices/colorsync_manager/1805306-newcmconcatcallbackupp)
- [DisposeCMConcatCallBackUPP](/documentation/applicationservices/colorsync_manager/1805310-disposecmconcatcallbackupp)
- [InvokeCMConcatCallBackUPP](/documentation/applicationservices/colorsync_manager/1805312-invokecmconcatcallbackupp)
- [NewCMFlattenUPP](/documentation/applicationservices/colorsync_manager/1805315-newcmflattenupp)
- [DisposeCMFlattenUPP](/documentation/applicationservices/colorsync_manager/1805318-disposecmflattenupp)
- [InvokeCMFlattenUPP](/documentation/applicationservices/colorsync_manager/1805320-invokecmflattenupp)
- [NewCMMIterateUPP](/documentation/applicationservices/colorsync_manager/1805322-newcmmiterateupp)
- [DisposeCMMIterateUPP](/documentation/applicationservices/colorsync_manager/1805323-disposecmmiterateupp)
- [InvokeCMMIterateUPP](/documentation/applicationservices/colorsync_manager/1805325-invokecmmiterateupp)
- [NewCMProfileIterateUPP](/documentation/applicationservices/colorsync_manager/1805339-newcmprofileiterateupp)
- [DisposeCMProfileIterateUPP](/documentation/applicationservices/colorsync_manager/1805341-disposecmprofileiterateupp)
- [InvokeCMProfileIterateUPP](/documentation/applicationservices/colorsync_manager/1805343-invokecmprofileiterateupp)

### Callbacks

- [CMFlattenProcPtr](/documentation/applicationservices/cmflattenprocptr)

### Data Types

- [CM2Profile](/documentation/applicationservices/cm2profile)

#### Initializers

- [init()](/documentation/applicationservices/cm2profile/1463399-init)
- [init(header: CM2Header, tagTable: CMTagElemTable, elemData: CChar)](/documentation/applicationservices/cm2profile/1460462-init)

#### Instance Properties

- [var elemData: CChar](/documentation/applicationservices/cm2profile/1459647-elemdata)
- [var header: CM2Header](/documentation/applicationservices/cm2profile/1462495-header)
- [var tagTable: CMTagElemTable](/documentation/applicationservices/cm2profile/1459173-tagtable)
- [CMDeviceInfo](/documentation/applicationservices/cmdeviceinfo)

#### Initializers

- [init()](/documentation/applicationservices/cmdeviceinfo/1458828-init)
- [init(dataVersion: UInt32, deviceClass: CMDeviceClass, deviceID: UInt32, deviceScope: CMDeviceScope, deviceState: UInt32, defaultProfileID: UInt32, deviceName: UnsafeMutablePointer<Unmanaged<CFDictionary>?>!, profileCount: UInt32, reserved: UInt32)](/documentation/applicationservices/cmdeviceinfo/1461251-init)

#### Instance Properties

- [var dataVersion: UInt32](/documentation/applicationservices/cmdeviceinfo/1464698-dataversion)
- [var defaultProfileID: UInt32](/documentation/applicationservices/cmdeviceinfo/1461755-defaultprofileid)
- [var deviceClass: CMDeviceClass](/documentation/applicationservices/cmdeviceinfo/1463209-deviceclass)
- [var deviceID: UInt32](/documentation/applicationservices/cmdeviceinfo/1458888-deviceid)
- [var deviceName: UnsafeMutablePointer<Unmanaged<CFDictionary>?>!](/documentation/applicationservices/cmdeviceinfo/1460441-devicename)
- [var deviceScope: CMDeviceScope](/documentation/applicationservices/cmdeviceinfo/1458913-devicescope)
- [var deviceState: UInt32](/documentation/applicationservices/cmdeviceinfo/1460889-devicestate)
- [var profileCount: UInt32](/documentation/applicationservices/cmdeviceinfo/1462497-profilecount)
- [var reserved: UInt32](/documentation/applicationservices/cmdeviceinfo/1459154-reserved)
- [CMDeviceProfileArray](/documentation/applicationservices/cmdeviceprofilearray)

#### Initializers

- [init()](/documentation/applicationservices/cmdeviceprofilearray/1462893-init)
- [init(profileCount: UInt32, profiles: CMDeviceProfileInfo)](/documentation/applicationservices/cmdeviceprofilearray/1458849-init)

#### Instance Properties

- [var profileCount: UInt32](/documentation/applicationservices/cmdeviceprofilearray/1463926-profilecount)
- [var profiles: CMDeviceProfileInfo](/documentation/applicationservices/cmdeviceprofilearray/1460443-profiles)
- [CMDeviceScope](/documentation/applicationservices/cmdevicescope)

#### Initializers

- [init()](/documentation/applicationservices/cmdevicescope/1460786-init)
- [init(deviceUser: Unmanaged<CFString>!, deviceHost: Unmanaged<CFString>!)](/documentation/applicationservices/cmdevicescope/1463053-init)

#### Instance Properties

- [var deviceHost: Unmanaged<CFString>!](/documentation/applicationservices/cmdevicescope/1463585-devicehost)
- [var deviceUser: Unmanaged<CFString>!](/documentation/applicationservices/cmdevicescope/1459017-deviceuser)
- [CMError](/documentation/coremotion/cmerror)
- [CMFlattenUPP](/documentation/applicationservices/cmflattenupp)
- [CMMultiFunctLutA2BType](/documentation/applicationservices/cmmultifunctluta2btype)
- [CMMultiFunctLutType](/documentation/applicationservices/cmmultifunctluttype)

#### Initializers

- [init()](/documentation/applicationservices/cmmultifunctluttype/1459815-init)
- [init(typeDescriptor: OSType, reserved: UInt32, inputChannels: UInt8, outputChannels: UInt8, reserved2: UInt16, offsetBcurves: UInt32, offsetMatrix: UInt32, offsetMcurves: UInt32, offsetCLUT: UInt32, offsetAcurves: UInt32, data: UInt8)](/documentation/applicationservices/cmmultifunctluttype/1459199-init)

#### Instance Properties

- [var data: UInt8](/documentation/applicationservices/cmmultifunctluttype/1459674-data)
- [var inputChannels: UInt8](/documentation/applicationservices/cmmultifunctluttype/1460768-inputchannels)
- [var offsetAcurves: UInt32](/documentation/applicationservices/cmmultifunctluttype/1460358-offsetacurves)
- [var offsetBcurves: UInt32](/documentation/applicationservices/cmmultifunctluttype/1459105-offsetbcurves)
- [var offsetCLUT: UInt32](/documentation/applicationservices/cmmultifunctluttype/1459754-offsetclut)
- [var offsetMatrix: UInt32](/documentation/applicationservices/cmmultifunctluttype/1461992-offsetmatrix)
- [var offsetMcurves: UInt32](/documentation/applicationservices/cmmultifunctluttype/1459305-offsetmcurves)
- [var outputChannels: UInt8](/documentation/applicationservices/cmmultifunctluttype/1464459-outputchannels)
- [var reserved: UInt32](/documentation/applicationservices/cmmultifunctluttype/1460102-reserved)
- [var reserved2: UInt16](/documentation/applicationservices/cmmultifunctluttype/1459994-reserved2)
- [var typeDescriptor: OSType](/documentation/applicationservices/cmmultifunctluttype/1464404-typedescriptor)
- [CMXYZColor](/documentation/applicationservices/cmxyzcolor)

#### Initializers

- [init()](/documentation/applicationservices/cmxyzcolor/1462111-init)
- [init(X: CMXYZComponent, Y: CMXYZComponent, Z: CMXYZComponent)](/documentation/applicationservices/cmxyzcolor/1459192-init)

#### Instance Properties

- [var X: CMXYZComponent](/documentation/applicationservices/cmxyzcolor/1458784-x)
- [var Y: CMXYZComponent](/documentation/applicationservices/cmxyzcolor/1463301-y)
- [var Z: CMXYZComponent](/documentation/applicationservices/cmxyzcolor/1460905-z)
- [CMXYZComponent](/documentation/applicationservices/cmxyzcomponent)

### Constants

- [Abstract Color Space Constants](/documentation/applicationservices/colorsync_manager/1560701-abstract_color_space_constants)

#### Constants

- [var cmNoSpace: Int](/documentation/applicationservices/cmnospace)
- [var cmRGBSpace: Int](/documentation/applicationservices/cmrgbspace)
- [var cmCMYKSpace: Int](/documentation/applicationservices/cmcmykspace)
- [var cmHSVSpace: Int](/documentation/applicationservices/cmhsvspace)
- [var cmHLSSpace: Int](/documentation/applicationservices/cmhlsspace)
- [var cmYXYSpace: Int](/documentation/applicationservices/cmyxyspace)
- [var cmXYZSpace: Int](/documentation/applicationservices/cmxyzspace)
- [var cmLUVSpace: Int](/documentation/applicationservices/cmluvspace)
- [var cmLABSpace: Int](/documentation/applicationservices/cmlabspace)
- [var cmReservedSpace1: Int](/documentation/applicationservices/cmreservedspace1)
- [var cmGraySpace: Int](/documentation/applicationservices/cmgrayspace)
- [var cmReservedSpace2: Int](/documentation/applicationservices/cmreservedspace2)
- [var cmGamutResultSpace: Int](/documentation/applicationservices/cmgamutresultspace)
- [var cmNamedIndexedSpace: Int](/documentation/applicationservices/cmnamedindexedspace)
- [var cmMCFiveSpace: Int](/documentation/applicationservices/cmmcfivespace)
- [var cmMCSixSpace: Int](/documentation/applicationservices/cmmcsixspace)
- [var cmMCSevenSpace: Int](/documentation/applicationservices/cmmcsevenspace)
- [var cmMCEightSpace: Int](/documentation/applicationservices/cmmceightspace)
- [var cmAlphaPmulSpace: Int](/documentation/applicationservices/cmalphapmulspace)
- [var cmAlphaSpace: Int](/documentation/applicationservices/cmalphaspace)
- [var cmRGBASpace: Int](/documentation/applicationservices/cmrgbaspace)
- [var cmGrayASpace: Int](/documentation/applicationservices/cmgrayaspace)
- [var cmRGBAPmulSpace: Int](/documentation/applicationservices/cmrgbapmulspace)
- [var cmGrayAPmulSpace: Int](/documentation/applicationservices/cmgrayapmulspace)
- [Channel Encoding Format](/documentation/applicationservices/colorsync_manager/1560324-channel_encoding_format)

#### Constants

- [var cmSRGB16ChannelEncoding: Int](/documentation/applicationservices/cmsrgb16channelencoding)
- [Color Packing for Color Spaces](/documentation/applicationservices/colorsync_manager/1560270-color_packing_for_color_spaces)

#### Constants

- [var cmNoColorPacking: Int](/documentation/applicationservices/cmnocolorpacking)
- [var cmWord5ColorPacking: Int](/documentation/applicationservices/cmword5colorpacking)
- [var cmWord565ColorPacking: Int](/documentation/applicationservices/cmword565colorpacking)
- [var cmLong8ColorPacking: Int](/documentation/applicationservices/cmlong8colorpacking)
- [var cmLong10ColorPacking: Int](/documentation/applicationservices/cmlong10colorpacking)
- [var cmAlphaFirstPacking: Int](/documentation/applicationservices/cmalphafirstpacking)
- [var cmOneBitDirectPacking: Int](/documentation/applicationservices/cmonebitdirectpacking)
- [var cmAlphaLastPacking: Int](/documentation/applicationservices/cmalphalastpacking)
- [var cm8_8ColorPacking: Int](/documentation/applicationservices/cm8_8colorpacking)
- [var cm16_8ColorPacking: Int](/documentation/applicationservices/cm16_8colorpacking)
- [var cm24_8ColorPacking: Int](/documentation/applicationservices/cm24_8colorpacking)
- [var cm32_8ColorPacking: Int](/documentation/applicationservices/cm32_8colorpacking)
- [var cm40_8ColorPacking: Int](/documentation/applicationservices/cm40_8colorpacking)
- [var cm48_8ColorPacking: Int](/documentation/applicationservices/cm48_8colorpacking)
- [var cm56_8ColorPacking: Int](/documentation/applicationservices/cm56_8colorpacking)
- [var cm64_8ColorPacking: Int](/documentation/applicationservices/cm64_8colorpacking)
- [var cm32_16ColorPacking: Int](/documentation/applicationservices/cm32_16colorpacking)
- [var cm48_16ColorPacking: Int](/documentation/applicationservices/cm48_16colorpacking)
- [var cm64_16ColorPacking: Int](/documentation/applicationservices/cm64_16colorpacking)
- [var cm32_32ColorPacking: Int](/documentation/applicationservices/cm32_32colorpacking)
- [var cmLittleEndianPacking: Int](/documentation/applicationservices/cmlittleendianpacking)
- [var cmReverseChannelPacking: Int](/documentation/applicationservices/cmreversechannelpacking)
- [Color Space Signatures](/documentation/applicationservices/colorsync_manager/1560276-color_space_signatures)

#### Constants

- [var cmXYZData: Int](/documentation/applicationservices/cmxyzdata)
- [var cmLabData: Int](/documentation/applicationservices/cmlabdata)
- [var cmLuvData: Int](/documentation/applicationservices/cmluvdata)
- [var cmYCbCrData: Int](/documentation/applicationservices/cmycbcrdata)
- [var cmYxyData: Int](/documentation/applicationservices/cmyxydata)
- [var cmRGBData: Int](/documentation/applicationservices/cmrgbdata)
- [var cmSRGBData: Int](/documentation/applicationservices/cmsrgbdata)
- [var cmGrayData: Int](/documentation/applicationservices/cmgraydata)
- [var cmHSVData: Int](/documentation/applicationservices/cmhsvdata)
- [var cmHLSData: Int](/documentation/applicationservices/cmhlsdata)
- [var cmCMYKData: Int](/documentation/applicationservices/cmcmykdata)
- [var cmCMYData: Int](/documentation/applicationservices/cmcmydata)
- [var cmMCH5Data: Int](/documentation/applicationservices/cmmch5data)
- [var cmMCH6Data: Int](/documentation/applicationservices/cmmch6data)
- [var cmMCH7Data: Int](/documentation/applicationservices/cmmch7data)
- [var cmMCH8Data: Int](/documentation/applicationservices/cmmch8data)
- [var cm3CLRData: Int](/documentation/applicationservices/cm3clrdata)
- [var cm4CLRData: Int](/documentation/applicationservices/cm4clrdata)
- [var cm5CLRData: Int](/documentation/applicationservices/cm5clrdata)
- [var cm6CLRData: Int](/documentation/applicationservices/cm6clrdata)
- [var cm7CLRData: Int](/documentation/applicationservices/cm7clrdata)
- [var cm8CLRData: Int](/documentation/applicationservices/cm8clrdata)
- [var cm9CLRData: Int](/documentation/applicationservices/cm9clrdata)
- [var cm10CLRData: Int](/documentation/applicationservices/cm10clrdata)
- [var cm11CLRData: Int](/documentation/applicationservices/cm11clrdata)
- [var cm12CLRData: Int](/documentation/applicationservices/cm12clrdata)
- [var cm13CLRData: Int](/documentation/applicationservices/cm13clrdata)
- [var cm14CLRData: Int](/documentation/applicationservices/cm14clrdata)
- [var cm15CLRData: Int](/documentation/applicationservices/cm15clrdata)
- [var cmNamedData: Int](/documentation/applicationservices/cmnameddata)
- [Color Space Masks](/documentation/applicationservices/colorsync_manager/1560521-color_space_masks)

#### Constants

- [var cmColorSpaceSpaceMask: Int](/documentation/applicationservices/cmcolorspacespacemask)
- [var cmColorSpacePremulAlphaMask: Int](/documentation/applicationservices/cmcolorspacepremulalphamask)
- [var cmColorSpaceAlphaMask: Int](/documentation/applicationservices/cmcolorspacealphamask)
- [var cmColorSpaceSpaceAndAlphaMask: Int](/documentation/applicationservices/cmcolorspacespaceandalphamask)
- [var cmColorSpacePackingMask: Int](/documentation/applicationservices/cmcolorspacepackingmask)
- [var cmColorSpaceEncodingMask: Int](/documentation/applicationservices/cmcolorspaceencodingmask)
- [var cmColorSpaceReservedMask: Int](/documentation/applicationservices/cmcolorspacereservedmask)
- [Current Device Versions](/documentation/applicationservices/colorsync_manager/1560472-current_device_versions)

#### Constants

- [var cmDeviceInfoVersion1: Int](/documentation/applicationservices/cmdeviceinfoversion1)
- [var cmDeviceProfileInfoVersion1: Int](/documentation/applicationservices/cmdeviceprofileinfoversion1)
- [var cmDeviceProfileInfoVersion2: Int](/documentation/applicationservices/cmdeviceprofileinfoversion2)
- [Current Info Versions](/documentation/applicationservices/colorsync_manager/1560146-current_info_versions)

#### Constants

- [var cmCurrentDeviceInfoVersion: Int](/documentation/applicationservices/cmcurrentdeviceinfoversion)
- [var cmCurrentProfileInfoVersion: Int](/documentation/applicationservices/cmcurrentprofileinfoversion)
- [Current Major Version Mask](/documentation/applicationservices/colorsync_manager/1560659-current_major_version_mask)

#### Constants

- [var cmProfileMajorVersionMask: Int](/documentation/applicationservices/cmprofilemajorversionmask)
- [var cmCurrentProfileMajorVersion: Int](/documentation/applicationservices/cmcurrentprofilemajorversion)
- [Data Transfer Commands](/documentation/applicationservices/colorsync_manager/1560166-data_transfer_commands)

#### Constants

- [var cmOpenReadSpool: Int](/documentation/applicationservices/cmopenreadspool)
- [var cmOpenWriteSpool: Int](/documentation/applicationservices/cmopenwritespool)
- [var cmReadSpool: Int](/documentation/applicationservices/cmreadspool)
- [var cmWriteSpool: Int](/documentation/applicationservices/cmwritespool)
- [var cmCloseSpool: Int](/documentation/applicationservices/cmclosespool)
- [Data Type Element Values](/documentation/applicationservices/colorsync_manager/1560593-data_type_element_values)

#### Constants

- [var cmAsciiData: Int](/documentation/applicationservices/cmasciidata)
- [var cmBinaryData: Int](/documentation/applicationservices/cmbinarydata)
- [Default CMM Signature](/documentation/applicationservices/colorsync_manager/1560689-default_cmm_signature)

#### Constants

- [var kDefaultCMMSignature: Int](/documentation/applicationservices/kdefaultcmmsignature)
- [Default IDs](/documentation/applicationservices/colorsync_manager/1560386-default_ids)

#### Constants

- [var cmDefaultDeviceID: Int](/documentation/applicationservices/cmdefaultdeviceid)
- [var cmDefaultProfileID: Int](/documentation/applicationservices/cmdefaultprofileid)
- [Device Attribute Values for Version 2.x Profiles](/documentation/applicationservices/colorsync_manager/1560447-device_attribute_values_for_vers)

#### Constants

- [var cmReflectiveTransparentMask: Int](/documentation/applicationservices/cmreflectivetransparentmask)
- [var cmGlossyMatteMask: Int](/documentation/applicationservices/cmglossymattemask)
- [CMDeviceClass](/documentation/applicationservices/cmdeviceclass)

#### Constants

- [var cmScannerDeviceClass: Int](/documentation/applicationservices/cmscannerdeviceclass)
- [var cmCameraDeviceClass: Int](/documentation/applicationservices/cmcameradeviceclass)
- [var cmDisplayDeviceClass: Int](/documentation/applicationservices/cmdisplaydeviceclass)
- [var cmPrinterDeviceClass: Int](/documentation/applicationservices/cmprinterdeviceclass)
- [var cmProofDeviceClass: Int](/documentation/applicationservices/cmproofdeviceclass)
- [Device and Media Attributes](/documentation/applicationservices/colorsync_manager/1560327-device_and_media_attributes)

#### Constants

- [var cmReflective: Int](/documentation/applicationservices/cmreflective)
- [var cmGlossy: Int](/documentation/applicationservices/cmglossy)
- [Device States](/documentation/applicationservices/colorsync_manager/1560516-device_states)

#### Constants

- [var cmDeviceStateDefault: Int](/documentation/applicationservices/cmdevicestatedefault)
- [var cmDeviceStateOffline: Int](/documentation/applicationservices/cmdevicestateoffline)
- [var cmDeviceStateBusy: Int](/documentation/applicationservices/cmdevicestatebusy)
- [var cmDeviceStateForceNotify: Int](/documentation/applicationservices/cmdevicestateforcenotify)
- [var cmDeviceStateDeviceRsvdBits: Int](/documentation/applicationservices/cmdevicestatedevicersvdbits)
- [var cmDeviceStateAppleRsvdBits: Int](/documentation/applicationservices/cmdevicestateapplersvdbits)
- [Element Tags and Signatures for Version 1.0 Profiles](/documentation/applicationservices/colorsync_manager/1560273-element_tags_and_signatures_for_)

#### Constants

- [var cmCS1ChromTag: Int](/documentation/applicationservices/cmcs1chromtag)
- [var cmCS1TRCTag: Int](/documentation/applicationservices/cmcs1trctag)
- [var cmCS1NameTag: Int](/documentation/applicationservices/cmcs1nametag)
- [var cmCS1CustTag: Int](/documentation/applicationservices/cmcs1custtag)
- [Embedded Profile Flags](/documentation/applicationservices/colorsync_manager/1560148-embedded_profile_flags)

#### Constants

- [var cmEmbeddedProfile: Int](/documentation/applicationservices/cmembeddedprofile)
- [var cmEmbeddedUse: Int](/documentation/applicationservices/cmembeddeduse)
- [Flag Mask Definitions for Version 2.x Profiles](/documentation/applicationservices/colorsync_manager/1560699-flag_mask_definitions_for_versio)

#### Constants

- [var cmICCReservedFlagsMask: Int](/documentation/applicationservices/cmiccreservedflagsmask)
- [var cmEmbeddedMask: Int](/documentation/applicationservices/cmembeddedmask)
- [var cmEmbeddedUseMask: Int](/documentation/applicationservices/cmembeddedusemask)
- [var cmCMSReservedFlagsMask: Int](/documentation/applicationservices/cmcmsreservedflagsmask)
- [var cmQualityMask: Int](/documentation/applicationservices/cmqualitymask)
- [var cmInterpolationMask: Int](/documentation/applicationservices/cminterpolationmask)
- [var cmGamutCheckingMask: Int](/documentation/applicationservices/cmgamutcheckingmask)
- [var cmBlackPointCompensationMask: Int](/documentation/applicationservices/cmblackpointcompensationmask)
- [ICC Profile Versions](/documentation/applicationservices/colorsync_manager/1560658-icc_profile_versions)

#### Constants

- [var cmICCProfileVersion4: Int](/documentation/applicationservices/cmiccprofileversion4)
- [var cmICCProfileVersion2: Int](/documentation/applicationservices/cmiccprofileversion2)
- [var cmICCProfileVersion21: Int](/documentation/applicationservices/cmiccprofileversion21)
- [var cmCS2ProfileVersion: Int](/documentation/applicationservices/cmcs2profileversion)
- [var cmCS1ProfileVersion: Int](/documentation/applicationservices/cmcs1profileversion)
- [Illuminant Measurement Endocings](/documentation/applicationservices/colorsync_manager/1560108-illuminant_measurement_endocings)

#### Constants

- [var cmIlluminantUnknown: Int](/documentation/applicationservices/cmilluminantunknown)
- [var cmIlluminantD50: Int](/documentation/applicationservices/cmilluminantd50)
- [var cmIlluminantD65: Int](/documentation/applicationservices/cmilluminantd65)
- [var cmIlluminantD93: Int](/documentation/applicationservices/cmilluminantd93)
- [var cmIlluminantF2: Int](/documentation/applicationservices/cmilluminantf2)
- [var cmIlluminantD55: Int](/documentation/applicationservices/cmilluminantd55)
- [var cmIlluminantA: Int](/documentation/applicationservices/cmilluminanta)
- [var cmIlluminantEquiPower: Int](/documentation/applicationservices/cmilluminantequipower)
- [var cmIlluminantF8: Int](/documentation/applicationservices/cmilluminantf8)
- [Magic Cookie Number](/documentation/applicationservices/colorsync_manager/1560690-magic_cookie_number)

#### Constants

- [var cmMagicNumber: Int](/documentation/applicationservices/cmmagicnumber)
- [Maximum Path Size](/documentation/applicationservices/colorsync_manager/1560101-maximum_path_size)

#### Constants

- [var CS_MAX_PATH: Int](/documentation/applicationservices/cs_max_path)
- [Measurement Flares](/documentation/applicationservices/colorsync_manager/1560283-measurement_flares)

#### Constants

- [var cmFlare0: Int](/documentation/applicationservices/cmflare0)
- [var cmFlare100: Int](/documentation/applicationservices/cmflare100)
- [Measurement Geometries](/documentation/applicationservices/colorsync_manager/1560539-measurement_geometries)

#### Constants

- [var cmGeometryUnknown: Int](/documentation/applicationservices/cmgeometryunknown)
- [var cmGeometry045or450: Int](/documentation/applicationservices/cmgeometry045or450)
- [var cmGeometry0dord0: Int](/documentation/applicationservices/cmgeometry0dord0)
- [Parametric Types](/documentation/applicationservices/colorsync_manager/1560541-parametric_types)

#### Constants

- [var cmParametricType0: Int](/documentation/applicationservices/cmparametrictype0)
- [var cmParametricType1: Int](/documentation/applicationservices/cmparametrictype1)
- [var cmParametricType2: Int](/documentation/applicationservices/cmparametrictype2)
- [var cmParametricType3: Int](/documentation/applicationservices/cmparametrictype3)
- [var cmParametricType4: Int](/documentation/applicationservices/cmparametrictype4)
- [Platform Enumeration Values](/documentation/applicationservices/colorsync_manager/1560191-platform_enumeration_values)

#### Constants

- [var cmMacintosh: Int](/documentation/applicationservices/cmmacintosh)
- [var cmMicrosoft: Int](/documentation/applicationservices/cmmicrosoft)
- [var cmSiliconGraphics: Int](/documentation/applicationservices/cmsilicongraphics)
- [var cmSolaris: Int](/documentation/applicationservices/cmsolaris)
- [var cmTaligent: Int](/documentation/applicationservices/cmtaligent)
- [Profile Iteration Values](/documentation/applicationservices/colorsync_manager/1560091-profile_iteration_values)

#### Constants

- [var cmIterateFactoryDeviceProfiles: Int](/documentation/applicationservices/cmiteratefactorydeviceprofiles)
- [var cmIterateCustomDeviceProfiles: Int](/documentation/applicationservices/cmiteratecustomdeviceprofiles)
- [var cmIterateCurrentDeviceProfiles: Int](/documentation/applicationservices/cmiteratecurrentdeviceprofiles)
- [var cmIterateAllDeviceProfiles: Int](/documentation/applicationservices/cmiteratealldeviceprofiles)
- [var cmIterateDeviceProfilesMask: Int](/documentation/applicationservices/cmiteratedeviceprofilesmask)
- [Profile Location Sizes](/documentation/applicationservices/colorsync_manager/1560369-profile_location_sizes)

#### Constants

- [var cmOriginalProfileLocationSize: Int](/documentation/applicationservices/cmoriginalprofilelocationsize)
- [var cmCurrentProfileLocationSize: Int](/documentation/applicationservices/cmcurrentprofilelocationsize)
- [PostScript Data Formats](/documentation/applicationservices/colorsync_manager/1560551-postscript_data_formats)

#### Constants

- [var cmPS7bit: Int](/documentation/applicationservices/cmps7bit)
- [var cmPS8bit: Int](/documentation/applicationservices/cmps8bit)
- [Profile Access Procedures](/documentation/applicationservices/colorsync_manager/1560733-profile_access_procedures)

#### Constants

- [var cmOpenReadAccess: Int](/documentation/applicationservices/cmopenreadaccess)
- [var cmOpenWriteAccess: Int](/documentation/applicationservices/cmopenwriteaccess)
- [var cmReadAccess: Int](/documentation/applicationservices/cmreadaccess)
- [var cmWriteAccess: Int](/documentation/applicationservices/cmwriteaccess)
- [var cmCloseAccess: Int](/documentation/applicationservices/cmcloseaccess)
- [var cmCreateNewAccess: Int](/documentation/applicationservices/cmcreatenewaccess)
- [var cmAbortWriteAccess: Int](/documentation/applicationservices/cmabortwriteaccess)
- [var cmBeginAccess: Int](/documentation/applicationservices/cmbeginaccess)
- [var cmEndAccess: Int](/documentation/applicationservices/cmendaccess)
- [Profile Classes](/documentation/applicationservices/colorsync_manager/1560630-profile_classes)

#### Constants

- [var cmInputClass: Int](/documentation/applicationservices/cminputclass)
- [var cmDisplayClass: Int](/documentation/applicationservices/cmdisplayclass)
- [var cmOutputClass: Int](/documentation/applicationservices/cmoutputclass)
- [var cmLinkClass: Int](/documentation/applicationservices/cmlinkclass)
- [var cmAbstractClass: Int](/documentation/applicationservices/cmabstractclass)
- [var cmColorSpaceClass: Int](/documentation/applicationservices/cmcolorspaceclass)
- [var cmNamedColorClass: Int](/documentation/applicationservices/cmnamedcolorclass)
- [Profile Concatenation Values](/documentation/applicationservices/colorsync_manager/1560373-profile_concatenation_values)

#### Constants

- [var kNoTransform: Int](/documentation/applicationservices/knotransform)
- [var kUseAtoB: Int](/documentation/applicationservices/kuseatob)
- [var kUseBtoA: Int](/documentation/applicationservices/kusebtoa)
- [var kUseBtoB: Int](/documentation/applicationservices/kusebtob)
- [var kDeviceToPCS: Int](/documentation/applicationservices/kdevicetopcs)
- [var kPCSToDevice: Int](/documentation/applicationservices/kpcstodevice)
- [var kPCSToPCS: Int](/documentation/applicationservices/kpcstopcs)
- [var kUseProfileIntent: Int](/documentation/applicationservices/kuseprofileintent)
- [Profile Iteration Constants](/documentation/applicationservices/colorsync_manager/1560189-profile_iteration_constants)

#### Constants

- [var cmProfileIterateDataVersion1: Int](/documentation/applicationservices/cmprofileiteratedataversion1)
- [var cmProfileIterateDataVersion2: Int](/documentation/applicationservices/cmprofileiteratedataversion2)
- [var cmProfileIterateDataVersion3: Int](/documentation/applicationservices/cmprofileiteratedataversion3)
- [var cmProfileIterateDataVersion4: Int](/documentation/applicationservices/cmprofileiteratedataversion4)
- [Profile Location Type](/documentation/applicationservices/colorsync_manager/1560599-profile_location_type)

#### Constants

- [var cmNoProfileBase: Int](/documentation/applicationservices/cmnoprofilebase)
- [var cmPathBasedProfile: Int](/documentation/applicationservices/cmpathbasedprofile)
- [var cmBufferBasedProfile: Int](/documentation/applicationservices/cmbufferbasedprofile)
- [Public Tags](/documentation/applicationservices/colorsync_manager/1560717-public_tags)

#### Constants

- [var cmAToB0Tag: Int](/documentation/applicationservices/cmatob0tag)
- [var cmAToB1Tag: Int](/documentation/applicationservices/cmatob1tag)
- [var cmAToB2Tag: Int](/documentation/applicationservices/cmatob2tag)
- [var cmBlueColorantTag: Int](/documentation/applicationservices/cmbluecoloranttag)
- [var cmBlueTRCTag: Int](/documentation/applicationservices/cmbluetrctag)
- [var cmBToA0Tag: Int](/documentation/applicationservices/cmbtoa0tag)
- [var cmBToA1Tag: Int](/documentation/applicationservices/cmbtoa1tag)
- [var cmBToA2Tag: Int](/documentation/applicationservices/cmbtoa2tag)
- [var cmCalibrationDateTimeTag: Int](/documentation/applicationservices/cmcalibrationdatetimetag)
- [var cmChromaticAdaptationTag: Int](/documentation/applicationservices/cmchromaticadaptationtag)
- [var cmCharTargetTag: Int](/documentation/applicationservices/cmchartargettag)
- [var cmCopyrightTag: Int](/documentation/applicationservices/cmcopyrighttag)
- [var cmDeviceMfgDescTag: Int](/documentation/applicationservices/cmdevicemfgdesctag)
- [var cmDeviceModelDescTag: Int](/documentation/applicationservices/cmdevicemodeldesctag)
- [var cmGamutTag: Int](/documentation/applicationservices/cmgamuttag)
- [var cmGrayTRCTag: Int](/documentation/applicationservices/cmgraytrctag)
- [var cmGreenColorantTag: Int](/documentation/applicationservices/cmgreencoloranttag)
- [var cmGreenTRCTag: Int](/documentation/applicationservices/cmgreentrctag)
- [var cmLuminanceTag: Int](/documentation/applicationservices/cmluminancetag)
- [var cmMeasurementTag: Int](/documentation/applicationservices/cmmeasurementtag)
- [var cmMediaBlackPointTag: Int](/documentation/applicationservices/cmmediablackpointtag)
- [var cmMediaWhitePointTag: Int](/documentation/applicationservices/cmmediawhitepointtag)
- [var cmNamedColorTag: Int](/documentation/applicationservices/cmnamedcolortag)
- [var cmNamedColor2Tag: Int](/documentation/applicationservices/cmnamedcolor2tag)
- [var cmPreview0Tag: Int](/documentation/applicationservices/cmpreview0tag)
- [var cmPreview1Tag: Int](/documentation/applicationservices/cmpreview1tag)
- [var cmPreview2Tag: Int](/documentation/applicationservices/cmpreview2tag)
- [var cmProfileDescriptionTag: Int](/documentation/applicationservices/cmprofiledescriptiontag)
- [var cmProfileSequenceDescTag: Int](/documentation/applicationservices/cmprofilesequencedesctag)
- [var cmPS2CRD0Tag: Int](/documentation/applicationservices/cmps2crd0tag)
- [var cmPS2CRD1Tag: Int](/documentation/applicationservices/cmps2crd1tag)
- [var cmPS2CRD2Tag: Int](/documentation/applicationservices/cmps2crd2tag)
- [var cmPS2CRD3Tag: Int](/documentation/applicationservices/cmps2crd3tag)
- [var cmPS2CSATag: Int](/documentation/applicationservices/cmps2csatag)
- [var cmPS2RenderingIntentTag: Int](/documentation/applicationservices/cmps2renderingintenttag)
- [var cmRedColorantTag: Int](/documentation/applicationservices/cmredcoloranttag)
- [var cmRedTRCTag: Int](/documentation/applicationservices/cmredtrctag)
- [var cmScreeningDescTag: Int](/documentation/applicationservices/cmscreeningdesctag)
- [var cmScreeningTag: Int](/documentation/applicationservices/cmscreeningtag)
- [var cmTechnologyTag: Int](/documentation/applicationservices/cmtechnologytag)
- [var cmUcrBgTag: Int](/documentation/applicationservices/cmucrbgtag)
- [var cmViewingConditionsDescTag: Int](/documentation/applicationservices/cmviewingconditionsdesctag)
- [var cmViewingConditionsTag: Int](/documentation/applicationservices/cmviewingconditionstag)
- [Public Type Signatures](/documentation/applicationservices/colorsync_manager/1560346-public_type_signatures)

#### Constants

- [var cmSigCrdInfoType: Int](/documentation/applicationservices/cmsigcrdinfotype)
- [var cmSigCurveType: Int](/documentation/applicationservices/cmsigcurvetype)
- [var cmSigDataType: Int](/documentation/applicationservices/cmsigdatatype)
- [var cmSigDateTimeType: Int](/documentation/applicationservices/cmsigdatetimetype)
- [var cmSigLut16Type: Int](/documentation/applicationservices/cmsiglut16type)
- [var cmSigLut8Type: Int](/documentation/applicationservices/cmsiglut8type)
- [var cmSigMeasurementType: Int](/documentation/applicationservices/cmsigmeasurementtype)
- [var cmSigMultiFunctA2BType: Int](/documentation/applicationservices/cmsigmultifuncta2btype)
- [var cmSigMultiFunctB2AType: Int](/documentation/applicationservices/cmsigmultifunctb2atype)
- [var cmSigNamedColorType: Int](/documentation/applicationservices/cmsignamedcolortype)
- [var cmSigNamedColor2Type: Int](/documentation/applicationservices/cmsignamedcolor2type)
- [var cmSigParametricCurveType: Int](/documentation/applicationservices/cmsigparametriccurvetype)
- [var cmSigProfileDescriptionType: Int](/documentation/applicationservices/cmsigprofiledescriptiontype)
- [var cmSigProfileSequenceDescType: Int](/documentation/applicationservices/cmsigprofilesequencedesctype)
- [var cmSigScreeningType: Int](/documentation/applicationservices/cmsigscreeningtype)
- [var cmSigS15Fixed16Type: Int](/documentation/applicationservices/cmsigs15fixed16type)
- [var cmSigSignatureType: Int](/documentation/applicationservices/cmsigsignaturetype)
- [var cmSigTextType: Int](/documentation/applicationservices/cmsigtexttype)
- [var cmSigU16Fixed16Type: Int](/documentation/applicationservices/cmsigu16fixed16type)
- [var cmSigU1Fixed15Type: Int](/documentation/applicationservices/cmsigu1fixed15type)
- [var cmSigUInt8Type: Int](/documentation/applicationservices/cmsiguint8type)
- [var cmSigUInt16Type: Int](/documentation/applicationservices/cmsiguint16type)
- [var cmSigUInt32Type: Int](/documentation/applicationservices/cmsiguint32type)
- [var cmSigUInt64Type: Int](/documentation/applicationservices/cmsiguint64type)
- [var cmSigUcrBgType: Int](/documentation/applicationservices/cmsigucrbgtype)
- [var cmSigUnicodeTextType: Int](/documentation/applicationservices/cmsigunicodetexttype)
- [var cmSigViewingConditionsType: Int](/documentation/applicationservices/cmsigviewingconditionstype)
- [var cmSigXYZType: Int](/documentation/applicationservices/cmsigxyztype)
- [Quality Flag Values for Version 2.x Profiles](/documentation/applicationservices/colorsync_manager/1560115-quality_flag_values_for_version_)

#### Constants

- [var cmNormalMode: Int](/documentation/applicationservices/cmnormalmode)
- [var cmDraftMode: Int](/documentation/applicationservices/cmdraftmode)
- [var cmBestMode: Int](/documentation/applicationservices/cmbestmode)
- [Rendering Intent Values for Version 2.x Profiles](/documentation/applicationservices/colorsync_manager/1560278-rendering_intent_values_for_vers)

#### Constants

- [var cmPerceptual: Int](/documentation/applicationservices/cmperceptual)
- [var cmRelativeColorimetric: Int](/documentation/applicationservices/cmrelativecolorimetric)
- [var cmSaturation: Int](/documentation/applicationservices/cmsaturation)
- [var cmAbsoluteColorimetric: Int](/documentation/applicationservices/cmabsolutecolorimetric)
- [Screen Encoding Tags](/documentation/applicationservices/colorsync_manager/1560247-screen_encoding_tags)

#### Constants

- [var cmPrtrDefaultScreens: Int](/documentation/applicationservices/cmprtrdefaultscreens)
- [var cmLinesPer: Int](/documentation/applicationservices/cmlinesper)
- [Spot Function Values](/documentation/applicationservices/colorsync_manager/1560411-spot_function_values)

#### Constants

- [var cmSpotFunctionUnknown: Int](/documentation/applicationservices/cmspotfunctionunknown)
- [var cmSpotFunctionDefault: Int](/documentation/applicationservices/cmspotfunctiondefault)
- [var cmSpotFunctionRound: Int](/documentation/applicationservices/cmspotfunctionround)
- [var cmSpotFunctionDiamond: Int](/documentation/applicationservices/cmspotfunctiondiamond)
- [var cmSpotFunctionEllipse: Int](/documentation/applicationservices/cmspotfunctionellipse)
- [var cmSpotFunctionLine: Int](/documentation/applicationservices/cmspotfunctionline)
- [var cmSpotFunctionSquare: Int](/documentation/applicationservices/cmspotfunctionsquare)
- [var cmSpotFunctionCross: Int](/documentation/applicationservices/cmspotfunctioncross)
- [Standard Observer](/documentation/applicationservices/colorsync_manager/1560388-standard_observer)

#### Constants

- [var cmStdobsUnknown: Int](/documentation/applicationservices/cmstdobsunknown)
- [var cmStdobs1931TwoDegrees: Int](/documentation/applicationservices/cmstdobs1931twodegrees)
- [var cmStdobs1964TenDegrees: Int](/documentation/applicationservices/cmstdobs1964tendegrees)
- [Tag Type Information](/documentation/applicationservices/colorsync_manager/1560086-tag_type_information)

#### Constants

- [var cmNumHeaderElements: Int](/documentation/applicationservices/cmnumheaderelements)
- [Technology Tag Descriptions](/documentation/applicationservices/colorsync_manager/1560433-technology_tag_descriptions)

#### Constants

- [var cmTechnologyDigitalCamera: Int](/documentation/applicationservices/cmtechnologydigitalcamera)
- [var cmTechnologyFilmScanner: Int](/documentation/applicationservices/cmtechnologyfilmscanner)
- [var cmTechnologyReflectiveScanner: Int](/documentation/applicationservices/cmtechnologyreflectivescanner)
- [var cmTechnologyInkJetPrinter: Int](/documentation/applicationservices/cmtechnologyinkjetprinter)
- [var cmTechnologyThermalWaxPrinter: Int](/documentation/applicationservices/cmtechnologythermalwaxprinter)
- [var cmTechnologyElectrophotographicPrinter: Int](/documentation/applicationservices/cmtechnologyelectrophotographicprinter)
- [var cmTechnologyElectrostaticPrinter: Int](/documentation/applicationservices/cmtechnologyelectrostaticprinter)
- [var cmTechnologyDyeSublimationPrinter: Int](/documentation/applicationservices/cmtechnologydyesublimationprinter)
- [var cmTechnologyPhotographicPaperPrinter: Int](/documentation/applicationservices/cmtechnologyphotographicpaperprinter)
- [var cmTechnologyFilmWriter: Int](/documentation/applicationservices/cmtechnologyfilmwriter)
- [var cmTechnologyVideoMonitor: Int](/documentation/applicationservices/cmtechnologyvideomonitor)
- [var cmTechnologyVideoCamera: Int](/documentation/applicationservices/cmtechnologyvideocamera)
- [var cmTechnologyProjectionTelevision: Int](/documentation/applicationservices/cmtechnologyprojectiontelevision)
- [var cmTechnologyCRTDisplay: Int](/documentation/applicationservices/cmtechnologycrtdisplay)
- [var cmTechnologyPMDisplay: Int](/documentation/applicationservices/cmtechnologypmdisplay)
- [var cmTechnologyAMDisplay: Int](/documentation/applicationservices/cmtechnologyamdisplay)
- [var cmTechnologyPhotoCD: Int](/documentation/applicationservices/cmtechnologyphotocd)
- [var cmTechnologyPhotoImageSetter: Int](/documentation/applicationservices/cmtechnologyphotoimagesetter)
- [var cmTechnologyGravure: Int](/documentation/applicationservices/cmtechnologygravure)
- [var cmTechnologyOffsetLithography: Int](/documentation/applicationservices/cmtechnologyoffsetlithography)
- [var cmTechnologySilkscreen: Int](/documentation/applicationservices/cmtechnologysilkscreen)
- [var cmTechnologyFlexography: Int](/documentation/applicationservices/cmtechnologyflexography)
- [Use Types](/documentation/applicationservices/colorsync_manager/1560730-use_types)

#### Constants

- [var cmInputUse: Int](/documentation/applicationservices/cminputuse)
- [var cmOutputUse: Int](/documentation/applicationservices/cmoutputuse)
- [var cmDisplayUse: Int](/documentation/applicationservices/cmdisplayuse)
- [var cmProofUse: Int](/documentation/applicationservices/cmproofuse)
- [Video Card Gamma Storage Types](/documentation/applicationservices/colorsync_manager/1560344-video_card_gamma_storage_types)

#### Constants

- [var cmVideoCardGammaTableType: Int](/documentation/applicationservices/cmvideocardgammatabletype)
- [var cmVideoCardGammaFormulaType: Int](/documentation/applicationservices/cmvideocardgammaformulatype)
- [Video Card Gamma Tags](/documentation/applicationservices/colorsync_manager/1560164-video_card_gamma_tags)

#### Constants

- [var cmPS2CRDVMSizeTag: Int](/documentation/applicationservices/cmps2crdvmsizetag)
- [var cmVideoCardGammaTag: Int](/documentation/applicationservices/cmvideocardgammatag)
- [var cmMakeAndModelTag: Int](/documentation/applicationservices/cmmakeandmodeltag)
- [var cmProfileDescriptionMLTag: Int](/documentation/applicationservices/cmprofiledescriptionmltag)
- [var cmNativeDisplayInfoTag: Int](/documentation/applicationservices/cmnativedisplayinfotag)
- [Video Card Gamma Signatures](/documentation/applicationservices/colorsync_manager/1560275-video_card_gamma_signatures)

#### Constants

- [var cmSigPS2CRDVMSizeType: Int](/documentation/applicationservices/cmsigps2crdvmsizetype)
- [var cmSigVideoCardGammaType: Int](/documentation/applicationservices/cmsigvideocardgammatype)
- [var cmSigMakeAndModelType: Int](/documentation/applicationservices/cmsigmakeandmodeltype)
- [var cmSigNativeDisplayInfoType: Int](/documentation/applicationservices/cmsignativedisplayinfotype)
- [var cmSigMultiLocalizedUniCodeType: Int](/documentation/applicationservices/cmsigmultilocalizedunicodetype)

### Result Codes

- [var cmProfileError: Int](/documentation/coreservices/cmprofileerror)
- [var cmMethodError: Int](/documentation/coreservices/cmmethoderror)
- [var cmMethodNotFound: Int](/documentation/coreservices/cmmethodnotfound)
- [var cmProfileNotFound: Int](/documentation/coreservices/cmprofilenotfound)
- [var cmProfilesIdentical: Int](/documentation/coreservices/cmprofilesidentical)
- [var cmCantConcatenateError: Int](/documentation/coreservices/cmcantconcatenateerror)
- [var cmCantXYZ: Int](/documentation/coreservices/cmcantxyz)
- [var cmCantDeleteProfile: Int](/documentation/coreservices/cmcantdeleteprofile)
- [var cmUnsupportedDataType: Int](/documentation/coreservices/cmunsupporteddatatype)
- [var cmNoCurrentProfile: Int](/documentation/coreservices/cmnocurrentprofile)
- [var cmElementTagNotFound: Int](/documentation/coreservices/cmelementtagnotfound)
- [var cmIndexRangeErr: Int](/documentation/coreservices/cmindexrangeerr)
- [var cmCantDeleteElement: Int](/documentation/coreservices/cmcantdeleteelement)
- [var cmFatalProfileErr: Int](/documentation/coreservices/cmfatalprofileerr)
- [var cmInvalidProfile: Int](/documentation/coreservices/cminvalidprofile)
- [var cmInvalidProfileLocation: Int](/documentation/coreservices/cminvalidprofilelocation)
- [var cmInvalidSearch: Int](/documentation/coreservices/cminvalidsearch)
- [var cmSearchError: Int](/documentation/coreservices/cmsearcherror)
- [var cmErrIncompatibleProfile: Int](/documentation/coreservices/cmerrincompatibleprofile)
- [var cmInvalidColorSpace: Int](/documentation/coreservices/cminvalidcolorspace)
- [var cmInvalidSrcMap: Int](/documentation/coreservices/cminvalidsrcmap)
- [var cmInvalidDstMap: Int](/documentation/coreservices/cminvaliddstmap)
- [var cmNoGDevicesError: Int](/documentation/coreservices/cmnogdeviceserror)
- [var cmInvalidProfileComment: Int](/documentation/coreservices/cminvalidprofilecomment)
- [var cmRangeOverFlow: Int](/documentation/coreservices/cmrangeoverflow)
- [var cmCantCopyModifiedV1Profile: Int](/documentation/coreservices/cmcantcopymodifiedv1profile)
- [var cmNamedColorNotFound: Int](/documentation/coreservices/cmnamedcolornotfound)
- [var cmCantGamutCheckError: Int](/documentation/coreservices/cmcantgamutcheckerror)
- [var cmDeviceDBNotFoundErr: Int](/documentation/applicationservices/cmdevicedbnotfounderr)
- [var cmDeviceAlreadyRegistered: Int](/documentation/applicationservices/cmdevicealreadyregistered)
- [var cmDeviceNotRegistered: Int](/documentation/applicationservices/cmdevicenotregistered)
- [var cmDeviceProfilesNotFound: Int](/documentation/applicationservices/cmdeviceprofilesnotfound)
- [var cmInternalCFErr: Int](/documentation/applicationservices/cminternalcferr)
- [Speech Synthesis Manager](/documentation/applicationservices/speech_synthesis_manager)

### Changing Speech Attributes

- [func SetSpeechProperty(SpeechChannel, CFString, CFTypeRef?) -> OSErr](/documentation/applicationservices/1459256-setspeechproperty)
- [func SetSpeechPitch(SpeechChannel, Fixed) -> OSErr](/documentation/applicationservices/1462674-setspeechpitch)
- [func SetSpeechRate(SpeechChannel, Fixed) -> OSErr](/documentation/applicationservices/1459896-setspeechrate)

### Converting Text To Phonemes

- [func CopyPhonemesFromText(SpeechChannel, CFString, UnsafeMutablePointer<CFString?>) -> OSErr](/documentation/applicationservices/1460918-copyphonemesfromtext)

### Installing a Pronunciation Dictionary

- [func UseSpeechDictionary(SpeechChannel, CFDictionary) -> OSErr](/documentation/applicationservices/1463688-usespeechdictionary)

### Managing Speech Channels

- [func DisposeSpeechChannel(SpeechChannel) -> OSErr](/documentation/applicationservices/1462081-disposespeechchannel)
- [func NewSpeechChannel(UnsafeMutablePointer<VoiceSpec>?, UnsafeMutablePointer<SpeechChannel?>) -> OSErr](/documentation/applicationservices/1461367-newspeechchannel)

### Obtaining Information About Speech and Speech Channels

- [func CopySpeechProperty(SpeechChannel, CFString, UnsafeMutablePointer<CFTypeRef?>) -> OSErr](/documentation/applicationservices/1459075-copyspeechproperty)
- [func GetSpeechPitch(SpeechChannel, UnsafeMutablePointer<Fixed>) -> OSErr](/documentation/applicationservices/1464774-getspeechpitch)
- [func GetSpeechRate(SpeechChannel, UnsafeMutablePointer<Fixed>) -> OSErr](/documentation/applicationservices/1460797-getspeechrate)
- [func SpeechBusy() -> Int16](/documentation/applicationservices/1464581-speechbusy)
- [func SpeechBusySystemWide() -> Int16](/documentation/applicationservices/1460113-speechbusysystemwide)
- [func SpeechManagerVersion() -> NumVersion](/documentation/applicationservices/1462334-speechmanagerversion)

### Getting Information About Voices

- [func CountVoices(UnsafeMutablePointer<Int16>) -> OSErr](/documentation/applicationservices/1459947-countvoices)
- [func GetIndVoice(Int16, UnsafeMutablePointer<VoiceSpec>) -> OSErr](/documentation/applicationservices/1464595-getindvoice)
- [func GetVoiceDescription(UnsafePointer<VoiceSpec>?, UnsafeMutablePointer<VoiceDescription>?, Int) -> OSErr](/documentation/applicationservices/1463940-getvoicedescription)
- [func GetVoiceInfo(UnsafePointer<VoiceSpec>?, OSType, UnsafeMutableRawPointer) -> OSErr](/documentation/applicationservices/1461410-getvoiceinfo)
- [func MakeVoiceSpec(OSType, OSType, UnsafeMutablePointer<VoiceSpec>) -> OSErr](/documentation/applicationservices/1461446-makevoicespec)

### Starting, Stopping, and Pausing Speech

- [func ContinueSpeech(SpeechChannel) -> OSErr](/documentation/applicationservices/1462728-continuespeech)
- [func PauseSpeechAt(SpeechChannel, Int32) -> OSErr](/documentation/applicationservices/1461174-pausespeechat)
- [func SpeakCFString(SpeechChannel, CFString, CFDictionary?) -> OSErr](/documentation/applicationservices/1461621-speakcfstring)
- [func StopSpeech(SpeechChannel) -> OSErr](/documentation/applicationservices/1462745-stopspeech)
- [func StopSpeechAt(SpeechChannel, Int32) -> OSErr](/documentation/applicationservices/1459780-stopspeechat)

### Registering and Unregistering Synthesizers and Voices

- [func SpeechSynthesisRegisterModuleURL(CFURL) -> OSErr](/documentation/applicationservices/1459624-speechsynthesisregistermoduleurl)
- [func SpeechSynthesisUnregisterModuleURL(CFURL) -> OSErr](/documentation/applicationservices/1462511-speechsynthesisunregistermoduleu)

### Callbacks

- [SpeechDoneProcPtr](/documentation/applicationservices/speechdoneprocptr)
- [SpeechErrorProcPtr](/documentation/applicationservices/speecherrorprocptr)
- [SpeechErrorCFProcPtr](/documentation/applicationservices/speecherrorcfprocptr)
- [SpeechPhonemeProcPtr](/documentation/applicationservices/speechphonemeprocptr)
- [SpeechSyncProcPtr](/documentation/applicationservices/speechsyncprocptr)
- [SpeechTextDoneProcPtr](/documentation/applicationservices/speechtextdoneprocptr)
- [SpeechWordProcPtr](/documentation/applicationservices/speechwordprocptr)
- [SpeechWordCFProcPtr](/documentation/applicationservices/speechwordcfprocptr)

### Data Types

- [DelimiterInfo](/documentation/applicationservices/delimiterinfo)

#### Initializers

- [init()](/documentation/applicationservices/delimiterinfo/1460927-init)
- [init(startDelimiter: (UInt8, UInt8), endDelimiter: (UInt8, UInt8))](/documentation/applicationservices/delimiterinfo/1464001-init)

#### Instance Properties

- [var endDelimiter: (UInt8, UInt8)](/documentation/applicationservices/delimiterinfo/1462493-enddelimiter)
- [var startDelimiter: (UInt8, UInt8)](/documentation/applicationservices/delimiterinfo/1462284-startdelimiter)
- [PhonemeDescriptor](/documentation/applicationservices/phonemedescriptor)

#### Initializers

- [init()](/documentation/applicationservices/phonemedescriptor/1461428-init)
- [init(phonemeCount: Int16, thePhonemes: PhonemeInfo)](/documentation/applicationservices/phonemedescriptor/1464380-init)

#### Instance Properties

- [var phonemeCount: Int16](/documentation/applicationservices/phonemedescriptor/1463147-phonemecount)
- [var thePhonemes: PhonemeInfo](/documentation/applicationservices/phonemedescriptor/1464118-thephonemes)
- [PhonemeInfo](/documentation/applicationservices/phonemeinfo)

#### Initializers

- [init()](/documentation/applicationservices/phonemeinfo/1461979-init)
- [init(opcode: Int16, phStr: Str15, exampleStr: Str31, hiliteStart: Int16, hiliteEnd: Int16)](/documentation/applicationservices/phonemeinfo/1459158-init)

#### Instance Properties

- [var exampleStr: Str31](/documentation/applicationservices/phonemeinfo/1460341-examplestr)
- [var hiliteEnd: Int16](/documentation/applicationservices/phonemeinfo/1464802-hiliteend)
- [var hiliteStart: Int16](/documentation/applicationservices/phonemeinfo/1464138-hilitestart)
- [var opcode: Int16](/documentation/applicationservices/phonemeinfo/1459025-opcode)
- [var phStr: Str15](/documentation/applicationservices/phonemeinfo/1461253-phstr)
- [SpeechChannelRecord](/documentation/applicationservices/speechchannelrecord)

#### Initializers

- [init()](/documentation/applicationservices/speechchannelrecord/1461764-init)
- [init(data: Int)](/documentation/applicationservices/speechchannelrecord/1459019-init)

#### Instance Properties

- [var data: Int](/documentation/applicationservices/speechchannelrecord/1460355-data)
- [SpeechChannel](/documentation/applicationservices/speechchannel)
- [SpeechDoneUPP](/documentation/applicationservices/speechdoneupp)
- [SpeechErrorInfo](/documentation/applicationservices/speecherrorinfo)

#### Initializers

- [init()](/documentation/applicationservices/speecherrorinfo/1463016-init)
- [init(count: Int16, oldest: OSErr, oldPos: Int, newest: OSErr, newPos: Int)](/documentation/applicationservices/speecherrorinfo/1464795-init)

#### Instance Properties

- [var count: Int16](/documentation/applicationservices/speecherrorinfo/1459251-count)
- [var newPos: Int](/documentation/applicationservices/speecherrorinfo/1464494-newpos)
- [var newest: OSErr](/documentation/applicationservices/speecherrorinfo/1461434-newest)
- [var oldPos: Int](/documentation/applicationservices/speecherrorinfo/1460065-oldpos)
- [var oldest: OSErr](/documentation/applicationservices/speecherrorinfo/1463962-oldest)
- [SpeechErrorUPP](/documentation/applicationservices/speecherrorupp)
- [SpeechPhonemeUPP](/documentation/applicationservices/speechphonemeupp)
- [SpeechStatusInfo](/documentation/applicationservices/speechstatusinfo)

#### Initializers

- [init()](/documentation/applicationservices/speechstatusinfo/1463999-init)
- [init(outputBusy: DarwinBoolean, outputPaused: DarwinBoolean, inputBytesLeft: Int, phonemeCode: Int16)](/documentation/applicationservices/speechstatusinfo/1463725-init)

#### Instance Properties

- [var inputBytesLeft: Int](/documentation/applicationservices/speechstatusinfo/1461214-inputbytesleft)
- [var outputBusy: DarwinBoolean](/documentation/applicationservices/speechstatusinfo/1459111-outputbusy)
- [var outputPaused: DarwinBoolean](/documentation/applicationservices/speechstatusinfo/1460606-outputpaused)
- [var phonemeCode: Int16](/documentation/applicationservices/speechstatusinfo/1461423-phonemecode)
- [SpeechSyncUPP](/documentation/applicationservices/speechsyncupp)
- [SpeechTextDoneUPP](/documentation/applicationservices/speechtextdoneupp)
- [SpeechVersionInfo](/documentation/applicationservices/speechversioninfo)

#### Initializers

- [init()](/documentation/applicationservices/speechversioninfo/1462191-init)
- [init(synthType: OSType, synthSubType: OSType, synthManufacturer: OSType, synthFlags: Int32, synthVersion: NumVersion)](/documentation/applicationservices/speechversioninfo/1458819-init)

#### Instance Properties

- [var synthFlags: Int32](/documentation/applicationservices/speechversioninfo/1464789-synthflags)
- [var synthManufacturer: OSType](/documentation/applicationservices/speechversioninfo/1458822-synthmanufacturer)
- [var synthSubType: OSType](/documentation/applicationservices/speechversioninfo/1460351-synthsubtype)
- [var synthType: OSType](/documentation/applicationservices/speechversioninfo/1459500-synthtype)
- [var synthVersion: NumVersion](/documentation/applicationservices/speechversioninfo/1459222-synthversion)
- [SpeechWordUPP](/documentation/applicationservices/speechwordupp)
- [SpeechXtndData](/documentation/applicationservices/speechxtnddata)

#### Initializers

- [init()](/documentation/applicationservices/speechxtnddata/1459302-init)
- [init(synthCreator: OSType, synthData: (UInt8, UInt8))](/documentation/applicationservices/speechxtnddata/1461482-init)

#### Instance Properties

- [var synthCreator: OSType](/documentation/applicationservices/speechxtnddata/1462619-synthcreator)
- [var synthData: (UInt8, UInt8)](/documentation/applicationservices/speechxtnddata/1459201-synthdata)
- [VoiceDescription](/documentation/applicationservices/voicedescription)

#### Initializers

- [init()](/documentation/applicationservices/voicedescription/1460513-init)
- [init(length: Int32, voice: VoiceSpec, version: Int32, name: Str63, comment: Str255, gender: Int16, age: Int16, script: Int16, language: Int16, region: Int16, reserved: (Int32, Int32, Int32, Int32))](/documentation/applicationservices/voicedescription/1463154-init)

#### Instance Properties

- [var age: Int16](/documentation/applicationservices/voicedescription/1462733-age)
- [var comment: Str255](/documentation/applicationservices/voicedescription/1461098-comment)
- [var gender: Int16](/documentation/applicationservices/voicedescription/1460238-gender)
- [var language: Int16](/documentation/applicationservices/voicedescription/1464160-language)
- [var length: Int32](/documentation/applicationservices/voicedescription/1463606-length)
- [var name: Str63](/documentation/applicationservices/voicedescription/1459756-name)
- [var region: Int16](/documentation/applicationservices/voicedescription/1462975-region)
- [var reserved: (Int32, Int32, Int32, Int32)](/documentation/applicationservices/voicedescription/1462772-reserved)
- [var script: Int16](/documentation/applicationservices/voicedescription/1461925-script)
- [var version: Int32](/documentation/applicationservices/voicedescription/1464717-version)
- [var voice: VoiceSpec](/documentation/applicationservices/voicedescription/1462456-voice)
- [VoiceFileInfo](/documentation/applicationservices/voicefileinfo)

#### Initializers

- [init()](/documentation/applicationservices/voicefileinfo/1464655-init)
- [init(fileSpec: FSSpec, resID: Int16)](/documentation/applicationservices/voicefileinfo/1460648-init)

#### Instance Properties

- [var fileSpec: FSSpec](/documentation/applicationservices/voicefileinfo/1460824-filespec)
- [var resID: Int16](/documentation/applicationservices/voicefileinfo/1462134-resid)
- [VoiceSpec](/documentation/applicationservices/voicespec)

#### Initializers

- [init()](/documentation/applicationservices/voicespec/1461864-init)
- [init(creator: OSType, id: OSType)](/documentation/applicationservices/voicespec/1459363-init)

#### Instance Properties

- [var creator: OSType](/documentation/applicationservices/voicespec/1461398-creator)
- [var id: OSType](/documentation/applicationservices/voicespec/1464319-id)

### Constants

- [Control Flags Constants](/documentation/applicationservices/speech_synthesis_manager/1552213-control_flags_constants)

#### Constants

- [var kNoEndingProsody: Int32](/documentation/applicationservices/knoendingprosody)
- [var kNoSpeechInterrupt: Int32](/documentation/applicationservices/knospeechinterrupt)
- [var kPreflightThenPause: Int32](/documentation/applicationservices/kpreflightthenpause)
- [Gender Constants](/documentation/applicationservices/speech_synthesis_manager/1552246-gender_constants)

#### Constants

- [var kNeuter: Int16](/documentation/applicationservices/kneuter)
- [var kMale: Int16](/documentation/applicationservices/kmale)
- [var kFemale: Int16](/documentation/applicationservices/kfemale)
- [Audio Unit Constants](/documentation/applicationservices/speech_synthesis_manager/1552263-audio_unit_constants)

#### Constants

- [var kAudioUnitSubType_SpeechSynthesis: UInt32](/documentation/applicationservices/kaudiounitsubtype_speechsynthesis)
- [var kAudioUnitProperty_Voice: UInt32](/documentation/applicationservices/kaudiounitproperty_voice)
- [var kAudioUnitProperty_SpeechChannel: UInt32](/documentation/applicationservices/kaudiounitproperty_speechchannel)
- [Stop Speech Locations](/documentation/applicationservices/speech_synthesis_manager/1552264-stop_speech_locations)

#### Constants

- [var kImmediate: Int32](/documentation/applicationservices/kimmediate)
- [var kEndOfWord: Int32](/documentation/applicationservices/kendofword)
- [var kEndOfSentence: Int32](/documentation/applicationservices/kendofsentence)
- [Speech Synthesis Manager Operating System Types](/documentation/applicationservices/speech_synthesis_manager/1552231-speech_synthesis_manager_operati)

#### Constants

- [var kTextToSpeechSynthType: OSType](/documentation/applicationservices/ktexttospeechsynthtype)
- [var kTextToSpeechVoiceType: OSType](/documentation/applicationservices/ktexttospeechvoicetype)
- [var kTextToSpeechVoiceFileType: OSType](/documentation/applicationservices/ktexttospeechvoicefiletype)
- [var kTextToSpeechVoiceBundleType: OSType](/documentation/applicationservices/ktexttospeechvoicebundletype)
- [Speech-Channel Modes](/documentation/applicationservices/speech_synthesis_manager/1552256-speech-channel_modes)

#### Constants

- [var modeText: OSType](/documentation/applicationservices/modetext)
- [var modePhonemes: OSType](/documentation/applicationservices/modephonemes)
- [var modeNormal: OSType](/documentation/applicationservices/modenormal)
- [var modeLiteral: OSType](/documentation/applicationservices/modeliteral)
- [var modeTune: OSType](/documentation/applicationservices/modetune)
- [Speech-Channel Modes for Core Foundation-based Functions](/documentation/applicationservices/speech_synthesis_manager/speech-channel_modes_for_core_foundation-based_functions)

#### Constants

- [let kSpeechModeText: CFString](/documentation/applicationservices/kspeechmodetext)
- [let kSpeechModePhoneme: CFString](/documentation/applicationservices/kspeechmodephoneme)
- [let kSpeechModeNormal: CFString](/documentation/applicationservices/kspeechmodenormal)
- [let kSpeechModeLiteral: CFString](/documentation/applicationservices/kspeechmodeliteral)
- [Voice Information Selectors](/documentation/applicationservices/speech_synthesis_manager/1552254-voice_information_selectors)

#### Constants

- [var soVoiceDescription: OSType](/documentation/applicationservices/sovoicedescription)
- [var soVoiceFile: OSType](/documentation/applicationservices/sovoicefile)
- [Speech-Channel Information Constants](/documentation/applicationservices/speech_synthesis_manager/1552228-speech-channel_information_constants)

#### Constants

- [var soStatus: OSType](/documentation/applicationservices/sostatus)
- [var soErrors: OSType](/documentation/applicationservices/soerrors)
- [var soInputMode: OSType](/documentation/applicationservices/soinputmode)
- [var soCharacterMode: OSType](/documentation/applicationservices/socharactermode)
- [var soNumberMode: OSType](/documentation/applicationservices/sonumbermode)
- [var soRate: OSType](/documentation/applicationservices/sorate)
- [var soPitchBase: OSType](/documentation/applicationservices/sopitchbase)
- [var soPitchMod: OSType](/documentation/applicationservices/sopitchmod)
- [var soVolume: OSType](/documentation/applicationservices/sovolume)
- [var soSynthType: OSType](/documentation/applicationservices/sosynthtype)
- [var soRecentSync: OSType](/documentation/applicationservices/sorecentsync)
- [var soPhonemeSymbols: OSType](/documentation/applicationservices/sophonemesymbols)
- [var soCurrentVoice: OSType](/documentation/applicationservices/socurrentvoice)
- [var soCommandDelimiter: OSType](/documentation/applicationservices/socommanddelimiter)
- [var soReset: OSType](/documentation/applicationservices/soreset)
- [var soCurrentA5: OSType](/documentation/applicationservices/socurrenta5)
- [var soRefCon: OSType](/documentation/applicationservices/sorefcon)
- [var soTextDoneCallBack: OSType](/documentation/applicationservices/sotextdonecallback)
- [var soSpeechDoneCallBack: OSType](/documentation/applicationservices/sospeechdonecallback)
- [var soSyncCallBack: OSType](/documentation/applicationservices/sosynccallback)
- [var soErrorCallBack: OSType](/documentation/applicationservices/soerrorcallback)
- [var soPhonemeCallBack: OSType](/documentation/applicationservices/sophonemecallback)
- [var soWordCallBack: OSType](/documentation/applicationservices/sowordcallback)
- [var soSynthExtension: OSType](/documentation/applicationservices/sosynthextension)
- [var soSoundOutput: OSType](/documentation/applicationservices/sosoundoutput)
- [var soOutputToFileWithCFURL: OSType](/documentation/applicationservices/sooutputtofilewithcfurl)
- [var soOutputToExtAudioFile: OSType](/documentation/applicationservices/sooutputtoextaudiofile)
- [var soPhonemeOptions: OSType](/documentation/applicationservices/sophonemeoptions)
- [var soOutputToAudioDevice: OSType](/documentation/applicationservices/sooutputtoaudiodevice)
- [Phoneme Generation Options](/documentation/applicationservices/speech_synthesis_manager/1552233-phoneme_generation_options)

#### Constants

- [var kSpeechGenerateTune: Int32](/documentation/applicationservices/kspeechgeneratetune)
- [var kSpeechRelativePitch: Int32](/documentation/applicationservices/kspeechrelativepitch)
- [var kSpeechRelativeDuration: Int32](/documentation/applicationservices/kspeechrelativeduration)
- [var kSpeechShowSyllables: Int32](/documentation/applicationservices/kspeechshowsyllables)
- [Speech-Channel Properties](/documentation/applicationservices/speech_synthesis_manager/speech-channel_properties)

#### Constants

- [let kSpeechStatusProperty: CFString](/documentation/applicationservices/kspeechstatusproperty)
- [let kSpeechErrorsProperty: CFString](/documentation/applicationservices/kspeecherrorsproperty)
- [let kSpeechInputModeProperty: CFString](/documentation/applicationservices/kspeechinputmodeproperty)
- [let kSpeechCharacterModeProperty: CFString](/documentation/applicationservices/kspeechcharactermodeproperty)
- [let kSpeechNumberModeProperty: CFString](/documentation/applicationservices/kspeechnumbermodeproperty)
- [let kSpeechRateProperty: CFString](/documentation/applicationservices/kspeechrateproperty)
- [let kSpeechPitchBaseProperty: CFString](/documentation/applicationservices/kspeechpitchbaseproperty)
- [let kSpeechPitchModProperty: CFString](/documentation/applicationservices/kspeechpitchmodproperty)
- [let kSpeechVolumeProperty: CFString](/documentation/applicationservices/kspeechvolumeproperty)
- [let kSpeechSynthesizerInfoProperty: CFString](/documentation/applicationservices/kspeechsynthesizerinfoproperty)
- [let kSpeechRecentSyncProperty: CFString](/documentation/applicationservices/kspeechrecentsyncproperty)
- [let kSpeechPhonemeSymbolsProperty: CFString](/documentation/applicationservices/kspeechphonemesymbolsproperty)
- [let kSpeechCurrentVoiceProperty: CFString](/documentation/applicationservices/kspeechcurrentvoiceproperty)
- [let kSpeechCommandDelimiterProperty: CFString](/documentation/applicationservices/kspeechcommanddelimiterproperty)
- [let kSpeechResetProperty: CFString](/documentation/applicationservices/kspeechresetproperty)
- [let kSpeechOutputToFileURLProperty: CFString](/documentation/applicationservices/kspeechoutputtofileurlproperty)
- [let kSpeechOutputToExtAudioFileProperty: CFString](/documentation/applicationservices/kspeechoutputtoextaudiofileproperty)
- [let kSpeechRefConProperty: CFString](/documentation/applicationservices/kspeechrefconproperty)
- [let kSpeechTextDoneCallBack: CFString](/documentation/applicationservices/kspeechtextdonecallback)
- [let kSpeechSpeechDoneCallBack: CFString](/documentation/applicationservices/kspeechspeechdonecallback)
- [let kSpeechSyncCallBack: CFString](/documentation/applicationservices/kspeechsynccallback)
- [let kSpeechPhonemeCallBack: CFString](/documentation/applicationservices/kspeechphonemecallback)
- [let kSpeechErrorCFCallBack: CFString](/documentation/applicationservices/kspeecherrorcfcallback)
- [let kSpeechWordCFCallBack: CFString](/documentation/applicationservices/kspeechwordcfcallback)
- [let kSpeechPhonemeOptionsProperty: CFString](/documentation/applicationservices/kspeechphonemeoptionsproperty)
- [let kSpeechOutputToAudioDeviceProperty: CFString](/documentation/applicationservices/kspeechoutputtoaudiodeviceproperty)
- [Synthesizer Option Keys](/documentation/applicationservices/speech_synthesis_manager/synthesizer_option_keys)

#### Constants

- [let kSpeechNoEndingProsody: CFString](/documentation/applicationservices/kspeechnoendingprosody)
- [let kSpeechNoSpeechInterrupt: CFString](/documentation/applicationservices/kspeechnospeechinterrupt)
- [let kSpeechPreflightThenPause: CFString](/documentation/applicationservices/kspeechpreflightthenpause)
- [Speech Status Keys](/documentation/applicationservices/speech_synthesis_manager/speech_status_keys)

#### Constants

- [let kSpeechStatusOutputBusy: CFString](/documentation/applicationservices/kspeechstatusoutputbusy)
- [let kSpeechStatusOutputPaused: CFString](/documentation/applicationservices/kspeechstatusoutputpaused)
- [let kSpeechStatusNumberOfCharactersLeft: CFString](/documentation/applicationservices/kspeechstatusnumberofcharactersleft)
- [let kSpeechStatusPhonemeCode: CFString](/documentation/applicationservices/kspeechstatusphonemecode)
- [Speech Error Keys](/documentation/applicationservices/speech_synthesis_manager/speech_error_keys)

#### Constants

- [let kSpeechErrorCount: CFString](/documentation/applicationservices/kspeecherrorcount)
- [let kSpeechErrorOldest: CFString](/documentation/applicationservices/kspeecherroroldest)
- [let kSpeechErrorOldestCharacterOffset: CFString](/documentation/applicationservices/kspeecherroroldestcharacteroffset)
- [let kSpeechErrorNewest: CFString](/documentation/applicationservices/kspeecherrornewest)
- [let kSpeechErrorNewestCharacterOffset: CFString](/documentation/applicationservices/kspeecherrornewestcharacteroffset)
- [Speech Synthesizer Information Keys](/documentation/applicationservices/speech_synthesis_manager/speech_synthesizer_information_keys)

#### Constants

- [let kSpeechSynthesizerInfoIdentifier: CFString](/documentation/applicationservices/kspeechsynthesizerinfoidentifier)
- [let kSpeechSynthesizerInfoVersion: CFString](/documentation/applicationservices/kspeechsynthesizerinfoversion)
- [let kSpeechSynthesizerInfoManufacturer: CFString](/documentation/applicationservices/kspeechsynthesizerinfomanufacturer)
- [Phoneme Symbols Keys](/documentation/applicationservices/speech_synthesis_manager/phoneme_symbols_keys)

#### Constants

- [let kSpeechPhonemeInfoOpcode: CFString](/documentation/applicationservices/kspeechphonemeinfoopcode)
- [let kSpeechPhonemeInfoSymbol: CFString](/documentation/applicationservices/kspeechphonemeinfosymbol)
- [let kSpeechPhonemeInfoExample: CFString](/documentation/applicationservices/kspeechphonemeinfoexample)
- [let kSpeechPhonemeInfoHiliteStart: CFString](/documentation/applicationservices/kspeechphonemeinfohilitestart)
- [let kSpeechPhonemeInfoHiliteEnd: CFString](/documentation/applicationservices/kspeechphonemeinfohiliteend)
- [Current Voice Keys](/documentation/applicationservices/speech_synthesis_manager/current_voice_keys)

#### Constants

- [let kSpeechVoiceCreator: CFString](/documentation/applicationservices/kspeechvoicecreator)
- [let kSpeechVoiceID: CFString](/documentation/applicationservices/kspeechvoiceid)
- [Command Delimiter Keys](/documentation/applicationservices/speech_synthesis_manager/command_delimiter_keys)

#### Constants

- [let kSpeechCommandPrefix: CFString](/documentation/applicationservices/kspeechcommandprefix)
- [let kSpeechCommandSuffix: CFString](/documentation/applicationservices/kspeechcommandsuffix)
- [Speech Dictionary Keys](/documentation/applicationservices/speech_synthesis_manager/speech_dictionary_keys)

#### Constants

- [let kSpeechDictionaryLocaleIdentifier: CFString](/documentation/applicationservices/kspeechdictionarylocaleidentifier)
- [let kSpeechDictionaryModificationDate: CFString](/documentation/applicationservices/kspeechdictionarymodificationdate)
- [let kSpeechDictionaryPronunciations: CFString](/documentation/applicationservices/kspeechdictionarypronunciations)
- [let kSpeechDictionaryAbbreviations: CFString](/documentation/applicationservices/kspeechdictionaryabbreviations)
- [let kSpeechDictionaryEntrySpelling: CFString](/documentation/applicationservices/kspeechdictionaryentryspelling)
- [let kSpeechDictionaryEntryPhonemes: CFString](/documentation/applicationservices/kspeechdictionaryentryphonemes)
- [Error Callback User-Information String](/documentation/applicationservices/speech_synthesis_manager/error_callback_user-information_string)

#### Constants

- [let kSpeechErrorCallbackSpokenString: CFString](/documentation/applicationservices/kspeecherrorcallbackspokenstring)
- [let kSpeechErrorCallbackCharacterOffset: CFString](/documentation/applicationservices/kspeecherrorcallbackcharacteroffset)

### Result Codes

- [var noSynthFound: Int](/documentation/coreservices/nosynthfound)
- [var synthOpenFailed: Int](/documentation/coreservices/synthopenfailed)
- [var synthNotReady: Int](/documentation/coreservices/synthnotready)
- [var bufTooSmall: Int](/documentation/coreservices/buftoosmall)
- [var voiceNotFound: Int](/documentation/coreservices/voicenotfound)
- [var incompatibleVoice: Int](/documentation/coreservices/incompatiblevoice)
- [var badDictFormat: Int](/documentation/coreservices/baddictformat)
- [var badInputText: Int](/documentation/coreservices/badinputtext)

## Reference

- [Carbon Accessibility](/documentation/applicationservices/carbon_accessibility)

### Accessibility Events

- [Accessibility Event Class](/documentation/applicationservices/carbon_accessibility/accessibility_event_class)

### Accessibility Object Constants

- [Roles](/documentation/applicationservices/carbon_accessibility/roles)

#### Constants

- [var kAXApplicationRole: String](/documentation/applicationservices/kaxapplicationrole)
- [var kAXSystemWideRole: String](/documentation/applicationservices/kaxsystemwiderole)
- [var kAXWindowRole: String](/documentation/applicationservices/kaxwindowrole)
- [var kAXSheetRole: String](/documentation/applicationservices/kaxsheetrole)
- [var kAXDrawerRole: String](/documentation/applicationservices/kaxdrawerrole)
- [var kAXGrowAreaRole: String](/documentation/applicationservices/kaxgrowarearole)
- [var kAXImageRole: String](/documentation/applicationservices/kaximagerole)
- [var kAXUnknownRole: String](/documentation/applicationservices/kaxunknownrole)
- [var kAXButtonRole: String](/documentation/applicationservices/kaxbuttonrole)
- [var kAXRadioButtonRole: String](/documentation/applicationservices/kaxradiobuttonrole)
- [var kAXCheckBoxRole: String](/documentation/applicationservices/kaxcheckboxrole)
- [var kAXPopUpButtonRole: String](/documentation/applicationservices/kaxpopupbuttonrole)
- [var kAXMenuButtonRole: String](/documentation/applicationservices/kaxmenubuttonrole)
- [var kAXTabGroupRole: String](/documentation/applicationservices/kaxtabgrouprole)
- [var kAXTableRole: String](/documentation/applicationservices/kaxtablerole)
- [var kAXColumnRole: String](/documentation/applicationservices/kaxcolumnrole)
- [var kAXRowRole: String](/documentation/applicationservices/kaxrowrole)
- [var kAXOutlineRole: String](/documentation/applicationservices/kaxoutlinerole)
- [var kAXBrowserRole: String](/documentation/applicationservices/kaxbrowserrole)
- [var kAXScrollAreaRole: String](/documentation/applicationservices/kaxscrollarearole)
- [var kAXScrollBarRole: String](/documentation/applicationservices/kaxscrollbarrole)
- [var kAXRadioGroupRole: String](/documentation/applicationservices/kaxradiogrouprole)
- [var kAXListRole: String](/documentation/applicationservices/kaxlistrole)
- [var kAXGroupRole: String](/documentation/applicationservices/kaxgrouprole)
- [var kAXValueIndicatorRole: String](/documentation/applicationservices/kaxvalueindicatorrole)
- [var kAXComboBoxRole: String](/documentation/applicationservices/kaxcomboboxrole)
- [var kAXSliderRole: String](/documentation/applicationservices/kaxsliderrole)
- [var kAXIncrementorRole: String](/documentation/applicationservices/kaxincrementorrole)
- [var kAXBusyIndicatorRole: String](/documentation/applicationservices/kaxbusyindicatorrole)
- [var kAXProgressIndicatorRole: String](/documentation/applicationservices/kaxprogressindicatorrole)
- [var kAXRelevanceIndicatorRole: String](/documentation/applicationservices/kaxrelevanceindicatorrole)
- [var kAXToolbarRole: String](/documentation/applicationservices/kaxtoolbarrole)
- [var kAXDisclosureTriangleRole: String](/documentation/applicationservices/kaxdisclosuretrianglerole)
- [var kAXTextFieldRole: String](/documentation/applicationservices/kaxtextfieldrole)
- [var kAXTextAreaRole: String](/documentation/applicationservices/kaxtextarearole)
- [var kAXStaticTextRole: String](/documentation/applicationservices/kaxstatictextrole)
- [var kAXMenuBarRole: String](/documentation/applicationservices/kaxmenubarrole)
- [var kAXMenuBarItemRole: String](/documentation/applicationservices/kaxmenubaritemrole)
- [var kAXMenuRole: String](/documentation/applicationservices/kaxmenurole)
- [var kAXMenuItemRole: String](/documentation/applicationservices/kaxmenuitemrole)
- [var kAXSplitGroupRole: String](/documentation/applicationservices/kaxsplitgrouprole)
- [var kAXSplitterRole: String](/documentation/applicationservices/kaxsplitterrole)
- [var kAXColorWellRole: String](/documentation/applicationservices/kaxcolorwellrole)
- [var kAXTimeFieldRole: String](/documentation/applicationservices/kaxtimefieldrole)
- [var kAXDateFieldRole: String](/documentation/applicationservices/kaxdatefieldrole)
- [var kAXHelpTagRole: String](/documentation/applicationservices/kaxhelptagrole)
- [var kAXMatteRole: String](/documentation/applicationservices/kaxmatterole)
- [var kAXDockItemRole: String](/documentation/applicationservices/kaxdockitemrole)
- [Subroles](/documentation/applicationservices/carbon_accessibility/subroles)

#### Constants

- [var kAXCloseButtonSubrole: String](/documentation/applicationservices/kaxclosebuttonsubrole)
- [var kAXMinimizeButtonSubrole: String](/documentation/applicationservices/kaxminimizebuttonsubrole)
- [var kAXZoomButtonSubrole: String](/documentation/applicationservices/kaxzoombuttonsubrole)
- [var kAXToolbarButtonSubrole: String](/documentation/applicationservices/kaxtoolbarbuttonsubrole)
- [var kAXSecureTextFieldSubrole: String](/documentation/applicationservices/kaxsecuretextfieldsubrole)
- [var kAXTableRowSubrole: String](/documentation/applicationservices/kaxtablerowsubrole)
- [var kAXOutlineRowSubrole: String](/documentation/applicationservices/kaxoutlinerowsubrole)
- [var kAXUnknownSubrole: String](/documentation/applicationservices/kaxunknownsubrole)
- [var kAXStandardWindowSubrole: String](/documentation/applicationservices/kaxstandardwindowsubrole)
- [var kAXDialogSubrole: String](/documentation/applicationservices/kaxdialogsubrole)
- [var kAXSystemDialogSubrole: String](/documentation/applicationservices/kaxsystemdialogsubrole)
- [var kAXFloatingWindowSubrole: String](/documentation/applicationservices/kaxfloatingwindowsubrole)
- [var kAXSystemFloatingWindowSubrole: String](/documentation/applicationservices/kaxsystemfloatingwindowsubrole)
- [var kAXIncrementArrowSubrole: String](/documentation/applicationservices/kaxincrementarrowsubrole)
- [var kAXDecrementArrowSubrole: String](/documentation/applicationservices/kaxdecrementarrowsubrole)
- [var kAXIncrementPageSubrole: String](/documentation/applicationservices/kaxincrementpagesubrole)
- [var kAXDecrementPageSubrole: String](/documentation/applicationservices/kaxdecrementpagesubrole)
- [var kAXSortButtonSubrole: String](/documentation/applicationservices/kaxsortbuttonsubrole)
- [var kAXSearchFieldSubrole: String](/documentation/applicationservices/kaxsearchfieldsubrole)
- [var kAXApplicationDockItemSubrole: String](/documentation/applicationservices/kaxapplicationdockitemsubrole)
- [var kAXDocumentDockItemSubrole: String](/documentation/applicationservices/kaxdocumentdockitemsubrole)
- [var kAXFolderDockItemSubrole: String](/documentation/applicationservices/kaxfolderdockitemsubrole)
- [var kAXMinimizedWindowDockItemSubrole: String](/documentation/applicationservices/kaxminimizedwindowdockitemsubrole)
- [var kAXURLDockItemSubrole: String](/documentation/applicationservices/kaxurldockitemsubrole)
- [var kAXDockExtraDockItemSubrole: String](/documentation/applicationservices/kaxdockextradockitemsubrole)
- [var kAXTrashDockItemSubrole: String](/documentation/applicationservices/kaxtrashdockitemsubrole)
- [var kAXProcessSwitcherListSubrole: String](/documentation/applicationservices/kaxprocessswitcherlistsubrole)
- [Attributes](/documentation/applicationservices/carbon_accessibility/attributes)

#### Constants

- [var kAXRoleAttribute: String](/documentation/applicationservices/kaxroleattribute)
- [var kAXSubroleAttribute: String](/documentation/applicationservices/kaxsubroleattribute)
- [var kAXRoleDescriptionAttribute: String](/documentation/applicationservices/kaxroledescriptionattribute)
- [var kAXHelpAttribute: String](/documentation/applicationservices/kaxhelpattribute)
- [var kAXTitleAttribute: String](/documentation/applicationservices/kaxtitleattribute)
- [var kAXValueAttribute: String](/documentation/applicationservices/kaxvalueattribute)
- [var kAXMinValueAttribute: String](/documentation/applicationservices/kaxminvalueattribute)
- [var kAXMaxValueAttribute: String](/documentation/applicationservices/kaxmaxvalueattribute)
- [var kAXValueIncrementAttribute: String](/documentation/applicationservices/kaxvalueincrementattribute)
- [var kAXAllowedValuesAttribute: String](/documentation/applicationservices/kaxallowedvaluesattribute)
- [var kAXEnabledAttribute: String](/documentation/applicationservices/kaxenabledattribute)
- [var kAXFocusedAttribute: String](/documentation/applicationservices/kaxfocusedattribute)
- [var kAXParentAttribute: String](/documentation/applicationservices/kaxparentattribute)
- [var kAXChildrenAttribute: String](/documentation/applicationservices/kaxchildrenattribute)
- [var kAXSelectedChildrenAttribute: String](/documentation/applicationservices/kaxselectedchildrenattribute)
- [var kAXVisibleChildrenAttribute: String](/documentation/applicationservices/kaxvisiblechildrenattribute)
- [var kAXWindowAttribute: String](/documentation/applicationservices/kaxwindowattribute)
- [var kAXPositionAttribute: String](/documentation/applicationservices/kaxpositionattribute)
- [var kAXTopLevelUIElementAttribute: String](/documentation/applicationservices/kaxtopleveluielementattribute)
- [var kAXSizeAttribute: String](/documentation/applicationservices/kaxsizeattribute)
- [var kAXOrientationAttribute: String](/documentation/applicationservices/kaxorientationattribute)
- [var kAXDescriptionAttribute: String](/documentation/applicationservices/kaxdescriptionattribute)
- [var kAXSelectedTextAttribute: String](/documentation/applicationservices/kaxselectedtextattribute)
- [var kAXSelectedTextRangeAttribute: String](/documentation/applicationservices/kaxselectedtextrangeattribute)
- [var kAXVisibleCharacterRangeAttribute: String](/documentation/applicationservices/kaxvisiblecharacterrangeattribute)
- [var kAXNumberOfCharactersAttribute: String](/documentation/applicationservices/kaxnumberofcharactersattribute)
- [var kAXSharedTextUIElementsAttribute: String](/documentation/applicationservices/kaxsharedtextuielementsattribute)
- [var kAXSharedCharacterRangeAttribute: String](/documentation/applicationservices/kaxsharedcharacterrangeattribute)
- [var kAXMainAttribute: String](/documentation/applicationservices/kaxmainattribute)
- [var kAXMinimizedAttribute: String](/documentation/applicationservices/kaxminimizedattribute)
- [var kAXCloseButtonAttribute: String](/documentation/applicationservices/kaxclosebuttonattribute)
- [var kAXZoomButtonAttribute: String](/documentation/applicationservices/kaxzoombuttonattribute)
- [var kAXMinimizeButtonAttribute: String](/documentation/applicationservices/kaxminimizebuttonattribute)
- [var kAXToolbarButtonAttribute: String](/documentation/applicationservices/kaxtoolbarbuttonattribute)
- [var kAXGrowAreaAttribute: String](/documentation/applicationservices/kaxgrowareaattribute)
- [var kAXProxyAttribute: String](/documentation/applicationservices/kaxproxyattribute)
- [var kAXModalAttribute: String](/documentation/applicationservices/kaxmodalattribute)
- [var kAXDefaultButtonAttribute: String](/documentation/applicationservices/kaxdefaultbuttonattribute)
- [var kAXCancelButtonAttribute: String](/documentation/applicationservices/kaxcancelbuttonattribute)
- [var kAXMenuItemCmdCharAttribute: String](/documentation/applicationservices/kaxmenuitemcmdcharattribute)
- [var kAXMenuItemCmdVirtualKeyAttribute: String](/documentation/applicationservices/kaxmenuitemcmdvirtualkeyattribute)
- [var kAXMenuItemCmdGlyphAttribute: String](/documentation/applicationservices/kaxmenuitemcmdglyphattribute)
- [var kAXMenuItemCmdModifiersAttribute: String](/documentation/applicationservices/kaxmenuitemcmdmodifiersattribute)
- [var kAXMenuItemMarkCharAttribute: String](/documentation/applicationservices/kaxmenuitemmarkcharattribute)
- [var kAXMenuItemPrimaryUIElementAttribute: String](/documentation/applicationservices/kaxmenuitemprimaryuielementattribute)
- [var kAXMenuBarAttribute: String](/documentation/applicationservices/kaxmenubarattribute)
- [var kAXWindowsAttribute: String](/documentation/applicationservices/kaxwindowsattribute)
- [var kAXFrontmostAttribute: String](/documentation/applicationservices/kaxfrontmostattribute)
- [var kAXHiddenAttribute: String](/documentation/applicationservices/kaxhiddenattribute)
- [var kAXMainWindowAttribute: String](/documentation/applicationservices/kaxmainwindowattribute)
- [var kAXFocusedWindowAttribute: String](/documentation/applicationservices/kaxfocusedwindowattribute)
- [var kAXHeaderAttribute: String](/documentation/applicationservices/kaxheaderattribute)
- [var kAXEditedAttribute: String](/documentation/applicationservices/kaxeditedattribute)
- [var kAXTitleUIElementAttribute: String](/documentation/applicationservices/kaxtitleuielementattribute)
- [var kAXValueWrapsAttribute: String](/documentation/applicationservices/kaxvaluewrapsattribute)
- [var kAXTabsAttribute: String](/documentation/applicationservices/kaxtabsattribute)
- [var kAXHorizontalScrollBarAttribute: String](/documentation/applicationservices/kaxhorizontalscrollbarattribute)
- [var kAXVerticalScrollBarAttribute: String](/documentation/applicationservices/kaxverticalscrollbarattribute)
- [var kAXOverflowButtonAttribute: String](/documentation/applicationservices/kaxoverflowbuttonattribute)
- [var kAXFilenameAttribute: String](/documentation/applicationservices/kaxfilenameattribute)
- [var kAXExpandedAttribute: String](/documentation/applicationservices/kaxexpandedattribute)
- [var kAXSelectedAttribute: String](/documentation/applicationservices/kaxselectedattribute)
- [var kAXSplittersAttribute: String](/documentation/applicationservices/kaxsplittersattribute)
- [var kAXNextContentsAttribute: String](/documentation/applicationservices/kaxnextcontentsattribute)
- [var kAXPreviousContentsAttribute: String](/documentation/applicationservices/kaxpreviouscontentsattribute)
- [var kAXDocumentAttribute: String](/documentation/applicationservices/kaxdocumentattribute)
- [var kAXIncrementButtonAttribute: String](/documentation/applicationservices/kaxincrementbuttonattribute)
- [var kAXDecrementButtonAttribute: String](/documentation/applicationservices/kaxdecrementbuttonattribute)
- [var kAXContentsAttribute: String](/documentation/applicationservices/kaxcontentsattribute)
- [var kAXIncrementorAttribute: String](/documentation/applicationservices/kaxincrementorattribute)
- [var kAXHourFieldAttribute: String](/documentation/applicationservices/kaxhourfieldattribute)
- [var kAXMinuteFieldAttribute: String](/documentation/applicationservices/kaxminutefieldattribute)
- [var kAXSecondFieldAttribute: String](/documentation/applicationservices/kaxsecondfieldattribute)
- [var kAXAMPMFieldAttribute: String](/documentation/applicationservices/kaxampmfieldattribute)
- [var kAXDayFieldAttribute: String](/documentation/applicationservices/kaxdayfieldattribute)
- [var kAXMonthFieldAttribute: String](/documentation/applicationservices/kaxmonthfieldattribute)
- [var kAXYearFieldAttribute: String](/documentation/applicationservices/kaxyearfieldattribute)
- [var kAXColumnTitleAttribute: String](/documentation/applicationservices/kaxcolumntitleattribute)
- [var kAXURLAttribute: String](/documentation/applicationservices/kaxurlattribute)
- [var kAXLabelUIElementsAttribute: String](/documentation/applicationservices/kaxlabeluielementsattribute)
- [var kAXLabelValueAttribute: String](/documentation/applicationservices/kaxlabelvalueattribute)
- [var kAXShownMenuUIElementAttribute: String](/documentation/applicationservices/kaxshownmenuuielementattribute)
- [var kAXServesAsTitleForUIElementsAttribute: String](/documentation/applicationservices/kaxservesastitleforuielementsattribute)
- [var kAXLinkedUIElementsAttribute: String](/documentation/applicationservices/kaxlinkeduielementsattribute)
- [var kAXRowsAttribute: String](/documentation/applicationservices/kaxrowsattribute)
- [var kAXVisibleRowsAttribute: String](/documentation/applicationservices/kaxvisiblerowsattribute)
- [var kAXSelectedRowsAttribute: String](/documentation/applicationservices/kaxselectedrowsattribute)
- [var kAXColumnsAttribute: String](/documentation/applicationservices/kaxcolumnsattribute)
- [var kAXVisibleColumnsAttribute: String](/documentation/applicationservices/kaxvisiblecolumnsattribute)
- [var kAXSelectedColumnsAttribute: String](/documentation/applicationservices/kaxselectedcolumnsattribute)
- [var kAXSortDirectionAttribute: String](/documentation/applicationservices/kaxsortdirectionattribute)
- [var kAXColumnHeaderUIElementsAttribute: String](/documentation/applicationservices/kaxcolumnheaderuielementsattribute)
- [var kAXIndexAttribute: String](/documentation/applicationservices/kaxindexattribute)
- [var kAXDisclosingAttribute: String](/documentation/applicationservices/kaxdisclosingattribute)
- [var kAXDisclosedRowsAttribute: String](/documentation/applicationservices/kaxdisclosedrowsattribute)
- [var kAXDisclosedByRowAttribute: String](/documentation/applicationservices/kaxdisclosedbyrowattribute)
- [var kAXMatteHoleAttribute: String](/documentation/applicationservices/kaxmatteholeattribute)
- [var kAXMatteContentUIElementAttribute: String](/documentation/applicationservices/kaxmattecontentuielementattribute)
- [var kAXIsApplicationRunningAttribute: String](/documentation/applicationservices/kaxisapplicationrunningattribute)
- [var kAXFocusedApplicationAttribute: String](/documentation/applicationservices/kaxfocusedapplicationattribute)
- [var kAXInsertionPointLineNumberAttribute: String](/documentation/applicationservices/kaxinsertionpointlinenumberattribute)
- [Parameterized Attributes](/documentation/applicationservices/carbon_accessibility/parameterized_attributes)

#### Constants

- [var kAXLineForIndexParameterizedAttribute: String](/documentation/applicationservices/kaxlineforindexparameterizedattribute)
- [var kAXRangeForLineParameterizedAttribute: String](/documentation/applicationservices/kaxrangeforlineparameterizedattribute)
- [var kAXStringForRangeParameterizedAttribute: String](/documentation/applicationservices/kaxstringforrangeparameterizedattribute)
- [var kAXRangeForPositionParameterizedAttribute: String](/documentation/applicationservices/kaxrangeforpositionparameterizedattribute)
- [var kAXRangeForIndexParameterizedAttribute: String](/documentation/applicationservices/kaxrangeforindexparameterizedattribute)
- [var kAXBoundsForRangeParameterizedAttribute: String](/documentation/applicationservices/kaxboundsforrangeparameterizedattribute)
- [var kAXRTFForRangeParameterizedAttribute: String](/documentation/applicationservices/kaxrtfforrangeparameterizedattribute)
- [var kAXAttributedStringForRangeParameterizedAttribute: String](/documentation/applicationservices/kaxattributedstringforrangeparameterizedattribute)
- [var kAXStyleRangeForIndexParameterizedAttribute: String](/documentation/applicationservices/kaxstylerangeforindexparameterizedattribute)
- [Actions](/documentation/applicationservices/carbon_accessibility/actions)

#### Constants

- [var kAXPressAction: String](/documentation/applicationservices/kaxpressaction)
- [var kAXIncrementAction: String](/documentation/applicationservices/kaxincrementaction)
- [var kAXDecrementAction: String](/documentation/applicationservices/kaxdecrementaction)
- [var kAXConfirmAction: String](/documentation/applicationservices/kaxconfirmaction)
- [var kAXCancelAction: String](/documentation/applicationservices/kaxcancelaction)
- [var kAXRaiseAction: String](/documentation/applicationservices/kaxraiseaction)
- [var kAXShowMenuAction: String](/documentation/applicationservices/kaxshowmenuaction)
- [Notifications](/documentation/applicationservices/carbon_accessibility/notifications)

#### Constants

- [var kAXMainWindowChangedNotification: String](/documentation/applicationservices/kaxmainwindowchangednotification)
- [var kAXFocusedWindowChangedNotification: String](/documentation/applicationservices/kaxfocusedwindowchangednotification)
- [var kAXFocusedUIElementChangedNotification: String](/documentation/applicationservices/kaxfocuseduielementchangednotification)
- [var kAXApplicationActivatedNotification: String](/documentation/applicationservices/kaxapplicationactivatednotification)
- [var kAXApplicationDeactivatedNotification: String](/documentation/applicationservices/kaxapplicationdeactivatednotification)
- [var kAXApplicationHiddenNotification: String](/documentation/applicationservices/kaxapplicationhiddennotification)
- [var kAXApplicationShownNotification: String](/documentation/applicationservices/kaxapplicationshownnotification)
- [var kAXWindowCreatedNotification: String](/documentation/applicationservices/kaxwindowcreatednotification)
- [var kAXWindowMovedNotification: String](/documentation/applicationservices/kaxwindowmovednotification)
- [var kAXWindowResizedNotification: String](/documentation/applicationservices/kaxwindowresizednotification)
- [var kAXWindowMiniaturizedNotification: String](/documentation/applicationservices/kaxwindowminiaturizednotification)
- [var kAXWindowDeminiaturizedNotification: String](/documentation/applicationservices/kaxwindowdeminiaturizednotification)
- [var kAXDrawerCreatedNotification: String](/documentation/applicationservices/kaxdrawercreatednotification)
- [var kAXSheetCreatedNotification: String](/documentation/applicationservices/kaxsheetcreatednotification)
- [var kAXHelpTagCreatedNotification: String](/documentation/applicationservices/kaxhelptagcreatednotification)
- [var kAXValueChangedNotification: String](/documentation/applicationservices/kaxvaluechangednotification)
- [var kAXUIElementDestroyedNotification: String](/documentation/applicationservices/kaxuielementdestroyednotification)
- [var kAXMenuOpenedNotification: String](/documentation/applicationservices/kaxmenuopenednotification)
- [var kAXMenuClosedNotification: String](/documentation/applicationservices/kaxmenuclosednotification)
- [var kAXMenuItemSelectedNotification: String](/documentation/applicationservices/kaxmenuitemselectednotification)
- [var kAXRowCountChangedNotification: String](/documentation/applicationservices/kaxrowcountchangednotification)
- [var kAXSelectedChildrenChangedNotification: String](/documentation/applicationservices/kaxselectedchildrenchangednotification)
- [var kAXResizedNotification: String](/documentation/applicationservices/kaxresizednotification)
- [var kAXMovedNotification: String](/documentation/applicationservices/kaxmovednotification)
- [var kAXCreatedNotification: String](/documentation/applicationservices/kaxcreatednotification)
- [Orientations and Sort Directions](/documentation/applicationservices/carbon_accessibility/orientations_and_sort_directions)

#### Constants

- [var kAXHorizontalOrientationValue: String](/documentation/applicationservices/kaxhorizontalorientationvalue)
- [var kAXVerticalOrientationValue: String](/documentation/applicationservices/kaxverticalorientationvalue)
- [var kAXUnknownOrientationValue: String](/documentation/applicationservices/kaxunknownorientationvalue)
- [var kAXAscendingSortDirectionValue: String](/documentation/applicationservices/kaxascendingsortdirectionvalue)
- [var kAXUnknownSortDirectionValue: String](/documentation/applicationservices/kaxunknownsortdirectionvalue)

### Result Codes

- [case illegalArgument](/documentation/applicationservices/axerror/illegalargument)
- [case invalidUIElement](/documentation/applicationservices/axerror/invaliduielement)
- [case invalidUIElementObserver](/documentation/applicationservices/axerror/invaliduielementobserver)
- [case cannotComplete](/documentation/applicationservices/axerror/cannotcomplete)
- [case attributeUnsupported](/documentation/applicationservices/axerror/attributeunsupported)
- [case actionUnsupported](/documentation/applicationservices/axerror/actionunsupported)
- [case apiDisabled](/documentation/applicationservices/axerror/apidisabled)
- [case parameterizedAttributeUnsupported](/documentation/applicationservices/axerror/parameterizedattributeunsupported)
- [Core Printing](/documentation/applicationservices/core_printing)

### Releasing and Retaining Printing Objects

- [func PMRelease(PMObject?) -> OSStatus](/documentation/applicationservices/1461402-pmrelease)
- [func PMRetain(PMObject?) -> OSStatus](/documentation/applicationservices/1460190-pmretain)

### Creating and Using Page Format Objects

- [func PMCreatePageFormat(UnsafeMutablePointer<PMPageFormat?>) -> OSStatus](/documentation/applicationservices/1459485-pmcreatepageformat)
- [func PMCreatePageFormatWithPMPaper(UnsafeMutablePointer<PMPageFormat?>, PMPaper) -> OSStatus](/documentation/applicationservices/1459274-pmcreatepageformatwithpmpaper)
- [func PMCopyPageFormat(PMPageFormat, PMPageFormat) -> OSStatus](/documentation/applicationservices/1464669-pmcopypageformat)
- [func PMSessionDefaultPageFormat(PMPrintSession, PMPageFormat) -> OSStatus](/documentation/applicationservices/1462217-pmsessiondefaultpageformat)
- [func PMSessionValidatePageFormat(PMPrintSession, PMPageFormat, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/applicationservices/1459090-pmsessionvalidatepageformat)
- [func PMSessionCreatePageFormatList(PMPrintSession, PMPrinter?, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1463985-pmsessioncreatepageformatlist)
- [func PMPageFormatCreateDataRepresentation(PMPageFormat, UnsafeMutablePointer<Unmanaged<CFData>?>, PMDataFormat) -> OSStatus](/documentation/applicationservices/1464227-pmpageformatcreatedatarepresenta)
- [func PMPageFormatCreateWithDataRepresentation(CFData, UnsafeMutablePointer<PMPageFormat?>) -> OSStatus](/documentation/applicationservices/1462876-pmpageformatcreatewithdatarepres)

### Accessing Data in Page Format Objects

- [func PMGetPageFormatExtendedData(PMPageFormat, OSType, UnsafeMutablePointer<UInt32>?, UnsafeMutableRawPointer?) -> OSStatus](/documentation/applicationservices/1464455-pmgetpageformatextendeddata)
- [func PMSetPageFormatExtendedData(PMPageFormat, OSType, UInt32, UnsafeMutableRawPointer) -> OSStatus](/documentation/applicationservices/1463464-pmsetpageformatextendeddata)
- [func PMGetPageFormatPaper(PMPageFormat, UnsafeMutablePointer<PMPaper?>) -> OSStatus](/documentation/applicationservices/1461319-pmgetpageformatpaper)
- [func PMPageFormatGetPrinterID(PMPageFormat, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1462961-pmpageformatgetprinterid)
- [func PMGetOrientation(PMPageFormat, UnsafeMutablePointer<PMOrientation>) -> OSStatus](/documentation/applicationservices/1459144-pmgetorientation)
- [func PMSetOrientation(PMPageFormat, PMOrientation, Bool) -> OSStatus](/documentation/applicationservices/1459016-pmsetorientation)
- [func PMGetScale(PMPageFormat, UnsafeMutablePointer<Double>) -> OSStatus](/documentation/applicationservices/1458796-pmgetscale)
- [func PMSetScale(PMPageFormat, Double) -> OSStatus](/documentation/applicationservices/1463343-pmsetscale)
- [func PMGetAdjustedPageRect(PMPageFormat, UnsafeMutablePointer<PMRect>) -> OSStatus](/documentation/applicationservices/1461543-pmgetadjustedpagerect)
- [func PMGetAdjustedPaperRect(PMPageFormat, UnsafeMutablePointer<PMRect>) -> OSStatus](/documentation/applicationservices/1459167-pmgetadjustedpaperrect)
- [func PMGetUnadjustedPageRect(PMPageFormat, UnsafeMutablePointer<PMRect>) -> OSStatus](/documentation/applicationservices/1462944-pmgetunadjustedpagerect)
- [func PMGetUnadjustedPaperRect(PMPageFormat, UnsafeMutablePointer<PMRect>) -> OSStatus](/documentation/applicationservices/1462939-pmgetunadjustedpaperrect)

### Creating and Using Print Settings Objects

- [func PMCreatePrintSettings(UnsafeMutablePointer<PMPrintSettings?>) -> OSStatus](/documentation/applicationservices/1463239-pmcreateprintsettings)
- [func PMSessionDefaultPrintSettings(PMPrintSession, PMPrintSettings) -> OSStatus](/documentation/applicationservices/1460138-pmsessiondefaultprintsettings)
- [func PMSessionValidatePrintSettings(PMPrintSession, PMPrintSettings, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/applicationservices/1458994-pmsessionvalidateprintsettings)
- [func PMPrintSettingsCreateDataRepresentation(PMPrintSettings, UnsafeMutablePointer<Unmanaged<CFData>?>, PMDataFormat) -> OSStatus](/documentation/applicationservices/1464570-pmprintsettingscreatedatareprese)
- [func PMPrintSettingsCreateWithDataRepresentation(CFData, UnsafeMutablePointer<PMPrintSettings?>) -> OSStatus](/documentation/applicationservices/1462203-pmprintsettingscreatewithdatarep)
- [func PMCopyPrintSettings(PMPrintSettings, PMPrintSettings) -> OSStatus](/documentation/applicationservices/1462491-pmcopyprintsettings)
- [func PMPrintSettingsToOptions(PMPrintSettings, UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>) -> OSStatus](/documentation/applicationservices/1459069-pmprintsettingstooptions)
- [func PMPrintSettingsToOptionsWithPrinterAndPageFormat(PMPrintSettings, PMPrinter, PMPageFormat?, UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>) -> OSStatus](/documentation/applicationservices/1459435-pmprintsettingstooptionswithprin)

### Accessing Data in Print Settings Objects

- [func PMGetFirstPage(PMPrintSettings, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/applicationservices/1460271-pmgetfirstpage)
- [func PMSetFirstPage(PMPrintSettings, UInt32, Bool) -> OSStatus](/documentation/applicationservices/1461519-pmsetfirstpage)
- [func PMGetLastPage(PMPrintSettings, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/applicationservices/1462747-pmgetlastpage)
- [func PMSetLastPage(PMPrintSettings, UInt32, Bool) -> OSStatus](/documentation/applicationservices/1463595-pmsetlastpage)
- [func PMGetPageRange(PMPrintSettings, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/applicationservices/1459324-pmgetpagerange)
- [func PMSetPageRange(PMPrintSettings, UInt32, UInt32) -> OSStatus](/documentation/applicationservices/1462294-pmsetpagerange)
- [func PMPrintSettingsGetJobName(PMPrintSettings, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1459233-pmprintsettingsgetjobname)
- [func PMPrintSettingsSetJobName(PMPrintSettings, CFString) -> OSStatus](/documentation/applicationservices/1460149-pmprintsettingssetjobname)
- [func PMGetCopies(PMPrintSettings, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/applicationservices/1464480-pmgetcopies)
- [func PMSetCopies(PMPrintSettings, UInt32, Bool) -> OSStatus](/documentation/applicationservices/1463804-pmsetcopies)
- [func PMGetCollate(PMPrintSettings, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/applicationservices/1464492-pmgetcollate)
- [func PMSetCollate(PMPrintSettings, Bool) -> OSStatus](/documentation/applicationservices/1463223-pmsetcollate)
- [func PMGetDuplex(PMPrintSettings, UnsafeMutablePointer<PMDuplexMode>) -> OSStatus](/documentation/applicationservices/1458921-pmgetduplex)
- [func PMSetDuplex(PMPrintSettings, PMDuplexMode) -> OSStatus](/documentation/applicationservices/1462000-pmsetduplex)
- [func PMPrintSettingsGetValue(PMPrintSettings, CFString, UnsafeMutablePointer<Unmanaged<CFTypeRef>?>) -> OSStatus](/documentation/applicationservices/1460602-pmprintsettingsgetvalue)
- [func PMPrintSettingsSetValue(PMPrintSettings, CFString, CFTypeRef?, Bool) -> OSStatus](/documentation/applicationservices/1461697-pmprintsettingssetvalue)
- [func PMPrintSettingsCopyAsDictionary(PMPrintSettings, UnsafeMutablePointer<Unmanaged<CFDictionary>?>) -> OSStatus](/documentation/applicationservices/1459088-pmprintsettingscopyasdictionary)
- [func PMPrintSettingsCopyKeys(PMPrintSettings, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1462730-pmprintsettingscopykeys)

### Creating Printing Session Objects

- [func PMCreateSession(UnsafeMutablePointer<PMPrintSession?>) -> OSStatus](/documentation/applicationservices/1463247-pmcreatesession)

### Accessing Data in Printing Session Objects

- [func PMSessionGetDataFromSession(PMPrintSession, CFString, UnsafeMutablePointer<Unmanaged<CFTypeRef>?>) -> OSStatus](/documentation/applicationservices/1462964-pmsessiongetdatafromsession)
- [func PMSessionSetDataInSession(PMPrintSession, CFString, CFTypeRef) -> OSStatus](/documentation/applicationservices/1461902-pmsessionsetdatainsession)
- [func PMSessionGetCurrentPrinter(PMPrintSession, UnsafeMutablePointer<PMPrinter?>) -> OSStatus](/documentation/applicationservices/1458998-pmsessiongetcurrentprinter)
- [func PMSessionSetCurrentPMPrinter(PMPrintSession, PMPrinter) -> OSStatus](/documentation/applicationservices/1461096-pmsessionsetcurrentpmprinter)
- [func PMSessionGetCGGraphicsContext(PMPrintSession, UnsafeMutablePointer<Unmanaged<CGContext>?>) -> OSStatus](/documentation/applicationservices/1461952-pmsessiongetcggraphicscontext)
- [func PMSessionError(PMPrintSession) -> OSStatus](/documentation/applicationservices/1460003-pmsessionerror)
- [func PMSessionSetError(PMPrintSession, OSStatus) -> OSStatus](/documentation/applicationservices/1460216-pmsessionseterror)

### Using Printer Presets

- [func PMPresetCopyName(PMPreset, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1460343-pmpresetcopyname)
- [func PMPresetCreatePrintSettings(PMPreset, PMPrintSession, UnsafeMutablePointer<PMPrintSettings?>) -> OSStatus](/documentation/applicationservices/1463414-pmpresetcreateprintsettings)
- [func PMPresetGetAttributes(PMPreset, UnsafeMutablePointer<Unmanaged<CFDictionary>?>) -> OSStatus](/documentation/applicationservices/1459042-pmpresetgetattributes)

### Creating and Using Paper Objects

- [func PMPaperCreateCustom(PMPrinter?, CFString?, CFString?, Double, Double, UnsafePointer<PMPaperMargins>, UnsafeMutablePointer<PMPaper?>) -> OSStatus](/documentation/applicationservices/1459322-pmpapercreatecustom)
- [func PMPaperIsCustom(PMPaper) -> Bool](/documentation/applicationservices/1459526-pmpaperiscustom)

### Accessing Data in Paper Objects

- [func PMPaperGetID(PMPaper, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1462910-pmpapergetid)
- [func PMPaperGetWidth(PMPaper, UnsafeMutablePointer<Double>) -> OSStatus](/documentation/applicationservices/1459209-pmpapergetwidth)
- [func PMPaperGetHeight(PMPaper, UnsafeMutablePointer<Double>) -> OSStatus](/documentation/applicationservices/1460389-pmpapergetheight)
- [func PMPaperGetMargins(PMPaper, UnsafeMutablePointer<PMPaperMargins>) -> OSStatus](/documentation/applicationservices/1461994-pmpapergetmargins)
- [func PMPaperCreateLocalizedName(PMPaper, PMPrinter, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1460981-pmpapercreatelocalizedname)
- [func PMPaperGetPrinterID(PMPaper, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1461737-pmpapergetprinterid)
- [func PMPaperGetPPDPaperName(PMPaper, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1461039-pmpapergetppdpapername)

### Print Loop Functions

- [func PMSessionBeginCGDocumentNoDialog(PMPrintSession, PMPrintSettings, PMPageFormat) -> OSStatus](/documentation/applicationservices/1460101-pmsessionbegincgdocumentnodialog)
- [func PMSessionEndDocumentNoDialog(PMPrintSession) -> OSStatus](/documentation/applicationservices/1464527-pmsessionenddocumentnodialog)
- [func PMSessionBeginPageNoDialog(PMPrintSession, PMPageFormat?, UnsafePointer<PMRect>?) -> OSStatus](/documentation/applicationservices/1463416-pmsessionbeginpagenodialog)
- [func PMSessionEndPageNoDialog(PMPrintSession) -> OSStatus](/documentation/applicationservices/1462014-pmsessionendpagenodialog)

### Accessing the Print Job Destination

- [func PMSessionSetDestination(PMPrintSession, PMPrintSettings, PMDestinationType, CFString?, CFURL?) -> OSStatus](/documentation/applicationservices/1459855-pmsessionsetdestination)
- [func PMSessionGetDestinationType(PMPrintSession, PMPrintSettings, UnsafeMutablePointer<PMDestinationType>) -> OSStatus](/documentation/applicationservices/1461071-pmsessiongetdestinationtype)
- [func PMSessionCopyDestinationFormat(PMPrintSession, PMPrintSettings, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1464266-pmsessioncopydestinationformat)
- [func PMSessionCopyDestinationLocation(PMPrintSession, PMPrintSettings, UnsafeMutablePointer<Unmanaged<CFURL>?>) -> OSStatus](/documentation/applicationservices/1462967-pmsessioncopydestinationlocation)
- [func PMSessionCopyOutputFormatList(PMPrintSession, PMDestinationType, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1461332-pmsessioncopyoutputformatlist)

### Creating Printer Objects

- [func PMServerLaunchPrinterBrowser(PMServer?, CFDictionary?) -> OSStatus](/documentation/applicationservices/1460175-pmserverlaunchprinterbrowser)
- [func PMServerCreatePrinterList(PMServer?, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1459953-pmservercreateprinterlist)
- [func PMSessionCreatePrinterList(PMPrintSession, UnsafeMutablePointer<Unmanaged<CFArray>?>, UnsafeMutablePointer<CFIndex>?, UnsafeMutablePointer<PMPrinter?>?) -> OSStatus](/documentation/applicationservices/1460119-pmsessioncreateprinterlist)
- [func PMPrinterCreateFromPrinterID(CFString) -> PMPrinter?](/documentation/applicationservices/1461363-pmprintercreatefromprinterid)
- [func PMCreateGenericPrinter(UnsafeMutablePointer<PMPrinter?>) -> OSStatus](/documentation/applicationservices/1461960-pmcreategenericprinter)

### Accessing Information About a Printer

- [func PMPrinterCopyDescriptionURL(PMPrinter, CFString, UnsafeMutablePointer<Unmanaged<CFURL>?>) -> OSStatus](/documentation/applicationservices/1459187-pmprintercopydescriptionurl)
- [func PMPrinterCopyDeviceURI(PMPrinter, UnsafeMutablePointer<Unmanaged<CFURL>?>) -> OSStatus](/documentation/applicationservices/1460543-pmprintercopydeviceuri)
- [func PMPrinterCopyHostName(PMPrinter, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1462076-pmprintercopyhostname)
- [func PMPrinterCopyPresets(PMPrinter, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1459117-pmprintercopypresets)
- [func PMPrinterGetCommInfo(PMPrinter, UnsafeMutablePointer<DarwinBoolean>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/applicationservices/1461069-pmprintergetcomminfo)
- [func PMPrinterGetDriverCreator(PMPrinter, UnsafeMutablePointer<OSType>) -> OSStatus](/documentation/applicationservices/1459107-pmprintergetdrivercreator)
- [func PMPrinterGetID(PMPrinter) -> Unmanaged<CFString>?](/documentation/applicationservices/1459606-pmprintergetid)
- [func PMPrinterGetLocation(PMPrinter) -> Unmanaged<CFString>?](/documentation/applicationservices/1461467-pmprintergetlocation)
- [func PMPrinterGetMakeAndModelName(PMPrinter, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/applicationservices/1463347-pmprintergetmakeandmodelname)
- [func PMPrinterGetMimeTypes(PMPrinter, PMPrintSettings?, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1460125-pmprintergetmimetypes)
- [func PMPrinterGetName(PMPrinter) -> Unmanaged<CFString>?](/documentation/applicationservices/1459018-pmprintergetname)
- [func PMPrinterGetOutputResolution(PMPrinter, PMPrintSettings, UnsafeMutablePointer<PMResolution>) -> OSStatus](/documentation/applicationservices/1459076-pmprintergetoutputresolution)
- [func PMPrinterSetOutputResolution(PMPrinter, PMPrintSettings, UnsafePointer<PMResolution>) -> OSStatus](/documentation/applicationservices/1459931-pmprintersetoutputresolution)
- [func PMPrinterGetPaperList(PMPrinter, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1460088-pmprintergetpaperlist)
- [func PMPrinterGetPrinterResolutionCount(PMPrinter, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/applicationservices/1462004-pmprintergetprinterresolutioncou)
- [func PMPrinterGetIndexedPrinterResolution(PMPrinter, UInt32, UnsafeMutablePointer<PMResolution>) -> OSStatus](/documentation/applicationservices/1464490-pmprintergetindexedprinterresolu)
- [func PMPrinterGetState(PMPrinter, UnsafeMutablePointer<PMPrinterState>) -> OSStatus](/documentation/applicationservices/1462954-pmprintergetstate)
- [func PMPrinterSetDefault(PMPrinter) -> OSStatus](/documentation/applicationservices/1461118-pmprintersetdefault)
- [func PMPrinterIsDefault(PMPrinter) -> Bool](/documentation/applicationservices/1459030-pmprinterisdefault)
- [func PMPrinterIsFavorite(PMPrinter) -> Bool](/documentation/applicationservices/1462074-pmprinterisfavorite)
- [func PMPrinterIsPostScriptCapable(PMPrinter) -> Bool](/documentation/applicationservices/1464168-pmprinterispostscriptcapable)
- [func PMPrinterIsPostScriptPrinter(PMPrinter, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/applicationservices/1462257-pmprinterispostscriptprinter)
- [func PMPrinterIsRemote(PMPrinter, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/applicationservices/1461377-pmprinterisremote)

### Submitting a Print Job to a Printer

- [func PMPrinterPrintWithFile(PMPrinter, PMPrintSettings, PMPageFormat?, CFString?, CFURL) -> OSStatus](/documentation/applicationservices/1464600-pmprinterprintwithfile)
- [func PMPrinterPrintWithProvider(PMPrinter, PMPrintSettings, PMPageFormat?, CFString, CGDataProvider) -> OSStatus](/documentation/applicationservices/1461110-pmprinterprintwithprovider)

### Accessing PostScript Printer Description Files

- [func PMCopyAvailablePPDs(PMPPDDomain, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1464170-pmcopyavailableppds)
- [func PMCopyLocalizedPPD(CFURL, UnsafeMutablePointer<Unmanaged<CFURL>?>) -> OSStatus](/documentation/applicationservices/1459690-pmcopylocalizedppd)
- [func PMCopyPPDData(CFURL, UnsafeMutablePointer<Unmanaged<CFData>?>) -> OSStatus](/documentation/applicationservices/1460345-pmcopyppddata)

### Printing with PostScript Data

- [func PMCGImageCreateWithEPSDataProvider(CGDataProvider?, CGImage) -> Unmanaged<CGImage>?](/documentation/applicationservices/1462361-pmcgimagecreatewithepsdataprovid)
- [func PMPrinterWritePostScriptToURL(PMPrinter, PMPrintSettings, PMPageFormat?, CFString?, CFURL, CFURL) -> OSStatus](/documentation/applicationservices/1459729-pmprinterwritepostscripttourl)

### Using PDF Workflow Items

- [func PMWorkflowCopyItems(UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/applicationservices/1459914-pmworkflowcopyitems)
- [func PMWorkflowSubmitPDFWithOptions(CFURL, CFString?, UnsafePointer<CChar>?, CFURL) -> OSStatus](/documentation/applicationservices/1463747-pmworkflowsubmitpdfwithoptions)
- [func PMWorkflowSubmitPDFWithSettings(CFURL, PMPrintSettings, CFURL) -> OSStatus](/documentation/applicationservices/1458874-pmworkflowsubmitpdfwithsettings)

### Data Types

- [PMObject](/documentation/applicationservices/pmobject)
- [PMPageFormat](/documentation/applicationservices/pmpageformat)
- [PMPaper](/documentation/applicationservices/pmpaper)
- [PMPaperMargins](/documentation/applicationservices/pmpapermargins)
- [PMPreset](/documentation/applicationservices/pmpreset)
- [PMPrinter](/documentation/applicationservices/pmprinter)
- [PMPrintSession](/documentation/applicationservices/pmprintsession)
- [PMPrintSettings](/documentation/applicationservices/pmprintsettings)
- [PMServer](/documentation/applicationservices/pmserver)

### Constants

- [PMDataFormat](/documentation/applicationservices/pmdataformat)

#### Constants

- [var kPMDataFormatXMLDefault: PMDataFormat](/documentation/applicationservices/kpmdataformatxmldefault)
- [var kPMDataFormatXMLMinimal: PMDataFormat](/documentation/applicationservices/kpmdataformatxmlminimal)
- [var kPMDataFormatXMLCompressed: PMDataFormat](/documentation/applicationservices/kpmdataformatxmlcompressed)

#### Initializers

- [init(UInt32)](/documentation/applicationservices/pmdataformat/1462724-init)
- [init(rawValue: UInt32)](/documentation/applicationservices/pmdataformat/1459732-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/applicationservices/pmdataformat/1459960-rawvalue)
- [PMDestinationType](/documentation/applicationservices/pmdestinationtype)

#### Constants

- [var kPMDestinationInvalid: Int](/documentation/applicationservices/kpmdestinationinvalid)
- [var kPMDestinationPrinter: Int](/documentation/applicationservices/kpmdestinationprinter)
- [var kPMDestinationFile: Int](/documentation/applicationservices/kpmdestinationfile)
- [var kPMDestinationFax: Int](/documentation/applicationservices/kpmdestinationfax)
- [var kPMDestinationPreview: Int](/documentation/applicationservices/kpmdestinationpreview)
- [var kPMDestinationProcessPDF: Int](/documentation/applicationservices/kpmdestinationprocesspdf)
- [PMDuplexMode](/documentation/applicationservices/pmduplexmode)

#### Constants

- [var kPMDuplexNone: Int](/documentation/applicationservices/kpmduplexnone)
- [var kPMDuplexNoTumble: Int](/documentation/applicationservices/kpmduplexnotumble)
- [var kPMDuplexTumble: Int](/documentation/applicationservices/kpmduplextumble)
- [var kPMSimplexTumble: Int](/documentation/applicationservices/kpmsimplextumble)
- [PMOrientation](/documentation/applicationservices/pmorientation)

#### Constants

- [var kPMPortrait: Int](/documentation/applicationservices/kpmportrait)
- [var kPMLandscape: Int](/documentation/applicationservices/kpmlandscape)
- [var kPMReversePortrait: Int](/documentation/applicationservices/kpmreverseportrait)
- [var kPMReverseLandscape: Int](/documentation/applicationservices/kpmreverselandscape)
- [PDF Workflow Dictionary Keys](/documentation/applicationservices/core_printing/pdf_workflow_dictionary_keys)

#### Constants

- [var kPDFWorkflowDisplayNameKey: String](/documentation/applicationservices/kpdfworkflowdisplaynamekey)
- [var kPDFWorkflowItemsKey: String](/documentation/applicationservices/kpdfworkflowitemskey)
- [PMPPDDomain](/documentation/applicationservices/pmppddomain)

#### Constants

- [var kAllPPDDomains: Int](/documentation/applicationservices/kallppddomains)
- [var kSystemPPDDomain: Int](/documentation/applicationservices/ksystemppddomain)
- [var kLocalPPDDomain: Int](/documentation/applicationservices/klocalppddomain)
- [var kNetworkPPDDomain: Int](/documentation/applicationservices/knetworkppddomain)
- [var kUserPPDDomain: Int](/documentation/applicationservices/kuserppddomain)
- [var kCUPSPPDDomain: Int](/documentation/applicationservices/kcupsppddomain)
- [Print All Pages Constant](/documentation/applicationservices/core_printing/1506768-print_all_pages_constant)

#### Constants

- [var kPMPrintAllPages: Int](/documentation/applicationservices/kpmprintallpages)
- [PMQualityMode](/documentation/applicationservices/pmqualitymode)

#### Constants

- [var kPMQualityLowest: Int](/documentation/applicationservices/kpmqualitylowest)
- [var kPMQualityInkSaver: Int](/documentation/applicationservices/kpmqualityinksaver)
- [var kPMQualityDraft: Int](/documentation/applicationservices/kpmqualitydraft)
- [var kPMQualityNormal: Int](/documentation/applicationservices/kpmqualitynormal)
- [var kPMQualityPhoto: Int](/documentation/applicationservices/kpmqualityphoto)
- [var kPMQualityBest: Int](/documentation/applicationservices/kpmqualitybest)
- [var kPMQualityHighest: Int](/documentation/applicationservices/kpmqualityhighest)
- [PMPrinterState](/documentation/applicationservices/pmprinterstate)

#### Constants

- [var kPMPrinterIdle: Int](/documentation/applicationservices/kpmprinteridle)
- [var kPMPrinterProcessing: Int](/documentation/applicationservices/kpmprinterprocessing)
- [var kPMPrinterStopped: Int](/documentation/applicationservices/kpmprinterstopped)
- [Printer Description Types](/documentation/applicationservices/core_printing/printer_description_types)

#### Constants

- [var kPMPPDDescriptionType: String](/documentation/applicationservices/kpmppddescriptiontype)
- [User Cancellation Constant](/documentation/applicationservices/core_printing/1506795-user_cancellation_constant)

#### Constants

- [var kPMCancel: Int](/documentation/applicationservices/kpmcancel)

### Result Codes

- [var kPMGeneralError: Int](/documentation/applicationservices/kpmgeneralerror)
- [var kPMOutOfScope: Int](/documentation/applicationservices/kpmoutofscope)
- [var kPMNoDefaultPrinter: Int](/documentation/applicationservices/kpmnodefaultprinter)
- [var kPMNotImplemented: Int](/documentation/applicationservices/kpmnotimplemented)
- [var kPMNoSuchEntry: Int](/documentation/applicationservices/kpmnosuchentry)
- [var kPMInvalidPrintSettings: Int](/documentation/applicationservices/kpminvalidprintsettings)
- [var kPMInvalidPageFormat: Int](/documentation/applicationservices/kpminvalidpageformat)
- [var kPMValueOutOfRange: Int](/documentation/applicationservices/kpmvalueoutofrange)
- [var kPMInvalidPrintSession: Int](/documentation/applicationservices/kpminvalidprintsession)
- [var kPMInvalidPrinter: Int](/documentation/applicationservices/kpminvalidprinter)
- [var kPMObjectInUse: Int](/documentation/applicationservices/kpmobjectinuse)
- [var kPMInvalidIndex: Int](/documentation/applicationservices/kpminvalidindex)
- [var kPMStringConversionFailure: Int](/documentation/applicationservices/kpmstringconversionfailure)
- [var kPMXMLParseError: Int](/documentation/applicationservices/kpmxmlparseerror)
- [var kPMInvalidJobTemplate: Int](/documentation/applicationservices/kpminvalidjobtemplate)
- [var kPMInvalidPrinterInfo: Int](/documentation/applicationservices/kpminvalidprinterinfo)
- [var kPMInvalidConnection: Int](/documentation/applicationservices/kpminvalidconnection)
- [var kPMInvalidKey: Int](/documentation/applicationservices/kpminvalidkey)
- [var kPMInvalidValue: Int](/documentation/applicationservices/kpminvalidvalue)
- [var kPMInvalidAllocator: Int](/documentation/applicationservices/kpminvalidallocator)
- [var kPMInvalidTicket: Int](/documentation/applicationservices/kpminvalidticket)
- [var kPMInvalidItem: Int](/documentation/applicationservices/kpminvaliditem)
- [var kPMInvalidType: Int](/documentation/applicationservices/kpminvalidtype)
- [var kPMInvalidReply: Int](/documentation/applicationservices/kpminvalidreply)
- [var kPMInvalidFileType: Int](/documentation/applicationservices/kpminvalidfiletype)
- [var kPMInvalidObject: Int](/documentation/applicationservices/kpminvalidobject)
- [var kPMInvalidPaper: Int](/documentation/applicationservices/kpminvalidpaper)
- [var kPMInvalidCalibrationTarget: Int](/documentation/applicationservices/kpminvalidcalibrationtarget)
- [var kPMInvalidPreset: Int](/documentation/applicationservices/kpminvalidpreset)
- [AXActionConstants.h](/documentation/applicationservices/axactionconstants_h)

### Constants

- [Miscellaneous Defines](/documentation/applicationservices/axactionconstants_h/miscellaneous_defines)

#### Constants

- [var kAXCancelAction: String](/documentation/applicationservices/kaxcancelaction)
- [var kAXConfirmAction: String](/documentation/applicationservices/kaxconfirmaction)
- [var kAXDecrementAction: String](/documentation/applicationservices/kaxdecrementaction)
- [var kAXIncrementAction: String](/documentation/applicationservices/kaxincrementaction)
- [var kAXPickAction: String](/documentation/applicationservices/kaxpickaction)
- [var kAXPressAction: String](/documentation/applicationservices/kaxpressaction)
- [var kAXRaiseAction: String](/documentation/applicationservices/kaxraiseaction)
- [var kAXShowAlternateUIAction: String](/documentation/applicationservices/kaxshowalternateuiaction)
- [var kAXShowDefaultUIAction: String](/documentation/applicationservices/kaxshowdefaultuiaction)
- [var kAXShowMenuAction: String](/documentation/applicationservices/kaxshowmenuaction)
- [AXAttributeConstants.h](/documentation/applicationservices/axattributeconstants_h)

### Constants

- [Miscellaneous Defines](/documentation/applicationservices/axattributeconstants_h/miscellaneous_defines)

#### Constants

- [var kAXAllowedValuesAttribute: String](/documentation/applicationservices/kaxallowedvaluesattribute)
- [var kAXAMPMFieldAttribute: String](/documentation/applicationservices/kaxampmfieldattribute)
- [var kAXCancelButtonAttribute: String](/documentation/applicationservices/kaxcancelbuttonattribute)
- [var kAXChildrenAttribute: String](/documentation/applicationservices/kaxchildrenattribute)
- [var kAXCloseButtonAttribute: String](/documentation/applicationservices/kaxclosebuttonattribute)
- [var kAXColumnTitleAttribute: String](/documentation/applicationservices/kaxcolumntitleattribute)
- [var kAXContentsAttribute: String](/documentation/applicationservices/kaxcontentsattribute)
- [var kAXDayFieldAttribute: String](/documentation/applicationservices/kaxdayfieldattribute)
- [var kAXDefaultButtonAttribute: String](/documentation/applicationservices/kaxdefaultbuttonattribute)
- [var kAXDescriptionAttribute: String](/documentation/applicationservices/kaxdescriptionattribute)
- [var kAXEnabledAttribute: String](/documentation/applicationservices/kaxenabledattribute)
- [var kAXFocusedAttribute: String](/documentation/applicationservices/kaxfocusedattribute)
- [var kAXGrowAreaAttribute: String](/documentation/applicationservices/kaxgrowareaattribute)
- [var kAXHeaderAttribute: String](/documentation/applicationservices/kaxheaderattribute)
- [var kAXHelpAttribute: String](/documentation/applicationservices/kaxhelpattribute)
- [var kAXHourFieldAttribute: String](/documentation/applicationservices/kaxhourfieldattribute)
- [var kAXIncrementorAttribute: String](/documentation/applicationservices/kaxincrementorattribute)
- [var kAXInsertionPointLineNumberAttribute: String](/documentation/applicationservices/kaxinsertionpointlinenumberattribute)
- [var kAXMainAttribute: String](/documentation/applicationservices/kaxmainattribute)
- [var kAXMaxValueAttribute: String](/documentation/applicationservices/kaxmaxvalueattribute)
- [var kAXMinimizeButtonAttribute: String](/documentation/applicationservices/kaxminimizebuttonattribute)
- [var kAXMinimizedAttribute: String](/documentation/applicationservices/kaxminimizedattribute)
- [var kAXMinuteFieldAttribute: String](/documentation/applicationservices/kaxminutefieldattribute)
- [var kAXMinValueAttribute: String](/documentation/applicationservices/kaxminvalueattribute)
- [var kAXModalAttribute: String](/documentation/applicationservices/kaxmodalattribute)
- [var kAXMonthFieldAttribute: String](/documentation/applicationservices/kaxmonthfieldattribute)
- [var kAXNumberOfCharactersAttribute: String](/documentation/applicationservices/kaxnumberofcharactersattribute)
- [var kAXOrientationAttribute: String](/documentation/applicationservices/kaxorientationattribute)
- [var kAXParentAttribute: String](/documentation/applicationservices/kaxparentattribute)
- [var kAXPositionAttribute: String](/documentation/applicationservices/kaxpositionattribute)
- [var kAXProxyAttribute: String](/documentation/applicationservices/kaxproxyattribute)
- [var kAXRoleAttribute: String](/documentation/applicationservices/kaxroleattribute)
- [var kAXRoleDescriptionAttribute: String](/documentation/applicationservices/kaxroledescriptionattribute)
- [var kAXSecondFieldAttribute: String](/documentation/applicationservices/kaxsecondfieldattribute)
- [var kAXSelectedChildrenAttribute: String](/documentation/applicationservices/kaxselectedchildrenattribute)
- [var kAXSelectedTextAttribute: String](/documentation/applicationservices/kaxselectedtextattribute)
- [var kAXSelectedTextRangeAttribute: String](/documentation/applicationservices/kaxselectedtextrangeattribute)
- [var kAXSelectedTextRangesAttribute: String](/documentation/applicationservices/kaxselectedtextrangesattribute)
- [var kAXSharedCharacterRangeAttribute: String](/documentation/applicationservices/kaxsharedcharacterrangeattribute)
- [var kAXSharedTextUIElementsAttribute: String](/documentation/applicationservices/kaxsharedtextuielementsattribute)
- [var kAXSizeAttribute: String](/documentation/applicationservices/kaxsizeattribute)
- [var kAXSubroleAttribute: String](/documentation/applicationservices/kaxsubroleattribute)
- [var kAXTitleAttribute: String](/documentation/applicationservices/kaxtitleattribute)
- [var kAXToolbarButtonAttribute: String](/documentation/applicationservices/kaxtoolbarbuttonattribute)
- [var kAXTopLevelUIElementAttribute: String](/documentation/applicationservices/kaxtopleveluielementattribute)
- [var kAXURLAttribute: String](/documentation/applicationservices/kaxurlattribute)
- [var kAXValueAttribute: String](/documentation/applicationservices/kaxvalueattribute)
- [var kAXValueDescriptionAttribute: String](/documentation/applicationservices/kaxvaluedescriptionattribute)
- [var kAXValueIncrementAttribute: String](/documentation/applicationservices/kaxvalueincrementattribute)
- [var kAXVisibleCharacterRangeAttribute: String](/documentation/applicationservices/kaxvisiblecharacterrangeattribute)
- [var kAXVisibleChildrenAttribute: String](/documentation/applicationservices/kaxvisiblechildrenattribute)
- [var kAXVisibleColumnsAttribute: String](/documentation/applicationservices/kaxvisiblecolumnsattribute)
- [var kAXWindowAttribute: String](/documentation/applicationservices/kaxwindowattribute)
- [var kAXYearFieldAttribute: String](/documentation/applicationservices/kaxyearfieldattribute)
- [var kAXZoomButtonAttribute: String](/documentation/applicationservices/kaxzoombuttonattribute)
- [AXMenuItemModifiers](/documentation/applicationservices/axmenuitemmodifiers)

#### Initializers

- [init(rawValue: UInt32)](/documentation/applicationservices/axmenuitemmodifiers/1460320-init)

#### Type Properties

- [static var control: AXMenuItemModifiers](/documentation/applicationservices/axmenuitemmodifiers/1464333-control)
- [static var noCommand: AXMenuItemModifiers](/documentation/applicationservices/axmenuitemmodifiers/1464506-nocommand)
- [static var option: AXMenuItemModifiers](/documentation/applicationservices/axmenuitemmodifiers/1462352-option)
- [static var shift: AXMenuItemModifiers](/documentation/applicationservices/axmenuitemmodifiers/1461092-shift)
- [AXError.h](/documentation/applicationservices/axerror_h)

### Constants

- [AXError](/documentation/applicationservices/axerror)

#### Enumeration Cases

- [case apiDisabled](/documentation/applicationservices/axerror/apidisabled)
- [case actionUnsupported](/documentation/applicationservices/axerror/actionunsupported)
- [case attributeUnsupported](/documentation/applicationservices/axerror/attributeunsupported)
- [case cannotComplete](/documentation/applicationservices/axerror/cannotcomplete)
- [case failure](/documentation/applicationservices/axerror/failure)
- [case illegalArgument](/documentation/applicationservices/axerror/illegalargument)
- [case invalidUIElement](/documentation/applicationservices/axerror/invaliduielement)
- [case invalidUIElementObserver](/documentation/applicationservices/axerror/invaliduielementobserver)
- [case noValue](/documentation/applicationservices/axerror/novalue)
- [case notEnoughPrecision](/documentation/applicationservices/axerror/notenoughprecision)
- [case notImplemented](/documentation/applicationservices/axerror/notimplemented)
- [case notificationAlreadyRegistered](/documentation/applicationservices/axerror/notificationalreadyregistered)
- [case notificationNotRegistered](/documentation/applicationservices/axerror/notificationnotregistered)
- [case notificationUnsupported](/documentation/applicationservices/axerror/notificationunsupported)
- [case parameterizedAttributeUnsupported](/documentation/applicationservices/axerror/parameterizedattributeunsupported)
- [case success](/documentation/applicationservices/axerror/success)
- [AXNotificationConstants.h](/documentation/applicationservices/axnotificationconstants_h)

### Callbacks

- [CFIndex](/documentation/corefoundation/cfindex)

### Constants

- [Miscellaneous Defines](/documentation/applicationservices/axnotificationconstants_h/miscellaneous_defines)

#### Constants

- [var kAXAnnouncementKey: String](/documentation/applicationservices/kaxannouncementkey)
- [var kAXAnnouncementRequestedNotification: String](/documentation/applicationservices/kaxannouncementrequestednotification)
- [var kAXApplicationActivatedNotification: String](/documentation/applicationservices/kaxapplicationactivatednotification)
- [var kAXApplicationDeactivatedNotification: String](/documentation/applicationservices/kaxapplicationdeactivatednotification)
- [var kAXApplicationHiddenNotification: String](/documentation/applicationservices/kaxapplicationhiddennotification)
- [var kAXApplicationShownNotification: String](/documentation/applicationservices/kaxapplicationshownnotification)
- [var kAXCreatedNotification: String](/documentation/applicationservices/kaxcreatednotification)
- [var kAXDrawerCreatedNotification: String](/documentation/applicationservices/kaxdrawercreatednotification)
- [var kAXFocusedUIElementChangedNotification: String](/documentation/applicationservices/kaxfocuseduielementchangednotification)
- [var kAXFocusedWindowChangedNotification: String](/documentation/applicationservices/kaxfocusedwindowchangednotification)
- [var kAXHelpTagCreatedNotification: String](/documentation/applicationservices/kaxhelptagcreatednotification)
- [var kAXLayoutChangedNotification: String](/documentation/applicationservices/kaxlayoutchangednotification)
- [var kAXMainWindowChangedNotification: String](/documentation/applicationservices/kaxmainwindowchangednotification)
- [var kAXMenuClosedNotification: String](/documentation/applicationservices/kaxmenuclosednotification)
- [var kAXMenuItemSelectedNotification: String](/documentation/applicationservices/kaxmenuitemselectednotification)
- [var kAXMenuOpenedNotification: String](/documentation/applicationservices/kaxmenuopenednotification)
- [var kAXMovedNotification: String](/documentation/applicationservices/kaxmovednotification)
- [var kAXPriorityKey: String](/documentation/applicationservices/kaxprioritykey)
- [var kAXResizedNotification: String](/documentation/applicationservices/kaxresizednotification)
- [var kAXRowCollapsedNotification: String](/documentation/applicationservices/kaxrowcollapsednotification)
- [var kAXRowCountChangedNotification: String](/documentation/applicationservices/kaxrowcountchangednotification)
- [var kAXRowExpandedNotification: String](/documentation/applicationservices/kaxrowexpandednotification)
- [var kAXSelectedCellsChangedNotification: String](/documentation/applicationservices/kaxselectedcellschangednotification)
- [var kAXSelectedChildrenChangedNotification: String](/documentation/applicationservices/kaxselectedchildrenchangednotification)
- [var kAXSelectedChildrenMovedNotification: String](/documentation/applicationservices/kaxselectedchildrenmovednotification)
- [var kAXSelectedColumnsChangedNotification: String](/documentation/applicationservices/kaxselectedcolumnschangednotification)
- [var kAXSelectedRowsChangedNotification: String](/documentation/applicationservices/kaxselectedrowschangednotification)
- [var kAXSelectedTextChangedNotification: String](/documentation/applicationservices/kaxselectedtextchangednotification)
- [var kAXSheetCreatedNotification: String](/documentation/applicationservices/kaxsheetcreatednotification)
- [var kAXTitleChangedNotification: String](/documentation/applicationservices/kaxtitlechangednotification)
- [var kAXUIElementDestroyedNotification: String](/documentation/applicationservices/kaxuielementdestroyednotification)
- [var kAXUIElementsKey: String](/documentation/applicationservices/kaxuielementskey)
- [var kAXUnitsChangedNotification: String](/documentation/applicationservices/kaxunitschangednotification)
- [var kAXValueChangedNotification: String](/documentation/applicationservices/kaxvaluechangednotification)
- [var kAXWindowCreatedNotification: String](/documentation/applicationservices/kaxwindowcreatednotification)
- [var kAXWindowDeminiaturizedNotification: String](/documentation/applicationservices/kaxwindowdeminiaturizednotification)
- [var kAXWindowMiniaturizedNotification: String](/documentation/applicationservices/kaxwindowminiaturizednotification)
- [var kAXWindowMovedNotification: String](/documentation/applicationservices/kaxwindowmovednotification)
- [var kAXWindowResizedNotification: String](/documentation/applicationservices/kaxwindowresizednotification)
- [AXRoleConstants.h](/documentation/applicationservices/axroleconstants_h)

### Constants

- [Miscellaneous Defines](/documentation/applicationservices/axroleconstants_h/miscellaneous_defines)

#### Constants

- [var kAXApplicationRole: String](/documentation/applicationservices/kaxapplicationrole)
- [var kAXBrowserRole: String](/documentation/applicationservices/kaxbrowserrole)
- [var kAXButtonRole: String](/documentation/applicationservices/kaxbuttonrole)
- [var kAXCheckBoxRole: String](/documentation/applicationservices/kaxcheckboxrole)
- [var kAXColumnRole: String](/documentation/applicationservices/kaxcolumnrole)
- [var kAXDrawerRole: String](/documentation/applicationservices/kaxdrawerrole)
- [var kAXGrowAreaRole: String](/documentation/applicationservices/kaxgrowarearole)
- [var kAXImageRole: String](/documentation/applicationservices/kaximagerole)
- [var kAXMenuButtonRole: String](/documentation/applicationservices/kaxmenubuttonrole)
- [var kAXOutlineRole: String](/documentation/applicationservices/kaxoutlinerole)
- [var kAXPopUpButtonRole: String](/documentation/applicationservices/kaxpopupbuttonrole)
- [var kAXRadioButtonRole: String](/documentation/applicationservices/kaxradiobuttonrole)
- [var kAXRowRole: String](/documentation/applicationservices/kaxrowrole)
- [var kAXSheetRole: String](/documentation/applicationservices/kaxsheetrole)
- [var kAXSystemWideRole: String](/documentation/applicationservices/kaxsystemwiderole)
- [var kAXTabGroupRole: String](/documentation/applicationservices/kaxtabgrouprole)
- [var kAXTableRole: String](/documentation/applicationservices/kaxtablerole)
- [var kAXUnknownRole: String](/documentation/applicationservices/kaxunknownrole)
- [var kAXWindowRole: String](/documentation/applicationservices/kaxwindowrole)
- [AXTextAttributedString.h](/documentation/applicationservices/axtextattributedstring_h)

### Constants

- [Global Variables](/documentation/applicationservices/axtextattributedstring_h/global_variables)

#### Constants

- [var kAXAttachmentTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxattachmenttextattribute)
- [var kAXAutocorrectedTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxautocorrectedtextattribute)
- [var kAXBackgroundColorTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxbackgroundcolortextattribute)
- [var kAXFontFamilyKey: Unmanaged<CFString>](/documentation/applicationservices/kaxfontfamilykey)
- [var kAXFontNameKey: Unmanaged<CFString>](/documentation/applicationservices/kaxfontnamekey)
- [var kAXFontSizeKey: Unmanaged<CFString>](/documentation/applicationservices/kaxfontsizekey)
- [var kAXFontTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxfonttextattribute)
- [var kAXForegroundColorTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxforegroundcolortextattribute)
- [var kAXLinkTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxlinktextattribute)
- [var kAXMarkedMisspelledTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxmarkedmisspelledtextattribute)
- [var kAXMisspelledTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxmisspelledtextattribute)
- [var kAXNaturalLanguageTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxnaturallanguagetextattribute)
- [var kAXReplacementStringTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxreplacementstringtextattribute)
- [var kAXShadowTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxshadowtextattribute)
- [var kAXStrikethroughColorTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxstrikethroughcolortextattribute)
- [var kAXStrikethroughTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxstrikethroughtextattribute)
- [var kAXSuperscriptTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxsuperscripttextattribute)
- [var kAXUnderlineColorTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxunderlinecolortextattribute)
- [var kAXUnderlineTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxunderlinetextattribute)
- [var kAXVisibleNameKey: Unmanaged<CFString>](/documentation/applicationservices/kaxvisiblenamekey)
- [AXUnderlineStyle](/documentation/applicationservices/axunderlinestyle)

#### Enumeration Cases

- [case double](/documentation/applicationservices/axunderlinestyle/double)
- [case none](/documentation/applicationservices/axunderlinestyle/none)
- [case single](/documentation/applicationservices/axunderlinestyle/single)
- [case thick](/documentation/applicationservices/axunderlinestyle/thick)
- [AXUIElement.h](/documentation/applicationservices/axuielement_h)

### Notification API

- [func AXObserverAddNotification(AXObserver, AXUIElement, CFString, UnsafeMutableRawPointer?) -> AXError](/documentation/applicationservices/1462089-axobserveraddnotification)
- [func AXObserverCreate(pid_t, AXObserverCallback, UnsafeMutablePointer<AXObserver?>) -> AXError](/documentation/applicationservices/1460133-axobservercreate)
- [func AXObserverCreateWithInfoCallback(pid_t, AXObserverCallbackWithInfo, UnsafeMutablePointer<AXObserver?>) -> AXError](/documentation/applicationservices/1460610-axobservercreatewithinfocallback)
- [func AXObserverGetRunLoopSource(AXObserver) -> CFRunLoopSource](/documentation/applicationservices/1459139-axobservergetrunloopsource)
- [func AXObserverGetTypeID() -> CFTypeID](/documentation/applicationservices/1461244-axobservergettypeid)
- [func AXObserverRemoveNotification(AXObserver, AXUIElement, CFString) -> AXError](/documentation/applicationservices/1462066-axobserverremovenotification)

### Miscellaneous

- [func AXIsProcessTrusted() -> Bool](/documentation/applicationservices/1460720-axisprocesstrusted)
- [func AXIsProcessTrustedWithOptions(CFDictionary?) -> Bool](/documentation/applicationservices/1459186-axisprocesstrustedwithoptions)
- [func AXUIElementCopyActionDescription(AXUIElement, CFString, UnsafeMutablePointer<CFString?>) -> AXError](/documentation/applicationservices/1462075-axuielementcopyactiondescription)
- [func AXUIElementCopyActionNames(AXUIElement, UnsafeMutablePointer<CFArray?>) -> AXError](/documentation/applicationservices/1462053-axuielementcopyactionnames)
- [func AXUIElementCopyAttributeNames(AXUIElement, UnsafeMutablePointer<CFArray?>) -> AXError](/documentation/applicationservices/1459475-axuielementcopyattributenames)
- [func AXUIElementCopyAttributeValue(AXUIElement, CFString, UnsafeMutablePointer<CFTypeRef?>) -> AXError](/documentation/applicationservices/1462085-axuielementcopyattributevalue)
- [func AXUIElementCopyAttributeValues(AXUIElement, CFString, CFIndex, CFIndex, UnsafeMutablePointer<CFArray?>) -> AXError](/documentation/applicationservices/1462060-axuielementcopyattributevalues)
- [func AXUIElementCopyElementAtPosition(AXUIElement, Float, Float, UnsafeMutablePointer<AXUIElement?>) -> AXError](/documentation/applicationservices/1462077-axuielementcopyelementatposition)
- [func AXUIElementCopyMultipleAttributeValues(AXUIElement, CFArray, AXCopyMultipleAttributeOptions, UnsafeMutablePointer<CFArray?>) -> AXError](/documentation/applicationservices/1462051-axuielementcopymultipleattribute)
- [func AXUIElementCopyParameterizedAttributeNames(AXUIElement, UnsafeMutablePointer<CFArray?>) -> AXError](/documentation/applicationservices/1458783-axuielementcopyparameterizedattr)
- [func AXUIElementCopyParameterizedAttributeValue(AXUIElement, CFString, CFTypeRef, UnsafeMutablePointer<CFTypeRef?>) -> AXError](/documentation/applicationservices/1461203-axuielementcopyparameterizedattr)
- [func AXUIElementCreateApplication(pid_t) -> AXUIElement](/documentation/applicationservices/1459374-axuielementcreateapplication)
- [func AXUIElementCreateSystemWide() -> AXUIElement](/documentation/applicationservices/1462095-axuielementcreatesystemwide)
- [func AXUIElementGetAttributeValueCount(AXUIElement, CFString, UnsafeMutablePointer<CFIndex>) -> AXError](/documentation/applicationservices/1459066-axuielementgetattributevaluecoun)
- [func AXUIElementGetPid(AXUIElement, UnsafeMutablePointer<pid_t>) -> AXError](/documentation/applicationservices/1460337-axuielementgetpid)
- [func AXUIElementGetTypeID() -> CFTypeID](/documentation/applicationservices/1460085-axuielementgettypeid)
- [func AXUIElementIsAttributeSettable(AXUIElement, CFString, UnsafeMutablePointer<DarwinBoolean>) -> AXError](/documentation/applicationservices/1459972-axuielementisattributesettable)
- [func AXUIElementPerformAction(AXUIElement, CFString) -> AXError](/documentation/applicationservices/1462091-axuielementperformaction)
- [func AXUIElementSetAttributeValue(AXUIElement, CFString, CFTypeRef) -> AXError](/documentation/applicationservices/1460434-axuielementsetattributevalue)
- [func AXUIElementSetMessagingTimeout(AXUIElement, Float) -> AXError](/documentation/applicationservices/1459345-axuielementsetmessagingtimeout)

### Callbacks

- [AXObserverCallback](/documentation/applicationservices/axobservercallback)
- [AXObserverCallbackWithInfo](/documentation/applicationservices/axobservercallbackwithinfo)

### Data Types

- [AXCopyMultipleAttributeOptions](/documentation/applicationservices/axcopymultipleattributeoptions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/applicationservices/axcopymultipleattributeoptions/1459579-init)

#### Type Properties

- [static var stopOnError: AXCopyMultipleAttributeOptions](/documentation/applicationservices/axcopymultipleattributeoptions/1460788-stoponerror)
- [AXObserver](/documentation/applicationservices/axobserver)
- [AXUIElement](/documentation/applicationservices/axuielement)
- [AXValue.h](/documentation/applicationservices/axvalue_h)

### Miscellaneous

- [func AXValueCreate(AXValueType, UnsafeRawPointer) -> AXValue?](/documentation/applicationservices/1459351-axvaluecreate)
- [func AXValueGetType(AXValue) -> AXValueType](/documentation/applicationservices/1460911-axvaluegettype)
- [func AXValueGetTypeID() -> CFTypeID](/documentation/applicationservices/1460780-axvaluegettypeid)
- [func AXValueGetValue(AXValue, AXValueType, UnsafeMutableRawPointer) -> Bool](/documentation/applicationservices/1462933-axvaluegetvalue)

### Data Types

- [AXValue](/documentation/applicationservices/axvalue)
- [AXValueType](/documentation/applicationservices/axvaluetype)

#### Constants

- [kAXValueCGPointType](/documentation/applicationservices/axvaluetype/kaxvaluecgpointtype)
- [kAXValueCGSizeType](/documentation/applicationservices/axvaluetype/kaxvaluecgsizetype)
- [kAXValueCGRectType](/documentation/applicationservices/axvaluetype/kaxvaluecgrecttype)
- [kAXValueCFRangeType](/documentation/applicationservices/axvaluetype/kaxvaluecfrangetype)
- [kAXValueAXErrorType](/documentation/applicationservices/axvaluetype/kaxvalueaxerrortype)
- [kAXValueIllegalType](/documentation/applicationservices/axvaluetype/kaxvalueillegaltype)

#### Enumeration Cases

- [case axError](/documentation/applicationservices/axvaluetype/axerror)
- [case cfRange](/documentation/applicationservices/axvaluetype/cfrange)
- [case cgPoint](/documentation/applicationservices/axvaluetype/cgpoint)
- [case cgRect](/documentation/applicationservices/axvaluetype/cgrect)
- [case cgSize](/documentation/applicationservices/axvaluetype/cgsize)
- [case illegal](/documentation/applicationservices/axvaluetype/illegal)
- [AXValueConstants.h](/documentation/applicationservices/axvalueconstants_h)

### Constants

- [Miscellaneous Defines](/documentation/applicationservices/axvalueconstants_h/miscellaneous_defines)

#### Constants

- [var kAXAscendingSortDirectionValue: String](/documentation/applicationservices/kaxascendingsortdirectionvalue)
- [var kAXDescendingSortDirectionValue: String](/documentation/applicationservices/kaxdescendingsortdirectionvalue)
- [var kAXHorizontalOrientationValue: String](/documentation/applicationservices/kaxhorizontalorientationvalue)
- [var kAXUnknownOrientationValue: String](/documentation/applicationservices/kaxunknownorientationvalue)
- [var kAXUnknownSortDirectionValue: String](/documentation/applicationservices/kaxunknownsortdirectionvalue)
- [var kAXVerticalOrientationValue: String](/documentation/applicationservices/kaxverticalorientationvalue)
- [UniversalAccess.h](/documentation/applicationservices/universalaccess_h)

### Miscellaneous

- [func UAZoomChangeFocus(UnsafePointer<CGRect>!, UnsafePointer<CGRect>!, UAZoomChangeFocusType) -> OSStatus](/documentation/applicationservices/1458830-uazoomchangefocus)
- [func UAZoomEnabled() -> Bool](/documentation/applicationservices/1462288-uazoomenabled)

### Data Types

- [UAZoomChangeFocusType](/documentation/applicationservices/uazoomchangefocustype)

### Constants

- [UAZoomFocusTypes](/documentation/applicationservices/universalaccess_h/1553162-uazoomfocustypes)

#### Constants

- [var kUAZoomFocusTypeOther: Int](/documentation/applicationservices/kuazoomfocustypeother)
- [var kUAZoomFocusTypeInsertionPoint: Int](/documentation/applicationservices/kuazoomfocustypeinsertionpoint)
- [ApplicationServices Structures](/documentation/applicationservices/applicationservices_structures)

### Structures

- [ATSFSSpec](/documentation/applicationservices/atsfsspec)

#### Initializers

- [init()](/documentation/applicationservices/atsfsspec/1461552-init)
- [init(vRefNum: FSVolumeRefNum, parID: Int32, name: StrFileName)](/documentation/applicationservices/atsfsspec/1463783-init)

#### Instance Properties

- [var name: StrFileName](/documentation/applicationservices/atsfsspec/1460126-name)
- [var parID: Int32](/documentation/applicationservices/atsfsspec/1459119-parid)
- [var vRefNum: FSVolumeRefNum](/documentation/applicationservices/atsfsspec/1459405-vrefnum)
- [ATSFlatDataFontNameDataHeader](/documentation/applicationservices/atsflatdatafontnamedataheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatafontnamedataheader/1464214-init)
- [init(nameSpecifierType: ATSFlatDataFontSpeciferType, nameSpecifierSize: UInt32)](/documentation/applicationservices/atsflatdatafontnamedataheader/1463521-init)

#### Instance Properties

- [var nameSpecifierSize: UInt32](/documentation/applicationservices/atsflatdatafontnamedataheader/1462952-namespecifiersize)
- [var nameSpecifierType: ATSFlatDataFontSpeciferType](/documentation/applicationservices/atsflatdatafontnamedataheader/1460209-namespecifiertype)
- [ATSFlatDataFontSpecRawNameData](/documentation/applicationservices/atsflatdatafontspecrawnamedata)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatafontspecrawnamedata/1464240-init)
- [init(fontNameType: FontNameCode, fontNamePlatform: FontPlatformCode, fontNameScript: FontScriptCode, fontNameLanguage: FontLanguageCode, fontNameLength: UInt32)](/documentation/applicationservices/atsflatdatafontspecrawnamedata/1464806-init)

#### Instance Properties

- [var fontNameLanguage: FontLanguageCode](/documentation/applicationservices/atsflatdatafontspecrawnamedata/1460770-fontnamelanguage)
- [var fontNameLength: UInt32](/documentation/applicationservices/atsflatdatafontspecrawnamedata/1459401-fontnamelength)
- [var fontNamePlatform: FontPlatformCode](/documentation/applicationservices/atsflatdatafontspecrawnamedata/1460968-fontnameplatform)
- [var fontNameScript: FontScriptCode](/documentation/applicationservices/atsflatdatafontspecrawnamedata/1461188-fontnamescript)
- [var fontNameType: FontNameCode](/documentation/applicationservices/atsflatdatafontspecrawnamedata/1462901-fontnametype)
- [ATSFlatDataFontSpecRawNameDataHeader](/documentation/applicationservices/atsflatdatafontspecrawnamedataheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatafontspecrawnamedataheader/1462957-init)
- [init(numberOfFlattenedNames: UInt32, nameDataArray: ATSFlatDataFontSpecRawNameData)](/documentation/applicationservices/atsflatdatafontspecrawnamedataheader/1459561-init)

#### Instance Properties

- [var nameDataArray: ATSFlatDataFontSpecRawNameData](/documentation/applicationservices/atsflatdatafontspecrawnamedataheader/1463817-namedataarray)
- [var numberOfFlattenedNames: UInt32](/documentation/applicationservices/atsflatdatafontspecrawnamedataheader/1459137-numberofflattenednames)
- [ATSFlatDataLayoutControlsDataHeader](/documentation/applicationservices/atsflatdatalayoutcontrolsdataheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatalayoutcontrolsdataheader/1458894-init)
- [init(numberOfLayoutControls: UInt32, controlArray: ATSUAttributeInfo)](/documentation/applicationservices/atsflatdatalayoutcontrolsdataheader/1461981-init)

#### Instance Properties

- [var controlArray: ATSUAttributeInfo](/documentation/applicationservices/atsflatdatalayoutcontrolsdataheader/1461055-controlarray)
- [var numberOfLayoutControls: UInt32](/documentation/applicationservices/atsflatdatalayoutcontrolsdataheader/1460030-numberoflayoutcontrols)
- [ATSFlatDataLineInfoData](/documentation/applicationservices/atsflatdatalineinfodata)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatalineinfodata/1461454-init)
- [init(lineLength: UInt32, numberOfLineControls: UInt32)](/documentation/applicationservices/atsflatdatalineinfodata/1462859-init)

#### Instance Properties

- [var lineLength: UInt32](/documentation/applicationservices/atsflatdatalineinfodata/1462995-linelength)
- [var numberOfLineControls: UInt32](/documentation/applicationservices/atsflatdatalineinfodata/1460103-numberoflinecontrols)
- [ATSFlatDataLineInfoHeader](/documentation/applicationservices/atsflatdatalineinfoheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatalineinfoheader/1462389-init)
- [init(numberOfLines: UInt32, lineInfoArray: ATSFlatDataLineInfoData)](/documentation/applicationservices/atsflatdatalineinfoheader/1464577-init)

#### Instance Properties

- [var lineInfoArray: ATSFlatDataLineInfoData](/documentation/applicationservices/atsflatdatalineinfoheader/1458798-lineinfoarray)
- [var numberOfLines: UInt32](/documentation/applicationservices/atsflatdatalineinfoheader/1461905-numberoflines)
- [ATSFlatDataMainHeaderBlock](/documentation/applicationservices/atsflatdatamainheaderblock)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatamainheaderblock/1460379-init)
- [init(version: UInt32, sizeOfDataBlock: UInt32, offsetToTextLayouts: UInt32, offsetToStyleRuns: UInt32, offsetToStyleList: UInt32)](/documentation/applicationservices/atsflatdatamainheaderblock/1461857-init)

#### Instance Properties

- [var offsetToStyleList: UInt32](/documentation/applicationservices/atsflatdatamainheaderblock/1458944-offsettostylelist)
- [var offsetToStyleRuns: UInt32](/documentation/applicationservices/atsflatdatamainheaderblock/1463892-offsettostyleruns)
- [var offsetToTextLayouts: UInt32](/documentation/applicationservices/atsflatdatamainheaderblock/1458901-offsettotextlayouts)
- [var sizeOfDataBlock: UInt32](/documentation/applicationservices/atsflatdatamainheaderblock/1464208-sizeofdatablock)
- [var version: UInt32](/documentation/applicationservices/atsflatdatamainheaderblock/1460451-version)
- [ATSFlatDataStyleListFeatureData](/documentation/applicationservices/atsflatdatastylelistfeaturedata)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatastylelistfeaturedata/1459027-init)
- [init(theFeatureType: ATSUFontFeatureType, theFeatureSelector: ATSUFontFeatureSelector)](/documentation/applicationservices/atsflatdatastylelistfeaturedata/1463856-init)

#### Instance Properties

- [var theFeatureSelector: ATSUFontFeatureSelector](/documentation/applicationservices/atsflatdatastylelistfeaturedata/1461688-thefeatureselector)
- [var theFeatureType: ATSUFontFeatureType](/documentation/applicationservices/atsflatdatastylelistfeaturedata/1461496-thefeaturetype)
- [ATSFlatDataStyleListHeader](/documentation/applicationservices/atsflatdatastylelistheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatastylelistheader/1461739-init)
- [init(numberOfStyles: UInt32, styleDataArray: ATSFlatDataStyleListStyleDataHeader)](/documentation/applicationservices/atsflatdatastylelistheader/1462628-init)

#### Instance Properties

- [var numberOfStyles: UInt32](/documentation/applicationservices/atsflatdatastylelistheader/1459380-numberofstyles)
- [var styleDataArray: ATSFlatDataStyleListStyleDataHeader](/documentation/applicationservices/atsflatdatastylelistheader/1463390-styledataarray)
- [ATSFlatDataStyleListStyleDataHeader](/documentation/applicationservices/atsflatdatastyleliststyledataheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatastyleliststyledataheader/1464591-init)
- [init(sizeOfStyleInfo: UInt32, numberOfSetAttributes: UInt32, numberOfSetFeatures: UInt32, numberOfSetVariations: UInt32)](/documentation/applicationservices/atsflatdatastyleliststyledataheader/1461742-init)

#### Instance Properties

- [var numberOfSetAttributes: UInt32](/documentation/applicationservices/atsflatdatastyleliststyledataheader/1462751-numberofsetattributes)
- [var numberOfSetFeatures: UInt32](/documentation/applicationservices/atsflatdatastyleliststyledataheader/1458791-numberofsetfeatures)
- [var numberOfSetVariations: UInt32](/documentation/applicationservices/atsflatdatastyleliststyledataheader/1459725-numberofsetvariations)
- [var sizeOfStyleInfo: UInt32](/documentation/applicationservices/atsflatdatastyleliststyledataheader/1463190-sizeofstyleinfo)
- [ATSFlatDataStyleListVariationData](/documentation/applicationservices/atsflatdatastylelistvariationdata)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatastylelistvariationdata/1460818-init)
- [init(theVariationAxis: ATSUFontVariationAxis, theVariationValue: ATSUFontVariationValue)](/documentation/applicationservices/atsflatdatastylelistvariationdata/1462840-init)

#### Instance Properties

- [var theVariationAxis: ATSUFontVariationAxis](/documentation/applicationservices/atsflatdatastylelistvariationdata/1459497-thevariationaxis)
- [var theVariationValue: ATSUFontVariationValue](/documentation/applicationservices/atsflatdatastylelistvariationdata/1458824-thevariationvalue)
- [ATSFlatDataStyleRunDataHeader](/documentation/applicationservices/atsflatdatastylerundataheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatastylerundataheader/1460360-init)
- [init(numberOfStyleRuns: UInt32, styleRunArray: ATSUStyleRunInfo)](/documentation/applicationservices/atsflatdatastylerundataheader/1461196-init)

#### Instance Properties

- [var numberOfStyleRuns: UInt32](/documentation/applicationservices/atsflatdatastylerundataheader/1464504-numberofstyleruns)
- [var styleRunArray: ATSUStyleRunInfo](/documentation/applicationservices/atsflatdatastylerundataheader/1460053-stylerunarray)
- [ATSFlatDataTextLayoutDataHeader](/documentation/applicationservices/atsflatdatatextlayoutdataheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatatextlayoutdataheader/1459230-init)
- [init(sizeOfLayoutData: UInt32, textLayoutLength: UInt32, offsetToLayoutControls: UInt32, offsetToLineInfo: UInt32)](/documentation/applicationservices/atsflatdatatextlayoutdataheader/1463703-init)

#### Instance Properties

- [var offsetToLayoutControls: UInt32](/documentation/applicationservices/atsflatdatatextlayoutdataheader/1459348-offsettolayoutcontrols)
- [var offsetToLineInfo: UInt32](/documentation/applicationservices/atsflatdatatextlayoutdataheader/1461794-offsettolineinfo)
- [var sizeOfLayoutData: UInt32](/documentation/applicationservices/atsflatdatatextlayoutdataheader/1462613-sizeoflayoutdata)
- [var textLayoutLength: UInt32](/documentation/applicationservices/atsflatdatatextlayoutdataheader/1459534-textlayoutlength)
- [ATSFlatDataTextLayoutHeader](/documentation/applicationservices/atsflatdatatextlayoutheader)

#### Initializers

- [init()](/documentation/applicationservices/atsflatdatatextlayoutheader/1464272-init)
- [init(numFlattenedTextLayouts: UInt32, flattenedTextLayouts: ATSFlatDataTextLayoutDataHeader)](/documentation/applicationservices/atsflatdatatextlayoutheader/1464280-init)

#### Instance Properties

- [var flattenedTextLayouts: ATSFlatDataTextLayoutDataHeader](/documentation/applicationservices/atsflatdatatextlayoutheader/1463120-flattenedtextlayouts)
- [var numFlattenedTextLayouts: UInt32](/documentation/applicationservices/atsflatdatatextlayoutheader/1460854-numflattenedtextlayouts)
- [ATSFontFilter](/documentation/applicationservices/atsfontfilter)

#### Initializers

- [init()](/documentation/applicationservices/atsfontfilter/1464606-init)
- [init(version: UInt32, filterSelector: ATSFontFilterSelector, filter: ATSFontFilter.__Unnamed_union_filter)](/documentation/applicationservices/atsfontfilter/1463749-init)

#### Instance Properties

- [var filter: ATSFontFilter.__Unnamed_union_filter](/documentation/applicationservices/atsfontfilter/1459868-filter)
- [var filterSelector: ATSFontFilterSelector](/documentation/applicationservices/atsfontfilter/1462340-filterselector)
- [var version: UInt32](/documentation/applicationservices/atsfontfilter/1459521-version)
- [ATSFontFilterSelector](/documentation/applicationservices/atsfontfilterselector)

#### Initializers

- [init(UInt32)](/documentation/applicationservices/atsfontfilterselector/1461500-init)
- [init(rawValue: UInt32)](/documentation/applicationservices/atsfontfilterselector/1464100-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/applicationservices/atsfontfilterselector/1462941-rawvalue)
- [ATSFontMetrics](/documentation/applicationservices/atsfontmetrics)

#### Initializers

- [init()](/documentation/applicationservices/atsfontmetrics/1462411-init)
- [init(version: UInt32, ascent: CGFloat, descent: CGFloat, leading: CGFloat, avgAdvanceWidth: CGFloat, maxAdvanceWidth: CGFloat, minLeftSideBearing: CGFloat, minRightSideBearing: CGFloat, stemWidth: CGFloat, stemHeight: CGFloat, capHeight: CGFloat, xHeight: CGFloat, italicAngle: CGFloat, underlinePosition: CGFloat, underlineThickness: CGFloat)](/documentation/applicationservices/atsfontmetrics/1460253-init)

#### Instance Properties

- [var ascent: CGFloat](/documentation/applicationservices/atsfontmetrics/1463007-ascent)
- [var avgAdvanceWidth: CGFloat](/documentation/applicationservices/atsfontmetrics/1459981-avgadvancewidth)
- [var capHeight: CGFloat](/documentation/applicationservices/atsfontmetrics/1464044-capheight)
- [var descent: CGFloat](/documentation/applicationservices/atsfontmetrics/1464751-descent)
- [var italicAngle: CGFloat](/documentation/applicationservices/atsfontmetrics/1461100-italicangle)
- [var leading: CGFloat](/documentation/applicationservices/atsfontmetrics/1463751-leading)
- [var maxAdvanceWidth: CGFloat](/documentation/applicationservices/atsfontmetrics/1462606-maxadvancewidth)
- [var minLeftSideBearing: CGFloat](/documentation/applicationservices/atsfontmetrics/1461606-minleftsidebearing)
- [var minRightSideBearing: CGFloat](/documentation/applicationservices/atsfontmetrics/1459984-minrightsidebearing)
- [var stemHeight: CGFloat](/documentation/applicationservices/atsfontmetrics/1464042-stemheight)
- [var stemWidth: CGFloat](/documentation/applicationservices/atsfontmetrics/1462806-stemwidth)
- [var underlinePosition: CGFloat](/documentation/applicationservices/atsfontmetrics/1461458-underlineposition)
- [var underlineThickness: CGFloat](/documentation/applicationservices/atsfontmetrics/1463727-underlinethickness)
- [var version: UInt32](/documentation/applicationservices/atsfontmetrics/1460836-version)
- [var xHeight: CGFloat](/documentation/applicationservices/atsfontmetrics/1464396-xheight)
- [ATSFontNotifyAction](/documentation/applicationservices/atsfontnotifyaction)

#### Initializers

- [init(UInt32)](/documentation/applicationservices/atsfontnotifyaction/1462300-init)
- [init(rawValue: UInt32)](/documentation/applicationservices/atsfontnotifyaction/1458772-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/applicationservices/atsfontnotifyaction/1460117-rawvalue)
- [ATSFontNotifyOption](/documentation/applicationservices/atsfontnotifyoption)

#### Initializers

- [init(UInt32)](/documentation/applicationservices/atsfontnotifyoption/1464537-init)
- [init(rawValue: UInt32)](/documentation/applicationservices/atsfontnotifyoption/1463214-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/applicationservices/atsfontnotifyoption/1460764-rawvalue)
- [ATSFontQueryMessageID](/documentation/applicationservices/atsfontquerymessageid)

#### Initializers

- [init(UInt32)](/documentation/applicationservices/atsfontquerymessageid/1464198-init)
- [init(rawValue: UInt32)](/documentation/applicationservices/atsfontquerymessageid/1459713-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/applicationservices/atsfontquerymessageid/1461661-rawvalue)
- [ATSFontQuerySourceContext](/documentation/applicationservices/atsfontquerysourcecontext)

#### Initializers

- [init()](/documentation/applicationservices/atsfontquerysourcecontext/1460069-init)
- [init(version: UInt32, refCon: UnsafeMutableRawPointer!, retain: CFAllocatorRetainCallBack!, release: CFAllocatorReleaseCallBack!)](/documentation/applicationservices/atsfontquerysourcecontext/1778162-init)

#### Instance Properties

- [var refCon: UnsafeMutableRawPointer!](/documentation/applicationservices/atsfontquerysourcecontext/1461013-refcon)
- [var release: CFAllocatorReleaseCallBack!](/documentation/applicationservices/atsfontquerysourcecontext/1460736-release)
- [var retain: CFAllocatorRetainCallBack!](/documentation/applicationservices/atsfontquerysourcecontext/1463355-retain)
- [var version: UInt32](/documentation/applicationservices/atsfontquerysourcecontext/1464515-version)
- [ATSGlyphIdealMetrics](/documentation/applicationservices/atsglyphidealmetrics)

#### Initializers

- [init()](/documentation/applicationservices/atsglyphidealmetrics/1463112-init)
- [init(advance: ATSPoint, sideBearing: ATSPoint, otherSideBearing: ATSPoint)](/documentation/applicationservices/atsglyphidealmetrics/1463284-init)

#### Instance Properties

- [var advance: ATSPoint](/documentation/applicationservices/atsglyphidealmetrics/1459461-advance)
- [var otherSideBearing: ATSPoint](/documentation/applicationservices/atsglyphidealmetrics/1460692-othersidebearing)
- [var sideBearing: ATSPoint](/documentation/applicationservices/atsglyphidealmetrics/1460251-sidebearing)
- [ATSGlyphScreenMetrics](/documentation/applicationservices/atsglyphscreenmetrics)

#### Initializers

- [init()](/documentation/applicationservices/atsglyphscreenmetrics/1459655-init)
- [init(deviceAdvance: ATSPoint, topLeft: ATSPoint, height: UInt32, width: UInt32, sideBearing: ATSPoint, otherSideBearing: ATSPoint)](/documentation/applicationservices/atsglyphscreenmetrics/1458792-init)

#### Instance Properties

- [var deviceAdvance: ATSPoint](/documentation/applicationservices/atsglyphscreenmetrics/1463647-deviceadvance)
- [var height: UInt32](/documentation/applicationservices/atsglyphscreenmetrics/1461550-height)
- [var otherSideBearing: ATSPoint](/documentation/applicationservices/atsglyphscreenmetrics/1460147-othersidebearing)
- [var sideBearing: ATSPoint](/documentation/applicationservices/atsglyphscreenmetrics/1461192-sidebearing)
- [var topLeft: ATSPoint](/documentation/applicationservices/atsglyphscreenmetrics/1461460-topleft)
- [var width: UInt32](/documentation/applicationservices/atsglyphscreenmetrics/1458790-width)
- [ATSJustWidthDeltaEntryOverride](/documentation/applicationservices/atsjustwidthdeltaentryoverride)

#### Initializers

- [init()](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1462175-init)
- [init(beforeGrowLimit: Fixed, beforeShrinkLimit: Fixed, afterGrowLimit: Fixed, afterShrinkLimit: Fixed, growFlags: JustificationFlags, shrinkFlags: JustificationFlags)](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1458778-init)

#### Instance Properties

- [var afterGrowLimit: Fixed](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1462046-aftergrowlimit)
- [var afterShrinkLimit: Fixed](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1460699-aftershrinklimit)
- [var beforeGrowLimit: Fixed](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1464220-beforegrowlimit)
- [var beforeShrinkLimit: Fixed](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1459567-beforeshrinklimit)
- [var growFlags: JustificationFlags](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1459465-growflags)
- [var shrinkFlags: JustificationFlags](/documentation/applicationservices/atsjustwidthdeltaentryoverride/1464744-shrinkflags)
- [ATSLayoutRecord](/documentation/applicationservices/atslayoutrecord)

#### Initializers

- [init()](/documentation/applicationservices/atslayoutrecord/1462838-init)
- [init(glyphID: ATSGlyphRef, flags: ATSGlyphInfoFlags, originalOffset: Int, realPos: Fixed)](/documentation/applicationservices/atslayoutrecord/1462040-init)

#### Instance Properties

- [var flags: ATSGlyphInfoFlags](/documentation/applicationservices/atslayoutrecord/1460040-flags)
- [var glyphID: ATSGlyphRef](/documentation/applicationservices/atslayoutrecord/1464040-glyphid)
- [var originalOffset: Int](/documentation/applicationservices/atslayoutrecord/1462059-originaloffset)
- [var realPos: Fixed](/documentation/applicationservices/atslayoutrecord/1462194-realpos)
- [ATSTrapezoid](/documentation/applicationservices/atstrapezoid)

#### Initializers

- [init()](/documentation/applicationservices/atstrapezoid/1462379-init)
- [init(upperLeft: FixedPoint, upperRight: FixedPoint, lowerRight: FixedPoint, lowerLeft: FixedPoint)](/documentation/applicationservices/atstrapezoid/1462513-init)

#### Instance Properties

- [var lowerLeft: FixedPoint](/documentation/applicationservices/atstrapezoid/1460362-lowerleft)
- [var lowerRight: FixedPoint](/documentation/applicationservices/atstrapezoid/1464539-lowerright)
- [var upperLeft: FixedPoint](/documentation/applicationservices/atstrapezoid/1463451-upperleft)
- [var upperRight: FixedPoint](/documentation/applicationservices/atstrapezoid/1464166-upperright)
- [ATSUAttributeInfo](/documentation/applicationservices/atsuattributeinfo)

#### Initializers

- [init()](/documentation/applicationservices/atsuattributeinfo/1458906-init)
- [init(fTag: ATSUAttributeTag, fValueSize: Int)](/documentation/applicationservices/atsuattributeinfo/1462369-init)

#### Instance Properties

- [var fTag: ATSUAttributeTag](/documentation/applicationservices/atsuattributeinfo/1452170-ftag)
- [var fValueSize: Int](/documentation/applicationservices/atsuattributeinfo/1452185-fvaluesize)
- [ATSUBackgroundData](/documentation/applicationservices/atsubackgrounddata)

#### Instance Properties

- [var backgroundColor: ATSUBackgroundColor](/documentation/applicationservices/atsubackgrounddata/1452008-backgroundcolor)
- [var backgroundUPP: RedrawBackgroundUPP!](/documentation/applicationservices/atsubackgrounddata/1452266-backgroundupp)

#### Initializers

- [init()](/documentation/applicationservices/atsubackgrounddata/1461456-init)
- [init(backgroundColor: ATSUBackgroundColor)](/documentation/applicationservices/atsubackgrounddata/1459124-init)
- [init(backgroundUPP: RedrawBackgroundUPP!)](/documentation/applicationservices/atsubackgrounddata/1778161-init)
- [ATSUCaret](/documentation/applicationservices/atsucaret)

#### Initializers

- [init()](/documentation/applicationservices/atsucaret/1461786-init)
- [init(fX: Fixed, fY: Fixed, fDeltaX: Fixed, fDeltaY: Fixed)](/documentation/applicationservices/atsucaret/1464003-init)

#### Instance Properties

- [var fDeltaX: Fixed](/documentation/applicationservices/atsucaret/1452079-fdeltax)
- [var fDeltaY: Fixed](/documentation/applicationservices/atsucaret/1452236-fdeltay)
- [var fX: Fixed](/documentation/applicationservices/atsucaret/1452024-fx)
- [var fY: Fixed](/documentation/applicationservices/atsucaret/1452222-fy)
- [ATSUCurvePath](/documentation/applicationservices/atsucurvepath)

#### Initializers

- [init()](/documentation/applicationservices/atsucurvepath/1462862-init)
- [init(vectors: UInt32, controlBits: UInt32, vector: ATSPoint)](/documentation/applicationservices/atsucurvepath/1459100-init)

#### Instance Properties

- [var controlBits: UInt32](/documentation/applicationservices/atsucurvepath/1463251-controlbits)
- [var vector: ATSPoint](/documentation/applicationservices/atsucurvepath/1461479-vector)
- [var vectors: UInt32](/documentation/applicationservices/atsucurvepath/1462624-vectors)
- [ATSUCurvePaths](/documentation/applicationservices/atsucurvepaths)

#### Initializers

- [init()](/documentation/applicationservices/atsucurvepaths/1459051-init)
- [init(contours: UInt32, contour: ATSUCurvePath)](/documentation/applicationservices/atsucurvepaths/1462590-init)

#### Instance Properties

- [var contour: ATSUCurvePath](/documentation/applicationservices/atsucurvepaths/1461494-contour)
- [var contours: UInt32](/documentation/applicationservices/atsucurvepaths/1460682-contours)
- [ATSUGlyphInfo](/documentation/applicationservices/atsuglyphinfo)

#### Initializers

- [init()](/documentation/applicationservices/atsuglyphinfo/1460092-init)
- [init(glyphID: GlyphID, reserved: UInt16, layoutFlags: UInt32, charIndex: UniCharArrayOffset, style: ATSUStyle!, deltaY: Float32, idealX: Float32, screenX: Int16, caretX: Int16)](/documentation/applicationservices/atsuglyphinfo/1690597-init)

#### Instance Properties

- [var caretX: Int16](/documentation/applicationservices/atsuglyphinfo/1452025-caretx)
- [var charIndex: UniCharArrayOffset](/documentation/applicationservices/atsuglyphinfo/1452119-charindex)
- [var deltaY: Float32](/documentation/applicationservices/atsuglyphinfo/1452001-deltay)
- [var glyphID: GlyphID](/documentation/applicationservices/atsuglyphinfo/1452124-glyphid)
- [var idealX: Float32](/documentation/applicationservices/atsuglyphinfo/1452059-idealx)
- [var layoutFlags: UInt32](/documentation/applicationservices/atsuglyphinfo/1452273-layoutflags)
- [var reserved: UInt16](/documentation/applicationservices/atsuglyphinfo/1452290-reserved)
- [var screenX: Int16](/documentation/applicationservices/atsuglyphinfo/1452183-screenx)
- [var style: ATSUStyle!](/documentation/applicationservices/atsuglyphinfo/1452143-style)
- [ATSUGlyphInfoArray](/documentation/applicationservices/atsuglyphinfoarray)

#### Initializers

- [init()](/documentation/applicationservices/atsuglyphinfoarray/1459409-init)
- [init(layout: ATSUTextLayout!, numGlyphs: Int, glyphs: ATSUGlyphInfo)](/documentation/applicationservices/atsuglyphinfoarray/1690599-init)

#### Instance Properties

- [var glyphs: ATSUGlyphInfo](/documentation/applicationservices/atsuglyphinfoarray/1452027-glyphs)
- [var layout: ATSUTextLayout!](/documentation/applicationservices/atsuglyphinfoarray/1452037-layout)
- [var numGlyphs: Int](/documentation/applicationservices/atsuglyphinfoarray/1452089-numglyphs)
- [ATSUGlyphSelector](/documentation/applicationservices/atsuglyphselector)

#### Initializers

- [init()](/documentation/applicationservices/atsuglyphselector/1459028-init)
- [init(collection: GlyphCollection, glyphID: GlyphID)](/documentation/applicationservices/atsuglyphselector/1459219-init)

#### Instance Properties

- [var collection: GlyphCollection](/documentation/applicationservices/atsuglyphselector/1452061-collection)
- [var glyphID: GlyphID](/documentation/applicationservices/atsuglyphselector/1452296-glyphid)
- [ATSULayoutOperationOverrideSpecifier](/documentation/applicationservices/atsulayoutoperationoverridespecifier)

#### Initializers

- [init()](/documentation/applicationservices/atsulayoutoperationoverridespecifier/1458986-init)
- [init(operationSelector: ATSULayoutOperationSelector, overrideUPP: ATSUDirectLayoutOperationOverrideUPP!)](/documentation/applicationservices/atsulayoutoperationoverridespecifier/1778160-init)

#### Instance Properties

- [var operationSelector: ATSULayoutOperationSelector](/documentation/applicationservices/atsulayoutoperationoverridespecifier/1460081-operationselector)
- [var overrideUPP: ATSUDirectLayoutOperationOverrideUPP!](/documentation/applicationservices/atsulayoutoperationoverridespecifier/1463665-overrideupp)
- [ATSURGBAlphaColor](/documentation/applicationservices/atsurgbalphacolor)

#### Initializers

- [init()](/documentation/applicationservices/atsurgbalphacolor/1462940-init)
- [init(red: Float, green: Float, blue: Float, alpha: Float)](/documentation/applicationservices/atsurgbalphacolor/1459046-init)

#### Instance Properties

- [var alpha: Float](/documentation/applicationservices/atsurgbalphacolor/1452180-alpha)
- [var blue: Float](/documentation/applicationservices/atsurgbalphacolor/1452313-blue)
- [var green: Float](/documentation/applicationservices/atsurgbalphacolor/1452063-green)
- [var red: Float](/documentation/applicationservices/atsurgbalphacolor/1452109-red)
- [ATSUStyleRunInfo](/documentation/applicationservices/atsustyleruninfo)

#### Initializers

- [init()](/documentation/applicationservices/atsustyleruninfo/1460482-init)
- [init(runLength: UInt32, styleObjectIndex: UInt32)](/documentation/applicationservices/atsustyleruninfo/1462702-init)

#### Instance Properties

- [var runLength: UInt32](/documentation/applicationservices/atsustyleruninfo/1458993-runlength)
- [var styleObjectIndex: UInt32](/documentation/applicationservices/atsustyleruninfo/1462152-styleobjectindex)
- [ATSUTab](/documentation/applicationservices/atsutab)

#### Initializers

- [init()](/documentation/applicationservices/atsutab/1458896-init)
- [init(tabPosition: ATSUTextMeasurement, tabType: ATSUTabType)](/documentation/applicationservices/atsutab/1464597-init)

#### Instance Properties

- [var tabPosition: ATSUTextMeasurement](/documentation/applicationservices/atsutab/1452324-tabposition)
- [var tabType: ATSUTabType](/documentation/applicationservices/atsutab/1452107-tabtype)
- [ATSUUnhighlightData](/documentation/applicationservices/atsuunhighlightdata)

#### Initializers

- [init()](/documentation/applicationservices/atsuunhighlightdata/1461116-init)
- [init(dataType: ATSUBackgroundDataType, unhighlightData: ATSUBackgroundData)](/documentation/applicationservices/atsuunhighlightdata/1462113-init)

#### Instance Properties

- [var dataType: ATSUBackgroundDataType](/documentation/applicationservices/atsuunhighlightdata/1452129-datatype)
- [var unhighlightData: ATSUBackgroundData](/documentation/applicationservices/atsuunhighlightdata/1452095-unhighlightdata)
- [AppParameters](/documentation/applicationservices/appparameters)

#### Initializers

- [init()](/documentation/applicationservices/appparameters/1461985-init)
- [init(theMsgEvent: AppParameters.__Unnamed_struct_theMsgEvent, eventRefCon: UInt32, messageLength: UInt32)](/documentation/applicationservices/appparameters/1461815-init)

#### Instance Properties

- [var eventRefCon: UInt32](/documentation/applicationservices/appparameters/1462847-eventrefcon)
- [var messageLength: UInt32](/documentation/applicationservices/appparameters/1463729-messagelength)
- [var theMsgEvent: AppParameters.__Unnamed_struct_theMsgEvent](/documentation/applicationservices/appparameters/1462322-themsgevent)
- [AsscEntry](/documentation/applicationservices/asscentry)

#### Initializers

- [init()](/documentation/applicationservices/asscentry/1458948-init)
- [init(fontSize: Int16, fontStyle: Int16, fontID: Int16)](/documentation/applicationservices/asscentry/1462127-init)

#### Instance Properties

- [var fontID: Int16](/documentation/applicationservices/asscentry/1458788-fontid)
- [var fontSize: Int16](/documentation/applicationservices/asscentry/1464349-fontsize)
- [var fontStyle: Int16](/documentation/applicationservices/asscentry/1460878-fontstyle)
- [BitMap](/documentation/applicationservices/bitmap)

#### Initializers

- [init()](/documentation/applicationservices/bitmap/1459270-init)
- [init(baseAddr: Ptr!, rowBytes: Int16, bounds: Rect)](/documentation/applicationservices/bitmap/1464073-init)

#### Instance Properties

- [var baseAddr: Ptr!](/documentation/applicationservices/bitmap/1459306-baseaddr)
- [var bounds: Rect](/documentation/applicationservices/bitmap/1460869-bounds)
- [var rowBytes: Int16](/documentation/applicationservices/bitmap/1464780-rowbytes)
- [CMFloatBitmapFlags](/documentation/applicationservices/cmfloatbitmapflags)

#### Initializers

- [init(UInt32)](/documentation/applicationservices/cmfloatbitmapflags/1463192-init)
- [init(rawValue: UInt32)](/documentation/applicationservices/cmfloatbitmapflags/1463715-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/applicationservices/cmfloatbitmapflags/1462169-rawvalue)
- [CQDProcs](/documentation/applicationservices/cqdprocs)

#### Initializers

- [init()](/documentation/applicationservices/cqdprocs/1463473-init)
- [init(textProc: QDTextUPP!, lineProc: QDLineUPP!, rectProc: QDRectUPP!, rRectProc: QDRRectUPP!, ovalProc: QDOvalUPP!, arcProc: QDArcUPP!, polyProc: QDPolyUPP!, rgnProc: QDRgnUPP!, bitsProc: QDBitsUPP!, commentProc: QDCommentUPP!, txMeasProc: QDTxMeasUPP!, getPicProc: QDGetPicUPP!, putPicProc: QDPutPicUPP!, opcodeProc: QDOpcodeUPP!, newProc1: UniversalProcPtr!, glyphsProc: QDStdGlyphsUPP!, printerStatusProc: QDPrinterStatusUPP!, newProc4: UniversalProcPtr!, newProc5: UniversalProcPtr!, newProc6: UniversalProcPtr!)](/documentation/applicationservices/cqdprocs/1778159-init)

#### Instance Properties

- [var arcProc: QDArcUPP!](/documentation/applicationservices/cqdprocs/1462707-arcproc)
- [var bitsProc: QDBitsUPP!](/documentation/applicationservices/cqdprocs/1463001-bitsproc)
- [var commentProc: QDCommentUPP!](/documentation/applicationservices/cqdprocs/1463288-commentproc)
- [var getPicProc: QDGetPicUPP!](/documentation/applicationservices/cqdprocs/1462475-getpicproc)
- [var glyphsProc: QDStdGlyphsUPP!](/documentation/applicationservices/cqdprocs/1459000-glyphsproc)
- [var lineProc: QDLineUPP!](/documentation/applicationservices/cqdprocs/1463885-lineproc)
- [var newProc1: UniversalProcPtr!](/documentation/applicationservices/cqdprocs/1461234-newproc1)
- [var newProc4: UniversalProcPtr!](/documentation/applicationservices/cqdprocs/1461037-newproc4)
- [var newProc5: UniversalProcPtr!](/documentation/applicationservices/cqdprocs/1461848-newproc5)
- [var newProc6: UniversalProcPtr!](/documentation/applicationservices/cqdprocs/1459877-newproc6)
- [var opcodeProc: QDOpcodeUPP!](/documentation/applicationservices/cqdprocs/1459207-opcodeproc)
- [var ovalProc: QDOvalUPP!](/documentation/applicationservices/cqdprocs/1462138-ovalproc)
- [var polyProc: QDPolyUPP!](/documentation/applicationservices/cqdprocs/1461442-polyproc)
- [var printerStatusProc: QDPrinterStatusUPP!](/documentation/applicationservices/cqdprocs/1464531-printerstatusproc)
- [var putPicProc: QDPutPicUPP!](/documentation/applicationservices/cqdprocs/1461526-putpicproc)
- [var rRectProc: QDRRectUPP!](/documentation/applicationservices/cqdprocs/1461880-rrectproc)
- [var rectProc: QDRectUPP!](/documentation/applicationservices/cqdprocs/1464519-rectproc)
- [var rgnProc: QDRgnUPP!](/documentation/applicationservices/cqdprocs/1463631-rgnproc)
- [var textProc: QDTextUPP!](/documentation/applicationservices/cqdprocs/1460192-textproc)
- [var txMeasProc: QDTxMeasUPP!](/documentation/applicationservices/cqdprocs/1464721-txmeasproc)
- [ColorSpec](/documentation/applicationservices/colorspec)

#### Initializers

- [init()](/documentation/applicationservices/colorspec/1459225-init)
- [init(value: Int16, rgb: RGBColor)](/documentation/applicationservices/colorspec/1459898-init)

#### Instance Properties

- [var rgb: RGBColor](/documentation/applicationservices/colorspec/1459786-rgb)
- [var value: Int16](/documentation/applicationservices/colorspec/1458915-value)
- [ColorSyncAlphaInfo](/documentation/colorsync/colorsyncalphainfo)
- [ColorSyncDataDepth](/documentation/colorsync/colorsyncdatadepth)
- [ColorSyncMD5](/documentation/colorsync/colorsyncmd5)
- [ColorTable](/documentation/applicationservices/colortable)

#### Initializers

- [init()](/documentation/applicationservices/colortable/1460110-init)
- [init(ctSeed: Int32, ctFlags: Int16, ctSize: Int16, ctTable: CSpecArray)](/documentation/applicationservices/colortable/1459206-init)

#### Instance Properties

- [var ctFlags: Int16](/documentation/applicationservices/colortable/1463837-ctflags)
- [var ctSeed: Int32](/documentation/applicationservices/colortable/1460104-ctseed)
- [var ctSize: Int16](/documentation/applicationservices/colortable/1463559-ctsize)
- [var ctTable: CSpecArray](/documentation/applicationservices/colortable/1462125-cttable)
- [FMFilter](/documentation/applicationservices/fmfilter)

#### Initializers

- [init()](/documentation/applicationservices/fmfilter/1462810-init)
- [init(format: UInt32, selector: FMFilterSelector, filter: FMFilter.__Unnamed_union_filter)](/documentation/applicationservices/fmfilter/1461528-init)

#### Instance Properties

- [var filter: FMFilter.__Unnamed_union_filter](/documentation/applicationservices/fmfilter/1461915-filter)
- [var format: UInt32](/documentation/applicationservices/fmfilter/1463378-format)
- [var selector: FMFilterSelector](/documentation/applicationservices/fmfilter/1459528-selector)
- [FMFontDirectoryFilter](/documentation/applicationservices/fmfontdirectoryfilter)

#### Initializers

- [init()](/documentation/applicationservices/fmfontdirectoryfilter/1459271-init)
- [init(fontFolderDomain: Int16, reserved: (UInt32, UInt32))](/documentation/applicationservices/fmfontdirectoryfilter/1463177-init)

#### Instance Properties

- [var fontFolderDomain: Int16](/documentation/applicationservices/fmfontdirectoryfilter/1461760-fontfolderdomain)
- [var reserved: (UInt32, UInt32)](/documentation/applicationservices/fmfontdirectoryfilter/1462718-reserved)
- [FMFontFamilyInstance](/documentation/applicationservices/fmfontfamilyinstance)

#### Initializers

- [init()](/documentation/applicationservices/fmfontfamilyinstance/1458803-init)
- [init(fontFamily: FMFontFamily, fontStyle: FMFontStyle)](/documentation/applicationservices/fmfontfamilyinstance/1459287-init)

#### Instance Properties

- [var fontFamily: FMFontFamily](/documentation/applicationservices/fmfontfamilyinstance/1460371-fontfamily)
- [var fontStyle: FMFontStyle](/documentation/applicationservices/fmfontfamilyinstance/1462092-fontstyle)
- [FMFontFamilyInstanceIterator](/documentation/applicationservices/fmfontfamilyinstanceiterator)

#### Initializers

- [init()](/documentation/applicationservices/fmfontfamilyinstanceiterator/1463179-init)
- [init(reserved: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32))](/documentation/applicationservices/fmfontfamilyinstanceiterator/1463692-init)

#### Instance Properties

- [var reserved: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32)](/documentation/applicationservices/fmfontfamilyinstanceiterator/1459492-reserved)
- [FMFontFamilyIterator](/documentation/applicationservices/fmfontfamilyiterator)

#### Initializers

- [init()](/documentation/applicationservices/fmfontfamilyiterator/1461711-init)
- [init(reserved: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32))](/documentation/applicationservices/fmfontfamilyiterator/1459715-init)

#### Instance Properties

- [var reserved: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32)](/documentation/applicationservices/fmfontfamilyiterator/1459061-reserved)
- [FMFontIterator](/documentation/applicationservices/fmfontiterator)

#### Initializers

- [init()](/documentation/applicationservices/fmfontiterator/1460106-init)
- [init(reserved: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32))](/documentation/applicationservices/fmfontiterator/1459132-init)

#### Instance Properties

- [var reserved: (UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32, UInt32)](/documentation/applicationservices/fmfontiterator/1463041-reserved)
- [FMInput](/documentation/applicationservices/fminput)

#### Initializers

- [init()](/documentation/applicationservices/fminput/1464126-init)
- [init(family: Int16, size: Int16, face: Style, needBits: DarwinBoolean, device: Int16, numer: Point, denom: Point)](/documentation/applicationservices/fminput/1463772-init)

#### Instance Properties

- [var denom: Point](/documentation/applicationservices/fminput/1464568-denom)
- [var device: Int16](/documentation/applicationservices/fminput/1464621-device)
- [var face: Style](/documentation/applicationservices/fminput/1463150-face)
- [var family: Int16](/documentation/applicationservices/fminput/1462404-family)
- [var needBits: DarwinBoolean](/documentation/applicationservices/fminput/1464683-needbits)
- [var numer: Point](/documentation/applicationservices/fminput/1463137-numer)
- [var size: Int16](/documentation/applicationservices/fminput/1459339-size)
- [FamRec](/documentation/applicationservices/famrec)

#### Initializers

- [init()](/documentation/applicationservices/famrec/1462610-init)
- [init(ffFlags: Int16, ffFamID: Int16, ffFirstChar: Int16, ffLastChar: Int16, ffAscent: Int16, ffDescent: Int16, ffLeading: Int16, ffWidMax: Int16, ffWTabOff: Int32, ffKernOff: Int32, ffStylOff: Int32, ffProperty: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16), ffIntl: (Int16, Int16), ffVersion: Int16)](/documentation/applicationservices/famrec/1459680-init)

#### Instance Properties

- [var ffAscent: Int16](/documentation/applicationservices/famrec/1459002-ffascent)
- [var ffDescent: Int16](/documentation/applicationservices/famrec/1459078-ffdescent)
- [var ffFamID: Int16](/documentation/applicationservices/famrec/1459067-fffamid)
- [var ffFirstChar: Int16](/documentation/applicationservices/famrec/1459138-fffirstchar)
- [var ffFlags: Int16](/documentation/applicationservices/famrec/1464706-ffflags)
- [var ffIntl: (Int16, Int16)](/documentation/applicationservices/famrec/1458964-ffintl)
- [var ffKernOff: Int32](/documentation/applicationservices/famrec/1460597-ffkernoff)
- [var ffLastChar: Int16](/documentation/applicationservices/famrec/1463029-fflastchar)
- [var ffLeading: Int16](/documentation/applicationservices/famrec/1461684-ffleading)
- [var ffProperty: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16)](/documentation/applicationservices/famrec/1459261-ffproperty)
- [var ffStylOff: Int32](/documentation/applicationservices/famrec/1463090-ffstyloff)
- [var ffVersion: Int16](/documentation/applicationservices/famrec/1463441-ffversion)
- [var ffWTabOff: Int32](/documentation/applicationservices/famrec/1459368-ffwtaboff)
- [var ffWidMax: Int16](/documentation/applicationservices/famrec/1459379-ffwidmax)
- [FontAssoc](/documentation/applicationservices/fontassoc)

#### Initializers

- [init()](/documentation/applicationservices/fontassoc/1462765-init)
- [init(numAssoc: Int16)](/documentation/applicationservices/fontassoc/1460328-init)

#### Instance Properties

- [var numAssoc: Int16](/documentation/applicationservices/fontassoc/1462375-numassoc)
- [FontInfo](/documentation/applicationservices/fontinfo)

#### Initializers

- [init()](/documentation/applicationservices/fontinfo/1463847-init)
- [init(ascent: Int16, descent: Int16, widMax: Int16, leading: Int16)](/documentation/applicationservices/fontinfo/1461469-init)

#### Instance Properties

- [var ascent: Int16](/documentation/applicationservices/fontinfo/1459407-ascent)
- [var descent: Int16](/documentation/applicationservices/fontinfo/1460432-descent)
- [var leading: Int16](/documentation/applicationservices/fontinfo/1463200-leading)
- [var widMax: Int16](/documentation/applicationservices/fontinfo/1459929-widmax)
- [FontRec](/documentation/applicationservices/fontrec)

#### Initializers

- [init()](/documentation/applicationservices/fontrec/1460466-init)
- [init(fontType: Int16, firstChar: Int16, lastChar: Int16, widMax: Int16, kernMax: Int16, nDescent: Int16, fRectWidth: Int16, fRectHeight: Int16, owTLoc: UInt16, ascent: Int16, descent: Int16, leading: Int16, rowWords: Int16)](/documentation/applicationservices/fontrec/1463741-init)

#### Instance Properties

- [var ascent: Int16](/documentation/applicationservices/fontrec/1459540-ascent)
- [var descent: Int16](/documentation/applicationservices/fontrec/1459204-descent)
- [var fRectHeight: Int16](/documentation/applicationservices/fontrec/1459979-frectheight)
- [var fRectWidth: Int16](/documentation/applicationservices/fontrec/1459740-frectwidth)
- [var firstChar: Int16](/documentation/applicationservices/fontrec/1459289-firstchar)
- [var fontType: Int16](/documentation/applicationservices/fontrec/1461475-fonttype)
- [var kernMax: Int16](/documentation/applicationservices/fontrec/1459125-kernmax)
- [var lastChar: Int16](/documentation/applicationservices/fontrec/1462036-lastchar)
- [var leading: Int16](/documentation/applicationservices/fontrec/1464376-leading)
- [var nDescent: Int16](/documentation/applicationservices/fontrec/1464673-ndescent)
- [var owTLoc: UInt16](/documentation/applicationservices/fontrec/1463357-owtloc)
- [var rowWords: Int16](/documentation/applicationservices/fontrec/1460020-rowwords)
- [var widMax: Int16](/documentation/applicationservices/fontrec/1459085-widmax)
- [GDevice](/documentation/applicationservices/gdevice)

#### Initializers

- [init()](/documentation/applicationservices/gdevice/1460146-init)
- [init(gdRefNum: Int16, gdID: Int16, gdType: Int16, gdITable: Handle!, gdResPref: Int16, gdSearchProc: Handle!, gdCompProc: Handle!, gdFlags: Int16, gdPMap: PixMapHandle!, gdRefCon: Int32, gdNextGD: GDHandle!, gdRect: Rect, gdMode: Int32, gdCCBytes: Int16, gdCCDepth: Int16, gdCCXData: Handle!, gdCCXMask: Handle!, gdExt: Handle!)](/documentation/applicationservices/gdevice/1458837-init)

#### Instance Properties

- [var gdCCBytes: Int16](/documentation/applicationservices/gdevice/1462812-gdccbytes)
- [var gdCCDepth: Int16](/documentation/applicationservices/gdevice/1462418-gdccdepth)
- [var gdCCXData: Handle!](/documentation/applicationservices/gdevice/1459010-gdccxdata)
- [var gdCCXMask: Handle!](/documentation/applicationservices/gdevice/1459120-gdccxmask)
- [var gdCompProc: Handle!](/documentation/applicationservices/gdevice/1459239-gdcompproc)
- [var gdExt: Handle!](/documentation/applicationservices/gdevice/1459670-gdext)
- [var gdFlags: Int16](/documentation/applicationservices/gdevice/1463938-gdflags)
- [var gdID: Int16](/documentation/applicationservices/gdevice/1459653-gdid)
- [var gdITable: Handle!](/documentation/applicationservices/gdevice/1458907-gditable)
- [var gdMode: Int32](/documentation/applicationservices/gdevice/1461199-gdmode)
- [var gdNextGD: GDHandle!](/documentation/applicationservices/gdevice/1458799-gdnextgd)
- [var gdPMap: PixMapHandle!](/documentation/applicationservices/gdevice/1459113-gdpmap)
- [var gdRect: Rect](/documentation/applicationservices/gdevice/1460132-gdrect)
- [var gdRefCon: Int32](/documentation/applicationservices/gdevice/1461387-gdrefcon)
- [var gdRefNum: Int16](/documentation/applicationservices/gdevice/1459092-gdrefnum)
- [var gdResPref: Int16](/documentation/applicationservices/gdevice/1461823-gdrespref)
- [var gdSearchProc: Handle!](/documentation/applicationservices/gdevice/1462338-gdsearchproc)
- [var gdType: Int16](/documentation/applicationservices/gdevice/1462956-gdtype)
- [GrafPort](/documentation/applicationservices/grafport)

#### Initializers

- [init()](/documentation/applicationservices/grafport/1461186-init)

#### Instance Properties

- [var whatever: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16)](/documentation/applicationservices/grafport/1462530-whatever)
- [ICAppSpec](/documentation/applicationservices/icappspec)

#### Initializers

- [init()](/documentation/applicationservices/icappspec/1463686-init)
- [init(fCreator: OSType, name: Str63)](/documentation/applicationservices/icappspec/1459250-init)

#### Instance Properties

- [var fCreator: OSType](/documentation/applicationservices/icappspec/1462979-fcreator)
- [var name: Str63](/documentation/applicationservices/icappspec/1461948-name)
- [ICAppSpecList](/documentation/applicationservices/icappspeclist)

#### Initializers

- [init()](/documentation/applicationservices/icappspeclist/1461354-init)
- [init(numberOfItems: Int16, appSpecs: ICAppSpec)](/documentation/applicationservices/icappspeclist/1460778-init)

#### Instance Properties

- [var appSpecs: ICAppSpec](/documentation/applicationservices/icappspeclist/1461602-appspecs)
- [var numberOfItems: Int16](/documentation/applicationservices/icappspeclist/1462245-numberofitems)
- [ICCharTable](/documentation/applicationservices/icchartable)

#### Initializers

- [init()](/documentation/applicationservices/icchartable/1464629-init)
- [init(netToMac:macToNet:)](/documentation/applicationservices/icchartable/1459871-init)

#### Instance Properties

- [var macToNet: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/applicationservices/icchartable/1462864-mactonet)
- [var netToMac: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/applicationservices/icchartable/1460201-nettomac)
- [ICFileSpec](/documentation/applicationservices/icfilespec)

#### Initializers

- [init()](/documentation/applicationservices/icfilespec/1461792-init)
- [init(volName: Str31, volCreationDate: Int32, fss: FSSpec, alias: AliasRecord)](/documentation/applicationservices/icfilespec/1460097-init)

#### Instance Properties

- [var alias: AliasRecord](/documentation/applicationservices/icfilespec/1460048-alias)
- [var fss: FSSpec](/documentation/applicationservices/icfilespec/1459277-fss)
- [var volCreationDate: Int32](/documentation/applicationservices/icfilespec/1459254-volcreationdate)
- [var volName: Str31](/documentation/applicationservices/icfilespec/1462535-volname)
- [ICFontRecord](/documentation/applicationservices/icfontrecord)

#### Initializers

- [init()](/documentation/applicationservices/icfontrecord/1462684-init)
- [init(size: Int16, face: Style, pad: CChar, font: Str255)](/documentation/applicationservices/icfontrecord/1458842-init)

#### Instance Properties

- [var face: Style](/documentation/applicationservices/icfontrecord/1460532-face)
- [var font: Str255](/documentation/applicationservices/icfontrecord/1463495-font)
- [var pad: CChar](/documentation/applicationservices/icfontrecord/1462786-pad)
- [var size: Int16](/documentation/applicationservices/icfontrecord/1460574-size)
- [ICMapEntry](/documentation/applicationservices/icmapentry)

#### Initializers

- [init()](/documentation/applicationservices/icmapentry/1462224-init)
- [init(totalLength: Int16, fixedLength: ICFixedLength, version: Int16, fileType: OSType, fileCreator: OSType, postCreator: OSType, flags: ICMapEntryFlags, extension: Str255, creatorAppName: Str255, postAppName: Str255, MIMEType: Str255, entryName: Str255)](/documentation/applicationservices/icmapentry/1463249-init)

#### Instance Properties

- [var MIMEType: Str255](/documentation/applicationservices/icmapentry/1462908-mimetype)
- [var creatorAppName: Str255](/documentation/applicationservices/icmapentry/1463557-creatorappname)
- [var entryName: Str255](/documentation/applicationservices/icmapentry/1463382-entryname)
- [var `extension`: Str255](/documentation/applicationservices/icmapentry/1459990-extension)
- [var fileCreator: OSType](/documentation/applicationservices/icmapentry/1461576-filecreator)
- [var fileType: OSType](/documentation/applicationservices/icmapentry/1459150-filetype)
- [var fixedLength: ICFixedLength](/documentation/applicationservices/icmapentry/1461563-fixedlength)
- [var flags: ICMapEntryFlags](/documentation/applicationservices/icmapentry/1461969-flags)
- [var postAppName: Str255](/documentation/applicationservices/icmapentry/1464312-postappname)
- [var postCreator: OSType](/documentation/applicationservices/icmapentry/1460179-postcreator)
- [var totalLength: Int16](/documentation/applicationservices/icmapentry/1464080-totallength)
- [var version: Int16](/documentation/applicationservices/icmapentry/1462319-version)
- [ICServiceEntry](/documentation/applicationservices/icserviceentry)

#### Initializers

- [init()](/documentation/applicationservices/icserviceentry/1461309-init)
- [init(name: Str255, port: Int16, flags: ICServiceEntryFlags)](/documentation/applicationservices/icserviceentry/1459244-init)

#### Instance Properties

- [var flags: ICServiceEntryFlags](/documentation/applicationservices/icserviceentry/1459651-flags)
- [var name: Str255](/documentation/applicationservices/icserviceentry/1460135-name)
- [var port: Int16](/documentation/applicationservices/icserviceentry/1459975-port)
- [ICServices](/documentation/applicationservices/icservices)

#### Initializers

- [init()](/documentation/applicationservices/icservices/1459875-init)
- [init(count: Int16, services: ICServiceEntry)](/documentation/applicationservices/icservices/1459296-init)

#### Instance Properties

- [var count: Int16](/documentation/applicationservices/icservices/1464619-count)
- [var services: ICServiceEntry](/documentation/applicationservices/icservices/1459734-services)
- [KernEntry](/documentation/applicationservices/kernentry)

#### Initializers

- [init()](/documentation/applicationservices/kernentry/1459742-init)
- [init(kernStyle: Int16, kernLength: Int16)](/documentation/applicationservices/kernentry/1464675-init)

#### Instance Properties

- [var kernLength: Int16](/documentation/applicationservices/kernentry/1462716-kernlength)
- [var kernStyle: Int16](/documentation/applicationservices/kernentry/1463739-kernstyle)
- [KernPair](/documentation/applicationservices/kernpair)

#### Initializers

- [init()](/documentation/applicationservices/kernpair/1463574-init)
- [init(kernFirst: CChar, kernSecond: CChar, kernWidth: Int16)](/documentation/applicationservices/kernpair/1463010-init)

#### Instance Properties

- [var kernFirst: CChar](/documentation/applicationservices/kernpair/1459592-kernfirst)
- [var kernSecond: CChar](/documentation/applicationservices/kernpair/1461967-kernsecond)
- [var kernWidth: Int16](/documentation/applicationservices/kernpair/1463405-kernwidth)
- [KernTable](/documentation/applicationservices/kerntable)

#### Initializers

- [init()](/documentation/applicationservices/kerntable/1462098-init)
- [init(numKerns: Int16)](/documentation/applicationservices/kerntable/1461047-init)

#### Instance Properties

- [var numKerns: Int16](/documentation/applicationservices/kerntable/1459332-numkerns)
- [LaunchParamBlockRec](/documentation/applicationservices/launchparamblockrec)

#### Initializers

- [init()](/documentation/applicationservices/launchparamblockrec/1460224-init)
- [init(reserved1: UInt32, reserved2: UInt16, launchBlockID: UInt16, launchEPBLength: UInt32, launchFileFlags: UInt16, launchControlFlags: LaunchFlags, launchAppRef: FSRefPtr!, launchProcessSN: ProcessSerialNumber, launchPreferredSize: UInt32, launchMinimumSize: UInt32, launchAvailableSize: UInt32, launchAppParameters: AppParametersPtr!)](/documentation/applicationservices/launchparamblockrec/1459112-init)

#### Instance Properties

- [var launchAppParameters: AppParametersPtr!](/documentation/applicationservices/launchparamblockrec/1459942-launchappparameters)
- [var launchAppRef: FSRefPtr!](/documentation/applicationservices/launchparamblockrec/1460856-launchappref)
- [var launchAvailableSize: UInt32](/documentation/applicationservices/launchparamblockrec/1459169-launchavailablesize)
- [var launchBlockID: UInt16](/documentation/applicationservices/launchparamblockrec/1462452-launchblockid)
- [var launchControlFlags: LaunchFlags](/documentation/applicationservices/launchparamblockrec/1460826-launchcontrolflags)
- [var launchEPBLength: UInt32](/documentation/applicationservices/launchparamblockrec/1459313-launchepblength)
- [var launchFileFlags: UInt16](/documentation/applicationservices/launchparamblockrec/1462584-launchfileflags)
- [var launchMinimumSize: UInt32](/documentation/applicationservices/launchparamblockrec/1461626-launchminimumsize)
- [var launchPreferredSize: UInt32](/documentation/applicationservices/launchparamblockrec/1462310-launchpreferredsize)
- [var launchProcessSN: ProcessSerialNumber](/documentation/applicationservices/launchparamblockrec/1459263-launchprocesssn)
- [var reserved1: UInt32](/documentation/applicationservices/launchparamblockrec/1460726-reserved1)
- [var reserved2: UInt16](/documentation/applicationservices/launchparamblockrec/1461414-reserved2)
- [MacPolygon](/documentation/applicationservices/macpolygon)

#### Initializers

- [init()](/documentation/applicationservices/macpolygon/1460474-init)
- [init(polySize: Int16, polyBBox: Rect, polyPoints: Point)](/documentation/applicationservices/macpolygon/1460666-init)

#### Instance Properties

- [var polyBBox: Rect](/documentation/applicationservices/macpolygon/1459437-polybbox)
- [var polyPoints: Point](/documentation/applicationservices/macpolygon/1459181-polypoints)
- [var polySize: Int16](/documentation/applicationservices/macpolygon/1463005-polysize)
- [NameTable](/documentation/applicationservices/nametable)

#### Initializers

- [init()](/documentation/applicationservices/nametable/1459498-init)
- [init(stringCount: Int16, baseFontName: Str255)](/documentation/applicationservices/nametable/1462387-init)

#### Instance Properties

- [var baseFontName: Str255](/documentation/applicationservices/nametable/1463733-basefontname)
- [var stringCount: Int16](/documentation/applicationservices/nametable/1462393-stringcount)
- [OpenCPicParams](/documentation/applicationservices/opencpicparams)

#### Initializers

- [init()](/documentation/applicationservices/opencpicparams/1463952-init)
- [init(srcRect: Rect, hRes: Fixed, vRes: Fixed, version: Int16, reserved1: Int16, reserved2: Int32)](/documentation/applicationservices/opencpicparams/1464130-init)

#### Instance Properties

- [var hRes: Fixed](/documentation/applicationservices/opencpicparams/1461719-hres)
- [var reserved1: Int16](/documentation/applicationservices/opencpicparams/1463913-reserved1)
- [var reserved2: Int32](/documentation/applicationservices/opencpicparams/1459077-reserved2)
- [var srcRect: Rect](/documentation/applicationservices/opencpicparams/1463268-srcrect)
- [var vRes: Fixed](/documentation/applicationservices/opencpicparams/1463078-vres)
- [var version: Int16](/documentation/applicationservices/opencpicparams/1462801-version)
- [PMLanguageInfo](/documentation/applicationservices/pmlanguageinfo)

#### Initializers

- [init()](/documentation/applicationservices/pmlanguageinfo/1461392-init)
- [init(level: Str32, version: Str32, release: Str32)](/documentation/applicationservices/pmlanguageinfo/1464084-init)

#### Instance Properties

- [var level: Str32](/documentation/applicationservices/pmlanguageinfo/1459988-level)
- [var release: Str32](/documentation/applicationservices/pmlanguageinfo/1459131-release)
- [var version: Str32](/documentation/applicationservices/pmlanguageinfo/1459038-version)
- [PMPageToPaperMappingType](/documentation/applicationservices/pmpagetopapermappingtype)

#### Initializers

- [init(UInt32)](/documentation/applicationservices/pmpagetopapermappingtype/1463504-init)
- [init(rawValue: UInt32)](/documentation/applicationservices/pmpagetopapermappingtype/1461342-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/applicationservices/pmpagetopapermappingtype/1460449-rawvalue)
- [PMRect](/documentation/applicationservices/pmrect)

#### Initializers

- [init()](/documentation/applicationservices/pmrect/1460457-init)
- [init(top: Double, left: Double, bottom: Double, right: Double)](/documentation/applicationservices/pmrect/1464415-init)

#### Instance Properties

- [var bottom: Double](/documentation/applicationservices/pmrect/1458973-bottom)
- [var left: Double](/documentation/applicationservices/pmrect/1459041-left)
- [var right: Double](/documentation/applicationservices/pmrect/1459337-right)
- [var top: Double](/documentation/applicationservices/pmrect/1461523-top)
- [PMResolution](/documentation/applicationservices/pmresolution)

#### Initializers

- [init()](/documentation/applicationservices/pmresolution/1460236-init)
- [init(hRes: Double, vRes: Double)](/documentation/applicationservices/pmresolution/1459309-init)

#### Instance Properties

- [var hRes: Double](/documentation/applicationservices/pmresolution/1460032-hres)
- [var vRes: Double](/documentation/applicationservices/pmresolution/1464671-vres)
- [PasteboardFlavorFlags](/documentation/applicationservices/pasteboardflavorflags)

#### Type Properties

- [static var notSaved: PasteboardFlavorFlags](/documentation/applicationservices/pasteboardflavorflags/1461870-notsaved)
- [static var promised: PasteboardFlavorFlags](/documentation/applicationservices/pasteboardflavorflags/1464646-promised)
- [static var requestOnly: PasteboardFlavorFlags](/documentation/applicationservices/pasteboardflavorflags/1463690-requestonly)
- [static var senderOnly: PasteboardFlavorFlags](/documentation/applicationservices/pasteboardflavorflags/1462180-senderonly)
- [static var senderTranslated: PasteboardFlavorFlags](/documentation/applicationservices/pasteboardflavorflags/1459364-sendertranslated)
- [static var systemTranslated: PasteboardFlavorFlags](/documentation/applicationservices/pasteboardflavorflags/1461894-systemtranslated)

#### Initializers

- [init(rawValue: OptionBits)](/documentation/applicationservices/pasteboardflavorflags/1644092-init)
- [PasteboardSyncFlags](/documentation/applicationservices/pasteboardsyncflags)

#### Type Properties

- [static var clientIsOwner: PasteboardSyncFlags](/documentation/applicationservices/pasteboardsyncflags/1460509-clientisowner)
- [static var modified: PasteboardSyncFlags](/documentation/applicationservices/pasteboardsyncflags/1458804-modified)

#### Initializers

- [init(rawValue: OptionBits)](/documentation/applicationservices/pasteboardsyncflags/1644060-init)
- [Pattern](/documentation/applicationservices/pattern)

#### Initializers

- [init()](/documentation/applicationservices/pattern/1462790-init)
- [init(pat: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/applicationservices/pattern/1460076-init)

#### Instance Properties

- [var pat: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/applicationservices/pattern/1459488-pat)
- [Picture](/documentation/applicationservices/picture)

#### Initializers

- [init()](/documentation/applicationservices/picture/1459281-init)
- [init(picSize: Int16, picFrame: Rect)](/documentation/applicationservices/picture/1463672-init)

#### Instance Properties

- [var picFrame: Rect](/documentation/applicationservices/picture/1461473-picframe)
- [var picSize: Int16](/documentation/applicationservices/picture/1462314-picsize)
- [PixMap](/documentation/applicationservices/pixmap)

#### Initializers

- [init()](/documentation/applicationservices/pixmap/1464317-init)
- [init(baseAddr: Ptr!, rowBytes: Int16, bounds: Rect, pmVersion: Int16, packType: Int16, packSize: Int32, hRes: Fixed, vRes: Fixed, pixelType: Int16, pixelSize: Int16, cmpCount: Int16, cmpSize: Int16, pixelFormat: OSType, pmTable: CTabHandle!, pmExt: UnsafeMutableRawPointer!)](/documentation/applicationservices/pixmap/1461182-init)

#### Instance Properties

- [var baseAddr: Ptr!](/documentation/applicationservices/pixmap/1459096-baseaddr)
- [var bounds: Rect](/documentation/applicationservices/pixmap/1460186-bounds)
- [var cmpCount: Int16](/documentation/applicationservices/pixmap/1459843-cmpcount)
- [var cmpSize: Int16](/documentation/applicationservices/pixmap/1464685-cmpsize)
- [var hRes: Fixed](/documentation/applicationservices/pixmap/1459752-hres)
- [var packSize: Int32](/documentation/applicationservices/pixmap/1463449-packsize)
- [var packType: Int16](/documentation/applicationservices/pixmap/1459316-packtype)
- [var pixelFormat: OSType](/documentation/applicationservices/pixmap/1459241-pixelformat)
- [var pixelSize: Int16](/documentation/applicationservices/pixmap/1460391-pixelsize)
- [var pixelType: Int16](/documentation/applicationservices/pixmap/1463694-pixeltype)
- [var pmExt: UnsafeMutableRawPointer!](/documentation/applicationservices/pixmap/1462255-pmext)
- [var pmTable: CTabHandle!](/documentation/applicationservices/pixmap/1459634-pmtable)
- [var pmVersion: Int16](/documentation/applicationservices/pixmap/1460848-pmversion)
- [var rowBytes: Int16](/documentation/applicationservices/pixmap/1462797-rowbytes)
- [var vRes: Fixed](/documentation/applicationservices/pixmap/1459423-vres)
- [PixPat](/documentation/applicationservices/pixpat)

#### Initializers

- [init()](/documentation/applicationservices/pixpat/1463403-init)
- [init(patType: Int16, patMap: PixMapHandle!, patData: Handle!, patXData: Handle!, patXValid: Int16, patXMap: Handle!, pat1Data: Pattern)](/documentation/applicationservices/pixpat/1460972-init)

#### Instance Properties

- [var pat1Data: Pattern](/documentation/applicationservices/pixpat/1462308-pat1data)
- [var patData: Handle!](/documentation/applicationservices/pixpat/1459829-patdata)
- [var patMap: PixMapHandle!](/documentation/applicationservices/pixpat/1464638-patmap)
- [var patType: Int16](/documentation/applicationservices/pixpat/1462564-pattype)
- [var patXData: Handle!](/documentation/applicationservices/pixpat/1459286-patxdata)
- [var patXMap: Handle!](/documentation/applicationservices/pixpat/1463879-patxmap)
- [var patXValid: Int16](/documentation/applicationservices/pixpat/1462271-patxvalid)
- [ProcessInfoExtendedRec](/documentation/applicationservices/processinfoextendedrec)

#### Initializers

- [init()](/documentation/applicationservices/processinfoextendedrec/1464665-init)
- [init(processInfoLength: UInt32, processName: StringPtr!, processNumber: ProcessSerialNumber, processType: UInt32, processSignature: OSType, processMode: UInt32, processLocation: Ptr!, processSize: UInt32, processFreeMem: UInt32, processLauncher: ProcessSerialNumber, processLaunchDate: UInt32, processActiveTime: UInt32, processAppRef: FSRefPtr!, processTempMemTotal: UInt32, processPurgeableTempMemTotal: UInt32)](/documentation/applicationservices/processinfoextendedrec/1462532-init)

#### Instance Properties

- [var processActiveTime: UInt32](/documentation/applicationservices/processinfoextendedrec/1461059-processactivetime)
- [var processAppRef: FSRefPtr!](/documentation/applicationservices/processinfoextendedrec/1464388-processappref)
- [var processFreeMem: UInt32](/documentation/applicationservices/processinfoextendedrec/1458795-processfreemem)
- [var processInfoLength: UInt32](/documentation/applicationservices/processinfoextendedrec/1461721-processinfolength)
- [var processLaunchDate: UInt32](/documentation/applicationservices/processinfoextendedrec/1460999-processlaunchdate)
- [var processLauncher: ProcessSerialNumber](/documentation/applicationservices/processinfoextendedrec/1462399-processlauncher)
- [var processLocation: Ptr!](/documentation/applicationservices/processinfoextendedrec/1463684-processlocation)
- [var processMode: UInt32](/documentation/applicationservices/processinfoextendedrec/1462055-processmode)
- [var processName: StringPtr!](/documentation/applicationservices/processinfoextendedrec/1462598-processname)
- [var processNumber: ProcessSerialNumber](/documentation/applicationservices/processinfoextendedrec/1464114-processnumber)
- [var processPurgeableTempMemTotal: UInt32](/documentation/applicationservices/processinfoextendedrec/1458942-processpurgeabletempmemtotal)
- [var processSignature: OSType](/documentation/applicationservices/processinfoextendedrec/1461232-processsignature)
- [var processSize: UInt32](/documentation/applicationservices/processinfoextendedrec/1459964-processsize)
- [var processTempMemTotal: UInt32](/documentation/applicationservices/processinfoextendedrec/1459478-processtempmemtotal)
- [var processType: UInt32](/documentation/applicationservices/processinfoextendedrec/1459518-processtype)
- [ProcessInfoRec](/documentation/applicationservices/processinforec)

#### Initializers

- [init()](/documentation/applicationservices/processinforec/1461452-init)
- [init(processInfoLength: UInt32, processName: StringPtr!, processNumber: ProcessSerialNumber, processType: UInt32, processSignature: OSType, processMode: UInt32, processLocation: Ptr!, processSize: UInt32, processFreeMem: UInt32, processLauncher: ProcessSerialNumber, processLaunchDate: UInt32, processActiveTime: UInt32, processAppRef: FSRefPtr!)](/documentation/applicationservices/processinforec/1463048-init)

#### Instance Properties

- [var processActiveTime: UInt32](/documentation/applicationservices/processinforec/1458826-processactivetime)
- [var processAppRef: FSRefPtr!](/documentation/applicationservices/processinforec/1461921-processappref)
- [var processFreeMem: UInt32](/documentation/applicationservices/processinforec/1461649-processfreemem)
- [var processInfoLength: UInt32](/documentation/applicationservices/processinforec/1464021-processinfolength)
- [var processLaunchDate: UInt32](/documentation/applicationservices/processinforec/1463946-processlaunchdate)
- [var processLauncher: ProcessSerialNumber](/documentation/applicationservices/processinforec/1464681-processlauncher)
- [var processLocation: Ptr!](/documentation/applicationservices/processinforec/1462868-processlocation)
- [var processMode: UInt32](/documentation/applicationservices/processinforec/1463645-processmode)
- [var processName: StringPtr!](/documentation/applicationservices/processinforec/1462097-processname)
- [var processNumber: ProcessSerialNumber](/documentation/applicationservices/processinforec/1460704-processnumber)
- [var processSignature: OSType](/documentation/applicationservices/processinforec/1461669-processsignature)
- [var processSize: UInt32](/documentation/applicationservices/processinforec/1462249-processsize)
- [var processType: UInt32](/documentation/applicationservices/processinforec/1463681-processtype)
- [RGBColor](/documentation/applicationservices/rgbcolor)

#### Initializers

- [init()](/documentation/applicationservices/rgbcolor/1463509-init)
- [init(red: UInt16, green: UInt16, blue: UInt16)](/documentation/applicationservices/rgbcolor/1464262-init)

#### Instance Properties

- [var blue: UInt16](/documentation/applicationservices/rgbcolor/1462232-blue)
- [var green: UInt16](/documentation/applicationservices/rgbcolor/1459366-green)
- [var red: UInt16](/documentation/applicationservices/rgbcolor/1459194-red)
- [SizeResourceRec](/documentation/applicationservices/sizeresourcerec)

#### Initializers

- [init()](/documentation/applicationservices/sizeresourcerec/1460792-init)
- [init(flags: UInt16, preferredHeapSize: UInt32, minimumHeapSize: UInt32)](/documentation/applicationservices/sizeresourcerec/1458780-init)

#### Instance Properties

- [var flags: UInt16](/documentation/applicationservices/sizeresourcerec/1463163-flags)
- [var minimumHeapSize: UInt32](/documentation/applicationservices/sizeresourcerec/1462207-minimumheapsize)
- [var preferredHeapSize: UInt32](/documentation/applicationservices/sizeresourcerec/1460058-preferredheapsize)
- [StyleTable](/documentation/applicationservices/styletable)

#### Initializers

- [init()](/documentation/applicationservices/styletable/1464270-init)
- [init(fontClass: Int16, offset: Int32, reserved: Int32, indexes: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar))](/documentation/applicationservices/styletable/1458832-init)

#### Instance Properties

- [var fontClass: Int16](/documentation/applicationservices/styletable/1463459-fontclass)
- [var indexes: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar)](/documentation/applicationservices/styletable/1464734-indexes)
- [var offset: Int32](/documentation/applicationservices/styletable/1461282-offset)
- [var reserved: Int32](/documentation/applicationservices/styletable/1464390-reserved)
- [VDGammaRecord](/documentation/applicationservices/vdgammarecord)

#### Initializers

- [init()](/documentation/applicationservices/vdgammarecord/1459857-init)
- [init(csGTable: Ptr!)](/documentation/applicationservices/vdgammarecord/1464585-init)

#### Instance Properties

- [var csGTable: Ptr!](/documentation/applicationservices/vdgammarecord/1458775-csgtable)
- [ApplicationServices Enumerations](/documentation/applicationservices/applicationservices_enumerations)

### Enumerations

- [AXError](/documentation/applicationservices/axerror)

#### Enumeration Cases

- [case apiDisabled](/documentation/applicationservices/axerror/apidisabled)
- [case actionUnsupported](/documentation/applicationservices/axerror/actionunsupported)
- [case attributeUnsupported](/documentation/applicationservices/axerror/attributeunsupported)
- [case cannotComplete](/documentation/applicationservices/axerror/cannotcomplete)
- [case failure](/documentation/applicationservices/axerror/failure)
- [case illegalArgument](/documentation/applicationservices/axerror/illegalargument)
- [case invalidUIElement](/documentation/applicationservices/axerror/invaliduielement)
- [case invalidUIElementObserver](/documentation/applicationservices/axerror/invaliduielementobserver)
- [case noValue](/documentation/applicationservices/axerror/novalue)
- [case notEnoughPrecision](/documentation/applicationservices/axerror/notenoughprecision)
- [case notImplemented](/documentation/applicationservices/axerror/notimplemented)
- [case notificationAlreadyRegistered](/documentation/applicationservices/axerror/notificationalreadyregistered)
- [case notificationNotRegistered](/documentation/applicationservices/axerror/notificationnotregistered)
- [case notificationUnsupported](/documentation/applicationservices/axerror/notificationunsupported)
- [case parameterizedAttributeUnsupported](/documentation/applicationservices/axerror/parameterizedattributeunsupported)
- [case success](/documentation/applicationservices/axerror/success)
- [AXPriority](/documentation/applicationservices/axpriority)

#### Enumeration Cases

- [case high](/documentation/applicationservices/axpriority/high)
- [case low](/documentation/applicationservices/axpriority/low)
- [case medium](/documentation/applicationservices/axpriority/medium)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1535445-anonymous)

#### Constants

- [var k16BE555PixelFormat: Int](/documentation/applicationservices/k16be555pixelformat)
- [var k16BE565PixelFormat: Int](/documentation/applicationservices/k16be565pixelformat)
- [var k16LE5551PixelFormat: Int](/documentation/applicationservices/k16le5551pixelformat)
- [var k16LE555PixelFormat: Int](/documentation/applicationservices/k16le555pixelformat)
- [var k16LE565PixelFormat: Int](/documentation/applicationservices/k16le565pixelformat)
- [var k1IndexedGrayPixelFormat: Int](/documentation/applicationservices/k1indexedgraypixelformat)
- [var k1MonochromePixelFormat: Int](/documentation/applicationservices/k1monochromepixelformat)
- [var k24BGRPixelFormat: Int](/documentation/applicationservices/k24bgrpixelformat)
- [var k24RGBPixelFormat: Int](/documentation/applicationservices/k24rgbpixelformat)
- [var k2IndexedGrayPixelFormat: Int](/documentation/applicationservices/k2indexedgraypixelformat)
- [var k2IndexedPixelFormat: Int](/documentation/applicationservices/k2indexedpixelformat)
- [var k2vuyPixelFormat: Int](/documentation/applicationservices/k2vuypixelformat)
- [var k32ABGRPixelFormat: Int](/documentation/applicationservices/k32abgrpixelformat)
- [var k32ARGBPixelFormat: Int](/documentation/applicationservices/k32argbpixelformat)
- [var k32BGRAPixelFormat: Int](/documentation/applicationservices/k32bgrapixelformat)
- [var k32RGBAPixelFormat: Int](/documentation/applicationservices/k32rgbapixelformat)
- [var k4IndexedGrayPixelFormat: Int](/documentation/applicationservices/k4indexedgraypixelformat)
- [var k4IndexedPixelFormat: Int](/documentation/applicationservices/k4indexedpixelformat)
- [var k8IndexedGrayPixelFormat: Int](/documentation/applicationservices/k8indexedgraypixelformat)
- [var k8IndexedPixelFormat: Int](/documentation/applicationservices/k8indexedpixelformat)
- [var kUYVY422PixelFormat: Int](/documentation/applicationservices/kuyvy422pixelformat)
- [var kYUV211PixelFormat: Int](/documentation/applicationservices/kyuv211pixelformat)
- [var kYUV411PixelFormat: Int](/documentation/applicationservices/kyuv411pixelformat)
- [var kYUVSPixelFormat: Int](/documentation/applicationservices/kyuvspixelformat)
- [var kYUVUPixelFormat: Int](/documentation/applicationservices/kyuvupixelformat)
- [var kYVU9PixelFormat: Int](/documentation/applicationservices/kyvu9pixelformat)
- [var kYVYU422PixelFormat: Int](/documentation/applicationservices/kyvyu422pixelformat)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1535370-anonymous)

#### Constants

- [var kHorizontalConstraint: Int](/documentation/applicationservices/khorizontalconstraint)
- [var kNoConstraint: Int](/documentation/applicationservices/knoconstraint)
- [var kVerticalConstraint: Int](/documentation/applicationservices/kverticalconstraint)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1521901-anonymous)

#### Constants

- [var kATSUFlattenOptionNoOptionsMask: Int](/documentation/applicationservices/katsuflattenoptionnooptionsmask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1521913-anonymous)

#### Constants

- [var kATSFlattenedFontSpecifierRawNameData: Int](/documentation/applicationservices/katsflattenedfontspecifierrawnamedata)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1521918-anonymous)

#### Constants

- [var kATSFlatDataUstlCurrentVersion: Int](/documentation/applicationservices/katsflatdataustlcurrentversion)
- [var kATSFlatDataUstlVersion0: Int](/documentation/applicationservices/katsflatdataustlversion0)
- [var kATSFlatDataUstlVersion1: Int](/documentation/applicationservices/katsflatdataustlversion1)
- [var kATSFlatDataUstlVersion2: Int](/documentation/applicationservices/katsflatdataustlversion2)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1521927-anonymous)

#### Constants

- [var kATSUUnFlattenOptionNoOptionsMask: Int](/documentation/applicationservices/katsuunflattenoptionnooptionsmask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1521903-anonymous)

#### Constants

- [var kATSUDataStreamUnicodeStyledText: Int](/documentation/applicationservices/katsudatastreamunicodestyledtext)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1526301-anonymous)

#### Constants

- [var badPasteboardFlavorErr: Int](/documentation/applicationservices/badpasteboardflavorerr)
- [var badPasteboardIndexErr: Int](/documentation/applicationservices/badpasteboardindexerr)
- [var badPasteboardItemErr: Int](/documentation/applicationservices/badpasteboarditemerr)
- [var badPasteboardSyncErr: Int](/documentation/applicationservices/badpasteboardsyncerr)
- [var duplicatePasteboardFlavorErr: Int](/documentation/applicationservices/duplicatepasteboardflavorerr)
- [var noPasteboardPromiseKeeperErr: Int](/documentation/applicationservices/nopasteboardpromisekeepererr)
- [var notPasteboardOwnerErr: Int](/documentation/applicationservices/notpasteboardownererr)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1507763-anonymous)

#### Constants

- [var ttDisabled: Int](/documentation/applicationservices/ttdisabled)
- [var ttLabel1: Int](/documentation/applicationservices/ttlabel1)
- [var ttLabel2: Int](/documentation/applicationservices/ttlabel2)
- [var ttLabel3: Int](/documentation/applicationservices/ttlabel3)
- [var ttLabel4: Int](/documentation/applicationservices/ttlabel4)
- [var ttLabel5: Int](/documentation/applicationservices/ttlabel5)
- [var ttLabel6: Int](/documentation/applicationservices/ttlabel6)
- [var ttLabel7: Int](/documentation/applicationservices/ttlabel7)
- [var ttNone: Int](/documentation/applicationservices/ttnone)
- [var ttOffline: Int](/documentation/applicationservices/ttoffline)
- [var ttOpen: Int](/documentation/applicationservices/ttopen)
- [var ttSelected: Int](/documentation/applicationservices/ttselected)
- [var ttSelectedDisabled: Int](/documentation/applicationservices/ttselecteddisabled)
- [var ttSelectedOffline: Int](/documentation/applicationservices/ttselectedoffline)
- [var ttSelectedOpen: Int](/documentation/applicationservices/ttselectedopen)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1507687-anonymous)

#### Constants

- [var svAll1BitData: UInt32](/documentation/applicationservices/svall1bitdata)
- [var svAll4BitData: UInt32](/documentation/applicationservices/svall4bitdata)
- [var svAll8BitData: UInt32](/documentation/applicationservices/svall8bitdata)
- [var svAllAvailableData: UInt32](/documentation/applicationservices/svallavailabledata)
- [var svAllLargeData: UInt32](/documentation/applicationservices/svalllargedata)
- [var svAllMiniData: UInt32](/documentation/applicationservices/svallminidata)
- [var svAllSmallData: UInt32](/documentation/applicationservices/svallsmalldata)
- [var svLarge1Bit: UInt32](/documentation/applicationservices/svlarge1bit)
- [var svLarge4Bit: UInt32](/documentation/applicationservices/svlarge4bit)
- [var svLarge8Bit: UInt32](/documentation/applicationservices/svlarge8bit)
- [var svMini1Bit: UInt32](/documentation/applicationservices/svmini1bit)
- [var svMini4Bit: UInt32](/documentation/applicationservices/svmini4bit)
- [var svMini8Bit: UInt32](/documentation/applicationservices/svmini8bit)
- [var svSmall1Bit: UInt32](/documentation/applicationservices/svsmall1bit)
- [var svSmall4Bit: UInt32](/documentation/applicationservices/svsmall4bit)
- [var svSmall8Bit: UInt32](/documentation/applicationservices/svsmall8bit)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1507672-anonymous)

#### Constants

- [var kTransformDisabled: Int](/documentation/applicationservices/ktransformdisabled)
- [var kTransformLabel1: Int](/documentation/applicationservices/ktransformlabel1)
- [var kTransformLabel2: Int](/documentation/applicationservices/ktransformlabel2)
- [var kTransformLabel3: Int](/documentation/applicationservices/ktransformlabel3)
- [var kTransformLabel4: Int](/documentation/applicationservices/ktransformlabel4)
- [var kTransformLabel5: Int](/documentation/applicationservices/ktransformlabel5)
- [var kTransformLabel6: Int](/documentation/applicationservices/ktransformlabel6)
- [var kTransformLabel7: Int](/documentation/applicationservices/ktransformlabel7)
- [var kTransformNone: Int](/documentation/applicationservices/ktransformnone)
- [var kTransformOffline: Int](/documentation/applicationservices/ktransformoffline)
- [var kTransformOpen: Int](/documentation/applicationservices/ktransformopen)
- [var kTransformSelected: Int](/documentation/applicationservices/ktransformselected)
- [var kTransformSelectedDisabled: Int](/documentation/applicationservices/ktransformselecteddisabled)
- [var kTransformSelectedOffline: Int](/documentation/applicationservices/ktransformselectedoffline)
- [var kTransformSelectedOpen: Int](/documentation/applicationservices/ktransformselectedopen)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1507713-anonymous)

#### Constants

- [var kSelectorAll1BitData: UInt32](/documentation/applicationservices/kselectorall1bitdata)
- [var kSelectorAll32BitData: UInt32](/documentation/applicationservices/kselectorall32bitdata)
- [var kSelectorAll4BitData: UInt32](/documentation/applicationservices/kselectorall4bitdata)
- [var kSelectorAll8BitData: UInt32](/documentation/applicationservices/kselectorall8bitdata)
- [var kSelectorAllAvailableData: UInt32](/documentation/applicationservices/kselectorallavailabledata)
- [var kSelectorAllHugeData: UInt32](/documentation/applicationservices/kselectorallhugedata)
- [var kSelectorAllLargeData: UInt32](/documentation/applicationservices/kselectoralllargedata)
- [var kSelectorAllMiniData: UInt32](/documentation/applicationservices/kselectorallminidata)
- [var kSelectorAllSmallData: UInt32](/documentation/applicationservices/kselectorallsmalldata)
- [var kSelectorHuge1Bit: UInt32](/documentation/applicationservices/kselectorhuge1bit)
- [var kSelectorHuge32Bit: UInt32](/documentation/applicationservices/kselectorhuge32bit)
- [var kSelectorHuge4Bit: UInt32](/documentation/applicationservices/kselectorhuge4bit)
- [var kSelectorHuge8Bit: UInt32](/documentation/applicationservices/kselectorhuge8bit)
- [var kSelectorHuge8BitMask: UInt32](/documentation/applicationservices/kselectorhuge8bitmask)
- [var kSelectorLarge1Bit: UInt32](/documentation/applicationservices/kselectorlarge1bit)
- [var kSelectorLarge32Bit: UInt32](/documentation/applicationservices/kselectorlarge32bit)
- [var kSelectorLarge4Bit: UInt32](/documentation/applicationservices/kselectorlarge4bit)
- [var kSelectorLarge8Bit: UInt32](/documentation/applicationservices/kselectorlarge8bit)
- [var kSelectorLarge8BitMask: UInt32](/documentation/applicationservices/kselectorlarge8bitmask)
- [var kSelectorMini1Bit: UInt32](/documentation/applicationservices/kselectormini1bit)
- [var kSelectorMini4Bit: UInt32](/documentation/applicationservices/kselectormini4bit)
- [var kSelectorMini8Bit: UInt32](/documentation/applicationservices/kselectormini8bit)
- [var kSelectorSmall1Bit: UInt32](/documentation/applicationservices/kselectorsmall1bit)
- [var kSelectorSmall32Bit: UInt32](/documentation/applicationservices/kselectorsmall32bit)
- [var kSelectorSmall4Bit: UInt32](/documentation/applicationservices/kselectorsmall4bit)
- [var kSelectorSmall8Bit: UInt32](/documentation/applicationservices/kselectorsmall8bit)
- [var kSelectorSmall8BitMask: UInt32](/documentation/applicationservices/kselectorsmall8bitmask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1507703-anonymous)

#### Constants

- [var atAbsoluteCenter: Int](/documentation/applicationservices/atabsolutecenter)
- [var atBottom: Int](/documentation/applicationservices/atbottom)
- [var atBottomLeft: Int](/documentation/applicationservices/atbottomleft)
- [var atBottomRight: Int](/documentation/applicationservices/atbottomright)
- [var atCenterBottom: Int](/documentation/applicationservices/atcenterbottom)
- [var atCenterLeft: Int](/documentation/applicationservices/atcenterleft)
- [var atCenterRight: Int](/documentation/applicationservices/atcenterright)
- [var atCenterTop: Int](/documentation/applicationservices/atcentertop)
- [var atHorizontalCenter: Int](/documentation/applicationservices/athorizontalcenter)
- [var atLeft: Int](/documentation/applicationservices/atleft)
- [var atNone: Int](/documentation/applicationservices/atnone)
- [var atRight: Int](/documentation/applicationservices/atright)
- [var atTop: Int](/documentation/applicationservices/attop)
- [var atTopLeft: Int](/documentation/applicationservices/attopleft)
- [var atTopRight: Int](/documentation/applicationservices/attopright)
- [var atVerticalCenter: Int](/documentation/applicationservices/atverticalcenter)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1507743-anonymous)

#### Constants

- [var kPlotIconRefNoImage: Int](/documentation/applicationservices/kploticonrefnoimage)
- [var kPlotIconRefNoMask: Int](/documentation/applicationservices/kploticonrefnomask)
- [var kPlotIconRefNormalFlags: Int](/documentation/applicationservices/kploticonrefnormalflags)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1507611-anonymous)

#### Constants

- [var kAlignAbsoluteCenter: Int](/documentation/applicationservices/kalignabsolutecenter)
- [var kAlignBottom: Int](/documentation/applicationservices/kalignbottom)
- [var kAlignBottomLeft: Int](/documentation/applicationservices/kalignbottomleft)
- [var kAlignBottomRight: Int](/documentation/applicationservices/kalignbottomright)
- [var kAlignCenterBottom: Int](/documentation/applicationservices/kaligncenterbottom)
- [var kAlignCenterLeft: Int](/documentation/applicationservices/kaligncenterleft)
- [var kAlignCenterRight: Int](/documentation/applicationservices/kaligncenterright)
- [var kAlignCenterTop: Int](/documentation/applicationservices/kaligncentertop)
- [var kAlignHorizontalCenter: Int](/documentation/applicationservices/kalignhorizontalcenter)
- [var kAlignLeft: Int](/documentation/applicationservices/kalignleft)
- [var kAlignNone: Int](/documentation/applicationservices/kalignnone)
- [var kAlignRight: Int](/documentation/applicationservices/kalignright)
- [var kAlignTop: Int](/documentation/applicationservices/kaligntop)
- [var kAlignTopLeft: Int](/documentation/applicationservices/kaligntopleft)
- [var kAlignTopRight: Int](/documentation/applicationservices/kaligntopright)
- [var kAlignVerticalCenter: Int](/documentation/applicationservices/kalignverticalcenter)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1418010-anonymous)

#### Constants

- [var kPMCoverPageAfter: Int](/documentation/applicationservices/kpmcoverpageafter)
- [var kPMCoverPageBefore: Int](/documentation/applicationservices/kpmcoverpagebefore)
- [var kPMCoverPageNone: Int](/documentation/applicationservices/kpmcoverpagenone)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506808-anonymous)

#### Constants

- [var kPMBorderDoubleHairline: Int](/documentation/applicationservices/kpmborderdoublehairline)
- [var kPMBorderDoubleThickline: Int](/documentation/applicationservices/kpmborderdoublethickline)
- [var kPMBorderSingleHairline: Int](/documentation/applicationservices/kpmbordersinglehairline)
- [var kPMBorderSingleThickline: Int](/documentation/applicationservices/kpmbordersinglethickline)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506734-anonymous)

#### Constants

- [var kPMScalingCenterOnImgArea: Int](/documentation/applicationservices/kpmscalingcenteronimgarea)
- [var kPMScalingCenterOnPaper: Int](/documentation/applicationservices/kpmscalingcenteronpaper)
- [var kPMScalingPinBottomLeft: Int](/documentation/applicationservices/kpmscalingpinbottomleft)
- [var kPMScalingPinBottomRight: Int](/documentation/applicationservices/kpmscalingpinbottomright)
- [var kPMScalingPinTopLeft: Int](/documentation/applicationservices/kpmscalingpintopleft)
- [var kPMScalingPinTopRight: Int](/documentation/applicationservices/kpmscalingpintopright)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506750-anonymous)

#### Constants

- [var kPMLandscape: Int](/documentation/applicationservices/kpmlandscape)
- [var kPMPortrait: Int](/documentation/applicationservices/kpmportrait)
- [var kPMReverseLandscape: Int](/documentation/applicationservices/kpmreverselandscape)
- [var kPMReversePortrait: Int](/documentation/applicationservices/kpmreverseportrait)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506818-anonymous)

#### Constants

- [var kPMPrinterIdle: Int](/documentation/applicationservices/kpmprinteridle)
- [var kPMPrinterProcessing: Int](/documentation/applicationservices/kpmprinterprocessing)
- [var kPMPrinterStopped: Int](/documentation/applicationservices/kpmprinterstopped)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506811-anonymous)

#### Constants

- [var kPMPaperTypeCoated: Int](/documentation/applicationservices/kpmpapertypecoated)
- [var kPMPaperTypeGlossy: Int](/documentation/applicationservices/kpmpapertypeglossy)
- [var kPMPaperTypePlain: Int](/documentation/applicationservices/kpmpapertypeplain)
- [var kPMPaperTypePremium: Int](/documentation/applicationservices/kpmpapertypepremium)
- [var kPMPaperTypeTShirt: Int](/documentation/applicationservices/kpmpapertypetshirt)
- [var kPMPaperTypeTransparency: Int](/documentation/applicationservices/kpmpapertypetransparency)
- [var kPMPaperTypeUnknown: Int](/documentation/applicationservices/kpmpapertypeunknown)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506820-anonymous)

#### Constants

- [var kPMCMYKColorSpaceModel: Int](/documentation/applicationservices/kpmcmykcolorspacemodel)
- [var kPMDevNColorSpaceModel: Int](/documentation/applicationservices/kpmdevncolorspacemodel)
- [var kPMGrayColorSpaceModel: Int](/documentation/applicationservices/kpmgraycolorspacemodel)
- [var kPMRGBColorSpaceModel: Int](/documentation/applicationservices/kpmrgbcolorspacemodel)
- [var kPMUnknownColorSpaceModel: Int](/documentation/applicationservices/kpmunknowncolorspacemodel)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506722-anonymous)

#### Constants

- [var kPMGeneralError: Int](/documentation/applicationservices/kpmgeneralerror)
- [var kPMInvalidPageFormat: Int](/documentation/applicationservices/kpminvalidpageformat)
- [var kPMInvalidParameter: Int](/documentation/applicationservices/kpminvalidparameter)
- [var kPMInvalidPrintSettings: Int](/documentation/applicationservices/kpminvalidprintsettings)
- [var kPMNoDefaultPrinter: Int](/documentation/applicationservices/kpmnodefaultprinter)
- [var kPMNoError: Int](/documentation/applicationservices/kpmnoerror)
- [var kPMNoSuchEntry: Int](/documentation/applicationservices/kpmnosuchentry)
- [var kPMNotImplemented: Int](/documentation/applicationservices/kpmnotimplemented)
- [var kPMOutOfScope: Int](/documentation/applicationservices/kpmoutofscope)
- [var kPMValueOutOfRange: Int](/documentation/applicationservices/kpmvalueoutofrange)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506800-anonymous)

#### Constants

- [var kPMInvalidPreset: Int](/documentation/applicationservices/kpminvalidpreset)
- [var kPMInvalidPrintSession: Int](/documentation/applicationservices/kpminvalidprintsession)
- [var kPMInvalidPrinter: Int](/documentation/applicationservices/kpminvalidprinter)
- [var kPMObjectInUse: Int](/documentation/applicationservices/kpmobjectinuse)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506772-anonymous)

#### Constants

- [var kPMHideInlineItems: Int](/documentation/applicationservices/kpmhideinlineitems)
- [var kPMShowDefaultInlineItems: Int](/documentation/applicationservices/kpmshowdefaultinlineitems)
- [var kPMShowInlineCopies: Int](/documentation/applicationservices/kpmshowinlinecopies)
- [var kPMShowInlineOrientation: Int](/documentation/applicationservices/kpmshowinlineorientation)
- [var kPMShowInlinePageRange: Int](/documentation/applicationservices/kpmshowinlinepagerange)
- [var kPMShowInlinePageRangeWithSelection: Int](/documentation/applicationservices/kpmshowinlinepagerangewithselection)
- [var kPMShowInlinePaperSize: Int](/documentation/applicationservices/kpmshowinlinepapersize)
- [var kPMShowInlineScale: Int](/documentation/applicationservices/kpmshowinlinescale)
- [var kPMShowPageAttributesPDE: Int](/documentation/applicationservices/kpmshowpageattributespde)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506762-anonymous)

#### Constants

- [var kAllPPDDomains: Int](/documentation/applicationservices/kallppddomains)
- [var kCUPSPPDDomain: Int](/documentation/applicationservices/kcupsppddomain)
- [var kLocalPPDDomain: Int](/documentation/applicationservices/klocalppddomain)
- [var kNetworkPPDDomain: Int](/documentation/applicationservices/knetworkppddomain)
- [var kSystemPPDDomain: Int](/documentation/applicationservices/ksystemppddomain)
- [var kUserPPDDomain: Int](/documentation/applicationservices/kuserppddomain)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506743-anonymous)

#### Constants

- [var kPMQualityBest: Int](/documentation/applicationservices/kpmqualitybest)
- [var kPMQualityDraft: Int](/documentation/applicationservices/kpmqualitydraft)
- [var kPMQualityHighest: Int](/documentation/applicationservices/kpmqualityhighest)
- [var kPMQualityInkSaver: Int](/documentation/applicationservices/kpmqualityinksaver)
- [var kPMQualityLowest: Int](/documentation/applicationservices/kpmqualitylowest)
- [var kPMQualityNormal: Int](/documentation/applicationservices/kpmqualitynormal)
- [var kPMQualityPhoto: Int](/documentation/applicationservices/kpmqualityphoto)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506830-anonymous)

#### Constants

- [var kPMUnlocked: Int](/documentation/applicationservices/kpmunlocked)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506831-anonymous)

#### Constants

- [var kPMDestinationFax: Int](/documentation/applicationservices/kpmdestinationfax)
- [var kPMDestinationFile: Int](/documentation/applicationservices/kpmdestinationfile)
- [var kPMDestinationInvalid: Int](/documentation/applicationservices/kpmdestinationinvalid)
- [var kPMDestinationPreview: Int](/documentation/applicationservices/kpmdestinationpreview)
- [var kPMDestinationPrinter: Int](/documentation/applicationservices/kpmdestinationprinter)
- [var kPMDestinationProcessPDF: Int](/documentation/applicationservices/kpmdestinationprocesspdf)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506751-anonymous)

#### Constants

- [var kPMDuplexNoTumble: Int](/documentation/applicationservices/kpmduplexnotumble)
- [var kPMDuplexNone: Int](/documentation/applicationservices/kpmduplexnone)
- [var kPMDuplexTumble: Int](/documentation/applicationservices/kpmduplextumble)
- [var kPMSimplexTumble: Int](/documentation/applicationservices/kpmsimplextumble)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1506805-anonymous)

#### Constants

- [var kPMLayoutBottomTopLeftRight: Int](/documentation/applicationservices/kpmlayoutbottomtopleftright)
- [var kPMLayoutBottomTopRightLeft: Int](/documentation/applicationservices/kpmlayoutbottomtoprightleft)
- [var kPMLayoutLeftRightBottomTop: Int](/documentation/applicationservices/kpmlayoutleftrightbottomtop)
- [var kPMLayoutLeftRightTopBottom: Int](/documentation/applicationservices/kpmlayoutleftrighttopbottom)
- [var kPMLayoutRightLeftBottomTop: Int](/documentation/applicationservices/kpmlayoutrightleftbottomtop)
- [var kPMLayoutRightLeftTopBottom: Int](/documentation/applicationservices/kpmlayoutrightlefttopbottom)
- [var kPMLayoutTopBottomLeftRight: Int](/documentation/applicationservices/kpmlayouttopbottomleftright)
- [var kPMLayoutTopBottomRightLeft: Int](/documentation/applicationservices/kpmlayouttopbottomrightleft)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1561493-anonymous)

#### Constants

- [var kColorSyncAlphaInfoMask: Int](/documentation/colorsync/kcolorsyncalphainfomask)
- [var kColorSyncByteOrder16Big: Int](/documentation/colorsync/kcolorsyncbyteorder16big)
- [var kColorSyncByteOrder16Little: Int](/documentation/colorsync/kcolorsyncbyteorder16little)
- [var kColorSyncByteOrder32Big: Int](/documentation/colorsync/kcolorsyncbyteorder32big)
- [var kColorSyncByteOrder32Little: Int](/documentation/colorsync/kcolorsyncbyteorder32little)
- [var kColorSyncByteOrderDefault: Int](/documentation/colorsync/kcolorsyncbyteorderdefault)
- [var kColorSyncByteOrderMask: Int](/documentation/colorsync/kcolorsyncbyteordermask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550906-anonymous)

#### Constants

- [var kATSFontFormatUnspecified: Int](/documentation/applicationservices/katsfontformatunspecified)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550905-anonymous)

#### Constants

- [var kFMFontCallbackFilterSelector: Int](/documentation/applicationservices/kfmfontcallbackfilterselector)
- [var kFMFontContainerFilterSelector: Int](/documentation/applicationservices/kfmfontcontainerfilterselector)
- [var kFMFontDirectoryFilterSelector: Int](/documentation/applicationservices/kfmfontdirectoryfilterselector)
- [var kFMFontFamilyCallbackFilterSelector: Int](/documentation/applicationservices/kfmfontfamilycallbackfilterselector)
- [var kFMFontFileRefFilterSelector: Int](/documentation/applicationservices/kfmfontfilereffilterselector)
- [var kFMFontTechnologyFilterSelector: Int](/documentation/applicationservices/kfmfonttechnologyfilterselector)
- [var kFMGenerationFilterSelector: Int](/documentation/applicationservices/kfmgenerationfilterselector)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550897-anonymous)

#### Constants

- [var kATSDeletedGlyphcode: Int](/documentation/applicationservices/katsdeletedglyphcode)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550902-anonymous)

#### Constants

- [var kATSBoldQDStretch: Int](/documentation/applicationservices/katsboldqdstretch)
- [var kATSItalicQDSkew: Int](/documentation/applicationservices/katsitalicqdskew)
- [var kATSRadiansFactor: Int](/documentation/applicationservices/katsradiansfactor)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550911-anonymous)

#### Constants

- [var kFMPostScriptFontTechnology: Int](/documentation/applicationservices/kfmpostscriptfonttechnology)
- [var kFMTrueTypeFontTechnology: Int](/documentation/applicationservices/kfmtruetypefonttechnology)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550904-anonymous)

#### Constants

- [var kInvalidFont: Int](/documentation/applicationservices/kinvalidfont)
- [var kInvalidFontFamily: Int](/documentation/applicationservices/kinvalidfontfamily)
- [var kInvalidGeneration: Int](/documentation/applicationservices/kinvalidgeneration)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550901-anonymous)

#### Constants

- [var kATSFontContainerRefUnspecified: Int](/documentation/applicationservices/katsfontcontainerrefunspecified)
- [var kATSFontFamilyRefUnspecified: Int](/documentation/applicationservices/katsfontfamilyrefunspecified)
- [var kATSFontRefUnspecified: Int](/documentation/applicationservices/katsfontrefunspecified)
- [var kATSGenerationUnspecified: Int](/documentation/applicationservices/katsgenerationunspecified)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550895-anonymous)

#### Constants

- [var kATSCubicCurveType: Int](/documentation/applicationservices/katscubiccurvetype)
- [var kATSOtherCurveType: Int](/documentation/applicationservices/katsothercurvetype)
- [var kATSQuadCurveType: Int](/documentation/applicationservices/katsquadcurvetype)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1550913-anonymous)

#### Constants

- [var kFMCurrentFilterFormat: Int](/documentation/applicationservices/kfmcurrentfilterformat)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1560580-anonymous)

#### Constants

- [var cmBradfordChromaticAdaptation: Int](/documentation/applicationservices/cmbradfordchromaticadaptation)
- [var cmLinearChromaticAdaptation: Int](/documentation/applicationservices/cmlinearchromaticadaptation)
- [var cmUseDefaultChromaticAdaptation: Int](/documentation/applicationservices/cmusedefaultchromaticadaptation)
- [var cmVonKriesChromaticAdaptation: Int](/documentation/applicationservices/cmvonkrieschromaticadaptation)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1560338-anonymous)

#### Constants

- [var cmBlackPointCompensation: Int](/documentation/applicationservices/cmblackpointcompensation)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1560256-anonymous)

#### Constants

- [var cmARGB32PmulSpace: Int](/documentation/applicationservices/cmargb32pmulspace)
- [var cmARGB32Space: Int](/documentation/applicationservices/cmargb32space)
- [var cmARGB64LPmulSpace: Int](/documentation/applicationservices/cmargb64lpmulspace)
- [var cmARGB64LSpace: Int](/documentation/applicationservices/cmargb64lspace)
- [var cmARGB64PmulSpace: Int](/documentation/applicationservices/cmargb64pmulspace)
- [var cmARGB64Space: Int](/documentation/applicationservices/cmargb64space)
- [var cmCMYK32Space: Int](/documentation/applicationservices/cmcmyk32space)
- [var cmCMYK64LSpace: Int](/documentation/applicationservices/cmcmyk64lspace)
- [var cmCMYK64Space: Int](/documentation/applicationservices/cmcmyk64space)
- [var cmGamutResult1Space: Int](/documentation/applicationservices/cmgamutresult1space)
- [var cmGray16LSpace: Int](/documentation/applicationservices/cmgray16lspace)
- [var cmGray16Space: Int](/documentation/applicationservices/cmgray16space)
- [var cmGray8Space: Int](/documentation/applicationservices/cmgray8space)
- [var cmGrayA16PmulSpace: Int](/documentation/applicationservices/cmgraya16pmulspace)
- [var cmGrayA16Space: Int](/documentation/applicationservices/cmgraya16space)
- [var cmGrayA32LPmulSpace: Int](/documentation/applicationservices/cmgraya32lpmulspace)
- [var cmGrayA32LSpace: Int](/documentation/applicationservices/cmgraya32lspace)
- [var cmGrayA32PmulSpace: Int](/documentation/applicationservices/cmgraya32pmulspace)
- [var cmGrayA32Space: Int](/documentation/applicationservices/cmgraya32space)
- [var cmHLS32Space: Int](/documentation/applicationservices/cmhls32space)
- [var cmHSV32Space: Int](/documentation/applicationservices/cmhsv32space)
- [var cmLAB24Space: Int](/documentation/applicationservices/cmlab24space)
- [var cmLAB32Space: Int](/documentation/applicationservices/cmlab32space)
- [var cmLAB48LSpace: Int](/documentation/applicationservices/cmlab48lspace)
- [var cmLAB48Space: Int](/documentation/applicationservices/cmlab48space)
- [var cmLUV32Space: Int](/documentation/applicationservices/cmluv32space)
- [var cmMCEight8Space: Int](/documentation/applicationservices/cmmceight8space)
- [var cmMCFive8Space: Int](/documentation/applicationservices/cmmcfive8space)
- [var cmMCSeven8Space: Int](/documentation/applicationservices/cmmcseven8space)
- [var cmMCSix8Space: Int](/documentation/applicationservices/cmmcsix8space)
- [var cmNamedIndexed32LSpace: Int](/documentation/applicationservices/cmnamedindexed32lspace)
- [var cmNamedIndexed32Space: Int](/documentation/applicationservices/cmnamedindexed32space)
- [var cmRGB16LSpace: Int](/documentation/applicationservices/cmrgb16lspace)
- [var cmRGB16Space: Int](/documentation/applicationservices/cmrgb16space)
- [var cmRGB24Space: Int](/documentation/applicationservices/cmrgb24space)
- [var cmRGB32Space: Int](/documentation/applicationservices/cmrgb32space)
- [var cmRGB48LSpace: Int](/documentation/applicationservices/cmrgb48lspace)
- [var cmRGB48Space: Int](/documentation/applicationservices/cmrgb48space)
- [var cmRGB565LSpace: Int](/documentation/applicationservices/cmrgb565lspace)
- [var cmRGB565Space: Int](/documentation/applicationservices/cmrgb565space)
- [var cmRGBA32PmulSpace: Int](/documentation/applicationservices/cmrgba32pmulspace)
- [var cmRGBA32Space: Int](/documentation/applicationservices/cmrgba32space)
- [var cmRGBA64LPmulSpace: Int](/documentation/applicationservices/cmrgba64lpmulspace)
- [var cmRGBA64LSpace: Int](/documentation/applicationservices/cmrgba64lspace)
- [var cmRGBA64PmulSpace: Int](/documentation/applicationservices/cmrgba64pmulspace)
- [var cmRGBA64Space: Int](/documentation/applicationservices/cmrgba64space)
- [var cmXYZ24Space: Int](/documentation/applicationservices/cmxyz24space)
- [var cmXYZ32Space: Int](/documentation/applicationservices/cmxyz32space)
- [var cmXYZ48LSpace: Int](/documentation/applicationservices/cmxyz48lspace)
- [var cmXYZ48Space: Int](/documentation/applicationservices/cmxyz48space)
- [var cmYXY32Space: Int](/documentation/applicationservices/cmyxy32space)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1560667-anonymous)

#### Constants

- [var cmCameraDeviceClass: Int](/documentation/applicationservices/cmcameradeviceclass)
- [var cmDisplayDeviceClass: Int](/documentation/applicationservices/cmdisplaydeviceclass)
- [var cmPrinterDeviceClass: Int](/documentation/applicationservices/cmprinterdeviceclass)
- [var cmProofDeviceClass: Int](/documentation/applicationservices/cmproofdeviceclass)
- [var cmScannerDeviceClass: Int](/documentation/applicationservices/cmscannerdeviceclass)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1560507-anonymous)

#### Constants

- [var cmDeviceAlreadyRegistered: Int](/documentation/applicationservices/cmdevicealreadyregistered)
- [var cmDeviceDBNotFoundErr: Int](/documentation/applicationservices/cmdevicedbnotfounderr)
- [var cmDeviceNotRegistered: Int](/documentation/applicationservices/cmdevicenotregistered)
- [var cmDeviceProfilesNotFound: Int](/documentation/applicationservices/cmdeviceprofilesnotfound)
- [var cmInternalCFErr: Int](/documentation/applicationservices/cminternalcferr)
- [var cmPrefsSynchError: Int](/documentation/applicationservices/cmprefssyncherror)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1516910-anonymous)

#### Constants

- [var kATSUseCaretOrigins: Int](/documentation/applicationservices/katsusecaretorigins)
- [var kATSUseDeviceOrigins: Int](/documentation/applicationservices/katsusedeviceorigins)
- [var kATSUseFractionalOrigins: Int](/documentation/applicationservices/katsusefractionalorigins)
- [var kATSUseOriginFlags: Int](/documentation/applicationservices/katsuseoriginflags)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1516838-anonymous)

#### Constants

- [var kATSStyleAppleReserved: UInt32](/documentation/applicationservices/katsstyleapplereserved)
- [var kATSStyleApplyAntiAliasing: UInt32](/documentation/applicationservices/katsstyleapplyantialiasing)
- [var kATSStyleApplyHints: UInt32](/documentation/applicationservices/katsstyleapplyhints)
- [var kATSStyleNoAntiAliasing: UInt32](/documentation/applicationservices/katsstylenoantialiasing)
- [var kATSStyleNoHinting: UInt32](/documentation/applicationservices/katsstylenohinting)
- [var kATSStyleNoOptions: UInt32](/documentation/applicationservices/katsstylenooptions)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1516876-anonymous)

#### Constants

- [var kATSULayoutOperationAppleReserved: UInt32](/documentation/applicationservices/katsulayoutoperationapplereserved)
- [var kATSULayoutOperationBaselineAdjustment: UInt32](/documentation/applicationservices/katsulayoutoperationbaselineadjustment)
- [var kATSULayoutOperationJustification: UInt32](/documentation/applicationservices/katsulayoutoperationjustification)
- [var kATSULayoutOperationKerningAdjustment: UInt32](/documentation/applicationservices/katsulayoutoperationkerningadjustment)
- [var kATSULayoutOperationMorph: UInt32](/documentation/applicationservices/katsulayoutoperationmorph)
- [var kATSULayoutOperationNone: UInt32](/documentation/applicationservices/katsulayoutoperationnone)
- [var kATSULayoutOperationPostLayoutAdjustment: UInt32](/documentation/applicationservices/katsulayoutoperationpostlayoutadjustment)
- [var kATSULayoutOperationTrackingAdjustment: UInt32](/documentation/applicationservices/katsulayoutoperationtrackingadjustment)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1516921-anonymous)

#### Constants

- [var kATSLineAppleReserved: UInt32](/documentation/applicationservices/katslineapplereserved)
- [var kATSLineApplyAntiAliasing: UInt32](/documentation/applicationservices/katslineapplyantialiasing)
- [var kATSLineBreakToNearestCharacter: UInt32](/documentation/applicationservices/katslinebreaktonearestcharacter)
- [var kATSLineDisableAllBaselineAdjustments: UInt32](/documentation/applicationservices/katslinedisableallbaselineadjustments)
- [var kATSLineDisableAllGlyphMorphing: UInt32](/documentation/applicationservices/katslinedisableallglyphmorphing)
- [var kATSLineDisableAllJustification: UInt32](/documentation/applicationservices/katslinedisablealljustification)
- [var kATSLineDisableAllKerningAdjustments: UInt32](/documentation/applicationservices/katslinedisableallkerningadjustments)
- [var kATSLineDisableAllLayoutOperations: UInt32](/documentation/applicationservices/katslinedisablealllayoutoperations)
- [var kATSLineDisableAllTrackingAdjustments: UInt32](/documentation/applicationservices/katslinedisablealltrackingadjustments)
- [var kATSLineDisableAutoAdjustDisplayPos: UInt32](/documentation/applicationservices/katslinedisableautoadjustdisplaypos)
- [var kATSLineDisableNegativeJustification: UInt32](/documentation/applicationservices/katslinedisablenegativejustification)
- [var kATSLineFillOutToWidth: UInt32](/documentation/applicationservices/katslinefillouttowidth)
- [var kATSLineFractDisable: UInt32](/documentation/applicationservices/katslinefractdisable)
- [var kATSLineHasNoHangers: UInt32](/documentation/applicationservices/katslinehasnohangers)
- [var kATSLineHasNoOpticalAlignment: UInt32](/documentation/applicationservices/katslinehasnoopticalalignment)
- [var kATSLineIgnoreFontLeading: UInt32](/documentation/applicationservices/katslineignorefontleading)
- [var kATSLineImposeNoAngleForEnds: UInt32](/documentation/applicationservices/katslineimposenoangleforends)
- [var kATSLineIsDisplayOnly: UInt32](/documentation/applicationservices/katslineisdisplayonly)
- [var kATSLineKeepSpacesOutOfMargin: UInt32](/documentation/applicationservices/katslinekeepspacesoutofmargin)
- [var kATSLineLastNoJustification: UInt32](/documentation/applicationservices/katslinelastnojustification)
- [var kATSLineNoAntiAliasing: UInt32](/documentation/applicationservices/katslinenoantialiasing)
- [var kATSLineNoLayoutOptions: UInt32](/documentation/applicationservices/katslinenolayoutoptions)
- [var kATSLineNoSpecialJustification: UInt32](/documentation/applicationservices/katslinenospecialjustification)
- [var kATSLineTabAdjustEnabled: UInt32](/documentation/applicationservices/katslinetabadjustenabled)
- [var kATSLineUseDeviceMetrics: UInt32](/documentation/applicationservices/katslineusedevicemetrics)
- [var kATSLineUseQDRendering: UInt32](/documentation/applicationservices/katslineuseqdrendering)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1516884-anonymous)

#### Constants

- [var kATSNoTracking: Int](/documentation/applicationservices/katsnotracking)
- [var kATSUseGlyphAdvance: Int](/documentation/applicationservices/katsuseglyphadvance)
- [var kATSUseLineHeight: Int](/documentation/applicationservices/katsuselineheight)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1516882-anonymous)

#### Constants

- [var kATSULayoutOperationCallbackStatusContinue: Int](/documentation/applicationservices/katsulayoutoperationcallbackstatuscontinue)
- [var kATSULayoutOperationCallbackStatusHandled: Int](/documentation/applicationservices/katsulayoutoperationcallbackstatushandled)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1516912-anonymous)

#### Constants

- [var kATSGlyphInfoAppleReserved: UInt32](/documentation/applicationservices/katsglyphinfoapplereserved)
- [var kATSGlyphInfoByteSizeMask: UInt32](/documentation/applicationservices/katsglyphinfobytesizemask)
- [var kATSGlyphInfoHasImposedWidth: UInt32](/documentation/applicationservices/katsglyphinfohasimposedwidth)
- [var kATSGlyphInfoIsAttachment: UInt32](/documentation/applicationservices/katsglyphinfoisattachment)
- [var kATSGlyphInfoIsLTHanger: UInt32](/documentation/applicationservices/katsglyphinfoislthanger)
- [var kATSGlyphInfoIsRBHanger: UInt32](/documentation/applicationservices/katsglyphinfoisrbhanger)
- [var kATSGlyphInfoIsWhiteSpace: UInt32](/documentation/applicationservices/katsglyphinfoiswhitespace)
- [var kATSGlyphInfoTerminatorGlyph: UInt32](/documentation/applicationservices/katsglyphinfoterminatorglyph)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1563659-anonymous)

#### Constants

- [var kATSOptionFlagsActivateDisabled: Int](/documentation/applicationservices/katsoptionflagsactivatedisabled)
- [var kATSOptionFlagsDoNotNotify: Int](/documentation/applicationservices/katsoptionflagsdonotnotify)
- [var kATSOptionFlagsProcessSubdirectories: Int](/documentation/applicationservices/katsoptionflagsprocesssubdirectories)
- [var kATSOptionFlagsRecordPersistently: Int](/documentation/applicationservices/katsoptionflagsrecordpersistently)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1563695-anonymous)

#### Constants

- [var kATSOptionFlagsDefaultScope: Int](/documentation/applicationservices/katsoptionflagsdefaultscope)
- [var kATSOptionFlagsIncludeDisabledMask: Int](/documentation/applicationservices/katsoptionflagsincludedisabledmask)
- [var kATSOptionFlagsIterateByPrecedenceMask: Int](/documentation/applicationservices/katsoptionflagsiteratebyprecedencemask)
- [var kATSOptionFlagsIterationScopeMask: Int](/documentation/applicationservices/katsoptionflagsiterationscopemask)
- [var kATSOptionFlagsRestrictedScope: Int](/documentation/applicationservices/katsoptionflagsrestrictedscope)
- [var kATSOptionFlagsUnRestrictedScope: Int](/documentation/applicationservices/katsoptionflagsunrestrictedscope)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1563700-anonymous)

#### Constants

- [var kATSFontContextGlobal: Int](/documentation/applicationservices/katsfontcontextglobal)
- [var kATSFontContextLocal: Int](/documentation/applicationservices/katsfontcontextlocal)
- [var kATSFontContextUnspecified: Int](/documentation/applicationservices/katsfontcontextunspecified)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1563660-anonymous)

#### Constants

- [var kATSFontAutoActivationAsk: Int](/documentation/applicationservices/katsfontautoactivationask)
- [var kATSFontAutoActivationDefault: Int](/documentation/applicationservices/katsfontautoactivationdefault)
- [var kATSFontAutoActivationDisabled: Int](/documentation/applicationservices/katsfontautoactivationdisabled)
- [var kATSFontAutoActivationEnabled: Int](/documentation/applicationservices/katsfontautoactivationenabled)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1563683-anonymous)

#### Constants

- [var kATSInvalidFontAccess: Int](/documentation/applicationservices/katsinvalidfontaccess)
- [var kATSInvalidFontContainerAccess: Int](/documentation/applicationservices/katsinvalidfontcontaineraccess)
- [var kATSInvalidFontFamilyAccess: Int](/documentation/applicationservices/katsinvalidfontfamilyaccess)
- [var kATSInvalidFontTableAccess: Int](/documentation/applicationservices/katsinvalidfonttableaccess)
- [var kATSInvalidGlyphAccess: Int](/documentation/applicationservices/katsinvalidglyphaccess)
- [var kATSIterationCompleted: Int](/documentation/applicationservices/katsiterationcompleted)
- [var kATSIterationScopeModified: Int](/documentation/applicationservices/katsiterationscopemodified)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1563698-anonymous)

#### Constants

- [var kATSOptionFlagsComposeFontPostScriptName: Int](/documentation/applicationservices/katsoptionflagscomposefontpostscriptname)
- [var kATSOptionFlagsDefault: Int](/documentation/applicationservices/katsoptionflagsdefault)
- [var kATSOptionFlagsUseDataFork: Int](/documentation/applicationservices/katsoptionflagsusedatafork)
- [var kATSOptionFlagsUseDataForkAsResourceFork: Int](/documentation/applicationservices/katsoptionflagsusedataforkasresourcefork)
- [var kATSOptionFlagsUseResourceFork: Int](/documentation/applicationservices/katsoptionflagsuseresourcefork)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1563652-anonymous)

#### Constants

- [var kATSFontFilterCurrentVersion: Int](/documentation/applicationservices/katsfontfiltercurrentversion)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1572714-anonymous)

#### Constants

- [var kHIShapeParseFromBottom: Int](/documentation/applicationservices/khishapeparsefrombottom)
- [var kHIShapeParseFromBottomRight: Int](/documentation/applicationservices/khishapeparsefrombottomright)
- [var kHIShapeParseFromLeft: Int](/documentation/applicationservices/khishapeparsefromleft)
- [var kHIShapeParseFromRight: Int](/documentation/applicationservices/khishapeparsefromright)
- [var kHIShapeParseFromTop: Int](/documentation/applicationservices/khishapeparsefromtop)
- [var kHIShapeParseFromTopLeft: Int](/documentation/applicationservices/khishapeparsefromtopleft)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1572715-anonymous)

#### Constants

- [var kHIShapeEnumerateInit: Int](/documentation/applicationservices/khishapeenumerateinit)
- [var kHIShapeEnumerateRect: Int](/documentation/applicationservices/khishapeenumeraterect)
- [var kHIShapeEnumerateTerminate: Int](/documentation/applicationservices/khishapeenumerateterminate)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1560805-anonymous)

#### Constants

- [var kTranslationDataTranslation: Int](/documentation/applicationservices/ktranslationdatatranslation)
- [var kTranslationFileTranslation: Int](/documentation/applicationservices/ktranslationfiletranslation)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1560806-anonymous)

#### Constants

- [var badTranslationRefErr: Int](/documentation/applicationservices/badtranslationreferr)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1501044-anonymous)

#### Constants

- [var cdevGenErr: Int](/documentation/applicationservices/cdevgenerr)
- [var cdevMemErr: Int](/documentation/applicationservices/cdevmemerr)
- [var cdevResErr: Int](/documentation/applicationservices/cdevreserr)
- [var cdevUnset: Int](/documentation/applicationservices/cdevunset)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1501094-anonymous)

#### Constants

- [var activDev: Int](/documentation/applicationservices/activdev)
- [var clearDev: Int](/documentation/applicationservices/cleardev)
- [var closeDev: Int](/documentation/applicationservices/closedev)
- [var copyDev: Int](/documentation/applicationservices/copydev)
- [var cursorDev: Int](/documentation/applicationservices/cursordev)
- [var cutDev: Int](/documentation/applicationservices/cutdev)
- [var deactivDev: Int](/documentation/applicationservices/deactivdev)
- [var hitDev: Int](/documentation/applicationservices/hitdev)
- [var initDev: Int](/documentation/applicationservices/initdev)
- [var keyEvtDev: Int](/documentation/applicationservices/keyevtdev)
- [var macDev: Int](/documentation/applicationservices/macdev)
- [var nulDev: Int](/documentation/applicationservices/nuldev)
- [var pasteDev: Int](/documentation/applicationservices/pastedev)
- [var undoDev: Int](/documentation/applicationservices/undodev)
- [var updateDev: Int](/documentation/applicationservices/updatedev)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1500982-anonymous)

#### Constants

- [var kProcessDictionaryIncludeAllInformationMask: Int](/documentation/applicationservices/kprocessdictionaryincludeallinformationmask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1501086-anonymous)

#### Constants

- [var kQuitAtNormalTimeMask: Int](/documentation/applicationservices/kquitatnormaltimemask)
- [var kQuitBeforeFBAsQuitMask: Int](/documentation/applicationservices/kquitbeforefbasquitmask)
- [var kQuitBeforeNormalTimeMask: Int](/documentation/applicationservices/kquitbeforenormaltimemask)
- [var kQuitBeforeShellQuitsMask: Int](/documentation/applicationservices/kquitbeforeshellquitsmask)
- [var kQuitBeforeTerminatorAppQuitsMask: Int](/documentation/applicationservices/kquitbeforeterminatorappquitsmask)
- [var kQuitNeverMask: Int](/documentation/applicationservices/kquitnevermask)
- [var kQuitNotQuitDuringInstallMask: Int](/documentation/applicationservices/kquitnotquitduringinstallmask)
- [var kQuitNotQuitDuringLogoutMask: Int](/documentation/applicationservices/kquitnotquitduringlogoutmask)
- [var kQuitOptionsMask: Int](/documentation/applicationservices/kquitoptionsmask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1500998-anonymous)

#### Constants

- [var mode32BitCompatible: Int](/documentation/applicationservices/mode32bitcompatible)
- [var modeCanBackground: Int](/documentation/applicationservices/modecanbackground)
- [var modeControlPanel: Int](/documentation/applicationservices/modecontrolpanel)
- [var modeDeskAccessory: Int](/documentation/applicationservices/modedeskaccessory)
- [var modeDisplayManagerAware: Int](/documentation/applicationservices/modedisplaymanageraware)
- [var modeDoesActivateOnFGSwitch: Int](/documentation/applicationservices/modedoesactivateonfgswitch)
- [var modeGetAppDiedMsg: Int](/documentation/applicationservices/modegetappdiedmsg)
- [var modeGetFrontClicks: Int](/documentation/applicationservices/modegetfrontclicks)
- [var modeHighLevelEventAware: Int](/documentation/applicationservices/modehighleveleventaware)
- [var modeLaunchDontSwitch: Int](/documentation/applicationservices/modelaunchdontswitch)
- [var modeLocalAndRemoteHLEvents: Int](/documentation/applicationservices/modelocalandremotehlevents)
- [var modeMultiLaunch: Int](/documentation/applicationservices/modemultilaunch)
- [var modeNeedSuspendResume: Int](/documentation/applicationservices/modeneedsuspendresume)
- [var modeOnlyBackground: Int](/documentation/applicationservices/modeonlybackground)
- [var modeReserved: Int](/documentation/applicationservices/modereserved)
- [var modeStationeryAware: Int](/documentation/applicationservices/modestationeryaware)
- [var modeUseTextEditServices: Int](/documentation/applicationservices/modeusetexteditservices)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1501055-anonymous)

#### Constants

- [var launchAllow24Bit: Int](/documentation/applicationservices/launchallow24bit)
- [var launchContinue: Int](/documentation/applicationservices/launchcontinue)
- [var launchDontSwitch: Int](/documentation/applicationservices/launchdontswitch)
- [var launchInhibitDaemon: Int](/documentation/applicationservices/launchinhibitdaemon)
- [var launchNoFileFlags: Int](/documentation/applicationservices/launchnofileflags)
- [var launchUseMinimum: Int](/documentation/applicationservices/launchuseminimum)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1501096-anonymous)

#### Constants

- [var kCurrentProcess: Int](/documentation/applicationservices/kcurrentprocess)
- [var kNoProcess: Int](/documentation/applicationservices/knoprocess)
- [var kSystemProcess: Int](/documentation/applicationservices/ksystemprocess)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1501101-anonymous)

#### Constants

- [var kSetFrontProcessCausedByUser: Int](/documentation/applicationservices/ksetfrontprocesscausedbyuser)
- [var kSetFrontProcessFrontWindowOnly: Int](/documentation/applicationservices/ksetfrontprocessfrontwindowonly)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1500996-anonymous)

#### Constants

- [var extendedBlock: Int](/documentation/applicationservices/extendedblock)
- [var extendedBlockLen: Int](/documentation/applicationservices/extendedblocklen)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1501117-anonymous)

#### Constants

- [var kProcessTransformToBackgroundApplication: Int](/documentation/applicationservices/kprocesstransformtobackgroundapplication)
- [var kProcessTransformToForegroundApplication: Int](/documentation/applicationservices/kprocesstransformtoforegroundapplication)
- [var kProcessTransformToUIElementApplication: Int](/documentation/applicationservices/kprocesstransformtouielementapplication)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452070-anonymous)

#### Constants

- [var kATSUDefaultFontFallbacks: Int](/documentation/applicationservices/katsudefaultfontfallbacks)
- [var kATSULastResortOnlyFallback: Int](/documentation/applicationservices/katsulastresortonlyfallback)
- [var kATSUSequentialFallbacksExclusive: Int](/documentation/applicationservices/katsusequentialfallbacksexclusive)
- [var kATSUSequentialFallbacksPreferred: Int](/documentation/applicationservices/katsusequentialfallbackspreferred)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452151-anonymous)

#### Constants

- [var kATSUByCharacter: Int](/documentation/applicationservices/katsubycharacter)
- [var kATSUByCharacterCluster: Int](/documentation/applicationservices/katsubycharactercluster)
- [var kATSUByCluster: Int](/documentation/applicationservices/katsubycluster)
- [var kATSUByTypographicCluster: Int](/documentation/applicationservices/katsubytypographiccluster)
- [var kATSUByWord: Int](/documentation/applicationservices/katsubyword)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452352-anonymous)

#### Constants

- [var kATSUStronglyHorizontal: Int](/documentation/applicationservices/katsustronglyhorizontal)
- [var kATSUStronglyVertical: Int](/documentation/applicationservices/katsustronglyvertical)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452210-anonymous)

#### Constants

- [var kInvertHighlighting: Int](/documentation/applicationservices/kinverthighlighting)
- [var kRedrawHighlighting: Int](/documentation/applicationservices/kredrawhighlighting)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452020-anonymous)

#### Constants

- [var kATSUStyleContainedBy: Int](/documentation/applicationservices/katsustylecontainedby)
- [var kATSUStyleContains: Int](/documentation/applicationservices/katsustylecontains)
- [var kATSUStyleEquals: Int](/documentation/applicationservices/katsustyleequals)
- [var kATSUStyleUnequal: Int](/documentation/applicationservices/katsustyleunequal)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452085-anonymous)

#### Constants

- [var kATSUClearAll: UInt32](/documentation/applicationservices/katsuclearall)
- [var kATSUUseGrafPortPenLoc: UInt32](/documentation/applicationservices/katsuusegrafportpenloc)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452064-anonymous)

#### Constants

- [var kATSUCenterTab: Int](/documentation/applicationservices/katsucentertab)
- [var kATSUDecimalTab: Int](/documentation/applicationservices/katsudecimaltab)
- [var kATSULeftTab: Int](/documentation/applicationservices/katsulefttab)
- [var kATSUNumberTabTypes: Int](/documentation/applicationservices/katsunumbertabtypes)
- [var kATSURightTab: Int](/documentation/applicationservices/katsurighttab)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452336-anonymous)

#### Constants

- [var kATSUTruncFeatNoSquishing: Int](/documentation/applicationservices/katsutruncfeatnosquishing)
- [var kATSUTruncateEnd: Int](/documentation/applicationservices/katsutruncateend)
- [var kATSUTruncateMiddle: Int](/documentation/applicationservices/katsutruncatemiddle)
- [var kATSUTruncateNone: Int](/documentation/applicationservices/katsutruncatenone)
- [var kATSUTruncateSpecificationMask: Int](/documentation/applicationservices/katsutruncatespecificationmask)
- [var kATSUTruncateStart: Int](/documentation/applicationservices/katsutruncatestart)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452068-anonymous)

#### Constants

- [var kATSULeftToRightBaseDirection: Int](/documentation/applicationservices/katsulefttorightbasedirection)
- [var kATSURightToLeftBaseDirection: Int](/documentation/applicationservices/katsurighttoleftbasedirection)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452073-anonymous)

#### Constants

- [var kGlyphCollectionAdobeCNS1: Int](/documentation/applicationservices/kglyphcollectionadobecns1)
- [var kGlyphCollectionAdobeGB1: Int](/documentation/applicationservices/kglyphcollectionadobegb1)
- [var kGlyphCollectionAdobeJapan1: Int](/documentation/applicationservices/kglyphcollectionadobejapan1)
- [var kGlyphCollectionAdobeJapan2: Int](/documentation/applicationservices/kglyphcollectionadobejapan2)
- [var kGlyphCollectionAdobeKorea1: Int](/documentation/applicationservices/kglyphcollectionadobekorea1)
- [var kGlyphCollectionGID: Int](/documentation/applicationservices/kglyphcollectiongid)
- [var kGlyphCollectionUnspecified: Int](/documentation/applicationservices/kglyphcollectionunspecified)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452284-anonymous)

#### Constants

- [var kATSUStyleDoubleLineCount: Int](/documentation/applicationservices/katsustyledoublelinecount)
- [var kATSUStyleSingleLineCount: Int](/documentation/applicationservices/katsustylesinglelinecount)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1451999-anonymous)

#### Constants

- [var kATSUInvalidFontID: Int](/documentation/applicationservices/katsuinvalidfontid)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452204-anonymous)

#### Constants

- [var kATSUAfterWithStreamShiftTag: Int](/documentation/applicationservices/katsuafterwithstreamshifttag)
- [var kATSUAscentTag: Int](/documentation/applicationservices/katsuascenttag)
- [var kATSUBaselineClassTag: Int](/documentation/applicationservices/katsubaselineclasstag)
- [var kATSUBeforeWithStreamShiftTag: Int](/documentation/applicationservices/katsubeforewithstreamshifttag)
- [var kATSUCGContextTag: Int](/documentation/applicationservices/katsucgcontexttag)
- [var kATSUColorTag: Int](/documentation/applicationservices/katsucolortag)
- [var kATSUCrossStreamShiftTag: Int](/documentation/applicationservices/katsucrossstreamshifttag)
- [var kATSUDecompositionFactorTag: Int](/documentation/applicationservices/katsudecompositionfactortag)
- [var kATSUDescentTag: Int](/documentation/applicationservices/katsudescenttag)
- [var kATSUFontMatrixTag: Int](/documentation/applicationservices/katsufontmatrixtag)
- [var kATSUFontTag: Int](/documentation/applicationservices/katsufonttag)
- [var kATSUForceHangingTag: Int](/documentation/applicationservices/katsuforcehangingtag)
- [var kATSUGlyphSelectorTag: Int](/documentation/applicationservices/katsuglyphselectortag)
- [var kATSUHangingInhibitFactorTag: Int](/documentation/applicationservices/katsuhanginginhibitfactortag)
- [var kATSUImposeWidthTag: Int](/documentation/applicationservices/katsuimposewidthtag)
- [var kATSUKerningInhibitFactorTag: Int](/documentation/applicationservices/katsukerninginhibitfactortag)
- [var kATSULangRegionTag: Int](/documentation/applicationservices/katsulangregiontag)
- [var kATSULanguageTag: Int](/documentation/applicationservices/katsulanguagetag)
- [var kATSULayoutOperationOverrideTag: Int](/documentation/applicationservices/katsulayoutoperationoverridetag)
- [var kATSULeadingTag: Int](/documentation/applicationservices/katsuleadingtag)
- [var kATSULineAscentTag: Int](/documentation/applicationservices/katsulineascenttag)
- [var kATSULineBaselineValuesTag: Int](/documentation/applicationservices/katsulinebaselinevaluestag)
- [var kATSULineDecimalTabCharacterTag: Int](/documentation/applicationservices/katsulinedecimaltabcharactertag)
- [var kATSULineDescentTag: Int](/documentation/applicationservices/katsulinedescenttag)
- [var kATSULineDirectionTag: Int](/documentation/applicationservices/katsulinedirectiontag)
- [var kATSULineFlushFactorTag: Int](/documentation/applicationservices/katsulineflushfactortag)
- [var kATSULineFontFallbacksTag: Int](/documentation/applicationservices/katsulinefontfallbackstag)
- [var kATSULineHighlightCGColorTag: Int](/documentation/applicationservices/katsulinehighlightcgcolortag)
- [var kATSULineJustificationFactorTag: Int](/documentation/applicationservices/katsulinejustificationfactortag)
- [var kATSULineLangRegionTag: Int](/documentation/applicationservices/katsulinelangregiontag)
- [var kATSULineLanguageTag: Int](/documentation/applicationservices/katsulinelanguagetag)
- [var kATSULineLayoutOptionsTag: Int](/documentation/applicationservices/katsulinelayoutoptionstag)
- [var kATSULineRotationTag: Int](/documentation/applicationservices/katsulinerotationtag)
- [var kATSULineTextLocatorTag: Int](/documentation/applicationservices/katsulinetextlocatortag)
- [var kATSULineTruncationTag: Int](/documentation/applicationservices/katsulinetruncationtag)
- [var kATSULineWidthTag: Int](/documentation/applicationservices/katsulinewidthtag)
- [var kATSUMaxATSUITagValue: Int](/documentation/applicationservices/katsumaxatsuitagvalue)
- [var kATSUMaxLineTag: Int](/documentation/applicationservices/katsumaxlinetag)
- [var kATSUMaxStyleTag: Int](/documentation/applicationservices/katsumaxstyletag)
- [var kATSUNoCaretAngleTag: Int](/documentation/applicationservices/katsunocaretangletag)
- [var kATSUNoLigatureSplitTag: Int](/documentation/applicationservices/katsunoligaturesplittag)
- [var kATSUNoOpticalAlignmentTag: Int](/documentation/applicationservices/katsunoopticalalignmenttag)
- [var kATSUNoSpecialJustificationTag: Int](/documentation/applicationservices/katsunospecialjustificationtag)
- [var kATSUPriorityJustOverrideTag: Int](/documentation/applicationservices/katsupriorityjustoverridetag)
- [var kATSUQDBoldfaceTag: Int](/documentation/applicationservices/katsuqdboldfacetag)
- [var kATSUQDCondensedTag: Int](/documentation/applicationservices/katsuqdcondensedtag)
- [var kATSUQDExtendedTag: Int](/documentation/applicationservices/katsuqdextendedtag)
- [var kATSUQDItalicTag: Int](/documentation/applicationservices/katsuqditalictag)
- [var kATSUQDUnderlineTag: Int](/documentation/applicationservices/katsuqdunderlinetag)
- [var kATSURGBAlphaColorTag: Int](/documentation/applicationservices/katsurgbalphacolortag)
- [var kATSUSizeTag: Int](/documentation/applicationservices/katsusizetag)
- [var kATSUStyleDropShadowBlurOptionTag: Int](/documentation/applicationservices/katsustyledropshadowbluroptiontag)
- [var kATSUStyleDropShadowColorOptionTag: Int](/documentation/applicationservices/katsustyledropshadowcoloroptiontag)
- [var kATSUStyleDropShadowOffsetOptionTag: Int](/documentation/applicationservices/katsustyledropshadowoffsetoptiontag)
- [var kATSUStyleDropShadowTag: Int](/documentation/applicationservices/katsustyledropshadowtag)
- [var kATSUStyleRenderingOptionsTag: Int](/documentation/applicationservices/katsustylerenderingoptionstag)
- [var kATSUStyleStrikeThroughColorOptionTag: Int](/documentation/applicationservices/katsustylestrikethroughcoloroptiontag)
- [var kATSUStyleStrikeThroughCountOptionTag: Int](/documentation/applicationservices/katsustylestrikethroughcountoptiontag)
- [var kATSUStyleStrikeThroughTag: Int](/documentation/applicationservices/katsustylestrikethroughtag)
- [var kATSUStyleTextLocatorTag: Int](/documentation/applicationservices/katsustyletextlocatortag)
- [var kATSUStyleUnderlineColorOptionTag: Int](/documentation/applicationservices/katsustyleunderlinecoloroptiontag)
- [var kATSUStyleUnderlineCountOptionTag: Int](/documentation/applicationservices/katsustyleunderlinecountoptiontag)
- [var kATSUSuppressCrossKerningTag: Int](/documentation/applicationservices/katsusuppresscrosskerningtag)
- [var kATSUTrackingTag: Int](/documentation/applicationservices/katsutrackingtag)
- [var kATSUVerticalCharacterTag: Int](/documentation/applicationservices/katsuverticalcharactertag)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452264-anonymous)

#### Constants

- [var kATSUFromFollowingLayout: UInt32](/documentation/applicationservices/katsufromfollowinglayout)
- [var kATSUFromPreviousLayout: UInt32](/documentation/applicationservices/katsufrompreviouslayout)
- [var kATSUFromTextBeginning: UInt32](/documentation/applicationservices/katsufromtextbeginning)
- [var kATSUToTextEnd: UInt32](/documentation/applicationservices/katsutotextend)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452003-anonymous)

#### Constants

- [var kATSUUseLineControlWidth: Int](/documentation/applicationservices/katsuuselinecontrolwidth)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452248-anonymous)

#### Constants

- [var kATSUBackgroundCallback: Int](/documentation/applicationservices/katsubackgroundcallback)
- [var kATSUBackgroundColor: Int](/documentation/applicationservices/katsubackgroundcolor)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1452093-anonymous)

#### Constants

- [var kATSUNoSelector: Int](/documentation/applicationservices/katsunoselector)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1570866-anonymous)

#### Constants

- [var kPMAllocationFailure: Int](/documentation/applicationservices/kpmallocationfailure)
- [var kPMCVMSymbolNotFound: Int](/documentation/applicationservices/kpmcvmsymbolnotfound)
- [var kPMCloseFailed: Int](/documentation/applicationservices/kpmclosefailed)
- [var kPMCreateMessageFailed: Int](/documentation/applicationservices/kpmcreatemessagefailed)
- [var kPMDeleteSubTicketFailed: Int](/documentation/applicationservices/kpmdeletesubticketfailed)
- [var kPMDocumentNotFound: Int](/documentation/applicationservices/kpmdocumentnotfound)
- [var kPMDontSwitchPDEError: Int](/documentation/applicationservices/kpmdontswitchpdeerror)
- [var kPMEditRequestFailed: Int](/documentation/applicationservices/kpmeditrequestfailed)
- [var kPMFeatureNotInstalled: Int](/documentation/applicationservices/kpmfeaturenotinstalled)
- [var kPMFileOrDirOperationFailed: Int](/documentation/applicationservices/kpmfileordiroperationfailed)
- [var kPMFontNameTooLong: Int](/documentation/applicationservices/kpmfontnametoolong)
- [var kPMFontNotFound: Int](/documentation/applicationservices/kpmfontnotfound)
- [var kPMGeneralCGError: Int](/documentation/applicationservices/kpmgeneralcgerror)
- [var kPMIOAttrNotAvailable: Int](/documentation/applicationservices/kpmioattrnotavailable)
- [var kPMIOMSymbolNotFound: Int](/documentation/applicationservices/kpmiomsymbolnotfound)
- [var kPMInternalError: Int](/documentation/applicationservices/kpminternalerror)
- [var kPMInvalidAllocator: Int](/documentation/applicationservices/kpminvalidallocator)
- [var kPMInvalidCVMContext: Int](/documentation/applicationservices/kpminvalidcvmcontext)
- [var kPMInvalidCalibrationTarget: Int](/documentation/applicationservices/kpminvalidcalibrationtarget)
- [var kPMInvalidConnection: Int](/documentation/applicationservices/kpminvalidconnection)
- [var kPMInvalidFileType: Int](/documentation/applicationservices/kpminvalidfiletype)
- [var kPMInvalidIOMContext: Int](/documentation/applicationservices/kpminvalidiomcontext)
- [var kPMInvalidIndex: Int](/documentation/applicationservices/kpminvalidindex)
- [var kPMInvalidItem: Int](/documentation/applicationservices/kpminvaliditem)
- [var kPMInvalidJobID: Int](/documentation/applicationservices/kpminvalidjobid)
- [var kPMInvalidJobTemplate: Int](/documentation/applicationservices/kpminvalidjobtemplate)
- [var kPMInvalidKey: Int](/documentation/applicationservices/kpminvalidkey)
- [var kPMInvalidLookupSpec: Int](/documentation/applicationservices/kpminvalidlookupspec)
- [var kPMInvalidObject: Int](/documentation/applicationservices/kpminvalidobject)
- [var kPMInvalidPBMRef: Int](/documentation/applicationservices/kpminvalidpbmref)
- [var kPMInvalidPDEContext: Int](/documentation/applicationservices/kpminvalidpdecontext)
- [var kPMInvalidPMContext: Int](/documentation/applicationservices/kpminvalidpmcontext)
- [var kPMInvalidPaper: Int](/documentation/applicationservices/kpminvalidpaper)
- [var kPMInvalidPrinterAddress: Int](/documentation/applicationservices/kpminvalidprinteraddress)
- [var kPMInvalidPrinterInfo: Int](/documentation/applicationservices/kpminvalidprinterinfo)
- [var kPMInvalidReply: Int](/documentation/applicationservices/kpminvalidreply)
- [var kPMInvalidState: Int](/documentation/applicationservices/kpminvalidstate)
- [var kPMInvalidSubTicket: Int](/documentation/applicationservices/kpminvalidsubticket)
- [var kPMInvalidTicket: Int](/documentation/applicationservices/kpminvalidticket)
- [var kPMInvalidType: Int](/documentation/applicationservices/kpminvalidtype)
- [var kPMInvalidValue: Int](/documentation/applicationservices/kpminvalidvalue)
- [var kPMItemIsLocked: Int](/documentation/applicationservices/kpmitemislocked)
- [var kPMJobBusy: Int](/documentation/applicationservices/kpmjobbusy)
- [var kPMJobCanceled: Int](/documentation/applicationservices/kpmjobcanceled)
- [var kPMJobGetTicketBadFormatError: Int](/documentation/applicationservices/kpmjobgetticketbadformaterror)
- [var kPMJobGetTicketReadError: Int](/documentation/applicationservices/kpmjobgetticketreaderror)
- [var kPMJobManagerAborted: Int](/documentation/applicationservices/kpmjobmanageraborted)
- [var kPMJobNotFound: Int](/documentation/applicationservices/kpmjobnotfound)
- [var kPMJobStreamEndError: Int](/documentation/applicationservices/kpmjobstreamenderror)
- [var kPMJobStreamOpenFailed: Int](/documentation/applicationservices/kpmjobstreamopenfailed)
- [var kPMJobStreamReadFailed: Int](/documentation/applicationservices/kpmjobstreamreadfailed)
- [var kPMKeyNotFound: Int](/documentation/applicationservices/kpmkeynotfound)
- [var kPMKeyNotUnique: Int](/documentation/applicationservices/kpmkeynotunique)
- [var kPMKeyOrValueNotFound: Int](/documentation/applicationservices/kpmkeyorvaluenotfound)
- [var kPMLastErrorCodeToMakeMaintenanceOfThisListEasier: Int](/documentation/applicationservices/kpmlasterrorcodetomakemaintenanceofthislisteasier)
- [var kPMMessagingError: Int](/documentation/applicationservices/kpmmessagingerror)
- [var kPMNoDefaultItem: Int](/documentation/applicationservices/kpmnodefaultitem)
- [var kPMNoDefaultSettings: Int](/documentation/applicationservices/kpmnodefaultsettings)
- [var kPMNoPrinterJobID: Int](/documentation/applicationservices/kpmnoprinterjobid)
- [var kPMNoSelectedPrinters: Int](/documentation/applicationservices/kpmnoselectedprinters)
- [var kPMOpenFailed: Int](/documentation/applicationservices/kpmopenfailed)
- [var kPMPMSymbolNotFound: Int](/documentation/applicationservices/kpmpmsymbolnotfound)
- [var kPMPermissionError: Int](/documentation/applicationservices/kpmpermissionerror)
- [var kPMPluginNotFound: Int](/documentation/applicationservices/kpmpluginnotfound)
- [var kPMPluginRegisterationFailed: Int](/documentation/applicationservices/kpmpluginregisterationfailed)
- [var kPMPrBrowserNoUI: Int](/documentation/applicationservices/kpmprbrowsernoui)
- [var kPMQueueAlreadyExists: Int](/documentation/applicationservices/kpmqueuealreadyexists)
- [var kPMQueueJobFailed: Int](/documentation/applicationservices/kpmqueuejobfailed)
- [var kPMQueueNotFound: Int](/documentation/applicationservices/kpmqueuenotfound)
- [var kPMReadFailed: Int](/documentation/applicationservices/kpmreadfailed)
- [var kPMReadGotZeroData: Int](/documentation/applicationservices/kpmreadgotzerodata)
- [var kPMServerAlreadyRunning: Int](/documentation/applicationservices/kpmserveralreadyrunning)
- [var kPMServerAttributeRestricted: Int](/documentation/applicationservices/kpmserverattributerestricted)
- [var kPMServerCommunicationFailed: Int](/documentation/applicationservices/kpmservercommunicationfailed)
- [var kPMServerNotFound: Int](/documentation/applicationservices/kpmservernotfound)
- [var kPMServerSuspended: Int](/documentation/applicationservices/kpmserversuspended)
- [var kPMStatusFailed: Int](/documentation/applicationservices/kpmstatusfailed)
- [var kPMStringConversionFailure: Int](/documentation/applicationservices/kpmstringconversionfailure)
- [var kPMSubTicketNotFound: Int](/documentation/applicationservices/kpmsubticketnotfound)
- [var kPMSyncRequestFailed: Int](/documentation/applicationservices/kpmsyncrequestfailed)
- [var kPMTemplateIsLocked: Int](/documentation/applicationservices/kpmtemplateislocked)
- [var kPMTicketIsLocked: Int](/documentation/applicationservices/kpmticketislocked)
- [var kPMTicketTypeNotFound: Int](/documentation/applicationservices/kpmtickettypenotfound)
- [var kPMUnableToFindProcess: Int](/documentation/applicationservices/kpmunabletofindprocess)
- [var kPMUnexpectedImagingError: Int](/documentation/applicationservices/kpmunexpectedimagingerror)
- [var kPMUnknownDataType: Int](/documentation/applicationservices/kpmunknowndatatype)
- [var kPMUnknownMessage: Int](/documentation/applicationservices/kpmunknownmessage)
- [var kPMUnsupportedConnection: Int](/documentation/applicationservices/kpmunsupportedconnection)
- [var kPMUpdateTicketFailed: Int](/documentation/applicationservices/kpmupdateticketfailed)
- [var kPMUserOrGroupNotFound: Int](/documentation/applicationservices/kpmuserorgroupnotfound)
- [var kPMValidateTicketFailed: Int](/documentation/applicationservices/kpmvalidateticketfailed)
- [var kPMWriteFailed: Int](/documentation/applicationservices/kpmwritefailed)
- [var kPMXMLParseError: Int](/documentation/applicationservices/kpmxmlparseerror)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1393710-anonymous)

#### Constants

- [var kATSUDirectDataAdvanceDeltaFixedArray: Int](/documentation/applicationservices/katsudirectdataadvancedeltafixedarray)
- [var kATSUDirectDataBaselineDeltaFixedArray: Int](/documentation/applicationservices/katsudirectdatabaselinedeltafixedarray)
- [var kATSUDirectDataDeviceDeltaSInt16Array: Int](/documentation/applicationservices/katsudirectdatadevicedeltasint16array)
- [var kATSUDirectDataLayoutRecordATSLayoutRecordCurrent: Int](/documentation/applicationservices/katsudirectdatalayoutrecordatslayoutrecordcurrent)
- [var kATSUDirectDataLayoutRecordATSLayoutRecordVersion1: Int](/documentation/applicationservices/katsudirectdatalayoutrecordatslayoutrecordversion1)
- [var kATSUDirectDataStyleIndexUInt16Array: Int](/documentation/applicationservices/katsudirectdatastyleindexuint16array)
- [var kATSUDirectDataStyleSettingATSUStyleSettingRefArray: Int](/documentation/applicationservices/katsudirectdatastylesettingatsustylesettingrefarray)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578531-anonymous)

#### Constants

- [var icConfigInappropriateErr: Int](/documentation/applicationservices/icconfiginappropriateerr)
- [var icConfigNotFoundErr: Int](/documentation/applicationservices/icconfignotfounderr)
- [var icInternalErr: Int](/documentation/applicationservices/icinternalerr)
- [var icNoMoreWritersErr: Int](/documentation/applicationservices/icnomorewriterserr)
- [var icNoURLErr: Int](/documentation/applicationservices/icnourlerr)
- [var icNothingToOverrideErr: Int](/documentation/applicationservices/icnothingtooverrideerr)
- [var icPermErr: Int](/documentation/applicationservices/icpermerr)
- [var icPrefDataErr: Int](/documentation/applicationservices/icprefdataerr)
- [var icPrefNotFoundErr: Int](/documentation/applicationservices/icprefnotfounderr)
- [var icProfileNotFoundErr: Int](/documentation/applicationservices/icprofilenotfounderr)
- [var icTooManyProfilesErr: Int](/documentation/applicationservices/ictoomanyprofileserr)
- [var icTruncatedErr: Int](/documentation/applicationservices/ictruncatederr)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578527-anonymous)

#### Constants

- [var kICComponentInterfaceVersion: Int](/documentation/applicationservices/kiccomponentinterfaceversion)
- [var kICComponentInterfaceVersion0: Int](/documentation/applicationservices/kiccomponentinterfaceversion0)
- [var kICComponentInterfaceVersion1: Int](/documentation/applicationservices/kiccomponentinterfaceversion1)
- [var kICComponentInterfaceVersion2: Int](/documentation/applicationservices/kiccomponentinterfaceversion2)
- [var kICComponentInterfaceVersion3: Int](/documentation/applicationservices/kiccomponentinterfaceversion3)
- [var kICComponentInterfaceVersion4: Int](/documentation/applicationservices/kiccomponentinterfaceversion4)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578529-anonymous)

#### Constants

- [var kICAttrLockedMask: UInt32](/documentation/applicationservices/kicattrlockedmask)
- [var kICAttrNoChange: UInt32](/documentation/applicationservices/kicattrnochange)
- [var kICAttrVolatileMask: UInt32](/documentation/applicationservices/kicattrvolatilemask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578484-anonymous)

#### Constants

- [var kICMapFixedLength: Int](/documentation/applicationservices/kicmapfixedlength)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578521-anonymous)

#### Constants

- [var kAEFetchURL: Int](/documentation/applicationservices/kaefetchurl)
- [var kAEGetURL: Int](/documentation/applicationservices/kaegeturl)
- [var kInternetEventClass: Int](/documentation/applicationservices/kinterneteventclass)
- [var keyAEAttaching: Int](/documentation/applicationservices/keyaeattaching)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578499-anonymous)

#### Constants

- [var kICAttrLockedBit: Int](/documentation/applicationservices/kicattrlockedbit)
- [var kICAttrVolatileBit: Int](/documentation/applicationservices/kicattrvolatilebit)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578538-anonymous)

#### Constants

- [var kICCreator: Int](/documentation/applicationservices/kiccreator)
- [var kICFileType: Int](/documentation/applicationservices/kicfiletype)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578541-anonymous)

#### Constants

- [var kICNilProfileID: Int](/documentation/applicationservices/kicnilprofileid)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578543-anonymous)

#### Constants

- [var kICFileSpecHeaderSize: Int](/documentation/applicationservices/kicfilespecheadersize)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578497-anonymous)

#### Constants

- [var kICMapBinaryBit: Int](/documentation/applicationservices/kicmapbinarybit)
- [var kICMapDataForkBit: Int](/documentation/applicationservices/kicmapdataforkbit)
- [var kICMapNotIncomingBit: Int](/documentation/applicationservices/kicmapnotincomingbit)
- [var kICMapNotOutgoingBit: Int](/documentation/applicationservices/kicmapnotoutgoingbit)
- [var kICMapPostBit: Int](/documentation/applicationservices/kicmappostbit)
- [var kICMapResourceForkBit: Int](/documentation/applicationservices/kicmapresourceforkbit)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578524-anonymous)

#### Constants

- [var kICComponentVersion: Int](/documentation/applicationservices/kiccomponentversion)
- [var kICNumVersion: Int](/documentation/applicationservices/kicnumversion)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578496-anonymous)

#### Constants

- [var kICServicesTCPBit: Int](/documentation/applicationservices/kicservicestcpbit)
- [var kICServicesUDPBit: Int](/documentation/applicationservices/kicservicesudpbit)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578525-anonymous)

#### Constants

- [var kICServicesTCPMask: Int](/documentation/applicationservices/kicservicestcpmask)
- [var kICServicesUDPMask: Int](/documentation/applicationservices/kicservicesudpmask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578530-anonymous)

#### Constants

- [var kICNoUserInteractionMask: Int](/documentation/applicationservices/kicnouserinteractionmask)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578516-anonymous)

#### Constants

- [var kICNoUserInteractionBit: Int](/documentation/applicationservices/kicnouserinteractionbit)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578535-anonymous)

#### Constants

- [var kICEditPreferenceEvent: Int](/documentation/applicationservices/kiceditpreferenceevent)
- [var kICEditPreferenceEventClass: Int](/documentation/applicationservices/kiceditpreferenceeventclass)
- [var keyICEditPreferenceDestination: Int](/documentation/applicationservices/keyiceditpreferencedestination)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578537-anonymous)

#### Constants

- [var icNoPerm: Int](/documentation/applicationservices/icnoperm)
- [var icReadOnlyPerm: Int](/documentation/applicationservices/icreadonlyperm)
- [var icReadWritePerm: Int](/documentation/applicationservices/icreadwriteperm)
- [Anonymous](/documentation/applicationservices/applicationservices_enumerations/1578491-anonymous)

#### Constants

- [var kICMapBinaryMask: Int](/documentation/applicationservices/kicmapbinarymask)
- [var kICMapDataForkMask: Int](/documentation/applicationservices/kicmapdataforkmask)
- [var kICMapNotIncomingMask: Int](/documentation/applicationservices/kicmapnotincomingmask)
- [var kICMapNotOutgoingMask: Int](/documentation/applicationservices/kicmapnotoutgoingmask)
- [var kICMapPostMask: Int](/documentation/applicationservices/kicmappostmask)
- [var kICMapResourceForkMask: Int](/documentation/applicationservices/kicmapresourceforkmask)
- [PasteboardStandardLocation](/documentation/applicationservices/pasteboardstandardlocation)

#### Enumeration Cases

- [case trash](/documentation/applicationservices/pasteboardstandardlocation/trash)
- [case unknown](/documentation/applicationservices/pasteboardstandardlocation/unknown)
- [ApplicationServices Constants](/documentation/applicationservices/applicationservices_constants)

### Constants

- [var ATSFONTREF_DEFINED: Int32](/documentation/coretext/atsfontref_defined)
- [var CMBITMAPCALLBACKPROCPTR_DEFINED: Int32](/documentation/applicationservices/cmbitmapcallbackprocptr_defined)
- [var COLORSYNC_MD5_LENGTH: Int32](/documentation/colorsync/colorsync_md5_length)
- [var COLORSYNC_PROFILE_INSTALL_ENTITLEMENT: String](/documentation/colorsync/colorsync_profile_install_entitlement)
- [var QD_HEADERS_ARE_PRIVATE: Int32](/documentation/applicationservices/qd_headers_are_private)
- [var kATSFileReferenceFilterSelector: ATSFontFilterSelector](/documentation/applicationservices/katsfilereferencefilterselector)
- [var kATSFontFilterSelectorFontApplierFunction: ATSFontFilterSelector](/documentation/applicationservices/katsfontfilterselectorfontapplierfunction)
- [var kATSFontFilterSelectorFontFamily: ATSFontFilterSelector](/documentation/applicationservices/katsfontfilterselectorfontfamily)
- [var kATSFontFilterSelectorFontFamilyApplierFunction: ATSFontFilterSelector](/documentation/applicationservices/katsfontfilterselectorfontfamilyapplierfunction)
- [var kATSFontFilterSelectorGeneration: ATSFontFilterSelector](/documentation/applicationservices/katsfontfilterselectorgeneration)
- [var kATSFontFilterSelectorUnspecified: ATSFontFilterSelector](/documentation/applicationservices/katsfontfilterselectorunspecified)
- [var kATSFontNameTableBytes: String](/documentation/applicationservices/katsfontnametablebytes)
- [var kATSFontNameTableCode: String](/documentation/applicationservices/katsfontnametablecode)
- [var kATSFontNameTableLanguage: String](/documentation/applicationservices/katsfontnametablelanguage)
- [var kATSFontNameTablePlatform: String](/documentation/applicationservices/katsfontnametableplatform)
- [var kATSFontNameTableScript: String](/documentation/applicationservices/katsfontnametablescript)
- [var kATSFontNotifyActionDirectoriesChanged: ATSFontNotifyAction](/documentation/applicationservices/katsfontnotifyactiondirectorieschanged)
- [var kATSFontNotifyActionFontsChanged: ATSFontNotifyAction](/documentation/applicationservices/katsfontnotifyactionfontschanged)
- [var kATSFontNotifyOptionDefault: ATSFontNotifyOption](/documentation/applicationservices/katsfontnotifyoptiondefault)
- [var kATSFontNotifyOptionReceiveWhileSuspended: ATSFontNotifyOption](/documentation/applicationservices/katsfontnotifyoptionreceivewhilesuspended)
- [var kATSQueryActivateFontMessage: ATSFontQueryMessageID](/documentation/applicationservices/katsqueryactivatefontmessage)
- [var kATSQueryClientPID: String](/documentation/applicationservices/katsqueryclientpid)
- [var kATSQueryFontName: String](/documentation/applicationservices/katsqueryfontname)
- [var kATSQueryFontNameTableEntries: String](/documentation/applicationservices/katsqueryfontnametableentries)
- [var kATSQueryFontPostScriptName: String](/documentation/applicationservices/katsqueryfontpostscriptname)
- [var kATSQueryQDFamilyName: String](/documentation/applicationservices/katsqueryqdfamilyname)
- [var kATSUCenterAlignment: Fract](/documentation/applicationservices/katsucenteralignment)
- [var kATSUEndAlignment: Fract](/documentation/applicationservices/katsuendalignment)
- [var kATSUFullJustification: Fract](/documentation/applicationservices/katsufulljustification)
- [var kATSUNoJustification: Fract](/documentation/applicationservices/katsunojustification)
- [var kATSUStartAlignment: Fract](/documentation/applicationservices/katsustartalignment)
- [var kAXAlternateUIVisibleAttribute: String](/documentation/applicationservices/kaxalternateuivisibleattribute)
- [var kAXCellForColumnAndRowParameterizedAttribute: String](/documentation/applicationservices/kaxcellforcolumnandrowparameterizedattribute)
- [var kAXCellRole: String](/documentation/applicationservices/kaxcellrole)
- [var kAXClearButtonAttribute: String](/documentation/applicationservices/kaxclearbuttonattribute)
- [var kAXColumnCountAttribute: String](/documentation/applicationservices/kaxcolumncountattribute)
- [var kAXColumnIndexRangeAttribute: String](/documentation/applicationservices/kaxcolumnindexrangeattribute)
- [var kAXColumnTitlesAttribute: String](/documentation/applicationservices/kaxcolumntitlesattribute)
- [var kAXContentListSubrole: String](/documentation/applicationservices/kaxcontentlistsubrole)
- [var kAXCriticalValueAttribute: String](/documentation/applicationservices/kaxcriticalvalueattribute)
- [var kAXDefinitionListSubrole: String](/documentation/applicationservices/kaxdefinitionlistsubrole)
- [var kAXDescription: String](/documentation/applicationservices/kaxdescription)
- [var kAXDescriptionListSubrole: String](/documentation/applicationservices/kaxdescriptionlistsubrole)
- [var kAXDisclosureLevelAttribute: String](/documentation/applicationservices/kaxdisclosurelevelattribute)
- [var kAXElementBusyAttribute: String](/documentation/applicationservices/kaxelementbusyattribute)
- [var kAXElementBusyChangedNotification: String](/documentation/applicationservices/kaxelementbusychangednotification)
- [var kAXExtrasMenuBarAttribute: String](/documentation/applicationservices/kaxextrasmenubarattribute)
- [var kAXFocusedUIElementAttribute: String](/documentation/applicationservices/kaxfocuseduielementattribute)
- [var kAXForegoundColorTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxforegoundcolortextattribute)
- [var kAXFullScreenButtonAttribute: String](/documentation/applicationservices/kaxfullscreenbuttonattribute)
- [var kAXFullScreenButtonSubrole: String](/documentation/applicationservices/kaxfullscreenbuttonsubrole)
- [var kAXGridRole: String](/documentation/applicationservices/kaxgridrole)
- [var kAXHandleRole: String](/documentation/applicationservices/kaxhandlerole)
- [var kAXHandlesAttribute: String](/documentation/applicationservices/kaxhandlesattribute)
- [var kAXHorizontalUnitDescriptionAttribute: String](/documentation/applicationservices/kaxhorizontalunitdescriptionattribute)
- [var kAXHorizontalUnitsAttribute: String](/documentation/applicationservices/kaxhorizontalunitsattribute)
- [var kAXIdentifierAttribute: String](/documentation/applicationservices/kaxidentifierattribute)
- [var kAXIsEditableAttribute: String](/documentation/applicationservices/kaxiseditableattribute)
- [var kAXLayoutAreaRole: String](/documentation/applicationservices/kaxlayoutarearole)
- [var kAXLayoutItemRole: String](/documentation/applicationservices/kaxlayoutitemrole)
- [var kAXLayoutPointForScreenPointParameterizedAttribute: String](/documentation/applicationservices/kaxlayoutpointforscreenpointparameterizedattribute)
- [var kAXLayoutSizeForScreenSizeParameterizedAttribute: String](/documentation/applicationservices/kaxlayoutsizeforscreensizeparameterizedattribute)
- [var kAXLevelIndicatorRole: String](/documentation/applicationservices/kaxlevelindicatorrole)
- [var kAXListItemIndexTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxlistitemindextextattribute)
- [var kAXListItemLevelTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxlistitemleveltextattribute)
- [var kAXListItemPrefixTextAttribute: Unmanaged<CFString>](/documentation/applicationservices/kaxlistitemprefixtextattribute)
- [var kAXMarkerTypeAttribute: String](/documentation/applicationservices/kaxmarkertypeattribute)
- [var kAXMarkerTypeDescriptionAttribute: String](/documentation/applicationservices/kaxmarkertypedescriptionattribute)
- [var kAXMarkerUIElementsAttribute: String](/documentation/applicationservices/kaxmarkeruielementsattribute)
- [var kAXOrderedByRowAttribute: String](/documentation/applicationservices/kaxorderedbyrowattribute)
- [var kAXPlaceholderValueAttribute: String](/documentation/applicationservices/kaxplaceholdervalueattribute)
- [var kAXPopoverRole: String](/documentation/applicationservices/kaxpopoverrole)
- [var kAXRatingIndicatorSubrole: String](/documentation/applicationservices/kaxratingindicatorsubrole)
- [var kAXRowCountAttribute: String](/documentation/applicationservices/kaxrowcountattribute)
- [var kAXRowHeaderUIElementsAttribute: String](/documentation/applicationservices/kaxrowheaderuielementsattribute)
- [var kAXRowIndexRangeAttribute: String](/documentation/applicationservices/kaxrowindexrangeattribute)
- [var kAXRulerMarkerRole: String](/documentation/applicationservices/kaxrulermarkerrole)
- [var kAXRulerRole: String](/documentation/applicationservices/kaxrulerrole)
- [var kAXScreenPointForLayoutPointParameterizedAttribute: String](/documentation/applicationservices/kaxscreenpointforlayoutpointparameterizedattribute)
- [var kAXScreenSizeForLayoutSizeParameterizedAttribute: String](/documentation/applicationservices/kaxscreensizeforlayoutsizeparameterizedattribute)
- [var kAXSearchButtonAttribute: String](/documentation/applicationservices/kaxsearchbuttonattribute)
- [var kAXSelectedCellsAttribute: String](/documentation/applicationservices/kaxselectedcellsattribute)
- [var kAXSeparatorDockItemSubrole: String](/documentation/applicationservices/kaxseparatordockitemsubrole)
- [var kAXSharedFocusElementsAttribute: String](/documentation/applicationservices/kaxsharedfocuselementsattribute)
- [var kAXSwitchSubrole: String](/documentation/applicationservices/kaxswitchsubrole)
- [var kAXTextAttribute: String](/documentation/applicationservices/kaxtextattribute)
- [var kAXTimelineSubrole: String](/documentation/applicationservices/kaxtimelinesubrole)
- [var kAXToggleSubrole: String](/documentation/applicationservices/kaxtogglesubrole)
- [var kAXTrustedCheckOptionPrompt: Unmanaged<CFString>](/documentation/applicationservices/kaxtrustedcheckoptionprompt)
- [var kAXUnitDescriptionAttribute: String](/documentation/applicationservices/kaxunitdescriptionattribute)
- [var kAXUnitsAttribute: String](/documentation/applicationservices/kaxunitsattribute)
- [let kAXValueAXErrorType: UInt32](/documentation/applicationservices/kaxvalueaxerrortype)
- [let kAXValueCFRangeType: UInt32](/documentation/applicationservices/kaxvaluecfrangetype)
- [let kAXValueCGPointType: UInt32](/documentation/applicationservices/kaxvaluecgpointtype)
- [let kAXValueCGRectType: UInt32](/documentation/applicationservices/kaxvaluecgrecttype)
- [let kAXValueCGSizeType: UInt32](/documentation/applicationservices/kaxvaluecgsizetype)
- [let kAXValueIllegalType: UInt32](/documentation/applicationservices/kaxvalueillegaltype)
- [var kAXVerticalUnitDescriptionAttribute: String](/documentation/applicationservices/kaxverticalunitdescriptionattribute)
- [var kAXVerticalUnitsAttribute: String](/documentation/applicationservices/kaxverticalunitsattribute)
- [var kAXVisibleCellsAttribute: String](/documentation/applicationservices/kaxvisiblecellsattribute)
- [var kAXVisibleTextAttribute: String](/documentation/applicationservices/kaxvisibletextattribute)
- [var kAXWarningValueAttribute: String](/documentation/applicationservices/kaxwarningvalueattribute)
- [var kCMDefaultDeviceNotification: String](/documentation/applicationservices/kcmdefaultdevicenotification)
- [var kCMDefaultDeviceProfileNotification: String](/documentation/applicationservices/kcmdefaultdeviceprofilenotification)
- [var kCMDeviceOfflineNotification: String](/documentation/applicationservices/kcmdeviceofflinenotification)
- [var kCMDeviceOnlineNotification: String](/documentation/applicationservices/kcmdeviceonlinenotification)
- [var kCMDeviceProfilesNotification: String](/documentation/applicationservices/kcmdeviceprofilesnotification)
- [var kCMDeviceRegisteredNotification: String](/documentation/applicationservices/kcmdeviceregisterednotification)
- [var kCMDeviceStateNotification: String](/documentation/applicationservices/kcmdevicestatenotification)
- [var kCMDeviceUnregisteredNotification: String](/documentation/applicationservices/kcmdeviceunregisterednotification)
- [var kCMDisplayDeviceProfilesNotification: String](/documentation/applicationservices/kcmdisplaydeviceprofilesnotification)
- [var kCMFloatBitmapFlagsAlpha: CMFloatBitmapFlags](/documentation/applicationservices/kcmfloatbitmapflagsalpha)
- [var kCMFloatBitmapFlagsAlphaPremul: CMFloatBitmapFlags](/documentation/applicationservices/kcmfloatbitmapflagsalphapremul)
- [var kCMFloatBitmapFlagsNone: CMFloatBitmapFlags](/documentation/applicationservices/kcmfloatbitmapflagsnone)
- [var kCMFloatBitmapFlagsRangeClipped: CMFloatBitmapFlags](/documentation/applicationservices/kcmfloatbitmapflagsrangeclipped)
- [var kCMMApplyTransformProcName: Unmanaged<CFString>!](/documentation/colorsync/kcmmapplytransformprocname)
- [var kCMMCreateTransformPropertyProcName: Unmanaged<CFString>!](/documentation/colorsync/kcmmcreatetransformpropertyprocname)
- [var kCMMInitializeLinkProfileProcName: Unmanaged<CFString>!](/documentation/colorsync/kcmminitializelinkprofileprocname)
- [var kCMMInitializeTransformProcName: Unmanaged<CFString>!](/documentation/colorsync/kcmminitializetransformprocname)
- [var kCMPrefsChangedNotification: String](/documentation/applicationservices/kcmprefschangednotification)
- [var kColorSync10BitInteger: ColorSyncDataDepth](/documentation/colorsync/kcolorsync10bitinteger)
- [var kColorSync16BitFloat: ColorSyncDataDepth](/documentation/colorsync/kcolorsync16bitfloat)
- [var kColorSync16BitInteger: ColorSyncDataDepth](/documentation/colorsync/kcolorsync16bitinteger)
- [var kColorSync1BitGamut: ColorSyncDataDepth](/documentation/colorsync/kcolorsync1bitgamut)
- [var kColorSync32BitFloat: ColorSyncDataDepth](/documentation/colorsync/kcolorsync32bitfloat)
- [var kColorSync32BitInteger: ColorSyncDataDepth](/documentation/colorsync/kcolorsync32bitinteger)
- [var kColorSync32BitNamedColorIndex: ColorSyncDataDepth](/documentation/colorsync/kcolorsync32bitnamedcolorindex)
- [var kColorSync8BitInteger: ColorSyncDataDepth](/documentation/colorsync/kcolorsync8bitinteger)
- [var kColorSyncACESCGLinearProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncacescglinearprofile)
- [var kColorSyncAdobeRGB1998Profile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncadobergb1998profile)
- [var kColorSyncAlphaFirst: ColorSyncAlphaInfo](/documentation/colorsync/kcolorsyncalphafirst)
- [var kColorSyncAlphaLast: ColorSyncAlphaInfo](/documentation/colorsync/kcolorsyncalphalast)
- [var kColorSyncAlphaNone: ColorSyncAlphaInfo](/documentation/colorsync/kcolorsyncalphanone)
- [var kColorSyncAlphaNoneSkipFirst: ColorSyncAlphaInfo](/documentation/colorsync/kcolorsyncalphanoneskipfirst)
- [var kColorSyncAlphaNoneSkipLast: ColorSyncAlphaInfo](/documentation/colorsync/kcolorsyncalphanoneskiplast)
- [var kColorSyncAlphaPremultipliedFirst: ColorSyncAlphaInfo](/documentation/colorsync/kcolorsyncalphapremultipliedfirst)
- [var kColorSyncAlphaPremultipliedLast: ColorSyncAlphaInfo](/documentation/colorsync/kcolorsyncalphapremultipliedlast)
- [var kColorSyncBestQuality: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncbestquality)
- [var kColorSyncBlackPointCompensation: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncblackpointcompensation)
- [var kColorSyncCameraDeviceClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynccameradeviceclass)
- [var kColorSyncConversion1DLut: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversion1dlut)
- [var kColorSyncConversion3DLut: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversion3dlut)
- [var kColorSyncConversionBPC: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionbpc)
- [var kColorSyncConversionChannelID: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionchannelid)
- [var kColorSyncConversionGridPoints: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversiongridpoints)
- [var kColorSyncConversionInpChan: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversioninpchan)
- [var kColorSyncConversionMatrix: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionmatrix)
- [var kColorSyncConversionNDLut: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionndlut)
- [var kColorSyncConversionOutChan: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionoutchan)
- [var kColorSyncConversionParamCurve0: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionparamcurve0)
- [var kColorSyncConversionParamCurve1: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionparamcurve1)
- [var kColorSyncConversionParamCurve2: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionparamcurve2)
- [var kColorSyncConversionParamCurve3: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionparamcurve3)
- [var kColorSyncConversionParamCurve4: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconversionparamcurve4)
- [var kColorSyncConvertQuality: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconvertquality)
- [var kColorSyncConvertUseExtendedRange: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncconvertuseextendedrange)
- [var kColorSyncCustomProfiles: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynccustomprofiles)
- [var kColorSyncDCIP3Profile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdcip3profile)
- [var kColorSyncDeviceClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceclass)
- [var kColorSyncDeviceDefaultProfileID: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdevicedefaultprofileid)
- [var kColorSyncDeviceDescription: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdevicedescription)
- [var kColorSyncDeviceDescriptions: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdevicedescriptions)
- [var kColorSyncDeviceHostScope: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdevicehostscope)
- [var kColorSyncDeviceID: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceid)
- [var kColorSyncDeviceModeDescription: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdevicemodedescription)
- [var kColorSyncDeviceModeDescriptions: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdevicemodedescriptions)
- [var kColorSyncDeviceProfileID: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceprofileid)
- [var kColorSyncDeviceProfileIsCurrent: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceprofileiscurrent)
- [var kColorSyncDeviceProfileIsDefault: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceprofileisdefault)
- [var kColorSyncDeviceProfileIsFactory: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceprofileisfactory)
- [var kColorSyncDeviceProfileURL: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceprofileurl)
- [var kColorSyncDeviceProfilesNotification: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceprofilesnotification)
- [var kColorSyncDeviceRegisteredNotification: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceregisterednotification)
- [var kColorSyncDeviceUnregisteredNotification: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceunregisterednotification)
- [var kColorSyncDeviceUserScope: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdeviceuserscope)
- [var kColorSyncDisplayDeviceClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdisplaydeviceclass)
- [var kColorSyncDisplayDeviceProfilesNotification: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdisplaydeviceprofilesnotification)
- [var kColorSyncDisplayP3Profile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdisplayp3profile)
- [var kColorSyncDraftQuality: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncdraftquality)
- [var kColorSyncFactoryProfiles: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncfactoryprofiles)
- [var kColorSyncFixedPointRange: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncfixedpointrange)
- [var kColorSyncGenericCMYKProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncgenericcmykprofile)
- [var kColorSyncGenericGrayGamma22Profile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncgenericgraygamma22profile)
- [var kColorSyncGenericGrayProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncgenericgrayprofile)
- [var kColorSyncGenericLabProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncgenericlabprofile)
- [var kColorSyncGenericRGBProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncgenericrgbprofile)
- [var kColorSyncGenericXYZProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncgenericxyzprofile)
- [var kColorSyncITUR2020Profile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncitur2020profile)
- [var kColorSyncITUR709Profile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncitur709profile)
- [var kColorSyncNormalQuality: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncnormalquality)
- [var kColorSyncPreferredCMM: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncpreferredcmm)
- [var kColorSyncPrinterDeviceClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprinterdeviceclass)
- [var kColorSyncProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofile)
- [var kColorSyncProfileClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofileclass)
- [var kColorSyncProfileColorSpace: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofilecolorspace)
- [var kColorSyncProfileComputerDomain: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofilecomputerdomain)
- [var kColorSyncProfileDescription: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofiledescription)
- [var kColorSyncProfileHeader: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofileheader)
- [var kColorSyncProfileHostScope: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofilehostscope)
- [var kColorSyncProfileMD5Digest: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofilemd5digest)
- [var kColorSyncProfilePCS: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofilepcs)
- [var kColorSyncProfileURL: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofileurl)
- [var kColorSyncProfileUserDomain: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofileuserdomain)
- [var kColorSyncProfileUserScope: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncprofileuserscope)
- [var kColorSyncROMMRGBProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncrommrgbprofile)
- [var kColorSyncRenderingIntent: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncrenderingintent)
- [var kColorSyncRenderingIntentAbsolute: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncrenderingintentabsolute)
- [var kColorSyncRenderingIntentPerceptual: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncrenderingintentperceptual)
- [var kColorSyncRenderingIntentRelative: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncrenderingintentrelative)
- [var kColorSyncRenderingIntentSaturation: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncrenderingintentsaturation)
- [var kColorSyncRenderingIntentUseProfileHeader: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncrenderingintentuseprofileheader)
- [var kColorSyncSRGBProfile: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsrgbprofile)
- [var kColorSyncScannerDeviceClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncscannerdeviceclass)
- [var kColorSyncSigAToB0Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigatob0tag)
- [var kColorSyncSigAToB1Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigatob1tag)
- [var kColorSyncSigAToB2Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigatob2tag)
- [var kColorSyncSigAbstractClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigabstractclass)
- [var kColorSyncSigBToA0Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigbtoa0tag)
- [var kColorSyncSigBToA1Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigbtoa1tag)
- [var kColorSyncSigBToA2Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigbtoa2tag)
- [var kColorSyncSigBlueColorantTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigbluecoloranttag)
- [var kColorSyncSigBlueTRCTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigbluetrctag)
- [var kColorSyncSigCmykData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigcmykdata)
- [var kColorSyncSigColorSpaceClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigcolorspaceclass)
- [var kColorSyncSigCopyrightTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigcopyrighttag)
- [var kColorSyncSigDeviceMfgDescTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigdevicemfgdesctag)
- [var kColorSyncSigDeviceModelDescTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigdevicemodeldesctag)
- [var kColorSyncSigDisplayClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigdisplayclass)
- [var kColorSyncSigGamutTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiggamuttag)
- [var kColorSyncSigGrayData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiggraydata)
- [var kColorSyncSigGrayTRCTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiggraytrctag)
- [var kColorSyncSigGreenColorantTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiggreencoloranttag)
- [var kColorSyncSigGreenTRCTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiggreentrctag)
- [var kColorSyncSigInputClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiginputclass)
- [var kColorSyncSigLabData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiglabdata)
- [var kColorSyncSigLinkClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsiglinkclass)
- [var kColorSyncSigMediaBlackPointTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigmediablackpointtag)
- [var kColorSyncSigMediaWhitePointTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigmediawhitepointtag)
- [var kColorSyncSigNamedColor2Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsignamedcolor2tag)
- [var kColorSyncSigNamedColorClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsignamedcolorclass)
- [var kColorSyncSigOutputClass: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigoutputclass)
- [var kColorSyncSigPreview0Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigpreview0tag)
- [var kColorSyncSigPreview1Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigpreview1tag)
- [var kColorSyncSigPreview2Tag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigpreview2tag)
- [var kColorSyncSigProfileDescriptionTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigprofiledescriptiontag)
- [var kColorSyncSigProfileSequenceDescTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigprofilesequencedesctag)
- [var kColorSyncSigRedColorantTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigredcoloranttag)
- [var kColorSyncSigRedTRCTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigredtrctag)
- [var kColorSyncSigRgbData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigrgbdata)
- [var kColorSyncSigTechnologyTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigtechnologytag)
- [var kColorSyncSigViewingCondDescTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigviewingconddesctag)
- [var kColorSyncSigViewingConditionsTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigviewingconditionstag)
- [var kColorSyncSigXYZData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsyncsigxyzdata)
- [var kColorSyncTransformCodeFragmentType: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformcodefragmenttype)
- [var kColorSyncTransformCreator: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformcreator)
- [var kColorSyncTransformDeviceToDevice: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformdevicetodevice)
- [var kColorSyncTransformDeviceToPCS: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformdevicetopcs)
- [var kColorSyncTransformDstSpace: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformdstspace)
- [var kColorSyncTransformFullConversionData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformfullconversiondata)
- [var kColorSyncTransformGamutCheck: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformgamutcheck)
- [var kColorSyncTransformPCSToDevice: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformpcstodevice)
- [var kColorSyncTransformPCSToPCS: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformpcstopcs)
- [var kColorSyncTransformParametricConversionData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformparametricconversiondata)
- [var kColorSyncTransformSimplifiedConversionData: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformsimplifiedconversiondata)
- [var kColorSyncTransformSrcSpace: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformsrcspace)
- [var kColorSyncTransformTag: Unmanaged<CFString>!](/documentation/colorsync/kcolorsynctransformtag)
- [var kICArchieAll: String](/documentation/applicationservices/kicarchieall)
- [var kICArchiePreferred: String](/documentation/applicationservices/kicarchiepreferred)
- [var kICCharacterSet: String](/documentation/applicationservices/kiccharacterset)
- [var kICDocumentFont: String](/documentation/applicationservices/kicdocumentfont)
- [var kICDownloadFolder: String](/documentation/applicationservices/kicdownloadfolder)
- [var kICEmail: String](/documentation/applicationservices/kicemail)
- [var kICFTPHost: String](/documentation/applicationservices/kicftphost)
- [var kICFTPProxyAccount: String](/documentation/applicationservices/kicftpproxyaccount)
- [var kICFTPProxyHost: String](/documentation/applicationservices/kicftpproxyhost)
- [var kICFTPProxyPassword: String](/documentation/applicationservices/kicftpproxypassword)
- [var kICFTPProxyUser: String](/documentation/applicationservices/kicftpproxyuser)
- [var kICFingerHost: String](/documentation/applicationservices/kicfingerhost)
- [var kICGopherHost: String](/documentation/applicationservices/kicgopherhost)
- [var kICGopherProxy: String](/documentation/applicationservices/kicgopherproxy)
- [var kICHTTPProxyHost: String](/documentation/applicationservices/kichttpproxyhost)
- [var kICIRCHost: String](/documentation/applicationservices/kicirchost)
- [var kICInfoMacAll: String](/documentation/applicationservices/kicinfomacall)
- [var kICInfoMacPreferred: String](/documentation/applicationservices/kicinfomacpreferred)
- [var kICLDAPSearchbase: String](/documentation/applicationservices/kicldapsearchbase)
- [var kICLDAPServer: String](/documentation/applicationservices/kicldapserver)
- [var kICListFont: String](/documentation/applicationservices/kiclistfont)
- [var kICMacSearchHost: String](/documentation/applicationservices/kicmacsearchhost)
- [var kICMailAccount: String](/documentation/applicationservices/kicmailaccount)
- [var kICMailHeaders: String](/documentation/applicationservices/kicmailheaders)
- [var kICMailPassword: String](/documentation/applicationservices/kicmailpassword)
- [var kICMapping: String](/documentation/applicationservices/kicmapping)
- [var kICNNTPHost: String](/documentation/applicationservices/kicnntphost)
- [var kICNTPHost: String](/documentation/applicationservices/kicntphost)
- [var kICNewMailDialog: String](/documentation/applicationservices/kicnewmaildialog)
- [var kICNewMailFlashIcon: String](/documentation/applicationservices/kicnewmailflashicon)
- [var kICNewMailPlaySound: String](/documentation/applicationservices/kicnewmailplaysound)
- [var kICNewMailSoundName: String](/documentation/applicationservices/kicnewmailsoundname)
- [var kICNewsAuthPassword: String](/documentation/applicationservices/kicnewsauthpassword)
- [var kICNewsAuthUsername: String](/documentation/applicationservices/kicnewsauthusername)
- [var kICNewsHeaders: String](/documentation/applicationservices/kicnewsheaders)
- [var kICNoProxyDomains: String](/documentation/applicationservices/kicnoproxydomains)
- [var kICOrganization: String](/documentation/applicationservices/kicorganization)
- [var kICPhHost: String](/documentation/applicationservices/kicphhost)
- [var kICPlan: String](/documentation/applicationservices/kicplan)
- [var kICPrinterFont: String](/documentation/applicationservices/kicprinterfont)
- [var kICQuotingString: String](/documentation/applicationservices/kicquotingstring)
- [var kICRTSPProxyHost: String](/documentation/applicationservices/kicrtspproxyhost)
- [var kICRealName: String](/documentation/applicationservices/kicrealname)
- [var kICReservedKey: String](/documentation/applicationservices/kicreservedkey)
- [var kICSMTPHost: String](/documentation/applicationservices/kicsmtphost)
- [var kICScreenFont: String](/documentation/applicationservices/kicscreenfont)
- [var kICServices: String](/documentation/applicationservices/kicservices)
- [var kICSignature: String](/documentation/applicationservices/kicsignature)
- [var kICSnailMailAddress: String](/documentation/applicationservices/kicsnailmailaddress)
- [var kICSocksHost: String](/documentation/applicationservices/kicsockshost)
- [var kICTelnetHost: String](/documentation/applicationservices/kictelnethost)
- [var kICUMichAll: String](/documentation/applicationservices/kicumichall)
- [var kICUMichPreferred: String](/documentation/applicationservices/kicumichpreferred)
- [var kICUseFTPProxy: String](/documentation/applicationservices/kicuseftpproxy)
- [var kICUseGopherProxy: String](/documentation/applicationservices/kicusegopherproxy)
- [var kICUseHTTPProxy: String](/documentation/applicationservices/kicusehttpproxy)
- [var kICUsePassiveFTP: String](/documentation/applicationservices/kicusepassiveftp)
- [var kICUseRTSPProxy: String](/documentation/applicationservices/kicusertspproxy)
- [var kICUseSocks: String](/documentation/applicationservices/kicusesocks)
- [var kICWAISGateway: String](/documentation/applicationservices/kicwaisgateway)
- [var kICWWWHomePage: String](/documentation/applicationservices/kicwwwhomepage)
- [var kICWebBackgroundColour: String](/documentation/applicationservices/kicwebbackgroundcolour)
- [var kICWebSearchPagePrefs: String](/documentation/applicationservices/kicwebsearchpageprefs)
- [var kICWebTextColor: String](/documentation/applicationservices/kicwebtextcolor)
- [var kICWhoisHost: String](/documentation/applicationservices/kicwhoishost)
- [var kPDFWorkflowItemURLKey: String](/documentation/applicationservices/kpdfworkflowitemurlkey)
- [var kPMApplicationColorMatchingStr: String](/documentation/applicationservices/kpmapplicationcolormatchingstr)
- [var kPMBorderStr: String](/documentation/applicationservices/kpmborderstr)
- [var kPMBorderTypeStr: String](/documentation/applicationservices/kpmbordertypestr)
- [var kPMCollateAEProp: String](/documentation/applicationservices/kpmcollateaeprop)
- [var kPMColorMatchingModeStr: String](/documentation/applicationservices/kpmcolormatchingmodestr)
- [var kPMColorSpaceModelCount: Int32](/documentation/applicationservices/kpmcolorspacemodelcount)
- [var kPMColorSyncProfileIDStr: String](/documentation/applicationservices/kpmcolorsyncprofileidstr)
- [var kPMCopiesAEProp: String](/documentation/applicationservices/kpmcopiesaeprop)
- [var kPMCopiesStr: String](/documentation/applicationservices/kpmcopiesstr)
- [var kPMCopyCollateStr: String](/documentation/applicationservices/kpmcopycollatestr)
- [var kPMCoverPageSourceStr: String](/documentation/applicationservices/kpmcoverpagesourcestr)
- [var kPMCoverPageStr: String](/documentation/applicationservices/kpmcoverpagestr)
- [var kPMCustomProfilePathStr: String](/documentation/applicationservices/kpmcustomprofilepathstr)
- [var kPMDataFormatXMLCompressed: PMDataFormat](/documentation/applicationservices/kpmdataformatxmlcompressed)
- [var kPMDataFormatXMLDefault: PMDataFormat](/documentation/applicationservices/kpmdataformatxmldefault)
- [var kPMDataFormatXMLMinimal: PMDataFormat](/documentation/applicationservices/kpmdataformatxmlminimal)
- [var kPMDestinationPrinterIDStr: String](/documentation/applicationservices/kpmdestinationprinteridstr)
- [var kPMDestinationTypeStr: String](/documentation/applicationservices/kpmdestinationtypestr)
- [var kPMDocumentFormatDefault: String](/documentation/applicationservices/kpmdocumentformatdefault)
- [var kPMDocumentFormatPDF: String](/documentation/applicationservices/kpmdocumentformatpdf)
- [var kPMDocumentFormatPostScript: String](/documentation/applicationservices/kpmdocumentformatpostscript)
- [var kPMDuplexingStr: String](/documentation/applicationservices/kpmduplexingstr)
- [var kPMErrorHandlingAEProp: String](/documentation/applicationservices/kpmerrorhandlingaeprop)
- [var kPMFaxCoverSheetMessageStr: String](/documentation/applicationservices/kpmfaxcoversheetmessagestr)
- [var kPMFaxCoverSheetStr: String](/documentation/applicationservices/kpmfaxcoversheetstr)
- [var kPMFaxDateLabelStr: String](/documentation/applicationservices/kpmfaxdatelabelstr)
- [var kPMFaxFromLabelStr: String](/documentation/applicationservices/kpmfaxfromlabelstr)
- [var kPMFaxNumberAEProp: String](/documentation/applicationservices/kpmfaxnumberaeprop)
- [var kPMFaxNumberStr: String](/documentation/applicationservices/kpmfaxnumberstr)
- [var kPMFaxPrefixStr: String](/documentation/applicationservices/kpmfaxprefixstr)
- [var kPMFaxSheetsLabelStr: String](/documentation/applicationservices/kpmfaxsheetslabelstr)
- [var kPMFaxSubjectLabelStr: String](/documentation/applicationservices/kpmfaxsubjectlabelstr)
- [var kPMFaxSubjectStr: String](/documentation/applicationservices/kpmfaxsubjectstr)
- [var kPMFaxToLabelStr: String](/documentation/applicationservices/kpmfaxtolabelstr)
- [var kPMFaxToStr: String](/documentation/applicationservices/kpmfaxtostr)
- [var kPMFaxToneDialingStr: String](/documentation/applicationservices/kpmfaxtonedialingstr)
- [var kPMFaxUseSoundStr: String](/documentation/applicationservices/kpmfaxusesoundstr)
- [var kPMFaxWaitForDialToneStr: String](/documentation/applicationservices/kpmfaxwaitfordialtonestr)
- [var kPMFeatureAEProp: String](/documentation/applicationservices/kpmfeatureaeprop)
- [var kPMFirstPageAEProp: String](/documentation/applicationservices/kpmfirstpageaeprop)
- [var kPMFitToPageStr: String](/documentation/applicationservices/kpmfittopagestr)
- [var kPMGraphicsContextCoreGraphics: String](/documentation/applicationservices/kpmgraphicscontextcoregraphics)
- [var kPMGraphicsContextDefault: String](/documentation/applicationservices/kpmgraphicscontextdefault)
- [var kPMInlineWorkflowStr: String](/documentation/applicationservices/kpminlineworkflowstr)
- [var kPMJobHoldUntilTimeStr: String](/documentation/applicationservices/kpmjobholduntiltimestr)
- [var kPMJobPriorityStr: String](/documentation/applicationservices/kpmjobprioritystr)
- [var kPMJobStateStr: String](/documentation/applicationservices/kpmjobstatestr)
- [var kPMLastPageAEProp: String](/documentation/applicationservices/kpmlastpageaeprop)
- [var kPMLayoutAcrossAEProp: String](/documentation/applicationservices/kpmlayoutacrossaeprop)
- [var kPMLayoutColumnsStr: String](/documentation/applicationservices/kpmlayoutcolumnsstr)
- [var kPMLayoutDirectionStr: String](/documentation/applicationservices/kpmlayoutdirectionstr)
- [var kPMLayoutDownAEProp: String](/documentation/applicationservices/kpmlayoutdownaeprop)
- [var kPMLayoutNUpStr: String](/documentation/applicationservices/kpmlayoutnupstr)
- [var kPMLayoutRowsStr: String](/documentation/applicationservices/kpmlayoutrowsstr)
- [var kPMLayoutTileOrientationStr: String](/documentation/applicationservices/kpmlayouttileorientationstr)
- [var kPMMirrorStr: String](/documentation/applicationservices/kpmmirrorstr)
- [var kPMOutputFilenameStr: String](/documentation/applicationservices/kpmoutputfilenamestr)
- [var kPMOutputOrderStr: String](/documentation/applicationservices/kpmoutputorderstr)
- [var kPMPDFWorkFlowAEProp: String](/documentation/applicationservices/kpmpdfworkflowaeprop)
- [var kPMPSErrorHandlerStr: String](/documentation/applicationservices/kpmpserrorhandlerstr)
- [var kPMPSTraySwitchStr: String](/documentation/applicationservices/kpmpstrayswitchstr)
- [var kPMPageSetStr: String](/documentation/applicationservices/kpmpagesetstr)
- [var kPMPageToPaperMappingAllowScalingUpStr: String](/documentation/applicationservices/kpmpagetopapermappingallowscalingupstr)
- [var kPMPageToPaperMappingNone: PMPageToPaperMappingType](/documentation/applicationservices/kpmpagetopapermappingnone)
- [var kPMPageToPaperMappingScaleToFit: PMPageToPaperMappingType](/documentation/applicationservices/kpmpagetopapermappingscaletofit)
- [var kPMPageToPaperMappingTypeStr: String](/documentation/applicationservices/kpmpagetopapermappingtypestr)
- [var kPMPageToPaperMediaNameStr: String](/documentation/applicationservices/kpmpagetopapermedianamestr)
- [var kPMPresetAEProp: String](/documentation/applicationservices/kpmpresetaeprop)
- [var kPMPresetGraphicsTypeAll: String](/documentation/applicationservices/kpmpresetgraphicstypeall)
- [var kPMPresetGraphicsTypeGeneral: String](/documentation/applicationservices/kpmpresetgraphicstypegeneral)
- [var kPMPresetGraphicsTypeKey: String](/documentation/applicationservices/kpmpresetgraphicstypekey)
- [var kPMPresetGraphicsTypeNone: String](/documentation/applicationservices/kpmpresetgraphicstypenone)
- [var kPMPresetGraphicsTypePhoto: String](/documentation/applicationservices/kpmpresetgraphicstypephoto)
- [var kPMPrimaryPaperFeedStr: String](/documentation/applicationservices/kpmprimarypaperfeedstr)
- [var kPMPrintSelectionOnlyStr: String](/documentation/applicationservices/kpmprintselectiononlystr)
- [var kPMPrintSelectionTitleKey: String](/documentation/applicationservices/kpmprintselectiontitlekey)
- [var kPMPrintTimeAEProp: String](/documentation/applicationservices/kpmprinttimeaeprop)
- [var kPMSaveAsPDFAEProp: String](/documentation/applicationservices/kpmsaveaspdfaeprop)
- [var kPMSaveAsPSAEProp: String](/documentation/applicationservices/kpmsaveaspsaeprop)
- [var kPMSecondaryPaperFeedStr: String](/documentation/applicationservices/kpmsecondarypaperfeedstr)
- [var kPMTargetPrinterAEProp: String](/documentation/applicationservices/kpmtargetprinteraeprop)
- [var kPMTotalBeginPagesStr: String](/documentation/applicationservices/kpmtotalbeginpagesstr)
- [var kPMTotalSidesImagedStr: String](/documentation/applicationservices/kpmtotalsidesimagedstr)
- [var kPMUseOptionalAccountIDStr: String](/documentation/applicationservices/kpmuseoptionalaccountidstr)
- [var kPMUseOptionalPINStr: String](/documentation/applicationservices/kpmuseoptionalpinstr)
- [var kPMVendorColorMatchingStr: String](/documentation/applicationservices/kpmvendorcolormatchingstr)
- [var kPasteboardClipboard: String](/documentation/applicationservices/kpasteboardclipboard)
- [var kPasteboardFind: String](/documentation/applicationservices/kpasteboardfind)
- [var kPasteboardTypeFilePromiseContent: String](/documentation/applicationservices/kpasteboardtypefilepromisecontent)
- [var kPasteboardTypeFileURLPromise: String](/documentation/applicationservices/kpasteboardtypefileurlpromise)
- [let kSpeechAudioGraphProperty: CFString](/documentation/applicationservices/kspeechaudiographproperty)
- [let kSpeechAudioOutputFormatProperty: CFString](/documentation/applicationservices/kspeechaudiooutputformatproperty)
- [let kSpeechAudioUnitProperty: CFString](/documentation/applicationservices/kspeechaudiounitproperty)
- [let kSpeechModeTune: CFString](/documentation/applicationservices/kspeechmodetune)
- [let kSpeechOutputChannelMapProperty: CFString](/documentation/applicationservices/kspeechoutputchannelmapproperty)
- [let kSpeechOutputToFileDescriptorProperty: CFString](/documentation/applicationservices/kspeechoutputtofiledescriptorproperty)
- [let kSpeechSynthExtensionProperty: CFString](/documentation/applicationservices/kspeechsynthextensionproperty)
- [var ATS_LEGACY_API: Int32](/documentation/applicationservices/ats_legacy_api)
- [var SUMMARY_DISPLAY_ORDER: String](/documentation/applicationservices/summary_display_order)
- [var kAXDecorativeSubrole: String](/documentation/applicationservices/kaxdecorativesubrole)
- [var kAXHeadingRole: String](/documentation/applicationservices/kaxheadingrole)
- [var kAXUIElementTitleKey: String](/documentation/applicationservices/kaxuielementtitlekey)
- [var kAppPageSetupDialogTypeIDStr: String](/documentation/applicationservices/kapppagesetupdialogtypeidstr)
- [var kAppPrintDialogTypeIDStr: String](/documentation/applicationservices/kappprintdialogtypeidstr)
- [var kAppPrintThumbnailTypeIDStr: String](/documentation/applicationservices/kappprintthumbnailtypeidstr)
- [var kDialogExtensionIntfIDStr: String](/documentation/applicationservices/kdialogextensionintfidstr)
- [var kGeneralPageSetupDialogTypeIDStr: String](/documentation/applicationservices/kgeneralpagesetupdialogtypeidstr)
- [var kGeneralPrintDialogTypeIDStr: String](/documentation/applicationservices/kgeneralprintdialogtypeidstr)
- [var kPDFWorkflowModifiedKey: String](/documentation/applicationservices/kpdfworkflowmodifiedkey)
- [var kPMColorMatchingPDEKindID: String](/documentation/applicationservices/kpmcolormatchingpdekindid)
- [var kPMColorPDEKindID: String](/documentation/applicationservices/kpmcolorpdekindid)
- [var kPMCopiesAndPagesPDEKindID: String](/documentation/applicationservices/kpmcopiesandpagespdekindid)
- [var kPMCoverPagePDEKindID: String](/documentation/applicationservices/kpmcoverpagepdekindid)
- [var kPMCustomPaperSizePDEKindID: String](/documentation/applicationservices/kpmcustompapersizepdekindid)
- [var kPMDuplexPDEKindID: String](/documentation/applicationservices/kpmduplexpdekindid)
- [var kPMErrorHandlingPDEKindID: String](/documentation/applicationservices/kpmerrorhandlingpdekindid)
- [var kPMFaxAddressesPDEKindID: String](/documentation/applicationservices/kpmfaxaddressespdekindid)
- [var kPMFaxCoverPagePDEKindID: String](/documentation/applicationservices/kpmfaxcoverpagepdekindid)
- [var kPMFaxModemPDEKindID: String](/documentation/applicationservices/kpmfaxmodempdekindid)
- [var kPMImagingOptionsPDEKindID: String](/documentation/applicationservices/kpmimagingoptionspdekindid)
- [var kPMInkPDEKindID: String](/documentation/applicationservices/kpminkpdekindid)
- [var kPMJobPINPDEKindID: String](/documentation/applicationservices/kpmjobpinpdekindid)
- [var kPMLayoutPDEKindID: String](/documentation/applicationservices/kpmlayoutpdekindid)
- [var kPMMediaQualityPDEKindID: String](/documentation/applicationservices/kpmmediaqualitypdekindid)
- [var kPMOutputOptionsPDEKindID: String](/documentation/applicationservices/kpmoutputoptionspdekindid)
- [var kPMPDFEffectsPDEKindID: String](/documentation/applicationservices/kpmpdfeffectspdekindid)
- [var kPMPageAttributesKindID: String](/documentation/applicationservices/kpmpageattributeskindid)
- [var kPMPaperFeedPDEKindID: String](/documentation/applicationservices/kpmpaperfeedpdekindid)
- [var kPMPaperHandlingPDEKindID: String](/documentation/applicationservices/kpmpaperhandlingpdekindid)
- [var kPMPaperSourcePDEKindID: String](/documentation/applicationservices/kpmpapersourcepdekindid)
- [var kPMPrinterFeaturesPDEKindID: String](/documentation/applicationservices/kpmprinterfeaturespdekindid)
- [var kPMPriorityPDEKindID: String](/documentation/applicationservices/kpmprioritypdekindid)
- [var kPMRotationScalingPDEKindID: String](/documentation/applicationservices/kpmrotationscalingpdekindid)
- [var kPMSandboxCompatiblePDEs: String](/documentation/applicationservices/kpmsandboxcompatiblepdes)
- [var kPMSchedulerPDEKindID: String](/documentation/applicationservices/kpmschedulerpdekindid)
- [var kPMSummaryPanelKindID: String](/documentation/applicationservices/kpmsummarypanelkindid)
- [var kPMUniPrinterPDEKindID: String](/documentation/applicationservices/kpmuniprinterpdekindid)
- [var kPMUnsupportedPDEKindID: String](/documentation/applicationservices/kpmunsupportedpdekindid)
- [var kPMWatermarkPDEKindID: String](/documentation/applicationservices/kpmwatermarkpdekindid)
- [var kPrinterModuleTypeIDStr: String](/documentation/applicationservices/kprintermoduletypeidstr)
- [ApplicationServices Functions](/documentation/applicationservices/applicationservices_functions)

### Functions

- [func CGDisplayCreateUUIDFromDisplayID(UInt32) -> Unmanaged<CFUUID>!](/documentation/colorsync/cgdisplaycreateuuidfromdisplayid(_:))
- [func CGDisplayGetDisplayIDFromUUID(CFUUID!) -> UInt32](/documentation/colorsync/cgdisplaygetdisplayidfromuuid(_:))
- [func ColorSyncCMMCopyCMMIdentifier(ColorSyncCMM!) -> Unmanaged<CFString>?](/documentation/colorsync/colorsynccmmcopycmmidentifier(_:))
- [func ColorSyncCMMCopyLocalizedName(ColorSyncCMM!) -> Unmanaged<CFString>?](/documentation/colorsync/colorsynccmmcopylocalizedname(_:))
- [func ColorSyncCMMCreate(CFBundle!) -> Unmanaged<ColorSyncCMM>?](/documentation/colorsync/colorsynccmmcreate(_:))
- [func ColorSyncCMMGetBundle(ColorSyncCMM!) -> Unmanaged<CFBundle>?](/documentation/colorsync/colorsynccmmgetbundle(_:))
- [func ColorSyncCMMGetTypeID() -> CFTypeID](/documentation/colorsync/colorsynccmmgettypeid())
- [func ColorSyncDeviceCopyDeviceInfo(CFString!, CFUUID!) -> Unmanaged<CFDictionary>?](/documentation/colorsync/colorsyncdevicecopydeviceinfo(_:_:))
- [func ColorSyncDeviceSetCustomProfiles(CFString!, CFUUID!, CFDictionary!) -> Bool](/documentation/colorsync/colorsyncdevicesetcustomprofiles(_:_:_:))
- [func ColorSyncIterateDeviceProfiles(ColorSyncDeviceProfileIterateCallback!, UnsafeMutableRawPointer?)](/documentation/colorsync/colorsynciteratedeviceprofiles(_:_:))
- [func ColorSyncIterateInstalledCMMs(ColorSyncCMMIterateCallback!, UnsafeMutableRawPointer?)](/documentation/colorsync/colorsynciterateinstalledcmms(_:_:))
- [func ColorSyncIterateInstalledProfiles(ColorSyncProfileIterateCallback?, UnsafeMutablePointer<UInt32>?, UnsafeMutableRawPointer?, UnsafeMutablePointer<Unmanaged<CFError>?>?)](/documentation/colorsync/colorsynciterateinstalledprofiles(_:_:_:_:))
- [func ColorSyncProfileContainsTag(ColorSyncProfile!, CFString!) -> Bool](/documentation/colorsync/colorsyncprofilecontainstag(_:_:))
- [func ColorSyncProfileCopyData(ColorSyncProfile!, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<CFData>!](/documentation/colorsync/colorsyncprofilecopydata(_:_:))
- [func ColorSyncProfileCopyDescriptionString(ColorSyncProfile!) -> Unmanaged<CFString>?](/documentation/colorsync/colorsyncprofilecopydescriptionstring(_:))
- [func ColorSyncProfileCopyHeader(ColorSyncProfile!) -> Unmanaged<CFData>!](/documentation/colorsync/colorsyncprofilecopyheader(_:))
- [func ColorSyncProfileCopyTag(ColorSyncProfile!, CFString!) -> Unmanaged<CFData>?](/documentation/colorsync/colorsyncprofilecopytag(_:_:))
- [func ColorSyncProfileCopyTagSignatures(ColorSyncProfile!) -> Unmanaged<CFArray>?](/documentation/colorsync/colorsyncprofilecopytagsignatures(_:))
- [func ColorSyncProfileCreate(CFData!, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<ColorSyncProfile>?](/documentation/colorsync/colorsyncprofilecreate(_:_:))
- [func ColorSyncProfileCreateDeviceProfile(CFString!, CFUUID!, CFTypeRef!) -> Unmanaged<ColorSyncProfile>?](/documentation/colorsync/colorsyncprofilecreatedeviceprofile(_:_:_:))
- [func ColorSyncProfileCreateDisplayTransferTablesFromVCGT(ColorSyncProfile!, UnsafeMutablePointer<Int>!) -> Unmanaged<CFData>?](/documentation/colorsync/colorsyncprofilecreatedisplaytransfertablesfromvcgt(_:_:))
- [func ColorSyncProfileCreateLink(CFArray!, CFDictionary?) -> Unmanaged<ColorSyncProfile>?](/documentation/colorsync/colorsyncprofilecreatelink(_:_:))
- [func ColorSyncProfileCreateMutable() -> Unmanaged<ColorSyncMutableProfile>?](/documentation/colorsync/colorsyncprofilecreatemutable())
- [func ColorSyncProfileCreateMutableCopy(ColorSyncProfile!) -> Unmanaged<ColorSyncMutableProfile>?](/documentation/colorsync/colorsyncprofilecreatemutablecopy(_:))
- [func ColorSyncProfileCreateWithDisplayID(UInt32) -> Unmanaged<ColorSyncProfile>?](/documentation/colorsync/colorsyncprofilecreatewithdisplayid(_:))
- [func ColorSyncProfileCreateWithName(CFString!) -> Unmanaged<ColorSyncProfile>?](/documentation/colorsync/colorsyncprofilecreatewithname(_:))
- [func ColorSyncProfileCreateWithURL(CFURL!, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<ColorSyncProfile>?](/documentation/colorsync/colorsyncprofilecreatewithurl(_:_:))
- [func ColorSyncProfileEstimateGamma(ColorSyncProfile!, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Float](/documentation/colorsync/colorsyncprofileestimategamma(_:_:))
- [func ColorSyncProfileEstimateGammaWithDisplayID(Int32, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Float](/documentation/colorsync/colorsyncprofileestimategammawithdisplayid(_:_:))
- [func ColorSyncProfileGetDisplayTransferFormulaFromVCGT(ColorSyncProfile!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!, UnsafeMutablePointer<Float>!) -> Bool](/documentation/colorsync/colorsyncprofilegetdisplaytransferformulafromvcgt(_:_:_:_:_:_:_:_:_:_:))
- [func ColorSyncProfileGetMD5(ColorSyncProfile!) -> ColorSyncMD5](/documentation/colorsync/colorsyncprofilegetmd5(_:))
- [func ColorSyncProfileGetTypeID() -> CFTypeID](/documentation/colorsync/colorsyncprofilegettypeid())
- [func ColorSyncProfileGetURL(ColorSyncProfile!, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<CFURL>!](/documentation/colorsync/colorsyncprofilegeturl(_:_:))
- [func ColorSyncProfileInstall(ColorSyncProfile!, CFString!, CFString!, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/colorsync/colorsyncprofileinstall(_:_:_:_:))
- [func ColorSyncProfileRemoveTag(ColorSyncMutableProfile!, CFString!)](/documentation/colorsync/colorsyncprofileremovetag(_:_:))
- [func ColorSyncProfileSetHeader(ColorSyncMutableProfile!, CFData!)](/documentation/colorsync/colorsyncprofilesetheader(_:_:))
- [func ColorSyncProfileSetTag(ColorSyncMutableProfile!, CFString!, CFData!)](/documentation/colorsync/colorsyncprofilesettag(_:_:_:))
- [func ColorSyncProfileUninstall(ColorSyncProfile!, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/colorsync/colorsyncprofileuninstall(_:_:))
- [func ColorSyncProfileVerify(ColorSyncProfile!, UnsafeMutablePointer<Unmanaged<CFError>?>?, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/colorsync/colorsyncprofileverify(_:_:_:))
- [func ColorSyncRegisterDevice(CFString!, CFUUID!, CFDictionary!) -> Bool](/documentation/colorsync/colorsyncregisterdevice(_:_:_:))
- [func ColorSyncTransformConvert(ColorSyncTransform!, Int, Int, UnsafeMutableRawPointer!, ColorSyncDataDepth, ColorSyncDataLayout, Int, UnsafeRawPointer!, ColorSyncDataDepth, ColorSyncDataLayout, Int, CFDictionary?) -> Bool](/documentation/colorsync/colorsynctransformconvert(_:_:_:_:_:_:_:_:_:_:_:_:))
- [func ColorSyncTransformCopyProperty(ColorSyncTransform!, CFTypeRef!, CFDictionary?) -> Unmanaged<CFTypeRef>?](/documentation/colorsync/colorsynctransformcopyproperty(_:_:_:))
- [func ColorSyncTransformCreate(CFArray?, CFDictionary?) -> Unmanaged<ColorSyncTransform>?](/documentation/colorsync/colorsynctransformcreate(_:_:))
- [func ColorSyncTransformGetTypeID() -> CFTypeID](/documentation/colorsync/colorsynctransformgettypeid())
- [func ColorSyncTransformSetProperty(ColorSyncTransform!, CFTypeRef!, CFTypeRef?)](/documentation/colorsync/colorsynctransformsetproperty(_:_:_:))
- [func ColorSyncUnregisterDevice(CFString!, CFUUID!) -> Bool](/documentation/colorsync/colorsyncunregisterdevice(_:_:))
- [func DisposeIconActionUPP(IconActionUPP!)](/documentation/applicationservices/1461028-disposeiconactionupp)
- [func DisposeIconGetterUPP(IconGetterUPP!)](/documentation/applicationservices/1461061-disposeicongetterupp)
- [func GetIconFamilyData(IconFamilyHandle!, OSType, Handle!) -> OSErr](/documentation/applicationservices/1462743-geticonfamilydata)
- [func GetIconRefVariant(IconRef!, OSType, UnsafeMutablePointer<IconTransformType>!) -> IconRef!](/documentation/applicationservices/1463088-geticonrefvariant)
- [func HIShapeContainsPoint(HIShape!, UnsafePointer<CGPoint>!) -> Bool](/documentation/applicationservices/1464704-hishapecontainspoint)
- [func HIShapeCreateCopy(HIShape!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1463131-hishapecreatecopy)
- [func HIShapeCreateDifference(HIShape!, HIShape!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1460901-hishapecreatedifference)
- [func HIShapeCreateEmpty() -> Unmanaged<HIShape>!](/documentation/applicationservices/1462651-hishapecreateempty)
- [func HIShapeCreateIntersection(HIShape!, HIShape!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1464400-hishapecreateintersection)
- [func HIShapeCreateMutable() -> Unmanaged<HIMutableShape>!](/documentation/applicationservices/1459565-hishapecreatemutable)
- [func HIShapeCreateMutableCopy(HIShape!) -> Unmanaged<HIMutableShape>!](/documentation/applicationservices/1463298-hishapecreatemutablecopy)
- [func HIShapeCreateMutableWithRect(UnsafePointer<CGRect>!) -> Unmanaged<HIMutableShape>!](/documentation/applicationservices/1459532-hishapecreatemutablewithrect)
- [func HIShapeCreateUnion(HIShape!, HIShape!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1460112-hishapecreateunion)
- [func HIShapeCreateWithQDRgn(RgnHandle!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1464296-hishapecreatewithqdrgn)
- [func HIShapeCreateWithRect(UnsafePointer<CGRect>!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1460650-hishapecreatewithrect)
- [func HIShapeCreateXor(HIShape!, HIShape!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1459148-hishapecreatexor)
- [func HIShapeDifference(HIShape!, HIShape!, HIMutableShape!) -> OSStatus](/documentation/applicationservices/1458876-hishapedifference)
- [func HIShapeEnumerate(HIShape!, OptionBits, HIShapeEnumerateProcPtr!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/applicationservices/1459161-hishapeenumerate)
- [func HIShapeGetAsQDRgn(HIShape!, RgnHandle!) -> OSStatus](/documentation/applicationservices/1464369-hishapegetasqdrgn)
- [func HIShapeGetBounds(HIShape!, UnsafeMutablePointer<CGRect>!) -> UnsafeMutablePointer<CGRect>!](/documentation/applicationservices/1460255-hishapegetbounds)
- [func HIShapeGetTypeID() -> CFTypeID](/documentation/applicationservices/1463371-hishapegettypeid)
- [func HIShapeInset(HIMutableShape!, CGFloat, CGFloat) -> OSStatus](/documentation/applicationservices/1463337-hishapeinset)
- [func HIShapeIntersect(HIShape!, HIShape!, HIMutableShape!) -> OSStatus](/documentation/applicationservices/1462645-hishapeintersect)
- [func HIShapeIntersectsRect(HIShape!, UnsafePointer<CGRect>!) -> Bool](/documentation/applicationservices/1459614-hishapeintersectsrect)
- [func HIShapeIsEmpty(HIShape!) -> Bool](/documentation/applicationservices/1461878-hishapeisempty)
- [func HIShapeIsRectangular(HIShape!) -> Bool](/documentation/applicationservices/1461292-hishapeisrectangular)
- [func HIShapeOffset(HIMutableShape!, CGFloat, CGFloat) -> OSStatus](/documentation/applicationservices/1461775-hishapeoffset)
- [func HIShapeReplacePathInCGContext(HIShape!, CGContext!) -> OSStatus](/documentation/applicationservices/1460747-hishapereplacepathincgcontext)
- [func HIShapeSetEmpty(HIMutableShape!) -> OSStatus](/documentation/applicationservices/1461259-hishapesetempty)
- [func HIShapeSetWithShape(HIMutableShape!, HIShape!) -> OSStatus](/documentation/applicationservices/1462473-hishapesetwithshape)
- [func HIShapeUnion(HIShape!, HIShape!, HIMutableShape!) -> OSStatus](/documentation/applicationservices/1459542-hishapeunion)
- [func HIShapeUnionWithRect(HIMutableShape!, UnsafePointer<CGRect>!) -> OSStatus](/documentation/applicationservices/1462757-hishapeunionwithrect)
- [func HIShapeXor(HIShape!, HIShape!, HIMutableShape!) -> OSStatus](/documentation/applicationservices/1461294-hishapexor)
- [func IconRefContainsCGPoint(UnsafePointer<CGPoint>!, UnsafePointer<CGRect>!, IconAlignmentType, IconServicesUsageFlags, IconRef!) -> Bool](/documentation/applicationservices/1461049-iconrefcontainscgpoint)
- [func IconRefIntersectsCGRect(UnsafePointer<CGRect>!, UnsafePointer<CGRect>!, IconAlignmentType, IconServicesUsageFlags, IconRef!) -> Bool](/documentation/applicationservices/1462553-iconrefintersectscgrect)
- [func IconRefToHIShape(UnsafePointer<CGRect>!, IconAlignmentType, IconServicesUsageFlags, IconRef!) -> Unmanaged<HIShape>!](/documentation/applicationservices/1464005-iconreftohishape)
- [func IconRefToIconFamily(IconRef!, IconSelectorValue, UnsafeMutablePointer<IconFamilyHandle?>!) -> OSErr](/documentation/applicationservices/1459977-iconreftoiconfamily)
- [func InvokeIconActionUPP(ResType, UnsafeMutablePointer<Handle?>!, UnsafeMutableRawPointer!, IconActionUPP!) -> OSErr](/documentation/applicationservices/1464116-invokeiconactionupp)
- [func InvokeIconGetterUPP(ResType, UnsafeMutableRawPointer!, IconGetterUPP!) -> Handle!](/documentation/applicationservices/1460976-invokeicongetterupp)
- [func IsIconRefMaskEmpty(IconRef!) -> Bool](/documentation/applicationservices/1464419-isiconrefmaskempty)
- [func NewIconActionUPP(IconActionProcPtr!) -> IconActionUPP!](/documentation/applicationservices/1462738-newiconactionupp)
- [func NewIconGetterUPP(IconGetterProcPtr!) -> IconGetterUPP!](/documentation/applicationservices/1458777-newicongetterupp)
- [func PMPrinterCopyState(PMPrinter, UnsafeMutablePointer<Unmanaged<CFDictionary>?>) -> OSStatus](/documentation/applicationservices/1460381-pmprintercopystate)
- [func PMPrinterSendCommand(PMPrinter, CFString, CFString?, CFDictionary?) -> OSStatus](/documentation/applicationservices/1463872-pmprintersendcommand)
- [func PasteboardClear(Pasteboard) -> OSStatus](/documentation/applicationservices/1460800-pasteboardclear)
- [func PasteboardCopyItemFlavorData(Pasteboard, PasteboardItemID, CFString, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/applicationservices/1458917-pasteboardcopyitemflavordata)
- [func PasteboardCopyItemFlavors(Pasteboard, PasteboardItemID, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/applicationservices/1460005-pasteboardcopyitemflavors)
- [func PasteboardCopyName(Pasteboard, UnsafeMutablePointer<CFString?>) -> OSStatus](/documentation/applicationservices/1459455-pasteboardcopyname)
- [func PasteboardCopyPasteLocation(Pasteboard, UnsafeMutablePointer<CFURL?>) -> OSStatus](/documentation/applicationservices/1462546-pasteboardcopypastelocation)
- [func PasteboardCreate(CFString?, UnsafeMutablePointer<Pasteboard?>) -> OSStatus](/documentation/applicationservices/1461248-pasteboardcreate)
- [func PasteboardGetItemCount(Pasteboard, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/applicationservices/1459551-pasteboardgetitemcount)
- [func PasteboardGetItemFlavorFlags(Pasteboard, PasteboardItemID, CFString, UnsafeMutablePointer<PasteboardFlavorFlags>) -> OSStatus](/documentation/applicationservices/1459353-pasteboardgetitemflavorflags)
- [func PasteboardGetItemIdentifier(Pasteboard, CFIndex, UnsafeMutablePointer<PasteboardItemID?>) -> OSStatus](/documentation/applicationservices/1463412-pasteboardgetitemidentifier)
- [func PasteboardGetTypeID() -> CFTypeID](/documentation/applicationservices/1463386-pasteboardgettypeid)
- [func PasteboardPutItemFlavor(Pasteboard, PasteboardItemID, CFString, CFData?, PasteboardFlavorFlags) -> OSStatus](/documentation/applicationservices/1463184-pasteboardputitemflavor)
- [func PasteboardResolvePromises(Pasteboard) -> OSStatus](/documentation/applicationservices/1460816-pasteboardresolvepromises)
- [func PasteboardSetPasteLocation(Pasteboard, CFURL) -> OSStatus](/documentation/applicationservices/1460572-pasteboardsetpastelocation)
- [func PasteboardSetPromiseKeeper(Pasteboard, PasteboardPromiseKeeperProcPtr, UnsafeMutableRawPointer?) -> OSStatus](/documentation/applicationservices/1463604-pasteboardsetpromisekeeper)
- [func PasteboardSynchronize(Pasteboard) -> PasteboardSyncFlags](/documentation/applicationservices/1459590-pasteboardsynchronize)
- [func PlotIconRefInContext(CGContext!, UnsafePointer<CGRect>!, IconAlignmentType, IconTransformType, UnsafePointer<RGBColor>!, PlotIconRefFlags, IconRef!) -> OSStatus](/documentation/applicationservices/1463721-ploticonrefincontext)
- [func SetIconFamilyData(IconFamilyHandle!, OSType, Handle!) -> OSErr](/documentation/applicationservices/1462050-seticonfamilydata)
- [func TransformProcessType(UnsafePointer<ProcessSerialNumber>!, ProcessApplicationTransformState) -> OSStatus](/documentation/applicationservices/1462420-transformprocesstype)
- [func TranslationCopyDestinationType(Translation!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/applicationservices/1459620-translationcopydestinationtype)
- [func TranslationCopySourceType(Translation!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/applicationservices/1459344-translationcopysourcetype)
- [func TranslationCreate(CFString!, CFString!, TranslationFlags, UnsafeMutablePointer<Unmanaged<Translation>?>!) -> OSStatus](/documentation/applicationservices/1459231-translationcreate)
- [func TranslationCreateWithSourceArray(CFArray!, TranslationFlags, UnsafeMutablePointer<Unmanaged<CFArray>?>!, UnsafeMutablePointer<Unmanaged<CFDictionary>?>!) -> OSStatus](/documentation/applicationservices/1464306-translationcreatewithsourcearray)
- [func TranslationGetTranslationFlags(Translation!, UnsafeMutablePointer<TranslationFlags>!) -> OSStatus](/documentation/applicationservices/1459307-translationgettranslationflags)
- [func TranslationGetTypeID() -> CFTypeID](/documentation/applicationservices/1463809-translationgettypeid)
- [func TranslationPerformForData(Translation!, CFData!, UnsafeMutablePointer<Unmanaged<CFData>?>!) -> OSStatus](/documentation/applicationservices/1460828-translationperformfordata)
- [func TranslationPerformForFile(Translation!, UnsafePointer<FSRef>!, UnsafePointer<FSRef>!, CFString!, UnsafeMutablePointer<FSRef>!) -> OSStatus](/documentation/applicationservices/1464541-translationperformforfile)
- [func TranslationPerformForURL(Translation!, CFURL!, CFURL!, UnsafeMutablePointer<Unmanaged<CFURL>?>!) -> OSStatus](/documentation/applicationservices/1460118-translationperformforurl)
- [func ATSCreateFontQueryRunLoopSource(CFIndex, CFIndex, ATSFontQueryCallback!, UnsafePointer<ATSFontQuerySourceContext>!) -> Unmanaged<CFRunLoopSource>!](/documentation/applicationservices/1563673-atscreatefontqueryrunloopsource)
- [func ATSFontActivateFromFileReference(UnsafePointer<FSRef>!, ATSFontContext, ATSFontFormat, UnsafeMutableRawPointer!, ATSOptionFlags, UnsafeMutablePointer<ATSFontContainerRef>!) -> OSStatus](/documentation/applicationservices/1563693-atsfontactivatefromfilereference)
- [func ATSFontActivateFromMemory(LogicalAddress!, Int, ATSFontContext, ATSFontFormat, UnsafeMutableRawPointer!, ATSOptionFlags, UnsafeMutablePointer<ATSFontContainerRef>!) -> OSStatus](/documentation/applicationservices/1563678-atsfontactivatefrommemory)
- [func ATSFontApplyFunction(ATSFontApplierFunction!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/applicationservices/1563664-atsfontapplyfunction)
- [func ATSFontDeactivate(ATSFontContainerRef, UnsafeMutableRawPointer!, ATSOptionFlags) -> OSStatus](/documentation/applicationservices/1563682-atsfontdeactivate)
- [func ATSFontFamilyApplyFunction(ATSFontFamilyApplierFunction!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/applicationservices/1563672-atsfontfamilyapplyfunction)
- [func ATSFontFamilyFindFromName(CFString!, ATSOptionFlags) -> ATSFontFamilyRef](/documentation/applicationservices/1563662-atsfontfamilyfindfromname)
- [func ATSFontFamilyFindFromQuickDrawName(ConstStr255Param!) -> ATSFontFamilyRef](/documentation/applicationservices/1563687-atsfontfamilyfindfromquickdrawna)
- [func ATSFontFamilyGetEncoding(ATSFontFamilyRef) -> TextEncoding](/documentation/applicationservices/1563658-atsfontfamilygetencoding)
- [func ATSFontFamilyGetGeneration(ATSFontFamilyRef) -> ATSGeneration](/documentation/applicationservices/1563689-atsfontfamilygetgeneration)
- [func ATSFontFamilyGetName(ATSFontFamilyRef, ATSOptionFlags, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/applicationservices/1563697-atsfontfamilygetname)
- [func ATSFontFamilyGetQuickDrawName(ATSFontFamilyRef, UnsafeMutablePointer<UInt8>!) -> OSStatus](/documentation/applicationservices/1563692-atsfontfamilygetquickdrawname)
- [func ATSFontFamilyIteratorCreate(ATSFontContext, UnsafePointer<ATSFontFilter>!, UnsafeMutableRawPointer!, ATSOptionFlags, UnsafeMutablePointer<ATSFontFamilyIterator?>!) -> OSStatus](/documentation/applicationservices/1563688-atsfontfamilyiteratorcreate)
- [func ATSFontFamilyIteratorNext(ATSFontFamilyIterator!, UnsafeMutablePointer<ATSFontFamilyRef>!) -> OSStatus](/documentation/applicationservices/1563679-atsfontfamilyiteratornext)
- [func ATSFontFamilyIteratorRelease(UnsafeMutablePointer<ATSFontFamilyIterator?>!) -> OSStatus](/documentation/applicationservices/1563681-atsfontfamilyiteratorrelease)
- [func ATSFontFamilyIteratorReset(ATSFontContext, UnsafePointer<ATSFontFilter>!, UnsafeMutableRawPointer!, ATSOptionFlags, UnsafeMutablePointer<ATSFontFamilyIterator?>!) -> OSStatus](/documentation/applicationservices/1563671-atsfontfamilyiteratorreset)
- [func ATSFontFindFromContainer(ATSFontContainerRef, ATSOptionFlags, Int, UnsafeMutablePointer<ATSFontRef>!, UnsafeMutablePointer<Int>!) -> OSStatus](/documentation/applicationservices/1563690-atsfontfindfromcontainer)
- [func ATSFontFindFromName(CFString!, ATSOptionFlags) -> ATSFontRef](/documentation/applicationservices/1563676-atsfontfindfromname)
- [func ATSFontFindFromPostScriptName(CFString!, ATSOptionFlags) -> ATSFontRef](/documentation/applicationservices/1563685-atsfontfindfrompostscriptname)
- [func ATSFontGetAutoActivationSettingForApplication(CFURL!) -> ATSFontAutoActivationSetting](/documentation/applicationservices/1563691-atsfontgetautoactivationsettingf)
- [func ATSFontGetContainer(ATSFontRef, ATSOptionFlags, UnsafeMutablePointer<ATSFontContainerRef>!) -> OSStatus](/documentation/applicationservices/1563651-atsfontgetcontainer)
- [func ATSFontGetContainerFromFileReference(UnsafePointer<FSRef>!, ATSFontContext, ATSOptionFlags, UnsafeMutablePointer<ATSFontContainerRef>!) -> OSStatus](/documentation/applicationservices/1563656-atsfontgetcontainerfromfilerefer)
- [func ATSFontGetFileReference(ATSFontRef, UnsafeMutablePointer<FSRef>!) -> OSStatus](/documentation/applicationservices/1563669-atsfontgetfilereference)
- [func ATSFontGetFontFamilyResource(ATSFontRef, Int, UnsafeMutableRawPointer!, UnsafeMutablePointer<Int>!) -> OSStatus](/documentation/applicationservices/1563684-atsfontgetfontfamilyresource)
- [func ATSFontGetGeneration(ATSFontRef) -> ATSGeneration](/documentation/applicationservices/1563670-atsfontgetgeneration)
- [func ATSFontGetGlobalAutoActivationSetting() -> ATSFontAutoActivationSetting](/documentation/applicationservices/1563702-atsfontgetglobalautoactivationse)
- [func ATSFontGetHorizontalMetrics(ATSFontRef, ATSOptionFlags, UnsafeMutablePointer<ATSFontMetrics>!) -> OSStatus](/documentation/applicationservices/1563665-atsfontgethorizontalmetrics)
- [func ATSFontGetName(ATSFontRef, ATSOptionFlags, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/applicationservices/1563657-atsfontgetname)
- [func ATSFontGetPostScriptName(ATSFontRef, ATSOptionFlags, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/applicationservices/1563666-atsfontgetpostscriptname)
- [func ATSFontGetTable(ATSFontRef, FourCharCode, ByteOffset, Int, UnsafeMutableRawPointer!, UnsafeMutablePointer<Int>!) -> OSStatus](/documentation/applicationservices/1563699-atsfontgettable)
- [func ATSFontGetTableDirectory(ATSFontRef, Int, UnsafeMutableRawPointer!, UnsafeMutablePointer<Int>!) -> OSStatus](/documentation/applicationservices/1563677-atsfontgettabledirectory)
- [func ATSFontGetVerticalMetrics(ATSFontRef, ATSOptionFlags, UnsafeMutablePointer<ATSFontMetrics>!) -> OSStatus](/documentation/applicationservices/1563653-atsfontgetverticalmetrics)
- [func ATSFontIsEnabled(ATSFontRef) -> Bool](/documentation/applicationservices/1563655-atsfontisenabled)
- [func ATSFontIteratorCreate(ATSFontContext, UnsafePointer<ATSFontFilter>!, UnsafeMutableRawPointer!, ATSOptionFlags, UnsafeMutablePointer<ATSFontIterator?>!) -> OSStatus](/documentation/applicationservices/1563668-atsfontiteratorcreate)
- [func ATSFontIteratorNext(ATSFontIterator!, UnsafeMutablePointer<ATSFontRef>!) -> OSStatus](/documentation/applicationservices/1563654-atsfontiteratornext)
- [func ATSFontIteratorRelease(UnsafeMutablePointer<ATSFontIterator?>!) -> OSStatus](/documentation/applicationservices/1563661-atsfontiteratorrelease)
- [func ATSFontIteratorReset(ATSFontContext, UnsafePointer<ATSFontFilter>!, UnsafeMutableRawPointer!, ATSOptionFlags, UnsafeMutablePointer<ATSFontIterator?>!) -> OSStatus](/documentation/applicationservices/1563680-atsfontiteratorreset)
- [func ATSFontNotificationSubscribe(ATSNotificationCallback!, ATSFontNotifyOption, UnsafeMutableRawPointer!, UnsafeMutablePointer<ATSFontNotificationRef?>!) -> OSStatus](/documentation/applicationservices/1563696-atsfontnotificationsubscribe)
- [func ATSFontNotificationUnsubscribe(ATSFontNotificationRef!) -> OSStatus](/documentation/applicationservices/1563675-atsfontnotificationunsubscribe)
- [func ATSFontNotify(ATSFontNotifyAction, UnsafeMutableRawPointer!) -> OSStatus](/documentation/applicationservices/1563701-atsfontnotify)
- [func ATSFontSetAutoActivationSettingForApplication(ATSFontAutoActivationSetting, CFURL!) -> OSStatus](/documentation/applicationservices/1563686-atsfontsetautoactivationsettingf)
- [func ATSFontSetEnabled(ATSFontRef, ATSOptionFlags, Bool) -> OSStatus](/documentation/applicationservices/1563667-atsfontsetenabled)
- [func ATSFontSetGlobalAutoActivationSetting(ATSFontAutoActivationSetting) -> OSStatus](/documentation/applicationservices/1563663-atsfontsetglobalautoactivationse)
- [func ATSGetGeneration() -> ATSGeneration](/documentation/applicationservices/1563694-atsgetgeneration)
- [func AXTextMarkerCreate(CFAllocator?, UnsafePointer<UInt8>, CFIndex) -> AXTextMarker](/documentation/applicationservices/3882823-axtextmarkercreate)
- [func AXTextMarkerGetBytePtr(AXTextMarker) -> UnsafePointer<UInt8>](/documentation/applicationservices/3882824-axtextmarkergetbyteptr)
- [func AXTextMarkerGetLength(AXTextMarker) -> CFIndex](/documentation/applicationservices/3882825-axtextmarkergetlength)
- [func AXTextMarkerGetTypeID() -> CFTypeID](/documentation/applicationservices/3882826-axtextmarkergettypeid)
- [func AXTextMarkerRangeCopyEndMarker(AXTextMarkerRange) -> AXTextMarker](/documentation/applicationservices/3882827-axtextmarkerrangecopyendmarker)
- [func AXTextMarkerRangeCopyStartMarker(AXTextMarkerRange) -> AXTextMarker](/documentation/applicationservices/3882828-axtextmarkerrangecopystartmarker)
- [func AXTextMarkerRangeCreate(CFAllocator?, AXTextMarker, AXTextMarker) -> AXTextMarkerRange](/documentation/applicationservices/3882829-axtextmarkerrangecreate)
- [func AXTextMarkerRangeCreateWithBytes(CFAllocator?, UnsafePointer<UInt8>, CFIndex, UnsafePointer<UInt8>, CFIndex) -> AXTextMarkerRange](/documentation/applicationservices/3882830-axtextmarkerrangecreatewithbytes)
- [func AXTextMarkerRangeGetTypeID() -> CFTypeID](/documentation/applicationservices/3882831-axtextmarkerrangegettypeid)
- [func DisposeSpeechDoneUPP(SpeechDoneUPP)](/documentation/applicationservices/4030001-disposespeechdoneupp)
- [func DisposeSpeechErrorUPP(SpeechErrorUPP)](/documentation/applicationservices/4030002-disposespeecherrorupp)
- [func DisposeSpeechPhonemeUPP(SpeechPhonemeUPP)](/documentation/applicationservices/4030003-disposespeechphonemeupp)
- [func DisposeSpeechSyncUPP(SpeechSyncUPP)](/documentation/applicationservices/4030004-disposespeechsyncupp)
- [func DisposeSpeechTextDoneUPP(SpeechTextDoneUPP)](/documentation/applicationservices/4030005-disposespeechtextdoneupp)
- [func DisposeSpeechWordUPP(SpeechWordUPP)](/documentation/applicationservices/4030006-disposespeechwordupp)
- [func GetSpeechInfo(SpeechChannel, OSType, UnsafeMutableRawPointer) -> OSErr](/documentation/applicationservices/4030007-getspeechinfo)
- [func InvokeSpeechDoneUPP(SpeechChannel, SRefCon, SpeechDoneUPP)](/documentation/applicationservices/4030008-invokespeechdoneupp)
- [func InvokeSpeechErrorUPP(SpeechChannel, SRefCon, OSErr, Int, SpeechErrorUPP)](/documentation/applicationservices/4030009-invokespeecherrorupp)
- [func InvokeSpeechPhonemeUPP(SpeechChannel, SRefCon, Int16, SpeechPhonemeUPP)](/documentation/applicationservices/4030010-invokespeechphonemeupp)
- [func InvokeSpeechSyncUPP(SpeechChannel, SRefCon, OSType, SpeechSyncUPP)](/documentation/applicationservices/4030011-invokespeechsyncupp)
- [func InvokeSpeechTextDoneUPP(SpeechChannel, SRefCon, UnsafeMutablePointer<UnsafeRawPointer?>?, UnsafeMutablePointer<UInt>, UnsafeMutablePointer<Int32>, SpeechTextDoneUPP)](/documentation/applicationservices/4030012-invokespeechtextdoneupp)
- [func InvokeSpeechWordUPP(SpeechChannel, SRefCon, UInt, UInt16, SpeechWordUPP)](/documentation/applicationservices/4030013-invokespeechwordupp)
- [func NewSpeechDoneUPP(SpeechDoneProcPtr) -> SpeechDoneUPP](/documentation/applicationservices/4030014-newspeechdoneupp)
- [func NewSpeechErrorUPP(SpeechErrorProcPtr) -> SpeechErrorUPP](/documentation/applicationservices/4030015-newspeecherrorupp)
- [func NewSpeechPhonemeUPP(SpeechPhonemeProcPtr) -> SpeechPhonemeUPP](/documentation/applicationservices/4030016-newspeechphonemeupp)
- [func NewSpeechSyncUPP(SpeechSyncProcPtr) -> SpeechSyncUPP](/documentation/applicationservices/4030017-newspeechsyncupp)
- [func NewSpeechTextDoneUPP(SpeechTextDoneProcPtr) -> SpeechTextDoneUPP](/documentation/applicationservices/4030018-newspeechtextdoneupp)
- [func NewSpeechWordUPP(SpeechWordProcPtr) -> SpeechWordUPP](/documentation/applicationservices/4030019-newspeechwordupp)
- [func SetSpeechInfo(SpeechChannel, OSType, UnsafeRawPointer?) -> OSErr](/documentation/applicationservices/4030020-setspeechinfo)
- [func SpeakBuffer(SpeechChannel, UnsafeRawPointer, UInt, Int32) -> OSErr](/documentation/applicationservices/4030021-speakbuffer)
- [func SpeakString(ConstStr255Param) -> OSErr](/documentation/applicationservices/4030022-speakstring)
- [func SpeakText(SpeechChannel, UnsafeRawPointer, UInt) -> OSErr](/documentation/applicationservices/4030023-speaktext)
- [func TextToPhonemes(SpeechChannel, UnsafeRawPointer, UInt, Handle, UnsafeMutablePointer<Int>) -> OSErr](/documentation/applicationservices/4030024-texttophonemes)
- [func UseDictionary(SpeechChannel, Handle) -> OSErr](/documentation/applicationservices/4030025-usedictionary)
- [ApplicationServices Data Types](/documentation/applicationservices/applicationservices_data_types)

### Data Types

- [ATSCubicClosePathProcPtr](/documentation/applicationservices/atscubicclosepathprocptr)
- [ATSCubicClosePathUPP](/documentation/applicationservices/atscubicclosepathupp)
- [ATSCubicCurveToProcPtr](/documentation/applicationservices/atscubiccurvetoprocptr)
- [ATSCubicCurveToUPP](/documentation/applicationservices/atscubiccurvetoupp)
- [ATSCubicLineToProcPtr](/documentation/applicationservices/atscubiclinetoprocptr)
- [ATSCubicLineToUPP](/documentation/applicationservices/atscubiclinetoupp)
- [ATSCubicMoveToProcPtr](/documentation/applicationservices/atscubicmovetoprocptr)
- [ATSCubicMoveToUPP](/documentation/applicationservices/atscubicmovetoupp)
- [ATSCurveType](/documentation/applicationservices/atscurvetype)
- [ATSFlatDataFontSpeciferType](/documentation/applicationservices/atsflatdatafontspecifertype)
- [ATSFontApplierFunction](/documentation/applicationservices/atsfontapplierfunction)
- [ATSFontAutoActivationSetting](/documentation/applicationservices/atsfontautoactivationsetting)
- [ATSFontContainerRef](/documentation/applicationservices/atsfontcontainerref)
- [ATSFontContext](/documentation/applicationservices/atsfontcontext)
- [ATSFontFamilyApplierFunction](/documentation/applicationservices/atsfontfamilyapplierfunction)
- [ATSFontFamilyIterator](/documentation/applicationservices/atsfontfamilyiterator)
- [ATSFontFamilyRef](/documentation/applicationservices/atsfontfamilyref)
- [ATSFontFormat](/documentation/applicationservices/atsfontformat)
- [ATSFontIterator](/documentation/applicationservices/atsfontiterator)
- [ATSFontNotificationInfoRef](/documentation/applicationservices/atsfontnotificationinforef)
- [ATSFontNotificationRef](/documentation/applicationservices/atsfontnotificationref)
- [ATSFontQueryCallback](/documentation/applicationservices/atsfontquerycallback)
- [ATSFontRef](/documentation/coretext/atsfontref)
- [ATSFontSize](/documentation/applicationservices/atsfontsize)
- [ATSGeneration](/documentation/applicationservices/atsgeneration)
- [ATSGlyphInfoFlags](/documentation/applicationservices/atsglyphinfoflags)
- [ATSGlyphRef](/documentation/applicationservices/atsglyphref)
- [ATSJustPriorityWidthDeltaOverrides](/documentation/applicationservices/atsjustprioritywidthdeltaoverrides)
- [ATSLineLayoutOptions](/documentation/applicationservices/atslinelayoutoptions)
- [ATSNotificationCallback](/documentation/applicationservices/atsnotificationcallback)
- [ATSOptionFlags](/documentation/applicationservices/atsoptionflags)
- [ATSPoint](/documentation/applicationservices/atspoint)
- [ATSQuadraticClosePathProcPtr](/documentation/applicationservices/atsquadraticclosepathprocptr)
- [ATSQuadraticClosePathUPP](/documentation/applicationservices/atsquadraticclosepathupp)
- [ATSQuadraticCurveProcPtr](/documentation/applicationservices/atsquadraticcurveprocptr)
- [ATSQuadraticCurveUPP](/documentation/applicationservices/atsquadraticcurveupp)
- [ATSQuadraticLineProcPtr](/documentation/applicationservices/atsquadraticlineprocptr)
- [ATSQuadraticLineUPP](/documentation/applicationservices/atsquadraticlineupp)
- [ATSQuadraticNewPathProcPtr](/documentation/applicationservices/atsquadraticnewpathprocptr)
- [ATSQuadraticNewPathUPP](/documentation/applicationservices/atsquadraticnewpathupp)
- [ATSStyleRenderingOptions](/documentation/applicationservices/atsstylerenderingoptions)
- [ATSUAttributeTag](/documentation/applicationservices/atsuattributetag)
- [ATSUAttributeValuePtr](/documentation/applicationservices/atsuattributevalueptr)
- [ATSUBackgroundColor](/documentation/applicationservices/atsubackgroundcolor)
- [ATSUBackgroundDataType](/documentation/applicationservices/atsubackgrounddatatype)
- [ATSUCursorMovementType](/documentation/applicationservices/atsucursormovementtype)
- [ATSUDirectDataSelector](/documentation/applicationservices/atsudirectdataselector)
- [ATSUDirectLayoutOperationOverrideProcPtr](/documentation/applicationservices/atsudirectlayoutoperationoverrideprocptr)
- [ATSUDirectLayoutOperationOverrideUPP](/documentation/applicationservices/atsudirectlayoutoperationoverrideupp)
- [ATSUFlattenStyleRunOptions](/documentation/applicationservices/atsuflattenstylerunoptions)
- [ATSUFlattenedDataStreamFormat](/documentation/applicationservices/atsuflatteneddatastreamformat)
- [ATSUFontFallbackMethod](/documentation/applicationservices/atsufontfallbackmethod)
- [ATSUFontFallbacks](/documentation/applicationservices/atsufontfallbacks)
- [ATSUFontFeatureSelector](/documentation/applicationservices/atsufontfeatureselector)
- [ATSUFontFeatureType](/documentation/applicationservices/atsufontfeaturetype)
- [ATSUFontID](/documentation/applicationservices/atsufontid)
- [ATSUFontVariationAxis](/documentation/applicationservices/atsufontvariationaxis)
- [ATSUFontVariationValue](/documentation/applicationservices/atsufontvariationvalue)
- [ATSUHighlightMethod](/documentation/applicationservices/atsuhighlightmethod)
- [ATSULayoutOperationCallbackStatus](/documentation/applicationservices/atsulayoutoperationcallbackstatus)
- [ATSULayoutOperationSelector](/documentation/applicationservices/atsulayoutoperationselector)
- [ATSULineRef](/documentation/applicationservices/atsulineref)
- [ATSULineTruncation](/documentation/applicationservices/atsulinetruncation)
- [ATSUStyle](/documentation/applicationservices/atsustyle)
- [ATSUStyleComparison](/documentation/applicationservices/atsustylecomparison)
- [ATSUStyleLineCountType](/documentation/applicationservices/atsustylelinecounttype)
- [ATSUStyleSettingRef](/documentation/applicationservices/atsustylesettingref)
- [ATSUTabType](/documentation/applicationservices/atsutabtype)
- [ATSUTextLayout](/documentation/applicationservices/atsutextlayout)
- [ATSUTextMeasurement](/documentation/applicationservices/atsutextmeasurement)
- [ATSUUnFlattenStyleRunOptions](/documentation/applicationservices/atsuunflattenstylerunoptions)
- [ATSUVerticalCharacterType](/documentation/applicationservices/atsuverticalcharactertype)
- [AppParametersPtr](/documentation/applicationservices/appparametersptr)
- [BitMapHandle](/documentation/applicationservices/bitmaphandle)
- [BitMapPtr](/documentation/applicationservices/bitmapptr)
- [CGrafPort](/documentation/applicationservices/cgrafport)
- [CM2ProfilePtr](/documentation/applicationservices/cm2profileptr)
- [CMMApplyTransformProc](/documentation/colorsync/cmmapplytransformproc)
- [CMMCreateTransformPropertyProc](/documentation/colorsync/cmmcreatetransformpropertyproc)
- [CMMInitializeLinkProfileProc](/documentation/colorsync/cmminitializelinkprofileproc)
- [CMMInitializeTransformProc](/documentation/colorsync/cmminitializetransformproc)
- [CQDProcsPtr](/documentation/applicationservices/cqdprocsptr)
- [CSpecArray](/documentation/applicationservices/cspecarray)
- [ColorComplementProcPtr](/documentation/applicationservices/colorcomplementprocptr)
- [ColorComplementUPP](/documentation/applicationservices/colorcomplementupp)
- [ColorSearchProcPtr](/documentation/applicationservices/colorsearchprocptr)
- [ColorSearchUPP](/documentation/applicationservices/colorsearchupp)
- [ColorSpecPtr](/documentation/applicationservices/colorspecptr)
- [ColorSyncCMMIterateCallback](/documentation/colorsync/colorsynccmmiteratecallback)
- [ColorSyncDataLayout](/documentation/colorsync/colorsyncdatalayout)
- [ColorSyncDeviceProfileIterateCallback](/documentation/colorsync/colorsyncdeviceprofileiteratecallback)
- [ColorSyncProfileIterateCallback](/documentation/colorsync/colorsyncprofileiteratecallback)
- [ConstATSUAttributeValuePtr](/documentation/applicationservices/constatsuattributevalueptr)
- [DragConstraint](/documentation/applicationservices/dragconstraint)
- [DragGrayRgnProcPtr](/documentation/applicationservices/draggrayrgnprocptr)
- [DragGrayRgnUPP](/documentation/applicationservices/draggrayrgnupp)
- [FMFilterSelector](/documentation/applicationservices/fmfilterselector)
- [FMFont](/documentation/applicationservices/fmfont)
- [FMFontCallbackFilterProcPtr](/documentation/applicationservices/fmfontcallbackfilterprocptr)
- [FMFontCallbackFilterUPP](/documentation/applicationservices/fmfontcallbackfilterupp)
- [FMFontFamily](/documentation/applicationservices/fmfontfamily)
- [FMFontFamilyCallbackFilterProcPtr](/documentation/applicationservices/fmfontfamilycallbackfilterprocptr)
- [FMFontFamilyCallbackFilterUPP](/documentation/applicationservices/fmfontfamilycallbackfilterupp)
- [FMFontSize](/documentation/applicationservices/fmfontsize)
- [FMFontStyle](/documentation/applicationservices/fmfontstyle)
- [FMGeneration](/documentation/applicationservices/fmgeneration)
- [FontRecHdl](/documentation/applicationservices/fontrechdl)
- [FontRecPtr](/documentation/applicationservices/fontrecptr)
- [GlyphCollection](/documentation/applicationservices/glyphcollection)
- [GlyphID](/documentation/applicationservices/glyphid)
- [GrafVerb](/documentation/applicationservices/grafverb)
- [HIShapeEnumerateProcPtr](/documentation/applicationservices/hishapeenumerateprocptr)
- [ICAppSpecHandle](/documentation/applicationservices/icappspechandle)
- [ICAppSpecListHandle](/documentation/applicationservices/icappspeclisthandle)
- [ICAppSpecListPtr](/documentation/applicationservices/icappspeclistptr)
- [ICAppSpecPtr](/documentation/applicationservices/icappspecptr)
- [ICAttr](/documentation/applicationservices/icattr)
- [ICCharTableHandle](/documentation/applicationservices/icchartablehandle)
- [ICCharTablePtr](/documentation/applicationservices/icchartableptr)
- [ICFileSpecHandle](/documentation/applicationservices/icfilespechandle)
- [ICFileSpecPtr](/documentation/applicationservices/icfilespecptr)
- [ICFixedLength](/documentation/applicationservices/icfixedlength)
- [ICFontRecordHandle](/documentation/applicationservices/icfontrecordhandle)
- [ICFontRecordPtr](/documentation/applicationservices/icfontrecordptr)
- [ICInstance](/documentation/applicationservices/icinstance)
- [ICMapEntryFlags](/documentation/applicationservices/icmapentryflags)
- [ICMapEntryHandle](/documentation/applicationservices/icmapentryhandle)
- [ICMapEntryPtr](/documentation/applicationservices/icmapentryptr)
- [ICPerm](/documentation/applicationservices/icperm)
- [ICProfileID](/documentation/applicationservices/icprofileid)
- [ICProfileIDPtr](/documentation/applicationservices/icprofileidptr)
- [ICServiceEntryFlags](/documentation/applicationservices/icserviceentryflags)
- [ICServiceEntryHandle](/documentation/applicationservices/icserviceentryhandle)
- [ICServiceEntryPtr](/documentation/applicationservices/icserviceentryptr)
- [ICServicesHandle](/documentation/applicationservices/icserviceshandle)
- [ICServicesPtr](/documentation/applicationservices/icservicesptr)
- [IconActionProcPtr](/documentation/applicationservices/iconactionprocptr)
- [IconActionUPP](/documentation/applicationservices/iconactionupp)
- [IconAlignmentType](/documentation/applicationservices/iconalignmenttype)
- [IconGetterProcPtr](/documentation/applicationservices/icongetterprocptr)
- [IconGetterUPP](/documentation/applicationservices/icongetterupp)
- [IconSelectorValue](/documentation/applicationservices/iconselectorvalue)
- [IconTransformType](/documentation/applicationservices/icontransformtype)
- [LaunchFlags](/documentation/applicationservices/launchflags)
- [LaunchPBPtr](/documentation/applicationservices/launchpbptr)
- [PMBorderType](/documentation/applicationservices/pmbordertype)
- [PMColorSpaceModel](/documentation/applicationservices/pmcolorspacemodel)
- [PMLayoutDirection](/documentation/applicationservices/pmlayoutdirection)
- [PMPaperType](/documentation/applicationservices/pmpapertype)
- [PMPrintDialogOptionFlags](/documentation/applicationservices/pmprintdialogoptionflags)
- [PMScalingAlignment](/documentation/applicationservices/pmscalingalignment)
- [PasteboardItemID](/documentation/applicationservices/pasteboarditemid)
- [PasteboardPromiseKeeperProcPtr](/documentation/applicationservices/pasteboardpromisekeeperprocptr)
- [PatHandle](/documentation/applicationservices/pathandle)
- [PatPtr](/documentation/applicationservices/patptr)
- [PixPatHandle](/documentation/applicationservices/pixpathandle)
- [PixPatPtr](/documentation/applicationservices/pixpatptr)
- [PlotIconRefFlags](/documentation/applicationservices/ploticonrefflags)
- [PolyHandle](/documentation/applicationservices/polyhandle)
- [PolyPtr](/documentation/applicationservices/polyptr)
- [Polygon](/documentation/applicationservices/polygon)
- [PrinterStatusOpcode](/documentation/applicationservices/printerstatusopcode)
- [ProcessApplicationTransformState](/documentation/applicationservices/processapplicationtransformstate)
- [ProcessInfoExtendedRecPtr](/documentation/applicationservices/processinfoextendedrecptr)
- [ProcessInfoRecPtr](/documentation/applicationservices/processinforecptr)
- [QDArcProcPtr](/documentation/applicationservices/qdarcprocptr)
- [QDArcUPP](/documentation/applicationservices/qdarcupp)
- [QDBitsProcPtr](/documentation/applicationservices/qdbitsprocptr)
- [QDBitsUPP](/documentation/applicationservices/qdbitsupp)
- [QDCommentProcPtr](/documentation/applicationservices/qdcommentprocptr)
- [QDCommentUPP](/documentation/applicationservices/qdcommentupp)
- [QDErr](/documentation/applicationservices/qderr)
- [QDGetPicProcPtr](/documentation/applicationservices/qdgetpicprocptr)
- [QDGetPicUPP](/documentation/applicationservices/qdgetpicupp)
- [QDJShieldCursorProcPtr](/documentation/applicationservices/qdjshieldcursorprocptr)
- [QDJShieldCursorUPP](/documentation/applicationservices/qdjshieldcursorupp)
- [QDLineProcPtr](/documentation/applicationservices/qdlineprocptr)
- [QDLineUPP](/documentation/applicationservices/qdlineupp)
- [QDOpcodeProcPtr](/documentation/applicationservices/qdopcodeprocptr)
- [QDOpcodeUPP](/documentation/applicationservices/qdopcodeupp)
- [QDOvalProcPtr](/documentation/applicationservices/qdovalprocptr)
- [QDOvalUPP](/documentation/applicationservices/qdovalupp)
- [QDPolyProcPtr](/documentation/applicationservices/qdpolyprocptr)
- [QDPolyUPP](/documentation/applicationservices/qdpolyupp)
- [QDPrinterStatusProcPtr](/documentation/applicationservices/qdprinterstatusprocptr)
- [QDPrinterStatusUPP](/documentation/applicationservices/qdprinterstatusupp)
- [QDPutPicProcPtr](/documentation/applicationservices/qdputpicprocptr)
- [QDPutPicUPP](/documentation/applicationservices/qdputpicupp)
- [QDRRectProcPtr](/documentation/applicationservices/qdrrectprocptr)
- [QDRRectUPP](/documentation/applicationservices/qdrrectupp)
- [QDRectProcPtr](/documentation/applicationservices/qdrectprocptr)
- [QDRectUPP](/documentation/applicationservices/qdrectupp)
- [QDRegionParseDirection](/documentation/applicationservices/qdregionparsedirection)
- [QDRgnProcPtr](/documentation/applicationservices/qdrgnprocptr)
- [QDRgnUPP](/documentation/applicationservices/qdrgnupp)
- [QDStdGlyphsProcPtr](/documentation/applicationservices/qdstdglyphsprocptr)
- [QDStdGlyphsUPP](/documentation/applicationservices/qdstdglyphsupp)
- [QDTextProcPtr](/documentation/applicationservices/qdtextprocptr)
- [QDTextUPP](/documentation/applicationservices/qdtextupp)
- [QDTxMeasProcPtr](/documentation/applicationservices/qdtxmeasprocptr)
- [QDTxMeasUPP](/documentation/applicationservices/qdtxmeasupp)
- [RedrawBackgroundProcPtr](/documentation/applicationservices/redrawbackgroundprocptr)
- [RedrawBackgroundUPP](/documentation/applicationservices/redrawbackgroundupp)
- [RegionToRectsProcPtr](/documentation/applicationservices/regiontorectsprocptr)
- [RegionToRectsUPP](/documentation/applicationservices/regiontorectsupp)
- [SizeResourceRecHandle](/documentation/applicationservices/sizeresourcerechandle)
- [SizeResourceRecPtr](/documentation/applicationservices/sizeresourcerecptr)
- [TranslationFlags](/documentation/applicationservices/translationflags)
- [TruncCode](/documentation/applicationservices/trunccode)
- [VDGamRecPtr](/documentation/applicationservices/vdgamrecptr)
- [VoiceSpecPtr](/documentation/applicationservices/voicespecptr)

## Classes

- [ColorSyncCMM](/documentation/colorsync/colorsynccmm)
- [ColorSyncMutableProfile](/documentation/colorsync/colorsyncmutableprofile)
- [ColorSyncProfile](/documentation/coregraphics/colorsyncprofile)
- [ColorSyncTransform](/documentation/colorsync/colorsynctransform)
- [HIMutableShape](/documentation/applicationservices/himutableshape)
- [HIShape](/documentation/applicationservices/hishape)
- [Pasteboard](/documentation/applicationservices/pasteboard)
- [Translation](/documentation/applicationservices/translation)
- [AXTextMarker](/documentation/applicationservices/axtextmarker)
- [AXTextMarkerRange](/documentation/applicationservices/axtextmarkerrange)

## Protocols

- [PDEPanel](/documentation/applicationservices/pdepanel)

### Instance Methods

- [func panelKind() -> String](/documentation/applicationservices/pdepanel/3930820-panelkind)
- [func panelName() -> String](/documentation/applicationservices/pdepanel/3930821-panelname)
- [func panelView() -> NSView?](/documentation/applicationservices/pdepanel/3930822-panelview)
- [func ppdOptionKeyValueDidChange(String, ppdChoice: String)](/documentation/applicationservices/pdepanel/3930823-ppdoptionkeyvaluedidchange)
- [func printWindowWillClose(Bool)](/documentation/applicationservices/pdepanel/3930824-printwindowwillclose)
- [func restoreValues()](/documentation/applicationservices/pdepanel/3930825-restorevalues)
- [func saveValues()](/documentation/applicationservices/pdepanel/3930826-savevalues)
- [func shouldHide() -> Bool](/documentation/applicationservices/pdepanel/3930827-shouldhide)
- [func shouldPrint() -> Bool](/documentation/applicationservices/pdepanel/3930828-shouldprint)
- [func shouldShowHelp() -> Bool](/documentation/applicationservices/pdepanel/3930829-shouldshowhelp)
- [func summaryInfo() -> [String : String]?](/documentation/applicationservices/pdepanel/3930830-summaryinfo)
- [func supportedPPDOptionKeys() -> [String]?](/documentation/applicationservices/pdepanel/3930831-supportedppdoptionkeys)
- [func willShow()](/documentation/applicationservices/pdepanel/3930832-willshow)
- [PDEPlugIn](/documentation/applicationservices/pdeplugin)

### Initializers

- [init?(bundle: Bundle)](/documentation/applicationservices/pdeplugin/3930834-init)

### Instance Methods

- [func pdePanels(forType: String, withHostInfo: any PDEPlugInCallbackProtocol) -> [any PDEPanel]?](/documentation/applicationservices/pdeplugin/3930835-pdepanels)
- [PDEPlugInCallbackProtocol](/documentation/applicationservices/pdeplugincallbackprotocol)

### Instance Methods

- [func pageFormat() -> PMPageFormat?](/documentation/applicationservices/pdeplugincallbackprotocol/3930837-pageformat)
- [func pmPrinter() -> PMPrinter](/documentation/applicationservices/pdeplugincallbackprotocol/3930838-pmprinter)
- [func ppdFile() -> UnsafeMutablePointer<ppd_file_s>?](/documentation/applicationservices/pdeplugincallbackprotocol/3930839-ppdfile)
- [func printSession() -> PMPrintSession?](/documentation/applicationservices/pdeplugincallbackprotocol/3930840-printsession)
- [func printSettings() -> PMPrintSettings?](/documentation/applicationservices/pdeplugincallbackprotocol/3930841-printsettings)
- [func willChangePPDOptionKeyValue(String, ppdChoice: String) -> Bool](/documentation/applicationservices/pdeplugincallbackprotocol/3930842-willchangeppdoptionkeyvalue)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
