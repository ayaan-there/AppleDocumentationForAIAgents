# LightweightCodeRequirements Documentation

Source: https://sosumi.ai/documentation/lightweightcoderequirements

---
title: LightweightCodeRequirements
source: https://developer.apple.com/documentation/lightweightcoderequirements
timestamp: 2026-02-13T18:58:40.715Z
---

## Checking code requirements for running processes

- [func SecTaskValidateForRequirement(task: SecTask, requirement: ProcessCodeRequirement) throws -> Bool](/documentation/lightweightcoderequirements/sectaskvalidateforrequirement(task:requirement:))
- [ProcessCodeRequirement](/documentation/lightweightcoderequirements/processcoderequirement)

### Initializers

- [init(OnDiskCodeRequirement) throws](/documentation/lightweightcoderequirements/processcoderequirement/init(_:)-1va02)
- [init(LaunchCodeRequirement) throws](/documentation/lightweightcoderequirements/processcoderequirement/init(_:)-4gkz2)
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/processcoderequirement/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/processcoderequirement/encode(to:))

### Type Methods

- [static func allOf(requirement: () -> [any ProcessConstraint]) throws -> ProcessCodeRequirement](/documentation/lightweightcoderequirements/processcoderequirement/allof(requirement:))
- [static func anyOf(requirement: () -> [any ProcessConstraint]) throws -> ProcessCodeRequirement](/documentation/lightweightcoderequirements/processcoderequirement/anyof(requirement:))
- [func allOf(requirement: () -> [any ProcessConstraint]) -> any ProcessConstraint](/documentation/lightweightcoderequirements/allof(requirement:)-4k3ay)
- [func anyOf(requirement: () -> [any ProcessConstraint]) -> any ProcessConstraint](/documentation/lightweightcoderequirements/anyof(requirement:)-vwhn)
- [ProcessConstraint](/documentation/lightweightcoderequirements/processconstraint)
- [ProcessCodeSigningFlags](/documentation/lightweightcoderequirements/processcodesigningflags)

### Structures

- [ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset)

#### Type Properties

- [static let isAdhocSigned: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/isadhocsigned)
- [static let isCertificateExpirationEnforced: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/iscertificateexpirationenforced)
- [static let isCodeSignatureRequiredForAllExecutableCode: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/iscodesignaturerequiredforallexecutablecode)
- [static let isDebuggable: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/isdebuggable)
- [static let isDebugged: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/isdebugged)
- [static let isDynamicLinkerPolicyHardened: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/isdynamiclinkerpolicyhardened)
- [static let isDynamicallyValid: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/isdynamicallyvalid)
- [static let isHardenedRuntimeEnforced: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/ishardenedruntimeenforced)
- [static let isLibraryValidationRequired: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/islibraryvalidationrequired)
- [static let isPlatformSigned: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/isplatformsigned)
- [static let isSigned: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/issigned)
- [static let isSignedByLinker: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/issignedbylinker)
- [static let signalsBusErrorOnCodeSigningFailure: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/signalsbuserroroncodesigningfailure)
- [static let terminatesOnCodeSigningFailure: ProcessCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/processcodesigningflags/valueset/terminatesoncodesigningfailure)

### Type Aliases

- [ProcessCodeSigningFlags.DataType](/documentation/lightweightcoderequirements/processcodesigningflags/datatype)
- [ProcessCodeSigningFlags.OutType](/documentation/lightweightcoderequirements/processcodesigningflags/outtype)

### Type Methods

- [static func isSuperset(of: ProcessCodeSigningFlags.DataType) -> ProcessCodeSigningFlags.OutType](/documentation/lightweightcoderequirements/processcodesigningflags/issuperset(of:))
- [ProcessConstraintBuilder](/documentation/lightweightcoderequirements/processconstraintbuilder)

### Type Methods

