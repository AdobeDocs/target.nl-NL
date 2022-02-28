---
keywords: mbox;mbox3rdPartyId;profile syncing;profile synch;PCID
description: Learn how to use the mbox3rdPartyId, which is your organization's visitor ID, such as membership ID or your organization's loyalty program.
title: How Do I Use Real-Time Profile Syncing for mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 8969b3b04b8f02a4ae9860bafe4b0a1c80a6f35e
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Real-time profile syncing for mbox3rdPartyId

`mbox3rdPartyId`[!DNL Adobe Target]

When a visitor logs in to a company&#39;s site, the company typically creates an ID that is tied to the visitor&#39;s account, loyalty card, membership number, or other applicable identifiers for that company.

[!DNL Target][!DNL Target] `mbox3rdPartyId`[!DNL Target][!DNL Target]`mbox3rdPartyId`[!DNL Target]

Every three to five minutes, updates are synced with the database. `mbox3rdPartyId` `mbox3rdPartyId``mbox3rdPartyId``mbox3rdPartyId` `mbox3rdPartyId``mbox3rdPartyId`

| PCID (Not Logged In) | mbox3rdPartyId (Logged In) | Merged and Saved to mbox3rdPartyId |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Activity 1, Experience A | Activity 1, Experience B | Activity 1, Experience B |
| Activity 1 |  | Activity 1 |

When the visitor logs out, the merged profile is maintained.

>[!NOTE]
>
>[!DNL Adobe Experience Cloud Identity Service] After a user is associated with mbox3rdPartyID, it remains associated with the user even after signing out.

>[!NOTE]
>
>[!DNL Adobe Analytics][!DNL Adobe Experience Cloud][!DNL Target] [!DNL Analytics for Target]

## Considerations {#considerations}

* `3rdPartyID`[!DNL Target] `3rdPartyID` `3rdPartyId`

   For example, suppose that a visitor accesses a page before logging in and sees an experience. `3rdPartyID` `3rdPartyID` The visitor visits various pages on the site and then uses the Back button to return to the main page accessed before logging in and sees a different experience. `3rdPartyID` `3rdPartyID`

* [!DNL Target]

   1. `mbox3rdPartyId``thirdPartyId`

      * `mbox3rdPartyId``targetPageParams``targetPageParamsAll`
      * `thirdPartyId`
      * You can send only one value in this parameter.
   1. `setCustomerId``customerIds`

      * `setCustomerId`
      * `customerIds`
      * `mbox3rdPartyId``thirdPartyId`[!DNL Target]

   `mbox3rdPartyId``thirdPartyId`[!DNL Target][!DNL Adobe Experience Cloud] `setCustomerId``customerIds`

   >[!IMPORTANT]
   >
   > [!DNL Target]
   >
   >`mbox3rdPartyId``thirdPartyId``setCustomerID``customerIds`
   >
   >`setCustomerID``customerIds``thirdPartyId``mbox3rdPartyId`

