# WorkoutKit Documentation

Source: https://sosumi.ai/documentation/workoutkit

---
title: WorkoutKit
source: https://developer.apple.com/documentation/workoutkit
timestamp: 2026-02-13T19:04:20.671Z
---

## Essentials

- [Customizing workouts with WorkoutKit](/documentation/workoutkit/customizing-workouts-with-workoutkit)

## Common workouts

- [SingleGoalWorkout](/documentation/workoutkit/singlegoalworkout)

### Creating single goal workouts

- [init(activity: HKWorkoutActivityType, location: HKWorkoutSessionLocationType, swimmingLocation: HKWorkoutSwimmingLocationType, goal: WorkoutGoal)](/documentation/workoutkit/singlegoalworkout/init(activity:location:swimminglocation:goal:))
- [static func supportsActivity(HKWorkoutActivityType) -> Bool](/documentation/workoutkit/singlegoalworkout/supportsactivity(_:))
- [static func supportsGoal(WorkoutGoal, activity: HKWorkoutActivityType, location: HKWorkoutSessionLocationType) -> Bool](/documentation/workoutkit/singlegoalworkout/supportsgoal(_:activity:location:))

### Accessing workout data

- [var activity: HKWorkoutActivityType](/documentation/workoutkit/singlegoalworkout/activity)
- [var location: HKWorkoutSessionLocationType](/documentation/workoutkit/singlegoalworkout/location)
- [var swimmingLocation: HKWorkoutSwimmingLocationType](/documentation/workoutkit/singlegoalworkout/swimminglocation)
- [var goal: WorkoutGoal](/documentation/workoutkit/singlegoalworkout/goal)

### Comparing workouts

