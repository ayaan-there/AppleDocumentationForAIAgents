# Nearby Interaction Documentation

Source: https://sosumi.ai/documentation/nearbyinteraction

---
title: Nearby Interaction
source: https://developer.apple.com/documentation/nearbyinteraction
timestamp: 2026-02-13T18:59:57.291Z
---

## Setup

- [Initiating and maintaining a session](/documentation/nearbyinteraction/initiating-and-maintaining-a-session)
- [NISession](/documentation/nearbyinteraction/nisession)

### Ensuring feature support

- [class var deviceCapabilities: any NIDeviceCapability](/documentation/nearbyinteraction/nisession/devicecapabilities)
- [NIDeviceCapability](/documentation/nearbyinteraction/nidevicecapability)

#### Session features

- [var supportsPreciseDistanceMeasurement: Bool](/documentation/nearbyinteraction/nidevicecapability/supportsprecisedistancemeasurement)
- [var supportsDirectionMeasurement: Bool](/documentation/nearbyinteraction/nidevicecapability/supportsdirectionmeasurement)
- [var supportsCameraAssistance: Bool](/documentation/nearbyinteraction/nidevicecapability/supportscameraassistance)
- [var supportsExtendedDistanceMeasurement: Bool](/documentation/nearbyinteraction/nidevicecapability/supportsextendeddistancemeasurement)
- [var supportsDLTDOAMeasurement: Bool](/documentation/nearbyinteraction/nidevicecapability/supportsdltdoameasurement)

### Connecting to A Peer Device

- [var discoveryToken: NIDiscoveryToken?](/documentation/nearbyinteraction/nisession/discoverytoken)
- [NIDiscoveryToken](/documentation/nearbyinteraction/nidiscoverytoken)

#### Understanding device capabilities

- [var deviceCapabilities: any NIDeviceCapability](/documentation/nearbyinteraction/nidiscoverytoken/devicecapabilities)
- [func run(NIConfiguration)](/documentation/nearbyinteraction/nisession/run(_:))
- [var configuration: NIConfiguration?](/documentation/nearbyinteraction/nisession/configuration)
- [var delegateQueue: dispatch_queue_t?](/documentation/nearbyinteraction/nisession/delegatequeue)

### Managing life cycle

- [var delegate: (any NISessionDelegate)?](/documentation/nearbyinteraction/nisession/delegate)
- [func pause()](/documentation/nearbyinteraction/nisession/pause())
- [func invalidate()](/documentation/nearbyinteraction/nisession/invalidate())

### Utilizing Camera Assistance

- [func setARSession(ARSession)](/documentation/nearbyinteraction/nisession/setarsession(_:))
- [func worldTransform(for: NINearbyObject) -> simd_float4x4?](/documentation/nearbyinteraction/nisession/worldtransform(for:))

### Deprecated

- [class var isSupported: Bool](/documentation/nearbyinteraction/nisession/issupported)

## Authorization

- [NSNearbyInteractionUsageDescription](/documentation/bundleresources/information-property-list/nsnearbyinteractionusagedescription)

## Phone interaction

- [Implementing interactions between users in close proximity](/documentation/nearbyinteraction/implementing-interactions-between-users-in-close-proximity)
- [Discovering peers with Multipeer Connectivity](/documentation/nearbyinteraction/discovering-peers-with-multipeer-connectivity)
- [Extending advanced direction finding and ranging](/documentation/nearbyinteraction/extending-advanced-direction-finding-and-ranging)
- [NINearbyPeerConfiguration](/documentation/nearbyinteraction/ninearbypeerconfiguration)

### Creating a configuration

- [init(peerToken: NIDiscoveryToken)](/documentation/nearbyinteraction/ninearbypeerconfiguration/init(peertoken:))

### Accessing the discovery token

- [var peerDiscoveryToken: NIDiscoveryToken](/documentation/nearbyinteraction/ninearbypeerconfiguration/peerdiscoverytoken)

### Subclassing a configuration

- [NIConfiguration](/documentation/nearbyinteraction/niconfiguration)

### Enabling Camera Assistance

- [var isCameraAssistanceEnabled: Bool](/documentation/nearbyinteraction/ninearbypeerconfiguration/iscameraassistanceenabled)

### Checking distance measurement capability

