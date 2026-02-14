# Contacts Documentation

Source: https://sosumi.ai/documentation/contacts

---
title: Contacts
source: https://developer.apple.com/documentation/contacts
timestamp: 2026-02-13T19:23:03.915Z
---

## Essentials

- [Accessing the contact store](/documentation/contacts/accessing-the-contact-store)
- [Accessing a person’s contact data using Contacts and ContactsUI](/documentation/contacts/accessing-a-person-s-contact-data-using-contacts-and-contactsui)
- [CNContactStore](/documentation/contacts/cncontactstore)

### Requesting access to the user’s contacts

- [func requestAccess(for: CNEntityType, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/contacts/cncontactstore/requestaccess(for:completionhandler:))
- [class func authorizationStatus(for: CNEntityType) -> CNAuthorizationStatus](/documentation/contacts/cncontactstore/authorizationstatus(for:))
- [CNAuthorizationStatus](/documentation/contacts/cnauthorizationstatus)

#### Authorization statuses

- [case notDetermined](/documentation/contacts/cnauthorizationstatus/notdetermined)
- [case restricted](/documentation/contacts/cnauthorizationstatus/restricted)
- [case denied](/documentation/contacts/cnauthorizationstatus/denied)
- [case authorized](/documentation/contacts/cnauthorizationstatus/authorized)
- [case limited](/documentation/contacts/cnauthorizationstatus/limited)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cnauthorizationstatus/init(rawvalue:))
- [CNEntityType](/documentation/contacts/cnentitytype)

#### Entities

- [case contacts](/documentation/contacts/cnentitytype/contacts)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cnentitytype/init(rawvalue:))

### Fetching contacts

- [func enumerateContacts(with: CNContactFetchRequest, usingBlock: (CNContact, UnsafeMutablePointer<ObjCBool>) -> Void) throws](/documentation/contacts/cncontactstore/enumeratecontacts(with:usingblock:))
- [func unifiedMeContactWithKeys(toFetch: [any CNKeyDescriptor]) throws -> CNContact](/documentation/contacts/cncontactstore/unifiedmecontactwithkeys(tofetch:))
- [func unifiedContact(withIdentifier: String, keysToFetch: [any CNKeyDescriptor]) throws -> CNContact](/documentation/contacts/cncontactstore/unifiedcontact(withidentifier:keystofetch:))
- [func unifiedContacts(matching: NSPredicate, keysToFetch: [any CNKeyDescriptor]) throws -> [CNContact]](/documentation/contacts/cncontactstore/unifiedcontacts(matching:keystofetch:))

### Fetching groups and containers

- [func defaultContainerIdentifier() -> String](/documentation/contacts/cncontactstore/defaultcontaineridentifier())
- [func groups(matching: NSPredicate?) throws -> [CNGroup]](/documentation/contacts/cncontactstore/groups(matching:))
- [func containers(matching: NSPredicate?) throws -> [CNContainer]](/documentation/contacts/cncontactstore/containers(matching:))

### Fetching change history info

- [var currentHistoryToken: Data?](/documentation/contacts/cncontactstore/currenthistorytoken)

### Saving changes

- [func execute(CNSaveRequest) throws](/documentation/contacts/cncontactstore/execute(_:))

### Responding to contact store changes

- [static let CNContactStoreDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/cncontactstoredidchange)
- [NSContactsUsageDescription](/documentation/bundleresources/information-property-list/nscontactsusagedescription)
- [com.apple.developer.contacts.notes](/documentation/bundleresources/entitlements/com.apple.developer.contacts.notes)

## Contact data

- [CNContact](/documentation/contacts/cncontact)

### Identifying the Contact

- [var identifier: String](/documentation/contacts/cncontact/identifier)
- [var contactType: CNContactType](/documentation/contacts/cncontact/contacttype)
- [CNContactType](/documentation/contacts/cncontacttype)

#### Constants

- [case person](/documentation/contacts/cncontacttype/person)
- [case organization](/documentation/contacts/cncontacttype/organization)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cncontacttype/init(rawvalue:))

### Getting Name Information

- [var namePrefix: String](/documentation/contacts/cncontact/nameprefix)
- [var givenName: String](/documentation/contacts/cncontact/givenname)
- [var middleName: String](/documentation/contacts/cncontact/middlename)
- [var familyName: String](/documentation/contacts/cncontact/familyname)
- [var previousFamilyName: String](/documentation/contacts/cncontact/previousfamilyname)
- [var nameSuffix: String](/documentation/contacts/cncontact/namesuffix)
- [var nickname: String](/documentation/contacts/cncontact/nickname)
- [var phoneticGivenName: String](/documentation/contacts/cncontact/phoneticgivenname)
- [var phoneticMiddleName: String](/documentation/contacts/cncontact/phoneticmiddlename)
- [var phoneticFamilyName: String](/documentation/contacts/cncontact/phoneticfamilyname)

### Getting Work Information

- [var jobTitle: String](/documentation/contacts/cncontact/jobtitle)
- [var departmentName: String](/documentation/contacts/cncontact/departmentname)
- [var organizationName: String](/documentation/contacts/cncontact/organizationname)
- [var phoneticOrganizationName: String](/documentation/contacts/cncontact/phoneticorganizationname)

### Getting Addresses

- [var postalAddresses: [CNLabeledValue<CNPostalAddress>]](/documentation/contacts/cncontact/postaladdresses)
- [var emailAddresses: [CNLabeledValue<NSString>]](/documentation/contacts/cncontact/emailaddresses)
- [var urlAddresses: [CNLabeledValue<NSString>]](/documentation/contacts/cncontact/urladdresses)

### Getting Phone Information

- [var phoneNumbers: [CNLabeledValue<CNPhoneNumber>]](/documentation/contacts/cncontact/phonenumbers)

### Getting Social Profiles

- [var socialProfiles: [CNLabeledValue<CNSocialProfile>]](/documentation/contacts/cncontact/socialprofiles)

### Getting Birthday Information

- [var birthday: DateComponents?](/documentation/contacts/cncontact/birthday)
- [var nonGregorianBirthday: DateComponents?](/documentation/contacts/cncontact/nongregorianbirthday)
- [var dates: [CNLabeledValue<NSDateComponents>]](/documentation/contacts/cncontact/dates)

### Getting Notes

- [var note: String](/documentation/contacts/cncontact/note)

### Getting Contact Images

- [var imageData: Data?](/documentation/contacts/cncontact/imagedata)
- [var thumbnailImageData: Data?](/documentation/contacts/cncontact/thumbnailimagedata)
- [var imageDataAvailable: Bool](/documentation/contacts/cncontact/imagedataavailable)

### Getting Related Information

- [var contactRelations: [CNLabeledValue<CNContactRelation>]](/documentation/contacts/cncontact/contactrelations)
- [var instantMessageAddresses: [CNLabeledValue<CNInstantMessageAddress>]](/documentation/contacts/cncontact/instantmessageaddresses)

### Localizing Contact Data

- [class func localizedString(forKey: String) -> String](/documentation/contacts/cncontact/localizedstring(forkey:))

### Comparing Contacts

- [class func descriptorForAllComparatorKeys() -> any CNKeyDescriptor](/documentation/contacts/cncontact/descriptorforallcomparatorkeys())
- [class func comparator(forNameSortOrder: CNContactSortOrder) -> Comparator](/documentation/contacts/cncontact/comparator(fornamesortorder:))
- [func isUnifiedWithContact(withIdentifier: String) -> Bool](/documentation/contacts/cncontact/isunifiedwithcontact(withidentifier:))
- [CNContactSortOrder](/documentation/contacts/cncontactsortorder)

#### Sort Orders

- [case none](/documentation/contacts/cncontactsortorder/none)
- [case userDefault](/documentation/contacts/cncontactsortorder/userdefault)
- [case givenName](/documentation/contacts/cncontactsortorder/givenname)
- [case familyName](/documentation/contacts/cncontactsortorder/familyname)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cncontactsortorder/init(rawvalue:))

### Checking the Availability of Data

- [func isKeyAvailable(String) -> Bool](/documentation/contacts/cncontact/iskeyavailable(_:))
- [func areKeysAvailable([any CNKeyDescriptor]) -> Bool](/documentation/contacts/cncontact/arekeysavailable(_:))

### Getting Search Predicates

- [class func predicateForContacts(matchingName: String) -> NSPredicate](/documentation/contacts/cncontact/predicateforcontacts(matchingname:))
- [class func predicateForContacts(withIdentifiers: [String]) -> NSPredicate](/documentation/contacts/cncontact/predicateforcontacts(withidentifiers:))
- [class func predicateForContactsInGroup(withIdentifier: String) -> NSPredicate](/documentation/contacts/cncontact/predicateforcontactsingroup(withidentifier:))
- [class func predicateForContactsInContainer(withIdentifier: String) -> NSPredicate](/documentation/contacts/cncontact/predicateforcontactsincontainer(withidentifier:))
- [class func predicateForContacts(matching: CNPhoneNumber) -> NSPredicate](/documentation/contacts/cncontact/predicateforcontacts(matching:))
- [class func predicateForContacts(matchingEmailAddress: String) -> NSPredicate](/documentation/contacts/cncontact/predicateforcontacts(matchingemailaddress:))
- [CNMutableContact](/documentation/contacts/cnmutablecontact)

### Setting the Identity of the Contact

- [var contactType: CNContactType](/documentation/contacts/cnmutablecontact/contacttype)

### Setting Name Information

- [var namePrefix: String](/documentation/contacts/cnmutablecontact/nameprefix)
- [var givenName: String](/documentation/contacts/cnmutablecontact/givenname)
- [var middleName: String](/documentation/contacts/cnmutablecontact/middlename)
- [var familyName: String](/documentation/contacts/cnmutablecontact/familyname)
- [var previousFamilyName: String](/documentation/contacts/cnmutablecontact/previousfamilyname)
- [var nameSuffix: String](/documentation/contacts/cnmutablecontact/namesuffix)
- [var nickname: String](/documentation/contacts/cnmutablecontact/nickname)
- [var phoneticGivenName: String](/documentation/contacts/cnmutablecontact/phoneticgivenname)
- [var phoneticMiddleName: String](/documentation/contacts/cnmutablecontact/phoneticmiddlename)
- [var phoneticFamilyName: String](/documentation/contacts/cnmutablecontact/phoneticfamilyname)

### Setting Work Information

- [var jobTitle: String](/documentation/contacts/cnmutablecontact/jobtitle)
- [var departmentName: String](/documentation/contacts/cnmutablecontact/departmentname)
- [var organizationName: String](/documentation/contacts/cnmutablecontact/organizationname)
- [var phoneticOrganizationName: String](/documentation/contacts/cnmutablecontact/phoneticorganizationname)

### Setting Addresses

- [var postalAddresses: [CNLabeledValue<CNPostalAddress>]](/documentation/contacts/cnmutablecontact/postaladdresses)
- [var emailAddresses: [CNLabeledValue<NSString>]](/documentation/contacts/cnmutablecontact/emailaddresses)
- [var urlAddresses: [CNLabeledValue<NSString>]](/documentation/contacts/cnmutablecontact/urladdresses)

