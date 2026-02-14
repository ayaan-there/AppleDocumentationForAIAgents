# Sound Analysis Documentation

Source: https://sosumi.ai/documentation/soundanalysis

---
title: Sound Analysis
source: https://developer.apple.com/documentation/soundanalysis
timestamp: 2026-02-13T19:02:27.521Z
---

## Audio analyzers

- [Classifying Sounds in an Audio File](/documentation/soundanalysis/classifying-sounds-in-an-audio-file)
- [SNAudioFileAnalyzer](/documentation/soundanalysis/snaudiofileanalyzer)

### Creating an Analyzer

- [init(url: URL) throws](/documentation/soundanalysis/snaudiofileanalyzer/init(url:))

### Managing Requests

- [func add(any SNRequest, withObserver: any SNResultsObserving) throws](/documentation/soundanalysis/snaudiofileanalyzer/add(_:withobserver:))
- [SNRequest](/documentation/soundanalysis/snrequest)
- [SNResultsObserving](/documentation/soundanalysis/snresultsobserving)

#### Handling Requests

- [func request(any SNRequest, didProduce: any SNResult)](/documentation/soundanalysis/snresultsobserving/request(_:didproduce:))
- [SNResult](/documentation/soundanalysis/snresult)
- [func request(any SNRequest, didFailWithError: any Error)](/documentation/soundanalysis/snresultsobserving/request(_:didfailwitherror:))
- [func requestDidComplete(any SNRequest)](/documentation/soundanalysis/snresultsobserving/requestdidcomplete(_:))
- [func remove(any SNRequest)](/documentation/soundanalysis/snaudiofileanalyzer/remove(_:))
- [func removeAllRequests()](/documentation/soundanalysis/snaudiofileanalyzer/removeallrequests())

### Analyzing Data

- [func analyze()](/documentation/soundanalysis/snaudiofileanalyzer/analyze())
- [func analyze(completionHandler: (Bool) -> Void)](/documentation/soundanalysis/snaudiofileanalyzer/analyze(completionhandler:))
- [func cancelAnalysis()](/documentation/soundanalysis/snaudiofileanalyzer/cancelanalysis())
- [Classifying Sounds in an Audio Stream](/documentation/soundanalysis/classifying-sounds-in-an-audio-stream)
- [SNAudioStreamAnalyzer](/documentation/soundanalysis/snaudiostreamanalyzer)

### Creating an Analyzer

- [init(format: AVAudioFormat)](/documentation/soundanalysis/snaudiostreamanalyzer/init(format:))

### Managing Requests

- [func add(any SNRequest, withObserver: any SNResultsObserving) throws](/documentation/soundanalysis/snaudiostreamanalyzer/add(_:withobserver:))
- [SNRequest](/documentation/soundanalysis/snrequest)
- [SNResultsObserving](/documentation/soundanalysis/snresultsobserving)

#### Handling Requests

- [func request(any SNRequest, didProduce: any SNResult)](/documentation/soundanalysis/snresultsobserving/request(_:didproduce:))
- [SNResult](/documentation/soundanalysis/snresult)
- [func request(any SNRequest, didFailWithError: any Error)](/documentation/soundanalysis/snresultsobserving/request(_:didfailwitherror:))
- [func requestDidComplete(any SNRequest)](/documentation/soundanalysis/snresultsobserving/requestdidcomplete(_:))
- [func remove(any SNRequest)](/documentation/soundanalysis/snaudiostreamanalyzer/remove(_:))
- [func removeAllRequests()](/documentation/soundanalysis/snaudiostreamanalyzer/removeallrequests())

### Analyzing Data

- [func analyze(AVAudioBuffer, atAudioFramePosition: AVAudioFramePosition)](/documentation/soundanalysis/snaudiostreamanalyzer/analyze(_:ataudioframeposition:))
- [func completeAnalysis()](/documentation/soundanalysis/snaudiostreamanalyzer/completeanalysis())

## Sound classification requests

- [Classifying Live Audio Input with a Built-in Sound Classifier](/documentation/soundanalysis/classifying-live-audio-input-with-a-built-in-sound-classifier)
- [SNClassifySoundRequest](/documentation/soundanalysis/snclassifysoundrequest)

### Creating a Request

