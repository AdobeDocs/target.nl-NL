---
keywords: vec;visual experience composer; vec;iframe;extension;browser;faq
description: Ontdek waarom sommige websites niet betrouwbaar kunnen worden geopend in de [!UICONTROL Visual Experience Composer] (VEC). Met de browserextensie [!UICONTROL Visual Editing Helper] kunt u websites betrouwbaar laden binnen de VEC.
title: Hoe gebruik ik de extensie [!UICONTROL Visual Editing Helper] ?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: 86139b5971f98091affefd771d9d138e31574727
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# [!UICONTROL Visual Editing Helper] extension

Met de extensie [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] browser voor [!DNL Google Chrome] kunt u websites op betrouwbare wijze laden binnen de VEC ([!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] ), zodat u snel websites kunt ontwerpen en kwaliteitscontrole kunt gebruiken.

>[!IMPORTANT]
>
>* Deze nieuwe uitbreiding vervangt de vorige [ Browser van de Helper van het Doel VEC van het Doel uitbreiding ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). Zie de belangrijke opmerking boven aan dat artikel. Vanwege beveiligingsverbeteringen in Manifest v3 vereist [!DNL Adobe] het downloaden van deze nieuwe extensie om door te gaan met het visueel ontwerpen van uw websites in [!DNL Target] .

## Wijzigingen in de extensie [!UICONTROL Visual Editing Helper] (17 januari 2026)

### **Vaste een kwestie door de nieuwe startkoekjesschoonmaakbeurt experimentele eigenschap in de Helper VEC toe te voegen.**

* Probleem verholpen door een nieuwe experimentele functie voor het opschonen van opstartcookies toe te voegen in de VEC Helper.
* Deze verbetering verbetert de prestaties en betrouwbaarheid door ongepartitioneerde cookies één keer per tab te reinigen wanneer het ontwerpen begint in plaats van continu.
* De eigenschap volgt lusjegeschiedenis om overtollige schoonmaak te verhinderen, en het ontruimt de geschiedenis op lusjedichte zodat schoonmaakbeurt correct gedraagt wanneer een lusje opnieuw wordt geopend.
* Uitgebreide eenheidstests toegevoegd om consistent gedrag te verzekeren.

![ VEC nieuwe opties ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper.png)

## Redenen waarom sommige websites niet betrouwbaar in de VEC kunnen worden geopend

* De website heeft een strikt beveiligingsbeleid.
* De website bevindt zich in een iframe.
* De QA- of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).

De [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] browser uitbreiding voor lost plaats-ladende kwesties op waarvoor de klanten nu op [!DNL Target] [ Verbeterde Composer van de Ervaring ](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) of derdeuitbreidingen, zoals vereisen vertrouwen.

## De voordelen van de extensie [!UICONTROL Visual Editing Helper]