### Setting Phone Information

- [var phoneNumbers: [CNLabeledValue<CNPhoneNumber>]](/documentation/contacts/cnmutablecontact/phonenumbers)

### Setting Social Profiles

- [var socialProfiles: [CNLabeledValue<CNSocialProfile>]](/documentation/contacts/cnmutablecontact/socialprofiles)

### Setting Birthday Information

- [var dates: [CNLabeledValue<NSDateComponents>]](/documentation/contacts/cnmutablecontact/dates)
- [var nonGregorianBirthday: DateComponents?](/documentation/contacts/cnmutablecontact/nongregorianbirthday)
- [var birthday: DateComponents?](/documentation/contacts/cnmutablecontact/birthday)

### Setting Notes

- [var note: String](/documentation/contacts/cnmutablecontact/note)

### Setting Images

- [var imageData: Data?](/documentation/contacts/cnmutablecontact/imagedata)

### Relating Other Information to the Contact

- [var contactRelations: [CNLabeledValue<CNContactRelation>]](/documentation/contacts/cnmutablecontact/contactrelations)
- [var instantMessageAddresses: [CNLabeledValue<CNInstantMessageAddress>]](/documentation/contacts/cnmutablecontact/instantmessageaddresses)

### Instance Properties

- [var id: UUID](/documentation/contacts/cnmutablecontact/id)
- [Data Objects](/documentation/contacts/data-objects)

### Addresses

- [CNPostalAddress](/documentation/contacts/cnpostaladdress)

#### Getting the Parts of a Postal Address

- [var street: String](/documentation/contacts/cnpostaladdress/street)
- [var city: String](/documentation/contacts/cnpostaladdress/city)
- [var state: String](/documentation/contacts/cnpostaladdress/state)
- [var postalCode: String](/documentation/contacts/cnpostaladdress/postalcode)
- [var country: String](/documentation/contacts/cnpostaladdress/country)
- [var isoCountryCode: String](/documentation/contacts/cnpostaladdress/isocountrycode)
- [var subAdministrativeArea: String](/documentation/contacts/cnpostaladdress/subadministrativearea)
- [var subLocality: String](/documentation/contacts/cnpostaladdress/sublocality)

#### Getting Localized Postal Values

- [class func localizedString(forKey: String) -> String](/documentation/contacts/cnpostaladdress/localizedstring(forkey:))
- [let CNPostalAddressStreetKey: String](/documentation/contacts/cnpostaladdressstreetkey)
- [let CNPostalAddressCityKey: String](/documentation/contacts/cnpostaladdresscitykey)
- [let CNPostalAddressStateKey: String](/documentation/contacts/cnpostaladdressstatekey)
- [let CNPostalAddressPostalCodeKey: String](/documentation/contacts/cnpostaladdresspostalcodekey)
- [let CNPostalAddressCountryKey: String](/documentation/contacts/cnpostaladdresscountrykey)
- [let CNPostalAddressISOCountryCodeKey: String](/documentation/contacts/cnpostaladdressisocountrycodekey)
- [CNMutablePostalAddress](/documentation/contacts/cnmutablepostaladdress)

#### Modifying the Parts of a Postal Address

- [var street: String](/documentation/contacts/cnmutablepostaladdress/street)
- [var city: String](/documentation/contacts/cnmutablepostaladdress/city)
- [var state: String](/documentation/contacts/cnmutablepostaladdress/state)
- [var postalCode: String](/documentation/contacts/cnmutablepostaladdress/postalcode)
- [var country: String](/documentation/contacts/cnmutablepostaladdress/country)
- [var isoCountryCode: String](/documentation/contacts/cnmutablepostaladdress/isocountrycode)
- [var subAdministrativeArea: String](/documentation/contacts/cnmutablepostaladdress/subadministrativearea)
- [var subLocality: String](/documentation/contacts/cnmutablepostaladdress/sublocality)
- [CNInstantMessageAddress](/documentation/contacts/cninstantmessageaddress)

#### Creating an Instant Message Address

- [init(username: String, service: String)](/documentation/contacts/cninstantmessageaddress/init(username:service:))

#### Getting the Address Information

- [var service: String](/documentation/contacts/cninstantmessageaddress/service)
- [var username: String](/documentation/contacts/cninstantmessageaddress/username)

#### Getting Localized Address Information

- [class func localizedString(forKey: String) -> String](/documentation/contacts/cninstantmessageaddress/localizedstring(forkey:))
- [let CNInstantMessageAddressUsernameKey: String](/documentation/contacts/cninstantmessageaddressusernamekey)
- [let CNInstantMessageAddressServiceKey: String](/documentation/contacts/cninstantmessageaddressservicekey)

#### Getting Localized Service Names

- [class func localizedString(forService: String) -> String](/documentation/contacts/cninstantmessageaddress/localizedstring(forservice:))
- [let CNInstantMessageServiceAIM: String](/documentation/contacts/cninstantmessageserviceaim)
- [let CNInstantMessageServiceFacebook: String](/documentation/contacts/cninstantmessageservicefacebook)
- [let CNInstantMessageServiceGaduGadu: String](/documentation/contacts/cninstantmessageservicegadugadu)
- [let CNInstantMessageServiceGoogleTalk: String](/documentation/contacts/cninstantmessageservicegoogletalk)
- [let CNInstantMessageServiceICQ: String](/documentation/contacts/cninstantmessageserviceicq)
- [let CNInstantMessageServiceJabber: String](/documentation/contacts/cninstantmessageservicejabber)
- [let CNInstantMessageServiceMSN: String](/documentation/contacts/cninstantmessageservicemsn)
- [let CNInstantMessageServiceQQ: String](/documentation/contacts/cninstantmessageserviceqq)
- [let CNInstantMessageServiceSkype: String](/documentation/contacts/cninstantmessageserviceskype)
- [let CNInstantMessageServiceYahoo: String](/documentation/contacts/cninstantmessageserviceyahoo)

### Phone Numbers

- [CNPhoneNumber](/documentation/contacts/cnphonenumber)

#### Creating a Phone Number Object

- [init(stringValue: String)](/documentation/contacts/cnphonenumber/init(stringvalue:))

#### Getting the Phone Number

- [var stringValue: String](/documentation/contacts/cnphonenumber/stringvalue)

#### Getting Phone-Related Keys

- [let CNContactPhoneNumbersKey: String](/documentation/contacts/cncontactphonenumberskey)

#### Deprecated

- [init!()](/documentation/contacts/cnphonenumber/init())
- [class func new() -> Self!](/documentation/contacts/cnphonenumber/new())

### Groups and Containers

- [CNGroup](/documentation/contacts/cngroup)

#### Getting the Group Information

- [var name: String](/documentation/contacts/cngroup/name)
- [var identifier: String](/documentation/contacts/cngroup/identifier)

#### Generating Search Predicates for Groups

- [class func predicateForGroups(withIdentifiers: [String]) -> NSPredicate](/documentation/contacts/cngroup/predicateforgroups(withidentifiers:))
- [class func predicateForGroupsInContainer(withIdentifier: String) -> NSPredicate](/documentation/contacts/cngroup/predicateforgroupsincontainer(withidentifier:))
- [class func predicateForSubgroupsInGroup(withIdentifier: String) -> NSPredicate](/documentation/contacts/cngroup/predicateforsubgroupsingroup(withidentifier:))

#### Getting Group-Related Keys

- [let CNGroupIdentifierKey: String](/documentation/contacts/cngroupidentifierkey)
- [let CNGroupNameKey: String](/documentation/contacts/cngroupnamekey)
- [CNMutableGroup](/documentation/contacts/cnmutablegroup)

#### Modifying the Group Name

- [var name: String](/documentation/contacts/cnmutablegroup/name)
- [CNContainer](/documentation/contacts/cncontainer)

#### Getting the Container Information

- [var name: String](/documentation/contacts/cncontainer/name)
- [var identifier: String](/documentation/contacts/cncontainer/identifier)
- [var type: CNContainerType](/documentation/contacts/cncontainer/type)
- [CNContainerType](/documentation/contacts/cncontainertype)

##### Constants

- [case local](/documentation/contacts/cncontainertype/local)
- [case exchange](/documentation/contacts/cncontainertype/exchange)
- [case cardDAV](/documentation/contacts/cncontainertype/carddav)
- [case unassigned](/documentation/contacts/cncontainertype/unassigned)

##### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cncontainertype/init(rawvalue:))

#### Generating Search Predicates for Containers

- [class func predicateForContainerOfContact(withIdentifier: String) -> NSPredicate](/documentation/contacts/cncontainer/predicateforcontainerofcontact(withidentifier:))
- [class func predicateForContainers(withIdentifiers: [String]) -> NSPredicate](/documentation/contacts/cncontainer/predicateforcontainers(withidentifiers:))
- [class func predicateForContainerOfGroup(withIdentifier: String) -> NSPredicate](/documentation/contacts/cncontainer/predicateforcontainerofgroup(withidentifier:))

#### Getting Container-Related Keys

- [let CNContainerIdentifierKey: String](/documentation/contacts/cncontaineridentifierkey)
- [let CNContainerNameKey: String](/documentation/contacts/cncontainernamekey)
- [let CNContainerTypeKey: String](/documentation/contacts/cncontainertypekey)

### Social Profiles

- [CNSocialProfile](/documentation/contacts/cnsocialprofile)

#### Creating a Social Profile Object

- [init(urlString: String?, username: String?, userIdentifier: String?, service: String?)](/documentation/contacts/cnsocialprofile/init(urlstring:username:useridentifier:service:))

#### Getting Social Profile Information

- [var username: String](/documentation/contacts/cnsocialprofile/username)
- [var service: String](/documentation/contacts/cnsocialprofile/service)
- [var urlString: String](/documentation/contacts/cnsocialprofile/urlstring)
- [var userIdentifier: String](/documentation/contacts/cnsocialprofile/useridentifier)

#### Getting Localized User Profile Information

- [class func localizedString(forKey: String) -> String](/documentation/contacts/cnsocialprofile/localizedstring(forkey:))
- [let CNSocialProfileUsernameKey: String](/documentation/contacts/cnsocialprofileusernamekey)
- [let CNSocialProfileServiceKey: String](/documentation/contacts/cnsocialprofileservicekey)
- [let CNSocialProfileURLStringKey: String](/documentation/contacts/cnsocialprofileurlstringkey)
- [let CNSocialProfileUserIdentifierKey: String](/documentation/contacts/cnsocialprofileuseridentifierkey)

#### Getting Localized Service Names

- [class func localizedString(forService: String) -> String](/documentation/contacts/cnsocialprofile/localizedstring(forservice:))
- [let CNSocialProfileServiceFacebook: String](/documentation/contacts/cnsocialprofileservicefacebook)
- [let CNSocialProfileServiceFlickr: String](/documentation/contacts/cnsocialprofileserviceflickr)
- [let CNSocialProfileServiceGameCenter: String](/documentation/contacts/cnsocialprofileservicegamecenter)
- [let CNSocialProfileServiceLinkedIn: String](/documentation/contacts/cnsocialprofileservicelinkedin)
- [let CNSocialProfileServiceMySpace: String](/documentation/contacts/cnsocialprofileservicemyspace)
- [let CNSocialProfileServiceSinaWeibo: String](/documentation/contacts/cnsocialprofileservicesinaweibo)
- [let CNSocialProfileServiceTencentWeibo: String](/documentation/contacts/cnsocialprofileservicetencentweibo)
- [let CNSocialProfileServiceTwitter: String](/documentation/contacts/cnsocialprofileservicetwitter)
- [let CNSocialProfileServiceYelp: String](/documentation/contacts/cnsocialprofileserviceyelp)

