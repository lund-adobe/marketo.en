---
unique-page-id: 14352602
description: My Dynamic Fields Aren't Filling Out - Marketo Docs - Product Documentation
title: My Dynamic Fields Aren't Filling Out
exl-id: fb3e8b56-506a-41f8-a84f-41370381c058
---
# My Dynamic Fields Aren't Filling Out {#my-dynamic-fields-arent-filling-out}

Dynamic fields will only work when you're using a template. Individual one-off emails that you write won't fill these out.

## What to Check {#what-to-check}

There are three types of dynamic fields in Sales Connect: Basic, Custom, and Salesforce. Basic and Custom both look to pull information from the [web application](https://toutapp.com/login). If the information does not exist in the web application, the fields will be blank. Salesforce fields pull information from [Salesforce.com](https://salesforce.com).

**Troubleshooting Salesforce Fields**

Salesforce Fields: e.g. `{{sfdc_account_name}}`

* Make sure it's properly hooked up with Sales Connect. Go to the [Settings](https://toutapp.com/login) page and click **Manage** next to your CRM.

**Troubleshooting Basic and Custom Fields**

Tout Basic Fields: e.g. `{{company}}`

Tout Custom Fields: e.g. `{{custom_field_favorite_movie}}`

* The corresponding field needs to be saved for your contact in the [People page](https://toutapp.com/next#relationships) for our dynamic field to reference. For example, if you're sending an email to Mary and using the `{{company}}` field, but her contact record doesn't list a company, we won't be able to fill that out.

## Why Did My Email Send Without Populating All Dynamic Fields? {#why-did-my-email-send-without-populating-all-dynamic-fields}

Sales Connect will stop your emails from being sent out if we cannot populate all your dynamic fields in the email. **However**, there are a few exceptions to this rule. Some fields will send out blank, or auto-populate a value if we can find one. These fields and how they'll react if they can't populate the field are listed below.

`{{first_name}}` = BLANK

`{{last_name}}` =BLANK

`{{title}}` = BLANK

`{{company}}` = "your company"

`{{friendly_company}}` = "your company"

>[!NOTE]
>
>The `{{first_name}}` field will look in both Sales Connect and Salesforce to attempt to pull information. All other fields in this list are only looking in Sales Connect to populate the field.
