# CryptoKit Documentation

Source: https://sosumi.ai/documentation/cryptokit

---
title: Apple CryptoKit
source: https://developer.apple.com/documentation/cryptokit
timestamp: 2026-02-13T19:58:12.128Z
---

## Essentials

- [Complying with Encryption Export Regulations](/documentation/security/complying-with-encryption-export-regulations)
- [Performing Common Cryptographic Operations](/documentation/cryptokit/performing-common-cryptographic-operations)
- [Storing CryptoKit Keys in the Keychain](/documentation/cryptokit/storing-cryptokit-keys-in-the-keychain)
- [Enhancing your app’s privacy and security with quantum-secure workflows](/documentation/cryptokit/enhancing-your-app-s-privacy-and-security-with-quantum-secure-workflows)

## Cryptographically secure hashes

- [HashFunction](/documentation/cryptokit/hashfunction)

### Specifying the output type

- [Digest](/documentation/cryptokit/hashfunction/digest)
- [Digest](/documentation/cryptokit/digest)

#### Getting the digest length

- [static var byteCount: Int](/documentation/cryptokit/digest/bytecount)

#### Comparing digests

- [static func == <D>(Self, D) -> Bool](/documentation/cryptokit/digest/==(_:_:)-7yz3z)
- [static func == (Self, Self) -> Bool](/documentation/cryptokit/digest/==(_:_:)-6m59k)

#### Default Implementations

- [CustomStringConvertible Implementations](/documentation/cryptokit/digest/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/cryptokit/digest/description)

### Computing a hash in one call

- [static func hash<D>(data: D) -> Self.Digest](/documentation/cryptokit/hashfunction/hash(data:))

### Computing a hash iteratively

- [init()](/documentation/cryptokit/hashfunction/init())
- [func update<D>(data: D)](/documentation/cryptokit/hashfunction/update(data:))
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/hashfunction/update(bufferpointer:))
- [func finalize() -> Self.Digest](/documentation/cryptokit/hashfunction/finalize())

### Inspecting hash information

- [static var blockByteCount: Int](/documentation/cryptokit/hashfunction/blockbytecount)
- [SHA512](/documentation/cryptokit/sha512)

### Specifying the output type

- [SHA512.Digest](/documentation/cryptokit/sha512/digest)
- [SHA512Digest](/documentation/cryptokit/sha512digest)

#### Inspecting the digest length

- [static var byteCount: Int](/documentation/cryptokit/sha512digest/bytecount)

#### Describing a digest

- [var description: String](/documentation/cryptokit/sha512digest/description)

#### Hashing a digest

- [func hash(into: inout Hasher)](/documentation/cryptokit/sha512digest/hash(into:))

### Computing a hash iteratively

- [init()](/documentation/cryptokit/sha512/init())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/sha512/update(bufferpointer:))
- [func finalize() -> SHA512.Digest](/documentation/cryptokit/sha512/finalize())

### Inspecting hash information

- [static let byteCount: Int](/documentation/cryptokit/sha512/bytecount)
- [static let blockByteCount: Int](/documentation/cryptokit/sha512/blockbytecount)
- [SHA384](/documentation/cryptokit/sha384)

### Specifying the output type

- [SHA384.Digest](/documentation/cryptokit/sha384/digest)
- [SHA384Digest](/documentation/cryptokit/sha384digest)

#### Inspecting the digest length

- [static var byteCount: Int](/documentation/cryptokit/sha384digest/bytecount)

#### Describing a digest

- [var description: String](/documentation/cryptokit/sha384digest/description)

#### Hashing a digest

- [func hash(into: inout Hasher)](/documentation/cryptokit/sha384digest/hash(into:))

### Computing a hash iteratively

- [init()](/documentation/cryptokit/sha384/init())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/sha384/update(bufferpointer:))
- [func finalize() -> SHA384.Digest](/documentation/cryptokit/sha384/finalize())

### Inspecting hash information

- [static let byteCount: Int](/documentation/cryptokit/sha384/bytecount)
- [static let blockByteCount: Int](/documentation/cryptokit/sha384/blockbytecount)
- [SHA256](/documentation/cryptokit/sha256)

### Specifying the output type

- [SHA256.Digest](/documentation/cryptokit/sha256/digest)
- [SHA256Digest](/documentation/cryptokit/sha256digest)

#### Inspecting the digest length

- [static var byteCount: Int](/documentation/cryptokit/sha256digest/bytecount)

#### Describing a digest

- [var description: String](/documentation/cryptokit/sha256digest/description)

#### Hashing a digest

- [func hash(into: inout Hasher)](/documentation/cryptokit/sha256digest/hash(into:))

### Computing a hash iteratively

- [init()](/documentation/cryptokit/sha256/init())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/sha256/update(bufferpointer:))
- [func finalize() -> SHA256.Digest](/documentation/cryptokit/sha256/finalize())

### Inspecting hash information

- [static let byteCount: Int](/documentation/cryptokit/sha256/bytecount)
- [static let blockByteCount: Int](/documentation/cryptokit/sha256/blockbytecount)

## Message authentication codes

- [HMAC](/documentation/cryptokit/hmac)

### Getting a key

- [HMAC.Key](/documentation/cryptokit/hmac/key)
- [SymmetricKey](/documentation/cryptokit/symmetrickey)

#### Creating a key

- [init<D>(data: D)](/documentation/cryptokit/symmetrickey/init(data:))
- [init(size: SymmetricKeySize)](/documentation/cryptokit/symmetrickey/init(size:))

#### Getting the key length

- [var bitCount: Int](/documentation/cryptokit/symmetrickey/bitcount)

### Working with codes

- [HMAC.MAC](/documentation/cryptokit/hmac/mac)
- [HashedAuthenticationCode](/documentation/cryptokit/hashedauthenticationcode)

#### Retrieving the code length

- [var byteCount: Int](/documentation/cryptokit/hashedauthenticationcode/bytecount)

#### Describing a code

- [var description: String](/documentation/cryptokit/hashedauthenticationcode/description)
- [MessageAuthenticationCode](/documentation/cryptokit/messageauthenticationcode)

#### Retrieving the code length

- [var byteCount: Int](/documentation/cryptokit/messageauthenticationcode/bytecount)

#### Comparing codes

- [static func == <D>(Self, D) -> Bool](/documentation/cryptokit/messageauthenticationcode/==(_:_:)-3rxc4)
- [static func == (Self, Self) -> Bool](/documentation/cryptokit/messageauthenticationcode/==(_:_:)-b90)

#### Default Implementations

- [CustomStringConvertible Implementations](/documentation/cryptokit/messageauthenticationcode/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/cryptokit/messageauthenticationcode/description)

### Creating an authentication code with one call

- [static func authenticationCode<D>(for: D, using: SymmetricKey) -> HMAC<H>.MAC](/documentation/cryptokit/hmac/authenticationcode(for:using:))

### Creating an authentication code iteratively

- [init(key: SymmetricKey)](/documentation/cryptokit/hmac/init(key:))
- [func update<D>(data: D)](/documentation/cryptokit/hmac/update(data:))
- [func finalize() -> HMAC<H>.MAC](/documentation/cryptokit/hmac/finalize())

### Checking an authentication code

- [static func isValidAuthenticationCode<D>(HMAC<H>.MAC, authenticating: D, using: SymmetricKey) -> Bool](/documentation/cryptokit/hmac/isvalidauthenticationcode(_:authenticating:using:)-8ezmw)
- [static func isValidAuthenticationCode(HMAC<H>.MAC, authenticating: UnsafeRawBufferPointer, using: SymmetricKey) -> Bool](/documentation/cryptokit/hmac/isvalidauthenticationcode(_:authenticating:using:)-5jbc8)
- [static func isValidAuthenticationCode<C, D>(C, authenticating: D, using: SymmetricKey) -> Bool](/documentation/cryptokit/hmac/isvalidauthenticationcode(_:authenticating:using:)-5ilt9)
- [SymmetricKey](/documentation/cryptokit/symmetrickey)

### Creating a key

- [init<D>(data: D)](/documentation/cryptokit/symmetrickey/init(data:))
- [init(size: SymmetricKeySize)](/documentation/cryptokit/symmetrickey/init(size:))

### Getting the key length

- [var bitCount: Int](/documentation/cryptokit/symmetrickey/bitcount)
- [SymmetricKeySize](/documentation/cryptokit/symmetrickeysize)

### Using standard key lengths

- [static var bits128: SymmetricKeySize](/documentation/cryptokit/symmetrickeysize/bits128)
- [static var bits192: SymmetricKeySize](/documentation/cryptokit/symmetrickeysize/bits192)
- [static var bits256: SymmetricKeySize](/documentation/cryptokit/symmetrickeysize/bits256)

### Creating a nonstandard key length

- [init(bitCount: Int)](/documentation/cryptokit/symmetrickeysize/init(bitcount:))

### Getting the length

- [let bitCount: Int](/documentation/cryptokit/symmetrickeysize/bitcount)

## Ciphers

- [AES](/documentation/cryptokit/aes)

### AES modes

- [AES.GCM](/documentation/cryptokit/aes/gcm)

#### Storing the output

- [AES.GCM.SealedBox](/documentation/cryptokit/aes/gcm/sealedbox)

##### Creating the sealed box

- [init<C, T>(nonce: AES.GCM.Nonce, ciphertext: C, tag: T) throws](/documentation/cryptokit/aes/gcm/sealedbox/init(nonce:ciphertext:tag:))
- [init<D>(combined: D) throws](/documentation/cryptokit/aes/gcm/sealedbox/init(combined:))

##### Retrieving the combined contents

- [var combined: Data?](/documentation/cryptokit/aes/gcm/sealedbox/combined)

##### Inspecting the component elements

- [var nonce: AES.GCM.Nonce](/documentation/cryptokit/aes/gcm/sealedbox/nonce)
- [var ciphertext: Data](/documentation/cryptokit/aes/gcm/sealedbox/ciphertext)
- [var tag: Data](/documentation/cryptokit/aes/gcm/sealedbox/tag)

#### Getting a nonce

- [AES.GCM.Nonce](/documentation/cryptokit/aes/gcm/nonce)

##### Creating a nonce

- [init()](/documentation/cryptokit/aes/gcm/nonce/init())
- [init<D>(data: D) throws](/documentation/cryptokit/aes/gcm/nonce/init(data:))

##### Iterating over a nonce’s bytes

- [func makeIterator() -> Array<UInt8>.Iterator](/documentation/cryptokit/aes/gcm/nonce/makeiterator())

#### Securing the plaintext message

