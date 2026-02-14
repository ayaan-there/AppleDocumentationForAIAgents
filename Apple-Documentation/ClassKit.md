# ClassKit Documentation

Source: https://sosumi.ai/documentation/classkit

---
title: ClassKit
source: https://developer.apple.com/documentation/classkit
timestamp: 2026-02-13T18:54:49.521Z
---

## Essentials

- [Enabling ClassKit in your app](/documentation/classkit/enabling-classkit-in-your-app)

### Development mode

- [Testing your ClassKit app during development](/documentation/classkit/testing-your-classkit-app-during-development)

### User roles

- [About ClassKit and user roles](/documentation/classkit/about-classkit-and-user-roles)
- [ClassKit Environment Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.classkit-environment)
- [Incorporating ClassKit into an Educational App](/documentation/classkit/incorporating-classkit-into-an-educational-app)
- [CLSDataStore](/documentation/classkit/clsdatastore)

### Accessing the shared data store

- [class var shared: CLSDataStore](/documentation/classkit/clsdatastore/shared)

### Managing the delegate

- [Building missing contexts](/documentation/classkit/building-missing-contexts)
- [var delegate: (any CLSDataStoreDelegate)?](/documentation/classkit/clsdatastore/delegate)
- [CLSDataStoreDelegate](/documentation/classkit/clsdatastoredelegate)

#### Creating Contexts

- [func createContext(forIdentifier: String, parentContext: CLSContext, parentIdentifierPath: [String]) -> CLSContext?](/documentation/classkit/clsdatastoredelegate/createcontext(foridentifier:parentcontext:parentidentifierpath:))

### Accessing specific contexts and activities

- [var mainAppContext: CLSContext](/documentation/classkit/clsdatastore/mainappcontext)
- [var activeContext: CLSContext?](/documentation/classkit/clsdatastore/activecontext)
- [var runningActivity: CLSActivity?](/documentation/classkit/clsdatastore/runningactivity)
- [func fetchActivity(for: URL, completion: (CLSActivity?, (any Error)?) -> Void)](/documentation/classkit/clsdatastore/fetchactivity(for:completion:))
- [func completeAllAssignedActivities(matching: [String])](/documentation/classkit/clsdatastore/completeallassignedactivities(matching:))

### Finding contexts that match criteria

- [func contexts(matchingIdentifierPath: [String], completion: ([CLSContext], (any Error)?) -> Void)](/documentation/classkit/clsdatastore/contexts(matchingidentifierpath:completion:))
- [func contexts(matching: NSPredicate, completion: ([CLSContext], (any Error)?) -> Void)](/documentation/classkit/clsdatastore/contexts(matching:completion:))
- [CLSPredicateKeyPath](/documentation/classkit/clspredicatekeypath)

#### Predicate Key Paths

- [static let dateCreated: CLSPredicateKeyPath](/documentation/classkit/clspredicatekeypath/datecreated)
- [static let identifier: CLSPredicateKeyPath](/documentation/classkit/clspredicatekeypath/identifier)
- [static let parent: CLSPredicateKeyPath](/documentation/classkit/clspredicatekeypath/parent)
- [static let title: CLSPredicateKeyPath](/documentation/classkit/clspredicatekeypath/title)
- [static let topic: CLSPredicateKeyPath](/documentation/classkit/clspredicatekeypath/topic)
- [static let universalLinkURL: CLSPredicateKeyPath](/documentation/classkit/clspredicatekeypath/universallinkurl)

#### Initializing a Predicate Key Path

- [init(String)](/documentation/classkit/clspredicatekeypath/init(_:))
- [init(rawValue: String)](/documentation/classkit/clspredicatekeypath/init(rawvalue:))

### Removing contexts

- [func remove(CLSContext)](/documentation/classkit/clsdatastore/remove(_:))

### Saving changes

- [func save(completion: (((any Error)?) -> Void)?)](/documentation/classkit/clsdatastore/save(completion:))

## Contexts

- [Advertising your app’s assignable content](/documentation/classkit/advertising-your-app-s-assignable-content)

### Context management

