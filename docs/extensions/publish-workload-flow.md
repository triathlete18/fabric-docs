---
title: Overview of Fabric extensibility publishing flow (Public Preview)
description: Learn how to publish a workload over the Fabric extensibility platform.
author: rasala
ms.author: rasala, gesaur
ms.reviewer: gesaur
ms.topic: how-to
ms.custom:
ms.date: 04/17/2024
---

# Intro
This document is about publishing a workload extension to Fabric Hub. To learn more about Fabric and workloads [find these article](https://review.learn.microsoft.com/en-us/fabric/extensions/extensibility-overview?branch=release-extensibility#introduction).

The Fabric Workload Hub serves as a marketplace. Users can browse, explore, and manage workloads within Fabric. Workloads are categorized into two groups: Core Fabric workloads and those developed by Microsoft partners.

The hub is structured with two main views:

**My Workloads:** This view lists the workloads that have been added by the user or others within the organization, including built-in workloads that are part of Fabric.

**More Workloads:** This view showcases all available workloads that can be added to Fabric.

Publishing your workload to the Fabric Workload Hub involves several key steps to ensure a smooth and successful process. Below is a step by step flow with other details to guide you through each stage. Review all steps before you start developing your workload and make sure you comply with all of the mandatory requirements.



## Step 1: Develop and Test Your Workload
Ensure your workload is compatible with the Fabric Extensibility framework and prepare your branding materials for listing.
Find this comprehensive [guide](https://github.com/microsoft/Microsoft-Fabric-developer-sample/blob/main/README.md) that covers everything you need to know to create your own custom Fabric workload.

## Step 2: Comply with the requirements
In order to pass all validation checks and display it publicly in the Fabric Workload Hub, your workload must comply with the following functional and design [requirements.](./requirements.md)


## Step 3: Create an Azure  Marketplace Listing 

### Prerequisite
To submit your Fabric, you must be enrolled with [Partner Center](https://learn.microsoft.com/partner-center/overview). If you're not yet enrolled, [Open a developer account in Partner Center](https://learn.microsoft.com/azure/marketplace/create-account).

### 3.1. Create a SaaS offer
Once you have a Partner Center account follow these [steps](https://learn.microsoft.com/partner-center/marketplace/create-new-saas-offer) to create a SaaS offer.
If your already have an exting SaaS offer in Azure Marketplace, you don't need to create a new one. Just make sure the SaaS offer metadata in Partner center and the Workload package metadata you created, are identical and that the you comply to the SaaS offer [requirements.](./requirements.md), then add the SaaS offer public link to the metadata as described in in section 3.1 in this article.
Choose the configuration based on your solution and business model presences. For instance if you already have a transacatbility model choose the option "No, I would prefer to only list my offer through the marketplace and process transactions independently".

The SaaS offer linked to the Fabric Workload must meet all requirements defined in [100 General](https://learn.microsoft.com/legal/marketplace/certification-policies#100-general) and [1000 Software as a Service (SaaS)](https://learn.microsoft.com/legal/marketplace/certification-policies#1000-software-as-a-service-saas) Find more information about the SaaS [requirements.](./requirements.md). 

> [!NOTE]
> Your SaaS offer must have [Azure Marketplace](https://azuremarketplace.microsoft.com/home) storefront entry. Having both [AppSource](https://appsource.microsoft.com/) and Azure Marketplace is also allowed. However, the offer setup combination of "Yes, I would like to sell through Microsoft and have Microsoft host transactions on my behalf" and "Yes, I would like Microsoft to manage customer licenses on my behalf" will create a SaaS offer in AppSource only, therefore it is not supported. 

> [!NOTE]
> Offer metadata should match across the Fabric Workload pacake manifests and the SaaS listing in Azure Marketplace. Any duplicated metadata should be identical in SaaS offer setup in Partner Ceneter and in the Workload package manifest. Metadata includes but not limited to:
> Workload title
> Icons
> Screenshots
> Descriptions
> Publisher name
> Product compliance documentations



### 3.1. Link your SaaS offer to Workload package
The SaaS offer must be live in Azure Marketplace and has at least one public plan. The Workload package manifest should completely and accurately define the public SaaS URL linked to the Workload manifest. In the `licnese` field under the `supportLink` section add the public SaaS link offer linked to your Workload. 

## Step 4 Reach out to our Workload Fabric Team
Once you have a public SaaS link in Azure Marketplace and the Workload complies with the [requirements.](./requirements.md),
reach out to our team for opting in to the public preview
mailto: fabric_wdt_submission@service.microsoft.com
Include in your email:
* Workload package
> [!NOTE]
Either the publisher of SaaS offer shoud be the same publisher who reach out to us via emial, OR the email domain of the engineering contact in the SaaS offer (in offer listing page) should match the email domain of the publisher reaching out to us with the Workload package. 

## Step 5 Preview and publish your workload
After your package passed validation you'll receive an email from the team, and you'll be able to preview your workload with specific tenants or publicly publish it to all tenants through the "Workload" page in the admin portal that will be available only for ISVs who passed validation and opt in to PuPr.

If you are willing to update any of the duplicated metadata such as Workload description, title and screenshots you should resubmit your SaaS offer and update the metadata in both; Workload package manifest and the SaaS offer metadata in Partner Center. Changes in metadata available only in Workload package manifest requires only a resubmission of new Workload package. 
   
    