- [static func seal<Plaintext>(Plaintext, using: SymmetricKey, nonce: AES.GCM.Nonce?) throws -> AES.GCM.SealedBox](/documentation/cryptokit/aes/gcm/seal(_:using:nonce:))
- [static func seal<Plaintext, AuthenticatedData>(Plaintext, using: SymmetricKey, nonce: AES.GCM.Nonce?, authenticating: AuthenticatedData) throws -> AES.GCM.SealedBox](/documentation/cryptokit/aes/gcm/seal(_:using:nonce:authenticating:))

#### Decrypting and verifying the message

- [static func open(AES.GCM.SealedBox, using: SymmetricKey) throws -> Data](/documentation/cryptokit/aes/gcm/open(_:using:))
- [static func open<AuthenticatedData>(AES.GCM.SealedBox, using: SymmetricKey, authenticating: AuthenticatedData) throws -> Data](/documentation/cryptokit/aes/gcm/open(_:using:authenticating:))

### AES wrappers

- [AES.KeyWrap](/documentation/cryptokit/aes/keywrap)

#### Wrapping an AES key

- [static func wrap(SymmetricKey, using: SymmetricKey) throws -> Data](/documentation/cryptokit/aes/keywrap/wrap(_:using:))

#### Unwrapping an AES key

- [static func unwrap<WrappedKey>(WrappedKey, using: SymmetricKey) throws -> SymmetricKey](/documentation/cryptokit/aes/keywrap/unwrap(_:using:))
- [ChaChaPoly](/documentation/cryptokit/chachapoly)

### Storing the output

- [ChaChaPoly.SealedBox](/documentation/cryptokit/chachapoly/sealedbox)

#### Creating the sealed box

- [init<D>(combined: D) throws](/documentation/cryptokit/chachapoly/sealedbox/init(combined:))
- [init<C, T>(nonce: ChaChaPoly.Nonce, ciphertext: C, tag: T) throws](/documentation/cryptokit/chachapoly/sealedbox/init(nonce:ciphertext:tag:))

#### Retrieving the combined contents

- [let combined: Data](/documentation/cryptokit/chachapoly/sealedbox/combined)

#### Inspecting the component elements

- [var nonce: ChaChaPoly.Nonce](/documentation/cryptokit/chachapoly/sealedbox/nonce)
- [var ciphertext: Data](/documentation/cryptokit/chachapoly/sealedbox/ciphertext)
- [var tag: Data](/documentation/cryptokit/chachapoly/sealedbox/tag)

### Getting a nonce

- [ChaChaPoly.Nonce](/documentation/cryptokit/chachapoly/nonce)

#### Creating a nonce

- [init()](/documentation/cryptokit/chachapoly/nonce/init())
- [init<D>(data: D) throws](/documentation/cryptokit/chachapoly/nonce/init(data:))

#### Iterating over a nonce’s bytes

- [func makeIterator() -> Array<UInt8>.Iterator](/documentation/cryptokit/chachapoly/nonce/makeiterator())

### Securing the plaintext message

- [static func seal<Plaintext>(Plaintext, using: SymmetricKey, nonce: ChaChaPoly.Nonce?) throws -> ChaChaPoly.SealedBox](/documentation/cryptokit/chachapoly/seal(_:using:nonce:))
- [static func seal<Plaintext, AuthenticatedData>(Plaintext, using: SymmetricKey, nonce: ChaChaPoly.Nonce?, authenticating: AuthenticatedData) throws -> ChaChaPoly.SealedBox](/documentation/cryptokit/chachapoly/seal(_:using:nonce:authenticating:))

### Decrypting and verifying the message

- [static func open(ChaChaPoly.SealedBox, using: SymmetricKey) throws -> Data](/documentation/cryptokit/chachapoly/open(_:using:))
- [static func open<AuthenticatedData>(ChaChaPoly.SealedBox, using: SymmetricKey, authenticating: AuthenticatedData) throws -> Data](/documentation/cryptokit/chachapoly/open(_:using:authenticating:))

## Public key cryptography

- [Curve25519](/documentation/cryptokit/curve25519)

### Performing operations

- [Curve25519.KeyAgreement](/documentation/cryptokit/curve25519/keyagreement)

#### Using keys

- [Curve25519.KeyAgreement.PrivateKey](/documentation/cryptokit/curve25519/keyagreement/privatekey)

##### Creating a private key

- [init()](/documentation/cryptokit/curve25519/keyagreement/privatekey/init())
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/curve25519/keyagreement/privatekey/init(rawrepresentation:))

##### Reporting the private key

- [var rawRepresentation: Data](/documentation/cryptokit/curve25519/keyagreement/privatekey/rawrepresentation)

##### Finding the public key

- [var publicKey: Curve25519.KeyAgreement.PublicKey](/documentation/cryptokit/curve25519/keyagreement/privatekey/publickey)

##### Creating a shared secret

