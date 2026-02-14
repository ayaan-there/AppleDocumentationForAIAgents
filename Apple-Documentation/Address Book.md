# Address Book Documentation

Source: https://sosumi.ai/documentation/addressbook

---
title: Address Book
source: https://developer.apple.com/documentation/addressbook
timestamp: 2026-02-13T19:06:40.275Z
---

## Essentials

- [ABAddressBook](/documentation/addressbook/abaddressbook)

### Creating and Initializing an Address Book

- [class func shared() -> ABAddressBook!](/documentation/addressbook/abaddressbook/shared())

### Retrieving Groups and People

- [func groups() -> [Any]!](/documentation/addressbook/abaddressbook/groups())
- [func people() -> [Any]!](/documentation/addressbook/abaddressbook/people())

### Setting and Retrieving the Logged-in User’s Record

- [func me() -> ABPerson!](/documentation/addressbook/abaddressbook/me())
- [func setMe(ABPerson!)](/documentation/addressbook/abaddressbook/setme(_:))

### Retrieving a Specific Record

- [func record(forUniqueId: String!) -> ABRecord!](/documentation/addressbook/abaddressbook/record(foruniqueid:))

### Retrieving the Class of a Record

- [func recordClass(fromUniqueId: String!) -> String!](/documentation/addressbook/abaddressbook/recordclass(fromuniqueid:))

### Retrieving a Formatted Address

- [func formattedAddress(from: [AnyHashable : Any]!) -> NSAttributedString!](/documentation/addressbook/abaddressbook/formattedaddress(from:))

### Retrieving Default Values

- [func defaultCountryCode() -> String!](/documentation/addressbook/abaddressbook/defaultcountrycode())
- [func defaultNameOrdering() -> Int](/documentation/addressbook/abaddressbook/defaultnameordering())

### Adding and Removing Records

- [func add(ABRecord!, error: ()) throws](/documentation/addressbook/abaddressbook/add(_:error:))
- [func add(ABRecord!) -> Bool](/documentation/addressbook/abaddressbook/add(_:))
- [func remove(ABRecord!, error: ()) throws](/documentation/addressbook/abaddressbook/remove(_:error:))
- [func remove(ABRecord!) -> Bool](/documentation/addressbook/abaddressbook/remove(_:))

### Searching

- [func records(matching: ABSearchElement!) -> [Any]!](/documentation/addressbook/abaddressbook/records(matching:))

### Saving and Detecting Changes

- [func hasUnsavedChanges() -> Bool](/documentation/addressbook/abaddressbook/hasunsavedchanges())
- [func save() -> Bool](/documentation/addressbook/abaddressbook/save())
- [func saveAndReturnError() throws](/documentation/addressbook/abaddressbook/saveandreturnerror())

### Constants

- [Database change notification keys](/documentation/addressbook/database-change-notification-keys)

#### Constants

- [let kABInsertedRecords: String](/documentation/addressbook/kabinsertedrecords)
- [let kABUpdatedRecords: String](/documentation/addressbook/kabupdatedrecords)
- [let kABDeletedRecords: String](/documentation/addressbook/kabdeletedrecords)
- [Errors](/documentation/addressbook/1529225-errors)

#### Constants

- [var ABAddRecordsError: Int](/documentation/addressbook/abaddrecordserror)
- [var ABRemoveRecordsError: Int](/documentation/addressbook/abremoverecordserror)
- [var ABPropertyValueValidationError: Int](/documentation/addressbook/abpropertyvaluevalidationerror)
- [var ABPropertyUnsupportedBySourceError: Int](/documentation/addressbook/abpropertyunsupportedbysourceerror)
- [var ABPropertyReadOnlyError: Int](/documentation/addressbook/abpropertyreadonlyerror)

### Notifications

- [static let abDatabaseChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/abdatabasechanged)
- [static let abDatabaseChangedExternally: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/abdatabasechangedexternally)

## Data Types

- [ABPerson](/documentation/addressbook/abperson)

### Managing Properties

- [class func addPropertiesAndTypes([AnyHashable : Any]!) -> Int](/documentation/addressbook/abperson/addpropertiesandtypes(_:))
- [class func removeProperties([Any]!) -> Int](/documentation/addressbook/abperson/removeproperties(_:))
- [class func properties() -> [Any]!](/documentation/addressbook/abperson/properties())
- [class func type(ofProperty: String!) -> ABPropertyType](/documentation/addressbook/abperson/type(ofproperty:))

### Managing Linked People

- [func linkedPeople() -> [Any]!](/documentation/addressbook/abperson/linkedpeople())

### Managing Groups

- [func parentGroups() -> [Any]!](/documentation/addressbook/abperson/parentgroups())

### Managing Images

- [class func cancelLoadingImageData(forTag: Int)](/documentation/addressbook/abperson/cancelloadingimagedata(fortag:))
- [func beginLoadingImageData(for: (any ABImageClient)!) -> Int](/documentation/addressbook/abperson/beginloadingimagedata(for:))
- [func imageData() -> Data!](/documentation/addressbook/abperson/imagedata())
- [func setImageData(Data!) -> Bool](/documentation/addressbook/abperson/setimagedata(_:))

### Searching

- [class func searchElement(forProperty: String!, label: String!, key: String!, value: Any!, comparison: ABSearchComparison) -> ABSearchElement!](/documentation/addressbook/abperson/searchelement(forproperty:label:key:value:comparison:))

### Importing and Exporting vCard Formatted Files

- [init!(VCardRepresentation: Data!)](/documentation/addressbook/abperson/init(vcardrepresentation:))
- [func vCardRepresentation() -> Data!](/documentation/addressbook/abperson/vcardrepresentation())

### Constants

- [Person Flags](/documentation/addressbook/person-flags)

#### Constants

- [var kABShowAsMask: Int32](/documentation/addressbook/kabshowasmask)
- [var kABShowAsPerson: Int32](/documentation/addressbook/kabshowasperson)
- [var kABShowAsCompany: Int32](/documentation/addressbook/kabshowascompany)
- [var kABShowAsResource: Int32](/documentation/addressbook/kabshowasresource)
- [var kABShowAsRoom: Int32](/documentation/addressbook/kabshowasroom)
- [var kABNameOrderingMask: Int32](/documentation/addressbook/kabnameorderingmask)
- [var kABDefaultNameOrdering: Int32](/documentation/addressbook/kabdefaultnameordering)
- [var kABFirstNameFirst: Int32](/documentation/addressbook/kabfirstnamefirst)
- [var kABLastNameFirst: Int32](/documentation/addressbook/kablastnamefirst)
- [ABGroup](/documentation/addressbook/abgroup)

### Managing properties

- [class func addPropertiesAndTypes([AnyHashable : Any]!) -> Int](/documentation/addressbook/abgroup/addpropertiesandtypes(_:))
- [class func removeProperties([Any]!) -> Int](/documentation/addressbook/abgroup/removeproperties(_:))
- [class func properties() -> [Any]!](/documentation/addressbook/abgroup/properties())
- [class func type(ofProperty: String!) -> ABPropertyType](/documentation/addressbook/abgroup/type(ofproperty:))

### Managing persons

- [func addMember(ABPerson!) -> Bool](/documentation/addressbook/abgroup/addmember(_:))
- [func removeMember(ABPerson!) -> Bool](/documentation/addressbook/abgroup/removemember(_:))
- [func members() -> [Any]!](/documentation/addressbook/abgroup/members())

### Managing subgroups

- [func addSubgroup(ABGroup!) -> Bool](/documentation/addressbook/abgroup/addsubgroup(_:))
- [func removeSubgroup(ABGroup!) -> Bool](/documentation/addressbook/abgroup/removesubgroup(_:))
- [func parentGroups() -> [Any]!](/documentation/addressbook/abgroup/parentgroups())
- [func subgroups() -> [Any]!](/documentation/addressbook/abgroup/subgroups())

### Managing Distribution Lists

- [func distributionIdentifier(forProperty: String!, person: ABPerson!) -> String!](/documentation/addressbook/abgroup/distributionidentifier(forproperty:person:))
- [func setDistributionIdentifier(String!, forProperty: String!, person: ABPerson!) -> Bool](/documentation/addressbook/abgroup/setdistributionidentifier(_:forproperty:person:))

### Searching

- [class func searchElement(forProperty: String!, label: String!, key: String!, value: Any!, comparison: ABSearchComparison) -> ABSearchElement!](/documentation/addressbook/abgroup/searchelement(forproperty:label:key:value:comparison:))
- [ABMultiValue](/documentation/addressbook/abmultivalue)

### Accessing the primary identifier

- [func primaryIdentifier() -> String!](/documentation/addressbook/abmultivalue/primaryidentifier())

### Accessing identifiers

- [func identifier(at: Int) -> String!](/documentation/addressbook/abmultivalue/identifier(at:))
- [func index(forIdentifier: String!) -> Int](/documentation/addressbook/abmultivalue/index(foridentifier:))

### Accessing entries

- [func label(at: Int) -> String!](/documentation/addressbook/abmultivalue/label(at:))
- [func value(at: Int) -> Any!](/documentation/addressbook/abmultivalue/value(at:))
- [func value(forIdentifier: String!) -> Any!](/documentation/addressbook/abmultivalue/value(foridentifier:))
- [func label(forIdentifier: String!) -> Any!](/documentation/addressbook/abmultivalue/label(foridentifier:))

### Querying the list

- [func count() -> Int](/documentation/addressbook/abmultivalue/count())
- [func propertyType() -> ABPropertyType](/documentation/addressbook/abmultivalue/propertytype())
- [ABMutableMultiValue](/documentation/addressbook/abmutablemultivalue)

### Adding a value

- [func add(Any!, withLabel: String!) -> String!](/documentation/addressbook/abmutablemultivalue/add(_:withlabel:))
- [func insert(Any!, withLabel: String!, at: Int) -> String!](/documentation/addressbook/abmutablemultivalue/insert(_:withlabel:at:))

### Replacing values and labels

- [func replaceLabel(at: Int, withLabel: String!) -> Bool](/documentation/addressbook/abmutablemultivalue/replacelabel(at:withlabel:))
- [func replace(at: Int, withValue: Any!) -> Bool](/documentation/addressbook/abmutablemultivalue/replace(at:withvalue:))

### Removing values

- [func removeAndLabel(at: Int) -> Bool](/documentation/addressbook/abmutablemultivalue/removeandlabel(at:))

### Setting the Primary identifier

- [func setPrimaryIdentifier(String!) -> Bool](/documentation/addressbook/abmutablemultivalue/setprimaryidentifier(_:))
- [ABImageClient](/documentation/addressbook/abimageclient)

### Loading an image

- [func consumeImageData(Data!, forTag: Int)](/documentation/addressbook/abimageclient/consumeimagedata(_:fortag:))
- [ABRecord](/documentation/addressbook/abrecord)