- [Declaring your app’s context hierarchy](/documentation/classkit/declaring-your-app-s-context-hierarchy)
- [Building missing contexts](/documentation/classkit/building-missing-contexts)
- [Informing ClassKit that a task is about to begin](/documentation/classkit/informing-classkit-that-a-task-is-about-to-begin)

### Deep links

- [Linking directly to assignments](/documentation/classkit/linking-directly-to-assignments)

### Bookmarks

- [Creating bookmarks and assignments from your app](/documentation/classkit/creating-bookmarks-and-assignments-from-your-app)
- [CLSContext](/documentation/classkit/clscontext)

### Creating contexts

- [init(type: CLSContextType, identifier: String, title: String)](/documentation/classkit/clscontext/init(type:identifier:title:))
- [CLSObject](/documentation/classkit/clsobject)

#### Accessing Object Information

- [var dateCreated: Date](/documentation/classkit/clsobject/datecreated)
- [var dateLastModified: Date](/documentation/classkit/clsobject/datelastmodified)

### Identifying the context

- [var identifier: String](/documentation/classkit/clscontext/identifier)
- [var title: String](/documentation/classkit/clscontext/title)
- [var summary: String?](/documentation/classkit/clscontext/summary)
- [var thumbnail: CGImage?](/documentation/classkit/clscontext/thumbnail)

### Managing the context type

- [var type: CLSContextType](/documentation/classkit/clscontext/type)
- [func setType(CLSContextType)](/documentation/classkit/clscontext/settype(_:))
- [CLSContextType](/documentation/classkit/clscontexttype)

#### Context Types

- [case app](/documentation/classkit/clscontexttype/app)
- [case audio](/documentation/classkit/clscontexttype/audio)
- [case book](/documentation/classkit/clscontexttype/book)
- [case challenge](/documentation/classkit/clscontexttype/challenge)
- [case chapter](/documentation/classkit/clscontexttype/chapter)
- [case course](/documentation/classkit/clscontexttype/course)
- [case custom](/documentation/classkit/clscontexttype/custom)
- [case document](/documentation/classkit/clscontexttype/document)
- [case exercise](/documentation/classkit/clscontexttype/exercise)
- [case game](/documentation/classkit/clscontexttype/game)
- [case lesson](/documentation/classkit/clscontexttype/lesson)
- [case level](/documentation/classkit/clscontexttype/level)
- [case none](/documentation/classkit/clscontexttype/none)
- [case page](/documentation/classkit/clscontexttype/page)
- [case quiz](/documentation/classkit/clscontexttype/quiz)
- [case section](/documentation/classkit/clscontexttype/section)
- [case task](/documentation/classkit/clscontexttype/task)
- [case video](/documentation/classkit/clscontexttype/video)

#### Initializers

- [init?(rawValue: Int)](/documentation/classkit/clscontexttype/init(rawvalue:))
- [var customTypeName: String?](/documentation/classkit/clscontext/customtypename)

### Characterizing the context

- [var suggestedAge: NSRange](/documentation/classkit/clscontext/suggestedage)
- [var suggestedCompletionTime: NSRange](/documentation/classkit/clscontext/suggestedcompletiontime)
- [var isAssignable: Bool](/documentation/classkit/clscontext/isassignable)

### Managing context presentation

- [var displayOrder: Int](/documentation/classkit/clscontext/displayorder)
- [var topic: CLSContextTopic?](/documentation/classkit/clscontext/topic)
- [CLSContextTopic](/documentation/classkit/clscontexttopic)

#### Context Topics

- [static let artsAndMusic: CLSContextTopic](/documentation/classkit/clscontexttopic/artsandmusic)
- [static let computerScienceAndEngineering: CLSContextTopic](/documentation/classkit/clscontexttopic/computerscienceandengineering)
- [static let healthAndFitness: CLSContextTopic](/documentation/classkit/clscontexttopic/healthandfitness)
- [static let literacyAndWriting: CLSContextTopic](/documentation/classkit/clscontexttopic/literacyandwriting)
- [static let math: CLSContextTopic](/documentation/classkit/clscontexttopic/math)
- [static let science: CLSContextTopic](/documentation/classkit/clscontexttopic/science)
- [static let socialScience: CLSContextTopic](/documentation/classkit/clscontexttopic/socialscience)
- [static let worldLanguage: CLSContextTopic](/documentation/classkit/clscontexttopic/worldlanguage)

