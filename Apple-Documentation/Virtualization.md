# Virtualization Documentation

Source: https://sosumi.ai/documentation/virtualization

---
title: Virtualization
source: https://developer.apple.com/documentation/virtualization
timestamp: 2026-02-13T19:03:41.437Z
---

## Essentials

- [Adding the Virtualization Entitlement to Your Project](/documentation/virtualization/adding-the-virtualization-entitlement-to-your-project)
- [com.apple.security.virtualization](/documentation/bundleresources/entitlements/com.apple.security.virtualization)
- [Using iCloud with macOS virtual machines](/documentation/virtualization/using-icloud-with-macos-virtual-machines)

## Virtual machine setup

- [Running macOS in a virtual machine on Apple silicon](/documentation/virtualization/running-macos-in-a-virtual-machine-on-apple-silicon)
- [Running Linux in a Virtual Machine](/documentation/virtualization/running-linux-in-a-virtual-machine)
- [Running GUI Linux in a virtual machine on a Mac](/documentation/virtualization/running-gui-linux-in-a-virtual-machine-on-a-mac)
- [Installing macOS on a Virtual Machine](/documentation/virtualization/installing-macos-on-a-virtual-machine)
- [Creating and Running a Linux Virtual Machine](/documentation/virtualization/creating-and-running-a-linux-virtual-machine)
- [Virtualize macOS on a Mac](/documentation/virtualization/virtualize-macos-on-a-mac)

### Platform components

- [VZVirtualMachineConfiguration](/documentation/virtualization/vzvirtualmachineconfiguration)

#### Configuring the guest system

- [var bootLoader: VZBootLoader?](/documentation/virtualization/vzvirtualmachineconfiguration/bootloader)

#### Setting the number of CPUs

- [var cpuCount: Int](/documentation/virtualization/vzvirtualmachineconfiguration/cpucount)
- [class var minimumAllowedCPUCount: Int](/documentation/virtualization/vzvirtualmachineconfiguration/minimumallowedcpucount)
- [class var maximumAllowedCPUCount: Int](/documentation/virtualization/vzvirtualmachineconfiguration/maximumallowedcpucount)

#### Sizing the memory partition