- [var isExtendedDistanceMeasurementEnabled: Bool](/documentation/nearbyinteraction/ninearbypeerconfiguration/isextendeddistancemeasurementenabled)

## Watch interaction

- [Implementing proximity-based interactions between a phone and watch](/documentation/nearbyinteraction/implementing-proximity-based-interactions-between-a-phone-and-watch)

## Third-party accessories

- [Implementing spatial interactions with third-party accessories](/documentation/nearbyinteraction/implementing-spatial-interactions-with-third-party-accessories)
- [NINearbyAccessoryConfiguration](/documentation/nearbyinteraction/ninearbyaccessoryconfiguration)

### Creating a configuration

- [init(data: Data) throws](/documentation/nearbyinteraction/ninearbyaccessoryconfiguration/init(data:))
- [init(accessoryData: Data, bluetoothPeerIdentifier: UUID) throws](/documentation/nearbyinteraction/ninearbyaccessoryconfiguration/init(accessorydata:bluetoothpeeridentifier:))

### Identifying the peer

- [var accessoryDiscoveryToken: NIDiscoveryToken](/documentation/nearbyinteraction/ninearbyaccessoryconfiguration/accessorydiscoverytoken)

### Enabling Camera Assistance

- [var isCameraAssistanceEnabled: Bool](/documentation/nearbyinteraction/ninearbyaccessoryconfiguration/iscameraassistanceenabled)

## Periodic updates

- [NINearbyObject](/documentation/nearbyinteraction/ninearbyobject)

### Identifying a nearby device

- [var discoveryToken: NIDiscoveryToken](/documentation/nearbyinteraction/ninearbyobject/discoverytoken)

### Acquring relative distance

- [var distance: Float?](/documentation/nearbyinteraction/ninearbyobject/distance-676dm)

### Acquiring relative direction

- [var direction: simd_float3?](/documentation/nearbyinteraction/ninearbyobject/direction-4qh5w)
- [var horizontalAngle: Float?](/documentation/nearbyinteraction/ninearbyobject/horizontalangle-hsg)
- [var verticalDirectionEstimate: NINearbyObject.VerticalDirectionEstimate](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.property)
- [NINearbyObject.VerticalDirectionEstimate](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.enum)

#### Relative vertical location

- [case unknown](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.enum/unknown)
- [case same](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.enum/same)
- [case above](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.enum/above)
- [case below](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.enum/below)
- [case aboveOrBelow](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.enum/aboveorbelow)

#### Initializers

- [init?(rawValue: Int)](/documentation/nearbyinteraction/ninearbyobject/verticaldirectionestimate-swift.enum/init(rawvalue:))

### Explaining participation

- [NINearbyObject.RemovalReason](/documentation/nearbyinteraction/ninearbyobject/removalreason)

#### Reasons

- [case peerEnded](/documentation/nearbyinteraction/ninearbyobject/removalreason/peerended)
- [case timeout](/documentation/nearbyinteraction/ninearbyobject/removalreason/timeout)
- [case peerEnded](/documentation/nearbyinteraction/ninearbyobject/removalreason/peerended)
- [case timeout](/documentation/nearbyinteraction/ninearbyobject/removalreason/timeout)

#### Initializers

- [init?(rawValue: Int)](/documentation/nearbyinteraction/ninearbyobject/removalreason/init(rawvalue:))
- [NISessionDelegate](/documentation/nearbyinteraction/nisessiondelegate)

### Reacting to session start

- [func sessionDidStartRunning(NISession)](/documentation/nearbyinteraction/nisessiondelegate/sessiondidstartrunning(_:))

### Monitoring peers

- [func session(NISession, didUpdate: [NINearbyObject])](/documentation/nearbyinteraction/nisessiondelegate/session(_:didupdate:))
- [func session(NISession, didGenerateShareableConfigurationData: Data, for: NINearbyObject)](/documentation/nearbyinteraction/nisessiondelegate/session(_:didgenerateshareableconfigurationdata:for:))
- [func session(NISession, didRemove: [NINearbyObject], reason: NINearbyObject.RemovalReason)](/documentation/nearbyinteraction/nisessiondelegate/session(_:didremove:reason:))
- [NINearbyObject.RemovalReason](/documentation/nearbyinteraction/ninearbyobject/removalreason)

