---
title: "Service Encryption"
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.date: 10/3/2019
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: "Summary: Understand data resiliency in Microsoft Office 365."
---

# Service Encryption

In addition to using volume-level encryption, Exchange Online, Skype for Business, SharePoint Online, and OneDrive for Business also use Service Encryption to encrypt customer data. Service Encryption allows for two key management options:

- Microsoft manages all cryptographic keys. (This option is currently available in SharePoint Online, OneDrive for Business, and Skype for Business.)

- Your organization supplies the root keys. You manage these keys using Azure Key Vault. This option is called Customer Key. Customer Key is currently available for Exchange Online, SharePoint Online, OneDrive for Business, Skype for Business, and Teams files. If you use Customer Key, these keys replace Microsoft-managed keys to encrypt your data.

Service encryption provides multiple benefits. For example, Customer Key:

- Provides rights protection and management features on top of strong encryption protection.

- Includes a Customer Key option that enables multi-tenant services to provide per-tenant key management.

- Provides separation of Windows operating system administrators from access to customer data stored or processed by the operating system.

- Enhances the ability of Microsoft 365 to meet the demands of customers that have compliance requirements regarding encryption.

## Customer Key

Using Customer Key, you can generate your own cryptographic keys using either an on-premises Hardware Service Module (HSM) or Azure Key Vault (AKV). Regardless of how you generate the key, you use AKV to control and manage the cryptographic keys used by Office 365. Once your keys are stored in AKV, they can be used as the root of one of the keychains that encrypts your mailbox data or files.

Another benefit of Customer Key is the control you have over the ability of Microsoft to process your data. If you want to remove data from Office 365, such as if you want to terminate service with Microsoft or remove a portion of your data stored in the cloud, you can do so and use Customer Key as a technical control. This ensures that no one, including Microsoft, can access or process the data. Customer Key is in addition and complementary to Customer Lockbox that you use to control access to your data by Microsoft personnel.

To learn how to set up Customer Key for Microsoft 365 for Exchange Online, Skype for Business, SharePoint Online, including Team Sites, and OneDrive for Business, see these articles:

- [Service encryption with Customer Key](customer-key-overview.md)

- [Set up Customer Key](customer-key-set-up.md)

- [Manage Customer Key](customer-key-manage.md)

- [Roll or rotate a customer key or an availability key](customer-key-availability-key-roll.md)

- [Understand the availability key](customer-key-availability-key-understand.md)
 
