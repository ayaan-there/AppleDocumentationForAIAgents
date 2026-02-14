# Core Motion Documentation

Source: https://sosumi.ai/documentation/coremotion

---
title: Core Motion
source: https://developer.apple.com/documentation/coremotion
timestamp: 2026-02-13T18:55:33.995Z
---

## Essentials

- [Core Motion updates](/documentation/updates/coremotion)
- [CMMotionManager](/documentation/coremotion/cmmotionmanager)

### Determining the Availability of Services

- [var isDeviceMotionAvailable: Bool](/documentation/coremotion/cmmotionmanager/isdevicemotionavailable)
- [var isAccelerometerAvailable: Bool](/documentation/coremotion/cmmotionmanager/isaccelerometeravailable)
- [var isGyroAvailable: Bool](/documentation/coremotion/cmmotionmanager/isgyroavailable)
- [var isMagnetometerAvailable: Bool](/documentation/coremotion/cmmotionmanager/ismagnetometeravailable)

### Determining Which Services Are Active

- [var isDeviceMotionActive: Bool](/documentation/coremotion/cmmotionmanager/isdevicemotionactive)
- [var isAccelerometerActive: Bool](/documentation/coremotion/cmmotionmanager/isaccelerometeractive)
- [var isGyroActive: Bool](/documentation/coremotion/cmmotionmanager/isgyroactive)
- [var isMagnetometerActive: Bool](/documentation/coremotion/cmmotionmanager/ismagnetometeractive)

### Managing Device Motion Updates

- [var showsDeviceMovementDisplay: Bool](/documentation/coremotion/cmmotionmanager/showsdevicemovementdisplay)
- [var deviceMotionUpdateInterval: TimeInterval](/documentation/coremotion/cmmotionmanager/devicemotionupdateinterval)
- [func startDeviceMotionUpdates(using: CMAttitudeReferenceFrame, to: OperationQueue, withHandler: CMDeviceMotionHandler)](/documentation/coremotion/cmmotionmanager/startdevicemotionupdates(using:to:withhandler:))
- [func startDeviceMotionUpdates(to: OperationQueue, withHandler: CMDeviceMotionHandler)](/documentation/coremotion/cmmotionmanager/startdevicemotionupdates(to:withhandler:))
- [func startDeviceMotionUpdates(using: CMAttitudeReferenceFrame)](/documentation/coremotion/cmmotionmanager/startdevicemotionupdates(using:))
- [func startDeviceMotionUpdates()](/documentation/coremotion/cmmotionmanager/startdevicemotionupdates())
- [func stopDeviceMotionUpdates()](/documentation/coremotion/cmmotionmanager/stopdevicemotionupdates())
- [var deviceMotion: CMDeviceMotion?](/documentation/coremotion/cmmotionmanager/devicemotion)
- [CMDeviceMotionHandler](/documentation/coremotion/cmdevicemotionhandler)

### Managing Accelerometer Updates

- [var accelerometerUpdateInterval: TimeInterval](/documentation/coremotion/cmmotionmanager/accelerometerupdateinterval)
- [func startAccelerometerUpdates(to: OperationQueue, withHandler: CMAccelerometerHandler)](/documentation/coremotion/cmmotionmanager/startaccelerometerupdates(to:withhandler:))
- [func startAccelerometerUpdates()](/documentation/coremotion/cmmotionmanager/startaccelerometerupdates())
- [func stopAccelerometerUpdates()](/documentation/coremotion/cmmotionmanager/stopaccelerometerupdates())
- [var accelerometerData: CMAccelerometerData?](/documentation/coremotion/cmmotionmanager/accelerometerdata)
- [CMAccelerometerHandler](/documentation/coremotion/cmaccelerometerhandler)

### Managing Gyroscope Updates

- [var gyroUpdateInterval: TimeInterval](/documentation/coremotion/cmmotionmanager/gyroupdateinterval)
- [func startGyroUpdates(to: OperationQueue, withHandler: CMGyroHandler)](/documentation/coremotion/cmmotionmanager/startgyroupdates(to:withhandler:))
- [func startGyroUpdates()](/documentation/coremotion/cmmotionmanager/startgyroupdates())
- [func stopGyroUpdates()](/documentation/coremotion/cmmotionmanager/stopgyroupdates())
- [var gyroData: CMGyroData?](/documentation/coremotion/cmmotionmanager/gyrodata)
- [CMGyroHandler](/documentation/coremotion/cmgyrohandler)

### Managing Magnetometer Updates

- [var magnetometerUpdateInterval: TimeInterval](/documentation/coremotion/cmmotionmanager/magnetometerupdateinterval)
- [func startMagnetometerUpdates(to: OperationQueue, withHandler: CMMagnetometerHandler)](/documentation/coremotion/cmmotionmanager/startmagnetometerupdates(to:withhandler:))
- [func startMagnetometerUpdates()](/documentation/coremotion/cmmotionmanager/startmagnetometerupdates())
- [func stopMagnetometerUpdates()](/documentation/coremotion/cmmotionmanager/stopmagnetometerupdates())
- [var magnetometerData: CMMagnetometerData?](/documentation/coremotion/cmmotionmanager/magnetometerdata)
- [CMMagnetometerHandler](/documentation/coremotion/cmmagnetometerhandler)

### Accessing Attitude Reference Frames

- [var attitudeReferenceFrame: CMAttitudeReferenceFrame](/documentation/coremotion/cmmotionmanager/attitudereferenceframe)
- [class func availableAttitudeReferenceFrames() -> CMAttitudeReferenceFrame](/documentation/coremotion/cmmotionmanager/availableattitudereferenceframes())

### Understanding Errors

- [let CMErrorDomain: String](/documentation/coremotion/cmerrordomain)
- [CMError](/documentation/coremotion/cmerror)

#### Errors

- [var CMErrorDeviceRequiresMovement: CMError](/documentation/coremotion/cmerrordevicerequiresmovement)
- [var CMErrorInvalidAction: CMError](/documentation/coremotion/cmerrorinvalidaction)
- [var CMErrorInvalidParameter: CMError](/documentation/coremotion/cmerrorinvalidparameter)
- [var CMErrorMotionActivityNotAuthorized: CMError](/documentation/coremotion/cmerrormotionactivitynotauthorized)
- [var CMErrorMotionActivityNotAvailable: CMError](/documentation/coremotion/cmerrormotionactivitynotavailable)
- [var CMErrorMotionActivityNotEntitled: CMError](/documentation/coremotion/cmerrormotionactivitynotentitled)
- [var CMErrorNilData: CMError](/documentation/coremotion/cmerrornildata)
- [var CMErrorNULL: CMError](/documentation/coremotion/cmerrornull)
- [var CMErrorNotAuthorized: CMError](/documentation/coremotion/cmerrornotauthorized)
- [var CMErrorNotAvailable: CMError](/documentation/coremotion/cmerrornotavailable)
- [var CMErrorNotEntitled: CMError](/documentation/coremotion/cmerrornotentitled)
- [var CMErrorSize: CMError](/documentation/coremotion/cmerrorsize)
- [var CMErrorTrueNorthNotAvailable: CMError](/documentation/coremotion/cmerrortruenorthnotavailable)
- [var CMErrorUnknown: CMError](/documentation/coremotion/cmerrorunknown)