#### Reasons

- [case peerEnded](/documentation/nearbyinteraction/ninearbyobject/removalreason/peerended)
- [case timeout](/documentation/nearbyinteraction/ninearbyobject/removalreason/timeout)
- [case peerEnded](/documentation/nearbyinteraction/ninearbyobject/removalreason/peerended)
- [case timeout](/documentation/nearbyinteraction/ninearbyobject/removalreason/timeout)

#### Initializers

- [init?(rawValue: Int)](/documentation/nearbyinteraction/ninearbyobject/removalreason/init(rawvalue:))

### Managing interruption

- [func sessionWasSuspended(NISession)](/documentation/nearbyinteraction/nisessiondelegate/sessionwassuspended(_:))
- [func sessionSuspensionEnded(NISession)](/documentation/nearbyinteraction/nisessiondelegate/sessionsuspensionended(_:))

### Handling errors

- [func session(NISession, didInvalidateWith: any Error)](/documentation/nearbyinteraction/nisessiondelegate/session(_:didinvalidatewith:))

### Coaching the user

- [func session(NISession, didUpdateAlgorithmConvergence: NIAlgorithmConvergence, for: NINearbyObject?)](/documentation/nearbyinteraction/nisessiondelegate/session(_:didupdatealgorithmconvergence:for:))
- [NIAlgorithmConvergenceStatus](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve)

#### Interpreting the convergence state

- [case converged](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/converged)
- [case notConverged([NIAlgorithmConvergenceStatus.Reason])](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/notconverged(_:))
- [case unknown](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/unknown)

#### Comparing convergence states

- [static func == (NIAlgorithmConvergenceStatus, NIAlgorithmConvergenceStatus) -> Bool](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/==(_:_:))

#### Inspecting the convergence state reason

- [NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason)

##### Comparing convergence status reasons

- [var localizedDescription: String?](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/localizeddescription)

##### Interpreting the convergence status reason

- [static let insufficientMovement: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientmovement)
- [static let insufficientHorizontalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficienthorizontalsweep)
- [static let insufficientVerticalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientverticalsweep)
- [static let insufficientLighting: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientlighting)
- [static let insufficientSignalStrength: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientsignalstrength)
- [NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason)

#### Comparing convergence status reasons

- [var localizedDescription: String?](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/localizeddescription)

#### Interpreting the convergence status reason

- [static let insufficientMovement: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientmovement)
- [static let insufficientHorizontalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficienthorizontalsweep)
- [static let insufficientVerticalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientverticalsweep)
- [static let insufficientLighting: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientlighting)
- [static let insufficientSignalStrength: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientsignalstrength)

### Monitoring DL-TDoA measurements

- [func session(NISession, didUpdateDLTDOA: [NIDLTDOAMeasurement])](/documentation/nearbyinteraction/nisessiondelegate/session(_:didupdatedltdoa:))

## Camera assistance

- [Finding devices with precision](/documentation/nearbyinteraction/finding-devices-with-precision)
- [NIAlgorithmConvergence](/documentation/nearbyinteraction/nialgorithmconvergence)

### Determining convergence state

- [var status: NIAlgorithmConvergenceStatus](/documentation/nearbyinteraction/nialgorithmconvergence/status-654t)
- [NIAlgorithmConvergenceStatus](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve)

### Interpreting the convergence state

- [case converged](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/converged)
- [case notConverged([NIAlgorithmConvergenceStatus.Reason])](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/notconverged(_:))
- [case unknown](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/unknown)

### Comparing convergence states

- [static func == (NIAlgorithmConvergenceStatus, NIAlgorithmConvergenceStatus) -> Bool](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/==(_:_:))

### Inspecting the convergence state reason

- [NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason)

#### Comparing convergence status reasons

- [var localizedDescription: String?](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/localizeddescription)

#### Interpreting the convergence status reason

- [static let insufficientMovement: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientmovement)
- [static let insufficientHorizontalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficienthorizontalsweep)
- [static let insufficientVerticalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientverticalsweep)
- [static let insufficientLighting: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientlighting)
- [static let insufficientSignalStrength: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientsignalstrength)
- [Algorithm Convergence Status](/documentation/nearbyinteraction/algorithm-convergence-status)