- [init(mlModel: MLModel) throws](/documentation/soundanalysis/snclassifysoundrequest/init(mlmodel:))
- [init(classifierIdentifier: SNClassifierIdentifier) throws](/documentation/soundanalysis/snclassifysoundrequest/init(classifieridentifier:))
- [SNClassifierIdentifier](/documentation/soundanalysis/snclassifieridentifier)

#### Selecting a Sound Classifier

- [static let version1: SNClassifierIdentifier](/documentation/soundanalysis/snclassifieridentifier/version1)

#### Creating an Identifier

- [init(rawValue: String)](/documentation/soundanalysis/snclassifieridentifier/init(rawvalue:))

### Configuring a Request

- [var overlapFactor: Double](/documentation/soundanalysis/snclassifysoundrequest/overlapfactor)
- [var windowDuration: CMTime](/documentation/soundanalysis/snclassifysoundrequest/windowduration)

### Inspecting a Request

- [var knownClassifications: [String]](/documentation/soundanalysis/snclassifysoundrequest/knownclassifications)
- [SNTimeDurationConstraint](/documentation/soundanalysis/sntimedurationconstraint-swift.enum)

#### Inspecting a Constraint

- [case durationRange(CMTimeRange)](/documentation/soundanalysis/sntimedurationconstraint-swift.enum/durationrange(_:))
- [case enumeratedDurations([CMTime])](/documentation/soundanalysis/sntimedurationconstraint-swift.enum/enumerateddurations(_:))

### Instance Properties

- [var windowDurationConstraint: SNTimeDurationConstraint](/documentation/soundanalysis/snclassifysoundrequest/windowdurationconstraint-5no60)
- [SNClassificationResult](/documentation/soundanalysis/snclassificationresult)

### Inspecting the Result

- [var timeRange: CMTimeRange](/documentation/soundanalysis/snclassificationresult/timerange)
- [var classifications: [SNClassification]](/documentation/soundanalysis/snclassificationresult/classifications)
- [SNClassification](/documentation/soundanalysis/snclassification)

#### Inspecting a Classification

- [var identifier: String](/documentation/soundanalysis/snclassification/identifier)
- [var confidence: Double](/documentation/soundanalysis/snclassification/confidence)
- [func classification(forIdentifier: String) -> SNClassification?](/documentation/soundanalysis/snclassificationresult/classification(foridentifier:))

## Errors

- [SNError](/documentation/soundanalysis/snerror)

### Error Codes

- [static var invalidModel: SNError.Code](/documentation/soundanalysis/snerror/invalidmodel)
- [static var invalidFormat: SNError.Code](/documentation/soundanalysis/snerror/invalidformat)
- [static var invalidFile: SNError.Code](/documentation/soundanalysis/snerror/invalidfile)
- [static var operationFailed: SNError.Code](/documentation/soundanalysis/snerror/operationfailed)
- [static var unknownError: SNError.Code](/documentation/soundanalysis/snerror/unknownerror)

### Error Information

- [SNError.Code](/documentation/soundanalysis/snerror/code)

#### Errors

- [case invalidModel](/documentation/soundanalysis/snerror/code/invalidmodel)
- [case invalidFormat](/documentation/soundanalysis/snerror/code/invalidformat)
- [case invalidFile](/documentation/soundanalysis/snerror/code/invalidfile)
- [case operationFailed](/documentation/soundanalysis/snerror/code/operationfailed)
- [case unknownError](/documentation/soundanalysis/snerror/code/unknownerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/soundanalysis/snerror/code/init(rawvalue:))

### Error Domain

- [let SNErrorDomain: String](/documentation/soundanalysis/snerrordomain)
- [static var errorDomain: String](/documentation/soundanalysis/snerror/errordomain)
- [SNError.Code](/documentation/soundanalysis/snerror/code)

### Errors

- [case invalidModel](/documentation/soundanalysis/snerror/code/invalidmodel)
- [case invalidFormat](/documentation/soundanalysis/snerror/code/invalidformat)
- [case invalidFile](/documentation/soundanalysis/snerror/code/invalidfile)
- [case operationFailed](/documentation/soundanalysis/snerror/code/operationfailed)
- [case unknownError](/documentation/soundanalysis/snerror/code/unknownerror)

### Initializers

- [init?(rawValue: Int)](/documentation/soundanalysis/snerror/code/init(rawvalue:))
- [let SNErrorDomain: String](/documentation/soundanalysis/snerrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