- [var hashValue: Int](/documentation/workoutkit/singlegoalworkout/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/singlegoalworkout/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/singlegoalworkout/!=(_:_:))
- [static func == (SingleGoalWorkout, SingleGoalWorkout) -> Bool](/documentation/workoutkit/singlegoalworkout/==(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/singlegoalworkout/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/singlegoalworkout/!=(_:_:))
- [PacerWorkout](/documentation/workoutkit/pacerworkout)

### Creating a new pacer workout

- [init(activity: HKWorkoutActivityType, location: HKWorkoutSessionLocationType, distance: Measurement<UnitLength>, time: Measurement<UnitDuration>)](/documentation/workoutkit/pacerworkout/init(activity:location:distance:time:))
- [static func supportsActivity(HKWorkoutActivityType) -> Bool](/documentation/workoutkit/pacerworkout/supportsactivity(_:))

### Accessing workout data

- [var activity: HKWorkoutActivityType](/documentation/workoutkit/pacerworkout/activity)
- [var location: HKWorkoutSessionLocationType](/documentation/workoutkit/pacerworkout/location)
- [var distance: Measurement<UnitLength>](/documentation/workoutkit/pacerworkout/distance)
- [var time: Measurement<UnitDuration>](/documentation/workoutkit/pacerworkout/time)

### Comparing workouts

- [var hashValue: Int](/documentation/workoutkit/pacerworkout/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/pacerworkout/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/pacerworkout/!=(_:_:))
- [static func == (PacerWorkout, PacerWorkout) -> Bool](/documentation/workoutkit/pacerworkout/==(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/pacerworkout/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/pacerworkout/!=(_:_:))
- [SwimBikeRunWorkout](/documentation/workoutkit/swimbikerunworkout)

### Creating new multisport workouts.

- [init(activities: [SwimBikeRunWorkout.Activity], displayName: String?)](/documentation/workoutkit/swimbikerunworkout/init(activities:displayname:))
- [SwimBikeRunWorkout.Activity](/documentation/workoutkit/swimbikerunworkout/activity)

#### Setting valid activities

- [case cycling(HKWorkoutSessionLocationType)](/documentation/workoutkit/swimbikerunworkout/activity/cycling(_:))
- [case running(HKWorkoutSessionLocationType)](/documentation/workoutkit/swimbikerunworkout/activity/running(_:))
- [case swimming(HKWorkoutSwimmingLocationType)](/documentation/workoutkit/swimbikerunworkout/activity/swimming(_:))

#### Comparing activities

- [var hashValue: Int](/documentation/workoutkit/swimbikerunworkout/activity/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/swimbikerunworkout/activity/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/swimbikerunworkout/activity/!=(_:_:))
- [static func == (SwimBikeRunWorkout.Activity, SwimBikeRunWorkout.Activity) -> Bool](/documentation/workoutkit/swimbikerunworkout/activity/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/swimbikerunworkout/activity/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/swimbikerunworkout/activity/!=(_:_:))
- [static func supportsActivityOrdering([SwimBikeRunWorkout.Activity]) -> Bool](/documentation/workoutkit/swimbikerunworkout/supportsactivityordering(_:))

### Accessing workout data

- [var activities: [SwimBikeRunWorkout.Activity]](/documentation/workoutkit/swimbikerunworkout/activities)
- [var displayName: String?](/documentation/workoutkit/swimbikerunworkout/displayname)

### Comparing workouts

- [var hashValue: Int](/documentation/workoutkit/swimbikerunworkout/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/swimbikerunworkout/hash(into:))
- [static func == (SwimBikeRunWorkout, SwimBikeRunWorkout) -> Bool](/documentation/workoutkit/swimbikerunworkout/==(_:_:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/swimbikerunworkout/!=(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/swimbikerunworkout/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/swimbikerunworkout/!=(_:_:))

## Custom interval workouts

- [CustomWorkout](/documentation/workoutkit/customworkout)

### Creating custom workouts

- [init(activity: HKWorkoutActivityType, location: HKWorkoutSessionLocationType, displayName: String?, warmup: WorkoutStep?, blocks: [IntervalBlock], cooldown: WorkoutStep?)](/documentation/workoutkit/customworkout/init(activity:location:displayname:warmup:blocks:cooldown:))
- [static func supportsActivity(HKWorkoutActivityType) -> Bool](/documentation/workoutkit/customworkout/supportsactivity(_:))
- [static func supportsAlert(WorkoutAlert, activity: HKWorkoutActivityType, location: HKWorkoutSessionLocationType) -> Bool](/documentation/workoutkit/customworkout/supportsalert(_:activity:location:))
- [static func supportsGoal(WorkoutGoal, activity: HKWorkoutActivityType, location: HKWorkoutSessionLocationType) -> Bool](/documentation/workoutkit/customworkout/supportsgoal(_:activity:location:))

### Accessing workout data

- [var displayName: String?](/documentation/workoutkit/customworkout/displayname)
- [var activity: HKWorkoutActivityType](/documentation/workoutkit/customworkout/activity)
- [var location: HKWorkoutSessionLocationType](/documentation/workoutkit/customworkout/location)
- [var warmup: WorkoutStep?](/documentation/workoutkit/customworkout/warmup)
- [var blocks: [IntervalBlock]](/documentation/workoutkit/customworkout/blocks)
- [var cooldown: WorkoutStep?](/documentation/workoutkit/customworkout/cooldown)

### Comparing workouts

- [var hashValue: Int](/documentation/workoutkit/customworkout/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/customworkout/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/customworkout/!=(_:_:))
- [static func == (CustomWorkout, CustomWorkout) -> Bool](/documentation/workoutkit/customworkout/==(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/customworkout/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/customworkout/!=(_:_:))
- [WorkoutStep](/documentation/workoutkit/workoutstep)

### Creating new workout steps

- [init(goal: WorkoutGoal, alert: (WorkoutAlert)?)](/documentation/workoutkit/workoutstep/init(goal:alert:))

### Accessing step data

- [var alert: (WorkoutAlert)?](/documentation/workoutkit/workoutstep/alert)
- [var goal: WorkoutGoal](/documentation/workoutkit/workoutstep/goal)

### Comparing workout steps

- [var hashValue: Int](/documentation/workoutkit/workoutstep/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/workoutstep/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutstep/!=(_:_:))
- [static func == (WorkoutStep, WorkoutStep) -> Bool](/documentation/workoutkit/workoutstep/==(_:_:))

### Initializers

- [init(goal: WorkoutGoal, alert: (any WorkoutAlert)?, displayName: String?)](/documentation/workoutkit/workoutstep/init(goal:alert:displayname:))

### Instance Properties

- [var displayName: String?](/documentation/workoutkit/workoutstep/displayname)

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/workoutstep/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutstep/!=(_:_:))
- [IntervalBlock](/documentation/workoutkit/intervalblock)

### Creating an interval block

- [init(steps: [IntervalStep], iterations: Int)](/documentation/workoutkit/intervalblock/init(steps:iterations:))

### Accessing interval block properties

- [var steps: [IntervalStep]](/documentation/workoutkit/intervalblock/steps)
- [var iterations: Int](/documentation/workoutkit/intervalblock/iterations)

### Hashing interval blocks

- [var hashValue: Int](/documentation/workoutkit/intervalblock/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/intervalblock/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/intervalblock/!=(_:_:))
- [static func == (IntervalBlock, IntervalBlock) -> Bool](/documentation/workoutkit/intervalblock/==(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/intervalblock/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/intervalblock/!=(_:_:))
- [IntervalStep](/documentation/workoutkit/intervalstep)

### Creating interval steps

- [init(IntervalStep.Purpose, goal: WorkoutGoal, alert: (WorkoutAlert)?)](/documentation/workoutkit/intervalstep/init(_:goal:alert:))
- [init(IntervalStep.Purpose, step: WorkoutStep)](/documentation/workoutkit/intervalstep/init(_:step:))

### Accessing step data

- [var purpose: IntervalStep.Purpose](/documentation/workoutkit/intervalstep/purpose-swift.property)
- [var step: WorkoutStep](/documentation/workoutkit/intervalstep/step)

### Comparing interval steps

- [var hashValue: Int](/documentation/workoutkit/intervalstep/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/intervalstep/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/intervalstep/!=(_:_:))
- [static func == (IntervalStep, IntervalStep) -> Bool](/documentation/workoutkit/intervalstep/==(_:_:))

### Enumerations

- [IntervalStep.Purpose](/documentation/workoutkit/intervalstep/purpose-swift.enum)

#### Determining the purpose

- [case recovery](/documentation/workoutkit/intervalstep/purpose-swift.enum/recovery)
- [case work](/documentation/workoutkit/intervalstep/purpose-swift.enum/work)

#### Comparing purposes

- [var hashValue: Int](/documentation/workoutkit/intervalstep/purpose-swift.enum/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/intervalstep/purpose-swift.enum/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/intervalstep/purpose-swift.enum/!=(_:_:))
- [static func == (IntervalStep.Purpose, IntervalStep.Purpose) -> Bool](/documentation/workoutkit/intervalstep/purpose-swift.enum/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/intervalstep/purpose-swift.enum/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/intervalstep/purpose-swift.enum/!=(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/intervalstep/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/intervalstep/!=(_:_:))
- [WorkoutGoal](/documentation/workoutkit/workoutgoal)

### Determining workout goals

- [case open](/documentation/workoutkit/workoutgoal/open)
- [case distance(Double, UnitLength)](/documentation/workoutkit/workoutgoal/distance(_:_:))
- [case energy(Double, UnitEnergy)](/documentation/workoutkit/workoutgoal/energy(_:_:))
- [case time(Double, UnitDuration)](/documentation/workoutkit/workoutgoal/time(_:_:))

### Comparing workout goals

- [var hashValue: Int](/documentation/workoutkit/workoutgoal/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/workoutgoal/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutgoal/!=(_:_:))
- [static func == (WorkoutGoal, WorkoutGoal) -> Bool](/documentation/workoutkit/workoutgoal/==(_:_:))

### Enumeration Cases

- [case poolSwimDistanceWithTime(Measurement<UnitLength>, Measurement<UnitDuration>)](/documentation/workoutkit/workoutgoal/poolswimdistancewithtime(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/workoutgoal/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutgoal/!=(_:_:))
- [WorkoutAlert](/documentation/workoutkit/workoutalert)

### Determining support

- [func supports(activity: HKWorkoutActivityType, location: HKWorkoutSessionLocationType) -> Bool](/documentation/workoutkit/workoutalert/supports(activity:location:))

### Setting the alert metric

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/workoutalert/metric)
- [WorkoutAlertMetric](/documentation/workoutkit/workoutalertmetric)

#### Determining the metric’s type

- [case average](/documentation/workoutkit/workoutalertmetric/average)
- [case current](/documentation/workoutkit/workoutalertmetric/current)

#### Accessing the metric’s value

- [static var countPerMinute: UnitFrequency](/documentation/workoutkit/workoutalertmetric/countperminute)

#### Comparing metrics

- [static func == (WorkoutAlertMetric, WorkoutAlertMetric) -> Bool](/documentation/workoutkit/workoutalertmetric/==(_:_:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutalertmetric/!=(_:_:))
- [var hashValue: Int](/documentation/workoutkit/workoutalertmetric/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/workoutalertmetric/hash(into:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/workoutalertmetric/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutalertmetric/!=(_:_:))

### Creating cadence alerts

- [static func cadence(ClosedRange<Double>, unit: UnitFrequency) -> Self](/documentation/workoutkit/workoutalert/cadence(_:unit:)-y8da)
- [CadenceRangeAlert](/documentation/workoutkit/cadencerangealert)

#### Creating new cadence range alerts

- [static func cadence(ClosedRange<Double>, unit: UnitFrequency) -> Self](/documentation/workoutkit/cadencerangealert/cadence(_:unit:))
- [init(target: ClosedRange<Measurement<UnitFrequency>>)](/documentation/workoutkit/cadencerangealert/init(target:))

#### Accessing the alert data

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/cadencerangealert/metric)
- [var target: ClosedRange<Measurement<UnitFrequency>>](/documentation/workoutkit/cadencerangealert/target)
- [var targetQuantityLowerBound: HKQuantity](/documentation/workoutkit/cadencerangealert/targetquantitylowerbound)
- [var targetQuantityUpperBound: HKQuantity](/documentation/workoutkit/cadencerangealert/targetquantityupperbound)

#### Comparing alerts

- [var hashValue: Int](/documentation/workoutkit/cadencerangealert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/cadencerangealert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/cadencerangealert/!=(_:_:))
- [static func == (CadenceRangeAlert, CadenceRangeAlert) -> Bool](/documentation/workoutkit/cadencerangealert/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/cadencerangealert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/cadencerangealert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/cadencerangealert/workoutalert-implementations)

##### Type Methods

- [static func cadence(ClosedRange<Double>, unit: UnitFrequency) -> Self](/documentation/workoutkit/cadencerangealert/cadence(_:unit:))
- [static func cadence(Double, unit: UnitFrequency) -> Self](/documentation/workoutkit/workoutalert/cadence(_:unit:)-3fnpg)
- [CadenceThresholdAlert](/documentation/workoutkit/cadencethresholdalert)

#### Creating new cadence threshold alerts

- [static func cadence(Double, unit: UnitFrequency) -> Self](/documentation/workoutkit/cadencethresholdalert/cadence(_:unit:))
- [init(target: Measurement<UnitFrequency>)](/documentation/workoutkit/cadencethresholdalert/init(target:))

#### Accessing the alert data

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/cadencethresholdalert/metric)
- [var target: Measurement<UnitFrequency>](/documentation/workoutkit/cadencethresholdalert/target)
- [var targetQuantity: HKQuantity](/documentation/workoutkit/cadencethresholdalert/targetquantity)

#### Comparing cadence threshold alerts

- [var hashValue: Int](/documentation/workoutkit/cadencethresholdalert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/cadencethresholdalert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/cadencethresholdalert/!=(_:_:))
- [static func == (CadenceThresholdAlert, CadenceThresholdAlert) -> Bool](/documentation/workoutkit/cadencethresholdalert/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/cadencethresholdalert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/cadencethresholdalert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/cadencethresholdalert/workoutalert-implementations)

##### Type Methods

- [static func cadence(Double, unit: UnitFrequency) -> Self](/documentation/workoutkit/cadencethresholdalert/cadence(_:unit:))

### Creating heart rate alerts

- [static func heartRate(ClosedRange<Double>, unit: UnitFrequency) -> Self](/documentation/workoutkit/workoutalert/heartrate(_:unit:))
- [HeartRateRangeAlert](/documentation/workoutkit/heartraterangealert)

#### Creating new heart rate alerts

- [static func heartRate(ClosedRange<Double>, unit: UnitFrequency) -> Self](/documentation/workoutkit/heartraterangealert/heartrate(_:unit:))
- [init(target: ClosedRange<Measurement<UnitFrequency>>)](/documentation/workoutkit/heartraterangealert/init(target:))

#### Accessing the alert data

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/heartraterangealert/metric)
- [var target: ClosedRange<Measurement<UnitFrequency>>](/documentation/workoutkit/heartraterangealert/target)
- [var targetQuantityLowerBound: HKQuantity](/documentation/workoutkit/heartraterangealert/targetquantitylowerbound)
- [var targetQuantityUpperBound: HKQuantity](/documentation/workoutkit/heartraterangealert/targetquantityupperbound)

#### Comparing heart rate range alerts

- [var hashValue: Int](/documentation/workoutkit/heartraterangealert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/heartraterangealert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/heartraterangealert/!=(_:_:))
- [static func == (HeartRateRangeAlert, HeartRateRangeAlert) -> Bool](/documentation/workoutkit/heartraterangealert/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/heartraterangealert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/heartraterangealert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/heartraterangealert/workoutalert-implementations)

##### Type Methods

- [static func heartRate(ClosedRange<Double>, unit: UnitFrequency) -> Self](/documentation/workoutkit/heartraterangealert/heartrate(_:unit:))
- [static func heartRate(zone: Int) -> Self](/documentation/workoutkit/workoutalert/heartrate(zone:))
- [HeartRateZoneAlert](/documentation/workoutkit/heartratezonealert)

#### Creating new heart rate zone alerts

- [static func heartRate(zone: Int) -> Self](/documentation/workoutkit/heartratezonealert/heartrate(zone:))
- [init(zone: Int)](/documentation/workoutkit/heartratezonealert/init(zone:))

#### Accessing the alert data

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/heartratezonealert/metric)
- [var zone: Int](/documentation/workoutkit/heartratezonealert/zone)

#### Comparing heart rate zone alerts

- [var hashValue: Int](/documentation/workoutkit/heartratezonealert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/heartratezonealert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/heartratezonealert/!=(_:_:))
- [static func == (HeartRateZoneAlert, HeartRateZoneAlert) -> Bool](/documentation/workoutkit/heartratezonealert/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/heartratezonealert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/heartratezonealert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/heartratezonealert/workoutalert-implementations)

##### Type Methods

- [static func heartRate(zone: Int) -> Self](/documentation/workoutkit/heartratezonealert/heartrate(zone:))

### Creating power alerts

- [static func power(ClosedRange<Double>, unit: UnitPower) -> Self](/documentation/workoutkit/workoutalert/power(_:unit:)-57ekz)
- [PowerRangeAlert](/documentation/workoutkit/powerrangealert)

#### Creating new power range alerts

- [static func power(ClosedRange<Double>, unit: UnitPower) -> Self](/documentation/workoutkit/powerrangealert/power(_:unit:))
- [init(target: ClosedRange<Measurement<UnitPower>>)](/documentation/workoutkit/powerrangealert/init(target:))

#### Accessing the alert value

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/powerrangealert/metric)
- [var target: ClosedRange<Measurement<UnitPower>>](/documentation/workoutkit/powerrangealert/target)
- [var targetQuantityLowerBound: HKQuantity](/documentation/workoutkit/powerrangealert/targetquantitylowerbound)
- [var targetQuantityUpperBound: HKQuantity](/documentation/workoutkit/powerrangealert/targetquantityupperbound)

#### Comparing alerts

- [var hashValue: Int](/documentation/workoutkit/powerrangealert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/powerrangealert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/powerrangealert/!=(_:_:))
- [static func == (PowerRangeAlert, PowerRangeAlert) -> Bool](/documentation/workoutkit/powerrangealert/==(_:_:))

#### Initializers

- [init(target: ClosedRange<Measurement<UnitPower>>, metric: WorkoutAlertMetric)](/documentation/workoutkit/powerrangealert/init(target:metric:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/powerrangealert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/powerrangealert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/powerrangealert/workoutalert-implementations)

##### Type Methods

- [static func power(ClosedRange<Double>, unit: UnitPower) -> Self](/documentation/workoutkit/powerrangealert/power(_:unit:))
- [static func power(Double, unit: UnitPower) -> Self](/documentation/workoutkit/workoutalert/power(_:unit:)-289mz)
- [PowerThresholdAlert](/documentation/workoutkit/powerthresholdalert)

#### Creating power threshold alerts

- [static func power(Double, unit: UnitPower) -> Self](/documentation/workoutkit/powerthresholdalert/power(_:unit:))
- [init(target: Measurement<UnitPower>)](/documentation/workoutkit/powerthresholdalert/init(target:))

#### Accessing alert data

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/powerthresholdalert/metric)
- [var target: Measurement<UnitPower>](/documentation/workoutkit/powerthresholdalert/target)
- [var targetQuantity: HKQuantity](/documentation/workoutkit/powerthresholdalert/targetquantity)

#### Comparing alerts

- [var hashValue: Int](/documentation/workoutkit/powerthresholdalert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/powerthresholdalert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/powerthresholdalert/!=(_:_:))
- [static func == (PowerThresholdAlert, PowerThresholdAlert) -> Bool](/documentation/workoutkit/powerthresholdalert/==(_:_:))

#### Initializers

- [init(target: Measurement<UnitPower>, metric: WorkoutAlertMetric)](/documentation/workoutkit/powerthresholdalert/init(target:metric:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/powerthresholdalert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/powerthresholdalert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/powerthresholdalert/workoutalert-implementations)

##### Type Methods

- [static func power(Double, unit: UnitPower) -> Self](/documentation/workoutkit/powerthresholdalert/power(_:unit:))
- [static func power(zone: Int) -> Self](/documentation/workoutkit/workoutalert/power(zone:))
- [PowerZoneAlert](/documentation/workoutkit/powerzonealert)

#### Creating power zone alerts

- [static func power(zone: Int) -> Self](/documentation/workoutkit/powerzonealert/power(zone:))
- [init(zone: Int)](/documentation/workoutkit/powerzonealert/init(zone:))

#### Accessing alert data

- [var metric: WorkoutAlertMetric](/documentation/workoutkit/powerzonealert/metric)
- [var zone: Int](/documentation/workoutkit/powerzonealert/zone)

#### Comparing alerts

- [var hashValue: Int](/documentation/workoutkit/powerzonealert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/powerzonealert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/powerzonealert/!=(_:_:))
- [static func == (PowerZoneAlert, PowerZoneAlert) -> Bool](/documentation/workoutkit/powerzonealert/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/powerzonealert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/powerzonealert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/powerzonealert/workoutalert-implementations)

##### Type Methods

- [static func power(zone: Int) -> Self](/documentation/workoutkit/powerzonealert/power(zone:))

### Creating speed alerts

- [static func speed(ClosedRange<Double>, unit: UnitSpeed, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/workoutalert/speed(_:unit:metric:)-1o2j)
- [SpeedRangeAlert](/documentation/workoutkit/speedrangealert)

#### Creating speed range alerts

- [static func speed(ClosedRange<Double>, unit: UnitSpeed, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/speedrangealert/speed(_:unit:metric:))
- [init(target: ClosedRange<Measurement<UnitSpeed>>, metric: WorkoutAlertMetric)](/documentation/workoutkit/speedrangealert/init(target:metric:))

#### Accessing alert data

- [var target: ClosedRange<Measurement<UnitSpeed>>](/documentation/workoutkit/speedrangealert/target)
- [var targetQuantityLowerBound: HKQuantity](/documentation/workoutkit/speedrangealert/targetquantitylowerbound)
- [var targetQuantityUpperBound: HKQuantity](/documentation/workoutkit/speedrangealert/targetquantityupperbound)
- [var metric: WorkoutAlertMetric](/documentation/workoutkit/speedrangealert/metric)

#### Comparing alerts

- [var hashValue: Int](/documentation/workoutkit/speedrangealert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/speedrangealert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/speedrangealert/!=(_:_:))
- [static func == (SpeedRangeAlert, SpeedRangeAlert) -> Bool](/documentation/workoutkit/speedrangealert/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/speedrangealert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/speedrangealert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/speedrangealert/workoutalert-implementations)

##### Type Methods

- [static func speed(ClosedRange<Double>, unit: UnitSpeed, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/speedrangealert/speed(_:unit:metric:))
- [static func speed(Double, unit: UnitSpeed, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/workoutalert/speed(_:unit:metric:)-4zald)
- [SpeedThresholdAlert](/documentation/workoutkit/speedthresholdalert)

#### Creating speed threshold alerts

- [static func speed(Double, unit: UnitSpeed, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/speedthresholdalert/speed(_:unit:metric:))
- [init(target: Measurement<UnitSpeed>, metric: WorkoutAlertMetric)](/documentation/workoutkit/speedthresholdalert/init(target:metric:))

#### Accessing alert data

- [var target: Measurement<UnitSpeed>](/documentation/workoutkit/speedthresholdalert/target)
- [var targetQuantity: HKQuantity](/documentation/workoutkit/speedthresholdalert/targetquantity)
- [var metric: WorkoutAlertMetric](/documentation/workoutkit/speedthresholdalert/metric)

#### Comparing alerts

- [var hashValue: Int](/documentation/workoutkit/speedthresholdalert/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/speedthresholdalert/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/speedthresholdalert/!=(_:_:))
- [static func == (SpeedThresholdAlert, SpeedThresholdAlert) -> Bool](/documentation/workoutkit/speedthresholdalert/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/speedthresholdalert/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/speedthresholdalert/!=(_:_:))
- [WorkoutAlert Implementations](/documentation/workoutkit/speedthresholdalert/workoutalert-implementations)

##### Type Methods

- [static func speed(Double, unit: UnitSpeed, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/speedthresholdalert/speed(_:unit:metric:))

### Type Methods

- [static func power(Double, unit: UnitPower, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/workoutalert/power(_:unit:metric:)-2847m)
- [static func power(ClosedRange<Double>, unit: UnitPower, metric: WorkoutAlertMetric) -> Self](/documentation/workoutkit/workoutalert/power(_:unit:metric:)-5c94p)

## Workout plans and schedules

- [WorkoutPlan](/documentation/workoutkit/workoutplan)

### Creating a workout plan

- [init(WorkoutPlan.Workout, id: UUID)](/documentation/workoutkit/workoutplan/init(_:id:))
- [WorkoutPlan.Workout](/documentation/workoutkit/workoutplan/workout-swift.enum)

#### Setting the workout

- [case custom(CustomWorkout)](/documentation/workoutkit/workoutplan/workout-swift.enum/custom(_:))
- [case goal(SingleGoalWorkout)](/documentation/workoutkit/workoutplan/workout-swift.enum/goal(_:))
- [case pacer(PacerWorkout)](/documentation/workoutkit/workoutplan/workout-swift.enum/pacer(_:))
- [case swimBikeRun(SwimBikeRunWorkout)](/documentation/workoutkit/workoutplan/workout-swift.enum/swimbikerun(_:))

#### Accessing workout data

- [var activity: HKWorkoutActivityType](/documentation/workoutkit/workoutplan/workout-swift.enum/activity)

#### Comparing workout plans

- [var hashValue: Int](/documentation/workoutkit/workoutplan/workout-swift.enum/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/workoutplan/workout-swift.enum/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutplan/workout-swift.enum/!=(_:_:))
- [static func == (WorkoutPlan.Workout, WorkoutPlan.Workout) -> Bool](/documentation/workoutkit/workoutplan/workout-swift.enum/==(_:_:))

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/workoutplan/workout-swift.enum/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutplan/workout-swift.enum/!=(_:_:))

### Accessing workout plan data

- [var id: UUID](/documentation/workoutkit/workoutplan/id-swift.property)
- [WorkoutPlan.ID](/documentation/workoutkit/workoutplan/id-swift.typealias)
- [var workout: WorkoutPlan.Workout](/documentation/workoutkit/workoutplan/workout-swift.property)

### Opening the workout plan

- [func openInWorkoutApp() async throws](/documentation/workoutkit/workoutplan/openinworkoutapp())

### Initializers

- [init(from: Data) throws](/documentation/workoutkit/workoutplan/init(from:))

### Instance Properties

- [var dataRepresentation: Data](/documentation/workoutkit/workoutplan/datarepresentation)
- [var hashValue: Int](/documentation/workoutkit/workoutplan/hashvalue)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/workoutkit/workoutplan/hash(into:))

### Operator Functions

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutplan/!=(_:_:))
- [static func == (WorkoutPlan, WorkoutPlan) -> Bool](/documentation/workoutkit/workoutplan/==(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/workoutplan/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutplan/!=(_:_:))
- [ScheduledWorkoutPlan](/documentation/workoutkit/scheduledworkoutplan)

### Creating scheduled workout plans

- [init(WorkoutPlan, date: DateComponents)](/documentation/workoutkit/scheduledworkoutplan/init(_:date:))

### Accessing plan data

- [var plan: WorkoutPlan](/documentation/workoutkit/scheduledworkoutplan/plan)
- [var date: DateComponents](/documentation/workoutkit/scheduledworkoutplan/date)
- [var complete: Bool](/documentation/workoutkit/scheduledworkoutplan/complete)

### Comparing plans

- [var hashValue: Int](/documentation/workoutkit/scheduledworkoutplan/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/scheduledworkoutplan/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/scheduledworkoutplan/!=(_:_:))
- [static func == (ScheduledWorkoutPlan, ScheduledWorkoutPlan) -> Bool](/documentation/workoutkit/scheduledworkoutplan/==(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/scheduledworkoutplan/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/scheduledworkoutplan/!=(_:_:))
- [WorkoutScheduler](/documentation/workoutkit/workoutscheduler)

### Accessing the scheduler

- [static let shared: WorkoutScheduler](/documentation/workoutkit/workoutscheduler/shared)
- [static var isSupported: Bool](/documentation/workoutkit/workoutscheduler/issupported)
- [func requestAuthorization() async -> WorkoutScheduler.AuthorizationState](/documentation/workoutkit/workoutscheduler/requestauthorization())
- [var authorizationState: WorkoutScheduler.AuthorizationState](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.property)
- [WorkoutScheduler.AuthorizationState](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum)

#### Determining the authorization status

- [case authorized](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/authorized)
- [case denied](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/denied)
- [case notDetermined](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/notdetermined)
- [case restricted](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/restricted)

#### Working with the raw value

- [init?(rawValue: Int)](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/init(rawvalue:))
- [WorkoutScheduler.AuthorizationState.RawValue](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/rawvalue-swift.typealias)

#### Comparing authorization statuses

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/!=(_:_:))
- [var hashValue: Int](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/hash(into:))
- [var rawValue: Int](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/rawvalue-swift.property)

#### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/!=(_:_:))
- [RawRepresentable Implementations](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/rawrepresentable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/workoutkit/workoutscheduler/authorizationstate-swift.enum/hash(into:))

### Scheduling workouts

- [func schedule(WorkoutPlan, at: DateComponents) async](/documentation/workoutkit/workoutscheduler/schedule(_:at:))

### Managing scheduled workouts

- [var scheduledWorkouts: [ScheduledWorkoutPlan]](/documentation/workoutkit/workoutscheduler/scheduledworkouts)
- [static let maxAllowedScheduledWorkoutCount: Int](/documentation/workoutkit/workoutscheduler/maxallowedscheduledworkoutcount)
- [func markComplete(WorkoutPlan, at: DateComponents) async](/documentation/workoutkit/workoutscheduler/markcomplete(_:at:))
- [func remove(WorkoutPlan, at: DateComponents) async](/documentation/workoutkit/workoutscheduler/remove(_:at:))
- [func removeAllWorkouts() async](/documentation/workoutkit/workoutscheduler/removeallworkouts())

## Errors

- [StateError](/documentation/workoutkit/stateerror)

### Getting the error type

- [case watchNotPaired](/documentation/workoutkit/stateerror/watchnotpaired)
- [case workoutApplicationNotInstalled](/documentation/workoutkit/stateerror/workoutapplicationnotinstalled)

### Getting the error description

- [var localizedDescription: String](/documentation/workoutkit/stateerror/localizeddescription)

### Comparing state errors

- [var hashValue: Int](/documentation/workoutkit/stateerror/hashvalue)
- [func hash(into: inout Hasher)](/documentation/workoutkit/stateerror/hash(into:))
- [static func != (Self, Self) -> Bool](/documentation/workoutkit/stateerror/!=(_:_:))
- [static func == (StateError, StateError) -> Bool](/documentation/workoutkit/stateerror/==(_:_:))

### Default Implementations

- [Equatable Implementations](/documentation/workoutkit/stateerror/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/workoutkit/stateerror/!=(_:_:))
- [Error Implementations](/documentation/workoutkit/stateerror/error-implementations)

#### Instance Properties

- [var localizedDescription: String](/documentation/workoutkit/stateerror/localizeddescription)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
