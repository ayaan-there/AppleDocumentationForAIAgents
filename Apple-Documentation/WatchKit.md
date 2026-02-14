# WatchKit Documentation

Source: https://sosumi.ai/documentation/watchkit

---
title: WatchKit
source: https://developer.apple.com/documentation/watchkit
timestamp: 2026-02-13T19:03:58.916Z
---

## App structure

- [Setting up a watchOS project](/documentation/watchkit/setting-up-a-watchos-project)

### Information Property List Keys

- [WKWatchKitApp](/documentation/bundleresources/information-property-list/wkwatchkitapp)
- [WKAppBundleIdentifier](/documentation/bundleresources/information-property-list/wkappbundleidentifier)
- [WKCompanionAppBundleIdentifier](/documentation/bundleresources/information-property-list/wkcompanionappbundleidentifier)
- [WKExtensionDelegateClassName](/documentation/bundleresources/information-property-list/wkextensiondelegateclassname)
- [WKRunsIndependentlyOfCompanionApp](/documentation/bundleresources/information-property-list/wkrunsindependentlyofcompanionapp)
- [WKWatchOnly](/documentation/bundleresources/information-property-list/wkwatchonly)
- [WKApplication](/documentation/watchkit/wkapplication)

### Getting the app object

- [class func shared() -> WKApplication](/documentation/watchkit/wkapplication/shared())

### Accessing the app delegate

- [var delegate: (any WKApplicationDelegate)?](/documentation/watchkit/wkapplication/delegate)
- [WKApplicationDelegate](/documentation/watchkit/wkapplicationdelegate)

#### Monitoring state changes

- [Working with the watchOS app life cycle](/documentation/watchkit/working-with-the-watchos-app-life-cycle)
- [static func main()](/documentation/watchkit/wkapplicationdelegate/main())
- [func applicationDidFinishLaunching()](/documentation/watchkit/wkapplicationdelegate/applicationdidfinishlaunching())
- [func applicationDidBecomeActive()](/documentation/watchkit/wkapplicationdelegate/applicationdidbecomeactive())
- [func applicationWillResignActive()](/documentation/watchkit/wkapplicationdelegate/applicationwillresignactive())
- [func applicationWillEnterForeground()](/documentation/watchkit/wkapplicationdelegate/applicationwillenterforeground())
- [func applicationDidEnterBackground()](/documentation/watchkit/wkapplicationdelegate/applicationdidenterbackground())
- [func deviceOrientationDidChange()](/documentation/watchkit/wkapplicationdelegate/deviceorientationdidchange())

#### Responding to intents

- [func handle(INIntent, completionHandler: (INIntentResponse) -> Void)](/documentation/watchkit/wkapplicationdelegate/handle(_:completionhandler:))

#### Setup Now Playing interface

- [func handleRemoteNowPlayingActivity()](/documentation/watchkit/wkapplicationdelegate/handleremotenowplayingactivity())

#### Handling a workout session

- [func handle(HKWorkoutConfiguration)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-1pfoc)
- [func handleActiveWorkoutRecovery()](/documentation/watchkit/wkapplicationdelegate/handleactiveworkoutrecovery())

#### Handling background tasks

- [func handle(Set<WKRefreshBackgroundTask>)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-4vdjo)

#### Handling extended runtime tasks

- [func handle(WKExtendedRuntimeSession)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-7kiwx)

#### Managing remote notifications

- [func didRegisterForRemoteNotifications(withDeviceToken: Data)](/documentation/watchkit/wkapplicationdelegate/didregisterforremotenotifications(withdevicetoken:))
- [func didFailToRegisterForRemoteNotificationsWithError(any Error)](/documentation/watchkit/wkapplicationdelegate/didfailtoregisterforremotenotificationswitherror(_:))
- [func didReceiveRemoteNotification([AnyHashable : Any], fetchCompletionHandler: (WKBackgroundFetchResult) -> Void)](/documentation/watchkit/wkapplicationdelegate/didreceiveremotenotification(_:fetchcompletionhandler:))
- [WKBackgroundFetchResult](/documentation/watchkit/wkbackgroundfetchresult)

##### Fetch Results

- [case failed](/documentation/watchkit/wkbackgroundfetchresult/failed)
- [case newData](/documentation/watchkit/wkbackgroundfetchresult/newdata)
- [case noData](/documentation/watchkit/wkbackgroundfetchresult/nodata)

##### Initializers

- [init?(rawValue: UInt)](/documentation/watchkit/wkbackgroundfetchresult/init(rawvalue:))

#### Coordinating Handoff activity

- [func handleUserActivity([AnyHashable : Any]?)](/documentation/watchkit/wkapplicationdelegate/handleuseractivity(_:))
- [func handle(NSUserActivity)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-3kqsk)

#### Accepting CloudKit shares

- [func userDidAcceptCloudKitShare(with: CKShareMetadata)](/documentation/watchkit/wkapplicationdelegate/userdidacceptcloudkitshare(with:))

### Opening a URL resource

- [func openSystemURL(URL)](/documentation/watchkit/wkapplication/opensystemurl(_:))

### Getting the interface controller

- [var rootInterfaceController: WKInterfaceController?](/documentation/watchkit/wkapplication/rootinterfacecontroller)
- [var visibleInterfaceController: WKInterfaceController?](/documentation/watchkit/wkapplication/visibleinterfacecontroller)

### Managing the app state

- [var applicationState: WKApplicationState](/documentation/watchkit/wkapplication/applicationstate)
- [WKApplicationState](/documentation/watchkit/wkapplicationstate)

#### Constants

- [case active](/documentation/watchkit/wkapplicationstate/active)
- [case inactive](/documentation/watchkit/wkapplicationstate/inactive)
- [case background](/documentation/watchkit/wkapplicationstate/background)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkapplicationstate/init(rawvalue:))
- [var isApplicationRunningInDock: Bool](/documentation/watchkit/wkapplication/isapplicationrunningindock)
- [func scheduleBackgroundRefresh(withPreferredDate: Date, userInfo: (any NSSecureCoding & NSObjectProtocol)?, scheduledCompletion: ((any Error)?) -> Void)](/documentation/watchkit/wkapplication/schedulebackgroundrefresh(withpreferreddate:userinfo:scheduledcompletion:))

### Managing the user interface

- [var isAutorotating: Bool](/documentation/watchkit/wkapplication/isautorotating)
- [var isAutorotated: Bool](/documentation/watchkit/wkapplication/isautorotated)
- [var globalTintColor: UIColor](/documentation/watchkit/wkapplication/globaltintcolor)

### Managing the snapshot

- [func scheduleSnapshotRefresh(withPreferredDate: Date, userInfo: (any NSSecureCoding & NSObjectProtocol)?, scheduledCompletion: ((any Error)?) -> Void)](/documentation/watchkit/wkapplication/schedulesnapshotrefresh(withpreferreddate:userinfo:scheduledcompletion:))

### Observing messages from the notification center

- [static let didFinishLaunchingNotification: NSNotification.Name](/documentation/watchkit/wkapplication/didfinishlaunchingnotification)
- [static let didBecomeActiveNotification: NSNotification.Name](/documentation/watchkit/wkapplication/didbecomeactivenotification)
- [static let willResignActiveNotification: NSNotification.Name](/documentation/watchkit/wkapplication/willresignactivenotification)
- [static let willEnterForegroundNotification: NSNotification.Name](/documentation/watchkit/wkapplication/willenterforegroundnotification)
- [static let didEnterBackgroundNotification: NSNotification.Name](/documentation/watchkit/wkapplication/didenterbackgroundnotification)

### Registering for remote notifications

- [func registerForRemoteNotifications()](/documentation/watchkit/wkapplication/registerforremotenotifications())
- [func unregisterForRemoteNotifications()](/documentation/watchkit/wkapplication/unregisterforremotenotifications())
- [var isRegisteredForRemoteNotifications: Bool](/documentation/watchkit/wkapplication/isregisteredforremotenotifications)
- [WKApplicationDelegate](/documentation/watchkit/wkapplicationdelegate)

### Monitoring state changes

- [Working with the watchOS app life cycle](/documentation/watchkit/working-with-the-watchos-app-life-cycle)
- [static func main()](/documentation/watchkit/wkapplicationdelegate/main())
- [func applicationDidFinishLaunching()](/documentation/watchkit/wkapplicationdelegate/applicationdidfinishlaunching())
- [func applicationDidBecomeActive()](/documentation/watchkit/wkapplicationdelegate/applicationdidbecomeactive())
- [func applicationWillResignActive()](/documentation/watchkit/wkapplicationdelegate/applicationwillresignactive())
- [func applicationWillEnterForeground()](/documentation/watchkit/wkapplicationdelegate/applicationwillenterforeground())
- [func applicationDidEnterBackground()](/documentation/watchkit/wkapplicationdelegate/applicationdidenterbackground())
- [func deviceOrientationDidChange()](/documentation/watchkit/wkapplicationdelegate/deviceorientationdidchange())

### Responding to intents

- [func handle(INIntent, completionHandler: (INIntentResponse) -> Void)](/documentation/watchkit/wkapplicationdelegate/handle(_:completionhandler:))

### Setup Now Playing interface

- [func handleRemoteNowPlayingActivity()](/documentation/watchkit/wkapplicationdelegate/handleremotenowplayingactivity())

### Handling a workout session

- [func handle(HKWorkoutConfiguration)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-1pfoc)
- [func handleActiveWorkoutRecovery()](/documentation/watchkit/wkapplicationdelegate/handleactiveworkoutrecovery())

### Handling background tasks

- [func handle(Set<WKRefreshBackgroundTask>)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-4vdjo)

### Handling extended runtime tasks

- [func handle(WKExtendedRuntimeSession)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-7kiwx)

### Managing remote notifications

- [func didRegisterForRemoteNotifications(withDeviceToken: Data)](/documentation/watchkit/wkapplicationdelegate/didregisterforremotenotifications(withdevicetoken:))
- [func didFailToRegisterForRemoteNotificationsWithError(any Error)](/documentation/watchkit/wkapplicationdelegate/didfailtoregisterforremotenotificationswitherror(_:))
- [func didReceiveRemoteNotification([AnyHashable : Any], fetchCompletionHandler: (WKBackgroundFetchResult) -> Void)](/documentation/watchkit/wkapplicationdelegate/didreceiveremotenotification(_:fetchcompletionhandler:))
- [WKBackgroundFetchResult](/documentation/watchkit/wkbackgroundfetchresult)

#### Fetch Results

- [case failed](/documentation/watchkit/wkbackgroundfetchresult/failed)
- [case newData](/documentation/watchkit/wkbackgroundfetchresult/newdata)
- [case noData](/documentation/watchkit/wkbackgroundfetchresult/nodata)

#### Initializers

- [init?(rawValue: UInt)](/documentation/watchkit/wkbackgroundfetchresult/init(rawvalue:))

### Coordinating Handoff activity

- [func handleUserActivity([AnyHashable : Any]?)](/documentation/watchkit/wkapplicationdelegate/handleuseractivity(_:))
- [func handle(NSUserActivity)](/documentation/watchkit/wkapplicationdelegate/handle(_:)-3kqsk)

### Accepting CloudKit shares

- [func userDidAcceptCloudKitShare(with: CKShareMetadata)](/documentation/watchkit/wkapplicationdelegate/userdidacceptcloudkitshare(with:))
- [WKExtension](/documentation/watchkit/wkextension)

### Getting the extension object

- [class func shared() -> WKExtension](/documentation/watchkit/wkextension/shared())

### Accessing the extension delegate

- [var delegate: (any WKExtensionDelegate)?](/documentation/watchkit/wkextension/delegate)
- [WKExtensionDelegate](/documentation/watchkit/wkextensiondelegate)

#### Monitoring state changes

- [Working with the watchOS app life cycle](/documentation/watchkit/working-with-the-watchos-app-life-cycle)
- [func applicationDidFinishLaunching()](/documentation/watchkit/wkextensiondelegate/applicationdidfinishlaunching())
- [func applicationDidBecomeActive()](/documentation/watchkit/wkextensiondelegate/applicationdidbecomeactive())
- [func applicationWillResignActive()](/documentation/watchkit/wkextensiondelegate/applicationwillresignactive())
- [func applicationWillEnterForeground()](/documentation/watchkit/wkextensiondelegate/applicationwillenterforeground())
- [func applicationDidEnterBackground()](/documentation/watchkit/wkextensiondelegate/applicationdidenterbackground())
- [func deviceOrientationDidChange()](/documentation/watchkit/wkextensiondelegate/deviceorientationdidchange())

