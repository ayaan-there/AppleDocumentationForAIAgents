# Core Data Documentation

Source: https://sosumi.ai/documentation/coredata

---
title: Core Data
source: https://developer.apple.com/documentation/coredata
timestamp: 2026-02-13T19:23:07.795Z
---

## Essentials

- [Creating a Core Data model](/documentation/coredata/creating-a-core-data-model)
- [Setting up a Core Data stack](/documentation/coredata/setting-up-a-core-data-stack)

### Legacy Stack Setup

- [Setting up a Core Data stack manually](/documentation/coredata/setting-up-a-core-data-stack-manually)
- [Core Data stack](/documentation/coredata/core-data-stack)

### Stack Setup

- [NSPersistentContainer](/documentation/coredata/nspersistentcontainer)

#### Creating a Container

- [convenience init(name: String)](/documentation/coredata/nspersistentcontainer/init(name:))
- [init(name: String, managedObjectModel: NSManagedObjectModel)](/documentation/coredata/nspersistentcontainer/init(name:managedobjectmodel:))

#### Getting the Container’s Configuration

- [var managedObjectModel: NSManagedObjectModel](/documentation/coredata/nspersistentcontainer/managedobjectmodel)
- [var name: String](/documentation/coredata/nspersistentcontainer/name)
- [var persistentStoreCoordinator: NSPersistentStoreCoordinator](/documentation/coredata/nspersistentcontainer/persistentstorecoordinator)

#### Accessing the Default Directory

- [class var defaultDirectoryURL: URL](/documentation/coredata/nspersistentcontainer/defaultdirectoryurl-swift.type.property)
- [class func defaultDirectoryURL() -> URL](/documentation/coredata/nspersistentcontainer/defaultdirectoryurl())

#### Managing Persistent Stores

- [var persistentStoreDescriptions: [NSPersistentStoreDescription]](/documentation/coredata/nspersistentcontainer/persistentstoredescriptions)
- [func loadPersistentStores(completionHandler: (NSPersistentStoreDescription, (any Error)?) -> Void)](/documentation/coredata/nspersistentcontainer/loadpersistentstores(completionhandler:))

#### Acquiring Contexts

- [func newBackgroundContext() -> NSManagedObjectContext](/documentation/coredata/nspersistentcontainer/newbackgroundcontext())
- [var viewContext: NSManagedObjectContext](/documentation/coredata/nspersistentcontainer/viewcontext)

#### Performing Background Tasks

- [func performBackgroundTask((NSManagedObjectContext) -> Void)](/documentation/coredata/nspersistentcontainer/performbackgroundtask(_:)-39sch)
- [func performBackgroundTask<T>((NSManagedObjectContext) throws -> T) async rethrows -> T](/documentation/coredata/nspersistentcontainer/performbackgroundtask(_:)-25nok)

### Object Modeling

- [NSManagedObjectModel](/documentation/coredata/nsmanagedobjectmodel)

#### Creating a managed object model

- [convenience init?(contentsOf: URL)](/documentation/coredata/nsmanagedobjectmodel/init(contentsof:))
- [init()](/documentation/coredata/nsmanagedobjectmodel/init())
- [class func mergedModel(from: [Bundle]?) -> NSManagedObjectModel?](/documentation/coredata/nsmanagedobjectmodel/mergedmodel(from:))
- [class func mergedModel(from: [Bundle]?, forStoreMetadata: [String : Any]) -> NSManagedObjectModel?](/documentation/coredata/nsmanagedobjectmodel/mergedmodel(from:forstoremetadata:))
- [init?(byMerging: [NSManagedObjectModel]?)](/documentation/coredata/nsmanagedobjectmodel/init(bymerging:))
- [init?(byMerging: [NSManagedObjectModel], forStoreMetadata: [String : Any])](/documentation/coredata/nsmanagedobjectmodel/init(bymerging:forstoremetadata:))

#### Managing entities and configurations

- [var entities: [NSEntityDescription]](/documentation/coredata/nsmanagedobjectmodel/entities)
- [var entitiesByName: [String : NSEntityDescription]](/documentation/coredata/nsmanagedobjectmodel/entitiesbyname)
- [var configurations: [String]](/documentation/coredata/nsmanagedobjectmodel/configurations)
- [func entities(forConfigurationName: String?) -> [NSEntityDescription]?](/documentation/coredata/nsmanagedobjectmodel/entities(forconfigurationname:))
- [func setEntities([NSEntityDescription], forConfigurationName: String)](/documentation/coredata/nsmanagedobjectmodel/setentities(_:forconfigurationname:))

#### Manipulating fetch request templates

- [var fetchRequestTemplatesByName: [String : NSFetchRequest<any NSFetchRequestResult>]](/documentation/coredata/nsmanagedobjectmodel/fetchrequesttemplatesbyname)
- [func fetchRequestTemplate(forName: String) -> NSFetchRequest<any NSFetchRequestResult>?](/documentation/coredata/nsmanagedobjectmodel/fetchrequesttemplate(forname:))
- [func fetchRequestFromTemplate(withName: String, substitutionVariables: [String : Any]) -> NSFetchRequest<any NSFetchRequestResult>?](/documentation/coredata/nsmanagedobjectmodel/fetchrequestfromtemplate(withname:substitutionvariables:))
- [func setFetchRequestTemplate(NSFetchRequest<any NSFetchRequestResult>?, forName: String)](/documentation/coredata/nsmanagedobjectmodel/setfetchrequesttemplate(_:forname:))

#### Handling localization

- [var localizationDictionary: [String : String]?](/documentation/coredata/nsmanagedobjectmodel/localizationdictionary)

#### Versioning and migrating entities

- [var versionChecksum: String](/documentation/coredata/nsmanagedobjectmodel/versionchecksum)
- [var versionIdentifiers: Set<AnyHashable>](/documentation/coredata/nsmanagedobjectmodel/versionidentifiers)
- [var entityVersionHashesByName: [String : Data]](/documentation/coredata/nsmanagedobjectmodel/entityversionhashesbyname)
- [func isConfiguration(withName: String?, compatibleWithStoreMetadata: [String : Any]) -> Bool](/documentation/coredata/nsmanagedobjectmodel/isconfiguration(withname:compatiblewithstoremetadata:))

#### Working with indexes

- [NSFetchIndexElementType](/documentation/coredata/nsfetchindexelementtype)

##### Index Types

- [case binary](/documentation/coredata/nsfetchindexelementtype/binary)
- [case rTree](/documentation/coredata/nsfetchindexelementtype/rtree)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsfetchindexelementtype/init(rawvalue:))
- [NSFetchIndexDescription](/documentation/coredata/nsfetchindexdescription)

##### Creating an Index Description

- [init(name: String, elements: [NSFetchIndexElementDescription]?)](/documentation/coredata/nsfetchindexdescription/init(name:elements:))

##### Inspecting an Index Description

- [var elements: [NSFetchIndexElementDescription]](/documentation/coredata/nsfetchindexdescription/elements)
- [var entity: NSEntityDescription?](/documentation/coredata/nsfetchindexdescription/entity)
- [var name: String](/documentation/coredata/nsfetchindexdescription/name)
- [var partialIndexPredicate: NSPredicate?](/documentation/coredata/nsfetchindexdescription/partialindexpredicate)
- [NSFetchIndexElementDescription](/documentation/coredata/nsfetchindexelementdescription)

##### Creating an Index Element Description

- [init(property: NSPropertyDescription, collationType: NSFetchIndexElementType)](/documentation/coredata/nsfetchindexelementdescription/init(property:collationtype:))

##### Inspecting an Index Element Description

- [var collationType: NSFetchIndexElementType](/documentation/coredata/nsfetchindexelementdescription/collationtype)
- [var indexDescription: NSFetchIndexDescription?](/documentation/coredata/nsfetchindexelementdescription/indexdescription)
- [var isAscending: Bool](/documentation/coredata/nsfetchindexelementdescription/isascending)
- [var property: NSPropertyDescription?](/documentation/coredata/nsfetchindexelementdescription/property)
- [var propertyName: String?](/documentation/coredata/nsfetchindexelementdescription/propertyname)

#### Instance Methods

- [func makeManagedObjectModel(for: Schema, mergedWith: NSManagedObjectModel?) -> NSManagedObjectModel?](/documentation/coredata/nsmanagedobjectmodel/makemanagedobjectmodel(for:mergedwith:)-swift.method)

#### Type Methods

- [static func makeManagedObjectModel(for: any PersistentModel.Type..., mergedWith: NSManagedObjectModel?) -> NSManagedObjectModel?](/documentation/coredata/nsmanagedobjectmodel/makemanagedobjectmodel(for:mergedwith:)-2tc31)
- [static func makeManagedObjectModel(for: [any PersistentModel.Type], mergedWith: NSManagedObjectModel?) -> NSManagedObjectModel?](/documentation/coredata/nsmanagedobjectmodel/makemanagedobjectmodel(for:mergedwith:)-37opo)
- [static func makeManagedObjectModel(for: Schema, mergedWith: NSManagedObjectModel?) -> NSManagedObjectModel?](/documentation/coredata/nsmanagedobjectmodel/makemanagedobjectmodel(for:mergedwith:)-7lqq9)
- [NSEntityDescription](/documentation/coredata/nsentitydescription)

#### Getting descriptive information

- [var name: String?](/documentation/coredata/nsentitydescription/name)
- [var managedObjectModel: NSManagedObjectModel](/documentation/coredata/nsentitydescription/managedobjectmodel)
- [var managedObjectClassName: String!](/documentation/coredata/nsentitydescription/managedobjectclassname)
- [var renamingIdentifier: String?](/documentation/coredata/nsentitydescription/renamingidentifier)
- [var isAbstract: Bool](/documentation/coredata/nsentitydescription/isabstract)
- [var userInfo: [AnyHashable : Any]?](/documentation/coredata/nsentitydescription/userinfo)
- [var coreSpotlightDisplayNameExpression: NSExpression](/documentation/coredata/nsentitydescription/corespotlightdisplaynameexpression)

#### Managing inheritance

- [var subentitiesByName: [String : NSEntityDescription]](/documentation/coredata/nsentitydescription/subentitiesbyname)
- [var subentities: [NSEntityDescription]](/documentation/coredata/nsentitydescription/subentities)
- [var superentity: NSEntityDescription?](/documentation/coredata/nsentitydescription/superentity)
- [func isKindOf(entity: NSEntityDescription) -> Bool](/documentation/coredata/nsentitydescription/iskindof(entity:))

#### Working with properties

- [var propertiesByName: [String : NSPropertyDescription]](/documentation/coredata/nsentitydescription/propertiesbyname)
- [var properties: [NSPropertyDescription]](/documentation/coredata/nsentitydescription/properties)
- [var attributesByName: [String : NSAttributeDescription]](/documentation/coredata/nsentitydescription/attributesbyname)
- [var relationshipsByName: [String : NSRelationshipDescription]](/documentation/coredata/nsentitydescription/relationshipsbyname)
- [func relationships(forDestination: NSEntityDescription) -> [NSRelationshipDescription]](/documentation/coredata/nsentitydescription/relationships(fordestination:))

#### Configuring indexes and constraints

- [var indexes: [NSFetchIndexDescription]](/documentation/coredata/nsentitydescription/indexes)
- [var uniquenessConstraints: [[Any]]](/documentation/coredata/nsentitydescription/uniquenessconstraints)
- [var compoundIndexes: [[Any]]](/documentation/coredata/nsentitydescription/compoundindexes)

#### Creating a managed object

- [class func insertNewObject(forEntityName: String, into: NSManagedObjectContext) -> NSManagedObject](/documentation/coredata/nsentitydescription/insertnewobject(forentityname:into:))

#### Retrieving a description by its name

- [class func entity(forEntityName: String, in: NSManagedObjectContext) -> NSEntityDescription?](/documentation/coredata/nsentitydescription/entity(forentityname:in:))

#### Managing versioning

- [var versionHash: Data](/documentation/coredata/nsentitydescription/versionhash)
- [var versionHashModifier: String?](/documentation/coredata/nsentitydescription/versionhashmodifier)
- [NSPropertyDescription](/documentation/coredata/nspropertydescription)

#### Accessing Features of a Property

- [var entity: NSEntityDescription](/documentation/coredata/nspropertydescription/entity)
- [var isIndexed: Bool](/documentation/coredata/nspropertydescription/isindexed)
- [var isOptional: Bool](/documentation/coredata/nspropertydescription/isoptional)
- [var isTransient: Bool](/documentation/coredata/nspropertydescription/istransient)
- [var name: String](/documentation/coredata/nspropertydescription/name)
- [var userInfo: [AnyHashable : Any]?](/documentation/coredata/nspropertydescription/userinfo)

#### Supporting Validation

- [var validationPredicates: [NSPredicate]](/documentation/coredata/nspropertydescription/validationpredicates)
- [var validationWarnings: [Any]](/documentation/coredata/nspropertydescription/validationwarnings)
- [func setValidationPredicates([NSPredicate]?, withValidationWarnings: [String]?)](/documentation/coredata/nspropertydescription/setvalidationpredicates(_:withvalidationwarnings:))

#### Supporting Versioning

- [var versionHash: Data](/documentation/coredata/nspropertydescription/versionhash)
- [var versionHashModifier: String?](/documentation/coredata/nspropertydescription/versionhashmodifier)
- [var renamingIdentifier: String?](/documentation/coredata/nspropertydescription/renamingidentifier)

#### Specifying Spotlight Support

- [var isIndexedBySpotlight: Bool](/documentation/coredata/nspropertydescription/isindexedbyspotlight)
- [var isStoredInExternalRecord: Bool](/documentation/coredata/nspropertydescription/isstoredinexternalrecord)
- [NSAttributeDescription](/documentation/coredata/nsattributedescription)

#### Managing the type

- [var attributeValueClassName: String?](/documentation/coredata/nsattributedescription/attributevalueclassname)
- [var type: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/type)
- [NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct)

##### Attribute Types

- [static let binaryData: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/binarydata)
- [static let boolean: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/boolean)
- [static let composite: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/composite)
- [static let date: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/date)
- [static let decimal: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/decimal)
- [static let double: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/double)
- [static let float: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/float)
- [static let integer16: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/integer16)
- [static let integer32: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/integer32)
- [static let integer64: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/integer64)
- [static let objectID: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/objectid)
- [static let string: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/string)
- [static let transformable: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/transformable)
- [static let undefined: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/undefined)
- [static let uri: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/uri)
- [static let uuid: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/uuid)
- [var attributeType: NSAttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.property)
- [NSAttributeType](/documentation/coredata/nsattributetype)

##### Attribute types

- [case binaryDataAttributeType](/documentation/coredata/nsattributetype/binarydataattributetype)
- [case booleanAttributeType](/documentation/coredata/nsattributetype/booleanattributetype)
- [case compositeAttributeType](/documentation/coredata/nsattributetype/compositeattributetype)
- [case dateAttributeType](/documentation/coredata/nsattributetype/dateattributetype)
- [case decimalAttributeType](/documentation/coredata/nsattributetype/decimalattributetype)
- [case doubleAttributeType](/documentation/coredata/nsattributetype/doubleattributetype)
- [case floatAttributeType](/documentation/coredata/nsattributetype/floatattributetype)
- [case integer16AttributeType](/documentation/coredata/nsattributetype/integer16attributetype)
- [case integer32AttributeType](/documentation/coredata/nsattributetype/integer32attributetype)
- [case integer64AttributeType](/documentation/coredata/nsattributetype/integer64attributetype)
- [case objectIDAttributeType](/documentation/coredata/nsattributetype/objectidattributetype)
- [case stringAttributeType](/documentation/coredata/nsattributetype/stringattributetype)
- [case transformableAttributeType](/documentation/coredata/nsattributetype/transformableattributetype)
- [case undefinedAttributeType](/documentation/coredata/nsattributetype/undefinedattributetype)
- [case URIAttributeType](/documentation/coredata/nsattributetype/uriattributetype)
- [case UUIDAttributeType](/documentation/coredata/nsattributetype/uuidattributetype)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsattributetype/init(rawvalue:))

#### Configuring the behavior

- [var allowsCloudEncryption: Bool](/documentation/coredata/nsattributedescription/allowscloudencryption)
- [var allowsExternalBinaryDataStorage: Bool](/documentation/coredata/nsattributedescription/allowsexternalbinarydatastorage)
- [var defaultValue: Any?](/documentation/coredata/nsattributedescription/defaultvalue)
- [var preservesValueInHistoryOnDeletion: Bool](/documentation/coredata/nsattributedescription/preservesvalueinhistoryondeletion)
- [var valueTransformerName: String?](/documentation/coredata/nsattributedescription/valuetransformername)

#### Getting version information

- [var versionHash: Data](/documentation/coredata/nsattributedescription/versionhash)

#### Deprecated

- [Deprecated symbols](/documentation/coredata/nsattributedescription-deprecated-symbols)

##### Deprecated properties

- [var attributeType: NSAttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.property)
- [NSDerivedAttributeDescription](/documentation/coredata/nsderivedattributedescription)

#### Specifying the Derivation Expression

- [var derivationExpression: NSExpression?](/documentation/coredata/nsderivedattributedescription/derivationexpression)
- [NSRelationshipDescription](/documentation/coredata/nsrelationshipdescription)

#### Configuring the Destination

- [var inverseRelationship: NSRelationshipDescription?](/documentation/coredata/nsrelationshipdescription/inverserelationship)
- [var destinationEntity: NSEntityDescription?](/documentation/coredata/nsrelationshipdescription/destinationentity)
- [var isOrdered: Bool](/documentation/coredata/nsrelationshipdescription/isordered)

#### Configuring Cardinality

- [var isToMany: Bool](/documentation/coredata/nsrelationshipdescription/istomany)
- [var minCount: Int](/documentation/coredata/nsrelationshipdescription/mincount)
- [var maxCount: Int](/documentation/coredata/nsrelationshipdescription/maxcount)

#### Configuring Delete Behavior

- [var deleteRule: NSDeleteRule](/documentation/coredata/nsrelationshipdescription/deleterule)
- [NSDeleteRule](/documentation/coredata/nsdeleterule)

##### Delete Rules

- [case noActionDeleteRule](/documentation/coredata/nsdeleterule/noactiondeleterule)
- [case nullifyDeleteRule](/documentation/coredata/nsdeleterule/nullifydeleterule)
- [case cascadeDeleteRule](/documentation/coredata/nsdeleterule/cascadedeleterule)
- [case denyDeleteRule](/documentation/coredata/nsdeleterule/denydeleterule)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsdeleterule/init(rawvalue:))

#### Getting Version Data

- [var versionHash: Data](/documentation/coredata/nsrelationshipdescription/versionhash)

### Object Management

- [NSManagedObjectContext](/documentation/coredata/nsmanagedobjectcontext)

#### Creating a context

- [convenience init(NSManagedObjectContext.ConcurrencyType)](/documentation/coredata/nsmanagedobjectcontext/init(_:))
- [NSManagedObjectContext.ConcurrencyType](/documentation/coredata/nsmanagedobjectcontext/concurrencytype-swift.struct)

##### Concurrency Types

- [static let mainQueue: NSManagedObjectContext.ConcurrencyType](/documentation/coredata/nsmanagedobjectcontext/concurrencytype-swift.struct/mainqueue)
- [static let privateQueue: NSManagedObjectContext.ConcurrencyType](/documentation/coredata/nsmanagedobjectcontext/concurrencytype-swift.struct/privatequeue)
- [init(concurrencyType: NSManagedObjectContextConcurrencyType)](/documentation/coredata/nsmanagedobjectcontext/init(concurrencytype:))
- [NSManagedObjectContextConcurrencyType](/documentation/coredata/nsmanagedobjectcontextconcurrencytype)

##### Concurrency Types

- [case privateQueueConcurrencyType](/documentation/coredata/nsmanagedobjectcontextconcurrencytype/privatequeueconcurrencytype)
- [case mainQueueConcurrencyType](/documentation/coredata/nsmanagedobjectcontextconcurrencytype/mainqueueconcurrencytype)
- [case confinementConcurrencyType](/documentation/coredata/nsmanagedobjectcontextconcurrencytype/confinementconcurrencytype)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsmanagedobjectcontextconcurrencytype/init(rawvalue:))

#### Configuring a context

- [var persistentStoreCoordinator: NSPersistentStoreCoordinator?](/documentation/coredata/nsmanagedobjectcontext/persistentstorecoordinator)
- [var parent: NSManagedObjectContext?](/documentation/coredata/nsmanagedobjectcontext/parent)
- [var name: String?](/documentation/coredata/nsmanagedobjectcontext/name)
- [var userInfo: NSMutableDictionary](/documentation/coredata/nsmanagedobjectcontext/userinfo)

#### Registering and fetching objects

