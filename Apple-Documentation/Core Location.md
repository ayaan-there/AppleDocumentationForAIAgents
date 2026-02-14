# Core Location Documentation

Source: https://sosumi.ai/documentation/corelocation

---
title: Core Location
source: https://developer.apple.com/documentation/corelocation
timestamp: 2026-02-13T19:23:11.666Z
---

## Essentials

- [Configuring your app to use location services](/documentation/corelocation/configuring-your-app-to-use-location-services)
- [Supporting live updates in SwiftUI and Mac Catalyst apps](/documentation/corelocation/supporting-live-updates-in-swiftui-and-mac-catalyst-apps)
- [CLLocationManager](/documentation/corelocation/cllocationmanager)

### Determining the availability of services

- [class func significantLocationChangeMonitoringAvailable() -> Bool](/documentation/corelocation/cllocationmanager/significantlocationchangemonitoringavailable())
- [class func headingAvailable() -> Bool](/documentation/corelocation/cllocationmanager/headingavailable())
- [var isAuthorizedForWidgetUpdates: Bool](/documentation/corelocation/cllocationmanager/isauthorizedforwidgetupdates)
- [var accuracyAuthorization: CLAccuracyAuthorization](/documentation/corelocation/cllocationmanager/accuracyauthorization)
- [class func isMonitoringAvailable(for: AnyClass) -> Bool](/documentation/corelocation/cllocationmanager/ismonitoringavailable(for:))
- [class func isRangingAvailable() -> Bool](/documentation/corelocation/cllocationmanager/israngingavailable())
- [class func locationServicesEnabled() -> Bool](/documentation/corelocation/cllocationmanager/locationservicesenabled())

#### Related Documentation

- [func locationManager(CLLocationManager, didFailWithError: any Error)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didfailwitherror:))
- [func locationManager(CLLocationManager, monitoringDidFailFor: CLRegion?, withError: any Error)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:monitoringdidfailfor:witherror:))

### Receiving data from location services

- [var delegate: (any CLLocationManagerDelegate)?](/documentation/corelocation/cllocationmanager/delegate)
- [CLLocationManagerDelegate](/documentation/corelocation/cllocationmanagerdelegate)

#### Responding to authorization changes

- [func locationManagerDidChangeAuthorization(CLLocationManager)](/documentation/corelocation/cllocationmanagerdelegate/locationmanagerdidchangeauthorization(_:))
- [func locationManager(CLLocationManager, didChangeAuthorization: CLAuthorizationStatus)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didchangeauthorization:))

#### Handling errors

- [func locationManager(CLLocationManager, didFailWithError: any Error)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didfailwitherror:))

#### Receiving location updates

- [func locationManager(CLLocationManager, didUpdateLocations: [CLLocation])](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didupdatelocations:))

##### Related Documentation

- [MapKit](/documentation/mapkit)
- [MapKit JS](/documentation/mapkitjs)
- [func locationManager(CLLocationManager, didUpdateTo: CLLocation, from: CLLocation)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didupdateto:from:))
- [func locationManager(CLLocationManager, didFinishDeferredUpdatesWithError: (any Error)?)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didfinishdeferredupdateswitherror:))

#### Pausing location updates

- [func locationManagerDidPauseLocationUpdates(CLLocationManager)](/documentation/corelocation/cllocationmanagerdelegate/locationmanagerdidpauselocationupdates(_:))
- [func locationManagerDidResumeLocationUpdates(CLLocationManager)](/documentation/corelocation/cllocationmanagerdelegate/locationmanagerdidresumelocationupdates(_:))

#### Receiving visit updates

- [func locationManager(CLLocationManager, didVisit: CLVisit)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didvisit:))

#### Receiving heading updates

- [func locationManager(CLLocationManager, didUpdateHeading: CLHeading)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didupdateheading:))
- [func locationManagerShouldDisplayHeadingCalibration(CLLocationManager) -> Bool](/documentation/corelocation/cllocationmanagerdelegate/locationmanagershoulddisplayheadingcalibration(_:))

#### Receiving region-related updates

- [func locationManager(CLLocationManager, didEnterRegion: CLRegion)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didenterregion:))
- [func locationManager(CLLocationManager, didExitRegion: CLRegion)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didexitregion:))
- [func locationManager(CLLocationManager, didDetermineState: CLRegionState, for: CLRegion)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:diddeterminestate:for:))
- [func locationManager(CLLocationManager, monitoringDidFailFor: CLRegion?, withError: any Error)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:monitoringdidfailfor:witherror:))
- [func locationManager(CLLocationManager, didStartMonitoringFor: CLRegion)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didstartmonitoringfor:))
- [CLRegionState](/documentation/corelocation/clregionstate)

##### Region States

- [case unknown](/documentation/corelocation/clregionstate/unknown)
- [case inside](/documentation/corelocation/clregionstate/inside)
- [case outside](/documentation/corelocation/clregionstate/outside)

##### Initializers

- [init?(rawValue: Int)](/documentation/corelocation/clregionstate/init(rawvalue:))

#### Receiving beacon-related updates

- [func locationManager(CLLocationManager, didRange: [CLBeacon], satisfying: CLBeaconIdentityConstraint)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didrange:satisfying:))
- [func locationManager(CLLocationManager, didFailRangingFor: CLBeaconIdentityConstraint, error: any Error)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didfailrangingfor:error:))
- [func locationManager(CLLocationManager, didRangeBeacons: [CLBeacon], in: CLBeaconRegion)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:didrangebeacons:in:))
- [func locationManager(CLLocationManager, rangingBeaconsDidFailFor: CLBeaconRegion, withError: any Error)](/documentation/corelocation/cllocationmanagerdelegate/locationmanager(_:rangingbeaconsdidfailfor:witherror:))

### Requesting authorization for location services

- [func requestWhenInUseAuthorization()](/documentation/corelocation/cllocationmanager/requestwheninuseauthorization())

#### Related Documentation

- [Handling location updates in the background](/documentation/corelocation/handling-location-updates-in-the-background)
- [NSLocationWhenInUseUsageDescription](/documentation/bundleresources/information-property-list/nslocationwheninuseusagedescription)
- [func requestAlwaysAuthorization()](/documentation/corelocation/cllocationmanager/requestalwaysauthorization())

#### Related Documentation

- [NSLocationAlwaysUsageDescription](/documentation/bundleresources/information-property-list/nslocationalwaysusagedescription)
- [func requestTemporaryFullAccuracyAuthorization(withPurposeKey: String, completion: (((any Error)?) -> Void)?)](/documentation/corelocation/cllocationmanager/requesttemporaryfullaccuracyauthorization(withpurposekey:completion:))
- [func requestTemporaryFullAccuracyAuthorization(withPurposeKey: String)](/documentation/corelocation/cllocationmanager/requesttemporaryfullaccuracyauthorization(withpurposekey:))
- [var authorizationStatus: CLAuthorizationStatus](/documentation/corelocation/cllocationmanager/authorizationstatus-swift.property)
- [CLAuthorizationStatus](/documentation/corelocation/clauthorizationstatus)

#### Getting the authorization status

- [case notDetermined](/documentation/corelocation/clauthorizationstatus/notdetermined)
- [case restricted](/documentation/corelocation/clauthorizationstatus/restricted)
- [case denied](/documentation/corelocation/clauthorizationstatus/denied)
- [static var authorized: CLAuthorizationStatus](/documentation/corelocation/clauthorizationstatus/authorized)
- [case authorizedAlways](/documentation/corelocation/clauthorizationstatus/authorizedalways)
- [case authorizedWhenInUse](/documentation/corelocation/clauthorizationstatus/authorizedwheninuse)