#### Responding to intents

- [func handle(INIntent, completionHandler: (INIntentResponse) -> Void)](/documentation/watchkit/wkextensiondelegate/handle(_:completionhandler:))

#### Setup Now Playing interface

- [func handleRemoteNowPlayingActivity()](/documentation/watchkit/wkextensiondelegate/handleremotenowplayingactivity())

#### Handling a workout session

- [func handle(HKWorkoutConfiguration)](/documentation/watchkit/wkextensiondelegate/handle(_:)-f27i)
- [func handleActiveWorkoutRecovery()](/documentation/watchkit/wkextensiondelegate/handleactiveworkoutrecovery())

#### Handling background tasks

- [func handle(Set<WKRefreshBackgroundTask>)](/documentation/watchkit/wkextensiondelegate/handle(_:)-92ulv)

#### Handling extended runtime sessions

- [func handle(WKExtendedRuntimeSession)](/documentation/watchkit/wkextensiondelegate/handle(_:)-4qxgv)

#### Managing remote notifications

- [func didRegisterForRemoteNotifications(withDeviceToken: Data)](/documentation/watchkit/wkextensiondelegate/didregisterforremotenotifications(withdevicetoken:))
- [func didFailToRegisterForRemoteNotificationsWithError(any Error)](/documentation/watchkit/wkextensiondelegate/didfailtoregisterforremotenotificationswitherror(_:))
- [func didReceiveRemoteNotification([AnyHashable : Any], fetchCompletionHandler: (WKBackgroundFetchResult) -> Void)](/documentation/watchkit/wkextensiondelegate/didreceiveremotenotification(_:fetchcompletionhandler:))
- [WKBackgroundFetchResult](/documentation/watchkit/wkbackgroundfetchresult)

##### Fetch Results

- [case failed](/documentation/watchkit/wkbackgroundfetchresult/failed)
- [case newData](/documentation/watchkit/wkbackgroundfetchresult/newdata)
- [case noData](/documentation/watchkit/wkbackgroundfetchresult/nodata)

##### Initializers

- [init?(rawValue: UInt)](/documentation/watchkit/wkbackgroundfetchresult/init(rawvalue:))

#### Coordinating handoff activity

- [func handleUserActivity([AnyHashable : Any]?)](/documentation/watchkit/wkextensiondelegate/handleuseractivity(_:))
- [func handle(NSUserActivity)](/documentation/watchkit/wkextensiondelegate/handle(_:)-5pyj1)

#### Accepting CloudKit shares

- [func userDidAcceptCloudKitShare(with: CKShareMetadata)](/documentation/watchkit/wkextensiondelegate/userdidacceptcloudkitshare(with:))

#### Deprecated Methods

- [func didReceiveRemoteNotification([AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/didreceiveremotenotification(_:))
- [func didReceive(UILocalNotification)](/documentation/watchkit/wkextensiondelegate/didreceive(_:))
- [func handleAction(withIdentifier: String?, forRemoteNotification: [AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:forremotenotification:))
- [func handleAction(withIdentifier: String?, forRemoteNotification: [AnyHashable : Any], withResponseInfo: [AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:forremotenotification:withresponseinfo:))
- [func handleAction(withIdentifier: String?, for: UILocalNotification)](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:for:))
- [func handleAction(withIdentifier: String?, for: UILocalNotification, withResponseInfo: [AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:for:withresponseinfo:))

### Opening a URL resource

- [func openSystemURL(URL)](/documentation/watchkit/wkextension/opensystemurl(_:))

### Getting the interface controllers

- [var rootInterfaceController: WKInterfaceController?](/documentation/watchkit/wkextension/rootinterfacecontroller)
- [var visibleInterfaceController: WKInterfaceController?](/documentation/watchkit/wkextension/visibleinterfacecontroller)

### Managing the execution state

- [var applicationState: WKApplicationState](/documentation/watchkit/wkextension/applicationstate)
- [WKApplicationState](/documentation/watchkit/wkapplicationstate)

#### Constants

- [case active](/documentation/watchkit/wkapplicationstate/active)
- [case inactive](/documentation/watchkit/wkapplicationstate/inactive)
- [case background](/documentation/watchkit/wkapplicationstate/background)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkapplicationstate/init(rawvalue:))
- [var isApplicationRunningInDock: Bool](/documentation/watchkit/wkextension/isapplicationrunningindock)
- [func scheduleBackgroundRefresh(withPreferredDate: Date, userInfo: (any NSSecureCoding & NSObjectProtocol)?, scheduledCompletion: ((any Error)?) -> Void)](/documentation/watchkit/wkextension/schedulebackgroundrefresh(withpreferreddate:userinfo:scheduledcompletion:))
- [var isFrontmostTimeoutExtended: Bool](/documentation/watchkit/wkextension/isfrontmosttimeoutextended)

### Managing the user interface

- [var isAutorotating: Bool](/documentation/watchkit/wkextension/isautorotating)
- [var isAutorotated: Bool](/documentation/watchkit/wkextension/isautorotated)
- [var globalTintColor: UIColor](/documentation/watchkit/wkextension/globaltintcolor)
- [func enableWaterLock()](/documentation/watchkit/wkextension/enablewaterlock())

### Managing the snapshot

- [func scheduleSnapshotRefresh(withPreferredDate: Date, userInfo: (any NSSecureCoding & NSObjectProtocol)?, scheduledCompletion: ((any Error)?) -> Void)](/documentation/watchkit/wkextension/schedulesnapshotrefresh(withpreferreddate:userinfo:scheduledcompletion:))

### Observing messages from the notification center

- [class let applicationDidFinishLaunchingNotification: NSNotification.Name](/documentation/watchkit/wkextension/applicationdidfinishlaunchingnotification)
- [class let applicationDidBecomeActiveNotification: NSNotification.Name](/documentation/watchkit/wkextension/applicationdidbecomeactivenotification)
- [class let applicationWillResignActiveNotification: NSNotification.Name](/documentation/watchkit/wkextension/applicationwillresignactivenotification)
- [class let applicationWillEnterForegroundNotification: NSNotification.Name](/documentation/watchkit/wkextension/applicationwillenterforegroundnotification)
- [class let applicationDidEnterBackgroundNotification: NSNotification.Name](/documentation/watchkit/wkextension/applicationdidenterbackgroundnotification)

### Registering for remote notifications

- [func registerForRemoteNotifications()](/documentation/watchkit/wkextension/registerforremotenotifications())
- [func unregisterForRemoteNotifications()](/documentation/watchkit/wkextension/unregisterforremotenotifications())
- [var isRegisteredForRemoteNotifications: Bool](/documentation/watchkit/wkextension/isregisteredforremotenotifications)
- [WKExtensionDelegate](/documentation/watchkit/wkextensiondelegate)

### Monitoring state changes

- [Working with the watchOS app life cycle](/documentation/watchkit/working-with-the-watchos-app-life-cycle)
- [func applicationDidFinishLaunching()](/documentation/watchkit/wkextensiondelegate/applicationdidfinishlaunching())
- [func applicationDidBecomeActive()](/documentation/watchkit/wkextensiondelegate/applicationdidbecomeactive())
- [func applicationWillResignActive()](/documentation/watchkit/wkextensiondelegate/applicationwillresignactive())
- [func applicationWillEnterForeground()](/documentation/watchkit/wkextensiondelegate/applicationwillenterforeground())
- [func applicationDidEnterBackground()](/documentation/watchkit/wkextensiondelegate/applicationdidenterbackground())
- [func deviceOrientationDidChange()](/documentation/watchkit/wkextensiondelegate/deviceorientationdidchange())

### Responding to intents

- [func handle(INIntent, completionHandler: (INIntentResponse) -> Void)](/documentation/watchkit/wkextensiondelegate/handle(_:completionhandler:))

### Setup Now Playing interface

- [func handleRemoteNowPlayingActivity()](/documentation/watchkit/wkextensiondelegate/handleremotenowplayingactivity())

### Handling a workout session

- [func handle(HKWorkoutConfiguration)](/documentation/watchkit/wkextensiondelegate/handle(_:)-f27i)
- [func handleActiveWorkoutRecovery()](/documentation/watchkit/wkextensiondelegate/handleactiveworkoutrecovery())

### Handling background tasks

- [func handle(Set<WKRefreshBackgroundTask>)](/documentation/watchkit/wkextensiondelegate/handle(_:)-92ulv)

### Handling extended runtime sessions

- [func handle(WKExtendedRuntimeSession)](/documentation/watchkit/wkextensiondelegate/handle(_:)-4qxgv)

### Managing remote notifications

- [func didRegisterForRemoteNotifications(withDeviceToken: Data)](/documentation/watchkit/wkextensiondelegate/didregisterforremotenotifications(withdevicetoken:))
- [func didFailToRegisterForRemoteNotificationsWithError(any Error)](/documentation/watchkit/wkextensiondelegate/didfailtoregisterforremotenotificationswitherror(_:))
- [func didReceiveRemoteNotification([AnyHashable : Any], fetchCompletionHandler: (WKBackgroundFetchResult) -> Void)](/documentation/watchkit/wkextensiondelegate/didreceiveremotenotification(_:fetchcompletionhandler:))
- [WKBackgroundFetchResult](/documentation/watchkit/wkbackgroundfetchresult)

#### Fetch Results

- [case failed](/documentation/watchkit/wkbackgroundfetchresult/failed)
- [case newData](/documentation/watchkit/wkbackgroundfetchresult/newdata)
- [case noData](/documentation/watchkit/wkbackgroundfetchresult/nodata)

#### Initializers

- [init?(rawValue: UInt)](/documentation/watchkit/wkbackgroundfetchresult/init(rawvalue:))

### Coordinating handoff activity

- [func handleUserActivity([AnyHashable : Any]?)](/documentation/watchkit/wkextensiondelegate/handleuseractivity(_:))
- [func handle(NSUserActivity)](/documentation/watchkit/wkextensiondelegate/handle(_:)-5pyj1)

### Accepting CloudKit shares

- [func userDidAcceptCloudKitShare(with: CKShareMetadata)](/documentation/watchkit/wkextensiondelegate/userdidacceptcloudkitshare(with:))

### Deprecated Methods

- [func didReceiveRemoteNotification([AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/didreceiveremotenotification(_:))
- [func didReceive(UILocalNotification)](/documentation/watchkit/wkextensiondelegate/didreceive(_:))
- [func handleAction(withIdentifier: String?, forRemoteNotification: [AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:forremotenotification:))
- [func handleAction(withIdentifier: String?, forRemoteNotification: [AnyHashable : Any], withResponseInfo: [AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:forremotenotification:withresponseinfo:))
- [func handleAction(withIdentifier: String?, for: UILocalNotification)](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:for:))
- [func handleAction(withIdentifier: String?, for: UILocalNotification, withResponseInfo: [AnyHashable : Any])](/documentation/watchkit/wkextensiondelegate/handleaction(withidentifier:for:withresponseinfo:))
- [func WKApplicationMain(Int32, UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>, String?) -> Int32](/documentation/watchkit/wkapplicationmain(_:_:_:))
- [WKInterfaceDevice](/documentation/watchkit/wkinterfacedevice)

### Accessing the Shared Device Object

- [class func current() -> WKInterfaceDevice](/documentation/watchkit/wkinterfacedevice/current())

### Reading the Screen Information

- [var screenBounds: CGRect](/documentation/watchkit/wkinterfacedevice/screenbounds)
- [var screenScale: CGFloat](/documentation/watchkit/wkinterfacedevice/screenscale)

### Reading the Device Settings

- [var name: String](/documentation/watchkit/wkinterfacedevice/name)
- [var model: String](/documentation/watchkit/wkinterfacedevice/model)
- [var localizedModel: String](/documentation/watchkit/wkinterfacedevice/localizedmodel)
- [var wristLocation: WKInterfaceDeviceWristLocation](/documentation/watchkit/wkinterfacedevice/wristlocation)
- [WKInterfaceDeviceWristLocation](/documentation/watchkit/wkinterfacedevicewristlocation)

#### Constants

- [case left](/documentation/watchkit/wkinterfacedevicewristlocation/left)
- [case right](/documentation/watchkit/wkinterfacedevicewristlocation/right)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacedevicewristlocation/init(rawvalue:))
- [var crownOrientation: WKInterfaceDeviceCrownOrientation](/documentation/watchkit/wkinterfacedevice/crownorientation)
- [WKInterfaceDeviceCrownOrientation](/documentation/watchkit/wkinterfacedevicecrownorientation)

#### Constants

- [case left](/documentation/watchkit/wkinterfacedevicecrownorientation/left)
- [case right](/documentation/watchkit/wkinterfacedevicecrownorientation/right)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacedevicecrownorientation/init(rawvalue:))
- [var preferredContentSizeCategory: String](/documentation/watchkit/wkinterfacedevice/preferredcontentsizecategory)

### Reading System Information

- [var systemName: String](/documentation/watchkit/wkinterfacedevice/systemname)
- [var systemVersion: String](/documentation/watchkit/wkinterfacedevice/systemversion)

### Accessing the Layout Direction

- [var layoutDirection: WKInterfaceLayoutDirection](/documentation/watchkit/wkinterfacedevice/layoutdirection)
- [class func interfaceLayoutDirection(for: WKInterfaceSemanticContentAttribute) -> WKInterfaceLayoutDirection](/documentation/watchkit/wkinterfacedevice/interfacelayoutdirection(for:))
- [WKInterfaceSemanticContentAttribute](/documentation/watchkit/wkinterfacesemanticcontentattribute)

#### Constants

- [case unspecified](/documentation/watchkit/wkinterfacesemanticcontentattribute/unspecified)
- [case playback](/documentation/watchkit/wkinterfacesemanticcontentattribute/playback)
- [case spatial](/documentation/watchkit/wkinterfacesemanticcontentattribute/spatial)
- [case forceLeftToRight](/documentation/watchkit/wkinterfacesemanticcontentattribute/forcelefttoright)
- [case forceRightToLeft](/documentation/watchkit/wkinterfacesemanticcontentattribute/forcerighttoleft)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacesemanticcontentattribute/init(rawvalue:))
- [WKInterfaceLayoutDirection](/documentation/watchkit/wkinterfacelayoutdirection)

#### Constants

- [case leftToRight](/documentation/watchkit/wkinterfacelayoutdirection/lefttoright)
- [case rightToLeft](/documentation/watchkit/wkinterfacelayoutdirection/righttoleft)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacelayoutdirection/init(rawvalue:))

### Reading Information About the Battery

- [var isBatteryMonitoringEnabled: Bool](/documentation/watchkit/wkinterfacedevice/isbatterymonitoringenabled)
- [var batteryLevel: Float](/documentation/watchkit/wkinterfacedevice/batterylevel)
- [var batteryState: WKInterfaceDeviceBatteryState](/documentation/watchkit/wkinterfacedevice/batterystate)
- [WKInterfaceDeviceBatteryState](/documentation/watchkit/wkinterfacedevicebatterystate)

#### Battery States

- [case charging](/documentation/watchkit/wkinterfacedevicebatterystate/charging)
- [case full](/documentation/watchkit/wkinterfacedevicebatterystate/full)
- [case unknown](/documentation/watchkit/wkinterfacedevicebatterystate/unknown)
- [case unplugged](/documentation/watchkit/wkinterfacedevicebatterystate/unplugged)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacedevicebatterystate/init(rawvalue:))

### Accessing Water Resistance and Lock

- [var waterResistanceRating: WKWaterResistanceRating](/documentation/watchkit/wkinterfacedevice/waterresistancerating)
- [WKWaterResistanceRating](/documentation/watchkit/wkwaterresistancerating)

#### Enumeration Cases

- [case ipx7](/documentation/watchkit/wkwaterresistancerating/ipx7)
- [case wr50](/documentation/watchkit/wkwaterresistancerating/wr50)
- [case wr100](/documentation/watchkit/wkwaterresistancerating/wr100)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkwaterresistancerating/init(rawvalue:))
- [var isWaterLockEnabled: Bool](/documentation/watchkit/wkinterfacedevice/iswaterlockenabled)
- [func enableWaterLock()](/documentation/watchkit/wkinterfacedevice/enablewaterlock())

