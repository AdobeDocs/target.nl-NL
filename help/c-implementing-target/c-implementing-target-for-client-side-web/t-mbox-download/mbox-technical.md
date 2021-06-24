---
keywords: implementatie;mbox.js;dom-manipulatiebibliotheek;target.js;visual experience composer;iframe;angular sites;single page-toepassingen;single page-app;SPA
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Wat doet de bibliotheek  [!DNL Target] mbox.js?
feature: at.js
role: Developer
exl-id: 62f0cbd2-17f0-43f4-98d3-ea39f314525e
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Wat doet mbox.js

Informatie om uw technisch personeel te helpen de implementatie mbox.js begrijpen en hoe het uw plaats zou kunnen beïnvloeden.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## DOM-manipulatie {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js] beheert de DOM manipulatiebibliotheek die door Standaard wordt gebruikt. [!DNL target.js] verwijst naar [!DNL sizzle.js] (versie1.10.8-pre) om de inhoud van een website weer te geven. [!DNL Sizzle.js] schakelt de HTML-elementkiezers in. Met uitzondering van [!DNL sizzle.js] wordt alleen native JavaScript gebruikt. Er is geen query vereist.

Daarnaast wordt het volgende fragment gebruikt voor de opiniepeiling van de DOM:
`https://github.com/dperini/ContentLoaded`

## Target.js en de Visuele Composer van de Ervaring {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

Wanneer u [!UICONTROL Visual Experience Composer] gebruikt om een ervaring voor een activiteit op te zetten, wordt uw Web-pagina geopend in een iFrame. Wanneer iFrame is geladen, verzendt Standard een API-aanroep van HTML5 `postMessage`. [!DNL Target.js] detecteert eventuele  `postMessage` aanroepen en neemt de volgende JavaScript-bibliotheken op de website op:

* Voor het genereren van miniaturen: [!DNL https://html2canvas.hertzen.com/]
* Voor interdomeinquery: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css], gebruikt om berichten over iFrames te verzenden. Met deze scripts kan Adobe gegevens tussen de pagina&#39;s verzenden.

## Overwegingen voor Angular-sites en Single-Page-toepassingen {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Als u Doel implementeert in een Angular-site of in een toepassing voor één pagina (SPA), moet u de bibliotheek at.js gebruiken in plaats van mbox.js.
