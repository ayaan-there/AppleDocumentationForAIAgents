# SecureElementCredential Documentation

Source: https://sosumi.ai/documentation/secureelementcredential

---
title: SecureElementCredential
source: https://developer.apple.com/documentation/secureelementcredential
timestamp: 2026-02-13T19:01:49.331Z
---

## Essentials

- [Accessing and using secure element credentials](/documentation/secureelementcredential/accessing-and-using-secure-element-credentials)

## Entitlements

- [com.apple.developer.secure-element-credential](/documentation/bundleresources/entitlements/com.apple.developer.secure-element-credential)
- [com.apple.developer.secure-element-credential.default-contactless-app](/documentation/bundleresources/entitlements/com.apple.developer.secure-element-credential.default-contactless-app)

## Credentials

- [CredentialSession](/documentation/secureelementcredential/credentialsession)

### Verifying eligibility

- [static var isEligible: Bool](/documentation/secureelementcredential/credentialsession/iseligible)

### Accessing hardware information

- [var secureElementInfo: CredentialSession.SecureElementInfo](/documentation/secureelementcredential/credentialsession/secureelementinfo-swift.property)
- [CredentialSession.SecureElementInfo](/documentation/secureelementcredential/credentialsession/secureelementinfo-swift.struct)

#### Getting hardware information

- [let hardwareReleaseVersionInfo: String](/documentation/secureelementcredential/credentialsession/secureelementinfo-swift.struct/hardwarereleaseversioninfo)
- [let secureElementPlatformSigningCertificate: Data](/documentation/secureelementcredential/credentialsession/secureelementinfo-swift.struct/secureelementplatformsigningcertificate)

### Managing the credential session life cycle

- [static func startSession() async throws -> CredentialSession](/documentation/secureelementcredential/credentialsession/startsession())
- [func invalidate() async throws](/documentation/secureelementcredential/credentialsession/invalidate())

### Accessing the session state

- [var state: CredentialSession.State](/documentation/secureelementcredential/credentialsession/state-swift.property)
- [CredentialSession.State](/documentation/secureelementcredential/credentialsession/state-swift.enum)

#### Card session states

- [case management](/documentation/secureelementcredential/credentialsession/state-swift.enum/management)
- [case wired(credential: CredentialSession.Credential)](/documentation/secureelementcredential/credentialsession/state-swift.enum/wired(credential:))
- [case cardEmulation(credential: CredentialSession.Credential)](/documentation/secureelementcredential/credentialsession/state-swift.enum/cardemulation(credential:))
- [CredentialSession.Credential](/documentation/secureelementcredential/credentialsession/credential)

##### Identifying a credential

- [let identifier: UUID](/documentation/secureelementcredential/credentialsession/credential/identifier)

##### Getting a display name

- [let name: String](/documentation/secureelementcredential/credentialsession/credential/name)

##### Inspecting credential state

- [let state: CredentialSession.Credential.State](/documentation/secureelementcredential/credentialsession/credential/state-swift.property)
- [CredentialSession.Credential.State](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum)

###### Credential states

- [case installationPending](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installationpending)
- [case installed(instances: [CredentialSession.Credential.InstanceInfo])](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installed(instances:))
- [CredentialSession.Credential.InstanceInfo](/documentation/secureelementcredential/credentialsession/credential/instanceinfo)

###### Inspecting instance identifiers

- [let instanceAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instanceaid)
- [let packageAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/packageaid)
- [let moduleAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/moduleaid)

###### Inspecting the instance type

- [let instanceType: CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.property)
- [CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum)

###### Instance types

- [case standalone](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/standalone)
- [case headApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/headapplication)
- [case groupApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/groupapplication)

###### Creating a secure channel

- [let securityDomainAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainaid)
- [let securityDomainKeyInfo: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainkeyinfo)

###### Inspecting applet instance state

- [let lifeCycleState: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/lifecyclestate)

###### Instance Properties

- [var securityDomainCounter: Int](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomaincounter)
- [case installationFailed](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installationfailed)

##### Hashing

