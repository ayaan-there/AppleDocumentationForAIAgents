# Address Book UI Documentation

Source: https://sosumi.ai/documentation/addressbookui

---
title: Address Book UI
source: https://developer.apple.com/documentation/addressbookui
timestamp: 2026-02-13T19:06:42.301Z
---

## People Picker

- [ABPeoplePickerNavigationController](/documentation/addressbookui/abpeoplepickernavigationcontroller)

### Responding to View Controller Interactions

- [var peoplePickerDelegate: (any ABPeoplePickerNavigationControllerDelegate)?](/documentation/addressbookui/abpeoplepickernavigationcontroller/peoplepickerdelegate)
- [ABPeoplePickerNavigationControllerDelegate](/documentation/addressbookui/abpeoplepickernavigationcontrollerdelegate)

#### Responding to User Events

- [func peoplePickerNavigationController(ABPeoplePickerNavigationController, shouldContinueAfterSelectingPerson: ABRecord) -> Bool](/documentation/addressbookui/abpeoplepickernavigationcontrollerdelegate/peoplepickernavigationcontroller(_:shouldcontinueafterselectingperson:))
- [func peoplePickerNavigationController(ABPeoplePickerNavigationController, shouldContinueAfterSelectingPerson: ABRecord, property: ABPropertyID, identifier: ABMultiValueIdentifier) -> Bool](/documentation/addressbookui/abpeoplepickernavigationcontrollerdelegate/peoplepickernavigationcontroller(_:shouldcontinueafterselectingperson:property:identifier:))
- [func peoplePickerNavigationControllerDidCancel(ABPeoplePickerNavigationController)](/documentation/addressbookui/abpeoplepickernavigationcontrollerdelegate/peoplepickernavigationcontrollerdidcancel(_:))
- [func peoplePickerNavigationController(ABPeoplePickerNavigationController, didSelectPerson: ABRecord)](/documentation/addressbookui/abpeoplepickernavigationcontrollerdelegate/peoplepickernavigationcontroller(_:didselectperson:))
- [func peoplePickerNavigationController(ABPeoplePickerNavigationController, didSelectPerson: ABRecord, property: ABPropertyID, identifier: ABMultiValueIdentifier)](/documentation/addressbookui/abpeoplepickernavigationcontrollerdelegate/peoplepickernavigationcontroller(_:didselectperson:property:identifier:))

### Displaying Person Properties

- [var displayedProperties: [NSNumber]?](/documentation/addressbookui/abpeoplepickernavigationcontroller/displayedproperties)

### Configuring People Pickers

- [var addressBook: ABAddressBook?](/documentation/addressbookui/abpeoplepickernavigationcontroller/addressbook)

### Customizing Display and Selection

- [var predicateForEnablingPerson: NSPredicate?](/documentation/addressbookui/abpeoplepickernavigationcontroller/predicateforenablingperson)
- [var predicateForSelectionOfPerson: NSPredicate?](/documentation/addressbookui/abpeoplepickernavigationcontroller/predicateforselectionofperson)
- [var predicateForSelectionOfProperty: NSPredicate?](/documentation/addressbookui/abpeoplepickernavigationcontroller/predicateforselectionofproperty)

### Constants

- [Address Book Properties](/documentation/addressbookui/address-book-properties)

#### Constants

- [let ABPersonNamePrefixProperty: String](/documentation/addressbookui/abpersonnameprefixproperty)
- [let ABPersonGivenNameProperty: String](/documentation/addressbookui/abpersongivennameproperty)
- [let ABPersonMiddleNameProperty: String](/documentation/addressbookui/abpersonmiddlenameproperty)
- [let ABPersonFamilyNameProperty: String](/documentation/addressbookui/abpersonfamilynameproperty)
- [let ABPersonNameSuffixProperty: String](/documentation/addressbookui/abpersonnamesuffixproperty)
- [let ABPersonPreviousFamilyNameProperty: String](/documentation/addressbookui/abpersonpreviousfamilynameproperty)
- [let ABPersonNicknameProperty: String](/documentation/addressbookui/abpersonnicknameproperty)
- [let ABPersonPhoneticGivenNameProperty: String](/documentation/addressbookui/abpersonphoneticgivennameproperty)
- [let ABPersonPhoneticMiddleNameProperty: String](/documentation/addressbookui/abpersonphoneticmiddlenameproperty)
- [let ABPersonPhoneticFamilyNameProperty: String](/documentation/addressbookui/abpersonphoneticfamilynameproperty)
- [let ABPersonOrganizationNameProperty: String](/documentation/addressbookui/abpersonorganizationnameproperty)
- [let ABPersonDepartmentNameProperty: String](/documentation/addressbookui/abpersondepartmentnameproperty)
- [let ABPersonJobTitleProperty: String](/documentation/addressbookui/abpersonjobtitleproperty)
- [let ABPersonBirthdayProperty: String](/documentation/addressbookui/abpersonbirthdayproperty)
- [let ABPersonNoteProperty: String](/documentation/addressbookui/abpersonnoteproperty)
- [let ABPersonPhoneNumbersProperty: String](/documentation/addressbookui/abpersonphonenumbersproperty)
- [let ABPersonEmailAddressesProperty: String](/documentation/addressbookui/abpersonemailaddressesproperty)
- [let ABPersonUrlAddressesProperty: String](/documentation/addressbookui/abpersonurladdressesproperty)
- [let ABPersonDatesProperty: String](/documentation/addressbookui/abpersondatesproperty)
- [let ABPersonInstantMessageAddressesProperty: String](/documentation/addressbookui/abpersoninstantmessageaddressesproperty)
- [let ABPersonRelatedNamesProperty: String](/documentation/addressbookui/abpersonrelatednamesproperty)
- [let ABPersonSocialProfilesProperty: String](/documentation/addressbookui/abpersonsocialprofilesproperty)
- [let ABPersonPostalAddressesProperty: String](/documentation/addressbookui/abpersonpostaladdressesproperty)