#### Initializers

- [init?(rawValue: Int32)](/documentation/corelocation/clauthorizationstatus/init(rawvalue:))
- [NSLocationDefaultAccuracyReduced](/documentation/bundleresources/information-property-list/nslocationdefaultaccuracyreduced)
- [NSLocationAlwaysAndWhenInUseUsageDescription](/documentation/bundleresources/information-property-list/nslocationalwaysandwheninuseusagedescription)

### Specifying distance and accuracy

- [var distanceFilter: CLLocationDistance](/documentation/corelocation/cllocationmanager/distancefilter)
- [let CLLocationDistanceMax: CLLocationDistance](/documentation/corelocation/cllocationdistancemax)
- [let kCLDistanceFilterNone: CLLocationDistance](/documentation/corelocation/kcldistancefilternone)
- [CLLocationDistance](/documentation/corelocation/cllocationdistance)
- [var desiredAccuracy: CLLocationAccuracy](/documentation/corelocation/cllocationmanager/desiredaccuracy)
- [CLLocationAccuracy](/documentation/corelocation/cllocationaccuracy)

#### Desired Accuracy Constants

- [let kCLLocationAccuracyBestForNavigation: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracybestfornavigation)
- [let kCLLocationAccuracyBest: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracybest)
- [let kCLLocationAccuracyNearestTenMeters: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracynearesttenmeters)
- [let kCLLocationAccuracyHundredMeters: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracyhundredmeters)
- [let kCLLocationAccuracyKilometer: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracykilometer)
- [let kCLLocationAccuracyThreeKilometers: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracythreekilometers)
- [let kCLLocationAccuracyReduced: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracyreduced)

### Running the standard location service

- [func startUpdatingLocation()](/documentation/corelocation/cllocationmanager/startupdatinglocation())
- [func stopUpdatingLocation()](/documentation/corelocation/cllocationmanager/stopupdatinglocation())
- [func requestLocation()](/documentation/corelocation/cllocationmanager/requestlocation())
- [var pausesLocationUpdatesAutomatically: Bool](/documentation/corelocation/cllocationmanager/pauseslocationupdatesautomatically)
- [var allowsBackgroundLocationUpdates: Bool](/documentation/corelocation/cllocationmanager/allowsbackgroundlocationupdates)
- [var showsBackgroundLocationIndicator: Bool](/documentation/corelocation/cllocationmanager/showsbackgroundlocationindicator)
- [var activityType: CLActivityType](/documentation/corelocation/cllocationmanager/activitytype)
- [CLActivityType](/documentation/corelocation/clactivitytype)

#### Activity types

- [case other](/documentation/corelocation/clactivitytype/other)
- [case automotiveNavigation](/documentation/corelocation/clactivitytype/automotivenavigation)
- [case fitness](/documentation/corelocation/clactivitytype/fitness)
- [case otherNavigation](/documentation/corelocation/clactivitytype/othernavigation)
- [case airborne](/documentation/corelocation/clactivitytype/airborne)

#### Initializers

- [init?(rawValue: Int)](/documentation/corelocation/clactivitytype/init(rawvalue:))

### Running the significant change location service

- [func startMonitoringSignificantLocationChanges()](/documentation/corelocation/cllocationmanager/startmonitoringsignificantlocationchanges())
- [func stopMonitoringSignificantLocationChanges()](/documentation/corelocation/cllocationmanager/stopmonitoringsignificantlocationchanges())

### Running the visits location service

- [func startMonitoringVisits()](/documentation/corelocation/cllocationmanager/startmonitoringvisits())
- [func stopMonitoringVisits()](/documentation/corelocation/cllocationmanager/stopmonitoringvisits())

### Running the heading service

- [func startUpdatingHeading()](/documentation/corelocation/cllocationmanager/startupdatingheading())

#### Related Documentation

- [var headingAvailable: Bool](/documentation/corelocation/cllocationmanager/headingavailable-swift.property)
- [func stopUpdatingHeading()](/documentation/corelocation/cllocationmanager/stopupdatingheading())
- [func dismissHeadingCalibrationDisplay()](/documentation/corelocation/cllocationmanager/dismissheadingcalibrationdisplay())
- [var headingFilter: CLLocationDegrees](/documentation/corelocation/cllocationmanager/headingfilter)
- [let kCLHeadingFilterNone: CLLocationDegrees](/documentation/corelocation/kclheadingfilternone)
- [CLLocationDegrees](/documentation/corelocation/cllocationdegrees)
- [var headingOrientation: CLDeviceOrientation](/documentation/corelocation/cllocationmanager/headingorientation)
- [CLDeviceOrientation](/documentation/corelocation/cldeviceorientation)

#### Device Orientations

- [case unknown](/documentation/corelocation/cldeviceorientation/unknown)
- [case portrait](/documentation/corelocation/cldeviceorientation/portrait)
- [case portraitUpsideDown](/documentation/corelocation/cldeviceorientation/portraitupsidedown)
- [case landscapeLeft](/documentation/corelocation/cldeviceorientation/landscapeleft)
- [case landscapeRight](/documentation/corelocation/cldeviceorientation/landscaperight)
- [case faceUp](/documentation/corelocation/cldeviceorientation/faceup)
- [case faceDown](/documentation/corelocation/cldeviceorientation/facedown)

#### Initializers

- [init?(rawValue: Int32)](/documentation/corelocation/cldeviceorientation/init(rawvalue:))

### Running the region-monitoring service

- [var monitoredRegions: Set<CLRegion>](/documentation/corelocation/cllocationmanager/monitoredregions)
- [var maximumRegionMonitoringDistance: CLLocationDistance](/documentation/corelocation/cllocationmanager/maximumregionmonitoringdistance)

### Performing beacon ranging

- [func startRangingBeacons(satisfying: CLBeaconIdentityConstraint)](/documentation/corelocation/cllocationmanager/startrangingbeacons(satisfying:))
- [func stopRangingBeacons(satisfying: CLBeaconIdentityConstraint)](/documentation/corelocation/cllocationmanager/stoprangingbeacons(satisfying:))
- [var rangedBeaconConstraints: Set<CLBeaconIdentityConstraint>](/documentation/corelocation/cllocationmanager/rangedbeaconconstraints)

### Monitoring location push notifications

- [func startMonitoringLocationPushes(completion: ((Data?, (any Error)?) -> Void)?)](/documentation/corelocation/cllocationmanager/startmonitoringlocationpushes(completion:))
- [func stopMonitoringLocationPushes()](/documentation/corelocation/cllocationmanager/stopmonitoringlocationpushes())

### Getting recent location and heading data

- [var location: CLLocation?](/documentation/corelocation/cllocationmanager/location)

#### Related Documentation

- [func startUpdatingLocation()](/documentation/corelocation/cllocationmanager/startupdatinglocation())
- [var heading: CLHeading?](/documentation/corelocation/cllocationmanager/heading)

### Deferring location updates

- [let CLTimeIntervalMax: TimeInterval](/documentation/corelocation/cltimeintervalmax)

### Deprecated

- [Deprecated symbols](/documentation/corelocation/deprecated-symbols)

#### Properties

