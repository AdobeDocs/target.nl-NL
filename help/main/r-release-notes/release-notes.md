---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates,huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 0f96fb2a74a0716542308037d183847c91b1dc04
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard] - en [!DNL Target Premium] -release. Daarnaast worden releaseopmerkingen voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## [!DNL Target Standard/Premium] 25.5.1 (5 mei 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij werd voorkomen dat publieksverfijningen worden weergegeven voor bepaalde activiteiten in de bijgewerkte gebruikersinterface. (TGT-52057)
* Probleem verholpen waarbij het gebruik van gecombineerd publiek in activiteiten werd voorkomen. (TGT-52346)
* Probleem verholpen waarbij het maken van een nieuwe activiteit in een niet-standaardwerkruimte werd voorkomen met een alleen-activiteit publiek in dezelfde werkruimte. (TGE-52349)
* Probleem verholpen waarbij alleen-activiteit publiek uit de bijgewerkte gebruikersinterface verdween nadat een nieuw publiek was gemaakt en geselecteerd. (TGT=52091)
* Probleem verholpen waarbij het gebruik van dubbele doelgroepen in activiteiten werd voorkomen. (TGT-51200 &amp; TGT-52057)
* Probleem verholpen waarbij publieksverfijningen en het activiteitenpubliek werden omgekeerd in de bijgewerkte gebruikersinterface. (TGT-52158)
* Probleem verholpen waarbij het maken van een nieuwe activiteit niet mogelijk was als gevolg van een gebruikersinvoerfout: &quot;Niet-standaardwerkruimte niet toegestaan voor deze gebruiker.&quot; (TGT-52267)
* Probleem verholpen waardoor voorstellen niet konden worden weergegeven in de bijgewerkte gebruikersinterface voor zowel standaardwerkruimten als niet-standaardwerkruimten. [!DNL Target] geeft nu voorstellen van beide werkruimten weer. (TGT-52339)
* [!DNL Target] heeft een probleem verholpen waarbij klanten niet werden gewaarschuwd wanneer ze een activiteit bewerkten en een gewijzigd website-element veranderden. (TGT-52100)
* Probleem verholpen waarbij tijdens het bewerken van een voorstel met ad-hocaanbiedingen een nieuwe aanbieding werd gemaakt in plaats van de bestaande aanbieding bij te werken. (TGT-52135)
* Probleem verholpen dat een ongeldige laadfout veroorzaakte bij het verplaatsen van voorstellen naar mappen. (TGT-52325)
* Probleem verholpen waarbij een fout met gebruikersinvoer werd veroorzaakt bij het verplaatsen van aanbiedingen naar mappen. (TGT-52296)
* Er is een veld `audienceMetadata` toegevoegd voor elke activiteit en er is voor gezorgd dat dit wordt gelezen en bijgewerkt tijdens het bewerken van de activiteit. (TGT-51004)

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
