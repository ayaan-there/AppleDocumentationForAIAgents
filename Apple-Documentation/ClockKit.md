# ClockKit Documentation

Source: https://sosumi.ai/documentation/clockkit

---
title: ClockKit
source: https://developer.apple.com/documentation/clockkit
timestamp: 2026-02-13T18:54:53.630Z
---

## Migration Support

- [Migrating ClockKit complications to WidgetKit](/documentation/widgetkit/converting-a-clockkit-app)
- [CLKComplicationDataSource](/documentation/clockkit/clkcomplicationdatasource)

### Migrating to WidgetKit

- [var widgetMigrator: any CLKComplicationWidgetMigrator](/documentation/clockkit/clkcomplicationdatasource/widgetmigrator)
- [CLKComplicationStaticWidgetMigrationConfiguration](/documentation/clockkit/clkcomplicationstaticwidgetmigrationconfiguration)

#### Creating static complication configurations

- [init(kind: String, extensionBundleIdentifier: String)](/documentation/clockkit/clkcomplicationstaticwidgetmigrationconfiguration/init(kind:extensionbundleidentifier:))

#### Accessing configuration properties

- [var kind: String](/documentation/clockkit/clkcomplicationstaticwidgetmigrationconfiguration/kind)
- [var extensionBundleIdentifier: String](/documentation/clockkit/clkcomplicationstaticwidgetmigrationconfiguration/extensionbundleidentifier)
- [CLKComplicationAppIntentWidgetMigrationConfiguration](/documentation/clockkit/clkcomplicationappintentwidgetmigrationconfiguration)

#### Creating configurations

- [init(kind: String, extensionBundleIdentifier: String, intent: Intent, localizedDisplayName: String)](/documentation/clockkit/clkcomplicationappintentwidgetmigrationconfiguration/init(kind:extensionbundleidentifier:intent:localizeddisplayname:))

#### Accessing configuration properties

- [let kind: String](/documentation/clockkit/clkcomplicationappintentwidgetmigrationconfiguration/kind)
- [let extensionBundleIdentifier: String](/documentation/clockkit/clkcomplicationappintentwidgetmigrationconfiguration/extensionbundleidentifier)
- [let intent: Intent](/documentation/clockkit/clkcomplicationappintentwidgetmigrationconfiguration/intent)
- [let localizedDisplayName: String](/documentation/clockkit/clkcomplicationappintentwidgetmigrationconfiguration/localizeddisplayname)

#### Initializers

- [init?(coder: NSCoder)](/documentation/clockkit/clkcomplicationappintentwidgetmigrationconfiguration/init(coder:))
- [CLKComplicationIntentWidgetMigrationConfiguration](/documentation/clockkit/clkcomplicationintentwidgetmigrationconfiguration)

#### Creating Intent widget configurations

- [init(kind: String, extensionBundleIdentifier: String, intent: INIntent, localizedDisplayName: String)](/documentation/clockkit/clkcomplicationintentwidgetmigrationconfiguration/init(kind:extensionbundleidentifier:intent:localizeddisplayname:))

#### Accessing configuration properties

- [var kind: String](/documentation/clockkit/clkcomplicationintentwidgetmigrationconfiguration/kind)
- [var extensionBundleIdentifier: String](/documentation/clockkit/clkcomplicationintentwidgetmigrationconfiguration/extensionbundleidentifier)
- [var intent: INIntent](/documentation/clockkit/clkcomplicationintentwidgetmigrationconfiguration/intent)
- [var localizedDisplayName: String](/documentation/clockkit/clkcomplicationintentwidgetmigrationconfiguration/localizeddisplayname)
- [CLKComplicationWidgetMigrator](/documentation/clockkit/clkcomplicationwidgetmigrator)

#### Migrating complications

- [func getWidgetConfiguration(from: CLKComplicationDescriptor, completionHandler: (CLKComplicationWidgetMigrationConfiguration?) -> Void)](/documentation/clockkit/clkcomplicationwidgetmigrator/getwidgetconfiguration(from:completionhandler:))
- [CLKComplicationWidgetMigrationConfiguration](/documentation/clockkit/clkcomplicationwidgetmigrationconfiguration)

### Setting information property keys

- [CLKComplicationPrincipalClass](/documentation/bundleresources/information-property-list/clkcomplicationprincipalclass)

### Deprecated methods