- [var headingAvailable: Bool](/documentation/corelocation/cllocationmanager/headingavailable-swift.property)
- [var locationServicesEnabled: Bool](/documentation/corelocation/cllocationmanager/locationservicesenabled-swift.property)
- [var purpose: String?](/documentation/corelocation/cllocationmanager/purpose)
- [var rangedRegions: Set<CLRegion>](/documentation/corelocation/cllocationmanager/rangedregions)

##### Related Documentation

- [func startRangingBeacons(in: CLBeaconRegion)](/documentation/corelocation/cllocationmanager/startrangingbeacons(in:))

#### Methods

- [func startMonitoring(for: CLRegion)](/documentation/corelocation/cllocationmanager/startmonitoring(for:))
- [func stopMonitoring(for: CLRegion)](/documentation/corelocation/cllocationmanager/stopmonitoring(for:))
- [class func regionMonitoringAvailable() -> Bool](/documentation/corelocation/cllocationmanager/regionmonitoringavailable())
- [class func regionMonitoringEnabled() -> Bool](/documentation/corelocation/cllocationmanager/regionmonitoringenabled())
- [class func authorizationStatus() -> CLAuthorizationStatus](/documentation/corelocation/cllocationmanager/authorizationstatus())
- [func startMonitoring(for: CLRegion, desiredAccuracy: CLLocationAccuracy)](/documentation/corelocation/cllocationmanager/startmonitoring(for:desiredaccuracy:))
- [func requestState(for: CLRegion)](/documentation/corelocation/cllocationmanager/requeststate(for:))
- [func startRangingBeacons(in: CLBeaconRegion)](/documentation/corelocation/cllocationmanager/startrangingbeacons(in:))
- [func stopRangingBeacons(in: CLBeaconRegion)](/documentation/corelocation/cllocationmanager/stoprangingbeacons(in:))
- [class func deferredLocationUpdatesAvailable() -> Bool](/documentation/corelocation/cllocationmanager/deferredlocationupdatesavailable())
- [func allowDeferredLocationUpdates(untilTraveled: CLLocationDistance, timeout: TimeInterval)](/documentation/corelocation/cllocationmanager/allowdeferredlocationupdates(untiltraveled:timeout:))
- [func disallowDeferredLocationUpdates()](/documentation/corelocation/cllocationmanager/disallowdeferredlocationupdates())

### Instance Methods

- [func requestHistoricalLocations(purposeKey: String, sampleCount: Int, completionHandler: ([CLLocation], (any Error)?) -> Void)](/documentation/corelocation/cllocationmanager/requesthistoricallocations(purposekey:samplecount:completionhandler:))
- [CLBackgroundActivitySession](/documentation/corelocation/clbackgroundactivitysession-3mzv3)

### Creating a background activity session

- [init()](/documentation/corelocation/clbackgroundactivitysession-3mzv3/init())

### Ending the session

- [func invalidate()](/documentation/corelocation/clbackgroundactivitysession-3mzv3/invalidate())

### Classes

- [CLBackgroundActivitySession.Diagnostics](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostics-swift.class)

#### Structures

- [CLBackgroundActivitySession.Diagnostics.Iterator](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostics-swift.class/iterator)

### Structures

- [CLBackgroundActivitySession.Diagnostic](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostic)

#### Instance Properties

- [var authorizationDenied: Bool](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostic/authorizationdenied)
- [var authorizationDeniedGlobally: Bool](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostic/authorizationdeniedglobally)
- [var authorizationRequestInProgress: Bool](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostic/authorizationrequestinprogress)
- [var authorizationRestricted: Bool](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostic/authorizationrestricted)
- [var insufficientlyInUse: Bool](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostic/insufficientlyinuse)
- [var serviceSessionRequired: Bool](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostic/servicesessionrequired)

### Instance Properties

- [var diagnostics: CLBackgroundActivitySession.Diagnostics](/documentation/corelocation/clbackgroundactivitysession-3mzv3/diagnostics-swift.property)
- [CLLocationUpdate](/documentation/corelocation/cllocationupdate)

### Determining movement and location

- [var isStationary: Bool](/documentation/corelocation/cllocationupdate/isstationary)
- [var location: CLLocation?](/documentation/corelocation/cllocationupdate/location)

### Receiving location updates

- [static func liveUpdates(CLLocationUpdate.LiveConfiguration) -> CLLocationUpdate.Updates](/documentation/corelocation/cllocationupdate/liveupdates(_:))
- [CLLocationUpdate.LiveConfiguration](/documentation/corelocation/cllocationupdate/liveconfiguration)

#### Location types

- [case `default`](/documentation/corelocation/cllocationupdate/liveconfiguration/default)
- [case airborne](/documentation/corelocation/cllocationupdate/liveconfiguration/airborne)
- [case automotiveNavigation](/documentation/corelocation/cllocationupdate/liveconfiguration/automotivenavigation)
- [case fitness](/documentation/corelocation/cllocationupdate/liveconfiguration/fitness)
- [case otherNavigation](/documentation/corelocation/cllocationupdate/liveconfiguration/othernavigation)
- [CLLocationUpdate.Updates](/documentation/corelocation/cllocationupdate/updates)

#### Type aliases

- [CLLocationUpdate.Updates.Iterator](/documentation/corelocation/cllocationupdate/updates/iterator)

### Instance Properties

- [var accuracyLimited: Bool](/documentation/corelocation/cllocationupdate/accuracylimited)
- [var authorizationDenied: Bool](/documentation/corelocation/cllocationupdate/authorizationdenied)
- [var authorizationDeniedGlobally: Bool](/documentation/corelocation/cllocationupdate/authorizationdeniedglobally)
- [var authorizationRequestInProgress: Bool](/documentation/corelocation/cllocationupdate/authorizationrequestinprogress)
- [var authorizationRestricted: Bool](/documentation/corelocation/cllocationupdate/authorizationrestricted)
- [var insufficientlyInUse: Bool](/documentation/corelocation/cllocationupdate/insufficientlyinuse)
- [var locationUnavailable: Bool](/documentation/corelocation/cllocationupdate/locationunavailable)
- [var serviceSessionRequired: Bool](/documentation/corelocation/cllocationupdate/servicesessionrequired)
- [var stationary: Bool](/documentation/corelocation/cllocationupdate/stationary)
- [Adopting live updates in Core Location](/documentation/corelocation/adopting-live-updates-in-core-location)
- [Monitoring location changes with Core Location](/documentation/corelocation/monitoring-location-changes-with-core-location)

## Authorization

- [Requesting authorization to use location services](/documentation/corelocation/requesting-authorization-to-use-location-services)
- [Suspending authorization requests](/documentation/corelocation/suspending-authorization-requests)
- [CLAuthorizationStatus](/documentation/corelocation/clauthorizationstatus)

### Getting the authorization status

- [case notDetermined](/documentation/corelocation/clauthorizationstatus/notdetermined)
- [case restricted](/documentation/corelocation/clauthorizationstatus/restricted)
- [case denied](/documentation/corelocation/clauthorizationstatus/denied)
- [static var authorized: CLAuthorizationStatus](/documentation/corelocation/clauthorizationstatus/authorized)
- [case authorizedAlways](/documentation/corelocation/clauthorizationstatus/authorizedalways)
- [case authorizedWhenInUse](/documentation/corelocation/clauthorizationstatus/authorizedwheninuse)

### Initializers

- [init?(rawValue: Int32)](/documentation/corelocation/clauthorizationstatus/init(rawvalue:))
- [CLAccuracyAuthorization](/documentation/corelocation/claccuracyauthorization)