### Playing Haptic Feedback

- [func play(WKHapticType)](/documentation/watchkit/wkinterfacedevice/play(_:))
- [WKHapticType](/documentation/watchkit/wkhaptictype)

#### Constants

- [case notification](/documentation/watchkit/wkhaptictype/notification)
- [case directionUp](/documentation/watchkit/wkhaptictype/directionup)
- [case directionDown](/documentation/watchkit/wkhaptictype/directiondown)
- [case success](/documentation/watchkit/wkhaptictype/success)
- [case failure](/documentation/watchkit/wkhaptictype/failure)
- [case retry](/documentation/watchkit/wkhaptictype/retry)
- [case start](/documentation/watchkit/wkhaptictype/start)
- [case stop](/documentation/watchkit/wkhaptictype/stop)
- [case click](/documentation/watchkit/wkhaptictype/click)
- [case navigationGenericManeuver](/documentation/watchkit/wkhaptictype/navigationgenericmaneuver)
- [case navigationLeftTurn](/documentation/watchkit/wkhaptictype/navigationleftturn)
- [case navigationRightTurn](/documentation/watchkit/wkhaptictype/navigationrightturn)

#### Enumeration Cases

- [case underwaterDepthCriticalPrompt](/documentation/watchkit/wkhaptictype/underwaterdepthcriticalprompt)
- [case underwaterDepthPrompt](/documentation/watchkit/wkhaptictype/underwaterdepthprompt)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkhaptictype/init(rawvalue:))

### Streaming Audio

- [var supportsAudioStreaming: Bool](/documentation/watchkit/wkinterfacedevice/supportsaudiostreaming)

### Validating In-App Purchases

- [var identifierForVendor: UUID?](/documentation/watchkit/wkinterfacedevice/identifierforvendor)
- [WKPrefersNetworkUponForeground](/documentation/bundleresources/information-property-list/wkprefersnetworkuponforeground)

## Runtime management

- [Background execution](/documentation/watchkit/background-execution)

### Background tasks

- [Using background tasks](/documentation/watchkit/using-background-tasks)
- [Preparing to take your watchOS app’s snapshot](/documentation/watchkit/preparing-to-take-your-watchos-app-s-snapshot)
- [WKApplicationRefreshBackgroundTask](/documentation/watchkit/wkapplicationrefreshbackgroundtask)
- [WKURLSessionRefreshBackgroundTask](/documentation/watchkit/wkurlsessionrefreshbackgroundtask)

#### Accessing background task data

- [var sessionIdentifier: String](/documentation/watchkit/wkurlsessionrefreshbackgroundtask/sessionidentifier)
- [WKWatchConnectivityRefreshBackgroundTask](/documentation/watchkit/wkwatchconnectivityrefreshbackgroundtask)
- [WKBluetoothAlertRefreshBackgroundTask](/documentation/watchkit/wkbluetoothalertrefreshbackgroundtask)
- [WKIntentDidRunRefreshBackgroundTask](/documentation/watchkit/wkintentdidrunrefreshbackgroundtask)
- [WKRelevantShortcutRefreshBackgroundTask](/documentation/watchkit/wkrelevantshortcutrefreshbackgroundtask)
- [WKSnapshotRefreshBackgroundTask](/documentation/watchkit/wksnapshotrefreshbackgroundtask)

#### Completing the background task

- [func setTaskCompleted(restoredDefaultState: Bool, estimatedSnapshotExpiration: Date?, userInfo: (any NSSecureCoding & NSObjectProtocol)?)](/documentation/watchkit/wksnapshotrefreshbackgroundtask/settaskcompleted(restoreddefaultstate:estimatedsnapshotexpiration:userinfo:))

#### Instance properties

- [var reasonForSnapshot: WKSnapshotReason](/documentation/watchkit/wksnapshotrefreshbackgroundtask/reasonforsnapshot)
- [WKSnapshotReason](/documentation/watchkit/wksnapshotreason)

##### Enumeration Cases

- [case appBackgrounded](/documentation/watchkit/wksnapshotreason/appbackgrounded)
- [case appScheduled](/documentation/watchkit/wksnapshotreason/appscheduled)
- [case complicationUpdate](/documentation/watchkit/wksnapshotreason/complicationupdate)
- [case prelaunch](/documentation/watchkit/wksnapshotreason/prelaunch)
- [case returnToDefaultState](/documentation/watchkit/wksnapshotreason/returntodefaultstate)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wksnapshotreason/init(rawvalue:))
- [var returnToDefaultState: Bool](/documentation/watchkit/wksnapshotrefreshbackgroundtask/returntodefaultstate)
- [WKRefreshBackgroundTask](/documentation/watchkit/wkrefreshbackgroundtask)

#### Accessing background task data

- [var userInfo: (any NSSecureCoding & NSObjectProtocol)?](/documentation/watchkit/wkrefreshbackgroundtask/userinfo)

#### Completing the background task

- [var expirationHandler: (() -> Void)?](/documentation/watchkit/wkrefreshbackgroundtask/expirationhandler)
- [func setTaskCompletedWithSnapshot(Bool)](/documentation/watchkit/wkrefreshbackgroundtask/settaskcompletedwithsnapshot(_:))
- [func setTaskCompleted()](/documentation/watchkit/wkrefreshbackgroundtask/settaskcompleted())

### Background sessions

- [Enabling Background Sessions](/documentation/watchkit/enabling-background-sessions)
- [Playing Background Audio](/documentation/watchkit/playing-background-audio)
- [WKBackgroundModes](/documentation/bundleresources/information-property-list/wkbackgroundmodes)
- [UIBackgroundModes](/documentation/bundleresources/information-property-list/uibackgroundmodes)
- [Life cycles](/documentation/watchkit/life-cycles)

### Responding to life cycle events

- [Handling Common State Transitions](/documentation/watchkit/handling-common-state-transitions)
- [Working with the watchOS app life cycle](/documentation/watchkit/working-with-the-watchos-app-life-cycle)
- [Handling User Activity](/documentation/watchkit/handling-user-activity)
- [Taking Advantage of Frontmost App State](/documentation/watchkit/taking-advantage-of-frontmost-app-state)
- [Using extended runtime sessions](/documentation/watchkit/using-extended-runtime-sessions)
- [WKExtendedRuntimeSession](/documentation/watchkit/wkextendedruntimesession)

### Creating a Session

- [var delegate: (any WKExtendedRuntimeSessionDelegate)?](/documentation/watchkit/wkextendedruntimesession/delegate)
- [WKExtendedRuntimeSessionDelegate](/documentation/watchkit/wkextendedruntimesessiondelegate)

#### Monitoring State Changes

- [func extendedRuntimeSessionDidStart(WKExtendedRuntimeSession)](/documentation/watchkit/wkextendedruntimesessiondelegate/extendedruntimesessiondidstart(_:))
- [func extendedRuntimeSessionWillExpire(WKExtendedRuntimeSession)](/documentation/watchkit/wkextendedruntimesessiondelegate/extendedruntimesessionwillexpire(_:))
- [func extendedRuntimeSession(WKExtendedRuntimeSession, didInvalidateWith: WKExtendedRuntimeSessionInvalidationReason, error: (any Error)?)](/documentation/watchkit/wkextendedruntimesessiondelegate/extendedruntimesession(_:didinvalidatewith:error:))
- [WKExtendedRuntimeSessionInvalidationReason](/documentation/watchkit/wkextendedruntimesessioninvalidationreason)

##### Invalidation Reasons

- [case error](/documentation/watchkit/wkextendedruntimesessioninvalidationreason/error)
- [case none](/documentation/watchkit/wkextendedruntimesessioninvalidationreason/none)
- [case sessionInProgress](/documentation/watchkit/wkextendedruntimesessioninvalidationreason/sessioninprogress)
- [case expired](/documentation/watchkit/wkextendedruntimesessioninvalidationreason/expired)
- [case resignedFrontmost](/documentation/watchkit/wkextendedruntimesessioninvalidationreason/resignedfrontmost)
- [case suppressedBySystem](/documentation/watchkit/wkextendedruntimesessioninvalidationreason/suppressedbysystem)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkextendedruntimesessioninvalidationreason/init(rawvalue:))

### Managing the Session State

