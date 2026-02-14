# Shared with You Documentation

Source: https://sosumi.ai/documentation/sharedwithyou

---
title: Shared with You
source: https://developer.apple.com/documentation/sharedwithyou
timestamp: 2026-02-13T19:02:09.800Z
---

## Frameworks

- [Shared with You Core](/documentation/sharedwithyoucore)

## Shared content

- [Making your app content shareable](/documentation/sharedwithyou/making-your-app-content-shareable)
- [Shared content interactions](/documentation/sharedwithyou/shared-content-interactions)

### Attributions

- [SWAttributionView](/documentation/sharedwithyou/swattributionview)

#### Customizing highlights

- [var backgroundStyle: SWAttributionView.BackgroundStyle](/documentation/sharedwithyou/swattributionview/backgroundstyle-swift.property)
- [var displayContext: SWAttributionView.DisplayContext](/documentation/sharedwithyou/swattributionview/displaycontext-swift.property)
- [var highlight: SWHighlight?](/documentation/sharedwithyou/swattributionview/highlight)
- [var highlightMenu: UIMenu](/documentation/sharedwithyou/swattributionview/highlightmenu)
- [var horizontalAlignment: SWAttributionView.HorizontalAlignment](/documentation/sharedwithyou/swattributionview/horizontalalignment-swift.property)
- [var menuTitleForHideAction: String?](/documentation/sharedwithyou/swattributionview/menutitleforhideaction)
- [var preferredMaxLayoutWidth: CGFloat](/documentation/sharedwithyou/swattributionview/preferredmaxlayoutwidth)
- [var supplementalMenu: UIMenu?](/documentation/sharedwithyou/swattributionview/supplementalmenu)

#### Customizing the view

- [SWAttributionView.BackgroundStyle](/documentation/sharedwithyou/swattributionview/backgroundstyle-swift.enum)

##### Background styles

- [case `default`](/documentation/sharedwithyou/swattributionview/backgroundstyle-swift.enum/default)
- [case color](/documentation/sharedwithyou/swattributionview/backgroundstyle-swift.enum/color)
- [case material](/documentation/sharedwithyou/swattributionview/backgroundstyle-swift.enum/material)

##### Initializers

- [init?(rawValue: Int)](/documentation/sharedwithyou/swattributionview/backgroundstyle-swift.enum/init(rawvalue:))
- [SWAttributionView.DisplayContext](/documentation/sharedwithyou/swattributionview/displaycontext-swift.enum)

##### Context styles

- [case summary](/documentation/sharedwithyou/swattributionview/displaycontext-swift.enum/summary)
- [case detail](/documentation/sharedwithyou/swattributionview/displaycontext-swift.enum/detail)

##### Initializers

- [init?(rawValue: Int)](/documentation/sharedwithyou/swattributionview/displaycontext-swift.enum/init(rawvalue:))
- [SWAttributionView.HorizontalAlignment](/documentation/sharedwithyou/swattributionview/horizontalalignment-swift.enum)

##### Horizontal alignments

- [case `default`](/documentation/sharedwithyou/swattributionview/horizontalalignment-swift.enum/default)
- [case leading](/documentation/sharedwithyou/swattributionview/horizontalalignment-swift.enum/leading)
- [case center](/documentation/sharedwithyou/swattributionview/horizontalalignment-swift.enum/center)
- [case trailing](/documentation/sharedwithyou/swattributionview/horizontalalignment-swift.enum/trailing)

##### Initializers

- [init?(rawValue: Int)](/documentation/sharedwithyou/swattributionview/horizontalalignment-swift.enum/init(rawvalue:))

### Highlights

- [SWHighlight](/documentation/sharedwithyou/swhighlight)

#### Viewing highlight attributes

- [var identifier: any NSCopying & NSSecureCoding](/documentation/sharedwithyou/swhighlight/identifier)
- [var url: URL](/documentation/sharedwithyou/swhighlight/url)
- [SWHighlightCenter](/documentation/sharedwithyou/swhighlightcenter)

#### Setting the delegate

- [var delegate: (any SWHighlightCenterDelegate)?](/documentation/sharedwithyou/swhighlightcenter/delegate)
- [SWHighlightCenterDelegate](/documentation/sharedwithyou/swhighlightcenterdelegate)

##### Protocol Attributes

- [func highlightCenterHighlightsDidChange(SWHighlightCenter)](/documentation/sharedwithyou/swhighlightcenterdelegate/highlightcenterhighlightsdidchange(_:))

#### Accessing highlights

