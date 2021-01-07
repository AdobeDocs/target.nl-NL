---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Informatie om de Adobe Target Visual Experience Composer (VEC) te gebruiken Helper browser uitbreiding om websites betrouwbaar binnen VEC te laden om snel auteur en QA ervaart te schrijven.
title: Helperextensie Adobe Target Visual Experience Composer (VEC)
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---


# Helpextensie Visual Experience Composer

Met de [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper browser extension for Google Chrome kunt u websites op betrouwbare wijze laden binnen de VEC, zodat u snel websites kunt ontwerpen en kwaliteitscontrole kunt gebruiken.

>[!NOTE]
>
>De browser VEC Helper is een Chrome-extensie. Deze extensie is niet nodig wanneer u Mozilla Firefox gebruikt.

## Redenen waarom sommige websites niet betrouwbaar in de VEC kunnen worden geopend

* De website heeft een strikt beveiligingsbeleid.
* De website bevindt zich in een iframe.
* De bibliotheek at.js is nog niet geïmplementeerd op de website.
* De QA- en/of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).
* U gebruikt Google Chrome 80+ met het verbeterde beleid voor het toepassen van cookies op SameSite. Zie [Hoe beïnvloedt het onlangs aangekondigde beleid van Google Chrome SameSite cookie handhaving VEC en EEC](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

Met de VEC Helper-browserextensie voor Chrome worden problemen met het laden van de site opgelost waarvoor klanten nu vertrouwen op de [!DNL Target] [Enhanced Experience Composer](/help/administrating-target/visual-experience-composer-set-up.md#eec) of externe extensies, zoals Request.

## Voordelen van het gebruik van de extensie VEC Helper

* Alle iFrame-opbouwheaders, zoals X-Frame-Options en Content-Security-Policy, worden impliciet verwijderd van de website. Het is niet langer nodig om hiervoor ingewikkelde voorschriften in te voeren.
* Als een webpagina nog niet de JavaScript-bibliotheek [!DNL Target] at.js bevat, kunt u de extensie gebruiken om de bibliotheek te injecteren zodat u de website kunt ontwerpen. U kunt vervolgens activiteiten maken en deze via voorvertoningskoppelingen kwaliteitscontrole laten uitvoeren.

   Let op: bij gebruik van de Enhanced Experience Composer (EEC) injecteert de extensie niet in at.js, maar is de functionaliteit SameSite Cookie nog steeds aanwezig. Schakel de EEG uit als u om 1.js op de webpagina wilt injecteren.

* [Mobiele ](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) viewers worden ook zonder  [!UICONTROL Enhanced Experience Composer] (EEG) ondersteund.
* Klanten die nog niet bekend zijn met [!DNL Target] kunnen de extensie gebruiken om te experimenteren met [!DNL Target], zelfs als hun IT-ontwikkelaars [!DNL Target] nog niet op hun websites hebben geïmplementeerd.
* Partners die de websites van veelvoudige klanten en [!DNL Target] rekeningen onderhouden hebben nu één eenvoudig mechanisme om laden VEC te steunen, in plaats van het beheren van veelvoudige regels in derdehulpmiddelen.

## VEC Helper-browserextensie opvragen en installeren

1. Navigeer naar de [Adobe Target VEC Helper browser extensie in de Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klik op **[!UICONTROL Add to Chrome > Add Extension]**.
1. Open VEC in [!DNL Target].
1. Als u de extensie wilt gebruiken, klikt u op het pictogram voor VEC Helper-browserextensie ( ![VEC Helper icon](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png) ) op de werkbalk van de Chrome-browser terwijl u zich in de VEC of [QA-modus](/help/c-activities/c-activity-qa/activity-qa.md) bevindt.
1. (Voorwaardelijk) Schuif de **[!UICONTROL Inject Target Libraries]**-schakeloptie naar de positie &quot;aan&quot; als de webpagina nog niet de JavaScript-bibliotheek [!DNL Target] at.js bevat.

   De volgende illustratie toont de Helper VEC met [!UICONTROL Inject Target Libraries] toegelaten plaatsen:

   ![VEC-helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   In de volgende afbeelding ziet u hoe de VEC Helper u vraagt of u [!DNL Target] bibliotheken op de pagina wilt injecteren om ontwerpen mogelijk te maken:

   ![VEC-helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Voorwaardelijk) Schuif **[!UICONTROL Cookies]** knevel aan &quot;op&quot;positie om automatisch de het attributenbrowser van SameSite=None moeilijke situatie toe te voegen, dan specificeer de koekjesnaam en het domein.

   ![Kookies in de VEC helperuitbreiding](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   De volgende koppelingen bieden aanvullende informatie:

   * Zie &quot;Hoe beïnvloedt het onlangs aangekondigde beleid van Google Chrome SameSite cookie executie VEC en EEC&quot; voor meer informatie over de browser fix van het kenmerk SameSite=None?&quot; in [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

   * De cookienaam is &quot;mbox&quot;en het koekjesdomein is de tweede en hoogste niveaus van de domeinen waarvan u mbox dient. Omdat het van het domein van uw bedrijf wordt gediend, is het koekje een eerste partijkoekje. Voorbeeld: `mycompany.com`. Voor meer informatie, zie [Adobe Target Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html) in *de Gids van de Gebruiker van de Interface van de Experience Cloud*.

## Notities

* Uw implementatie moet de [!DNL Target] at.js-bibliotheek gebruiken. U kunt geen mbox.js-implementatie gebruiken met de extensie.
* De markering [!UICONTROL Inject Target libraries] in de extensie is standaard UIT. U kunt deze markering inschakelen als u de VEC wilt gebruiken voor een site die nog niet is geïmplementeerd voor [!DNL Target].

   Houd er rekening mee dat deze markering een algemene instelling is. De vlag wordt toegelaten of gehandicapt voor alle websites die in VEC worden geopend. Als u deze markering bijvoorbeeld instelt op &quot;on&quot; en een website opent die al is geïmplementeerd met at.js, ontvangt u een bericht met de melding dat at.js al is geladen. We verwachten dat de meeste klanten at.js al hebben geïmplementeerd op hun pagina&#39;s en de standaardinstelling van &#39;off&#39; gebruiken.

* De extensie laadt de nieuwste versie van at.js die beschikbaar is in [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* Wanneer u de extensie gebruikt om te injecteren in [QA-modus](/help/c-activities/c-activity-qa/activity-qa.md), moet u een ander Chrome-tabblad openen. Dit tabblad Chrome moet worden geverifieerd bij dezelfde [!DNL Adobe Experience Cloud] Organisatie waarin u de activiteit hebt gemaakt.
* De volgende berichten helpen u op de hoogte houden:

   * Als u probeert om een website te laden die VEC gebruikt die er niet in slaagt te laden, toont een bericht die suggereert dat u de VEC Helper browser uitbreiding installeert.
   * Als at.js nog niet op de website wordt uitgevoerd, toont een bericht in VEC die dat u de uitbreiding installeert.
   * Als de extensie is ingeschakeld en de laadbewerking uitvoert, worden berichten weergegeven wanneer de extensie de bibliotheek at.js injecteert (indien nodig) of wanneer de website betrouwbaar wordt geopend in de VEC.

