# AppMigrationKit Documentation

Source: https://sosumi.ai/documentation/appmigrationkit

---
title: AppMigrationKit
source: https://developer.apple.com/documentation/appmigrationkit
timestamp: 2026-02-13T18:53:52.544Z
---

## App extensions

- [AppMigrationExtension](/documentation/appmigrationkit/appmigrationextension)

### Accessing migration data

- [var appContainer: MigrationDataContainer](/documentation/appmigrationkit/appmigrationextension/appcontainer)
- [MigrationDataContainer](/documentation/appmigrationkit/migrationdatacontainer)

#### Identifying the app

- [let bundleIdentifier: String](/documentation/appmigrationkit/migrationdatacontainer/bundleidentifier)

#### Accessing app directories

- [let containerRootDirectory: URL](/documentation/appmigrationkit/migrationdatacontainer/containerrootdirectory)
- [var applicationSupportDirectory: URL](/documentation/appmigrationkit/migrationdatacontainer/applicationsupportdirectory)
- [var documentsDirectory: URL](/documentation/appmigrationkit/migrationdatacontainer/documentsdirectory)
- [com.apple.developer.app-migration.data-container-access](/documentation/bundleresources/entitlements/com.apple.developer.app-migration.data-container-access)

## Export operations

- [ResourcesExportingWithOptions](/documentation/appmigrationkit/resourcesexportingwithoptions)

### Exporting resources

- [func exportResources(to: sending ResourcesArchiver, request: MigrationRequestWithOptions<Self.OptionsType>) async throws](/documentation/appmigrationkit/resourcesexportingwithoptions/exportresources(to:request:))
- [ResourcesArchiver](/documentation/appmigrationkit/resourcesarchiver)

#### Appending resources

- [func appendItem(at: URL, pathInArchive: String?) async throws](/documentation/appmigrationkit/resourcesarchiver/appenditem(at:pathinarchive:))
- [MigrationRequestWithOptions](/documentation/appmigrationkit/migrationrequestwithoptions)

#### Creating a migration request instance

- [init(destinationPlatform: MigrationPlatform, options: [OptionsType : Data])](/documentation/appmigrationkit/migrationrequestwithoptions/init(destinationplatform:options:))

#### Inspecting migration request properties

- [let destinationPlatform: MigrationPlatform](/documentation/appmigrationkit/migrationrequestwithoptions/destinationplatform)
- [MigrationPlatform](/documentation/appmigrationkit/migrationplatform)

##### Creating a migration platform instance

- [init(String)](/documentation/appmigrationkit/migrationplatform/init(_:))

##### Identifying migration platforms

- [static let android: MigrationPlatform](/documentation/appmigrationkit/migrationplatform/android)
- [let options: [OptionsType : Data]](/documentation/appmigrationkit/migrationrequestwithoptions/options)

#### Declaring default options

- [MigrationDefaultSupportedOptions](/documentation/appmigrationkit/migrationdefaultsupportedoptions)

##### Accessing all options

- [static let allCases: [MigrationDefaultSupportedOptions]](/documentation/appmigrationkit/migrationdefaultsupportedoptions/allcases)
- [MigrationRequest](/documentation/appmigrationkit/migrationrequest)

### Declaring resource properties

- [var resourcesSizeEstimate: Int](/documentation/appmigrationkit/resourcesexportingwithoptions/resourcessizeestimate)
- [var resourcesVersion: String](/documentation/appmigrationkit/resourcesexportingwithoptions/resourcesversion)
- [var resourcesCompressible: Bool](/documentation/appmigrationkit/resourcesexportingwithoptions/resourcescompressible)

### Declaring export options

- [OptionsType](/documentation/appmigrationkit/resourcesexportingwithoptions/optionstype)
- [ResourcesExporting](/documentation/appmigrationkit/resourcesexporting)

## Import operations

- [ResourcesImporting](/documentation/appmigrationkit/resourcesimporting)

### Importing resources

- [func importResources(at: URL, request: ResourcesImportRequest) async throws](/documentation/appmigrationkit/resourcesimporting/importresources(at:request:))
- [ResourcesImportRequest](/documentation/appmigrationkit/resourcesimportrequest)

