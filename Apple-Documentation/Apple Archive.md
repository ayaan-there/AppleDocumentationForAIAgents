# Apple Archive Documentation

Source: https://sosumi.ai/documentation/applearchive

---
title: Apple Archive
source: https://developer.apple.com/documentation/applearchive
timestamp: 2026-02-13T18:53:27.944Z
---

## Apple Archive essentials

- [Compressing single files](/documentation/accelerate/compressing-single-files)
- [Decompressing single files](/documentation/accelerate/decompressing-single-files)
- [Compressing file system directories](/documentation/accelerate/compressing-file-system-directories)
- [Decompressing and extracting an archived directory](/documentation/accelerate/decompressing-and-extracting-an-archived-directory)
- [Compressing and saving a string to the file system](/documentation/accelerate/compressing-and-saving-a-string-to-the-file-system)
- [Decompressing and parsing an archived string](/documentation/accelerate/decompressing-and-parsing-an-archived-string)

## Apple Encrypted Archive essentials

- [Encrypting and Decrypting a String](/documentation/applearchive/encrypting-and-decrypting-a-string)
- [Encrypting and Decrypting a Single File](/documentation/applearchive/encrypting-and-decrypting-a-single-file)
- [Encrypting and Decrypting Directories](/documentation/applearchive/encrypting-and-decrypting-directories)
- [ArchiveEncryptionContext](/documentation/applearchive/archiveencryptioncontext)

### Creating an archive encryption context

- [init?(from: ArchiveByteStream)](/documentation/applearchive/archiveencryptioncontext/init(from:))
- [init(profile: ArchiveEncryptionContext.Profile, compressionAlgorithm: ArchiveCompression, compressionBlockSize: Int)](/documentation/applearchive/archiveencryptioncontext/init(profile:compressionalgorithm:compressionblocksize:))

### Setting and retrieving keys

- [var mainKey: SymmetricKey?](/documentation/applearchive/archiveencryptioncontext/mainkey)
- [var symmetricKey: SymmetricKey?](/documentation/applearchive/archiveencryptioncontext/symmetrickey)
- [func generateSymmetricKey() throws -> SymmetricKey](/documentation/applearchive/archiveencryptioncontext/generatesymmetrickey())
- [func setSymmetricKey(SymmetricKey) throws](/documentation/applearchive/archiveencryptioncontext/setsymmetrickey(_:))
- [func setRecipientPrivateKey(P256.KeyAgreement.PrivateKey) throws](/documentation/applearchive/archiveencryptioncontext/setrecipientprivatekey(_:))
- [func setSigningPrivateKey(P256.Signing.PrivateKey) throws](/documentation/applearchive/archiveencryptioncontext/setsigningprivatekey(_:))
- [func setRecipientPublicKey(P256.KeyAgreement.PublicKey) throws](/documentation/applearchive/archiveencryptioncontext/setrecipientpublickey(_:))
- [func setSigningPublicKey(P256.Signing.PublicKey) throws](/documentation/applearchive/archiveencryptioncontext/setsigningpublickey(_:))

### Signing an encryption context

- [static func sign(encryptedStream: ArchiveByteStream, encryptionContext: ArchiveEncryptionContext) throws](/documentation/applearchive/archiveencryptioncontext/sign(encryptedstream:encryptioncontext:))
- [var signatureMode: ArchiveEncryptionContext.SignatureMode](/documentation/applearchive/archiveencryptioncontext/signaturemode-swift.property)
- [ArchiveEncryptionContext.SignatureMode](/documentation/applearchive/archiveencryptioncontext/signaturemode-swift.struct)

#### Signature Mode Constants

- [static let none: ArchiveEncryptionContext.SignatureMode](/documentation/applearchive/archiveencryptioncontext/signaturemode-swift.struct/none)
- [static let ecdsa_p256: ArchiveEncryptionContext.SignatureMode](/documentation/applearchive/archiveencryptioncontext/signaturemode-swift.struct/ecdsa_p256)

#### Raw Values

- [var rawValue: UInt32](/documentation/applearchive/archiveencryptioncontext/signaturemode-swift.struct/rawvalue)

### Getting and setting encryption context properties