- [func hash(into: inout Hasher)](/documentation/secureelementcredential/credentialsession/credential/hash(into:))

##### Supporting types

- [CredentialSession.Credential.InstanceInfo](/documentation/secureelementcredential/credentialsession/credential/instanceinfo)

###### Inspecting instance identifiers

- [let instanceAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instanceaid)
- [let packageAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/packageaid)
- [let moduleAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/moduleaid)

###### Inspecting the instance type

- [let instanceType: CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.property)
- [CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum)

###### Instance types

- [case standalone](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/standalone)
- [case headApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/headapplication)
- [case groupApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/groupapplication)

###### Creating a secure channel

- [let securityDomainAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainaid)
- [let securityDomainKeyInfo: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainkeyinfo)

###### Inspecting applet instance state

- [let lifeCycleState: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/lifecyclestate)

###### Instance Properties

- [var securityDomainCounter: Int](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomaincounter)
- [case invalid](/documentation/secureelementcredential/credentialsession/state-swift.enum/invalid)

### Accessing credentials

- [func listCredentials() async throws -> [CredentialSession.Credential]](/documentation/secureelementcredential/credentialsession/listcredentials())
- [CredentialSession.Credential](/documentation/secureelementcredential/credentialsession/credential)

#### Identifying a credential

- [let identifier: UUID](/documentation/secureelementcredential/credentialsession/credential/identifier)

#### Getting a display name

- [let name: String](/documentation/secureelementcredential/credentialsession/credential/name)

#### Inspecting credential state

- [let state: CredentialSession.Credential.State](/documentation/secureelementcredential/credentialsession/credential/state-swift.property)
- [CredentialSession.Credential.State](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum)

##### Credential states

- [case installationPending](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installationpending)
- [case installed(instances: [CredentialSession.Credential.InstanceInfo])](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installed(instances:))
- [CredentialSession.Credential.InstanceInfo](/documentation/secureelementcredential/credentialsession/credential/instanceinfo)

###### Inspecting instance identifiers

- [let instanceAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instanceaid)
- [let packageAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/packageaid)
- [let moduleAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/moduleaid)

###### Inspecting the instance type

- [let instanceType: CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.property)
- [CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum)

###### Instance types

- [case standalone](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/standalone)
- [case headApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/headapplication)
- [case groupApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/groupapplication)

###### Creating a secure channel

- [let securityDomainAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainaid)
- [let securityDomainKeyInfo: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainkeyinfo)

###### Inspecting applet instance state

- [let lifeCycleState: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/lifecyclestate)

###### Instance Properties

- [var securityDomainCounter: Int](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomaincounter)
- [case installationFailed](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installationfailed)

#### Hashing

- [func hash(into: inout Hasher)](/documentation/secureelementcredential/credentialsession/credential/hash(into:))

#### Supporting types

- [CredentialSession.Credential.InstanceInfo](/documentation/secureelementcredential/credentialsession/credential/instanceinfo)

##### Inspecting instance identifiers

- [let instanceAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instanceaid)
- [let packageAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/packageaid)
- [let moduleAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/moduleaid)

##### Inspecting the instance type

- [let instanceType: CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.property)
- [CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum)

###### Instance types

- [case standalone](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/standalone)
- [case headApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/headapplication)
- [case groupApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/groupapplication)

##### Creating a secure channel

- [let securityDomainAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainaid)
- [let securityDomainKeyInfo: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainkeyinfo)

##### Inspecting applet instance state

- [let lifeCycleState: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/lifecyclestate)

##### Instance Properties

- [var securityDomainCounter: Int](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomaincounter)

### Acquiring exclusive foreground privileges

- [func acquirePresentmentAssertion() async throws -> CredentialSession.PresentmentIntentAssertion](/documentation/secureelementcredential/credentialsession/acquirepresentmentassertion())
- [CredentialSession.PresentmentIntentAssertion](/documentation/secureelementcredential/credentialsession/presentmentintentassertion)

#### Inspecting assertion state