### Getting the location accuracy

- [case fullAccuracy](/documentation/corelocation/claccuracyauthorization/fullaccuracy)

#### Related Documentation

- [var accuracyAuthorization: CLAccuracyAuthorization](/documentation/corelocation/cllocationmanager/accuracyauthorization)
- [case reducedAccuracy](/documentation/corelocation/claccuracyauthorization/reducedaccuracy)

#### Related Documentation

- [var accuracyAuthorization: CLAccuracyAuthorization](/documentation/corelocation/cllocationmanager/accuracyauthorization)

### Initializers

- [init?(rawValue: Int)](/documentation/corelocation/claccuracyauthorization/init(rawvalue:))
- [NSLocationAlwaysAndWhenInUseUsageDescription](/documentation/bundleresources/information-property-list/nslocationalwaysandwheninuseusagedescription)
- [NSLocationWhenInUseUsageDescription](/documentation/bundleresources/information-property-list/nslocationwheninuseusagedescription)
- [NSLocationUsageDescription](/documentation/bundleresources/information-property-list/nslocationusagedescription)
- [NSLocationDefaultAccuracyReduced](/documentation/bundleresources/information-property-list/nslocationdefaultaccuracyreduced)
- [NSLocationAlwaysUsageDescription](/documentation/bundleresources/information-property-list/nslocationalwaysusagedescription)

## Monitoring

- [CLMonitor](/documentation/corelocation/clmonitor-2r51v)

### Creating a monitor

- [init(String) async](/documentation/corelocation/clmonitor-2r51v/init(_:))

### Adding and removing conditions

- [func add(any CLCondition, identifier: String)](/documentation/corelocation/clmonitor-2r51v/add(_:identifier:))
- [func add(any CLCondition, identifier: String, assuming: CLMonitor.Event.State)](/documentation/corelocation/clmonitor-2r51v/add(_:identifier:assuming:))
- [func record(for: String) -> CLMonitor.Record?](/documentation/corelocation/clmonitor-2r51v/record(for:))
- [func remove(String)](/documentation/corelocation/clmonitor-2r51v/remove(_:))

### Accessing the location monitor’s identifiers

- [var identifiers: [String]](/documentation/corelocation/clmonitor-2r51v/identifiers)

### Accessing the monitor’s events

- [let events: CLMonitor.Events](/documentation/corelocation/clmonitor-2r51v/events-swift.property)

### Monitor conditions

- [CLMonitor.BeaconIdentityCondition](/documentation/corelocation/clmonitor-2r51v/beaconidentitycondition)

#### Creating a beacon identity condition

- [init(uuid: UUID)](/documentation/corelocation/clmonitor-2r51v/beaconidentitycondition/init(uuid:))
- [init(uuid: UUID, major: UInt16)](/documentation/corelocation/clmonitor-2r51v/beaconidentitycondition/init(uuid:major:))
- [init(uuid: UUID, major: UInt16, minor: UInt16)](/documentation/corelocation/clmonitor-2r51v/beaconidentitycondition/init(uuid:major:minor:))

#### Instance Properties

- [let major: UInt16?](/documentation/corelocation/clmonitor-2r51v/beaconidentitycondition/major)
- [let minor: UInt16?](/documentation/corelocation/clmonitor-2r51v/beaconidentitycondition/minor)
- [let uuid: UUID](/documentation/corelocation/clmonitor-2r51v/beaconidentitycondition/uuid)
- [CLMonitor.CircularGeographicCondition](/documentation/corelocation/clmonitor-2r51v/circulargeographiccondition)

#### Creating a circular geographic condition

- [init(center: CLLocationCoordinate2D, radius: CLLocationDistance)](/documentation/corelocation/clmonitor-2r51v/circulargeographiccondition/init(center:radius:))

#### Condition characteristics

- [let center: CLLocationCoordinate2D](/documentation/corelocation/clmonitor-2r51v/circulargeographiccondition/center)
- [let radius: CLLocationDistance](/documentation/corelocation/clmonitor-2r51v/circulargeographiccondition/radius)

### Monitor events

- [CLMonitor.Event](/documentation/corelocation/clmonitor-2r51v/event)

#### Event states

- [var accuracyLimited: Bool](/documentation/corelocation/clmonitor-2r51v/event/accuracylimited)
- [var authorizationDenied: Bool](/documentation/corelocation/clmonitor-2r51v/event/authorizationdenied)
- [var authorizationDeniedGlobally: Bool](/documentation/corelocation/clmonitor-2r51v/event/authorizationdeniedglobally)
- [var authorizationRequestInProgress: Bool](/documentation/corelocation/clmonitor-2r51v/event/authorizationrequestinprogress)
- [var authorizationRestricted: Bool](/documentation/corelocation/clmonitor-2r51v/event/authorizationrestricted)
- [var conditionLimitExceeded: Bool](/documentation/corelocation/clmonitor-2r51v/event/conditionlimitexceeded)
- [var conditionUnsupported: Bool](/documentation/corelocation/clmonitor-2r51v/event/conditionunsupported)
- [var insufficientlyInUse: Bool](/documentation/corelocation/clmonitor-2r51v/event/insufficientlyinuse)
- [var persistenceUnavailable: Bool](/documentation/corelocation/clmonitor-2r51v/event/persistenceunavailable)
- [var serviceSessionRequired: Bool](/documentation/corelocation/clmonitor-2r51v/event/servicesessionrequired)

#### Event characteristics

- [var date: Date](/documentation/corelocation/clmonitor-2r51v/event/date)
- [var identifier: String](/documentation/corelocation/clmonitor-2r51v/event/identifier)
- [let refinement: (any CLCondition)?](/documentation/corelocation/clmonitor-2r51v/event/refinement)
- [var state: CLMonitor.Event.State](/documentation/corelocation/clmonitor-2r51v/event/state-swift.property)

#### Type aliases

- [CLMonitor.Event.State](/documentation/corelocation/clmonitor-2r51v/event/state-swift.typealias)
- [CLMonitor.Record](/documentation/corelocation/clmonitor-2r51v/record)

#### Record characteristics

- [let condition: any CLCondition](/documentation/corelocation/clmonitor-2r51v/record/condition)
- [let lastEvent: CLMonitor.Event](/documentation/corelocation/clmonitor-2r51v/record/lastevent)
- [CLMonitor.Events](/documentation/corelocation/clmonitor-2r51v/events-swift.struct)

#### Utility methods

- [CLMonitor.Events.Iterator](/documentation/corelocation/clmonitor-2r51v/events-swift.struct/iterator)

## Location updates

- [Getting the current location of a device](/documentation/corelocation/getting-the-current-location-of-a-device)
- [Handling location updates in the background](/documentation/corelocation/handling-location-updates-in-the-background)
- [Creating a location push service extension](/documentation/corelocation/creating-a-location-push-service-extension)
- [CLLocation](/documentation/corelocation/cllocation)

### Creating a location object