- [var memorySize: UInt64](/documentation/virtualization/vzvirtualmachineconfiguration/memorysize)
- [class var minimumAllowedMemorySize: UInt64](/documentation/virtualization/vzvirtualmachineconfiguration/minimumallowedmemorysize)
- [class var maximumAllowedMemorySize: UInt64](/documentation/virtualization/vzvirtualmachineconfiguration/maximumallowedmemorysize)
- [var memoryBalloonDevices: [VZMemoryBalloonDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/memoryballoondevices)

#### Adding devices to the VM

- [var consoleDevices: [VZConsoleDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/consoledevices)
- [var networkDevices: [VZNetworkDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/networkdevices)
- [var socketDevices: [VZSocketDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/socketdevices)
- [var serialPorts: [VZSerialPortConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/serialports)
- [var storageDevices: [VZStorageDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/storagedevices)
- [var entropyDevices: [VZEntropyDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/entropydevices)
- [var audioDevices: [VZAudioDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/audiodevices)
- [var directorySharingDevices: [VZDirectorySharingDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/directorysharingdevices)
- [var graphicsDevices: [VZGraphicsDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/graphicsdevices)
- [var keyboards: [VZKeyboardConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/keyboards)
- [var platform: VZPlatformConfiguration](/documentation/virtualization/vzvirtualmachineconfiguration/platform)
- [var pointingDevices: [VZPointingDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/pointingdevices)
- [var usbControllers: [VZUSBControllerConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/usbcontrollers)

#### Validating the configuration

- [func validate() throws](/documentation/virtualization/vzvirtualmachineconfiguration/validate())
- [func validateSaveRestoreSupport() throws](/documentation/virtualization/vzvirtualmachineconfiguration/validatesaverestoresupport())
- [VZMacOSVirtualMachineStartOptions](/documentation/virtualization/vzmacosvirtualmachinestartoptions)

#### Setting recovery mode

- [var startUpFromMacOSRecovery: Bool](/documentation/virtualization/vzmacosvirtualmachinestartoptions/startupfrommacosrecovery)
- [VZMacPlatformConfiguration](/documentation/virtualization/vzmacplatformconfiguration)

#### Creating a platform configuration

- [init()](/documentation/virtualization/vzmacplatformconfiguration/init())

#### Getting platform properties

- [var auxiliaryStorage: VZMacAuxiliaryStorage?](/documentation/virtualization/vzmacplatformconfiguration/auxiliarystorage)
- [var hardwareModel: VZMacHardwareModel](/documentation/virtualization/vzmacplatformconfiguration/hardwaremodel)
- [var machineIdentifier: VZMacMachineIdentifier](/documentation/virtualization/vzmacplatformconfiguration/machineidentifier)
- [VZPlatformConfiguration](/documentation/virtualization/vzplatformconfiguration)
- [VZMacHardwareModel](/documentation/virtualization/vzmachardwaremodel)

#### Creating the hardware model

- [init?(dataRepresentation: Data)](/documentation/virtualization/vzmachardwaremodel/init(datarepresentation:))

#### Configuring the hardware model

- [var dataRepresentation: Data](/documentation/virtualization/vzmachardwaremodel/datarepresentation)
- [var isSupported: Bool](/documentation/virtualization/vzmachardwaremodel/issupported)
- [VZMacMachineIdentifier](/documentation/virtualization/vzmacmachineidentifier)

#### Creating a machine identifier

- [init?(dataRepresentation: Data)](/documentation/virtualization/vzmacmachineidentifier/init(datarepresentation:))
- [init()](/documentation/virtualization/vzmacmachineidentifier/init())

#### Machine data representation

- [var dataRepresentation: Data](/documentation/virtualization/vzmacmachineidentifier/datarepresentation)
- [VZMacAuxiliaryStorage](/documentation/virtualization/vzmacauxiliarystorage)

#### Creating the auxiliary storage

- [init(contentsOfURL: URL)](/documentation/virtualization/vzmacauxiliarystorage/init(contentsofurl:))
- [init(url: URL)](/documentation/virtualization/vzmacauxiliarystorage/init(url:))
- [init(creatingStorageAt: URL, hardwareModel: VZMacHardwareModel, options: VZMacAuxiliaryStorage.InitializationOptions) throws](/documentation/virtualization/vzmacauxiliarystorage/init(creatingstorageat:hardwaremodel:options:))
- [VZMacAuxiliaryStorage.InitializationOptions](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions)

##### Mac auxiliary storage structure

- [init(rawValue: UInt)](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions/init(rawvalue:))

##### Controlling overwrites

- [static var allowOverwrite: VZMacAuxiliaryStorage.InitializationOptions](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions/allowoverwrite)
- [static var allowOverwrite: VZMacAuxiliaryStorage.InitializationOptions](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions/allowoverwrite)

#### Configuring the auxiliary storage location

- [var url: URL](/documentation/virtualization/vzmacauxiliarystorage/url)

### Boot images

- [VZMacOSBootLoader](/documentation/virtualization/vzmacosbootloader)

#### Creating a macOS boot loader

- [init()](/documentation/virtualization/vzmacosbootloader/init())
- [VZBootLoader](/documentation/virtualization/vzbootloader)

### Installers

- [VZMacOSInstaller](/documentation/virtualization/vzmacosinstaller)

#### Creating a macOS Installer

- [init(virtualMachine: VZVirtualMachine, restoringFromImageAt: URL)](/documentation/virtualization/vzmacosinstaller/init(virtualmachine:restoringfromimageat:))

#### Getting Information About an Installation

- [var progress: Progress](/documentation/virtualization/vzmacosinstaller/progress)
- [var restoreImageURL: URL](/documentation/virtualization/vzmacosinstaller/restoreimageurl)
- [var virtualMachine: VZVirtualMachine](/documentation/virtualization/vzmacosinstaller/virtualmachine)

#### Installing macOS

- [func install(completionHandler: (Result<Void, any Error>) -> Void)](/documentation/virtualization/vzmacosinstaller/install(completionhandler:))
- [func install() async throws](/documentation/virtualization/vzmacosinstaller/install())
- [VZMacOSRestoreImage](/documentation/virtualization/vzmacosrestoreimage)

#### Getting Information About the Restore Image

- [var buildVersion: String](/documentation/virtualization/vzmacosrestoreimage/buildversion)
- [var isSupported: Bool](/documentation/virtualization/vzmacosrestoreimage/issupported)
- [var mostFeaturefulSupportedConfiguration: VZMacOSConfigurationRequirements?](/documentation/virtualization/vzmacosrestoreimage/mostfeaturefulsupportedconfiguration)
- [var operatingSystemVersion: OperatingSystemVersion](/documentation/virtualization/vzmacosrestoreimage/operatingsystemversion)
- [var url: URL](/documentation/virtualization/vzmacosrestoreimage/url)

#### Controlling the Restoration Process

- [class func fetchLatestSupported(completionHandler: (Result<VZMacOSRestoreImage, any Error>) -> Void)](/documentation/virtualization/vzmacosrestoreimage/fetchlatestsupported(completionhandler:))
- [class func load(from: URL, completionHandler: (Result<VZMacOSRestoreImage, any Error>) -> Void)](/documentation/virtualization/vzmacosrestoreimage/load(from:completionhandler:))
- [class var latestSupported: VZMacOSRestoreImage](/documentation/virtualization/vzmacosrestoreimage/latestsupported)
- [class func image(from: URL) async throws -> VZMacOSRestoreImage](/documentation/virtualization/vzmacosrestoreimage/image(from:))
- [VZMacOSConfigurationRequirements](/documentation/virtualization/vzmacosconfigurationrequirements)

#### Configuration Requirements

- [var hardwareModel: VZMacHardwareModel](/documentation/virtualization/vzmacosconfigurationrequirements/hardwaremodel)
- [var minimumSupportedCPUCount: Int](/documentation/virtualization/vzmacosconfigurationrequirements/minimumsupportedcpucount)
- [var minimumSupportedMemorySize: UInt64](/documentation/virtualization/vzmacosconfigurationrequirements/minimumsupportedmemorysize)
- [Virtualize Linux on a Mac](/documentation/virtualization/virtualize-linux-on-a-mac)

### Configurations

- [VZVirtualMachineConfiguration](/documentation/virtualization/vzvirtualmachineconfiguration)

#### Configuring the guest system

- [var bootLoader: VZBootLoader?](/documentation/virtualization/vzvirtualmachineconfiguration/bootloader)

#### Setting the number of CPUs

- [var cpuCount: Int](/documentation/virtualization/vzvirtualmachineconfiguration/cpucount)
- [class var minimumAllowedCPUCount: Int](/documentation/virtualization/vzvirtualmachineconfiguration/minimumallowedcpucount)
- [class var maximumAllowedCPUCount: Int](/documentation/virtualization/vzvirtualmachineconfiguration/maximumallowedcpucount)

#### Sizing the memory partition

- [var memorySize: UInt64](/documentation/virtualization/vzvirtualmachineconfiguration/memorysize)
- [class var minimumAllowedMemorySize: UInt64](/documentation/virtualization/vzvirtualmachineconfiguration/minimumallowedmemorysize)
- [class var maximumAllowedMemorySize: UInt64](/documentation/virtualization/vzvirtualmachineconfiguration/maximumallowedmemorysize)
- [var memoryBalloonDevices: [VZMemoryBalloonDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/memoryballoondevices)

#### Adding devices to the VM

- [var consoleDevices: [VZConsoleDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/consoledevices)
- [var networkDevices: [VZNetworkDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/networkdevices)
- [var socketDevices: [VZSocketDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/socketdevices)
- [var serialPorts: [VZSerialPortConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/serialports)
- [var storageDevices: [VZStorageDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/storagedevices)
- [var entropyDevices: [VZEntropyDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/entropydevices)
- [var audioDevices: [VZAudioDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/audiodevices)
- [var directorySharingDevices: [VZDirectorySharingDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/directorysharingdevices)
- [var graphicsDevices: [VZGraphicsDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/graphicsdevices)
- [var keyboards: [VZKeyboardConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/keyboards)
- [var platform: VZPlatformConfiguration](/documentation/virtualization/vzvirtualmachineconfiguration/platform)
- [var pointingDevices: [VZPointingDeviceConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/pointingdevices)
- [var usbControllers: [VZUSBControllerConfiguration]](/documentation/virtualization/vzvirtualmachineconfiguration/usbcontrollers)

#### Validating the configuration

- [func validate() throws](/documentation/virtualization/vzvirtualmachineconfiguration/validate())
- [func validateSaveRestoreSupport() throws](/documentation/virtualization/vzvirtualmachineconfiguration/validatesaverestoresupport())
- [VZVirtualMachineStartOptions](/documentation/virtualization/vzvirtualmachinestartoptions)
- [VZGenericPlatformConfiguration](/documentation/virtualization/vzgenericplatformconfiguration)

#### Creating a platform configuration

- [init()](/documentation/virtualization/vzgenericplatformconfiguration/init())

#### Identifying the platform configuration

- [var machineIdentifier: VZGenericMachineIdentifier](/documentation/virtualization/vzgenericplatformconfiguration/machineidentifier)
- [var isNestedVirtualizationEnabled: Bool](/documentation/virtualization/vzgenericplatformconfiguration/isnestedvirtualizationenabled)
- [class var isNestedVirtualizationSupported: Bool](/documentation/virtualization/vzgenericplatformconfiguration/isnestedvirtualizationsupported)
- [VZGenericMachineIdentifier](/documentation/virtualization/vzgenericmachineidentifier)

##### Creating a Machine Identifier

- [init()](/documentation/virtualization/vzgenericmachineidentifier/init())
- [init?(dataRepresentation: Data)](/documentation/virtualization/vzgenericmachineidentifier/init(datarepresentation:))

##### Getting Information About the Machine Identifier

- [var dataRepresentation: Data](/documentation/virtualization/vzgenericmachineidentifier/datarepresentation)
- [VZPlatformConfiguration](/documentation/virtualization/vzplatformconfiguration)

### Boot loaders

- [VZBootLoader](/documentation/virtualization/vzbootloader)
- [VZLinuxBootLoader](/documentation/virtualization/vzlinuxbootloader)

#### Creating the Linux boot loader

- [init(kernelURL: URL)](/documentation/virtualization/vzlinuxbootloader/init(kernelurl:))

#### Configuring the boot parameters

- [var commandLine: String](/documentation/virtualization/vzlinuxbootloader/commandline)
- [var initialRamdiskURL: URL?](/documentation/virtualization/vzlinuxbootloader/initialramdiskurl)

#### Getting the kernel file

- [var kernelURL: URL](/documentation/virtualization/vzlinuxbootloader/kernelurl)
- [VZEFIBootLoader](/documentation/virtualization/vzefibootloader)

#### Creating an EFI boot loader

- [init()](/documentation/virtualization/vzefibootloader/init())

#### Instance properties

- [var variableStore: VZEFIVariableStore?](/documentation/virtualization/vzefibootloader/variablestore)
- [VZEFIVariableStore](/documentation/virtualization/vzefivariablestore)

#### Creating the variable store

- [init(creatingVariableStoreAt: URL, options: VZEFIVariableStore.InitializationOptions) throws](/documentation/virtualization/vzefivariablestore/init(creatingvariablestoreat:options:))
- [init(url: URL)](/documentation/virtualization/vzefivariablestore/init(url:))
- [VZEFIVariableStore.InitializationOptions](/documentation/virtualization/vzefivariablestore/initializationoptions)

##### Creating an EFI initialization store

- [init(rawValue: UInt)](/documentation/virtualization/vzefivariablestore/initializationoptions/init(rawvalue:))

##### Constants that control overwriting

- [static var allowOverwrite: VZEFIVariableStore.InitializationOptions](/documentation/virtualization/vzefivariablestore/initializationoptions/allowoverwrite)
- [static var allowOverwrite: VZEFIVariableStore.InitializationOptions](/documentation/virtualization/vzefivariablestore/initializationoptions/allowoverwrite)

#### Instance properties

- [var url: URL](/documentation/virtualization/vzefivariablestore/url)
- [Running Intel Binaries in Linux VMs with Rosetta](/documentation/virtualization/running-intel-binaries-in-linux-vms-with-rosetta)
- [Accelerating the performance of Rosetta](/documentation/virtualization/accelerating-the-performance-of-rosetta)

## Runtime

- [VZVirtualMachine](/documentation/virtualization/vzvirtualmachine)

### Creating the VM

- [convenience init(configuration: VZVirtualMachineConfiguration)](/documentation/virtualization/vzvirtualmachine/init(configuration:))
- [init(configuration: VZVirtualMachineConfiguration, queue: dispatch_queue_t)](/documentation/virtualization/vzvirtualmachine/init(configuration:queue:))
- [class var isSupported: Bool](/documentation/virtualization/vzvirtualmachine/issupported)

### Responding to a stopped VM

- [var delegate: (any VZVirtualMachineDelegate)?](/documentation/virtualization/vzvirtualmachine/delegate)
- [VZVirtualMachineDelegate](/documentation/virtualization/vzvirtualmachinedelegate)

#### Stopping the VM

- [func guestDidStop(VZVirtualMachine)](/documentation/virtualization/vzvirtualmachinedelegate/guestdidstop(_:))
- [func virtualMachine(VZVirtualMachine, didStopWithError: any Error)](/documentation/virtualization/vzvirtualmachinedelegate/virtualmachine(_:didstopwitherror:))

#### Responding to network device errors

- [func virtualMachine(VZVirtualMachine, networkDevice: VZNetworkDevice, attachmentWasDisconnectedWithError: any Error)](/documentation/virtualization/vzvirtualmachinedelegate/virtualmachine(_:networkdevice:attachmentwasdisconnectedwitherror:))

### Starting and stopping the VM

- [func start(completionHandler: (Result<Void, any Error>) -> Void)](/documentation/virtualization/vzvirtualmachine/start(completionhandler:))
- [func start() async throws](/documentation/virtualization/vzvirtualmachine/start())
- [func start(options: VZVirtualMachineStartOptions, completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzvirtualmachine/start(options:completionhandler:))
- [func stop(completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzvirtualmachine/stop(completionhandler:))
- [func pause(completionHandler: (Result<Void, any Error>) -> Void)](/documentation/virtualization/vzvirtualmachine/pause(completionhandler:))
- [func requestStop() throws](/documentation/virtualization/vzvirtualmachine/requeststop())
- [func resume(completionHandler: (Result<Void, any Error>) -> Void)](/documentation/virtualization/vzvirtualmachine/resume(completionhandler:))
- [func pause() async throws](/documentation/virtualization/vzvirtualmachine/pause())
- [func resume() async throws](/documentation/virtualization/vzvirtualmachine/resume())
- [VZVirtualMachineStartOptions](/documentation/virtualization/vzvirtualmachinestartoptions)

### Configuring VM attributes at runtime

- [var consoleDevices: [VZConsoleDevice]](/documentation/virtualization/vzvirtualmachine/consoledevices)
- [var memoryBalloonDevices: [VZMemoryBalloonDevice]](/documentation/virtualization/vzvirtualmachine/memoryballoondevices)
- [var networkDevices: [VZNetworkDevice]](/documentation/virtualization/vzvirtualmachine/networkdevices)
- [var socketDevices: [VZSocketDevice]](/documentation/virtualization/vzvirtualmachine/socketdevices)
- [var directorySharingDevices: [VZDirectorySharingDevice]](/documentation/virtualization/vzvirtualmachine/directorysharingdevices)
- [var usbControllers: [VZUSBController]](/documentation/virtualization/vzvirtualmachine/usbcontrollers)

### Getting the state of the VM

- [var state: VZVirtualMachine.State](/documentation/virtualization/vzvirtualmachine/state-swift.property)
- [VZVirtualMachine.State](/documentation/virtualization/vzvirtualmachine/state-swift.enum)

#### States

- [case stopped](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopped)
- [case running](/documentation/virtualization/vzvirtualmachine/state-swift.enum/running)
- [case paused](/documentation/virtualization/vzvirtualmachine/state-swift.enum/paused)
- [case error](/documentation/virtualization/vzvirtualmachine/state-swift.enum/error)
- [case starting](/documentation/virtualization/vzvirtualmachine/state-swift.enum/starting)
- [case pausing](/documentation/virtualization/vzvirtualmachine/state-swift.enum/pausing)
- [case stopping](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopping)
- [case resuming](/documentation/virtualization/vzvirtualmachine/state-swift.enum/resuming)
- [case restoring](/documentation/virtualization/vzvirtualmachine/state-swift.enum/restoring)
- [case saving](/documentation/virtualization/vzvirtualmachine/state-swift.enum/saving)
- [case stopped](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopped)
- [case running](/documentation/virtualization/vzvirtualmachine/state-swift.enum/running)
- [case paused](/documentation/virtualization/vzvirtualmachine/state-swift.enum/paused)
- [case error](/documentation/virtualization/vzvirtualmachine/state-swift.enum/error)
- [case starting](/documentation/virtualization/vzvirtualmachine/state-swift.enum/starting)
- [case pausing](/documentation/virtualization/vzvirtualmachine/state-swift.enum/pausing)
- [case stopping](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopping)
- [case resuming](/documentation/virtualization/vzvirtualmachine/state-swift.enum/resuming)
- [case restoring](/documentation/virtualization/vzvirtualmachine/state-swift.enum/restoring)
- [case saving](/documentation/virtualization/vzvirtualmachine/state-swift.enum/saving)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzvirtualmachine/state-swift.enum/init(rawvalue:))
- [var graphicsDevices: [VZGraphicsDevice]](/documentation/virtualization/vzvirtualmachine/graphicsdevices)
- [var canStart: Bool](/documentation/virtualization/vzvirtualmachine/canstart)
- [var canPause: Bool](/documentation/virtualization/vzvirtualmachine/canpause)
- [var canResume: Bool](/documentation/virtualization/vzvirtualmachine/canresume)
- [var canStop: Bool](/documentation/virtualization/vzvirtualmachine/canstop)
- [var canRequestStop: Bool](/documentation/virtualization/vzvirtualmachine/canrequeststop)
- [var queue: dispatch_queue_t](/documentation/virtualization/vzvirtualmachine/queue)

### Saving and restoring the VM state

- [func saveMachineStateTo(url: URL, completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzvirtualmachine/savemachinestateto(url:completionhandler:))
- [func restoreMachineStateFrom(url: URL, completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzvirtualmachine/restoremachinestatefrom(url:completionhandler:))
- [VZVirtualMachineView](/documentation/virtualization/vzvirtualmachineview)

### Configuring the VM

- [var automaticallyReconfiguresDisplay: Bool](/documentation/virtualization/vzvirtualmachineview/automaticallyreconfiguresdisplay)
- [var capturesSystemKeys: Bool](/documentation/virtualization/vzvirtualmachineview/capturessystemkeys)
- [var virtualMachine: VZVirtualMachine?](/documentation/virtualization/vzvirtualmachineview/virtualmachine)
- [VZLinuxRosettaDirectoryShare](/documentation/virtualization/vzlinuxrosettadirectoryshare)

### Creating a Rosetta directory share

- [init() throws](/documentation/virtualization/vzlinuxrosettadirectoryshare/init())

### Checking Rosetta availability

- [class var availability: VZLinuxRosettaAvailability](/documentation/virtualization/vzlinuxrosettadirectoryshare/availability)
- [VZLinuxRosettaAvailability](/documentation/virtualization/vzlinuxrosettaavailability)

#### Rosetta availability states

- [case notSupported](/documentation/virtualization/vzlinuxrosettaavailability/notsupported)
- [case notInstalled](/documentation/virtualization/vzlinuxrosettaavailability/notinstalled)
- [case installed](/documentation/virtualization/vzlinuxrosettaavailability/installed)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzlinuxrosettaavailability/init(rawvalue:))

### Installing Rosetta

- [class func installRosetta(completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzlinuxrosettadirectoryshare/installrosetta(completionhandler:))

### Setting the ahead of time (AOT) caching options

- [var cachingOptions: VZLinuxRosettaDirectoryShare.CachingOptions?](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.property)
- [func setCachingOptions(VZLinuxRosettaDirectoryShare.CachingOptions?) throws](/documentation/virtualization/vzlinuxrosettadirectoryshare/setcachingoptions(_:))
- [VZLinuxRosettaDirectoryShare.CachingOptions](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum)

#### Socket types

- [case abstractSocket(String)](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/abstractsocket(_:))
- [case unixSocket(String)](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/unixsocket(_:))

#### Type properties

- [static var defaultUnixSocket: VZLinuxRosettaDirectoryShare.CachingOptions](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/defaultunixsocket)
- [static var maximumNameLength: Int](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/maximumnamelength)
- [static var maximumPathLength: Int](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/maximumpathlength)

## Devices

- [Audio](/documentation/virtualization/audio)

### Configurations

- [VZVirtioSoundDeviceConfiguration](/documentation/virtualization/vzvirtiosounddeviceconfiguration)

#### Creating a sound device configuration

- [init()](/documentation/virtualization/vzvirtiosounddeviceconfiguration/init())

#### Accessing the sound streams

- [var streams: [VZVirtioSoundDeviceStreamConfiguration]](/documentation/virtualization/vzvirtiosounddeviceconfiguration/streams)
- [VZVirtioSoundDeviceOutputStreamConfiguration](/documentation/virtualization/vzvirtiosounddeviceoutputstreamconfiguration)

#### Creating an output stream configuration

- [init()](/documentation/virtualization/vzvirtiosounddeviceoutputstreamconfiguration/init())

#### Accessing the sound sink

- [var sink: VZAudioOutputStreamSink?](/documentation/virtualization/vzvirtiosounddeviceoutputstreamconfiguration/sink)

#### Output sink

- [VZHostAudioOutputStreamSink](/documentation/virtualization/vzhostaudiooutputstreamsink)

##### Creating the audio output stream sink

- [init()](/documentation/virtualization/vzhostaudiooutputstreamsink/init())
- [VZAudioOutputStreamSink](/documentation/virtualization/vzaudiooutputstreamsink)
- [VZVirtioSoundDeviceInputStreamConfiguration](/documentation/virtualization/vzvirtiosounddeviceinputstreamconfiguration)

#### Creating an input stream configuration

- [init()](/documentation/virtualization/vzvirtiosounddeviceinputstreamconfiguration/init())

#### Accessing the sound source

- [var source: VZAudioInputStreamSource?](/documentation/virtualization/vzvirtiosounddeviceinputstreamconfiguration/source)

#### Input source

- [VZHostAudioInputStreamSource](/documentation/virtualization/vzhostaudioinputstreamsource)

##### Creating the audio input stream source

- [init()](/documentation/virtualization/vzhostaudioinputstreamsource/init())
- [VZAudioInputStreamSource](/documentation/virtualization/vzaudioinputstreamsource)
- [VZAudioDeviceConfiguration](/documentation/virtualization/vzaudiodeviceconfiguration)
- [VZVirtioSoundDeviceStreamConfiguration](/documentation/virtualization/vzvirtiosounddevicestreamconfiguration)

### Audio streams

- [VZHostAudioOutputStreamSink](/documentation/virtualization/vzhostaudiooutputstreamsink)

#### Creating the audio output stream sink

- [init()](/documentation/virtualization/vzhostaudiooutputstreamsink/init())
- [VZHostAudioInputStreamSource](/documentation/virtualization/vzhostaudioinputstreamsource)

#### Creating the audio input stream source

- [init()](/documentation/virtualization/vzhostaudioinputstreamsource/init())
- [VZAudioOutputStreamSink](/documentation/virtualization/vzaudiooutputstreamsink)
- [VZAudioInputStreamSource](/documentation/virtualization/vzaudioinputstreamsource)
- [Graphics](/documentation/virtualization/graphics)

### Configurations

- [VZGraphicsDisplayConfiguration](/documentation/virtualization/vzgraphicsdisplayconfiguration)
- [VZMacGraphicsDeviceConfiguration](/documentation/virtualization/vzmacgraphicsdeviceconfiguration)

#### Creating the graphics device configuration

- [init()](/documentation/virtualization/vzmacgraphicsdeviceconfiguration/init())

#### Configuring displays

- [var displays: [VZMacGraphicsDisplayConfiguration]](/documentation/virtualization/vzmacgraphicsdeviceconfiguration/displays)
- [VZMacGraphicsDisplayConfiguration](/documentation/virtualization/vzmacgraphicsdisplayconfiguration)

#### Creating the display configuration

- [convenience init(for: NSScreen, sizeInPoints: NSSize)](/documentation/virtualization/vzmacgraphicsdisplayconfiguration/init(for:sizeinpoints:))
- [init(widthInPixels: Int, heightInPixels: Int, pixelsPerInch: Int)](/documentation/virtualization/vzmacgraphicsdisplayconfiguration/init(widthinpixels:heightinpixels:pixelsperinch:))

#### Configuring the display properties

- [var heightInPixels: Int](/documentation/virtualization/vzmacgraphicsdisplayconfiguration/heightinpixels)
- [var widthInPixels: Int](/documentation/virtualization/vzmacgraphicsdisplayconfiguration/widthinpixels)
- [var pixelsPerInch: Int](/documentation/virtualization/vzmacgraphicsdisplayconfiguration/pixelsperinch)
- [VZGraphicsDeviceConfiguration](/documentation/virtualization/vzgraphicsdeviceconfiguration)
- [VZVirtioGraphicsDeviceConfiguration](/documentation/virtualization/vzvirtiographicsdeviceconfiguration)

#### Creating the configuration object

- [init()](/documentation/virtualization/vzvirtiographicsdeviceconfiguration/init())

#### Instance properties

- [var scanouts: [VZVirtioGraphicsScanoutConfiguration]](/documentation/virtualization/vzvirtiographicsdeviceconfiguration/scanouts)
- [VZVirtioGraphicsScanoutConfiguration](/documentation/virtualization/vzvirtiographicsscanoutconfiguration)

##### Creating the configuration object

- [init(widthInPixels: Int, heightInPixels: Int)](/documentation/virtualization/vzvirtiographicsscanoutconfiguration/init(widthinpixels:heightinpixels:))

##### Instance properties

- [var heightInPixels: Int](/documentation/virtualization/vzvirtiographicsscanoutconfiguration/heightinpixels)
- [var widthInPixels: Int](/documentation/virtualization/vzvirtiographicsscanoutconfiguration/widthinpixels)

### Devices

- [VZGraphicsDevice](/documentation/virtualization/vzgraphicsdevice)

#### Getting the device’s displays

- [var displays: [VZGraphicsDisplay]](/documentation/virtualization/vzgraphicsdevice/displays)
- [VZGraphicsDisplay](/documentation/virtualization/vzgraphicsdisplay)

#### Getting the display size

- [var sizeInPixels: CGSize](/documentation/virtualization/vzgraphicsdisplay/sizeinpixels)

#### Observing changes to the display configuration

- [func addObserver(any VZGraphicsDisplayObserver)](/documentation/virtualization/vzgraphicsdisplay/addobserver(_:))
- [func removeObserver(any VZGraphicsDisplayObserver)](/documentation/virtualization/vzgraphicsdisplay/removeobserver(_:))
- [VZGraphicsDisplayObserver](/documentation/virtualization/vzgraphicsdisplayobserver)

##### Reacting to changes in display configuration

- [func displayDidBeginReconfiguration(VZGraphicsDisplay)](/documentation/virtualization/vzgraphicsdisplayobserver/displaydidbeginreconfiguration(_:))
- [func displayDidEndReconfiguration(VZGraphicsDisplay)](/documentation/virtualization/vzgraphicsdisplayobserver/displaydidendreconfiguration(_:))

#### Changing the display configuration

- [func reconfigure(sizeInPixels: CGSize) throws](/documentation/virtualization/vzgraphicsdisplay/reconfigure(sizeinpixels:))
- [func reconfigure(configuration: VZGraphicsDisplayConfiguration) throws](/documentation/virtualization/vzgraphicsdisplay/reconfigure(configuration:))
- [VZMacGraphicsDevice](/documentation/virtualization/vzmacgraphicsdevice)
- [VZVirtioGraphicsScanout](/documentation/virtualization/vzvirtiographicsscanout)
- [VZMacGraphicsDisplay](/documentation/virtualization/vzmacgraphicsdisplay)

#### Getting the display’s pixel density

- [var pixelsPerInch: Int](/documentation/virtualization/vzmacgraphicsdisplay/pixelsperinch)
- [VZVirtioGraphicsDevice](/documentation/virtualization/vzvirtiographicsdevice)
- [Keyboards and pointing devices](/documentation/virtualization/keyboards-and-pointing-devices)

### Keyboards

- [VZKeyboardConfiguration](/documentation/virtualization/vzkeyboardconfiguration)
- [VZMacKeyboardConfiguration](/documentation/virtualization/vzmackeyboardconfiguration)

#### Creating a new Mac keyboard configuration

- [init()](/documentation/virtualization/vzmackeyboardconfiguration/init())
- [VZUSBKeyboardConfiguration](/documentation/virtualization/vzusbkeyboardconfiguration)

#### Creating a USB keyboard

- [init()](/documentation/virtualization/vzusbkeyboardconfiguration/init())

### Pointing devices

- [VZMacTrackpadConfiguration](/documentation/virtualization/vzmactrackpadconfiguration)

#### Initializers

- [init()](/documentation/virtualization/vzmactrackpadconfiguration/init())
- [VZUSBScreenCoordinatePointingDeviceConfiguration](/documentation/virtualization/vzusbscreencoordinatepointingdeviceconfiguration)

#### Creating pointing devices

- [init()](/documentation/virtualization/vzusbscreencoordinatepointingdeviceconfiguration/init())
- [VZPointingDeviceConfiguration](/documentation/virtualization/vzpointingdeviceconfiguration)
- [Memory](/documentation/virtualization/memory)

### Configuration

- [VZVirtioTraditionalMemoryBalloonDeviceConfiguration](/documentation/virtualization/vzvirtiotraditionalmemoryballoondeviceconfiguration)

#### Creating the Configuration Object

- [init()](/documentation/virtualization/vzvirtiotraditionalmemoryballoondeviceconfiguration/init())
- [VZMemoryBalloonDeviceConfiguration](/documentation/virtualization/vzmemoryballoondeviceconfiguration)

### Memory balloon devices

- [VZVirtioTraditionalMemoryBalloonDevice](/documentation/virtualization/vzvirtiotraditionalmemoryballoondevice)

#### Changing the memory partition size

- [var targetVirtualMachineMemorySize: UInt64](/documentation/virtualization/vzvirtiotraditionalmemoryballoondevice/targetvirtualmachinememorysize)
- [VZMemoryBalloonDevice](/documentation/virtualization/vzmemoryballoondevice)
- [Network](/documentation/virtualization/network)

### Configurations

- [VZVirtioNetworkDeviceConfiguration](/documentation/virtualization/vzvirtionetworkdeviceconfiguration)

#### Creating the configuration object

- [init()](/documentation/virtualization/vzvirtionetworkdeviceconfiguration/init())
- [VZNetworkDeviceConfiguration](/documentation/virtualization/vznetworkdeviceconfiguration)

#### Setting configuration attributes

- [var attachment: VZNetworkDeviceAttachment?](/documentation/virtualization/vznetworkdeviceconfiguration/attachment)
- [var macAddress: VZMACAddress](/documentation/virtualization/vznetworkdeviceconfiguration/macaddress)
- [VZMACAddress](/documentation/virtualization/vzmacaddress)

#### Creating a MAC address

- [class func randomLocallyAdministered() -> Self](/documentation/virtualization/vzmacaddress/randomlocallyadministered())
- [convenience init?(string: String)](/documentation/virtualization/vzmacaddress/init(string:))
- [init(ethernetAddress: ether_addr_t)](/documentation/virtualization/vzmacaddress/init(ethernetaddress:))

#### Getting the address

- [var string: String](/documentation/virtualization/vzmacaddress/string)
- [var ethernetAddress: ether_addr_t](/documentation/virtualization/vzmacaddress/ethernetaddress)

#### Getting address attributes

- [var isBroadcastAddress: Bool](/documentation/virtualization/vzmacaddress/isbroadcastaddress)
- [var isMulticastAddress: Bool](/documentation/virtualization/vzmacaddress/ismulticastaddress)
- [var isUnicastAddress: Bool](/documentation/virtualization/vzmacaddress/isunicastaddress)
- [var isLocallyAdministeredAddress: Bool](/documentation/virtualization/vzmacaddress/islocallyadministeredaddress)
- [var isUniversallyAdministeredAddress: Bool](/documentation/virtualization/vzmacaddress/isuniversallyadministeredaddress)

### Attachment points

- [VZBridgedNetworkDeviceAttachment](/documentation/virtualization/vzbridgednetworkdeviceattachment)

#### Creating the attachment point

- [init(interface: VZBridgedNetworkInterface)](/documentation/virtualization/vzbridgednetworkdeviceattachment/init(interface:))

#### Getting the network interface

- [var interface: VZBridgedNetworkInterface](/documentation/virtualization/vzbridgednetworkdeviceattachment/interface)
- [VZFileHandleNetworkDeviceAttachment](/documentation/virtualization/vzfilehandlenetworkdeviceattachment)

#### Creating the attachment point

- [init(fileHandle: FileHandle)](/documentation/virtualization/vzfilehandlenetworkdeviceattachment/init(filehandle:))

#### Getting the file handle

- [var fileHandle: FileHandle](/documentation/virtualization/vzfilehandlenetworkdeviceattachment/filehandle)

#### Specifying the network packet size

- [var maximumTransmissionUnit: Int](/documentation/virtualization/vzfilehandlenetworkdeviceattachment/maximumtransmissionunit)
- [VZNATNetworkDeviceAttachment](/documentation/virtualization/vznatnetworkdeviceattachment)

#### Creating the Attachment Point

- [init()](/documentation/virtualization/vznatnetworkdeviceattachment/init())
- [VZVmnetNetworkDeviceAttachment](/documentation/virtualization/vzvmnetnetworkdeviceattachment)

#### Creating the vmnet network device attachment

- [init(network: vmnet_network_ref)](/documentation/virtualization/vzvmnetnetworkdeviceattachment/init(network:))
- [var network: vmnet_network_ref](/documentation/virtualization/vzvmnetnetworkdeviceattachment/network)
- [VZNetworkDeviceAttachment](/documentation/virtualization/vznetworkdeviceattachment)

### Hardware interfaces

- [VZBridgedNetworkInterface](/documentation/virtualization/vzbridgednetworkinterface)

#### Getting the available interfaces

- [class var networkInterfaces: [VZBridgedNetworkInterface]](/documentation/virtualization/vzbridgednetworkinterface/networkinterfaces)

#### Getting the interface description

- [var identifier: String](/documentation/virtualization/vzbridgednetworkinterface/identifier)
- [var localizedDisplayName: String?](/documentation/virtualization/vzbridgednetworkinterface/localizeddisplayname)

### Devices

- [VZNetworkDevice](/documentation/virtualization/vznetworkdevice)

#### Getting the network attachment point

- [var attachment: VZNetworkDeviceAttachment?](/documentation/virtualization/vznetworkdevice/attachment)
- [Randomization](/documentation/virtualization/randomization)

### Configurations

- [VZVirtioEntropyDeviceConfiguration](/documentation/virtualization/vzvirtioentropydeviceconfiguration)

#### Creating the configuration object

- [init()](/documentation/virtualization/vzvirtioentropydeviceconfiguration/init())
- [VZEntropyDeviceConfiguration](/documentation/virtualization/vzentropydeviceconfiguration)
- [Serial ports](/documentation/virtualization/serial-ports)

### Configurations

- [VZVirtioConsoleDeviceSerialPortConfiguration](/documentation/virtualization/vzvirtioconsoledeviceserialportconfiguration)

#### Creating the Configuration Object

- [init()](/documentation/virtualization/vzvirtioconsoledeviceserialportconfiguration/init())
- [VZSerialPortConfiguration](/documentation/virtualization/vzserialportconfiguration)

#### Configuring the Attachment Point

- [var attachment: VZSerialPortAttachment?](/documentation/virtualization/vzserialportconfiguration/attachment)

### Attachment points

- [VZFileHandleSerialPortAttachment](/documentation/virtualization/vzfilehandleserialportattachment)

#### Creating the attachment point

- [init(fileHandleForReading: FileHandle?, fileHandleForWriting: FileHandle?)](/documentation/virtualization/vzfilehandleserialportattachment/init(filehandleforreading:filehandleforwriting:))

#### Getting the file handles

- [var fileHandleForReading: FileHandle?](/documentation/virtualization/vzfilehandleserialportattachment/filehandleforreading)
- [var fileHandleForWriting: FileHandle?](/documentation/virtualization/vzfilehandleserialportattachment/filehandleforwriting)
- [VZFileSerialPortAttachment](/documentation/virtualization/vzfileserialportattachment)

#### Creating the attachment point

- [init(url: URL, append: Bool) throws](/documentation/virtualization/vzfileserialportattachment/init(url:append:))

#### Getting the file details

- [var url: URL](/documentation/virtualization/vzfileserialportattachment/url)
- [var append: Bool](/documentation/virtualization/vzfileserialportattachment/append)
- [VZSerialPortAttachment](/documentation/virtualization/vzserialportattachment)
- [Shared directories](/documentation/virtualization/shared-directories)

### Configurations

- [VZVirtioFileSystemDeviceConfiguration](/documentation/virtualization/vzvirtiofilesystemdeviceconfiguration)

#### Creating a file system device configuration

- [init(tag: String)](/documentation/virtualization/vzvirtiofilesystemdeviceconfiguration/init(tag:))

#### Getting file system information

- [var share: VZDirectoryShare?](/documentation/virtualization/vzvirtiofilesystemdeviceconfiguration/share)
- [var tag: String](/documentation/virtualization/vzvirtiofilesystemdeviceconfiguration/tag)
- [class var macOSGuestAutomountTag: String](/documentation/virtualization/vzvirtiofilesystemdeviceconfiguration/macosguestautomounttag)

#### Tag validation

- [class func validateTag(String) throws](/documentation/virtualization/vzvirtiofilesystemdeviceconfiguration/validatetag(_:))
- [VZDirectorySharingDeviceConfiguration](/documentation/virtualization/vzdirectorysharingdeviceconfiguration)
- [VZLinuxRosettaDirectoryShare](/documentation/virtualization/vzlinuxrosettadirectoryshare)

#### Creating a Rosetta directory share

- [init() throws](/documentation/virtualization/vzlinuxrosettadirectoryshare/init())

#### Checking Rosetta availability

- [class var availability: VZLinuxRosettaAvailability](/documentation/virtualization/vzlinuxrosettadirectoryshare/availability)
- [VZLinuxRosettaAvailability](/documentation/virtualization/vzlinuxrosettaavailability)

##### Rosetta availability states

- [case notSupported](/documentation/virtualization/vzlinuxrosettaavailability/notsupported)
- [case notInstalled](/documentation/virtualization/vzlinuxrosettaavailability/notinstalled)
- [case installed](/documentation/virtualization/vzlinuxrosettaavailability/installed)

##### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzlinuxrosettaavailability/init(rawvalue:))

#### Installing Rosetta

- [class func installRosetta(completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzlinuxrosettadirectoryshare/installrosetta(completionhandler:))

#### Setting the ahead of time (AOT) caching options

- [var cachingOptions: VZLinuxRosettaDirectoryShare.CachingOptions?](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.property)
- [func setCachingOptions(VZLinuxRosettaDirectoryShare.CachingOptions?) throws](/documentation/virtualization/vzlinuxrosettadirectoryshare/setcachingoptions(_:))
- [VZLinuxRosettaDirectoryShare.CachingOptions](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum)

##### Socket types

- [case abstractSocket(String)](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/abstractsocket(_:))
- [case unixSocket(String)](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/unixsocket(_:))

##### Type properties

- [static var defaultUnixSocket: VZLinuxRosettaDirectoryShare.CachingOptions](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/defaultunixsocket)
- [static var maximumNameLength: Int](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/maximumnamelength)
- [static var maximumPathLength: Int](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/maximumpathlength)

### Shared directory devices

- [VZVirtioFileSystemDevice](/documentation/virtualization/vzvirtiofilesystemdevice)

#### Accessing directory properties

- [var share: VZDirectoryShare?](/documentation/virtualization/vzvirtiofilesystemdevice/share)
- [var tag: String](/documentation/virtualization/vzvirtiofilesystemdevice/tag)
- [VZDirectorySharingDevice](/documentation/virtualization/vzdirectorysharingdevice)

### Directory Shares

- [VZMultipleDirectoryShare](/documentation/virtualization/vzmultipledirectoryshare)

#### Creating a directory share

- [convenience init()](/documentation/virtualization/vzmultipledirectoryshare/init())
- [init(directories: [String : VZSharedDirectory])](/documentation/virtualization/vzmultipledirectoryshare/init(directories:))

#### Accessing the shared directories

- [var directories: [String : VZSharedDirectory]](/documentation/virtualization/vzmultipledirectoryshare/directories)

#### Directory name utility methods

- [class func canonicalizedName(from: String) -> String?](/documentation/virtualization/vzmultipledirectoryshare/canonicalizedname(from:))
- [class func validateName(String) throws](/documentation/virtualization/vzmultipledirectoryshare/validatename(_:))
- [VZSingleDirectoryShare](/documentation/virtualization/vzsingledirectoryshare)

#### Creating a directory share

- [init(directory: VZSharedDirectory)](/documentation/virtualization/vzsingledirectoryshare/init(directory:))

#### Accessing directory properties

- [var directory: VZSharedDirectory](/documentation/virtualization/vzsingledirectoryshare/directory)
- [VZSharedDirectory](/documentation/virtualization/vzshareddirectory)

#### Creating a Shared Directory

- [init(url: URL, readOnly: Bool)](/documentation/virtualization/vzshareddirectory/init(url:readonly:))

#### Accessing Directory Properties

- [var url: URL](/documentation/virtualization/vzshareddirectory/url)
- [var isReadOnly: Bool](/documentation/virtualization/vzshareddirectory/isreadonly)
- [VZDirectoryShare](/documentation/virtualization/vzdirectoryshare)
- [VZLinuxRosettaDirectoryShare](/documentation/virtualization/vzlinuxrosettadirectoryshare)

#### Creating a Rosetta directory share

- [init() throws](/documentation/virtualization/vzlinuxrosettadirectoryshare/init())

#### Checking Rosetta availability

- [class var availability: VZLinuxRosettaAvailability](/documentation/virtualization/vzlinuxrosettadirectoryshare/availability)
- [VZLinuxRosettaAvailability](/documentation/virtualization/vzlinuxrosettaavailability)

##### Rosetta availability states

- [case notSupported](/documentation/virtualization/vzlinuxrosettaavailability/notsupported)
- [case notInstalled](/documentation/virtualization/vzlinuxrosettaavailability/notinstalled)
- [case installed](/documentation/virtualization/vzlinuxrosettaavailability/installed)

##### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzlinuxrosettaavailability/init(rawvalue:))

#### Installing Rosetta

- [class func installRosetta(completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzlinuxrosettadirectoryshare/installrosetta(completionhandler:))

#### Setting the ahead of time (AOT) caching options

- [var cachingOptions: VZLinuxRosettaDirectoryShare.CachingOptions?](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.property)
- [func setCachingOptions(VZLinuxRosettaDirectoryShare.CachingOptions?) throws](/documentation/virtualization/vzlinuxrosettadirectoryshare/setcachingoptions(_:))
- [VZLinuxRosettaDirectoryShare.CachingOptions](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum)

##### Socket types

- [case abstractSocket(String)](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/abstractsocket(_:))
- [case unixSocket(String)](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/unixsocket(_:))

##### Type properties

- [static var defaultUnixSocket: VZLinuxRosettaDirectoryShare.CachingOptions](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/defaultunixsocket)
- [static var maximumNameLength: Int](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/maximumnamelength)
- [static var maximumPathLength: Int](/documentation/virtualization/vzlinuxrosettadirectoryshare/cachingoptions-swift.enum/maximumpathlength)
- [Sockets](/documentation/virtualization/sockets)

### Configurations

- [VZVirtioSocketDeviceConfiguration](/documentation/virtualization/vzvirtiosocketdeviceconfiguration)

#### Creating the Configuration Object

- [init()](/documentation/virtualization/vzvirtiosocketdeviceconfiguration/init())
- [VZSocketDeviceConfiguration](/documentation/virtualization/vzsocketdeviceconfiguration)

### Devices

- [VZVirtioSocketDevice](/documentation/virtualization/vzvirtiosocketdevice)

#### Configuring Port Listeners

- [func setSocketListener(VZVirtioSocketListener, forPort: UInt32)](/documentation/virtualization/vzvirtiosocketdevice/setsocketlistener(_:forport:))
- [func removeSocketListener(forPort: UInt32)](/documentation/virtualization/vzvirtiosocketdevice/removesocketlistener(forport:))

#### Connecting to Guest System Ports

- [func connect(toPort: UInt32, completionHandler: (Result<VZVirtioSocketConnection, any Error>) -> Void)](/documentation/virtualization/vzvirtiosocketdevice/connect(toport:completionhandler:))
- [func connect(toPort: UInt32) async throws -> VZVirtioSocketConnection](/documentation/virtualization/vzvirtiosocketdevice/connect(toport:))
- [VZSocketDevice](/documentation/virtualization/vzsocketdevice)

### Connection management

- [VZVirtioSocketListener](/documentation/virtualization/vzvirtiosocketlistener)

#### Responding to new connections

- [var delegate: (any VZVirtioSocketListenerDelegate)?](/documentation/virtualization/vzvirtiosocketlistener/delegate)
- [VZVirtioSocketListenerDelegate](/documentation/virtualization/vzvirtiosocketlistenerdelegate)

##### Accepting new connections

- [func listener(VZVirtioSocketListener, shouldAcceptNewConnection: VZVirtioSocketConnection, from: VZVirtioSocketDevice) -> Bool](/documentation/virtualization/vzvirtiosocketlistenerdelegate/listener(_:shouldacceptnewconnection:from:))
- [VZVirtioSocketConnection](/documentation/virtualization/vzvirtiosocketconnection)

#### Getting the connection details

- [var sourcePort: UInt32](/documentation/virtualization/vzvirtiosocketconnection/sourceport)
- [var destinationPort: UInt32](/documentation/virtualization/vzvirtiosocketconnection/destinationport)
- [var fileDescriptor: Int32](/documentation/virtualization/vzvirtiosocketconnection/filedescriptor)

#### Closing the connection

- [func close()](/documentation/virtualization/vzvirtiosocketconnection/close())
- [Storage](/documentation/virtualization/storage)

### Configurations

- [VZVirtioBlockDeviceConfiguration](/documentation/virtualization/vzvirtioblockdeviceconfiguration)

#### Creating the configuration object

- [init(attachment: VZStorageDeviceAttachment)](/documentation/virtualization/vzvirtioblockdeviceconfiguration/init(attachment:))

#### Identifying a block device

- [var blockDeviceIdentifier: String](/documentation/virtualization/vzvirtioblockdeviceconfiguration/blockdeviceidentifier)

#### Validating device identifiers

- [class func validateBlockDeviceIdentifier(String) throws](/documentation/virtualization/vzvirtioblockdeviceconfiguration/validateblockdeviceidentifier(_:))
- [VZStorageDeviceConfiguration](/documentation/virtualization/vzstoragedeviceconfiguration)

#### Getting the attachment point

- [var attachment: VZStorageDeviceAttachment](/documentation/virtualization/vzstoragedeviceconfiguration/attachment)
- [VZUSBMassStorageDeviceConfiguration](/documentation/virtualization/vzusbmassstoragedeviceconfiguration)

#### Creating the configuration object

- [init(attachment: VZStorageDeviceAttachment)](/documentation/virtualization/vzusbmassstoragedeviceconfiguration/init(attachment:))
- [VZDiskImageCachingMode](/documentation/virtualization/vzdiskimagecachingmode)

#### Disk image caching modes

- [case automatic](/documentation/virtualization/vzdiskimagecachingmode/automatic)
- [case cached](/documentation/virtualization/vzdiskimagecachingmode/cached)
- [case uncached](/documentation/virtualization/vzdiskimagecachingmode/uncached)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzdiskimagecachingmode/init(rawvalue:))
- [VZDiskImageSynchronizationMode](/documentation/virtualization/vzdiskimagesynchronizationmode)

#### Disk image synchronization modes

- [case full](/documentation/virtualization/vzdiskimagesynchronizationmode/full)
- [case fsync](/documentation/virtualization/vzdiskimagesynchronizationmode/fsync)
- [case none](/documentation/virtualization/vzdiskimagesynchronizationmode/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzdiskimagesynchronizationmode/init(rawvalue:))
- [VZNVMExpressControllerDeviceConfiguration](/documentation/virtualization/vznvmexpresscontrollerdeviceconfiguration)

#### Creating a new device configuration

- [init(attachment: VZStorageDeviceAttachment)](/documentation/virtualization/vznvmexpresscontrollerdeviceconfiguration/init(attachment:))

### Devices

- [VZStorageDevice](/documentation/virtualization/vzstoragedevice)

### Attachment points

- [VZDiskBlockDeviceStorageDeviceAttachment](/documentation/virtualization/vzdiskblockdevicestoragedeviceattachment)

#### Initializers

- [init(fileHandle: FileHandle, readOnly: Bool, synchronizationMode: VZDiskSynchronizationMode) throws](/documentation/virtualization/vzdiskblockdevicestoragedeviceattachment/init(filehandle:readonly:synchronizationmode:))

#### Getting the block storage device details

- [var fileHandle: FileHandle](/documentation/virtualization/vzdiskblockdevicestoragedeviceattachment/filehandle)
- [var isReadOnly: Bool](/documentation/virtualization/vzdiskblockdevicestoragedeviceattachment/isreadonly)
- [var synchronizationMode: VZDiskSynchronizationMode](/documentation/virtualization/vzdiskblockdevicestoragedeviceattachment/synchronizationmode)
- [VZDiskImageStorageDeviceAttachment](/documentation/virtualization/vzdiskimagestoragedeviceattachment)

#### Creating the attachment point

- [init(url: URL, readOnly: Bool) throws](/documentation/virtualization/vzdiskimagestoragedeviceattachment/init(url:readonly:))
- [init(url: URL, readOnly: Bool, cachingMode: VZDiskImageCachingMode, synchronizationMode: VZDiskImageSynchronizationMode) throws](/documentation/virtualization/vzdiskimagestoragedeviceattachment/init(url:readonly:cachingmode:synchronizationmode:))

#### Getting the disk image details

- [var url: URL](/documentation/virtualization/vzdiskimagestoragedeviceattachment/url)
- [var isReadOnly: Bool](/documentation/virtualization/vzdiskimagestoragedeviceattachment/isreadonly)
- [var cachingMode: VZDiskImageCachingMode](/documentation/virtualization/vzdiskimagestoragedeviceattachment/cachingmode)
- [var synchronizationMode: VZDiskImageSynchronizationMode](/documentation/virtualization/vzdiskimagestoragedeviceattachment/synchronizationmode)
- [VZNetworkBlockDeviceStorageDeviceAttachment](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment)

#### Creating network block device attachments

- [convenience init(url: URL) throws](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/init(url:))
- [init(url: URL, timeout: TimeInterval, isForcedReadOnly: Bool, synchronizationMode: VZDiskSynchronizationMode) throws](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/init(url:timeout:isforcedreadonly:synchronizationmode:))

#### Validating a network block device’s URL

- [class func validate(URL) throws](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/validate(_:))

#### Getting information about the attachment point

- [var isForcedReadOnly: Bool](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/isforcedreadonly)
- [var synchronizationMode: VZDiskSynchronizationMode](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/synchronizationmode)
- [var timeout: TimeInterval](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/timeout)
- [var url: URL](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/url)

#### Observing changes to the network block device

- [var delegate: (any VZNetworkBlockDeviceStorageDeviceAttachmentDelegate)?](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachment/delegate)
- [VZNetworkBlockDeviceStorageDeviceAttachmentDelegate](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachmentdelegate)

##### Responding to connectivity changes

- [func attachment(VZNetworkBlockDeviceStorageDeviceAttachment, didEncounterError: any Error)](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachmentdelegate/attachment(_:didencountererror:))
- [func attachmentWasConnected(VZNetworkBlockDeviceStorageDeviceAttachment)](/documentation/virtualization/vznetworkblockdevicestoragedeviceattachmentdelegate/attachmentwasconnected(_:))
- [VZStorageDeviceAttachment](/documentation/virtualization/vzstoragedeviceattachment)
- [Consoles](/documentation/virtualization/consoles)

### Configurations

- [VZConsoleDeviceConfiguration](/documentation/virtualization/vzconsoledeviceconfiguration)
- [VZConsolePortConfiguration](/documentation/virtualization/vzconsoleportconfiguration)

#### Configuring the attachment

- [var attachment: VZSerialPortAttachment?](/documentation/virtualization/vzconsoleportconfiguration/attachment)
- [VZVirtioConsoleDeviceConfiguration](/documentation/virtualization/vzvirtioconsoledeviceconfiguration)

#### Creating the configuration object

- [init()](/documentation/virtualization/vzvirtioconsoledeviceconfiguration/init())

#### Configuring the console ports

- [var ports: VZVirtioConsolePortConfigurationArray](/documentation/virtualization/vzvirtioconsoledeviceconfiguration/ports)
- [VZVirtioConsolePortConfiguration](/documentation/virtualization/vzvirtioconsoleportconfiguration)

#### Creating a port configuration

- [init()](/documentation/virtualization/vzvirtioconsoleportconfiguration/init())

#### Configuring the port

- [var isConsole: Bool](/documentation/virtualization/vzvirtioconsoleportconfiguration/isconsole)
- [var name: String?](/documentation/virtualization/vzvirtioconsoleportconfiguration/name)
- [VZVirtioConsolePortConfigurationArray](/documentation/virtualization/vzvirtioconsoleportconfigurationarray)

#### Determining the number of ports

- [var maximumPortCount: UInt32](/documentation/virtualization/vzvirtioconsoleportconfigurationarray/maximumportcount)

#### Accessing a specific port

- [subscript(Int) -> VZVirtioConsolePortConfiguration?](/documentation/virtualization/vzvirtioconsoleportconfigurationarray/subscript(_:))

### Console ports

- [VZVirtioConsolePort](/documentation/virtualization/vzvirtioconsoleport)

#### Configuring the port

- [var name: String?](/documentation/virtualization/vzvirtioconsoleport/name)
- [var attachment: VZSerialPortAttachment?](/documentation/virtualization/vzvirtioconsoleport/attachment)
- [VZVirtioConsolePortArray](/documentation/virtualization/vzvirtioconsoleportarray)

#### Determining the number of ports

- [var maximumPortCount: UInt32](/documentation/virtualization/vzvirtioconsoleportarray/maximumportcount)

#### Accessing a specific port

- [subscript(Int) -> VZVirtioConsolePort?](/documentation/virtualization/vzvirtioconsoleportarray/subscript(_:))

### Devices

- [VZConsoleDevice](/documentation/virtualization/vzconsoledevice)
- [VZVirtioConsoleDevice](/documentation/virtualization/vzvirtioconsoledevice)

#### Configuring the console

- [var ports: VZVirtioConsolePortArray](/documentation/virtualization/vzvirtioconsoledevice/ports)
- [var delegate: (any VZVirtioConsoleDeviceDelegate)?](/documentation/virtualization/vzvirtioconsoledevice/delegate)
- [VZVirtioConsoleDeviceDelegate](/documentation/virtualization/vzvirtioconsoledevicedelegate)

##### Responding to console device changes

- [func consoleDevice(VZVirtioConsoleDevice, didOpen: VZVirtioConsolePort)](/documentation/virtualization/vzvirtioconsoledevicedelegate/consoledevice(_:didopen:))
- [func consoleDevice(VZVirtioConsoleDevice, didClose: VZVirtioConsolePort)](/documentation/virtualization/vzvirtioconsoledevicedelegate/consoledevice(_:didclose:))
- [Clipboard sharing](/documentation/virtualization/clipboard-sharing)

### Attachement points

- [VZSpiceAgentPortAttachment](/documentation/virtualization/vzspiceagentportattachment)

#### Creating a shared clipboard

- [init()](/documentation/virtualization/vzspiceagentportattachment/init())

#### Enabling clipboard sharing between the host and the VM

- [var sharesClipboard: Bool](/documentation/virtualization/vzspiceagentportattachment/sharesclipboard)

#### Naming the Virtio console port for the Spice guest agent

- [class var spiceAgentPortName: String](/documentation/virtualization/vzspiceagentportattachment/spiceagentportname)
- [USB Devices](/documentation/virtualization/usb-devices)

### Storage Devices

- [VZUSBMassStorageDevice](/documentation/virtualization/vzusbmassstoragedevice)

#### Creating a USB mass storage device

- [init(configuration: VZUSBMassStorageDeviceConfiguration)](/documentation/virtualization/vzusbmassstoragedevice/init(configuration:))

### Configurations

- [VZUSBControllerConfiguration](/documentation/virtualization/vzusbcontrollerconfiguration)

#### Instance properties

- [var usbDevices: [any VZUSBDeviceConfiguration]](/documentation/virtualization/vzusbcontrollerconfiguration/usbdevices)
- [VZXHCIControllerConfiguration](/documentation/virtualization/vzxhcicontrollerconfiguration)

#### Initializers

- [init()](/documentation/virtualization/vzxhcicontrollerconfiguration/init())

### Controllers

- [VZUSBController](/documentation/virtualization/vzusbcontroller)

#### Instance properties

- [var usbDevices: [any VZUSBDevice]](/documentation/virtualization/vzusbcontroller/usbdevices)

#### Attaching and detaching devices

- [func attach(device: any VZUSBDevice, completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzusbcontroller/attach(device:completionhandler:))
- [func detach(device: any VZUSBDevice, completionHandler: ((any Error)?) -> Void)](/documentation/virtualization/vzusbcontroller/detach(device:completionhandler:))
- [VZXHCIController](/documentation/virtualization/vzxhcicontroller)

### Protocols

- [VZUSBDevice](/documentation/virtualization/vzusbdevice)

#### Properties

- [var usbController: VZUSBController?](/documentation/virtualization/vzusbdevice/usbcontroller)
- [var uuid: UUID](/documentation/virtualization/vzusbdevice/uuid)
- [VZUSBDeviceConfiguration](/documentation/virtualization/vzusbdeviceconfiguration)

#### Properties

- [var uuid: UUID](/documentation/virtualization/vzusbdeviceconfiguration/uuid)

## Enumerations

- [Virtualization enumerations](/documentation/virtualization/virtualization-enumerations)

### Virtual disk image caching modes

- [VZDiskImageCachingMode](/documentation/virtualization/vzdiskimagecachingmode)

#### Disk image caching modes

- [case automatic](/documentation/virtualization/vzdiskimagecachingmode/automatic)
- [case cached](/documentation/virtualization/vzdiskimagecachingmode/cached)
- [case uncached](/documentation/virtualization/vzdiskimagecachingmode/uncached)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzdiskimagecachingmode/init(rawvalue:))

### Virtual disk synchronization modes

- [VZDiskImageSynchronizationMode](/documentation/virtualization/vzdiskimagesynchronizationmode)

#### Disk image synchronization modes

- [case full](/documentation/virtualization/vzdiskimagesynchronizationmode/full)
- [case fsync](/documentation/virtualization/vzdiskimagesynchronizationmode/fsync)
- [case none](/documentation/virtualization/vzdiskimagesynchronizationmode/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzdiskimagesynchronizationmode/init(rawvalue:))
- [VZDiskSynchronizationMode](/documentation/virtualization/vzdisksynchronizationmode)

#### Synchronization modes

- [case full](/documentation/virtualization/vzdisksynchronizationmode/full)
- [case none](/documentation/virtualization/vzdisksynchronizationmode/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzdisksynchronizationmode/init(rawvalue:))

### Mac-specific auxiliary storage options

- [VZMacAuxiliaryStorage.InitializationOptions](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions)

#### Mac auxiliary storage structure

- [init(rawValue: UInt)](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions/init(rawvalue:))

#### Controlling overwrites

- [static var allowOverwrite: VZMacAuxiliaryStorage.InitializationOptions](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions/allowoverwrite)
- [static var allowOverwrite: VZMacAuxiliaryStorage.InitializationOptions](/documentation/virtualization/vzmacauxiliarystorage/initializationoptions/allowoverwrite)

### Rosetta availability states

- [VZLinuxRosettaAvailability](/documentation/virtualization/vzlinuxrosettaavailability)

#### Rosetta availability states

- [case notSupported](/documentation/virtualization/vzlinuxrosettaavailability/notsupported)
- [case notInstalled](/documentation/virtualization/vzlinuxrosettaavailability/notinstalled)
- [case installed](/documentation/virtualization/vzlinuxrosettaavailability/installed)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzlinuxrosettaavailability/init(rawvalue:))

### Virtualization error codes

- [VZError.Code](/documentation/virtualization/vzerror/code)

#### Error codes

- [case internalError](/documentation/virtualization/vzerror/code/internalerror)
- [case invalidVirtualMachineConfiguration](/documentation/virtualization/vzerror/code/invalidvirtualmachineconfiguration)
- [case invalidVirtualMachineState](/documentation/virtualization/vzerror/code/invalidvirtualmachinestate)
- [case invalidVirtualMachineStateTransition](/documentation/virtualization/vzerror/code/invalidvirtualmachinestatetransition)
- [case invalidDiskImage](/documentation/virtualization/vzerror/code/invaliddiskimage)
- [case virtualMachineLimitExceeded](/documentation/virtualization/vzerror/code/virtualmachinelimitexceeded)
- [case networkError](/documentation/virtualization/vzerror/code/networkerror)
- [case notSupported](/documentation/virtualization/vzerror/code/notsupported)
- [case outOfDiskSpace](/documentation/virtualization/vzerror/code/outofdiskspace)
- [case operationCancelled](/documentation/virtualization/vzerror/code/operationcancelled)
- [case installationFailed](/documentation/virtualization/vzerror/code/installationfailed)
- [case installationRequiresUpdate](/documentation/virtualization/vzerror/code/installationrequiresupdate)
- [case invalidRestoreImage](/documentation/virtualization/vzerror/code/invalidrestoreimage)
- [case invalidRestoreImageCatalog](/documentation/virtualization/vzerror/code/invalidrestoreimagecatalog)
- [case noSupportedRestoreImagesInCatalog](/documentation/virtualization/vzerror/code/nosupportedrestoreimagesincatalog)
- [case restoreImageCatalogLoadFailed](/documentation/virtualization/vzerror/code/restoreimagecatalogloadfailed)
- [case restoreImageLoadFailed](/documentation/virtualization/vzerror/code/restoreimageloadfailed)
- [case networkBlockDeviceNegotiationFailed](/documentation/virtualization/vzerror/code/networkblockdevicenegotiationfailed)
- [case networkBlockDeviceDisconnected](/documentation/virtualization/vzerror/code/networkblockdevicedisconnected)
- [case restore](/documentation/virtualization/vzerror/code/restore)
- [case save](/documentation/virtualization/vzerror/code/save)
- [case deviceAlreadyAttached](/documentation/virtualization/vzerror/code/devicealreadyattached)
- [case deviceInitializationFailure](/documentation/virtualization/vzerror/code/deviceinitializationfailure)
- [case deviceNotFound](/documentation/virtualization/vzerror/code/devicenotfound)
- [case usbControllerNotFound](/documentation/virtualization/vzerror/code/usbcontrollernotfound)
- [case internalError](/documentation/virtualization/vzerror/code/internalerror)
- [case invalidVirtualMachineConfiguration](/documentation/virtualization/vzerror/code/invalidvirtualmachineconfiguration)
- [case invalidVirtualMachineState](/documentation/virtualization/vzerror/code/invalidvirtualmachinestate)
- [case invalidVirtualMachineStateTransition](/documentation/virtualization/vzerror/code/invalidvirtualmachinestatetransition)
- [case invalidDiskImage](/documentation/virtualization/vzerror/code/invaliddiskimage)
- [case virtualMachineLimitExceeded](/documentation/virtualization/vzerror/code/virtualmachinelimitexceeded)
- [case networkError](/documentation/virtualization/vzerror/code/networkerror)
- [case notSupported](/documentation/virtualization/vzerror/code/notsupported)
- [case outOfDiskSpace](/documentation/virtualization/vzerror/code/outofdiskspace)
- [case operationCancelled](/documentation/virtualization/vzerror/code/operationcancelled)
- [case installationFailed](/documentation/virtualization/vzerror/code/installationfailed)
- [case installationRequiresUpdate](/documentation/virtualization/vzerror/code/installationrequiresupdate)
- [case invalidRestoreImage](/documentation/virtualization/vzerror/code/invalidrestoreimage)
- [case invalidRestoreImageCatalog](/documentation/virtualization/vzerror/code/invalidrestoreimagecatalog)
- [case noSupportedRestoreImagesInCatalog](/documentation/virtualization/vzerror/code/nosupportedrestoreimagesincatalog)
- [case restoreImageCatalogLoadFailed](/documentation/virtualization/vzerror/code/restoreimagecatalogloadfailed)
- [case restoreImageLoadFailed](/documentation/virtualization/vzerror/code/restoreimageloadfailed)
- [case networkBlockDeviceNegotiationFailed](/documentation/virtualization/vzerror/code/networkblockdevicenegotiationfailed)
- [case networkBlockDeviceDisconnected](/documentation/virtualization/vzerror/code/networkblockdevicedisconnected)
- [case restore](/documentation/virtualization/vzerror/code/restore)
- [case save](/documentation/virtualization/vzerror/code/save)
- [case deviceAlreadyAttached](/documentation/virtualization/vzerror/code/devicealreadyattached)
- [case deviceInitializationFailure](/documentation/virtualization/vzerror/code/deviceinitializationfailure)
- [case deviceNotFound](/documentation/virtualization/vzerror/code/devicenotfound)
- [case usbControllerNotFound](/documentation/virtualization/vzerror/code/usbcontrollernotfound)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzerror/code/init(rawvalue:))

### VM states

- [VZVirtualMachine.State](/documentation/virtualization/vzvirtualmachine/state-swift.enum)

#### States

- [case stopped](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopped)
- [case running](/documentation/virtualization/vzvirtualmachine/state-swift.enum/running)
- [case paused](/documentation/virtualization/vzvirtualmachine/state-swift.enum/paused)
- [case error](/documentation/virtualization/vzvirtualmachine/state-swift.enum/error)
- [case starting](/documentation/virtualization/vzvirtualmachine/state-swift.enum/starting)
- [case pausing](/documentation/virtualization/vzvirtualmachine/state-swift.enum/pausing)
- [case stopping](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopping)
- [case resuming](/documentation/virtualization/vzvirtualmachine/state-swift.enum/resuming)
- [case restoring](/documentation/virtualization/vzvirtualmachine/state-swift.enum/restoring)
- [case saving](/documentation/virtualization/vzvirtualmachine/state-swift.enum/saving)
- [case stopped](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopped)
- [case running](/documentation/virtualization/vzvirtualmachine/state-swift.enum/running)
- [case paused](/documentation/virtualization/vzvirtualmachine/state-swift.enum/paused)
- [case error](/documentation/virtualization/vzvirtualmachine/state-swift.enum/error)
- [case starting](/documentation/virtualization/vzvirtualmachine/state-swift.enum/starting)
- [case pausing](/documentation/virtualization/vzvirtualmachine/state-swift.enum/pausing)
- [case stopping](/documentation/virtualization/vzvirtualmachine/state-swift.enum/stopping)
- [case resuming](/documentation/virtualization/vzvirtualmachine/state-swift.enum/resuming)
- [case restoring](/documentation/virtualization/vzvirtualmachine/state-swift.enum/restoring)
- [case saving](/documentation/virtualization/vzvirtualmachine/state-swift.enum/saving)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzvirtualmachine/state-swift.enum/init(rawvalue:))

## Errors

- [let VZErrorDomain: String](/documentation/virtualization/vzerrordomain)
- [VZError](/documentation/virtualization/vzerror)

### Getting the error codes

- [static var internalError: VZError.Code](/documentation/virtualization/vzerror/internalerror)
- [static var invalidVirtualMachineConfiguration: VZError.Code](/documentation/virtualization/vzerror/invalidvirtualmachineconfiguration)
- [static var invalidVirtualMachineState: VZError.Code](/documentation/virtualization/vzerror/invalidvirtualmachinestate)
- [static var invalidVirtualMachineStateTransition: VZError.Code](/documentation/virtualization/vzerror/invalidvirtualmachinestatetransition)
- [static var invalidDiskImage: VZError.Code](/documentation/virtualization/vzerror/invaliddiskimage)
- [static var networkError: VZError.Code](/documentation/virtualization/vzerror/networkerror)
- [static var notSupported: VZError.Code](/documentation/virtualization/vzerror/notsupported)
- [static var outOfDiskSpace: VZError.Code](/documentation/virtualization/vzerror/outofdiskspace)
- [static var operationCancelled: VZError.Code](/documentation/virtualization/vzerror/operationcancelled)
- [static var installationFailed: VZError.Code](/documentation/virtualization/vzerror/installationfailed)
- [static var installationRequiresUpdate: VZError.Code](/documentation/virtualization/vzerror/installationrequiresupdate)
- [static var invalidRestoreImage: VZError.Code](/documentation/virtualization/vzerror/invalidrestoreimage)
- [static var invalidRestoreImageCatalog: VZError.Code](/documentation/virtualization/vzerror/invalidrestoreimagecatalog)
- [static var noSupportedRestoreImagesInCatalog: VZError.Code](/documentation/virtualization/vzerror/nosupportedrestoreimagesincatalog)
- [static var restoreImageCatalogLoadFailed: VZError.Code](/documentation/virtualization/vzerror/restoreimagecatalogloadfailed)
- [static var restoreImageLoadFailed: VZError.Code](/documentation/virtualization/vzerror/restoreimageloadfailed)
- [static var restore: VZError.Code](/documentation/virtualization/vzerror/restore)
- [static var save: VZError.Code](/documentation/virtualization/vzerror/save)
- [static var deviceAlreadyAttached: VZError.Code](/documentation/virtualization/vzerror/devicealreadyattached)
- [static var deviceInitializationFailure: VZError.Code](/documentation/virtualization/vzerror/deviceinitializationfailure)
- [static var deviceNotFound: VZError.Code](/documentation/virtualization/vzerror/devicenotfound)
- [static var usbControllerNotFound: VZError.Code](/documentation/virtualization/vzerror/usbcontrollernotfound)
- [VZError.Code](/documentation/virtualization/vzerror/code)

#### Error codes

- [case internalError](/documentation/virtualization/vzerror/code/internalerror)
- [case invalidVirtualMachineConfiguration](/documentation/virtualization/vzerror/code/invalidvirtualmachineconfiguration)
- [case invalidVirtualMachineState](/documentation/virtualization/vzerror/code/invalidvirtualmachinestate)
- [case invalidVirtualMachineStateTransition](/documentation/virtualization/vzerror/code/invalidvirtualmachinestatetransition)
- [case invalidDiskImage](/documentation/virtualization/vzerror/code/invaliddiskimage)
- [case virtualMachineLimitExceeded](/documentation/virtualization/vzerror/code/virtualmachinelimitexceeded)
- [case networkError](/documentation/virtualization/vzerror/code/networkerror)
- [case notSupported](/documentation/virtualization/vzerror/code/notsupported)
- [case outOfDiskSpace](/documentation/virtualization/vzerror/code/outofdiskspace)
- [case operationCancelled](/documentation/virtualization/vzerror/code/operationcancelled)
- [case installationFailed](/documentation/virtualization/vzerror/code/installationfailed)
- [case installationRequiresUpdate](/documentation/virtualization/vzerror/code/installationrequiresupdate)
- [case invalidRestoreImage](/documentation/virtualization/vzerror/code/invalidrestoreimage)
- [case invalidRestoreImageCatalog](/documentation/virtualization/vzerror/code/invalidrestoreimagecatalog)
- [case noSupportedRestoreImagesInCatalog](/documentation/virtualization/vzerror/code/nosupportedrestoreimagesincatalog)
- [case restoreImageCatalogLoadFailed](/documentation/virtualization/vzerror/code/restoreimagecatalogloadfailed)
- [case restoreImageLoadFailed](/documentation/virtualization/vzerror/code/restoreimageloadfailed)
- [case networkBlockDeviceNegotiationFailed](/documentation/virtualization/vzerror/code/networkblockdevicenegotiationfailed)
- [case networkBlockDeviceDisconnected](/documentation/virtualization/vzerror/code/networkblockdevicedisconnected)
- [case restore](/documentation/virtualization/vzerror/code/restore)
- [case save](/documentation/virtualization/vzerror/code/save)
- [case deviceAlreadyAttached](/documentation/virtualization/vzerror/code/devicealreadyattached)
- [case deviceInitializationFailure](/documentation/virtualization/vzerror/code/deviceinitializationfailure)
- [case deviceNotFound](/documentation/virtualization/vzerror/code/devicenotfound)
- [case usbControllerNotFound](/documentation/virtualization/vzerror/code/usbcontrollernotfound)
- [case internalError](/documentation/virtualization/vzerror/code/internalerror)
- [case invalidVirtualMachineConfiguration](/documentation/virtualization/vzerror/code/invalidvirtualmachineconfiguration)
- [case invalidVirtualMachineState](/documentation/virtualization/vzerror/code/invalidvirtualmachinestate)
- [case invalidVirtualMachineStateTransition](/documentation/virtualization/vzerror/code/invalidvirtualmachinestatetransition)
- [case invalidDiskImage](/documentation/virtualization/vzerror/code/invaliddiskimage)
- [case virtualMachineLimitExceeded](/documentation/virtualization/vzerror/code/virtualmachinelimitexceeded)
- [case networkError](/documentation/virtualization/vzerror/code/networkerror)
- [case notSupported](/documentation/virtualization/vzerror/code/notsupported)
- [case outOfDiskSpace](/documentation/virtualization/vzerror/code/outofdiskspace)
- [case operationCancelled](/documentation/virtualization/vzerror/code/operationcancelled)
- [case installationFailed](/documentation/virtualization/vzerror/code/installationfailed)
- [case installationRequiresUpdate](/documentation/virtualization/vzerror/code/installationrequiresupdate)
- [case invalidRestoreImage](/documentation/virtualization/vzerror/code/invalidrestoreimage)
- [case invalidRestoreImageCatalog](/documentation/virtualization/vzerror/code/invalidrestoreimagecatalog)
- [case noSupportedRestoreImagesInCatalog](/documentation/virtualization/vzerror/code/nosupportedrestoreimagesincatalog)
- [case restoreImageCatalogLoadFailed](/documentation/virtualization/vzerror/code/restoreimagecatalogloadfailed)
- [case restoreImageLoadFailed](/documentation/virtualization/vzerror/code/restoreimageloadfailed)
- [case networkBlockDeviceNegotiationFailed](/documentation/virtualization/vzerror/code/networkblockdevicenegotiationfailed)
- [case networkBlockDeviceDisconnected](/documentation/virtualization/vzerror/code/networkblockdevicedisconnected)
- [case restore](/documentation/virtualization/vzerror/code/restore)
- [case save](/documentation/virtualization/vzerror/code/save)
- [case deviceAlreadyAttached](/documentation/virtualization/vzerror/code/devicealreadyattached)
- [case deviceInitializationFailure](/documentation/virtualization/vzerror/code/deviceinitializationfailure)
- [case deviceNotFound](/documentation/virtualization/vzerror/code/devicenotfound)
- [case usbControllerNotFound](/documentation/virtualization/vzerror/code/usbcontrollernotfound)

#### Initializers

- [init?(rawValue: Int)](/documentation/virtualization/vzerror/code/init(rawvalue:))

### Accessing the error information

- [static var virtualMachineLimitExceeded: VZError.Code](/documentation/virtualization/vzerror/virtualmachinelimitexceeded)

### Type properties

- [static var networkBlockDeviceDisconnected: VZError.Code](/documentation/virtualization/vzerror/networkblockdevicedisconnected)
- [static var networkBlockDeviceNegotiationFailed: VZError.Code](/documentation/virtualization/vzerror/networkblockdevicenegotiationfailed)

### Type Properties

- [static var errorDomain: String](/documentation/virtualization/vzerror/errordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
