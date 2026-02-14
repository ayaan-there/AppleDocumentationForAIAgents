# Notification Center Documentation

Source: https://sosumi.ai/documentation/notificationcenter

---
title: Notification Center
source: https://developer.apple.com/documentation/notificationcenter
timestamp: 2026-02-13T19:00:08.538Z
---

## Core Widget

- [NCWidgetProviding](/documentation/notificationcenter/ncwidgetproviding)

### Customizing the Display

- [func widgetMarginInsets(forProposedMarginInsets: UIEdgeInsets) -> UIEdgeInsets](/documentation/notificationcenter/ncwidgetproviding/widgetmargininsets(forproposedmargininsets:))
- [func widgetActiveDisplayModeDidChange(NCWidgetDisplayMode, withMaximumSize: CGSize)](/documentation/notificationcenter/ncwidgetproviding/widgetactivedisplaymodedidchange(_:withmaximumsize:))
- [NCWidgetDisplayMode](/documentation/notificationcenter/ncwidgetdisplaymode)

#### Constants

- [case compact](/documentation/notificationcenter/ncwidgetdisplaymode/compact)
- [case expanded](/documentation/notificationcenter/ncwidgetdisplaymode/expanded)

#### Initializers

- [init?(rawValue: Int)](/documentation/notificationcenter/ncwidgetdisplaymode/init(rawvalue:))

### Updating a Widget’s Contents

- [func widgetPerformUpdate(completionHandler: (NCUpdateResult) -> Void)](/documentation/notificationcenter/ncwidgetproviding/widgetperformupdate(completionhandler:))
- [NCUpdateResult](/documentation/notificationcenter/ncupdateresult)

#### Constants

- [case newData](/documentation/notificationcenter/ncupdateresult/newdata)
- [case noData](/documentation/notificationcenter/ncupdateresult/nodata)
- [case failed](/documentation/notificationcenter/ncupdateresult/failed)

#### Initializers

- [init?(rawValue: UInt)](/documentation/notificationcenter/ncupdateresult/init(rawvalue:))

### Supporting Editing

- [var widgetAllowsEditing: Bool](/documentation/notificationcenter/ncwidgetproviding/widgetallowsediting)
- [func widgetDidBeginEditing()](/documentation/notificationcenter/ncwidgetproviding/widgetdidbeginediting())
- [func widgetDidEndEditing()](/documentation/notificationcenter/ncwidgetproviding/widgetdidendediting())
- [NCWidgetController](/documentation/notificationcenter/ncwidgetcontroller)

### Getting a Widget Controller

- [class func widgetController() -> Self](/documentation/notificationcenter/ncwidgetcontroller/widgetcontroller())

### Specifying the Presence of Content

- [func setHasContent(Bool, forWidgetWithBundleIdentifier: String)](/documentation/notificationcenter/ncwidgetcontroller/sethascontent(_:forwidgetwithbundleidentifier:))

### Type Methods

- [class func `default`() -> NCWidgetController](/documentation/notificationcenter/ncwidgetcontroller/default())

## Search View

- [NCWidgetSearchViewController](/documentation/notificationcenter/ncwidgetsearchviewcontroller)

### Enabling Search

- [var delegate: (any NCWidgetSearchViewDelegate)?](/documentation/notificationcenter/ncwidgetsearchviewcontroller/delegate)
- [NCWidgetSearchViewDelegate](/documentation/notificationcenter/ncwidgetsearchviewdelegate)

#### Searching Your Content

- [func widgetSearch(NCWidgetSearchViewController, searchForTerm: String, maxResults: Int)](/documentation/notificationcenter/ncwidgetsearchviewdelegate/widgetsearch(_:searchforterm:maxresults:))

#### Responding to User Choices

- [func widgetSearch(NCWidgetSearchViewController, resultSelected: Any)](/documentation/notificationcenter/ncwidgetsearchviewdelegate/widgetsearch(_:resultselected:))
- [func widgetSearchTermCleared(NCWidgetSearchViewController)](/documentation/notificationcenter/ncwidgetsearchviewdelegate/widgetsearchtermcleared(_:))