- [let CLKLaunchedTimelineEntryDateKey: String](/documentation/clockkit/clklaunchedtimelineentrydatekey)
- [let CLKLaunchedComplicationIdentifierKey: String](/documentation/clockkit/clklaunchedcomplicationidentifierkey)
- [func getComplicationDescriptors(handler: ([CLKComplicationDescriptor]) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getcomplicationdescriptors(handler:))
- [func handleSharedComplicationDescriptors([CLKComplicationDescriptor])](/documentation/clockkit/clkcomplicationdatasource/handlesharedcomplicationdescriptors(_:))
- [func getLocalizableSampleTemplate(for: CLKComplication, withHandler: (CLKComplicationTemplate?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getlocalizablesampletemplate(for:withhandler:))
- [func getPrivacyBehavior(for: CLKComplication, withHandler: (CLKComplicationPrivacyBehavior) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getprivacybehavior(for:withhandler:))

#### Privacy Behaviors

- [CLKComplicationPrivacyBehavior](/documentation/clockkit/clkcomplicationprivacybehavior)

##### Constants

- [case showOnLockScreen](/documentation/clockkit/clkcomplicationprivacybehavior/showonlockscreen)
- [case hideOnLockScreen](/documentation/clockkit/clkcomplicationprivacybehavior/hideonlockscreen)

##### Initializers

- [init?(rawValue: UInt)](/documentation/clockkit/clkcomplicationprivacybehavior/init(rawvalue:))
- [CLKComplicationPrivacyBehavior](/documentation/clockkit/clkcomplicationprivacybehavior)

#### Constants

- [case showOnLockScreen](/documentation/clockkit/clkcomplicationprivacybehavior/showonlockscreen)
- [case hideOnLockScreen](/documentation/clockkit/clkcomplicationprivacybehavior/hideonlockscreen)

#### Initializers

- [init?(rawValue: UInt)](/documentation/clockkit/clkcomplicationprivacybehavior/init(rawvalue:))
- [func getAlwaysOnTemplate(for: CLKComplication, withHandler: (CLKComplicationTemplate?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getalwaysontemplate(for:withhandler:))
- [func getTimelineEndDate(for: CLKComplication, withHandler: (Date?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/gettimelineenddate(for:withhandler:))
- [func getCurrentTimelineEntry(for: CLKComplication, withHandler: (CLKComplicationTimelineEntry?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getcurrenttimelineentry(for:withhandler:))
- [func getTimelineEntries(for: CLKComplication, after: Date, limit: Int, withHandler: ([CLKComplicationTimelineEntry]?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/gettimelineentries(for:after:limit:withhandler:))
- [func getTimelineAnimationBehavior(for: CLKComplication, withHandler: (CLKComplicationTimelineAnimationBehavior) -> Void)](/documentation/clockkit/clkcomplicationdatasource/gettimelineanimationbehavior(for:withhandler:))

#### Animation Behaviors

- [CLKComplicationTimelineAnimationBehavior](/documentation/clockkit/clkcomplicationtimelineanimationbehavior)

##### Constants

- [case never](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/never)
- [case grouped](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/grouped)
- [case always](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/always)

##### Initializers

- [init?(rawValue: UInt)](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/init(rawvalue:))
- [CLKComplicationTimelineAnimationBehavior](/documentation/clockkit/clkcomplicationtimelineanimationbehavior)

#### Constants

- [case never](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/never)
- [case grouped](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/grouped)
- [case always](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/always)

#### Initializers

- [init?(rawValue: UInt)](/documentation/clockkit/clkcomplicationtimelineanimationbehavior/init(rawvalue:))
- [func getSupportedTimeTravelDirections(for: CLKComplication, withHandler: (CLKComplicationTimeTravelDirections) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getsupportedtimetraveldirections(for:withhandler:))

#### Time Travel Directions

- [CLKComplicationTimeTravelDirections](/documentation/clockkit/clkcomplicationtimetraveldirections)

##### Constants

- [static var forward: CLKComplicationTimeTravelDirections](/documentation/clockkit/clkcomplicationtimetraveldirections/forward)
- [static var backward: CLKComplicationTimeTravelDirections](/documentation/clockkit/clkcomplicationtimetraveldirections/backward)

##### Initializers

- [init(rawValue: UInt)](/documentation/clockkit/clkcomplicationtimetraveldirections/init(rawvalue:))
- [CLKComplicationTimeTravelDirections](/documentation/clockkit/clkcomplicationtimetraveldirections)

#### Constants

- [static var forward: CLKComplicationTimeTravelDirections](/documentation/clockkit/clkcomplicationtimetraveldirections/forward)
- [static var backward: CLKComplicationTimeTravelDirections](/documentation/clockkit/clkcomplicationtimetraveldirections/backward)

#### Initializers

- [init(rawValue: UInt)](/documentation/clockkit/clkcomplicationtimetraveldirections/init(rawvalue:))
- [func getTimelineStartDate(for: CLKComplication, withHandler: (Date?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/gettimelinestartdate(for:withhandler:))
- [func getTimelineEntries(for: CLKComplication, before: Date, limit: Int, withHandler: ([CLKComplicationTimelineEntry]?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/gettimelineentries(for:before:limit:withhandler:))
- [func getNextRequestedUpdateDate(handler: (Date?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getnextrequestedupdatedate(handler:))
- [func requestedUpdateDidBegin()](/documentation/clockkit/clkcomplicationdatasource/requestedupdatedidbegin())
- [func requestedUpdateBudgetExhausted()](/documentation/clockkit/clkcomplicationdatasource/requestedupdatebudgetexhausted())
- [func getPlaceholderTemplate(for: CLKComplication, withHandler: (CLKComplicationTemplate?) -> Void)](/documentation/clockkit/clkcomplicationdatasource/getplaceholdertemplate(for:withhandler:))
- [let CLKDefaultComplicationIdentifier: String](/documentation/clockkit/clkdefaultcomplicationidentifier)
- [CLKComplicationDescriptor](/documentation/clockkit/clkcomplicationdescriptor)

### Creating descriptors

- [convenience init(identifier: String, displayName: String, supportedFamilies: [CLKComplicationFamily])](/documentation/clockkit/clkcomplicationdescriptor/init(identifier:displayname:supportedfamilies:))
- [convenience init(identifier: String, displayName: String, supportedFamilies: [CLKComplicationFamily], userActivity: NSUserActivity)](/documentation/clockkit/clkcomplicationdescriptor/init(identifier:displayname:supportedfamilies:useractivity:))
- [convenience init(identifier: String, displayName: String, supportedFamilies: [CLKComplicationFamily], userInfo: [AnyHashable : Any])](/documentation/clockkit/clkcomplicationdescriptor/init(identifier:displayname:supportedfamilies:userinfo:))

### Accessing the descriptor’s data

- [var identifier: String](/documentation/clockkit/clkcomplicationdescriptor/identifier)
- [var displayName: String](/documentation/clockkit/clkcomplicationdescriptor/displayname)
- [var supportedFamilies: [CLKComplicationFamily]](/documentation/clockkit/clkcomplicationdescriptor/supportedfamilies-4ckbx)
- [var userActivity: NSUserActivity?](/documentation/clockkit/clkcomplicationdescriptor/useractivity)
- [var userInfo: [AnyHashable : Any]?](/documentation/clockkit/clkcomplicationdescriptor/userinfo)

## Face Sharing

- [Sharing an Apple Watch face](/documentation/clockkit/sharing-an-apple-watch-face)
- [CLKWatchFaceLibrary](/documentation/clockkit/clkwatchfacelibrary)

### Importing a Watch Face

- [func addWatchFace(at: URL, completionHandler: ((any Error)?) -> Void)](/documentation/clockkit/clkwatchfacelibrary/addwatchface(at:completionhandler:))

### Handling Errors

- [class let ErrorDomain: String](/documentation/clockkit/clkwatchfacelibrary/errordomain)
- [CLKWatchFaceLibrary.ErrorCode](/documentation/clockkit/clkwatchfacelibrary/errorcode)

#### Errors

- [case notFileURL](/documentation/clockkit/clkwatchfacelibrary/errorcode/notfileurl)
- [case invalidFile](/documentation/clockkit/clkwatchfacelibrary/errorcode/invalidfile)
- [case permissionDenied](/documentation/clockkit/clkwatchfacelibrary/errorcode/permissiondenied)
- [case faceNotAvailable](/documentation/clockkit/clkwatchfacelibrary/errorcode/facenotavailable)
- [case notFileURL](/documentation/clockkit/clkwatchfacelibrary/errorcode/notfileurl)
- [case invalidFile](/documentation/clockkit/clkwatchfacelibrary/errorcode/invalidfile)
- [case permissionDenied](/documentation/clockkit/clkwatchfacelibrary/errorcode/permissiondenied)
- [case faceNotAvailable](/documentation/clockkit/clkwatchfacelibrary/errorcode/facenotavailable)

#### Enumeration Cases

- [case noURL](/documentation/clockkit/clkwatchfacelibrary/errorcode/nourl)

#### Initializers

- [init?(rawValue: Int)](/documentation/clockkit/clkwatchfacelibrary/errorcode/init(rawvalue:))

## Deprecated

- [Deprecated articles and symbols](/documentation/clockkit/deprecated-articles-and-symbols)

### Articles

- [Creating complications for your watchOS app](/documentation/clockkit/creating-complications-for-your-watchos-app)

#### Configure Complications

- [Enabling Complications for Your watchOS App](/documentation/clockkit/enabling-complications-for-your-watchos-app)
- [Adding Placeholders for Your Complication](/documentation/clockkit/adding-placeholders-for-your-complication)
- [Declaring complications for your app](/documentation/clockkit/declaring-complications-for-your-app)
- [Creating a timeline entry](/documentation/clockkit/creating-a-timeline-entry)
- [Loading future timeline events](/documentation/clockkit/loading-future-timeline-events)
- [Keeping your complications up to date](/documentation/clockkit/keeping-your-complications-up-to-date)
- [Building complications with SwiftUI](/documentation/clockkit/building-complications-with-swiftui)
- [Displaying progress views and gauges](/documentation/clockkit/displaying-progress-views-and-gauges)
- [Adding text to a complication](/documentation/clockkit/adding-text-to-a-complication)

### Other Symbols

- [CLKComplicationServer](/documentation/clockkit/clkcomplicationserver)

#### Getting the Complication Server

- [class func sharedInstance() -> Self](/documentation/clockkit/clkcomplicationserver/sharedinstance())

#### Getting the Active Complications

- [var activeComplications: [CLKComplication]?](/documentation/clockkit/clkcomplicationserver/activecomplications)

#### Updating Your Timeline Data

- [func reloadTimeline(for: CLKComplication)](/documentation/clockkit/clkcomplicationserver/reloadtimeline(for:))
- [func extendTimeline(for: CLKComplication)](/documentation/clockkit/clkcomplicationserver/extendtimeline(for:))

#### Updating Complication Types

- [func reloadComplicationDescriptors()](/documentation/clockkit/clkcomplicationserver/reloadcomplicationdescriptors())

#### Getting the Time Travel Boundaries

- [var earliestTimeTravelDate: Date](/documentation/clockkit/clkcomplicationserver/earliesttimetraveldate)
- [var latestTimeTravelDate: Date](/documentation/clockkit/clkcomplicationserver/latesttimetraveldate)
- [CLKComplication](/documentation/clockkit/clkcomplication)

#### Accessing Data About the Complication

- [var family: CLKComplicationFamily](/documentation/clockkit/clkcomplication/family)
- [var identifier: String](/documentation/clockkit/clkcomplication/identifier)
- [var userActivity: NSUserActivity?](/documentation/clockkit/clkcomplication/useractivity)
- [var userInfo: [AnyHashable : Any]?](/documentation/clockkit/clkcomplication/userinfo)
- [CLKComplicationTimelineEntry](/documentation/clockkit/clkcomplicationtimelineentry)

#### Creating a Timeline Entry

- [convenience init(date: Date, complicationTemplate: CLKComplicationTemplate)](/documentation/clockkit/clkcomplicationtimelineentry/init(date:complicationtemplate:))
- [convenience init(date: Date, complicationTemplate: CLKComplicationTemplate, timelineAnimationGroup: String?)](/documentation/clockkit/clkcomplicationtimelineentry/init(date:complicationtemplate:timelineanimationgroup:))

#### Setting the Entry Values

- [var date: Date](/documentation/clockkit/clkcomplicationtimelineentry/date)
- [var complicationTemplate: CLKComplicationTemplate](/documentation/clockkit/clkcomplicationtimelineentry/complicationtemplate)
- [var timelineAnimationGroup: String?](/documentation/clockkit/clkcomplicationtimelineentry/timelineanimationgroup)

### Sample Code

- [Providing Multiple Complications](/documentation/clockkit/providing-multiple-complications)
- [Creating and updating a complication’s timeline](/documentation/clockkit/creating-and-updating-a-complication-s-timeline)

### Templates

- [SwiftUI templates](/documentation/clockkit/swiftui-templates)

#### Corner templates

- [CLKComplicationTemplateGraphicCornerCircularView](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularview)

##### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularview/init(_:))

##### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularview/content)
- [CLKComplicationTemplateGraphicCornerGaugeView](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview)

##### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, leadingTextProvider: CLKTextProvider?, trailingTextProvider: CLKTextProvider?, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/init(gaugeprovider:leadingtextprovider:trailingtextprovider:label:))

##### Accessing the Content

- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/label)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/gaugeprovider)
- [var leadingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/leadingtextprovider)
- [var trailingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/trailingtextprovider)
- [CLKComplicationTemplateGraphicCornerTextView](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview)

##### Creating the Template

- [init(textProvider: CLKTextProvider, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview/init(textprovider:label:))

##### Accessing the Content

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview/textprovider)
- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview/label)

#### Circular templates

- [CLKComplicationTemplateGraphicCircularView](/documentation/clockkit/clkcomplicationtemplategraphiccircularview)

##### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphiccircularview/init(_:))

##### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphiccircularview/content)
- [CLKComplicationTemplateGraphicCircularOpenGaugeView](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview)

##### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, centerTextProvider: CLKTextProvider, bottomLabel: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/init(gaugeprovider:centertextprovider:bottomlabel:))

##### Accesing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/gaugeprovider)
- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/centertextprovider)
- [var bottomLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/bottomlabel)
- [CLKComplicationTemplateGraphicCircularClosedGaugeView](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview)

##### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview/init(gaugeprovider:label:))

##### Accessing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview/gaugeprovider)
- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview/label)
- [CLKComplicationTemplateGraphicCircularStackViewText](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext)

##### Creating the Template

- [init(content: Content, textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext/init(content:textprovider:))

##### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext/content)
- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext/textprovider)

#### Rectangular templates

- [CLKComplicationTemplateGraphicRectangularStandardBodyView](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview)

##### Creating the Template

- [init(headerLabel: Label, headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, body2TextProvider: CLKTextProvider?)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/init(headerlabel:headertextprovider:body1textprovider:body2textprovider:))

##### Accessing the Content

- [var headerLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/headerlabel)
- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/headertextprovider)
- [var body1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/body1textprovider)
- [var body2TextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/body2textprovider)
- [CLKComplicationTemplateGraphicRectangularTextGaugeView](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview)

##### Creating the Template

- [init(headerLabel: Label, headerTextProvider: CLKTextProvider, bodyTextProvider: CLKTextProvider, gaugeProvider: CLKGaugeProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/init(headerlabel:headertextprovider:bodytextprovider:gaugeprovider:))

##### Accessing the Content

- [var headerLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/headerlabel)
- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/headertextprovider)
- [var bodyTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/bodytextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/gaugeprovider)
- [CLKComplicationTemplateGraphicRectangularLargeView](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview)

##### Creating the Template

- [init(headerTextProvider: CLKTextProvider, content: Content)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview/init(headertextprovider:content:))

##### Accessing the Content

- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview/headertextprovider)
- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview/content)
- [CLKComplicationTemplateGraphicRectangularFullView](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullview)

##### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullview/init(_:))

##### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullview/content)

#### Extra large templates

- [CLKComplicationTemplateGraphicExtraLargeCircularView](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularview)

##### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularview/init(_:))

##### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularview/content)
- [CLKComplicationTemplateGraphicExtraLargeCircularOpenGaugeView](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview)

##### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, centerTextProvider: CLKTextProvider, bottomLabel: Label)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/init(gaugeprovider:centertextprovider:bottomlabel:))

##### Accessing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/gaugeprovider)
- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/centertextprovider)
- [var bottomLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/bottomlabel)
- [CLKComplicationTemplateGraphicExtraLargeCircularClosedGaugeView](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview)

##### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview/init(gaugeprovider:label:))

##### Accessing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview/gaugeprovider)
- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview/label)
- [CLKComplicationTemplateGraphicExtraLargeCircularStackViewText](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext)

##### Creating the Template

- [init(content: Content, textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext/init(content:textprovider:))

##### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext/content)
- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext/textprovider)
- [ComplicationRenderingMode](/documentation/clockkit/complicationrenderingmode)

#### Rendering Modes

- [case fullColor](/documentation/clockkit/complicationrenderingmode/fullcolor)
- [case tinted](/documentation/clockkit/complicationrenderingmode/tinted)
- [Data providers](/documentation/clockkit/data-providers)

#### Text providers

- [CLKSimpleTextProvider](/documentation/clockkit/clksimpletextprovider)

##### Creating a Text Provider

- [convenience init(text: String)](/documentation/clockkit/clksimpletextprovider/init(text:))
- [convenience init(text: String, shortText: String?)](/documentation/clockkit/clksimpletextprovider/init(text:shorttext:))
- [convenience init(text: String, shortText: String?, accessibilityLabel: String?)](/documentation/clockkit/clksimpletextprovider/init(text:shorttext:accessibilitylabel:))

##### Getting the Text

- [var text: String](/documentation/clockkit/clksimpletextprovider/text)
- [var shortText: String?](/documentation/clockkit/clksimpletextprovider/shorttext)
- [CLKDateTextProvider](/documentation/clockkit/clkdatetextprovider)

##### Creating a Text Provider

- [convenience init(date: Date, units: NSCalendar.Unit)](/documentation/clockkit/clkdatetextprovider/init(date:units:))
- [convenience init(date: Date, units: NSCalendar.Unit, timeZone: TimeZone?)](/documentation/clockkit/clkdatetextprovider/init(date:units:timezone:))

##### Getting the Date Information

- [var date: Date](/documentation/clockkit/clkdatetextprovider/date)
- [var timeZone: TimeZone?](/documentation/clockkit/clkdatetextprovider/timezone)
- [var calendarUnits: NSCalendar.Unit](/documentation/clockkit/clkdatetextprovider/calendarunits)
- [var uppercase: Bool](/documentation/clockkit/clkdatetextprovider/uppercase)
- [CLKRelativeDateTextProvider](/documentation/clockkit/clkrelativedatetextprovider)

##### Creating a Text Provider

- [convenience init(date: Date, style: CLKRelativeDateStyle, units: NSCalendar.Unit)](/documentation/clockkit/clkrelativedatetextprovider/init(date:style:units:))
- [convenience init(date: Date, relativeTo: Date?, style: CLKRelativeDateStyle, units: NSCalendar.Unit)](/documentation/clockkit/clkrelativedatetextprovider/init(date:relativeto:style:units:))

##### Getting the Date Information

- [var date: Date](/documentation/clockkit/clkrelativedatetextprovider/date)
- [var relativeToDate: Date?](/documentation/clockkit/clkrelativedatetextprovider/relativetodate)
- [var relativeDateStyle: CLKRelativeDateStyle](/documentation/clockkit/clkrelativedatetextprovider/relativedatestyle)
- [var calendarUnits: NSCalendar.Unit](/documentation/clockkit/clkrelativedatetextprovider/calendarunits)

##### Constants

- [CLKRelativeDateStyle](/documentation/clockkit/clkrelativedatestyle)

###### Date Styles

- [case natural](/documentation/clockkit/clkrelativedatestyle/natural)
- [case naturalAbbreviated](/documentation/clockkit/clkrelativedatestyle/naturalabbreviated)
- [case naturalFull](/documentation/clockkit/clkrelativedatestyle/naturalfull)
- [case offset](/documentation/clockkit/clkrelativedatestyle/offset)
- [case offsetShort](/documentation/clockkit/clkrelativedatestyle/offsetshort)
- [case timer](/documentation/clockkit/clkrelativedatestyle/timer)

###### Initializers

- [init?(rawValue: Int)](/documentation/clockkit/clkrelativedatestyle/init(rawvalue:))
- [CLKTimeIntervalTextProvider](/documentation/clockkit/clktimeintervaltextprovider)

##### Creating the Text Provider

- [convenience init(start: Date, end: Date)](/documentation/clockkit/clktimeintervaltextprovider/init(start:end:))
- [convenience init(start: Date, end: Date, timeZone: TimeZone?)](/documentation/clockkit/clktimeintervaltextprovider/init(start:end:timezone:))

##### Getting the Time Information

- [var startDate: Date](/documentation/clockkit/clktimeintervaltextprovider/startdate)
- [var endDate: Date](/documentation/clockkit/clktimeintervaltextprovider/enddate)
- [var timeZone: TimeZone?](/documentation/clockkit/clktimeintervaltextprovider/timezone)
- [CLKTimeTextProvider](/documentation/clockkit/clktimetextprovider)

##### Creating a Text Provider

- [convenience init(date: Date)](/documentation/clockkit/clktimetextprovider/init(date:))
- [convenience init(date: Date, timeZone: TimeZone?)](/documentation/clockkit/clktimetextprovider/init(date:timezone:))

##### Getting the Time Information

- [var date: Date](/documentation/clockkit/clktimetextprovider/date)
- [var timeZone: TimeZone?](/documentation/clockkit/clktimetextprovider/timezone)
- [CLKTextProvider](/documentation/clockkit/clktextprovider)

##### Creating a Compound Text Provider

- [convenience init(format: String, any CVarArg...)](/documentation/clockkit/clktextprovider/init(format:_:))

##### Creating Localized Text Providers

- [class func localizableTextProvider(withStringsFileTextKey: String) -> Self](/documentation/clockkit/clktextprovider/localizabletextprovider(withstringsfiletextkey:))
- [class func localizableTextProvider(withStringsFileTextKey: String, shortTextKey: String?) -> Self](/documentation/clockkit/clktextprovider/localizabletextprovider(withstringsfiletextkey:shorttextkey:))
- [class func localizableTextProvider(withStringsFileFormatKey: String, textProviders: [CLKTextProvider]) -> Self](/documentation/clockkit/clktextprovider/localizabletextprovider(withstringsfileformatkey:textproviders:))

##### Setting the Tint Color

- [var tintColor: UIColor](/documentation/clockkit/clktextprovider/tintcolor)

##### Supporting Accessibility

- [var accessibilityLabel: String?](/documentation/clockkit/clktextprovider/accessibilitylabel)

##### Creating Empty Text Providers

- [init()](/documentation/clockkit/clktextprovider/init())
- [class func new() -> Self](/documentation/clockkit/clktextprovider/new())

#### Image providers

- [CLKImageProvider](/documentation/clockkit/clkimageprovider)

##### Creating an Image Provider

- [convenience init(onePieceImage: UIImage)](/documentation/clockkit/clkimageprovider/init(onepieceimage:))
- [convenience init(onePieceImage: UIImage, twoPieceImageBackground: UIImage?, twoPieceImageForeground: UIImage?)](/documentation/clockkit/clkimageprovider/init(onepieceimage:twopieceimagebackground:twopieceimageforeground:))

##### Getting the Image Data

- [var onePieceImage: UIImage](/documentation/clockkit/clkimageprovider/onepieceimage)
- [var tintColor: UIColor?](/documentation/clockkit/clkimageprovider/tintcolor)
- [var twoPieceImageBackground: UIImage?](/documentation/clockkit/clkimageprovider/twopieceimagebackground)
- [var twoPieceImageForeground: UIImage?](/documentation/clockkit/clkimageprovider/twopieceimageforeground)

##### Setting the Accessibility Label

- [var accessibilityLabel: String?](/documentation/clockkit/clkimageprovider/accessibilitylabel)

##### Creating Empty Image Providers

- [class func new() -> Self](/documentation/clockkit/clkimageprovider/new())
- [init()](/documentation/clockkit/clkimageprovider/init())
- [CLKFullColorImageProvider](/documentation/clockkit/clkfullcolorimageprovider)

##### Creating an Image Provider

- [convenience init(fullColorImage: UIImage)](/documentation/clockkit/clkfullcolorimageprovider/init(fullcolorimage:))
- [convenience init(fullColorImage: UIImage, tintedImageProvider: CLKImageProvider?)](/documentation/clockkit/clkfullcolorimageprovider/init(fullcolorimage:tintedimageprovider:))

##### Getting the Image Data

- [var image: UIImage](/documentation/clockkit/clkfullcolorimageprovider/image)
- [var tintedImageProvider: CLKImageProvider?](/documentation/clockkit/clkfullcolorimageprovider/tintedimageprovider)

##### Setting the Accessibility Label

- [var accessibilityLabel: String?](/documentation/clockkit/clkfullcolorimageprovider/accessibilitylabel)

##### Creating Empty Image Providers

- [init()](/documentation/clockkit/clkfullcolorimageprovider/init())
- [class func new() -> Self](/documentation/clockkit/clkfullcolorimageprovider/new())

#### Gauge providers

- [CLKSimpleGaugeProvider](/documentation/clockkit/clksimplegaugeprovider)

##### Creating a Simple Gauge Provider

- [convenience init(style: CLKGaugeProviderStyle, gaugeColor: UIColor, fillFraction: Float)](/documentation/clockkit/clksimplegaugeprovider/init(style:gaugecolor:fillfraction:))
- [convenience init(style: CLKGaugeProviderStyle, gaugeColors: [UIColor]?, gaugeColorLocations: [NSNumber]?, fillFraction: Float)](/documentation/clockkit/clksimplegaugeprovider/init(style:gaugecolors:gaugecolorlocations:fillfraction:))

##### Getting Information About the Gauge

- [var fillFraction: Float](/documentation/clockkit/clksimplegaugeprovider/fillfraction)
- [CLKTimeIntervalGaugeProvider](/documentation/clockkit/clktimeintervalgaugeprovider)

##### Creating a Time Interval Gauge

- [convenience init(style: CLKGaugeProviderStyle, gaugeColors: [UIColor]?, gaugeColorLocations: [NSNumber]?, start: Date, end: Date)](/documentation/clockkit/clktimeintervalgaugeprovider/init(style:gaugecolors:gaugecolorlocations:start:end:))
- [convenience init(style: CLKGaugeProviderStyle, gaugeColors: [UIColor]?, gaugeColorLocations: [NSNumber]?, start: Date, startFillFraction: Float, end: Date, endFillFraction: Float)](/documentation/clockkit/clktimeintervalgaugeprovider/init(style:gaugecolors:gaugecolorlocations:start:startfillfraction:end:endfillfraction:))

##### Getting Information about the Gauge

- [var startDate: Date](/documentation/clockkit/clktimeintervalgaugeprovider/startdate)
- [var endDate: Date](/documentation/clockkit/clktimeintervalgaugeprovider/enddate)
- [var startFillFraction: Float](/documentation/clockkit/clktimeintervalgaugeprovider/startfillfraction)
- [var endFillFraction: Float](/documentation/clockkit/clktimeintervalgaugeprovider/endfillfraction)
- [CLKGaugeProvider](/documentation/clockkit/clkgaugeprovider)

##### Setting the Gauge’s Appearance

- [var gaugeColors: [UIColor]?](/documentation/clockkit/clkgaugeprovider/gaugecolors)
- [var gaugeColorLocations: [NSNumber]?](/documentation/clockkit/clkgaugeprovider/gaugecolorlocations)
- [var style: CLKGaugeProviderStyle](/documentation/clockkit/clkgaugeprovider/style)

##### Adding Accessibility

- [var accessibilityLabel: String?](/documentation/clockkit/clkgaugeprovider/accessibilitylabel)
- [let CLKSimpleGaugeProviderFillFractionEmpty: Float](/documentation/clockkit/clksimplegaugeproviderfillfractionempty)
- [CLKGaugeProviderStyle](/documentation/clockkit/clkgaugeproviderstyle)

##### Styles

- [case fill](/documentation/clockkit/clkgaugeproviderstyle/fill)
- [case ring](/documentation/clockkit/clkgaugeproviderstyle/ring)

##### Initializers

- [init?(rawValue: Int)](/documentation/clockkit/clkgaugeproviderstyle/init(rawvalue:))
- [Circular small](/documentation/clockkit/circular-small)

#### Image templates

- [CLKComplicationTemplateCircularSmallRingImage](/documentation/clockkit/clkcomplicationtemplatecircularsmallringimage)

##### Creating the Template

- [init(imageProvider: CLKImageProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplatecircularsmallringimage/init(imageprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallringimage/imageprovider)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplatecircularsmallringimage/ringstyle)
- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplatecircularsmallringimage/fillfraction)
- [CLKComplicationTemplateCircularSmallSimpleImage](/documentation/clockkit/clkcomplicationtemplatecircularsmallsimpleimage)

##### Creating the Template

- [init(imageProvider: CLKImageProvider)](/documentation/clockkit/clkcomplicationtemplatecircularsmallsimpleimage/init(imageprovider:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallsimpleimage/imageprovider)
- [CLKComplicationTemplateCircularSmallStackImage](/documentation/clockkit/clkcomplicationtemplatecircularsmallstackimage)

##### Creating the Template

- [init(line1ImageProvider: CLKImageProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatecircularsmallstackimage/init(line1imageprovider:line2textprovider:))

##### Setting the Complication Data

- [var line1ImageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallstackimage/line1imageprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallstackimage/line2textprovider)

#### Text templates

- [CLKComplicationTemplateCircularSmallRingText](/documentation/clockkit/clkcomplicationtemplatecircularsmallringtext)

##### Creating the Template

- [init(textProvider: CLKTextProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplatecircularsmallringtext/init(textprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallringtext/textprovider)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplatecircularsmallringtext/ringstyle)
- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplatecircularsmallringtext/fillfraction)
- [CLKComplicationTemplateCircularSmallSimpleText](/documentation/clockkit/clkcomplicationtemplatecircularsmallsimpletext)

##### Creating the Template

- [init(textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatecircularsmallsimpletext/init(textprovider:))

##### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallsimpletext/textprovider)
- [CLKComplicationTemplateCircularSmallStackText](/documentation/clockkit/clkcomplicationtemplatecircularsmallstacktext)

##### Creating the Template

- [init(line1TextProvider: CLKTextProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatecircularsmallstacktext/init(line1textprovider:line2textprovider:))

##### Setting the Complication Data

- [var line1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallstacktext/line1textprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatecircularsmallstacktext/line2textprovider)
- [Extra large](/documentation/clockkit/extra-large)

#### Image templates

- [CLKComplicationTemplateExtraLargeRingImage](/documentation/clockkit/clkcomplicationtemplateextralargeringimage)

##### Creating the Template

- [init(imageProvider: CLKImageProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplateextralargeringimage/init(imageprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplateextralargeringimage/fillfraction)
- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplateextralargeringimage/imageprovider)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplateextralargeringimage/ringstyle)
- [CLKComplicationTemplateExtraLargeSimpleImage](/documentation/clockkit/clkcomplicationtemplateextralargesimpleimage)

##### Creating the Template

- [init(imageProvider: CLKImageProvider)](/documentation/clockkit/clkcomplicationtemplateextralargesimpleimage/init(imageprovider:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplateextralargesimpleimage/imageprovider)
- [CLKComplicationTemplateExtraLargeStackImage](/documentation/clockkit/clkcomplicationtemplateextralargestackimage)

##### Creating the Template

- [init(line1ImageProvider: CLKImageProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplateextralargestackimage/init(line1imageprovider:line2textprovider:))

##### Setting the Complication Data

- [var highlightLine2: Bool](/documentation/clockkit/clkcomplicationtemplateextralargestackimage/highlightline2)
- [var line1ImageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplateextralargestackimage/line1imageprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargestackimage/line2textprovider)

#### Text templates

- [CLKComplicationTemplateExtraLargeColumnsText](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext)

##### Creating the Template

- [init(row1Column1TextProvider: CLKTextProvider, row1Column2TextProvider: CLKTextProvider, row2Column1TextProvider: CLKTextProvider, row2Column2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext/init(row1column1textprovider:row1column2textprovider:row2column1textprovider:row2column2textprovider:))

##### Setting the Complication Data

- [var column2Alignment: CLKComplicationColumnAlignment](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext/column2alignment)
- [var highlightColumn2: Bool](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext/highlightcolumn2)
- [var row1Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext/row1column1textprovider)
- [var row1Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext/row1column2textprovider)
- [var row2Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext/row2column1textprovider)
- [var row2Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargecolumnstext/row2column2textprovider)
- [CLKComplicationTemplateExtraLargeRingText](/documentation/clockkit/clkcomplicationtemplateextralargeringtext)

##### Creating the Template

- [init(textProvider: CLKTextProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplateextralargeringtext/init(textprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplateextralargeringtext/fillfraction)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplateextralargeringtext/ringstyle)
- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargeringtext/textprovider)
- [CLKComplicationTemplateExtraLargeSimpleText](/documentation/clockkit/clkcomplicationtemplateextralargesimpletext)

##### Creating the Template

- [init(textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplateextralargesimpletext/init(textprovider:))

##### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargesimpletext/textprovider)
- [CLKComplicationTemplateExtraLargeStackText](/documentation/clockkit/clkcomplicationtemplateextralargestacktext)

##### Creating the Template

- [init(line1TextProvider: CLKTextProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplateextralargestacktext/init(line1textprovider:line2textprovider:))

##### Setting the Complication Data

- [var highlightLine2: Bool](/documentation/clockkit/clkcomplicationtemplateextralargestacktext/highlightline2)
- [var line1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargestacktext/line1textprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateextralargestacktext/line2textprovider)
- [Modular small](/documentation/clockkit/modular-small)

#### Image templates

- [CLKComplicationTemplateModularSmallRingImage](/documentation/clockkit/clkcomplicationtemplatemodularsmallringimage)

##### Creating the Template

- [init(imageProvider: CLKImageProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplatemodularsmallringimage/init(imageprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallringimage/imageprovider)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplatemodularsmallringimage/ringstyle)
- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplatemodularsmallringimage/fillfraction)
- [CLKComplicationTemplateModularSmallSimpleImage](/documentation/clockkit/clkcomplicationtemplatemodularsmallsimpleimage)

##### Creating the Template

- [init(imageProvider: CLKImageProvider)](/documentation/clockkit/clkcomplicationtemplatemodularsmallsimpleimage/init(imageprovider:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallsimpleimage/imageprovider)
- [CLKComplicationTemplateModularSmallStackImage](/documentation/clockkit/clkcomplicationtemplatemodularsmallstackimage)

##### Creating the Template

- [init(line1ImageProvider: CLKImageProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularsmallstackimage/init(line1imageprovider:line2textprovider:))

##### Setting the Complication Data

- [var line1ImageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallstackimage/line1imageprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallstackimage/line2textprovider)
- [var highlightLine2: Bool](/documentation/clockkit/clkcomplicationtemplatemodularsmallstackimage/highlightline2)

#### Text templates

- [CLKComplicationTemplateModularSmallColumnsText](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext)

##### Creating the Template

- [init(row1Column1TextProvider: CLKTextProvider, row1Column2TextProvider: CLKTextProvider, row2Column1TextProvider: CLKTextProvider, row2Column2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext/init(row1column1textprovider:row1column2textprovider:row2column1textprovider:row2column2textprovider:))

##### Setting the Complication Data

- [var row1Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext/row1column1textprovider)
- [var row1Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext/row1column2textprovider)
- [var row2Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext/row2column1textprovider)
- [var row2Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext/row2column2textprovider)
- [var column2Alignment: CLKComplicationColumnAlignment](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext/column2alignment)
- [var highlightColumn2: Bool](/documentation/clockkit/clkcomplicationtemplatemodularsmallcolumnstext/highlightcolumn2)
- [CLKComplicationTemplateModularSmallRingText](/documentation/clockkit/clkcomplicationtemplatemodularsmallringtext)

##### Creating the Template

- [init(textProvider: CLKTextProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplatemodularsmallringtext/init(textprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallringtext/textprovider)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplatemodularsmallringtext/ringstyle)
- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplatemodularsmallringtext/fillfraction)
- [CLKComplicationTemplateModularSmallSimpleText](/documentation/clockkit/clkcomplicationtemplatemodularsmallsimpletext)

##### Creating the Template

- [init(textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularsmallsimpletext/init(textprovider:))

##### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallsimpletext/textprovider)
- [CLKComplicationTemplateModularSmallStackText](/documentation/clockkit/clkcomplicationtemplatemodularsmallstacktext)

##### Creating the Template

- [init(line1TextProvider: CLKTextProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularsmallstacktext/init(line1textprovider:line2textprovider:))

##### Setting the Complication Data

- [var line1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallstacktext/line1textprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularsmallstacktext/line2textprovider)
- [var highlightLine2: Bool](/documentation/clockkit/clkcomplicationtemplatemodularsmallstacktext/highlightline2)
- [Modular large](/documentation/clockkit/modular-large)

#### Body templates

- [CLKComplicationTemplateModularLargeStandardBody](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody)

##### Creating the Template

- [init(headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/init(headertextprovider:body1textprovider:))
- [init(headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, body2TextProvider: CLKTextProvider?)](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/init(headertextprovider:body1textprovider:body2textprovider:))
- [init(headerImageProvider: CLKImageProvider?, headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/init(headerimageprovider:headertextprovider:body1textprovider:))
- [init(headerImageProvider: CLKImageProvider?, headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, body2TextProvider: CLKTextProvider?)](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/init(headerimageprovider:headertextprovider:body1textprovider:body2textprovider:))

##### Setting the Complication Data

- [var headerImageProvider: CLKImageProvider?](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/headerimageprovider)
- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/headertextprovider)
- [var body1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/body1textprovider)
- [var body2TextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplatemodularlargestandardbody/body2textprovider)
- [CLKComplicationTemplateModularLargeTallBody](/documentation/clockkit/clkcomplicationtemplatemodularlargetallbody)

##### Creating the Template

- [init(headerTextProvider: CLKTextProvider, bodyTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularlargetallbody/init(headertextprovider:bodytextprovider:))

##### Setting the Complication Data

- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargetallbody/headertextprovider)
- [var bodyTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargetallbody/bodytextprovider)

#### Table templates

- [CLKComplicationTemplateModularLargeColumns](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns)

##### Creating the Template

- [init(row1Column1TextProvider: CLKTextProvider, row1Column2TextProvider: CLKTextProvider, row2Column1TextProvider: CLKTextProvider, row2Column2TextProvider: CLKTextProvider, row3Column1TextProvider: CLKTextProvider, row3Column2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/init(row1column1textprovider:row1column2textprovider:row2column1textprovider:row2column2textprovider:row3column1textprovider:row3column2textprovider:))
- [init(row1ImageProvider: CLKImageProvider?, row1Column1TextProvider: CLKTextProvider, row1Column2TextProvider: CLKTextProvider, row2ImageProvider: CLKImageProvider?, row2Column1TextProvider: CLKTextProvider, row2Column2TextProvider: CLKTextProvider, row3ImageProvider: CLKImageProvider?, row3Column1TextProvider: CLKTextProvider, row3Column2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/init(row1imageprovider:row1column1textprovider:row1column2textprovider:row2imageprovider:row2column1textprovider:row2column2textprovider:row3imageprovider:row3column1textprovider:row3column2textprovider:))

##### Setting the Complication Data

- [var row1ImageProvider: CLKImageProvider?](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row1imageprovider)
- [var row1Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row1column1textprovider)
- [var row1Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row1column2textprovider)
- [var row2ImageProvider: CLKImageProvider?](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row2imageprovider)
- [var row2Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row2column1textprovider)
- [var row2Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row2column2textprovider)
- [var row3ImageProvider: CLKImageProvider?](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row3imageprovider)
- [var row3Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row3column1textprovider)
- [var row3Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/row3column2textprovider)
- [var column2Alignment: CLKComplicationColumnAlignment](/documentation/clockkit/clkcomplicationtemplatemodularlargecolumns/column2alignment)
- [CLKComplicationTemplateModularLargeTable](/documentation/clockkit/clkcomplicationtemplatemodularlargetable)

##### Creating the Template

- [init(headerTextProvider: CLKTextProvider, row1Column1TextProvider: CLKTextProvider, row1Column2TextProvider: CLKTextProvider, row2Column1TextProvider: CLKTextProvider, row2Column2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/init(headertextprovider:row1column1textprovider:row1column2textprovider:row2column1textprovider:row2column2textprovider:))
- [init(headerImageProvider: CLKImageProvider?, headerTextProvider: CLKTextProvider, row1Column1TextProvider: CLKTextProvider, row1Column2TextProvider: CLKTextProvider, row2Column1TextProvider: CLKTextProvider, row2Column2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/init(headerimageprovider:headertextprovider:row1column1textprovider:row1column2textprovider:row2column1textprovider:row2column2textprovider:))

##### Setting the Complication Data

- [var headerImageProvider: CLKImageProvider?](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/headerimageprovider)
- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/headertextprovider)
- [var row1Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/row1column1textprovider)
- [var row1Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/row1column2textprovider)
- [var row2Column1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/row2column1textprovider)
- [var row2Column2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/row2column2textprovider)
- [var column2Alignment: CLKComplicationColumnAlignment](/documentation/clockkit/clkcomplicationtemplatemodularlargetable/column2alignment)
- [Utilitarian](/documentation/clockkit/utilitarian)

#### Utilitarian small

- [CLKComplicationTemplateUtilitarianSmallFlat](/documentation/clockkit/clkcomplicationtemplateutilitariansmallflat)

##### Creating the Template

- [init(textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplateutilitariansmallflat/init(textprovider:))
- [init(textProvider: CLKTextProvider, imageProvider: CLKImageProvider?)](/documentation/clockkit/clkcomplicationtemplateutilitariansmallflat/init(textprovider:imageprovider:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider?](/documentation/clockkit/clkcomplicationtemplateutilitariansmallflat/imageprovider)
- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateutilitariansmallflat/textprovider)
- [CLKComplicationTemplateUtilitarianSmallRingImage](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringimage)

##### Creating the Template

- [init(imageProvider: CLKImageProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringimage/init(imageprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringimage/imageprovider)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringimage/ringstyle)
- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringimage/fillfraction)
- [CLKComplicationTemplateUtilitarianSmallRingText](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringtext)

##### Creating the Template

- [init(textProvider: CLKTextProvider, fillFraction: Float, ringStyle: CLKComplicationRingStyle)](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringtext/init(textprovider:fillfraction:ringstyle:))

##### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringtext/textprovider)
- [var ringStyle: CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringtext/ringstyle)
- [var fillFraction: Float](/documentation/clockkit/clkcomplicationtemplateutilitariansmallringtext/fillfraction)
- [CLKComplicationTemplateUtilitarianSmallSquare](/documentation/clockkit/clkcomplicationtemplateutilitariansmallsquare)

##### Creating the Template

- [init(imageProvider: CLKImageProvider)](/documentation/clockkit/clkcomplicationtemplateutilitariansmallsquare/init(imageprovider:))

##### Setting the Complication Data

- [var imageProvider: CLKImageProvider](/documentation/clockkit/clkcomplicationtemplateutilitariansmallsquare/imageprovider)

#### Utilitarian large

- [CLKComplicationTemplateUtilitarianLargeFlat](/documentation/clockkit/clkcomplicationtemplateutilitarianlargeflat)

##### Creating the Template

- [init(textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplateutilitarianlargeflat/init(textprovider:))
- [init(textProvider: CLKTextProvider, imageProvider: CLKImageProvider?)](/documentation/clockkit/clkcomplicationtemplateutilitarianlargeflat/init(textprovider:imageprovider:))

##### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplateutilitarianlargeflat/textprovider)
- [var imageProvider: CLKImageProvider?](/documentation/clockkit/clkcomplicationtemplateutilitarianlargeflat/imageprovider)
- [Graphic](/documentation/clockkit/graphic)

#### Graphic data

- [Displaying essential information on a watch face](/documentation/clockkit/displaying-essential-information-on-a-watch-face)

#### Graphic template families

- [Circular complication templates](/documentation/clockkit/circular-complication-templates)

##### Text and images

- [CLKComplicationTemplateGraphicCircularImage](/documentation/clockkit/clkcomplicationtemplategraphiccircularimage)

###### Creating the Template

- [init(imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularimage/init(imageprovider:))

###### Setting the Complication Data

- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularimage/imageprovider)
- [CLKComplicationTemplateGraphicCircularView](/documentation/clockkit/clkcomplicationtemplategraphiccircularview)

###### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphiccircularview/init(_:))

###### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphiccircularview/content)
- [CLKComplicationTemplateGraphicCircularStackImage](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackimage)

###### Creating the Template

- [init(line1ImageProvider: CLKFullColorImageProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackimage/init(line1imageprovider:line2textprovider:))

###### Setting the Complicaiton Data

- [var line1ImageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackimage/line1imageprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackimage/line2textprovider)
- [CLKComplicationTemplateGraphicCircularStackViewText](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext)

###### Creating the Template

- [init(content: Content, textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext/init(content:textprovider:))

###### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext/content)
- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularstackviewtext/textprovider)
- [CLKComplicationTemplateGraphicCircularStackText](/documentation/clockkit/clkcomplicationtemplategraphiccircularstacktext)

###### Creating the Template

- [init(line1TextProvider: CLKTextProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularstacktext/init(line1textprovider:line2textprovider:))

###### Setting the Complication Data

- [var line1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularstacktext/line1textprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularstacktext/line2textprovider)

##### Open and closed gauges

- [CLKComplicationTemplateGraphicCircularOpenGaugeImage](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeimage)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, bottomImageProvider: CLKFullColorImageProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeimage/init(gaugeprovider:bottomimageprovider:centertextprovider:))

###### Setting the Complication Data

- [var bottomImageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeimage/bottomimageprovider)
- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeimage/centertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeimage/gaugeprovider)
- [CLKComplicationTemplateGraphicCircularOpenGaugeView](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, centerTextProvider: CLKTextProvider, bottomLabel: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/init(gaugeprovider:centertextprovider:bottomlabel:))

###### Accesing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/gaugeprovider)
- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/centertextprovider)
- [var bottomLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugeview/bottomlabel)
- [CLKComplicationTemplateGraphicCircularOpenGaugeSimpleText](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugesimpletext)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, bottomTextProvider: CLKTextProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugesimpletext/init(gaugeprovider:bottomtextprovider:centertextprovider:))

###### Setting the Complication Data

- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugesimpletext/centertextprovider)
- [var bottomTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugesimpletext/bottomtextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugesimpletext/gaugeprovider)
- [CLKComplicationTemplateGraphicCircularOpenGaugeRangeText](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugerangetext)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, leadingTextProvider: CLKTextProvider, trailingTextProvider: CLKTextProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugerangetext/init(gaugeprovider:leadingtextprovider:trailingtextprovider:centertextprovider:))

###### Setting the Complication Data

- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugerangetext/centertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugerangetext/gaugeprovider)
- [var leadingTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugerangetext/leadingtextprovider)
- [var trailingTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularopengaugerangetext/trailingtextprovider)
- [CLKComplicationTemplateGraphicCircularClosedGaugeImage](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeimage)

###### Creating the Tempate

- [init(gaugeProvider: CLKGaugeProvider, imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeimage/init(gaugeprovider:imageprovider:))

###### Setting the Complication Data

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeimage/gaugeprovider)
- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeimage/imageprovider)
- [CLKComplicationTemplateGraphicCircularClosedGaugeView](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview/init(gaugeprovider:label:))

###### Accessing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview/gaugeprovider)
- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugeview/label)
- [CLKComplicationTemplateGraphicCircularClosedGaugeText](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugetext)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugetext/init(gaugeprovider:centertextprovider:))

###### Setting the Complication Data

- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugetext/centertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccircularclosedgaugetext/gaugeprovider)

##### Abstract superclass

- [CLKComplicationTemplateGraphicCircular](/documentation/clockkit/clkcomplicationtemplategraphiccircular)
- [Corner complication templates](/documentation/clockkit/corner-complication-templates)

##### Text and image

- [CLKComplicationTemplateGraphicCornerCircularImage](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularimage)

###### Creating the Template

- [init(imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularimage/init(imageprovider:))

###### Setting the Complication Data

- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularimage/imageprovider)
- [CLKComplicationTemplateGraphicCornerCircularView](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularview)

###### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularview/init(_:))

###### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphiccornercircularview/content)
- [CLKComplicationTemplateGraphicCornerStackText](/documentation/clockkit/clkcomplicationtemplategraphiccornerstacktext)

###### Creating the Template

- [init(innerTextProvider: CLKTextProvider, outerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccornerstacktext/init(innertextprovider:outertextprovider:))

###### Setting the Complication Data

- [var outerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornerstacktext/outertextprovider)
- [var innerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornerstacktext/innertextprovider)
- [CLKComplicationTemplateGraphicCornerTextImage](/documentation/clockkit/clkcomplicationtemplategraphiccornertextimage)

###### Creating the Template

- [init(textProvider: CLKTextProvider, imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccornertextimage/init(textprovider:imageprovider:))

###### Setting the Complication Data

- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornertextimage/imageprovider)
- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornertextimage/textprovider)
- [CLKComplicationTemplateGraphicCornerTextView](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview)

###### Creating the Template

- [init(textProvider: CLKTextProvider, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview/init(textprovider:label:))

###### Accessing the Content

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview/textprovider)
- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphiccornertextview/label)

##### Gauges

- [CLKComplicationTemplateGraphicCornerGaugeImage](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeimage)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeimage/init(gaugeprovider:imageprovider:))
- [init(gaugeProvider: CLKGaugeProvider, leadingTextProvider: CLKTextProvider?, trailingTextProvider: CLKTextProvider?, imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeimage/init(gaugeprovider:leadingtextprovider:trailingtextprovider:imageprovider:))

###### Setting the Complication Data

- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeimage/imageprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeimage/gaugeprovider)
- [var leadingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeimage/leadingtextprovider)
- [var trailingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeimage/trailingtextprovider)
- [CLKComplicationTemplateGraphicCornerGaugeView](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, leadingTextProvider: CLKTextProvider?, trailingTextProvider: CLKTextProvider?, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/init(gaugeprovider:leadingtextprovider:trailingtextprovider:label:))

###### Accessing the Content

- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/label)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/gaugeprovider)
- [var leadingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/leadingtextprovider)
- [var trailingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugeview/trailingtextprovider)
- [CLKComplicationTemplateGraphicCornerGaugeText](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugetext)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, outerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugetext/init(gaugeprovider:outertextprovider:))
- [init(gaugeProvider: CLKGaugeProvider, leadingTextProvider: CLKTextProvider?, trailingTextProvider: CLKTextProvider?, outerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugetext/init(gaugeprovider:leadingtextprovider:trailingtextprovider:outertextprovider:))

###### Setting the Complication Data

- [var outerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugetext/outertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugetext/gaugeprovider)
- [var leadingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugetext/leadingtextprovider)
- [var trailingTextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphiccornergaugetext/trailingtextprovider)
- [Rectangular complication templates.](/documentation/clockkit/rectangular-complication-templates)

##### Text and gauges

- [CLKComplicationTemplateGraphicRectangularStandardBody](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody)

###### Creating the Template

- [init(headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/init(headertextprovider:body1textprovider:))
- [init(headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, body2TextProvider: CLKTextProvider?)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/init(headertextprovider:body1textprovider:body2textprovider:))
- [init(headerImageProvider: CLKFullColorImageProvider?, headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/init(headerimageprovider:headertextprovider:body1textprovider:))
- [init(headerImageProvider: CLKFullColorImageProvider?, headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, body2TextProvider: CLKTextProvider?)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/init(headerimageprovider:headertextprovider:body1textprovider:body2textprovider:))

###### Setting the Complication Data

- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/headertextprovider)
- [var headerImageProvider: CLKFullColorImageProvider?](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/headerimageprovider)
- [var body1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/body1textprovider)
- [var body2TextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbody/body2textprovider)
- [CLKComplicationTemplateGraphicRectangularStandardBodyView](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview)

###### Creating the Template

- [init(headerLabel: Label, headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, body2TextProvider: CLKTextProvider?)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/init(headerlabel:headertextprovider:body1textprovider:body2textprovider:))

###### Accessing the Content

- [var headerLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/headerlabel)
- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/headertextprovider)
- [var body1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/body1textprovider)
- [var body2TextProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphicrectangularstandardbodyview/body2textprovider)
- [CLKComplicationTemplateGraphicRectangularTextGauge](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgauge)

###### Creating the Template

- [init(headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, gaugeProvider: CLKGaugeProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgauge/init(headertextprovider:body1textprovider:gaugeprovider:))
- [init(headerImageProvider: CLKFullColorImageProvider?, headerTextProvider: CLKTextProvider, body1TextProvider: CLKTextProvider, gaugeProvider: CLKGaugeProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgauge/init(headerimageprovider:headertextprovider:body1textprovider:gaugeprovider:))

###### Setting the Complication Data

- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgauge/headertextprovider)
- [var headerImageProvider: CLKFullColorImageProvider?](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgauge/headerimageprovider)
- [var body1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgauge/body1textprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgauge/gaugeprovider)
- [CLKComplicationTemplateGraphicRectangularTextGaugeView](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview)

###### Creating the Template

- [init(headerLabel: Label, headerTextProvider: CLKTextProvider, bodyTextProvider: CLKTextProvider, gaugeProvider: CLKGaugeProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/init(headerlabel:headertextprovider:bodytextprovider:gaugeprovider:))

###### Accessing the Content

- [var headerLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/headerlabel)
- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/headertextprovider)
- [var bodyTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/bodytextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangulartextgaugeview/gaugeprovider)

##### Large Images and Views

- [CLKComplicationTemplateGraphicRectangularLargeImage](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeimage)

###### Creating the Template

- [init(textProvider: CLKTextProvider, imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeimage/init(textprovider:imageprovider:))

###### Setting the Complication Data

- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeimage/textprovider)
- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeimage/imageprovider)
- [CLKComplicationTemplateGraphicRectangularLargeView](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview)

###### Creating the Template

- [init(headerTextProvider: CLKTextProvider, content: Content)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview/init(headertextprovider:content:))

###### Accessing the Content

- [var headerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview/headertextprovider)
- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicrectangularlargeview/content)
- [CLKComplicationTemplateGraphicRectangularFullImage](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullimage)

###### Creating the Template

- [init(imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullimage/init(imageprovider:))

###### Setting the Complication Data

- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullimage/imageprovider)
- [CLKComplicationTemplateGraphicRectangularFullView](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullview)

###### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullview/init(_:))

###### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicrectangularfullview/content)
- [Extra large circular templates](/documentation/clockkit/extra-large-circular-templates)

##### Text and images

- [CLKComplicationTemplateGraphicExtraLargeCircularImage](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularimage)

###### Creating the Template

- [init(imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularimage/init(imageprovider:))

###### Setting the Complication Data

- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularimage/imageprovider)
- [CLKComplicationTemplateGraphicExtraLargeCircularView](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularview)

###### Creating the Template

- [init(Content)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularview/init(_:))

###### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularview/content)
- [CLKComplicationTemplateGraphicExtraLargeCircularStackImage](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackimage)

###### Creating the Template

- [init(line1ImageProvider: CLKFullColorImageProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackimage/init(line1imageprovider:line2textprovider:))

###### Setting the Complication Data

- [var line1ImageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackimage/line1imageprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackimage/line2textprovider)
- [CLKComplicationTemplateGraphicExtraLargeCircularStackViewText](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext)

###### Creating the Template

- [init(content: Content, textProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext/init(content:textprovider:))

###### Accessing the Content

- [var content: Content](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext/content)
- [var textProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstackviewtext/textprovider)
- [CLKComplicationTemplateGraphicExtraLargeCircularStackText](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstacktext)

###### Creating the Template

- [init(line1TextProvider: CLKTextProvider, line2TextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstacktext/init(line1textprovider:line2textprovider:))

###### Setting the Complication Data

- [var line1TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstacktext/line1textprovider)
- [var line2TextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularstacktext/line2textprovider)

##### Open and closed gauges

- [CLKComplicationTemplateGraphicExtraLargeCircularOpenGaugeImage](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeimage)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, bottomImageProvider: CLKFullColorImageProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeimage/init(gaugeprovider:bottomimageprovider:centertextprovider:))

###### Setting the Complication Data

- [var bottomImageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeimage/bottomimageprovider)
- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeimage/centertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeimage/gaugeprovider)
- [CLKComplicationTemplateGraphicExtraLargeCircularOpenGaugeView](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, centerTextProvider: CLKTextProvider, bottomLabel: Label)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/init(gaugeprovider:centertextprovider:bottomlabel:))

###### Accessing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/gaugeprovider)
- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/centertextprovider)
- [var bottomLabel: Label](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugeview/bottomlabel)
- [CLKComplicationTemplateGraphicExtraLargeCircularOpenGaugeSimpleText](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugesimpletext)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, bottomTextProvider: CLKTextProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugesimpletext/init(gaugeprovider:bottomtextprovider:centertextprovider:))

###### Setting the Complication Data

- [var bottomTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugesimpletext/bottomtextprovider)
- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugesimpletext/centertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugesimpletext/gaugeprovider)
- [CLKComplicationTemplateGraphicExtraLargeCircularOpenGaugeRangeText](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugerangetext)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, leadingTextProvider: CLKTextProvider, trailingTextProvider: CLKTextProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugerangetext/init(gaugeprovider:leadingtextprovider:trailingtextprovider:centertextprovider:))

###### Setting the Complication Data

- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugerangetext/centertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugerangetext/gaugeprovider)
- [var leadingTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugerangetext/leadingtextprovider)
- [var trailingTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularopengaugerangetext/trailingtextprovider)
- [CLKComplicationTemplateGraphicExtraLargeCircularClosedGaugeImage](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeimage)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, imageProvider: CLKFullColorImageProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeimage/init(gaugeprovider:imageprovider:))

###### Setting the Complication Data

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeimage/gaugeprovider)
- [var imageProvider: CLKFullColorImageProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeimage/imageprovider)
- [CLKComplicationTemplateGraphicExtraLargeCircularClosedGaugeView](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, label: Label)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview/init(gaugeprovider:label:))

###### Accessing the Content

- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview/gaugeprovider)
- [var label: Label](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugeview/label)
- [CLKComplicationTemplateGraphicExtraLargeCircularClosedGaugeText](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugetext)

###### Creating the Template

- [init(gaugeProvider: CLKGaugeProvider, centerTextProvider: CLKTextProvider)](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugetext/init(gaugeprovider:centertextprovider:))

###### Setting the Complication Data

- [var centerTextProvider: CLKTextProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugetext/centertextprovider)
- [var gaugeProvider: CLKGaugeProvider](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircularclosedgaugetext/gaugeprovider)

##### Abstract superclass

- [CLKComplicationTemplateGraphicExtraLargeCircular](/documentation/clockkit/clkcomplicationtemplategraphicextralargecircular)
- [CLKComplicationTemplateGraphicBezelCircularText](/documentation/clockkit/clkcomplicationtemplategraphicbezelcirculartext)

##### Creating the Template

- [init(circularTemplate: CLKComplicationTemplateGraphicCircular)](/documentation/clockkit/clkcomplicationtemplategraphicbezelcirculartext/init(circulartemplate:))
- [init(circularTemplate: CLKComplicationTemplateGraphicCircular, textProvider: CLKTextProvider?)](/documentation/clockkit/clkcomplicationtemplategraphicbezelcirculartext/init(circulartemplate:textprovider:))

##### Setting the Complication Data

- [var circularTemplate: CLKComplicationTemplateGraphicCircular](/documentation/clockkit/clkcomplicationtemplategraphicbezelcirculartext/circulartemplate)
- [var textProvider: CLKTextProvider?](/documentation/clockkit/clkcomplicationtemplategraphicbezelcirculartext/textprovider)
- [CLKComplicationTemplate](/documentation/clockkit/clkcomplicationtemplate)

#### Setting the Tint Color

- [var tintColor: UIColor?](/documentation/clockkit/clkcomplicationtemplate/tintcolor)

#### Displaying Previews

- [func previewContext(faceColor: CLKComplicationTemplate.PreviewFaceColor) -> some View](/documentation/clockkit/clkcomplicationtemplate/previewcontext(facecolor:))
- [CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor)

##### Colors

- [static var allColors: [CLKComplicationTemplate.PreviewFaceColor]](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/allcolors)
- [static let multicolor: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/multicolor)
- [static let pink: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/pink)
- [static let red: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/red)
- [static let orange: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/orange)
- [static let yellow: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/yellow)
- [static let green: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/green)
- [static let blue: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/blue)
- [static let purple: CLKComplicationTemplate.PreviewFaceColor](/documentation/clockkit/clkcomplicationtemplate/previewfacecolor/purple)

#### Specifying Styles

- [CLKComplicationColumnAlignment](/documentation/clockkit/clkcomplicationcolumnalignment)

##### Constants

- [case leading](/documentation/clockkit/clkcomplicationcolumnalignment/leading)
- [case trailing](/documentation/clockkit/clkcomplicationcolumnalignment/trailing)
- [static var left: CLKComplicationColumnAlignment](/documentation/clockkit/clkcomplicationcolumnalignment/left)
- [static var right: CLKComplicationColumnAlignment](/documentation/clockkit/clkcomplicationcolumnalignment/right)

##### Initializers

- [init?(rawValue: Int)](/documentation/clockkit/clkcomplicationcolumnalignment/init(rawvalue:))
- [CLKComplicationRingStyle](/documentation/clockkit/clkcomplicationringstyle)

##### Constants

- [case closed](/documentation/clockkit/clkcomplicationringstyle/closed)
- [case open](/documentation/clockkit/clkcomplicationringstyle/open)

##### Initializers

- [init?(rawValue: Int)](/documentation/clockkit/clkcomplicationringstyle/init(rawvalue:))

#### Creating Empty Templates

- [init()](/documentation/clockkit/clkcomplicationtemplate/init())
- [class func new() -> Self](/documentation/clockkit/clkcomplicationtemplate/new())
- [CLKComplicationFamily](/documentation/clockkit/clkcomplicationfamily)

#### Circular Small

- [case circularSmall](/documentation/clockkit/clkcomplicationfamily/circularsmall)

#### Extra Large

- [case extraLarge](/documentation/clockkit/clkcomplicationfamily/extralarge)

#### Modular

- [case modularSmall](/documentation/clockkit/clkcomplicationfamily/modularsmall)
- [case modularLarge](/documentation/clockkit/clkcomplicationfamily/modularlarge)

#### Utilitarian

- [case utilitarianSmall](/documentation/clockkit/clkcomplicationfamily/utilitariansmall)
- [case utilitarianSmallFlat](/documentation/clockkit/clkcomplicationfamily/utilitariansmallflat)
- [case utilitarianLarge](/documentation/clockkit/clkcomplicationfamily/utilitarianlarge)

#### Graphic

- [case graphicCorner](/documentation/clockkit/clkcomplicationfamily/graphiccorner)
- [case graphicCircular](/documentation/clockkit/clkcomplicationfamily/graphiccircular)
- [case graphicBezel](/documentation/clockkit/clkcomplicationfamily/graphicbezel)
- [case graphicRectangular](/documentation/clockkit/clkcomplicationfamily/graphicrectangular)
- [case graphicExtraLarge](/documentation/clockkit/clkcomplicationfamily/graphicextralarge)

#### Initializers

- [init?(rawValue: Int)](/documentation/clockkit/clkcomplicationfamily/init(rawvalue:))
- [CLKComplicationSupportedFamilies](/documentation/bundleresources/information-property-list/clkcomplicationsupportedfamilies)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