- [var highlights: [SWHighlight]](/documentation/sharedwithyou/swhighlightcenter/highlights)
- [class var highlightCollectionTitle: String](/documentation/sharedwithyou/swhighlightcenter/highlightcollectiontitle)

#### Retrieving collaboration highlights

- [class var isSystemCollaborationSupportAvailable: Bool](/documentation/sharedwithyou/swhighlightcenter/issystemcollaborationsupportavailable)
- [func collaborationHighlight(forIdentifier: SWCollaborationIdentifier) throws -> SWCollaborationHighlight](/documentation/sharedwithyou/swhighlightcenter/collaborationhighlight(foridentifier:)-23ytv)
- [func collaborationHighlight(forIdentifier: String) throws -> SWCollaborationHighlight](/documentation/sharedwithyou/swhighlightcenter/collaborationhighlight(foridentifier:)-87lhr)
- [func getCollaborationHighlight(for: URL, completionHandler: (SWCollaborationHighlight?, (any Error)?) -> Void)](/documentation/sharedwithyou/swhighlightcenter/getcollaborationhighlight(for:completionhandler:))
- [func getHighlightFor(URL, completionHandler: (SWHighlight?, (any Error)?) -> Void)](/documentation/sharedwithyou/swhighlightcenter/gethighlightfor(_:completionhandler:))
- [func getSignedIdentityProof(for: SWCollaborationHighlight, using: Data, completionHandler: (SWPerson.SignedIdentityProof?, (any Error)?) -> Void)](/documentation/sharedwithyou/swhighlightcenter/getsignedidentityproof(for:using:completionhandler:))

#### Posting highlight events

- [func postNotice(for: any SWHighlightEvent)](/documentation/sharedwithyou/swhighlightcenter/postnotice(for:))
- [func clearNotices(for: SWCollaborationHighlight)](/documentation/sharedwithyou/swhighlightcenter/clearnotices(for:))

#### Handling errors

- [SWHighlightCenterErrorCode](/documentation/sharedwithyou/swhighlightcentererrorcode)

##### Highlight center errors

- [case noError](/documentation/sharedwithyou/swhighlightcentererrorcode/noerror)
- [case internalError](/documentation/sharedwithyou/swhighlightcentererrorcode/internalerror)
- [case invalidURL](/documentation/sharedwithyou/swhighlightcentererrorcode/invalidurl)
- [case accessDenied](/documentation/sharedwithyou/swhighlightcentererrorcode/accessdenied)

##### Initializers

- [init?(rawValue: Int)](/documentation/sharedwithyou/swhighlightcentererrorcode/init(rawvalue:))

### Highlight events

- [SWHighlightEvent](/documentation/sharedwithyou/swhighlightevent)

#### Accessing the URL

- [var highlightURL: URL](/documentation/sharedwithyou/swhighlightevent/highlighturl)
- [SWHighlightChangeEvent](/documentation/sharedwithyou/swhighlightchangeevent)

#### Creating a change event

- [init(highlight: SWHighlight, trigger: SWHighlightChangeEventTrigger)](/documentation/sharedwithyou/swhighlightchangeevent/init(highlight:trigger:))

#### Accessing event attributes

- [var highlightURL: URL](/documentation/sharedwithyou/swhighlightchangeevent/highlighturl)
- [var changeEventTrigger: SWHighlightChangeEventTrigger](/documentation/sharedwithyou/swhighlightchangeevent/changeeventtrigger)
- [SWHighlightChangeEventTrigger](/documentation/sharedwithyou/swhighlightchangeeventtrigger)

##### Change actions

- [case edit](/documentation/sharedwithyou/swhighlightchangeeventtrigger/edit)
- [case comment](/documentation/sharedwithyou/swhighlightchangeeventtrigger/comment)

##### Initializers

- [init?(rawValue: Int)](/documentation/sharedwithyou/swhighlightchangeeventtrigger/init(rawvalue:))
- [SWHighlightMembershipEvent](/documentation/sharedwithyou/swhighlightmembershipevent)

#### Creating a membership event

- [init(highlight: SWHighlight, trigger: SWHighlightMembershipEventTrigger)](/documentation/sharedwithyou/swhighlightmembershipevent/init(highlight:trigger:))

#### Accessing an event trigger

- [var membershipEventTrigger: SWHighlightMembershipEventTrigger](/documentation/sharedwithyou/swhighlightmembershipevent/membershipeventtrigger)
- [SWHighlightMembershipEventTrigger](/documentation/sharedwithyou/swhighlightmembershipeventtrigger)

##### Collaborator actions

