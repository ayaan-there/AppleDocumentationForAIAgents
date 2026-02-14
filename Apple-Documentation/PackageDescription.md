# PackageDescription Documentation

Source: https://sosumi.ai/documentation/packagedescription

---
title: PackageDescription
source: https://developer.apple.com/documentation/packagedescription
timestamp: 2026-02-13T19:00:20.272Z
---

## Creating a Package

- [Package](/documentation/packagedescription/package)

### Creating a Package

- [init(name: String, defaultLocalization: LanguageTag?, platforms: [SupportedPlatform]?, pkgConfig: String?, providers: [SystemPackageProvider]?, products: [Product], dependencies: [Package.Dependency], targets: [Target], swiftLanguageModes: [SwiftLanguageMode]?, cLanguageStandard: CLanguageStandard?, cxxLanguageStandard: CXXLanguageStandard?)](/documentation/packagedescription/package/init(name:defaultlocalization:platforms:pkgconfig:providers:products:dependencies:targets:swiftlanguagemodes:clanguagestandard:cxxlanguagestandard:))
- [init(name: String, defaultLocalization: LanguageTag?, platforms: [SupportedPlatform]?, pkgConfig: String?, providers: [SystemPackageProvider]?, products: [Product], traits: Set<Trait>, dependencies: [Package.Dependency], targets: [Target], swiftLanguageModes: [SwiftLanguageMode]?, cLanguageStandard: CLanguageStandard?, cxxLanguageStandard: CXXLanguageStandard?)](/documentation/packagedescription/package/init(name:defaultlocalization:platforms:pkgconfig:providers:products:traits:dependencies:targets:swiftlanguagemodes:clanguagestandard:cxxlanguagestandard:))
- [init(name: String, defaultLocalization: LanguageTag?, platforms: [SupportedPlatform]?, pkgConfig: String?, providers: [SystemPackageProvider]?, products: [Product], dependencies: [Package.Dependency], targets: [Target], swiftLanguageVersions: [SwiftVersion]?, cLanguageStandard: CLanguageStandard?, cxxLanguageStandard: CXXLanguageStandard?)](/documentation/packagedescription/package/init(name:defaultlocalization:platforms:pkgconfig:providers:products:dependencies:targets:swiftlanguageversions:clanguagestandard:cxxlanguagestandard:))
- [init(name: String, platforms: [SupportedPlatform]?, pkgConfig: String?, providers: [SystemPackageProvider]?, products: [Product], dependencies: [Package.Dependency], targets: [Target], swiftLanguageVersions: [SwiftVersion]?, cLanguageStandard: CLanguageStandard?, cxxLanguageStandard: CXXLanguageStandard?)](/documentation/packagedescription/package/init(name:platforms:pkgconfig:providers:products:dependencies:targets:swiftlanguageversions:clanguagestandard:cxxlanguagestandard:))
- [init(name: String, pkgConfig: String?, providers: [SystemPackageProvider]?, products: [Product], dependencies: [Package.Dependency], targets: [Target], swiftLanguageVersions: [Int]?, cLanguageStandard: CLanguageStandard?, cxxLanguageStandard: CXXLanguageStandard?)](/documentation/packagedescription/package/init(name:pkgconfig:providers:products:dependencies:targets:swiftlanguageversions:clanguagestandard:cxxlanguagestandard:)-7ld3y)
- [init(name: String, pkgConfig: String?, providers: [SystemPackageProvider]?, products: [Product], dependencies: [Package.Dependency], targets: [Target], swiftLanguageVersions: [SwiftVersion]?, cLanguageStandard: CLanguageStandard?, cxxLanguageStandard: CXXLanguageStandard?)](/documentation/packagedescription/package/init(name:pkgconfig:providers:products:dependencies:targets:swiftlanguageversions:clanguagestandard:cxxlanguagestandard:)-767rj)

### Naming the Package

- [var name: String](/documentation/packagedescription/package/name)

### Localizing Package Resources

- [var defaultLocalization: LanguageTag?](/documentation/packagedescription/package/defaultlocalization)
- [LanguageTag](/documentation/packagedescription/languagetag)

#### Creating a Language Tag

- [init(extendedGraphemeClusterLiteral: String)](/documentation/packagedescription/languagetag/init(extendedgraphemeclusterliteral:))
- [init(stringLiteral: String)](/documentation/packagedescription/languagetag/init(stringliteral:))
- [init(unicodeScalarLiteral: String)](/documentation/packagedescription/languagetag/init(unicodescalarliteral:))
- [init?(rawValue: String)](/documentation/packagedescription/languagetag/init(rawvalue:))

#### Describing a Language Tag

- [var description: String](/documentation/packagedescription/languagetag/description)

#### Default Implementations

- [CustomStringConvertible Implementations](/documentation/packagedescription/languagetag/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/packagedescription/languagetag/description)
- [ExpressibleByExtendedGraphemeClusterLiteral Implementations](/documentation/packagedescription/languagetag/expressiblebyextendedgraphemeclusterliteral-implementations)

##### Initializers

- [init(extendedGraphemeClusterLiteral: String)](/documentation/packagedescription/languagetag/init(extendedgraphemeclusterliteral:))
- [ExpressibleByStringLiteral Implementations](/documentation/packagedescription/languagetag/expressiblebystringliteral-implementations)

##### Initializers

- [init(stringLiteral: String)](/documentation/packagedescription/languagetag/init(stringliteral:))
- [ExpressibleByUnicodeScalarLiteral Implementations](/documentation/packagedescription/languagetag/expressiblebyunicodescalarliteral-implementations)

##### Initializers

- [init(unicodeScalarLiteral: String)](/documentation/packagedescription/languagetag/init(unicodescalarliteral:))
- [RawRepresentable Implementations](/documentation/packagedescription/languagetag/rawrepresentable-implementations)

##### Initializers

- [init?(rawValue: String)](/documentation/packagedescription/languagetag/init(rawvalue:))

### Configuring Products

- [var products: [Product]](/documentation/packagedescription/package/products)
- [Product](/documentation/packagedescription/product)

#### Creating a Library Product

- [static func library(name: String, type: Product.Library.LibraryType?, targets: [String]) -> Product](/documentation/packagedescription/product/library(name:type:targets:))
- [Product.Library](/documentation/packagedescription/product/library)

##### Describing a Library Product

- [let targets: [String]](/documentation/packagedescription/product/library/targets)
- [let type: Product.Library.LibraryType?](/documentation/packagedescription/product/library/type)
- [Product.Library.LibraryType](/documentation/packagedescription/product/library/librarytype)

###### Enumeration Cases

- [case dynamic](/documentation/packagedescription/product/library/librarytype/dynamic)
- [case `static`](/documentation/packagedescription/product/library/librarytype/static)

#### Creating an Executable Product

- [static func executable(name: String, targets: [String]) -> Product](/documentation/packagedescription/product/executable(name:targets:))
- [Product.Executable](/documentation/packagedescription/product/executable)