- [init(latitude: CLLocationDegrees, longitude: CLLocationDegrees)](/documentation/corelocation/cllocation/init(latitude:longitude:))
- [init(coordinate: CLLocationCoordinate2D, altitude: CLLocationDistance, horizontalAccuracy: CLLocationAccuracy, verticalAccuracy: CLLocationAccuracy, timestamp: Date)](/documentation/corelocation/cllocation/init(coordinate:altitude:horizontalaccuracy:verticalaccuracy:timestamp:))
- [init(coordinate: CLLocationCoordinate2D, altitude: CLLocationDistance, horizontalAccuracy: CLLocationAccuracy, verticalAccuracy: CLLocationAccuracy, course: CLLocationDirection, speed: CLLocationSpeed, timestamp: Date)](/documentation/corelocation/cllocation/init(coordinate:altitude:horizontalaccuracy:verticalaccuracy:course:speed:timestamp:))
- [init(coordinate: CLLocationCoordinate2D, altitude: CLLocationDistance, horizontalAccuracy: CLLocationAccuracy, verticalAccuracy: CLLocationAccuracy, course: CLLocationDirection, courseAccuracy: CLLocationDirectionAccuracy, speed: CLLocationSpeed, speedAccuracy: CLLocationSpeedAccuracy, timestamp: Date)](/documentation/corelocation/cllocation/init(coordinate:altitude:horizontalaccuracy:verticalaccuracy:course:courseaccuracy:speed:speedaccuracy:timestamp:))
- [init(coordinate: CLLocationCoordinate2D, altitude: CLLocationDistance, horizontalAccuracy: CLLocationAccuracy, verticalAccuracy: CLLocationAccuracy, course: CLLocationDirection, courseAccuracy: CLLocationDirectionAccuracy, speed: CLLocationSpeed, speedAccuracy: CLLocationSpeedAccuracy, timestamp: Date, sourceInfo: CLLocationSourceInformation)](/documentation/corelocation/cllocation/init(coordinate:altitude:horizontalaccuracy:verticalaccuracy:course:courseaccuracy:speed:speedaccuracy:timestamp:sourceinfo:))

### Getting the location attributes

- [var coordinate: CLLocationCoordinate2D](/documentation/corelocation/cllocation/coordinate)
- [var altitude: CLLocationDistance](/documentation/corelocation/cllocation/altitude)
- [var ellipsoidalAltitude: CLLocationDistance](/documentation/corelocation/cllocation/ellipsoidalaltitude)
- [CLLocationDistance](/documentation/corelocation/cllocationdistance)
- [var floor: CLFloor?](/documentation/corelocation/cllocation/floor)
- [var timestamp: Date](/documentation/corelocation/cllocation/timestamp)
- [var sourceInformation: CLLocationSourceInformation?](/documentation/corelocation/cllocation/sourceinformation)

### Getting the location accuracy

- [var horizontalAccuracy: CLLocationAccuracy](/documentation/corelocation/cllocation/horizontalaccuracy)
- [var verticalAccuracy: CLLocationAccuracy](/documentation/corelocation/cllocation/verticalaccuracy)
- [CLLocationAccuracy](/documentation/corelocation/cllocationaccuracy)

#### Desired Accuracy Constants

- [let kCLLocationAccuracyBestForNavigation: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracybestfornavigation)
- [let kCLLocationAccuracyBest: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracybest)
- [let kCLLocationAccuracyNearestTenMeters: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracynearesttenmeters)
- [let kCLLocationAccuracyHundredMeters: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracyhundredmeters)
- [let kCLLocationAccuracyKilometer: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracykilometer)
- [let kCLLocationAccuracyThreeKilometers: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracythreekilometers)
- [let kCLLocationAccuracyReduced: CLLocationAccuracy](/documentation/corelocation/kcllocationaccuracyreduced)

### Measuring the distance between coordinates

- [func distance(from: CLLocation) -> CLLocationDistance](/documentation/corelocation/cllocation/distance(from:))
- [func getDistanceFrom(CLLocation) -> CLLocationDistance](/documentation/corelocation/cllocation/getdistancefrom(_:))

### Getting speed and course information

- [var speed: CLLocationSpeed](/documentation/corelocation/cllocation/speed)
- [var speedAccuracy: CLLocationSpeedAccuracy](/documentation/corelocation/cllocation/speedaccuracy)
- [var course: CLLocationDirection](/documentation/corelocation/cllocation/course)
- [var courseAccuracy: CLLocationDirectionAccuracy](/documentation/corelocation/cllocation/courseaccuracy)
- [CLLocationSpeed](/documentation/corelocation/cllocationspeed)
- [CLLocationDirection](/documentation/corelocation/cllocationdirection)
- [CLLocationSpeedAccuracy](/documentation/corelocation/cllocationspeedaccuracy)
- [CLLocationDirectionAccuracy](/documentation/corelocation/cllocationdirectionaccuracy)
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)

### Creating a location coordinate

- [init()](/documentation/corelocation/cllocationcoordinate2d/init())
- [init(latitude: CLLocationDegrees, longitude: CLLocationDegrees)](/documentation/corelocation/cllocationcoordinate2d/init(latitude:longitude:))
- [func CLLocationCoordinate2DMake(CLLocationDegrees, CLLocationDegrees) -> CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2dmake(_:_:))

### Getting the geographic coordinates

- [var latitude: CLLocationDegrees](/documentation/corelocation/cllocationcoordinate2d/latitude)
- [var longitude: CLLocationDegrees](/documentation/corelocation/cllocationcoordinate2d/longitude)

### Validating a coordinate

- [func CLLocationCoordinate2DIsValid(CLLocationCoordinate2D) -> Bool](/documentation/corelocation/cllocationcoordinate2disvalid(_:))
- [let kCLLocationCoordinate2DInvalid: CLLocationCoordinate2D](/documentation/corelocation/kcllocationcoordinate2dinvalid)
- [CLFloor](/documentation/corelocation/clfloor)

### Getting the floor level

- [var level: Int](/documentation/corelocation/clfloor/level)
- [CLVisit](/documentation/corelocation/clvisit)

### Getting the location

- [var coordinate: CLLocationCoordinate2D](/documentation/corelocation/clvisit/coordinate)
- [var horizontalAccuracy: CLLocationAccuracy](/documentation/corelocation/clvisit/horizontalaccuracy)

### Getting the visit duration

- [var arrivalDate: Date](/documentation/corelocation/clvisit/arrivaldate)
- [var departureDate: Date](/documentation/corelocation/clvisit/departuredate)
- [CLLocationSourceInformation](/documentation/corelocation/cllocationsourceinformation)

### Creating a location source information object

- [init(softwareSimulationState: Bool, andExternalAccessoryState: Bool)](/documentation/corelocation/cllocationsourceinformation/init(softwaresimulationstate:andexternalaccessorystate:))

### Identifying the source of location data

- [var isProducedByAccessory: Bool](/documentation/corelocation/cllocationsourceinformation/isproducedbyaccessory)
- [var isSimulatedBySoftware: Bool](/documentation/corelocation/cllocationsourceinformation/issimulatedbysoftware)
- [Monitoring location changes with Core Location](/documentation/corelocation/monitoring-location-changes-with-core-location)
- [CLServiceSession](/documentation/corelocation/clservicesession-pt7n)

### Classes

- [CLServiceSession.Diagnostics](/documentation/corelocation/clservicesession-pt7n/diagnostics-swift.class)

#### Structures

- [CLServiceSession.Diagnostics.Iterator](/documentation/corelocation/clservicesession-pt7n/diagnostics-swift.class/iterator)

### Structures

- [CLServiceSession.Diagnostic](/documentation/corelocation/clservicesession-pt7n/diagnostic)

#### Instance Properties