- [func fetch(NSFetchRequest<any NSFetchRequestResult>) throws -> [Any]](/documentation/coredata/nsmanagedobjectcontext/fetch(_:)-38ys1)
- [func fetch<T>(NSFetchRequest<T>) throws -> [T]](/documentation/coredata/nsmanagedobjectcontext/fetch(_:)-4xeoz)
- [func count(for: NSFetchRequest<any NSFetchRequestResult>) throws -> Int](/documentation/coredata/nsmanagedobjectcontext/count(for:)-93zbm)
- [func registeredObject(for: NSManagedObjectID) -> NSManagedObject?](/documentation/coredata/nsmanagedobjectcontext/registeredobject(for:))
- [func object(with: NSManagedObjectID) -> NSManagedObject](/documentation/coredata/nsmanagedobjectcontext/object(with:))
- [func existingObject(with: NSManagedObjectID) throws -> NSManagedObject](/documentation/coredata/nsmanagedobjectcontext/existingobject(with:))
- [var registeredObjects: Set<NSManagedObject>](/documentation/coredata/nsmanagedobjectcontext/registeredobjects)
- [func count<T>(for: NSFetchRequest<T>) throws -> Int](/documentation/coredata/nsmanagedobjectcontext/count(for:)-3r91z)
- [func execute(NSPersistentStoreRequest) throws -> NSPersistentStoreResult](/documentation/coredata/nsmanagedobjectcontext/execute(_:))
- [func refreshAllObjects()](/documentation/coredata/nsmanagedobjectcontext/refreshallobjects())
- [var retainsRegisteredObjects: Bool](/documentation/coredata/nsmanagedobjectcontext/retainsregisteredobjects)

#### Handling managed objects

- [var shouldDeleteInaccessibleFaults: Bool](/documentation/coredata/nsmanagedobjectcontext/shoulddeleteinaccessiblefaults)
- [var insertedObjects: Set<NSManagedObject>](/documentation/coredata/nsmanagedobjectcontext/insertedobjects)
- [var updatedObjects: Set<NSManagedObject>](/documentation/coredata/nsmanagedobjectcontext/updatedobjects)
- [var deletedObjects: Set<NSManagedObject>](/documentation/coredata/nsmanagedobjectcontext/deletedobjects)
- [func shouldHandleInaccessibleFault(NSManagedObject, for: NSManagedObjectID, triggeredByProperty: NSPropertyDescription?) -> Bool](/documentation/coredata/nsmanagedobjectcontext/shouldhandleinaccessiblefault(_:for:triggeredbyproperty:))
- [func insert(NSManagedObject)](/documentation/coredata/nsmanagedobjectcontext/insert(_:))
- [func delete(NSManagedObject)](/documentation/coredata/nsmanagedobjectcontext/delete(_:))
- [func assign(Any, to: NSPersistentStore)](/documentation/coredata/nsmanagedobjectcontext/assign(_:to:))
- [func obtainPermanentIDs(for: [NSManagedObject]) throws](/documentation/coredata/nsmanagedobjectcontext/obtainpermanentids(for:))
- [func detectConflicts(for: NSManagedObject)](/documentation/coredata/nsmanagedobjectcontext/detectconflicts(for:))
- [func refresh(NSManagedObject, mergeChanges: Bool)](/documentation/coredata/nsmanagedobjectcontext/refresh(_:mergechanges:))
- [func processPendingChanges()](/documentation/coredata/nsmanagedobjectcontext/processpendingchanges())
- [func observeValue(forKeyPath: String?, of: Any?, change: [String : Any]?, context: UnsafeMutableRawPointer?)](/documentation/coredata/nsmanagedobjectcontext/observevalue(forkeypath:of:change:context:))

#### Managing concurrency

- [let NSManagedObjectContextQueryGenerationKey: String](/documentation/coredata/nsmanagedobjectcontextquerygenerationkey)
- [class func mergeChanges(fromRemoteContextSave: [AnyHashable : Any], into: [NSManagedObjectContext])](/documentation/coredata/nsmanagedobjectcontext/mergechanges(fromremotecontextsave:into:))
- [var automaticallyMergesChangesFromParent: Bool](/documentation/coredata/nsmanagedobjectcontext/automaticallymergeschangesfromparent)
- [var concurrencyType: NSManagedObjectContextConcurrencyType](/documentation/coredata/nsmanagedobjectcontext/concurrencytype-swift.property)
- [var mergePolicy: Any](/documentation/coredata/nsmanagedobjectcontext/mergepolicy)
- [var queryGenerationToken: NSQueryGenerationToken?](/documentation/coredata/nsmanagedobjectcontext/querygenerationtoken)
- [var transactionAuthor: String?](/documentation/coredata/nsmanagedobjectcontext/transactionauthor)
- [func mergeChanges(fromContextDidSave: Notification)](/documentation/coredata/nsmanagedobjectcontext/mergechanges(fromcontextdidsave:))
- [func setQueryGenerationFrom(NSQueryGenerationToken?) throws](/documentation/coredata/nsmanagedobjectcontext/setquerygenerationfrom(_:))

#### Managing notifications

- [static let didChangeObjectsNotification: Notification.Name](/documentation/coredata/nsmanagedobjectcontext/didchangeobjectsnotification)
- [static let NSManagedObjectContextObjectsDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nsmanagedobjectcontextobjectsdidchange)
- [static let didSaveObjectsNotification: Notification.Name](/documentation/coredata/nsmanagedobjectcontext/didsaveobjectsnotification)
- [static let NSManagedObjectContextDidSave: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nsmanagedobjectcontextdidsave)
- [static let willSaveObjectsNotification: Notification.Name](/documentation/coredata/nsmanagedobjectcontext/willsaveobjectsnotification)
- [static let NSManagedObjectContextWillSave: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nsmanagedobjectcontextwillsave)
- [let NSInsertedObjectsKey: String](/documentation/coredata/nsinsertedobjectskey)
- [let NSUpdatedObjectsKey: String](/documentation/coredata/nsupdatedobjectskey)
- [let NSDeletedObjectsKey: String](/documentation/coredata/nsdeletedobjectskey)
- [let NSRefreshedObjectsKey: String](/documentation/coredata/nsrefreshedobjectskey)
- [let NSInvalidatedObjectsKey: String](/documentation/coredata/nsinvalidatedobjectskey)
- [let NSInvalidatedAllObjectsKey: String](/documentation/coredata/nsinvalidatedallobjectskey)
- [static let didMergeChangesObjectIDsNotification: Notification.Name](/documentation/coredata/nsmanagedobjectcontext/didmergechangesobjectidsnotification)
- [static let didSaveObjectIDsNotification: Notification.Name](/documentation/coredata/nsmanagedobjectcontext/didsaveobjectidsnotification)
- [NSManagedObjectContext.NotificationKey](/documentation/coredata/nsmanagedobjectcontext/notificationkey)

##### Constants

- [case deletedObjectIDs](/documentation/coredata/nsmanagedobjectcontext/notificationkey/deletedobjectids)
- [case deletedObjects](/documentation/coredata/nsmanagedobjectcontext/notificationkey/deletedobjects)
- [case insertedObjectIDs](/documentation/coredata/nsmanagedobjectcontext/notificationkey/insertedobjectids)
- [case insertedObjects](/documentation/coredata/nsmanagedobjectcontext/notificationkey/insertedobjects)
- [case invalidatedAllObjects](/documentation/coredata/nsmanagedobjectcontext/notificationkey/invalidatedallobjects)
- [case invalidatedObjectIDs](/documentation/coredata/nsmanagedobjectcontext/notificationkey/invalidatedobjectids)
- [case invalidatedObjects](/documentation/coredata/nsmanagedobjectcontext/notificationkey/invalidatedobjects)
- [case queryGeneration](/documentation/coredata/nsmanagedobjectcontext/notificationkey/querygeneration)
- [case refreshedObjectIDs](/documentation/coredata/nsmanagedobjectcontext/notificationkey/refreshedobjectids)
- [case refreshedObjects](/documentation/coredata/nsmanagedobjectcontext/notificationkey/refreshedobjects)
- [case updatedObjectIDs](/documentation/coredata/nsmanagedobjectcontext/notificationkey/updatedobjectids)
- [case updatedObjects](/documentation/coredata/nsmanagedobjectcontext/notificationkey/updatedobjects)

#### Managing unsaved and uncommitted changes

- [func save() throws](/documentation/coredata/nsmanagedobjectcontext/save())
- [var hasChanges: Bool](/documentation/coredata/nsmanagedobjectcontext/haschanges)

#### Undoing changes

- [var undoManager: UndoManager?](/documentation/coredata/nsmanagedobjectcontext/undomanager)
- [func undo()](/documentation/coredata/nsmanagedobjectcontext/undo())
- [func redo()](/documentation/coredata/nsmanagedobjectcontext/redo())
- [func reset()](/documentation/coredata/nsmanagedobjectcontext/reset())
- [func rollback()](/documentation/coredata/nsmanagedobjectcontext/rollback())

#### Handling delete propagation

- [var propagatesDeletesAtEndOfEvent: Bool](/documentation/coredata/nsmanagedobjectcontext/propagatesdeletesatendofevent)

#### Managing the staleness interval

- [var stalenessInterval: TimeInterval](/documentation/coredata/nsmanagedobjectcontext/stalenessinterval)

#### Performing block operations

- [func perform(() -> Void)](/documentation/coredata/nsmanagedobjectcontext/perform(_:))
- [func perform<T>(schedule: NSManagedObjectContext.ScheduledTaskType, () throws -> T) async rethrows -> T](/documentation/coredata/nsmanagedobjectcontext/perform(schedule:_:))
- [func performAndWait(() -> Void)](/documentation/coredata/nsmanagedobjectcontext/performandwait(_:)-ypye)
- [func performAndWait<T>(() throws -> T) rethrows -> T](/documentation/coredata/nsmanagedobjectcontext/performandwait(_:)-6aaf1)
- [NSManagedObjectContext.ScheduledTaskType](/documentation/coredata/nsmanagedobjectcontext/scheduledtasktype)

##### Scheduled Task Types

- [case enqueued](/documentation/coredata/nsmanagedobjectcontext/scheduledtasktype/enqueued)
- [case immediate](/documentation/coredata/nsmanagedobjectcontext/scheduledtasktype/immediate)

#### Deprecated

- [Deprecated symbols](/documentation/coredata/nsmanagedobjectcontext-deprecated-symbols)

##### Deprecated type methods

- [class func new() -> Self](/documentation/coredata/nsmanagedobjectcontext/new())

##### Deprecated instance methods

- [init(concurrencyType: NSManagedObjectContextConcurrencyType)](/documentation/coredata/nsmanagedobjectcontext/init(concurrencytype:))
- [convenience init()](/documentation/coredata/nsmanagedobjectcontext/init())
- [func lock()](/documentation/coredata/nsmanagedobjectcontext/lock())
- [func tryLock() -> Bool](/documentation/coredata/nsmanagedobjectcontext/trylock())
- [func unlock()](/documentation/coredata/nsmanagedobjectcontext/unlock())
- [NSManagedObject](/documentation/coredata/nsmanagedobject)

#### Creating a Managed Object

- [init(entity: NSEntityDescription, insertInto: NSManagedObjectContext?)](/documentation/coredata/nsmanagedobject/init(entity:insertinto:))
- [convenience init(context: NSManagedObjectContext)](/documentation/coredata/nsmanagedobject/init(context:))

#### Getting a Managed Object’s Identity

- [var entity: NSEntityDescription](/documentation/coredata/nsmanagedobject/entity-swift.property)
- [var objectID: NSManagedObjectID](/documentation/coredata/nsmanagedobject/objectid)
- [class func entity() -> NSEntityDescription](/documentation/coredata/nsmanagedobject/entity())

#### Getting State Information

- [var managedObjectContext: NSManagedObjectContext?](/documentation/coredata/nsmanagedobject/managedobjectcontext)
- [var hasChanges: Bool](/documentation/coredata/nsmanagedobject/haschanges)
- [var isInserted: Bool](/documentation/coredata/nsmanagedobject/isinserted)
- [var isUpdated: Bool](/documentation/coredata/nsmanagedobject/isupdated)
- [var isDeleted: Bool](/documentation/coredata/nsmanagedobject/isdeleted)
- [var isFault: Bool](/documentation/coredata/nsmanagedobject/isfault)
- [var faultingState: Int](/documentation/coredata/nsmanagedobject/faultingstate)
- [func hasFault(forRelationshipNamed: String) -> Bool](/documentation/coredata/nsmanagedobject/hasfault(forrelationshipnamed:))
- [var hasPersistentChangedValues: Bool](/documentation/coredata/nsmanagedobject/haspersistentchangedvalues)

#### Managing Change Events

- [class var contextShouldIgnoreUnmodeledPropertyChanges: Bool](/documentation/coredata/nsmanagedobject/contextshouldignoreunmodeledpropertychanges)
- [func awakeFromFetch()](/documentation/coredata/nsmanagedobject/awakefromfetch())
- [func awakeFromInsert()](/documentation/coredata/nsmanagedobject/awakefrominsert())
- [func awake(fromSnapshotEvents: NSSnapshotEventType)](/documentation/coredata/nsmanagedobject/awake(fromsnapshotevents:))
- [func changedValues() -> [String : Any]](/documentation/coredata/nsmanagedobject/changedvalues())
- [func changedValuesForCurrentEvent() -> [String : Any]](/documentation/coredata/nsmanagedobject/changedvaluesforcurrentevent())
- [func committedValues(forKeys: [String]?) -> [String : Any]](/documentation/coredata/nsmanagedobject/committedvalues(forkeys:))
- [func prepareForDeletion()](/documentation/coredata/nsmanagedobject/preparefordeletion())
- [func willSave()](/documentation/coredata/nsmanagedobject/willsave())
- [func didSave()](/documentation/coredata/nsmanagedobject/didsave())
- [func willTurnIntoFault()](/documentation/coredata/nsmanagedobject/willturnintofault())
- [func didTurnIntoFault()](/documentation/coredata/nsmanagedobject/didturnintofault())
- [class func fetchRequest() -> NSFetchRequest<any NSFetchRequestResult>](/documentation/coredata/nsmanagedobject/fetchrequest())

#### Supporting Key-Value Coding

- [func value(forKey: String) -> Any?](/documentation/coredata/nsmanagedobject/value(forkey:))
- [func setValue(Any?, forKey: String)](/documentation/coredata/nsmanagedobject/setvalue(_:forkey:))
- [func primitiveValue(forKey: String) -> Any?](/documentation/coredata/nsmanagedobject/primitivevalue(forkey:))
- [func setPrimitiveValue(Any?, forKey: String)](/documentation/coredata/nsmanagedobject/setprimitivevalue(_:forkey:))
- [func objectIDs(forRelationshipNamed: String) -> [NSManagedObjectID]](/documentation/coredata/nsmanagedobject/objectids(forrelationshipnamed:))

#### Managing Data Validation

- [func validateValue(AutoreleasingUnsafeMutablePointer<AnyObject?>, forKey: String) throws](/documentation/coredata/nsmanagedobject/validatevalue(_:forkey:))
- [func validateForDelete() throws](/documentation/coredata/nsmanagedobject/validatefordelete())
- [func validateForInsert() throws](/documentation/coredata/nsmanagedobject/validateforinsert())
- [func validateForUpdate() throws](/documentation/coredata/nsmanagedobject/validateforupdate())
- [Validation error codes](/documentation/coredata/1535452-validation-error-codes)

##### Error codes

- [var NSCoreDataError: Int](/documentation/coredata/nscoredataerror)
- [var NSEntityMigrationPolicyError: Int](/documentation/coredata/nsentitymigrationpolicyerror)
- [var NSExternalRecordImportError: Int](/documentation/coredata/nsexternalrecordimporterror)
- [var NSInferredMappingModelError: Int](/documentation/coredata/nsinferredmappingmodelerror)
- [var NSManagedObjectConstraintMergeError: Int](/documentation/coredata/nsmanagedobjectconstraintmergeerror)
- [var NSManagedObjectConstraintValidationError: Int](/documentation/coredata/nsmanagedobjectconstraintvalidationerror)
- [var NSManagedObjectContextLockingError: Int](/documentation/coredata/nsmanagedobjectcontextlockingerror)
- [var NSManagedObjectExternalRelationshipError: Int](/documentation/coredata/nsmanagedobjectexternalrelationshiperror)
- [var NSManagedObjectMergeError: Int](/documentation/coredata/nsmanagedobjectmergeerror)
- [var NSManagedObjectModelReferenceNotFoundError: Int](/documentation/coredata/nsmanagedobjectmodelreferencenotfounderror)
- [var NSManagedObjectReferentialIntegrityError: Int](/documentation/coredata/nsmanagedobjectreferentialintegrityerror)
- [var NSManagedObjectValidationError: Int](/documentation/coredata/nsmanagedobjectvalidationerror)
- [var NSMigrationCancelledError: Int](/documentation/coredata/nsmigrationcancellederror)
- [var NSMigrationConstraintViolationError: Int](/documentation/coredata/nsmigrationconstraintviolationerror)
- [var NSMigrationError: Int](/documentation/coredata/nsmigrationerror)
- [var NSMigrationManagerDestinationStoreError: Int](/documentation/coredata/nsmigrationmanagerdestinationstoreerror)
- [var NSMigrationManagerSourceStoreError: Int](/documentation/coredata/nsmigrationmanagersourcestoreerror)
- [var NSMigrationMissingMappingModelError: Int](/documentation/coredata/nsmigrationmissingmappingmodelerror)
- [var NSMigrationMissingSourceModelError: Int](/documentation/coredata/nsmigrationmissingsourcemodelerror)
- [var NSPersistentHistoryTokenExpiredError: Int](/documentation/coredata/nspersistenthistorytokenexpirederror)
- [var NSPersistentStoreCoordinatorLockingError: Int](/documentation/coredata/nspersistentstorecoordinatorlockingerror)
- [var NSPersistentStoreIncompatibleSchemaError: Int](/documentation/coredata/nspersistentstoreincompatibleschemaerror)
- [var NSPersistentStoreIncompatibleVersionHashError: Int](/documentation/coredata/nspersistentstoreincompatibleversionhasherror)
- [var NSPersistentStoreIncompleteSaveError: Int](/documentation/coredata/nspersistentstoreincompletesaveerror)
- [var NSPersistentStoreInvalidTypeError: Int](/documentation/coredata/nspersistentstoreinvalidtypeerror)
- [var NSPersistentStoreOpenError: Int](/documentation/coredata/nspersistentstoreopenerror)
- [var NSPersistentStoreOperationError: Int](/documentation/coredata/nspersistentstoreoperationerror)
- [var NSPersistentStoreSaveConflictsError: Int](/documentation/coredata/nspersistentstoresaveconflictserror)
- [var NSPersistentStoreSaveError: Int](/documentation/coredata/nspersistentstoresaveerror)
- [var NSPersistentStoreTimeoutError: Int](/documentation/coredata/nspersistentstoretimeouterror)
- [var NSPersistentStoreTypeMismatchError: Int](/documentation/coredata/nspersistentstoretypemismatcherror)
- [var NSPersistentStoreUnsupportedRequestTypeError: Int](/documentation/coredata/nspersistentstoreunsupportedrequesttypeerror)
- [var NSSQLiteError: Int](/documentation/coredata/nssqliteerror)
- [var NSStagedMigrationBackwardMigrationError: Int](/documentation/coredata/nsstagedmigrationbackwardmigrationerror)
- [var NSStagedMigrationFrameworkVersionMismatchError: Int](/documentation/coredata/nsstagedmigrationframeworkversionmismatcherror)
- [var NSValidationInvalidURIError: Int](/documentation/coredata/nsvalidationinvalidurierror)
- [var NSValidationMultipleErrorsError: Int](/documentation/coredata/nsvalidationmultipleerrorserror)
- [var NSValidationMissingMandatoryPropertyError: Int](/documentation/coredata/nsvalidationmissingmandatorypropertyerror)
- [var NSValidationRelationshipLacksMinimumCountError: Int](/documentation/coredata/nsvalidationrelationshiplacksminimumcounterror)
- [var NSValidationRelationshipExceedsMaximumCountError: Int](/documentation/coredata/nsvalidationrelationshipexceedsmaximumcounterror)
- [var NSValidationRelationshipDeniedDeleteError: Int](/documentation/coredata/nsvalidationrelationshipdenieddeleteerror)
- [var NSValidationNumberTooLargeError: Int](/documentation/coredata/nsvalidationnumbertoolargeerror)
- [var NSValidationNumberTooSmallError: Int](/documentation/coredata/nsvalidationnumbertoosmallerror)
- [var NSValidationDateTooLateError: Int](/documentation/coredata/nsvalidationdatetoolateerror)
- [var NSValidationDateTooSoonError: Int](/documentation/coredata/nsvalidationdatetoosoonerror)
- [var NSValidationInvalidDateError: Int](/documentation/coredata/nsvalidationinvaliddateerror)
- [var NSValidationStringTooLongError: Int](/documentation/coredata/nsvalidationstringtoolongerror)
- [var NSValidationStringTooShortError: Int](/documentation/coredata/nsvalidationstringtooshorterror)
- [var NSValidationStringPatternMatchingError: Int](/documentation/coredata/nsvalidationstringpatternmatchingerror)
- [let NSValidationKeyErrorKey: String](/documentation/coredata/nsvalidationkeyerrorkey)
- [let NSValidationObjectErrorKey: String](/documentation/coredata/nsvalidationobjecterrorkey)
- [let NSValidationPredicateErrorKey: String](/documentation/coredata/nsvalidationpredicateerrorkey)
- [let NSValidationValueErrorKey: String](/documentation/coredata/nsvalidationvalueerrorkey)

