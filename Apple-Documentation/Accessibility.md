# Accessibility Documentation

Source: https://sosumi.ai/documentation/accessibility

---
title: Accessibility
source: https://developer.apple.com/documentation/accessibility
timestamp: 2026-02-13T19:06:25.552Z
---

## Essentials

- [Accessibility updates](/documentation/updates/accessibility)
- [Accessibility](/design/human-interface-guidelines/accessibility)
- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)

## Sample code

- [Enhancing the accessibility of your SwiftUI app](/documentation/accessibility/enhancing-the-accessibility-of-your-swiftui-app)
- [Creating accessible views](/documentation/swiftui/creating-accessible-views)
- [Delivering an exceptional accessibility experience](/documentation/accessibility/delivering_an_exceptional_accessibility_experience)
- [Integrating accessibility into your app](/documentation/accessibility/integrating-accessibility-into-your-app)
- [Accessibility design for Mac Catalyst](/documentation/accessibility/accessibility_design_for_mac_catalyst)

## Domains

- [Vision](/documentation/accessibility/vision)

### Supporting vision accessibility features

- [VoiceOver](/documentation/accessibility/voiceover)

#### Develop for VoiceOver

- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [Supporting VoiceOver in your app](/documentation/uikit/supporting-voiceover-in-your-app)
- [WWDC21 Challenge: VoiceOver Maze](/documentation/accessibility/wwdc21_challenge_voiceover_maze)
- [Flashing lights](/documentation/mediaaccessibility/flashing-lights)
- [Audio graphs](/documentation/accessibility/audio-graphs)

#### Essentials

- [Representing chart data as an audio graph](/documentation/accessibility/representing-chart-data-as-an-audio-graph)

#### Chart representation

- [AXChart](/documentation/accessibility/axchart)

##### Supporting accessibility

- [var accessibilityChartDescriptor: AXChartDescriptor?](/documentation/accessibility/axchart/accessibilitychartdescriptor)
- [AXChartDescriptor](/documentation/accessibility/axchartdescriptor)

###### Creating a chart