- [func decryptAttributes() -> Bool](/documentation/applearchive/archiveencryptioncontext/decryptattributes())
- [var archiveIdentifier: Data?](/documentation/applearchive/archiveencryptioncontext/archiveidentifier)
- [var authData: Data?](/documentation/applearchive/archiveencryptioncontext/authdata)
- [var checksumMode: ArchiveEncryptionContext.ChecksumMode](/documentation/applearchive/archiveencryptioncontext/checksummode-swift.property)
- [ArchiveEncryptionContext.ChecksumMode](/documentation/applearchive/archiveencryptioncontext/checksummode-swift.struct)

#### Checksum Mode Constants

- [static let none: ArchiveEncryptionContext.ChecksumMode](/documentation/applearchive/archiveencryptioncontext/checksummode-swift.struct/none)
- [static let murmurhash64: ArchiveEncryptionContext.ChecksumMode](/documentation/applearchive/archiveencryptioncontext/checksummode-swift.struct/murmurhash64)
- [static let sha256: ArchiveEncryptionContext.ChecksumMode](/documentation/applearchive/archiveencryptioncontext/checksummode-swift.struct/sha256)
- [var containerSize: Int](/documentation/applearchive/archiveencryptioncontext/containersize)
- [var encryptionMode: ArchiveEncryptionContext.EncryptionMode](/documentation/applearchive/archiveencryptioncontext/encryptionmode-swift.property)
- [ArchiveEncryptionContext.EncryptionMode](/documentation/applearchive/archiveencryptioncontext/encryptionmode-swift.struct)

#### Encryption Mode Constants

- [static let none: ArchiveEncryptionContext.EncryptionMode](/documentation/applearchive/archiveencryptioncontext/encryptionmode-swift.struct/none)
- [static let ecdhe_p256: ArchiveEncryptionContext.EncryptionMode](/documentation/applearchive/archiveencryptioncontext/encryptionmode-swift.struct/ecdhe_p256)
- [static let scrypt: ArchiveEncryptionContext.EncryptionMode](/documentation/applearchive/archiveencryptioncontext/encryptionmode-swift.struct/scrypt)
- [static let symmetric: ArchiveEncryptionContext.EncryptionMode](/documentation/applearchive/archiveencryptioncontext/encryptionmode-swift.struct/symmetric)
- [var compressionAlgorithm: ArchiveCompression](/documentation/applearchive/archiveencryptioncontext/compressionalgorithm)
- [ArchiveCompression](/documentation/applearchive/archivecompression)

#### Type Properties

- [static let none: ArchiveCompression](/documentation/applearchive/archivecompression/none)
- [static let lzfse: ArchiveCompression](/documentation/applearchive/archivecompression/lzfse)
- [static let lz4: ArchiveCompression](/documentation/applearchive/archivecompression/lz4)
- [static let lzma: ArchiveCompression](/documentation/applearchive/archivecompression/lzma)
- [static let zlib: ArchiveCompression](/documentation/applearchive/archivecompression/zlib)
- [static let lzbitmap: ArchiveCompression](/documentation/applearchive/archivecompression/lzbitmap)

#### Initializers

- [init(algo: Algorithm)](/documentation/applearchive/archivecompression/init(algo:))
- [var compressionBlockSize: Int](/documentation/applearchive/archiveencryptioncontext/compressionblocksize)
- [var paddingSize: Int](/documentation/applearchive/archiveencryptioncontext/paddingsize)
- [var profile: ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.property)
- [ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.struct)

#### Profile Constants

- [static let hkdf_sha256_hmac__none__ecdsa_p256: ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.struct/hkdf_sha256_hmac__none__ecdsa_p256)
- [static let hkdf_sha256_aesctr_hmac__symmetric__none: ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.struct/hkdf_sha256_aesctr_hmac__symmetric__none)
- [static let hkdf_sha256_aesctr_hmac__symmetric__ecdsa_p256: ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.struct/hkdf_sha256_aesctr_hmac__symmetric__ecdsa_p256)
- [static let hkdf_sha256_aesctr_hmac__ecdhe_p256__none: ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.struct/hkdf_sha256_aesctr_hmac__ecdhe_p256__none)
- [static let hkdf_sha256_aesctr_hmac__ecdhe_p256__ecdsa_p256: ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.struct/hkdf_sha256_aesctr_hmac__ecdhe_p256__ecdsa_p256)
- [static let hkdf_sha256_aesctr_hmac__scrypt__none: ArchiveEncryptionContext.Profile](/documentation/applearchive/archiveencryptioncontext/profile-swift.struct/hkdf_sha256_aesctr_hmac__scrypt__none)
- [var rawSize: Int](/documentation/applearchive/archiveencryptioncontext/rawsize)
- [var signatureEncryptionKey: SymmetricKey?](/documentation/applearchive/archiveencryptioncontext/signatureencryptionkey)