#### Supporting Key-Value Observing

- [func didAccessValue(forKey: String?)](/documentation/coredata/nsmanagedobject/didaccessvalue(forkey:))
- [func observationInfo() -> UnsafeMutableRawPointer?](/documentation/coredata/nsmanagedobject/observationinfo())
- [func setObservationInfo(UnsafeMutableRawPointer?)](/documentation/coredata/nsmanagedobject/setobservationinfo(_:))
- [func willAccessValue(forKey: String?)](/documentation/coredata/nsmanagedobject/willaccessvalue(forkey:))
- [func didChangeValue(forKey: String)](/documentation/coredata/nsmanagedobject/didchangevalue(forkey:))
- [func didChangeValue(forKey: String, withSetMutation: NSKeyValueSetMutationKind, using: Set<AnyHashable>)](/documentation/coredata/nsmanagedobject/didchangevalue(forkey:withsetmutation:using:))
- [func willChangeValue(forKey: String)](/documentation/coredata/nsmanagedobject/willchangevalue(forkey:))
- [func willChangeValue(forKey: String, withSetMutation: NSKeyValueSetMutationKind, using: Set<AnyHashable>)](/documentation/coredata/nsmanagedobject/willchangevalue(forkey:withsetmutation:using:))

#### Reinitializing Values

- [NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype)

##### Event Types

- [static var undoInsertion: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/undoinsertion)
- [static var undoDeletion: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/undodeletion)
- [static var undoUpdate: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/undoupdate)
- [static var rollback: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/rollback)
- [static var refresh: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/refresh)
- [static var mergePolicy: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/mergepolicy)

##### Initializers

- [init(rawValue: UInt)](/documentation/coredata/nssnapshoteventtype/init(rawvalue:))

#### Subscripts

- [subscript(String) -> Any?](/documentation/coredata/nsmanagedobject/subscript(_:))
- [NSManagedObjectID](/documentation/coredata/nsmanagedobjectid)

#### Getting Managed Object ID Information

- [var entity: NSEntityDescription](/documentation/coredata/nsmanagedobjectid/entity)
- [var isTemporaryID: Bool](/documentation/coredata/nsmanagedobjectid/istemporaryid)
- [var persistentStore: NSPersistentStore?](/documentation/coredata/nsmanagedobjectid/persistentstore)
- [func uriRepresentation() -> URL](/documentation/coredata/nsmanagedobjectid/urirepresentation())

### Store Coordination

- [NSPersistentStoreCoordinator](/documentation/coredata/nspersistentstorecoordinator)

#### Creating a persistent store coordinator

- [init(managedObjectModel: NSManagedObjectModel)](/documentation/coredata/nspersistentstorecoordinator/init(managedobjectmodel:))
- [Store options](/documentation/coredata/store-options)

##### Constants

- [let NSReadOnlyPersistentStoreOption: String](/documentation/coredata/nsreadonlypersistentstoreoption)
- [let NSValidateXMLStoreOption: String](/documentation/coredata/nsvalidatexmlstoreoption)
- [let NSPersistentStoreTimeoutOption: String](/documentation/coredata/nspersistentstoretimeoutoption)
- [let NSSQLitePragmasOption: String](/documentation/coredata/nssqlitepragmasoption)
- [let NSSQLiteAnalyzeOption: String](/documentation/coredata/nssqliteanalyzeoption)
- [let NSSQLiteManualVacuumOption: String](/documentation/coredata/nssqlitemanualvacuumoption)
- [let NSPersistentStoreFileProtectionKey: String](/documentation/coredata/nspersistentstorefileprotectionkey)
- [let NSPersistentStoreForceDestroyOption: String](/documentation/coredata/nspersistentstoreforcedestroyoption)

##### Deprecated

- [let NSExternalRecordsDirectoryOption: String](/documentation/coredata/nsexternalrecordsdirectoryoption)
- [let NSExternalRecordExtensionOption: String](/documentation/coredata/nsexternalrecordextensionoption)
- [let NSExternalRecordsFileFormatOption: String](/documentation/coredata/nsexternalrecordsfileformatoption)
- [let NSPersistentStoreUbiquitousContentNameKey: String](/documentation/coredata/nspersistentstoreubiquitouscontentnamekey)
- [let NSPersistentStoreUbiquitousContentURLKey: String](/documentation/coredata/nspersistentstoreubiquitouscontenturlkey)
- [let NSPersistentStoreUbiquitousPeerTokenOption: String](/documentation/coredata/nspersistentstoreubiquitouspeertokenoption)
- [let NSPersistentStoreRemoveUbiquitousMetadataOption: String](/documentation/coredata/nspersistentstoreremoveubiquitousmetadataoption)
- [let NSPersistentStoreUbiquitousContainerIdentifierKey: String](/documentation/coredata/nspersistentstoreubiquitouscontaineridentifierkey)
- [let NSPersistentStoreRebuildFromUbiquitousContentOption: String](/documentation/coredata/nspersistentstorerebuildfromubiquitouscontentoption)
- [Migration options](/documentation/coredata/migration-options)

##### Constants

- [let NSIgnorePersistentStoreVersioningOption: String](/documentation/coredata/nsignorepersistentstoreversioningoption)
- [let NSMigratePersistentStoresAutomaticallyOption: String](/documentation/coredata/nsmigratepersistentstoresautomaticallyoption)
- [let NSInferMappingModelAutomaticallyOption: String](/documentation/coredata/nsinfermappingmodelautomaticallyoption)
- [Store versions](/documentation/coredata/store-versions)

##### Constants

- [let NSStoreModelVersionHashesKey: String](/documentation/coredata/nsstoremodelversionhasheskey)
- [let NSStoreModelVersionIdentifiersKey: String](/documentation/coredata/nsstoremodelversionidentifierskey)
- [let NSPersistentStoreOSCompatibility: String](/documentation/coredata/nspersistentstoreoscompatibility)

#### Managing configuration

- [var name: String?](/documentation/coredata/nspersistentstorecoordinator/name)
- [var managedObjectModel: NSManagedObjectModel](/documentation/coredata/nspersistentstorecoordinator/managedobjectmodel)
- [var persistentStores: [NSPersistentStore]](/documentation/coredata/nspersistentstorecoordinator/persistentstores)

#### Registering store types

- [class func registerStoreClass(AnyClass?, type: NSPersistentStore.StoreType)](/documentation/coredata/nspersistentstorecoordinator/registerstoreclass(_:type:))
- [class func registerStoreClass(AnyClass?, forStoreType: String)](/documentation/coredata/nspersistentstorecoordinator/registerstoreclass(_:forstoretype:))
- [class var registeredStoreTypes: [String : NSValue]](/documentation/coredata/nspersistentstorecoordinator/registeredstoretypes)

#### Adding or removing a store

- [func addPersistentStore(type: NSPersistentStore.StoreType, configuration: String?, at: URL, options: [AnyHashable : Any]?) throws -> NSPersistentStore](/documentation/coredata/nspersistentstorecoordinator/addpersistentstore(type:configuration:at:options:))
- [func addPersistentStore(ofType: String, configurationName: String?, at: URL?, options: [AnyHashable : Any]?) throws -> NSPersistentStore](/documentation/coredata/nspersistentstorecoordinator/addpersistentstore(oftype:configurationname:at:options:))
- [func addPersistentStore(with: NSPersistentStoreDescription, completionHandler: (NSPersistentStoreDescription, (any Error)?) -> Void)](/documentation/coredata/nspersistentstorecoordinator/addpersistentstore(with:completionhandler:))
- [func remove(NSPersistentStore) throws](/documentation/coredata/nspersistentstorecoordinator/remove(_:))

#### Modifying a store

- [func destroyPersistentStore(at: URL, type: NSPersistentStore.StoreType, options: [AnyHashable : Any]?) throws](/documentation/coredata/nspersistentstorecoordinator/destroypersistentstore(at:type:options:))
- [func migratePersistentStore(NSPersistentStore, to: URL, options: [AnyHashable : Any]?, type: NSPersistentStore.StoreType) throws -> NSPersistentStore](/documentation/coredata/nspersistentstorecoordinator/migratepersistentstore(_:to:options:type:))
- [func replacePersistentStore(at: URL, destinationOptions: [AnyHashable : Any]?, withPersistentStoreFrom: URL, sourceOptions: [AnyHashable : Any]?, type: NSPersistentStore.StoreType) throws](/documentation/coredata/nspersistentstorecoordinator/replacepersistentstore(at:destinationoptions:withpersistentstorefrom:sourceoptions:type:))
- [func destroyPersistentStore(at: URL, ofType: String, options: [AnyHashable : Any]?) throws](/documentation/coredata/nspersistentstorecoordinator/destroypersistentstore(at:oftype:options:))
- [func migratePersistentStore(NSPersistentStore, to: URL, options: [AnyHashable : Any]?, withType: String) throws -> NSPersistentStore](/documentation/coredata/nspersistentstorecoordinator/migratepersistentstore(_:to:options:withtype:))
- [func replacePersistentStore(at: URL, destinationOptions: [AnyHashable : Any]?, withPersistentStoreFrom: URL, sourceOptions: [AnyHashable : Any]?, ofType: String) throws](/documentation/coredata/nspersistentstorecoordinator/replacepersistentstore(at:destinationoptions:withpersistentstorefrom:sourceoptions:oftype:))

#### Managing a store’s location

- [func setURL(URL, for: NSPersistentStore) -> Bool](/documentation/coredata/nspersistentstorecoordinator/seturl(_:for:))
- [func persistentStore(for: URL) -> NSPersistentStore?](/documentation/coredata/nspersistentstorecoordinator/persistentstore(for:))
- [func url(for: NSPersistentStore) -> URL](/documentation/coredata/nspersistentstorecoordinator/url(for:))

#### Managing a store’s metadata

- [class func setMetadata([String : Any]?, type: NSPersistentStore.StoreType, at: URL, options: [AnyHashable : Any]?) throws](/documentation/coredata/nspersistentstorecoordinator/setmetadata(_:type:at:options:))
- [class func metadataForPersistentStore(type: NSPersistentStore.StoreType, at: URL, options: [AnyHashable : Any]?) throws -> [String : Any]](/documentation/coredata/nspersistentstorecoordinator/metadataforpersistentstore(type:at:options:))
- [class func setMetadata([String : Any]?, forPersistentStoreOfType: String, at: URL, options: [AnyHashable : Any]?) throws](/documentation/coredata/nspersistentstorecoordinator/setmetadata(_:forpersistentstoreoftype:at:options:))
- [class func metadataForPersistentStore(ofType: String, at: URL, options: [AnyHashable : Any]?) throws -> [String : Any]](/documentation/coredata/nspersistentstorecoordinator/metadataforpersistentstore(oftype:at:options:))
- [func metadata(for: NSPersistentStore) -> [String : Any]](/documentation/coredata/nspersistentstorecoordinator/metadata(for:))
- [func setMetadata([String : Any]?, for: NSPersistentStore)](/documentation/coredata/nspersistentstorecoordinator/setmetadata(_:for:))
- [let NSStoreTypeKey: String](/documentation/coredata/nsstoretypekey)
- [let NSStoreUUIDKey: String](/documentation/coredata/nsstoreuuidkey)

#### Deferring a store’s migrations

- [let NSPersistentStoreDeferredLightweightMigrationOptionKey: String](/documentation/coredata/nspersistentstoredeferredlightweightmigrationoptionkey)
- [func finishDeferredLightweightMigrationTask() throws](/documentation/coredata/nspersistentstorecoordinator/finishdeferredlightweightmigrationtask())
- [func finishDeferredLightweightMigration() throws](/documentation/coredata/nspersistentstorecoordinator/finishdeferredlightweightmigration())

#### Performing tasks

- [func perform<T>(() throws -> T) async rethrows -> T](/documentation/coredata/nspersistentstorecoordinator/perform(_:)-74udx)
- [func performAndWait<T>(() throws -> T) rethrows -> T](/documentation/coredata/nspersistentstorecoordinator/performandwait(_:)-15ude)
- [func perform(() -> Void)](/documentation/coredata/nspersistentstorecoordinator/perform(_:)-7jqb)
- [func performAndWait(() -> Void)](/documentation/coredata/nspersistentstorecoordinator/performandwait(_:)-d3kq)
- [func execute(NSPersistentStoreRequest, with: NSManagedObjectContext) throws -> Any](/documentation/coredata/nspersistentstorecoordinator/execute(_:with:))

#### Maintaining a record of changes

- [let NSPersistentHistoryTrackingKey: String](/documentation/coredata/nspersistenthistorytrackingkey)
- [func currentPersistentHistoryToken(fromStores: [Any]?) -> NSPersistentHistoryToken?](/documentation/coredata/nspersistentstorecoordinator/currentpersistenthistorytoken(fromstores:))

#### Integrating with Spotlight

- [let NSCoreDataCoreSpotlightExporter: String](/documentation/coredata/nscoredatacorespotlightexporter)
- [NSCoreDataCoreSpotlightDelegate](/documentation/coredata/nscoredatacorespotlightdelegate)

##### Creating a Core Spotlight Delegate

- [init(forStoreWith: NSPersistentStoreDescription, coordinator: NSPersistentStoreCoordinator)](/documentation/coredata/nscoredatacorespotlightdelegate/init(forstorewith:coordinator:))
- [convenience init(forStoreWith: NSPersistentStoreDescription, model: NSManagedObjectModel)](/documentation/coredata/nscoredatacorespotlightdelegate/init(forstorewith:model:))

##### Configuring the Index

- [var isIndexingEnabled: Bool](/documentation/coredata/nscoredatacorespotlightdelegate/isindexingenabled)
- [func domainIdentifier() -> String](/documentation/coredata/nscoredatacorespotlightdelegate/domainidentifier())
- [func indexName() -> String?](/documentation/coredata/nscoredatacorespotlightdelegate/indexname())

##### Managing the Index

- [func attributeSet(for: NSManagedObject) -> CSSearchableItemAttributeSet?](/documentation/coredata/nscoredatacorespotlightdelegate/attributeset(for:))
- [func deleteSpotlightIndex(completionHandler: ((any Error)?) -> Void)](/documentation/coredata/nscoredatacorespotlightdelegate/deletespotlightindex(completionhandler:))
- [func startSpotlightIndexing()](/documentation/coredata/nscoredatacorespotlightdelegate/startspotlightindexing())
- [func stopSpotlightIndexing()](/documentation/coredata/nscoredatacorespotlightdelegate/stopspotlightindexing())

##### Updating the Index

- [static let indexDidUpdateNotification: Notification.Name](/documentation/coredata/nscoredatacorespotlightdelegate/indexdidupdatenotification)
- [func searchableIndex(CSSearchableIndex, reindexAllSearchableItemsWithAcknowledgementHandler: () -> Void)](/documentation/coredata/nscoredatacorespotlightdelegate/searchableindex(_:reindexallsearchableitemswithacknowledgementhandler:))
- [func searchableIndex(CSSearchableIndex, reindexSearchableItemsWithIdentifiers: [String], acknowledgementHandler: () -> Void)](/documentation/coredata/nscoredatacorespotlightdelegate/searchableindex(_:reindexsearchableitemswithidentifiers:acknowledgementhandler:))
- [Spotlight record keys](/documentation/coredata/spotlight-record-keys)

##### Constants

- [let NSEntityNameInPathKey: String](/documentation/coredata/nsentitynameinpathkey)
- [let NSStoreUUIDInPathKey: String](/documentation/coredata/nsstoreuuidinpathkey)
- [let NSStorePathKey: String](/documentation/coredata/nsstorepathkey)
- [let NSModelPathKey: String](/documentation/coredata/nsmodelpathkey)
- [let NSObjectURIKey: String](/documentation/coredata/nsobjecturikey)
- [Showcase App Data in Spotlight](/documentation/coredata/showcase-app-data-in-spotlight)

#### Getting individual object identifiers

- [func managedObjectID(forURIRepresentation: URL) -> NSManagedObjectID?](/documentation/coredata/nspersistentstorecoordinator/managedobjectid(forurirepresentation:))

#### Responding to changes of the coordinator’s registered stores

- [static let NSPersistentStoreCoordinatorStoresWillChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspersistentstorecoordinatorstoreswillchange)
- [static let NSPersistentStoreCoordinatorStoresDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspersistentstorecoordinatorstoresdidchange)
- [static let NSPersistentStoreCoordinatorWillRemoveStore: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspersistentstorecoordinatorwillremovestore)
- [Notification keys](/documentation/coredata/notification-keys)

##### Constants

- [let NSAddedPersistentStoresKey: String](/documentation/coredata/nsaddedpersistentstoreskey)
- [let NSRemovedPersistentStoresKey: String](/documentation/coredata/nsremovedpersistentstoreskey)
- [let NSUUIDChangedPersistentStoresKey: String](/documentation/coredata/nsuuidchangedpersistentstoreskey)
- [let NSPersistentStoreConnectionPoolMaxSizeKey: String](/documentation/coredata/nspersistentstoreconnectionpoolmaxsizekey)
- [let NSPersistentStoreSaveConflictsErrorKey: String](/documentation/coredata/nspersistentstoresaveconflictserrorkey)
- [let NSPersistentStoreUbiquitousTransitionTypeKey: String](/documentation/coredata/nspersistentstoreubiquitoustransitiontypekey)

#### Deprecated

- [Deprecated Symbols](/documentation/coredata/nspersistentstorecoordinator-deprecated-symbols)

##### Deprecated constants

- [let NSXMLExternalRecordType: String](/documentation/coredata/nsxmlexternalrecordtype)
- [let NSBinaryExternalRecordType: String](/documentation/coredata/nsbinaryexternalrecordtype)

##### Deprecated enumerations

- [NSPersistentStoreUbiquitousTransitionType](/documentation/coredata/nspersistentstoreubiquitoustransitiontype)

###### Constants

- [case accountAdded](/documentation/coredata/nspersistentstoreubiquitoustransitiontype/accountadded)
- [case accountRemoved](/documentation/coredata/nspersistentstoreubiquitoustransitiontype/accountremoved)
- [case contentRemoved](/documentation/coredata/nspersistentstoreubiquitoustransitiontype/contentremoved)
- [case initialImportCompleted](/documentation/coredata/nspersistentstoreubiquitoustransitiontype/initialimportcompleted)

###### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nspersistentstoreubiquitoustransitiontype/init(rawvalue:))

##### Deprecated type properties

- [static let NSPersistentStoreDidImportUbiquitousContentChanges: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/nspersistentstoredidimportubiquitouscontentchanges)

##### Deprecated type methods

- [class func elementsDerived(fromExternalRecordAt: URL) -> [AnyHashable : Any]](/documentation/coredata/nspersistentstorecoordinator/elementsderived(fromexternalrecordat:))
- [class func metadataForPersistentStore(with: URL) throws -> [AnyHashable : Any]](/documentation/coredata/nspersistentstorecoordinator/metadataforpersistentstore(with:))
- [class func metadataForPersistentStore(ofType: String?, at: URL) throws -> [String : Any]](/documentation/coredata/nspersistentstorecoordinator/metadataforpersistentstore(oftype:at:))
- [class func metadataForPersistentStore(ofType: String, at: URL, options: [AnyHashable : Any]?) throws -> [String : Any]](/documentation/coredata/nspersistentstorecoordinator/metadataforpersistentstore(oftype:at:options:))
- [class func registerStoreClass(AnyClass?, forStoreType: String)](/documentation/coredata/nspersistentstorecoordinator/registerstoreclass(_:forstoretype:))
- [class func removeUbiquitousContentAndPersistentStore(at: URL, options: [AnyHashable : Any]?) throws](/documentation/coredata/nspersistentstorecoordinator/removeubiquitouscontentandpersistentstore(at:options:))
- [class func setMetadata([String : Any]?, forPersistentStoreOfType: String?, at: URL) throws](/documentation/coredata/nspersistentstorecoordinator/setmetadata(_:forpersistentstoreoftype:at:))
- [class func setMetadata([String : Any]?, forPersistentStoreOfType: String, at: URL, options: [AnyHashable : Any]?) throws](/documentation/coredata/nspersistentstorecoordinator/setmetadata(_:forpersistentstoreoftype:at:options:))

##### Deprecated instance methods

