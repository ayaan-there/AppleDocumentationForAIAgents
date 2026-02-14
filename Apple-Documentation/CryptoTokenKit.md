# CryptoTokenKit Documentation

Source: https://sosumi.ai/documentation/cryptotokenkit

---
title: CryptoTokenKit
source: https://developer.apple.com/documentation/cryptotokenkit
timestamp: 2026-02-13T18:56:01.144Z
---

## Smart Cards

- [Using Cryptographic Assets Stored on a Smart Card](/documentation/cryptotokenkit/using-cryptographic-assets-stored-on-a-smart-card)
- [TKSmartCardSlotManager](/documentation/cryptotokenkit/tksmartcardslotmanager)

### Creating a Card Slot Manager

- [class var `default`: TKSmartCardSlotManager?](/documentation/cryptotokenkit/tksmartcardslotmanager/default)

### Accessing Smart Card Slots

- [var slotNames: [String]](/documentation/cryptotokenkit/tksmartcardslotmanager/slotnames)
- [func getSlot(withName: String, reply: (TKSmartCardSlot?) -> Void)](/documentation/cryptotokenkit/tksmartcardslotmanager/getslot(withname:reply:))
- [func slotNamed(String) -> TKSmartCardSlot?](/documentation/cryptotokenkit/tksmartcardslotmanager/slotnamed(_:))

### Instance Methods

