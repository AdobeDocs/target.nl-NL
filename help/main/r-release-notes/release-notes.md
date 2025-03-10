---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates,huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: cee17e318dedffaadccd2f93ae593e5fdd2bd600
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard] - en [!DNL Target Premium] -release. Daarnaast worden releaseopmerkingen voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## [!DNL Target Standard/Premium] 25.3.4 (7 maart 2025)

Deze release bevat de volgende correcties en updates:

* Oplossing voor een probleem waarbij alleen-activiteit publiek niet zichtbaar was in het deelvenster [!UICONTROL Audiences] , zodat het niet kon worden bewerkt of hergebruikt. (TGT-51860)
* Probleem verholpen waarbij [!DNL Target Standard] klanten ervan weerhield activiteiten te maken met behulp van [!UICONTROL Analytics for Target] (A4T)-rapporten. (TGT-51854)
* Probleem verholpen waarbij lokale id-tellers tijdens het maken en bewerken van batchbewerkingen werden uitgesloten van de payload. (TGT-51867)

## [!DNL Target Standard/Premium] 25.3.2 (6 maart 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij het kopiëren van een activiteit met een alleen-activiteit publiek er niet in slaagde een nieuwe activiteit te maken, in plaats daarvan per ongeluk het publiek van de oorspronkelijke activiteit te gebruiken. (TGT-51855)
* Probleem verholpen waardoor [!UICONTROL Experience Targeting] (XT)-activiteiten niet konden worden bewerkt met alleen-activiteit publiek. (TGT-51846)
* Probleem verholpen waarbij [!UICONTROL Visual Experience Composer] (VEC) geen wijzigingen toepaste op een ervaring die correct werd verwerkt bij de eerste bewerking. (TGT-51843)
* Probleem verholpen waarbij een &#39;ID&#39;-fout optrad wanneer werd geklikt op bepaalde elementen in de VEC. (TGT-51814)
* Bijgewerkte fout behandeling in VEC tijdens activiteitenverwezenlijking. (TGT-51759)
* Probleem verholpen waarbij een ontbrekende weergave in het deelvenster [!UICONTROL Modifications] een fout met &#39;ongeldige gebruikersinvoer&#39; veroorzaakte bij het opslaan van de activiteit. (TGT-51827)
* Probleem opgelost waarbij geen aanbevelingen konden worden geformuleerd. (TGT-51834)
* Er is een bevestigingsbericht toegevoegd voordat naar een andere URL wordt omgeleid. (TGT-51703)
* Problemen verholpen met GraphQL-integratietests in aanbiedingen en mappen. (TGT-51839)

## [!DNL Target Standard/Premium] 25.3.1 (3 maart 2025)

Deze release bevat de volgende correcties en updates:

* Een gecombineerd publiek kan subgroepen bevatten, die elk meerdere soorten publiek bevatten. Deze release verholpen een probleem dat ervoor zorgde dat het publiek van de subgroep niet kon weergeven in het dialoogvenster [!UICONTROL Rules] . (TGT-51813)
* Het volgende probleem is opgelost: sommige ervaringsgebruikers zijn vervangen door [!UICONTROL All Visitors] bij het openen van oudere activiteiten. (TGT-51812)
* Het probleem dat bewerkingsactiviteiten niet mogelijk maakte, is opgelost met alleen-activiteit publiek. (TGT-51807)
* Oplossing voor een probleem waardoor wijzigingen in de paginakoppen in de bijgewerkte gebruikersinterface van [!DNL Target] niet konden worden bewerkt. (TGT-51797)
* Oplossing voor een null-fout die optrad bij het dupliceren van een ervaring, het verwijderen van een andere ervaring en het vervolgens opslaan van de activiteit. (TGT-51796)
* Oplossing voor een probleem dat ervoor zorgde dat de uitsluitingsregels van het publiek niet konden worden weergegeven in het deelvenster met publieksinfo tijdens de [!UICONTROL Targeting] -stap van het maken van activiteiten. (TGT-51579)
* Bijgewerkte foutberichten die in het Koreaans zijn gelokaliseerd. (TGT-51701 &amp; TGT-51699)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html) {target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html) {target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html) {target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