- [func addPersistentStore(ofType: String, configurationName: String?, at: URL?, options: [AnyHashable : Any]?) throws -> NSPersistentStore](/documentation/coredata/nspersistentstorecoordinator/addpersistentstore(oftype:configurationname:at:options:))
- [func destroyPersistentStore(at: URL, ofType: String, options: [AnyHashable : Any]?) throws](/documentation/coredata/nspersistentstorecoordinator/destroypersistentstore(at:oftype:options:))
- [func importStore(withIdentifier: String?, fromExternalRecordsDirectoryAt: URL, to: URL, options: [AnyHashable : Any]?, ofType: String) throws -> NSPersistentStore](/documentation/coredata/nspersistentstorecoordinator/importstore(withidentifier:fromexternalrecordsdirectoryat:to:options:oftype:))
- [func lock()](/documentation/coredata/nspersistentstorecoordinator/lock())
- [func migratePersistentStore(NSPersistentStore, to: URL, options: [AnyHashable : Any]?, withType: String) throws -> NSPersistentStore](/documentation/coredata/nspersistentstorecoordinator/migratepersistentstore(_:to:options:withtype:))
- [func replacePersistentStore(at: URL, destinationOptions: [AnyHashable : Any]?, withPersistentStoreFrom: URL, sourceOptions: [AnyHashable : Any]?, ofType: String) throws](/documentation/coredata/nspersistentstorecoordinator/replacepersistentstore(at:destinationoptions:withpersistentstorefrom:sourceoptions:oftype:))
- [func tryLock() -> Bool](/documentation/coredata/nspersistentstorecoordinator/trylock())
- [func unlock()](/documentation/coredata/nspersistentstorecoordinator/unlock())
- [func perform(() -> Void)](/documentation/coredata/nspersistentstorecoordinator/perform(_:)-7jqb)
- [func performAndWait(() -> Void)](/documentation/coredata/nspersistentstorecoordinator/performandwait(_:)-d3kq)

#### Instance Methods

- [func managedObjectID(for: String) -> NSManagedObjectID?](/documentation/coredata/nspersistentstorecoordinator/managedobjectid(for:))
- [NSPersistentStore](/documentation/coredata/nspersistentstore)

#### Creating a Persistent Store

- [init(persistentStoreCoordinator: NSPersistentStoreCoordinator?, configurationName: String?, at: URL, options: [AnyHashable : Any]?)](/documentation/coredata/nspersistentstore/init(persistentstorecoordinator:configurationname:at:options:))

#### Getting Store Configuration

- [var configurationName: String](/documentation/coredata/nspersistentstore/configurationname)
- [var options: [AnyHashable : Any]?](/documentation/coredata/nspersistentstore/options)
- [var persistentStoreCoordinator: NSPersistentStoreCoordinator?](/documentation/coredata/nspersistentstore/persistentstorecoordinator)
- [var type: String](/documentation/coredata/nspersistentstore/type)
- [NSPersistentStore.StoreType](/documentation/coredata/nspersistentstore/storetype)

##### Store Types

- [static let binary: NSPersistentStore.StoreType](/documentation/coredata/nspersistentstore/storetype/binary)
- [static let inMemory: NSPersistentStore.StoreType](/documentation/coredata/nspersistentstore/storetype/inmemory)
- [static let sqlite: NSPersistentStore.StoreType](/documentation/coredata/nspersistentstore/storetype/sqlite)
- [static let xml: NSPersistentStore.StoreType](/documentation/coredata/nspersistentstore/storetype/xml)
- [Persistent Store Types](/documentation/coredata/persistent-store-types)

##### Constants

- [let NSSQLiteStoreType: String](/documentation/coredata/nssqlitestoretype)
- [let NSXMLStoreType: String](/documentation/coredata/nsxmlstoretype)
- [let NSBinaryStoreType: String](/documentation/coredata/nsbinarystoretype)
- [let NSInMemoryStoreType: String](/documentation/coredata/nsinmemorystoretype)

#### Managing Store Attributes

- [var identifier: String!](/documentation/coredata/nspersistentstore/identifier)
- [var isReadOnly: Bool](/documentation/coredata/nspersistentstore/isreadonly)
- [var url: URL?](/documentation/coredata/nspersistentstore/url)

#### Managing Store Metadata

- [class func metadataForPersistentStore(with: URL) throws -> [String : Any]](/documentation/coredata/nspersistentstore/metadataforpersistentstore(with:))
- [class func setMetadata([String : Any]?, forPersistentStoreAt: URL) throws](/documentation/coredata/nspersistentstore/setmetadata(_:forpersistentstoreat:))
- [func loadMetadata() throws](/documentation/coredata/nspersistentstore/loadmetadata())
- [var metadata: [String : Any]!](/documentation/coredata/nspersistentstore/metadata)

#### Responding to the Store Life Cycle

- [func didAdd(to: NSPersistentStoreCoordinator)](/documentation/coredata/nspersistentstore/didadd(to:))
- [func willRemove(from: NSPersistentStoreCoordinator?)](/documentation/coredata/nspersistentstore/willremove(from:))

#### Integrating with Spotlight

- [var coreSpotlightExporter: NSCoreDataCoreSpotlightDelegate](/documentation/coredata/nspersistentstore/corespotlightexporter)

#### Providing a Migration Manager

- [class func migrationManagerClass() -> AnyClass](/documentation/coredata/nspersistentstore/migrationmanagerclass())
- [NSPersistentStoreDescription](/documentation/coredata/nspersistentstoredescription)

#### Creating a Persistent Store Description

- [init(url: URL)](/documentation/coredata/nspersistentstoredescription/init(url:))

#### Configuring a Persistent Store Description

- [var url: URL?](/documentation/coredata/nspersistentstoredescription/url)
- [var configuration: String?](/documentation/coredata/nspersistentstoredescription/configuration)
- [var timeout: TimeInterval](/documentation/coredata/nspersistentstoredescription/timeout)
- [var type: String](/documentation/coredata/nspersistentstoredescription/type)
- [var isReadOnly: Bool](/documentation/coredata/nspersistentstoredescription/isreadonly)
- [var shouldAddStoreAsynchronously: Bool](/documentation/coredata/nspersistentstoredescription/shouldaddstoreasynchronously)
- [var shouldInferMappingModelAutomatically: Bool](/documentation/coredata/nspersistentstoredescription/shouldinfermappingmodelautomatically)
- [var shouldMigrateStoreAutomatically: Bool](/documentation/coredata/nspersistentstoredescription/shouldmigratestoreautomatically)
- [func setOption(NSObject?, forKey: String)](/documentation/coredata/nspersistentstoredescription/setoption(_:forkey:))
- [func setValue(NSObject?, forPragmaNamed: String)](/documentation/coredata/nspersistentstoredescription/setvalue(_:forpragmanamed:))

#### Accessing the Configuration Options

- [var options: [String : NSObject]](/documentation/coredata/nspersistentstoredescription/options)
- [var sqlitePragmas: [String : NSObject]](/documentation/coredata/nspersistentstoredescription/sqlitepragmas)

#### Syncing to CloudKit

- [var cloudKitContainerOptions: NSPersistentCloudKitContainerOptions?](/documentation/coredata/nspersistentstoredescription/cloudkitcontaineroptions)
- [NSPersistentStoreRequest](/documentation/coredata/nspersistentstorerequest)

#### Configuring a Request

- [var affectedStores: [NSPersistentStore]?](/documentation/coredata/nspersistentstorerequest/affectedstores)
- [var requestType: NSPersistentStoreRequestType](/documentation/coredata/nspersistentstorerequest/requesttype)
- [NSPersistentStoreRequestType](/documentation/coredata/nspersistentstorerequesttype)

##### Constants

- [case fetchRequestType](/documentation/coredata/nspersistentstorerequesttype/fetchrequesttype)
- [case saveRequestType](/documentation/coredata/nspersistentstorerequesttype/saverequesttype)
- [case batchInsertRequestType](/documentation/coredata/nspersistentstorerequesttype/batchinsertrequesttype)
- [case batchUpdateRequestType](/documentation/coredata/nspersistentstorerequesttype/batchupdaterequesttype)
- [case batchDeleteRequestType](/documentation/coredata/nspersistentstorerequesttype/batchdeleterequesttype)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nspersistentstorerequesttype/init(rawvalue:))
- [NSPersistentStoreResult](/documentation/coredata/nspersistentstoreresult)
- [NSPersistentStoreAsynchronousResult](/documentation/coredata/nspersistentstoreasynchronousresult)

#### Inspecting the Result

- [var managedObjectContext: NSManagedObjectContext](/documentation/coredata/nspersistentstoreasynchronousresult/managedobjectcontext)
- [var operationError: (any Error)?](/documentation/coredata/nspersistentstoreasynchronousresult/operationerror)
- [var progress: Progress?](/documentation/coredata/nspersistentstoreasynchronousresult/progress)

#### Canceling the Result

- [func cancel()](/documentation/coredata/nspersistentstoreasynchronousresult/cancel())

#### Data Types

- [NSPersistentStoreAsynchronousFetchResultCompletionBlock](/documentation/coredata/nspersistentstoreasynchronousfetchresultcompletionblock)
- [NSSaveChangesRequest](/documentation/coredata/nssavechangesrequest)

#### Initializing a Request

- [init(inserted: Set<NSManagedObject>?, updated: Set<NSManagedObject>?, deleted: Set<NSManagedObject>?, locked: Set<NSManagedObject>?)](/documentation/coredata/nssavechangesrequest/init(inserted:updated:deleted:locked:))

#### Getting Information about a Request

- [var insertedObjects: Set<NSManagedObject>?](/documentation/coredata/nssavechangesrequest/insertedobjects)
- [var updatedObjects: Set<NSManagedObject>?](/documentation/coredata/nssavechangesrequest/updatedobjects)
- [var deletedObjects: Set<NSManagedObject>?](/documentation/coredata/nssavechangesrequest/deletedobjects)
- [var lockedObjects: Set<NSManagedObject>?](/documentation/coredata/nssavechangesrequest/lockedobjects)
- [NSAtomicStore](/documentation/coredata/nsatomicstore)

#### Initializing a Store

- [init(persistentStoreCoordinator: NSPersistentStoreCoordinator?, configurationName: String?, at: URL, options: [AnyHashable : Any]?)](/documentation/coredata/nsatomicstore/init(persistentstorecoordinator:configurationname:at:options:))

#### Loading a Store

- [func load() throws](/documentation/coredata/nsatomicstore/load())
- [func objectID(for: NSEntityDescription, withReferenceObject: Any) -> NSManagedObjectID](/documentation/coredata/nsatomicstore/objectid(for:withreferenceobject:))
- [func addCacheNodes(Set<NSAtomicStoreCacheNode>)](/documentation/coredata/nsatomicstore/addcachenodes(_:))

#### Updating Cache Nodes

- [func newCacheNode(for: NSManagedObject) -> NSAtomicStoreCacheNode](/documentation/coredata/nsatomicstore/newcachenode(for:))
- [func newReferenceObject(for: NSManagedObject) -> Any](/documentation/coredata/nsatomicstore/newreferenceobject(for:))
- [func updateCacheNode(NSAtomicStoreCacheNode, from: NSManagedObject)](/documentation/coredata/nsatomicstore/updatecachenode(_:from:))
- [func willRemoveCacheNodes(Set<NSAtomicStoreCacheNode>)](/documentation/coredata/nsatomicstore/willremovecachenodes(_:))

#### Saving a Store

- [func save() throws](/documentation/coredata/nsatomicstore/save())

#### Utility Methods

- [func cacheNodes() -> Set<NSAtomicStoreCacheNode>](/documentation/coredata/nsatomicstore/cachenodes())
- [func cacheNode(for: NSManagedObjectID) -> NSAtomicStoreCacheNode?](/documentation/coredata/nsatomicstore/cachenode(for:))
- [func referenceObject(for: NSManagedObjectID) -> Any](/documentation/coredata/nsatomicstore/referenceobject(for:))
- [NSAtomicStoreCacheNode](/documentation/coredata/nsatomicstorecachenode)

#### Initializing a Cache Node

- [init(objectID: NSManagedObjectID)](/documentation/coredata/nsatomicstorecachenode/init(objectid:))

#### Managing Node Data

- [var objectID: NSManagedObjectID](/documentation/coredata/nsatomicstorecachenode/objectid)
- [var propertyCache: NSMutableDictionary?](/documentation/coredata/nsatomicstorecachenode/propertycache)
- [func value(forKey: String) -> Any?](/documentation/coredata/nsatomicstorecachenode/value(forkey:))
- [func setValue(Any?, forKey: String)](/documentation/coredata/nsatomicstorecachenode/setvalue(_:forkey:))
- [NSIncrementalStore](/documentation/coredata/nsincrementalstore)

#### Manipulating Managed Objects

- [func execute(NSPersistentStoreRequest, with: NSManagedObjectContext?) throws -> Any](/documentation/coredata/nsincrementalstore/execute(_:with:))
- [func newValuesForObject(with: NSManagedObjectID, with: NSManagedObjectContext) throws -> NSIncrementalStoreNode](/documentation/coredata/nsincrementalstore/newvaluesforobject(with:with:))
- [func newValue(forRelationship: NSRelationshipDescription, forObjectWith: NSManagedObjectID, with: NSManagedObjectContext?) throws -> Any](/documentation/coredata/nsincrementalstore/newvalue(forrelationship:forobjectwith:with:))
- [func obtainPermanentIDs(for: [NSManagedObject]) throws -> [NSManagedObjectID]](/documentation/coredata/nsincrementalstore/obtainpermanentids(for:))
- [func newObjectID(for: NSEntityDescription, referenceObject: Any) -> NSManagedObjectID](/documentation/coredata/nsincrementalstore/newobjectid(for:referenceobject:))
- [func referenceObject(for: NSManagedObjectID) -> Any](/documentation/coredata/nsincrementalstore/referenceobject(for:))

#### Responding to Context Changes

- [func managedObjectContextDidRegisterObjects(with: [NSManagedObjectID])](/documentation/coredata/nsincrementalstore/managedobjectcontextdidregisterobjects(with:))
- [func managedObjectContextDidUnregisterObjects(with: [NSManagedObjectID])](/documentation/coredata/nsincrementalstore/managedobjectcontextdidunregisterobjects(with:))

#### Accessing Metadata

- [class func identifierForNewStore(at: URL) -> Any](/documentation/coredata/nsincrementalstore/identifierfornewstore(at:))
- [func loadMetadata() throws](/documentation/coredata/nsincrementalstore/loadmetadata())
- [NSIncrementalStoreNode](/documentation/coredata/nsincrementalstorenode)

#### Initializing a Node

- [init(objectID: NSManagedObjectID, withValues: [String : Any], version: UInt64)](/documentation/coredata/nsincrementalstorenode/init(objectid:withvalues:version:))

#### Managing Node Data

- [var objectID: NSManagedObjectID](/documentation/coredata/nsincrementalstorenode/objectid)
- [func update(withValues: [String : Any], version: UInt64)](/documentation/coredata/nsincrementalstorenode/update(withvalues:version:))
- [func value(for: NSPropertyDescription) -> Any?](/documentation/coredata/nsincrementalstorenode/value(for:))
- [var version: UInt64](/documentation/coredata/nsincrementalstorenode/version)
- [Handling Different Data Types in Core Data](/documentation/coredata/handling-different-data-types-in-core-data)
- [Linking Data Between Two Core Data Stores](/documentation/coredata/linking-data-between-two-core-data-stores)

## Data modeling

- [Modeling data](/documentation/coredata/modeling-data)

### Configuring a Core Data Model

- [Configuring Entities](/documentation/coredata/configuring-entities)
- [Configuring Attributes](/documentation/coredata/configuring-attributes)
- [Configuring Relationships](/documentation/coredata/configuring-relationships)
- [Generating code](/documentation/coredata/generating-code)
- [Core Data model](/documentation/coredata/core-data-model)

### Objects and entities

- [NSManagedObject](/documentation/coredata/nsmanagedobject)

#### Creating a Managed Object

- [init(entity: NSEntityDescription, insertInto: NSManagedObjectContext?)](/documentation/coredata/nsmanagedobject/init(entity:insertinto:))
- [convenience init(context: NSManagedObjectContext)](/documentation/coredata/nsmanagedobject/init(context:))

#### Getting a Managed Object’s Identity

- [var entity: NSEntityDescription](/documentation/coredata/nsmanagedobject/entity-swift.property)
- [var objectID: NSManagedObjectID](/documentation/coredata/nsmanagedobject/objectid)
- [class func entity() -> NSEntityDescription](/documentation/coredata/nsmanagedobject/entity())

#### Getting State Information

- [var managedObjectContext: NSManagedObjectContext?](/documentation/coredata/nsmanagedobject/managedobjectcontext)
- [var hasChanges: Bool](/documentation/coredata/nsmanagedobject/haschanges)
- [var isInserted: Bool](/documentation/coredata/nsmanagedobject/isinserted)
- [var isUpdated: Bool](/documentation/coredata/nsmanagedobject/isupdated)
- [var isDeleted: Bool](/documentation/coredata/nsmanagedobject/isdeleted)
- [var isFault: Bool](/documentation/coredata/nsmanagedobject/isfault)
- [var faultingState: Int](/documentation/coredata/nsmanagedobject/faultingstate)
- [func hasFault(forRelationshipNamed: String) -> Bool](/documentation/coredata/nsmanagedobject/hasfault(forrelationshipnamed:))
- [var hasPersistentChangedValues: Bool](/documentation/coredata/nsmanagedobject/haspersistentchangedvalues)

#### Managing Change Events

- [class var contextShouldIgnoreUnmodeledPropertyChanges: Bool](/documentation/coredata/nsmanagedobject/contextshouldignoreunmodeledpropertychanges)
- [func awakeFromFetch()](/documentation/coredata/nsmanagedobject/awakefromfetch())
- [func awakeFromInsert()](/documentation/coredata/nsmanagedobject/awakefrominsert())
- [func awake(fromSnapshotEvents: NSSnapshotEventType)](/documentation/coredata/nsmanagedobject/awake(fromsnapshotevents:))
- [func changedValues() -> [String : Any]](/documentation/coredata/nsmanagedobject/changedvalues())
- [func changedValuesForCurrentEvent() -> [String : Any]](/documentation/coredata/nsmanagedobject/changedvaluesforcurrentevent())
- [func committedValues(forKeys: [String]?) -> [String : Any]](/documentation/coredata/nsmanagedobject/committedvalues(forkeys:))
- [func prepareForDeletion()](/documentation/coredata/nsmanagedobject/preparefordeletion())
- [func willSave()](/documentation/coredata/nsmanagedobject/willsave())
- [func didSave()](/documentation/coredata/nsmanagedobject/didsave())
- [func willTurnIntoFault()](/documentation/coredata/nsmanagedobject/willturnintofault())
- [func didTurnIntoFault()](/documentation/coredata/nsmanagedobject/didturnintofault())
- [class func fetchRequest() -> NSFetchRequest<any NSFetchRequestResult>](/documentation/coredata/nsmanagedobject/fetchrequest())

#### Supporting Key-Value Coding

- [func value(forKey: String) -> Any?](/documentation/coredata/nsmanagedobject/value(forkey:))
- [func setValue(Any?, forKey: String)](/documentation/coredata/nsmanagedobject/setvalue(_:forkey:))
- [func primitiveValue(forKey: String) -> Any?](/documentation/coredata/nsmanagedobject/primitivevalue(forkey:))
- [func setPrimitiveValue(Any?, forKey: String)](/documentation/coredata/nsmanagedobject/setprimitivevalue(_:forkey:))
- [func objectIDs(forRelationshipNamed: String) -> [NSManagedObjectID]](/documentation/coredata/nsmanagedobject/objectids(forrelationshipnamed:))

#### Managing Data Validation

- [func validateValue(AutoreleasingUnsafeMutablePointer<AnyObject?>, forKey: String) throws](/documentation/coredata/nsmanagedobject/validatevalue(_:forkey:))
- [func validateForDelete() throws](/documentation/coredata/nsmanagedobject/validatefordelete())
- [func validateForInsert() throws](/documentation/coredata/nsmanagedobject/validateforinsert())
- [func validateForUpdate() throws](/documentation/coredata/nsmanagedobject/validateforupdate())
- [Validation error codes](/documentation/coredata/1535452-validation-error-codes)

##### Error codes