### Creating a Record

- [init!(addressBook: ABAddressBook!)](/documentation/addressbook/abrecord/init(addressbook:))
- [init!()](/documentation/addressbook/abrecord/init())

### Retrieving and Setting Values

- [func removeValue(forProperty: String!) -> Bool](/documentation/addressbook/abrecord/removevalue(forproperty:))
- [func setValue(Any!, forProperty: String!) -> Bool](/documentation/addressbook/abrecord/setvalue(_:forproperty:))
- [func setValue(Any!, forProperty: String!, error: ()) throws](/documentation/addressbook/abrecord/setvalue(_:forproperty:error:))
- [func value(forProperty: String!) -> Any!](/documentation/addressbook/abrecord/value(forproperty:))

### Retrieving a Specific Record

- [func isReadOnly() -> Bool](/documentation/addressbook/abrecord/isreadonly())

### Getting Identifying Information

- [var displayName: String!](/documentation/addressbook/abrecord/displayname)
- [var uniqueId: String!](/documentation/addressbook/abrecord/uniqueid)

## Pickers

- [ABPeoplePickerView](/documentation/addressbook/abpeoplepickerview)

### Working with Properties in the Record List

- [func addProperty(String!)](/documentation/addressbook/abpeoplepickerview/addproperty(_:))
- [func columnTitle(forProperty: String!) -> String!](/documentation/addressbook/abpeoplepickerview/columntitle(forproperty:))
- [var displayedProperty: String!](/documentation/addressbook/abpeoplepickerview/displayedproperty)
- [func properties() -> [Any]!](/documentation/addressbook/abpeoplepickerview/properties())
- [func removeProperty(String!)](/documentation/addressbook/abpeoplepickerview/removeproperty(_:))
- [func setColumnTitle(String!, forProperty: String!)](/documentation/addressbook/abpeoplepickerview/setcolumntitle(_:forproperty:))

### Specifying Selection Behavior

- [var valueSelectionBehavior: ABPeoplePickerSelectionBehavior](/documentation/addressbook/abpeoplepickerview/valueselectionbehavior)
- [ABPeoplePickerSelectionBehavior](/documentation/addressbook/abpeoplepickerselectionbehavior)

#### Selection Behaviors

- [var ABNoValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/abnovalueselection)
- [var ABSingleValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/absinglevalueselection)
- [var ABMultipleValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/abmultiplevalueselection)

#### Initializers

- [init(UInt32)](/documentation/addressbook/abpeoplepickerselectionbehavior/init(_:))
- [init(rawValue: UInt32)](/documentation/addressbook/abpeoplepickerselectionbehavior/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/addressbook/abpeoplepickerselectionbehavior/rawvalue)

### Selecting Groups and Records

- [var allowsGroupSelection: Bool](/documentation/addressbook/abpeoplepickerview/allowsgroupselection)
- [var allowsMultipleSelection: Bool](/documentation/addressbook/abpeoplepickerview/allowsmultipleselection)
- [func deselectAll(Any!)](/documentation/addressbook/abpeoplepickerview/deselectall(_:))
- [func deselect(ABGroup!)](/documentation/addressbook/abpeoplepickerview/deselect(_:)-3x7tl)
- [func deselectIdentifier(String!, for: ABPerson!)](/documentation/addressbook/abpeoplepickerview/deselectidentifier(_:for:))
- [func deselect(ABRecord!)](/documentation/addressbook/abpeoplepickerview/deselect(_:)-1yy11)
- [var selectedGroups: [Any]!](/documentation/addressbook/abpeoplepickerview/selectedgroups)
- [func selectedIdentifiers(for: ABPerson!) -> [Any]!](/documentation/addressbook/abpeoplepickerview/selectedidentifiers(for:))
- [var selectedRecords: [Any]!](/documentation/addressbook/abpeoplepickerview/selectedrecords)
- [func selectedValues() -> [Any]!](/documentation/addressbook/abpeoplepickerview/selectedvalues())
- [func select(ABGroup!, byExtendingSelection: Bool)](/documentation/addressbook/abpeoplepickerview/select(_:byextendingselection:)-6mrii)
- [func selectIdentifier(String!, for: ABPerson!, byExtendingSelection: Bool)](/documentation/addressbook/abpeoplepickerview/selectidentifier(_:for:byextendingselection:))
- [func select(ABRecord!, byExtendingSelection: Bool)](/documentation/addressbook/abpeoplepickerview/select(_:byextendingselection:)-9eldk)

### Specifying the Accessory View

- [var accessoryView: NSView!](/documentation/addressbook/abpeoplepickerview/accessoryview)

### Managing Actions

- [func clearSearchField(Any!)](/documentation/addressbook/abpeoplepickerview/clearsearchfield(_:))
- [func editInAddressBook(Any!)](/documentation/addressbook/abpeoplepickerview/editinaddressbook(_:))
- [var groupDoubleAction: Selector!](/documentation/addressbook/abpeoplepickerview/groupdoubleaction)
- [var nameDoubleAction: Selector!](/documentation/addressbook/abpeoplepickerview/namedoubleaction)
- [func selectInAddressBook(Any!)](/documentation/addressbook/abpeoplepickerview/selectinaddressbook(_:))
- [var target: AnyObject!](/documentation/addressbook/abpeoplepickerview/target)

### Managing Persistent User Settings

- [var autosaveName: String!](/documentation/addressbook/abpeoplepickerview/autosavename)
- [ABPersonView](/documentation/addressbook/abpersonview)

### Working with Person Views

- [var editing: Bool](/documentation/addressbook/abpersonview/editing)
- [var person: ABPerson!](/documentation/addressbook/abpersonview/person)
- [var shouldShowLinkedPeople: Bool](/documentation/addressbook/abpersonview/shouldshowlinkedpeople)

## Search Elements

- [ABSearchElement](/documentation/addressbook/absearchelement)

### Searching

- [init!(forConjunction: ABSearchConjunction, children: [Any]!)](/documentation/addressbook/absearchelement/init(forconjunction:children:))

### Matching

- [func matchesRecord(ABRecord!) -> Bool](/documentation/addressbook/absearchelement/matchesrecord(_:))

### Constants

- [ABSearchConjunction](/documentation/addressbook/absearchconjunction)

#### Constants

- [var kABSearchAnd: _ABSearchConjunction](/documentation/addressbook/kabsearchand)
- [var kABSearchOr: _ABSearchConjunction](/documentation/addressbook/kabsearchor)
- [ABSearchComparison](/documentation/addressbook/absearchcomparison)

#### Constants

- [var kABEqual: _ABSearchComparison](/documentation/addressbook/kabequal)
- [var kABNotEqual: _ABSearchComparison](/documentation/addressbook/kabnotequal)
- [var kABNotEqualCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabnotequalcaseinsensitive)
- [var kABLessThan: _ABSearchComparison](/documentation/addressbook/kablessthan)
- [var kABLessThanOrEqual: _ABSearchComparison](/documentation/addressbook/kablessthanorequal)
- [var kABGreaterThan: _ABSearchComparison](/documentation/addressbook/kabgreaterthan)
- [var kABGreaterThanOrEqual: _ABSearchComparison](/documentation/addressbook/kabgreaterthanorequal)
- [var kABEqualCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabequalcaseinsensitive)
- [var kABContainsSubString: _ABSearchComparison](/documentation/addressbook/kabcontainssubstring)
- [var kABContainsSubStringCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabcontainssubstringcaseinsensitive)
- [var kABPrefixMatch: _ABSearchComparison](/documentation/addressbook/kabprefixmatch)
- [var kABPrefixMatchCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabprefixmatchcaseinsensitive)
- [var kABSuffixMatch: _ABSearchComparison](/documentation/addressbook/kabsuffixmatch)
- [var kABSuffixMatchCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabsuffixmatchcaseinsensitive)
- [var kABBitsInBitFieldMatch: _ABSearchComparison](/documentation/addressbook/kabbitsinbitfieldmatch)
- [var kABDoesNotContainSubString: _ABSearchComparison](/documentation/addressbook/kabdoesnotcontainsubstring)
- [var kABDoesNotContainSubStringCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabdoesnotcontainsubstringcaseinsensitive)
- [var kABWithinIntervalAroundToday: _ABSearchComparison](/documentation/addressbook/kabwithinintervalaroundtoday)
- [var kABWithinIntervalAroundTodayYearless: _ABSearchComparison](/documentation/addressbook/kabwithinintervalaroundtodayyearless)
- [var kABNotWithinIntervalAroundToday: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalaroundtoday)
- [var kABNotWithinIntervalAroundTodayYearless: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalaroundtodayyearless)
- [var kABWithinIntervalFromToday: _ABSearchComparison](/documentation/addressbook/kabwithinintervalfromtoday)
- [var kABWithinIntervalFromTodayYearless: _ABSearchComparison](/documentation/addressbook/kabwithinintervalfromtodayyearless)
- [var kABNotWithinIntervalFromToday: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalfromtoday)
- [var kABNotWithinIntervalFromTodayYearless: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalfromtodayyearless)
- [ABSearchElementRef](/documentation/addressbook/absearchelementref)

## Action Plug-In

- [ABActionDelegate](/documentation/addressbook/abactiondelegate)

### Performing actions

- [func performAction(for: ABPerson!, identifier: String!)](/documentation/objectivec/nsobject-swift.class/performaction(for:identifier:))

### Querying

- [func actionProperty() -> String!](/documentation/objectivec/nsobject-swift.class/actionproperty())
- [func shouldEnableAction(for: ABPerson!, identifier: String!) -> Bool](/documentation/objectivec/nsobject-swift.class/shouldenableaction(for:identifier:))
- [func title(for: ABPerson!, identifier: String!) -> String!](/documentation/objectivec/nsobject-swift.class/title(for:identifier:))

## C Interfaces

- [C Types](/documentation/addressbook/c-types)

### Essentials

- [ABAddressBook](/documentation/addressbook/abaddressbookref)

### Data Types

- [ABPersonRef](/documentation/addressbook/abpersonref)
- [ABGroupRef](/documentation/addressbook/abgroupref)
- [ABMultiValue](/documentation/addressbook/abmultivalueref)
- [ABMutableMultiValue](/documentation/addressbook/abmutablemultivalueref)

### Deprecated

- [ABPersonImageFormat](/documentation/addressbook/abpersonimageformat)

#### Constants

- [init(UInt32)](/documentation/addressbook/abpersonimageformat/init(_:))
- [init(rawValue: UInt32)](/documentation/addressbook/abpersonimageformat/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/addressbook/abpersonimageformat/rawvalue)
- [var kABPersonImageFormatOriginalSize: ABPersonImageFormat](/documentation/addressbook/kabpersonimageformatoriginalsize)
- [var kABPersonImageFormatThumbnail: ABPersonImageFormat](/documentation/addressbook/kabpersonimageformatthumbnail)
- [AddressBook Functions](/documentation/addressbook/addressbook-functions)

