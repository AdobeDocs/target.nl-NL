---
keywords: qa;preview;bookmarklet;preview links
description: Informatie die u helpt bij het gebruik van de Adobe Target QA-bladwijzer om Target te forceren u uit de QA-modus vrij te geven.
title: Activity QA-bladwijzer voor Adobe Target
feature: null
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---


# Activity QA-bladwijzer{#activity-qa-bookmarklet}

Informatie die u helpt met het gebruik van de [!DNL Target] [!DNL Target] QA-bladwijzer om u af te dwingen van de QA-modus.

Omdat de [QA-modus](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) vastzit, moet uw [!DNL Target] sessie verlopen nadat u in de QA-modus door een website hebt gebladerd. U moet de QA-modus [!DNL Target] loslaten voordat u uw site als een typische bezoeker kunt bekijken. Gebruik de QA- [!DNL Target] boekmarkering om uzelf uit de QA-modus te forceren.

Als u de [!DNL Target] QA-bladwijzer wilt gebruiken, maakt u een bladwijzer met de volgende JavaScript-code en voegt u deze toe aan de werkbalk Bladwijzers van uw browser:

```
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

De bladwijzer moet dan op de werkbalk worden weergegeven voor hergebruik.

>[!NOTE]
>
>Het proces voor het maken van een bladwijzer varieert per type browser en versie. Raadpleeg de Help van uw browser of zoek op internet voor specifieke instructies.

U kunt uzelf ook handmatig uit de QA-modus afdwingen door een pagina op uw site te laden met de `at_preview_token` parameter met een lege waarde.

Bijvoorbeeld:

`https://www.mysite.com/?at_preview_token=`