### Setting a password

- [var password: String?](/documentation/applearchive/archiveencryptioncontext/password)
- [func generatePassword() throws -> String](/documentation/applearchive/archiveencryptioncontext/generatepassword())
- [func setPassword(String) throws](/documentation/applearchive/archiveencryptioncontext/setpassword(_:))

## Apple Archive headers

- [ArchiveHeader](/documentation/applearchive/archiveheader)

### Creating an Archive Header

- [init()](/documentation/applearchive/archiveheader/init())
- [init?(keySet: ArchiveHeader.FieldKeySet, directory: FilePath, path: FilePath, flags: ArchiveFlags)](/documentation/applearchive/archiveheader/init(keyset:directory:path:flags:))
- [init?(withAAEncodedData: UnsafeBufferPointer<UInt8>)](/documentation/applearchive/archiveheader/init(withaaencodeddata:))
- [init(copying: ArchiveHeader)](/documentation/applearchive/archiveheader/init(copying:))

### Manipulating Fields

- [func field(forKey: ArchiveHeader.FieldKey) -> ArchiveHeader.Field?](/documentation/applearchive/archiveheader/field(forkey:))
- [ArchiveHeader.FieldKey](/documentation/applearchive/archiveheader/fieldkey-swift.struct)

#### Field Key Creation

- [init(String)](/documentation/applearchive/archiveheader/fieldkey-swift.struct/init(_:))

#### Instance Properties

- [var description: String](/documentation/applearchive/archiveheader/fieldkey-swift.struct/description)

#### Equatable Requirements

- [static func == (ArchiveHeader.FieldKey, ArchiveHeader.FieldKey) -> Bool](/documentation/applearchive/archiveheader/fieldkey-swift.struct/==(_:_:))

#### Hash Values

- [func hash(into: inout Hasher)](/documentation/applearchive/archiveheader/fieldkey-swift.struct/hash(into:))
- [ArchiveHeader.Field](/documentation/applearchive/archiveheader/field)

#### Field Constants

- [case blob(key: ArchiveHeader.FieldKey, size: UInt64, offset: UInt64)](/documentation/applearchive/archiveheader/field/blob(key:size:offset:))
- [case flag(key: ArchiveHeader.FieldKey)](/documentation/applearchive/archiveheader/field/flag(key:))
- [case hash(key: ArchiveHeader.FieldKey, hashFunction: ArchiveHash, value: ContiguousArray<UInt8>)](/documentation/applearchive/archiveheader/field/hash(key:hashfunction:value:))
- [case string(key: ArchiveHeader.FieldKey, value: String)](/documentation/applearchive/archiveheader/field/string(key:value:))
- [case timespec(key: ArchiveHeader.FieldKey, value: timespec)](/documentation/applearchive/archiveheader/field/timespec(key:value:))
- [case uint(key: ArchiveHeader.FieldKey, value: UInt64)](/documentation/applearchive/archiveheader/field/uint(key:value:))

#### Instance Properties

- [var key: ArchiveHeader.FieldKey](/documentation/applearchive/archiveheader/field/key)
- [var type: ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/field/type)
- [var fieldType: ArchiveHeader._FieldTypes](/documentation/applearchive/archiveheader/fieldtype-swift.property)
- [ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/fieldtype-swift.struct)

#### Field Types

- [static let blob: ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/fieldtype-swift.struct/blob)
- [static let flag: ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/fieldtype-swift.struct/flag)
- [static let hash: ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/fieldtype-swift.struct/hash)
- [static let string: ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/fieldtype-swift.struct/string)
- [static let timespec: ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/fieldtype-swift.struct/timespec)
- [static let uint: ArchiveHeader.FieldType](/documentation/applearchive/archiveheader/fieldtype-swift.struct/uint)

#### Raw Values