#### Initializing a Topic

- [init(rawValue: String)](/documentation/classkit/clscontexttopic/init(rawvalue:))

### Indicating progress reporting capabilities

- [var progressReportingCapabilities: Set<CLSProgressReportingCapability>](/documentation/classkit/clscontext/progressreportingcapabilities)
- [func addProgressReportingCapabilities(Set<CLSProgressReportingCapability>)](/documentation/classkit/clscontext/addprogressreportingcapabilities(_:))
- [func resetProgressReportingCapabilities()](/documentation/classkit/clscontext/resetprogressreportingcapabilities())
- [CLSProgressReportingCapability](/documentation/classkit/clsprogressreportingcapability)

#### Creating a Progress Reporting Capability

- [init(kind: CLSProgressReportingCapability.Kind, details: String?)](/documentation/classkit/clsprogressreportingcapability/init(kind:details:))

#### Characterizing the Capability

- [var details: String?](/documentation/classkit/clsprogressreportingcapability/details)
- [var kind: CLSProgressReportingCapability.Kind](/documentation/classkit/clsprogressreportingcapability/kind-swift.property)
- [CLSProgressReportingCapability.Kind](/documentation/classkit/clsprogressreportingcapability/kind-swift.enum)

##### Reporting Capabilities

- [case duration](/documentation/classkit/clsprogressreportingcapability/kind-swift.enum/duration)
- [case percent](/documentation/classkit/clsprogressreportingcapability/kind-swift.enum/percent)
- [case binary](/documentation/classkit/clsprogressreportingcapability/kind-swift.enum/binary)
- [case quantity](/documentation/classkit/clsprogressreportingcapability/kind-swift.enum/quantity)
- [case score](/documentation/classkit/clsprogressreportingcapability/kind-swift.enum/score)

##### Initializers

- [init?(rawValue: Int)](/documentation/classkit/clsprogressreportingcapability/kind-swift.enum/init(rawvalue:))

### Activating and deactivating a context

- [Informing ClassKit that a task is about to begin](/documentation/classkit/informing-classkit-that-a-task-is-about-to-begin)
- [func becomeActive()](/documentation/classkit/clscontext/becomeactive())
- [func resignActive()](/documentation/classkit/clscontext/resignactive())
- [var isActive: Bool](/documentation/classkit/clscontext/isactive)

### Creating activities

- [var currentActivity: CLSActivity?](/documentation/classkit/clscontext/currentactivity)
- [func createNewActivity() -> CLSActivity](/documentation/classkit/clscontext/createnewactivity())

### Managing context hierarchy

- [var identifierPath: [String]](/documentation/classkit/clscontext/identifierpath)
- [var parent: CLSContext?](/documentation/classkit/clscontext/parent)
- [func removeFromParent()](/documentation/classkit/clscontext/removefromparent())
- [func addChildContext(CLSContext)](/documentation/classkit/clscontext/addchildcontext(_:))
- [func descendant(matchingIdentifierPath: [String], completion: (CLSContext?, (any Error)?) -> Void)](/documentation/classkit/clscontext/descendant(matchingidentifierpath:completion:))

### Creating a context presentation hierarchy

- [var navigationChildContexts: [CLSContext]](/documentation/classkit/clscontext/navigationchildcontexts)
- [func addNavigationChildContext(CLSContext)](/documentation/classkit/clscontext/addnavigationchildcontext(_:))
- [func removeNavigationChildContext(CLSContext)](/documentation/classkit/clscontext/removenavigationchildcontext(_:))

### Configuring deep links

- [Linking directly to assignments](/documentation/classkit/linking-directly-to-assignments)
- [var universalLinkURL: URL?](/documentation/classkit/clscontext/universallinkurl)
- [var isClassKitDeepLink: Bool](/documentation/foundation/nsuseractivity/isclasskitdeeplink)
- [var contextIdentifierPath: [String]?](/documentation/foundation/nsuseractivity/contextidentifierpath)
- [CLSContextProvider](/documentation/classkit/clscontextprovider)

