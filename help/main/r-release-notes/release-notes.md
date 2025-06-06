---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates,huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5f41bcebce4e103fada006f53cd3ccd297769d0d
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard] - en [!DNL Target Premium] -release. Daarnaast worden releaseopmerkingen voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## [!DNL Target Standard/Premium] 25.6.1 (6 juni 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij QA-koppelingen niet de juiste ervaring voor de bijbehorende activiteit hebben opgeleverd. (TGT-52163 &amp; TGT-52790)
* Probleem opgelost waarbij voor QA-koppelingen de bijbehorende gebruikers-id ontbrak. (TGT-52722)
* Probleem verholpen om ervoor te zorgen dat ervaringen alleen worden opgedaan wanneer de geconfigureerde URL voor het leveren van pagina&#39;s correct is voldaan. (TGT-52696)
* Probleem verholpen waardoor klanten geen [!DNL Recommendations] -ontwerpsjabloon konden maken. Als u een sjabloon probeerde te maken, werd de fout geactiveerd: &quot;Er moet ten minste één entiteitsvariabele in het script worden gebruikt.&quot; (TGT-52395)
* Probleem verholpen waarbij het opslaan van [!DNL Recommendations] -ontwerpen met behulp van snelheidsarrays werd voorkomen. Het foutbericht &quot;Er moet ten minste één entiteitsvariabele in het script worden gebruikt&quot; is onjuist geactiveerd. (TGT-52734)
* Correctie van een probleem waarbij wijzigingen niet toegankelijk waren in de map [!UICONTROL Visual Experience Composer] (VEC) wanneer de pagina niet kon worden geladen voor interne webpagina&#39;s. (TGT-52488 &amp;TGT-52470)
* Probleem verholpen waarbij het deelvenster [!UICONTROL Modifications] niet zichtbaar was op kleinere schermgrootten in de VEC. (TGT-52470)
* Probleem verholpen in de bijgewerkte VEC waarbij het overschakelen van de modus [!UICONTROL Browse] naar de modus [!UICONTROL Design] een consolefout veroorzaakte en verdere interactie werd voorkomen. (TGT-52532)
* Probleem verholpen waarbij het klikken op bepaalde elementen per ongeluk de grootte ervan uitbreidde. (TGT-52497)
* Probleem verholpen waarbij bepaalde pagina-elementen niet konden worden geladen of herkend in de VEC, waardoor interactie zoals het selecteren van knoppen of banners en het verstoren van het nauwkeurig bijhouden van gebeurtenissen in activiteiten werd voorkomen. (TGT-52663)
* Probleem verholpen waardoor klanten aanbiedingen in [!UICONTROL Automated Personalization] (AP)-activiteiten niet konden verwijderen of verwijderen. (TGT-52690)
* Probleem verholpen dat inconsistente kwalificatiegedrag van activiteiten in activiteiten met meerdere pagina&#39;s veroorzaakte. (TGT-52694)
* Probleem verholpen waarbij op de pagina [!UICONTROL Overview] van de activiteit een ongeldige URL voor de [!UICONTROL Activity Location] werd weergegeven. (TGT-52695)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] die ervoor zorgde dat dubbele items werden weergegeven voor activiteitenlocaties. (TGT-52693)
* Probleem verholpen dat een `getAudiencesV3` -fout veroorzaakte, waardoor klanten activiteiten niet konden bewerken of kopiëren. (TGT-52709)
* Probleem verholpen dat een ongeldige payload-fout veroorzaakte bij het toevoegen van [!UICONTROL Experience Fragments] - of HTML-aanbiedingen aan een activiteit. (TGT-52779 &amp; TGT-52773)
* Probleem verholpen waarbij E [!UICONTROL xperience Fragments] niet correct werd weergegeven vanwege een ongeldige invoerfout in de bijgewerkte [!DNL Target] UI. (TGT-52701)
* Probleem verholpen waardoor klanten hun activiteiten in de [!UICONTROL Form-based Experience Composer] niet konden bewerken vanwege een ongeldige gebruikersfout. (TGT-52470)
* Probleem met lokalisatie in de Koreaanse taal verholpen waarbij in eerdere vertalingen tekens werden gebruikt buiten het meertalige basisvlak. In de bijgewerkte vertaling worden de juiste tekens gebruikt die de bedoelde betekenis nauwkeurig aangeven. (TGT-52508 &amp; TGT-52509)
* Probleem met lokalisatie in de Koreaanse taal verholpen waarbij de vertaling voor &quot;date&quot; inconsistent was bij het selecteren van begin- en einddatums voor een activiteit. (TGT-52510)