- [func start()](/documentation/watchkit/wkextendedruntimesession/start())
- [func start(at: Date)](/documentation/watchkit/wkextendedruntimesession/start(at:))
- [func invalidate()](/documentation/watchkit/wkextendedruntimesession/invalidate())
- [var state: WKExtendedRuntimeSessionState](/documentation/watchkit/wkextendedruntimesession/state)
- [WKExtendedRuntimeSessionState](/documentation/watchkit/wkextendedruntimesessionstate)

#### Session States

- [case notStarted](/documentation/watchkit/wkextendedruntimesessionstate/notstarted)
- [case scheduled](/documentation/watchkit/wkextendedruntimesessionstate/scheduled)
- [case running](/documentation/watchkit/wkextendedruntimesessionstate/running)
- [case invalid](/documentation/watchkit/wkextendedruntimesessionstate/invalid)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkextendedruntimesessionstate/init(rawvalue:))
- [var expirationDate: Date?](/documentation/watchkit/wkextendedruntimesession/expirationdate)
- [class func requestAutoLaunchAuthorizationStatus(completion: (WKExtendedRuntimeSessionAutoLaunchAuthorizationStatus, (any Error)?) -> Void)](/documentation/watchkit/wkextendedruntimesession/requestautolaunchauthorizationstatus(completion:))
- [WKExtendedRuntimeSessionAutoLaunchAuthorizationStatus](/documentation/watchkit/wkextendedruntimesessionautolaunchauthorizationstatus)

#### Enumeration Cases

- [case active](/documentation/watchkit/wkextendedruntimesessionautolaunchauthorizationstatus/active)
- [case inactive](/documentation/watchkit/wkextendedruntimesessionautolaunchauthorizationstatus/inactive)
- [case unknown](/documentation/watchkit/wkextendedruntimesessionautolaunchauthorizationstatus/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkextendedruntimesessionautolaunchauthorizationstatus/init(rawvalue:))

### Alerting the User

- [func notifyUser(hapticType: WKHapticType, repeatHandler: ((UnsafeMutablePointer<WKHapticType>) -> TimeInterval)?)](/documentation/watchkit/wkextendedruntimesession/notifyuser(haptictype:repeathandler:))

### Handling Errors

- [WKExtendedRuntimeSessionErrorCode](/documentation/watchkit/wkextendedruntimesessionerrorcode)

#### Error Codes

- [case unknown](/documentation/watchkit/wkextendedruntimesessionerrorcode/unknown)
- [case scheduledTooFarInAdvance](/documentation/watchkit/wkextendedruntimesessionerrorcode/scheduledtoofarinadvance)
- [case mustBeActiveToStartOrSchedule](/documentation/watchkit/wkextendedruntimesessionerrorcode/mustbeactivetostartorschedule)
- [case notYetStarted](/documentation/watchkit/wkextendedruntimesessionerrorcode/notyetstarted)
- [case exceededResourceLimits](/documentation/watchkit/wkextendedruntimesessionerrorcode/exceededresourcelimits)
- [case barDisabled](/documentation/watchkit/wkextendedruntimesessionerrorcode/bardisabled)
- [case notApprovedToStartSession](/documentation/watchkit/wkextendedruntimesessionerrorcode/notapprovedtostartsession)
- [case notApprovedToSchedule](/documentation/watchkit/wkextendedruntimesessionerrorcode/notapprovedtoschedule)

#### Enumeration Cases

- [case mustBeActiveToPrompt](/documentation/watchkit/wkextendedruntimesessionerrorcode/mustbeactivetoprompt)
- [case unsupportedSessionType](/documentation/watchkit/wkextendedruntimesessionerrorcode/unsupportedsessiontype)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkextendedruntimesessionerrorcode/init(rawvalue:))
- [let WKExtendedRuntimeSessionErrorDomain: String](/documentation/watchkit/wkextendedruntimesessionerrordomain)
- [Interacting with Bluetooth peripherals during background app refresh](/documentation/watchkit/interacting-with-bluetooth-peripherals-during-background-app-refresh)

## User interface

- [Storyboard support](/documentation/watchkit/storyboard-support)

### User interface basics

- [Building watchOS app Interfaces Using the Storyboard](/documentation/watchkit/building-watchos-app-interfaces-using-the-storyboard)

#### Controls

- [Connecting Your User Interface to Your Code](/documentation/watchkit/connecting-your-user-interface-to-your-code)

#### Navigation

- [Navigating Between Scenes](/documentation/watchkit/navigating-between-scenes)
- [WKInterfaceObject](/documentation/watchkit/wkinterfaceobject)

#### Hiding and Showing an Object

- [func setHidden(Bool)](/documentation/watchkit/wkinterfaceobject/sethidden(_:))
- [func setAlpha(CGFloat)](/documentation/watchkit/wkinterfaceobject/setalpha(_:))

#### Getting the Property Name

- [var interfaceProperty: String](/documentation/watchkit/wkinterfaceobject/interfaceproperty)

#### Changing an Object’s Size

- [func setWidth(CGFloat)](/documentation/watchkit/wkinterfaceobject/setwidth(_:))
- [func setHeight(CGFloat)](/documentation/watchkit/wkinterfaceobject/setheight(_:))
- [func setRelativeWidth(CGFloat, withAdjustment: CGFloat)](/documentation/watchkit/wkinterfaceobject/setrelativewidth(_:withadjustment:))
- [func setRelativeHeight(CGFloat, withAdjustment: CGFloat)](/documentation/watchkit/wkinterfaceobject/setrelativeheight(_:withadjustment:))
- [func sizeToFitWidth()](/documentation/watchkit/wkinterfaceobject/sizetofitwidth())
- [func sizeToFitHeight()](/documentation/watchkit/wkinterfaceobject/sizetofitheight())

#### Setting an Object’s Alignment

- [func setHorizontalAlignment(WKInterfaceObjectHorizontalAlignment)](/documentation/watchkit/wkinterfaceobject/sethorizontalalignment(_:))
- [func setVerticalAlignment(WKInterfaceObjectVerticalAlignment)](/documentation/watchkit/wkinterfaceobject/setverticalalignment(_:))

#### Configuring the Accessibility Attributes

- [func setAccessibilityIdentifier(String?)](/documentation/watchkit/wkinterfaceobject/setaccessibilityidentifier(_:))
- [func setAccessibilityLabel(String?)](/documentation/watchkit/wkinterfaceobject/setaccessibilitylabel(_:))
- [func setAccessibilityHint(String?)](/documentation/watchkit/wkinterfaceobject/setaccessibilityhint(_:))
- [func setAccessibilityValue(String?)](/documentation/watchkit/wkinterfaceobject/setaccessibilityvalue(_:))
- [func setIsAccessibilityElement(Bool)](/documentation/watchkit/wkinterfaceobject/setisaccessibilityelement(_:))
- [func setAccessibilityTraits(UIAccessibilityTraits)](/documentation/watchkit/wkinterfaceobject/setaccessibilitytraits(_:))
- [func setAccessibilityImageRegions([WKAccessibilityImageRegion])](/documentation/watchkit/wkinterfaceobject/setaccessibilityimageregions(_:))

#### Setting the Layout Direction

- [func setSemanticContentAttribute(WKInterfaceSemanticContentAttribute)](/documentation/watchkit/wkinterfaceobject/setsemanticcontentattribute(_:))

#### Constants

- [WKInterfaceObjectHorizontalAlignment](/documentation/watchkit/wkinterfaceobjecthorizontalalignment)

##### Constants

- [case left](/documentation/watchkit/wkinterfaceobjecthorizontalalignment/left)
- [case center](/documentation/watchkit/wkinterfaceobjecthorizontalalignment/center)
- [case right](/documentation/watchkit/wkinterfaceobjecthorizontalalignment/right)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfaceobjecthorizontalalignment/init(rawvalue:))
- [WKInterfaceObjectVerticalAlignment](/documentation/watchkit/wkinterfaceobjectverticalalignment)

##### Constants

- [case top](/documentation/watchkit/wkinterfaceobjectverticalalignment/top)
- [case center](/documentation/watchkit/wkinterfaceobjectverticalalignment/center)
- [case bottom](/documentation/watchkit/wkinterfaceobjectverticalalignment/bottom)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfaceobjectverticalalignment/init(rawvalue:))
- [WKInterfaceController](/documentation/watchkit/wkinterfacecontroller)

#### Creating the interface controller

- [init()](/documentation/watchkit/wkinterfacecontroller/init())
- [func awake(withContext: Any?)](/documentation/watchkit/wkinterfacecontroller/awake(withcontext:))
- [func setTitle(String?)](/documentation/watchkit/wkinterfacecontroller/settitle(_:))

#### Responding to activation and appearance events

- [func willActivate()](/documentation/watchkit/wkinterfacecontroller/willactivate())
- [func didDeactivate()](/documentation/watchkit/wkinterfacecontroller/diddeactivate())
- [func didAppear()](/documentation/watchkit/wkinterfacecontroller/didappear())
- [func willDisappear()](/documentation/watchkit/wkinterfacecontroller/willdisappear())

#### Implementing a navigation interface

- [func pushController(withName: String, context: Any?)](/documentation/watchkit/wkinterfacecontroller/pushcontroller(withname:context:))
- [func pop()](/documentation/watchkit/wkinterfacecontroller/pop())
- [func popToRootController()](/documentation/watchkit/wkinterfacecontroller/poptorootcontroller())

#### Presenting interface controllers modally

- [func presentController(withName: String, context: Any?)](/documentation/watchkit/wkinterfacecontroller/presentcontroller(withname:context:))
- [func presentController(withNames: [String], contexts: [Any]?)](/documentation/watchkit/wkinterfacecontroller/presentcontroller(withnames:contexts:))
- [func presentController(withNamesAndContexts: [(name: String, context: AnyObject)])](/documentation/watchkit/wkinterfacecontroller/presentcontroller(withnamesandcontexts:))
- [func presentAlert(withTitle: String?, message: String?, preferredStyle: WKAlertControllerStyle, actions: [WKAlertAction])](/documentation/watchkit/wkinterfacecontroller/presentalert(withtitle:message:preferredstyle:actions:))
- [WKAlertControllerStyle](/documentation/watchkit/wkalertcontrollerstyle)

##### Constants

- [case alert](/documentation/watchkit/wkalertcontrollerstyle/alert)
- [case sideBySideButtonsAlert](/documentation/watchkit/wkalertcontrollerstyle/sidebysidebuttonsalert)
- [case actionSheet](/documentation/watchkit/wkalertcontrollerstyle/actionsheet)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkalertcontrollerstyle/init(rawvalue:))
- [func dismiss()](/documentation/watchkit/wkinterfacecontroller/dismiss())

#### Navigating a page-based interface

- [class func reloadRootPageControllers(withNames: [String], contexts: [Any]?, orientation: WKPageOrientation, pageIndex: Int)](/documentation/watchkit/wkinterfacecontroller/reloadrootpagecontrollers(withnames:contexts:orientation:pageindex:))
- [WKPageOrientation](/documentation/watchkit/wkpageorientation)

##### Enumeration Cases

- [case horizontal](/documentation/watchkit/wkpageorientation/horizontal)
- [case vertical](/documentation/watchkit/wkpageorientation/vertical)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkpageorientation/init(rawvalue:))
- [class func reloadRootControllers(withNamesAndContexts: [(name: String, context: AnyObject)])](/documentation/watchkit/wkinterfacecontroller/reloadrootcontrollers(withnamesandcontexts:))
- [func becomeCurrentPage()](/documentation/watchkit/wkinterfacecontroller/becomecurrentpage())

#### Managing segue-based transitions

- [func contextForSegue(withIdentifier: String) -> Any?](/documentation/watchkit/wkinterfacecontroller/contextforsegue(withidentifier:))
- [func contextsForSegue(withIdentifier: String) -> [Any]?](/documentation/watchkit/wkinterfacecontroller/contextsforsegue(withidentifier:))
- [func contextForSegue(withIdentifier: String, in: WKInterfaceTable, rowIndex: Int) -> Any?](/documentation/watchkit/wkinterfacecontroller/contextforsegue(withidentifier:in:rowindex:))
- [func contextsForSegue(withIdentifier: String, in: WKInterfaceTable, rowIndex: Int) -> [Any]?](/documentation/watchkit/wkinterfacecontroller/contextsforsegue(withidentifier:in:rowindex:))