- [case addedCollaborator](/documentation/sharedwithyou/swhighlightmembershipeventtrigger/addedcollaborator)
- [case removedCollaborator](/documentation/sharedwithyou/swhighlightmembershipeventtrigger/removedcollaborator)

##### Initializers

- [init?(rawValue: Int)](/documentation/sharedwithyou/swhighlightmembershipeventtrigger/init(rawvalue:))
- [SWHighlightMentionEvent](/documentation/sharedwithyou/swhighlightmentionevent)

#### Creating a mention event

- [init(highlight: SWHighlight, mentionedPersonCloudKitShareHandle: String)](/documentation/sharedwithyou/swhighlightmentionevent/init(highlight:mentionedpersoncloudkitsharehandle:))
- [init(highlight: SWHighlight, mentionedPersonIdentity: SWPerson.Identity)](/documentation/sharedwithyou/swhighlightmentionevent/init(highlight:mentionedpersonidentity:))

#### Accessing the event person

- [var mentionedPersonHandle: String](/documentation/sharedwithyou/swhighlightmentionevent/mentionedpersonhandle)
- [SWHighlightPersistenceEvent](/documentation/sharedwithyou/swhighlightpersistenceevent)

#### Creating a persistence event

- [init(highlight: SWHighlight, trigger: SWHighlightPersistenceEventTrigger)](/documentation/sharedwithyou/swhighlightpersistenceevent/init(highlight:trigger:))

#### Accessing an event trigger

- [var persistenceEventTrigger: SWHighlightPersistenceEventTrigger](/documentation/sharedwithyou/swhighlightpersistenceevent/persistenceeventtrigger)
- [SWHighlightPersistenceEventTrigger](/documentation/sharedwithyou/swhighlightpersistenceeventtrigger)

##### Persistence actions

- [case created](/documentation/sharedwithyou/swhighlightpersistenceeventtrigger/created)
- [case deleted](/documentation/sharedwithyou/swhighlightpersistenceeventtrigger/deleted)
- [case renamed](/documentation/sharedwithyou/swhighlightpersistenceeventtrigger/renamed)
- [case moved](/documentation/sharedwithyou/swhighlightpersistenceeventtrigger/moved)

##### Initializers

- [init?(rawValue: Int)](/documentation/sharedwithyou/swhighlightpersistenceeventtrigger/init(rawvalue:))

### Participants

- [SWPerson](/documentation/sharedwithyoucore/swperson)
- [SWRemoveParticipantAlert](/documentation/sharedwithyou/swremoveparticipantalert)

#### Requesting participant removal

- [class func show(withParticipant: SWPerson, highlight: SWCollaborationHighlight, in: NSWindow?)](/documentation/sharedwithyou/swremoveparticipantalert/show(withparticipant:highlight:in:))
- [SWRemoveParticipantAlertController](/documentation/sharedwithyou/swremoveparticipantalertcontroller)

##### Creating the alert controller

- [convenience init(participant: SWPerson, highlight: SWCollaborationHighlight)](/documentation/sharedwithyou/swremoveparticipantalertcontroller/init(participant:highlight:))

## Collaboration

- [Adding shared content collaboration to your app](/documentation/sharedwithyou/adding-shared-content-collaboration-to-your-app)
- [Adding custom collaboration to your app](/documentation/sharedwithyou/adding-custom-collaboration-to-your-app)
- [Collaboration views](/documentation/sharedwithyou/collaboration-views)

### Collaboration views

- [SWCollaborationView](/documentation/sharedwithyou/swcollaborationview)

#### Creating a collaboration view

- [init(itemProvider: NSItemProvider)](/documentation/sharedwithyou/swcollaborationview/init(itemprovider:))

#### Accessing view attributes

- [var activeParticipantCount: Int](/documentation/sharedwithyou/swcollaborationview/activeparticipantcount)
- [var cloudSharingDelegate: (any UICloudSharingControllerDelegate)?](/documentation/sharedwithyou/swcollaborationview/cloudsharingdelegate)
- [var delegate: (any SWCollaborationViewDelegate)?](/documentation/sharedwithyou/swcollaborationview/delegate)
- [var headerImage: UIImage](/documentation/sharedwithyou/swcollaborationview/headerimage)
- [var headerSubtitle: String](/documentation/sharedwithyou/swcollaborationview/headersubtitle)
- [var headerTitle: String](/documentation/sharedwithyou/swcollaborationview/headertitle)
- [var manageButtonTitle: String](/documentation/sharedwithyou/swcollaborationview/managebuttontitle)
- [var menuFormRepresentation: NSMenuItem](/documentation/sharedwithyou/swcollaborationview/menuformrepresentation-3sffe)
- [var menuFormRepresentation: NSMenuItem](/documentation/sharedwithyou/swcollaborationview/menuformrepresentation-55skx)

