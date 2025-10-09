---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Ontdek waarom sommige websites niet betrouwbaar kunnen worden geopend in de [!UICONTROL Visual Experience Composer] (VEC). Met de VEC Helper-browserextensie kunt u websites betrouwbaar laden binnen de VEC.
title: Hoe gebruik ik de Helper Extension [!UICONTROL Visual Experience Composer] (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: 6f4fd14a46f06c1366c02cfaf5a0cee5edbb00c4
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 0%

---

# [!UICONTROL Visual Experience Composer] helperextensie

Met de extensie [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper browser voor [!DNL Google Chrome] kunt u websites betrouwbaar laden binnen de VEC om snel een auteur en QA-webbeleving te maken.

De VEC Helper-browser is een [!DNL Chrome] -extensie. Deze extensie is niet nodig wanneer u [!DNL Mozilla Firefox] gebruikt.

>[!IMPORTANT]
>
>* De oudere [!DNL Target] VEC Helper-extensie die in dit artikel wordt beschreven, is gemaakt met Manifest V2. [!DNL Google] kondigde aan dat het geen extensies meer toestaat die zijn gemaakt met Manifest V2 vanaf juni 2024. Voor meer informatie, zie de [&#x200B; Manifest V2 verklaring van de steunchronologie &#x200B;](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} van [!DNL Google] op *Chrome voor de plaats van Ontwikkelaars*.
>
>* Vanaf juni 2024 wordt in [!DNL Google] begonnen met het uitschakelen van extensies die zijn gemaakt met Manifest V2, inclusief de extensie die in dit onderwerp wordt beschreven. [!DNL Adobe] adviseert dat de klanten zich aan de nieuwere [&#x200B; Visuele het Uitgeven uitbreiding van de Helper &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) zo spoedig mogelijk bewegen.

## Redenen waarom sommige websites niet betrouwbaar in de VEC kunnen worden geopend

* De website heeft een strikt beveiligingsbeleid.
* De website bevindt zich in een iframe.
* De bibliotheek at.js is nog niet geïmplementeerd op de website.
* De QA- of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).
* Er zijn sommige huidige beperkingen wanneer het proberen om VEC te gebruiken om een website te openen die [&#x200B; de Werknemers van de Dienst &#x200B;](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank} (SW) gebruikt.

SW is een Webtechnologie die kan worden gebruikt om verzoeken voor het domein te onderscheppen zij op door een Web-pagina worden geïnstalleerd. De SBW heeft het paginabezoek overleefd en activeert zichzelf bij volgende bezoeken. SW beslist welke verzoeken door gaan en welke degenen in plaats daarvan van een geheim voorgeheugen worden onderschept en worden gediend.

SW kan het in het voorgeheugen onderbrengen; kan de Web-pagina zelf, statische middelen zoals JS, CSS, IMG, AJAX verzoeken, hun inhoud, en hun antwoordkopballen, met inbegrip van degenen in cache plaatsen die onze [&#x200B; uitbreiding van de Hulp van het Doel VEC &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) probeert te verwijderen, zoals x-kader-Opties: SAMEORIGIN, CSP (Content-Security-Policy), of reeks-Cookie.

Jammer genoeg, ontvangen de uitbreiding APIs van Chrome die Webverzoeken onderscheppen niet de verzoeken die werden onderschept en door SW behandeld. Daarom kan de uitbreiding niet de kopballen en de koekjes bevestigen als het Web-pagina verzoek van een geheime voorgeheugen door een SW werd gediend omdat de Web-pagina niet binnen VEC wegens de x-Kader-Opties of CSP kopballen zal laden die ook in het voorgeheugen werden opgenomen.

Als mogelijke oplossing kunt u de Workers van de Dienst van de Hulpmiddelen van de Ontwikkelaar van Chrome onbruikbaar maken > het lusje van de Toepassing, dan om &quot;Bypass voor netwerk&quot;checkbox onder de sectie van de Werknemers van de Dienst toe te laten.

* U gebruikt Google Chrome 80+ met het verbeterde beleid voor het uitvoeren van cookies van SameSite. Voor meer informatie, zie [&#x200B; Hoe beïnvloedt onlangs aangekondigde Google Chrome SameSite het handhavingsbeleid van het koekjesbeleid VEC en EEC &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

De browser van de Helper VEC uitbreiding voor Chrome lost plaats-ladende kwesties op waarvoor de klanten nu op [!DNL Target] [&#x200B; Verbeterde Composer van de Ervaring &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) of derdeuitbreidingen, zoals vereisen vertrouwen.

## Voordelen van het gebruik van de extensie VEC Helper

* Alle iFrame-opbouwheaders, zoals X-Frame-Options en Content-Security-Policy, worden impliciet verwijderd van de website. Het is niet langer nodig om ingewikkelde regels voor verplichte naleving op te stellen.
* Als een webpagina nog niet de JavaScript-bibliotheek [!DNL Target] at.js bevat, kunt u de extensie gebruiken om de bibliotheek te injecteren zodat u de website kunt ontwerpen. U kunt vervolgens activiteiten maken en deze via voorvertoningskoppelingen kwaliteitscontrole laten uitvoeren.

  Let op: met de Enhanced Experience Composer (EEC) injecteert de extensie niet in at.js, maar is de functionaliteit SameSite Cookie nog steeds aanwezig. Schakel de EEG uit als u om 1.js op de webpagina wilt injecteren.

* [&#x200B; Mobiele viewports &#x200B;](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) wordt gesteund zelfs zonder [!UICONTROL Enhanced Experience Composer] (EEG).
* Klanten die [!DNL Target] nog niet eerder hebben gebruikt, kunnen de extensie gebruiken om te experimenteren met [!DNL Target] , zelfs als hun IT-ontwikkelaars [!DNL Target] nog niet hebben geïmplementeerd op hun websites.
* Partners die de websites van veelvoudige klanten en [!DNL Target] rekeningen onderhouden hebben nu één eenvoudig mechanisme om laden VEC te steunen, in plaats van het beheren van veelvoudige regels in derdehulpmiddelen.

## VEC Helper-browserextensie opvragen en installeren

1. Navigeer aan de [&#x200B; browser van de Helper van Adobe Target VEC uitbreiding in de Opslag van het Web van Chrome &#x200B;](https://chromewebstore.google.com/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca).
1. Klik op **[!UICONTROL Add to Chrome > Add Extension]**.
1. Open VEC in [!DNL Target].
1. Om de uitbreiding te gebruiken, klik het VEC Helper browser uitbreidingspictogram ( ![&#x200B; pictogram van de Helper VEC &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)) in uw browser van Chrome terwijl op de Wijze van VEC of [&#x200B; QA &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa.md).
1. (Voorwaardelijk) Schuif de schakeloptie **[!UICONTROL Inject Target Libraries]** naar de positie &quot;aan&quot; als de webpagina nog niet de JavaScript-bibliotheek [!DNL Target] at.js bevat.

   In de volgende afbeelding ziet u de VEC Helper waarvoor de instelling [!UICONTROL Inject Target Libraries] is ingeschakeld:

   ![&#x200B; VEC helper 1 &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   In de volgende afbeelding ziet u hoe de VEC Helper u vraagt of u [!DNL Target] bibliotheken op de pagina wilt injecteren om ontwerpen mogelijk te maken:

   ![&#x200B; VEC helper 2 &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Voorwaardelijk) Schuif de schakeloptie **[!UICONTROL Cookies]** naar de positie &quot;Aan&quot; om automatisch de correctie voor de `SameSite=None` -kenmerkbrowser toe te voegen.

   ![&#x200B; de knevel van Cookies in de VEC helperuitbreiding &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Zie &quot;Hoe beïnvloedt het onlangs aangekondigde Google Chrome SameSite-beleid voor het toepassen van cookies het VEC en EEC?&quot; voor meer informatie over de functie voor het corrigeren van `SameSite=None` -kenmerken in de browser? in [&#x200B; Problemen van het Oplossen van problemen met betrekking tot de Visuele Composer van de Ervaring en Verbeterde Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Notities

* De markering [!UICONTROL Inject Target libraries] in de extensie is standaard UIT. U kunt deze markering inschakelen als u de VEC wilt gebruiken voor een site die nog niet is geïmplementeerd voor [!DNL Target] .

  Deze markering is een globale instelling. De vlag wordt toegelaten of gehandicapt voor alle websites die in VEC worden geopend. Als u deze markering bijvoorbeeld instelt op &quot;on&quot; en een website opent die al is geïmplementeerd met at.js, ontvangt u een bericht met de melding dat at.js al is geladen. Adobe verwacht dat de meeste klanten at.js al hebben geïmplementeerd op hun pagina&#39;s en de standaardinstelling van &quot;off&quot; gebruiken.

* De extensie laadt de nieuwste versie van at.js die beschikbaar is in de map [!DNL Target UI] in [!UICONTROL Administration > Implementation] .
* Wanneer het gebruiken van de uitbreiding aan inspringing at.js terwijl in [&#x200B; Wijze QA &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa.md), moet u een ander open lusje van Chrome hebben. Dit Chrome-tabblad moet worden geverifieerd bij dezelfde [!DNL Adobe Experience Cloud] -organisatie waarin u de activiteit hebt gemaakt.
* De volgende berichten helpen u op de hoogte houden:

   * Als u probeert om een website te laden die VEC gebruikt die er niet in slaagt te laden, toont een bericht die suggereert dat u de VEC Helper browser uitbreiding installeert.
   * Als at.js nog niet op de website wordt uitgevoerd, toont een bericht in VEC die dat u de uitbreiding installeert.
   * Als de extensie is ingeschakeld en de laadbewerking uitvoert, worden berichten weergegeven wanneer de extensie de bibliotheek at.js injecteert (indien nodig) of wanneer de website betrouwbaar wordt geopend in de VEC.