- [var NSCoreDataError: Int](/documentation/coredata/nscoredataerror)
- [var NSEntityMigrationPolicyError: Int](/documentation/coredata/nsentitymigrationpolicyerror)
- [var NSExternalRecordImportError: Int](/documentation/coredata/nsexternalrecordimporterror)
- [var NSInferredMappingModelError: Int](/documentation/coredata/nsinferredmappingmodelerror)
- [var NSManagedObjectConstraintMergeError: Int](/documentation/coredata/nsmanagedobjectconstraintmergeerror)
- [var NSManagedObjectConstraintValidationError: Int](/documentation/coredata/nsmanagedobjectconstraintvalidationerror)
- [var NSManagedObjectContextLockingError: Int](/documentation/coredata/nsmanagedobjectcontextlockingerror)
- [var NSManagedObjectExternalRelationshipError: Int](/documentation/coredata/nsmanagedobjectexternalrelationshiperror)
- [var NSManagedObjectMergeError: Int](/documentation/coredata/nsmanagedobjectmergeerror)
- [var NSManagedObjectModelReferenceNotFoundError: Int](/documentation/coredata/nsmanagedobjectmodelreferencenotfounderror)
- [var NSManagedObjectReferentialIntegrityError: Int](/documentation/coredata/nsmanagedobjectreferentialintegrityerror)
- [var NSManagedObjectValidationError: Int](/documentation/coredata/nsmanagedobjectvalidationerror)
- [var NSMigrationCancelledError: Int](/documentation/coredata/nsmigrationcancellederror)
- [var NSMigrationConstraintViolationError: Int](/documentation/coredata/nsmigrationconstraintviolationerror)
- [var NSMigrationError: Int](/documentation/coredata/nsmigrationerror)
- [var NSMigrationManagerDestinationStoreError: Int](/documentation/coredata/nsmigrationmanagerdestinationstoreerror)
- [var NSMigrationManagerSourceStoreError: Int](/documentation/coredata/nsmigrationmanagersourcestoreerror)
- [var NSMigrationMissingMappingModelError: Int](/documentation/coredata/nsmigrationmissingmappingmodelerror)
- [var NSMigrationMissingSourceModelError: Int](/documentation/coredata/nsmigrationmissingsourcemodelerror)
- [var NSPersistentHistoryTokenExpiredError: Int](/documentation/coredata/nspersistenthistorytokenexpirederror)
- [var NSPersistentStoreCoordinatorLockingError: Int](/documentation/coredata/nspersistentstorecoordinatorlockingerror)
- [var NSPersistentStoreIncompatibleSchemaError: Int](/documentation/coredata/nspersistentstoreincompatibleschemaerror)
- [var NSPersistentStoreIncompatibleVersionHashError: Int](/documentation/coredata/nspersistentstoreincompatibleversionhasherror)
- [var NSPersistentStoreIncompleteSaveError: Int](/documentation/coredata/nspersistentstoreincompletesaveerror)
- [var NSPersistentStoreInvalidTypeError: Int](/documentation/coredata/nspersistentstoreinvalidtypeerror)
- [var NSPersistentStoreOpenError: Int](/documentation/coredata/nspersistentstoreopenerror)
- [var NSPersistentStoreOperationError: Int](/documentation/coredata/nspersistentstoreoperationerror)
- [var NSPersistentStoreSaveConflictsError: Int](/documentation/coredata/nspersistentstoresaveconflictserror)
- [var NSPersistentStoreSaveError: Int](/documentation/coredata/nspersistentstoresaveerror)
- [var NSPersistentStoreTimeoutError: Int](/documentation/coredata/nspersistentstoretimeouterror)
- [var NSPersistentStoreTypeMismatchError: Int](/documentation/coredata/nspersistentstoretypemismatcherror)
- [var NSPersistentStoreUnsupportedRequestTypeError: Int](/documentation/coredata/nspersistentstoreunsupportedrequesttypeerror)
- [var NSSQLiteError: Int](/documentation/coredata/nssqliteerror)
- [var NSStagedMigrationBackwardMigrationError: Int](/documentation/coredata/nsstagedmigrationbackwardmigrationerror)
- [var NSStagedMigrationFrameworkVersionMismatchError: Int](/documentation/coredata/nsstagedmigrationframeworkversionmismatcherror)
- [var NSValidationInvalidURIError: Int](/documentation/coredata/nsvalidationinvalidurierror)
- [var NSValidationMultipleErrorsError: Int](/documentation/coredata/nsvalidationmultipleerrorserror)
- [var NSValidationMissingMandatoryPropertyError: Int](/documentation/coredata/nsvalidationmissingmandatorypropertyerror)
- [var NSValidationRelationshipLacksMinimumCountError: Int](/documentation/coredata/nsvalidationrelationshiplacksminimumcounterror)
- [var NSValidationRelationshipExceedsMaximumCountError: Int](/documentation/coredata/nsvalidationrelationshipexceedsmaximumcounterror)
- [var NSValidationRelationshipDeniedDeleteError: Int](/documentation/coredata/nsvalidationrelationshipdenieddeleteerror)
- [var NSValidationNumberTooLargeError: Int](/documentation/coredata/nsvalidationnumbertoolargeerror)
- [var NSValidationNumberTooSmallError: Int](/documentation/coredata/nsvalidationnumbertoosmallerror)
- [var NSValidationDateTooLateError: Int](/documentation/coredata/nsvalidationdatetoolateerror)
- [var NSValidationDateTooSoonError: Int](/documentation/coredata/nsvalidationdatetoosoonerror)
- [var NSValidationInvalidDateError: Int](/documentation/coredata/nsvalidationinvaliddateerror)
- [var NSValidationStringTooLongError: Int](/documentation/coredata/nsvalidationstringtoolongerror)
- [var NSValidationStringTooShortError: Int](/documentation/coredata/nsvalidationstringtooshorterror)
- [var NSValidationStringPatternMatchingError: Int](/documentation/coredata/nsvalidationstringpatternmatchingerror)
- [let NSValidationKeyErrorKey: String](/documentation/coredata/nsvalidationkeyerrorkey)
- [let NSValidationObjectErrorKey: String](/documentation/coredata/nsvalidationobjecterrorkey)
- [let NSValidationPredicateErrorKey: String](/documentation/coredata/nsvalidationpredicateerrorkey)
- [let NSValidationValueErrorKey: String](/documentation/coredata/nsvalidationvalueerrorkey)

#### Supporting Key-Value Observing

- [func didAccessValue(forKey: String?)](/documentation/coredata/nsmanagedobject/didaccessvalue(forkey:))
- [func observationInfo() -> UnsafeMutableRawPointer?](/documentation/coredata/nsmanagedobject/observationinfo())
- [func setObservationInfo(UnsafeMutableRawPointer?)](/documentation/coredata/nsmanagedobject/setobservationinfo(_:))
- [func willAccessValue(forKey: String?)](/documentation/coredata/nsmanagedobject/willaccessvalue(forkey:))
- [func didChangeValue(forKey: String)](/documentation/coredata/nsmanagedobject/didchangevalue(forkey:))
- [func didChangeValue(forKey: String, withSetMutation: NSKeyValueSetMutationKind, using: Set<AnyHashable>)](/documentation/coredata/nsmanagedobject/didchangevalue(forkey:withsetmutation:using:))
- [func willChangeValue(forKey: String)](/documentation/coredata/nsmanagedobject/willchangevalue(forkey:))
- [func willChangeValue(forKey: String, withSetMutation: NSKeyValueSetMutationKind, using: Set<AnyHashable>)](/documentation/coredata/nsmanagedobject/willchangevalue(forkey:withsetmutation:using:))

#### Reinitializing Values

- [NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype)

##### Event Types

- [static var undoInsertion: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/undoinsertion)
- [static var undoDeletion: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/undodeletion)
- [static var undoUpdate: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/undoupdate)
- [static var rollback: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/rollback)
- [static var refresh: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/refresh)
- [static var mergePolicy: NSSnapshotEventType](/documentation/coredata/nssnapshoteventtype/mergepolicy)

##### Initializers

- [init(rawValue: UInt)](/documentation/coredata/nssnapshoteventtype/init(rawvalue:))

#### Subscripts

- [subscript(String) -> Any?](/documentation/coredata/nsmanagedobject/subscript(_:))
- [NSEntityDescription](/documentation/coredata/nsentitydescription)

#### Getting descriptive information

- [var name: String?](/documentation/coredata/nsentitydescription/name)
- [var managedObjectModel: NSManagedObjectModel](/documentation/coredata/nsentitydescription/managedobjectmodel)
- [var managedObjectClassName: String!](/documentation/coredata/nsentitydescription/managedobjectclassname)
- [var renamingIdentifier: String?](/documentation/coredata/nsentitydescription/renamingidentifier)
- [var isAbstract: Bool](/documentation/coredata/nsentitydescription/isabstract)
- [var userInfo: [AnyHashable : Any]?](/documentation/coredata/nsentitydescription/userinfo)
- [var coreSpotlightDisplayNameExpression: NSExpression](/documentation/coredata/nsentitydescription/corespotlightdisplaynameexpression)

#### Managing inheritance

- [var subentitiesByName: [String : NSEntityDescription]](/documentation/coredata/nsentitydescription/subentitiesbyname)
- [var subentities: [NSEntityDescription]](/documentation/coredata/nsentitydescription/subentities)
- [var superentity: NSEntityDescription?](/documentation/coredata/nsentitydescription/superentity)
- [func isKindOf(entity: NSEntityDescription) -> Bool](/documentation/coredata/nsentitydescription/iskindof(entity:))

#### Working with properties

- [var propertiesByName: [String : NSPropertyDescription]](/documentation/coredata/nsentitydescription/propertiesbyname)
- [var properties: [NSPropertyDescription]](/documentation/coredata/nsentitydescription/properties)
- [var attributesByName: [String : NSAttributeDescription]](/documentation/coredata/nsentitydescription/attributesbyname)
- [var relationshipsByName: [String : NSRelationshipDescription]](/documentation/coredata/nsentitydescription/relationshipsbyname)
- [func relationships(forDestination: NSEntityDescription) -> [NSRelationshipDescription]](/documentation/coredata/nsentitydescription/relationships(fordestination:))

#### Configuring indexes and constraints

- [var indexes: [NSFetchIndexDescription]](/documentation/coredata/nsentitydescription/indexes)
- [var uniquenessConstraints: [[Any]]](/documentation/coredata/nsentitydescription/uniquenessconstraints)
- [var compoundIndexes: [[Any]]](/documentation/coredata/nsentitydescription/compoundindexes)

#### Creating a managed object

- [class func insertNewObject(forEntityName: String, into: NSManagedObjectContext) -> NSManagedObject](/documentation/coredata/nsentitydescription/insertnewobject(forentityname:into:))

#### Retrieving a description by its name

- [class func entity(forEntityName: String, in: NSManagedObjectContext) -> NSEntityDescription?](/documentation/coredata/nsentitydescription/entity(forentityname:in:))

#### Managing versioning

- [var versionHash: Data](/documentation/coredata/nsentitydescription/versionhash)
- [var versionHashModifier: String?](/documentation/coredata/nsentitydescription/versionhashmodifier)

### Standard attributes

- [NSPropertyDescription](/documentation/coredata/nspropertydescription)

#### Accessing Features of a Property

- [var entity: NSEntityDescription](/documentation/coredata/nspropertydescription/entity)
- [var isIndexed: Bool](/documentation/coredata/nspropertydescription/isindexed)
- [var isOptional: Bool](/documentation/coredata/nspropertydescription/isoptional)
- [var isTransient: Bool](/documentation/coredata/nspropertydescription/istransient)
- [var name: String](/documentation/coredata/nspropertydescription/name)
- [var userInfo: [AnyHashable : Any]?](/documentation/coredata/nspropertydescription/userinfo)

#### Supporting Validation

- [var validationPredicates: [NSPredicate]](/documentation/coredata/nspropertydescription/validationpredicates)
- [var validationWarnings: [Any]](/documentation/coredata/nspropertydescription/validationwarnings)
- [func setValidationPredicates([NSPredicate]?, withValidationWarnings: [String]?)](/documentation/coredata/nspropertydescription/setvalidationpredicates(_:withvalidationwarnings:))

#### Supporting Versioning

- [var versionHash: Data](/documentation/coredata/nspropertydescription/versionhash)
- [var versionHashModifier: String?](/documentation/coredata/nspropertydescription/versionhashmodifier)
- [var renamingIdentifier: String?](/documentation/coredata/nspropertydescription/renamingidentifier)

#### Specifying Spotlight Support

- [var isIndexedBySpotlight: Bool](/documentation/coredata/nspropertydescription/isindexedbyspotlight)
- [var isStoredInExternalRecord: Bool](/documentation/coredata/nspropertydescription/isstoredinexternalrecord)
- [NSAttributeDescription](/documentation/coredata/nsattributedescription)

#### Managing the type

- [var attributeValueClassName: String?](/documentation/coredata/nsattributedescription/attributevalueclassname)
- [var type: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/type)
- [NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct)

##### Attribute Types

- [static let binaryData: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/binarydata)
- [static let boolean: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/boolean)
- [static let composite: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/composite)
- [static let date: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/date)
- [static let decimal: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/decimal)
- [static let double: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/double)
- [static let float: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/float)
- [static let integer16: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/integer16)
- [static let integer32: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/integer32)
- [static let integer64: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/integer64)
- [static let objectID: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/objectid)
- [static let string: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/string)
- [static let transformable: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/transformable)
- [static let undefined: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/undefined)
- [static let uri: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/uri)
- [static let uuid: NSAttributeDescription.AttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.struct/uuid)
- [var attributeType: NSAttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.property)
- [NSAttributeType](/documentation/coredata/nsattributetype)

##### Attribute types

- [case binaryDataAttributeType](/documentation/coredata/nsattributetype/binarydataattributetype)
- [case booleanAttributeType](/documentation/coredata/nsattributetype/booleanattributetype)
- [case compositeAttributeType](/documentation/coredata/nsattributetype/compositeattributetype)
- [case dateAttributeType](/documentation/coredata/nsattributetype/dateattributetype)
- [case decimalAttributeType](/documentation/coredata/nsattributetype/decimalattributetype)
- [case doubleAttributeType](/documentation/coredata/nsattributetype/doubleattributetype)
- [case floatAttributeType](/documentation/coredata/nsattributetype/floatattributetype)
- [case integer16AttributeType](/documentation/coredata/nsattributetype/integer16attributetype)
- [case integer32AttributeType](/documentation/coredata/nsattributetype/integer32attributetype)
- [case integer64AttributeType](/documentation/coredata/nsattributetype/integer64attributetype)
- [case objectIDAttributeType](/documentation/coredata/nsattributetype/objectidattributetype)
- [case stringAttributeType](/documentation/coredata/nsattributetype/stringattributetype)
- [case transformableAttributeType](/documentation/coredata/nsattributetype/transformableattributetype)
- [case undefinedAttributeType](/documentation/coredata/nsattributetype/undefinedattributetype)
- [case URIAttributeType](/documentation/coredata/nsattributetype/uriattributetype)
- [case UUIDAttributeType](/documentation/coredata/nsattributetype/uuidattributetype)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsattributetype/init(rawvalue:))

#### Configuring the behavior

- [var allowsCloudEncryption: Bool](/documentation/coredata/nsattributedescription/allowscloudencryption)
- [var allowsExternalBinaryDataStorage: Bool](/documentation/coredata/nsattributedescription/allowsexternalbinarydatastorage)
- [var defaultValue: Any?](/documentation/coredata/nsattributedescription/defaultvalue)
- [var preservesValueInHistoryOnDeletion: Bool](/documentation/coredata/nsattributedescription/preservesvalueinhistoryondeletion)
- [var valueTransformerName: String?](/documentation/coredata/nsattributedescription/valuetransformername)

#### Getting version information

- [var versionHash: Data](/documentation/coredata/nsattributedescription/versionhash)

#### Deprecated

- [Deprecated symbols](/documentation/coredata/nsattributedescription-deprecated-symbols)

##### Deprecated properties

- [var attributeType: NSAttributeType](/documentation/coredata/nsattributedescription/attributetype-swift.property)
- [NSAttributeType](/documentation/coredata/nsattributetype)

#### Attribute types

- [case binaryDataAttributeType](/documentation/coredata/nsattributetype/binarydataattributetype)
- [case booleanAttributeType](/documentation/coredata/nsattributetype/booleanattributetype)
- [case compositeAttributeType](/documentation/coredata/nsattributetype/compositeattributetype)
- [case dateAttributeType](/documentation/coredata/nsattributetype/dateattributetype)
- [case decimalAttributeType](/documentation/coredata/nsattributetype/decimalattributetype)
- [case doubleAttributeType](/documentation/coredata/nsattributetype/doubleattributetype)
- [case floatAttributeType](/documentation/coredata/nsattributetype/floatattributetype)
- [case integer16AttributeType](/documentation/coredata/nsattributetype/integer16attributetype)
- [case integer32AttributeType](/documentation/coredata/nsattributetype/integer32attributetype)
- [case integer64AttributeType](/documentation/coredata/nsattributetype/integer64attributetype)
- [case objectIDAttributeType](/documentation/coredata/nsattributetype/objectidattributetype)
- [case stringAttributeType](/documentation/coredata/nsattributetype/stringattributetype)
- [case transformableAttributeType](/documentation/coredata/nsattributetype/transformableattributetype)
- [case undefinedAttributeType](/documentation/coredata/nsattributetype/undefinedattributetype)
- [case URIAttributeType](/documentation/coredata/nsattributetype/uriattributetype)
- [case UUIDAttributeType](/documentation/coredata/nsattributetype/uuidattributetype)

#### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsattributetype/init(rawvalue:))
- [NSRelationshipDescription](/documentation/coredata/nsrelationshipdescription)

#### Configuring the Destination

- [var inverseRelationship: NSRelationshipDescription?](/documentation/coredata/nsrelationshipdescription/inverserelationship)
- [var destinationEntity: NSEntityDescription?](/documentation/coredata/nsrelationshipdescription/destinationentity)
- [var isOrdered: Bool](/documentation/coredata/nsrelationshipdescription/isordered)

#### Configuring Cardinality

- [var isToMany: Bool](/documentation/coredata/nsrelationshipdescription/istomany)
- [var minCount: Int](/documentation/coredata/nsrelationshipdescription/mincount)
- [var maxCount: Int](/documentation/coredata/nsrelationshipdescription/maxcount)

#### Configuring Delete Behavior

- [var deleteRule: NSDeleteRule](/documentation/coredata/nsrelationshipdescription/deleterule)
- [NSDeleteRule](/documentation/coredata/nsdeleterule)

##### Delete Rules

- [case noActionDeleteRule](/documentation/coredata/nsdeleterule/noactiondeleterule)
- [case nullifyDeleteRule](/documentation/coredata/nsdeleterule/nullifydeleterule)
- [case cascadeDeleteRule](/documentation/coredata/nsdeleterule/cascadedeleterule)
- [case denyDeleteRule](/documentation/coredata/nsdeleterule/denydeleterule)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsdeleterule/init(rawvalue:))

#### Getting Version Data

- [var versionHash: Data](/documentation/coredata/nsrelationshipdescription/versionhash)

### Computed attributes

- [NSCompositeAttributeDescription](/documentation/coredata/nscompositeattributedescription)

#### Composing attributes

- [var elements: [NSAttributeDescription]](/documentation/coredata/nscompositeattributedescription/elements)
- [NSDerivedAttributeDescription](/documentation/coredata/nsderivedattributedescription)

#### Specifying the Derivation Expression

- [var derivationExpression: NSExpression?](/documentation/coredata/nsderivedattributedescription/derivationexpression)

### Fetched properties

- [NSFetchedPropertyDescription](/documentation/coredata/nsfetchedpropertydescription)

#### Getting and setting the fetch request

- [var fetchRequest: NSFetchRequest<any NSFetchRequestResult>?](/documentation/coredata/nsfetchedpropertydescription/fetchrequest)

## Fetch requests

- [NSFetchRequest](/documentation/coredata/nsfetchrequest)

### Managing the Fetch Request’s Entity

- [init()](/documentation/coredata/nsfetchrequest/init())
- [convenience init(entityName: String)](/documentation/coredata/nsfetchrequest/init(entityname:))
- [var entityName: String?](/documentation/coredata/nsfetchrequest/entityname)
- [var entity: NSEntityDescription?](/documentation/coredata/nsfetchrequest/entity)
- [var includesSubentities: Bool](/documentation/coredata/nsfetchrequest/includessubentities)
- [NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype)

#### Result Types

- [static var managedObjectResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/managedobjectresulttype)
- [static var managedObjectIDResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/managedobjectidresulttype)
- [static var dictionaryResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/dictionaryresulttype)
- [static var countResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/countresulttype)

#### Initializers

- [init(rawValue: UInt)](/documentation/coredata/nsfetchrequestresulttype/init(rawvalue:))

### Specifying Fetch Constraints

- [var predicate: NSPredicate?](/documentation/coredata/nsfetchrequest/predicate)
- [var fetchLimit: Int](/documentation/coredata/nsfetchrequest/fetchlimit)
- [var fetchOffset: Int](/documentation/coredata/nsfetchrequest/fetchoffset)
- [var fetchBatchSize: Int](/documentation/coredata/nsfetchrequest/fetchbatchsize)
- [var affectedStores: [NSPersistentStore]?](/documentation/coredata/nsfetchrequest/affectedstores)
- [NSFetchRequestExpression](/documentation/coredata/nsfetchrequestexpression)

#### Creating a Fetch Request Expression

- [class func expression(forFetch: NSExpression, context: NSExpression, countOnly: Bool) -> NSExpression](/documentation/coredata/nsfetchrequestexpression/expression(forfetch:context:countonly:))

#### Examining a Fetch Request Expression