- [var alwaysAuthorizationDenied: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/alwaysauthorizationdenied)
- [var authorizationDenied: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/authorizationdenied)
- [var authorizationDeniedGlobally: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/authorizationdeniedglobally)
- [var authorizationRequestInProgress: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/authorizationrequestinprogress)
- [var authorizationRestricted: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/authorizationrestricted)
- [var fullAccuracyDenied: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/fullaccuracydenied)
- [var insufficientlyInUse: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/insufficientlyinuse)
- [var serviceSessionRequired: Bool](/documentation/corelocation/clservicesession-pt7n/diagnostic/servicesessionrequired)

### Initializers

- [init(authorization: CLServiceSession.AuthorizationRequirement)](/documentation/corelocation/clservicesession-pt7n/init(authorization:))
- [init(authorization: CLServiceSession.AuthorizationRequirement, fullAccuracyPurposeKey: String)](/documentation/corelocation/clservicesession-pt7n/init(authorization:fullaccuracypurposekey:))

### Instance Properties

- [var diagnostics: CLServiceSession.Diagnostics](/documentation/corelocation/clservicesession-pt7n/diagnostics-swift.property)

### Instance Methods

- [func invalidate()](/documentation/corelocation/clservicesession-pt7n/invalidate())

### Enumerations

- [CLServiceSession.AuthorizationRequirement](/documentation/corelocation/clservicesession-pt7n/authorizationrequirement)

#### Enumeration Cases

- [case always](/documentation/corelocation/clservicesession-pt7n/authorizationrequirement/always)
- [case none](/documentation/corelocation/clservicesession-pt7n/authorizationrequirement/none)
- [case whenInUse](/documentation/corelocation/clservicesession-pt7n/authorizationrequirement/wheninuse)

## Region monitoring

- [Monitoring the user’s proximity to geographic regions](/documentation/corelocation/monitoring-the-user-s-proximity-to-geographic-regions)
- [CLRegion](/documentation/corelocation/clregion)

### Getting the region identifier

- [var identifier: String](/documentation/corelocation/clregion/identifier)

### Specifying the notification conditions

- [var notifyOnEntry: Bool](/documentation/corelocation/clregion/notifyonentry)
- [var notifyOnExit: Bool](/documentation/corelocation/clregion/notifyonexit)

### Deprecated

- [init(circularRegionWithCenter: CLLocationCoordinate2D, radius: CLLocationDistance, identifier: String)](/documentation/corelocation/clregion/init(circularregionwithcenter:radius:identifier:))
- [func contains(CLLocationCoordinate2D) -> Bool](/documentation/corelocation/clregion/contains(_:))
- [var center: CLLocationCoordinate2D](/documentation/corelocation/clregion/center)
- [var radius: CLLocationDistance](/documentation/corelocation/clregion/radius)

## iBeacon

- [Ranging for Beacons](/documentation/corelocation/ranging-for-beacons)
- [Determining the proximity to an iBeacon device](/documentation/corelocation/determining-the-proximity-to-an-ibeacon-device)
- [Turning an iOS device into an iBeacon device](/documentation/corelocation/turning-an-ios-device-into-an-ibeacon-device)
- [CLBeacon](/documentation/corelocation/clbeacon)

### Getting the beacon identity

- [var uuid: UUID](/documentation/corelocation/clbeacon/uuid)
- [var major: NSNumber](/documentation/corelocation/clbeacon/major)
- [var minor: NSNumber](/documentation/corelocation/clbeacon/minor)
- [var proximityUUID: UUID](/documentation/corelocation/clbeacon/proximityuuid)

### Determining the distance to the beacon

- [var proximity: CLProximity](/documentation/corelocation/clbeacon/proximity)
- [CLProximity](/documentation/corelocation/clproximity)

#### Proximity Values

- [case unknown](/documentation/corelocation/clproximity/unknown)
- [case immediate](/documentation/corelocation/clproximity/immediate)
- [case near](/documentation/corelocation/clproximity/near)
- [case far](/documentation/corelocation/clproximity/far)

#### Initializers

- [init?(rawValue: Int)](/documentation/corelocation/clproximity/init(rawvalue:))
- [var accuracy: CLLocationAccuracy](/documentation/corelocation/clbeacon/accuracy)
- [var rssi: Int](/documentation/corelocation/clbeacon/rssi)

### Getting the observation timestamp

- [var timestamp: Date](/documentation/corelocation/clbeacon/timestamp)
- [CLCondition](/documentation/corelocation/clcondition-swift.protocol)

## Compass headings

- [Getting heading and course information](/documentation/corelocation/getting-heading-and-course-information)
- [CLHeading](/documentation/corelocation/clheading)

### Getting the heading values

- [var magneticHeading: CLLocationDirection](/documentation/corelocation/clheading/magneticheading)
- [var trueHeading: CLLocationDirection](/documentation/corelocation/clheading/trueheading)
- [var headingAccuracy: CLLocationDirection](/documentation/corelocation/clheading/headingaccuracy)

### Getting the raw heading data

- [var x: CLHeadingComponentValue](/documentation/corelocation/clheading/x)
- [var y: CLHeadingComponentValue](/documentation/corelocation/clheading/y)
- [var z: CLHeadingComponentValue](/documentation/corelocation/clheading/z)
- [CLHeadingComponentValue](/documentation/corelocation/clheadingcomponentvalue)

### Getting the event timestamp

- [var timestamp: Date](/documentation/corelocation/clheading/timestamp)

## Geocoding

- [Converting between coordinates and user-friendly place names](/documentation/corelocation/converting-between-coordinates-and-user-friendly-place-names)
- [Converting a user’s location to a descriptive placemark](/documentation/corelocation/converting-a-user-s-location-to-a-descriptive-placemark)
- [CLGeocoder](/documentation/corelocation/clgeocoder)

### Reverse geocoding a location