- [convenience init(title: String?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(title:summary:xaxis:yaxis:additionalaxes:series:))
- [convenience init(attributedTitle: NSAttributedString?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(attributedtitle:summary:xaxis:yaxis:additionalaxes:series:))

###### Specifying the chart title

- [var title: String?](/documentation/accessibility/axchartdescriptor/title)
- [var attributedTitle: NSAttributedString?](/documentation/accessibility/axchartdescriptor/attributedtitle)

###### Specifying the chart summary

- [var summary: String?](/documentation/accessibility/axchartdescriptor/summary)

###### Specifying the axes

- [var xAxis: any AXDataAxisDescriptor](/documentation/accessibility/axchartdescriptor/xaxis-7sb9a)
- [var yAxis: AXNumericDataAxisDescriptor?](/documentation/accessibility/axchartdescriptor/yaxis)
- [var additionalAxes: [any AXDataAxisDescriptor]](/documentation/accessibility/axchartdescriptor/additionalaxes-2adwh)
- [AXDataAxisDescriptor](/documentation/accessibility/axdataaxisdescriptor)

###### Specifying the title

- [var title: String](/documentation/accessibility/axdataaxisdescriptor/title)
- [var attributedTitle: NSAttributedString](/documentation/accessibility/axdataaxisdescriptor/attributedtitle)

###### Specifying a series of data points

- [var series: [AXDataSeriesDescriptor]](/documentation/accessibility/axchartdescriptor/series)
- [AXDataSeriesDescriptor](/documentation/accessibility/axdataseriesdescriptor)

###### Creating a data series

- [init(name: String, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(name:iscontinuous:datapoints:))
- [init(attributedName: NSAttributedString, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(attributedname:iscontinuous:datapoints:))

###### Naming the series

- [var name: String?](/documentation/accessibility/axdataseriesdescriptor/name)
- [var attributedName: NSAttributedString](/documentation/accessibility/axdataseriesdescriptor/attributedname)

###### Configuring the data points

- [var isContinuous: Bool](/documentation/accessibility/axdataseriesdescriptor/iscontinuous)
- [var dataPoints: [AXDataPoint]](/documentation/accessibility/axdataseriesdescriptor/datapoints)
- [AXDataPoint](/documentation/accessibility/axdatapoint)

###### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

###### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

###### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)

###### Specifying the content layout

- [var contentFrame: CGRect](/documentation/accessibility/axchartdescriptor/contentframe)
- [var contentDirection: AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.property)
- [AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum)

###### Content directions

- [case leftToRight](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/lefttoright)
- [case rightToLeft](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/righttoleft)
- [case bottomToTop](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/bottomtotop)
- [case topToBottom](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/toptobottom)
- [case radialClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialclockwise)
- [case radialCounterClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialcounterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/init(rawvalue:))
- [AXChartDescriptor](/documentation/accessibility/axchartdescriptor)

##### Creating a chart

- [convenience init(title: String?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(title:summary:xaxis:yaxis:additionalaxes:series:))
- [convenience init(attributedTitle: NSAttributedString?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(attributedtitle:summary:xaxis:yaxis:additionalaxes:series:))

##### Specifying the chart title

- [var title: String?](/documentation/accessibility/axchartdescriptor/title)
- [var attributedTitle: NSAttributedString?](/documentation/accessibility/axchartdescriptor/attributedtitle)

##### Specifying the chart summary

- [var summary: String?](/documentation/accessibility/axchartdescriptor/summary)

##### Specifying the axes

- [var xAxis: any AXDataAxisDescriptor](/documentation/accessibility/axchartdescriptor/xaxis-7sb9a)
- [var yAxis: AXNumericDataAxisDescriptor?](/documentation/accessibility/axchartdescriptor/yaxis)
- [var additionalAxes: [any AXDataAxisDescriptor]](/documentation/accessibility/axchartdescriptor/additionalaxes-2adwh)
- [AXDataAxisDescriptor](/documentation/accessibility/axdataaxisdescriptor)

###### Specifying the title

- [var title: String](/documentation/accessibility/axdataaxisdescriptor/title)
- [var attributedTitle: NSAttributedString](/documentation/accessibility/axdataaxisdescriptor/attributedtitle)

##### Specifying a series of data points

- [var series: [AXDataSeriesDescriptor]](/documentation/accessibility/axchartdescriptor/series)
- [AXDataSeriesDescriptor](/documentation/accessibility/axdataseriesdescriptor)

###### Creating a data series

- [init(name: String, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(name:iscontinuous:datapoints:))
- [init(attributedName: NSAttributedString, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(attributedname:iscontinuous:datapoints:))

###### Naming the series

- [var name: String?](/documentation/accessibility/axdataseriesdescriptor/name)
- [var attributedName: NSAttributedString](/documentation/accessibility/axdataseriesdescriptor/attributedname)

###### Configuring the data points

- [var isContinuous: Bool](/documentation/accessibility/axdataseriesdescriptor/iscontinuous)
- [var dataPoints: [AXDataPoint]](/documentation/accessibility/axdataseriesdescriptor/datapoints)
- [AXDataPoint](/documentation/accessibility/axdatapoint)

###### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

###### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

###### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)

##### Specifying the content layout

- [var contentFrame: CGRect](/documentation/accessibility/axchartdescriptor/contentframe)
- [var contentDirection: AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.property)
- [AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum)

###### Content directions

- [case leftToRight](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/lefttoright)
- [case rightToLeft](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/righttoleft)
- [case bottomToTop](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/bottomtotop)
- [case topToBottom](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/toptobottom)
- [case radialClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialclockwise)
- [case radialCounterClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialcounterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/init(rawvalue:))

#### Axis representation

- [AXDataAxisDescriptor](/documentation/accessibility/axdataaxisdescriptor)

##### Specifying the title

- [var title: String](/documentation/accessibility/axdataaxisdescriptor/title)
- [var attributedTitle: NSAttributedString](/documentation/accessibility/axdataaxisdescriptor/attributedtitle)
- [AXCategoricalDataAxisDescriptor](/documentation/accessibility/axcategoricaldataaxisdescriptor)

##### Creating a categorical data axis

- [init(title: String, categoryOrder: [String])](/documentation/accessibility/axcategoricaldataaxisdescriptor/init(title:categoryorder:))
- [init(attributedTitle: NSAttributedString, categoryOrder: [String])](/documentation/accessibility/axcategoricaldataaxisdescriptor/init(attributedtitle:categoryorder:))

##### Configuring the order of categories

- [var categoryOrder: [String]](/documentation/accessibility/axcategoricaldataaxisdescriptor/categoryorder)
- [AXNumericDataAxisDescriptor](/documentation/accessibility/axnumericdataaxisdescriptor)

##### Creating a numeric data axis

- [convenience init(title: String, range: ClosedRange<Double>, gridlinePositions: [Double], valueDescriptionProvider: (Double) -> String)](/documentation/accessibility/axnumericdataaxisdescriptor/init(title:range:gridlinepositions:valuedescriptionprovider:))
- [convenience init(attributedTitle: NSAttributedString, range: ClosedRange<Double>, gridlinePositions: [Double], valueDescriptionProvider: (Double) -> String)](/documentation/accessibility/axnumericdataaxisdescriptor/init(attributedtitle:range:gridlinepositions:valuedescriptionprovider:))

##### Specifying the value description

- [var valueDescriptionProvider: (Double) -> String](/documentation/accessibility/axnumericdataaxisdescriptor/valuedescriptionprovider)

##### Configuring the axis scale

- [var scaleType: AXNumericDataAxisDescriptor.ScaleType](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.property)
- [AXNumericDataAxisDescriptor.ScaleType](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum)

###### Scales

- [case linear](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/linear)
- [case ln](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/ln)
- [case log10](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/log10)

###### Initializers

- [init?(rawValue: Int)](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/init(rawvalue:))

##### Configuring the axis range

- [var range: ClosedRange<Double>](/documentation/accessibility/axnumericdataaxisdescriptor/range)

##### Configuring the gridlines

- [var gridlinePositions: [Double]](/documentation/accessibility/axnumericdataaxisdescriptor/gridlinepositions-5cfmw)

#### Data representation

- [AXDataPoint](/documentation/accessibility/axdatapoint)

##### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

##### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

##### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)
- [AXDataSeriesDescriptor](/documentation/accessibility/axdataseriesdescriptor)

##### Creating a data series

- [init(name: String, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(name:iscontinuous:datapoints:))
- [init(attributedName: NSAttributedString, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(attributedname:iscontinuous:datapoints:))

##### Naming the series

- [var name: String?](/documentation/accessibility/axdataseriesdescriptor/name)
- [var attributedName: NSAttributedString](/documentation/accessibility/axdataseriesdescriptor/attributedname)

##### Configuring the data points

- [var isContinuous: Bool](/documentation/accessibility/axdataseriesdescriptor/iscontinuous)
- [var dataPoints: [AXDataPoint]](/documentation/accessibility/axdataseriesdescriptor/datapoints)
- [AXDataPoint](/documentation/accessibility/axdatapoint)

###### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

###### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

###### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)

#### Live audio graphs

- [AXLiveAudioGraph](/documentation/accessibility/axliveaudiograph)

##### Controlling playback

- [class func start()](/documentation/accessibility/axliveaudiograph/start())
- [class func stop()](/documentation/accessibility/axliveaudiograph/stop())

##### Configuring pitch

- [class func updateValue(Double)](/documentation/accessibility/axliveaudiograph/updatevalue(_:))
- [Braille displays](/documentation/accessibility/braille-displays)

#### Braille maps

- [AXBrailleMap](/documentation/accessibility/axbraillemap)

##### Creating a braille map

- [init?(coder: NSCoder)](/documentation/accessibility/axbraillemap/init(coder:))

##### Getting display dimensions

- [var dimensions: CGSize](/documentation/accessibility/axbraillemap/dimensions)

##### Accessing dots

- [func setHeight(Float, at: CGPoint)](/documentation/accessibility/axbraillemap/setheight(_:at:))
- [func height(at: CGPoint) -> Float](/documentation/accessibility/axbraillemap/height(at:))
- [subscript(CGPoint) -> Float](/documentation/accessibility/axbraillemap/subscript(_:))

##### Displaying images

- [func present(CGImage)](/documentation/accessibility/axbraillemap/present(_:))
- [AXBrailleMapRenderer](/documentation/accessibility/axbraillemaprenderer)

##### Rendering a specific region

- [var accessibilityBrailleMapRenderRegion: CGRect](/documentation/accessibility/axbraillemaprenderer/accessibilitybraillemaprenderregion)

##### Updating the braille map manually

- [var accessibilityBrailleMapRenderer: (AXBrailleMap) -> Void](/documentation/accessibility/axbraillemaprenderer/accessibilitybraillemaprenderer)
- [Animated images](/documentation/accessibility/animated-images)

#### Animated images

- [static var animatedImagesEnabled: Bool](/documentation/accessibility/accessibilitysettings/animatedimagesenabled)
- [static var animatedImagesEnabledDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/animatedimagesenableddidchangenotification)
- [Horizontal text](/documentation/accessibility/horizontal-text)

#### Horizontal text

- [static var prefersHorizontalTextLayout: Bool](/documentation/accessibility/accessibilitysettings/prefershorizontaltextlayout)
- [static var prefersHorizontalTextLayoutDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/prefershorizontaltextlayoutdidchangenotification)
- [WWDC21 Challenge: Large Text Challenge](/documentation/accessibility/wwdc21_challenge_large_text_challenge)
- [Speech](/documentation/accessibility/speech)

### Supporting speech accessibility features

- [Speech synthesis](/documentation/avfoundation/speech-synthesis)
- [AVSpeechSynthesizer](/documentation/avfaudio/avspeechsynthesizer)
- [WWDC21 Challenge: Speech Synthesizer Simulator](/documentation/accessibility/wwdc21_challenge_speech_synthesizer_simulator)
- [Mobility](/documentation/accessibility/mobility)

### Supporting mobility accessibility features

- [Voice Control](/documentation/accessibility/voice-control)

#### Develop for Voice Control

- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [Switch Control](/documentation/accessibility/switch-control)

#### Develop for Switch Control

- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [WWDC22 Challenge: Learn Switch Control through gaming](/documentation/accessibility/wwdc22_challenge_learn_switch_control_through_gaming)
- [Cognitive](/documentation/accessibility/cognitive)

### Supporting cognitive accessibility features

- [Assistive Access](/documentation/accessibility/assistive-access)

#### Develop for Assistive Access

- [Optimizing your app for Assistive Access](/documentation/accessibility/optimizing-your-app-for-assistive-access)
- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [static var isAssistiveAccessEnabled: Bool](/documentation/accessibility/accessibilitysettings/isassistiveaccessenabled)
- [var accessibilityAssistiveAccessEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityassistiveaccessenabled)
- [UISupportsFullScreenInAssistiveAccess](/documentation/bundleresources/information-property-list/uisupportsfullscreeninassistiveaccess)
- [static var isAssistiveAccessEnabled: Bool](/documentation/accessibility/accessibilitysettings/isassistiveaccessenabled)
- [UISupportsFullScreenInAssistiveAccess](/documentation/bundleresources/information-property-list/uisupportsfullscreeninassistiveaccess)
- [Hearing](/documentation/accessibility/hearing)

### Supporting hearing accessibility features

- [Hearing device support](/documentation/accessibility/hearing-device-support)

#### Hearing devices

- [AXMFiHearingDevice](/documentation/accessibility/axmfihearingdevice)

##### Streaming status

- [static func streamingEar() -> AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/streamingear())
- [AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear)

###### Constants

- [static var both: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/both)
- [static var left: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/left)
- [static var right: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/right)

###### Initializer

- [init(rawValue: UInt)](/documentation/accessibility/axmfihearingdevice/ear/init(rawvalue:))
- [static let streamingEarDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/streamingeardidchangenotification)

##### Streaming type

- [static func supportsBidirectionalStreaming() -> Bool](/documentation/accessibility/axmfihearingdevice/supportsbidirectionalstreaming())

##### Paired hearing devices

- [static func pairedDeviceIdentifiers() -> [UUID]](/documentation/accessibility/axmfihearingdevice/paireddeviceidentifiers())
- [static let pairedUUIDsDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/paireduuidsdidchangenotification)

#### Streaming status

- [AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear)

##### Constants

- [static var both: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/both)
- [static var left: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/left)
- [static var right: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/right)

##### Initializer

- [init(rawValue: UInt)](/documentation/accessibility/axmfihearingdevice/ear/init(rawvalue:))
- [static func streamingEar() -> AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/streamingear())
- [static let streamingEarDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/streamingeardidchangenotification)

#### Streaming type

- [static func supportsBidirectionalStreaming() -> Bool](/documentation/accessibility/axmfihearingdevice/supportsbidirectionalstreaming())

#### Paired hearing devices

- [static func pairedDeviceIdentifiers() -> [UUID]](/documentation/accessibility/axmfihearingdevice/paireddeviceidentifiers())
- [static let pairedUUIDsDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/paireduuidsdidchangenotification)
- [Music Haptics](/documentation/mediaaccessibility/music-haptics)
- [Captions](/documentation/mediaaccessibility/captions)

## Developer tools

- [Accessibility Inspector](/documentation/accessibility/accessibility-inspector)

### App inspection

- [Inspecting the accessibility of the screens in your app](/documentation/accessibility/inspecting-the-accessibility-of-screens)

### Accessibility audits

- [Performing accessibility audits for your app](/documentation/accessibility/performing-accessibility-audits-for-your-app)

### Accessibility feature testing

- [Testing system accessibility features in your app](/documentation/accessibility/testing-system-accessibility-features-in-your-app)

## Assistive technologies

- [Assistive technologies](/documentation/accessibility/assistive-technologies)

### Assistive technologies

- [VoiceOver](/documentation/accessibility/voiceover)

#### Develop for VoiceOver

- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [Supporting VoiceOver in your app](/documentation/uikit/supporting-voiceover-in-your-app)
- [WWDC21 Challenge: VoiceOver Maze](/documentation/accessibility/wwdc21_challenge_voiceover_maze)
- [Voice Control](/documentation/accessibility/voice-control)

#### Develop for Voice Control

- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [Switch Control](/documentation/accessibility/switch-control)

#### Develop for Switch Control

- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [WWDC22 Challenge: Learn Switch Control through gaming](/documentation/accessibility/wwdc22_challenge_learn_switch_control_through_gaming)
- [Assistive Access](/documentation/accessibility/assistive-access)

#### Develop for Assistive Access

- [Optimizing your app for Assistive Access](/documentation/accessibility/optimizing-your-app-for-assistive-access)
- [Performing accessibility testing for your app](/documentation/accessibility/performing-accessibility-testing-for-your-app)
- [static var isAssistiveAccessEnabled: Bool](/documentation/accessibility/accessibilitysettings/isassistiveaccessenabled)
- [var accessibilityAssistiveAccessEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityassistiveaccessenabled)
- [UISupportsFullScreenInAssistiveAccess](/documentation/bundleresources/information-property-list/uisupportsfullscreeninassistiveaccess)

## Accessibility framework

- [Accessibility API](/documentation/accessibility/accessibility-api)

### System settings

- [AccessibilitySettings](/documentation/accessibility/accessibilitysettings)

#### Opening the Settings app

- [static func openSettings(for: AccessibilitySettings.Feature) async throws](/documentation/accessibility/accessibilitysettings/opensettings(for:))
- [AccessibilitySettings.Feature](/documentation/accessibility/accessibilitysettings/feature)

##### Audio features

- [case personalVoiceAllowAppsToRequestToUse](/documentation/accessibility/accessibilitysettings/feature/personalvoiceallowappstorequesttouse)

##### Accessibility feature structure creation

- [init?(rawValue: Int)](/documentation/accessibility/accessibilitysettings/feature/init(rawvalue:))

##### Enumeration Cases

- [case allowAppsToAddAudioToCalls](/documentation/accessibility/accessibilitysettings/feature/allowappstoaddaudiotocalls)
- [case assistiveTouch](/documentation/accessibility/accessibilitysettings/feature/assistivetouch)
- [case assistiveTouchDevices](/documentation/accessibility/accessibilitysettings/feature/assistivetouchdevices)
- [case dwellControl](/documentation/accessibility/accessibilitysettings/feature/dwellcontrol)

#### Pausing animated images

- [Animated images](/documentation/accessibility/animated-images)

##### Animated images

- [static var animatedImagesEnabled: Bool](/documentation/accessibility/accessibilitysettings/animatedimagesenabled)
- [static var animatedImagesEnabledDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/animatedimagesenableddidchangenotification)
- [static var animatedImagesEnabled: Bool](/documentation/accessibility/accessibilitysettings/animatedimagesenabled)
- [static var animatedImagesEnabledDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/animatedimagesenableddidchangenotification)

#### Customizing vertical text layout

- [Horizontal text](/documentation/accessibility/horizontal-text)

##### Horizontal text

- [static var prefersHorizontalTextLayout: Bool](/documentation/accessibility/accessibilitysettings/prefershorizontaltextlayout)
- [static var prefersHorizontalTextLayoutDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/prefershorizontaltextlayoutdidchangenotification)
- [static var prefersHorizontalTextLayout: Bool](/documentation/accessibility/accessibilitysettings/prefershorizontaltextlayout)
- [static var prefersHorizontalTextLayoutDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/prefershorizontaltextlayoutdidchangenotification)

#### Supporting head-anchored content

- [static var prefersHeadAnchorAlternative: Bool](/documentation/accessibility/accessibilitysettings/prefersheadanchoralternative)
- [static var prefersHeadAnchorAlternativeDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/prefersheadanchoralternativedidchangenotification)

#### Reducing animation for text insertion indicators

- [static var prefersNonBlinkingTextInsertionIndicator: Bool](/documentation/accessibility/accessibilitysettings/prefersnonblinkingtextinsertionindicator)
- [static let prefersNonBlinkingTextInsertionIndicatorDidChangeNotification: NSNotification.Name](/documentation/accessibility/accessibilitysettings/prefersnonblinkingtextinsertionindicatordidchangenotification)

#### Checking if Assistive Access is running

- [static var isAssistiveAccessEnabled: Bool](/documentation/accessibility/accessibilitysettings/isassistiveaccessenabled)

#### Creating an accessibility settings structure

- [init()](/documentation/accessibility/accessibilitysettings/init())

#### Type Properties

- [static var prefersActionSliderAlternative: Bool](/documentation/accessibility/accessibilitysettings/prefersactionslideralternative)
- [static let prefersActionSliderAlternativeDidChangeNotification: NSNotification.Name](/documentation/accessibility/accessibilitysettings/prefersactionslideralternativedidchangenotification)
- [static var showBordersEnabled: Bool](/documentation/accessibility/accessibilitysettings/showbordersenabled)
- [static let showBordersEnabledStatusDidChangeNotification: NSNotification.Name](/documentation/accessibility/accessibilitysettings/showbordersenabledstatusdidchangenotification)

### Notifications

- [AccessibilityNotification](/documentation/accessibility/accessibilitynotification)

#### Notifications

- [AccessibilityNotification.Announcement](/documentation/accessibility/accessibilitynotification/announcement)

##### Creating an announcement notification

- [init(String)](/documentation/accessibility/accessibilitynotification/announcement/init(_:)-621va)
- [init(NSAttributedString)](/documentation/accessibility/accessibilitynotification/announcement/init(_:)-46byj)
- [init(AttributedString)](/documentation/accessibility/accessibilitynotification/announcement/init(_:)-btpf)
- [AccessibilityNotification.LayoutChanged](/documentation/accessibility/accessibilitynotification/layoutchanged)

##### Creating a layout change notification

- [init(Any?)](/documentation/accessibility/accessibilitynotification/layoutchanged/init(_:))
- [AccessibilityNotification.ScreenChanged](/documentation/accessibility/accessibilitynotification/screenchanged)

##### Creating a screen change notification

- [init(Any?)](/documentation/accessibility/accessibilitynotification/screenchanged/init(_:))
- [AccessibilityNotification.PageScrolled](/documentation/accessibility/accessibilitynotification/pagescrolled)

##### Creating a page scroll notification

- [init(String)](/documentation/accessibility/accessibilitynotification/pagescrolled/init(_:)-28520)
- [init(AttributedString)](/documentation/accessibility/accessibilitynotification/pagescrolled/init(_:)-39fee)
- [init(NSAttributedString)](/documentation/accessibility/accessibilitynotification/pagescrolled/init(_:)-2lkx)

### Assistive technologies

- [AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology)

#### Initializers

- [init(rawValue: String)](/documentation/accessibility/accessibilitytechnology/init(rawvalue:))
- [static let automation: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/automation)
- [static let fullKeyboardAccess: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/fullkeyboardaccess)
- [static let hoverText: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/hovertext)
- [static let speakScreen: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/speakscreen)
- [static let switchControl: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/switchcontrol)
- [static let voiceControl: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/voicecontrol)
- [static let voiceOver: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/voiceover)
- [static let zoom: AccessibilityTechnology](/documentation/accessibility/accessibilitytechnology/zoom)
- [AccessibilityRequest](/documentation/accessibility/accessibilityrequest)

#### Instance Properties

- [var technology: AccessibilityTechnology](/documentation/accessibility/accessibilityrequest/technology)

#### Type Properties

- [class var current: AccessibilityRequest?](/documentation/accessibility/accessibilityrequest/current)

### Features

- [Customized accessibility content](/documentation/accessibility/customized-accessibility-content)

#### Custom accessibility content

- [AXCustomContent](/documentation/accessibility/axcustomcontent)

##### Creating custom content

- [convenience init(attributedLabel: NSAttributedString, attributedValue: NSAttributedString)](/documentation/accessibility/axcustomcontent/init(attributedlabel:attributedvalue:))
- [convenience init(label: String, value: String)](/documentation/accessibility/axcustomcontent/init(label:value:))
- [init?(coder: NSCoder)](/documentation/accessibility/axcustomcontent/init(coder:))

##### Defining custom content

- [var label: String](/documentation/accessibility/axcustomcontent/label)
- [var attributedLabel: NSAttributedString](/documentation/accessibility/axcustomcontent/attributedlabel)
- [var value: String](/documentation/accessibility/axcustomcontent/value)
- [var attributedValue: NSAttributedString](/documentation/accessibility/axcustomcontent/attributedvalue)
- [var importance: AXCustomContent.Importance](/documentation/accessibility/axcustomcontent/importance-swift.property)
- [AXCustomContent.Importance](/documentation/accessibility/axcustomcontent/importance-swift.enum)

###### Creating a content importance enumeration

- [init?(rawValue: UInt)](/documentation/accessibility/axcustomcontent/importance-swift.enum/init(rawvalue:))

###### Setting content importance

- [case `default`](/documentation/accessibility/axcustomcontent/importance-swift.enum/default)
- [case high](/documentation/accessibility/axcustomcontent/importance-swift.enum/high)
- [AXCustomContentProvider](/documentation/accessibility/axcustomcontentprovider)

##### Providing custom content

- [var accessibilityCustomContent: [AXCustomContent]!](/documentation/accessibility/axcustomcontentprovider/accessibilitycustomcontent)

##### Instance Properties

- [var accessibilityCustomContentBlock: AXCustomContentReturnBlock?](/documentation/accessibility/axcustomcontentprovider/accessibilitycustomcontentblock)
- [AXCustomContentReturnBlock](/documentation/accessibility/axcustomcontentreturnblock)
- [Audio graphs](/documentation/accessibility/audio-graphs)

#### Essentials

- [Representing chart data as an audio graph](/documentation/accessibility/representing-chart-data-as-an-audio-graph)

#### Chart representation

- [AXChart](/documentation/accessibility/axchart)

##### Supporting accessibility

- [var accessibilityChartDescriptor: AXChartDescriptor?](/documentation/accessibility/axchart/accessibilitychartdescriptor)
- [AXChartDescriptor](/documentation/accessibility/axchartdescriptor)

###### Creating a chart

- [convenience init(title: String?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(title:summary:xaxis:yaxis:additionalaxes:series:))
- [convenience init(attributedTitle: NSAttributedString?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(attributedtitle:summary:xaxis:yaxis:additionalaxes:series:))

###### Specifying the chart title

- [var title: String?](/documentation/accessibility/axchartdescriptor/title)
- [var attributedTitle: NSAttributedString?](/documentation/accessibility/axchartdescriptor/attributedtitle)

###### Specifying the chart summary

- [var summary: String?](/documentation/accessibility/axchartdescriptor/summary)

###### Specifying the axes

- [var xAxis: any AXDataAxisDescriptor](/documentation/accessibility/axchartdescriptor/xaxis-7sb9a)
- [var yAxis: AXNumericDataAxisDescriptor?](/documentation/accessibility/axchartdescriptor/yaxis)
- [var additionalAxes: [any AXDataAxisDescriptor]](/documentation/accessibility/axchartdescriptor/additionalaxes-2adwh)
- [AXDataAxisDescriptor](/documentation/accessibility/axdataaxisdescriptor)

###### Specifying the title

- [var title: String](/documentation/accessibility/axdataaxisdescriptor/title)
- [var attributedTitle: NSAttributedString](/documentation/accessibility/axdataaxisdescriptor/attributedtitle)

###### Specifying a series of data points

- [var series: [AXDataSeriesDescriptor]](/documentation/accessibility/axchartdescriptor/series)
- [AXDataSeriesDescriptor](/documentation/accessibility/axdataseriesdescriptor)

###### Creating a data series

- [init(name: String, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(name:iscontinuous:datapoints:))
- [init(attributedName: NSAttributedString, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(attributedname:iscontinuous:datapoints:))

###### Naming the series

- [var name: String?](/documentation/accessibility/axdataseriesdescriptor/name)
- [var attributedName: NSAttributedString](/documentation/accessibility/axdataseriesdescriptor/attributedname)

###### Configuring the data points

- [var isContinuous: Bool](/documentation/accessibility/axdataseriesdescriptor/iscontinuous)
- [var dataPoints: [AXDataPoint]](/documentation/accessibility/axdataseriesdescriptor/datapoints)
- [AXDataPoint](/documentation/accessibility/axdatapoint)

###### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

###### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

###### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)

###### Specifying the content layout

- [var contentFrame: CGRect](/documentation/accessibility/axchartdescriptor/contentframe)
- [var contentDirection: AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.property)
- [AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum)

###### Content directions

- [case leftToRight](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/lefttoright)
- [case rightToLeft](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/righttoleft)
- [case bottomToTop](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/bottomtotop)
- [case topToBottom](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/toptobottom)
- [case radialClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialclockwise)
- [case radialCounterClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialcounterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/init(rawvalue:))
- [AXChartDescriptor](/documentation/accessibility/axchartdescriptor)

##### Creating a chart

- [convenience init(title: String?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(title:summary:xaxis:yaxis:additionalaxes:series:))
- [convenience init(attributedTitle: NSAttributedString?, summary: String?, xAxis: any AXDataAxisDescriptor, yAxis: AXNumericDataAxisDescriptor?, additionalAxes: [any AXDataAxisDescriptor], series: [AXDataSeriesDescriptor])](/documentation/accessibility/axchartdescriptor/init(attributedtitle:summary:xaxis:yaxis:additionalaxes:series:))

##### Specifying the chart title

- [var title: String?](/documentation/accessibility/axchartdescriptor/title)
- [var attributedTitle: NSAttributedString?](/documentation/accessibility/axchartdescriptor/attributedtitle)

##### Specifying the chart summary

- [var summary: String?](/documentation/accessibility/axchartdescriptor/summary)

##### Specifying the axes

- [var xAxis: any AXDataAxisDescriptor](/documentation/accessibility/axchartdescriptor/xaxis-7sb9a)
- [var yAxis: AXNumericDataAxisDescriptor?](/documentation/accessibility/axchartdescriptor/yaxis)
- [var additionalAxes: [any AXDataAxisDescriptor]](/documentation/accessibility/axchartdescriptor/additionalaxes-2adwh)
- [AXDataAxisDescriptor](/documentation/accessibility/axdataaxisdescriptor)

###### Specifying the title

- [var title: String](/documentation/accessibility/axdataaxisdescriptor/title)
- [var attributedTitle: NSAttributedString](/documentation/accessibility/axdataaxisdescriptor/attributedtitle)

##### Specifying a series of data points

- [var series: [AXDataSeriesDescriptor]](/documentation/accessibility/axchartdescriptor/series)
- [AXDataSeriesDescriptor](/documentation/accessibility/axdataseriesdescriptor)

###### Creating a data series

- [init(name: String, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(name:iscontinuous:datapoints:))
- [init(attributedName: NSAttributedString, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(attributedname:iscontinuous:datapoints:))

###### Naming the series

- [var name: String?](/documentation/accessibility/axdataseriesdescriptor/name)
- [var attributedName: NSAttributedString](/documentation/accessibility/axdataseriesdescriptor/attributedname)

###### Configuring the data points

- [var isContinuous: Bool](/documentation/accessibility/axdataseriesdescriptor/iscontinuous)
- [var dataPoints: [AXDataPoint]](/documentation/accessibility/axdataseriesdescriptor/datapoints)
- [AXDataPoint](/documentation/accessibility/axdatapoint)

###### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

###### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

###### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)

##### Specifying the content layout

- [var contentFrame: CGRect](/documentation/accessibility/axchartdescriptor/contentframe)
- [var contentDirection: AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.property)
- [AXChartDescriptor.ContentDirection](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum)

###### Content directions

- [case leftToRight](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/lefttoright)
- [case rightToLeft](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/righttoleft)
- [case bottomToTop](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/bottomtotop)
- [case topToBottom](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/toptobottom)
- [case radialClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialclockwise)
- [case radialCounterClockwise](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/radialcounterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/accessibility/axchartdescriptor/contentdirection-swift.enum/init(rawvalue:))

#### Axis representation

- [AXDataAxisDescriptor](/documentation/accessibility/axdataaxisdescriptor)

##### Specifying the title

- [var title: String](/documentation/accessibility/axdataaxisdescriptor/title)
- [var attributedTitle: NSAttributedString](/documentation/accessibility/axdataaxisdescriptor/attributedtitle)
- [AXCategoricalDataAxisDescriptor](/documentation/accessibility/axcategoricaldataaxisdescriptor)

##### Creating a categorical data axis

- [init(title: String, categoryOrder: [String])](/documentation/accessibility/axcategoricaldataaxisdescriptor/init(title:categoryorder:))
- [init(attributedTitle: NSAttributedString, categoryOrder: [String])](/documentation/accessibility/axcategoricaldataaxisdescriptor/init(attributedtitle:categoryorder:))

##### Configuring the order of categories

- [var categoryOrder: [String]](/documentation/accessibility/axcategoricaldataaxisdescriptor/categoryorder)
- [AXNumericDataAxisDescriptor](/documentation/accessibility/axnumericdataaxisdescriptor)

##### Creating a numeric data axis

- [convenience init(title: String, range: ClosedRange<Double>, gridlinePositions: [Double], valueDescriptionProvider: (Double) -> String)](/documentation/accessibility/axnumericdataaxisdescriptor/init(title:range:gridlinepositions:valuedescriptionprovider:))
- [convenience init(attributedTitle: NSAttributedString, range: ClosedRange<Double>, gridlinePositions: [Double], valueDescriptionProvider: (Double) -> String)](/documentation/accessibility/axnumericdataaxisdescriptor/init(attributedtitle:range:gridlinepositions:valuedescriptionprovider:))

##### Specifying the value description

- [var valueDescriptionProvider: (Double) -> String](/documentation/accessibility/axnumericdataaxisdescriptor/valuedescriptionprovider)

##### Configuring the axis scale

- [var scaleType: AXNumericDataAxisDescriptor.ScaleType](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.property)
- [AXNumericDataAxisDescriptor.ScaleType](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum)

###### Scales

- [case linear](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/linear)
- [case ln](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/ln)
- [case log10](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/log10)

###### Initializers

- [init?(rawValue: Int)](/documentation/accessibility/axnumericdataaxisdescriptor/scaletype-swift.enum/init(rawvalue:))

##### Configuring the axis range

- [var range: ClosedRange<Double>](/documentation/accessibility/axnumericdataaxisdescriptor/range)

##### Configuring the gridlines

- [var gridlinePositions: [Double]](/documentation/accessibility/axnumericdataaxisdescriptor/gridlinepositions-5cfmw)

#### Data representation

- [AXDataPoint](/documentation/accessibility/axdatapoint)

##### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

##### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

##### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)
- [AXDataSeriesDescriptor](/documentation/accessibility/axdataseriesdescriptor)

##### Creating a data series

- [init(name: String, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(name:iscontinuous:datapoints:))
- [init(attributedName: NSAttributedString, isContinuous: Bool, dataPoints: [AXDataPoint])](/documentation/accessibility/axdataseriesdescriptor/init(attributedname:iscontinuous:datapoints:))

##### Naming the series

- [var name: String?](/documentation/accessibility/axdataseriesdescriptor/name)
- [var attributedName: NSAttributedString](/documentation/accessibility/axdataseriesdescriptor/attributedname)

##### Configuring the data points

- [var isContinuous: Bool](/documentation/accessibility/axdataseriesdescriptor/iscontinuous)
- [var dataPoints: [AXDataPoint]](/documentation/accessibility/axdataseriesdescriptor/datapoints)
- [AXDataPoint](/documentation/accessibility/axdatapoint)

###### Creating a data point

- [convenience init(x: String, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-83xvg)
- [convenience init(x: Double, y: Double?, additionalValues: [AXDataPoint.Value], label: String?)](/documentation/accessibility/axdatapoint/init(x:y:additionalvalues:label:)-4v3sb)

###### Specifying the data value

- [var xValue: AXDataPointValue](/documentation/accessibility/axdatapoint/xvalue)
- [var yValue: AXDataPointValue?](/documentation/accessibility/axdatapoint/yvalue)
- [AXDataPointValue](/documentation/accessibility/axdatapointvalue)
- [AXDataPoint.Value](/documentation/accessibility/axdatapoint/value)

###### Constants

- [case category(String)](/documentation/accessibility/axdatapoint/value/category(_:))
- [case number(Double)](/documentation/accessibility/axdatapoint/value/number(_:))

###### Specifying the label

- [var label: String?](/documentation/accessibility/axdatapoint/label)
- [var attributedLabel: NSAttributedString?](/documentation/accessibility/axdatapoint/attributedlabel)

#### Live audio graphs

- [AXLiveAudioGraph](/documentation/accessibility/axliveaudiograph)

##### Controlling playback

- [class func start()](/documentation/accessibility/axliveaudiograph/start())
- [class func stop()](/documentation/accessibility/axliveaudiograph/stop())

##### Configuring pitch

- [class func updateValue(Double)](/documentation/accessibility/axliveaudiograph/updatevalue(_:))
- [Hearing device support](/documentation/accessibility/hearing-device-support)

#### Hearing devices

- [AXMFiHearingDevice](/documentation/accessibility/axmfihearingdevice)

##### Streaming status

- [static func streamingEar() -> AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/streamingear())
- [AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear)

###### Constants

- [static var both: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/both)
- [static var left: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/left)
- [static var right: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/right)

###### Initializer

- [init(rawValue: UInt)](/documentation/accessibility/axmfihearingdevice/ear/init(rawvalue:))
- [static let streamingEarDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/streamingeardidchangenotification)

##### Streaming type

- [static func supportsBidirectionalStreaming() -> Bool](/documentation/accessibility/axmfihearingdevice/supportsbidirectionalstreaming())

##### Paired hearing devices

- [static func pairedDeviceIdentifiers() -> [UUID]](/documentation/accessibility/axmfihearingdevice/paireddeviceidentifiers())
- [static let pairedUUIDsDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/paireduuidsdidchangenotification)

#### Streaming status

- [AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear)

##### Constants

- [static var both: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/both)
- [static var left: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/left)
- [static var right: AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/ear/right)

##### Initializer

- [init(rawValue: UInt)](/documentation/accessibility/axmfihearingdevice/ear/init(rawvalue:))
- [static func streamingEar() -> AXMFiHearingDevice.Ear](/documentation/accessibility/axmfihearingdevice/streamingear())
- [static let streamingEarDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/streamingeardidchangenotification)

#### Streaming type

- [static func supportsBidirectionalStreaming() -> Bool](/documentation/accessibility/axmfihearingdevice/supportsbidirectionalstreaming())

#### Paired hearing devices

- [static func pairedDeviceIdentifiers() -> [UUID]](/documentation/accessibility/axmfihearingdevice/paireddeviceidentifiers())
- [static let pairedUUIDsDidChangeNotification: NSNotification.Name](/documentation/accessibility/axmfihearingdevice/paireduuidsdidchangenotification)
- [func AXNameFromColor(CGColor) -> String](/documentation/accessibility/axnamefromcolor(_:))

### Braille

- [Braille displays](/documentation/accessibility/braille-displays)

#### Braille maps

- [AXBrailleMap](/documentation/accessibility/axbraillemap)

##### Creating a braille map

- [init?(coder: NSCoder)](/documentation/accessibility/axbraillemap/init(coder:))

##### Getting display dimensions

- [var dimensions: CGSize](/documentation/accessibility/axbraillemap/dimensions)

##### Accessing dots

- [func setHeight(Float, at: CGPoint)](/documentation/accessibility/axbraillemap/setheight(_:at:))
- [func height(at: CGPoint) -> Float](/documentation/accessibility/axbraillemap/height(at:))
- [subscript(CGPoint) -> Float](/documentation/accessibility/axbraillemap/subscript(_:))

##### Displaying images

- [func present(CGImage)](/documentation/accessibility/axbraillemap/present(_:))
- [AXBrailleMapRenderer](/documentation/accessibility/axbraillemaprenderer)

##### Rendering a specific region

- [var accessibilityBrailleMapRenderRegion: CGRect](/documentation/accessibility/axbraillemaprenderer/accessibilitybraillemaprenderregion)

##### Updating the braille map manually

- [var accessibilityBrailleMapRenderer: (AXBrailleMap) -> Void](/documentation/accessibility/axbraillemaprenderer/accessibilitybraillemaprenderer)
- [AXBrailleTable](/documentation/accessibility/axbrailletable)

#### Initializers

- [init?(identifier: String)](/documentation/accessibility/axbrailletable/init(identifier:))

#### Instance Properties

- [var identifier: String](/documentation/accessibility/axbrailletable/identifier)
- [var isEightDot: Bool](/documentation/accessibility/axbrailletable/iseightdot)
- [var language: Locale.Language](/documentation/accessibility/axbrailletable/language-3stsd)
- [var locales: Set<Locale>](/documentation/accessibility/axbrailletable/locales)
- [var localizedName: String](/documentation/accessibility/axbrailletable/localizedname)
- [var localizedProviderName: String](/documentation/accessibility/axbrailletable/localizedprovidername)
- [var providerIdentifier: String](/documentation/accessibility/axbrailletable/provideridentifier)

#### Type Methods

- [class func defaultTable(for: Locale) -> AXBrailleTable?](/documentation/accessibility/axbrailletable/defaulttable(for:))
- [class func languageAgnosticTables() -> Set<AXBrailleTable>](/documentation/accessibility/axbrailletable/languageagnostictables())
- [class func supportedLocales() -> Set<Locale>](/documentation/accessibility/axbrailletable/supportedlocales())
- [class func tables(for: Locale) -> Set<AXBrailleTable>](/documentation/accessibility/axbrailletable/tables(for:))
- [AXBrailleTranslator](/documentation/accessibility/axbrailletranslator)

#### Initializers

- [init(brailleTable: AXBrailleTable)](/documentation/accessibility/axbrailletranslator/init(brailletable:))

#### Instance Methods

- [func backTranslateBraille(String) -> AXBrailleTranslationResult](/documentation/accessibility/axbrailletranslator/backtranslatebraille(_:))
- [func translatePrintText(String) -> AXBrailleTranslationResult](/documentation/accessibility/axbrailletranslator/translateprinttext(_:))
- [AXBrailleTranslationResult](/documentation/accessibility/axbrailletranslationresult)

#### Instance Properties

- [var resultString: String](/documentation/accessibility/axbrailletranslationresult/resultstring)

#### Instance Methods

- [func inputIndex(forResultIndex: String.Index) -> String.Index?](/documentation/accessibility/axbrailletranslationresult/inputindex(forresultindex:))

### Math expressions

- [AXMathExpressionNumber](/documentation/accessibility/axmathexpressionnumber)

#### Initializers

- [init(content: String)](/documentation/accessibility/axmathexpressionnumber/init(content:))

#### Instance Properties

- [var content: String](/documentation/accessibility/axmathexpressionnumber/content)
- [AXMathExpressionIdentifier](/documentation/accessibility/axmathexpressionidentifier)

#### Initializers

- [init(content: String)](/documentation/accessibility/axmathexpressionidentifier/init(content:))

#### Instance Properties

- [var content: String](/documentation/accessibility/axmathexpressionidentifier/content)
- [AXMathExpressionOperator](/documentation/accessibility/axmathexpressionoperator)

#### Initializers

- [init(content: String)](/documentation/accessibility/axmathexpressionoperator/init(content:))

#### Instance Properties

- [var content: String](/documentation/accessibility/axmathexpressionoperator/content)
- [AXMathExpressionText](/documentation/accessibility/axmathexpressiontext)

#### Initializers

- [init(content: String)](/documentation/accessibility/axmathexpressiontext/init(content:))

#### Instance Properties

- [var content: String](/documentation/accessibility/axmathexpressiontext/content)
- [AXMathExpressionFenced](/documentation/accessibility/axmathexpressionfenced)

#### Initializers

- [init(expressions: [AXMathExpression], open: String, close: String)](/documentation/accessibility/axmathexpressionfenced/init(expressions:open:close:))

#### Instance Properties

- [var closeString: String](/documentation/accessibility/axmathexpressionfenced/closestring)
- [var expressions: [AXMathExpression]](/documentation/accessibility/axmathexpressionfenced/expressions)
- [var openString: String](/documentation/accessibility/axmathexpressionfenced/openstring)
- [AXMathExpressionRow](/documentation/accessibility/axmathexpressionrow)

#### Initializers

- [init(expressions: [AXMathExpression])](/documentation/accessibility/axmathexpressionrow/init(expressions:))

#### Instance Properties

- [var expressions: [AXMathExpression]](/documentation/accessibility/axmathexpressionrow/expressions)
- [AXMathExpressionTable](/documentation/accessibility/axmathexpressiontable)

#### Initializers

- [init(expressions: [AXMathExpression])](/documentation/accessibility/axmathexpressiontable/init(expressions:))

#### Instance Properties

- [var expressions: [AXMathExpression]](/documentation/accessibility/axmathexpressiontable/expressions)
- [AXMathExpressionTableCell](/documentation/accessibility/axmathexpressiontablecell)

#### Initializers

- [init(expressions: [AXMathExpression])](/documentation/accessibility/axmathexpressiontablecell/init(expressions:))

#### Instance Properties

- [var expressions: [AXMathExpression]](/documentation/accessibility/axmathexpressiontablecell/expressions)
- [AXMathExpressionTableRow](/documentation/accessibility/axmathexpressiontablerow)

#### Initializers

- [init(expressions: [AXMathExpression])](/documentation/accessibility/axmathexpressiontablerow/init(expressions:))

#### Instance Properties

- [var expressions: [AXMathExpression]](/documentation/accessibility/axmathexpressiontablerow/expressions)
- [AXMathExpressionUnderOver](/documentation/accessibility/axmathexpressionunderover)

#### Initializers

- [init(baseExpression: AXMathExpression, underExpression: AXMathExpression, overExpression: AXMathExpression)](/documentation/accessibility/axmathexpressionunderover/init(baseexpression:underexpression:overexpression:))

#### Instance Properties

- [var baseExpression: AXMathExpression](/documentation/accessibility/axmathexpressionunderover/baseexpression)
- [var overExpression: AXMathExpression](/documentation/accessibility/axmathexpressionunderover/overexpression)
- [var underExpression: AXMathExpression](/documentation/accessibility/axmathexpressionunderover/underexpression)
- [AXMathExpressionSubSuperscript](/documentation/accessibility/axmathexpressionsubsuperscript)

#### Initializers

- [init(baseExpression: [AXMathExpression], subscriptExpressions: [AXMathExpression], superscriptExpressions: [AXMathExpression])](/documentation/accessibility/axmathexpressionsubsuperscript/init(baseexpression:subscriptexpressions:superscriptexpressions:))

#### Instance Properties

- [var baseExpression: AXMathExpression](/documentation/accessibility/axmathexpressionsubsuperscript/baseexpression)
- [var subscriptExpressions: [AXMathExpression]](/documentation/accessibility/axmathexpressionsubsuperscript/subscriptexpressions)
- [var superscriptExpressions: [AXMathExpression]](/documentation/accessibility/axmathexpressionsubsuperscript/superscriptexpressions)
- [AXMathExpressionFraction](/documentation/accessibility/axmathexpressionfraction)

#### Initializers

- [init(numeratorExpression: AXMathExpression, denimonatorExpression: AXMathExpression)](/documentation/accessibility/axmathexpressionfraction/init(numeratorexpression:denimonatorexpression:))

#### Instance Properties

- [var denimonatorExpression: AXMathExpression](/documentation/accessibility/axmathexpressionfraction/denimonatorexpression)
- [var numeratorExpression: AXMathExpression](/documentation/accessibility/axmathexpressionfraction/numeratorexpression)
- [AXMathExpressionMultiscript](/documentation/accessibility/axmathexpressionmultiscript)

#### Initializers

- [init(baseExpression: AXMathExpression, prescriptExpressions: [AXMathExpressionSubSuperscript], postscriptExpressions: [AXMathExpressionSubSuperscript])](/documentation/accessibility/axmathexpressionmultiscript/init(baseexpression:prescriptexpressions:postscriptexpressions:))

#### Instance Properties

- [var baseExpression: AXMathExpression](/documentation/accessibility/axmathexpressionmultiscript/baseexpression)
- [var postscriptExpressions: [AXMathExpressionSubSuperscript]](/documentation/accessibility/axmathexpressionmultiscript/postscriptexpressions)
- [var prescriptExpressions: [AXMathExpressionSubSuperscript]](/documentation/accessibility/axmathexpressionmultiscript/prescriptexpressions)
- [AXMathExpressionRoot](/documentation/accessibility/axmathexpressionroot)

#### Initializers

- [init(radicandExpressions: [AXMathExpression], rootIndexExpression: AXMathExpression)](/documentation/accessibility/axmathexpressionroot/init(radicandexpressions:rootindexexpression:))

#### Instance Properties

- [var radicandExpressions: [AXMathExpression]](/documentation/accessibility/axmathexpressionroot/radicandexpressions)
- [var rootIndexExpression: AXMathExpression](/documentation/accessibility/axmathexpressionroot/rootindexexpression)
- [AXMathExpression](/documentation/accessibility/axmathexpression)
- [AXMathExpressionProvider](/documentation/accessibility/axmathexpressionprovider)

#### Instance Methods

- [func accessibilityMathExpression() -> AXMathExpression?](/documentation/accessibility/axmathexpressionprovider/accessibilitymathexpression())

### Override sessions

- [AXFeatureOverrideSession](/documentation/accessibility/axfeatureoverridesession)
- [AXFeatureOverrideSessionManager](/documentation/accessibility/axfeatureoverridesessionmanager)

#### Instance Methods

- [func beginOverrideSession(enabling: AXFeatureOverrideSession.Options, disabling: AXFeatureOverrideSession.Options) throws -> AXFeatureOverrideSession](/documentation/accessibility/axfeatureoverridesessionmanager/beginoverridesession(enabling:disabling:))
- [func end(AXFeatureOverrideSession) throws](/documentation/accessibility/axfeatureoverridesessionmanager/end(_:))

#### Type Properties

- [class var sharedInstance: AXFeatureOverrideSessionManager](/documentation/accessibility/axfeatureoverridesessionmanager/sharedinstance)
- [AXFeatureOverrideSession.Options](/documentation/accessibility/axfeatureoverridesession/options)

#### Initializers

- [init(rawValue: UInt)](/documentation/accessibility/axfeatureoverridesession/options/init(rawvalue:))

#### Type Properties

- [static var grayscale: AXFeatureOverrideSession.Options](/documentation/accessibility/axfeatureoverridesession/options/grayscale)
- [static var invertColors: AXFeatureOverrideSession.Options](/documentation/accessibility/axfeatureoverridesession/options/invertcolors)
- [static var voiceControl: AXFeatureOverrideSession.Options](/documentation/accessibility/axfeatureoverridesession/options/voicecontrol)
- [static var voiceOver: AXFeatureOverrideSession.Options](/documentation/accessibility/axfeatureoverridesession/options/voiceover)
- [static var zoom: AXFeatureOverrideSession.Options](/documentation/accessibility/axfeatureoverridesession/options/zoom)
- [let AXFeatureOverrideSessionErrorDomain: String](/documentation/accessibility/axfeatureoverridesessionerrordomain)
- [AXFeatureOverrideSessionError](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct)

#### Type Properties

- [static var appNotEntitled: AXFeatureOverrideSessionError.Code](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/appnotentitled)
- [static var errorDomain: String](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/errordomain)
- [static var overrideIsAlreadyActive: AXFeatureOverrideSessionError.Code](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/overrideisalreadyactive)
- [static var overrideNotFoundForUUID: AXFeatureOverrideSessionError.Code](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/overridenotfoundforuuid)
- [static var undefined: AXFeatureOverrideSessionError.Code](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/undefined)
- [AXFeatureOverrideSessionError.Code](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/code)

#### Enumeration Cases

- [case appNotEntitled](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/code/appnotentitled)
- [case overrideIsAlreadyActive](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/code/overrideisalreadyactive)
- [case overrideNotFoundForUUID](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/code/overridenotfoundforuuid)
- [case undefined](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/code/undefined)

#### Initializers

- [init?(rawValue: Int)](/documentation/accessibility/axfeatureoverridesessionerror-swift.struct/code/init(rawvalue:))
- [com.apple.developer.accessibility.merchant-api-control](/documentation/bundleresources/entitlements/com.apple.developer.accessibility.merchant-api-control)

### Deprecated

- [func AXAnimatedImagesEnabled() -> Bool](/documentation/accessibility/axanimatedimagesenabled())
- [func AXPrefersHeadAnchorAlternative() -> Bool](/documentation/accessibility/axprefersheadanchoralternative())
- [func AXPrefersHorizontalTextLayout() -> Bool](/documentation/accessibility/axprefershorizontaltextlayout())

## Platforms

- [Accessibility fundamentals](/documentation/swiftui/accessibility-fundamentals)
- [Accessibility for UIKit](/documentation/uikit/accessibility-for-uikit)
- [Accessibility for AppKit](/documentation/appkit/accessibility-for-appkit)
- [Accessibility for visionOS](/documentation/accessibility/accessibility-for-visionos)

### Design

- [Improving accessibility support in your visionOS app](/documentation/visionos/improving-accessibility-support-in-your-app)

### Head-anchored content

- [static var prefersHeadAnchorAlternative: Bool](/documentation/accessibility/accessibilitysettings/prefersheadanchoralternative)
- [static var prefersHeadAnchorAlternativeDidChangeNotification: Notification.Name](/documentation/accessibility/accessibilitysettings/prefersheadanchoralternativedidchangenotification)

## WWDC Challenges

- [WWDC22 Challenge: Learn Switch Control through gaming](/documentation/accessibility/wwdc22_challenge_learn_switch_control_through_gaming)
- [WWDC21 Challenge: Large Text Challenge](/documentation/accessibility/wwdc21_challenge_large_text_challenge)
- [WWDC21 Challenge: Speech Synthesizer Simulator](/documentation/accessibility/wwdc21_challenge_speech_synthesizer_simulator)
- [WWDC21 Challenge: VoiceOver Maze](/documentation/accessibility/wwdc21_challenge_voiceover_maze)

## Resources

- [Specifications](/documentation/accessibility/specifications)

### Human Interface Device (HID)

- [Brain-computer interface HID reference for connecting to Apple platforms](/documentation/accessibility/brain-computer-interface-hid-reference-for-connecting-to-apple-platforms)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