- [static func buildBlock([any ProcessConstraint]...) -> [any ProcessConstraint]](/documentation/lightweightcoderequirements/processconstraintbuilder/buildblock(_:))
- [static func buildEither(first: [any ProcessConstraint]) -> [any ProcessConstraint]](/documentation/lightweightcoderequirements/processconstraintbuilder/buildeither(first:))
- [static func buildEither(second: [any ProcessConstraint]) -> [any ProcessConstraint]](/documentation/lightweightcoderequirements/processconstraintbuilder/buildeither(second:))
- [static func buildExpression([any ProcessConstraint]) -> [any ProcessConstraint]](/documentation/lightweightcoderequirements/processconstraintbuilder/buildexpression(_:)-6zrmh)
- [static func buildExpression(any ProcessConstraint) -> [any ProcessConstraint]](/documentation/lightweightcoderequirements/processconstraintbuilder/buildexpression(_:)-7rglu)
- [static func buildOptional([any ProcessConstraint]?) -> [any ProcessConstraint]](/documentation/lightweightcoderequirements/processconstraintbuilder/buildoptional(_:))
- [TeamIdentifierMatchesCurrentProcess](/documentation/lightweightcoderequirements/teamidentifiermatchescurrentprocess)

### Initializers

- [init()](/documentation/lightweightcoderequirements/teamidentifiermatchescurrentprocess/init())
- [init(Bool)](/documentation/lightweightcoderequirements/teamidentifiermatchescurrentprocess/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/teamidentifiermatchescurrentprocess/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/teamidentifiermatchescurrentprocess/encode(to:))

## Checking code requirements for launching processes

- [func SecCodeCheckValidityWithProcessRequirement(code: SecCode, flags: SecCSFlags, requirement: ProcessCodeRequirement) -> ValidationResult](/documentation/lightweightcoderequirements/seccodecheckvaliditywithprocessrequirement(code:flags:requirement:))
- [var launchRequirement: LaunchCodeRequirement?](/documentation/foundation/process/launchrequirement)
- [LaunchCodeRequirement](/documentation/lightweightcoderequirements/launchcoderequirement)

### Initializers

- [init(ProcessCodeRequirement) throws](/documentation/lightweightcoderequirements/launchcoderequirement/init(_:)-5fh0u)
- [init(OnDiskCodeRequirement) throws](/documentation/lightweightcoderequirements/launchcoderequirement/init(_:)-6hixy)
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/launchcoderequirement/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/launchcoderequirement/encode(to:))

### Type Methods

- [static func allOf(requirement: () -> [any LaunchConstraint]) throws -> LaunchCodeRequirement](/documentation/lightweightcoderequirements/launchcoderequirement/allof(requirement:))
- [static func anyOf(requirement: () -> [any LaunchConstraint]) throws -> LaunchCodeRequirement](/documentation/lightweightcoderequirements/launchcoderequirement/anyof(requirement:))
- [func allOf(requirement: () -> [any LaunchConstraint]) -> any LaunchConstraint](/documentation/lightweightcoderequirements/allof(requirement:)-4gf5f)
- [func anyOf(requirement: () -> [any LaunchConstraint]) -> any LaunchConstraint](/documentation/lightweightcoderequirements/anyof(requirement:)-6nicx)
- [LaunchConstraint](/documentation/lightweightcoderequirements/launchconstraint)
- [LaunchConstraintBuilder](/documentation/lightweightcoderequirements/launchconstraintbuilder)

### Type Methods

- [static func buildBlock([any LaunchConstraint]...) -> [any LaunchConstraint]](/documentation/lightweightcoderequirements/launchconstraintbuilder/buildblock(_:))
- [static func buildEither(first: [any LaunchConstraint]) -> [any LaunchConstraint]](/documentation/lightweightcoderequirements/launchconstraintbuilder/buildeither(first:))
- [static func buildEither(second: [any LaunchConstraint]) -> [any LaunchConstraint]](/documentation/lightweightcoderequirements/launchconstraintbuilder/buildeither(second:))
- [static func buildExpression(any LaunchConstraint) -> [any LaunchConstraint]](/documentation/lightweightcoderequirements/launchconstraintbuilder/buildexpression(_:)-5tl61)
- [static func buildExpression([any LaunchConstraint]) -> [any LaunchConstraint]](/documentation/lightweightcoderequirements/launchconstraintbuilder/buildexpression(_:)-6l0k6)
- [static func buildOptional([any LaunchConstraint]?) -> [any LaunchConstraint]](/documentation/lightweightcoderequirements/launchconstraintbuilder/buildoptional(_:))

