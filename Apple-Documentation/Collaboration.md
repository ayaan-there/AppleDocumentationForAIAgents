# Collaboration Documentation

Source: https://sosumi.ai/documentation/collaboration

---
title: Collaboration
source: https://developer.apple.com/documentation/collaboration
timestamp: 2026-02-13T18:54:57.982Z
---

## Classes

- [CBGroupIdentity](/documentation/collaboration/cbgroupidentity)

### Finding Group Identities

- [init?(posixGID: gid_t, authority: CBIdentityAuthority)](/documentation/collaboration/cbgroupidentity/init(posixgid:authority:))

### Group Identity Attributes

- [var posixGID: gid_t](/documentation/collaboration/cbgroupidentity/posixgid)

### Instance Properties

- [var memberIdentities: [CBIdentity]](/documentation/collaboration/cbgroupidentity/memberidentities)
- [CBIdentity](/documentation/collaboration/cbidentity)

### Finding Identities

- [init?(name: String, authority: CBIdentityAuthority)](/documentation/collaboration/cbidentity/init(name:authority:))
- [init?(persistentReference: Data)](/documentation/collaboration/cbidentity/init(persistentreference:))
- [init?(uuidString: String, authority: CBIdentityAuthority)](/documentation/collaboration/cbidentity/init(uuidstring:authority:))

### Getting Identity Attributes

- [var aliases: [String]](/documentation/collaboration/cbidentity/aliases)
- [var authority: CBIdentityAuthority](/documentation/collaboration/cbidentity/authority)
- [var emailAddress: String?](/documentation/collaboration/cbidentity/emailaddress)
- [var fullName: String](/documentation/collaboration/cbidentity/fullname)
- [var image: NSImage?](/documentation/collaboration/cbidentity/image)
- [var isHidden: Bool](/documentation/collaboration/cbidentity/ishidden)
- [func isMember(ofGroup: CBGroupIdentity) -> Bool](/documentation/collaboration/cbidentity/ismember(ofgroup:))
- [var posixName: String](/documentation/collaboration/cbidentity/posixname)
- [var uuidString: String](/documentation/collaboration/cbidentity/uuidstring)

### Storing Identities

- [var persistentReference: Data?](/documentation/collaboration/cbidentity/persistentreference)

### Initializers

- [init?(uniqueIdentifier: UUID, authority: CBIdentityAuthority)](/documentation/collaboration/cbidentity/init(uniqueidentifier:authority:))

### Instance Properties

- [var uniqueIdentifier: UUID](/documentation/collaboration/cbidentity/uniqueidentifier)
- [CBIdentityAuthority](/documentation/collaboration/cbidentityauthority)

### Accessing Identity Authorities

- [var localizedName: String](/documentation/collaboration/cbidentityauthority/localizedname)
- [class func local() -> CBIdentityAuthority](/documentation/collaboration/cbidentityauthority/local())
- [class func managed() -> CBIdentityAuthority](/documentation/collaboration/cbidentityauthority/managed())
- [class func `default`() -> CBIdentityAuthority](/documentation/collaboration/cbidentityauthority/default())
- [CBIdentityPicker](/documentation/collaboration/cbidentitypicker)

### Running an Identity Picker

- [func runModal(for: NSWindow, modalDelegate: Any?, didEnd: Selector?, contextInfo: UnsafeMutableRawPointer?)](/documentation/collaboration/cbidentitypicker/runmodal(for:modaldelegate:didend:contextinfo:))
- [func runModal(for: NSWindow, completionHandler: ((NSApplication.ModalResponse) -> Void)?)](/documentation/collaboration/cbidentitypicker/runmodal(for:completionhandler:))
- [func runModal() -> Int](/documentation/collaboration/cbidentitypicker/runmodal())

### Retrieving Identities

- [var identities: [CBIdentity]](/documentation/collaboration/cbidentitypicker/identities)

### Setting and Getting Properties

- [var title: String?](/documentation/collaboration/cbidentitypicker/title)
- [var allowsMultipleSelection: Bool](/documentation/collaboration/cbidentitypicker/allowsmultipleselection)
- [CBUserIdentity](/documentation/collaboration/cbuseridentity)

### Password Authentication

- [func authenticate(withPassword: String) -> Bool](/documentation/collaboration/cbuseridentity/authenticate(withpassword:))
- [var certificate: SecCertificate?](/documentation/collaboration/cbuseridentity/certificate)
- [var isEnabled: Bool](/documentation/collaboration/cbuseridentity/isenabled)

### Using UIDs

- [var posixUID: uid_t](/documentation/collaboration/cbuseridentity/posixuid)
- [init?(posixUID: uid_t, authority: CBIdentityAuthority)](/documentation/collaboration/cbuseridentity/init(posixuid:authority:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
