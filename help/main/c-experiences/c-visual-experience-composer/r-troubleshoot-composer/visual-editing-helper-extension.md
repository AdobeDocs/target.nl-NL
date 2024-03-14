---
keywords: vec;visual experience composer; vec;iframe;extension;browser;faq
description: Ontdek waarom sommige websites niet betrouwbaar kunnen worden geopend in de [!UICONTROL Visual Experience Composer] (VEC). De [!UICONTROL Visual Editing Helper] Met browserextensie kunt u websites betrouwbaar laden binnen de VEC.
title: Hoe gebruik ik de [!UICONTROL Visual Editing Helper] Uitbreiding?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: 5df9ba6eb249dfc690279177ecb5936aaefa7bdd
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# [!UICONTROL Visual Editing Helper] extension

De [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] browserextensie voor [!DNL Google Chrome] Hiermee kunt u websites betrouwbaar laden binnen de [!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) voor een snelle ervaring met auteurs en QA-websites.

>[!IMPORTANT]
>
>Deze nieuwe extensie vervangt de vorige [Doel VEC Helper-browserextensie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). Zie de belangrijke opmerking boven aan dat artikel.

## Redenen waarom sommige websites niet betrouwbaar in de VEC kunnen worden geopend

* De website heeft een strikt beveiligingsbeleid.
* De website bevindt zich in een iframe.
* De QA- of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).

De [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] browserextensie voor het oplossen van problemen bij het laden van sites waarop klanten nu vertrouwen op de [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) of extensies van derden, zoals &quot;opzichtig&quot;.

## De voordelen van het gebruik van de [!UICONTROL Visual Editing Helper] extension

* Alle iframe-opwindende headers, zoals `X-Frame-Options` en `Content-Security-Policy`, impliciet uit de website worden verwijderd. Het is niet nodig om ingewikkelde regels te creëren die verplicht zijn.
* Als een webpagina nog geen [!DNL Target] in de bibliotheek at.js kunt u de extensie gebruiken om de bibliotheek te injecteren, zodat u de website kunt ontwerpen. U kunt vervolgens activiteiten maken en deze via voorvertoningskoppelingen kwaliteitscontrole laten uitvoeren.

  Met de [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec), injecteert de extensie niet in at.js, maar is de functionaliteit SameSite Cookie nog steeds aanwezig. Schakel de EEG uit als u om 1.js op de webpagina wilt injecteren.

* [Mobiele viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) worden zelfs zonder de [!UICONTROL Enhanced Experience Composer] (EEG).
* Klanten die niet bekend zijn met [!DNL Target] kan de extensie gebruiken om met [!DNL Target] zelfs als hun ontwikkelaars van IT nog niet ten uitvoer hebben gelegd [!DNL Target] op hun websites.
* Partners die de websites van veelvoudige klanten onderhouden en [!DNL Target] de rekeningen hebben nu één eenvoudig mechanisme om laden VEC te steunen, in plaats van het beheren van veelvoudige regels in derdehulpmiddelen.

## Verkrijg en installeer [!UICONTROL Visual Editing Helper] browserextensie

1. Ga naar de [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] browserextensie in de Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Klikken **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.
1. VEC openen in [!DNL Target].
1. Klik op de knop [!UICONTROL Visual Editing Helper] browserextensiepictogram ( ![Pictogram Visuele bewerkingsextensie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) in de werkbalk van uw Chrome-browser in de modus VEC of QA.

   De [!UICONTROL Visual Editing Helper] wordt automatisch ingeschakeld wanneer een website wordt geopend in het dialoogvenster [!UICONTROL Target] VEC aan macht authoring. De extensie heeft geen voorwaardelijke instellingen. De extensie verwerkt automatisch alle instellingen, inclusief de instellingen voor SameSite-cookies.

   Voor meer informatie over de `SameSite=None` kenmerkenbrowser moeilijke situatie, zie &quot;hoe beïnvloedt het onlangs aangekondigde de koekjeshandhavingsbeleid van Google Chrome SameSite VEC en EEC?&quot; in [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Notities

* Voor [!DNL Target], laadt de extensie de nieuwste versie van at.js die beschikbaar is via de [!DNL Target] UI in [!UICONTROL Administration] > [!UICONTROL Implementation] en at.js downloadt de ontwerpbibliotheken.
* Wanneer u de extensie gebruikt om te injecteren op .js tijdens het innemen van [QA-modus](/help/main/c-activities/c-activity-qa/activity-qa.md), moet er een ander Chrome-tabblad zijn geopend. Dit tabblad Chrome moet op dezelfde manier worden geverifieerd [!DNL Adobe Experience Cloud] organisatie waarin u de activiteit hebt gemaakt.
* De volgende berichten helpen u op de hoogte houden:

   * Als u probeert een website te laden met de VEC die niet kan worden geladen, wordt een bericht weergegeven waarin wordt gesuggereerd dat u de [!UICONTROL Visual Editing Helper] browserextensie.
   * Als at.js of alloy.js nog niet op de website wordt uitgevoerd, toont een bericht in VEC die suggereert dat u de uitbreiding installeert.
* Als u de nieuwe extensie probeert te gebruiken, gaat u terug naar de [oude extensie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) en [!DNL Target] kan uw website niet laden, alle browsergegevens wissen en de nieuwe extensie uitschakelen.

## Veelgestelde vragen

### Doet de uitbreiding, wanneer actief, om het even wat wanneer gebruikt buiten [!DNL Adobe Target] of [!UICONTROL Adobe Journey Optimizer] (AJO)?

De extensie wordt alleen geactiveerd wanneer de betreffende website is geladen in een iFrame in [!DNL Adobe] producten ([!DNL Target], [!DNL AJO]). Buiten deze flow probeert de extensie geen kopteksten toe te voegen, te verwijderen of te wijzigen en probeert de extensie geen code binnen de website te injecteren.

### Wat doet de extensie als deze actief is in het dialoogvenster [!DNL Adobe Target] VEC?

Wanneer een website in een iFrame wordt geladen in [!DNL Adobe] producten ([!DNL Target], [!DNL AJO]), de extensie injecteert code (gebundeld met de extensie) op de website en downloadt hulpbestanden van de [!DNL Adobe] CDN om visueel ontwerpen toe te laten.
