---
description: Audience Criteria - Marketo Docs - Product Documentation
title: Audience Criteria
exl-id: 9b70b03e-229e-469e-bd65-07aaf2dcbec6
---
# Audience Criteria {#audience-criteria}

Similar to Marketo Smart Lists, Audience Criteria attributes allow you to define your target audience. You can target known or unknown people using inferred, person, or company attributes (or a combination thereof).

## Events {#events}

   ![](assets/audience-criteria-0.png)

Events allow you to target visitors based on how much they scroll or how long they're on your page/site. In the example below, we're targeting visitors who have been on a specific page for more than 20 seconds.

1. Grab the **Time on Page** event and drag it to the right.

   ![](assets/audience-criteria-0a.png)

1. Set the "Greater Than" time to 20 seconds.

   ![](assets/audience-criteria-0b.png)

1. Add the URL of the desired page in the [Target](#target) section.

   ![](assets/audience-criteria-0c.png)

## Attributes {#attributes}

   ![](assets/audience-criteria-0d.png)

**Known People**

There are _many_ attribute combinations to choose from. In the example below, we're targeting all **known people** in California who work at a company with more than 50 employees.

1. Grab the **Person State** attribute and drag it to the right.

   ![](assets/audience-criteria-1.png)

1. _Is_ is set by default. In the Select Values field, type in CA (you can also click the drop-down and select from the list).

   ![](assets/audience-criteria-2.png)

1. Grab the **Company Size** attribute and drag it to where it says _drag and drop an attribute here_.

   ![](assets/audience-criteria-3.png)

   >[!NOTE]
   >
   >You can also choose an attribute by clicking its **+** icon.

1. Click the operator drop-down and select **Greater Than**.

   ![](assets/audience-criteria-4.png)

1. Type 50 and click elsewhere on the screen to save.

   ![](assets/audience-criteria-5.png)

And that's it!

**Anonymous People**

There's an easy way to specifically target people who are not in your database yet. In this example, we're targeting all **anonymous people** located in the New York area.

1. Grab the **Person Email** attribute and drag it to the right.

   ![](assets/audience-criteria-6.png)

1. Click the operator drop-down and select **Is Empty**.

   ![](assets/audience-criteria-7.png)

1. Grab the **Inferred State** attribute and drag it to where it says _drag and drop an attribute here_.

   ![](assets/audience-criteria-8.png)

   >[!NOTE]
   >
   >When someone visits your website, [Munchkin](/help/marketo/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website.md) cookies them and puts them into the system. We look up their IP in a special database and infer all kinds of good info.

1. _Is_ is set by default. In the Select Values field, type in NY (you can also click the drop-down and select from the list).

   ![](assets/audience-criteria-9.png)

## Add Groups {#add-groups}

You have the option of grouping attributes as well, in case you want to have all of certain attributes along with "all or any" of another. You can add multiple groups.

   ![](assets/audience-criteria-10.png)

   ![](assets/audience-criteria-11.png)

## Target {#target}

This is where you enter the URL(s) that you want a specific Dialogue to be shown on. You also have the option of adding exclusions.

Acceptable formats:

* `http://website.com`
* `https://*.website.com`
* `http://website.com/folder/*`
* `https://*.website.com/folder/*`

>[!NOTE]
>
>Using an asterisk acts as a catch-all wilcard. So `https://*.website.com` would put the dialogue on every page of the site, including subdomains (ex: `support.website.com`). And `https://website.com/folder/*` would put the dialogue on every HTML page in the subsequent folder (ex: in this case let's say the folder is "sports," so: website.com/sports/baseball.html, website.com/sports/football.html, etc.).

**Exclusions**

Use exclusions to ensure your Dialogue does **not** appear on a specific page/area of your site. Exclusions follow the same format as inclusions.

   ![](assets/audience-criteria-12.png)

>[!MORELIKETHIS]
>
>* [Create a Dialogue](/help/marketo/product-docs/demand-generation/dynamic-chat/dialogues/create-a-dialogue.md){target="_blank"}
>* [Stream Designer](/help/marketo/product-docs/demand-generation/dynamic-chat/dialogues/stream-designer.md){target="_blank"}
>* [Reports](/help/marketo/product-docs/demand-generation/dynamic-chat/dialogues/reports.md){target="_blank"}