#### Initializers

- [init(UInt32)](/documentation/coremotion/cmerror/init(_:))
- [init(rawValue: UInt32)](/documentation/coremotion/cmerror/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/coremotion/cmerror/rawvalue)

## Device motion

- [Getting processed device-motion data](/documentation/coremotion/getting-processed-device-motion-data)
- [CMDeviceMotion](/documentation/coremotion/cmdevicemotion)

### Getting Attitude and Rotation Rate

- [var attitude: CMAttitude](/documentation/coremotion/cmdevicemotion/attitude)
- [var rotationRate: CMRotationRate](/documentation/coremotion/cmdevicemotion/rotationrate)

### Getting Acceleration Data

- [var gravity: CMAcceleration](/documentation/coremotion/cmdevicemotion/gravity)
- [var userAcceleration: CMAcceleration](/documentation/coremotion/cmdevicemotion/useracceleration)

### Getting the Calibrated Magnetic Field

- [var magneticField: CMCalibratedMagneticField](/documentation/coremotion/cmdevicemotion/magneticfield)
- [CMCalibratedMagneticField](/documentation/coremotion/cmcalibratedmagneticfield)

#### Initializers

- [init()](/documentation/coremotion/cmcalibratedmagneticfield/init())
- [init(field: CMMagneticField, accuracy: CMMagneticFieldCalibrationAccuracy)](/documentation/coremotion/cmcalibratedmagneticfield/init(field:accuracy:))

#### Accessing the Field Values

- [var field: CMMagneticField](/documentation/coremotion/cmcalibratedmagneticfield/field)
- [var accuracy: CMMagneticFieldCalibrationAccuracy](/documentation/coremotion/cmcalibratedmagneticfield/accuracy)
- [CMMagneticFieldCalibrationAccuracy](/documentation/coremotion/cmmagneticfieldcalibrationaccuracy)

#### Constants

- [case uncalibrated](/documentation/coremotion/cmmagneticfieldcalibrationaccuracy/uncalibrated)
- [case low](/documentation/coremotion/cmmagneticfieldcalibrationaccuracy/low)
- [case medium](/documentation/coremotion/cmmagneticfieldcalibrationaccuracy/medium)
- [case high](/documentation/coremotion/cmmagneticfieldcalibrationaccuracy/high)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coremotion/cmmagneticfieldcalibrationaccuracy/init(rawvalue:))

### Getting the Heading

- [var heading: Double](/documentation/coremotion/cmdevicemotion/heading)

### Getting the Sensor Location

- [var sensorLocation: CMDeviceMotion.SensorLocation](/documentation/coremotion/cmdevicemotion/sensorlocation-swift.property)
- [CMDeviceMotion.SensorLocation](/documentation/coremotion/cmdevicemotion/sensorlocation-swift.enum)

#### Sensor Locations

- [case `default`](/documentation/coremotion/cmdevicemotion/sensorlocation-swift.enum/default)
- [case headphoneLeft](/documentation/coremotion/cmdevicemotion/sensorlocation-swift.enum/headphoneleft)
- [case headphoneRight](/documentation/coremotion/cmdevicemotion/sensorlocation-swift.enum/headphoneright)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmdevicemotion/sensorlocation-swift.enum/init(rawvalue:))
- [CMAttitude](/documentation/coremotion/cmattitude)

### Getting a Mathematical Representation of Attitude as Euler Angles

- [var roll: Double](/documentation/coremotion/cmattitude/roll)
- [var pitch: Double](/documentation/coremotion/cmattitude/pitch)
- [var yaw: Double](/documentation/coremotion/cmattitude/yaw)

### Getting a Mathematical Representation of Attitude as a Rotation Matrix

- [var rotationMatrix: CMRotationMatrix](/documentation/coremotion/cmattitude/rotationmatrix)
- [CMRotationMatrix](/documentation/coremotion/cmrotationmatrix)

#### Fields

- [var m11: Double](/documentation/coremotion/cmrotationmatrix/m11)
- [var m12: Double](/documentation/coremotion/cmrotationmatrix/m12)
- [var m13: Double](/documentation/coremotion/cmrotationmatrix/m13)
- [var m21: Double](/documentation/coremotion/cmrotationmatrix/m21)
- [var m22: Double](/documentation/coremotion/cmrotationmatrix/m22)
- [var m23: Double](/documentation/coremotion/cmrotationmatrix/m23)
- [var m31: Double](/documentation/coremotion/cmrotationmatrix/m31)
- [var m32: Double](/documentation/coremotion/cmrotationmatrix/m32)
- [var m33: Double](/documentation/coremotion/cmrotationmatrix/m33)

#### Initializers

- [init()](/documentation/coremotion/cmrotationmatrix/init())
- [init(m11: Double, m12: Double, m13: Double, m21: Double, m22: Double, m23: Double, m31: Double, m32: Double, m33: Double)](/documentation/coremotion/cmrotationmatrix/init(m11:m12:m13:m21:m22:m23:m31:m32:m33:))

### Getting a Mathematical Representation of Attitude as a Quaternion

- [var quaternion: CMQuaternion](/documentation/coremotion/cmattitude/quaternion)
- [CMQuaternion](/documentation/coremotion/cmquaternion)

#### Initializing the Quaternion

- [init()](/documentation/coremotion/cmquaternion/init())
- [init(x: Double, y: Double, z: Double, w: Double)](/documentation/coremotion/cmquaternion/init(x:y:z:w:))

#### Getting the Quaternion Values

- [var w: Double](/documentation/coremotion/cmquaternion/w)
- [var x: Double](/documentation/coremotion/cmquaternion/x)
- [var y: Double](/documentation/coremotion/cmquaternion/y)
- [var z: Double](/documentation/coremotion/cmquaternion/z)

### Obtaining the Change in Attitude

- [func multiply(byInverseOf: CMAttitude)](/documentation/coremotion/cmattitude/multiply(byinverseof:))
- [CMAttitudeReferenceFrame](/documentation/coremotion/cmattitudereferenceframe)