- [var state: CredentialSession.PresentmentIntentAssertion.State](/documentation/secureelementcredential/credentialsession/presentmentintentassertion/state-swift.property)
- [CredentialSession.PresentmentIntentAssertion.State](/documentation/secureelementcredential/credentialsession/presentmentintentassertion/state-swift.enum)

##### Assertion states

- [case active](/documentation/secureelementcredential/credentialsession/presentmentintentassertion/state-swift.enum/active)
- [case invalid](/documentation/secureelementcredential/credentialsession/presentmentintentassertion/state-swift.enum/invalid)

#### Relinquishing presentment intent

- [func relinquish() async throws](/documentation/secureelementcredential/credentialsession/presentmentintentassertion/relinquish())

### Handling session events

- [var eventStream: AsyncStream<CredentialSession.Event>](/documentation/secureelementcredential/credentialsession/eventstream)
- [CredentialSession.Event](/documentation/secureelementcredential/credentialsession/event)

#### Credential events

- [case credentialFinishedInstalling(credential: CredentialSession.Credential)](/documentation/secureelementcredential/credentialsession/event/credentialfinishedinstalling(credential:))
- [CredentialSession.Credential](/documentation/secureelementcredential/credentialsession/credential)

##### Identifying a credential

- [let identifier: UUID](/documentation/secureelementcredential/credentialsession/credential/identifier)

##### Getting a display name

- [let name: String](/documentation/secureelementcredential/credentialsession/credential/name)

##### Inspecting credential state

- [let state: CredentialSession.Credential.State](/documentation/secureelementcredential/credentialsession/credential/state-swift.property)
- [CredentialSession.Credential.State](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum)

###### Credential states

- [case installationPending](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installationpending)
- [case installed(instances: [CredentialSession.Credential.InstanceInfo])](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installed(instances:))
- [CredentialSession.Credential.InstanceInfo](/documentation/secureelementcredential/credentialsession/credential/instanceinfo)

###### Inspecting instance identifiers

- [let instanceAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instanceaid)
- [let packageAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/packageaid)
- [let moduleAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/moduleaid)

###### Inspecting the instance type

- [let instanceType: CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.property)
- [CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum)

###### Instance types

- [case standalone](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/standalone)
- [case headApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/headapplication)
- [case groupApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/groupapplication)

###### Creating a secure channel

- [let securityDomainAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainaid)
- [let securityDomainKeyInfo: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainkeyinfo)

###### Inspecting applet instance state

- [let lifeCycleState: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/lifecyclestate)

###### Instance Properties

- [var securityDomainCounter: Int](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomaincounter)
- [case installationFailed](/documentation/secureelementcredential/credentialsession/credential/state-swift.enum/installationfailed)

##### Hashing

- [func hash(into: inout Hasher)](/documentation/secureelementcredential/credentialsession/credential/hash(into:))

##### Supporting types

- [CredentialSession.Credential.InstanceInfo](/documentation/secureelementcredential/credentialsession/credential/instanceinfo)

###### Inspecting instance identifiers

- [let instanceAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instanceaid)
- [let packageAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/packageaid)
- [let moduleAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/moduleaid)

###### Inspecting the instance type

- [let instanceType: CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.property)
- [CredentialSession.Credential.InstanceInfo.InstanceType](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum)

###### Instance types

- [case standalone](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/standalone)
- [case headApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/headapplication)
- [case groupApplication](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/instancetype-swift.enum/groupapplication)

###### Creating a secure channel

- [let securityDomainAID: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainaid)
- [let securityDomainKeyInfo: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomainkeyinfo)

###### Inspecting applet instance state

- [let lifeCycleState: Data](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/lifecyclestate)

###### Instance Properties

- [var securityDomainCounter: Int](/documentation/secureelementcredential/credentialsession/credential/instanceinfo/securitydomaincounter)

#### Card emulation events

- [case connectivityEvent(CredentialSession.ConnectivityEvent)](/documentation/secureelementcredential/credentialsession/event/connectivityevent(_:))
- [CredentialSession.ConnectivityEvent](/documentation/secureelementcredential/credentialsession/connectivityevent)