## Checking code requirements for code files on disk

- [func SecStaticCodeCheckValidityWithOnDiskRequirement(code: SecStaticCode, flags: SecCSFlags, requirement: OnDiskCodeRequirement) -> ValidationResult](/documentation/lightweightcoderequirements/secstaticcodecheckvaliditywithondiskrequirement(code:flags:requirement:))
- [func SecCodeCheckValidityWithOnDiskRequirement(code: SecCode, flags: SecCSFlags, requirement: OnDiskCodeRequirement) -> ValidationResult](/documentation/lightweightcoderequirements/seccodecheckvaliditywithondiskrequirement(code:flags:requirement:))
- [ValidationResult](/documentation/lightweightcoderequirements/validationresult)

### Instance Properties

- [let failureReason: OSStatus](/documentation/lightweightcoderequirements/validationresult/failurereason)
- [let requirementMatched: Bool](/documentation/lightweightcoderequirements/validationresult/requirementmatched)
- [let signatureIsValid: Bool](/documentation/lightweightcoderequirements/validationresult/signatureisvalid)
- [OnDiskCodeRequirement](/documentation/lightweightcoderequirements/ondiskcoderequirement)

### Initializers

- [init(LaunchCodeRequirement) throws](/documentation/lightweightcoderequirements/ondiskcoderequirement/init(_:)-2lfey)
- [init(ProcessCodeRequirement) throws](/documentation/lightweightcoderequirements/ondiskcoderequirement/init(_:)-9imtm)
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/ondiskcoderequirement/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/ondiskcoderequirement/encode(to:))

### Type Methods

- [static func allOf(requirement: () -> [any OnDiskConstraint]) throws -> OnDiskCodeRequirement](/documentation/lightweightcoderequirements/ondiskcoderequirement/allof(requirement:))
- [static func anyOf(requirement: () -> [any OnDiskConstraint]) throws -> OnDiskCodeRequirement](/documentation/lightweightcoderequirements/ondiskcoderequirement/anyof(requirement:))
- [func allOf(requirement: () -> [any OnDiskConstraint]) -> any OnDiskConstraint](/documentation/lightweightcoderequirements/allof(requirement:)-2ocwl)
- [func anyOf(requirement: () -> [any OnDiskConstraint]) -> any OnDiskConstraint](/documentation/lightweightcoderequirements/anyof(requirement:)-71pff)
- [OnDiskConstraint](/documentation/lightweightcoderequirements/ondiskconstraint)
- [OnDiskCodeSigningFlags](/documentation/lightweightcoderequirements/ondiskcodesigningflags)

### Structures

- [OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset)

#### Type Properties

- [static let isAdhocSigned: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/isadhocsigned)
- [static let isCertificateExpirationEnforced: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/iscertificateexpirationenforced)
- [static let isCodeSignatureRequiredForAllExecutableCode: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/iscodesignaturerequiredforallexecutablecode)
- [static let isDynamicLinkerPolicyHardened: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/isdynamiclinkerpolicyhardened)
- [static let isHardenedRuntimeEnforced: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/ishardenedruntimeenforced)
- [static let isLibraryValidationRequired: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/islibraryvalidationrequired)
- [static let isSignedByLinker: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/issignedbylinker)
- [static let signalsBusErrorOnCodeSigningFailure: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/signalsbuserroroncodesigningfailure)
- [static let terminatesOnCodeSigningFailure: OnDiskCodeSigningFlags.ValueSet](/documentation/lightweightcoderequirements/ondiskcodesigningflags/valueset/terminatesoncodesigningfailure)

### Type Aliases

