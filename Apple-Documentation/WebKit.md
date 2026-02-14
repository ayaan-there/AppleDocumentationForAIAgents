# WebKit Documentation

Source: https://sosumi.ai/documentation/webkit

---
title: WebKit
source: https://developer.apple.com/documentation/webkit
timestamp: 2026-02-13T19:04:08.871Z
---

## WebKit APIs

- [WebKit for AppKit and UIKit](/documentation/webkit/webkit-for-appkit-and-uikit)

### Web views

- [Replacing UIWebView in your app](/documentation/webkit/replacing-uiwebview-in-your-app)
- [Viewing Desktop or Mobile Web Content Using a Web View](/documentation/webkit/viewing-desktop-or-mobile-web-content-using-a-web-view)
- [WKWebView](/documentation/webkit/wkwebview)

#### Creating a web view

- [init(frame: CGRect, configuration: WKWebViewConfiguration)](/documentation/webkit/wkwebview/init(frame:configuration:))
- [init?(coder: NSCoder)](/documentation/webkit/wkwebview/init(coder:))
- [var configuration: WKWebViewConfiguration](/documentation/webkit/wkwebview/configuration)

#### Determining whether WebKit can load content

- [class func handlesURLScheme(String) -> Bool](/documentation/webkit/wkwebview/handlesurlscheme(_:))

#### Displaying native user interface elements

- [var uiDelegate: (any WKUIDelegate)?](/documentation/webkit/wkwebview/uidelegate)
- [WKUIDelegate](/documentation/webkit/wkuidelegate)

##### Creating and closing the web view

- [func webView(WKWebView, createWebViewWith: WKWebViewConfiguration, for: WKNavigationAction, windowFeatures: WKWindowFeatures) -> WKWebView?](/documentation/webkit/wkuidelegate/webview(_:createwebviewwith:for:windowfeatures:))
- [func webViewDidClose(WKWebView)](/documentation/webkit/wkuidelegate/webviewdidclose(_:))

##### Displaying UI panels

- [func webView(WKWebView, runJavaScriptAlertPanelWithMessage: String, initiatedByFrame: WKFrameInfo, completionHandler: () -> Void)](/documentation/webkit/wkuidelegate/webview(_:runjavascriptalertpanelwithmessage:initiatedbyframe:completionhandler:))
- [func webView(WKWebView, runJavaScriptConfirmPanelWithMessage: String, initiatedByFrame: WKFrameInfo, completionHandler: (Bool) -> Void)](/documentation/webkit/wkuidelegate/webview(_:runjavascriptconfirmpanelwithmessage:initiatedbyframe:completionhandler:))
- [func webView(WKWebView, runJavaScriptTextInputPanelWithPrompt: String, defaultText: String?, initiatedByFrame: WKFrameInfo, completionHandler: (String?) -> Void)](/documentation/webkit/wkuidelegate/webview(_:runjavascripttextinputpanelwithprompt:defaulttext:initiatedbyframe:completionhandler:))
- [func webView(WKWebView, showLockdownModeFirstUseMessage: String, completionHandler: (WKDialogResult) -> Void)](/documentation/webkit/wkuidelegate/webview(_:showlockdownmodefirstusemessage:completionhandler:))
- [WKDialogResult](/documentation/webkit/wkdialogresult)

###### First use dialog results

- [case askAgain](/documentation/webkit/wkdialogresult/askagain)
- [case handled](/documentation/webkit/wkdialogresult/handled)
- [case showDefault](/documentation/webkit/wkdialogresult/showdefault)

###### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkdialogresult/init(rawvalue:))

##### Displaying an upload panel

- [func webView(WKWebView, runOpenPanelWith: WKOpenPanelParameters, initiatedByFrame: WKFrameInfo, completionHandler: ([URL]?) -> Void)](/documentation/webkit/wkuidelegate/webview(_:runopenpanelwith:initiatedbyframe:completionhandler:))
- [WKOpenPanelParameters](/documentation/webkit/wkopenpanelparameters)

###### Configuring the panel parameters

- [var allowsMultipleSelection: Bool](/documentation/webkit/wkopenpanelparameters/allowsmultipleselection)
- [var allowsDirectories: Bool](/documentation/webkit/wkopenpanelparameters/allowsdirectories)

##### Displaying a contextual menu

- [Adding context menus in your app](/documentation/uikit/adding-context-menus-in-your-app)
- [func webView(WKWebView, contextMenuConfigurationForElement: WKContextMenuElementInfo, completionHandler: (UIContextMenuConfiguration?) -> Void)](/documentation/webkit/wkuidelegate/webview(_:contextmenuconfigurationforelement:completionhandler:))
- [func webView(WKWebView, contextMenuForElement: WKContextMenuElementInfo, willCommitWithAnimator: any UIContextMenuInteractionCommitAnimating)](/documentation/webkit/wkuidelegate/webview(_:contextmenuforelement:willcommitwithanimator:))
- [func webView(WKWebView, contextMenuWillPresentForElement: WKContextMenuElementInfo)](/documentation/webkit/wkuidelegate/webview(_:contextmenuwillpresentforelement:))
- [func webView(WKWebView, contextMenuDidEndForElement: WKContextMenuElementInfo)](/documentation/webkit/wkuidelegate/webview(_:contextmenudidendforelement:))
- [UIContextMenuConfiguration](/documentation/uikit/uicontextmenuconfiguration)

##### Displaying an edit menu

- [func webView(WKWebView, willDismissEditMenuWithAnimator: any UIEditMenuInteractionAnimating)](/documentation/webkit/wkuidelegate/webview(_:willdismisseditmenuwithanimator:))
- [func webView(WKWebView, willPresentEditMenuWithAnimator: any UIEditMenuInteractionAnimating)](/documentation/webkit/wkuidelegate/webview(_:willpresenteditmenuwithanimator:))

##### Requesting permissions

- [func webView(WKWebView, requestDeviceOrientationAndMotionPermissionFor: WKSecurityOrigin, initiatedByFrame: WKFrameInfo, decisionHandler: (WKPermissionDecision) -> Void)](/documentation/webkit/wkuidelegate/webview(_:requestdeviceorientationandmotionpermissionfor:initiatedbyframe:decisionhandler:))
- [func webView(WKWebView, requestMediaCapturePermissionFor: WKSecurityOrigin, initiatedByFrame: WKFrameInfo, type: WKMediaCaptureType, decisionHandler: (WKPermissionDecision) -> Void)](/documentation/webkit/wkuidelegate/webview(_:requestmediacapturepermissionfor:initiatedbyframe:type:decisionhandler:))
- [WKPermissionDecision](/documentation/webkit/wkpermissiondecision)

###### Constants

- [case deny](/documentation/webkit/wkpermissiondecision/deny)
- [case grant](/documentation/webkit/wkpermissiondecision/grant)
- [case prompt](/documentation/webkit/wkpermissiondecision/prompt)

###### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkpermissiondecision/init(rawvalue:))
- [WKMediaCaptureType](/documentation/webkit/wkmediacapturetype)

###### Constants

- [case camera](/documentation/webkit/wkmediacapturetype/camera)
- [case cameraAndMicrophone](/documentation/webkit/wkmediacapturetype/cameraandmicrophone)
- [case microphone](/documentation/webkit/wkmediacapturetype/microphone)

###### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkmediacapturetype/init(rawvalue:))

##### Deprecated

- [Deprecated symbols](/documentation/webkit/wkuidelegate-deprecated-symbols)

###### Responding to Force Touch actions

- [func webView(WKWebView, shouldPreviewElement: WKPreviewElementInfo) -> Bool](/documentation/webkit/wkuidelegate/webview(_:shouldpreviewelement:))
- [func webView(WKWebView, previewingViewControllerForElement: WKPreviewElementInfo, defaultActions: [any WKPreviewActionItem]) -> UIViewController?](/documentation/webkit/wkuidelegate/webview(_:previewingviewcontrollerforelement:defaultactions:))
- [func webView(WKWebView, commitPreviewingViewController: UIViewController)](/documentation/webkit/wkuidelegate/webview(_:commitpreviewingviewcontroller:))

#### Managing navigation between webpages

- [var navigationDelegate: (any WKNavigationDelegate)?](/documentation/webkit/wkwebview/navigationdelegate)
- [WKNavigationDelegate](/documentation/webkit/wknavigationdelegate)

##### Allowing or denying navigation requests

- [func webView(WKWebView, decidePolicyFor: WKNavigationAction, preferences: WKWebpagePreferences, decisionHandler: (WKNavigationActionPolicy, WKWebpagePreferences) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:decidepolicyfor:preferences:decisionhandler:))
- [func webView(WKWebView, decidePolicyFor: WKNavigationAction, decisionHandler: (WKNavigationActionPolicy) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:decidepolicyfor:decisionhandler:)-2ni62)
- [WKNavigationActionPolicy](/documentation/webkit/wknavigationactionpolicy)

###### Constants

- [case cancel](/documentation/webkit/wknavigationactionpolicy/cancel)
- [case allow](/documentation/webkit/wknavigationactionpolicy/allow)
- [case download](/documentation/webkit/wknavigationactionpolicy/download)

###### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wknavigationactionpolicy/init(rawvalue:))
- [func webView(WKWebView, decidePolicyFor: WKNavigationResponse, decisionHandler: (WKNavigationResponsePolicy) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:decidepolicyfor:decisionhandler:)-19mn2)
- [WKNavigationResponsePolicy](/documentation/webkit/wknavigationresponsepolicy)

###### Constants

- [case cancel](/documentation/webkit/wknavigationresponsepolicy/cancel)
- [case allow](/documentation/webkit/wknavigationresponsepolicy/allow)
- [case download](/documentation/webkit/wknavigationresponsepolicy/download)

###### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wknavigationresponsepolicy/init(rawvalue:))

##### Tracking the load progress of a request

- [func webView(WKWebView, didStartProvisionalNavigation: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didstartprovisionalnavigation:))
- [func webView(WKWebView, didReceiveServerRedirectForProvisionalNavigation: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didreceiveserverredirectforprovisionalnavigation:))
- [func webView(WKWebView, didCommit: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didcommit:))
- [func webView(WKWebView, didFinish: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didfinish:))

##### Responding to authentication challenges

- [func webView(WKWebView, didReceive: URLAuthenticationChallenge, completionHandler: (URLSession.AuthChallengeDisposition, URLCredential?) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:didreceive:completionhandler:))
- [func webView(WKWebView, authenticationChallenge: URLAuthenticationChallenge, shouldAllowDeprecatedTLS: (Bool) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:authenticationchallenge:shouldallowdeprecatedtls:))

##### Responding to navigation errors

- [func webView(WKWebView, didFail: WKNavigation!, withError: any Error)](/documentation/webkit/wknavigationdelegate/webview(_:didfail:witherror:))
- [func webView(WKWebView, didFailProvisionalNavigation: WKNavigation!, withError: any Error)](/documentation/webkit/wknavigationdelegate/webview(_:didfailprovisionalnavigation:witherror:))
- [func webViewWebContentProcessDidTerminate(WKWebView)](/documentation/webkit/wknavigationdelegate/webviewwebcontentprocessdidterminate(_:))

##### Handling download progress

- [func webView(WKWebView, navigationResponse: WKNavigationResponse, didBecome: WKDownload)](/documentation/webkit/wknavigationdelegate/webview(_:navigationresponse:didbecome:))
- [func webView(WKWebView, navigationAction: WKNavigationAction, didBecome: WKDownload)](/documentation/webkit/wknavigationdelegate/webview(_:navigationaction:didbecome:))

##### Instance Methods

- [func webView(WKWebView, shouldGoTo: WKBackForwardListItem, willUseInstantBack: Bool, completionHandler: (Bool) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:shouldgoto:willuseinstantback:completionhandler:))

#### Loading web content

- [func load(URLRequest) -> WKNavigation?](/documentation/webkit/wkwebview/load(_:))
- [func load(Data, mimeType: String, characterEncodingName: String, baseURL: URL) -> WKNavigation?](/documentation/webkit/wkwebview/load(_:mimetype:characterencodingname:baseurl:))
- [func loadHTMLString(String, baseURL: URL?) -> WKNavigation?](/documentation/webkit/wkwebview/loadhtmlstring(_:baseurl:))
- [func loadFileRequest(URLRequest, allowingReadAccessTo: URL) -> WKNavigation](/documentation/webkit/wkwebview/loadfilerequest(_:allowingreadaccessto:))
- [func loadFileURL(URL, allowingReadAccessTo: URL) -> WKNavigation?](/documentation/webkit/wkwebview/loadfileurl(_:allowingreadaccessto:))
- [func loadSimulatedRequest(URLRequest, response: URLResponse, responseData: Data) -> WKNavigation](/documentation/webkit/wkwebview/loadsimulatedrequest(_:response:responsedata:))
- [func loadSimulatedRequest(URLRequest, responseHTML: String) -> WKNavigation](/documentation/webkit/wkwebview/loadsimulatedrequest(_:responsehtml:))
- [var isLoading: Bool](/documentation/webkit/wkwebview/isloading)
- [var estimatedProgress: Double](/documentation/webkit/wkwebview/estimatedprogress)

#### Managing the loading process

- [func reload() -> WKNavigation?](/documentation/webkit/wkwebview/reload())
- [func reload(Any?)](/documentation/webkit/wkwebview/reload(_:))
- [func reloadFromOrigin() -> WKNavigation?](/documentation/webkit/wkwebview/reloadfromorigin())
- [func reloadFromOrigin(Any?)](/documentation/webkit/wkwebview/reloadfromorigin(_:))
- [func stopLoading()](/documentation/webkit/wkwebview/stoploading())
- [func stopLoading(Any?)](/documentation/webkit/wkwebview/stoploading(_:))

#### Managing downloads

- [func startDownload(using: URLRequest, completionHandler: (WKDownload) -> Void)](/documentation/webkit/wkwebview/startdownload(using:completionhandler:))
- [func resumeDownload(fromResumeData: Data, completionHandler: (WKDownload) -> Void)](/documentation/webkit/wkwebview/resumedownload(fromresumedata:completionhandler:))

#### Making web content inspectable

- [var isInspectable: Bool](/documentation/webkit/wkwebview/isinspectable)

#### Inspecting the view information

- [var scrollView: UIScrollView](/documentation/webkit/wkwebview/scrollview)
- [var title: String?](/documentation/webkit/wkwebview/title)
- [var url: URL?](/documentation/webkit/wkwebview/url)
- [var mediaType: String?](/documentation/webkit/wkwebview/mediatype)
- [var customUserAgent: String?](/documentation/webkit/wkwebview/customuseragent)
- [var serverTrust: SecTrust?](/documentation/webkit/wkwebview/servertrust)
- [var hasOnlySecureContent: Bool](/documentation/webkit/wkwebview/hasonlysecurecontent)
- [var themeColor: UIColor?](/documentation/webkit/wkwebview/themecolor)
- [var underPageBackgroundColor: UIColor!](/documentation/webkit/wkwebview/underpagebackgroundcolor)

#### Scaling content

- [var pageZoom: CGFloat](/documentation/webkit/wkwebview/pagezoom)
- [var allowsMagnification: Bool](/documentation/webkit/wkwebview/allowsmagnification)
- [var magnification: CGFloat](/documentation/webkit/wkwebview/magnification)
- [func setMagnification(CGFloat, centeredAt: CGPoint)](/documentation/webkit/wkwebview/setmagnification(_:centeredat:))

#### Interacting with media

- [func pauseAllMediaPlayback(completionHandler: (() -> Void)?)](/documentation/webkit/wkwebview/pauseallmediaplayback(completionhandler:))
- [func requestMediaPlaybackState(completionHandler: (WKMediaPlaybackState) -> Void)](/documentation/webkit/wkwebview/requestmediaplaybackstate(completionhandler:))
- [func setAllMediaPlaybackSuspended(Bool, completionHandler: (() -> Void)?)](/documentation/webkit/wkwebview/setallmediaplaybacksuspended(_:completionhandler:))
- [func closeAllMediaPresentations(completionHandler: (() -> Void)?)](/documentation/webkit/wkwebview/closeallmediapresentations(completionhandler:))
- [WKMediaPlaybackState](/documentation/webkit/wkmediaplaybackstate)

##### Constants

- [case none](/documentation/webkit/wkmediaplaybackstate/none)
- [case paused](/documentation/webkit/wkmediaplaybackstate/paused)
- [case playing](/documentation/webkit/wkmediaplaybackstate/playing)
- [case suspended](/documentation/webkit/wkmediaplaybackstate/suspended)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkmediaplaybackstate/init(rawvalue:))

#### Managing the microphone and camera

- [var cameraCaptureState: WKMediaCaptureState](/documentation/webkit/wkwebview/cameracapturestate)
- [var microphoneCaptureState: WKMediaCaptureState](/documentation/webkit/wkwebview/microphonecapturestate)
- [func setCameraCaptureState(WKMediaCaptureState, completionHandler: (() -> Void)?)](/documentation/webkit/wkwebview/setcameracapturestate(_:completionhandler:))
- [func setMicrophoneCaptureState(WKMediaCaptureState, completionHandler: (() -> Void)?)](/documentation/webkit/wkwebview/setmicrophonecapturestate(_:completionhandler:))
- [WKMediaCaptureState](/documentation/webkit/wkmediacapturestate)

##### Constants

- [case active](/documentation/webkit/wkmediacapturestate/active)
- [case muted](/documentation/webkit/wkmediacapturestate/muted)
- [case none](/documentation/webkit/wkmediacapturestate/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkmediacapturestate/init(rawvalue:))

#### Searching the current page’s content

- [func find(String, configuration: WKFindConfiguration, completionHandler: (WKFindResult) -> Void)](/documentation/webkit/wkwebview/find(_:configuration:completionhandler:))
- [func find(String, configuration: WKFindConfiguration) async throws -> WKFindResult](/documentation/webkit/wkwebview/find(_:configuration:))
- [WKFindConfiguration](/documentation/webkit/wkfindconfiguration)

##### Configuring the Search Parameters

- [var backwards: Bool](/documentation/webkit/wkfindconfiguration/backwards)
- [var caseSensitive: Bool](/documentation/webkit/wkfindconfiguration/casesensitive)
- [var wraps: Bool](/documentation/webkit/wkfindconfiguration/wraps)
- [WKFindResult](/documentation/webkit/wkfindresult)

##### Getting the Search Result

- [var matchFound: Bool](/documentation/webkit/wkfindresult/matchfound)

#### Navigating between webpages

- [var allowsBackForwardNavigationGestures: Bool](/documentation/webkit/wkwebview/allowsbackforwardnavigationgestures)
- [var backForwardList: WKBackForwardList](/documentation/webkit/wkwebview/backforwardlist)
- [func goBack(Any?)](/documentation/webkit/wkwebview/goback(_:))
- [func goBack() -> WKNavigation?](/documentation/webkit/wkwebview/goback())
- [func goForward(Any?)](/documentation/webkit/wkwebview/goforward(_:))
- [func goForward() -> WKNavigation?](/documentation/webkit/wkwebview/goforward())
- [func go(to: WKBackForwardListItem) -> WKNavigation?](/documentation/webkit/wkwebview/go(to:))
- [var canGoBack: Bool](/documentation/webkit/wkwebview/cangoback)
- [var canGoForward: Bool](/documentation/webkit/wkwebview/cangoforward)
- [var allowsLinkPreview: Bool](/documentation/webkit/wkwebview/allowslinkpreview)
- [var interactionState: Any?](/documentation/webkit/wkwebview/interactionstate)

#### Executing JavaScript

- [func evaluateJavaScript(String, completionHandler: ((Any?, (any Error)?) -> Void)?)](/documentation/webkit/wkwebview/evaluatejavascript(_:completionhandler:))
- [func evaluateJavaScript(String, in: WKFrameInfo?, in: WKContentWorld, completionHandler: ((Result<Any, any Error>) -> Void)?)](/documentation/webkit/wkwebview/evaluatejavascript(_:in:in:completionhandler:))
- [func evaluateJavaScript(String, in: WKFrameInfo?, contentWorld: WKContentWorld) async throws -> Any?](/documentation/webkit/wkwebview/evaluatejavascript(_:in:contentworld:))
- [func callAsyncJavaScript(String, arguments: [String : Any], in: WKFrameInfo?, in: WKContentWorld, completionHandler: ((Result<Any, any Error>) -> Void)?)](/documentation/webkit/wkwebview/callasyncjavascript(_:arguments:in:in:completionhandler:))
- [func callAsyncJavaScript(String, arguments: [String : Any], in: WKFrameInfo?, contentWorld: WKContentWorld) async throws -> Any?](/documentation/webkit/wkwebview/callasyncjavascript(_:arguments:in:contentworld:))

#### Capturing the web view’s content

- [func takeSnapshot(with: WKSnapshotConfiguration?, completionHandler: (UIImage?, (any Error)?) -> Void)](/documentation/webkit/wkwebview/takesnapshot(with:completionhandler:))
- [func createPDF(configuration: WKPDFConfiguration, completionHandler: (Result<Data, any Error>) -> Void)](/documentation/webkit/wkwebview/createpdf(configuration:completionhandler:))
- [func pdf(configuration: WKPDFConfiguration) async throws -> Data](/documentation/webkit/wkwebview/pdf(configuration:))
- [func createWebArchiveData(completionHandler: (Result<Data, any Error>) -> Void)](/documentation/webkit/wkwebview/createwebarchivedata(completionhandler:))
- [func printOperation(with: NSPrintInfo) -> NSPrintOperation](/documentation/webkit/wkwebview/printoperation(with:))
- [WKSnapshotConfiguration](/documentation/webkit/wksnapshotconfiguration)

##### Specifying the snapshot dimensions

- [var rect: CGRect](/documentation/webkit/wksnapshotconfiguration/rect)
- [var snapshotWidth: NSNumber?](/documentation/webkit/wksnapshotconfiguration/snapshotwidth)

##### Configuring the capture behavior

- [var afterScreenUpdates: Bool](/documentation/webkit/wksnapshotconfiguration/afterscreenupdates)
- [WKPDFConfiguration](/documentation/webkit/wkpdfconfiguration)

##### Specifying the snapshot dimensions

- [var rect: CGRect?](/documentation/webkit/wkpdfconfiguration/rect-2a0vp)

##### Specifying snapshot properties

- [var allowTransparentBackground: Bool](/documentation/webkit/wkpdfconfiguration/allowtransparentbackground)

#### Supporting Find and Replace

- [var isFindInteractionEnabled: Bool](/documentation/webkit/wkwebview/isfindinteractionenabled)
- [var findInteraction: UIFindInteraction?](/documentation/webkit/wkwebview/findinteraction)

#### Handling full-screen transitions

- [var fullscreenState: WKWebView.FullscreenState](/documentation/webkit/wkwebview/fullscreenstate-swift.property)
- [WKWebView.FullscreenState](/documentation/webkit/wkwebview/fullscreenstate-swift.enum)

##### Constants

- [case enteringFullscreen](/documentation/webkit/wkwebview/fullscreenstate-swift.enum/enteringfullscreen)
- [case exitingFullscreen](/documentation/webkit/wkwebview/fullscreenstate-swift.enum/exitingfullscreen)
- [case inFullscreen](/documentation/webkit/wkwebview/fullscreenstate-swift.enum/infullscreen)
- [case notInFullscreen](/documentation/webkit/wkwebview/fullscreenstate-swift.enum/notinfullscreen)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkwebview/fullscreenstate-swift.enum/init(rawvalue:))

#### Configuring viewport insets

- [func setMinimumViewportInset(UIEdgeInsets, maximumViewportInset: UIEdgeInsets)](/documentation/webkit/wkwebview/setminimumviewportinset(_:maximumviewportinset:))
- [var minimumViewportInset: UIEdgeInsets](/documentation/webkit/wkwebview/minimumviewportinset)
- [var maximumViewportInset: UIEdgeInsets](/documentation/webkit/wkwebview/maximumviewportinset)

#### Examining data types

- [WKWebViewDataType](/documentation/webkit/wkwebviewdatatype)

##### Initializers

- [init(rawValue: UInt)](/documentation/webkit/wkwebviewdatatype/init(rawvalue:))

##### Type Properties

- [static var sessionStorage: WKWebViewDataType](/documentation/webkit/wkwebviewdatatype/sessionstorage)

#### Deprecated

- [Deprecated symbols](/documentation/webkit/wkwebview-deprecated-symbols)

##### Deprecated

- [var certificateChain: [Any]](/documentation/webkit/wkwebview/certificatechain)
- [func closeAllMediaPresentations()](/documentation/webkit/wkwebview/closeallmediapresentations())
- [func loadSimulatedRequest(URLRequest, with: URLResponse, responseData: Data) -> WKNavigation](/documentation/webkit/wkwebview/loadsimulatedrequest(_:with:responsedata:))
- [func loadSimulatedRequest(URLRequest, withResponseHTML: String) -> WKNavigation](/documentation/webkit/wkwebview/loadsimulatedrequest(_:withresponsehtml:))

#### Instance Properties

- [var isBlockedByScreenTime: Bool](/documentation/webkit/wkwebview/isblockedbyscreentime)
- [var isWritingToolsActive: Bool](/documentation/webkit/wkwebview/iswritingtoolsactive)
- [var obscuredContentInsets: UIEdgeInsets](/documentation/webkit/wkwebview/obscuredcontentinsets)

#### Instance Methods

- [func fetchData(of: WKWebViewDataType, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/webkit/wkwebview/fetchdata(of:completionhandler:))
- [func restoreData(Data, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebview/restoredata(_:completionhandler:))
- [WKUIDelegate](/documentation/webkit/wkuidelegate)

#### Creating and closing the web view

- [func webView(WKWebView, createWebViewWith: WKWebViewConfiguration, for: WKNavigationAction, windowFeatures: WKWindowFeatures) -> WKWebView?](/documentation/webkit/wkuidelegate/webview(_:createwebviewwith:for:windowfeatures:))
- [func webViewDidClose(WKWebView)](/documentation/webkit/wkuidelegate/webviewdidclose(_:))

#### Displaying UI panels

- [func webView(WKWebView, runJavaScriptAlertPanelWithMessage: String, initiatedByFrame: WKFrameInfo, completionHandler: () -> Void)](/documentation/webkit/wkuidelegate/webview(_:runjavascriptalertpanelwithmessage:initiatedbyframe:completionhandler:))
- [func webView(WKWebView, runJavaScriptConfirmPanelWithMessage: String, initiatedByFrame: WKFrameInfo, completionHandler: (Bool) -> Void)](/documentation/webkit/wkuidelegate/webview(_:runjavascriptconfirmpanelwithmessage:initiatedbyframe:completionhandler:))
- [func webView(WKWebView, runJavaScriptTextInputPanelWithPrompt: String, defaultText: String?, initiatedByFrame: WKFrameInfo, completionHandler: (String?) -> Void)](/documentation/webkit/wkuidelegate/webview(_:runjavascripttextinputpanelwithprompt:defaulttext:initiatedbyframe:completionhandler:))
- [func webView(WKWebView, showLockdownModeFirstUseMessage: String, completionHandler: (WKDialogResult) -> Void)](/documentation/webkit/wkuidelegate/webview(_:showlockdownmodefirstusemessage:completionhandler:))
- [WKDialogResult](/documentation/webkit/wkdialogresult)

##### First use dialog results

- [case askAgain](/documentation/webkit/wkdialogresult/askagain)
- [case handled](/documentation/webkit/wkdialogresult/handled)
- [case showDefault](/documentation/webkit/wkdialogresult/showdefault)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkdialogresult/init(rawvalue:))

#### Displaying an upload panel

- [func webView(WKWebView, runOpenPanelWith: WKOpenPanelParameters, initiatedByFrame: WKFrameInfo, completionHandler: ([URL]?) -> Void)](/documentation/webkit/wkuidelegate/webview(_:runopenpanelwith:initiatedbyframe:completionhandler:))
- [WKOpenPanelParameters](/documentation/webkit/wkopenpanelparameters)

##### Configuring the panel parameters

- [var allowsMultipleSelection: Bool](/documentation/webkit/wkopenpanelparameters/allowsmultipleselection)
- [var allowsDirectories: Bool](/documentation/webkit/wkopenpanelparameters/allowsdirectories)

#### Displaying a contextual menu

- [Adding context menus in your app](/documentation/uikit/adding-context-menus-in-your-app)
- [func webView(WKWebView, contextMenuConfigurationForElement: WKContextMenuElementInfo, completionHandler: (UIContextMenuConfiguration?) -> Void)](/documentation/webkit/wkuidelegate/webview(_:contextmenuconfigurationforelement:completionhandler:))
- [func webView(WKWebView, contextMenuForElement: WKContextMenuElementInfo, willCommitWithAnimator: any UIContextMenuInteractionCommitAnimating)](/documentation/webkit/wkuidelegate/webview(_:contextmenuforelement:willcommitwithanimator:))
- [func webView(WKWebView, contextMenuWillPresentForElement: WKContextMenuElementInfo)](/documentation/webkit/wkuidelegate/webview(_:contextmenuwillpresentforelement:))
- [func webView(WKWebView, contextMenuDidEndForElement: WKContextMenuElementInfo)](/documentation/webkit/wkuidelegate/webview(_:contextmenudidendforelement:))
- [UIContextMenuConfiguration](/documentation/uikit/uicontextmenuconfiguration)

#### Displaying an edit menu

- [func webView(WKWebView, willDismissEditMenuWithAnimator: any UIEditMenuInteractionAnimating)](/documentation/webkit/wkuidelegate/webview(_:willdismisseditmenuwithanimator:))
- [func webView(WKWebView, willPresentEditMenuWithAnimator: any UIEditMenuInteractionAnimating)](/documentation/webkit/wkuidelegate/webview(_:willpresenteditmenuwithanimator:))

#### Requesting permissions

- [func webView(WKWebView, requestDeviceOrientationAndMotionPermissionFor: WKSecurityOrigin, initiatedByFrame: WKFrameInfo, decisionHandler: (WKPermissionDecision) -> Void)](/documentation/webkit/wkuidelegate/webview(_:requestdeviceorientationandmotionpermissionfor:initiatedbyframe:decisionhandler:))
- [func webView(WKWebView, requestMediaCapturePermissionFor: WKSecurityOrigin, initiatedByFrame: WKFrameInfo, type: WKMediaCaptureType, decisionHandler: (WKPermissionDecision) -> Void)](/documentation/webkit/wkuidelegate/webview(_:requestmediacapturepermissionfor:initiatedbyframe:type:decisionhandler:))
- [WKPermissionDecision](/documentation/webkit/wkpermissiondecision)

##### Constants

- [case deny](/documentation/webkit/wkpermissiondecision/deny)
- [case grant](/documentation/webkit/wkpermissiondecision/grant)
- [case prompt](/documentation/webkit/wkpermissiondecision/prompt)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkpermissiondecision/init(rawvalue:))
- [WKMediaCaptureType](/documentation/webkit/wkmediacapturetype)

##### Constants

- [case camera](/documentation/webkit/wkmediacapturetype/camera)
- [case cameraAndMicrophone](/documentation/webkit/wkmediacapturetype/cameraandmicrophone)
- [case microphone](/documentation/webkit/wkmediacapturetype/microphone)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkmediacapturetype/init(rawvalue:))

#### Deprecated

- [Deprecated symbols](/documentation/webkit/wkuidelegate-deprecated-symbols)

##### Responding to Force Touch actions

- [func webView(WKWebView, shouldPreviewElement: WKPreviewElementInfo) -> Bool](/documentation/webkit/wkuidelegate/webview(_:shouldpreviewelement:))
- [func webView(WKWebView, previewingViewControllerForElement: WKPreviewElementInfo, defaultActions: [any WKPreviewActionItem]) -> UIViewController?](/documentation/webkit/wkuidelegate/webview(_:previewingviewcontrollerforelement:defaultactions:))
- [func webView(WKWebView, commitPreviewingViewController: UIViewController)](/documentation/webkit/wkuidelegate/webview(_:commitpreviewingviewcontroller:))

### Web view configuration

- [WKWebViewConfiguration](/documentation/webkit/wkwebviewconfiguration)

#### Configuring the web view’s behavior

- [var websiteDataStore: WKWebsiteDataStore](/documentation/webkit/wkwebviewconfiguration/websitedatastore)
- [var userContentController: WKUserContentController](/documentation/webkit/wkwebviewconfiguration/usercontentcontroller)
- [var processPool: WKProcessPool](/documentation/webkit/wkwebviewconfiguration/processpool)
- [var applicationNameForUserAgent: String?](/documentation/webkit/wkwebviewconfiguration/applicationnameforuseragent)
- [var limitsNavigationsToAppBoundDomains: Bool](/documentation/webkit/wkwebviewconfiguration/limitsnavigationstoappbounddomains)
- [var upgradeKnownHostsToHTTPS: Bool](/documentation/webkit/wkwebviewconfiguration/upgradeknownhoststohttps)

#### Configuring the web view’s preferences

- [var preferences: WKPreferences](/documentation/webkit/wkwebviewconfiguration/preferences)
- [var defaultWebpagePreferences: WKWebpagePreferences!](/documentation/webkit/wkwebviewconfiguration/defaultwebpagepreferences)

#### Adding handlers for custom URL schemes

- [func setURLSchemeHandler((any WKURLSchemeHandler)?, forURLScheme: String)](/documentation/webkit/wkwebviewconfiguration/seturlschemehandler(_:forurlscheme:))
- [func urlSchemeHandler(forURLScheme: String) -> (any WKURLSchemeHandler)?](/documentation/webkit/wkwebviewconfiguration/urlschemehandler(forurlscheme:))

#### Configuring the rendering behavior

- [var ignoresViewportScaleLimits: Bool](/documentation/webkit/wkwebviewconfiguration/ignoresviewportscalelimits)
- [var suppressesIncrementalRendering: Bool](/documentation/webkit/wkwebviewconfiguration/suppressesincrementalrendering)

#### Setting media playback preferences

- [var allowsInlineMediaPlayback: Bool](/documentation/webkit/wkwebviewconfiguration/allowsinlinemediaplayback)
- [var allowsAirPlayForMediaPlayback: Bool](/documentation/webkit/wkwebviewconfiguration/allowsairplayformediaplayback)
- [var allowsPictureInPictureMediaPlayback: Bool](/documentation/webkit/wkwebviewconfiguration/allowspictureinpicturemediaplayback)
- [var mediaTypesRequiringUserActionForPlayback: WKAudiovisualMediaTypes](/documentation/webkit/wkwebviewconfiguration/mediatypesrequiringuseractionforplayback)
- [WKAudiovisualMediaTypes](/documentation/webkit/wkaudiovisualmediatypes)

##### Media Types

- [static var audio: WKAudiovisualMediaTypes](/documentation/webkit/wkaudiovisualmediatypes/audio)
- [static var video: WKAudiovisualMediaTypes](/documentation/webkit/wkaudiovisualmediatypes/video)
- [static var all: WKAudiovisualMediaTypes](/documentation/webkit/wkaudiovisualmediatypes/all)

##### Initializers

- [init(rawValue: UInt)](/documentation/webkit/wkaudiovisualmediatypes/init(rawvalue:))

#### Identifying data types

- [var dataDetectorTypes: WKDataDetectorTypes](/documentation/webkit/wkwebviewconfiguration/datadetectortypes)
- [WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes)

##### Data Detector Types

- [static var phoneNumber: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/phonenumber)
- [static var link: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/link)
- [static var address: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/address)
- [static var calendarEvent: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/calendarevent)
- [static var trackingNumber: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/trackingnumber)
- [static var flightNumber: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/flightnumber)
- [static var lookupSuggestion: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/lookupsuggestion)
- [static var all: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/all)

##### Initializers

- [init(rawValue: UInt)](/documentation/webkit/wkdatadetectortypes/init(rawvalue:))

##### Deprecated Types

- [static var spotlightSuggestion: WKDataDetectorTypes](/documentation/webkit/wkdatadetectortypes/spotlightsuggestion)

#### Setting selection granularity

- [var selectionGranularity: WKSelectionGranularity](/documentation/webkit/wkwebviewconfiguration/selectiongranularity)
- [WKSelectionGranularity](/documentation/webkit/wkselectiongranularity)

##### Getting the Granularity Options

- [case dynamic](/documentation/webkit/wkselectiongranularity/dynamic)
- [case character](/documentation/webkit/wkselectiongranularity/character)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkselectiongranularity/init(rawvalue:))

#### Selecting user interface directionality

- [var userInterfaceDirectionPolicy: WKUserInterfaceDirectionPolicy](/documentation/webkit/wkwebviewconfiguration/userinterfacedirectionpolicy)
- [WKUserInterfaceDirectionPolicy](/documentation/webkit/wkuserinterfacedirectionpolicy)

##### Direction Policies

- [case content](/documentation/webkit/wkuserinterfacedirectionpolicy/content)
- [case system](/documentation/webkit/wkuserinterfacedirectionpolicy/system)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkuserinterfacedirectionpolicy/init(rawvalue:))

#### Deprecated

- [var mediaPlaybackAllowsAirPlay: Bool](/documentation/webkit/wkwebviewconfiguration/mediaplaybackallowsairplay)
- [var requiresUserActionForMediaPlayback: Bool](/documentation/webkit/wkwebviewconfiguration/requiresuseractionformediaplayback)
- [var mediaPlaybackRequiresUserAction: Bool](/documentation/webkit/wkwebviewconfiguration/mediaplaybackrequiresuseraction)

#### Instance Properties

- [var allowsInlinePredictions: Bool](/documentation/webkit/wkwebviewconfiguration/allowsinlinepredictions)
- [var showsSystemScreenTimeBlockingView: Bool](/documentation/webkit/wkwebviewconfiguration/showssystemscreentimeblockingview)
- [var supportsAdaptiveImageGlyph: Bool](/documentation/webkit/wkwebviewconfiguration/supportsadaptiveimageglyph)
- [var webExtensionController: WKWebExtensionController?](/documentation/webkit/wkwebviewconfiguration/webextensioncontroller)
- [var writingToolsBehavior: UIWritingToolsBehavior](/documentation/webkit/wkwebviewconfiguration/writingtoolsbehavior)
- [WKWindowFeatures](/documentation/webkit/wkwindowfeatures)

#### Inspecting Window Position and Dimensions

- [var allowsResizing: NSNumber?](/documentation/webkit/wkwindowfeatures/allowsresizing)
- [var height: NSNumber?](/documentation/webkit/wkwindowfeatures/height)
- [var width: NSNumber?](/documentation/webkit/wkwindowfeatures/width)
- [var x: NSNumber?](/documentation/webkit/wkwindowfeatures/x)
- [var y: NSNumber?](/documentation/webkit/wkwindowfeatures/y)

#### Inspecting Visibility Properties

- [var menuBarVisibility: NSNumber?](/documentation/webkit/wkwindowfeatures/menubarvisibility)
- [var statusBarVisibility: NSNumber?](/documentation/webkit/wkwindowfeatures/statusbarvisibility)
- [var toolbarsVisibility: NSNumber?](/documentation/webkit/wkwindowfeatures/toolbarsvisibility)
- [WKProcessPool](/documentation/webkit/wkprocesspool)
- [WKPreferences](/documentation/webkit/wkpreferences)

#### Setting Rendering Preferences

- [var minimumFontSize: CGFloat](/documentation/webkit/wkpreferences/minimumfontsize)
- [var shouldPrintBackgrounds: Bool](/documentation/webkit/wkpreferences/shouldprintbackgrounds)

#### Setting Behavior Preferences

- [var tabFocusesLinks: Bool](/documentation/webkit/wkpreferences/tabfocuseslinks)
- [var isTextInteractionEnabled: Bool](/documentation/webkit/wkpreferences/istextinteractionenabled)
- [var isElementFullscreenEnabled: Bool](/documentation/webkit/wkpreferences/iselementfullscreenenabled)
- [var inactiveSchedulingPolicy: WKPreferences.InactiveSchedulingPolicy](/documentation/webkit/wkpreferences/inactiveschedulingpolicy-swift.property)
- [WKPreferences.InactiveSchedulingPolicy](/documentation/webkit/wkpreferences/inactiveschedulingpolicy-swift.enum)

##### Scheduling policies

- [case none](/documentation/webkit/wkpreferences/inactiveschedulingpolicy-swift.enum/none)
- [case suspend](/documentation/webkit/wkpreferences/inactiveschedulingpolicy-swift.enum/suspend)
- [case throttle](/documentation/webkit/wkpreferences/inactiveschedulingpolicy-swift.enum/throttle)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkpreferences/inactiveschedulingpolicy-swift.enum/init(rawvalue:))

#### Setting Java and JavaScript Preferences

- [var javaScriptCanOpenWindowsAutomatically: Bool](/documentation/webkit/wkpreferences/javascriptcanopenwindowsautomatically)
- [var isSiteSpecificQuirksModeEnabled: Bool](/documentation/webkit/wkpreferences/issitespecificquirksmodeenabled)

#### Setting Fraud Warning Preferences

- [var isFraudulentWebsiteWarningEnabled: Bool](/documentation/webkit/wkpreferences/isfraudulentwebsitewarningenabled)

#### Deprecated

- [var javaEnabled: Bool](/documentation/webkit/wkpreferences/javaenabled)
- [var javaScriptEnabled: Bool](/documentation/webkit/wkpreferences/javascriptenabled)
- [var plugInsEnabled: Bool](/documentation/webkit/wkpreferences/pluginsenabled)

#### Instance Properties

- [var isLookToScrollEnabled: Bool](/documentation/webkit/wkpreferences/islooktoscrollenabled)
- [WKWebpagePreferences](/documentation/webkit/wkwebpagepreferences)

#### Setting the JavaScript preferences

- [var allowsContentJavaScript: Bool](/documentation/webkit/wkwebpagepreferences/allowscontentjavascript)

#### Setting the preferred content mode

- [var preferredContentMode: WKWebpagePreferences.ContentMode](/documentation/webkit/wkwebpagepreferences/preferredcontentmode)
- [WKWebpagePreferences.ContentMode](/documentation/webkit/wkwebpagepreferences/contentmode)

##### Getting the Content Modes

- [case recommended](/documentation/webkit/wkwebpagepreferences/contentmode/recommended)
- [case desktop](/documentation/webkit/wkwebpagepreferences/contentmode/desktop)
- [case mobile](/documentation/webkit/wkwebpagepreferences/contentmode/mobile)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkwebpagepreferences/contentmode/init(rawvalue:))

#### Getting Lockdown Mode info

- [var isLockdownModeEnabled: Bool](/documentation/webkit/wkwebpagepreferences/islockdownmodeenabled)

#### Instance Properties

- [var preferredHTTPSNavigationPolicy: WKWebpagePreferences.UpgradeToHTTPSPolicy](/documentation/webkit/wkwebpagepreferences/preferredhttpsnavigationpolicy)

#### Enumerations

- [WKWebpagePreferences.UpgradeToHTTPSPolicy](/documentation/webkit/wkwebpagepreferences/upgradetohttpspolicy)

##### Enumeration Cases

- [case automaticFallbackToHTTP](/documentation/webkit/wkwebpagepreferences/upgradetohttpspolicy/automaticfallbacktohttp)
- [case errorOnFailure](/documentation/webkit/wkwebpagepreferences/upgradetohttpspolicy/erroronfailure)
- [case keepAsRequested](/documentation/webkit/wkwebpagepreferences/upgradetohttpspolicy/keepasrequested)
- [case userMediatedFallbackToHTTP](/documentation/webkit/wkwebpagepreferences/upgradetohttpspolicy/usermediatedfallbacktohttp)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkwebpagepreferences/upgradetohttpspolicy/init(rawvalue:))

### Web data management

- [WKWebsiteDataStore](/documentation/webkit/wkwebsitedatastore)

#### Creating a data store object

- [class func `default`() -> WKWebsiteDataStore](/documentation/webkit/wkwebsitedatastore/default())
- [class func nonPersistent() -> WKWebsiteDataStore](/documentation/webkit/wkwebsitedatastore/nonpersistent())
- [init(forIdentifier: UUID)](/documentation/webkit/wkwebsitedatastore/init(foridentifier:))

#### Finding data stores

- [class func fetchAllDataStoreIdentifiers(([UUID]) -> Void)](/documentation/webkit/wkwebsitedatastore/fetchalldatastoreidentifiers(_:))

#### Inspecting data store properties

- [var identifier: UUID?](/documentation/webkit/wkwebsitedatastore/identifier)
- [var isPersistent: Bool](/documentation/webkit/wkwebsitedatastore/ispersistent)

#### Retrieving a cookie store

- [var httpCookieStore: WKHTTPCookieStore](/documentation/webkit/wkwebsitedatastore/httpcookiestore)

#### Retrieving specific types of data

- [func fetchDataRecords(ofTypes: Set<String>, completionHandler: ([WKWebsiteDataRecord]) -> Void)](/documentation/webkit/wkwebsitedatastore/fetchdatarecords(oftypes:completionhandler:))
- [class func allWebsiteDataTypes() -> Set<String>](/documentation/webkit/wkwebsitedatastore/allwebsitedatatypes())

#### Removing specific types of data

- [func removeData(ofTypes: Set<String>, for: [WKWebsiteDataRecord], completionHandler: () -> Void)](/documentation/webkit/wkwebsitedatastore/removedata(oftypes:for:completionhandler:))
- [func removeData(ofTypes: Set<String>, modifiedSince: Date, completionHandler: () -> Void)](/documentation/webkit/wkwebsitedatastore/removedata(oftypes:modifiedsince:completionhandler:))

#### Removing a data store

- [class func remove(forIdentifier: UUID, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebsitedatastore/remove(foridentifier:completionhandler:))

#### Instance Properties

- [var proxyConfigurations: [ProxyConfiguration]](/documentation/webkit/wkwebsitedatastore/proxyconfigurations-cdc1)

#### Instance Methods

- [func fetchData(of: Set<String>, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/webkit/wkwebsitedatastore/fetchdata(of:completionhandler:))
- [func restoreData(Data, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebsitedatastore/restoredata(_:completionhandler:))
- [WKWebsiteDataRecord](/documentation/webkit/wkwebsitedatarecord)

#### Getting the Record Information

- [var displayName: String](/documentation/webkit/wkwebsitedatarecord/displayname)

#### Getting the Data Type

- [var dataTypes: Set<String>](/documentation/webkit/wkwebsitedatarecord/datatypes)
- [Data Store Record Types](/documentation/webkit/data-store-record-types)

##### Cookie type

- [let WKWebsiteDataTypeCookies: String](/documentation/webkit/wkwebsitedatatypecookies)

##### Cache types

- [let WKWebsiteDataTypeMemoryCache: String](/documentation/webkit/wkwebsitedatatypememorycache)
- [let WKWebsiteDataTypeDiskCache: String](/documentation/webkit/wkwebsitedatatypediskcache)
- [let WKWebsiteDataTypeOfflineWebApplicationCache: String](/documentation/webkit/wkwebsitedatatypeofflinewebapplicationcache)

##### Storage types

- [let WKWebsiteDataTypeLocalStorage: String](/documentation/webkit/wkwebsitedatatypelocalstorage)
- [let WKWebsiteDataTypeSessionStorage: String](/documentation/webkit/wkwebsitedatatypesessionstorage)

##### Database types

- [let WKWebsiteDataTypeWebSQLDatabases: String](/documentation/webkit/wkwebsitedatatypewebsqldatabases)
- [let WKWebsiteDataTypeIndexedDBDatabases: String](/documentation/webkit/wkwebsitedatatypeindexeddbdatabases)

##### Screen time type

- [let WKWebsiteDataTypeScreenTime: String](/documentation/webkit/wkwebsitedatatypescreentime)
- [WKHTTPCookieStore](/documentation/webkit/wkhttpcookiestore)

#### Managing cookies

- [func getAllCookies(([HTTPCookie]) -> Void)](/documentation/webkit/wkhttpcookiestore/getallcookies(_:))
- [func setCookie(HTTPCookie, completionHandler: (() -> Void)?)](/documentation/webkit/wkhttpcookiestore/setcookie(_:completionhandler:))
- [func delete(HTTPCookie, completionHandler: (() -> Void)?)](/documentation/webkit/wkhttpcookiestore/delete(_:completionhandler:))

#### Permitting cookie storage

- [func getCookiePolicy((WKHTTPCookieStore.CookiePolicy) -> Void)](/documentation/webkit/wkhttpcookiestore/getcookiepolicy(_:))
- [func setCookiePolicy(WKHTTPCookieStore.CookiePolicy, completionHandler: (() -> Void)?)](/documentation/webkit/wkhttpcookiestore/setcookiepolicy(_:completionhandler:))
- [WKHTTPCookieStore.CookiePolicy](/documentation/webkit/wkhttpcookiestore/cookiepolicy)

##### Specifying a cookie policy

- [case allow](/documentation/webkit/wkhttpcookiestore/cookiepolicy/allow)
- [case disallow](/documentation/webkit/wkhttpcookiestore/cookiepolicy/disallow)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkhttpcookiestore/cookiepolicy/init(rawvalue:))

#### Observing cookie store changes

- [func add(any WKHTTPCookieStoreObserver)](/documentation/webkit/wkhttpcookiestore/add(_:))
- [func remove(any WKHTTPCookieStoreObserver)](/documentation/webkit/wkhttpcookiestore/remove(_:))
- [WKHTTPCookieStoreObserver](/documentation/webkit/wkhttpcookiestoreobserver)

##### Responding to Cookie Changes

- [func cookiesDidChange(in: WKHTTPCookieStore)](/documentation/webkit/wkhttpcookiestoreobserver/cookiesdidchange(in:))

#### Instance Methods

- [func setCookies([HTTPCookie], completionHandler: (() -> Void)?)](/documentation/webkit/wkhttpcookiestore/setcookies(_:completionhandler:))
- [WKURLSchemeHandler](/documentation/webkit/wkurlschemehandler)

#### Loading a Custom Resource

- [func webView(WKWebView, start: any WKURLSchemeTask)](/documentation/webkit/wkurlschemehandler/webview(_:start:))

#### Responding to a Canceled Resource Request

- [func webView(WKWebView, stop: any WKURLSchemeTask)](/documentation/webkit/wkurlschemehandler/webview(_:stop:))
- [WKURLSchemeTask](/documentation/webkit/wkurlschemetask)

#### Getting the URL of the Requested Resource

- [var request: URLRequest](/documentation/webkit/wkurlschemetask/request)

#### Reporting Progress Back to WebKit

- [func didReceive(URLResponse)](/documentation/webkit/wkurlschemetask/didreceive(_:)-2u23r)
- [func didReceive(Data)](/documentation/webkit/wkurlschemetask/didreceive(_:)-8t5f8)
- [func didFinish()](/documentation/webkit/wkurlschemetask/didfinish())

#### Reporting an Error to WebKit

- [func didFailWithError(any Error)](/documentation/webkit/wkurlschemetask/didfailwitherror(_:))
- [static let readAccessURL: NSAttributedString.DocumentReadingOptionKey](/documentation/foundation/nsattributedstring/documentreadingoptionkey/readaccessurl)

### Navigation

- [WKNavigationDelegate](/documentation/webkit/wknavigationdelegate)

#### Allowing or denying navigation requests

- [func webView(WKWebView, decidePolicyFor: WKNavigationAction, preferences: WKWebpagePreferences, decisionHandler: (WKNavigationActionPolicy, WKWebpagePreferences) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:decidepolicyfor:preferences:decisionhandler:))
- [func webView(WKWebView, decidePolicyFor: WKNavigationAction, decisionHandler: (WKNavigationActionPolicy) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:decidepolicyfor:decisionhandler:)-2ni62)
- [WKNavigationActionPolicy](/documentation/webkit/wknavigationactionpolicy)

##### Constants

- [case cancel](/documentation/webkit/wknavigationactionpolicy/cancel)
- [case allow](/documentation/webkit/wknavigationactionpolicy/allow)
- [case download](/documentation/webkit/wknavigationactionpolicy/download)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wknavigationactionpolicy/init(rawvalue:))
- [func webView(WKWebView, decidePolicyFor: WKNavigationResponse, decisionHandler: (WKNavigationResponsePolicy) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:decidepolicyfor:decisionhandler:)-19mn2)
- [WKNavigationResponsePolicy](/documentation/webkit/wknavigationresponsepolicy)

##### Constants

- [case cancel](/documentation/webkit/wknavigationresponsepolicy/cancel)
- [case allow](/documentation/webkit/wknavigationresponsepolicy/allow)
- [case download](/documentation/webkit/wknavigationresponsepolicy/download)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wknavigationresponsepolicy/init(rawvalue:))

#### Tracking the load progress of a request

- [func webView(WKWebView, didStartProvisionalNavigation: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didstartprovisionalnavigation:))
- [func webView(WKWebView, didReceiveServerRedirectForProvisionalNavigation: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didreceiveserverredirectforprovisionalnavigation:))
- [func webView(WKWebView, didCommit: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didcommit:))
- [func webView(WKWebView, didFinish: WKNavigation!)](/documentation/webkit/wknavigationdelegate/webview(_:didfinish:))

#### Responding to authentication challenges

- [func webView(WKWebView, didReceive: URLAuthenticationChallenge, completionHandler: (URLSession.AuthChallengeDisposition, URLCredential?) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:didreceive:completionhandler:))
- [func webView(WKWebView, authenticationChallenge: URLAuthenticationChallenge, shouldAllowDeprecatedTLS: (Bool) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:authenticationchallenge:shouldallowdeprecatedtls:))

#### Responding to navigation errors

- [func webView(WKWebView, didFail: WKNavigation!, withError: any Error)](/documentation/webkit/wknavigationdelegate/webview(_:didfail:witherror:))
- [func webView(WKWebView, didFailProvisionalNavigation: WKNavigation!, withError: any Error)](/documentation/webkit/wknavigationdelegate/webview(_:didfailprovisionalnavigation:witherror:))
- [func webViewWebContentProcessDidTerminate(WKWebView)](/documentation/webkit/wknavigationdelegate/webviewwebcontentprocessdidterminate(_:))

#### Handling download progress

- [func webView(WKWebView, navigationResponse: WKNavigationResponse, didBecome: WKDownload)](/documentation/webkit/wknavigationdelegate/webview(_:navigationresponse:didbecome:))
- [func webView(WKWebView, navigationAction: WKNavigationAction, didBecome: WKDownload)](/documentation/webkit/wknavigationdelegate/webview(_:navigationaction:didbecome:))

#### Instance Methods

- [func webView(WKWebView, shouldGoTo: WKBackForwardListItem, willUseInstantBack: Bool, completionHandler: (Bool) -> Void)](/documentation/webkit/wknavigationdelegate/webview(_:shouldgoto:willuseinstantback:completionhandler:))
- [WKBackForwardList](/documentation/webkit/wkbackforwardlist)

#### Getting the Most Recent Items

- [var backItem: WKBackForwardListItem?](/documentation/webkit/wkbackforwardlist/backitem)
- [var currentItem: WKBackForwardListItem?](/documentation/webkit/wkbackforwardlist/currentitem)
- [var forwardItem: WKBackForwardListItem?](/documentation/webkit/wkbackforwardlist/forwarditem)

#### Getting Specific Items in the List

- [func item(at: Int) -> WKBackForwardListItem?](/documentation/webkit/wkbackforwardlist/item(at:))

#### Getting Sublists

- [var backList: [WKBackForwardListItem]](/documentation/webkit/wkbackforwardlist/backlist)
- [var forwardList: [WKBackForwardListItem]](/documentation/webkit/wkbackforwardlist/forwardlist)
- [WKBackForwardListItem](/documentation/webkit/wkbackforwardlistitem)

#### Getting the Page-Specific Information

- [var title: String?](/documentation/webkit/wkbackforwardlistitem/title)
- [var url: URL](/documentation/webkit/wkbackforwardlistitem/url)

#### Getting the Requesting Page

- [var initialURL: URL](/documentation/webkit/wkbackforwardlistitem/initialurl)
- [WKNavigation](/documentation/webkit/wknavigation)

#### Getting the Content Mode

- [var effectiveContentMode: WKWebpagePreferences.ContentMode](/documentation/webkit/wknavigation/effectivecontentmode)
- [WKNavigationAction](/documentation/webkit/wknavigationaction)

#### Getting the navigation type

- [var navigationType: WKNavigationType](/documentation/webkit/wknavigationaction/navigationtype)
- [WKNavigationType](/documentation/webkit/wknavigationtype)

##### Getting the Navigation Types

- [case linkActivated](/documentation/webkit/wknavigationtype/linkactivated)
- [case formSubmitted](/documentation/webkit/wknavigationtype/formsubmitted)
- [case backForward](/documentation/webkit/wknavigationtype/backforward)
- [case reload](/documentation/webkit/wknavigationtype/reload)
- [case formResubmitted](/documentation/webkit/wknavigationtype/formresubmitted)
- [case other](/documentation/webkit/wknavigationtype/other)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wknavigationtype/init(rawvalue:))

#### Inspecting navigation information

- [var request: URLRequest](/documentation/webkit/wknavigationaction/request)
- [var sourceFrame: WKFrameInfo](/documentation/webkit/wknavigationaction/sourceframe)
- [var targetFrame: WKFrameInfo?](/documentation/webkit/wknavigationaction/targetframe)
- [var shouldPerformDownload: Bool](/documentation/webkit/wknavigationaction/shouldperformdownload)

#### Inspecting user actions

- [var buttonNumber: UIEvent.ButtonMask](/documentation/webkit/wknavigationaction/buttonnumber)
- [var modifierFlags: UIKeyModifierFlags](/documentation/webkit/wknavigationaction/modifierflags)

#### Instance Properties

- [var isContentRuleListRedirect: Bool](/documentation/webkit/wknavigationaction/iscontentrulelistredirect)
- [WKNavigationResponse](/documentation/webkit/wknavigationresponse)

#### Getting the Response Details

- [var response: URLResponse](/documentation/webkit/wknavigationresponse/response)

#### Getting Additional Response Information

- [var canShowMIMEType: Bool](/documentation/webkit/wknavigationresponse/canshowmimetype)
- [var isForMainFrame: Bool](/documentation/webkit/wknavigationresponse/isformainframe)

### Downloads

- [WKDownload](/documentation/webkit/wkdownload)

#### Managing the download

- [var delegate: (any WKDownloadDelegate)?](/documentation/webkit/wkdownload/delegate)
- [func cancel(((Data?) -> Void)?)](/documentation/webkit/wkdownload/cancel(_:))
- [WKDownload.RedirectPolicy](/documentation/webkit/wkdownload/redirectpolicy)

##### Constants

- [case allow](/documentation/webkit/wkdownload/redirectpolicy/allow)
- [case cancel](/documentation/webkit/wkdownload/redirectpolicy/cancel)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkdownload/redirectpolicy/init(rawvalue:))

#### Inspecting the download

- [var originalRequest: URLRequest?](/documentation/webkit/wkdownload/originalrequest)
- [var webView: WKWebView?](/documentation/webkit/wkdownload/webview)

#### Instance Properties

- [var isUserInitiated: Bool](/documentation/webkit/wkdownload/isuserinitiated)
- [var originatingFrame: WKFrameInfo](/documentation/webkit/wkdownload/originatingframe)

#### Enumerations

- [WKDownload.PlaceholderPolicy](/documentation/webkit/wkdownload/placeholderpolicy)

##### Enumeration Cases

- [case disable](/documentation/webkit/wkdownload/placeholderpolicy/disable)
- [case enable](/documentation/webkit/wkdownload/placeholderpolicy/enable)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkdownload/placeholderpolicy/init(rawvalue:))
- [WKDownloadDelegate](/documentation/webkit/wkdownloaddelegate)

#### Tracking Download Progress

- [func download(WKDownload, decideDestinationUsing: URLResponse, suggestedFilename: String, completionHandler: (URL?) -> Void)](/documentation/webkit/wkdownloaddelegate/download(_:decidedestinationusing:suggestedfilename:completionhandler:))
- [func downloadDidFinish(WKDownload)](/documentation/webkit/wkdownloaddelegate/downloaddidfinish(_:))
- [func download(WKDownload, didFailWithError: any Error, resumeData: Data?)](/documentation/webkit/wkdownloaddelegate/download(_:didfailwitherror:resumedata:))

#### Responding to Authorization Challenges

- [func download(WKDownload, didReceive: URLAuthenticationChallenge, completionHandler: (URLSession.AuthChallengeDisposition, URLCredential?) -> Void)](/documentation/webkit/wkdownloaddelegate/download(_:didreceive:completionhandler:))
- [WKDownload.RedirectPolicy](/documentation/webkit/wkdownload/redirectpolicy)

##### Constants

- [case allow](/documentation/webkit/wkdownload/redirectpolicy/allow)
- [case cancel](/documentation/webkit/wkdownload/redirectpolicy/cancel)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkdownload/redirectpolicy/init(rawvalue:))

#### Responding to Redirects

- [func download(WKDownload, willPerformHTTPRedirection: HTTPURLResponse, newRequest: URLRequest, decisionHandler: (WKDownload.RedirectPolicy) -> Void)](/documentation/webkit/wkdownloaddelegate/download(_:willperformhttpredirection:newrequest:decisionhandler:))
- [WKDownload.RedirectPolicy](/documentation/webkit/wkdownload/redirectpolicy)

##### Constants

- [case allow](/documentation/webkit/wkdownload/redirectpolicy/allow)
- [case cancel](/documentation/webkit/wkdownload/redirectpolicy/cancel)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkdownload/redirectpolicy/init(rawvalue:))

#### Instance Methods

- [func download(WKDownload, decidePlaceholderPolicy: (WKDownload.PlaceholderPolicy, URL?) -> Void)](/documentation/webkit/wkdownloaddelegate/download(_:decideplaceholderpolicy:))
- [func download(WKDownload, didReceiveFinalURL: URL)](/documentation/webkit/wkdownloaddelegate/download(_:didreceivefinalurl:))
- [func download(WKDownload, didReceivePlaceholderURL: URL, completionHandler: () -> Void)](/documentation/webkit/wkdownloaddelegate/download(_:didreceiveplaceholderurl:completionhandler:))

### Page content

- [WKUserContentController](/documentation/webkit/wkusercontentcontroller)

#### Adding and Removing Custom Scripts

- [func addUserScript(WKUserScript)](/documentation/webkit/wkusercontentcontroller/adduserscript(_:))
- [func removeAllUserScripts()](/documentation/webkit/wkusercontentcontroller/removealluserscripts())
- [var userScripts: [WKUserScript]](/documentation/webkit/wkusercontentcontroller/userscripts)

#### Adding and Removing Message Handlers

- [func add(any WKScriptMessageHandler, name: String)](/documentation/webkit/wkusercontentcontroller/add(_:name:))
- [func add(any WKScriptMessageHandler, contentWorld: WKContentWorld, name: String)](/documentation/webkit/wkusercontentcontroller/add(_:contentworld:name:))
- [func addScriptMessageHandler(any WKScriptMessageHandlerWithReply, contentWorld: WKContentWorld, name: String)](/documentation/webkit/wkusercontentcontroller/addscriptmessagehandler(_:contentworld:name:))
- [func removeScriptMessageHandler(forName: String)](/documentation/webkit/wkusercontentcontroller/removescriptmessagehandler(forname:))
- [func removeScriptMessageHandler(forName: String, contentWorld: WKContentWorld)](/documentation/webkit/wkusercontentcontroller/removescriptmessagehandler(forname:contentworld:))
- [func removeAllScriptMessageHandlers(from: WKContentWorld)](/documentation/webkit/wkusercontentcontroller/removeallscriptmessagehandlers(from:))
- [func removeAllScriptMessageHandlers()](/documentation/webkit/wkusercontentcontroller/removeallscriptmessagehandlers())
- [WKScriptMessageHandler](/documentation/webkit/wkscriptmessagehandler)

##### Receiving Messages

- [func userContentController(WKUserContentController, didReceive: WKScriptMessage)](/documentation/webkit/wkscriptmessagehandler/usercontentcontroller(_:didreceive:))
- [WKScriptMessage](/documentation/webkit/wkscriptmessage)

###### Getting the Message Contents

- [var body: Any](/documentation/webkit/wkscriptmessage/body)

###### Getting Message-Related Information

- [var frameInfo: WKFrameInfo](/documentation/webkit/wkscriptmessage/frameinfo)
- [var webView: WKWebView?](/documentation/webkit/wkscriptmessage/webview)
- [var world: WKContentWorld](/documentation/webkit/wkscriptmessage/world)

###### Getting the Message Handler’s Name

- [var name: String](/documentation/webkit/wkscriptmessage/name)
- [WKScriptMessageHandlerWithReply](/documentation/webkit/wkscriptmessagehandlerwithreply)

##### Receiving Messages

- [func userContentController(WKUserContentController, didReceive: WKScriptMessage, replyHandler: (Any?, String?) -> Void)](/documentation/webkit/wkscriptmessagehandlerwithreply/usercontentcontroller(_:didreceive:replyhandler:))
- [WKScriptMessage](/documentation/webkit/wkscriptmessage)

###### Getting the Message Contents

- [var body: Any](/documentation/webkit/wkscriptmessage/body)

###### Getting Message-Related Information

- [var frameInfo: WKFrameInfo](/documentation/webkit/wkscriptmessage/frameinfo)
- [var webView: WKWebView?](/documentation/webkit/wkscriptmessage/webview)
- [var world: WKContentWorld](/documentation/webkit/wkscriptmessage/world)

###### Getting the Message Handler’s Name

- [var name: String](/documentation/webkit/wkscriptmessage/name)

#### Adding and Removing Content Rules

- [func add(WKContentRuleList)](/documentation/webkit/wkusercontentcontroller/add(_:))
- [func remove(WKContentRuleList)](/documentation/webkit/wkusercontentcontroller/remove(_:))
- [func removeAllContentRuleLists()](/documentation/webkit/wkusercontentcontroller/removeallcontentrulelists())
- [WKContentRuleList](/documentation/webkit/wkcontentrulelist)

##### Getting the Rules List Identifier

- [var identifier: String!](/documentation/webkit/wkcontentrulelist/identifier)
- [WKContentRuleListStore](/documentation/webkit/wkcontentruleliststore)

#### Creating a Content Rule List Store

- [class func `default`() -> Self!](/documentation/webkit/wkcontentruleliststore/default())
- [convenience init!(url: URL!)](/documentation/webkit/wkcontentruleliststore/init(url:))

#### Creating and Deleting Content Rule Lists

- [func compileContentRuleList(forIdentifier: String!, encodedContentRuleList: String!, completionHandler: ((WKContentRuleList?, (any Error)?) -> Void)!)](/documentation/webkit/wkcontentruleliststore/compilecontentrulelist(foridentifier:encodedcontentrulelist:completionhandler:))
- [func removeContentRuleList(forIdentifier: String!, completionHandler: (((any Error)?) -> Void)!)](/documentation/webkit/wkcontentruleliststore/removecontentrulelist(foridentifier:completionhandler:))

#### Accessing the Current Rule Lists

- [func getAvailableContentRuleListIdentifiers((([String]?) -> Void)!)](/documentation/webkit/wkcontentruleliststore/getavailablecontentrulelistidentifiers(_:))
- [func lookUpContentRuleList(forIdentifier: String!, completionHandler: ((WKContentRuleList?, (any Error)?) -> Void)!)](/documentation/webkit/wkcontentruleliststore/lookupcontentrulelist(foridentifier:completionhandler:))
- [WKContentWorld](/documentation/webkit/wkcontentworld)

#### Getting the Default Content World

- [class var defaultClient: WKContentWorld](/documentation/webkit/wkcontentworld/defaultclient)

#### Getting the Namespace for the Current Page

- [class var page: WKContentWorld](/documentation/webkit/wkcontentworld/page)

#### Retrieving a Custom Content World

- [class func world(name: String) -> WKContentWorld](/documentation/webkit/wkcontentworld/world(name:))
- [var name: String?](/documentation/webkit/wkcontentworld/name)
- [WKFrameInfo](/documentation/webkit/wkframeinfo)

#### Inspecting frame information

- [var isMainFrame: Bool](/documentation/webkit/wkframeinfo/ismainframe)
- [var request: URLRequest](/documentation/webkit/wkframeinfo/request)
- [var securityOrigin: WKSecurityOrigin](/documentation/webkit/wkframeinfo/securityorigin)
- [var webView: WKWebView?](/documentation/webkit/wkframeinfo/webview)
- [WKSecurityOrigin](/documentation/webkit/wksecurityorigin)

#### Getting the Host Information

- [var host: String](/documentation/webkit/wksecurityorigin/host)
- [var port: Int](/documentation/webkit/wksecurityorigin/port)

#### Getting the Host Protocol

- [var `protocol`: String](/documentation/webkit/wksecurityorigin/protocol)
- [WKUserScript](/documentation/webkit/wkuserscript)

#### Creating a User Script Object

- [init(source: String, injectionTime: WKUserScriptInjectionTime, forMainFrameOnly: Bool)](/documentation/webkit/wkuserscript/init(source:injectiontime:formainframeonly:))
- [init(source: String, injectionTime: WKUserScriptInjectionTime, forMainFrameOnly: Bool, in: WKContentWorld)](/documentation/webkit/wkuserscript/init(source:injectiontime:formainframeonly:in:))

#### Inspecting Script Information

- [var source: String](/documentation/webkit/wkuserscript/source)
- [var injectionTime: WKUserScriptInjectionTime](/documentation/webkit/wkuserscript/injectiontime)
- [WKUserScriptInjectionTime](/documentation/webkit/wkuserscriptinjectiontime)

##### Script-Injection Times

- [case atDocumentStart](/documentation/webkit/wkuserscriptinjectiontime/atdocumentstart)
- [case atDocumentEnd](/documentation/webkit/wkuserscriptinjectiontime/atdocumentend)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkuserscriptinjectiontime/init(rawvalue:))
- [var isForMainFrameOnly: Bool](/documentation/webkit/wkuserscript/isformainframeonly)

### Page-level search

- [WKFindConfiguration](/documentation/webkit/wkfindconfiguration)

#### Configuring the Search Parameters

- [var backwards: Bool](/documentation/webkit/wkfindconfiguration/backwards)
- [var caseSensitive: Bool](/documentation/webkit/wkfindconfiguration/casesensitive)
- [var wraps: Bool](/documentation/webkit/wkfindconfiguration/wraps)
- [WKFindResult](/documentation/webkit/wkfindresult)

#### Getting the Search Result

- [var matchFound: Bool](/documentation/webkit/wkfindresult/matchfound)

### Contextual menus

- [WKContextMenuElementInfo](/documentation/webkit/wkcontextmenuelementinfo)

#### Getting the Element Information

- [var linkURL: URL?](/documentation/webkit/wkcontextmenuelementinfo/linkurl)

### Snapshots

- [WKSnapshotConfiguration](/documentation/webkit/wksnapshotconfiguration)

#### Specifying the snapshot dimensions

- [var rect: CGRect](/documentation/webkit/wksnapshotconfiguration/rect)
- [var snapshotWidth: NSNumber?](/documentation/webkit/wksnapshotconfiguration/snapshotwidth)

#### Configuring the capture behavior

- [var afterScreenUpdates: Bool](/documentation/webkit/wksnapshotconfiguration/afterscreenupdates)
- [WKPDFConfiguration](/documentation/webkit/wkpdfconfiguration)

#### Specifying the snapshot dimensions

- [var rect: CGRect?](/documentation/webkit/wkpdfconfiguration/rect-2a0vp)

#### Specifying snapshot properties

- [var allowTransparentBackground: Bool](/documentation/webkit/wkpdfconfiguration/allowtransparentbackground)

### Web extensions

- [WKWebExtension](/documentation/webkit/wkwebextension)

#### Classes

- [WKWebExtension.Action](/documentation/webkit/wkwebextension/action)

##### Instance Properties

- [var associatedTab: (any WKWebExtensionTab)?](/documentation/webkit/wkwebextension/action/associatedtab)
- [var badgeText: String](/documentation/webkit/wkwebextension/action/badgetext)
- [var hasUnreadBadgeText: Bool](/documentation/webkit/wkwebextension/action/hasunreadbadgetext)
- [var inspectionName: String?](/documentation/webkit/wkwebextension/action/inspectionname)
- [var isEnabled: Bool](/documentation/webkit/wkwebextension/action/isenabled)
- [var label: String](/documentation/webkit/wkwebextension/action/label)
- [var menuItems: [UIMenuElement]](/documentation/webkit/wkwebextension/action/menuitems)
- [var popupPopover: NSPopover?](/documentation/webkit/wkwebextension/action/popuppopover)
- [var popupViewController: UIViewController?](/documentation/webkit/wkwebextension/action/popupviewcontroller)
- [var popupWebView: WKWebView?](/documentation/webkit/wkwebextension/action/popupwebview)
- [var presentsPopup: Bool](/documentation/webkit/wkwebextension/action/presentspopup)
- [var webExtensionContext: WKWebExtensionContext?](/documentation/webkit/wkwebextension/action/webextensioncontext)

##### Instance Methods

- [func closePopup()](/documentation/webkit/wkwebextension/action/closepopup())
- [func icon(for: CGSize) -> UIImage?](/documentation/webkit/wkwebextension/action/icon(for:))
- [WKWebExtension.Command](/documentation/webkit/wkwebextension/command)

##### Instance Properties

- [var activationKey: String?](/documentation/webkit/wkwebextension/command/activationkey)
- [var id: String](/documentation/webkit/wkwebextension/command/id)
- [var keyCommand: UIKeyCommand?](/documentation/webkit/wkwebextension/command/keycommand)
- [var menuItem: UIMenuElement](/documentation/webkit/wkwebextension/command/menuitem)
- [var modifierFlags: UIKeyModifierFlags](/documentation/webkit/wkwebextension/command/modifierflags)
- [var title: String](/documentation/webkit/wkwebextension/command/title)
- [var webExtensionContext: WKWebExtensionContext?](/documentation/webkit/wkwebextension/command/webextensioncontext)
- [WKWebExtension.DataRecord](/documentation/webkit/wkwebextension/datarecord)

##### Structures

- [WKWebExtension.DataRecord.Error](/documentation/webkit/wkwebextension/datarecord/error)

###### Type Properties

- [static var errorDomain: String](/documentation/webkit/wkwebextension/datarecord/error/errordomain)
- [static var localStorageFailed: WKWebExtension.DataRecord.Error.Code](/documentation/webkit/wkwebextension/datarecord/error/localstoragefailed)
- [static var sessionStorageFailed: WKWebExtension.DataRecord.Error.Code](/documentation/webkit/wkwebextension/datarecord/error/sessionstoragefailed)
- [static var synchronizedStorageFailed: WKWebExtension.DataRecord.Error.Code](/documentation/webkit/wkwebextension/datarecord/error/synchronizedstoragefailed)
- [static var unknown: WKWebExtension.DataRecord.Error.Code](/documentation/webkit/wkwebextension/datarecord/error/unknown)

##### Instance Properties

- [var containedDataTypes: Set<WKWebExtension.DataType>](/documentation/webkit/wkwebextension/datarecord/containeddatatypes)
- [var displayName: String](/documentation/webkit/wkwebextension/datarecord/displayname)
- [var errors: [any Error]](/documentation/webkit/wkwebextension/datarecord/errors)
- [var totalSizeInBytes: Int](/documentation/webkit/wkwebextension/datarecord/totalsizeinbytes)
- [var uniqueIdentifier: String](/documentation/webkit/wkwebextension/datarecord/uniqueidentifier)

##### Instance Methods

- [func sizeInBytes(ofTypes: Set<WKWebExtension.DataType>) -> Int](/documentation/webkit/wkwebextension/datarecord/sizeinbytes(oftypes:))
- [WKWebExtension.MatchPattern](/documentation/webkit/wkwebextension/matchpattern)

##### Errors

- [WKWebExtension.MatchPattern.Error](/documentation/webkit/wkwebextension/matchpattern/error)

###### Type Properties

- [static var errorDomain: String](/documentation/webkit/wkwebextension/matchpattern/error/errordomain)
- [static var invalidHost: WKWebExtension.MatchPattern.Error.Code](/documentation/webkit/wkwebextension/matchpattern/error/invalidhost)
- [static var invalidPath: WKWebExtension.MatchPattern.Error.Code](/documentation/webkit/wkwebextension/matchpattern/error/invalidpath)
- [static var invalidScheme: WKWebExtension.MatchPattern.Error.Code](/documentation/webkit/wkwebextension/matchpattern/error/invalidscheme)
- [static var unknown: WKWebExtension.MatchPattern.Error.Code](/documentation/webkit/wkwebextension/matchpattern/error/unknown)
- [WKWebExtension.MatchPattern.Error.Code](/documentation/webkit/wkwebextension/matchpattern/error/code)

###### Enumeration Cases

- [case invalidHost](/documentation/webkit/wkwebextension/matchpattern/error/code/invalidhost)
- [case invalidPath](/documentation/webkit/wkwebextension/matchpattern/error/code/invalidpath)
- [case invalidScheme](/documentation/webkit/wkwebextension/matchpattern/error/code/invalidscheme)
- [case unknown](/documentation/webkit/wkwebextension/matchpattern/error/code/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkwebextension/matchpattern/error/code/init(rawvalue:))
- [class let errorDomain: String](/documentation/webkit/wkwebextension/matchpattern/errordomain)

##### Structures

- [WKWebExtension.MatchPattern.Options](/documentation/webkit/wkwebextension/matchpattern/options)

###### Initializers

- [init(rawValue: UInt)](/documentation/webkit/wkwebextension/matchpattern/options/init(rawvalue:))

###### Type Properties

- [static var ignorePaths: WKWebExtension.MatchPattern.Options](/documentation/webkit/wkwebextension/matchpattern/options/ignorepaths)
- [static var ignoreSchemes: WKWebExtension.MatchPattern.Options](/documentation/webkit/wkwebextension/matchpattern/options/ignoreschemes)
- [static var matchBidirectionally: WKWebExtension.MatchPattern.Options](/documentation/webkit/wkwebextension/matchpattern/options/matchbidirectionally)

##### Initializers

- [init(scheme: String, host: String, path: String) throws](/documentation/webkit/wkwebextension/matchpattern/init(scheme:host:path:))
- [init(string: String) throws](/documentation/webkit/wkwebextension/matchpattern/init(string:))

##### Instance Properties

- [var host: String?](/documentation/webkit/wkwebextension/matchpattern/host)
- [var matchesAllHosts: Bool](/documentation/webkit/wkwebextension/matchpattern/matchesallhosts)
- [var matchesAllURLs: Bool](/documentation/webkit/wkwebextension/matchpattern/matchesallurls)
- [var path: String?](/documentation/webkit/wkwebextension/matchpattern/path)
- [var scheme: String?](/documentation/webkit/wkwebextension/matchpattern/scheme)
- [var string: String](/documentation/webkit/wkwebextension/matchpattern/string)

##### Instance Methods

- [func matches(URL?) -> Bool](/documentation/webkit/wkwebextension/matchpattern/matches(_:)-471rf)
- [func matches(WKWebExtension.MatchPattern?) -> Bool](/documentation/webkit/wkwebextension/matchpattern/matches(_:)-4d84f)
- [func matches(URL?, options: WKWebExtension.MatchPattern.Options) -> Bool](/documentation/webkit/wkwebextension/matchpattern/matches(_:options:)-5wo3g)
- [func matches(WKWebExtension.MatchPattern?, options: WKWebExtension.MatchPattern.Options) -> Bool](/documentation/webkit/wkwebextension/matchpattern/matches(_:options:)-fnde)

##### Type Methods

- [class func allHostsAndSchemes() -> Self](/documentation/webkit/wkwebextension/matchpattern/allhostsandschemes())
- [class func allURLs() -> Self](/documentation/webkit/wkwebextension/matchpattern/allurls())
- [class func registerCustomURLScheme(String)](/documentation/webkit/wkwebextension/matchpattern/registercustomurlscheme(_:))
- [WKWebExtension.MessagePort](/documentation/webkit/wkwebextension/messageport)

##### Structures

- [WKWebExtension.MessagePort.Error](/documentation/webkit/wkwebextension/messageport/error)

###### Type Properties

- [static var errorDomain: String](/documentation/webkit/wkwebextension/messageport/error/errordomain)
- [static var messageInvalid: WKWebExtension.MessagePort.Error.Code](/documentation/webkit/wkwebextension/messageport/error/messageinvalid)
- [static var notConnected: WKWebExtension.MessagePort.Error.Code](/documentation/webkit/wkwebextension/messageport/error/notconnected)
- [static var unknown: WKWebExtension.MessagePort.Error.Code](/documentation/webkit/wkwebextension/messageport/error/unknown)

##### Instance Properties

- [var applicationIdentifier: String?](/documentation/webkit/wkwebextension/messageport/applicationidentifier)
- [var disconnectHandler: (((any Error)?) -> Void)?](/documentation/webkit/wkwebextension/messageport/disconnecthandler)
- [var isDisconnected: Bool](/documentation/webkit/wkwebextension/messageport/isdisconnected)
- [var messageHandler: ((Any?, (any Error)?) -> Void)?](/documentation/webkit/wkwebextension/messageport/messagehandler)

##### Instance Methods

- [func disconnect()](/documentation/webkit/wkwebextension/messageport/disconnect())
- [func disconnect(throwing: (any Error)?)](/documentation/webkit/wkwebextension/messageport/disconnect(throwing:))
- [func sendMessage(Any?, completionHandler: (((any Error)?) -> Void)?)](/documentation/webkit/wkwebextension/messageport/sendmessage(_:completionhandler:))
- [WKWebExtension.TabConfiguration](/documentation/webkit/wkwebextension/tabconfiguration)

##### Instance Properties

- [var index: Int](/documentation/webkit/wkwebextension/tabconfiguration/index)
- [var parentTab: (any WKWebExtensionTab)?](/documentation/webkit/wkwebextension/tabconfiguration/parenttab)
- [var shouldAddToSelection: Bool](/documentation/webkit/wkwebextension/tabconfiguration/shouldaddtoselection)
- [var shouldBeActive: Bool](/documentation/webkit/wkwebextension/tabconfiguration/shouldbeactive)
- [var shouldBeMuted: Bool](/documentation/webkit/wkwebextension/tabconfiguration/shouldbemuted)
- [var shouldBePinned: Bool](/documentation/webkit/wkwebextension/tabconfiguration/shouldbepinned)
- [var shouldReaderModeBeActive: Bool](/documentation/webkit/wkwebextension/tabconfiguration/shouldreadermodebeactive)
- [var url: URL?](/documentation/webkit/wkwebextension/tabconfiguration/url)
- [var window: (any WKWebExtensionWindow)?](/documentation/webkit/wkwebextension/tabconfiguration/window)
- [WKWebExtension.WindowConfiguration](/documentation/webkit/wkwebextension/windowconfiguration)

##### Instance Properties

- [var frame: CGRect](/documentation/webkit/wkwebextension/windowconfiguration/frame)
- [var shouldBeFocused: Bool](/documentation/webkit/wkwebextension/windowconfiguration/shouldbefocused)
- [var shouldBePrivate: Bool](/documentation/webkit/wkwebextension/windowconfiguration/shouldbeprivate)
- [var tabURLs: [URL]](/documentation/webkit/wkwebextension/windowconfiguration/taburls)
- [var tabs: [any WKWebExtensionTab]](/documentation/webkit/wkwebextension/windowconfiguration/tabs)
- [var windowState: WKWebExtension.WindowState](/documentation/webkit/wkwebextension/windowconfiguration/windowstate)
- [var windowType: WKWebExtension.WindowType](/documentation/webkit/wkwebextension/windowconfiguration/windowtype)
- [WKWebExtensionController.Configuration](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class)

##### Initializers

- [convenience init(identifier: UUID)](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class/init(identifier:))

##### Instance Properties

- [var defaultWebsiteDataStore: WKWebsiteDataStore!](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class/defaultwebsitedatastore)
- [var identifier: UUID?](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class/identifier)
- [var isPersistent: Bool](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class/ispersistent)
- [var webViewConfiguration: WKWebViewConfiguration!](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class/webviewconfiguration)

##### Type Methods

- [class func `default`() -> Self](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class/default())
- [class func nonPersistent() -> Self](/documentation/webkit/wkwebextensioncontroller/configuration-swift.class/nonpersistent())

#### Structures

- [WKWebExtension.DataType](/documentation/webkit/wkwebextension/datatype)

##### Constants

- [static let local: WKWebExtension.DataType](/documentation/webkit/wkwebextension/datatype/local)
- [static let session: WKWebExtension.DataType](/documentation/webkit/wkwebextension/datatype/session)
- [static let synchronized: WKWebExtension.DataType](/documentation/webkit/wkwebextension/datatype/synchronized)

##### Initializers

- [init(rawValue: String)](/documentation/webkit/wkwebextension/datatype/init(rawvalue:))
- [WKWebExtension.Error](/documentation/webkit/wkwebextension/error)

##### Type Properties

- [static var errorDomain: String](/documentation/webkit/wkwebextension/error/errordomain)
- [static var invalidArchive: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/invalidarchive)
- [static var invalidBackgroundPersistence: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/invalidbackgroundpersistence)
- [static var invalidDeclarativeNetRequestEntry: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/invaliddeclarativenetrequestentry)
- [static var invalidManifest: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/invalidmanifest)
- [static var invalidManifestEntry: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/invalidmanifestentry)
- [static var invalidResourceCodeSignature: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/invalidresourcecodesignature)
- [static var resourceNotFound: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/resourcenotfound)
- [static var unknown: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/unknown)
- [static var unsupportedManifestVersion: WKWebExtension.Error.Code](/documentation/webkit/wkwebextension/error/unsupportedmanifestversion)
- [WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission)

##### Constants

- [static let activeTab: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/activetab)
- [static let alarms: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/alarms)
- [static let clipboardWrite: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/clipboardwrite)
- [static let contextMenus: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/contextmenus)
- [static let cookies: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/cookies)
- [static let declarativeNetRequest: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/declarativenetrequest)
- [static let declarativeNetRequestFeedback: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/declarativenetrequestfeedback)
- [static let declarativeNetRequestWithHostAccess: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/declarativenetrequestwithhostaccess)
- [static let menus: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/menus)
- [static let nativeMessaging: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/nativemessaging)
- [static let scripting: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/scripting)
- [static let storage: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/storage)
- [static let tabs: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/tabs)
- [static let unlimitedStorage: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/unlimitedstorage)
- [static let webNavigation: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/webnavigation)
- [static let webRequest: WKWebExtension.Permission](/documentation/webkit/wkwebextension/permission/webrequest)

##### Initializers

- [init(String)](/documentation/webkit/wkwebextension/permission/init(_:))
- [init(rawValue: String)](/documentation/webkit/wkwebextension/permission/init(rawvalue:))
- [WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties)

##### Initializers

- [init(rawValue: UInt)](/documentation/webkit/wkwebextension/tabchangedproperties/init(rawvalue:))

##### Type Properties

- [static var URL: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/url)
- [static var loading: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/loading)
- [static var muted: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/muted)
- [static var pinned: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/pinned)
- [static var playingAudio: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/playingaudio)
- [static var readerMode: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/readermode)
- [static var size: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/size)
- [static var title: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/title)
- [static var zoomFactor: WKWebExtension.TabChangedProperties](/documentation/webkit/wkwebextension/tabchangedproperties/zoomfactor)

#### Enumerations

- [WKWebExtension.WindowState](/documentation/webkit/wkwebextension/windowstate)

##### Enumeration Cases

- [case fullscreen](/documentation/webkit/wkwebextension/windowstate/fullscreen)
- [case maximized](/documentation/webkit/wkwebextension/windowstate/maximized)
- [case minimized](/documentation/webkit/wkwebextension/windowstate/minimized)
- [case normal](/documentation/webkit/wkwebextension/windowstate/normal)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkwebextension/windowstate/init(rawvalue:))
- [WKWebExtension.WindowType](/documentation/webkit/wkwebextension/windowtype)

##### Enumeration Cases

- [case normal](/documentation/webkit/wkwebextension/windowtype/normal)
- [case popup](/documentation/webkit/wkwebextension/windowtype/popup)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkwebextension/windowtype/init(rawvalue:))

#### Initializers

- [convenience init(appExtensionBundle: Bundle) async throws](/documentation/webkit/wkwebextension/init(appextensionbundle:))
- [convenience init(resourceBaseURL: URL) async throws](/documentation/webkit/wkwebextension/init(resourcebaseurl:))

#### Instance Properties

- [var allRequestedMatchPatterns: Set<WKWebExtension.MatchPattern>](/documentation/webkit/wkwebextension/allrequestedmatchpatterns)
- [var defaultLocale: Locale?](/documentation/webkit/wkwebextension/defaultlocale)
- [var displayActionLabel: String?](/documentation/webkit/wkwebextension/displayactionlabel)
- [var displayDescription: String?](/documentation/webkit/wkwebextension/displaydescription)
- [var displayName: String?](/documentation/webkit/wkwebextension/displayname)
- [var displayShortName: String?](/documentation/webkit/wkwebextension/displayshortname)
- [var displayVersion: String?](/documentation/webkit/wkwebextension/displayversion)
- [var errors: [any Error]](/documentation/webkit/wkwebextension/errors)
- [var hasBackgroundContent: Bool](/documentation/webkit/wkwebextension/hasbackgroundcontent)
- [var hasCommands: Bool](/documentation/webkit/wkwebextension/hascommands)
- [var hasContentModificationRules: Bool](/documentation/webkit/wkwebextension/hascontentmodificationrules)
- [var hasInjectedContent: Bool](/documentation/webkit/wkwebextension/hasinjectedcontent)
- [var hasOptionsPage: Bool](/documentation/webkit/wkwebextension/hasoptionspage)
- [var hasOverrideNewTabPage: Bool](/documentation/webkit/wkwebextension/hasoverridenewtabpage)
- [var hasPersistentBackgroundContent: Bool](/documentation/webkit/wkwebextension/haspersistentbackgroundcontent)
- [var manifest: [String : Any]](/documentation/webkit/wkwebextension/manifest)
- [var manifestVersion: Double](/documentation/webkit/wkwebextension/manifestversion)
- [var optionalPermissionMatchPatterns: Set<WKWebExtension.MatchPattern>](/documentation/webkit/wkwebextension/optionalpermissionmatchpatterns)
- [var optionalPermissions: Set<WKWebExtension.Permission>](/documentation/webkit/wkwebextension/optionalpermissions)
- [var requestedPermissionMatchPatterns: Set<WKWebExtension.MatchPattern>](/documentation/webkit/wkwebextension/requestedpermissionmatchpatterns)
- [var requestedPermissions: Set<WKWebExtension.Permission>](/documentation/webkit/wkwebextension/requestedpermissions)
- [var version: String?](/documentation/webkit/wkwebextension/version)

#### Instance Methods

- [func actionIcon(for: CGSize) -> UIImage?](/documentation/webkit/wkwebextension/actionicon(for:))
- [func icon(for: CGSize) -> UIImage?](/documentation/webkit/wkwebextension/icon(for:))
- [func supportsManifestVersion(Double) -> Bool](/documentation/webkit/wkwebextension/supportsmanifestversion(_:))
- [WKWebExtensionTab](/documentation/webkit/wkwebextensiontab)

#### Instance Methods

- [func activate(for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/activate(for:completionhandler:))
- [func close(for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/close(for:completionhandler:))
- [func detectWebpageLocale(for: WKWebExtensionContext, completionHandler: (Locale?, (any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/detectwebpagelocale(for:completionhandler:))
- [func duplicate(using: WKWebExtension.TabConfiguration, for: WKWebExtensionContext, completionHandler: ((any WKWebExtensionTab)?, (any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/duplicate(using:for:completionhandler:))
- [func goBack(for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/goback(for:completionhandler:))
- [func goForward(for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/goforward(for:completionhandler:))
- [func indexInWindow(for: WKWebExtensionContext) -> Int](/documentation/webkit/wkwebextensiontab/indexinwindow(for:))
- [func isLoadingComplete(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/isloadingcomplete(for:))
- [func isMuted(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/ismuted(for:))
- [func isPinned(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/ispinned(for:))
- [func isPlayingAudio(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/isplayingaudio(for:))
- [func isReaderModeActive(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/isreadermodeactive(for:))
- [func isReaderModeAvailable(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/isreadermodeavailable(for:))
- [func isSelected(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/isselected(for:))
- [func loadURL(URL, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/loadurl(_:for:completionhandler:))
- [func parentTab(for: WKWebExtensionContext) -> (any WKWebExtensionTab)?](/documentation/webkit/wkwebextensiontab/parenttab(for:))
- [func pendingURL(for: WKWebExtensionContext) -> URL?](/documentation/webkit/wkwebextensiontab/pendingurl(for:))
- [func reload(fromOrigin: Bool, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/reload(fromorigin:for:completionhandler:))
- [func setMuted(Bool, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/setmuted(_:for:completionhandler:))
- [func setParentTab((any WKWebExtensionTab)?, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/setparenttab(_:for:completionhandler:))
- [func setPinned(Bool, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/setpinned(_:for:completionhandler:))
- [func setReaderModeActive(Bool, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/setreadermodeactive(_:for:completionhandler:))
- [func setSelected(Bool, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/setselected(_:for:completionhandler:))
- [func setZoomFactor(Double, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/setzoomfactor(_:for:completionhandler:))
- [func shouldBypassPermissions(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/shouldbypasspermissions(for:))
- [func shouldGrantPermissionsOnUserGesture(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensiontab/shouldgrantpermissionsonusergesture(for:))
- [func size(for: WKWebExtensionContext) -> CGSize](/documentation/webkit/wkwebextensiontab/size(for:))
- [func takeSnapshot(using: WKSnapshotConfiguration, for: WKWebExtensionContext, completionHandler: (UIImage?, (any Error)?) -> Void)](/documentation/webkit/wkwebextensiontab/takesnapshot(using:for:completionhandler:))
- [func title(for: WKWebExtensionContext) -> String?](/documentation/webkit/wkwebextensiontab/title(for:))
- [func url(for: WKWebExtensionContext) -> URL?](/documentation/webkit/wkwebextensiontab/url(for:))
- [func webView(for: WKWebExtensionContext) -> WKWebView?](/documentation/webkit/wkwebextensiontab/webview(for:))
- [func window(for: WKWebExtensionContext) -> (any WKWebExtensionWindow)?](/documentation/webkit/wkwebextensiontab/window(for:))
- [func zoomFactor(for: WKWebExtensionContext) -> Double](/documentation/webkit/wkwebextensiontab/zoomfactor(for:))
- [WKWebExtensionWindow](/documentation/webkit/wkwebextensionwindow)

#### Instance Methods

- [func activeTab(for: WKWebExtensionContext) -> (any WKWebExtensionTab)?](/documentation/webkit/wkwebextensionwindow/activetab(for:))
- [func close(for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensionwindow/close(for:completionhandler:))
- [func focus(for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensionwindow/focus(for:completionhandler:))
- [func frame(for: WKWebExtensionContext) -> CGRect](/documentation/webkit/wkwebextensionwindow/frame(for:))
- [func isPrivate(for: WKWebExtensionContext) -> Bool](/documentation/webkit/wkwebextensionwindow/isprivate(for:))
- [func screenFrame(for: WKWebExtensionContext) -> CGRect](/documentation/webkit/wkwebextensionwindow/screenframe(for:))
- [func setFrame(CGRect, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensionwindow/setframe(_:for:completionhandler:))
- [func setWindowState(WKWebExtension.WindowState, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensionwindow/setwindowstate(_:for:completionhandler:))
- [func tabs(for: WKWebExtensionContext) -> [any WKWebExtensionTab]](/documentation/webkit/wkwebextensionwindow/tabs(for:))
- [func windowState(for: WKWebExtensionContext) -> WKWebExtension.WindowState](/documentation/webkit/wkwebextensionwindow/windowstate(for:))
- [func windowType(for: WKWebExtensionContext) -> WKWebExtension.WindowType](/documentation/webkit/wkwebextensionwindow/windowtype(for:))
- [WKWebExtensionContext](/documentation/webkit/wkwebextensioncontext)

#### Enumerations

- [WKWebExtensionContext.PermissionStatus](/documentation/webkit/wkwebextensioncontext/permissionstatus)

##### Enumeration Cases

- [case deniedExplicitly](/documentation/webkit/wkwebextensioncontext/permissionstatus/deniedexplicitly)
- [case deniedImplicitly](/documentation/webkit/wkwebextensioncontext/permissionstatus/deniedimplicitly)
- [case grantedExplicitly](/documentation/webkit/wkwebextensioncontext/permissionstatus/grantedexplicitly)
- [case grantedImplicitly](/documentation/webkit/wkwebextensioncontext/permissionstatus/grantedimplicitly)
- [case requestedExplicitly](/documentation/webkit/wkwebextensioncontext/permissionstatus/requestedexplicitly)
- [case requestedImplicitly](/documentation/webkit/wkwebextensioncontext/permissionstatus/requestedimplicitly)
- [case unknown](/documentation/webkit/wkwebextensioncontext/permissionstatus/unknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkwebextensioncontext/permissionstatus/init(rawvalue:))

#### Structures

- [WKWebExtensionContext.Error](/documentation/webkit/wkwebextensioncontext/error)

##### Type Properties

- [static var alreadyLoaded: WKWebExtensionContext.Error.Code](/documentation/webkit/wkwebextensioncontext/error/alreadyloaded)
- [static var backgroundContentFailedToLoad: WKWebExtensionContext.Error.Code](/documentation/webkit/wkwebextensioncontext/error/backgroundcontentfailedtoload)
- [static var baseURLAlreadyInUse: WKWebExtensionContext.Error.Code](/documentation/webkit/wkwebextensioncontext/error/baseurlalreadyinuse)
- [static var errorDomain: String](/documentation/webkit/wkwebextensioncontext/error/errordomain)
- [static var noBackgroundContent: WKWebExtensionContext.Error.Code](/documentation/webkit/wkwebextensioncontext/error/nobackgroundcontent)
- [static var notLoaded: WKWebExtensionContext.Error.Code](/documentation/webkit/wkwebextensioncontext/error/notloaded)
- [static var unknown: WKWebExtensionContext.Error.Code](/documentation/webkit/wkwebextensioncontext/error/unknown)
- [WKWebExtensionContext.NotificationUserInfoKey](/documentation/webkit/wkwebextensioncontext/notificationuserinfokey)

##### Type properties

- [static let matchPatterns: WKWebExtensionContext.NotificationUserInfoKey](/documentation/webkit/wkwebextensioncontext/notificationuserinfokey/matchpatterns)
- [static let permissions: WKWebExtensionContext.NotificationUserInfoKey](/documentation/webkit/wkwebextensioncontext/notificationuserinfokey/permissions)

##### Initializers

- [init(String)](/documentation/webkit/wkwebextensioncontext/notificationuserinfokey/init(_:))
- [init(rawValue: String)](/documentation/webkit/wkwebextensioncontext/notificationuserinfokey/init(rawvalue:))

#### Initializers

- [init(for: WKWebExtension)](/documentation/webkit/wkwebextensioncontext/init(for:))

#### Instance Properties

- [var baseURL: URL](/documentation/webkit/wkwebextensioncontext/baseurl)
- [var commands: [WKWebExtension.Command]](/documentation/webkit/wkwebextensioncontext/commands)
- [var currentPermissionMatchPatterns: Set<WKWebExtension.MatchPattern>](/documentation/webkit/wkwebextensioncontext/currentpermissionmatchpatterns)
- [var currentPermissions: Set<WKWebExtension.Permission>](/documentation/webkit/wkwebextensioncontext/currentpermissions)
- [var deniedPermissionMatchPatterns: [WKWebExtension.MatchPattern : Date]](/documentation/webkit/wkwebextensioncontext/deniedpermissionmatchpatterns)
- [var deniedPermissions: [WKWebExtension.Permission : Date]](/documentation/webkit/wkwebextensioncontext/deniedpermissions)
- [var errors: [any Error]](/documentation/webkit/wkwebextensioncontext/errors)
- [var focusedWindow: (any WKWebExtensionWindow)?](/documentation/webkit/wkwebextensioncontext/focusedwindow)
- [var grantedPermissionMatchPatterns: [WKWebExtension.MatchPattern : Date]](/documentation/webkit/wkwebextensioncontext/grantedpermissionmatchpatterns)
- [var grantedPermissions: [WKWebExtension.Permission : Date]](/documentation/webkit/wkwebextensioncontext/grantedpermissions)
- [var hasAccessToAllHosts: Bool](/documentation/webkit/wkwebextensioncontext/hasaccesstoallhosts)
- [var hasAccessToAllURLs: Bool](/documentation/webkit/wkwebextensioncontext/hasaccesstoallurls)
- [var hasAccessToPrivateData: Bool](/documentation/webkit/wkwebextensioncontext/hasaccesstoprivatedata)
- [var hasContentModificationRules: Bool](/documentation/webkit/wkwebextensioncontext/hascontentmodificationrules)
- [var hasInjectedContent: Bool](/documentation/webkit/wkwebextensioncontext/hasinjectedcontent)
- [var hasRequestedOptionalAccessToAllHosts: Bool](/documentation/webkit/wkwebextensioncontext/hasrequestedoptionalaccesstoallhosts)
- [var inspectionName: String?](/documentation/webkit/wkwebextensioncontext/inspectionname)
- [var isInspectable: Bool](/documentation/webkit/wkwebextensioncontext/isinspectable)
- [var isLoaded: Bool](/documentation/webkit/wkwebextensioncontext/isloaded)
- [var openTabs: Set<AnyHashable>](/documentation/webkit/wkwebextensioncontext/opentabs)
- [var openWindows: [any WKWebExtensionWindow]](/documentation/webkit/wkwebextensioncontext/openwindows)
- [var optionsPageURL: URL?](/documentation/webkit/wkwebextensioncontext/optionspageurl)
- [var overrideNewTabPageURL: URL?](/documentation/webkit/wkwebextensioncontext/overridenewtabpageurl)
- [var uniqueIdentifier: String](/documentation/webkit/wkwebextensioncontext/uniqueidentifier)
- [var unsupportedAPIs: Set<String>!](/documentation/webkit/wkwebextensioncontext/unsupportedapis)
- [var webExtension: WKWebExtension](/documentation/webkit/wkwebextensioncontext/webextension)
- [var webExtensionController: WKWebExtensionController?](/documentation/webkit/wkwebextensioncontext/webextensioncontroller)
- [var webViewConfiguration: WKWebViewConfiguration?](/documentation/webkit/wkwebextensioncontext/webviewconfiguration)

#### Instance Methods

- [func action(for: (any WKWebExtensionTab)?) -> WKWebExtension.Action?](/documentation/webkit/wkwebextensioncontext/action(for:))
- [func clearUserGesture(in: any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontext/clearusergesture(in:))
- [func command(for: NSEvent) -> WKWebExtension.Command?](/documentation/webkit/wkwebextensioncontext/command(for:))
- [func didActivateTab(any WKWebExtensionTab, previousActiveTab: (any WKWebExtensionTab)?)](/documentation/webkit/wkwebextensioncontext/didactivatetab(_:previousactivetab:))
- [func didChangeTabProperties(WKWebExtension.TabChangedProperties, for: any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontext/didchangetabproperties(_:for:))
- [func didCloseTab(any WKWebExtensionTab, windowIsClosing: Bool)](/documentation/webkit/wkwebextensioncontext/didclosetab(_:windowisclosing:))
- [func didCloseWindow(any WKWebExtensionWindow)](/documentation/webkit/wkwebextensioncontext/didclosewindow(_:))
- [func didDeselectTabs([any WKWebExtensionTab])](/documentation/webkit/wkwebextensioncontext/diddeselecttabs(_:))
- [func didFocusWindow((any WKWebExtensionWindow)?)](/documentation/webkit/wkwebextensioncontext/didfocuswindow(_:))
- [func didMoveTab(any WKWebExtensionTab, from: Int, in: (any WKWebExtensionWindow)?)](/documentation/webkit/wkwebextensioncontext/didmovetab(_:from:in:))
- [func didOpenTab(any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontext/didopentab(_:))
- [func didOpenWindow(any WKWebExtensionWindow)](/documentation/webkit/wkwebextensioncontext/didopenwindow(_:))
- [func didReplaceTab(any WKWebExtensionTab, with: any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontext/didreplacetab(_:with:))
- [func didSelectTabs([any WKWebExtensionTab])](/documentation/webkit/wkwebextensioncontext/didselecttabs(_:))
- [func hasAccess(to: URL) -> Bool](/documentation/webkit/wkwebextensioncontext/hasaccess(to:))
- [func hasAccess(to: URL, in: (any WKWebExtensionTab)?) -> Bool](/documentation/webkit/wkwebextensioncontext/hasaccess(to:in:))
- [func hasActiveUserGesture(in: any WKWebExtensionTab) -> Bool](/documentation/webkit/wkwebextensioncontext/hasactiveusergesture(in:))
- [func hasInjectedContent(for: URL) -> Bool](/documentation/webkit/wkwebextensioncontext/hasinjectedcontent(for:))
- [func hasPermission(WKWebExtension.Permission) -> Bool](/documentation/webkit/wkwebextensioncontext/haspermission(_:))
- [func hasPermission(WKWebExtension.Permission, in: (any WKWebExtensionTab)?) -> Bool](/documentation/webkit/wkwebextensioncontext/haspermission(_:in:))
- [func loadBackgroundContent(completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensioncontext/loadbackgroundcontent(completionhandler:))
- [func menuItems(for: any WKWebExtensionTab) -> [UIMenuElement]](/documentation/webkit/wkwebextensioncontext/menuitems(for:))
- [func performAction(for: (any WKWebExtensionTab)?)](/documentation/webkit/wkwebextensioncontext/performaction(for:))
- [func performCommand(WKWebExtension.Command)](/documentation/webkit/wkwebextensioncontext/performcommand(_:))
- [func performCommand(for: UIKeyCommand) -> Bool](/documentation/webkit/wkwebextensioncontext/performcommand(for:)-25rd1)
- [func performCommand(for: NSEvent) -> Bool](/documentation/webkit/wkwebextensioncontext/performcommand(for:)-8btj0)
- [func permissionStatus(for: WKWebExtension.Permission) -> WKWebExtensionContext.PermissionStatus](/documentation/webkit/wkwebextensioncontext/permissionstatus(for:)-3qq2w)
- [func permissionStatus(for: WKWebExtension.MatchPattern) -> WKWebExtensionContext.PermissionStatus](/documentation/webkit/wkwebextensioncontext/permissionstatus(for:)-7mu8)
- [func permissionStatus(for: URL) -> WKWebExtensionContext.PermissionStatus](/documentation/webkit/wkwebextensioncontext/permissionstatus(for:)-7ojrb)
- [func permissionStatus(for: WKWebExtension.Permission, in: (any WKWebExtensionTab)?) -> WKWebExtensionContext.PermissionStatus](/documentation/webkit/wkwebextensioncontext/permissionstatus(for:in:)-4h82n)
- [func permissionStatus(for: URL, in: (any WKWebExtensionTab)?) -> WKWebExtensionContext.PermissionStatus](/documentation/webkit/wkwebextensioncontext/permissionstatus(for:in:)-96xaf)
- [func permissionStatus(for: WKWebExtension.MatchPattern, in: (any WKWebExtensionTab)?) -> WKWebExtensionContext.PermissionStatus](/documentation/webkit/wkwebextensioncontext/permissionstatus(for:in:)-nqhm)
- [func setPermissionStatus(WKWebExtensionContext.PermissionStatus, for: WKWebExtension.Permission)](/documentation/webkit/wkwebextensioncontext/setpermissionstatus(_:for:)-4u95f)
- [func setPermissionStatus(WKWebExtensionContext.PermissionStatus, for: URL)](/documentation/webkit/wkwebextensioncontext/setpermissionstatus(_:for:)-5xahd)
- [func setPermissionStatus(WKWebExtensionContext.PermissionStatus, for: WKWebExtension.MatchPattern)](/documentation/webkit/wkwebextensioncontext/setpermissionstatus(_:for:)-6auqv)
- [func setPermissionStatus(WKWebExtensionContext.PermissionStatus, for: URL, expirationDate: Date?)](/documentation/webkit/wkwebextensioncontext/setpermissionstatus(_:for:expirationdate:)-5q9id)
- [func setPermissionStatus(WKWebExtensionContext.PermissionStatus, for: WKWebExtension.Permission, expirationDate: Date?)](/documentation/webkit/wkwebextensioncontext/setpermissionstatus(_:for:expirationdate:)-692ui)
- [func setPermissionStatus(WKWebExtensionContext.PermissionStatus, for: WKWebExtension.MatchPattern, expirationDate: Date?)](/documentation/webkit/wkwebextensioncontext/setpermissionstatus(_:for:expirationdate:)-7038f)
- [func userGesturePerformed(in: any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontext/usergestureperformed(in:))
- [WKWebExtensionController](/documentation/webkit/wkwebextensioncontroller)

#### Initializers

- [init()](/documentation/webkit/wkwebextensioncontroller/init())
- [init(configuration: WKWebExtensionController.Configuration)](/documentation/webkit/wkwebextensioncontroller/init(configuration:))

#### Instance Properties

- [var configuration: WKWebExtensionController.Configuration](/documentation/webkit/wkwebextensioncontroller/configuration-swift.property)
- [var delegate: (any WKWebExtensionControllerDelegate)?](/documentation/webkit/wkwebextensioncontroller/delegate)
- [var extensionContexts: Set<WKWebExtensionContext>](/documentation/webkit/wkwebextensioncontroller/extensioncontexts)
- [var extensions: Set<WKWebExtension>](/documentation/webkit/wkwebextensioncontroller/extensions)

#### Instance Methods

- [func didActivateTab(any WKWebExtensionTab, previousActiveTab: (any WKWebExtensionTab)?)](/documentation/webkit/wkwebextensioncontroller/didactivatetab(_:previousactivetab:))
- [func didChangeTabProperties(WKWebExtension.TabChangedProperties, for: any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontroller/didchangetabproperties(_:for:))
- [func didCloseTab(any WKWebExtensionTab, windowIsClosing: Bool)](/documentation/webkit/wkwebextensioncontroller/didclosetab(_:windowisclosing:))
- [func didCloseWindow(any WKWebExtensionWindow)](/documentation/webkit/wkwebextensioncontroller/didclosewindow(_:))
- [func didDeselectTabs([any WKWebExtensionTab])](/documentation/webkit/wkwebextensioncontroller/diddeselecttabs(_:))
- [func didFocusWindow((any WKWebExtensionWindow)?)](/documentation/webkit/wkwebextensioncontroller/didfocuswindow(_:))
- [func didMoveTab(any WKWebExtensionTab, from: Int, in: (any WKWebExtensionWindow)?)](/documentation/webkit/wkwebextensioncontroller/didmovetab(_:from:in:))
- [func didOpenTab(any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontroller/didopentab(_:))
- [func didOpenWindow(any WKWebExtensionWindow)](/documentation/webkit/wkwebextensioncontroller/didopenwindow(_:))
- [func didReplaceTab(any WKWebExtensionTab, with: any WKWebExtensionTab)](/documentation/webkit/wkwebextensioncontroller/didreplacetab(_:with:))
- [func didSelectTabs([any WKWebExtensionTab])](/documentation/webkit/wkwebextensioncontroller/didselecttabs(_:))
- [func extensionContext(for: URL) -> WKWebExtensionContext?](/documentation/webkit/wkwebextensioncontroller/extensioncontext(for:)-2kr4)
- [func extensionContext(for: WKWebExtension) -> WKWebExtensionContext?](/documentation/webkit/wkwebextensioncontroller/extensioncontext(for:)-6ecpm)
- [func fetchDataRecord(ofTypes: Set<WKWebExtension.DataType>, for: WKWebExtensionContext, completionHandler: (WKWebExtension.DataRecord?) -> Void)](/documentation/webkit/wkwebextensioncontroller/fetchdatarecord(oftypes:for:completionhandler:))
- [func fetchDataRecords(ofTypes: Set<WKWebExtension.DataType>, completionHandler: ([WKWebExtension.DataRecord]) -> Void)](/documentation/webkit/wkwebextensioncontroller/fetchdatarecords(oftypes:completionhandler:))
- [func load(WKWebExtensionContext) throws](/documentation/webkit/wkwebextensioncontroller/load(_:))
- [func removeData(ofTypes: Set<WKWebExtension.DataType>, from: [WKWebExtension.DataRecord], completionHandler: () -> Void)](/documentation/webkit/wkwebextensioncontroller/removedata(oftypes:from:completionhandler:))
- [func unload(WKWebExtensionContext) throws](/documentation/webkit/wkwebextensioncontroller/unload(_:))

#### Type Properties

- [class var allExtensionDataTypes: Set<WKWebExtension.DataType>](/documentation/webkit/wkwebextensioncontroller/allextensiondatatypes)
- [WKWebExtensionControllerDelegate](/documentation/webkit/wkwebextensioncontrollerdelegate)

#### Instance Methods

- [func webExtensionController(WKWebExtensionController, connectUsing: WKWebExtension.MessagePort, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:connectusing:for:completionhandler:))
- [func webExtensionController(WKWebExtensionController, didUpdate: WKWebExtension.Action, forExtensionContext: WKWebExtensionContext)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:didupdate:forextensioncontext:))
- [func webExtensionController(WKWebExtensionController, focusedWindowFor: WKWebExtensionContext) -> (any WKWebExtensionWindow)?](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:focusedwindowfor:))
- [func webExtensionController(WKWebExtensionController, openNewTabUsing: WKWebExtension.TabConfiguration, for: WKWebExtensionContext, completionHandler: ((any WKWebExtensionTab)?, (any Error)?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:opennewtabusing:for:completionhandler:))
- [func webExtensionController(WKWebExtensionController, openNewWindowUsing: WKWebExtension.WindowConfiguration, for: WKWebExtensionContext, completionHandler: ((any WKWebExtensionWindow)?, (any Error)?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:opennewwindowusing:for:completionhandler:))
- [func webExtensionController(WKWebExtensionController, openOptionsPageFor: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:openoptionspagefor:completionhandler:))
- [func webExtensionController(WKWebExtensionController, openWindowsFor: WKWebExtensionContext) -> [any WKWebExtensionWindow]](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:openwindowsfor:))
- [func webExtensionController(WKWebExtensionController, presentActionPopup: WKWebExtension.Action, for: WKWebExtensionContext, completionHandler: ((any Error)?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:presentactionpopup:for:completionhandler:))
- [func webExtensionController(WKWebExtensionController, promptForPermissionMatchPatterns: Set<WKWebExtension.MatchPattern>, in: (any WKWebExtensionTab)?, for: WKWebExtensionContext, completionHandler: (Set<WKWebExtension.MatchPattern>, Date?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:promptforpermissionmatchpatterns:in:for:completionhandler:))
- [func webExtensionController(WKWebExtensionController, promptForPermissionToAccess: Set<URL>, in: (any WKWebExtensionTab)?, for: WKWebExtensionContext, completionHandler: (Set<URL>, Date?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:promptforpermissiontoaccess:in:for:completionhandler:))
- [func webExtensionController(WKWebExtensionController, promptForPermissions: Set<WKWebExtension.Permission>, in: (any WKWebExtensionTab)?, for: WKWebExtensionContext, completionHandler: (Set<WKWebExtension.Permission>, Date?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:promptforpermissions:in:for:completionhandler:))
- [func webExtensionController(WKWebExtensionController, sendMessage: Any, toApplicationWithIdentifier: String?, for: WKWebExtensionContext, replyHandler: (Any?, (any Error)?) -> Void)](/documentation/webkit/wkwebextensioncontrollerdelegate/webextensioncontroller(_:sendmessage:toapplicationwithidentifier:for:replyhandler:))

### Errors

- [WKError.Code](/documentation/webkit/wkerror/code)

#### Errors

- [case unknown](/documentation/webkit/wkerror/code/unknown)
- [case webContentProcessTerminated](/documentation/webkit/wkerror/code/webcontentprocessterminated)
- [case webViewInvalidated](/documentation/webkit/wkerror/code/webviewinvalidated)
- [case javaScriptExceptionOccurred](/documentation/webkit/wkerror/code/javascriptexceptionoccurred)
- [case javaScriptResultTypeIsUnsupported](/documentation/webkit/wkerror/code/javascriptresulttypeisunsupported)
- [case contentRuleListStoreCompileFailed](/documentation/webkit/wkerror/code/contentruleliststorecompilefailed)
- [case contentRuleListStoreLookUpFailed](/documentation/webkit/wkerror/code/contentruleliststorelookupfailed)
- [case contentRuleListStoreRemoveFailed](/documentation/webkit/wkerror/code/contentruleliststoreremovefailed)
- [case contentRuleListStoreVersionMismatch](/documentation/webkit/wkerror/code/contentruleliststoreversionmismatch)
- [case attributedStringContentFailedToLoad](/documentation/webkit/wkerror/code/attributedstringcontentfailedtoload)
- [case attributedStringContentLoadTimedOut](/documentation/webkit/wkerror/code/attributedstringcontentloadtimedout)
- [case javaScriptInvalidFrameTarget](/documentation/webkit/wkerror/code/javascriptinvalidframetarget)
- [case navigationAppBoundDomain](/documentation/webkit/wkerror/code/navigationappbounddomain)
- [case javaScriptAppBoundDomain](/documentation/webkit/wkerror/code/javascriptappbounddomain)
- [case credentialNotFound](/documentation/webkit/wkerror/code/credentialnotfound)
- [case duplicateCredential](/documentation/webkit/wkerror/code/duplicatecredential)
- [case malformedCredential](/documentation/webkit/wkerror/code/malformedcredential)

#### Initializers

- [init?(rawValue: Int)](/documentation/webkit/wkerror/code/init(rawvalue:))
- [WKError](/documentation/webkit/wkerror)

#### Getting the Error Codes

- [static var unknown: WKError.Code](/documentation/webkit/wkerror/unknown)
- [static var webContentProcessTerminated: WKError.Code](/documentation/webkit/wkerror/webcontentprocessterminated)
- [static var webViewInvalidated: WKError.Code](/documentation/webkit/wkerror/webviewinvalidated)
- [static var javaScriptExceptionOccurred: WKError.Code](/documentation/webkit/wkerror/javascriptexceptionoccurred)
- [static var javaScriptResultTypeIsUnsupported: WKError.Code](/documentation/webkit/wkerror/javascriptresulttypeisunsupported)
- [static var contentRuleListStoreCompileFailed: WKError.Code](/documentation/webkit/wkerror/contentruleliststorecompilefailed)
- [static var contentRuleListStoreLookUpFailed: WKError.Code](/documentation/webkit/wkerror/contentruleliststorelookupfailed)
- [static var contentRuleListStoreRemoveFailed: WKError.Code](/documentation/webkit/wkerror/contentruleliststoreremovefailed)
- [static var contentRuleListStoreVersionMismatch: WKError.Code](/documentation/webkit/wkerror/contentruleliststoreversionmismatch)
- [static var attributedStringContentFailedToLoad: WKError.Code](/documentation/webkit/wkerror/attributedstringcontentfailedtoload)
- [static var attributedStringContentLoadTimedOut: WKError.Code](/documentation/webkit/wkerror/attributedstringcontentloadtimedout)
- [static var javaScriptInvalidFrameTarget: WKError.Code](/documentation/webkit/wkerror/javascriptinvalidframetarget)
- [static var navigationAppBoundDomain: WKError.Code](/documentation/webkit/wkerror/navigationappbounddomain)
- [static var javaScriptAppBoundDomain: WKError.Code](/documentation/webkit/wkerror/javascriptappbounddomain)
- [static var credentialNotFound: WKError.Code](/documentation/webkit/wkerror/credentialnotfound)
- [static var duplicateCredential: WKError.Code](/documentation/webkit/wkerror/duplicatecredential)
- [static var malformedCredential: WKError.Code](/documentation/webkit/wkerror/malformedcredential)

#### Type Properties

- [static var errorDomain: String](/documentation/webkit/wkerror/errordomain)

### Deprecated

- [Deprecated Symbols](/documentation/webkit/deprecated-symbols)

#### WebKit Legacy APIs

- [Document Object Models API (Legacy)](/documentation/webkit/document-object-models-api-legacy)

##### Document Object Model (DOM) APIs

- [DOMAbstractView](/documentation/webkit/domabstractview)

###### Instance Properties

- [var document: DOMDocument!](/documentation/webkit/domabstractview/document)
- [DOMAttr](/documentation/webkit/domattr)

###### Instance Properties

- [var name: String!](/documentation/webkit/domattr/name)
- [var ownerElement: DOMElement!](/documentation/webkit/domattr/ownerelement)
- [var specified: Bool](/documentation/webkit/domattr/specified)
- [var style: DOMCSSStyleDeclaration!](/documentation/webkit/domattr/style)
- [var value: String!](/documentation/webkit/domattr/value)
- [DOMBlob](/documentation/webkit/domblob)

###### Instance Properties

- [var size: UInt64](/documentation/webkit/domblob/size)
- [DOMCDATASection](/documentation/webkit/domcdatasection)
- [DOMCharacterData](/documentation/webkit/domcharacterdata)

###### Instance Properties

- [var data: String!](/documentation/webkit/domcharacterdata/data)
- [var length: UInt32](/documentation/webkit/domcharacterdata/length)

###### Instance Methods

- [func appendData(String!)](/documentation/webkit/domcharacterdata/appenddata(_:))
- [func deleteData(UInt32, length: UInt32)](/documentation/webkit/domcharacterdata/deletedata(_:length:))
- [func insertData(UInt32, data: String!)](/documentation/webkit/domcharacterdata/insertdata(_:data:))
- [func replaceData(UInt32, length: UInt32, data: String!)](/documentation/webkit/domcharacterdata/replacedata(_:length:data:))
- [func substringData(UInt32, length: UInt32) -> String!](/documentation/webkit/domcharacterdata/substringdata(_:length:))
- [DOMComment](/documentation/webkit/domcomment)
- [DOMCounter](/documentation/webkit/domcounter)

###### Instance Properties

- [var identifier: String!](/documentation/webkit/domcounter/identifier)
- [var listStyle: String!](/documentation/webkit/domcounter/liststyle)
- [var separator: String!](/documentation/webkit/domcounter/separator)
- [DOMCSSCharsetRule](/documentation/webkit/domcsscharsetrule)

###### Instance Properties

- [var encoding: String!](/documentation/webkit/domcsscharsetrule/encoding)
- [DOMCSSFontFaceRule](/documentation/webkit/domcssfontfacerule)

###### Instance Properties

- [var style: DOMCSSStyleDeclaration!](/documentation/webkit/domcssfontfacerule/style)
- [DOMCSSImportRule](/documentation/webkit/domcssimportrule)

###### Instance Properties

- [var href: String!](/documentation/webkit/domcssimportrule/href)
- [var media: DOMMediaList!](/documentation/webkit/domcssimportrule/media)
- [var styleSheet: DOMCSSStyleSheet!](/documentation/webkit/domcssimportrule/stylesheet)
- [DOMCSSMediaRule](/documentation/webkit/domcssmediarule)

###### Instance Properties

- [var cssRules: DOMCSSRuleList!](/documentation/webkit/domcssmediarule/cssrules)
- [var media: DOMMediaList!](/documentation/webkit/domcssmediarule/media)

###### Instance Methods

- [func delete(UInt32)](/documentation/webkit/domcssmediarule/delete(_:))
- [func insert(String!, index: UInt32) -> UInt32](/documentation/webkit/domcssmediarule/insert(_:index:))
- [DOMCSSPageRule](/documentation/webkit/domcsspagerule)

###### Instance Properties

- [var selectorText: String!](/documentation/webkit/domcsspagerule/selectortext)
- [var style: DOMCSSStyleDeclaration!](/documentation/webkit/domcsspagerule/style)
- [DOMCSSPrimitiveValue](/documentation/webkit/domcssprimitivevalue)

###### Instance Properties

- [var primitiveType: UInt16](/documentation/webkit/domcssprimitivevalue/primitivetype)

###### Instance Methods

- [func getCounterValue() -> DOMCounter!](/documentation/webkit/domcssprimitivevalue/getcountervalue())
- [func getFloat(UInt16) -> Float](/documentation/webkit/domcssprimitivevalue/getfloat(_:))
- [func getRGBColorValue() -> DOMRGBColor!](/documentation/webkit/domcssprimitivevalue/getrgbcolorvalue())
- [func getRectValue() -> DOMRect!](/documentation/webkit/domcssprimitivevalue/getrectvalue())
- [func getStringValue() -> String!](/documentation/webkit/domcssprimitivevalue/getstringvalue())
- [func setFloat(UInt16, floatValue: Float)](/documentation/webkit/domcssprimitivevalue/setfloat(_:floatvalue:))
- [func setString(UInt16, stringValue: String!)](/documentation/webkit/domcssprimitivevalue/setstring(_:stringvalue:))
- [DOMCSSRule](/documentation/webkit/domcssrule)

###### Instance Properties

- [var cssText: String!](/documentation/webkit/domcssrule/csstext)
- [var parent: DOMCSSRule!](/documentation/webkit/domcssrule/parent)
- [var parentStyleSheet: DOMCSSStyleSheet!](/documentation/webkit/domcssrule/parentstylesheet)
- [var type: UInt16](/documentation/webkit/domcssrule/type)
- [DOMCSSRuleList](/documentation/webkit/domcssrulelist)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domcssrulelist/length)

###### Instance Methods

- [func item(UInt32) -> DOMCSSRule!](/documentation/webkit/domcssrulelist/item(_:))
- [DOMCSSStyleDeclaration](/documentation/webkit/domcssstyledeclaration)

###### Instance Properties

- [var cssText: String!](/documentation/webkit/domcssstyledeclaration/csstext)
- [var length: UInt32](/documentation/webkit/domcssstyledeclaration/length)
- [var parentRule: DOMCSSRule!](/documentation/webkit/domcssstyledeclaration/parentrule)

###### Instance Methods

- [func azimuth() -> String!](/documentation/webkit/domcssstyledeclaration/azimuth())
- [func background() -> String!](/documentation/webkit/domcssstyledeclaration/background())
- [func backgroundAttachment() -> String!](/documentation/webkit/domcssstyledeclaration/backgroundattachment())
- [func backgroundColor() -> String!](/documentation/webkit/domcssstyledeclaration/backgroundcolor())
- [func backgroundImage() -> String!](/documentation/webkit/domcssstyledeclaration/backgroundimage())
- [func backgroundPosition() -> String!](/documentation/webkit/domcssstyledeclaration/backgroundposition())
- [func backgroundRepeat() -> String!](/documentation/webkit/domcssstyledeclaration/backgroundrepeat())
- [func border() -> String!](/documentation/webkit/domcssstyledeclaration/border())
- [func borderBottom() -> String!](/documentation/webkit/domcssstyledeclaration/borderbottom())
- [func borderBottomColor() -> String!](/documentation/webkit/domcssstyledeclaration/borderbottomcolor())
- [func borderBottomStyle() -> String!](/documentation/webkit/domcssstyledeclaration/borderbottomstyle())
- [func borderBottomWidth() -> String!](/documentation/webkit/domcssstyledeclaration/borderbottomwidth())
- [func borderCollapse() -> String!](/documentation/webkit/domcssstyledeclaration/bordercollapse())
- [func borderColor() -> String!](/documentation/webkit/domcssstyledeclaration/bordercolor())
- [func borderLeft() -> String!](/documentation/webkit/domcssstyledeclaration/borderleft())
- [func borderLeftColor() -> String!](/documentation/webkit/domcssstyledeclaration/borderleftcolor())
- [func borderLeftStyle() -> String!](/documentation/webkit/domcssstyledeclaration/borderleftstyle())
- [func borderLeftWidth() -> String!](/documentation/webkit/domcssstyledeclaration/borderleftwidth())
- [func borderRight() -> String!](/documentation/webkit/domcssstyledeclaration/borderright())
- [func borderRightColor() -> String!](/documentation/webkit/domcssstyledeclaration/borderrightcolor())
- [func borderRightStyle() -> String!](/documentation/webkit/domcssstyledeclaration/borderrightstyle())
- [func borderRightWidth() -> String!](/documentation/webkit/domcssstyledeclaration/borderrightwidth())
- [func borderSpacing() -> String!](/documentation/webkit/domcssstyledeclaration/borderspacing())
- [func borderStyle() -> String!](/documentation/webkit/domcssstyledeclaration/borderstyle())
- [func borderTop() -> String!](/documentation/webkit/domcssstyledeclaration/bordertop())
- [func borderTopColor() -> String!](/documentation/webkit/domcssstyledeclaration/bordertopcolor())
- [func borderTopStyle() -> String!](/documentation/webkit/domcssstyledeclaration/bordertopstyle())
- [func borderTopWidth() -> String!](/documentation/webkit/domcssstyledeclaration/bordertopwidth())
- [func borderWidth() -> String!](/documentation/webkit/domcssstyledeclaration/borderwidth())
- [func bottom() -> String!](/documentation/webkit/domcssstyledeclaration/bottom())
- [func captionSide() -> String!](/documentation/webkit/domcssstyledeclaration/captionside())
- [func clear() -> String!](/documentation/webkit/domcssstyledeclaration/clear())
- [func clip() -> String!](/documentation/webkit/domcssstyledeclaration/clip())
- [func color() -> String!](/documentation/webkit/domcssstyledeclaration/color())
- [func content() -> String!](/documentation/webkit/domcssstyledeclaration/content())
- [func counterIncrement() -> String!](/documentation/webkit/domcssstyledeclaration/counterincrement())
- [func counterReset() -> String!](/documentation/webkit/domcssstyledeclaration/counterreset())
- [func cssFloat() -> String!](/documentation/webkit/domcssstyledeclaration/cssfloat())
- [func cue() -> String!](/documentation/webkit/domcssstyledeclaration/cue())
- [func cueAfter() -> String!](/documentation/webkit/domcssstyledeclaration/cueafter())
- [func cueBefore() -> String!](/documentation/webkit/domcssstyledeclaration/cuebefore())
- [func cursor() -> String!](/documentation/webkit/domcssstyledeclaration/cursor())
- [func direction() -> String!](/documentation/webkit/domcssstyledeclaration/direction())
- [func display() -> String!](/documentation/webkit/domcssstyledeclaration/display())
- [func elevation() -> String!](/documentation/webkit/domcssstyledeclaration/elevation())
- [func emptyCells() -> String!](/documentation/webkit/domcssstyledeclaration/emptycells())
- [func font() -> String!](/documentation/webkit/domcssstyledeclaration/font())
- [func fontFamily() -> String!](/documentation/webkit/domcssstyledeclaration/fontfamily())
- [func fontSize() -> String!](/documentation/webkit/domcssstyledeclaration/fontsize())
- [func fontSizeAdjust() -> String!](/documentation/webkit/domcssstyledeclaration/fontsizeadjust())
- [func fontStretch() -> String!](/documentation/webkit/domcssstyledeclaration/fontstretch())
- [func fontStyle() -> String!](/documentation/webkit/domcssstyledeclaration/fontstyle())
- [func fontVariant() -> String!](/documentation/webkit/domcssstyledeclaration/fontvariant())
- [func fontWeight() -> String!](/documentation/webkit/domcssstyledeclaration/fontweight())
- [func getPropertyCSSValue(String!) -> DOMCSSValue!](/documentation/webkit/domcssstyledeclaration/getpropertycssvalue(_:))
- [func getPropertyPriority(String!) -> String!](/documentation/webkit/domcssstyledeclaration/getpropertypriority(_:))
- [func getPropertyValue(String!) -> String!](/documentation/webkit/domcssstyledeclaration/getpropertyvalue(_:))
- [func height() -> String!](/documentation/webkit/domcssstyledeclaration/height())
- [func isPropertyImplicit(String!) -> Bool](/documentation/webkit/domcssstyledeclaration/ispropertyimplicit(_:))
- [func item(UInt32) -> String!](/documentation/webkit/domcssstyledeclaration/item(_:))
- [func left() -> String!](/documentation/webkit/domcssstyledeclaration/left())
- [func letterSpacing() -> String!](/documentation/webkit/domcssstyledeclaration/letterspacing())
- [func lineHeight() -> String!](/documentation/webkit/domcssstyledeclaration/lineheight())
- [func listStyle() -> String!](/documentation/webkit/domcssstyledeclaration/liststyle())
- [func listStyleImage() -> String!](/documentation/webkit/domcssstyledeclaration/liststyleimage())
- [func listStylePosition() -> String!](/documentation/webkit/domcssstyledeclaration/liststyleposition())
- [func listStyleType() -> String!](/documentation/webkit/domcssstyledeclaration/liststyletype())
- [func margin() -> String!](/documentation/webkit/domcssstyledeclaration/margin())
- [func marginBottom() -> String!](/documentation/webkit/domcssstyledeclaration/marginbottom())
- [func marginLeft() -> String!](/documentation/webkit/domcssstyledeclaration/marginleft())
- [func marginRight() -> String!](/documentation/webkit/domcssstyledeclaration/marginright())
- [func marginTop() -> String!](/documentation/webkit/domcssstyledeclaration/margintop())
- [func markerOffset() -> String!](/documentation/webkit/domcssstyledeclaration/markeroffset())
- [func marks() -> String!](/documentation/webkit/domcssstyledeclaration/marks())
- [func maxHeight() -> String!](/documentation/webkit/domcssstyledeclaration/maxheight())
- [func maxWidth() -> String!](/documentation/webkit/domcssstyledeclaration/maxwidth())
- [func minHeight() -> String!](/documentation/webkit/domcssstyledeclaration/minheight())
- [func minWidth() -> String!](/documentation/webkit/domcssstyledeclaration/minwidth())
- [func orphans() -> String!](/documentation/webkit/domcssstyledeclaration/orphans())
- [func outline() -> String!](/documentation/webkit/domcssstyledeclaration/outline())
- [func outlineColor() -> String!](/documentation/webkit/domcssstyledeclaration/outlinecolor())
- [func outlineStyle() -> String!](/documentation/webkit/domcssstyledeclaration/outlinestyle())
- [func outlineWidth() -> String!](/documentation/webkit/domcssstyledeclaration/outlinewidth())
- [func overflow() -> String!](/documentation/webkit/domcssstyledeclaration/overflow())
- [func padding() -> String!](/documentation/webkit/domcssstyledeclaration/padding())
- [func paddingBottom() -> String!](/documentation/webkit/domcssstyledeclaration/paddingbottom())
- [func paddingLeft() -> String!](/documentation/webkit/domcssstyledeclaration/paddingleft())
- [func paddingRight() -> String!](/documentation/webkit/domcssstyledeclaration/paddingright())
- [func paddingTop() -> String!](/documentation/webkit/domcssstyledeclaration/paddingtop())
- [func page() -> String!](/documentation/webkit/domcssstyledeclaration/page())
- [func pageBreakAfter() -> String!](/documentation/webkit/domcssstyledeclaration/pagebreakafter())
- [func pageBreakBefore() -> String!](/documentation/webkit/domcssstyledeclaration/pagebreakbefore())
- [func pageBreakInside() -> String!](/documentation/webkit/domcssstyledeclaration/pagebreakinside())
- [func pause() -> String!](/documentation/webkit/domcssstyledeclaration/pause())
- [func pauseAfter() -> String!](/documentation/webkit/domcssstyledeclaration/pauseafter())
- [func pauseBefore() -> String!](/documentation/webkit/domcssstyledeclaration/pausebefore())
- [func pitch() -> String!](/documentation/webkit/domcssstyledeclaration/pitch())
- [func pitchRange() -> String!](/documentation/webkit/domcssstyledeclaration/pitchrange())
- [func playDuring() -> String!](/documentation/webkit/domcssstyledeclaration/playduring())
- [func position() -> String!](/documentation/webkit/domcssstyledeclaration/position())
- [func quotes() -> String!](/documentation/webkit/domcssstyledeclaration/quotes())
- [func removeProperty(String!) -> String!](/documentation/webkit/domcssstyledeclaration/removeproperty(_:))
- [func richness() -> String!](/documentation/webkit/domcssstyledeclaration/richness())
- [func right() -> String!](/documentation/webkit/domcssstyledeclaration/right())
- [func setAzimuth(String!)](/documentation/webkit/domcssstyledeclaration/setazimuth(_:))
- [func setBackground(String!)](/documentation/webkit/domcssstyledeclaration/setbackground(_:))
- [func setBackgroundAttachment(String!)](/documentation/webkit/domcssstyledeclaration/setbackgroundattachment(_:))
- [func setBackgroundColor(String!)](/documentation/webkit/domcssstyledeclaration/setbackgroundcolor(_:))
- [func setBackgroundImage(String!)](/documentation/webkit/domcssstyledeclaration/setbackgroundimage(_:))
- [func setBackgroundPosition(String!)](/documentation/webkit/domcssstyledeclaration/setbackgroundposition(_:))
- [func setBackgroundRepeat(String!)](/documentation/webkit/domcssstyledeclaration/setbackgroundrepeat(_:))
- [func setBorder(String!)](/documentation/webkit/domcssstyledeclaration/setborder(_:))
- [func setBorderBottom(String!)](/documentation/webkit/domcssstyledeclaration/setborderbottom(_:))
- [func setBorderBottomColor(String!)](/documentation/webkit/domcssstyledeclaration/setborderbottomcolor(_:))
- [func setBorderBottomStyle(String!)](/documentation/webkit/domcssstyledeclaration/setborderbottomstyle(_:))
- [func setBorderBottomWidth(String!)](/documentation/webkit/domcssstyledeclaration/setborderbottomwidth(_:))
- [func setBorderCollapse(String!)](/documentation/webkit/domcssstyledeclaration/setbordercollapse(_:))
- [func setBorderColor(String!)](/documentation/webkit/domcssstyledeclaration/setbordercolor(_:))
- [func setBorderLeft(String!)](/documentation/webkit/domcssstyledeclaration/setborderleft(_:))
- [func setBorderLeftColor(String!)](/documentation/webkit/domcssstyledeclaration/setborderleftcolor(_:))
- [func setBorderLeftStyle(String!)](/documentation/webkit/domcssstyledeclaration/setborderleftstyle(_:))
- [func setBorderLeftWidth(String!)](/documentation/webkit/domcssstyledeclaration/setborderleftwidth(_:))
- [func setBorderRight(String!)](/documentation/webkit/domcssstyledeclaration/setborderright(_:))
- [func setBorderRightColor(String!)](/documentation/webkit/domcssstyledeclaration/setborderrightcolor(_:))
- [func setBorderRightStyle(String!)](/documentation/webkit/domcssstyledeclaration/setborderrightstyle(_:))
- [func setBorderRightWidth(String!)](/documentation/webkit/domcssstyledeclaration/setborderrightwidth(_:))
- [func setBorderSpacing(String!)](/documentation/webkit/domcssstyledeclaration/setborderspacing(_:))
- [func setBorderStyle(String!)](/documentation/webkit/domcssstyledeclaration/setborderstyle(_:))
- [func setBorderTop(String!)](/documentation/webkit/domcssstyledeclaration/setbordertop(_:))
- [func setBorderTopColor(String!)](/documentation/webkit/domcssstyledeclaration/setbordertopcolor(_:))
- [func setBorderTopStyle(String!)](/documentation/webkit/domcssstyledeclaration/setbordertopstyle(_:))
- [func setBorderTopWidth(String!)](/documentation/webkit/domcssstyledeclaration/setbordertopwidth(_:))
- [func setBorderWidth(String!)](/documentation/webkit/domcssstyledeclaration/setborderwidth(_:))
- [func setBottom(String!)](/documentation/webkit/domcssstyledeclaration/setbottom(_:))
- [func setCaptionSide(String!)](/documentation/webkit/domcssstyledeclaration/setcaptionside(_:))
- [func setClear(String!)](/documentation/webkit/domcssstyledeclaration/setclear(_:))
- [func setClip(String!)](/documentation/webkit/domcssstyledeclaration/setclip(_:))
- [func setColor(String!)](/documentation/webkit/domcssstyledeclaration/setcolor(_:))
- [func setContent(String!)](/documentation/webkit/domcssstyledeclaration/setcontent(_:))
- [func setCounterIncrement(String!)](/documentation/webkit/domcssstyledeclaration/setcounterincrement(_:))
- [func setCounterReset(String!)](/documentation/webkit/domcssstyledeclaration/setcounterreset(_:))
- [func setCssFloat(String!)](/documentation/webkit/domcssstyledeclaration/setcssfloat(_:))
- [func setCue(String!)](/documentation/webkit/domcssstyledeclaration/setcue(_:))
- [func setCueAfter(String!)](/documentation/webkit/domcssstyledeclaration/setcueafter(_:))
- [func setCueBefore(String!)](/documentation/webkit/domcssstyledeclaration/setcuebefore(_:))
- [func setCursor(String!)](/documentation/webkit/domcssstyledeclaration/setcursor(_:))
- [func setDirection(String!)](/documentation/webkit/domcssstyledeclaration/setdirection(_:))
- [func setDisplay(String!)](/documentation/webkit/domcssstyledeclaration/setdisplay(_:))
- [func setElevation(String!)](/documentation/webkit/domcssstyledeclaration/setelevation(_:))
- [func setEmptyCells(String!)](/documentation/webkit/domcssstyledeclaration/setemptycells(_:))
- [func setFont(String!)](/documentation/webkit/domcssstyledeclaration/setfont(_:))
- [func setFontFamily(String!)](/documentation/webkit/domcssstyledeclaration/setfontfamily(_:))
- [func setFontSize(String!)](/documentation/webkit/domcssstyledeclaration/setfontsize(_:))
- [func setFontSizeAdjust(String!)](/documentation/webkit/domcssstyledeclaration/setfontsizeadjust(_:))
- [func setFontStretch(String!)](/documentation/webkit/domcssstyledeclaration/setfontstretch(_:))
- [func setFontStyle(String!)](/documentation/webkit/domcssstyledeclaration/setfontstyle(_:))
- [func setFontVariant(String!)](/documentation/webkit/domcssstyledeclaration/setfontvariant(_:))
- [func setFontWeight(String!)](/documentation/webkit/domcssstyledeclaration/setfontweight(_:))
- [func setHeight(String!)](/documentation/webkit/domcssstyledeclaration/setheight(_:))
- [func setLeft(String!)](/documentation/webkit/domcssstyledeclaration/setleft(_:))
- [func setLetterSpacing(String!)](/documentation/webkit/domcssstyledeclaration/setletterspacing(_:))
- [func setLineHeight(String!)](/documentation/webkit/domcssstyledeclaration/setlineheight(_:))
- [func setListStyle(String!)](/documentation/webkit/domcssstyledeclaration/setliststyle(_:))
- [func setListStyleImage(String!)](/documentation/webkit/domcssstyledeclaration/setliststyleimage(_:))
- [func setListStylePosition(String!)](/documentation/webkit/domcssstyledeclaration/setliststyleposition(_:))
- [func setListStyleType(String!)](/documentation/webkit/domcssstyledeclaration/setliststyletype(_:))
- [func setMargin(String!)](/documentation/webkit/domcssstyledeclaration/setmargin(_:))
- [func setMarginBottom(String!)](/documentation/webkit/domcssstyledeclaration/setmarginbottom(_:))
- [func setMarginLeft(String!)](/documentation/webkit/domcssstyledeclaration/setmarginleft(_:))
- [func setMarginRight(String!)](/documentation/webkit/domcssstyledeclaration/setmarginright(_:))
- [func setMarginTop(String!)](/documentation/webkit/domcssstyledeclaration/setmargintop(_:))
- [func setMarkerOffset(String!)](/documentation/webkit/domcssstyledeclaration/setmarkeroffset(_:))
- [func setMarks(String!)](/documentation/webkit/domcssstyledeclaration/setmarks(_:))
- [func setMaxHeight(String!)](/documentation/webkit/domcssstyledeclaration/setmaxheight(_:))
- [func setMaxWidth(String!)](/documentation/webkit/domcssstyledeclaration/setmaxwidth(_:))
- [func setMinHeight(String!)](/documentation/webkit/domcssstyledeclaration/setminheight(_:))
- [func setMinWidth(String!)](/documentation/webkit/domcssstyledeclaration/setminwidth(_:))
- [func setOrphans(String!)](/documentation/webkit/domcssstyledeclaration/setorphans(_:))
- [func setOutline(String!)](/documentation/webkit/domcssstyledeclaration/setoutline(_:))
- [func setOutlineColor(String!)](/documentation/webkit/domcssstyledeclaration/setoutlinecolor(_:))
- [func setOutlineStyle(String!)](/documentation/webkit/domcssstyledeclaration/setoutlinestyle(_:))
- [func setOutlineWidth(String!)](/documentation/webkit/domcssstyledeclaration/setoutlinewidth(_:))
- [func setOverflow(String!)](/documentation/webkit/domcssstyledeclaration/setoverflow(_:))
- [func setPadding(String!)](/documentation/webkit/domcssstyledeclaration/setpadding(_:))
- [func setPaddingBottom(String!)](/documentation/webkit/domcssstyledeclaration/setpaddingbottom(_:))
- [func setPaddingLeft(String!)](/documentation/webkit/domcssstyledeclaration/setpaddingleft(_:))
- [func setPaddingRight(String!)](/documentation/webkit/domcssstyledeclaration/setpaddingright(_:))
- [func setPaddingTop(String!)](/documentation/webkit/domcssstyledeclaration/setpaddingtop(_:))
- [func setPage(String!)](/documentation/webkit/domcssstyledeclaration/setpage(_:))
- [func setPageBreakAfter(String!)](/documentation/webkit/domcssstyledeclaration/setpagebreakafter(_:))
- [func setPageBreakBefore(String!)](/documentation/webkit/domcssstyledeclaration/setpagebreakbefore(_:))
- [func setPageBreakInside(String!)](/documentation/webkit/domcssstyledeclaration/setpagebreakinside(_:))
- [func setPause(String!)](/documentation/webkit/domcssstyledeclaration/setpause(_:))
- [func setPauseAfter(String!)](/documentation/webkit/domcssstyledeclaration/setpauseafter(_:))
- [func setPauseBefore(String!)](/documentation/webkit/domcssstyledeclaration/setpausebefore(_:))
- [func setPitch(String!)](/documentation/webkit/domcssstyledeclaration/setpitch(_:))
- [func setPitchRange(String!)](/documentation/webkit/domcssstyledeclaration/setpitchrange(_:))
- [func setPlayDuring(String!)](/documentation/webkit/domcssstyledeclaration/setplayduring(_:))
- [func setPosition(String!)](/documentation/webkit/domcssstyledeclaration/setposition(_:))
- [func setProperty(String!, value: String!, priority: String!)](/documentation/webkit/domcssstyledeclaration/setproperty(_:value:priority:))
- [func setQuotes(String!)](/documentation/webkit/domcssstyledeclaration/setquotes(_:))
- [func setRichness(String!)](/documentation/webkit/domcssstyledeclaration/setrichness(_:))
- [func setRight(String!)](/documentation/webkit/domcssstyledeclaration/setright(_:))
- [func setSize(String!)](/documentation/webkit/domcssstyledeclaration/setsize(_:))
- [func setSpeak(String!)](/documentation/webkit/domcssstyledeclaration/setspeak(_:))
- [func setSpeakHeader(String!)](/documentation/webkit/domcssstyledeclaration/setspeakheader(_:))
- [func setSpeakNumeral(String!)](/documentation/webkit/domcssstyledeclaration/setspeaknumeral(_:))
- [func setSpeakPunctuation(String!)](/documentation/webkit/domcssstyledeclaration/setspeakpunctuation(_:))
- [func setSpeechRate(String!)](/documentation/webkit/domcssstyledeclaration/setspeechrate(_:))
- [func setStress(String!)](/documentation/webkit/domcssstyledeclaration/setstress(_:))
- [func setTableLayout(String!)](/documentation/webkit/domcssstyledeclaration/settablelayout(_:))
- [func setTextAlign(String!)](/documentation/webkit/domcssstyledeclaration/settextalign(_:))
- [func setTextDecoration(String!)](/documentation/webkit/domcssstyledeclaration/settextdecoration(_:))
- [func setTextIndent(String!)](/documentation/webkit/domcssstyledeclaration/settextindent(_:))
- [func setTextShadow(String!)](/documentation/webkit/domcssstyledeclaration/settextshadow(_:))
- [func setTextTransform(String!)](/documentation/webkit/domcssstyledeclaration/settexttransform(_:))
- [func setTop(String!)](/documentation/webkit/domcssstyledeclaration/settop(_:))
- [func setUnicodeBidi(String!)](/documentation/webkit/domcssstyledeclaration/setunicodebidi(_:))
- [func setVerticalAlign(String!)](/documentation/webkit/domcssstyledeclaration/setverticalalign(_:))
- [func setVisibility(String!)](/documentation/webkit/domcssstyledeclaration/setvisibility(_:))
- [func setVoiceFamily(String!)](/documentation/webkit/domcssstyledeclaration/setvoicefamily(_:))
- [func setVolume(String!)](/documentation/webkit/domcssstyledeclaration/setvolume(_:))
- [func setWhiteSpace(String!)](/documentation/webkit/domcssstyledeclaration/setwhitespace(_:))
- [func setWidows(String!)](/documentation/webkit/domcssstyledeclaration/setwidows(_:))
- [func setWidth(String!)](/documentation/webkit/domcssstyledeclaration/setwidth(_:))
- [func setWordSpacing(String!)](/documentation/webkit/domcssstyledeclaration/setwordspacing(_:))
- [func setZIndex(String!)](/documentation/webkit/domcssstyledeclaration/setzindex(_:))
- [func size() -> String!](/documentation/webkit/domcssstyledeclaration/size())
- [func speak() -> String!](/documentation/webkit/domcssstyledeclaration/speak())
- [func speakHeader() -> String!](/documentation/webkit/domcssstyledeclaration/speakheader())
- [func speakNumeral() -> String!](/documentation/webkit/domcssstyledeclaration/speaknumeral())
- [func speakPunctuation() -> String!](/documentation/webkit/domcssstyledeclaration/speakpunctuation())
- [func speechRate() -> String!](/documentation/webkit/domcssstyledeclaration/speechrate())
- [func stress() -> String!](/documentation/webkit/domcssstyledeclaration/stress())
- [func tableLayout() -> String!](/documentation/webkit/domcssstyledeclaration/tablelayout())
- [func textAlign() -> String!](/documentation/webkit/domcssstyledeclaration/textalign())
- [func textDecoration() -> String!](/documentation/webkit/domcssstyledeclaration/textdecoration())
- [func textIndent() -> String!](/documentation/webkit/domcssstyledeclaration/textindent())
- [func textShadow() -> String!](/documentation/webkit/domcssstyledeclaration/textshadow())
- [func textTransform() -> String!](/documentation/webkit/domcssstyledeclaration/texttransform())
- [func top() -> String!](/documentation/webkit/domcssstyledeclaration/top())
- [func unicodeBidi() -> String!](/documentation/webkit/domcssstyledeclaration/unicodebidi())
- [func verticalAlign() -> String!](/documentation/webkit/domcssstyledeclaration/verticalalign())
- [func visibility() -> String!](/documentation/webkit/domcssstyledeclaration/visibility())
- [func voiceFamily() -> String!](/documentation/webkit/domcssstyledeclaration/voicefamily())
- [func volume() -> String!](/documentation/webkit/domcssstyledeclaration/volume())
- [func whiteSpace() -> String!](/documentation/webkit/domcssstyledeclaration/whitespace())
- [func widows() -> String!](/documentation/webkit/domcssstyledeclaration/widows())
- [func width() -> String!](/documentation/webkit/domcssstyledeclaration/width())
- [func wordSpacing() -> String!](/documentation/webkit/domcssstyledeclaration/wordspacing())
- [func zIndex() -> String!](/documentation/webkit/domcssstyledeclaration/zindex())
- [DOMCSSStyleRule](/documentation/webkit/domcssstylerule)

###### Instance Properties

- [var selectorText: String!](/documentation/webkit/domcssstylerule/selectortext)
- [var style: DOMCSSStyleDeclaration!](/documentation/webkit/domcssstylerule/style)
- [DOMCSSStyleSheet](/documentation/webkit/domcssstylesheet)

###### Instance Properties

- [var cssRules: DOMCSSRuleList!](/documentation/webkit/domcssstylesheet/cssrules)
- [var ownerRule: DOMCSSRule!](/documentation/webkit/domcssstylesheet/ownerrule)
- [var rules: DOMCSSRuleList!](/documentation/webkit/domcssstylesheet/rules)

###### Instance Methods

- [func addRule(String!, style: String!, index: UInt32) -> Int32](/documentation/webkit/domcssstylesheet/addrule(_:style:index:))
- [func deleteRule(UInt32)](/documentation/webkit/domcssstylesheet/deleterule(_:))
- [func insertRule(String!, index: UInt32) -> UInt32](/documentation/webkit/domcssstylesheet/insertrule(_:index:))
- [func removeRule(UInt32)](/documentation/webkit/domcssstylesheet/removerule(_:))
- [DOMCSSUnknownRule](/documentation/webkit/domcssunknownrule)
- [DOMCSSValue](/documentation/webkit/domcssvalue)

###### Instance Properties

- [var cssText: String!](/documentation/webkit/domcssvalue/csstext)
- [var cssValueType: UInt16](/documentation/webkit/domcssvalue/cssvaluetype)
- [DOMCSSValueList](/documentation/webkit/domcssvaluelist)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domcssvaluelist/length)

###### Instance Methods

- [func item(UInt32) -> DOMCSSValue!](/documentation/webkit/domcssvaluelist/item(_:))
- [DOMDocument](/documentation/webkit/domdocument)

###### Instance Properties

- [var activeElement: DOMElement!](/documentation/webkit/domdocument/activeelement)
- [var anchors: DOMHTMLCollection!](/documentation/webkit/domdocument/anchors)
- [var applets: DOMHTMLCollection!](/documentation/webkit/domdocument/applets)
- [var body: DOMHTMLElement!](/documentation/webkit/domdocument/body)
- [var characterSet: String!](/documentation/webkit/domdocument/characterset)
- [var charset: String!](/documentation/webkit/domdocument/charset)
- [var cookie: String!](/documentation/webkit/domdocument/cookie)
- [var defaultCharset: String!](/documentation/webkit/domdocument/defaultcharset)
- [var defaultView: DOMAbstractView!](/documentation/webkit/domdocument/defaultview)
- [var doctype: DOMDocumentType!](/documentation/webkit/domdocument/doctype)
- [var documentElement: DOMElement!](/documentation/webkit/domdocument/documentelement)
- [var documentURI: String!](/documentation/webkit/domdocument/documenturi)
- [var domain: String!](/documentation/webkit/domdocument/domain)
- [var forms: DOMHTMLCollection!](/documentation/webkit/domdocument/forms)
- [var images: DOMHTMLCollection!](/documentation/webkit/domdocument/images)
- [var implementation: DOMImplementation!](/documentation/webkit/domdocument/implementation)
- [var inputEncoding: String!](/documentation/webkit/domdocument/inputencoding)
- [var lastModified: String!](/documentation/webkit/domdocument/lastmodified)
- [var links: DOMHTMLCollection!](/documentation/webkit/domdocument/links)
- [var preferredStylesheetSet: String!](/documentation/webkit/domdocument/preferredstylesheetset)
- [var readyState: String!](/documentation/webkit/domdocument/readystate)
- [var referrer: String!](/documentation/webkit/domdocument/referrer)
- [var selectedStylesheetSet: String!](/documentation/webkit/domdocument/selectedstylesheetset)
- [var styleSheets: DOMStyleSheetList!](/documentation/webkit/domdocument/stylesheets)
- [var title: String!](/documentation/webkit/domdocument/title)
- [var url: String!](/documentation/webkit/domdocument/url)
- [var webFrame: WebFrame!](/documentation/webkit/domdocument/webframe)
- [var xmlEncoding: String!](/documentation/webkit/domdocument/xmlencoding)
- [var xmlStandalone: Bool](/documentation/webkit/domdocument/xmlstandalone)
- [var xmlVersion: String!](/documentation/webkit/domdocument/xmlversion)

###### Instance Methods

- [func adoptNode(DOMNode!) -> DOMNode!](/documentation/webkit/domdocument/adoptnode(_:))
- [func createAttribute(String!) -> DOMAttr!](/documentation/webkit/domdocument/createattribute(_:))
- [func createAttributeNS(String!, qualifiedName: String!) -> DOMAttr!](/documentation/webkit/domdocument/createattributens(_:qualifiedname:))
- [func createCDATASection(String!) -> DOMCDATASection!](/documentation/webkit/domdocument/createcdatasection(_:))
- [func createCSSStyleDeclaration() -> DOMCSSStyleDeclaration!](/documentation/webkit/domdocument/createcssstyledeclaration())
- [func createComment(String!) -> DOMComment!](/documentation/webkit/domdocument/createcomment(_:))
- [func createDocumentFragment() -> DOMDocumentFragment!](/documentation/webkit/domdocument/createdocumentfragment())
- [func createElement(String!) -> DOMElement!](/documentation/webkit/domdocument/createelement(_:))
- [func createElementNS(String!, qualifiedName: String!) -> DOMElement!](/documentation/webkit/domdocument/createelementns(_:qualifiedname:))
- [func createEntityReference(String!) -> DOMEntityReference!](/documentation/webkit/domdocument/createentityreference(_:))
- [func createEvent(String!) -> DOMEvent!](/documentation/webkit/domdocument/createevent(_:))
- [func createExpression(String!, resolver: (any DOMXPathNSResolver)!) -> DOMXPathExpression!](/documentation/webkit/domdocument/createexpression(_:resolver:))
- [func createNSResolver(DOMNode!) -> (any DOMXPathNSResolver)!](/documentation/webkit/domdocument/creatensresolver(_:))
- [func createNodeIterator(DOMNode!, whatToShow: UInt32, filter: (any DOMNodeFilter)!, expandEntityReferences: Bool) -> DOMNodeIterator!](/documentation/webkit/domdocument/createnodeiterator(_:whattoshow:filter:expandentityreferences:))
- [func createProcessingInstruction(String!, data: String!) -> DOMProcessingInstruction!](/documentation/webkit/domdocument/createprocessinginstruction(_:data:))
- [func createRange() -> DOMRange!](/documentation/webkit/domdocument/createrange())
- [func createTextNode(String!) -> DOMText!](/documentation/webkit/domdocument/createtextnode(_:))
- [func createTreeWalker(DOMNode!, whatToShow: UInt32, filter: (any DOMNodeFilter)!, expandEntityReferences: Bool) -> DOMTreeWalker!](/documentation/webkit/domdocument/createtreewalker(_:whattoshow:filter:expandentityreferences:))
- [func element(fromPoint: Int32, y: Int32) -> DOMElement!](/documentation/webkit/domdocument/element(frompoint:y:))
- [func evaluate(String!, contextNode: DOMNode!, resolver: (any DOMXPathNSResolver)!, type: UInt16, in: DOMXPathResult!) -> DOMXPathResult!](/documentation/webkit/domdocument/evaluate(_:contextnode:resolver:type:in:))
- [func execCommand(String!) -> Bool](/documentation/webkit/domdocument/execcommand(_:))
- [func execCommand(String!, userInterface: Bool) -> Bool](/documentation/webkit/domdocument/execcommand(_:userinterface:))
- [func execCommand(String!, userInterface: Bool, value: String!) -> Bool](/documentation/webkit/domdocument/execcommand(_:userinterface:value:))
- [func getComputedStyle(DOMElement!, pseudoElement: String!) -> DOMCSSStyleDeclaration!](/documentation/webkit/domdocument/getcomputedstyle(_:pseudoelement:))
- [func getElementById(String!) -> DOMElement!](/documentation/webkit/domdocument/getelementbyid(_:))
- [func getElementsByClassName(String!) -> DOMNodeList!](/documentation/webkit/domdocument/getelementsbyclassname(_:))
- [func getElementsByName(String!) -> DOMNodeList!](/documentation/webkit/domdocument/getelementsbyname(_:))
- [func getElementsByTagName(String!) -> DOMNodeList!](/documentation/webkit/domdocument/getelementsbytagname(_:))
- [func getElementsByTagNameNS(String!, localName: String!) -> DOMNodeList!](/documentation/webkit/domdocument/getelementsbytagnamens(_:localname:))
- [func getMatchedCSSRules(DOMElement!, pseudoElement: String!) -> DOMCSSRuleList!](/documentation/webkit/domdocument/getmatchedcssrules(_:pseudoelement:))
- [func getMatchedCSSRules(DOMElement!, pseudoElement: String!, authorOnly: Bool) -> DOMCSSRuleList!](/documentation/webkit/domdocument/getmatchedcssrules(_:pseudoelement:authoronly:))
- [func getOverrideStyle(DOMElement!, pseudoElement: String!) -> DOMCSSStyleDeclaration!](/documentation/webkit/domdocument/getoverridestyle(_:pseudoelement:))
- [func hasFocus() -> Bool](/documentation/webkit/domdocument/hasfocus())
- [func `import`(DOMNode!, deep: Bool) -> DOMNode!](/documentation/webkit/domdocument/import(_:deep:))
- [func queryCommandEnabled(String!) -> Bool](/documentation/webkit/domdocument/querycommandenabled(_:))
- [func queryCommandIndeterm(String!) -> Bool](/documentation/webkit/domdocument/querycommandindeterm(_:))
- [func queryCommandState(String!) -> Bool](/documentation/webkit/domdocument/querycommandstate(_:))
- [func queryCommandSupported(String!) -> Bool](/documentation/webkit/domdocument/querycommandsupported(_:))
- [func queryCommandValue(String!) -> String!](/documentation/webkit/domdocument/querycommandvalue(_:))
- [func querySelector(String!) -> DOMElement!](/documentation/webkit/domdocument/queryselector(_:))
- [func querySelectorAll(String!) -> DOMNodeList!](/documentation/webkit/domdocument/queryselectorall(_:))
- [func url(withAttributeString: String!) -> URL!](/documentation/webkit/domdocument/url(withattributestring:))
- [func webkitCancelFullScreen()](/documentation/webkit/domdocument/webkitcancelfullscreen())
- [DOMDocumentFragment](/documentation/webkit/domdocumentfragment)
- [DOMDocumentType](/documentation/webkit/domdocumenttype)

###### Instance Properties

- [var entities: DOMNamedNodeMap!](/documentation/webkit/domdocumenttype/entities)
- [var internalSubset: String!](/documentation/webkit/domdocumenttype/internalsubset)
- [var name: String!](/documentation/webkit/domdocumenttype/name)
- [var notations: DOMNamedNodeMap!](/documentation/webkit/domdocumenttype/notations)
- [var publicId: String!](/documentation/webkit/domdocumenttype/publicid)
- [var systemId: String!](/documentation/webkit/domdocumenttype/systemid)
- [DOMElement](/documentation/webkit/domelement)

###### Instance Properties

- [var childElementCount: UInt32](/documentation/webkit/domelement/childelementcount)
- [var className: String!](/documentation/webkit/domelement/classname)
- [var clientHeight: Int32](/documentation/webkit/domelement/clientheight)
- [var clientLeft: Int32](/documentation/webkit/domelement/clientleft)
- [var clientTop: Int32](/documentation/webkit/domelement/clienttop)
- [var clientWidth: Int32](/documentation/webkit/domelement/clientwidth)
- [var firstElementChild: DOMElement!](/documentation/webkit/domelement/firstelementchild)
- [var innerHTML: String!](/documentation/webkit/domelement/innerhtml)
- [var innerText: String!](/documentation/webkit/domelement/innertext)
- [var lastElementChild: DOMElement!](/documentation/webkit/domelement/lastelementchild)
- [var nextElementSibling: DOMElement!](/documentation/webkit/domelement/nextelementsibling)
- [var offsetHeight: Int32](/documentation/webkit/domelement/offsetheight)
- [var offsetLeft: Int32](/documentation/webkit/domelement/offsetleft)
- [var offsetParent: DOMElement!](/documentation/webkit/domelement/offsetparent)
- [var offsetTop: Int32](/documentation/webkit/domelement/offsettop)
- [var offsetWidth: Int32](/documentation/webkit/domelement/offsetwidth)
- [var outerHTML: String!](/documentation/webkit/domelement/outerhtml)
- [var previousElementSibling: DOMElement!](/documentation/webkit/domelement/previouselementsibling)
- [var scrollHeight: Int32](/documentation/webkit/domelement/scrollheight)
- [var scrollLeft: Int32](/documentation/webkit/domelement/scrollleft)
- [var scrollTop: Int32](/documentation/webkit/domelement/scrolltop)
- [var scrollWidth: Int32](/documentation/webkit/domelement/scrollwidth)
- [var style: DOMCSSStyleDeclaration!](/documentation/webkit/domelement/style)
- [var tagName: String!](/documentation/webkit/domelement/tagname)

###### Instance Methods

- [func blur()](/documentation/webkit/domelement/blur())
- [func focus()](/documentation/webkit/domelement/focus())
- [func getAttribute(String!) -> String!](/documentation/webkit/domelement/getattribute(_:))
- [func getAttributeNS(String!, localName: String!) -> String!](/documentation/webkit/domelement/getattributens(_:localname:))
- [func getAttributeNode(String!) -> DOMAttr!](/documentation/webkit/domelement/getattributenode(_:))
- [func getAttributeNodeNS(String!, localName: String!) -> DOMAttr!](/documentation/webkit/domelement/getattributenodens(_:localname:))
- [func getElementsByClassName(String!) -> DOMNodeList!](/documentation/webkit/domelement/getelementsbyclassname(_:))
- [func getElementsByTagName(String!) -> DOMNodeList!](/documentation/webkit/domelement/getelementsbytagname(_:))
- [func getElementsByTagNameNS(String!, localName: String!) -> DOMNodeList!](/documentation/webkit/domelement/getelementsbytagnamens(_:localname:))
- [func hasAttribute(String!) -> Bool](/documentation/webkit/domelement/hasattribute(_:))
- [func hasAttributeNS(String!, localName: String!) -> Bool](/documentation/webkit/domelement/hasattributens(_:localname:))
- [func image() -> NSImage!](/documentation/webkit/domelement/image())
- [func querySelector(String!) -> DOMElement!](/documentation/webkit/domelement/queryselector(_:))
- [func querySelectorAll(String!) -> DOMNodeList!](/documentation/webkit/domelement/queryselectorall(_:))
- [func removeAttribute(String!)](/documentation/webkit/domelement/removeattribute(_:))
- [func removeAttributeNS(String!, localName: String!)](/documentation/webkit/domelement/removeattributens(_:localname:))
- [func removeAttributeNode(DOMAttr!) -> DOMAttr!](/documentation/webkit/domelement/removeattributenode(_:))
- [func scroll(byLines: Int32)](/documentation/webkit/domelement/scroll(bylines:))
- [func scroll(byPages: Int32)](/documentation/webkit/domelement/scroll(bypages:))
- [func scroll(intoView: Bool)](/documentation/webkit/domelement/scroll(intoview:))
- [func scroll(intoViewIfNeeded: Bool)](/documentation/webkit/domelement/scroll(intoviewifneeded:))
- [func setAttribute(String!, value: String!)](/documentation/webkit/domelement/setattribute(_:value:))
- [func setAttributeNS(String!, qualifiedName: String!, value: String!)](/documentation/webkit/domelement/setattributens(_:qualifiedname:value:))
- [func setAttributeNode(DOMAttr!) -> DOMAttr!](/documentation/webkit/domelement/setattributenode(_:))
- [func setAttributeNodeNS(DOMAttr!) -> DOMAttr!](/documentation/webkit/domelement/setattributenodens(_:))
- [func webkitRequestFullScreen(UInt16)](/documentation/webkit/domelement/webkitrequestfullscreen(_:))
- [DOMEntity](/documentation/webkit/domentity)

###### Instance Properties

- [var notationName: String!](/documentation/webkit/domentity/notationname)
- [var publicId: String!](/documentation/webkit/domentity/publicid)
- [var systemId: String!](/documentation/webkit/domentity/systemid)
- [DOMEntityReference](/documentation/webkit/domentityreference)
- [DOMEvent](/documentation/webkit/domevent)

###### Instance Properties

- [var bubbles: Bool](/documentation/webkit/domevent/bubbles)
- [var cancelBubble: Bool](/documentation/webkit/domevent/cancelbubble)
- [var cancelable: Bool](/documentation/webkit/domevent/cancelable)
- [var currentTarget: (any DOMEventTarget)!](/documentation/webkit/domevent/currenttarget)
- [var eventPhase: UInt16](/documentation/webkit/domevent/eventphase)
- [var returnValue: Bool](/documentation/webkit/domevent/returnvalue)
- [var srcElement: (any DOMEventTarget)!](/documentation/webkit/domevent/srcelement)
- [var target: (any DOMEventTarget)!](/documentation/webkit/domevent/target)
- [var timeStamp: DOMTimeStamp](/documentation/webkit/domevent/timestamp)
- [var type: String!](/documentation/webkit/domevent/type)

###### Instance Methods

- [func initEvent(String!, canBubbleArg: Bool, cancelableArg: Bool)](/documentation/webkit/domevent/initevent(_:canbubblearg:cancelablearg:))
- [func preventDefault()](/documentation/webkit/domevent/preventdefault())
- [func stopPropagation()](/documentation/webkit/domevent/stoppropagation())
- [DOMFile](/documentation/webkit/domfile)

###### Instance Properties

- [var name: String!](/documentation/webkit/domfile/name)
- [DOMFileList](/documentation/webkit/domfilelist)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domfilelist/length)

###### Instance Methods

- [func item(UInt32) -> DOMFile!](/documentation/webkit/domfilelist/item(_:))
- [DOMHTMLAnchorElement](/documentation/webkit/domhtmlanchorelement)

###### Instance Properties

- [var absoluteLinkURL: URL!](/documentation/webkit/domhtmlanchorelement/absolutelinkurl)
- [var charset: String!](/documentation/webkit/domhtmlanchorelement/charset)
- [var coords: String!](/documentation/webkit/domhtmlanchorelement/coords)
- [var hashName: String!](/documentation/webkit/domhtmlanchorelement/hashname)
- [var host: String!](/documentation/webkit/domhtmlanchorelement/host)
- [var hostname: String!](/documentation/webkit/domhtmlanchorelement/hostname)
- [var href: String!](/documentation/webkit/domhtmlanchorelement/href)
- [var hreflang: String!](/documentation/webkit/domhtmlanchorelement/hreflang)
- [var name: String!](/documentation/webkit/domhtmlanchorelement/name)
- [var pathname: String!](/documentation/webkit/domhtmlanchorelement/pathname)
- [var port: String!](/documentation/webkit/domhtmlanchorelement/port)
- [var `protocol`: String!](/documentation/webkit/domhtmlanchorelement/protocol)
- [var rel: String!](/documentation/webkit/domhtmlanchorelement/rel)
- [var rev: String!](/documentation/webkit/domhtmlanchorelement/rev)
- [var search: String!](/documentation/webkit/domhtmlanchorelement/search)
- [var shape: String!](/documentation/webkit/domhtmlanchorelement/shape)
- [var target: String!](/documentation/webkit/domhtmlanchorelement/target)
- [var text: String!](/documentation/webkit/domhtmlanchorelement/text)
- [var type: String!](/documentation/webkit/domhtmlanchorelement/type)
- [DOMHTMLAppletElement](/documentation/webkit/domhtmlappletelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmlappletelement/align)
- [var alt: String!](/documentation/webkit/domhtmlappletelement/alt)
- [var archive: String!](/documentation/webkit/domhtmlappletelement/archive)
- [var code: String!](/documentation/webkit/domhtmlappletelement/code)
- [var codeBase: String!](/documentation/webkit/domhtmlappletelement/codebase)
- [var height: String!](/documentation/webkit/domhtmlappletelement/height)
- [var hspace: Int32](/documentation/webkit/domhtmlappletelement/hspace)
- [var name: String!](/documentation/webkit/domhtmlappletelement/name)
- [var object: String!](/documentation/webkit/domhtmlappletelement/object)
- [var vspace: Int32](/documentation/webkit/domhtmlappletelement/vspace)
- [var width: String!](/documentation/webkit/domhtmlappletelement/width)
- [DOMHTMLAreaElement](/documentation/webkit/domhtmlareaelement)

###### Instance Properties

- [var absoluteLinkURL: URL!](/documentation/webkit/domhtmlareaelement/absolutelinkurl)
- [var alt: String!](/documentation/webkit/domhtmlareaelement/alt)
- [var coords: String!](/documentation/webkit/domhtmlareaelement/coords)
- [var hashName: String!](/documentation/webkit/domhtmlareaelement/hashname)
- [var host: String!](/documentation/webkit/domhtmlareaelement/host)
- [var hostname: String!](/documentation/webkit/domhtmlareaelement/hostname)
- [var href: String!](/documentation/webkit/domhtmlareaelement/href)
- [var noHref: Bool](/documentation/webkit/domhtmlareaelement/nohref)
- [var pathname: String!](/documentation/webkit/domhtmlareaelement/pathname)
- [var port: String!](/documentation/webkit/domhtmlareaelement/port)
- [var `protocol`: String!](/documentation/webkit/domhtmlareaelement/protocol)
- [var search: String!](/documentation/webkit/domhtmlareaelement/search)
- [var shape: String!](/documentation/webkit/domhtmlareaelement/shape)
- [var target: String!](/documentation/webkit/domhtmlareaelement/target)
- [DOMHTMLBaseElement](/documentation/webkit/domhtmlbaseelement)

###### Instance Properties

- [var href: String!](/documentation/webkit/domhtmlbaseelement/href)
- [var target: String!](/documentation/webkit/domhtmlbaseelement/target)
- [DOMHTMLBaseFontElement](/documentation/webkit/domhtmlbasefontelement)

###### Instance Properties

- [var color: String!](/documentation/webkit/domhtmlbasefontelement/color)
- [var face: String!](/documentation/webkit/domhtmlbasefontelement/face)
- [var size: String!](/documentation/webkit/domhtmlbasefontelement/size)
- [DOMHTMLBodyElement](/documentation/webkit/domhtmlbodyelement)

###### Instance Properties

- [var aLink: String!](/documentation/webkit/domhtmlbodyelement/alink)
- [var background: String!](/documentation/webkit/domhtmlbodyelement/background)
- [var bgColor: String!](/documentation/webkit/domhtmlbodyelement/bgcolor)
- [var link: String!](/documentation/webkit/domhtmlbodyelement/link)
- [var text: String!](/documentation/webkit/domhtmlbodyelement/text)
- [var vLink: String!](/documentation/webkit/domhtmlbodyelement/vlink)
- [DOMHTMLBRElement](/documentation/webkit/domhtmlbrelement)

###### Instance Properties

- [var clear: String!](/documentation/webkit/domhtmlbrelement/clear)
- [DOMHTMLButtonElement](/documentation/webkit/domhtmlbuttonelement)

###### Instance Properties

- [var autofocus: Bool](/documentation/webkit/domhtmlbuttonelement/autofocus)
- [var disabled: Bool](/documentation/webkit/domhtmlbuttonelement/disabled)
- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmlbuttonelement/form)
- [var name: String!](/documentation/webkit/domhtmlbuttonelement/name)
- [var type: String!](/documentation/webkit/domhtmlbuttonelement/type)
- [var value: String!](/documentation/webkit/domhtmlbuttonelement/value)
- [var willValidate: Bool](/documentation/webkit/domhtmlbuttonelement/willvalidate)

###### Instance Methods

- [func click()](/documentation/webkit/domhtmlbuttonelement/click())
- [DOMHTMLCollection](/documentation/webkit/domhtmlcollection)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domhtmlcollection/length)

###### Instance Methods

- [func item(UInt32) -> DOMNode!](/documentation/webkit/domhtmlcollection/item(_:))
- [func namedItem(String!) -> DOMNode!](/documentation/webkit/domhtmlcollection/nameditem(_:))
- [func tags(String!) -> DOMNodeList!](/documentation/webkit/domhtmlcollection/tags(_:))
- [DOMHTMLDirectoryElement](/documentation/webkit/domhtmldirectoryelement)

###### Instance Properties

- [var compact: Bool](/documentation/webkit/domhtmldirectoryelement/compact)
- [DOMHTMLDivElement](/documentation/webkit/domhtmldivelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmldivelement/align)
- [DOMHTMLDListElement](/documentation/webkit/domhtmldlistelement)

###### Instance Properties

- [var compact: Bool](/documentation/webkit/domhtmldlistelement/compact)
- [DOMHTMLDocument](/documentation/webkit/domhtmldocument)

###### Instance Properties

- [var alinkColor: String!](/documentation/webkit/domhtmldocument/alinkcolor)
- [var bgColor: String!](/documentation/webkit/domhtmldocument/bgcolor)
- [var compatMode: String!](/documentation/webkit/domhtmldocument/compatmode)
- [var designMode: String!](/documentation/webkit/domhtmldocument/designmode)
- [var dir: String!](/documentation/webkit/domhtmldocument/dir)
- [var embeds: DOMHTMLCollection!](/documentation/webkit/domhtmldocument/embeds)
- [var fgColor: String!](/documentation/webkit/domhtmldocument/fgcolor)
- [var height: Int32](/documentation/webkit/domhtmldocument/height)
- [var linkColor: String!](/documentation/webkit/domhtmldocument/linkcolor)
- [var plugins: DOMHTMLCollection!](/documentation/webkit/domhtmldocument/plugins)
- [var scripts: DOMHTMLCollection!](/documentation/webkit/domhtmldocument/scripts)
- [var vlinkColor: String!](/documentation/webkit/domhtmldocument/vlinkcolor)
- [var width: Int32](/documentation/webkit/domhtmldocument/width)

###### Instance Methods

- [func captureEvents()](/documentation/webkit/domhtmldocument/captureevents())
- [func clear()](/documentation/webkit/domhtmldocument/clear())
- [func close()](/documentation/webkit/domhtmldocument/close())
- [func createDocumentFragment(withMarkupString: String!, baseURL: URL!) -> DOMDocumentFragment!](/documentation/webkit/domhtmldocument/createdocumentfragment(withmarkupstring:baseurl:))
- [func createDocumentFragment(withText: String!) -> DOMDocumentFragment!](/documentation/webkit/domhtmldocument/createdocumentfragment(withtext:))
- [func open()](/documentation/webkit/domhtmldocument/open())
- [func releaseEvents()](/documentation/webkit/domhtmldocument/releaseevents())
- [func write(String!)](/documentation/webkit/domhtmldocument/write(_:))
- [func writeln(String!)](/documentation/webkit/domhtmldocument/writeln(_:))
- [DOMHTMLElement](/documentation/webkit/domhtmlelement)

###### Instance Properties

- [var accessKey: String!](/documentation/webkit/domhtmlelement/accesskey)
- [var children: DOMHTMLCollection!](/documentation/webkit/domhtmlelement/children)
- [var contentEditable: String!](/documentation/webkit/domhtmlelement/contenteditable)
- [var dir: String!](/documentation/webkit/domhtmlelement/dir)
- [var idName: String!](/documentation/webkit/domhtmlelement/idname)
- [var innerText: String!](/documentation/webkit/domhtmlelement/innertext)
- [var isContentEditable: Bool](/documentation/webkit/domhtmlelement/iscontenteditable)
- [var lang: String!](/documentation/webkit/domhtmlelement/lang)
- [var outerText: String!](/documentation/webkit/domhtmlelement/outertext)
- [var tabIndex: Int32](/documentation/webkit/domhtmlelement/tabindex)
- [var title: String!](/documentation/webkit/domhtmlelement/title)
- [var titleDisplayString: String!](/documentation/webkit/domhtmlelement/titledisplaystring)

###### Instance Methods

- [func click()](/documentation/webkit/domhtmlelement/click())
- [DOMHTMLEmbedElement](/documentation/webkit/domhtmlembedelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmlembedelement/align)
- [var height: Int32](/documentation/webkit/domhtmlembedelement/height)
- [var name: String!](/documentation/webkit/domhtmlembedelement/name)
- [var src: String!](/documentation/webkit/domhtmlembedelement/src)
- [var type: String!](/documentation/webkit/domhtmlembedelement/type)
- [var width: Int32](/documentation/webkit/domhtmlembedelement/width)
- [DOMHTMLFieldSetElement](/documentation/webkit/domhtmlfieldsetelement)

###### Instance Properties

- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmlfieldsetelement/form)
- [DOMHTMLFontElement](/documentation/webkit/domhtmlfontelement)

###### Instance Properties

- [var color: String!](/documentation/webkit/domhtmlfontelement/color)
- [var face: String!](/documentation/webkit/domhtmlfontelement/face)
- [var size: String!](/documentation/webkit/domhtmlfontelement/size)
- [DOMHTMLFormElement](/documentation/webkit/domhtmlformelement)

###### Instance Properties

- [var acceptCharset: String!](/documentation/webkit/domhtmlformelement/acceptcharset)
- [var action: String!](/documentation/webkit/domhtmlformelement/action)
- [var elements: DOMHTMLCollection!](/documentation/webkit/domhtmlformelement/elements)
- [var encoding: String!](/documentation/webkit/domhtmlformelement/encoding)
- [var enctype: String!](/documentation/webkit/domhtmlformelement/enctype)
- [var length: Int32](/documentation/webkit/domhtmlformelement/length)
- [var method: String!](/documentation/webkit/domhtmlformelement/method)
- [var name: String!](/documentation/webkit/domhtmlformelement/name)
- [var target: String!](/documentation/webkit/domhtmlformelement/target)

###### Instance Methods

- [func reset()](/documentation/webkit/domhtmlformelement/reset())
- [func submit()](/documentation/webkit/domhtmlformelement/submit())
- [DOMHTMLFrameElement](/documentation/webkit/domhtmlframeelement)

###### Instance Properties

- [var contentDocument: DOMDocument!](/documentation/webkit/domhtmlframeelement/contentdocument)
- [var contentFrame: WebFrame!](/documentation/webkit/domhtmlframeelement/contentframe)
- [var contentWindow: DOMAbstractView!](/documentation/webkit/domhtmlframeelement/contentwindow)
- [var frameBorder: String!](/documentation/webkit/domhtmlframeelement/frameborder)
- [var height: Int32](/documentation/webkit/domhtmlframeelement/height)
- [var location: String!](/documentation/webkit/domhtmlframeelement/location)
- [var longDesc: String!](/documentation/webkit/domhtmlframeelement/longdesc)
- [var marginHeight: String!](/documentation/webkit/domhtmlframeelement/marginheight)
- [var marginWidth: String!](/documentation/webkit/domhtmlframeelement/marginwidth)
- [var name: String!](/documentation/webkit/domhtmlframeelement/name)
- [var noResize: Bool](/documentation/webkit/domhtmlframeelement/noresize)
- [var scrolling: String!](/documentation/webkit/domhtmlframeelement/scrolling)
- [var src: String!](/documentation/webkit/domhtmlframeelement/src)
- [var width: Int32](/documentation/webkit/domhtmlframeelement/width)
- [DOMHTMLFrameSetElement](/documentation/webkit/domhtmlframesetelement)

###### Instance Properties

- [var cols: String!](/documentation/webkit/domhtmlframesetelement/cols)
- [var rows: String!](/documentation/webkit/domhtmlframesetelement/rows)
- [DOMHTMLHeadElement](/documentation/webkit/domhtmlheadelement)

###### Instance Properties

- [var profile: String!](/documentation/webkit/domhtmlheadelement/profile)
- [DOMHTMLHeadingElement](/documentation/webkit/domhtmlheadingelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmlheadingelement/align)
- [DOMHTMLHRElement](/documentation/webkit/domhtmlhrelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmlhrelement/align)
- [var noShade: Bool](/documentation/webkit/domhtmlhrelement/noshade)
- [var size: String!](/documentation/webkit/domhtmlhrelement/size)
- [var width: String!](/documentation/webkit/domhtmlhrelement/width)
- [DOMHTMLHtmlElement](/documentation/webkit/domhtmlhtmlelement)

###### Instance Properties

- [var version: String!](/documentation/webkit/domhtmlhtmlelement/version)
- [DOMHTMLIFrameElement](/documentation/webkit/domhtmliframeelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmliframeelement/align)
- [var contentDocument: DOMDocument!](/documentation/webkit/domhtmliframeelement/contentdocument)
- [var contentFrame: WebFrame!](/documentation/webkit/domhtmliframeelement/contentframe)
- [var contentWindow: DOMAbstractView!](/documentation/webkit/domhtmliframeelement/contentwindow)
- [var frameBorder: String!](/documentation/webkit/domhtmliframeelement/frameborder)
- [var height: String!](/documentation/webkit/domhtmliframeelement/height)
- [var longDesc: String!](/documentation/webkit/domhtmliframeelement/longdesc)
- [var marginHeight: String!](/documentation/webkit/domhtmliframeelement/marginheight)
- [var marginWidth: String!](/documentation/webkit/domhtmliframeelement/marginwidth)
- [var name: String!](/documentation/webkit/domhtmliframeelement/name)
- [var scrolling: String!](/documentation/webkit/domhtmliframeelement/scrolling)
- [var src: String!](/documentation/webkit/domhtmliframeelement/src)
- [var width: String!](/documentation/webkit/domhtmliframeelement/width)
- [DOMHTMLImageElement](/documentation/webkit/domhtmlimageelement)

###### Instance Properties

- [var absoluteImageURL: URL!](/documentation/webkit/domhtmlimageelement/absoluteimageurl)
- [var align: String!](/documentation/webkit/domhtmlimageelement/align)
- [var alt: String!](/documentation/webkit/domhtmlimageelement/alt)
- [var altDisplayString: String!](/documentation/webkit/domhtmlimageelement/altdisplaystring)
- [var border: String!](/documentation/webkit/domhtmlimageelement/border)
- [var complete: Bool](/documentation/webkit/domhtmlimageelement/complete)
- [var height: Int32](/documentation/webkit/domhtmlimageelement/height)
- [var hspace: Int32](/documentation/webkit/domhtmlimageelement/hspace)
- [var isMap: Bool](/documentation/webkit/domhtmlimageelement/ismap)
- [var longDesc: String!](/documentation/webkit/domhtmlimageelement/longdesc)
- [var lowsrc: String!](/documentation/webkit/domhtmlimageelement/lowsrc)
- [var name: String!](/documentation/webkit/domhtmlimageelement/name)
- [var naturalHeight: Int32](/documentation/webkit/domhtmlimageelement/naturalheight)
- [var naturalWidth: Int32](/documentation/webkit/domhtmlimageelement/naturalwidth)
- [var src: String!](/documentation/webkit/domhtmlimageelement/src)
- [var useMap: String!](/documentation/webkit/domhtmlimageelement/usemap)
- [var vspace: Int32](/documentation/webkit/domhtmlimageelement/vspace)
- [var width: Int32](/documentation/webkit/domhtmlimageelement/width)
- [var x: Int32](/documentation/webkit/domhtmlimageelement/x)
- [var y: Int32](/documentation/webkit/domhtmlimageelement/y)
- [DOMHTMLInputElement](/documentation/webkit/domhtmlinputelement)

###### Instance Properties

- [var absoluteImageURL: URL!](/documentation/webkit/domhtmlinputelement/absoluteimageurl)
- [var accept: String!](/documentation/webkit/domhtmlinputelement/accept)
- [var align: String!](/documentation/webkit/domhtmlinputelement/align)
- [var alt: String!](/documentation/webkit/domhtmlinputelement/alt)
- [var altDisplayString: String!](/documentation/webkit/domhtmlinputelement/altdisplaystring)
- [var autofocus: Bool](/documentation/webkit/domhtmlinputelement/autofocus)
- [var checked: Bool](/documentation/webkit/domhtmlinputelement/checked)
- [var defaultChecked: Bool](/documentation/webkit/domhtmlinputelement/defaultchecked)
- [var defaultValue: String!](/documentation/webkit/domhtmlinputelement/defaultvalue)
- [var disabled: Bool](/documentation/webkit/domhtmlinputelement/disabled)
- [var files: DOMFileList!](/documentation/webkit/domhtmlinputelement/files)
- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmlinputelement/form)
- [var indeterminate: Bool](/documentation/webkit/domhtmlinputelement/indeterminate)
- [var maxLength: Int32](/documentation/webkit/domhtmlinputelement/maxlength)
- [var multiple: Bool](/documentation/webkit/domhtmlinputelement/multiple)
- [var name: String!](/documentation/webkit/domhtmlinputelement/name)
- [var readOnly: Bool](/documentation/webkit/domhtmlinputelement/readonly)
- [var selectionEnd: Int32](/documentation/webkit/domhtmlinputelement/selectionend)
- [var selectionStart: Int32](/documentation/webkit/domhtmlinputelement/selectionstart)
- [var size: String!](/documentation/webkit/domhtmlinputelement/size)
- [var src: String!](/documentation/webkit/domhtmlinputelement/src)
- [var type: String!](/documentation/webkit/domhtmlinputelement/type)
- [var useMap: String!](/documentation/webkit/domhtmlinputelement/usemap)
- [var value: String!](/documentation/webkit/domhtmlinputelement/value)
- [var willValidate: Bool](/documentation/webkit/domhtmlinputelement/willvalidate)

###### Instance Methods

- [func click()](/documentation/webkit/domhtmlinputelement/click())
- [func select()](/documentation/webkit/domhtmlinputelement/select())
- [func setSelectionRange(Int32, end: Int32)](/documentation/webkit/domhtmlinputelement/setselectionrange(_:end:))
- [DOMHTMLLabelElement](/documentation/webkit/domhtmllabelelement)

###### Instance Properties

- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmllabelelement/form)
- [var htmlFor: String!](/documentation/webkit/domhtmllabelelement/htmlfor)
- [DOMHTMLLegendElement](/documentation/webkit/domhtmllegendelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmllegendelement/align)
- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmllegendelement/form)
- [DOMHTMLLIElement](/documentation/webkit/domhtmllielement)

###### Instance Properties

- [var type: String!](/documentation/webkit/domhtmllielement/type)
- [var value: Int32](/documentation/webkit/domhtmllielement/value)
- [DOMHTMLLinkElement](/documentation/webkit/domhtmllinkelement)

###### Instance Properties

- [var absoluteLinkURL: URL!](/documentation/webkit/domhtmllinkelement/absolutelinkurl)
- [var charset: String!](/documentation/webkit/domhtmllinkelement/charset)
- [var disabled: Bool](/documentation/webkit/domhtmllinkelement/disabled)
- [var href: String!](/documentation/webkit/domhtmllinkelement/href)
- [var hreflang: String!](/documentation/webkit/domhtmllinkelement/hreflang)
- [var media: String!](/documentation/webkit/domhtmllinkelement/media)
- [var rel: String!](/documentation/webkit/domhtmllinkelement/rel)
- [var rev: String!](/documentation/webkit/domhtmllinkelement/rev)
- [var sheet: DOMStyleSheet!](/documentation/webkit/domhtmllinkelement/sheet)
- [var target: String!](/documentation/webkit/domhtmllinkelement/target)
- [var type: String!](/documentation/webkit/domhtmllinkelement/type)
- [DOMHTMLMapElement](/documentation/webkit/domhtmlmapelement)

###### Instance Properties

- [var areas: DOMHTMLCollection!](/documentation/webkit/domhtmlmapelement/areas)
- [var name: String!](/documentation/webkit/domhtmlmapelement/name)
- [DOMHTMLMarqueeElement](/documentation/webkit/domhtmlmarqueeelement)

###### Instance Methods

- [func start()](/documentation/webkit/domhtmlmarqueeelement/start())
- [func stop()](/documentation/webkit/domhtmlmarqueeelement/stop())
- [DOMHTMLMenuElement](/documentation/webkit/domhtmlmenuelement)

###### Instance Properties

- [var compact: Bool](/documentation/webkit/domhtmlmenuelement/compact)
- [DOMHTMLMetaElement](/documentation/webkit/domhtmlmetaelement)

###### Instance Properties

- [var content: String!](/documentation/webkit/domhtmlmetaelement/content)
- [var httpEquiv: String!](/documentation/webkit/domhtmlmetaelement/httpequiv)
- [var name: String!](/documentation/webkit/domhtmlmetaelement/name)
- [var scheme: String!](/documentation/webkit/domhtmlmetaelement/scheme)
- [DOMHTMLModElement](/documentation/webkit/domhtmlmodelement)

###### Instance Properties

- [var cite: String!](/documentation/webkit/domhtmlmodelement/cite)
- [var dateTime: String!](/documentation/webkit/domhtmlmodelement/datetime)
- [DOMHTMLObjectElement](/documentation/webkit/domhtmlobjectelement)

###### Instance Properties

- [var absoluteImageURL: URL!](/documentation/webkit/domhtmlobjectelement/absoluteimageurl)
- [var align: String!](/documentation/webkit/domhtmlobjectelement/align)
- [var archive: String!](/documentation/webkit/domhtmlobjectelement/archive)
- [var border: String!](/documentation/webkit/domhtmlobjectelement/border)
- [var code: String!](/documentation/webkit/domhtmlobjectelement/code)
- [var codeBase: String!](/documentation/webkit/domhtmlobjectelement/codebase)
- [var codeType: String!](/documentation/webkit/domhtmlobjectelement/codetype)
- [var contentDocument: DOMDocument!](/documentation/webkit/domhtmlobjectelement/contentdocument)
- [var contentFrame: WebFrame!](/documentation/webkit/domhtmlobjectelement/contentframe)
- [var data: String!](/documentation/webkit/domhtmlobjectelement/data)
- [var declare: Bool](/documentation/webkit/domhtmlobjectelement/declare)
- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmlobjectelement/form)
- [var height: String!](/documentation/webkit/domhtmlobjectelement/height)
- [var hspace: Int32](/documentation/webkit/domhtmlobjectelement/hspace)
- [var name: String!](/documentation/webkit/domhtmlobjectelement/name)
- [var standby: String!](/documentation/webkit/domhtmlobjectelement/standby)
- [var type: String!](/documentation/webkit/domhtmlobjectelement/type)
- [var useMap: String!](/documentation/webkit/domhtmlobjectelement/usemap)
- [var vspace: Int32](/documentation/webkit/domhtmlobjectelement/vspace)
- [var width: String!](/documentation/webkit/domhtmlobjectelement/width)
- [DOMHTMLOListElement](/documentation/webkit/domhtmlolistelement)

###### Instance Properties

- [var compact: Bool](/documentation/webkit/domhtmlolistelement/compact)
- [var start: Int32](/documentation/webkit/domhtmlolistelement/start)
- [var type: String!](/documentation/webkit/domhtmlolistelement/type)
- [DOMHTMLOptGroupElement](/documentation/webkit/domhtmloptgroupelement)

###### Instance Properties

- [var disabled: Bool](/documentation/webkit/domhtmloptgroupelement/disabled)
- [var label: String!](/documentation/webkit/domhtmloptgroupelement/label)
- [DOMHTMLOptionElement](/documentation/webkit/domhtmloptionelement)

###### Instance Properties

- [var defaultSelected: Bool](/documentation/webkit/domhtmloptionelement/defaultselected)
- [var disabled: Bool](/documentation/webkit/domhtmloptionelement/disabled)
- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmloptionelement/form)
- [var index: Int32](/documentation/webkit/domhtmloptionelement/index)
- [var label: String!](/documentation/webkit/domhtmloptionelement/label)
- [var selected: Bool](/documentation/webkit/domhtmloptionelement/selected)
- [var text: String!](/documentation/webkit/domhtmloptionelement/text)
- [var value: String!](/documentation/webkit/domhtmloptionelement/value)
- [DOMHTMLOptionsCollection](/documentation/webkit/domhtmloptionscollection)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domhtmloptionscollection/length)
- [var selectedIndex: Int32](/documentation/webkit/domhtmloptionscollection/selectedindex)

###### Instance Methods

- [func add(DOMHTMLOptionElement!, index: UInt32)](/documentation/webkit/domhtmloptionscollection/add(_:index:))
- [func item(UInt32) -> DOMNode!](/documentation/webkit/domhtmloptionscollection/item(_:))
- [func namedItem(String!) -> DOMNode!](/documentation/webkit/domhtmloptionscollection/nameditem(_:))
- [func remove(UInt32)](/documentation/webkit/domhtmloptionscollection/remove(_:))
- [DOMHTMLParagraphElement](/documentation/webkit/domhtmlparagraphelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmlparagraphelement/align)
- [DOMHTMLParamElement](/documentation/webkit/domhtmlparamelement)

###### Instance Properties

- [var name: String!](/documentation/webkit/domhtmlparamelement/name)
- [var type: String!](/documentation/webkit/domhtmlparamelement/type)
- [var value: String!](/documentation/webkit/domhtmlparamelement/value)
- [var valueType: String!](/documentation/webkit/domhtmlparamelement/valuetype)
- [DOMHTMLPreElement](/documentation/webkit/domhtmlpreelement)

###### Instance Properties

- [var width: Int32](/documentation/webkit/domhtmlpreelement/width)
- [var wrap: Bool](/documentation/webkit/domhtmlpreelement/wrap)
- [DOMHTMLQuoteElement](/documentation/webkit/domhtmlquoteelement)

###### Instance Properties

- [var cite: String!](/documentation/webkit/domhtmlquoteelement/cite)
- [DOMHTMLScriptElement](/documentation/webkit/domhtmlscriptelement)

###### Instance Properties

- [var charset: String!](/documentation/webkit/domhtmlscriptelement/charset)
- [var `defer`: Bool](/documentation/webkit/domhtmlscriptelement/defer)
- [var event: String!](/documentation/webkit/domhtmlscriptelement/event)
- [var htmlFor: String!](/documentation/webkit/domhtmlscriptelement/htmlfor)
- [var src: String!](/documentation/webkit/domhtmlscriptelement/src)
- [var text: String!](/documentation/webkit/domhtmlscriptelement/text)
- [var type: String!](/documentation/webkit/domhtmlscriptelement/type)
- [DOMHTMLSelectElement](/documentation/webkit/domhtmlselectelement)

###### Instance Properties

- [var autofocus: Bool](/documentation/webkit/domhtmlselectelement/autofocus)
- [var disabled: Bool](/documentation/webkit/domhtmlselectelement/disabled)
- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmlselectelement/form)
- [var length: Int32](/documentation/webkit/domhtmlselectelement/length)
- [var multiple: Bool](/documentation/webkit/domhtmlselectelement/multiple)
- [var name: String!](/documentation/webkit/domhtmlselectelement/name)
- [var options: DOMHTMLOptionsCollection!](/documentation/webkit/domhtmlselectelement/options)
- [var selectedIndex: Int32](/documentation/webkit/domhtmlselectelement/selectedindex)
- [var size: Int32](/documentation/webkit/domhtmlselectelement/size)
- [var type: String!](/documentation/webkit/domhtmlselectelement/type)
- [var value: String!](/documentation/webkit/domhtmlselectelement/value)
- [var willValidate: Bool](/documentation/webkit/domhtmlselectelement/willvalidate)

###### Instance Methods

- [func add(DOMHTMLElement!, before: DOMHTMLElement!)](/documentation/webkit/domhtmlselectelement/add(_:before:))
- [func item(UInt32) -> DOMNode!](/documentation/webkit/domhtmlselectelement/item(_:))
- [func namedItem(String!) -> DOMNode!](/documentation/webkit/domhtmlselectelement/nameditem(_:))
- [func remove(Int32)](/documentation/webkit/domhtmlselectelement/remove(_:))
- [DOMHTMLStyleElement](/documentation/webkit/domhtmlstyleelement)

###### Instance Properties

- [var disabled: Bool](/documentation/webkit/domhtmlstyleelement/disabled)
- [var media: String!](/documentation/webkit/domhtmlstyleelement/media)
- [var sheet: DOMStyleSheet!](/documentation/webkit/domhtmlstyleelement/sheet)
- [var type: String!](/documentation/webkit/domhtmlstyleelement/type)
- [DOMHTMLTableCaptionElement](/documentation/webkit/domhtmltablecaptionelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmltablecaptionelement/align)
- [DOMHTMLTableCellElement](/documentation/webkit/domhtmltablecellelement)

###### Instance Properties

- [var abbr: String!](/documentation/webkit/domhtmltablecellelement/abbr)
- [var align: String!](/documentation/webkit/domhtmltablecellelement/align)
- [var axis: String!](/documentation/webkit/domhtmltablecellelement/axis)
- [var bgColor: String!](/documentation/webkit/domhtmltablecellelement/bgcolor)
- [var cellIndex: Int32](/documentation/webkit/domhtmltablecellelement/cellindex)
- [var ch: String!](/documentation/webkit/domhtmltablecellelement/ch)
- [var chOff: String!](/documentation/webkit/domhtmltablecellelement/choff)
- [var colSpan: Int32](/documentation/webkit/domhtmltablecellelement/colspan)
- [var headers: String!](/documentation/webkit/domhtmltablecellelement/headers)
- [var height: String!](/documentation/webkit/domhtmltablecellelement/height)
- [var noWrap: Bool](/documentation/webkit/domhtmltablecellelement/nowrap)
- [var rowSpan: Int32](/documentation/webkit/domhtmltablecellelement/rowspan)
- [var scope: String!](/documentation/webkit/domhtmltablecellelement/scope)
- [var vAlign: String!](/documentation/webkit/domhtmltablecellelement/valign)
- [var width: String!](/documentation/webkit/domhtmltablecellelement/width)
- [DOMHTMLTableColElement](/documentation/webkit/domhtmltablecolelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmltablecolelement/align)
- [var ch: String!](/documentation/webkit/domhtmltablecolelement/ch)
- [var chOff: String!](/documentation/webkit/domhtmltablecolelement/choff)
- [var span: Int32](/documentation/webkit/domhtmltablecolelement/span)
- [var vAlign: String!](/documentation/webkit/domhtmltablecolelement/valign)
- [var width: String!](/documentation/webkit/domhtmltablecolelement/width)
- [DOMHTMLTableElement](/documentation/webkit/domhtmltableelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmltableelement/align)
- [var bgColor: String!](/documentation/webkit/domhtmltableelement/bgcolor)
- [var border: String!](/documentation/webkit/domhtmltableelement/border)
- [var caption: DOMHTMLTableCaptionElement!](/documentation/webkit/domhtmltableelement/caption)
- [var cellPadding: String!](/documentation/webkit/domhtmltableelement/cellpadding)
- [var cellSpacing: String!](/documentation/webkit/domhtmltableelement/cellspacing)
- [var frameBorders: String!](/documentation/webkit/domhtmltableelement/frameborders)
- [var rows: DOMHTMLCollection!](/documentation/webkit/domhtmltableelement/rows)
- [var rules: String!](/documentation/webkit/domhtmltableelement/rules)
- [var summary: String!](/documentation/webkit/domhtmltableelement/summary)
- [var tBodies: DOMHTMLCollection!](/documentation/webkit/domhtmltableelement/tbodies)
- [var tFoot: DOMHTMLTableSectionElement!](/documentation/webkit/domhtmltableelement/tfoot)
- [var tHead: DOMHTMLTableSectionElement!](/documentation/webkit/domhtmltableelement/thead)
- [var width: String!](/documentation/webkit/domhtmltableelement/width)

###### Instance Methods

- [func createCaption() -> DOMHTMLElement!](/documentation/webkit/domhtmltableelement/createcaption())
- [func createTFoot() -> DOMHTMLElement!](/documentation/webkit/domhtmltableelement/createtfoot())
- [func createTHead() -> DOMHTMLElement!](/documentation/webkit/domhtmltableelement/createthead())
- [func deleteCaption()](/documentation/webkit/domhtmltableelement/deletecaption())
- [func deleteRow(Int32)](/documentation/webkit/domhtmltableelement/deleterow(_:))
- [func deleteTFoot()](/documentation/webkit/domhtmltableelement/deletetfoot())
- [func deleteTHead()](/documentation/webkit/domhtmltableelement/deletethead())
- [func insertRow(Int32) -> DOMHTMLElement!](/documentation/webkit/domhtmltableelement/insertrow(_:))
- [DOMHTMLTableRowElement](/documentation/webkit/domhtmltablerowelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmltablerowelement/align)
- [var bgColor: String!](/documentation/webkit/domhtmltablerowelement/bgcolor)
- [var cells: DOMHTMLCollection!](/documentation/webkit/domhtmltablerowelement/cells)
- [var ch: String!](/documentation/webkit/domhtmltablerowelement/ch)
- [var chOff: String!](/documentation/webkit/domhtmltablerowelement/choff)
- [var rowIndex: Int32](/documentation/webkit/domhtmltablerowelement/rowindex)
- [var sectionRowIndex: Int32](/documentation/webkit/domhtmltablerowelement/sectionrowindex)
- [var vAlign: String!](/documentation/webkit/domhtmltablerowelement/valign)

###### Instance Methods

- [func deleteCell(Int32)](/documentation/webkit/domhtmltablerowelement/deletecell(_:))
- [func insertCell(Int32) -> DOMHTMLElement!](/documentation/webkit/domhtmltablerowelement/insertcell(_:))
- [DOMHTMLTableSectionElement](/documentation/webkit/domhtmltablesectionelement)

###### Instance Properties

- [var align: String!](/documentation/webkit/domhtmltablesectionelement/align)
- [var ch: String!](/documentation/webkit/domhtmltablesectionelement/ch)
- [var chOff: String!](/documentation/webkit/domhtmltablesectionelement/choff)
- [var rows: DOMHTMLCollection!](/documentation/webkit/domhtmltablesectionelement/rows)
- [var vAlign: String!](/documentation/webkit/domhtmltablesectionelement/valign)

###### Instance Methods

- [func deleteRow(Int32)](/documentation/webkit/domhtmltablesectionelement/deleterow(_:))
- [func insertRow(Int32) -> DOMHTMLElement!](/documentation/webkit/domhtmltablesectionelement/insertrow(_:))
- [DOMHTMLTextAreaElement](/documentation/webkit/domhtmltextareaelement)

###### Instance Properties

- [var autofocus: Bool](/documentation/webkit/domhtmltextareaelement/autofocus)
- [var cols: Int32](/documentation/webkit/domhtmltextareaelement/cols)
- [var defaultValue: String!](/documentation/webkit/domhtmltextareaelement/defaultvalue)
- [var disabled: Bool](/documentation/webkit/domhtmltextareaelement/disabled)
- [var form: DOMHTMLFormElement!](/documentation/webkit/domhtmltextareaelement/form)
- [var name: String!](/documentation/webkit/domhtmltextareaelement/name)
- [var readOnly: Bool](/documentation/webkit/domhtmltextareaelement/readonly)
- [var rows: Int32](/documentation/webkit/domhtmltextareaelement/rows)
- [var selectionEnd: Int32](/documentation/webkit/domhtmltextareaelement/selectionend)
- [var selectionStart: Int32](/documentation/webkit/domhtmltextareaelement/selectionstart)
- [var type: String!](/documentation/webkit/domhtmltextareaelement/type)
- [var value: String!](/documentation/webkit/domhtmltextareaelement/value)
- [var willValidate: Bool](/documentation/webkit/domhtmltextareaelement/willvalidate)

###### Instance Methods

- [func select()](/documentation/webkit/domhtmltextareaelement/select())
- [func setSelectionRange(Int32, end: Int32)](/documentation/webkit/domhtmltextareaelement/setselectionrange(_:end:))
- [DOMHTMLTitleElement](/documentation/webkit/domhtmltitleelement)

###### Instance Properties

- [var text: String!](/documentation/webkit/domhtmltitleelement/text)
- [DOMHTMLUListElement](/documentation/webkit/domhtmlulistelement)

###### Instance Properties

- [var compact: Bool](/documentation/webkit/domhtmlulistelement/compact)
- [var type: String!](/documentation/webkit/domhtmlulistelement/type)
- [DOMImplementation](/documentation/webkit/domimplementation)

###### Instance Methods

- [func createCSSStyleSheet(String!, media: String!) -> DOMCSSStyleSheet!](/documentation/webkit/domimplementation/createcssstylesheet(_:media:))
- [func createDocument(String!, qualifiedName: String!, doctype: DOMDocumentType!) -> DOMDocument!](/documentation/webkit/domimplementation/createdocument(_:qualifiedname:doctype:))
- [func createDocumentType(String!, publicId: String!, systemId: String!) -> DOMDocumentType!](/documentation/webkit/domimplementation/createdocumenttype(_:publicid:systemid:))
- [func createHTMLDocument(String!) -> DOMHTMLDocument!](/documentation/webkit/domimplementation/createhtmldocument(_:))
- [func hasFeature(String!, version: String!) -> Bool](/documentation/webkit/domimplementation/hasfeature(_:version:))
- [DOMKeyboardEvent](/documentation/webkit/domkeyboardevent)

###### Instance Properties

- [var altGraphKey: Bool](/documentation/webkit/domkeyboardevent/altgraphkey)
- [var altKey: Bool](/documentation/webkit/domkeyboardevent/altkey)
- [var charCode: Int32](/documentation/webkit/domkeyboardevent/charcode)
- [var ctrlKey: Bool](/documentation/webkit/domkeyboardevent/ctrlkey)
- [var keyCode: Int32](/documentation/webkit/domkeyboardevent/keycode)
- [var keyIdentifier: String!](/documentation/webkit/domkeyboardevent/keyidentifier)
- [var location: UInt32](/documentation/webkit/domkeyboardevent/location)
- [var metaKey: Bool](/documentation/webkit/domkeyboardevent/metakey)
- [var shiftKey: Bool](/documentation/webkit/domkeyboardevent/shiftkey)

###### Instance Methods

- [func getModifierState(String!) -> Bool](/documentation/webkit/domkeyboardevent/getmodifierstate(_:))
- [func initKeyboardEvent(String!, canBubble: Bool, cancelable: Bool, view: DOMAbstractView!, keyIdentifier: String!, location: UInt32, ctrlKey: Bool, altKey: Bool, shiftKey: Bool, metaKey: Bool)](/documentation/webkit/domkeyboardevent/initkeyboardevent(_:canbubble:cancelable:view:keyidentifier:location:ctrlkey:altkey:shiftkey:metakey:))
- [func initKeyboardEvent(String!, canBubble: Bool, cancelable: Bool, view: DOMAbstractView!, keyIdentifier: String!, location: UInt32, ctrlKey: Bool, altKey: Bool, shiftKey: Bool, metaKey: Bool, altGraphKey: Bool)](/documentation/webkit/domkeyboardevent/initkeyboardevent(_:canbubble:cancelable:view:keyidentifier:location:ctrlkey:altkey:shiftkey:metakey:altgraphkey:))
- [DOMMediaList](/documentation/webkit/dommedialist)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/dommedialist/length)
- [var mediaText: String!](/documentation/webkit/dommedialist/mediatext)

###### Instance Methods

- [func appendMedium(String!)](/documentation/webkit/dommedialist/appendmedium(_:))
- [func deleteMedium(String!)](/documentation/webkit/dommedialist/deletemedium(_:))
- [func item(UInt32) -> String!](/documentation/webkit/dommedialist/item(_:))
- [DOMMouseEvent](/documentation/webkit/dommouseevent)

###### Instance Properties

- [var altKey: Bool](/documentation/webkit/dommouseevent/altkey)
- [var button: Int16](/documentation/webkit/dommouseevent/button)
- [var clientX: Int32](/documentation/webkit/dommouseevent/clientx)
- [var clientY: Int32](/documentation/webkit/dommouseevent/clienty)
- [var ctrlKey: Bool](/documentation/webkit/dommouseevent/ctrlkey)
- [var fromElement: DOMNode!](/documentation/webkit/dommouseevent/fromelement)
- [var metaKey: Bool](/documentation/webkit/dommouseevent/metakey)
- [var offsetX: Int32](/documentation/webkit/dommouseevent/offsetx)
- [var offsetY: Int32](/documentation/webkit/dommouseevent/offsety)
- [var relatedTarget: (any DOMEventTarget)!](/documentation/webkit/dommouseevent/relatedtarget)
- [var screenX: Int32](/documentation/webkit/dommouseevent/screenx)
- [var screenY: Int32](/documentation/webkit/dommouseevent/screeny)
- [var shiftKey: Bool](/documentation/webkit/dommouseevent/shiftkey)
- [var toElement: DOMNode!](/documentation/webkit/dommouseevent/toelement)
- [var x: Int32](/documentation/webkit/dommouseevent/x)
- [var y: Int32](/documentation/webkit/dommouseevent/y)

###### Instance Methods

- [func initMouseEvent(String!, canBubble: Bool, cancelable: Bool, view: DOMAbstractView!, detail: Int32, screenX: Int32, screenY: Int32, clientX: Int32, clientY: Int32, ctrlKey: Bool, altKey: Bool, shiftKey: Bool, metaKey: Bool, button: UInt16, relatedTarget: (any DOMEventTarget)!)](/documentation/webkit/dommouseevent/initmouseevent(_:canbubble:cancelable:view:detail:screenx:screeny:clientx:clienty:ctrlkey:altkey:shiftkey:metakey:button:relatedtarget:))
- [DOMMutationEvent](/documentation/webkit/dommutationevent)

###### Instance Properties

- [var attrChange: UInt16](/documentation/webkit/dommutationevent/attrchange)
- [var attrName: String!](/documentation/webkit/dommutationevent/attrname)
- [var newValue: String!](/documentation/webkit/dommutationevent/newvalue)
- [var prevValue: String!](/documentation/webkit/dommutationevent/prevvalue)
- [var relatedNode: DOMNode!](/documentation/webkit/dommutationevent/relatednode)

###### Instance Methods

- [func initMutationEvent(String!, canBubble: Bool, cancelable: Bool, relatedNode: DOMNode!, prevValue: String!, newValue: String!, attrName: String!, attrChange: UInt16)](/documentation/webkit/dommutationevent/initmutationevent(_:canbubble:cancelable:relatednode:prevvalue:newvalue:attrname:attrchange:))
- [DOMNamedNodeMap](/documentation/webkit/domnamednodemap)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domnamednodemap/length)

###### Instance Methods

- [func getNamedItem(String!) -> DOMNode!](/documentation/webkit/domnamednodemap/getnameditem(_:))
- [func getNamedItemNS(String!, localName: String!) -> DOMNode!](/documentation/webkit/domnamednodemap/getnameditemns(_:localname:))
- [func item(UInt32) -> DOMNode!](/documentation/webkit/domnamednodemap/item(_:))
- [func removeNamedItem(String!) -> DOMNode!](/documentation/webkit/domnamednodemap/removenameditem(_:))
- [func removeNamedItemNS(String!, localName: String!) -> DOMNode!](/documentation/webkit/domnamednodemap/removenameditemns(_:localname:))
- [func setNamedItem(DOMNode!) -> DOMNode!](/documentation/webkit/domnamednodemap/setnameditem(_:))
- [func setNamedItemNS(DOMNode!) -> DOMNode!](/documentation/webkit/domnamednodemap/setnameditemns(_:))
- [DOMNode](/documentation/webkit/domnode)

###### Instance Properties

- [var attributes: DOMNamedNodeMap!](/documentation/webkit/domnode/attributes)
- [var baseURI: String!](/documentation/webkit/domnode/baseuri)
- [var childNodes: DOMNodeList!](/documentation/webkit/domnode/childnodes)
- [var firstChild: DOMNode!](/documentation/webkit/domnode/firstchild)
- [var isContentEditable: Bool](/documentation/webkit/domnode/iscontenteditable)
- [var lastChild: DOMNode!](/documentation/webkit/domnode/lastchild)
- [var localName: String!](/documentation/webkit/domnode/localname)
- [var namespaceURI: String!](/documentation/webkit/domnode/namespaceuri)
- [var nextSibling: DOMNode!](/documentation/webkit/domnode/nextsibling)
- [var nodeName: String!](/documentation/webkit/domnode/nodename)
- [var nodeType: UInt16](/documentation/webkit/domnode/nodetype)
- [var nodeValue: String!](/documentation/webkit/domnode/nodevalue)
- [var ownerDocument: DOMDocument!](/documentation/webkit/domnode/ownerdocument)
- [var parent: DOMNode!](/documentation/webkit/domnode/parent)
- [var parentElement: DOMElement!](/documentation/webkit/domnode/parentelement)
- [var prefix: String!](/documentation/webkit/domnode/prefix)
- [var previousSibling: DOMNode!](/documentation/webkit/domnode/previoussibling)
- [var textContent: String!](/documentation/webkit/domnode/textcontent)
- [var webArchive: WebArchive!](/documentation/webkit/domnode/webarchive)

###### Instance Methods

- [func appendChild(DOMNode!) -> DOMNode!](/documentation/webkit/domnode/appendchild(_:))
- [func boundingBox() -> NSRect](/documentation/webkit/domnode/boundingbox())
- [func cloneNode(Bool) -> DOMNode!](/documentation/webkit/domnode/clonenode(_:))
- [func compareDocumentPosition(DOMNode!) -> UInt16](/documentation/webkit/domnode/comparedocumentposition(_:))
- [func contains(DOMNode!) -> Bool](/documentation/webkit/domnode/contains(_:))
- [func hasAttributes() -> Bool](/documentation/webkit/domnode/hasattributes())
- [func hasChildNodes() -> Bool](/documentation/webkit/domnode/haschildnodes())
- [func insert(before: DOMNode!, refChild: DOMNode!) -> DOMNode!](/documentation/webkit/domnode/insert(before:refchild:))
- [func isDefaultNamespace(String!) -> Bool](/documentation/webkit/domnode/isdefaultnamespace(_:))
- [func isEqualNode(DOMNode!) -> Bool](/documentation/webkit/domnode/isequalnode(_:))
- [func isSameNode(DOMNode!) -> Bool](/documentation/webkit/domnode/issamenode(_:))
- [func isSupported(String!, version: String!) -> Bool](/documentation/webkit/domnode/issupported(_:version:))
- [func lineBoxRects() -> [Any]!](/documentation/webkit/domnode/lineboxrects())
- [func lookupNamespaceURI(String!) -> String!](/documentation/webkit/domnode/lookupnamespaceuri(_:))
- [func lookupPrefix(String!) -> String!](/documentation/webkit/domnode/lookupprefix(_:))
- [func normalize()](/documentation/webkit/domnode/normalize())
- [func removeChild(DOMNode!) -> DOMNode!](/documentation/webkit/domnode/removechild(_:))
- [func replaceChild(DOMNode!, oldChild: DOMNode!) -> DOMNode!](/documentation/webkit/domnode/replacechild(_:oldchild:))
- [DOMNodeIterator](/documentation/webkit/domnodeiterator)

###### Instance Properties

- [var expandEntityReferences: Bool](/documentation/webkit/domnodeiterator/expandentityreferences)
- [var filter: (any DOMNodeFilter)!](/documentation/webkit/domnodeiterator/filter)
- [var pointerBeforeReferenceNode: Bool](/documentation/webkit/domnodeiterator/pointerbeforereferencenode)
- [var referenceNode: DOMNode!](/documentation/webkit/domnodeiterator/referencenode)
- [var root: DOMNode!](/documentation/webkit/domnodeiterator/root)
- [var whatToShow: UInt32](/documentation/webkit/domnodeiterator/whattoshow)

###### Instance Methods

- [func detach()](/documentation/webkit/domnodeiterator/detach())
- [func nextNode() -> DOMNode!](/documentation/webkit/domnodeiterator/nextnode())
- [func previousNode() -> DOMNode!](/documentation/webkit/domnodeiterator/previousnode())
- [DOMNodeList](/documentation/webkit/domnodelist)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domnodelist/length)

###### Instance Methods

- [func item(UInt32) -> DOMNode!](/documentation/webkit/domnodelist/item(_:))
- [DOMObject](/documentation/webkit/domobject)

###### Instance Properties

- [var sheet: DOMStyleSheet!](/documentation/webkit/domobject/sheet)
- [DOMOverflowEvent](/documentation/webkit/domoverflowevent)

###### Instance Properties

- [var horizontalOverflow: Bool](/documentation/webkit/domoverflowevent/horizontaloverflow)
- [var orient: UInt16](/documentation/webkit/domoverflowevent/orient)
- [var verticalOverflow: Bool](/documentation/webkit/domoverflowevent/verticaloverflow)

###### Instance Methods

- [func initOverflowEvent(UInt16, horizontalOverflow: Bool, verticalOverflow: Bool)](/documentation/webkit/domoverflowevent/initoverflowevent(_:horizontaloverflow:verticaloverflow:))
- [DOMProcessingInstruction](/documentation/webkit/domprocessinginstruction)

###### Instance Properties

- [var sheet: DOMStyleSheet!](/documentation/webkit/domprocessinginstruction/sheet)
- [var target: String!](/documentation/webkit/domprocessinginstruction/target)
- [DOMProgressEvent](/documentation/webkit/domprogressevent)

###### Instance Properties

- [var lengthComputable: Bool](/documentation/webkit/domprogressevent/lengthcomputable)
- [var loaded: UInt64](/documentation/webkit/domprogressevent/loaded)
- [var total: UInt64](/documentation/webkit/domprogressevent/total)
- [DOMRange](/documentation/webkit/domrange)

###### Instance Properties

- [var collapsed: Bool](/documentation/webkit/domrange/collapsed)
- [var commonAncestorContainer: DOMNode!](/documentation/webkit/domrange/commonancestorcontainer)
- [var endContainer: DOMNode!](/documentation/webkit/domrange/endcontainer)
- [var endOffset: Int32](/documentation/webkit/domrange/endoffset)
- [var markupString: String!](/documentation/webkit/domrange/markupstring)
- [var startContainer: DOMNode!](/documentation/webkit/domrange/startcontainer)
- [var startOffset: Int32](/documentation/webkit/domrange/startoffset)
- [var text: String!](/documentation/webkit/domrange/text)
- [var webArchive: WebArchive!](/documentation/webkit/domrange/webarchive)

###### Instance Methods

- [func clone() -> DOMRange!](/documentation/webkit/domrange/clone())
- [func cloneContents() -> DOMDocumentFragment!](/documentation/webkit/domrange/clonecontents())
- [func collapse(Bool)](/documentation/webkit/domrange/collapse(_:))
- [func compare(DOMNode!) -> Int16](/documentation/webkit/domrange/compare(_:))
- [func compareBoundaryPoints(UInt16, sourceRange: DOMRange!) -> Int16](/documentation/webkit/domrange/compareboundarypoints(_:sourcerange:))
- [func comparePoint(DOMNode!, offset: Int32) -> Int16](/documentation/webkit/domrange/comparepoint(_:offset:))
- [func createContextualFragment(String!) -> DOMDocumentFragment!](/documentation/webkit/domrange/createcontextualfragment(_:))
- [func deleteContents()](/documentation/webkit/domrange/deletecontents())
- [func detach()](/documentation/webkit/domrange/detach())
- [func extractContents() -> DOMDocumentFragment!](/documentation/webkit/domrange/extractcontents())
- [func insert(DOMNode!)](/documentation/webkit/domrange/insert(_:))
- [func intersects(DOMNode!) -> Bool](/documentation/webkit/domrange/intersects(_:))
- [func isPoint(inRange: DOMNode!, offset: Int32) -> Bool](/documentation/webkit/domrange/ispoint(inrange:offset:))
- [func select(DOMNode!)](/documentation/webkit/domrange/select(_:))
- [func selectNodeContents(DOMNode!)](/documentation/webkit/domrange/selectnodecontents(_:))
- [func setEnd(DOMNode!, offset: Int32)](/documentation/webkit/domrange/setend(_:offset:))
- [func setEndAfter(DOMNode!)](/documentation/webkit/domrange/setendafter(_:))
- [func setEndBefore(DOMNode!)](/documentation/webkit/domrange/setendbefore(_:))
- [func setStart(DOMNode!, offset: Int32)](/documentation/webkit/domrange/setstart(_:offset:))
- [func setStartAfter(DOMNode!)](/documentation/webkit/domrange/setstartafter(_:))
- [func setStartBefore(DOMNode!)](/documentation/webkit/domrange/setstartbefore(_:))
- [func surroundContents(DOMNode!)](/documentation/webkit/domrange/surroundcontents(_:))
- [func toString() -> String!](/documentation/webkit/domrange/tostring())
- [DOMRect](/documentation/webkit/domrect)

###### Instance Properties

- [var bottom: DOMCSSPrimitiveValue!](/documentation/webkit/domrect/bottom)
- [var left: DOMCSSPrimitiveValue!](/documentation/webkit/domrect/left)
- [var right: DOMCSSPrimitiveValue!](/documentation/webkit/domrect/right)
- [var top: DOMCSSPrimitiveValue!](/documentation/webkit/domrect/top)
- [DOMRGBColor](/documentation/webkit/domrgbcolor)

###### Instance Properties

- [var alpha: DOMCSSPrimitiveValue!](/documentation/webkit/domrgbcolor/alpha)
- [var blue: DOMCSSPrimitiveValue!](/documentation/webkit/domrgbcolor/blue)
- [var color: NSColor!](/documentation/webkit/domrgbcolor/color)
- [var green: DOMCSSPrimitiveValue!](/documentation/webkit/domrgbcolor/green)
- [var red: DOMCSSPrimitiveValue!](/documentation/webkit/domrgbcolor/red)
- [DOMStyleSheet](/documentation/webkit/domstylesheet)

###### Instance Properties

- [var disabled: Bool](/documentation/webkit/domstylesheet/disabled)
- [var href: String!](/documentation/webkit/domstylesheet/href)
- [var media: DOMMediaList!](/documentation/webkit/domstylesheet/media)
- [var ownerNode: DOMNode!](/documentation/webkit/domstylesheet/ownernode)
- [var parent: DOMStyleSheet!](/documentation/webkit/domstylesheet/parent)
- [var title: String!](/documentation/webkit/domstylesheet/title)
- [var type: String!](/documentation/webkit/domstylesheet/type)
- [DOMStyleSheetList](/documentation/webkit/domstylesheetlist)

###### Instance Properties

- [var length: UInt32](/documentation/webkit/domstylesheetlist/length)

###### Instance Methods

- [func item(UInt32) -> DOMStyleSheet!](/documentation/webkit/domstylesheetlist/item(_:))
- [DOMText](/documentation/webkit/domtext)

###### Instance Properties

- [var wholeText: String!](/documentation/webkit/domtext/wholetext)

###### Instance Methods

- [func replaceWholeText(String!) -> DOMText!](/documentation/webkit/domtext/replacewholetext(_:))
- [func splitText(UInt32) -> DOMText!](/documentation/webkit/domtext/splittext(_:))
- [DOMTreeWalker](/documentation/webkit/domtreewalker)

###### Instance Properties

- [var currentNode: DOMNode!](/documentation/webkit/domtreewalker/currentnode)
- [var expandEntityReferences: Bool](/documentation/webkit/domtreewalker/expandentityreferences)
- [var filter: (any DOMNodeFilter)!](/documentation/webkit/domtreewalker/filter)
- [var root: DOMNode!](/documentation/webkit/domtreewalker/root)
- [var whatToShow: UInt32](/documentation/webkit/domtreewalker/whattoshow)

###### Instance Methods

- [func firstChild() -> DOMNode!](/documentation/webkit/domtreewalker/firstchild())
- [func lastChild() -> DOMNode!](/documentation/webkit/domtreewalker/lastchild())
- [func nextNode() -> DOMNode!](/documentation/webkit/domtreewalker/nextnode())
- [func nextSibling() -> DOMNode!](/documentation/webkit/domtreewalker/nextsibling())
- [func parentNode() -> DOMNode!](/documentation/webkit/domtreewalker/parentnode())
- [func previousNode() -> DOMNode!](/documentation/webkit/domtreewalker/previousnode())
- [func previousSibling() -> DOMNode!](/documentation/webkit/domtreewalker/previoussibling())
- [DOMUIEvent](/documentation/webkit/domuievent)

###### Instance Properties

- [var charCode: Int32](/documentation/webkit/domuievent/charcode)
- [var detail: Int32](/documentation/webkit/domuievent/detail)
- [var keyCode: Int32](/documentation/webkit/domuievent/keycode)
- [var pageX: Int32](/documentation/webkit/domuievent/pagex)
- [var pageY: Int32](/documentation/webkit/domuievent/pagey)
- [var view: DOMAbstractView!](/documentation/webkit/domuievent/view)
- [var which: Int32](/documentation/webkit/domuievent/which)

###### Instance Methods

- [func initUIEvent(String!, canBubble: Bool, cancelable: Bool, view: DOMAbstractView!, detail: Int32)](/documentation/webkit/domuievent/inituievent(_:canbubble:cancelable:view:detail:))
- [DOMWheelEvent](/documentation/webkit/domwheelevent)

###### Instance Properties

- [var isHorizontal: Bool](/documentation/webkit/domwheelevent/ishorizontal)
- [var wheelDelta: Int32](/documentation/webkit/domwheelevent/wheeldelta)
- [var wheelDeltaX: Int32](/documentation/webkit/domwheelevent/wheeldeltax)
- [var wheelDeltaY: Int32](/documentation/webkit/domwheelevent/wheeldeltay)

###### Instance Methods

- [func initWheelEvent(Int32, wheelDeltaY: Int32, view: DOMAbstractView!, screenX: Int32, screenY: Int32, clientX: Int32, clientY: Int32, ctrlKey: Bool, altKey: Bool, shiftKey: Bool, metaKey: Bool)](/documentation/webkit/domwheelevent/initwheelevent(_:wheeldeltay:view:screenx:screeny:clientx:clienty:ctrlkey:altkey:shiftkey:metakey:))
- [DOMXPathExpression](/documentation/webkit/domxpathexpression)

###### Instance Methods

- [func evaluate(DOMNode!, type: UInt16, in: DOMXPathResult!) -> DOMXPathResult!](/documentation/webkit/domxpathexpression/evaluate(_:type:in:))
- [DOMXPathResult](/documentation/webkit/domxpathresult)

###### Instance Properties

- [var booleanValue: Bool](/documentation/webkit/domxpathresult/booleanvalue)
- [var invalidIteratorState: Bool](/documentation/webkit/domxpathresult/invaliditeratorstate)
- [var numberValue: Double](/documentation/webkit/domxpathresult/numbervalue)
- [var resultType: UInt16](/documentation/webkit/domxpathresult/resulttype)
- [var singleNodeValue: DOMNode!](/documentation/webkit/domxpathresult/singlenodevalue)
- [var snapshotLength: UInt32](/documentation/webkit/domxpathresult/snapshotlength)
- [var stringValue: String!](/documentation/webkit/domxpathresult/stringvalue)

###### Instance Methods

- [func iterateNext() -> DOMNode!](/documentation/webkit/domxpathresult/iteratenext())
- [func snapshotItem(UInt32) -> DOMNode!](/documentation/webkit/domxpathresult/snapshotitem(_:))
- [DOMEventListener](/documentation/webkit/domeventlistener)

###### Instance Methods

- [func handle(DOMEvent!)](/documentation/webkit/domeventlistener/handle(_:))
- [DOMEventTarget](/documentation/webkit/domeventtarget)

###### Instance Methods

- [func addEventListener(String!, listener: (any DOMEventListener)!, useCapture: Bool)](/documentation/webkit/domeventtarget/addeventlistener(_:listener:usecapture:))
- [func dispatchEvent(DOMEvent!) -> Bool](/documentation/webkit/domeventtarget/dispatchevent(_:))
- [func removeEventListener(String!, listener: (any DOMEventListener)!, useCapture: Bool)](/documentation/webkit/domeventtarget/removeeventlistener(_:listener:usecapture:))
- [DOMNodeFilter](/documentation/webkit/domnodefilter)

###### Instance Methods

- [func accept(DOMNode!) -> Int16](/documentation/webkit/domnodefilter/accept(_:))
- [DOMXPathNSResolver](/documentation/webkit/domxpathnsresolver)

###### Instance Methods

- [func lookupNamespaceURI(String!) -> String!](/documentation/webkit/domxpathnsresolver/lookupnamespaceuri(_:))
- [DOMDocument Additions](/documentation/webkit/domdocument-additions)

###### Getting the web frame

- [var webFrame: WebFrame!](/documentation/webkit/domdocument/webframe)

###### Constructing URLs

- [func url(withAttributeString: String!) -> URL!](/documentation/webkit/domdocument/url(withattributestring:))
- [DOMElement Additions](/documentation/webkit/domelement-additions)

###### Getting Properties

- [func image() -> NSImage!](/documentation/webkit/domelement/image())
- [DOMHTMLDocument Additions](/documentation/webkit/domhtmldocument-additions)

###### Creating Document Fragments

- [func createDocumentFragment(withMarkupString: String!, baseURL: URL!) -> DOMDocumentFragment!](/documentation/webkit/domhtmldocument/createdocumentfragment(withmarkupstring:baseurl:))
- [func createDocumentFragment(withText: String!) -> DOMDocumentFragment!](/documentation/webkit/domhtmldocument/createdocumentfragment(withtext:))
- [DOMHTMLFrameElement Additions](/documentation/webkit/domhtmlframeelement-additions)

###### Getting the Content Frame

- [var contentFrame: WebFrame!](/documentation/webkit/domhtmlframeelement/contentframe)
- [DOMHTMLIFrameElement Additions](/documentation/webkit/domhtmliframeelement-additions)

###### Getting the Content Frame

- [var contentFrame: WebFrame!](/documentation/webkit/domhtmliframeelement/contentframe)
- [DOMHTMLObjectElement Additions](/documentation/webkit/domhtmlobjectelement-additions)

###### Getting the content frame

- [var contentFrame: WebFrame!](/documentation/webkit/domhtmlobjectelement/contentframe)
- [DOMNode Additions](/documentation/webkit/domnode-additions)

###### Creating archives

- [var webArchive: WebArchive!](/documentation/webkit/domnode/webarchive)

###### Obtaining layout rectangles

- [func boundingBox() -> NSRect](/documentation/webkit/domnode/boundingbox())
- [func lineBoxRects() -> [Any]!](/documentation/webkit/domnode/lineboxrects())
- [DOMRange Additions](/documentation/webkit/domrange-additions)

###### Creating archives

- [var webArchive: WebArchive!](/documentation/webkit/domrange/webarchive)

###### Formatting content ranges

- [var markupString: String!](/documentation/webkit/domrange/markupstring)
- [WebKit Constants](/documentation/webkit/webkit-constants)

###### WKPreview Constants

- [let WKPreviewActionItemIdentifierAddToReadingList: String](/documentation/webkit/wkpreviewactionitemidentifieraddtoreadinglist)
- [let WKPreviewActionItemIdentifierCopy: String](/documentation/webkit/wkpreviewactionitemidentifiercopy)
- [let WKPreviewActionItemIdentifierOpen: String](/documentation/webkit/wkpreviewactionitemidentifieropen)
- [let WKPreviewActionItemIdentifierShare: String](/documentation/webkit/wkpreviewactionitemidentifiershare)

###### WKWebsiteDataType Constants

- [let WKWebsiteDataTypeCookies: String](/documentation/webkit/wkwebsitedatatypecookies)
- [let WKWebsiteDataTypeDiskCache: String](/documentation/webkit/wkwebsitedatatypediskcache)
- [let WKWebsiteDataTypeIndexedDBDatabases: String](/documentation/webkit/wkwebsitedatatypeindexeddbdatabases)
- [let WKWebsiteDataTypeLocalStorage: String](/documentation/webkit/wkwebsitedatatypelocalstorage)
- [let WKWebsiteDataTypeMemoryCache: String](/documentation/webkit/wkwebsitedatatypememorycache)
- [let WKWebsiteDataTypeOfflineWebApplicationCache: String](/documentation/webkit/wkwebsitedatatypeofflinewebapplicationcache)
- [let WKWebsiteDataTypeSessionStorage: String](/documentation/webkit/wkwebsitedatatypesessionstorage)
- [let WKWebsiteDataTypeWebSQLDatabases: String](/documentation/webkit/wkwebsitedatatypewebsqldatabases)

###### DOM Constants

- [let DOMEventException: String](/documentation/webkit/domeventexception)
- [let DOMException: String](/documentation/webkit/domexception)
- [let DOMRangeException: String](/documentation/webkit/domrangeexception)
- [let DOMXPathException: String](/documentation/webkit/domxpathexception)
- [var DOM_BAD_BOUNDARYPOINTS_ERR: DOMRangeExceptionCode](/documentation/webkit/dom_bad_boundarypoints_err)
- [var DOM_DOMSTRING_SIZE_ERR: DOMExceptionCode](/documentation/webkit/dom_domstring_size_err)
- [var DOM_HIERARCHY_REQUEST_ERR: DOMExceptionCode](/documentation/webkit/dom_hierarchy_request_err)
- [var DOM_INDEX_SIZE_ERR: DOMExceptionCode](/documentation/webkit/dom_index_size_err)
- [var DOM_INUSE_ATTRIBUTE_ERR: DOMExceptionCode](/documentation/webkit/dom_inuse_attribute_err)
- [var DOM_INVALID_ACCESS_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_access_err)
- [var DOM_INVALID_CHARACTER_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_character_err)
- [var DOM_INVALID_EXPRESSION_ERR: DOMXPathExceptionCode](/documentation/webkit/dom_invalid_expression_err)
- [var DOM_INVALID_MODIFICATION_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_modification_err)
- [var DOM_INVALID_NODE_TYPE_ERR: DOMRangeExceptionCode](/documentation/webkit/dom_invalid_node_type_err)
- [var DOM_INVALID_STATE_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_state_err)
- [var DOM_NAMESPACE_ERR: DOMExceptionCode](/documentation/webkit/dom_namespace_err)
- [var DOM_NOT_FOUND_ERR: DOMExceptionCode](/documentation/webkit/dom_not_found_err)
- [var DOM_NOT_SUPPORTED_ERR: DOMExceptionCode](/documentation/webkit/dom_not_supported_err)
- [var DOM_NO_DATA_ALLOWED_ERR: DOMExceptionCode](/documentation/webkit/dom_no_data_allowed_err)
- [var DOM_NO_MODIFICATION_ALLOWED_ERR: DOMExceptionCode](/documentation/webkit/dom_no_modification_allowed_err)
- [var DOM_SYNTAX_ERR: DOMExceptionCode](/documentation/webkit/dom_syntax_err)
- [var DOM_TYPE_ERR: DOMXPathExceptionCode](/documentation/webkit/dom_type_err)
- [var DOM_UNSPECIFIED_EVENT_TYPE_ERR: DOMEventExceptionCode](/documentation/webkit/dom_unspecified_event_type_err)
- [var DOM_WRONG_DOCUMENT_ERR: DOMExceptionCode](/documentation/webkit/dom_wrong_document_err)

###### WebKit Constants (Legacy)

- [let WebActionButtonKey: String](/documentation/webkit/webactionbuttonkey)
- [let WebActionElementKey: String](/documentation/webkit/webactionelementkey)
- [let WebActionModifierFlagsKey: String](/documentation/webkit/webactionmodifierflagskey)
- [let WebActionNavigationTypeKey: String](/documentation/webkit/webactionnavigationtypekey)
- [let WebActionOriginalURLKey: String](/documentation/webkit/webactionoriginalurlkey)
- [let WebArchivePboardType: String](/documentation/webkit/webarchivepboardtype)
- [let WebElementDOMNodeKey: String](/documentation/webkit/webelementdomnodekey)
- [let WebElementFrameKey: String](/documentation/webkit/webelementframekey)
- [let WebElementImageAltStringKey: String](/documentation/webkit/webelementimagealtstringkey)
- [let WebElementImageKey: String](/documentation/webkit/webelementimagekey)
- [let WebElementImageRectKey: String](/documentation/webkit/webelementimagerectkey)
- [let WebElementImageURLKey: String](/documentation/webkit/webelementimageurlkey)
- [let WebElementIsSelectedKey: String](/documentation/webkit/webelementisselectedkey)
- [let WebElementLinkLabelKey: String](/documentation/webkit/webelementlinklabelkey)
- [let WebElementLinkTargetFrameKey: String](/documentation/webkit/webelementlinktargetframekey)
- [let WebElementLinkTitleKey: String](/documentation/webkit/webelementlinktitlekey)
- [let WebElementLinkURLKey: String](/documentation/webkit/webelementlinkurlkey)
- [static let WebHistoryAllItemsRemoved: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryallitemsremoved)
- [static let WebHistoryItemChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryitemchanged)
- [static let WebHistoryItemsAdded: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryitemsadded)
- [let WebHistoryItemsKey: String](/documentation/webkit/webhistoryitemskey)
- [static let WebHistoryItemsRemoved: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryitemsremoved)
- [static let WebHistoryLoaded: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryloaded)
- [static let WebHistorySaved: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistorysaved)
- [let WebKitErrorDomain: String](/documentation/webkit/webkiterrordomain)
- [let WebKitErrorMIMETypeKey: String](/documentation/webkit/webkiterrormimetypekey)
- [let WebKitErrorPlugInNameKey: String](/documentation/webkit/webkiterrorpluginnamekey)
- [let WebKitErrorPlugInPageURLStringKey: String](/documentation/webkit/webkiterrorpluginpageurlstringkey)
- [let WebPlugInAttributesKey: String](/documentation/webkit/webpluginattributeskey)
- [let WebPlugInBaseURLKey: String](/documentation/webkit/webpluginbaseurlkey)
- [let WebPlugInContainerKey: String](/documentation/webkit/webplugincontainerkey)
- [let WebPlugInContainingElementKey: String](/documentation/webkit/webplugincontainingelementkey)
- [let WebPlugInShouldLoadMainResourceKey: String](/documentation/webkit/webpluginshouldloadmainresourcekey)
- [static let WebPreferencesChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webpreferenceschanged)
- [static let WebViewDidBeginEditing: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidbeginediting)
- [static let WebViewDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchange)
- [static let WebViewDidChangeSelection: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchangeselection)
- [static let WebViewDidChangeTypingStyle: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchangetypingstyle)
- [static let WebViewDidEndEditing: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidendediting)
- [static let WebViewProgressEstimateChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressestimatechanged)
- [static let WebViewProgressFinished: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressfinished)
- [static let WebViewProgressStarted: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressstarted)

###### Constants

- [let WKErrorDomain: String](/documentation/webkit/wkerrordomain)
- [let WKWebsiteDataTypeFetchCache: String](/documentation/webkit/wkwebsitedatatypefetchcache)
- [let WKWebsiteDataTypeFileSystem: String](/documentation/webkit/wkwebsitedatatypefilesystem)
- [let WKWebsiteDataTypeHashSalt: String](/documentation/webkit/wkwebsitedatatypehashsalt)
- [let WKWebsiteDataTypeMediaKeys: String](/documentation/webkit/wkwebsitedatatypemediakeys)
- [let WKWebsiteDataTypeSearchFieldRecentSearches: String](/documentation/webkit/wkwebsitedatatypesearchfieldrecentsearches)
- [let WKWebsiteDataTypeServiceWorkerRegistrations: String](/documentation/webkit/wkwebsitedatatypeserviceworkerregistrations)

##### Enumerations

- [DOM Rule Enumeration (Legacy)](/documentation/webkit/1403866-dom-rule-enumeration-legacy)

###### Constants

- [var DOM_CHARSET_RULE: Int](/documentation/webkit/dom_charset_rule)
- [var DOM_FONT_FACE_RULE: Int](/documentation/webkit/dom_font_face_rule)
- [var DOM_IMPORT_RULE: Int](/documentation/webkit/dom_import_rule)
- [var DOM_KEYFRAMES_RULE: Int](/documentation/webkit/dom_keyframes_rule)
- [var DOM_KEYFRAME_RULE: Int](/documentation/webkit/dom_keyframe_rule)
- [var DOM_MEDIA_RULE: Int](/documentation/webkit/dom_media_rule)
- [var DOM_PAGE_RULE: Int](/documentation/webkit/dom_page_rule)
- [var DOM_STYLE_RULE: Int](/documentation/webkit/dom_style_rule)
- [var DOM_SUPPORTS_RULE: Int](/documentation/webkit/dom_supports_rule)
- [var DOM_UNKNOWN_RULE: Int](/documentation/webkit/dom_unknown_rule)
- [var DOM_WEBKIT_KEYFRAMES_RULE: Int](/documentation/webkit/dom_webkit_keyframes_rule)
- [var DOM_WEBKIT_KEYFRAME_RULE: Int](/documentation/webkit/dom_webkit_keyframe_rule)
- [var DOM_WEBKIT_REGION_RULE: Int](/documentation/webkit/dom_webkit_region_rule)
- [var DOM_NAMESPACE_RULE: Int](/documentation/webkit/dom_namespace_rule)
- [DOM Alignment Enumeration (Legacy)](/documentation/webkit/1574395-dom-alignment-enumeration-legacy)

###### Constants

- [var DOM_BOTH: Int](/documentation/webkit/dom_both)
- [var DOM_HORIZONTAL: Int](/documentation/webkit/dom_horizontal)
- [var DOM_VERTICAL: Int](/documentation/webkit/dom_vertical)
- [DOM Measurement Enumeration (Legacy)](/documentation/webkit/1418446-dom-measurement-enumeration-lega)

###### Constants

- [var DOM_CSS_ATTR: Int](/documentation/webkit/dom_css_attr)
- [var DOM_CSS_CM: Int](/documentation/webkit/dom_css_cm)
- [var DOM_CSS_COUNTER: Int](/documentation/webkit/dom_css_counter)
- [var DOM_CSS_DEG: Int](/documentation/webkit/dom_css_deg)
- [var DOM_CSS_DIMENSION: Int](/documentation/webkit/dom_css_dimension)
- [var DOM_CSS_EMS: Int](/documentation/webkit/dom_css_ems)
- [var DOM_CSS_EXS: Int](/documentation/webkit/dom_css_exs)
- [var DOM_CSS_GRAD: Int](/documentation/webkit/dom_css_grad)
- [var DOM_CSS_HZ: Int](/documentation/webkit/dom_css_hz)
- [var DOM_CSS_IDENT: Int](/documentation/webkit/dom_css_ident)
- [var DOM_CSS_IN: Int](/documentation/webkit/dom_css_in)
- [var DOM_CSS_KHZ: Int](/documentation/webkit/dom_css_khz)
- [var DOM_CSS_MM: Int](/documentation/webkit/dom_css_mm)
- [var DOM_CSS_MS: Int](/documentation/webkit/dom_css_ms)
- [var DOM_CSS_NUMBER: Int](/documentation/webkit/dom_css_number)
- [var DOM_CSS_PC: Int](/documentation/webkit/dom_css_pc)
- [var DOM_CSS_PERCENTAGE: Int](/documentation/webkit/dom_css_percentage)
- [var DOM_CSS_PT: Int](/documentation/webkit/dom_css_pt)
- [var DOM_CSS_PX: Int](/documentation/webkit/dom_css_px)
- [var DOM_CSS_RAD: Int](/documentation/webkit/dom_css_rad)
- [var DOM_CSS_RECT: Int](/documentation/webkit/dom_css_rect)
- [var DOM_CSS_RGBCOLOR: Int](/documentation/webkit/dom_css_rgbcolor)
- [var DOM_CSS_S: Int](/documentation/webkit/dom_css_s)
- [var DOM_CSS_STRING: Int](/documentation/webkit/dom_css_string)
- [var DOM_CSS_UNKNOWN: Int](/documentation/webkit/dom_css_unknown)
- [var DOM_CSS_URI: Int](/documentation/webkit/dom_css_uri)
- [var DOM_CSS_VH: Int](/documentation/webkit/dom_css_vh)
- [var DOM_CSS_VMAX: Int](/documentation/webkit/dom_css_vmax)
- [var DOM_CSS_VMIN: Int](/documentation/webkit/dom_css_vmin)
- [var DOM_CSS_VW: Int](/documentation/webkit/dom_css_vw)
- [DOM Location Enumeration  (Legacy)](/documentation/webkit/1476932-dom-location-enumeration-legacy)

###### Constants

- [var DOM_KEY_LOCATION_LEFT: Int](/documentation/webkit/dom_key_location_left)
- [var DOM_KEY_LOCATION_NUMPAD: Int](/documentation/webkit/dom_key_location_numpad)
- [var DOM_KEY_LOCATION_RIGHT: Int](/documentation/webkit/dom_key_location_right)
- [var DOM_KEY_LOCATION_STANDARD: Int](/documentation/webkit/dom_key_location_standard)
- [DOM Filter Enumeration (Legacy)](/documentation/webkit/1455659-dom-filter-enumeration-legacy)

###### Constants

- [var DOM_FILTER_ACCEPT: UInt32](/documentation/webkit/dom_filter_accept)
- [var DOM_FILTER_REJECT: UInt32](/documentation/webkit/dom_filter_reject)
- [var DOM_FILTER_SKIP: UInt32](/documentation/webkit/dom_filter_skip)
- [var DOM_SHOW_ALL: UInt32](/documentation/webkit/dom_show_all)
- [var DOM_SHOW_ATTRIBUTE: UInt32](/documentation/webkit/dom_show_attribute)
- [var DOM_SHOW_CDATA_SECTION: UInt32](/documentation/webkit/dom_show_cdata_section)
- [var DOM_SHOW_COMMENT: UInt32](/documentation/webkit/dom_show_comment)
- [var DOM_SHOW_DOCUMENT: UInt32](/documentation/webkit/dom_show_document)
- [var DOM_SHOW_DOCUMENT_FRAGMENT: UInt32](/documentation/webkit/dom_show_document_fragment)
- [var DOM_SHOW_DOCUMENT_TYPE: UInt32](/documentation/webkit/dom_show_document_type)
- [var DOM_SHOW_ELEMENT: UInt32](/documentation/webkit/dom_show_element)
- [var DOM_SHOW_ENTITY: UInt32](/documentation/webkit/dom_show_entity)
- [var DOM_SHOW_ENTITY_REFERENCE: UInt32](/documentation/webkit/dom_show_entity_reference)
- [var DOM_SHOW_NOTATION: UInt32](/documentation/webkit/dom_show_notation)
- [var DOM_SHOW_PROCESSING_INSTRUCTION: UInt32](/documentation/webkit/dom_show_processing_instruction)
- [var DOM_SHOW_TEXT: UInt32](/documentation/webkit/dom_show_text)
- [DOM Element Enumeration (Legacy)](/documentation/webkit/1517978-dom-element-enumeration-legacy)

###### Constants

- [var DOM_ATTRIBUTE_NODE: Int](/documentation/webkit/dom_attribute_node)
- [var DOM_CDATA_SECTION_NODE: Int](/documentation/webkit/dom_cdata_section_node)
- [var DOM_COMMENT_NODE: Int](/documentation/webkit/dom_comment_node)
- [var DOM_DOCUMENT_FRAGMENT_NODE: Int](/documentation/webkit/dom_document_fragment_node)
- [var DOM_DOCUMENT_NODE: Int](/documentation/webkit/dom_document_node)
- [var DOM_DOCUMENT_POSITION_CONTAINED_BY: Int](/documentation/webkit/dom_document_position_contained_by)
- [var DOM_DOCUMENT_POSITION_CONTAINS: Int](/documentation/webkit/dom_document_position_contains)
- [var DOM_DOCUMENT_POSITION_DISCONNECTED: Int](/documentation/webkit/dom_document_position_disconnected)
- [var DOM_DOCUMENT_POSITION_FOLLOWING: Int](/documentation/webkit/dom_document_position_following)
- [var DOM_DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC: Int](/documentation/webkit/dom_document_position_implementation_specific)
- [var DOM_DOCUMENT_POSITION_PRECEDING: Int](/documentation/webkit/dom_document_position_preceding)
- [var DOM_DOCUMENT_TYPE_NODE: Int](/documentation/webkit/dom_document_type_node)
- [var DOM_ELEMENT_NODE: Int](/documentation/webkit/dom_element_node)
- [var DOM_ENTITY_NODE: Int](/documentation/webkit/dom_entity_node)
- [var DOM_ENTITY_REFERENCE_NODE: Int](/documentation/webkit/dom_entity_reference_node)
- [var DOM_NOTATION_NODE: Int](/documentation/webkit/dom_notation_node)
- [var DOM_PROCESSING_INSTRUCTION_NODE: Int](/documentation/webkit/dom_processing_instruction_node)
- [var DOM_TEXT_NODE: Int](/documentation/webkit/dom_text_node)
- [DOM Modification Enumeration (Legacy)](/documentation/webkit/1393660-dom-modification-enumeration-leg)

###### Constants

- [var DOM_ADDITION: Int](/documentation/webkit/dom_addition)
- [var DOM_MODIFICATION: Int](/documentation/webkit/dom_modification)
- [var DOM_REMOVAL: Int](/documentation/webkit/dom_removal)
- [WebKit Plugin Enumeration (Legacy)](/documentation/webkit/1569747-webkit-plugin-enumeration-legacy)

###### Constants

- [var WebKitErrorBlockedPlugInVersion: Int](/documentation/webkit/webkiterrorblockedpluginversion)
- [var WebKitErrorCannotFindPlugIn: Int](/documentation/webkit/webkiterrorcannotfindplugin)
- [var WebKitErrorCannotLoadPlugIn: Int](/documentation/webkit/webkiterrorcannotloadplugin)
- [var WebKitErrorJavaUnavailable: Int](/documentation/webkit/webkiterrorjavaunavailable)
- [WebKit Loading Fail Enumeration (Legacy)](/documentation/webkit/1569748-webkit-loading-fail-enumeration)

###### Constants

- [var WebKitErrorCannotShowMIMEType: Int](/documentation/webkit/webkiterrorcannotshowmimetype)
- [var WebKitErrorCannotShowURL: Int](/documentation/webkit/webkiterrorcannotshowurl)
- [var WebKitErrorFrameLoadInterruptedByPolicyChange: Int](/documentation/webkit/webkiterrorframeloadinterruptedbypolicychange)
- [DOM Type Enumeration (Legacy)](/documentation/webkit/1538223-dom-type-enumeration-legacy)

###### Constants

- [var DOM_ANY_TYPE: Int](/documentation/webkit/dom_any_type)
- [var DOM_ANY_UNORDERED_NODE_TYPE: Int](/documentation/webkit/dom_any_unordered_node_type)
- [var DOM_BOOLEAN_TYPE: Int](/documentation/webkit/dom_boolean_type)
- [var DOM_FIRST_ORDERED_NODE_TYPE: Int](/documentation/webkit/dom_first_ordered_node_type)
- [var DOM_NUMBER_TYPE: Int](/documentation/webkit/dom_number_type)
- [var DOM_ORDERED_NODE_ITERATOR_TYPE: Int](/documentation/webkit/dom_ordered_node_iterator_type)
- [var DOM_ORDERED_NODE_SNAPSHOT_TYPE: Int](/documentation/webkit/dom_ordered_node_snapshot_type)
- [var DOM_STRING_TYPE: Int](/documentation/webkit/dom_string_type)
- [var DOM_UNORDERED_NODE_ITERATOR_TYPE: Int](/documentation/webkit/dom_unordered_node_iterator_type)
- [var DOM_UNORDERED_NODE_SNAPSHOT_TYPE: Int](/documentation/webkit/dom_unordered_node_snapshot_type)
- [DOM Inheritance Enumeration (Legacy)](/documentation/webkit/1518003-dom-inheritance-enumeration-lega)

###### Constants

- [var DOM_CSS_CUSTOM: Int](/documentation/webkit/dom_css_custom)
- [var DOM_CSS_INHERIT: Int](/documentation/webkit/dom_css_inherit)
- [var DOM_CSS_PRIMITIVE_VALUE: Int](/documentation/webkit/dom_css_primitive_value)
- [var DOM_CSS_VALUE_LIST: Int](/documentation/webkit/dom_css_value_list)
- [DOM Direction Enumeration (Legacy)](/documentation/webkit/1403298-dom-direction-enumeration-legacy)

###### Constants

- [var DOM_END_TO_END: Int](/documentation/webkit/dom_end_to_end)
- [var DOM_END_TO_START: Int](/documentation/webkit/dom_end_to_start)
- [var DOM_NODE_AFTER: Int](/documentation/webkit/dom_node_after)
- [var DOM_NODE_BEFORE: Int](/documentation/webkit/dom_node_before)
- [var DOM_NODE_BEFORE_AND_AFTER: Int](/documentation/webkit/dom_node_before_and_after)
- [var DOM_NODE_INSIDE: Int](/documentation/webkit/dom_node_inside)
- [var DOM_START_TO_END: Int](/documentation/webkit/dom_start_to_end)
- [var DOM_START_TO_START: Int](/documentation/webkit/dom_start_to_start)
- [DOM Keyboard Input Enumeration (Legacy)](/documentation/webkit/1476191-dom-keyboard-input-enumeration-l)

###### Constants

- [var DOM_ALLOW_KEYBOARD_INPUT: Int](/documentation/webkit/dom_allow_keyboard_input)
- [DOM Delta Enumeration (Legacy)](/documentation/webkit/1420212-dom-delta-enumeration-legacy)

###### Constants

- [var DOM_DOM_DELTA_LINE: Int](/documentation/webkit/dom_dom_delta_line)
- [var DOM_DOM_DELTA_PAGE: Int](/documentation/webkit/dom_dom_delta_page)
- [var DOM_DOM_DELTA_PIXEL: Int](/documentation/webkit/dom_dom_delta_pixel)
- [DOM Phase Enumeration (Legacy)](/documentation/webkit/1558620-dom-phase-enumeration-legacy)

###### Constants

- [var DOM_AT_TARGET: Int](/documentation/webkit/dom_at_target)
- [var DOM_BUBBLING_PHASE: Int](/documentation/webkit/dom_bubbling_phase)
- [var DOM_CAPTURING_PHASE: Int](/documentation/webkit/dom_capturing_phase)
- [var DOM_NONE: Int](/documentation/webkit/dom_none)

##### Data Types

- [DOMTimeStamp](/documentation/webkit/domtimestamp)
- [DOMEventExceptionCode](/documentation/webkit/domeventexceptioncode)

###### Constants

- [var DOM_UNSPECIFIED_EVENT_TYPE_ERR: DOMEventExceptionCode](/documentation/webkit/dom_unspecified_event_type_err)

###### Initializers

- [init(UInt32)](/documentation/webkit/domeventexceptioncode/init(_:))
- [init(rawValue: UInt32)](/documentation/webkit/domeventexceptioncode/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/webkit/domeventexceptioncode/rawvalue)
- [DOMExceptionCode](/documentation/webkit/domexceptioncode)

###### Constants

- [var DOM_DOMSTRING_SIZE_ERR: DOMExceptionCode](/documentation/webkit/dom_domstring_size_err)
- [var DOM_HIERARCHY_REQUEST_ERR: DOMExceptionCode](/documentation/webkit/dom_hierarchy_request_err)
- [var DOM_INDEX_SIZE_ERR: DOMExceptionCode](/documentation/webkit/dom_index_size_err)
- [var DOM_INUSE_ATTRIBUTE_ERR: DOMExceptionCode](/documentation/webkit/dom_inuse_attribute_err)
- [var DOM_INVALID_ACCESS_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_access_err)
- [var DOM_INVALID_CHARACTER_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_character_err)
- [var DOM_INVALID_MODIFICATION_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_modification_err)
- [var DOM_INVALID_STATE_ERR: DOMExceptionCode](/documentation/webkit/dom_invalid_state_err)
- [var DOM_NAMESPACE_ERR: DOMExceptionCode](/documentation/webkit/dom_namespace_err)
- [var DOM_NOT_FOUND_ERR: DOMExceptionCode](/documentation/webkit/dom_not_found_err)
- [var DOM_NOT_SUPPORTED_ERR: DOMExceptionCode](/documentation/webkit/dom_not_supported_err)
- [var DOM_NO_DATA_ALLOWED_ERR: DOMExceptionCode](/documentation/webkit/dom_no_data_allowed_err)
- [var DOM_NO_MODIFICATION_ALLOWED_ERR: DOMExceptionCode](/documentation/webkit/dom_no_modification_allowed_err)
- [var DOM_SYNTAX_ERR: DOMExceptionCode](/documentation/webkit/dom_syntax_err)
- [var DOM_WRONG_DOCUMENT_ERR: DOMExceptionCode](/documentation/webkit/dom_wrong_document_err)

###### Initializers

- [init(UInt32)](/documentation/webkit/domexceptioncode/init(_:))
- [init(rawValue: UInt32)](/documentation/webkit/domexceptioncode/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/webkit/domexceptioncode/rawvalue)
- [DOMRangeExceptionCode](/documentation/webkit/domrangeexceptioncode)

###### Constants

- [var DOM_BAD_BOUNDARYPOINTS_ERR: DOMRangeExceptionCode](/documentation/webkit/dom_bad_boundarypoints_err)
- [var DOM_INVALID_NODE_TYPE_ERR: DOMRangeExceptionCode](/documentation/webkit/dom_invalid_node_type_err)

###### Initializers

- [init(UInt32)](/documentation/webkit/domrangeexceptioncode/init(_:))
- [init(rawValue: UInt32)](/documentation/webkit/domrangeexceptioncode/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/webkit/domrangeexceptioncode/rawvalue)
- [DOMXPathExceptionCode](/documentation/webkit/domxpathexceptioncode)

###### Constants

- [var DOM_INVALID_EXPRESSION_ERR: DOMXPathExceptionCode](/documentation/webkit/dom_invalid_expression_err)
- [var DOM_TYPE_ERR: DOMXPathExceptionCode](/documentation/webkit/dom_type_err)

###### Initializers

- [init(UInt32)](/documentation/webkit/domxpathexceptioncode/init(_:))
- [init(rawValue: UInt32)](/documentation/webkit/domxpathexceptioncode/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/webkit/domxpathexceptioncode/rawvalue)
- [Setting Up a Web View (Legacy)](/documentation/webkit/setting-up-a-web-view-legacy)

##### Setting Up a Web View (Legacy)

- [WebView](/documentation/webkit/webview-swift.class)

###### Registering Document Views and Representations

- [class func registerURLScheme(asLocal: String!)](/documentation/webkit/webview-swift.class/registerurlscheme(aslocal:))
- [class func registerClass(AnyClass!, representationClass: AnyClass!, forMIMEType: String!)](/documentation/webkit/webview-swift.class/registerclass(_:representationclass:formimetype:))

###### Initializing Views

- [init!(frame: NSRect, frameName: String!, groupName: String!)](/documentation/webkit/webview-swift.class/init(frame:framename:groupname:))

###### Closing the View

- [func close()](/documentation/webkit/webview-swift.class/close())
- [var shouldCloseWithWindow: Bool](/documentation/webkit/webview-swift.class/shouldclosewithwindow)

###### Getting the Main Frame

- [var mainFrame: WebFrame!](/documentation/webkit/webview-swift.class/mainframe)

###### Loading Content

- [func stopLoading(Any?)](/documentation/webkit/webview-swift.class/stoploading(_:))
- [func takeStringURLFrom(Any?)](/documentation/webkit/webview-swift.class/takestringurlfrom(_:))
- [func reload(Any?)](/documentation/webkit/webview-swift.class/reload(_:))
- [func reloadFromOrigin(Any?)](/documentation/webkit/webview-swift.class/reloadfromorigin(_:))
- [var estimatedProgress: Double](/documentation/webkit/webview-swift.class/estimatedprogress)

###### Drawing

- [var drawsBackground: Bool](/documentation/webkit/webview-swift.class/drawsbackground)
- [var shouldUpdateWhileOffscreen: Bool](/documentation/webkit/webview-swift.class/shouldupdatewhileoffscreen)

###### Moving Back and Forward

- [func setMaintainsBackForwardList(Bool)](/documentation/webkit/webview-swift.class/setmaintainsbackforwardlist(_:))
- [var backForwardList: WebBackForwardList!](/documentation/webkit/webview-swift.class/backforwardlist)
- [var canGoBack: Bool](/documentation/webkit/webview-swift.class/cangoback)
- [func goBack() -> Bool](/documentation/webkit/webview-swift.class/goback())
- [func goBack(Any?)](/documentation/webkit/webview-swift.class/goback(_:))
- [var canGoForward: Bool](/documentation/webkit/webview-swift.class/cangoforward)
- [func goForward() -> Bool](/documentation/webkit/webview-swift.class/goforward())
- [func goForward(Any?)](/documentation/webkit/webview-swift.class/goforward(_:))
- [func go(toBackForwardItem: WebHistoryItem!) -> Bool](/documentation/webkit/webview-swift.class/go(tobackforwarditem:))

###### Changing the Text Size

- [var canMakeTextLarger: Bool](/documentation/webkit/webview-swift.class/canmaketextlarger)
- [func makeTextLarger(Any?)](/documentation/webkit/webview-swift.class/maketextlarger(_:))
- [var canMakeTextSmaller: Bool](/documentation/webkit/webview-swift.class/canmaketextsmaller)
- [func makeTextSmaller(Any?)](/documentation/webkit/webview-swift.class/maketextsmaller(_:))

###### Getting and Setting Delegates

- [var downloadDelegate: (any WebDownloadDelegate)!](/documentation/webkit/webview-swift.class/downloaddelegate)
- [var frameLoadDelegate: (any WebFrameLoadDelegate)!](/documentation/webkit/webview-swift.class/frameloaddelegate)
- [var policyDelegate: (any WebPolicyDelegate)!](/documentation/webkit/webview-swift.class/policydelegate)
- [var resourceLoadDelegate: (any WebResourceLoadDelegate)!](/documentation/webkit/webview-swift.class/resourceloaddelegate)
- [var uiDelegate: (any WebUIDelegate)!](/documentation/webkit/webview-swift.class/uidelegate)

###### Getting and Setting the Window

- [var hostWindow: NSWindow!](/documentation/webkit/webview-swift.class/hostwindow)

###### Getting and Setting Preferences

- [var preferences: WebPreferences!](/documentation/webkit/webview-swift.class/preferences)
- [var preferencesIdentifier: String!](/documentation/webkit/webview-swift.class/preferencesidentifier)

###### Getting and Setting Frame Contents

- [var isLoading: Bool](/documentation/webkit/webview-swift.class/isloading)
- [var selectedFrame: WebFrame!](/documentation/webkit/webview-swift.class/selectedframe)
- [var mainFrameURL: String!](/documentation/webkit/webview-swift.class/mainframeurl)
- [var mainFrameTitle: String!](/documentation/webkit/webview-swift.class/mainframetitle)
- [var mainFrameIcon: NSImage!](/documentation/webkit/webview-swift.class/mainframeicon)
- [var mainFrameDocument: DOMDocument!](/documentation/webkit/webview-swift.class/mainframedocument)

###### Getting and Setting Content Information

- [class func canShowMIMEType(String!) -> Bool](/documentation/webkit/webview-swift.class/canshowmimetype(_:))
- [class func mimeTypesShownAsHTML() -> [Any]!](/documentation/webkit/webview-swift.class/mimetypesshownashtml())
- [class func setMIMETypesShownAsHTML([Any]!)](/documentation/webkit/webview-swift.class/setmimetypesshownashtml(_:))
- [class func canShowMIMEType(asHTML: String!) -> Bool](/documentation/webkit/webview-swift.class/canshowmimetype(ashtml:))
- [var supportsTextEncoding: Bool](/documentation/webkit/webview-swift.class/supportstextencoding)
- [var customTextEncodingName: String!](/documentation/webkit/webview-swift.class/customtextencodingname)
- [var textSizeMultiplier: Float](/documentation/webkit/webview-swift.class/textsizemultiplier)

###### Searching the Document

- [func search(for: String!, direction: Bool, caseSensitive: Bool, wrap: Bool) -> Bool](/documentation/webkit/webview-swift.class/search(for:direction:casesensitive:wrap:))

###### Getting and Setting the Group Name

- [var groupName: String!](/documentation/webkit/webview-swift.class/groupname)

###### Getting and Setting User-agent Strings

- [func userAgent(for: URL!) -> String!](/documentation/webkit/webview-swift.class/useragent(for:))
- [var applicationNameForUserAgent: String!](/documentation/webkit/webview-swift.class/applicationnameforuseragent)
- [var customUserAgent: String!](/documentation/webkit/webview-swift.class/customuseragent)

###### Processing JavaScript

- [func stringByEvaluatingJavaScript(from: String!) -> String!](/documentation/webkit/webview-swift.class/stringbyevaluatingjavascript(from:))

###### Using the Pasteboard

- [class func url(from: NSPasteboard!) -> URL!](/documentation/webkit/webview-swift.class/url(from:))
- [class func urlTitle(from: NSPasteboard!) -> String!](/documentation/webkit/webview-swift.class/urltitle(from:))
- [func pasteboardTypes(forElement: [AnyHashable : Any]!) -> [Any]!](/documentation/webkit/webview-swift.class/pasteboardtypes(forelement:))
- [var pasteboardTypesForSelection: [Any]!](/documentation/webkit/webview-swift.class/pasteboardtypesforselection)
- [func writeElement([AnyHashable : Any]!, withPasteboardTypes: [Any]!, to: NSPasteboard!)](/documentation/webkit/webview-swift.class/writeelement(_:withpasteboardtypes:to:))
- [func writeSelection(withPasteboardTypes: [Any]!, to: NSPasteboard!)](/documentation/webkit/webview-swift.class/writeselection(withpasteboardtypes:to:))

###### Dragging

- [func element(at: NSPoint) -> [AnyHashable : Any]!](/documentation/webkit/webview-swift.class/element(at:))
- [func moveDragCaret(to: NSPoint)](/documentation/webkit/webview-swift.class/movedragcaret(to:))
- [func removeDragCaret()](/documentation/webkit/webview-swift.class/removedragcaret())

###### Cut, Copy and Paste Action Methods

- [func copy(Any?)](/documentation/webkit/webview-swift.class/copy(_:))
- [func copyFont(Any?)](/documentation/webkit/webview-swift.class/copyfont(_:))
- [func cut(Any?)](/documentation/webkit/webview-swift.class/cut(_:))
- [func delete(Any?)](/documentation/webkit/webview-swift.class/delete(_:))
- [func paste(Any?)](/documentation/webkit/webview-swift.class/paste(_:))
- [func pasteFont(Any?)](/documentation/webkit/webview-swift.class/pastefont(_:))
- [func pasteAsPlainText(Any?)](/documentation/webkit/webview-swift.class/pasteasplaintext(_:))
- [func pasteAsRichText(Any?)](/documentation/webkit/webview-swift.class/pasteasrichtext(_:))

###### Content Alignment Action Methods

- [func alignCenter(Any?)](/documentation/webkit/webview-swift.class/aligncenter(_:))
- [func alignJustified(Any?)](/documentation/webkit/webview-swift.class/alignjustified(_:))
- [func alignLeft(Any?)](/documentation/webkit/webview-swift.class/alignleft(_:))
- [func alignRight(Any?)](/documentation/webkit/webview-swift.class/alignright(_:))

###### Changing the Font, Color and Other Attributes When Editing

- [func changeFont(Any?)](/documentation/webkit/webview-swift.class/changefont(_:))
- [func changeAttributes(Any?)](/documentation/webkit/webview-swift.class/changeattributes(_:))
- [func changeDocumentBackgroundColor(Any?)](/documentation/webkit/webview-swift.class/changedocumentbackgroundcolor(_:))
- [func changeColor(Any?)](/documentation/webkit/webview-swift.class/changecolor(_:))

###### Spell-checking Action Methods

- [func checkSpelling(Any?)](/documentation/webkit/webview-swift.class/checkspelling(_:))
- [func showGuessPanel(Any?)](/documentation/webkit/webview-swift.class/showguesspanel(_:))

###### Find Panel Action Method

- [func performFindPanelAction(Any?)](/documentation/webkit/webview-swift.class/performfindpanelaction(_:))

###### Controlling Speakable Text

- [func startSpeaking(Any?)](/documentation/webkit/webview-swift.class/startspeaking(_:))
- [func stopSpeaking(Any?)](/documentation/webkit/webview-swift.class/stopspeaking(_:))

###### Getting and Setting Document Editing Attributes

- [var isEditable: Bool](/documentation/webkit/webview-swift.class/iseditable)
- [var smartInsertDeleteEnabled: Bool](/documentation/webkit/webview-swift.class/smartinsertdeleteenabled)
- [var isContinuousSpellCheckingEnabled: Bool](/documentation/webkit/webview-swift.class/iscontinuousspellcheckingenabled)
- [var spellCheckerDocumentTag: Int](/documentation/webkit/webview-swift.class/spellcheckerdocumenttag)
- [var undoManager: UndoManager!](/documentation/webkit/webview-swift.class/undomanager)
- [var editingDelegate: (any WebEditingDelegate)!](/documentation/webkit/webview-swift.class/editingdelegate)
- [func editableDOMRange(for: NSPoint) -> DOMRange!](/documentation/webkit/webview-swift.class/editabledomrange(for:))

###### Editing Documents

- [func replaceSelection(with: DOMNode!)](/documentation/webkit/webview-swift.class/replaceselection(with:)-5px9m)
- [func replaceSelection(withText: String!)](/documentation/webkit/webview-swift.class/replaceselection(withtext:))
- [func replaceSelection(withMarkupString: String!)](/documentation/webkit/webview-swift.class/replaceselection(withmarkupstring:))
- [func replaceSelection(with: WebArchive!)](/documentation/webkit/webview-swift.class/replaceselection(with:)-3vj8l)
- [func deleteSelection()](/documentation/webkit/webview-swift.class/deleteselection())
- [func moveToBeginningOfSentence(Any?)](/documentation/webkit/webview-swift.class/movetobeginningofsentence(_:))
- [func moveToBeginningOfSentenceAndModifySelection(Any?)](/documentation/webkit/webview-swift.class/movetobeginningofsentenceandmodifyselection(_:))
- [func moveToEndOfSentence(Any?)](/documentation/webkit/webview-swift.class/movetoendofsentence(_:))
- [func moveToEndOfSentenceAndModifySelection(Any?)](/documentation/webkit/webview-swift.class/movetoendofsentenceandmodifyselection(_:))
- [func selectSentence(Any?)](/documentation/webkit/webview-swift.class/selectsentence(_:))
- [func toggleContinuousSpellChecking(Any?)](/documentation/webkit/webview-swift.class/togglecontinuousspellchecking(_:))
- [func toggleSmartInsertDelete(Any?)](/documentation/webkit/webview-swift.class/togglesmartinsertdelete(_:))
- [var canMakeTextStandardSize: Bool](/documentation/webkit/webview-swift.class/canmaketextstandardsize)
- [func makeTextStandardSize(Any?)](/documentation/webkit/webview-swift.class/maketextstandardsize(_:))
- [var maintainsInactiveSelection: Bool](/documentation/webkit/webview-swift.class/maintainsinactiveselection)

###### Selecting Content in the Document

- [var selectedDOMRange: DOMRange!](/documentation/webkit/webview-swift.class/selecteddomrange)
- [func setSelectedDOMRange(DOMRange!, affinity: NSSelectionAffinity)](/documentation/webkit/webview-swift.class/setselecteddomrange(_:affinity:))
- [var selectionAffinity: NSSelectionAffinity](/documentation/webkit/webview-swift.class/selectionaffinity)

###### Getting and Setting CSS Properties

- [func computedStyle(for: DOMElement!, pseudoElement: String!) -> DOMCSSStyleDeclaration!](/documentation/webkit/webview-swift.class/computedstyle(for:pseudoelement:))
- [var mediaStyle: String!](/documentation/webkit/webview-swift.class/mediastyle)
- [var typingStyle: DOMCSSStyleDeclaration!](/documentation/webkit/webview-swift.class/typingstyle)
- [func styleDeclaration(withText: String!) -> DOMCSSStyleDeclaration!](/documentation/webkit/webview-swift.class/styledeclaration(withtext:))
- [func applyStyle(DOMCSSStyleDeclaration!)](/documentation/webkit/webview-swift.class/applystyle(_:))

###### Using WebScript

- [var windowScriptObject: WebScriptObject!](/documentation/webkit/webview-swift.class/windowscriptobject)

###### Constants

- [Element Dictionary Keys](/documentation/webkit/element-dictionary-keys)

###### Constants

- [let WebElementDOMNodeKey: String](/documentation/webkit/webelementdomnodekey)
- [let WebElementFrameKey: String](/documentation/webkit/webelementframekey)
- [let WebElementImageAltStringKey: String](/documentation/webkit/webelementimagealtstringkey)
- [let WebElementImageKey: String](/documentation/webkit/webelementimagekey)
- [let WebElementImageRectKey: String](/documentation/webkit/webelementimagerectkey)
- [let WebElementImageURLKey: String](/documentation/webkit/webelementimageurlkey)
- [let WebElementIsSelectedKey: String](/documentation/webkit/webelementisselectedkey)
- [let WebElementLinkURLKey: String](/documentation/webkit/webelementlinkurlkey)
- [let WebElementLinkTargetFrameKey: String](/documentation/webkit/webelementlinktargetframekey)
- [let WebElementLinkTitleKey: String](/documentation/webkit/webelementlinktitlekey)
- [let WebElementLinkLabelKey: String](/documentation/webkit/webelementlinklabelkey)

###### Notifications

- [static let WebViewDidBeginEditing: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidbeginediting)
- [static let WebViewDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchange)
- [static let WebViewDidChangeSelection: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchangeselection)
- [static let WebViewDidChangeTypingStyle: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchangetypingstyle)
- [static let WebViewDidEndEditing: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidendediting)
- [static let WebViewProgressEstimateChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressestimatechanged)
- [static let WebViewProgressFinished: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressfinished)
- [static let WebViewProgressStarted: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressstarted)

###### Instance Methods

- [func overWrite(Any?)](/documentation/webkit/webview-swift.class/overwrite(_:))
- [WebPreferences](/documentation/webkit/webpreferences)

###### Getting the Standard Preferences

- [class func standard() -> WebPreferences!](/documentation/webkit/webpreferences/standard())

###### Initializing Preferences

- [init!(identifier: String!)](/documentation/webkit/webpreferences/init(identifier:))

###### Getting the Identifier

- [var identifier: String!](/documentation/webkit/webpreferences/identifier)

###### Saving Preferences to the User Defaults Database

- [var autosaves: Bool](/documentation/webkit/webpreferences/autosaves)

###### Enabling Java

- [var isJavaEnabled: Bool](/documentation/webkit/webpreferences/isjavaenabled)

###### Enabling JavaScript

- [var isJavaScriptEnabled: Bool](/documentation/webkit/webpreferences/isjavascriptenabled)
- [var javaScriptCanOpenWindowsAutomatically: Bool](/documentation/webkit/webpreferences/javascriptcanopenwindowsautomatically)

###### Enabling Plug-ins

- [var arePlugInsEnabled: Bool](/documentation/webkit/webpreferences/arepluginsenabled)

###### Enabling Style Sheets

- [var userStyleSheetEnabled: Bool](/documentation/webkit/webpreferences/userstylesheetenabled)

###### Getting and Setting Fonts

- [var cursiveFontFamily: String!](/documentation/webkit/webpreferences/cursivefontfamily)
- [var fantasyFontFamily: String!](/documentation/webkit/webpreferences/fantasyfontfamily)
- [var fixedFontFamily: String!](/documentation/webkit/webpreferences/fixedfontfamily)
- [var sansSerifFontFamily: String!](/documentation/webkit/webpreferences/sansseriffontfamily)
- [var serifFontFamily: String!](/documentation/webkit/webpreferences/seriffontfamily)
- [var standardFontFamily: String!](/documentation/webkit/webpreferences/standardfontfamily)

###### Getting and Setting Font Sizes

- [var defaultFixedFontSize: Int32](/documentation/webkit/webpreferences/defaultfixedfontsize)
- [var defaultFontSize: Int32](/documentation/webkit/webpreferences/defaultfontsize)
- [var minimumFontSize: Int32](/documentation/webkit/webpreferences/minimumfontsize)
- [var minimumLogicalFontSize: Int32](/documentation/webkit/webpreferences/minimumlogicalfontsize)

###### Getting and Setting Text Encoding

- [var defaultTextEncodingName: String!](/documentation/webkit/webpreferences/defaulttextencodingname)

###### Getting and Setting Incremental Rendering

- [var suppressesIncrementalRendering: Bool](/documentation/webkit/webpreferences/suppressesincrementalrendering)

###### Handling Images

- [var allowsAnimatedImageLooping: Bool](/documentation/webkit/webpreferences/allowsanimatedimagelooping)
- [var allowsAnimatedImages: Bool](/documentation/webkit/webpreferences/allowsanimatedimages)
- [var loadsImagesAutomatically: Bool](/documentation/webkit/webpreferences/loadsimagesautomatically)

###### Printing Backgrounds

- [var shouldPrintBackgrounds: Bool](/documentation/webkit/webpreferences/shouldprintbackgrounds)

###### Enabling Private Browsing

- [var privateBrowsingEnabled: Bool](/documentation/webkit/webpreferences/privatebrowsingenabled)

###### Controlling User Focus

- [var tabsToLinks: Bool](/documentation/webkit/webpreferences/tabstolinks)

###### Caching

- [var usesPageCache: Bool](/documentation/webkit/webpreferences/usespagecache)
- [var cacheModel: WebCacheModel](/documentation/webkit/webpreferences/cachemodel)

###### Constants

- [WebCacheModel](/documentation/webkit/webcachemodel)

###### Constants

- [case documentViewer](/documentation/webkit/webcachemodel/documentviewer)
- [case documentBrowser](/documentation/webkit/webcachemodel/documentbrowser)
- [case primaryWebBrowser](/documentation/webkit/webcachemodel/primarywebbrowser)

###### Initializers

- [init?(rawValue: UInt)](/documentation/webkit/webcachemodel/init(rawvalue:))

###### Notifications

- [static let WebPreferencesChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webpreferenceschanged)

###### Instance Properties

- [var allowsAirPlayForMediaPlayback: Bool](/documentation/webkit/webpreferences/allowsairplayformediaplayback)
- [var userStyleSheetLocation: URL!](/documentation/webkit/webpreferences/userstylesheetlocation)
- [WebEditingDelegate](/documentation/webkit/webeditingdelegate)

###### Instance Methods

- [func undoManager(for: WebView!) -> UndoManager!](/documentation/webkit/webeditingdelegate/undomanager(for:))
- [func webView(WebView!, doCommandBy: Selector!) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:docommandby:))
- [func webView(WebView!, shouldApplyStyle: DOMCSSStyleDeclaration!, toElementsIn: DOMRange!) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shouldapplystyle:toelementsin:))
- [func webView(WebView!, shouldBeginEditingIn: DOMRange!) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shouldbegineditingin:))
- [func webView(WebView!, shouldChangeSelectedDOMRange: DOMRange!, to: DOMRange!, affinity: NSSelectionAffinity, stillSelecting: Bool) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shouldchangeselecteddomrange:to:affinity:stillselecting:))
- [func webView(WebView!, shouldChangeTypingStyle: DOMCSSStyleDeclaration!, toStyle: DOMCSSStyleDeclaration!) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shouldchangetypingstyle:tostyle:))
- [func webView(WebView!, shouldDelete: DOMRange!) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shoulddelete:))
- [func webView(WebView!, shouldEndEditingIn: DOMRange!) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shouldendeditingin:))
- [func webView(WebView!, shouldInsert: DOMNode!, replacing: DOMRange!, given: WebViewInsertAction) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shouldinsert:replacing:given:))
- [func webView(WebView!, shouldInsertText: String!, replacing: DOMRange!, given: WebViewInsertAction) -> Bool](/documentation/webkit/webeditingdelegate/webview(_:shouldinserttext:replacing:given:))
- [func webViewDidBeginEditing(Notification!)](/documentation/webkit/webeditingdelegate/webviewdidbeginediting(_:))
- [func webViewDidChange(Notification!)](/documentation/webkit/webeditingdelegate/webviewdidchange(_:))
- [func webViewDidChangeSelection(Notification!)](/documentation/webkit/webeditingdelegate/webviewdidchangeselection(_:))
- [func webViewDidChangeTypingStyle(Notification!)](/documentation/webkit/webeditingdelegate/webviewdidchangetypingstyle(_:))
- [func webViewDidEndEditing(Notification!)](/documentation/webkit/webeditingdelegate/webviewdidendediting(_:))
- [WebUIDelegate](/documentation/webkit/webuidelegate)

###### Creating and Closing Windows

- [func webView(WebView!, createWebViewModalDialogWith: URLRequest!) -> WebView!](/documentation/webkit/webuidelegate/webview(_:createwebviewmodaldialogwith:))
- [func webViewRunModal(WebView!)](/documentation/webkit/webuidelegate/webviewrunmodal(_:))
- [func webView(WebView!, createWebViewWith: URLRequest!) -> WebView!](/documentation/webkit/webuidelegate/webview(_:createwebviewwith:))
- [func webViewClose(WebView!)](/documentation/webkit/webuidelegate/webviewclose(_:))

###### Moving and Resizing Windows

- [func webViewIsResizable(WebView!) -> Bool](/documentation/webkit/webuidelegate/webviewisresizable(_:))
- [func webView(WebView!, setResizable: Bool)](/documentation/webkit/webuidelegate/webview(_:setresizable:))
- [func webView(WebView!, setFrame: NSRect)](/documentation/webkit/webuidelegate/webview(_:setframe:))
- [func webViewFrame(WebView!) -> NSRect](/documentation/webkit/webuidelegate/webviewframe(_:))

###### Making Windows Key and Main

- [func webViewFocus(WebView!)](/documentation/webkit/webuidelegate/webviewfocus(_:))
- [func webViewUnfocus(WebView!)](/documentation/webkit/webuidelegate/webviewunfocus(_:))

###### Ordering Windows

- [func webViewShow(WebView!)](/documentation/webkit/webuidelegate/webviewshow(_:))

###### Working with the Responder Chain

- [func webViewFirstResponder(WebView!) -> NSResponder!](/documentation/webkit/webuidelegate/webviewfirstresponder(_:))
- [func webView(WebView!, makeFirstResponder: NSResponder!)](/documentation/webkit/webuidelegate/webview(_:makefirstresponder:))

###### Handling Mouse Events

- [func webView(WebView!, mouseDidMoveOverElement: [AnyHashable : Any]!, modifierFlags: Int)](/documentation/webkit/webuidelegate/webview(_:mousedidmoveoverelement:modifierflags:))
- [func webView(WebView!, contextMenuItemsForElement: [AnyHashable : Any]!, defaultMenuItems: [Any]!) -> [Any]!](/documentation/webkit/webuidelegate/webview(_:contextmenuitemsforelement:defaultmenuitems:))

###### Opening Panels

- [func webView(WebView!, runJavaScriptAlertPanelWithMessage: String!, initiatedBy: WebFrame!)](/documentation/webkit/webuidelegate/webview(_:runjavascriptalertpanelwithmessage:initiatedby:))
- [func webView(WebView!, runJavaScriptConfirmPanelWithMessage: String!, initiatedBy: WebFrame!) -> Bool](/documentation/webkit/webuidelegate/webview(_:runjavascriptconfirmpanelwithmessage:initiatedby:))
- [func webView(WebView!, runJavaScriptTextInputPanelWithPrompt: String!, defaultText: String!, initiatedBy: WebFrame!) -> String!](/documentation/webkit/webuidelegate/webview(_:runjavascripttextinputpanelwithprompt:defaulttext:initiatedby:))
- [func webView(WebView!, runOpenPanelForFileButtonWith: (any WebOpenPanelResultListener)!)](/documentation/webkit/webuidelegate/webview(_:runopenpanelforfilebuttonwith:))
- [func webView(WebView!, runOpenPanelForFileButtonWith: (any WebOpenPanelResultListener)!, allowMultipleFiles: Bool)](/documentation/webkit/webuidelegate/webview(_:runopenpanelforfilebuttonwith:allowmultiplefiles:))
- [func webView(WebView!, runBeforeUnloadConfirmPanelWithMessage: String!, initiatedBy: WebFrame!) -> Bool](/documentation/webkit/webuidelegate/webview(_:runbeforeunloadconfirmpanelwithmessage:initiatedby:))

###### Displaying Status Messages

- [func webView(WebView!, setStatusText: String!)](/documentation/webkit/webuidelegate/webview(_:setstatustext:))
- [func webViewStatusText(WebView!) -> String!](/documentation/webkit/webuidelegate/webviewstatustext(_:))

###### Managing Toolbars and the Status Bar

- [func webViewAreToolbarsVisible(WebView!) -> Bool](/documentation/webkit/webuidelegate/webviewaretoolbarsvisible(_:))
- [func webView(WebView!, setToolbarsVisible: Bool)](/documentation/webkit/webuidelegate/webview(_:settoolbarsvisible:))
- [func webViewIsStatusBarVisible(WebView!) -> Bool](/documentation/webkit/webuidelegate/webviewisstatusbarvisible(_:))
- [func webView(WebView!, setStatusBarVisible: Bool)](/documentation/webkit/webuidelegate/webview(_:setstatusbarvisible:))

###### Controlling Drag Behavior

- [func webView(WebView!, dragDestinationActionMaskFor: (any NSDraggingInfo)!) -> Int](/documentation/webkit/webuidelegate/webview(_:dragdestinationactionmaskfor:))
- [func webView(WebView!, dragSourceActionMaskFor: NSPoint) -> Int](/documentation/webkit/webuidelegate/webview(_:dragsourceactionmaskfor:))
- [func webView(WebView!, willPerform: WebDragDestinationAction, for: (any NSDraggingInfo)!)](/documentation/webkit/webuidelegate/webview(_:willperform:for:))
- [func webView(WebView!, willPerform: WebDragSourceAction, from: NSPoint, with: NSPasteboard!)](/documentation/webkit/webuidelegate/webview(_:willperform:from:with:))

###### Controlling Other Behaviors

- [func webView(WebView!, shouldPerformAction: Selector!, fromSender: Any!) -> Bool](/documentation/webkit/webuidelegate/webview(_:shouldperformaction:fromsender:))
- [func webView(WebView!, validate: (any NSValidatedUserInterfaceItem)!, defaultValidation: Bool) -> Bool](/documentation/webkit/webuidelegate/webview(_:validate:defaultvalidation:))

###### Printing

- [func webView(WebView!, print: WebFrameView!)](/documentation/webkit/webuidelegate/webview(_:print:))
- [func webViewHeaderHeight(WebView!) -> Float](/documentation/webkit/webuidelegate/webviewheaderheight(_:))
- [func webViewFooterHeight(WebView!) -> Float](/documentation/webkit/webuidelegate/webviewfooterheight(_:))
- [func webView(WebView!, drawHeaderIn: NSRect)](/documentation/webkit/webuidelegate/webview(_:drawheaderin:))
- [func webView(WebView!, drawFooterIn: NSRect)](/documentation/webkit/webuidelegate/webview(_:drawfooterin:))

###### Constants

- [Menu Item Tags](/documentation/webkit/menu-item-tags)

###### Constants

- [var WebMenuItemTagOpenLinkInNewWindow: Int](/documentation/webkit/webmenuitemtagopenlinkinnewwindow)
- [var WebMenuItemTagDownloadLinkToDisk: Int](/documentation/webkit/webmenuitemtagdownloadlinktodisk)
- [var WebMenuItemTagCopyLinkToClipboard: Int](/documentation/webkit/webmenuitemtagcopylinktoclipboard)
- [var WebMenuItemTagOpenImageInNewWindow: Int](/documentation/webkit/webmenuitemtagopenimageinnewwindow)
- [var WebMenuItemTagDownloadImageToDisk: Int](/documentation/webkit/webmenuitemtagdownloadimagetodisk)
- [var WebMenuItemTagCopyImageToClipboard: Int](/documentation/webkit/webmenuitemtagcopyimagetoclipboard)
- [var WebMenuItemTagOpenFrameInNewWindow: Int](/documentation/webkit/webmenuitemtagopenframeinnewwindow)
- [var WebMenuItemTagCopy: Int](/documentation/webkit/webmenuitemtagcopy)
- [var WebMenuItemTagGoBack: Int](/documentation/webkit/webmenuitemtaggoback)
- [var WebMenuItemTagGoForward: Int](/documentation/webkit/webmenuitemtaggoforward)
- [var WebMenuItemTagStop: Int](/documentation/webkit/webmenuitemtagstop)
- [var WebMenuItemTagReload: Int](/documentation/webkit/webmenuitemtagreload)
- [var WebMenuItemTagCut: Int](/documentation/webkit/webmenuitemtagcut)
- [var WebMenuItemTagPaste: Int](/documentation/webkit/webmenuitemtagpaste)
- [var WebMenuItemTagSpellingGuess: Int](/documentation/webkit/webmenuitemtagspellingguess)
- [var WebMenuItemTagNoGuessesFound: Int](/documentation/webkit/webmenuitemtagnoguessesfound)
- [var WebMenuItemTagIgnoreSpelling: Int](/documentation/webkit/webmenuitemtagignorespelling)
- [var WebMenuItemTagLearnSpelling: Int](/documentation/webkit/webmenuitemtaglearnspelling)
- [var WebMenuItemTagOther: Int](/documentation/webkit/webmenuitemtagother)
- [var WebMenuItemTagSearchInSpotlight: Int](/documentation/webkit/webmenuitemtagsearchinspotlight)
- [var WebMenuItemTagSearchWeb: Int](/documentation/webkit/webmenuitemtagsearchweb)
- [var WebMenuItemTagLookUpInDictionary: Int](/documentation/webkit/webmenuitemtaglookupindictionary)
- [var WebMenuItemTagOpenWithDefaultApplication: Int](/documentation/webkit/webmenuitemtagopenwithdefaultapplication)
- [var WebMenuItemPDFActualSize: Int](/documentation/webkit/webmenuitempdfactualsize)
- [var WebMenuItemPDFZoomIn: Int](/documentation/webkit/webmenuitempdfzoomin)
- [var WebMenuItemPDFZoomOut: Int](/documentation/webkit/webmenuitempdfzoomout)
- [var WebMenuItemPDFAutoSize: Int](/documentation/webkit/webmenuitempdfautosize)
- [var WebMenuItemPDFSinglePage: Int](/documentation/webkit/webmenuitempdfsinglepage)
- [var WebMenuItemPDFFacingPages: Int](/documentation/webkit/webmenuitempdffacingpages)
- [var WebMenuItemPDFContinuous: Int](/documentation/webkit/webmenuitempdfcontinuous)
- [var WebMenuItemPDFNextPage: Int](/documentation/webkit/webmenuitempdfnextpage)
- [var WebMenuItemPDFPreviousPage: Int](/documentation/webkit/webmenuitempdfpreviouspage)
- [WebDragDestinationAction](/documentation/webkit/webdragdestinationaction)

###### Constants

- [static var DHTML: WebDragDestinationAction](/documentation/webkit/webdragdestinationaction/dhtml)
- [static var edit: WebDragDestinationAction](/documentation/webkit/webdragdestinationaction/edit)
- [static var load: WebDragDestinationAction](/documentation/webkit/webdragdestinationaction/load)
- [static var any: WebDragDestinationAction](/documentation/webkit/webdragdestinationaction/any)

###### Initializers

- [init(rawValue: UInt)](/documentation/webkit/webdragdestinationaction/init(rawvalue:))
- [WebDragSourceAction](/documentation/webkit/webdragsourceaction)

###### Constants

- [static var DHTML: WebDragSourceAction](/documentation/webkit/webdragsourceaction/dhtml)
- [static var image: WebDragSourceAction](/documentation/webkit/webdragsourceaction/image)
- [static var link: WebDragSourceAction](/documentation/webkit/webdragsourceaction/link)
- [static var selection: WebDragSourceAction](/documentation/webkit/webdragsourceaction/selection)
- [static var any: WebDragSourceAction](/documentation/webkit/webdragsourceaction/any)

###### Initializers

- [init(rawValue: UInt)](/documentation/webkit/webdragsourceaction/init(rawvalue:))
- [Accessing Previous Webpages (Legacy)](/documentation/webkit/accessing-previous-webpages-legacy)

##### Accessing Previous Webpages (Legacy)

- [WebBackForwardList](/documentation/webkit/webbackforwardlist)

###### Adding and Removing Items

- [func add(WebHistoryItem!)](/documentation/webkit/webbackforwardlist/add(_:))

###### Moving Backward and Forward

- [func goBack()](/documentation/webkit/webbackforwardlist/goback())
- [func goForward()](/documentation/webkit/webbackforwardlist/goforward())
- [func go(to: WebHistoryItem!)](/documentation/webkit/webbackforwardlist/go(to:))

###### Querying the Back-Forward List

- [var backItem: WebHistoryItem!](/documentation/webkit/webbackforwardlist/backitem)
- [var backListCount: Int32](/documentation/webkit/webbackforwardlist/backlistcount)
- [func back(withLimit: Int32) -> [Any]!](/documentation/webkit/webbackforwardlist/back(withlimit:))
- [func contains(WebHistoryItem!) -> Bool](/documentation/webkit/webbackforwardlist/contains(_:))
- [var currentItem: WebHistoryItem!](/documentation/webkit/webbackforwardlist/currentitem)
- [func item(at: Int32) -> WebHistoryItem!](/documentation/webkit/webbackforwardlist/item(at:))
- [var forwardItem: WebHistoryItem!](/documentation/webkit/webbackforwardlist/forwarditem)
- [var forwardListCount: Int32](/documentation/webkit/webbackforwardlist/forwardlistcount)
- [func forwardList(withLimit: Int32) -> [Any]!](/documentation/webkit/webbackforwardlist/forwardlist(withlimit:))

###### Page Caching

- [func pageCacheSize() -> Int](/documentation/webkit/webbackforwardlist/pagecachesize())
- [func setPageCacheSize(Int)](/documentation/webkit/webbackforwardlist/setpagecachesize(_:))

###### Setting Attributes

- [var capacity: Int32](/documentation/webkit/webbackforwardlist/capacity)
- [WebHistory](/documentation/webkit/webhistory)

###### Accessing Shared History Objects

- [class func optionalShared() -> WebHistory!](/documentation/webkit/webhistory/optionalshared())
- [class func setOptionalShared(WebHistory!)](/documentation/webkit/webhistory/setoptionalshared(_:))

###### Adding and Removing History Items

- [func addItems([Any]!)](/documentation/webkit/webhistory/additems(_:))
- [func removeItems([Any]!)](/documentation/webkit/webhistory/removeitems(_:))
- [func removeAllItems()](/documentation/webkit/webhistory/removeallitems())

###### Getting Web History Items

- [func orderedItemsLastVisited(onDay: NSCalendarDate!) -> [Any]!](/documentation/webkit/webhistory/ordereditemslastvisited(onday:))
- [var orderedLastVisitedDays: [Any]!](/documentation/webkit/webhistory/orderedlastvisiteddays)
- [func item(for: URL!) -> WebHistoryItem!](/documentation/webkit/webhistory/item(for:))

###### Loading and Saving History Information

- [func load(from: URL!) throws](/documentation/webkit/webhistory/load(from:))
- [func save(to: URL!) throws](/documentation/webkit/webhistory/save(to:))

###### Getting and Setting Attributes

- [var historyAgeInDaysLimit: Int32](/documentation/webkit/webhistory/historyageindayslimit)
- [var historyItemLimit: Int32](/documentation/webkit/webhistory/historyitemlimit)

###### Constants

- [Web History Dictionary Keys](/documentation/webkit/web-history-dictionary-keys)

###### Constants

- [let WebHistoryItemsKey: String](/documentation/webkit/webhistoryitemskey)

###### Notifications

- [static let WebHistoryAllItemsRemoved: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryallitemsremoved)
- [static let WebHistoryItemChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryitemchanged)
- [static let WebHistoryItemsAdded: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryitemsadded)
- [static let WebHistoryItemsRemoved: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryitemsremoved)
- [static let WebHistoryLoaded: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistoryloaded)
- [static let WebHistorySaved: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webhistorysaved)
- [WebHistoryItem](/documentation/webkit/webhistoryitem)

###### Initializing WebHistoryItem objects

- [init!(urlString: String!, title: String!, lastVisitedTimeInterval: TimeInterval)](/documentation/webkit/webhistoryitem/init(urlstring:title:lastvisitedtimeinterval:))

###### Getting URL information

- [var urlString: String!](/documentation/webkit/webhistoryitem/urlstring)
- [var originalURLString: String!](/documentation/webkit/webhistoryitem/originalurlstring)

###### Getting and setting page titles

- [var title: String!](/documentation/webkit/webhistoryitem/title)
- [var alternateTitle: String!](/documentation/webkit/webhistoryitem/alternatetitle)

###### Getting other attributes

- [var icon: NSImage!](/documentation/webkit/webhistoryitem/icon)
- [var lastVisitedTimeInterval: TimeInterval](/documentation/webkit/webhistoryitem/lastvisitedtimeinterval)
- [Archiving Webpages (Legacy)](/documentation/webkit/archiving-webpages-legacy)

##### Archiving Webpages (Legacy)

- [WebArchive](/documentation/webkit/webarchive)

###### Initializing

- [init!(mainResource: WebResource!, subresources: [Any]!, subframeArchives: [Any]!)](/documentation/webkit/webarchive/init(mainresource:subresources:subframearchives:))
- [init!(data: Data!)](/documentation/webkit/webarchive/init(data:))

###### Getting attributes

- [var mainResource: WebResource!](/documentation/webkit/webarchive/mainresource)
- [var subresources: [Any]!](/documentation/webkit/webarchive/subresources)
- [var subframeArchives: [Any]!](/documentation/webkit/webarchive/subframearchives)
- [var data: Data!](/documentation/webkit/webarchive/data)

###### Constants

- [let WebArchivePboardType: String](/documentation/webkit/webarchivepboardtype)
- [Loading Resources (Legacy)](/documentation/webkit/loading-resources-legacy)

##### Loading Resources (Legacy)

- [WebResource](/documentation/webkit/webresource)

###### Initializing

- [init!(data: Data!, url: URL!, mimeType: String!, textEncodingName: String!, frameName: String!)](/documentation/webkit/webresource/init(data:url:mimetype:textencodingname:framename:))

###### Getting attributes

- [var data: Data!](/documentation/webkit/webresource/data)
- [var url: URL!](/documentation/webkit/webresource/url)
- [var mimeType: String!](/documentation/webkit/webresource/mimetype)
- [var textEncodingName: String!](/documentation/webkit/webresource/textencodingname)
- [var frameName: String!](/documentation/webkit/webresource/framename)
- [WebResourceLoadDelegate](/documentation/webkit/webresourceloaddelegate)

###### Setting Identifiers

- [func webView(WebView!, identifierForInitialRequest: URLRequest!, from: WebDataSource!) -> Any!](/documentation/webkit/webresourceloaddelegate/webview(_:identifierforinitialrequest:from:))

###### Loading Content

- [func webView(WebView!, resource: Any!, willSend: URLRequest!, redirectResponse: URLResponse!, from: WebDataSource!) -> URLRequest!](/documentation/webkit/webresourceloaddelegate/webview(_:resource:willsend:redirectresponse:from:))
- [func webView(WebView!, resource: Any!, didFinishLoadingFrom: WebDataSource!)](/documentation/webkit/webresourceloaddelegate/webview(_:resource:didfinishloadingfrom:))
- [func webView(WebView!, resource: Any!, didReceive: URLResponse!, from: WebDataSource!)](/documentation/webkit/webresourceloaddelegate/webview(_:resource:didreceive:from:)-22bdg)
- [func webView(WebView!, resource: Any!, didReceiveContentLength: Int, from: WebDataSource!)](/documentation/webkit/webresourceloaddelegate/webview(_:resource:didreceivecontentlength:from:))
- [func webView(WebView!, resource: Any!, didFailLoadingWithError: (any Error)!, from: WebDataSource!)](/documentation/webkit/webresourceloaddelegate/webview(_:resource:didfailloadingwitherror:from:))
- [func webView(WebView!, plugInFailedWithError: (any Error)!, dataSource: WebDataSource!)](/documentation/webkit/webresourceloaddelegate/webview(_:pluginfailedwitherror:datasource:))

###### Authenticating Resources

- [func webView(WebView!, resource: Any!, didReceive: URLAuthenticationChallenge!, from: WebDataSource!)](/documentation/webkit/webresourceloaddelegate/webview(_:resource:didreceive:from:)-54xbd)
- [func webView(WebView!, resource: Any!, didCancel: URLAuthenticationChallenge!, from: WebDataSource!)](/documentation/webkit/webresourceloaddelegate/webview(_:resource:didcancel:from:))
- [Working with Frames (legacy)](/documentation/webkit/working-with-frames-legacy)

##### Working with Frames (Legacy)

- [WebFrame](/documentation/webkit/webframe)

###### Initializing Frames

- [init!(name: String!, webFrameView: WebFrameView!, webView: WebView!)](/documentation/webkit/webframe/init(name:webframeview:webview:))

###### Loading Content

- [func load(URLRequest!)](/documentation/webkit/webframe/load(_:)-47p2s)
- [func reload()](/documentation/webkit/webframe/reload())
- [func reloadFromOrigin()](/documentation/webkit/webframe/reloadfromorigin())
- [func stopLoading()](/documentation/webkit/webframe/stoploading())
- [func loadAlternateHTMLString(String!, baseURL: URL!, forUnreachableURL: URL!)](/documentation/webkit/webframe/loadalternatehtmlstring(_:baseurl:forunreachableurl:))
- [func loadHTMLString(String!, baseURL: URL!)](/documentation/webkit/webframe/loadhtmlstring(_:baseurl:))
- [func load(Data!, mimeType: String!, textEncodingName: String!, baseURL: URL!)](/documentation/webkit/webframe/load(_:mimetype:textencodingname:baseurl:))
- [func load(WebArchive!)](/documentation/webkit/webframe/load(_:)-6wkx6)

###### Getting the Data Source

- [var dataSource: WebDataSource?](/documentation/webkit/webframe/datasource)
- [var provisionalDataSource: WebDataSource!](/documentation/webkit/webframe/provisionaldatasource)

###### Getting Related Frames and Views

- [var parent: WebFrame!](/documentation/webkit/webframe/parent)
- [var childFrames: [Any]!](/documentation/webkit/webframe/childframes)
- [var frameView: WebFrameView!](/documentation/webkit/webframe/frameview)
- [var webView: WebView!](/documentation/webkit/webframe/webview)

###### Finding Frames

- [func findNamed(String!) -> WebFrame!](/documentation/webkit/webframe/findnamed(_:))
- [var name: String!](/documentation/webkit/webframe/name)

###### Getting DOM Objects

- [var domDocument: DOMDocument!](/documentation/webkit/webframe/domdocument)
- [var frameElement: DOMHTMLElement!](/documentation/webkit/webframe/frameelement)
- [var globalContext: JSGlobalContextRef!](/documentation/webkit/webframe/globalcontext)
- [var javaScriptContext: JSContext!](/documentation/webkit/webframe/javascriptcontext)
- [var windowObject: WebScriptObject!](/documentation/webkit/webframe/windowobject)
- [WebDataSource](/documentation/webkit/webdatasource)

###### Initializing an instance

- [init!(request: URLRequest!)](/documentation/webkit/webdatasource/init(request:))

###### Querying page data and state

- [var data: Data!](/documentation/webkit/webdatasource/data)
- [var isLoading: Bool](/documentation/webkit/webdatasource/isloading)
- [var pageTitle: String!](/documentation/webkit/webdatasource/pagetitle)
- [var representation: (any WebDocumentRepresentation)!](/documentation/webkit/webdatasource/representation)
- [var textEncodingName: String!](/documentation/webkit/webdatasource/textencodingname)

###### Getting the request and response

- [var initialRequest: URLRequest!](/documentation/webkit/webdatasource/initialrequest)
- [var request: NSMutableURLRequest!](/documentation/webkit/webdatasource/request)
- [var response: URLResponse!](/documentation/webkit/webdatasource/response)

###### Getting the web frame

- [var webFrame: WebFrame!](/documentation/webkit/webdatasource/webframe)

###### Getting an unreachable URL

- [var unreachableURL: URL!](/documentation/webkit/webdatasource/unreachableurl)

###### Getting a web archive

- [var webArchive: WebArchive!](/documentation/webkit/webdatasource/webarchive)

###### Accessing subresources

- [var mainResource: WebResource!](/documentation/webkit/webdatasource/mainresource)
- [func addSubresource(WebResource!)](/documentation/webkit/webdatasource/addsubresource(_:))
- [func subresource(for: URL!) -> WebResource!](/documentation/webkit/webdatasource/subresource(for:))
- [var subresources: [Any]!](/documentation/webkit/webdatasource/subresources)
- [WebFrameView](/documentation/webkit/webframeview)

###### Getting the Web Frame

- [var webFrame: WebFrame!](/documentation/webkit/webframeview/webframe)

###### Getting Subviews

- [var documentView: (any NSView & WebDocumentView)!](/documentation/webkit/webframeview/documentview)

###### Setting Scrolling Behavior

- [var allowsScrolling: Bool](/documentation/webkit/webframeview/allowsscrolling)

###### Printing Views

- [var canPrintHeadersAndFooters: Bool](/documentation/webkit/webframeview/canprintheadersandfooters)
- [func printOperation(with: NSPrintInfo!) -> NSPrintOperation!](/documentation/webkit/webframeview/printoperation(with:))
- [var documentViewShouldHandlePrint: Bool](/documentation/webkit/webframeview/documentviewshouldhandleprint)
- [func printDocumentView()](/documentation/webkit/webframeview/printdocumentview())
- [WebFrameLoadDelegate](/documentation/webkit/webframeloaddelegate)

###### Instance Methods

- [func webView(WebView!, didCancelClientRedirectFor: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didcancelclientredirectfor:))
- [func webView(WebView!, didChangeLocationWithinPageFor: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didchangelocationwithinpagefor:))
- [func webView(WebView!, didClearWindowObject: WebScriptObject!, for: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didclearwindowobject:for:))
- [func webView(WebView!, didCommitLoadFor: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didcommitloadfor:))
- [func webView(WebView!, didCreateJavaScriptContext: JSContext!, for: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didcreatejavascriptcontext:for:))
- [func webView(WebView!, didFailLoadWithError: (any Error)!, for: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didfailloadwitherror:for:))
- [func webView(WebView!, didFailProvisionalLoadWithError: (any Error)!, for: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didfailprovisionalloadwitherror:for:))
- [func webView(WebView!, didFinishLoadFor: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didfinishloadfor:))
- [func webView(WebView!, didReceiveIcon: NSImage!, for: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didreceiveicon:for:))
- [func webView(WebView!, didReceiveServerRedirectForProvisionalLoadFor: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didreceiveserverredirectforprovisionalloadfor:))
- [func webView(WebView!, didReceiveTitle: String!, for: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didreceivetitle:for:))
- [func webView(WebView!, didStartProvisionalLoadFor: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:didstartprovisionalloadfor:))
- [func webView(WebView!, willClose: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:willclose:))
- [func webView(WebView!, willPerformClientRedirectTo: URL!, delay: TimeInterval, fire: Date!, for: WebFrame!)](/documentation/webkit/webframeloaddelegate/webview(_:willperformclientredirectto:delay:fire:for:))
- [Downloading Information (Legacy)](/documentation/webkit/downloading-information-legacy)

##### Downloading Information (Legacy)

- [WebDownload](/documentation/webkit/webdownload)
- [WebDownloadDelegate](/documentation/webkit/webdownloaddelegate)

###### Authentication messages

- [func downloadWindow(forAuthenticationSheet: WebDownload!) -> NSWindow!](/documentation/webkit/webdownloaddelegate/downloadwindow(forauthenticationsheet:))
- [Opening a File (Legacy)](/documentation/webkit/opening-a-file-legacy)

##### Opening a File (Legacy)

- [WebOpenPanelResultListener](/documentation/webkit/webopenpanelresultlistener)

###### Setting a File Name

- [func chooseFilename(String!)](/documentation/webkit/webopenpanelresultlistener/choosefilename(_:))
- [func chooseFilenames([Any]!)](/documentation/webkit/webopenpanelresultlistener/choosefilenames(_:))

###### Cancelling a File Open Operation

- [func cancel()](/documentation/webkit/webopenpanelresultlistener/cancel())
- [Setting Policies (Legacy)](/documentation/webkit/setting-policies-legacy)

##### Setting Policies (Legacy)

- [WebPolicyDecisionListener](/documentation/webkit/webpolicydecisionlistener)

###### Making Resource-Usage Decisions

- [func download()](/documentation/webkit/webpolicydecisionlistener/download())
- [func ignore()](/documentation/webkit/webpolicydecisionlistener/ignore())
- [func use()](/documentation/webkit/webpolicydecisionlistener/use())
- [WebPolicyDelegate](/documentation/webkit/webpolicydelegate)

###### Instance Methods

- [func webView(WebView!, decidePolicyForMIMEType: String!, request: URLRequest!, frame: WebFrame!, decisionListener: (any WebPolicyDecisionListener)!)](/documentation/webkit/webpolicydelegate/webview(_:decidepolicyformimetype:request:frame:decisionlistener:))
- [func webView(WebView!, decidePolicyForNavigationAction: [AnyHashable : Any]!, request: URLRequest!, frame: WebFrame!, decisionListener: (any WebPolicyDecisionListener)!)](/documentation/webkit/webpolicydelegate/webview(_:decidepolicyfornavigationaction:request:frame:decisionlistener:))
- [func webView(WebView!, decidePolicyForNewWindowAction: [AnyHashable : Any]!, request: URLRequest!, newFrameName: String!, decisionListener: (any WebPolicyDecisionListener)!)](/documentation/webkit/webpolicydelegate/webview(_:decidepolicyfornewwindowaction:request:newframename:decisionlistener:))
- [func webView(WebView!, unableToImplementPolicyWithError: (any Error)!, frame: WebFrame!)](/documentation/webkit/webpolicydelegate/webview(_:unabletoimplementpolicywitherror:frame:))
- [Implementing Plugins (Legacy)](/documentation/webkit/implementing-plugins-legacy)

##### Implementing Plugins  (Legacy)

- [WebPlugIn](/documentation/objectivec/webplugin)
- [WebPlugInContainer](/documentation/objectivec/webplugincontainer)
- [WebPlugInViewFactory](/documentation/webkit/webpluginviewfactory)

###### Type Methods

- [static func plugInView(withArguments: [AnyHashable : Any]!) -> NSView!](/documentation/webkit/webpluginviewfactory/pluginview(witharguments:))
- [Incorporating Scripts (Legacy)](/documentation/webkit/incorporating-scripts-legacy)

##### Incorporating Scripts (Legacy)

- [WebScriptObject](/documentation/webkit/webscriptobject)

###### Getting and setting properties

- [func jsObject() -> JSObjectRef!](/documentation/webkit/webscriptobject/jsobject())
- [func removeWebScriptKey(String!)](/documentation/webkit/webscriptobject/removewebscriptkey(_:))
- [func webScriptValue(at: UInt32) -> Any!](/documentation/webkit/webscriptobject/webscriptvalue(at:))
- [func setWebScriptValueAt(UInt32, value: Any!)](/documentation/webkit/webscriptobject/setwebscriptvalueat(_:value:))

###### Executing scripts

- [func callWebScriptMethod(String!, withArguments: [Any]!) -> Any!](/documentation/webkit/webscriptobject/callwebscriptmethod(_:witharguments:))
- [func evaluateWebScript(String!) -> Any!](/documentation/webkit/webscriptobject/evaluatewebscript(_:))

###### Raising exceptions

- [class func throwException(String!) -> Bool](/documentation/webkit/webscriptobject/throwexception(_:))
- [func setException(String!)](/documentation/webkit/webscriptobject/setexception(_:))

###### Getting a string representation

- [func stringRepresentation() -> String!](/documentation/webkit/webscriptobject/stringrepresentation())

###### Instance Methods

- [func jsValue() -> JSValue!](/documentation/webkit/webscriptobject/jsvalue())
- [WebScripting](/documentation/objectivec/webscripting)
- [WebUndefined](/documentation/webkit/webundefined)
- [Working With Document Web Views (Legacy)](/documentation/webkit/working-with-document-web-views-legacy)

##### Working With Document Web Views (Legacy)

- [WebDocumentRepresentation](/documentation/webkit/webdocumentrepresentation)

###### Setting the data source

- [func setDataSource(WebDataSource!)](/documentation/webkit/webdocumentrepresentation/setdatasource(_:))

###### Loading content

- [func receivedData(Data!, with: WebDataSource!)](/documentation/webkit/webdocumentrepresentation/receiveddata(_:with:))
- [func receivedError((any Error)!, with: WebDataSource!)](/documentation/webkit/webdocumentrepresentation/receivederror(_:with:))
- [func finishedLoading(with: WebDataSource!)](/documentation/webkit/webdocumentrepresentation/finishedloading(with:))

###### Getting document source

- [func canProvideDocumentSource() -> Bool](/documentation/webkit/webdocumentrepresentation/canprovidedocumentsource())
- [func documentSource() -> String!](/documentation/webkit/webdocumentrepresentation/documentsource())

###### Getting the document title

- [func title() -> String!](/documentation/webkit/webdocumentrepresentation/title())
- [WebDocumentSearching](/documentation/webkit/webdocumentsearching)

###### Searching a document

- [func search(for: String!, direction: Bool, caseSensitive: Bool, wrap: Bool) -> Bool](/documentation/webkit/webdocumentsearching/search(for:direction:casesensitive:wrap:))
- [WebDocumentText](/documentation/webkit/webdocumenttext)

###### Getting document content

- [func string() -> String!](/documentation/webkit/webdocumenttext/string())
- [func attributedString() -> NSAttributedString!](/documentation/webkit/webdocumenttext/attributedstring())

###### Selecting and deselecting text

- [func selectAll()](/documentation/webkit/webdocumenttext/selectall())
- [func deselectAll()](/documentation/webkit/webdocumenttext/deselectall())
- [func selectedString() -> String!](/documentation/webkit/webdocumenttext/selectedstring())
- [func selectedAttributedString() -> NSAttributedString!](/documentation/webkit/webdocumenttext/selectedattributedstring())

###### Text encoding

- [func supportsTextEncoding() -> Bool](/documentation/webkit/webdocumenttext/supportstextencoding())
- [WebDocumentView](/documentation/webkit/webdocumentview)

###### Setting the data source

- [func setDataSource(WebDataSource!)](/documentation/webkit/webdocumentview/setdatasource(_:))
- [func dataSourceUpdated(WebDataSource!)](/documentation/webkit/webdocumentview/datasourceupdated(_:))

###### Controlling the layout

- [func setNeedsLayout(Bool)](/documentation/webkit/webdocumentview/setneedslayout(_:))
- [func layout()](/documentation/webkit/webdocumentview/layout())

###### Attaching to a window

- [func viewDidMoveToHostWindow()](/documentation/webkit/webdocumentview/viewdidmovetohostwindow())
- [func viewWillMove(toHostWindow: NSWindow!)](/documentation/webkit/webdocumentview/viewwillmove(tohostwindow:))

#### Preview

- [WKPreviewElementInfo](/documentation/webkit/wkpreviewelementinfo)

##### Accessing the Preview Link

- [var linkURL: URL?](/documentation/webkit/wkpreviewelementinfo/linkurl)
- [WKPreviewActionItem](/documentation/webkit/wkpreviewactionitem)

##### Accessing Preview Actions

- [var identifier: String!](/documentation/webkit/wkpreviewactionitem/identifier)

#### Content

- [WebView](/documentation/webkit/webview-swift.class)

##### Registering Document Views and Representations

- [class func registerURLScheme(asLocal: String!)](/documentation/webkit/webview-swift.class/registerurlscheme(aslocal:))
- [class func registerClass(AnyClass!, representationClass: AnyClass!, forMIMEType: String!)](/documentation/webkit/webview-swift.class/registerclass(_:representationclass:formimetype:))

##### Initializing Views

- [init!(frame: NSRect, frameName: String!, groupName: String!)](/documentation/webkit/webview-swift.class/init(frame:framename:groupname:))

##### Closing the View

- [func close()](/documentation/webkit/webview-swift.class/close())
- [var shouldCloseWithWindow: Bool](/documentation/webkit/webview-swift.class/shouldclosewithwindow)

##### Getting the Main Frame

- [var mainFrame: WebFrame!](/documentation/webkit/webview-swift.class/mainframe)

##### Loading Content

- [func stopLoading(Any?)](/documentation/webkit/webview-swift.class/stoploading(_:))
- [func takeStringURLFrom(Any?)](/documentation/webkit/webview-swift.class/takestringurlfrom(_:))
- [func reload(Any?)](/documentation/webkit/webview-swift.class/reload(_:))
- [func reloadFromOrigin(Any?)](/documentation/webkit/webview-swift.class/reloadfromorigin(_:))
- [var estimatedProgress: Double](/documentation/webkit/webview-swift.class/estimatedprogress)

##### Drawing

- [var drawsBackground: Bool](/documentation/webkit/webview-swift.class/drawsbackground)
- [var shouldUpdateWhileOffscreen: Bool](/documentation/webkit/webview-swift.class/shouldupdatewhileoffscreen)

##### Moving Back and Forward

- [func setMaintainsBackForwardList(Bool)](/documentation/webkit/webview-swift.class/setmaintainsbackforwardlist(_:))
- [var backForwardList: WebBackForwardList!](/documentation/webkit/webview-swift.class/backforwardlist)
- [var canGoBack: Bool](/documentation/webkit/webview-swift.class/cangoback)
- [func goBack() -> Bool](/documentation/webkit/webview-swift.class/goback())
- [func goBack(Any?)](/documentation/webkit/webview-swift.class/goback(_:))
- [var canGoForward: Bool](/documentation/webkit/webview-swift.class/cangoforward)
- [func goForward() -> Bool](/documentation/webkit/webview-swift.class/goforward())
- [func goForward(Any?)](/documentation/webkit/webview-swift.class/goforward(_:))
- [func go(toBackForwardItem: WebHistoryItem!) -> Bool](/documentation/webkit/webview-swift.class/go(tobackforwarditem:))

##### Changing the Text Size

- [var canMakeTextLarger: Bool](/documentation/webkit/webview-swift.class/canmaketextlarger)
- [func makeTextLarger(Any?)](/documentation/webkit/webview-swift.class/maketextlarger(_:))
- [var canMakeTextSmaller: Bool](/documentation/webkit/webview-swift.class/canmaketextsmaller)
- [func makeTextSmaller(Any?)](/documentation/webkit/webview-swift.class/maketextsmaller(_:))

##### Getting and Setting Delegates

- [var downloadDelegate: (any WebDownloadDelegate)!](/documentation/webkit/webview-swift.class/downloaddelegate)
- [var frameLoadDelegate: (any WebFrameLoadDelegate)!](/documentation/webkit/webview-swift.class/frameloaddelegate)
- [var policyDelegate: (any WebPolicyDelegate)!](/documentation/webkit/webview-swift.class/policydelegate)
- [var resourceLoadDelegate: (any WebResourceLoadDelegate)!](/documentation/webkit/webview-swift.class/resourceloaddelegate)
- [var uiDelegate: (any WebUIDelegate)!](/documentation/webkit/webview-swift.class/uidelegate)

##### Getting and Setting the Window

- [var hostWindow: NSWindow!](/documentation/webkit/webview-swift.class/hostwindow)

##### Getting and Setting Preferences

- [var preferences: WebPreferences!](/documentation/webkit/webview-swift.class/preferences)
- [var preferencesIdentifier: String!](/documentation/webkit/webview-swift.class/preferencesidentifier)

##### Getting and Setting Frame Contents

- [var isLoading: Bool](/documentation/webkit/webview-swift.class/isloading)
- [var selectedFrame: WebFrame!](/documentation/webkit/webview-swift.class/selectedframe)
- [var mainFrameURL: String!](/documentation/webkit/webview-swift.class/mainframeurl)
- [var mainFrameTitle: String!](/documentation/webkit/webview-swift.class/mainframetitle)
- [var mainFrameIcon: NSImage!](/documentation/webkit/webview-swift.class/mainframeicon)
- [var mainFrameDocument: DOMDocument!](/documentation/webkit/webview-swift.class/mainframedocument)

##### Getting and Setting Content Information

- [class func canShowMIMEType(String!) -> Bool](/documentation/webkit/webview-swift.class/canshowmimetype(_:))
- [class func mimeTypesShownAsHTML() -> [Any]!](/documentation/webkit/webview-swift.class/mimetypesshownashtml())
- [class func setMIMETypesShownAsHTML([Any]!)](/documentation/webkit/webview-swift.class/setmimetypesshownashtml(_:))
- [class func canShowMIMEType(asHTML: String!) -> Bool](/documentation/webkit/webview-swift.class/canshowmimetype(ashtml:))
- [var supportsTextEncoding: Bool](/documentation/webkit/webview-swift.class/supportstextencoding)
- [var customTextEncodingName: String!](/documentation/webkit/webview-swift.class/customtextencodingname)
- [var textSizeMultiplier: Float](/documentation/webkit/webview-swift.class/textsizemultiplier)

##### Searching the Document

- [func search(for: String!, direction: Bool, caseSensitive: Bool, wrap: Bool) -> Bool](/documentation/webkit/webview-swift.class/search(for:direction:casesensitive:wrap:))

##### Getting and Setting the Group Name

- [var groupName: String!](/documentation/webkit/webview-swift.class/groupname)

##### Getting and Setting User-agent Strings

- [func userAgent(for: URL!) -> String!](/documentation/webkit/webview-swift.class/useragent(for:))
- [var applicationNameForUserAgent: String!](/documentation/webkit/webview-swift.class/applicationnameforuseragent)
- [var customUserAgent: String!](/documentation/webkit/webview-swift.class/customuseragent)

##### Processing JavaScript

- [func stringByEvaluatingJavaScript(from: String!) -> String!](/documentation/webkit/webview-swift.class/stringbyevaluatingjavascript(from:))

##### Using the Pasteboard

- [class func url(from: NSPasteboard!) -> URL!](/documentation/webkit/webview-swift.class/url(from:))
- [class func urlTitle(from: NSPasteboard!) -> String!](/documentation/webkit/webview-swift.class/urltitle(from:))
- [func pasteboardTypes(forElement: [AnyHashable : Any]!) -> [Any]!](/documentation/webkit/webview-swift.class/pasteboardtypes(forelement:))
- [var pasteboardTypesForSelection: [Any]!](/documentation/webkit/webview-swift.class/pasteboardtypesforselection)
- [func writeElement([AnyHashable : Any]!, withPasteboardTypes: [Any]!, to: NSPasteboard!)](/documentation/webkit/webview-swift.class/writeelement(_:withpasteboardtypes:to:))
- [func writeSelection(withPasteboardTypes: [Any]!, to: NSPasteboard!)](/documentation/webkit/webview-swift.class/writeselection(withpasteboardtypes:to:))

##### Dragging

- [func element(at: NSPoint) -> [AnyHashable : Any]!](/documentation/webkit/webview-swift.class/element(at:))
- [func moveDragCaret(to: NSPoint)](/documentation/webkit/webview-swift.class/movedragcaret(to:))
- [func removeDragCaret()](/documentation/webkit/webview-swift.class/removedragcaret())

##### Cut, Copy and Paste Action Methods

- [func copy(Any?)](/documentation/webkit/webview-swift.class/copy(_:))
- [func copyFont(Any?)](/documentation/webkit/webview-swift.class/copyfont(_:))
- [func cut(Any?)](/documentation/webkit/webview-swift.class/cut(_:))
- [func delete(Any?)](/documentation/webkit/webview-swift.class/delete(_:))
- [func paste(Any?)](/documentation/webkit/webview-swift.class/paste(_:))
- [func pasteFont(Any?)](/documentation/webkit/webview-swift.class/pastefont(_:))
- [func pasteAsPlainText(Any?)](/documentation/webkit/webview-swift.class/pasteasplaintext(_:))
- [func pasteAsRichText(Any?)](/documentation/webkit/webview-swift.class/pasteasrichtext(_:))

##### Content Alignment Action Methods

- [func alignCenter(Any?)](/documentation/webkit/webview-swift.class/aligncenter(_:))
- [func alignJustified(Any?)](/documentation/webkit/webview-swift.class/alignjustified(_:))
- [func alignLeft(Any?)](/documentation/webkit/webview-swift.class/alignleft(_:))
- [func alignRight(Any?)](/documentation/webkit/webview-swift.class/alignright(_:))

##### Changing the Font, Color and Other Attributes When Editing

- [func changeFont(Any?)](/documentation/webkit/webview-swift.class/changefont(_:))
- [func changeAttributes(Any?)](/documentation/webkit/webview-swift.class/changeattributes(_:))
- [func changeDocumentBackgroundColor(Any?)](/documentation/webkit/webview-swift.class/changedocumentbackgroundcolor(_:))
- [func changeColor(Any?)](/documentation/webkit/webview-swift.class/changecolor(_:))

##### Spell-checking Action Methods

- [func checkSpelling(Any?)](/documentation/webkit/webview-swift.class/checkspelling(_:))
- [func showGuessPanel(Any?)](/documentation/webkit/webview-swift.class/showguesspanel(_:))

##### Find Panel Action Method

- [func performFindPanelAction(Any?)](/documentation/webkit/webview-swift.class/performfindpanelaction(_:))

##### Controlling Speakable Text

- [func startSpeaking(Any?)](/documentation/webkit/webview-swift.class/startspeaking(_:))
- [func stopSpeaking(Any?)](/documentation/webkit/webview-swift.class/stopspeaking(_:))

##### Getting and Setting Document Editing Attributes

- [var isEditable: Bool](/documentation/webkit/webview-swift.class/iseditable)
- [var smartInsertDeleteEnabled: Bool](/documentation/webkit/webview-swift.class/smartinsertdeleteenabled)
- [var isContinuousSpellCheckingEnabled: Bool](/documentation/webkit/webview-swift.class/iscontinuousspellcheckingenabled)
- [var spellCheckerDocumentTag: Int](/documentation/webkit/webview-swift.class/spellcheckerdocumenttag)
- [var undoManager: UndoManager!](/documentation/webkit/webview-swift.class/undomanager)
- [var editingDelegate: (any WebEditingDelegate)!](/documentation/webkit/webview-swift.class/editingdelegate)
- [func editableDOMRange(for: NSPoint) -> DOMRange!](/documentation/webkit/webview-swift.class/editabledomrange(for:))

##### Editing Documents

- [func replaceSelection(with: DOMNode!)](/documentation/webkit/webview-swift.class/replaceselection(with:)-5px9m)
- [func replaceSelection(withText: String!)](/documentation/webkit/webview-swift.class/replaceselection(withtext:))
- [func replaceSelection(withMarkupString: String!)](/documentation/webkit/webview-swift.class/replaceselection(withmarkupstring:))
- [func replaceSelection(with: WebArchive!)](/documentation/webkit/webview-swift.class/replaceselection(with:)-3vj8l)
- [func deleteSelection()](/documentation/webkit/webview-swift.class/deleteselection())
- [func moveToBeginningOfSentence(Any?)](/documentation/webkit/webview-swift.class/movetobeginningofsentence(_:))
- [func moveToBeginningOfSentenceAndModifySelection(Any?)](/documentation/webkit/webview-swift.class/movetobeginningofsentenceandmodifyselection(_:))
- [func moveToEndOfSentence(Any?)](/documentation/webkit/webview-swift.class/movetoendofsentence(_:))
- [func moveToEndOfSentenceAndModifySelection(Any?)](/documentation/webkit/webview-swift.class/movetoendofsentenceandmodifyselection(_:))
- [func selectSentence(Any?)](/documentation/webkit/webview-swift.class/selectsentence(_:))
- [func toggleContinuousSpellChecking(Any?)](/documentation/webkit/webview-swift.class/togglecontinuousspellchecking(_:))
- [func toggleSmartInsertDelete(Any?)](/documentation/webkit/webview-swift.class/togglesmartinsertdelete(_:))
- [var canMakeTextStandardSize: Bool](/documentation/webkit/webview-swift.class/canmaketextstandardsize)
- [func makeTextStandardSize(Any?)](/documentation/webkit/webview-swift.class/maketextstandardsize(_:))
- [var maintainsInactiveSelection: Bool](/documentation/webkit/webview-swift.class/maintainsinactiveselection)

##### Selecting Content in the Document

- [var selectedDOMRange: DOMRange!](/documentation/webkit/webview-swift.class/selecteddomrange)
- [func setSelectedDOMRange(DOMRange!, affinity: NSSelectionAffinity)](/documentation/webkit/webview-swift.class/setselecteddomrange(_:affinity:))
- [var selectionAffinity: NSSelectionAffinity](/documentation/webkit/webview-swift.class/selectionaffinity)

##### Getting and Setting CSS Properties

- [func computedStyle(for: DOMElement!, pseudoElement: String!) -> DOMCSSStyleDeclaration!](/documentation/webkit/webview-swift.class/computedstyle(for:pseudoelement:))
- [var mediaStyle: String!](/documentation/webkit/webview-swift.class/mediastyle)
- [var typingStyle: DOMCSSStyleDeclaration!](/documentation/webkit/webview-swift.class/typingstyle)
- [func styleDeclaration(withText: String!) -> DOMCSSStyleDeclaration!](/documentation/webkit/webview-swift.class/styledeclaration(withtext:))
- [func applyStyle(DOMCSSStyleDeclaration!)](/documentation/webkit/webview-swift.class/applystyle(_:))

##### Using WebScript

- [var windowScriptObject: WebScriptObject!](/documentation/webkit/webview-swift.class/windowscriptobject)

##### Constants

- [Element Dictionary Keys](/documentation/webkit/element-dictionary-keys)

###### Constants

- [let WebElementDOMNodeKey: String](/documentation/webkit/webelementdomnodekey)
- [let WebElementFrameKey: String](/documentation/webkit/webelementframekey)
- [let WebElementImageAltStringKey: String](/documentation/webkit/webelementimagealtstringkey)
- [let WebElementImageKey: String](/documentation/webkit/webelementimagekey)
- [let WebElementImageRectKey: String](/documentation/webkit/webelementimagerectkey)
- [let WebElementImageURLKey: String](/documentation/webkit/webelementimageurlkey)
- [let WebElementIsSelectedKey: String](/documentation/webkit/webelementisselectedkey)
- [let WebElementLinkURLKey: String](/documentation/webkit/webelementlinkurlkey)
- [let WebElementLinkTargetFrameKey: String](/documentation/webkit/webelementlinktargetframekey)
- [let WebElementLinkTitleKey: String](/documentation/webkit/webelementlinktitlekey)
- [let WebElementLinkLabelKey: String](/documentation/webkit/webelementlinklabelkey)

##### Notifications

- [static let WebViewDidBeginEditing: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidbeginediting)
- [static let WebViewDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchange)
- [static let WebViewDidChangeSelection: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchangeselection)
- [static let WebViewDidChangeTypingStyle: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidchangetypingstyle)
- [static let WebViewDidEndEditing: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewdidendediting)
- [static let WebViewProgressEstimateChanged: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressestimatechanged)
- [static let WebViewProgressFinished: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressfinished)
- [static let WebViewProgressStarted: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/webviewprogressstarted)

##### Instance Methods

- [func overWrite(Any?)](/documentation/webkit/webview-swift.class/overwrite(_:))
- [WebNavigationType](/documentation/webkit/webnavigationtype)

##### Constants

- [case linkClicked](/documentation/webkit/webnavigationtype/linkclicked)
- [case formSubmitted](/documentation/webkit/webnavigationtype/formsubmitted)
- [case backForward](/documentation/webkit/webnavigationtype/backforward)
- [case reload](/documentation/webkit/webnavigationtype/reload)
- [case formResubmitted](/documentation/webkit/webnavigationtype/formresubmitted)
- [case other](/documentation/webkit/webnavigationtype/other)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/webnavigationtype/init(rawvalue:))
- [WebViewInsertAction](/documentation/webkit/webviewinsertaction)

##### Constants

- [case typed](/documentation/webkit/webviewinsertaction/typed)
- [case pasted](/documentation/webkit/webviewinsertaction/pasted)
- [case dropped](/documentation/webkit/webviewinsertaction/dropped)

##### Initializers

- [init?(rawValue: Int)](/documentation/webkit/webviewinsertaction/init(rawvalue:))
- [WebKit for SwiftUI](/documentation/webkit/webkit-for-swiftui)

### Essentials

- [WebView](/documentation/webkit/webview-swift.struct)

#### Creating web views

- [init(WebPage)](/documentation/webkit/webview-swift.struct/init(_:))
- [init(url: URL?)](/documentation/webkit/webview-swift.struct/init(url:))

#### Modifying web interactions

- [WebView.BackForwardNavigationGesturesBehavior](/documentation/webkit/webview-swift.struct/backforwardnavigationgesturesbehavior)

##### Type Properties

- [static let automatic: WebView.BackForwardNavigationGesturesBehavior](/documentation/webkit/webview-swift.struct/backforwardnavigationgesturesbehavior/automatic)
- [static let disabled: WebView.BackForwardNavigationGesturesBehavior](/documentation/webkit/webview-swift.struct/backforwardnavigationgesturesbehavior/disabled)
- [static let enabled: WebView.BackForwardNavigationGesturesBehavior](/documentation/webkit/webview-swift.struct/backforwardnavigationgesturesbehavior/enabled)
- [WebView.LinkPreviewBehavior](/documentation/webkit/webview-swift.struct/linkpreviewbehavior)

##### Type Properties

- [static let automatic: WebView.LinkPreviewBehavior](/documentation/webkit/webview-swift.struct/linkpreviewbehavior/automatic)
- [static let disabled: WebView.LinkPreviewBehavior](/documentation/webkit/webview-swift.struct/linkpreviewbehavior/disabled)
- [static let enabled: WebView.LinkPreviewBehavior](/documentation/webkit/webview-swift.struct/linkpreviewbehavior/enabled)
- [WebView.ActivatedElementInfo](/documentation/webkit/webview-swift.struct/activatedelementinfo)

##### Instance Properties

- [let linkURL: URL?](/documentation/webkit/webview-swift.struct/activatedelementinfo/linkurl)
- [WebView.ElementFullscreenBehavior](/documentation/webkit/webview-swift.struct/elementfullscreenbehavior)

##### Type Properties

- [static let automatic: WebView.ElementFullscreenBehavior](/documentation/webkit/webview-swift.struct/elementfullscreenbehavior/automatic)
- [static let disabled: WebView.ElementFullscreenBehavior](/documentation/webkit/webview-swift.struct/elementfullscreenbehavior/disabled)
- [static let enabled: WebView.ElementFullscreenBehavior](/documentation/webkit/webview-swift.struct/elementfullscreenbehavior/enabled)
- [WebView.MagnificationGesturesBehavior](/documentation/webkit/webview-swift.struct/magnificationgesturesbehavior)

##### Type Properties

- [static let automatic: WebView.MagnificationGesturesBehavior](/documentation/webkit/webview-swift.struct/magnificationgesturesbehavior/automatic)
- [static let disabled: WebView.MagnificationGesturesBehavior](/documentation/webkit/webview-swift.struct/magnificationgesturesbehavior/disabled)
- [static let enabled: WebView.MagnificationGesturesBehavior](/documentation/webkit/webview-swift.struct/magnificationgesturesbehavior/enabled)
- [WebPage](/documentation/webkit/webpage)

#### Creating a WebPage

- [WebPage.Configuration](/documentation/webkit/webpage/configuration)

##### Initializers

- [init()](/documentation/webkit/webpage/configuration/init())

##### Instance Properties

- [var allowsAirPlayForMediaPlayback: Bool](/documentation/webkit/webpage/configuration/allowsairplayformediaplayback)
- [var allowsInlinePredictions: Bool](/documentation/webkit/webpage/configuration/allowsinlinepredictions)
- [var applicationNameForUserAgent: String?](/documentation/webkit/webpage/configuration/applicationnameforuseragent)
- [var dataDetectorTypes: WKDataDetectorTypes](/documentation/webkit/webpage/configuration/datadetectortypes)
- [var defaultNavigationPreferences: WebPage.NavigationPreferences](/documentation/webkit/webpage/configuration/defaultnavigationpreferences)
- [var deviceSensorAuthorization: WebPage.DeviceSensorAuthorization](/documentation/webkit/webpage/configuration/devicesensorauthorization)
- [var ignoresViewportScaleLimits: Bool](/documentation/webkit/webpage/configuration/ignoresviewportscalelimits)
- [var limitsNavigationsToAppBoundDomains: Bool](/documentation/webkit/webpage/configuration/limitsnavigationstoappbounddomains)
- [var loadsSubresources: Bool](/documentation/webkit/webpage/configuration/loadssubresources)
- [var mediaPlaybackBehavior: WebPage.Configuration.MediaPlaybackBehavior](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.property)
- [var showsSystemScreenTimeBlockingView: Bool](/documentation/webkit/webpage/configuration/showssystemscreentimeblockingview)
- [var supportsAdaptiveImageGlyph: Bool](/documentation/webkit/webpage/configuration/supportsadaptiveimageglyph)
- [var suppressesIncrementalRendering: Bool](/documentation/webkit/webpage/configuration/suppressesincrementalrendering)
- [var upgradeKnownHostsToHTTPS: Bool](/documentation/webkit/webpage/configuration/upgradeknownhoststohttps)
- [var urlSchemeHandlers: [URLScheme : any URLSchemeHandler]](/documentation/webkit/webpage/configuration/urlschemehandlers)
- [var userContentController: WKUserContentController](/documentation/webkit/webpage/configuration/usercontentcontroller)
- [var userInterfaceDirectionPolicy: WKUserInterfaceDirectionPolicy](/documentation/webkit/webpage/configuration/userinterfacedirectionpolicy)
- [var webExtensionController: WKWebExtensionController?](/documentation/webkit/webpage/configuration/webextensioncontroller)
- [var websiteDataStore: WKWebsiteDataStore](/documentation/webkit/webpage/configuration/websitedatastore)

##### Enumerations

- [WebPage.Configuration.MediaPlaybackBehavior](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum)

###### Enumeration Cases

- [case allowsInlinePlayback](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/allowsinlineplayback)
- [case alwaysFullscreen](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/alwaysfullscreen)
- [case automatic](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/automatic)
- [convenience init(configuration: WebPage.Configuration)](/documentation/webkit/webpage/init(configuration:))
- [convenience init(configuration: WebPage.Configuration, dialogPresenter: some WebPage.DialogPresenting)](/documentation/webkit/webpage/init(configuration:dialogpresenter:))
- [convenience init(configuration: WebPage.Configuration, navigationDecider: some WebPage.NavigationDeciding)](/documentation/webkit/webpage/init(configuration:navigationdecider:))
- [convenience init(configuration: WebPage.Configuration, navigationDecider: some WebPage.NavigationDeciding, dialogPresenter: some WebPage.DialogPresenting)](/documentation/webkit/webpage/init(configuration:navigationdecider:dialogpresenter:))

#### Managing navigation between webpages

- [WebPage.NavigationDeciding](/documentation/webkit/webpage/navigationdeciding)

##### Instance Methods

- [func decideAuthenticationChallengeDisposition(for: URLAuthenticationChallenge) async -> (URLSession.AuthChallengeDisposition, URLCredential?)](/documentation/webkit/webpage/navigationdeciding/decideauthenticationchallengedisposition(for:))
- [func decidePolicy(for: WebPage.NavigationResponse) async -> WKNavigationResponsePolicy](/documentation/webkit/webpage/navigationdeciding/decidepolicy(for:))
- [func decidePolicy(for: WebPage.NavigationAction, preferences: inout WebPage.NavigationPreferences) async -> WKNavigationActionPolicy](/documentation/webkit/webpage/navigationdeciding/decidepolicy(for:preferences:))
- [WebPage.NavigationAction](/documentation/webkit/webpage/navigationaction)

##### Instance Properties

- [var buttonNumber: Int](/documentation/webkit/webpage/navigationaction/buttonnumber-29qsu)
- [var buttonNumber: UIEvent.ButtonMask](/documentation/webkit/webpage/navigationaction/buttonnumber-4sg9k)
- [var isContentRuleListRedirect: Bool](/documentation/webkit/webpage/navigationaction/iscontentrulelistredirect)
- [var modifierFlags: EventModifiers](/documentation/webkit/webpage/navigationaction/modifierflags)
- [var navigationType: WKNavigationType](/documentation/webkit/webpage/navigationaction/navigationtype)
- [var request: URLRequest](/documentation/webkit/webpage/navigationaction/request)
- [var shouldPerformDownload: Bool](/documentation/webkit/webpage/navigationaction/shouldperformdownload)
- [var source: WebPage.FrameInfo](/documentation/webkit/webpage/navigationaction/source)
- [var target: WebPage.FrameInfo?](/documentation/webkit/webpage/navigationaction/target)
- [WebPage.NavigationResponse](/documentation/webkit/webpage/navigationresponse)

##### Instance Properties

- [var canShowMimeType: Bool](/documentation/webkit/webpage/navigationresponse/canshowmimetype)
- [var response: URLResponse](/documentation/webkit/webpage/navigationresponse/response)
- [WebPage.NavigationPreferences](/documentation/webkit/webpage/navigationpreferences)

##### Initializers

- [init()](/documentation/webkit/webpage/navigationpreferences/init())

##### Instance Properties

- [var allowsContentJavaScript: Bool](/documentation/webkit/webpage/navigationpreferences/allowscontentjavascript)
- [var isLockdownModeEnabled: Bool](/documentation/webkit/webpage/navigationpreferences/islockdownmodeenabled)
- [var preferredContentMode: WebPage.NavigationPreferences.ContentMode](/documentation/webkit/webpage/navigationpreferences/preferredcontentmode)
- [var preferredHTTPSNavigationPolicy: WebPage.NavigationPreferences.UpgradeToHTTPSPolicy](/documentation/webkit/webpage/navigationpreferences/preferredhttpsnavigationpolicy)

##### Enumerations

- [WebPage.NavigationPreferences.ContentMode](/documentation/webkit/webpage/navigationpreferences/contentmode)

###### Enumeration Cases

- [case desktop](/documentation/webkit/webpage/navigationpreferences/contentmode/desktop)
- [case mobile](/documentation/webkit/webpage/navigationpreferences/contentmode/mobile)
- [case recommended](/documentation/webkit/webpage/navigationpreferences/contentmode/recommended)
- [WebPage.NavigationPreferences.UpgradeToHTTPSPolicy](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy)

###### Enumeration Cases

- [case automaticFallbackToHTTP](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/automaticfallbacktohttp)
- [case errorOnFailure](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/erroronfailure)
- [case keepAsRequested](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/keepasrequested)
- [case userMediatedFallbackToHTTP](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/usermediatedfallbacktohttp)
- [var backForwardList: WebPage.BackForwardList](/documentation/webkit/webpage/backforwardlist-swift.property)
- [WebPage.FrameInfo](/documentation/webkit/webpage/frameinfo)

##### Instance Properties

- [var isMainFrame: Bool](/documentation/webkit/webpage/frameinfo/ismainframe)
- [var request: URLRequest](/documentation/webkit/webpage/frameinfo/request)
- [var securityOrigin: WKSecurityOrigin](/documentation/webkit/webpage/frameinfo/securityorigin)

#### Observing navigation between webpages

- [WebPage.BackForwardList](/documentation/webkit/webpage/backforwardlist-swift.struct)

##### Structures

- [WebPage.BackForwardList.Item](/documentation/webkit/webpage/backforwardlist-swift.struct/item)

###### Structures

- [WebPage.BackForwardList.Item.ID](/documentation/webkit/webpage/backforwardlist-swift.struct/item/id-swift.struct)

###### Instance Properties

- [let id: WebPage.BackForwardList.Item.ID](/documentation/webkit/webpage/backforwardlist-swift.struct/item/id-swift.property)
- [let initialURL: URL](/documentation/webkit/webpage/backforwardlist-swift.struct/item/initialurl)
- [let title: String?](/documentation/webkit/webpage/backforwardlist-swift.struct/item/title)
- [let url: URL](/documentation/webkit/webpage/backforwardlist-swift.struct/item/url)

##### Instance Properties

- [var backList: [WebPage.BackForwardList.Item]](/documentation/webkit/webpage/backforwardlist-swift.struct/backlist)
- [var currentItem: WebPage.BackForwardList.Item?](/documentation/webkit/webpage/backforwardlist-swift.struct/currentitem)
- [var forwardList: [WebPage.BackForwardList.Item]](/documentation/webkit/webpage/backforwardlist-swift.struct/forwardlist)

##### Subscripts

- [subscript(Int) -> WebPage.BackForwardList.Item?](/documentation/webkit/webpage/backforwardlist-swift.struct/subscript(_:))
- [WebPage.NavigationEvent](/documentation/webkit/webpage/navigationevent)

##### Enumeration Cases

- [case committed](/documentation/webkit/webpage/navigationevent/committed)
- [case finished](/documentation/webkit/webpage/navigationevent/finished)
- [case receivedServerRedirect](/documentation/webkit/webpage/navigationevent/receivedserverredirect)
- [case startedProvisionalNavigation](/documentation/webkit/webpage/navigationevent/startedprovisionalnavigation)
- [var navigations: some AsyncSequence<WebPage.NavigationEvent, any Error>](/documentation/webkit/webpage/navigations)
- [WebPage.NavigationError](/documentation/webkit/webpage/navigationerror)

##### Enumeration Cases

- [case failedProvisionalNavigation(any Error)](/documentation/webkit/webpage/navigationerror/failedprovisionalnavigation(_:))
- [case invalidURL](/documentation/webkit/webpage/navigationerror/invalidurl)
- [case pageClosed](/documentation/webkit/webpage/navigationerror/pageclosed)
- [case webContentProcessTerminated](/documentation/webkit/webpage/navigationerror/webcontentprocessterminated)

#### Configuring a WebPage

- [WebPage.Configuration](/documentation/webkit/webpage/configuration)

##### Initializers

- [init()](/documentation/webkit/webpage/configuration/init())

##### Instance Properties

- [var allowsAirPlayForMediaPlayback: Bool](/documentation/webkit/webpage/configuration/allowsairplayformediaplayback)
- [var allowsInlinePredictions: Bool](/documentation/webkit/webpage/configuration/allowsinlinepredictions)
- [var applicationNameForUserAgent: String?](/documentation/webkit/webpage/configuration/applicationnameforuseragent)
- [var dataDetectorTypes: WKDataDetectorTypes](/documentation/webkit/webpage/configuration/datadetectortypes)
- [var defaultNavigationPreferences: WebPage.NavigationPreferences](/documentation/webkit/webpage/configuration/defaultnavigationpreferences)
- [var deviceSensorAuthorization: WebPage.DeviceSensorAuthorization](/documentation/webkit/webpage/configuration/devicesensorauthorization)
- [var ignoresViewportScaleLimits: Bool](/documentation/webkit/webpage/configuration/ignoresviewportscalelimits)
- [var limitsNavigationsToAppBoundDomains: Bool](/documentation/webkit/webpage/configuration/limitsnavigationstoappbounddomains)
- [var loadsSubresources: Bool](/documentation/webkit/webpage/configuration/loadssubresources)
- [var mediaPlaybackBehavior: WebPage.Configuration.MediaPlaybackBehavior](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.property)
- [var showsSystemScreenTimeBlockingView: Bool](/documentation/webkit/webpage/configuration/showssystemscreentimeblockingview)
- [var supportsAdaptiveImageGlyph: Bool](/documentation/webkit/webpage/configuration/supportsadaptiveimageglyph)
- [var suppressesIncrementalRendering: Bool](/documentation/webkit/webpage/configuration/suppressesincrementalrendering)
- [var upgradeKnownHostsToHTTPS: Bool](/documentation/webkit/webpage/configuration/upgradeknownhoststohttps)
- [var urlSchemeHandlers: [URLScheme : any URLSchemeHandler]](/documentation/webkit/webpage/configuration/urlschemehandlers)
- [var userContentController: WKUserContentController](/documentation/webkit/webpage/configuration/usercontentcontroller)
- [var userInterfaceDirectionPolicy: WKUserInterfaceDirectionPolicy](/documentation/webkit/webpage/configuration/userinterfacedirectionpolicy)
- [var webExtensionController: WKWebExtensionController?](/documentation/webkit/webpage/configuration/webextensioncontroller)
- [var websiteDataStore: WKWebsiteDataStore](/documentation/webkit/webpage/configuration/websitedatastore)

##### Enumerations

- [WebPage.Configuration.MediaPlaybackBehavior](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum)

###### Enumeration Cases

- [case allowsInlinePlayback](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/allowsinlineplayback)
- [case alwaysFullscreen](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/alwaysfullscreen)
- [case automatic](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/automatic)
- [WebPage.DeviceSensorAuthorization](/documentation/webkit/webpage/devicesensorauthorization)

##### Initializers

- [init(decision: WKPermissionDecision)](/documentation/webkit/webpage/devicesensorauthorization/init(decision:))
- [init(decisionHandler: (WebPage.DeviceSensorAuthorization.Permission, WebPage.FrameInfo, WKSecurityOrigin) async -> WKPermissionDecision)](/documentation/webkit/webpage/devicesensorauthorization/init(decisionhandler:))

##### Enumerations

- [WebPage.DeviceSensorAuthorization.Permission](/documentation/webkit/webpage/devicesensorauthorization/permission)

###### Enumeration Cases

- [case deviceOrientationAndMotion](/documentation/webkit/webpage/devicesensorauthorization/permission/deviceorientationandmotion)
- [case mediaCapture(WKMediaCaptureType)](/documentation/webkit/webpage/devicesensorauthorization/permission/mediacapture(_:))
- [URLScheme](/documentation/webkit/urlscheme)

##### Initializers

- [init?(String)](/documentation/webkit/urlscheme/init(_:))

##### Instance Properties

- [let rawValue: String](/documentation/webkit/urlscheme/rawvalue)
- [URLSchemeHandler](/documentation/webkit/urlschemehandler)

##### Associated Types

- [TaskSequence](/documentation/webkit/urlschemehandler/tasksequence)

##### Instance Methods

- [func reply(for: URLRequest) -> Self.TaskSequence](/documentation/webkit/urlschemehandler/reply(for:))
- [URLSchemeTaskResult](/documentation/webkit/urlschemetaskresult)

##### Enumeration Cases

- [case data(Data)](/documentation/webkit/urlschemetaskresult/data(_:))
- [case response(URLResponse)](/documentation/webkit/urlschemetaskresult/response(_:))

#### Loading web content

- [func load(WebPage.BackForwardList.Item) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/load(_:)-32ngj)
- [func load(URLRequest) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/load(_:)-7kw3h)
- [func load(URL?) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/load(_:)-8wfiq)
- [func load(Data, mimeType: String, characterEncoding: String.Encoding, baseURL: URL) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/load(_:mimetype:characterencoding:baseurl:))
- [func load(html: String, baseURL: URL) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/load(html:baseurl:))
- [func load(simulatedRequest: URLRequest, responseHTML: String) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/load(simulatedrequest:responsehtml:))
- [func load(simulatedRequest: URLRequest, response: URLResponse, responseData: Data) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/load(simulatedrequest:response:responsedata:))
- [var isLoading: Bool](/documentation/webkit/webpage/isloading)
- [var estimatedProgress: Double](/documentation/webkit/webpage/estimatedprogress)

#### Managing the loading process

- [func reload(fromOrigin: Bool) -> some AsyncSequence<WebPage.NavigationEvent, any Error>
](/documentation/webkit/webpage/reload(fromorigin:))
- [func stopLoading()](/documentation/webkit/webpage/stoploading())

#### Inspecting page information

- [WebPage.CSSMediaType](/documentation/webkit/webpage/cssmediatype)

##### Initializers

- [init(rawValue: String)](/documentation/webkit/webpage/cssmediatype/init(rawvalue:))

##### Instance Properties

- [let rawValue: String](/documentation/webkit/webpage/cssmediatype/rawvalue)

##### Type Properties

- [static let all: WebPage.CSSMediaType](/documentation/webkit/webpage/cssmediatype/all)
- [static let print: WebPage.CSSMediaType](/documentation/webkit/webpage/cssmediatype/print)
- [static let screen: WebPage.CSSMediaType](/documentation/webkit/webpage/cssmediatype/screen)
- [var title: String](/documentation/webkit/webpage/title)
- [var url: URL?](/documentation/webkit/webpage/url)
- [var mediaType: WebPage.CSSMediaType?](/documentation/webkit/webpage/mediatype)
- [var customUserAgent: String?](/documentation/webkit/webpage/customuseragent)
- [var serverTrust: SecTrust?](/documentation/webkit/webpage/servertrust)
- [var hasOnlySecureContent: Bool](/documentation/webkit/webpage/hasonlysecurecontent)
- [var themeColor: Color?](/documentation/webkit/webpage/themecolor)
- [var isBlockedByScreenTime: Bool](/documentation/webkit/webpage/isblockedbyscreentime)
- [var isInspectable: Bool](/documentation/webkit/webpage/isinspectable)
- [var isWritingToolsActive: Bool](/documentation/webkit/webpage/iswritingtoolsactive)

#### Executing JavaScript

- [func callJavaScript(String, arguments: [String : Any], in: WebPage.FrameInfo?, contentWorld: WKContentWorld?) async throws -> sending Any?](/documentation/webkit/webpage/calljavascript(_:arguments:in:contentworld:))

#### Customizing JavaScript dialogs

- [WebPage.DialogPresenting](/documentation/webkit/webpage/dialogpresenting)

##### Instance Methods

- [func handleFileInputPrompt(parameters: WKOpenPanelParameters, initiatedBy: WebPage.FrameInfo) async -> WebPage.FileInputPromptResult](/documentation/webkit/webpage/dialogpresenting/handlefileinputprompt(parameters:initiatedby:))
- [func handleJavaScriptAlert(message: String, initiatedBy: WebPage.FrameInfo) async](/documentation/webkit/webpage/dialogpresenting/handlejavascriptalert(message:initiatedby:))
- [func handleJavaScriptConfirm(message: String, initiatedBy: WebPage.FrameInfo) async -> WebPage.JavaScriptConfirmResult](/documentation/webkit/webpage/dialogpresenting/handlejavascriptconfirm(message:initiatedby:))
- [func handleJavaScriptPrompt(message: String, defaultText: String?, initiatedBy: WebPage.FrameInfo) async -> WebPage.JavaScriptPromptResult](/documentation/webkit/webpage/dialogpresenting/handlejavascriptprompt(message:defaulttext:initiatedby:))
- [WebPage.FileInputPromptResult](/documentation/webkit/webpage/fileinputpromptresult)

##### Enumeration Cases

- [case cancel](/documentation/webkit/webpage/fileinputpromptresult/cancel)
- [case selected([URL])](/documentation/webkit/webpage/fileinputpromptresult/selected(_:))
- [WebPage.JavaScriptConfirmResult](/documentation/webkit/webpage/javascriptconfirmresult)

##### Enumeration Cases

- [case cancel](/documentation/webkit/webpage/javascriptconfirmresult/cancel)
- [case ok](/documentation/webkit/webpage/javascriptconfirmresult/ok)
- [WebPage.JavaScriptPromptResult](/documentation/webkit/webpage/javascriptpromptresult)

##### Enumeration Cases

- [case cancel](/documentation/webkit/webpage/javascriptpromptresult/cancel)
- [case ok(String)](/documentation/webkit/webpage/javascriptpromptresult/ok(_:))

#### Exporting webpage content

- [WebPage.ExportedContentConfiguration](/documentation/webkit/webpage/exportedcontentconfiguration)

##### Configurable types

- [WebPage.ExportedContentConfiguration.Region](/documentation/webkit/webpage/exportedcontentconfiguration/region)

###### Type Properties

- [static var contents: WebPage.ExportedContentConfiguration.Region](/documentation/webkit/webpage/exportedcontentconfiguration/region/contents)

###### Type Methods

- [static func rect(CGRect) -> WebPage.ExportedContentConfiguration.Region](/documentation/webkit/webpage/exportedcontentconfiguration/region/rect(_:))
- [static func image(region: WebPage.ExportedContentConfiguration.Region, allowTransparentBackground: Bool, snapshotWidth: CGFloat?, afterScreenUpdates: Bool) -> WebPage.ExportedContentConfiguration](/documentation/webkit/webpage/exportedcontentconfiguration/image(region:allowtransparentbackground:snapshotwidth:afterscreenupdates:))
- [static func pdf(region: WebPage.ExportedContentConfiguration.Region, allowTransparentBackground: Bool) -> WebPage.ExportedContentConfiguration](/documentation/webkit/webpage/exportedcontentconfiguration/pdf(region:allowtransparentbackground:))
- [func exported(as: WebPage.ExportedContentConfiguration) async throws -> Data](/documentation/webkit/webpage/exported(as:))

#### Interacting with media

- [WebPage.FullscreenState](/documentation/webkit/webpage/fullscreenstate-swift.enum)

##### Enumeration Cases

- [case enteringFullscreen](/documentation/webkit/webpage/fullscreenstate-swift.enum/enteringfullscreen)
- [case exitingFullscreen](/documentation/webkit/webpage/fullscreenstate-swift.enum/exitingfullscreen)
- [case inFullscreen](/documentation/webkit/webpage/fullscreenstate-swift.enum/infullscreen)
- [case notInFullscreen](/documentation/webkit/webpage/fullscreenstate-swift.enum/notinfullscreen)
- [func pauseAllMediaPlayback() async](/documentation/webkit/webpage/pauseallmediaplayback())
- [func mediaPlaybackState() async -> WKMediaPlaybackState](/documentation/webkit/webpage/mediaplaybackstate())
- [func setAllMediaPlaybackSuspended(Bool) async](/documentation/webkit/webpage/setallmediaplaybacksuspended(_:))
- [func closeAllMediaPresentations() async](/documentation/webkit/webpage/closeallmediapresentations())
- [var fullscreenState: WebPage.FullscreenState](/documentation/webkit/webpage/fullscreenstate-swift.property)

#### Managing the microphone and camera

- [var cameraCaptureState: WKMediaCaptureState](/documentation/webkit/webpage/cameracapturestate)
- [var microphoneCaptureState: WKMediaCaptureState](/documentation/webkit/webpage/microphonecapturestate)
- [func setCameraCaptureState(WKMediaCaptureState) async](/documentation/webkit/webpage/setcameracapturestate(_:))
- [func setMicrophoneCaptureState(WKMediaCaptureState) async](/documentation/webkit/webpage/setmicrophonecapturestate(_:))

### Managing navigation between webpages

- [WebPage.NavigationDeciding](/documentation/webkit/webpage/navigationdeciding)

#### Instance Methods

- [func decideAuthenticationChallengeDisposition(for: URLAuthenticationChallenge) async -> (URLSession.AuthChallengeDisposition, URLCredential?)](/documentation/webkit/webpage/navigationdeciding/decideauthenticationchallengedisposition(for:))
- [func decidePolicy(for: WebPage.NavigationResponse) async -> WKNavigationResponsePolicy](/documentation/webkit/webpage/navigationdeciding/decidepolicy(for:))
- [func decidePolicy(for: WebPage.NavigationAction, preferences: inout WebPage.NavigationPreferences) async -> WKNavigationActionPolicy](/documentation/webkit/webpage/navigationdeciding/decidepolicy(for:preferences:))
- [WebPage.NavigationAction](/documentation/webkit/webpage/navigationaction)

#### Instance Properties

- [var buttonNumber: Int](/documentation/webkit/webpage/navigationaction/buttonnumber-29qsu)
- [var buttonNumber: UIEvent.ButtonMask](/documentation/webkit/webpage/navigationaction/buttonnumber-4sg9k)
- [var isContentRuleListRedirect: Bool](/documentation/webkit/webpage/navigationaction/iscontentrulelistredirect)
- [var modifierFlags: EventModifiers](/documentation/webkit/webpage/navigationaction/modifierflags)
- [var navigationType: WKNavigationType](/documentation/webkit/webpage/navigationaction/navigationtype)
- [var request: URLRequest](/documentation/webkit/webpage/navigationaction/request)
- [var shouldPerformDownload: Bool](/documentation/webkit/webpage/navigationaction/shouldperformdownload)
- [var source: WebPage.FrameInfo](/documentation/webkit/webpage/navigationaction/source)
- [var target: WebPage.FrameInfo?](/documentation/webkit/webpage/navigationaction/target)
- [WebPage.NavigationResponse](/documentation/webkit/webpage/navigationresponse)

#### Instance Properties

- [var canShowMimeType: Bool](/documentation/webkit/webpage/navigationresponse/canshowmimetype)
- [var response: URLResponse](/documentation/webkit/webpage/navigationresponse/response)
- [WebPage.NavigationPreferences](/documentation/webkit/webpage/navigationpreferences)

#### Initializers

- [init()](/documentation/webkit/webpage/navigationpreferences/init())

#### Instance Properties

- [var allowsContentJavaScript: Bool](/documentation/webkit/webpage/navigationpreferences/allowscontentjavascript)
- [var isLockdownModeEnabled: Bool](/documentation/webkit/webpage/navigationpreferences/islockdownmodeenabled)
- [var preferredContentMode: WebPage.NavigationPreferences.ContentMode](/documentation/webkit/webpage/navigationpreferences/preferredcontentmode)
- [var preferredHTTPSNavigationPolicy: WebPage.NavigationPreferences.UpgradeToHTTPSPolicy](/documentation/webkit/webpage/navigationpreferences/preferredhttpsnavigationpolicy)

#### Enumerations

- [WebPage.NavigationPreferences.ContentMode](/documentation/webkit/webpage/navigationpreferences/contentmode)

##### Enumeration Cases

- [case desktop](/documentation/webkit/webpage/navigationpreferences/contentmode/desktop)
- [case mobile](/documentation/webkit/webpage/navigationpreferences/contentmode/mobile)
- [case recommended](/documentation/webkit/webpage/navigationpreferences/contentmode/recommended)
- [WebPage.NavigationPreferences.UpgradeToHTTPSPolicy](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy)

##### Enumeration Cases

- [case automaticFallbackToHTTP](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/automaticfallbacktohttp)
- [case errorOnFailure](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/erroronfailure)
- [case keepAsRequested](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/keepasrequested)
- [case userMediatedFallbackToHTTP](/documentation/webkit/webpage/navigationpreferences/upgradetohttpspolicy/usermediatedfallbacktohttp)
- [WebPage.FrameInfo](/documentation/webkit/webpage/frameinfo)

#### Instance Properties

- [var isMainFrame: Bool](/documentation/webkit/webpage/frameinfo/ismainframe)
- [var request: URLRequest](/documentation/webkit/webpage/frameinfo/request)
- [var securityOrigin: WKSecurityOrigin](/documentation/webkit/webpage/frameinfo/securityorigin)

### Observing navigation between webpages

- [WebPage.BackForwardList](/documentation/webkit/webpage/backforwardlist-swift.struct)

#### Structures

- [WebPage.BackForwardList.Item](/documentation/webkit/webpage/backforwardlist-swift.struct/item)

##### Structures

- [WebPage.BackForwardList.Item.ID](/documentation/webkit/webpage/backforwardlist-swift.struct/item/id-swift.struct)

##### Instance Properties

- [let id: WebPage.BackForwardList.Item.ID](/documentation/webkit/webpage/backforwardlist-swift.struct/item/id-swift.property)
- [let initialURL: URL](/documentation/webkit/webpage/backforwardlist-swift.struct/item/initialurl)
- [let title: String?](/documentation/webkit/webpage/backforwardlist-swift.struct/item/title)
- [let url: URL](/documentation/webkit/webpage/backforwardlist-swift.struct/item/url)

#### Instance Properties

- [var backList: [WebPage.BackForwardList.Item]](/documentation/webkit/webpage/backforwardlist-swift.struct/backlist)
- [var currentItem: WebPage.BackForwardList.Item?](/documentation/webkit/webpage/backforwardlist-swift.struct/currentitem)
- [var forwardList: [WebPage.BackForwardList.Item]](/documentation/webkit/webpage/backforwardlist-swift.struct/forwardlist)

#### Subscripts

- [subscript(Int) -> WebPage.BackForwardList.Item?](/documentation/webkit/webpage/backforwardlist-swift.struct/subscript(_:))
- [WebPage.NavigationEvent](/documentation/webkit/webpage/navigationevent)

#### Enumeration Cases

- [case committed](/documentation/webkit/webpage/navigationevent/committed)
- [case finished](/documentation/webkit/webpage/navigationevent/finished)
- [case receivedServerRedirect](/documentation/webkit/webpage/navigationevent/receivedserverredirect)
- [case startedProvisionalNavigation](/documentation/webkit/webpage/navigationevent/startedprovisionalnavigation)

### Configuring a WebPage

- [WebPage.Configuration](/documentation/webkit/webpage/configuration)

#### Initializers

- [init()](/documentation/webkit/webpage/configuration/init())

#### Instance Properties

- [var allowsAirPlayForMediaPlayback: Bool](/documentation/webkit/webpage/configuration/allowsairplayformediaplayback)
- [var allowsInlinePredictions: Bool](/documentation/webkit/webpage/configuration/allowsinlinepredictions)
- [var applicationNameForUserAgent: String?](/documentation/webkit/webpage/configuration/applicationnameforuseragent)
- [var dataDetectorTypes: WKDataDetectorTypes](/documentation/webkit/webpage/configuration/datadetectortypes)
- [var defaultNavigationPreferences: WebPage.NavigationPreferences](/documentation/webkit/webpage/configuration/defaultnavigationpreferences)
- [var deviceSensorAuthorization: WebPage.DeviceSensorAuthorization](/documentation/webkit/webpage/configuration/devicesensorauthorization)
- [var ignoresViewportScaleLimits: Bool](/documentation/webkit/webpage/configuration/ignoresviewportscalelimits)
- [var limitsNavigationsToAppBoundDomains: Bool](/documentation/webkit/webpage/configuration/limitsnavigationstoappbounddomains)
- [var loadsSubresources: Bool](/documentation/webkit/webpage/configuration/loadssubresources)
- [var mediaPlaybackBehavior: WebPage.Configuration.MediaPlaybackBehavior](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.property)
- [var showsSystemScreenTimeBlockingView: Bool](/documentation/webkit/webpage/configuration/showssystemscreentimeblockingview)
- [var supportsAdaptiveImageGlyph: Bool](/documentation/webkit/webpage/configuration/supportsadaptiveimageglyph)
- [var suppressesIncrementalRendering: Bool](/documentation/webkit/webpage/configuration/suppressesincrementalrendering)
- [var upgradeKnownHostsToHTTPS: Bool](/documentation/webkit/webpage/configuration/upgradeknownhoststohttps)
- [var urlSchemeHandlers: [URLScheme : any URLSchemeHandler]](/documentation/webkit/webpage/configuration/urlschemehandlers)
- [var userContentController: WKUserContentController](/documentation/webkit/webpage/configuration/usercontentcontroller)
- [var userInterfaceDirectionPolicy: WKUserInterfaceDirectionPolicy](/documentation/webkit/webpage/configuration/userinterfacedirectionpolicy)
- [var webExtensionController: WKWebExtensionController?](/documentation/webkit/webpage/configuration/webextensioncontroller)
- [var websiteDataStore: WKWebsiteDataStore](/documentation/webkit/webpage/configuration/websitedatastore)

#### Enumerations

- [WebPage.Configuration.MediaPlaybackBehavior](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum)

##### Enumeration Cases

- [case allowsInlinePlayback](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/allowsinlineplayback)
- [case alwaysFullscreen](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/alwaysfullscreen)
- [case automatic](/documentation/webkit/webpage/configuration/mediaplaybackbehavior-swift.enum/automatic)
- [WebPage.DeviceSensorAuthorization](/documentation/webkit/webpage/devicesensorauthorization)

#### Initializers

- [init(decision: WKPermissionDecision)](/documentation/webkit/webpage/devicesensorauthorization/init(decision:))
- [init(decisionHandler: (WebPage.DeviceSensorAuthorization.Permission, WebPage.FrameInfo, WKSecurityOrigin) async -> WKPermissionDecision)](/documentation/webkit/webpage/devicesensorauthorization/init(decisionhandler:))

#### Enumerations

- [WebPage.DeviceSensorAuthorization.Permission](/documentation/webkit/webpage/devicesensorauthorization/permission)

##### Enumeration Cases

- [case deviceOrientationAndMotion](/documentation/webkit/webpage/devicesensorauthorization/permission/deviceorientationandmotion)
- [case mediaCapture(WKMediaCaptureType)](/documentation/webkit/webpage/devicesensorauthorization/permission/mediacapture(_:))
- [URLScheme](/documentation/webkit/urlscheme)

#### Initializers

- [init?(String)](/documentation/webkit/urlscheme/init(_:))

#### Instance Properties

- [let rawValue: String](/documentation/webkit/urlscheme/rawvalue)
- [URLSchemeHandler](/documentation/webkit/urlschemehandler)

#### Associated Types

- [TaskSequence](/documentation/webkit/urlschemehandler/tasksequence)

#### Instance Methods

- [func reply(for: URLRequest) -> Self.TaskSequence](/documentation/webkit/urlschemehandler/reply(for:))
- [URLSchemeTaskResult](/documentation/webkit/urlschemetaskresult)

#### Enumeration Cases

- [case data(Data)](/documentation/webkit/urlschemetaskresult/data(_:))
- [case response(URLResponse)](/documentation/webkit/urlschemetaskresult/response(_:))

## Safari Support

- [Optimizing Your Website for Safari](/documentation/webkit/optimizing-your-website-for-safari)
- [Delivering Video Content for Safari](/documentation/webkit/delivering-video-content-for-safari)
- [Promoting Apps with Smart App Banners](/documentation/webkit/promoting-apps-with-smart-app-banners)

## WebDriver

- [macOS WebDriver Commands for Safari 11.1 and earlier](/documentation/webkit/macos-webdriver-commands-for-safari-11-1-and-earlier)
- [macOS WebDriver Commands for Safari 12 and later](/documentation/webkit/macos-webdriver-commands-for-safari-12-and-later)
- [About WebDriver for Safari](/documentation/webkit/about-webdriver-for-safari)
- [Testing with WebDriver in Safari](/documentation/webkit/testing-with-webdriver-in-safari)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