## Detail Display

- [ABNewPersonViewController](/documentation/addressbookui/abnewpersonviewcontroller)

### Responding to View Controller Interactions

- [var newPersonViewDelegate: (any ABNewPersonViewControllerDelegate)?](/documentation/addressbookui/abnewpersonviewcontroller/newpersonviewdelegate)
- [ABNewPersonViewControllerDelegate](/documentation/addressbookui/abnewpersonviewcontrollerdelegate)

#### Responding to User Events

- [func newPersonViewController(ABNewPersonViewController, didCompleteWithNewPerson: ABRecord?)](/documentation/addressbookui/abnewpersonviewcontrollerdelegate/newpersonviewcontroller(_:didcompletewithnewperson:))

### Displaying Person Properties

- [var displayedPerson: ABRecord?](/documentation/addressbookui/abnewpersonviewcontroller/displayedperson)

### Configuring New Person Views

- [var addressBook: ABAddressBook?](/documentation/addressbookui/abnewpersonviewcontroller/addressbook)
- [var parentGroup: ABRecord?](/documentation/addressbookui/abnewpersonviewcontroller/parentgroup)
- [ABPersonViewController](/documentation/addressbookui/abpersonviewcontroller)

### Responding to View Controller Interactions

- [var personViewDelegate: (any ABPersonViewControllerDelegate)?](/documentation/addressbookui/abpersonviewcontroller/personviewdelegate)
- [ABPersonViewControllerDelegate](/documentation/addressbookui/abpersonviewcontrollerdelegate)

#### Responding to User Events

- [func personViewController(ABPersonViewController, shouldPerformDefaultActionForPerson: ABRecord, property: ABPropertyID, identifier: ABMultiValueIdentifier) -> Bool](/documentation/addressbookui/abpersonviewcontrollerdelegate/personviewcontroller(_:shouldperformdefaultactionforperson:property:identifier:))

### Displaying Person Properties

- [var displayedPerson: ABRecord](/documentation/addressbookui/abpersonviewcontroller/displayedperson)
- [var displayedProperties: [NSNumber]?](/documentation/addressbookui/abpersonviewcontroller/displayedproperties)
- [var shouldShowLinkedPeople: Bool](/documentation/addressbookui/abpersonviewcontroller/shouldshowlinkedpeople)

### Configuring Person Views

- [var addressBook: ABAddressBook?](/documentation/addressbookui/abpersonviewcontroller/addressbook)
- [var allowsActions: Bool](/documentation/addressbookui/abpersonviewcontroller/allowsactions)
- [var allowsEditing: Bool](/documentation/addressbookui/abpersonviewcontroller/allowsediting)
- [func setHighlightedItemForProperty(ABPropertyID, withIdentifier: ABMultiValueIdentifier)](/documentation/addressbookui/abpersonviewcontroller/sethighlighteditemforproperty(_:withidentifier:))
- [ABUnknownPersonViewController](/documentation/addressbookui/abunknownpersonviewcontroller)

### Responding to View Controller Interactions

- [var unknownPersonViewDelegate: (any ABUnknownPersonViewControllerDelegate)?](/documentation/addressbookui/abunknownpersonviewcontroller/unknownpersonviewdelegate)
- [ABUnknownPersonViewControllerDelegate](/documentation/addressbookui/abunknownpersonviewcontrollerdelegate)

#### Responding to User Events

- [func unknownPersonViewController(ABUnknownPersonViewController, didResolveToPerson: ABRecord?)](/documentation/addressbookui/abunknownpersonviewcontrollerdelegate/unknownpersonviewcontroller(_:didresolvetoperson:))
- [func unknownPersonViewController(ABUnknownPersonViewController, shouldPerformDefaultActionForPerson: ABRecord, property: ABPropertyID, identifier: ABMultiValueIdentifier) -> Bool](/documentation/addressbookui/abunknownpersonviewcontrollerdelegate/unknownpersonviewcontroller(_:shouldperformdefaultactionforperson:property:identifier:))

### Displaying Person Properties

- [var alternateName: String?](/documentation/addressbookui/abunknownpersonviewcontroller/alternatename)
- [var message: String?](/documentation/addressbookui/abunknownpersonviewcontroller/message)
- [var displayedPerson: ABRecord](/documentation/addressbookui/abunknownpersonviewcontroller/displayedperson)

### Configuring the Interface Details

- [var addressBook: ABAddressBook?](/documentation/addressbookui/abunknownpersonviewcontroller/addressbook)
- [var allowsActions: Bool](/documentation/addressbookui/abunknownpersonviewcontroller/allowsactions)
- [var allowsAddingToAddressBook: Bool](/documentation/addressbookui/abunknownpersonviewcontroller/allowsaddingtoaddressbook)
- [func ABCreateStringWithAddressDictionary([AnyHashable : Any], Bool) -> String](/documentation/addressbookui/abcreatestringwithaddressdictionary(_:_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
