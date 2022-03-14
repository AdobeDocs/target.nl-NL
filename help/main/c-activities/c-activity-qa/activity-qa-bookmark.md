---
keywords: qa;preview;bookmarklet;voorvertoning van koppelingen
description: Leer hoe u de Adobe gebruikt [!DNL Target] QA-boekmarkering afdwingen [!DNL Target] om u van wijze QA vrij te geven.
title: How Do I use the Activity QA Bookmarklet?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Activity QA bookmarklet

Informatie die u helpt bij het gebruik van de [!DNL Target] QA-boekmarkering afdwingen [!DNL Target] om u van wijze QA vrij te geven.

>[!NOTE]
>
>The process to create a bookmarklet varies by browser type and version. Consult your browser&#39;s help or search on the Internet for specific directions.

## Activity QA bookmarklet voor at.js 1.*x*

Because [QA mode](/help/main/c-activities/c-activity-qa/activity-qa.md) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. De kwaliteitscontrole gebruiken [!DNL Target] bookmarklet om uzelf uit wijze te dwingen QA.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser&#39;s Bookmarks Toolbar:

```javascript
javascript:(
    function () {
        if (window.location.href.indexOf('?') != -1) {
            var parts = window.location.href.split('at_preview_token',2);
            if (parts.length > 1) {
                window.location.href = parts[0].concat('at_preview_token=');
            } else {
                window.location.href = window.location.href.concat("&at_preview_token=")
            }
        } else {
            window.location.href = window.location.href.concat("?at_preview_token=")
        }
    }
)();
```

U kunt uzelf ook handmatig uit de QA-modus afdwingen door een pagina op uw site te laden met de `at_preview_token` parameter met een lege waarde.

Bijvoorbeeld:

`https://www.mysite.com/?at_preview_token=`

## Activity QA bookmarklet voor at.js 2.*x*

In contrast to at.js 1.*x*, om.js 2.*x* ondersteunt geen cookies van derden en de QA-modus blijft alleen van toepassing op het domein van de eerste partij (door middel van een cookie van de eerste partij ingesteld door at.js). Dus in at.js 2.*x*, wordt de QA wijzesessie beheerd slechts op de cliënt-kant en geen QA wijzecookies worden verzonden naar Doel.

Als u de opdracht [!DNL Target] Maak een bladwijzerplaat voor QA-bladwijzers die de volgende JavaScript-code bevat en voeg deze toe aan de werkbalk Bladwijzers van uw browser:

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {
            document.cookie = AT_QA_MODE + '; Path=/; Max-Age=-0;';
            var url = window.location.href.split('at_preview_token',2)[0];
            window.open(url.substring(0, url.length - 1), '_self', 'noreferrer');
        }
    })();
```

## De Activity QA-bladwijzer gebruiken

Klik op de bladwijzer op de werkbalk van uw browser.
