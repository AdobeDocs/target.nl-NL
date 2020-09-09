---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release van Adobe Target (huidige) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 419825546dd5bf26f7a5a5498014c01bae65bd7b
workflow-type: tm+mt
source-wordcount: '1073'
ht-degree: 0%

---


# Opmerkingen bij de doelversie (huidig){#target-release-notes-current}

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke doelstandaard- en doelpremiumversie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>* **Adobe noemde opnieuw een leider in het Magisch Kwadrant Gartner voor Personalisatietechnieken**: Adobe werd opnieuw benoemd tot leider in het derde jaarlijkse Gartner Magic Quadrant for Personalization Engines, verslag 2020. Het Magische kwadrant van Gartner voor de Motoren van de Personalisatie evalueerde verkopers over 15 criteria die in twee categorieën vallen: de volledigheid van het gezichtsvermogen en de uitvoerbaarheid. [Lees er over op The Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **afdruk** mbox.js: Op 18 januari 2021 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 18 januari 2021, zullen alle vraag die van mbox.js wordt gemaakt zachtjes ontbreken en zullen uw pagina&#39;s beïnvloeden die de activiteiten van het Doel hebben die door standaardinhoud te dienen lopen. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, zullen onze ingenieurs en steunpersoneel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.
   >
   >
* **Doelaankondigingen**: Zie de de aankondigingspagina van het Doel voor informatie over aanstaande gebeurtenissen, met inbegrip van de zittingen van de Bouwer van de Vaardigheid van het Doel, ontwikkelaarchats, webinars, en de zittingen van het Break van de Koffie van het Doel. Voor meer informatie, zie [de aankondigingen](/help/r-release-notes/target-announcements.md)van het Doel.


De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

## Target Standard/Premium 20.8.2 (10 september 2020)

| Functie | Details |
| --- | --- |
| De aanbevelingen van de controle groeven binnen de opeenvolgingen van criteria | Met Criteria Sequences kunt u nu het aantal sleuven bepalen dat wordt opgenomen door de criteria van elke aanbeveling, zodat u verschillende typen items of een andere algoritme kunt combineren en afstemmen.<br>Zie [Criteria maken voor meer informatie](/help/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) . |

## Target Standard/Premium 20.8.1 (2 september 2020)

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij fouten werden weergegeven bij het laden van de nieuwe [!UICONTROL Administration] pagina&#39;s na het schakelen tussen organisaties. (TGT-37730)
* Probleem verholpen waarbij de onjuiste clientcode op de [!UICONTROL Administration > Implementation] pagina werd weergegeven. (TGT-37849)
* Probleem verholpen waardoor gebruikers soms de bewerkingsfuncties in de [!UICONTROL Visual Experience Composer] (VEC) niet konden gebruiken nadat de VEC met succes was geladen. (TGT-37162)
* Probleem verholpen waardoor pagina&#39;s niet konden worden geladen in de VEC en de Enhanced Experience Composer (EEC), ook al was de extensie VEC Helper geïnstalleerd. Dit was het gevolg van wijzigingen in Google Chrome 80+. Download de [bijgewerkte extensie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)VEC Helper. (TGT-37893)
* Probleem verholpen waarbij gebruikers soms werden verhinderd om 0,00 pagina te downloaden van de [!UICONTROL Administration > Implementation] pagina na het schakelen tussen organisaties. (TGT-37668)
* De downloadknop at.js is nu uitgeschakeld tijdens het laden om te voorkomen dat meerdere aanvragen worden verzonden [!DNL Target] als gebruikers meerdere keren op de downloadknop klikken. (TGT-37633)
* Probleem verholpen met [!UICONTROL Experience Targeting] (XT)-activiteiten die ertoe hebben geleid dat ervaringen gedurende een langere periode &quot;ophaalresultaten&quot; hebben getoond. (TGT-37684)
* Verbeterde navigatie en functionaliteit voor gebruikers met alleen toetsenbord. (TGT-34479 &amp; TGT-34473)
* Toegevoegde labels in de gebruikersinterface voor gebruikers die ondersteunende hulpmiddelen gebruiken. (TGT-34480)
* Het foutbericht is verbeterd bij het verwijderen van een mobiele viewport die momenteel wordt gebruikt in een activiteit. Het foutbericht luidt nu: &quot;Deze viewport is momenteel gekoppeld aan een of meerdere activiteiten. U moet viewport uit die activiteiten verwijderen alvorens het te kunnen schrappen.&quot; (TGT-37030)
* Toegevoegde steun in VEC om klik het volgen op een css selecteur toe te staan die meer dan één element in de pagina aanpast. (TGT-37323)
* Probleem verholpen waardoor bepaalde gebruikers de [!UICONTROL Activity] lijst niet konden weergeven. Het volgende foutbericht is weergegeven: &quot;Kan geen URL-suggesties ophalen.&quot; De fout kwam voor gebruikers voor gebruikend wagenterugloop in hun FirstName (FirstName/r/n) in het systeem van de Achterkant van de Adobe. (TGT-37330)
* Probleem verholpen waardoor gebruikers de [!UICONTROL Activity] pagina niet konden weergeven als de naam van de werkruimte (opgegeven in de [!UICONTROL Adobe Admin Console for Enterprise]) een apostrof bevat. (TGT-37709)
* Probleem verholpen bij [!UICONTROL Auto-Allocate] activiteiten tijdens het selecteren van optimalisatie- en conversiemetriek waarbij een foutbericht gebruikers verkeerd informeerde een rapportsuite te selecteren, ook al was er al een rapportsuite opgegeven. (TGT-37689)
* Probleem verholpen waarbij metrische gegevens op de [!UICONTROL Goals and Settings] pagina soms leeg werden na het navigeren naar de [!UICONTROL Targeting] pagina en vervolgens weer. (TGT-37691)
* Probleem verholpen waarbij een onjuiste laatst gewijzigde waarde voor [!DNL Recommendations] criteria werd veroorzaakt. (TGT-37666)
* Probleem verholpen waarbij id&#39;s van een box in de vervolgkeuzelijst Mboxes werden weergegeven in plaats van namen van een box. (TGT-37739)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release - Doelserver-side API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Opmerkingen bij de release met betrekking tot API&#39;s van de Adobe Target-server. |
| [Opmerkingen bij de release - Doel Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Release-aantekeningen met betrekking tot Adobe Target Node.js SDK. |
| [Opmerkingen bij de release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Opmerkingen bij de release met betrekking tot de Adobe Target Java SDK. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek van Adobe Target at.js. |
| [mbox.js, versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Op deze pagina worden wijzigingen in elke versie van mbox.js weergegeven.<br>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die mogelijk niet zijn opgenomen in deze releaseopmerkingen.<br>Zie [Documentatiewijzigingen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de [Versie voor vorige versies](../r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release [Experience Cloud voor meer informatie](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdatelijst | Meld u aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie, zie de Nota&#39;s van de Versie van het [Doel - pre-releasepagina](/help/r-release-notes/target-release-notes.md) . |