### Getting the reference frames

- [static var xArbitraryZVertical: CMAttitudeReferenceFrame](/documentation/coremotion/cmattitudereferenceframe/xarbitraryzvertical)
- [static var xArbitraryCorrectedZVertical: CMAttitudeReferenceFrame](/documentation/coremotion/cmattitudereferenceframe/xarbitrarycorrectedzvertical)
- [static var xMagneticNorthZVertical: CMAttitudeReferenceFrame](/documentation/coremotion/cmattitudereferenceframe/xmagneticnorthzvertical)
- [static var xTrueNorthZVertical: CMAttitudeReferenceFrame](/documentation/coremotion/cmattitudereferenceframe/xtruenorthzvertical)

### Initializers

- [init(rawValue: UInt)](/documentation/coremotion/cmattitudereferenceframe/init(rawvalue:))
- [CMHeadphoneMotionManager](/documentation/coremotion/cmheadphonemotionmanager)

### Checking Availability

- [var isDeviceMotionAvailable: Bool](/documentation/coremotion/cmheadphonemotionmanager/isdevicemotionavailable)
- [var isDeviceMotionActive: Bool](/documentation/coremotion/cmheadphonemotionmanager/isdevicemotionactive)
- [var isConnectionStatusActive: Bool](/documentation/coremotion/cmheadphonemotionmanager/isconnectionstatusactive)
- [class func authorizationStatus() -> CMAuthorizationStatus](/documentation/coremotion/cmheadphonemotionmanager/authorizationstatus())

### Starting and Stopping Updates

- [func startDeviceMotionUpdates()](/documentation/coremotion/cmheadphonemotionmanager/startdevicemotionupdates())
- [func startDeviceMotionUpdates(to: OperationQueue, withHandler: CMHeadphoneMotionManager.DeviceMotionHandler)](/documentation/coremotion/cmheadphonemotionmanager/startdevicemotionupdates(to:withhandler:))
- [func startConnectionStatusUpdates()](/documentation/coremotion/cmheadphonemotionmanager/startconnectionstatusupdates())
- [func stopDeviceMotionUpdates()](/documentation/coremotion/cmheadphonemotionmanager/stopdevicemotionupdates())
- [func stopConnectionStatusUpdates()](/documentation/coremotion/cmheadphonemotionmanager/stopconnectionstatusupdates())

### Getting the Delegate

- [var delegate: (any CMHeadphoneMotionManagerDelegate)?](/documentation/coremotion/cmheadphonemotionmanager/delegate)
- [CMHeadphoneMotionManagerDelegate](/documentation/coremotion/cmheadphonemotionmanagerdelegate)

#### Connecting and Disconnecting Headphones

- [func headphoneMotionManagerDidConnect(CMHeadphoneMotionManager)](/documentation/coremotion/cmheadphonemotionmanagerdelegate/headphonemotionmanagerdidconnect(_:))
- [func headphoneMotionManagerDidDisconnect(CMHeadphoneMotionManager)](/documentation/coremotion/cmheadphonemotionmanagerdelegate/headphonemotionmanagerdiddisconnect(_:))
- [CMHeadphoneMotionManager.DeviceMotionHandler](/documentation/coremotion/cmheadphonemotionmanager/devicemotionhandler)

### Getting Device-Motion Information

- [var deviceMotion: CMDeviceMotion?](/documentation/coremotion/cmheadphonemotionmanager/devicemotion)

## Accelerometers

- [Getting raw accelerometer events](/documentation/coremotion/getting-raw-accelerometer-events)
- [CMAccelerometerData](/documentation/coremotion/cmaccelerometerdata)

### Accessing Accelerometer Data

- [var acceleration: CMAcceleration](/documentation/coremotion/cmaccelerometerdata/acceleration)
- [CMAcceleration](/documentation/coremotion/cmacceleration)

#### Initializers

- [init()](/documentation/coremotion/cmacceleration/init())
- [init(x: Double, y: Double, z: Double)](/documentation/coremotion/cmacceleration/init(x:y:z:))

#### Getting the Acceleration Values

- [var x: Double](/documentation/coremotion/cmacceleration/x)
- [var y: Double](/documentation/coremotion/cmacceleration/y)
- [var z: Double](/documentation/coremotion/cmacceleration/z)
- [CMRecordedAccelerometerData](/documentation/coremotion/cmrecordedaccelerometerdata)

### Getting the Accelerometer Data

- [var startDate: Date](/documentation/coremotion/cmrecordedaccelerometerdata/startdate)
- [var identifier: UInt64](/documentation/coremotion/cmrecordedaccelerometerdata/identifier)
- [CMSensorRecorder](/documentation/coremotion/cmsensorrecorder)

### Checking the Availability of Sensor Recording

- [class func isAccelerometerRecordingAvailable() -> Bool](/documentation/coremotion/cmsensorrecorder/isaccelerometerrecordingavailable())
- [class func authorizationStatus() -> CMAuthorizationStatus](/documentation/coremotion/cmsensorrecorder/authorizationstatus())
- [CMAuthorizationStatus](/documentation/coremotion/cmauthorizationstatus)

#### Enumeration Cases

- [case notDetermined](/documentation/coremotion/cmauthorizationstatus/notdetermined)
- [case restricted](/documentation/coremotion/cmauthorizationstatus/restricted)
- [case denied](/documentation/coremotion/cmauthorizationstatus/denied)
- [case authorized](/documentation/coremotion/cmauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmauthorizationstatus/init(rawvalue:))
- [class func isAuthorizedForRecording() -> Bool](/documentation/coremotion/cmsensorrecorder/isauthorizedforrecording())

### Recording Accelerometer Data

- [func recordAccelerometer(forDuration: TimeInterval)](/documentation/coremotion/cmsensorrecorder/recordaccelerometer(forduration:))

### Retrieving Past Accelerometer Data

- [func accelerometerData(from: Date, to: Date) -> CMSensorDataList?](/documentation/coremotion/cmsensorrecorder/accelerometerdata(from:to:))
- [CMSensorDataList](/documentation/coremotion/cmsensordatalist)

## Gyroscopes

- [Getting raw gyroscope events](/documentation/coremotion/getting-raw-gyroscope-events)
- [CMGyroData](/documentation/coremotion/cmgyrodata)

### Getting the Rotation Rate

- [var rotationRate: CMRotationRate](/documentation/coremotion/cmgyrodata/rotationrate)
- [CMRotationRate](/documentation/coremotion/cmrotationrate)

#### Getting the Rotation Rates