- [var requestExpression: NSExpression](/documentation/coredata/nsfetchrequestexpression/requestexpression)
- [var contextExpression: NSExpression](/documentation/coredata/nsfetchrequestexpression/contextexpression)
- [var isCountOnlyRequest: Bool](/documentation/coredata/nsfetchrequestexpression/iscountonlyrequest)

#### Constants

- [let NSFetchRequestExpressionType: NSExpression.ExpressionType](/documentation/coredata/nsfetchrequestexpressiontype)
- [NSExpressionDescription](/documentation/coredata/nsexpressiondescription)

#### Configuring the Expression Description

- [var expression: NSExpression?](/documentation/coredata/nsexpressiondescription/expression)
- [var resultType: NSAttributeDescription.AttributeType](/documentation/coredata/nsexpressiondescription/resulttype)
- [var expressionResultType: NSAttributeType](/documentation/coredata/nsexpressiondescription/expressionresulttype)

#### Deprecated

- [Deprecated Symbols](/documentation/coredata/nsexpressiondescription-deprecated-symbols)

##### Deprecated Properties

- [var expressionResultType: NSAttributeType](/documentation/coredata/nsexpressiondescription/expressionresulttype)
- [NSFetchedPropertyDescription](/documentation/coredata/nsfetchedpropertydescription)

#### Getting and setting the fetch request

- [var fetchRequest: NSFetchRequest<any NSFetchRequestResult>?](/documentation/coredata/nsfetchedpropertydescription/fetchrequest)

### Sorting the Results

- [var sortDescriptors: [NSSortDescriptor]?](/documentation/coredata/nsfetchrequest/sortdescriptors)

### Prefetching Related Objects

- [var relationshipKeyPathsForPrefetching: [String]?](/documentation/coredata/nsfetchrequest/relationshipkeypathsforprefetching)

### Managing How Results Are Returned

- [var resultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequest/resulttype)
- [var includesPendingChanges: Bool](/documentation/coredata/nsfetchrequest/includespendingchanges)
- [var propertiesToFetch: [Any]?](/documentation/coredata/nsfetchrequest/propertiestofetch)
- [var returnsDistinctResults: Bool](/documentation/coredata/nsfetchrequest/returnsdistinctresults)
- [var includesPropertyValues: Bool](/documentation/coredata/nsfetchrequest/includespropertyvalues)
- [var shouldRefreshRefetchedObjects: Bool](/documentation/coredata/nsfetchrequest/shouldrefreshrefetchedobjects)
- [var returnsObjectsAsFaults: Bool](/documentation/coredata/nsfetchrequest/returnsobjectsasfaults)
- [NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype)

#### Result Types

- [static var managedObjectResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/managedobjectresulttype)
- [static var managedObjectIDResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/managedobjectidresulttype)
- [static var dictionaryResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/dictionaryresulttype)
- [static var countResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/countresulttype)

#### Initializers

- [init(rawValue: UInt)](/documentation/coredata/nsfetchrequestresulttype/init(rawvalue:))
- [NSFetchRequestResult](/documentation/coredata/nsfetchrequestresult)

### Grouping and Filtering Dictionary Results

- [var propertiesToGroupBy: [Any]?](/documentation/coredata/nsfetchrequest/propertiestogroupby)
- [var havingPredicate: NSPredicate?](/documentation/coredata/nsfetchrequest/havingpredicate)

### Executing a Fetch Request Directly

- [func execute() throws -> [ResultType]](/documentation/coredata/nsfetchrequest/execute())
- [NSAsynchronousFetchRequest](/documentation/coredata/nsasynchronousfetchrequest)

### Initializing a Request

- [init(fetchRequest: NSFetchRequest<ResultType>, completionBlock: ((NSAsynchronousFetchResult<ResultType>) -> Void)?)](/documentation/coredata/nsasynchronousfetchrequest/init(fetchrequest:completionblock:))

### Preparing a Request

- [var completionBlock: NSPersistentStoreAsynchronousFetchResultCompletionBlock?](/documentation/coredata/nsasynchronousfetchrequest/completionblock)
- [var estimatedResultCount: Int](/documentation/coredata/nsasynchronousfetchrequest/estimatedresultcount)
- [var fetchRequest: NSFetchRequest<ResultType>](/documentation/coredata/nsasynchronousfetchrequest/fetchrequest)
- [NSAsynchronousFetchResult](/documentation/coredata/nsasynchronousfetchresult)

### Getting Information About a Result

- [var fetchRequest: NSAsynchronousFetchRequest<ResultType>](/documentation/coredata/nsasynchronousfetchresult/fetchrequest)
- [var finalResult: [ResultType]?](/documentation/coredata/nsasynchronousfetchresult/finalresult)
- [NSFetchedResultsController](/documentation/coredata/nsfetchedresultscontroller)

### Initializing a Fetched Results Controller

- [init(fetchRequest: NSFetchRequest<ResultType>, managedObjectContext: NSManagedObjectContext, sectionNameKeyPath: String?, cacheName: String?)](/documentation/coredata/nsfetchedresultscontroller/init(fetchrequest:managedobjectcontext:sectionnamekeypath:cachename:))
- [func performFetch() throws](/documentation/coredata/nsfetchedresultscontroller/performfetch())

### Getting Configuration Information

- [var fetchRequest: NSFetchRequest<ResultType>](/documentation/coredata/nsfetchedresultscontroller/fetchrequest)
- [var managedObjectContext: NSManagedObjectContext](/documentation/coredata/nsfetchedresultscontroller/managedobjectcontext)
- [var sectionNameKeyPath: String?](/documentation/coredata/nsfetchedresultscontroller/sectionnamekeypath)
- [var cacheName: String?](/documentation/coredata/nsfetchedresultscontroller/cachename)
- [var delegate: (any NSFetchedResultsControllerDelegate)?](/documentation/coredata/nsfetchedresultscontroller/delegate)
- [class func deleteCache(withName: String?)](/documentation/coredata/nsfetchedresultscontroller/deletecache(withname:))

### Accessing Results

- [var fetchedObjects: [ResultType]?](/documentation/coredata/nsfetchedresultscontroller/fetchedobjects)
- [func object(at: IndexPath) -> ResultType](/documentation/coredata/nsfetchedresultscontroller/object(at:))
- [func indexPath(forObject: ResultType) -> IndexPath?](/documentation/coredata/nsfetchedresultscontroller/indexpath(forobject:))

### Querying Section Information

- [var sections: [any NSFetchedResultsSectionInfo]?](/documentation/coredata/nsfetchedresultscontroller/sections)
- [func section(forSectionIndexTitle: String, at: Int) -> Int](/documentation/coredata/nsfetchedresultscontroller/section(forsectionindextitle:at:))

### Configuring Section Information

- [func sectionIndexTitle(forSectionName: String) -> String?](/documentation/coredata/nsfetchedresultscontroller/sectionindextitle(forsectionname:))
- [var sectionIndexTitles: [String]](/documentation/coredata/nsfetchedresultscontroller/sectionindextitles)

### Responding to Changes

- [NSFetchedResultsControllerDelegate](/documentation/coredata/nsfetchedresultscontrollerdelegate)

#### Responding to Changes

- [func controller(NSFetchedResultsController<any NSFetchRequestResult>, didChangeContentWith: NSDiffableDataSourceSnapshot)](/documentation/coredata/nsfetchedresultscontrollerdelegate/controller(_:didchangecontentwith:)-4kezq)
- [func controller(NSFetchedResultsController<any NSFetchRequestResult>, didChangeContentWith: CollectionDifference<NSManagedObjectID>)](/documentation/coredata/nsfetchedresultscontrollerdelegate/controller(_:didchangecontentwith:)-5ullb)
- [func controllerWillChangeContent(NSFetchedResultsController<any NSFetchRequestResult>)](/documentation/coredata/nsfetchedresultscontrollerdelegate/controllerwillchangecontent(_:))
- [func controller(NSFetchedResultsController<any NSFetchRequestResult>, didChange: Any, at: IndexPath?, for: NSFetchedResultsChangeType, newIndexPath: IndexPath?)](/documentation/coredata/nsfetchedresultscontrollerdelegate/controller(_:didchange:at:for:newindexpath:))
- [func controller(NSFetchedResultsController<any NSFetchRequestResult>, didChange: any NSFetchedResultsSectionInfo, atSectionIndex: Int, for: NSFetchedResultsChangeType)](/documentation/coredata/nsfetchedresultscontrollerdelegate/controller(_:didchange:atsectionindex:for:))
- [func controllerDidChangeContent(NSFetchedResultsController<any NSFetchRequestResult>)](/documentation/coredata/nsfetchedresultscontrollerdelegate/controllerdidchangecontent(_:))

#### Customizing Section Names

- [func controller(NSFetchedResultsController<any NSFetchRequestResult>, sectionIndexTitleForSectionName: String) -> String?](/documentation/coredata/nsfetchedresultscontrollerdelegate/controller(_:sectionindextitleforsectionname:))

#### Constants

- [NSFetchedResultsChangeType](/documentation/coredata/nsfetchedresultschangetype)

##### Constants

- [case insert](/documentation/coredata/nsfetchedresultschangetype/insert)
- [case delete](/documentation/coredata/nsfetchedresultschangetype/delete)
- [case move](/documentation/coredata/nsfetchedresultschangetype/move)
- [case update](/documentation/coredata/nsfetchedresultschangetype/update)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsfetchedresultschangetype/init(rawvalue:))
- [NSFetchedResultsSectionInfo](/documentation/coredata/nsfetchedresultssectioninfo)

#### Accessing Objects

- [var numberOfObjects: Int](/documentation/coredata/nsfetchedresultssectioninfo/numberofobjects)
- [var objects: [Any]?](/documentation/coredata/nsfetchedresultssectioninfo/objects)

#### Accessing the Name and Title

- [var name: String](/documentation/coredata/nsfetchedresultssectioninfo/name)
- [var indexTitle: String?](/documentation/coredata/nsfetchedresultssectioninfo/indextitle)
- [NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype)

#### Result Types

- [static var managedObjectResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/managedobjectresulttype)
- [static var managedObjectIDResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/managedobjectidresulttype)
- [static var dictionaryResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/dictionaryresulttype)
- [static var countResultType: NSFetchRequestResultType](/documentation/coredata/nsfetchrequestresulttype/countresulttype)

#### Initializers

- [init(rawValue: UInt)](/documentation/coredata/nsfetchrequestresulttype/init(rawvalue:))
- [NSFetchedResultsChangeType](/documentation/coredata/nsfetchedresultschangetype)

#### Constants

- [case insert](/documentation/coredata/nsfetchedresultschangetype/insert)
- [case delete](/documentation/coredata/nsfetchedresultschangetype/delete)
- [case move](/documentation/coredata/nsfetchedresultschangetype/move)
- [case update](/documentation/coredata/nsfetchedresultschangetype/update)

#### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsfetchedresultschangetype/init(rawvalue:))

## SwiftData migration and coexistence

- [Adopting SwiftData for a Core Data app](/documentation/coredata/adopting-swiftdata-for-a-core-data-app)

## CloudKit mirroring

- [Mirroring a Core Data store with CloudKit](/documentation/coredata/mirroring-a-core-data-store-with-cloudkit)

### Configuring CloudKit Mirroring

- [Setting Up Core Data with CloudKit](/documentation/coredata/setting-up-core-data-with-cloudkit)
- [Creating a Core Data Model for CloudKit](/documentation/coredata/creating-a-core-data-model-for-cloudkit)
- [Syncing a Core Data Store with CloudKit](/documentation/coredata/syncing-a-core-data-store-with-cloudkit)
- [Reading CloudKit Records for Core Data](/documentation/coredata/reading-cloudkit-records-for-core-data)
- [Synchronizing a local store to the cloud](/documentation/coredata/synchronizing-a-local-store-to-the-cloud)
- [NSPersistentCloudKitContainer](/documentation/coredata/nspersistentcloudkitcontainer)

### Checking Permissions

- [func canUpdateRecord(forManagedObjectWith: NSManagedObjectID) -> Bool](/documentation/coredata/nspersistentcloudkitcontainer/canupdaterecord(formanagedobjectwith:))
- [func canDeleteRecord(forManagedObjectWith: NSManagedObjectID) -> Bool](/documentation/coredata/nspersistentcloudkitcontainer/candeleterecord(formanagedobjectwith:))
- [func canModifyManagedObjects(in: NSPersistentStore) -> Bool](/documentation/coredata/nspersistentcloudkitcontainer/canmodifymanagedobjects(in:))

### Sharing Objects

- [Accepting Share Invitations in a SwiftUI App](/documentation/coredata/accepting-share-invitations-in-a-swiftui-app)

### Promoting Your Schema

- [func initializeCloudKitSchema(options: NSPersistentCloudKitContainerSchemaInitializationOptions) throws](/documentation/coredata/nspersistentcloudkitcontainer/initializecloudkitschema(options:))
- [NSPersistentCloudKitContainerSchemaInitializationOptions](/documentation/coredata/nspersistentcloudkitcontainerschemainitializationoptions)

#### Constants

- [static var dryRun: NSPersistentCloudKitContainerSchemaInitializationOptions](/documentation/coredata/nspersistentcloudkitcontainerschemainitializationoptions/dryrun)
- [static var printSchema: NSPersistentCloudKitContainerSchemaInitializationOptions](/documentation/coredata/nspersistentcloudkitcontainerschemainitializationoptions/printschema)

#### Initializers

- [init(rawValue: UInt)](/documentation/coredata/nspersistentcloudkitcontainerschemainitializationoptions/init(rawvalue:))

### Monitoring Container Events

- [NSPersistentCloudKitContainer.Event](/documentation/coredata/nspersistentcloudkitcontainer/event)

#### Inspecting Event Properties

- [var type: NSPersistentCloudKitContainer.EventType](/documentation/coredata/nspersistentcloudkitcontainer/event/type)
- [var identifier: UUID](/documentation/coredata/nspersistentcloudkitcontainer/event/identifier)
- [var storeIdentifier: String](/documentation/coredata/nspersistentcloudkitcontainer/event/storeidentifier)
- [var succeeded: Bool](/documentation/coredata/nspersistentcloudkitcontainer/event/succeeded)
- [var startDate: Date](/documentation/coredata/nspersistentcloudkitcontainer/event/startdate)
- [var endDate: Date?](/documentation/coredata/nspersistentcloudkitcontainer/event/enddate)
- [var error: (any Error)?](/documentation/coredata/nspersistentcloudkitcontainer/event/error)
- [NSPersistentCloudKitContainer.EventType](/documentation/coredata/nspersistentcloudkitcontainer/eventtype)

#### Event Types

- [case setup](/documentation/coredata/nspersistentcloudkitcontainer/eventtype/setup)
- [case `import`](/documentation/coredata/nspersistentcloudkitcontainer/eventtype/import)
- [case export](/documentation/coredata/nspersistentcloudkitcontainer/eventtype/export)

#### Initializers

- [init?(rawValue: Int)](/documentation/coredata/nspersistentcloudkitcontainer/eventtype/init(rawvalue:))
- [NSPersistentCloudKitContainerEventRequest](/documentation/coredata/nspersistentcloudkitcontainereventrequest)

#### Fetching Events

- [class func fetchEvents(after: Date) -> Self](/documentation/coredata/nspersistentcloudkitcontainereventrequest/fetchevents(after:)-5izg7)
- [class func fetchEvents(after: NSPersistentCloudKitContainer.Event?) -> Self](/documentation/coredata/nspersistentcloudkitcontainereventrequest/fetchevents(after:)-3yfp)
- [class func fetchEvents(matchingFetch: NSFetchRequest<any NSFetchRequestResult>) -> Self](/documentation/coredata/nspersistentcloudkitcontainereventrequest/fetchevents(matchingfetch:))
- [class func fetchForEvents() -> NSFetchRequest<any NSFetchRequestResult>](/documentation/coredata/nspersistentcloudkitcontainereventrequest/fetchforevents())
- [var resultType: NSPersistentCloudKitContainerEventResult.ResultType](/documentation/coredata/nspersistentcloudkitcontainereventrequest/resulttype)
- [NSPersistentCloudKitContainerEventResult](/documentation/coredata/nspersistentcloudkitcontainereventresult)

#### Handling Event Results

- [var result: Any?](/documentation/coredata/nspersistentcloudkitcontainereventresult/result)
- [var resultType: NSPersistentCloudKitContainerEventResult.ResultType](/documentation/coredata/nspersistentcloudkitcontainereventresult/resulttype-swift.property)
- [NSPersistentCloudKitContainerEventResult.ResultType](/documentation/coredata/nspersistentcloudkitcontainereventresult/resulttype-swift.enum)

##### Result Types

- [case events](/documentation/coredata/nspersistentcloudkitcontainereventresult/resulttype-swift.enum/events)
- [case countEvents](/documentation/coredata/nspersistentcloudkitcontainereventresult/resulttype-swift.enum/countevents)

##### Initializers

- [init?(rawValue: Int)](/documentation/coredata/nspersistentcloudkitcontainereventresult/resulttype-swift.enum/init(rawvalue:))
- [class let eventChangedNotification: NSNotification.Name](/documentation/coredata/nspersistentcloudkitcontainer/eventchangednotification)
- [class let eventNotificationUserInfoKey: String](/documentation/coredata/nspersistentcloudkitcontainer/eventnotificationuserinfokey)
- [NSPersistentCloudKitContainerOptions](/documentation/coredata/nspersistentcloudkitcontaineroptions)

### Creating Container Options

- [init(containerIdentifier: String)](/documentation/coredata/nspersistentcloudkitcontaineroptions/init(containeridentifier:))
- [var containerIdentifier: String](/documentation/coredata/nspersistentcloudkitcontaineroptions/containeridentifier)
- [var databaseScope: CKDatabase.Scope](/documentation/coredata/nspersistentcloudkitcontaineroptions/databasescope-4c72t)
- [Sharing Core Data objects between iCloud users](/documentation/coredata/sharing-core-data-objects-between-icloud-users)

## Change processing

- [Accessing data when the store changes](/documentation/coredata/accessing-data-when-the-store-changes)
- [Consuming relevant store changes](/documentation/coredata/consuming-relevant-store-changes)
- [Persistent history](/documentation/coredata/persistent-history)

### Tracking History

- [NSPersistentHistoryToken](/documentation/coredata/nspersistenthistorytoken)

### Requesting History

- [NSPersistentHistoryChangeRequest](/documentation/coredata/nspersistenthistorychangerequest)

#### Configuring the Request

- [var fetchRequest: NSFetchRequest<any NSFetchRequestResult>?](/documentation/coredata/nspersistenthistorychangerequest/fetchrequest)
- [var resultType: NSPersistentHistoryResultType](/documentation/coredata/nspersistenthistorychangerequest/resulttype)

#### Getting the Token

- [var token: NSPersistentHistoryToken?](/documentation/coredata/nspersistenthistorychangerequest/token)

#### Fetching History

- [class func fetchHistory(after: Date) -> Self](/documentation/coredata/nspersistenthistorychangerequest/fetchhistory(after:)-qi5b)
- [class func fetchHistory(after: NSPersistentHistoryToken?) -> Self](/documentation/coredata/nspersistenthistorychangerequest/fetchhistory(after:)-3rmfm)
- [class func fetchHistory(after: NSPersistentHistoryTransaction?) -> Self](/documentation/coredata/nspersistenthistorychangerequest/fetchhistory(after:)-9cuj5)
- [class func fetchHistory(withFetch: NSFetchRequest<any NSFetchRequestResult>) -> Self](/documentation/coredata/nspersistenthistorychangerequest/fetchhistory(withfetch:))

#### Purging History

- [class func deleteHistory(before: Date) -> Self](/documentation/coredata/nspersistenthistorychangerequest/deletehistory(before:)-7t2th)
- [class func deleteHistory(before: NSPersistentHistoryToken?) -> Self](/documentation/coredata/nspersistenthistorychangerequest/deletehistory(before:)-5kghb)
- [class func deleteHistory(before: NSPersistentHistoryTransaction?) -> Self](/documentation/coredata/nspersistenthistorychangerequest/deletehistory(before:)-9l06p)
- [NSPersistentHistoryResult](/documentation/coredata/nspersistenthistoryresult)

#### Inspecting History Results

- [var result: Any?](/documentation/coredata/nspersistenthistoryresult/result)
- [var resultType: NSPersistentHistoryResultType](/documentation/coredata/nspersistenthistoryresult/resulttype)
- [NSPersistentHistoryResultType](/documentation/coredata/nspersistenthistoryresulttype)

##### Result Types

- [case statusOnly](/documentation/coredata/nspersistenthistoryresulttype/statusonly)
- [case count](/documentation/coredata/nspersistenthistoryresulttype/count)
- [case objectIDs](/documentation/coredata/nspersistenthistoryresulttype/objectids)
- [case transactionsAndChanges](/documentation/coredata/nspersistenthistoryresulttype/transactionsandchanges)
- [case transactionsOnly](/documentation/coredata/nspersistenthistoryresulttype/transactionsonly)
- [case changesOnly](/documentation/coredata/nspersistenthistoryresulttype/changesonly)