##### Describing an executable product

- [let targets: [String]](/documentation/packagedescription/product/executable/targets)

#### Creating a Plugin Product

- [static func plugin(name: String, targets: [String]) -> Product](/documentation/packagedescription/product/plugin(name:targets:))
- [Product.Plugin](/documentation/packagedescription/product/plugin)

##### Describing a plug-in product

- [let targets: [String]](/documentation/packagedescription/product/plugin/targets)

#### Naming the product

- [let name: String](/documentation/packagedescription/product/name)

### Configuring Targets

- [var targets: [Target]](/documentation/packagedescription/package/targets)
- [Target](/documentation/packagedescription/target)

#### Naming the Target

- [var name: String](/documentation/packagedescription/target/name)

#### Configuring File Locations

- [var path: String?](/documentation/packagedescription/target/path)
- [var exclude: [String]](/documentation/packagedescription/target/exclude)
- [var sources: [String]?](/documentation/packagedescription/target/sources)
- [var resources: [Resource]?](/documentation/packagedescription/target/resources)
- [Resource](/documentation/packagedescription/resource)

##### Applying Rules

- [static func process(String, localization: Resource.Localization?) -> Resource](/documentation/packagedescription/resource/process(_:localization:))
- [Resource.Localization](/documentation/packagedescription/resource/localization)

###### Enumeration Cases

- [case base](/documentation/packagedescription/resource/localization/base)
- [case `default`](/documentation/packagedescription/resource/localization/default)
- [static func copy(String) -> Resource](/documentation/packagedescription/resource/copy(_:))
- [static func embedInCode(String) -> Resource](/documentation/packagedescription/resource/embedincode(_:))
- [var publicHeadersPath: String?](/documentation/packagedescription/target/publicheaderspath)

#### Creating a Binary Target

- [static func binaryTarget(name: String, path: String) -> Target](/documentation/packagedescription/target/binarytarget(name:path:))
- [static func binaryTarget(name: String, url: String, checksum: String) -> Target](/documentation/packagedescription/target/binarytarget(name:url:checksum:))
- [var url: String?](/documentation/packagedescription/target/url)
- [var checksum: String?](/documentation/packagedescription/target/checksum)

#### Creating a System Library Target

- [static func systemLibrary(name: String, path: String?, pkgConfig: String?, providers: [SystemPackageProvider]?) -> Target](/documentation/packagedescription/target/systemlibrary(name:path:pkgconfig:providers:))
- [let pkgConfig: String?](/documentation/packagedescription/target/pkgconfig)
- [let providers: [SystemPackageProvider]?](/documentation/packagedescription/target/providers)

#### Creating an Executable Target

- [static func executableTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, publicHeadersPath: String?, packageAccess: Bool, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?, plugins: [Target.PluginUsage]?) -> Target](/documentation/packagedescription/target/executabletarget(name:dependencies:path:exclude:sources:resources:publicheaderspath:packageaccess:csettings:cxxsettings:swiftsettings:linkersettings:plugins:))
- [static func executableTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, publicHeadersPath: String?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?, plugins: [Target.PluginUsage]?) -> Target](/documentation/packagedescription/target/executabletarget(name:dependencies:path:exclude:sources:resources:publicheaderspath:csettings:cxxsettings:swiftsettings:linkersettings:plugins:))
- [static func executableTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, publicHeadersPath: String?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?) -> Target](/documentation/packagedescription/target/executabletarget(name:dependencies:path:exclude:sources:resources:publicheaderspath:csettings:cxxsettings:swiftsettings:linkersettings:))

#### Creating a Regular Target

- [static func target(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, publicHeadersPath: String?, packageAccess: Bool, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?, plugins: [Target.PluginUsage]?) -> Target](/documentation/packagedescription/target/target(name:dependencies:path:exclude:sources:resources:publicheaderspath:packageaccess:csettings:cxxsettings:swiftsettings:linkersettings:plugins:))
- [static func target(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, publicHeadersPath: String?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?, plugins: [Target.PluginUsage]?) -> Target](/documentation/packagedescription/target/target(name:dependencies:path:exclude:sources:resources:publicheaderspath:csettings:cxxsettings:swiftsettings:linkersettings:plugins:))
- [static func target(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, publicHeadersPath: String?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?) -> Target](/documentation/packagedescription/target/target(name:dependencies:path:exclude:sources:resources:publicheaderspath:csettings:cxxsettings:swiftsettings:linkersettings:))
- [static func target(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, publicHeadersPath: String?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?) -> Target](/documentation/packagedescription/target/target(name:dependencies:path:exclude:sources:publicheaderspath:csettings:cxxsettings:swiftsettings:linkersettings:))
- [static func target(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, publicHeadersPath: String?) -> Target](/documentation/packagedescription/target/target(name:dependencies:path:exclude:sources:publicheaderspath:))

#### Creating a Test Target

- [static func testTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, packageAccess: Bool, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?, plugins: [Target.PluginUsage]?) -> Target](/documentation/packagedescription/target/testtarget(name:dependencies:path:exclude:sources:resources:packageaccess:csettings:cxxsettings:swiftsettings:linkersettings:plugins:))
- [static func testTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?, plugins: [Target.PluginUsage]?) -> Target](/documentation/packagedescription/target/testtarget(name:dependencies:path:exclude:sources:resources:csettings:cxxsettings:swiftsettings:linkersettings:plugins:))
- [static func testTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, resources: [Resource]?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?) -> Target](/documentation/packagedescription/target/testtarget(name:dependencies:path:exclude:sources:resources:csettings:cxxsettings:swiftsettings:linkersettings:))
- [static func testTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, cSettings: [CSetting]?, cxxSettings: [CXXSetting]?, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?) -> Target](/documentation/packagedescription/target/testtarget(name:dependencies:path:exclude:sources:csettings:cxxsettings:swiftsettings:linkersettings:))
- [static func testTarget(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?) -> Target](/documentation/packagedescription/target/testtarget(name:dependencies:path:exclude:sources:))

#### Creating a Plugin Target

- [static func plugin(name: String, capability: Target.PluginCapability, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, packageAccess: Bool) -> Target](/documentation/packagedescription/target/plugin(name:capability:dependencies:path:exclude:sources:packageaccess:))
- [var pluginCapability: Target.PluginCapability?](/documentation/packagedescription/target/plugincapability-swift.property)
- [Target.PluginCapability](/documentation/packagedescription/target/plugincapability-swift.enum)

##### Creating a Plugin Capability

- [static func buildTool() -> Target.PluginCapability](/documentation/packagedescription/target/plugincapability-swift.enum/buildtool())
- [case command(intent: PluginCommandIntent, permissions: [PluginPermission])](/documentation/packagedescription/target/plugincapability-swift.enum/command(intent:permissions:))

##### Enumeration Cases