##### Identifying the target instance

- [let instanceApplicationIdentifier: Data](/documentation/secureelementcredential/credentialsession/connectivityevent/instanceapplicationidentifier)

##### Inspecting event data

- [let data: Data](/documentation/secureelementcredential/credentialsession/connectivityevent/data)

#### NFC field events

- [case fieldStateChanged(info: CredentialSession.NFCFieldInformation)](/documentation/secureelementcredential/credentialsession/event/fieldstatechanged(info:))
- [CredentialSession.NFCFieldInformation](/documentation/secureelementcredential/credentialsession/nfcfieldinformation)

##### Field states

- [case fieldAbsent](/documentation/secureelementcredential/credentialsession/nfcfieldinformation/fieldabsent)
- [case fieldPresent](/documentation/secureelementcredential/credentialsession/nfcfieldinformation/fieldpresent)

#### Invalidation events

- [case sessionInvalidated(reason: CredentialSession.ErrorCode)](/documentation/secureelementcredential/credentialsession/event/sessioninvalidated(reason:))
- [CredentialSession.ErrorCode](/documentation/secureelementcredential/credentialsession/errorcode)

##### Authorization and permission error codes

- [case userNotAuthorized](/documentation/secureelementcredential/credentialsession/errorcode/usernotauthorized)
- [case accessDenied](/documentation/secureelementcredential/credentialsession/errorcode/accessdenied)
- [case clientNotInForeground](/documentation/secureelementcredential/credentialsession/errorcode/clientnotinforeground)
- [case userCanceledAuthorization](/documentation/secureelementcredential/credentialsession/errorcode/usercanceledauthorization)
- [case userAuthorizationTimedOut](/documentation/secureelementcredential/credentialsession/errorcode/userauthorizationtimedout)
- [case featureUnavailable](/documentation/secureelementcredential/credentialsession/errorcode/featureunavailable)
- [case ineligible](/documentation/secureelementcredential/credentialsession/errorcode/ineligible)
- [case conditionsNotSatisfied](/documentation/secureelementcredential/credentialsession/errorcode/conditionsnotsatisfied)

##### Credential error codes

- [case invalidCredentialState](/documentation/secureelementcredential/credentialsession/errorcode/invalidcredentialstate)
- [case credentialDoesNotExist](/documentation/secureelementcredential/credentialsession/errorcode/credentialdoesnotexist)
- [case instanceDoesNotExist](/documentation/secureelementcredential/credentialsession/errorcode/instancedoesnotexist)

##### Session error codes

- [case invalidSessionState](/documentation/secureelementcredential/credentialsession/errorcode/invalidsessionstate)
- [case sessionInvalidated](/documentation/secureelementcredential/credentialsession/errorcode/sessioninvalidated)

##### Command error codes

- [case commandNotSupported](/documentation/secureelementcredential/credentialsession/errorcode/commandnotsupported)

##### Network-related error codes

- [case network](/documentation/secureelementcredential/credentialsession/errorcode/network)

##### Presentment intent assertion error codes

- [case presentmentIntentAssertionTimeout](/documentation/secureelementcredential/credentialsession/errorcode/presentmentintentassertiontimeout)

##### UIKit error codes

- [case invalidView](/documentation/secureelementcredential/credentialsession/errorcode/invalidview)

##### Hardware error codes

- [case insufficientSpace](/documentation/secureelementcredential/credentialsession/errorcode/insufficientspace)

##### Temporary error codes

- [case resourceUnavailable](/documentation/secureelementcredential/credentialsession/errorcode/resourceunavailable)
- [case acquiredResourceRelinquished](/documentation/secureelementcredential/credentialsession/errorcode/acquiredresourcerelinquished)

##### Miscellaneous error codes

- [case invalidInput](/documentation/secureelementcredential/credentialsession/errorcode/invalidinput)
- [case internalError](/documentation/secureelementcredential/credentialsession/errorcode/internalerror)

#### Timeout events

