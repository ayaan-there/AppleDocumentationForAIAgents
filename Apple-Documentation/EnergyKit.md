# EnergyKit Documentation

Source: https://sosumi.ai/documentation/energykit

---
title: EnergyKit
source: https://developer.apple.com/documentation/energykit
timestamp: 2026-02-13T18:56:36.025Z
---

## Essentials

- [Optimizing home electricity usage](/documentation/energykit/optimizing-home-electricity-usage)
- [com.apple.developer.energykit](/documentation/bundleresources/entitlements/com.apple.developer.energykit)

## Load events

- [ElectricHVACLoadEvent](/documentation/energykit/electrichvacloadevent)

### Creating an electrical load event

- [init(timestamp: Date, measurement: ElectricHVACLoadEvent.ElectricalMeasurement, session: ElectricHVACLoadEvent.Session, deviceID: String)](/documentation/energykit/electrichvacloadevent/init(timestamp:measurement:session:deviceid:))
- [ElectricHVACLoadEvent.Session](/documentation/energykit/electrichvacloadevent/session-swift.struct)

#### Creating a session

- [init(id: UUID, state: ElectricHVACLoadEvent.Session.State, guidanceState: ElectricHVACLoadEvent.Session.GuidanceState)](/documentation/energykit/electrichvacloadevent/session-swift.struct/init(id:state:guidancestate:))

#### Getting the session information

- [let id: UUID](/documentation/energykit/electrichvacloadevent/session-swift.struct/id)
- [let state: ElectricHVACLoadEvent.Session.State](/documentation/energykit/electrichvacloadevent/session-swift.struct/state-swift.property)
- [ElectricHVACLoadEvent.Session.State](/documentation/energykit/electrichvacloadevent/session-swift.struct/state-swift.enum)

##### Setting session states

- [case active](/documentation/energykit/electrichvacloadevent/session-swift.struct/state-swift.enum/active)
- [case begin](/documentation/energykit/electrichvacloadevent/session-swift.struct/state-swift.enum/begin)
- [case end](/documentation/energykit/electrichvacloadevent/session-swift.struct/state-swift.enum/end)

#### Identifying the guidance state

- [ElectricHVACLoadEvent.Session.GuidanceState](/documentation/energykit/electrichvacloadevent/session-swift.struct/guidancestate-swift.struct)

##### Checking the guidance state

- [init(wasFollowingGuidance: Bool, guidanceToken: UUID)](/documentation/energykit/electrichvacloadevent/session-swift.struct/guidancestate-swift.struct/init(wasfollowingguidance:guidancetoken:))
- [var guidanceToken: UUID](/documentation/energykit/electrichvacloadevent/session-swift.struct/guidancestate-swift.struct/guidancetoken)
- [let wasFollowingGuidance: Bool](/documentation/energykit/electrichvacloadevent/session-swift.struct/guidancestate-swift.struct/wasfollowingguidance)
- [let guidanceState: ElectricHVACLoadEvent.Session.GuidanceState](/documentation/energykit/electrichvacloadevent/session-swift.struct/guidancestate-swift.property)
- [ElectricHVACLoadEvent.ElectricalMeasurement](/documentation/energykit/electrichvacloadevent/electricalmeasurement)

#### Initializing an electrical measurement

- [init(stage: Int)](/documentation/energykit/electrichvacloadevent/electricalmeasurement/init(stage:))
- [let stage: Int](/documentation/energykit/electrichvacloadevent/electricalmeasurement/stage)

### Getting the electrical load event information

- [let id: UUID](/documentation/energykit/electrichvacloadevent/id)
- [let session: ElectricHVACLoadEvent.Session](/documentation/energykit/electrichvacloadevent/session-swift.property)
- [let timestamp: Date](/documentation/energykit/electrichvacloadevent/timestamp)

### Getting the device information

- [let deviceID: String](/documentation/energykit/electrichvacloadevent/deviceid)
- [let measurement: ElectricHVACLoadEvent.ElectricalMeasurement](/documentation/energykit/electrichvacloadevent/measurement)
- [ElectricVehicleLoadEvent](/documentation/energykit/electricvehicleloadevent)

### Creating an electrical load event

- [init(timestamp: Date, measurement: ElectricVehicleLoadEvent.ElectricalMeasurement, session: ElectricVehicleLoadEvent.Session, deviceID: String)](/documentation/energykit/electricvehicleloadevent/init(timestamp:measurement:session:deviceid:))
- [ElectricVehicleLoadEvent.Session](/documentation/energykit/electricvehicleloadevent/session-swift.struct)

#### Creating a load event

