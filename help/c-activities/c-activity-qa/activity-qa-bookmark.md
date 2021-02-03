---
keywords: qa;preview;bookmarklet;voorvertoning van koppelingen
description: Informatie die u helpt bij het gebruik van de Adobe Target QA-bladwijzer om Target te forceren u uit de QA-modus vrij te geven.
title: Activity QA-bladwijzer
feature: Activities
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# Activity QA-bladwijzer

Informatie om u te helpen [!DNL Target] QA bookmarklet gebruiken om [!DNL Target] te dwingen om u van wijze QA vrij te geven.

>[!NOTE]
>
>Het proces voor het maken van een bladwijzer varieert per type browser en versie. Raadpleeg de Help van uw browser of zoek op internet voor specifieke instructies.

## Activity QA bookmarklet voor at.js 1.*x*

Omdat de QA-modus [vastzit, moet uw [!DNL Target]-sessie verlopen nadat u in de QA-modus door een website hebt gebladerd. Als u uw site als een typische bezoeker wilt bekijken, moet [!DNL Target] de QA-modus uitschakelen voordat u uw site kunt bekijken. ](/help/c-activities/c-activity-qa/activity-qa.md) Gebruik de bladwijzer QA [!DNL Target] om uzelf uit wijze QA te dwingen.

Als u de QA0/>-bladwijzer voor kwaliteitscontrole wilt gebruiken, maakt u een bladwijzer met de volgende JavaScript-code en voegt u deze toe aan de werkbalk Bladwijzers van uw browser:[!DNL Target]

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

U kunt uzelf ook handmatig uit de QA-modus afdwingen door een pagina op uw site te laden met de parameter `at_preview_token` met een lege waarde.

Bijvoorbeeld:

`https://www.mysite.com/?at_preview_token=`

## Activity QA bookmarklet voor at.js 2.*x*

In tegenstelling tot at.js 1.*x*, at.js 2.*De* xdoes geen steun derdekoekjes, en de wijze QA is slechts kleverig voor het eerste-partijdomein (door middel van een eerstepartijkoekje dat door at.js wordt geplaatst). Dus in at.js 2.*x*, wordt de QA wijzesessie beheerd slechts op cliënt-kant en geen QA wijzecookies worden verzonden naar Doel.

Als u de QA0/>-bladwijzer voor kwaliteitscontrole wilt gebruiken, maakt u een bladwijzer met de volgende JavaScript-code en voegt u deze toe aan de werkbalk Bladwijzers van uw browser:[!DNL Target]

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

