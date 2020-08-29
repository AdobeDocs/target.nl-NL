---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Informatie om de Adobe Target Visual Experience Composer (VEC) te gebruiken Helper browser uitbreiding om websites betrouwbaar binnen VEC te laden om snel auteur en QA ervaart te schrijven.
title: Helperextensie Adobe Target Visual Experience Composer (VEC)
feature: vec
topic: Standard
translation-type: tm+mt
source-git-commit: c77561696c35a5890c10591fc1014d812485f0f8
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---


# Helpextensie Visual Experience Composer

Met de [!DNL Adobe Target] Visual Experience Composer (VEC) Helper browser extension for Google Chrome kunt u websites betrouwbaar laden binnen de VEC om snel een auteur en QA webbeleving te maken.

Redenen waarom sommige websites niet betrouwbaar in de VEC kunnen worden geopend:

* De website heeft een strikt beveiligingsbeleid.
* De website bevindt zich in een iframe.
* De bibliotheek at.js is nog niet geïmplementeerd op de website.
* De QA- en/of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).
* U gebruikt Google Chrome 80+ met het verbeterde beleid voor het toepassen van cookies op SameSite. Zie [Hoe beïnvloedt het onlangs aangekondigde beleid van Google Chrome SameSite voor de handhaving van cookies de VEC en EEC](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

Met de VEC Helper-browserextensie voor Chrome worden de problemen opgelost die door klanten worden veroorzaakt en die nu door de extensie [!DNL Target] [!UICONTROL Enhanced Experience Composer] of door derden worden veroorzaakt, zoals &quot;opzichtig&quot;.

Voordelen van het gebruik van de extensie VEC Helper:

* Alle iFrame-opbouwheaders, zoals X-Frame-Options en Content-Security-Policy, worden impliciet verwijderd van de website. Het is niet langer nodig om hiervoor ingewikkelde voorschriften in te voeren.
* Als een webpagina nog niet de JavaScript-bibliotheek [!DNL Target] at.js bevat, kunt u de extensie gebruiken om de bibliotheek te injecteren zodat u de website kunt ontwerpen. U kunt vervolgens activiteiten maken en deze via voorvertoningskoppelingen kwaliteitscontrole laten uitvoeren.
* Mobiele Viewports worden ondersteund, zelfs zonder [!UICONTROL Enhanced Experience Composer] (EEG).
* Klanten die nog niet eerder [!DNL Target] zijn, kunnen de extensie gebruiken om te experimenteren met [!DNL Target] zelfs als hun IT-ontwikkelaars deze nog niet [!DNL Target] op hun websites hebben geïmplementeerd.
* Partners die de websites en de rekeningen van veelvoudige klanten onderhouden hebben nu één eenvoudig mechanisme om het laden VEC te steunen, in plaats van het beheren van veelvoudige regels in derdehulpmiddelen. [!DNL Target]

## VEC Helper-browserextensie opvragen en installeren

1. Navigeer naar de [Adobe Target VEC Helper browser extensie in de Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klik op [!UICONTROL Add to Chrome > Add Extension].
1. Als u de extensie wilt gebruiken, klikt u op het pictogram voor VEC Helper-browserextensie ( ![pictogram](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png) VEC Helper ) op de werkbalk van de Chrome-browser terwijl u in de VEC- of [QA-modus](/help/c-activities/c-activity-qa/activity-qa.md)werkt.

In het volgende voorbeeld wordt de VEC Helper weergegeven met de [!UICONTROL Inject Target Libraries] instelling ingeschakeld:

![VEC-helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

In de volgende afbeelding ziet u hoe de VEC Helper u vraagt of u [!DNL Target] bibliotheken op de pagina wilt injecteren om ontwerpen mogelijk te maken:

![VEC-helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

## Notities

* Uw implementatie moet de bibliotheek [!DNL Target] at.js gebruiken. U kunt geen mbox.js-implementatie gebruiken met de extensie.
* De [!UICONTROL Inject Target libraries] markering in de extensie is standaard UIT. U kunt deze markering inschakelen als u de VEC wilt gebruiken voor een site waarvoor nog geen implementatie is uitgevoerd [!DNL Target].

   Houd er rekening mee dat deze markering een algemene instelling is. De vlag wordt toegelaten of gehandicapt voor alle websites die in VEC worden geopend. Als u deze markering bijvoorbeeld instelt op ON en een website opent die al is geïmplementeerd met at.js, ontvangt u een bericht met de melding dat at.js al is geladen. We verwachten dat de meeste klanten at.js al hebben geïmplementeerd op hun pagina&#39;s en de standaardinstelling van OFF gebruiken.

* De extensie laadt de nieuwste versie van at.js die beschikbaar is via de [!DNL Target UI] insteekmodule [!UICONTROL Administration > Implementation].
* Als u de extensie gebruikt om te injecteren in [QA-modus](/help/c-activities/c-activity-qa/activity-qa.md), moet u een ander Chrome-tabblad openen. Dit tabblad Chrome moet worden geverifieerd bij dezelfde [!DNL Adobe Experience Cloud] organisatie waarin u de activiteit hebt gemaakt.
* De volgende berichten helpen u op de hoogte houden:

   * Als u probeert om een website te laden die VEC gebruikt die er niet in slaagt te laden, toont een bericht die suggereert dat u de VEC Helper browser uitbreiding installeert.
   * Als at.js nog niet op de website wordt uitgevoerd, toont een bericht in VEC die dat u de uitbreiding installeert.
   * Als de extensie is ingeschakeld en de laadbewerking uitvoert, worden berichten weergegeven wanneer de extensie de bibliotheek at.js injecteert (indien nodig) of wanneer de website betrouwbaar wordt geopend in de VEC.