### Related Data

- [CNContactRelation](/documentation/contacts/cncontactrelation)

#### Creating a Contact Relation Object

- [init(name: String)](/documentation/contacts/cncontactrelation/init(name:))

#### Getting the Relation Name

- [var name: String](/documentation/contacts/cncontactrelation/name)

#### Getting the Common Relationship Labels

- [let CNLabelContactRelationSpouse: String](/documentation/contacts/cnlabelcontactrelationspouse)
- [let CNLabelContactRelationPartner: String](/documentation/contacts/cnlabelcontactrelationpartner)
- [let CNLabelContactRelationDaughter: String](/documentation/contacts/cnlabelcontactrelationdaughter)
- [let CNLabelContactRelationSon: String](/documentation/contacts/cnlabelcontactrelationson)
- [let CNLabelContactRelationChild: String](/documentation/contacts/cnlabelcontactrelationchild)
- [let CNLabelContactRelationFather: String](/documentation/contacts/cnlabelcontactrelationfather)
- [let CNLabelContactRelationMother: String](/documentation/contacts/cnlabelcontactrelationmother)
- [let CNLabelContactRelationParent: String](/documentation/contacts/cnlabelcontactrelationparent)
- [let CNLabelContactRelationBrother: String](/documentation/contacts/cnlabelcontactrelationbrother)
- [let CNLabelContactRelationSister: String](/documentation/contacts/cnlabelcontactrelationsister)
- [let CNLabelContactRelationFriend: String](/documentation/contacts/cnlabelcontactrelationfriend)
- [let CNLabelContactRelationAssistant: String](/documentation/contacts/cnlabelcontactrelationassistant)
- [let CNLabelContactRelationManager: String](/documentation/contacts/cnlabelcontactrelationmanager)

### Generic Types

- [CNLabeledValue](/documentation/contacts/cnlabeledvalue)

#### Creating a labeled value

- [init(label: String?, value: ValueType)](/documentation/contacts/cnlabeledvalue/init(label:value:))

#### Getting the label and value

- [var label: String?](/documentation/contacts/cnlabeledvalue/label)
- [var value: ValueType](/documentation/contacts/cnlabeledvalue/value)

#### Setting labels and values

- [func settingLabel(String?) -> Self](/documentation/contacts/cnlabeledvalue/settinglabel(_:))
- [func settingLabel(String?, value: ValueType) -> Self](/documentation/contacts/cnlabeledvalue/settinglabel(_:value:))
- [func settingValue(ValueType) -> Self](/documentation/contacts/cnlabeledvalue/settingvalue(_:))

#### Localizing the label and value

- [class func localizedString(forLabel: String) -> String](/documentation/contacts/cnlabeledvalue/localizedstring(forlabel:))

#### Getting the unique identifier

- [var identifier: String](/documentation/contacts/cnlabeledvalue/identifier)

#### Getting common labels

- [let CNLabelHome: String](/documentation/contacts/cnlabelhome)
- [let CNLabelWork: String](/documentation/contacts/cnlabelwork)
- [let CNLabelSchool: String](/documentation/contacts/cnlabelschool)
- [let CNLabelOther: String](/documentation/contacts/cnlabelother)
- [let CNLabelEmailiCloud: String](/documentation/contacts/cnlabelemailicloud)
- [let CNLabelURLAddressHomePage: String](/documentation/contacts/cnlabelurladdresshomepage)
- [let CNLabelDateAnniversary: String](/documentation/contacts/cnlabeldateanniversary)

#### Getting phone number labels

- [let CNLabelPhoneNumberMain: String](/documentation/contacts/cnlabelphonenumbermain)
- [let CNLabelPhoneNumberiPhone: String](/documentation/contacts/cnlabelphonenumberiphone)
- [let CNLabelPhoneNumberAppleWatch: String](/documentation/contacts/cnlabelphonenumberapplewatch)
- [let CNLabelPhoneNumberMobile: String](/documentation/contacts/cnlabelphonenumbermobile)
- [let CNLabelPhoneNumberPager: String](/documentation/contacts/cnlabelphonenumberpager)
- [let CNLabelPhoneNumberWorkFax: String](/documentation/contacts/cnlabelphonenumberworkfax)
- [let CNLabelPhoneNumberHomeFax: String](/documentation/contacts/cnlabelphonenumberhomefax)
- [let CNLabelPhoneNumberOtherFax: String](/documentation/contacts/cnlabelphonenumberotherfax)

#### Getting immediate family relationship labels

- [let CNLabelContactRelationBrother: String](/documentation/contacts/cnlabelcontactrelationbrother)
- [let CNLabelContactRelationChild: String](/documentation/contacts/cnlabelcontactrelationchild)
- [let CNLabelContactRelationDaughter: String](/documentation/contacts/cnlabelcontactrelationdaughter)
- [let CNLabelContactRelationElderBrother: String](/documentation/contacts/cnlabelcontactrelationelderbrother)
- [let CNLabelContactRelationElderSibling: String](/documentation/contacts/cnlabelcontactrelationeldersibling)
- [let CNLabelContactRelationElderSister: String](/documentation/contacts/cnlabelcontactrelationeldersister)
- [let CNLabelContactRelationEldestBrother: String](/documentation/contacts/cnlabelcontactrelationeldestbrother)
- [let CNLabelContactRelationEldestSister: String](/documentation/contacts/cnlabelcontactrelationeldestsister)
- [let CNLabelContactRelationFather: String](/documentation/contacts/cnlabelcontactrelationfather)
- [let CNLabelContactRelationFemalePartner: String](/documentation/contacts/cnlabelcontactrelationfemalepartner)
- [let CNLabelContactRelationHusband: String](/documentation/contacts/cnlabelcontactrelationhusband)
- [let CNLabelContactRelationMalePartner: String](/documentation/contacts/cnlabelcontactrelationmalepartner)
- [let CNLabelContactRelationMother: String](/documentation/contacts/cnlabelcontactrelationmother)
- [let CNLabelContactRelationParent: String](/documentation/contacts/cnlabelcontactrelationparent)
- [let CNLabelContactRelationPartner: String](/documentation/contacts/cnlabelcontactrelationpartner)
- [let CNLabelContactRelationSibling: String](/documentation/contacts/cnlabelcontactrelationsibling)
- [let CNLabelContactRelationSister: String](/documentation/contacts/cnlabelcontactrelationsister)
- [let CNLabelContactRelationSon: String](/documentation/contacts/cnlabelcontactrelationson)
- [let CNLabelContactRelationSpouse: String](/documentation/contacts/cnlabelcontactrelationspouse)
- [let CNLabelContactRelationStepbrother: String](/documentation/contacts/cnlabelcontactrelationstepbrother)
- [let CNLabelContactRelationStepchild: String](/documentation/contacts/cnlabelcontactrelationstepchild)
- [let CNLabelContactRelationStepdaughter: String](/documentation/contacts/cnlabelcontactrelationstepdaughter)
- [let CNLabelContactRelationStepfather: String](/documentation/contacts/cnlabelcontactrelationstepfather)
- [let CNLabelContactRelationStepmother: String](/documentation/contacts/cnlabelcontactrelationstepmother)
- [let CNLabelContactRelationStepparent: String](/documentation/contacts/cnlabelcontactrelationstepparent)
- [let CNLabelContactRelationStepsister: String](/documentation/contacts/cnlabelcontactrelationstepsister)
- [let CNLabelContactRelationStepson: String](/documentation/contacts/cnlabelcontactrelationstepson)
- [let CNLabelContactRelationWife: String](/documentation/contacts/cnlabelcontactrelationwife)
- [let CNLabelContactRelationYoungerBrother: String](/documentation/contacts/cnlabelcontactrelationyoungerbrother)
- [let CNLabelContactRelationYoungerSibling: String](/documentation/contacts/cnlabelcontactrelationyoungersibling)
- [let CNLabelContactRelationYoungerSister: String](/documentation/contacts/cnlabelcontactrelationyoungersister)
- [let CNLabelContactRelationYoungestBrother: String](/documentation/contacts/cnlabelcontactrelationyoungestbrother)
- [let CNLabelContactRelationYoungestSister: String](/documentation/contacts/cnlabelcontactrelationyoungestsister)

#### Getting acquaintance relationship labels

- [let CNLabelContactRelationBoyfriend: String](/documentation/contacts/cnlabelcontactrelationboyfriend)
- [let CNLabelContactRelationColleague: String](/documentation/contacts/cnlabelcontactrelationcolleague)
- [let CNLabelContactRelationFemaleFriend: String](/documentation/contacts/cnlabelcontactrelationfemalefriend)
- [let CNLabelContactRelationFriend: String](/documentation/contacts/cnlabelcontactrelationfriend)
- [let CNLabelContactRelationGirlfriend: String](/documentation/contacts/cnlabelcontactrelationgirlfriend)
- [let CNLabelContactRelationGirlfriendOrBoyfriend: String](/documentation/contacts/cnlabelcontactrelationgirlfriendorboyfriend)
- [let CNLabelContactRelationMaleFriend: String](/documentation/contacts/cnlabelcontactrelationmalefriend)

#### Getting business relationship labels

- [let CNLabelContactRelationAssistant: String](/documentation/contacts/cnlabelcontactrelationassistant)
- [let CNLabelContactRelationManager: String](/documentation/contacts/cnlabelcontactrelationmanager)

#### Getting education relationship labels

- [let CNLabelContactRelationTeacher: String](/documentation/contacts/cnlabelcontactrelationteacher)

#### Getting in-law relationship labels