#### Creating an import request for testing

- [init(sourceAppIdentifier: MigrationAppIdentifier, sourceVersion: String)](/documentation/appmigrationkit/resourcesimportrequest/init(sourceappidentifier:sourceversion:))

#### Inspecting import request properties

- [let sourceAppIdentifier: MigrationAppIdentifier](/documentation/appmigrationkit/resourcesimportrequest/sourceappidentifier)
- [MigrationAppIdentifier](/documentation/appmigrationkit/migrationappidentifier)

##### Creating a migration app identifier

- [init(storeIdentifier: MigrationAppIdentifier.StoreIdentifier, bundleIdentifier: String, platform: MigrationPlatform)](/documentation/appmigrationkit/migrationappidentifier/init(storeidentifier:bundleidentifier:platform:))

##### Working with identifier properties

- [let storeIdentifier: MigrationAppIdentifier.StoreIdentifier](/documentation/appmigrationkit/migrationappidentifier/storeidentifier-swift.property)
- [MigrationAppIdentifier.StoreIdentifier](/documentation/appmigrationkit/migrationappidentifier/storeidentifier-swift.struct)

###### Creating a store identifier instance

- [init(String)](/documentation/appmigrationkit/migrationappidentifier/storeidentifier-swift.struct/init(_:))

###### Type Properties

- [static let googlePlay: MigrationAppIdentifier.StoreIdentifier](/documentation/appmigrationkit/migrationappidentifier/storeidentifier-swift.struct/googleplay)
- [let bundleIdentifier: String](/documentation/appmigrationkit/migrationappidentifier/bundleidentifier)
- [let platform: MigrationPlatform](/documentation/appmigrationkit/migrationappidentifier/platform)
- [MigrationPlatform](/documentation/appmigrationkit/migrationplatform)

###### Creating a migration platform instance

- [init(String)](/documentation/appmigrationkit/migrationplatform/init(_:))

###### Identifying migration platforms

- [static let android: MigrationPlatform](/documentation/appmigrationkit/migrationplatform/android)
- [let sourceVersion: String](/documentation/appmigrationkit/resourcesimportrequest/sourceversion)

### Expressing progress

- [var resourcesImportProgress: Progress](/documentation/appmigrationkit/resourcesimporting/resourcesimportprogress)

## Migration status

- [MigrationStatus](/documentation/appmigrationkit/migrationstatus)

### Accessing the import status

- [static var importStatus: MigrationStatus?](/documentation/appmigrationkit/migrationstatus/importstatus)
- [static func clearImportStatus()](/documentation/appmigrationkit/migrationstatus/clearimportstatus())

### Examining migration statuses

- [case success](/documentation/appmigrationkit/migrationstatus/success)
- [case failure(any Error)](/documentation/appmigrationkit/migrationstatus/failure(_:))

## Migration code tests

- [AppMigrationTester](/documentation/appmigrationkit/appmigrationtester)

### Creating a tester instance

- [init(platform: MigrationPlatform) async throws](/documentation/appmigrationkit/appmigrationtester/init(platform:))

### Testing export

- [var exportController: AppMigrationTester.AppExportController](/documentation/appmigrationkit/appmigrationtester/exportcontroller)
- [AppMigrationTester.AppExportController](/documentation/appmigrationkit/appmigrationtester/appexportcontroller)

#### Testing resource export

- [func exportResources<SupportedOptions>(request: MigrationRequestWithOptions<SupportedOptions>?, progress: Progress?) async throws -> AppMigrationTester.ResourcesExportResult](/documentation/appmigrationkit/appmigrationtester/appexportcontroller/exportresources(request:progress:)-15m4v)
- [func exportResources(request: MigrationRequest?, progress: Progress?) async throws -> AppMigrationTester.ResourcesExportResult](/documentation/appmigrationkit/appmigrationtester/appexportcontroller/exportresources(request:progress:)-5mw8u)
- [AppMigrationTester.ResourcesExportResult](/documentation/appmigrationkit/appmigrationtester/resourcesexportresult)