- [init(rawValue: UInt32)](/documentation/applearchive/archiveheader/fieldtype-swift.struct/init(rawvalue:))
- [var rawValue: UInt32](/documentation/applearchive/archiveheader/fieldtype-swift.struct/rawvalue)

#### Instance Properties

- [var description: String](/documentation/applearchive/archiveheader/fieldtype-swift.struct/description)
- [var fieldKey: ArchiveHeader._FieldKeys](/documentation/applearchive/archiveheader/fieldkey-swift.property)
- [ArchiveHeader.FieldKeySet](/documentation/applearchive/archiveheader/fieldkeyset)

#### Creating a Field Key Set

- [init()](/documentation/applearchive/archiveheader/fieldkeyset/init())
- [init?(String)](/documentation/applearchive/archiveheader/fieldkeyset/init(_:))
- [init(copying: ArchiveHeader.FieldKeySet)](/documentation/applearchive/archiveheader/fieldkeyset/init(copying:))

#### Specifying Default Field Key Sets

- [static var defaultForArchive: ArchiveHeader.FieldKeySet](/documentation/applearchive/archiveheader/fieldkeyset/defaultforarchive)
- [static var defaultForManifest: ArchiveHeader.FieldKeySet](/documentation/applearchive/archiveheader/fieldkeyset/defaultformanifest)

### Manipulating Entries

- [ArchiveHeader.EntryAttributes](/documentation/applearchive/archiveheader/entryattributes)

#### Instance Properties

- [var btm: timespec?](/documentation/applearchive/archiveheader/entryattributes/btm)
- [var ctm: timespec?](/documentation/applearchive/archiveheader/entryattributes/ctm)
- [var flg: UInt32?](/documentation/applearchive/archiveheader/entryattributes/flg)
- [var gid: UInt32?](/documentation/applearchive/archiveheader/entryattributes/gid)
- [var mod: UInt32?](/documentation/applearchive/archiveheader/entryattributes/mod)
- [var mtm: timespec?](/documentation/applearchive/archiveheader/entryattributes/mtm)
- [var uid: UInt32?](/documentation/applearchive/archiveheader/entryattributes/uid)
- [ArchiveHeader.EntryXATBlob](/documentation/applearchive/archiveheader/entryxatblob)

#### Creating an Extended Attributes Blob

- [init()](/documentation/applearchive/archiveheader/entryxatblob/init())
- [init?(directory: FilePath, path: FilePath, flags: ArchiveFlags)](/documentation/applearchive/archiveheader/entryxatblob/init(directory:path:flags:))
- [init?(withAAEncodedData: UnsafeBufferPointer<UInt8>)](/documentation/applearchive/archiveheader/entryxatblob/init(withaaencodeddata:))

#### Applying an Extended Attributes Blob

- [func apply(directory: FilePath, path: FilePath, flags: ArchiveFlags) throws](/documentation/applearchive/archiveheader/entryxatblob/apply(directory:path:flags:))

#### Describing Extended Attributes

- [ArchiveHeader.EntryXATBlob.ExtendedAttribute](/documentation/applearchive/archiveheader/entryxatblob/extendedattribute)

##### Creating an Extended Attribute

- [init(key: String, data: ContiguousArray<UInt8>)](/documentation/applearchive/archiveheader/entryxatblob/extendedattribute/init(key:data:))

#### Collection Requirements

- [func append(ArchiveHeader.EntryXATBlob.ExtendedAttribute)](/documentation/applearchive/archiveheader/entryxatblob/append(_:))
- [func remove(at: Int) -> ArchiveHeader.EntryXATBlob.ExtendedAttribute](/documentation/applearchive/archiveheader/entryxatblob/remove(at:))
- [func removeAll()](/documentation/applearchive/archiveheader/entryxatblob/removeall())
- [func withAAEncodedData<R>((UnsafeBufferPointer<UInt8>) throws -> R) rethrows -> R](/documentation/applearchive/archiveheader/entryxatblob/withaaencodeddata(_:))
- [var entryType: ArchiveHeader.EntryType?](/documentation/applearchive/archiveheader/entrytype-swift.property)
- [ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct)

#### Entry Types