- [init(id: UUID, state: ElectricVehicleLoadEvent.Session.State, guidanceState: ElectricVehicleLoadEvent.Session.GuidanceState)](/documentation/energykit/electricvehicleloadevent/session-swift.struct/init(id:state:guidancestate:))
- [let guidanceState: ElectricVehicleLoadEvent.Session.GuidanceState](/documentation/energykit/electricvehicleloadevent/session-swift.struct/guidancestate-swift.property)
- [let id: UUID](/documentation/energykit/electricvehicleloadevent/session-swift.struct/id)
- [let state: ElectricVehicleLoadEvent.Session.State](/documentation/energykit/electricvehicleloadevent/session-swift.struct/state-swift.property)
- [ElectricVehicleLoadEvent.Session.GuidanceState](/documentation/energykit/electricvehicleloadevent/session-swift.struct/guidancestate-swift.struct)

##### Initializers

- [init(wasFollowingGuidance: Bool, guidanceToken: UUID)](/documentation/energykit/electricvehicleloadevent/session-swift.struct/guidancestate-swift.struct/init(wasfollowingguidance:guidancetoken:))

##### Instance Properties

- [var guidanceToken: UUID](/documentation/energykit/electricvehicleloadevent/session-swift.struct/guidancestate-swift.struct/guidancetoken)
- [let wasFollowingGuidance: Bool](/documentation/energykit/electricvehicleloadevent/session-swift.struct/guidancestate-swift.struct/wasfollowingguidance)
- [ElectricVehicleLoadEvent.Session.State](/documentation/energykit/electricvehicleloadevent/session-swift.struct/state-swift.enum)

##### Enumeration Cases

- [case active](/documentation/energykit/electricvehicleloadevent/session-swift.struct/state-swift.enum/active)
- [case begin](/documentation/energykit/electricvehicleloadevent/session-swift.struct/state-swift.enum/begin)
- [case end](/documentation/energykit/electricvehicleloadevent/session-swift.struct/state-swift.enum/end)
- [ElectricVehicleLoadEvent.ElectricalMeasurement](/documentation/energykit/electricvehicleloadevent/electricalmeasurement)

#### Initializing an electrical measurement

- [init(stateOfCharge: Int, direction: ElectricityFlowDirection, power: Measurement<UnitPower>, energy: Measurement<UnitEnergy>)](/documentation/energykit/electricvehicleloadevent/electricalmeasurement/init(stateofcharge:direction:power:energy:))

#### Getting the electrical measurements

- [let direction: ElectricityFlowDirection](/documentation/energykit/electricvehicleloadevent/electricalmeasurement/direction)
- [let energy: Measurement<UnitEnergy>](/documentation/energykit/electricvehicleloadevent/electricalmeasurement/energy)
- [let stateOfCharge: Int](/documentation/energykit/electricvehicleloadevent/electricalmeasurement/stateofcharge)
- [let power: Measurement<UnitPower>](/documentation/energykit/electricvehicleloadevent/electricalmeasurement/power)

### Getting the electrical load event information

- [let id: UUID](/documentation/energykit/electricvehicleloadevent/id)
- [let session: ElectricVehicleLoadEvent.Session](/documentation/energykit/electricvehicleloadevent/session-swift.property)
- [let timestamp: Date](/documentation/energykit/electricvehicleloadevent/timestamp)

### Getting the device information

- [let deviceID: String](/documentation/energykit/electricvehicleloadevent/deviceid)
- [let measurement: ElectricVehicleLoadEvent.ElectricalMeasurement](/documentation/energykit/electricvehicleloadevent/measurement)
- [EnergyVenue](/documentation/energykit/energyvenue)

### Returning electricity sites

- [static func venue(for: UUID) async throws -> EnergyVenue](/documentation/energykit/energyvenue/venue(for:))
- [static func venue(matchingHomeUniqueIdentifier: UUID) async throws -> EnergyVenue](/documentation/energykit/energyvenue/venue(matchinghomeuniqueidentifier:))

### Submitting load events

- [func submitEvents<Event>([Event]) async throws](/documentation/energykit/energyvenue/submitevents(_:))

### Identifying the location

- [let id: UUID](/documentation/energykit/energyvenue/id)
- [let name: String](/documentation/energykit/energyvenue/name)

### Type Methods

- [static func venues() async throws -> [EnergyVenue]](/documentation/energykit/energyvenue/venues())
- [ElectricityFlowDirection](/documentation/energykit/electricityflowdirection)

### Specifying electricity flow

- [case exported](/documentation/energykit/electricityflowdirection/exported)
- [case imported](/documentation/energykit/electricityflowdirection/imported)
- [ElectricalLoadEventProtocol](/documentation/energykit/electricalloadeventprotocol)

## Guidance

- [ElectricityGuidance](/documentation/energykit/electricityguidance)

### Getting the electricity guidance data

- [ElectricityGuidance.Service](/documentation/energykit/electricityguidance/service)

#### Obtaining guidance data

