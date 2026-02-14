# RelevanceKit Documentation

Source: https://sosumi.ai/documentation/relevancekit

---
title: RelevanceKit
source: https://developer.apple.com/documentation/relevancekit
timestamp: 2026-02-13T19:01:12.879Z
---

## Providing relevance information

- [Increasing the visibility of widgets in Smart Stacks](/documentation/widgetkit/widget-suggestions-in-smart-stacks)
- [RelevantContext](/documentation/relevancekit/relevantcontext)

### Fitness clues

- [static func fitness(RelevantContext.FitnessCondition) -> RelevantContext](/documentation/relevancekit/relevantcontext/fitness(_:))
- [RelevantContext.FitnessCondition](/documentation/relevancekit/relevantcontext/fitnesscondition)

#### Conditions

- [static var activityRingsIncomplete: RelevantContext.FitnessCondition](/documentation/relevancekit/relevantcontext/fitnesscondition/activityringsincomplete)
- [static var workoutActive: RelevantContext.FitnessCondition](/documentation/relevancekit/relevantcontext/fitnesscondition/workoutactive)

### Hardware clues

- [static func hardware(headphones: RelevantContext.HeadphonesCondition) -> RelevantContext](/documentation/relevancekit/relevantcontext/hardware(headphones:))
- [RelevantContext.HeadphonesCondition](/documentation/relevancekit/relevantcontext/headphonescondition)

#### Conditions

- [static var connected: RelevantContext.HeadphonesCondition](/documentation/relevancekit/relevantcontext/headphonescondition/connected)

### Location clues

- [static func location(category: MKPointOfInterestCategory) -> RelevantContext?](/documentation/relevancekit/relevantcontext/location(category:))
- [static func location(CLRegion) -> RelevantContext](/documentation/relevancekit/relevantcontext/location(_:))
- [static func location(inferred: RelevantContext.InferredLocation) -> RelevantContext](/documentation/relevancekit/relevantcontext/location(inferred:))
- [RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation)

#### Conditions

- [static var commute: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/commute)
- [static var home: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/home)
- [static var school: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/school)
- [static var work: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/work)

### Sleep clues

- [static func sleep(RelevantContext.SleepCondition) -> RelevantContext](/documentation/relevancekit/relevantcontext/sleep(_:))
- [RelevantContext.SleepCondition](/documentation/relevancekit/relevantcontext/sleepcondition)

#### Conditions

- [static var bedtime: RelevantContext.SleepCondition](/documentation/relevancekit/relevantcontext/sleepcondition/bedtime)
- [static var wakeup: RelevantContext.SleepCondition](/documentation/relevancekit/relevantcontext/sleepcondition/wakeup)

### Time clues

- [static func date(Date) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(_:))
- [static func date(Date, kind: RelevantContext.DateKind) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(_:kind:))
- [static func date(interval: DateInterval, kind: RelevantContext.DateKind) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(interval:kind:))
- [static func date(range: ClosedRange<Date>, kind: RelevantContext.DateKind) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(range:kind:))
- [RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind)

#### Date types

- [static var `default`: RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind/default)
- [static var informational: RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind/informational)
- [static var scheduled: RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind/scheduled)
- [static func date(from: Date, to: Date) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(from:to:))

## Fitness clues

- [static func fitness(RelevantContext.FitnessCondition) -> RelevantContext](/documentation/relevancekit/relevantcontext/fitness(_:))
- [RelevantContext.FitnessCondition](/documentation/relevancekit/relevantcontext/fitnesscondition)

### Conditions

- [static var activityRingsIncomplete: RelevantContext.FitnessCondition](/documentation/relevancekit/relevantcontext/fitnesscondition/activityringsincomplete)
- [static var workoutActive: RelevantContext.FitnessCondition](/documentation/relevancekit/relevantcontext/fitnesscondition/workoutactive)

## Hardware clues

- [static func hardware(headphones: RelevantContext.HeadphonesCondition) -> RelevantContext](/documentation/relevancekit/relevantcontext/hardware(headphones:))
- [RelevantContext.HeadphonesCondition](/documentation/relevancekit/relevantcontext/headphonescondition)

### Conditions

- [static var connected: RelevantContext.HeadphonesCondition](/documentation/relevancekit/relevantcontext/headphonescondition/connected)

## Location clues

- [static func location(CLRegion) -> RelevantContext](/documentation/relevancekit/relevantcontext/location(_:))
- [static func location(inferred: RelevantContext.InferredLocation) -> RelevantContext](/documentation/relevancekit/relevantcontext/location(inferred:))
- [RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation)

### Conditions

- [static var commute: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/commute)
- [static var home: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/home)
- [static var school: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/school)
- [static var work: RelevantContext.InferredLocation](/documentation/relevancekit/relevantcontext/inferredlocation/work)

## Sleep clues

- [static func sleep(RelevantContext.SleepCondition) -> RelevantContext](/documentation/relevancekit/relevantcontext/sleep(_:))
- [RelevantContext.SleepCondition](/documentation/relevancekit/relevantcontext/sleepcondition)

### Conditions

- [static var bedtime: RelevantContext.SleepCondition](/documentation/relevancekit/relevantcontext/sleepcondition/bedtime)
- [static var wakeup: RelevantContext.SleepCondition](/documentation/relevancekit/relevantcontext/sleepcondition/wakeup)

## Time clues

- [static func date(Date) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(_:))
- [static func date(Date, kind: RelevantContext.DateKind) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(_:kind:))
- [static func date(interval: DateInterval, kind: RelevantContext.DateKind) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(interval:kind:))
- [static func date(range: ClosedRange<Date>, kind: RelevantContext.DateKind) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(range:kind:))
- [RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind)

### Date types

- [static var `default`: RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind/default)
- [static var informational: RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind/informational)
- [static var scheduled: RelevantContext.DateKind](/documentation/relevancekit/relevantcontext/datekind/scheduled)
- [static func date(from: Date, to: Date) -> RelevantContext](/documentation/relevancekit/relevantcontext/date(from:to:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
