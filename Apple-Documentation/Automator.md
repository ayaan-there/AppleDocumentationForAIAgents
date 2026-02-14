# Automator Documentation

Source: https://sosumi.ai/documentation/automator

---
title: Automator
source: https://developer.apple.com/documentation/automator
timestamp: 2026-02-13T18:54:13.956Z
---

## Actions

- [AMBundleAction](/documentation/automator/ambundleaction)

### Initializing the Action

- [func awakeFromBundle()](/documentation/automator/ambundleaction/awakefrombundle())

### Managing Action Properties

- [var bundle: Bundle](/documentation/automator/ambundleaction/bundle)
- [var hasView: Bool](/documentation/automator/ambundleaction/hasview)
- [var view: NSView?](/documentation/automator/ambundleaction/view)
- [var parameters: NSMutableDictionary?](/documentation/automator/ambundleaction/parameters)
- [AMShellScriptAction](/documentation/automator/amshellscriptaction)

### Handling the I/O Separator Character

- [var inputFieldSeparator: String](/documentation/automator/amshellscriptaction/inputfieldseparator)
- [var outputFieldSeparator: String](/documentation/automator/amshellscriptaction/outputfieldseparator)
- [var remapLineEndings: Bool](/documentation/automator/amshellscriptaction/remaplineendings)
- [AMAction](/documentation/automator/amaction)

### Initializing and Encoding

- [init?(definition: [String : Any]?, fromArchive: Bool)](/documentation/automator/amaction/init(definition:fromarchive:))
- [init(contentsOf: URL) throws](/documentation/automator/amaction/init(contentsof:))
- [func write(to: NSMutableDictionary)](/documentation/automator/amaction/write(to:))

### Controlling the Action

- [func run(withInput: Any?) throws -> Any](/documentation/automator/amaction/run(withinput:))
- [func runAsynchronously(withInput: Any?)](/documentation/automator/amaction/runasynchronously(withinput:))
- [func finishRunningWithError((any Error)?)](/documentation/automator/amaction/finishrunningwitherror(_:))
- [func willFinishRunning()](/documentation/automator/amaction/willfinishrunning())
- [func stop()](/documentation/automator/amaction/stop())
- [func reset()](/documentation/automator/amaction/reset())

### Initializing and Synchronizing the Action User Interface

- [func activated()](/documentation/automator/amaction/activated())
- [func opened()](/documentation/automator/amaction/opened())

### Performing Logging

- [AMLogLevel](/documentation/automator/amloglevel)

#### Constants

- [case debug](/documentation/automator/amloglevel/debug)
- [case info](/documentation/automator/amloglevel/info)
- [case warn](/documentation/automator/amloglevel/warn)
- [case error](/documentation/automator/amloglevel/error)

#### Initializers

- [init?(rawValue: UInt)](/documentation/automator/amloglevel/init(rawvalue:))

### Updating Action Parameters

- [func parametersUpdated()](/documentation/automator/amaction/parametersupdated())
- [func updateParameters()](/documentation/automator/amaction/updateparameters())

### Getting Action Information

- [var name: String](/documentation/automator/amaction/name)
- [var progressValue: CGFloat](/documentation/automator/amaction/progressvalue)
- [var ignoresInput: Bool](/documentation/automator/amaction/ignoresinput)
- [var output: Any?](/documentation/automator/amaction/output)
- [var selectedInputType: String?](/documentation/automator/amaction/selectedinputtype)
- [var selectedOutputType: String?](/documentation/automator/amaction/selectedoutputtype)
- [var isStopped: Bool](/documentation/automator/amaction/isstopped)

### Performing Cleanup Operations

- [func closed()](/documentation/automator/amaction/closed())

## Workflows

- [AMWorkflow](/documentation/automator/amworkflow)

### Creating a Workflow

- [init()](/documentation/automator/amworkflow/init())
- [convenience init(contentsOf: URL) throws](/documentation/automator/amworkflow/init(contentsof:))

### Running a Workflow

- [class func run(at: URL, withInput: Any?) throws -> Any](/documentation/automator/amworkflow/run(at:withinput:))