- [func createNFCSlot(message: String?, completion: (TKSmartCardSlotNFCSession?, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcardslotmanager/createnfcslot(message:completion:))
- [func isNFCSupported() -> Bool](/documentation/cryptotokenkit/tksmartcardslotmanager/isnfcsupported())
- [TKSmartCardSlot](/documentation/cryptotokenkit/tksmartcardslot)

### Instantiating Smart Cards

- [func makeSmartCard() -> TKSmartCard?](/documentation/cryptotokenkit/tksmartcardslot/makesmartcard())

### Getting the Slot State

- [var state: TKSmartCardSlot.State](/documentation/cryptotokenkit/tksmartcardslot/state-swift.property)
- [TKSmartCardSlot.State](/documentation/cryptotokenkit/tksmartcardslot/state-swift.enum)

#### Constants

- [case missing](/documentation/cryptotokenkit/tksmartcardslot/state-swift.enum/missing)
- [case empty](/documentation/cryptotokenkit/tksmartcardslot/state-swift.enum/empty)
- [case probing](/documentation/cryptotokenkit/tksmartcardslot/state-swift.enum/probing)
- [case muteCard](/documentation/cryptotokenkit/tksmartcardslot/state-swift.enum/mutecard)
- [case validCard](/documentation/cryptotokenkit/tksmartcardslot/state-swift.enum/validcard)

#### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tksmartcardslot/state-swift.enum/init(rawvalue:))

### Getting the Slot Configuration

- [var name: String](/documentation/cryptotokenkit/tksmartcardslot/name)
- [var maxInputLength: Int](/documentation/cryptotokenkit/tksmartcardslot/maxinputlength)
- [var maxOutputLength: Int](/documentation/cryptotokenkit/tksmartcardslot/maxoutputlength)

### Reading the Answer to Reset

- [var atr: TKSmartCardATR?](/documentation/cryptotokenkit/tksmartcardslot/atr)
- [TKSmartCardATR](/documentation/cryptotokenkit/tksmartcardatr)

#### Creating a Smart Card ATR

- [init?(bytes: Data)](/documentation/cryptotokenkit/tksmartcardatr/init(bytes:))
- [init?(source: () -> Int32)](/documentation/cryptotokenkit/tksmartcardatr/init(source:))

#### Accessing ATR Attributes

- [var protocols: [NSNumber]](/documentation/cryptotokenkit/tksmartcardatr/protocols)
- [var bytes: Data](/documentation/cryptotokenkit/tksmartcardatr/bytes)
- [var historicalBytes: Data](/documentation/cryptotokenkit/tksmartcardatr/historicalbytes)
- [var historicalRecords: [TKCompactTLVRecord]?](/documentation/cryptotokenkit/tksmartcardatr/historicalrecords)

#### Retrieving Interface Groups

- [func interfaceGroup(at: Int) -> TKSmartCardATR.InterfaceGroup?](/documentation/cryptotokenkit/tksmartcardatr/interfacegroup(at:))
- [func interfaceGroup(for: TKSmartCardProtocol) -> TKSmartCardATR.InterfaceGroup?](/documentation/cryptotokenkit/tksmartcardatr/interfacegroup(for:))
- [TKSmartCardATR.InterfaceGroup](/documentation/cryptotokenkit/tksmartcardatr/interfacegroup)

##### Accessing Interface Group Protocol and Bytes

- [var `protocol`: NSNumber?](/documentation/cryptotokenkit/tksmartcardatr/interfacegroup/protocol)
- [var ta: NSNumber?](/documentation/cryptotokenkit/tksmartcardatr/interfacegroup/ta)
- [var tb: NSNumber?](/documentation/cryptotokenkit/tksmartcardatr/interfacegroup/tb)
- [var tc: NSNumber?](/documentation/cryptotokenkit/tksmartcardatr/interfacegroup/tc)
- [TKSmartCard](/documentation/cryptotokenkit/tksmartcard)

### Configuring the Smart Card

- [var slot: TKSmartCardSlot](/documentation/cryptotokenkit/tksmartcard/slot)
- [var isValid: Bool](/documentation/cryptotokenkit/tksmartcard/isvalid)
- [var isSensitive: Bool](/documentation/cryptotokenkit/tksmartcard/issensitive)
- [var context: Any?](/documentation/cryptotokenkit/tksmartcard/context)

### Setting the Communication Protocol

- [var allowedProtocols: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcard/allowedprotocols)
- [var currentProtocol: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcard/currentprotocol)
- [TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol)

#### Constants

- [static var t0: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/t0)
- [static var t1: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/t1)
- [static var t15: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/t15)
- [static var any: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/any)

#### Initializers

- [init(rawValue: UInt)](/documentation/cryptotokenkit/tksmartcardprotocol/init(rawvalue:))

### Communicating with the Smart Card

- [func beginSession(reply: (Bool, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcard/beginsession(reply:))
- [func transmit(Data, reply: (Data?, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcard/transmit(_:reply:))
- [func endSession()](/documentation/cryptotokenkit/tksmartcard/endsession())

### Managing User Interaction

- [func userInteractionForSecurePINVerification(TKSmartCardPINFormat, apdu: Data, pinByteOffset: Int) -> TKSmartCardUserInteractionForSecurePINVerification?](/documentation/cryptotokenkit/tksmartcard/userinteractionforsecurepinverification(_:apdu:pinbyteoffset:))
- [func userInteractionForSecurePINChange(TKSmartCardPINFormat, apdu: Data, currentPINByteOffset: Int, newPINByteOffset: Int) -> TKSmartCardUserInteractionForSecurePINChange?](/documentation/cryptotokenkit/tksmartcard/userinteractionforsecurepinchange(_:apdu:currentpinbyteoffset:newpinbyteoffset:))
- [TKSmartCardPINFormat](/documentation/cryptotokenkit/tksmartcardpinformat)

#### Configuring PIN Formatting

- [var charset: TKSmartCardPINFormat.Charset](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.property)
- [var encoding: TKSmartCardPINFormat.Encoding](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.property)
- [var minPINLength: Int](/documentation/cryptotokenkit/tksmartcardpinformat/minpinlength)
- [var maxPINLength: Int](/documentation/cryptotokenkit/tksmartcardpinformat/maxpinlength)
- [var pinBlockByteLength: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinblockbytelength)
- [var pinJustification: TKSmartCardPINFormat.Justification](/documentation/cryptotokenkit/tksmartcardpinformat/pinjustification)
- [var pinBitOffset: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinbitoffset)
- [var pinLengthBitOffset: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinlengthbitoffset)
- [var pinLengthBitSize: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinlengthbitsize)

#### PIN Characteristics

- [TKSmartCardPINFormat.Charset](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum)

##### Constants

- [case numeric](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/numeric)
- [case alphanumeric](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/alphanumeric)
- [case upperAlphanumeric](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/upperalphanumeric)

##### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/init(rawvalue:))
- [TKSmartCardPINFormat.Encoding](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum)

##### Constants

- [case binary](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/binary)
- [case ascii](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/ascii)
- [case bcd](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/bcd)

##### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/init(rawvalue:))
- [TKSmartCardPINFormat.Justification](/documentation/cryptotokenkit/tksmartcardpinformat/justification)

##### Constants

- [case left](/documentation/cryptotokenkit/tksmartcardpinformat/justification/left)
- [case right](/documentation/cryptotokenkit/tksmartcardpinformat/justification/right)

##### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tksmartcardpinformat/justification/init(rawvalue:))
- [TKSmartCardUserInteraction](/documentation/cryptotokenkit/tksmartcarduserinteraction)

#### Handling User Interaction Events

- [var delegate: (any TKSmartCardUserInteractionDelegate)?](/documentation/cryptotokenkit/tksmartcarduserinteraction/delegate)
- [TKSmartCardUserInteractionDelegate](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate)

##### Delegate Methods

- [func characterEntered(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/characterentered(in:))
- [func correctionKeyPressed(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/correctionkeypressed(in:))
- [func validationKeyPressed(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/validationkeypressed(in:))
- [func invalidCharacterEntered(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/invalidcharacterentered(in:))
- [func oldPINRequested(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/oldpinrequested(in:))
- [func newPINRequested(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/newpinrequested(in:))
- [func newPINConfirmationRequested(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/newpinconfirmationrequested(in:))

#### Configuring Timeout

- [var initialTimeout: TimeInterval](/documentation/cryptotokenkit/tksmartcarduserinteraction/initialtimeout)
- [var interactionTimeout: TimeInterval](/documentation/cryptotokenkit/tksmartcarduserinteraction/interactiontimeout)

#### Starting and Stopping

- [func run(reply: (Bool, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcarduserinteraction/run(reply:))
- [func cancel() -> Bool](/documentation/cryptotokenkit/tksmartcarduserinteraction/cancel())
- [TKSmartCardUserInteractionForPINOperation](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation)

#### Managing Pin Completion

- [var pinCompletion: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/pincompletion)
- [TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion)

##### Type Properties

- [static var key: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/key)
- [static var maxLength: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/maxlength)
- [static var timeout: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/timeout)

##### Initializers

- [init(rawValue: UInt)](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/init(rawvalue:))

#### Configuring Messages

- [var pinMessageIndices: [NSNumber]?](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/pinmessageindices)
- [var locale: Locale!](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/locale)

#### Accessing Response Data

- [var resultSW: UInt16](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/resultsw)
- [var resultData: Data?](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/resultdata)
- [TKSmartCardUserInteractionForSecurePINChange](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange)

#### Configuring User Interaction

- [var pinConfirmation: TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/pinconfirmation)
- [TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation)

##### Type Properties

- [static var current: TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation/current)
- [static var new: TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation/new)

##### Initializers

- [init(rawValue: UInt)](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation/init(rawvalue:))
- [TKSmartCardUserInteractionForSecurePINVerification](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinverification)

### Configuring APDU Behavior

- [var cla: UInt8](/documentation/cryptotokenkit/tksmartcard/cla)
- [var useExtendedLength: Bool](/documentation/cryptotokenkit/tksmartcard/useextendedlength)
- [var useCommandChaining: Bool](/documentation/cryptotokenkit/tksmartcard/usecommandchaining)

### Transmitting Data

- [func send(ins: UInt8, p1: UInt8, p2: UInt8, data: Data?, le: Int?, reply: (Data?, UInt16, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcard/send(ins:p1:p2:data:le:reply:))
- [func send(ins: UInt8, p1: UInt8, p2: UInt8, data: Data?, le: Int?) throws -> (sw: UInt16, response: Data)](/documentation/cryptotokenkit/tksmartcard/send(ins:p1:p2:data:le:))
- [func withSession<T>(() throws -> T) throws -> T](/documentation/cryptotokenkit/tksmartcard/withsession(_:))

## Smart Card App Extensions

- [Authenticating Users with a Cryptographic Token](/documentation/cryptotokenkit/authenticating-users-with-a-cryptographic-token)
- [Configuring Smart Card Authentication](/documentation/cryptotokenkit/configuring-smart-card-authentication)
- [TKSmartCardTokenDriver](/documentation/cryptotokenkit/tksmartcardtokendriver)

### Responding to Token Creation

- [TKSmartCardTokenDriverDelegate](/documentation/cryptotokenkit/tksmartcardtokendriverdelegate)

#### Delegate Methods

- [func tokenDriver(TKSmartCardTokenDriver, createTokenFor: TKSmartCard, aid: Data?) throws -> TKSmartCardToken](/documentation/cryptotokenkit/tksmartcardtokendriverdelegate/tokendriver(_:createtokenfor:aid:))
- [TKSmartCardToken](/documentation/cryptotokenkit/tksmartcardtoken)

### Creating Smart Card Tokens

- [init(smartCard: TKSmartCard, aid: Data?, instanceID: String, tokenDriver: TKSmartCardTokenDriver)](/documentation/cryptotokenkit/tksmartcardtoken/init(smartcard:aid:instanceid:tokendriver:))

### Accessing the Application Identifier

- [var aid: Data?](/documentation/cryptotokenkit/tksmartcardtoken/aid)

### Accessing Smart Cards

- [TKSmartCard](/documentation/cryptotokenkit/tksmartcard)

#### Configuring the Smart Card

- [var slot: TKSmartCardSlot](/documentation/cryptotokenkit/tksmartcard/slot)
- [var isValid: Bool](/documentation/cryptotokenkit/tksmartcard/isvalid)
- [var isSensitive: Bool](/documentation/cryptotokenkit/tksmartcard/issensitive)
- [var context: Any?](/documentation/cryptotokenkit/tksmartcard/context)

#### Setting the Communication Protocol

- [var allowedProtocols: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcard/allowedprotocols)
- [var currentProtocol: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcard/currentprotocol)
- [TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol)

##### Constants

- [static var t0: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/t0)
- [static var t1: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/t1)
- [static var t15: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/t15)
- [static var any: TKSmartCardProtocol](/documentation/cryptotokenkit/tksmartcardprotocol/any)

##### Initializers

- [init(rawValue: UInt)](/documentation/cryptotokenkit/tksmartcardprotocol/init(rawvalue:))

#### Communicating with the Smart Card

- [func beginSession(reply: (Bool, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcard/beginsession(reply:))
- [func transmit(Data, reply: (Data?, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcard/transmit(_:reply:))
- [func endSession()](/documentation/cryptotokenkit/tksmartcard/endsession())

#### Managing User Interaction

- [func userInteractionForSecurePINVerification(TKSmartCardPINFormat, apdu: Data, pinByteOffset: Int) -> TKSmartCardUserInteractionForSecurePINVerification?](/documentation/cryptotokenkit/tksmartcard/userinteractionforsecurepinverification(_:apdu:pinbyteoffset:))
- [func userInteractionForSecurePINChange(TKSmartCardPINFormat, apdu: Data, currentPINByteOffset: Int, newPINByteOffset: Int) -> TKSmartCardUserInteractionForSecurePINChange?](/documentation/cryptotokenkit/tksmartcard/userinteractionforsecurepinchange(_:apdu:currentpinbyteoffset:newpinbyteoffset:))
- [TKSmartCardPINFormat](/documentation/cryptotokenkit/tksmartcardpinformat)

##### Configuring PIN Formatting

- [var charset: TKSmartCardPINFormat.Charset](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.property)
- [var encoding: TKSmartCardPINFormat.Encoding](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.property)
- [var minPINLength: Int](/documentation/cryptotokenkit/tksmartcardpinformat/minpinlength)
- [var maxPINLength: Int](/documentation/cryptotokenkit/tksmartcardpinformat/maxpinlength)
- [var pinBlockByteLength: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinblockbytelength)
- [var pinJustification: TKSmartCardPINFormat.Justification](/documentation/cryptotokenkit/tksmartcardpinformat/pinjustification)
- [var pinBitOffset: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinbitoffset)
- [var pinLengthBitOffset: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinlengthbitoffset)
- [var pinLengthBitSize: Int](/documentation/cryptotokenkit/tksmartcardpinformat/pinlengthbitsize)

##### PIN Characteristics

- [TKSmartCardPINFormat.Charset](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum)

###### Constants

- [case numeric](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/numeric)
- [case alphanumeric](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/alphanumeric)
- [case upperAlphanumeric](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/upperalphanumeric)

###### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tksmartcardpinformat/charset-swift.enum/init(rawvalue:))
- [TKSmartCardPINFormat.Encoding](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum)

###### Constants

- [case binary](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/binary)
- [case ascii](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/ascii)
- [case bcd](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/bcd)

###### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tksmartcardpinformat/encoding-swift.enum/init(rawvalue:))
- [TKSmartCardPINFormat.Justification](/documentation/cryptotokenkit/tksmartcardpinformat/justification)

###### Constants

- [case left](/documentation/cryptotokenkit/tksmartcardpinformat/justification/left)
- [case right](/documentation/cryptotokenkit/tksmartcardpinformat/justification/right)

###### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tksmartcardpinformat/justification/init(rawvalue:))
- [TKSmartCardUserInteraction](/documentation/cryptotokenkit/tksmartcarduserinteraction)

##### Handling User Interaction Events

- [var delegate: (any TKSmartCardUserInteractionDelegate)?](/documentation/cryptotokenkit/tksmartcarduserinteraction/delegate)
- [TKSmartCardUserInteractionDelegate](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate)

###### Delegate Methods

- [func characterEntered(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/characterentered(in:))
- [func correctionKeyPressed(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/correctionkeypressed(in:))
- [func validationKeyPressed(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/validationkeypressed(in:))
- [func invalidCharacterEntered(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/invalidcharacterentered(in:))
- [func oldPINRequested(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/oldpinrequested(in:))
- [func newPINRequested(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/newpinrequested(in:))
- [func newPINConfirmationRequested(in: TKSmartCardUserInteraction)](/documentation/cryptotokenkit/tksmartcarduserinteractiondelegate/newpinconfirmationrequested(in:))

##### Configuring Timeout

- [var initialTimeout: TimeInterval](/documentation/cryptotokenkit/tksmartcarduserinteraction/initialtimeout)
- [var interactionTimeout: TimeInterval](/documentation/cryptotokenkit/tksmartcarduserinteraction/interactiontimeout)

##### Starting and Stopping

- [func run(reply: (Bool, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcarduserinteraction/run(reply:))
- [func cancel() -> Bool](/documentation/cryptotokenkit/tksmartcarduserinteraction/cancel())
- [TKSmartCardUserInteractionForPINOperation](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation)

##### Managing Pin Completion

- [var pinCompletion: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/pincompletion)
- [TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion)

###### Type Properties

- [static var key: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/key)
- [static var maxLength: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/maxlength)
- [static var timeout: TKSmartCardUserInteractionForPINOperation.Completion](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/timeout)

###### Initializers

- [init(rawValue: UInt)](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/completion/init(rawvalue:))

##### Configuring Messages

- [var pinMessageIndices: [NSNumber]?](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/pinmessageindices)
- [var locale: Locale!](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/locale)

##### Accessing Response Data

- [var resultSW: UInt16](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/resultsw)
- [var resultData: Data?](/documentation/cryptotokenkit/tksmartcarduserinteractionforpinoperation/resultdata)
- [TKSmartCardUserInteractionForSecurePINChange](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange)

##### Configuring User Interaction

- [var pinConfirmation: TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/pinconfirmation)
- [TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation)

###### Type Properties

- [static var current: TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation/current)
- [static var new: TKSmartCardUserInteractionForSecurePINChange.Confirmation](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation/new)

###### Initializers

- [init(rawValue: UInt)](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinchange/confirmation/init(rawvalue:))
- [TKSmartCardUserInteractionForSecurePINVerification](/documentation/cryptotokenkit/tksmartcarduserinteractionforsecurepinverification)

#### Configuring APDU Behavior

- [var cla: UInt8](/documentation/cryptotokenkit/tksmartcard/cla)
- [var useExtendedLength: Bool](/documentation/cryptotokenkit/tksmartcard/useextendedlength)
- [var useCommandChaining: Bool](/documentation/cryptotokenkit/tksmartcard/usecommandchaining)

#### Transmitting Data

- [func send(ins: UInt8, p1: UInt8, p2: UInt8, data: Data?, le: Int?, reply: (Data?, UInt16, (any Error)?) -> Void)](/documentation/cryptotokenkit/tksmartcard/send(ins:p1:p2:data:le:reply:))
- [func send(ins: UInt8, p1: UInt8, p2: UInt8, data: Data?, le: Int?) throws -> (sw: UInt16, response: Data)](/documentation/cryptotokenkit/tksmartcard/send(ins:p1:p2:data:le:))
- [func withSession<T>(() throws -> T) throws -> T](/documentation/cryptotokenkit/tksmartcard/withsession(_:))

### Working with Tag-Length-Value Records

- [TKTLVRecord](/documentation/cryptotokenkit/tktlvrecord)

#### Creating Records

- [class func sequenceOfRecords(from: Data) -> [TKTLVRecord]?](/documentation/cryptotokenkit/tktlvrecord/sequenceofrecords(from:))
- [convenience init?(from: Data)](/documentation/cryptotokenkit/tktlvrecord/init(from:))

#### Accessing the Tag Field

- [var tag: TKTLVTag](/documentation/cryptotokenkit/tktlvrecord/tag)
- [TKTLVTag](/documentation/cryptotokenkit/tktlvtag)

#### Accessing the Value Field

- [var value: Data](/documentation/cryptotokenkit/tktlvrecord/value)

#### Accessing Record Data

- [var data: Data](/documentation/cryptotokenkit/tktlvrecord/data)
- [TKBERTLVRecord](/documentation/cryptotokenkit/tkbertlvrecord)

#### Creating TLV Records

- [init(tag: TKTLVTag, value: Data)](/documentation/cryptotokenkit/tkbertlvrecord/init(tag:value:))
- [init(tag: TKTLVTag, records: [TKTLVRecord])](/documentation/cryptotokenkit/tkbertlvrecord/init(tag:records:))
- [TKTLVTag](/documentation/cryptotokenkit/tktlvtag)

#### Encoding Data

- [class func data(forTag: TKTLVTag) -> Data](/documentation/cryptotokenkit/tkbertlvrecord/data(fortag:))
- [TKCompactTLVRecord](/documentation/cryptotokenkit/tkcompacttlvrecord)

#### Creating TLV Records

- [init(tag: UInt8, value: Data)](/documentation/cryptotokenkit/tkcompacttlvrecord/init(tag:value:))
- [TKSimpleTLVRecord](/documentation/cryptotokenkit/tksimpletlvrecord)

#### Creating TLV Records

- [init(tag: UInt8, value: Data)](/documentation/cryptotokenkit/tksimpletlvrecord/init(tag:value:))
- [TKSmartCardTokenSession](/documentation/cryptotokenkit/tksmartcardtokensession)

### Accessing the Smart Card

- [var smartCard: TKSmartCard](/documentation/cryptotokenkit/tksmartcardtokensession/smartcard)

### Instance Methods

- [func getSmartCard() throws -> TKSmartCard](/documentation/cryptotokenkit/tksmartcardtokensession/getsmartcard())

## Tokens

- [TKTokenWatcher](/documentation/cryptotokenkit/tktokenwatcher)

### Creating Token Watchers

- [init()](/documentation/cryptotokenkit/tktokenwatcher/init())
- [init(insertionHandler: (String) -> Void)](/documentation/cryptotokenkit/tktokenwatcher/init(insertionhandler:))

### Accessing Token Identifiers

- [var tokenIDs: [String]](/documentation/cryptotokenkit/tktokenwatcher/tokenids)

### Configuring Handlers

- [func addRemovalHandler((String) -> Void, forTokenID: String)](/documentation/cryptotokenkit/tktokenwatcher/addremovalhandler(_:fortokenid:))
- [func setInsertionHandler((String) -> Void)](/documentation/cryptotokenkit/tktokenwatcher/setinsertionhandler(_:))

### Classes

- [TKTokenWatcher.TokenInfo](/documentation/cryptotokenkit/tktokenwatcher/tokeninfo)

#### Instance Properties

- [var driverName: String?](/documentation/cryptotokenkit/tktokenwatcher/tokeninfo/drivername)
- [var slotName: String?](/documentation/cryptotokenkit/tktokenwatcher/tokeninfo/slotname)
- [var tokenID: String](/documentation/cryptotokenkit/tktokenwatcher/tokeninfo/tokenid)

### Instance Methods

- [func tokenInfo(forTokenID: String) -> TKTokenWatcher.TokenInfo?](/documentation/cryptotokenkit/tktokenwatcher/tokeninfo(fortokenid:))
- [TKTokenDriver](/documentation/cryptotokenkit/tktokendriver)

### Responding to Token Creation

- [var delegate: (any TKTokenDriverDelegate)?](/documentation/cryptotokenkit/tktokendriver/delegate)
- [TKTokenDriverDelegate](/documentation/cryptotokenkit/tktokendriverdelegate)

#### Creating and Removing Tokens

- [func tokenDriver(TKTokenDriver, terminateToken: TKToken)](/documentation/cryptotokenkit/tktokendriverdelegate/tokendriver(_:terminatetoken:))
- [func tokenDriver(TKTokenDriver, tokenFor: TKToken.Configuration) throws -> TKToken](/documentation/cryptotokenkit/tktokendriverdelegate/tokendriver(_:tokenfor:))
- [TKTokenDriver.ClassID](/documentation/cryptotokenkit/tktokendriver/classid)
- [TKTokenDriver.Configuration](/documentation/cryptotokenkit/tktokendriver/configuration)

#### Reporting Configuration Information

- [var classID: TKTokenDriver.ClassID](/documentation/cryptotokenkit/tktokendriver/configuration/classid)
- [var tokenConfigurations: [TKToken.InstanceID : TKToken.Configuration]](/documentation/cryptotokenkit/tktokendriver/configuration/tokenconfigurations)
- [class var driverConfigurations: [TKTokenDriver.ClassID : TKTokenDriver.Configuration]](/documentation/cryptotokenkit/tktokendriver/configuration/driverconfigurations)

#### Adding and Removing Configurations

- [func addTokenConfiguration(for: TKToken.InstanceID) -> TKToken.Configuration](/documentation/cryptotokenkit/tktokendriver/configuration/addtokenconfiguration(for:))
- [func removeTokenConfiguration(for: TKToken.InstanceID)](/documentation/cryptotokenkit/tktokendriver/configuration/removetokenconfiguration(for:))
- [TKToken](/documentation/cryptotokenkit/tktoken)

### Creating Tokens

- [init(tokenDriver: TKTokenDriver, instanceID: TKToken.InstanceID)](/documentation/cryptotokenkit/tktoken/init(tokendriver:instanceid:))
- [TKToken.InstanceID](/documentation/cryptotokenkit/tktoken/instanceid)

### Responding to Session Creation

- [var delegate: (any TKTokenDelegate)?](/documentation/cryptotokenkit/tktoken/delegate)
- [TKTokenDelegate](/documentation/cryptotokenkit/tktokendelegate)

#### Delegate Methods

- [func createSession(TKToken) throws -> TKTokenSession](/documentation/cryptotokenkit/tktokendelegate/createsession(_:))
- [func token(TKToken, terminateSession: TKTokenSession)](/documentation/cryptotokenkit/tktokendelegate/token(_:terminatesession:))

### Accessing the Driver

- [var tokenDriver: TKTokenDriver](/documentation/cryptotokenkit/tktoken/tokendriver)

### Accessing Keychain Items

- [var keychainContents: TKTokenKeychainContents?](/documentation/cryptotokenkit/tktoken/keychaincontents)
- [TKTokenKeychainContents](/documentation/cryptotokenkit/tktokenkeychaincontents)

#### Adding Keychain Items

- [func fill(with: [TKTokenKeychainItem])](/documentation/cryptotokenkit/tktokenkeychaincontents/fill(with:))

#### Accessing Keychain Items

- [var items: [TKTokenKeychainItem]](/documentation/cryptotokenkit/tktokenkeychaincontents/items)
- [func key(forObjectID: TKToken.ObjectID) throws -> TKTokenKeychainKey](/documentation/cryptotokenkit/tktokenkeychaincontents/key(forobjectid:))
- [func certificate(forObjectID: TKToken.ObjectID) throws -> TKTokenKeychainCertificate](/documentation/cryptotokenkit/tktokenkeychaincontents/certificate(forobjectid:))
- [TKTokenKeychainItem](/documentation/cryptotokenkit/tktokenkeychainitem)

#### Creating Token Keychain Items

- [init(objectID: TKToken.ObjectID)](/documentation/cryptotokenkit/tktokenkeychainitem/init(objectid:))

#### Accessing Keychain Item Attributes

- [var objectID: TKToken.ObjectID](/documentation/cryptotokenkit/tktokenkeychainitem/objectid)
- [var label: String?](/documentation/cryptotokenkit/tktokenkeychainitem/label)
- [var constraints: [NSNumber : Any]?](/documentation/cryptotokenkit/tktokenkeychainitem/constraints)
- [TKTokenKeychainCertificate](/documentation/cryptotokenkit/tktokenkeychaincertificate)

#### Creating Token Keychain Certificates

- [init?(certificate: SecCertificate, objectID: TKToken.ObjectID)](/documentation/cryptotokenkit/tktokenkeychaincertificate/init(certificate:objectid:))

#### Accessing Certificate Data

- [var data: Data](/documentation/cryptotokenkit/tktokenkeychaincertificate/data)
- [TKTokenKeychainKey](/documentation/cryptotokenkit/tktokenkeychainkey)

#### Creating Token Keychain Keys

- [init?(certificate: SecCertificate?, objectID: TKToken.ObjectID)](/documentation/cryptotokenkit/tktokenkeychainkey/init(certificate:objectid:))

#### Accessing Key Attributes

- [var keyType: String](/documentation/cryptotokenkit/tktokenkeychainkey/keytype)
- [var keySizeInBits: Int](/documentation/cryptotokenkit/tktokenkeychainkey/keysizeinbits)
- [var applicationTag: Data?](/documentation/cryptotokenkit/tktokenkeychainkey/applicationtag)
- [var publicKeyData: Data?](/documentation/cryptotokenkit/tktokenkeychainkey/publickeydata)
- [var publicKeyHash: Data?](/documentation/cryptotokenkit/tktokenkeychainkey/publickeyhash)
- [var canDecrypt: Bool](/documentation/cryptotokenkit/tktokenkeychainkey/candecrypt)
- [var canSign: Bool](/documentation/cryptotokenkit/tktokenkeychainkey/cansign)
- [var canPerformKeyExchange: Bool](/documentation/cryptotokenkit/tktokenkeychainkey/canperformkeyexchange)
- [var isSuitableForLogin: Bool](/documentation/cryptotokenkit/tktokenkeychainkey/issuitableforlogin)
- [TKToken.ObjectID](/documentation/cryptotokenkit/tktoken/objectid)
- [TKToken.ObjectID](/documentation/cryptotokenkit/tktoken/objectid)

### Configuring the Token

- [var configuration: TKToken.Configuration](/documentation/cryptotokenkit/tktoken/configuration-swift.property)
- [TKToken.Configuration](/documentation/cryptotokenkit/tktoken/configuration-swift.class)

#### Reporting Configuration Information

- [var instanceID: TKToken.InstanceID](/documentation/cryptotokenkit/tktoken/configuration-swift.class/instanceid)
- [var configurationData: Data?](/documentation/cryptotokenkit/tktoken/configuration-swift.class/configurationdata)

#### Retrieving Keys and Certificates

- [var keychainItems: [TKTokenKeychainItem]](/documentation/cryptotokenkit/tktoken/configuration-swift.class/keychainitems)
- [func certificate(for: TKToken.ObjectID) throws -> TKTokenKeychainCertificate](/documentation/cryptotokenkit/tktoken/configuration-swift.class/certificate(for:))
- [func key(for: TKToken.ObjectID) throws -> TKTokenKeychainKey](/documentation/cryptotokenkit/tktoken/configuration-swift.class/key(for:))
- [TKTokenSession](/documentation/cryptotokenkit/tktokensession)

### Creating Token Sessions

- [init(token: TKToken)](/documentation/cryptotokenkit/tktokensession/init(token:))

### Responding to Authentication Events

- [var delegate: (any TKTokenSessionDelegate)?](/documentation/cryptotokenkit/tktokensession/delegate)
- [TKTokenSessionDelegate](/documentation/cryptotokenkit/tktokensessiondelegate)

#### Determining Support for Operations

- [func tokenSession(TKTokenSession, supports: TKTokenOperation, keyObjectID: TKToken.ObjectID, algorithm: TKTokenKeyAlgorithm) -> Bool](/documentation/cryptotokenkit/tktokensessiondelegate/tokensession(_:supports:keyobjectid:algorithm:))
- [TKTokenOperation](/documentation/cryptotokenkit/tktokenoperation)

##### Constants

- [case none](/documentation/cryptotokenkit/tktokenoperation/none)
- [case readData](/documentation/cryptotokenkit/tktokenoperation/readdata)
- [case signData](/documentation/cryptotokenkit/tktokenoperation/signdata)
- [case decryptData](/documentation/cryptotokenkit/tktokenoperation/decryptdata)
- [case performKeyExchange](/documentation/cryptotokenkit/tktokenoperation/performkeyexchange)

##### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tktokenoperation/init(rawvalue:))
- [TKToken.ObjectID](/documentation/cryptotokenkit/tktoken/objectid)
- [TKTokenKeyAlgorithm](/documentation/cryptotokenkit/tktokenkeyalgorithm)

##### Determining Algorithm Usage

- [func isAlgorithm(SecKeyAlgorithm) -> Bool](/documentation/cryptotokenkit/tktokenkeyalgorithm/isalgorithm(_:))
- [func supportsAlgorithm(SecKeyAlgorithm) -> Bool](/documentation/cryptotokenkit/tktokenkeyalgorithm/supportsalgorithm(_:))

#### Authenticating

- [func tokenSession(TKTokenSession, beginAuthFor: TKTokenOperation, constraint: Any) throws -> TKTokenAuthOperation](/documentation/cryptotokenkit/tktokensessiondelegate/tokensession(_:beginauthfor:constraint:))
- [TKTokenOperationConstraint](/documentation/cryptotokenkit/tktokenoperationconstraint)
- [TKTokenAuthOperation](/documentation/cryptotokenkit/tktokenauthoperation)

##### Finishing the Operation

- [func finish() throws](/documentation/cryptotokenkit/tktokenauthoperation/finish())
- [TKTokenPasswordAuthOperation](/documentation/cryptotokenkit/tktokenpasswordauthoperation)

##### Managing the Password

- [var password: String?](/documentation/cryptotokenkit/tktokenpasswordauthoperation/password)
- [TKTokenSmartCardPINAuthOperation](/documentation/cryptotokenkit/tktokensmartcardpinauthoperation)

##### Configuring the Operation

- [var pinFormat: TKSmartCardPINFormat](/documentation/cryptotokenkit/tktokensmartcardpinauthoperation/pinformat)
- [var apduTemplate: Data?](/documentation/cryptotokenkit/tktokensmartcardpinauthoperation/apdutemplate)
- [var pinByteOffset: Int](/documentation/cryptotokenkit/tktokensmartcardpinauthoperation/pinbyteoffset)
- [var smartCard: TKSmartCard?](/documentation/cryptotokenkit/tktokensmartcardpinauthoperation/smartcard)

##### Accessing the PIN

- [var pin: String?](/documentation/cryptotokenkit/tktokensmartcardpinauthoperation/pin)

#### Performing Cryptographic Operations

- [func tokenSession(TKTokenSession, sign: Data, keyObjectID: TKToken.ObjectID, algorithm: TKTokenKeyAlgorithm) throws -> Data](/documentation/cryptotokenkit/tktokensessiondelegate/tokensession(_:sign:keyobjectid:algorithm:))
- [func tokenSession(TKTokenSession, decrypt: Data, keyObjectID: TKToken.ObjectID, algorithm: TKTokenKeyAlgorithm) throws -> Data](/documentation/cryptotokenkit/tktokensessiondelegate/tokensession(_:decrypt:keyobjectid:algorithm:))
- [func tokenSession(TKTokenSession, performKeyExchange: Data, keyObjectID: TKToken.ObjectID, algorithm: TKTokenKeyAlgorithm, parameters: TKTokenKeyExchangeParameters) throws -> Data](/documentation/cryptotokenkit/tktokensessiondelegate/tokensession(_:performkeyexchange:keyobjectid:algorithm:parameters:))
- [TKTokenKeyExchangeParameters](/documentation/cryptotokenkit/tktokenkeyexchangeparameters)

##### Accessing Parameters

- [var requestedSize: Int](/documentation/cryptotokenkit/tktokenkeyexchangeparameters/requestedsize)
- [var sharedInfo: Data?](/documentation/cryptotokenkit/tktokenkeyexchangeparameters/sharedinfo)

### Accessing the Token

- [var token: TKToken](/documentation/cryptotokenkit/tktokensession/token)

## Errors

- [TKError](/documentation/cryptotokenkit/tkerror)

### Checking Error Codes

- [static var notImplemented: TKError.Code](/documentation/cryptotokenkit/tkerror/notimplemented)
- [static var communicationError: TKError.Code](/documentation/cryptotokenkit/tkerror/communicationerror)
- [static var corruptedData: TKError.Code](/documentation/cryptotokenkit/tkerror/corrupteddata)
- [static var canceledByUser: TKError.Code](/documentation/cryptotokenkit/tkerror/canceledbyuser)
- [static var authenticationFailed: TKError.Code](/documentation/cryptotokenkit/tkerror/authenticationfailed)
- [static var objectNotFound: TKError.Code](/documentation/cryptotokenkit/tkerror/objectnotfound)
- [static var tokenNotFound: TKError.Code](/documentation/cryptotokenkit/tkerror/tokennotfound)
- [static var badParameter: TKError.Code](/documentation/cryptotokenkit/tkerror/badparameter)
- [static var authenticationNeeded: TKError.Code](/documentation/cryptotokenkit/tkerror/authenticationneeded)
- [static var TKErrorAuthenticationFailed: TKError.Code](/documentation/cryptotokenkit/tkerror/tkerrorauthenticationfailed)
- [static var TKErrorObjectNotFound: TKError.Code](/documentation/cryptotokenkit/tkerror/tkerrorobjectnotfound)
- [static var TKErrorTokenNotFound: TKError.Code](/documentation/cryptotokenkit/tkerror/tkerrortokennotfound)

### Type Properties

- [static var errorDomain: String](/documentation/cryptotokenkit/tkerror/errordomain)
- [let TKErrorDomain: String](/documentation/cryptotokenkit/tkerrordomain)
- [TKError.Code](/documentation/cryptotokenkit/tkerror/code)

### Error Codes

- [case notImplemented](/documentation/cryptotokenkit/tkerror/code/notimplemented)
- [case communicationError](/documentation/cryptotokenkit/tkerror/code/communicationerror)
- [case corruptedData](/documentation/cryptotokenkit/tkerror/code/corrupteddata)
- [case canceledByUser](/documentation/cryptotokenkit/tkerror/code/canceledbyuser)
- [case authenticationFailed](/documentation/cryptotokenkit/tkerror/code/authenticationfailed)
- [case objectNotFound](/documentation/cryptotokenkit/tkerror/code/objectnotfound)
- [case tokenNotFound](/documentation/cryptotokenkit/tkerror/code/tokennotfound)
- [case badParameter](/documentation/cryptotokenkit/tkerror/code/badparameter)
- [case authenticationNeeded](/documentation/cryptotokenkit/tkerror/code/authenticationneeded)
- [static var TKErrorAuthenticationFailed: TKError.Code](/documentation/cryptotokenkit/tkerror/code/tkerrorauthenticationfailed)
- [static var TKErrorObjectNotFound: TKError.Code](/documentation/cryptotokenkit/tkerror/code/tkerrorobjectnotfound)
- [static var TKErrorTokenNotFound: TKError.Code](/documentation/cryptotokenkit/tkerror/code/tkerrortokennotfound)

### Initializers

- [init?(rawValue: Int)](/documentation/cryptotokenkit/tkerror/code/init(rawvalue:))

## Classes

- [TKSmartCardSlotNFCSession](/documentation/cryptotokenkit/tksmartcardslotnfcsession)

### Instance Properties

- [var slotName: String?](/documentation/cryptotokenkit/tksmartcardslotnfcsession/slotname)

### Instance Methods

- [func end()](/documentation/cryptotokenkit/tksmartcardslotnfcsession/end())
- [func update(message: String) throws](/documentation/cryptotokenkit/tksmartcardslotnfcsession/update(message:))
- [TKSmartCardTokenRegistrationManager](/documentation/cryptotokenkit/tksmartcardtokenregistrationmanager)

### Instance Properties

- [var registeredSmartCardTokens: [String]](/documentation/cryptotokenkit/tksmartcardtokenregistrationmanager/registeredsmartcardtokens)

### Instance Methods

- [func registerSmartCard(tokenID: String, promptMessage: String) throws](/documentation/cryptotokenkit/tksmartcardtokenregistrationmanager/registersmartcard(tokenid:promptmessage:))
- [func unregisterSmartCard(tokenID: String) throws](/documentation/cryptotokenkit/tksmartcardtokenregistrationmanager/unregistersmartcard(tokenid:))

### Type Properties

- [class var `default`: TKSmartCardTokenRegistrationManager](/documentation/cryptotokenkit/tksmartcardtokenregistrationmanager/default)

## Type Aliases

- [TKTokenObjectID](/documentation/cryptotokenkit/tktokenobjectid-8mo7f)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
