---
author: jnHs
Description: Add-ons are published through the Windows Dev Center dashboard.
title: Add-on submissions
ms.assetid: E175AF9E-A1D4-45DF-B353-5E24E573AE67
ms.author: wdg-dev-content
ms.date: 02/08/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp
---

# Add-on submissions

Add-ons (also sometimes referred to as in-app products) are supplementary items for your app that can be purchased by customers. An add-on can be a fun new add-on feature, a new game level, or anything else you think will keep users engaged. Not only are add-ons a great way to make money, but they help to drive customer interaction and engagement.

Add-ons are published through the Windows Dev Center dashboard. You'll also need to [enable the add-ons](../monetize/in-app-purchases-and-trials.md) in your app's code.

The first step in the add-on submission process is to create the add-on in the dashboard by [defining its product type and product ID](set-your-add-on-product-id.md). After that, you can create a submission so that your add-on can be purchased via the Windows Store. You can submit an add-on at the same time you [submit your app](app-submissions.md), or you can work on it independently. And you can make [updates](#updating-an-add-on-after-publication) to add-ons after the app is in the Store without having to resubmit the app again.

> **Note**&nbsp;&nbsp;This section of the documentation describes how to submit add-ons in the Dev Center dashboard. Alternatively, you can use the [Windows Store submission API](../monetize/create-and-manage-submissions-using-windows-store-services.md) to automate add-on submissions.

## Checklist for submitting an add-on

Here's a list of the info that you provide when creating your add-on submission. The items that you are required to provide are noted below. Some of these are optional, or have default values already provided that you can change as desired.

### Create a new add-on page
| Field name                    | Notes                            |
|-------------------------------|----------------------------------|
| [**Product type**](set-your-add-on-product-id.md#product-type)      | Required. If **Durable**, a **Product lifetime** is required. |  
| [**Product ID**](set-your-add-on-product-id.md#product-id)          | Required |        

<span/>

### Properties page
| Field name                    | Notes                              |   
|-------------------------------|------------------------------------|
| [**Product lifetime**](enter-add-on-properties.md#product-lifetime)  | Required if the product type is **Durable**. Not applicable to other product types. |
| [**Quantity**](enter-add-on-properties.md#quantity)  | Required if the product type is **Store-managed consumable**. Not applicable to other product types.
| [**Content type**](enter-add-on-properties.md#content-type)          | Required       |               
| [**Keywords**](enter-add-on-properties.md#keywords)                  | Optional (up to 10 keywords, 30 character limit each) |
| [**Custom developer data**](enter-add-on-properties.md#custom-developer-data)                               | Optional (3000 character limit)             |

<span/>

### Pricing and availability page
| Field name                    | Notes                                       |
|-------------------------------|---------------------------------------------|
| [**Base price**](set-add-on-pricing-and-availability.md#base-price)                | Required                                    |
| [**Markets and custom pricing**](set-add-on-pricing-and-availability.md#markets-and-custom-prices)  | Default: available in all possible markets |
| [**Sale pricing**](put-apps-and-add-ons-on-sale.md)               | Optional                             |
| [**Distribution and visibility**](set-add-on-pricing-and-availability.md#distribution-and-visibility)   | Default: add-on can be found by customers browsing or searching the Store |
| [**Publish date**](set-add-on-pricing-and-availability.md#publish-date)                | Default: Publish as soon as the add-on passes certification |

<span/>

### Store listings
One Store listing required. We recommend providing Store listings for every [language](create-add-on-store-listings.md#languages) your app supports.

| Field name                    | Notes                                       |
|-------------------------------|---------------------------------------------|
| [**Title**](create-add-on-store-listings.md#title)                    | Required (100 character limit)              |
| [**Description**](create-add-on-store-listings.md#description)       | Optional (200 character limit)              |
| [**Icon**](create-add-on-store-listings.md#icon)                    | Optional (.png, 300x300 pixels)             |

<span/>

When you've finished entering this info, click **Submit to the Store**. In most cases, the certification process takes about an hour. After that, your add-on will be published to the Store and ready for customers to purchase.

>**Note**&nbsp;&nbsp;The add-on must also be implemented in your app's code. For more info, see [In-app purchases and trials](../monetize/in-app-purchases-and-trials.md).


## Updating an add-on after publication

You can make changes to a published add-on at any time. add-on changes are submitted and published independently of your app, so you generally don't need to update the entire app in order to make changes to an add-on such as updating its price or description.

> **Important**&nbsp;&nbsp;If your app is available to customers on Windows 8.x, you will need to create and publish a new app submission in order to make the add-on updates visible to those customers. Similarly, if you add new add-ons to an app targeting Windows 8.x after the app has been published, you'll need to update your app's code to reference those add-ons, then resubmit the app. Otherwise, the new add-ons won't be visible to customers on Windows 8.x.

To submit updates, go to the add-on's page in your dashboard and click **Update**. This will create a new submission for the add-on using the info from your previous submission as a starting point. Change the info you'd like, and then click **Submit to the Store**.

If you'd like to remove an add-on you've previously offered, you can do this by creating a new submission and changing the [Distribution and visibility](set-add-on-pricing-and-availability.md) option to **No longer available for purchase. Not displayed in your app's listing**. Be sure to update your app's code as needed to also remove references to the add-on.
