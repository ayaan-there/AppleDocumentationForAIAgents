# Managed Settings UI Documentation

Source: https://sosumi.ai/documentation/managedsettingsui

---
title: ManagedSettingsUI
source: https://developer.apple.com/documentation/managedsettingsui
timestamp: 2026-02-13T18:59:05.233Z
---

## Shield Configuration

- [ShieldConfigurationDataSource](/documentation/managedsettingsui/shieldconfigurationdatasource)

### Styling an Application Shield

- [func configuration(shielding: Application) -> ShieldConfiguration](/documentation/managedsettingsui/shieldconfigurationdatasource/configuration(shielding:)-5uqm1)
- [func configuration(shielding: Application, in: ActivityCategory) -> ShieldConfiguration](/documentation/managedsettingsui/shieldconfigurationdatasource/configuration(shielding:in:)-ia14)

### Styling a Website Shield

- [func configuration(shielding: WebDomain) -> ShieldConfiguration](/documentation/managedsettingsui/shieldconfigurationdatasource/configuration(shielding:)-18i24)
- [func configuration(shielding: WebDomain, in: ActivityCategory) -> ShieldConfiguration](/documentation/managedsettingsui/shieldconfigurationdatasource/configuration(shielding:in:)-6n6rd)

### Initializers

- [init()](/documentation/managedsettingsui/shieldconfigurationdatasource/init())
- [ShieldConfiguration](/documentation/managedsettingsui/shieldconfiguration)

### Defining the Appearance

- [let backgroundBlurStyle: UIBlurEffect.Style?](/documentation/managedsettingsui/shieldconfiguration/backgroundblurstyle)
- [let backgroundColor: UIColor?](/documentation/managedsettingsui/shieldconfiguration/backgroundcolor)
- [let icon: UIImage?](/documentation/managedsettingsui/shieldconfiguration/icon)
- [let primaryButtonBackgroundColor: UIColor?](/documentation/managedsettingsui/shieldconfiguration/primarybuttonbackgroundcolor)
- [let primaryButtonLabel: ShieldConfiguration.Label?](/documentation/managedsettingsui/shieldconfiguration/primarybuttonlabel)
- [let secondaryButtonLabel: ShieldConfiguration.Label?](/documentation/managedsettingsui/shieldconfiguration/secondarybuttonlabel)
- [let subtitle: ShieldConfiguration.Label?](/documentation/managedsettingsui/shieldconfiguration/subtitle)
- [let title: ShieldConfiguration.Label?](/documentation/managedsettingsui/shieldconfiguration/title)
- [ShieldConfiguration.Label](/documentation/managedsettingsui/shieldconfiguration/label)

#### Initializers

- [init(text: String, color: UIColor)](/documentation/managedsettingsui/shieldconfiguration/label/init(text:color:))

#### Instance Properties

- [let color: UIColor](/documentation/managedsettingsui/shieldconfiguration/label/color)
- [let text: String](/documentation/managedsettingsui/shieldconfiguration/label/text)

### Creating the Shield Configuration

- [init(backgroundBlurStyle: UIBlurEffect.Style?, backgroundColor: UIColor?, icon: UIImage?, title: ShieldConfiguration.Label?, subtitle: ShieldConfiguration.Label?, primaryButtonLabel: ShieldConfiguration.Label?, primaryButtonBackgroundColor: UIColor?, secondaryButtonLabel: ShieldConfiguration.Label?)](/documentation/managedsettingsui/shieldconfiguration/init(backgroundblurstyle:backgroundcolor:icon:title:subtitle:primarybuttonlabel:primarybuttonbackgroundcolor:secondarybuttonlabel:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