- [func guidance(using: ElectricityGuidance.Query, at: UUID) -> some AsyncSequence<ElectricityGuidance, any Error>
](/documentation/energykit/electricityguidance/service/guidance(using:at:))
- [static let sharedService: ElectricityGuidance.Service](/documentation/energykit/electricityguidance/sharedservice)

### Getting the electrical load weight

- [ElectricityGuidance.Value](/documentation/energykit/electricityguidance/value)

#### Creating a date interval

- [init(interval: DateInterval, rating: Double)](/documentation/energykit/electricityguidance/value/init(interval:rating:))
- [let interval: DateInterval](/documentation/energykit/electricityguidance/value/interval)
- [let rating: Double](/documentation/energykit/electricityguidance/value/rating)
- [let values: [ElectricityGuidance.Value]](/documentation/energykit/electricityguidance/values)
- [ElectricityGuidance.Options](/documentation/energykit/electricityguidance/options-swift.enum)

#### Getting the options

- [case locationHasRatePlan](/documentation/energykit/electricityguidance/options-swift.enum/locationhasrateplan)
- [case guidanceIncorporatesRatePlan](/documentation/energykit/electricityguidance/options-swift.enum/guidanceincorporatesrateplan)
- [let options: Set<ElectricityGuidance.Options>](/documentation/energykit/electricityguidance/options-swift.property)

### Identifying the guidance parameters

- [let interval: DateInterval](/documentation/energykit/electricityguidance/interval)
- [let energyVenueID: UUID](/documentation/energykit/electricityguidance/energyvenueid)
- [let guidanceToken: UUID](/documentation/energykit/electricityguidance/guidancetoken)

### Getting the guidance suggestion

- [ElectricityGuidance.Query](/documentation/energykit/electricityguidance/query)

#### Creating a query

- [init(suggestedAction: ElectricityGuidance.SuggestedAction)](/documentation/energykit/electricityguidance/query/init(suggestedaction:))
- [let suggestedAction: ElectricityGuidance.SuggestedAction](/documentation/energykit/electricityguidance/suggestedaction-swift.property)
- [ElectricityGuidance.SuggestedAction](/documentation/energykit/electricityguidance/suggestedaction-swift.enum)

#### Suggesting electrical load usage

- [case reduce](/documentation/energykit/electricityguidance/suggestedaction-swift.enum/reduce)
- [case shift](/documentation/energykit/electricityguidance/suggestedaction-swift.enum/shift)

## Insights

- [ElectricityInsightRecord](/documentation/energykit/electricityinsightrecord)

### Getting the grid data

- [ElectricityInsightRecord.GridCleanliness](/documentation/energykit/electricityinsightrecord/gridcleanliness)

#### Initializing the grid data

- [init(cleaner: Measure?, lessClean: Measure?, avoid: Measure?, unknown: Measure?)](/documentation/energykit/electricityinsightrecord/gridcleanliness/init(cleaner:lessclean:avoid:unknown:))

#### Getting grid cleanliness information

- [var cleaner: Measure?](/documentation/energykit/electricityinsightrecord/gridcleanliness/cleaner)
- [var lessClean: Measure?](/documentation/energykit/electricityinsightrecord/gridcleanliness/lessclean)
- [var avoid: Measure?](/documentation/energykit/electricityinsightrecord/gridcleanliness/avoid)
- [var unknown: Measure?](/documentation/energykit/electricityinsightrecord/gridcleanliness/unknown)
- [var dataByGridCleanliness: ElectricityInsightRecord<Measure>.GridCleanliness?](/documentation/energykit/electricityinsightrecord/databygridcleanliness)

### Getting the tariff peak data

- [ElectricityInsightRecord.TariffPeak](/documentation/energykit/electricityinsightrecord/tariffpeak)

#### Initializing the peak energy data

- [init(superOffPeak: Measure?, offPeak: Measure?, partialPeak: Measure?, onPeak: Measure?, criticalPeak: Measure?, unknown: Measure?)](/documentation/energykit/electricityinsightrecord/tariffpeak/init(superoffpeak:offpeak:partialpeak:onpeak:criticalpeak:unknown:))

#### Getting the peak energy data

- [var criticalPeak: Measure?](/documentation/energykit/electricityinsightrecord/tariffpeak/criticalpeak)
- [var offPeak: Measure?](/documentation/energykit/electricityinsightrecord/tariffpeak/offpeak)
- [var onPeak: Measure?](/documentation/energykit/electricityinsightrecord/tariffpeak/onpeak)
- [var partialPeak: Measure?](/documentation/energykit/electricityinsightrecord/tariffpeak/partialpeak)
- [var superOffPeak: Measure?](/documentation/energykit/electricityinsightrecord/tariffpeak/superoffpeak)
- [var unknown: Measure?](/documentation/energykit/electricityinsightrecord/tariffpeak/unknown)
- [var dataByTariffPeak: ElectricityInsightRecord<Measure>.TariffPeak?](/documentation/energykit/electricityinsightrecord/databytariffpeak)