#### Managing Scrolling

- [func scroll(to: WKInterfaceObject, at: WKInterfaceScrollPosition, animated: Bool)](/documentation/watchkit/wkinterfacecontroller/scroll(to:at:animated:))
- [WKInterfaceScrollPosition](/documentation/watchkit/wkinterfacescrollposition)

##### Enumeration Cases

- [case bottom](/documentation/watchkit/wkinterfacescrollposition/bottom)
- [case centeredVertically](/documentation/watchkit/wkinterfacescrollposition/centeredvertically)
- [case top](/documentation/watchkit/wkinterfacescrollposition/top)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacescrollposition/init(rawvalue:))
- [func interfaceDidScrollToTop()](/documentation/watchkit/wkinterfacecontroller/interfacedidscrolltotop())
- [func interfaceOffsetDidScrollToTop()](/documentation/watchkit/wkinterfacecontroller/interfaceoffsetdidscrolltotop())
- [func interfaceOffsetDidScrollToBottom()](/documentation/watchkit/wkinterfacecontroller/interfaceoffsetdidscrolltobottom())
- [var isTableScrollingHapticFeedbackEnabled: Bool](/documentation/watchkit/wkinterfacecontroller/istablescrollinghapticfeedbackenabled)

#### Respecting safe areas and layout margins

- [var contentSafeAreaInsets: UIEdgeInsets](/documentation/watchkit/wkinterfacecontroller/contentsafeareainsets)
- [var systemMinimumLayoutMargins: NSDirectionalEdgeInsets](/documentation/watchkit/wkinterfacecontroller/systemminimumlayoutmargins)
- [var contentFrame: CGRect](/documentation/watchkit/wkinterfacecontroller/contentframe)

#### Animating changes to the interface

- [func animate(withDuration: TimeInterval, animations: () -> Void)](/documentation/watchkit/wkinterfacecontroller/animate(withduration:animations:))

#### Handling text input

- [func presentTextInputController(withSuggestions: [String]?, allowedInputMode: WKTextInputMode, completion: ([Any]?) -> Void)](/documentation/watchkit/wkinterfacecontroller/presenttextinputcontroller(withsuggestions:allowedinputmode:completion:))
- [func presentTextInputControllerWithSuggestions(forLanguage: ((String) -> [Any]?)?, allowedInputMode: WKTextInputMode, completion: ([Any]?) -> Void)](/documentation/watchkit/wkinterfacecontroller/presenttextinputcontrollerwithsuggestions(forlanguage:allowedinputmode:completion:))
- [func dismissTextInputController()](/documentation/watchkit/wkinterfacecontroller/dismisstextinputcontroller())
- [WKTextInputMode](/documentation/watchkit/wktextinputmode)

##### Constants

- [case plain](/documentation/watchkit/wktextinputmode/plain)
- [case allowEmoji](/documentation/watchkit/wktextinputmode/allowemoji)
- [case allowAnimatedEmoji](/documentation/watchkit/wktextinputmode/allowanimatedemoji)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wktextinputmode/init(rawvalue:))

#### Presenting video and audio interfaces

- [func presentMediaPlayerController(with: URL, options: [AnyHashable : Any]?, completion: (Bool, TimeInterval, (any Error)?) -> Void)](/documentation/watchkit/wkinterfacecontroller/presentmediaplayercontroller(with:options:completion:))
- [Media Player Options](/documentation/watchkit/media-player-options)

##### Constants

- [let WKMediaPlayerControllerOptionsAutoplayKey: String](/documentation/watchkit/wkmediaplayercontrolleroptionsautoplaykey)
- [let WKMediaPlayerControllerOptionsStartTimeKey: String](/documentation/watchkit/wkmediaplayercontrolleroptionsstarttimekey)
- [let WKMediaPlayerControllerOptionsVideoGravityKey: String](/documentation/watchkit/wkmediaplayercontrolleroptionsvideogravitykey)
- [let WKMediaPlayerControllerOptionsLoopsKey: String](/documentation/watchkit/wkmediaplayercontrolleroptionsloopskey)
- [func dismissMediaPlayerController()](/documentation/watchkit/wkinterfacecontroller/dismissmediaplayercontroller())
- [func presentAudioRecorderController(withOutputURL: URL, preset: WKAudioRecorderPreset, options: [AnyHashable : Any]?, completion: (Bool, (any Error)?) -> Void)](/documentation/watchkit/wkinterfacecontroller/presentaudiorecordercontroller(withoutputurl:preset:options:completion:))
- [WKAudioRecorderPreset](/documentation/watchkit/wkaudiorecorderpreset)

##### Constants

- [case narrowBandSpeech](/documentation/watchkit/wkaudiorecorderpreset/narrowbandspeech)
- [case wideBandSpeech](/documentation/watchkit/wkaudiorecorderpreset/widebandspeech)
- [case highQualityAudio](/documentation/watchkit/wkaudiorecorderpreset/highqualityaudio)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkaudiorecorderpreset/init(rawvalue:))
- [Audio Recording Options](/documentation/watchkit/audio-recording-options)

##### Constants

- [let WKAudioRecorderControllerOptionsActionTitleKey: String](/documentation/watchkit/wkaudiorecordercontrolleroptionsactiontitlekey)
- [let WKAudioRecorderControllerOptionsAlwaysShowActionTitleKey: String](/documentation/watchkit/wkaudiorecordercontrolleroptionsalwaysshowactiontitlekey)
- [let WKAudioRecorderControllerOptionsAutorecordKey: String](/documentation/watchkit/wkaudiorecordercontrolleroptionsautorecordkey)
- [let WKAudioRecorderControllerOptionsMaximumDurationKey: String](/documentation/watchkit/wkaudiorecordercontrolleroptionsmaximumdurationkey)
- [func dismissAudioRecorderController()](/documentation/watchkit/wkinterfacecontroller/dismissaudiorecordercontroller())

#### Handling table-row selections

- [func table(WKInterfaceTable, didSelectRowAt: Int)](/documentation/watchkit/wkinterfacecontroller/table(_:didselectrowat:))

#### Managing pickers

- [func pickerDidFocus(WKInterfacePicker)](/documentation/watchkit/wkinterfacecontroller/pickerdidfocus(_:))
- [func pickerDidResignFocus(WKInterfacePicker)](/documentation/watchkit/wkinterfacecontroller/pickerdidresignfocus(_:))
- [func pickerDidSettle(WKInterfacePicker)](/documentation/watchkit/wkinterfacecontroller/pickerdidsettle(_:))

#### Getting the crown sequencer

- [var crownSequencer: WKCrownSequencer](/documentation/watchkit/wkinterfacecontroller/crownsequencer)

#### Coordinating Handoff activity

- [func update(NSUserActivity)](/documentation/watchkit/wkinterfacecontroller/update(_:))
- [func invalidateUserActivity()](/documentation/watchkit/wkinterfacecontroller/invalidateuseractivity())

#### Adding PassKit passes

- [func presentAddPassesController(withPasses: [PKPass], completion: () -> Void)](/documentation/watchkit/wkinterfacecontroller/presentaddpassescontroller(withpasses:completion:))
- [func dismissAddPassesController()](/documentation/watchkit/wkinterfacecontroller/dismissaddpassescontroller())

#### Managing Notifications

- [let WKAccessibilityVoiceOverStatusChanged: String](/documentation/watchkit/wkaccessibilityvoiceoverstatuschanged)

#### Deprecated symbols

- [Text Response Key](/documentation/watchkit/text-response-key)

##### Constants

- [let UIUserNotificationActionResponseTypedTextKey: String](/documentation/uikit/uiusernotificationactionresponsetypedtextkey)
- [func addMenuItem(withImageNamed: String, title: String, action: Selector)](/documentation/watchkit/wkinterfacecontroller/addmenuitem(withimagenamed:title:action:))
- [func addMenuItem(with: WKMenuItemIcon, title: String, action: Selector)](/documentation/watchkit/wkinterfacecontroller/addmenuitem(with:title:action:)-6pb4t)
- [func addMenuItem(with: UIImage, title: String, action: Selector)](/documentation/watchkit/wkinterfacecontroller/addmenuitem(with:title:action:)-1q2zj)
- [func beginGlanceUpdates()](/documentation/watchkit/wkinterfacecontroller/beginglanceupdates())
- [func clearAllMenuItems()](/documentation/watchkit/wkinterfacecontroller/clearallmenuitems())
- [func endGlanceUpdates()](/documentation/watchkit/wkinterfacecontroller/endglanceupdates())
- [func handleUserActivity([AnyHashable : Any]?)](/documentation/watchkit/wkinterfacecontroller/handleuseractivity(_:))
- [func presentController([(name: String, context: AnyObject)])](/documentation/watchkit/wkinterfacecontroller/presentcontroller(_:))
- [class func reloadRootControllers(withNames: [String], contexts: [Any]?)](/documentation/watchkit/wkinterfacecontroller/reloadrootcontrollers(withnames:contexts:))
- [func updateUserActivity(String, userInfo: [AnyHashable : Any]?, webpageURL: URL?)](/documentation/watchkit/wkinterfacecontroller/updateuseractivity(_:userinfo:webpageurl:))
- [WKMenuItemIcon](/documentation/watchkit/wkmenuitemicon)

##### Constants

- [case accept](/documentation/watchkit/wkmenuitemicon/accept)
- [case add](/documentation/watchkit/wkmenuitemicon/add)
- [case block](/documentation/watchkit/wkmenuitemicon/block)
- [case decline](/documentation/watchkit/wkmenuitemicon/decline)
- [case info](/documentation/watchkit/wkmenuitemicon/info)
- [case maybe](/documentation/watchkit/wkmenuitemicon/maybe)
- [case more](/documentation/watchkit/wkmenuitemicon/more)
- [case mute](/documentation/watchkit/wkmenuitemicon/mute)
- [case pause](/documentation/watchkit/wkmenuitemicon/pause)
- [case play](/documentation/watchkit/wkmenuitemicon/play)
- [case `repeat`](/documentation/watchkit/wkmenuitemicon/repeat)
- [case resume](/documentation/watchkit/wkmenuitemicon/resume)
- [case share](/documentation/watchkit/wkmenuitemicon/share)
- [case shuffle](/documentation/watchkit/wkmenuitemicon/shuffle)
- [case speaker](/documentation/watchkit/wkmenuitemicon/speaker)
- [case trash](/documentation/watchkit/wkmenuitemicon/trash)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkmenuitemicon/init(rawvalue:))
- [WKAlertAction](/documentation/watchkit/wkalertaction)

#### Creating an Action

- [convenience init(title: String, style: WKAlertActionStyle, handler: WKAlertActionHandler)](/documentation/watchkit/wkalertaction/init(title:style:handler:))

#### Constants

- [WKAlertActionStyle](/documentation/watchkit/wkalertactionstyle)

##### Constants

- [case `default`](/documentation/watchkit/wkalertactionstyle/default)
- [case cancel](/documentation/watchkit/wkalertactionstyle/cancel)
- [case destructive](/documentation/watchkit/wkalertactionstyle/destructive)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkalertactionstyle/init(rawvalue:))
- [WKAlertActionHandler](/documentation/watchkit/wkalertactionhandler)
- [WKAccessibilityImageRegion](/documentation/watchkit/wkaccessibilityimageregion)

#### Getting the Region Attributes

- [var frame: CGRect](/documentation/watchkit/wkaccessibilityimageregion/frame)
- [var label: String](/documentation/watchkit/wkaccessibilityimageregion/label)
- [func WKAccessibilityIsVoiceOverRunning() -> Bool](/documentation/watchkit/wkaccessibilityisvoiceoverrunning())
- [func WKAccessibilityIsReduceMotionEnabled() -> Bool](/documentation/watchkit/wkaccessibilityisreducemotionenabled())

### Controls

- [WKInterfaceLabel](/documentation/watchkit/wkinterfacelabel)

#### Setting the Label Text

- [func setText(String?)](/documentation/watchkit/wkinterfacelabel/settext(_:))
- [func setTextColor(UIColor?)](/documentation/watchkit/wkinterfacelabel/settextcolor(_:))
- [func setAttributedText(NSAttributedString?)](/documentation/watchkit/wkinterfacelabel/setattributedtext(_:))
- [WKInterfaceDate](/documentation/watchkit/wkinterfacedate)

