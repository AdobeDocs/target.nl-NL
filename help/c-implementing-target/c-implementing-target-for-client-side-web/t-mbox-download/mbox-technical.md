---
keywords: implementation;mbox.js;dom manipulation library;target.js;visual experience composer;iframe;angular sites;single page applications;single page app;SPA
description: Informatie om uw technisch personeel te helpen de implementatie mbox.js begrijpen en hoe het uw plaats zou kunnen beïnvloeden.
title: Wat doet mbox.js
feature: null
subtopic: Getting Started
topic: Standard
uuid: 5529d620-4a33-479c-871f-18dcd59abb07
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---


# Wat doet mbox.js{#what-mbox-js-does}

Informatie om uw technisch personeel te helpen de implementatie mbox.js begrijpen en hoe het uw plaats zou kunnen beïnvloeden.

Voor de doelstandaard is [!DNL mbox.js] versie 58 of hoger vereist. Zie [!DNL mbox.js]Mbox-implementatie [](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420)voor instructies over het downloaden en bijwerken van bestanden.

Roept voor Target Standard een ander JavaScript-bestand aan [!DNL mbox.js] [!DNL target.js]. [!DNL Target.js] wordt gehost door Adobe en wordt automatisch bijgewerkt door Adobe. Er is niets u te doen om bij te werken [!DNL target.js], en er zijn geen cliënt-specifieke aanpassingen.

[!DNL Target.js] Hiermee maakt u een box met de naam `target-global-mbox` in de `<head>` sectie van de pagina.

[!DNL Target.js] wordt aangeroepen [!DNL mbox.js] door een regel JavaScript-code die aan het [!UICONTROL Extra JavaScript] veld in is toegevoegd [!DNL mbox.js]. De enige manier om onbruikbaar te maken [!DNL target.js] is deze lijn van code niet te omvatten, zo ook onbruikbaar makend [!DNL Target].

[!DNL Target.js] heeft twee functies in [!DNL Target]:

* DOM-manipulatie
* Hiermee schakelt u visuele elementen van de [!UICONTROL Visual Experience Composer]

## DOM-manipulatie {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js] beheert de DOM manipulatiebibliotheek die door Standaard wordt gebruikt. Als u de inhoud van een website wilt weergeven, [!DNL target.js] verwijst u naar [!DNL sizzle.js] (versie 1.10.8-vooraf). [!DNL Sizzle.js] schakelt de HTML-elementkiezers in. Behalve [!DNL sizzle.js]wordt alleen native JavaScript gebruikt. Er is geen query vereist.

Daarnaast wordt het volgende fragment gebruikt voor de opiniepeiling van de DOM:
`https://github.com/dperini/ContentLoaded`

## Target.js en de Visuele Composer van de Ervaring {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

Wanneer u de pagina gebruikt [!UICONTROL Visual Experience Composer] om een handeling in te stellen, wordt de webpagina geopend in een iFrame. Wanneer het iFrame is geladen, verzendt Standard een HTML5 `postMessage` -API-aanroep. [!DNL Target.js] detecteert eventuele `postMessage` aanroepen en neemt de volgende JavaScript-bibliotheken op de website op:

* Voor het genereren van miniaturen: [!DNL https://html2canvas.hertzen.com/]
* Voor interdomeinquery: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css], gebruikt om berichten over iFrames te verzenden. Met deze scripts kan Adobe gegevens tussen de pagina&#39;s verzenden.

## Overwegingen bij hoeksites en toepassingen voor één pagina {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Als u Doel in een Hoekplaats of in om het even welke enig-Pagina Toepassing (SPA) uitvoert, zou u de bibliotheek at.js in plaats van mbox.js moeten gebruiken.

Zie [at.js Implementation](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17)voor meer informatie.
