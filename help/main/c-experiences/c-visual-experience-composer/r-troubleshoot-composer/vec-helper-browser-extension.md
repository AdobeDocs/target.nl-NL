---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Ontdek waarom sommige websites niet betrouwbaar kunnen worden geopend in de [!UICONTROL Visual Experience Composer] (VEC). Met de VEC Helper-browserextensie kunt u websites betrouwbaar laden binnen de VEC.
title: Hoe gebruik ik de [!UICONTROL Visual Experience Composer] (VEC) Helper Extension?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: 97b1d78de2d6ba33c1dd72494edcfc97fc3ba7e6
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 0%

---

# [!UICONTROL Visual Experience Composer] helperuitbreiding

De [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper browser extension for [!DNL Google Chrome] Hiermee kunt u websites betrouwbaar laden binnen de VEC zodat u snel een product kunt ontwerpen en een kwaliteitscontrole kunt gebruiken.

De VEC Helper-browser is een [!DNL Chrome] extensie. Deze extensie is niet nodig wanneer u [!DNL Mozilla Firefox].

>[!IMPORTANT]
>
>De nalatenschap [!DNL Target] De in dit artikel gedocumenteerde VEC Helper-extensie is gemaakt met Manifest V2. [!DNL Google] heeft aangekondigd dat het geen extensies meer zal toestaan die zijn gemaakt met Manifest V2 vanaf juni 2024. Zie de klasse [Duidelijke aankondiging van tijdlijn voor V2-ondersteuning](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} van [!DNL Google] op de *Chrome voor ontwikkelaars* site.
>
>Vanaf juni 2024 [!DNL Google] zal beginnen onbruikbaar makend uitbreidingen die gebruikend Manifest V2 worden gecreeerd, met inbegrip van de uitbreiding die in dit onderwerp wordt gedocumenteerd. [!DNL Adobe] raadt klanten aan naar de nieuwere [De extensie Visuele bewerkingshulp](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) zo spoedig mogelijk.

## Redenen waarom sommige websites niet betrouwbaar in de VEC kunnen worden geopend

* De website heeft een strikt beveiligingsbeleid.
* De website bevindt zich in een iframe.
* De bibliotheek at.js is nog niet geïmplementeerd op de website.
* De QA- of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).
* Er zijn momenteel enkele beperkingen wanneer u probeert de VEC te gebruiken om een website te openen die [Dienstverleners](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank} (SW).

SW is een Webtechnologie die kan worden gebruikt om verzoeken voor het domein te onderscheppen zij op door een Web-pagina worden geïnstalleerd. De SBW heeft het paginabezoek overleefd en activeert zichzelf bij volgende bezoeken. SW beslist welke verzoeken door gaan en welke degenen in plaats daarvan van een geheim voorgeheugen worden onderschept en worden gediend.

De software kan de caching controleren; kan de Web-pagina zelf, statische middelen zoals JS, CSS, IMG, AJAX verzoeken, hun inhoud, en hun antwoordkopballen, met inbegrip van die in het voorgeheugen onderbrengen die onze [Doel VEC Helper-extensie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) probeert om, als x-kader-Opties te verwijderen: SAMEORIGIN, CSP (Content-Security-Policy), of reeks-Koekje.

Jammer genoeg, ontvangen de uitbreiding APIs van Chrome die Webverzoeken onderscheppen niet de verzoeken die werden onderschept en door SW behandeld. Daarom kan de uitbreiding niet de kopballen en de koekjes bevestigen als het Web-pagina verzoek van een geheime voorgeheugen door een SW werd gediend omdat de Web-pagina niet binnen VEC wegens de x-Kader-Opties of CSP kopballen zal laden die ook in het voorgeheugen werden opgenomen.

Als potentiële oplossing, kunt u de Werknemers van de Dienst van de Hulpmiddelen van de Ontwikkelaar van Chrome onbruikbaar maken > het lusje van de Toepassing, dan om &quot;Bypass voor netwerk&quot;checkbox onder de sectie van de Werknemers van de Dienst toe te laten.