#### Configuring the Date and Time Display

- [func setTextColor(UIColor?)](/documentation/watchkit/wkinterfacedate/settextcolor(_:))
- [func setTimeZone(TimeZone?)](/documentation/watchkit/wkinterfacedate/settimezone(_:))
- [func setCalendar(Calendar?)](/documentation/watchkit/wkinterfacedate/setcalendar(_:))
- [WKInterfaceTimer](/documentation/watchkit/wkinterfacetimer)

#### Configuring the Timer Attributes

- [func setDate(Date)](/documentation/watchkit/wkinterfacetimer/setdate(_:))
- [func setTextColor(UIColor?)](/documentation/watchkit/wkinterfacetimer/settextcolor(_:))

#### Starting and Stopping the Timer

- [func start()](/documentation/watchkit/wkinterfacetimer/start())
- [func stop()](/documentation/watchkit/wkinterfacetimer/stop())
- [WKInterfaceButton](/documentation/watchkit/wkinterfacebutton)

#### Setting the Button Title

- [func setTitle(String?)](/documentation/watchkit/wkinterfacebutton/settitle(_:))
- [func setAttributedTitle(NSAttributedString?)](/documentation/watchkit/wkinterfacebutton/setattributedtitle(_:))

#### Setting the Button Background

- [func setBackgroundColor(UIColor?)](/documentation/watchkit/wkinterfacebutton/setbackgroundcolor(_:))
- [func setBackgroundImage(UIImage?)](/documentation/watchkit/wkinterfacebutton/setbackgroundimage(_:))
- [func setBackgroundImageData(Data?)](/documentation/watchkit/wkinterfacebutton/setbackgroundimagedata(_:))
- [func setBackgroundImageNamed(String?)](/documentation/watchkit/wkinterfacebutton/setbackgroundimagenamed(_:))

#### Enabling and Disabling the Button

- [func setEnabled(Bool)](/documentation/watchkit/wkinterfacebutton/setenabled(_:))
- [WKInterfaceAuthorizationAppleIDButton](/documentation/watchkit/wkinterfaceauthorizationappleidbutton)

#### Initializing for SwiftUI

- [init(style: WKInterfaceAuthorizationAppleIDButton.Style, target: Any?, action: Selector)](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/init(style:target:action:))
- [WKInterfaceAuthorizationAppleIDButton.Style](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/style)

##### Styles

- [case `default`](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/style/default)
- [case white](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/style/white)
- [case `default`](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/style/default)
- [case white](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/style/white)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/style/init(rawvalue:))
- [init(target: Any?, action: Selector)](/documentation/watchkit/wkinterfaceauthorizationappleidbutton/init(target:action:))
- [WKInterfacePaymentButton](/documentation/watchkit/wkinterfacepaymentbutton)

#### Initializing for SwiftUI

- [init(target: Any?, action: Selector)](/documentation/watchkit/wkinterfacepaymentbutton/init(target:action:))
- [WKInterfaceTextField](/documentation/watchkit/wkinterfacetextfield)

#### Specifying the Content Type

- [func setTextContentType(WKTextContentType?)](/documentation/watchkit/wkinterfacetextfield/settextcontenttype(_:))
- [WKTextContentType](/documentation/watchkit/wktextcontenttype)

##### Name

- [static let name: WKTextContentType](/documentation/watchkit/wktextcontenttype/name)
- [static let namePrefix: WKTextContentType](/documentation/watchkit/wktextcontenttype/nameprefix)
- [static let givenName: WKTextContentType](/documentation/watchkit/wktextcontenttype/givenname)
- [static let middleName: WKTextContentType](/documentation/watchkit/wktextcontenttype/middlename)
- [static let familyName: WKTextContentType](/documentation/watchkit/wktextcontenttype/familyname)
- [static let nameSuffix: WKTextContentType](/documentation/watchkit/wktextcontenttype/namesuffix)
- [static let nickname: WKTextContentType](/documentation/watchkit/wktextcontenttype/nickname)

##### Employment

- [static let jobTitle: WKTextContentType](/documentation/watchkit/wktextcontenttype/jobtitle)
- [static let organizationName: WKTextContentType](/documentation/watchkit/wktextcontenttype/organizationname)

##### Address

- [static let location: WKTextContentType](/documentation/watchkit/wktextcontenttype/location)
- [static let fullStreetAddress: WKTextContentType](/documentation/watchkit/wktextcontenttype/fullstreetaddress)
- [static let streetAddressLine1: WKTextContentType](/documentation/watchkit/wktextcontenttype/streetaddressline1)
- [static let streetAddressLine2: WKTextContentType](/documentation/watchkit/wktextcontenttype/streetaddressline2)
- [static let addressCity: WKTextContentType](/documentation/watchkit/wktextcontenttype/addresscity)
- [static let addressState: WKTextContentType](/documentation/watchkit/wktextcontenttype/addressstate)
- [static let addressCityAndState: WKTextContentType](/documentation/watchkit/wktextcontenttype/addresscityandstate)
- [static let sublocality: WKTextContentType](/documentation/watchkit/wktextcontenttype/sublocality)
- [static let countryName: WKTextContentType](/documentation/watchkit/wktextcontenttype/countryname)
- [static let postalCode: WKTextContentType](/documentation/watchkit/wktextcontenttype/postalcode)

##### Contact Information

- [static let telephoneNumber: WKTextContentType](/documentation/watchkit/wktextcontenttype/telephonenumber)
- [static let emailAddress: WKTextContentType](/documentation/watchkit/wktextcontenttype/emailaddress)

##### Other

- [static let URL: WKTextContentType](/documentation/watchkit/wktextcontenttype/url)
- [static let creditCardNumber: WKTextContentType](/documentation/watchkit/wktextcontenttype/creditcardnumber)

##### Login Credentials

- [static let username: WKTextContentType](/documentation/watchkit/wktextcontenttype/username)
- [static let password: WKTextContentType](/documentation/watchkit/wktextcontenttype/password)
- [static let newPassword: WKTextContentType](/documentation/watchkit/wktextcontenttype/newpassword)
- [static let oneTimeCode: WKTextContentType](/documentation/watchkit/wktextcontenttype/onetimecode)

##### Initializers

- [init(rawValue: String)](/documentation/watchkit/wktextcontenttype/init(rawvalue:))

#### Setting the Text

- [func setText(String?)](/documentation/watchkit/wkinterfacetextfield/settext(_:))
- [func setAttributedText(NSAttributedString?)](/documentation/watchkit/wkinterfacetextfield/setattributedtext(_:))
- [func setTextColor(UIColor?)](/documentation/watchkit/wkinterfacetextfield/settextcolor(_:))

#### Setting a Placeholder

- [func setPlaceholder(String?)](/documentation/watchkit/wkinterfacetextfield/setplaceholder(_:))
- [func setAttributedPlaceholder(NSAttributedString?)](/documentation/watchkit/wkinterfacetextfield/setattributedplaceholder(_:))

#### Configuring the Control

- [func setEnabled(Bool)](/documentation/watchkit/wkinterfacetextfield/setenabled(_:))
- [func setSecureTextEntry(Bool)](/documentation/watchkit/wkinterfacetextfield/setsecuretextentry(_:))
- [WKInterfaceSwitch](/documentation/watchkit/wkinterfaceswitch)

#### Setting the Switch’s Title

- [func setTitle(String?)](/documentation/watchkit/wkinterfaceswitch/settitle(_:))
- [func setAttributedTitle(NSAttributedString?)](/documentation/watchkit/wkinterfaceswitch/setattributedtitle(_:))

#### Configuring the Switch

- [func setOn(Bool)](/documentation/watchkit/wkinterfaceswitch/seton(_:))
- [func setColor(UIColor?)](/documentation/watchkit/wkinterfaceswitch/setcolor(_:))

#### Enabling the Switch

- [func setEnabled(Bool)](/documentation/watchkit/wkinterfaceswitch/setenabled(_:))
- [WKInterfaceSlider](/documentation/watchkit/wkinterfaceslider)

#### Setting the Slider Value

- [func setValue(Float)](/documentation/watchkit/wkinterfaceslider/setvalue(_:))
- [func setColor(UIColor?)](/documentation/watchkit/wkinterfaceslider/setcolor(_:))
- [func setNumberOfSteps(Int)](/documentation/watchkit/wkinterfaceslider/setnumberofsteps(_:))

#### Enabling the Slider

- [func setEnabled(Bool)](/documentation/watchkit/wkinterfaceslider/setenabled(_:))
- [WKInterfaceActivityRing](/documentation/watchkit/wkinterfaceactivityring)

#### Setting the Activity Summary

- [func setActivitySummary(HKActivitySummary?, animated: Bool)](/documentation/watchkit/wkinterfaceactivityring/setactivitysummary(_:animated:))

#### Initializing for SwiftUI

- [init()](/documentation/watchkit/wkinterfaceactivityring/init())
- [WKInterfaceMap](/documentation/watchkit/wkinterfacemap)

#### Specifying the Map Region

- [func setVisibleMapRect(MKMapRect)](/documentation/watchkit/wkinterfacemap/setvisiblemaprect(_:))
- [func setRegion(MKCoordinateRegion)](/documentation/watchkit/wkinterfacemap/setregion(_:))

#### Managing Map Annotations

- [func addAnnotation(CLLocationCoordinate2D, with: UIImage?, centerOffset: CGPoint)](/documentation/watchkit/wkinterfacemap/addannotation(_:with:centeroffset:))
- [func addAnnotation(CLLocationCoordinate2D, withImageNamed: String?, centerOffset: CGPoint)](/documentation/watchkit/wkinterfacemap/addannotation(_:withimagenamed:centeroffset:))
- [func addAnnotation(CLLocationCoordinate2D, with: WKInterfaceMapPinColor)](/documentation/watchkit/wkinterfacemap/addannotation(_:with:))
- [WKInterfaceMapPinColor](/documentation/watchkit/wkinterfacemappincolor)

##### Constants

- [case red](/documentation/watchkit/wkinterfacemappincolor/red)
- [case green](/documentation/watchkit/wkinterfacemappincolor/green)
- [case purple](/documentation/watchkit/wkinterfacemappincolor/purple)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacemappincolor/init(rawvalue:))
- [func removeAllAnnotations()](/documentation/watchkit/wkinterfacemap/removeallannotations())

#### Displaying the User’s Location

- [func setShowsUserLocation(Bool)](/documentation/watchkit/wkinterfacemap/setshowsuserlocation(_:))
- [func setShowsUserHeading(Bool)](/documentation/watchkit/wkinterfacemap/setshowsuserheading(_:))
- [func setUserTrackingMode(WKInterfaceMap.UserTrackingMode, animated: Bool)](/documentation/watchkit/wkinterfacemap/setusertrackingmode(_:animated:))
- [WKInterfaceMap.UserTrackingMode](/documentation/watchkit/wkinterfacemap/usertrackingmode)

##### Tracking Modes

- [case follow](/documentation/watchkit/wkinterfacemap/usertrackingmode/follow)
- [case none](/documentation/watchkit/wkinterfacemap/usertrackingmode/none)
- [case follow](/documentation/watchkit/wkinterfacemap/usertrackingmode/follow)
- [case none](/documentation/watchkit/wkinterfacemap/usertrackingmode/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacemap/usertrackingmode/init(rawvalue:))

#### Initializing for SwiftUI

- [init()](/documentation/watchkit/wkinterfacemap/init())

### Containers

- [WKInterfaceGroup](/documentation/watchkit/wkinterfacegroup)

#### Setting the Group’s Content

- [func setBackgroundColor(UIColor?)](/documentation/watchkit/wkinterfacegroup/setbackgroundcolor(_:))
- [func setBackgroundImage(UIImage?)](/documentation/watchkit/wkinterfacegroup/setbackgroundimage(_:))
- [func setBackgroundImageData(Data?)](/documentation/watchkit/wkinterfacegroup/setbackgroundimagedata(_:))
- [func setBackgroundImageNamed(String?)](/documentation/watchkit/wkinterfacegroup/setbackgroundimagenamed(_:))

#### Setting the Layout Information

- [func setCornerRadius(CGFloat)](/documentation/watchkit/wkinterfacegroup/setcornerradius(_:))
- [func setContentInset(UIEdgeInsets)](/documentation/watchkit/wkinterfacegroup/setcontentinset(_:))
- [WKInterfaceSeparator](/documentation/watchkit/wkinterfaceseparator)