- [static let blockSpecial: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/blockspecial)
- [static let characterSpecial: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/characterspecial)
- [static let directory: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/directory)
- [static let door: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/door)
- [static let fifo: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/fifo)
- [static let link: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/link)
- [static let metadata: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/metadata)
- [static let port: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/port)
- [static let regularFile: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/regularfile)
- [static let socket: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/socket)
- [static let whiteout: ArchiveHeader.EntryType](/documentation/applearchive/archiveheader/entrytype-swift.struct/whiteout)

#### Instance Properties

- [var description: String](/documentation/applearchive/archiveheader/entrytype-swift.struct/description)

#### Raw Values

- [init(rawValue: UInt32)](/documentation/applearchive/archiveheader/entrytype-swift.struct/init(rawvalue:))
- [var rawValue: UInt32](/documentation/applearchive/archiveheader/entrytype-swift.struct/rawvalue)
- [ArchiveHeader.EntryFilter](/documentation/applearchive/archiveheader/entryfilter)
- [ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage)

#### Entry Messages

- [static let convertExclude: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/convertexclude)
- [static let decodeReading: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/decodereading)
- [static let encodeScanning: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/encodescanning)
- [static let encodeWriting: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/encodewriting)
- [static let extractACL: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/extractacl)
- [static let extractAttributes: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/extractattributes)
- [static let extractBegin: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/extractbegin)
- [static let extractEnd: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/extractend)
- [static let extractFail: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/extractfail)
- [static let extractXAT: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/extractxat)
- [static let processExclude: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/processexclude)
- [static let searchExclude: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/searchexclude)
- [static let searchFail: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/searchfail)
- [static let searchPruneDirectory: ArchiveHeader.EntryMessage](/documentation/applearchive/archiveheader/entrymessage/searchprunedirectory)

#### Instance Properties

- [var description: String](/documentation/applearchive/archiveheader/entrymessage/description)

#### Raw Values

- [var rawValue: UInt32](/documentation/applearchive/archiveheader/entrymessage/rawvalue)
- [init(rawValue: UInt32)](/documentation/applearchive/archiveheader/entrymessage/init(rawvalue:))
- [ArchiveHeader.EntryFilterData](/documentation/applearchive/archiveheader/entryfilterdata)

#### Enumeration Cases

- [case entryAttributes(ArchiveHeader.EntryAttributes)](/documentation/applearchive/archiveheader/entryfilterdata/entryattributes(_:))
- [case entryXAT(ArchiveHeader.EntryXATBlob)](/documentation/applearchive/archiveheader/entryfilterdata/entryxat(_:))
- [case header(ArchiveHeader)](/documentation/applearchive/archiveheader/entryfilterdata/header(_:))
- [ArchiveHeader.EntryMessageStatus](/documentation/applearchive/archiveheader/entrymessagestatus)

#### Entry Message Statuses

- [static let cancel: ArchiveHeader.EntryMessageStatus](/documentation/applearchive/archiveheader/entrymessagestatus/cancel)
- [static let ok: ArchiveHeader.EntryMessageStatus](/documentation/applearchive/archiveheader/entrymessagestatus/ok)
- [static let skip: ArchiveHeader.EntryMessageStatus](/documentation/applearchive/archiveheader/entrymessagestatus/skip)

#### Instance Properties

- [var description: String](/documentation/applearchive/archiveheader/entrymessagestatus/description)

#### Raw Values

- [var rawValue: Int32](/documentation/applearchive/archiveheader/entrymessagestatus/rawvalue)
- [init(rawValue: Int32)](/documentation/applearchive/archiveheader/entrymessagestatus/init(rawvalue:))

### Accessing File Paths

- [var entryPath: FilePath?](/documentation/applearchive/archiveheader/entrypath)

### Accessing AppleArchive Encoded Data

- [func withAAEncodedData<R>((UnsafeBufferPointer<UInt8>) throws -> R) rethrows -> R](/documentation/applearchive/archiveheader/withaaencodeddata(_:))

### Collection Requirements

- [func append(ArchiveHeader.Field)](/documentation/applearchive/archiveheader/append(_:))
- [func remove(at: Int) -> ArchiveHeader.Field](/documentation/applearchive/archiveheader/remove(at:))
- [func removeAll()](/documentation/applearchive/archiveheader/removeall())

## Apple Archive streams

- [ArchiveStreamProtocol](/documentation/applearchive/archivestreamprotocol)

### Reading and Writing Blobs