- [let CNLabelContactRelationBrotherInLaw: String](/documentation/contacts/cnlabelcontactrelationbrotherinlaw)
- [let CNLabelContactRelationBrotherInLawElderSistersHusband: String](/documentation/contacts/cnlabelcontactrelationbrotherinlaweldersistershusband)
- [let CNLabelContactRelationBrotherInLawHusbandsBrother: String](/documentation/contacts/cnlabelcontactrelationbrotherinlawhusbandsbrother)
- [let CNLabelContactRelationBrotherInLawHusbandsSistersHusband: String](/documentation/contacts/cnlabelcontactrelationbrotherinlawhusbandssistershusband)
- [let CNLabelContactRelationBrotherInLawSistersHusband: String](/documentation/contacts/cnlabelcontactrelationbrotherinlawsistershusband)
- [let CNLabelContactRelationBrotherInLawSpousesBrother: String](/documentation/contacts/cnlabelcontactrelationbrotherinlawspousesbrother)
- [let CNLabelContactRelationBrotherInLawWifesBrother: String](/documentation/contacts/cnlabelcontactrelationbrotherinlawwifesbrother)
- [let CNLabelContactRelationBrotherInLawWifesSistersHusband: String](/documentation/contacts/cnlabelcontactrelationbrotherinlawwifessistershusband)
- [let CNLabelContactRelationBrotherInLawYoungerSistersHusband: String](/documentation/contacts/cnlabelcontactrelationbrotherinlawyoungersistershusband)
- [let CNLabelContactRelationChildInLaw: String](/documentation/contacts/cnlabelcontactrelationchildinlaw)
- [let CNLabelContactRelationCoBrotherInLaw: String](/documentation/contacts/cnlabelcontactrelationcobrotherinlaw)
- [let CNLabelContactRelationCoFatherInLaw: String](/documentation/contacts/cnlabelcontactrelationcofatherinlaw)
- [let CNLabelContactRelationCoMotherInLaw: String](/documentation/contacts/cnlabelcontactrelationcomotherinlaw)
- [let CNLabelContactRelationCoParentInLaw: String](/documentation/contacts/cnlabelcontactrelationcoparentinlaw)
- [let CNLabelContactRelationCoSiblingInLaw: String](/documentation/contacts/cnlabelcontactrelationcosiblinginlaw)
- [let CNLabelContactRelationCoSisterInLaw: String](/documentation/contacts/cnlabelcontactrelationcosisterinlaw)
- [let CNLabelContactRelationElderBrotherInLaw: String](/documentation/contacts/cnlabelcontactrelationelderbrotherinlaw)
- [let CNLabelContactRelationElderSiblingInLaw: String](/documentation/contacts/cnlabelcontactrelationeldersiblinginlaw)
- [let CNLabelContactRelationElderSisterInLaw: String](/documentation/contacts/cnlabelcontactrelationeldersisterinlaw)
- [let CNLabelContactRelationFatherInLaw: String](/documentation/contacts/cnlabelcontactrelationfatherinlaw)
- [let CNLabelContactRelationFatherInLawHusbandsFather: String](/documentation/contacts/cnlabelcontactrelationfatherinlawhusbandsfather)
- [let CNLabelContactRelationFatherInLawOrStepfather: String](/documentation/contacts/cnlabelcontactrelationfatherinlaworstepfather)
- [let CNLabelContactRelationFatherInLawWifesFather: String](/documentation/contacts/cnlabelcontactrelationfatherinlawwifesfather)
- [let CNLabelContactRelationMotherInLaw: String](/documentation/contacts/cnlabelcontactrelationmotherinlaw)
- [let CNLabelContactRelationMotherInLawHusbandsMother: String](/documentation/contacts/cnlabelcontactrelationmotherinlawhusbandsmother)
- [let CNLabelContactRelationMotherInLawOrStepmother: String](/documentation/contacts/cnlabelcontactrelationmotherinlaworstepmother)
- [let CNLabelContactRelationMotherInLawWifesMother: String](/documentation/contacts/cnlabelcontactrelationmotherinlawwifesmother)
- [let CNLabelContactRelationParentInLaw: String](/documentation/contacts/cnlabelcontactrelationparentinlaw)
- [let CNLabelContactRelationSiblingInLaw: String](/documentation/contacts/cnlabelcontactrelationsiblinginlaw)
- [let CNLabelContactRelationSisterInLaw: String](/documentation/contacts/cnlabelcontactrelationsisterinlaw)
- [let CNLabelContactRelationSisterInLawBrothersWife: String](/documentation/contacts/cnlabelcontactrelationsisterinlawbrotherswife)
- [let CNLabelContactRelationSisterInLawElderBrothersWife: String](/documentation/contacts/cnlabelcontactrelationsisterinlawelderbrotherswife)
- [let CNLabelContactRelationSisterInLawHusbandsBrothersWife: String](/documentation/contacts/cnlabelcontactrelationsisterinlawhusbandsbrotherswife)
- [let CNLabelContactRelationSisterInLawHusbandsSister: String](/documentation/contacts/cnlabelcontactrelationsisterinlawhusbandssister)
- [let CNLabelContactRelationSisterInLawSpousesSister: String](/documentation/contacts/cnlabelcontactrelationsisterinlawspousessister)
- [let CNLabelContactRelationSisterInLawWifesBrothersWife: String](/documentation/contacts/cnlabelcontactrelationsisterinlawwifesbrotherswife)
- [let CNLabelContactRelationSisterInLawWifesSister: String](/documentation/contacts/cnlabelcontactrelationsisterinlawwifessister)
- [let CNLabelContactRelationSisterInLawYoungerBrothersWife: String](/documentation/contacts/cnlabelcontactrelationsisterinlawyoungerbrotherswife)
- [let CNLabelContactRelationYoungerBrotherInLaw: String](/documentation/contacts/cnlabelcontactrelationyoungerbrotherinlaw)
- [let CNLabelContactRelationYoungerSiblingInLaw: String](/documentation/contacts/cnlabelcontactrelationyoungersiblinginlaw)
- [let CNLabelContactRelationYoungerSisterInLaw: String](/documentation/contacts/cnlabelcontactrelationyoungersisterinlaw)

#### Getting extended family relationship labels