- [func sharedSecretFromKeyAgreement(with: Curve25519.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/curve25519/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [SharedSecret](/documentation/cryptokit/sharedsecret)

###### Deriving keys

- [func hkdfDerivedSymmetricKey<H, Salt, SI>(using: H.Type, salt: Salt, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/hkdfderivedsymmetrickey(using:salt:sharedinfo:outputbytecount:))
- [func x963DerivedSymmetricKey<H, SI>(using: H.Type, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/x963derivedsymmetrickey(using:sharedinfo:outputbytecount:))

###### Comparing shared secrets

- [static func == <D>(SharedSecret, D) -> Bool](/documentation/cryptokit/sharedsecret/==(_:_:))
- [Curve25519.KeyAgreement.PublicKey](/documentation/cryptokit/curve25519/keyagreement/publickey)

##### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/curve25519/keyagreement/publickey/init(rawrepresentation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/curve25519/keyagreement/publickey/rawrepresentation)

##### Type Aliases

- [Curve25519.KeyAgreement.PublicKey.HPKEEphemeralPrivateKey](/documentation/cryptokit/curve25519/keyagreement/publickey/hpkeephemeralprivatekey)

##### Default Implementations

- [HPKEDiffieHellmanPublicKey Implementations](/documentation/cryptokit/curve25519/keyagreement/publickey/hpkediffiehellmanpublickey-implementations)

###### Type Aliases

- [Curve25519.KeyAgreement.PublicKey.EphemeralPrivateKey](/documentation/cryptokit/curve25519/keyagreement/publickey/ephemeralprivatekey)
- [HPKEPublicKeySerialization Implementations](/documentation/cryptokit/curve25519/keyagreement/publickey/hpkepublickeyserialization-implementations)

###### Initializers

- [init<D>(D, kem: HPKE.KEM) throws](/documentation/cryptokit/curve25519/keyagreement/publickey/init(_:kem:))

###### Instance Methods

- [func hpkeRepresentation(kem: HPKE.KEM) throws -> Data](/documentation/cryptokit/curve25519/keyagreement/publickey/hpkerepresentation(kem:))
- [Curve25519.Signing](/documentation/cryptokit/curve25519/signing)

#### Using keys

- [Curve25519.Signing.PrivateKey](/documentation/cryptokit/curve25519/signing/privatekey)

##### Creating a private key

- [init()](/documentation/cryptokit/curve25519/signing/privatekey/init())
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/curve25519/signing/privatekey/init(rawrepresentation:))

##### Reporting the private key

- [var rawRepresentation: Data](/documentation/cryptokit/curve25519/signing/privatekey/rawrepresentation)

##### Finding the public key

- [var publicKey: Curve25519.Signing.PublicKey](/documentation/cryptokit/curve25519/signing/privatekey/publickey)

##### Creating a signature

- [func signature<D>(for: D) throws -> Data](/documentation/cryptokit/curve25519/signing/privatekey/signature(for:))
- [Curve25519.Signing.PublicKey](/documentation/cryptokit/curve25519/signing/publickey)

##### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/curve25519/signing/publickey/init(rawrepresentation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/curve25519/signing/publickey/rawrepresentation)

##### Verifying a signature

- [func isValidSignature<S, D>(S, for: D) -> Bool](/documentation/cryptokit/curve25519/signing/publickey/isvalidsignature(_:for:))
- [P521](/documentation/cryptokit/p521)

### Performing operations

- [P521.KeyAgreement](/documentation/cryptokit/p521/keyagreement)

#### Using keys

- [P521.KeyAgreement.PrivateKey](/documentation/cryptokit/p521/keyagreement/privatekey)

##### Creating a private key

- [init(compactRepresentable: Bool)](/documentation/cryptokit/p521/keyagreement/privatekey/init(compactrepresentable:))
- [init<Bytes>(rawRepresentation: Bytes) throws](/documentation/cryptokit/p521/keyagreement/privatekey/init(rawrepresentation:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p521/keyagreement/privatekey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p521/keyagreement/privatekey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p521/keyagreement/privatekey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p521/keyagreement/privatekey/rawrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p521/keyagreement/privatekey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p521/keyagreement/privatekey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p521/keyagreement/privatekey/x963representation)

##### Finding the public key

- [var publicKey: P521.KeyAgreement.PublicKey](/documentation/cryptokit/p521/keyagreement/privatekey/publickey)

##### Creating a shared secret

- [func sharedSecretFromKeyAgreement(with: P521.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/p521/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [SharedSecret](/documentation/cryptokit/sharedsecret)

###### Deriving keys

- [func hkdfDerivedSymmetricKey<H, Salt, SI>(using: H.Type, salt: Salt, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/hkdfderivedsymmetrickey(using:salt:sharedinfo:outputbytecount:))
- [func x963DerivedSymmetricKey<H, SI>(using: H.Type, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/x963derivedsymmetrickey(using:sharedinfo:outputbytecount:))

###### Comparing shared secrets

- [static func == <D>(SharedSecret, D) -> Bool](/documentation/cryptokit/sharedsecret/==(_:_:))

##### Default Implementations

- [DiffieHellmanKeyAgreement Implementations](/documentation/cryptokit/p521/keyagreement/privatekey/diffiehellmankeyagreement-implementations)

###### Instance Methods

- [func sharedSecretFromKeyAgreement(with: P521.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/p521/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [HPKEDiffieHellmanPrivateKeyGeneration Implementations](/documentation/cryptokit/p521/keyagreement/privatekey/hpkediffiehellmanprivatekeygeneration-implementations)

###### Initializers

- [init()](/documentation/cryptokit/p521/keyagreement/privatekey/init())
- [P521.KeyAgreement.PublicKey](/documentation/cryptokit/p521/keyagreement/publickey)

##### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p521/keyagreement/publickey/init(rawrepresentation:))
- [init<Bytes>(compactRepresentation: Bytes) throws](/documentation/cryptokit/p521/keyagreement/publickey/init(compactrepresentation:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p521/keyagreement/publickey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p521/keyagreement/publickey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p521/keyagreement/publickey/init(x963representation:))
- [init<Bytes>(compressedRepresentation: Bytes) throws](/documentation/cryptokit/p521/keyagreement/publickey/init(compressedrepresentation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p521/keyagreement/publickey/rawrepresentation)
- [var compactRepresentation: Data?](/documentation/cryptokit/p521/keyagreement/publickey/compactrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p521/keyagreement/publickey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p521/keyagreement/publickey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p521/keyagreement/publickey/x963representation)
- [var compressedRepresentation: Data](/documentation/cryptokit/p521/keyagreement/publickey/compressedrepresentation)

##### Type Aliases

- [P521.KeyAgreement.PublicKey.HPKEEphemeralPrivateKey](/documentation/cryptokit/p521/keyagreement/publickey/hpkeephemeralprivatekey)

##### Default Implementations

- [HPKEDiffieHellmanPublicKey Implementations](/documentation/cryptokit/p521/keyagreement/publickey/hpkediffiehellmanpublickey-implementations)

###### Type Aliases

- [P521.KeyAgreement.PublicKey.EphemeralPrivateKey](/documentation/cryptokit/p521/keyagreement/publickey/ephemeralprivatekey)
- [HPKEPublicKeySerialization Implementations](/documentation/cryptokit/p521/keyagreement/publickey/hpkepublickeyserialization-implementations)

###### Initializers

- [init<D>(D, kem: HPKE.KEM) throws](/documentation/cryptokit/p521/keyagreement/publickey/init(_:kem:))

###### Instance Methods

- [func hpkeRepresentation(kem: HPKE.KEM) throws -> Data](/documentation/cryptokit/p521/keyagreement/publickey/hpkerepresentation(kem:))
- [P521.Signing](/documentation/cryptokit/p521/signing)

#### Using keys

- [P521.Signing.PrivateKey](/documentation/cryptokit/p521/signing/privatekey)

##### Creating a key

- [init<Bytes>(rawRepresentation: Bytes) throws](/documentation/cryptokit/p521/signing/privatekey/init(rawrepresentation:))
- [init(compactRepresentable: Bool)](/documentation/cryptokit/p521/signing/privatekey/init(compactrepresentable:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p521/signing/privatekey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p521/signing/privatekey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p521/signing/privatekey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p521/signing/privatekey/rawrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p521/signing/privatekey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p521/signing/privatekey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p521/signing/privatekey/x963representation)

##### Finding the public key

- [var publicKey: P521.Signing.PublicKey](/documentation/cryptokit/p521/signing/privatekey/publickey)

##### Creating a signature

- [func signature<D>(for: D) throws -> P521.Signing.ECDSASignature](/documentation/cryptokit/p521/signing/privatekey/signature(for:)-34g01)
- [func signature<D>(for: D) throws -> P521.Signing.ECDSASignature](/documentation/cryptokit/p521/signing/privatekey/signature(for:)-7rxva)
- [P521.Signing.ECDSASignature](/documentation/cryptokit/p521/signing/ecdsasignature)

###### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p521/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p521/signing/ecdsasignature/init(rawrepresentation:))

###### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p521/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p521/signing/ecdsasignature/rawrepresentation)
- [P521.Signing.PublicKey](/documentation/cryptokit/p521/signing/publickey)

##### Creating a key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p521/signing/publickey/init(rawrepresentation:))
- [init<Bytes>(compactRepresentation: Bytes) throws](/documentation/cryptokit/p521/signing/publickey/init(compactrepresentation:))
- [init<Bytes>(compressedRepresentation: Bytes) throws](/documentation/cryptokit/p521/signing/publickey/init(compressedrepresentation:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p521/signing/publickey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p521/signing/publickey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p521/signing/publickey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p521/signing/publickey/rawrepresentation)
- [var compactRepresentation: Data?](/documentation/cryptokit/p521/signing/publickey/compactrepresentation)
- [var compressedRepresentation: Data](/documentation/cryptokit/p521/signing/publickey/compressedrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p521/signing/publickey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p521/signing/publickey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p521/signing/publickey/x963representation)

##### Verifying a signature

- [func isValidSignature<D>(P521.Signing.ECDSASignature, for: D) -> Bool](/documentation/cryptokit/p521/signing/publickey/isvalidsignature(_:for:)-5kwev)
- [func isValidSignature<D>(P521.Signing.ECDSASignature, for: D) -> Bool](/documentation/cryptokit/p521/signing/publickey/isvalidsignature(_:for:)-dhjh)
- [P521.Signing.ECDSASignature](/documentation/cryptokit/p521/signing/ecdsasignature)

###### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p521/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p521/signing/ecdsasignature/init(rawrepresentation:))

###### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p521/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p521/signing/ecdsasignature/rawrepresentation)

#### Structures

- [P521.Signing.ECDSASignature](/documentation/cryptokit/p521/signing/ecdsasignature)

##### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p521/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p521/signing/ecdsasignature/init(rawrepresentation:))

##### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p521/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p521/signing/ecdsasignature/rawrepresentation)
- [P384](/documentation/cryptokit/p384)

### Performing operations

- [P384.KeyAgreement](/documentation/cryptokit/p384/keyagreement)

#### Using keys

- [P384.KeyAgreement.PrivateKey](/documentation/cryptokit/p384/keyagreement/privatekey)

##### Creating a private key

- [init<Bytes>(rawRepresentation: Bytes) throws](/documentation/cryptokit/p384/keyagreement/privatekey/init(rawrepresentation:))
- [init(compactRepresentable: Bool)](/documentation/cryptokit/p384/keyagreement/privatekey/init(compactrepresentable:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p384/keyagreement/privatekey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p384/keyagreement/privatekey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p384/keyagreement/privatekey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p384/keyagreement/privatekey/rawrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p384/keyagreement/privatekey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p384/keyagreement/privatekey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p384/keyagreement/privatekey/x963representation)

##### Finding the public key

- [var publicKey: P384.KeyAgreement.PublicKey](/documentation/cryptokit/p384/keyagreement/privatekey/publickey)

##### Creating a shared secret

- [func sharedSecretFromKeyAgreement(with: P384.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/p384/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [SharedSecret](/documentation/cryptokit/sharedsecret)

###### Deriving keys

- [func hkdfDerivedSymmetricKey<H, Salt, SI>(using: H.Type, salt: Salt, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/hkdfderivedsymmetrickey(using:salt:sharedinfo:outputbytecount:))
- [func x963DerivedSymmetricKey<H, SI>(using: H.Type, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/x963derivedsymmetrickey(using:sharedinfo:outputbytecount:))

###### Comparing shared secrets

- [static func == <D>(SharedSecret, D) -> Bool](/documentation/cryptokit/sharedsecret/==(_:_:))

##### Default Implementations

- [DiffieHellmanKeyAgreement Implementations](/documentation/cryptokit/p384/keyagreement/privatekey/diffiehellmankeyagreement-implementations)

###### Instance Methods

- [func sharedSecretFromKeyAgreement(with: P384.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/p384/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [HPKEDiffieHellmanPrivateKeyGeneration Implementations](/documentation/cryptokit/p384/keyagreement/privatekey/hpkediffiehellmanprivatekeygeneration-implementations)

###### Initializers

- [init()](/documentation/cryptokit/p384/keyagreement/privatekey/init())
- [P384.KeyAgreement.PublicKey](/documentation/cryptokit/p384/keyagreement/publickey)

##### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p384/keyagreement/publickey/init(rawrepresentation:))
- [init<Bytes>(compactRepresentation: Bytes) throws](/documentation/cryptokit/p384/keyagreement/publickey/init(compactrepresentation:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p384/keyagreement/publickey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p384/keyagreement/publickey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p384/keyagreement/publickey/init(x963representation:))
- [init<Bytes>(compressedRepresentation: Bytes) throws](/documentation/cryptokit/p384/keyagreement/publickey/init(compressedrepresentation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p384/keyagreement/publickey/rawrepresentation)
- [var compactRepresentation: Data?](/documentation/cryptokit/p384/keyagreement/publickey/compactrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p384/keyagreement/publickey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p384/keyagreement/publickey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p384/keyagreement/publickey/x963representation)
- [var compressedRepresentation: Data](/documentation/cryptokit/p384/keyagreement/publickey/compressedrepresentation)

##### Default Implementations

- [HPKEDiffieHellmanPublicKey Implementations](/documentation/cryptokit/p384/keyagreement/publickey/hpkediffiehellmanpublickey-implementations)

###### Type Aliases

- [P384.KeyAgreement.PublicKey.EphemeralPrivateKey](/documentation/cryptokit/p384/keyagreement/publickey/ephemeralprivatekey)
- [HPKEPublicKeySerialization Implementations](/documentation/cryptokit/p384/keyagreement/publickey/hpkepublickeyserialization-implementations)

###### Initializers

- [init<D>(D, kem: HPKE.KEM) throws](/documentation/cryptokit/p384/keyagreement/publickey/init(_:kem:))

###### Instance Methods

- [func hpkeRepresentation(kem: HPKE.KEM) throws -> Data](/documentation/cryptokit/p384/keyagreement/publickey/hpkerepresentation(kem:))
- [P384.Signing](/documentation/cryptokit/p384/signing)

#### Using keys

- [P384.Signing.PrivateKey](/documentation/cryptokit/p384/signing/privatekey)

##### Creating a private key

- [init<Bytes>(rawRepresentation: Bytes) throws](/documentation/cryptokit/p384/signing/privatekey/init(rawrepresentation:))
- [init(compactRepresentable: Bool)](/documentation/cryptokit/p384/signing/privatekey/init(compactrepresentable:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p384/signing/privatekey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p384/signing/privatekey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p384/signing/privatekey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p384/signing/privatekey/rawrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p384/signing/privatekey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p384/signing/privatekey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p384/signing/privatekey/x963representation)

##### Finding the public key

- [var publicKey: P384.Signing.PublicKey](/documentation/cryptokit/p384/signing/privatekey/publickey)

##### Creating a signature

- [func signature<D>(for: D) throws -> P384.Signing.ECDSASignature](/documentation/cryptokit/p384/signing/privatekey/signature(for:)-8nncg)
- [func signature<D>(for: D) throws -> P384.Signing.ECDSASignature](/documentation/cryptokit/p384/signing/privatekey/signature(for:)-wrsj)
- [P384.Signing.ECDSASignature](/documentation/cryptokit/p384/signing/ecdsasignature)

###### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p384/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p384/signing/ecdsasignature/init(rawrepresentation:))

###### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p384/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p384/signing/ecdsasignature/rawrepresentation)
- [P384.Signing.PublicKey](/documentation/cryptokit/p384/signing/publickey)

##### Creating a key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p384/signing/publickey/init(rawrepresentation:))
- [init<Bytes>(compactRepresentation: Bytes) throws](/documentation/cryptokit/p384/signing/publickey/init(compactrepresentation:))
- [init<Bytes>(compressedRepresentation: Bytes) throws](/documentation/cryptokit/p384/signing/publickey/init(compressedrepresentation:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p384/signing/publickey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p384/signing/publickey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p384/signing/publickey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p384/signing/publickey/rawrepresentation)
- [var compactRepresentation: Data?](/documentation/cryptokit/p384/signing/publickey/compactrepresentation)
- [var compressedRepresentation: Data](/documentation/cryptokit/p384/signing/publickey/compressedrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p384/signing/publickey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p384/signing/publickey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p384/signing/publickey/x963representation)

##### Verifying a signature

- [func isValidSignature<D>(P384.Signing.ECDSASignature, for: D) -> Bool](/documentation/cryptokit/p384/signing/publickey/isvalidsignature(_:for:)-2zf75)
- [func isValidSignature<D>(P384.Signing.ECDSASignature, for: D) -> Bool](/documentation/cryptokit/p384/signing/publickey/isvalidsignature(_:for:)-1hrtv)
- [P384.Signing.ECDSASignature](/documentation/cryptokit/p384/signing/ecdsasignature)

###### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p384/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p384/signing/ecdsasignature/init(rawrepresentation:))

###### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p384/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p384/signing/ecdsasignature/rawrepresentation)

#### Structures

- [P384.Signing.ECDSASignature](/documentation/cryptokit/p384/signing/ecdsasignature)

##### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p384/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p384/signing/ecdsasignature/init(rawrepresentation:))

##### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p384/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p384/signing/ecdsasignature/rawrepresentation)
- [P256](/documentation/cryptokit/p256)

### Performing operations

- [P256.KeyAgreement](/documentation/cryptokit/p256/keyagreement)

#### Using keys

- [P256.KeyAgreement.PrivateKey](/documentation/cryptokit/p256/keyagreement/privatekey)

##### Creating a private key

- [init<Bytes>(rawRepresentation: Bytes) throws](/documentation/cryptokit/p256/keyagreement/privatekey/init(rawrepresentation:))
- [init(compactRepresentable: Bool)](/documentation/cryptokit/p256/keyagreement/privatekey/init(compactrepresentable:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p256/keyagreement/privatekey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p256/keyagreement/privatekey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p256/keyagreement/privatekey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p256/keyagreement/privatekey/rawrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p256/keyagreement/privatekey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p256/keyagreement/privatekey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p256/keyagreement/privatekey/x963representation)

##### Finding the public key

- [var publicKey: P256.KeyAgreement.PublicKey](/documentation/cryptokit/p256/keyagreement/privatekey/publickey)

##### Creating a shared secret

- [func sharedSecretFromKeyAgreement(with: P256.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/p256/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [SharedSecret](/documentation/cryptokit/sharedsecret)

###### Deriving keys

- [func hkdfDerivedSymmetricKey<H, Salt, SI>(using: H.Type, salt: Salt, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/hkdfderivedsymmetrickey(using:salt:sharedinfo:outputbytecount:))
- [func x963DerivedSymmetricKey<H, SI>(using: H.Type, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/x963derivedsymmetrickey(using:sharedinfo:outputbytecount:))

###### Comparing shared secrets

- [static func == <D>(SharedSecret, D) -> Bool](/documentation/cryptokit/sharedsecret/==(_:_:))

##### Default Implementations

- [DiffieHellmanKeyAgreement Implementations](/documentation/cryptokit/p256/keyagreement/privatekey/diffiehellmankeyagreement-implementations)

###### Instance Methods

- [func sharedSecretFromKeyAgreement(with: P256.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/p256/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [HPKEDiffieHellmanPrivateKeyGeneration Implementations](/documentation/cryptokit/p256/keyagreement/privatekey/hpkediffiehellmanprivatekeygeneration-implementations)

###### Initializers

- [init()](/documentation/cryptokit/p256/keyagreement/privatekey/init())
- [P256.KeyAgreement.PublicKey](/documentation/cryptokit/p256/keyagreement/publickey)

##### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p256/keyagreement/publickey/init(rawrepresentation:))
- [init<Bytes>(compactRepresentation: Bytes) throws](/documentation/cryptokit/p256/keyagreement/publickey/init(compactrepresentation:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p256/keyagreement/publickey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p256/keyagreement/publickey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p256/keyagreement/publickey/init(x963representation:))
- [init<Bytes>(compressedRepresentation: Bytes) throws](/documentation/cryptokit/p256/keyagreement/publickey/init(compressedrepresentation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p256/keyagreement/publickey/rawrepresentation)
- [var compactRepresentation: Data?](/documentation/cryptokit/p256/keyagreement/publickey/compactrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p256/keyagreement/publickey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p256/keyagreement/publickey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p256/keyagreement/publickey/x963representation)
- [var compressedRepresentation: Data](/documentation/cryptokit/p256/keyagreement/publickey/compressedrepresentation)

##### Type Aliases

- [P256.KeyAgreement.PublicKey.HPKEEphemeralPrivateKey](/documentation/cryptokit/p256/keyagreement/publickey/hpkeephemeralprivatekey)

##### Default Implementations

- [HPKEDiffieHellmanPublicKey Implementations](/documentation/cryptokit/p256/keyagreement/publickey/hpkediffiehellmanpublickey-implementations)

###### Type Aliases

- [P256.KeyAgreement.PublicKey.EphemeralPrivateKey](/documentation/cryptokit/p256/keyagreement/publickey/ephemeralprivatekey)
- [HPKEPublicKeySerialization Implementations](/documentation/cryptokit/p256/keyagreement/publickey/hpkepublickeyserialization-implementations)

###### Initializers

- [init<D>(D, kem: HPKE.KEM) throws](/documentation/cryptokit/p256/keyagreement/publickey/init(_:kem:))

###### Instance Methods

- [func hpkeRepresentation(kem: HPKE.KEM) throws -> Data](/documentation/cryptokit/p256/keyagreement/publickey/hpkerepresentation(kem:))
- [P256.Signing](/documentation/cryptokit/p256/signing)

#### Using keys

- [P256.Signing.PrivateKey](/documentation/cryptokit/p256/signing/privatekey)

##### Creating a private key

- [init<Bytes>(rawRepresentation: Bytes) throws](/documentation/cryptokit/p256/signing/privatekey/init(rawrepresentation:))
- [init(compactRepresentable: Bool)](/documentation/cryptokit/p256/signing/privatekey/init(compactrepresentable:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p256/signing/privatekey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p256/signing/privatekey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p256/signing/privatekey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p256/signing/privatekey/rawrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p256/signing/privatekey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p256/signing/privatekey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p256/signing/privatekey/x963representation)

##### Finding the public key

- [var publicKey: P256.Signing.PublicKey](/documentation/cryptokit/p256/signing/privatekey/publickey)

##### Creating a signature

- [func signature<D>(for: D) throws -> P256.Signing.ECDSASignature](/documentation/cryptokit/p256/signing/privatekey/signature(for:)-5h94p)
- [func signature<D>(for: D) throws -> P256.Signing.ECDSASignature](/documentation/cryptokit/p256/signing/privatekey/signature(for:)-1iyzc)
- [P256.Signing.ECDSASignature](/documentation/cryptokit/p256/signing/ecdsasignature)

###### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p256/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p256/signing/ecdsasignature/init(rawrepresentation:))

###### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p256/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p256/signing/ecdsasignature/rawrepresentation)
- [P256.Signing.PublicKey](/documentation/cryptokit/p256/signing/publickey)

##### Creating a key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p256/signing/publickey/init(rawrepresentation:))
- [init<Bytes>(compactRepresentation: Bytes) throws](/documentation/cryptokit/p256/signing/publickey/init(compactrepresentation:))
- [init<Bytes>(compressedRepresentation: Bytes) throws](/documentation/cryptokit/p256/signing/publickey/init(compressedrepresentation:))
- [init<Bytes>(derRepresentation: Bytes) throws](/documentation/cryptokit/p256/signing/publickey/init(derrepresentation:))
- [init(pemRepresentation: String) throws](/documentation/cryptokit/p256/signing/publickey/init(pemrepresentation:))
- [init<Bytes>(x963Representation: Bytes) throws](/documentation/cryptokit/p256/signing/publickey/init(x963representation:))

##### Representing the key

- [var rawRepresentation: Data](/documentation/cryptokit/p256/signing/publickey/rawrepresentation)
- [var compactRepresentation: Data?](/documentation/cryptokit/p256/signing/publickey/compactrepresentation)
- [var compressedRepresentation: Data](/documentation/cryptokit/p256/signing/publickey/compressedrepresentation)
- [var derRepresentation: Data](/documentation/cryptokit/p256/signing/publickey/derrepresentation)
- [var pemRepresentation: String](/documentation/cryptokit/p256/signing/publickey/pemrepresentation)
- [var x963Representation: Data](/documentation/cryptokit/p256/signing/publickey/x963representation)

##### Verifying a signature

- [func isValidSignature<D>(P256.Signing.ECDSASignature, for: D) -> Bool](/documentation/cryptokit/p256/signing/publickey/isvalidsignature(_:for:)-3da2m)
- [func isValidSignature<D>(P256.Signing.ECDSASignature, for: D) -> Bool](/documentation/cryptokit/p256/signing/publickey/isvalidsignature(_:for:)-2rsb5)
- [P256.Signing.ECDSASignature](/documentation/cryptokit/p256/signing/ecdsasignature)

###### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p256/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p256/signing/ecdsasignature/init(rawrepresentation:))

###### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p256/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p256/signing/ecdsasignature/rawrepresentation)

#### Structures

- [P256.Signing.ECDSASignature](/documentation/cryptokit/p256/signing/ecdsasignature)

##### Creating a signature

- [init<D>(derRepresentation: D) throws](/documentation/cryptokit/p256/signing/ecdsasignature/init(derrepresentation:))
- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/p256/signing/ecdsasignature/init(rawrepresentation:))

##### Representing the signature

- [var derRepresentation: Data](/documentation/cryptokit/p256/signing/ecdsasignature/derrepresentation)
- [var rawRepresentation: Data](/documentation/cryptokit/p256/signing/ecdsasignature/rawrepresentation)
- [SharedSecret](/documentation/cryptokit/sharedsecret)

### Deriving keys

- [func hkdfDerivedSymmetricKey<H, Salt, SI>(using: H.Type, salt: Salt, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/hkdfderivedsymmetrickey(using:salt:sharedinfo:outputbytecount:))
- [func x963DerivedSymmetricKey<H, SI>(using: H.Type, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/x963derivedsymmetrickey(using:sharedinfo:outputbytecount:))

### Comparing shared secrets

- [static func == <D>(SharedSecret, D) -> Bool](/documentation/cryptokit/sharedsecret/==(_:_:))
- [SecureEnclave](/documentation/cryptokit/secureenclave)

### Checking availability

- [static var isAvailable: Bool](/documentation/cryptokit/secureenclave/isavailable)

### Using the secure enclave

- [SecureEnclave.P256](/documentation/cryptokit/secureenclave/p256)

#### Performing operations

- [SecureEnclave.P256.KeyAgreement](/documentation/cryptokit/secureenclave/p256/keyagreement)

##### Using keys

- [SecureEnclave.P256.KeyAgreement.PrivateKey](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey)

###### Creating a private key

- [init(dataRepresentation: Data, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/init(datarepresentation:authenticationcontext:))
- [init(compactRepresentable: Bool, accessControl: SecAccessControl, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/init(compactrepresentable:accesscontrol:authenticationcontext:))

###### Representing the key

- [let dataRepresentation: Data](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/datarepresentation)

###### Finding the public key

- [let publicKey: P256.KeyAgreement.PublicKey](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/publickey)

###### Creating a shared secret

- [func sharedSecretFromKeyAgreement(with: P256.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [SharedSecret](/documentation/cryptokit/sharedsecret)

###### Deriving keys

- [func hkdfDerivedSymmetricKey<H, Salt, SI>(using: H.Type, salt: Salt, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/hkdfderivedsymmetrickey(using:salt:sharedinfo:outputbytecount:))
- [func x963DerivedSymmetricKey<H, SI>(using: H.Type, sharedInfo: SI, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/sharedsecret/x963derivedsymmetrickey(using:sharedinfo:outputbytecount:))

###### Comparing shared secrets

- [static func == <D>(SharedSecret, D) -> Bool](/documentation/cryptokit/sharedsecret/==(_:_:))

###### Initializers

- [init(compactRepresentable: Bool, accessControl: SecAccessControl) throws](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/init(compactrepresentable:accesscontrol:))
- [init(dataRepresentation: Data) throws](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/init(datarepresentation:))

###### Default Implementations

- [DiffieHellmanKeyAgreement Implementations](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/diffiehellmankeyagreement-implementations)

###### Instance Methods

- [func sharedSecretFromKeyAgreement(with: P256.KeyAgreement.PublicKey) throws -> SharedSecret](/documentation/cryptokit/secureenclave/p256/keyagreement/privatekey/sharedsecretfromkeyagreement(with:))
- [SecureEnclave.P256.Signing](/documentation/cryptokit/secureenclave/p256/signing)

##### Using keys

- [SecureEnclave.P256.Signing.PrivateKey](/documentation/cryptokit/secureenclave/p256/signing/privatekey)

###### Creating a private key

- [init(dataRepresentation: Data, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/p256/signing/privatekey/init(datarepresentation:authenticationcontext:))
- [init(compactRepresentable: Bool, accessControl: SecAccessControl, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/p256/signing/privatekey/init(compactrepresentable:accesscontrol:authenticationcontext:))

###### Representing the key

- [let dataRepresentation: Data](/documentation/cryptokit/secureenclave/p256/signing/privatekey/datarepresentation)

###### Getting the public key

- [let publicKey: P256.Signing.PublicKey](/documentation/cryptokit/secureenclave/p256/signing/privatekey/publickey)

###### Generating a signature

- [func signature<D>(for: D) throws -> P256.Signing.ECDSASignature](/documentation/cryptokit/secureenclave/p256/signing/privatekey/signature(for:)-3xogs)
- [func signature<D>(for: D) throws -> P256.Signing.ECDSASignature](/documentation/cryptokit/secureenclave/p256/signing/privatekey/signature(for:)-76j0u)

###### Initializers

- [init(compactRepresentable: Bool, accessControl: SecAccessControl) throws](/documentation/cryptokit/secureenclave/p256/signing/privatekey/init(compactrepresentable:accesscontrol:))
- [init(dataRepresentation: Data) throws](/documentation/cryptokit/secureenclave/p256/signing/privatekey/init(datarepresentation:))
- [SecureEnclave.MLKEM1024](/documentation/cryptokit/secureenclave/mlkem1024)

#### Keys

- [SecureEnclave.MLKEM1024.PrivateKey](/documentation/cryptokit/secureenclave/mlkem1024/privatekey)

##### Creating a private key

- [static func generate() throws -> SecureEnclave.MLKEM1024.PrivateKey](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/generate())
- [init(accessControl: SecAccessControl, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/init(accesscontrol:authenticationcontext:))
- [init<D>(dataRepresentation: D, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/init(datarepresentation:authenticationcontext:))

##### Accessing a key’s properties

- [let dataRepresentation: Data](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/datarepresentation)
- [let publicKey: MLKEM1024.PublicKey](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/publickey)

##### Decapsulating shared secrets

- [func decapsulate<D>(D) throws -> SymmetricKey](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/decapsulate(_:))

##### Initializers

- [init(accessControl: SecAccessControl) throws](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/init(accesscontrol:))
- [init<D>(dataRepresentation: D) throws](/documentation/cryptokit/secureenclave/mlkem1024/privatekey/init(datarepresentation:))
- [SecureEnclave.MLKEM768](/documentation/cryptokit/secureenclave/mlkem768)

#### Keys

- [SecureEnclave.MLKEM768.PrivateKey](/documentation/cryptokit/secureenclave/mlkem768/privatekey)

##### Creating a private key

- [static func generate() throws -> SecureEnclave.MLKEM768.PrivateKey](/documentation/cryptokit/secureenclave/mlkem768/privatekey/generate())
- [init(accessControl: SecAccessControl, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mlkem768/privatekey/init(accesscontrol:authenticationcontext:))
- [init<D>(dataRepresentation: D, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mlkem768/privatekey/init(datarepresentation:authenticationcontext:))

##### Accessing the key’s properties

- [let dataRepresentation: Data](/documentation/cryptokit/secureenclave/mlkem768/privatekey/datarepresentation)
- [let publicKey: MLKEM768.PublicKey](/documentation/cryptokit/secureenclave/mlkem768/privatekey/publickey)

##### Decapsulating shared secrets

- [func decapsulate<D>(D) throws -> SymmetricKey](/documentation/cryptokit/secureenclave/mlkem768/privatekey/decapsulate(_:))

##### Initializers

- [init(accessControl: SecAccessControl) throws](/documentation/cryptokit/secureenclave/mlkem768/privatekey/init(accesscontrol:))
- [init<D>(dataRepresentation: D) throws](/documentation/cryptokit/secureenclave/mlkem768/privatekey/init(datarepresentation:))

### Enumerations

- [SecureEnclave.MLDSA65](/documentation/cryptokit/secureenclave/mldsa65)

#### Structures

- [SecureEnclave.MLDSA65.PrivateKey](/documentation/cryptokit/secureenclave/mldsa65/privatekey)

##### Initializers

- [init(accessControl: SecAccessControl) throws](/documentation/cryptokit/secureenclave/mldsa65/privatekey/init(accesscontrol:))
- [init(accessControl: SecAccessControl, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mldsa65/privatekey/init(accesscontrol:authenticationcontext:))
- [init<D>(dataRepresentation: D) throws](/documentation/cryptokit/secureenclave/mldsa65/privatekey/init(datarepresentation:))
- [init<D>(dataRepresentation: D, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mldsa65/privatekey/init(datarepresentation:authenticationcontext:))

##### Instance Properties

- [let dataRepresentation: Data](/documentation/cryptokit/secureenclave/mldsa65/privatekey/datarepresentation)
- [let publicKey: MLDSA65.PublicKey](/documentation/cryptokit/secureenclave/mldsa65/privatekey/publickey)

##### Instance Methods

- [func signature<D>(for: D) throws -> Data](/documentation/cryptokit/secureenclave/mldsa65/privatekey/signature(for:))
- [func signature<D, C>(for: D, context: C) throws -> Data](/documentation/cryptokit/secureenclave/mldsa65/privatekey/signature(for:context:))
- [SecureEnclave.MLDSA87](/documentation/cryptokit/secureenclave/mldsa87)

#### Structures

- [SecureEnclave.MLDSA87.PrivateKey](/documentation/cryptokit/secureenclave/mldsa87/privatekey)

##### Initializers

- [init(accessControl: SecAccessControl) throws](/documentation/cryptokit/secureenclave/mldsa87/privatekey/init(accesscontrol:))
- [init(accessControl: SecAccessControl, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mldsa87/privatekey/init(accesscontrol:authenticationcontext:))
- [init<D>(dataRepresentation: D) throws](/documentation/cryptokit/secureenclave/mldsa87/privatekey/init(datarepresentation:))
- [init<D>(dataRepresentation: D, authenticationContext: LAContext?) throws](/documentation/cryptokit/secureenclave/mldsa87/privatekey/init(datarepresentation:authenticationcontext:))

##### Instance Properties

- [let dataRepresentation: Data](/documentation/cryptokit/secureenclave/mldsa87/privatekey/datarepresentation)
- [let publicKey: MLDSA87.PublicKey](/documentation/cryptokit/secureenclave/mldsa87/privatekey/publickey)

##### Instance Methods

- [func signature<D>(for: D) throws -> Data](/documentation/cryptokit/secureenclave/mldsa87/privatekey/signature(for:))
- [func signature<D, C>(for: D, context: C) throws -> Data](/documentation/cryptokit/secureenclave/mldsa87/privatekey/signature(for:context:))
- [HPKE](/documentation/cryptokit/hpke)

### Sending and receiving messages

- [HPKE.Sender](/documentation/cryptokit/hpke/sender)

#### Initializers

- [init<PK>(recipientKey: PK, ciphersuite: HPKE.Ciphersuite, info: Data) throws](/documentation/cryptokit/hpke/sender/init(recipientkey:ciphersuite:info:)-56p88)
- [init<PK>(recipientKey: PK, ciphersuite: HPKE.Ciphersuite, info: Data) throws](/documentation/cryptokit/hpke/sender/init(recipientkey:ciphersuite:info:)-swk5)
- [init<SK>(recipientKey: SK.PublicKey, ciphersuite: HPKE.Ciphersuite, info: Data, authenticatedBy: SK) throws](/documentation/cryptokit/hpke/sender/init(recipientkey:ciphersuite:info:authenticatedby:))
- [init<SK>(recipientKey: SK.PublicKey, ciphersuite: HPKE.Ciphersuite, info: Data, authenticatedBy: SK, presharedKey: SymmetricKey, presharedKeyIdentifier: Data) throws](/documentation/cryptokit/hpke/sender/init(recipientkey:ciphersuite:info:authenticatedby:presharedkey:presharedkeyidentifier:))
- [init<PK>(recipientKey: PK, ciphersuite: HPKE.Ciphersuite, info: Data, presharedKey: SymmetricKey, presharedKeyIdentifier: Data) throws](/documentation/cryptokit/hpke/sender/init(recipientkey:ciphersuite:info:presharedkey:presharedkeyidentifier:))

#### Instance Properties

- [let encapsulatedKey: Data](/documentation/cryptokit/hpke/sender/encapsulatedkey)

#### Instance Methods

- [func exportSecret<Context>(context: Context, outputByteCount: Int) throws -> SymmetricKey](/documentation/cryptokit/hpke/sender/exportsecret(context:outputbytecount:))
- [func seal<M>(M) throws -> Data](/documentation/cryptokit/hpke/sender/seal(_:))
- [func seal<M, AD>(M, authenticating: AD) throws -> Data](/documentation/cryptokit/hpke/sender/seal(_:authenticating:))
- [HPKE.Recipient](/documentation/cryptokit/hpke/recipient)

#### Initializers

- [init<SK>(privateKey: SK, ciphersuite: HPKE.Ciphersuite, info: Data, encapsulatedKey: Data) throws](/documentation/cryptokit/hpke/recipient/init(privatekey:ciphersuite:info:encapsulatedkey:)-6jqhf)
- [init<SK>(privateKey: SK, ciphersuite: HPKE.Ciphersuite, info: Data, encapsulatedKey: Data) throws](/documentation/cryptokit/hpke/recipient/init(privatekey:ciphersuite:info:encapsulatedkey:)-7v86b)
- [init<SK>(privateKey: SK, ciphersuite: HPKE.Ciphersuite, info: Data, encapsulatedKey: Data, authenticatedBy: SK.PublicKey) throws](/documentation/cryptokit/hpke/recipient/init(privatekey:ciphersuite:info:encapsulatedkey:authenticatedby:))
- [init<SK>(privateKey: SK, ciphersuite: HPKE.Ciphersuite, info: Data, encapsulatedKey: Data, authenticatedBy: SK.PublicKey, presharedKey: SymmetricKey, presharedKeyIdentifier: Data) throws](/documentation/cryptokit/hpke/recipient/init(privatekey:ciphersuite:info:encapsulatedkey:authenticatedby:presharedkey:presharedkeyidentifier:))
- [init<SK>(privateKey: SK, ciphersuite: HPKE.Ciphersuite, info: Data, encapsulatedKey: Data, presharedKey: SymmetricKey, presharedKeyIdentifier: Data) throws](/documentation/cryptokit/hpke/recipient/init(privatekey:ciphersuite:info:encapsulatedkey:presharedkey:presharedkeyidentifier:))

#### Instance Methods

- [func exportSecret<Context>(context: Context, outputByteCount: Int) throws -> SymmetricKey](/documentation/cryptokit/hpke/recipient/exportsecret(context:outputbytecount:))
- [func open<C>(C) throws -> Data](/documentation/cryptokit/hpke/recipient/open(_:))
- [func open<C, AD>(C, authenticating: AD) throws -> Data](/documentation/cryptokit/hpke/recipient/open(_:authenticating:))

### Choosing cryptographic algorithms

- [HPKE.Ciphersuite](/documentation/cryptokit/hpke/ciphersuite)

#### Using post-quantum cipher suites

- [static let XWingMLKEM768X25519_SHA256_AES_GCM_256: HPKE.Ciphersuite](/documentation/cryptokit/hpke/ciphersuite/xwingmlkem768x25519_sha256_aes_gcm_256)

#### Using elliptic curve cipher suites

- [static let Curve25519_SHA256_ChachaPoly: HPKE.Ciphersuite](/documentation/cryptokit/hpke/ciphersuite/curve25519_sha256_chachapoly)
- [static let P256_SHA256_AES_GCM_256: HPKE.Ciphersuite](/documentation/cryptokit/hpke/ciphersuite/p256_sha256_aes_gcm_256)
- [static let P384_SHA384_AES_GCM_256: HPKE.Ciphersuite](/documentation/cryptokit/hpke/ciphersuite/p384_sha384_aes_gcm_256)
- [static let P521_SHA512_AES_GCM_256: HPKE.Ciphersuite](/documentation/cryptokit/hpke/ciphersuite/p521_sha512_aes_gcm_256)

#### Creating a cipher suite

- [init(kem: HPKE.KEM, kdf: HPKE.KDF, aead: HPKE.AEAD)](/documentation/cryptokit/hpke/ciphersuite/init(kem:kdf:aead:))

#### Inspecting a cipher suite

- [let aead: HPKE.AEAD](/documentation/cryptokit/hpke/ciphersuite/aead)
- [let kdf: HPKE.KDF](/documentation/cryptokit/hpke/ciphersuite/kdf)
- [let kem: HPKE.KEM](/documentation/cryptokit/hpke/ciphersuite/kem)
- [HPKE.AEAD](/documentation/cryptokit/hpke/aead)

#### Enumeration Cases

- [case AES_GCM_128](/documentation/cryptokit/hpke/aead/aes_gcm_128)
- [case AES_GCM_256](/documentation/cryptokit/hpke/aead/aes_gcm_256)
- [case chaChaPoly](/documentation/cryptokit/hpke/aead/chachapoly)
- [case exportOnly](/documentation/cryptokit/hpke/aead/exportonly)
- [HPKE.KDF](/documentation/cryptokit/hpke/kdf)

#### Enumeration Cases

- [case HKDF_SHA256](/documentation/cryptokit/hpke/kdf/hkdf_sha256)
- [case HKDF_SHA384](/documentation/cryptokit/hpke/kdf/hkdf_sha384)
- [case HKDF_SHA512](/documentation/cryptokit/hpke/kdf/hkdf_sha512)
- [HPKE.KEM](/documentation/cryptokit/hpke/kem)

#### Elliptic curve key encapsulation mechanisms

- [case Curve25519_HKDF_SHA256](/documentation/cryptokit/hpke/kem/curve25519_hkdf_sha256)
- [case P256_HKDF_SHA256](/documentation/cryptokit/hpke/kem/p256_hkdf_sha256)
- [case P384_HKDF_SHA384](/documentation/cryptokit/hpke/kem/p384_hkdf_sha384)
- [case P521_HKDF_SHA512](/documentation/cryptokit/hpke/kem/p521_hkdf_sha512)

#### Enumeration Cases

- [case XWingMLKEM768X25519](/documentation/cryptokit/hpke/kem/xwingmlkem768x25519)
- [HPKE.DHKEM](/documentation/cryptokit/hpke/dhkem)

### Handling errors

- [HPKE.Errors](/documentation/cryptokit/hpke/errors)

#### Enumeration Cases

- [case ciphertextTooShort](/documentation/cryptokit/hpke/errors/ciphertexttooshort)
- [case expectedPSK](/documentation/cryptokit/hpke/errors/expectedpsk)
- [case exportOnlyMode](/documentation/cryptokit/hpke/errors/exportonlymode)
- [case inconsistentCiphersuiteAndKey](/documentation/cryptokit/hpke/errors/inconsistentciphersuiteandkey)
- [case inconsistentPSKInputs](/documentation/cryptokit/hpke/errors/inconsistentpskinputs)
- [case inconsistentParameters](/documentation/cryptokit/hpke/errors/inconsistentparameters)
- [case outOfRangeSequenceNumber](/documentation/cryptokit/hpke/errors/outofrangesequencenumber)
- [case unexpectedPSK](/documentation/cryptokit/hpke/errors/unexpectedpsk)

## Key derivation functions

- [HKDF](/documentation/cryptokit/hkdf)

### Deriving a key

- [static func deriveKey(inputKeyMaterial: SymmetricKey, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/hkdf/derivekey(inputkeymaterial:outputbytecount:))
- [static func deriveKey<Info>(inputKeyMaterial: SymmetricKey, info: Info, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/hkdf/derivekey(inputkeymaterial:info:outputbytecount:))
- [static func deriveKey<Salt>(inputKeyMaterial: SymmetricKey, salt: Salt, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/hkdf/derivekey(inputkeymaterial:salt:outputbytecount:))
- [static func deriveKey<Salt, Info>(inputKeyMaterial: SymmetricKey, salt: Salt, info: Info, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/hkdf/derivekey(inputkeymaterial:salt:info:outputbytecount:))

### Controlling key derivation

- [static func extract<Salt>(inputKeyMaterial: SymmetricKey, salt: Salt?) -> HashedAuthenticationCode<H>](/documentation/cryptokit/hkdf/extract(inputkeymaterial:salt:))
- [static func expand<PRK, Info>(pseudoRandomKey: PRK, info: Info?, outputByteCount: Int) -> SymmetricKey](/documentation/cryptokit/hkdf/expand(pseudorandomkey:info:outputbytecount:))

## Key encapsulation mechanisms (KEM)

- [KEM](/documentation/cryptokit/kem)

### Defining encapsulation outputs

- [KEM.EncapsulationResult](/documentation/cryptokit/kem/encapsulationresult)

#### Initializers

- [init(sharedSecret: SymmetricKey, encapsulated: Data)](/documentation/cryptokit/kem/encapsulationresult/init(sharedsecret:encapsulated:))

#### Instance Properties

- [let encapsulated: Data](/documentation/cryptokit/kem/encapsulationresult/encapsulated)
- [let sharedSecret: SymmetricKey](/documentation/cryptokit/kem/encapsulationresult/sharedsecret)

### Handling errors

- [KEM.Errors](/documentation/cryptokit/kem/errors)

#### Enumeration Cases

- [case invalidSeed](/documentation/cryptokit/kem/errors/invalidseed)
- [case publicKeyMismatchDuringInitialization](/documentation/cryptokit/kem/errors/publickeymismatchduringinitialization)
- [MLKEM768](/documentation/cryptokit/mlkem768)

### Keys

- [MLKEM768.PrivateKey](/documentation/cryptokit/mlkem768/privatekey)

#### Creating a private key

- [static func generate() throws -> MLKEM768.PrivateKey](/documentation/cryptokit/mlkem768/privatekey/generate())
- [init() throws](/documentation/cryptokit/mlkem768/privatekey/init())
- [init<D>(integrityCheckedRepresentation: D) throws](/documentation/cryptokit/mlkem768/privatekey/init(integritycheckedrepresentation:))
- [init<D>(seedRepresentation: D, publicKey: MLKEM768.PublicKey?) throws](/documentation/cryptokit/mlkem768/privatekey/init(seedrepresentation:publickey:))

#### Inspecting a private key’s properties

- [var integrityCheckedRepresentation: Data](/documentation/cryptokit/mlkem768/privatekey/integritycheckedrepresentation)
- [var publicKey: MLKEM768.PublicKey](/documentation/cryptokit/mlkem768/privatekey/publickey)
- [var seedRepresentation: Data](/documentation/cryptokit/mlkem768/privatekey/seedrepresentation)

#### Decapsulating shared secrets

- [func decapsulate<D>(D) throws -> SymmetricKey](/documentation/cryptokit/mlkem768/privatekey/decapsulate(_:))
- [MLKEM768.PublicKey](/documentation/cryptokit/mlkem768/publickey)

#### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/mlkem768/publickey/init(rawrepresentation:))

#### Accessing a key’s raw representation

- [var rawRepresentation: Data](/documentation/cryptokit/mlkem768/publickey/rawrepresentation)

#### Encapsulating a shared secret

- [func encapsulate() throws -> KEM.EncapsulationResult](/documentation/cryptokit/mlkem768/publickey/encapsulate())
- [MLKEM1024](/documentation/cryptokit/mlkem1024)

### Keys

- [MLKEM1024.PrivateKey](/documentation/cryptokit/mlkem1024/privatekey)

#### Creating a private key

- [static func generate() throws -> MLKEM1024.PrivateKey](/documentation/cryptokit/mlkem1024/privatekey/generate())
- [init() throws](/documentation/cryptokit/mlkem1024/privatekey/init())
- [init<D>(integrityCheckedRepresentation: D) throws](/documentation/cryptokit/mlkem1024/privatekey/init(integritycheckedrepresentation:))
- [init<D>(seedRepresentation: D, publicKey: MLKEM1024.PublicKey?) throws](/documentation/cryptokit/mlkem1024/privatekey/init(seedrepresentation:publickey:))

#### Inspecting a private key’s properties

- [var integrityCheckedRepresentation: Data](/documentation/cryptokit/mlkem1024/privatekey/integritycheckedrepresentation)
- [var publicKey: MLKEM1024.PublicKey](/documentation/cryptokit/mlkem1024/privatekey/publickey)
- [var seedRepresentation: Data](/documentation/cryptokit/mlkem1024/privatekey/seedrepresentation)

#### Decapsulating shared secrets

- [func decapsulate<D>(D) throws -> SymmetricKey](/documentation/cryptokit/mlkem1024/privatekey/decapsulate(_:))
- [MLKEM1024.PublicKey](/documentation/cryptokit/mlkem1024/publickey)

#### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/mlkem1024/publickey/init(rawrepresentation:))

#### Accessing a key’s raw representation

- [var rawRepresentation: Data](/documentation/cryptokit/mlkem1024/publickey/rawrepresentation)

#### Encapsulating a shared secret

- [func encapsulate() throws -> KEM.EncapsulationResult](/documentation/cryptokit/mlkem1024/publickey/encapsulate())
- [XWingMLKEM768X25519](/documentation/cryptokit/xwingmlkem768x25519)

### Keys

- [XWingMLKEM768X25519.PrivateKey](/documentation/cryptokit/xwingmlkem768x25519/privatekey)

#### Creating a private key

- [init<D>(integrityCheckedRepresentation: D) throws](/documentation/cryptokit/xwingmlkem768x25519/privatekey/init(integritycheckedrepresentation:))
- [init<D>(seedRepresentation: D, publicKey: XWingMLKEM768X25519.PublicKey?) throws](/documentation/cryptokit/xwingmlkem768x25519/privatekey/init(seedrepresentation:publickey:))

#### Inspecting a private key’s properties

- [var integrityCheckedRepresentation: Data](/documentation/cryptokit/xwingmlkem768x25519/privatekey/integritycheckedrepresentation)
- [var seedRepresentation: Data](/documentation/cryptokit/xwingmlkem768x25519/privatekey/seedrepresentation)
- [XWingMLKEM768X25519.PublicKey](/documentation/cryptokit/xwingmlkem768x25519/publickey)

#### Accessing a key’s raw representation

- [var rawRepresentation: Data](/documentation/cryptokit/xwingmlkem768x25519/publickey/rawrepresentation)

#### Accessing the corresponding private key type

- [XWingMLKEM768X25519.PublicKey.HPKEEphemeralPrivateKey](/documentation/cryptokit/xwingmlkem768x25519/publickey/hpkeephemeralprivatekey)

#### Initializers

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/xwingmlkem768x25519/publickey/init(rawrepresentation:))

#### Default Implementations

- [HPKEKEMPublicKey Implementations](/documentation/cryptokit/xwingmlkem768x25519/publickey/hpkekempublickey-implementations)

##### Type Aliases

- [XWingMLKEM768X25519.PublicKey.EphemeralPrivateKey](/documentation/cryptokit/xwingmlkem768x25519/publickey/ephemeralprivatekey)
- [HPKEPublicKeySerialization Implementations](/documentation/cryptokit/xwingmlkem768x25519/publickey/hpkepublickeyserialization-implementations)

##### Initializers

- [init<D>(D, kem: HPKE.KEM) throws](/documentation/cryptokit/xwingmlkem768x25519/publickey/init(_:kem:))

##### Instance Methods

- [func hpkeRepresentation(kem: HPKE.KEM) throws -> Data](/documentation/cryptokit/xwingmlkem768x25519/publickey/hpkerepresentation(kem:))

## KEM keys

- [KEMPrivateKey](/documentation/cryptokit/kemprivatekey)

### Associated Types

- [PublicKey](/documentation/cryptokit/kemprivatekey/publickey-swift.associatedtype)

### Instance Properties

- [var publicKey: Self.PublicKey](/documentation/cryptokit/kemprivatekey/publickey-swift.property)

### Instance Methods

- [func decapsulate(Data) throws -> SymmetricKey](/documentation/cryptokit/kemprivatekey/decapsulate(_:))

### Type Methods

- [static func generate() throws -> Self](/documentation/cryptokit/kemprivatekey/generate())
- [KEMPublicKey](/documentation/cryptokit/kempublickey)

### Instance Methods

- [func encapsulate() throws -> KEM.EncapsulationResult](/documentation/cryptokit/kempublickey/encapsulate())

## Errors

- [CryptoKitError](/documentation/cryptokit/cryptokiterror)

### Reporting errors

- [case incorrectKeySize](/documentation/cryptokit/cryptokiterror/incorrectkeysize)
- [case invalidParameter](/documentation/cryptokit/cryptokiterror/invalidparameter)
- [case incorrectParameterSize](/documentation/cryptokit/cryptokiterror/incorrectparametersize)
- [case underlyingCoreCryptoError(error: Int32)](/documentation/cryptokit/cryptokiterror/underlyingcorecryptoerror(error:))
- [case authenticationFailure](/documentation/cryptokit/cryptokiterror/authenticationfailure)
- [case wrapFailure](/documentation/cryptokit/cryptokiterror/wrapfailure)
- [case unwrapFailure](/documentation/cryptokit/cryptokiterror/unwrapfailure)
- [CryptoKitASN1Error](/documentation/cryptokit/cryptokitasn1error)

### Reporting errors

- [case invalidASN1IntegerEncoding](/documentation/cryptokit/cryptokitasn1error/invalidasn1integerencoding)
- [case invalidASN1Object](/documentation/cryptokit/cryptokitasn1error/invalidasn1object)
- [case invalidFieldIdentifier](/documentation/cryptokit/cryptokitasn1error/invalidfieldidentifier)
- [case invalidObjectIdentifier](/documentation/cryptokit/cryptokitasn1error/invalidobjectidentifier)
- [case invalidPEMDocument](/documentation/cryptokit/cryptokitasn1error/invalidpemdocument)
- [case truncatedASN1Field](/documentation/cryptokit/cryptokitasn1error/truncatedasn1field)
- [case unexpectedFieldType](/documentation/cryptokit/cryptokitasn1error/unexpectedfieldtype)
- [case unsupportedFieldLength](/documentation/cryptokit/cryptokitasn1error/unsupportedfieldlength)

## Legacy algorithms

- [Insecure](/documentation/cryptokit/insecure)

### Hashes

- [Insecure.MD5](/documentation/cryptokit/insecure/md5)

#### Specifying the output type

- [Insecure.MD5.Digest](/documentation/cryptokit/insecure/md5/digest)
- [Insecure.MD5Digest](/documentation/cryptokit/insecure/md5digest)

##### Inspecting the digest length

- [static var byteCount: Int](/documentation/cryptokit/insecure/md5digest/bytecount)

##### Describing a digest

- [var description: String](/documentation/cryptokit/insecure/md5digest/description)

##### Hashing a digest

- [func hash(into: inout Hasher)](/documentation/cryptokit/insecure/md5digest/hash(into:))

#### Reporting the hash length

- [static let byteCount: Int](/documentation/cryptokit/insecure/md5/bytecount)

#### Computing a hash iteratively

- [init()](/documentation/cryptokit/insecure/md5/init())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/insecure/md5/update(bufferpointer:))
- [func finalize() -> Insecure.MD5.Digest](/documentation/cryptokit/insecure/md5/finalize())

#### Reporting hash function information

- [static let blockByteCount: Int](/documentation/cryptokit/insecure/md5/blockbytecount)
- [Insecure.SHA1](/documentation/cryptokit/insecure/sha1)

#### Specifying the output type

- [Insecure.SHA1.Digest](/documentation/cryptokit/insecure/sha1/digest)
- [Insecure.SHA1Digest](/documentation/cryptokit/insecure/sha1digest)

##### Inspecting the digest length

- [static var byteCount: Int](/documentation/cryptokit/insecure/sha1digest/bytecount)

##### Describing a digest

- [var description: String](/documentation/cryptokit/insecure/sha1digest/description)

##### Hasing a digest

- [func hash(into: inout Hasher)](/documentation/cryptokit/insecure/sha1digest/hash(into:))

#### Reporting the hash length

- [static let byteCount: Int](/documentation/cryptokit/insecure/sha1/bytecount)

#### Computing a hash iteratively

- [init()](/documentation/cryptokit/insecure/sha1/init())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/insecure/sha1/update(bufferpointer:))
- [func finalize() -> Insecure.SHA1.Digest](/documentation/cryptokit/insecure/sha1/finalize())

#### Reporting hash function information

- [static let blockByteCount: Int](/documentation/cryptokit/insecure/sha1/blockbytecount)

### Structures

- [Insecure.MD5Digest](/documentation/cryptokit/insecure/md5digest)

#### Inspecting the digest length

- [static var byteCount: Int](/documentation/cryptokit/insecure/md5digest/bytecount)

#### Describing a digest

- [var description: String](/documentation/cryptokit/insecure/md5digest/description)

#### Hashing a digest

- [func hash(into: inout Hasher)](/documentation/cryptokit/insecure/md5digest/hash(into:))
- [Insecure.SHA1Digest](/documentation/cryptokit/insecure/sha1digest)

#### Inspecting the digest length

- [static var byteCount: Int](/documentation/cryptokit/insecure/sha1digest/bytecount)

#### Describing a digest

- [var description: String](/documentation/cryptokit/insecure/sha1digest/description)

#### Hasing a digest

- [func hash(into: inout Hasher)](/documentation/cryptokit/insecure/sha1digest/hash(into:))

## Protocols

- [DiffieHellmanKeyAgreement](/documentation/cryptokit/diffiehellmankeyagreement)

### Associated Types

- [PublicKey](/documentation/cryptokit/diffiehellmankeyagreement/publickey-swift.associatedtype)

### Instance Properties

- [var publicKey: Self.PublicKey](/documentation/cryptokit/diffiehellmankeyagreement/publickey-swift.property)

### Instance Methods

- [func sharedSecretFromKeyAgreement(with: Self.PublicKey) throws -> SharedSecret](/documentation/cryptokit/diffiehellmankeyagreement/sharedsecretfromkeyagreement(with:))
- [HPKEDiffieHellmanPrivateKey](/documentation/cryptokit/hpkediffiehellmanprivatekey)
- [HPKEDiffieHellmanPrivateKeyGeneration](/documentation/cryptokit/hpkediffiehellmanprivatekeygeneration)

### Initializers

- [init()](/documentation/cryptokit/hpkediffiehellmanprivatekeygeneration/init())
- [HPKEDiffieHellmanPublicKey](/documentation/cryptokit/hpkediffiehellmanpublickey)

### Associated Types

- [EphemeralPrivateKey](/documentation/cryptokit/hpkediffiehellmanpublickey/ephemeralprivatekey)
- [HPKEKEMPrivateKey](/documentation/cryptokit/hpkekemprivatekey)
- [HPKEKEMPrivateKeyGeneration](/documentation/cryptokit/hpkekemprivatekeygeneration)

### Initializers

- [init() throws](/documentation/cryptokit/hpkekemprivatekeygeneration/init())
- [HPKEKEMPublicKey](/documentation/cryptokit/hpkekempublickey)

### Associated Types

- [EphemeralPrivateKey](/documentation/cryptokit/hpkekempublickey/ephemeralprivatekey)
- [HPKEPublicKeySerialization](/documentation/cryptokit/hpkepublickeyserialization)

### Initializers

- [init<D>(D, kem: HPKE.KEM) throws](/documentation/cryptokit/hpkepublickeyserialization/init(_:kem:))

### Instance Methods

- [func hpkeRepresentation(kem: HPKE.KEM) throws -> Data](/documentation/cryptokit/hpkepublickeyserialization/hpkerepresentation(kem:))

## Structures

- [CorecryptoCurveType](/documentation/cryptokit/corecryptocurvetype)
- [SHA3_256](/documentation/cryptokit/sha3_256)

### Initializers

- [init()](/documentation/cryptokit/sha3_256/init())

### Instance Methods

- [func finalize() -> SHA3_256.Digest](/documentation/cryptokit/sha3_256/finalize())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/sha3_256/update(bufferpointer:))

### Type Aliases

- [SHA3_256.Digest](/documentation/cryptokit/sha3_256/digest)

### Type Properties

- [static let blockByteCount: Int](/documentation/cryptokit/sha3_256/blockbytecount)
- [static let byteCount: Int](/documentation/cryptokit/sha3_256/bytecount)
- [SHA3_256Digest](/documentation/cryptokit/sha3_256digest)

### Instance Properties

- [var description: String](/documentation/cryptokit/sha3_256digest/description)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/cryptokit/sha3_256digest/hash(into:))

### Type Properties

- [static var byteCount: Int](/documentation/cryptokit/sha3_256digest/bytecount)
- [SHA3_384](/documentation/cryptokit/sha3_384)

### Initializers

- [init()](/documentation/cryptokit/sha3_384/init())

### Instance Methods

- [func finalize() -> SHA3_384.Digest](/documentation/cryptokit/sha3_384/finalize())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/sha3_384/update(bufferpointer:))

### Type Aliases

- [SHA3_384.Digest](/documentation/cryptokit/sha3_384/digest)

### Type Properties

- [static let blockByteCount: Int](/documentation/cryptokit/sha3_384/blockbytecount)
- [static let byteCount: Int](/documentation/cryptokit/sha3_384/bytecount)
- [SHA3_384Digest](/documentation/cryptokit/sha3_384digest)

### Instance Properties

- [var description: String](/documentation/cryptokit/sha3_384digest/description)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/cryptokit/sha3_384digest/hash(into:))

### Type Properties

- [static var byteCount: Int](/documentation/cryptokit/sha3_384digest/bytecount)
- [SHA3_512](/documentation/cryptokit/sha3_512)

### Initializers

- [init()](/documentation/cryptokit/sha3_512/init())

### Instance Methods

- [func finalize() -> SHA3_512.Digest](/documentation/cryptokit/sha3_512/finalize())
- [func update(bufferPointer: UnsafeRawBufferPointer)](/documentation/cryptokit/sha3_512/update(bufferpointer:))

### Type Aliases

- [SHA3_512.Digest](/documentation/cryptokit/sha3_512/digest)

### Type Properties

- [static let blockByteCount: Int](/documentation/cryptokit/sha3_512/blockbytecount)
- [static let byteCount: Int](/documentation/cryptokit/sha3_512/bytecount)
- [SHA3_512Digest](/documentation/cryptokit/sha3_512digest)

### Instance Properties

- [var description: String](/documentation/cryptokit/sha3_512digest/description)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/cryptokit/sha3_512digest/hash(into:))

### Type Properties

- [static var byteCount: Int](/documentation/cryptokit/sha3_512digest/bytecount)

## Type Aliases

- [CryptoKitMetaError](/documentation/cryptokit/cryptokitmetaerror)
- [SHA2_256](/documentation/cryptokit/sha2_256)
- [SHA2_384](/documentation/cryptokit/sha2_384)
- [SHA2_512](/documentation/cryptokit/sha2_512)

## Enumerations

- [MLDSA65](/documentation/cryptokit/mldsa65)

### Keys

- [MLDSA65.PrivateKey](/documentation/cryptokit/mldsa65/privatekey)

#### Creating a private key

- [init() throws](/documentation/cryptokit/mldsa65/privatekey/init())
- [init<D>(integrityCheckedRepresentation: D) throws](/documentation/cryptokit/mldsa65/privatekey/init(integritycheckedrepresentation:))
- [init<D>(seedRepresentation: D, publicKey: MLDSA65.PublicKey?) throws](/documentation/cryptokit/mldsa65/privatekey/init(seedrepresentation:publickey:))

#### Inspecting a private key’s properties

- [var integrityCheckedRepresentation: Data](/documentation/cryptokit/mldsa65/privatekey/integritycheckedrepresentation)
- [var publicKey: MLDSA65.PublicKey](/documentation/cryptokit/mldsa65/privatekey/publickey)
- [var seedRepresentation: Data](/documentation/cryptokit/mldsa65/privatekey/seedrepresentation)

#### Signing data

- [func signature<D>(for: D) throws -> Data](/documentation/cryptokit/mldsa65/privatekey/signature(for:))
- [func signature<D, C>(for: D, context: C) throws -> Data](/documentation/cryptokit/mldsa65/privatekey/signature(for:context:))
- [MLDSA65.PublicKey](/documentation/cryptokit/mldsa65/publickey)

#### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/mldsa65/publickey/init(rawrepresentation:))

#### Getting the raw representation

- [var rawRepresentation: Data](/documentation/cryptokit/mldsa65/publickey/rawrepresentation)

#### Instance Methods

- [func isValidSignature<S, D>(S, for: D) -> Bool](/documentation/cryptokit/mldsa65/publickey/isvalidsignature(_:for:))
- [func isValidSignature<S, D, C>(S, for: D, context: C) -> Bool](/documentation/cryptokit/mldsa65/publickey/isvalidsignature(_:for:context:))
- [MLDSA87](/documentation/cryptokit/mldsa87)

### Keys

- [MLDSA87.PrivateKey](/documentation/cryptokit/mldsa87/privatekey)

#### Creating a private key

- [init() throws](/documentation/cryptokit/mldsa87/privatekey/init())
- [init<D>(integrityCheckedRepresentation: D) throws](/documentation/cryptokit/mldsa87/privatekey/init(integritycheckedrepresentation:))
- [init<D>(seedRepresentation: D, publicKey: MLDSA87.PublicKey?) throws](/documentation/cryptokit/mldsa87/privatekey/init(seedrepresentation:publickey:))

#### Inspecting a private key’s properties

- [var integrityCheckedRepresentation: Data](/documentation/cryptokit/mldsa87/privatekey/integritycheckedrepresentation)
- [var publicKey: MLDSA87.PublicKey](/documentation/cryptokit/mldsa87/privatekey/publickey)
- [var seedRepresentation: Data](/documentation/cryptokit/mldsa87/privatekey/seedrepresentation)

#### Signing data

- [func signature<D>(for: D) throws -> Data](/documentation/cryptokit/mldsa87/privatekey/signature(for:))
- [func signature<D, C>(for: D, context: C) throws -> Data](/documentation/cryptokit/mldsa87/privatekey/signature(for:context:))
- [MLDSA87.PublicKey](/documentation/cryptokit/mldsa87/publickey)

#### Creating a public key

- [init<D>(rawRepresentation: D) throws](/documentation/cryptokit/mldsa87/publickey/init(rawrepresentation:))

#### Getting the raw representation

- [var rawRepresentation: Data](/documentation/cryptokit/mldsa87/publickey/rawrepresentation)

#### Instance Methods

- [func isValidSignature<S, D>(S, for: D) -> Bool](/documentation/cryptokit/mldsa87/publickey/isvalidsignature(_:for:))
- [func isValidSignature<S, D, C>(S, for: D, context: C) -> Bool](/documentation/cryptokit/mldsa87/publickey/isvalidsignature(_:for:context:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