- [func readBlob(key: ArchiveHeader.FieldKey, into: UnsafeMutableRawBufferPointer) throws](/documentation/applearchive/archivestreamprotocol/readblob(key:into:))
- [func writeBlob(key: ArchiveHeader.FieldKey, from: UnsafeRawBufferPointer) throws](/documentation/applearchive/archivestreamprotocol/writeblob(key:from:))

### Reading and Writing Headers

- [func readHeader() throws -> ArchiveHeader?](/documentation/applearchive/archivestreamprotocol/readheader())
- [func writeHeader(ArchiveHeader) throws](/documentation/applearchive/archivestreamprotocol/writeheader(_:))

### Using Archive Streams

- [func cancel()](/documentation/applearchive/archivestreamprotocol/cancel())
- [func close() throws](/documentation/applearchive/archivestreamprotocol/close())
- [ArchiveStream](/documentation/applearchive/archivestream)

### Creating an Archive Stream

- [init(object: _AAOptionalObjectWrapperWithFilter<_AAArchiveStreamTraits>.AAType?, owned: Bool, messageProc: ArchiveHeader._EntryFilterWrapper?)](/documentation/applearchive/archivestream/init(object:owned:messageproc:))

### Writing Directory Contents

- [func writeDirectoryContents(archiveFrom: FilePath, path: FilePath?, keySet: ArchiveHeader.FieldKeySet, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int) throws](/documentation/applearchive/archivestream/writedirectorycontents(archivefrom:path:keyset:selectusing:flags:threadcount:))

### Extracting Data

- [static func extractStream(extractingTo: FilePath, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int) -> ArchiveStream?](/documentation/applearchive/archivestream/extractstream(extractingto:selectusing:flags:threadcount:))
- [static func withExtractStream<E>(extractingTo: FilePath, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int, (ArchiveStream) throws -> E) throws -> E](/documentation/applearchive/archivestream/withextractstream(extractingto:selectusing:flags:threadcount:_:))

### Encoding Data

- [static func encodeStream(writingTo: ArchiveByteStream, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int) -> ArchiveStream?](/documentation/applearchive/archivestream/encodestream(writingto:selectusing:flags:threadcount:))
- [static func withEncodeStream<E>(writingTo: ArchiveByteStream, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int, (ArchiveStream) throws -> E) throws -> E](/documentation/applearchive/archivestream/withencodestream(writingto:selectusing:flags:threadcount:_:))

### Decoding Data

- [static func decodeStream(readingFrom: ArchiveByteStream, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int) -> ArchiveStream?](/documentation/applearchive/archivestream/decodestream(readingfrom:selectusing:flags:threadcount:))
- [static func withDecodeStream<E>(readingFrom: ArchiveByteStream, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int, (ArchiveStream) throws -> E) throws -> E](/documentation/applearchive/archivestream/withdecodestream(readingfrom:selectusing:flags:threadcount:_:))

### Converting Data

- [static func convertStream(writingTo: ArchiveStream, insertKeySet: ArchiveHeader.FieldKeySet, removeKeySet: ArchiveHeader.FieldKeySet, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int) -> ArchiveStream?](/documentation/applearchive/archivestream/convertstream(writingto:insertkeyset:removekeyset:selectusing:flags:threadcount:))
- [static func withConvertStream<E>(writingTo: ArchiveStream, insertKeySet: ArchiveHeader.FieldKeySet, removeKeySet: ArchiveHeader.FieldKeySet, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int, (ArchiveStream) throws -> E) throws -> E](/documentation/applearchive/archivestream/withconvertstream(writingto:insertkeyset:removekeyset:selectusing:flags:threadcount:_:))

### Processing Data

- [static func process(readingFrom: ArchiveStream, writingTo: ArchiveStream, selectUsing: ArchiveHeader.EntryFilter?, flags: ArchiveFlags, threadCount: Int) throws -> Int](/documentation/applearchive/archivestream/process(readingfrom:writingto:selectusing:flags:threadcount:))

### Using Custom Streams

- [static func customStream<C>(instance: C) -> ArchiveStream?](/documentation/applearchive/archivestream/customstream(instance:))
- [static func withStream<C, E>(wrapping: C, (ArchiveStream) throws -> E) throws -> E](/documentation/applearchive/archivestream/withstream(wrapping:_:))
- [ArchiveByteStreamProtocol](/documentation/applearchive/archivebytestreamprotocol)