### Address Book

- [func ABGetSharedAddressBook() -> Unmanaged<ABAddressBookRef>!](/documentation/addressbook/abgetsharedaddressbook())
- [func ABCopyDefaultCountryCode(ABAddressBookRef!) -> Unmanaged<CFString>!](/documentation/addressbook/abcopydefaultcountrycode(_:))
- [func ABHasUnsavedChanges(ABAddressBookRef!) -> Bool](/documentation/addressbook/abhasunsavedchanges(_:))
- [func ABSave(ABAddressBookRef!) -> Bool](/documentation/addressbook/absave(_:))

### People

- [func ABCopyArrayOfAllPeople(ABAddressBookRef!) -> Unmanaged<CFArray>!](/documentation/addressbook/abcopyarrayofallpeople(_:))
- [func ABGetMe(ABAddressBookRef!) -> Unmanaged<ABPersonRef>!](/documentation/addressbook/abgetme(_:))
- [func ABPersonCopyImageData(ABRecord!) -> Unmanaged<CFData>!](/documentation/addressbook/abpersoncopyimagedata(_:))
- [func ABPersonCopyParentGroups(ABPersonRef!) -> Unmanaged<CFArray>!](/documentation/addressbook/abpersoncopyparentgroups(_:))
- [func ABPersonCopyVCardRepresentation(ABPersonRef!) -> Unmanaged<CFData>!](/documentation/addressbook/abpersoncopyvcardrepresentation(_:))
- [func ABPersonCreate() -> Unmanaged<ABRecord>!](/documentation/addressbook/abpersoncreate())
- [func ABPersonCreateSearchElement(CFString!, CFString!, CFString!, CFTypeRef!, ABSearchComparison) -> Unmanaged<ABSearchElementRef>!](/documentation/addressbook/abpersoncreatesearchelement(_:_:_:_:_:))
- [func ABPersonCreateWithVCardRepresentation(CFData!) -> Unmanaged<ABPersonRef>!](/documentation/addressbook/abpersoncreatewithvcardrepresentation(_:))
- [func ABPersonSetImageData(ABRecord!, CFData!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abpersonsetimagedata(_:_:))
- [func ABSetMe(ABAddressBookRef!, ABPersonRef!)](/documentation/addressbook/absetme(_:_:))

### Groups

- [func ABCopyArrayOfAllGroups(ABAddressBookRef!) -> Unmanaged<CFArray>!](/documentation/addressbook/abcopyarrayofallgroups(_:))
- [func ABGroupAddGroup(ABGroupRef!, ABGroupRef!) -> Bool](/documentation/addressbook/abgroupaddgroup(_:_:))
- [func ABGroupAddMember(ABRecord!, ABRecord!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abgroupaddmember(_:_:))
- [func ABGroupCopyArrayOfAllMembers(ABRecord!) -> Unmanaged<CFArray>!](/documentation/addressbook/abgroupcopyarrayofallmembers(_:))
- [func ABGroupCopyArrayOfAllSubgroups(ABGroupRef!) -> Unmanaged<CFArray>!](/documentation/addressbook/abgroupcopyarrayofallsubgroups(_:))
- [func ABGroupCopyDistributionIdentifier(ABGroupRef!, ABPersonRef!, CFString!) -> Unmanaged<CFString>!](/documentation/addressbook/abgroupcopydistributionidentifier(_:_:_:))
- [func ABGroupCopyParentGroups(ABGroupRef!) -> Unmanaged<CFArray>!](/documentation/addressbook/abgroupcopyparentgroups(_:))
- [func ABGroupCreate() -> Unmanaged<ABRecord>!](/documentation/addressbook/abgroupcreate())
- [func ABGroupCreateSearchElement(CFString!, CFString!, CFString!, CFTypeRef!, ABSearchComparison) -> Unmanaged<ABSearchElementRef>!](/documentation/addressbook/abgroupcreatesearchelement(_:_:_:_:_:))
- [func ABGroupRemoveGroup(ABGroupRef!, ABGroupRef!) -> Bool](/documentation/addressbook/abgroupremovegroup(_:_:))
- [func ABGroupRemoveMember(ABRecord!, ABRecord!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abgroupremovemember(_:_:))
- [func ABGroupSetDistributionIdentifier(ABGroupRef!, ABPersonRef!, CFString!, CFString!) -> Bool](/documentation/addressbook/abgroupsetdistributionidentifier(_:_:_:_:))

### Multi Values

- [func ABMultiValueAdd(ABMutableMultiValueRef!, CFTypeRef!, CFString!, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> Bool](/documentation/addressbook/abmultivalueadd(_:_:_:_:))
- [func ABMultiValueCopyIdentifierAtIndex(ABMultiValueRef!, CFIndex) -> Unmanaged<CFString>!](/documentation/addressbook/abmultivaluecopyidentifieratindex(_:_:))
- [func ABMultiValueCopyLabelAtIndex(ABMultiValue!, CFIndex) -> Unmanaged<CFString>!](/documentation/addressbook/abmultivaluecopylabelatindex(_:_:))
- [func ABMultiValueCopyPrimaryIdentifier(ABMultiValueRef!) -> Unmanaged<CFString>!](/documentation/addressbook/abmultivaluecopyprimaryidentifier(_:))
- [func ABMultiValueCopyValueAtIndex(ABMultiValue!, CFIndex) -> Unmanaged<CFTypeRef>!](/documentation/addressbook/abmultivaluecopyvalueatindex(_:_:))
- [func ABMultiValueCount(ABMultiValueRef!) -> CFIndex](/documentation/addressbook/abmultivaluecount(_:))
- [func ABMultiValueCreate() -> Unmanaged<ABMultiValueRef>!](/documentation/addressbook/abmultivaluecreate())
- [func ABMultiValueCreateCopy(ABMultiValueRef!) -> Unmanaged<ABMultiValueRef>!](/documentation/addressbook/abmultivaluecreatecopy(_:))
- [func ABMultiValueCreateMutable(ABPropertyType) -> Unmanaged<ABMutableMultiValue>!](/documentation/addressbook/abmultivaluecreatemutable())
- [func ABMultiValueCreateMutableCopy(ABMultiValue!) -> Unmanaged<ABMutableMultiValue>!](/documentation/addressbook/abmultivaluecreatemutablecopy(_:))
- [func ABMultiValueIndexForIdentifier(ABMultiValueRef!, CFString!) -> CFIndex](/documentation/addressbook/abmultivalueindexforidentifier(_:_:))
- [func ABMultiValueInsert(ABMutableMultiValueRef!, CFTypeRef!, CFString!, CFIndex, UnsafeMutablePointer<Unmanaged<CFString>?>!) -> Bool](/documentation/addressbook/abmultivalueinsert(_:_:_:_:_:))
- [func ABMultiValuePropertyType(ABMultiValueRef!) -> ABPropertyType](/documentation/addressbook/abmultivaluepropertytype(_:))
- [func ABMultiValueRemove(ABMutableMultiValueRef!, CFIndex) -> Bool](/documentation/addressbook/abmultivalueremove(_:_:))
- [func ABMultiValueReplaceLabel(ABMutableMultiValueRef!, CFString!, CFIndex) -> Bool](/documentation/addressbook/abmultivaluereplacelabel(_:_:_:))
- [func ABMultiValueReplaceValue(ABMutableMultiValueRef!, CFTypeRef!, CFIndex) -> Bool](/documentation/addressbook/abmultivaluereplacevalue(_:_:_:))
- [func ABMultiValueSetPrimaryIdentifier(ABMutableMultiValueRef!, CFString!) -> Bool](/documentation/addressbook/abmultivaluesetprimaryidentifier(_:_:))

### Images

- [func ABBeginLoadingImageDataForClient(ABPersonRef!, ABImageClientCallback!, UnsafeMutableRawPointer!) -> CFIndex](/documentation/addressbook/abbeginloadingimagedataforclient(_:_:_:))
- [func ABCancelLoadingImageDataForTag(CFIndex)](/documentation/addressbook/abcancelloadingimagedatafortag(_:))

### Search Elements

- [func ABCopyArrayOfMatchingRecords(ABAddressBookRef!, ABSearchElementRef!) -> Unmanaged<CFArray>!](/documentation/addressbook/abcopyarrayofmatchingrecords(_:_:))
- [func ABSearchElementCreateWithConjunction(ABSearchConjunction, CFArray!) -> Unmanaged<ABSearchElementRef>!](/documentation/addressbook/absearchelementcreatewithconjunction(_:_:))
- [func ABSearchElementMatchesRecord(ABSearchElementRef!, ABRecordRef!) -> Bool](/documentation/addressbook/absearchelementmatchesrecord(_:_:))

### Properties

- [func ABAddPropertiesAndTypes(ABAddressBookRef!, CFString!, CFDictionary!) -> CFIndex](/documentation/addressbook/abaddpropertiesandtypes(_:_:_:))
- [func ABCopyArrayOfPropertiesForRecordType(ABAddressBookRef!, CFString!) -> Unmanaged<CFArray>!](/documentation/addressbook/abcopyarrayofpropertiesforrecordtype(_:_:))
- [func ABCopyLocalizedPropertyOrLabel(CFString!) -> Unmanaged<CFString>!](/documentation/addressbook/abcopylocalizedpropertyorlabel(_:))
- [func ABLocalizedPropertyOrLabel(String!) -> String!](/documentation/addressbook/ablocalizedpropertyorlabel(_:))
- [func ABRemoveProperties(ABAddressBookRef!, CFString!, CFArray!) -> CFIndex](/documentation/addressbook/abremoveproperties(_:_:_:))
- [func ABTypeOfProperty(ABAddressBookRef!, CFString!, CFString!) -> ABPropertyType](/documentation/addressbook/abtypeofproperty(_:_:_:))

### Records

- [func ABAddRecord(ABAddressBookRef!, ABRecordRef!) -> Bool](/documentation/addressbook/abaddrecord(_:_:))
- [func ABCopyRecordForUniqueId(ABAddressBookRef!, CFString!) -> Unmanaged<ABRecordRef>!](/documentation/addressbook/abcopyrecordforuniqueid(_:_:))
- [func ABCopyRecordTypeFromUniqueId(ABAddressBookRef!, CFString!) -> Unmanaged<CFString>!](/documentation/addressbook/abcopyrecordtypefromuniqueid(_:_:))
- [func ABCreateFormattedAddressFromDictionary(ABAddressBookRef!, CFDictionary!) -> Unmanaged<CFString>!](/documentation/addressbook/abcreateformattedaddressfromdictionary(_:_:))
- [func ABRecordCopyRecordType(ABRecordRef!) -> Unmanaged<CFString>!](/documentation/addressbook/abrecordcopyrecordtype(_:))
- [func ABRecordCopyUniqueId(ABRecordRef!) -> Unmanaged<CFString>!](/documentation/addressbook/abrecordcopyuniqueid(_:))
- [func ABRecordCopyValue(ABRecord!, ABPropertyID) -> Unmanaged<CFTypeRef>!](/documentation/addressbook/abrecordcopyvalue(_:_:))
- [func ABRecordCreateCopy(ABRecordRef!) -> Unmanaged<ABRecordRef>!](/documentation/addressbook/abrecordcreatecopy(_:))
- [func ABRecordIsReadOnly(ABRecordRef!) -> Bool](/documentation/addressbook/abrecordisreadonly(_:))
- [func ABRecordRemoveValue(ABRecord!, ABPropertyID, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abrecordremovevalue(_:_:))
- [func ABRecordSetValue(ABRecord!, ABPropertyID, CFTypeRef!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abrecordsetvalue(_:_:_:))
- [func ABRemoveRecord(ABAddressBookRef!, ABRecordRef!) -> Bool](/documentation/addressbook/abremoverecord(_:_:))

### Deprecated

- [func ABAddressBookAddRecord(ABAddressBook!, ABRecord!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abaddressbookaddrecord(_:_:_:))
- [func ABAddressBookCopyArrayOfAllGroups(ABAddressBook!) -> Unmanaged<CFArray>!](/documentation/addressbook/abaddressbookcopyarrayofallgroups(_:))
- [func ABAddressBookCopyArrayOfAllGroupsInSource(ABAddressBook!, ABRecord!) -> Unmanaged<CFArray>!](/documentation/addressbook/abaddressbookcopyarrayofallgroupsinsource(_:_:))
- [func ABAddressBookCopyArrayOfAllPeople(ABAddressBook!) -> Unmanaged<CFArray>!](/documentation/addressbook/abaddressbookcopyarrayofallpeople(_:))
- [func ABAddressBookCopyArrayOfAllPeopleInSource(ABAddressBook!, ABRecord!) -> Unmanaged<CFArray>!](/documentation/addressbook/abaddressbookcopyarrayofallpeopleinsource(_:_:))
- [func ABAddressBookCopyArrayOfAllPeopleInSourceWithSortOrdering(ABAddressBook!, ABRecord!, ABPersonSortOrdering) -> Unmanaged<CFArray>!](/documentation/addressbook/abaddressbookcopyarrayofallpeopleinsourcewithsortordering(_:_:_:))
- [func ABAddressBookCopyArrayOfAllSources(ABAddressBook!) -> Unmanaged<CFArray>!](/documentation/addressbook/abaddressbookcopyarrayofallsources(_:))
- [func ABAddressBookCopyDefaultSource(ABAddressBook!) -> Unmanaged<ABRecord>!](/documentation/addressbook/abaddressbookcopydefaultsource(_:))
- [func ABAddressBookCopyLocalizedLabel(CFString!) -> Unmanaged<CFString>!](/documentation/addressbook/abaddressbookcopylocalizedlabel(_:))
- [func ABAddressBookCopyPeopleWithName(ABAddressBook!, CFString!) -> Unmanaged<CFArray>!](/documentation/addressbook/abaddressbookcopypeoplewithname(_:_:))
- [func ABAddressBookCreate() -> Unmanaged<ABAddressBook>!](/documentation/addressbook/abaddressbookcreate())
- [func ABAddressBookCreateWithOptions(CFDictionary!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Unmanaged<ABAddressBook>!](/documentation/addressbook/abaddressbookcreatewithoptions(_:_:))
- [func ABAddressBookGetAuthorizationStatus() -> ABAuthorizationStatus](/documentation/addressbook/abaddressbookgetauthorizationstatus())
- [func ABAddressBookGetGroupCount(ABAddressBook!) -> CFIndex](/documentation/addressbook/abaddressbookgetgroupcount(_:))
- [func ABAddressBookGetGroupWithRecordID(ABAddressBook!, ABRecordID) -> Unmanaged<ABRecord>!](/documentation/addressbook/abaddressbookgetgroupwithrecordid(_:_:))
- [func ABAddressBookGetPersonCount(ABAddressBook!) -> CFIndex](/documentation/addressbook/abaddressbookgetpersoncount(_:))
- [func ABAddressBookGetPersonWithRecordID(ABAddressBook!, ABRecordID) -> Unmanaged<ABRecord>!](/documentation/addressbook/abaddressbookgetpersonwithrecordid(_:_:))
- [func ABAddressBookGetSourceWithRecordID(ABAddressBook!, ABRecordID) -> Unmanaged<ABRecord>!](/documentation/addressbook/abaddressbookgetsourcewithrecordid(_:_:))
- [func ABAddressBookHasUnsavedChanges(ABAddressBook!) -> Bool](/documentation/addressbook/abaddressbookhasunsavedchanges(_:))
- [func ABAddressBookRegisterExternalChangeCallback(ABAddressBook!, ABExternalChangeCallback!, UnsafeMutableRawPointer!)](/documentation/addressbook/abaddressbookregisterexternalchangecallback(_:_:_:))
- [func ABAddressBookRemoveRecord(ABAddressBook!, ABRecord!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abaddressbookremoverecord(_:_:_:))
- [func ABAddressBookRequestAccessWithCompletion(ABAddressBook!, ABAddressBookRequestAccessCompletionHandler!)](/documentation/addressbook/abaddressbookrequestaccesswithcompletion(_:_:))
- [func ABAddressBookRevert(ABAddressBook!)](/documentation/addressbook/abaddressbookrevert(_:))
- [func ABAddressBookSave(ABAddressBook!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abaddressbooksave(_:_:))
- [func ABAddressBookUnregisterExternalChangeCallback(ABAddressBook!, ABExternalChangeCallback!, UnsafeMutableRawPointer!)](/documentation/addressbook/abaddressbookunregisterexternalchangecallback(_:_:_:))
- [func ABGroupCopyArrayOfAllMembersWithSortOrdering(ABRecord!, ABPersonSortOrdering) -> Unmanaged<CFArray>!](/documentation/addressbook/abgroupcopyarrayofallmemberswithsortordering(_:_:))
- [func ABGroupCopySource(ABRecord!) -> Unmanaged<ABRecord>!](/documentation/addressbook/abgroupcopysource(_:))
- [func ABGroupCreateInSource(ABRecord!) -> Unmanaged<ABRecord>!](/documentation/addressbook/abgroupcreateinsource(_:))
- [func ABMultiValueAddValueAndLabel(ABMutableMultiValue!, CFTypeRef!, CFString!, UnsafeMutablePointer<ABMultiValueIdentifier>!) -> Bool](/documentation/addressbook/abmultivalueaddvalueandlabel(_:_:_:_:))
- [func ABMultiValueCopyArrayOfAllValues(ABMultiValue!) -> Unmanaged<CFArray>!](/documentation/addressbook/abmultivaluecopyarrayofallvalues(_:))
- [func ABMultiValueGetCount(ABMultiValue!) -> CFIndex](/documentation/addressbook/abmultivaluegetcount(_:))
- [func ABMultiValueGetFirstIndexOfValue(ABMultiValue!, CFTypeRef!) -> CFIndex](/documentation/addressbook/abmultivaluegetfirstindexofvalue(_:_:))
- [func ABMultiValueGetIdentifierAtIndex(ABMultiValue!, CFIndex) -> ABMultiValueIdentifier](/documentation/addressbook/abmultivaluegetidentifieratindex(_:_:))
- [func ABMultiValueGetIndexForIdentifier(ABMultiValue!, ABMultiValueIdentifier) -> CFIndex](/documentation/addressbook/abmultivaluegetindexforidentifier(_:_:))
- [func ABMultiValueGetPropertyType(ABMultiValue!) -> ABPropertyType](/documentation/addressbook/abmultivaluegetpropertytype(_:))
- [func ABMultiValueInsertValueAndLabelAtIndex(ABMutableMultiValue!, CFTypeRef!, CFString!, CFIndex, UnsafeMutablePointer<ABMultiValueIdentifier>!) -> Bool](/documentation/addressbook/abmultivalueinsertvalueandlabelatindex(_:_:_:_:_:))
- [func ABMultiValueRemoveValueAndLabelAtIndex(ABMutableMultiValue!, CFIndex) -> Bool](/documentation/addressbook/abmultivalueremovevalueandlabelatindex(_:_:))
- [func ABMultiValueReplaceLabelAtIndex(ABMutableMultiValue!, CFString!, CFIndex) -> Bool](/documentation/addressbook/abmultivaluereplacelabelatindex(_:_:_:))
- [func ABMultiValueReplaceValueAtIndex(ABMutableMultiValue!, CFTypeRef!, CFIndex) -> Bool](/documentation/addressbook/abmultivaluereplacevalueatindex(_:_:_:))
- [func ABPersonComparePeopleByName(ABRecord!, ABRecord!, ABPersonSortOrdering) -> CFComparisonResult](/documentation/addressbook/abpersoncomparepeoplebyname(_:_:_:))
- [func ABPersonCopyArrayOfAllLinkedPeople(ABRecord!) -> Unmanaged<CFArray>!](/documentation/addressbook/abpersoncopyarrayofalllinkedpeople(_:))
- [func ABPersonCopyCompositeNameDelimiterForRecord(ABRecord!) -> Unmanaged<CFString>!](/documentation/addressbook/abpersoncopycompositenamedelimiterforrecord(_:))
- [func ABPersonCopyImageDataWithFormat(ABRecord!, ABPersonImageFormat) -> Unmanaged<CFData>!](/documentation/addressbook/abpersoncopyimagedatawithformat(_:_:))
- [func ABPersonCopyLocalizedPropertyName(ABPropertyID) -> Unmanaged<CFString>!](/documentation/addressbook/abpersoncopylocalizedpropertyname(_:))
- [func ABPersonCopySource(ABRecord!) -> Unmanaged<ABRecord>!](/documentation/addressbook/abpersoncopysource(_:))
- [func ABPersonCreateInSource(ABRecord!) -> Unmanaged<ABRecord>!](/documentation/addressbook/abpersoncreateinsource(_:))
- [func ABPersonCreatePeopleInSourceWithVCardRepresentation(ABRecord!, CFData!) -> Unmanaged<CFArray>!](/documentation/addressbook/abpersoncreatepeopleinsourcewithvcardrepresentation(_:_:))
- [func ABPersonCreateVCardRepresentationWithPeople(CFArray!) -> Unmanaged<CFData>!](/documentation/addressbook/abpersoncreatevcardrepresentationwithpeople(_:))
- [func ABPersonGetCompositeNameFormat() -> ABPersonCompositeNameFormat](/documentation/addressbook/abpersongetcompositenameformat())
- [func ABPersonGetCompositeNameFormatForRecord(ABRecord!) -> ABPersonCompositeNameFormat](/documentation/addressbook/abpersongetcompositenameformatforrecord(_:))
- [func ABPersonGetSortOrdering() -> ABPersonSortOrdering](/documentation/addressbook/abpersongetsortordering())
- [func ABPersonGetTypeOfProperty(ABPropertyID) -> ABPropertyType](/documentation/addressbook/abpersongettypeofproperty(_:))
- [func ABPersonHasImageData(ABRecord!) -> Bool](/documentation/addressbook/abpersonhasimagedata(_:))
- [func ABPersonRemoveImageData(ABRecord!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abpersonremoveimagedata(_:_:))
- [func ABRecordCopyCompositeName(ABRecord!) -> Unmanaged<CFString>!](/documentation/addressbook/abrecordcopycompositename(_:))
- [func ABRecordGetRecordID(ABRecord!) -> ABRecordID](/documentation/addressbook/abrecordgetrecordid(_:))
- [func ABRecordGetRecordType(ABRecord!) -> ABRecordType](/documentation/addressbook/abrecordgetrecordtype(_:))
- [Address Book Constants](/documentation/addressbook/address-book-constants)

### Data Type Constants

- [Address Keys](/documentation/addressbook/address-keys)

#### Constants

- [let kABAddressStreetKey: String](/documentation/addressbook/kabaddressstreetkey)
- [let kABAddressCityKey: String](/documentation/addressbook/kabaddresscitykey)
- [let kABAddressStateKey: String](/documentation/addressbook/kabaddressstatekey)
- [let kABAddressZIPKey: String](/documentation/addressbook/kabaddresszipkey)
- [let kABAddressCountryKey: String](/documentation/addressbook/kabaddresscountrykey)
- [let kABAddressCountryCodeKey: String](/documentation/addressbook/kabaddresscountrycodekey)
- [Default Person Properties](/documentation/addressbook/default-person-properties)

#### Constants

- [let kABFirstNameProperty: String](/documentation/addressbook/kabfirstnameproperty)
- [let kABLastNameProperty: String](/documentation/addressbook/kablastnameproperty)
- [let kABFirstNamePhoneticProperty: String](/documentation/addressbook/kabfirstnamephoneticproperty)
- [let kABLastNamePhoneticProperty: String](/documentation/addressbook/kablastnamephoneticproperty)
- [let kABNicknameProperty: String](/documentation/addressbook/kabnicknameproperty)
- [let kABMaidenNameProperty: String](/documentation/addressbook/kabmaidennameproperty)
- [let kABBirthdayProperty: String](/documentation/addressbook/kabbirthdayproperty)
- [let kABBirthdayComponentsProperty: String](/documentation/addressbook/kabbirthdaycomponentsproperty)
- [let kABOrganizationProperty: String](/documentation/addressbook/kaborganizationproperty)
- [let kABJobTitleProperty: String](/documentation/addressbook/kabjobtitleproperty)
- [let kABHomePageProperty: String](/documentation/addressbook/kabhomepageproperty)
- [let kABURLsProperty: String](/documentation/addressbook/kaburlsproperty)
- [let kABCalendarURIsProperty: String](/documentation/addressbook/kabcalendarurisproperty)
- [let kABEmailProperty: String](/documentation/addressbook/kabemailproperty)
- [let kABAddressProperty: String](/documentation/addressbook/kabaddressproperty)
- [let kABOtherDatesProperty: String](/documentation/addressbook/kabotherdatesproperty)
- [let kABOtherDateComponentsProperty: String](/documentation/addressbook/kabotherdatecomponentsproperty)
- [let kABRelatedNamesProperty: String](/documentation/addressbook/kabrelatednamesproperty)
- [let kABDepartmentProperty: String](/documentation/addressbook/kabdepartmentproperty)
- [let kABPersonFlags: String](/documentation/addressbook/kabpersonflags)
- [let kABPhoneProperty: String](/documentation/addressbook/kabphoneproperty)
- [let kABInstantMessageProperty: String](/documentation/addressbook/kabinstantmessageproperty)
- [let kABNoteProperty: String](/documentation/addressbook/kabnoteproperty)
- [let kABSocialProfileProperty: String](/documentation/addressbook/kabsocialprofileproperty)
- [let kABMiddleNameProperty: String](/documentation/addressbook/kabmiddlenameproperty)
- [let kABMiddleNamePhoneticProperty: String](/documentation/addressbook/kabmiddlenamephoneticproperty)
- [let kABTitleProperty: String](/documentation/addressbook/kabtitleproperty)
- [let kABSuffixProperty: String](/documentation/addressbook/kabsuffixproperty)
- [Default Group Properties](/documentation/addressbook/default-group-properties)

#### Constants

- [let kABGroupNameProperty: Int32](/documentation/addressbook/kabgroupnameproperty)
- [Default Multivalue List Labels](/documentation/addressbook/default-multivalue-list-labels)

#### Constants

- [let kABHomePageLabel: String](/documentation/addressbook/kabhomepagelabel)
- [let kABEmailWorkLabel: String](/documentation/addressbook/kabemailworklabel)
- [let kABEmailHomeLabel: String](/documentation/addressbook/kabemailhomelabel)
- [let kABEmailMobileMeLabel: String](/documentation/addressbook/kabemailmobilemelabel)
- [let kABAddressHomeLabel: String](/documentation/addressbook/kabaddresshomelabel)
- [let kABAddressWorkLabel: String](/documentation/addressbook/kabaddressworklabel)
- [let kABAnniversaryLabel: String](/documentation/addressbook/kabanniversarylabel)
- [let kABFatherLabel: String](/documentation/addressbook/kabfatherlabel)
- [let kABMotherLabel: String](/documentation/addressbook/kabmotherlabel)
- [let kABParentLabel: String](/documentation/addressbook/kabparentlabel)
- [let kABBrotherLabel: String](/documentation/addressbook/kabbrotherlabel)
- [let kABSisterLabel: String](/documentation/addressbook/kabsisterlabel)
- [let kABChildLabel: String](/documentation/addressbook/kabchildlabel)
- [let kABFriendLabel: String](/documentation/addressbook/kabfriendlabel)
- [let kABSpouseLabel: String](/documentation/addressbook/kabspouselabel)
- [let kABPartnerLabel: String](/documentation/addressbook/kabpartnerlabel)
- [let kABAssistantLabel: String](/documentation/addressbook/kabassistantlabel)
- [let kABManagerLabel: String](/documentation/addressbook/kabmanagerlabel)
- [let kABPhoneWorkLabel: String](/documentation/addressbook/kabphoneworklabel)
- [let kABPhoneHomeLabel: String](/documentation/addressbook/kabphonehomelabel)
- [let kABPhoneiPhoneLabel: String](/documentation/addressbook/kabphoneiphonelabel)
- [let kABPhoneMobileLabel: String](/documentation/addressbook/kabphonemobilelabel)
- [let kABPhoneMainLabel: String](/documentation/addressbook/kabphonemainlabel)
- [let kABPhoneHomeFAXLabel: String](/documentation/addressbook/kabphonehomefaxlabel)
- [let kABPhoneWorkFAXLabel: String](/documentation/addressbook/kabphoneworkfaxlabel)
- [let kABPhonePagerLabel: String](/documentation/addressbook/kabphonepagerlabel)
- [Generic Multivalue List Labels](/documentation/addressbook/generic-multivalue-list-labels)

#### Constants

- [let kABWorkLabel: CFString!](/documentation/addressbook/kabworklabel)
- [let kABHomeLabel: CFString!](/documentation/addressbook/kabhomelabel)
- [let kABOtherLabel: CFString!](/documentation/addressbook/kabotherlabel)
- [let kABMobileMeLabel: String](/documentation/addressbook/kabmobilemelabel)
- [Multivalue Property](/documentation/addressbook/multivalue-property)

#### Constants

- [var kABMultiValueMask: Int32](/documentation/addressbook/kabmultivaluemask)
- [Default Record Properties](/documentation/addressbook/default-record-properties)

#### Constants

- [let kABUIDProperty: String](/documentation/addressbook/kabuidproperty)
- [let kABCreationDateProperty: String](/documentation/addressbook/kabcreationdateproperty)
- [let kABModificationDateProperty: String](/documentation/addressbook/kabmodificationdateproperty)
- [Property Types](/documentation/addressbook/property_types)

#### Constants

- [var kABErrorInProperty: _ABPropertyType](/documentation/addressbook/kaberrorinproperty)
- [var kABStringProperty: _ABPropertyType](/documentation/addressbook/kabstringproperty)
- [var kABIntegerProperty: _ABPropertyType](/documentation/addressbook/kabintegerproperty)
- [var kABRealProperty: _ABPropertyType](/documentation/addressbook/kabrealproperty)
- [var kABDateProperty: _ABPropertyType](/documentation/addressbook/kabdateproperty)
- [var kABArrayProperty: _ABPropertyType](/documentation/addressbook/kabarrayproperty)
- [var kABDictionaryProperty: _ABPropertyType](/documentation/addressbook/kabdictionaryproperty)
- [var kABDataProperty: _ABPropertyType](/documentation/addressbook/kabdataproperty)
- [var kABDateComponentsProperty: _ABPropertyType](/documentation/addressbook/kabdatecomponentsproperty)
- [var kABMultiStringProperty: _ABPropertyType](/documentation/addressbook/kabmultistringproperty)
- [var kABMultiIntegerProperty: _ABPropertyType](/documentation/addressbook/kabmultiintegerproperty)
- [var kABMultiRealProperty: _ABPropertyType](/documentation/addressbook/kabmultirealproperty)
- [var kABMultiDateProperty: _ABPropertyType](/documentation/addressbook/kabmultidateproperty)
- [var kABMultiArrayProperty: _ABPropertyType](/documentation/addressbook/kabmultiarrayproperty)
- [var kABMultiDictionaryProperty: _ABPropertyType](/documentation/addressbook/kabmultidictionaryproperty)
- [var kABMultiDataProperty: _ABPropertyType](/documentation/addressbook/kabmultidataproperty)
- [var kABMultiDateComponentsProperty: _ABPropertyType](/documentation/addressbook/kabmultidatecomponentsproperty)

### Social Media Constants

- [Instant Messaging Keys](/documentation/addressbook/instant-messaging-keys)

#### Constants

- [let kABInstantMessageUsernameKey: String](/documentation/addressbook/kabinstantmessageusernamekey)
- [let kABInstantMessageServiceKey: String](/documentation/addressbook/kabinstantmessageservicekey)
- [Instant Messaging Services](/documentation/addressbook/instant-messaging-services)

#### Constants

- [let kABInstantMessageServiceAIM: String](/documentation/addressbook/kabinstantmessageserviceaim)
- [let kABInstantMessageServiceFacebook: String](/documentation/addressbook/kabinstantmessageservicefacebook)
- [let kABInstantMessageServiceGaduGadu: String](/documentation/addressbook/kabinstantmessageservicegadugadu)
- [let kABInstantMessageServiceGoogleTalk: String](/documentation/addressbook/kabinstantmessageservicegoogletalk)
- [let kABInstantMessageServiceICQ: String](/documentation/addressbook/kabinstantmessageserviceicq)
- [let kABInstantMessageServiceJabber: String](/documentation/addressbook/kabinstantmessageservicejabber)
- [let kABInstantMessageServiceMSN: String](/documentation/addressbook/kabinstantmessageservicemsn)
- [let kABInstantMessageServiceQQ: String](/documentation/addressbook/kabinstantmessageserviceqq)
- [let kABInstantMessageServiceSkype: String](/documentation/addressbook/kabinstantmessageserviceskype)
- [let kABInstantMessageServiceYahoo: String](/documentation/addressbook/kabinstantmessageserviceyahoo)
- [Social Profile Services](/documentation/addressbook/social-profile-services)

#### Services

- [let kABSocialProfileServiceTwitter: String](/documentation/addressbook/kabsocialprofileservicetwitter)
- [let kABSocialProfileServiceFacebook: String](/documentation/addressbook/kabsocialprofileservicefacebook)
- [let kABSocialProfileServiceMySpace: String](/documentation/addressbook/kabsocialprofileservicemyspace)
- [let kABSocialProfileServiceLinkedIn: String](/documentation/addressbook/kabsocialprofileservicelinkedin)
- [let kABSocialProfileServiceFlickr: String](/documentation/addressbook/kabsocialprofileserviceflickr)
- [let kABSocialProfileServiceSinaWeibo: String](/documentation/addressbook/kabsocialprofileservicesinaweibo)

#### Keys

- [let kABSocialProfileURLKey: String](/documentation/addressbook/kabsocialprofileurlkey)
- [let kABSocialProfileServiceKey: String](/documentation/addressbook/kabsocialprofileservicekey)
- [let kABSocialProfileUsernameKey: String](/documentation/addressbook/kabsocialprofileusernamekey)
- [let kABSocialProfileUserIdentifierKey: String](/documentation/addressbook/kabsocialprofileuseridentifierkey)

### Errors

- [let ABAddressBookErrorDomain: CFString!](/documentation/addressbook/abaddressbookerrordomain)
- [Error Codes](/documentation/addressbook/error-codes)

#### Errors

- [var ABAddRecordsError: Int](/documentation/addressbook/abaddrecordserror)
- [var ABRemoveRecordsError: Int](/documentation/addressbook/abremoverecordserror)
- [var ABPropertyValueValidationError: Int](/documentation/addressbook/abpropertyvaluevalidationerror)
- [var ABPropertyUnsupportedBySourceError: Int](/documentation/addressbook/abpropertyunsupportedbysourceerror)
- [var ABPropertyReadOnlyError: Int](/documentation/addressbook/abpropertyreadonlyerror)

#### Dictionary Keys

- [let ABMultiValueIdentifiersErrorKey: String](/documentation/addressbook/abmultivalueidentifierserrorkey)

### Miscellaneous

- [var ABMultipleValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/abmultiplevalueselection)
- [var ABNoValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/abnovalueselection)
- [var ABSingleValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/absinglevalueselection)
- [let kABAlternateBirthdayComponentsProperty: String](/documentation/addressbook/kabalternatebirthdaycomponentsproperty)
- [var kABBitsInBitFieldMatch: _ABSearchComparison](/documentation/addressbook/kabbitsinbitfieldmatch)
- [var kABContainsSubString: _ABSearchComparison](/documentation/addressbook/kabcontainssubstring)
- [var kABContainsSubStringCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabcontainssubstringcaseinsensitive)
- [var kABDefaultNameOrdering: Int32](/documentation/addressbook/kabdefaultnameordering)
- [let kABDeletedRecords: String](/documentation/addressbook/kabdeletedrecords)
- [var kABDoesNotContainSubString: _ABSearchComparison](/documentation/addressbook/kabdoesnotcontainsubstring)
- [var kABDoesNotContainSubStringCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabdoesnotcontainsubstringcaseinsensitive)
- [var kABEqual: _ABSearchComparison](/documentation/addressbook/kabequal)
- [var kABEqualCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabequalcaseinsensitive)
- [var kABFirstNameFirst: Int32](/documentation/addressbook/kabfirstnamefirst)
- [var kABGreaterThan: _ABSearchComparison](/documentation/addressbook/kabgreaterthan)
- [var kABGreaterThanOrEqual: _ABSearchComparison](/documentation/addressbook/kabgreaterthanorequal)
- [let kABInsertedRecords: String](/documentation/addressbook/kabinsertedrecords)
- [var kABLastNameFirst: Int32](/documentation/addressbook/kablastnamefirst)
- [var kABLessThan: _ABSearchComparison](/documentation/addressbook/kablessthan)
- [var kABLessThanOrEqual: _ABSearchComparison](/documentation/addressbook/kablessthanorequal)
- [var kABMultiValueInvalidIdentifier: Int32](/documentation/addressbook/kabmultivalueinvalididentifier)
- [var kABNameOrderingMask: Int32](/documentation/addressbook/kabnameorderingmask)
- [var kABNotEqual: _ABSearchComparison](/documentation/addressbook/kabnotequal)
- [var kABNotEqualCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabnotequalcaseinsensitive)
- [var kABNotWithinIntervalAroundToday: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalaroundtoday)
- [var kABNotWithinIntervalAroundTodayYearless: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalaroundtodayyearless)
- [var kABNotWithinIntervalFromToday: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalfromtoday)
- [var kABNotWithinIntervalFromTodayYearless: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalfromtodayyearless)
- [let kABOrganizationPhoneticProperty: String](/documentation/addressbook/kaborganizationphoneticproperty)
- [var kABPrefixMatch: _ABSearchComparison](/documentation/addressbook/kabprefixmatch)
- [var kABPrefixMatchCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabprefixmatchcaseinsensitive)
- [var kABPropertyInvalidID: Int32](/documentation/addressbook/kabpropertyinvalidid)
- [var kABRecordInvalidID: Int32](/documentation/addressbook/kabrecordinvalidid)
- [var kABSearchAnd: _ABSearchConjunction](/documentation/addressbook/kabsearchand)
- [var kABSearchOr: _ABSearchConjunction](/documentation/addressbook/kabsearchor)
- [var kABShowAsCompany: Int32](/documentation/addressbook/kabshowascompany)
- [var kABShowAsMask: Int32](/documentation/addressbook/kabshowasmask)
- [var kABShowAsPerson: Int32](/documentation/addressbook/kabshowasperson)
- [var kABShowAsResource: Int32](/documentation/addressbook/kabshowasresource)
- [var kABShowAsRoom: Int32](/documentation/addressbook/kabshowasroom)
- [let kABSocialProfileServiceTencentWeibo: String](/documentation/addressbook/kabsocialprofileservicetencentweibo)
- [let kABSocialProfileServiceYelp: String](/documentation/addressbook/kabsocialprofileserviceyelp)
- [var kABSourceTypeSearchableMask: Int32](/documentation/addressbook/kabsourcetypesearchablemask)
- [var kABSuffixMatch: _ABSearchComparison](/documentation/addressbook/kabsuffixmatch)
- [var kABSuffixMatchCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabsuffixmatchcaseinsensitive)
- [let kABUpdatedRecords: String](/documentation/addressbook/kabupdatedrecords)
- [var kABWithinIntervalAroundToday: _ABSearchComparison](/documentation/addressbook/kabwithinintervalaroundtoday)
- [var kABWithinIntervalAroundTodayYearless: _ABSearchComparison](/documentation/addressbook/kabwithinintervalaroundtodayyearless)
- [var kABWithinIntervalFromToday: _ABSearchComparison](/documentation/addressbook/kabwithinintervalfromtoday)
- [var kABWithinIntervalFromTodayYearless: _ABSearchComparison](/documentation/addressbook/kabwithinintervalfromtodayyearless)

### Deprecated

- [let kABPersonAddressCityKey: CFString!](/documentation/addressbook/kabpersonaddresscitykey)
- [let kABPersonAddressCountryCodeKey: CFString!](/documentation/addressbook/kabpersonaddresscountrycodekey)
- [let kABPersonAddressCountryKey: CFString!](/documentation/addressbook/kabpersonaddresscountrykey)
- [let kABPersonAddressProperty: ABPropertyID](/documentation/addressbook/kabpersonaddressproperty)
- [let kABPersonAddressStateKey: CFString!](/documentation/addressbook/kabpersonaddressstatekey)
- [let kABPersonAddressStreetKey: CFString!](/documentation/addressbook/kabpersonaddressstreetkey)
- [let kABPersonAddressZIPKey: CFString!](/documentation/addressbook/kabpersonaddresszipkey)
- [let kABPersonAlternateBirthdayCalendarIdentifierKey: CFString!](/documentation/addressbook/kabpersonalternatebirthdaycalendaridentifierkey)
- [let kABPersonAlternateBirthdayDayKey: CFString!](/documentation/addressbook/kabpersonalternatebirthdaydaykey)
- [let kABPersonAlternateBirthdayEraKey: CFString!](/documentation/addressbook/kabpersonalternatebirthdayerakey)
- [let kABPersonAlternateBirthdayIsLeapMonthKey: CFString!](/documentation/addressbook/kabpersonalternatebirthdayisleapmonthkey)
- [let kABPersonAlternateBirthdayMonthKey: CFString!](/documentation/addressbook/kabpersonalternatebirthdaymonthkey)
- [let kABPersonAlternateBirthdayProperty: ABPropertyID](/documentation/addressbook/kabpersonalternatebirthdayproperty)
- [let kABPersonAlternateBirthdayYearKey: CFString!](/documentation/addressbook/kabpersonalternatebirthdayyearkey)
- [let kABPersonAnniversaryLabel: CFString!](/documentation/addressbook/kabpersonanniversarylabel)
- [let kABPersonAssistantLabel: CFString!](/documentation/addressbook/kabpersonassistantlabel)
- [let kABPersonBirthdayProperty: ABPropertyID](/documentation/addressbook/kabpersonbirthdayproperty)
- [let kABPersonBrotherLabel: CFString!](/documentation/addressbook/kabpersonbrotherlabel)
- [let kABPersonChildLabel: CFString!](/documentation/addressbook/kabpersonchildlabel)
- [let kABPersonCreationDateProperty: ABPropertyID](/documentation/addressbook/kabpersoncreationdateproperty)
- [let kABPersonDateProperty: ABPropertyID](/documentation/addressbook/kabpersondateproperty)
- [let kABPersonDepartmentProperty: ABPropertyID](/documentation/addressbook/kabpersondepartmentproperty)
- [let kABPersonEmailProperty: ABPropertyID](/documentation/addressbook/kabpersonemailproperty)
- [let kABPersonFatherLabel: CFString!](/documentation/addressbook/kabpersonfatherlabel)
- [let kABPersonFirstNamePhoneticProperty: ABPropertyID](/documentation/addressbook/kabpersonfirstnamephoneticproperty)
- [let kABPersonFirstNameProperty: ABPropertyID](/documentation/addressbook/kabpersonfirstnameproperty)
- [let kABPersonFriendLabel: CFString!](/documentation/addressbook/kabpersonfriendlabel)
- [let kABPersonHomePageLabel: CFString!](/documentation/addressbook/kabpersonhomepagelabel)
- [var kABPersonImageFormatOriginalSize: ABPersonImageFormat](/documentation/addressbook/kabpersonimageformatoriginalsize)
- [var kABPersonImageFormatThumbnail: ABPersonImageFormat](/documentation/addressbook/kabpersonimageformatthumbnail)
- [let kABPersonInstantMessageProperty: ABPropertyID](/documentation/addressbook/kabpersoninstantmessageproperty)
- [let kABPersonInstantMessageServiceAIM: CFString!](/documentation/addressbook/kabpersoninstantmessageserviceaim)
- [let kABPersonInstantMessageServiceFacebook: CFString!](/documentation/addressbook/kabpersoninstantmessageservicefacebook)
- [let kABPersonInstantMessageServiceGaduGadu: CFString!](/documentation/addressbook/kabpersoninstantmessageservicegadugadu)
- [let kABPersonInstantMessageServiceGoogleTalk: CFString!](/documentation/addressbook/kabpersoninstantmessageservicegoogletalk)
- [let kABPersonInstantMessageServiceICQ: CFString!](/documentation/addressbook/kabpersoninstantmessageserviceicq)
- [let kABPersonInstantMessageServiceJabber: CFString!](/documentation/addressbook/kabpersoninstantmessageservicejabber)
- [let kABPersonInstantMessageServiceKey: CFString!](/documentation/addressbook/kabpersoninstantmessageservicekey)
- [let kABPersonInstantMessageServiceMSN: CFString!](/documentation/addressbook/kabpersoninstantmessageservicemsn)
- [let kABPersonInstantMessageServiceQQ: CFString!](/documentation/addressbook/kabpersoninstantmessageserviceqq)
- [let kABPersonInstantMessageServiceSkype: CFString!](/documentation/addressbook/kabpersoninstantmessageserviceskype)
- [let kABPersonInstantMessageServiceYahoo: CFString!](/documentation/addressbook/kabpersoninstantmessageserviceyahoo)
- [let kABPersonInstantMessageUsernameKey: CFString!](/documentation/addressbook/kabpersoninstantmessageusernamekey)
- [let kABPersonJobTitleProperty: ABPropertyID](/documentation/addressbook/kabpersonjobtitleproperty)
- [let kABPersonKindOrganization: CFNumber!](/documentation/addressbook/kabpersonkindorganization)
- [let kABPersonKindPerson: CFNumber!](/documentation/addressbook/kabpersonkindperson)
- [let kABPersonKindProperty: ABPropertyID](/documentation/addressbook/kabpersonkindproperty)
- [let kABPersonLastNamePhoneticProperty: ABPropertyID](/documentation/addressbook/kabpersonlastnamephoneticproperty)
- [let kABPersonLastNameProperty: ABPropertyID](/documentation/addressbook/kabpersonlastnameproperty)
- [let kABPersonManagerLabel: CFString!](/documentation/addressbook/kabpersonmanagerlabel)
- [let kABPersonMiddleNamePhoneticProperty: ABPropertyID](/documentation/addressbook/kabpersonmiddlenamephoneticproperty)
- [let kABPersonMiddleNameProperty: ABPropertyID](/documentation/addressbook/kabpersonmiddlenameproperty)
- [let kABPersonModificationDateProperty: ABPropertyID](/documentation/addressbook/kabpersonmodificationdateproperty)
- [let kABPersonMotherLabel: CFString!](/documentation/addressbook/kabpersonmotherlabel)
- [let kABPersonNicknameProperty: ABPropertyID](/documentation/addressbook/kabpersonnicknameproperty)
- [let kABPersonNoteProperty: ABPropertyID](/documentation/addressbook/kabpersonnoteproperty)
- [let kABPersonOrganizationProperty: ABPropertyID](/documentation/addressbook/kabpersonorganizationproperty)
- [let kABPersonParentLabel: CFString!](/documentation/addressbook/kabpersonparentlabel)
- [let kABPersonPartnerLabel: CFString!](/documentation/addressbook/kabpersonpartnerlabel)
- [let kABPersonPhoneHomeFAXLabel: CFString!](/documentation/addressbook/kabpersonphonehomefaxlabel)
- [let kABPersonPhoneIPhoneLabel: CFString!](/documentation/addressbook/kabpersonphoneiphonelabel)
- [let kABPersonPhoneMainLabel: CFString!](/documentation/addressbook/kabpersonphonemainlabel)
- [let kABPersonPhoneMobileLabel: CFString!](/documentation/addressbook/kabpersonphonemobilelabel)
- [let kABPersonPhoneOtherFAXLabel: CFString!](/documentation/addressbook/kabpersonphoneotherfaxlabel)
- [let kABPersonPhonePagerLabel: CFString!](/documentation/addressbook/kabpersonphonepagerlabel)
- [let kABPersonPhoneProperty: ABPropertyID](/documentation/addressbook/kabpersonphoneproperty)
- [let kABPersonPhoneWorkFAXLabel: CFString!](/documentation/addressbook/kabpersonphoneworkfaxlabel)
- [let kABPersonPrefixProperty: ABPropertyID](/documentation/addressbook/kabpersonprefixproperty)
- [let kABPersonRelatedNamesProperty: ABPropertyID](/documentation/addressbook/kabpersonrelatednamesproperty)
- [let kABPersonSisterLabel: CFString!](/documentation/addressbook/kabpersonsisterlabel)
- [let kABPersonSocialProfileProperty: ABPropertyID](/documentation/addressbook/kabpersonsocialprofileproperty)
- [let kABPersonSocialProfileServiceFacebook: CFString!](/documentation/addressbook/kabpersonsocialprofileservicefacebook)
- [let kABPersonSocialProfileServiceFlickr: CFString!](/documentation/addressbook/kabpersonsocialprofileserviceflickr)
- [let kABPersonSocialProfileServiceGameCenter: CFString!](/documentation/addressbook/kabpersonsocialprofileservicegamecenter)
- [let kABPersonSocialProfileServiceKey: CFString!](/documentation/addressbook/kabpersonsocialprofileservicekey)
- [let kABPersonSocialProfileServiceLinkedIn: CFString!](/documentation/addressbook/kabpersonsocialprofileservicelinkedin)
- [let kABPersonSocialProfileServiceMyspace: CFString!](/documentation/addressbook/kabpersonsocialprofileservicemyspace)
- [let kABPersonSocialProfileServiceSinaWeibo: CFString!](/documentation/addressbook/kabpersonsocialprofileservicesinaweibo)
- [let kABPersonSocialProfileServiceTwitter: CFString!](/documentation/addressbook/kabpersonsocialprofileservicetwitter)
- [let kABPersonSocialProfileURLKey: CFString!](/documentation/addressbook/kabpersonsocialprofileurlkey)
- [let kABPersonSocialProfileUserIdentifierKey: CFString!](/documentation/addressbook/kabpersonsocialprofileuseridentifierkey)
- [let kABPersonSocialProfileUsernameKey: CFString!](/documentation/addressbook/kabpersonsocialprofileusernamekey)
- [let kABPersonSpouseLabel: CFString!](/documentation/addressbook/kabpersonspouselabel)
- [let kABPersonSuffixProperty: ABPropertyID](/documentation/addressbook/kabpersonsuffixproperty)
- [let kABPersonURLProperty: ABPropertyID](/documentation/addressbook/kabpersonurlproperty)
- [let kABSourceNameProperty: ABPropertyID](/documentation/addressbook/kabsourcenameproperty)
- [let kABSourceTypeProperty: ABPropertyID](/documentation/addressbook/kabsourcetypeproperty)
- [AddressBook Enumerations](/documentation/addressbook/addressbook-enumerations)

### Picker

- [ABPeoplePickerSelectionBehavior](/documentation/addressbook/abpeoplepickerselectionbehavior)

#### Selection Behaviors

- [var ABNoValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/abnovalueselection)
- [var ABSingleValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/absinglevalueselection)
- [var ABMultipleValueSelection: ABPeoplePickerSelectionBehavior](/documentation/addressbook/abmultiplevalueselection)

#### Initializers

- [init(UInt32)](/documentation/addressbook/abpeoplepickerselectionbehavior/init(_:))
- [init(rawValue: UInt32)](/documentation/addressbook/abpeoplepickerselectionbehavior/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/addressbook/abpeoplepickerselectionbehavior/rawvalue)
- [People-Picker Event Class](/documentation/addressbook/people-picker-event-class)
- [People-Picker Event Kinds](/documentation/addressbook/people-picker-event-kinds)
- [People-Picker Event Parameter Name](/documentation/addressbook/people-picker-event-parameter-name)
- [People-Picker Selection Behavior](/documentation/addressbook/people-picker-selection-behavior)

### Errors

- [Address Book Errors](/documentation/addressbook/address-book-errors)

#### Constants

- [var kABOperationNotPermittedByStoreError: Int](/documentation/addressbook/kaboperationnotpermittedbystoreerror)
- [var kABOperationNotPermittedByUserError: Int](/documentation/addressbook/kaboperationnotpermittedbyusererror)
- [Errors](/documentation/addressbook/1529225-errors)

#### Constants

- [var ABAddRecordsError: Int](/documentation/addressbook/abaddrecordserror)
- [var ABRemoveRecordsError: Int](/documentation/addressbook/abremoverecordserror)
- [var ABPropertyValueValidationError: Int](/documentation/addressbook/abpropertyvaluevalidationerror)
- [var ABPropertyUnsupportedBySourceError: Int](/documentation/addressbook/abpropertyunsupportedbysourceerror)
- [var ABPropertyReadOnlyError: Int](/documentation/addressbook/abpropertyreadonlyerror)

### Miscellaneous

- [Composite Name Format](/documentation/addressbook/1619815-composite-name-format)

#### Constants

- [var kABPersonCompositeNameFormatFirstNameFirst: Int](/documentation/addressbook/kabpersoncompositenameformatfirstnamefirst)
- [var kABPersonCompositeNameFormatLastNameFirst: Int](/documentation/addressbook/kabpersoncompositenameformatlastnamefirst)
- [Record Property Types](/documentation/addressbook/1614731-record-property-types)

#### Constants

- [var kABInvalidPropertyType: Int](/documentation/addressbook/kabinvalidpropertytype)
- [var kABStringPropertyType: Int](/documentation/addressbook/kabstringpropertytype)
- [var kABIntegerPropertyType: Int](/documentation/addressbook/kabintegerpropertytype)
- [var kABRealPropertyType: Int](/documentation/addressbook/kabrealpropertytype)
- [var kABDateTimePropertyType: Int](/documentation/addressbook/kabdatetimepropertytype)
- [var kABDictionaryPropertyType: Int](/documentation/addressbook/kabdictionarypropertytype)
- [var kABMultiStringPropertyType: Int](/documentation/addressbook/kabmultistringpropertytype)
- [var kABMultiIntegerPropertyType: Int](/documentation/addressbook/kabmultiintegerpropertytype)
- [var kABMultiRealPropertyType: Int](/documentation/addressbook/kabmultirealpropertytype)
- [var kABMultiDateTimePropertyType: Int](/documentation/addressbook/kabmultidatetimepropertytype)
- [var kABMultiDictionaryPropertyType: Int](/documentation/addressbook/kabmultidictionarypropertytype)
- [Record Types](/documentation/addressbook/1614747-record-types)

#### Constants

- [var kABPersonType: Int](/documentation/addressbook/kabpersontype)
- [var kABGroupType: Int](/documentation/addressbook/kabgrouptype)
- [var kABSourceType: Int](/documentation/addressbook/kabsourcetype)
- [Sort Order](/documentation/addressbook/1619730-sort-order)

#### Constants

- [var kABPersonSortByFirstName: Int](/documentation/addressbook/kabpersonsortbyfirstname)
- [var kABPersonSortByLastName: Int](/documentation/addressbook/kabpersonsortbylastname)
- [Source Types](/documentation/addressbook/1619878-source-types)

#### Constants

- [var kABSourceTypeLocal: Int](/documentation/addressbook/kabsourcetypelocal)
- [var kABSourceTypeExchange: Int](/documentation/addressbook/kabsourcetypeexchange)
- [var kABSourceTypeExchangeGAL: Int](/documentation/addressbook/kabsourcetypeexchangegal)
- [var kABSourceTypeMobileMe: Int](/documentation/addressbook/kabsourcetypemobileme)
- [var kABSourceTypeLDAP: Int](/documentation/addressbook/kabsourcetypeldap)
- [var kABSourceTypeCardDAV: Int](/documentation/addressbook/kabsourcetypecarddav)
- [var kABSourceTypeCardDAVSearch: Int](/documentation/addressbook/kabsourcetypecarddavsearch)

### Deprecated

- [ABAuthorizationStatus](/documentation/addressbook/abauthorizationstatus)

#### Constants

- [case notDetermined](/documentation/addressbook/abauthorizationstatus/notdetermined)
- [case restricted](/documentation/addressbook/abauthorizationstatus/restricted)
- [case denied](/documentation/addressbook/abauthorizationstatus/denied)
- [case authorized](/documentation/addressbook/abauthorizationstatus/authorized)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/addressbook/abauthorizationstatus/init(rawvalue:))
- [ABPersonImageFormat](/documentation/addressbook/abpersonimageformat)

#### Constants

- [init(UInt32)](/documentation/addressbook/abpersonimageformat/init(_:))
- [init(rawValue: UInt32)](/documentation/addressbook/abpersonimageformat/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/addressbook/abpersonimageformat/rawvalue)
- [var kABPersonImageFormatOriginalSize: ABPersonImageFormat](/documentation/addressbook/kabpersonimageformatoriginalsize)
- [var kABPersonImageFormatThumbnail: ABPersonImageFormat](/documentation/addressbook/kabpersonimageformatthumbnail)
- [AddressBook Data Types](/documentation/addressbook/addressbook-data-types)

### Callbacks

- [ABImageClientCallback](/documentation/addressbook/abimageclientcallback)

### Miscellaneous

- [ABPropertyType](/documentation/addressbook/abpropertytype)

#### Constants

- [var kABErrorInProperty: _ABPropertyType](/documentation/addressbook/kaberrorinproperty)
- [var kABStringProperty: _ABPropertyType](/documentation/addressbook/kabstringproperty)
- [var kABIntegerProperty: _ABPropertyType](/documentation/addressbook/kabintegerproperty)
- [var kABRealProperty: _ABPropertyType](/documentation/addressbook/kabrealproperty)
- [var kABDateProperty: _ABPropertyType](/documentation/addressbook/kabdateproperty)
- [var kABArrayProperty: _ABPropertyType](/documentation/addressbook/kabarrayproperty)
- [var kABDictionaryProperty: _ABPropertyType](/documentation/addressbook/kabdictionaryproperty)
- [var kABDataProperty: _ABPropertyType](/documentation/addressbook/kabdataproperty)
- [var kABMultiStringProperty: _ABPropertyType](/documentation/addressbook/kabmultistringproperty)
- [var kABMultiIntegerProperty: _ABPropertyType](/documentation/addressbook/kabmultiintegerproperty)
- [var kABMultiRealProperty: _ABPropertyType](/documentation/addressbook/kabmultirealproperty)
- [var kABMultiDateProperty: _ABPropertyType](/documentation/addressbook/kabmultidateproperty)
- [var kABMultiArrayProperty: _ABPropertyType](/documentation/addressbook/kabmultiarrayproperty)
- [var kABMultiDictionaryProperty: _ABPropertyType](/documentation/addressbook/kabmultidictionaryproperty)
- [var kABMultiDataProperty: _ABPropertyType](/documentation/addressbook/kabmultidataproperty)
- [ABSearchComparison](/documentation/addressbook/absearchcomparison)

#### Constants

- [var kABEqual: _ABSearchComparison](/documentation/addressbook/kabequal)
- [var kABNotEqual: _ABSearchComparison](/documentation/addressbook/kabnotequal)
- [var kABNotEqualCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabnotequalcaseinsensitive)
- [var kABLessThan: _ABSearchComparison](/documentation/addressbook/kablessthan)
- [var kABLessThanOrEqual: _ABSearchComparison](/documentation/addressbook/kablessthanorequal)
- [var kABGreaterThan: _ABSearchComparison](/documentation/addressbook/kabgreaterthan)
- [var kABGreaterThanOrEqual: _ABSearchComparison](/documentation/addressbook/kabgreaterthanorequal)
- [var kABEqualCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabequalcaseinsensitive)
- [var kABContainsSubString: _ABSearchComparison](/documentation/addressbook/kabcontainssubstring)
- [var kABContainsSubStringCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabcontainssubstringcaseinsensitive)
- [var kABPrefixMatch: _ABSearchComparison](/documentation/addressbook/kabprefixmatch)
- [var kABPrefixMatchCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabprefixmatchcaseinsensitive)
- [var kABSuffixMatch: _ABSearchComparison](/documentation/addressbook/kabsuffixmatch)
- [var kABSuffixMatchCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabsuffixmatchcaseinsensitive)
- [var kABBitsInBitFieldMatch: _ABSearchComparison](/documentation/addressbook/kabbitsinbitfieldmatch)
- [var kABDoesNotContainSubString: _ABSearchComparison](/documentation/addressbook/kabdoesnotcontainsubstring)
- [var kABDoesNotContainSubStringCaseInsensitive: _ABSearchComparison](/documentation/addressbook/kabdoesnotcontainsubstringcaseinsensitive)
- [var kABWithinIntervalAroundToday: _ABSearchComparison](/documentation/addressbook/kabwithinintervalaroundtoday)
- [var kABWithinIntervalAroundTodayYearless: _ABSearchComparison](/documentation/addressbook/kabwithinintervalaroundtodayyearless)
- [var kABNotWithinIntervalAroundToday: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalaroundtoday)
- [var kABNotWithinIntervalAroundTodayYearless: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalaroundtodayyearless)
- [var kABWithinIntervalFromToday: _ABSearchComparison](/documentation/addressbook/kabwithinintervalfromtoday)
- [var kABWithinIntervalFromTodayYearless: _ABSearchComparison](/documentation/addressbook/kabwithinintervalfromtodayyearless)
- [var kABNotWithinIntervalFromToday: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalfromtoday)
- [var kABNotWithinIntervalFromTodayYearless: _ABSearchComparison](/documentation/addressbook/kabnotwithinintervalfromtodayyearless)
- [ABSearchConjunction](/documentation/addressbook/absearchconjunction)

#### Constants

- [var kABSearchAnd: _ABSearchConjunction](/documentation/addressbook/kabsearchand)
- [var kABSearchOr: _ABSearchConjunction](/documentation/addressbook/kabsearchor)

### Deprecated

- [ABAddressBookRequestAccessCompletionHandler](/documentation/addressbook/abaddressbookrequestaccesscompletionhandler)
- [ABExternalChangeCallback](/documentation/addressbook/abexternalchangecallback)
- [ABMultiValueIdentifier](/documentation/addressbook/abmultivalueidentifier)
- [ABPersonCompositeNameFormat](/documentation/addressbook/abpersoncompositenameformat)
- [ABPersonSortOrdering](/documentation/addressbook/abpersonsortordering)
- [ABPropertyID](/documentation/addressbook/abpropertyid)
- [ABRecordID](/documentation/addressbook/abrecordid)
- [ABRecordType](/documentation/addressbook/abrecordtype)
- [ABSourceType](/documentation/addressbook/absourcetype)

## Deprecated symbols

- [Deprecated symbols](/documentation/addressbook/deprecated-symbols)

### Deprecated classes

- [func ABGroupAddMember(ABRecord!, ABRecord!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abgroupaddmember(_:_:))
- [func ABGroupRemoveMember(ABRecord!, ABRecord!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abgroupremovemember(_:_:))
- [func ABMultiValueCreateMutable(ABPropertyType) -> Unmanaged<ABMutableMultiValue>!](/documentation/addressbook/abmultivaluecreatemutable())
- [func ABPersonSetImageData(ABRecord!, CFData!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abpersonsetimagedata(_:_:))
- [func ABRecordRemoveValue(ABRecord!, ABPropertyID, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abrecordremovevalue(_:_:))
- [func ABRecordSetValue(ABRecord!, ABPropertyID, CFTypeRef!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/addressbook/abrecordsetvalue(_:_:_:))
- [ABAddressBook](/documentation/addressbook/abaddressbookref)
- [ABMultiValue](/documentation/addressbook/abmultivalueref)
- [ABMutableMultiValue](/documentation/addressbook/abmutablemultivalueref)
- [ABRecord](/documentation/addressbook/abrecordref)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
