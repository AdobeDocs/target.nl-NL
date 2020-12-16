---
keywords: implementation;mbox.js;dom manipulation library;target.js;visual experience composer;iframe;angular sites;single page applications;single page app;SPA
description: Informatie om uw technisch personeel te helpen de implementatie mbox.js begrijpen en hoe het uw plaats zou kunnen beïnvloeden.
title: Wat doet mbox.js
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---


# Wat mbox.js doet{#what-mbox-js-does}

Informatie om uw technisch personeel te helpen de implementatie mbox.js begrijpen en hoe het uw plaats zou kunnen beïnvloeden.

Doelstandaard vereist [!DNL mbox.js] versie 58 of hoger. Zie [Mbox-implementatie](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420) voor instructies voor het downloaden en bijwerken van [!DNL mbox.js].

Voor de Standaard van het Doel, [!DNL mbox.js] roept een ander dossier JavaScript, [!DNL target.js]. [!DNL Target.js] wordt gehost door Adobe en wordt automatisch bijgewerkt door Adobe. Er is niets dat u hoeft te doen om [!DNL target.js] bij te werken en er zijn geen klantspecifieke aanpassingen.

[!DNL Target.js] Hiermee maakt u een box met de naam  `target-global-mbox` in de  `<head>` sectie van de pagina.

[!DNL Target.js] wordt aangeroepen  [!DNL mbox.js] door een regel JavaScript-code die aan het  [!UICONTROL Extra JavaScript] veld in  [!DNL mbox.js]. De enige manier om [!DNL target.js] onbruikbaar te maken is deze lijn van code niet te omvatten, zo ook onbruikbaar makend [!DNL Target].

[!DNL Target.js] heeft twee functies in  [!DNL Target]:

* DOM-manipulatie
* Hiermee schakelt u visuele elementen van de [!UICONTROL Visual Experience Composer] in

## DOM-manipulatie {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js] beheert de DOM manipulatiebibliotheek die door Standaard wordt gebruikt. [!DNL target.js] verwijst naar [!DNL sizzle.js] (versie1.10.8-pre) om de inhoud van een website weer te geven. [!DNL Sizzle.js] schakelt de HTML-elementkiezers in. Met uitzondering van [!DNL sizzle.js] wordt alleen native JavaScript gebruikt. Er is geen query vereist.

Daarnaast wordt het volgende fragment gebruikt voor de opiniepeiling van de DOM:
`https://github.com/dperini/ContentLoaded`

## Target.js en de Composer van de Visuele Ervaring {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

Wanneer u [!UICONTROL Visual Experience Composer] gebruikt om een ervaring voor een activiteit op te zetten, wordt uw Web-pagina geopend in een iFrame. Wanneer iFrame is geladen, verzendt Standard een API-aanroep van HTML5 `postMessage`. [!DNL Target.js] detecteert eventuele  `postMessage` aanroepen en neemt de volgende JavaScript-bibliotheken op de website op:

* Voor het genereren van miniaturen: [!DNL https://html2canvas.hertzen.com/]
* Voor interdomeinquery: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css], gebruikt om berichten over iFrames te verzenden. Met deze scripts kan Adobe gegevens tussen de pagina&#39;s verzenden.

## Overwegingen voor hoeksites en toepassingen voor één pagina {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Als u Doel implementeert in een hoeksite of in een toepassing voor één pagina (SPA), moet u de bibliotheek at.js gebruiken in plaats van mbox.js.

Zie [at.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) voor meer informatie.