- [var x: Double](/documentation/coremotion/cmrotationrate/x)
- [var y: Double](/documentation/coremotion/cmrotationrate/y)
- [var z: Double](/documentation/coremotion/cmrotationrate/z)

#### Initializers

- [init()](/documentation/coremotion/cmrotationrate/init())
- [init(x: Double, y: Double, z: Double)](/documentation/coremotion/cmrotationrate/init(x:y:z:))
- [CMRotationRateData](/documentation/coremotion/cmrotationratedata)

#### Accessing Rotation Data

- [var rotationRate: CMRotationRate](/documentation/coremotion/cmrotationratedata/rotationrate)
- [CMRecordedRotationRateData](/documentation/coremotion/cmrecordedrotationratedata)

#### Accessing Rotation Data

- [var startDate: Date](/documentation/coremotion/cmrecordedrotationratedata/startdate)

## Magnetometer

- [CMMagnetometerData](/documentation/coremotion/cmmagnetometerdata)

### Getting the Field Strength

- [var magneticField: CMMagneticField](/documentation/coremotion/cmmagnetometerdata/magneticfield)
- [CMMagneticField](/documentation/coremotion/cmmagneticfield)

#### Getting the Field Values

- [var x: Double](/documentation/coremotion/cmmagneticfield/x)
- [var y: Double](/documentation/coremotion/cmmagneticfield/y)
- [var z: Double](/documentation/coremotion/cmmagneticfield/z)

#### Initializers

- [init()](/documentation/coremotion/cmmagneticfield/init())
- [init(x: Double, y: Double, z: Double)](/documentation/coremotion/cmmagneticfield/init(x:y:z:))

## Altitude data

- [CMAltimeter](/documentation/coremotion/cmaltimeter)

### Determining Altitude Availability

- [class func isAbsoluteAltitudeAvailable() -> Bool](/documentation/coremotion/cmaltimeter/isabsolutealtitudeavailable())
- [class func isRelativeAltitudeAvailable() -> Bool](/documentation/coremotion/cmaltimeter/isrelativealtitudeavailable())
- [class func authorizationStatus() -> CMAuthorizationStatus](/documentation/coremotion/cmaltimeter/authorizationstatus())
- [CMAuthorizationStatus](/documentation/coremotion/cmauthorizationstatus)

#### Enumeration Cases

- [case notDetermined](/documentation/coremotion/cmauthorizationstatus/notdetermined)
- [case restricted](/documentation/coremotion/cmauthorizationstatus/restricted)
- [case denied](/documentation/coremotion/cmauthorizationstatus/denied)
- [case authorized](/documentation/coremotion/cmauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmauthorizationstatus/init(rawvalue:))

### Starting and Stopping Altitude Updates

- [func startAbsoluteAltitudeUpdates(to: OperationQueue, withHandler: CMAbsoluteAltitudeHandler)](/documentation/coremotion/cmaltimeter/startabsolutealtitudeupdates(to:withhandler:))
- [func stopAbsoluteAltitudeUpdates()](/documentation/coremotion/cmaltimeter/stopabsolutealtitudeupdates())
- [CMAbsoluteAltitudeHandler](/documentation/coremotion/cmabsolutealtitudehandler)
- [func startRelativeAltitudeUpdates(to: OperationQueue, withHandler: CMAltitudeHandler)](/documentation/coremotion/cmaltimeter/startrelativealtitudeupdates(to:withhandler:))
- [func stopRelativeAltitudeUpdates()](/documentation/coremotion/cmaltimeter/stoprelativealtitudeupdates())
- [CMAltitudeHandler](/documentation/coremotion/cmaltitudehandler)
- [CMAbsoluteAltitudeData](/documentation/coremotion/cmabsolutealtitudedata)

### Accessing Altitude Data

- [var altitude: Double](/documentation/coremotion/cmabsolutealtitudedata/altitude)
- [var accuracy: Double](/documentation/coremotion/cmabsolutealtitudedata/accuracy)
- [var precision: Double](/documentation/coremotion/cmabsolutealtitudedata/precision)
- [CMAltitudeData](/documentation/coremotion/cmaltitudedata)

### Getting the Altitude Data

- [var relativeAltitude: NSNumber](/documentation/coremotion/cmaltitudedata/relativealtitude)
- [var pressure: NSNumber](/documentation/coremotion/cmaltitudedata/pressure)

## Ambient pressure

- [CMRecordedPressureData](/documentation/coremotion/cmrecordedpressuredata)

### Instance Properties

- [var identifier: UInt64](/documentation/coremotion/cmrecordedpressuredata/identifier)
- [var startDate: Date](/documentation/coremotion/cmrecordedpressuredata/startdate)
- [CMAmbientPressureData](/documentation/coremotion/cmambientpressuredata)

### Accessing the data

- [var pressure: Measurement<UnitPressure>](/documentation/coremotion/cmambientpressuredata/pressure)
- [var temperature: Measurement<UnitTemperature>](/documentation/coremotion/cmambientpressuredata/temperature)

## Water submersion

- [Accessing submersion data](/documentation/coremotion/accessing-submersion-data)
- [CMWaterSubmersionManager](/documentation/coremotion/cmwatersubmersionmanager)

### Setting the delegate

- [var delegate: (any CMWaterSubmersionManagerDelegate)?](/documentation/coremotion/cmwatersubmersionmanager/delegate)

### Checking availability and authorization

- [class var waterSubmersionAvailable: Bool](/documentation/coremotion/cmwatersubmersionmanager/watersubmersionavailable)
- [class var authorizationStatus: CMAuthorizationStatus](/documentation/coremotion/cmwatersubmersionmanager/authorizationstatus)

### Accessing the maximum depth

- [var maximumDepth: Measurement<UnitLength>?](/documentation/coremotion/cmwatersubmersionmanager/maximumdepth)
- [CMWaterSubmersionManagerDelegate](/documentation/coremotion/cmwatersubmersionmanagerdelegate)

### Receiving updates

- [func manager(CMWaterSubmersionManager, didUpdate: CMWaterSubmersionEvent)](/documentation/coremotion/cmwatersubmersionmanagerdelegate/manager(_:didupdate:)-6qux6)
- [func manager(CMWaterSubmersionManager, didUpdate: CMWaterSubmersionMeasurement)](/documentation/coremotion/cmwatersubmersionmanagerdelegate/manager(_:didupdate:)-7nhjb)
- [func manager(CMWaterSubmersionManager, didUpdate: CMWaterTemperature)](/documentation/coremotion/cmwatersubmersionmanagerdelegate/manager(_:didupdate:)-18wua)
- [func manager(CMWaterSubmersionManager, errorOccurred: any Error)](/documentation/coremotion/cmwatersubmersionmanagerdelegate/manager(_:erroroccurred:))
- [CMWaterSubmersionEvent](/documentation/coremotion/cmwatersubmersionevent)

