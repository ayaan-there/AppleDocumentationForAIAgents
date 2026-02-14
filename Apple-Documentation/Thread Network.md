# Thread Network Documentation

Source: https://sosumi.ai/documentation/threadnetwork

---
title: ThreadNetwork
source: https://developer.apple.com/documentation/threadnetwork
timestamp: 2026-02-13T19:03:07.579Z
---

## Setting up Thread Border Routers

- [Getting started with ThreadNetwork](/documentation/threadnetwork/getting-started-with-threadnetwork)
- [Configuring a Border Router](/documentation/threadnetwork/configuring-a-border-router)
- [Managing Thread network credentials](/documentation/threadnetwork/managing-thread-network-credentials)

## Managing clients and sharing credentials

- [com.apple.developer.networking.manage-thread-network-credentials](/documentation/bundleresources/entitlements/com.apple.developer.networking.manage-thread-network-credentials)
- [THClient](/documentation/threadnetwork/thclient)

### Creating the Client

- [init()](/documentation/threadnetwork/thclient/init())

### Retrieving Credentials

- [func isPreferredNetworkAvailable(completion: (Bool) -> Void)](/documentation/threadnetwork/thclient/ispreferrednetworkavailable(completion:))
- [func checkPreferredNetwork(forActiveOperationalDataset: Data, completion: (Bool) -> Void)](/documentation/threadnetwork/thclient/checkpreferrednetwork(foractiveoperationaldataset:completion:))
- [func retrieveCredentials(forBorderAgent: Data, completion: (THCredentials?, (any Error)?) -> Void)](/documentation/threadnetwork/thclient/retrievecredentials(forborderagent:completion:))
- [func retrieveCredentials(forExtendedPANID: Data, completion: (THCredentials?, (any Error)?) -> Void)](/documentation/threadnetwork/thclient/retrievecredentials(forextendedpanid:completion:))
- [func retrieveAllCredentials((Set<THCredentials>?, (any Error)?) -> Void)](/documentation/threadnetwork/thclient/retrieveallcredentials(_:))
- [func retrievePreferredCredentials((THCredentials?, (any Error)?) -> Void)](/documentation/threadnetwork/thclient/retrievepreferredcredentials(_:))
- [func retrieveAllActiveCredentials((Set<THCredentials>?, (any Error)?) -> Void)](/documentation/threadnetwork/thclient/retrieveallactivecredentials(_:))

### Storing and Deleting Credentials

- [func deleteCredentials(forBorderAgent: Data, completion: ((any Error)?) -> Void)](/documentation/threadnetwork/thclient/deletecredentials(forborderagent:completion:))
- [func storeCredentials(forBorderAgent: Data, activeOperationalDataSet: Data, completion: ((any Error)?) -> Void)](/documentation/threadnetwork/thclient/storecredentials(forborderagent:activeoperationaldataset:completion:))
- [THCredentials](/documentation/threadnetwork/thcredentials)

### Getting the Thread Parameters

- [var activeOperationalDataSet: Data?](/documentation/threadnetwork/thcredentials/activeoperationaldataset)
- [var borderAgentID: Data?](/documentation/threadnetwork/thcredentials/borderagentid)
- [var channel: UInt8](/documentation/threadnetwork/thcredentials/channel)
- [var extendedPANID: Data?](/documentation/threadnetwork/thcredentials/extendedpanid)
- [var networkKey: Data?](/documentation/threadnetwork/thcredentials/networkkey)
- [var networkName: String?](/documentation/threadnetwork/thcredentials/networkname)
- [var panID: Data?](/documentation/threadnetwork/thcredentials/panid)
- [var pskc: Data?](/documentation/threadnetwork/thcredentials/pskc)

### Getting the Framework Parameters

- [var creationDate: Date?](/documentation/threadnetwork/thcredentials/creationdate)
- [var lastModificationDate: Date?](/documentation/threadnetwork/thcredentials/lastmodificationdate)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