- [case buildTool](/documentation/packagedescription/target/plugincapability-swift.enum/buildtool)
- [PluginCommandIntent](/documentation/packagedescription/plugincommandintent)

##### Creating a Command Intent

- [static func documentationGeneration() -> PluginCommandIntent](/documentation/packagedescription/plugincommandintent/documentationgeneration())
- [static func sourceCodeFormatting() -> PluginCommandIntent](/documentation/packagedescription/plugincommandintent/sourcecodeformatting())
- [case custom(verb: String, description: String)](/documentation/packagedescription/plugincommandintent/custom(verb:description:))

##### Enumeration Cases

- [case documentationGeneration](/documentation/packagedescription/plugincommandintent/documentationgeneration)
- [case sourceCodeFormatting](/documentation/packagedescription/plugincommandintent/sourcecodeformatting)
- [PluginPermission](/documentation/packagedescription/pluginpermission)

##### Create a permission

- [case allowNetworkConnections(scope: PluginNetworkPermissionScope, reason: String)](/documentation/packagedescription/pluginpermission/allownetworkconnections(scope:reason:))
- [case writeToPackageDirectory(reason: String)](/documentation/packagedescription/pluginpermission/writetopackagedirectory(reason:))

##### Allow network connection

- [PluginNetworkPermissionScope](/documentation/packagedescription/pluginnetworkpermissionscope)

###### Enumeration Cases

- [case all(ports: [Int])](/documentation/packagedescription/pluginnetworkpermissionscope/all(ports:)-swift.enum.case)
- [case docker](/documentation/packagedescription/pluginnetworkpermissionscope/docker)
- [case local(ports: [Int])](/documentation/packagedescription/pluginnetworkpermissionscope/local(ports:)-swift.enum.case)
- [case none](/documentation/packagedescription/pluginnetworkpermissionscope/none)
- [case unixDomainSocket](/documentation/packagedescription/pluginnetworkpermissionscope/unixdomainsocket)

###### Type Methods

- [static func all(ports: Range<Int>) -> PluginNetworkPermissionScope](/documentation/packagedescription/pluginnetworkpermissionscope/all(ports:)-swift.type.method)
- [static func local(ports: Range<Int>) -> PluginNetworkPermissionScope](/documentation/packagedescription/pluginnetworkpermissionscope/local(ports:)-swift.type.method)
- [static func plugin(name: String, capability: Target.PluginCapability, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?) -> Target](/documentation/packagedescription/target/plugin(name:capability:dependencies:path:exclude:sources:))

#### Declaring a Dependency Target

- [var dependencies: [Target.Dependency]](/documentation/packagedescription/target/dependencies)
- [Target.Dependency](/documentation/packagedescription/target/dependency)

##### Creating a Target Dependency

- [static func product(name: String, package: String, moduleAliases: [String : String]?, condition: TargetDependencyCondition?) -> Target.Dependency](/documentation/packagedescription/target/dependency/product(name:package:modulealiases:condition:))
- [case productItem(name: String, package: String?, moduleAliases: [String : String]?, condition: TargetDependencyCondition?)](/documentation/packagedescription/target/dependency/productitem(name:package:modulealiases:condition:))
- [static func target(name: String, condition: TargetDependencyCondition?) -> Target.Dependency](/documentation/packagedescription/target/dependency/target(name:condition:))
- [case targetItem(name: String, condition: TargetDependencyCondition?)](/documentation/packagedescription/target/dependency/targetitem(name:condition:))
- [static func byName(name: String, condition: TargetDependencyCondition?) -> Target.Dependency](/documentation/packagedescription/target/dependency/byname(name:condition:))
- [case byNameItem(name: String, condition: TargetDependencyCondition?)](/documentation/packagedescription/target/dependency/bynameitem(name:condition:))
- [TargetDependencyCondition](/documentation/packagedescription/targetdependencycondition)

###### Creating a Dependency Condition

- [static func when(platforms: [Platform]) -> TargetDependencyCondition?](/documentation/packagedescription/targetdependencycondition/when(platforms:)-5bxhc)
- [static func when(traits: Set<String>) -> TargetDependencyCondition?](/documentation/packagedescription/targetdependencycondition/when(traits:))
- [static func when(platforms: [Platform], traits: Set<String>) -> TargetDependencyCondition?](/documentation/packagedescription/targetdependencycondition/when(platforms:traits:))
- [static func when(platforms: [Platform]?) -> TargetDependencyCondition](/documentation/packagedescription/targetdependencycondition/when(platforms:)-4djh6)
- [init(stringLiteral: String)](/documentation/packagedescription/target/dependency/init(stringliteral:))
- [static func product(name: String, package: String, condition: TargetDependencyCondition?) -> Target.Dependency](/documentation/packagedescription/target/dependency/product(name:package:condition:))
- [static func product(name: String, package: String?) -> Target.Dependency](/documentation/packagedescription/target/dependency/product(name:package:)-fp0j)
- [static func product(name: String, package: String) -> Target.Dependency](/documentation/packagedescription/target/dependency/product(name:package:)-2nako)
- [static func productItem(name: String, package: String?, condition: TargetDependencyCondition?) -> Target.Dependency](/documentation/packagedescription/target/dependency/productitem(name:package:condition:))
- [static func target(name: String) -> Target.Dependency](/documentation/packagedescription/target/dependency/target(name:))
- [static func byName(name: String) -> Target.Dependency](/documentation/packagedescription/target/dependency/byname(name:))

##### Default Implementations

- [ExpressibleByStringLiteral Implementations](/documentation/packagedescription/target/dependency/expressiblebystringliteral-implementations)

###### Initializers

- [init(stringLiteral: String)](/documentation/packagedescription/target/dependency/init(stringliteral:))
- [TargetDependencyCondition](/documentation/packagedescription/targetdependencycondition)

##### Creating a Dependency Condition

- [static func when(platforms: [Platform]) -> TargetDependencyCondition?](/documentation/packagedescription/targetdependencycondition/when(platforms:)-5bxhc)
- [static func when(traits: Set<String>) -> TargetDependencyCondition?](/documentation/packagedescription/targetdependencycondition/when(traits:))
- [static func when(platforms: [Platform], traits: Set<String>) -> TargetDependencyCondition?](/documentation/packagedescription/targetdependencycondition/when(platforms:traits:))
- [static func when(platforms: [Platform]?) -> TargetDependencyCondition](/documentation/packagedescription/targetdependencycondition/when(platforms:)-4djh6)

#### Configuring the Target

- [var cSettings: [CSetting]?](/documentation/packagedescription/target/csettings)
- [var cxxSettings: [CXXSetting]?](/documentation/packagedescription/target/cxxsettings)
- [var swiftSettings: [SwiftSetting]?](/documentation/packagedescription/target/swiftsettings)
- [var linkerSettings: [LinkerSetting]?](/documentation/packagedescription/target/linkersettings)
- [var plugins: [Target.PluginUsage]?](/documentation/packagedescription/target/plugins)
- [BuildConfiguration](/documentation/packagedescription/buildconfiguration)