### Saving Changes to a Workflow

- [func write(to: URL) throws](/documentation/automator/amworkflow/write(to:))

### Getting Information About a Workflow

- [var actions: [AMAction]](/documentation/automator/amworkflow/actions)
- [var fileURL: URL?](/documentation/automator/amworkflow/fileurl)
- [func valueForVariable(withName: String) -> Any?](/documentation/automator/amworkflow/valueforvariable(withname:))

### Working with the Workflow’s Input and Output

- [var input: Any?](/documentation/automator/amworkflow/input)
- [var output: Any?](/documentation/automator/amworkflow/output)

### Manipulating the Workflow

- [func setValue(Any?, forVariableWithName: String) -> Bool](/documentation/automator/amworkflow/setvalue(_:forvariablewithname:))

### Manipulating the Workflow’s Actions

- [func addAction(AMAction)](/documentation/automator/amworkflow/addaction(_:))
- [func insertAction(AMAction, at: Int)](/documentation/automator/amworkflow/insertaction(_:at:))
- [func moveAction(at: Int, to: Int)](/documentation/automator/amworkflow/moveaction(at:to:))
- [func removeAction(AMAction)](/documentation/automator/amworkflow/removeaction(_:))
- [AMWorkflowController](/documentation/automator/amworkflowcontroller)

### Accessing the Workflow

- [var workflow: AMWorkflow?](/documentation/automator/amworkflowcontroller/workflow)

### Accessing the Workflow View

- [var workflowView: AMWorkflowView?](/documentation/automator/amworkflowcontroller/workflowview-swift.property)

### Accessing the Delegate

- [var delegate: (any AMWorkflowControllerDelegate)?](/documentation/automator/amworkflowcontroller/delegate)
- [AMWorkflowControllerDelegate](/documentation/automator/amworkflowcontrollerdelegate)

#### Preparing to Run