- [OnDiskCodeSigningFlags.DataType](/documentation/lightweightcoderequirements/ondiskcodesigningflags/datatype)
- [OnDiskCodeSigningFlags.OutType](/documentation/lightweightcoderequirements/ondiskcodesigningflags/outtype)

### Type Methods

- [static func isSuperset(of: OnDiskCodeSigningFlags.DataType) -> OnDiskCodeSigningFlags.OutType](/documentation/lightweightcoderequirements/ondiskcodesigningflags/issuperset(of:))
- [OnDiskConstraintBuilder](/documentation/lightweightcoderequirements/ondiskconstraintbuilder)

### Type Methods

- [static func buildBlock([any OnDiskConstraint]...) -> [any OnDiskConstraint]](/documentation/lightweightcoderequirements/ondiskconstraintbuilder/buildblock(_:))
- [static func buildEither(first: [any OnDiskConstraint]) -> [any OnDiskConstraint]](/documentation/lightweightcoderequirements/ondiskconstraintbuilder/buildeither(first:))
- [static func buildEither(second: [any OnDiskConstraint]) -> [any OnDiskConstraint]](/documentation/lightweightcoderequirements/ondiskconstraintbuilder/buildeither(second:))
- [static func buildExpression(any OnDiskConstraint) -> [any OnDiskConstraint]](/documentation/lightweightcoderequirements/ondiskconstraintbuilder/buildexpression(_:)-1qla)
- [static func buildExpression([any OnDiskConstraint]) -> [any OnDiskConstraint]](/documentation/lightweightcoderequirements/ondiskconstraintbuilder/buildexpression(_:)-3uyy8)
- [static func buildOptional([any OnDiskConstraint]?) -> [any OnDiskConstraint]](/documentation/lightweightcoderequirements/ondiskconstraintbuilder/buildoptional(_:))

## Testing properties of executable code

- [CodeDirectoryHash](/documentation/lightweightcoderequirements/codedirectoryhash)

### Initializers

- [init(Data)](/documentation/lightweightcoderequirements/codedirectoryhash/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/codedirectoryhash/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/codedirectoryhash/encode(to:))

### Type Aliases

- [CodeDirectoryHash.DataType](/documentation/lightweightcoderequirements/codedirectoryhash/datatype)
- [CodeDirectoryHash.OutType](/documentation/lightweightcoderequirements/codedirectoryhash/outtype)

### Type Methods

- [static func `in`([CodeDirectoryHash.DataType]) -> CodeDirectoryHash.OutType](/documentation/lightweightcoderequirements/codedirectoryhash/in(_:)-1kiuo)
- [static func `in`(CodeDirectoryHash.DataType...) -> CodeDirectoryHash.OutType](/documentation/lightweightcoderequirements/codedirectoryhash/in(_:)-912dv)
- [EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery)

### Initializers

- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/entitlementsquery/init(from:))

### Instance Methods

