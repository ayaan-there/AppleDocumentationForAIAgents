# Contacts UI Documentation

Source: https://sosumi.ai/documentation/contactsui

---
title: Contacts UI
source: https://developer.apple.com/documentation/contactsui
timestamp: 2026-02-13T18:55:08.023Z
---

## Contact viewer

- [CNContactViewController](/documentation/contactsui/cncontactviewcontroller)

### Creating the Contact Viewer

- [convenience init(for: CNContact)](/documentation/contactsui/cncontactviewcontroller/init(for:))
- [convenience init(forContact: CNContact)](/documentation/contactsui/cncontactviewcontroller/init(forcontact:))
- [convenience init(forUnknownContact: CNContact)](/documentation/contactsui/cncontactviewcontroller/init(forunknowncontact:))
- [convenience init(forNewContact: CNContact?)](/documentation/contactsui/cncontactviewcontroller/init(fornewcontact:))

### Handling Interactions with the Interface

- [var delegate: (any CNContactViewControllerDelegate)?](/documentation/contactsui/cncontactviewcontroller/delegate)
- [CNContactViewControllerDelegate](/documentation/contactsui/cncontactviewcontrollerdelegate)

#### Responding to User Events

- [func contactViewController(CNContactViewController, shouldPerformDefaultActionFor: CNContactProperty) -> Bool](/documentation/contactsui/cncontactviewcontrollerdelegate/contactviewcontroller(_:shouldperformdefaultactionfor:))
- [func contactViewController(CNContactViewController, didCompleteWith: CNContact?)](/documentation/contactsui/cncontactviewcontrollerdelegate/contactviewcontroller(_:didcompletewith:))

### Required Keys

- [class func descriptorForRequiredKeys() -> any CNKeyDescriptor](/documentation/contactsui/cncontactviewcontroller/descriptorforrequiredkeys())

### Displaying Contact Properties

- [var contact: CNContact](/documentation/contactsui/cncontactviewcontroller/contact)
- [var alternateName: String?](/documentation/contactsui/cncontactviewcontroller/alternatename)
- [var message: String?](/documentation/contactsui/cncontactviewcontroller/message)
- [var displayedPropertyKeys: [Any]?](/documentation/contactsui/cncontactviewcontroller/displayedpropertykeys)

### Configuring the Contact’s Relationships

- [var parentGroup: CNGroup?](/documentation/contactsui/cncontactviewcontroller/parentgroup)
- [var parentContainer: CNContainer?](/documentation/contactsui/cncontactviewcontroller/parentcontainer)

### Contact Store

- [var contactStore: CNContactStore?](/documentation/contactsui/cncontactviewcontroller/contactstore)

### Customizing Contact Card

- [var allowsEditing: Bool](/documentation/contactsui/cncontactviewcontroller/allowsediting)
- [var allowsActions: Bool](/documentation/contactsui/cncontactviewcontroller/allowsactions)
- [var shouldShowLinkedContacts: Bool](/documentation/contactsui/cncontactviewcontroller/shouldshowlinkedcontacts)

### Highlighting a Property

- [func highlightProperty(withKey: String, identifier: String?)](/documentation/contactsui/cncontactviewcontroller/highlightproperty(withkey:identifier:))

## Contact pickers

- [CNContactPickerViewController](/documentation/contactsui/cncontactpickerviewcontroller)

### Displaying Contacts Properties

- [var displayedPropertyKeys: [String]?](/documentation/contactsui/cncontactpickerviewcontroller/displayedpropertykeys)

### Responding to User Interactions

- [var delegate: (any CNContactPickerDelegate)?](/documentation/contactsui/cncontactpickerviewcontroller/delegate)
- [CNContactPickerDelegate](/documentation/contactsui/cncontactpickerdelegate)

#### Responding to User Selections

- [func contactPicker(CNContactPickerViewController, didSelect: CNContact)](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselect:)-7vcyc)
- [func contactPicker(CNContactPickerViewController, didSelect: CNContactProperty)](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselect:)-1xfpt)
- [func contactPicker(CNContactPickerViewController, didSelect: [CNContact])](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselect:)-5neeo)
- [func contactPicker(CNContactPickerViewController, didSelectContactProperties: [CNContactProperty])](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselectcontactproperties:))

