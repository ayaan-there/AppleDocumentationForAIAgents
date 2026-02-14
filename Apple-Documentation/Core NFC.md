# Core NFC Documentation

Source: https://sosumi.ai/documentation/corenfc

---
title: Core NFC
source: https://developer.apple.com/documentation/corenfc
timestamp: 2026-02-13T18:55:36.152Z
---

## Essentials

- [Building an NFC Tag-Reader App](/documentation/corenfc/building-an-nfc-tag-reader-app)
- [Adding Support for Background Tag Reading](/documentation/corenfc/adding-support-for-background-tag-reading)
- [NFCReaderUsageDescription](/documentation/bundleresources/information-property-list/nfcreaderusagedescription)

## Reader sessions

- [NFCNDEFReaderSession](/documentation/corenfc/nfcndefreadersession)

### Creating a Session

- [init(delegate: any NFCNDEFReaderSessionDelegate, queue: dispatch_queue_t?, invalidateAfterFirstRead: Bool)](/documentation/corenfc/nfcndefreadersession/init(delegate:queue:invalidateafterfirstread:))
- [NFCNDEFReaderSessionDelegate](/documentation/corenfc/nfcndefreadersessiondelegate)

#### Handling Session Activation

- [func readerSessionDidBecomeActive(NFCNDEFReaderSession)](/documentation/corenfc/nfcndefreadersessiondelegate/readersessiondidbecomeactive(_:))

#### Finding NDEF Messages and Tags

- [func readerSession(NFCNDEFReaderSession, didDetectNDEFs: [NFCNDEFMessage])](/documentation/corenfc/nfcndefreadersessiondelegate/readersession(_:diddetectndefs:))
- [func readerSession(NFCNDEFReaderSession, didDetect: [any NFCNDEFTag])](/documentation/corenfc/nfcndefreadersessiondelegate/readersession(_:diddetect:))

#### Handling an Invalidated Session

- [func readerSession(NFCNDEFReaderSession, didInvalidateWithError: any Error)](/documentation/corenfc/nfcndefreadersessiondelegate/readersession(_:didinvalidatewitherror:))

### Connecting to a Tag