### Accessing event data

- [var date: Date](/documentation/coremotion/cmwatersubmersionevent/date)
- [var state: CMWaterSubmersionEvent.State](/documentation/coremotion/cmwatersubmersionevent/state-swift.property)
- [CMWaterSubmersionEvent.State](/documentation/coremotion/cmwatersubmersionevent/state-swift.enum)

#### Submersion states

- [case notSubmerged](/documentation/coremotion/cmwatersubmersionevent/state-swift.enum/notsubmerged)
- [case submerged](/documentation/coremotion/cmwatersubmersionevent/state-swift.enum/submerged)
- [case unknown](/documentation/coremotion/cmwatersubmersionevent/state-swift.enum/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmwatersubmersionevent/state-swift.enum/init(rawvalue:))
- [CMWaterSubmersionMeasurement](/documentation/coremotion/cmwatersubmersionmeasurement)

### Accessing the data

- [var date: Date](/documentation/coremotion/cmwatersubmersionmeasurement/date)
- [var depth: Measurement<UnitLength>?](/documentation/coremotion/cmwatersubmersionmeasurement/depth)
- [var pressure: Measurement<UnitPressure>?](/documentation/coremotion/cmwatersubmersionmeasurement/pressure)
- [var surfacePressure: Measurement<UnitPressure>](/documentation/coremotion/cmwatersubmersionmeasurement/surfacepressure)
- [var submersionState: CMWaterSubmersionMeasurement.DepthState](/documentation/coremotion/cmwatersubmersionmeasurement/submersionstate)
- [CMWaterSubmersionMeasurement.DepthState](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate)

#### Depth states

- [case notSubmerged](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/notsubmerged)
- [case submergedShallow](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/submergedshallow)
- [case submergedDeep](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/submergeddeep)
- [case approachingMaxDepth](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/approachingmaxdepth)
- [case pastMaxDepth](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/pastmaxdepth)
- [case sensorDepthError](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/sensordeptherror)
- [case unknown](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmwatersubmersionmeasurement/depthstate/init(rawvalue:))
- [CMWaterTemperature](/documentation/coremotion/cmwatertemperature)

### Accessing the data

- [var date: Date](/documentation/coremotion/cmwatertemperature/date)
- [var temperature: Measurement<UnitTemperature>](/documentation/coremotion/cmwatertemperature/temperature)
- [var temperatureUncertainty: Measurement<UnitTemperature>](/documentation/coremotion/cmwatertemperature/temperatureuncertainty)

## Activity

- [CMMotionActivityManager](/documentation/coremotion/cmmotionactivitymanager)

### Determining Activity Availability

- [class func isActivityAvailable() -> Bool](/documentation/coremotion/cmmotionactivitymanager/isactivityavailable())
- [class func authorizationStatus() -> CMAuthorizationStatus](/documentation/coremotion/cmmotionactivitymanager/authorizationstatus())
- [CMAuthorizationStatus](/documentation/coremotion/cmauthorizationstatus)

#### Enumeration Cases

- [case notDetermined](/documentation/coremotion/cmauthorizationstatus/notdetermined)
- [case restricted](/documentation/coremotion/cmauthorizationstatus/restricted)
- [case denied](/documentation/coremotion/cmauthorizationstatus/denied)
- [case authorized](/documentation/coremotion/cmauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmauthorizationstatus/init(rawvalue:))

### Starting and Stopping Activity Updates

- [func startActivityUpdates(to: OperationQueue, withHandler: CMMotionActivityHandler)](/documentation/coremotion/cmmotionactivitymanager/startactivityupdates(to:withhandler:))
- [func stopActivityUpdates()](/documentation/coremotion/cmmotionactivitymanager/stopactivityupdates())
- [CMMotionActivityHandler](/documentation/coremotion/cmmotionactivityhandler)

### Getting Historical Activity Data

- [func queryActivityStarting(from: Date, to: Date, to: OperationQueue, withHandler: CMMotionActivityQueryHandler)](/documentation/coremotion/cmmotionactivitymanager/queryactivitystarting(from:to:to:withhandler:))
- [CMMotionActivityQueryHandler](/documentation/coremotion/cmmotionactivityqueryhandler)
- [CMHeadphoneActivityManager](/documentation/coremotion/cmheadphoneactivitymanager)

### Checking Availability

- [var isActivityAvailable: Bool](/documentation/coremotion/cmheadphoneactivitymanager/isactivityavailable)
- [var isActivityActive: Bool](/documentation/coremotion/cmheadphoneactivitymanager/isactivityactive)
- [var isStatusAvailable: Bool](/documentation/coremotion/cmheadphoneactivitymanager/isstatusavailable)
- [var isStatusActive: Bool](/documentation/coremotion/cmheadphoneactivitymanager/isstatusactive)
- [class func authorizationStatus() -> CMAuthorizationStatus](/documentation/coremotion/cmheadphoneactivitymanager/authorizationstatus())

### Starting and Stopping Updates

- [func startActivityUpdates(to: OperationQueue, withHandler: CMHeadphoneActivityManager.ActivityHandler)](/documentation/coremotion/cmheadphoneactivitymanager/startactivityupdates(to:withhandler:))
- [func stopActivityUpdates()](/documentation/coremotion/cmheadphoneactivitymanager/stopactivityupdates())
- [func startStatusUpdates(to: OperationQueue, withHandler: CMHeadphoneActivityManager.StatusHandler)](/documentation/coremotion/cmheadphoneactivitymanager/startstatusupdates(to:withhandler:))
- [func stopStatusUpdates()](/documentation/coremotion/cmheadphoneactivitymanager/stopstatusupdates())

### Supporting Types

- [CMHeadphoneActivityManager.Status](/documentation/coremotion/cmheadphoneactivitymanager/status)

#### Enumeration Cases

- [case connected](/documentation/coremotion/cmheadphoneactivitymanager/status/connected)
- [case disconnected](/documentation/coremotion/cmheadphoneactivitymanager/status/disconnected)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmheadphoneactivitymanager/status/init(rawvalue:))
- [CMHeadphoneActivityManager.ActivityHandler](/documentation/coremotion/cmheadphoneactivitymanager/activityhandler)
- [CMHeadphoneActivityManager.StatusHandler](/documentation/coremotion/cmheadphoneactivitymanager/statushandler)
- [CMMotionActivity](/documentation/coremotion/cmmotionactivity)

