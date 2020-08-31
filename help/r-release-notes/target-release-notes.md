---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-releases.
title: Voorlopige Adobe Target-opmerkingen
feature: null
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 405715f1ee1afd1d298dc7f1ef0cd3599620cbca
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 0%

---


# Opmerkingen bij de release Doel (preRelease){#target-release-notes-prerelease}

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 31 augustus 2020**

Voor informatie over de huidige versie, zie de Nota&#39;s [van de Versie van het](release-notes.md)Doel. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

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
* Probleem verholpen waarbij de laatst gewijzigde waarde voor [!DNL Recommendations] criteria onjuist is. (TGT-37666)
* Probleem verholpen waarbij id&#39;s van een box in de vervolgkeuzelijst Mboxes werden weergegeven in plaats van namen van een box. (TGT-37739)

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