### Updating contexts

- [func updateDescendants(of: CLSContext, completion: ((any Error)?) -> Void)](/documentation/classkit/clscontextprovider/updatedescendants(of:completion:))

## Activities

- [Recording student progress](/documentation/classkit/recording-student-progress)
- [CLSActivity](/documentation/classkit/clsactivity)

### Starting and stopping an activity

- [func start()](/documentation/classkit/clsactivity/start())
- [func stop()](/documentation/classkit/clsactivity/stop())
- [var isStarted: Bool](/documentation/classkit/clsactivity/isstarted)
- [var duration: TimeInterval](/documentation/classkit/clsactivity/duration)

### Measuring progress

- [var progress: Double](/documentation/classkit/clsactivity/progress)
- [func addProgressRange(fromStart: Double, toEnd: Double)](/documentation/classkit/clsactivity/addprogressrange(fromstart:toend:))

### Managing activity items

- [func addAdditionalActivityItem(CLSActivityItem)](/documentation/classkit/clsactivity/addadditionalactivityitem(_:))
- [var primaryActivityItem: CLSActivityItem?](/documentation/classkit/clsactivity/primaryactivityitem)
- [var additionalActivityItems: [CLSActivityItem]](/documentation/classkit/clsactivity/additionalactivityitems)
- [func removeAllActivityItems()](/documentation/classkit/clsactivity/removeallactivityitems())

## Activity items

- [Recording additional metrics about a completed task](/documentation/classkit/recording-additional-metrics-about-a-completed-task)
- [CLSScoreItem](/documentation/classkit/clsscoreitem)

### Creating Score Activity Items

- [init(identifier: String, title: String, score: Double, maxScore: Double)](/documentation/classkit/clsscoreitem/init(identifier:title:score:maxscore:))

### Managing the Score

- [var score: Double](/documentation/classkit/clsscoreitem/score)
- [var maxScore: Double](/documentation/classkit/clsscoreitem/maxscore)
- [CLSBinaryItem](/documentation/classkit/clsbinaryitem)

### Creating Binary Activity Items

- [init(identifier: String, title: String, type: CLSBinaryValueType)](/documentation/classkit/clsbinaryitem/init(identifier:title:type:))
- [CLSBinaryValueType](/documentation/classkit/clsbinaryvaluetype)

#### Value Types

- [case passFail](/documentation/classkit/clsbinaryvaluetype/passfail)
- [case trueFalse](/documentation/classkit/clsbinaryvaluetype/truefalse)
- [case yesNo](/documentation/classkit/clsbinaryvaluetype/yesno)
- [case correctIncorrect](/documentation/classkit/clsbinaryvaluetype/correctincorrect)

#### Initializers

- [init?(rawValue: Int)](/documentation/classkit/clsbinaryvaluetype/init(rawvalue:))

### Managing the Value

- [var value: Bool](/documentation/classkit/clsbinaryitem/value)
- [var valueType: CLSBinaryValueType](/documentation/classkit/clsbinaryitem/valuetype)
- [CLSQuantityItem](/documentation/classkit/clsquantityitem)

### Creating Quantity Activity Items

- [init(identifier: String, title: String)](/documentation/classkit/clsquantityitem/init(identifier:title:))

### Managing the Quantity

- [var quantity: Double](/documentation/classkit/clsquantityitem/quantity)
- [CLSActivityItem](/documentation/classkit/clsactivityitem)

### Accessing Activity Item Information

- [var identifier: String](/documentation/classkit/clsactivityitem/identifier)
- [var title: String](/documentation/classkit/clsactivityitem/title)

## Errors

- [CLSError](/documentation/classkit/clserror)

### Error Domain

- [let CLSErrorCodeDomain: String](/documentation/classkit/clserrorcodedomain)

### Error Codes