#### Configuring the Separator

- [func setColor(UIColor?)](/documentation/watchkit/wkinterfaceseparator/setcolor(_:))
- [WKInterfaceTable](/documentation/watchkit/wkinterfacetable)

#### Specifying the Row Types

- [func setRowTypes([String])](/documentation/watchkit/wkinterfacetable/setrowtypes(_:))
- [func setNumberOfRows(Int, withRowType: String)](/documentation/watchkit/wkinterfacetable/setnumberofrows(_:withrowtype:))

#### Getting the Row Controllers

- [var numberOfRows: Int](/documentation/watchkit/wkinterfacetable/numberofrows)
- [func rowController(at: Int) -> Any?](/documentation/watchkit/wkinterfacetable/rowcontroller(at:))

#### Inserting and Removing Rows

- [func insertRows(at: IndexSet, withRowType: String)](/documentation/watchkit/wkinterfacetable/insertrows(at:withrowtype:))
- [func removeRows(at: IndexSet)](/documentation/watchkit/wkinterfacetable/removerows(at:))

#### Scrolling

- [func scrollToRow(at: Int)](/documentation/watchkit/wkinterfacetable/scrolltorow(at:))
- [var curvesAtBottom: Bool](/documentation/watchkit/wkinterfacetable/curvesatbottom)
- [var curvesAtTop: Bool](/documentation/watchkit/wkinterfacetable/curvesattop)

#### Performing segues

- [func performSegue(forRow: Int)](/documentation/watchkit/wkinterfacetable/performsegue(forrow:))
- [WKInterfacePicker](/documentation/watchkit/wkinterfacepicker)

#### Managing the Picker Contents

- [func setItems([WKPickerItem]?)](/documentation/watchkit/wkinterfacepicker/setitems(_:))
- [WKPickerItem](/documentation/watchkit/wkpickeritem)

##### Setting the Picker Item’s Content

- [var contentImage: WKImage?](/documentation/watchkit/wkpickeritem/contentimage)
- [var title: String?](/documentation/watchkit/wkpickeritem/title)
- [var accessoryImage: WKImage?](/documentation/watchkit/wkpickeritem/accessoryimage)
- [var caption: String?](/documentation/watchkit/wkpickeritem/caption)
- [func setSelectedItemIndex(Int)](/documentation/watchkit/wkinterfacepicker/setselecteditemindex(_:))
- [func setCoordinatedAnimations([any WKInterfaceObject & WKImageAnimatable]?)](/documentation/watchkit/wkinterfacepicker/setcoordinatedanimations(_:))

#### Managing Input from the Digital Crown

- [func focus()](/documentation/watchkit/wkinterfacepicker/focus())
- [func resignFocus()](/documentation/watchkit/wkinterfacepicker/resignfocus())

#### Enabling and Disabling the Picker

- [func setEnabled(Bool)](/documentation/watchkit/wkinterfacepicker/setenabled(_:))

### Audio

- [Playing Background Audio](/documentation/watchkit/playing-background-audio)
- [Adding a Now Playing View](/documentation/watchkit/adding-a-now-playing-view)
- [WKInterfaceVolumeControl](/documentation/watchkit/wkinterfacevolumecontrol)

#### Setting the Tint Color

- [func setTintColor(UIColor?)](/documentation/watchkit/wkinterfacevolumecontrol/settintcolor(_:))

#### Managing Input from the Digital Crown

- [func focus()](/documentation/watchkit/wkinterfacevolumecontrol/focus())
- [func resignFocus()](/documentation/watchkit/wkinterfacevolumecontrol/resignfocus())

#### SwiftUI

- [init(origin: WKInterfaceVolumeControl.Origin)](/documentation/watchkit/wkinterfacevolumecontrol/init(origin:))
- [WKInterfaceVolumeControl.Origin](/documentation/watchkit/wkinterfacevolumecontrol/origin)

##### Audio Sources

- [case companion](/documentation/watchkit/wkinterfacevolumecontrol/origin/companion)
- [case local](/documentation/watchkit/wkinterfacevolumecontrol/origin/local)
- [case companion](/documentation/watchkit/wkinterfacevolumecontrol/origin/companion)
- [case local](/documentation/watchkit/wkinterfacevolumecontrol/origin/local)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkinterfacevolumecontrol/origin/init(rawvalue:))
- [PUICAutoLaunchAudioOptOut](/documentation/bundleresources/information-property-list/puicautolaunchaudiooptout)
- [WKAudioFilePlayer](/documentation/watchkit/wkaudiofileplayer)

#### Creating a Player

- [convenience init(playerItem: WKAudioFilePlayerItem)](/documentation/watchkit/wkaudiofileplayer/init(playeritem:))
- [func replaceCurrentItem(with: WKAudioFilePlayerItem?)](/documentation/watchkit/wkaudiofileplayer/replacecurrentitem(with:))

#### Configuring and Controlling Playback

- [func play()](/documentation/watchkit/wkaudiofileplayer/play())
- [func pause()](/documentation/watchkit/wkaudiofileplayer/pause())
- [var rate: Float](/documentation/watchkit/wkaudiofileplayer/rate)

#### Getting Information About the Player

- [var currentItem: WKAudioFilePlayerItem?](/documentation/watchkit/wkaudiofileplayer/currentitem)
- [var status: WKAudioFilePlayerStatus](/documentation/watchkit/wkaudiofileplayer/status)
- [var error: (any Error)?](/documentation/watchkit/wkaudiofileplayer/error)

#### Getting Timing Information

- [var currentTime: TimeInterval](/documentation/watchkit/wkaudiofileplayer/currenttime)

#### Constants

- [WKAudioFilePlayerStatus](/documentation/watchkit/wkaudiofileplayerstatus)

##### Constants

- [case unknown](/documentation/watchkit/wkaudiofileplayerstatus/unknown)
- [case readyToPlay](/documentation/watchkit/wkaudiofileplayerstatus/readytoplay)
- [case failed](/documentation/watchkit/wkaudiofileplayerstatus/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkaudiofileplayerstatus/init(rawvalue:))
- [WKAudioFileQueuePlayer](/documentation/watchkit/wkaudiofilequeueplayer)

#### Creating a Queue Player

- [convenience init(items: [WKAudioFilePlayerItem])](/documentation/watchkit/wkaudiofilequeueplayer/init(items:))

#### Managing Items

- [var items: [WKAudioFilePlayerItem]](/documentation/watchkit/wkaudiofilequeueplayer/items)
- [func advanceToNextItem()](/documentation/watchkit/wkaudiofilequeueplayer/advancetonextitem())
- [func appendItem(WKAudioFilePlayerItem)](/documentation/watchkit/wkaudiofilequeueplayer/appenditem(_:))
- [func removeItem(WKAudioFilePlayerItem)](/documentation/watchkit/wkaudiofilequeueplayer/removeitem(_:))
- [func removeAllItems()](/documentation/watchkit/wkaudiofilequeueplayer/removeallitems())
- [WKAudioFilePlayerItem](/documentation/watchkit/wkaudiofileplayeritem)

#### Creating a Player Item

- [init(asset: WKAudioFileAsset)](/documentation/watchkit/wkaudiofileplayeritem/init(asset:))

#### Getting Information About the Item

- [var asset: WKAudioFileAsset](/documentation/watchkit/wkaudiofileplayeritem/asset)
- [var status: WKAudioFilePlayerItemStatus](/documentation/watchkit/wkaudiofileplayeritem/status)
- [var error: (any Error)?](/documentation/watchkit/wkaudiofileplayeritem/error)

#### Managing the Playback Position

- [var currentTime: TimeInterval](/documentation/watchkit/wkaudiofileplayeritem/currenttime)
- [func setCurrentTime(TimeInterval)](/documentation/watchkit/wkaudiofileplayeritem/setcurrenttime(_:))

#### Accessing the Item’s Status

- [WKAudioFilePlayerItemStatus](/documentation/watchkit/wkaudiofileplayeritemstatus)

##### Statuses

- [case unknown](/documentation/watchkit/wkaudiofileplayeritemstatus/unknown)
- [case readyToPlay](/documentation/watchkit/wkaudiofileplayeritemstatus/readytoplay)
- [case failed](/documentation/watchkit/wkaudiofileplayeritemstatus/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkaudiofileplayeritemstatus/init(rawvalue:))
- [WKAudioFileAsset](/documentation/watchkit/wkaudiofileasset)

#### Creating an Asset

- [convenience init(url: URL)](/documentation/watchkit/wkaudiofileasset/init(url:))
- [convenience init(url: URL, title: String?, albumTitle: String?, artist: String?)](/documentation/watchkit/wkaudiofileasset/init(url:title:albumtitle:artist:))

#### Getting the Asset’s Properties

- [var url: URL](/documentation/watchkit/wkaudiofileasset/url)
- [var duration: TimeInterval](/documentation/watchkit/wkaudiofileasset/duration)
- [var title: String?](/documentation/watchkit/wkaudiofileasset/title)
- [var albumTitle: String?](/documentation/watchkit/wkaudiofileasset/albumtitle)
- [var artist: String?](/documentation/watchkit/wkaudiofileasset/artist)

### Images and movies

- [WKInterfaceImage](/documentation/watchkit/wkinterfaceimage)

#### Configuring the Image

- [func setImage(UIImage?)](/documentation/watchkit/wkinterfaceimage/setimage(_:))
- [func setImageData(Data?)](/documentation/watchkit/wkinterfaceimage/setimagedata(_:))
- [func setImageNamed(String?)](/documentation/watchkit/wkinterfaceimage/setimagenamed(_:))
- [func setTintColor(UIColor?)](/documentation/watchkit/wkinterfaceimage/settintcolor(_:))
- [WKImage](/documentation/watchkit/wkimage)

#### Creating Image Objects

- [convenience init(image: UIImage)](/documentation/watchkit/wkimage/init(image:))
- [convenience init(imageData: Data)](/documentation/watchkit/wkimage/init(imagedata:))
- [convenience init(imageName: String)](/documentation/watchkit/wkimage/init(imagename:))

#### Getting the Image Data

- [var image: UIImage?](/documentation/watchkit/wkimage/image)
- [var imageData: Data?](/documentation/watchkit/wkimage/imagedata)
- [var imageName: String?](/documentation/watchkit/wkimage/imagename)
- [WKImageAnimatable](/documentation/watchkit/wkimageanimatable)

#### Animating an Image Sequence

- [func startAnimating()](/documentation/watchkit/wkimageanimatable/startanimating())
- [func startAnimatingWithImages(in: NSRange, duration: TimeInterval, repeatCount: Int)](/documentation/watchkit/wkimageanimatable/startanimatingwithimages(in:duration:repeatcount:))
- [func stopAnimating()](/documentation/watchkit/wkimageanimatable/stopanimating())
- [WKInterfaceMovie](/documentation/watchkit/wkinterfacemovie)

#### Setting the Movie Attributes

- [func setMovieURL(URL)](/documentation/watchkit/wkinterfacemovie/setmovieurl(_:))
- [func setVideoGravity(WKVideoGravity)](/documentation/watchkit/wkinterfacemovie/setvideogravity(_:))
- [func setPosterImage(WKImage?)](/documentation/watchkit/wkinterfacemovie/setposterimage(_:))
- [func setLoops(Bool)](/documentation/watchkit/wkinterfacemovie/setloops(_:))

#### Initializing for SwiftUI

- [init()](/documentation/watchkit/wkinterfacemovie/init())
- [WKInterfaceInlineMovie](/documentation/watchkit/wkinterfaceinlinemovie)

#### Setting Movie Properties

- [func setAutoplays(Bool)](/documentation/watchkit/wkinterfaceinlinemovie/setautoplays(_:))
- [func setLoops(Bool)](/documentation/watchkit/wkinterfaceinlinemovie/setloops(_:))
- [func setMovieURL(URL)](/documentation/watchkit/wkinterfaceinlinemovie/setmovieurl(_:))
- [func setPosterImage(WKImage?)](/documentation/watchkit/wkinterfaceinlinemovie/setposterimage(_:))
- [func setVideoGravity(WKVideoGravity)](/documentation/watchkit/wkinterfaceinlinemovie/setvideogravity(_:))

#### Controlling Playback