### Displaying the Search Interface

- [var searchDescription: String?](/documentation/notificationcenter/ncwidgetsearchviewcontroller/searchdescription)
- [var searchResultsPlaceholderString: String?](/documentation/notificationcenter/ncwidgetsearchviewcontroller/searchresultsplaceholderstring)

### Displaying Search Results

- [var searchResultKeyPath: String?](/documentation/notificationcenter/ncwidgetsearchviewcontroller/searchresultkeypath)
- [var searchResults: [Any]?](/documentation/notificationcenter/ncwidgetsearchviewcontroller/searchresults)
- [NCWidgetSearchViewDelegate](/documentation/notificationcenter/ncwidgetsearchviewdelegate)

### Searching Your Content

- [func widgetSearch(NCWidgetSearchViewController, searchForTerm: String, maxResults: Int)](/documentation/notificationcenter/ncwidgetsearchviewdelegate/widgetsearch(_:searchforterm:maxresults:))

### Responding to User Choices

- [func widgetSearch(NCWidgetSearchViewController, resultSelected: Any)](/documentation/notificationcenter/ncwidgetsearchviewdelegate/widgetsearch(_:resultselected:))
- [func widgetSearchTermCleared(NCWidgetSearchViewController)](/documentation/notificationcenter/ncwidgetsearchviewdelegate/widgetsearchtermcleared(_:))

## List View

- [NCWidgetListViewController](/documentation/notificationcenter/ncwidgetlistviewcontroller)

### Displaying and Editing List Content

- [var delegate: (any NCWidgetListViewDelegate)?](/documentation/notificationcenter/ncwidgetlistviewcontroller/delegate)
- [NCWidgetListViewDelegate](/documentation/notificationcenter/ncwidgetlistviewdelegate)

#### Creating a Content View Controller

- [func widgetList(NCWidgetListViewController, viewControllerForRow: Int) -> NSViewController](/documentation/notificationcenter/ncwidgetlistviewdelegate/widgetlist(_:viewcontrollerforrow:))

#### Adding and Deleting Rows

- [func widgetList(NCWidgetListViewController, didRemoveRow: Int)](/documentation/notificationcenter/ncwidgetlistviewdelegate/widgetlist(_:didremoverow:))
- [func widgetList(NCWidgetListViewController, shouldRemoveRow: Int) -> Bool](/documentation/notificationcenter/ncwidgetlistviewdelegate/widgetlist(_:shouldremoverow:))
- [func widgetListPerformAddAction(NCWidgetListViewController)](/documentation/notificationcenter/ncwidgetlistviewdelegate/widgetlistperformaddaction(_:))

#### Reordering List Rows

- [func widgetList(NCWidgetListViewController, didReorderRow: Int, toRow: Int)](/documentation/notificationcenter/ncwidgetlistviewdelegate/widgetlist(_:didreorderrow:torow:))
- [func widgetList(NCWidgetListViewController, shouldReorderRow: Int) -> Bool](/documentation/notificationcenter/ncwidgetlistviewdelegate/widgetlist(_:shouldreorderrow:))

### Accessing Content

- [var contents: [Any]](/documentation/notificationcenter/ncwidgetlistviewcontroller/contents)
- [func row(for: NSViewController) -> Int](/documentation/notificationcenter/ncwidgetlistviewcontroller/row(for:))
- [func viewController(atRow: Int, makeIfNecessary: Bool) -> NSViewController](/documentation/notificationcenter/ncwidgetlistviewcontroller/viewcontroller(atrow:makeifnecessary:))

### Customizing the List Appearance

- [var minimumVisibleRowCount: Int](/documentation/notificationcenter/ncwidgetlistviewcontroller/minimumvisiblerowcount)
- [var hasDividerLines: Bool](/documentation/notificationcenter/ncwidgetlistviewcontroller/hasdividerlines)

### Supporting Editing

- [var editing: Bool](/documentation/notificationcenter/ncwidgetlistviewcontroller/editing)
- [var showsAddButtonWhenEditing: Bool](/documentation/notificationcenter/ncwidgetlistviewcontroller/showsaddbuttonwhenediting)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
