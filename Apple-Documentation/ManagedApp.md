# ManagedApp Documentation

Source: https://sosumi.ai/documentation/managedapp

---
title: ManagedApp
source: https://developer.apple.com/documentation/managedapp
timestamp: 2026-02-13T18:59:07.420Z
---

## Configuration

- [Specifying and decoding a configuration](/documentation/managedapp/specifying-and-decoding-a-configuration)
- [ManagedAppConfigurationProvider](/documentation/managedapp/managedappconfigurationprovider)

### Initializing a configuration provider

- [init()](/documentation/managedapp/managedappconfigurationprovider/init())

### Accessing configurations

- [func configurations<Configuration>(Configuration.Type) async -> some AsyncSequence<Optional<Configuration>, Never>
](/documentation/managedapp/managedappconfigurationprovider/configurations(_:))

## Secrets and identifiers

- [Accessing provisioned secrets with identifiers](/documentation/managedapp/accessing-provisioned-secrets-with-identifiers)
- [ManagedAppCertificatesProvider](/documentation/managedapp/managedappcertificatesprovider)

### Initializing a certificates provider

- [init()](/documentation/managedapp/managedappcertificatesprovider/init())

### Identifying cerificates

- [var identifiers: some AsyncSequence<Array<String>, Never>](/documentation/managedapp/managedappcertificatesprovider/identifiers)

### Accessing certificates

- [func certificate(withIdentifier: String) async throws(ManagedAppError) -> SecCertificate](/documentation/managedapp/managedappcertificatesprovider/certificate(withidentifier:))
- [ManagedAppIdentitiesProvider](/documentation/managedapp/managedappidentitiesprovider)

### Initializing an identities provider

- [init()](/documentation/managedapp/managedappidentitiesprovider/init())

### Identifying identities

- [var identifiers: some AsyncSequence<Array<String>, Never>](/documentation/managedapp/managedappidentitiesprovider/identifiers)

### Accessing identities

- [func identity(withIdentifier: String) async throws(ManagedAppError) -> SecIdentity](/documentation/managedapp/managedappidentitiesprovider/identity(withidentifier:))
- [ManagedAppPasswordsProvider](/documentation/managedapp/managedapppasswordsprovider)

### Initializing a passwords provider

- [init()](/documentation/managedapp/managedapppasswordsprovider/init())

### Identifying passwords

- [var identifiers: some AsyncSequence<Array<String>, Never>](/documentation/managedapp/managedapppasswordsprovider/identifiers)

### Accessing passwords

- [func password(withIdentifier: String) async throws(ManagedAppError) -> String](/documentation/managedapp/managedapppasswordsprovider/password(withidentifier:))

## Errors

- [ManagedAppError](/documentation/managedapp/managedapperror)

### Interpreting an error

- [case invalidIdentifier](/documentation/managedapp/managedapperror/invalididentifier)

### Enumeration Cases

- [case internalError](/documentation/managedapp/managedapperror/internalerror)
- [case serverError](/documentation/managedapp/managedapperror/servererror)
- [ManagedAppConfigurationDecodingError](/documentation/managedapp/managedappconfigurationdecodingerror)

### Identifying an error

- [var code: ManagedAppConfigurationDecodingErrorCode](/documentation/managedapp/managedappconfigurationdecodingerror/code)

### Interpreting an error

- [var message: String](/documentation/managedapp/managedappconfigurationdecodingerror/message)
- [ManagedAppConfigurationDecodingErrorCode](/documentation/managedapp/managedappconfigurationdecodingerrorcode)

### Initializing an error

- [init?(rawValue: Int)](/documentation/managedapp/managedappconfigurationdecodingerrorcode/init(rawvalue:))

### Identifying an error

- [let rawValue: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/rawvalue)

### Type Properties

- [static let dataCorrupted: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/datacorrupted)
- [static let firstReserved: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/firstreserved)
- [static let generic: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/generic)
- [static let keyNotFound: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/keynotfound)
- [static let timeout: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/timeout)
- [static let typeMismatch: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/typemismatch)
- [static let valueNotFound: Int](/documentation/managedapp/managedappconfigurationdecodingerrorcode/valuenotfound)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