### Status

- [NIAlgorithmConvergenceStatus](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve)

#### Interpreting the convergence state

- [case converged](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/converged)
- [case notConverged([NIAlgorithmConvergenceStatus.Reason])](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/notconverged(_:))
- [case unknown](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/unknown)

#### Comparing convergence states

- [static func == (NIAlgorithmConvergenceStatus, NIAlgorithmConvergenceStatus) -> Bool](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/==(_:_:))

#### Inspecting the convergence state reason

- [NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason)

##### Comparing convergence status reasons

- [var localizedDescription: String?](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/localizeddescription)

##### Interpreting the convergence status reason

- [static let insufficientMovement: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientmovement)
- [static let insufficientHorizontalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficienthorizontalsweep)
- [static let insufficientVerticalSweep: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientverticalsweep)
- [static let insufficientLighting: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientlighting)
- [static let insufficientSignalStrength: NIAlgorithmConvergenceStatus.Reason](/documentation/nearbyinteraction/nialgorithmconvergencestatus-2fnve/reason/insufficientsignalstrength)

## DL-TDoA ranging

- [Downlink time difference of arrival ranging](/documentation/nearbyinteraction/dl-tdoa-ranging)

### Configuration

- [NIDLTDOAConfiguration](/documentation/nearbyinteraction/nidltdoaconfiguration)

#### Creating a configuration

- [init(networkIdentifier: Int)](/documentation/nearbyinteraction/nidltdoaconfiguration/init(networkidentifier:))

#### Identifying the network

- [var networkIdentifier: Int](/documentation/nearbyinteraction/nidltdoaconfiguration/networkidentifier)

### Measurements

- [NIDLTDOAMeasurement](/documentation/nearbyinteraction/nidltdoameasurement)

#### Identifying the anchor

- [var address: Int](/documentation/nearbyinteraction/nidltdoameasurement/address)

#### Locating the anchor

- [var coordinates: simd_double3](/documentation/nearbyinteraction/nidltdoameasurement/coordinates)
- [var coordinatesType: NIDLTDOACoordinatesType](/documentation/nearbyinteraction/nidltdoameasurement/coordinatestype)
- [var signalStrength: Double](/documentation/nearbyinteraction/nidltdoameasurement/signalstrength)

#### Assessing time difference

- [var receiveTime: Double](/documentation/nearbyinteraction/nidltdoameasurement/receivetime)
- [var transmitTime: Double](/documentation/nearbyinteraction/nidltdoameasurement/transmittime)

#### Evaluating the message

- [var measurementType: NIDLTDOAMeasurementType](/documentation/nearbyinteraction/nidltdoameasurement/measurementtype)
- [var carrierFrequencyOffset: Double](/documentation/nearbyinteraction/nidltdoameasurement/carrierfrequencyoffset)
- [NIDLTDOACoordinatesType](/documentation/nearbyinteraction/nidltdoacoordinatestype)

#### Identifying a coordinate type

- [case geodetic](/documentation/nearbyinteraction/nidltdoacoordinatestype/geodetic)
- [case relative](/documentation/nearbyinteraction/nidltdoacoordinatestype/relative)

#### Creating a coordinate type

- [init?(rawValue: Int)](/documentation/nearbyinteraction/nidltdoacoordinatestype/init(rawvalue:))
- [NIDLTDOAMeasurementType](/documentation/nearbyinteraction/nidltdoameasurementtype)

#### Identifying the measurement type

- [case poll](/documentation/nearbyinteraction/nidltdoameasurementtype/poll)
- [case response](/documentation/nearbyinteraction/nidltdoameasurementtype/response)
- [case final](/documentation/nearbyinteraction/nidltdoameasurementtype/final)

#### Creating a measurement type

- [init?(rawValue: Int)](/documentation/nearbyinteraction/nidltdoameasurementtype/init(rawvalue:))

## Errors

- [NIError](/documentation/nearbyinteraction/nierror)

### Identifying an error cause

- [NIError.Code](/documentation/nearbyinteraction/nierror/code)

#### Errors