#### Dismissing the Picker Interface

- [func contactPickerDidCancel(CNContactPickerViewController)](/documentation/contactsui/cncontactpickerdelegate/contactpickerdidcancel(_:))
- [func contactPickerWillClose(CNContactPicker)](/documentation/contactsui/cncontactpickerdelegate/contactpickerwillclose(_:))
- [func contactPickerDidClose(CNContactPicker)](/documentation/contactsui/cncontactpickerdelegate/contactpickerdidclose(_:))

### Predicates For Selecting Contacts

- [var predicateForEnablingContact: NSPredicate?](/documentation/contactsui/cncontactpickerviewcontroller/predicateforenablingcontact)
- [var predicateForSelectionOfContact: NSPredicate?](/documentation/contactsui/cncontactpickerviewcontroller/predicateforselectionofcontact)
- [var predicateForSelectionOfProperty: NSPredicate?](/documentation/contactsui/cncontactpickerviewcontroller/predicateforselectionofproperty)
- [CNContactPicker](/documentation/contactsui/cncontactpicker)

### Responding to Picker Interactions

- [var delegate: (any CNContactPickerDelegate)?](/documentation/contactsui/cncontactpicker/delegate)
- [CNContactPickerDelegate](/documentation/contactsui/cncontactpickerdelegate)

#### Responding to User Selections

- [func contactPicker(CNContactPickerViewController, didSelect: CNContact)](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselect:)-7vcyc)
- [func contactPicker(CNContactPickerViewController, didSelect: CNContactProperty)](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselect:)-1xfpt)
- [func contactPicker(CNContactPickerViewController, didSelect: [CNContact])](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselect:)-5neeo)
- [func contactPicker(CNContactPickerViewController, didSelectContactProperties: [CNContactProperty])](/documentation/contactsui/cncontactpickerdelegate/contactpicker(_:didselectcontactproperties:))

#### Dismissing the Picker Interface

- [func contactPickerDidCancel(CNContactPickerViewController)](/documentation/contactsui/cncontactpickerdelegate/contactpickerdidcancel(_:))
- [func contactPickerWillClose(CNContactPicker)](/documentation/contactsui/cncontactpickerdelegate/contactpickerwillclose(_:))
- [func contactPickerDidClose(CNContactPicker)](/documentation/contactsui/cncontactpickerdelegate/contactpickerdidclose(_:))

### Configuring the Picker Contents

- [var displayedKeys: [String]](/documentation/contactsui/cncontactpicker/displayedkeys)

### Displaying the Popover

- [func showRelative(to: NSRect, of: NSView, preferredEdge: NSRectEdge)](/documentation/contactsui/cncontactpicker/showrelative(to:of:preferrededge:))

### Closing the Popover

- [func close()](/documentation/contactsui/cncontactpicker/close())

## Contact access

- [ContactAccessButton](/documentation/contactsui/contactaccessbutton)

### Creating a contact access button

- [init(queryString: String, ignoredEmails: Set<String>?, ignoredPhoneNumbers: Set<String>?, approvalCallback: (([String]) -> ())?)](/documentation/contactsui/contactaccessbutton/init(querystring:ignoredemails:ignoredphonenumbers:approvalcallback:))

### Setting the button caption

- [ContactAccessButton.Caption](/documentation/contactsui/contactaccessbutton/caption)

#### Caption options

- [case defaultText](/documentation/contactsui/contactaccessbutton/caption/defaulttext)
- [case email](/documentation/contactsui/contactaccessbutton/caption/email)
- [case phone](/documentation/contactsui/contactaccessbutton/caption/phone)

### Accessing button style

- [ContactAccessButton.Style](/documentation/contactsui/contactaccessbutton/style)

#### Creating a style instance

- [init(imageTrailingEdgePadding: CGFloat?, imageWidth: CGFloat?, imageColor: Color?)](/documentation/contactsui/contactaccessbutton/style/init(imagetrailingedgepadding:imagewidth:imagecolor:))

#### Working with common styles

- [static let automatic: ContactAccessButton.Style](/documentation/contactsui/contactaccessbutton/style/automatic)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