### Reading and Writing Data

- [func read(into: UnsafeMutableRawBufferPointer) throws -> Int](/documentation/applearchive/archivebytestreamprotocol/read(into:))
- [func read(into: UnsafeMutableRawBufferPointer, atOffset: Int64) throws -> Int](/documentation/applearchive/archivebytestreamprotocol/read(into:atoffset:))
- [func write(from: UnsafeRawBufferPointer) throws -> Int](/documentation/applearchive/archivebytestreamprotocol/write(from:))
- [func write(from: UnsafeRawBufferPointer, atOffset: Int64) throws -> Int](/documentation/applearchive/archivebytestreamprotocol/write(from:atoffset:))

### Using Archive Byte Streams

- [func seek(toOffset: Int64, relativeTo: FileDescriptor.SeekOrigin) throws -> Int64](/documentation/applearchive/archivebytestreamprotocol/seek(tooffset:relativeto:))
- [func cancel()](/documentation/applearchive/archivebytestreamprotocol/cancel())
- [func close() throws](/documentation/applearchive/archivebytestreamprotocol/close())
- [ArchiveByteStream](/documentation/applearchive/archivebytestream)

### Creating an Archive Byte Stream

- [init(object: _AAOptionalObjectWrapper<_AAByteStreamTraits>.AAType?, owned: Bool)](/documentation/applearchive/archivebytestream/init(object:owned:))

### Using Archive Byte Streams

- [func close(updatingContext: ArchiveEncryptionContext) throws](/documentation/applearchive/archivebytestream/close(updatingcontext:))

### Compressing Data