- [let CNLabelContactRelationAunt: String](/documentation/contacts/cnlabelcontactrelationaunt)
- [let CNLabelContactRelationAuntFathersBrothersWife: String](/documentation/contacts/cnlabelcontactrelationauntfathersbrotherswife)
- [let CNLabelContactRelationAuntFathersElderBrothersWife: String](/documentation/contacts/cnlabelcontactrelationauntfatherselderbrotherswife)
- [let CNLabelContactRelationAuntFathersElderSister: String](/documentation/contacts/cnlabelcontactrelationauntfatherseldersister)
- [let CNLabelContactRelationAuntFathersSister: String](/documentation/contacts/cnlabelcontactrelationauntfatherssister)
- [let CNLabelContactRelationAuntFathersYoungerBrothersWife: String](/documentation/contacts/cnlabelcontactrelationauntfathersyoungerbrotherswife)
- [let CNLabelContactRelationAuntFathersYoungerSister: String](/documentation/contacts/cnlabelcontactrelationauntfathersyoungersister)
- [let CNLabelContactRelationAuntMothersBrothersWife: String](/documentation/contacts/cnlabelcontactrelationauntmothersbrotherswife)
- [let CNLabelContactRelationAuntMothersElderSister: String](/documentation/contacts/cnlabelcontactrelationauntmotherseldersister)
- [let CNLabelContactRelationAuntMothersSister: String](/documentation/contacts/cnlabelcontactrelationauntmotherssister)
- [let CNLabelContactRelationAuntMothersYoungerSister: String](/documentation/contacts/cnlabelcontactrelationauntmothersyoungersister)
- [let CNLabelContactRelationAuntParentsElderSister: String](/documentation/contacts/cnlabelcontactrelationauntparentseldersister)
- [let CNLabelContactRelationAuntParentsSister: String](/documentation/contacts/cnlabelcontactrelationauntparentssister)
- [let CNLabelContactRelationAuntParentsYoungerSister: String](/documentation/contacts/cnlabelcontactrelationauntparentsyoungersister)
- [let CNLabelContactRelationCousin: String](/documentation/contacts/cnlabelcontactrelationcousin)
- [let CNLabelContactRelationCousinFathersBrothersDaughter: String](/documentation/contacts/cnlabelcontactrelationcousinfathersbrothersdaughter)
- [let CNLabelContactRelationCousinFathersBrothersSon: String](/documentation/contacts/cnlabelcontactrelationcousinfathersbrothersson)
- [let CNLabelContactRelationCousinFathersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationcousinfatherssistersdaughter)
- [let CNLabelContactRelationCousinFathersSistersSon: String](/documentation/contacts/cnlabelcontactrelationcousinfatherssistersson)
- [let CNLabelContactRelationCousinGrandparentsSiblingsChild: String](/documentation/contacts/cnlabelcontactrelationcousingrandparentssiblingschild)
- [let CNLabelContactRelationCousinGrandparentsSiblingsDaughter: String](/documentation/contacts/cnlabelcontactrelationcousingrandparentssiblingsdaughter)
- [let CNLabelContactRelationCousinGrandparentsSiblingsSon: String](/documentation/contacts/cnlabelcontactrelationcousingrandparentssiblingsson)
- [let CNLabelContactRelationCousinMothersBrothersDaughter: String](/documentation/contacts/cnlabelcontactrelationcousinmothersbrothersdaughter)
- [let CNLabelContactRelationCousinMothersBrothersSon: String](/documentation/contacts/cnlabelcontactrelationcousinmothersbrothersson)
- [let CNLabelContactRelationCousinMothersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationcousinmotherssistersdaughter)
- [let CNLabelContactRelationCousinMothersSistersSon: String](/documentation/contacts/cnlabelcontactrelationcousinmotherssistersson)
- [let CNLabelContactRelationCousinOrSiblingsChild: String](/documentation/contacts/cnlabelcontactrelationcousinorsiblingschild)
- [let CNLabelContactRelationCousinParentsSiblingsChild: String](/documentation/contacts/cnlabelcontactrelationcousinparentssiblingschild)
- [let CNLabelContactRelationCousinParentsSiblingsDaughter: String](/documentation/contacts/cnlabelcontactrelationcousinparentssiblingsdaughter)
- [let CNLabelContactRelationCousinParentsSiblingsSon: String](/documentation/contacts/cnlabelcontactrelationcousinparentssiblingsson)
- [let CNLabelContactRelationDaughterInLaw: String](/documentation/contacts/cnlabelcontactrelationdaughterinlaw)
- [let CNLabelContactRelationDaughterInLawOrSisterInLaw: String](/documentation/contacts/cnlabelcontactrelationdaughterinlaworsisterinlaw)
- [let CNLabelContactRelationDaughterInLawOrStepdaughter: String](/documentation/contacts/cnlabelcontactrelationdaughterinlaworstepdaughter)
- [let CNLabelContactRelationElderCousin: String](/documentation/contacts/cnlabelcontactrelationeldercousin)
- [let CNLabelContactRelationElderCousinFathersBrothersDaughter: String](/documentation/contacts/cnlabelcontactrelationeldercousinfathersbrothersdaughter)
- [let CNLabelContactRelationElderCousinFathersBrothersSon: String](/documentation/contacts/cnlabelcontactrelationeldercousinfathersbrothersson)
- [let CNLabelContactRelationElderCousinFathersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationeldercousinfatherssistersdaughter)
- [let CNLabelContactRelationElderCousinFathersSistersSon: String](/documentation/contacts/cnlabelcontactrelationeldercousinfatherssistersson)
- [let CNLabelContactRelationElderCousinMothersBrothersDaughter: String](/documentation/contacts/cnlabelcontactrelationeldercousinmothersbrothersdaughter)
- [let CNLabelContactRelationElderCousinMothersBrothersSon: String](/documentation/contacts/cnlabelcontactrelationeldercousinmothersbrothersson)
- [let CNLabelContactRelationElderCousinMothersSiblingsDaughterOrFathersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationeldercousinmotherssiblingsdaughterorfatherssistersdaughter)
- [let CNLabelContactRelationElderCousinMothersSiblingsSonOrFathersSistersSon: String](/documentation/contacts/cnlabelcontactrelationeldercousinmotherssiblingssonorfatherssistersson)
- [let CNLabelContactRelationElderCousinMothersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationeldercousinmotherssistersdaughter)
- [let CNLabelContactRelationElderCousinMothersSistersSon: String](/documentation/contacts/cnlabelcontactrelationeldercousinmotherssistersson)
- [let CNLabelContactRelationElderCousinParentsSiblingsDaughter: String](/documentation/contacts/cnlabelcontactrelationeldercousinparentssiblingsdaughter)
- [let CNLabelContactRelationElderCousinParentsSiblingsSon: String](/documentation/contacts/cnlabelcontactrelationeldercousinparentssiblingsson)
- [let CNLabelContactRelationFemaleCousin: String](/documentation/contacts/cnlabelcontactrelationfemalecousin)
- [let CNLabelContactRelationGrandaunt: String](/documentation/contacts/cnlabelcontactrelationgrandaunt)
- [let CNLabelContactRelationGrandchild: String](/documentation/contacts/cnlabelcontactrelationgrandchild)
- [let CNLabelContactRelationGrandchildOrSiblingsChild: String](/documentation/contacts/cnlabelcontactrelationgrandchildorsiblingschild)
- [let CNLabelContactRelationGranddaughter: String](/documentation/contacts/cnlabelcontactrelationgranddaughter)
- [let CNLabelContactRelationGranddaughterDaughtersDaughter: String](/documentation/contacts/cnlabelcontactrelationgranddaughterdaughtersdaughter)
- [let CNLabelContactRelationGranddaughterSonsDaughter: String](/documentation/contacts/cnlabelcontactrelationgranddaughtersonsdaughter)
- [let CNLabelContactRelationGranddaughterOrNiece: String](/documentation/contacts/cnlabelcontactrelationgranddaughterorniece)
- [let CNLabelContactRelationGrandfather: String](/documentation/contacts/cnlabelcontactrelationgrandfather)
- [let CNLabelContactRelationGrandfatherFathersFather: String](/documentation/contacts/cnlabelcontactrelationgrandfatherfathersfather)
- [let CNLabelContactRelationGrandfatherMothersFather: String](/documentation/contacts/cnlabelcontactrelationgrandfathermothersfather)
- [let CNLabelContactRelationGrandmother: String](/documentation/contacts/cnlabelcontactrelationgrandmother)
- [let CNLabelContactRelationGrandmotherFathersMother: String](/documentation/contacts/cnlabelcontactrelationgrandmotherfathersmother)
- [let CNLabelContactRelationGrandmotherMothersMother: String](/documentation/contacts/cnlabelcontactrelationgrandmothermothersmother)
- [let CNLabelContactRelationGrandnephew: String](/documentation/contacts/cnlabelcontactrelationgrandnephew)
- [let CNLabelContactRelationGrandnephewBrothersGrandson: String](/documentation/contacts/cnlabelcontactrelationgrandnephewbrothersgrandson)
- [let CNLabelContactRelationGrandnephewSistersGrandson: String](/documentation/contacts/cnlabelcontactrelationgrandnephewsistersgrandson)
- [let CNLabelContactRelationGrandniece: String](/documentation/contacts/cnlabelcontactrelationgrandniece)
- [let CNLabelContactRelationGrandnieceBrothersGranddaughter: String](/documentation/contacts/cnlabelcontactrelationgrandniecebrothersgranddaughter)
- [let CNLabelContactRelationGrandnieceSistersGranddaughter: String](/documentation/contacts/cnlabelcontactrelationgrandniecesistersgranddaughter)
- [let CNLabelContactRelationGrandparent: String](/documentation/contacts/cnlabelcontactrelationgrandparent)
- [let CNLabelContactRelationGrandson: String](/documentation/contacts/cnlabelcontactrelationgrandson)
- [let CNLabelContactRelationGrandsonDaughtersSon: String](/documentation/contacts/cnlabelcontactrelationgrandsondaughtersson)
- [let CNLabelContactRelationGrandsonSonsSon: String](/documentation/contacts/cnlabelcontactrelationgrandsonsonsson)
- [let CNLabelContactRelationGrandsonOrNephew: String](/documentation/contacts/cnlabelcontactrelationgrandsonornephew)
- [let CNLabelContactRelationGranduncle: String](/documentation/contacts/cnlabelcontactrelationgranduncle)
- [let CNLabelContactRelationGreatGrandchild: String](/documentation/contacts/cnlabelcontactrelationgreatgrandchild)
- [let CNLabelContactRelationGreatGrandchildOrSiblingsGrandchild: String](/documentation/contacts/cnlabelcontactrelationgreatgrandchildorsiblingsgrandchild)
- [let CNLabelContactRelationGreatGranddaughter: String](/documentation/contacts/cnlabelcontactrelationgreatgranddaughter)
- [let CNLabelContactRelationGreatGrandfather: String](/documentation/contacts/cnlabelcontactrelationgreatgrandfather)
- [let CNLabelContactRelationGreatGrandmother: String](/documentation/contacts/cnlabelcontactrelationgreatgrandmother)
- [let CNLabelContactRelationGreatGrandparent: String](/documentation/contacts/cnlabelcontactrelationgreatgrandparent)
- [let CNLabelContactRelationGreatGrandson: String](/documentation/contacts/cnlabelcontactrelationgreatgrandson)
- [let CNLabelContactRelationMaleCousin: String](/documentation/contacts/cnlabelcontactrelationmalecousin)
- [let CNLabelContactRelationNephew: String](/documentation/contacts/cnlabelcontactrelationnephew)
- [let CNLabelContactRelationNephewBrothersSon: String](/documentation/contacts/cnlabelcontactrelationnephewbrothersson)
- [let CNLabelContactRelationNephewBrothersSonOrHusbandsSiblingsSon: String](/documentation/contacts/cnlabelcontactrelationnephewbrotherssonorhusbandssiblingsson)
- [let CNLabelContactRelationNephewOrCousin: String](/documentation/contacts/cnlabelcontactrelationnepheworcousin)
- [let CNLabelContactRelationNephewSistersSon: String](/documentation/contacts/cnlabelcontactrelationnephewsistersson)
- [let CNLabelContactRelationNephewSistersSonOrWifesSiblingsSon: String](/documentation/contacts/cnlabelcontactrelationnephewsisterssonorwifessiblingsson)
- [let CNLabelContactRelationNiece: String](/documentation/contacts/cnlabelcontactrelationniece)
- [let CNLabelContactRelationNieceBrothersDaughter: String](/documentation/contacts/cnlabelcontactrelationniecebrothersdaughter)
- [let CNLabelContactRelationNieceBrothersDaughterOrHusbandsSiblingsDaughter: String](/documentation/contacts/cnlabelcontactrelationniecebrothersdaughterorhusbandssiblingsdaughter)
- [let CNLabelContactRelationNieceOrCousin: String](/documentation/contacts/cnlabelcontactrelationnieceorcousin)
- [let CNLabelContactRelationNieceSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationniecesistersdaughter)
- [let CNLabelContactRelationNieceSistersDaughterOrWifesSiblingsDaughter: String](/documentation/contacts/cnlabelcontactrelationniecesistersdaughterorwifessiblingsdaughter)
- [let CNLabelContactRelationParentsElderSibling: String](/documentation/contacts/cnlabelcontactrelationparentseldersibling)
- [let CNLabelContactRelationParentsSibling: String](/documentation/contacts/cnlabelcontactrelationparentssibling)
- [let CNLabelContactRelationParentsSiblingFathersElderSibling: String](/documentation/contacts/cnlabelcontactrelationparentssiblingfatherseldersibling)
- [let CNLabelContactRelationParentsSiblingFathersSibling: String](/documentation/contacts/cnlabelcontactrelationparentssiblingfatherssibling)
- [let CNLabelContactRelationParentsSiblingFathersYoungerSibling: String](/documentation/contacts/cnlabelcontactrelationparentssiblingfathersyoungersibling)
- [let CNLabelContactRelationParentsSiblingMothersElderSibling: String](/documentation/contacts/cnlabelcontactrelationparentssiblingmotherseldersibling)
- [let CNLabelContactRelationParentsSiblingMothersSibling: String](/documentation/contacts/cnlabelcontactrelationparentssiblingmotherssibling)
- [let CNLabelContactRelationParentsSiblingMothersYoungerSibling: String](/documentation/contacts/cnlabelcontactrelationparentssiblingmothersyoungersibling)
- [let CNLabelContactRelationParentsYoungerSibling: String](/documentation/contacts/cnlabelcontactrelationparentsyoungersibling)
- [let CNLabelContactRelationSiblingsChild: String](/documentation/contacts/cnlabelcontactrelationsiblingschild)
- [let CNLabelContactRelationSonInLaw: String](/documentation/contacts/cnlabelcontactrelationsoninlaw)
- [let CNLabelContactRelationSonInLawOrBrotherInLaw: String](/documentation/contacts/cnlabelcontactrelationsoninlaworbrotherinlaw)
- [let CNLabelContactRelationSonInLawOrStepson: String](/documentation/contacts/cnlabelcontactrelationsoninlaworstepson)
- [let CNLabelContactRelationUncle: String](/documentation/contacts/cnlabelcontactrelationuncle)
- [let CNLabelContactRelationUncleFathersBrother: String](/documentation/contacts/cnlabelcontactrelationunclefathersbrother)
- [let CNLabelContactRelationUncleFathersElderBrother: String](/documentation/contacts/cnlabelcontactrelationunclefatherselderbrother)
- [let CNLabelContactRelationUncleFathersElderSistersHusband: String](/documentation/contacts/cnlabelcontactrelationunclefatherseldersistershusband)
- [let CNLabelContactRelationUncleFathersSistersHusband: String](/documentation/contacts/cnlabelcontactrelationunclefatherssistershusband)
- [let CNLabelContactRelationUncleFathersYoungerBrother: String](/documentation/contacts/cnlabelcontactrelationunclefathersyoungerbrother)
- [let CNLabelContactRelationUncleFathersYoungerSistersHusband: String](/documentation/contacts/cnlabelcontactrelationunclefathersyoungersistershusband)
- [let CNLabelContactRelationUncleMothersBrother: String](/documentation/contacts/cnlabelcontactrelationunclemothersbrother)
- [let CNLabelContactRelationUncleMothersElderBrother: String](/documentation/contacts/cnlabelcontactrelationunclemotherselderbrother)
- [let CNLabelContactRelationUncleMothersSistersHusband: String](/documentation/contacts/cnlabelcontactrelationunclemotherssistershusband)
- [let CNLabelContactRelationUncleMothersYoungerBrother: String](/documentation/contacts/cnlabelcontactrelationunclemothersyoungerbrother)
- [let CNLabelContactRelationUncleParentsBrother: String](/documentation/contacts/cnlabelcontactrelationuncleparentsbrother)
- [let CNLabelContactRelationUncleParentsElderBrother: String](/documentation/contacts/cnlabelcontactrelationuncleparentselderbrother)
- [let CNLabelContactRelationUncleParentsYoungerBrother: String](/documentation/contacts/cnlabelcontactrelationuncleparentsyoungerbrother)
- [let CNLabelContactRelationYoungerCousin: String](/documentation/contacts/cnlabelcontactrelationyoungercousin)
- [let CNLabelContactRelationYoungerCousinFathersBrothersDaughter: String](/documentation/contacts/cnlabelcontactrelationyoungercousinfathersbrothersdaughter)
- [let CNLabelContactRelationYoungerCousinFathersBrothersSon: String](/documentation/contacts/cnlabelcontactrelationyoungercousinfathersbrothersson)
- [let CNLabelContactRelationYoungerCousinFathersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationyoungercousinfatherssistersdaughter)
- [let CNLabelContactRelationYoungerCousinFathersSistersSon: String](/documentation/contacts/cnlabelcontactrelationyoungercousinfatherssistersson)
- [let CNLabelContactRelationYoungerCousinMothersBrothersDaughter: String](/documentation/contacts/cnlabelcontactrelationyoungercousinmothersbrothersdaughter)
- [let CNLabelContactRelationYoungerCousinMothersBrothersSon: String](/documentation/contacts/cnlabelcontactrelationyoungercousinmothersbrothersson)
- [let CNLabelContactRelationYoungerCousinMothersSiblingsDaughterOrFathersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationyoungercousinmotherssiblingsdaughterorfatherssistersdaughter)
- [let CNLabelContactRelationYoungerCousinMothersSiblingsSonOrFathersSistersSon: String](/documentation/contacts/cnlabelcontactrelationyoungercousinmotherssiblingssonorfatherssistersson)
- [let CNLabelContactRelationYoungerCousinMothersSistersDaughter: String](/documentation/contacts/cnlabelcontactrelationyoungercousinmotherssistersdaughter)
- [let CNLabelContactRelationYoungerCousinMothersSistersSon: String](/documentation/contacts/cnlabelcontactrelationyoungercousinmotherssistersson)
- [let CNLabelContactRelationYoungerCousinParentsSiblingsDaughter: String](/documentation/contacts/cnlabelcontactrelationyoungercousinparentssiblingsdaughter)
- [let CNLabelContactRelationYoungerCousinParentsSiblingsSon: String](/documentation/contacts/cnlabelcontactrelationyoungercousinparentssiblingsson)
- [CNContactProperty](/documentation/contacts/cncontactproperty)