* U gebruikt Google Chrome 80+ met het verbeterde beleid voor het uitvoeren van cookies van SameSite. Zie voor meer informatie [Hoe beïnvloedt het onlangs aangekondigde Google Chrome SameSite cookie handhavingsbeleid de VEC en EEC](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

Met de VEC Helper-browserextensie voor Chrome worden de problemen opgelost die gebruikers momenteel ondervinden bij het laden van sites [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) of extensies van derden, zoals &quot;opzichtig&quot;.

## Voordelen van het gebruik van de extensie VEC Helper

* Alle iFrame-opbouwheaders, zoals X-Frame-Options en Content-Security-Policy, worden impliciet verwijderd van de website. Het is niet langer nodig om ingewikkelde regels voor verplichte naleving op te stellen.
* Als een webpagina nog geen [!DNL Target] in de JavaScript-bibliotheek at.js kunt u de extensie gebruiken om de bibliotheek te injecteren, zodat u de website kunt ontwerpen. U kunt vervolgens activiteiten maken en deze via voorvertoningskoppelingen kwaliteitscontrole laten uitvoeren.

  Let op: met de Enhanced Experience Composer (EEC) injecteert de extensie niet in at.js, maar is de functionaliteit SameSite Cookie nog steeds aanwezig. Schakel de EEG uit als u om 1.js op de webpagina wilt injecteren.

* [Mobiele viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) worden zelfs zonder de [!UICONTROL Enhanced Experience Composer] (EEG).
* Klanten die niet bekend zijn met [!DNL Target] kan de extensie gebruiken om met [!DNL Target] zelfs als hun ontwikkelaars van IT nog niet ten uitvoer hebben gelegd [!DNL Target] op hun websites.
* Partners die de websites van veelvoudige klanten onderhouden en [!DNL Target] de rekeningen hebben nu één eenvoudig mechanisme om laden VEC te steunen, in plaats van het beheren van veelvoudige regels in derdehulpmiddelen.

## VEC Helper-browserextensie opvragen en installeren

1. Ga naar de [Adobe Target VEC Helper-browserextensie in de Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klik op **[!UICONTROL Add to Chrome > Add Extension]**.
1. VEC openen in [!DNL Target].
1. Als u de extensie wilt gebruiken, klikt u op het pictogram voor VEC Helper-browserextensie ( ![VEC Helper-pictogram](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png) ) in de werkbalk van uw Chrome-browser wanneer u zich in de VEC of [QA-modus](/help/main/c-activities/c-activity-qa/activity-qa.md).
1. (Voorwaardelijk) Schuif de **[!UICONTROL Inject Target Libraries]** Schakel over naar de positie &quot;Aan&quot; als de webpagina nog niet de [!DNL Target] at.js JavaScript-bibliotheek.

   De volgende afbeelding toont de VEC Helper met de [!UICONTROL Inject Target Libraries] instelling ingeschakeld:

   ![VEC-helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   De volgende afbeelding toont de VEC Helper die u vraagt of u het wilt injecteren [!DNL Target] bibliotheken op de pagina om ontwerpen in te schakelen:

   ![VEC-helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Voorwaardelijk) Schuif de **[!UICONTROL Cookies]** schakelen naar de positie &quot;aan&quot; om automatisch de `SameSite=None` corrigeren van de kenmerkbrowser.

   ![Kookies in de VEC helperuitbreiding](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Voor meer informatie over de `SameSite=None` kenmerkenbrowser moeilijke situatie, zie &quot;hoe beïnvloedt het onlangs aangekondigde de koekjeshandhavingsbeleid van Google Chrome SameSite VEC en EEC?&quot; in [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Notities

* De [!UICONTROL Inject Target libraries] markering in de extensie is standaard UIT. U kunt deze markering inschakelen als u de VEC wilt gebruiken voor een site waarvoor nog geen implementatie is uitgevoerd [!DNL Target].

  Deze markering is een globale instelling. De vlag wordt toegelaten of gehandicapt voor alle websites die in VEC worden geopend. Als u deze markering bijvoorbeeld instelt op &quot;on&quot; en een website opent die al is geïmplementeerd met at.js, ontvangt u een bericht met de melding dat at.js al is geladen. Adobe verwacht dat de meeste klanten at.js al hebben geïmplementeerd op hun pagina&#39;s en de standaardinstelling van &quot;off.&quot; gebruiken.

* De extensie laadt de nieuwste versie van at.js die beschikbaar is via de [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* Wanneer u de extensie gebruikt om te injecteren op .js tijdens het innemen van [QA-modus](/help/main/c-activities/c-activity-qa/activity-qa.md), moet er een ander Chrome-tabblad zijn geopend. Dit tabblad Chrome moet op dezelfde manier worden geverifieerd [!DNL Adobe Experience Cloud] Organisatie waarin u de activiteit hebt gemaakt.
* De volgende berichten helpen u op de hoogte houden:

   * Als u probeert om een website te laden die VEC gebruikt die er niet in slaagt te laden, toont een bericht die suggereert dat u de VEC Helper browser uitbreiding installeert.
   * Als at.js nog niet op de website wordt uitgevoerd, toont een bericht in VEC die dat u de uitbreiding installeert.
   * Als de extensie is ingeschakeld en de laadbewerking uitvoert, worden berichten weergegeven wanneer de extensie de bibliotheek at.js injecteert (indien nodig) of wanneer de website betrouwbaar wordt geopend in de VEC.