### Getting the Type of Motion

- [var stationary: Bool](/documentation/coremotion/cmmotionactivity/stationary)
- [var walking: Bool](/documentation/coremotion/cmmotionactivity/walking)
- [var running: Bool](/documentation/coremotion/cmmotionactivity/running)
- [var automotive: Bool](/documentation/coremotion/cmmotionactivity/automotive)
- [var cycling: Bool](/documentation/coremotion/cmmotionactivity/cycling)
- [var unknown: Bool](/documentation/coremotion/cmmotionactivity/unknown)

### Getting Metadata for the Motion

- [var startDate: Date](/documentation/coremotion/cmmotionactivity/startdate)
- [var confidence: CMMotionActivityConfidence](/documentation/coremotion/cmmotionactivity/confidence)
- [CMMotionActivityConfidence](/documentation/coremotion/cmmotionactivityconfidence)

#### Constants

- [case low](/documentation/coremotion/cmmotionactivityconfidence/low)
- [case medium](/documentation/coremotion/cmmotionactivityconfidence/medium)
- [case high](/documentation/coremotion/cmmotionactivityconfidence/high)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmmotionactivityconfidence/init(rawvalue:))
- [Getting motion-activity data from headphones](/documentation/coremotion/getting-motion-activity-data-from-headphones)

## Pedometer and fitness

- [CMPedometer](/documentation/coremotion/cmpedometer)

### Determining Pedometer Availability

- [class func isStepCountingAvailable() -> Bool](/documentation/coremotion/cmpedometer/isstepcountingavailable())
- [class func isDistanceAvailable() -> Bool](/documentation/coremotion/cmpedometer/isdistanceavailable())
- [class func isFloorCountingAvailable() -> Bool](/documentation/coremotion/cmpedometer/isfloorcountingavailable())
- [class func isPaceAvailable() -> Bool](/documentation/coremotion/cmpedometer/ispaceavailable())
- [class func isCadenceAvailable() -> Bool](/documentation/coremotion/cmpedometer/iscadenceavailable())
- [class func isPedometerEventTrackingAvailable() -> Bool](/documentation/coremotion/cmpedometer/ispedometereventtrackingavailable())
- [class func authorizationStatus() -> CMAuthorizationStatus](/documentation/coremotion/cmpedometer/authorizationstatus())
- [CMAuthorizationStatus](/documentation/coremotion/cmauthorizationstatus)

#### Enumeration Cases

- [case notDetermined](/documentation/coremotion/cmauthorizationstatus/notdetermined)
- [case restricted](/documentation/coremotion/cmauthorizationstatus/restricted)
- [case denied](/documentation/coremotion/cmauthorizationstatus/denied)
- [case authorized](/documentation/coremotion/cmauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmauthorizationstatus/init(rawvalue:))

### Gathering Live Pedometer Data

- [func startUpdates(from: Date, withHandler: CMPedometerHandler)](/documentation/coremotion/cmpedometer/startupdates(from:withhandler:))
- [func stopUpdates()](/documentation/coremotion/cmpedometer/stopupdates())
- [func startEventUpdates(handler: CMPedometerEventHandler)](/documentation/coremotion/cmpedometer/starteventupdates(handler:))
- [func stopEventUpdates()](/documentation/coremotion/cmpedometer/stopeventupdates())
- [CMPedometerHandler](/documentation/coremotion/cmpedometerhandler)
- [CMPedometerEventHandler](/documentation/coremotion/cmpedometereventhandler)

### Fetching Historical Pedometer Data

- [func queryPedometerData(from: Date, to: Date, withHandler: CMPedometerHandler)](/documentation/coremotion/cmpedometer/querypedometerdata(from:to:withhandler:))
- [CMPedometerData](/documentation/coremotion/cmpedometerdata)

### Getting the Dates

- [var startDate: Date](/documentation/coremotion/cmpedometerdata/startdate)
- [var endDate: Date](/documentation/coremotion/cmpedometerdata/enddate)

### Getting the Pedestrian Data

- [var numberOfSteps: NSNumber](/documentation/coremotion/cmpedometerdata/numberofsteps)
- [var distance: NSNumber?](/documentation/coremotion/cmpedometerdata/distance)
- [var averageActivePace: NSNumber?](/documentation/coremotion/cmpedometerdata/averageactivepace)
- [var currentPace: NSNumber?](/documentation/coremotion/cmpedometerdata/currentpace)
- [var currentCadence: NSNumber?](/documentation/coremotion/cmpedometerdata/currentcadence)

### Getting the Floor Counts

- [var floorsAscended: NSNumber?](/documentation/coremotion/cmpedometerdata/floorsascended)
- [var floorsDescended: NSNumber?](/documentation/coremotion/cmpedometerdata/floorsdescended)
- [CMPedometerEvent](/documentation/coremotion/cmpedometerevent)

### Pedometer Data

- [var date: Date](/documentation/coremotion/cmpedometerevent/date)
- [var type: CMPedometerEventType](/documentation/coremotion/cmpedometerevent/type)
- [CMPedometerEventType](/documentation/coremotion/cmpedometereventtype)

#### Enumeration Cases

- [case pause](/documentation/coremotion/cmpedometereventtype/pause)
- [case resume](/documentation/coremotion/cmpedometereventtype/resume)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmpedometereventtype/init(rawvalue:))
- [CMStepCounter](/documentation/coremotion/cmstepcounter)

### Determining Step Counting Availability

- [class func isStepCountingAvailable() -> Bool](/documentation/coremotion/cmstepcounter/isstepcountingavailable())

### Starting and Stopping Step Counting Updates

- [func startStepCountingUpdates(to: OperationQueue, updateOn: Int, withHandler: CMStepUpdateHandler)](/documentation/coremotion/cmstepcounter/startstepcountingupdates(to:updateon:withhandler:))
- [func stopStepCountingUpdates()](/documentation/coremotion/cmstepcounter/stopstepcountingupdates())
- [CMStepUpdateHandler](/documentation/coremotion/cmstepupdatehandler)

### Getting Historical Step Counting Data

- [func queryStepCountStarting(from: Date, to: Date, to: OperationQueue, withHandler: CMStepQueryHandler)](/documentation/coremotion/cmstepcounter/querystepcountstarting(from:to:to:withhandler:))
- [CMStepQueryHandler](/documentation/coremotion/cmstepqueryhandler)
- [CMOdometerData](/documentation/coremotion/cmodometerdata)

### Getting speed and slope