- [case cardEmulationTimeout](/documentation/secureelementcredential/credentialsession/event/cardemulationtimeout)
- [case presentmentIntentAssertionTimeout](/documentation/secureelementcredential/credentialsession/event/presentmentintentassertiontimeout)

### Managing a credential

- [func provisionCredential(configurationUUID: UUID, name: String) async throws -> CredentialSession.Credential](/documentation/secureelementcredential/credentialsession/provisioncredential(configurationuuid:name:))
- [func deleteCredential(CredentialSession.Credential) async throws](/documentation/secureelementcredential/credentialsession/deletecredential(_:))

### Performing wired mode actions

- [func performWiredTransaction(using: CredentialSession.Credential, over: UIScene, instanceAID: Data) async throws](/documentation/secureelementcredential/credentialsession/performwiredtransaction(using:over:instanceaid:))
- [func enterWiredMode(using: CredentialSession.Credential) async throws](/documentation/secureelementcredential/credentialsession/enterwiredmode(using:))
- [func transceive(Data) async throws -> Data](/documentation/secureelementcredential/credentialsession/transceive(_:))
- [func endWiredMode() async throws](/documentation/secureelementcredential/credentialsession/endwiredmode())

### Performing card emulation

- [func performCardEmulationTransactionWithCurrentCredential(over: UIScene, options: CredentialSession.CardEmulationOptions) async throws](/documentation/secureelementcredential/credentialsession/performcardemulationtransactionwithcurrentcredential(over:options:))
- [func performTransaction(using: CredentialSession.Credential, over: UIScene, options: CredentialSession.CardEmulationOptions) async throws](/documentation/secureelementcredential/credentialsession/performtransaction(using:over:options:))
- [CredentialSession.CardEmulationOptions](/documentation/secureelementcredential/credentialsession/cardemulationoptions)

#### Creating an options instance

- [init()](/documentation/secureelementcredential/credentialsession/cardemulationoptions/init())
- [func endCardEmulation() async throws](/documentation/secureelementcredential/credentialsession/endcardemulation())

### Using SwiftUI

- [func configuration() async throws -> CredentialTransaction.Configuration](/documentation/secureelementcredential/credentialsession/configuration())
- [CredentialTransaction.Configuration](/documentation/secureelementcredential/credentialtransaction/configuration)

#### Invalidating a configuration

- [func invalidate() async throws](/documentation/secureelementcredential/credentialtransaction/configuration/invalidate())

### Handling errors

- [CredentialSession.ErrorCode](/documentation/secureelementcredential/credentialsession/errorcode)

#### Authorization and permission error codes

- [case userNotAuthorized](/documentation/secureelementcredential/credentialsession/errorcode/usernotauthorized)
- [case accessDenied](/documentation/secureelementcredential/credentialsession/errorcode/accessdenied)
- [case clientNotInForeground](/documentation/secureelementcredential/credentialsession/errorcode/clientnotinforeground)
- [case userCanceledAuthorization](/documentation/secureelementcredential/credentialsession/errorcode/usercanceledauthorization)
- [case userAuthorizationTimedOut](/documentation/secureelementcredential/credentialsession/errorcode/userauthorizationtimedout)
- [case featureUnavailable](/documentation/secureelementcredential/credentialsession/errorcode/featureunavailable)
- [case ineligible](/documentation/secureelementcredential/credentialsession/errorcode/ineligible)
- [case conditionsNotSatisfied](/documentation/secureelementcredential/credentialsession/errorcode/conditionsnotsatisfied)

#### Credential error codes

- [case invalidCredentialState](/documentation/secureelementcredential/credentialsession/errorcode/invalidcredentialstate)
- [case credentialDoesNotExist](/documentation/secureelementcredential/credentialsession/errorcode/credentialdoesnotexist)
- [case instanceDoesNotExist](/documentation/secureelementcredential/credentialsession/errorcode/instancedoesnotexist)

#### Session error codes

- [case invalidSessionState](/documentation/secureelementcredential/credentialsession/errorcode/invalidsessionstate)
- [case sessionInvalidated](/documentation/secureelementcredential/credentialsession/errorcode/sessioninvalidated)