- [func reverseGeocodeLocation(CLLocation, preferredLocale: Locale?, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/reversegeocodelocation(_:preferredlocale:completionhandler:))
- [func reverseGeocodeLocation(CLLocation, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/reversegeocodelocation(_:completionhandler:))
- [CLGeocodeCompletionHandler](/documentation/corelocation/clgeocodecompletionhandler)

### Geocoding an address

- [func geocodeAddressString(String, in: CLRegion?, preferredLocale: Locale?, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/geocodeaddressstring(_:in:preferredlocale:completionhandler:))
- [func geocodeAddressString(String, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/geocodeaddressstring(_:completionhandler:))
- [func geocodeAddressString(String, in: CLRegion?, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/geocodeaddressstring(_:in:completionhandler:))
- [func geocodePostalAddress(CNPostalAddress, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/geocodepostaladdress(_:completionhandler:))
- [func geocodePostalAddress(CNPostalAddress, preferredLocale: Locale?, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/geocodepostaladdress(_:preferredlocale:completionhandler:))
- [func geocodeAddressDictionary([AnyHashable : Any], completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/geocodeaddressdictionary(_:completionhandler:))

### Managing geocoding requests

- [func cancelGeocode()](/documentation/corelocation/clgeocoder/cancelgeocode())
- [var isGeocoding: Bool](/documentation/corelocation/clgeocoder/isgeocoding)

### Instance Methods

- [func geocodeAddressString(String, inRegionCenteredAt: CLLocationCoordinate2D, inRegionRadius: CLLocationDistance, preferredLocale: Locale?, completionHandler: ([CLPlacemark]?, (any Error)?) -> Void)](/documentation/corelocation/clgeocoder/geocodeaddressstring(_:inregioncenteredat:inregionradius:preferredlocale:completionhandler:))
- [CLPlacemark](/documentation/corelocation/clplacemark)

### Creating a placemark object

- [init(placemark: CLPlacemark)](/documentation/corelocation/clplacemark/init(placemark:))

### Getting the placemark’s location

- [var location: CLLocation?](/documentation/corelocation/clplacemark/location)
- [var region: CLRegion?](/documentation/corelocation/clplacemark/region)

### Getting the placemark name

- [var name: String?](/documentation/corelocation/clplacemark/name)

### Getting the placemark details

- [var thoroughfare: String?](/documentation/corelocation/clplacemark/thoroughfare)
- [var subThoroughfare: String?](/documentation/corelocation/clplacemark/subthoroughfare)
- [var locality: String?](/documentation/corelocation/clplacemark/locality)
- [var subLocality: String?](/documentation/corelocation/clplacemark/sublocality)
- [var administrativeArea: String?](/documentation/corelocation/clplacemark/administrativearea)
- [var subAdministrativeArea: String?](/documentation/corelocation/clplacemark/subadministrativearea)
- [var postalCode: String?](/documentation/corelocation/clplacemark/postalcode)

### Getting the placemark’s country

- [var isoCountryCode: String?](/documentation/corelocation/clplacemark/isocountrycode)
- [var country: String?](/documentation/corelocation/clplacemark/country)

### Getting the associated contact details

- [var postalAddress: CNPostalAddress?](/documentation/corelocation/clplacemark/postaladdress)
- [var addressDictionary: [AnyHashable : Any]?](/documentation/corelocation/clplacemark/addressdictionary)

### Getting landscape information

- [var inlandWater: String?](/documentation/corelocation/clplacemark/inlandwater)
- [var ocean: String?](/documentation/corelocation/clplacemark/ocean)

### Getting points of interest

- [var areasOfInterest: [String]?](/documentation/corelocation/clplacemark/areasofinterest)

### Getting the placemark’s time zone

- [var timeZone: TimeZone?](/documentation/corelocation/clplacemark/timezone)

### Type Aliases

- [CLPlacemark.Specification](/documentation/corelocation/clplacemark/specification)
- [CLPlacemark.UnwrappedType](/documentation/corelocation/clplacemark/unwrappedtype)
- [CLPlacemark.ValueType](/documentation/corelocation/clplacemark/valuetype)

### Type Properties

- [static var defaultResolverSpecification: EmptyResolverSpecification<CLPlacemark>](/documentation/corelocation/clplacemark/defaultresolverspecification)

### Initializers

- [convenience init(location: CLLocation, name: String?, postalAddress: CNPostalAddress?)](/documentation/corelocation/clplacemark/init(location:name:postaladdress:))

## Location push service extension

- [Location Push Service Extension](/documentation/bundleresources/entitlements/com.apple.developer.location.push)
- [CLLocationPushServiceExtension](/documentation/corelocation/cllocationpushserviceextension)

### Getting the push notification payload

- [func didReceiveLocationPushPayload([String : Any], completion: () -> Void)](/documentation/corelocation/cllocationpushserviceextension/didreceivelocationpushpayload(_:completion:))

### Handling the extension termination

- [func serviceExtensionWillTerminate()](/documentation/corelocation/cllocationpushserviceextension/serviceextensionwillterminate())
- [CLLocationPushServiceError](/documentation/corelocation/cllocationpushserviceerror-swift.struct)

### Getting the error code

- [static var unknown: CLLocationPushServiceError.Code](/documentation/corelocation/cllocationpushserviceerror-swift.struct/unknown)
- [static var missingPushExtension: CLLocationPushServiceError.Code](/documentation/corelocation/cllocationpushserviceerror-swift.struct/missingpushextension)
- [static var missingPushServerEnvironment: CLLocationPushServiceError.Code](/documentation/corelocation/cllocationpushserviceerror-swift.struct/missingpushserverenvironment)
- [static var missingEntitlement: CLLocationPushServiceError.Code](/documentation/corelocation/cllocationpushserviceerror-swift.struct/missingentitlement)
- [static var unsupportedPlatform: CLLocationPushServiceError.Code](/documentation/corelocation/cllocationpushserviceerror-swift.struct/unsupportedplatform)
- [CLLocationPushServiceError.Code](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code)

#### Getting the error code

- [case unknown](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/unknown)
- [case missingPushExtension](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/missingpushextension)
- [case missingPushServerEnvironment](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/missingpushserverenvironment)
- [case missingEntitlement](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/missingentitlement)
- [case unsupportedPlatform](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/unsupportedplatform)

#### Initializers

- [init?(rawValue: Int)](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/corelocation/cllocationpushserviceerror-swift.struct/errordomain)
- [let CLLocationPushServiceErrorDomain: String](/documentation/corelocation/cllocationpushserviceerrordomain)
- [CLLocationPushServiceError.Code](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code)

### Getting the error code

- [case unknown](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/unknown)
- [case missingPushExtension](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/missingpushextension)
- [case missingPushServerEnvironment](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/missingpushserverenvironment)
- [case missingEntitlement](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/missingentitlement)
- [case unsupportedPlatform](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/unsupportedplatform)

### Initializers

- [init?(rawValue: Int)](/documentation/corelocation/cllocationpushserviceerror-swift.struct/code/init(rawvalue:))

## Errors

- [CLError](/documentation/corelocation/clerror-swift.struct)

### Getting general errors

- [static var locationUnknown: CLError.Code](/documentation/corelocation/clerror-swift.struct/locationunknown)
- [static var denied: CLError.Code](/documentation/corelocation/clerror-swift.struct/denied)
- [static var promptDeclined: CLError.Code](/documentation/corelocation/clerror-swift.struct/promptdeclined)
- [static var network: CLError.Code](/documentation/corelocation/clerror-swift.struct/network)
- [static var headingFailure: CLError.Code](/documentation/corelocation/clerror-swift.struct/headingfailure)
- [static var rangingUnavailable: CLError.Code](/documentation/corelocation/clerror-swift.struct/rangingunavailable)
- [static var rangingFailure: CLError.Code](/documentation/corelocation/clerror-swift.struct/rangingfailure)
- [CLError.Code](/documentation/corelocation/clerror-swift.struct/code)

#### Getting general errors

- [case locationUnknown](/documentation/corelocation/clerror-swift.struct/code/locationunknown)
- [case denied](/documentation/corelocation/clerror-swift.struct/code/denied)
- [case promptDeclined](/documentation/corelocation/clerror-swift.struct/code/promptdeclined)
- [case network](/documentation/corelocation/clerror-swift.struct/code/network)
- [case headingFailure](/documentation/corelocation/clerror-swift.struct/code/headingfailure)
- [case rangingUnavailable](/documentation/corelocation/clerror-swift.struct/code/rangingunavailable)
- [case rangingFailure](/documentation/corelocation/clerror-swift.struct/code/rangingfailure)

#### Getting region monitoring errors

- [case regionMonitoringDenied](/documentation/corelocation/clerror-swift.struct/code/regionmonitoringdenied)
- [case regionMonitoringFailure](/documentation/corelocation/clerror-swift.struct/code/regionmonitoringfailure)
- [case regionMonitoringSetupDelayed](/documentation/corelocation/clerror-swift.struct/code/regionmonitoringsetupdelayed)
- [case regionMonitoringResponseDelayed](/documentation/corelocation/clerror-swift.struct/code/regionmonitoringresponsedelayed)

#### Getting geocoding errors

- [case geocodeCanceled](/documentation/corelocation/clerror-swift.struct/code/geocodecanceled)
- [case geocodeFoundNoResult](/documentation/corelocation/clerror-swift.struct/code/geocodefoundnoresult)
- [case geocodeFoundPartialResult](/documentation/corelocation/clerror-swift.struct/code/geocodefoundpartialresult)

#### Getting deferred location update errors

- [case deferredFailed](/documentation/corelocation/clerror-swift.struct/code/deferredfailed)
- [case deferredCanceled](/documentation/corelocation/clerror-swift.struct/code/deferredcanceled)
- [case deferredAccuracyTooLow](/documentation/corelocation/clerror-swift.struct/code/deferredaccuracytoolow)
- [case deferredDistanceFiltered](/documentation/corelocation/clerror-swift.struct/code/deferreddistancefiltered)
- [case deferredNotUpdatingLocation](/documentation/corelocation/clerror-swift.struct/code/deferrednotupdatinglocation)

#### Enumeration cases

- [case historicalLocationError](/documentation/corelocation/clerror-swift.struct/code/historicallocationerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/corelocation/clerror-swift.struct/code/init(rawvalue:))

### Getting region monitoring errors

- [static var regionMonitoringDenied: CLError.Code](/documentation/corelocation/clerror-swift.struct/regionmonitoringdenied)
- [static var regionMonitoringFailure: CLError.Code](/documentation/corelocation/clerror-swift.struct/regionmonitoringfailure)
- [static var regionMonitoringSetupDelayed: CLError.Code](/documentation/corelocation/clerror-swift.struct/regionmonitoringsetupdelayed)
- [static var regionMonitoringResponseDelayed: CLError.Code](/documentation/corelocation/clerror-swift.struct/regionmonitoringresponsedelayed)

### Getting geocoding errors

- [static var geocodeCanceled: CLError.Code](/documentation/corelocation/clerror-swift.struct/geocodecanceled)
- [static var geocodeFoundNoResult: CLError.Code](/documentation/corelocation/clerror-swift.struct/geocodefoundnoresult)
- [static var geocodeFoundPartialResult: CLError.Code](/documentation/corelocation/clerror-swift.struct/geocodefoundpartialresult)

### Getting deferred location update errors

- [static var deferredFailed: CLError.Code](/documentation/corelocation/clerror-swift.struct/deferredfailed)
- [static var deferredCanceled: CLError.Code](/documentation/corelocation/clerror-swift.struct/deferredcanceled)
- [static var deferredAccuracyTooLow: CLError.Code](/documentation/corelocation/clerror-swift.struct/deferredaccuracytoolow)
- [static var deferredDistanceFiltered: CLError.Code](/documentation/corelocation/clerror-swift.struct/deferreddistancefiltered)
- [static var deferredNotUpdatingLocation: CLError.Code](/documentation/corelocation/clerror-swift.struct/deferrednotupdatinglocation)

### Getting the error details

- [var alternateRegion: CLRegion?](/documentation/corelocation/clerror-swift.struct/alternateregion)

### Type Properties

- [static var historicalLocationError: CLError.Code](/documentation/corelocation/clerror-swift.struct/historicallocationerror)
- [static var errorDomain: String](/documentation/corelocation/clerror-swift.struct/errordomain)
- [let kCLErrorDomain: String](/documentation/corelocation/kclerrordomain)
- [let kCLErrorUserInfoAlternateRegionKey: String](/documentation/corelocation/kclerroruserinfoalternateregionkey)

## Deprecated

- [Deprecated](/documentation/corelocation/deprecated)

### Classes

- [CLBeaconRegion](/documentation/corelocation/clbeaconregion)

#### Creating a beacon region

- [init(beaconIdentityConstraint: CLBeaconIdentityConstraint, identifier: String)](/documentation/corelocation/clbeaconregion/init(beaconidentityconstraint:identifier:))
- [init(uuid: UUID, identifier: String)](/documentation/corelocation/clbeaconregion/init(uuid:identifier:))
- [init(uuid: UUID, major: CLBeaconMajorValue, identifier: String)](/documentation/corelocation/clbeaconregion/init(uuid:major:identifier:))
- [init(uuid: UUID, major: CLBeaconMajorValue, minor: CLBeaconMinorValue, identifier: String)](/documentation/corelocation/clbeaconregion/init(uuid:major:minor:identifier:))
- [CLBeaconMajorValue](/documentation/corelocation/clbeaconmajorvalue)
- [CLBeaconMinorValue](/documentation/corelocation/clbeaconminorvalue)

#### Getting the beacon identity

- [var uuid: UUID](/documentation/corelocation/clbeaconregion/uuid)
- [var major: NSNumber?](/documentation/corelocation/clbeaconregion/major)
- [var minor: NSNumber?](/documentation/corelocation/clbeaconregion/minor)
- [var beaconIdentityConstraint: CLBeaconIdentityConstraint](/documentation/corelocation/clbeaconregion/beaconidentityconstraint)

#### Specifying when to send notifications

- [var notifyEntryStateOnDisplay: Bool](/documentation/corelocation/clbeaconregion/notifyentrystateondisplay)

#### Getting the beacon’s advertisement data

- [func peripheralData(withMeasuredPower: NSNumber?) -> NSMutableDictionary](/documentation/corelocation/clbeaconregion/peripheraldata(withmeasuredpower:))

#### Deprecated

- [init(proximityUUID: UUID, identifier: String)](/documentation/corelocation/clbeaconregion/init(proximityuuid:identifier:))
- [init(proximityUUID: UUID, major: CLBeaconMajorValue, identifier: String)](/documentation/corelocation/clbeaconregion/init(proximityuuid:major:identifier:))
- [init(proximityUUID: UUID, major: CLBeaconMajorValue, minor: CLBeaconMinorValue, identifier: String)](/documentation/corelocation/clbeaconregion/init(proximityuuid:major:minor:identifier:))
- [var proximityUUID: UUID](/documentation/corelocation/clbeaconregion/proximityuuid)
- [CLBeaconIdentityConstraint](/documentation/corelocation/clbeaconidentityconstraint)

#### Getting the beacon identity

- [var major: UInt16?](/documentation/corelocation/clbeaconidentityconstraint/major)
- [var minor: UInt16?](/documentation/corelocation/clbeaconidentityconstraint/minor)
- [CLCircularRegion](/documentation/corelocation/clcircularregion)

#### Creating a circular region

- [init(center: CLLocationCoordinate2D, radius: CLLocationDistance, identifier: String)](/documentation/corelocation/clcircularregion/init(center:radius:identifier:))

#### Getting the circle’s center and radius

- [var center: CLLocationCoordinate2D](/documentation/corelocation/clcircularregion/center)
- [var radius: CLLocationDistance](/documentation/corelocation/clcircularregion/radius)

#### Performing hit testing in the region

- [func contains(CLLocationCoordinate2D) -> Bool](/documentation/corelocation/clcircularregion/contains(_:))

## Reference

- [Core Location Constants](/documentation/corelocation/core-location-constants)

### Constants

- [var CL_TARGET_SUPPORTS_CONDITIONS: Int32](/documentation/corelocation/cl_target_supports_conditions)
- [Core Location Functions](/documentation/corelocation/core-location-functions)

### Functions

- [func CLLocationCoordinate2DMake(CLLocationDegrees, CLLocationDegrees) -> CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2dmake(_:_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
