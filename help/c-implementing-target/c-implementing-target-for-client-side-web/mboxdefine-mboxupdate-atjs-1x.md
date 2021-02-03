---
keywords: mboxDefine;mboxdefine;mbox define;mboxUpdate;mbox update;mbox update;at.js;functions;function
description: Informatie over de functies mboxDefine() en mboxUpdate() voor de JavaScript-bibliotheek van Adobe Target at.js.
title: Mboxdefine() en Mboxupdate() - at.js 1.x
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# mboxDefine() en mboxUpdate() - at.js 1.x

Definieer en werk een box bij in Adobe Target.

>[!NOTE]
>
>Deze functies zijn beschikbaar voor at.js versies 1.** Alleen. Deze functies zijn vervangen door de release van at.js 2.x. Deze functies retourneren standaardinhoud als deze wordt gebruikt met at.js 2.x.

`mboxDefine()` en  `mboxCreate()` zijn gekoppeld aan HTML DIV-elementen waarin het aanbod moet worden weergegeven. Deze HTML DIV-elementen moeten de klasse `mboxDefault` hebben. Als deze klasse niet wordt gekoppeld aan de HTML-elementen, ziet u een merkbare flikkering.

## mboxDefine {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Maakt een interne toewijzing tussen een nodeId en een naam van een box, maar voert de aanvraag niet uit. Wordt gebruikt in combinatie met `mboxUpdate()`. Gemaakt in [!DNL at.js]vooral om de overgang van [!DNL mbox.js]naar [!DNL at.js] te vergemakkelijken.

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Voert het verzoek uit en past de aanbieding op het element toe dat door `nodeId` in `mboxDefine()` wordt geïdentificeerd. Kan ook worden gebruikt om een mbox bij te werken die door `mboxCreate` in werking wordt gesteld. Gemaakt in [!DNL at.js] vooral om de overgang van [!DNL mbox.js] naar [!DNL at.js] te vergemakkelijken. `mboxDefine()`/  `mboxUpdate()` kan worden vervangen door  [adobe.target.getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) en  [adobe.target.applyOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) met behulp van de selectoroptie.

## Voorbeeld {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```javascript
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```
