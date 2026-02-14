# CloudKit Documentation

Source: https://sosumi.ai/documentation/cloudkit

---
title: CloudKit
source: https://developer.apple.com/documentation/cloudkit
timestamp: 2026-02-13T19:22:59.409Z
---

## Essentials

- [Deciding whether CloudKit is right for your app](/documentation/cloudkit/deciding-whether-cloudkit-is-right-for-your-app)
- [Enabling CloudKit in Your App](/documentation/cloudkit/enabling-cloudkit-in-your-app)

## Schemas

- [Designing and Creating a CloudKit Database](/documentation/cloudkit/designing-and-creating-a-cloudkit-database)
- [Managing iCloud Containers with CloudKit Database App](/documentation/cloudkit/managing-icloud-containers-with-cloudkit-database-app)

### Container Management

- [Inspecting and Editing an iCloud Container’s Schema](/documentation/cloudkit/inspecting-and-editing-an-icloud-container-s-schema)
- [Handling an iCloud Container’s Data](/documentation/cloudkit/handling-an-icloud-container-s-data)
- [Deploying an iCloud Container’s Schema](/documentation/cloudkit/deploying-an-icloud-container-s-schema)
- [Obtaining an API Token for an iCloud Container](/documentation/cloudkit/obtaining-an-api-token-for-an-icloud-container)
- [CKRecordZone](/documentation/cloudkit/ckrecordzone)

### Creating a Record Zone

- [init(zoneName: String)](/documentation/cloudkit/ckrecordzone/init(zonename:))
- [init(zoneID: CKRecordZone.ID)](/documentation/cloudkit/ckrecordzone/init(zoneid:))
- [CKRecordZone.ID](/documentation/cloudkit/ckrecordzone/id)

#### Creating a Record Zone ID

- [convenience init(zoneName: String, ownerName: String)](/documentation/cloudkit/ckrecordzone/id/init(zonename:ownername:)-22irr)

#### Getting the Record Zone ID Attributes

- [var zoneName: String](/documentation/cloudkit/ckrecordzone/id/zonename)
- [var ownerName: String](/documentation/cloudkit/ckrecordzone/id/ownername)

#### Accessing the Default Zone

- [static let `default`: CKRecordZone.ID](/documentation/cloudkit/ckrecordzone/id/default)
- [static let defaultZoneName: String](/documentation/cloudkit/ckrecordzone/id/defaultzonename)

#### Initializers

- [convenience init(zoneName: String, ownerName: String?)](/documentation/cloudkit/ckrecordzone/id/init(zonename:ownername:)-2hzo4)

### Getting the Default Record Zone

- [class func `default`() -> CKRecordZone](/documentation/cloudkit/ckrecordzone/default())

### Getting the Zone Attributes

- [var zoneID: CKRecordZone.ID](/documentation/cloudkit/ckrecordzone/zoneid)
- [var capabilities: CKRecordZone.Capabilities](/documentation/cloudkit/ckrecordzone/capabilities-swift.property)
- [CKRecordZone.Capabilities](/documentation/cloudkit/ckrecordzone/capabilities-swift.struct)

#### Creating Zone Capabilities

- [init(rawValue: UInt)](/documentation/cloudkit/ckrecordzone/capabilities-swift.struct/init(rawvalue:))

#### Zone Capabilities

- [static var atomic: CKRecordZone.Capabilities](/documentation/cloudkit/ckrecordzone/capabilities-swift.struct/atomic)
- [static var fetchChanges: CKRecordZone.Capabilities](/documentation/cloudkit/ckrecordzone/capabilities-swift.struct/fetchchanges)
- [static var sharing: CKRecordZone.Capabilities](/documentation/cloudkit/ckrecordzone/capabilities-swift.struct/sharing)
- [static var zoneWideSharing: CKRecordZone.Capabilities](/documentation/cloudkit/ckrecordzone/capabilities-swift.struct/zonewidesharing)

### Sharing Records

- [var share: CKRecord.Reference?](/documentation/cloudkit/ckrecordzone/share)

### Instance Properties

- [var encryptionScope: CKRecordZone.EncryptionScope](/documentation/cloudkit/ckrecordzone/encryptionscope-swift.property)

### Enumerations

- [CKRecordZone.EncryptionScope](/documentation/cloudkit/ckrecordzone/encryptionscope-swift.enum)

#### Enumeration Cases

- [case perRecord](/documentation/cloudkit/ckrecordzone/encryptionscope-swift.enum/perrecord)
- [case perZone](/documentation/cloudkit/ckrecordzone/encryptionscope-swift.enum/perzone)

#### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckrecordzone/encryptionscope-swift.enum/init(rawvalue:))
- [CKRecord](/documentation/cloudkit/ckrecord)

### Creating a Record

- [convenience init(recordType: CKRecord.RecordType, recordID: CKRecord.ID)](/documentation/cloudkit/ckrecord/init(recordtype:recordid:))
- [CKRecord.RecordType](/documentation/cloudkit/ckrecord/recordtype-swift.typealias)
- [CKRecord.FieldKey](/documentation/cloudkit/ckrecord/fieldkey)
- [convenience init(recordType: CKRecord.RecordType, zoneID: CKRecordZone.ID)](/documentation/cloudkit/ckrecord/init(recordtype:zoneid:))

### Accessing the Record’s Fields

- [func object(forKey: CKRecord.FieldKey) -> (any __CKRecordObjCValue)?](/documentation/cloudkit/ckrecord/object(forkey:))
- [subscript(String) -> (any __CKRecordObjCValue)?](/documentation/cloudkit/ckrecord/subscript(_:)-51whk)
- [subscript(CKRecord.FieldKey) -> (any __CKRecordObjCValue)?](/documentation/cloudkit/ckrecord/subscript(_:)-4g91i)
- [func setObject((any __CKRecordObjCValue)?, forKey: CKRecord.FieldKey)](/documentation/cloudkit/ckrecord/setobject(_:forkey:))
- [func allKeys() -> [CKRecord.FieldKey]](/documentation/cloudkit/ckrecord/allkeys())
- [func changedKeys() -> [CKRecord.FieldKey]](/documentation/cloudkit/ckrecord/changedkeys())
- [CKRecordKeyValueIterator](/documentation/cloudkit/ckrecordkeyvalueiterator)
- [CKRecordValueProtocol](/documentation/cloudkit/ckrecordvalueprotocol)
- [CKRecordKeyValueSetting](/documentation/cloudkit/ckrecordkeyvaluesetting)

#### Accessing a Record’s Fields

- [func object(forKey: String) -> (any __CKRecordObjCValue)?](/documentation/cloudkit/ckrecordkeyvaluesetting/object(forkey:))
- [subscript(String) -> (any __CKRecordObjCValue)?](/documentation/cloudkit/ckrecordkeyvaluesetting/subscript(_:))
- [func setObject((any __CKRecordObjCValue)?, forKey: String)](/documentation/cloudkit/ckrecordkeyvaluesetting/setobject(_:forkey:))
- [func allKeys() -> [String]](/documentation/cloudkit/ckrecordkeyvaluesetting/allkeys())
- [func changedKeys() -> [String]](/documentation/cloudkit/ckrecordkeyvaluesetting/changedkeys())
- [CKRecordValue](/documentation/cloudkit/ckrecordvalue-swift.typealias)

### Accessing the Record’s Metadata

- [var recordID: CKRecord.ID](/documentation/cloudkit/ckrecord/recordid)
- [var recordType: CKRecord.RecordType](/documentation/cloudkit/ckrecord/recordtype-6v7au)
- [CKRecord.SystemType](/documentation/cloudkit/ckrecord/systemtype)

#### Types of System Records

- [static let share: CKRecord.RecordType](/documentation/cloudkit/ckrecord/systemtype/share)
- [static let userRecord: CKRecord.RecordType](/documentation/cloudkit/ckrecord/systemtype/userrecord)
- [var creationDate: Date?](/documentation/cloudkit/ckrecord/creationdate)
- [var creatorUserRecordID: CKRecord.ID?](/documentation/cloudkit/ckrecord/creatoruserrecordid)
- [var modificationDate: Date?](/documentation/cloudkit/ckrecord/modificationdate)
- [var lastModifiedUserRecordID: CKRecord.ID?](/documentation/cloudkit/ckrecord/lastmodifieduserrecordid)
- [var recordChangeTag: String?](/documentation/cloudkit/ckrecord/recordchangetag)
- [CKRecord.ID](/documentation/cloudkit/ckrecord/id)

#### Creating a Record ID

- [convenience init(recordName: String)](/documentation/cloudkit/ckrecord/id/init(recordname:))
- [convenience init(recordName: String, zoneID: CKRecordZone.ID)](/documentation/cloudkit/ckrecord/id/init(recordname:zoneid:))
- [let CKRecordNameZoneWideShare: String](/documentation/cloudkit/ckrecordnamezonewideshare)

#### Getting the Record ID’s Name

- [var recordName: String](/documentation/cloudkit/ckrecord/id/recordname)

#### Getting the Record ID’s Zone

- [var zoneID: CKRecordZone.ID](/documentation/cloudkit/ckrecord/id/zoneid)

### Encrypting the Record’s Values

- [var encryptedValues: any CKRecordKeyValueSetting & Sendable](/documentation/cloudkit/ckrecord/encryptedvalues)

### Getting Data for Full-Text Searches

- [func allTokens() -> [String]](/documentation/cloudkit/ckrecord/alltokens())

### Encoding the Record’s Metadata

- [func encodeSystemFields(with: NSCoder)](/documentation/cloudkit/ckrecord/encodesystemfields(with:))

### Sharing Records

- [var parent: CKRecord.Reference?](/documentation/cloudkit/ckrecord/parent)
- [var share: CKRecord.Reference?](/documentation/cloudkit/ckrecord/share)
- [CKRecord.Reference](/documentation/cloudkit/ckrecord/reference)

#### Creating a Reference

- [init(recordID: CKRecord.ID, action: CKRecord.ReferenceAction)](/documentation/cloudkit/ckrecord/reference/init(recordid:action:))
- [convenience init(record: CKRecord, action: CKRecord.ReferenceAction)](/documentation/cloudkit/ckrecord/reference/init(record:action:))
- [CKRecord.Reference.Action](/documentation/cloudkit/ckrecord/reference/action-swift.typealias)

#### Getting the Reference Attributes

- [var action: CKRecord.ReferenceAction](/documentation/cloudkit/ckrecord/reference/action-swift.property)
- [var recordID: CKRecord.ID](/documentation/cloudkit/ckrecord/reference/recordid)
- [CKRecord.ReferenceAction](/documentation/cloudkit/ckrecord/referenceaction)

##### Deletion Reference Actions

- [case none](/documentation/cloudkit/ckrecord/referenceaction/none)
- [case deleteSelf](/documentation/cloudkit/ckrecord/referenceaction/deleteself)

##### Initializers

- [init?(rawValue: UInt)](/documentation/cloudkit/ckrecord/referenceaction/init(rawvalue:))
- [func setParent(CKRecord?)](/documentation/cloudkit/ckrecord/setparent(_:)-23du1)
- [func setParent(CKRecord.ID?)](/documentation/cloudkit/ckrecord/setparent(_:)-7egcx)
- [CKRecord.SystemFieldKey](/documentation/cloudkit/ckrecord/systemfieldkey)

#### Types of Shared Records

- [static let parent: CKRecord.FieldKey](/documentation/cloudkit/ckrecord/systemfieldkey/parent)
- [static let share: CKRecord.FieldKey](/documentation/cloudkit/ckrecord/systemfieldkey/share)

#### Type Properties

- [static var creationDate: CKRecord.FieldKey](/documentation/cloudkit/ckrecord/systemfieldkey/creationdate)
- [static var creatorUserRecordID: CKRecord.FieldKey](/documentation/cloudkit/ckrecord/systemfieldkey/creatoruserrecordid)
- [static var lastModifiedUserRecordID: CKRecord.FieldKey](/documentation/cloudkit/ckrecord/systemfieldkey/lastmodifieduserrecordid)
- [static var modificationDate: CKRecord.FieldKey](/documentation/cloudkit/ckrecord/systemfieldkey/modificationdate)
- [static var recordID: CKRecord.FieldKey](/documentation/cloudkit/ckrecord/systemfieldkey/recordid)
- [CKRecord.Reference](/documentation/cloudkit/ckrecord/reference)

### Creating a Reference

- [init(recordID: CKRecord.ID, action: CKRecord.ReferenceAction)](/documentation/cloudkit/ckrecord/reference/init(recordid:action:))
- [convenience init(record: CKRecord, action: CKRecord.ReferenceAction)](/documentation/cloudkit/ckrecord/reference/init(record:action:))
- [CKRecord.Reference.Action](/documentation/cloudkit/ckrecord/reference/action-swift.typealias)

### Getting the Reference Attributes

- [var action: CKRecord.ReferenceAction](/documentation/cloudkit/ckrecord/reference/action-swift.property)
- [var recordID: CKRecord.ID](/documentation/cloudkit/ckrecord/reference/recordid)
- [CKRecord.ReferenceAction](/documentation/cloudkit/ckrecord/referenceaction)

#### Deletion Reference Actions

- [case none](/documentation/cloudkit/ckrecord/referenceaction/none)
- [case deleteSelf](/documentation/cloudkit/ckrecord/referenceaction/deleteself)

#### Initializers

- [init?(rawValue: UInt)](/documentation/cloudkit/ckrecord/referenceaction/init(rawvalue:))
- [CKAsset](/documentation/cloudkit/ckasset)

### Creating an Asset

- [init(fileURL: URL)](/documentation/cloudkit/ckasset/init(fileurl:))

### Getting the URL of the Asset

- [var fileURL: URL?](/documentation/cloudkit/ckasset/fileurl)
- [Integrating a Text-Based Schema into Your Workflow](/documentation/cloudkit/integrating-a-text-based-schema-into-your-workflow)

## Records

- [Local Records](/documentation/cloudkit/local-records)

### Transactions

- [CKModifyRecordZonesOperation](/documentation/cloudkit/ckmodifyrecordzonesoperation)

#### Creating a Modify Zones Operation

- [convenience init(recordZonesToSave: [CKRecordZone]?, recordZoneIDsToDelete: [CKRecordZone.ID]?)](/documentation/cloudkit/ckmodifyrecordzonesoperation/init(recordzonestosave:recordzoneidstodelete:))
- [init()](/documentation/cloudkit/ckmodifyrecordzonesoperation/init())

#### Configuring the Modify Zones Operation

- [var recordZonesToSave: [CKRecordZone]?](/documentation/cloudkit/ckmodifyrecordzonesoperation/recordzonestosave)
- [var recordZoneIDsToDelete: [CKRecordZone.ID]?](/documentation/cloudkit/ckmodifyrecordzonesoperation/recordzoneidstodelete)

#### Processing the Modify Zones Results

- [var modifyRecordZonesCompletionBlock: (([CKRecordZone]?, [CKRecordZone.ID]?, (any Error)?) -> Void)?](/documentation/cloudkit/ckmodifyrecordzonesoperation/modifyrecordzonescompletionblock)

#### Instance Properties

