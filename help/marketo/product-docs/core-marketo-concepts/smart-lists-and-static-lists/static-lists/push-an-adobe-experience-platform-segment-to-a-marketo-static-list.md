---
description: Push an Adobe Experience Platform Segment to a Marketo Static List - Marketo Docs - Product Documentation
title: Push an Adobe Experience Platform Segment to a Marketo Static List
exl-id: 8df11bf4-06f4-4927-8dfb-954414fce6dc
---
# Push an Adobe Experience Platform Segment to a Marketo Static List {#push-an-adobe-experience-platform-segment-to-a-marketo-static-list}

This feature allows you to push segments located in your Adobe Experience Platform over to Marketo in the form of a static list.

>[!PREREQUISITES]
>
>* [Edit the API Role](/help/marketo/product-docs/administration/users-and-roles/create-delete-edit-and-change-a-user-role.md#edit-an-existing-role) to make sure it has the **Read-Write Person** permission (found under the Access API drop-down).
>* [Create an API User](/help/marketo/product-docs/administration/users-and-roles/create-an-api-only-user.md) in Marketo.
>* Go to **Admin** > **Launchpoint**. Find the name of the role you just created and click **View Details**. Copy and save the info in **Client ID** and **Client Secret**, as you could need it for Step 7.
>* In Marketo, create a static list, or find and select one you've already created. You'll need its ID.

1. Log in to [Adobe Experience Platform](https://experience.adobe.com/).

   ![](assets/push-an-adobe-experience-platform-segment-1.png)

1. Click the grid icon and select **Experience Platform**.

   ![](assets/push-an-adobe-experience-platform-segment-2.png)

1. In the left nav, click **Destinations**.

   ![](assets/push-an-adobe-experience-platform-segment-3.png)

1. Click **Catalog**.

   ![](assets/push-an-adobe-experience-platform-segment-4.png)

1. Find the Marketo Engage tile and click **Activate**.

   ![](assets/push-an-adobe-experience-platform-segment-5.png)

1. Click **Configure New Destination**.

   ![](assets/push-an-adobe-experience-platform-segment-6.png)


1. Under Account Type, select the Existing or New Account radio button (in this example, we're choosing **Existing Account**). Click the Select Account icon.

   ![](assets/push-an-adobe-experience-platform-segment-7.png)

   >[!NOTE]
   >
   >If you are choosing New Account, you can find your Munchkin ID by going to **Admin** > **Munchkin** (it's also part of your Marketo URL once logged in). Client ID/Secret you should have from following the prerequisites at the top of this article.

1. Choose the destination account and click **Select**.

   ![](assets/push-an-adobe-experience-platform-segment-8.png)

1. Enter a Destination **Name** and an optional Description. Click the Person Creation drop-down and choose "Match Existing Marketo People and Create Missing People in Marketo" _or_ "Match Existing Marketo People Only." In this example we're choosing the former.

   ![](assets/push-an-adobe-experience-platform-segment-9.png)

   >[!NOTE]
   >
   >If you choose "Match Existing Marketo People Only" you'll only need to map the Email and/or ECID, so you can skip Steps 13-16.

1. This section is optional. Click **Create** to skip.

   ![](assets/push-an-adobe-experience-platform-segment-10.png)

1. Select the destination you created and click **Next**.

   ![](assets/push-an-adobe-experience-platform-segment-11.png)

1. Choose the segment you want to send to Marketo and click **Next**.

   ![](assets/push-an-adobe-experience-platform-segment-12.png)

   >[!NOTE]
   >
   >If you choose multiple segments, you'll have to map each segment to a specified static list in the Segment Schedule tab.

   >[!IMPORTANT]
   >
   >After a segment has been activated to the Marketo destination for the first time, backfilling profiles that already existed in the segment prior to Marketo destination activation can take **up to 24 hours**. Going forward, any time profiles are added to the segment, they'll be added to Marketo immediately.

1. Click **Add New Mapping**.

   ![](assets/push-an-adobe-experience-platform-segment-13.png)

1. Click the mapping icon.

   ![](assets/push-an-adobe-experience-platform-segment-14.png)

1. Map First Name by selecting **firstName** and clicking **Select**.

   ![](assets/push-an-adobe-experience-platform-segment-15.png)

1. Map the Last Name and Company Name by clicking **Add New Mapping** again and repeating Step 15 twice, choosing **lastName** and then **companyName**.

   ![](assets/push-an-adobe-experience-platform-segment-16.png)

1. Now it's time to map the email address. Click **Add New Mapping** again.

   ![](assets/push-an-adobe-experience-platform-segment-17.png)

1. Click the mapping icon.

   ![](assets/push-an-adobe-experience-platform-segment-18.png)

1. Click the Select Identity Namespace radio button, choose  **Email**, then click **Select**.

   ![](assets/push-an-adobe-experience-platform-segment-19.png)

   >[!IMPORTANT]
   >
   >Mapping Email and/or ECID from the **Identity Namespace** tab is the most important thing to do to ensure the person is matched in Marketo. Mapping Email will ensure the highest match rate.

1. Now it's time to choose the source fields. For email, click the cursor icon.

   ![](assets/push-an-adobe-experience-platform-segment-20.png)

1. Click the Select Identity Namespace radio button, find and select **Email**, then click **Select**.

   ![](assets/push-an-adobe-experience-platform-segment-21.png)

1. To choose the Company Name source field, click the cursor icon in its row.

   ![](assets/push-an-adobe-experience-platform-segment-22.png)

1. Leave the Select Attributes radio button checked. Search for "company" and select **companyName**, then click **Select**.

   ![](assets/push-an-adobe-experience-platform-segment-23.png)

1. Map the source fields for Last Name and First Name by clicking the cursor icon for each and repeating Step 23 twice, choosing **lastName** and then **firstName**.

   ![](assets/push-an-adobe-experience-platform-segment-24.png)

1. Click **Next**.

   ![](assets/push-an-adobe-experience-platform-segment-25.png)

1. You will now need your list's ID. Click the tab in your browser that has your Marketo static list open (or open a new tab and select your desired static list).

   ![](assets/push-an-adobe-experience-platform-segment-26.png)

   >[!NOTE]
   >
   >For best results, use an empty Marketo Engage list.

1. Highlight and copy the list ID at the end of the URL.

   ![](assets/push-an-adobe-experience-platform-segment-27.png)

1. Paste the ID you just copied under Mapping ID and click **Next**.

   ![](assets/push-an-adobe-experience-platform-segment-28.png)

1. Click **Finish**.

   ![](assets/push-an-adobe-experience-platform-segment-29.png)