#### Command error codes

- [case commandNotSupported](/documentation/secureelementcredential/credentialsession/errorcode/commandnotsupported)

#### Network-related error codes

- [case network](/documentation/secureelementcredential/credentialsession/errorcode/network)

#### Presentment intent assertion error codes

- [case presentmentIntentAssertionTimeout](/documentation/secureelementcredential/credentialsession/errorcode/presentmentintentassertiontimeout)

#### UIKit error codes

- [case invalidView](/documentation/secureelementcredential/credentialsession/errorcode/invalidview)

#### Hardware error codes

- [case insufficientSpace](/documentation/secureelementcredential/credentialsession/errorcode/insufficientspace)

#### Temporary error codes

- [case resourceUnavailable](/documentation/secureelementcredential/credentialsession/errorcode/resourceunavailable)
- [case acquiredResourceRelinquished](/documentation/secureelementcredential/credentialsession/errorcode/acquiredresourcerelinquished)

#### Miscellaneous error codes

- [case invalidInput](/documentation/secureelementcredential/credentialsession/errorcode/invalidinput)
- [case internalError](/documentation/secureelementcredential/credentialsession/errorcode/internalerror)

### Infrequently-used functionality

- [init()](/documentation/secureelementcredential/credentialsession/init())

### Structures

- [CredentialSession.ConnectivityEvent](/documentation/secureelementcredential/credentialsession/connectivityevent)

#### Identifying the target instance

- [let instanceApplicationIdentifier: Data](/documentation/secureelementcredential/credentialsession/connectivityevent/instanceapplicationidentifier)

#### Inspecting event data

- [let data: Data](/documentation/secureelementcredential/credentialsession/connectivityevent/data)

### Enumerations

- [CredentialSession.NFCFieldInformation](/documentation/secureelementcredential/credentialsession/nfcfieldinformation)

#### Field states

- [case fieldAbsent](/documentation/secureelementcredential/credentialsession/nfcfieldinformation/fieldabsent)
- [case fieldPresent](/documentation/secureelementcredential/credentialsession/nfcfieldinformation/fieldpresent)

## Transactions

- [CredentialTransaction](/documentation/secureelementcredential/credentialtransaction)

### Configuring transactions

- [CredentialTransaction.Configuration](/documentation/secureelementcredential/credentialtransaction/configuration)

#### Invalidating a configuration

- [func invalidate() async throws](/documentation/secureelementcredential/credentialtransaction/configuration/invalidate())

### Performing transactions

- [func performTransaction(using: Credential, options: CardEmulationOptions) async throws](/documentation/secureelementcredential/credentialtransaction/performtransaction(using:options:))
- [func performTransactionInWiredMode(using: Credential, instanceAID: Data) async throws](/documentation/secureelementcredential/credentialtransaction/performtransactioninwiredmode(using:instanceaid:))
- [func performCardEmulationTransactionWithCurrentCredential(options: CardEmulationOptions) async throws](/documentation/secureelementcredential/credentialtransaction/performcardemulationtransactionwithcurrentcredential(options:))

### Supporting types

- [Credential](/documentation/secureelementcredential/credential)
- [CardEmulationOptions](/documentation/secureelementcredential/cardemulationoptions)

## UIKit scene delegate

- [CredentialSessionWindowSceneDelegate](/documentation/secureelementcredential/credentialsessionwindowscenedelegate)

### Handling events

- [func windowScene(UIWindowScene, didReceiveCredentialSessionWindowSceneEvent: CredentialSessionWindowSceneEvent)](/documentation/secureelementcredential/credentialsessionwindowscenedelegate/windowscene(_:didreceivecredentialsessionwindowsceneevent:))
- [CredentialSessionWindowSceneEvent](/documentation/secureelementcredential/credentialsessionwindowsceneevent)

#### Events

- [case presentation](/documentation/secureelementcredential/credentialsessionwindowsceneevent/presentation)
- [case readerDetected](/documentation/secureelementcredential/credentialsessionwindowsceneevent/readerdetected)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
