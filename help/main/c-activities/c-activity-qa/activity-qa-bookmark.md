---
keywords: qa;preview;bookmarklet;voorbeeld koppelingen
description: Leer hoe te om Adobe  [!DNL Target]  QA bookmarklet te gebruiken om  [!DNL Target]  te dwingen om u van wijze vrij te geven QA.
title: Hoe gebruik ik de Activity QA Bookmarklet?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
source-git-commit: 4b5111c00384fdc73eaadbf0eec22ac6c2784a22
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Activity QA-bladwijzer

Informatie die u helpt bij het gebruik van de [!DNL Target] QA-bladwijzer om [!DNL Target] te dwingen de QA-modus te verlaten.

>[!NOTE]
>
>Het proces voor het maken van een bladwijzer varieert per type browser en versie. Raadpleeg de Help van uw browser of zoek op internet voor specifieke instructies.

## Activity QA bookmarklet voor at.js 1.*x*

Omdat [&#x200B; wijze QA &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa.md) kleverig is, nadat u een website op wijze QA doorbladert, moet uw [!DNL Target] zitting verlopen of u moet [!DNL Target] geven u van wijze QA alvorens u uw plaats als een typische bezoeker kunt bekijken. Gebruik de bladwijzer QA [!DNL Target] om uzelf uit de modus QA te forceren.

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

U kunt uzelf ook handmatig afdwingen uit de QA-modus door een pagina op uw site te laden met de parameter `at_preview_token` met een lege waarde.

Bijvoorbeeld:

`https://www.mysite.com/?at_preview_token=`

## Activity QA bookmarklet voor at.js 2.*x*

In tegenstelling tot at.js 1.*x*, at.js 2.*x* steunt derdekoekjes niet, en de wijze QA is slechts kleverig voor het eerste-partijdomein (door middel van een eerstepartijkoekje dat door at.js wordt geplaatst). Dus in at.js 2.*x*, QA wordt wijzesessie beheerd slechts op cliënt-kant en geen QA wijzecookies worden verzonden naar Doel.

Als u de [!DNL Target] QA-bladwijzer wilt gebruiken, maakt u een bladwijzer met de volgende JavaScript-code en voegt u deze toe aan de werkbalk Bladwijzers van uw browser:

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {            
            document.cookie = AT_QA_MODE + ';domain='+window.location.hostname+";Path=/; Max-Age=-0;";
            var token = window.location.href.indexOf("?at_preview_token")<0? "&at_preview_token" : "?at_preview_token";
            var url = window.location.href.split(token,2)[0];
            window.open(url, '_self', 'noreferrer');
        }
    })(); 
```

## De Activity QA-bladwijzer gebruiken

Klik op de bladwijzer op de werkbalk van uw browser.
