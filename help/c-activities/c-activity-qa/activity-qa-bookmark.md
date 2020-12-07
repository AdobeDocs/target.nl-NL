---
keywords: qa;preview;bookmarklet;preview links
description: Informatie die u helpt bij het gebruik van de Adobe Target QA-bladwijzer om Target te forceren u uit de QA-modus vrij te geven.
title: Activity QA-bladwijzer voor Adobe Target
feature: qa
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Activity QA-bladwijzer{#activity-qa-bookmarklet}

Informatie die u helpt met het gebruik van de [!DNL Target] [!DNL Target] QA-bladwijzer om u af te dwingen van de QA-modus.

>[!NOTE]
>
>Het proces voor het maken van een bladwijzer varieert per type browser en versie. Raadpleeg de Help van uw browser of zoek op internet voor specifieke instructies.

## Activity QA bookmarklet voor at.js 1.*x*

Omdat de [QA-modus](/help/c-activities/c-activity-qa/activity-qa.md) vastzit, moet uw [!DNL Target] sessie verlopen nadat u in de QA-modus door een website hebt gebladerd. U moet de QA-modus [!DNL Target] loslaten voordat u uw site als een typische bezoeker kunt bekijken. Gebruik de QA- [!DNL Target] boekmarkering om uzelf uit de QA-modus te forceren.

Als u de [!DNL Target] QA-bladwijzer wilt gebruiken, maakt u een bladwijzer met de volgende JavaScript-code en voegt u deze toe aan de werkbalk Bladwijzers van uw browser:

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

In tegenstelling tot at.js 1.*x*, at.js 2.*x* ondersteunt geen cookies van derden en de QA-modus blijft alleen van toepassing op het domein van de eerste partij (door middel van een cookie van de eerste partij ingesteld door at.js). Dus in at.js 2.*x*, wordt de QA wijzesessie beheerd slechts op cliënt-kant en geen QA wijzecookies worden verzonden naar Doel.

Als u de [!DNL Target] QA-bladwijzer wilt gebruiken, maakt u een bladwijzer met de volgende JavaScript-code en voegt u deze toe aan de werkbalk Bladwijzers van uw browser:

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