##### Initializers

- [init?(rawValue: Int)](/documentation/coredata/nspersistenthistoryresulttype/init(rawvalue:))

### Reading History

- [NSPersistentHistoryTransaction](/documentation/coredata/nspersistenthistorytransaction)

#### Requesting Notifications

- [func objectIDNotification() -> Notification](/documentation/coredata/nspersistenthistorytransaction/objectidnotification())

#### Customizing History Fetch Requests

- [class var fetchRequest: NSFetchRequest<any NSFetchRequestResult>?](/documentation/coredata/nspersistenthistorytransaction/fetchrequest)
- [class var entityDescription: NSEntityDescription?](/documentation/coredata/nspersistenthistorytransaction/entitydescription)
- [class func entityDescription(with: NSManagedObjectContext) -> NSEntityDescription?](/documentation/coredata/nspersistenthistorytransaction/entitydescription(with:))

#### Inspecting Transaction Details

- [var author: String?](/documentation/coredata/nspersistenthistorytransaction/author)
- [var bundleID: String](/documentation/coredata/nspersistenthistorytransaction/bundleid)
- [var changes: [NSPersistentHistoryChange]?](/documentation/coredata/nspersistenthistorytransaction/changes)
- [var contextName: String?](/documentation/coredata/nspersistenthistorytransaction/contextname)
- [var processID: String](/documentation/coredata/nspersistenthistorytransaction/processid)
- [var storeID: String](/documentation/coredata/nspersistenthistorytransaction/storeid)
- [var timestamp: Date](/documentation/coredata/nspersistenthistorytransaction/timestamp)
- [var token: NSPersistentHistoryToken](/documentation/coredata/nspersistenthistorytransaction/token)
- [var transactionNumber: Int64](/documentation/coredata/nspersistenthistorytransaction/transactionnumber)
- [NSPersistentHistoryChange](/documentation/coredata/nspersistenthistorychange)

#### Inspecting Change Metadata

- [class var fetchRequest: NSFetchRequest<any NSFetchRequestResult>?](/documentation/coredata/nspersistenthistorychange/fetchrequest)
- [class var entityDescription: NSEntityDescription?](/documentation/coredata/nspersistenthistorychange/entitydescription)
- [class func entityDescription(with: NSManagedObjectContext) -> NSEntityDescription?](/documentation/coredata/nspersistenthistorychange/entitydescription(with:))

#### Inspecting Change Details

- [var changeID: Int64](/documentation/coredata/nspersistenthistorychange/changeid)
- [var changeType: NSPersistentHistoryChangeType](/documentation/coredata/nspersistenthistorychange/changetype)
- [NSPersistentHistoryChangeType](/documentation/coredata/nspersistenthistorychangetype)

##### Change Types

- [case delete](/documentation/coredata/nspersistenthistorychangetype/delete)
- [case insert](/documentation/coredata/nspersistenthistorychangetype/insert)
- [case update](/documentation/coredata/nspersistenthistorychangetype/update)

##### Initializers

- [init?(rawValue: Int)](/documentation/coredata/nspersistenthistorychangetype/init(rawvalue:))
- [var changedObjectID: NSManagedObjectID](/documentation/coredata/nspersistenthistorychange/changedobjectid)
- [var tombstone: [AnyHashable : Any]?](/documentation/coredata/nspersistenthistorychange/tombstone)
- [var transaction: NSPersistentHistoryTransaction?](/documentation/coredata/nspersistenthistorychange/transaction)
- [var updatedProperties: Set<NSPropertyDescription>?](/documentation/coredata/nspersistenthistorychange/updatedproperties)

## Background tasks

- [Using Core Data in the background](/documentation/coredata/using-core-data-in-the-background)
- [Loading and displaying a large data feed](/documentation/swiftui/loading-and-displaying-a-large-data-feed)
- [Conflict resolution](/documentation/coredata/conflict-resolution)

### Conflict Management

- [NSConstraintConflict](/documentation/coredata/nsconstraintconflict)

#### Initializing a Conflict

- [init(constraint: [String], database: NSManagedObject?, databaseSnapshot: [AnyHashable : Any]?, conflicting: [NSManagedObject], conflictingSnapshots: [Any])](/documentation/coredata/nsconstraintconflict/init(constraint:database:databasesnapshot:conflicting:conflictingsnapshots:))

#### Inspecting a Conflict

- [var conflictingObjects: [NSManagedObject]](/documentation/coredata/nsconstraintconflict/conflictingobjects)
- [var conflictingSnapshots: [[AnyHashable : Any]]](/documentation/coredata/nsconstraintconflict/conflictingsnapshots)
- [var constraint: [String]](/documentation/coredata/nsconstraintconflict/constraint)
- [var constraintValues: [String : Any]](/documentation/coredata/nsconstraintconflict/constraintvalues)
- [var databaseObject: NSManagedObject?](/documentation/coredata/nsconstraintconflict/databaseobject)
- [var databaseSnapshot: [String : Any]?](/documentation/coredata/nsconstraintconflict/databasesnapshot)
- [NSMergeConflict](/documentation/coredata/nsmergeconflict)

#### Initializing a Merge Conflict

- [init(source: NSManagedObject, newVersion: Int, oldVersion: Int, cachedSnapshot: [String : Any]?, persistedSnapshot: [String : Any]?)](/documentation/coredata/nsmergeconflict/init(source:newversion:oldversion:cachedsnapshot:persistedsnapshot:))

#### Accessing Merge Conflict Details

- [var sourceObject: NSManagedObject](/documentation/coredata/nsmergeconflict/sourceobject)
- [var objectSnapshot: [String : Any]?](/documentation/coredata/nsmergeconflict/objectsnapshot)
- [var cachedSnapshot: [String : Any]?](/documentation/coredata/nsmergeconflict/cachedsnapshot)
- [var persistedSnapshot: [String : Any]?](/documentation/coredata/nsmergeconflict/persistedsnapshot)
- [var newVersionNumber: Int](/documentation/coredata/nsmergeconflict/newversionnumber)
- [var oldVersionNumber: Int](/documentation/coredata/nsmergeconflict/oldversionnumber)
- [NSMergePolicy](/documentation/coredata/nsmergepolicy)

#### Getting a Merge Policy

- [init(merge: NSMergePolicyType)](/documentation/coredata/nsmergepolicy/init(merge:))
- [var mergeType: NSMergePolicyType](/documentation/coredata/nsmergepolicy/mergetype)

#### Resolving a Conflict

- [func resolve(mergeConflicts: [Any]) throws](/documentation/coredata/nsmergepolicy/resolve(mergeconflicts:))
- [func resolve(constraintConflicts: [NSConstraintConflict]) throws](/documentation/coredata/nsmergepolicy/resolve(constraintconflicts:))
- [func resolve(optimisticLockingConflicts: [NSMergeConflict]) throws](/documentation/coredata/nsmergepolicy/resolve(optimisticlockingconflicts:))

#### Defining Merge Policies

- [class var error: NSMergePolicy](/documentation/coredata/nsmergepolicy/error)
- [class var mergeByPropertyStoreTrump: NSMergePolicy](/documentation/coredata/nsmergepolicy/mergebypropertystoretrump)
- [class var mergeByPropertyObjectTrump: NSMergePolicy](/documentation/coredata/nsmergepolicy/mergebypropertyobjecttrump)
- [class var overwrite: NSMergePolicy](/documentation/coredata/nsmergepolicy/overwrite)
- [class var rollback: NSMergePolicy](/documentation/coredata/nsmergepolicy/rollback)
- [Merge Policies](/documentation/coredata/merge-policies)

##### Policies

- [var NSErrorMergePolicy: AnyObject](/documentation/coredata/nserrormergepolicy)
- [var NSMergeByPropertyStoreTrumpMergePolicy: AnyObject](/documentation/coredata/nsmergebypropertystoretrumpmergepolicy)
- [var NSMergeByPropertyObjectTrumpMergePolicy: AnyObject](/documentation/coredata/nsmergebypropertyobjecttrumpmergepolicy)
- [var NSOverwriteMergePolicy: AnyObject](/documentation/coredata/nsoverwritemergepolicy)
- [var NSRollbackMergePolicy: AnyObject](/documentation/coredata/nsrollbackmergepolicy)
- [NSMergePolicyType](/documentation/coredata/nsmergepolicytype)

###### Policies

- [case errorMergePolicyType](/documentation/coredata/nsmergepolicytype/errormergepolicytype)
- [case mergeByPropertyStoreTrumpMergePolicyType](/documentation/coredata/nsmergepolicytype/mergebypropertystoretrumpmergepolicytype)
- [case mergeByPropertyObjectTrumpMergePolicyType](/documentation/coredata/nsmergepolicytype/mergebypropertyobjecttrumpmergepolicytype)
- [case overwriteMergePolicyType](/documentation/coredata/nsmergepolicytype/overwritemergepolicytype)
- [case rollbackMergePolicyType](/documentation/coredata/nsmergepolicytype/rollbackmergepolicytype)

###### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsmergepolicytype/init(rawvalue:))
- [NSQueryGenerationToken](/documentation/coredata/nsquerygenerationtoken)

#### Identifying Generations of App Data

- [class var current: NSQueryGenerationToken](/documentation/coredata/nsquerygenerationtoken/current)
- [Batch processing](/documentation/coredata/batch-processing)

### Data Inserts

- [NSBatchInsertRequest](/documentation/coredata/nsbatchinsertrequest)

#### Creating a Request

- [convenience init(entity: NSEntityDescription, dictionaryHandler: (NSMutableDictionary) -> Bool)](/documentation/coredata/nsbatchinsertrequest/init(entity:dictionaryhandler:))
- [convenience init(entity: NSEntityDescription, managedObjectHandler: (NSManagedObject) -> Bool)](/documentation/coredata/nsbatchinsertrequest/init(entity:managedobjecthandler:))
- [convenience init(entityName: String, dictionaryHandler: (NSMutableDictionary) -> Bool)](/documentation/coredata/nsbatchinsertrequest/init(entityname:dictionaryhandler:))
- [convenience init(entityName: String, managedObjectHandler: (NSManagedObject) -> Bool)](/documentation/coredata/nsbatchinsertrequest/init(entityname:managedobjecthandler:))
- [init(entity: NSEntityDescription, objects: [[String : Any]])](/documentation/coredata/nsbatchinsertrequest/init(entity:objects:))
- [init(entityName: String, objects: [[String : Any]])](/documentation/coredata/nsbatchinsertrequest/init(entityname:objects:))
- [convenience init()](/documentation/coredata/nsbatchinsertrequest/init())

#### Configuring a Request

- [var dictionaryHandler: ((NSMutableDictionary) -> Bool)?](/documentation/coredata/nsbatchinsertrequest/dictionaryhandler)
- [var entity: NSEntityDescription?](/documentation/coredata/nsbatchinsertrequest/entity)
- [var entityName: String](/documentation/coredata/nsbatchinsertrequest/entityname)
- [var managedObjectHandler: ((NSManagedObject) -> Bool)?](/documentation/coredata/nsbatchinsertrequest/managedobjecthandler)
- [var objectsToInsert: [[String : Any]]?](/documentation/coredata/nsbatchinsertrequest/objectstoinsert)
- [var resultType: NSBatchInsertRequestResultType](/documentation/coredata/nsbatchinsertrequest/resulttype)
- [NSBatchInsertResult](/documentation/coredata/nsbatchinsertresult)

#### Accessing Results

- [var result: Any?](/documentation/coredata/nsbatchinsertresult/result)
- [var resultType: NSBatchInsertRequestResultType](/documentation/coredata/nsbatchinsertresult/resulttype)
- [NSBatchInsertRequestResultType](/documentation/coredata/nsbatchinsertrequestresulttype)

##### Request Types

- [case statusOnly](/documentation/coredata/nsbatchinsertrequestresulttype/statusonly)
- [case objectIDs](/documentation/coredata/nsbatchinsertrequestresulttype/objectids)
- [case count](/documentation/coredata/nsbatchinsertrequestresulttype/count)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsbatchinsertrequestresulttype/init(rawvalue:))

### Data Updates

- [NSBatchUpdateRequest](/documentation/coredata/nsbatchupdaterequest)

#### Creating a Request

- [init(entity: NSEntityDescription)](/documentation/coredata/nsbatchupdaterequest/init(entity:))
- [init(entityName: String)](/documentation/coredata/nsbatchupdaterequest/init(entityname:))

#### Configuring a Request

- [var entity: NSEntityDescription](/documentation/coredata/nsbatchupdaterequest/entity)
- [var entityName: String](/documentation/coredata/nsbatchupdaterequest/entityname)
- [var includesSubentities: Bool](/documentation/coredata/nsbatchupdaterequest/includessubentities)
- [var predicate: NSPredicate?](/documentation/coredata/nsbatchupdaterequest/predicate)
- [var propertiesToUpdate: [AnyHashable : Any]?](/documentation/coredata/nsbatchupdaterequest/propertiestoupdate)
- [var resultType: NSBatchUpdateRequestResultType](/documentation/coredata/nsbatchupdaterequest/resulttype)
- [NSBatchUpdateResult](/documentation/coredata/nsbatchupdateresult)

#### Accessing Results

- [var result: Any?](/documentation/coredata/nsbatchupdateresult/result)
- [var resultType: NSBatchUpdateRequestResultType](/documentation/coredata/nsbatchupdateresult/resulttype)
- [NSBatchUpdateRequestResultType](/documentation/coredata/nsbatchupdaterequestresulttype)

##### Request Types

- [case statusOnlyResultType](/documentation/coredata/nsbatchupdaterequestresulttype/statusonlyresulttype)
- [case updatedObjectIDsResultType](/documentation/coredata/nsbatchupdaterequestresulttype/updatedobjectidsresulttype)
- [case updatedObjectsCountResultType](/documentation/coredata/nsbatchupdaterequestresulttype/updatedobjectscountresulttype)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsbatchupdaterequestresulttype/init(rawvalue:))

### Data Deletion

- [NSBatchDeleteRequest](/documentation/coredata/nsbatchdeleterequest)

#### Creating a Request

- [init(fetchRequest: NSFetchRequest<any NSFetchRequestResult>)](/documentation/coredata/nsbatchdeleterequest/init(fetchrequest:))
- [convenience init(objectIDs: [NSManagedObjectID])](/documentation/coredata/nsbatchdeleterequest/init(objectids:))

#### Accessing the Fetch Request

- [var fetchRequest: NSFetchRequest<any NSFetchRequestResult>](/documentation/coredata/nsbatchdeleterequest/fetchrequest)

#### Configuring the Result Type

- [var resultType: NSBatchDeleteRequestResultType](/documentation/coredata/nsbatchdeleterequest/resulttype)
- [NSBatchDeleteRequestResultType](/documentation/coredata/nsbatchdeleterequestresulttype)

##### Result Types

- [case resultTypeCount](/documentation/coredata/nsbatchdeleterequestresulttype/resulttypecount)
- [case resultTypeObjectIDs](/documentation/coredata/nsbatchdeleterequestresulttype/resulttypeobjectids)
- [case resultTypeStatusOnly](/documentation/coredata/nsbatchdeleterequestresulttype/resulttypestatusonly)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsbatchdeleterequestresulttype/init(rawvalue:))
- [NSBatchDeleteResult](/documentation/coredata/nsbatchdeleteresult)

#### Accessing the Result

- [var result: Any?](/documentation/coredata/nsbatchdeleteresult/result)
- [var resultType: NSBatchDeleteRequestResultType](/documentation/coredata/nsbatchdeleteresult/resulttype)
- [NSBatchDeleteRequestResultType](/documentation/coredata/nsbatchdeleterequestresulttype)

##### Result Types

- [case resultTypeCount](/documentation/coredata/nsbatchdeleterequestresulttype/resulttypecount)
- [case resultTypeObjectIDs](/documentation/coredata/nsbatchdeleterequestresulttype/resulttypeobjectids)
- [case resultTypeStatusOnly](/documentation/coredata/nsbatchdeleterequestresulttype/resulttypestatusonly)

##### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsbatchdeleterequestresulttype/init(rawvalue:))

## Data model migration

- [Migrating your data model automatically](/documentation/coredata/migrating-your-data-model-automatically)
- [Staged migrations](/documentation/coredata/staged-migrations)

### Migration staging

- [let NSPersistentStoreStagedMigrationManagerOptionKey: String](/documentation/coredata/nspersistentstorestagedmigrationmanageroptionkey)
- [NSStagedMigrationManager](/documentation/coredata/nsstagedmigrationmanager)

#### Creating a migration manager

- [convenience init([NSMigrationStage])](/documentation/coredata/nsstagedmigrationmanager/init(_:))

#### Accessing the persistent container

- [var container: NSPersistentContainer?](/documentation/coredata/nsstagedmigrationmanager/container)

#### Accessing the stages

- [var stages: [NSMigrationStage]](/documentation/coredata/nsstagedmigrationmanager/stages)

### Migration stages

- [NSLightweightMigrationStage](/documentation/coredata/nslightweightmigrationstage)

#### Creating a migration stage

- [convenience init([String])](/documentation/coredata/nslightweightmigrationstage/init(_:))

#### Accessing the checksums

- [var versionChecksums: [String]](/documentation/coredata/nslightweightmigrationstage/versionchecksums)
- [NSCustomMigrationStage](/documentation/coredata/nscustommigrationstage)

#### Creating a custom migration stage

- [convenience init(migratingFrom: NSManagedObjectModelReference, to: NSManagedObjectModelReference)](/documentation/coredata/nscustommigrationstage/init(migratingfrom:to:))
- [NSManagedObjectModelReference](/documentation/coredata/nsmanagedobjectmodelreference)

##### Creating a reference

- [init(model: NSManagedObjectModel, versionChecksum: String)](/documentation/coredata/nsmanagedobjectmodelreference/init(model:versionchecksum:))
- [init(fileURL: URL, versionChecksum: String)](/documentation/coredata/nsmanagedobjectmodelreference/init(fileurl:versionchecksum:))
- [init(name: String, in: Bundle?, versionChecksum: String)](/documentation/coredata/nsmanagedobjectmodelreference/init(name:in:versionchecksum:))
- [init(entityVersionHashes: [AnyHashable : Any], in: Bundle?, versionChecksum: String)](/documentation/coredata/nsmanagedobjectmodelreference/init(entityversionhashes:in:versionchecksum:))

##### Resolving the model object

- [var resolvedModel: NSManagedObjectModel](/documentation/coredata/nsmanagedobjectmodelreference/resolvedmodel)
- [var versionChecksum: String](/documentation/coredata/nsmanagedobjectmodelreference/versionchecksum)

#### Accessing model references

- [var currentModel: NSManagedObjectModelReference](/documentation/coredata/nscustommigrationstage/currentmodel)
- [var nextModel: NSManagedObjectModelReference](/documentation/coredata/nscustommigrationstage/nextmodel)

#### Assigning event handlers

- [var willMigrateHandler: ((NSStagedMigrationManager, NSCustomMigrationStage) throws -> Void)?](/documentation/coredata/nscustommigrationstage/willmigratehandler-5wead)
- [var didMigrateHandler: ((NSStagedMigrationManager, NSCustomMigrationStage) throws -> Void)?](/documentation/coredata/nscustommigrationstage/didmigratehandler-2zbss)
- [NSMigrationStage](/documentation/coredata/nsmigrationstage)

#### Describing the purpose

- [var label: String!](/documentation/coredata/nsmigrationstage/label)
- [Manual migrations](/documentation/coredata/manual-migrations)

### Entity Mapping

- [NSMigrationManager](/documentation/coredata/nsmigrationmanager)

#### Creating a Migration Manager

- [init(sourceModel: NSManagedObjectModel, destinationModel: NSManagedObjectModel)](/documentation/coredata/nsmigrationmanager/init(sourcemodel:destinationmodel:))

#### Getting the Manager’s Configuration

- [var destinationContext: NSManagedObjectContext](/documentation/coredata/nsmigrationmanager/destinationcontext)
- [var destinationModel: NSManagedObjectModel](/documentation/coredata/nsmigrationmanager/destinationmodel)
- [var mappingModel: NSMappingModel](/documentation/coredata/nsmigrationmanager/mappingmodel)
- [var sourceContext: NSManagedObjectContext](/documentation/coredata/nsmigrationmanager/sourcecontext)
- [var sourceModel: NSManagedObjectModel](/documentation/coredata/nsmigrationmanager/sourcemodel)
- [func destinationEntity(for: NSEntityMapping) -> NSEntityDescription?](/documentation/coredata/nsmigrationmanager/destinationentity(for:))
- [func sourceEntity(for: NSEntityMapping) -> NSEntityDescription?](/documentation/coredata/nsmigrationmanager/sourceentity(for:))

#### Customizing the Manager

- [var userInfo: [AnyHashable : Any]?](/documentation/coredata/nsmigrationmanager/userinfo)
- [var usesStoreSpecificMigrationManager: Bool](/documentation/coredata/nsmigrationmanager/usesstorespecificmigrationmanager)