- [case activeSessionsLimitExceeded](/documentation/nearbyinteraction/nierror/code/activesessionslimitexceeded)
- [case invalidConfiguration](/documentation/nearbyinteraction/nierror/code/invalidconfiguration)
- [case resourceUsageTimeout](/documentation/nearbyinteraction/nierror/code/resourceusagetimeout)
- [case sessionFailed](/documentation/nearbyinteraction/nierror/code/sessionfailed)
- [case unsupportedPlatform](/documentation/nearbyinteraction/nierror/code/unsupportedplatform)
- [case userDidNotAllow](/documentation/nearbyinteraction/nierror/code/userdidnotallow)
- [case invalidARConfiguration](/documentation/nearbyinteraction/nierror/code/invalidarconfiguration)
- [case accessoryPeerDeviceUnavailable](/documentation/nearbyinteraction/nierror/code/accessorypeerdeviceunavailable)
- [case incompatiblePeerDevice](/documentation/nearbyinteraction/nierror/code/incompatiblepeerdevice)
- [case activeExtendedDistanceSessionsLimitExceeded](/documentation/nearbyinteraction/nierror/code/activeextendeddistancesessionslimitexceeded)

#### Initializers

- [init?(rawValue: Int)](/documentation/nearbyinteraction/nierror/code/init(rawvalue:))
- [static var activeSessionsLimitExceeded: NIError.Code](/documentation/nearbyinteraction/nierror/activesessionslimitexceeded)
- [static var invalidConfiguration: NIError.Code](/documentation/nearbyinteraction/nierror/invalidconfiguration)
- [static var resourceUsageTimeout: NIError.Code](/documentation/nearbyinteraction/nierror/resourceusagetimeout)
- [static var sessionFailed: NIError.Code](/documentation/nearbyinteraction/nierror/sessionfailed)
- [static var unsupportedPlatform: NIError.Code](/documentation/nearbyinteraction/nierror/unsupportedplatform)
- [static var userDidNotAllow: NIError.Code](/documentation/nearbyinteraction/nierror/userdidnotallow)
- [static var invalidARConfiguration: NIError.Code](/documentation/nearbyinteraction/nierror/invalidarconfiguration)
- [static var activeExtendedDistanceSessionsLimitExceeded: NIError.Code](/documentation/nearbyinteraction/nierror/activeextendeddistancesessionslimitexceeded)
- [static var incompatiblePeerDevice: NIError.Code](/documentation/nearbyinteraction/nierror/incompatiblepeerdevice)
- [static var accessoryPeerDeviceUnavailable: NIError.Code](/documentation/nearbyinteraction/nierror/accessorypeerdeviceunavailable)

### Type Properties

- [static var errorDomain: String](/documentation/nearbyinteraction/nierror/errordomain)
- [NIError.Code](/documentation/nearbyinteraction/nierror/code)

### Errors

- [case activeSessionsLimitExceeded](/documentation/nearbyinteraction/nierror/code/activesessionslimitexceeded)
- [case invalidConfiguration](/documentation/nearbyinteraction/nierror/code/invalidconfiguration)
- [case resourceUsageTimeout](/documentation/nearbyinteraction/nierror/code/resourceusagetimeout)
- [case sessionFailed](/documentation/nearbyinteraction/nierror/code/sessionfailed)
- [case unsupportedPlatform](/documentation/nearbyinteraction/nierror/code/unsupportedplatform)
- [case userDidNotAllow](/documentation/nearbyinteraction/nierror/code/userdidnotallow)
- [case invalidARConfiguration](/documentation/nearbyinteraction/nierror/code/invalidarconfiguration)
- [case accessoryPeerDeviceUnavailable](/documentation/nearbyinteraction/nierror/code/accessorypeerdeviceunavailable)
- [case incompatiblePeerDevice](/documentation/nearbyinteraction/nierror/code/incompatiblepeerdevice)
- [case activeExtendedDistanceSessionsLimitExceeded](/documentation/nearbyinteraction/nierror/code/activeextendeddistancesessionslimitexceeded)

### Initializers

- [init?(rawValue: Int)](/documentation/nearbyinteraction/nierror/code/init(rawvalue:))
- [let NIErrorDomain: String](/documentation/nearbyinteraction/nierrordomain)

## Deprecated

- [NSNearbyInteractionAllowOnceUsageDescription](/documentation/bundleresources/information-property-list/nsnearbyinteractionallowonceusagedescription)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
