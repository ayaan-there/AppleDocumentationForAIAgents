# EventKit UI Documentation

Source: https://sosumi.ai/documentation/eventkitui

---
title: EventKit UI
source: https://developer.apple.com/documentation/eventkitui
timestamp: 2026-02-13T18:56:40.153Z
---

## Calendar Views

- [EKEventViewController](/documentation/eventkitui/ekeventviewcontroller)

### Dismissing the Event Interface

- [var delegate: (any EKEventViewDelegate)?](/documentation/eventkitui/ekeventviewcontroller/delegate)
- [EKEventViewDelegate](/documentation/eventkitui/ekeventviewdelegate)

#### Responding to the Interface’s Dismissal

- [EKEventViewAction](/documentation/eventkitui/ekeventviewaction)

##### Constants

- [case done](/documentation/eventkitui/ekeventviewaction/done)
- [case responded](/documentation/eventkitui/ekeventviewaction/responded)
- [case deleted](/documentation/eventkitui/ekeventviewaction/deleted)

##### Initializers

- [init?(rawValue: Int)](/documentation/eventkitui/ekeventviewaction/init(rawvalue:))
- [func eventViewController(EKEventViewController, didCompleteWith: EKEventViewAction)](/documentation/eventkitui/ekeventviewdelegate/eventviewcontroller(_:didcompletewith:))

### Getting and Setting the Event

- [var event: EKEvent!](/documentation/eventkitui/ekeventviewcontroller/event)

### Displaying and Editing Event Previews

- [var allowsCalendarPreview: Bool](/documentation/eventkitui/ekeventviewcontroller/allowscalendarpreview)
- [var allowsEditing: Bool](/documentation/eventkitui/ekeventviewcontroller/allowsediting)

## Calendar Edits

- [EKEventEditViewController](/documentation/eventkitui/ekeventeditviewcontroller)

### Managing the Event Editing Interface

- [var editViewDelegate: (any EKEventEditViewDelegate)?](/documentation/eventkitui/ekeventeditviewcontroller/editviewdelegate)
- [EKEventEditViewDelegate](/documentation/eventkitui/ekeventeditviewdelegate)

#### Getting the Default Calendar

- [func eventEditViewControllerDefaultCalendar(forNewEvents: EKEventEditViewController) -> EKCalendar](/documentation/eventkitui/ekeventeditviewdelegate/eventeditviewcontrollerdefaultcalendar(fornewevents:))

#### Finishing an Edit

- [func eventEditViewController(EKEventEditViewController, didCompleteWith: EKEventEditViewAction)](/documentation/eventkitui/ekeventeditviewdelegate/eventeditviewcontroller(_:didcompletewith:))
- [EKEventEditViewAction](/documentation/eventkitui/ekeventeditviewaction)

##### Constants

- [case canceled](/documentation/eventkitui/ekeventeditviewaction/canceled)
- [case saved](/documentation/eventkitui/ekeventeditviewaction/saved)
- [case deleted](/documentation/eventkitui/ekeventeditviewaction/deleted)
- [static var cancelled: EKEventEditViewAction](/documentation/eventkitui/ekeventeditviewaction/cancelled)

##### Initializers

- [init?(rawValue: Int)](/documentation/eventkitui/ekeventeditviewaction/init(rawvalue:))

### Creating and Saving Events

- [var event: EKEvent?](/documentation/eventkitui/ekeventeditviewcontroller/event)
- [var eventStore: EKEventStore!](/documentation/eventkitui/ekeventeditviewcontroller/eventstore)

### Canceling Edits to Events

- [func cancelEditing()](/documentation/eventkitui/ekeventeditviewcontroller/cancelediting())

## Calendar Selection

- [EKCalendarChooser](/documentation/eventkitui/ekcalendarchooser)

### Initializing Calendar Choosers

- [init(selectionStyle: EKCalendarChooserSelectionStyle, displayStyle: EKCalendarChooserDisplayStyle, eventStore: EKEventStore)](/documentation/eventkitui/ekcalendarchooser/init(selectionstyle:displaystyle:eventstore:))
- [init(selectionStyle: EKCalendarChooserSelectionStyle, displayStyle: EKCalendarChooserDisplayStyle, entityType: EKEntityType, eventStore: EKEventStore)](/documentation/eventkitui/ekcalendarchooser/init(selectionstyle:displaystyle:entitytype:eventstore:))

### Managing Calendar Selection

- [var delegate: (any EKCalendarChooserDelegate)?](/documentation/eventkitui/ekcalendarchooser/delegate)
- [EKCalendarChooserDelegate](/documentation/eventkitui/ekcalendarchooserdelegate)

#### Selecting Calendars

- [func calendarChooserDidFinish(EKCalendarChooser)](/documentation/eventkitui/ekcalendarchooserdelegate/calendarchooserdidfinish(_:))
- [func calendarChooserSelectionDidChange(EKCalendarChooser)](/documentation/eventkitui/ekcalendarchooserdelegate/calendarchooserselectiondidchange(_:))
- [func calendarChooserDidCancel(EKCalendarChooser)](/documentation/eventkitui/ekcalendarchooserdelegate/calendarchooserdidcancel(_:))

### Selecting a Calendar Type

- [var selectedCalendars: Set<EKCalendar>](/documentation/eventkitui/ekcalendarchooser/selectedcalendars)
- [var selectionStyle: EKCalendarChooserSelectionStyle](/documentation/eventkitui/ekcalendarchooser/selectionstyle)
- [EKCalendarChooserSelectionStyle](/documentation/eventkitui/ekcalendarchooserselectionstyle)

#### Constants

- [case single](/documentation/eventkitui/ekcalendarchooserselectionstyle/single)
- [case multiple](/documentation/eventkitui/ekcalendarchooserselectionstyle/multiple)

#### Initializers

- [init?(rawValue: Int)](/documentation/eventkitui/ekcalendarchooserselectionstyle/init(rawvalue:))
- [EKCalendarChooserDisplayStyle](/documentation/eventkitui/ekcalendarchooserdisplaystyle)

#### Constants

- [case allCalendars](/documentation/eventkitui/ekcalendarchooserdisplaystyle/allcalendars)
- [case writableCalendarsOnly](/documentation/eventkitui/ekcalendarchooserdisplaystyle/writablecalendarsonly)

#### Initializers

- [init?(rawValue: Int)](/documentation/eventkitui/ekcalendarchooserdisplaystyle/init(rawvalue:))

### Changing the Appearance

- [var showsCancelButton: Bool](/documentation/eventkitui/ekcalendarchooser/showscancelbutton)
- [var showsDoneButton: Bool](/documentation/eventkitui/ekcalendarchooser/showsdonebutton)

## EventKit Bundle Access

- [func EventKitUIBundle() -> Bundle!](/documentation/eventkitui/eventkituibundle())

## Reference

- [EventKitUI Constants](/documentation/eventkitui/eventkitui-constants)

### Constants

- [var EKUI_IS_IOS: Int32](/documentation/eventkitui/ekui_is_ios)
- [var EKUI_IS_SIMULATOR: Int32](/documentation/eventkitui/ekui_is_simulator)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