- [func elementAtIndex(Int64) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/elementatindex(_:))
- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/entitlementsquery/encode(to:))
- [func key(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/key(_:)-swift.method)
- [func keyPrefix(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/keyprefix(_:)-swift.method)
- [func match(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/match(_:)-5cqvy)
- [func match(Bool) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/match(_:)-5cw98)
- [func match(Int64) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/match(_:)-6msza)
- [func matchPrefix(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/matchprefix(_:))
- [func matchPrefixSingle(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/matchprefixsingle(_:))
- [func matchSingle(Int64) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/matchsingle(_:)-49kv7)
- [func matchSingle(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/matchsingle(_:)-8ggh1)
- [func matchType(EntitlementsQuery.DataType) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/matchtype(_:))

### Type Methods

- [static func key(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/key(_:)-swift.type.method)
- [static func keyPrefix(String) -> EntitlementsQuery](/documentation/lightweightcoderequirements/entitlementsquery/keyprefix(_:)-swift.type.method)

### Enumerations

- [EntitlementsQuery.DataType](/documentation/lightweightcoderequirements/entitlementsquery/datatype)

#### Enumeration Cases

- [case array](/documentation/lightweightcoderequirements/entitlementsquery/datatype/array)
- [case boolean](/documentation/lightweightcoderequirements/entitlementsquery/datatype/boolean)
- [case dictionary](/documentation/lightweightcoderequirements/entitlementsquery/datatype/dictionary)
- [case integer](/documentation/lightweightcoderequirements/entitlementsquery/datatype/integer)
- [case string](/documentation/lightweightcoderequirements/entitlementsquery/datatype/string)
- [InfoPlistHash](/documentation/lightweightcoderequirements/infoplisthash)

### Initializers

- [init(Data)](/documentation/lightweightcoderequirements/infoplisthash/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/infoplisthash/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/infoplisthash/encode(to:))

### Type Aliases

- [InfoPlistHash.DataType](/documentation/lightweightcoderequirements/infoplisthash/datatype)
- [InfoPlistHash.OutType](/documentation/lightweightcoderequirements/infoplisthash/outtype)

### Type Methods

- [static func `in`(InfoPlistHash.DataType...) -> InfoPlistHash.OutType](/documentation/lightweightcoderequirements/infoplisthash/in(_:)-18amo)
- [static func `in`([InfoPlistHash.DataType]) -> InfoPlistHash.OutType](/documentation/lightweightcoderequirements/infoplisthash/in(_:)-1rwy8)
- [IsInitProcess](/documentation/lightweightcoderequirements/isinitprocess)

### Initializers

- [init()](/documentation/lightweightcoderequirements/isinitprocess/init())
- [init(Bool)](/documentation/lightweightcoderequirements/isinitprocess/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/isinitprocess/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/isinitprocess/encode(to:))
- [IsMainBinary](/documentation/lightweightcoderequirements/ismainbinary)

### Initializers

- [init()](/documentation/lightweightcoderequirements/ismainbinary/init())
- [init(Bool)](/documentation/lightweightcoderequirements/ismainbinary/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/ismainbinary/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/ismainbinary/encode(to:))
- [IsSIPProtected](/documentation/lightweightcoderequirements/issipprotected)

### Initializers

- [init()](/documentation/lightweightcoderequirements/issipprotected/init())
- [init(Bool)](/documentation/lightweightcoderequirements/issipprotected/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/issipprotected/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/issipprotected/encode(to:))
- [PlatformType](/documentation/lightweightcoderequirements/platformtype)

### Structures

- [PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value)

#### Initializers

- [init?(rawValue: Int64)](/documentation/lightweightcoderequirements/platformtype/value/init(rawvalue:))

#### Instance Properties

- [let rawValue: Int64](/documentation/lightweightcoderequirements/platformtype/value/rawvalue)

#### Type Properties

- [static let driverKit: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/driverkit)
- [static let iOS: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/ios)
- [static let iOSSimulator: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/iossimulator)
- [static let macCatalyst: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/maccatalyst)
- [static let macOS: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/macos)
- [static let tvOS: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/tvos)
- [static let tvOSSimulator: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/tvossimulator)
- [static let visionOS: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/visionos)
- [static let visionOSSimulator: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/visionossimulator)
- [static let watchOS: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/watchos)
- [static let watchOSSimulator: PlatformType.Value](/documentation/lightweightcoderequirements/platformtype/value/watchossimulator)

### Initializers

- [init(PlatformType.Value)](/documentation/lightweightcoderequirements/platformtype/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/platformtype/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/platformtype/encode(to:))

### Type Aliases

- [PlatformType.DataType](/documentation/lightweightcoderequirements/platformtype/datatype)
- [PlatformType.OutType](/documentation/lightweightcoderequirements/platformtype/outtype)

### Type Methods

- [static func `in`(PlatformType.DataType...) -> PlatformType.OutType](/documentation/lightweightcoderequirements/platformtype/in(_:)-1ndmu)
- [static func `in`([PlatformType.DataType]) -> PlatformType.OutType](/documentation/lightweightcoderequirements/platformtype/in(_:)-44pc3)
- [SigningIdentifier](/documentation/lightweightcoderequirements/signingidentifier)

### Initializers

- [init(String)](/documentation/lightweightcoderequirements/signingidentifier/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/signingidentifier/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/signingidentifier/encode(to:))

### Type Aliases

- [SigningIdentifier.DataType](/documentation/lightweightcoderequirements/signingidentifier/datatype)
- [SigningIdentifier.OutType](/documentation/lightweightcoderequirements/signingidentifier/outtype)

### Type Methods

- [static func `in`(SigningIdentifier.DataType...) -> SigningIdentifier.OutType](/documentation/lightweightcoderequirements/signingidentifier/in(_:)-57h8m)
- [static func `in`([SigningIdentifier.DataType]) -> SigningIdentifier.OutType](/documentation/lightweightcoderequirements/signingidentifier/in(_:)-57qq8)
- [TeamIdentifier](/documentation/lightweightcoderequirements/teamidentifier)

### Initializers

- [init(String)](/documentation/lightweightcoderequirements/teamidentifier/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/teamidentifier/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/teamidentifier/encode(to:))

### Type Aliases

- [TeamIdentifier.DataType](/documentation/lightweightcoderequirements/teamidentifier/datatype)
- [TeamIdentifier.OutType](/documentation/lightweightcoderequirements/teamidentifier/outtype)

### Type Methods

- [static func `in`([TeamIdentifier.DataType]) -> TeamIdentifier.OutType](/documentation/lightweightcoderequirements/teamidentifier/in(_:)-1z4vz)
- [static func `in`(TeamIdentifier.DataType...) -> TeamIdentifier.OutType](/documentation/lightweightcoderequirements/teamidentifier/in(_:)-9x3l9)
- [ValidationCategory](/documentation/lightweightcoderequirements/validationcategory)

### Structures

- [ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value)

#### Initializers

- [init?(rawValue: Int64)](/documentation/lightweightcoderequirements/validationcategory/value/init(rawvalue:))

#### Instance Properties

- [let rawValue: Int64](/documentation/lightweightcoderequirements/validationcategory/value/rawvalue)

#### Type Properties

- [static let appStore: ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value/appstore)
- [static let developerID: ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value/developerid)
- [static let development: ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value/development)
- [static let enterprise: ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value/enterprise)
- [static let none: ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value/none)
- [static let platform: ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value/platform)
- [static let testflight: ValidationCategory.Value](/documentation/lightweightcoderequirements/validationcategory/value/testflight)

### Initializers

- [init(ValidationCategory.Value)](/documentation/lightweightcoderequirements/validationcategory/init(_:))
- [init(from: any Decoder) throws](/documentation/lightweightcoderequirements/validationcategory/init(from:))

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/lightweightcoderequirements/validationcategory/encode(to:))

### Type Aliases

- [ValidationCategory.DataType](/documentation/lightweightcoderequirements/validationcategory/datatype)
- [ValidationCategory.OutType](/documentation/lightweightcoderequirements/validationcategory/outtype)

### Type Methods

- [static func `in`([ValidationCategory.DataType]) -> ValidationCategory.OutType](/documentation/lightweightcoderequirements/validationcategory/in(_:)-1skt4)
- [static func `in`(ValidationCategory.DataType...) -> ValidationCategory.OutType](/documentation/lightweightcoderequirements/validationcategory/in(_:)-94p2z)

## Handling errors

- [ConstraintError](/documentation/lightweightcoderequirements/constrainterror)

### Enumeration Cases

- [case duplicateKey](/documentation/lightweightcoderequirements/constrainterror/duplicatekey)
- [case malformedConstraint](/documentation/lightweightcoderequirements/constrainterror/malformedconstraint)
- [case taskIsNoLongerValid](/documentation/lightweightcoderequirements/constrainterror/taskisnolongervalid)
- [case unsupportedConstraintForRequirementType](/documentation/lightweightcoderequirements/constrainterror/unsupportedconstraintforrequirementtype)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