- [static func compressionStream(using: ArchiveCompression, writingTo: ArchiveByteStream, blockSize: Int, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/compressionstream(using:writingto:blocksize:flags:threadcount:))
- [static func withCompressionStream<E>(using: ArchiveCompression, writingTo: ArchiveByteStream, blockSize: Int, flags: ArchiveFlags, threadCount: Int, (ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withcompressionstream(using:writingto:blocksize:flags:threadcount:_:))
- [static func compressionStream(appendingTo: ArchiveByteStream, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/compressionstream(appendingto:flags:threadcount:))
- [static func withCompressionStream<E>(appendingTo: ArchiveByteStream, flags: ArchiveFlags, threadCount: Int, (ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withcompressionstream(appendingto:flags:threadcount:_:))

### Decompressing Data

- [static func decompressionStream(readingFrom: ArchiveByteStream, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/decompressionstream(readingfrom:flags:threadcount:))
- [static func withDecompressionStream<E>(readingFrom: ArchiveByteStream, flags: ArchiveFlags, threadCount: Int, (ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withdecompressionstream(readingfrom:flags:threadcount:_:))
- [static func randomAccessDecompressionStream(readingFrom: ArchiveByteStream, allocationLimit: Int, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/randomaccessdecompressionstream(readingfrom:allocationlimit:flags:threadcount:))
- [static func withRandomAccessDecompressionStream<E>(readingFrom: ArchiveByteStream, allocationLimit: Int, flags: ArchiveFlags, threadCount: Int, (ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withrandomaccessdecompressionstream(readingfrom:allocationlimit:flags:threadcount:_:))

### Encrypting Data

- [static func encryptionStream(appendingTo: ArchiveByteStream, encryptionContext: ArchiveEncryptionContext, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/encryptionstream(appendingto:encryptioncontext:flags:threadcount:))
- [static func encryptionStream(writingTo: ArchiveByteStream, encryptionContext: ArchiveEncryptionContext, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/encryptionstream(writingto:encryptioncontext:flags:threadcount:))

### Decrypting Data

- [static func decryptionStream(readingFrom: ArchiveByteStream, encryptionContext: ArchiveEncryptionContext, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/decryptionstream(readingfrom:encryptioncontext:flags:threadcount:))
- [static func randomAccessDecryptionStream(readingFrom: ArchiveByteStream, encryptionContext: ArchiveEncryptionContext, allocationLimit: Int, flags: ArchiveFlags, threadCount: Int) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/randomaccessdecryptionstream(readingfrom:encryptioncontext:allocationlimit:flags:threadcount:))

### Processing Data

- [static func process(readingFrom: ArchiveByteStream, writingTo: ArchiveByteStream) throws -> Int64](/documentation/applearchive/archivebytestream/process(readingfrom:writingto:))

### File Streaming

- [static func fileStream(fd: FileDescriptor, automaticClose: Bool) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/filestream(fd:automaticclose:))
- [static func withFileStream<E>(fd: FileDescriptor, automaticClose: Bool, (ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withfilestream(fd:automaticclose:_:))
- [static func fileStream(path: FilePath, mode: FileDescriptor.AccessMode, options: FileDescriptor.OpenOptions, permissions: FilePermissions) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/filestream(path:mode:options:permissions:))
- [static func withFileStream<E>(path: FilePath, mode: FileDescriptor.AccessMode, options: FileDescriptor.OpenOptions, permissions: FilePermissions, (ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withfilestream(path:mode:options:permissions:_:))
- [static func temporaryFileStream() -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/temporaryfilestream())
- [static func withTemporaryFileStream<E>((ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withtemporaryfilestream(_:))

### Streaming with Custom Streams

- [static func customStream<C>(instance: C) -> ArchiveByteStream?](/documentation/applearchive/archivebytestream/customstream(instance:))
- [static func withStream<C, E>(wrapping: C, (ArchiveByteStream) throws -> E) throws -> E](/documentation/applearchive/archivebytestream/withstream(wrapping:_:))
- [static func sharedBufferPipe(capacity: Int) -> (output: ArchiveByteStream, input: ArchiveByteStream)?](/documentation/applearchive/archivebytestream/sharedbufferpipe(capacity:))

## Apple Archive errors

- [ArchiveError](/documentation/applearchive/archiveerror)

### AppleArchive Errors

- [case invalidValue](/documentation/applearchive/archiveerror/invalidvalue)
- [case ioError](/documentation/applearchive/archiveerror/ioerror)

## Constants

- [var APPLE_ARCHIVE_API_VERSION: Int32](/documentation/applearchive/apple_archive_api_version)

## Reference

- [Apple Archive structures](/documentation/applearchive/apple-archive-structures)

### Structures

- [AEAContextTraits](/documentation/applearchive/aeacontexttraits)

#### Type Aliases

- [AEAContextTraits.AAType](/documentation/applearchive/aeacontexttraits/aatype)

#### Type Methods

- [static func aaDestroy(AEAContextTraits.AAType?)](/documentation/applearchive/aeacontexttraits/aadestroy(_:))
- [ArchiveFlags](/documentation/applearchive/archiveflags)

#### Type Properties

- [static let archiveDeduplicateData: ArchiveFlags](/documentation/applearchive/archiveflags/archivededuplicatedata)
- [static let extractNoAutoDeduplicate: ArchiveFlags](/documentation/applearchive/archiveflags/extractnoautodeduplicate)
- [static let extractNoAutoSparse: ArchiveFlags](/documentation/applearchive/archiveflags/extractnoautosparse)
- [static let ignoreOperationNotPermitted: ArchiveFlags](/documentation/applearchive/archiveflags/ignoreoperationnotpermitted)
- [static let replaceAttributes: ArchiveFlags](/documentation/applearchive/archiveflags/replaceattributes)

#### Type Methods

- [static func verbosity(level: Int) -> ArchiveFlags](/documentation/applearchive/archiveflags/verbosity(level:))
- [ArchiveHash](/documentation/applearchive/archivehash)

#### Initializers

- [init(rawValue: UInt32)](/documentation/applearchive/archivehash/init(rawvalue:))

#### Instance Properties

- [var description: String](/documentation/applearchive/archivehash/description)
- [var rawValue: UInt32](/documentation/applearchive/archivehash/rawvalue)
- [var size: Int](/documentation/applearchive/archivehash/size)

#### Type Properties

- [static let crc32: ArchiveHash](/documentation/applearchive/archivehash/crc32)
- [static let maxSize: Int](/documentation/applearchive/archivehash/maxsize)
- [static let sha1: ArchiveHash](/documentation/applearchive/archivehash/sha1)
- [static let sha256: ArchiveHash](/documentation/applearchive/archivehash/sha256)
- [static let sha384: ArchiveHash](/documentation/applearchive/archivehash/sha384)
- [static let sha512: ArchiveHash](/documentation/applearchive/archivehash/sha512)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