- [func pause()](/documentation/watchkit/wkinterfaceinlinemovie/pause())
- [func play()](/documentation/watchkit/wkinterfaceinlinemovie/play())
- [func playFromBeginning()](/documentation/watchkit/wkinterfaceinlinemovie/playfrombeginning())

#### Initializing for SwiftUI

- [init()](/documentation/watchkit/wkinterfaceinlinemovie/init())
- [WKInterfaceHMCamera](/documentation/watchkit/wkinterfacehmcamera)

#### Setting the Camera Source

- [func setCameraSource(HMCameraSource?)](/documentation/watchkit/wkinterfacehmcamera/setcamerasource(_:))

#### Initializing for SwiftUI

- [init()](/documentation/watchkit/wkinterfacehmcamera/init())
- [WKVideoGravity](/documentation/watchkit/wkvideogravity)

#### Constants

- [case resizeAspect](/documentation/watchkit/wkvideogravity/resizeaspect)
- [case resizeAspectFill](/documentation/watchkit/wkvideogravity/resizeaspectfill)
- [case resize](/documentation/watchkit/wkvideogravity/resize)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkvideogravity/init(rawvalue:))

### Graphics and games

- [WKInterfaceSKScene](/documentation/watchkit/wkinterfaceskscene)

#### Displaying a Scene

- [var scene: SKScene?](/documentation/watchkit/wkinterfaceskscene/scene)
- [func presentScene(SKScene?)](/documentation/watchkit/wkinterfaceskscene/presentscene(_:))
- [func presentScene(SKScene, transition: SKTransition)](/documentation/watchkit/wkinterfaceskscene/presentscene(_:transition:))

#### Configuring the Scene in a Storyboard

- [Configuring a WatchKit Scene in a Storyboard](/documentation/watchkit/configuring-a-watchkit-scene-in-a-storyboard)

#### Controlling the Timing of a Scene’s Rendering

- [var preferredFramesPerSecond: Int](/documentation/watchkit/wkinterfaceskscene/preferredframespersecond)
- [var isPaused: Bool](/documentation/watchkit/wkinterfaceskscene/ispaused)

#### Snapshotting Nodes to a Texture

- [func texture(from: SKNode) -> SKTexture?](/documentation/watchkit/wkinterfaceskscene/texture(from:))
- [func texture(from: SKNode, crop: CGRect) -> SKTexture?](/documentation/watchkit/wkinterfaceskscene/texture(from:crop:))

#### Initializing for SwiftUI

- [init()](/documentation/watchkit/wkinterfaceskscene/init())
- [WKInterfaceSCNScene](/documentation/watchkit/wkinterfacescnscene)

#### Managing the SceneKit Scene

- [var antialiasingMode: SCNAntialiasingMode](/documentation/watchkit/wkinterfacescnscene/antialiasingmode)
- [var preferredFramesPerSecond: Int](/documentation/watchkit/wkinterfacescnscene/preferredframespersecond)
- [var scene: SCNScene?](/documentation/watchkit/wkinterfacescnscene/scene)
- [func snapshot() -> UIImage](/documentation/watchkit/wkinterfacescnscene/snapshot())

#### Initializing for SwiftUI

- [init()](/documentation/watchkit/wkinterfacescnscene/init())

### Event handling

- [WKCrownSequencer](/documentation/watchkit/wkcrownsequencer)

#### Getting the Current Crown Status

- [var rotationsPerSecond: Double](/documentation/watchkit/wkcrownsequencer/rotationspersecond)
- [var isIdle: Bool](/documentation/watchkit/wkcrownsequencer/isidle)

#### Accessing the Delegate

- [var delegate: (any WKCrownDelegate)?](/documentation/watchkit/wkcrownsequencer/delegate)

#### Managing the Focus

- [func focus()](/documentation/watchkit/wkcrownsequencer/focus())
- [func resignFocus()](/documentation/watchkit/wkcrownsequencer/resignfocus())

#### Managing Haptic Feedback

- [var isHapticFeedbackEnabled: Bool](/documentation/watchkit/wkcrownsequencer/ishapticfeedbackenabled)
- [WKCrownDelegate](/documentation/watchkit/wkcrowndelegate)

#### Receiving Crown Events

- [func crownDidRotate(WKCrownSequencer?, rotationalDelta: Double)](/documentation/watchkit/wkcrowndelegate/crowndidrotate(_:rotationaldelta:))
- [func crownDidBecomeIdle(WKCrownSequencer?)](/documentation/watchkit/wkcrowndelegate/crowndidbecomeidle(_:))
- [WKGestureRecognizer](/documentation/watchkit/wkgesturerecognizer)

#### Getting the Touch Information

- [func locationInObject() -> CGPoint](/documentation/watchkit/wkgesturerecognizer/locationinobject())
- [func objectBounds() -> CGRect](/documentation/watchkit/wkgesturerecognizer/objectbounds())

#### Getting the Gesture Recognizer’s State

- [var state: WKGestureRecognizerState](/documentation/watchkit/wkgesturerecognizer/state)
- [var isEnabled: Bool](/documentation/watchkit/wkgesturerecognizer/isenabled)

#### Constants

- [WKGestureRecognizerState](/documentation/watchkit/wkgesturerecognizerstate)

##### Enumeration Cases

- [case began](/documentation/watchkit/wkgesturerecognizerstate/began)
- [case cancelled](/documentation/watchkit/wkgesturerecognizerstate/cancelled)
- [case changed](/documentation/watchkit/wkgesturerecognizerstate/changed)
- [case ended](/documentation/watchkit/wkgesturerecognizerstate/ended)
- [case failed](/documentation/watchkit/wkgesturerecognizerstate/failed)
- [case possible](/documentation/watchkit/wkgesturerecognizerstate/possible)
- [case recognized](/documentation/watchkit/wkgesturerecognizerstate/recognized)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkgesturerecognizerstate/init(rawvalue:))
- [WKLongPressGestureRecognizer](/documentation/watchkit/wklongpressgesturerecognizer)

#### Configuring the Gesture Recognizer

- [var minimumPressDuration: CFTimeInterval](/documentation/watchkit/wklongpressgesturerecognizer/minimumpressduration)
- [var numberOfTapsRequired: Int](/documentation/watchkit/wklongpressgesturerecognizer/numberoftapsrequired)
- [var allowableMovement: CGFloat](/documentation/watchkit/wklongpressgesturerecognizer/allowablemovement)
- [WKPanGestureRecognizer](/documentation/watchkit/wkpangesturerecognizer)

#### Tracking the Location and Velocity of the Gesture

- [func translationInObject() -> CGPoint](/documentation/watchkit/wkpangesturerecognizer/translationinobject())
- [func velocityInObject() -> CGPoint](/documentation/watchkit/wkpangesturerecognizer/velocityinobject())
- [WKSwipeGestureRecognizer](/documentation/watchkit/wkswipegesturerecognizer)

#### Configuring the Gesture Recognizer

- [var direction: WKSwipeGestureRecognizerDirection](/documentation/watchkit/wkswipegesturerecognizer/direction)

#### Constants

- [WKSwipeGestureRecognizerDirection](/documentation/watchkit/wkswipegesturerecognizerdirection)

##### Constants

- [static var right: WKSwipeGestureRecognizerDirection](/documentation/watchkit/wkswipegesturerecognizerdirection/right)
- [static var left: WKSwipeGestureRecognizerDirection](/documentation/watchkit/wkswipegesturerecognizerdirection/left)
- [static var up: WKSwipeGestureRecognizerDirection](/documentation/watchkit/wkswipegesturerecognizerdirection/up)
- [static var down: WKSwipeGestureRecognizerDirection](/documentation/watchkit/wkswipegesturerecognizerdirection/down)

##### Initializers

- [init(rawValue: UInt)](/documentation/watchkit/wkswipegesturerecognizerdirection/init(rawvalue:))
- [WKTapGestureRecognizer](/documentation/watchkit/wktapgesturerecognizer)

#### Configuring the Gesture

- [var numberOfTapsRequired: Int](/documentation/watchkit/wktapgesturerecognizer/numberoftapsrequired)

### Notifications

- [WKUserNotificationInterfaceController](/documentation/watchkit/wkusernotificationinterfacecontroller)

#### Initializing the Interface Controller

- [init()](/documentation/watchkit/wkusernotificationinterfacecontroller/init())

#### Processing the Notification

- [func didReceive(UNNotification)](/documentation/watchkit/wkusernotificationinterfacecontroller/didreceive(_:))
- [func didReceive(UNNotification, withCompletion: (WKUserNotificationInterfaceType) -> Void)](/documentation/watchkit/wkusernotificationinterfacecontroller/didreceive(_:withcompletion:))

#### Working with Actions

- [var notificationActions: [UNNotificationAction]](/documentation/watchkit/wkusernotificationinterfacecontroller/notificationactions)
- [func performNotificationDefaultAction()](/documentation/watchkit/wkusernotificationinterfacecontroller/performnotificationdefaultaction())
- [func performDismissAction()](/documentation/watchkit/wkusernotificationinterfacecontroller/performdismissaction())
- [func dismiss()](/documentation/watchkit/wkusernotificationinterfacecontroller/dismiss())

#### Offering Suggestions for Text Input

- [func suggestionsForResponseToAction(withIdentifier: String, for: UNNotification, inputLanguage: String) -> [String]](/documentation/watchkit/wkusernotificationinterfacecontroller/suggestionsforresponsetoaction(withidentifier:for:inputlanguage:))

#### Constants

- [WKUserNotificationInterfaceType](/documentation/watchkit/wkusernotificationinterfacetype)

##### Constants

- [case `default`](/documentation/watchkit/wkusernotificationinterfacetype/default)
- [case custom](/documentation/watchkit/wkusernotificationinterfacetype/custom)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/wkusernotificationinterfacetype/init(rawvalue:))
- [NowPlayingView](/documentation/watchkit/nowplayingview)

### Creating a Now Playing View

- [init()](/documentation/watchkit/nowplayingview/init())

## Errors

- [WatchKitError](/documentation/watchkit/watchkiterror)

### Accessing Error Codes

- [static var downloadFailed: WatchKitError.Code](/documentation/watchkit/watchkiterror/downloadfailed)
- [static var invalidArgument: WatchKitError.Code](/documentation/watchkit/watchkiterror/invalidargument)
- [static var mediaPlayerFailed: WatchKitError.Code](/documentation/watchkit/watchkiterror/mediaplayerfailed)
- [static var recordingFailed: WatchKitError.Code](/documentation/watchkit/watchkiterror/recordingfailed)
- [static var unknown: WatchKitError.Code](/documentation/watchkit/watchkiterror/unknown)
- [static var applicationDelegateWatchKitRequestReplyNotCalled: WatchKitError.Code](/documentation/watchkit/watchkiterror/applicationdelegatewatchkitrequestreplynotcalled)

### Accessing the Error Domain

- [let WatchKitErrorDomain: String](/documentation/watchkit/watchkiterrordomain)

### Accessing Error Properties

- [WatchKitError.Code](/documentation/watchkit/watchkiterror/code)

#### Error Codes

- [case downloadFailed](/documentation/watchkit/watchkiterror/code/downloadfailed)
- [case invalidArgument](/documentation/watchkit/watchkiterror/code/invalidargument)
- [case mediaPlayerFailed](/documentation/watchkit/watchkiterror/code/mediaplayerfailed)
- [case recordingFailed](/documentation/watchkit/watchkiterror/code/recordingfailed)
- [case unknown](/documentation/watchkit/watchkiterror/code/unknown)
- [case applicationDelegateWatchKitRequestReplyNotCalled](/documentation/watchkit/watchkiterror/code/applicationdelegatewatchkitrequestreplynotcalled)
- [case downloadFailed](/documentation/watchkit/watchkiterror/code/downloadfailed)
- [case invalidArgument](/documentation/watchkit/watchkiterror/code/invalidargument)
- [case mediaPlayerFailed](/documentation/watchkit/watchkiterror/code/mediaplayerfailed)
- [case recordingFailed](/documentation/watchkit/watchkiterror/code/recordingfailed)
- [case unknown](/documentation/watchkit/watchkiterror/code/unknown)
- [case applicationDelegateWatchKitRequestReplyNotCalled](/documentation/watchkit/watchkiterror/code/applicationdelegatewatchkitrequestreplynotcalled)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchkit/watchkiterror/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/watchkit/watchkiterror/errordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