- [var modifyRecordZonesResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckmodifyrecordzonesoperation/modifyrecordzonesresultblock)
- [var perRecordZoneDeleteBlock: ((CKRecordZone.ID, Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckmodifyrecordzonesoperation/perrecordzonedeleteblock-6c82y)
- [var perRecordZoneSaveBlock: ((CKRecordZone.ID, Result<CKRecordZone, any Error>) -> Void)?](/documentation/cloudkit/ckmodifyrecordzonesoperation/perrecordzonesaveblock-1m45y)
- [CKModifyRecordsOperation](/documentation/cloudkit/ckmodifyrecordsoperation)

#### Creating a Modify Record Operation

- [convenience init(recordsToSave: [CKRecord]?, recordIDsToDelete: [CKRecord.ID]?)](/documentation/cloudkit/ckmodifyrecordsoperation/init(recordstosave:recordidstodelete:))
- [init()](/documentation/cloudkit/ckmodifyrecordsoperation/init())

#### Configuring the Modify Record Operation

- [var recordsToSave: [CKRecord]?](/documentation/cloudkit/ckmodifyrecordsoperation/recordstosave)
- [var recordIDsToDelete: [CKRecord.ID]?](/documentation/cloudkit/ckmodifyrecordsoperation/recordidstodelete)
- [var clientChangeTokenData: Data?](/documentation/cloudkit/ckmodifyrecordsoperation/clientchangetokendata)
- [var isAtomic: Bool](/documentation/cloudkit/ckmodifyrecordsoperation/isatomic)
- [var savePolicy: CKModifyRecordsOperation.RecordSavePolicy](/documentation/cloudkit/ckmodifyrecordsoperation/savepolicy)
- [CKModifyRecordsOperation.RecordSavePolicy](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy)

##### Save Policies

- [case ifServerRecordUnchanged](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/ifserverrecordunchanged)
- [case changedKeys](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/changedkeys)
- [case allKeys](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/allkeys)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/init(rawvalue:))

#### Processing the Modify Record Results

- [var perRecordProgressBlock: ((CKRecord, Double) -> Void)?](/documentation/cloudkit/ckmodifyrecordsoperation/perrecordprogressblock)
- [var perRecordCompletionBlock: ((CKRecord, (any Error)?) -> Void)?](/documentation/cloudkit/ckmodifyrecordsoperation/perrecordcompletionblock)
- [var modifyRecordsCompletionBlock: (([CKRecord]?, [CKRecord.ID]?, (any Error)?) -> Void)?](/documentation/cloudkit/ckmodifyrecordsoperation/modifyrecordscompletionblock)

#### Instance Properties

- [var modifyRecordsResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckmodifyrecordsoperation/modifyrecordsresultblock)
- [var perRecordDeleteBlock: ((CKRecord.ID, Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckmodifyrecordsoperation/perrecorddeleteblock-9czoo)
- [var perRecordSaveBlock: ((CKRecord.ID, Result<CKRecord, any Error>) -> Void)?](/documentation/cloudkit/ckmodifyrecordsoperation/perrecordsaveblock-7yq9d)

### Fetch Requests

- [CKFetchRecordZonesOperation](/documentation/cloudkit/ckfetchrecordzonesoperation)

#### Initializing the Zone Fetch Operation

- [convenience init(recordZoneIDs: [CKRecordZone.ID])](/documentation/cloudkit/ckfetchrecordzonesoperation/init(recordzoneids:))
- [init()](/documentation/cloudkit/ckfetchrecordzonesoperation/init())

#### Getting All Record Zones

- [class func fetchAllRecordZonesOperation() -> Self](/documentation/cloudkit/ckfetchrecordzonesoperation/fetchallrecordzonesoperation())

#### Configuring a Zone Fetch Operation

- [var recordZoneIDs: [CKRecordZone.ID]?](/documentation/cloudkit/ckfetchrecordzonesoperation/recordzoneids)

#### Processing Zone Fetch Results

- [var fetchRecordZonesCompletionBlock: (([CKRecordZone.ID : CKRecordZone]?, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchrecordzonesoperation/fetchrecordzonescompletionblock)

#### Instance Properties

- [var fetchRecordZonesResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckfetchrecordzonesoperation/fetchrecordzonesresultblock)
- [var perRecordZoneResultBlock: ((CKRecordZone.ID, Result<CKRecordZone, any Error>) -> Void)?](/documentation/cloudkit/ckfetchrecordzonesoperation/perrecordzoneresultblock)
- [CKFetchRecordsOperation](/documentation/cloudkit/ckfetchrecordsoperation)

#### Creating a Record Fetch Operation

- [convenience init(recordIDs: [CKRecord.ID])](/documentation/cloudkit/ckfetchrecordsoperation/init(recordids:))
- [init()](/documentation/cloudkit/ckfetchrecordsoperation/init())

#### Getting the Current User Record

- [class func fetchCurrentUserRecordOperation() -> Self](/documentation/cloudkit/ckfetchrecordsoperation/fetchcurrentuserrecordoperation())

#### Configuring a Record Fetch Operation

- [var recordIDs: [CKRecord.ID]?](/documentation/cloudkit/ckfetchrecordsoperation/recordids)
- [var desiredKeys: [CKRecord.FieldKey]?](/documentation/cloudkit/ckfetchrecordsoperation/desiredkeys-31bbq)

#### Processing Record Fetch Results

- [var perRecordProgressBlock: ((CKRecord.ID, Double) -> Void)?](/documentation/cloudkit/ckfetchrecordsoperation/perrecordprogressblock)
- [var perRecordCompletionBlock: ((CKRecord?, CKRecord.ID?, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchrecordsoperation/perrecordcompletionblock)
- [var fetchRecordsCompletionBlock: (([CKRecord.ID : CKRecord]?, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchrecordsoperation/fetchrecordscompletionblock)

#### Instance Properties

- [var fetchRecordsResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckfetchrecordsoperation/fetchrecordsresultblock)
- [var perRecordResultBlock: ((CKRecord.ID, Result<CKRecord, any Error>) -> Void)?](/documentation/cloudkit/ckfetchrecordsoperation/perrecordresultblock)

### Queries

- [CKQuery](/documentation/cloudkit/ckquery)

#### Creating a Query

- [init(coder: NSCoder)](/documentation/cloudkit/ckquery/init(coder:))
- [convenience init(recordType: CKRecord.RecordType, predicate: NSPredicate)](/documentation/cloudkit/ckquery/init(recordtype:predicate:))

#### Accessing the Query Parameters

- [var recordType: CKRecord.RecordType](/documentation/cloudkit/ckquery/recordtype-6ajii)
- [var predicate: NSPredicate](/documentation/cloudkit/ckquery/predicate)
- [var sortDescriptors: [NSSortDescriptor]?](/documentation/cloudkit/ckquery/sortdescriptors)
- [CKQueryOperation](/documentation/cloudkit/ckqueryoperation)

#### Creating a Query Operation

- [convenience init(query: CKQuery)](/documentation/cloudkit/ckqueryoperation/init(query:))
- [convenience init(cursor: CKQueryOperation.Cursor)](/documentation/cloudkit/ckqueryoperation/init(cursor:))
- [init()](/documentation/cloudkit/ckqueryoperation/init())

#### Configuring the Query Operation

- [var query: CKQuery?](/documentation/cloudkit/ckqueryoperation/query)
- [var cursor: CKQueryOperation.Cursor?](/documentation/cloudkit/ckqueryoperation/cursor-swift.property)
- [CKQueryOperation.Cursor](/documentation/cloudkit/ckqueryoperation/cursor-swift.class)
- [var zoneID: CKRecordZone.ID?](/documentation/cloudkit/ckqueryoperation/zoneid)
- [var resultsLimit: Int](/documentation/cloudkit/ckqueryoperation/resultslimit)
- [class let maximumResults: Int](/documentation/cloudkit/ckqueryoperation/maximumresults)
- [var desiredKeys: [CKRecord.FieldKey]?](/documentation/cloudkit/ckqueryoperation/desiredkeys-7qrse)

#### Processing the Query Results

- [var recordFetchedBlock: ((CKRecord) -> Void)?](/documentation/cloudkit/ckqueryoperation/recordfetchedblock)
- [var queryCompletionBlock: ((CKQueryOperation.Cursor?, (any Error)?) -> Void)?](/documentation/cloudkit/ckqueryoperation/querycompletionblock)

#### Instance Properties

- [var queryResultBlock: ((Result<CKQueryOperation.Cursor?, any Error>) -> Void)?](/documentation/cloudkit/ckqueryoperation/queryresultblock)
- [var recordMatchedBlock: ((CKRecord.ID, Result<CKRecord, any Error>) -> Void)?](/documentation/cloudkit/ckqueryoperation/recordmatchedblock-2qze7)
- [CKLocationSortDescriptor](/documentation/cloudkit/cklocationsortdescriptor)

#### Creating a Location Sort Descriptor

- [init(key: String, relativeLocation: CLLocation)](/documentation/cloudkit/cklocationsortdescriptor/init(key:relativelocation:))
- [init(coder: NSCoder)](/documentation/cloudkit/cklocationsortdescriptor/init(coder:))

#### Accessing the Location Value

- [var relativeLocation: CLLocation](/documentation/cloudkit/cklocationsortdescriptor/relativelocation)

### Base Objects

- [CKDatabaseOperation](/documentation/cloudkit/ckdatabaseoperation)

#### Accessing the Database

- [var database: CKDatabase?](/documentation/cloudkit/ckdatabaseoperation/database)
- [Remote Records](/documentation/cloudkit/remote-records)

### Database Changes

- [CKDatabaseSubscription](/documentation/cloudkit/ckdatabasesubscription)

#### Creating a Database Subscription

- [convenience init()](/documentation/cloudkit/ckdatabasesubscription/init())
- [convenience init(subscriptionID: CKSubscription.ID)](/documentation/cloudkit/ckdatabasesubscription/init(subscriptionid:))
- [init(coder: NSCoder)](/documentation/cloudkit/ckdatabasesubscription/init(coder:))

#### Accessing the Subscription Metadata

- [var recordType: CKRecord.RecordType?](/documentation/cloudkit/ckdatabasesubscription/recordtype-46v7a)
- [CKDatabaseNotification](/documentation/cloudkit/ckdatabasenotification)

#### Getting the Database Scope

- [var databaseScope: CKDatabase.Scope](/documentation/cloudkit/ckdatabasenotification/databasescope)
- [CKFetchDatabaseChangesOperation](/documentation/cloudkit/ckfetchdatabasechangesoperation)

#### Creating an Operation

- [convenience init(previousServerChangeToken: CKServerChangeToken?)](/documentation/cloudkit/ckfetchdatabasechangesoperation/init(previousserverchangetoken:))
- [init()](/documentation/cloudkit/ckfetchdatabasechangesoperation/init())

#### Configuring the Operation

- [var fetchAllChanges: Bool](/documentation/cloudkit/ckfetchdatabasechangesoperation/fetchallchanges)
- [var previousServerChangeToken: CKServerChangeToken?](/documentation/cloudkit/ckfetchdatabasechangesoperation/previousserverchangetoken)
- [var resultsLimit: Int](/documentation/cloudkit/ckfetchdatabasechangesoperation/resultslimit)

#### Processing the Operation’s Results

- [var recordZoneWithIDChangedBlock: ((CKRecordZone.ID) -> Void)?](/documentation/cloudkit/ckfetchdatabasechangesoperation/recordzonewithidchangedblock)
- [var recordZoneWithIDWasDeletedBlock: ((CKRecordZone.ID) -> Void)?](/documentation/cloudkit/ckfetchdatabasechangesoperation/recordzonewithidwasdeletedblock)
- [var recordZoneWithIDWasDeletedDueToUserEncryptedDataResetBlock: ((CKRecordZone.ID) -> Void)?](/documentation/cloudkit/ckfetchdatabasechangesoperation/recordzonewithidwasdeletedduetouserencrypteddataresetblock)
- [var recordZoneWithIDWasPurgedBlock: ((CKRecordZone.ID) -> Void)?](/documentation/cloudkit/ckfetchdatabasechangesoperation/recordzonewithidwaspurgedblock)
- [var changeTokenUpdatedBlock: ((CKServerChangeToken) -> Void)?](/documentation/cloudkit/ckfetchdatabasechangesoperation/changetokenupdatedblock)
- [var fetchDatabaseChangesCompletionBlock: ((CKServerChangeToken?, Bool, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchdatabasechangesoperation/fetchdatabasechangescompletionblock)

#### Instance Properties

- [var fetchDatabaseChangesResultBlock: ((Result<(serverChangeToken: CKServerChangeToken, moreComing: Bool), any Error>) -> Void)?](/documentation/cloudkit/ckfetchdatabasechangesoperation/fetchdatabasechangesresultblock)

### Record Zone Changes

- [CKRecordZoneSubscription](/documentation/cloudkit/ckrecordzonesubscription)

#### Creating a Zone-Based Subscription

- [convenience init(zoneID: CKRecordZone.ID)](/documentation/cloudkit/ckrecordzonesubscription/init(zoneid:))
- [convenience init(zoneID: CKRecordZone.ID, subscriptionID: CKSubscription.ID)](/documentation/cloudkit/ckrecordzonesubscription/init(zoneid:subscriptionid:))
- [init(coder: NSCoder)](/documentation/cloudkit/ckrecordzonesubscription/init(coder:))

#### Accessing the Subscription Metadata

- [var recordType: CKRecord.RecordType?](/documentation/cloudkit/ckrecordzonesubscription/recordtype-1fuqo)
- [var zoneID: CKRecordZone.ID](/documentation/cloudkit/ckrecordzonesubscription/zoneid)
- [CKRecordZoneNotification](/documentation/cloudkit/ckrecordzonenotification)

#### Getting the Record Zone ID

- [var recordZoneID: CKRecordZone.ID?](/documentation/cloudkit/ckrecordzonenotification/recordzoneid)

#### Getting the Database Scope

- [var databaseScope: CKDatabase.Scope](/documentation/cloudkit/ckrecordzonenotification/databasescope)
- [CKFetchRecordZoneChangesOperation](/documentation/cloudkit/ckfetchrecordzonechangesoperation)

#### Creating a Zone Change Operation

- [convenience init(recordZoneIDs: [CKRecordZone.ID]?, configurationsByRecordZoneID: [CKRecordZone.ID : CKFetchRecordZoneChangesOperation.ZoneConfiguration]?)](/documentation/cloudkit/ckfetchrecordzonechangesoperation/init(recordzoneids:configurationsbyrecordzoneid:))
- [init()](/documentation/cloudkit/ckfetchrecordzonechangesoperation/init())

#### Configuring the Zone Change Operation

- [var configurationsByRecordZoneID: [CKRecordZone.ID : CKFetchRecordZoneChangesOperation.ZoneConfiguration]?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/configurationsbyrecordzoneid)
- [CKFetchRecordZoneChangesOperation.ZoneConfiguration](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneconfiguration)

##### Creating a Zone Change Configuration

- [convenience init(previousServerChangeToken: CKServerChangeToken?, resultsLimit: Int?, desiredKeys: [CKRecord.FieldKey]?)](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneconfiguration/init(previousserverchangetoken:resultslimit:desiredkeys:))

##### Accessing a Zone Change Configuration

- [var previousServerChangeToken: CKServerChangeToken?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneconfiguration/previousserverchangetoken)
- [var resultsLimit: Int](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneconfiguration/resultslimit)
- [var desiredKeys: [CKRecord.FieldKey]?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneconfiguration/desiredkeys)
- [var fetchAllChanges: Bool](/documentation/cloudkit/ckfetchrecordzonechangesoperation/fetchallchanges)
- [var recordZoneIDs: [CKRecordZone.ID]?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/recordzoneids)

#### Processing the Zone Change Operation Results

- [var recordChangedBlock: ((CKRecord) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/recordchangedblock)
- [var recordWithIDWasDeletedBlock: ((CKRecord.ID, CKRecord.RecordType) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/recordwithidwasdeletedblock-3z14c)
- [var recordZoneChangeTokensUpdatedBlock: ((CKRecordZone.ID, CKServerChangeToken?, Data?) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/recordzonechangetokensupdatedblock)
- [var recordZoneFetchCompletionBlock: ((CKRecordZone.ID, CKServerChangeToken?, Data?, Bool, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/recordzonefetchcompletionblock)
- [var fetchRecordZoneChangesCompletionBlock: (((any Error)?) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/fetchrecordzonechangescompletionblock)

#### Deprecated

- [Deprecated Symbols](/documentation/cloudkit/ckfetchrecordzonechangesoperation-deprecated-symbols)

##### Deprecated Methods

- [convenience init(recordZoneIDs: [CKRecordZone.ID], optionsByRecordZoneID: [CKRecordZone.ID : CKFetchRecordZoneChangesOperation.ZoneOptions]?)](/documentation/cloudkit/ckfetchrecordzonechangesoperation/init(recordzoneids:optionsbyrecordzoneid:))
- [CKFetchRecordZoneChangesOperation.ZoneOptions](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneoptions)

###### Zone Change Options

- [var desiredKeys: [String]?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneoptions/desiredkeys)
- [var previousServerChangeToken: CKServerChangeToken?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneoptions/previousserverchangetoken)
- [var resultsLimit: Int](/documentation/cloudkit/ckfetchrecordzonechangesoperation/zoneoptions/resultslimit)

##### Deprecated Properties

- [var optionsByRecordZoneID: [CKRecordZone.ID : CKFetchRecordZoneChangesOperation.ZoneOptions]?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/optionsbyrecordzoneid)

#### Instance Properties

- [var fetchRecordZoneChangesResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/fetchrecordzonechangesresultblock)
- [var recordWasChangedBlock: ((CKRecord.ID, Result<CKRecord, any Error>) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/recordwaschangedblock-x5bw)
- [var recordZoneFetchResultBlock: ((CKRecordZone.ID, Result<(serverChangeToken: CKServerChangeToken, clientChangeTokenData: Data?, moreComing: Bool), any Error>) -> Void)?](/documentation/cloudkit/ckfetchrecordzonechangesoperation/recordzonefetchresultblock)

### Change Tokens

- [CKServerChangeToken](/documentation/cloudkit/ckserverchangetoken)

### Subscription Management

- [CKFetchSubscriptionsOperation](/documentation/cloudkit/ckfetchsubscriptionsoperation)

#### Creating a Fetch Subscriptions Operation

- [convenience init(subscriptionIDs: [CKSubscription.ID])](/documentation/cloudkit/ckfetchsubscriptionsoperation/init(subscriptionids:))
- [init()](/documentation/cloudkit/ckfetchsubscriptionsoperation/init())

#### Getting All Subscriptions

- [class func fetchAllSubscriptionsOperation() -> Self](/documentation/cloudkit/ckfetchsubscriptionsoperation/fetchallsubscriptionsoperation())

#### Configuring the Fetch Subscriptions Operation

- [var subscriptionIDs: [CKSubscription.ID]?](/documentation/cloudkit/ckfetchsubscriptionsoperation/subscriptionids-17f4q)

#### Processing the Fetch Subscription Results

- [var fetchSubscriptionCompletionBlock: (([CKSubscription.ID : CKSubscription]?, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchsubscriptionsoperation/fetchsubscriptioncompletionblock-6hhpi)

#### Instance Properties

- [var fetchSubscriptionsResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckfetchsubscriptionsoperation/fetchsubscriptionsresultblock)
- [var perSubscriptionResultBlock: ((CKSubscription.ID, Result<CKSubscription, any Error>) -> Void)?](/documentation/cloudkit/ckfetchsubscriptionsoperation/persubscriptionresultblock)
- [CKModifySubscriptionsOperation](/documentation/cloudkit/ckmodifysubscriptionsoperation)

#### Creating a Modify Subscriptions Operation

- [convenience init(subscriptionsToSave: [CKSubscription]?, subscriptionIDsToDelete: [CKSubscription.ID]?)](/documentation/cloudkit/ckmodifysubscriptionsoperation/init(subscriptionstosave:subscriptionidstodelete:))
- [init()](/documentation/cloudkit/ckmodifysubscriptionsoperation/init())

#### Configuring the Modify Subscriptions Operation

- [var subscriptionsToSave: [CKSubscription]?](/documentation/cloudkit/ckmodifysubscriptionsoperation/subscriptionstosave)
- [var subscriptionIDsToDelete: [CKSubscription.ID]?](/documentation/cloudkit/ckmodifysubscriptionsoperation/subscriptionidstodelete-3534e)

#### Processing the Modify Subscription Results

- [var modifySubscriptionsCompletionBlock: (([CKSubscription]?, [CKSubscription.ID]?, (any Error)?) -> Void)?](/documentation/cloudkit/ckmodifysubscriptionsoperation/modifysubscriptionscompletionblock-7l56)

#### Instance Properties

- [var modifySubscriptionsResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckmodifysubscriptionsoperation/modifysubscriptionsresultblock)
- [var perSubscriptionDeleteBlock: ((CKSubscription.ID, Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckmodifysubscriptionsoperation/persubscriptiondeleteblock-5ke2l)
- [var perSubscriptionSaveBlock: ((CKSubscription.ID, Result<CKSubscription, any Error>) -> Void)?](/documentation/cloudkit/ckmodifysubscriptionsoperation/persubscriptionsaveblock-8y9zn)

### Predicate-Driven Changes

- [CKQuerySubscription](/documentation/cloudkit/ckquerysubscription)

#### Creating a Subscription

- [convenience init(recordType: CKRecord.RecordType, predicate: NSPredicate, subscriptionID: CKSubscription.ID, options: CKQuerySubscription.Options)](/documentation/cloudkit/ckquerysubscription/init(recordtype:predicate:subscriptionid:options:))
- [init(coder: NSCoder)](/documentation/cloudkit/ckquerysubscription/init(coder:))

#### Accessing the Subscription Search Parameters

- [var predicate: NSPredicate](/documentation/cloudkit/ckquerysubscription/predicate)
- [var querySubscriptionOptions: CKQuerySubscription.Options](/documentation/cloudkit/ckquerysubscription/querysubscriptionoptions)
- [CKQuerySubscription.Options](/documentation/cloudkit/ckquerysubscription/options)

##### Creating Query Subscription Options

- [init(rawValue: UInt)](/documentation/cloudkit/ckquerysubscription/options/init(rawvalue:))

##### Accessing Subscription Options

- [static var firesOnRecordCreation: CKQuerySubscription.Options](/documentation/cloudkit/ckquerysubscription/options/firesonrecordcreation)
- [static var firesOnRecordDeletion: CKQuerySubscription.Options](/documentation/cloudkit/ckquerysubscription/options/firesonrecorddeletion)
- [static var firesOnRecordUpdate: CKQuerySubscription.Options](/documentation/cloudkit/ckquerysubscription/options/firesonrecordupdate)
- [static var firesOnce: CKQuerySubscription.Options](/documentation/cloudkit/ckquerysubscription/options/firesonce)

#### Accessing the Subscription Metadata

- [var recordType: CKRecord.RecordType?](/documentation/cloudkit/ckquerysubscription/recordtype-4qgdo)
- [var zoneID: CKRecordZone.ID?](/documentation/cloudkit/ckquerysubscription/zoneid)

#### Initializers

- [convenience init(recordType: CKRecord.RecordType, predicate: NSPredicate, options: CKQuerySubscription.Options)](/documentation/cloudkit/ckquerysubscription/init(recordtype:predicate:options:))
- [CKQueryNotification](/documentation/cloudkit/ckquerynotification)

#### Getting the Database Scope

- [var databaseScope: CKDatabase.Scope](/documentation/cloudkit/ckquerynotification/databasescope)

#### Getting the Notification Attributes

- [var queryNotificationReason: CKQueryNotification.Reason](/documentation/cloudkit/ckquerynotification/querynotificationreason)
- [CKQueryNotification.Reason](/documentation/cloudkit/ckquerynotification/reason)

##### Constants

- [case recordCreated](/documentation/cloudkit/ckquerynotification/reason/recordcreated)
- [case recordUpdated](/documentation/cloudkit/ckquerynotification/reason/recordupdated)
- [case recordDeleted](/documentation/cloudkit/ckquerynotification/reason/recorddeleted)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckquerynotification/reason/init(rawvalue:))

#### Getting the Record Information

- [var recordID: CKRecord.ID?](/documentation/cloudkit/ckquerynotification/recordid)
- [var recordFields: [String : Any]?](/documentation/cloudkit/ckquerynotification/recordfields)

### Base Objects

- [CKSubscription](/documentation/cloudkit/cksubscription)

#### Specifying the Push Notification Data

- [var notificationInfo: CKSubscription.NotificationInfo?](/documentation/cloudkit/cksubscription/notificationinfo-swift.property)
- [CKSubscription.NotificationInfo](/documentation/cloudkit/cksubscription/notificationinfo-swift.class)

##### Creating Notification Information

- [convenience init(alertBody: String?, alertLocalizationKey: String?, alertLocalizationArgs: [CKRecord.FieldKey], title: String?, titleLocalizationKey: String?, titleLocalizationArgs: [CKRecord.FieldKey], subtitle: String?, subtitleLocalizationKey: String?, subtitleLocalizationArgs: [CKRecord.FieldKey], alertActionLocalizationKey: String?, alertLaunchImage: String?, soundName: String?, desiredKeys: [CKRecord.FieldKey], shouldBadge: Bool, shouldSendContentAvailable: Bool, shouldSendMutableContent: Bool, category: String?, collapseIDKey: String?)](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/init(alertbody:alertlocalizationkey:alertlocalizationargs:title:titlelocalizationkey:titlelocalizationargs:subtitle:subtitlelocalizationkey:subtitlelocalizationargs:alertactionlocalizationkey:alertlaunchimage:soundname:desiredkeys:shouldbad-47rj5)

##### Grouping Notifications

- [var category: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/category)
- [var collapseIDKey: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/collapseidkey)

##### Displaying Badges

- [var shouldBadge: Bool](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/shouldbadge)

##### Accessing the Notification Alert

- [var alertBody: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/alertbody)
- [var alertLocalizationKey: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/alertlocalizationkey)
- [var alertLocalizationArgs: [CKRecord.FieldKey]?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/alertlocalizationargs)
- [var alertActionLocalizationKey: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/alertactionlocalizationkey)
- [var alertLaunchImage: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/alertlaunchimage)
- [var soundName: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/soundname)

##### Accessing the Notification Info

- [var shouldSendContentAvailable: Bool](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/shouldsendcontentavailable)
- [var shouldSendMutableContent: Bool](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/shouldsendmutablecontent)

##### Accessing the Record’s Data

- [var desiredKeys: [CKRecord.FieldKey]?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/desiredkeys)

##### Accessing the Notification Title

- [var title: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/title)
- [var titleLocalizationKey: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/titlelocalizationkey)
- [var titleLocalizationArgs: [CKRecord.FieldKey]?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/titlelocalizationargs)

##### Accessing the Notification Subtitle

- [var subtitle: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/subtitle)
- [var subtitleLocalizationKey: String?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/subtitlelocalizationkey)
- [var subtitleLocalizationArgs: [CKRecord.FieldKey]?](/documentation/cloudkit/cksubscription/notificationinfo-swift.class/subtitlelocalizationargs)

#### Accessing the Subscription Metadata

- [var subscriptionID: CKSubscription.ID](/documentation/cloudkit/cksubscription/subscriptionid-6fp3j)
- [CKSubscription.ID](/documentation/cloudkit/cksubscription/id)
- [var subscriptionType: CKSubscription.SubscriptionType](/documentation/cloudkit/cksubscription/subscriptiontype-swift.property)
- [CKSubscription.SubscriptionType](/documentation/cloudkit/cksubscription/subscriptiontype-swift.enum)

##### Subscription Types

- [case query](/documentation/cloudkit/cksubscription/subscriptiontype-swift.enum/query)
- [case database](/documentation/cloudkit/cksubscription/subscriptiontype-swift.enum/database)
- [case recordZone](/documentation/cloudkit/cksubscription/subscriptiontype-swift.enum/recordzone)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksubscription/subscriptiontype-swift.enum/init(rawvalue:))
- [CKNotification](/documentation/cloudkit/cknotification)

#### Creating a Notification

- [convenience init?(fromRemoteNotificationDictionary: [AnyHashable : Any])](/documentation/cloudkit/cknotification/init(fromremotenotificationdictionary:))

#### Identifying the Notification

- [var notificationID: CKNotification.ID?](/documentation/cloudkit/cknotification/notificationid)
- [CKNotification.ID](/documentation/cloudkit/cknotification/id)
- [var notificationType: CKNotification.NotificationType](/documentation/cloudkit/cknotification/notificationtype-swift.property)
- [CKNotification.NotificationType](/documentation/cloudkit/cknotification/notificationtype-swift.enum)

##### Notification Types

- [case query](/documentation/cloudkit/cknotification/notificationtype-swift.enum/query)
- [case database](/documentation/cloudkit/cknotification/notificationtype-swift.enum/database)
- [case recordZone](/documentation/cloudkit/cknotification/notificationtype-swift.enum/recordzone)
- [case readNotification](/documentation/cloudkit/cknotification/notificationtype-swift.enum/readnotification)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cknotification/notificationtype-swift.enum/init(rawvalue:))
- [var containerIdentifier: String?](/documentation/cloudkit/cknotification/containeridentifier)

#### Getting the Notification’s Status

- [var isPruned: Bool](/documentation/cloudkit/cknotification/ispruned)

#### Accessing the Notification Info

- [var alertBody: String?](/documentation/cloudkit/cknotification/alertbody)
- [var alertLocalizationKey: String?](/documentation/cloudkit/cknotification/alertlocalizationkey)
- [var alertLocalizationArgs: [String]?](/documentation/cloudkit/cknotification/alertlocalizationargs)
- [var alertActionLocalizationKey: String?](/documentation/cloudkit/cknotification/alertactionlocalizationkey)
- [var alertLaunchImage: String?](/documentation/cloudkit/cknotification/alertlaunchimage)
- [var soundName: String?](/documentation/cloudkit/cknotification/soundname)
- [var badge: NSNumber?](/documentation/cloudkit/cknotification/badge)
- [var category: String?](/documentation/cloudkit/cknotification/category)
- [var subscriptionID: CKSubscription.ID?](/documentation/cloudkit/cknotification/subscriptionid-16ygj)
- [var subscriptionOwnerUserRecordID: CKRecord.ID?](/documentation/cloudkit/cknotification/subscriptionowneruserrecordid)
- [var title: String?](/documentation/cloudkit/cknotification/title)
- [var titleLocalizationKey: String?](/documentation/cloudkit/cknotification/titlelocalizationkey)
- [var titleLocalizationArgs: [String]?](/documentation/cloudkit/cknotification/titlelocalizationargs)
- [var subtitle: String?](/documentation/cloudkit/cknotification/subtitle)
- [var subtitleLocalizationKey: String?](/documentation/cloudkit/cknotification/subtitlelocalizationkey)
- [var subtitleLocalizationArgs: [String]?](/documentation/cloudkit/cknotification/subtitlelocalizationargs)
- [CKDatabaseOperation](/documentation/cloudkit/ckdatabaseoperation)

#### Accessing the Database

- [var database: CKDatabase?](/documentation/cloudkit/ckdatabaseoperation/database)
- [CKSyncEngine](/documentation/cloudkit/cksyncengine-5sie5)

### Creating a sync engine

- [init(CKSyncEngine.Configuration)](/documentation/cloudkit/cksyncengine-5sie5/init(_:))
- [CKSyncEngine.Configuration](/documentation/cloudkit/cksyncengine-5sie5/configuration)

#### Creating configurations

- [init(database: CKDatabase, stateSerialization: CKSyncEngine.State.Serialization?, delegate: any CKSyncEngineDelegate)](/documentation/cloudkit/cksyncengine-5sie5/configuration/init(database:stateserialization:delegate:))

#### Handling record changes

- [var delegate: any CKSyncEngineDelegate](/documentation/cloudkit/cksyncengine-5sie5/configuration/delegate)
- [CKSyncEngineDelegate](/documentation/cloudkit/cksyncenginedelegate-1q7g8)

##### Handling sync events

- [func handleEvent(CKSyncEngine.Event, syncEngine: CKSyncEngine) async](/documentation/cloudkit/cksyncenginedelegate-1q7g8/handleevent(_:syncengine:))
- [CKSyncEngine.Event](/documentation/cloudkit/cksyncengine-5sie5/event)

###### Account changes

- [case accountChange(CKSyncEngine.Event.AccountChange)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange(_:))
- [CKSyncEngine.Event.AccountChange](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange)

###### Understanding the change

- [let changeType: CKSyncEngine.Event.AccountChange.ChangeType](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.property)
- [CKSyncEngine.Event.AccountChange.ChangeType](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum)

###### Account change types

- [case signIn(currentUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/signin(currentuser:))
- [case signOut(previousUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/signout(previoususer:))
- [case switchAccounts(previousUser: CKRecord.ID, currentUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/switchaccounts(previoususer:currentuser:))
- [CKSyncEngineAccountChangeType](/documentation/cloudkit/cksyncengineaccountchangetype)

###### Account change types

- [case signIn](/documentation/cloudkit/cksyncengineaccountchangetype/signin)
- [case signOut](/documentation/cloudkit/cksyncengineaccountchangetype/signout)
- [case switchAccounts](/documentation/cloudkit/cksyncengineaccountchangetype/switchaccounts)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncengineaccountchangetype/init(rawvalue:))

###### Remote database changes

- [case willFetchChanges(CKSyncEngine.Event.WillFetchChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges(_:))
- [CKSyncEngine.Event.WillFetchChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges)

###### Instance Properties

- [let context: CKSyncEngine.FetchChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges/context)
- [case fetchedDatabaseChanges(CKSyncEngine.Event.FetchedDatabaseChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges(_:))
- [CKSyncEngine.Event.FetchedDatabaseChanges](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges)

###### Accessing changes

- [let deletions: [CKDatabase.DatabaseChange.Deletion]](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges/deletions)
- [CKSyncEngineZoneDeletionReason](/documentation/cloudkit/cksyncenginezonedeletionreason)

###### Deletion reasons

- [case deleted](/documentation/cloudkit/cksyncenginezonedeletionreason/deleted)
- [case encryptedDataReset](/documentation/cloudkit/cksyncenginezonedeletionreason/encrypteddatareset)
- [case purged](/documentation/cloudkit/cksyncenginezonedeletionreason/purged)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginezonedeletionreason/init(rawvalue:))
- [let modifications: [CKDatabase.DatabaseChange.Modification]](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges/modifications)
- [case didFetchChanges(CKSyncEngine.Event.DidFetchChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges(_:))
- [CKSyncEngine.Event.DidFetchChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges)

###### Instance Properties

- [let context: CKSyncEngine.FetchChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges/context)

###### Remote record zone changes

- [case willFetchRecordZoneChanges(CKSyncEngine.Event.WillFetchRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges(_:))
- [CKSyncEngine.Event.WillFetchRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges)

###### Identifying the record zone

- [let zoneID: CKRecordZone.ID](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges/zoneid)
- [case fetchedRecordZoneChanges(CKSyncEngine.Event.FetchedRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges(_:))
- [CKSyncEngine.Event.FetchedRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges)

###### Accessing changes

- [let deletions: [CKDatabase.RecordZoneChange.Deletion]](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges/deletions)
- [let modifications: [CKDatabase.RecordZoneChange.Modification]](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges/modifications)
- [case didFetchRecordZoneChanges(CKSyncEngine.Event.DidFetchRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges(_:))
- [CKSyncEngine.Event.DidFetchRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges)

###### Identifying the record zone

- [let zoneID: CKRecordZone.ID](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges/zoneid)

###### Handling errors

- [let error: CKError?](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges/error)

###### Pending local changes

- [case willSendChanges(CKSyncEngine.Event.WillSendChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges(_:))
- [CKSyncEngine.Event.WillSendChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges)

###### Accessing the context

- [let context: CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges/context)
- [case sentDatabaseChanges(CKSyncEngine.Event.SentDatabaseChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges(_:))
- [CKSyncEngine.Event.SentDatabaseChanges](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges)

###### Accessing successful changes

- [let deletedZoneIDs: [CKRecordZone.ID]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/deletedzoneids)
- [let savedZones: [CKRecordZone]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/savedzones)

###### Accessing failed changes

- [let failedZoneDeletes: [CKRecordZone.ID : CKError]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonedeletes)
- [let failedZoneSaves: [CKSyncEngine.Event.SentDatabaseChanges.FailedZoneSave]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesaves)
- [CKSyncEngine.Event.SentDatabaseChanges.FailedZoneSave](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave)

###### Accessing the record zone

- [let zone: CKRecordZone](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave/zone)

###### Accessing the error

- [let error: CKError](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave/error)
- [case sentRecordZoneChanges(CKSyncEngine.Event.SentRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges(_:))
- [CKSyncEngine.Event.SentRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges)

###### Accessing successful changes

- [let deletedRecordIDs: [CKRecord.ID]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/deletedrecordids)
- [let savedRecords: [CKRecord]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/savedrecords)

###### Accessing failed changes

- [let failedRecordDeletes: [CKRecord.ID : CKError]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecorddeletes)
- [let failedRecordSaves: [CKSyncEngine.Event.SentRecordZoneChanges.FailedRecordSave]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsaves)
- [CKSyncEngine.Event.SentRecordZoneChanges.FailedRecordSave](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave)

###### Accessing the record

- [let record: CKRecord](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave/record)

###### Accessing the error

- [let error: CKError](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave/error)
- [case didSendChanges(CKSyncEngine.Event.DidSendChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges(_:))
- [CKSyncEngine.Event.DidSendChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges)

###### Accessing the context

- [let context: CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges/context)

###### State updates

- [case stateUpdate(CKSyncEngine.Event.StateUpdate)](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate(_:))
- [CKSyncEngine.Event.StateUpdate](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate)

###### Accessing the state

- [let stateSerialization: CKSyncEngine.State.Serialization](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate/stateserialization)
- [CKSyncEngineEventType](/documentation/cloudkit/cksyncengineeventtype)

###### Event types

- [case stateUpdate](/documentation/cloudkit/cksyncengineeventtype/stateupdate)
- [case accountChange](/documentation/cloudkit/cksyncengineeventtype/accountchange)
- [case fetchedDatabaseChanges](/documentation/cloudkit/cksyncengineeventtype/fetcheddatabasechanges)
- [case fetchedRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/fetchedrecordzonechanges)
- [case sentDatabaseChanges](/documentation/cloudkit/cksyncengineeventtype/sentdatabasechanges)
- [case sentRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/sentrecordzonechanges)
- [case willFetchChanges](/documentation/cloudkit/cksyncengineeventtype/willfetchchanges)
- [case willFetchRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/willfetchrecordzonechanges)
- [case didFetchRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/didfetchrecordzonechanges)
- [case didFetchChanges](/documentation/cloudkit/cksyncengineeventtype/didfetchchanges)
- [case willSendChanges](/documentation/cloudkit/cksyncengineeventtype/willsendchanges)
- [case didSendChanges](/documentation/cloudkit/cksyncengineeventtype/didsendchanges)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncengineeventtype/init(rawvalue:))

##### Sending changes

- [func nextRecordZoneChangeBatch(CKSyncEngine.SendChangesContext, syncEngine: CKSyncEngine) async -> CKSyncEngine.RecordZoneChangeBatch?](/documentation/cloudkit/cksyncenginedelegate-1q7g8/nextrecordzonechangebatch(_:syncengine:))
- [CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext)

###### Accessing specific attributes

- [let reason: CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext/reason)
- [CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/syncreason)

###### Sync reasons

- [case scheduled](/documentation/cloudkit/cksyncengine-5sie5/syncreason/scheduled)
- [case manual](/documentation/cloudkit/cksyncengine-5sie5/syncreason/manual)
- [CKSyncEngineSyncReason](/documentation/cloudkit/cksyncenginesyncreason)

###### Sync reasons

- [case scheduled](/documentation/cloudkit/cksyncenginesyncreason/scheduled)
- [case manual](/documentation/cloudkit/cksyncenginesyncreason/manual)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginesyncreason/init(rawvalue:))
- [let options: CKSyncEngine.SendChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext/options)
- [CKSyncEngine.SendChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions)

###### Managing attributes

- [var operationGroup: CKOperationGroup](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/operationgroup)

###### Initializers

- [init(scope: CKSyncEngine.SendChangesOptions.Scope, operationGroup: CKOperationGroup?)](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/init(scope:operationgroup:))

###### Instance Properties

- [var scope: CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.property)

###### Enumerations

- [CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum)

###### Enumeration Cases

- [case all](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/all)
- [case allExcluding([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/allexcluding(_:))
- [case recordIDs([CKRecord.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/recordids(_:))
- [case zoneIDs([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/zoneids(_:))

###### Instance Methods

- [func contains(CKRecord.ID) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-59hve)
- [func contains(CKSyncEngine.PendingRecordZoneChange) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-8qiyf)
- [CKSyncEngine.RecordZoneChangeBatch](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch)

###### Creating a batch

- [init?(pendingChanges: [CKSyncEngine.PendingRecordZoneChange], recordProvider: (CKRecord.ID) async -> CKRecord?) async](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/init(pendingchanges:recordprovider:))
- [CKSyncEngine.PendingRecordZoneChange](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange)

###### Record change types

- [CKSyncEnginePendingRecordZoneChangeType](/documentation/cloudkit/cksyncenginependingrecordzonechangetype)

###### Enumeration Cases

- [case deleteRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/deleterecord)
- [case saveRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/saverecord)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/init(rawvalue:))

###### Enumeration Cases

- [case deleteRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/deleterecord(_:))
- [case saveRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/saverecord(_:))
- [init(recordsToSave: [CKRecord], recordIDsToDelete: [CKRecord.ID], atomicByZone: Bool)](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/init(recordstosave:recordidstodelete:atomicbyzone:))

###### Managing atomicity

- [var atomicByZone: Bool](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/atomicbyzone)

###### Managing the records

- [var recordIDsToDelete: [CKRecord.ID]](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/recordidstodelete)
- [var recordsToSave: [CKRecord]](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/recordstosave)

##### Instance Methods

- [func nextFetchChangesOptions(CKSyncEngine.FetchChangesContext, syncEngine: CKSyncEngine) async -> CKSyncEngine.FetchChangesOptions](/documentation/cloudkit/cksyncenginedelegate-1q7g8/nextfetchchangesoptions(_:syncengine:))

#### Managing attributes

- [var automaticallySync: Bool](/documentation/cloudkit/cksyncengine-5sie5/configuration/automaticallysync)
- [var database: CKDatabase](/documentation/cloudkit/cksyncengine-5sie5/configuration/database)
- [var subscriptionID: CKSubscription.ID?](/documentation/cloudkit/cksyncengine-5sie5/configuration/subscriptionid)
- [var stateSerialization: CKSyncEngine.State.Serialization?](/documentation/cloudkit/cksyncengine-5sie5/configuration/stateserialization)

### Accessing the engine’s attributes

- [var database: CKDatabase](/documentation/cloudkit/cksyncengine-5sie5/database)
- [var state: CKSyncEngine.State](/documentation/cloudkit/cksyncengine-5sie5/state-swift.property)
- [CKSyncEngine.State](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class)

#### Accessing pending changes

- [var hasPendingUntrackedChanges: Bool](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/haspendinguntrackedchanges)
- [var pendingDatabaseChanges: [CKSyncEngine.PendingDatabaseChange]](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/pendingdatabasechanges)
- [var pendingRecordZoneChanges: [CKSyncEngine.PendingRecordZoneChange]](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/pendingrecordzonechanges)

#### Manipulating pending changes

- [func add(pendingDatabaseChanges: [CKSyncEngine.PendingDatabaseChange])](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/add(pendingdatabasechanges:))
- [func remove(pendingDatabaseChanges: [CKSyncEngine.PendingDatabaseChange])](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/remove(pendingdatabasechanges:))
- [CKSyncEngine.PendingDatabaseChange](/documentation/cloudkit/cksyncengine-5sie5/pendingdatabasechange)

##### Database change types

- [CKSyncEnginePendingDatabaseChangeType](/documentation/cloudkit/cksyncenginependingdatabasechangetype)

###### Enumeration Cases

- [case deleteZone](/documentation/cloudkit/cksyncenginependingdatabasechangetype/deletezone)
- [case saveZone](/documentation/cloudkit/cksyncenginependingdatabasechangetype/savezone)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginependingdatabasechangetype/init(rawvalue:))

##### Enumeration Cases

- [case deleteZone(CKRecordZone.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingdatabasechange/deletezone(_:))
- [case saveZone(CKRecordZone)](/documentation/cloudkit/cksyncengine-5sie5/pendingdatabasechange/savezone(_:))
- [func add(pendingRecordZoneChanges: [CKSyncEngine.PendingRecordZoneChange])](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/add(pendingrecordzonechanges:))
- [func remove(pendingRecordZoneChanges: [CKSyncEngine.PendingRecordZoneChange])](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/remove(pendingrecordzonechanges:))
- [CKSyncEngine.PendingRecordZoneChange](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange)

##### Record change types

- [CKSyncEnginePendingRecordZoneChangeType](/documentation/cloudkit/cksyncenginependingrecordzonechangetype)

###### Enumeration Cases

- [case deleteRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/deleterecord)
- [case saveRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/saverecord)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/init(rawvalue:))

##### Enumeration Cases

- [case deleteRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/deleterecord(_:))
- [case saveRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/saverecord(_:))

#### Serializing state

- [CKSyncEngine.State.Serialization](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/serialization)

#### Instance Properties

- [var zoneIDsWithUnfetchedServerChanges: [CKRecordZone.ID]](/documentation/cloudkit/cksyncengine-5sie5/state-swift.class/zoneidswithunfetchedserverchanges)

### Participating in scheduled sync operations

- [CKSyncEngineDelegate](/documentation/cloudkit/cksyncenginedelegate-1q7g8)

#### Handling sync events

- [func handleEvent(CKSyncEngine.Event, syncEngine: CKSyncEngine) async](/documentation/cloudkit/cksyncenginedelegate-1q7g8/handleevent(_:syncengine:))
- [CKSyncEngine.Event](/documentation/cloudkit/cksyncengine-5sie5/event)

##### Account changes

- [case accountChange(CKSyncEngine.Event.AccountChange)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange(_:))
- [CKSyncEngine.Event.AccountChange](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange)

###### Understanding the change

- [let changeType: CKSyncEngine.Event.AccountChange.ChangeType](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.property)
- [CKSyncEngine.Event.AccountChange.ChangeType](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum)

###### Account change types

- [case signIn(currentUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/signin(currentuser:))
- [case signOut(previousUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/signout(previoususer:))
- [case switchAccounts(previousUser: CKRecord.ID, currentUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/switchaccounts(previoususer:currentuser:))
- [CKSyncEngineAccountChangeType](/documentation/cloudkit/cksyncengineaccountchangetype)

###### Account change types

- [case signIn](/documentation/cloudkit/cksyncengineaccountchangetype/signin)
- [case signOut](/documentation/cloudkit/cksyncengineaccountchangetype/signout)
- [case switchAccounts](/documentation/cloudkit/cksyncengineaccountchangetype/switchaccounts)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncengineaccountchangetype/init(rawvalue:))

##### Remote database changes

- [case willFetchChanges(CKSyncEngine.Event.WillFetchChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges(_:))
- [CKSyncEngine.Event.WillFetchChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges)

###### Instance Properties

- [let context: CKSyncEngine.FetchChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges/context)
- [case fetchedDatabaseChanges(CKSyncEngine.Event.FetchedDatabaseChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges(_:))
- [CKSyncEngine.Event.FetchedDatabaseChanges](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges)

###### Accessing changes

- [let deletions: [CKDatabase.DatabaseChange.Deletion]](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges/deletions)
- [CKSyncEngineZoneDeletionReason](/documentation/cloudkit/cksyncenginezonedeletionreason)

###### Deletion reasons

- [case deleted](/documentation/cloudkit/cksyncenginezonedeletionreason/deleted)
- [case encryptedDataReset](/documentation/cloudkit/cksyncenginezonedeletionreason/encrypteddatareset)
- [case purged](/documentation/cloudkit/cksyncenginezonedeletionreason/purged)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginezonedeletionreason/init(rawvalue:))
- [let modifications: [CKDatabase.DatabaseChange.Modification]](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges/modifications)
- [case didFetchChanges(CKSyncEngine.Event.DidFetchChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges(_:))
- [CKSyncEngine.Event.DidFetchChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges)

###### Instance Properties

- [let context: CKSyncEngine.FetchChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges/context)

##### Remote record zone changes

- [case willFetchRecordZoneChanges(CKSyncEngine.Event.WillFetchRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges(_:))
- [CKSyncEngine.Event.WillFetchRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges)

###### Identifying the record zone

- [let zoneID: CKRecordZone.ID](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges/zoneid)
- [case fetchedRecordZoneChanges(CKSyncEngine.Event.FetchedRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges(_:))
- [CKSyncEngine.Event.FetchedRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges)

###### Accessing changes

- [let deletions: [CKDatabase.RecordZoneChange.Deletion]](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges/deletions)
- [let modifications: [CKDatabase.RecordZoneChange.Modification]](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges/modifications)
- [case didFetchRecordZoneChanges(CKSyncEngine.Event.DidFetchRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges(_:))
- [CKSyncEngine.Event.DidFetchRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges)

###### Identifying the record zone

- [let zoneID: CKRecordZone.ID](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges/zoneid)

###### Handling errors

- [let error: CKError?](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges/error)

##### Pending local changes

- [case willSendChanges(CKSyncEngine.Event.WillSendChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges(_:))
- [CKSyncEngine.Event.WillSendChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges)

###### Accessing the context

- [let context: CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges/context)
- [case sentDatabaseChanges(CKSyncEngine.Event.SentDatabaseChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges(_:))
- [CKSyncEngine.Event.SentDatabaseChanges](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges)

###### Accessing successful changes

- [let deletedZoneIDs: [CKRecordZone.ID]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/deletedzoneids)
- [let savedZones: [CKRecordZone]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/savedzones)

###### Accessing failed changes

- [let failedZoneDeletes: [CKRecordZone.ID : CKError]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonedeletes)
- [let failedZoneSaves: [CKSyncEngine.Event.SentDatabaseChanges.FailedZoneSave]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesaves)
- [CKSyncEngine.Event.SentDatabaseChanges.FailedZoneSave](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave)

###### Accessing the record zone

- [let zone: CKRecordZone](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave/zone)

###### Accessing the error

- [let error: CKError](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave/error)
- [case sentRecordZoneChanges(CKSyncEngine.Event.SentRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges(_:))
- [CKSyncEngine.Event.SentRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges)

###### Accessing successful changes

- [let deletedRecordIDs: [CKRecord.ID]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/deletedrecordids)
- [let savedRecords: [CKRecord]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/savedrecords)

###### Accessing failed changes

- [let failedRecordDeletes: [CKRecord.ID : CKError]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecorddeletes)
- [let failedRecordSaves: [CKSyncEngine.Event.SentRecordZoneChanges.FailedRecordSave]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsaves)
- [CKSyncEngine.Event.SentRecordZoneChanges.FailedRecordSave](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave)

###### Accessing the record

- [let record: CKRecord](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave/record)

###### Accessing the error

- [let error: CKError](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave/error)
- [case didSendChanges(CKSyncEngine.Event.DidSendChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges(_:))
- [CKSyncEngine.Event.DidSendChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges)

###### Accessing the context

- [let context: CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges/context)

##### State updates

- [case stateUpdate(CKSyncEngine.Event.StateUpdate)](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate(_:))
- [CKSyncEngine.Event.StateUpdate](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate)

###### Accessing the state

- [let stateSerialization: CKSyncEngine.State.Serialization](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate/stateserialization)
- [CKSyncEngineEventType](/documentation/cloudkit/cksyncengineeventtype)

##### Event types

- [case stateUpdate](/documentation/cloudkit/cksyncengineeventtype/stateupdate)
- [case accountChange](/documentation/cloudkit/cksyncengineeventtype/accountchange)
- [case fetchedDatabaseChanges](/documentation/cloudkit/cksyncengineeventtype/fetcheddatabasechanges)
- [case fetchedRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/fetchedrecordzonechanges)
- [case sentDatabaseChanges](/documentation/cloudkit/cksyncengineeventtype/sentdatabasechanges)
- [case sentRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/sentrecordzonechanges)
- [case willFetchChanges](/documentation/cloudkit/cksyncengineeventtype/willfetchchanges)
- [case willFetchRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/willfetchrecordzonechanges)
- [case didFetchRecordZoneChanges](/documentation/cloudkit/cksyncengineeventtype/didfetchrecordzonechanges)
- [case didFetchChanges](/documentation/cloudkit/cksyncengineeventtype/didfetchchanges)
- [case willSendChanges](/documentation/cloudkit/cksyncengineeventtype/willsendchanges)
- [case didSendChanges](/documentation/cloudkit/cksyncengineeventtype/didsendchanges)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncengineeventtype/init(rawvalue:))

#### Sending changes

- [func nextRecordZoneChangeBatch(CKSyncEngine.SendChangesContext, syncEngine: CKSyncEngine) async -> CKSyncEngine.RecordZoneChangeBatch?](/documentation/cloudkit/cksyncenginedelegate-1q7g8/nextrecordzonechangebatch(_:syncengine:))
- [CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext)

##### Accessing specific attributes

- [let reason: CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext/reason)
- [CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/syncreason)

###### Sync reasons

- [case scheduled](/documentation/cloudkit/cksyncengine-5sie5/syncreason/scheduled)
- [case manual](/documentation/cloudkit/cksyncengine-5sie5/syncreason/manual)
- [CKSyncEngineSyncReason](/documentation/cloudkit/cksyncenginesyncreason)

###### Sync reasons

- [case scheduled](/documentation/cloudkit/cksyncenginesyncreason/scheduled)
- [case manual](/documentation/cloudkit/cksyncenginesyncreason/manual)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginesyncreason/init(rawvalue:))
- [let options: CKSyncEngine.SendChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext/options)
- [CKSyncEngine.SendChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions)

###### Managing attributes

- [var operationGroup: CKOperationGroup](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/operationgroup)

###### Initializers

- [init(scope: CKSyncEngine.SendChangesOptions.Scope, operationGroup: CKOperationGroup?)](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/init(scope:operationgroup:))

###### Instance Properties

- [var scope: CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.property)

###### Enumerations

- [CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum)

###### Enumeration Cases

- [case all](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/all)
- [case allExcluding([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/allexcluding(_:))
- [case recordIDs([CKRecord.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/recordids(_:))
- [case zoneIDs([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/zoneids(_:))

###### Instance Methods

- [func contains(CKRecord.ID) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-59hve)
- [func contains(CKSyncEngine.PendingRecordZoneChange) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-8qiyf)
- [CKSyncEngine.RecordZoneChangeBatch](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch)

##### Creating a batch

- [init?(pendingChanges: [CKSyncEngine.PendingRecordZoneChange], recordProvider: (CKRecord.ID) async -> CKRecord?) async](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/init(pendingchanges:recordprovider:))
- [CKSyncEngine.PendingRecordZoneChange](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange)

###### Record change types

- [CKSyncEnginePendingRecordZoneChangeType](/documentation/cloudkit/cksyncenginependingrecordzonechangetype)

###### Enumeration Cases

- [case deleteRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/deleterecord)
- [case saveRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/saverecord)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/init(rawvalue:))

###### Enumeration Cases

- [case deleteRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/deleterecord(_:))
- [case saveRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/saverecord(_:))
- [init(recordsToSave: [CKRecord], recordIDsToDelete: [CKRecord.ID], atomicByZone: Bool)](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/init(recordstosave:recordidstodelete:atomicbyzone:))

##### Managing atomicity

- [var atomicByZone: Bool](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/atomicbyzone)

##### Managing the records

- [var recordIDsToDelete: [CKRecord.ID]](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/recordidstodelete)
- [var recordsToSave: [CKRecord]](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/recordstosave)

#### Instance Methods

- [func nextFetchChangesOptions(CKSyncEngine.FetchChangesContext, syncEngine: CKSyncEngine) async -> CKSyncEngine.FetchChangesOptions](/documentation/cloudkit/cksyncenginedelegate-1q7g8/nextfetchchangesoptions(_:syncengine:))

### Invoking manual sync operations

- [func fetchChanges(CKSyncEngine.FetchChangesOptions) async throws](/documentation/cloudkit/cksyncengine-5sie5/fetchchanges(_:))
- [CKSyncEngine.FetchChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions)

#### Managing attributes

- [var operationGroup: CKOperationGroup](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/operationgroup)

#### Initializers

- [init(scope: CKSyncEngine.FetchChangesOptions.Scope, operationGroup: CKOperationGroup?)](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/init(scope:operationgroup:))

#### Instance Properties

- [var prioritizedZoneIDs: [CKRecordZone.ID]](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/prioritizedzoneids)
- [var scope: CKSyncEngine.FetchChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/scope-swift.property)

#### Enumerations

- [CKSyncEngine.FetchChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/scope-swift.enum)

##### Enumeration Cases

- [case all](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/scope-swift.enum/all)
- [case allExcluding([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/scope-swift.enum/allexcluding(_:))
- [case zoneIDs([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/scope-swift.enum/zoneids(_:))

##### Instance Methods

- [func contains(CKRecordZone.ID) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/fetchchangesoptions/scope-swift.enum/contains(_:))
- [func sendChanges(CKSyncEngine.SendChangesOptions) async throws](/documentation/cloudkit/cksyncengine-5sie5/sendchanges(_:))
- [CKSyncEngine.SendChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions)

#### Managing attributes

- [var operationGroup: CKOperationGroup](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/operationgroup)

#### Initializers

- [init(scope: CKSyncEngine.SendChangesOptions.Scope, operationGroup: CKOperationGroup?)](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/init(scope:operationgroup:))

#### Instance Properties

- [var scope: CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.property)

#### Enumerations

- [CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum)

##### Enumeration Cases

- [case all](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/all)
- [case allExcluding([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/allexcluding(_:))
- [case recordIDs([CKRecord.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/recordids(_:))
- [case zoneIDs([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/zoneids(_:))

##### Instance Methods

- [func contains(CKRecord.ID) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-59hve)
- [func contains(CKSyncEngine.PendingRecordZoneChange) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-8qiyf)

### Canceling operations

- [func cancelOperations() async](/documentation/cloudkit/cksyncengine-5sie5/canceloperations())

### Structures

- [CKSyncEngine.FetchChangesContext](/documentation/cloudkit/cksyncengine-5sie5/fetchchangescontext)

#### Instance Properties

- [let options: CKSyncEngine.FetchChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/fetchchangescontext/options)
- [let reason: CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/fetchchangescontext/reason)
- [CKSyncEngine.RecordZoneChangeBatch](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch)

#### Creating a batch

- [init?(pendingChanges: [CKSyncEngine.PendingRecordZoneChange], recordProvider: (CKRecord.ID) async -> CKRecord?) async](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/init(pendingchanges:recordprovider:))
- [CKSyncEngine.PendingRecordZoneChange](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange)

##### Record change types

- [CKSyncEnginePendingRecordZoneChangeType](/documentation/cloudkit/cksyncenginependingrecordzonechangetype)

###### Enumeration Cases

- [case deleteRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/deleterecord)
- [case saveRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/saverecord)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/init(rawvalue:))

##### Enumeration Cases

- [case deleteRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/deleterecord(_:))
- [case saveRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/saverecord(_:))
- [init(recordsToSave: [CKRecord], recordIDsToDelete: [CKRecord.ID], atomicByZone: Bool)](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/init(recordstosave:recordidstodelete:atomicbyzone:))

#### Managing atomicity

- [var atomicByZone: Bool](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/atomicbyzone)

#### Managing the records

- [var recordIDsToDelete: [CKRecord.ID]](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/recordidstodelete)
- [var recordsToSave: [CKRecord]](/documentation/cloudkit/cksyncengine-5sie5/recordzonechangebatch/recordstosave)
- [CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext)

#### Accessing specific attributes

- [let reason: CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext/reason)
- [CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/syncreason)

##### Sync reasons

- [case scheduled](/documentation/cloudkit/cksyncengine-5sie5/syncreason/scheduled)
- [case manual](/documentation/cloudkit/cksyncengine-5sie5/syncreason/manual)
- [CKSyncEngineSyncReason](/documentation/cloudkit/cksyncenginesyncreason)

##### Sync reasons

- [case scheduled](/documentation/cloudkit/cksyncenginesyncreason/scheduled)
- [case manual](/documentation/cloudkit/cksyncenginesyncreason/manual)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginesyncreason/init(rawvalue:))
- [let options: CKSyncEngine.SendChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/sendchangescontext/options)
- [CKSyncEngine.SendChangesOptions](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions)

##### Managing attributes

- [var operationGroup: CKOperationGroup](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/operationgroup)

##### Initializers

- [init(scope: CKSyncEngine.SendChangesOptions.Scope, operationGroup: CKOperationGroup?)](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/init(scope:operationgroup:))

##### Instance Properties

- [var scope: CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.property)

##### Enumerations

- [CKSyncEngine.SendChangesOptions.Scope](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum)

###### Enumeration Cases

- [case all](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/all)
- [case allExcluding([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/allexcluding(_:))
- [case recordIDs([CKRecord.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/recordids(_:))
- [case zoneIDs([CKRecordZone.ID])](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/zoneids(_:))

###### Instance Methods

- [func contains(CKRecord.ID) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-59hve)
- [func contains(CKSyncEngine.PendingRecordZoneChange) -> Bool](/documentation/cloudkit/cksyncengine-5sie5/sendchangesoptions/scope-swift.enum/contains(_:)-8qiyf)

### Enumerations

- [CKSyncEngine.Event](/documentation/cloudkit/cksyncengine-5sie5/event)

#### Account changes

- [case accountChange(CKSyncEngine.Event.AccountChange)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange(_:))
- [CKSyncEngine.Event.AccountChange](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange)

##### Understanding the change

- [let changeType: CKSyncEngine.Event.AccountChange.ChangeType](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.property)
- [CKSyncEngine.Event.AccountChange.ChangeType](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum)

###### Account change types

- [case signIn(currentUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/signin(currentuser:))
- [case signOut(previousUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/signout(previoususer:))
- [case switchAccounts(previousUser: CKRecord.ID, currentUser: CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/event/accountchange/changetype-swift.enum/switchaccounts(previoususer:currentuser:))
- [CKSyncEngineAccountChangeType](/documentation/cloudkit/cksyncengineaccountchangetype)

###### Account change types

- [case signIn](/documentation/cloudkit/cksyncengineaccountchangetype/signin)
- [case signOut](/documentation/cloudkit/cksyncengineaccountchangetype/signout)
- [case switchAccounts](/documentation/cloudkit/cksyncengineaccountchangetype/switchaccounts)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncengineaccountchangetype/init(rawvalue:))

#### Remote database changes

- [case willFetchChanges(CKSyncEngine.Event.WillFetchChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges(_:))
- [CKSyncEngine.Event.WillFetchChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges)

##### Instance Properties

- [let context: CKSyncEngine.FetchChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchchanges/context)
- [case fetchedDatabaseChanges(CKSyncEngine.Event.FetchedDatabaseChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges(_:))
- [CKSyncEngine.Event.FetchedDatabaseChanges](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges)

##### Accessing changes

- [let deletions: [CKDatabase.DatabaseChange.Deletion]](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges/deletions)
- [CKSyncEngineZoneDeletionReason](/documentation/cloudkit/cksyncenginezonedeletionreason)

###### Deletion reasons

- [case deleted](/documentation/cloudkit/cksyncenginezonedeletionreason/deleted)
- [case encryptedDataReset](/documentation/cloudkit/cksyncenginezonedeletionreason/encrypteddatareset)
- [case purged](/documentation/cloudkit/cksyncenginezonedeletionreason/purged)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginezonedeletionreason/init(rawvalue:))
- [let modifications: [CKDatabase.DatabaseChange.Modification]](/documentation/cloudkit/cksyncengine-5sie5/event/fetcheddatabasechanges/modifications)
- [case didFetchChanges(CKSyncEngine.Event.DidFetchChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges(_:))
- [CKSyncEngine.Event.DidFetchChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges)

##### Instance Properties

- [let context: CKSyncEngine.FetchChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchchanges/context)

#### Remote record zone changes

- [case willFetchRecordZoneChanges(CKSyncEngine.Event.WillFetchRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges(_:))
- [CKSyncEngine.Event.WillFetchRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges)

##### Identifying the record zone

- [let zoneID: CKRecordZone.ID](/documentation/cloudkit/cksyncengine-5sie5/event/willfetchrecordzonechanges/zoneid)
- [case fetchedRecordZoneChanges(CKSyncEngine.Event.FetchedRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges(_:))
- [CKSyncEngine.Event.FetchedRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges)

##### Accessing changes

- [let deletions: [CKDatabase.RecordZoneChange.Deletion]](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges/deletions)
- [let modifications: [CKDatabase.RecordZoneChange.Modification]](/documentation/cloudkit/cksyncengine-5sie5/event/fetchedrecordzonechanges/modifications)
- [case didFetchRecordZoneChanges(CKSyncEngine.Event.DidFetchRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges(_:))
- [CKSyncEngine.Event.DidFetchRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges)

##### Identifying the record zone

- [let zoneID: CKRecordZone.ID](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges/zoneid)

##### Handling errors

- [let error: CKError?](/documentation/cloudkit/cksyncengine-5sie5/event/didfetchrecordzonechanges/error)

#### Pending local changes

- [case willSendChanges(CKSyncEngine.Event.WillSendChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges(_:))
- [CKSyncEngine.Event.WillSendChanges](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges)

##### Accessing the context

- [let context: CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/willsendchanges/context)
- [case sentDatabaseChanges(CKSyncEngine.Event.SentDatabaseChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges(_:))
- [CKSyncEngine.Event.SentDatabaseChanges](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges)

##### Accessing successful changes

- [let deletedZoneIDs: [CKRecordZone.ID]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/deletedzoneids)
- [let savedZones: [CKRecordZone]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/savedzones)

##### Accessing failed changes

- [let failedZoneDeletes: [CKRecordZone.ID : CKError]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonedeletes)
- [let failedZoneSaves: [CKSyncEngine.Event.SentDatabaseChanges.FailedZoneSave]](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesaves)
- [CKSyncEngine.Event.SentDatabaseChanges.FailedZoneSave](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave)

###### Accessing the record zone

- [let zone: CKRecordZone](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave/zone)

###### Accessing the error

- [let error: CKError](/documentation/cloudkit/cksyncengine-5sie5/event/sentdatabasechanges/failedzonesave/error)
- [case sentRecordZoneChanges(CKSyncEngine.Event.SentRecordZoneChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges(_:))
- [CKSyncEngine.Event.SentRecordZoneChanges](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges)

##### Accessing successful changes

- [let deletedRecordIDs: [CKRecord.ID]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/deletedrecordids)
- [let savedRecords: [CKRecord]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/savedrecords)

##### Accessing failed changes

- [let failedRecordDeletes: [CKRecord.ID : CKError]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecorddeletes)
- [let failedRecordSaves: [CKSyncEngine.Event.SentRecordZoneChanges.FailedRecordSave]](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsaves)
- [CKSyncEngine.Event.SentRecordZoneChanges.FailedRecordSave](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave)

###### Accessing the record

- [let record: CKRecord](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave/record)

###### Accessing the error

- [let error: CKError](/documentation/cloudkit/cksyncengine-5sie5/event/sentrecordzonechanges/failedrecordsave/error)
- [case didSendChanges(CKSyncEngine.Event.DidSendChanges)](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges(_:))
- [CKSyncEngine.Event.DidSendChanges](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges)

##### Accessing the context

- [let context: CKSyncEngine.SendChangesContext](/documentation/cloudkit/cksyncengine-5sie5/event/didsendchanges/context)

#### State updates

- [case stateUpdate(CKSyncEngine.Event.StateUpdate)](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate(_:))
- [CKSyncEngine.Event.StateUpdate](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate)

##### Accessing the state

- [let stateSerialization: CKSyncEngine.State.Serialization](/documentation/cloudkit/cksyncengine-5sie5/event/stateupdate/stateserialization)
- [CKSyncEngine.PendingDatabaseChange](/documentation/cloudkit/cksyncengine-5sie5/pendingdatabasechange)

#### Database change types

- [CKSyncEnginePendingDatabaseChangeType](/documentation/cloudkit/cksyncenginependingdatabasechangetype)

##### Enumeration Cases

- [case deleteZone](/documentation/cloudkit/cksyncenginependingdatabasechangetype/deletezone)
- [case saveZone](/documentation/cloudkit/cksyncenginependingdatabasechangetype/savezone)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginependingdatabasechangetype/init(rawvalue:))

#### Enumeration Cases

- [case deleteZone(CKRecordZone.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingdatabasechange/deletezone(_:))
- [case saveZone(CKRecordZone)](/documentation/cloudkit/cksyncengine-5sie5/pendingdatabasechange/savezone(_:))
- [CKSyncEngine.PendingRecordZoneChange](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange)

#### Record change types

- [CKSyncEnginePendingRecordZoneChangeType](/documentation/cloudkit/cksyncenginependingrecordzonechangetype)

##### Enumeration Cases

- [case deleteRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/deleterecord)
- [case saveRecord](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/saverecord)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/cksyncenginependingrecordzonechangetype/init(rawvalue:))

#### Enumeration Cases

- [case deleteRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/deleterecord(_:))
- [case saveRecord(CKRecord.ID)](/documentation/cloudkit/cksyncengine-5sie5/pendingrecordzonechange/saverecord(_:))
- [CKSyncEngine.SyncReason](/documentation/cloudkit/cksyncengine-5sie5/syncreason)

#### Sync reasons

- [case scheduled](/documentation/cloudkit/cksyncengine-5sie5/syncreason/scheduled)
- [case manual](/documentation/cloudkit/cksyncengine-5sie5/syncreason/manual)
- [Shared Records](/documentation/cloudkit/shared-records)

### Collaboration

- [Sharing CloudKit Data with Other iCloud Users](/documentation/cloudkit/sharing-cloudkit-data-with-other-icloud-users)
- [Sharing Core Data objects between iCloud users](/documentation/coredata/sharing-core-data-objects-between-icloud-users)
- [CKShare](/documentation/cloudkit/ckshare)

#### Creating a Share

- [init(coder: NSCoder)](/documentation/cloudkit/ckshare/init(coder:))
- [convenience init(rootRecord: CKRecord)](/documentation/cloudkit/ckshare/init(rootrecord:))
- [init(rootRecord: CKRecord, shareID: CKRecord.ID)](/documentation/cloudkit/ckshare/init(rootrecord:shareid:))
- [init(recordZoneID: CKRecordZone.ID)](/documentation/cloudkit/ckshare/init(recordzoneid:))

#### Accessing the Share’s Attributes

- [var owner: CKShare.Participant](/documentation/cloudkit/ckshare/owner)
- [var currentUserParticipant: CKShare.Participant?](/documentation/cloudkit/ckshare/currentuserparticipant)
- [var participants: [CKShare.Participant]](/documentation/cloudkit/ckshare/participants)
- [var url: URL?](/documentation/cloudkit/ckshare/url)

#### Configuring the Share

- [var publicPermission: CKShare.ParticipantPermission](/documentation/cloudkit/ckshare/publicpermission)
- [func addParticipant(CKShare.Participant)](/documentation/cloudkit/ckshare/addparticipant(_:))
- [func removeParticipant(CKShare.Participant)](/documentation/cloudkit/ckshare/removeparticipant(_:))
- [CKShare.Participant](/documentation/cloudkit/ckshare/participant)

##### Accessing the Participant’s Status

- [var acceptanceStatus: CKShare.ParticipantAcceptanceStatus](/documentation/cloudkit/ckshare/participant/acceptancestatus-swift.property)
- [CKShare.Participant.AcceptanceStatus](/documentation/cloudkit/ckshare/participant/acceptancestatus-swift.typealias)
- [CKShare.ParticipantAcceptanceStatus](/documentation/cloudkit/ckshare/participantacceptancestatus)

###### Constants

- [case unknown](/documentation/cloudkit/ckshare/participantacceptancestatus/unknown)
- [case pending](/documentation/cloudkit/ckshare/participantacceptancestatus/pending)
- [case accepted](/documentation/cloudkit/ckshare/participantacceptancestatus/accepted)
- [case removed](/documentation/cloudkit/ckshare/participantacceptancestatus/removed)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participantacceptancestatus/init(rawvalue:))

##### Accessing the Participant’s Identity

- [var userIdentity: CKUserIdentity](/documentation/cloudkit/ckshare/participant/useridentity)

##### Managing the Participant’s Capabilites

- [var permission: CKShare.ParticipantPermission](/documentation/cloudkit/ckshare/participant/permission-swift.property)
- [CKShare.Participant.Permission](/documentation/cloudkit/ckshare/participant/permission-swift.typealias)
- [CKShare.ParticipantPermission](/documentation/cloudkit/ckshare/participantpermission)

###### Permissions

- [case none](/documentation/cloudkit/ckshare/participantpermission/none)
- [case readOnly](/documentation/cloudkit/ckshare/participantpermission/readonly)
- [case readWrite](/documentation/cloudkit/ckshare/participantpermission/readwrite)
- [case unknown](/documentation/cloudkit/ckshare/participantpermission/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participantpermission/init(rawvalue:))
- [var role: CKShare.ParticipantRole](/documentation/cloudkit/ckshare/participant/role-swift.property)
- [CKShare.Participant.Role](/documentation/cloudkit/ckshare/participant/role-swift.typealias)
- [CKShare.ParticipantRole](/documentation/cloudkit/ckshare/participantrole)

###### Roles

- [case owner](/documentation/cloudkit/ckshare/participantrole/owner)
- [case privateUser](/documentation/cloudkit/ckshare/participantrole/privateuser)
- [case publicUser](/documentation/cloudkit/ckshare/participantrole/publicuser)
- [case unknown](/documentation/cloudkit/ckshare/participantrole/unknown)

###### Enumeration Cases

- [case administrator](/documentation/cloudkit/ckshare/participantrole/administrator)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participantrole/init(rawvalue:))

##### Deprecated

- [Deprecated Symbols](/documentation/cloudkit/participant-deprecated-symbols)

###### Deprecated Properties

- [var type: CKShare.ParticipantType](/documentation/cloudkit/ckshare/participant/type)
- [CKShare.Participant.ParticipantType](/documentation/cloudkit/ckshare/participant/participanttype)
- [CKShare.ParticipantType](/documentation/cloudkit/ckshare/participanttype)

###### Constants

- [case owner](/documentation/cloudkit/ckshare/participantrole/owner)
- [case privateUser](/documentation/cloudkit/ckshare/participantrole/privateuser)
- [case publicUser](/documentation/cloudkit/ckshare/participantrole/publicuser)
- [case unknown](/documentation/cloudkit/ckshare/participantrole/unknown)
- [case unknown](/documentation/cloudkit/ckshare/participanttype/unknown)
- [case owner](/documentation/cloudkit/ckshare/participanttype/owner)
- [case privateUser](/documentation/cloudkit/ckshare/participanttype/privateuser)
- [case publicUser](/documentation/cloudkit/ckshare/participanttype/publicuser)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participanttype/init(rawvalue:))

##### Instance Properties

- [var dateAddedToShare: Date?](/documentation/cloudkit/ckshare/participant/dateaddedtoshare)
- [var isApprovedRequester: Bool](/documentation/cloudkit/ckshare/participant/isapprovedrequester)
- [var participantID: CKShare.Participant.ID](/documentation/cloudkit/ckshare/participant/participantid)

##### Type Aliases

- [CKShare.Participant.ID](/documentation/cloudkit/ckshare/participant/id)

##### Type Methods

- [class func oneTimeURLParticipant() -> Self](/documentation/cloudkit/ckshare/participant/onetimeurlparticipant())

#### Accessing Metadata

- [CKShare.Metadata](/documentation/cloudkit/ckshare/metadata)

##### Accessing the Share

- [var share: CKShare](/documentation/cloudkit/ckshare/metadata/share)
- [var containerIdentifier: String](/documentation/cloudkit/ckshare/metadata/containeridentifier)
- [var ownerIdentity: CKUserIdentity](/documentation/cloudkit/ckshare/metadata/owneridentity)

##### Accessing the Root Record

- [var hierarchicalRootRecordID: CKRecord.ID?](/documentation/cloudkit/ckshare/metadata/hierarchicalrootrecordid)
- [var rootRecord: CKRecord?](/documentation/cloudkit/ckshare/metadata/rootrecord)
- [var rootRecordID: CKRecord.ID](/documentation/cloudkit/ckshare/metadata/rootrecordid)

##### Accessing the Participant’s Capabilities

- [var participantRole: CKShare.ParticipantRole](/documentation/cloudkit/ckshare/metadata/participantrole)
- [var participantPermission: CKShare.ParticipantPermission](/documentation/cloudkit/ckshare/metadata/participantpermission)
- [var participantStatus: CKShare.ParticipantAcceptanceStatus](/documentation/cloudkit/ckshare/metadata/participantstatus)
- [var participantType: CKShare.ParticipantType](/documentation/cloudkit/ckshare/metadata/participanttype)

#### Subscripting

- [CKShare.SystemFieldKey](/documentation/cloudkit/ckshare/systemfieldkey)

##### Constants

- [static let shareType: CKRecord.FieldKey](/documentation/cloudkit/ckshare/systemfieldkey/sharetype)
- [static let title: CKRecord.FieldKey](/documentation/cloudkit/ckshare/systemfieldkey/title)
- [static let thumbnailImageData: CKRecord.FieldKey](/documentation/cloudkit/ckshare/systemfieldkey/thumbnailimagedata)

#### Classes

- [CKShare.AccessRequester](/documentation/cloudkit/ckshare/accessrequester)

##### Instance Properties

- [var contact: CNContact](/documentation/cloudkit/ckshare/accessrequester/contact)
- [var participantLookupInfo: CKUserIdentity.LookupInfo](/documentation/cloudkit/ckshare/accessrequester/participantlookupinfo)
- [var userIdentity: CKUserIdentity](/documentation/cloudkit/ckshare/accessrequester/useridentity)
- [CKShare.BlockedIdentity](/documentation/cloudkit/ckshare/blockedidentity)

##### Instance Properties

- [var contact: CNContact](/documentation/cloudkit/ckshare/blockedidentity/contact)
- [var userIdentity: CKUserIdentity](/documentation/cloudkit/ckshare/blockedidentity/useridentity)

#### Instance Properties

- [var allowsAccessRequests: Bool](/documentation/cloudkit/ckshare/allowsaccessrequests)
- [var blockedIdentities: [CKShare.BlockedIdentity]](/documentation/cloudkit/ckshare/blockedidentities)
- [var requesters: [CKShare.AccessRequester]](/documentation/cloudkit/ckshare/requesters)

#### Instance Methods

- [func blockRequesters([CKShare.AccessRequester])](/documentation/cloudkit/ckshare/blockrequesters(_:))
- [func denyRequesters([CKShare.AccessRequester])](/documentation/cloudkit/ckshare/denyrequesters(_:))
- [func oneTimeURL(for: CKShare.Participant.ID) -> URL?](/documentation/cloudkit/ckshare/onetimeurl(for:))
- [func unblockIdentities([CKShare.BlockedIdentity])](/documentation/cloudkit/ckshare/unblockidentities(_:))
- [CKShareTransferRepresentation](/documentation/cloudkit/cksharetransferrepresentation)

#### Creating a transfer representation

- [init(exporter: (Item) throws -> CKShareTransferRepresentation<Item>.ExportedShare)](/documentation/cloudkit/cksharetransferrepresentation/init(exporter:))

#### Accessing transfer representation attributes

- [CKShareTransferRepresentation.ExportedShare](/documentation/cloudkit/cksharetransferrepresentation/exportedshare)

##### Preparing an exported share

- [static func existing(CKShare, container: CKContainer, allowedSharingOptions: CKAllowedSharingOptions) -> CKShareTransferRepresentation<Item>.ExportedShare](/documentation/cloudkit/cksharetransferrepresentation/exportedshare/existing(_:container:allowedsharingoptions:))
- [static func prepareShare(container: CKContainer, allowedSharingOptions: CKAllowedSharingOptions, preparationHandler: () async throws -> CKShare) -> CKShareTransferRepresentation<Item>.ExportedShare](/documentation/cloudkit/cksharetransferrepresentation/exportedshare/prepareshare(container:allowedsharingoptions:preparationhandler:))
- [CKAllowedSharingOptions](/documentation/cloudkit/ckallowedsharingoptions)

#### Creating sharing options

- [init(allowedParticipantPermissionOptions: CKSharingParticipantPermissionOption, allowedParticipantAccessOptions: CKSharingParticipantAccessOption)](/documentation/cloudkit/ckallowedsharingoptions/init(allowedparticipantpermissionoptions:allowedparticipantaccessoptions:))

#### Using the standard options

- [class var standard: CKAllowedSharingOptions](/documentation/cloudkit/ckallowedsharingoptions/standard)

#### Configuring the options

- [var allowedParticipantAccessOptions: CKSharingParticipantAccessOption](/documentation/cloudkit/ckallowedsharingoptions/allowedparticipantaccessoptions)
- [var allowedParticipantPermissionOptions: CKSharingParticipantPermissionOption](/documentation/cloudkit/ckallowedsharingoptions/allowedparticipantpermissionoptions)
- [CKSharingParticipantAccessOption](/documentation/cloudkit/cksharingparticipantaccessoption)

##### Creating an access option

- [init(rawValue: UInt)](/documentation/cloudkit/cksharingparticipantaccessoption/init(rawvalue:))

##### Configuring the options

- [static var any: CKSharingParticipantAccessOption](/documentation/cloudkit/cksharingparticipantaccessoption/any)
- [static var anyoneWithLink: CKSharingParticipantAccessOption](/documentation/cloudkit/cksharingparticipantaccessoption/anyonewithlink)
- [static var specifiedRecipientsOnly: CKSharingParticipantAccessOption](/documentation/cloudkit/cksharingparticipantaccessoption/specifiedrecipientsonly)
- [CKSharingParticipantPermissionOption](/documentation/cloudkit/cksharingparticipantpermissionoption)

##### Creating an access option

- [init(rawValue: UInt)](/documentation/cloudkit/cksharingparticipantpermissionoption/init(rawvalue:))

##### Configuring the options

- [static var any: CKSharingParticipantPermissionOption](/documentation/cloudkit/cksharingparticipantpermissionoption/any)
- [static var readOnly: CKSharingParticipantPermissionOption](/documentation/cloudkit/cksharingparticipantpermissionoption/readonly)
- [static var readWrite: CKSharingParticipantPermissionOption](/documentation/cloudkit/cksharingparticipantpermissionoption/readwrite)

#### Instance Properties

- [var allowsAccessRequests: Bool](/documentation/cloudkit/ckallowedsharingoptions/allowsaccessrequests)
- [var allowsParticipantsToInviteOthers: Bool](/documentation/cloudkit/ckallowedsharingoptions/allowsparticipantstoinviteothers)
- [CKSystemSharingUIObserver](/documentation/cloudkit/cksystemsharinguiobserver)

#### Creating a sharing observer

- [init(container: CKContainer)](/documentation/cloudkit/cksystemsharinguiobserver/init(container:))

#### Accessing sharing blocks

- [var systemSharingUIDidSaveShareBlock: ((CKRecord.ID, Result<CKShare, any Error>) -> Void)?](/documentation/cloudkit/cksystemsharinguiobserver/systemsharinguididsaveshareblock-8c9vi)
- [var systemSharingUIDidStopSharingBlock: ((CKRecord.ID, Result<Void, any Error>) -> Void)?](/documentation/cloudkit/cksystemsharinguiobserver/systemsharinguididstopsharingblock-7nmiw)
- [UICloudSharingController](/documentation/uikit/uicloudsharingcontroller)
- [CKSharingSupported](/documentation/bundleresources/information-property-list/cksharingsupported)

### Share Requests

- [CKFetchShareMetadataOperation](/documentation/cloudkit/ckfetchsharemetadataoperation)

#### Creating an Operation

- [init()](/documentation/cloudkit/ckfetchsharemetadataoperation/init())
- [convenience init(shareURLs: [URL])](/documentation/cloudkit/ckfetchsharemetadataoperation/init(shareurls:))

#### Configuring the Operation

- [var shareURLs: [URL]?](/documentation/cloudkit/ckfetchsharemetadataoperation/shareurls)
- [var shouldFetchRootRecord: Bool](/documentation/cloudkit/ckfetchsharemetadataoperation/shouldfetchrootrecord)

#### Processing the Operation’s Results

- [var perShareMetadataBlock: ((URL, CKShare.Metadata?, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchsharemetadataoperation/persharemetadatablock)
- [var fetchShareMetadataCompletionBlock: (((any Error)?) -> Void)?](/documentation/cloudkit/ckfetchsharemetadataoperation/fetchsharemetadatacompletionblock)

#### Instance Properties

- [var fetchShareMetadataResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckfetchsharemetadataoperation/fetchsharemetadataresultblock)
- [var perShareMetadataResultBlock: ((URL, Result<CKShare.Metadata, any Error>) -> Void)?](/documentation/cloudkit/ckfetchsharemetadataoperation/persharemetadataresultblock)
- [var rootRecordDesiredKeys: [CKRecord.FieldKey]?](/documentation/cloudkit/ckfetchsharemetadataoperation/rootrecorddesiredkeys-3xrex)
- [CKShare.Metadata](/documentation/cloudkit/ckshare/metadata)

#### Accessing the Share

- [var share: CKShare](/documentation/cloudkit/ckshare/metadata/share)
- [var containerIdentifier: String](/documentation/cloudkit/ckshare/metadata/containeridentifier)
- [var ownerIdentity: CKUserIdentity](/documentation/cloudkit/ckshare/metadata/owneridentity)

#### Accessing the Root Record

- [var hierarchicalRootRecordID: CKRecord.ID?](/documentation/cloudkit/ckshare/metadata/hierarchicalrootrecordid)
- [var rootRecord: CKRecord?](/documentation/cloudkit/ckshare/metadata/rootrecord)
- [var rootRecordID: CKRecord.ID](/documentation/cloudkit/ckshare/metadata/rootrecordid)

#### Accessing the Participant’s Capabilities

- [var participantRole: CKShare.ParticipantRole](/documentation/cloudkit/ckshare/metadata/participantrole)
- [var participantPermission: CKShare.ParticipantPermission](/documentation/cloudkit/ckshare/metadata/participantpermission)
- [var participantStatus: CKShare.ParticipantAcceptanceStatus](/documentation/cloudkit/ckshare/metadata/participantstatus)
- [var participantType: CKShare.ParticipantType](/documentation/cloudkit/ckshare/metadata/participanttype)
- [CKAcceptSharesOperation](/documentation/cloudkit/ckacceptsharesoperation)

#### Creating a Share Accept Operation

- [init()](/documentation/cloudkit/ckacceptsharesoperation/init())
- [convenience init(shareMetadatas: [CKShare.Metadata])](/documentation/cloudkit/ckacceptsharesoperation/init(sharemetadatas:))

#### Processing the Share Accept Results

- [var shareMetadatas: [CKShare.Metadata]?](/documentation/cloudkit/ckacceptsharesoperation/sharemetadatas)
- [var perShareCompletionBlock: ((CKShare.Metadata, CKShare?, (any Error)?) -> Void)?](/documentation/cloudkit/ckacceptsharesoperation/persharecompletionblock)
- [var acceptSharesCompletionBlock: (((any Error)?) -> Void)?](/documentation/cloudkit/ckacceptsharesoperation/acceptsharescompletionblock)

#### Instance Properties

- [var acceptSharesResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckacceptsharesoperation/acceptsharesresultblock)
- [var perShareResultBlock: ((CKShare.Metadata, Result<CKShare, any Error>) -> Void)?](/documentation/cloudkit/ckacceptsharesoperation/pershareresultblock)

### Participants

- [CKFetchShareParticipantsOperation](/documentation/cloudkit/ckfetchshareparticipantsoperation)

#### Creating an Operation

- [init()](/documentation/cloudkit/ckfetchshareparticipantsoperation/init())
- [convenience init(userIdentityLookupInfos: [CKUserIdentity.LookupInfo])](/documentation/cloudkit/ckfetchshareparticipantsoperation/init(useridentitylookupinfos:))

#### Configuring the Operation

- [var userIdentityLookupInfos: [CKUserIdentity.LookupInfo]?](/documentation/cloudkit/ckfetchshareparticipantsoperation/useridentitylookupinfos)

#### Processing the Operation’s Results

- [var shareParticipantFetchedBlock: ((CKShare.Participant) -> Void)?](/documentation/cloudkit/ckfetchshareparticipantsoperation/shareparticipantfetchedblock)
- [var fetchShareParticipantsCompletionBlock: (((any Error)?) -> Void)?](/documentation/cloudkit/ckfetchshareparticipantsoperation/fetchshareparticipantscompletionblock)

#### Instance Properties

- [var fetchShareParticipantsResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckfetchshareparticipantsoperation/fetchshareparticipantsresultblock)
- [var perShareParticipantResultBlock: ((CKUserIdentity.LookupInfo, Result<CKShare.Participant, any Error>) -> Void)?](/documentation/cloudkit/ckfetchshareparticipantsoperation/pershareparticipantresultblock)
- [CKShare.Participant](/documentation/cloudkit/ckshare/participant)

#### Accessing the Participant’s Status

- [var acceptanceStatus: CKShare.ParticipantAcceptanceStatus](/documentation/cloudkit/ckshare/participant/acceptancestatus-swift.property)
- [CKShare.Participant.AcceptanceStatus](/documentation/cloudkit/ckshare/participant/acceptancestatus-swift.typealias)
- [CKShare.ParticipantAcceptanceStatus](/documentation/cloudkit/ckshare/participantacceptancestatus)

##### Constants

- [case unknown](/documentation/cloudkit/ckshare/participantacceptancestatus/unknown)
- [case pending](/documentation/cloudkit/ckshare/participantacceptancestatus/pending)
- [case accepted](/documentation/cloudkit/ckshare/participantacceptancestatus/accepted)
- [case removed](/documentation/cloudkit/ckshare/participantacceptancestatus/removed)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participantacceptancestatus/init(rawvalue:))

#### Accessing the Participant’s Identity

- [var userIdentity: CKUserIdentity](/documentation/cloudkit/ckshare/participant/useridentity)

#### Managing the Participant’s Capabilites

- [var permission: CKShare.ParticipantPermission](/documentation/cloudkit/ckshare/participant/permission-swift.property)
- [CKShare.Participant.Permission](/documentation/cloudkit/ckshare/participant/permission-swift.typealias)
- [CKShare.ParticipantPermission](/documentation/cloudkit/ckshare/participantpermission)

##### Permissions

- [case none](/documentation/cloudkit/ckshare/participantpermission/none)
- [case readOnly](/documentation/cloudkit/ckshare/participantpermission/readonly)
- [case readWrite](/documentation/cloudkit/ckshare/participantpermission/readwrite)
- [case unknown](/documentation/cloudkit/ckshare/participantpermission/unknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participantpermission/init(rawvalue:))
- [var role: CKShare.ParticipantRole](/documentation/cloudkit/ckshare/participant/role-swift.property)
- [CKShare.Participant.Role](/documentation/cloudkit/ckshare/participant/role-swift.typealias)
- [CKShare.ParticipantRole](/documentation/cloudkit/ckshare/participantrole)

##### Roles

- [case owner](/documentation/cloudkit/ckshare/participantrole/owner)
- [case privateUser](/documentation/cloudkit/ckshare/participantrole/privateuser)
- [case publicUser](/documentation/cloudkit/ckshare/participantrole/publicuser)
- [case unknown](/documentation/cloudkit/ckshare/participantrole/unknown)

##### Enumeration Cases

- [case administrator](/documentation/cloudkit/ckshare/participantrole/administrator)

##### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participantrole/init(rawvalue:))

#### Deprecated

- [Deprecated Symbols](/documentation/cloudkit/participant-deprecated-symbols)

##### Deprecated Properties

- [var type: CKShare.ParticipantType](/documentation/cloudkit/ckshare/participant/type)
- [CKShare.Participant.ParticipantType](/documentation/cloudkit/ckshare/participant/participanttype)
- [CKShare.ParticipantType](/documentation/cloudkit/ckshare/participanttype)

###### Constants

- [case owner](/documentation/cloudkit/ckshare/participantrole/owner)
- [case privateUser](/documentation/cloudkit/ckshare/participantrole/privateuser)
- [case publicUser](/documentation/cloudkit/ckshare/participantrole/publicuser)
- [case unknown](/documentation/cloudkit/ckshare/participantrole/unknown)
- [case unknown](/documentation/cloudkit/ckshare/participanttype/unknown)
- [case owner](/documentation/cloudkit/ckshare/participanttype/owner)
- [case privateUser](/documentation/cloudkit/ckshare/participanttype/privateuser)
- [case publicUser](/documentation/cloudkit/ckshare/participanttype/publicuser)

###### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckshare/participanttype/init(rawvalue:))

#### Instance Properties

- [var dateAddedToShare: Date?](/documentation/cloudkit/ckshare/participant/dateaddedtoshare)
- [var isApprovedRequester: Bool](/documentation/cloudkit/ckshare/participant/isapprovedrequester)
- [var participantID: CKShare.Participant.ID](/documentation/cloudkit/ckshare/participant/participantid)

#### Type Aliases

- [CKShare.Participant.ID](/documentation/cloudkit/ckshare/participant/id)

#### Type Methods

- [class func oneTimeURLParticipant() -> Self](/documentation/cloudkit/ckshare/participant/onetimeurlparticipant())

### Base Objects

- [CKOperation](/documentation/cloudkit/ckoperation)

#### Creating an Operation

- [init()](/documentation/cloudkit/ckoperation/init())

#### Identifying the Operation

- [var operationID: CKOperation.ID](/documentation/cloudkit/ckoperation/operationid-8auuc)
- [CKOperation.ID](/documentation/cloudkit/ckoperation/id)

#### Managing the Operation’s Configuration

- [var configuration: CKOperation.Configuration!](/documentation/cloudkit/ckoperation/configuration-swift.property)
- [CKOperation.Configuration](/documentation/cloudkit/ckoperation/configuration-swift.class)

##### Preparing a Configuration

- [var allowsCellularAccess: Bool](/documentation/cloudkit/ckoperation/configuration-swift.class/allowscellularaccess)
- [var container: CKContainer?](/documentation/cloudkit/ckoperation/configuration-swift.class/container)
- [var isLongLived: Bool](/documentation/cloudkit/ckoperation/configuration-swift.class/islonglived)
- [var qualityOfService: QualityOfService](/documentation/cloudkit/ckoperation/configuration-swift.class/qualityofservice)
- [var timeoutIntervalForRequest: TimeInterval](/documentation/cloudkit/ckoperation/configuration-swift.class/timeoutintervalforrequest)
- [var timeoutIntervalForResource: TimeInterval](/documentation/cloudkit/ckoperation/configuration-swift.class/timeoutintervalforresource)
- [var group: CKOperationGroup?](/documentation/cloudkit/ckoperation/group)
- [var longLivedOperationWasPersistedBlock: (() -> Void)?](/documentation/cloudkit/ckoperation/longlivedoperationwaspersistedblock)

#### Deprecated

- [Deprecated Symbols](/documentation/cloudkit/ckoperation-deprecated-symbols)

##### Deprecated Properties

- [var allowsCellularAccess: Bool](/documentation/cloudkit/ckoperation/allowscellularaccess)
- [var container: CKContainer?](/documentation/cloudkit/ckoperation/container)
- [var isLongLived: Bool](/documentation/cloudkit/ckoperation/islonglived)
- [var timeoutIntervalForRequest: TimeInterval](/documentation/cloudkit/ckoperation/timeoutintervalforrequest)
- [var timeoutIntervalForResource: TimeInterval](/documentation/cloudkit/ckoperation/timeoutintervalforresource)

## User discovery

- [CKUserIdentity](/documentation/cloudkit/ckuseridentity)

### Accessing iCloud Information

- [var hasiCloudAccount: Bool](/documentation/cloudkit/ckuseridentity/hasicloudaccount)
- [var lookupInfo: CKUserIdentity.LookupInfo?](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.property)
- [CKUserIdentity.LookupInfo](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class)

#### Creating a Lookup Info

- [init(emailAddress: String)](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/init(emailaddress:))
- [init(phoneNumber: String)](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/init(phonenumber:))
- [init(userRecordID: CKRecord.ID)](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/init(userrecordid:))

#### Creating Multiple Lookup Infos

- [class func lookupInfos(withEmails: [String]) -> [CKUserIdentity.LookupInfo]](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/lookupinfos(withemails:))
- [class func lookupInfos(withPhoneNumbers: [String]) -> [CKUserIdentity.LookupInfo]](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/lookupinfos(withphonenumbers:))
- [class func lookupInfos(with: [CKRecord.ID]) -> [CKUserIdentity.LookupInfo]](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/lookupinfos(with:))

#### Accessing the Criteria

- [var emailAddress: String?](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/emailaddress)
- [var phoneNumber: String?](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/phonenumber)
- [var userRecordID: CKRecord.ID?](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/userrecordid)

### Accessing User Information

- [var userRecordID: CKRecord.ID?](/documentation/cloudkit/ckuseridentity/userrecordid)
- [var contactIdentifiers: [String]](/documentation/cloudkit/ckuseridentity/contactidentifiers)
- [var nameComponents: PersonNameComponents?](/documentation/cloudkit/ckuseridentity/namecomponents)
- [CKUserIdentity.LookupInfo](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class)

### Creating a Lookup Info

- [init(emailAddress: String)](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/init(emailaddress:))
- [init(phoneNumber: String)](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/init(phonenumber:))
- [init(userRecordID: CKRecord.ID)](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/init(userrecordid:))

### Creating Multiple Lookup Infos

- [class func lookupInfos(withEmails: [String]) -> [CKUserIdentity.LookupInfo]](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/lookupinfos(withemails:))
- [class func lookupInfos(withPhoneNumbers: [String]) -> [CKUserIdentity.LookupInfo]](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/lookupinfos(withphonenumbers:))
- [class func lookupInfos(with: [CKRecord.ID]) -> [CKUserIdentity.LookupInfo]](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/lookupinfos(with:))

### Accessing the Criteria

- [var emailAddress: String?](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/emailaddress)
- [var phoneNumber: String?](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/phonenumber)
- [var userRecordID: CKRecord.ID?](/documentation/cloudkit/ckuseridentity/lookupinfo-swift.class/userrecordid)

## Core objects

- [CKContainer](/documentation/cloudkit/ckcontainer)

### Creating Containers

- [class func `default`() -> CKContainer](/documentation/cloudkit/ckcontainer/default())
- [init(identifier: String)](/documentation/cloudkit/ckcontainer/init(identifier:))

### Getting the Public and Private Databases

- [var privateCloudDatabase: CKDatabase](/documentation/cloudkit/ckcontainer/privateclouddatabase)
- [var publicCloudDatabase: CKDatabase](/documentation/cloudkit/ckcontainer/publicclouddatabase)
- [var sharedCloudDatabase: CKDatabase](/documentation/cloudkit/ckcontainer/sharedclouddatabase)
- [func database(with: CKDatabase.Scope) -> CKDatabase](/documentation/cloudkit/ckcontainer/database(with:))

### Getting the Container’s Identifier

- [var containerIdentifier: String?](/documentation/cloudkit/ckcontainer/containeridentifier)

### Determining the User’s iCloud Access Status

- [func accountStatus(completionHandler: (CKAccountStatus, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/accountstatus(completionhandler:))
- [CKAccountStatus](/documentation/cloudkit/ckaccountstatus)

#### Account Statuses

- [case available](/documentation/cloudkit/ckaccountstatus/available)
- [case couldNotDetermine](/documentation/cloudkit/ckaccountstatus/couldnotdetermine)
- [case noAccount](/documentation/cloudkit/ckaccountstatus/noaccount)
- [case restricted](/documentation/cloudkit/ckaccountstatus/restricted)
- [case temporarilyUnavailable](/documentation/cloudkit/ckaccountstatus/temporarilyunavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckaccountstatus/init(rawvalue:))

### Requesting and Determining App Permissions

- [func requestApplicationPermission(CKContainer.ApplicationPermissions, completionHandler: (CKContainer.ApplicationPermissionStatus, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/requestapplicationpermission(_:completionhandler:))
- [func status(forApplicationPermission: CKContainer.ApplicationPermissions, completionHandler: (CKContainer.ApplicationPermissionStatus, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/status(forapplicationpermission:completionhandler:))
- [CKContainer.Application](/documentation/cloudkit/ckcontainer/application)

#### Container Application Types

- [CKContainer.Application.Permissions](/documentation/cloudkit/ckcontainer/application/permissions)
- [CKContainer.Application.PermissionBlock](/documentation/cloudkit/ckcontainer/application/permissionblock)
- [CKContainer.Application.PermissionStatus](/documentation/cloudkit/ckcontainer/application/permissionstatus)
- [CKContainer.ApplicationPermissions](/documentation/cloudkit/ckcontainer/applicationpermissions)

#### Creating Permissions

- [init(rawValue: UInt)](/documentation/cloudkit/ckcontainer/applicationpermissions/init(rawvalue:))

#### Accessing Permissions

- [static var userDiscoverability: CKContainer.ApplicationPermissions](/documentation/cloudkit/ckcontainer/applicationpermissions/userdiscoverability)
- [CKContainer.ApplicationPermissionBlock](/documentation/cloudkit/ckcontainer/applicationpermissionblock)
- [CKContainer.ApplicationPermissionStatus](/documentation/cloudkit/ckcontainer/applicationpermissionstatus)

#### Permission Statuses

- [case initialState](/documentation/cloudkit/ckcontainer/applicationpermissionstatus/initialstate)
- [case couldNotComplete](/documentation/cloudkit/ckcontainer/applicationpermissionstatus/couldnotcomplete)
- [case denied](/documentation/cloudkit/ckcontainer/applicationpermissionstatus/denied)
- [case granted](/documentation/cloudkit/ckcontainer/applicationpermissionstatus/granted)

#### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckcontainer/applicationpermissionstatus/init(rawvalue:))

### Performing Operations on the Container

- [func add(CKOperation)](/documentation/cloudkit/ckcontainer/add(_:))

### Discovering User Records

- [func discoverAllIdentities(completionHandler: ([CKUserIdentity]?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/discoverallidentities(completionhandler:))
- [func discoverUserIdentity(withEmailAddress: String, completionHandler: (CKUserIdentity?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/discoveruseridentity(withemailaddress:completionhandler:))
- [func discoverUserIdentity(withPhoneNumber: String, completionHandler: (CKUserIdentity?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/discoveruseridentity(withphonenumber:completionhandler:))
- [func discoverUserIdentity(withUserRecordID: CKRecord.ID, completionHandler: (CKUserIdentity?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/discoveruseridentity(withuserrecordid:completionhandler:))
- [func fetchShareParticipant(withEmailAddress: String, completionHandler: (CKShare.Participant?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/fetchshareparticipant(withemailaddress:completionhandler:))
- [func fetchShareParticipant(withPhoneNumber: String, completionHandler: (CKShare.Participant?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/fetchshareparticipant(withphonenumber:completionhandler:))
- [func fetchShareParticipant(withUserRecordID: CKRecord.ID, completionHandler: (CKShare.Participant?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/fetchshareparticipant(withuserrecordid:completionhandler:))
- [func fetchUserRecordID(completionHandler: (CKRecord.ID?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/fetchuserrecordid(completionhandler:))
- [let CKCurrentUserDefaultName: String](/documentation/cloudkit/ckcurrentuserdefaultname)
- [let CKOwnerDefaultName: String](/documentation/cloudkit/ckownerdefaultname)

### Fetching Long-Lived Operations

- [func fetchAllLongLivedOperationIDs(completionHandler: ([CKOperation.ID]?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/fetchalllonglivedoperationids(completionhandler:))
- [func fetchLongLivedOperation(withID: CKOperation.ID, completionHandler: (CKOperation?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/fetchlonglivedoperation(withid:completionhandler:))

### Accessing Container Metadata

- [func fetchShareMetadata(with: URL, completionHandler: (CKShare.Metadata?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/fetchsharemetadata(with:completionhandler:))
- [func accept(CKShare.Metadata, completionHandler: (CKShare?, (any Error)?) -> Void)](/documentation/cloudkit/ckcontainer/accept(_:completionhandler:)-949ea)
- [static let CKAccountChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/ckaccountchanged)

### Instance Methods

- [func accept([CKShare.Metadata]) async throws -> [CKShare.Metadata : Result<CKShare, any Error>]](/documentation/cloudkit/ckcontainer/accept(_:))
- [func accept([CKShare.Metadata], completionHandler: (Result<[CKShare.Metadata : Result<CKShare, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/accept(_:completionhandler:)-7s3t7)
- [func allLongLivedOperationIDs() async throws -> [CKOperation.ID]](/documentation/cloudkit/ckcontainer/alllonglivedoperationids())
- [func configuredWith<R>(configuration: CKOperation.Configuration?, group: CKOperationGroup?, body: (CKContainer) throws -> R) rethrows -> R](/documentation/cloudkit/ckcontainer/configuredwith(configuration:group:body:)-40x6k)
- [func configuredWith<R>(configuration: CKOperation.Configuration?, group: CKOperationGroup?, body: (CKContainer) async throws -> R) async rethrows -> R](/documentation/cloudkit/ckcontainer/configuredwith(configuration:group:body:)-4kc2l)
- [func discoverUserIdentities(forEmailAddresses: [String], completionHandler: (Result<[String : CKUserIdentity], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/discoveruseridentities(foremailaddresses:completionhandler:))
- [func discoverUserIdentities(forPhoneNumbers: [String], completionHandler: (Result<[String : CKUserIdentity], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/discoveruseridentities(forphonenumbers:completionhandler:))
- [func discoverUserIdentities(forUserRecordIDs: [CKRecord.ID], completionHandler: (Result<[CKRecord.ID : CKUserIdentity], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/discoveruseridentities(foruserrecordids:completionhandler:))
- [func fetchShareMetadatas(for: [URL], completionHandler: (Result<[URL : Result<CKShare.Metadata, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/fetchsharemetadatas(for:completionhandler:))
- [func fetchShareParticipants(forEmailAddresses: [String], completionHandler: (Result<[String : Result<CKShare.Participant, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/fetchshareparticipants(foremailaddresses:completionhandler:))
- [func fetchShareParticipants(forPhoneNumbers: [String], completionHandler: (Result<[String : Result<CKShare.Participant, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/fetchshareparticipants(forphonenumbers:completionhandler:))
- [func fetchShareParticipants(forUserRecordIDs: [CKRecord.ID], completionHandler: (Result<[CKRecord.ID : Result<CKShare.Participant, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckcontainer/fetchshareparticipants(foruserrecordids:completionhandler:))
- [func longLivedOperation(for: CKOperation.ID) async throws -> CKOperation?](/documentation/cloudkit/ckcontainer/longlivedoperation(for:))
- [func requestShareAccess(for: [URL]) async throws -> [URL : Result<Void, any Error>]](/documentation/cloudkit/ckcontainer/requestshareaccess(for:))
- [func shareMetadatas(for: [URL]) async throws -> [URL : Result<CKShare.Metadata, any Error>]](/documentation/cloudkit/ckcontainer/sharemetadatas(for:))
- [func shareParticipants(for: [CKUserIdentity.LookupInfo]) async throws -> [CKUserIdentity.LookupInfo : Result<CKShare.Participant, any Error>]](/documentation/cloudkit/ckcontainer/shareparticipants(for:))
- [func shareParticipants(forEmailAddresses: [String]) async throws -> [String : Result<CKShare.Participant, any Error>]](/documentation/cloudkit/ckcontainer/shareparticipants(foremailaddresses:))
- [func shareParticipants(forPhoneNumbers: [String]) async throws -> [String : Result<CKShare.Participant, any Error>]](/documentation/cloudkit/ckcontainer/shareparticipants(forphonenumbers:))
- [func shareParticipants(forUserRecordIDs: [CKRecord.ID]) async throws -> [CKRecord.ID : Result<CKShare.Participant, any Error>]](/documentation/cloudkit/ckcontainer/shareparticipants(foruserrecordids:))
- [func userIdentities(forEmailAddresses: [String]) async throws -> [String : CKUserIdentity]](/documentation/cloudkit/ckcontainer/useridentities(foremailaddresses:))
- [func userIdentities(forPhoneNumbers: [String]) async throws -> [String : CKUserIdentity]](/documentation/cloudkit/ckcontainer/useridentities(forphonenumbers:))
- [func userIdentities(forUserRecordIDs: [CKRecord.ID]) async throws -> [CKRecord.ID : CKUserIdentity]](/documentation/cloudkit/ckcontainer/useridentities(foruserrecordids:))
- [CKDatabase](/documentation/cloudkit/ckdatabase)

### Configuring Database Requests

- [func configuredWith<R>(configuration: CKOperation.Configuration?, group: CKOperationGroup?, body: (CKDatabase) async throws -> R) async rethrows -> R](/documentation/cloudkit/ckdatabase/configuredwith(configuration:group:body:)-637p1)
- [func configuredWith<R>(configuration: CKOperation.Configuration?, group: CKOperationGroup?, body: (CKDatabase) throws -> R) rethrows -> R](/documentation/cloudkit/ckdatabase/configuredwith(configuration:group:body:)-12vrs)

### Fetching Records

- [func records(for: [CKRecord.ID], desiredKeys: [CKRecord.FieldKey]?) async throws -> [CKRecord.ID : Result<CKRecord, any Error>]](/documentation/cloudkit/ckdatabase/records(for:desiredkeys:))
- [func fetch(withRecordIDs: [CKRecord.ID], desiredKeys: [CKRecord.FieldKey]?, completionHandler: (Result<[CKRecord.ID : Result<CKRecord, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withrecordids:desiredkeys:completionhandler:))
- [func fetch(withRecordID: CKRecord.ID, completionHandler: (CKRecord?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withrecordid:completionhandler:))

### Querying Records

- [func records(matching: CKQuery, inZoneWith: CKRecordZone.ID?, desiredKeys: [CKRecord.FieldKey]?, resultsLimit: Int) async throws -> (matchResults: [(CKRecord.ID, Result<CKRecord, any Error>)], queryCursor: CKQueryOperation.Cursor?)](/documentation/cloudkit/ckdatabase/records(matching:inzonewith:desiredkeys:resultslimit:))
- [func records(continuingMatchFrom: CKQueryOperation.Cursor, desiredKeys: [CKRecord.FieldKey]?, resultsLimit: Int) async throws -> (matchResults: [(CKRecord.ID, Result<CKRecord, any Error>)], queryCursor: CKQueryOperation.Cursor?)](/documentation/cloudkit/ckdatabase/records(continuingmatchfrom:desiredkeys:resultslimit:))
- [func fetch(withQuery: CKQuery, inZoneWith: CKRecordZone.ID?, desiredKeys: [CKRecord.FieldKey]?, resultsLimit: Int, completionHandler: (Result<(matchResults: [(CKRecord.ID, Result<CKRecord, any Error>)], queryCursor: CKQueryOperation.Cursor?), any Error>) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withquery:inzonewith:desiredkeys:resultslimit:completionhandler:))
- [func fetch(withCursor: CKQueryOperation.Cursor, desiredKeys: [CKRecord.FieldKey]?, resultsLimit: Int, completionHandler: (Result<(matchResults: [(CKRecord.ID, Result<CKRecord, any Error>)], queryCursor: CKQueryOperation.Cursor?), any Error>) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withcursor:desiredkeys:resultslimit:completionhandler:))
- [func perform(CKQuery, inZoneWith: CKRecordZone.ID?, completionHandler: ([CKRecord]?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/perform(_:inzonewith:completionhandler:))
- [func records(matching: CKQuery, inZoneWith: CKRecordZone.ID?) async throws -> [CKRecord]](/documentation/cloudkit/ckdatabase/records(matching:inzonewith:))

### Modifying Records

- [func modifyRecords(saving: [CKRecord], deleting: [CKRecord.ID], savePolicy: CKModifyRecordsOperation.RecordSavePolicy, atomically: Bool) async throws -> (saveResults: [CKRecord.ID : Result<CKRecord, any Error>], deleteResults: [CKRecord.ID : Result<Void, any Error>])](/documentation/cloudkit/ckdatabase/modifyrecords(saving:deleting:savepolicy:atomically:))
- [func modifyRecords(saving: [CKRecord], deleting: [CKRecord.ID], savePolicy: CKModifyRecordsOperation.RecordSavePolicy, atomically: Bool, completionHandler: (Result<(saveResults: [CKRecord.ID : Result<CKRecord, any Error>], deleteResults: [CKRecord.ID : Result<Void, any Error>]), any Error>) -> Void)](/documentation/cloudkit/ckdatabase/modifyrecords(saving:deleting:savepolicy:atomically:completionhandler:))
- [CKModifyRecordsOperation.RecordSavePolicy](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy)

#### Save Policies

- [case ifServerRecordUnchanged](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/ifserverrecordunchanged)
- [case changedKeys](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/changedkeys)
- [case allKeys](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/allkeys)

#### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckmodifyrecordsoperation/recordsavepolicy/init(rawvalue:))
- [func save(CKRecord, completionHandler: (CKRecord?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/save(_:completionhandler:)-3tatz)
- [func delete(withRecordID: CKRecord.ID, completionHandler: (CKRecord.ID?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/delete(withrecordid:completionhandler:))

### Fetching Record Zones

- [func recordZones(for: [CKRecordZone.ID]) async throws -> [CKRecordZone.ID : Result<CKRecordZone, any Error>]](/documentation/cloudkit/ckdatabase/recordzones(for:))
- [func fetch(withRecordZoneIDs: [CKRecordZone.ID], completionHandler: (Result<[CKRecordZone.ID : Result<CKRecordZone, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withrecordzoneids:completionhandler:))
- [func fetchAllRecordZones(completionHandler: ([CKRecordZone]?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/fetchallrecordzones(completionhandler:))
- [func fetch(withRecordZoneID: CKRecordZone.ID, completionHandler: (CKRecordZone?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withrecordzoneid:completionhandler:))

### Modifying Record Zones

- [func modifyRecordZones(saving: [CKRecordZone], deleting: [CKRecordZone.ID]) async throws -> (saveResults: [CKRecordZone.ID : Result<CKRecordZone, any Error>], deleteResults: [CKRecordZone.ID : Result<Void, any Error>])](/documentation/cloudkit/ckdatabase/modifyrecordzones(saving:deleting:))
- [func modifyRecordZones(saving: [CKRecordZone], deleting: [CKRecordZone.ID], completionHandler: (Result<(saveResults: [CKRecordZone.ID : Result<CKRecordZone, any Error>], deleteResults: [CKRecordZone.ID : Result<Void, any Error>]), any Error>) -> Void)](/documentation/cloudkit/ckdatabase/modifyrecordzones(saving:deleting:completionhandler:))
- [func save(CKRecordZone, completionHandler: (CKRecordZone?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/save(_:completionhandler:)-32ffr)
- [func delete(withRecordZoneID: CKRecordZone.ID, completionHandler: (CKRecordZone.ID?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/delete(withrecordzoneid:completionhandler:))

### Fetching Subscriptions

- [func subscriptions(for: [CKSubscription.ID]) async throws -> [CKSubscription.ID : Result<CKSubscription, any Error>]](/documentation/cloudkit/ckdatabase/subscriptions(for:))
- [func fetch(withSubscriptionIDs: [CKSubscription.ID], completionHandler: (Result<[CKSubscription.ID : Result<CKSubscription, any Error>], any Error>) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withsubscriptionids:completionhandler:))
- [func subscription(for: CKSubscription.ID) async throws -> CKSubscription](/documentation/cloudkit/ckdatabase/subscription(for:))
- [func fetch(withSubscriptionID: CKSubscription.ID, completionHandler: (CKSubscription?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/fetch(withsubscriptionid:completionhandler:))
- [func fetchAllSubscriptions(completionHandler: ([CKSubscription]?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/fetchallsubscriptions(completionhandler:))

### Modifying Subscriptions

- [func modifySubscriptions(saving: [CKSubscription], deleting: [CKSubscription.ID]) async throws -> (saveResults: [CKSubscription.ID : Result<CKSubscription, any Error>], deleteResults: [CKSubscription.ID : Result<Void, any Error>])](/documentation/cloudkit/ckdatabase/modifysubscriptions(saving:deleting:))
- [func modifySubscriptions(saving: [CKSubscription], deleting: [CKSubscription.ID], completionHandler: (Result<(saveResults: [CKSubscription.ID : Result<CKSubscription, any Error>], deleteResults: [CKSubscription.ID : Result<Void, any Error>]), any Error>) -> Void)](/documentation/cloudkit/ckdatabase/modifysubscriptions(saving:deleting:completionhandler:))
- [func save(CKSubscription, completionHandler: (CKSubscription?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/save(_:completionhandler:)-9pona)
- [func deleteSubscription(withID: CKSubscription.ID) async throws -> CKSubscription.ID](/documentation/cloudkit/ckdatabase/deletesubscription(withid:))
- [func delete(withSubscriptionID: CKSubscription.ID, completionHandler: (String?, (any Error)?) -> Void)](/documentation/cloudkit/ckdatabase/delete(withsubscriptionid:completionhandler:))

### Fetching Changes

- [func databaseChanges(since: CKServerChangeToken?, resultsLimit: Int?) async throws -> (modifications: [CKDatabase.DatabaseChange.Modification], deletions: [CKDatabase.DatabaseChange.Deletion], changeToken: CKServerChangeToken, moreComing: Bool)](/documentation/cloudkit/ckdatabase/databasechanges(since:resultslimit:))
- [func fetchDatabaseChanges(since: CKServerChangeToken?, resultsLimit: Int?, completionHandler: (Result<(modifications: [CKDatabase.DatabaseChange.Modification], deletions: [CKDatabase.DatabaseChange.Deletion], changeToken: CKServerChangeToken, moreComing: Bool), any Error>) -> Void)](/documentation/cloudkit/ckdatabase/fetchdatabasechanges(since:resultslimit:completionhandler:))
- [CKDatabase.DatabaseChange](/documentation/cloudkit/ckdatabase/databasechange)

#### Modifications

- [CKDatabase.DatabaseChange.Modification](/documentation/cloudkit/ckdatabase/databasechange/modification)

##### Identifying the Modified Record Zone

- [var zoneID: CKRecordZone.ID](/documentation/cloudkit/ckdatabase/databasechange/modification/zoneid)

#### Deletions

- [CKDatabase.DatabaseChange.Deletion](/documentation/cloudkit/ckdatabase/databasechange/deletion)

##### Identifying the Deleted Record Zone

- [var zoneID: CKRecordZone.ID](/documentation/cloudkit/ckdatabase/databasechange/deletion/zoneid)
- [var purged: Bool](/documentation/cloudkit/ckdatabase/databasechange/deletion/purged)

##### Instance Properties

- [var reason: CKDatabase.DatabaseChange.Deletion.Reason](/documentation/cloudkit/ckdatabase/databasechange/deletion/reason-swift.property)

##### Enumerations

- [CKDatabase.DatabaseChange.Deletion.Reason](/documentation/cloudkit/ckdatabase/databasechange/deletion/reason-swift.enum)

###### Enumeration Cases

- [case deleted](/documentation/cloudkit/ckdatabase/databasechange/deletion/reason-swift.enum/deleted)
- [case encryptedDataReset](/documentation/cloudkit/ckdatabase/databasechange/deletion/reason-swift.enum/encrypteddatareset)
- [case purged](/documentation/cloudkit/ckdatabase/databasechange/deletion/reason-swift.enum/purged)
- [func recordZoneChanges(inZoneWith: CKRecordZone.ID, since: CKServerChangeToken?, desiredKeys: [CKRecord.FieldKey]?, resultsLimit: Int?) async throws -> (modificationResultsByID: [CKRecord.ID : Result<CKDatabase.RecordZoneChange.Modification, any Error>], deletions: [CKDatabase.RecordZoneChange.Deletion], changeToken: CKServerChangeToken, moreComing: Bool)](/documentation/cloudkit/ckdatabase/recordzonechanges(inzonewith:since:desiredkeys:resultslimit:))
- [func fetchRecordZoneChanges(inZoneWith: CKRecordZone.ID, since: CKServerChangeToken?, desiredKeys: [CKRecord.FieldKey]?, resultsLimit: Int?, completionHandler: (Result<(modificationResultsByID: [CKRecord.ID : Result<CKDatabase.RecordZoneChange.Modification, any Error>], deletions: [CKDatabase.RecordZoneChange.Deletion], changeToken: CKServerChangeToken, moreComing: Bool), any Error>) -> Void)](/documentation/cloudkit/ckdatabase/fetchrecordzonechanges(inzonewith:since:desiredkeys:resultslimit:completionhandler:))
- [CKDatabase.RecordZoneChange](/documentation/cloudkit/ckdatabase/recordzonechange)

#### Modifications

- [CKDatabase.RecordZoneChange.Modification](/documentation/cloudkit/ckdatabase/recordzonechange/modification)

##### Getting the Modified Record

- [var record: CKRecord](/documentation/cloudkit/ckdatabase/recordzonechange/modification/record)

#### Deletions

- [CKDatabase.RecordZoneChange.Deletion](/documentation/cloudkit/ckdatabase/recordzonechange/deletion)

##### Identifying the Deleted Record

- [var recordID: CKRecord.ID](/documentation/cloudkit/ckdatabase/recordzonechange/deletion/recordid)
- [var recordType: CKRecord.RecordType](/documentation/cloudkit/ckdatabase/recordzonechange/deletion/recordtype)

### Running Operations

- [func add(CKDatabaseOperation)](/documentation/cloudkit/ckdatabase/add(_:))

### Getting the Database Type

- [var databaseScope: CKDatabase.Scope](/documentation/cloudkit/ckdatabase/databasescope)
- [CKDatabase.Scope](/documentation/cloudkit/ckdatabase/scope)

#### Database Scopes

- [case `public`](/documentation/cloudkit/ckdatabase/scope/public)
- [case `private`](/documentation/cloudkit/ckdatabase/scope/private)
- [case shared](/documentation/cloudkit/ckdatabase/scope/shared)

#### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckdatabase/scope/init(rawvalue:))
- [CKOperationGroup](/documentation/cloudkit/ckoperationgroup)

### Creating an Operation Group

- [init()](/documentation/cloudkit/ckoperationgroup/init())
- [init(coder: NSCoder)](/documentation/cloudkit/ckoperationgroup/init(coder:))

### Configuring an Operation Group

- [var defaultConfiguration: CKOperation.Configuration!](/documentation/cloudkit/ckoperationgroup/defaultconfiguration)
- [var expectedReceiveSize: CKOperationGroup.TransferSize](/documentation/cloudkit/ckoperationgroup/expectedreceivesize)
- [var expectedSendSize: CKOperationGroup.TransferSize](/documentation/cloudkit/ckoperationgroup/expectedsendsize)
- [var name: String?](/documentation/cloudkit/ckoperationgroup/name)
- [var operationGroupID: String](/documentation/cloudkit/ckoperationgroup/operationgroupid)
- [var quantity: Int](/documentation/cloudkit/ckoperationgroup/quantity)
- [CKOperationGroup.TransferSize](/documentation/cloudkit/ckoperationgroup/transfersize)

#### Transfer Sizes

- [case kilobytes](/documentation/cloudkit/ckoperationgroup/transfersize/kilobytes)
- [case megabytes](/documentation/cloudkit/ckoperationgroup/transfersize/megabytes)
- [case gigabytes](/documentation/cloudkit/ckoperationgroup/transfersize/gigabytes)
- [case tensOfMegabytes](/documentation/cloudkit/ckoperationgroup/transfersize/tensofmegabytes)
- [case tensOfGigabytes](/documentation/cloudkit/ckoperationgroup/transfersize/tensofgigabytes)
- [case hundredsOfMegabytes](/documentation/cloudkit/ckoperationgroup/transfersize/hundredsofmegabytes)
- [case hundredsOfGigabytes](/documentation/cloudkit/ckoperationgroup/transfersize/hundredsofgigabytes)
- [case unknown](/documentation/cloudkit/ckoperationgroup/transfersize/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckoperationgroup/transfersize/init(rawvalue:))

## Privacy

- [Encrypting User Data](/documentation/cloudkit/encrypting-user-data)
- [Providing User Access to CloudKit Data](/documentation/cloudkit/providing-user-access-to-cloudkit-data)
- [Changing Access Controls on User Data](/documentation/cloudkit/changing-access-controls-on-user-data)
- [CKFetchWebAuthTokenOperation](/documentation/cloudkit/ckfetchwebauthtokenoperation)

### Creating a Fetch Token Operation

- [convenience init(apiToken: String)](/documentation/cloudkit/ckfetchwebauthtokenoperation/init(apitoken:))
- [init()](/documentation/cloudkit/ckfetchwebauthtokenoperation/init())

### Managing the Operation’s Configuration

- [var apiToken: String?](/documentation/cloudkit/ckfetchwebauthtokenoperation/apitoken)
- [var fetchWebAuthTokenCompletionBlock: ((String?, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchwebauthtokenoperation/fetchwebauthtokencompletionblock)

### Instance Properties

- [var fetchWebAuthTokenResultBlock: ((Result<String, any Error>) -> Void)?](/documentation/cloudkit/ckfetchwebauthtokenoperation/fetchwebauthtokenresultblock)
- [Responding to Requests to Delete Data](/documentation/cloudkit/responding-to-requests-to-delete-data)
- [Identifying an App’s Containers](/documentation/cloudkit/identifying-an-app-s-containers)

## Errors

- [let CKErrorDomain: String](/documentation/cloudkit/ckerrordomain)
- [CKError](/documentation/cloudkit/ckerror)

### Getting Error Codes

- [static var accountTemporarilyUnavailable: CKError.Code](/documentation/cloudkit/ckerror/accounttemporarilyunavailable)
- [static var alreadyShared: CKError.Code](/documentation/cloudkit/ckerror/alreadyshared)
- [static var assetFileModified: CKError.Code](/documentation/cloudkit/ckerror/assetfilemodified)
- [static var assetFileNotFound: CKError.Code](/documentation/cloudkit/ckerror/assetfilenotfound)
- [static var assetNotAvailable: CKError.Code](/documentation/cloudkit/ckerror/assetnotavailable)
- [static var badContainer: CKError.Code](/documentation/cloudkit/ckerror/badcontainer)
- [static var badDatabase: CKError.Code](/documentation/cloudkit/ckerror/baddatabase)
- [static var batchRequestFailed: CKError.Code](/documentation/cloudkit/ckerror/batchrequestfailed)
- [static var changeTokenExpired: CKError.Code](/documentation/cloudkit/ckerror/changetokenexpired)
- [static var constraintViolation: CKError.Code](/documentation/cloudkit/ckerror/constraintviolation)
- [static var incompatibleVersion: CKError.Code](/documentation/cloudkit/ckerror/incompatibleversion)
- [static var internalError: CKError.Code](/documentation/cloudkit/ckerror/internalerror)
- [static var invalidArguments: CKError.Code](/documentation/cloudkit/ckerror/invalidarguments)
- [static var limitExceeded: CKError.Code](/documentation/cloudkit/ckerror/limitexceeded)
- [static var managedAccountRestricted: CKError.Code](/documentation/cloudkit/ckerror/managedaccountrestricted)
- [static var missingEntitlement: CKError.Code](/documentation/cloudkit/ckerror/missingentitlement)
- [static var networkFailure: CKError.Code](/documentation/cloudkit/ckerror/networkfailure)
- [static var networkUnavailable: CKError.Code](/documentation/cloudkit/ckerror/networkunavailable)
- [static var notAuthenticated: CKError.Code](/documentation/cloudkit/ckerror/notauthenticated)
- [static var operationCancelled: CKError.Code](/documentation/cloudkit/ckerror/operationcancelled)
- [static var partialFailure: CKError.Code](/documentation/cloudkit/ckerror/partialfailure)
- [static var participantMayNeedVerification: CKError.Code](/documentation/cloudkit/ckerror/participantmayneedverification)
- [static var permissionFailure: CKError.Code](/documentation/cloudkit/ckerror/permissionfailure)
- [static var quotaExceeded: CKError.Code](/documentation/cloudkit/ckerror/quotaexceeded)
- [static var referenceViolation: CKError.Code](/documentation/cloudkit/ckerror/referenceviolation)
- [static var requestRateLimited: CKError.Code](/documentation/cloudkit/ckerror/requestratelimited)
- [static var serverRecordChanged: CKError.Code](/documentation/cloudkit/ckerror/serverrecordchanged)
- [static var serverRejectedRequest: CKError.Code](/documentation/cloudkit/ckerror/serverrejectedrequest)
- [static var serverResponseLost: CKError.Code](/documentation/cloudkit/ckerror/serverresponselost)
- [static var serviceUnavailable: CKError.Code](/documentation/cloudkit/ckerror/serviceunavailable)
- [static var tooManyParticipants: CKError.Code](/documentation/cloudkit/ckerror/toomanyparticipants)
- [static var unknownItem: CKError.Code](/documentation/cloudkit/ckerror/unknownitem)
- [static var userDeletedZone: CKError.Code](/documentation/cloudkit/ckerror/userdeletedzone)
- [static var zoneBusy: CKError.Code](/documentation/cloudkit/ckerror/zonebusy)
- [static var zoneNotFound: CKError.Code](/documentation/cloudkit/ckerror/zonenotfound)
- [static var resultsTruncated: CKError.Code](/documentation/cloudkit/ckerror/resultstruncated)
- [CKError.Code](/documentation/cloudkit/ckerror/code)

#### Error Codes

- [case accountTemporarilyUnavailable](/documentation/cloudkit/ckerror/code/accounttemporarilyunavailable)
- [case alreadyShared](/documentation/cloudkit/ckerror/code/alreadyshared)
- [case assetFileModified](/documentation/cloudkit/ckerror/code/assetfilemodified)
- [case assetFileNotFound](/documentation/cloudkit/ckerror/code/assetfilenotfound)
- [case assetNotAvailable](/documentation/cloudkit/ckerror/code/assetnotavailable)
- [case badContainer](/documentation/cloudkit/ckerror/code/badcontainer)
- [case badDatabase](/documentation/cloudkit/ckerror/code/baddatabase)
- [case batchRequestFailed](/documentation/cloudkit/ckerror/code/batchrequestfailed)
- [case changeTokenExpired](/documentation/cloudkit/ckerror/code/changetokenexpired)
- [case constraintViolation](/documentation/cloudkit/ckerror/code/constraintviolation)
- [case incompatibleVersion](/documentation/cloudkit/ckerror/code/incompatibleversion)
- [case internalError](/documentation/cloudkit/ckerror/code/internalerror)
- [case invalidArguments](/documentation/cloudkit/ckerror/code/invalidarguments)
- [case limitExceeded](/documentation/cloudkit/ckerror/code/limitexceeded)
- [case managedAccountRestricted](/documentation/cloudkit/ckerror/code/managedaccountrestricted)
- [case missingEntitlement](/documentation/cloudkit/ckerror/code/missingentitlement)
- [case networkFailure](/documentation/cloudkit/ckerror/code/networkfailure)
- [case networkUnavailable](/documentation/cloudkit/ckerror/code/networkunavailable)
- [case notAuthenticated](/documentation/cloudkit/ckerror/code/notauthenticated)
- [case operationCancelled](/documentation/cloudkit/ckerror/code/operationcancelled)
- [case partialFailure](/documentation/cloudkit/ckerror/code/partialfailure)
- [case participantMayNeedVerification](/documentation/cloudkit/ckerror/code/participantmayneedverification)
- [case permissionFailure](/documentation/cloudkit/ckerror/code/permissionfailure)
- [case quotaExceeded](/documentation/cloudkit/ckerror/code/quotaexceeded)
- [case referenceViolation](/documentation/cloudkit/ckerror/code/referenceviolation)
- [case requestRateLimited](/documentation/cloudkit/ckerror/code/requestratelimited)
- [case serverRecordChanged](/documentation/cloudkit/ckerror/code/serverrecordchanged)
- [case serverRejectedRequest](/documentation/cloudkit/ckerror/code/serverrejectedrequest)
- [case serverResponseLost](/documentation/cloudkit/ckerror/code/serverresponselost)
- [case serviceUnavailable](/documentation/cloudkit/ckerror/code/serviceunavailable)
- [case tooManyParticipants](/documentation/cloudkit/ckerror/code/toomanyparticipants)
- [case unknownItem](/documentation/cloudkit/ckerror/code/unknownitem)
- [case userDeletedZone](/documentation/cloudkit/ckerror/code/userdeletedzone)
- [case zoneBusy](/documentation/cloudkit/ckerror/code/zonebusy)
- [case zoneNotFound](/documentation/cloudkit/ckerror/code/zonenotfound)
- [case resultsTruncated](/documentation/cloudkit/ckerror/code/resultstruncated)

#### Enumeration Cases

- [case participantAlreadyInvited](/documentation/cloudkit/ckerror/code/participantalreadyinvited)

#### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckerror/code/init(rawvalue:))

### Getting Partial Errors

- [var partialErrorsByItemID: [AnyHashable : any Error]?](/documentation/cloudkit/ckerror/partialerrorsbyitemid)

### Getting Conflicted Records

- [var ancestorRecord: CKRecord?](/documentation/cloudkit/ckerror/ancestorrecord)
- [var clientRecord: CKRecord?](/documentation/cloudkit/ckerror/clientrecord)
- [var serverRecord: CKRecord?](/documentation/cloudkit/ckerror/serverrecord)

### Getting Retry Information

- [var retryAfterSeconds: Double?](/documentation/cloudkit/ckerror/retryafterseconds)

### Type Properties

- [static var errorDomain: String](/documentation/cloudkit/ckerror/errordomain)
- [static var participantAlreadyInvited: CKError.Code](/documentation/cloudkit/ckerror/participantalreadyinvited)
- [CKError.Code](/documentation/cloudkit/ckerror/code)

### Error Codes

- [case accountTemporarilyUnavailable](/documentation/cloudkit/ckerror/code/accounttemporarilyunavailable)
- [case alreadyShared](/documentation/cloudkit/ckerror/code/alreadyshared)
- [case assetFileModified](/documentation/cloudkit/ckerror/code/assetfilemodified)
- [case assetFileNotFound](/documentation/cloudkit/ckerror/code/assetfilenotfound)
- [case assetNotAvailable](/documentation/cloudkit/ckerror/code/assetnotavailable)
- [case badContainer](/documentation/cloudkit/ckerror/code/badcontainer)
- [case badDatabase](/documentation/cloudkit/ckerror/code/baddatabase)
- [case batchRequestFailed](/documentation/cloudkit/ckerror/code/batchrequestfailed)
- [case changeTokenExpired](/documentation/cloudkit/ckerror/code/changetokenexpired)
- [case constraintViolation](/documentation/cloudkit/ckerror/code/constraintviolation)
- [case incompatibleVersion](/documentation/cloudkit/ckerror/code/incompatibleversion)
- [case internalError](/documentation/cloudkit/ckerror/code/internalerror)
- [case invalidArguments](/documentation/cloudkit/ckerror/code/invalidarguments)
- [case limitExceeded](/documentation/cloudkit/ckerror/code/limitexceeded)
- [case managedAccountRestricted](/documentation/cloudkit/ckerror/code/managedaccountrestricted)
- [case missingEntitlement](/documentation/cloudkit/ckerror/code/missingentitlement)
- [case networkFailure](/documentation/cloudkit/ckerror/code/networkfailure)
- [case networkUnavailable](/documentation/cloudkit/ckerror/code/networkunavailable)
- [case notAuthenticated](/documentation/cloudkit/ckerror/code/notauthenticated)
- [case operationCancelled](/documentation/cloudkit/ckerror/code/operationcancelled)
- [case partialFailure](/documentation/cloudkit/ckerror/code/partialfailure)
- [case participantMayNeedVerification](/documentation/cloudkit/ckerror/code/participantmayneedverification)
- [case permissionFailure](/documentation/cloudkit/ckerror/code/permissionfailure)
- [case quotaExceeded](/documentation/cloudkit/ckerror/code/quotaexceeded)
- [case referenceViolation](/documentation/cloudkit/ckerror/code/referenceviolation)
- [case requestRateLimited](/documentation/cloudkit/ckerror/code/requestratelimited)
- [case serverRecordChanged](/documentation/cloudkit/ckerror/code/serverrecordchanged)
- [case serverRejectedRequest](/documentation/cloudkit/ckerror/code/serverrejectedrequest)
- [case serverResponseLost](/documentation/cloudkit/ckerror/code/serverresponselost)
- [case serviceUnavailable](/documentation/cloudkit/ckerror/code/serviceunavailable)
- [case tooManyParticipants](/documentation/cloudkit/ckerror/code/toomanyparticipants)
- [case unknownItem](/documentation/cloudkit/ckerror/code/unknownitem)
- [case userDeletedZone](/documentation/cloudkit/ckerror/code/userdeletedzone)
- [case zoneBusy](/documentation/cloudkit/ckerror/code/zonebusy)
- [case zoneNotFound](/documentation/cloudkit/ckerror/code/zonenotfound)
- [case resultsTruncated](/documentation/cloudkit/ckerror/code/resultstruncated)

### Enumeration Cases

- [case participantAlreadyInvited](/documentation/cloudkit/ckerror/code/participantalreadyinvited)

### Initializers

- [init?(rawValue: Int)](/documentation/cloudkit/ckerror/code/init(rawvalue:))
- [let CKErrorRetryAfterKey: String](/documentation/cloudkit/ckerrorretryafterkey)
- [let CKErrorUserDidResetEncryptedDataKey: String](/documentation/cloudkit/ckerroruserdidresetencrypteddatakey)
- [let CKPartialErrorsByItemIDKey: String](/documentation/cloudkit/ckpartialerrorsbyitemidkey)
- [Record Changed Error Keys](/documentation/cloudkit/record-changed-error-keys)

### Record Changed Error Keys

- [let CKRecordChangedErrorAncestorRecordKey: String](/documentation/cloudkit/ckrecordchangederrorancestorrecordkey)
- [let CKRecordChangedErrorClientRecordKey: String](/documentation/cloudkit/ckrecordchangederrorclientrecordkey)
- [let CKRecordChangedErrorServerRecordKey: String](/documentation/cloudkit/ckrecordchangederrorserverrecordkey)

## Deprecated

- [Deprecated Symbols](/documentation/cloudkit/deprecated-symbols)

### Deprecated classes

- [CKDiscoverAllUserIdentitiesOperation](/documentation/cloudkit/ckdiscoveralluseridentitiesoperation)

#### Creating an Operation

- [init()](/documentation/cloudkit/ckdiscoveralluseridentitiesoperation/init())

#### Processing the Operation Results

- [var userIdentityDiscoveredBlock: ((CKUserIdentity) -> Void)?](/documentation/cloudkit/ckdiscoveralluseridentitiesoperation/useridentitydiscoveredblock)
- [var discoverAllUserIdentitiesCompletionBlock: (((any Error)?) -> Void)?](/documentation/cloudkit/ckdiscoveralluseridentitiesoperation/discoveralluseridentitiescompletionblock)

#### Instance Properties

- [var discoverAllUserIdentitiesResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckdiscoveralluseridentitiesoperation/discoveralluseridentitiesresultblock)
- [CKDiscoverUserIdentitiesOperation](/documentation/cloudkit/ckdiscoveruseridentitiesoperation)

#### Creating an Operation

- [init()](/documentation/cloudkit/ckdiscoveruseridentitiesoperation/init())
- [convenience init(userIdentityLookupInfos: [CKUserIdentity.LookupInfo])](/documentation/cloudkit/ckdiscoveruseridentitiesoperation/init(useridentitylookupinfos:))

#### Configuring the Operation

- [var userIdentityLookupInfos: [CKUserIdentity.LookupInfo]](/documentation/cloudkit/ckdiscoveruseridentitiesoperation/useridentitylookupinfos)

#### Processing the Results

- [var userIdentityDiscoveredBlock: ((CKUserIdentity, CKUserIdentity.LookupInfo) -> Void)?](/documentation/cloudkit/ckdiscoveruseridentitiesoperation/useridentitydiscoveredblock)
- [var discoverUserIdentitiesCompletionBlock: (((any Error)?) -> Void)?](/documentation/cloudkit/ckdiscoveruseridentitiesoperation/discoveruseridentitiescompletionblock)

#### Instance Properties

- [var discoverUserIdentitiesResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/ckdiscoveruseridentitiesoperation/discoveruseridentitiesresultblock)
- [CKFetchRecordChangesOperation](/documentation/cloudkit/ckfetchrecordchangesoperation)

#### Creating the Fetch Record Changes Operation

- [convenience init(recordZoneID: CKRecordZone.ID, previousServerChangeToken: CKServerChangeToken?)](/documentation/cloudkit/ckfetchrecordchangesoperation/init(recordzoneid:previousserverchangetoken:))
- [init()](/documentation/cloudkit/ckfetchrecordchangesoperation/init())

#### Configuring the Fetch Record Changes Operation

- [var recordZoneID: CKRecordZone.ID?](/documentation/cloudkit/ckfetchrecordchangesoperation/recordzoneid)
- [var previousServerChangeToken: CKServerChangeToken?](/documentation/cloudkit/ckfetchrecordchangesoperation/previousserverchangetoken)
- [var desiredKeys: [String]?](/documentation/cloudkit/ckfetchrecordchangesoperation/desiredkeys)
- [var resultsLimit: Int](/documentation/cloudkit/ckfetchrecordchangesoperation/resultslimit)
- [var moreComing: Bool](/documentation/cloudkit/ckfetchrecordchangesoperation/morecoming)

#### Processing the Fetch Record Changes Results

- [var recordChangedBlock: ((CKRecord) -> Void)?](/documentation/cloudkit/ckfetchrecordchangesoperation/recordchangedblock)
- [var recordWithIDWasDeletedBlock: ((CKRecord.ID) -> Void)?](/documentation/cloudkit/ckfetchrecordchangesoperation/recordwithidwasdeletedblock)
- [var fetchRecordChangesCompletionBlock: ((CKServerChangeToken?, Data?, (any Error)?) -> Void)?](/documentation/cloudkit/ckfetchrecordchangesoperation/fetchrecordchangescompletionblock)

### Deprecated type aliases

- [CKContainer_Application_PermissionBlock](/documentation/cloudkit/ckcontainer_application_permissionblock)
- [CKContainer_Application_PermissionStatus](/documentation/cloudkit/ckcontainer_application_permissionstatus)
- [CKContainer_Application_Permissions](/documentation/cloudkit/ckcontainer_application_permissions)
- [CKRecord_Reference_Action](/documentation/cloudkit/ckrecord_reference_action)
- [CKShare_Participant_AcceptanceStatus](/documentation/cloudkit/ckshare_participant_acceptancestatus)
- [CKShare_Participant_ParticipantType](/documentation/cloudkit/ckshare_participant_participanttype)
- [CKShare_Participant_Permission](/documentation/cloudkit/ckshare_participant_permission)
- [CKShare_Participant_Role](/documentation/cloudkit/ckshare_participant_role)

## Classes

- [CKShareRequestAccessOperation](/documentation/cloudkit/cksharerequestaccessoperation)

### Initializers

- [init()](/documentation/cloudkit/cksharerequestaccessoperation/init())
- [convenience init(shareURLs: [URL])](/documentation/cloudkit/cksharerequestaccessoperation/init(shareurls:))

### Instance Properties

- [var perShareAccessRequestResultBlock: ((URL, Result<Void, any Error>) -> Void)?](/documentation/cloudkit/cksharerequestaccessoperation/pershareaccessrequestresultblock)
- [var shareAccessRequestResultBlock: ((Result<Void, any Error>) -> Void)?](/documentation/cloudkit/cksharerequestaccessoperation/shareaccessrequestresultblock)
- [var shareURLs: [URL]?](/documentation/cloudkit/cksharerequestaccessoperation/shareurls)

## Variables

- [let CKRecordParentKey: String](/documentation/cloudkit/ckrecordparentkey-1elhg)
- [let CKRecordShareKey: String](/documentation/cloudkit/ckrecordsharekey-gc8w)
- [let CKRecordTypeShare: String](/documentation/cloudkit/ckrecordtypeshare-7lec1)
- [let CKRecordTypeUserRecord: String](/documentation/cloudkit/ckrecordtypeuserrecord-6iwgn)
- [let CKRecordZoneDefaultName: String](/documentation/cloudkit/ckrecordzonedefaultname-1uuiu)
- [let CKShareThumbnailImageDataKey: String](/documentation/cloudkit/cksharethumbnailimagedatakey-rxjd)
- [let CKShareTitleKey: String](/documentation/cloudkit/cksharetitlekey-1cs9j)
- [let CKShareTypeKey: String](/documentation/cloudkit/cksharetypekey-5m83p)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