- [func connect(to: any NFCNDEFTag, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfcndefreadersession/connect(to:completionhandler:))

### Restarting the Polling Sequence

- [func restartPolling()](/documentation/corenfc/nfcndefreadersession/restartpolling())
- [NFCTagReaderSession](/documentation/corenfc/nfctagreadersession)

### Creating a Tag Reader Session

- [convenience init?(pollingOption: NFCTagReaderSession.PollingOption, delegate: any NFCTagReaderSessionDelegate, queue: DispatchQueue?)](/documentation/corenfc/nfctagreadersession/init(pollingoption:delegate:queue:))
- [NFCTagReaderSession.PollingOption](/documentation/corenfc/nfctagreadersession/pollingoption)

#### Polling Options

- [static var iso14443: NFCTagReaderSession.PollingOption](/documentation/corenfc/nfctagreadersession/pollingoption/iso14443)
- [static var iso15693: NFCTagReaderSession.PollingOption](/documentation/corenfc/nfctagreadersession/pollingoption/iso15693)
- [static var iso18092: NFCTagReaderSession.PollingOption](/documentation/corenfc/nfctagreadersession/pollingoption/iso18092)

#### Initializers

- [init(rawValue: Int)](/documentation/corenfc/nfctagreadersession/pollingoption/init(rawvalue:))

#### Type Properties

- [static var pace: NFCTagReaderSession.PollingOption](/documentation/corenfc/nfctagreadersession/pollingoption/pace)
- [NFCTagReaderSessionDelegate](/documentation/corenfc/nfctagreadersessiondelegate-2joku)

#### Handling Session Activation

- [func tagReaderSessionDidBecomeActive(NFCTagReaderSession)](/documentation/corenfc/nfctagreadersessiondelegate-2joku/tagreadersessiondidbecomeactive(_:))

#### Finding NFC Tags

- [func tagReaderSession(NFCTagReaderSession, didDetect: [NFCTag])](/documentation/corenfc/nfctagreadersessiondelegate-2joku/tagreadersession(_:diddetect:))

#### Handling an Invalidated Session

- [func tagReaderSession(NFCTagReaderSession, didInvalidateWithError: any Error)](/documentation/corenfc/nfctagreadersessiondelegate-2joku/tagreadersession(_:didinvalidatewitherror:))

### Connecting to a Tag

- [func connect(to: NFCTag, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfctagreadersession/connect(to:completionhandler:))
- [var connectedTag: NFCTag?](/documentation/corenfc/nfctagreadersession/connectedtag-3mlqu)

### Restarting the Polling Sequence

- [func restartPolling()](/documentation/corenfc/nfctagreadersession/restartpolling())

### Instance Methods

- [func connect(to: NFCTag) async throws](/documentation/corenfc/nfctagreadersession/connect(to:))
- [NFCPaymentTagReaderSession](/documentation/corenfc/nfcpaymenttagreadersession)

### Creating a tag reader session

- [convenience init(delegate: any NFCTagReaderSessionDelegate, queue: DispatchQueue?)](/documentation/corenfc/nfcpaymenttagreadersession/init(delegate:queue:))
- [NFCTagReaderSessionDelegate](/documentation/corenfc/nfctagreadersessiondelegate-2joku)

#### Handling Session Activation

- [func tagReaderSessionDidBecomeActive(NFCTagReaderSession)](/documentation/corenfc/nfctagreadersessiondelegate-2joku/tagreadersessiondidbecomeactive(_:))

#### Finding NFC Tags

- [func tagReaderSession(NFCTagReaderSession, didDetect: [NFCTag])](/documentation/corenfc/nfctagreadersessiondelegate-2joku/tagreadersession(_:diddetect:))

#### Handling an Invalidated Session

- [func tagReaderSession(NFCTagReaderSession, didInvalidateWithError: any Error)](/documentation/corenfc/nfctagreadersessiondelegate-2joku/tagreadersession(_:didinvalidatewitherror:))
- [NFCVASReaderSession](/documentation/corenfc/nfcvasreadersession)

### Creating a VAS Reader Session

- [init(vasCommandConfigurations: [NFCVASCommandConfiguration], delegate: any NFCVASReaderSessionDelegate, queue: dispatch_queue_t?)](/documentation/corenfc/nfcvasreadersession/init(vascommandconfigurations:delegate:queue:))
- [NFCVASCommandConfiguration](/documentation/corenfc/nfcvascommandconfiguration)

#### Creating a Command Configuration

- [init(vasMode: NFCVASCommandConfiguration.Mode, passTypeIdentifier: String, url: URL?)](/documentation/corenfc/nfcvascommandconfiguration/init(vasmode:passtypeidentifier:url:))

#### Setting Configuration Items

- [var mode: NFCVASCommandConfiguration.Mode](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.property)
- [VASMode](/documentation/corenfc/vasmode)

##### Modes

- [static var VASModeNormal: NFCVASCommandConfiguration.Mode](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.enum/vasmodenormal)
- [var passTypeIdentifier: String](/documentation/corenfc/nfcvascommandconfiguration/passtypeidentifier)
- [var url: URL?](/documentation/corenfc/nfcvascommandconfiguration/url)
- [NFCVASReaderSessionDelegate](/documentation/corenfc/nfcvasreadersessiondelegate)

#### Handling Session Activation

- [func readerSessionDidBecomeActive(NFCVASReaderSession)](/documentation/corenfc/nfcvasreadersessiondelegate/readersessiondidbecomeactive(_:))

#### Receiving VAS Responses

- [func readerSession(NFCVASReaderSession, didReceive: [NFCVASResponse])](/documentation/corenfc/nfcvasreadersessiondelegate/readersession(_:didreceive:))
- [NFCVASResponse](/documentation/corenfc/nfcvasresponse)

##### Getting the Response Status

- [var status: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/status)
- [VASErrorCode](/documentation/corenfc/vaserrorcode)

###### Status Codes

- [static var VASErrorCodeSuccess: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodesuccess)
- [static var VASErrorCodeUserIntervention: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodeuserintervention)

###### Data Codes

- [static var VASErrorCodeDataNotActivated: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodedatanotactivated)
- [static var VASErrorCodeDataNotFound: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodedatanotfound)
- [static var VASErrorCodeIncorrectData: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodeincorrectdata)

###### Error Codes

- [static var VASErrorCodeUnsupportedApplicationVersion: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodeunsupportedapplicationversion)
- [static var VASErrorCodeWrongLCField: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodewronglcfield)
- [static var VASErrorCodeWrongParameters: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodewrongparameters)

##### Getting the VAS Data

- [var vasData: Data](/documentation/corenfc/nfcvasresponse/vasdata)

##### Getting the Mobile Token

- [var mobileToken: Data](/documentation/corenfc/nfcvasresponse/mobiletoken)

#### Handling an Invalidated Session

- [func readerSession(NFCVASReaderSession, didInvalidateWithError: any Error)](/documentation/corenfc/nfcvasreadersessiondelegate/readersession(_:didinvalidatewitherror:))
- [NFCReaderSession](/documentation/corenfc/nfcreadersession-swift.class)

### Determining Tag Reading Capability

- [class var readingAvailable: Bool](/documentation/corenfc/nfcreadersession-swift.class/readingavailable)

### Working with a Session

- [var delegate: AnyObject?](/documentation/corenfc/nfcreadersession-swift.class/delegate)
- [var sessionQueue: dispatch_queue_t](/documentation/corenfc/nfcreadersession-swift.class/sessionqueue)
- [NFCReaderSessionProtocol](/documentation/corenfc/nfcreadersessionprotocol)

### Determining Reader Session Readiness

- [var isReady: Bool](/documentation/corenfc/nfcreadersessionprotocol/isready)
- [var isReady: Bool](/documentation/corenfc/nfcreadersessionprotocol/isready)

### Managing a Reader Session

- [func begin()](/documentation/corenfc/nfcreadersessionprotocol/begin())
- [func invalidate()](/documentation/corenfc/nfcreadersessionprotocol/invalidate())
- [func invalidate(errorMessage: String)](/documentation/corenfc/nfcreadersessionprotocol/invalidate(errormessage:))
- [var alertMessage: String](/documentation/corenfc/nfcreadersessionprotocol/alertmessage)
- [func begin()](/documentation/corenfc/nfcreadersessionprotocol/begin())
- [func invalidate()](/documentation/corenfc/nfcreadersessionprotocol/invalidate())
- [func invalidate(errorMessage: String)](/documentation/corenfc/nfcreadersessionprotocol/invalidate(errormessage:))
- [var alertMessage: String](/documentation/corenfc/nfcreadersessionprotocol/alertmessage)
- [Near Field Communication Tag Reader Session Formats Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.nfc.readersession.formats)

## Tag types

- [Creating NFC Tags from Your iPhone](/documentation/corenfc/creating-nfc-tags-from-your-iphone)
- [NFCISO7816Tag](/documentation/corenfc/nfciso7816tag)

### Specifying Application Identifiers

- [ISO7816 application identifiers for NFC Tag Reader Session](/documentation/bundleresources/entitlements/com.apple.developer.nfc.readersession.iso7816.select-identifiers)

### Getting Tag Information

- [var initialSelectedAID: String](/documentation/corenfc/nfciso7816tag/initialselectedaid)
- [var identifier: Data](/documentation/corenfc/nfciso7816tag/identifier)
- [var historicalBytes: Data?](/documentation/corenfc/nfciso7816tag/historicalbytes)
- [var applicationData: Data?](/documentation/corenfc/nfciso7816tag/applicationdata)
- [var proprietaryApplicationDataCoding: Bool](/documentation/corenfc/nfciso7816tag/proprietaryapplicationdatacoding)

### Sending a Command

- [func sendCommand(apdu: NFCISO7816APDU, resultHandler: (Result<NFCISO7816ResponseAPDU, any Error>) -> Void)](/documentation/corenfc/nfciso7816tag/sendcommand(apdu:resulthandler:))
- [func sendCommand(apdu: NFCISO7816APDU, completionHandler: (Data, UInt8, UInt8, (any Error)?) -> Void)](/documentation/corenfc/nfciso7816tag/sendcommand(apdu:completionhandler:))
- [NFCISO7816APDU](/documentation/corenfc/nfciso7816apdu)

#### Creating an APDU Object

- [init(instructionClass: UInt8, instructionCode: UInt8, p1Parameter: UInt8, p2Parameter: UInt8, data: Data, expectedResponseLength: Int)](/documentation/corenfc/nfciso7816apdu/init(instructionclass:instructioncode:p1parameter:p2parameter:data:expectedresponselength:))
- [init?(data: Data)](/documentation/corenfc/nfciso7816apdu/init(data:))

#### Getting the Instruction Bytes

- [var instructionClass: UInt8](/documentation/corenfc/nfciso7816apdu/instructionclass)
- [var instructionCode: UInt8](/documentation/corenfc/nfciso7816apdu/instructioncode)

#### Get the Parameter Bytes

- [var p1Parameter: UInt8](/documentation/corenfc/nfciso7816apdu/p1parameter)
- [var p2Parameter: UInt8](/documentation/corenfc/nfciso7816apdu/p2parameter)

#### Getting the APDU Data

- [var data: Data?](/documentation/corenfc/nfciso7816apdu/data)

#### Getting the Expected Response Length

- [var expectedResponseLength: Int](/documentation/corenfc/nfciso7816apdu/expectedresponselength)
- [NFCISO7816ResponseAPDU](/documentation/corenfc/nfciso7816responseapdu)

#### Response Data

- [var payload: Data?](/documentation/corenfc/nfciso7816responseapdu/payload)
- [var statusWord1: UInt8](/documentation/corenfc/nfciso7816responseapdu/statusword1)
- [var statusWord2: UInt8](/documentation/corenfc/nfciso7816responseapdu/statusword2)
- [NFCISO15693Tag](/documentation/corenfc/nfciso15693tag)

### Getting Tag Information

- [var icManufacturerCode: Int](/documentation/corenfc/nfciso15693tag/icmanufacturercode)
- [var icSerialNumber: Data](/documentation/corenfc/nfciso15693tag/icserialnumber)
- [var identifier: Data](/documentation/corenfc/nfciso15693tag/identifier)

### Selecting Request Flag Options

- [RequestFlag](/documentation/corenfc/requestflag)

#### Request Flags

- [static var RequestFlagDualSubCarriers: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagdualsubcarriers)
- [static var RequestFlagHighDataRate: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflaghighdatarate)
- [static var RequestFlagProtocolExtension: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagprotocolextension)
- [static var RequestFlagSelect: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagselect)
- [static var RequestFlagAddress: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagaddress)
- [static var RequestFlagOption: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagoption)

### Getting System Information

- [func getSystemInfo(requestFlags: NFCISO15693RequestFlag, completionHandler: (Int, Int, Int, Int, Int, (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/getsysteminfo(requestflags:completionhandler:))

### Sending Single Block Commands

- [func readSingleBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: UInt8, completionHandler: (Data, (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/readsingleblock(requestflags:blocknumber:completionhandler:))
- [func writeSingleBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: UInt8, dataBlock: Data, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/writesingleblock(requestflags:blocknumber:datablock:completionhandler:))
- [func lockBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: UInt8, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/lockblock(requestflags:blocknumber:completionhandler:))

### Sending Multi-block Commands

- [func readMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, completionHandler: ([Data], (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/readmultipleblocks(requestflags:blockrange:completionhandler:))
- [func writeMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, dataBlocks: [Data], completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/writemultipleblocks(requestflags:blockrange:datablocks:completionhandler:))
- [func getMultipleBlockSecurityStatus(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, completionHandler: ([NSNumber], (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/getmultipleblocksecuritystatus(requestflags:blockrange:completionhandler:))

### Sending Application Family Identifier Commands

- [func writeAFI(requestFlags: NFCISO15693RequestFlag, afi: UInt8, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/writeafi(requestflags:afi:completionhandler:))
- [func lockAFI(requestFlags: NFCISO15693RequestFlag, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/lockafi(requestflags:completionhandler:))

### Sending Data Storage Format Identifier Commands

- [func writeDSFID(requestFlags: NFCISO15693RequestFlag, dsfid: UInt8, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/writedsfid(requestflags:dsfid:completionhandler:))
- [func lockDFSID(requestFlags: NFCISO15693RequestFlag, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/lockdfsid(requestflags:completionhandler:))

### Sending Reset to Ready Command

- [func resetToReady(requestFlags: NFCISO15693RequestFlag, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/resettoready(requestflags:completionhandler:))

### Sending Select Command

- [func select(requestFlags: NFCISO15693RequestFlag, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/select(requestflags:completionhandler:))

### Sending Stay Quiet Command

- [func stayQuiet(completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/stayquiet(completionhandler:))

### Sending Custom Commands

- [func customCommand(requestFlags: NFCISO15693RequestFlag, customCommandCode: Int, customRequestParameters: Data, completionHandler: (Data, (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/customcommand(requestflags:customcommandcode:customrequestparameters:completionhandler:))

### Sending Extended Commands

- [func extendedReadSingleBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: Int, completionHandler: (Data, (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/extendedreadsingleblock(requestflags:blocknumber:completionhandler:))
- [func extendedWriteSingleBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: Int, dataBlock: Data, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/extendedwritesingleblock(requestflags:blocknumber:datablock:completionhandler:))
- [func extendedLockBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: Int, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/extendedlockblock(requestflags:blocknumber:completionhandler:))
- [func extendedReadMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, completionHandler: ([Data], (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/extendedreadmultipleblocks(requestflags:blockrange:completionhandler:))

### Getting Response Errors

- [let NFCISO15693TagResponseErrorKey: String](/documentation/corenfc/nfciso15693tagresponseerrorkey)

### Instance Methods

- [func authenticate(requestFlags: NFCISO15693RequestFlag, cryptoSuiteIdentifier: Int, message: Data) async throws -> (NFCISO15693ResponseFlag, Data)](/documentation/corenfc/nfciso15693tag/authenticate(requestflags:cryptosuiteidentifier:message:))
- [func authenticate(requestFlags: NFCISO15693RequestFlag, cryptoSuiteIdentifier: Int, message: Data, resultHandler: (Result<(NFCISO15693ResponseFlag, Data), any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/authenticate(requestflags:cryptosuiteidentifier:message:resulthandler:))
- [func challenge(requestFlags: NFCISO15693RequestFlag, cryptoSuiteIdentifier: Int, message: Data) async throws](/documentation/corenfc/nfciso15693tag/challenge(requestflags:cryptosuiteidentifier:message:))
- [func challenge(requestFlags: NFCISO15693RequestFlag, cryptoSuiteIdentifier: Int, message: Data, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/challenge(requestflags:cryptosuiteidentifier:message:completionhandler:))
- [func customCommand(requestFlags: NFCISO15693RequestFlag, customCommandCode: Int, customRequestParameters: Data, resultHandler: (Result<Data, any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/customcommand(requestflags:customcommandcode:customrequestparameters:resulthandler:))
- [func extendedFastReadMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange) async throws -> [Data]](/documentation/corenfc/nfciso15693tag/extendedfastreadmultipleblocks(requestflags:blockrange:))
- [func extendedFastReadMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, resultHandler: (Result<[Data], any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/extendedfastreadmultipleblocks(requestflags:blockrange:resulthandler:))
- [func extendedGetMultipleBlockSecurityStatus(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange) async throws -> NFCISO15693MultipleBlockSecurityStatus](/documentation/corenfc/nfciso15693tag/extendedgetmultipleblocksecuritystatus(requestflags:blockrange:))
- [func extendedGetMultipleBlockSecurityStatus(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, resultHandler: (Result<NFCISO15693MultipleBlockSecurityStatus, any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/extendedgetmultipleblocksecuritystatus(requestflags:blockrange:resulthandler:))
- [func extendedReadSingleBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: Int, resultHandler: (Result<Data, any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/extendedreadsingleblock(requestflags:blocknumber:resulthandler:))
- [func extendedWriteMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, dataBlocks: [Data]) async throws](/documentation/corenfc/nfciso15693tag/extendedwritemultipleblocks(requestflags:blockrange:datablocks:))
- [func extendedWriteMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, dataBlocks: [Data], completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/extendedwritemultipleblocks(requestflags:blockrange:datablocks:completionhandler:))
- [func fastReadMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange) async throws -> [Data]](/documentation/corenfc/nfciso15693tag/fastreadmultipleblocks(requestflags:blockrange:))
- [func fastReadMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, resultHandler: (Result<[Data], any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/fastreadmultipleblocks(requestflags:blockrange:resulthandler:))
- [func getSystemInfo(requestFlags: NFCISO15693RequestFlag, resultHandler: (Result<NFCISO15693SystemInfo, any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/getsysteminfo(requestflags:resulthandler:))
- [func keyUpdate(requestFlags: NFCISO15693RequestFlag, keyIdentifier: Int, message: Data) async throws -> (NFCISO15693ResponseFlag, Data)](/documentation/corenfc/nfciso15693tag/keyupdate(requestflags:keyidentifier:message:))
- [func keyUpdate(requestFlags: NFCISO15693RequestFlag, keyIdentifier: Int, message: Data, resultHandler: (Result<(NFCISO15693ResponseFlag, Data), any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/keyupdate(requestflags:keyidentifier:message:resulthandler:))
- [func lockDSFID(requestFlags: NFCISO15693RequestFlag, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/lockdsfid(requestflags:completionhandler:))
- [func readBuffer(requestFlags: NFCISO15693RequestFlag) async throws -> (NFCISO15693ResponseFlag, Data)](/documentation/corenfc/nfciso15693tag/readbuffer(requestflags:))
- [func readBuffer(requestFlags: NFCISO15693RequestFlag, resultHandler: (Result<(NFCISO15693ResponseFlag, Data), any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/readbuffer(requestflags:resulthandler:))
- [func readMultipleBlock(readConfiguration: NFCISO15693ReadMultipleBlocksConfiguration, completionHandler: (Data, (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/readmultipleblock(readconfiguration:completionhandler:))
- [func readMultipleBlocks(requestFlags: NFCISO15693RequestFlag, blockRange: NSRange, resultHandler: (Result<[Data], any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/readmultipleblocks(requestflags:blockrange:resulthandler:))
- [func readSingleBlock(requestFlags: NFCISO15693RequestFlag, blockNumber: UInt8, resultHandler: (Result<Data, any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/readsingleblock(requestflags:blocknumber:resulthandler:))
- [func sendCustomCommand(commandConfiguration: NFCISO15693CustomCommandConfiguration, completionHandler: (Data, (any Error)?) -> Void)](/documentation/corenfc/nfciso15693tag/sendcustomcommand(commandconfiguration:completionhandler:))
- [func sendRequest(requestFlags: Int, commandCode: Int, data: Data?) async throws -> (NFCISO15693ResponseFlag, Data?)](/documentation/corenfc/nfciso15693tag/sendrequest(requestflags:commandcode:data:))
- [func sendRequest(requestFlags: Int, commandCode: Int, data: Data?, resultHandler: (Result<(NFCISO15693ResponseFlag, Data?), any Error>) -> Void)](/documentation/corenfc/nfciso15693tag/sendrequest(requestflags:commandcode:data:resulthandler:))
- [func systemInfo(requestFlags: NFCISO15693RequestFlag) async throws -> NFCISO15693SystemInfo](/documentation/corenfc/nfciso15693tag/systeminfo(requestflags:))
- [NFCFeliCaTag](/documentation/corenfc/nfcfelicatag)

### Specifying System Codes

- [ISO18092 system codes for NFC Tag Reader Session](/documentation/bundleresources/entitlements/com.apple.developer.nfc.readersession.felica.systemcodes)

### Getting Current Information

- [var currentSystemCode: Data](/documentation/corenfc/nfcfelicatag/currentsystemcode)
- [var currentIDm: Data](/documentation/corenfc/nfcfelicatag/currentidm)

### Polling

- [func polling(systemCode: Data, requestCode: NFCFeliCaPollingRequestCode, timeSlot: NFCFeliCaPollingTimeSlot, completionHandler: (Data, Data, (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/polling(systemcode:requestcode:timeslot:completionhandler:))
- [PollingRequestCode](/documentation/corenfc/pollingrequestcode)

#### Request Codes

- [static var PollingRequestCodeNoRequest: NFCFeliCaPollingRequestCode](/documentation/corenfc/nfcfelicapollingrequestcode/pollingrequestcodenorequest)
- [static var PollingRequestCodeSystemCode: NFCFeliCaPollingRequestCode](/documentation/corenfc/nfcfelicapollingrequestcode/pollingrequestcodesystemcode)
- [static var PollingRequestCodeCommunicationPerformance: NFCFeliCaPollingRequestCode](/documentation/corenfc/nfcfelicapollingrequestcode/pollingrequestcodecommunicationperformance)
- [PollingTimeSlot](/documentation/corenfc/pollingtimeslot)

#### Maximum Slots

- [static var PollingTimeSlotMax1: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax1)
- [static var PollingTimeSlotMax2: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax2)
- [static var PollingTimeSlotMax4: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax4)
- [static var PollingTimeSlotMax8: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax8)
- [static var PollingTimeSlotMax16: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax16)

### Requesting Services

- [func requestService(nodeCodeList: [Data], completionHandler: ([Data], (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/requestservice(nodecodelist:completionhandler:))
- [func requestServiceV2(nodeCodeList: [Data], completionHandler: (Int, Int, NFCFeliCaEncryptionId, [Data], [Data], (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/requestservicev2(nodecodelist:completionhandler:))
- [EncryptionId](/documentation/corenfc/encryptionid)

#### Identifiers

- [static var aes: NFCFeliCaEncryptionId](/documentation/corenfc/nfcfelicaencryptionid/aes-swift.type.property)
- [static var aes_des: NFCFeliCaEncryptionId](/documentation/corenfc/nfcfelicaencryptionid/aes_des-swift.type.property)

### Requesting Responses

- [func requestResponse(completionHandler: (Int, (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/requestresponse(completionhandler:))

### Requesting Specification Versions

- [func requestSpecificationVersion(completionHandler: (Int, Int, Data, Data, (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/requestspecificationversion(completionhandler:))

### Requesting System Codes

- [func requestSystemCode(completionHandler: ([Data], (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/requestsystemcode(completionhandler:))

### Resetting Modes

- [func resetMode(completionHandler: (Int, Int, (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/resetmode(completionhandler:))

### Reading and Writing Without Encryption

- [func readWithoutEncryption(serviceCodeList: [Data], blockList: [Data], completionHandler: (Int, Int, [Data], (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/readwithoutencryption(servicecodelist:blocklist:completionhandler:))
- [func writeWithoutEncryption(serviceCodeList: [Data], blockList: [Data], blockData: [Data], completionHandler: (Int, Int, (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/writewithoutencryption(servicecodelist:blocklist:blockdata:completionhandler:))

### Sending FeliCa Commands

- [func sendFeliCaCommand(commandPacket: Data, completionHandler: (Data, (any Error)?) -> Void)](/documentation/corenfc/nfcfelicatag/sendfelicacommand(commandpacket:completionhandler:))

### Instance Methods

- [func polling(systemCode: Data, requestCode: NFCFeliCaPollingRequestCode, timeSlot: NFCFeliCaPollingTimeSlot, resultHandler: (Result<NFCFeliCaPollingResponse, any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/polling(systemcode:requestcode:timeslot:resulthandler:))
- [func readWithoutEncryption(serviceCodeList: [Data], blockList: [Data], resultHandler: (Result<(NFCFeliCaStatusFlag, [Data]), any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/readwithoutencryption(servicecodelist:blocklist:resulthandler:))
- [func requestResponse(resultHandler: (Result<Int, any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/requestresponse(resulthandler:))
- [func requestService(nodeCodeList: [Data], resultHandler: (Result<[Data], any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/requestservice(nodecodelist:resulthandler:))
- [func requestServiceV2(nodeCodeList: [Data], resultHandler: (Result<NFCFeliCaRequsetServiceV2Response, any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/requestservicev2(nodecodelist:resulthandler:))
- [func requestSpecificationVersion(resultHandler: (Result<NFCFeliCaRequestSpecificationVersionResponse, any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/requestspecificationversion(resulthandler:))
- [func requestSystemCode(resultHandler: (Result<[Data], any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/requestsystemcode(resulthandler:))
- [func resetMode(resultHandler: (Result<NFCFeliCaStatusFlag, any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/resetmode(resulthandler:))
- [func sendFeliCaCommand(commandPacket: Data, resultHandler: (Result<Data, any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/sendfelicacommand(commandpacket:resulthandler:))
- [func writeWithoutEncryption(serviceCodeList: [Data], blockList: [Data], blockData: [Data], resultHandler: (Result<NFCFeliCaStatusFlag, any Error>) -> Void)](/documentation/corenfc/nfcfelicatag/writewithoutencryption(servicecodelist:blocklist:blockdata:resulthandler:))
- [NFCMiFareTag](/documentation/corenfc/nfcmifaretag)

### Getting Tag Information

- [var mifareFamily: NFCMiFareFamily](/documentation/corenfc/nfcmifaretag/mifarefamily)
- [NFCMiFareFamily](/documentation/corenfc/nfcmifarefamily)

#### Product Families

- [case unknown](/documentation/corenfc/nfcmifarefamily/unknown)
- [case ultralight](/documentation/corenfc/nfcmifarefamily/ultralight)
- [case plus](/documentation/corenfc/nfcmifarefamily/plus)
- [case desfire](/documentation/corenfc/nfcmifarefamily/desfire)

#### Initializers

- [init?(rawValue: UInt)](/documentation/corenfc/nfcmifarefamily/init(rawvalue:))
- [var identifier: Data](/documentation/corenfc/nfcmifaretag/identifier)
- [var historicalBytes: Data?](/documentation/corenfc/nfcmifaretag/historicalbytes)

### Sending Commands

- [func sendMiFareCommand(commandPacket: Data, completionHandler: (Data, (any Error)?) -> Void)](/documentation/corenfc/nfcmifaretag/sendmifarecommand(commandpacket:completionhandler:))
- [func sendMiFareISO7816Command(NFCISO7816APDU, completionHandler: (Data, UInt8, UInt8, (any Error)?) -> Void)](/documentation/corenfc/nfcmifaretag/sendmifareiso7816command(_:completionhandler:))

### Instance Methods

- [func sendMiFareCommand(commandPacket: Data, resultHandler: (Result<Data, any Error>) -> Void)](/documentation/corenfc/nfcmifaretag/sendmifarecommand(commandpacket:resulthandler:))
- [func sendMiFareISO7816Command(NFCISO7816APDU, resultHandler: (Result<NFCISO7816ResponseAPDU, any Error>) -> Void)](/documentation/corenfc/nfcmifaretag/sendmifareiso7816command(_:resulthandler:))
- [NFCNDEFTag](/documentation/corenfc/nfcndeftag)

### Getting the Tag Status

- [var isAvailable: Bool](/documentation/corenfc/nfcndeftag/isavailable)
- [func queryNDEFStatus(completionHandler: (NFCNDEFStatus, Int, (any Error)?) -> Void)](/documentation/corenfc/nfcndeftag/queryndefstatus(completionhandler:))
- [NFCNDEFStatus](/documentation/corenfc/nfcndefstatus)

#### Statuses

- [case notSupported](/documentation/corenfc/nfcndefstatus/notsupported)
- [case readOnly](/documentation/corenfc/nfcndefstatus/readonly)
- [case readWrite](/documentation/corenfc/nfcndefstatus/readwrite)

#### Initializers

- [init?(rawValue: UInt)](/documentation/corenfc/nfcndefstatus/init(rawvalue:))

### Reading the Tag

- [func readNDEF(completionHandler: (NFCNDEFMessage?, (any Error)?) -> Void)](/documentation/corenfc/nfcndeftag/readndef(completionhandler:))

### Writing to the Tag

- [func writeNDEF(NFCNDEFMessage, completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfcndeftag/writendef(_:completionhandler:))
- [func writeLock(completionHandler: ((any Error)?) -> Void)](/documentation/corenfc/nfcndeftag/writelock(completionhandler:))
- [NFCTag](/documentation/corenfc/nfctag-swift.enum)

### Getting Information About a Tag

- [var isAvailable: Bool](/documentation/corenfc/nfctag-swift.enum/isavailable)

### Getting a Specific Tag Type

- [case iso15693(any NFCISO15693Tag)](/documentation/corenfc/nfctag-swift.enum/iso15693(_:))
- [case iso7816(any NFCISO7816Tag)](/documentation/corenfc/nfctag-swift.enum/iso7816(_:))
- [case feliCa(any NFCFeliCaTag)](/documentation/corenfc/nfctag-swift.enum/felica(_:))
- [case miFare(any NFCMiFareTag)](/documentation/corenfc/nfctag-swift.enum/mifare(_:))
- [NFCTagCommandConfiguration](/documentation/corenfc/nfctagcommandconfiguration)

### Configuring a Tag Command

- [var maximumRetries: Int](/documentation/corenfc/nfctagcommandconfiguration/maximumretries)
- [var retryInterval: TimeInterval](/documentation/corenfc/nfctagcommandconfiguration/retryinterval)

## NDEF messages and payloads

- [NFCNDEFMessage](/documentation/corenfc/nfcndefmessage)

### Creating an NDEF Message

- [init(records: [NFCNDEFPayload])](/documentation/corenfc/nfcndefmessage/init(records:))
- [convenience init?(data: Data)](/documentation/corenfc/nfcndefmessage/init(data:))

### Accessing NDEF Records

- [var records: [NFCNDEFPayload]](/documentation/corenfc/nfcndefmessage/records)

### Getting the Message Length

- [var length: Int](/documentation/corenfc/nfcndefmessage/length)
- [NFCNDEFPayload](/documentation/corenfc/nfcndefpayload)

### Creating a Payload Record

- [class func wellKnownTypeURIPayload(url: URL) -> Self?](/documentation/corenfc/nfcndefpayload/wellknowntypeuripayload(url:))
- [class func wellKnownTypeURIPayload(string: String) -> Self?](/documentation/corenfc/nfcndefpayload/wellknowntypeuripayload(string:))
- [class func wellKnownTypeTextPayload(string: String, locale: Locale) -> Self?](/documentation/corenfc/nfcndefpayload/wellknowntypetextpayload(string:locale:))
- [init(format: NFCTypeNameFormat, type: Data, identifier: Data, payload: Data)](/documentation/corenfc/nfcndefpayload/init(format:type:identifier:payload:))
- [init(format: NFCTypeNameFormat, type: Data, identifier: Data, payload: Data, chunkSize: Int)](/documentation/corenfc/nfcndefpayload/init(format:type:identifier:payload:chunksize:))
- [class func wellKnowTypeTextPayload(string: String, locale: Locale) -> Self?](/documentation/corenfc/nfcndefpayload/wellknowtypetextpayload(string:locale:))

### Getting Information About a Payload Record

- [var identifier: Data](/documentation/corenfc/nfcndefpayload/identifier)
- [var payload: Data](/documentation/corenfc/nfcndefpayload/payload)
- [var type: Data](/documentation/corenfc/nfcndefpayload/type)
- [var typeNameFormat: NFCTypeNameFormat](/documentation/corenfc/nfcndefpayload/typenameformat)
- [NFCTypeNameFormat](/documentation/corenfc/nfctypenameformat)

#### Content Types

- [case absoluteURI](/documentation/corenfc/nfctypenameformat/absoluteuri)
- [case empty](/documentation/corenfc/nfctypenameformat/empty)
- [case media](/documentation/corenfc/nfctypenameformat/media)
- [case nfcExternal](/documentation/corenfc/nfctypenameformat/nfcexternal)
- [case nfcWellKnown](/documentation/corenfc/nfctypenameformat/nfcwellknown)
- [case unchanged](/documentation/corenfc/nfctypenameformat/unchanged)
- [case unknown](/documentation/corenfc/nfctypenameformat/unknown)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/corenfc/nfctypenameformat/init(rawvalue:))

### Getting the URI from a Payload Record

- [func wellKnownTypeURIPayload() -> URL?](/documentation/corenfc/nfcndefpayload/wellknowntypeuripayload())

### Getting Text from a Payload Record

- [func wellKnownTypeTextPayload() -> (String?, Locale?)](/documentation/corenfc/nfcndefpayload/wellknowntypetextpayload())

## Card sessions

- [CardSession](/documentation/corenfc/cardsession)

### Creating a card session

- [init() async throws](/documentation/corenfc/cardsession/init())
- [CardSession.Error](/documentation/corenfc/cardsession/error)

#### Card session errors

- [case invalidated](/documentation/corenfc/cardsession/error/invalidated)
- [case userInvalidated](/documentation/corenfc/cardsession/error/userinvalidated)
- [case maxSessionDurationReached](/documentation/corenfc/cardsession/error/maxsessiondurationreached)
- [case transmissionError](/documentation/corenfc/cardsession/error/transmissionerror)
- [case systemNotAvailable](/documentation/corenfc/cardsession/error/systemnotavailable)
- [case accessNotAccepted](/documentation/corenfc/cardsession/error/accessnotaccepted)
- [case systemEligibilityFailed](/documentation/corenfc/cardsession/error/systemeligibilityfailed)
- [case emulationStopped](/documentation/corenfc/cardsession/error/emulationstopped)
- [case radioDisabled](/documentation/corenfc/cardsession/error/radiodisabled)

### Determining card session availability

- [class var isSupported: Bool](/documentation/corenfc/cardsession/issupported)
- [static var isEligible: Bool](/documentation/corenfc/cardsession/iseligible)

### Managing card emulation

- [func startEmulation() async throws](/documentation/corenfc/cardsession/startemulation())
- [CardSession.Error](/documentation/corenfc/cardsession/error)

#### Card session errors

- [case invalidated](/documentation/corenfc/cardsession/error/invalidated)
- [case userInvalidated](/documentation/corenfc/cardsession/error/userinvalidated)
- [case maxSessionDurationReached](/documentation/corenfc/cardsession/error/maxsessiondurationreached)
- [case transmissionError](/documentation/corenfc/cardsession/error/transmissionerror)
- [case systemNotAvailable](/documentation/corenfc/cardsession/error/systemnotavailable)
- [case accessNotAccepted](/documentation/corenfc/cardsession/error/accessnotaccepted)
- [case systemEligibilityFailed](/documentation/corenfc/cardsession/error/systemeligibilityfailed)
- [case emulationStopped](/documentation/corenfc/cardsession/error/emulationstopped)
- [case radioDisabled](/documentation/corenfc/cardsession/error/radiodisabled)
- [func stopEmulation(status: CardSession.EmulationUIStatus) async](/documentation/corenfc/cardsession/stopemulation(status:))
- [CardSession.EmulationUIStatus](/documentation/corenfc/cardsession/emulationuistatus)

#### Emulation statuses

- [case success](/documentation/corenfc/cardsession/emulationuistatus/success)
- [case failure](/documentation/corenfc/cardsession/emulationuistatus/failure)
- [var isEmulationInProgress: Bool](/documentation/corenfc/cardsession/isemulationinprogress)

### Handling card events

- [var eventStream: CardSession.EventStream](/documentation/corenfc/cardsession/eventstream-swift.property)
- [CardSession.EventStream](/documentation/corenfc/cardsession/eventstream-swift.class)

#### Creating an iterator

- [CardSession.EventStream.Iterator](/documentation/corenfc/cardsession/eventstream-swift.class/iterator)
- [CardSession.Event](/documentation/corenfc/cardsession/event)

#### Events

- [case sessionStarted](/documentation/corenfc/cardsession/event/sessionstarted)
- [case readerDetected](/documentation/corenfc/cardsession/event/readerdetected)
- [case received(CardSession.APDU)](/documentation/corenfc/cardsession/event/received(_:))
- [CardSession.APDU](/documentation/corenfc/cardsession/apdu)

##### Receiving data

- [let payload: Data](/documentation/corenfc/cardsession/apdu/payload)

##### Communicating with the card session

- [func respond(response: Data) async throws](/documentation/corenfc/cardsession/apdu/respond(response:))
- [case readerDeselected](/documentation/corenfc/cardsession/event/readerdeselected)
- [case sessionInvalidated(reason: CardSession.Error)](/documentation/corenfc/cardsession/event/sessioninvalidated(reason:))

### Updating the user interface

- [var alertMessage: String](/documentation/corenfc/cardsession/alertmessage)

### Ending a card session

- [func invalidate()](/documentation/corenfc/cardsession/invalidate())

### Entitlements

- [com.apple.developer.nfc.hce](/documentation/bundleresources/entitlements/com.apple.developer.nfc.hce)
- [com.apple.developer.nfc.hce.iso7816.select-identifier-prefixes](/documentation/bundleresources/entitlements/com.apple.developer.nfc.hce.iso7816.select-identifier-prefixes)
- [com.apple.developer.nfc.hce.default-contactless-app](/documentation/bundleresources/entitlements/com.apple.developer.nfc.hce.default-contactless-app)

### Classes

- [CardSession.APDU](/documentation/corenfc/cardsession/apdu)

#### Receiving data

- [let payload: Data](/documentation/corenfc/cardsession/apdu/payload)

#### Communicating with the card session

- [func respond(response: Data) async throws](/documentation/corenfc/cardsession/apdu/respond(response:))
- [NFCPresentmentIntentAssertion](/documentation/corenfc/nfcpresentmentintentassertion)

### Acquiring a presentment intention instance

- [static func acquire() async throws -> NFCPresentmentIntentAssertion](/documentation/corenfc/nfcpresentmentintentassertion/acquire())

### Testing presentment intention validity

- [var isValid: Bool](/documentation/corenfc/nfcpresentmentintentassertion/isvalid)
- [NFCPresentmentIntentAssertion.Error](/documentation/corenfc/nfcpresentmentintentassertion/error)

#### Presentment intent assertion errors

- [case systemEligibilityFailed](/documentation/corenfc/nfcpresentmentintentassertion/error/systemeligibilityfailed)
- [case systemNotAvailable](/documentation/corenfc/nfcpresentmentintentassertion/error/systemnotavailable)

## NFC window scenes

- [NFCWindowSceneDelegate](/documentation/corenfc/nfcwindowscenedelegate)

### Handling events

- [func windowScene(UIWindowScene, didReceiveNFCWindowSceneEvent: NFCWindowSceneEvent)](/documentation/corenfc/nfcwindowscenedelegate/windowscene(_:didreceivenfcwindowsceneevent:))
- [NFCWindowSceneEvent](/documentation/corenfc/nfcwindowsceneevent)

#### Events

- [case readerDetected](/documentation/corenfc/nfcwindowsceneevent/readerdetected)
- [case presentation](/documentation/corenfc/nfcwindowsceneevent/presentation)
- [NFCWindowSceneEvent](/documentation/corenfc/nfcwindowsceneevent)

### Events

- [case readerDetected](/documentation/corenfc/nfcwindowsceneevent/readerdetected)
- [case presentation](/documentation/corenfc/nfcwindowsceneevent/presentation)

## Errors

- [NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/code)

### Session Errors

- [case readerSessionInvalidationErrorFirstNDEFTagRead](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorfirstndeftagread)
- [case readerSessionInvalidationErrorSessionTerminatedUnexpectedly](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorsessionterminatedunexpectedly)
- [case readerSessionInvalidationErrorSessionTimeout](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorsessiontimeout)
- [case readerSessionInvalidationErrorSystemIsBusy](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorsystemisbusy)
- [case readerSessionInvalidationErrorUserCanceled](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorusercanceled)
- [case readerSessionInvalidationErrorFirstNDEFTagRead](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorfirstndeftagread)
- [case readerSessionInvalidationErrorSessionTerminatedUnexpectedly](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorsessionterminatedunexpectedly)
- [case readerSessionInvalidationErrorSessionTimeout](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorsessiontimeout)
- [case readerSessionInvalidationErrorSystemIsBusy](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorsystemisbusy)
- [case readerSessionInvalidationErrorUserCanceled](/documentation/corenfc/nfcreadererror-swift.struct/code/readersessioninvalidationerrorusercanceled)

### NDEF Tag Errors

- [case ndefReaderSessionErrorTagNotWritable](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrortagnotwritable)
- [case ndefReaderSessionErrorTagSizeTooSmall](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrortagsizetoosmall)
- [case ndefReaderSessionErrorTagUpdateFailure](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrortagupdatefailure)
- [case ndefReaderSessionErrorZeroLengthMessage](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrorzerolengthmessage)
- [case ndefReaderSessionErrorTagNotWritable](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrortagnotwritable)
- [case ndefReaderSessionErrorTagSizeTooSmall](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrortagsizetoosmall)
- [case ndefReaderSessionErrorTagUpdateFailure](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrortagupdatefailure)
- [case ndefReaderSessionErrorZeroLengthMessage](/documentation/corenfc/nfcreadererror-swift.struct/code/ndefreadersessionerrorzerolengthmessage)

### Transceive Errors

- [case readerTransceiveErrorRetryExceeded](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrorretryexceeded)
- [case readerTransceiveErrorTagConnectionLost](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrortagconnectionlost)
- [case readerTransceiveErrorTagNotConnected](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrortagnotconnected)
- [case readerTransceiveErrorTagResponseError](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrortagresponseerror)
- [case readerTransceiveErrorSessionInvalidated](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrorsessioninvalidated)
- [case readerTransceiveErrorPacketTooLong](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrorpackettoolong)
- [case readerTransceiveErrorRetryExceeded](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrorretryexceeded)
- [case readerTransceiveErrorTagConnectionLost](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrortagconnectionlost)
- [case readerTransceiveErrorTagNotConnected](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrortagnotconnected)
- [case readerTransceiveErrorTagResponseError](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrortagresponseerror)
- [case readerTransceiveErrorSessionInvalidated](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrorsessioninvalidated)
- [case readerTransceiveErrorPacketTooLong](/documentation/corenfc/nfcreadererror-swift.struct/code/readertransceiveerrorpackettoolong)

### Tag Command Configuration Error

- [case tagCommandConfigurationErrorInvalidParameters](/documentation/corenfc/nfcreadererror-swift.struct/code/tagcommandconfigurationerrorinvalidparameters)
- [case tagCommandConfigurationErrorInvalidParameters](/documentation/corenfc/nfcreadererror-swift.struct/code/tagcommandconfigurationerrorinvalidparameters)

### Other Errors

- [case readerErrorUnsupportedFeature](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorunsupportedfeature)
- [case readerErrorInvalidParameter](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorinvalidparameter)
- [case readerErrorInvalidParameterLength](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorinvalidparameterlength)
- [case readerErrorParameterOutOfBound](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorparameteroutofbound)
- [case readerErrorRadioDisabled](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorradiodisabled)
- [case readerErrorSecurityViolation](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorsecurityviolation)
- [case readerErrorUnsupportedFeature](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorunsupportedfeature)
- [case readerErrorInvalidParameter](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorinvalidparameter)
- [case readerErrorInvalidParameterLength](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorinvalidparameterlength)
- [case readerErrorParameterOutOfBound](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorparameteroutofbound)
- [case readerErrorRadioDisabled](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorradiodisabled)
- [case readerErrorSecurityViolation](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorsecurityviolation)

### Enumeration Cases

- [case readerErrorAccessNotAccepted](/documentation/corenfc/nfcreadererror-swift.struct/code/readererroraccessnotaccepted)
- [case readerErrorIneligible](/documentation/corenfc/nfcreadererror-swift.struct/code/readererrorineligible)

### Initializers

- [init?(rawValue: Int)](/documentation/corenfc/nfcreadererror-swift.struct/code/init(rawvalue:))
- [NFCReaderError](/documentation/corenfc/nfcreadererror-swift.struct)

### Session Errors

- [static var readerSessionInvalidationErrorFirstNDEFTagRead: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readersessioninvalidationerrorfirstndeftagread)
- [static var readerSessionInvalidationErrorSessionTerminatedUnexpectedly: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readersessioninvalidationerrorsessionterminatedunexpectedly)
- [static var readerSessionInvalidationErrorSessionTimeout: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readersessioninvalidationerrorsessiontimeout)
- [static var readerSessionInvalidationErrorSystemIsBusy: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readersessioninvalidationerrorsystemisbusy)
- [static var readerSessionInvalidationErrorUserCanceled: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readersessioninvalidationerrorusercanceled)

### NDEF Tag Errors

- [static var ndefReaderSessionErrorTagNotWritable: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/ndefreadersessionerrortagnotwritable)
- [static var ndefReaderSessionErrorTagSizeTooSmall: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/ndefreadersessionerrortagsizetoosmall)
- [static var ndefReaderSessionErrorTagUpdateFailure: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/ndefreadersessionerrortagupdatefailure)
- [static var ndefReaderSessionErrorZeroLengthMessage: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/ndefreadersessionerrorzerolengthmessage)

### Transceive Errors

- [static var readerTransceiveErrorRetryExceeded: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readertransceiveerrorretryexceeded)
- [static var readerTransceiveErrorTagConnectionLost: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readertransceiveerrortagconnectionlost)
- [static var readerTransceiveErrorTagNotConnected: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readertransceiveerrortagnotconnected)
- [static var readerTransceiveErrorTagResponseError: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readertransceiveerrortagresponseerror)
- [static var readerTransceiveErrorSessionInvalidated: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readertransceiveerrorsessioninvalidated)
- [static var readerTransceiveErrorPacketTooLong: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readertransceiveerrorpackettoolong)

### Tag Command Configuration Error

- [static var tagCommandConfigurationErrorInvalidParameters: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/tagcommandconfigurationerrorinvalidparameters)

### Other Errors

- [static var readerErrorUnsupportedFeature: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererrorunsupportedfeature)
- [static var readerErrorInvalidParameter: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererrorinvalidparameter)
- [static var readerErrorInvalidParameterLength: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererrorinvalidparameterlength)
- [static var readerErrorParameterOutOfBound: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererrorparameteroutofbound)
- [static var readerErrorRadioDisabled: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererrorradiodisabled)
- [static var readerErrorSecurityViolation: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererrorsecurityviolation)

### Error Domain

- [let NFCErrorDomain: String](/documentation/corenfc/nfcerrordomain)

### Type Properties

- [static var errorDomain: String](/documentation/corenfc/nfcreadererror-swift.struct/errordomain)
- [static var readerErrorAccessNotAccepted: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererroraccessnotaccepted)
- [static var readerErrorIneligible: NFCReaderError.Code](/documentation/corenfc/nfcreadererror-swift.struct/readererrorineligible)
- [let NFCErrorDomain: String](/documentation/corenfc/nfcerrordomain)
- [let NFCTagResponseUnexpectedLengthErrorKey: String](/documentation/corenfc/nfctagresponseunexpectedlengtherrorkey)

## Reference

- [CoreNFC Enumerations](/documentation/corenfc/corenfc-enumerations)

### Enumerations

- [NFCFeliCaEncryptionId](/documentation/corenfc/nfcfelicaencryptionid)

#### Enumeration Cases

- [case AES](/documentation/corenfc/nfcfelicaencryptionid/aes-swift.enum.case)
- [case AES_DES](/documentation/corenfc/nfcfelicaencryptionid/aes_des-swift.enum.case)

#### Initializers

- [init?(rawValue: Int)](/documentation/corenfc/nfcfelicaencryptionid/init(rawvalue:))

#### Type Properties

- [static var aes: NFCFeliCaEncryptionId](/documentation/corenfc/nfcfelicaencryptionid/aes-swift.type.property)
- [static var aes_des: NFCFeliCaEncryptionId](/documentation/corenfc/nfcfelicaencryptionid/aes_des-swift.type.property)
- [NFCFeliCaPollingRequestCode](/documentation/corenfc/nfcfelicapollingrequestcode)

#### Enumeration Cases

- [case communicationPerformance](/documentation/corenfc/nfcfelicapollingrequestcode/communicationperformance)
- [case noRequest](/documentation/corenfc/nfcfelicapollingrequestcode/norequest)
- [case systemCode](/documentation/corenfc/nfcfelicapollingrequestcode/systemcode)

#### Initializers

- [init?(rawValue: Int)](/documentation/corenfc/nfcfelicapollingrequestcode/init(rawvalue:))

#### Type Properties

- [static var PollingRequestCodeCommunicationPerformance: NFCFeliCaPollingRequestCode](/documentation/corenfc/nfcfelicapollingrequestcode/pollingrequestcodecommunicationperformance)
- [static var PollingRequestCodeNoRequest: NFCFeliCaPollingRequestCode](/documentation/corenfc/nfcfelicapollingrequestcode/pollingrequestcodenorequest)
- [static var PollingRequestCodeSystemCode: NFCFeliCaPollingRequestCode](/documentation/corenfc/nfcfelicapollingrequestcode/pollingrequestcodesystemcode)
- [NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot)

#### Enumeration Cases

- [case max1](/documentation/corenfc/nfcfelicapollingtimeslot/max1)
- [case max16](/documentation/corenfc/nfcfelicapollingtimeslot/max16)
- [case max2](/documentation/corenfc/nfcfelicapollingtimeslot/max2)
- [case max4](/documentation/corenfc/nfcfelicapollingtimeslot/max4)
- [case max8](/documentation/corenfc/nfcfelicapollingtimeslot/max8)

#### Initializers

- [init?(rawValue: Int)](/documentation/corenfc/nfcfelicapollingtimeslot/init(rawvalue:))

#### Type Properties

- [static var PollingTimeSlotMax1: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax1)
- [static var PollingTimeSlotMax16: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax16)
- [static var PollingTimeSlotMax2: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax2)
- [static var PollingTimeSlotMax4: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax4)
- [static var PollingTimeSlotMax8: NFCFeliCaPollingTimeSlot](/documentation/corenfc/nfcfelicapollingtimeslot/pollingtimeslotmax8)
- [NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag)

#### Initializers

- [init(rawValue: UInt8)](/documentation/corenfc/nfciso15693requestflag/init(rawvalue:))

#### Type Properties

- [static var RequestFlagAddress: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagaddress)
- [static var RequestFlagDualSubCarriers: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagdualsubcarriers)
- [static var RequestFlagHighDataRate: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflaghighdatarate)
- [static var RequestFlagOption: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagoption)
- [static var RequestFlagProtocolExtension: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagprotocolextension)
- [static var RequestFlagSelect: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/requestflagselect)
- [static var address: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/address)
- [static var commandSpecificBit8: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/commandspecificbit8)
- [static var dualSubCarriers: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/dualsubcarriers)
- [static var highDataRate: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/highdatarate)
- [static var option: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/option)
- [static var protocolExtension: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/protocolextension)
- [static var select: NFCISO15693RequestFlag](/documentation/corenfc/nfciso15693requestflag/select)
- [NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag)

#### Initializers

- [init(rawValue: UInt8)](/documentation/corenfc/nfciso15693responseflag/init(rawvalue:))

#### Type Properties

- [static var blockSecurityStatusBit5: NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag/blocksecuritystatusbit5)
- [static var blockSecurityStatusBit6: NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag/blocksecuritystatusbit6)
- [static var error: NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag/error)
- [static var finalResponse: NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag/finalresponse)
- [static var protocolExtension: NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag/protocolextension)
- [static var responseBufferValid: NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag/responsebuffervalid)
- [static var waitTimeExtension: NFCISO15693ResponseFlag](/documentation/corenfc/nfciso15693responseflag/waittimeextension)
- [NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode)

#### Enumeration Cases

- [case dataNotActivated](/documentation/corenfc/nfcvasresponse/errorcode/datanotactivated)
- [case dataNotFound](/documentation/corenfc/nfcvasresponse/errorcode/datanotfound)
- [case incorrectData](/documentation/corenfc/nfcvasresponse/errorcode/incorrectdata)
- [case success](/documentation/corenfc/nfcvasresponse/errorcode/success)
- [case unsupportedApplicationVersion](/documentation/corenfc/nfcvasresponse/errorcode/unsupportedapplicationversion)
- [case userIntervention](/documentation/corenfc/nfcvasresponse/errorcode/userintervention)
- [case wrongLCField](/documentation/corenfc/nfcvasresponse/errorcode/wronglcfield)
- [case wrongParameters](/documentation/corenfc/nfcvasresponse/errorcode/wrongparameters)

#### Initializers

- [init?(rawValue: Int)](/documentation/corenfc/nfcvasresponse/errorcode/init(rawvalue:))

#### Type Properties

- [static var VASErrorCodeDataNotActivated: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodedatanotactivated)
- [static var VASErrorCodeDataNotFound: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodedatanotfound)
- [static var VASErrorCodeIncorrectData: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodeincorrectdata)
- [static var VASErrorCodeSuccess: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodesuccess)
- [static var VASErrorCodeUnsupportedApplicationVersion: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodeunsupportedapplicationversion)
- [static var VASErrorCodeUserIntervention: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodeuserintervention)
- [static var VASErrorCodeWrongLCField: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodewronglcfield)
- [static var VASErrorCodeWrongParameters: NFCVASResponse.ErrorCode](/documentation/corenfc/nfcvasresponse/errorcode/vaserrorcodewrongparameters)
- [NFCVASCommandConfiguration.Mode](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.enum)

#### Enumeration Cases

- [case normal](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.enum/normal)
- [case urlOnly](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.enum/urlonly)

#### Initializers

- [init?(rawValue: Int)](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.enum/init(rawvalue:))

#### Type Properties

- [static var VASModeNormal: NFCVASCommandConfiguration.Mode](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.enum/vasmodenormal)
- [static var VASModeURLOnly: NFCVASCommandConfiguration.Mode](/documentation/corenfc/nfcvascommandconfiguration/mode-swift.enum/vasmodeurlonly)

## Classes

- [NFCISO15693CustomCommandConfiguration](/documentation/corenfc/nfciso15693customcommandconfiguration)

### Initializers

- [init(manufacturerCode: Int, customCommandCode: Int, requestParameters: Data?)](/documentation/corenfc/nfciso15693customcommandconfiguration/init(manufacturercode:customcommandcode:requestparameters:))
- [init(manufacturerCode: Int, customCommandCode: Int, requestParameters: Data?, maximumRetries: Int, retryInterval: TimeInterval)](/documentation/corenfc/nfciso15693customcommandconfiguration/init(manufacturercode:customcommandcode:requestparameters:maximumretries:retryinterval:))

### Instance Properties

- [var customCommandCode: Int](/documentation/corenfc/nfciso15693customcommandconfiguration/customcommandcode)
- [var manufacturerCode: Int](/documentation/corenfc/nfciso15693customcommandconfiguration/manufacturercode)
- [var requestParameters: Data](/documentation/corenfc/nfciso15693customcommandconfiguration/requestparameters)
- [NFCISO15693ReadMultipleBlocksConfiguration](/documentation/corenfc/nfciso15693readmultipleblocksconfiguration)

### Initializers

- [init(range: NSRange, chunkSize: Int)](/documentation/corenfc/nfciso15693readmultipleblocksconfiguration/init(range:chunksize:))
- [init(range: NSRange, chunkSize: Int, maximumRetries: Int, retryInterval: TimeInterval)](/documentation/corenfc/nfciso15693readmultipleblocksconfiguration/init(range:chunksize:maximumretries:retryinterval:))

### Instance Properties

- [var chunkSize: Int](/documentation/corenfc/nfciso15693readmultipleblocksconfiguration/chunksize)
- [var range: NSRange](/documentation/corenfc/nfciso15693readmultipleblocksconfiguration/range)

## Structures

- [NFCFeliCaPollingResponse](/documentation/corenfc/nfcfelicapollingresponse)

### Instance Properties

- [var manufactureParameter: Data](/documentation/corenfc/nfcfelicapollingresponse/manufactureparameter)
- [var requestData: Data?](/documentation/corenfc/nfcfelicapollingresponse/requestdata)
- [NFCFeliCaRequestSpecificationVersionResponse](/documentation/corenfc/nfcfelicarequestspecificationversionresponse)

### Instance Properties

- [var basicVersion: Data?](/documentation/corenfc/nfcfelicarequestspecificationversionresponse/basicversion)
- [var optionVersion: Data?](/documentation/corenfc/nfcfelicarequestspecificationversionresponse/optionversion)
- [var statusFlag1: Int](/documentation/corenfc/nfcfelicarequestspecificationversionresponse/statusflag1)
- [var statusFlag2: Int](/documentation/corenfc/nfcfelicarequestspecificationversionresponse/statusflag2)
- [NFCFeliCaRequsetServiceV2Response](/documentation/corenfc/nfcfelicarequsetservicev2response)

### Instance Properties

- [var encryptionIdentifier: NFCFeliCaEncryptionId](/documentation/corenfc/nfcfelicarequsetservicev2response/encryptionidentifier)
- [var nodeKeyVersionListAES: [Data]?](/documentation/corenfc/nfcfelicarequsetservicev2response/nodekeyversionlistaes)
- [var nodeKeyVersionListDES: [Data]?](/documentation/corenfc/nfcfelicarequsetservicev2response/nodekeyversionlistdes)
- [var statusFlag1: Int](/documentation/corenfc/nfcfelicarequsetservicev2response/statusflag1)
- [var statusFlag2: Int](/documentation/corenfc/nfcfelicarequsetservicev2response/statusflag2)
- [NFCFeliCaStatusFlag](/documentation/corenfc/nfcfelicastatusflag)

### Instance Properties

- [var statusFlag1: Int](/documentation/corenfc/nfcfelicastatusflag/statusflag1)
- [var statusFlag2: Int](/documentation/corenfc/nfcfelicastatusflag/statusflag2)
- [NFCISO15693MultipleBlockSecurityStatus](/documentation/corenfc/nfciso15693multipleblocksecuritystatus)

### Instance Properties

- [var blockSecurityStatus: [Int]](/documentation/corenfc/nfciso15693multipleblocksecuritystatus/blocksecuritystatus)
- [NFCISO15693SystemInfo](/documentation/corenfc/nfciso15693systeminfo)

### Instance Properties

- [var applicationFamilyIdentifier: Int](/documentation/corenfc/nfciso15693systeminfo/applicationfamilyidentifier)
- [var blockSize: Int](/documentation/corenfc/nfciso15693systeminfo/blocksize)
- [var dataStorageFormatIdentifier: Int](/documentation/corenfc/nfciso15693systeminfo/datastorageformatidentifier)
- [var icReference: Int](/documentation/corenfc/nfciso15693systeminfo/icreference)
- [var totalBlocks: Int](/documentation/corenfc/nfciso15693systeminfo/totalblocks)
- [var uniqueIdentifier: Data](/documentation/corenfc/nfciso15693systeminfo/uniqueidentifier)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