##### Describing Build Configurations

- [static let debug: BuildConfiguration](/documentation/packagedescription/buildconfiguration/debug)
- [static let release: BuildConfiguration](/documentation/packagedescription/buildconfiguration/release)
- [BuildSettingCondition](/documentation/packagedescription/buildsettingcondition)

##### Checking for a Build Condition

- [static func when(platforms: [Platform]) -> BuildSettingCondition](/documentation/packagedescription/buildsettingcondition/when(platforms:))
- [static func when(configuration: BuildConfiguration) -> BuildSettingCondition](/documentation/packagedescription/buildsettingcondition/when(configuration:))
- [static func when(platforms: [Platform], configuration: BuildConfiguration) -> BuildSettingCondition](/documentation/packagedescription/buildsettingcondition/when(platforms:configuration:)-475co)
- [static func when(platforms: [Platform]?, configuration: BuildConfiguration?, traits: Set<String>?) -> BuildSettingCondition](/documentation/packagedescription/buildsettingcondition/when(platforms:configuration:traits:))
- [static func when(platforms: [Platform]?, configuration: BuildConfiguration?) -> BuildSettingCondition](/documentation/packagedescription/buildsettingcondition/when(platforms:configuration:)-2991l)
- [CSetting](/documentation/packagedescription/csetting)

##### Configuring C Settings

- [static func define(String, to: String?, BuildSettingCondition?) -> CSetting](/documentation/packagedescription/csetting/define(_:to:_:))
- [static func headerSearchPath(String, BuildSettingCondition?) -> CSetting](/documentation/packagedescription/csetting/headersearchpath(_:_:))
- [static func unsafeFlags([String], BuildSettingCondition?) -> CSetting](/documentation/packagedescription/csetting/unsafeflags(_:_:))

##### Type Methods

- [static func disableWarning(String, BuildSettingCondition?) -> CSetting](/documentation/packagedescription/csetting/disablewarning(_:_:))
- [static func enableWarning(String, BuildSettingCondition?) -> CSetting](/documentation/packagedescription/csetting/enablewarning(_:_:))
- [static func treatAllWarnings(as: WarningLevel, BuildSettingCondition?) -> CSetting](/documentation/packagedescription/csetting/treatallwarnings(as:_:))
- [static func treatWarning(String, as: WarningLevel, BuildSettingCondition?) -> CSetting](/documentation/packagedescription/csetting/treatwarning(_:as:_:))
- [CXXSetting](/documentation/packagedescription/cxxsetting)

##### Configuring CXX Settings

- [static func define(String, to: String?, BuildSettingCondition?) -> CXXSetting](/documentation/packagedescription/cxxsetting/define(_:to:_:))
- [static func headerSearchPath(String, BuildSettingCondition?) -> CXXSetting](/documentation/packagedescription/cxxsetting/headersearchpath(_:_:))
- [static func unsafeFlags([String], BuildSettingCondition?) -> CXXSetting](/documentation/packagedescription/cxxsetting/unsafeflags(_:_:))

##### Type Methods

- [static func disableWarning(String, BuildSettingCondition?) -> CXXSetting](/documentation/packagedescription/cxxsetting/disablewarning(_:_:))
- [static func enableWarning(String, BuildSettingCondition?) -> CXXSetting](/documentation/packagedescription/cxxsetting/enablewarning(_:_:))
- [static func treatAllWarnings(as: WarningLevel, BuildSettingCondition?) -> CXXSetting](/documentation/packagedescription/cxxsetting/treatallwarnings(as:_:))
- [static func treatWarning(String, as: WarningLevel, BuildSettingCondition?) -> CXXSetting](/documentation/packagedescription/cxxsetting/treatwarning(_:as:_:))
- [SwiftSetting](/documentation/packagedescription/swiftsetting)

##### Configuring Swift Settings

