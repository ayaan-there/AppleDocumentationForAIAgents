# Social Documentation

Source: https://sosumi.ai/documentation/social

---
title: Social
source: https://developer.apple.com/documentation/social
timestamp: 2026-02-13T19:02:25.396Z
---

## Composition Interfaces

- [SLComposeServiceViewController](/documentation/social/slcomposeserviceviewcontroller)

### Configuring the Post Details

- [func configurationItems() -> [Any]!](/documentation/social/slcomposeserviceviewcontroller/configurationitems())
- [SLComposeSheetConfigurationItem](/documentation/social/slcomposesheetconfigurationitem)

#### Creating a Configuration Item

- [init!()](/documentation/social/slcomposesheetconfigurationitem/init())

#### Responding to User Interaction

- [var tapHandler: SLComposeSheetConfigurationItemTapHandler!](/documentation/social/slcomposesheetconfigurationitem/taphandler)
- [SLComposeSheetConfigurationItemTapHandler](/documentation/social/slcomposesheetconfigurationitemtaphandler)

#### Specifying Configuration Information

- [var title: String!](/documentation/social/slcomposesheetconfigurationitem/title)
- [var value: String!](/documentation/social/slcomposesheetconfigurationitem/value)
- [var valuePending: Bool](/documentation/social/slcomposesheetconfigurationitem/valuepending)
- [func reloadConfigurationItems()](/documentation/social/slcomposeserviceviewcontroller/reloadconfigurationitems())

### Managing the Contents of the Post

- [var contentText: String!](/documentation/social/slcomposeserviceviewcontroller/contenttext)
- [var placeholder: String!](/documentation/social/slcomposeserviceviewcontroller/placeholder)
- [var textView: UITextView!](/documentation/social/slcomposeserviceviewcontroller/textview)

### Presenting the View Controller

- [func pushConfigurationViewController(UIViewController!)](/documentation/social/slcomposeserviceviewcontroller/pushconfigurationviewcontroller(_:))
- [func popConfigurationViewController()](/documentation/social/slcomposeserviceviewcontroller/popconfigurationviewcontroller())

### Responding to Lifecycle Events

- [func presentationAnimationDidFinish()](/documentation/social/slcomposeserviceviewcontroller/presentationanimationdidfinish())
- [func didSelectCancel()](/documentation/social/slcomposeserviceviewcontroller/didselectcancel())
- [func didSelectPost()](/documentation/social/slcomposeserviceviewcontroller/didselectpost())

### Canceling a Post

- [func cancel()](/documentation/social/slcomposeserviceviewcontroller/cancel())

### Validating Content

- [var charactersRemaining: NSNumber!](/documentation/social/slcomposeserviceviewcontroller/charactersremaining)
- [func isContentValid() -> Bool](/documentation/social/slcomposeserviceviewcontroller/iscontentvalid())
- [func validateContent()](/documentation/social/slcomposeserviceviewcontroller/validatecontent())

### Previewing Attachments

- [func loadPreviewView() -> UIView!](/documentation/social/slcomposeserviceviewcontroller/loadpreviewview())

### Enabling Text Autocompletion

- [var autoCompletionViewController: UIViewController!](/documentation/social/slcomposeserviceviewcontroller/autocompletionviewcontroller)
- [SLComposeViewController](/documentation/social/slcomposeviewcontroller)

### Creating a Social Compose View Controller

- [init!(forServiceType: String!)](/documentation/social/slcomposeviewcontroller/init(forservicetype:))

### Checking the Social Service Type

- [class func isAvailable(forServiceType: String!) -> Bool](/documentation/social/slcomposeviewcontroller/isavailable(forservicetype:))
- [var serviceType: String!](/documentation/social/slcomposeviewcontroller/servicetype)

### Specifying the Contents of the Post

- [func setInitialText(String!) -> Bool](/documentation/social/slcomposeviewcontroller/setinitialtext(_:))
- [func add(UIImage!) -> Bool](/documentation/social/slcomposeviewcontroller/add(_:)-1z68a)
- [func add(URL!) -> Bool](/documentation/social/slcomposeviewcontroller/add(_:)-3mn1w)
- [func removeAllImages() -> Bool](/documentation/social/slcomposeviewcontroller/removeallimages())
- [func removeAllURLs() -> Bool](/documentation/social/slcomposeviewcontroller/removeallurls())

### Processing the Results

- [var completionHandler: SLComposeViewControllerCompletionHandler!](/documentation/social/slcomposeviewcontroller/completionhandler)
- [SLComposeViewControllerCompletionHandler](/documentation/social/slcomposeviewcontrollercompletionhandler)
- [SLComposeViewControllerResult](/documentation/social/slcomposeviewcontrollerresult)

#### Constants

- [case cancelled](/documentation/social/slcomposeviewcontrollerresult/cancelled)
- [case done](/documentation/social/slcomposeviewcontrollerresult/done)

#### Initializers

- [init?(rawValue: Int)](/documentation/social/slcomposeviewcontrollerresult/init(rawvalue:))

## Server Communication

- [SLRequest](/documentation/social/slrequest)

### Initializing Requests

- [init!(forServiceType: String!, requestMethod: SLRequestMethod, url: URL!, parameters: [AnyHashable : Any]!)](/documentation/social/slrequest/init(forservicetype:requestmethod:url:parameters:))
- [let SLServiceTypeFacebook: String](/documentation/social/slservicetypefacebook)
- [let SLServiceTypeTwitter: String](/documentation/social/slservicetypetwitter)
- [let SLServiceTypeSinaWeibo: String](/documentation/social/slservicetypesinaweibo)
- [let SLServiceTypeLinkedIn: String](/documentation/social/slservicetypelinkedin)
- [let SLServiceTypeTencentWeibo: String](/documentation/social/slservicetypetencentweibo)

### Sending a Request

- [func perform(handler: SLRequestHandler!)](/documentation/social/slrequest/perform(handler:))
- [SLRequestHandler](/documentation/social/slrequesthandler)

### Providing User Credentials

- [var account: ACAccount!](/documentation/social/slrequest/account)

### Getting the Request Details

- [func preparedURLRequest() -> URLRequest!](/documentation/social/slrequest/preparedurlrequest())
- [var requestMethod: SLRequestMethod](/documentation/social/slrequest/requestmethod)
- [SLRequestMethod](/documentation/social/slrequestmethod)

#### Constants

- [case GET](/documentation/social/slrequestmethod/get)
- [case POST](/documentation/social/slrequestmethod/post)
- [case DELETE](/documentation/social/slrequestmethod/delete)
- [case PUT](/documentation/social/slrequestmethod/put)

#### Initializers

- [init?(rawValue: Int)](/documentation/social/slrequestmethod/init(rawvalue:))
- [var url: URL!](/documentation/social/slrequest/url)
- [var parameters: [AnyHashable : Any]!](/documentation/social/slrequest/parameters)

### Adding Data to the Request

- [func addMultipartData(Data!, withName: String!, type: String!, filename: String!)](/documentation/social/slrequest/addmultipartdata(_:withname:type:filename:))
- [func addMultipartData(Data!, withName: String!, type: String!)](/documentation/social/slrequest/addmultipartdata(_:withname:type:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