#### Getting the Contact Object

- [var contact: CNContact](/documentation/contacts/cncontactproperty/contact)

#### Getting the Property Information

- [var key: String](/documentation/contacts/cncontactproperty/key)
- [var value: Any?](/documentation/contacts/cncontactproperty/value)
- [var label: String?](/documentation/contacts/cncontactproperty/label)
- [var identifier: String?](/documentation/contacts/cncontactproperty/identifier)

#### Handling Exceptions

- [let CNContactPropertyNotFetchedExceptionName: String](/documentation/contacts/cncontactpropertynotfetchedexceptionname)
- [Contact Keys](/documentation/contacts/contact-keys)

### Contact Identification

- [let CNContactIdentifierKey: String](/documentation/contacts/cncontactidentifierkey)
- [let CNContactTypeKey: String](/documentation/contacts/cncontacttypekey)
- [let CNContactPropertyAttribute: String](/documentation/contacts/cncontactpropertyattribute)

### Name

- [let CNContactNamePrefixKey: String](/documentation/contacts/cncontactnameprefixkey)
- [let CNContactGivenNameKey: String](/documentation/contacts/cncontactgivennamekey)
- [let CNContactMiddleNameKey: String](/documentation/contacts/cncontactmiddlenamekey)
- [let CNContactFamilyNameKey: String](/documentation/contacts/cncontactfamilynamekey)
- [let CNContactPreviousFamilyNameKey: String](/documentation/contacts/cncontactpreviousfamilynamekey)
- [let CNContactNameSuffixKey: String](/documentation/contacts/cncontactnamesuffixkey)
- [let CNContactNicknameKey: String](/documentation/contacts/cncontactnicknamekey)
- [let CNContactPhoneticGivenNameKey: String](/documentation/contacts/cncontactphoneticgivennamekey)
- [let CNContactPhoneticMiddleNameKey: String](/documentation/contacts/cncontactphoneticmiddlenamekey)
- [let CNContactPhoneticFamilyNameKey: String](/documentation/contacts/cncontactphoneticfamilynamekey)

### Work

- [let CNContactJobTitleKey: String](/documentation/contacts/cncontactjobtitlekey)
- [let CNContactDepartmentNameKey: String](/documentation/contacts/cncontactdepartmentnamekey)
- [let CNContactOrganizationNameKey: String](/documentation/contacts/cncontactorganizationnamekey)
- [let CNContactPhoneticOrganizationNameKey: String](/documentation/contacts/cncontactphoneticorganizationnamekey)

### Addresses

- [let CNContactPostalAddressesKey: String](/documentation/contacts/cncontactpostaladdresseskey)
- [let CNContactEmailAddressesKey: String](/documentation/contacts/cncontactemailaddresseskey)
- [let CNContactUrlAddressesKey: String](/documentation/contacts/cncontacturladdresseskey)
- [let CNContactInstantMessageAddressesKey: String](/documentation/contacts/cncontactinstantmessageaddresseskey)

### Phone

- [let CNContactPhoneNumbersKey: String](/documentation/contacts/cncontactphonenumberskey)

### Social Profiles

- [let CNContactSocialProfilesKey: String](/documentation/contacts/cncontactsocialprofileskey)

### Birthday

- [let CNContactBirthdayKey: String](/documentation/contacts/cncontactbirthdaykey)
- [let CNContactNonGregorianBirthdayKey: String](/documentation/contacts/cncontactnongregorianbirthdaykey)
- [let CNContactDatesKey: String](/documentation/contacts/cncontactdateskey)

### Notes

- [let CNContactNoteKey: String](/documentation/contacts/cncontactnotekey)
- [com.apple.developer.contacts.notes](/documentation/bundleresources/entitlements/com.apple.developer.contacts.notes)

### Images

- [let CNContactImageDataKey: String](/documentation/contacts/cncontactimagedatakey)
- [let CNContactThumbnailImageDataKey: String](/documentation/contacts/cncontactthumbnailimagedatakey)
- [let CNContactImageDataAvailableKey: String](/documentation/contacts/cncontactimagedataavailablekey)

### Relationships

- [let CNContactRelationsKey: String](/documentation/contacts/cncontactrelationskey)

### Groups and Containers

- [let CNGroupNameKey: String](/documentation/contacts/cngroupnamekey)
- [let CNGroupIdentifierKey: String](/documentation/contacts/cngroupidentifierkey)
- [let CNContainerNameKey: String](/documentation/contacts/cncontainernamekey)
- [let CNContainerTypeKey: String](/documentation/contacts/cncontainertypekey)

### Instant Messaging Keys

- [let CNInstantMessageAddressServiceKey: String](/documentation/contacts/cninstantmessageaddressservicekey)
- [let CNInstantMessageAddressUsernameKey: String](/documentation/contacts/cninstantmessageaddressusernamekey)

### Social Profile Keys

- [let CNSocialProfileServiceKey: String](/documentation/contacts/cnsocialprofileservicekey)
- [let CNSocialProfileURLStringKey: String](/documentation/contacts/cnsocialprofileurlstringkey)
- [let CNSocialProfileUsernameKey: String](/documentation/contacts/cnsocialprofileusernamekey)
- [let CNSocialProfileUserIdentifierKey: String](/documentation/contacts/cnsocialprofileuseridentifierkey)

### Key Descriptors

- [CNKeyDescriptor](/documentation/contacts/cnkeydescriptor)

## Fetch and save requests

- [CNContactFetchRequest](/documentation/contacts/cncontactfetchrequest)

### Creating a Fetch Request

- [init(keysToFetch: [any CNKeyDescriptor])](/documentation/contacts/cncontactfetchrequest/init(keystofetch:))
- [CNKeyDescriptor](/documentation/contacts/cnkeydescriptor)

### Specifying the Search Predicate

- [var predicate: NSPredicate?](/documentation/contacts/cncontactfetchrequest/predicate)

### Configuring the Fetch Options

- [var mutableObjects: Bool](/documentation/contacts/cncontactfetchrequest/mutableobjects)
- [var unifyResults: Bool](/documentation/contacts/cncontactfetchrequest/unifyresults)
- [var sortOrder: CNContactSortOrder](/documentation/contacts/cncontactfetchrequest/sortorder)
- [CNContactSortOrder](/documentation/contacts/cncontactsortorder)

#### Sort Orders

- [case none](/documentation/contacts/cncontactsortorder/none)
- [case userDefault](/documentation/contacts/cncontactsortorder/userdefault)
- [case givenName](/documentation/contacts/cncontactsortorder/givenname)
- [case familyName](/documentation/contacts/cncontactsortorder/familyname)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cncontactsortorder/init(rawvalue:))

### Specifying the Keys to Fetch

- [var keysToFetch: [any CNKeyDescriptor]](/documentation/contacts/cncontactfetchrequest/keystofetch)
- [CNFetchRequest](/documentation/contacts/cnfetchrequest)
- [CNFetchResult](/documentation/contacts/cnfetchresult)

### Accessing results

- [var currentHistoryToken: Data](/documentation/contacts/cnfetchresult/currenthistorytoken)
- [var value: ValueType](/documentation/contacts/cnfetchresult/value)
- [CNSaveRequest](/documentation/contacts/cnsaverequest)

### Saving contact changes

- [func add(CNMutableContact, toContainerWithIdentifier: String?)](/documentation/contacts/cnsaverequest/add(_:tocontainerwithidentifier:)-7eut4)
- [func update(CNMutableContact)](/documentation/contacts/cnsaverequest/update(_:)-3gaig)
- [func delete(CNMutableContact)](/documentation/contacts/cnsaverequest/delete(_:)-8m1tc)

### Saving group changes

- [func add(CNMutableGroup, toContainerWithIdentifier: String?)](/documentation/contacts/cnsaverequest/add(_:tocontainerwithidentifier:)-4ikaa)
- [func update(CNMutableGroup)](/documentation/contacts/cnsaverequest/update(_:)-8h6f6)
- [func delete(CNMutableGroup)](/documentation/contacts/cnsaverequest/delete(_:)-29lsm)
- [func addMember(CNContact, to: CNGroup)](/documentation/contacts/cnsaverequest/addmember(_:to:))
- [func removeMember(CNContact, from: CNGroup)](/documentation/contacts/cnsaverequest/removemember(_:from:))

### Adding and removing subgroups

- [func addSubgroup(CNGroup, to: CNGroup)](/documentation/contacts/cnsaverequest/addsubgroup(_:to:))
- [func removeSubgroup(CNGroup, from: CNGroup)](/documentation/contacts/cnsaverequest/removesubgroup(_:from:))

### Configuring the save request

- [var shouldRefetchContacts: Bool](/documentation/contacts/cnsaverequest/shouldrefetchcontacts)
- [var transactionAuthor: String?](/documentation/contacts/cnsaverequest/transactionauthor)

## Change history data

- [CNChangeHistoryAddContactEvent](/documentation/contacts/cnchangehistoryaddcontactevent)

