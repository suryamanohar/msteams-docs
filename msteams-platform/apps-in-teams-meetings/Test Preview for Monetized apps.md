---
title: Test Preview for Monetized apps 
author: ypalikila
description: overview of apps in Teams meetings based on participant and user role
ms.topic: overview
ms.author: ypalikila
ms.localizationpriority: medium
keywords: teams apps monetization preview offer  
---

# Test Preview for Monetized apps

As a developer, you can create a software as a service (SaaS) offer with the Teams app and test the end-to-end purchase experience of their Teams apps within teams before pushing the offer live. Anyone who has been added to the preview audience can test the preview offer withing Teams.

## Prerequisites

1. [Developer Account](https://docs.microsoft.com/en-us/office/developer-program/microsoft-365-developer-program-get-started)
1. [Create a SaaS offer](https://docs.microsoft.com/azure/marketplace/create-saas-dev-test-offer)
1. [Add a preview audience for a SaaS offer](https://docs.microsoft.com/azure/marketplace/create-new-saas-offer-preview)

## Create a preview offer ID

You need to create a preview offer ID for the SaaS offer using the **App Source preview link** in the Partner Center .

1. Go to [Partner Center](https://go.microsoft.com/fwlink/?linkid=2166002) and sign in using your developer credentials.
1. Select **Marketplace offers**.
1. Select the SaaS offer you want to preview.
1. Select **App source preview link** under **Go Live** to generate a Preview Offer ID.
1. Copy the Preview Offer ID generated in the URL along with the *-Preview* suffix.

:::image type="content" source="../assets/images/apps-in-meetings/publish-status-publisher-signoff.png" alt-text="App source preview":::

## Configure your app with the Preview offer ID

After you've generated your Preview offer ID, you must link the offer ID to your Teams app for the audience to view your Preview offer in the Teams Store.

1. Go to [Developer Portal](https://dev.teams.microsoft.com/).
1. Select **Apps** from the left nav pane.
1. Select the app you're linking the SaaS offer to.
1. Select **Plans and pricing** and enter the **Publisher ID** and **Offer ID**.
  1.  Ensure that the offer ID contains *-Preview* suffix.
1. Select **View** to preview your subscription plans.
1. Review the plans listed under **Apps Subscription** and click **Save**.

:::image type="content" source="../assets/images/apps-in-meetings/Plans-and-pricing-preview-offer.png" alt-text="preview offer label":::

The subscriptionOffer property is added to your app manifest.
```json
"subscriptio(nOffer": {
     "offerId": "publisherId.offerId"-preview  
     }
```
>[!NOTE]
> You can identify the preview offer with the label *preview offer* next to **Apps Subscription**.

## Sideload the app to Teams

After configuring your app with the preview offer ID, create an updated app package and upload the app package to Teams for the preview audience to test purchasing the app. For more information see [Upload your app in Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/apps-upload).
 
You can also select **Preview in Teams** in the developer portal to launch your app quickly in the Teams client.

:::image type="content" source="../assets/images/apps-in-meetings/Preview-in-teams.png" alt-text="Preview offer in Teams":::

>[!NOTE]
> * If the user is not part of the preview audience and tries to sideload the app. The user can't see **Buy a subscription** button and will see a warning *No plans found in the preview. Make  sure you're in the preview audience*.
> * If the **offer ID** specified in manifest is not for a preview offer, the user will not be able to sideload the app and  will see a warning *This isn't a preview offer, ensure to append '-preview' to the offer ID*.

## Next step

> [!div class="nextstepaction"]
> [Review and publish an offer to the commercial marketplace](https://docs.microsoft.com/azure/marketplace/review-publish-offer#validation-and-publishing-steps).

## See also

* [Configure SaaS offer properties](https://docs.microsoft.com/azure/marketplace/create-new-saas-offer-properties).