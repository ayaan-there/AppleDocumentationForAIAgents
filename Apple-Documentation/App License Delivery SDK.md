# App License Delivery SDK Documentation

Source: https://sosumi.ai/documentation/applicensedeliverysdk

---
title: App License Delivery SDK
source: https://developer.apple.com/documentation/applicensedeliverysdk
timestamp: 2026-02-13T18:53:11.229Z
---

## Essentials

- [Configuring your app licensing environment](/documentation/applicensedeliverysdk/configuring-the-app-licensing-environment)

## App licensing

- [Licensing alternative distribution apps](/documentation/applicensedeliverysdk/licensing-alternative-distribution-apps)
- [Renewing and revoking app licenses](/documentation/applicensedeliverysdk/renewing-and-revoking-app-licenses)
- [ALDAppKey](/documentation/applicensedeliverysdk/aldappkey)

### Initializers

- [init(appleItemID: UInt64, appKeyBlob: [UInt8]) throws](/documentation/applicensedeliverysdk/aldappkey/init(appleitemid:appkeyblob:))
- [ALDLicenseAttribute](/documentation/applicensedeliverysdk/aldlicenseattribute)

### Initializers

- [init(licenseID: UInt64)](/documentation/applicensedeliverysdk/aldlicenseattribute/init(licenseid:))

### Instance Properties

- [var duration: UInt64](/documentation/applicensedeliverysdk/aldlicenseattribute/duration)
- [var issuedTime: UInt64](/documentation/applicensedeliverysdk/aldlicenseattribute/issuedtime)

### Instance Methods

- [func addAppKey(ALDAppKey) throws](/documentation/applicensedeliverysdk/aldlicenseattribute/addappkey(_:))
- [func revokeAppleItemID(UInt64) throws](/documentation/applicensedeliverysdk/aldlicenseattribute/revokeappleitemid(_:))
- [ALDProvider](/documentation/applicensedeliverysdk/aldprovider)

### Initializers

- [init(encryptionCert: [UInt8], signingCert: [UInt8], PASK: [UInt8], signingKey: [UInt8]?)](/documentation/applicensedeliverysdk/aldprovider/init(encryptioncert:signingcert:pask:signingkey:))

### Instance Methods

- [func createSession(clientRequest: [UInt8]) throws -> ALDSession](/documentation/applicensedeliverysdk/aldprovider/createsession(clientrequest:))
- [ALDSession](/documentation/applicensedeliverysdk/aldsession)

### Initializers

- [init(request: [UInt8], PASK: [UInt8], encryptionCert: [UInt8], signingCert: [UInt8], signingKey: [UInt8]?) throws](/documentation/applicensedeliverysdk/aldsession/init(request:pask:encryptioncert:signingcert:signingkey:))
- [init(signingCert: [UInt8], signingKey: [UInt8]?, PASK: [UInt8]) throws](/documentation/applicensedeliverysdk/aldsession/init(signingcert:signingkey:pask:))

### Instance Properties

- [var requestAction: ALDLicenseAction](/documentation/applicensedeliverysdk/aldsession/requestaction)
- [var requestDeviceID: [UInt8]](/documentation/applicensedeliverysdk/aldsession/requestdeviceid)
- [var requestID: UInt64](/documentation/applicensedeliverysdk/aldsession/requestid)
- [var requestTime: UInt64](/documentation/applicensedeliverysdk/aldsession/requesttime)
- [var requestVersion: UInt32](/documentation/applicensedeliverysdk/aldsession/requestversion)
- [var requestedAppleItemIDList: [UInt64]](/documentation/applicensedeliverysdk/aldsession/requestedappleitemidlist)
- [var requestedLicenseIDList: [UInt64]](/documentation/applicensedeliverysdk/aldsession/requestedlicenseidlist)
- [var sessionType: ALDSessionType](/documentation/applicensedeliverysdk/aldsession/sessiontype)

### Instance Methods

- [func finalizeLicenseResponse(licenseResponse: [UInt8], signature: [UInt8]?) throws -> [UInt8]](/documentation/applicensedeliverysdk/aldsession/finalizelicenseresponse(licenseresponse:signature:))
- [func generateLicense(attr: ALDLicenseAttribute) throws](/documentation/applicensedeliverysdk/aldsession/generatelicense(attr:))
- [func generateLicenseResponse() throws -> [UInt8]](/documentation/applicensedeliverysdk/aldsession/generatelicenseresponse())
- [func generateStaticLicense(licenseID: UInt64, appKey: ALDAppKey) throws](/documentation/applicensedeliverysdk/aldsession/generatestaticlicense(licenseid:appkey:))

### Enumerations

- [ALDSession.ALDLicenseAction](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction)

#### Enumeration Cases

- [case create](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/create)
- [case generateStatic](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/generatestatic)
- [case renew](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/renew)
- [case unknown](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/unknown)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/init(rawvalue:))

#### Default Implementations

- [Equatable Implementations](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/!=(_:_:))
- [RawRepresentable Implementations](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/rawrepresentable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/applicensedeliverysdk/aldsession/aldlicenseaction/hash(into:))
- [ALDSession.ALDSessionType](/documentation/applicensedeliverysdk/aldsession/aldsessiontype)

#### Enumeration Cases

- [case normalSession](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/normalsession)
- [case staticSession](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/staticsession)
- [case unknown](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/unknown)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/init(rawvalue:))

#### Default Implementations

- [Equatable Implementations](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/!=(_:_:))
- [RawRepresentable Implementations](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/rawrepresentable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/applicensedeliverysdk/aldsession/aldsessiontype/hash(into:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