#### Managing Sources and Destinations

- [func associate(sourceInstance: NSManagedObject, withDestinationInstance: NSManagedObject, for: NSEntityMapping)](/documentation/coredata/nsmigrationmanager/associate(sourceinstance:withdestinationinstance:for:))
- [func destinationInstances(forEntityMappingName: String, sourceInstances: [NSManagedObject]?) -> [NSManagedObject]](/documentation/coredata/nsmigrationmanager/destinationinstances(forentitymappingname:sourceinstances:))
- [func sourceInstances(forEntityMappingName: String, destinationInstances: [NSManagedObject]?) -> [NSManagedObject]](/documentation/coredata/nsmigrationmanager/sourceinstances(forentitymappingname:destinationinstances:))

#### Performing a Migration

- [func migrateStore(from: URL, type: NSPersistentStore.StoreType, options: [AnyHashable : Any]?, mapping: NSMappingModel, to: URL, type: NSPersistentStore.StoreType, options: [AnyHashable : Any]?) throws](/documentation/coredata/nsmigrationmanager/migratestore(from:type:options:mapping:to:type:options:))
- [func migrateStore(from: URL, sourceType: String, options: [AnyHashable : Any]?, with: NSMappingModel?, toDestinationURL: URL, destinationType: String, destinationOptions: [AnyHashable : Any]?) throws](/documentation/coredata/nsmigrationmanager/migratestore(from:sourcetype:options:with:todestinationurl:destinationtype:destinationoptions:))

#### Monitoring a Migration’s Progress

- [var migrationProgress: Float](/documentation/coredata/nsmigrationmanager/migrationprogress)
- [var currentEntityMapping: NSEntityMapping](/documentation/coredata/nsmigrationmanager/currententitymapping)

#### Aborting a Migration

- [func cancelMigrationWithError(any Error)](/documentation/coredata/nsmigrationmanager/cancelmigrationwitherror(_:))
- [func reset()](/documentation/coredata/nsmigrationmanager/reset())

#### Deprecated

- [Deprecated Symbols](/documentation/coredata/nsmigrationmanager-deprecated-symbols)

##### Deprecated Methods

- [func migrateStore(from: URL, sourceType: String, options: [AnyHashable : Any]?, with: NSMappingModel?, toDestinationURL: URL, destinationType: String, destinationOptions: [AnyHashable : Any]?) throws](/documentation/coredata/nsmigrationmanager/migratestore(from:sourcetype:options:with:todestinationurl:destinationtype:destinationoptions:))
- [NSMappingModel](/documentation/coredata/nsmappingmodel)

#### Creating a Mapping

- [init?(from: [Bundle]?, forSourceModel: NSManagedObjectModel?, destinationModel: NSManagedObjectModel?)](/documentation/coredata/nsmappingmodel/init(from:forsourcemodel:destinationmodel:))
- [class func inferredMappingModel(forSourceModel: NSManagedObjectModel, destinationModel: NSManagedObjectModel) throws -> NSMappingModel](/documentation/coredata/nsmappingmodel/inferredmappingmodel(forsourcemodel:destinationmodel:))
- [init?(contentsOf: URL?)](/documentation/coredata/nsmappingmodel/init(contentsof:))

#### Managing Entity Mappings

- [var entityMappings: [NSEntityMapping]!](/documentation/coredata/nsmappingmodel/entitymappings)
- [var entityMappingsByName: [String : NSEntityMapping]](/documentation/coredata/nsmappingmodel/entitymappingsbyname)
- [NSEntityMapping](/documentation/coredata/nsentitymapping)

#### Managing Source Information

- [var sourceEntityName: String?](/documentation/coredata/nsentitymapping/sourceentityname)
- [var sourceEntityVersionHash: Data?](/documentation/coredata/nsentitymapping/sourceentityversionhash)
- [var sourceExpression: NSExpression?](/documentation/coredata/nsentitymapping/sourceexpression)

#### Managing Destination Information

- [var destinationEntityName: String?](/documentation/coredata/nsentitymapping/destinationentityname)
- [var destinationEntityVersionHash: Data?](/documentation/coredata/nsentitymapping/destinationentityversionhash)

#### Managing Mapping Information

- [var name: String!](/documentation/coredata/nsentitymapping/name)
- [var mappingType: NSEntityMappingType](/documentation/coredata/nsentitymapping/mappingtype)
- [var entityMigrationPolicyClassName: String?](/documentation/coredata/nsentitymapping/entitymigrationpolicyclassname)
- [var attributeMappings: [NSPropertyMapping]?](/documentation/coredata/nsentitymapping/attributemappings)
- [var relationshipMappings: [NSPropertyMapping]?](/documentation/coredata/nsentitymapping/relationshipmappings)
- [var userInfo: [AnyHashable : Any]?](/documentation/coredata/nsentitymapping/userinfo)

#### Constants

- [case undefinedEntityMappingType](/documentation/coredata/nsentitymappingtype/undefinedentitymappingtype)
- [case customEntityMappingType](/documentation/coredata/nsentitymappingtype/customentitymappingtype)
- [case addEntityMappingType](/documentation/coredata/nsentitymappingtype/addentitymappingtype)
- [case removeEntityMappingType](/documentation/coredata/nsentitymappingtype/removeentitymappingtype)
- [case copyEntityMappingType](/documentation/coredata/nsentitymappingtype/copyentitymappingtype)
- [case transformEntityMappingType](/documentation/coredata/nsentitymappingtype/transformentitymappingtype)
- [NSEntityMigrationPolicy](/documentation/coredata/nsentitymigrationpolicy)

#### Customizing Stages of the Mapping Life Cycle

- [func begin(NSEntityMapping, with: NSMigrationManager) throws](/documentation/coredata/nsentitymigrationpolicy/begin(_:with:))
- [func createDestinationInstances(forSource: NSManagedObject, in: NSEntityMapping, manager: NSMigrationManager) throws](/documentation/coredata/nsentitymigrationpolicy/createdestinationinstances(forsource:in:manager:))
- [func endInstanceCreation(forMapping: NSEntityMapping, manager: NSMigrationManager) throws](/documentation/coredata/nsentitymigrationpolicy/endinstancecreation(formapping:manager:))
- [func createRelationships(forDestination: NSManagedObject, in: NSEntityMapping, manager: NSMigrationManager) throws](/documentation/coredata/nsentitymigrationpolicy/createrelationships(fordestination:in:manager:))
- [func endRelationshipCreation(forMapping: NSEntityMapping, manager: NSMigrationManager) throws](/documentation/coredata/nsentitymigrationpolicy/endrelationshipcreation(formapping:manager:))
- [func performCustomValidation(forMapping: NSEntityMapping, manager: NSMigrationManager) throws](/documentation/coredata/nsentitymigrationpolicy/performcustomvalidation(formapping:manager:))
- [func end(NSEntityMapping, manager: NSMigrationManager) throws](/documentation/coredata/nsentitymigrationpolicy/end(_:manager:))

#### Constants

- [let NSMigrationManagerKey: String](/documentation/coredata/nsmigrationmanagerkey)
- [let NSMigrationSourceObjectKey: String](/documentation/coredata/nsmigrationsourceobjectkey)
- [let NSMigrationDestinationObjectKey: String](/documentation/coredata/nsmigrationdestinationobjectkey)
- [let NSMigrationEntityMappingKey: String](/documentation/coredata/nsmigrationentitymappingkey)
- [let NSMigrationPropertyMappingKey: String](/documentation/coredata/nsmigrationpropertymappingkey)
- [let NSMigrationEntityPolicyKey: String](/documentation/coredata/nsmigrationentitypolicykey)
- [NSEntityMappingType](/documentation/coredata/nsentitymappingtype)

#### Enumeration Cases

- [case addEntityMappingType](/documentation/coredata/nsentitymappingtype/addentitymappingtype)
- [case copyEntityMappingType](/documentation/coredata/nsentitymappingtype/copyentitymappingtype)
- [case customEntityMappingType](/documentation/coredata/nsentitymappingtype/customentitymappingtype)
- [case removeEntityMappingType](/documentation/coredata/nsentitymappingtype/removeentitymappingtype)
- [case transformEntityMappingType](/documentation/coredata/nsentitymappingtype/transformentitymappingtype)
- [case undefinedEntityMappingType](/documentation/coredata/nsentitymappingtype/undefinedentitymappingtype)

#### Initializers

- [init?(rawValue: UInt)](/documentation/coredata/nsentitymappingtype/init(rawvalue:))
- [NSPropertyMapping](/documentation/coredata/nspropertymapping)

#### Managing Mapping Attributes

- [var name: String?](/documentation/coredata/nspropertymapping/name)
- [var valueExpression: NSExpression?](/documentation/coredata/nspropertymapping/valueexpression)
- [var userInfo: [AnyHashable : Any]?](/documentation/coredata/nspropertymapping/userinfo)

## Related types

- [Core Data Constants](/documentation/coredata/core-data-constants)

### Core Data Versions

- [var NSCoreDataVersionNumber: Double](/documentation/coredata/nscoredataversionnumber)
- [var NSCoreDataVersionNumber10_10: Double](/documentation/coredata/nscoredataversionnumber10_10)
- [var NSCoreDataVersionNumber10_10_2: Double](/documentation/coredata/nscoredataversionnumber10_10_2)
- [var NSCoreDataVersionNumber10_10_3: Double](/documentation/coredata/nscoredataversionnumber10_10_3)
- [var NSCoreDataVersionNumber10_11: Double](/documentation/coredata/nscoredataversionnumber10_11)
- [var NSCoreDataVersionNumber10_11_3: Double](/documentation/coredata/nscoredataversionnumber10_11_3)
- [var NSCoreDataVersionNumber10_4: Double](/documentation/coredata/nscoredataversionnumber10_4)
- [var NSCoreDataVersionNumber10_4_3: Double](/documentation/coredata/nscoredataversionnumber10_4_3)
- [var NSCoreDataVersionNumber10_5: Double](/documentation/coredata/nscoredataversionnumber10_5)
- [var NSCoreDataVersionNumber10_5_3: Double](/documentation/coredata/nscoredataversionnumber10_5_3)
- [var NSCoreDataVersionNumber10_6: Double](/documentation/coredata/nscoredataversionnumber10_6)
- [var NSCoreDataVersionNumber10_6_2: Double](/documentation/coredata/nscoredataversionnumber10_6_2)
- [var NSCoreDataVersionNumber10_6_3: Double](/documentation/coredata/nscoredataversionnumber10_6_3)
- [var NSCoreDataVersionNumber10_7: Double](/documentation/coredata/nscoredataversionnumber10_7)
- [var NSCoreDataVersionNumber10_7_2: Double](/documentation/coredata/nscoredataversionnumber10_7_2)
- [var NSCoreDataVersionNumber10_7_3: Double](/documentation/coredata/nscoredataversionnumber10_7_3)
- [var NSCoreDataVersionNumber10_7_4: Double](/documentation/coredata/nscoredataversionnumber10_7_4)
- [var NSCoreDataVersionNumber10_8: Double](/documentation/coredata/nscoredataversionnumber10_8)
- [var NSCoreDataVersionNumber10_8_2: Double](/documentation/coredata/nscoredataversionnumber10_8_2)
- [var NSCoreDataVersionNumber10_9: Double](/documentation/coredata/nscoredataversionnumber10_9)
- [var NSCoreDataVersionNumber10_9_2: Double](/documentation/coredata/nscoredataversionnumber10_9_2)
- [var NSCoreDataVersionNumber10_9_3: Double](/documentation/coredata/nscoredataversionnumber10_9_3)
- [var NSCoreDataVersionNumber_iPhoneOS_3_0: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_3_0)
- [var NSCoreDataVersionNumber_iPhoneOS_3_1: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_3_1)
- [var NSCoreDataVersionNumber_iPhoneOS_3_2: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_3_2)
- [var NSCoreDataVersionNumber_iPhoneOS_4_0: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_4_0)
- [var NSCoreDataVersionNumber_iPhoneOS_4_1: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_4_1)
- [var NSCoreDataVersionNumber_iPhoneOS_4_2: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_4_2)
- [var NSCoreDataVersionNumber_iPhoneOS_4_3: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_4_3)
- [var NSCoreDataVersionNumber_iPhoneOS_5_0: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_5_0)
- [var NSCoreDataVersionNumber_iPhoneOS_5_1: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_5_1)
- [var NSCoreDataVersionNumber_iPhoneOS_6_0: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_6_0)
- [var NSCoreDataVersionNumber_iPhoneOS_6_1: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_6_1)
- [var NSCoreDataVersionNumber_iPhoneOS_7_0: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_7_0)
- [var NSCoreDataVersionNumber_iPhoneOS_7_1: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_7_1)
- [var NSCoreDataVersionNumber_iPhoneOS_8_0: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_8_0)
- [var NSCoreDataVersionNumber_iPhoneOS_8_3: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_8_3)
- [var NSCoreDataVersionNumber_iPhoneOS_9_0: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_9_0)
- [var NSCoreDataVersionNumber_iPhoneOS_9_2: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_9_2)
- [var NSCoreDataVersionNumber_iPhoneOS_9_3: Double](/documentation/coredata/nscoredataversionnumber_iphoneos_9_3)

### Errors

- [let NSSQLiteErrorDomain: String](/documentation/coredata/nssqliteerrordomain)
- [Validation Error Codes](/documentation/coredata/error-codes)

#### Error codes

- [var NSCoreDataError: Int](/documentation/coredata/nscoredataerror)
- [var NSEntityMigrationPolicyError: Int](/documentation/coredata/nsentitymigrationpolicyerror)
- [var NSExternalRecordImportError: Int](/documentation/coredata/nsexternalrecordimporterror)
- [var NSInferredMappingModelError: Int](/documentation/coredata/nsinferredmappingmodelerror)
- [var NSManagedObjectConstraintMergeError: Int](/documentation/coredata/nsmanagedobjectconstraintmergeerror)
- [var NSManagedObjectConstraintValidationError: Int](/documentation/coredata/nsmanagedobjectconstraintvalidationerror)
- [var NSManagedObjectContextLockingError: Int](/documentation/coredata/nsmanagedobjectcontextlockingerror)
- [var NSManagedObjectExternalRelationshipError: Int](/documentation/coredata/nsmanagedobjectexternalrelationshiperror)
- [var NSManagedObjectMergeError: Int](/documentation/coredata/nsmanagedobjectmergeerror)
- [var NSManagedObjectModelReferenceNotFoundError: Int](/documentation/coredata/nsmanagedobjectmodelreferencenotfounderror)
- [var NSManagedObjectReferentialIntegrityError: Int](/documentation/coredata/nsmanagedobjectreferentialintegrityerror)
- [var NSManagedObjectValidationError: Int](/documentation/coredata/nsmanagedobjectvalidationerror)
- [var NSMigrationCancelledError: Int](/documentation/coredata/nsmigrationcancellederror)
- [var NSMigrationConstraintViolationError: Int](/documentation/coredata/nsmigrationconstraintviolationerror)
- [var NSMigrationError: Int](/documentation/coredata/nsmigrationerror)
- [var NSMigrationManagerDestinationStoreError: Int](/documentation/coredata/nsmigrationmanagerdestinationstoreerror)
- [var NSMigrationManagerSourceStoreError: Int](/documentation/coredata/nsmigrationmanagersourcestoreerror)
- [var NSMigrationMissingMappingModelError: Int](/documentation/coredata/nsmigrationmissingmappingmodelerror)
- [var NSMigrationMissingSourceModelError: Int](/documentation/coredata/nsmigrationmissingsourcemodelerror)
- [var NSPersistentHistoryTokenExpiredError: Int](/documentation/coredata/nspersistenthistorytokenexpirederror)
- [var NSPersistentStoreCoordinatorLockingError: Int](/documentation/coredata/nspersistentstorecoordinatorlockingerror)
- [var NSPersistentStoreIncompatibleSchemaError: Int](/documentation/coredata/nspersistentstoreincompatibleschemaerror)
- [var NSPersistentStoreIncompatibleVersionHashError: Int](/documentation/coredata/nspersistentstoreincompatibleversionhasherror)
- [var NSPersistentStoreIncompleteSaveError: Int](/documentation/coredata/nspersistentstoreincompletesaveerror)
- [var NSPersistentStoreInvalidTypeError: Int](/documentation/coredata/nspersistentstoreinvalidtypeerror)
- [var NSPersistentStoreOpenError: Int](/documentation/coredata/nspersistentstoreopenerror)
- [var NSPersistentStoreOperationError: Int](/documentation/coredata/nspersistentstoreoperationerror)
- [var NSPersistentStoreSaveConflictsError: Int](/documentation/coredata/nspersistentstoresaveconflictserror)
- [var NSPersistentStoreSaveError: Int](/documentation/coredata/nspersistentstoresaveerror)
- [var NSPersistentStoreTimeoutError: Int](/documentation/coredata/nspersistentstoretimeouterror)
- [var NSPersistentStoreTypeMismatchError: Int](/documentation/coredata/nspersistentstoretypemismatcherror)
- [var NSPersistentStoreUnsupportedRequestTypeError: Int](/documentation/coredata/nspersistentstoreunsupportedrequesttypeerror)
- [var NSSQLiteError: Int](/documentation/coredata/nssqliteerror)
- [var NSStagedMigrationBackwardMigrationError: Int](/documentation/coredata/nsstagedmigrationbackwardmigrationerror)
- [var NSStagedMigrationFrameworkVersionMismatchError: Int](/documentation/coredata/nsstagedmigrationframeworkversionmismatcherror)
- [var NSValidationInvalidURIError: Int](/documentation/coredata/nsvalidationinvalidurierror)
- [var NSValidationMultipleErrorsError: Int](/documentation/coredata/nsvalidationmultipleerrorserror)
- [var NSValidationMissingMandatoryPropertyError: Int](/documentation/coredata/nsvalidationmissingmandatorypropertyerror)
- [var NSValidationRelationshipLacksMinimumCountError: Int](/documentation/coredata/nsvalidationrelationshiplacksminimumcounterror)
- [var NSValidationRelationshipExceedsMaximumCountError: Int](/documentation/coredata/nsvalidationrelationshipexceedsmaximumcounterror)
- [var NSValidationRelationshipDeniedDeleteError: Int](/documentation/coredata/nsvalidationrelationshipdenieddeleteerror)
- [var NSValidationNumberTooLargeError: Int](/documentation/coredata/nsvalidationnumbertoolargeerror)
- [var NSValidationNumberTooSmallError: Int](/documentation/coredata/nsvalidationnumbertoosmallerror)
- [var NSValidationDateTooLateError: Int](/documentation/coredata/nsvalidationdatetoolateerror)
- [var NSValidationDateTooSoonError: Int](/documentation/coredata/nsvalidationdatetoosoonerror)
- [var NSValidationInvalidDateError: Int](/documentation/coredata/nsvalidationinvaliddateerror)
- [var NSValidationStringTooLongError: Int](/documentation/coredata/nsvalidationstringtoolongerror)
- [var NSValidationStringTooShortError: Int](/documentation/coredata/nsvalidationstringtooshorterror)
- [var NSValidationStringPatternMatchingError: Int](/documentation/coredata/nsvalidationstringpatternmatchingerror)

### User Info Dictionary Keys

- [let NSAffectedObjectsErrorKey: String](/documentation/coredata/nsaffectedobjectserrorkey)
- [let NSAffectedStoresErrorKey: String](/documentation/coredata/nsaffectedstoreserrorkey)
- [let NSDetailedErrorsKey: String](/documentation/coredata/nsdetailederrorskey)
- [let NSDeletedObjectIDsKey: String](/documentation/coredata/nsdeletedobjectidskey)
- [let NSInsertedObjectIDsKey: String](/documentation/coredata/nsinsertedobjectidskey)
- [let NSInvalidatedObjectIDsKey: String](/documentation/coredata/nsinvalidatedobjectidskey)
- [let NSPersistentHistoryTokenKey: String](/documentation/coredata/nspersistenthistorytokenkey)
- [let NSPersistentStoreURLKey: String](/documentation/coredata/nspersistentstoreurlkey)
- [let NSRefreshedObjectIDsKey: String](/documentation/coredata/nsrefreshedobjectidskey)
- [let NSUpdatedObjectIDsKey: String](/documentation/coredata/nsupdatedobjectidskey)

### Persistent Store Metadata Keys

- [let NSBinaryStoreInsecureDecodingCompatibilityOption: String](/documentation/coredata/nsbinarystoreinsecuredecodingcompatibilityoption)
- [let NSBinaryStoreSecureDecodingClasses: String](/documentation/coredata/nsbinarystoresecuredecodingclasses)
- [let NSPersistentStoreRemoteChangeNotificationPostOptionKey: String](/documentation/coredata/nspersistentstoreremotechangenotificationpostoptionkey)
- [let NSPersistentStoreModelVersionChecksumKey: String](/documentation/coredata/nspersistentstoremodelversionchecksumkey)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