##### Inspecting result properties

- [let extractedResourcesURL: URL](/documentation/appmigrationkit/appmigrationtester/resourcesexportresult/extractedresourcesurl)
- [let exportProperties: AppMigrationTester.DeviceToDeviceExportProperties](/documentation/appmigrationkit/appmigrationtester/resourcesexportresult/exportproperties)
- [AppMigrationTester.DeviceToDeviceExportProperties](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties)

###### Inspecting data size properties

- [let uncompressedBytes: Int](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/uncompressedbytes)
- [let compressedBytes: Int?](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/compressedbytes)
- [let sizeEstimate: Int](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/sizeestimate)

###### Inspecting metadata properties

- [let version: String](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/version)

#### Supporting types

- [MigrationRequestWithOptions](/documentation/appmigrationkit/migrationrequestwithoptions)

##### Creating a migration request instance

- [init(destinationPlatform: MigrationPlatform, options: [OptionsType : Data])](/documentation/appmigrationkit/migrationrequestwithoptions/init(destinationplatform:options:))

##### Inspecting migration request properties

- [let destinationPlatform: MigrationPlatform](/documentation/appmigrationkit/migrationrequestwithoptions/destinationplatform)
- [MigrationPlatform](/documentation/appmigrationkit/migrationplatform)

###### Creating a migration platform instance

- [init(String)](/documentation/appmigrationkit/migrationplatform/init(_:))

###### Identifying migration platforms

- [static let android: MigrationPlatform](/documentation/appmigrationkit/migrationplatform/android)
- [let options: [OptionsType : Data]](/documentation/appmigrationkit/migrationrequestwithoptions/options)

##### Declaring default options

- [MigrationDefaultSupportedOptions](/documentation/appmigrationkit/migrationdefaultsupportedoptions)

###### Accessing all options

- [static let allCases: [MigrationDefaultSupportedOptions]](/documentation/appmigrationkit/migrationdefaultsupportedoptions/allcases)
- [MigrationRequest](/documentation/appmigrationkit/migrationrequest)
- [MigrationRequest](/documentation/appmigrationkit/migrationrequest)

### Testing import

- [var importController: AppMigrationTester.AppImportController](/documentation/appmigrationkit/appmigrationtester/importcontroller)
- [AppMigrationTester.AppImportController](/documentation/appmigrationkit/appmigrationtester/appimportcontroller)

#### Testing resource import

- [func importResources(from: URL, importRequest: ResourcesImportRequest?, progress: Progress?) async throws](/documentation/appmigrationkit/appmigrationtester/appimportcontroller/importresources(from:importrequest:progress:))

#### Completing an import

- [func registerImportCompletion(with: MigrationStatus) async throws](/documentation/appmigrationkit/appmigrationtester/appimportcontroller/registerimportcompletion(with:))

### Supporting types

- [AppMigrationTester.DeviceToDeviceExportProperties](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties)

#### Inspecting data size properties

- [let uncompressedBytes: Int](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/uncompressedbytes)
- [let compressedBytes: Int?](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/compressedbytes)
- [let sizeEstimate: Int](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/sizeestimate)

#### Inspecting metadata properties

- [let version: String](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/version)
- [AppMigrationTester.ResourcesExportResult](/documentation/appmigrationkit/appmigrationtester/resourcesexportresult)

#### Inspecting result properties

- [let extractedResourcesURL: URL](/documentation/appmigrationkit/appmigrationtester/resourcesexportresult/extractedresourcesurl)
- [let exportProperties: AppMigrationTester.DeviceToDeviceExportProperties](/documentation/appmigrationkit/appmigrationtester/resourcesexportresult/exportproperties)
- [AppMigrationTester.DeviceToDeviceExportProperties](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties)

##### Inspecting data size properties

- [let uncompressedBytes: Int](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/uncompressedbytes)
- [let compressedBytes: Int?](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/compressedbytes)
- [let sizeEstimate: Int](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/sizeestimate)

##### Inspecting metadata properties

- [let version: String](/documentation/appmigrationkit/appmigrationtester/devicetodeviceexportproperties/version)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