- [static var none: CLSError.Code](/documentation/classkit/clserror/none)
- [static var authorizationDenied: CLSError.Code](/documentation/classkit/clserror/authorizationdenied)
- [static var classKitUnavailable: CLSError.Code](/documentation/classkit/clserror/classkitunavailable)
- [static var databaseInaccessible: CLSError.Code](/documentation/classkit/clserror/databaseinaccessible)
- [static var invalidAccountCredentials: CLSError.Code](/documentation/classkit/clserror/invalidaccountcredentials)
- [static var invalidArgument: CLSError.Code](/documentation/classkit/clserror/invalidargument)
- [static var invalidCreate: CLSError.Code](/documentation/classkit/clserror/invalidcreate)
- [static var invalidModification: CLSError.Code](/documentation/classkit/clserror/invalidmodification)
- [static var invalidUpdate: CLSError.Code](/documentation/classkit/clserror/invalidupdate)
- [static var limits: CLSError.Code](/documentation/classkit/clserror/limits)
- [static var partialFailure: CLSError.Code](/documentation/classkit/clserror/partialfailure)
- [CLSError.Code](/documentation/classkit/clserror/code)

#### Error codes

- [case none](/documentation/classkit/clserror/code/none)
- [case authorizationDenied](/documentation/classkit/clserror/code/authorizationdenied)
- [case classKitUnavailable](/documentation/classkit/clserror/code/classkitunavailable)
- [case databaseInaccessible](/documentation/classkit/clserror/code/databaseinaccessible)
- [case invalidAccountCredentials](/documentation/classkit/clserror/code/invalidaccountcredentials)
- [case invalidArgument](/documentation/classkit/clserror/code/invalidargument)
- [case invalidCreate](/documentation/classkit/clserror/code/invalidcreate)
- [case invalidModification](/documentation/classkit/clserror/code/invalidmodification)
- [case invalidUpdate](/documentation/classkit/clserror/code/invalidupdate)
- [case limits](/documentation/classkit/clserror/code/limits)
- [case partialFailure](/documentation/classkit/clserror/code/partialfailure)

#### Initializers

- [init?(rawValue: Int)](/documentation/classkit/clserror/code/init(rawvalue:))

### User info

- [CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey)

#### Keys

- [static let objectKey: CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey/objectkey)
- [static let successfulObjectsKey: CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey/successfulobjectskey)
- [static let underlyingErrorsKey: CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey/underlyingerrorskey)

#### Initializers

- [init(String)](/documentation/classkit/clserroruserinfokey/init(_:))
- [init(rawValue: String)](/documentation/classkit/clserroruserinfokey/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/classkit/clserror/errordomain)
- [let CLSErrorCodeDomain: String](/documentation/classkit/clserrorcodedomain)
- [CLSError.Code](/documentation/classkit/clserror/code)

### Error codes

- [case none](/documentation/classkit/clserror/code/none)
- [case authorizationDenied](/documentation/classkit/clserror/code/authorizationdenied)
- [case classKitUnavailable](/documentation/classkit/clserror/code/classkitunavailable)
- [case databaseInaccessible](/documentation/classkit/clserror/code/databaseinaccessible)
- [case invalidAccountCredentials](/documentation/classkit/clserror/code/invalidaccountcredentials)
- [case invalidArgument](/documentation/classkit/clserror/code/invalidargument)
- [case invalidCreate](/documentation/classkit/clserror/code/invalidcreate)
- [case invalidModification](/documentation/classkit/clserror/code/invalidmodification)
- [case invalidUpdate](/documentation/classkit/clserror/code/invalidupdate)
- [case limits](/documentation/classkit/clserror/code/limits)
- [case partialFailure](/documentation/classkit/clserror/code/partialfailure)

### Initializers

- [init?(rawValue: Int)](/documentation/classkit/clserror/code/init(rawvalue:))
- [CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey)

### Keys

- [static let objectKey: CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey/objectkey)
- [static let successfulObjectsKey: CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey/successfulobjectskey)
- [static let underlyingErrorsKey: CLSErrorUserInfoKey](/documentation/classkit/clserroruserinfokey/underlyingerrorskey)

### Initializers

- [init(String)](/documentation/classkit/clserroruserinfokey/init(_:))
- [init(rawValue: String)](/documentation/classkit/clserroruserinfokey/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