### Getting event details

- [var contact: CNContact](/documentation/contacts/cnchangehistoryaddcontactevent/contact)
- [var containerIdentifier: String?](/documentation/contacts/cnchangehistoryaddcontactevent/containeridentifier)
- [CNChangeHistoryAddGroupEvent](/documentation/contacts/cnchangehistoryaddgroupevent)

### Getting event details

- [var group: CNGroup](/documentation/contacts/cnchangehistoryaddgroupevent/group)
- [var containerIdentifier: String](/documentation/contacts/cnchangehistoryaddgroupevent/containeridentifier)
- [CNChangeHistoryAddMemberToGroupEvent](/documentation/contacts/cnchangehistoryaddmembertogroupevent)

### Getting event details

- [var group: CNGroup](/documentation/contacts/cnchangehistoryaddmembertogroupevent/group)
- [var member: CNContact](/documentation/contacts/cnchangehistoryaddmembertogroupevent/member)
- [CNChangeHistoryAddSubgroupToGroupEvent](/documentation/contacts/cnchangehistoryaddsubgrouptogroupevent)

### Getting event details

- [var group: CNGroup](/documentation/contacts/cnchangehistoryaddsubgrouptogroupevent/group)
- [var subgroup: CNGroup](/documentation/contacts/cnchangehistoryaddsubgrouptogroupevent/subgroup)
- [CNChangeHistoryDeleteContactEvent](/documentation/contacts/cnchangehistorydeletecontactevent)

### Getting event details

- [var contactIdentifier: String](/documentation/contacts/cnchangehistorydeletecontactevent/contactidentifier)
- [CNChangeHistoryDeleteGroupEvent](/documentation/contacts/cnchangehistorydeletegroupevent)

### Getting event details

- [var groupIdentifier: String](/documentation/contacts/cnchangehistorydeletegroupevent/groupidentifier)
- [CNChangeHistoryDropEverythingEvent](/documentation/contacts/cnchangehistorydropeverythingevent)
- [CNChangeHistoryEvent](/documentation/contacts/cnchangehistoryevent)

### Processing an event

- [func accept(any CNChangeHistoryEventVisitor)](/documentation/contacts/cnchangehistoryevent/accept(_:))
- [CNChangeHistoryFetchRequest](/documentation/contacts/cnchangehistoryfetchrequest)

### Configuring the fetch request

- [var additionalContactKeyDescriptors: [any CNKeyDescriptor]?](/documentation/contacts/cnchangehistoryfetchrequest/additionalcontactkeydescriptors)
- [var excludedTransactionAuthors: [String]?](/documentation/contacts/cnchangehistoryfetchrequest/excludedtransactionauthors)
- [var includeGroupChanges: Bool](/documentation/contacts/cnchangehistoryfetchrequest/includegroupchanges)
- [var mutableObjects: Bool](/documentation/contacts/cnchangehistoryfetchrequest/mutableobjects)
- [var shouldUnifyResults: Bool](/documentation/contacts/cnchangehistoryfetchrequest/shouldunifyresults)
- [var startingToken: Data?](/documentation/contacts/cnchangehistoryfetchrequest/startingtoken)
- [CNChangeHistoryRemoveMemberFromGroupEvent](/documentation/contacts/cnchangehistoryremovememberfromgroupevent)

### Getting event details

- [var group: CNGroup](/documentation/contacts/cnchangehistoryremovememberfromgroupevent/group)
- [var member: CNContact](/documentation/contacts/cnchangehistoryremovememberfromgroupevent/member)
- [CNChangeHistoryRemoveSubgroupFromGroupEvent](/documentation/contacts/cnchangehistoryremovesubgroupfromgroupevent)

### Getting event details

- [var group: CNGroup](/documentation/contacts/cnchangehistoryremovesubgroupfromgroupevent/group)
- [var subgroup: CNGroup](/documentation/contacts/cnchangehistoryremovesubgroupfromgroupevent/subgroup)
- [CNChangeHistoryUpdateContactEvent](/documentation/contacts/cnchangehistoryupdatecontactevent)

### Getting event details

- [var contact: CNContact](/documentation/contacts/cnchangehistoryupdatecontactevent/contact)
- [CNChangeHistoryUpdateGroupEvent](/documentation/contacts/cnchangehistoryupdategroupevent)

### Getting event details

- [var group: CNGroup](/documentation/contacts/cnchangehistoryupdategroupevent/group)
- [CNChangeHistoryEventVisitor](/documentation/contacts/cnchangehistoryeventvisitor)

### Updating contacts

- [func visit(CNChangeHistoryAddContactEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visit(_:)-9w73y)
- [func visit(CNChangeHistoryUpdateContactEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visit(_:)-1pf2a)
- [func visit(CNChangeHistoryDeleteContactEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visit(_:)-ci4z)

### Updating groups

- [func visit(CNChangeHistoryAddGroupEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visit(_:)-ve62)
- [func visit(CNChangeHistoryUpdateGroupEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visit(_:)-23p9h)
- [func visit(CNChangeHistoryDeleteGroupEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visit(_:)-82duo)

### Updating subgroups

- [func visitAddSubgroup(CNChangeHistoryAddSubgroupToGroupEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visitaddsubgroup(_:))
- [func visitRemoveSubgroup(CNChangeHistoryRemoveSubgroupFromGroupEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visitremovesubgroup(_:))

### Updating contacts in groups

- [func visitAddMember(CNChangeHistoryAddMemberToGroupEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visitaddmember(_:))
- [func visitRemoveMember(CNChangeHistoryRemoveMemberFromGroupEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visitremovemember(_:))

### Resetting synced data

- [func visit(CNChangeHistoryDropEverythingEvent)](/documentation/contacts/cnchangehistoryeventvisitor/visit(_:)-2yhz3)

## Formatters

- [CNContactFormatter](/documentation/contacts/cncontactformatter)

### Creating a formatted attributed string

- [func attributedString(from: CNContact, defaultAttributes: [AnyHashable : Any]?) -> NSAttributedString?](/documentation/contacts/cncontactformatter/attributedstring(from:defaultattributes:))
- [class func attributedString(from: CNContact, style: CNContactFormatterStyle, defaultAttributes: [AnyHashable : Any]?) -> NSAttributedString?](/documentation/contacts/cncontactformatter/attributedstring(from:style:defaultattributes:))

### Creating a formatted string

- [func string(from: CNContact) -> String?](/documentation/contacts/cncontactformatter/string(from:))
- [class func string(from: CNContact, style: CNContactFormatterStyle) -> String?](/documentation/contacts/cncontactformatter/string(from:style:))

### Specifying the formatting style

- [var style: CNContactFormatterStyle](/documentation/contacts/cncontactformatter/style)
- [CNContactFormatterStyle](/documentation/contacts/cncontactformatterstyle)

#### Constants

- [case fullName](/documentation/contacts/cncontactformatterstyle/fullname)
- [case phoneticFullName](/documentation/contacts/cncontactformatterstyle/phoneticfullname)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cncontactformatterstyle/init(rawvalue:))

### Getting a descriptor

- [class func descriptorForRequiredKeys(for: CNContactFormatterStyle) -> any CNKeyDescriptor](/documentation/contacts/cncontactformatter/descriptorforrequiredkeys(for:))
- [class var descriptorForRequiredKeysForDelimiter: any CNKeyDescriptor](/documentation/contacts/cncontactformatter/descriptorforrequiredkeysfordelimiter)
- [class var descriptorForRequiredKeysForNameOrder: any CNKeyDescriptor](/documentation/contacts/cncontactformatter/descriptorforrequiredkeysfornameorder)

### Getting format information

- [class func delimiter(for: CNContact) -> String](/documentation/contacts/cncontactformatter/delimiter(for:))
- [class func nameOrder(for: CNContact) -> CNContactDisplayNameOrder](/documentation/contacts/cncontactformatter/nameorder(for:))
- [CNContactDisplayNameOrder](/documentation/contacts/cncontactdisplaynameorder)

#### Constants

- [case userDefault](/documentation/contacts/cncontactdisplaynameorder/userdefault)
- [case givenNameFirst](/documentation/contacts/cncontactdisplaynameorder/givennamefirst)
- [case familyNameFirst](/documentation/contacts/cncontactdisplaynameorder/familynamefirst)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cncontactdisplaynameorder/init(rawvalue:))
- [CNPostalAddressFormatter](/documentation/contacts/cnpostaladdressformatter)

### Generating a formatted attributed string

- [func attributedString(from: CNPostalAddress, withDefaultAttributes: [AnyHashable : Any]) -> NSAttributedString](/documentation/contacts/cnpostaladdressformatter/attributedstring(from:withdefaultattributes:))
- [class func attributedString(from: CNPostalAddress, style: CNPostalAddressFormatterStyle, withDefaultAttributes: [AnyHashable : Any]) -> NSAttributedString](/documentation/contacts/cnpostaladdressformatter/attributedstring(from:style:withdefaultattributes:))
- [let CNPostalAddressPropertyAttribute: String](/documentation/contacts/cnpostaladdresspropertyattribute)
- [let CNPostalAddressLocalizedPropertyNameAttribute: String](/documentation/contacts/cnpostaladdresslocalizedpropertynameattribute)

### Generating a formatted string

- [func string(from: CNPostalAddress) -> String](/documentation/contacts/cnpostaladdressformatter/string(from:))
- [class func string(from: CNPostalAddress, style: CNPostalAddressFormatterStyle) -> String](/documentation/contacts/cnpostaladdressformatter/string(from:style:))

### Specifying the formatting style

- [var style: CNPostalAddressFormatterStyle](/documentation/contacts/cnpostaladdressformatter/style)
- [CNPostalAddressFormatterStyle](/documentation/contacts/cnpostaladdressformatterstyle)

#### Styles

- [case mailingAddress](/documentation/contacts/cnpostaladdressformatterstyle/mailingaddress)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cnpostaladdressformatterstyle/init(rawvalue:))

### Getting the postal attribute keys

- [let CNPostalAddressCityKey: String](/documentation/contacts/cnpostaladdresscitykey)
- [let CNPostalAddressCountryKey: String](/documentation/contacts/cnpostaladdresscountrykey)
- [let CNPostalAddressISOCountryCodeKey: String](/documentation/contacts/cnpostaladdressisocountrycodekey)
- [let CNPostalAddressPostalCodeKey: String](/documentation/contacts/cnpostaladdresspostalcodekey)
- [let CNPostalAddressStateKey: String](/documentation/contacts/cnpostaladdressstatekey)
- [let CNPostalAddressStreetKey: String](/documentation/contacts/cnpostaladdressstreetkey)
- [let CNPostalAddressSubAdministrativeAreaKey: String](/documentation/contacts/cnpostaladdresssubadministrativeareakey)
- [let CNPostalAddressSubLocalityKey: String](/documentation/contacts/cnpostaladdresssublocalitykey)
- [CNContactVCardSerialization](/documentation/contacts/cncontactvcardserialization)

### Extracting Contacts from a vCard

- [class func contacts(with: Data) throws -> [CNContact]](/documentation/contacts/cncontactvcardserialization/contacts(with:))

### Getting a vCard for Contacts

- [class func data(with: [CNContact]) throws -> Data](/documentation/contacts/cncontactvcardserialization/data(with:))

### Getting a Descriptor

- [class func descriptorForRequiredKeys() -> any CNKeyDescriptor](/documentation/contacts/cncontactvcardserialization/descriptorforrequiredkeys())
- [CNContactsUserDefaults](/documentation/contacts/cncontactsuserdefaults)

### Getting the Shared Database

- [class func shared() -> Self](/documentation/contacts/cncontactsuserdefaults/shared())

### Getting the Default Values

- [var countryCode: String](/documentation/contacts/cncontactsuserdefaults/countrycode)
- [var sortOrder: CNContactSortOrder](/documentation/contacts/cncontactsuserdefaults/sortorder)

## Errors

- [Error Information](/documentation/contacts/error-information)

### Error domain

- [let CNErrorDomain: String](/documentation/contacts/cnerrordomain)

### Error codes

- [CNError](/documentation/contacts/cnerror)

#### Error codes

- [static var authorizationDenied: CNError.Code](/documentation/contacts/cnerror/authorizationdenied)
- [static var changeHistoryExpired: CNError.Code](/documentation/contacts/cnerror/changehistoryexpired)
- [static var changeHistoryInvalidAnchor: CNError.Code](/documentation/contacts/cnerror/changehistoryinvalidanchor)
- [static var changeHistoryInvalidFetchRequest: CNError.Code](/documentation/contacts/cnerror/changehistoryinvalidfetchrequest)
- [static var clientIdentifierCollision: CNError.Code](/documentation/contacts/cnerror/clientidentifiercollision)
- [static var clientIdentifierDoesNotExist: CNError.Code](/documentation/contacts/cnerror/clientidentifierdoesnotexist)
- [static var clientIdentifierInvalid: CNError.Code](/documentation/contacts/cnerror/clientidentifierinvalid)
- [static var communicationError: CNError.Code](/documentation/contacts/cnerror/communicationerror)
- [static var containmentCycle: CNError.Code](/documentation/contacts/cnerror/containmentcycle)
- [static var containmentScope: CNError.Code](/documentation/contacts/cnerror/containmentscope)
- [static var dataAccessError: CNError.Code](/documentation/contacts/cnerror/dataaccesserror)
- [static var featureDisabledByUser: CNError.Code](/documentation/contacts/cnerror/featuredisabledbyuser)
- [static var featureNotAvailable: CNError.Code](/documentation/contacts/cnerror/featurenotavailable)
- [static var insertedRecordAlreadyExists: CNError.Code](/documentation/contacts/cnerror/insertedrecordalreadyexists)
- [static var noAccessableWritableContainers: CNError.Code](/documentation/contacts/cnerror/noaccessablewritablecontainers)
- [static var parentContainerNotWritable: CNError.Code](/documentation/contacts/cnerror/parentcontainernotwritable)
- [static var parentRecordDoesNotExist: CNError.Code](/documentation/contacts/cnerror/parentrecorddoesnotexist)
- [static var policyViolation: CNError.Code](/documentation/contacts/cnerror/policyviolation)
- [static var predicateInvalid: CNError.Code](/documentation/contacts/cnerror/predicateinvalid)
- [static var recordDoesNotExist: CNError.Code](/documentation/contacts/cnerror/recorddoesnotexist)
- [static var recordIdentifierInvalid: CNError.Code](/documentation/contacts/cnerror/recordidentifierinvalid)
- [static var recordNotWritable: CNError.Code](/documentation/contacts/cnerror/recordnotwritable)
- [static var unauthorizedKeys: CNError.Code](/documentation/contacts/cnerror/unauthorizedkeys)
- [static var vCardMalformed: CNError.Code](/documentation/contacts/cnerror/vcardmalformed)
- [static var vCardSummarizationError: CNError.Code](/documentation/contacts/cnerror/vcardsummarizationerror)
- [static var validationConfigurationError: CNError.Code](/documentation/contacts/cnerror/validationconfigurationerror)
- [static var validationMultipleErrors: CNError.Code](/documentation/contacts/cnerror/validationmultipleerrors)
- [static var validationTypeMismatch: CNError.Code](/documentation/contacts/cnerror/validationtypemismatch)

#### Error details

- [var affectedRecordIdentifiers: [String]?](/documentation/contacts/cnerror/affectedrecordidentifiers)
- [var affectedRecords: [AnyObject]?](/documentation/contacts/cnerror/affectedrecords)
- [CNError.Code](/documentation/contacts/cnerror/code)

##### Errors

- [case authorizationDenied](/documentation/contacts/cnerror/code/authorizationdenied)
- [case changeHistoryExpired](/documentation/contacts/cnerror/code/changehistoryexpired)
- [case changeHistoryInvalidAnchor](/documentation/contacts/cnerror/code/changehistoryinvalidanchor)
- [case changeHistoryInvalidFetchRequest](/documentation/contacts/cnerror/code/changehistoryinvalidfetchrequest)
- [case clientIdentifierCollision](/documentation/contacts/cnerror/code/clientidentifiercollision)
- [case clientIdentifierInvalid](/documentation/contacts/cnerror/code/clientidentifierinvalid)
- [case clientIdentifierDoesNotExist](/documentation/contacts/cnerror/code/clientidentifierdoesnotexist)
- [case communicationError](/documentation/contacts/cnerror/code/communicationerror)
- [case containmentCycle](/documentation/contacts/cnerror/code/containmentcycle)
- [case containmentScope](/documentation/contacts/cnerror/code/containmentscope)
- [case dataAccessError](/documentation/contacts/cnerror/code/dataaccesserror)
- [case featureDisabledByUser](/documentation/contacts/cnerror/code/featuredisabledbyuser)
- [case featureNotAvailable](/documentation/contacts/cnerror/code/featurenotavailable)
- [case insertedRecordAlreadyExists](/documentation/contacts/cnerror/code/insertedrecordalreadyexists)
- [case noAccessableWritableContainers](/documentation/contacts/cnerror/code/noaccessablewritablecontainers)
- [case parentContainerNotWritable](/documentation/contacts/cnerror/code/parentcontainernotwritable)
- [case parentRecordDoesNotExist](/documentation/contacts/cnerror/code/parentrecorddoesnotexist)
- [case policyViolation](/documentation/contacts/cnerror/code/policyviolation)
- [case predicateInvalid](/documentation/contacts/cnerror/code/predicateinvalid)
- [case recordDoesNotExist](/documentation/contacts/cnerror/code/recorddoesnotexist)
- [case recordIdentifierInvalid](/documentation/contacts/cnerror/code/recordidentifierinvalid)
- [case recordNotWritable](/documentation/contacts/cnerror/code/recordnotwritable)
- [case unauthorizedKeys](/documentation/contacts/cnerror/code/unauthorizedkeys)
- [case validationMultipleErrors](/documentation/contacts/cnerror/code/validationmultipleerrors)
- [case validationTypeMismatch](/documentation/contacts/cnerror/code/validationtypemismatch)
- [case validationConfigurationError](/documentation/contacts/cnerror/code/validationconfigurationerror)
- [case vCardMalformed](/documentation/contacts/cnerror/code/vcardmalformed)
- [case vCardSummarizationError](/documentation/contacts/cnerror/code/vcardsummarizationerror)

##### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cnerror/code/init(rawvalue:))
- [var keyPaths: [String]?](/documentation/contacts/cnerror/keypaths)

#### Type Properties

- [static var errorDomain: String](/documentation/contacts/cnerror/errordomain)
- [CNError.Code](/documentation/contacts/cnerror/code)

#### Errors

- [case authorizationDenied](/documentation/contacts/cnerror/code/authorizationdenied)
- [case changeHistoryExpired](/documentation/contacts/cnerror/code/changehistoryexpired)
- [case changeHistoryInvalidAnchor](/documentation/contacts/cnerror/code/changehistoryinvalidanchor)
- [case changeHistoryInvalidFetchRequest](/documentation/contacts/cnerror/code/changehistoryinvalidfetchrequest)
- [case clientIdentifierCollision](/documentation/contacts/cnerror/code/clientidentifiercollision)
- [case clientIdentifierInvalid](/documentation/contacts/cnerror/code/clientidentifierinvalid)
- [case clientIdentifierDoesNotExist](/documentation/contacts/cnerror/code/clientidentifierdoesnotexist)
- [case communicationError](/documentation/contacts/cnerror/code/communicationerror)
- [case containmentCycle](/documentation/contacts/cnerror/code/containmentcycle)
- [case containmentScope](/documentation/contacts/cnerror/code/containmentscope)
- [case dataAccessError](/documentation/contacts/cnerror/code/dataaccesserror)
- [case featureDisabledByUser](/documentation/contacts/cnerror/code/featuredisabledbyuser)
- [case featureNotAvailable](/documentation/contacts/cnerror/code/featurenotavailable)
- [case insertedRecordAlreadyExists](/documentation/contacts/cnerror/code/insertedrecordalreadyexists)
- [case noAccessableWritableContainers](/documentation/contacts/cnerror/code/noaccessablewritablecontainers)
- [case parentContainerNotWritable](/documentation/contacts/cnerror/code/parentcontainernotwritable)
- [case parentRecordDoesNotExist](/documentation/contacts/cnerror/code/parentrecorddoesnotexist)
- [case policyViolation](/documentation/contacts/cnerror/code/policyviolation)
- [case predicateInvalid](/documentation/contacts/cnerror/code/predicateinvalid)
- [case recordDoesNotExist](/documentation/contacts/cnerror/code/recorddoesnotexist)
- [case recordIdentifierInvalid](/documentation/contacts/cnerror/code/recordidentifierinvalid)
- [case recordNotWritable](/documentation/contacts/cnerror/code/recordnotwritable)
- [case unauthorizedKeys](/documentation/contacts/cnerror/code/unauthorizedkeys)
- [case validationMultipleErrors](/documentation/contacts/cnerror/code/validationmultipleerrors)
- [case validationTypeMismatch](/documentation/contacts/cnerror/code/validationtypemismatch)
- [case validationConfigurationError](/documentation/contacts/cnerror/code/validationconfigurationerror)
- [case vCardMalformed](/documentation/contacts/cnerror/code/vcardmalformed)
- [case vCardSummarizationError](/documentation/contacts/cnerror/code/vcardsummarizationerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/contacts/cnerror/code/init(rawvalue:))

### Error data keys

- [let CNErrorUserInfoAffectedRecordsKey: String](/documentation/contacts/cnerroruserinfoaffectedrecordskey)
- [let CNErrorUserInfoAffectedRecordIdentifiersKey: String](/documentation/contacts/cnerroruserinfoaffectedrecordidentifierskey)
- [let CNErrorUserInfoValidationErrorsKey: String](/documentation/contacts/cnerroruserinfovalidationerrorskey)
- [let CNErrorUserInfoKeyPathsKey: String](/documentation/contacts/cnerroruserinfokeypathskey)

### Exceptions

- [let CNContactPropertyNotFetchedExceptionName: String](/documentation/contacts/cncontactpropertynotfetchedexceptionname)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