* Alle iframe-opwindende headers, zoals `X-Frame-Options` en `Content-Security-Policy` , worden impliciet verwijderd van de website. Het is niet nodig om ingewikkelde regels te creëren die verplicht zijn.
* Als een webpagina nog niet de bibliotheek [!DNL Target] at.js bevat, kunt u de extensie gebruiken om de bibliotheek te injecteren zodat u de website kunt ontwerpen. U kunt vervolgens activiteiten maken en deze via voorvertoningskoppelingen kwaliteitscontrole laten uitvoeren.

  Gebruikend [ Verbeterde Composer van de Ervaring ](/help/main/administrating-target/visual-experience-composer-set-up.md#eec), injecteert de uitbreiding niet at.js, maar de functionaliteit van het Koekje SameSite is nog aanwezig. Schakel de EEG uit als u om 1.js op de webpagina wilt injecteren.

* [ Mobiele viewports ](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) wordt gesteund zelfs zonder [!UICONTROL Enhanced Experience Composer] (EEG).
* Klanten die [!DNL Target] nog niet eerder hebben gebruikt, kunnen de extensie gebruiken om te experimenteren met [!DNL Target] , zelfs als hun IT-ontwikkelaars [!DNL Target] nog niet hebben geïmplementeerd op hun websites.
* Partners die de websites van veelvoudige klanten en [!DNL Target] rekeningen onderhouden hebben nu één eenvoudig mechanisme om laden VEC te steunen, in plaats van het beheren van veelvoudige regels in derdehulpmiddelen.

## De browserextensie [!UICONTROL Visual Editing Helper] opvragen en installeren

1. Navigeer naar de [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] browserextensie in de Chrome Web Store ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank} .
1. Klik op **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]** .
1. Open VEC in [!DNL Target].
1. Om de uitbreiding te gebruiken, klik het [!UICONTROL Visual Editing Helper] pictogram van de browser uitbreiding ( ![ Visuele het Uitgeven pictogram van de Uitbreiding ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png)) in uw browser van Chrome browser terwijl op de Wijze VEC of QA.

   [!UICONTROL Visual Editing Helper] wordt automatisch ingeschakeld wanneer een website in [!UICONTROL Target] VEC wordt geopend voor het maken van bestanden. De extensie heeft geen voorwaardelijke instellingen. De extensie verwerkt automatisch alle instellingen, inclusief de instellingen voor SameSite-cookies.

   Zie &quot;Hoe beïnvloedt het onlangs aangekondigde Google Chrome SameSite-beleid voor het toepassen van cookies het VEC en EEC?&quot; voor meer informatie over de functie voor het corrigeren van `SameSite=None` -kenmerken in de browser? in [ Problemen van het Oplossen van problemen met betrekking tot de Visuele Composer van de Ervaring en Verbeterde Composer van de Ervaring ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Notities

* Voor [!DNL Target] laadt de extensie de nieuwste versie van at.js die beschikbaar is via de [!DNL Target] UI in [!UICONTROL Administration] > [!UICONTROL Implementation] en at.js downloadt de ontwerpbibliotheken.
* Wanneer het gebruiken van de uitbreiding aan inspringing at.js terwijl in [ Wijze QA ](/help/main/c-activities/c-activity-qa/activity-qa.md), moet u een ander open lusje van Chrome hebben. Dit Chrome-tabblad moet worden geverifieerd door dezelfde [!DNL Adobe Experience Cloud] -organisatie waarin u de activiteit hebt gemaakt.
* De volgende berichten helpen u op de hoogte houden:

   * Als u probeert een website te laden met de VEC die niet kan worden geladen, wordt een bericht weergegeven waarin wordt gesuggereerd dat u de extensie van de [!UICONTROL Visual Editing Helper] browser installeert.
   * Als at.js of alloy.js nog niet op de website wordt uitgevoerd, toont een bericht in VEC die suggereert dat u de uitbreiding installeert.
* Als u probeert gebruikend de nieuwe uitbreiding en dan terug naar de [ oude uitbreiding ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) gaat en [!DNL Target] er niet in slaagt om uw website te laden, alle browser gegevens te ontruimen en de nieuwe uitbreiding onbruikbaar te maken.

## Veelgestelde vragen

### Doet de extensie, indien actief, iets wanneer deze buiten [!DNL Adobe Target] of [!UICONTROL Adobe Journey Optimizer] (AJO) wordt gebruikt?

De extensie wordt alleen geactiveerd wanneer de betreffende website in een iFrame wordt geladen in [!DNL Adobe] -producten ([!DNL Target] , [!DNL AJO] ). Buiten deze flow probeert de extensie geen kopteksten toe te voegen, te verwijderen of te wijzigen en probeert de extensie geen code binnen de website te injecteren.

### Wat doet de extensie wanneer deze actief is in de [!DNL Adobe Target] VEC?

Wanneer een website in een iFrame in [!DNL Adobe] producten ([!DNL Target], [!DNL AJO]) wordt geladen, injecteert de extensie code (die met de extensie is meegeleverd) op de website en downloadt de extensie helperbestanden van de [!DNL Adobe] CDN om visueel ontwerpen mogelijk te maken.
