# Core Services Documentation

Source: https://sosumi.ai/documentation/coreservices

---
title: Core Services
source: https://developer.apple.com/documentation/coreservices
timestamp: 2026-02-13T18:55:39.571Z
---

## Reference

- [Apple Events](/documentation/coreservices/apple_events)

### Structures

- [func AECallObjectAccessor(DescType, UnsafePointer<AEDesc>!, DescType, DescType, UnsafePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1447059-aecallobjectaccessor)
- [func AECheckIsRecord(UnsafePointer<AEDesc>!) -> Bool](/documentation/coreservices/1444011-aecheckisrecord)
- [func AECoerceDesc(UnsafePointer<AEDesc>!, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1446519-aecoercedesc)
- [func AECoercePtr(DescType, UnsafeRawPointer!, Size, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1441846-aecoerceptr)
- [func AECompareDesc(UnsafePointer<AEDesc>!, UnsafePointer<AEDesc>!, UnsafeMutablePointer<DarwinBoolean>!) -> OSStatus](/documentation/coreservices/1448782-aecomparedesc)
- [func AECountItems(UnsafePointer<AEDescList>!, UnsafeMutablePointer<Int>!) -> OSErr](/documentation/coreservices/1449533-aecountitems)
- [func AECreateAppleEvent(AEEventClass, AEEventID, UnsafePointer<AEAddressDesc>!, AEReturnID, AETransactionID, UnsafeMutablePointer<AppleEvent>!) -> OSErr](/documentation/coreservices/1448525-aecreateappleevent)
- [func AECreateDesc(DescType, UnsafeRawPointer!, Size, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1448535-aecreatedesc)
- [func AECreateDescFromExternalPtr(OSType, UnsafeRawPointer!, Size, AEDisposeExternalUPP!, SRefCon!, UnsafeMutablePointer<AEDesc>!) -> OSStatus](/documentation/coreservices/1446239-aecreatedescfromexternalptr)
- [func AECreateList(UnsafeRawPointer!, Size, Bool, UnsafeMutablePointer<AEDescList>!) -> OSErr](/documentation/coreservices/1448643-aecreatelist)
- [func AECreateRemoteProcessResolver(CFAllocator!, CFURL!) -> AERemoteProcessResolverRef!](/documentation/coreservices/1445692-aecreateremoteprocessresolver)
- [func AEDecodeMessage(UnsafeMutablePointer<mach_msg_header_t>!, UnsafeMutablePointer<AppleEvent>!, UnsafeMutablePointer<AppleEvent>!) -> OSStatus](/documentation/coreservices/1447827-aedecodemessage)
- [func AEDeleteItem(UnsafeMutablePointer<AEDescList>!, Int) -> OSErr](/documentation/coreservices/1447164-aedeleteitem)
- [func AEDeleteParam(UnsafeMutablePointer<AppleEvent>!, AEKeyword) -> OSErr](/documentation/coreservices/1444338-aedeleteparam)
- [func AEDisposeDesc(UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1444208-aedisposedesc)
- [func AEDisposeRemoteProcessResolver(AERemoteProcessResolverRef!)](/documentation/coreservices/1442572-aedisposeremoteprocessresolver)
- [func AEDisposeToken(UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1446783-aedisposetoken)
- [func AEDuplicateDesc(UnsafePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1442661-aeduplicatedesc)
- [func AEFlattenDesc(UnsafePointer<AEDesc>!, Ptr!, Size, UnsafeMutablePointer<Size>!) -> OSStatus](/documentation/coreservices/1441808-aeflattendesc)
- [func AEGetArray(UnsafePointer<AEDescList>!, AEArrayType, AEArrayDataPointer!, Size, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!, UnsafeMutablePointer<Int>!) -> OSErr](/documentation/coreservices/1445720-aegetarray)
- [func AEGetAttributeDesc(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1450314-aegetattributedesc)
- [func AEGetAttributePtr(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<DescType>!, UnsafeMutableRawPointer!, Size, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1445109-aegetattributeptr)
- [func AEGetCoercionHandler(DescType, DescType, UnsafeMutablePointer<AECoercionHandlerUPP?>!, UnsafeMutablePointer<SRefCon?>!, UnsafeMutablePointer<DarwinBoolean>!, Bool) -> OSErr](/documentation/coreservices/1445348-aegetcoercionhandler)
- [func AEGetDescData(UnsafePointer<AEDesc>!, UnsafeMutableRawPointer!, Size) -> OSErr](/documentation/coreservices/1444427-aegetdescdata)
- [func AEGetDescDataRange(UnsafePointer<AEDesc>!, UnsafeMutableRawPointer!, Size, Size) -> OSStatus](/documentation/coreservices/1446560-aegetdescdatarange)
- [func AEGetDescDataSize(UnsafePointer<AEDesc>!) -> Size](/documentation/coreservices/1450119-aegetdescdatasize)
- [func AEGetEventHandler(AEEventClass, AEEventID, UnsafeMutablePointer<AEEventHandlerUPP?>!, UnsafeMutablePointer<SRefCon?>!, Bool) -> OSErr](/documentation/coreservices/1445631-aegeteventhandler)
- [func AEGetNthDesc(UnsafePointer<AEDescList>!, Int, DescType, UnsafeMutablePointer<AEKeyword>!, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1448326-aegetnthdesc)
- [func AEGetNthPtr(UnsafePointer<AEDescList>!, Int, DescType, UnsafeMutablePointer<AEKeyword>!, UnsafeMutablePointer<DescType>!, UnsafeMutableRawPointer!, Size, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1447539-aegetnthptr)
- [func AEGetObjectAccessor(DescType, DescType, UnsafeMutablePointer<OSLAccessorUPP?>!, UnsafeMutablePointer<SRefCon?>!, Bool) -> OSErr](/documentation/coreservices/1449054-aegetobjectaccessor)
- [func AEGetParamDesc(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1449233-aegetparamdesc)
- [func AEGetParamPtr(UnsafePointer<AppleEvent>!, AEKeyword, DescType, UnsafeMutablePointer<DescType>!, UnsafeMutableRawPointer!, Size, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1444069-aegetparamptr)
- [func AEGetRegisteredMachPort() -> mach_port_t](/documentation/coreservices/1449736-aegetregisteredmachport)
- [func AEGetSpecialHandler(AEKeyword, UnsafeMutablePointer<AEEventHandlerUPP?>!, Bool) -> OSErr](/documentation/coreservices/1444274-aegetspecialhandler)
- [func AEInitializeDesc(UnsafeMutablePointer<AEDesc>!)](/documentation/coreservices/1446047-aeinitializedesc)
- [func AEInstallCoercionHandler(DescType, DescType, AECoercionHandlerUPP!, SRefCon!, Bool, Bool) -> OSErr](/documentation/coreservices/1445548-aeinstallcoercionhandler)
- [func AEInstallEventHandler(AEEventClass, AEEventID, AEEventHandlerUPP!, SRefCon!, Bool) -> OSErr](/documentation/coreservices/1448596-aeinstalleventhandler)
- [func AEInstallObjectAccessor(DescType, DescType, OSLAccessorUPP!, SRefCon!, Bool) -> OSErr](/documentation/coreservices/1447905-aeinstallobjectaccessor)
- [func AEInstallSpecialHandler(AEKeyword, AEEventHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1445532-aeinstallspecialhandler)
- [func AEManagerInfo(AEKeyword, UnsafeMutablePointer<Int>!) -> OSErr](/documentation/coreservices/1449373-aemanagerinfo)
- [func AEObjectInit() -> OSErr](/documentation/coreservices/1447372-aeobjectinit)
- [func AEPrintDescToHandle(UnsafePointer<AEDesc>!, UnsafeMutablePointer<Handle?>!) -> OSStatus](/documentation/coreservices/1445158-aeprintdesctohandle)
- [func AEProcessMessage(UnsafeMutablePointer<mach_msg_header_t>!) -> OSStatus](/documentation/coreservices/1444387-aeprocessmessage)
- [func AEPutArray(UnsafeMutablePointer<AEDescList>!, AEArrayType, UnsafePointer<AEArrayData>!, DescType, Size, Int) -> OSErr](/documentation/coreservices/1442535-aeputarray)
- [func AEPutAttributeDesc(UnsafeMutablePointer<AppleEvent>!, AEKeyword, UnsafePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1441790-aeputattributedesc)
- [func AEPutAttributePtr(UnsafeMutablePointer<AppleEvent>!, AEKeyword, DescType, UnsafeRawPointer!, Size) -> OSErr](/documentation/coreservices/1445940-aeputattributeptr)
- [func AEPutDesc(UnsafeMutablePointer<AEDescList>!, Int, UnsafePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1450093-aeputdesc)
- [func AEPutParamDesc(UnsafeMutablePointer<AppleEvent>!, AEKeyword, UnsafePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1447576-aeputparamdesc)
- [func AEPutParamPtr(UnsafeMutablePointer<AppleEvent>!, AEKeyword, DescType, UnsafeRawPointer!, Size) -> OSErr](/documentation/coreservices/1449263-aeputparamptr)
- [func AEPutPtr(UnsafeMutablePointer<AEDescList>!, Int, DescType, UnsafeRawPointer!, Size) -> OSErr](/documentation/coreservices/1445287-aeputptr)
- [func AERemoteProcessResolverGetProcesses(AERemoteProcessResolverRef!, UnsafeMutablePointer<CFStreamError>!) -> Unmanaged<CFArray>!](/documentation/coreservices/1444456-aeremoteprocessresolvergetproces)
- [func AERemoteProcessResolverScheduleWithRunLoop(AERemoteProcessResolverRef!, CFRunLoop!, CFString!, AERemoteProcessResolverCallback!, UnsafePointer<AERemoteProcessResolverContext>!)](/documentation/coreservices/1447259-aeremoteprocessresolverschedulew)
- [func AERemoveCoercionHandler(DescType, DescType, AECoercionHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1441907-aeremovecoercionhandler)
- [func AERemoveEventHandler(AEEventClass, AEEventID, AEEventHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1445239-aeremoveeventhandler)
- [func AERemoveObjectAccessor(DescType, DescType, OSLAccessorUPP!, Bool) -> OSErr](/documentation/coreservices/1442552-aeremoveobjectaccessor)
- [func AERemoveSpecialHandler(AEKeyword, AEEventHandlerUPP!, Bool) -> OSErr](/documentation/coreservices/1447960-aeremovespecialhandler)
- [func AEReplaceDescData(DescType, UnsafeRawPointer!, Size, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1446695-aereplacedescdata)
- [func AEResolve(UnsafePointer<AEDesc>!, Int16, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1449720-aeresolve)
- [func AESendMessage(UnsafePointer<AppleEvent>!, UnsafeMutablePointer<AppleEvent>!, AESendMode, Int) -> OSStatus](/documentation/coreservices/1442994-aesendmessage)
- [func AESetObjectCallbacks(OSLCompareUPP!, OSLCountUPP!, OSLDisposeTokenUPP!, OSLGetMarkTokenUPP!, OSLMarkUPP!, OSLAdjustMarksUPP!, OSLGetErrDescUPP!) -> OSErr](/documentation/coreservices/1447756-aesetobjectcallbacks)
- [func AESizeOfAttribute(UnsafePointer<AppleEvent>!, AEKeyword, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1445764-aesizeofattribute)
- [func AESizeOfFlattenedDesc(UnsafePointer<AEDesc>!) -> Size](/documentation/coreservices/1447305-aesizeofflatteneddesc)
- [func AESizeOfNthItem(UnsafePointer<AEDescList>!, Int, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1447307-aesizeofnthitem)
- [func AESizeOfParam(UnsafePointer<AppleEvent>!, AEKeyword, UnsafeMutablePointer<DescType>!, UnsafeMutablePointer<Size>!) -> OSErr](/documentation/coreservices/1449998-aesizeofparam)
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
- [func AEUnflattenDesc(UnsafeRawPointer!, UnsafeMutablePointer<AEDesc>!) -> OSStatus](/documentation/coreservices/1448997-aeunflattendesc)
- [AEArrayData](/documentation/coreservices/aearraydata)

#### Instance Properties

- [var kAEDataArray: Int16](/documentation/coreservices/aearraydata/1443096-kaedataarray)
- [var kAEDescArray: AEDesc](/documentation/coreservices/aearraydata/1442921-kaedescarray)
- [var kAEHandleArray: Handle?](/documentation/coreservices/aearraydata/1444461-kaehandlearray)
- [var kAEKeyDescArray: AEKeyDesc](/documentation/coreservices/aearraydata/1444282-kaekeydescarray)
- [var kAEPackedArray: CChar](/documentation/coreservices/aearraydata/1449947-kaepackedarray)

#### Initializers

- [init()](/documentation/coreservices/aearraydata/1447814-init)
- [init(kAEDataArray: Int16)](/documentation/coreservices/aearraydata/1442679-init)
- [init(kAEDescArray: AEDesc)](/documentation/coreservices/aearraydata/1450575-init)
- [init(kAEHandleArray: Handle?)](/documentation/coreservices/aearraydata/1448794-init)
- [init(kAEKeyDescArray: AEKeyDesc)](/documentation/coreservices/aearraydata/1442181-init)
- [init(kAEPackedArray: CChar)](/documentation/coreservices/aearraydata/1449681-init)
- [AEBuildError](/documentation/coreservices/aebuilderror)

#### Initializers

- [init()](/documentation/coreservices/aebuilderror/1447428-init)
- [init(fError: AEBuildErrorCode, fErrorPos: UInt32)](/documentation/coreservices/aebuilderror/1449472-init)

#### Instance Properties

- [var fError: AEBuildErrorCode](/documentation/coreservices/aebuilderror/1446581-ferror)
- [var fErrorPos: UInt32](/documentation/coreservices/aebuilderror/1448861-ferrorpos)
- [AEDesc](/documentation/coreservices/aedesc)

#### Initializers

- [init()](/documentation/coreservices/aedesc/1450256-init)
- [init(descriptorType: DescType, dataHandle: AEDataStorage!)](/documentation/coreservices/aedesc/1690318-init)

#### Instance Properties

- [var dataHandle: AEDataStorage!](/documentation/coreservices/aedesc/1444550-datahandle)
- [var descriptorType: DescType](/documentation/coreservices/aedesc/1445749-descriptortype)
- [AEKeyDesc](/documentation/coreservices/aekeydesc)

#### Initializers

- [init()](/documentation/coreservices/aekeydesc/1444200-init)
- [init(descKey: AEKeyword, descContent: AEDesc)](/documentation/coreservices/aekeydesc/1448884-init)

#### Instance Properties

- [var descContent: AEDesc](/documentation/coreservices/aekeydesc/1446095-desccontent)
- [var descKey: AEKeyword](/documentation/coreservices/aekeydesc/1443267-desckey)
- [AERemoteProcessResolverContext](/documentation/coreservices/aeremoteprocessresolvercontext)

#### Initializers

- [init()](/documentation/coreservices/aeremoteprocessresolvercontext/1449429-init)
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: CFAllocatorRetainCallBack!, release: CFAllocatorReleaseCallBack!, copyDescription: CFAllocatorCopyDescriptionCallBack!)](/documentation/coreservices/aeremoteprocessresolvercontext/1792092-init)

#### Instance Properties

- [var copyDescription: CFAllocatorCopyDescriptionCallBack!](/documentation/coreservices/aeremoteprocessresolvercontext/1442771-copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/coreservices/aeremoteprocessresolvercontext/1449518-info)
- [var release: CFAllocatorReleaseCallBack!](/documentation/coreservices/aeremoteprocessresolvercontext/1444738-release)
- [var retain: CFAllocatorRetainCallBack!](/documentation/coreservices/aeremoteprocessresolvercontext/1450097-retain)
- [var version: CFIndex](/documentation/coreservices/aeremoteprocessresolvercontext/1445231-version)

### Constants

- [let kAERemoteProcessNameKey: CFString!](/documentation/coreservices/kaeremoteprocessnamekey)
- [let kAERemoteProcessProcessIDKey: CFString!](/documentation/coreservices/kaeremoteprocessprocessidkey)
- [let kAERemoteProcessURLKey: CFString!](/documentation/coreservices/kaeremoteprocessurlkey)
- [let kAERemoteProcessUserIDKey: CFString!](/documentation/coreservices/kaeremoteprocessuseridkey)

### Data Types

- [OSLAccessorProcPtr](/documentation/coreservices/oslaccessorprocptr)
- [OSLAccessorUPP](/documentation/coreservices/oslaccessorupp)
- [OSLAdjustMarksProcPtr](/documentation/coreservices/osladjustmarksprocptr)
- [OSLAdjustMarksUPP](/documentation/coreservices/osladjustmarksupp)
- [OSLCompareProcPtr](/documentation/coreservices/oslcompareprocptr)
- [OSLCompareUPP](/documentation/coreservices/oslcompareupp)
- [OSLCountProcPtr](/documentation/coreservices/oslcountprocptr)
- [OSLCountUPP](/documentation/coreservices/oslcountupp)
- [OSLDisposeTokenProcPtr](/documentation/coreservices/osldisposetokenprocptr)
- [OSLDisposeTokenUPP](/documentation/coreservices/osldisposetokenupp)
- [OSLGetErrDescProcPtr](/documentation/coreservices/oslgeterrdescprocptr)
- [OSLGetErrDescUPP](/documentation/coreservices/oslgeterrdescupp)
- [OSLGetMarkTokenProcPtr](/documentation/coreservices/oslgetmarktokenprocptr)
- [OSLGetMarkTokenUPP](/documentation/coreservices/oslgetmarktokenupp)
- [OSLMarkProcPtr](/documentation/coreservices/oslmarkprocptr)
- [OSLMarkUPP](/documentation/coreservices/oslmarkupp)
- [AEAddressDesc](/documentation/coreservices/aeaddressdesc)
- [AEArrayDataPointer](/documentation/coreservices/aearraydatapointer)
- [AEArrayType](/documentation/coreservices/aearraytype)
- [AEBuildErrorCode](/documentation/coreservices/aebuilderrorcode)

#### Constants

- [var aeBuildSyntaxNoErr: Int](/documentation/coreservices/aebuildsyntaxnoerr)
- [var aeBuildSyntaxBadToken: Int](/documentation/coreservices/aebuildsyntaxbadtoken)
- [var aeBuildSyntaxBadEOF: Int](/documentation/coreservices/aebuildsyntaxbadeof)
- [var aeBuildSyntaxNoEOF: Int](/documentation/coreservices/aebuildsyntaxnoeof)
- [var aeBuildSyntaxBadNegative: Int](/documentation/coreservices/aebuildsyntaxbadnegative)
- [var aeBuildSyntaxMissingQuote: Int](/documentation/coreservices/aebuildsyntaxmissingquote)
- [var aeBuildSyntaxBadHex: Int](/documentation/coreservices/aebuildsyntaxbadhex)
- [var aeBuildSyntaxOddHex: Int](/documentation/coreservices/aebuildsyntaxoddhex)
- [var aeBuildSyntaxNoCloseHex: Int](/documentation/coreservices/aebuildsyntaxnoclosehex)
- [var aeBuildSyntaxUncoercedHex: Int](/documentation/coreservices/aebuildsyntaxuncoercedhex)
- [var aeBuildSyntaxNoCloseString: Int](/documentation/coreservices/aebuildsyntaxnoclosestring)
- [var aeBuildSyntaxBadDesc: Int](/documentation/coreservices/aebuildsyntaxbaddesc)
- [var aeBuildSyntaxBadData: Int](/documentation/coreservices/aebuildsyntaxbaddata)
- [var aeBuildSyntaxNoCloseParen: Int](/documentation/coreservices/aebuildsyntaxnocloseparen)
- [var aeBuildSyntaxNoCloseBracket: Int](/documentation/coreservices/aebuildsyntaxnoclosebracket)
- [var aeBuildSyntaxNoCloseBrace: Int](/documentation/coreservices/aebuildsyntaxnoclosebrace)
- [var aeBuildSyntaxNoKey: Int](/documentation/coreservices/aebuildsyntaxnokey)
- [var aeBuildSyntaxNoColon: Int](/documentation/coreservices/aebuildsyntaxnocolon)
- [var aeBuildSyntaxCoercedList: Int](/documentation/coreservices/aebuildsyntaxcoercedlist)
- [var aeBuildSyntaxUncoercedDoubleAt: Int](/documentation/coreservices/aebuildsyntaxuncoerceddoubleat)
- [AECoerceDescProcPtr](/documentation/coreservices/aecoercedescprocptr)
- [AECoerceDescUPP](/documentation/coreservices/aecoercedescupp)
- [AECoercePtrProcPtr](/documentation/coreservices/aecoerceptrprocptr)
- [AECoercePtrUPP](/documentation/coreservices/aecoerceptrupp)
- [AECoercionHandlerUPP](/documentation/coreservices/aecoercionhandlerupp)
- [AEDataStorage](/documentation/coreservices/aedatastorage)
- [AEDataStorageType](/documentation/coreservices/aedatastoragetype)
- [AEDescList](/documentation/coreservices/aedesclist)
- [AEDescPtr](/documentation/coreservices/aedescptr)
- [AEDisposeExternalProcPtr](/documentation/coreservices/aedisposeexternalprocptr)
- [AEDisposeExternalUPP](/documentation/coreservices/aedisposeexternalupp)
- [AEEventClass](/documentation/coreservices/aeeventclass)
- [AEEventHandlerProcPtr](/documentation/coreservices/aeeventhandlerprocptr)
- [AEEventHandlerUPP](/documentation/coreservices/aeeventhandlerupp)
- [AEEventID](/documentation/coreservices/aeeventid)
- [AEEventSource](/documentation/coreservices/aeeventsource)
- [AEKeyword](/documentation/coreservices/aekeyword)
- [AERecord](/documentation/coreservices/aerecord)
- [AERemoteProcessResolverCallback](/documentation/coreservices/aeremoteprocessresolvercallback)
- [AERemoteProcessResolverRef](/documentation/coreservices/aeremoteprocessresolverref)
- [AEReturnID](/documentation/coreservices/aereturnid)
- [AESendMode](/documentation/coreservices/aesendmode)

#### Constants

- [var kAENoReply: Int](/documentation/coreservices/kaenoreply)
- [var kAEQueueReply: Int](/documentation/coreservices/kaequeuereply)
- [var kAEWaitReply: Int](/documentation/coreservices/kaewaitreply)
- [var kAEDontReconnect: Int](/documentation/coreservices/kaedontreconnect)
- [var kAEWantReceipt: Int](/documentation/coreservices/kaewantreceipt)
- [var kAENeverInteract: Int](/documentation/coreservices/kaeneverinteract)
- [var kAECanInteract: Int](/documentation/coreservices/kaecaninteract)
- [var kAEAlwaysInteract: Int](/documentation/coreservices/kaealwaysinteract)
- [var kAECanSwitchLayer: Int](/documentation/coreservices/kaecanswitchlayer)
- [var kAEDontRecord: Int](/documentation/coreservices/kaedontrecord)
- [var kAEDontExecute: Int](/documentation/coreservices/kaedontexecute)
- [var kAEProcessNonReplyEvents: Int](/documentation/coreservices/kaeprocessnonreplyevents)
- [AESendPriority](/documentation/coreservices/aesendpriority)
- [AEStreamRef](/documentation/coreservices/aestreamref)
- [AETransactionID](/documentation/coreservices/aetransactionid)

### Enumerations

- [kAEDebugPOSTHeader](/documentation/coreservices/apple_events/1542854-kaedebugpostheader)

#### Constants

- [var kAEDebugPOSTHeader: Int](/documentation/coreservices/kaedebugpostheader)
- [var kAEDebugReplyHeader: Int](/documentation/coreservices/kaedebugreplyheader)
- [var kAEDebugXMLDebugAll: Int](/documentation/coreservices/kaedebugxmldebugall)
- [var kAEDebugXMLRequest: Int](/documentation/coreservices/kaedebugxmlrequest)
- [var kAEDebugXMLResponse: Int](/documentation/coreservices/kaedebugxmlresponse)
- [kAEHandleArray](/documentation/coreservices/apple_events/1542886-kaehandlearray)

#### Constants

- [var kAEHandleArray: Int](/documentation/coreservices/kaehandlearray)
- [kAEISGetURL](/documentation/coreservices/apple_events/1556362-kaeisgeturl)

#### Constants

- [var KAEISHandleCGI: OSType](/documentation/coreservices/kaeishandlecgi)
- [var kAEISGetURL: OSType](/documentation/coreservices/kaeisgeturl)
- [kAEISHTTPSearchArgs](/documentation/coreservices/apple_events/1556404-kaeishttpsearchargs)

#### Constants

- [var kAEISAction: OSType](/documentation/coreservices/kaeisaction)
- [var kAEISActionPath: OSType](/documentation/coreservices/kaeisactionpath)
- [var kAEISClientAddress: OSType](/documentation/coreservices/kaeisclientaddress)
- [var kAEISClientIP: OSType](/documentation/coreservices/kaeisclientip)
- [var kAEISContentType: OSType](/documentation/coreservices/kaeiscontenttype)
- [var kAEISFromUser: OSType](/documentation/coreservices/kaeisfromuser)
- [var kAEISFullRequest: OSType](/documentation/coreservices/kaeisfullrequest)
- [var kAEISHTTPSearchArgs: OSType](/documentation/coreservices/kaeishttpsearchargs)
- [var kAEISMethod: OSType](/documentation/coreservices/kaeismethod)
- [var kAEISPassword: OSType](/documentation/coreservices/kaeispassword)
- [var kAEISPostArgs: OSType](/documentation/coreservices/kaeispostargs)
- [var kAEISReferrer: OSType](/documentation/coreservices/kaeisreferrer)
- [var kAEISScriptName: OSType](/documentation/coreservices/kaeisscriptname)
- [var kAEISServerName: OSType](/documentation/coreservices/kaeisservername)
- [var kAEISServerPort: OSType](/documentation/coreservices/kaeisserverport)
- [var kAEISUserAgent: OSType](/documentation/coreservices/kaeisuseragent)
- [var kAEISUserName: OSType](/documentation/coreservices/kaeisusername)
- [kAEInfo](/documentation/coreservices/apple_events/1556393-kaeinfo)

#### Constants

- [var kAEInfo: Int](/documentation/coreservices/kaeinfo)
- [var kAEMain: Int](/documentation/coreservices/kaemain)
- [var kAESharing: Int](/documentation/coreservices/kaesharing)
- [kAEInternetSuite](/documentation/coreservices/apple_events/1556388-kaeinternetsuite)

#### Constants

- [var kAEISWebStarSuite: OSType](/documentation/coreservices/kaeiswebstarsuite)
- [var kAEInternetSuite: OSType](/documentation/coreservices/kaeinternetsuite)
- [kAELogOut](/documentation/coreservices/apple_events/1556395-kaelogout)

#### Constants

- [var kAELogOut: OSType](/documentation/coreservices/kaelogout)
- [var kAEReallyLogOut: OSType](/documentation/coreservices/kaereallylogout)
- [var kAEShowRestartDialog: OSType](/documentation/coreservices/kaeshowrestartdialog)
- [var kAEShowShutdownDialog: OSType](/documentation/coreservices/kaeshowshutdowndialog)
- [kAEMenuClass](/documentation/coreservices/apple_events/1556392-kaemenuclass)

#### Constants

- [var kAEKeyDown: OSType](/documentation/coreservices/kaekeydown)
- [var kAEMenuClass: OSType](/documentation/coreservices/kaemenuclass)
- [var kAEMenuSelect: OSType](/documentation/coreservices/kaemenuselect)
- [var kAEMouseDown: OSType](/documentation/coreservices/kaemousedown)
- [var kAEMouseDownInBack: OSType](/documentation/coreservices/kaemousedowninback)
- [var kAEPromise: OSType](/documentation/coreservices/kaepromise)
- [var kAEResized: OSType](/documentation/coreservices/kaeresized)
- [kAEMouseClass](/documentation/coreservices/apple_events/1556409-kaemouseclass)

#### Constants

- [var kAEActivate: OSType](/documentation/coreservices/kaeactivate)
- [var kAEApplicationClass: OSType](/documentation/coreservices/kaeapplicationclass)
- [var kAEAutoDown: OSType](/documentation/coreservices/kaeautodown)
- [var kAECommandClass: OSType](/documentation/coreservices/kaecommandclass)
- [var kAEDeactivate: OSType](/documentation/coreservices/kaedeactivate)
- [var kAEDiskEvent: OSType](/documentation/coreservices/kaediskevent)
- [var kAEDown: OSType](/documentation/coreservices/kaedown)
- [var kAEHighLevel: OSType](/documentation/coreservices/kaehighlevel)
- [var kAEKeyClass: OSType](/documentation/coreservices/kaekeyclass)
- [var kAEMouseClass: OSType](/documentation/coreservices/kaemouseclass)
- [var kAEMoved: OSType](/documentation/coreservices/kaemoved)
- [var kAENavigationKey: OSType](/documentation/coreservices/kaenavigationkey)
- [var kAENullEvent: OSType](/documentation/coreservices/kaenullevent)
- [var kAERawKey: OSType](/documentation/coreservices/kaerawkey)
- [var kAEResume: OSType](/documentation/coreservices/kaeresume)
- [var kAEScrapEvent: OSType](/documentation/coreservices/kaescrapevent)
- [var kAEStoppedMoving: OSType](/documentation/coreservices/kaestoppedmoving)
- [var kAESuspend: OSType](/documentation/coreservices/kaesuspend)
- [var kAEUp: OSType](/documentation/coreservices/kaeup)
- [var kAEUpdate: OSType](/documentation/coreservices/kaeupdate)
- [var kAEVirtualKey: OSType](/documentation/coreservices/kaevirtualkey)
- [var kAEWakeUpEvent: OSType](/documentation/coreservices/kaewakeupevent)
- [var kAEWindowClass: OSType](/documentation/coreservices/kaewindowclass)
- [kAENonmodifiable](/documentation/coreservices/apple_events/1556386-kaenonmodifiable)

#### Constants

- [var kAENonmodifiable: OSType](/documentation/coreservices/kaenonmodifiable)
- [var kAEOpen: OSType](/documentation/coreservices/kaeopen)
- [var kAEOpenSelection: OSType](/documentation/coreservices/kaeopenselection)
- [var kAEOutline: OSType](/documentation/coreservices/kaeoutline)
- [var kAEPageSetup: OSType](/documentation/coreservices/kaepagesetup)
- [var kAEPaste: OSType](/documentation/coreservices/kaepaste)
- [var kAEPlain: OSType](/documentation/coreservices/kaeplain)
- [var kAEPrint: OSType](/documentation/coreservices/kaeprint)
- [var kAEPrintSelection: OSType](/documentation/coreservices/kaeprintselection)
- [var kAEPrintWindow: OSType](/documentation/coreservices/kaeprintwindow)
- [var kAEPutAwaySelection: OSType](/documentation/coreservices/kaeputawayselection)
- [var kAEQDAdMax: OSType](/documentation/coreservices/kaeqdadmax)
- [var kAEQDAdMin: OSType](/documentation/coreservices/kaeqdadmin)
- [var kAEQDAddOver: OSType](/documentation/coreservices/kaeqdaddover)
- [var kAEQDAddPin: OSType](/documentation/coreservices/kaeqdaddpin)
- [var kAEQDBic: OSType](/documentation/coreservices/kaeqdbic)
- [var kAEQDBlend: OSType](/documentation/coreservices/kaeqdblend)
- [var kAEQDCopy: OSType](/documentation/coreservices/kaeqdcopy)
- [var kAEQDNotBic: OSType](/documentation/coreservices/kaeqdnotbic)
- [var kAEQDNotCopy: OSType](/documentation/coreservices/kaeqdnotcopy)
- [kAEQDNotOr](/documentation/coreservices/apple_events/1556377-kaeqdnotor)

#### Constants

- [var kAEQDNotOr: OSType](/documentation/coreservices/kaeqdnotor)
- [var kAEQDNotXor: OSType](/documentation/coreservices/kaeqdnotxor)
- [var kAEQDOr: OSType](/documentation/coreservices/kaeqdor)
- [var kAEQDSubOver: OSType](/documentation/coreservices/kaeqdsubover)
- [var kAEQDSubPin: OSType](/documentation/coreservices/kaeqdsubpin)
- [var kAEQDSupplementalSuite: OSType](/documentation/coreservices/kaeqdsupplementalsuite)
- [var kAEQDXor: OSType](/documentation/coreservices/kaeqdxor)
- [var kAEQuickdrawSuite: OSType](/documentation/coreservices/kaequickdrawsuite)
- [var kAEQuitAll: OSType](/documentation/coreservices/kaequitall)
- [var kAERedo: OSType](/documentation/coreservices/kaeredo)
- [var kAERegular: OSType](/documentation/coreservices/kaeregular)
- [var kAEReopenApplication: OSType](/documentation/coreservices/kaereopenapplication)
- [var kAEReplace: OSType](/documentation/coreservices/kaereplace)
- [var kAERequiredSuite: OSType](/documentation/coreservices/kaerequiredsuite)
- [var kAERestart: OSType](/documentation/coreservices/kaerestart)
- [var kAERevealSelection: OSType](/documentation/coreservices/kaerevealselection)
- [var kAERevert: OSType](/documentation/coreservices/kaerevert)
- [var kAERightJustified: OSType](/documentation/coreservices/kaerightjustified)
- [var kAESave: OSType](/documentation/coreservices/kaesave)
- [var kAESelect: OSType](/documentation/coreservices/kaeselect)
- [var kAESetData: OSType](/documentation/coreservices/kaesetdata)
- [kAESetPosition](/documentation/coreservices/apple_events/1556407-kaesetposition)

#### Constants

- [var kAESetPosition: OSType](/documentation/coreservices/kaesetposition)
- [var kAEShadow: OSType](/documentation/coreservices/kaeshadow)
- [var kAEShowClipboard: OSType](/documentation/coreservices/kaeshowclipboard)
- [var kAEShutDown: OSType](/documentation/coreservices/kaeshutdown)
- [var kAESleep: OSType](/documentation/coreservices/kaesleep)
- [var kAESmallCaps: OSType](/documentation/coreservices/kaesmallcaps)
- [var kAESpecialClassProperties: OSType](/documentation/coreservices/kaespecialclassproperties)
- [var kAEStrikethrough: OSType](/documentation/coreservices/kaestrikethrough)
- [var kAESubscript: OSType](/documentation/coreservices/kaesubscript)
- [var kAESuperscript: OSType](/documentation/coreservices/kaesuperscript)
- [var kAETableSuite: OSType](/documentation/coreservices/kaetablesuite)
- [var kAETextSuite: OSType](/documentation/coreservices/kaetextsuite)
- [var kAETransactionTerminated: OSType](/documentation/coreservices/kaetransactionterminated)
- [var kAEUnderline: OSType](/documentation/coreservices/kaeunderline)
- [var kAEUndo: OSType](/documentation/coreservices/kaeundo)
- [var kAEWholeWordEquals: OSType](/documentation/coreservices/kaewholewordequals)
- [var kAEYes: OSType](/documentation/coreservices/kaeyes)
- [var kAEZoom: OSType](/documentation/coreservices/kaezoom)
- [kAESocks4Protocol](/documentation/coreservices/apple_events/1542847-kaesocks4protocol)

#### Constants

- [var kAESocks4Protocol: Int](/documentation/coreservices/kaesocks4protocol)
- [var kAESocks5Protocol: Int](/documentation/coreservices/kaesocks5protocol)
- [kAEUTHasReturningParam](/documentation/coreservices/apple_events/1457911-kaeuthasreturningparam)

#### Constants

- [var kAEUTApostrophe: Int](/documentation/coreservices/kaeutapostrophe)
- [var kAEUTChangesState: Int](/documentation/coreservices/kaeutchangesstate)
- [var kAEUTDirectParamIsReference: Int](/documentation/coreservices/kaeutdirectparamisreference)
- [var kAEUTEnumListIsExclusive: Int](/documentation/coreservices/kaeutenumlistisexclusive)
- [var kAEUTEnumerated: Int](/documentation/coreservices/kaeutenumerated)
- [var kAEUTEnumsAreTypes: Int](/documentation/coreservices/kaeutenumsaretypes)
- [var kAEUTFeminine: Int](/documentation/coreservices/kaeutfeminine)
- [var kAEUTHasReturningParam: Int](/documentation/coreservices/kaeuthasreturningparam)
- [var kAEUTMasculine: Int](/documentation/coreservices/kaeutmasculine)
- [var kAEUTNotDirectParamIsTarget: Int](/documentation/coreservices/kaeutnotdirectparamistarget)
- [var kAEUTOptional: Int](/documentation/coreservices/kaeutoptional)
- [var kAEUTParamIsReference: Int](/documentation/coreservices/kaeutparamisreference)
- [var kAEUTParamIsTarget: Int](/documentation/coreservices/kaeutparamistarget)
- [var kAEUTPlural: Int](/documentation/coreservices/kaeutplural)
- [var kAEUTPropertyIsReference: Int](/documentation/coreservices/kaeutpropertyisreference)
- [var kAEUTReadWrite: Int](/documentation/coreservices/kaeutreadwrite)
- [var kAEUTReplyIsReference: Int](/documentation/coreservices/kaeutreplyisreference)
- [var kAEUTTightBindingFunction: Int](/documentation/coreservices/kaeuttightbindingfunction)
- [var kAEUTlistOfItems: Int](/documentation/coreservices/kaeutlistofitems)
- [kAEUseHTTPProxyAttr](/documentation/coreservices/apple_events/1542824-kaeusehttpproxyattr)

#### Constants

- [var kAEUseHTTPProxyAttr: Int](/documentation/coreservices/kaeusehttpproxyattr)
- [var kAEHTTPProxyPortAttr: Int](/documentation/coreservices/kaehttpproxyportattr)
- [var kAEHTTPProxyHostAttr: Int](/documentation/coreservices/kaehttpproxyhostattr)
- [kAEUseSocksAttr](/documentation/coreservices/apple_events/1542933-kaeusesocksattr)

#### Constants

- [var kAESocksHostAttr: Int](/documentation/coreservices/kaesockshostattr)
- [var kAESocksPasswordAttr: Int](/documentation/coreservices/kaesockspasswordattr)
- [var kAESocksPortAttr: Int](/documentation/coreservices/kaesocksportattr)
- [var kAESocksProxyAttr: Int](/documentation/coreservices/kaesocksproxyattr)
- [var kAESocksUserAttr: Int](/documentation/coreservices/kaesocksuserattr)
- [var kAEUseSocksAttr: Int](/documentation/coreservices/kaeusesocksattr)
- [kAEUserTerminology](/documentation/coreservices/apple_events/1457902-kaeuserterminology)

#### Constants

- [var kAEOSAXSizeResource: OSType](/documentation/coreservices/kaeosaxsizeresource)
- [var kAEScriptingSizeResource: OSType](/documentation/coreservices/kaescriptingsizeresource)
- [var kAETerminologyExtension: OSType](/documentation/coreservices/kaeterminologyextension)
- [var kAEUserTerminology: OSType](/documentation/coreservices/kaeuserterminology)
- [kAEZoomIn](/documentation/coreservices/apple_events/1556365-kaezoomin)

#### Constants

- [var kAEZoomIn: Int](/documentation/coreservices/kaezoomin)
- [var kAEZoomOut: Int](/documentation/coreservices/kaezoomout)
- [keyAEAngle](/documentation/coreservices/apple_events/1556380-keyaeangle)

#### Constants

- [var keyAEAngle: AEKeyword](/documentation/coreservices/keyaeangle)
- [var keyAEArcAngle: AEKeyword](/documentation/coreservices/keyaearcangle)
- [keyAEBaseAddr](/documentation/coreservices/apple_events/1556383-keyaebaseaddr)

#### Constants

- [var keyAEBaseAddr: AEKeyword](/documentation/coreservices/keyaebaseaddr)
- [var keyAEBestType: AEKeyword](/documentation/coreservices/keyaebesttype)
- [var keyAEBgndColor: AEKeyword](/documentation/coreservices/keyaebgndcolor)
- [var keyAEBgndPattern: AEKeyword](/documentation/coreservices/keyaebgndpattern)
- [var keyAEBounds: AEKeyword](/documentation/coreservices/keyaebounds)
- [var keyAECellList: AEKeyword](/documentation/coreservices/keyaecelllist)
- [var keyAEClassID: AEKeyword](/documentation/coreservices/keyaeclassid)
- [var keyAEColor: AEKeyword](/documentation/coreservices/keyaecolor)
- [var keyAEColorTable: AEKeyword](/documentation/coreservices/keyaecolortable)
- [var keyAECurveHeight: AEKeyword](/documentation/coreservices/keyaecurveheight)
- [var keyAECurveWidth: AEKeyword](/documentation/coreservices/keyaecurvewidth)
- [var keyAEDashStyle: AEKeyword](/documentation/coreservices/keyaedashstyle)
- [var keyAEData: AEKeyword](/documentation/coreservices/keyaedata)
- [var keyAEDefaultType: AEKeyword](/documentation/coreservices/keyaedefaulttype)
- [var keyAEDefinitionRect: AEKeyword](/documentation/coreservices/keyaedefinitionrect)
- [var keyAEDescType: AEKeyword](/documentation/coreservices/keyaedesctype)
- [var keyAEDestination: AEKeyword](/documentation/coreservices/keyaedestination)
- [var keyAEDoAntiAlias: AEKeyword](/documentation/coreservices/keyaedoantialias)
- [var keyAEDoDithered: AEKeyword](/documentation/coreservices/keyaedodithered)
- [var keyAEDoRotate: AEKeyword](/documentation/coreservices/keyaedorotate)
- [keyAEDoScale](/documentation/coreservices/apple_events/1556387-keyaedoscale)

#### Constants

- [var keyAEDoScale: AEKeyword](/documentation/coreservices/keyaedoscale)
- [var keyAEDoTranslate: AEKeyword](/documentation/coreservices/keyaedotranslate)
- [var keyAEEditionFileLoc: AEKeyword](/documentation/coreservices/keyaeeditionfileloc)
- [var keyAEElements: AEKeyword](/documentation/coreservices/keyaeelements)
- [var keyAEEndPoint: AEKeyword](/documentation/coreservices/keyaeendpoint)
- [var keyAEEventClass: AEKeyword](/documentation/coreservices/keyaeeventclass)
- [var keyAEEventID: AEKeyword](/documentation/coreservices/keyaeeventid)
- [var keyAEFile: AEKeyword](/documentation/coreservices/keyaefile)
- [var keyAEFileType: AEKeyword](/documentation/coreservices/keyaefiletype)
- [var keyAEFillColor: AEKeyword](/documentation/coreservices/keyaefillcolor)
- [var keyAEFillPattern: AEKeyword](/documentation/coreservices/keyaefillpattern)
- [var keyAEFlipHorizontal: AEKeyword](/documentation/coreservices/keyaefliphorizontal)
- [var keyAEFlipVertical: AEKeyword](/documentation/coreservices/keyaeflipvertical)
- [var keyAEFont: AEKeyword](/documentation/coreservices/keyaefont)
- [var keyAEFormula: AEKeyword](/documentation/coreservices/keyaeformula)
- [var keyAEGraphicObjects: AEKeyword](/documentation/coreservices/keyaegraphicobjects)
- [var keyAEID: AEKeyword](/documentation/coreservices/keyaeid)
- [var keyAEImageQuality: AEKeyword](/documentation/coreservices/keyaeimagequality)
- [var keyAEInsertHere: AEKeyword](/documentation/coreservices/keyaeinserthere)
- [var keyAEKeyForms: AEKeyword](/documentation/coreservices/keyaekeyforms)
- [keyAEHiliteRange](/documentation/coreservices/apple_events/1556379-keyaehiliterange)

#### Constants

- [var keyAEClauseOffsets: AEKeyword](/documentation/coreservices/keyaeclauseoffsets)
- [var keyAEDragging: AEKeyword](/documentation/coreservices/keyaedragging)
- [var keyAEHiliteRange: AEKeyword](/documentation/coreservices/keyaehiliterange)
- [var keyAELeftSide: AEKeyword](/documentation/coreservices/keyaeleftside)
- [var keyAEOffset: AEKeyword](/documentation/coreservices/keyaeoffset)
- [var keyAEPinRange: AEKeyword](/documentation/coreservices/keyaepinrange)
- [var keyAEPoint: AEKeyword](/documentation/coreservices/keyaepoint)
- [var keyAERegionClass: AEKeyword](/documentation/coreservices/keyaeregionclass)
- [keyAEKeyword](/documentation/coreservices/apple_events/1556374-keyaekeyword)

#### Constants

- [var keyAEKeyword: AEKeyword](/documentation/coreservices/keyaekeyword)
- [var keyAELevel: AEKeyword](/documentation/coreservices/keyaelevel)
- [var keyAELineArrow: AEKeyword](/documentation/coreservices/keyaelinearrow)
- [var keyAEName: AEKeyword](/documentation/coreservices/keyaename)
- [var keyAENewElementLoc: AEKeyword](/documentation/coreservices/keyaenewelementloc)
- [var keyAEObject: AEKeyword](/documentation/coreservices/keyaeobject)
- [var keyAEObjectClass: AEKeyword](/documentation/coreservices/keyaeobjectclass)
- [var keyAEOffStyles: AEKeyword](/documentation/coreservices/keyaeoffstyles)
- [var keyAEOnStyles: AEKeyword](/documentation/coreservices/keyaeonstyles)
- [var keyAEPMTable: AEKeyword](/documentation/coreservices/keyaepmtable)
- [var keyAEParamFlags: AEKeyword](/documentation/coreservices/keyaeparamflags)
- [var keyAEParameters: AEKeyword](/documentation/coreservices/keyaeparameters)
- [var keyAEPenColor: AEKeyword](/documentation/coreservices/keyaepencolor)
- [var keyAEPenPattern: AEKeyword](/documentation/coreservices/keyaepenpattern)
- [var keyAEPenWidth: AEKeyword](/documentation/coreservices/keyaepenwidth)
- [var keyAEPixMapMinus: AEKeyword](/documentation/coreservices/keyaepixmapminus)
- [var keyAEPixelDepth: AEKeyword](/documentation/coreservices/keyaepixeldepth)
- [var keyAEPointList: AEKeyword](/documentation/coreservices/keyaepointlist)
- [var keyAEPointSize: AEKeyword](/documentation/coreservices/keyaepointsize)
- [var keyAEPosition: AEKeyword](/documentation/coreservices/keyaeposition)
- [keyAESuiteID](/documentation/coreservices/apple_events/1556370-keyaesuiteid)

#### Constants

- [var keyAESuiteID: AEKeyword](/documentation/coreservices/keyaesuiteid)
- [var keyAEText: AEKeyword](/documentation/coreservices/keyaetext)
- [var keyAETextColor: AEKeyword](/documentation/coreservices/keyaetextcolor)
- [var keyAETextFont: AEKeyword](/documentation/coreservices/keyaetextfont)
- [var keyAETextLineAscent: AEKeyword](/documentation/coreservices/keyaetextlineascent)
- [var keyAETextLineHeight: AEKeyword](/documentation/coreservices/keyaetextlineheight)
- [var keyAETextPointSize: AEKeyword](/documentation/coreservices/keyaetextpointsize)
- [var keyAETextStyles: AEKeyword](/documentation/coreservices/keyaetextstyles)
- [var keyAETheText: AEKeyword](/documentation/coreservices/keyaethetext)
- [var keyAETransferMode: AEKeyword](/documentation/coreservices/keyaetransfermode)
- [var keyAETranslation: AEKeyword](/documentation/coreservices/keyaetranslation)
- [var keyAETryAsStructGraf: AEKeyword](/documentation/coreservices/keyaetryasstructgraf)
- [var keyAEUniformStyles: AEKeyword](/documentation/coreservices/keyaeuniformstyles)
- [var keyAEUpdateOn: AEKeyword](/documentation/coreservices/keyaeupdateon)
- [var keyAEUserTerm: AEKeyword](/documentation/coreservices/keyaeuserterm)
- [var keyAEWindow: AEKeyword](/documentation/coreservices/keyaewindow)
- [var keyAEWritingCode: AEKeyword](/documentation/coreservices/keyaewritingcode)
- [keyMenuID](/documentation/coreservices/apple_events/1556381-keymenuid)

#### Constants

- [var keyCloseAllWindows: AEKeyword](/documentation/coreservices/keycloseallwindows)
- [var keyLocalWhere: AEKeyword](/documentation/coreservices/keylocalwhere)
- [var keyMenuID: AEKeyword](/documentation/coreservices/keymenuid)
- [var keyMenuItem: AEKeyword](/documentation/coreservices/keymenuitem)
- [var keyNewBounds: AEKeyword](/documentation/coreservices/keynewbounds)
- [var keyOriginalBounds: AEKeyword](/documentation/coreservices/keyoriginalbounds)
- [keyMiscellaneous](/documentation/coreservices/apple_events/1556399-keymiscellaneous)

#### Constants

- [var keyDriveNumber: AEKeyword](/documentation/coreservices/keydrivenumber)
- [var keyErrorCode: AEKeyword](/documentation/coreservices/keyerrorcode)
- [var keyHighLevelClass: AEKeyword](/documentation/coreservices/keyhighlevelclass)
- [var keyHighLevelID: AEKeyword](/documentation/coreservices/keyhighlevelid)
- [var keyKey: AEKeyword](/documentation/coreservices/keykey)
- [var keyKeyCode: AEKeyword](/documentation/coreservices/keykeycode)
- [var keyKeyboard: AEKeyword](/documentation/coreservices/keykeyboard)
- [var keyMiscellaneous: AEKeyword](/documentation/coreservices/keymiscellaneous)
- [var keyModifiers: AEKeyword](/documentation/coreservices/keymodifiers)
- [var keySelection: AEKeyword](/documentation/coreservices/keyselection)
- [var keyWhen: AEKeyword](/documentation/coreservices/keywhen)
- [var keyWhere: AEKeyword](/documentation/coreservices/keywhere)
- [var keyWindow: AEKeyword](/documentation/coreservices/keywindow)
- [keyReplyPortAttr](/documentation/coreservices/apple_events/1571648-keyreplyportattr)

#### Constants

- [var keyReplyPortAttr: AEKeyword](/documentation/coreservices/keyreplyportattr)
- [keySOAPStructureMetaData](/documentation/coreservices/apple_events/1542797-keysoapstructuremetadata)

#### Constants

- [var keySOAPSMDNamespace: AEKeyword](/documentation/coreservices/keysoapsmdnamespace)
- [var keySOAPSMDNamespaceURI: AEKeyword](/documentation/coreservices/keysoapsmdnamespaceuri)
- [var keySOAPSMDType: AEKeyword](/documentation/coreservices/keysoapsmdtype)
- [var keySOAPStructureMetaData: AEKeyword](/documentation/coreservices/keysoapstructuremetadata)
- [keyUserNameAttr](/documentation/coreservices/apple_events/1542780-keyusernameattr)

#### Constants

- [var kAERPCClass: AEKeyword](/documentation/coreservices/kaerpcclass)
- [var kAESOAPScheme: AEKeyword](/documentation/coreservices/kaesoapscheme)
- [var kAESharedScriptHandler: AEKeyword](/documentation/coreservices/kaesharedscripthandler)
- [var kAEXMLRPCScheme: AEKeyword](/documentation/coreservices/kaexmlrpcscheme)
- [var keyAEPOSTHeaderData: AEKeyword](/documentation/coreservices/keyaepostheaderdata)
- [var keyAEReplyHeaderData: AEKeyword](/documentation/coreservices/keyaereplyheaderdata)
- [var keyAEXMLReplyData: AEKeyword](/documentation/coreservices/keyaexmlreplydata)
- [var keyAEXMLRequestData: AEKeyword](/documentation/coreservices/keyaexmlrequestdata)
- [var keyAdditionalHTTPHeaders: AEKeyword](/documentation/coreservices/keyadditionalhttpheaders)
- [var keyDisableAuthenticationAttr: AEKeyword](/documentation/coreservices/keydisableauthenticationattr)
- [var keyRPCMethodName: AEKeyword](/documentation/coreservices/keyrpcmethodname)
- [var keyRPCMethodParam: AEKeyword](/documentation/coreservices/keyrpcmethodparam)
- [var keyRPCMethodParamOrder: AEKeyword](/documentation/coreservices/keyrpcmethodparamorder)
- [var keySOAPAction: AEKeyword](/documentation/coreservices/keysoapaction)
- [var keySOAPMethodNameSpace: AEKeyword](/documentation/coreservices/keysoapmethodnamespace)
- [var keySOAPMethodNameSpaceURI: AEKeyword](/documentation/coreservices/keysoapmethodnamespaceuri)
- [var keySOAPSchemaVersion: AEKeyword](/documentation/coreservices/keysoapschemaversion)
- [var keyUserNameAttr: AEKeyword](/documentation/coreservices/keyusernameattr)
- [var keyUserPasswordAttr: AEKeyword](/documentation/coreservices/keyuserpasswordattr)
- [var keyXMLDebuggingAttr: AEKeyword](/documentation/coreservices/keyxmldebuggingattr)
- [Apple Event Recording Event ID Constants](/documentation/coreservices/apple_events/1527224-apple_event_recording_event_id_c)

#### Constants

- [var kAEStartRecording: AEEventID](/documentation/coreservices/kaestartrecording)
- [var kAEStopRecording: AEEventID](/documentation/coreservices/kaestoprecording)
- [var kAENotifyStartRecording: AEEventID](/documentation/coreservices/kaenotifystartrecording)
- [var kAENotifyStopRecording: AEEventID](/documentation/coreservices/kaenotifystoprecording)
- [var kAENotifyRecording: AEEventID](/documentation/coreservices/kaenotifyrecording)
- [Callback Constants for the AEResolve Function](/documentation/coreservices/apple_events/1572741-callback_constants_for_the_aeres)

#### Constants

- [var kAEIDoMinimum: Int](/documentation/coreservices/kaeidominimum)
- [var kAEIDoWhose: Int](/documentation/coreservices/kaeidowhose)
- [var kAEIDoMarking: Int](/documentation/coreservices/kaeidomarking)
- [var kAEHandleSimpleRanges: Int](/documentation/coreservices/kaehandlesimpleranges)
- [var kAEPassSubDescs: Int](/documentation/coreservices/kaepasssubdescs)
- [var kAEResolveNestedLists: Int](/documentation/coreservices/kaeresolvenestedlists)
- [var kAEUseRelativeIterators: Int](/documentation/coreservices/kaeuserelativeiterators)
- [Constants for Object Specifiers, Positions, and Logical and Comparison Operations](/documentation/coreservices/apple_events/1572744-constants_for_object_specifiers_)

#### Constants

- [var kAEAND: Int](/documentation/coreservices/kaeand)
- [var kAEOR: Int](/documentation/coreservices/kaeor)
- [var kAENOT: Int](/documentation/coreservices/kaenot)
- [var kAEFirst: Int](/documentation/coreservices/kaefirst)
- [var kAELast: Int](/documentation/coreservices/kaelast)
- [var kAEMiddle: Int](/documentation/coreservices/kaemiddle)
- [var kAEAny: Int](/documentation/coreservices/kaeany)
- [var kAEAll: Int](/documentation/coreservices/kaeall)
- [var kAENext: Int](/documentation/coreservices/kaenext)
- [var kAEPrevious: Int](/documentation/coreservices/kaeprevious)
- [var keyAECompOperator: Int](/documentation/coreservices/keyaecompoperator)
- [var keyAELogicalTerms: Int](/documentation/coreservices/keyaelogicalterms)
- [var keyAELogicalOperator: Int](/documentation/coreservices/keyaelogicaloperator)
- [var keyAEObject1: Int](/documentation/coreservices/keyaeobject1)
- [var keyAEObject2: Int](/documentation/coreservices/keyaeobject2)
- [var keyAEDesiredClass: Int](/documentation/coreservices/keyaedesiredclass)
- [var keyAEContainer: Int](/documentation/coreservices/keyaecontainer)
- [var keyAEKeyForm: Int](/documentation/coreservices/keyaekeyform)
- [var keyAEKeyData: Int](/documentation/coreservices/keyaekeydata)
- [Data Array Constants](/documentation/coreservices/apple_events/1542848-data_array_constants)

#### Constants

- [var kAEDataArray: Int](/documentation/coreservices/kaedataarray)
- [var kAEPackedArray: Int](/documentation/coreservices/kaepackedarray)
- [var kAEDescArray: Int](/documentation/coreservices/kaedescarray)
- [var kAEKeyDescArray: Int](/documentation/coreservices/kaekeydescarray)
- [Descriptor Type Constants](/documentation/coreservices/apple_events/1542788-descriptor_type_constants)

#### Constants

- [var typeAEList: DescType](/documentation/coreservices/typeaelist)
- [var typeAERecord: DescType](/documentation/coreservices/typeaerecord)
- [var typeAppleEvent: DescType](/documentation/coreservices/typeappleevent)
- [var typeTrue: DescType](/documentation/coreservices/typetrue)
- [var typeFalse: DescType](/documentation/coreservices/typefalse)
- [var typeAlias: DescType](/documentation/coreservices/typealias)
- [var typeEnumerated: DescType](/documentation/coreservices/typeenumerated)
- [var typeType: DescType](/documentation/coreservices/typetype)
- [var typeAppParameters: DescType](/documentation/coreservices/typeappparameters)
- [var typeProperty: DescType](/documentation/coreservices/typeproperty)
- [var typeFSRef: DescType](/documentation/coreservices/typefsref)
- [var typeFileURL: DescType](/documentation/coreservices/typefileurl)
- [var typeKeyword: DescType](/documentation/coreservices/typekeyword)
- [var typeSectionH: DescType](/documentation/coreservices/typesectionh)
- [var typeWildCard: DescType](/documentation/coreservices/typewildcard)
- [var typeApplSignature: DescType](/documentation/coreservices/typeapplsignature)
- [var typeProcessSerialNumber: DescType](/documentation/coreservices/typeprocessserialnumber)
- [var typeApplicationURL: DescType](/documentation/coreservices/typeapplicationurl)
- [var typeNull: DescType](/documentation/coreservices/typenull)
- [var typeBookmarkData: DescType](/documentation/coreservices/typebookmarkdata)
- [var typeEventRecord: DescType](/documentation/coreservices/typeeventrecord)
- [var typeFixed: DescType](/documentation/coreservices/typefixed)
- [var typeQDRectangle: DescType](/documentation/coreservices/typeqdrectangle)
- [Event Class Constants](/documentation/coreservices/apple_events/1527210-event_class_constants)

#### Constants

- [var kCoreEventClass: DescType](/documentation/coreservices/kcoreeventclass)
- [Event ID Constants](/documentation/coreservices/apple_events/1527223-event_id_constants)

#### Constants

- [var kAEOpenApplication: AEEventID](/documentation/coreservices/kaeopenapplication)
- [var kAEReopenApplication: OSType](/documentation/coreservices/kaereopenapplication)
- [var kAEOpenDocuments: AEEventID](/documentation/coreservices/kaeopendocuments)
- [var kAEPrintDocuments: AEEventID](/documentation/coreservices/kaeprintdocuments)
- [var kAEOpenContents: AEEventID](/documentation/coreservices/kaeopencontents)
- [var kAEQuitApplication: AEEventID](/documentation/coreservices/kaequitapplication)
- [var kAEAnswer: AEEventID](/documentation/coreservices/kaeanswer)
- [var kAEApplicationDied: AEEventID](/documentation/coreservices/kaeapplicationdied)
- [var kAEShowPreferences: AEEventID](/documentation/coreservices/kaeshowpreferences)
- [Event Source Constants](/documentation/coreservices/apple_events/1527201-event_source_constants)

#### Constants

- [var kAEUnknownSource: Int](/documentation/coreservices/kaeunknownsource)
- [var kAEDirectCall: Int](/documentation/coreservices/kaedirectcall)
- [var kAESameProcess: Int](/documentation/coreservices/kaesameprocess)
- [var kAELocalProcess: Int](/documentation/coreservices/kaelocalprocess)
- [var kAERemoteProcess: Int](/documentation/coreservices/kaeremoteprocess)
- [Factoring Constants](/documentation/coreservices/apple_events/1542928-factoring_constants)

#### Constants

- [var kAEDescListFactorNone: Int](/documentation/coreservices/kaedesclistfactornone)
- [var kAEDescListFactorType: Int](/documentation/coreservices/kaedesclistfactortype)
- [var kAEDescListFactorTypeAndSize: Int](/documentation/coreservices/kaedesclistfactortypeandsize)
- [ID Constants for the AECreateAppleEvent Function](/documentation/coreservices/apple_events/1542799-id_constants_for_the_aecreateapp)

#### Constants

- [var kAutoGenerateReturnID: Int](/documentation/coreservices/kautogeneratereturnid)
- [var kAnyTransactionID: Int](/documentation/coreservices/kanytransactionid)
- [Key Form and Descriptor Type Object Specifier Constants](/documentation/coreservices/apple_events/1572731-key_form_and_descriptor_type_obj)

#### Constants

- [var formAbsolutePosition: Int](/documentation/coreservices/formabsoluteposition)
- [var formRelativePosition: Int](/documentation/coreservices/formrelativeposition)
- [var formTest: Int](/documentation/coreservices/formtest)
- [var formRange: Int](/documentation/coreservices/formrange)
- [var formPropertyID: Int](/documentation/coreservices/formpropertyid)
- [var formName: Int](/documentation/coreservices/formname)
- [var typeObjectSpecifier: DescType](/documentation/coreservices/typeobjectspecifier)
- [var typeObjectBeingExamined: DescType](/documentation/coreservices/typeobjectbeingexamined)
- [var typeCurrentContainer: DescType](/documentation/coreservices/typecurrentcontainer)
- [var typeToken: DescType](/documentation/coreservices/typetoken)
- [var typeRelativeDescriptor: DescType](/documentation/coreservices/typerelativedescriptor)
- [var typeAbsoluteOrdinal: DescType](/documentation/coreservices/typeabsoluteordinal)
- [var typeIndexDescriptor: DescType](/documentation/coreservices/typeindexdescriptor)
- [var typeRangeDescriptor: DescType](/documentation/coreservices/typerangedescriptor)
- [var typeLogicalDescriptor: DescType](/documentation/coreservices/typelogicaldescriptor)
- [var typeCompDescriptor: DescType](/documentation/coreservices/typecompdescriptor)
- [var typeOSLTokenList: DescType](/documentation/coreservices/typeosltokenlist)
- [var formUniqueID: Int](/documentation/coreservices/formuniqueid)
- [Keyword Attribute Constants](/documentation/coreservices/apple_events/1542920-keyword_attribute_constants)

#### Constants

- [var keyTransactionIDAttr: AEKeyword](/documentation/coreservices/keytransactionidattr)
- [var keyReturnIDAttr: AEKeyword](/documentation/coreservices/keyreturnidattr)
- [var keyEventClassAttr: AEKeyword](/documentation/coreservices/keyeventclassattr)
- [var keyEventIDAttr: AEKeyword](/documentation/coreservices/keyeventidattr)
- [var keyAddressAttr: AEKeyword](/documentation/coreservices/keyaddressattr)
- [var keyOptionalKeywordAttr: AEKeyword](/documentation/coreservices/keyoptionalkeywordattr)
- [var keyTimeoutAttr: AEKeyword](/documentation/coreservices/keytimeoutattr)
- [var keyInteractLevelAttr: AEKeyword](/documentation/coreservices/keyinteractlevelattr)
- [var keyEventSourceAttr: AEKeyword](/documentation/coreservices/keyeventsourceattr)
- [var keyMissedKeywordAttr: AEKeyword](/documentation/coreservices/keymissedkeywordattr)
- [var keyOriginalAddressAttr: AEKeyword](/documentation/coreservices/keyoriginaladdressattr)
- [var keyReplyRequestedAttr: AEKeyword](/documentation/coreservices/keyreplyrequestedattr)
- [var keyAcceptTimeoutAttr: AEKeyword](/documentation/coreservices/keyaccepttimeoutattr)
- [var keyActualSenderAuditToken: AEKeyword](/documentation/coreservices/keyactualsenderaudittoken)
- [var keySenderApplescriptEntitlementsAttr: AEKeyword](/documentation/coreservices/keysenderapplescriptentitlementsattr)
- [var keySenderApplicationIdentifierEntitlementAttr: AEKeyword](/documentation/coreservices/keysenderapplicationidentifierentitlementattr)
- [var keySenderApplicationSandboxed: AEKeyword](/documentation/coreservices/keysenderapplicationsandboxed)
- [var keySenderAuditTokenAttr: AEKeyword](/documentation/coreservices/keysenderaudittokenattr)
- [var keySenderEGIDAttr: AEKeyword](/documentation/coreservices/keysenderegidattr)
- [var keySenderEUIDAttr: AEKeyword](/documentation/coreservices/keysendereuidattr)
- [var keySenderGIDAttr: AEKeyword](/documentation/coreservices/keysendergidattr)
- [var keySenderPIDAttr: AEKeyword](/documentation/coreservices/keysenderpidattr)
- [var keySenderUIDAttr: AEKeyword](/documentation/coreservices/keysenderuidattr)
- [Keyword Parameter Constants](/documentation/coreservices/apple_events/1527206-keyword_parameter_constants)

#### Constants

- [var keyDirectObject: AEKeyword](/documentation/coreservices/keydirectobject)
- [var keyErrorNumber: AEKeyword](/documentation/coreservices/keyerrornumber)
- [var keyErrorString: AEKeyword](/documentation/coreservices/keyerrorstring)
- [var keyProcessSerialNumber: AEKeyword](/documentation/coreservices/keyprocessserialnumber)
- [var keyPreDispatch: AEKeyword](/documentation/coreservices/keypredispatch)
- [var keySelectProc: AEKeyword](/documentation/coreservices/keyselectproc)
- [var keyAERecorderCount: AEKeyword](/documentation/coreservices/keyaerecordercount)
- [var keyAEVersion: AEKeyword](/documentation/coreservices/keyaeversion)
- [Launch Apple Event Constants](/documentation/coreservices/apple_events/1556410-launch_apple_event_constants)

#### Constants

- [var keyAELaunchedAsLogInItem: AEKeyword](/documentation/coreservices/keyaelaunchedasloginitem)
- [var keyAELaunchedAsServiceItem: AEKeyword](/documentation/coreservices/keyaelaunchedasserviceitem)
- [Numeric Descriptor Type Constants](/documentation/coreservices/apple_events/1542872-numeric_descriptor_type_constant)

#### Constants

- [var typeSInt16: DescType](/documentation/coreservices/typesint16)
- [var typeUInt16: DescType](/documentation/coreservices/typeuint16)
- [var typeSInt32: DescType](/documentation/coreservices/typesint32)
- [var typeUInt32: DescType](/documentation/coreservices/typeuint32)
- [var typeSInt64: DescType](/documentation/coreservices/typesint64)
- [var typeUInt64: DescType](/documentation/coreservices/typeuint64)
- [var typeIEEE32BitFloatingPoint: DescType](/documentation/coreservices/typeieee32bitfloatingpoint)
- [var typeIEEE64BitFloatingPoint: DescType](/documentation/coreservices/typeieee64bitfloatingpoint)
- [var type128BitFloatingPoint: DescType](/documentation/coreservices/type128bitfloatingpoint)
- [var typeDecimalStruct: DescType](/documentation/coreservices/typedecimalstruct)
- [Object Class ID Constants](/documentation/coreservices/apple_events/1556368-object_class_id_constants)

#### Constants

- [var cParagraph: OSType](/documentation/coreservices/cparagraph)
- [var cPICT: OSType](/documentation/coreservices/cpict)
- [var cProperty: OSType](/documentation/coreservices/cproperty)
- [var cRGBColor: OSType](/documentation/coreservices/crgbcolor)
- [var cPixel: OSType](/documentation/coreservices/cpixel)
- [var cPixelMap: OSType](/documentation/coreservices/cpixelmap)
- [var cPolygon: OSType](/documentation/coreservices/cpolygon)
- [var cQDPoint: OSType](/documentation/coreservices/cqdpoint)
- [var cQDRectangle: OSType](/documentation/coreservices/cqdrectangle)
- [var cRectangle: OSType](/documentation/coreservices/crectangle)
- [var cRotation: OSType](/documentation/coreservices/crotation)
- [var cRoundedRectangle: OSType](/documentation/coreservices/croundedrectangle)
- [var cRow: OSType](/documentation/coreservices/crow)
- [var cSelection: OSType](/documentation/coreservices/cselection)
- [var cShortInteger: OSType](/documentation/coreservices/cshortinteger)
- [var cTable: OSType](/documentation/coreservices/ctable)
- [var cText: OSType](/documentation/coreservices/ctext)
- [var cTextFlow: OSType](/documentation/coreservices/ctextflow)
- [var cTextStyles: OSType](/documentation/coreservices/ctextstyles)
- [var cType: OSType](/documentation/coreservices/ctype)
- [Other Descriptor Type Constants](/documentation/coreservices/apple_events/1542760-other_descriptor_type_constants)

#### Constants

- [var typeBoolean: DescType](/documentation/coreservices/typeboolean)
- [var typeChar: DescType](/documentation/coreservices/typechar)
- [Priority Constants for the AESend Function (Deprecated in macOS)](/documentation/coreservices/apple_events/1542840-priority_constants_for_the_aesen)

#### Constants

- [var kAENormalPriority: Int](/documentation/coreservices/kaenormalpriority)
- [var kAEHighPriority: Int](/documentation/coreservices/kaehighpriority)
- [Special Handler Callback Constants](/documentation/coreservices/apple_events/1572726-special_handler_callback_constan)

#### Constants

- [var keyAERangeStart: AEKeyword](/documentation/coreservices/keyaerangestart)
- [var keyAERangeStop: AEKeyword](/documentation/coreservices/keyaerangestop)
- [var keyDisposeTokenProc: AEKeyword](/documentation/coreservices/keydisposetokenproc)
- [var keyAECompareProc: AEKeyword](/documentation/coreservices/keyaecompareproc)
- [var keyAECountProc: AEKeyword](/documentation/coreservices/keyaecountproc)
- [var keyAEMarkTokenProc: AEKeyword](/documentation/coreservices/keyaemarktokenproc)
- [var keyAEMarkProc: AEKeyword](/documentation/coreservices/keyaemarkproc)
- [var keyAEAdjustMarksProc: AEKeyword](/documentation/coreservices/keyaeadjustmarksproc)
- [var keyAEGetErrDescProc: AEKeyword](/documentation/coreservices/keyaegeterrdescproc)
- [Timeout Constants](/documentation/coreservices/apple_events/1542814-timeout_constants)

#### Constants

- [var kAEDefaultTimeout: Int](/documentation/coreservices/kaedefaulttimeout)
- [var kNoTimeOut: Int](/documentation/coreservices/knotimeout)
- [Backup Core](/documentation/coreservices/backup_core)

### Managing an Item’s Backup Exclusion Status

- [func CSBackupSetItemExcluded(CFURL!, Bool, Bool) -> OSStatus](/documentation/coreservices/1445043-csbackupsetitemexcluded)
- [func CSBackupIsItemExcluded(CFURL!, UnsafeMutablePointer<DarwinBoolean>!) -> Bool](/documentation/coreservices/1443602-csbackupisitemexcluded)
- [Dictionary Services](/documentation/coreservices/dictionary_services)

### Functions

- [func DCSGetTermRangeInString(DCSDictionary?, CFString, CFIndex) -> CFRange](/documentation/coreservices/1450556-dcsgettermrangeinstring)
- [func DCSCopyTextDefinition(DCSDictionary?, CFString, CFRange) -> Unmanaged<CFString>?](/documentation/coreservices/1446842-dcscopytextdefinition)

### Data Types

- [DCSDictionary](/documentation/coreservices/dcsdictionary)
- [File System Events](/documentation/coreservices/file_system_events)

### Functions

- [func FSEventStreamCopyDescription(ConstFSEventStreamRef) -> CFString](/documentation/coreservices/1442676-fseventstreamcopydescription)
- [func FSEventStreamCopyPathsBeingWatched(ConstFSEventStreamRef) -> CFArray](/documentation/coreservices/1447917-fseventstreamcopypathsbeingwatch)
- [func FSEventStreamCreate(CFAllocator?, FSEventStreamCallback, UnsafeMutablePointer<FSEventStreamContext>?, CFArray, FSEventStreamEventId, CFTimeInterval, FSEventStreamCreateFlags) -> FSEventStreamRef?](/documentation/coreservices/1443980-fseventstreamcreate)
- [func FSEventStreamCreateRelativeToDevice(CFAllocator?, FSEventStreamCallback, UnsafeMutablePointer<FSEventStreamContext>?, dev_t, CFArray, FSEventStreamEventId, CFTimeInterval, FSEventStreamCreateFlags) -> FSEventStreamRef?](/documentation/coreservices/1447341-fseventstreamcreaterelativetodev)
- [func FSEventStreamFlushAsync(FSEventStreamRef) -> FSEventStreamEventId](/documentation/coreservices/1441727-fseventstreamflushasync)
- [func FSEventStreamFlushSync(FSEventStreamRef)](/documentation/coreservices/1445629-fseventstreamflushsync)
- [func FSEventStreamGetDeviceBeingWatched(ConstFSEventStreamRef) -> dev_t](/documentation/coreservices/1449675-fseventstreamgetdevicebeingwatch)
- [func FSEventStreamGetLatestEventId(ConstFSEventStreamRef) -> FSEventStreamEventId](/documentation/coreservices/1446030-fseventstreamgetlatesteventid)
- [func FSEventStreamInvalidate(FSEventStreamRef)](/documentation/coreservices/1446990-fseventstreaminvalidate)
- [func FSEventStreamRelease(FSEventStreamRef)](/documentation/coreservices/1445989-fseventstreamrelease)
- [func FSEventStreamRetain(FSEventStreamRef)](/documentation/coreservices/1444986-fseventstreamretain)
- [func FSEventStreamScheduleWithRunLoop(FSEventStreamRef, CFRunLoop, CFString)](/documentation/coreservices/1447824-fseventstreamschedulewithrunloop)
- [func FSEventStreamSetDispatchQueue(FSEventStreamRef, dispatch_queue_t?)](/documentation/coreservices/1444164-fseventstreamsetdispatchqueue)
- [func FSEventStreamSetExclusionPaths(FSEventStreamRef, CFArray) -> Bool](/documentation/coreservices/1444666-fseventstreamsetexclusionpaths)
- [func FSEventStreamShow(ConstFSEventStreamRef)](/documentation/coreservices/1444302-fseventstreamshow)
- [func FSEventStreamStart(FSEventStreamRef) -> Bool](/documentation/coreservices/1448000-fseventstreamstart)
- [func FSEventStreamStop(FSEventStreamRef)](/documentation/coreservices/1447673-fseventstreamstop)
- [func FSEventStreamUnscheduleFromRunLoop(FSEventStreamRef, CFRunLoop, CFString)](/documentation/coreservices/1441982-fseventstreamunschedulefromrunlo)
- [func FSEventsCopyUUIDForDevice(dev_t) -> CFUUID?](/documentation/coreservices/1444453-fseventscopyuuidfordevice)
- [func FSEventsGetCurrentEventId() -> FSEventStreamEventId](/documentation/coreservices/1442917-fseventsgetcurrenteventid)
- [func FSEventsGetLastEventIdForDeviceBeforeTime(dev_t, CFAbsoluteTime) -> FSEventStreamEventId](/documentation/coreservices/1449772-fseventsgetlasteventidfordeviceb)
- [func FSEventsPurgeEventsForDeviceUpToEventId(dev_t, FSEventStreamEventId) -> Bool](/documentation/coreservices/1447985-fseventspurgeeventsfordeviceupto)

### Enumerations

- [FSEventStreamCreateFlags](/documentation/coreservices/file_system_events/1455376-fseventstreamcreateflags)

#### Constants

- [var kFSEventStreamCreateFlagNone: Int](/documentation/coreservices/kfseventstreamcreateflagnone)
- [var kFSEventStreamCreateFlagUseCFTypes: Int](/documentation/coreservices/kfseventstreamcreateflagusecftypes)
- [var kFSEventStreamCreateFlagNoDefer: Int](/documentation/coreservices/kfseventstreamcreateflagnodefer)
- [var kFSEventStreamCreateFlagWatchRoot: Int](/documentation/coreservices/kfseventstreamcreateflagwatchroot)
- [var kFSEventStreamCreateFlagIgnoreSelf: Int](/documentation/coreservices/kfseventstreamcreateflagignoreself)
- [var kFSEventStreamCreateFlagFileEvents: Int](/documentation/coreservices/kfseventstreamcreateflagfileevents)
- [var kFSEventStreamCreateFlagMarkSelf: Int](/documentation/coreservices/kfseventstreamcreateflagmarkself)
- [FSEventStreamEventFlags](/documentation/coreservices/file_system_events/1455361-fseventstreameventflags)

#### Constants

- [var kFSEventStreamEventFlagNone: Int](/documentation/coreservices/kfseventstreameventflagnone)
- [var kFSEventStreamEventFlagMustScanSubDirs: Int](/documentation/coreservices/kfseventstreameventflagmustscansubdirs)
- [var kFSEventStreamEventFlagUserDropped: Int](/documentation/coreservices/kfseventstreameventflaguserdropped)
- [var kFSEventStreamEventFlagKernelDropped: Int](/documentation/coreservices/kfseventstreameventflagkerneldropped)
- [var kFSEventStreamEventFlagEventIdsWrapped: Int](/documentation/coreservices/kfseventstreameventflageventidswrapped)
- [var kFSEventStreamEventFlagHistoryDone: Int](/documentation/coreservices/kfseventstreameventflaghistorydone)
- [var kFSEventStreamEventFlagRootChanged: Int](/documentation/coreservices/kfseventstreameventflagrootchanged)
- [var kFSEventStreamEventFlagMount: Int](/documentation/coreservices/kfseventstreameventflagmount)
- [var kFSEventStreamEventFlagUnmount: Int](/documentation/coreservices/kfseventstreameventflagunmount)
- [var kFSEventStreamEventFlagItemChangeOwner: Int](/documentation/coreservices/kfseventstreameventflagitemchangeowner)
- [var kFSEventStreamEventFlagItemCreated: Int](/documentation/coreservices/kfseventstreameventflagitemcreated)
- [var kFSEventStreamEventFlagItemFinderInfoMod: Int](/documentation/coreservices/kfseventstreameventflagitemfinderinfomod)
- [var kFSEventStreamEventFlagItemInodeMetaMod: Int](/documentation/coreservices/kfseventstreameventflagiteminodemetamod)
- [var kFSEventStreamEventFlagItemIsDir: Int](/documentation/coreservices/kfseventstreameventflagitemisdir)
- [var kFSEventStreamEventFlagItemIsFile: Int](/documentation/coreservices/kfseventstreameventflagitemisfile)
- [var kFSEventStreamEventFlagItemIsHardlink: Int](/documentation/coreservices/kfseventstreameventflagitemishardlink)
- [var kFSEventStreamEventFlagItemIsLastHardlink: Int](/documentation/coreservices/kfseventstreameventflagitemislasthardlink)
- [var kFSEventStreamEventFlagItemIsSymlink: Int](/documentation/coreservices/kfseventstreameventflagitemissymlink)
- [var kFSEventStreamEventFlagItemModified: Int](/documentation/coreservices/kfseventstreameventflagitemmodified)
- [var kFSEventStreamEventFlagItemRemoved: Int](/documentation/coreservices/kfseventstreameventflagitemremoved)
- [var kFSEventStreamEventFlagItemRenamed: Int](/documentation/coreservices/kfseventstreameventflagitemrenamed)
- [var kFSEventStreamEventFlagItemXattrMod: Int](/documentation/coreservices/kfseventstreameventflagitemxattrmod)
- [var kFSEventStreamEventFlagOwnEvent: Int](/documentation/coreservices/kfseventstreameventflagownevent)

### Data Types

- [FSEventStreamCallback](/documentation/coreservices/fseventstreamcallback)
- [FSEventStreamCreateFlags](/documentation/coreservices/fseventstreamcreateflags)
- [FSEventStreamEventFlags](/documentation/coreservices/fseventstreameventflags)
- [FSEventStreamEventId](/documentation/coreservices/fseventstreameventid)
- [FSEventStreamRef](/documentation/coreservices/fseventstreamref)

### Constants

- [var kFSEventStreamEventExtendedDataPathKey: String](/documentation/coreservices/kfseventstreameventextendeddatapathkey)
- [var kFSEventStreamEventExtendedFileIDKey: String](/documentation/coreservices/kfseventstreameventextendedfileidkey)
- [Launch Services](/documentation/coreservices/launch_services)

### Locating an App

- [func LSCopyDefaultApplicationURLForURL(CFURL, LSRolesMask, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<CFURL>?](/documentation/coreservices/1448824-lscopydefaultapplicationurlforur)
- [func LSCopyDefaultApplicationURLForContentType(CFString, LSRolesMask, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<CFURL>?](/documentation/coreservices/1447734-lscopydefaultapplicationurlforco)
- [func LSCopyApplicationURLsForURL(CFURL, LSRolesMask) -> Unmanaged<CFArray>?](/documentation/coreservices/1445148-lscopyapplicationurlsforurl)
- [func LSCanURLAcceptURL(CFURL, CFURL, LSRolesMask, LSAcceptanceFlags, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/coreservices/1441854-lscanurlaccepturl)
- [func LSCopyApplicationURLsForBundleIdentifier(CFString, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<CFArray>?](/documentation/coreservices/1449290-lscopyapplicationurlsforbundleid)

### Opening Items

- [func LSOpenCFURLRef(CFURL, UnsafeMutablePointer<Unmanaged<CFURL>?>?) -> OSStatus](/documentation/coreservices/1442850-lsopencfurlref)
- [func LSOpenFromURLSpec(UnsafePointer<LSLaunchURLSpec>, UnsafeMutablePointer<Unmanaged<CFURL>?>?) -> OSStatus](/documentation/coreservices/1441986-lsopenfromurlspec)
- [LSLaunchURLSpec](/documentation/coreservices/lslaunchurlspec)

#### Creating a Launch URL

- [init()](/documentation/coreservices/lslaunchurlspec/1444528-init)
- [init(appURL: Unmanaged<CFURL>?, itemURLs: Unmanaged<CFArray>?, passThruParams: UnsafePointer<AEDesc>?, launchFlags: LSLaunchFlags, asyncRefCon: UnsafeMutableRawPointer?)](/documentation/coreservices/lslaunchurlspec/1446360-init)

#### Configuring a Launch URL

- [var appURL: Unmanaged<CFURL>?](/documentation/coreservices/lslaunchurlspec/1443566-appurl)
- [var asyncRefCon: UnsafeMutableRawPointer?](/documentation/coreservices/lslaunchurlspec/1448168-asyncrefcon)
- [var itemURLs: Unmanaged<CFArray>?](/documentation/coreservices/lslaunchurlspec/1443759-itemurls)
- [var launchFlags: LSLaunchFlags](/documentation/coreservices/lslaunchurlspec/1443957-launchflags)
- [var passThruParams: UnsafePointer<AEDesc>?](/documentation/coreservices/lslaunchurlspec/1445136-passthruparams)
- [LSSharedFileList](/documentation/coreservices/lssharedfilelist)
- [LSSharedFileListItem](/documentation/coreservices/lssharedfilelistitem)

### Registering an App

- [func LSRegisterURL(CFURL, Bool) -> OSStatus](/documentation/coreservices/1446350-lsregisterurl)

### Working with Role Handlers

- [func LSCopyAllRoleHandlersForContentType(CFString, LSRolesMask) -> Unmanaged<CFArray>?](/documentation/coreservices/1448020-lscopyallrolehandlersforcontentt)
- [func LSCopyDefaultRoleHandlerForContentType(CFString, LSRolesMask) -> Unmanaged<CFString>?](/documentation/coreservices/1449868-lscopydefaultrolehandlerforconte)
- [func LSSetDefaultRoleHandlerForContentType(CFString, LSRolesMask, CFString) -> OSStatus](/documentation/coreservices/1444955-lssetdefaultrolehandlerforconten)
- [func LSSetDefaultHandlerForURLScheme(CFString, CFString) -> OSStatus](/documentation/coreservices/1447760-lssetdefaulthandlerforurlscheme)
- [LSRolesMask](/documentation/coreservices/lsrolesmask)

#### Constants

- [static var none: LSRolesMask](/documentation/coreservices/lsrolesmask/1442696-none)
- [static var viewer: LSRolesMask](/documentation/coreservices/lsrolesmask/1441708-viewer)
- [static var editor: LSRolesMask](/documentation/coreservices/lsrolesmask/1448087-editor)
- [static var shell: LSRolesMask](/documentation/coreservices/lsrolesmask/1442557-shell)
- [static var all: LSRolesMask](/documentation/coreservices/lsrolesmask/1450616-all)

#### Creating a Roles Mask

- [init(rawValue: OptionBits)](/documentation/coreservices/lsrolesmask/1445983-init)

### Understanding the Quarantine Properties Dictionary

- [let kLSQuarantineAgentBundleIdentifierKey: CFString](/documentation/coreservices/klsquarantineagentbundleidentifierkey)
- [let kLSQuarantineAgentNameKey: CFString](/documentation/coreservices/klsquarantineagentnamekey)
- [let kLSQuarantineTimeStampKey: CFString](/documentation/coreservices/klsquarantinetimestampkey)
- [let kLSQuarantineTypeKey: CFString](/documentation/coreservices/klsquarantinetypekey)
- [let kLSQuarantineDataURLKey: CFString](/documentation/coreservices/klsquarantinedataurlkey)
- [let kLSQuarantineOriginURLKey: CFString](/documentation/coreservices/klsquarantineoriginurlkey)

### Identifying the Quarantine Type

- [let kLSQuarantineTypeCalendarEventAttachment: CFString](/documentation/coreservices/klsquarantinetypecalendareventattachment)
- [let kLSQuarantineTypeEmailAttachment: CFString](/documentation/coreservices/klsquarantinetypeemailattachment)
- [let kLSQuarantineTypeInstantMessageAttachment: CFString](/documentation/coreservices/klsquarantinetypeinstantmessageattachment)
- [let kLSQuarantineTypeOtherAttachment: CFString](/documentation/coreservices/klsquarantinetypeotherattachment)
- [let kLSQuarantineTypeOtherDownload: CFString](/documentation/coreservices/klsquarantinetypeotherdownload)
- [let kLSQuarantineTypeWebDownload: CFString](/documentation/coreservices/klsquarantinetypewebdownload)

### Constants

- [LSLaunchFlags](/documentation/coreservices/lslaunchflags)

#### Creating Application Launch Flags

- [init(rawValue: OptionBits)](/documentation/coreservices/lslaunchflags/1449893-init)

#### Constants

- [static var defaults: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1443121-defaults)
- [static var andPrint: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1442495-andprint)
- [static var andDisplayErrors: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1443557-anddisplayerrors)
- [static var dontAddToRecents: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1442580-dontaddtorecents)
- [static var dontSwitch: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1442057-dontswitch)
- [static var async: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1445037-async)
- [static var newInstance: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1443359-newinstance)
- [static var andHide: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1444620-andhide)
- [static var andHideOthers: LSLaunchFlags](/documentation/coreservices/lslaunchflags/1448911-andhideothers)
- [LSAcceptanceFlags](/documentation/coreservices/lsacceptanceflags)

#### Creating Acceptance Flags

- [init(rawValue: OptionBits)](/documentation/coreservices/lsacceptanceflags/1443753-init)

#### Constants

- [static var acceptDefault: LSAcceptanceFlags](/documentation/coreservices/lsacceptanceflags/1447965-acceptdefault)
- [static var acceptAllowLoginUI: LSAcceptanceFlags](/documentation/coreservices/lsacceptanceflags/1443098-acceptallowloginui)
- [LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags)

#### Creating Item Information Flags

- [init(rawValue: OptionBits)](/documentation/coreservices/lsiteminfoflags/1442051-init)

#### Constants

- [static var isPlainFile: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1444223-isplainfile)
- [static var isPackage: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1449324-ispackage)
- [static var isApplication: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1449811-isapplication)
- [static var isContainer: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1443420-iscontainer)
- [static var isAliasFile: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1444478-isaliasfile)
- [static var isSymlink: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1446223-issymlink)
- [static var isInvisible: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1449065-isinvisible)
- [static var isNativeApp: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1443624-isnativeapp)
- [static var isClassicApp: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1449915-isclassicapp)
- [static var appPrefersNative: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1446535-appprefersnative)
- [static var appPrefersClassic: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1447454-appprefersclassic)
- [static var appIsScriptable: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1448463-appisscriptable)
- [static var isVolume: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1448330-isvolume)
- [static var extensionIsHidden: LSItemInfoFlags](/documentation/coreservices/lsiteminfoflags/1445838-extensionishidden)
- [LSHandlerOptions](/documentation/coreservices/lshandleroptions)

#### Creating Content Handler Options

- [init(rawValue: OptionBits)](/documentation/coreservices/lshandleroptions/1442692-init)

#### Constants

- [static var ignoreCreator: LSHandlerOptions](/documentation/coreservices/lshandleroptions/1445418-ignorecreator)
- [LSRequestedInfo](/documentation/coreservices/lsrequestedinfo)

#### Creating an Item Information Request

- [init(rawValue: OptionBits)](/documentation/coreservices/lsrequestedinfo/1443883-init)

#### Constants

- [static var requestExtension: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1448601-requestextension)
- [static var requestTypeCreator: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1446509-requesttypecreator)
- [static var requestBasicFlagsOnly: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1447145-requestbasicflagsonly)
- [static var requestAppTypeFlags: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1442110-requestapptypeflags)
- [static var requestAllFlags: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1445356-requestallflags)
- [static var requestIconAndKind: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1447945-requesticonandkind)
- [static var requestExtensionFlagsOnly: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1445164-requestextensionflagsonly)
- [static var requestAllInfo: LSRequestedInfo](/documentation/coreservices/lsrequestedinfo/1447901-requestallinfo)
- [Unknown Type or Creator](/documentation/coreservices/launch_services/1469201-unknown_type_or_creator)

#### Constants

- [var kLSUnknownType: OSType](/documentation/coreservices/klsunknowntype)
- [var kLSUnknownCreator: OSType](/documentation/coreservices/klsunknowncreator)

### Result Codes

- [var kLSAppInTrashErr: OSStatus](/documentation/coreservices/klsappintrasherr)
- [var kLSUnknownErr: OSStatus](/documentation/coreservices/klsunknownerr)
- [var kLSNotAnApplicationErr: OSStatus](/documentation/coreservices/klsnotanapplicationerr)
- [var kLSDataUnavailableErr: OSStatus](/documentation/coreservices/klsdataunavailableerr)
- [var kLSApplicationNotFoundErr: OSStatus](/documentation/coreservices/klsapplicationnotfounderr)
- [var kLSDataErr: OSStatus](/documentation/coreservices/klsdataerr)
- [var kLSLaunchInProgressErr: OSStatus](/documentation/coreservices/klslaunchinprogresserr)
- [var kLSServerCommunicationErr: OSStatus](/documentation/coreservices/klsservercommunicationerr)
- [var kLSCannotSetInfoErr: OSStatus](/documentation/coreservices/klscannotsetinfoerr)
- [var kLSIncompatibleSystemVersionErr: OSStatus](/documentation/coreservices/klsincompatiblesystemversionerr)
- [var kLSNoLaunchPermissionErr: OSStatus](/documentation/coreservices/klsnolaunchpermissionerr)
- [var kLSNoExecutableErr: OSStatus](/documentation/coreservices/klsnoexecutableerr)
- [var kLSMultipleSessionsNotSupportedErr: OSStatus](/documentation/coreservices/klsmultiplesessionsnotsupportederr)

### Deprecated

- [Deprecated Symbols](/documentation/coreservices/launch_services/deprecated_symbols)

#### Deprecated Constants

- [let kLSItemContentType: CFString!](/documentation/coreservices/klsitemcontenttype)
- [let kLSItemFileType: CFString!](/documentation/coreservices/klsitemfiletype)
- [let kLSItemFileCreator: CFString!](/documentation/coreservices/klsitemfilecreator)
- [let kLSItemExtension: CFString!](/documentation/coreservices/klsitemextension)
- [let kLSItemDisplayName: CFString!](/documentation/coreservices/klsitemdisplayname)
- [let kLSItemDisplayKind: CFString!](/documentation/coreservices/klsitemdisplaykind)
- [let kLSItemRoleHandlerDisplayName: CFString!](/documentation/coreservices/klsitemrolehandlerdisplayname)
- [let kLSItemIsInvisible: CFString!](/documentation/coreservices/klsitemisinvisible)
- [let kLSItemExtensionIsHidden: CFString!](/documentation/coreservices/klsitemextensionishidden)

#### Deprecated Structures

- [LSApplicationParameters](/documentation/coreservices/lsapplicationparameters)

##### Initializers

- [init()](/documentation/coreservices/lsapplicationparameters/1441947-init)
- [init(version: CFIndex, flags: LSLaunchFlags, application: UnsafePointer<FSRef>!, asyncLaunchRefCon: UnsafeMutableRawPointer!, environment: Unmanaged<CFDictionary>!, argv: Unmanaged<CFArray>!, initialEvent: UnsafeMutablePointer<AppleEvent>!)](/documentation/coreservices/lsapplicationparameters/1446779-init)

##### Instance Properties

- [var application: UnsafePointer<FSRef>!](/documentation/coreservices/lsapplicationparameters/1447460-application)
- [var argv: Unmanaged<CFArray>!](/documentation/coreservices/lsapplicationparameters/1445515-argv)
- [var asyncLaunchRefCon: UnsafeMutableRawPointer!](/documentation/coreservices/lsapplicationparameters/1444464-asynclaunchrefcon)
- [var environment: Unmanaged<CFDictionary>!](/documentation/coreservices/lsapplicationparameters/1449247-environment)
- [var flags: LSLaunchFlags](/documentation/coreservices/lsapplicationparameters/1450209-flags)
- [var initialEvent: UnsafeMutablePointer<AppleEvent>!](/documentation/coreservices/lsapplicationparameters/1446633-initialevent)
- [var version: CFIndex](/documentation/coreservices/lsapplicationparameters/1441822-version)
- [LSLaunchFSRefSpec](/documentation/coreservices/lslaunchfsrefspec)

##### Initializers

- [init()](/documentation/coreservices/lslaunchfsrefspec/1443478-init)
- [init(appRef: UnsafePointer<FSRef>!, numDocs: Int, itemRefs: UnsafePointer<FSRef>!, passThruParams: UnsafePointer<AEDesc>!, launchFlags: LSLaunchFlags, asyncRefCon: UnsafeMutableRawPointer!)](/documentation/coreservices/lslaunchfsrefspec/1442457-init)

##### Instance Properties

- [var appRef: UnsafePointer<FSRef>!](/documentation/coreservices/lslaunchfsrefspec/1448321-appref)
- [var asyncRefCon: UnsafeMutableRawPointer!](/documentation/coreservices/lslaunchfsrefspec/1450600-asyncrefcon)
- [var itemRefs: UnsafePointer<FSRef>!](/documentation/coreservices/lslaunchfsrefspec/1444360-itemrefs)
- [var launchFlags: LSLaunchFlags](/documentation/coreservices/lslaunchfsrefspec/1449431-launchflags)
- [var numDocs: Int](/documentation/coreservices/lslaunchfsrefspec/1450323-numdocs)
- [var passThruParams: UnsafePointer<AEDesc>!](/documentation/coreservices/lslaunchfsrefspec/1445933-passthruparams)
- [LSItemInfoRecord](/documentation/coreservices/lsiteminforecord)

##### Initializers

- [init()](/documentation/coreservices/lsiteminforecord/1445690-init)
- [init(flags: LSItemInfoFlags, filetype: OSType, creator: OSType, extension: Unmanaged<CFString>!)](/documentation/coreservices/lsiteminforecord/1448481-init)

##### Instance Properties

- [var creator: OSType](/documentation/coreservices/lsiteminforecord/1441870-creator)
- [var `extension`: Unmanaged<CFString>!](/documentation/coreservices/lsiteminforecord/1442123-extension)
- [var filetype: OSType](/documentation/coreservices/lsiteminforecord/1447384-filetype)
- [var flags: LSItemInfoFlags](/documentation/coreservices/lsiteminforecord/1446281-flags)

#### Deprecated Variables

- [var kLSLaunchHasUntrustedContents: Int](/documentation/coreservices/klslaunchhasuntrustedcontents)
- [var kLSLaunchNoParams: Int](/documentation/coreservices/klslaunchnoparams)
- [var kLSLaunchInhibitBGOnly: Int](/documentation/coreservices/klslaunchinhibitbgonly)
- [var kLSLaunchInClassic: Int](/documentation/coreservices/klslaunchinclassic)
- [var kLSLaunchStartClassic: Int](/documentation/coreservices/klslaunchstartclassic)
- [let kLSItemQuarantineProperties: CFString!](/documentation/coreservices/klsitemquarantineproperties)
- [var kLSSharedFileListFavoriteItems: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistfavoriteitems)
- [var kLSSharedFileListFavoriteVolumes: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistfavoritevolumes)
- [var kLSSharedFileListItemBeforeFirst: Unmanaged<LSSharedFileListItem>](/documentation/coreservices/klssharedfilelistitembeforefirst)
- [var kLSSharedFileListItemHidden: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistitemhidden)
- [var kLSSharedFileListItemLast: Unmanaged<LSSharedFileListItem>](/documentation/coreservices/klssharedfilelistitemlast)
- [var kLSSharedFileListLoginItemHidden: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistloginitemhidden)
- [var kLSSharedFileListRecentApplicationItems: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistrecentapplicationitems)
- [var kLSSharedFileListRecentDocumentItems: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistrecentdocumentitems)
- [var kLSSharedFileListRecentItemsMaxAmount: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistrecentitemsmaxamount)
- [var kLSSharedFileListRecentServerItems: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistrecentserveritems)
- [var kLSSharedFileListSessionLoginItems: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistsessionloginitems)
- [var kLSSharedFileListVolumesComputerVisible: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistvolumescomputervisible)
- [var kLSSharedFileListVolumesNetworkVisible: Unmanaged<CFString>](/documentation/coreservices/klssharedfilelistvolumesnetworkvisible)

#### Deprecated Functions

- [func LSGetHandlerOptionsForContentType(CFString!) -> LSHandlerOptions](/documentation/coreservices/1445296-lsgethandleroptionsforcontenttyp)
- [func LSSetHandlerOptionsForContentType(CFString!, LSHandlerOptions) -> OSStatus](/documentation/coreservices/1447588-lssethandleroptionsforcontenttyp)
- [func LSCopyAllHandlersForURLScheme(CFString) -> Unmanaged<CFArray>?](/documentation/coreservices/1443240-lscopyallhandlersforurlscheme)
- [func LSCopyDefaultHandlerForURLScheme(CFString) -> Unmanaged<CFString>?](/documentation/coreservices/1441725-lscopydefaulthandlerforurlscheme)
- [func LSGetApplicationForItem(UnsafePointer<FSRef>!, LSRolesMask, UnsafeMutablePointer<FSRef>!, UnsafeMutablePointer<Unmanaged<CFURL>?>!) -> OSStatus](/documentation/coreservices/1446185-lsgetapplicationforitem)
- [func LSGetApplicationForURL(CFURL!, LSRolesMask, UnsafeMutablePointer<FSRef>!, UnsafeMutablePointer<Unmanaged<CFURL>?>!) -> OSStatus](/documentation/coreservices/1445210-lsgetapplicationforurl)
- [func LSGetApplicationForInfo(OSType, OSType, CFString!, LSRolesMask, UnsafeMutablePointer<FSRef>!, UnsafeMutablePointer<Unmanaged<CFURL>?>!) -> OSStatus](/documentation/coreservices/1449928-lsgetapplicationforinfo)
- [func LSCopyApplicationForMIMEType(CFString!, LSRolesMask, UnsafeMutablePointer<Unmanaged<CFURL>?>!) -> OSStatus](/documentation/coreservices/1448586-lscopyapplicationformimetype)
- [func LSCanRefAcceptItem(UnsafePointer<FSRef>!, UnsafePointer<FSRef>!, LSRolesMask, LSAcceptanceFlags, UnsafeMutablePointer<DarwinBoolean>!) -> OSStatus](/documentation/coreservices/1442183-lscanrefacceptitem)
- [func LSFindApplicationForInfo(OSType, CFString!, CFString!, UnsafeMutablePointer<FSRef>!, UnsafeMutablePointer<Unmanaged<CFURL>?>!) -> OSStatus](/documentation/coreservices/1449588-lsfindapplicationforinfo)
- [func LSOpenApplication(UnsafePointer<LSApplicationParameters>!, UnsafeMutablePointer<ProcessSerialNumber>!) -> OSStatus](/documentation/coreservices/1447930-lsopenapplication)
- [func LSOpenItemsWithRole(UnsafePointer<FSRef>!, CFIndex, LSRolesMask, UnsafePointer<AEKeyDesc>!, UnsafePointer<LSApplicationParameters>!, UnsafeMutablePointer<ProcessSerialNumber>!, CFIndex) -> OSStatus](/documentation/coreservices/1449783-lsopenitemswithrole)
- [func LSOpenURLsWithRole(CFArray!, LSRolesMask, UnsafePointer<AEKeyDesc>!, UnsafePointer<LSApplicationParameters>!, UnsafeMutablePointer<ProcessSerialNumber>!, CFIndex) -> OSStatus](/documentation/coreservices/1448184-lsopenurlswithrole)
- [func LSOpenFSRef(UnsafePointer<FSRef>!, UnsafeMutablePointer<FSRef>!) -> OSStatus](/documentation/coreservices/1445663-lsopenfsref)
- [func LSOpenFromRefSpec(UnsafePointer<LSLaunchFSRefSpec>!, UnsafeMutablePointer<FSRef>!) -> OSStatus](/documentation/coreservices/1444466-lsopenfromrefspec)
- [func LSCopyItemInfoForRef(UnsafePointer<FSRef>!, LSRequestedInfo, UnsafeMutablePointer<LSItemInfoRecord>!) -> OSStatus](/documentation/coreservices/1445227-lscopyiteminfoforref)
- [func LSCopyItemInfoForURL(CFURL!, LSRequestedInfo, UnsafeMutablePointer<LSItemInfoRecord>!) -> OSStatus](/documentation/coreservices/1445685-lscopyiteminfoforurl)
- [func LSCopyDisplayNameForRef(UnsafePointer<FSRef>!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/coreservices/1442576-lscopydisplaynameforref)
- [func LSCopyDisplayNameForURL(CFURL!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/coreservices/1446850-lscopydisplaynameforurl)
- [func LSCopyKindStringForRef(UnsafePointer<FSRef>!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/coreservices/1448593-lscopykindstringforref)
- [func LSCopyKindStringForURL(CFURL!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/coreservices/1447481-lscopykindstringforurl)
- [func LSCopyKindStringForTypeInfo(OSType, OSType, CFString!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/coreservices/1446207-lscopykindstringfortypeinfo)
- [func LSCopyKindStringForMIMEType(CFString!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> OSStatus](/documentation/coreservices/1442446-lscopykindstringformimetype)
- [func LSCopyItemAttribute(UnsafePointer<FSRef>!, LSRolesMask, CFString!, UnsafeMutablePointer<Unmanaged<CFTypeRef>?>!) -> OSStatus](/documentation/coreservices/1445023-lscopyitemattribute)
- [func LSCopyItemAttributes(UnsafePointer<FSRef>!, LSRolesMask, CFArray!, UnsafeMutablePointer<Unmanaged<CFDictionary>?>!) -> OSStatus](/documentation/coreservices/1446078-lscopyitemattributes)
- [func LSGetExtensionInfo(Int, UnsafePointer<UniChar>!, UnsafeMutablePointer<Int>!) -> OSStatus](/documentation/coreservices/1446043-lsgetextensioninfo)
- [func LSSetExtensionHiddenForRef(UnsafePointer<FSRef>!, Bool) -> OSStatus](/documentation/coreservices/1442766-lssetextensionhiddenforref)
- [func LSSetExtensionHiddenForURL(CFURL!, Bool) -> OSStatus](/documentation/coreservices/1443948-lssetextensionhiddenforurl)
- [func LSRegisterFSRef(UnsafePointer<FSRef>!, Bool) -> OSStatus](/documentation/coreservices/1444582-lsregisterfsref)

#### Deprecated Result Codes

- [var kLSNotInitializedErr: OSStatus](/documentation/coreservices/klsnotinitializederr)
- [var kLSUnknownTypeErr: OSStatus](/documentation/coreservices/klsunknowntypeerr)
- [var kLSDataTooOldErr: OSStatus](/documentation/coreservices/klsdatatooolderr)
- [var kLSNotRegisteredErr: OSStatus](/documentation/coreservices/klsnotregisterederr)
- [var kLSAppDoesNotClaimTypeErr: OSStatus](/documentation/coreservices/klsappdoesnotclaimtypeerr)
- [var kLSAppDoesNotSupportSchemeWarning: OSStatus](/documentation/coreservices/klsappdoesnotsupportschemewarning)
- [var kLSNoRegistrationInfoErr: OSStatus](/documentation/coreservices/klsnoregistrationinfoerr)
- [var kLSNoClassicEnvironmentErr: OSStatus](/documentation/coreservices/klsnoclassicenvironmenterr)
- [File Metadata](/documentation/coreservices/file_metadata)

### Opaque Types

- [MDSchema](/documentation/coreservices/file_metadata/mdschema)

#### MDSchema Miscellaneous Functions

- [func MDSchemaCopyAllAttributes() -> CFArray!](/documentation/coreservices/1445665-mdschemacopyallattributes)
- [func MDSchemaCopyAttributesForContentType(CFString!) -> CFDictionary!](/documentation/coreservices/1444459-mdschemacopyattributesforcontent)
- [func MDSchemaCopyDisplayDescriptionForAttribute(CFString!) -> CFString!](/documentation/coreservices/1442582-mdschemacopydisplaydescriptionfo)
- [func MDSchemaCopyDisplayNameForAttribute(CFString!) -> CFString!](/documentation/coreservices/1450203-mdschemacopydisplaynameforattrib)
- [func MDSchemaCopyMetaAttributesForAttribute(CFString!) -> CFDictionary!](/documentation/coreservices/1450052-mdschemacopymetaattributesforatt)

#### Constants

- [Available Metadata Attribute Keys](/documentation/coreservices/file_metadata/mdschema/available_metadata_attribute_keys)

##### Constants

- [let kMDAttributeDisplayValues: CFString!](/documentation/coreservices/kmdattributedisplayvalues)
- [let kMDAttributeAllValues: CFString!](/documentation/coreservices/kmdattributeallvalues)
- [let kMDAttributeReadOnlyValues: CFString!](/documentation/coreservices/kmdattributereadonlyvalues)
- [let kMDExporterAvaliable: CFString!](/documentation/coreservices/kmdexporteravaliable)
- [Metadata Attribute Schema Description Keys](/documentation/coreservices/file_metadata/mdschema/metadata_attribute_schema_description_keys)

##### Constants

- [let kMDAttributeName: CFString!](/documentation/coreservices/kmdattributename)
- [let kMDAttributeType: CFString!](/documentation/coreservices/kmdattributetype)
- [let kMDAttributeMultiValued: CFString!](/documentation/coreservices/kmdattributemultivalued)
- [MDItem](/documentation/coreservices/file_metadata/mditem)

#### Creating an MDItem

- [func MDItemCreate(CFAllocator!, CFString!) -> MDItem!](/documentation/coreservices/1426917-mditemcreate)
- [func MDItemCreateWithURL(CFAllocator!, CFURL!) -> MDItem!](/documentation/coreservices/1427034-mditemcreatewithurl)

#### Getting the Type Identifier

- [func MDItemGetTypeID() -> CFTypeID](/documentation/coreservices/1427168-mditemgettypeid)

#### Retrieving Metadata Attributes 

- [func MDItemCopyAttribute(MDItem!, CFString!) -> CFTypeRef!](/documentation/coreservices/1427080-mditemcopyattribute)
- [func MDItemCopyAttributes(MDItem!, CFArray!) -> CFDictionary!](/documentation/coreservices/1426980-mditemcopyattributes)
- [func MDItemCopyAttributeNames(MDItem!) -> CFArray!](/documentation/coreservices/1427066-mditemcopyattributenames)

#### Data Types

- [MDItem](/documentation/coreservices/mditem)

#### Constants

- [Common Metadata Attribute Keys](/documentation/coreservices/file_metadata/mditem/common_metadata_attribute_keys)

##### Constants

- [let kMDItemAttributeChangeDate: CFString!](/documentation/coreservices/kmditemattributechangedate)
- [let kMDItemAudiences: CFString!](/documentation/coreservices/kmditemaudiences)
- [let kMDItemAuthors: CFString!](/documentation/coreservices/kmditemauthors)
- [let kMDItemAuthorAddresses: CFString!](/documentation/coreservices/kmditemauthoraddresses)
- [let kMDItemCity: CFString!](/documentation/coreservices/kmditemcity)
- [let kMDItemComment: CFString!](/documentation/coreservices/kmditemcomment)
- [let kMDItemContactKeywords: CFString!](/documentation/coreservices/kmditemcontactkeywords)
- [let kMDItemContentCreationDate: CFString!](/documentation/coreservices/kmditemcontentcreationdate)
- [let kMDItemContentModificationDate: CFString!](/documentation/coreservices/kmditemcontentmodificationdate)
- [let kMDItemContentType: CFString!](/documentation/coreservices/kmditemcontenttype)
- [let kMDItemContributors: CFString!](/documentation/coreservices/kmditemcontributors)
- [let kMDItemCopyright: CFString!](/documentation/coreservices/kmditemcopyright)
- [let kMDItemCountry: CFString!](/documentation/coreservices/kmditemcountry)
- [let kMDItemCoverage: CFString!](/documentation/coreservices/kmditemcoverage)
- [let kMDItemCreator: CFString!](/documentation/coreservices/kmditemcreator)
- [let kMDItemDescription: CFString!](/documentation/coreservices/kmditemdescription)
- [let kMDItemDueDate: CFString!](/documentation/coreservices/kmditemduedate)
- [let kMDItemDurationSeconds: CFString!](/documentation/coreservices/kmditemdurationseconds)
- [let kMDItemEmailAddresses: CFString!](/documentation/coreservices/kmditememailaddresses)
- [let kMDItemEncodingApplications: CFString!](/documentation/coreservices/kmditemencodingapplications)
- [let kMDItemFinderComment: CFString!](/documentation/coreservices/kmditemfindercomment)
- [let kMDItemFonts: CFString!](/documentation/coreservices/kmditemfonts)
- [let kMDItemHeadline: CFString!](/documentation/coreservices/kmditemheadline)
- [let kMDItemIdentifier: CFString!](/documentation/coreservices/kmditemidentifier)
- [let kMDItemInstantMessageAddresses: CFString!](/documentation/coreservices/kmditeminstantmessageaddresses)
- [let kMDItemInstructions: CFString!](/documentation/coreservices/kmditeminstructions)
- [let kMDItemKeywords: CFString!](/documentation/coreservices/kmditemkeywords)
- [let kMDItemKind: CFString!](/documentation/coreservices/kmditemkind)
- [let kMDItemLanguages: CFString!](/documentation/coreservices/kmditemlanguages)
- [let kMDItemLastUsedDate: CFString!](/documentation/coreservices/kmditemlastuseddate)
- [let kMDItemNumberOfPages: CFString!](/documentation/coreservices/kmditemnumberofpages)
- [let kMDItemOrganizations: CFString!](/documentation/coreservices/kmditemorganizations)
- [let kMDItemPageHeight: CFString!](/documentation/coreservices/kmditempageheight)
- [let kMDItemPageWidth: CFString!](/documentation/coreservices/kmditempagewidth)
- [let kMDItemParticipants: CFString!](/documentation/coreservices/kmditemparticipants)
- [let kMDItemPhoneNumbers: CFString!](/documentation/coreservices/kmditemphonenumbers)
- [let kMDItemProjects: CFString!](/documentation/coreservices/kmditemprojects)
- [let kMDItemPublishers: CFString!](/documentation/coreservices/kmditempublishers)
- [let kMDItemRecipients: CFString!](/documentation/coreservices/kmditemrecipients)
- [let kMDItemRecipientAddresses: CFString!](/documentation/coreservices/kmditemrecipientaddresses)
- [let kMDItemRights: CFString!](/documentation/coreservices/kmditemrights)
- [let kMDItemSecurityMethod: CFString!](/documentation/coreservices/kmditemsecuritymethod)
- [let kMDItemStarRating: CFString!](/documentation/coreservices/kmditemstarrating)
- [let kMDItemStateOrProvince: CFString!](/documentation/coreservices/kmditemstateorprovince)
- [let kMDItemTextContent: CFString!](/documentation/coreservices/kmditemtextcontent)
- [let kMDItemTitle: CFString!](/documentation/coreservices/kmditemtitle)
- [let kMDItemVersion: CFString!](/documentation/coreservices/kmditemversion)
- [let kMDItemWhereFroms: CFString!](/documentation/coreservices/kmditemwherefroms)
- [let kMDItemAuthorEmailAddresses: CFString!](/documentation/coreservices/kmditemauthoremailaddresses)
- [let kMDItemRecipientEmailAddresses: CFString!](/documentation/coreservices/kmditemrecipientemailaddresses)
- [let kMDItemTheme: CFString!](/documentation/coreservices/kmditemtheme)
- [let kMDItemSubject: CFString!](/documentation/coreservices/kmditemsubject)
- [let kMDItemCFBundleIdentifier: CFString!](/documentation/coreservices/kmditemcfbundleidentifier)
- [let kMDItemFSHasCustomIcon: CFString!](/documentation/coreservices/kmditemfshascustomicon)
- [let kMDItemFSIsStationery: CFString!](/documentation/coreservices/kmditemfsisstationery)
- [let kMDItemInformation: CFString!](/documentation/coreservices/kmditeminformation)
- [let kMDItemURL: CFString!](/documentation/coreservices/kmditemurl)
- [Image Metadata Attribute Keys](/documentation/coreservices/file_metadata/mditem/image_metadata_attribute_keys)

##### Constants

- [let kMDItemPixelHeight: CFString!](/documentation/coreservices/kmditempixelheight)
- [let kMDItemPixelWidth: CFString!](/documentation/coreservices/kmditempixelwidth)
- [let kMDItemPixelCount: CFString!](/documentation/coreservices/kmditempixelcount)
- [let kMDItemColorSpace: CFString!](/documentation/coreservices/kmditemcolorspace)
- [let kMDItemBitsPerSample: CFString!](/documentation/coreservices/kmditembitspersample)
- [let kMDItemFlashOnOff: CFString!](/documentation/coreservices/kmditemflashonoff)
- [let kMDItemFocalLength: CFString!](/documentation/coreservices/kmditemfocallength)
- [let kMDItemAcquisitionMake: CFString!](/documentation/coreservices/kmditemacquisitionmake)
- [let kMDItemAcquisitionModel: CFString!](/documentation/coreservices/kmditemacquisitionmodel)
- [let kMDItemISOSpeed: CFString!](/documentation/coreservices/kmditemisospeed)
- [let kMDItemOrientation: CFString!](/documentation/coreservices/kmditemorientation)
- [let kMDItemLayerNames: CFString!](/documentation/coreservices/kmditemlayernames)
- [let kMDItemWhiteBalance: CFString!](/documentation/coreservices/kmditemwhitebalance)
- [let kMDItemAperture: CFString!](/documentation/coreservices/kmditemaperture)
- [let kMDItemProfileName: CFString!](/documentation/coreservices/kmditemprofilename)
- [let kMDItemResolutionWidthDPI: CFString!](/documentation/coreservices/kmditemresolutionwidthdpi)
- [let kMDItemResolutionHeightDPI: CFString!](/documentation/coreservices/kmditemresolutionheightdpi)
- [let kMDItemExposureMode: CFString!](/documentation/coreservices/kmditemexposuremode)
- [let kMDItemExposureTimeSeconds: CFString!](/documentation/coreservices/kmditemexposuretimeseconds)
- [let kMDItemEXIFVersion: CFString!](/documentation/coreservices/kmditemexifversion)
- [let kMDItemAlbum: CFString!](/documentation/coreservices/kmditemalbum)
- [let kMDItemHasAlphaChannel: CFString!](/documentation/coreservices/kmditemhasalphachannel)
- [let kMDItemRedEyeOnOff: CFString!](/documentation/coreservices/kmditemredeyeonoff)
- [let kMDItemMeteringMode: CFString!](/documentation/coreservices/kmditemmeteringmode)
- [let kMDItemMaxAperture: CFString!](/documentation/coreservices/kmditemmaxaperture)
- [let kMDItemFNumber: CFString!](/documentation/coreservices/kmditemfnumber)
- [let kMDItemExposureProgram: CFString!](/documentation/coreservices/kmditemexposureprogram)
- [let kMDItemExposureTimeString: CFString!](/documentation/coreservices/kmditemexposuretimestring)
- [let kMDItemEXIFGPSVersion: CFString!](/documentation/coreservices/kmditemexifgpsversion)
- [let kMDItemAltitude: CFString!](/documentation/coreservices/kmditemaltitude)
- [let kMDItemLatitude: CFString!](/documentation/coreservices/kmditemlatitude)
- [let kMDItemLongitude: CFString!](/documentation/coreservices/kmditemlongitude)
- [let kMDItemTimestamp: CFString!](/documentation/coreservices/kmditemtimestamp)
- [let kMDItemSpeed: CFString!](/documentation/coreservices/kmditemspeed)
- [let kMDItemGPSTrack: CFString!](/documentation/coreservices/kmditemgpstrack)
- [let kMDItemImageDirection: CFString!](/documentation/coreservices/kmditemimagedirection)
- [let kMDItemNamedLocation: CFString!](/documentation/coreservices/kmditemnamedlocation)
- [Video Metadata Attribute Keys](/documentation/coreservices/file_metadata/mditem/video_metadata_attribute_keys)

##### Constants

- [let kMDItemAudioBitRate: CFString!](/documentation/coreservices/kmditemaudiobitrate)
- [let kMDItemCodecs: CFString!](/documentation/coreservices/kmditemcodecs)
- [let kMDItemDeliveryType: CFString!](/documentation/coreservices/kmditemdeliverytype)
- [let kMDItemMediaTypes: CFString!](/documentation/coreservices/kmditemmediatypes)
- [let kMDItemStreamable: CFString!](/documentation/coreservices/kmditemstreamable)
- [let kMDItemTotalBitRate: CFString!](/documentation/coreservices/kmditemtotalbitrate)
- [let kMDItemVideoBitRate: CFString!](/documentation/coreservices/kmditemvideobitrate)
- [let kMDItemDirector: CFString!](/documentation/coreservices/kmditemdirector)
- [let kMDItemProducer: CFString!](/documentation/coreservices/kmditemproducer)
- [let kMDItemGenre: CFString!](/documentation/coreservices/kmditemgenre)
- [let kMDItemPerformers: CFString!](/documentation/coreservices/kmditemperformers)
- [let kMDItemOriginalFormat: CFString!](/documentation/coreservices/kmditemoriginalformat)
- [let kMDItemOriginalSource: CFString!](/documentation/coreservices/kmditemoriginalsource)
- [Audio Metadata Attribute Keys](/documentation/coreservices/file_metadata/mditem/audio_metadata_attribute_keys)

##### Constants

- [let kMDItemAppleLoopDescriptors: CFString!](/documentation/coreservices/kmditemappleloopdescriptors)
- [let kMDItemAppleLoopsKeyFilterType: CFString!](/documentation/coreservices/kmditemappleloopskeyfiltertype)
- [let kMDItemAppleLoopsLoopMode: CFString!](/documentation/coreservices/kmditemappleloopsloopmode)
- [let kMDItemAppleLoopsRootKey: CFString!](/documentation/coreservices/kmditemappleloopsrootkey)
- [let kMDItemAudioChannelCount: CFString!](/documentation/coreservices/kmditemaudiochannelcount)
- [let kMDItemAudioEncodingApplication: CFString!](/documentation/coreservices/kmditemaudioencodingapplication)
- [let kMDItemAudioSampleRate: CFString!](/documentation/coreservices/kmditemaudiosamplerate)
- [let kMDItemAudioTrackNumber: CFString!](/documentation/coreservices/kmditemaudiotracknumber)
- [let kMDItemComposer: CFString!](/documentation/coreservices/kmditemcomposer)
- [let kMDItemIsGeneralMIDISequence: CFString!](/documentation/coreservices/kmditemisgeneralmidisequence)
- [let kMDItemKeySignature: CFString!](/documentation/coreservices/kmditemkeysignature)
- [let kMDItemLyricist: CFString!](/documentation/coreservices/kmditemlyricist)
- [let kMDItemMusicalGenre: CFString!](/documentation/coreservices/kmditemmusicalgenre)
- [let kMDItemMusicalInstrumentCategory: CFString!](/documentation/coreservices/kmditemmusicalinstrumentcategory)
- [let kMDItemMusicalInstrumentName: CFString!](/documentation/coreservices/kmditemmusicalinstrumentname)
- [let kMDItemRecordingDate: CFString!](/documentation/coreservices/kmditemrecordingdate)
- [let kMDItemRecordingYear: CFString!](/documentation/coreservices/kmditemrecordingyear)
- [let kMDItemTempo: CFString!](/documentation/coreservices/kmditemtempo)
- [let kMDItemTimeSignature: CFString!](/documentation/coreservices/kmditemtimesignature)
- [File System Metadata Attribute Keys](/documentation/coreservices/file_metadata/mditem/file_system_metadata_attribute_keys)

##### Constants

- [let kMDItemDisplayName: CFString!](/documentation/coreservices/kmditemdisplayname)
- [let kMDItemFSContentChangeDate: CFString!](/documentation/coreservices/kmditemfscontentchangedate)
- [let kMDItemFSCreationDate: CFString!](/documentation/coreservices/kmditemfscreationdate)
- [let kMDItemFSInvisible: CFString!](/documentation/coreservices/kmditemfsinvisible)
- [let kMDItemFSIsExtensionHidden: CFString!](/documentation/coreservices/kmditemfsisextensionhidden)
- [let kMDItemFSLabel: CFString!](/documentation/coreservices/kmditemfslabel)
- [let kMDItemFSName: CFString!](/documentation/coreservices/kmditemfsname)
- [let kMDItemFSNodeCount: CFString!](/documentation/coreservices/kmditemfsnodecount)
- [let kMDItemFSOwnerGroupID: CFString!](/documentation/coreservices/kmditemfsownergroupid)
- [let kMDItemFSOwnerUserID: CFString!](/documentation/coreservices/kmditemfsowneruserid)
- [let kMDItemFSSize: CFString!](/documentation/coreservices/kmditemfssize)
- [let kMDItemPath: CFString!](/documentation/coreservices/kmditempath)

### Structures

- [MDExporterInterfaceStruct](/documentation/coreservices/mdexporterinterfacestruct)

#### Initializers

- [init()](/documentation/coreservices/mdexporterinterfacestruct/1446815-init)
- [init(_reserved: UnsafeMutableRawPointer!, QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!, AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!, Release: ((UnsafeMutableRawPointer?) -> ULONG)!, ImporterExportData: ((UnsafeMutableRawPointer?, CFDictionary?, CFString?, CFString?) -> DarwinBoolean)!)](/documentation/coreservices/mdexporterinterfacestruct/1792091-init)

#### Instance Properties

- [var AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdexporterinterfacestruct/1449918-addref)
- [var ImporterExportData: ((UnsafeMutableRawPointer?, CFDictionary?, CFString?, CFString?) -> DarwinBoolean)!](/documentation/coreservices/mdexporterinterfacestruct/1446348-importerexportdata)
- [var QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!](/documentation/coreservices/mdexporterinterfacestruct/1450043-queryinterface)
- [var Release: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdexporterinterfacestruct/1448271-release)
- [MDImporterBundleWrapperURLInterfaceStruct](/documentation/coreservices/mdimporterbundlewrapperurlinterfacestruct)

#### Initializers

- [init()](/documentation/coreservices/mdimporterbundlewrapperurlinterfacestruct/1449064-init)
- [init(_reserved: UnsafeMutableRawPointer!, QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!, AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!, Release: ((UnsafeMutableRawPointer?) -> ULONG)!, ImporterImportBundleWrapperURLData: ((UnsafeMutableRawPointer?, CFMutableDictionary?, CFString?, CFURL?) -> DarwinBoolean)!)](/documentation/coreservices/mdimporterbundlewrapperurlinterfacestruct/1792098-init)

#### Instance Properties

- [var AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdimporterbundlewrapperurlinterfacestruct/1442108-addref)
- [var ImporterImportBundleWrapperURLData: ((UnsafeMutableRawPointer?, CFMutableDictionary?, CFString?, CFURL?) -> DarwinBoolean)!](/documentation/coreservices/mdimporterbundlewrapperurlinterfacestruct/1443517-importerimportbundlewrapperurlda)
- [var QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!](/documentation/coreservices/mdimporterbundlewrapperurlinterfacestruct/1445643-queryinterface)
- [var Release: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdimporterbundlewrapperurlinterfacestruct/1450356-release)
- [MDImporterInterfaceStruct](/documentation/coreservices/mdimporterinterfacestruct)

#### Initializers

- [init()](/documentation/coreservices/mdimporterinterfacestruct/1443848-init)
- [init(_reserved: UnsafeMutableRawPointer!, QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!, AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!, Release: ((UnsafeMutableRawPointer?) -> ULONG)!, ImporterImportData: ((UnsafeMutableRawPointer?, CFMutableDictionary?, CFString?, CFString?) -> DarwinBoolean)!)](/documentation/coreservices/mdimporterinterfacestruct/1792094-init)

#### Instance Properties

- [var AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdimporterinterfacestruct/1443912-addref)
- [var ImporterImportData: ((UnsafeMutableRawPointer?, CFMutableDictionary?, CFString?, CFString?) -> DarwinBoolean)!](/documentation/coreservices/mdimporterinterfacestruct/1444710-importerimportdata)
- [var QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!](/documentation/coreservices/mdimporterinterfacestruct/1446572-queryinterface)
- [var Release: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdimporterinterfacestruct/1441880-release)
- [MDImporterURLInterfaceStruct](/documentation/coreservices/mdimporterurlinterfacestruct)

#### Initializers

- [init()](/documentation/coreservices/mdimporterurlinterfacestruct/1441965-init)
- [init(_reserved: UnsafeMutableRawPointer!, QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!, AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!, Release: ((UnsafeMutableRawPointer?) -> ULONG)!, ImporterImportURLData: ((UnsafeMutableRawPointer?, CFMutableDictionary?, CFString?, CFURL?) -> DarwinBoolean)!)](/documentation/coreservices/mdimporterurlinterfacestruct/1792096-init)

#### Instance Properties

- [var AddRef: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdimporterurlinterfacestruct/1448177-addref)
- [var ImporterImportURLData: ((UnsafeMutableRawPointer?, CFMutableDictionary?, CFString?, CFURL?) -> DarwinBoolean)!](/documentation/coreservices/mdimporterurlinterfacestruct/1447378-importerimporturldata)
- [var QueryInterface: ((UnsafeMutableRawPointer?, REFIID, UnsafeMutablePointer<LPVOID?>?) -> HRESULT)!](/documentation/coreservices/mdimporterurlinterfacestruct/1442296-queryinterface)
- [var Release: ((UnsafeMutableRawPointer?) -> ULONG)!](/documentation/coreservices/mdimporterurlinterfacestruct/1450015-release)
- [MDLabelDomain](/documentation/coreservices/mdlabeldomain)

#### Initializers

- [init(UInt32)](/documentation/coreservices/mdlabeldomain/1444429-init)
- [init(rawValue: UInt32)](/documentation/coreservices/mdlabeldomain/1445483-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/coreservices/mdlabeldomain/1447882-rawvalue)
- [MDQuerySortOptionFlags](/documentation/coreservices/mdquerysortoptionflags)

#### Initializers

- [init(UInt32)](/documentation/coreservices/mdquerysortoptionflags/1446465-init)
- [init(rawValue: UInt32)](/documentation/coreservices/mdquerysortoptionflags/1442455-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/coreservices/mdquerysortoptionflags/1442589-rawvalue)

### Classes

- [MDLabel](/documentation/coreservices/mdlabel)

### Data Types

- [MDQuery](/documentation/coreservices/file_metadata/mdquery)

#### Creating Queries

- [func MDQueryCreate(CFAllocator!, CFString!, CFArray!, CFArray!) -> MDQuery!](/documentation/coreservices/1413029-mdquerycreate)
- [func MDQueryCreateSubset(CFAllocator!, MDQuery!, CFString!, CFArray!, CFArray!) -> MDQuery!](/documentation/coreservices/1413027-mdquerycreatesubset)
- [func MDQuerySetSearchScope(MDQuery!, CFArray!, OptionBits)](/documentation/coreservices/1413048-mdquerysetsearchscope)
- [func MDQuerySetDispatchQueue(MDQuery!, dispatch_queue_t!)](/documentation/coreservices/1413019-mdquerysetdispatchqueue)

#### Getting and Setting Query Parameters

- [func MDQuerySetMaxCount(MDQuery!, CFIndex)](/documentation/coreservices/1413085-mdquerysetmaxcount)
- [func MDQueryGetBatchingParameters(MDQuery!) -> MDQueryBatchingParams](/documentation/coreservices/1413006-mdquerygetbatchingparameters)
- [func MDQuerySetBatchingParameters(MDQuery!, MDQueryBatchingParams)](/documentation/coreservices/1413103-mdquerysetbatchingparameters)
- [func MDQueryCopyValueListAttributes(MDQuery!) -> CFArray!](/documentation/coreservices/1413071-mdquerycopyvaluelistattributes)
- [func MDQueryCopySortingAttributes(MDQuery!) -> CFArray!](/documentation/coreservices/1413059-mdquerycopysortingattributes)
- [func MDQueryCopyQueryString(MDQuery!) -> CFString!](/documentation/coreservices/1413004-mdquerycopyquerystring)

#### Setting Callback Functions

- [func MDQuerySetCreateResultFunction(MDQuery!, MDQueryCreateResultFunction!, UnsafeMutableRawPointer!, UnsafePointer<CFArrayCallBacks>!)](/documentation/coreservices/1413064-mdquerysetcreateresultfunction)
- [func MDQuerySetSortComparator(MDQuery!, MDQuerySortComparatorFunction!, UnsafeMutableRawPointer!)](/documentation/coreservices/1413087-mdquerysetsortcomparator)
- [func MDQuerySetCreateValueFunction(MDQuery!, MDQueryCreateValueFunction!, UnsafeMutableRawPointer!, UnsafePointer<CFArrayCallBacks>!)](/documentation/coreservices/1413017-mdquerysetcreatevaluefunction)

#### Starting, Stopping and Pausing Queries

- [func MDQueryExecute(MDQuery!, CFOptionFlags) -> Bool](/documentation/coreservices/1413099-mdqueryexecute)
- [func MDQueryStop(MDQuery!)](/documentation/coreservices/1413077-mdquerystop)
- [func MDQueryDisableUpdates(MDQuery!)](/documentation/coreservices/1413041-mdquerydisableupdates)
- [func MDQueryEnableUpdates(MDQuery!)](/documentation/coreservices/1413066-mdqueryenableupdates)
- [func MDQueryIsGatheringComplete(MDQuery!) -> Bool](/documentation/coreservices/1413032-mdqueryisgatheringcomplete)

#### Getting Query Result Values

- [func MDQueryCopyValuesOfAttribute(MDQuery!, CFString!) -> CFArray!](/documentation/coreservices/1413105-mdquerycopyvaluesofattribute)
- [func MDQueryGetAttributeValueOfResultAtIndex(MDQuery!, CFString!, CFIndex) -> UnsafeMutableRawPointer!](/documentation/coreservices/1413046-mdquerygetattributevalueofresult)
- [func MDQueryGetCountOfResultsWithAttributeValue(MDQuery!, CFString!, CFTypeRef!) -> CFIndex](/documentation/coreservices/1413009-mdquerygetcountofresultswithattr)
- [func MDQueryGetIndexOfResult(MDQuery!, UnsafeRawPointer!) -> CFIndex](/documentation/coreservices/1413093-mdquerygetindexofresult)
- [func MDQueryGetResultAtIndex(MDQuery!, CFIndex) -> UnsafeRawPointer!](/documentation/coreservices/1413055-mdquerygetresultatindex)
- [func MDQueryGetResultCount(MDQuery!) -> CFIndex](/documentation/coreservices/1413008-mdquerygetresultcount)
- [func MDQuerySetSortComparatorBlock(MDQuery!, ((UnsafePointer<Unmanaged<CFTypeRef>?>?, UnsafePointer<Unmanaged<CFTypeRef>?>?) -> CFComparisonResult)!)](/documentation/coreservices/1413021-mdquerysetsortcomparatorblock)

#### Getting the Type Identifier

- [func MDQueryGetTypeID() -> CFTypeID](/documentation/coreservices/1413037-mdquerygettypeid)

#### Callbacks

- [MDQuerySortComparatorFunction](/documentation/coreservices/mdquerysortcomparatorfunction)
- [MDQueryCreateResultFunction](/documentation/coreservices/mdquerycreateresultfunction)
- [MDQueryCreateValueFunction](/documentation/coreservices/mdquerycreatevaluefunction)

#### Batching Parameters

- [MDQueryBatchingParams](/documentation/coreservices/mdquerybatchingparams)

##### Initializers

- [init()](/documentation/coreservices/mdquerybatchingparams/1447614-init)
- [init(first_max_num: Int, first_max_ms: Int, progress_max_num: Int, progress_max_ms: Int, update_max_num: Int, update_max_ms: Int)](/documentation/coreservices/mdquerybatchingparams/1443087-init)

##### Instance Properties

- [var first_max_ms: Int](/documentation/coreservices/mdquerybatchingparams/1413073-first_max_ms)
- [var first_max_num: Int](/documentation/coreservices/mdquerybatchingparams/1413089-first_max_num)
- [var progress_max_ms: Int](/documentation/coreservices/mdquerybatchingparams/1413043-progress_max_ms)
- [var progress_max_num: Int](/documentation/coreservices/mdquerybatchingparams/1413036-progress_max_num)
- [var update_max_ms: Int](/documentation/coreservices/mdquerybatchingparams/1413034-update_max_ms)
- [var update_max_num: Int](/documentation/coreservices/mdquerybatchingparams/1413068-update_max_num)

#### Miscellaneous

- [MDQuery](/documentation/coreservices/mdquery)

#### Query Option Flags

- [MDQueryOptionFlags](/documentation/coreservices/mdqueryoptionflags)

##### Constants

- [var kMDQuerySynchronous: MDQueryOptionFlags](/documentation/coreservices/kmdquerysynchronous)
- [var kMDQueryWantsUpdates: MDQueryOptionFlags](/documentation/coreservices/kmdquerywantsupdates)
- [var kMDQueryAllowFSTranslation: MDQueryOptionFlags](/documentation/coreservices/kmdqueryallowfstranslation)

##### Initializers

- [init(UInt32)](/documentation/coreservices/mdqueryoptionflags/1443626-init)
- [init(rawValue: UInt32)](/documentation/coreservices/mdqueryoptionflags/1444315-init)

##### Instance Properties

- [var rawValue: UInt32](/documentation/coreservices/mdqueryoptionflags/1448284-rawvalue)

#### Notifications

- [kMDQueryDidFinishNotification](/documentation/coreservices/file_metadata/mdquery/kmdquerydidfinishnotification)

##### Constants

- [let kMDQueryDidFinishNotification: CFString!](/documentation/coreservices/kmdquerydidfinishnotification)
- [kMDQueryDidUpdateNotification](/documentation/coreservices/file_metadata/mdquery/kmdquerydidupdatenotification)

##### Constants

- [let kMDQueryDidUpdateNotification: CFString!](/documentation/coreservices/kmdquerydidupdatenotification)
- [kMDQueryProgressNotification](/documentation/coreservices/file_metadata/mdquery/kmdqueryprogressnotification)

##### Constants

- [let kMDQueryProgressNotification: CFString!](/documentation/coreservices/kmdqueryprogressnotification)

#### Notification Info Keys

- [Query Result Change Keys](/documentation/coreservices/file_metadata/mdquery/query_result_change_keys)

##### Constants

- [let kMDQueryUpdateAddedItems: CFString!](/documentation/coreservices/kmdqueryupdateaddeditems)
- [let kMDQueryUpdateChangedItems: CFString!](/documentation/coreservices/kmdqueryupdatechangeditems)
- [let kMDQueryUpdateRemovedItems: CFString!](/documentation/coreservices/kmdqueryupdateremoveditems)
- [Query Search Scope Keys](/documentation/coreservices/file_metadata/mdquery/query_search_scope_keys)

##### Constants

- [let kMDQueryScopeHome: CFString!](/documentation/coreservices/kmdqueryscopehome)
- [let kMDQueryScopeComputer: CFString!](/documentation/coreservices/kmdqueryscopecomputer)
- [let kMDQueryScopeNetwork: CFString!](/documentation/coreservices/kmdqueryscopenetwork)
- [let kMDQueryScopeAllIndexed: CFString!](/documentation/coreservices/kmdqueryscopeallindexed)
- [let kMDQueryScopeComputerIndexed: CFString!](/documentation/coreservices/kmdqueryscopecomputerindexed)
- [let kMDQueryScopeNetworkIndexed: CFString!](/documentation/coreservices/kmdqueryscopenetworkindexed)
- [Result Relevance Sorting Key](/documentation/coreservices/file_metadata/mdquery/result_relevance_sorting_key)

##### Constants

- [let kMDQueryResultContentRelevance: CFString!](/documentation/coreservices/kmdqueryresultcontentrelevance)

### Constants

- [let kMDItemApplicationCategories: CFString!](/documentation/coreservices/kmditemapplicationcategories)
- [let kMDItemCameraOwner: CFString!](/documentation/coreservices/kmditemcameraowner)
- [let kMDItemContentTypeTree: CFString!](/documentation/coreservices/kmditemcontenttypetree)
- [let kMDItemDateAdded: CFString!](/documentation/coreservices/kmditemdateadded)
- [let kMDItemDownloadedDate: CFString!](/documentation/coreservices/kmditemdownloadeddate)
- [let kMDItemEditors: CFString!](/documentation/coreservices/kmditemeditors)
- [let kMDItemExecutableArchitectures: CFString!](/documentation/coreservices/kmditemexecutablearchitectures)
- [let kMDItemExecutablePlatform: CFString!](/documentation/coreservices/kmditemexecutableplatform)
- [let kMDItemFocalLength35mm: CFString!](/documentation/coreservices/kmditemfocallength35mm)
- [let kMDItemGPSAreaInformation: CFString!](/documentation/coreservices/kmditemgpsareainformation)
- [let kMDItemGPSDOP: CFString!](/documentation/coreservices/kmditemgpsdop)
- [let kMDItemGPSDateStamp: CFString!](/documentation/coreservices/kmditemgpsdatestamp)
- [let kMDItemGPSDestBearing: CFString!](/documentation/coreservices/kmditemgpsdestbearing)
- [let kMDItemGPSDestDistance: CFString!](/documentation/coreservices/kmditemgpsdestdistance)
- [let kMDItemGPSDestLatitude: CFString!](/documentation/coreservices/kmditemgpsdestlatitude)
- [let kMDItemGPSDestLongitude: CFString!](/documentation/coreservices/kmditemgpsdestlongitude)
- [let kMDItemGPSDifferental: CFString!](/documentation/coreservices/kmditemgpsdifferental)
- [let kMDItemGPSMapDatum: CFString!](/documentation/coreservices/kmditemgpsmapdatum)
- [let kMDItemGPSMeasureMode: CFString!](/documentation/coreservices/kmditemgpsmeasuremode)
- [let kMDItemGPSProcessingMethod: CFString!](/documentation/coreservices/kmditemgpsprocessingmethod)
- [let kMDItemGPSStatus: CFString!](/documentation/coreservices/kmditemgpsstatus)
- [let kMDItemHTMLContent: CFString!](/documentation/coreservices/kmditemhtmlcontent)
- [let kMDItemIsApplicationManaged: CFString!](/documentation/coreservices/kmditemisapplicationmanaged)
- [let kMDItemIsLikelyJunk: CFString!](/documentation/coreservices/kmditemislikelyjunk)
- [let kMDItemLensModel: CFString!](/documentation/coreservices/kmditemlensmodel)
- [let kMDLabelAddedNotification: CFString!](/documentation/coreservices/kmdlabeladdednotification)
- [var kMDLabelBundleURL: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelbundleurl)
- [let kMDLabelChangedNotification: CFString!](/documentation/coreservices/kmdlabelchangednotification)
- [var kMDLabelContentChangeDate: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelcontentchangedate)
- [var kMDLabelDisplayName: Unmanaged<CFString>!](/documentation/coreservices/kmdlabeldisplayname)
- [var kMDLabelIconData: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelicondata)
- [var kMDLabelIconUUID: Unmanaged<CFString>!](/documentation/coreservices/kmdlabeliconuuid)
- [var kMDLabelIsMutuallyExclusiveSetMember: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelismutuallyexclusivesetmember)
- [var kMDLabelKind: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelkind)
- [var kMDLabelKindIsMutuallyExclusiveSetKey: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelkindismutuallyexclusivesetkey)
- [var kMDLabelKindVisibilityKey: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelkindvisibilitykey)
- [var kMDLabelLocalDomain: MDLabelDomain](/documentation/coreservices/kmdlabellocaldomain)
- [let kMDLabelRemovedNotification: CFString!](/documentation/coreservices/kmdlabelremovednotification)
- [var kMDLabelSetsFinderColor: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelsetsfindercolor)
- [var kMDLabelUUID: Unmanaged<CFString>!](/documentation/coreservices/kmdlabeluuid)
- [var kMDLabelUserDomain: MDLabelDomain](/documentation/coreservices/kmdlabeluserdomain)
- [var kMDLabelVisibility: Unmanaged<CFString>!](/documentation/coreservices/kmdlabelvisibility)
- [var kMDPrivateVisibility: Unmanaged<CFString>!](/documentation/coreservices/kmdprivatevisibility)
- [var kMDPublicVisibility: Unmanaged<CFString>!](/documentation/coreservices/kmdpublicvisibility)
- [var kMDQueryAllowFSTranslation: MDQueryOptionFlags](/documentation/coreservices/kmdqueryallowfstranslation)
- [var kMDQueryReverseSortOrderFlag: MDQuerySortOptionFlags](/documentation/coreservices/kmdqueryreversesortorderflag)
- [var kMDQuerySynchronous: MDQueryOptionFlags](/documentation/coreservices/kmdquerysynchronous)
- [var kMDQueryWantsUpdates: MDQueryOptionFlags](/documentation/coreservices/kmdquerywantsupdates)
- [OS Services](/documentation/coreservices/os_services)

### Reference

- [Identity Services](/documentation/coreservices/os_services/identity_services)

#### Classes

- [CSIdentity](/documentation/coreservices/csidentity)
- [CSIdentityAuthority](/documentation/coreservices/csidentityauthority)
- [CSIdentityQuery](/documentation/coreservices/csidentityquery)

#### Functions

- [func CSDiskSpaceCancelRecovery(CFUUID!)](/documentation/coreservices/1448335-csdiskspacecancelrecovery)
- [func CSDiskSpaceGetRecoveryEstimate(CFURL!) -> UInt64](/documentation/coreservices/1448439-csdiskspacegetrecoveryestimate)
- [func CSDiskSpaceStartRecovery(CFURL!, UInt64, CSDiskSpaceRecoveryOptions, UnsafeMutablePointer<Unmanaged<CFUUID>?>!, dispatch_queue_t!, CSDiskSpaceRecoveryCallback!)](/documentation/coreservices/1447968-csdiskspacestartrecovery)
- [func CSGetDefaultIdentityAuthority() -> Unmanaged<CSIdentityAuthority>!](/documentation/coreservices/1448826-csgetdefaultidentityauthority)
- [func CSGetLocalIdentityAuthority() -> Unmanaged<CSIdentityAuthority>!](/documentation/coreservices/1444814-csgetlocalidentityauthority)
- [func CSGetManagedIdentityAuthority() -> Unmanaged<CSIdentityAuthority>!](/documentation/coreservices/1446750-csgetmanagedidentityauthority)
- [func CSIdentityAddAlias(CSIdentity!, CFString!)](/documentation/coreservices/1443062-csidentityaddalias)
- [func CSIdentityAddMember(CSIdentity!, CSIdentity!)](/documentation/coreservices/1447513-csidentityaddmember)
- [func CSIdentityAuthenticateUsingPassword(CSIdentity!, CFString!) -> Bool](/documentation/coreservices/1449855-csidentityauthenticateusingpassw)
- [func CSIdentityAuthorityCopyLocalizedName(CSIdentityAuthority!) -> Unmanaged<CFString>!](/documentation/coreservices/1448990-csidentityauthoritycopylocalized)
- [func CSIdentityAuthorityGetTypeID() -> CFTypeID](/documentation/coreservices/1449199-csidentityauthoritygettypeid)
- [func CSIdentityCommit(CSIdentity!, AuthorizationRef!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/coreservices/1449575-csidentitycommit)
- [func CSIdentityCommitAsynchronously(CSIdentity!, UnsafePointer<CSIdentityClientContext>!, CFRunLoop!, CFString!, AuthorizationRef!) -> Bool](/documentation/coreservices/1447936-csidentitycommitasynchronously)
- [func CSIdentityCreate(CFAllocator!, CSIdentityClass, CFString!, CFString!, CSIdentityFlags, CSIdentityAuthority!) -> Unmanaged<CSIdentity>!](/documentation/coreservices/1447616-csidentitycreate)
- [func CSIdentityCreateCopy(CFAllocator!, CSIdentity!) -> Unmanaged<CSIdentity>!](/documentation/coreservices/1443553-csidentitycreatecopy)
- [func CSIdentityCreateGroupMembershipQuery(CFAllocator!, CSIdentity!) -> Unmanaged<CSIdentityQuery>!](/documentation/coreservices/1448605-csidentitycreategroupmembershipq)
- [func CSIdentityCreatePersistentReference(CFAllocator!, CSIdentity!) -> Unmanaged<CFData>!](/documentation/coreservices/1444037-csidentitycreatepersistentrefere)
- [func CSIdentityDelete(CSIdentity!)](/documentation/coreservices/1442616-csidentitydelete)
- [func CSIdentityGetAliases(CSIdentity!) -> Unmanaged<CFArray>!](/documentation/coreservices/1446455-csidentitygetaliases)
- [func CSIdentityGetAuthority(CSIdentity!) -> Unmanaged<CSIdentityAuthority>!](/documentation/coreservices/1446828-csidentitygetauthority)
- [func CSIdentityGetCertificate(CSIdentity!) -> Unmanaged<SecCertificate>!](/documentation/coreservices/1448582-csidentitygetcertificate)
- [func CSIdentityGetClass(CSIdentity!) -> CSIdentityClass](/documentation/coreservices/1447194-csidentitygetclass)
- [func CSIdentityGetEmailAddress(CSIdentity!) -> Unmanaged<CFString>!](/documentation/coreservices/1446211-csidentitygetemailaddress)
- [func CSIdentityGetFullName(CSIdentity!) -> Unmanaged<CFString>!](/documentation/coreservices/1447315-csidentitygetfullname)
- [func CSIdentityGetImageData(CSIdentity!) -> Unmanaged<CFData>!](/documentation/coreservices/1444544-csidentitygetimagedata)
- [func CSIdentityGetImageDataType(CSIdentity!) -> Unmanaged<CFString>!](/documentation/coreservices/1447478-csidentitygetimagedatatype)
- [func CSIdentityGetImageURL(CSIdentity!) -> Unmanaged<CFURL>!](/documentation/coreservices/1446099-csidentitygetimageurl)
- [func CSIdentityGetPosixID(CSIdentity!) -> id_t](/documentation/coreservices/1443230-csidentitygetposixid)
- [func CSIdentityGetPosixName(CSIdentity!) -> Unmanaged<CFString>!](/documentation/coreservices/1447210-csidentitygetposixname)
- [func CSIdentityGetTypeID() -> CFTypeID](/documentation/coreservices/1444732-csidentitygettypeid)
- [func CSIdentityGetUUID(CSIdentity!) -> Unmanaged<CFUUID>!](/documentation/coreservices/1447987-csidentitygetuuid)
- [func CSIdentityIsCommitting(CSIdentity!) -> Bool](/documentation/coreservices/1449734-csidentityiscommitting)
- [func CSIdentityIsEnabled(CSIdentity!) -> Bool](/documentation/coreservices/1443379-csidentityisenabled)
- [func CSIdentityIsHidden(CSIdentity!) -> Bool](/documentation/coreservices/1449476-csidentityishidden)
- [func CSIdentityIsMemberOfGroup(CSIdentity!, CSIdentity!) -> Bool](/documentation/coreservices/1449237-csidentityismemberofgroup)
- [func CSIdentityQueryCopyResults(CSIdentityQuery!) -> Unmanaged<CFArray>!](/documentation/coreservices/1429035-csidentityquerycopyresults)
- [func CSIdentityQueryCreate(CFAllocator!, CSIdentityClass, CSIdentityAuthority!) -> Unmanaged<CSIdentityQuery>!](/documentation/coreservices/1429003-csidentityquerycreate)
- [func CSIdentityQueryCreateForCurrentUser(CFAllocator!) -> Unmanaged<CSIdentityQuery>!](/documentation/coreservices/1429037-csidentityquerycreateforcurrentu)
- [func CSIdentityQueryCreateForName(CFAllocator!, CFString!, CSIdentityQueryStringComparisonMethod, CSIdentityClass, CSIdentityAuthority!) -> Unmanaged<CSIdentityQuery>!](/documentation/coreservices/1428997-csidentityquerycreateforname)
- [func CSIdentityQueryCreateForPersistentReference(CFAllocator!, CFData!) -> Unmanaged<CSIdentityQuery>!](/documentation/coreservices/1428991-csidentityquerycreateforpersiste)
- [func CSIdentityQueryCreateForPosixID(CFAllocator!, id_t, CSIdentityClass, CSIdentityAuthority!) -> Unmanaged<CSIdentityQuery>!](/documentation/coreservices/1428990-csidentityquerycreateforposixid)
- [func CSIdentityQueryCreateForUUID(CFAllocator!, CFUUID!, CSIdentityAuthority!) -> Unmanaged<CSIdentityQuery>!](/documentation/coreservices/1429007-csidentityquerycreateforuuid)
- [func CSIdentityQueryExecute(CSIdentityQuery!, CSIdentityQueryFlags, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/coreservices/1429041-csidentityqueryexecute)
- [func CSIdentityQueryExecuteAsynchronously(CSIdentityQuery!, CSIdentityQueryFlags, UnsafePointer<CSIdentityQueryClientContext>!, CFRunLoop!, CFString!) -> Bool](/documentation/coreservices/1429011-csidentityqueryexecuteasynchrono)
- [func CSIdentityQueryGetTypeID() -> CFTypeID](/documentation/coreservices/1429012-csidentityquerygettypeid)
- [func CSIdentityQueryStop(CSIdentityQuery!)](/documentation/coreservices/1429047-csidentityquerystop)
- [func CSIdentityRemoveAlias(CSIdentity!, CFString!)](/documentation/coreservices/1442114-csidentityremovealias)
- [func CSIdentityRemoveClient(CSIdentity!)](/documentation/coreservices/1448933-csidentityremoveclient)
- [func CSIdentityRemoveMember(CSIdentity!, CSIdentity!)](/documentation/coreservices/1448796-csidentityremovemember)
- [func CSIdentitySetCertificate(CSIdentity!, SecCertificate!)](/documentation/coreservices/1447691-csidentitysetcertificate)
- [func CSIdentitySetEmailAddress(CSIdentity!, CFString!)](/documentation/coreservices/1443235-csidentitysetemailaddress)
- [func CSIdentitySetFullName(CSIdentity!, CFString!)](/documentation/coreservices/1446623-csidentitysetfullname)
- [func CSIdentitySetImageData(CSIdentity!, CFData!, CFString!)](/documentation/coreservices/1441866-csidentitysetimagedata)
- [func CSIdentitySetImageURL(CSIdentity!, CFURL!)](/documentation/coreservices/1446717-csidentitysetimageurl)
- [func CSIdentitySetIsEnabled(CSIdentity!, Bool)](/documentation/coreservices/1443028-csidentitysetisenabled)
- [func CSIdentitySetPassword(CSIdentity!, CFString!)](/documentation/coreservices/1443568-csidentitysetpassword)

#### Structures

- [CSIdentityClientContext](/documentation/coreservices/csidentityclientcontext)

##### Initializers

- [init()](/documentation/coreservices/csidentityclientcontext/1448614-init)
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retain: CFAllocatorRetainCallBack!, release: CFAllocatorReleaseCallBack!, copyDescription: CFAllocatorCopyDescriptionCallBack!, statusUpdated: CSIdentityStatusUpdatedCallback!)](/documentation/coreservices/csidentityclientcontext/1792093-init)

##### Instance Properties

- [var copyDescription: CFAllocatorCopyDescriptionCallBack!](/documentation/coreservices/csidentityclientcontext/1445249-copydescription)
- [var info: UnsafeMutableRawPointer!](/documentation/coreservices/csidentityclientcontext/1443727-info)
- [var release: CFAllocatorReleaseCallBack!](/documentation/coreservices/csidentityclientcontext/1448741-release)
- [var retain: CFAllocatorRetainCallBack!](/documentation/coreservices/csidentityclientcontext/1444414-retain)
- [var statusUpdated: CSIdentityStatusUpdatedCallback!](/documentation/coreservices/csidentityclientcontext/1447852-statusupdated)
- [var version: CFIndex](/documentation/coreservices/csidentityclientcontext/1448370-version)
- [CSIdentityQueryClientContext](/documentation/coreservices/csidentityqueryclientcontext)

##### Initializers

- [init()](/documentation/coreservices/csidentityqueryclientcontext/1448054-init)
- [init(version: CFIndex, info: UnsafeMutableRawPointer!, retainInfo: CFAllocatorRetainCallBack!, releaseInfo: CFAllocatorReleaseCallBack!, copyInfoDescription: CFAllocatorCopyDescriptionCallBack!, receiveEvent: CSIdentityQueryReceiveEventCallback!)](/documentation/coreservices/csidentityqueryclientcontext/1792095-init)

##### Instance Properties

- [var copyInfoDescription: CFAllocatorCopyDescriptionCallBack!](/documentation/coreservices/csidentityqueryclientcontext/1428999-copyinfodescription)
- [var info: UnsafeMutableRawPointer!](/documentation/coreservices/csidentityqueryclientcontext/1429018-info)
- [var receiveEvent: CSIdentityQueryReceiveEventCallback!](/documentation/coreservices/csidentityqueryclientcontext/1429030-receiveevent)
- [var releaseInfo: CFAllocatorReleaseCallBack!](/documentation/coreservices/csidentityqueryclientcontext/1429034-releaseinfo)
- [var retainInfo: CFAllocatorRetainCallBack!](/documentation/coreservices/csidentityqueryclientcontext/1429016-retaininfo)
- [var version: CFIndex](/documentation/coreservices/csidentityqueryclientcontext/1429001-version)

#### Constants

- [let kCSIdentityErrorDomain: CFString!](/documentation/coreservices/kcsidentityerrordomain)
- [let kCSIdentityGeneratePosixName: CFString!](/documentation/coreservices/kcsidentitygenerateposixname)
- [Icon Storage](/documentation/coreservices/os_services/icon_storage)

#### Data Types

- [IconRef](/documentation/coreservices/iconref)
- [IconServicesUsageFlags](/documentation/coreservices/iconservicesusageflags)
- [Search Kit](/documentation/coreservices/search_kit)

### Creating, Opening, and Closing Indexes

- [func SKIndexCreateWithURL(CFURL!, CFString!, SKIndexType, CFDictionary!) -> Unmanaged<SKIndex>!](/documentation/coreservices/1446111-skindexcreatewithurl)
- [func SKIndexCreateWithMutableData(CFMutableData!, CFString!, SKIndexType, CFDictionary!) -> Unmanaged<SKIndex>!](/documentation/coreservices/1447500-skindexcreatewithmutabledata)
- [func SKIndexOpenWithData(CFData!, CFString!) -> Unmanaged<SKIndex>!](/documentation/coreservices/1446398-skindexopenwithdata)
- [func SKIndexOpenWithMutableData(CFMutableData!, CFString!) -> Unmanaged<SKIndex>!](/documentation/coreservices/1444201-skindexopenwithmutabledata)
- [func SKIndexOpenWithURL(CFURL!, CFString!, Bool) -> Unmanaged<SKIndex>!](/documentation/coreservices/1449017-skindexopenwithurl)
- [func SKIndexClose(SKIndex!)](/documentation/coreservices/1442401-skindexclose)
- [func SKIndexGetIndexType(SKIndex!) -> SKIndexType](/documentation/coreservices/1442236-skindexgetindextype)
- [func SKIndexGetTypeID() -> CFTypeID](/documentation/coreservices/1450223-skindexgettypeid)

### Managing Indexes

- [func SKIndexAddDocumentWithText(SKIndex!, SKDocument!, CFString!, Bool) -> Bool](/documentation/coreservices/1444518-skindexadddocumentwithtext)
- [func SKIndexAddDocument(SKIndex!, SKDocument!, CFString!, Bool) -> Bool](/documentation/coreservices/1444897-skindexadddocument)
- [func SKIndexFlush(SKIndex!) -> Bool](/documentation/coreservices/1450667-skindexflush)
- [func SKIndexCompact(SKIndex!) -> Bool](/documentation/coreservices/1443628-skindexcompact)
- [func SKIndexGetDocumentCount(SKIndex!) -> CFIndex](/documentation/coreservices/1449093-skindexgetdocumentcount)
- [func SKIndexGetMaximumDocumentID(SKIndex!) -> SKDocumentID](/documentation/coreservices/1444628-skindexgetmaximumdocumentid)
- [func SKIndexGetMaximumTermID(SKIndex!) -> CFIndex](/documentation/coreservices/1444278-skindexgetmaximumtermid)
- [func SKIndexDocumentIteratorCreate(SKIndex!, SKDocument!) -> Unmanaged<SKIndexDocumentIterator>!](/documentation/coreservices/1446189-skindexdocumentiteratorcreate)
- [func SKIndexDocumentIteratorCopyNext(SKIndexDocumentIterator!) -> Unmanaged<SKDocument>!](/documentation/coreservices/1442212-skindexdocumentiteratorcopynext)
- [func SKIndexDocumentIteratorGetTypeID() -> CFTypeID](/documentation/coreservices/1443022-skindexdocumentiteratorgettypeid)
- [func SKIndexGetAnalysisProperties(SKIndex!) -> Unmanaged<CFDictionary>!](/documentation/coreservices/1443461-skindexgetanalysisproperties)
- [func SKIndexMoveDocument(SKIndex!, SKDocument!, SKDocument!) -> Bool](/documentation/coreservices/1449899-skindexmovedocument)
- [func SKIndexRemoveDocument(SKIndex!, SKDocument!) -> Bool](/documentation/coreservices/1444375-skindexremovedocument)
- [func SKIndexRenameDocument(SKIndex!, SKDocument!, CFString!) -> Bool](/documentation/coreservices/1448935-skindexrenamedocument)
- [func SKIndexSetMaximumBytesBeforeFlush(SKIndex!, CFIndex)](/documentation/coreservices/1448696-skindexsetmaximumbytesbeforeflus)
- [func SKIndexGetMaximumBytesBeforeFlush(SKIndex!) -> CFIndex](/documentation/coreservices/1445329-skindexgetmaximumbytesbeforeflus)

### Working With Text Importers

- [func SKLoadDefaultExtractorPlugIns()](/documentation/coreservices/1447859-skloaddefaultextractorplugins)

### Working with Documents and Terms

- [func SKDocumentCreateWithURL(CFURL!) -> Unmanaged<SKDocument>!](/documentation/coreservices/1442564-skdocumentcreatewithurl)
- [func SKDocumentCreate(CFString!, SKDocument!, CFString!) -> Unmanaged<SKDocument>!](/documentation/coreservices/1443212-skdocumentcreate)
- [func SKDocumentCopyURL(SKDocument!) -> Unmanaged<CFURL>!](/documentation/coreservices/1449624-skdocumentcopyurl)
- [func SKDocumentGetName(SKDocument!) -> Unmanaged<CFString>!](/documentation/coreservices/1442657-skdocumentgetname)
- [func SKDocumentGetParent(SKDocument!) -> Unmanaged<SKDocument>!](/documentation/coreservices/1444449-skdocumentgetparent)
- [func SKDocumentGetSchemeName(SKDocument!) -> Unmanaged<CFString>!](/documentation/coreservices/1448262-skdocumentgetschemename)
- [func SKDocumentGetTypeID() -> CFTypeID](/documentation/coreservices/1448891-skdocumentgettypeid)
- [func SKIndexCopyDocumentForDocumentID(SKIndex!, SKDocumentID) -> Unmanaged<SKDocument>!](/documentation/coreservices/1442760-skindexcopydocumentfordocumentid)
- [func SKIndexCopyInfoForDocumentIDs(SKIndex!, CFIndex, UnsafeMutablePointer<SKDocumentID>!, UnsafeMutablePointer<Unmanaged<CFString>?>!, UnsafeMutablePointer<SKDocumentID>!)](/documentation/coreservices/1445499-skindexcopyinfofordocumentids)
- [func SKIndexCopyDocumentRefsForDocumentIDs(SKIndex!, CFIndex, UnsafeMutablePointer<SKDocumentID>!, UnsafeMutablePointer<Unmanaged<SKDocument>?>!)](/documentation/coreservices/1445305-skindexcopydocumentrefsfordocume)
- [func SKIndexCopyDocumentURLsForDocumentIDs(SKIndex!, CFIndex, UnsafeMutablePointer<SKDocumentID>!, UnsafeMutablePointer<Unmanaged<CFURL>?>!)](/documentation/coreservices/1443501-skindexcopydocumenturlsfordocume)
- [func SKIndexCopyDocumentIDArrayForTermID(SKIndex!, CFIndex) -> Unmanaged<CFArray>!](/documentation/coreservices/1448003-skindexcopydocumentidarrayforter)
- [func SKIndexCopyTermIDArrayForDocumentID(SKIndex!, SKDocumentID) -> Unmanaged<CFArray>!](/documentation/coreservices/1446868-skindexcopytermidarrayfordocumen)
- [func SKIndexCopyTermStringForTermID(SKIndex!, CFIndex) -> Unmanaged<CFString>!](/documentation/coreservices/1442802-skindexcopytermstringfortermid)
- [func SKIndexGetTermIDForTermString(SKIndex!, CFString!) -> CFIndex](/documentation/coreservices/1448558-skindexgettermidfortermstring)
- [func SKIndexSetDocumentProperties(SKIndex!, SKDocument!, CFDictionary!)](/documentation/coreservices/1444576-skindexsetdocumentproperties)
- [func SKIndexCopyDocumentProperties(SKIndex!, SKDocument!) -> Unmanaged<CFDictionary>!](/documentation/coreservices/1449500-skindexcopydocumentproperties)
- [func SKIndexGetDocumentState(SKIndex!, SKDocument!) -> SKDocumentIndexState](/documentation/coreservices/1443396-skindexgetdocumentstate)
- [func SKIndexGetDocumentTermCount(SKIndex!, SKDocumentID) -> CFIndex](/documentation/coreservices/1448341-skindexgetdocumenttermcount)
- [func SKIndexGetDocumentTermFrequency(SKIndex!, SKDocumentID, CFIndex) -> CFIndex](/documentation/coreservices/1447537-skindexgetdocumenttermfrequency)
- [func SKIndexGetTermDocumentCount(SKIndex!, CFIndex) -> CFIndex](/documentation/coreservices/1444015-skindexgettermdocumentcount)
- [func SKIndexGetDocumentID(SKIndex!, SKDocument!) -> SKDocumentID](/documentation/coreservices/1444437-skindexgetdocumentid)

### Fast Asynchronous Searching

- [func SKSearchCreate(SKIndex!, CFString!, SKSearchOptions) -> Unmanaged<SKSearch>!](/documentation/coreservices/1443079-sksearchcreate)
- [func SKSearchFindMatches(SKSearch!, CFIndex, UnsafeMutablePointer<SKDocumentID>!, UnsafeMutablePointer<Float>!, CFTimeInterval, UnsafeMutablePointer<CFIndex>!) -> Bool](/documentation/coreservices/1448608-sksearchfindmatches)
- [func SKSearchCancel(SKSearch!)](/documentation/coreservices/1442083-sksearchcancel)
- [func SKSearchGetTypeID() -> CFTypeID](/documentation/coreservices/1448621-sksearchgettypeid)

### Working With Summarization

- [func SKSummaryCreateWithString(CFString!) -> Unmanaged<SKSummary>!](/documentation/coreservices/1446229-sksummarycreatewithstring)
- [func SKSummaryGetSentenceSummaryInfo(SKSummary!, CFIndex, UnsafeMutablePointer<CFIndex>!, UnsafeMutablePointer<CFIndex>!, UnsafeMutablePointer<CFIndex>!) -> CFIndex](/documentation/coreservices/1444767-sksummarygetsentencesummaryinfo)
- [func SKSummaryGetParagraphSummaryInfo(SKSummary!, CFIndex, UnsafeMutablePointer<CFIndex>!, UnsafeMutablePointer<CFIndex>!) -> CFIndex](/documentation/coreservices/1447517-sksummarygetparagraphsummaryinfo)
- [func SKSummaryGetSentenceCount(SKSummary!) -> CFIndex](/documentation/coreservices/1450009-sksummarygetsentencecount)
- [func SKSummaryGetParagraphCount(SKSummary!) -> CFIndex](/documentation/coreservices/1449304-sksummarygetparagraphcount)
- [func SKSummaryCopySentenceAtIndex(SKSummary!, CFIndex) -> Unmanaged<CFString>!](/documentation/coreservices/1450287-sksummarycopysentenceatindex)
- [func SKSummaryCopyParagraphAtIndex(SKSummary!, CFIndex) -> Unmanaged<CFString>!](/documentation/coreservices/1445711-sksummarycopyparagraphatindex)
- [func SKSummaryCopySentenceSummaryString(SKSummary!, CFIndex) -> Unmanaged<CFString>!](/documentation/coreservices/1449700-sksummarycopysentencesummarystri)
- [func SKSummaryCopyParagraphSummaryString(SKSummary!, CFIndex) -> Unmanaged<CFString>!](/documentation/coreservices/1449746-sksummarycopyparagraphsummarystr)
- [func SKSummaryGetTypeID() -> CFTypeID](/documentation/coreservices/1444796-sksummarygettypeid)

### Callbacks

- [SKSearchResultsFilterCallBack](/documentation/coreservices/sksearchresultsfiltercallback)

### Data Types

- [SKDocument](/documentation/coreservices/skdocument)
- [SKIndexDocumentIterator](/documentation/coreservices/skindexdocumentiterator)
- [SKIndex](/documentation/coreservices/skindex)
- [SKSearch](/documentation/coreservices/sksearch)
- [SKSummary](/documentation/coreservices/sksummary)
- [SKDocumentID](/documentation/coreservices/skdocumentid)
- [SKSearchResults](/documentation/coreservices/sksearchresults)
- [SKSearchGroup](/documentation/coreservices/sksearchgroup)

### Constants

- [Text Analysis Keys](/documentation/coreservices/search_kit/text_analysis_keys)

#### Constants

- [let kSKMinTermLength: CFString!](/documentation/coreservices/kskmintermlength)
- [let kSKStopWords: CFString!](/documentation/coreservices/kskstopwords)
- [let kSKSubstitutions: CFString!](/documentation/coreservices/ksksubstitutions)
- [let kSKMaximumTerms: CFString!](/documentation/coreservices/kskmaximumterms)
- [let kSKProximityIndexing: CFString!](/documentation/coreservices/kskproximityindexing)
- [let kSKTermChars: CFString!](/documentation/coreservices/ksktermchars)
- [let kSKStartTermChars: CFString!](/documentation/coreservices/kskstarttermchars)
- [let kSKEndTermChars: CFString!](/documentation/coreservices/kskendtermchars)
- [SKDocumentIndexState](/documentation/coreservices/skdocumentindexstate)

#### Constants

- [var kSKDocumentStateNotIndexed: SKDocumentIndexState](/documentation/coreservices/kskdocumentstatenotindexed)
- [var kSKDocumentStateIndexed: SKDocumentIndexState](/documentation/coreservices/kskdocumentstateindexed)
- [var kSKDocumentStateAddPending: SKDocumentIndexState](/documentation/coreservices/kskdocumentstateaddpending)
- [var kSKDocumentStateDeletePending: SKDocumentIndexState](/documentation/coreservices/kskdocumentstatedeletepending)

#### Initializers

- [init(UInt32)](/documentation/coreservices/skdocumentindexstate/1450037-init)
- [init(rawValue: UInt32)](/documentation/coreservices/skdocumentindexstate/1441863-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/coreservices/skdocumentindexstate/1443351-rawvalue)
- [SKSearchOptions](/documentation/coreservices/sksearchoptions)

#### Constants

- [var kSKSearchOptionDefault: Int](/documentation/coreservices/ksksearchoptiondefault)
- [var kSKSearchOptionNoRelevanceScores: Int](/documentation/coreservices/ksksearchoptionnorelevancescores)
- [var kSKSearchOptionSpaceMeansOR: Int](/documentation/coreservices/ksksearchoptionspacemeansor)
- [var kSKSearchOptionFindSimilar: Int](/documentation/coreservices/ksksearchoptionfindsimilar)
- [SKIndexType](/documentation/coreservices/skindextype)

#### Constants

- [var kSKIndexUnknown: SKIndexType](/documentation/coreservices/kskindexunknown)
- [var kSKIndexInverted: SKIndexType](/documentation/coreservices/kskindexinverted)
- [var kSKIndexVector: SKIndexType](/documentation/coreservices/kskindexvector)
- [var kSKIndexInvertedVector: SKIndexType](/documentation/coreservices/kskindexinvertedvector)

#### Initializers

- [init(UInt32)](/documentation/coreservices/skindextype/1443295-init)
- [init(rawValue: UInt32)](/documentation/coreservices/skindextype/1442314-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/coreservices/skindextype/1450496-rawvalue)
- [SKSearchType](/documentation/coreservices/sksearchtype)

#### Constants

- [var kSKSearchRanked: SKSearchType](/documentation/coreservices/ksksearchranked)
- [var kSKSearchBooleanRanked: SKSearchType](/documentation/coreservices/ksksearchbooleanranked)
- [var kSKSearchRequiredRanked: SKSearchType](/documentation/coreservices/ksksearchrequiredranked)
- [var kSKSearchPrefixRanked: SKSearchType](/documentation/coreservices/ksksearchprefixranked)

#### Initializers

- [init(UInt32)](/documentation/coreservices/sksearchtype/1449367-init)
- [init(rawValue: UInt32)](/documentation/coreservices/sksearchtype/1448964-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/coreservices/sksearchtype/1445786-rawvalue)
- [var kSKDocumentStateAddPending: SKDocumentIndexState](/documentation/coreservices/kskdocumentstateaddpending)
- [var kSKDocumentStateDeletePending: SKDocumentIndexState](/documentation/coreservices/kskdocumentstatedeletepending)
- [var kSKDocumentStateIndexed: SKDocumentIndexState](/documentation/coreservices/kskdocumentstateindexed)
- [var kSKDocumentStateNotIndexed: SKDocumentIndexState](/documentation/coreservices/kskdocumentstatenotindexed)
- [var kSKIndexInverted: SKIndexType](/documentation/coreservices/kskindexinverted)
- [var kSKIndexInvertedVector: SKIndexType](/documentation/coreservices/kskindexinvertedvector)
- [var kSKIndexUnknown: SKIndexType](/documentation/coreservices/kskindexunknown)
- [var kSKIndexVector: SKIndexType](/documentation/coreservices/kskindexvector)
- [var kSKSearchBooleanRanked: SKSearchType](/documentation/coreservices/ksksearchbooleanranked)
- [var kSKSearchPrefixRanked: SKSearchType](/documentation/coreservices/ksksearchprefixranked)
- [var kSKSearchRanked: SKSearchType](/documentation/coreservices/ksksearchranked)
- [var kSKSearchRequiredRanked: SKSearchType](/documentation/coreservices/ksksearchrequiredranked)
- [Carbon Core](/documentation/coreservices/carbon_core)

### Managers

- [Component Manager](/documentation/coreservices/carbon_core/component_manager)

#### Result Codes

- [var invalidComponentID: Int](/documentation/coreservices/invalidcomponentid)
- [var validInstancesExist: Int](/documentation/coreservices/validinstancesexist)
- [var componentNotCaptured: Int](/documentation/coreservices/componentnotcaptured)
- [var componentDontRegister: Int](/documentation/coreservices/componentdontregister)
- [var unresolvedComponentDLLErr: Int](/documentation/coreservices/unresolvedcomponentdllerr)
- [var retryComponentRegistrationErr: Int](/documentation/coreservices/retrycomponentregistrationerr)
- [var badComponentSelector: Int](/documentation/coreservices/badcomponentselector)
- [var badComponentInstance: Int](/documentation/coreservices/badcomponentinstance)
- [Gestalt Manager](/documentation/coreservices/carbon_core/gestalt_manager)

#### Result Codes

- [var gestaltUnknownErr: Int](/documentation/coreservices/gestaltunknownerr)
- [var gestaltUndefSelectorErr: Int](/documentation/coreservices/gestaltundefselectorerr)
- [var gestaltDupSelectorErr: Int](/documentation/coreservices/gestaltdupselectorerr)
- [var gestaltLocationErr: Int](/documentation/coreservices/gestaltlocationerr)
- [Text Encoding Conversion Manager](/documentation/coreservices/carbon_core/text_encoding_conversion_manager)

#### Result Codes

- [var kTextUnsupportedEncodingErr: Int](/documentation/coreservices/ktextunsupportedencodingerr)
- [var kTextMalformedInputErr: Int](/documentation/coreservices/ktextmalformedinputerr)
- [var kTextUndefinedElementErr: Int](/documentation/coreservices/ktextundefinedelementerr)
- [var kTECMissingTableErr: Int](/documentation/coreservices/ktecmissingtableerr)
- [var kTECTableChecksumErr: Int](/documentation/coreservices/ktectablechecksumerr)
- [var kTECTableFormatErr: Int](/documentation/coreservices/ktectableformaterr)
- [var kTECCorruptConverterErr: Int](/documentation/coreservices/kteccorruptconvertererr)
- [var kTECNoConversionPathErr: Int](/documentation/coreservices/ktecnoconversionpatherr)
- [var kTECBufferBelowMinimumSizeErr: Int](/documentation/coreservices/ktecbufferbelowminimumsizeerr)
- [var kTECArrayFullErr: Int](/documentation/coreservices/ktecarrayfullerr)
- [var kTECPartialCharErr: Int](/documentation/coreservices/ktecpartialcharerr)
- [var kTECUnmappableElementErr: Int](/documentation/coreservices/ktecunmappableelementerr)
- [var kTECIncompleteElementErr: Int](/documentation/coreservices/ktecincompleteelementerr)
- [var kTECDirectionErr: Int](/documentation/coreservices/ktecdirectionerr)
- [var kTECGlobalsUnavailableErr: Int](/documentation/coreservices/ktecglobalsunavailableerr)
- [var kTECItemUnavailableErr: Int](/documentation/coreservices/ktecitemunavailableerr)
- [var kTECUsedFallbacksStatus: Int](/documentation/coreservices/ktecusedfallbacksstatus)
- [var kTECNeedFlushStatus: Int](/documentation/coreservices/ktecneedflushstatus)
- [var kTECOutputBufferFullStatus: Int](/documentation/coreservices/ktecoutputbufferfullstatus)

### Services

- [Multiprocessing Services](/documentation/coreservices/carbon_core/multiprocessing_services)

#### Result Codes

- [var kMPIterationEndErr: Int](/documentation/coreservices/kmpiterationenderr)
- [var kMPPrivilegedErr: Int](/documentation/coreservices/kmpprivilegederr)
- [var kMPProcessCreatedErr: Int](/documentation/coreservices/kmpprocesscreatederr)
- [var kMPProcessTerminatedErr: Int](/documentation/coreservices/kmpprocessterminatederr)
- [var kMPTaskCreatedErr: Int](/documentation/coreservices/kmptaskcreatederr)
- [var kMPTaskBlockedErr: Int](/documentation/coreservices/kmptaskblockederr)
- [var kMPTaskStoppedErr: Int](/documentation/coreservices/kmptaskstoppederr)
- [var kMPDeletedErr: Int](/documentation/coreservices/kmpdeletederr)
- [var kMPTimeoutErr: Int](/documentation/coreservices/kmptimeouterr)
- [var kMPInsufficientResourcesErr: Int](/documentation/coreservices/kmpinsufficientresourceserr)
- [var kMPInvalidIDErr: Int](/documentation/coreservices/kmpinvalididerr)

### Utilities

- [Unicode Utilities](/documentation/coreservices/carbon_core/unicode_utilities)

#### Inputting Unicode Text

- [func UCKeyTranslate(UnsafePointer<UCKeyboardLayout>!, UInt16, UInt16, UInt32, UInt32, OptionBits, UnsafeMutablePointer<UInt32>!, Int, UnsafeMutablePointer<Int>!, UnsafeMutablePointer<UniChar>!) -> OSStatus](/documentation/coreservices/1390584-uckeytranslate)

#### Comparing Unicode Strings

- [func UCCreateCollator(LocaleRef!, LocaleOperationVariant, UCCollateOptions, UnsafeMutablePointer<CollatorRef?>!) -> OSStatus](/documentation/coreservices/1390403-uccreatecollator)
- [func UCCompareText(CollatorRef!, UnsafePointer<UniChar>!, Int, UnsafePointer<UniChar>!, Int, UnsafeMutablePointer<DarwinBoolean>!, UnsafeMutablePointer<Int32>!) -> OSStatus](/documentation/coreservices/1390642-uccomparetext)
- [func UCGetCollationKey(CollatorRef!, UnsafePointer<UniChar>!, Int, Int, UnsafeMutablePointer<Int>!, UnsafeMutablePointer<UCCollationValue>!) -> OSStatus](/documentation/coreservices/1390468-ucgetcollationkey)
- [func UCCompareCollationKeys(UnsafePointer<UCCollationValue>!, Int, UnsafePointer<UCCollationValue>!, Int, UnsafeMutablePointer<DarwinBoolean>!, UnsafeMutablePointer<Int32>!) -> OSStatus](/documentation/coreservices/1390378-uccomparecollationkeys)
- [func UCDisposeCollator(UnsafeMutablePointer<CollatorRef?>!) -> OSStatus](/documentation/coreservices/1390435-ucdisposecollator)
- [func UCCompareTextDefault(UCCollateOptions, UnsafePointer<UniChar>!, Int, UnsafePointer<UniChar>!, Int, UnsafeMutablePointer<DarwinBoolean>!, UnsafeMutablePointer<Int32>!) -> OSStatus](/documentation/coreservices/1390472-uccomparetextdefault)
- [func UCCompareTextNoLocale(UCCollateOptions, UnsafePointer<UniChar>!, Int, UnsafePointer<UniChar>!, Int, UnsafeMutablePointer<DarwinBoolean>!, UnsafeMutablePointer<Int32>!) -> OSStatus](/documentation/coreservices/1390513-uccomparetextnolocale)

#### Data Types

- [CollatorRef](/documentation/coreservices/collatorref)
- [TextBreakLocatorRef](/documentation/coreservices/textbreaklocatorref)
- [UCCollationValue](/documentation/coreservices/uccollationvalue)
- [UCKeyboardLayout](/documentation/coreservices/uckeyboardlayout)

##### Initializers

- [init()](/documentation/coreservices/uckeyboardlayout/1447446-init)
- [init(keyLayoutHeaderFormat: UInt16, keyLayoutDataVersion: UInt16, keyLayoutFeatureInfoOffset: UInt32, keyboardTypeCount: UInt32, keyboardTypeList: UCKeyboardTypeHeader)](/documentation/coreservices/uckeyboardlayout/1448404-init)

##### Instance Properties

- [var keyLayoutDataVersion: UInt16](/documentation/coreservices/uckeyboardlayout/1390626-keylayoutdataversion)
- [var keyLayoutFeatureInfoOffset: UInt32](/documentation/coreservices/uckeyboardlayout/1390597-keylayoutfeatureinfooffset)
- [var keyLayoutHeaderFormat: UInt16](/documentation/coreservices/uckeyboardlayout/1390425-keylayoutheaderformat)
- [var keyboardTypeCount: UInt32](/documentation/coreservices/uckeyboardlayout/1390448-keyboardtypecount)
- [var keyboardTypeList: UCKeyboardTypeHeader](/documentation/coreservices/uckeyboardlayout/1390494-keyboardtypelist)
- [UCKeyboardTypeHeader](/documentation/coreservices/uckeyboardtypeheader)

##### Initializers

- [init()](/documentation/coreservices/uckeyboardtypeheader/1447622-init)
- [init(keyboardTypeFirst: UInt32, keyboardTypeLast: UInt32, keyModifiersToTableNumOffset: UInt32, keyToCharTableIndexOffset: UInt32, keyStateRecordsIndexOffset: UInt32, keyStateTerminatorsOffset: UInt32, keySequenceDataIndexOffset: UInt32)](/documentation/coreservices/uckeyboardtypeheader/1444448-init)

##### Instance Properties

- [var keyModifiersToTableNumOffset: UInt32](/documentation/coreservices/uckeyboardtypeheader/1390601-keymodifierstotablenumoffset)
- [var keySequenceDataIndexOffset: UInt32](/documentation/coreservices/uckeyboardtypeheader/1390532-keysequencedataindexoffset)
- [var keyStateRecordsIndexOffset: UInt32](/documentation/coreservices/uckeyboardtypeheader/1390632-keystaterecordsindexoffset)
- [var keyStateTerminatorsOffset: UInt32](/documentation/coreservices/uckeyboardtypeheader/1390415-keystateterminatorsoffset)
- [var keyToCharTableIndexOffset: UInt32](/documentation/coreservices/uckeyboardtypeheader/1390613-keytochartableindexoffset)
- [var keyboardTypeFirst: UInt32](/documentation/coreservices/uckeyboardtypeheader/1390499-keyboardtypefirst)
- [var keyboardTypeLast: UInt32](/documentation/coreservices/uckeyboardtypeheader/1390423-keyboardtypelast)
- [UCKeyCharSeq](/documentation/coreservices/uckeycharseq)
- [UCKeyLayoutFeatureInfo](/documentation/coreservices/uckeylayoutfeatureinfo)

##### Initializers

- [init()](/documentation/coreservices/uckeylayoutfeatureinfo/1442653-init)
- [init(keyLayoutFeatureInfoFormat: UInt16, reserved: UInt16, maxOutputStringLength: UInt32)](/documentation/coreservices/uckeylayoutfeatureinfo/1445182-init)

##### Instance Properties

- [var keyLayoutFeatureInfoFormat: UInt16](/documentation/coreservices/uckeylayoutfeatureinfo/1390617-keylayoutfeatureinfoformat)
- [var maxOutputStringLength: UInt32](/documentation/coreservices/uckeylayoutfeatureinfo/1390572-maxoutputstringlength)
- [var reserved: UInt16](/documentation/coreservices/uckeylayoutfeatureinfo/1390566-reserved)
- [UCKeyModifiersToTableNum](/documentation/coreservices/uckeymodifierstotablenum)

##### Initializers

- [init()](/documentation/coreservices/uckeymodifierstotablenum/1443345-init)
- [init(keyModifiersToTableNumFormat: UInt16, defaultTableNum: UInt16, modifiersCount: UInt32, tableNum: UInt8)](/documentation/coreservices/uckeymodifierstotablenum/1444613-init)

##### Instance Properties

- [var defaultTableNum: UInt16](/documentation/coreservices/uckeymodifierstotablenum/1390542-defaulttablenum)
- [var keyModifiersToTableNumFormat: UInt16](/documentation/coreservices/uckeymodifierstotablenum/1390556-keymodifierstotablenumformat)
- [var modifiersCount: UInt32](/documentation/coreservices/uckeymodifierstotablenum/1390509-modifierscount)
- [var tableNum: UInt8](/documentation/coreservices/uckeymodifierstotablenum/1390564-tablenum)
- [UCKeyOutput](/documentation/coreservices/uckeyoutput)
- [UCKeySequenceDataIndex](/documentation/coreservices/uckeysequencedataindex)

##### Initializers

- [init()](/documentation/coreservices/uckeysequencedataindex/1445802-init)
- [init(keySequenceDataIndexFormat: UInt16, charSequenceCount: UInt16, charSequenceOffsets: UInt16)](/documentation/coreservices/uckeysequencedataindex/1442334-init)

##### Instance Properties

- [var charSequenceCount: UInt16](/documentation/coreservices/uckeysequencedataindex/1390623-charsequencecount)
- [var charSequenceOffsets: UInt16](/documentation/coreservices/uckeysequencedataindex/1390466-charsequenceoffsets)
- [var keySequenceDataIndexFormat: UInt16](/documentation/coreservices/uckeysequencedataindex/1390357-keysequencedataindexformat)
- [UCKeyStateEntryRange](/documentation/coreservices/uckeystateentryrange)

##### Initializers

- [init()](/documentation/coreservices/uckeystateentryrange/1448909-init)
- [init(curStateStart: UInt16, curStateRange: UInt8, deltaMultiplier: UInt8, charData: UCKeyCharSeq, nextState: UInt16)](/documentation/coreservices/uckeystateentryrange/1446762-init)

##### Instance Properties

- [var charData: UCKeyCharSeq](/documentation/coreservices/uckeystateentryrange/1390454-chardata)
- [var curStateRange: UInt8](/documentation/coreservices/uckeystateentryrange/1390515-curstaterange)
- [var curStateStart: UInt16](/documentation/coreservices/uckeystateentryrange/1390496-curstatestart)
- [var deltaMultiplier: UInt8](/documentation/coreservices/uckeystateentryrange/1390570-deltamultiplier)
- [var nextState: UInt16](/documentation/coreservices/uckeystateentryrange/1390484-nextstate)
- [UCKeyStateEntryTerminal](/documentation/coreservices/uckeystateentryterminal)

##### Initializers

- [init()](/documentation/coreservices/uckeystateentryterminal/1443469-init)
- [init(curState: UInt16, charData: UCKeyCharSeq)](/documentation/coreservices/uckeystateentryterminal/1446872-init)

##### Instance Properties

- [var charData: UCKeyCharSeq](/documentation/coreservices/uckeystateentryterminal/1390590-chardata)
- [var curState: UInt16](/documentation/coreservices/uckeystateentryterminal/1390480-curstate)
- [UCKeyStateRecord](/documentation/coreservices/uckeystaterecord)

##### Initializers

- [init()](/documentation/coreservices/uckeystaterecord/1448351-init)
- [init(stateZeroCharData: UCKeyCharSeq, stateZeroNextState: UInt16, stateEntryCount: UInt16, stateEntryFormat: UInt16, stateEntryData: UInt32)](/documentation/coreservices/uckeystaterecord/1442959-init)

##### Instance Properties

- [var stateEntryCount: UInt16](/documentation/coreservices/uckeystaterecord/1390646-stateentrycount)
- [var stateEntryData: UInt32](/documentation/coreservices/uckeystaterecord/1390413-stateentrydata)
- [var stateEntryFormat: UInt16](/documentation/coreservices/uckeystaterecord/1390450-stateentryformat)
- [var stateZeroCharData: UCKeyCharSeq](/documentation/coreservices/uckeystaterecord/1390580-statezerochardata)
- [var stateZeroNextState: UInt16](/documentation/coreservices/uckeystaterecord/1390554-statezeronextstate)
- [UCKeyStateRecordsIndex](/documentation/coreservices/uckeystaterecordsindex)

##### Initializers

- [init()](/documentation/coreservices/uckeystaterecordsindex/1444702-init)
- [init(keyStateRecordsIndexFormat: UInt16, keyStateRecordCount: UInt16, keyStateRecordOffsets: UInt32)](/documentation/coreservices/uckeystaterecordsindex/1449991-init)

##### Instance Properties

- [var keyStateRecordCount: UInt16](/documentation/coreservices/uckeystaterecordsindex/1390398-keystaterecordcount)
- [var keyStateRecordOffsets: UInt32](/documentation/coreservices/uckeystaterecordsindex/1390490-keystaterecordoffsets)
- [var keyStateRecordsIndexFormat: UInt16](/documentation/coreservices/uckeystaterecordsindex/1390380-keystaterecordsindexformat)
- [UCKeyStateTerminators](/documentation/coreservices/uckeystateterminators)

##### Initializers

- [init()](/documentation/coreservices/uckeystateterminators/1448249-init)
- [init(keyStateTerminatorsFormat: UInt16, keyStateTerminatorCount: UInt16, keyStateTerminators: UCKeyCharSeq)](/documentation/coreservices/uckeystateterminators/1443209-init)

##### Instance Properties

- [var keyStateTerminatorCount: UInt16](/documentation/coreservices/uckeystateterminators/1390511-keystateterminatorcount)
- [var keyStateTerminators: UCKeyCharSeq](/documentation/coreservices/uckeystateterminators/1390409-keystateterminators)
- [var keyStateTerminatorsFormat: UInt16](/documentation/coreservices/uckeystateterminators/1390431-keystateterminatorsformat)
- [UCKeyToCharTableIndex](/documentation/coreservices/uckeytochartableindex)

##### Initializers

- [init()](/documentation/coreservices/uckeytochartableindex/1444832-init)
- [init(keyToCharTableIndexFormat: UInt16, keyToCharTableSize: UInt16, keyToCharTableCount: UInt32, keyToCharTableOffsets: UInt32)](/documentation/coreservices/uckeytochartableindex/1450385-init)

##### Instance Properties

- [var keyToCharTableCount: UInt32](/documentation/coreservices/uckeytochartableindex/1390611-keytochartablecount)
- [var keyToCharTableIndexFormat: UInt16](/documentation/coreservices/uckeytochartableindex/1390562-keytochartableindexformat)
- [var keyToCharTableOffsets: UInt32](/documentation/coreservices/uckeytochartableindex/1390388-keytochartableoffsets)
- [var keyToCharTableSize: UInt16](/documentation/coreservices/uckeytochartableindex/1390382-keytochartablesize)

#### Constants

- [Fixed Ordering Scheme](/documentation/coreservices/carbon_core/unicode_utilities/1390361-fixed_ordering_scheme)

##### Constants

- [var kUCCollateTypeHFSExtended: Int](/documentation/coreservices/kuccollatetypehfsextended)
- [Fixed Ordering Masks 1](/documentation/coreservices/carbon_core/unicode_utilities/1390370-fixed_ordering_masks_1)

##### Constants

- [var kUCCollateTypeSourceMask: Int](/documentation/coreservices/kuccollatetypesourcemask)
- [var kUCCollateTypeShiftBits: Int](/documentation/coreservices/kuccollatetypeshiftbits)
- [Fixed Ordering Masks 2](/documentation/coreservices/carbon_core/unicode_utilities/1390573-fixed_ordering_masks_2)

##### Constants

- [var kUCCollateTypeMask: UInt32](/documentation/coreservices/kuccollatetypemask)
- [Key Actions](/documentation/coreservices/carbon_core/unicode_utilities/1390619-key_actions)

##### Constants

- [var kUCKeyActionDown: Int](/documentation/coreservices/kuckeyactiondown)
- [var kUCKeyActionUp: Int](/documentation/coreservices/kuckeyactionup)
- [var kUCKeyActionAutoKey: Int](/documentation/coreservices/kuckeyactionautokey)
- [var kUCKeyActionDisplay: Int](/documentation/coreservices/kuckeyactiondisplay)
- [Key Format Codes](/documentation/coreservices/carbon_core/unicode_utilities/1390609-key_format_codes)

##### Constants

- [var kUCKeyLayoutHeaderFormat: Int](/documentation/coreservices/kuckeylayoutheaderformat)
- [var kUCKeyLayoutFeatureInfoFormat: Int](/documentation/coreservices/kuckeylayoutfeatureinfoformat)
- [var kUCKeyModifiersToTableNumFormat: Int](/documentation/coreservices/kuckeymodifierstotablenumformat)
- [var kUCKeyToCharTableIndexFormat: Int](/documentation/coreservices/kuckeytochartableindexformat)
- [var kUCKeyStateRecordsIndexFormat: Int](/documentation/coreservices/kuckeystaterecordsindexformat)
- [var kUCKeyStateTerminatorsFormat: Int](/documentation/coreservices/kuckeystateterminatorsformat)
- [var kUCKeySequenceDataIndexFormat: Int](/documentation/coreservices/kuckeysequencedataindexformat)
- [Key Output Index Masks](/documentation/coreservices/carbon_core/unicode_utilities/1390638-key_output_index_masks)

##### Constants

- [var kUCKeyOutputStateIndexMask: Int](/documentation/coreservices/kuckeyoutputstateindexmask)
- [var kUCKeyOutputSequenceIndexMask: Int](/documentation/coreservices/kuckeyoutputsequenceindexmask)
- [var kUCKeyOutputTestForIndexMask: Int](/documentation/coreservices/kuckeyoutputtestforindexmask)
- [var kUCKeyOutputGetIndexMask: Int](/documentation/coreservices/kuckeyoutputgetindexmask)
- [Key State Entry Formats](/documentation/coreservices/carbon_core/unicode_utilities/1390376-key_state_entry_formats)

##### Constants

- [var kUCKeyStateEntryTerminalFormat: Int](/documentation/coreservices/kuckeystateentryterminalformat)
- [var kUCKeyStateEntryRangeFormat: Int](/documentation/coreservices/kuckeystateentryrangeformat)
- [Key Translation Options Flag](/documentation/coreservices/carbon_core/unicode_utilities/1390507-key_translation_options_flag)

##### Constants

- [var kUCKeyTranslateNoDeadKeysBit: Int](/documentation/coreservices/kuckeytranslatenodeadkeysbit)
- [Key Translation Options Mask](/documentation/coreservices/carbon_core/unicode_utilities/1390568-key_translation_options_mask)

##### Constants

- [var kUCKeyTranslateNoDeadKeysMask: Int](/documentation/coreservices/kuckeytranslatenodeadkeysmask)
- [Operation Class](/documentation/coreservices/carbon_core/unicode_utilities/1390359-operation_class)

##### Constants

- [var kUnicodeCollationClass: Int](/documentation/coreservices/kunicodecollationclass)
- [Standard Options Mask](/documentation/coreservices/carbon_core/unicode_utilities/1390444-standard_options_mask)

##### Constants

- [var kUCCollateStandardOptions: Int](/documentation/coreservices/kuccollatestandardoptions)
- [UCCollateOptions](/documentation/coreservices/uccollateoptions)

##### Constants

- [var kUCCollateComposeInsensitiveMask: Int](/documentation/coreservices/kuccollatecomposeinsensitivemask)
- [var kUCCollateWidthInsensitiveMask: Int](/documentation/coreservices/kuccollatewidthinsensitivemask)
- [var kUCCollateCaseInsensitiveMask: Int](/documentation/coreservices/kuccollatecaseinsensitivemask)
- [var kUCCollateDiacritInsensitiveMask: Int](/documentation/coreservices/kuccollatediacritinsensitivemask)
- [var kUCCollatePunctuationSignificantMask: Int](/documentation/coreservices/kuccollatepunctuationsignificantmask)
- [var kUCCollateDigitsOverrideMask: Int](/documentation/coreservices/kuccollatedigitsoverridemask)
- [var kUCCollateDigitsAsNumberMask: Int](/documentation/coreservices/kuccollatedigitsasnumbermask)
- [UCTextBreakOptions](/documentation/coreservices/uctextbreakoptions)

##### Constants

- [var kUCTextBreakLeadingEdgeMask: Int](/documentation/coreservices/kuctextbreakleadingedgemask)
- [var kUCTextBreakGoBackwardsMask: Int](/documentation/coreservices/kuctextbreakgobackwardsmask)
- [var kUCTextBreakIterateMask: Int](/documentation/coreservices/kuctextbreakiteratemask)
- [UCTextBreakType](/documentation/coreservices/uctextbreaktype)

##### Constants

- [var kUCTextBreakCharMask: Int](/documentation/coreservices/kuctextbreakcharmask)
- [var kUCTextBreakClusterMask: Int](/documentation/coreservices/kuctextbreakclustermask)
- [var kUCTextBreakWordMask: Int](/documentation/coreservices/kuctextbreakwordmask)
- [var kUCTextBreakLineMask: Int](/documentation/coreservices/kuctextbreaklinemask)
- [Text Boundary Operation Class](/documentation/coreservices/carbon_core/unicode_utilities/1390460-text_boundary_operation_class)

##### Constants

- [var kUnicodeTextBreakClass: Int](/documentation/coreservices/kunicodetextbreakclass)

### Other Reference

- [Carbon Core Structures](/documentation/coreservices/carbon_core/carbon_core_structures)

#### Structures

- [FSEventStreamContext](/documentation/coreservices/fseventstreamcontext)

##### Initializers

- [init()](/documentation/coreservices/fseventstreamcontext/1445021-init)
- [init(version: CFIndex, info: UnsafeMutableRawPointer?, retain: CFAllocatorRetainCallBack?, release: CFAllocatorReleaseCallBack?, copyDescription: CFAllocatorCopyDescriptionCallBack?)](/documentation/coreservices/fseventstreamcontext/1792099-init)

##### Instance Properties

- [var copyDescription: CFAllocatorCopyDescriptionCallBack?](/documentation/coreservices/fseventstreamcontext/1445178-copydescription)
- [var info: UnsafeMutableRawPointer?](/documentation/coreservices/fseventstreamcontext/1446169-info)
- [var release: CFAllocatorReleaseCallBack?](/documentation/coreservices/fseventstreamcontext/1450554-release)
- [var retain: CFAllocatorRetainCallBack?](/documentation/coreservices/fseventstreamcontext/1450539-retain)
- [var version: CFIndex](/documentation/coreservices/fseventstreamcontext/1444474-version)
- [IntlText](/documentation/coreservices/intltext)

##### Initializers

- [init()](/documentation/coreservices/intltext/1449738-init)
- [init(theScriptCode: ScriptCode, theLangCode: LangCode, theText: CChar)](/documentation/coreservices/intltext/1442684-init)

##### Instance Properties

- [var theLangCode: LangCode](/documentation/coreservices/intltext/1441911-thelangcode)
- [var theScriptCode: ScriptCode](/documentation/coreservices/intltext/1441824-thescriptcode)
- [var theText: CChar](/documentation/coreservices/intltext/1442075-thetext)
- [OffsetArray](/documentation/coreservices/offsetarray)

##### Initializers

- [init()](/documentation/coreservices/offsetarray/1442543-init)
- [init(fNumOfOffsets: Int16, fOffset: Int32)](/documentation/coreservices/offsetarray/1444181-init)

##### Instance Properties

- [var fNumOfOffsets: Int16](/documentation/coreservices/offsetarray/1449726-fnumofoffsets)
- [var fOffset: Int32](/documentation/coreservices/offsetarray/1447345-foffset)
- [TScriptingSizeResource](/documentation/coreservices/tscriptingsizeresource)

##### Initializers

- [init()](/documentation/coreservices/tscriptingsizeresource/1448164-init)
- [init(scriptingSizeFlags: Int16, minStackSize: UInt32, preferredStackSize: UInt32, maxStackSize: UInt32, minHeapSize: UInt32, preferredHeapSize: UInt32, maxHeapSize: UInt32)](/documentation/coreservices/tscriptingsizeresource/1449828-init)

##### Instance Properties

- [var maxHeapSize: UInt32](/documentation/coreservices/tscriptingsizeresource/1445513-maxheapsize)
- [var maxStackSize: UInt32](/documentation/coreservices/tscriptingsizeresource/1446886-maxstacksize)
- [var minHeapSize: UInt32](/documentation/coreservices/tscriptingsizeresource/1447071-minheapsize)
- [var minStackSize: UInt32](/documentation/coreservices/tscriptingsizeresource/1447932-minstacksize)
- [var preferredHeapSize: UInt32](/documentation/coreservices/tscriptingsizeresource/1448874-preferredheapsize)
- [var preferredStackSize: UInt32](/documentation/coreservices/tscriptingsizeresource/1447038-preferredstacksize)
- [var scriptingSizeFlags: Int16](/documentation/coreservices/tscriptingsizeresource/1442854-scriptingsizeflags)
- [TextRange](/documentation/coreservices/textrange)

##### Initializers

- [init()](/documentation/coreservices/textrange/1445677-init)
- [init(fStart: Int32, fEnd: Int32, fHiliteStyle: Int16)](/documentation/coreservices/textrange/1442042-init)

##### Instance Properties

- [var fEnd: Int32](/documentation/coreservices/textrange/1448002-fend)
- [var fHiliteStyle: Int16](/documentation/coreservices/textrange/1450504-fhilitestyle)
- [var fStart: Int32](/documentation/coreservices/textrange/1449071-fstart)
- [TextRangeArray](/documentation/coreservices/textrangearray)

##### Initializers

- [init()](/documentation/coreservices/textrangearray/1444530-init)
- [init(fNumOfRanges: Int16, fRange: TextRange)](/documentation/coreservices/textrangearray/1442000-init)

##### Instance Properties

- [var fNumOfRanges: Int16](/documentation/coreservices/textrangearray/1444176-fnumofranges)
- [var fRange: TextRange](/documentation/coreservices/textrangearray/1444113-frange)
- [WritingCode](/documentation/coreservices/writingcode)

##### Initializers

- [init()](/documentation/coreservices/writingcode/1447186-init)
- [init(theScriptCode: ScriptCode, theLangCode: LangCode)](/documentation/coreservices/writingcode/1446315-init)

##### Instance Properties

- [var theLangCode: LangCode](/documentation/coreservices/writingcode/1443988-thelangcode)
- [var theScriptCode: ScriptCode](/documentation/coreservices/writingcode/1449673-thescriptcode)
- [ccntTokenRecord](/documentation/coreservices/ccnttokenrecord)

##### Initializers

- [init()](/documentation/coreservices/ccnttokenrecord/1442803-init)
- [init(tokenClass: DescType, token: AEDesc)](/documentation/coreservices/ccnttokenrecord/1443203-init)

##### Instance Properties

- [var token: AEDesc](/documentation/coreservices/ccnttokenrecord/1445534-token)
- [var tokenClass: DescType](/documentation/coreservices/ccnttokenrecord/1444917-tokenclass)
- [Carbon Core Enumerations](/documentation/coreservices/carbon_core/carbon_core_enumerations)

#### Enumerations

- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556447-anonymous)

##### Constants

- [var kToolbarAdvancedIcon: Int](/documentation/coreservices/ktoolbaradvancedicon)
- [var kToolbarApplicationsFolderIcon: Int](/documentation/coreservices/ktoolbarapplicationsfoldericon)
- [var kToolbarCustomizeIcon: Int](/documentation/coreservices/ktoolbarcustomizeicon)
- [var kToolbarDeleteIcon: Int](/documentation/coreservices/ktoolbardeleteicon)
- [var kToolbarDesktopFolderIcon: Int](/documentation/coreservices/ktoolbardesktopfoldericon)
- [var kToolbarDocumentsFolderIcon: Int](/documentation/coreservices/ktoolbardocumentsfoldericon)
- [var kToolbarDownloadsFolderIcon: Int](/documentation/coreservices/ktoolbardownloadsfoldericon)
- [var kToolbarFavoritesIcon: Int](/documentation/coreservices/ktoolbarfavoritesicon)
- [var kToolbarHomeIcon: Int](/documentation/coreservices/ktoolbarhomeicon)
- [var kToolbarInfoIcon: Int](/documentation/coreservices/ktoolbarinfoicon)
- [var kToolbarLabelsIcon: Int](/documentation/coreservices/ktoolbarlabelsicon)
- [var kToolbarLibraryFolderIcon: Int](/documentation/coreservices/ktoolbarlibraryfoldericon)
- [var kToolbarMovieFolderIcon: Int](/documentation/coreservices/ktoolbarmoviefoldericon)
- [var kToolbarMusicFolderIcon: Int](/documentation/coreservices/ktoolbarmusicfoldericon)
- [var kToolbarPicturesFolderIcon: Int](/documentation/coreservices/ktoolbarpicturesfoldericon)
- [var kToolbarPublicFolderIcon: Int](/documentation/coreservices/ktoolbarpublicfoldericon)
- [var kToolbarSitesFolderIcon: Int](/documentation/coreservices/ktoolbarsitesfoldericon)
- [var kToolbarUtilitiesFolderIcon: Int](/documentation/coreservices/ktoolbarutilitiesfoldericon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556440-anonymous)

##### Constants

- [var appleMenuFolderIconResource: Int](/documentation/coreservices/applemenufoldericonresource)
- [var desktopIconResource: Int](/documentation/coreservices/desktopiconresource)
- [var floppyIconResource: Int](/documentation/coreservices/floppyiconresource)
- [var genericApplicationIconResource: Int](/documentation/coreservices/genericapplicationiconresource)
- [var genericCDROMIconResource: Int](/documentation/coreservices/genericcdromiconresource)
- [var genericDeskAccessoryIconResource: Int](/documentation/coreservices/genericdeskaccessoryiconresource)
- [var genericDocumentIconResource: Int](/documentation/coreservices/genericdocumenticonresource)
- [var genericEditionFileIconResource: Int](/documentation/coreservices/genericeditionfileiconresource)
- [var genericExtensionIconResource: Int](/documentation/coreservices/genericextensioniconresource)
- [var genericFileServerIconResource: Int](/documentation/coreservices/genericfileservericonresource)
- [var genericFolderIconResource: Int](/documentation/coreservices/genericfoldericonresource)
- [var genericHardDiskIconResource: Int](/documentation/coreservices/genericharddiskiconresource)
- [var genericMoverObjectIconResource: Int](/documentation/coreservices/genericmoverobjecticonresource)
- [var genericPreferencesIconResource: Int](/documentation/coreservices/genericpreferencesiconresource)
- [var genericQueryDocumentIconResource: Int](/documentation/coreservices/genericquerydocumenticonresource)
- [var genericRAMDiskIconResource: Int](/documentation/coreservices/genericramdiskiconresource)
- [var genericStationeryIconResource: Int](/documentation/coreservices/genericstationeryiconresource)
- [var genericSuitcaseIconResource: Int](/documentation/coreservices/genericsuitcaseiconresource)
- [var openFolderIconResource: Int](/documentation/coreservices/openfoldericonresource)
- [var privateFolderIconResource: Int](/documentation/coreservices/privatefoldericonresource)
- [var systemFolderIconResource: Int](/documentation/coreservices/systemfoldericonresource)
- [var trashIconResource: Int](/documentation/coreservices/trashiconresource)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556433-anonymous)

##### Constants

- [var kIconServicesCatalogInfoMask: Int](/documentation/coreservices/kiconservicescataloginfomask)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556445-anonymous)

##### Constants

- [var kSystemIconsCreator: Int](/documentation/coreservices/ksystemiconscreator)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556421-anonymous)

##### Constants

- [var kAlertCautionBadgeIcon: Int](/documentation/coreservices/kalertcautionbadgeicon)
- [var kAliasBadgeIcon: Int](/documentation/coreservices/kaliasbadgeicon)
- [var kAppleScriptBadgeIcon: Int](/documentation/coreservices/kapplescriptbadgeicon)
- [var kLockedBadgeIcon: Int](/documentation/coreservices/klockedbadgeicon)
- [var kMountedBadgeIcon: Int](/documentation/coreservices/kmountedbadgeicon)
- [var kSharedBadgeIcon: Int](/documentation/coreservices/ksharedbadgeicon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556444-anonymous)

##### Constants

- [var kGroupIcon: Int](/documentation/coreservices/kgroupicon)
- [var kGuestUserIcon: Int](/documentation/coreservices/kguestusericon)
- [var kOwnerIcon: Int](/documentation/coreservices/kownericon)
- [var kUserFolderIcon: Int](/documentation/coreservices/kuserfoldericon)
- [var kUserIcon: Int](/documentation/coreservices/kusericon)
- [var kWorkgroupFolderIcon: Int](/documentation/coreservices/kworkgroupfoldericon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556432-anonymous)

##### Constants

- [var kControlPanelFolderIconResource: Int](/documentation/coreservices/kcontrolpanelfoldericonresource)
- [var kDropFolderIconResource: Int](/documentation/coreservices/kdropfoldericonresource)
- [var kExtensionsFolderIconResource: Int](/documentation/coreservices/kextensionsfoldericonresource)
- [var kFontsFolderIconResource: Int](/documentation/coreservices/kfontsfoldericonresource)
- [var kFullTrashIconResource: Int](/documentation/coreservices/kfulltrashiconresource)
- [var kMountedFolderIconResource: Int](/documentation/coreservices/kmountedfoldericonresource)
- [var kOwnedFolderIconResource: Int](/documentation/coreservices/kownedfoldericonresource)
- [var kPreferencesFolderIconResource: Int](/documentation/coreservices/kpreferencesfoldericonresource)
- [var kPrintMonitorFolderIconResource: Int](/documentation/coreservices/kprintmonitorfoldericonresource)
- [var kSharedFolderIconResource: Int](/documentation/coreservices/ksharedfoldericonresource)
- [var kStartupFolderIconResource: Int](/documentation/coreservices/kstartupfoldericonresource)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556420-anonymous)

##### Constants

- [var kSharingPrivsNotApplicableIcon: Int](/documentation/coreservices/ksharingprivsnotapplicableicon)
- [var kSharingPrivsReadOnlyIcon: Int](/documentation/coreservices/ksharingprivsreadonlyicon)
- [var kSharingPrivsReadWriteIcon: Int](/documentation/coreservices/ksharingprivsreadwriteicon)
- [var kSharingPrivsUnknownIcon: Int](/documentation/coreservices/ksharingprivsunknownicon)
- [var kSharingPrivsWritableIcon: Int](/documentation/coreservices/ksharingprivswritableicon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556424-anonymous)

##### Constants

- [var kAFPServerIcon: Int](/documentation/coreservices/kafpservericon)
- [var kAppleTalkIcon: Int](/documentation/coreservices/kappletalkicon)
- [var kAppleTalkZoneIcon: Int](/documentation/coreservices/kappletalkzoneicon)
- [var kFTPServerIcon: Int](/documentation/coreservices/kftpservericon)
- [var kGenericNetworkIcon: Int](/documentation/coreservices/kgenericnetworkicon)
- [var kHTTPServerIcon: Int](/documentation/coreservices/khttpservericon)
- [var kIPFileServerIcon: Int](/documentation/coreservices/kipfileservericon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556431-anonymous)

##### Constants

- [var kInternetLocationAppleShareIcon: Int](/documentation/coreservices/kinternetlocationappleshareicon)
- [var kInternetLocationAppleTalkZoneIcon: Int](/documentation/coreservices/kinternetlocationappletalkzoneicon)
- [var kInternetLocationFTPIcon: Int](/documentation/coreservices/kinternetlocationftpicon)
- [var kInternetLocationFileIcon: Int](/documentation/coreservices/kinternetlocationfileicon)
- [var kInternetLocationGenericIcon: Int](/documentation/coreservices/kinternetlocationgenericicon)
- [var kInternetLocationHTTPIcon: Int](/documentation/coreservices/kinternetlocationhttpicon)
- [var kInternetLocationMailIcon: Int](/documentation/coreservices/kinternetlocationmailicon)
- [var kInternetLocationNSLNeighborhoodIcon: Int](/documentation/coreservices/kinternetlocationnslneighborhoodicon)
- [var kInternetLocationNewsIcon: Int](/documentation/coreservices/kinternetlocationnewsicon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556442-anonymous)

##### Constants

- [var kClipboardIcon: Int](/documentation/coreservices/kclipboardicon)
- [var kClippingPictureTypeIcon: Int](/documentation/coreservices/kclippingpicturetypeicon)
- [var kClippingSoundTypeIcon: Int](/documentation/coreservices/kclippingsoundtypeicon)
- [var kClippingTextTypeIcon: Int](/documentation/coreservices/kclippingtexttypeicon)
- [var kClippingUnknownTypeIcon: Int](/documentation/coreservices/kclippingunknowntypeicon)
- [var kComputerIcon: Int](/documentation/coreservices/kcomputericon)
- [var kDesktopIcon: Int](/documentation/coreservices/kdesktopicon)
- [var kFinderIcon: Int](/documentation/coreservices/kfindericon)
- [var kFontSuitcaseIcon: Int](/documentation/coreservices/kfontsuitcaseicon)
- [var kFullTrashIcon: Int](/documentation/coreservices/kfulltrashicon)
- [var kGenericApplicationIcon: Int](/documentation/coreservices/kgenericapplicationicon)
- [var kGenericCDROMIcon: Int](/documentation/coreservices/kgenericcdromicon)
- [var kGenericComponentIcon: Int](/documentation/coreservices/kgenericcomponenticon)
- [var kGenericControlPanelIcon: Int](/documentation/coreservices/kgenericcontrolpanelicon)
- [var kGenericControlStripModuleIcon: Int](/documentation/coreservices/kgenericcontrolstripmoduleicon)
- [var kGenericDeskAccessoryIcon: Int](/documentation/coreservices/kgenericdeskaccessoryicon)
- [var kGenericDocumentIcon: Int](/documentation/coreservices/kgenericdocumenticon)
- [var kGenericEditionFileIcon: Int](/documentation/coreservices/kgenericeditionfileicon)
- [var kGenericExtensionIcon: Int](/documentation/coreservices/kgenericextensionicon)
- [var kGenericFileServerIcon: Int](/documentation/coreservices/kgenericfileservericon)
- [var kGenericFloppyIcon: Int](/documentation/coreservices/kgenericfloppyicon)
- [var kGenericFontIcon: Int](/documentation/coreservices/kgenericfonticon)
- [var kGenericFontScalerIcon: Int](/documentation/coreservices/kgenericfontscalericon)
- [var kGenericHardDiskIcon: Int](/documentation/coreservices/kgenericharddiskicon)
- [var kGenericIDiskIcon: Int](/documentation/coreservices/kgenericidiskicon)
- [var kGenericMoverObjectIcon: Int](/documentation/coreservices/kgenericmoverobjecticon)
- [var kGenericPCCardIcon: Int](/documentation/coreservices/kgenericpccardicon)
- [var kGenericPreferencesIcon: Int](/documentation/coreservices/kgenericpreferencesicon)
- [var kGenericQueryDocumentIcon: Int](/documentation/coreservices/kgenericquerydocumenticon)
- [var kGenericRAMDiskIcon: Int](/documentation/coreservices/kgenericramdiskicon)
- [var kGenericRemovableMediaIcon: Int](/documentation/coreservices/kgenericremovablemediaicon)
- [var kGenericSharedLibaryIcon: Int](/documentation/coreservices/kgenericsharedlibaryicon)
- [var kGenericStationeryIcon: Int](/documentation/coreservices/kgenericstationeryicon)
- [var kGenericSuitcaseIcon: Int](/documentation/coreservices/kgenericsuitcaseicon)
- [var kGenericURLIcon: Int](/documentation/coreservices/kgenericurlicon)
- [var kGenericWORMIcon: Int](/documentation/coreservices/kgenericwormicon)
- [var kInternationResourcesIcon: Int](/documentation/coreservices/kinternationresourcesicon)
- [var kInternationalResourcesIcon: Int](/documentation/coreservices/kinternationalresourcesicon)
- [var kKeyboardLayoutIcon: Int](/documentation/coreservices/kkeyboardlayouticon)
- [var kSoundFileIcon: Int](/documentation/coreservices/ksoundfileicon)
- [var kSystemSuitcaseIcon: Int](/documentation/coreservices/ksystemsuitcaseicon)
- [var kTrashIcon: Int](/documentation/coreservices/ktrashicon)
- [var kTrueTypeFlatFontIcon: Int](/documentation/coreservices/ktruetypeflatfonticon)
- [var kTrueTypeFontIcon: Int](/documentation/coreservices/ktruetypefonticon)
- [var kTrueTypeMultiFlatFontIcon: Int](/documentation/coreservices/ktruetypemultiflatfonticon)
- [var kUnknownFSObjectIcon: Int](/documentation/coreservices/kunknownfsobjecticon)
- [var kUserIDiskIcon: Int](/documentation/coreservices/kuseridiskicon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556428-anonymous)

##### Constants

- [var kAppearanceFolderIcon: Int](/documentation/coreservices/kappearancefoldericon)
- [var kAppleExtrasFolderIcon: Int](/documentation/coreservices/kappleextrasfoldericon)
- [var kAppleMenuFolderIcon: Int](/documentation/coreservices/kapplemenufoldericon)
- [var kApplicationSupportFolderIcon: Int](/documentation/coreservices/kapplicationsupportfoldericon)
- [var kApplicationsFolderIcon: Int](/documentation/coreservices/kapplicationsfoldericon)
- [var kAssistantsFolderIcon: Int](/documentation/coreservices/kassistantsfoldericon)
- [var kColorSyncFolderIcon: Int](/documentation/coreservices/kcolorsyncfoldericon)
- [var kContextualMenuItemsFolderIcon: Int](/documentation/coreservices/kcontextualmenuitemsfoldericon)
- [var kControlPanelDisabledFolderIcon: Int](/documentation/coreservices/kcontrolpaneldisabledfoldericon)
- [var kControlPanelFolderIcon: Int](/documentation/coreservices/kcontrolpanelfoldericon)
- [var kControlStripModulesFolderIcon: Int](/documentation/coreservices/kcontrolstripmodulesfoldericon)
- [var kDocumentsFolderIcon: Int](/documentation/coreservices/kdocumentsfoldericon)
- [var kExtensionsDisabledFolderIcon: Int](/documentation/coreservices/kextensionsdisabledfoldericon)
- [var kExtensionsFolderIcon: Int](/documentation/coreservices/kextensionsfoldericon)
- [var kFavoritesFolderIcon: Int](/documentation/coreservices/kfavoritesfoldericon)
- [var kFontsFolderIcon: Int](/documentation/coreservices/kfontsfoldericon)
- [var kHelpFolderIcon: Int](/documentation/coreservices/khelpfoldericon)
- [var kInternetFolderIcon: Int](/documentation/coreservices/kinternetfoldericon)
- [var kInternetPlugInFolderIcon: Int](/documentation/coreservices/kinternetpluginfoldericon)
- [var kInternetSearchSitesFolderIcon: Int](/documentation/coreservices/kinternetsearchsitesfoldericon)
- [var kLocalesFolderIcon: Int](/documentation/coreservices/klocalesfoldericon)
- [var kMacOSReadMeFolderIcon: Int](/documentation/coreservices/kmacosreadmefoldericon)
- [var kPreferencesFolderIcon: Int](/documentation/coreservices/kpreferencesfoldericon)
- [var kPrintMonitorFolderIcon: Int](/documentation/coreservices/kprintmonitorfoldericon)
- [var kPrinterDescriptionFolderIcon: Int](/documentation/coreservices/kprinterdescriptionfoldericon)
- [var kPrinterDriverFolderIcon: Int](/documentation/coreservices/kprinterdriverfoldericon)
- [var kPublicFolderIcon: Int](/documentation/coreservices/kpublicfoldericon)
- [var kRecentApplicationsFolderIcon: Int](/documentation/coreservices/krecentapplicationsfoldericon)
- [var kRecentDocumentsFolderIcon: Int](/documentation/coreservices/krecentdocumentsfoldericon)
- [var kRecentServersFolderIcon: Int](/documentation/coreservices/krecentserversfoldericon)
- [var kScriptingAdditionsFolderIcon: Int](/documentation/coreservices/kscriptingadditionsfoldericon)
- [var kScriptsFolderIcon: Int](/documentation/coreservices/kscriptsfoldericon)
- [var kSharedLibrariesFolderIcon: Int](/documentation/coreservices/ksharedlibrariesfoldericon)
- [var kShutdownItemsDisabledFolderIcon: Int](/documentation/coreservices/kshutdownitemsdisabledfoldericon)
- [var kShutdownItemsFolderIcon: Int](/documentation/coreservices/kshutdownitemsfoldericon)
- [var kSpeakableItemsFolder: Int](/documentation/coreservices/kspeakableitemsfolder)
- [var kStartupItemsDisabledFolderIcon: Int](/documentation/coreservices/kstartupitemsdisabledfoldericon)
- [var kStartupItemsFolderIcon: Int](/documentation/coreservices/kstartupitemsfoldericon)
- [var kSystemExtensionDisabledFolderIcon: Int](/documentation/coreservices/ksystemextensiondisabledfoldericon)
- [var kSystemFolderIcon: Int](/documentation/coreservices/ksystemfoldericon)
- [var kTextEncodingsFolderIcon: Int](/documentation/coreservices/ktextencodingsfoldericon)
- [var kUsersFolderIcon: Int](/documentation/coreservices/kusersfoldericon)
- [var kUtilitiesFolderIcon: Int](/documentation/coreservices/kutilitiesfoldericon)
- [var kVoicesFolderIcon: Int](/documentation/coreservices/kvoicesfoldericon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556423-anonymous)

##### Constants

- [var kAppleMenuFolderIconResource: Int](/documentation/coreservices/kapplemenufoldericonresource)
- [var kGenericExtensionIconResource: Int](/documentation/coreservices/kgenericextensioniconresource)
- [var kGenericPreferencesIconResource: Int](/documentation/coreservices/kgenericpreferencesiconresource)
- [var kGenericQueryDocumentIconResource: Int](/documentation/coreservices/kgenericquerydocumenticonresource)
- [var kHelpIconResource: Int](/documentation/coreservices/khelpiconresource)
- [var kSystemFolderIconResource: Int](/documentation/coreservices/ksystemfoldericonresource)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556436-anonymous)

##### Constants

- [var kDropFolderIcon: Int](/documentation/coreservices/kdropfoldericon)
- [var kGenericFolderIcon: Int](/documentation/coreservices/kgenericfoldericon)
- [var kMountedFolderIcon: Int](/documentation/coreservices/kmountedfoldericon)
- [var kOpenFolderIcon: Int](/documentation/coreservices/kopenfoldericon)
- [var kOwnedFolderIcon: Int](/documentation/coreservices/kownedfoldericon)
- [var kPrivateFolderIcon: Int](/documentation/coreservices/kprivatefoldericon)
- [var kSharedFolderIcon: Int](/documentation/coreservices/ksharedfoldericon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556435-anonymous)

##### Constants

- [var kIconServicesNoBadgeFlag: Int](/documentation/coreservices/kiconservicesnobadgeflag)
- [var kIconServicesNormalUsageFlag: Int](/documentation/coreservices/kiconservicesnormalusageflag)
- [var kIconServicesUpdateIfNeededFlag: Int](/documentation/coreservices/kiconservicesupdateifneededflag)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556430-anonymous)

##### Constants

- [var kAlertCautionIcon: Int](/documentation/coreservices/kalertcautionicon)
- [var kAlertNoteIcon: Int](/documentation/coreservices/kalertnoteicon)
- [var kAlertStopIcon: Int](/documentation/coreservices/kalertstopicon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556434-anonymous)

##### Constants

- [var kDesktopIconResource: Int](/documentation/coreservices/kdesktopiconresource)
- [var kGenericFileServerIconResource: Int](/documentation/coreservices/kgenericfileservericonresource)
- [var kGenericHardDiskIconResource: Int](/documentation/coreservices/kgenericharddiskiconresource)
- [var kGenericMoverObjectIconResource: Int](/documentation/coreservices/kgenericmoverobjecticonresource)
- [var kGenericSuitcaseIconResource: Int](/documentation/coreservices/kgenericsuitcaseiconresource)
- [var kOpenFolderIconResource: Int](/documentation/coreservices/kopenfoldericonresource)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556441-anonymous)

##### Constants

- [var kAppleLogoIcon: Int](/documentation/coreservices/kapplelogoicon)
- [var kAppleMenuIcon: Int](/documentation/coreservices/kapplemenuicon)
- [var kBackwardArrowIcon: Int](/documentation/coreservices/kbackwardarrowicon)
- [var kBurningIcon: Int](/documentation/coreservices/kburningicon)
- [var kConnectToIcon: Int](/documentation/coreservices/kconnecttoicon)
- [var kDeleteAliasIcon: Int](/documentation/coreservices/kdeletealiasicon)
- [var kEjectMediaIcon: Int](/documentation/coreservices/kejectmediaicon)
- [var kFavoriteItemsIcon: Int](/documentation/coreservices/kfavoriteitemsicon)
- [var kForwardArrowIcon: Int](/documentation/coreservices/kforwardarrowicon)
- [var kGenericWindowIcon: Int](/documentation/coreservices/kgenericwindowicon)
- [var kGridIcon: Int](/documentation/coreservices/kgridicon)
- [var kHelpIcon: Int](/documentation/coreservices/khelpicon)
- [var kKeepArrangedIcon: Int](/documentation/coreservices/kkeeparrangedicon)
- [var kLockedIcon: Int](/documentation/coreservices/klockedicon)
- [var kNoFilesIcon: Int](/documentation/coreservices/knofilesicon)
- [var kNoFolderIcon: Int](/documentation/coreservices/knofoldericon)
- [var kNoWriteIcon: Int](/documentation/coreservices/knowriteicon)
- [var kProtectedApplicationFolderIcon: Int](/documentation/coreservices/kprotectedapplicationfoldericon)
- [var kProtectedSystemFolderIcon: Int](/documentation/coreservices/kprotectedsystemfoldericon)
- [var kQuestionMarkIcon: Int](/documentation/coreservices/kquestionmarkicon)
- [var kRecentItemsIcon: Int](/documentation/coreservices/krecentitemsicon)
- [var kRightContainerArrowIcon: Int](/documentation/coreservices/krightcontainerarrowicon)
- [var kShortcutIcon: Int](/documentation/coreservices/kshortcuticon)
- [var kSortAscendingIcon: Int](/documentation/coreservices/ksortascendingicon)
- [var kSortDescendingIcon: Int](/documentation/coreservices/ksortdescendingicon)
- [var kUnlockedIcon: Int](/documentation/coreservices/kunlockedicon)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556425-anonymous)

##### Constants

- [var kFloppyIconResource: Int](/documentation/coreservices/kfloppyiconresource)
- [var kGenericApplicationIconResource: Int](/documentation/coreservices/kgenericapplicationiconresource)
- [var kGenericCDROMIconResource: Int](/documentation/coreservices/kgenericcdromiconresource)
- [var kGenericDeskAccessoryIconResource: Int](/documentation/coreservices/kgenericdeskaccessoryiconresource)
- [var kGenericDocumentIconResource: Int](/documentation/coreservices/kgenericdocumenticonresource)
- [var kGenericEditionFileIconResource: Int](/documentation/coreservices/kgenericeditionfileiconresource)
- [var kGenericFolderIconResource: Int](/documentation/coreservices/kgenericfoldericonresource)
- [var kGenericRAMDiskIconResource: Int](/documentation/coreservices/kgenericramdiskiconresource)
- [var kGenericStationeryIconResource: Int](/documentation/coreservices/kgenericstationeryiconresource)
- [var kPrivateFolderIconResource: Int](/documentation/coreservices/kprivatefoldericonresource)
- [var kTrashIconResource: Int](/documentation/coreservices/ktrashiconresource)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556422-anonymous)

##### Constants

- [var controlPanelFolderIconResource: Int](/documentation/coreservices/controlpanelfoldericonresource)
- [var dropFolderIconResource: Int](/documentation/coreservices/dropfoldericonresource)
- [var extensionsFolderIconResource: Int](/documentation/coreservices/extensionsfoldericonresource)
- [var fontsFolderIconResource: Int](/documentation/coreservices/fontsfoldericonresource)
- [var fullTrashIconResource: Int](/documentation/coreservices/fulltrashiconresource)
- [var mountedFolderIconResource: Int](/documentation/coreservices/mountedfoldericonresource)
- [var ownedFolderIconResource: Int](/documentation/coreservices/ownedfoldericonresource)
- [var preferencesFolderIconResource: Int](/documentation/coreservices/preferencesfoldericonresource)
- [var printMonitorFolderIconResource: Int](/documentation/coreservices/printmonitorfoldericonresource)
- [var sharedFolderIconResource: Int](/documentation/coreservices/sharedfoldericonresource)
- [var startupFolderIconResource: Int](/documentation/coreservices/startupfoldericonresource)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1415186-anonymous)

##### Constants

- [var kCSIdentityAuthorityNotAccessibleErr: Int](/documentation/coreservices/kcsidentityauthoritynotaccessibleerr)
- [var kCSIdentityDeletedErr: Int](/documentation/coreservices/kcsidentitydeletederr)
- [var kCSIdentityDuplicateFullNameErr: Int](/documentation/coreservices/kcsidentityduplicatefullnameerr)
- [var kCSIdentityDuplicatePosixNameErr: Int](/documentation/coreservices/kcsidentityduplicateposixnameerr)
- [var kCSIdentityInvalidFullNameErr: Int](/documentation/coreservices/kcsidentityinvalidfullnameerr)
- [var kCSIdentityInvalidPosixNameErr: Int](/documentation/coreservices/kcsidentityinvalidposixnameerr)
- [var kCSIdentityPermissionErr: Int](/documentation/coreservices/kcsidentitypermissionerr)
- [var kCSIdentityUnknownAuthorityErr: Int](/documentation/coreservices/kcsidentityunknownauthorityerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1542844-anonymous)

##### Constants

- [var typeAuditToken: DescType](/documentation/coreservices/typeaudittoken)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1542940-anonymous)

##### Constants

- [var typeCFArrayRef: DescType](/documentation/coreservices/typecfarrayref)
- [var typeCFAttributedStringRef: DescType](/documentation/coreservices/typecfattributedstringref)
- [var typeCFBooleanRef: DescType](/documentation/coreservices/typecfbooleanref)
- [var typeCFDictionaryRef: DescType](/documentation/coreservices/typecfdictionaryref)
- [var typeCFMutableArrayRef: DescType](/documentation/coreservices/typecfmutablearrayref)
- [var typeCFMutableAttributedStringRef: DescType](/documentation/coreservices/typecfmutableattributedstringref)
- [var typeCFMutableDictionaryRef: DescType](/documentation/coreservices/typecfmutabledictionaryref)
- [var typeCFMutableStringRef: DescType](/documentation/coreservices/typecfmutablestringref)
- [var typeCFNumberRef: DescType](/documentation/coreservices/typecfnumberref)
- [var typeCFStringRef: DescType](/documentation/coreservices/typecfstringref)
- [var typeCFTypeRef: DescType](/documentation/coreservices/typecftyperef)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1542914-anonymous)

##### Constants

- [var kAEAlwaysInteract: Int](/documentation/coreservices/kaealwaysinteract)
- [var kAECanInteract: Int](/documentation/coreservices/kaecaninteract)
- [var kAECanSwitchLayer: Int](/documentation/coreservices/kaecanswitchlayer)
- [var kAEDoNotAutomaticallyAddAnnotationsToEvent: Int](/documentation/coreservices/kaedonotautomaticallyaddannotationstoevent)
- [var kAEDontExecute: Int](/documentation/coreservices/kaedontexecute)
- [var kAEDontReconnect: Int](/documentation/coreservices/kaedontreconnect)
- [var kAEDontRecord: Int](/documentation/coreservices/kaedontrecord)
- [var kAENeverInteract: Int](/documentation/coreservices/kaeneverinteract)
- [var kAENoReply: Int](/documentation/coreservices/kaenoreply)
- [var kAEProcessNonReplyEvents: Int](/documentation/coreservices/kaeprocessnonreplyevents)
- [var kAEQueueReply: Int](/documentation/coreservices/kaequeuereply)
- [var kAEWaitReply: Int](/documentation/coreservices/kaewaitreply)
- [var kAEWantReceipt: Int](/documentation/coreservices/kaewantreceipt)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1542749-anonymous)

##### Constants

- [var typeCString: DescType](/documentation/coreservices/typecstring)
- [var typeEncodedString: DescType](/documentation/coreservices/typeencodedstring)
- [var typePString: DescType](/documentation/coreservices/typepstring)
- [var typeStyledUnicodeText: DescType](/documentation/coreservices/typestyledunicodetext)
- [var typeUnicodeText: DescType](/documentation/coreservices/typeunicodetext)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1553739-anonymous)

##### Constants

- [var kCSDiskSpaceRecoveryOptionNoUI: Int](/documentation/coreservices/kcsdiskspacerecoveryoptionnoui)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1581401-anonymous)

##### Constants

- [var kLSSharedFileListDoNotMountVolumes: Int](/documentation/coreservices/klssharedfilelistdonotmountvolumes)
- [var kLSSharedFileListNoUserInteraction: Int](/documentation/coreservices/klssharedfilelistnouserinteraction)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1527221-anonymous)

##### Constants

- [var errAEEventNotPermitted: Int](/documentation/coreservices/erraeeventnotpermitted)
- [var errAETargetAddressNotPermitted: Int](/documentation/coreservices/erraetargetaddressnotpermitted)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1513007-anonymous)

##### Constants

- [var kCSIdentityCommitCompleted: Int](/documentation/coreservices/kcsidentitycommitcompleted)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1513010-anonymous)

##### Constants

- [var kCSIdentityFlagHidden: Int](/documentation/coreservices/kcsidentityflaghidden)
- [var kCSIdentityFlagNone: Int](/documentation/coreservices/kcsidentityflagnone)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1512979-anonymous)

##### Constants

- [var kCSIdentityClassGroup: Int](/documentation/coreservices/kcsidentityclassgroup)
- [var kCSIdentityClassUser: Int](/documentation/coreservices/kcsidentityclassuser)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1573756-anonymous)

##### Constants

- [var aeBuildSyntaxBadData: Int](/documentation/coreservices/aebuildsyntaxbaddata)
- [var aeBuildSyntaxBadDesc: Int](/documentation/coreservices/aebuildsyntaxbaddesc)
- [var aeBuildSyntaxBadEOF: Int](/documentation/coreservices/aebuildsyntaxbadeof)
- [var aeBuildSyntaxBadHex: Int](/documentation/coreservices/aebuildsyntaxbadhex)
- [var aeBuildSyntaxBadNegative: Int](/documentation/coreservices/aebuildsyntaxbadnegative)
- [var aeBuildSyntaxBadToken: Int](/documentation/coreservices/aebuildsyntaxbadtoken)
- [var aeBuildSyntaxCoercedList: Int](/documentation/coreservices/aebuildsyntaxcoercedlist)
- [var aeBuildSyntaxMissingQuote: Int](/documentation/coreservices/aebuildsyntaxmissingquote)
- [var aeBuildSyntaxNoCloseBrace: Int](/documentation/coreservices/aebuildsyntaxnoclosebrace)
- [var aeBuildSyntaxNoCloseBracket: Int](/documentation/coreservices/aebuildsyntaxnoclosebracket)
- [var aeBuildSyntaxNoCloseHex: Int](/documentation/coreservices/aebuildsyntaxnoclosehex)
- [var aeBuildSyntaxNoCloseParen: Int](/documentation/coreservices/aebuildsyntaxnocloseparen)
- [var aeBuildSyntaxNoCloseString: Int](/documentation/coreservices/aebuildsyntaxnoclosestring)
- [var aeBuildSyntaxNoColon: Int](/documentation/coreservices/aebuildsyntaxnocolon)
- [var aeBuildSyntaxNoEOF: Int](/documentation/coreservices/aebuildsyntaxnoeof)
- [var aeBuildSyntaxNoErr: Int](/documentation/coreservices/aebuildsyntaxnoerr)
- [var aeBuildSyntaxNoKey: Int](/documentation/coreservices/aebuildsyntaxnokey)
- [var aeBuildSyntaxOddHex: Int](/documentation/coreservices/aebuildsyntaxoddhex)
- [var aeBuildSyntaxUncoercedDoubleAt: Int](/documentation/coreservices/aebuildsyntaxuncoerceddoubleat)
- [var aeBuildSyntaxUncoercedHex: Int](/documentation/coreservices/aebuildsyntaxuncoercedhex)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1572727-anonymous)

##### Constants

- [var formWhose: Int](/documentation/coreservices/formwhose)
- [var keyAEIndex: Int](/documentation/coreservices/keyaeindex)
- [var keyAETest: Int](/documentation/coreservices/keyaetest)
- [var keyAEWhoseRangeStart: Int](/documentation/coreservices/keyaewhoserangestart)
- [var keyAEWhoseRangeStop: Int](/documentation/coreservices/keyaewhoserangestop)
- [var typeWhoseDescriptor: Int](/documentation/coreservices/typewhosedescriptor)
- [var typeWhoseRange: Int](/documentation/coreservices/typewhoserange)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1645753-anonymous)

##### Constants

- [var typeAbsoluteOrdinal: DescType](/documentation/coreservices/typeabsoluteordinal)
- [var typeCompDescriptor: DescType](/documentation/coreservices/typecompdescriptor)
- [var typeCurrentContainer: DescType](/documentation/coreservices/typecurrentcontainer)
- [var typeIndexDescriptor: DescType](/documentation/coreservices/typeindexdescriptor)
- [var typeLogicalDescriptor: DescType](/documentation/coreservices/typelogicaldescriptor)
- [var typeOSLTokenList: DescType](/documentation/coreservices/typeosltokenlist)
- [var typeObjectBeingExamined: DescType](/documentation/coreservices/typeobjectbeingexamined)
- [var typeObjectSpecifier: DescType](/documentation/coreservices/typeobjectspecifier)
- [var typeRangeDescriptor: DescType](/documentation/coreservices/typerangedescriptor)
- [var typeRelativeDescriptor: DescType](/documentation/coreservices/typerelativedescriptor)
- [var typeToken: DescType](/documentation/coreservices/typetoken)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1455359-anonymous)

##### Constants

- [var kFSEventStreamEventIdSinceNow: UInt](/documentation/coreservices/kfseventstreameventidsincenow)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1645929-anonymous)

##### Constants

- [var kLSLaunchHasUntrustedContents: Int](/documentation/coreservices/klslaunchhasuntrustedcontents)
- [var kLSLaunchInClassic: Int](/documentation/coreservices/klslaunchinclassic)
- [var kLSLaunchInhibitBGOnly: Int](/documentation/coreservices/klslaunchinhibitbgonly)
- [var kLSLaunchNoParams: Int](/documentation/coreservices/klslaunchnoparams)
- [var kLSLaunchStartClassic: Int](/documentation/coreservices/klslaunchstartclassic)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559986-anonymous)

##### Constants

- [var kHIDDeviceNotReady: Int](/documentation/coreservices/khiddevicenotready)
- [var kHIDVersionIncompatibleErr: Int](/documentation/coreservices/khidversionincompatibleerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560077-anonymous)

##### Constants

- [var collectionIndexRangeErr: Int](/documentation/coreservices/collectionindexrangeerr)
- [var collectionItemLockedErr: Int](/documentation/coreservices/collectionitemlockederr)
- [var collectionItemNotFoundErr: Int](/documentation/coreservices/collectionitemnotfounderr)
- [var collectionVersionErr: Int](/documentation/coreservices/collectionversionerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560010-anonymous)

##### Constants

- [var memAZErr: Int](/documentation/coreservices/memazerr)
- [var memAdrErr: Int](/documentation/coreservices/memadrerr)
- [var memBCErr: Int](/documentation/coreservices/membcerr)
- [var memFullErr: Int](/documentation/coreservices/memfullerr)
- [var memLockedErr: Int](/documentation/coreservices/memlockederr)
- [var memPCErr: Int](/documentation/coreservices/mempcerr)
- [var memPurErr: Int](/documentation/coreservices/mempurerr)
- [var memROZErr: Int](/documentation/coreservices/memrozerr)
- [var memROZError: Int](/documentation/coreservices/memrozerror)
- [var memROZWarn: Int](/documentation/coreservices/memrozwarn)
- [var memSCErr: Int](/documentation/coreservices/memscerr)
- [var memWZErr: Int](/documentation/coreservices/memwzerr)
- [var nilHandleErr: Int](/documentation/coreservices/nilhandleerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560023-anonymous)

##### Constants

- [var kUCTokenNotFound: Int](/documentation/coreservices/kuctokennotfound)
- [var kUCTokenizerIterationFinished: Int](/documentation/coreservices/kuctokenizeriterationfinished)
- [var kUCTokenizerUnknownLang: Int](/documentation/coreservices/kuctokenizerunknownlang)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560030-anonymous)

##### Constants

- [var cfragAbortClosureErr: Int](/documentation/coreservices/cfragabortclosureerr)
- [var cfragArchitectureErr: Int](/documentation/coreservices/cfragarchitectureerr)
- [var cfragCFMInternalErr: Int](/documentation/coreservices/cfragcfminternalerr)
- [var cfragCFMStartupErr: Int](/documentation/coreservices/cfragcfmstartuperr)
- [var cfragCFragRsrcErr: Int](/documentation/coreservices/cfragcfragrsrcerr)
- [var cfragClosureIDErr: Int](/documentation/coreservices/cfragclosureiderr)
- [var cfragConnectionIDErr: Int](/documentation/coreservices/cfragconnectioniderr)
- [var cfragContainerIDErr: Int](/documentation/coreservices/cfragcontaineriderr)
- [var cfragContextIDErr: Int](/documentation/coreservices/cfragcontextiderr)
- [var cfragDupRegistrationErr: Int](/documentation/coreservices/cfragdupregistrationerr)
- [var cfragExecFileRefErr: Int](/documentation/coreservices/cfragexecfilereferr)
- [var cfragFileSizeErr: Int](/documentation/coreservices/cfragfilesizeerr)
- [var cfragFirstErrCode: Int](/documentation/coreservices/cfragfirsterrcode)
- [var cfragFragmentCorruptErr: Int](/documentation/coreservices/cfragfragmentcorrupterr)
- [var cfragFragmentFormatErr: Int](/documentation/coreservices/cfragfragmentformaterr)
- [var cfragFragmentUsageErr: Int](/documentation/coreservices/cfragfragmentusageerr)
- [var cfragImportTooNewErr: Int](/documentation/coreservices/cfragimporttoonewerr)
- [var cfragImportTooOldErr: Int](/documentation/coreservices/cfragimporttooolderr)
- [var cfragInitAtBootErr: Int](/documentation/coreservices/cfraginitatbooterr)
- [var cfragInitFunctionErr: Int](/documentation/coreservices/cfraginitfunctionerr)
- [var cfragInitLoopErr: Int](/documentation/coreservices/cfraginitlooperr)
- [var cfragInitOrderErr: Int](/documentation/coreservices/cfraginitordererr)
- [var cfragLastErrCode: Int](/documentation/coreservices/cfraglasterrcode)
- [var cfragLibConnErr: Int](/documentation/coreservices/cfraglibconnerr)
- [var cfragMapFileErr: Int](/documentation/coreservices/cfragmapfileerr)
- [var cfragNoApplicationErr: Int](/documentation/coreservices/cfragnoapplicationerr)
- [var cfragNoClientMemErr: Int](/documentation/coreservices/cfragnoclientmemerr)
- [var cfragNoIDsErr: Int](/documentation/coreservices/cfragnoidserr)
- [var cfragNoLibraryErr: Int](/documentation/coreservices/cfragnolibraryerr)
- [var cfragNoPositionErr: Int](/documentation/coreservices/cfragnopositionerr)
- [var cfragNoPrivateMemErr: Int](/documentation/coreservices/cfragnoprivatememerr)
- [var cfragNoRegistrationErr: Int](/documentation/coreservices/cfragnoregistrationerr)
- [var cfragNoSectionErr: Int](/documentation/coreservices/cfragnosectionerr)
- [var cfragNoSymbolErr: Int](/documentation/coreservices/cfragnosymbolerr)
- [var cfragNotClosureErr: Int](/documentation/coreservices/cfragnotclosureerr)
- [var cfragOutputLengthErr: Int](/documentation/coreservices/cfragoutputlengtherr)
- [var cfragRsrcForkErr: Int](/documentation/coreservices/cfragrsrcforkerr)
- [var cfragStdFolderErr: Int](/documentation/coreservices/cfragstdfoldererr)
- [var cfragUnresolvedErr: Int](/documentation/coreservices/cfragunresolvederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560061-anonymous)

##### Constants

- [var kDMCantBlock: Int](/documentation/coreservices/kdmcantblock)
- [var kDMDisplayAlreadyInstalledErr: Int](/documentation/coreservices/kdmdisplayalreadyinstallederr)
- [var kDMDisplayNotFoundErr: Int](/documentation/coreservices/kdmdisplaynotfounderr)
- [var kDMDriverNotDisplayMgrAwareErr: Int](/documentation/coreservices/kdmdrivernotdisplaymgrawareerr)
- [var kDMFoundErr: Int](/documentation/coreservices/kdmfounderr)
- [var kDMGenErr: Int](/documentation/coreservices/kdmgenerr)
- [var kDMMainDisplayCannotMoveErr: Int](/documentation/coreservices/kdmmaindisplaycannotmoveerr)
- [var kDMMirroringBlocked: Int](/documentation/coreservices/kdmmirroringblocked)
- [var kDMMirroringNotOn: Int](/documentation/coreservices/kdmmirroringnoton)
- [var kDMMirroringOnAlready: Int](/documentation/coreservices/kdmmirroringonalready)
- [var kDMNoDeviceTableclothErr: Int](/documentation/coreservices/kdmnodevicetableclotherr)
- [var kDMNotFoundErr: Int](/documentation/coreservices/kdmnotfounderr)
- [var kDMSWNotInitializedErr: Int](/documentation/coreservices/kdmswnotinitializederr)
- [var kDMWrongNumberOfDisplays: Int](/documentation/coreservices/kdmwrongnumberofdisplays)
- [var kSysSWTooOld: Int](/documentation/coreservices/ksysswtooold)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559949-anonymous)

##### Constants

- [var ds32BitMode: Int](/documentation/coreservices/ds32bitmode)
- [var dsBadPatch: Int](/documentation/coreservices/dsbadpatch)
- [var dsBufPtrTooLow: Int](/documentation/coreservices/dsbufptrtoolow)
- [var dsCantHoldSystemHeap: Int](/documentation/coreservices/dscantholdsystemheap)
- [var dsDirtyDisk: Int](/documentation/coreservices/dsdirtydisk)
- [var dsForcedQuit: Int](/documentation/coreservices/dsforcedquit)
- [var dsGibblyMovedToDisabledFolder: Int](/documentation/coreservices/dsgibblymovedtodisabledfolder)
- [var dsLostConnectionToNetworkDisk: Int](/documentation/coreservices/dslostconnectiontonetworkdisk)
- [var dsMBATAPISysError: Int](/documentation/coreservices/dsmbatapisyserror)
- [var dsMBATASysError: Int](/documentation/coreservices/dsmbatasyserror)
- [var dsMBExternFlpySysError: Int](/documentation/coreservices/dsmbexternflpysyserror)
- [var dsMBFlpySysError: Int](/documentation/coreservices/dsmbflpysyserror)
- [var dsMBSysError: Int](/documentation/coreservices/dsmbsyserror)
- [var dsMacOSROMVersionTooOld: Int](/documentation/coreservices/dsmacosromversiontooold)
- [var dsMustUseFCBAccessors: Int](/documentation/coreservices/dsmustusefcbaccessors)
- [var dsNeedToWriteBootBlocks: Int](/documentation/coreservices/dsneedtowritebootblocks)
- [var dsNoFPU: Int](/documentation/coreservices/dsnofpu)
- [var dsNoPatch: Int](/documentation/coreservices/dsnopatch)
- [var dsNotEnoughRAMToBoot: Int](/documentation/coreservices/dsnotenoughramtoboot)
- [var dsOldSystem: Int](/documentation/coreservices/dsoldsystem)
- [var dsPCCardATASysError: Int](/documentation/coreservices/dspccardatasyserror)
- [var dsParityErr: Int](/documentation/coreservices/dsparityerr)
- [var dsRAMDiskTooBig: Int](/documentation/coreservices/dsramdisktoobig)
- [var dsReinsert: Int](/documentation/coreservices/dsreinsert)
- [var dsRemoveDisk: Int](/documentation/coreservices/dsremovedisk)
- [var dsSCSIWarn: Int](/documentation/coreservices/dsscsiwarn)
- [var dsShutDownOrRestart: Int](/documentation/coreservices/dsshutdownorrestart)
- [var dsShutDownOrResume: Int](/documentation/coreservices/dsshutdownorresume)
- [var dsSwitchOffOrRestart: Int](/documentation/coreservices/dsswitchofforrestart)
- [var dsSystemRequiresPowerPC: Int](/documentation/coreservices/dssystemrequirespowerpc)
- [var dsUnBootableSystem: Int](/documentation/coreservices/dsunbootablesystem)
- [var dsVMBadBackingStore: Int](/documentation/coreservices/dsvmbadbackingstore)
- [var dsVMDeferredFuncTableFull: Int](/documentation/coreservices/dsvmdeferredfunctablefull)
- [var dsWriteToSupervisorStackGuardPage: Int](/documentation/coreservices/dswritetosupervisorstackguardpage)
- [var shutDownAlert: Int](/documentation/coreservices/shutdownalert)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560005-anonymous)

##### Constants

- [var badCodecCharacterizationErr: Int](/documentation/coreservices/badcodeccharacterizationerr)
- [var codecAbortErr: Int](/documentation/coreservices/codecaborterr)
- [var codecBadDataErr: Int](/documentation/coreservices/codecbaddataerr)
- [var codecCantQueueErr: Int](/documentation/coreservices/codeccantqueueerr)
- [var codecCantWhenErr: Int](/documentation/coreservices/codeccantwhenerr)
- [var codecConditionErr: Int](/documentation/coreservices/codecconditionerr)
- [var codecDataVersErr: Int](/documentation/coreservices/codecdataverserr)
- [var codecDisabledErr: Int](/documentation/coreservices/codecdisablederr)
- [var codecDroppedFrameErr: Int](/documentation/coreservices/codecdroppedframeerr)
- [var codecErr: Int](/documentation/coreservices/codecerr)
- [var codecExtensionNotFoundErr: Int](/documentation/coreservices/codecextensionnotfounderr)
- [var codecImageBufErr: Int](/documentation/coreservices/codecimagebuferr)
- [var codecNeedAccessKeyErr: Int](/documentation/coreservices/codecneedaccesskeyerr)
- [var codecNeedToFlushChainErr: Int](/documentation/coreservices/codecneedtoflushchainerr)
- [var codecNoMemoryPleaseWaitErr: Int](/documentation/coreservices/codecnomemorypleasewaiterr)
- [var codecNothingToBlitErr: Int](/documentation/coreservices/codecnothingtobliterr)
- [var codecOffscreenFailedErr: Int](/documentation/coreservices/codecoffscreenfailederr)
- [var codecOffscreenFailedPleaseRetryErr: Int](/documentation/coreservices/codecoffscreenfailedpleaseretryerr)
- [var codecOpenErr: Int](/documentation/coreservices/codecopenerr)
- [var codecParameterDialogConfirm: Int](/documentation/coreservices/codecparameterdialogconfirm)
- [var codecScreenBufErr: Int](/documentation/coreservices/codecscreenbuferr)
- [var codecSizeErr: Int](/documentation/coreservices/codecsizeerr)
- [var codecSpoolErr: Int](/documentation/coreservices/codecspoolerr)
- [var codecUnimpErr: Int](/documentation/coreservices/codecunimperr)
- [var codecWouldOffscreenErr: Int](/documentation/coreservices/codecwouldoffscreenerr)
- [var directXObjectAlreadyExists: Int](/documentation/coreservices/directxobjectalreadyexists)
- [var lockPortBitsBadPortErr: Int](/documentation/coreservices/lockportbitsbadporterr)
- [var lockPortBitsBadSurfaceErr: Int](/documentation/coreservices/lockportbitsbadsurfaceerr)
- [var lockPortBitsSurfaceLostErr: Int](/documentation/coreservices/lockportbitssurfacelosterr)
- [var lockPortBitsWindowClippedErr: Int](/documentation/coreservices/lockportbitswindowclippederr)
- [var lockPortBitsWindowMovedErr: Int](/documentation/coreservices/lockportbitswindowmovederr)
- [var lockPortBitsWindowResizedErr: Int](/documentation/coreservices/lockportbitswindowresizederr)
- [var lockPortBitsWrongGDeviceErr: Int](/documentation/coreservices/lockportbitswronggdeviceerr)
- [var noCodecErr: Int](/documentation/coreservices/nocodecerr)
- [var noThumbnailFoundErr: Int](/documentation/coreservices/nothumbnailfounderr)
- [var scTypeNotFoundErr: Int](/documentation/coreservices/sctypenotfounderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560009-anonymous)

##### Constants

- [var badFolderDescErr: Int](/documentation/coreservices/badfolderdescerr)
- [var badRoutingSizeErr: Int](/documentation/coreservices/badroutingsizeerr)
- [var duplicateFolderDescErr: Int](/documentation/coreservices/duplicatefolderdescerr)
- [var duplicateRoutingErr: Int](/documentation/coreservices/duplicateroutingerr)
- [var invalidFolderTypeErr: Int](/documentation/coreservices/invalidfoldertypeerr)
- [var noMoreFolderDescErr: Int](/documentation/coreservices/nomorefolderdescerr)
- [var routingNotFoundErr: Int](/documentation/coreservices/routingnotfounderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559939-anonymous)

##### Constants

- [var coreFoundationUnknownErr: Int](/documentation/coreservices/corefoundationunknownerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559932-anonymous)

##### Constants

- [var numberFormattingBadCurrencyPositionErr: Int](/documentation/coreservices/numberformattingbadcurrencypositionerr)
- [var numberFormattingBadFormatErr: Int](/documentation/coreservices/numberformattingbadformaterr)
- [var numberFormattingBadNumberFormattingObjectErr: Int](/documentation/coreservices/numberformattingbadnumberformattingobjecterr)
- [var numberFormattingBadOptionsErr: Int](/documentation/coreservices/numberformattingbadoptionserr)
- [var numberFormattingBadTokenErr: Int](/documentation/coreservices/numberformattingbadtokenerr)
- [var numberFormattingDelimiterMissingErr: Int](/documentation/coreservices/numberformattingdelimitermissingerr)
- [var numberFormattingEmptyFormatErr: Int](/documentation/coreservices/numberformattingemptyformaterr)
- [var numberFormattingLiteralMissingErr: Int](/documentation/coreservices/numberformattingliteralmissingerr)
- [var numberFormattingNotADigitErr: Int](/documentation/coreservices/numberformattingnotadigiterr)
- [var numberFormattingNotANumberErr: Int](/documentation/coreservices/numberformattingnotanumbererr)
- [var numberFormattingOverflowInDestinationErr: Int](/documentation/coreservices/numberformattingoverflowindestinationerr)
- [var numberFormattingSpuriousCharErr: Int](/documentation/coreservices/numberformattingspuriouscharerr)
- [var numberFormattingUnOrderedCurrencyRangeErr: Int](/documentation/coreservices/numberformattingunorderedcurrencyrangeerr)
- [var numberFormattingUnOrdredCurrencyRangeErr: Int](/documentation/coreservices/numberformattingunordredcurrencyrangeerr)
- [var numberFortmattingNotADigitErr: Int](/documentation/coreservices/numberfortmattingnotadigiterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559993-anonymous)

##### Constants

- [var driverHardwareGoneErr: Int](/documentation/coreservices/driverhardwaregoneerr)
- [var hwParamErr: Int](/documentation/coreservices/hwparamerr)
- [var teScrapSizeErr: Int](/documentation/coreservices/tescrapsizeerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559991-anonymous)

##### Constants

- [var kNSL68kContextNotSupported: Int](/documentation/coreservices/knsl68kcontextnotsupported)
- [var kNSLBadClientInfoPtr: Int](/documentation/coreservices/knslbadclientinfoptr)
- [var kNSLBadDataTypeErr: Int](/documentation/coreservices/knslbaddatatypeerr)
- [var kNSLBadNetConnection: Int](/documentation/coreservices/knslbadnetconnection)
- [var kNSLBadProtocolTypeErr: Int](/documentation/coreservices/knslbadprotocoltypeerr)
- [var kNSLBadReferenceErr: Int](/documentation/coreservices/knslbadreferenceerr)
- [var kNSLBadServiceTypeErr: Int](/documentation/coreservices/knslbadservicetypeerr)
- [var kNSLBadURLSyntax: Int](/documentation/coreservices/knslbadurlsyntax)
- [var kNSLBufferTooSmallForData: Int](/documentation/coreservices/knslbuffertoosmallfordata)
- [var kNSLCannotContinueLookup: Int](/documentation/coreservices/knslcannotcontinuelookup)
- [var kNSLErrNullPtrError: Int](/documentation/coreservices/knslerrnullptrerror)
- [var kNSLInitializationFailed: Int](/documentation/coreservices/knslinitializationfailed)
- [var kNSLInsufficientOTVer: Int](/documentation/coreservices/knslinsufficientotver)
- [var kNSLInsufficientSysVer: Int](/documentation/coreservices/knslinsufficientsysver)
- [var kNSLInvalidPluginSpec: Int](/documentation/coreservices/knslinvalidpluginspec)
- [var kNSLNoCarbonLib: Int](/documentation/coreservices/knslnocarbonlib)
- [var kNSLNoContextAvailable: Int](/documentation/coreservices/knslnocontextavailable)
- [var kNSLNoElementsInList: Int](/documentation/coreservices/knslnoelementsinlist)
- [var kNSLNoPluginsForSearch: Int](/documentation/coreservices/knslnopluginsforsearch)
- [var kNSLNoPluginsFound: Int](/documentation/coreservices/knslnopluginsfound)
- [var kNSLNoSupportForService: Int](/documentation/coreservices/knslnosupportforservice)
- [var kNSLNotImplementedYet: Int](/documentation/coreservices/knslnotimplementedyet)
- [var kNSLNotInitialized: Int](/documentation/coreservices/knslnotinitialized)
- [var kNSLNullListPtr: Int](/documentation/coreservices/knslnulllistptr)
- [var kNSLNullNeighborhoodPtr: Int](/documentation/coreservices/knslnullneighborhoodptr)
- [var kNSLPluginLoadFailed: Int](/documentation/coreservices/knslpluginloadfailed)
- [var kNSLRequestBufferAlreadyInList: Int](/documentation/coreservices/knslrequestbufferalreadyinlist)
- [var kNSLSchedulerError: Int](/documentation/coreservices/knslschedulererror)
- [var kNSLSearchAlreadyInProgress: Int](/documentation/coreservices/knslsearchalreadyinprogress)
- [var kNSLSomePluginsFailedToLoad: Int](/documentation/coreservices/knslsomepluginsfailedtoload)
- [var kNSLUILibraryNotAvailable: Int](/documentation/coreservices/knsluilibrarynotavailable)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560066-anonymous)

##### Constants

- [var errCppGeneral: Int](/documentation/coreservices/errcppgeneral)
- [var errCppLastSystemDefinedError: Int](/documentation/coreservices/errcpplastsystemdefinederror)
- [var errCppLastUserDefinedError: Int](/documentation/coreservices/errcpplastuserdefinederror)
- [var errCppbad_alloc: Int](/documentation/coreservices/errcppbad_alloc)
- [var errCppbad_cast: Int](/documentation/coreservices/errcppbad_cast)
- [var errCppbad_exception: Int](/documentation/coreservices/errcppbad_exception)
- [var errCppbad_typeid: Int](/documentation/coreservices/errcppbad_typeid)
- [var errCppdomain_error: Int](/documentation/coreservices/errcppdomain_error)
- [var errCppinvalid_argument: Int](/documentation/coreservices/errcppinvalid_argument)
- [var errCppios_base_failure: Int](/documentation/coreservices/errcppios_base_failure)
- [var errCpplength_error: Int](/documentation/coreservices/errcpplength_error)
- [var errCpplogic_error: Int](/documentation/coreservices/errcpplogic_error)
- [var errCppout_of_range: Int](/documentation/coreservices/errcppout_of_range)
- [var errCppoverflow_error: Int](/documentation/coreservices/errcppoverflow_error)
- [var errCpprange_error: Int](/documentation/coreservices/errcpprange_error)
- [var errCppruntime_error: Int](/documentation/coreservices/errcppruntime_error)
- [var errCppunderflow_error: Int](/documentation/coreservices/errcppunderflow_error)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560065-anonymous)

##### Constants

- [var ddpLenErr: Int](/documentation/coreservices/ddplenerr)
- [var ddpSktErr: Int](/documentation/coreservices/ddpskterr)
- [var excessCollsns: Int](/documentation/coreservices/excesscollsns)
- [var lapProtErr: Int](/documentation/coreservices/lapproterr)
- [var noBridgeErr: Int](/documentation/coreservices/nobridgeerr)
- [var portInUse: Int](/documentation/coreservices/portinuse)
- [var portNotCf: Int](/documentation/coreservices/portnotcf)
- [var portNotPwr: Int](/documentation/coreservices/portnotpwr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559996-anonymous)

##### Constants

- [var eLenErr: Int](/documentation/coreservices/elenerr)
- [var eMultiErr: Int](/documentation/coreservices/emultierr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560039-anonymous)

##### Constants

- [var dsBadLibrary: Int](/documentation/coreservices/dsbadlibrary)
- [var dsMixedModeFailure: Int](/documentation/coreservices/dsmixedmodefailure)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559992-anonymous)

##### Constants

- [var kATSUBadStreamErr: Int](/documentation/coreservices/katsubadstreamerr)
- [var kATSUInvalidCallInsideCallbackErr: Int](/documentation/coreservices/katsuinvalidcallinsidecallbackerr)
- [var kATSUInvalidFontFallbacksErr: Int](/documentation/coreservices/katsuinvalidfontfallbackserr)
- [var kATSULastErr: Int](/documentation/coreservices/katsulasterr)
- [var kATSUNoFontNameErr: Int](/documentation/coreservices/katsunofontnameerr)
- [var kATSUOutputBufferTooSmallErr: Int](/documentation/coreservices/katsuoutputbuffertoosmallerr)
- [var kATSUUnsupportedStreamFormatErr: Int](/documentation/coreservices/katsuunsupportedstreamformaterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560056-anonymous)

##### Constants

- [var badATPSkt: Int](/documentation/coreservices/badatpskt)
- [var badBuffNum: Int](/documentation/coreservices/badbuffnum)
- [var cbNotFound: Int](/documentation/coreservices/cbnotfound)
- [var noDataArea: Int](/documentation/coreservices/nodataarea)
- [var noRelErr: Int](/documentation/coreservices/norelerr)
- [var noSendResp: Int](/documentation/coreservices/nosendresp)
- [var reqAborted: Int](/documentation/coreservices/reqaborted)
- [var reqFailed: Int](/documentation/coreservices/reqfailed)
- [var tooManyReqs: Int](/documentation/coreservices/toomanyreqs)
- [var tooManySkts: Int](/documentation/coreservices/toomanyskts)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560048-anonymous)

##### Constants

- [var errIAAllocationErr: Int](/documentation/coreservices/erriaallocationerr)
- [var errIABufferTooSmall: Int](/documentation/coreservices/erriabuffertoosmall)
- [var errIACanceled: Int](/documentation/coreservices/erriacanceled)
- [var errIAEndOfTextRun: Int](/documentation/coreservices/erriaendoftextrun)
- [var errIAInvalidDocument: Int](/documentation/coreservices/erriainvaliddocument)
- [var errIANoErr: Int](/documentation/coreservices/errianoerr)
- [var errIANoMoreItems: Int](/documentation/coreservices/errianomoreitems)
- [var errIAParamErr: Int](/documentation/coreservices/erriaparamerr)
- [var errIATextExtractionErr: Int](/documentation/coreservices/erriatextextractionerr)
- [var errIAUnknownErr: Int](/documentation/coreservices/erriaunknownerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560037-anonymous)

##### Constants

- [var kURL68kNotSupportedError: Int](/documentation/coreservices/kurl68knotsupportederror)
- [var kURLAccessNotAvailableError: Int](/documentation/coreservices/kurlaccessnotavailableerror)
- [var kURLAuthenticationError: Int](/documentation/coreservices/kurlauthenticationerror)
- [var kURLDestinationExistsError: Int](/documentation/coreservices/kurldestinationexistserror)
- [var kURLExtensionFailureError: Int](/documentation/coreservices/kurlextensionfailureerror)
- [var kURLFileEmptyError: Int](/documentation/coreservices/kurlfileemptyerror)
- [var kURLInvalidCallError: Int](/documentation/coreservices/kurlinvalidcallerror)
- [var kURLInvalidConfigurationError: Int](/documentation/coreservices/kurlinvalidconfigurationerror)
- [var kURLInvalidURLError: Int](/documentation/coreservices/kurlinvalidurlerror)
- [var kURLInvalidURLReferenceError: Int](/documentation/coreservices/kurlinvalidurlreferenceerror)
- [var kURLProgressAlreadyDisplayedError: Int](/documentation/coreservices/kurlprogressalreadydisplayederror)
- [var kURLPropertyBufferTooSmallError: Int](/documentation/coreservices/kurlpropertybuffertoosmallerror)
- [var kURLPropertyNotYetKnownError: Int](/documentation/coreservices/kurlpropertynotyetknownerror)
- [var kURLServerBusyError: Int](/documentation/coreservices/kurlserverbusyerror)
- [var kURLUnknownPropertyError: Int](/documentation/coreservices/kurlunknownpropertyerror)
- [var kURLUnsettablePropertyError: Int](/documentation/coreservices/kurlunsettablepropertyerror)
- [var kURLUnsupportedSchemeError: Int](/documentation/coreservices/kurlunsupportedschemeerror)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560071-anonymous)

##### Constants

- [var cDepthErr: Int](/documentation/coreservices/cdeptherr)
- [var cDevErr: Int](/documentation/coreservices/cdeverr)
- [var cMatchErr: Int](/documentation/coreservices/cmatcherr)
- [var cNoMemErr: Int](/documentation/coreservices/cnomemerr)
- [var cProtectErr: Int](/documentation/coreservices/cprotecterr)
- [var cRangeErr: Int](/documentation/coreservices/crangeerr)
- [var cResErr: Int](/documentation/coreservices/creserr)
- [var cTempMemErr: Int](/documentation/coreservices/ctempmemerr)
- [var cantLoadPickMethodErr: Int](/documentation/coreservices/cantloadpickmethoderr)
- [var colorsRequestedErr: Int](/documentation/coreservices/colorsrequestederr)
- [var pictInfoIDErr: Int](/documentation/coreservices/pictinfoiderr)
- [var pictInfoVerbErr: Int](/documentation/coreservices/pictinfoverberr)
- [var pictInfoVersionErr: Int](/documentation/coreservices/pictinfoversionerr)
- [var pictureDataErr: Int](/documentation/coreservices/picturedataerr)
- [var rgnTooBigErr: Int](/documentation/coreservices/rgntoobigerr)
- [var updPixMemErr: Int](/documentation/coreservices/updpixmemerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559948-anonymous)

##### Constants

- [var kNSpAddPlayerFailedErr: Int](/documentation/coreservices/knspaddplayerfailederr)
- [var kNSpAddressInUseErr: Int](/documentation/coreservices/knspaddressinuseerr)
- [var kNSpAlreadyAdvertisingErr: Int](/documentation/coreservices/knspalreadyadvertisingerr)
- [var kNSpAlreadyInitializedErr: Int](/documentation/coreservices/knspalreadyinitializederr)
- [var kNSpCantBlockErr: Int](/documentation/coreservices/knspcantblockerr)
- [var kNSpConnectFailedErr: Int](/documentation/coreservices/knspconnectfailederr)
- [var kNSpCreateGroupFailedErr: Int](/documentation/coreservices/knspcreategroupfailederr)
- [var kNSpFeatureNotImplementedErr: Int](/documentation/coreservices/knspfeaturenotimplementederr)
- [var kNSpFreeQExhaustedErr: Int](/documentation/coreservices/knspfreeqexhaustederr)
- [var kNSpGameTerminatedErr: Int](/documentation/coreservices/knspgameterminatederr)
- [var kNSpHostFailedErr: Int](/documentation/coreservices/knsphostfailederr)
- [var kNSpInitializationFailedErr: Int](/documentation/coreservices/knspinitializationfailederr)
- [var kNSpInvalidAddressErr: Int](/documentation/coreservices/knspinvalidaddresserr)
- [var kNSpInvalidDefinitionErr: Int](/documentation/coreservices/knspinvaliddefinitionerr)
- [var kNSpInvalidGameRefErr: Int](/documentation/coreservices/knspinvalidgamereferr)
- [var kNSpInvalidGroupIDErr: Int](/documentation/coreservices/knspinvalidgroupiderr)
- [var kNSpInvalidParameterErr: Int](/documentation/coreservices/knspinvalidparametererr)
- [var kNSpInvalidPlayerIDErr: Int](/documentation/coreservices/knspinvalidplayeriderr)
- [var kNSpInvalidProtocolListErr: Int](/documentation/coreservices/knspinvalidprotocollisterr)
- [var kNSpInvalidProtocolRefErr: Int](/documentation/coreservices/knspinvalidprotocolreferr)
- [var kNSpJoinFailedErr: Int](/documentation/coreservices/knspjoinfailederr)
- [var kNSpMemAllocationErr: Int](/documentation/coreservices/knspmemallocationerr)
- [var kNSpMessageTooBigErr: Int](/documentation/coreservices/knspmessagetoobigerr)
- [var kNSpNameRequiredErr: Int](/documentation/coreservices/knspnamerequirederr)
- [var kNSpNoGroupsErr: Int](/documentation/coreservices/knspnogroupserr)
- [var kNSpNoHostVolunteersErr: Int](/documentation/coreservices/knspnohostvolunteerserr)
- [var kNSpNoPlayersErr: Int](/documentation/coreservices/knspnoplayerserr)
- [var kNSpNotAdvertisingErr: Int](/documentation/coreservices/knspnotadvertisingerr)
- [var kNSpOTNotPresentErr: Int](/documentation/coreservices/knspotnotpresenterr)
- [var kNSpOTVersionTooOldErr: Int](/documentation/coreservices/knspotversiontooolderr)
- [var kNSpPipeFullErr: Int](/documentation/coreservices/knsppipefullerr)
- [var kNSpProtocolNotAvailableErr: Int](/documentation/coreservices/knspprotocolnotavailableerr)
- [var kNSpRemovePlayerFailedErr: Int](/documentation/coreservices/knspremoveplayerfailederr)
- [var kNSpSendFailedErr: Int](/documentation/coreservices/knspsendfailederr)
- [var kNSpTimeoutErr: Int](/documentation/coreservices/knsptimeouterr)
- [var kNSpTopologyNotSupportedErr: Int](/documentation/coreservices/knsptopologynotsupportederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559955-anonymous)

##### Constants

- [var cmCantConcatenateError: Int](/documentation/coreservices/cmcantconcatenateerror)
- [var cmCantDeleteProfile: Int](/documentation/coreservices/cmcantdeleteprofile)
- [var cmCantXYZ: Int](/documentation/coreservices/cmcantxyz)
- [var cmMethodError: Int](/documentation/coreservices/cmmethoderror)
- [var cmMethodNotFound: Int](/documentation/coreservices/cmmethodnotfound)
- [var cmNoCurrentProfile: Int](/documentation/coreservices/cmnocurrentprofile)
- [var cmProfileError: Int](/documentation/coreservices/cmprofileerror)
- [var cmProfileNotFound: Int](/documentation/coreservices/cmprofilenotfound)
- [var cmProfilesIdentical: Int](/documentation/coreservices/cmprofilesidentical)
- [var cmUnsupportedDataType: Int](/documentation/coreservices/cmunsupporteddatatype)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559965-anonymous)

##### Constants

- [var laDictionaryNotOpenedErr: Int](/documentation/coreservices/ladictionarynotopenederr)
- [var laDictionaryTooManyErr: Int](/documentation/coreservices/ladictionarytoomanyerr)
- [var laDictionaryUnknownErr: Int](/documentation/coreservices/ladictionaryunknownerr)
- [var laEngineNotFoundErr: Int](/documentation/coreservices/laenginenotfounderr)
- [var laEnvironmentBusyErr: Int](/documentation/coreservices/laenvironmentbusyerr)
- [var laEnvironmentExistErr: Int](/documentation/coreservices/laenvironmentexisterr)
- [var laEnvironmentNotFoundErr: Int](/documentation/coreservices/laenvironmentnotfounderr)
- [var laFailAnalysisErr: Int](/documentation/coreservices/lafailanalysiserr)
- [var laInvalidPathErr: Int](/documentation/coreservices/lainvalidpatherr)
- [var laNoMoreMorphemeErr: Int](/documentation/coreservices/lanomoremorphemeerr)
- [var laPropertyErr: Int](/documentation/coreservices/lapropertyerr)
- [var laPropertyIsReadOnlyErr: Int](/documentation/coreservices/lapropertyisreadonlyerr)
- [var laPropertyNotFoundErr: Int](/documentation/coreservices/lapropertynotfounderr)
- [var laPropertyUnknownErr: Int](/documentation/coreservices/lapropertyunknownerr)
- [var laPropertyValueErr: Int](/documentation/coreservices/lapropertyvalueerr)
- [var laTextOverFlowErr: Int](/documentation/coreservices/latextoverflowerr)
- [var laTooSmallBufferErr: Int](/documentation/coreservices/latoosmallbuffererr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560059-anonymous)

##### Constants

- [var errAEAccessorNotFound: Int](/documentation/coreservices/erraeaccessornotfound)
- [var errAEBadListItem: Int](/documentation/coreservices/erraebadlistitem)
- [var errAEBadTestKey: Int](/documentation/coreservices/erraebadtestkey)
- [var errAEBufferTooSmall: Int](/documentation/coreservices/erraebuffertoosmall)
- [var errAEBuildSyntaxError: Int](/documentation/coreservices/erraebuildsyntaxerror)
- [var errAECoercionFail: Int](/documentation/coreservices/erraecoercionfail)
- [var errAECorruptData: Int](/documentation/coreservices/erraecorruptdata)
- [var errAEDescIsNull: Int](/documentation/coreservices/erraedescisnull)
- [var errAEDescNotFound: Int](/documentation/coreservices/erraedescnotfound)
- [var errAEDuplicateHandler: Int](/documentation/coreservices/erraeduplicatehandler)
- [var errAEEmptyListContainer: Int](/documentation/coreservices/erraeemptylistcontainer)
- [var errAEEventFiltered: Int](/documentation/coreservices/erraeeventfiltered)
- [var errAEEventNotHandled: Int](/documentation/coreservices/erraeeventnothandled)
- [var errAEHandlerNotFound: Int](/documentation/coreservices/erraehandlernotfound)
- [var errAEIllegalIndex: Int](/documentation/coreservices/erraeillegalindex)
- [var errAEImpossibleRange: Int](/documentation/coreservices/erraeimpossiblerange)
- [var errAENegativeCount: Int](/documentation/coreservices/erraenegativecount)
- [var errAENewerVersion: Int](/documentation/coreservices/erraenewerversion)
- [var errAENoSuchLogical: Int](/documentation/coreservices/erraenosuchlogical)
- [var errAENoSuchObject: Int](/documentation/coreservices/erraenosuchobject)
- [var errAENoUserInteraction: Int](/documentation/coreservices/erraenouserinteraction)
- [var errAENotAEDesc: Int](/documentation/coreservices/erraenotaedesc)
- [var errAENotASpecialFunction: Int](/documentation/coreservices/erraenotaspecialfunction)
- [var errAENotAnObjSpec: Int](/documentation/coreservices/erraenotanobjspec)
- [var errAENotAppleEvent: Int](/documentation/coreservices/erraenotappleevent)
- [var errAEParamMissed: Int](/documentation/coreservices/erraeparammissed)
- [var errAEReceiveEscapeCurrent: Int](/documentation/coreservices/erraereceiveescapecurrent)
- [var errAEReceiveTerminate: Int](/documentation/coreservices/erraereceiveterminate)
- [var errAERecordingIsAlreadyOn: Int](/documentation/coreservices/erraerecordingisalreadyon)
- [var errAEReplyNotArrived: Int](/documentation/coreservices/erraereplynotarrived)
- [var errAEReplyNotValid: Int](/documentation/coreservices/erraereplynotvalid)
- [var errAEStreamAlreadyConverted: Int](/documentation/coreservices/erraestreamalreadyconverted)
- [var errAEStreamBadNesting: Int](/documentation/coreservices/erraestreambadnesting)
- [var errAETimeout: Int](/documentation/coreservices/erraetimeout)
- [var errAEUnknownAddressType: Int](/documentation/coreservices/erraeunknownaddresstype)
- [var errAEUnknownObjectType: Int](/documentation/coreservices/erraeunknownobjecttype)
- [var errAEUnknownSendMode: Int](/documentation/coreservices/erraeunknownsendmode)
- [var errAEWaitCanceled: Int](/documentation/coreservices/erraewaitcanceled)
- [var errAEWrongDataType: Int](/documentation/coreservices/erraewrongdatatype)
- [var errAEWrongNumberArgs: Int](/documentation/coreservices/erraewrongnumberargs)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560063-anonymous)

##### Constants

- [var kDSpConfirmSwitchWarning: Int](/documentation/coreservices/kdspconfirmswitchwarning)
- [var kDSpContextAlreadyReservedErr: Int](/documentation/coreservices/kdspcontextalreadyreservederr)
- [var kDSpContextNotFoundErr: Int](/documentation/coreservices/kdspcontextnotfounderr)
- [var kDSpContextNotReservedErr: Int](/documentation/coreservices/kdspcontextnotreservederr)
- [var kDSpFrameRateNotReadyErr: Int](/documentation/coreservices/kdspframeratenotreadyerr)
- [var kDSpInternalErr: Int](/documentation/coreservices/kdspinternalerr)
- [var kDSpInvalidAttributesErr: Int](/documentation/coreservices/kdspinvalidattributeserr)
- [var kDSpInvalidContextErr: Int](/documentation/coreservices/kdspinvalidcontexterr)
- [var kDSpNotInitializedErr: Int](/documentation/coreservices/kdspnotinitializederr)
- [var kDSpStereoContextErr: Int](/documentation/coreservices/kdspstereocontexterr)
- [var kDSpSystemSWTooOldErr: Int](/documentation/coreservices/kdspsystemswtooolderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559994-anonymous)

##### Constants

- [var errKCAuthFailed: Int](/documentation/coreservices/errkcauthfailed)
- [var errKCBufferTooSmall: Int](/documentation/coreservices/errkcbuffertoosmall)
- [var errKCCreateChainFailed: Int](/documentation/coreservices/errkccreatechainfailed)
- [var errKCDataNotAvailable: Int](/documentation/coreservices/errkcdatanotavailable)
- [var errKCDataNotModifiable: Int](/documentation/coreservices/errkcdatanotmodifiable)
- [var errKCDataTooLarge: Int](/documentation/coreservices/errkcdatatoolarge)
- [var errKCDuplicateCallback: Int](/documentation/coreservices/errkcduplicatecallback)
- [var errKCDuplicateItem: Int](/documentation/coreservices/errkcduplicateitem)
- [var errKCDuplicateKeychain: Int](/documentation/coreservices/errkcduplicatekeychain)
- [var errKCInteractionNotAllowed: Int](/documentation/coreservices/errkcinteractionnotallowed)
- [var errKCInteractionRequired: Int](/documentation/coreservices/errkcinteractionrequired)
- [var errKCInvalidCallback: Int](/documentation/coreservices/errkcinvalidcallback)
- [var errKCInvalidItemRef: Int](/documentation/coreservices/errkcinvaliditemref)
- [var errKCInvalidKeychain: Int](/documentation/coreservices/errkcinvalidkeychain)
- [var errKCInvalidSearchRef: Int](/documentation/coreservices/errkcinvalidsearchref)
- [var errKCItemNotFound: Int](/documentation/coreservices/errkcitemnotfound)
- [var errKCKeySizeNotAllowed: Int](/documentation/coreservices/errkckeysizenotallowed)
- [var errKCNoCertificateModule: Int](/documentation/coreservices/errkcnocertificatemodule)
- [var errKCNoDefaultKeychain: Int](/documentation/coreservices/errkcnodefaultkeychain)
- [var errKCNoPolicyModule: Int](/documentation/coreservices/errkcnopolicymodule)
- [var errKCNoStorageModule: Int](/documentation/coreservices/errkcnostoragemodule)
- [var errKCNoSuchAttr: Int](/documentation/coreservices/errkcnosuchattr)
- [var errKCNoSuchClass: Int](/documentation/coreservices/errkcnosuchclass)
- [var errKCNoSuchKeychain: Int](/documentation/coreservices/errkcnosuchkeychain)
- [var errKCNotAvailable: Int](/documentation/coreservices/errkcnotavailable)
- [var errKCReadOnly: Int](/documentation/coreservices/errkcreadonly)
- [var errKCReadOnlyAttr: Int](/documentation/coreservices/errkcreadonlyattr)
- [var errKCWrongKCVersion: Int](/documentation/coreservices/errkcwrongkcversion)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559964-anonymous)

##### Constants

- [var badMDBErr: Int](/documentation/coreservices/badmdberr)
- [var badMovErr: Int](/documentation/coreservices/badmoverr)
- [var dirNFErr: Int](/documentation/coreservices/dirnferr)
- [var dupFNErr: Int](/documentation/coreservices/dupfnerr)
- [var extFSErr: Int](/documentation/coreservices/extfserr)
- [var fBsyErr: Int](/documentation/coreservices/fbsyerr)
- [var fsRnErr: Int](/documentation/coreservices/fsrnerr)
- [var gfpErr: Int](/documentation/coreservices/gfperr)
- [var noMacDskErr: Int](/documentation/coreservices/nomacdskerr)
- [var nsDrvErr: Int](/documentation/coreservices/nsdrverr)
- [var opWrErr: Int](/documentation/coreservices/opwrerr)
- [var permErr: Int](/documentation/coreservices/permerr)
- [var rfNumErr: Int](/documentation/coreservices/rfnumerr)
- [var tmwdoErr: Int](/documentation/coreservices/tmwdoerr)
- [var vLckdErr: Int](/documentation/coreservices/vlckderr)
- [var volGoneErr: Int](/documentation/coreservices/volgoneerr)
- [var volOffLinErr: Int](/documentation/coreservices/volofflinerr)
- [var volOnLinErr: Int](/documentation/coreservices/volonlinerr)
- [var wrPermErr: Int](/documentation/coreservices/wrpermerr)
- [var wrgVolTypErr: Int](/documentation/coreservices/wrgvoltyperr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560020-anonymous)

##### Constants

- [var cfragFirstReservedCode: Int](/documentation/coreservices/cfragfirstreservedcode)
- [var cfragReservedCode_1: Int](/documentation/coreservices/cfragreservedcode_1)
- [var cfragReservedCode_2: Int](/documentation/coreservices/cfragreservedcode_2)
- [var cfragReservedCode_3: Int](/documentation/coreservices/cfragreservedcode_3)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559941-anonymous)

##### Constants

- [var mmInternalError: Int](/documentation/coreservices/mminternalerror)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560076-anonymous)

##### Constants

- [var themeBadCursorIndexErr: Int](/documentation/coreservices/themebadcursorindexerr)
- [var themeBadTextColorErr: Int](/documentation/coreservices/themebadtextcolorerr)
- [var themeHasNoAccentsErr: Int](/documentation/coreservices/themehasnoaccentserr)
- [var themeInvalidBrushErr: Int](/documentation/coreservices/themeinvalidbrusherr)
- [var themeMonitorDepthNotSupportedErr: Int](/documentation/coreservices/thememonitordepthnotsupportederr)
- [var themeNoAppropriateBrushErr: Int](/documentation/coreservices/themenoappropriatebrusherr)
- [var themeProcessNotRegisteredErr: Int](/documentation/coreservices/themeprocessnotregisterederr)
- [var themeProcessRegisteredErr: Int](/documentation/coreservices/themeprocessregisterederr)
- [var themeScriptFontNotFoundErr: Int](/documentation/coreservices/themescriptfontnotfounderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560015-anonymous)

##### Constants

- [var kCollateAttributesNotFoundErr: Int](/documentation/coreservices/kcollateattributesnotfounderr)
- [var kCollateBufferTooSmall: Int](/documentation/coreservices/kcollatebuffertoosmall)
- [var kCollateInvalidChar: Int](/documentation/coreservices/kcollateinvalidchar)
- [var kCollateInvalidCollationRef: Int](/documentation/coreservices/kcollateinvalidcollationref)
- [var kCollateInvalidOptions: Int](/documentation/coreservices/kcollateinvalidoptions)
- [var kCollateMissingUnicodeTableErr: Int](/documentation/coreservices/kcollatemissingunicodetableerr)
- [var kCollatePatternNotFoundErr: Int](/documentation/coreservices/kcollatepatternnotfounderr)
- [var kCollateUnicodeConvertFailedErr: Int](/documentation/coreservices/kcollateunicodeconvertfailederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560053-anonymous)

##### Constants

- [var badFCBErr: Int](/documentation/coreservices/badfcberr)
- [var badFidErr: Int](/documentation/coreservices/badfiderr)
- [var catChangedErr: Int](/documentation/coreservices/catchangederr)
- [var desktopDamagedErr: Int](/documentation/coreservices/desktopdamagederr)
- [var diffVolErr: Int](/documentation/coreservices/diffvolerr)
- [var envBadVers: Int](/documentation/coreservices/envbadvers)
- [var envNotPresent: Int](/documentation/coreservices/envnotpresent)
- [var envVersTooBig: Int](/documentation/coreservices/envverstoobig)
- [var errFSAttributeNotFound: Int](/documentation/coreservices/errfsattributenotfound)
- [var errFSBadAllocFlags: Int](/documentation/coreservices/errfsbadallocflags)
- [var errFSBadBuffer: Int](/documentation/coreservices/errfsbadbuffer)
- [var errFSBadFSRef: Int](/documentation/coreservices/errfsbadfsref)
- [var errFSBadForkName: Int](/documentation/coreservices/errfsbadforkname)
- [var errFSBadForkRef: Int](/documentation/coreservices/errfsbadforkref)
- [var errFSBadInfoBitmap: Int](/documentation/coreservices/errfsbadinfobitmap)
- [var errFSBadItemCount: Int](/documentation/coreservices/errfsbaditemcount)
- [var errFSBadIteratorFlags: Int](/documentation/coreservices/errfsbaditeratorflags)
- [var errFSBadPosMode: Int](/documentation/coreservices/errfsbadposmode)
- [var errFSBadSearchParams: Int](/documentation/coreservices/errfsbadsearchparams)
- [var errFSForkExists: Int](/documentation/coreservices/errfsforkexists)
- [var errFSForkNotFound: Int](/documentation/coreservices/errfsforknotfound)
- [var errFSIteratorNotFound: Int](/documentation/coreservices/errfsiteratornotfound)
- [var errFSIteratorNotSupported: Int](/documentation/coreservices/errfsiteratornotsupported)
- [var errFSMissingCatInfo: Int](/documentation/coreservices/errfsmissingcatinfo)
- [var errFSMissingName: Int](/documentation/coreservices/errfsmissingname)
- [var errFSNameTooLong: Int](/documentation/coreservices/errfsnametoolong)
- [var errFSNoMoreItems: Int](/documentation/coreservices/errfsnomoreitems)
- [var errFSNotAFolder: Int](/documentation/coreservices/errfsnotafolder)
- [var errFSNotEnoughSpaceForOperation: Int](/documentation/coreservices/errfsnotenoughspaceforoperation)
- [var errFSOperationNotSupported: Int](/documentation/coreservices/errfsoperationnotsupported)
- [var errFSPropertyNotValid: Int](/documentation/coreservices/errfspropertynotvalid)
- [var errFSQuotaExceeded: Int](/documentation/coreservices/errfsquotaexceeded)
- [var errFSRefsDifferent: Int](/documentation/coreservices/errfsrefsdifferent)
- [var errFSUnknownCall: Int](/documentation/coreservices/errfsunknowncall)
- [var fidExists: Int](/documentation/coreservices/fidexists)
- [var fidNotFound: Int](/documentation/coreservices/fidnotfound)
- [var fileBoundsErr: Int](/documentation/coreservices/fileboundserr)
- [var firstDskErr: Int](/documentation/coreservices/firstdskerr)
- [var fontDecError: Int](/documentation/coreservices/fontdecerror)
- [var fontNotDeclared: Int](/documentation/coreservices/fontnotdeclared)
- [var fontNotOutlineErr: Int](/documentation/coreservices/fontnotoutlineerr)
- [var fontSubErr: Int](/documentation/coreservices/fontsuberr)
- [var fsDataTooBigErr: Int](/documentation/coreservices/fsdatatoobigerr)
- [var lastDskErr: Int](/documentation/coreservices/lastdskerr)
- [var noDriveErr: Int](/documentation/coreservices/nodriveerr)
- [var noNybErr: Int](/documentation/coreservices/nonyberr)
- [var notAFileErr: Int](/documentation/coreservices/notafileerr)
- [var notARemountErr: Int](/documentation/coreservices/notaremounterr)
- [var offLinErr: Int](/documentation/coreservices/offlinerr)
- [var sameFileErr: Int](/documentation/coreservices/samefileerr)
- [var volVMBusyErr: Int](/documentation/coreservices/volvmbusyerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560011-anonymous)

##### Constants

- [var kQTSSUnknownErr: Int](/documentation/coreservices/kqtssunknownerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559954-anonymous)

##### Constants

- [var badChannel: Int](/documentation/coreservices/badchannel)
- [var badFileFormat: Int](/documentation/coreservices/badfileformat)
- [var badFormat: Int](/documentation/coreservices/badformat)
- [var buffersTooSmall: Int](/documentation/coreservices/bufferstoosmall)
- [var channelBusy: Int](/documentation/coreservices/channelbusy)
- [var channelNotBusy: Int](/documentation/coreservices/channelnotbusy)
- [var noHardware: Int](/documentation/coreservices/nohardware)
- [var noMoreRealTime: Int](/documentation/coreservices/nomorerealtime)
- [var notEnoughBufferSpace: Int](/documentation/coreservices/notenoughbufferspace)
- [var notEnoughHardware: Int](/documentation/coreservices/notenoughhardware)
- [var queueFull: Int](/documentation/coreservices/queuefull)
- [var resProblem: Int](/documentation/coreservices/resproblem)
- [var siBadDeviceName: Int](/documentation/coreservices/sibaddevicename)
- [var siBadRefNum: Int](/documentation/coreservices/sibadrefnum)
- [var siBadSoundInDevice: Int](/documentation/coreservices/sibadsoundindevice)
- [var siDeviceBusyErr: Int](/documentation/coreservices/sidevicebusyerr)
- [var siHardDriveTooSlow: Int](/documentation/coreservices/siharddrivetooslow)
- [var siInputDeviceErr: Int](/documentation/coreservices/siinputdeviceerr)
- [var siInvalidCompression: Int](/documentation/coreservices/siinvalidcompression)
- [var siInvalidSampleRate: Int](/documentation/coreservices/siinvalidsamplerate)
- [var siInvalidSampleSize: Int](/documentation/coreservices/siinvalidsamplesize)
- [var siNoBufferSpecified: Int](/documentation/coreservices/sinobufferspecified)
- [var siNoSoundInHardware: Int](/documentation/coreservices/sinosoundinhardware)
- [var siUnknownInfoType: Int](/documentation/coreservices/siunknowninfotype)
- [var siUnknownQuality: Int](/documentation/coreservices/siunknownquality)
- [var siVBRCompressionNotSupported: Int](/documentation/coreservices/sivbrcompressionnotsupported)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559971-anonymous)

##### Constants

- [var kUSBNoDelay: Int](/documentation/coreservices/kusbnodelay)
- [var kUSBNoErr: Int](/documentation/coreservices/kusbnoerr)
- [var kUSBNoTran: Int](/documentation/coreservices/kusbnotran)
- [var kUSBPending: Int](/documentation/coreservices/kusbpending)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559945-anonymous)

##### Constants

- [var errASCantCompareMoreThan32k: Int](/documentation/coreservices/errascantcomparemorethan32k)
- [var errASCantConsiderAndIgnore: Int](/documentation/coreservices/errascantconsiderandignore)
- [var errASIllegalFormalParameter: Int](/documentation/coreservices/errasillegalformalparameter)
- [var errASInconsistentNames: Int](/documentation/coreservices/errasinconsistentnames)
- [var errASNoResultReturned: Int](/documentation/coreservices/errasnoresultreturned)
- [var errASParameterNotForEvent: Int](/documentation/coreservices/errasparameternotforevent)
- [var errASTerminologyNestingTooDeep: Int](/documentation/coreservices/errasterminologynestingtoodeep)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560003-anonymous)

##### Constants

- [var errAborted: Int](/documentation/coreservices/erraborted)
- [var errAttention: Int](/documentation/coreservices/errattention)
- [var errDSPQueueSize: Int](/documentation/coreservices/errdspqueuesize)
- [var errFwdReset: Int](/documentation/coreservices/errfwdreset)
- [var errOpenDenied: Int](/documentation/coreservices/erropendenied)
- [var errOpening: Int](/documentation/coreservices/erropening)
- [var errRefNum: Int](/documentation/coreservices/errrefnum)
- [var errState: Int](/documentation/coreservices/errstate)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560052-anonymous)

##### Constants

- [var kUSBAbortedError: Int](/documentation/coreservices/kusbabortederror)
- [var kUSBAlreadyOpenErr: Int](/documentation/coreservices/kusbalreadyopenerr)
- [var kUSBCompletionError: Int](/documentation/coreservices/kusbcompletionerror)
- [var kUSBDeviceBusy: Int](/documentation/coreservices/kusbdevicebusy)
- [var kUSBDeviceDisconnected: Int](/documentation/coreservices/kusbdevicedisconnected)
- [var kUSBDeviceErr: Int](/documentation/coreservices/kusbdeviceerr)
- [var kUSBDeviceNotSuspended: Int](/documentation/coreservices/kusbdevicenotsuspended)
- [var kUSBDevicePowerProblem: Int](/documentation/coreservices/kusbdevicepowerproblem)
- [var kUSBDeviceSuspended: Int](/documentation/coreservices/kusbdevicesuspended)
- [var kUSBFlagsError: Int](/documentation/coreservices/kusbflagserror)
- [var kUSBIncorrectTypeErr: Int](/documentation/coreservices/kusbincorrecttypeerr)
- [var kUSBInternalErr: Int](/documentation/coreservices/kusbinternalerr)
- [var kUSBInvalidBuffer: Int](/documentation/coreservices/kusbinvalidbuffer)
- [var kUSBNoBandwidthError: Int](/documentation/coreservices/kusbnobandwidtherror)
- [var kUSBNoDeviceErr: Int](/documentation/coreservices/kusbnodeviceerr)
- [var kUSBNotFound: Int](/documentation/coreservices/kusbnotfound)
- [var kUSBOutOfMemoryErr: Int](/documentation/coreservices/kusboutofmemoryerr)
- [var kUSBPBLengthError: Int](/documentation/coreservices/kusbpblengtherror)
- [var kUSBPBVersionError: Int](/documentation/coreservices/kusbpbversionerror)
- [var kUSBPipeIdleError: Int](/documentation/coreservices/kusbpipeidleerror)
- [var kUSBPipeStalledError: Int](/documentation/coreservices/kusbpipestallederror)
- [var kUSBPortDisabled: Int](/documentation/coreservices/kusbportdisabled)
- [var kUSBQueueAborted: Int](/documentation/coreservices/kusbqueueaborted)
- [var kUSBRqErr: Int](/documentation/coreservices/kusbrqerr)
- [var kUSBTimedOut: Int](/documentation/coreservices/kusbtimedout)
- [var kUSBTooManyPipesErr: Int](/documentation/coreservices/kusbtoomanypipeserr)
- [var kUSBTooManyTransactionsErr: Int](/documentation/coreservices/kusbtoomanytransactionserr)
- [var kUSBUnknownDeviceErr: Int](/documentation/coreservices/kusbunknowndeviceerr)
- [var kUSBUnknownInterfaceErr: Int](/documentation/coreservices/kusbunknowninterfaceerr)
- [var kUSBUnknownPipeErr: Int](/documentation/coreservices/kusbunknownpipeerr)
- [var kUSBUnknownRequestErr: Int](/documentation/coreservices/kusbunknownrequesterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559942-anonymous)

##### Constants

- [var badCallOrderErr: Int](/documentation/coreservices/badcallordererr)
- [var badDepthErr: Int](/documentation/coreservices/baddeptherr)
- [var digiUnimpErr: Int](/documentation/coreservices/digiunimperr)
- [var matrixErr: Int](/documentation/coreservices/matrixerr)
- [var noDMAErr: Int](/documentation/coreservices/nodmaerr)
- [var noMoreKeyColorsErr: Int](/documentation/coreservices/nomorekeycolorserr)
- [var notExactMatrixErr: Int](/documentation/coreservices/notexactmatrixerr)
- [var notExactSizeErr: Int](/documentation/coreservices/notexactsizeerr)
- [var qtParamErr: Int](/documentation/coreservices/qtparamerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560021-anonymous)

##### Constants

- [var kUSBInternalReserved1: Int](/documentation/coreservices/kusbinternalreserved1)
- [var kUSBInternalReserved10: Int](/documentation/coreservices/kusbinternalreserved10)
- [var kUSBInternalReserved2: Int](/documentation/coreservices/kusbinternalreserved2)
- [var kUSBInternalReserved3: Int](/documentation/coreservices/kusbinternalreserved3)
- [var kUSBInternalReserved4: Int](/documentation/coreservices/kusbinternalreserved4)
- [var kUSBInternalReserved5: Int](/documentation/coreservices/kusbinternalreserved5)
- [var kUSBInternalReserved6: Int](/documentation/coreservices/kusbinternalreserved6)
- [var kUSBInternalReserved7: Int](/documentation/coreservices/kusbinternalreserved7)
- [var kUSBInternalReserved8: Int](/documentation/coreservices/kusbinternalreserved8)
- [var kUSBInternalReserved9: Int](/documentation/coreservices/kusbinternalreserved9)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560062-anonymous)

##### Constants

- [var kSSpCantInstallErr: Int](/documentation/coreservices/ksspcantinstallerr)
- [var kSSpInternalErr: Int](/documentation/coreservices/ksspinternalerr)
- [var kSSpParallelUpVectorErr: Int](/documentation/coreservices/ksspparallelupvectorerr)
- [var kSSpScaleToZeroErr: Int](/documentation/coreservices/ksspscaletozeroerr)
- [var kSSpVersionErr: Int](/documentation/coreservices/ksspversionerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559987-anonymous)

##### Constants

- [var qtsAddressBusyErr: Int](/documentation/coreservices/qtsaddressbusyerr)
- [var qtsBadDataErr: Int](/documentation/coreservices/qtsbaddataerr)
- [var qtsBadSelectorErr: Int](/documentation/coreservices/qtsbadselectorerr)
- [var qtsBadStateErr: Int](/documentation/coreservices/qtsbadstateerr)
- [var qtsConnectionFailedErr: Int](/documentation/coreservices/qtsconnectionfailederr)
- [var qtsTimeoutErr: Int](/documentation/coreservices/qtstimeouterr)
- [var qtsTooMuchDataErr: Int](/documentation/coreservices/qtstoomuchdataerr)
- [var qtsUnknownValueErr: Int](/documentation/coreservices/qtsunknownvalueerr)
- [var qtsUnsupportedDataTypeErr: Int](/documentation/coreservices/qtsunsupporteddatatypeerr)
- [var qtsUnsupportedFeatureErr: Int](/documentation/coreservices/qtsunsupportedfeatureerr)
- [var qtsUnsupportedRateErr: Int](/documentation/coreservices/qtsunsupportedrateerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559935-anonymous)

##### Constants

- [var abortErr: Int](/documentation/coreservices/aborterr)
- [var bdNamErr: Int](/documentation/coreservices/bdnamerr)
- [var dceExtErr: Int](/documentation/coreservices/dceexterr)
- [var dirFulErr: Int](/documentation/coreservices/dirfulerr)
- [var dskFulErr: Int](/documentation/coreservices/dskfulerr)
- [var eofErr: Int](/documentation/coreservices/eoferr)
- [var fLckdErr: Int](/documentation/coreservices/flckderr)
- [var fnOpnErr: Int](/documentation/coreservices/fnopnerr)
- [var fnfErr: Int](/documentation/coreservices/fnferr)
- [var gcrOnMFMErr: Int](/documentation/coreservices/gcronmfmerr)
- [var iIOAbortErr: Int](/documentation/coreservices/iioaborterr)
- [var ioErr: Int](/documentation/coreservices/ioerr)
- [var mFulErr: Int](/documentation/coreservices/mfulerr)
- [var notOpenErr: Int](/documentation/coreservices/notopenerr)
- [var nsvErr: Int](/documentation/coreservices/nsverr)
- [var posErr: Int](/documentation/coreservices/poserr)
- [var slotNumErr: Int](/documentation/coreservices/slotnumerr)
- [var tmfoErr: Int](/documentation/coreservices/tmfoerr)
- [var unitTblFullErr: Int](/documentation/coreservices/unittblfullerr)
- [var wPrErr: Int](/documentation/coreservices/wprerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560008-anonymous)

##### Constants

- [var badDragFlavorErr: Int](/documentation/coreservices/baddragflavorerr)
- [var badDragItemErr: Int](/documentation/coreservices/baddragitemerr)
- [var badDragRefErr: Int](/documentation/coreservices/baddragreferr)
- [var badImageErr: Int](/documentation/coreservices/badimageerr)
- [var badImageRgnErr: Int](/documentation/coreservices/badimagergnerr)
- [var cantGetFlavorErr: Int](/documentation/coreservices/cantgetflavorerr)
- [var dragNotAcceptedErr: Int](/documentation/coreservices/dragnotacceptederr)
- [var duplicateFlavorErr: Int](/documentation/coreservices/duplicateflavorerr)
- [var duplicateHandlerErr: Int](/documentation/coreservices/duplicatehandlererr)
- [var handlerNotFoundErr: Int](/documentation/coreservices/handlernotfounderr)
- [var noSuitableDisplaysErr: Int](/documentation/coreservices/nosuitabledisplayserr)
- [var nonDragOriginatorErr: Int](/documentation/coreservices/nondragoriginatorerr)
- [var unsupportedForPlatformErr: Int](/documentation/coreservices/unsupportedforplatformerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560055-anonymous)

##### Constants

- [var kATSUBusyObjectErr: Int](/documentation/coreservices/katsubusyobjecterr)
- [var kATSUCoordinateOverflowErr: Int](/documentation/coreservices/katsucoordinateoverflowerr)
- [var kATSUFontsMatched: Int](/documentation/coreservices/katsufontsmatched)
- [var kATSUFontsNotMatched: Int](/documentation/coreservices/katsufontsnotmatched)
- [var kATSUInvalidAttributeSizeErr: Int](/documentation/coreservices/katsuinvalidattributesizeerr)
- [var kATSUInvalidAttributeTagErr: Int](/documentation/coreservices/katsuinvalidattributetagerr)
- [var kATSUInvalidAttributeValueErr: Int](/documentation/coreservices/katsuinvalidattributevalueerr)
- [var kATSUInvalidCacheErr: Int](/documentation/coreservices/katsuinvalidcacheerr)
- [var kATSUInvalidFontErr: Int](/documentation/coreservices/katsuinvalidfonterr)
- [var kATSUInvalidStyleErr: Int](/documentation/coreservices/katsuinvalidstyleerr)
- [var kATSUInvalidTextLayoutErr: Int](/documentation/coreservices/katsuinvalidtextlayouterr)
- [var kATSUInvalidTextRangeErr: Int](/documentation/coreservices/katsuinvalidtextrangeerr)
- [var kATSULineBreakInWord: Int](/documentation/coreservices/katsulinebreakinword)
- [var kATSULowLevelErr: Int](/documentation/coreservices/katsulowlevelerr)
- [var kATSUNoCorrespondingFontErr: Int](/documentation/coreservices/katsunocorrespondingfonterr)
- [var kATSUNoFontCmapAvailableErr: Int](/documentation/coreservices/katsunofontcmapavailableerr)
- [var kATSUNoFontScalerAvailableErr: Int](/documentation/coreservices/katsunofontscaleravailableerr)
- [var kATSUNoStyleRunsAssignedErr: Int](/documentation/coreservices/katsunostylerunsassignederr)
- [var kATSUNotSetErr: Int](/documentation/coreservices/katsunotseterr)
- [var kATSUQuickDrawTextErr: Int](/documentation/coreservices/katsuquickdrawtexterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559936-anonymous)

##### Constants

- [var dsBadLaunch: Int](/documentation/coreservices/dsbadlaunch)
- [var dsBadPatchHeader: Int](/documentation/coreservices/dsbadpatchheader)
- [var dsBadSANEOpcode: Int](/documentation/coreservices/dsbadsaneopcode)
- [var dsBadSlotInt: Int](/documentation/coreservices/dsbadslotint)
- [var dsCDEFNotFound: Int](/documentation/coreservices/dscdefnotfound)
- [var dsFSErr: Int](/documentation/coreservices/dsfserr)
- [var dsFinderErr: Int](/documentation/coreservices/dsfindererr)
- [var dsHMenuFindErr: Int](/documentation/coreservices/dshmenufinderr)
- [var dsMBarNFnd: Int](/documentation/coreservices/dsmbarnfnd)
- [var dsMDEFNotFound: Int](/documentation/coreservices/dsmdefnotfound)
- [var dsMemFullErr: Int](/documentation/coreservices/dsmemfullerr)
- [var dsNoPk3: Int](/documentation/coreservices/dsnopk3)
- [var dsNoPk4: Int](/documentation/coreservices/dsnopk4)
- [var dsNoPk5: Int](/documentation/coreservices/dsnopk5)
- [var dsNoPk6: Int](/documentation/coreservices/dsnopk6)
- [var dsNoPk7: Int](/documentation/coreservices/dsnopk7)
- [var dsStknHeap: Int](/documentation/coreservices/dsstknheap)
- [var dsWDEFNotFound: Int](/documentation/coreservices/dswdefnotfound)
- [var menuPrgErr: Int](/documentation/coreservices/menuprgerr)
- [var negZcbFreeErr: Int](/documentation/coreservices/negzcbfreeerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559981-anonymous)

##### Constants

- [var noMaskFoundErr: Int](/documentation/coreservices/nomaskfounderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560034-anonymous)

##### Constants

- [var tsmAlreadyRegisteredErr: Int](/documentation/coreservices/tsmalreadyregisterederr)
- [var tsmCantChangeForcedClassStateErr: Int](/documentation/coreservices/tsmcantchangeforcedclassstateerr)
- [var tsmCantOpenComponentErr: Int](/documentation/coreservices/tsmcantopencomponenterr)
- [var tsmComponentAlreadyOpenErr: Int](/documentation/coreservices/tsmcomponentalreadyopenerr)
- [var tsmComponentNoErr: Int](/documentation/coreservices/tsmcomponentnoerr)
- [var tsmComponentPropertyNotFoundErr: Int](/documentation/coreservices/tsmcomponentpropertynotfounderr)
- [var tsmComponentPropertyUnsupportedErr: Int](/documentation/coreservices/tsmcomponentpropertyunsupportederr)
- [var tsmDefaultIsNotInputMethodErr: Int](/documentation/coreservices/tsmdefaultisnotinputmethoderr)
- [var tsmDocNotActiveErr: Int](/documentation/coreservices/tsmdocnotactiveerr)
- [var tsmDocPropertyBufferTooSmallErr: Int](/documentation/coreservices/tsmdocpropertybuffertoosmallerr)
- [var tsmDocPropertyNotFoundErr: Int](/documentation/coreservices/tsmdocpropertynotfounderr)
- [var tsmDocumentOpenErr: Int](/documentation/coreservices/tsmdocumentopenerr)
- [var tsmInputMethodIsOldErr: Int](/documentation/coreservices/tsminputmethodisolderr)
- [var tsmInputMethodNotFoundErr: Int](/documentation/coreservices/tsminputmethodnotfounderr)
- [var tsmInputModeChangeFailedErr: Int](/documentation/coreservices/tsminputmodechangefailederr)
- [var tsmInvalidContext: Int](/documentation/coreservices/tsminvalidcontext)
- [var tsmInvalidDocIDErr: Int](/documentation/coreservices/tsminvaliddociderr)
- [var tsmNeverRegisteredErr: Int](/documentation/coreservices/tsmneverregisterederr)
- [var tsmNoHandler: Int](/documentation/coreservices/tsmnohandler)
- [var tsmNoMoreTokens: Int](/documentation/coreservices/tsmnomoretokens)
- [var tsmNoOpenTSErr: Int](/documentation/coreservices/tsmnoopentserr)
- [var tsmNoStem: Int](/documentation/coreservices/tsmnostem)
- [var tsmNotAnAppErr: Int](/documentation/coreservices/tsmnotanapperr)
- [var tsmScriptHasNoIMErr: Int](/documentation/coreservices/tsmscripthasnoimerr)
- [var tsmTSHasNoMenuErr: Int](/documentation/coreservices/tsmtshasnomenuerr)
- [var tsmTSMDocBusyErr: Int](/documentation/coreservices/tsmtsmdocbusyerr)
- [var tsmTSNotOpenErr: Int](/documentation/coreservices/tsmtsnotopenerr)
- [var tsmTextServiceNotFoundErr: Int](/documentation/coreservices/tsmtextservicenotfounderr)
- [var tsmUnknownErr: Int](/documentation/coreservices/tsmunknownerr)
- [var tsmUnsupScriptLanguageErr: Int](/documentation/coreservices/tsmunsupscriptlanguageerr)
- [var tsmUnsupportedTypeErr: Int](/documentation/coreservices/tsmunsupportedtypeerr)
- [var tsmUseInputWindowErr: Int](/documentation/coreservices/tsmuseinputwindowerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559959-anonymous)

##### Constants

- [var badProfileError: Int](/documentation/coreservices/badprofileerror)
- [var cantCreatePickerWindow: Int](/documentation/coreservices/cantcreatepickerwindow)
- [var cantLoadPackage: Int](/documentation/coreservices/cantloadpackage)
- [var cantLoadPicker: Int](/documentation/coreservices/cantloadpicker)
- [var colorSyncNotInstalled: Int](/documentation/coreservices/colorsyncnotinstalled)
- [var firstPickerError: Int](/documentation/coreservices/firstpickererror)
- [var invalidPickerType: Int](/documentation/coreservices/invalidpickertype)
- [var noHelpForItem: Int](/documentation/coreservices/nohelpforitem)
- [var pickerCantLive: Int](/documentation/coreservices/pickercantlive)
- [var pickerResourceError: Int](/documentation/coreservices/pickerresourceerror)
- [var requiredFlagsDontMatch: Int](/documentation/coreservices/requiredflagsdontmatch)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559990-anonymous)

##### Constants

- [var cantReceiveFromSynthesizerOSErr: Int](/documentation/coreservices/cantreceivefromsynthesizeroserr)
- [var cantSendToSynthesizerOSErr: Int](/documentation/coreservices/cantsendtosynthesizeroserr)
- [var illegalChannelOSErr: Int](/documentation/coreservices/illegalchanneloserr)
- [var illegalControllerOSErr: Int](/documentation/coreservices/illegalcontrolleroserr)
- [var illegalInstrumentOSErr: Int](/documentation/coreservices/illegalinstrumentoserr)
- [var illegalKnobOSErr: Int](/documentation/coreservices/illegalknoboserr)
- [var illegalKnobValueOSErr: Int](/documentation/coreservices/illegalknobvalueoserr)
- [var illegalNoteChannelOSErr: Int](/documentation/coreservices/illegalnotechanneloserr)
- [var illegalPartOSErr: Int](/documentation/coreservices/illegalpartoserr)
- [var illegalVoiceAllocationOSErr: Int](/documentation/coreservices/illegalvoiceallocationoserr)
- [var internalComponentErr: Int](/documentation/coreservices/internalcomponenterr)
- [var midiManagerAbsentOSErr: Int](/documentation/coreservices/midimanagerabsentoserr)
- [var noExportProcAvailableErr: Int](/documentation/coreservices/noexportprocavailableerr)
- [var notImplementedMusicOSErr: Int](/documentation/coreservices/notimplementedmusicoserr)
- [var noteChannelNotAllocatedOSErr: Int](/documentation/coreservices/notechannelnotallocatedoserr)
- [var synthesizerNotRespondingOSErr: Int](/documentation/coreservices/synthesizernotrespondingoserr)
- [var synthesizerOSErr: Int](/documentation/coreservices/synthesizeroserr)
- [var tuneParseOSErr: Int](/documentation/coreservices/tuneparseoserr)
- [var tunePlayerFullOSErr: Int](/documentation/coreservices/tuneplayerfulloserr)
- [var videoOutputInUseErr: Int](/documentation/coreservices/videooutputinuseerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560018-anonymous)

##### Constants

- [var kLocalesBufferTooSmallErr: Int](/documentation/coreservices/klocalesbuffertoosmallerr)
- [var kLocalesDefaultDisplayStatus: Int](/documentation/coreservices/klocalesdefaultdisplaystatus)
- [var kLocalesTableFormatErr: Int](/documentation/coreservices/klocalestableformaterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559975-anonymous)

##### Constants

- [var vmAddressNotInFileViewErr: Int](/documentation/coreservices/vmaddressnotinfileviewerr)
- [var vmBusyBackingFileErr: Int](/documentation/coreservices/vmbusybackingfileerr)
- [var vmFileViewAccessErr: Int](/documentation/coreservices/vmfileviewaccesserr)
- [var vmInvalidBackingFileIDErr: Int](/documentation/coreservices/vminvalidbackingfileiderr)
- [var vmInvalidFileViewIDErr: Int](/documentation/coreservices/vminvalidfileviewiderr)
- [var vmInvalidOwningProcessErr: Int](/documentation/coreservices/vminvalidowningprocesserr)
- [var vmMappingPrivilegesErr: Int](/documentation/coreservices/vmmappingprivilegeserr)
- [var vmNoMoreBackingFilesErr: Int](/documentation/coreservices/vmnomorebackingfileserr)
- [var vmNoMoreFileViewsErr: Int](/documentation/coreservices/vmnomorefileviewserr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560040-anonymous)

##### Constants

- [var nmTypErr: Int](/documentation/coreservices/nmtyperr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560051-anonymous)

##### Constants

- [var menuInvalidErr: Int](/documentation/coreservices/menuinvaliderr)
- [var menuItemNotFoundErr: Int](/documentation/coreservices/menuitemnotfounderr)
- [var menuNotFoundErr: Int](/documentation/coreservices/menunotfounderr)
- [var menuPropertyInvalid: Int](/documentation/coreservices/menupropertyinvalid)
- [var menuPropertyInvalidErr: Int](/documentation/coreservices/menupropertyinvaliderr)
- [var menuPropertyNotFoundErr: Int](/documentation/coreservices/menupropertynotfounderr)
- [var menuUsesSystemDefErr: Int](/documentation/coreservices/menuusessystemdeferr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560027-anonymous)

##### Constants

- [var kMPBlueBlockingErr: Int](/documentation/coreservices/kmpblueblockingerr)
- [var kMPDeletedErr: Int](/documentation/coreservices/kmpdeletederr)
- [var kMPInsufficientResourcesErr: Int](/documentation/coreservices/kmpinsufficientresourceserr)
- [var kMPInvalidIDErr: Int](/documentation/coreservices/kmpinvalididerr)
- [var kMPIterationEndErr: Int](/documentation/coreservices/kmpiterationenderr)
- [var kMPPrivilegedErr: Int](/documentation/coreservices/kmpprivilegederr)
- [var kMPProcessCreatedErr: Int](/documentation/coreservices/kmpprocesscreatederr)
- [var kMPProcessTerminatedErr: Int](/documentation/coreservices/kmpprocessterminatederr)
- [var kMPTaskAbortedErr: Int](/documentation/coreservices/kmptaskabortederr)
- [var kMPTaskBlockedErr: Int](/documentation/coreservices/kmptaskblockederr)
- [var kMPTaskCreatedErr: Int](/documentation/coreservices/kmptaskcreatederr)
- [var kMPTaskStoppedErr: Int](/documentation/coreservices/kmptaskstoppederr)
- [var kMPTimeoutErr: Int](/documentation/coreservices/kmptimeouterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560075-anonymous)

##### Constants

- [var hrHTMLRenderingLibNotInstalledErr: Int](/documentation/coreservices/hrhtmlrenderinglibnotinstallederr)
- [var hrMiscellaneousExceptionErr: Int](/documentation/coreservices/hrmiscellaneousexceptionerr)
- [var hrURLNotHandledErr: Int](/documentation/coreservices/hrurlnothandlederr)
- [var hrUnableToResizeHandleErr: Int](/documentation/coreservices/hrunabletoresizehandleerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560045-anonymous)

##### Constants

- [var kFMFontContainerAccessErr: Int](/documentation/coreservices/kfmfontcontaineraccesserr)
- [var kFMFontTableAccessErr: Int](/documentation/coreservices/kfmfonttableaccesserr)
- [var kFMInvalidFontErr: Int](/documentation/coreservices/kfminvalidfonterr)
- [var kFMInvalidFontFamilyErr: Int](/documentation/coreservices/kfminvalidfontfamilyerr)
- [var kFMIterationCompleted: Int](/documentation/coreservices/kfmiterationcompleted)
- [var kFMIterationScopeModifiedErr: Int](/documentation/coreservices/kfmiterationscopemodifiederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559938-anonymous)

##### Constants

- [var atpBadRsp: Int](/documentation/coreservices/atpbadrsp)
- [var atpLenErr: Int](/documentation/coreservices/atplenerr)
- [var buf2SmallErr: Int](/documentation/coreservices/buf2smallerr)
- [var ckSumErr: Int](/documentation/coreservices/cksumerr)
- [var extractErr: Int](/documentation/coreservices/extracterr)
- [var noMPPErr: Int](/documentation/coreservices/nompperr)
- [var readQErr: Int](/documentation/coreservices/readqerr)
- [var recNotFnd: Int](/documentation/coreservices/recnotfnd)
- [var sktClosedErr: Int](/documentation/coreservices/sktclosederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560017-anonymous)

##### Constants

- [var badDictFormat: Int](/documentation/coreservices/baddictformat)
- [var badInputText: Int](/documentation/coreservices/badinputtext)
- [var bufTooSmall: Int](/documentation/coreservices/buftoosmall)
- [var incompatibleVoice: Int](/documentation/coreservices/incompatiblevoice)
- [var noSynthFound: Int](/documentation/coreservices/nosynthfound)
- [var synthNotReady: Int](/documentation/coreservices/synthnotready)
- [var synthOpenFailed: Int](/documentation/coreservices/synthopenfailed)
- [var voiceNotFound: Int](/documentation/coreservices/voicenotfound)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559978-anonymous)

##### Constants

- [var smBLFieldBad: Int](/documentation/coreservices/smblfieldbad)
- [var smBadBoardId: Int](/documentation/coreservices/smbadboardid)
- [var smBadRefId: Int](/documentation/coreservices/smbadrefid)
- [var smBadsList: Int](/documentation/coreservices/smbadslist)
- [var smBusErrTO: Int](/documentation/coreservices/smbuserrto)
- [var smCodeRevErr: Int](/documentation/coreservices/smcodereverr)
- [var smDisposePErr: Int](/documentation/coreservices/smdisposeperr)
- [var smFHBlkDispErr: Int](/documentation/coreservices/smfhblkdisperr)
- [var smFHBlockRdErr: Int](/documentation/coreservices/smfhblockrderr)
- [var smGetPRErr: Int](/documentation/coreservices/smgetprerr)
- [var smInitStatVErr: Int](/documentation/coreservices/sminitstatverr)
- [var smInitTblVErr: Int](/documentation/coreservices/sminittblverr)
- [var smNoBoardId: Int](/documentation/coreservices/smnoboardid)
- [var smNoBoardSRsrc: Int](/documentation/coreservices/smnoboardsrsrc)
- [var smNoJmpTbl: Int](/documentation/coreservices/smnojmptbl)
- [var smReservedErr: Int](/documentation/coreservices/smreservederr)
- [var smReservedSlot: Int](/documentation/coreservices/smreservedslot)
- [var smResrvErr: Int](/documentation/coreservices/smresrverr)
- [var smUnExBusErr: Int](/documentation/coreservices/smunexbuserr)
- [var svDisabled: Int](/documentation/coreservices/svdisabled)
- [var svTempDisable: Int](/documentation/coreservices/svtempdisable)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559958-anonymous)

##### Constants

- [var gestaltDupSelectorErr: Int](/documentation/coreservices/gestaltdupselectorerr)
- [var gestaltLocationErr: Int](/documentation/coreservices/gestaltlocationerr)
- [var gestaltUndefSelectorErr: Int](/documentation/coreservices/gestaltundefselectorerr)
- [var gestaltUnknownErr: Int](/documentation/coreservices/gestaltunknownerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560069-anonymous)

##### Constants

- [var badComponentInstance: Int](/documentation/coreservices/badcomponentinstance)
- [var badComponentSelector: Int](/documentation/coreservices/badcomponentselector)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559956-anonymous)

##### Constants

- [var controlHandleInvalidErr: Int](/documentation/coreservices/controlhandleinvaliderr)
- [var controlInvalidDataVersionErr: Int](/documentation/coreservices/controlinvaliddataversionerr)
- [var controlPropertyInvalid: Int](/documentation/coreservices/controlpropertyinvalid)
- [var controlPropertyNotFoundErr: Int](/documentation/coreservices/controlpropertynotfounderr)
- [var errCantEmbedIntoSelf: Int](/documentation/coreservices/errcantembedintoself)
- [var errCantEmbedRoot: Int](/documentation/coreservices/errcantembedroot)
- [var errControlDoesntSupportFocus: Int](/documentation/coreservices/errcontroldoesntsupportfocus)
- [var errControlHiddenOrDisabled: Int](/documentation/coreservices/errcontrolhiddenordisabled)
- [var errControlIsNotEmbedder: Int](/documentation/coreservices/errcontrolisnotembedder)
- [var errControlsAlreadyExist: Int](/documentation/coreservices/errcontrolsalreadyexist)
- [var errCouldntSetFocus: Int](/documentation/coreservices/errcouldntsetfocus)
- [var errDataNotSupported: Int](/documentation/coreservices/errdatanotsupported)
- [var errDataSizeMismatch: Int](/documentation/coreservices/errdatasizemismatch)
- [var errInvalidPartCode: Int](/documentation/coreservices/errinvalidpartcode)
- [var errItemNotControl: Int](/documentation/coreservices/erritemnotcontrol)
- [var errMessageNotSupported: Int](/documentation/coreservices/errmessagenotsupported)
- [var errNoRootControl: Int](/documentation/coreservices/errnorootcontrol)
- [var errRootAlreadyExists: Int](/documentation/coreservices/errrootalreadyexists)
- [var errUnknownControl: Int](/documentation/coreservices/errunknowncontrol)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560057-anonymous)

##### Constants

- [var kISpBufferToSmallErr: Int](/documentation/coreservices/kispbuffertosmallerr)
- [var kISpDeviceActiveErr: Int](/documentation/coreservices/kispdeviceactiveerr)
- [var kISpDeviceInactiveErr: Int](/documentation/coreservices/kispdeviceinactiveerr)
- [var kISpElementInListErr: Int](/documentation/coreservices/kispelementinlisterr)
- [var kISpElementNotInListErr: Int](/documentation/coreservices/kispelementnotinlisterr)
- [var kISpInternalErr: Int](/documentation/coreservices/kispinternalerr)
- [var kISpListBusyErr: Int](/documentation/coreservices/kisplistbusyerr)
- [var kISpSystemActiveErr: Int](/documentation/coreservices/kispsystemactiveerr)
- [var kISpSystemInactiveErr: Int](/documentation/coreservices/kispsysteminactiveerr)
- [var kISpSystemListErr: Int](/documentation/coreservices/kispsystemlisterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559970-anonymous)

##### Constants

- [var kFBCaccessCanceled: Int](/documentation/coreservices/kfbcaccesscanceled)
- [var kFBCaccessorStoreFailed: Int](/documentation/coreservices/kfbcaccessorstorefailed)
- [var kFBCaddDocFailed: Int](/documentation/coreservices/kfbcadddocfailed)
- [var kFBCallocFailed: Int](/documentation/coreservices/kfbcallocfailed)
- [var kFBCanalysisNotAvailable: Int](/documentation/coreservices/kfbcanalysisnotavailable)
- [var kFBCbadIndexFile: Int](/documentation/coreservices/kfbcbadindexfile)
- [var kFBCbadIndexFileVersion: Int](/documentation/coreservices/kfbcbadindexfileversion)
- [var kFBCbadParam: Int](/documentation/coreservices/kfbcbadparam)
- [var kFBCbadSearchSession: Int](/documentation/coreservices/kfbcbadsearchsession)
- [var kFBCcommitFailed: Int](/documentation/coreservices/kfbccommitfailed)
- [var kFBCcompactionFailed: Int](/documentation/coreservices/kfbccompactionfailed)
- [var kFBCdeletionFailed: Int](/documentation/coreservices/kfbcdeletionfailed)
- [var kFBCfileNotIndexed: Int](/documentation/coreservices/kfbcfilenotindexed)
- [var kFBCflushFailed: Int](/documentation/coreservices/kfbcflushfailed)
- [var kFBCillegalSessionChange: Int](/documentation/coreservices/kfbcillegalsessionchange)
- [var kFBCindexCreationFailed: Int](/documentation/coreservices/kfbcindexcreationfailed)
- [var kFBCindexDiskIOFailed: Int](/documentation/coreservices/kfbcindexdiskiofailed)
- [var kFBCindexFileDestroyed: Int](/documentation/coreservices/kfbcindexfiledestroyed)
- [var kFBCindexNotAvailable: Int](/documentation/coreservices/kfbcindexnotavailable)
- [var kFBCindexNotFound: Int](/documentation/coreservices/kfbcindexnotfound)
- [var kFBCindexingCanceled: Int](/documentation/coreservices/kfbcindexingcanceled)
- [var kFBCindexingFailed: Int](/documentation/coreservices/kfbcindexingfailed)
- [var kFBCmergingFailed: Int](/documentation/coreservices/kfbcmergingfailed)
- [var kFBCmoveFailed: Int](/documentation/coreservices/kfbcmovefailed)
- [var kFBCnoIndexesFound: Int](/documentation/coreservices/kfbcnoindexesfound)
- [var kFBCnoSearchSession: Int](/documentation/coreservices/kfbcnosearchsession)
- [var kFBCnoSuchHit: Int](/documentation/coreservices/kfbcnosuchhit)
- [var kFBCsearchFailed: Int](/documentation/coreservices/kfbcsearchfailed)
- [var kFBCsomeFilesNotIndexed: Int](/documentation/coreservices/kfbcsomefilesnotindexed)
- [var kFBCsummarizationCanceled: Int](/documentation/coreservices/kfbcsummarizationcanceled)
- [var kFBCtokenizationFailed: Int](/documentation/coreservices/kfbctokenizationfailed)
- [var kFBCvTwinExceptionErr: Int](/documentation/coreservices/kfbcvtwinexceptionerr)
- [var kFBCvalidationFailed: Int](/documentation/coreservices/kfbcvalidationfailed)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559946-anonymous)

##### Constants

- [var invalidIconRefErr: Int](/documentation/coreservices/invalidiconreferr)
- [var noIconDataAvailableErr: Int](/documentation/coreservices/noicondataavailableerr)
- [var noSuchIconErr: Int](/documentation/coreservices/nosuchiconerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559933-anonymous)

##### Constants

- [var kNavCustomControlMessageFailedErr: Int](/documentation/coreservices/knavcustomcontrolmessagefailederr)
- [var kNavInvalidCustomControlMessageErr: Int](/documentation/coreservices/knavinvalidcustomcontrolmessageerr)
- [var kNavInvalidSystemConfigErr: Int](/documentation/coreservices/knavinvalidsystemconfigerr)
- [var kNavMissingKindStringErr: Int](/documentation/coreservices/knavmissingkindstringerr)
- [var kNavWrongDialogClassErr: Int](/documentation/coreservices/knavwrongdialogclasserr)
- [var kNavWrongDialogStateErr: Int](/documentation/coreservices/knavwrongdialogstateerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560060-anonymous)

##### Constants

- [var noScrapErr: Int](/documentation/coreservices/noscraperr)
- [var noTypeErr: Int](/documentation/coreservices/notypeerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559972-anonymous)

##### Constants

- [var nrCallNotSupported: Int](/documentation/coreservices/nrcallnotsupported)
- [var nrDataTruncatedErr: Int](/documentation/coreservices/nrdatatruncatederr)
- [var nrExitedIteratorScope: Int](/documentation/coreservices/nrexitediteratorscope)
- [var nrInvalidEntryIterationOp: Int](/documentation/coreservices/nrinvalidentryiterationop)
- [var nrInvalidNodeErr: Int](/documentation/coreservices/nrinvalidnodeerr)
- [var nrIterationDone: Int](/documentation/coreservices/nriterationdone)
- [var nrLockedErr: Int](/documentation/coreservices/nrlockederr)
- [var nrNameErr: Int](/documentation/coreservices/nrnameerr)
- [var nrNotCreatedErr: Int](/documentation/coreservices/nrnotcreatederr)
- [var nrNotEnoughMemoryErr: Int](/documentation/coreservices/nrnotenoughmemoryerr)
- [var nrNotFoundErr: Int](/documentation/coreservices/nrnotfounderr)
- [var nrNotModifiedErr: Int](/documentation/coreservices/nrnotmodifiederr)
- [var nrNotSlotDeviceErr: Int](/documentation/coreservices/nrnotslotdeviceerr)
- [var nrOverrunErr: Int](/documentation/coreservices/nroverrunerr)
- [var nrPathBufferTooSmall: Int](/documentation/coreservices/nrpathbuffertoosmall)
- [var nrPathNotFound: Int](/documentation/coreservices/nrpathnotfound)
- [var nrPowerErr: Int](/documentation/coreservices/nrpowererr)
- [var nrPowerSwitchAbortErr: Int](/documentation/coreservices/nrpowerswitchaborterr)
- [var nrPropertyAlreadyExists: Int](/documentation/coreservices/nrpropertyalreadyexists)
- [var nrResultCodeBase: Int](/documentation/coreservices/nrresultcodebase)
- [var nrTransactionAborted: Int](/documentation/coreservices/nrtransactionaborted)
- [var nrTypeMismatchErr: Int](/documentation/coreservices/nrtypemismatcherr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560042-anonymous)

##### Constants

- [var sdmInitErr: Int](/documentation/coreservices/sdminiterr)
- [var sdmJTInitErr: Int](/documentation/coreservices/sdmjtiniterr)
- [var sdmPRAMInitErr: Int](/documentation/coreservices/sdmpraminiterr)
- [var sdmPriInitErr: Int](/documentation/coreservices/sdmpriiniterr)
- [var sdmSRTInitErr: Int](/documentation/coreservices/sdmsrtiniterr)
- [var siInitSDTblErr: Int](/documentation/coreservices/siinitsdtblerr)
- [var siInitSPTblErr: Int](/documentation/coreservices/siinitsptblerr)
- [var siInitVBLQsErr: Int](/documentation/coreservices/siinitvblqserr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559989-anonymous)

##### Constants

- [var kUCTSNoKeysAddedToObjectErr: Int](/documentation/coreservices/kuctsnokeysaddedtoobjecterr)
- [var kUCTSSearchListErr: Int](/documentation/coreservices/kuctssearchlisterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559995-anonymous)

##### Constants

- [var midiDupIDErr: Int](/documentation/coreservices/mididupiderr)
- [var midiInvalidCmdErr: Int](/documentation/coreservices/midiinvalidcmderr)
- [var midiNameLenErr: Int](/documentation/coreservices/midinamelenerr)
- [var midiNoClientErr: Int](/documentation/coreservices/midinoclienterr)
- [var midiNoConErr: Int](/documentation/coreservices/midinoconerr)
- [var midiNoPortErr: Int](/documentation/coreservices/midinoporterr)
- [var midiTooManyConsErr: Int](/documentation/coreservices/miditoomanyconserr)
- [var midiTooManyPortsErr: Int](/documentation/coreservices/miditoomanyportserr)
- [var midiVConnectErr: Int](/documentation/coreservices/midivconnecterr)
- [var midiVConnectMade: Int](/documentation/coreservices/midivconnectmade)
- [var midiVConnectRmvd: Int](/documentation/coreservices/midivconnectrmvd)
- [var midiWriteErr: Int](/documentation/coreservices/midiwriteerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559947-anonymous)

##### Constants

- [var smCRCFail: Int](/documentation/coreservices/smcrcfail)
- [var smDisabledSlot: Int](/documentation/coreservices/smdisabledslot)
- [var smEmptySlot: Int](/documentation/coreservices/smemptyslot)
- [var smFormatErr: Int](/documentation/coreservices/smformaterr)
- [var smNoDir: Int](/documentation/coreservices/smnodir)
- [var smNosInfoArray: Int](/documentation/coreservices/smnosinfoarray)
- [var smPRAMInitErr: Int](/documentation/coreservices/smpraminiterr)
- [var smPriInitErr: Int](/documentation/coreservices/smpriiniterr)
- [var smRevisionErr: Int](/documentation/coreservices/smrevisionerr)
- [var smSDMInitErr: Int](/documentation/coreservices/smsdminiterr)
- [var smSRTInitErr: Int](/documentation/coreservices/smsrtiniterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560073-anonymous)

##### Constants

- [var smBadsPtrErr: Int](/documentation/coreservices/smbadsptrerr)
- [var smBlkMoveErr: Int](/documentation/coreservices/smblkmoveerr)
- [var smByteLanesErr: Int](/documentation/coreservices/smbytelaneserr)
- [var smCPUErr: Int](/documentation/coreservices/smcpuerr)
- [var smCkStatusErr: Int](/documentation/coreservices/smckstatuserr)
- [var smDisDrvrNamErr: Int](/documentation/coreservices/smdisdrvrnamerr)
- [var smGetDrvrNamErr: Int](/documentation/coreservices/smgetdrvrnamerr)
- [var smNewPErr: Int](/documentation/coreservices/smnewperr)
- [var smNilsBlockErr: Int](/documentation/coreservices/smnilsblockerr)
- [var smNoGoodOpens: Int](/documentation/coreservices/smnogoodopens)
- [var smNoMoresRsrcs: Int](/documentation/coreservices/smnomoresrsrcs)
- [var smOffsetErr: Int](/documentation/coreservices/smoffseterr)
- [var smRecNotFnd: Int](/documentation/coreservices/smrecnotfnd)
- [var smSRTOvrFlErr: Int](/documentation/coreservices/smsrtovrflerr)
- [var smSelOOBErr: Int](/documentation/coreservices/smselooberr)
- [var smSlotOOBErr: Int](/documentation/coreservices/smslotooberr)
- [var smsGetDrvrErr: Int](/documentation/coreservices/smsgetdrvrerr)
- [var smsPointerNil: Int](/documentation/coreservices/smspointernil)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560068-anonymous)

##### Constants

- [var afpAccessDenied: Int](/documentation/coreservices/afpaccessdenied)
- [var afpAlreadyLoggedInErr: Int](/documentation/coreservices/afpalreadyloggedinerr)
- [var afpAuthContinue: Int](/documentation/coreservices/afpauthcontinue)
- [var afpBadIDErr: Int](/documentation/coreservices/afpbadiderr)
- [var afpBadUAM: Int](/documentation/coreservices/afpbaduam)
- [var afpBadVersNum: Int](/documentation/coreservices/afpbadversnum)
- [var afpBitmapErr: Int](/documentation/coreservices/afpbitmaperr)
- [var afpCallNotAllowed: Int](/documentation/coreservices/afpcallnotallowed)
- [var afpCallNotSupported: Int](/documentation/coreservices/afpcallnotsupported)
- [var afpCantMove: Int](/documentation/coreservices/afpcantmove)
- [var afpCantRename: Int](/documentation/coreservices/afpcantrename)
- [var afpCatalogChanged: Int](/documentation/coreservices/afpcatalogchanged)
- [var afpContainsSharedErr: Int](/documentation/coreservices/afpcontainssharederr)
- [var afpDenyConflict: Int](/documentation/coreservices/afpdenyconflict)
- [var afpDiffVolErr: Int](/documentation/coreservices/afpdiffvolerr)
- [var afpDirNotEmpty: Int](/documentation/coreservices/afpdirnotempty)
- [var afpDirNotFound: Int](/documentation/coreservices/afpdirnotfound)
- [var afpDiskFull: Int](/documentation/coreservices/afpdiskfull)
- [var afpEofError: Int](/documentation/coreservices/afpeoferror)
- [var afpFileBusy: Int](/documentation/coreservices/afpfilebusy)
- [var afpFlatVol: Int](/documentation/coreservices/afpflatvol)
- [var afpIDExists: Int](/documentation/coreservices/afpidexists)
- [var afpIDNotFound: Int](/documentation/coreservices/afpidnotfound)
- [var afpIconTypeError: Int](/documentation/coreservices/afpicontypeerror)
- [var afpInsideSharedErr: Int](/documentation/coreservices/afpinsidesharederr)
- [var afpInsideTrashErr: Int](/documentation/coreservices/afpinsidetrasherr)
- [var afpItemNotFound: Int](/documentation/coreservices/afpitemnotfound)
- [var afpLockErr: Int](/documentation/coreservices/afplockerr)
- [var afpMiscErr: Int](/documentation/coreservices/afpmiscerr)
- [var afpNoMoreLocks: Int](/documentation/coreservices/afpnomorelocks)
- [var afpNoServer: Int](/documentation/coreservices/afpnoserver)
- [var afpObjectExists: Int](/documentation/coreservices/afpobjectexists)
- [var afpObjectLocked: Int](/documentation/coreservices/afpobjectlocked)
- [var afpObjectNotFound: Int](/documentation/coreservices/afpobjectnotfound)
- [var afpObjectTypeErr: Int](/documentation/coreservices/afpobjecttypeerr)
- [var afpParmErr: Int](/documentation/coreservices/afpparmerr)
- [var afpPwdExpiredErr: Int](/documentation/coreservices/afppwdexpirederr)
- [var afpPwdNeedsChangeErr: Int](/documentation/coreservices/afppwdneedschangeerr)
- [var afpPwdPolicyErr: Int](/documentation/coreservices/afppwdpolicyerr)
- [var afpPwdSameErr: Int](/documentation/coreservices/afppwdsameerr)
- [var afpPwdTooShortErr: Int](/documentation/coreservices/afppwdtooshorterr)
- [var afpRangeNotLocked: Int](/documentation/coreservices/afprangenotlocked)
- [var afpRangeOverlap: Int](/documentation/coreservices/afprangeoverlap)
- [var afpSameObjectErr: Int](/documentation/coreservices/afpsameobjecterr)
- [var afpServerGoingDown: Int](/documentation/coreservices/afpservergoingdown)
- [var afpSessClosed: Int](/documentation/coreservices/afpsessclosed)
- [var afpTooManyFilesOpen: Int](/documentation/coreservices/afptoomanyfilesopen)
- [var afpUserNotAuth: Int](/documentation/coreservices/afpusernotauth)
- [var afpVolLocked: Int](/documentation/coreservices/afpvollocked)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559952-anonymous)

##### Constants

- [var vmBadDriver: Int](/documentation/coreservices/vmbaddriver)
- [var vmKernelMMUInitErr: Int](/documentation/coreservices/vmkernelmmuiniterr)
- [var vmMemLckdErr: Int](/documentation/coreservices/vmmemlckderr)
- [var vmMorePhysicalThanVirtualErr: Int](/documentation/coreservices/vmmorephysicalthanvirtualerr)
- [var vmNoVectorErr: Int](/documentation/coreservices/vmnovectorerr)
- [var vmOffErr: Int](/documentation/coreservices/vmofferr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560072-anonymous)

##### Constants

- [var errTaskNotFound: Int](/documentation/coreservices/errtasknotfound)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560029-anonymous)

##### Constants

- [var OSAControlFlowError: Int](/documentation/coreservices/osacontrolflowerror)
- [var OSADuplicateHandler: Int](/documentation/coreservices/osaduplicatehandler)
- [var OSADuplicateParameter: Int](/documentation/coreservices/osaduplicateparameter)
- [var OSADuplicateProperty: Int](/documentation/coreservices/osaduplicateproperty)
- [var OSAIllegalAccess: Int](/documentation/coreservices/osaillegalaccess)
- [var OSAIllegalAssign: Int](/documentation/coreservices/osaillegalassign)
- [var OSAIllegalIndex: Int](/documentation/coreservices/osaillegalindex)
- [var OSAIllegalRange: Int](/documentation/coreservices/osaillegalrange)
- [var OSAInconsistentDeclarations: Int](/documentation/coreservices/osainconsistentdeclarations)
- [var OSAMessageNotUnderstood: Int](/documentation/coreservices/osamessagenotunderstood)
- [var OSAMissingParameter: Int](/documentation/coreservices/osamissingparameter)
- [var OSAParameterMismatch: Int](/documentation/coreservices/osaparametermismatch)
- [var OSASyntaxError: Int](/documentation/coreservices/osasyntaxerror)
- [var OSASyntaxTypeError: Int](/documentation/coreservices/osasyntaxtypeerror)
- [var OSATokenTooLong: Int](/documentation/coreservices/osatokentoolong)
- [var OSAUndefinedHandler: Int](/documentation/coreservices/osaundefinedhandler)
- [var OSAUndefinedVariable: Int](/documentation/coreservices/osaundefinedvariable)
- [var errOSATypeError: Int](/documentation/coreservices/errosatypeerror)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560046-anonymous)

##### Constants

- [var callNotSupportedByNodeErr: Int](/documentation/coreservices/callnotsupportedbynodeerr)
- [var constraintReachedErr: Int](/documentation/coreservices/constraintreachederr)
- [var invalidHotSpotIDErr: Int](/documentation/coreservices/invalidhotspotiderr)
- [var invalidNodeFormatErr: Int](/documentation/coreservices/invalidnodeformaterr)
- [var invalidNodeIDErr: Int](/documentation/coreservices/invalidnodeiderr)
- [var invalidViewStateErr: Int](/documentation/coreservices/invalidviewstateerr)
- [var limitReachedErr: Int](/documentation/coreservices/limitreachederr)
- [var noMemoryNodeFailedInitialize: Int](/documentation/coreservices/nomemorynodefailedinitialize)
- [var notAQTVRMovieErr: Int](/documentation/coreservices/notaqtvrmovieerr)
- [var propertyNotSupportedByNodeErr: Int](/documentation/coreservices/propertynotsupportedbynodeerr)
- [var qtvrLibraryLoadErr: Int](/documentation/coreservices/qtvrlibraryloaderr)
- [var qtvrUninitialized: Int](/documentation/coreservices/qtvruninitialized)
- [var selectorNotSupportedByNodeErr: Int](/documentation/coreservices/selectornotsupportedbynodeerr)
- [var settingNotSupportedByNodeErr: Int](/documentation/coreservices/settingnotsupportedbynodeerr)
- [var streamingNodeNotReadyErr: Int](/documentation/coreservices/streamingnodenotreadyerr)
- [var timeNotInViewErr: Int](/documentation/coreservices/timenotinviewerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560013-anonymous)

##### Constants

- [var dcmBadDataSizeErr: Int](/documentation/coreservices/dcmbaddatasizeerr)
- [var dcmBadDictionaryErr: Int](/documentation/coreservices/dcmbaddictionaryerr)
- [var dcmBadFeatureErr: Int](/documentation/coreservices/dcmbadfeatureerr)
- [var dcmBadFieldInfoErr: Int](/documentation/coreservices/dcmbadfieldinfoerr)
- [var dcmBadFieldTypeErr: Int](/documentation/coreservices/dcmbadfieldtypeerr)
- [var dcmBadFindMethodErr: Int](/documentation/coreservices/dcmbadfindmethoderr)
- [var dcmBadKeyErr: Int](/documentation/coreservices/dcmbadkeyerr)
- [var dcmBadPropertyErr: Int](/documentation/coreservices/dcmbadpropertyerr)
- [var dcmBlockFullErr: Int](/documentation/coreservices/dcmblockfullerr)
- [var dcmBufferOverflowErr: Int](/documentation/coreservices/dcmbufferoverflowerr)
- [var dcmDictionaryBusyErr: Int](/documentation/coreservices/dcmdictionarybusyerr)
- [var dcmDictionaryNotOpenErr: Int](/documentation/coreservices/dcmdictionarynotopenerr)
- [var dcmDupRecordErr: Int](/documentation/coreservices/dcmduprecorderr)
- [var dcmIterationCompleteErr: Int](/documentation/coreservices/dcmiterationcompleteerr)
- [var dcmNecessaryFieldErr: Int](/documentation/coreservices/dcmnecessaryfielderr)
- [var dcmNoAccessMethodErr: Int](/documentation/coreservices/dcmnoaccessmethoderr)
- [var dcmNoFieldErr: Int](/documentation/coreservices/dcmnofielderr)
- [var dcmNoRecordErr: Int](/documentation/coreservices/dcmnorecorderr)
- [var dcmNotDictionaryErr: Int](/documentation/coreservices/dcmnotdictionaryerr)
- [var dcmParamErr: Int](/documentation/coreservices/dcmparamerr)
- [var dcmPermissionErr: Int](/documentation/coreservices/dcmpermissionerr)
- [var dcmProtectedErr: Int](/documentation/coreservices/dcmprotectederr)
- [var dcmTooManyKeyErr: Int](/documentation/coreservices/dcmtoomanykeyerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560038-anonymous)

##### Constants

- [var dsAddressErr: Int](/documentation/coreservices/dsaddresserr)
- [var dsBusError: Int](/documentation/coreservices/dsbuserror)
- [var dsChkErr: Int](/documentation/coreservices/dschkerr)
- [var dsCoreErr: Int](/documentation/coreservices/dscoreerr)
- [var dsFPErr: Int](/documentation/coreservices/dsfperr)
- [var dsIOCoreErr: Int](/documentation/coreservices/dsiocoreerr)
- [var dsIllInstErr: Int](/documentation/coreservices/dsillinsterr)
- [var dsIrqErr: Int](/documentation/coreservices/dsirqerr)
- [var dsLineAErr: Int](/documentation/coreservices/dslineaerr)
- [var dsLineFErr: Int](/documentation/coreservices/dslineferr)
- [var dsLoadErr: Int](/documentation/coreservices/dsloaderr)
- [var dsMiscErr: Int](/documentation/coreservices/dsmiscerr)
- [var dsNoPackErr: Int](/documentation/coreservices/dsnopackerr)
- [var dsNoPk1: Int](/documentation/coreservices/dsnopk1)
- [var dsNoPk2: Int](/documentation/coreservices/dsnopk2)
- [var dsOvflowErr: Int](/documentation/coreservices/dsovflowerr)
- [var dsPrivErr: Int](/documentation/coreservices/dspriverr)
- [var dsTraceErr: Int](/documentation/coreservices/dstraceerr)
- [var dsZeroDivErr: Int](/documentation/coreservices/dszerodiverr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559974-anonymous)

##### Constants

- [var CDEFNFnd: Int](/documentation/coreservices/cdefnfnd)
- [var dsBadStartupDisk: Int](/documentation/coreservices/dsbadstartupdisk)
- [var dsHD20Installed: Int](/documentation/coreservices/dshd20installed)
- [var dsNotThe1: Int](/documentation/coreservices/dsnotthe1)
- [var dsSystemFileErr: Int](/documentation/coreservices/dssystemfileerr)
- [var exUserBreak: Int](/documentation/coreservices/exuserbreak)
- [var fsDSIntErr: Int](/documentation/coreservices/fsdsinterr)
- [var hMenuFindErr: Int](/documentation/coreservices/hmenufinderr)
- [var mBarNFnd: Int](/documentation/coreservices/mbarnfnd)
- [var strUserBreak: Int](/documentation/coreservices/struserbreak)
- [var userBreak: Int](/documentation/coreservices/userbreak)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559961-anonymous)

##### Constants

- [var kUCOutputBufferTooSmall: Int](/documentation/coreservices/kucoutputbuffertoosmall)
- [var kUCTextBreakLocatorMissingType: Int](/documentation/coreservices/kuctextbreaklocatormissingtype)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560058-anonymous)

##### Constants

- [var WDEFNFnd: Int](/documentation/coreservices/wdefnfnd)
- [var dsDisassemblerInstalled: Int](/documentation/coreservices/dsdisassemblerinstalled)
- [var dsExtensionsDisabled: Int](/documentation/coreservices/dsextensionsdisabled)
- [var dsGreeting: Int](/documentation/coreservices/dsgreeting)
- [var dsMacsBugInstalled: Int](/documentation/coreservices/dsmacsbuginstalled)
- [var dsNoExtsDisassembler: Int](/documentation/coreservices/dsnoextsdisassembler)
- [var dsNoExtsMacsBug: Int](/documentation/coreservices/dsnoextsmacsbug)
- [var dsSysErr: Int](/documentation/coreservices/dssyserr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560006-anonymous)

##### Constants

- [var kTECArrayFullErr: Int](/documentation/coreservices/ktecarrayfullerr)
- [var kTECBadTextRunErr: Int](/documentation/coreservices/ktecbadtextrunerr)
- [var kTECBufferBelowMinimumSizeErr: Int](/documentation/coreservices/ktecbufferbelowminimumsizeerr)
- [var kTECCorruptConverterErr: Int](/documentation/coreservices/kteccorruptconvertererr)
- [var kTECDirectionErr: Int](/documentation/coreservices/ktecdirectionerr)
- [var kTECGlobalsUnavailableErr: Int](/documentation/coreservices/ktecglobalsunavailableerr)
- [var kTECIncompleteElementErr: Int](/documentation/coreservices/ktecincompleteelementerr)
- [var kTECItemUnavailableErr: Int](/documentation/coreservices/ktecitemunavailableerr)
- [var kTECMissingTableErr: Int](/documentation/coreservices/ktecmissingtableerr)
- [var kTECNeedFlushStatus: Int](/documentation/coreservices/ktecneedflushstatus)
- [var kTECNoConversionPathErr: Int](/documentation/coreservices/ktecnoconversionpatherr)
- [var kTECOutputBufferFullStatus: Int](/documentation/coreservices/ktecoutputbufferfullstatus)
- [var kTECPartialCharErr: Int](/documentation/coreservices/ktecpartialcharerr)
- [var kTECTableChecksumErr: Int](/documentation/coreservices/ktectablechecksumerr)
- [var kTECTableFormatErr: Int](/documentation/coreservices/ktectableformaterr)
- [var kTECUnmappableElementErr: Int](/documentation/coreservices/ktecunmappableelementerr)
- [var kTECUsedFallbacksStatus: Int](/documentation/coreservices/ktecusedfallbacksstatus)
- [var kTextMalformedInputErr: Int](/documentation/coreservices/ktextmalformedinputerr)
- [var kTextUndefinedElementErr: Int](/documentation/coreservices/ktextundefinedelementerr)
- [var kTextUnsupportedEncodingErr: Int](/documentation/coreservices/ktextunsupportedencodingerr)
- [var unicodeBufErr: Int](/documentation/coreservices/unicodebuferr)
- [var unicodeCharErr: Int](/documentation/coreservices/unicodecharerr)
- [var unicodeChecksumErr: Int](/documentation/coreservices/unicodechecksumerr)
- [var unicodeContextualErr: Int](/documentation/coreservices/unicodecontextualerr)
- [var unicodeDirectionErr: Int](/documentation/coreservices/unicodedirectionerr)
- [var unicodeElementErr: Int](/documentation/coreservices/unicodeelementerr)
- [var unicodeFallbacksErr: Int](/documentation/coreservices/unicodefallbackserr)
- [var unicodeNoTableErr: Int](/documentation/coreservices/unicodenotableerr)
- [var unicodeNotFoundErr: Int](/documentation/coreservices/unicodenotfounderr)
- [var unicodePartConvertErr: Int](/documentation/coreservices/unicodepartconverterr)
- [var unicodeTableFormatErr: Int](/documentation/coreservices/unicodetableformaterr)
- [var unicodeTextEncodingDataErr: Int](/documentation/coreservices/unicodetextencodingdataerr)
- [var unicodeVariantErr: Int](/documentation/coreservices/unicodevarianterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560043-anonymous)

##### Constants

- [var kModemOutOfMemory: Int](/documentation/coreservices/kmodemoutofmemory)
- [var kModemPreferencesMissing: Int](/documentation/coreservices/kmodempreferencesmissing)
- [var kModemScriptMissing: Int](/documentation/coreservices/kmodemscriptmissing)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559966-anonymous)

##### Constants

- [var componentDllEntryNotFoundErr: Int](/documentation/coreservices/componentdllentrynotfounderr)
- [var componentDllLoadErr: Int](/documentation/coreservices/componentdllloaderr)
- [var componentNotThreadSafeErr: Int](/documentation/coreservices/componentnotthreadsafeerr)
- [var qtmlDllEntryNotFoundErr: Int](/documentation/coreservices/qtmldllentrynotfounderr)
- [var qtmlDllLoadErr: Int](/documentation/coreservices/qtmldllloaderr)
- [var qtmlUninitialized: Int](/documentation/coreservices/qtmluninitialized)
- [var unsupportedOSErr: Int](/documentation/coreservices/unsupportedoserr)
- [var unsupportedProcessorErr: Int](/documentation/coreservices/unsupportedprocessorerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559969-anonymous)

##### Constants

- [var kHIDBadLogPhysValuesErr: Int](/documentation/coreservices/khidbadlogphysvalueserr)
- [var kHIDBadLogicalMaximumErr: Int](/documentation/coreservices/khidbadlogicalmaximumerr)
- [var kHIDBadLogicalMinimumErr: Int](/documentation/coreservices/khidbadlogicalminimumerr)
- [var kHIDBadParameterErr: Int](/documentation/coreservices/khidbadparametererr)
- [var kHIDBaseError: Int](/documentation/coreservices/khidbaseerror)
- [var kHIDBufferTooSmallErr: Int](/documentation/coreservices/khidbuffertoosmallerr)
- [var kHIDEndOfDescriptorErr: Int](/documentation/coreservices/khidendofdescriptorerr)
- [var kHIDIncompatibleReportErr: Int](/documentation/coreservices/khidincompatiblereporterr)
- [var kHIDInvalidPreparsedDataErr: Int](/documentation/coreservices/khidinvalidpreparseddataerr)
- [var kHIDInvalidRangePageErr: Int](/documentation/coreservices/khidinvalidrangepageerr)
- [var kHIDInvalidReportLengthErr: Int](/documentation/coreservices/khidinvalidreportlengtherr)
- [var kHIDInvalidReportTypeErr: Int](/documentation/coreservices/khidinvalidreporttypeerr)
- [var kHIDInvertedLogicalRangeErr: Int](/documentation/coreservices/khidinvertedlogicalrangeerr)
- [var kHIDInvertedPhysicalRangeErr: Int](/documentation/coreservices/khidinvertedphysicalrangeerr)
- [var kHIDInvertedUsageRangeErr: Int](/documentation/coreservices/khidinvertedusagerangeerr)
- [var kHIDNotEnoughMemoryErr: Int](/documentation/coreservices/khidnotenoughmemoryerr)
- [var kHIDNotValueArrayErr: Int](/documentation/coreservices/khidnotvaluearrayerr)
- [var kHIDNullPointerErr: Int](/documentation/coreservices/khidnullpointererr)
- [var kHIDNullStateErr: Int](/documentation/coreservices/khidnullstateerr)
- [var kHIDReportCountZeroErr: Int](/documentation/coreservices/khidreportcountzeroerr)
- [var kHIDReportIDZeroErr: Int](/documentation/coreservices/khidreportidzeroerr)
- [var kHIDReportSizeZeroErr: Int](/documentation/coreservices/khidreportsizezeroerr)
- [var kHIDSuccess: Int](/documentation/coreservices/khidsuccess)
- [var kHIDUnmatchedDesignatorRangeErr: Int](/documentation/coreservices/khidunmatcheddesignatorrangeerr)
- [var kHIDUnmatchedStringRangeErr: Int](/documentation/coreservices/khidunmatchedstringrangeerr)
- [var kHIDUnmatchedUsageRangeErr: Int](/documentation/coreservices/khidunmatchedusagerangeerr)
- [var kHIDUsageNotFoundErr: Int](/documentation/coreservices/khidusagenotfounderr)
- [var kHIDUsagePageZeroErr: Int](/documentation/coreservices/khidusagepagezeroerr)
- [var kHIDValueOutOfRangeErr: Int](/documentation/coreservices/khidvalueoutofrangeerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559985-anonymous)

##### Constants

- [var evtNotEnb: Int](/documentation/coreservices/evtnotenb)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559998-anonymous)

##### Constants

- [var badScrapRefErr: Int](/documentation/coreservices/badscrapreferr)
- [var duplicateScrapFlavorErr: Int](/documentation/coreservices/duplicatescrapflavorerr)
- [var illegalScrapFlavorFlagsErr: Int](/documentation/coreservices/illegalscrapflavorflagserr)
- [var illegalScrapFlavorSizeErr: Int](/documentation/coreservices/illegalscrapflavorsizeerr)
- [var illegalScrapFlavorTypeErr: Int](/documentation/coreservices/illegalscrapflavortypeerr)
- [var internalScrapErr: Int](/documentation/coreservices/internalscraperr)
- [var needClearScrapErr: Int](/documentation/coreservices/needclearscraperr)
- [var nilScrapFlavorDataErr: Int](/documentation/coreservices/nilscrapflavordataerr)
- [var noScrapPromiseKeeperErr: Int](/documentation/coreservices/noscrappromisekeepererr)
- [var processStateIncorrectErr: Int](/documentation/coreservices/processstateincorrecterr)
- [var scrapFlavorFlagsMismatchErr: Int](/documentation/coreservices/scrapflavorflagsmismatcherr)
- [var scrapFlavorNotFoundErr: Int](/documentation/coreservices/scrapflavornotfounderr)
- [var scrapFlavorSizeMismatchErr: Int](/documentation/coreservices/scrapflavorsizemismatcherr)
- [var scrapPromiseNotKeptErr: Int](/documentation/coreservices/scrappromisenotkepterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560049-anonymous)

##### Constants

- [var badBtSlpErr: Int](/documentation/coreservices/badbtslperr)
- [var badCksmErr: Int](/documentation/coreservices/badcksmerr)
- [var badDBtSlp: Int](/documentation/coreservices/baddbtslp)
- [var badDCksum: Int](/documentation/coreservices/baddcksum)
- [var breakRecd: Int](/documentation/coreservices/breakrecd)
- [var cantStepErr: Int](/documentation/coreservices/cantsteperr)
- [var clkRdErr: Int](/documentation/coreservices/clkrderr)
- [var clkWrErr: Int](/documentation/coreservices/clkwrerr)
- [var dataVerErr: Int](/documentation/coreservices/datavererr)
- [var fmt1Err: Int](/documentation/coreservices/fmt1err)
- [var fmt2Err: Int](/documentation/coreservices/fmt2err)
- [var initIWMErr: Int](/documentation/coreservices/initiwmerr)
- [var noAdrMkErr: Int](/documentation/coreservices/noadrmkerr)
- [var noDtaMkErr: Int](/documentation/coreservices/nodtamkerr)
- [var prInitErr: Int](/documentation/coreservices/priniterr)
- [var prWrErr: Int](/documentation/coreservices/prwrerr)
- [var rcvrErr: Int](/documentation/coreservices/rcvrerr)
- [var sectNFErr: Int](/documentation/coreservices/sectnferr)
- [var seekErr: Int](/documentation/coreservices/seekerr)
- [var spdAdjErr: Int](/documentation/coreservices/spdadjerr)
- [var tk0BadErr: Int](/documentation/coreservices/tk0baderr)
- [var twoSideErr: Int](/documentation/coreservices/twosideerr)
- [var verErr: Int](/documentation/coreservices/vererr)
- [var wrUnderrun: Int](/documentation/coreservices/wrunderrun)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559944-anonymous)

##### Constants

- [var cannotDeferErr: Int](/documentation/coreservices/cannotdefererr)
- [var cannotMakeContiguousErr: Int](/documentation/coreservices/cannotmakecontiguouserr)
- [var interruptsMaskedErr: Int](/documentation/coreservices/interruptsmaskederr)
- [var noMMUErr: Int](/documentation/coreservices/nommuerr)
- [var notEnoughMemoryErr: Int](/documentation/coreservices/notenoughmemoryerr)
- [var notHeldErr: Int](/documentation/coreservices/nothelderr)
- [var notLockedErr: Int](/documentation/coreservices/notlockederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560007-anonymous)

##### Constants

- [var textParserBadParamErr: Int](/documentation/coreservices/textparserbadparamerr)
- [var textParserBadParserObjectErr: Int](/documentation/coreservices/textparserbadparserobjecterr)
- [var textParserBadTextEncodingErr: Int](/documentation/coreservices/textparserbadtextencodingerr)
- [var textParserBadTextLanguageErr: Int](/documentation/coreservices/textparserbadtextlanguageerr)
- [var textParserBadTokenValueErr: Int](/documentation/coreservices/textparserbadtokenvalueerr)
- [var textParserNoMoreTextErr: Int](/documentation/coreservices/textparsernomoretexterr)
- [var textParserNoMoreTokensErr: Int](/documentation/coreservices/textparsernomoretokenserr)
- [var textParserNoSuchTokenFoundErr: Int](/documentation/coreservices/textparsernosuchtokenfounderr)
- [var textParserObjectNotFoundErr: Int](/documentation/coreservices/textparserobjectnotfounderr)
- [var textParserParamErr: Int](/documentation/coreservices/textparserparamerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560025-anonymous)

##### Constants

- [var iIOAbort: Int](/documentation/coreservices/iioabort)
- [var iMemFullErr: Int](/documentation/coreservices/imemfullerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560001-anonymous)

##### Constants

- [var printerStatusOpCodeNotSupportedErr: Int](/documentation/coreservices/printerstatusopcodenotsupportederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560004-anonymous)

##### Constants

- [var debuggingDuplicateOptionErr: Int](/documentation/coreservices/debuggingduplicateoptionerr)
- [var debuggingDuplicateSignatureErr: Int](/documentation/coreservices/debuggingduplicatesignatureerr)
- [var debuggingExecutionContextErr: Int](/documentation/coreservices/debuggingexecutioncontexterr)
- [var debuggingInvalidNameErr: Int](/documentation/coreservices/debugginginvalidnameerr)
- [var debuggingInvalidOptionErr: Int](/documentation/coreservices/debugginginvalidoptionerr)
- [var debuggingInvalidSignatureErr: Int](/documentation/coreservices/debugginginvalidsignatureerr)
- [var debuggingNoCallbackErr: Int](/documentation/coreservices/debuggingnocallbackerr)
- [var debuggingNoMatchErr: Int](/documentation/coreservices/debuggingnomatcherr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560044-anonymous)

##### Constants

- [var afpAlreadyMounted: Int](/documentation/coreservices/afpalreadymounted)
- [var afpBadDirIDType: Int](/documentation/coreservices/afpbaddiridtype)
- [var afpCantMountMoreSrvre: Int](/documentation/coreservices/afpcantmountmoresrvre)
- [var afpSameNodeErr: Int](/documentation/coreservices/afpsamenodeerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560028-anonymous)

##### Constants

- [var appVersionTooOld: Int](/documentation/coreservices/appversiontooold)
- [var notAppropriateForClassic: Int](/documentation/coreservices/notappropriateforclassic)
- [var wrongApplicationPlatform: Int](/documentation/coreservices/wrongapplicationplatform)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560014-anonymous)

##### Constants

- [var dialogNoTimeoutErr: Int](/documentation/coreservices/dialognotimeouterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559984-anonymous)

##### Constants

- [var CantDecompress: Int](/documentation/coreservices/cantdecompress)
- [var addRefFailed: Int](/documentation/coreservices/addreffailed)
- [var addResFailed: Int](/documentation/coreservices/addresfailed)
- [var badExtResource: Int](/documentation/coreservices/badextresource)
- [var inputOutOfBounds: Int](/documentation/coreservices/inputoutofbounds)
- [var insufficientStackErr: Int](/documentation/coreservices/insufficientstackerr)
- [var mapReadErr: Int](/documentation/coreservices/mapreaderr)
- [var noMemForPictPlaybackErr: Int](/documentation/coreservices/nomemforpictplaybackerr)
- [var nsStackErr: Int](/documentation/coreservices/nsstackerr)
- [var pixMapTooDeepErr: Int](/documentation/coreservices/pixmaptoodeeperr)
- [var resAttrErr: Int](/documentation/coreservices/resattrerr)
- [var resFNotFound: Int](/documentation/coreservices/resfnotfound)
- [var resNotFound: Int](/documentation/coreservices/resnotfound)
- [var resourceInMemory: Int](/documentation/coreservices/resourceinmemory)
- [var rgnOverflowErr: Int](/documentation/coreservices/rgnoverflowerr)
- [var rgnTooBigError: Int](/documentation/coreservices/rgntoobigerror)
- [var rmvRefFailed: Int](/documentation/coreservices/rmvreffailed)
- [var rmvResFailed: Int](/documentation/coreservices/rmvresfailed)
- [var writingPastEnd: Int](/documentation/coreservices/writingpastend)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559967-anonymous)

##### Constants

- [var btDupRecErr: Int](/documentation/coreservices/btduprecerr)
- [var btKeyAttrErr: Int](/documentation/coreservices/btkeyattrerr)
- [var btKeyLenErr: Int](/documentation/coreservices/btkeylenerr)
- [var btNoSpace: Int](/documentation/coreservices/btnospace)
- [var btRecNotFnd: Int](/documentation/coreservices/btrecnotfnd)
- [var invalidIndexErr: Int](/documentation/coreservices/invalidindexerr)
- [var notBTree: Int](/documentation/coreservices/notbtree)
- [var recordDataTooBigErr: Int](/documentation/coreservices/recorddatatoobigerr)
- [var unknownInsertModeErr: Int](/documentation/coreservices/unknowninsertmodeerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559977-anonymous)

##### Constants

- [var kQDCorruptPICTDataErr: Int](/documentation/coreservices/kqdcorruptpictdataerr)
- [var kQDCursorAlreadyRegistered: Int](/documentation/coreservices/kqdcursoralreadyregistered)
- [var kQDCursorNotRegistered: Int](/documentation/coreservices/kqdcursornotregistered)
- [var kQDNoColorHWCursorSupport: Int](/documentation/coreservices/kqdnocolorhwcursorsupport)
- [var kQDNoPalette: Int](/documentation/coreservices/kqdnopalette)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559973-anonymous)

##### Constants

- [var errCorruptWindowDescription: Int](/documentation/coreservices/errcorruptwindowdescription)
- [var errFloatingWindowsNotInitialized: Int](/documentation/coreservices/errfloatingwindowsnotinitialized)
- [var errInvalidWindowProperty: Int](/documentation/coreservices/errinvalidwindowproperty)
- [var errInvalidWindowPtr: Int](/documentation/coreservices/errinvalidwindowptr)
- [var errInvalidWindowRef: Int](/documentation/coreservices/errinvalidwindowref)
- [var errUnrecognizedWindowClass: Int](/documentation/coreservices/errunrecognizedwindowclass)
- [var errUnsupportedWindowAttributesForClass: Int](/documentation/coreservices/errunsupportedwindowattributesforclass)
- [var errUserWantsToDragWindow: Int](/documentation/coreservices/erruserwantstodragwindow)
- [var errWindowDoesNotFitOnscreen: Int](/documentation/coreservices/errwindowdoesnotfitonscreen)
- [var errWindowDoesNotHaveProxy: Int](/documentation/coreservices/errwindowdoesnothaveproxy)
- [var errWindowDoesntSupportFocus: Int](/documentation/coreservices/errwindowdoesntsupportfocus)
- [var errWindowNotFound: Int](/documentation/coreservices/errwindownotfound)
- [var errWindowPropertyNotFound: Int](/documentation/coreservices/errwindowpropertynotfound)
- [var errWindowRegionCodeInvalid: Int](/documentation/coreservices/errwindowregioncodeinvalid)
- [var errWindowsAlreadyInitialized: Int](/documentation/coreservices/errwindowsalreadyinitialized)
- [var windowAppModalStateAlreadyExistsErr: Int](/documentation/coreservices/windowappmodalstatealreadyexistserr)
- [var windowAttributeImmutableErr: Int](/documentation/coreservices/windowattributeimmutableerr)
- [var windowAttributesConflictErr: Int](/documentation/coreservices/windowattributesconflicterr)
- [var windowGroupInvalidErr: Int](/documentation/coreservices/windowgroupinvaliderr)
- [var windowManagerInternalErr: Int](/documentation/coreservices/windowmanagerinternalerr)
- [var windowNoAppModalStateErr: Int](/documentation/coreservices/windownoappmodalstateerr)
- [var windowWrongStateErr: Int](/documentation/coreservices/windowwrongstateerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560002-anonymous)

##### Constants

- [var kBridgeSoftwareRunningCantSleep: Int](/documentation/coreservices/kbridgesoftwarerunningcantsleep)
- [var kCantReportProcessorTemperatureErr: Int](/documentation/coreservices/kcantreportprocessortemperatureerr)
- [var kNoSuchPowerSource: Int](/documentation/coreservices/knosuchpowersource)
- [var kPowerHandlerExistsForDeviceErr: Int](/documentation/coreservices/kpowerhandlerexistsfordeviceerr)
- [var kPowerHandlerNotFoundForDeviceErr: Int](/documentation/coreservices/kpowerhandlernotfoundfordeviceerr)
- [var kPowerHandlerNotFoundForProcErr: Int](/documentation/coreservices/kpowerhandlernotfoundforprocerr)
- [var kPowerMgtMessageNotHandled: Int](/documentation/coreservices/kpowermgtmessagenothandled)
- [var kPowerMgtRequestDenied: Int](/documentation/coreservices/kpowermgtrequestdenied)
- [var kProcessorTempRoutineRequiresMPLib2: Int](/documentation/coreservices/kprocessortemproutinerequiresmplib2)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559963-anonymous)

##### Constants

- [var errOSAAppNotHighLevelEventAware: Int](/documentation/coreservices/errosaappnothighleveleventaware)
- [var errOSACantAccess: Int](/documentation/coreservices/errosacantaccess)
- [var errOSACantAssign: Int](/documentation/coreservices/errosacantassign)
- [var errOSACantCoerce: Int](/documentation/coreservices/errosacantcoerce)
- [var errOSACantCreate: Int](/documentation/coreservices/errosacantcreate)
- [var errOSACantGetTerminology: Int](/documentation/coreservices/errosacantgetterminology)
- [var errOSACantLaunch: Int](/documentation/coreservices/errosacantlaunch)
- [var errOSACorruptTerminology: Int](/documentation/coreservices/errosacorruptterminology)
- [var errOSADataBlockTooLarge: Int](/documentation/coreservices/errosadatablocktoolarge)
- [var errOSADivideByZero: Int](/documentation/coreservices/errosadividebyzero)
- [var errOSAGeneralError: Int](/documentation/coreservices/errosageneralerror)
- [var errOSAInternalTableOverflow: Int](/documentation/coreservices/errosainternaltableoverflow)
- [var errOSANumericOverflow: Int](/documentation/coreservices/errosanumericoverflow)
- [var errOSAStackOverflow: Int](/documentation/coreservices/errosastackoverflow)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560047-anonymous)

##### Constants

- [var AAPNotCreatedErr: Int](/documentation/coreservices/aapnotcreatederr)
- [var AAPNotFoundErr: Int](/documentation/coreservices/aapnotfounderr)
- [var ASDBadForkErr: Int](/documentation/coreservices/asdbadforkerr)
- [var ASDBadHeaderErr: Int](/documentation/coreservices/asdbadheadererr)
- [var ASDEntryNotFoundErr: Int](/documentation/coreservices/asdentrynotfounderr)
- [var atomIndexInvalidErr: Int](/documentation/coreservices/atomindexinvaliderr)
- [var atomsNotOfSameTypeErr: Int](/documentation/coreservices/atomsnotofsametypeerr)
- [var cannotBeLeafAtomErr: Int](/documentation/coreservices/cannotbeleafatomerr)
- [var cannotFindAtomErr: Int](/documentation/coreservices/cannotfindatomerr)
- [var duplicateAtomTypeAndIDErr: Int](/documentation/coreservices/duplicateatomtypeandiderr)
- [var emptyPathErr: Int](/documentation/coreservices/emptypatherr)
- [var fileOffsetTooBigErr: Int](/documentation/coreservices/fileoffsettoobigerr)
- [var invalidAtomContainerErr: Int](/documentation/coreservices/invalidatomcontainererr)
- [var invalidAtomErr: Int](/documentation/coreservices/invalidatomerr)
- [var invalidAtomTypeErr: Int](/documentation/coreservices/invalidatomtypeerr)
- [var noPathMappingErr: Int](/documentation/coreservices/nopathmappingerr)
- [var notAllowedToSaveMovieErr: Int](/documentation/coreservices/notallowedtosavemovieerr)
- [var notEnoughDataErr: Int](/documentation/coreservices/notenoughdataerr)
- [var notLeafAtomErr: Int](/documentation/coreservices/notleafatomerr)
- [var pathNotVerifiedErr: Int](/documentation/coreservices/pathnotverifiederr)
- [var pathTooLongErr: Int](/documentation/coreservices/pathtoolongerr)
- [var qfcbNotCreatedErr: Int](/documentation/coreservices/qfcbnotcreatederr)
- [var qfcbNotFoundErr: Int](/documentation/coreservices/qfcbnotfounderr)
- [var qtActionNotHandledErr: Int](/documentation/coreservices/qtactionnothandlederr)
- [var qtNetworkAlreadyAllocatedErr: Int](/documentation/coreservices/qtnetworkalreadyallocatederr)
- [var qtXMLApplicationErr: Int](/documentation/coreservices/qtxmlapplicationerr)
- [var qtXMLParseErr: Int](/documentation/coreservices/qtxmlparseerr)
- [var unknownFormatErr: Int](/documentation/coreservices/unknownformaterr)
- [var urlDataHFTPBadNameListErr: Int](/documentation/coreservices/urldatahftpbadnamelisterr)
- [var urlDataHFTPBadPasswordErr: Int](/documentation/coreservices/urldatahftpbadpassworderr)
- [var urlDataHFTPBadUserErr: Int](/documentation/coreservices/urldatahftpbadusererr)
- [var urlDataHFTPDataConnectionErr: Int](/documentation/coreservices/urldatahftpdataconnectionerr)
- [var urlDataHFTPFilenameErr: Int](/documentation/coreservices/urldatahftpfilenameerr)
- [var urlDataHFTPNeedPasswordErr: Int](/documentation/coreservices/urldatahftpneedpassworderr)
- [var urlDataHFTPNoDirectoryErr: Int](/documentation/coreservices/urldatahftpnodirectoryerr)
- [var urlDataHFTPNoNetDriverErr: Int](/documentation/coreservices/urldatahftpnonetdrivererr)
- [var urlDataHFTPNoPasswordErr: Int](/documentation/coreservices/urldatahftpnopassworderr)
- [var urlDataHFTPPermissionsErr: Int](/documentation/coreservices/urldatahftppermissionserr)
- [var urlDataHFTPProtocolErr: Int](/documentation/coreservices/urldatahftpprotocolerr)
- [var urlDataHFTPQuotaErr: Int](/documentation/coreservices/urldatahftpquotaerr)
- [var urlDataHFTPServerDisconnectedErr: Int](/documentation/coreservices/urldatahftpserverdisconnectederr)
- [var urlDataHFTPServerErr: Int](/documentation/coreservices/urldatahftpservererr)
- [var urlDataHFTPShutdownErr: Int](/documentation/coreservices/urldatahftpshutdownerr)
- [var urlDataHFTPURLErr: Int](/documentation/coreservices/urldatahftpurlerr)
- [var urlDataHHTTPNoNetDriverErr: Int](/documentation/coreservices/urldatahhttpnonetdrivererr)
- [var urlDataHHTTPProtocolErr: Int](/documentation/coreservices/urldatahhttpprotocolerr)
- [var urlDataHHTTPRedirectErr: Int](/documentation/coreservices/urldatahhttpredirecterr)
- [var urlDataHHTTPURLErr: Int](/documentation/coreservices/urldatahhttpurlerr)
- [var wackBadFileErr: Int](/documentation/coreservices/wackbadfileerr)
- [var wackBadMetaDataErr: Int](/documentation/coreservices/wackbadmetadataerr)
- [var wackForkNotFoundErr: Int](/documentation/coreservices/wackforknotfounderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560019-anonymous)

##### Constants

- [var k16BitCardErr: Int](/documentation/coreservices/k16bitcarderr)
- [var kAlreadySavedStateErr: Int](/documentation/coreservices/kalreadysavedstateerr)
- [var kAttemptDupCardEntryErr: Int](/documentation/coreservices/kattemptdupcardentryerr)
- [var kBadAdapterErr: Int](/documentation/coreservices/kbadadaptererr)
- [var kBadArgLengthErr: Int](/documentation/coreservices/kbadarglengtherr)
- [var kBadArgsErr: Int](/documentation/coreservices/kbadargserr)
- [var kBadAttributeErr: Int](/documentation/coreservices/kbadattributeerr)
- [var kBadBaseErr: Int](/documentation/coreservices/kbadbaseerr)
- [var kBadCISErr: Int](/documentation/coreservices/kbadciserr)
- [var kBadCustomIFIDErr: Int](/documentation/coreservices/kbadcustomifiderr)
- [var kBadDeviceErr: Int](/documentation/coreservices/kbaddeviceerr)
- [var kBadEDCErr: Int](/documentation/coreservices/kbadedcerr)
- [var kBadHandleErr: Int](/documentation/coreservices/kbadhandleerr)
- [var kBadIRQErr: Int](/documentation/coreservices/kbadirqerr)
- [var kBadLinkErr: Int](/documentation/coreservices/kbadlinkerr)
- [var kBadOffsetErr: Int](/documentation/coreservices/kbadoffseterr)
- [var kBadPageErr: Int](/documentation/coreservices/kbadpageerr)
- [var kBadSizeErr: Int](/documentation/coreservices/kbadsizeerr)
- [var kBadSocketErr: Int](/documentation/coreservices/kbadsocketerr)
- [var kBadSpeedErr: Int](/documentation/coreservices/kbadspeederr)
- [var kBadTupleDataErr: Int](/documentation/coreservices/kbadtupledataerr)
- [var kBadTypeErr: Int](/documentation/coreservices/kbadtypeerr)
- [var kBadVccErr: Int](/documentation/coreservices/kbadvccerr)
- [var kBadVppErr: Int](/documentation/coreservices/kbadvpperr)
- [var kBadWindowErr: Int](/documentation/coreservices/kbadwindowerr)
- [var kBusyErr: Int](/documentation/coreservices/kbusyerr)
- [var kCantConfigureCardErr: Int](/documentation/coreservices/kcantconfigurecarderr)
- [var kCardBusCardErr: Int](/documentation/coreservices/kcardbuscarderr)
- [var kCardPowerOffErr: Int](/documentation/coreservices/kcardpowerofferr)
- [var kClientRequestDenied: Int](/documentation/coreservices/kclientrequestdenied)
- [var kConfigurationLockedErr: Int](/documentation/coreservices/kconfigurationlockederr)
- [var kGeneralFailureErr: Int](/documentation/coreservices/kgeneralfailureerr)
- [var kInUseErr: Int](/documentation/coreservices/kinuseerr)
- [var kInvalidCSClientErr: Int](/documentation/coreservices/kinvalidcsclienterr)
- [var kInvalidDeviceNumber: Int](/documentation/coreservices/kinvaliddevicenumber)
- [var kInvalidRegEntryErr: Int](/documentation/coreservices/kinvalidregentryerr)
- [var kNoCardBusCISErr: Int](/documentation/coreservices/knocardbusciserr)
- [var kNoCardEnablersFoundErr: Int](/documentation/coreservices/knocardenablersfounderr)
- [var kNoCardErr: Int](/documentation/coreservices/knocarderr)
- [var kNoCardSevicesSocketsErr: Int](/documentation/coreservices/knocardsevicessocketserr)
- [var kNoClientTableErr: Int](/documentation/coreservices/knoclienttableerr)
- [var kNoCompatibleNameErr: Int](/documentation/coreservices/knocompatiblenameerr)
- [var kNoEnablerForCardErr: Int](/documentation/coreservices/knoenablerforcarderr)
- [var kNoIOWindowRequestedErr: Int](/documentation/coreservices/knoiowindowrequestederr)
- [var kNoMoreInterruptSlotsErr: Int](/documentation/coreservices/knomoreinterruptslotserr)
- [var kNoMoreItemsErr: Int](/documentation/coreservices/knomoreitemserr)
- [var kNoMoreTimerClientsErr: Int](/documentation/coreservices/knomoretimerclientserr)
- [var kNotReadyErr: Int](/documentation/coreservices/knotreadyerr)
- [var kNotZVCapableErr: Int](/documentation/coreservices/knotzvcapableerr)
- [var kOutOfResourceErr: Int](/documentation/coreservices/koutofresourceerr)
- [var kPassCallToChainErr: Int](/documentation/coreservices/kpasscalltochainerr)
- [var kPostCardEventErr: Int](/documentation/coreservices/kpostcardeventerr)
- [var kReadFailureErr: Int](/documentation/coreservices/kreadfailureerr)
- [var kTooManyIOWindowsErr: Int](/documentation/coreservices/ktoomanyiowindowserr)
- [var kUnsupportedCardErr: Int](/documentation/coreservices/kunsupportedcarderr)
- [var kUnsupportedFunctionErr: Int](/documentation/coreservices/kunsupportedfunctionerr)
- [var kUnsupportedModeErr: Int](/documentation/coreservices/kunsupportedmodeerr)
- [var kUnsupportedVsErr: Int](/documentation/coreservices/kunsupportedvserr)
- [var kWriteFailureErr: Int](/documentation/coreservices/kwritefailureerr)
- [var kWriteProtectedErr: Int](/documentation/coreservices/kwriteprotectederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559979-anonymous)

##### Constants

- [var kIllegalClockValueErr: Int](/documentation/coreservices/killegalclockvalueerr)
- [var kUTCOverflowErr: Int](/documentation/coreservices/kutcoverflowerr)
- [var kUTCUnderflowErr: Int](/documentation/coreservices/kutcunderflowerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559957-anonymous)

##### Constants

- [var kFNSBadFlattenedSizeErr: Int](/documentation/coreservices/kfnsbadflattenedsizeerr)
- [var kFNSBadProfileVersionErr: Int](/documentation/coreservices/kfnsbadprofileversionerr)
- [var kFNSBadReferenceVersionErr: Int](/documentation/coreservices/kfnsbadreferenceversionerr)
- [var kFNSDuplicateReferenceErr: Int](/documentation/coreservices/kfnsduplicatereferenceerr)
- [var kFNSInsufficientDataErr: Int](/documentation/coreservices/kfnsinsufficientdataerr)
- [var kFNSInvalidProfileErr: Int](/documentation/coreservices/kfnsinvalidprofileerr)
- [var kFNSInvalidReferenceErr: Int](/documentation/coreservices/kfnsinvalidreferenceerr)
- [var kFNSMismatchErr: Int](/documentation/coreservices/kfnsmismatcherr)
- [var kFNSNameNotFoundErr: Int](/documentation/coreservices/kfnsnamenotfounderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560074-anonymous)

##### Constants

- [var authFailErr: Int](/documentation/coreservices/authfailerr)
- [var badLocNameErr: Int](/documentation/coreservices/badlocnameerr)
- [var badPortNameErr: Int](/documentation/coreservices/badportnameerr)
- [var badReqErr: Int](/documentation/coreservices/badreqerr)
- [var badServiceMethodErr: Int](/documentation/coreservices/badservicemethoderr)
- [var destPortErr: Int](/documentation/coreservices/destporterr)
- [var guestNotAllowedErr: Int](/documentation/coreservices/guestnotallowederr)
- [var localOnlyErr: Int](/documentation/coreservices/localonlyerr)
- [var nameTypeErr: Int](/documentation/coreservices/nametypeerr)
- [var networkErr: Int](/documentation/coreservices/networkerr)
- [var noDefaultUserErr: Int](/documentation/coreservices/nodefaultusererr)
- [var noGlobalsErr: Int](/documentation/coreservices/noglobalserr)
- [var noInformErr: Int](/documentation/coreservices/noinformerr)
- [var noMachineNameErr: Int](/documentation/coreservices/nomachinenameerr)
- [var noPortErr: Int](/documentation/coreservices/noporterr)
- [var noResponseErr: Int](/documentation/coreservices/noresponseerr)
- [var noSessionErr: Int](/documentation/coreservices/nosessionerr)
- [var noToolboxNameErr: Int](/documentation/coreservices/notoolboxnameerr)
- [var noUserNameErr: Int](/documentation/coreservices/nousernameerr)
- [var noUserRecErr: Int](/documentation/coreservices/nouserrecerr)
- [var noUserRefErr: Int](/documentation/coreservices/nouserreferr)
- [var notInitErr: Int](/documentation/coreservices/notiniterr)
- [var notLoggedInErr: Int](/documentation/coreservices/notloggedinerr)
- [var portClosedErr: Int](/documentation/coreservices/portclosederr)
- [var portNameExistsErr: Int](/documentation/coreservices/portnameexistserr)
- [var sessClosedErr: Int](/documentation/coreservices/sessclosederr)
- [var sessTableErr: Int](/documentation/coreservices/sesstableerr)
- [var userRejectErr: Int](/documentation/coreservices/userrejecterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559988-anonymous)

##### Constants

- [var rcDBAsyncNotSupp: Int](/documentation/coreservices/rcdbasyncnotsupp)
- [var rcDBBadAsyncPB: Int](/documentation/coreservices/rcdbbadasyncpb)
- [var rcDBBadDDEV: Int](/documentation/coreservices/rcdbbadddev)
- [var rcDBBadSessID: Int](/documentation/coreservices/rcdbbadsessid)
- [var rcDBBadSessNum: Int](/documentation/coreservices/rcdbbadsessnum)
- [var rcDBBadType: Int](/documentation/coreservices/rcdbbadtype)
- [var rcDBBreak: Int](/documentation/coreservices/rcdbbreak)
- [var rcDBError: Int](/documentation/coreservices/rcdberror)
- [var rcDBExec: Int](/documentation/coreservices/rcdbexec)
- [var rcDBNoHandler: Int](/documentation/coreservices/rcdbnohandler)
- [var rcDBNull: Int](/documentation/coreservices/rcdbnull)
- [var rcDBPackNotInited: Int](/documentation/coreservices/rcdbpacknotinited)
- [var rcDBValue: Int](/documentation/coreservices/rcdbvalue)
- [var rcDBWrongVersion: Int](/documentation/coreservices/rcdbwrongversion)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560050-anonymous)

##### Constants

- [var appIsDaemon: Int](/documentation/coreservices/appisdaemon)
- [var appMemFullErr: Int](/documentation/coreservices/appmemfullerr)
- [var appModeErr: Int](/documentation/coreservices/appmodeerr)
- [var bufferIsSmall: Int](/documentation/coreservices/bufferissmall)
- [var connectionInvalid: Int](/documentation/coreservices/connectioninvalid)
- [var hardwareConfigErr: Int](/documentation/coreservices/hardwareconfigerr)
- [var memFragErr: Int](/documentation/coreservices/memfragerr)
- [var noOutstandingHLE: Int](/documentation/coreservices/nooutstandinghle)
- [var noUserInteractionAllowed: Int](/documentation/coreservices/nouserinteractionallowed)
- [var procNotFound: Int](/documentation/coreservices/procnotfound)
- [var protocolErr: Int](/documentation/coreservices/protocolerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559962-anonymous)

##### Constants

- [var kTXNATSUIIsNotInstalledErr: Int](/documentation/coreservices/ktxnatsuiisnotinstallederr)
- [var kTXNAlreadyInitializedErr: Int](/documentation/coreservices/ktxnalreadyinitializederr)
- [var kTXNAttributeTagInvalidForRunErr: Int](/documentation/coreservices/ktxnattributetaginvalidforrunerr)
- [var kTXNBadDefaultFileTypeWarning: Int](/documentation/coreservices/ktxnbaddefaultfiletypewarning)
- [var kTXNCannotAddFrameErr: Int](/documentation/coreservices/ktxncannotaddframeerr)
- [var kTXNCannotSetAutoIndentErr: Int](/documentation/coreservices/ktxncannotsetautoindenterr)
- [var kTXNCannotTurnTSMOffWhenUsingUnicodeErr: Int](/documentation/coreservices/ktxncannotturntsmoffwhenusingunicodeerr)
- [var kTXNCopyNotAllowedInEchoModeErr: Int](/documentation/coreservices/ktxncopynotallowedinechomodeerr)
- [var kTXNDataTypeNotAllowedErr: Int](/documentation/coreservices/ktxndatatypenotallowederr)
- [var kTXNEndIterationErr: Int](/documentation/coreservices/ktxnenditerationerr)
- [var kTXNIllegalToCrossDataBoundariesErr: Int](/documentation/coreservices/ktxnillegaltocrossdataboundarieserr)
- [var kTXNInvalidFrameIDErr: Int](/documentation/coreservices/ktxninvalidframeiderr)
- [var kTXNInvalidRunIndex: Int](/documentation/coreservices/ktxninvalidrunindex)
- [var kTXNNoMatchErr: Int](/documentation/coreservices/ktxnnomatcherr)
- [var kTXNOutsideOfFrameErr: Int](/documentation/coreservices/ktxnoutsideofframeerr)
- [var kTXNOutsideOfLineErr: Int](/documentation/coreservices/ktxnoutsideoflineerr)
- [var kTXNRunIndexOutofBoundsErr: Int](/documentation/coreservices/ktxnrunindexoutofboundserr)
- [var kTXNSomeOrAllTagsInvalidForRunErr: Int](/documentation/coreservices/ktxnsomeoralltagsinvalidforrunerr)
- [var kTXNUserCanceledOperationErr: Int](/documentation/coreservices/ktxnusercanceledoperationerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559982-anonymous)

##### Constants

- [var errOSABadSelector: Int](/documentation/coreservices/errosabadselector)
- [var errOSABadStorageType: Int](/documentation/coreservices/errosabadstoragetype)
- [var errOSACantOpenComponent: Int](/documentation/coreservices/errosacantopencomponent)
- [var errOSACantStorePointers: Int](/documentation/coreservices/errosacantstorepointers)
- [var errOSAComponentMismatch: Int](/documentation/coreservices/errosacomponentmismatch)
- [var errOSACorruptData: Int](/documentation/coreservices/errosacorruptdata)
- [var errOSADataFormatObsolete: Int](/documentation/coreservices/errosadataformatobsolete)
- [var errOSADataFormatTooNew: Int](/documentation/coreservices/errosadataformattoonew)
- [var errOSAInvalidID: Int](/documentation/coreservices/errosainvalidid)
- [var errOSANoSuchDialect: Int](/documentation/coreservices/errosanosuchdialect)
- [var errOSARecordingIsAlreadyOn: Int](/documentation/coreservices/errosarecordingisalreadyon)
- [var errOSAScriptError: Int](/documentation/coreservices/errosascripterror)
- [var errOSASourceNotAvailable: Int](/documentation/coreservices/errosasourcenotavailable)
- [var errOSASystemError: Int](/documentation/coreservices/errosasystemerror)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560054-anonymous)

##### Constants

- [var threadBadAppContextErr: Int](/documentation/coreservices/threadbadappcontexterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560024-anonymous)

##### Constants

- [var pmBusyErr: Int](/documentation/coreservices/pmbusyerr)
- [var pmRecvEndErr: Int](/documentation/coreservices/pmrecvenderr)
- [var pmRecvStartErr: Int](/documentation/coreservices/pmrecvstarterr)
- [var pmReplyTOErr: Int](/documentation/coreservices/pmreplytoerr)
- [var pmSendEndErr: Int](/documentation/coreservices/pmsendenderr)
- [var pmSendStartErr: Int](/documentation/coreservices/pmsendstarterr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559960-anonymous)

##### Constants

- [var fsmBadFFSNameErr: Int](/documentation/coreservices/fsmbadffsnameerr)
- [var fsmBadFSDLenErr: Int](/documentation/coreservices/fsmbadfsdlenerr)
- [var fsmBadFSDVersionErr: Int](/documentation/coreservices/fsmbadfsdversionerr)
- [var fsmBusyFFSErr: Int](/documentation/coreservices/fsmbusyffserr)
- [var fsmDuplicateFSIDErr: Int](/documentation/coreservices/fsmduplicatefsiderr)
- [var fsmFFSNotFoundErr: Int](/documentation/coreservices/fsmffsnotfounderr)
- [var fsmNoAlternateStackErr: Int](/documentation/coreservices/fsmnoalternatestackerr)
- [var fsmUnknownFSMMessageErr: Int](/documentation/coreservices/fsmunknownfsmmessageerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560036-anonymous)

##### Constants

- [var errAEBadKeyForm: Int](/documentation/coreservices/erraebadkeyform)
- [var errAECantHandleClass: Int](/documentation/coreservices/erraecanthandleclass)
- [var errAECantPutThatThere: Int](/documentation/coreservices/erraecantputthatthere)
- [var errAECantSupplyType: Int](/documentation/coreservices/erraecantsupplytype)
- [var errAECantUndo: Int](/documentation/coreservices/erraecantundo)
- [var errAEEventFailed: Int](/documentation/coreservices/erraeeventfailed)
- [var errAEInTransaction: Int](/documentation/coreservices/erraeintransaction)
- [var errAEIndexTooLarge: Int](/documentation/coreservices/erraeindextoolarge)
- [var errAELocalOnly: Int](/documentation/coreservices/erraelocalonly)
- [var errAENoSuchTransaction: Int](/documentation/coreservices/erraenosuchtransaction)
- [var errAENoUserSelection: Int](/documentation/coreservices/erraenouserselection)
- [var errAENotASingleObject: Int](/documentation/coreservices/erraenotasingleobject)
- [var errAENotAnElement: Int](/documentation/coreservices/erraenotanelement)
- [var errAENotAnEnumMember: Int](/documentation/coreservices/erraenotanenummember)
- [var errAENotModifiable: Int](/documentation/coreservices/erraenotmodifiable)
- [var errAEPrivilegeError: Int](/documentation/coreservices/erraeprivilegeerror)
- [var errAEPropertiesClash: Int](/documentation/coreservices/erraepropertiesclash)
- [var errAEReadDenied: Int](/documentation/coreservices/erraereaddenied)
- [var errAETypeError: Int](/documentation/coreservices/erraetypeerror)
- [var errAEWriteDenied: Int](/documentation/coreservices/erraewritedenied)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560016-anonymous)

##### Constants

- [var kRAATalkInactive: Int](/documentation/coreservices/kraatalkinactive)
- [var kRACallBackFailed: Int](/documentation/coreservices/kracallbackfailed)
- [var kRAConfigurationDBInitErr: Int](/documentation/coreservices/kraconfigurationdbiniterr)
- [var kRAConnectionCanceled: Int](/documentation/coreservices/kraconnectioncanceled)
- [var kRADuplicateIPAddr: Int](/documentation/coreservices/kraduplicateipaddr)
- [var kRAExtAuthenticationFailed: Int](/documentation/coreservices/kraextauthenticationfailed)
- [var kRAIncompatiblePrefs: Int](/documentation/coreservices/kraincompatibleprefs)
- [var kRAInitOpenTransportFailed: Int](/documentation/coreservices/krainitopentransportfailed)
- [var kRAInstallationDamaged: Int](/documentation/coreservices/krainstallationdamaged)
- [var kRAInternalError: Int](/documentation/coreservices/krainternalerror)
- [var kRAInvalidParameter: Int](/documentation/coreservices/krainvalidparameter)
- [var kRAInvalidPassword: Int](/documentation/coreservices/krainvalidpassword)
- [var kRAInvalidPort: Int](/documentation/coreservices/krainvalidport)
- [var kRAInvalidPortState: Int](/documentation/coreservices/krainvalidportstate)
- [var kRAInvalidSerialProtocol: Int](/documentation/coreservices/krainvalidserialprotocol)
- [var kRAMissingResources: Int](/documentation/coreservices/kramissingresources)
- [var kRANCPRejectedbyPeer: Int](/documentation/coreservices/krancprejectedbypeer)
- [var kRANotConnected: Int](/documentation/coreservices/kranotconnected)
- [var kRANotEnabled: Int](/documentation/coreservices/kranotenabled)
- [var kRANotPrimaryInterface: Int](/documentation/coreservices/kranotprimaryinterface)
- [var kRANotSupported: Int](/documentation/coreservices/kranotsupported)
- [var kRAOutOfMemory: Int](/documentation/coreservices/kraoutofmemory)
- [var kRAPPPAuthenticationFailed: Int](/documentation/coreservices/krapppauthenticationfailed)
- [var kRAPPPNegotiationFailed: Int](/documentation/coreservices/krapppnegotiationfailed)
- [var kRAPPPPeerDisconnected: Int](/documentation/coreservices/krappppeerdisconnected)
- [var kRAPPPProtocolRejected: Int](/documentation/coreservices/krapppprotocolrejected)
- [var kRAPPPUserDisconnected: Int](/documentation/coreservices/krapppuserdisconnected)
- [var kRAPeerNotResponding: Int](/documentation/coreservices/krapeernotresponding)
- [var kRAPortBusy: Int](/documentation/coreservices/kraportbusy)
- [var kRAPortSetupFailed: Int](/documentation/coreservices/kraportsetupfailed)
- [var kRARemoteAccessNotReady: Int](/documentation/coreservices/kraremoteaccessnotready)
- [var kRAStartupFailed: Int](/documentation/coreservices/krastartupfailed)
- [var kRATCPIPInactive: Int](/documentation/coreservices/kratcpipinactive)
- [var kRATCPIPNotConfigured: Int](/documentation/coreservices/kratcpipnotconfigured)
- [var kRAUnknownPortState: Int](/documentation/coreservices/kraunknownportstate)
- [var kRAUnknownUser: Int](/documentation/coreservices/kraunknownuser)
- [var kRAUserInteractionRequired: Int](/documentation/coreservices/krauserinteractionrequired)
- [var kRAUserLoginDisabled: Int](/documentation/coreservices/krauserlogindisabled)
- [var kRAUserPwdChangeRequired: Int](/documentation/coreservices/krauserpwdchangerequired)
- [var kRAUserPwdEntryRequired: Int](/documentation/coreservices/krauserpwdentryrequired)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560031-anonymous)

##### Constants

- [var aspBadVersNum: Int](/documentation/coreservices/aspbadversnum)
- [var aspBufTooSmall: Int](/documentation/coreservices/aspbuftoosmall)
- [var aspNoAck: Int](/documentation/coreservices/aspnoack)
- [var aspNoMoreSess: Int](/documentation/coreservices/aspnomoresess)
- [var aspNoServers: Int](/documentation/coreservices/aspnoservers)
- [var aspParamErr: Int](/documentation/coreservices/aspparamerr)
- [var aspServerBusy: Int](/documentation/coreservices/aspserverbusy)
- [var aspSessClosed: Int](/documentation/coreservices/aspsessclosed)
- [var aspSizeErr: Int](/documentation/coreservices/aspsizeerr)
- [var aspTooMany: Int](/documentation/coreservices/asptoomany)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560022-anonymous)

##### Constants

- [var nbpBuffOvr: Int](/documentation/coreservices/nbpbuffovr)
- [var nbpConfDiff: Int](/documentation/coreservices/nbpconfdiff)
- [var nbpDuplicate: Int](/documentation/coreservices/nbpduplicate)
- [var nbpNISErr: Int](/documentation/coreservices/nbpniserr)
- [var nbpNoConfirm: Int](/documentation/coreservices/nbpnoconfirm)
- [var nbpNotFound: Int](/documentation/coreservices/nbpnotfound)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560026-anonymous)

##### Constants

- [var threadNotFoundErr: Int](/documentation/coreservices/threadnotfounderr)
- [var threadProtocolErr: Int](/documentation/coreservices/threadprotocolerr)
- [var threadTooManyReqsErr: Int](/documentation/coreservices/threadtoomanyreqserr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559934-anonymous)

##### Constants

- [var telAPattNotSupp: Int](/documentation/coreservices/telapattnotsupp)
- [var telAlreadyOpen: Int](/documentation/coreservices/telalreadyopen)
- [var telAutoAnsNotOn: Int](/documentation/coreservices/telautoansnoton)
- [var telBadAPattErr: Int](/documentation/coreservices/telbadapatterr)
- [var telBadBearerType: Int](/documentation/coreservices/telbadbearertype)
- [var telBadCAErr: Int](/documentation/coreservices/telbadcaerr)
- [var telBadCodeResource: Int](/documentation/coreservices/telbadcoderesource)
- [var telBadDNDType: Int](/documentation/coreservices/telbaddndtype)
- [var telBadDNErr: Int](/documentation/coreservices/telbaddnerr)
- [var telBadDNType: Int](/documentation/coreservices/telbaddntype)
- [var telBadDisplayMode: Int](/documentation/coreservices/telbaddisplaymode)
- [var telBadFeatureID: Int](/documentation/coreservices/telbadfeatureid)
- [var telBadFunction: Int](/documentation/coreservices/telbadfunction)
- [var telBadFwdType: Int](/documentation/coreservices/telbadfwdtype)
- [var telBadHTypeErr: Int](/documentation/coreservices/telbadhtypeerr)
- [var telBadHandErr: Int](/documentation/coreservices/telbadhanderr)
- [var telBadIndex: Int](/documentation/coreservices/telbadindex)
- [var telBadIntExt: Int](/documentation/coreservices/telbadintext)
- [var telBadIntercomID: Int](/documentation/coreservices/telbadintercomid)
- [var telBadLevelErr: Int](/documentation/coreservices/telbadlevelerr)
- [var telBadPageID: Int](/documentation/coreservices/telbadpageid)
- [var telBadParkID: Int](/documentation/coreservices/telbadparkid)
- [var telBadPickupGroupID: Int](/documentation/coreservices/telbadpickupgroupid)
- [var telBadProcErr: Int](/documentation/coreservices/telbadprocerr)
- [var telBadProcID: Int](/documentation/coreservices/telbadprocid)
- [var telBadRate: Int](/documentation/coreservices/telbadrate)
- [var telBadSWErr: Int](/documentation/coreservices/telbadswerr)
- [var telBadSampleRate: Int](/documentation/coreservices/telbadsamplerate)
- [var telBadSelect: Int](/documentation/coreservices/telbadselect)
- [var telBadStateErr: Int](/documentation/coreservices/telbadstateerr)
- [var telBadTermErr: Int](/documentation/coreservices/telbadtermerr)
- [var telBadVTypeErr: Int](/documentation/coreservices/telbadvtypeerr)
- [var telCANotAcceptable: Int](/documentation/coreservices/telcanotacceptable)
- [var telCANotDeflectable: Int](/documentation/coreservices/telcanotdeflectable)
- [var telCANotRejectable: Int](/documentation/coreservices/telcanotrejectable)
- [var telCAUnavail: Int](/documentation/coreservices/telcaunavail)
- [var telCBErr: Int](/documentation/coreservices/telcberr)
- [var telConfErr: Int](/documentation/coreservices/telconferr)
- [var telConfLimitErr: Int](/documentation/coreservices/telconflimiterr)
- [var telConfLimitExceeded: Int](/documentation/coreservices/telconflimitexceeded)
- [var telConfNoLimit: Int](/documentation/coreservices/telconfnolimit)
- [var telConfRej: Int](/documentation/coreservices/telconfrej)
- [var telDNDTypeNotSupp: Int](/documentation/coreservices/teldndtypenotsupp)
- [var telDNTypeNotSupp: Int](/documentation/coreservices/teldntypenotsupp)
- [var telDetAlreadyOn: Int](/documentation/coreservices/teldetalreadyon)
- [var telDeviceNotFound: Int](/documentation/coreservices/teldevicenotfound)
- [var telDisplayModeNotSupp: Int](/documentation/coreservices/teldisplaymodenotsupp)
- [var telFeatActive: Int](/documentation/coreservices/telfeatactive)
- [var telFeatNotAvail: Int](/documentation/coreservices/telfeatnotavail)
- [var telFeatNotSub: Int](/documentation/coreservices/telfeatnotsub)
- [var telFeatNotSupp: Int](/documentation/coreservices/telfeatnotsupp)
- [var telFwdTypeNotSupp: Int](/documentation/coreservices/telfwdtypenotsupp)
- [var telGenericError: Int](/documentation/coreservices/telgenericerror)
- [var telHTypeNotSupp: Int](/documentation/coreservices/telhtypenotsupp)
- [var telIndexNotSupp: Int](/documentation/coreservices/telindexnotsupp)
- [var telInitFailed: Int](/documentation/coreservices/telinitfailed)
- [var telIntExtNotSupp: Int](/documentation/coreservices/telintextnotsupp)
- [var telNoCallbackRef: Int](/documentation/coreservices/telnocallbackref)
- [var telNoCommFolder: Int](/documentation/coreservices/telnocommfolder)
- [var telNoErr: Int](/documentation/coreservices/telnoerr)
- [var telNoMemErr: Int](/documentation/coreservices/telnomemerr)
- [var telNoOpenErr: Int](/documentation/coreservices/telnoopenerr)
- [var telNoSuchTool: Int](/documentation/coreservices/telnosuchtool)
- [var telNoTools: Int](/documentation/coreservices/telnotools)
- [var telNotEnoughdspBW: Int](/documentation/coreservices/telnotenoughdspbw)
- [var telPBErr: Int](/documentation/coreservices/telpberr)
- [var telStateNotSupp: Int](/documentation/coreservices/telstatenotsupp)
- [var telStillNeeded: Int](/documentation/coreservices/telstillneeded)
- [var telTermNotOpen: Int](/documentation/coreservices/teltermnotopen)
- [var telTransferErr: Int](/documentation/coreservices/teltransfererr)
- [var telTransferRej: Int](/documentation/coreservices/teltransferrej)
- [var telUnknownErr: Int](/documentation/coreservices/telunknownerr)
- [var telVTypeNotSupp: Int](/documentation/coreservices/telvtypenotsupp)
- [var telValidateFailed: Int](/documentation/coreservices/telvalidatefailed)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560033-anonymous)

##### Constants

- [var kDTPAbortJobErr: Int](/documentation/coreservices/kdtpabortjoberr)
- [var kDTPHoldJobErr: Int](/documentation/coreservices/kdtpholdjoberr)
- [var kDTPStopQueueErr: Int](/documentation/coreservices/kdtpstopqueueerr)
- [var kDTPTryAgainErr: Int](/documentation/coreservices/kdtptryagainerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559980-anonymous)

##### Constants

- [var kMPNanokernelNeedsMemoryErr: Int](/documentation/coreservices/kmpnanokernelneedsmemoryerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559940-anonymous)

##### Constants

- [var componentDontRegister: Int](/documentation/coreservices/componentdontregister)
- [var componentNotCaptured: Int](/documentation/coreservices/componentnotcaptured)
- [var invalidComponentID: Int](/documentation/coreservices/invalidcomponentid)
- [var retryComponentRegistrationErr: Int](/documentation/coreservices/retrycomponentregistrationerr)
- [var unresolvedComponentDLLErr: Int](/documentation/coreservices/unresolvedcomponentdllerr)
- [var validInstancesExist: Int](/documentation/coreservices/validinstancesexist)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560064-anonymous)

##### Constants

- [var kernelAlreadyFreeErr: Int](/documentation/coreservices/kernelalreadyfreeerr)
- [var kernelAsyncReceiveLimitErr: Int](/documentation/coreservices/kernelasyncreceivelimiterr)
- [var kernelAsyncSendLimitErr: Int](/documentation/coreservices/kernelasyncsendlimiterr)
- [var kernelAttributeErr: Int](/documentation/coreservices/kernelattributeerr)
- [var kernelCanceledErr: Int](/documentation/coreservices/kernelcancelederr)
- [var kernelDeletePermissionErr: Int](/documentation/coreservices/kerneldeletepermissionerr)
- [var kernelExceptionErr: Int](/documentation/coreservices/kernelexceptionerr)
- [var kernelExecutePermissionErr: Int](/documentation/coreservices/kernelexecutepermissionerr)
- [var kernelExecutionLevelErr: Int](/documentation/coreservices/kernelexecutionlevelerr)
- [var kernelIDErr: Int](/documentation/coreservices/kerneliderr)
- [var kernelInUseErr: Int](/documentation/coreservices/kernelinuseerr)
- [var kernelIncompleteErr: Int](/documentation/coreservices/kernelincompleteerr)
- [var kernelObjectExistsErr: Int](/documentation/coreservices/kernelobjectexistserr)
- [var kernelOptionsErr: Int](/documentation/coreservices/kerneloptionserr)
- [var kernelPrivilegeErr: Int](/documentation/coreservices/kernelprivilegeerr)
- [var kernelReadPermissionErr: Int](/documentation/coreservices/kernelreadpermissionerr)
- [var kernelReturnValueErr: Int](/documentation/coreservices/kernelreturnvalueerr)
- [var kernelTerminatedErr: Int](/documentation/coreservices/kernelterminatederr)
- [var kernelTimeoutErr: Int](/documentation/coreservices/kerneltimeouterr)
- [var kernelUnrecoverableErr: Int](/documentation/coreservices/kernelunrecoverableerr)
- [var kernelUnsupportedErr: Int](/documentation/coreservices/kernelunsupportederr)
- [var kernelWritePermissionErr: Int](/documentation/coreservices/kernelwritepermissionerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560032-anonymous)

##### Constants

- [var errCoreEndianDataDoesNotMatchFormat: Int](/documentation/coreservices/errcoreendiandatadoesnotmatchformat)
- [var errCoreEndianDataTooLongForFormat: Int](/documentation/coreservices/errcoreendiandatatoolongforformat)
- [var errCoreEndianDataTooShortForFormat: Int](/documentation/coreservices/errcoreendiandatatooshortforformat)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560041-anonymous)

##### Constants

- [var badEditionFileErr: Int](/documentation/coreservices/badeditionfileerr)
- [var badSectionErr: Int](/documentation/coreservices/badsectionerr)
- [var badSubPartErr: Int](/documentation/coreservices/badsubparterr)
- [var containerAlreadyOpenWrn: Int](/documentation/coreservices/containeralreadyopenwrn)
- [var containerNotFoundWrn: Int](/documentation/coreservices/containernotfoundwrn)
- [var editionMgrInitErr: Int](/documentation/coreservices/editionmgriniterr)
- [var multiplePublisherWrn: Int](/documentation/coreservices/multiplepublisherwrn)
- [var notRegisteredSectionErr: Int](/documentation/coreservices/notregisteredsectionerr)
- [var notThePublisherWrn: Int](/documentation/coreservices/notthepublisherwrn)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560070-anonymous)

##### Constants

- [var badTranslationSpecErr: Int](/documentation/coreservices/badtranslationspecerr)
- [var couldNotParseSourceFileErr: Int](/documentation/coreservices/couldnotparsesourcefileerr)
- [var invalidTranslationPathErr: Int](/documentation/coreservices/invalidtranslationpatherr)
- [var noPrefAppErr: Int](/documentation/coreservices/noprefapperr)
- [var noTranslationPathErr: Int](/documentation/coreservices/notranslationpatherr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559953-anonymous)

##### Constants

- [var errAlreadyInImagingMode: Int](/documentation/coreservices/erralreadyinimagingmode)
- [var errCannotUndo: Int](/documentation/coreservices/errcannotundo)
- [var errEmptyScrap: Int](/documentation/coreservices/erremptyscrap)
- [var errEngineNotFound: Int](/documentation/coreservices/errenginenotfound)
- [var errInvalidRange: Int](/documentation/coreservices/errinvalidrange)
- [var errIteratorReachedEnd: Int](/documentation/coreservices/erriteratorreachedend)
- [var errMarginWilllNotFit: Int](/documentation/coreservices/errmarginwilllnotfit)
- [var errNoHiliteText: Int](/documentation/coreservices/errnohilitetext)
- [var errNonContiuousAttribute: Int](/documentation/coreservices/errnoncontiuousattribute)
- [var errNotInImagingMode: Int](/documentation/coreservices/errnotinimagingmode)
- [var errOffsetNotOnElementBounday: Int](/documentation/coreservices/erroffsetnotonelementbounday)
- [var errReadOnlyText: Int](/documentation/coreservices/errreadonlytext)
- [var errUnknownAttributeTag: Int](/documentation/coreservices/errunknownattributetag)
- [var errUnknownElement: Int](/documentation/coreservices/errunknownelement)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559997-anonymous)

##### Constants

- [var SlpTypeErr: Int](/documentation/coreservices/slptypeerr)
- [var badUnitErr: Int](/documentation/coreservices/baduniterr)
- [var closErr: Int](/documentation/coreservices/closerr)
- [var controlErr: Int](/documentation/coreservices/controlerr)
- [var corErr: Int](/documentation/coreservices/corerr)
- [var dInstErr: Int](/documentation/coreservices/dinsterr)
- [var dRemovErr: Int](/documentation/coreservices/dremoverr)
- [var noHardwareErr: Int](/documentation/coreservices/nohardwareerr)
- [var notEnoughHardwareErr: Int](/documentation/coreservices/notenoughhardwareerr)
- [var openErr: Int](/documentation/coreservices/openerr)
- [var paramErr: Int](/documentation/coreservices/paramerr)
- [var qErr: Int](/documentation/coreservices/qerr)
- [var readErr: Int](/documentation/coreservices/readerr)
- [var seNoDB: Int](/documentation/coreservices/senodb)
- [var statusErr: Int](/documentation/coreservices/statuserr)
- [var unimpErr: Int](/documentation/coreservices/unimperr)
- [var unitEmptyErr: Int](/documentation/coreservices/unitemptyerr)
- [var userCanceledErr: Int](/documentation/coreservices/usercancelederr)
- [var vTypErr: Int](/documentation/coreservices/vtyperr)
- [var writErr: Int](/documentation/coreservices/writerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560000-anonymous)

##### Constants

- [var kUSBBadDispatchTable: Int](/documentation/coreservices/kusbbaddispatchtable)
- [var kUSBNotHandled: Int](/documentation/coreservices/kusbnothandled)
- [var kUSBQueueFull: Int](/documentation/coreservices/kusbqueuefull)
- [var kUSBUnknownNotification: Int](/documentation/coreservices/kusbunknownnotification)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560035-anonymous)

##### Constants

- [var kEACCESErr: Int](/documentation/coreservices/keacceserr)
- [var kEADDRINUSEErr: Int](/documentation/coreservices/keaddrinuseerr)
- [var kEADDRNOTAVAILErr: Int](/documentation/coreservices/keaddrnotavailerr)
- [var kEAGAINErr: Int](/documentation/coreservices/keagainerr)
- [var kEALREADYErr: Int](/documentation/coreservices/kealreadyerr)
- [var kEBADFErr: Int](/documentation/coreservices/kebadferr)
- [var kEBADMSGErr: Int](/documentation/coreservices/kebadmsgerr)
- [var kEBUSYErr: Int](/documentation/coreservices/kebusyerr)
- [var kECANCELErr: Int](/documentation/coreservices/kecancelerr)
- [var kECONNABORTEDErr: Int](/documentation/coreservices/keconnabortederr)
- [var kECONNREFUSEDErr: Int](/documentation/coreservices/keconnrefusederr)
- [var kECONNRESETErr: Int](/documentation/coreservices/keconnreseterr)
- [var kEDEADLKErr: Int](/documentation/coreservices/kedeadlkerr)
- [var kEDESTADDRREQErr: Int](/documentation/coreservices/kedestaddrreqerr)
- [var kEEXISTErr: Int](/documentation/coreservices/keexisterr)
- [var kEFAULTErr: Int](/documentation/coreservices/kefaulterr)
- [var kEHOSTDOWNErr: Int](/documentation/coreservices/kehostdownerr)
- [var kEHOSTUNREACHErr: Int](/documentation/coreservices/kehostunreacherr)
- [var kEINPROGRESSErr: Int](/documentation/coreservices/keinprogresserr)
- [var kEINTRErr: Int](/documentation/coreservices/keintrerr)
- [var kEINVALErr: Int](/documentation/coreservices/keinvalerr)
- [var kEIOErr: Int](/documentation/coreservices/keioerr)
- [var kEISCONNErr: Int](/documentation/coreservices/keisconnerr)
- [var kEMSGSIZEErr: Int](/documentation/coreservices/kemsgsizeerr)
- [var kENETDOWNErr: Int](/documentation/coreservices/kenetdownerr)
- [var kENETRESETErr: Int](/documentation/coreservices/kenetreseterr)
- [var kENETUNREACHErr: Int](/documentation/coreservices/kenetunreacherr)
- [var kENOBUFSErr: Int](/documentation/coreservices/kenobufserr)
- [var kENODATAErr: Int](/documentation/coreservices/kenodataerr)
- [var kENODEVErr: Int](/documentation/coreservices/kenodeverr)
- [var kENOENTErr: Int](/documentation/coreservices/kenoenterr)
- [var kENOMEMErr: Int](/documentation/coreservices/kenomemerr)
- [var kENOMSGErr: Int](/documentation/coreservices/kenomsgerr)
- [var kENOPROTOOPTErr: Int](/documentation/coreservices/kenoprotoopterr)
- [var kENORSRCErr: Int](/documentation/coreservices/kenorsrcerr)
- [var kENOSRErr: Int](/documentation/coreservices/kenosrerr)
- [var kENOSTRErr: Int](/documentation/coreservices/kenostrerr)
- [var kENOTCONNErr: Int](/documentation/coreservices/kenotconnerr)
- [var kENOTSOCKErr: Int](/documentation/coreservices/kenotsockerr)
- [var kENOTTYErr: Int](/documentation/coreservices/kenottyerr)
- [var kENXIOErr: Int](/documentation/coreservices/kenxioerr)
- [var kEOPNOTSUPPErr: Int](/documentation/coreservices/keopnotsupperr)
- [var kEPERMErr: Int](/documentation/coreservices/kepermerr)
- [var kEPIPEErr: Int](/documentation/coreservices/kepipeerr)
- [var kEPROTOErr: Int](/documentation/coreservices/keprotoerr)
- [var kEPROTONOSUPPORTErr: Int](/documentation/coreservices/keprotonosupporterr)
- [var kEPROTOTYPEErr: Int](/documentation/coreservices/keprototypeerr)
- [var kERANGEErr: Int](/documentation/coreservices/kerangeerr)
- [var kESHUTDOWNErr: Int](/documentation/coreservices/keshutdownerr)
- [var kESOCKTNOSUPPORTErr: Int](/documentation/coreservices/kesocktnosupporterr)
- [var kESRCHErr: Int](/documentation/coreservices/kesrcherr)
- [var kETIMEDOUTErr: Int](/documentation/coreservices/ketimedouterr)
- [var kETIMEErr: Int](/documentation/coreservices/ketimeerr)
- [var kETOOMANYREFSErr: Int](/documentation/coreservices/ketoomanyrefserr)
- [var kEWOULDBLOCKErr: Int](/documentation/coreservices/kewouldblockerr)
- [var kOTAccessErr: Int](/documentation/coreservices/kotaccesserr)
- [var kOTAddressBusyErr: Int](/documentation/coreservices/kotaddressbusyerr)
- [var kOTBadAddressErr: Int](/documentation/coreservices/kotbadaddresserr)
- [var kOTBadConfigurationErr: Int](/documentation/coreservices/kotbadconfigurationerr)
- [var kOTBadDataErr: Int](/documentation/coreservices/kotbaddataerr)
- [var kOTBadFlagErr: Int](/documentation/coreservices/kotbadflagerr)
- [var kOTBadNameErr: Int](/documentation/coreservices/kotbadnameerr)
- [var kOTBadOptionErr: Int](/documentation/coreservices/kotbadoptionerr)
- [var kOTBadQLenErr: Int](/documentation/coreservices/kotbadqlenerr)
- [var kOTBadReferenceErr: Int](/documentation/coreservices/kotbadreferenceerr)
- [var kOTBadSequenceErr: Int](/documentation/coreservices/kotbadsequenceerr)
- [var kOTBadSyncErr: Int](/documentation/coreservices/kotbadsyncerr)
- [var kOTBufferOverflowErr: Int](/documentation/coreservices/kotbufferoverflowerr)
- [var kOTCanceledErr: Int](/documentation/coreservices/kotcancelederr)
- [var kOTClientNotInittedErr: Int](/documentation/coreservices/kotclientnotinittederr)
- [var kOTConfigurationChangedErr: Int](/documentation/coreservices/kotconfigurationchangederr)
- [var kOTDuplicateFoundErr: Int](/documentation/coreservices/kotduplicatefounderr)
- [var kOTFlowErr: Int](/documentation/coreservices/kotflowerr)
- [var kOTIndOutErr: Int](/documentation/coreservices/kotindouterr)
- [var kOTLookErr: Int](/documentation/coreservices/kotlookerr)
- [var kOTNoAddressErr: Int](/documentation/coreservices/kotnoaddresserr)
- [var kOTNoDataErr: Int](/documentation/coreservices/kotnodataerr)
- [var kOTNoDisconnectErr: Int](/documentation/coreservices/kotnodisconnecterr)
- [var kOTNoError: Int](/documentation/coreservices/kotnoerror)
- [var kOTNoReleaseErr: Int](/documentation/coreservices/kotnoreleaseerr)
- [var kOTNoStructureTypeErr: Int](/documentation/coreservices/kotnostructuretypeerr)
- [var kOTNoUDErrErr: Int](/documentation/coreservices/kotnouderrerr)
- [var kOTNotFoundErr: Int](/documentation/coreservices/kotnotfounderr)
- [var kOTNotSupportedErr: Int](/documentation/coreservices/kotnotsupportederr)
- [var kOTOutOfMemoryErr: Int](/documentation/coreservices/kotoutofmemoryerr)
- [var kOTOutStateErr: Int](/documentation/coreservices/kotoutstateerr)
- [var kOTPortHasDiedErr: Int](/documentation/coreservices/kotporthasdiederr)
- [var kOTPortLostConnection: Int](/documentation/coreservices/kotportlostconnection)
- [var kOTPortWasEjectedErr: Int](/documentation/coreservices/kotportwasejectederr)
- [var kOTProtocolErr: Int](/documentation/coreservices/kotprotocolerr)
- [var kOTProviderMismatchErr: Int](/documentation/coreservices/kotprovidermismatcherr)
- [var kOTQFullErr: Int](/documentation/coreservices/kotqfullerr)
- [var kOTResAddressErr: Int](/documentation/coreservices/kotresaddresserr)
- [var kOTResQLenErr: Int](/documentation/coreservices/kotresqlenerr)
- [var kOTStateChangeErr: Int](/documentation/coreservices/kotstatechangeerr)
- [var kOTSysErrorErr: Int](/documentation/coreservices/kotsyserrorerr)
- [var kOTUserRequestedErr: Int](/documentation/coreservices/kotuserrequestederr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559968-anonymous)

##### Constants

- [var cmCantCopyModifiedV1Profile: Int](/documentation/coreservices/cmcantcopymodifiedv1profile)
- [var cmCantDeleteElement: Int](/documentation/coreservices/cmcantdeleteelement)
- [var cmCantGamutCheckError: Int](/documentation/coreservices/cmcantgamutcheckerror)
- [var cmElementTagNotFound: Int](/documentation/coreservices/cmelementtagnotfound)
- [var cmErrIncompatibleProfile: Int](/documentation/coreservices/cmerrincompatibleprofile)
- [var cmFatalProfileErr: Int](/documentation/coreservices/cmfatalprofileerr)
- [var cmIndexRangeErr: Int](/documentation/coreservices/cmindexrangeerr)
- [var cmInvalidColorSpace: Int](/documentation/coreservices/cminvalidcolorspace)
- [var cmInvalidDstMap: Int](/documentation/coreservices/cminvaliddstmap)
- [var cmInvalidProfile: Int](/documentation/coreservices/cminvalidprofile)
- [var cmInvalidProfileComment: Int](/documentation/coreservices/cminvalidprofilecomment)
- [var cmInvalidProfileLocation: Int](/documentation/coreservices/cminvalidprofilelocation)
- [var cmInvalidSearch: Int](/documentation/coreservices/cminvalidsearch)
- [var cmInvalidSrcMap: Int](/documentation/coreservices/cminvalidsrcmap)
- [var cmNamedColorNotFound: Int](/documentation/coreservices/cmnamedcolornotfound)
- [var cmNoGDevicesError: Int](/documentation/coreservices/cmnogdeviceserror)
- [var cmRangeOverFlow: Int](/documentation/coreservices/cmrangeoverflow)
- [var cmSearchError: Int](/documentation/coreservices/cmsearcherror)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560012-anonymous)

##### Constants

- [var errEndOfBody: Int](/documentation/coreservices/errendofbody)
- [var errEndOfDocument: Int](/documentation/coreservices/errendofdocument)
- [var errOffsetInvalid: Int](/documentation/coreservices/erroffsetinvalid)
- [var errOffsetIsOutsideOfView: Int](/documentation/coreservices/erroffsetisoutsideofview)
- [var errTopOfBody: Int](/documentation/coreservices/errtopofbody)
- [var errTopOfDocument: Int](/documentation/coreservices/errtopofdocument)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559976-anonymous)

##### Constants

- [var kUSBBitstufErr: Int](/documentation/coreservices/kusbbitstuferr)
- [var kUSBBufOvrRunErr: Int](/documentation/coreservices/kusbbufovrrunerr)
- [var kUSBBufUnderRunErr: Int](/documentation/coreservices/kusbbufunderrunerr)
- [var kUSBCRCErr: Int](/documentation/coreservices/kusbcrcerr)
- [var kUSBDataToggleErr: Int](/documentation/coreservices/kusbdatatoggleerr)
- [var kUSBEndpointStallErr: Int](/documentation/coreservices/kusbendpointstallerr)
- [var kUSBLinkErr: Int](/documentation/coreservices/kusblinkerr)
- [var kUSBNotRespondingErr: Int](/documentation/coreservices/kusbnotrespondingerr)
- [var kUSBNotSent1Err: Int](/documentation/coreservices/kusbnotsent1err)
- [var kUSBNotSent2Err: Int](/documentation/coreservices/kusbnotsent2err)
- [var kUSBOverRunErr: Int](/documentation/coreservices/kusboverrunerr)
- [var kUSBPIDCheckErr: Int](/documentation/coreservices/kusbpidcheckerr)
- [var kUSBRes1Err: Int](/documentation/coreservices/kusbres1err)
- [var kUSBRes2Err: Int](/documentation/coreservices/kusbres2err)
- [var kUSBUnderRunErr: Int](/documentation/coreservices/kusbunderrunerr)
- [var kUSBWrongPIDErr: Int](/documentation/coreservices/kusbwrongpiderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559950-anonymous)

##### Constants

- [var auxiliaryExportDataUnavailable: Int](/documentation/coreservices/auxiliaryexportdataunavailable)
- [var badComponentType: Int](/documentation/coreservices/badcomponenttype)
- [var badDataRefIndex: Int](/documentation/coreservices/baddatarefindex)
- [var badEditIndex: Int](/documentation/coreservices/badeditindex)
- [var badEditList: Int](/documentation/coreservices/badeditlist)
- [var badImageDescription: Int](/documentation/coreservices/badimagedescription)
- [var badPublicMovieAtom: Int](/documentation/coreservices/badpublicmovieatom)
- [var badTrackIndex: Int](/documentation/coreservices/badtrackindex)
- [var cantCreateSingleForkFile: Int](/documentation/coreservices/cantcreatesingleforkfile)
- [var cantEnableTrack: Int](/documentation/coreservices/cantenabletrack)
- [var cantFindHandler: Int](/documentation/coreservices/cantfindhandler)
- [var cantOpenHandler: Int](/documentation/coreservices/cantopenhandler)
- [var cantPutPublicMovieAtom: Int](/documentation/coreservices/cantputpublicmovieatom)
- [var couldNotResolveDataRef: Int](/documentation/coreservices/couldnotresolvedataref)
- [var couldNotUseAnExistingSample: Int](/documentation/coreservices/couldnotuseanexistingsample)
- [var dataAlreadyClosed: Int](/documentation/coreservices/dataalreadyclosed)
- [var dataAlreadyOpenForWrite: Int](/documentation/coreservices/dataalreadyopenforwrite)
- [var dataNoDataRef: Int](/documentation/coreservices/datanodataref)
- [var dataNotOpenForRead: Int](/documentation/coreservices/datanotopenforread)
- [var dataNotOpenForWrite: Int](/documentation/coreservices/datanotopenforwrite)
- [var endOfDataReached: Int](/documentation/coreservices/endofdatareached)
- [var featureUnsupported: Int](/documentation/coreservices/featureunsupported)
- [var gWorldsNotSameDepthAndSizeErr: Int](/documentation/coreservices/gworldsnotsamedepthandsizeerr)
- [var internalQuickTimeError: Int](/documentation/coreservices/internalquicktimeerror)
- [var invalidChunkCache: Int](/documentation/coreservices/invalidchunkcache)
- [var invalidChunkNum: Int](/documentation/coreservices/invalidchunknum)
- [var invalidDataRef: Int](/documentation/coreservices/invaliddataref)
- [var invalidDataRefContainer: Int](/documentation/coreservices/invaliddatarefcontainer)
- [var invalidDuration: Int](/documentation/coreservices/invalidduration)
- [var invalidEditState: Int](/documentation/coreservices/invalideditstate)
- [var invalidHandler: Int](/documentation/coreservices/invalidhandler)
- [var invalidImageIndexErr: Int](/documentation/coreservices/invalidimageindexerr)
- [var invalidMedia: Int](/documentation/coreservices/invalidmedia)
- [var invalidMovie: Int](/documentation/coreservices/invalidmovie)
- [var invalidRect: Int](/documentation/coreservices/invalidrect)
- [var invalidSampleDescIndex: Int](/documentation/coreservices/invalidsampledescindex)
- [var invalidSampleDescription: Int](/documentation/coreservices/invalidsampledescription)
- [var invalidSampleNum: Int](/documentation/coreservices/invalidsamplenum)
- [var invalidSampleTable: Int](/documentation/coreservices/invalidsampletable)
- [var invalidSpriteIDErr: Int](/documentation/coreservices/invalidspriteiderr)
- [var invalidSpriteIndexErr: Int](/documentation/coreservices/invalidspriteindexerr)
- [var invalidSpritePropertyErr: Int](/documentation/coreservices/invalidspritepropertyerr)
- [var invalidSpriteWorldPropertyErr: Int](/documentation/coreservices/invalidspriteworldpropertyerr)
- [var invalidTime: Int](/documentation/coreservices/invalidtime)
- [var invalidTrack: Int](/documentation/coreservices/invalidtrack)
- [var maxSizeToGrowTooSmall: Int](/documentation/coreservices/maxsizetogrowtoosmall)
- [var mediaTypesDontMatch: Int](/documentation/coreservices/mediatypesdontmatch)
- [var missingRequiredParameterErr: Int](/documentation/coreservices/missingrequiredparametererr)
- [var movieTextNotFoundErr: Int](/documentation/coreservices/movietextnotfounderr)
- [var movieToolboxUninitialized: Int](/documentation/coreservices/movietoolboxuninitialized)
- [var noDataHandler: Int](/documentation/coreservices/nodatahandler)
- [var noDefaultDataRef: Int](/documentation/coreservices/nodefaultdataref)
- [var noMediaHandler: Int](/documentation/coreservices/nomediahandler)
- [var noMovieFound: Int](/documentation/coreservices/nomoviefound)
- [var noRecordOfApp: Int](/documentation/coreservices/norecordofapp)
- [var noSoundTrackInMovieErr: Int](/documentation/coreservices/nosoundtrackinmovieerr)
- [var noSourceTreeFoundErr: Int](/documentation/coreservices/nosourcetreefounderr)
- [var noVideoTrackInMovieErr: Int](/documentation/coreservices/novideotrackinmovieerr)
- [var nonMatchingEditState: Int](/documentation/coreservices/nonmatchingeditstate)
- [var progressProcAborted: Int](/documentation/coreservices/progressprocaborted)
- [var samplesAlreadyInMediaErr: Int](/documentation/coreservices/samplesalreadyinmediaerr)
- [var soundSupportNotAvailableErr: Int](/documentation/coreservices/soundsupportnotavailableerr)
- [var sourceNotFoundErr: Int](/documentation/coreservices/sourcenotfounderr)
- [var staleEditState: Int](/documentation/coreservices/staleeditstate)
- [var timeNotInMedia: Int](/documentation/coreservices/timenotinmedia)
- [var timeNotInTrack: Int](/documentation/coreservices/timenotintrack)
- [var trackIDNotFound: Int](/documentation/coreservices/trackidnotfound)
- [var trackNotInMovie: Int](/documentation/coreservices/tracknotinmovie)
- [var unsupportedAuxiliaryImportData: Int](/documentation/coreservices/unsupportedauxiliaryimportdata)
- [var userDataItemNotFound: Int](/documentation/coreservices/userdataitemnotfound)
- [var wfFileNotFound: Int](/documentation/coreservices/wffilenotfound)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559999-anonymous)

##### Constants

- [var hmBalloonAborted: Int](/documentation/coreservices/hmballoonaborted)
- [var hmCloseViewActive: Int](/documentation/coreservices/hmcloseviewactive)
- [var hmHelpDisabled: Int](/documentation/coreservices/hmhelpdisabled)
- [var hmHelpManagerNotInited: Int](/documentation/coreservices/hmhelpmanagernotinited)
- [var hmNoBalloonUp: Int](/documentation/coreservices/hmnoballoonup)
- [var hmOperationUnsupported: Int](/documentation/coreservices/hmoperationunsupported)
- [var hmSameAsLastBalloon: Int](/documentation/coreservices/hmsameaslastballoon)
- [var hmSkippedBalloon: Int](/documentation/coreservices/hmskippedballoon)
- [var hmUnknownHelpType: Int](/documentation/coreservices/hmunknownhelptype)
- [var hmWrongVersion: Int](/documentation/coreservices/hmwrongversion)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1560067-anonymous)

##### Constants

- [var kALMDeferSwitchErr: Int](/documentation/coreservices/kalmdeferswitcherr)
- [var kALMDuplicateModuleErr: Int](/documentation/coreservices/kalmduplicatemoduleerr)
- [var kALMGroupNotFoundErr: Int](/documentation/coreservices/kalmgroupnotfounderr)
- [var kALMInstallationErr: Int](/documentation/coreservices/kalminstallationerr)
- [var kALMInternalErr: Int](/documentation/coreservices/kalminternalerr)
- [var kALMModuleCommunicationErr: Int](/documentation/coreservices/kalmmodulecommunicationerr)
- [var kALMNoSuchModuleErr: Int](/documentation/coreservices/kalmnosuchmoduleerr)
- [var kALMRebootFlagsLevelErr: Int](/documentation/coreservices/kalmrebootflagslevelerr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559983-anonymous)

##### Constants

- [var kALMLocationNotFoundErr: Int](/documentation/coreservices/kalmlocationnotfounderr)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559951-anonymous)

##### Constants

- [var badControllerHeight: Int](/documentation/coreservices/badcontrollerheight)
- [var badSGChannel: Int](/documentation/coreservices/badsgchannel)
- [var cannotMoveAttachedController: Int](/documentation/coreservices/cannotmoveattachedcontroller)
- [var cannotSetWidthOfAttachedController: Int](/documentation/coreservices/cannotsetwidthofattachedcontroller)
- [var cantDoThatInCurrentMode: Int](/documentation/coreservices/cantdothatincurrentmode)
- [var controllerBoundsNotExact: Int](/documentation/coreservices/controllerboundsnotexact)
- [var controllerHasFixedHeight: Int](/documentation/coreservices/controllerhasfixedheight)
- [var couldntGetRequiredComponent: Int](/documentation/coreservices/couldntgetrequiredcomponent)
- [var deviceCantMeetRequest: Int](/documentation/coreservices/devicecantmeetrequest)
- [var editingNotAllowed: Int](/documentation/coreservices/editingnotallowed)
- [var grabTimeComplete: Int](/documentation/coreservices/grabtimecomplete)
- [var noDeviceForChannel: Int](/documentation/coreservices/nodeviceforchannel)
- [var notEnoughDiskSpaceToGrab: Int](/documentation/coreservices/notenoughdiskspacetograb)
- [var notEnoughMemoryToGrab: Int](/documentation/coreservices/notenoughmemorytograb)
- [var seqGrabInfoNotAvailable: Int](/documentation/coreservices/seqgrabinfonotavailable)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1559943-anonymous)

##### Constants

- [var kPOSIXErrorBase: Int](/documentation/coreservices/kposixerrorbase)
- [var kPOSIXErrorE2BIG: Int](/documentation/coreservices/kposixerrore2big)
- [var kPOSIXErrorEACCES: Int](/documentation/coreservices/kposixerroreacces)
- [var kPOSIXErrorEADDRINUSE: Int](/documentation/coreservices/kposixerroreaddrinuse)
- [var kPOSIXErrorEADDRNOTAVAIL: Int](/documentation/coreservices/kposixerroreaddrnotavail)
- [var kPOSIXErrorEAFNOSUPPORT: Int](/documentation/coreservices/kposixerroreafnosupport)
- [var kPOSIXErrorEAGAIN: Int](/documentation/coreservices/kposixerroreagain)
- [var kPOSIXErrorEALREADY: Int](/documentation/coreservices/kposixerrorealready)
- [var kPOSIXErrorEAUTH: Int](/documentation/coreservices/kposixerroreauth)
- [var kPOSIXErrorEBADARCH: Int](/documentation/coreservices/kposixerrorebadarch)
- [var kPOSIXErrorEBADEXEC: Int](/documentation/coreservices/kposixerrorebadexec)
- [var kPOSIXErrorEBADF: Int](/documentation/coreservices/kposixerrorebadf)
- [var kPOSIXErrorEBADMACHO: Int](/documentation/coreservices/kposixerrorebadmacho)
- [var kPOSIXErrorEBADMSG: Int](/documentation/coreservices/kposixerrorebadmsg)
- [var kPOSIXErrorEBADRPC: Int](/documentation/coreservices/kposixerrorebadrpc)
- [var kPOSIXErrorEBUSY: Int](/documentation/coreservices/kposixerrorebusy)
- [var kPOSIXErrorECANCELED: Int](/documentation/coreservices/kposixerrorecanceled)
- [var kPOSIXErrorECHILD: Int](/documentation/coreservices/kposixerrorechild)
- [var kPOSIXErrorECONNABORTED: Int](/documentation/coreservices/kposixerroreconnaborted)
- [var kPOSIXErrorECONNREFUSED: Int](/documentation/coreservices/kposixerroreconnrefused)
- [var kPOSIXErrorECONNRESET: Int](/documentation/coreservices/kposixerroreconnreset)
- [var kPOSIXErrorEDEADLK: Int](/documentation/coreservices/kposixerroredeadlk)
- [var kPOSIXErrorEDESTADDRREQ: Int](/documentation/coreservices/kposixerroredestaddrreq)
- [var kPOSIXErrorEDEVERR: Int](/documentation/coreservices/kposixerroredeverr)
- [var kPOSIXErrorEDOM: Int](/documentation/coreservices/kposixerroredom)
- [var kPOSIXErrorEDQUOT: Int](/documentation/coreservices/kposixerroredquot)
- [var kPOSIXErrorEEXIST: Int](/documentation/coreservices/kposixerroreexist)
- [var kPOSIXErrorEFAULT: Int](/documentation/coreservices/kposixerrorefault)
- [var kPOSIXErrorEFBIG: Int](/documentation/coreservices/kposixerrorefbig)
- [var kPOSIXErrorEFTYPE: Int](/documentation/coreservices/kposixerroreftype)
- [var kPOSIXErrorEHOSTDOWN: Int](/documentation/coreservices/kposixerrorehostdown)
- [var kPOSIXErrorEHOSTUNREACH: Int](/documentation/coreservices/kposixerrorehostunreach)
- [var kPOSIXErrorEIDRM: Int](/documentation/coreservices/kposixerroreidrm)
- [var kPOSIXErrorEILSEQ: Int](/documentation/coreservices/kposixerroreilseq)
- [var kPOSIXErrorEINPROGRESS: Int](/documentation/coreservices/kposixerroreinprogress)
- [var kPOSIXErrorEINTR: Int](/documentation/coreservices/kposixerroreintr)
- [var kPOSIXErrorEINVAL: Int](/documentation/coreservices/kposixerroreinval)
- [var kPOSIXErrorEIO: Int](/documentation/coreservices/kposixerroreio)
- [var kPOSIXErrorEISCONN: Int](/documentation/coreservices/kposixerroreisconn)
- [var kPOSIXErrorEISDIR: Int](/documentation/coreservices/kposixerroreisdir)
- [var kPOSIXErrorELOOP: Int](/documentation/coreservices/kposixerroreloop)
- [var kPOSIXErrorEMFILE: Int](/documentation/coreservices/kposixerroremfile)
- [var kPOSIXErrorEMLINK: Int](/documentation/coreservices/kposixerroremlink)
- [var kPOSIXErrorEMSGSIZE: Int](/documentation/coreservices/kposixerroremsgsize)
- [var kPOSIXErrorEMULTIHOP: Int](/documentation/coreservices/kposixerroremultihop)
- [var kPOSIXErrorENAMETOOLONG: Int](/documentation/coreservices/kposixerrorenametoolong)
- [var kPOSIXErrorENEEDAUTH: Int](/documentation/coreservices/kposixerroreneedauth)
- [var kPOSIXErrorENETDOWN: Int](/documentation/coreservices/kposixerrorenetdown)
- [var kPOSIXErrorENETRESET: Int](/documentation/coreservices/kposixerrorenetreset)
- [var kPOSIXErrorENETUNREACH: Int](/documentation/coreservices/kposixerrorenetunreach)
- [var kPOSIXErrorENFILE: Int](/documentation/coreservices/kposixerrorenfile)
- [var kPOSIXErrorENOATTR: Int](/documentation/coreservices/kposixerrorenoattr)
- [var kPOSIXErrorENOBUFS: Int](/documentation/coreservices/kposixerrorenobufs)
- [var kPOSIXErrorENODATA: Int](/documentation/coreservices/kposixerrorenodata)
- [var kPOSIXErrorENODEV: Int](/documentation/coreservices/kposixerrorenodev)
- [var kPOSIXErrorENOENT: Int](/documentation/coreservices/kposixerrorenoent)
- [var kPOSIXErrorENOEXEC: Int](/documentation/coreservices/kposixerrorenoexec)
- [var kPOSIXErrorENOLCK: Int](/documentation/coreservices/kposixerrorenolck)
- [var kPOSIXErrorENOLINK: Int](/documentation/coreservices/kposixerrorenolink)
- [var kPOSIXErrorENOMEM: Int](/documentation/coreservices/kposixerrorenomem)
- [var kPOSIXErrorENOMSG: Int](/documentation/coreservices/kposixerrorenomsg)
- [var kPOSIXErrorENOPROTOOPT: Int](/documentation/coreservices/kposixerrorenoprotoopt)
- [var kPOSIXErrorENOSPC: Int](/documentation/coreservices/kposixerrorenospc)
- [var kPOSIXErrorENOSR: Int](/documentation/coreservices/kposixerrorenosr)
- [var kPOSIXErrorENOSTR: Int](/documentation/coreservices/kposixerrorenostr)
- [var kPOSIXErrorENOSYS: Int](/documentation/coreservices/kposixerrorenosys)
- [var kPOSIXErrorENOTBLK: Int](/documentation/coreservices/kposixerrorenotblk)
- [var kPOSIXErrorENOTCONN: Int](/documentation/coreservices/kposixerrorenotconn)
- [var kPOSIXErrorENOTDIR: Int](/documentation/coreservices/kposixerrorenotdir)
- [var kPOSIXErrorENOTEMPTY: Int](/documentation/coreservices/kposixerrorenotempty)
- [var kPOSIXErrorENOTSOCK: Int](/documentation/coreservices/kposixerrorenotsock)
- [var kPOSIXErrorENOTSUP: Int](/documentation/coreservices/kposixerrorenotsup)
- [var kPOSIXErrorENOTTY: Int](/documentation/coreservices/kposixerrorenotty)
- [var kPOSIXErrorENXIO: Int](/documentation/coreservices/kposixerrorenxio)
- [var kPOSIXErrorEOPNOTSUPP: Int](/documentation/coreservices/kposixerroreopnotsupp)
- [var kPOSIXErrorEOVERFLOW: Int](/documentation/coreservices/kposixerroreoverflow)
- [var kPOSIXErrorEPERM: Int](/documentation/coreservices/kposixerroreperm)
- [var kPOSIXErrorEPFNOSUPPORT: Int](/documentation/coreservices/kposixerrorepfnosupport)
- [var kPOSIXErrorEPIPE: Int](/documentation/coreservices/kposixerrorepipe)
- [var kPOSIXErrorEPROCLIM: Int](/documentation/coreservices/kposixerroreproclim)
- [var kPOSIXErrorEPROCUNAVAIL: Int](/documentation/coreservices/kposixerroreprocunavail)
- [var kPOSIXErrorEPROGMISMATCH: Int](/documentation/coreservices/kposixerroreprogmismatch)
- [var kPOSIXErrorEPROGUNAVAIL: Int](/documentation/coreservices/kposixerroreprogunavail)
- [var kPOSIXErrorEPROTO: Int](/documentation/coreservices/kposixerroreproto)
- [var kPOSIXErrorEPROTONOSUPPORT: Int](/documentation/coreservices/kposixerroreprotonosupport)
- [var kPOSIXErrorEPROTOTYPE: Int](/documentation/coreservices/kposixerroreprototype)
- [var kPOSIXErrorEPWROFF: Int](/documentation/coreservices/kposixerrorepwroff)
- [var kPOSIXErrorERANGE: Int](/documentation/coreservices/kposixerrorerange)
- [var kPOSIXErrorEREMOTE: Int](/documentation/coreservices/kposixerroreremote)
- [var kPOSIXErrorEROFS: Int](/documentation/coreservices/kposixerrorerofs)
- [var kPOSIXErrorERPCMISMATCH: Int](/documentation/coreservices/kposixerrorerpcmismatch)
- [var kPOSIXErrorESHLIBVERS: Int](/documentation/coreservices/kposixerroreshlibvers)
- [var kPOSIXErrorESHUTDOWN: Int](/documentation/coreservices/kposixerroreshutdown)
- [var kPOSIXErrorESOCKTNOSUPPORT: Int](/documentation/coreservices/kposixerroresocktnosupport)
- [var kPOSIXErrorESPIPE: Int](/documentation/coreservices/kposixerrorespipe)
- [var kPOSIXErrorESRCH: Int](/documentation/coreservices/kposixerroresrch)
- [var kPOSIXErrorESTALE: Int](/documentation/coreservices/kposixerrorestale)
- [var kPOSIXErrorETIME: Int](/documentation/coreservices/kposixerroretime)
- [var kPOSIXErrorETIMEDOUT: Int](/documentation/coreservices/kposixerroretimedout)
- [var kPOSIXErrorETOOMANYREFS: Int](/documentation/coreservices/kposixerroretoomanyrefs)
- [var kPOSIXErrorETXTBSY: Int](/documentation/coreservices/kposixerroretxtbsy)
- [var kPOSIXErrorEUSERS: Int](/documentation/coreservices/kposixerroreusers)
- [var kPOSIXErrorEXDEV: Int](/documentation/coreservices/kposixerrorexdev)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1448600-anonymous)

##### Constants

- [var kSKSearchOptionDefault: Int](/documentation/coreservices/ksksearchoptiondefault)
- [var kSKSearchOptionFindSimilar: Int](/documentation/coreservices/ksksearchoptionfindsimilar)
- [var kSKSearchOptionNoRelevanceScores: Int](/documentation/coreservices/ksksearchoptionnorelevancescores)
- [var kSKSearchOptionSpaceMeansOR: Int](/documentation/coreservices/ksksearchoptionspacemeansor)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1390427-anonymous)

##### Constants

- [var kUCCollateCaseInsensitiveMask: Int](/documentation/coreservices/kuccollatecaseinsensitivemask)
- [var kUCCollateComposeInsensitiveMask: Int](/documentation/coreservices/kuccollatecomposeinsensitivemask)
- [var kUCCollateDiacritInsensitiveMask: Int](/documentation/coreservices/kuccollatediacritinsensitivemask)
- [var kUCCollateDigitsAsNumberMask: Int](/documentation/coreservices/kuccollatedigitsasnumbermask)
- [var kUCCollateDigitsOverrideMask: Int](/documentation/coreservices/kuccollatedigitsoverridemask)
- [var kUCCollatePunctuationSignificantMask: Int](/documentation/coreservices/kuccollatepunctuationsignificantmask)
- [var kUCCollateWidthInsensitiveMask: Int](/documentation/coreservices/kuccollatewidthinsensitivemask)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1390624-anonymous)

##### Constants

- [var kUCTSOptionsDataIsOrderedMask: Int](/documentation/coreservices/kuctsoptionsdataisorderedmask)
- [var kUCTSOptionsNoneMask: Int](/documentation/coreservices/kuctsoptionsnonemask)
- [var kUCTSOptionsReleaseStringMask: Int](/documentation/coreservices/kuctsoptionsreleasestringmask)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1390417-anonymous)

##### Constants

- [var kUCTSDirectionNext: Int](/documentation/coreservices/kuctsdirectionnext)
- [var kUCTSDirectionPrevious: Int](/documentation/coreservices/kuctsdirectionprevious)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1390433-anonymous)

##### Constants

- [var kUCTextBreakCharMask: Int](/documentation/coreservices/kuctextbreakcharmask)
- [var kUCTextBreakClusterMask: Int](/documentation/coreservices/kuctextbreakclustermask)
- [var kUCTextBreakLineMask: Int](/documentation/coreservices/kuctextbreaklinemask)
- [var kUCTextBreakParagraphMask: Int](/documentation/coreservices/kuctextbreakparagraphmask)
- [var kUCTextBreakWordMask: Int](/documentation/coreservices/kuctextbreakwordmask)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1390386-anonymous)

##### Constants

- [var kUCTextBreakGoBackwardsMask: Int](/documentation/coreservices/kuctextbreakgobackwardsmask)
- [var kUCTextBreakIterateMask: Int](/documentation/coreservices/kuctextbreakiteratemask)
- [var kUCTextBreakLeadingEdgeMask: Int](/documentation/coreservices/kuctextbreakleadingedgemask)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1390501-anonymous)

##### Constants

- [var kUCTypeSelectMaxListSize: UInt32](/documentation/coreservices/kuctypeselectmaxlistsize)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1429043-anonymous)

##### Constants

- [var kCSIdentityQueryStringBeginsWith: Int](/documentation/coreservices/kcsidentityquerystringbeginswith)
- [var kCSIdentityQueryStringEquals: Int](/documentation/coreservices/kcsidentityquerystringequals)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1428995-anonymous)

##### Constants

- [var kCSIdentityQueryGenerateUpdateEvents: Int](/documentation/coreservices/kcsidentityquerygenerateupdateevents)
- [var kCSIdentityQueryIncludeHiddenIdentities: Int](/documentation/coreservices/kcsidentityqueryincludehiddenidentities)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1429005-anonymous)

##### Constants

- [var kCSIdentityQueryEventErrorOccurred: Int](/documentation/coreservices/kcsidentityqueryeventerroroccurred)
- [var kCSIdentityQueryEventResultsAdded: Int](/documentation/coreservices/kcsidentityqueryeventresultsadded)
- [var kCSIdentityQueryEventResultsChanged: Int](/documentation/coreservices/kcsidentityqueryeventresultschanged)
- [var kCSIdentityQueryEventResultsRemoved: Int](/documentation/coreservices/kcsidentityqueryeventresultsremoved)
- [var kCSIdentityQueryEventSearchPhaseFinished: Int](/documentation/coreservices/kcsidentityqueryeventsearchphasefinished)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556401-anonymous)

##### Constants

- [var typeCFAbsoluteTime: DescType](/documentation/coreservices/typecfabsolutetime)
- [var typeFinderWindow: DescType](/documentation/coreservices/typefinderwindow)
- [var typeFixedPoint: DescType](/documentation/coreservices/typefixedpoint)
- [var typeFixedRectangle: DescType](/documentation/coreservices/typefixedrectangle)
- [var typeGraphicLine: DescType](/documentation/coreservices/typegraphicline)
- [var typeGraphicText: DescType](/documentation/coreservices/typegraphictext)
- [var typeGroupedGraphic: DescType](/documentation/coreservices/typegroupedgraphic)
- [var typeISO8601DateTime: DescType](/documentation/coreservices/typeiso8601datetime)
- [var typeInsertionLoc: DescType](/documentation/coreservices/typeinsertionloc)
- [var typeIntlText: DescType](/documentation/coreservices/typeintltext)
- [var typeIntlWritingCode: DescType](/documentation/coreservices/typeintlwritingcode)
- [var typeLongDateTime: DescType](/documentation/coreservices/typelongdatetime)
- [var typeLongFixed: DescType](/documentation/coreservices/typelongfixed)
- [var typeLongFixedPoint: DescType](/documentation/coreservices/typelongfixedpoint)
- [var typeLongFixedRectangle: DescType](/documentation/coreservices/typelongfixedrectangle)
- [var typeLongPoint: DescType](/documentation/coreservices/typelongpoint)
- [var typeLongRectangle: DescType](/documentation/coreservices/typelongrectangle)
- [var typeMachineLoc: DescType](/documentation/coreservices/typemachineloc)
- [var typeOval: DescType](/documentation/coreservices/typeoval)
- [var typeParamInfo: DescType](/documentation/coreservices/typeparaminfo)
- [var typePict: DescType](/documentation/coreservices/typepict)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556378-anonymous)

##### Constants

- [var keyAEPropData: AEKeyword](/documentation/coreservices/keyaepropdata)
- [var keyAEPropFlags: AEKeyword](/documentation/coreservices/keyaepropflags)
- [var keyAEPropID: AEKeyword](/documentation/coreservices/keyaepropid)
- [var keyAEProperties: AEKeyword](/documentation/coreservices/keyaeproperties)
- [var keyAEProperty: AEKeyword](/documentation/coreservices/keyaeproperty)
- [var keyAEProtection: AEKeyword](/documentation/coreservices/keyaeprotection)
- [var keyAERenderAs: AEKeyword](/documentation/coreservices/keyaerenderas)
- [var keyAERequestedType: AEKeyword](/documentation/coreservices/keyaerequestedtype)
- [var keyAEResult: AEKeyword](/documentation/coreservices/keyaeresult)
- [var keyAEResultInfo: AEKeyword](/documentation/coreservices/keyaeresultinfo)
- [var keyAERotPoint: AEKeyword](/documentation/coreservices/keyaerotpoint)
- [var keyAERotation: AEKeyword](/documentation/coreservices/keyaerotation)
- [var keyAERowList: AEKeyword](/documentation/coreservices/keyaerowlist)
- [var keyAESaveOptions: AEKeyword](/documentation/coreservices/keyaesaveoptions)
- [var keyAEScale: AEKeyword](/documentation/coreservices/keyaescale)
- [var keyAEScriptTag: AEKeyword](/documentation/coreservices/keyaescripttag)
- [var keyAESearchText: AEKeyword](/documentation/coreservices/keyaesearchtext)
- [var keyAEShowWhere: AEKeyword](/documentation/coreservices/keyaeshowwhere)
- [var keyAEStartAngle: AEKeyword](/documentation/coreservices/keyaestartangle)
- [var keyAEStartPoint: AEKeyword](/documentation/coreservices/keyaestartpoint)
- [var keyAEStyles: AEKeyword](/documentation/coreservices/keyaestyles)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556403-anonymous)

##### Constants

- [var kAEGetPrivilegeSelection: OSType](/documentation/coreservices/kaegetprivilegeselection)
- [var kAEGetSuiteInfo: OSType](/documentation/coreservices/kaegetsuiteinfo)
- [var kAEGreaterThan: OSType](/documentation/coreservices/kaegreaterthan)
- [var kAEGreaterThanEquals: OSType](/documentation/coreservices/kaegreaterthanequals)
- [var kAEGrow: OSType](/documentation/coreservices/kaegrow)
- [var kAEHiQuality: OSType](/documentation/coreservices/kaehiquality)
- [var kAEHidden: OSType](/documentation/coreservices/kaehidden)
- [var kAEImageGraphic: OSType](/documentation/coreservices/kaeimagegraphic)
- [var kAEIsUniform: OSType](/documentation/coreservices/kaeisuniform)
- [var kAEItalic: OSType](/documentation/coreservices/kaeitalic)
- [var kAELeftJustified: OSType](/documentation/coreservices/kaeleftjustified)
- [var kAELessThan: OSType](/documentation/coreservices/kaelessthan)
- [var kAELessThanEquals: OSType](/documentation/coreservices/kaelessthanequals)
- [var kAELowercase: OSType](/documentation/coreservices/kaelowercase)
- [var kAEMakeObjectsVisible: OSType](/documentation/coreservices/kaemakeobjectsvisible)
- [var kAEMiscStandards: OSType](/documentation/coreservices/kaemiscstandards)
- [var kAEModifiable: OSType](/documentation/coreservices/kaemodifiable)
- [var kAEMove: OSType](/documentation/coreservices/kaemove)
- [var kAENo: OSType](/documentation/coreservices/kaeno)
- [var kAENoArrow: OSType](/documentation/coreservices/kaenoarrow)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556394-anonymous)

##### Constants

- [var kAEAsk: OSType](/documentation/coreservices/kaeask)
- [var kAEBefore: OSType](/documentation/coreservices/kaebefore)
- [var kAEBeginTransaction: OSType](/documentation/coreservices/kaebegintransaction)
- [var kAEBeginning: OSType](/documentation/coreservices/kaebeginning)
- [var kAEBeginsWith: OSType](/documentation/coreservices/kaebeginswith)
- [var kAEBold: OSType](/documentation/coreservices/kaebold)
- [var kAECaseSensEquals: OSType](/documentation/coreservices/kaecasesensequals)
- [var kAECentered: OSType](/documentation/coreservices/kaecentered)
- [var kAEChangeView: OSType](/documentation/coreservices/kaechangeview)
- [var kAEClone: OSType](/documentation/coreservices/kaeclone)
- [var kAEClose: OSType](/documentation/coreservices/kaeclose)
- [var kAECondensed: OSType](/documentation/coreservices/kaecondensed)
- [var kAEContains: OSType](/documentation/coreservices/kaecontains)
- [var kAECopy: OSType](/documentation/coreservices/kaecopy)
- [var kAECoreSuite: OSType](/documentation/coreservices/kaecoresuite)
- [var kAECountElements: OSType](/documentation/coreservices/kaecountelements)
- [var kAECreateElement: OSType](/documentation/coreservices/kaecreateelement)
- [var kAECreatePublisher: OSType](/documentation/coreservices/kaecreatepublisher)
- [var kAECut: OSType](/documentation/coreservices/kaecut)
- [var kAEDelete: OSType](/documentation/coreservices/kaedelete)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556363-anonymous)

##### Constants

- [var kAEQuitPreserveState: OSType](/documentation/coreservices/kaequitpreservestate)
- [var kAEQuitReason: OSType](/documentation/coreservices/kaequitreason)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556390-anonymous)

##### Constants

- [var kAEDoObjectsExist: OSType](/documentation/coreservices/kaedoobjectsexist)
- [var kAEDoScript: OSType](/documentation/coreservices/kaedoscript)
- [var kAEDrag: OSType](/documentation/coreservices/kaedrag)
- [var kAEDuplicateSelection: OSType](/documentation/coreservices/kaeduplicateselection)
- [var kAEEditGraphic: OSType](/documentation/coreservices/kaeeditgraphic)
- [var kAEEmptyTrash: OSType](/documentation/coreservices/kaeemptytrash)
- [var kAEEnd: OSType](/documentation/coreservices/kaeend)
- [var kAEEndTransaction: OSType](/documentation/coreservices/kaeendtransaction)
- [var kAEEndsWith: OSType](/documentation/coreservices/kaeendswith)
- [var kAEEquals: OSType](/documentation/coreservices/kaeequals)
- [var kAEExpanded: OSType](/documentation/coreservices/kaeexpanded)
- [var kAEFast: OSType](/documentation/coreservices/kaefast)
- [var kAEFinderEvents: OSType](/documentation/coreservices/kaefinderevents)
- [var kAEFormulaProtect: OSType](/documentation/coreservices/kaeformulaprotect)
- [var kAEFullyJustified: OSType](/documentation/coreservices/kaefullyjustified)
- [var kAEGetClassInfo: OSType](/documentation/coreservices/kaegetclassinfo)
- [var kAEGetData: OSType](/documentation/coreservices/kaegetdata)
- [var kAEGetDataSize: OSType](/documentation/coreservices/kaegetdatasize)
- [var kAEGetEventInfo: OSType](/documentation/coreservices/kaegeteventinfo)
- [var kAEGetInfoSelection: OSType](/documentation/coreservices/kaegetinfoselection)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556364-anonymous)

##### Constants

- [var cVersion: OSType](/documentation/coreservices/cversion)
- [var cWindow: OSType](/documentation/coreservices/cwindow)
- [var cWord: OSType](/documentation/coreservices/cword)
- [var enumArrows: OSType](/documentation/coreservices/enumarrows)
- [var enumJustification: OSType](/documentation/coreservices/enumjustification)
- [var enumKeyForm: OSType](/documentation/coreservices/enumkeyform)
- [var enumPosition: OSType](/documentation/coreservices/enumposition)
- [var enumProtection: OSType](/documentation/coreservices/enumprotection)
- [var enumQuality: OSType](/documentation/coreservices/enumquality)
- [var enumSaveOptions: OSType](/documentation/coreservices/enumsaveoptions)
- [var enumStyle: OSType](/documentation/coreservices/enumstyle)
- [var enumTransferMode: OSType](/documentation/coreservices/enumtransfermode)
- [var kAEAbout: OSType](/documentation/coreservices/kaeabout)
- [var kAEAfter: OSType](/documentation/coreservices/kaeafter)
- [var kAEAliasSelection: OSType](/documentation/coreservices/kaealiasselection)
- [var kAEAllCaps: OSType](/documentation/coreservices/kaeallcaps)
- [var kAEArrowAtEnd: OSType](/documentation/coreservices/kaearrowatend)
- [var kAEArrowAtStart: OSType](/documentation/coreservices/kaearrowatstart)
- [var kAEArrowBothEnds: OSType](/documentation/coreservices/kaearrowbothends)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/1556396-anonymous)

##### Constants

- [var typePixMapMinus: DescType](/documentation/coreservices/typepixmapminus)
- [var typePixelMap: DescType](/documentation/coreservices/typepixelmap)
- [var typePolygon: DescType](/documentation/coreservices/typepolygon)
- [var typePropInfo: DescType](/documentation/coreservices/typepropinfo)
- [var typePtr: DescType](/documentation/coreservices/typeptr)
- [var typeQDPoint: DescType](/documentation/coreservices/typeqdpoint)
- [var typeQDRegion: DescType](/documentation/coreservices/typeqdregion)
- [var typeRGB16: DescType](/documentation/coreservices/typergb16)
- [var typeRGB96: DescType](/documentation/coreservices/typergb96)
- [var typeRGBColor: DescType](/documentation/coreservices/typergbcolor)
- [var typeRectangle: DescType](/documentation/coreservices/typerectangle)
- [var typeRotation: DescType](/documentation/coreservices/typerotation)
- [var typeRoundedRectangle: DescType](/documentation/coreservices/typeroundedrectangle)
- [var typeRow: DescType](/documentation/coreservices/typerow)
- [var typeScrapStyles: DescType](/documentation/coreservices/typescrapstyles)
- [var typeScript: DescType](/documentation/coreservices/typescript)
- [var typeStyledText: DescType](/documentation/coreservices/typestyledtext)
- [var typeSuiteInfo: DescType](/documentation/coreservices/typesuiteinfo)
- [var typeTable: DescType](/documentation/coreservices/typetable)
- [var typeTextStyles: DescType](/documentation/coreservices/typetextstyles)
- [cAEList](/documentation/applicationservices/apple_event_manager/1556411-caelist)
- [cInsertionLoc](/documentation/applicationservices/apple_event_manager/1556389-cinsertionloc)
- [cKeystroke](/documentation/applicationservices/apple_event_manager/1556385-ckeystroke)
- [cURL](/documentation/applicationservices/apple_event_manager/1556375-curl)
- [eScheme](/documentation/applicationservices/apple_event_manager/1556397-escheme)
- [kBySmallIcon](/documentation/applicationservices/apple_event_manager/1556391-kbysmallicon)
- [kConnSuite](/documentation/applicationservices/apple_event_manager/1556369-kconnsuite)
- [kFAServerApp](/documentation/applicationservices/apple_event_manager/1556384-kfaserverapp)
- [kLaunchToGetTerminology](/documentation/applicationservices/apple_event_manager/1457909-klaunchtogetterminology)
- [kNextBody](/documentation/applicationservices/apple_event_manager/1556402-knextbody)
- [kOSIZDontOpenResourceFile](/documentation/applicationservices/apple_event_manager/1457903-kosizdontopenresourcefile)
- [kReadExtensionTermsMask](/documentation/applicationservices/apple_event_manager/1457896-kreadextensiontermsmask)
- [kSOAP1999Schema](/documentation/applicationservices/apple_event_manager/1542943-ksoap1999schema)
- [kTSMHiliteCaretPosition](/documentation/applicationservices/apple_event_manager/1556398-ktsmhilitecaretposition)
- [kTSMOutsideOfBody](/documentation/applicationservices/apple_event_manager/1556371-ktsmoutsideofbody)
- [kTextServiceClass](/documentation/applicationservices/apple_event_manager/1556406-ktextserviceclass)
- [pArcAngle](/documentation/applicationservices/apple_event_manager/1556376-parcangle)
- [pFormula](/documentation/applicationservices/apple_event_manager/1556373-pformula)
- [pNewElementLoc](/documentation/applicationservices/apple_event_manager/1556400-pnewelementloc)
- [pScheme](/documentation/applicationservices/apple_event_manager/1556408-pscheme)
- [pTextStyles](/documentation/applicationservices/apple_event_manager/1556367-ptextstyles)
- [typeAEText](/documentation/applicationservices/apple_event_manager/1556366-typeaetext)
- [typeApplicationBundleID](/documentation/applicationservices/apple_event_manager/1542896-typeapplicationbundleid)
- [typeHIMenu](/documentation/applicationservices/apple_event_manager/1556372-typehimenu)
- [typeKernelProcessID](/documentation/applicationservices/apple_event_manager/1542936-typekernelprocessid)
- [typeMeters](/documentation/applicationservices/apple_event_manager/1556382-typemeters)
- [typeReplyPortAttr](/documentation/applicationservices/apple_event_manager/1571649-typereplyportattr)
- [typeTIFF](/documentation/applicationservices/apple_event_manager/1556405-typetiff)
- [typeUnicodeText](/documentation/applicationservices/apple_event_manager/1542918-typeunicodetext)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/3025780-anonymous)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/3025781-anonymous)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/3074489-anonymous)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/4013044-anonymous)
- [Anonymous](/documentation/coreservices/carbon_core/carbon_core_enumerations/4464838-anonymous)
- [Carbon Core Functions](/documentation/coreservices/carbon_core/carbon_core_functions)

#### Functions

- [func AcquireIconRef(IconRef!) -> OSErr](/documentation/coreservices/1441852-acquireiconref)
- [func CompositeIconRef(IconRef!, IconRef!, UnsafeMutablePointer<IconRef?>!) -> OSErr](/documentation/coreservices/1450541-compositeiconref)
- [func CreateCompDescriptor(DescType, UnsafeMutablePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1449155-createcompdescriptor)
- [func CreateLogicalDescriptor(UnsafeMutablePointer<AEDescList>!, DescType, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1445212-createlogicaldescriptor)
- [func CreateObjSpecifier(DescType, UnsafeMutablePointer<AEDesc>!, DescType, UnsafeMutablePointer<AEDesc>!, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1450244-createobjspecifier)
- [func CreateOffsetDescriptor(Int, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1444957-createoffsetdescriptor)
- [func CreateRangeDescriptor(UnsafeMutablePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!, Bool, UnsafeMutablePointer<AEDesc>!) -> OSErr](/documentation/coreservices/1444087-createrangedescriptor)
- [func DCSCopyTextDefinition(DCSDictionary?, CFString, CFRange) -> Unmanaged<CFString>?](/documentation/coreservices/1446842-dcscopytextdefinition)
- [func DCSGetTermRangeInString(DCSDictionary?, CFString, CFIndex) -> CFRange](/documentation/coreservices/1450556-dcsgettermrangeinstring)
- [func DisposeAECoerceDescUPP(AECoerceDescUPP!)](/documentation/coreservices/1448721-disposeaecoercedescupp)
- [func DisposeAECoercePtrUPP(AECoercePtrUPP!)](/documentation/coreservices/1450664-disposeaecoerceptrupp)
- [func DisposeAEDisposeExternalUPP(AEDisposeExternalUPP!)](/documentation/coreservices/1447284-disposeaedisposeexternalupp)
- [func DisposeAEEventHandlerUPP(AEEventHandlerUPP!)](/documentation/coreservices/1442066-disposeaeeventhandlerupp)
- [func DisposeIndexToUCStringUPP(IndexToUCStringUPP!)](/documentation/coreservices/1390390-disposeindextoucstringupp)
- [func DisposeOSLAccessorUPP(OSLAccessorUPP!)](/documentation/coreservices/1444684-disposeoslaccessorupp)
- [func DisposeOSLAdjustMarksUPP(OSLAdjustMarksUPP!)](/documentation/coreservices/1443940-disposeosladjustmarksupp)
- [func DisposeOSLCompareUPP(OSLCompareUPP!)](/documentation/coreservices/1448398-disposeoslcompareupp)
- [func DisposeOSLCountUPP(OSLCountUPP!)](/documentation/coreservices/1443984-disposeoslcountupp)
- [func DisposeOSLDisposeTokenUPP(OSLDisposeTokenUPP!)](/documentation/coreservices/1442670-disposeosldisposetokenupp)
- [func DisposeOSLGetErrDescUPP(OSLGetErrDescUPP!)](/documentation/coreservices/1446061-disposeoslgeterrdescupp)
- [func DisposeOSLGetMarkTokenUPP(OSLGetMarkTokenUPP!)](/documentation/coreservices/1442377-disposeoslgetmarktokenupp)
- [func DisposeOSLMarkUPP(OSLMarkUPP!)](/documentation/coreservices/1449253-disposeoslmarkupp)
- [func GetCustomIconsEnabled(Int16, UnsafeMutablePointer<DarwinBoolean>!) -> OSErr](/documentation/coreservices/1442255-getcustomiconsenabled)
- [func GetIconRef(Int16, OSType, OSType, UnsafeMutablePointer<IconRef?>!) -> OSErr](/documentation/coreservices/1442776-geticonref)
- [func GetIconRefFromFileInfo(UnsafePointer<FSRef>!, Int, UnsafePointer<UniChar>!, FSCatalogInfoBitmap, UnsafePointer<FSCatalogInfo>!, IconServicesUsageFlags, UnsafeMutablePointer<IconRef?>!, UnsafeMutablePointer<Int16>!) -> OSStatus](/documentation/coreservices/1447966-geticonreffromfileinfo)
- [func GetIconRefFromFolder(Int16, Int32, Int32, Int8, Int8, UnsafeMutablePointer<IconRef?>!) -> OSErr](/documentation/coreservices/1441712-geticonreffromfolder)
- [func GetIconRefFromIconFamilyPtr(UnsafePointer<IconFamilyResource>!, Size, UnsafeMutablePointer<IconRef?>!) -> OSStatus](/documentation/coreservices/1443251-geticonreffromiconfamilyptr)
- [func GetIconRefFromTypeInfo(OSType, OSType, CFString!, CFString!, IconServicesUsageFlags, UnsafeMutablePointer<IconRef?>!) -> OSErr](/documentation/coreservices/1445758-geticonreffromtypeinfo)
- [func GetIconRefOwners(IconRef!, UnsafeMutablePointer<UInt16>!) -> OSErr](/documentation/coreservices/1447221-geticonrefowners)
- [func InvokeAECoerceDescUPP(UnsafePointer<AEDesc>!, DescType, SRefCon!, UnsafeMutablePointer<AEDesc>!, AECoerceDescUPP!) -> OSErr](/documentation/coreservices/1445450-invokeaecoercedescupp)
- [func InvokeAECoercePtrUPP(DescType, UnsafeRawPointer!, Size, DescType, SRefCon!, UnsafeMutablePointer<AEDesc>!, AECoercePtrUPP!) -> OSErr](/documentation/coreservices/1447079-invokeaecoerceptrupp)
- [func InvokeAEDisposeExternalUPP(UnsafeRawPointer!, Size, SRefCon!, AEDisposeExternalUPP!)](/documentation/coreservices/1441717-invokeaedisposeexternalupp)
- [func InvokeAEEventHandlerUPP(UnsafePointer<AppleEvent>!, UnsafeMutablePointer<AppleEvent>!, SRefCon!, AEEventHandlerUPP!) -> OSErr](/documentation/coreservices/1446585-invokeaeeventhandlerupp)
- [func InvokeIndexToUCStringUPP(UInt32, UnsafeMutableRawPointer!, UnsafeMutableRawPointer!, UnsafeMutablePointer<Unmanaged<CFString>?>!, UnsafeMutablePointer<UCTypeSelectOptions>!, IndexToUCStringUPP!) -> Bool](/documentation/coreservices/1390660-invokeindextoucstringupp)
- [func InvokeOSLAccessorUPP(DescType, UnsafePointer<AEDesc>!, DescType, DescType, UnsafePointer<AEDesc>!, UnsafeMutablePointer<AEDesc>!, SRefCon!, OSLAccessorUPP!) -> OSErr](/documentation/coreservices/1448978-invokeoslaccessorupp)
- [func InvokeOSLAdjustMarksUPP(Int, Int, UnsafePointer<AEDesc>!, OSLAdjustMarksUPP!) -> OSErr](/documentation/coreservices/1448506-invokeosladjustmarksupp)
- [func InvokeOSLCompareUPP(DescType, UnsafePointer<AEDesc>!, UnsafePointer<AEDesc>!, UnsafeMutablePointer<DarwinBoolean>!, OSLCompareUPP!) -> OSErr](/documentation/coreservices/1443110-invokeoslcompareupp)
- [func InvokeOSLCountUPP(DescType, DescType, UnsafePointer<AEDesc>!, UnsafeMutablePointer<Int>!, OSLCountUPP!) -> OSErr](/documentation/coreservices/1448030-invokeoslcountupp)
- [func InvokeOSLDisposeTokenUPP(UnsafeMutablePointer<AEDesc>!, OSLDisposeTokenUPP!) -> OSErr](/documentation/coreservices/1443963-invokeosldisposetokenupp)
- [func InvokeOSLGetErrDescUPP(UnsafeMutablePointer<UnsafeMutablePointer<AEDesc>?>!, OSLGetErrDescUPP!) -> OSErr](/documentation/coreservices/1448420-invokeoslgeterrdescupp)
- [func InvokeOSLGetMarkTokenUPP(UnsafePointer<AEDesc>!, DescType, UnsafeMutablePointer<AEDesc>!, OSLGetMarkTokenUPP!) -> OSErr](/documentation/coreservices/1441894-invokeoslgetmarktokenupp)
- [func InvokeOSLMarkUPP(UnsafePointer<AEDesc>!, UnsafePointer<AEDesc>!, Int, OSLMarkUPP!) -> OSErr](/documentation/coreservices/1447444-invokeoslmarkupp)
- [func IsDataAvailableInIconRef(OSType, IconRef!) -> Bool](/documentation/coreservices/1446627-isdataavailableiniconref)
- [func IsIconRefComposite(IconRef!, UnsafeMutablePointer<IconRef?>!, UnsafeMutablePointer<IconRef?>!) -> OSErr](/documentation/coreservices/1446300-isiconrefcomposite)
- [func IsValidIconRef(IconRef!) -> Bool](/documentation/coreservices/1450233-isvalidiconref)
- [func LSSetItemAttribute(UnsafePointer<FSRef>!, LSRolesMask, CFString!, CFTypeRef!) -> OSStatus](/documentation/coreservices/1446733-lssetitemattribute)
- [func LSSharedFileListAddObserver(LSSharedFileList?, CFRunLoop, CFString, LSSharedFileListChangedProcPtr, UnsafeMutableRawPointer?)](/documentation/coreservices/1445770-lssharedfilelistaddobserver)
- [func LSSharedFileListCopyProperty(LSSharedFileList, CFString) -> Unmanaged<CFTypeRef>?](/documentation/coreservices/1444588-lssharedfilelistcopyproperty)
- [func LSSharedFileListCopySnapshot(LSSharedFileList, UnsafeMutablePointer<UInt32>?) -> Unmanaged<CFArray>?](/documentation/coreservices/1448112-lssharedfilelistcopysnapshot)
- [func LSSharedFileListCreate(CFAllocator?, CFString, CFTypeRef?) -> Unmanaged<LSSharedFileList>?](/documentation/coreservices/1443926-lssharedfilelistcreate)
- [func LSSharedFileListGetSeedValue(LSSharedFileList) -> UInt32](/documentation/coreservices/1444885-lssharedfilelistgetseedvalue)
- [func LSSharedFileListGetTypeID() -> CFTypeID](/documentation/coreservices/1450618-lssharedfilelistgettypeid)
- [func LSSharedFileListInsertItemFSRef(LSSharedFileList, LSSharedFileListItem, CFString?, IconRef?, UnsafePointer<FSRef>, CFDictionary?, CFArray?) -> LSSharedFileListItem?](/documentation/coreservices/1449884-lssharedfilelistinsertitemfsref)
- [func LSSharedFileListInsertItemURL(LSSharedFileList, LSSharedFileListItem, CFString?, IconRef?, CFURL, CFDictionary?, CFArray?) -> LSSharedFileListItem?](/documentation/coreservices/1444471-lssharedfilelistinsertitemurl)
- [func LSSharedFileListItemCopyDisplayName(LSSharedFileListItem) -> Unmanaged<CFString>](/documentation/coreservices/1449716-lssharedfilelistitemcopydisplayn)
- [func LSSharedFileListItemCopyIconRef(LSSharedFileListItem) -> IconRef](/documentation/coreservices/1442889-lssharedfilelistitemcopyiconref)
- [func LSSharedFileListItemCopyProperty(LSSharedFileListItem, CFString) -> Unmanaged<CFTypeRef>?](/documentation/coreservices/1445074-lssharedfilelistitemcopyproperty)
- [func LSSharedFileListItemCopyResolvedURL(LSSharedFileListItem, LSSharedFileListResolutionFlags, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Unmanaged<CFURL>?](/documentation/coreservices/1449882-lssharedfilelistitemcopyresolved)
- [func LSSharedFileListItemGetID(LSSharedFileListItem) -> UInt32](/documentation/coreservices/1443305-lssharedfilelistitemgetid)
- [func LSSharedFileListItemGetTypeID() -> CFTypeID](/documentation/coreservices/1447138-lssharedfilelistitemgettypeid)
- [func LSSharedFileListItemMove(LSSharedFileList, LSSharedFileListItem, LSSharedFileListItem) -> OSStatus](/documentation/coreservices/1444348-lssharedfilelistitemmove)
- [func LSSharedFileListItemRemove(LSSharedFileList, LSSharedFileListItem) -> OSStatus](/documentation/coreservices/1442025-lssharedfilelistitemremove)
- [func LSSharedFileListItemResolve(LSSharedFileListItem, LSSharedFileListResolutionFlags, UnsafeMutablePointer<Unmanaged<CFURL>?>?, UnsafeMutablePointer<FSRef>?) -> OSStatus](/documentation/coreservices/1447347-lssharedfilelistitemresolve)
- [func LSSharedFileListItemSetProperty(LSSharedFileListItem, CFString, CFTypeRef) -> OSStatus](/documentation/coreservices/1445766-lssharedfilelistitemsetproperty)
- [func LSSharedFileListRemoveAllItems(LSSharedFileList) -> OSStatus](/documentation/coreservices/1446389-lssharedfilelistremoveallitems)
- [func LSSharedFileListRemoveObserver(LSSharedFileList, CFRunLoop, CFString, LSSharedFileListChangedProcPtr, UnsafeMutableRawPointer?)](/documentation/coreservices/1443404-lssharedfilelistremoveobserver)
- [func LSSharedFileListSetAuthorization(LSSharedFileList, AuthorizationRef) -> OSStatus](/documentation/coreservices/1446834-lssharedfilelistsetauthorization)
- [func LSSharedFileListSetProperty(LSSharedFileList, CFString, CFTypeRef?) -> OSStatus](/documentation/coreservices/1448857-lssharedfilelistsetproperty)
- [func MDCopyLabelKinds() -> CFArray!](/documentation/coreservices/1442887-mdcopylabelkinds)
- [func MDCopyLabelWithUUID(CFUUID!) -> MDLabel!](/documentation/coreservices/1447030-mdcopylabelwithuuid)
- [func MDCopyLabelsMatchingExpression(CFString!) -> CFArray!](/documentation/coreservices/1448237-mdcopylabelsmatchingexpression)
- [func MDCopyLabelsWithKind(CFString!) -> CFArray!](/documentation/coreservices/1444230-mdcopylabelswithkind)
- [func MDItemCopyLabels(MDItem!) -> CFArray!](/documentation/coreservices/1442606-mditemcopylabels)
- [func MDItemRemoveLabel(MDItem!, MDLabel!) -> Bool](/documentation/coreservices/1446067-mditemremovelabel)
- [func MDItemSetLabel(MDItem!, MDLabel!) -> Bool](/documentation/coreservices/1442559-mditemsetlabel)
- [func MDItemsCopyAttributes(CFArray!, CFArray!) -> CFArray!](/documentation/coreservices/1426975-mditemscopyattributes)
- [func MDItemsCreateWithURLs(CFAllocator!, CFArray!) -> CFArray!](/documentation/coreservices/1427086-mditemscreatewithurls)
- [func MDLabelCopyAttribute(MDLabel!, CFString!) -> CFTypeRef!](/documentation/coreservices/1445456-mdlabelcopyattribute)
- [func MDLabelCopyAttributeName(MDLabel!) -> CFString!](/documentation/coreservices/1445522-mdlabelcopyattributename)
- [func MDLabelCreate(CFAllocator!, CFString!, CFString!, MDLabelDomain) -> MDLabel!](/documentation/coreservices/1442614-mdlabelcreate)
- [func MDLabelDelete(MDLabel!) -> Bool](/documentation/coreservices/1449203-mdlabeldelete)
- [func MDLabelGetTypeID() -> CFTypeID](/documentation/coreservices/1446579-mdlabelgettypeid)
- [func MDLabelSetAttributes(MDLabel!, CFDictionary!) -> Bool](/documentation/coreservices/1449005-mdlabelsetattributes)
- [func MDQueryCreateForItems(CFAllocator!, CFString!, CFArray!, CFArray!, CFArray!) -> MDQuery!](/documentation/coreservices/1413031-mdquerycreateforitems)
- [func MDQueryGetSortOptionFlagsForAttribute(MDQuery!, CFString!) -> UInt32](/documentation/coreservices/1413013-mdquerygetsortoptionflagsforattr)
- [func MDQuerySetSortOptionFlagsForAttribute(MDQuery!, CFString!, UInt32) -> Bool](/documentation/coreservices/1413075-mdquerysetsortoptionflagsforattr)
- [func MDQuerySetSortOrder(MDQuery!, CFArray!) -> Bool](/documentation/coreservices/1413096-mdquerysetsortorder)
- [func NewAECoerceDescUPP(AECoerceDescProcPtr!) -> AECoerceDescUPP!](/documentation/coreservices/1445885-newaecoercedescupp)
- [func NewAECoercePtrUPP(AECoercePtrProcPtr!) -> AECoercePtrUPP!](/documentation/coreservices/1449962-newaecoerceptrupp)
- [func NewAEDisposeExternalUPP(AEDisposeExternalProcPtr!) -> AEDisposeExternalUPP!](/documentation/coreservices/1447774-newaedisposeexternalupp)
- [func NewAEEventHandlerUPP(AEEventHandlerProcPtr!) -> AEEventHandlerUPP!](/documentation/coreservices/1446862-newaeeventhandlerupp)
- [func NewIndexToUCStringUPP(IndexToUCStringProcPtr!) -> IndexToUCStringUPP!](/documentation/coreservices/1390384-newindextoucstringupp)
- [func NewOSLAccessorUPP(OSLAccessorProcPtr!) -> OSLAccessorUPP!](/documentation/coreservices/1449584-newoslaccessorupp)
- [func NewOSLAdjustMarksUPP(OSLAdjustMarksProcPtr!) -> OSLAdjustMarksUPP!](/documentation/coreservices/1443347-newosladjustmarksupp)
- [func NewOSLCompareUPP(OSLCompareProcPtr!) -> OSLCompareUPP!](/documentation/coreservices/1444603-newoslcompareupp)
- [func NewOSLCountUPP(OSLCountProcPtr!) -> OSLCountUPP!](/documentation/coreservices/1448156-newoslcountupp)
- [func NewOSLDisposeTokenUPP(OSLDisposeTokenProcPtr!) -> OSLDisposeTokenUPP!](/documentation/coreservices/1450027-newosldisposetokenupp)
- [func NewOSLGetErrDescUPP(OSLGetErrDescProcPtr!) -> OSLGetErrDescUPP!](/documentation/coreservices/1447934-newoslgeterrdescupp)
- [func NewOSLGetMarkTokenUPP(OSLGetMarkTokenProcPtr!) -> OSLGetMarkTokenUPP!](/documentation/coreservices/1445166-newoslgetmarktokenupp)
- [func NewOSLMarkUPP(OSLMarkProcPtr!) -> OSLMarkUPP!](/documentation/coreservices/1446942-newoslmarkupp)
- [func OverrideIconRef(IconRef!, IconRef!) -> OSErr](/documentation/coreservices/1445253-overrideiconref)
- [func ReadIconFromFSRef(UnsafePointer<FSRef>!, UnsafeMutablePointer<IconFamilyHandle?>!) -> OSStatus](/documentation/coreservices/1444939-readiconfromfsref)
- [func RegisterIconRefFromFSRef(OSType, OSType, UnsafePointer<FSRef>!, UnsafeMutablePointer<IconRef?>!) -> OSStatus](/documentation/coreservices/1446795-registericonreffromfsref)
- [func RegisterIconRefFromIconFamily(OSType, OSType, IconFamilyHandle!, UnsafeMutablePointer<IconRef?>!) -> OSErr](/documentation/coreservices/1443918-registericonreffromiconfamily)
- [func ReleaseIconRef(IconRef!) -> OSErr](/documentation/coreservices/1443504-releaseiconref)
- [func RemoveIconRefOverride(IconRef!) -> OSErr](/documentation/coreservices/1445832-removeiconrefoverride)
- [func SetCustomIconsEnabled(Int16, Bool) -> OSErr](/documentation/coreservices/1449302-setcustomiconsenabled)
- [func UCTypeSelectAddKeyToSelector(UCTypeSelectRef!, CFString!, Double, UnsafeMutablePointer<DarwinBoolean>!) -> OSStatus](/documentation/coreservices/1390517-uctypeselectaddkeytoselector)
- [func UCTypeSelectCompare(UCTypeSelectRef!, CFString!, UnsafeMutablePointer<UCTypeSelectCompareResult>!) -> OSStatus](/documentation/coreservices/1390474-uctypeselectcompare)
- [func UCTypeSelectCreateSelector(LocaleRef!, LocaleOperationVariant, UCCollateOptions, UnsafeMutablePointer<UCTypeSelectRef?>!) -> OSStatus](/documentation/coreservices/1390445-uctypeselectcreateselector)
- [func UCTypeSelectFindItem(UCTypeSelectRef!, UInt32, UnsafeMutableRawPointer!, UnsafeMutableRawPointer!, IndexToUCStringUPP!, UnsafeMutablePointer<UInt32>!) -> OSStatus](/documentation/coreservices/1390368-uctypeselectfinditem)
- [func UCTypeSelectFlushSelectorData(UCTypeSelectRef!) -> OSStatus](/documentation/coreservices/1390367-uctypeselectflushselectordata)
- [func UCTypeSelectReleaseSelector(UnsafeMutablePointer<UCTypeSelectRef?>!) -> OSStatus](/documentation/coreservices/1390644-uctypeselectreleaseselector)
- [func UCTypeSelectWalkList(UCTypeSelectRef!, CFString!, UCTSWalkDirection, UInt32, UnsafeMutableRawPointer!, UnsafeMutableRawPointer!, IndexToUCStringUPP!, UnsafeMutablePointer<UInt32>!) -> OSStatus](/documentation/coreservices/1390442-uctypeselectwalklist)
- [func UCTypeSelectWouldResetBuffer(UCTypeSelectRef!, CFString!, Double) -> Bool](/documentation/coreservices/1390538-uctypeselectwouldresetbuffer)
- [func UTCreateStringForOSType(OSType) -> Unmanaged<CFString>](/documentation/coreservices/1442804-utcreatestringforostype)
- [func UTGetOSTypeFromString(CFString) -> OSType](/documentation/coreservices/1450472-utgetostypefromstring)
- [func UTTypeConformsTo(CFString, CFString) -> Bool](/documentation/coreservices/1444079-uttypeconformsto)
- [func UTTypeCopyAllTagsWithClass(CFString, CFString) -> Unmanaged<CFArray>?](/documentation/coreservices/1448473-uttypecopyalltagswithclass)
- [func UTTypeCopyDeclaration(CFString) -> Unmanaged<CFDictionary>?](/documentation/coreservices/1442505-uttypecopydeclaration)
- [func UTTypeCopyDeclaringBundleURL(CFString) -> Unmanaged<CFURL>?](/documentation/coreservices/1447781-uttypecopydeclaringbundleurl)
- [func UTTypeCopyDescription(CFString) -> Unmanaged<CFString>?](/documentation/coreservices/1448514-uttypecopydescription)
- [func UTTypeCopyPreferredTagWithClass(CFString, CFString) -> Unmanaged<CFString>?](/documentation/coreservices/1442744-uttypecopypreferredtagwithclass)
- [func UTTypeCreateAllIdentifiersForTag(CFString, CFString, CFString?) -> Unmanaged<CFArray>?](/documentation/coreservices/1447261-uttypecreateallidentifiersfortag)
- [func UTTypeCreatePreferredIdentifierForTag(CFString, CFString, CFString?) -> Unmanaged<CFString>?](/documentation/coreservices/1448939-uttypecreatepreferredidentifierf)
- [func UTTypeEqual(CFString, CFString) -> Bool](/documentation/coreservices/1447783-uttypeequal)
- [func UTTypeIsDeclared(CFString) -> Bool](/documentation/coreservices/1450352-uttypeisdeclared)
- [func UTTypeIsDynamic(CFString) -> Bool](/documentation/coreservices/1442980-uttypeisdynamic)
- [func UnregisterIconRef(OSType, OSType) -> OSErr](/documentation/coreservices/1444660-unregistericonref)
- [func UpdateIconRef(IconRef!) -> OSErr](/documentation/coreservices/1445921-updateiconref)
- [func vAEBuildAppleEvent(AEEventClass, AEEventID, DescType, UnsafeRawPointer!, Size, Int16, Int32, UnsafeMutablePointer<AppleEvent>!, UnsafeMutablePointer<AEBuildError>!, UnsafePointer<CChar>!, CVaListPointer) -> OSStatus](/documentation/coreservices/1441729-vaebuildappleevent)
- [func vAEBuildDesc(UnsafeMutablePointer<AEDesc>!, UnsafeMutablePointer<AEBuildError>!, UnsafePointer<CChar>!, CVaListPointer) -> OSStatus](/documentation/coreservices/1446775-vaebuilddesc)
- [func vAEBuildParameters(UnsafeMutablePointer<AppleEvent>!, UnsafeMutablePointer<AEBuildError>!, UnsafePointer<CChar>!, CVaListPointer) -> OSStatus](/documentation/coreservices/1448040-vaebuildparameters)
- [func AEDeterminePermissionToAutomateTarget(UnsafePointer<AEAddressDesc>!, AEEventClass, AEEventID, Bool) -> OSStatus](/documentation/coreservices/3025784-aedeterminepermissiontoautomatet)
- [func AEUnflattenDescFromBytes(UnsafeRawPointer!, Int, UnsafeMutablePointer<AEDesc>!) -> OSStatus](/documentation/coreservices/3553279-aeunflattendescfrombytes)
- [func MDItemGetCacheFileDescriptors(CFArray!, ((CFArray?) -> Void)!)](/documentation/coreservices/4485578-mditemgetcachefiledescriptors)
- [Carbon Core Data Types](/documentation/coreservices/carbon_core/carbon_core_data_types)

#### Data Types

- [AppleEvent](/documentation/coreservices/appleevent)
- [AppleEventPtr](/documentation/coreservices/appleeventptr)
- [CSDiskSpaceRecoveryCallback](/documentation/coreservices/csdiskspacerecoverycallback)
- [CSDiskSpaceRecoveryOptions](/documentation/coreservices/csdiskspacerecoveryoptions)
- [CSIdentityClass](/documentation/coreservices/csidentityclass)
- [CSIdentityFlags](/documentation/coreservices/csidentityflags)
- [CSIdentityQueryEvent](/documentation/coreservices/csidentityqueryevent)
- [CSIdentityQueryFlags](/documentation/coreservices/csidentityqueryflags)
- [CSIdentityQueryReceiveEventCallback](/documentation/coreservices/csidentityqueryreceiveeventcallback)
- [CSIdentityQueryStringComparisonMethod](/documentation/coreservices/csidentityquerystringcomparisonmethod)
- [CSIdentityStatusUpdatedCallback](/documentation/coreservices/csidentitystatusupdatedcallback)
- [ConstFSEventStreamRef](/documentation/coreservices/constfseventstreamref)
- [DescType](/documentation/coreservices/desctype)
- [IndexToUCStringProcPtr](/documentation/coreservices/indextoucstringprocptr)
- [IndexToUCStringUPP](/documentation/coreservices/indextoucstringupp)
- [LSSharedFileListChangedProcPtr](/documentation/coreservices/lssharedfilelistchangedprocptr)
- [LSSharedFileListResolutionFlags](/documentation/coreservices/lssharedfilelistresolutionflags)
- [OffsetArrayHandle](/documentation/coreservices/offsetarrayhandle)
- [OffsetArrayPtr](/documentation/coreservices/offsetarrayptr)
- [TextRangeArrayHandle](/documentation/coreservices/textrangearrayhandle)
- [TextRangeArrayPtr](/documentation/coreservices/textrangearrayptr)
- [TextRangeHandle](/documentation/coreservices/textrangehandle)
- [TextRangePtr](/documentation/coreservices/textrangeptr)
- [UCTSWalkDirection](/documentation/coreservices/uctswalkdirection)
- [UCTypeSelectCompareResult](/documentation/coreservices/uctypeselectcompareresult)
- [UCTypeSelectOptions](/documentation/coreservices/uctypeselectoptions)
- [UCTypeSelectRef](/documentation/coreservices/uctypeselectref)
- [ccntTokenRecHandle](/documentation/coreservices/ccnttokenrechandle)
- [ccntTokenRecPtr](/documentation/coreservices/ccnttokenrecptr)
- [Core Services Constants](/documentation/coreservices/core_services_constants)

### Constants

- [var kFSEventStreamEventExtendedDocIDKey: String](/documentation/coreservices/kfseventstreameventextendeddocidkey)
- [let kMDItemMediaExtensions: CFString!](/documentation/coreservices/kmditemmediaextensions)
- [let kMDItemXMPCredit: CFString!](/documentation/coreservices/kmditemxmpcredit)
- [let kMDItemXMPDigitalSourceType: CFString!](/documentation/coreservices/kmditemxmpdigitalsourcetype)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