- [var speed: CLLocationSpeed](/documentation/coremotion/cmodometerdata/speed)
- [var slope: Double?](/documentation/coremotion/cmodometerdata/slope-9h3m4)
- [var maxAbsSlope: Double?](/documentation/coremotion/cmodometerdata/maxabsslope-9mnfd)

### Getting date and times

- [var startDate: Date](/documentation/coremotion/cmodometerdata/startdate)
- [var endDate: Date](/documentation/coremotion/cmodometerdata/enddate)
- [var gpsDate: Date](/documentation/coremotion/cmodometerdata/gpsdate)

### Measuring distances

- [var deltaDistance: CLLocationDistance](/documentation/coremotion/cmodometerdata/deltadistance)
- [var deltaAltitude: CLLocationDistance](/documentation/coremotion/cmodometerdata/deltaaltitude)

### Getting the location accuracy

- [var speedAccuracy: CLLocationSpeedAccuracy](/documentation/coremotion/cmodometerdata/speedaccuracy)
- [var verticalAccuracy: CLLocationAccuracy](/documentation/coremotion/cmodometerdata/verticalaccuracy)
- [var deltaDistanceAccuracy: CLLocationAccuracy](/documentation/coremotion/cmodometerdata/deltadistanceaccuracy)

### Getting the device

- [var originDevice: CMOdometerOriginDevice](/documentation/coremotion/cmodometerdata/origindevice)
- [CMOdometerOriginDevice](/documentation/coremotion/cmodometerorigindevice)

#### Device origins

- [case unknown](/documentation/coremotion/cmodometerorigindevice/unknown)
- [case local](/documentation/coremotion/cmodometerorigindevice/local)
- [case remote](/documentation/coremotion/cmodometerorigindevice/remote)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmodometerorigindevice/init(rawvalue:))
- [CMHighFrequencyHeartRateData](/documentation/coremotion/cmhighfrequencyheartratedata)

### Accessing heart rate data

- [var heartRate: Double](/documentation/coremotion/cmhighfrequencyheartratedata/heartrate)
- [var confidence: CMHighFrequencyHeartRateDataConfidence](/documentation/coremotion/cmhighfrequencyheartratedata/confidence)
- [CMHighFrequencyHeartRateDataConfidence](/documentation/coremotion/cmhighfrequencyheartratedataconfidence)

#### Levels of confidence

- [case low](/documentation/coremotion/cmhighfrequencyheartratedataconfidence/low)
- [case medium](/documentation/coremotion/cmhighfrequencyheartratedataconfidence/medium)
- [case high](/documentation/coremotion/cmhighfrequencyheartratedataconfidence/high)
- [case highest](/documentation/coremotion/cmhighfrequencyheartratedataconfidence/highest)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmhighfrequencyheartratedataconfidence/init(rawvalue:))

### Getting the sample date

- [var date: Date?](/documentation/coremotion/cmhighfrequencyheartratedata/date)

## Movement disorder

- [Getting movement disorder symptom data](/documentation/coremotion/getting-movement-disorder-symptom-data)
- [Adhering to the movement disorder data collection requirements](/documentation/coremotion/adhering-to-the-movement-disorder-data-collection-requirements)
- [Movement disorder algorithm changelog](/documentation/coremotion/movement-disorder-algorithm-changelog)
- [CMMovementDisorderManager](/documentation/coremotion/cmmovementdisordermanager)

### Checking Availablility

- [class func isAvailable() -> Bool](/documentation/coremotion/cmmovementdisordermanager/isavailable())
- [class func authorizationStatus() -> CMAuthorizationStatus](/documentation/coremotion/cmmovementdisordermanager/authorizationstatus())
- [class func version() -> String?](/documentation/coremotion/cmmovementdisordermanager/version())

### Recording Movement Disorders

- [func monitorKinesias(forDuration: TimeInterval)](/documentation/coremotion/cmmovementdisordermanager/monitorkinesias(forduration:))
- [func monitorKinesiasExpirationDate() -> Date?](/documentation/coremotion/cmmovementdisordermanager/monitorkinesiasexpirationdate())

### Querying for Movement Disorders

- [func queryTremor(from: Date, to: Date, withHandler: CMTremorResultHandler)](/documentation/coremotion/cmmovementdisordermanager/querytremor(from:to:withhandler:))
- [CMTremorResultHandler](/documentation/coremotion/cmtremorresulthandler)
- [func queryDyskineticSymptom(from: Date, to: Date, withHandler: CMDyskineticSymptomResultHandler)](/documentation/coremotion/cmmovementdisordermanager/querydyskineticsymptom(from:to:withhandler:))
- [CMDyskineticSymptomResultHandler](/documentation/coremotion/cmdyskineticsymptomresulthandler)
- [func lastProcessedDate() -> Date?](/documentation/coremotion/cmmovementdisordermanager/lastprocesseddate())
- [CMTremorResult](/documentation/coremotion/cmtremorresult)

### Reading the Time Interval

- [var startDate: Date](/documentation/coremotion/cmtremorresult/startdate)
- [var endDate: Date](/documentation/coremotion/cmtremorresult/enddate)

### Accessing Tremor Data

- [var percentUnknown: Float](/documentation/coremotion/cmtremorresult/percentunknown)
- [var percentNone: Float](/documentation/coremotion/cmtremorresult/percentnone)
- [var percentSlight: Float](/documentation/coremotion/cmtremorresult/percentslight)
- [var percentMild: Float](/documentation/coremotion/cmtremorresult/percentmild)
- [var percentModerate: Float](/documentation/coremotion/cmtremorresult/percentmoderate)
- [var percentStrong: Float](/documentation/coremotion/cmtremorresult/percentstrong)
- [CMDyskineticSymptomResult](/documentation/coremotion/cmdyskineticsymptomresult)

### Reading the Time Interval

- [var startDate: Date](/documentation/coremotion/cmdyskineticsymptomresult/startdate)
- [var endDate: Date](/documentation/coremotion/cmdyskineticsymptomresult/enddate)

### Accessing Dyskinetic Symptom Data

- [var percentUnlikely: Float](/documentation/coremotion/cmdyskineticsymptomresult/percentunlikely)
- [var percentLikely: Float](/documentation/coremotion/cmdyskineticsymptomresult/percentlikely)

## Fall detection

- [CMFallDetectionManager](/documentation/coremotion/cmfalldetectionmanager)

### Checking Availability

- [class var isAvailable: Bool](/documentation/coremotion/cmfalldetectionmanager/isavailable)

### Requesting Authorization

- [func requestAuthorization(handler: (CMAuthorizationStatus) -> Void)](/documentation/coremotion/cmfalldetectionmanager/requestauthorization(handler:))
- [var authorizationStatus: CMAuthorizationStatus](/documentation/coremotion/cmfalldetectionmanager/authorizationstatus)
- [CMAuthorizationStatus](/documentation/coremotion/cmauthorizationstatus)