### Getting the insight record data

- [var totalRuntime: Duration?](/documentation/energykit/electricityinsightrecord/totalruntime)
- [let range: DateInterval](/documentation/energykit/electricityinsightrecord/range)
- [var totalEnergy: Measurement<UnitEnergy>?](/documentation/energykit/electricityinsightrecord/totalenergy)
- [ElectricityInsightService](/documentation/energykit/electricityinsightservice)

### Retrieving the shared instance

- [static let shared: ElectricityInsightService](/documentation/energykit/electricityinsightservice/shared)

### Getting device insights

- [func energyInsights(forDeviceID: String, using: ElectricityInsightQuery, atVenue: UUID) async throws -> AsyncStream<ElectricityInsightRecord<Measurement<UnitEnergy>>>](/documentation/energykit/electricityinsightservice/energyinsights(fordeviceid:using:atvenue:))
- [func runtimeInsights(forDeviceID: String, using: ElectricityInsightQuery, atVenue: UUID) async throws -> AsyncStream<ElectricityInsightRecord<Duration>>](/documentation/energykit/electricityinsightservice/runtimeinsights(fordeviceid:using:atvenue:))
- [ElectricityInsightQuery](/documentation/energykit/electricityinsightquery)

### Creating an insight query request

- [init(options: ElectricityInsightQuery.Options, range: DateInterval, granularity: ElectricityInsightQuery.Granularity, flowDirection: ElectricityFlowDirection)](/documentation/energykit/electricityinsightquery/init(options:range:granularity:flowdirection:))

### Adding optional insight records

- [ElectricityInsightQuery.Options](/documentation/energykit/electricityinsightquery/options-swift.struct)

#### Creating an option set

- [init(rawValue: UInt)](/documentation/energykit/electricityinsightquery/options-swift.struct/init(rawvalue:))
- [let rawValue: UInt](/documentation/energykit/electricityinsightquery/options-swift.struct/rawvalue)

#### Getting the optional query insights

- [static let cleanliness: ElectricityInsightQuery.Options](/documentation/energykit/electricityinsightquery/options-swift.struct/cleanliness)
- [static let tariff: ElectricityInsightQuery.Options](/documentation/energykit/electricityinsightquery/options-swift.struct/tariff)
- [let options: ElectricityInsightQuery.Options](/documentation/energykit/electricityinsightquery/options-swift.property)

### Getting the query request information

- [ElectricityInsightQuery.Granularity](/documentation/energykit/electricityinsightquery/granularity-swift.enum)

#### Returning electricity insight records

- [case daily](/documentation/energykit/electricityinsightquery/granularity-swift.enum/daily)
- [case hourly](/documentation/energykit/electricityinsightquery/granularity-swift.enum/hourly)
- [case monthly](/documentation/energykit/electricityinsightquery/granularity-swift.enum/monthly)
- [case weekly](/documentation/energykit/electricityinsightquery/granularity-swift.enum/weekly)
- [case yearly](/documentation/energykit/electricityinsightquery/granularity-swift.enum/yearly)
- [let granularity: ElectricityInsightQuery.Granularity](/documentation/energykit/electricityinsightquery/granularity-swift.property)
- [let flowDirection: ElectricityFlowDirection](/documentation/energykit/electricityinsightquery/flowdirection)
- [let range: DateInterval](/documentation/energykit/electricityinsightquery/range)
- [ElectricityInsightMeasure](/documentation/energykit/electricityinsightmeasure)

## Error response

- [EnergyKitError](/documentation/energykit/energykiterror)

### Viewing error reasons

- [case guidanceUnavailable](/documentation/energykit/energykiterror/guidanceunavailable)
- [case inProgress](/documentation/energykit/energykiterror/inprogress)
- [case invalidLoadEvent](/documentation/energykit/energykiterror/invalidloadevent)
- [case permissionDenied](/documentation/energykit/energykiterror/permissiondenied)
- [case serviceUnavailable](/documentation/energykit/energykiterror/serviceunavailable)
- [case venueUnavailable](/documentation/energykit/energykiterror/venueunavailable)
- [case locationServicesDenied](/documentation/energykit/energykiterror/locationservicesdenied)
- [case rateLimitExceeded](/documentation/energykit/energykiterror/ratelimitexceeded)
- [case unsupportedRegion](/documentation/energykit/energykiterror/unsupportedregion)

### Reading error messages

- [var errorDescription: String?](/documentation/energykit/energykiterror/errordescription)
- [var failureReason: String?](/documentation/energykit/energykiterror/failurereason)
- [var helpAnchor: String?](/documentation/energykit/energykiterror/helpanchor)
- [var recoverySuggestion: String?](/documentation/energykit/energykiterror/recoverysuggestion)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
