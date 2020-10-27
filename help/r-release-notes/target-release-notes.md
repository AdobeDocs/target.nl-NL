---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-releases.
title: Voorlopige Adobe Target-opmerkingen
feature: null
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 13fca0cb4e749edbb5d21b0a58af5d4f4a91c14d
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---


# Opmerkingen bij de release Doel (preRelease){#target-release-notes-prerelease}

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 27 oktober 2020**

Voor informatie over de huidige versie, zie de Nota&#39;s [van de Versie van het](release-notes.md)Doel. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

>[!IMPORTANT]
>
>* **Adobe noemde opnieuw een leider in het Magisch Kwadrant Gartner voor Personalisatietechnieken**: Adobe werd opnieuw benoemd tot leider in het derde jaarlijkse Gartner Magic Quadrant for Personalization Engines, verslag 2020. Het Magische kwadrant van Gartner voor de Motoren van de Personalisatie evalueerde verkopers over 15 criteria die in twee categorieën vallen: de volledigheid van het gezichtsvermogen en de uitvoerbaarheid. [Lees er over op The Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js end-of-life**: Op 18 januari 2021 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 18 januari 2021, zullen alle vraag die van mbox.js wordt gemaakt zachtjes ontbreken en zullen uw pagina&#39;s beïnvloeden die de activiteiten van het Doel hebben die door standaardinhoud te dienen lopen. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, zullen onze ingenieurs en steunpersoneel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.
   >
   >
* **Doelaankondigingen**: Zie de de aankondigingspagina van het Doel voor informatie over aanstaande gebeurtenissen, met inbegrip van de zittingen van de Bouwer van de Vaardigheid van het Doel, ontwikkelaarchats, webinars, en de zittingen van het Break van de Koffie van het Doel. Voor meer informatie, zie [de aankondigingen](/help/r-release-notes/target-announcements.md)van het Doel.


## Target Standard/Premium 20.10.1 (27 oktober 2020)

Deze release bevat de volgende nieuwe functies:

| Functie | Details |
| --- | --- |
| Apparaatbeslissingen | Bij beslissingen op het apparaat kunnen zowel marketers als productontwikkelaars experimenteren en op machinaal leren gebaseerde personalisatie vanuit het apparaat van de gebruiker, via kanalen, met een bijna-nullatentie.<br>De snelheid en de prestaties zaken-in klanteninzichten en gebruikerstevredenheid.<br>Door op het apparaat te beslissen kunt u belangrijke personalisatie- en experimenteringsinstructies in A/B Test and Experience Targeting (XT) activiteitstypen compileren in &quot;optimalisatieartefacten:&quot;JSON voorwerpen die op klantenapparaten via CDN worden geladen. En omdat beslissingen op het apparaat op een native manier verbinding maken met [!DNL Adobe Experience Cloud] producten, krijgen [!DNL Target] gebruikers een snelle analyse en snellere ervaringen met herhalingen.<br>Zie *[Inleiding tot apparaatbeslissingen](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning)* in de *Adobe Target SDKs Guide* voor meer informatie.<br>**Nu registreren voor een live webinar.** Neem deel aan de productexperts van Adobe Target terwijl ze bespreken hoe u met beslissingen voor optimalisatie van kritieke ervaring op uw apparaat lokaal kunt uitvoeren met een nullatentie, deuren kunt openen voor spannende nieuwe gebruikssituaties en de prestaties van uw klanten kunt verbeteren.<ul><li>10 november 2020</li><li>10.00 uur PT / 12.00 uur CT / 13.00 uur ET</li><li>[Hier registreren](https://www.adobeeventsonline.com/Target/2020/OnDeviceDecisions/invite.html)</li></ul> |

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij weergave in [!UICONTROL Average Lift Confidence Interval] rapportage voor de [!UICONTROL Confidence] rij werd verhinderd [!DNL Auto-Target] en [!UICONTROL Total] verhinderd. De metingen worden correct weergegeven voor alle afzonderlijke ervaringen. (TGT-37301)
* Oplossing van een probleem dat gevolgen had voor de [!DNL Adobe Target Premium] rapportage van [!UICONTROL Auto-Target] gebruikers vanaf 15 september om 14.30 uur. (PDT) tot 6 oktober, 9:25 (PDT). Wanneer het bekijken van rapporten voor de beïnvloede omzettingsmetriek (gevormd gebruikend of &quot;[!UICONTROL Viewed a page]&quot;of &quot;[!UICONTROL Clicked on mbox]&quot;optie), worden de omzettingspercentages verkeerd gemeld. Er is momenteel geen bekend leveringsprobleem. Zie [Auto-Target rapportage](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) onder *Opgeloste problemen* in *bekende problemen en opgeloste problemen* voor informatie over het opnieuw synchroniseren en corrigeren van rapporten.
* Er is een selecteerbare [!UICONTROL Last Updated At] kolom in de [!UICONTROL Catalog Search] tabel en een [!UICONTROL Last Updated At] filter toegevoegd. Deze verbetering bespaart tijd en inspanning omdat u niet elk individueel punt moet openen om te zien wanneer het laatst werd bijgewerkt en u kunt filtreren door datum de punten werden laatst bijgewerkt.

   ![Laatst bijgewerkt bij kolom- en filterillustratie](/help/r-release-notes/assets/column-and-filter.png)

* Er zijn updates aangebracht om de doelgebruikersinterface compatibel te maken met de toegankelijkheidsrichtlijnen [voor](https://www.w3.org/WAI/standards-guidelines/wcag/) webinhoud (Web Content Accessibility Guidelines 2.0 Level A and AA Success Criteria) (WCAG 2.0 AA). (TGT-34384 &amp; TGT-24679)
* Verbeterde CSP-functies (Content Security Policy). (TGT-37035)
* Introduceerde een manier om de cliëntcode als parameter voor klanten te specificeren die CNAME gebruiken. (TNT-38571)
* [!DNL Adobe Experience Cloud] de documentatie gaat verder naar [!DNL Experience League]. In oktober gaan alle opmerkingen bij de release, artikelen, video&#39;s en zelfstudies van de huidige locatie `docs.adobe.com` naar [!DNL Experience League]. Deze beweging zorgt ervoor dat al het leren, zelfhulp, enablement, en communautaire inhoud van één enkele plaats wordt gediend. Wanneer deze wijziging optreedt, hoeft u niets te doen, aangezien alle koppelingen naar andere koppelingen worden omgeleid [!DNL Experience League]. De opmerkingen bij de release worden bijgewerkt wanneer de cutover begint.

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