- [func workflowController(AMWorkflowController, willRun: AMAction)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:willrun:))
- [func workflowControllerWillRun(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerwillrun(_:))

#### Running

- [func workflowController(AMWorkflowController, didRun: AMAction)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:didrun:))
- [func workflowControllerDidRun(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerdidrun(_:))

#### Stopping

- [func workflowControllerWillStop(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerwillstop(_:))
- [func workflowControllerDidStop(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerdidstop(_:))

#### Handling Errors

- [func workflowController(AMWorkflowController, didError: any Error)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:diderror:))

#### Deprecated

- [func workflowController(AMWorkflowController, willRun: AMAction)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:willrun:))
- [func workflowControllerWillRun(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerwillrun(_:))
- [func workflowController(AMWorkflowController, didRun: AMAction)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:didrun:))
- [func workflowControllerDidRun(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerdidrun(_:))
- [func workflowControllerWillStop(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerwillstop(_:))
- [func workflowControllerDidStop(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerdidstop(_:))
- [func workflowController(AMWorkflowController, didError: any Error)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:diderror:))

### Controlling the Workflow

- [func pause(Any)](/documentation/automator/amworkflowcontroller/pause(_:))
- [func reset(Any)](/documentation/automator/amworkflowcontroller/reset(_:))
- [func run(Any)](/documentation/automator/amworkflowcontroller/run(_:))
- [func step(Any)](/documentation/automator/amworkflowcontroller/step(_:))
- [func stop(Any)](/documentation/automator/amworkflowcontroller/stop(_:))

### Getting Workflow Information

- [var canRun: Bool](/documentation/automator/amworkflowcontroller/canrun)
- [var isPaused: Bool](/documentation/automator/amworkflowcontroller/ispaused)
- [var isRunning: Bool](/documentation/automator/amworkflowcontroller/isrunning)
- [AMWorkflowView](/documentation/automator/amworkflowview)

### Configuring the Workflow View

- [var isEditable: Bool](/documentation/automator/amworkflowview/iseditable)
- [var workflowController: AMWorkflowController?](/documentation/automator/amworkflowview/workflowcontroller)
- [AMWorkspace](/documentation/automator/amworkspace)

### Accessing the Shared Workspace

- [class var shared: AMWorkspace!](/documentation/automator/amworkspace/shared)

### Running Workflows

- [func runWorkflow(atPath: String!, withInput: Any!) throws -> Any](/documentation/automator/amworkspace/runworkflow(atpath:withinput:))

## Errors

- [var AMAutomatorErrorDomain: String](/documentation/automator/amautomatorerrordomain)
- [var AMActionErrorKey: String](/documentation/automator/amactionerrorkey)
- [AMError](/documentation/automator/amerror)

### Error Codes

- [static var workflowActionsNotLoadedError: AMError.Code](/documentation/automator/amerror/workflowactionsnotloadederror)
- [static var workflowNewerActionVersionError: AMError.Code](/documentation/automator/amerror/workflowneweractionversionerror)
- [static var workflowNewerVersionError: AMError.Code](/documentation/automator/amerror/workflownewerversionerror)
- [static var workflowNoEnabledActionsError: AMError.Code](/documentation/automator/amerror/workflownoenabledactionserror)
- [static var workflowOlderActionVersionError: AMError.Code](/documentation/automator/amerror/workflowolderactionversionerror)
- [static var workflowPropertyListInvalidError: AMError.Code](/documentation/automator/amerror/workflowpropertylistinvaliderror)
- [static var userCanceledError: AMError.Code](/documentation/automator/amerror/usercancelederror)
- [static var actionApplicationResourceError: AMError.Code](/documentation/automator/amerror/actionapplicationresourceerror)
- [static var actionApplicationVersionResourceError: AMError.Code](/documentation/automator/amerror/actionapplicationversionresourceerror)
- [static var actionArchitectureMismatchError: AMError.Code](/documentation/automator/amerror/actionarchitecturemismatcherror)
- [static var actionExceptionError: AMError.Code](/documentation/automator/amerror/actionexceptionerror)
- [static var actionExecutionError: AMError.Code](/documentation/automator/amerror/actionexecutionerror)
- [static var actionFailedGatekeeperError: AMError.Code](/documentation/automator/amerror/actionfailedgatekeepererror)
- [static var actionFileResourceError: AMError.Code](/documentation/automator/amerror/actionfileresourceerror)
- [static var actionInitializationError: AMError.Code](/documentation/automator/amerror/actioninitializationerror)
- [static var actionInsufficientDataError: AMError.Code](/documentation/automator/amerror/actioninsufficientdataerror)
- [static var actionIsDeprecatedError: AMError.Code](/documentation/automator/amerror/actionisdeprecatederror)
- [static var actionLicenseResourceError: AMError.Code](/documentation/automator/amerror/actionlicenseresourceerror)
- [static var actionLinkError: AMError.Code](/documentation/automator/amerror/actionlinkerror)
- [static var actionLoadError: AMError.Code](/documentation/automator/amerror/actionloaderror)
- [static var actionMalwareError: AMError.Code](/documentation/automator/amerror/actionmalwareerror)
- [static var actionNotLoadableError: AMError.Code](/documentation/automator/amerror/actionnotloadableerror)
- [static var actionPropertyListInvalidError: AMError.Code](/documentation/automator/amerror/actionpropertylistinvaliderror)
- [static var actionQuarantineError: AMError.Code](/documentation/automator/amerror/actionquarantineerror)
- [static var actionRequiredActionResourceError: AMError.Code](/documentation/automator/amerror/actionrequiredactionresourceerror)
- [static var actionRuntimeMismatchError: AMError.Code](/documentation/automator/amerror/actionruntimemismatcherror)
- [static var actionSignatureCorruptError: AMError.Code](/documentation/automator/amerror/actionsignaturecorrupterror)
- [static var actionThirdPartyActionsNotAllowedError: AMError.Code](/documentation/automator/amerror/actionthirdpartyactionsnotallowederror)
- [static var actionXPCError: AMError.Code](/documentation/automator/amerror/actionxpcerror)
- [static var actionXProtectError: AMError.Code](/documentation/automator/amerror/actionxprotecterror)
- [static var noSuchActionError: AMError.Code](/documentation/automator/amerror/nosuchactionerror)
- [static var conversionFailedError: AMError.Code](/documentation/automator/amerror/conversionfailederror)
- [static var conversionNoDataError: AMError.Code](/documentation/automator/amerror/conversionnodataerror)
- [static var conversionNotPossibleError: AMError.Code](/documentation/automator/amerror/conversionnotpossibleerror)
- [AMError.Code](/documentation/automator/amerror/code)

#### Workflow Errors

- [case workflowActionsNotLoadedError](/documentation/automator/amerror/code/workflowactionsnotloadederror)
- [case workflowNewerActionVersionError](/documentation/automator/amerror/code/workflowneweractionversionerror)
- [case workflowNewerVersionError](/documentation/automator/amerror/code/workflownewerversionerror)
- [case workflowNoEnabledActionsError](/documentation/automator/amerror/code/workflownoenabledactionserror)
- [case workflowOlderActionVersionError](/documentation/automator/amerror/code/workflowolderactionversionerror)
- [case workflowPropertyListInvalidError](/documentation/automator/amerror/code/workflowpropertylistinvaliderror)

#### Workflow Runtime Errors

- [case userCanceledError](/documentation/automator/amerror/code/usercancelederror)

#### Action Errors

- [case actionApplicationResourceError](/documentation/automator/amerror/code/actionapplicationresourceerror)
- [case actionApplicationVersionResourceError](/documentation/automator/amerror/code/actionapplicationversionresourceerror)
- [case actionArchitectureMismatchError](/documentation/automator/amerror/code/actionarchitecturemismatcherror)
- [case actionExceptionError](/documentation/automator/amerror/code/actionexceptionerror)
- [case actionExecutionError](/documentation/automator/amerror/code/actionexecutionerror)
- [case actionFailedGatekeeperError](/documentation/automator/amerror/code/actionfailedgatekeepererror)
- [case actionFileResourceError](/documentation/automator/amerror/code/actionfileresourceerror)
- [case actionInitializationError](/documentation/automator/amerror/code/actioninitializationerror)
- [case actionInsufficientDataError](/documentation/automator/amerror/code/actioninsufficientdataerror)
- [case actionIsDeprecatedError](/documentation/automator/amerror/code/actionisdeprecatederror)
- [case actionLicenseResourceError](/documentation/automator/amerror/code/actionlicenseresourceerror)
- [case actionLinkError](/documentation/automator/amerror/code/actionlinkerror)
- [case actionLoadError](/documentation/automator/amerror/code/actionloaderror)
- [case actionMalwareError](/documentation/automator/amerror/code/actionmalwareerror)
- [case actionNotLoadableError](/documentation/automator/amerror/code/actionnotloadableerror)
- [case actionPropertyListInvalidError](/documentation/automator/amerror/code/actionpropertylistinvaliderror)
- [case actionQuarantineError](/documentation/automator/amerror/code/actionquarantineerror)
- [case actionRequiredActionResourceError](/documentation/automator/amerror/code/actionrequiredactionresourceerror)
- [case actionRuntimeMismatchError](/documentation/automator/amerror/code/actionruntimemismatcherror)
- [case actionSignatureCorruptError](/documentation/automator/amerror/code/actionsignaturecorrupterror)
- [case actionThirdPartyActionsNotAllowedError](/documentation/automator/amerror/code/actionthirdpartyactionsnotallowederror)
- [case actionXPCError](/documentation/automator/amerror/code/actionxpcerror)
- [case actionXProtectError](/documentation/automator/amerror/code/actionxprotecterror)
- [case noSuchActionError](/documentation/automator/amerror/code/nosuchactionerror)

#### Data Conversion Errors

- [case conversionFailedError](/documentation/automator/amerror/code/conversionfailederror)
- [case conversionNoDataError](/documentation/automator/amerror/code/conversionnodataerror)
- [case conversionNotPossibleError](/documentation/automator/amerror/code/conversionnotpossibleerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/automator/amerror/code/init(rawvalue:))

### Error Domain

- [var AMAutomatorErrorDomain: String](/documentation/automator/amautomatorerrordomain)
- [AMError.Code](/documentation/automator/amerror/code)

### Workflow Errors

- [case workflowActionsNotLoadedError](/documentation/automator/amerror/code/workflowactionsnotloadederror)
- [case workflowNewerActionVersionError](/documentation/automator/amerror/code/workflowneweractionversionerror)
- [case workflowNewerVersionError](/documentation/automator/amerror/code/workflownewerversionerror)
- [case workflowNoEnabledActionsError](/documentation/automator/amerror/code/workflownoenabledactionserror)
- [case workflowOlderActionVersionError](/documentation/automator/amerror/code/workflowolderactionversionerror)
- [case workflowPropertyListInvalidError](/documentation/automator/amerror/code/workflowpropertylistinvaliderror)

### Workflow Runtime Errors

- [case userCanceledError](/documentation/automator/amerror/code/usercancelederror)

### Action Errors

- [case actionApplicationResourceError](/documentation/automator/amerror/code/actionapplicationresourceerror)
- [case actionApplicationVersionResourceError](/documentation/automator/amerror/code/actionapplicationversionresourceerror)
- [case actionArchitectureMismatchError](/documentation/automator/amerror/code/actionarchitecturemismatcherror)
- [case actionExceptionError](/documentation/automator/amerror/code/actionexceptionerror)
- [case actionExecutionError](/documentation/automator/amerror/code/actionexecutionerror)
- [case actionFailedGatekeeperError](/documentation/automator/amerror/code/actionfailedgatekeepererror)
- [case actionFileResourceError](/documentation/automator/amerror/code/actionfileresourceerror)
- [case actionInitializationError](/documentation/automator/amerror/code/actioninitializationerror)
- [case actionInsufficientDataError](/documentation/automator/amerror/code/actioninsufficientdataerror)
- [case actionIsDeprecatedError](/documentation/automator/amerror/code/actionisdeprecatederror)
- [case actionLicenseResourceError](/documentation/automator/amerror/code/actionlicenseresourceerror)
- [case actionLinkError](/documentation/automator/amerror/code/actionlinkerror)
- [case actionLoadError](/documentation/automator/amerror/code/actionloaderror)
- [case actionMalwareError](/documentation/automator/amerror/code/actionmalwareerror)
- [case actionNotLoadableError](/documentation/automator/amerror/code/actionnotloadableerror)
- [case actionPropertyListInvalidError](/documentation/automator/amerror/code/actionpropertylistinvaliderror)
- [case actionQuarantineError](/documentation/automator/amerror/code/actionquarantineerror)
- [case actionRequiredActionResourceError](/documentation/automator/amerror/code/actionrequiredactionresourceerror)
- [case actionRuntimeMismatchError](/documentation/automator/amerror/code/actionruntimemismatcherror)
- [case actionSignatureCorruptError](/documentation/automator/amerror/code/actionsignaturecorrupterror)
- [case actionThirdPartyActionsNotAllowedError](/documentation/automator/amerror/code/actionthirdpartyactionsnotallowederror)
- [case actionXPCError](/documentation/automator/amerror/code/actionxpcerror)
- [case actionXProtectError](/documentation/automator/amerror/code/actionxprotecterror)
- [case noSuchActionError](/documentation/automator/amerror/code/nosuchactionerror)

### Data Conversion Errors

- [case conversionFailedError](/documentation/automator/amerror/code/conversionfailederror)
- [case conversionNoDataError](/documentation/automator/amerror/code/conversionnodataerror)
- [case conversionNotPossibleError](/documentation/automator/amerror/code/conversionnotpossibleerror)

### Initializers

- [init?(rawValue: Int)](/documentation/automator/amerror/code/init(rawvalue:))

## Deprecated

- [AMAppleScriptAction](/documentation/automator/amapplescriptaction)

### Accessing the script

- [var script: OSAScript?](/documentation/automator/amapplescriptaction/script)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