- [static func define(String, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/define(_:_:))
- [static func unsafeFlags([String], BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/unsafeflags(_:_:))
- [static func strictMemorySafety(BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/strictmemorysafety(_:))
- [static func swiftLanguageMode(SwiftLanguageMode, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/swiftlanguagemode(_:_:))
- [static func defaultIsolation(MainActor.Type?, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/defaultisolation(_:_:))
- [static func enableExperimentalFeature(String, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/enableexperimentalfeature(_:_:))
- [static func enableUpcomingFeature(String, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/enableupcomingfeature(_:_:))
- [static func interoperabilityMode(SwiftSetting.InteroperabilityMode, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/interoperabilitymode(_:_:))
- [SwiftSetting.InteroperabilityMode](/documentation/packagedescription/swiftsetting/interoperabilitymode)

###### Enumeration Cases

- [case C](/documentation/packagedescription/swiftsetting/interoperabilitymode/c)
- [case Cxx](/documentation/packagedescription/swiftsetting/interoperabilitymode/cxx)
- [static func swiftLanguageVersion(SwiftVersion, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/swiftlanguageversion(_:_:))

##### Type Methods

- [static func treatAllWarnings(as: WarningLevel, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/treatallwarnings(as:_:))
- [static func treatWarning(String, as: WarningLevel, BuildSettingCondition?) -> SwiftSetting](/documentation/packagedescription/swiftsetting/treatwarning(_:as:_:))
- [LinkerSetting](/documentation/packagedescription/linkersetting)

##### Configuring Linker Settings

- [static func linkedFramework(String, BuildSettingCondition?) -> LinkerSetting](/documentation/packagedescription/linkersetting/linkedframework(_:_:))
- [static func linkedLibrary(String, BuildSettingCondition?) -> LinkerSetting](/documentation/packagedescription/linkersetting/linkedlibrary(_:_:))
- [static func unsafeFlags([String], BuildSettingCondition?) -> LinkerSetting](/documentation/packagedescription/linkersetting/unsafeflags(_:_:))
- [Target.PluginUsage](/documentation/packagedescription/target/pluginusage)

##### Creating a Plugin Usage

- [static func plugin(name: String) -> Target.PluginUsage](/documentation/packagedescription/target/pluginusage/plugin(name:))
- [case plugin(name: String, package: String?)](/documentation/packagedescription/target/pluginusage/plugin(name:package:))

##### Default Implementations

- [ExpressibleByStringLiteral Implementations](/documentation/packagedescription/target/pluginusage/expressiblebystringliteral-implementations)

###### Initializers

- [init(stringLiteral: String)](/documentation/packagedescription/target/pluginusage/init(stringliteral:))
- [let packageAccess: Bool](/documentation/packagedescription/target/packageaccess)

#### Describing the Target Type

- [var isTest: Bool](/documentation/packagedescription/target/istest)
- [let type: Target.TargetType](/documentation/packagedescription/target/type)
- [Target.TargetType](/documentation/packagedescription/target/targettype)

##### Enumeration Cases

- [case regular](/documentation/packagedescription/target/targettype/regular)
- [case binary](/documentation/packagedescription/target/targettype/binary)
- [case system](/documentation/packagedescription/target/targettype/system)
- [case test](/documentation/packagedescription/target/targettype/test)
- [case executable](/documentation/packagedescription/target/targettype/executable)
- [case plugin](/documentation/packagedescription/target/targettype/plugin)
- [case macro](/documentation/packagedescription/target/targettype/macro)

#### Type Methods

- [static func macro(name: String, dependencies: [Target.Dependency], path: String?, exclude: [String], sources: [String]?, packageAccess: Bool, swiftSettings: [SwiftSetting]?, linkerSettings: [LinkerSetting]?, plugins: [Target.PluginUsage]?) -> Target](/documentation/packagedescription/target/macro(name:dependencies:path:exclude:sources:packageaccess:swiftsettings:linkersettings:plugins:))

### Declaring Supported Platforms

- [var platforms: [SupportedPlatform]?](/documentation/packagedescription/package/platforms)
- [SupportedPlatform](/documentation/packagedescription/supportedplatform)

#### Supporting iOS

- [static func iOS(SupportedPlatform.IOSVersion) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/ios(_:)-5pvv5)
- [static func iOS(String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/ios(_:)-83bbf)
- [static let iOS: Platform](/documentation/packagedescription/platform/ios)
- [SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion)

##### Type Properties

- [static let v10: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v10)
- [static let v11: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v11)
- [static let v12: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v12)
- [static let v13: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v13)
- [static let v14: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v14)
- [static let v15: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v15)
- [static let v16: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v16)
- [static let v17: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v17)
- [static let v18: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v18)
- [static let v26: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v26)
- [static let v8: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v8)
- [static let v9: SupportedPlatform.IOSVersion](/documentation/packagedescription/supportedplatform/iosversion/v9)

#### Supporting macOS

- [static func macOS(SupportedPlatform.MacOSVersion) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/macos(_:)-2wthp)
- [static func macOS(String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/macos(_:)-9771f)
- [static let macOS: Platform](/documentation/packagedescription/platform/macos)
- [SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion)

##### Type Properties

- [static let v10_10: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v10_10)
- [static let v10_11: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v10_11)
- [static let v10_12: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v10_12)
- [static let v10_13: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v10_13)
- [static let v10_14: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v10_14)
- [static let v10_15: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v10_15)
- [static let v11: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v11)
- [static let v12: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v12)
- [static let v13: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v13)
- [static let v14: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v14)
- [static let v15: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v15)
- [static let v26: SupportedPlatform.MacOSVersion](/documentation/packagedescription/supportedplatform/macosversion/v26)

#### Supporting watchOS

- [static func watchOS(SupportedPlatform.WatchOSVersion) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/watchos(_:)-t998)
- [static func watchOS(String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/watchos(_:)-4lrx0)
- [static let watchOS: Platform](/documentation/packagedescription/platform/watchos)
- [SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion)

##### Type Properties

- [static let v10: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v10)
- [static let v11: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v11)
- [static let v2: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v2)
- [static let v26: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v26)
- [static let v3: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v3)
- [static let v4: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v4)
- [static let v5: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v5)
- [static let v6: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v6)
- [static let v7: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v7)
- [static let v8: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v8)
- [static let v9: SupportedPlatform.WatchOSVersion](/documentation/packagedescription/supportedplatform/watchosversion/v9)

#### Supporting visionOS

- [static func visionOS(SupportedPlatform.VisionOSVersion) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/visionos(_:)-3ip0z)
- [static func visionOS(String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/visionos(_:)-6ur2u)
- [static let visionOS: Platform](/documentation/packagedescription/platform/visionos)
- [SupportedPlatform.VisionOSVersion](/documentation/packagedescription/supportedplatform/visionosversion)

##### Type Properties

- [static let v1: SupportedPlatform.VisionOSVersion](/documentation/packagedescription/supportedplatform/visionosversion/v1)
- [static let v2: SupportedPlatform.VisionOSVersion](/documentation/packagedescription/supportedplatform/visionosversion/v2)
- [static let v26: SupportedPlatform.VisionOSVersion](/documentation/packagedescription/supportedplatform/visionosversion/v26)

#### Supporting tvOS

- [static func tvOS(SupportedPlatform.TVOSVersion) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/tvos(_:)-6931l)
- [static func tvOS(String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/tvos(_:)-3k8sy)
- [static let tvOS: Platform](/documentation/packagedescription/platform/tvos)
- [SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion)

##### Type Properties

- [static let v10: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v10)
- [static let v11: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v11)
- [static let v12: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v12)
- [static let v13: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v13)
- [static let v14: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v14)
- [static let v15: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v15)
- [static let v16: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v16)
- [static let v17: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v17)
- [static let v18: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v18)
- [static let v26: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v26)
- [static let v9: SupportedPlatform.TVOSVersion](/documentation/packagedescription/supportedplatform/tvosversion/v9)

#### Supporting MacCatalyst

- [static func macCatalyst(SupportedPlatform.MacCatalystVersion) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/maccatalyst(_:)-6bh40)
- [static func macCatalyst(String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/maccatalyst(_:)-9wbz)
- [static let macCatalyst: Platform](/documentation/packagedescription/platform/maccatalyst)
- [SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion)

##### Type Properties

- [static let v13: SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion/v13)
- [static let v14: SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion/v14)
- [static let v15: SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion/v15)
- [static let v16: SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion/v16)
- [static let v17: SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion/v17)
- [static let v18: SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion/v18)
- [static let v26: SupportedPlatform.MacCatalystVersion](/documentation/packagedescription/supportedplatform/maccatalystversion/v26)

#### Supporting DriverKit

- [static func driverKit(SupportedPlatform.DriverKitVersion) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/driverkit(_:)-jxlz)
- [static func driverKit(String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/driverkit(_:)-6evdd)
- [static let driverKit: Platform](/documentation/packagedescription/platform/driverkit)
- [SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion)

##### Type Properties

- [static let v19: SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion/v19)
- [static let v20: SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion/v20)
- [static let v21: SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion/v21)
- [static let v22: SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion/v22)
- [static let v23: SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion/v23)
- [static let v24: SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion/v24)
- [static let v25: SupportedPlatform.DriverKitVersion](/documentation/packagedescription/supportedplatform/driverkitversion/v25)

#### Supporting Custom Platforms

- [static func custom(String, versionString: String) -> SupportedPlatform](/documentation/packagedescription/supportedplatform/custom(_:versionstring:))

#### Structures

- [SupportedPlatform.CustomPlatformVersion](/documentation/packagedescription/supportedplatform/customplatformversion)
- [Platform](/documentation/packagedescription/platform)

#### Platforms

- [static let iOS: Platform](/documentation/packagedescription/platform/ios)
- [static let macOS: Platform](/documentation/packagedescription/platform/macos)
- [static let tvOS: Platform](/documentation/packagedescription/platform/tvos)
- [static let watchOS: Platform](/documentation/packagedescription/platform/watchos)
- [static let visionOS: Platform](/documentation/packagedescription/platform/visionos)
- [static let macCatalyst: Platform](/documentation/packagedescription/platform/maccatalyst)
- [static let driverKit: Platform](/documentation/packagedescription/platform/driverkit)
- [static let android: Platform](/documentation/packagedescription/platform/android)
- [static let linux: Platform](/documentation/packagedescription/platform/linux)
- [static let freebsd: Platform](/documentation/packagedescription/platform/freebsd)
- [static let openbsd: Platform](/documentation/packagedescription/platform/openbsd)
- [static let wasi: Platform](/documentation/packagedescription/platform/wasi)
- [static let windows: Platform](/documentation/packagedescription/platform/windows)

#### Type methods

- [static func custom(String) -> Platform](/documentation/packagedescription/platform/custom(_:))

### Configuring System Packages

- [SystemPackageProvider](/documentation/packagedescription/systempackageprovider)

#### Providing Hints to Users of System Packages

- [static func apt([String]) -> SystemPackageProvider](/documentation/packagedescription/systempackageprovider/apt(_:))
- [static func brew([String]) -> SystemPackageProvider](/documentation/packagedescription/systempackageprovider/brew(_:))
- [static func nuget([String]) -> SystemPackageProvider](/documentation/packagedescription/systempackageprovider/nuget(_:))
- [static func yum([String]) -> SystemPackageProvider](/documentation/packagedescription/systempackageprovider/yum(_:))

#### Enumeration Cases

- [case aptItem([String])](/documentation/packagedescription/systempackageprovider/aptitem(_:))
- [case brewItem([String])](/documentation/packagedescription/systempackageprovider/brewitem(_:))
- [case nugetItem([String])](/documentation/packagedescription/systempackageprovider/nugetitem(_:))
- [case yumItem([String])](/documentation/packagedescription/systempackageprovider/yumitem(_:))
- [var pkgConfig: String?](/documentation/packagedescription/package/pkgconfig)
- [var providers: [SystemPackageProvider]?](/documentation/packagedescription/package/providers)

### Configuring Traits

- [var traits: Set<Trait>](/documentation/packagedescription/package/traits)
- [Trait](/documentation/packagedescription/trait)

#### Initializers

- [init(name: String, description: String?, enabledTraits: Set<String>)](/documentation/packagedescription/trait/init(name:description:enabledtraits:))

#### Instance Properties

- [var description: String?](/documentation/packagedescription/trait/description)
- [var enabledTraits: Set<String>](/documentation/packagedescription/trait/enabledtraits)
- [var name: String](/documentation/packagedescription/trait/name)

#### Type Methods

- [static func `default`(enabledTraits: Set<String>) -> Trait](/documentation/packagedescription/trait/default(enabledtraits:))
- [static func trait(name: String, description: String?, enabledTraits: Set<String>) -> Trait](/documentation/packagedescription/trait/trait(name:description:enabledtraits:))

### Declaring Package Dependencies

- [var dependencies: [Package.Dependency]](/documentation/packagedescription/package/dependencies)
- [Package.Dependency](/documentation/packagedescription/package/dependency)

#### Creating a package dependency from a URL

- [static func package(url: String, from: Version) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:from:))
- [static func package(url: String, from: Version, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:from:traits:))
- [static func package(url: String, Range<Version>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:_:)-2ys47)
- [static func package(url: String, Range<Version>, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:_:traits:)-5pt81)
- [static func package(url: String, ClosedRange<Version>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:_:)-1r6rc)
- [static func package(url: String, ClosedRange<Version>, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:_:traits:)-mjzv)
- [static func package(url: String, branch: String) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:branch:))
- [static func package(url: String, branch: String, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:branch:traits:))
- [static func package(url: String, revision: String) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:revision:))
- [static func package(url: String, revision: String, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:revision:traits:))
- [static func package(url: String, exact: Version) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:exact:))
- [static func package(url: String, exact: Version, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:exact:traits:))

#### Creating a package dependency from a registry

- [static func package(id: String, from: Version) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:from:))
- [static func package(id: String, from: Version, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:from:traits:))
- [static func package(id: String, Range<Version>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:_:)-27raa)
- [static func package(id: String, Range<Version>, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:_:traits:)-5rb8r)
- [static func package(id: String, ClosedRange<Version>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:_:)-6anr7)
- [static func package(id: String, ClosedRange<Version>, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:_:traits:)-5x94p)
- [static func package(id: String, exact: Version) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:exact:))
- [static func package(id: String, exact: Version, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(id:exact:traits:))

#### Creating a local dependency

- [static func package(name: String, path: String) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:path:))
- [static func package(name: String, path: String, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:path:traits:))
- [static func package(path: String) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(path:))
- [static func package(path: String, traits: Set<Package.Dependency.Trait>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(path:traits:))

#### Declaring Requirements

- [let traits: Set<Package.Dependency.Trait>](/documentation/packagedescription/package/dependency/traits)
- [Package.Dependency.Trait](/documentation/packagedescription/package/dependency/trait)

##### Structures

- [Package.Dependency.Trait.Condition](/documentation/packagedescription/package/dependency/trait/condition-swift.struct)

###### Type Methods

- [static func when(traits: Set<String>) -> Package.Dependency.Trait.Condition?](/documentation/packagedescription/package/dependency/trait/condition-swift.struct/when(traits:))

##### Initializers

- [init(name: String, condition: Package.Dependency.Trait.Condition?)](/documentation/packagedescription/package/dependency/trait/init(name:condition:))

##### Instance Properties

- [var condition: Package.Dependency.Trait.Condition?](/documentation/packagedescription/package/dependency/trait/condition-swift.property)
- [var name: String](/documentation/packagedescription/package/dependency/trait/name)

##### Type Properties

- [static let defaults: Package.Dependency.Trait](/documentation/packagedescription/package/dependency/trait/defaults)

##### Type Methods

- [static func trait(name: String, condition: Package.Dependency.Trait.Condition?) -> Package.Dependency.Trait](/documentation/packagedescription/package/dependency/trait/trait(name:condition:))
- [Package.Dependency.RegistryRequirement](/documentation/packagedescription/package/dependency/registryrequirement)

##### Enumeration Cases

- [case exact(Version)](/documentation/packagedescription/package/dependency/registryrequirement/exact(_:))
- [case range(Range<Version>)](/documentation/packagedescription/package/dependency/registryrequirement/range(_:))
- [Package.Dependency.SourceControlRequirement](/documentation/packagedescription/package/dependency/sourcecontrolrequirement)

##### Enumeration Cases

- [case branch(String)](/documentation/packagedescription/package/dependency/sourcecontrolrequirement/branch(_:))
- [case exact(Version)](/documentation/packagedescription/package/dependency/sourcecontrolrequirement/exact(_:))
- [case range(Range<Version>)](/documentation/packagedescription/package/dependency/sourcecontrolrequirement/range(_:))
- [case revision(String)](/documentation/packagedescription/package/dependency/sourcecontrolrequirement/revision(_:))
- [var requirement: Package.Dependency.Requirement](/documentation/packagedescription/package/dependency/requirement-swift.property)
- [Package.Dependency.Requirement](/documentation/packagedescription/package/dependency/requirement-swift.enum)

##### Enumeration Cases

- [case branchItem(String)](/documentation/packagedescription/package/dependency/requirement-swift.enum/branchitem(_:))
- [case exactItem(Version)](/documentation/packagedescription/package/dependency/requirement-swift.enum/exactitem(_:))
- [case localPackageItem](/documentation/packagedescription/package/dependency/requirement-swift.enum/localpackageitem)
- [case rangeItem(Range<Version>)](/documentation/packagedescription/package/dependency/requirement-swift.enum/rangeitem(_:))
- [case revisionItem(String)](/documentation/packagedescription/package/dependency/requirement-swift.enum/revisionitem(_:))

##### Type Methods

- [static func branch(String) -> Package.Dependency.Requirement](/documentation/packagedescription/package/dependency/requirement-swift.enum/branch(_:))
- [static func exact(Version) -> Package.Dependency.Requirement](/documentation/packagedescription/package/dependency/requirement-swift.enum/exact(_:))
- [static func revision(String) -> Package.Dependency.Requirement](/documentation/packagedescription/package/dependency/requirement-swift.enum/revision(_:))
- [static func upToNextMajor(from: Version) -> Package.Dependency.Requirement](/documentation/packagedescription/package/dependency/requirement-swift.enum/uptonextmajor(from:))
- [static func upToNextMinor(from: Version) -> Package.Dependency.Requirement](/documentation/packagedescription/package/dependency/requirement-swift.enum/uptonextminor(from:))

#### Describing a Package Dependency

- [let kind: Package.Dependency.Kind](/documentation/packagedescription/package/dependency/kind-swift.property)
- [Package.Dependency.Kind](/documentation/packagedescription/package/dependency/kind-swift.enum)

##### Enumeration Cases

- [case fileSystem(name: String?, path: String)](/documentation/packagedescription/package/dependency/kind-swift.enum/filesystem(name:path:))
- [case registry(id: String, requirement: Package.Dependency.RegistryRequirement)](/documentation/packagedescription/package/dependency/kind-swift.enum/registry(id:requirement:))
- [case sourceControl(name: String?, location: String, requirement: Package.Dependency.SourceControlRequirement)](/documentation/packagedescription/package/dependency/kind-swift.enum/sourcecontrol(name:location:requirement:))
- [Version](/documentation/packagedescription/version)

##### Creating a new version

- [init(Int, Int, Int, prereleaseIdentifiers: [String], buildMetadataIdentifiers: [String])](/documentation/packagedescription/version/init(_:_:_:prereleaseidentifiers:buildmetadataidentifiers:))

##### Inspecting a version

- [let major: Int](/documentation/packagedescription/version/major)
- [let minor: Int](/documentation/packagedescription/version/minor)
- [let patch: Int](/documentation/packagedescription/version/patch)
- [let prereleaseIdentifiers: [String]](/documentation/packagedescription/version/prereleaseidentifiers)
- [let buildMetadataIdentifiers: [String]](/documentation/packagedescription/version/buildmetadataidentifiers)

##### Default Implementations

- [Comparable Implementations](/documentation/packagedescription/version/comparable-implementations)

###### Operators

- [static func < (Version, Version) -> Bool](/documentation/packagedescription/version/_(_:_:))
- [CustomStringConvertible Implementations](/documentation/packagedescription/version/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/packagedescription/version/description)
- [Equatable Implementations](/documentation/packagedescription/version/equatable-implementations)

###### Operators

- [static func == (Version, Version) -> Bool](/documentation/packagedescription/version/==(_:_:))
- [ExpressibleByExtendedGraphemeClusterLiteral Implementations](/documentation/packagedescription/version/expressiblebyextendedgraphemeclusterliteral-implementations)

###### Initializers

- [init(extendedGraphemeClusterLiteral: String)](/documentation/packagedescription/version/init(extendedgraphemeclusterliteral:))
- [ExpressibleByStringLiteral Implementations](/documentation/packagedescription/version/expressiblebystringliteral-implementations)

###### Initializers

- [init(stringLiteral: String)](/documentation/packagedescription/version/init(stringliteral:))
- [ExpressibleByUnicodeScalarLiteral Implementations](/documentation/packagedescription/version/expressiblebyunicodescalarliteral-implementations)

###### Initializers

- [init(unicodeScalarLiteral: String)](/documentation/packagedescription/version/init(unicodescalarliteral:))
- [LosslessStringConvertible Implementations](/documentation/packagedescription/version/losslessstringconvertible-implementations)

###### Initializers

- [init?(String)](/documentation/packagedescription/version/init(_:))
- [var name: String?](/documentation/packagedescription/package/dependency/name)
- [var url: String?](/documentation/packagedescription/package/dependency/url)

#### Deprecated methods

- [static func package(name: String?, url: String, Package.Dependency.Requirement) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:url:_:)-6k3na)
- [static func package(name: String, url: String, Range<Version>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:url:_:)-nqbk)
- [static func package(name: String, url: String, ClosedRange<Version>) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:url:_:)-7zltl)
- [static func package(name: String, url: String, branch: String) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:url:branch:))
- [static func package(name: String, url: String, from: Version) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:url:from:))
- [static func package(name: String, url: String, revision: String) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(name:url:revision:))
- [static func package(url: String, Package.Dependency.Requirement) -> Package.Dependency](/documentation/packagedescription/package/dependency/package(url:_:)-4tkwi)
- [var name: String?](/documentation/packagedescription/package/dependency/name)
- [var url: String?](/documentation/packagedescription/package/dependency/url)

### Declaring Supported Languages

- [SwiftLanguageMode](/documentation/packagedescription/swiftlanguagemode)

#### Swift Language Modes

- [case v6](/documentation/packagedescription/swiftlanguagemode/v6)
- [case v5](/documentation/packagedescription/swiftlanguagemode/v5)
- [case v4_2](/documentation/packagedescription/swiftlanguagemode/v4_2)
- [case v4](/documentation/packagedescription/swiftlanguagemode/v4)
- [case version(String)](/documentation/packagedescription/swiftlanguagemode/version(_:))
- [case v3](/documentation/packagedescription/swiftlanguagemode/v3)
- [CLanguageStandard](/documentation/packagedescription/clanguagestandard)

#### Enumeration Cases

- [case c11](/documentation/packagedescription/clanguagestandard/c11)
- [case c17](/documentation/packagedescription/clanguagestandard/c17)
- [case c18](/documentation/packagedescription/clanguagestandard/c18)
- [case c2x](/documentation/packagedescription/clanguagestandard/c2x)
- [case c89](/documentation/packagedescription/clanguagestandard/c89)
- [case c90](/documentation/packagedescription/clanguagestandard/c90)
- [case c99](/documentation/packagedescription/clanguagestandard/c99)
- [case gnu11](/documentation/packagedescription/clanguagestandard/gnu11)
- [case gnu17](/documentation/packagedescription/clanguagestandard/gnu17)
- [case gnu18](/documentation/packagedescription/clanguagestandard/gnu18)
- [case gnu2x](/documentation/packagedescription/clanguagestandard/gnu2x)
- [case gnu89](/documentation/packagedescription/clanguagestandard/gnu89)
- [case gnu90](/documentation/packagedescription/clanguagestandard/gnu90)
- [case gnu99](/documentation/packagedescription/clanguagestandard/gnu99)
- [case iso9899_1990](/documentation/packagedescription/clanguagestandard/iso9899_1990)
- [case iso9899_199409](/documentation/packagedescription/clanguagestandard/iso9899_199409)
- [case iso9899_1999](/documentation/packagedescription/clanguagestandard/iso9899_1999)
- [case iso9899_2011](/documentation/packagedescription/clanguagestandard/iso9899_2011)
- [case iso9899_2017](/documentation/packagedescription/clanguagestandard/iso9899_2017)
- [case iso9899_2018](/documentation/packagedescription/clanguagestandard/iso9899_2018)
- [CXXLanguageStandard](/documentation/packagedescription/cxxlanguagestandard)

#### Enumeration Cases

- [case cxx03](/documentation/packagedescription/cxxlanguagestandard/cxx03)
- [case cxx11](/documentation/packagedescription/cxxlanguagestandard/cxx11)
- [case cxx14](/documentation/packagedescription/cxxlanguagestandard/cxx14)
- [case cxx1z](/documentation/packagedescription/cxxlanguagestandard/cxx1z)
- [case cxx98](/documentation/packagedescription/cxxlanguagestandard/cxx98)
- [case gnucxx03](/documentation/packagedescription/cxxlanguagestandard/gnucxx03)
- [case gnucxx11](/documentation/packagedescription/cxxlanguagestandard/gnucxx11)
- [case gnucxx14](/documentation/packagedescription/cxxlanguagestandard/gnucxx14)
- [case gnucxx1z](/documentation/packagedescription/cxxlanguagestandard/gnucxx1z)
- [case gnucxx98](/documentation/packagedescription/cxxlanguagestandard/gnucxx98)
- [case cxx17](/documentation/packagedescription/cxxlanguagestandard/cxx17)
- [case cxx20](/documentation/packagedescription/cxxlanguagestandard/cxx20)
- [case cxx2b](/documentation/packagedescription/cxxlanguagestandard/cxx2b)
- [case gnucxx17](/documentation/packagedescription/cxxlanguagestandard/gnucxx17)
- [case gnucxx20](/documentation/packagedescription/cxxlanguagestandard/gnucxx20)
- [case gnucxx2b](/documentation/packagedescription/cxxlanguagestandard/gnucxx2b)
- [var swiftLanguageModes: [SwiftLanguageMode]?](/documentation/packagedescription/package/swiftlanguagemodes)
- [var cLanguageStandard: CLanguageStandard?](/documentation/packagedescription/package/clanguagestandard)
- [var cxxLanguageStandard: CXXLanguageStandard?](/documentation/packagedescription/package/cxxlanguagestandard)
- [SwiftVersion](/documentation/packagedescription/swiftversion)
- [var swiftLanguageVersions: [SwiftVersion]?](/documentation/packagedescription/package/swiftlanguageversions)
- [Context](/documentation/packagedescription/context)

### Type Properties

- [static var environment: [String : String]](/documentation/packagedescription/context/environment)
- [static var gitInformation: GitInformation?](/documentation/packagedescription/context/gitinformation)
- [static var packageDirectory: String](/documentation/packagedescription/context/packagedirectory)

## Structures

- [GitInformation](/documentation/packagedescription/gitinformation)

### Instance Properties

- [let currentCommit: String](/documentation/packagedescription/gitinformation/currentcommit)
- [let currentTag: String?](/documentation/packagedescription/gitinformation/currenttag)
- [let hasUncommittedChanges: Bool](/documentation/packagedescription/gitinformation/hasuncommittedchanges)
- [Version](/documentation/packagedescription/version)

### Creating a new version

- [init(Int, Int, Int, prereleaseIdentifiers: [String], buildMetadataIdentifiers: [String])](/documentation/packagedescription/version/init(_:_:_:prereleaseidentifiers:buildmetadataidentifiers:))

### Inspecting a version

- [let major: Int](/documentation/packagedescription/version/major)
- [let minor: Int](/documentation/packagedescription/version/minor)
- [let patch: Int](/documentation/packagedescription/version/patch)
- [let prereleaseIdentifiers: [String]](/documentation/packagedescription/version/prereleaseidentifiers)
- [let buildMetadataIdentifiers: [String]](/documentation/packagedescription/version/buildmetadataidentifiers)

### Default Implementations

- [Comparable Implementations](/documentation/packagedescription/version/comparable-implementations)

#### Operators

- [static func < (Version, Version) -> Bool](/documentation/packagedescription/version/_(_:_:))
- [CustomStringConvertible Implementations](/documentation/packagedescription/version/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/packagedescription/version/description)
- [Equatable Implementations](/documentation/packagedescription/version/equatable-implementations)

#### Operators

- [static func == (Version, Version) -> Bool](/documentation/packagedescription/version/==(_:_:))
- [ExpressibleByExtendedGraphemeClusterLiteral Implementations](/documentation/packagedescription/version/expressiblebyextendedgraphemeclusterliteral-implementations)

#### Initializers

- [init(extendedGraphemeClusterLiteral: String)](/documentation/packagedescription/version/init(extendedgraphemeclusterliteral:))
- [ExpressibleByStringLiteral Implementations](/documentation/packagedescription/version/expressiblebystringliteral-implementations)

#### Initializers

- [init(stringLiteral: String)](/documentation/packagedescription/version/init(stringliteral:))
- [ExpressibleByUnicodeScalarLiteral Implementations](/documentation/packagedescription/version/expressiblebyunicodescalarliteral-implementations)

#### Initializers

- [init(unicodeScalarLiteral: String)](/documentation/packagedescription/version/init(unicodescalarliteral:))
- [LosslessStringConvertible Implementations](/documentation/packagedescription/version/losslessstringconvertible-implementations)

#### Initializers

- [init?(String)](/documentation/packagedescription/version/init(_:))

## Enumerations

- [WarningLevel](/documentation/packagedescription/warninglevel)

### Enumeration Cases

- [case error](/documentation/packagedescription/warninglevel/error)
- [case warning](/documentation/packagedescription/warninglevel/warning)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