## Afschrijving van versieschakelaar van doel-UI (23 mei 2025) {#toggle}

De uitrol van het nieuwe [!DNL Target] gebruikersinterface zal tegen **27 mei, 2025** volledig zijn. Op dat punt, zullen alle klanten toegang tot de recentste versie UI hebben.

Beginnend **Juni 22, 2025**, zal de knevel van de versie UI worden verwijderd. Alle gebruikers gaan permanent over naar de nieuwe interface, zonder optie om naar de vorige versie terug te keren.

### Belangrijke informatie over de knevel van de versie UI

We bieden een tijdelijke functie waarmee u met een schakelknop kunt schakelen tussen de bijgewerkte [!DNL Target] interface en de oudere versie. Deze optie is beschikbaar slechts tijdens de definitieve fase van de rollout UI.

![ de versiesknevel van het Doel UI ](/help/main/r-release-notes/assets/toggle.png)

Zodra de rollout volledig is, zal de knevel worden verwijderd, en alle gebruikers zullen permanent naar bijgewerkte UI op **Juni 22, 2025** overgaan. Adobe raadt aan vooruit te plannen, aangezien deze functie binnenkort wordt afgebouwd.

### Beperkingen van het gedrag van de UI-schakelfunctie

* **Zichtbaarheid van nieuwe activiteiten**: De activiteiten die in bijgewerkte UI worden gecreeerd zullen niet zichtbaar zijn als u terug naar erfenisUI schakelt.
* **het uitgeven van bestaande activiteiten**: De veranderingen die aan bestaande activiteiten (oorspronkelijk in erfenis UI) worden aangebracht terwijl het gebruiken van bijgewerkte UI zullen worden gepubliceerd aan uw website. Deze updates zijn echter niet zichtbaar in de oudere UI als u terugschakelt. Alleen de laatste updates die zijn uitgevoerd vanuit de oudere UI worden daar weergegeven.
* **Consistentie van activiteitendetails**: De meest recente veranderingen, ongeacht welke UI u gebruikt, zullen op uw levende website worden weerspiegeld. In de oudere gebruikersinterface worden echter alleen de laatste wijzigingen weergegeven die in die versie zijn aangebracht. Dit zou verwarring kunnen veroorzaken als de activiteiten die in bijgewerkte UI worden uitgegeven verschillend kijken dan wat u in erfenisUI ziet.

### Meer informatie over de bijgewerkte gebruikersinterface

* [[!DNL Target Standard/Premium]  25.2.1 (17 februari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Activities], [!UICONTROL Recommendations], en [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium]  25.1.1 (9 Januari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Offers Library].

* [ begrijp  [!DNL Target]  UI ](/help/main/c-intro/understand-the-target-ui.md): Verstrekt een kort overzicht om u te helpen vertrouwd worden met [!DNL Target] en verleent verbindingen voor meer diepgaande informatie en geleidelijke instructies.

* [[!UICONTROL Visual Experience Composer] changes ](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md) : In de release [!DNL Adobe Target Standard/Premium] 25.2.1 (17 februari 2015) wordt een bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) geïntroduceerd. Dit artikel verklaart de verschillen tussen de erfenis en bijgewerkte versies van VEC.

* [[!UICONTROL Visual Experience Composer] opties ](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): Dit artikel verklaart bijgewerkte UI VEC en zijn opties.

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=nl-NL) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