#### Setting view attributes

- [func setContent(UIView)](/documentation/sharedwithyou/swcollaborationview/setcontent(_:))
- [func setDetailViewListContent<ListContent>(ListContent)](/documentation/sharedwithyou/swcollaborationview/setdetailviewlistcontent(_:)-88gy5)
- [func setDetailViewListContent<ListContent>(() -> ListContent)](/documentation/sharedwithyou/swcollaborationview/setdetailviewlistcontent(_:)-8ml1c)
- [func setShowManageButton(Bool)](/documentation/sharedwithyou/swcollaborationview/setshowmanagebutton(_:))

#### Dismissing the popover

- [func dismissPopover((() -> Void)?)](/documentation/sharedwithyou/swcollaborationview/dismisspopover(_:))

#### Customizing the cloud-sharing behavior

- [var cloudSharingControllerDelegate: (any UICloudSharingControllerDelegate)?](/documentation/sharedwithyou/swcollaborationview/cloudsharingcontrollerdelegate)
- [var cloudSharingServiceDelegate: (any NSCloudSharingServiceDelegate)?](/documentation/sharedwithyou/swcollaborationview/cloudsharingservicedelegate)

### Collaboration attributes

- [SWCollaborationHighlight](/documentation/sharedwithyou/swcollaborationhighlight)

#### Accessing collaboration attributes

- [var collaborationIdentifier: String](/documentation/sharedwithyou/swcollaborationhighlight/collaborationidentifier)
- [var contentType: UTType](/documentation/sharedwithyou/swcollaborationhighlight/contenttype)
- [var creationDate: Date](/documentation/sharedwithyou/swcollaborationhighlight/creationdate)
- [var title: String?](/documentation/sharedwithyou/swcollaborationhighlight/title)
- [SWCollaborationMetadata](/documentation/sharedwithyoucore/swcollaborationmetadata)
- [SWCollaborationIdentifier](/documentation/sharedwithyoucore/swcollaborationidentifier)
- [SWLocalCollaborationIdentifier](/documentation/sharedwithyoucore/swlocalcollaborationidentifier)
- [let SWCollaborationMetadataTypeIdentifier: String](/documentation/sharedwithyou/swcollaborationmetadatatypeidentifier)

### Collaboration management

- [SWCollaborationViewDelegate](/documentation/sharedwithyou/swcollaborationviewdelegate)

#### Responding to popover activity

- [func collaborationViewShouldPresentPopover(SWCollaborationView) -> Bool](/documentation/sharedwithyou/swcollaborationviewdelegate/collaborationviewshouldpresentpopover(_:))
- [func collaborationViewDidDismissPopover(SWCollaborationView)](/documentation/sharedwithyou/swcollaborationviewdelegate/collaborationviewdiddismisspopover(_:))
- [func collaborationViewWillPresentPopover(SWCollaborationView)](/documentation/sharedwithyou/swcollaborationviewdelegate/collaborationviewwillpresentpopover(_:))
- [SWCollaborationCoordinator](/documentation/sharedwithyoucore/swcollaborationcoordinator)
- [SWCollaborationOption](/documentation/sharedwithyoucore/swcollaborationoption)
- [SWCollaborationOptionsGroup](/documentation/sharedwithyoucore/swcollaborationoptionsgroup)
- [SWCollaborationOptionsPickerGroup](/documentation/sharedwithyoucore/swcollaborationoptionspickergroup)
- [SWCollaborationShareOptions](/documentation/sharedwithyoucore/swcollaborationshareoptions)
- [let UTCollaborationOptionsTypeIdentifier: String](/documentation/sharedwithyoucore/utcollaborationoptionstypeidentifier)

### Actions

- [SWAction](/documentation/sharedwithyoucore/swaction)
- [SWStartCollaborationAction](/documentation/sharedwithyoucore/swstartcollaborationaction)
- [SWCollaborationActionHandler](/documentation/sharedwithyoucore/swcollaborationactionhandler)
- [SWUpdateCollaborationParticipantsAction](/documentation/sharedwithyoucore/swupdatecollaborationparticipantsaction)

## Framework versions

- [Version number](/documentation/sharedwithyou/version-number)
- [Version string](/documentation/sharedwithyou/version-string)

## Macros

- [Macros](/documentation/sharedwithyou/macros)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
