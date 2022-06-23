---
keywords: mboxDefine;mboxdefine;mbox define;mboxUpdate;mbox update;mbox update;at.js;functions;function
description: Gebruik de functies mboxDefine() en mboxUpdate() voor de Adobe [!DNL Target] JavaScript-bibliotheek at.js om een box te definiëren of bij te werken. (om 1.js)
title: Hoe gebruik ik de functies mboxDefine() en mboxUpdate()?
feature: at.js
role: Developer
exl-id: 48261be0-c4d0-4961-9712-ef7e0d2cb1c0
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# mboxDefine() en mboxUpdate() - at.js 1.x

Definieer en werk een box bij in Adobe Target.

>[!NOTE]
>
>Deze functies zijn beschikbaar voor at.js versies 1.*x* alleen. Deze functies zijn vervangen door de release van at.js 2.x. Deze functies retourneren standaardinhoud als deze wordt gebruikt met at.js 2.x.

`mboxDefine()` en `mboxCreate()` zijn gebonden aan HTML DIV-elementen waar het aanbod moet worden weergegeven. Deze HTML DIV-elementen moeten `mboxDefault` klasse. Als deze klasse niet wordt gekoppeld aan de HTML-elementen, ziet u een merkbare flikkering.

## mboxDefine {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Maakt een interne toewijzing tussen een nodeId en een naam van een box, maar voert de aanvraag niet uit. Wordt gebruikt in combinatie met `mboxUpdate()`. Ingebouwd in [!DNL at.js] vooral om de overgang van [!DNL mbox.js] (nu afgekeurd) naar [!DNL at.js].

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Voert het verzoek uit en past het aanbod toe op het element dat door de `nodeId` in de `mboxDefine()`. Kan ook worden gebruikt om een box bij te werken die is gestart door `mboxCreate`. Ingebouwd in [!DNL at.js] vooral om de overgang van [!DNL mbox.js] (nu afgekeurd) naar [!DNL at.js]. `mboxDefine()`/ `mboxUpdate()` kan worden vervangen door [adobe.target.getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank} en [adobe.target.applyOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffer/){target=_blank} met de optie Selector.

## Voorbeeld {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```javascript
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```