#### Enumeration Cases

- [case notDetermined](/documentation/coremotion/cmauthorizationstatus/notdetermined)
- [case restricted](/documentation/coremotion/cmauthorizationstatus/restricted)
- [case denied](/documentation/coremotion/cmauthorizationstatus/denied)
- [case authorized](/documentation/coremotion/cmauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmauthorizationstatus/init(rawvalue:))

### Handling Events

- [var delegate: (any CMFallDetectionDelegate)?](/documentation/coremotion/cmfalldetectionmanager/delegate)
- [CMFallDetectionDelegate](/documentation/coremotion/cmfalldetectiondelegate)

#### Detecting Falls

- [func fallDetectionManager(CMFallDetectionManager, didDetect: CMFallDetectionEvent, completionHandler: () -> Void)](/documentation/coremotion/cmfalldetectiondelegate/falldetectionmanager(_:diddetect:completionhandler:))

#### Detecting Authorization Changes

- [func fallDetectionManagerDidChangeAuthorization(CMFallDetectionManager)](/documentation/coremotion/cmfalldetectiondelegate/falldetectionmanagerdidchangeauthorization(_:))
- [CMFallDetectionDelegate](/documentation/coremotion/cmfalldetectiondelegate)

### Detecting Falls

- [func fallDetectionManager(CMFallDetectionManager, didDetect: CMFallDetectionEvent, completionHandler: () -> Void)](/documentation/coremotion/cmfalldetectiondelegate/falldetectionmanager(_:diddetect:completionhandler:))

### Detecting Authorization Changes

- [func fallDetectionManagerDidChangeAuthorization(CMFallDetectionManager)](/documentation/coremotion/cmfalldetectiondelegate/falldetectionmanagerdidchangeauthorization(_:))
- [CMFallDetectionEvent](/documentation/coremotion/cmfalldetectionevent)

### Accessing Fall Data

- [var resolution: CMFallDetectionEvent.UserResolution](/documentation/coremotion/cmfalldetectionevent/resolution)
- [CMFallDetectionEvent.UserResolution](/documentation/coremotion/cmfalldetectionevent/userresolution)

#### Resolutions

- [case confirmed](/documentation/coremotion/cmfalldetectionevent/userresolution/confirmed)
- [case dismissed](/documentation/coremotion/cmfalldetectionevent/userresolution/dismissed)
- [case rejected](/documentation/coremotion/cmfalldetectionevent/userresolution/rejected)
- [case unresponsive](/documentation/coremotion/cmfalldetectionevent/userresolution/unresponsive)

#### Initializers

- [init?(rawValue: Int)](/documentation/coremotion/cmfalldetectionevent/userresolution/init(rawvalue:))

### Getting the event date

- [var date: Date](/documentation/coremotion/cmfalldetectionevent/date)
- [NSFallDetectionUsageDescription](/documentation/bundleresources/information-property-list/nsfalldetectionusagedescription)

## Historical data

- [CMBatchedSensorManager](/documentation/coremotion/cmbatchedsensormanager)

### Determining authorization and availability

- [class var authorizationStatus: CMAuthorizationStatus](/documentation/coremotion/cmbatchedsensormanager/authorizationstatus)
- [class var isAccelerometerSupported: Bool](/documentation/coremotion/cmbatchedsensormanager/isaccelerometersupported)
- [class var isDeviceMotionSupported: Bool](/documentation/coremotion/cmbatchedsensormanager/isdevicemotionsupported)

### Configuring the update frequency

- [var deviceMotionDataFrequency: Int](/documentation/coremotion/cmbatchedsensormanager/devicemotiondatafrequency)
- [var accelerometerDataFrequency: Int](/documentation/coremotion/cmbatchedsensormanager/accelerometerdatafrequency)

### Collecting device-motion data

- [func startDeviceMotionUpdates()](/documentation/coremotion/cmbatchedsensormanager/startdevicemotionupdates())
- [func startDeviceMotionUpdates(handler: ([CMDeviceMotion]?, (any Error)?) -> Void)](/documentation/coremotion/cmbatchedsensormanager/startdevicemotionupdates(handler:))
- [func stopDeviceMotionUpdates()](/documentation/coremotion/cmbatchedsensormanager/stopdevicemotionupdates())
- [var deviceMotionBatch: [CMDeviceMotion]?](/documentation/coremotion/cmbatchedsensormanager/devicemotionbatch)
- [func deviceMotionUpdates() -> CMBatchedSensorManager.DeviceMotionUpdates](/documentation/coremotion/cmbatchedsensormanager/devicemotionupdates())
- [CMBatchedSensorManager.DeviceMotionUpdates](/documentation/coremotion/cmbatchedsensormanager/devicemotionupdates)

#### Structures

- [CMBatchedSensorManager.DeviceMotionUpdates.Iterator](/documentation/coremotion/cmbatchedsensormanager/devicemotionupdates/iterator)
- [var isDeviceMotionActive: Bool](/documentation/coremotion/cmbatchedsensormanager/isdevicemotionactive)

### Collecting accelerometer data

- [func startAccelerometerUpdates()](/documentation/coremotion/cmbatchedsensormanager/startaccelerometerupdates())
- [func startAccelerometerUpdates(handler: ([CMAccelerometerData]?, (any Error)?) -> Void)](/documentation/coremotion/cmbatchedsensormanager/startaccelerometerupdates(handler:))
- [func stopAccelerometerUpdates()](/documentation/coremotion/cmbatchedsensormanager/stopaccelerometerupdates())
- [var accelerometerBatch: [CMAccelerometerData]?](/documentation/coremotion/cmbatchedsensormanager/accelerometerbatch)
- [func accelerometerUpdates() -> CMBatchedSensorManager.AccelerometerUpdates](/documentation/coremotion/cmbatchedsensormanager/accelerometerupdates())
- [CMBatchedSensorManager.AccelerometerUpdates](/documentation/coremotion/cmbatchedsensormanager/accelerometerupdates)

#### Structures

- [CMBatchedSensorManager.AccelerometerUpdates.Iterator](/documentation/coremotion/cmbatchedsensormanager/accelerometerupdates/iterator)
- [var isAccelerometerActive: Bool](/documentation/coremotion/cmbatchedsensormanager/isaccelerometeractive)

## Common data

- [CMLogItem](/documentation/coremotion/cmlogitem)

### Getting the Time of the Event

- [var timestamp: TimeInterval](/documentation/coremotion/cmlogitem/timestamp)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
