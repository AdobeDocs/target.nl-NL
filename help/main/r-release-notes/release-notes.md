---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 9489655d18170c581f2abf8502f01c7b7e0626b7
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## [!DNL Target Standard/Premium] 22.5.1 (gespreide vrijgave; mei (11-13 mei 2022)

Deze release is beschikbaar volgens het volgende schema:

* **11 mei**: Regio Azië-Stille Oceaan (APAC)
* **12 mei**: Noord-Amerika (NA)
* **13 mei**: Europa, Midden-Oosten en Afrika (EMEA)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen dat een JavaScript-fout veroorzaakte en sommige klanten de toegang tot de activiteitsgegevens voor bepaalde [!UICONTROL Automated Personalization] (AP) activiteiten. (TGT-43526)
* Probleem verholpen waardoor sommige klanten geen specifieke aanbieding aan een AP-activiteit konden toevoegen (of bewerken). (TGT-43503)
* Probleem opgelost in het dialoogvenster [!DNL Target] UI die het volgende foutenbericht toonde: &quot;Uw globale box is mogelijk niet synchroon. Probeer het opnieuw op te slaan.&quot; Dit probleem betrof een UI-probleem en had geen invloed op de implementaties van klanten. (TGT-43475)
* Probleem verholpen waardoor één klant geen verfijningen en publiek op ervaringsniveau kon bewerken voor een activiteit als de verfijningen en het publiek vóór de nieuwe [!UICONTROL Audiences] UI is geïmplementeerd. (TGT-43433)
* Het probleem waarbij klanten dubbele gegevens konden selecteren, is opgelost. [!DNL Adobe Audience Manager] (AAM) publiek tijdens het bewerken van het rapportagepubliek voor een activiteit. (TGT-43430)
* Probleem verholpen waardoor klanten geen dubbel publiek konden maken, maar in verschillende werkruimten. (TGT-43423)
* Probleem verholpen waardoor klanten geen locaties konden verwijderen die ad-hocaanbiedingen hadden in activiteiten die in het dialoogvenster [!UICONTROL Form-Based Experience Composer]. (TGT-43315)
* Probleem verholpen waarbij klanten geen toegang kregen tot de aangeboden code nadat ze op de aanbiedingen voor afbeeldingen hadden geklikt en de interface vervolgens hadden vernieuwd. (TGT-43566)
* Zorgde ervoor dat de lijst van metriek beschikbaar in [!DNL Target] UI wanneer het creëren van activiteiten die gebruiken [!DNL Analytics for Target] (A4T) geeft alleen die metriek weer die zijn verzameld door [!DNL Adobe Analytics]. (TGT-43294)
* Probleem verholpen waarbij tijdens het bewerken van profielscripts het oorspronkelijke, onbewerkte script werd hersteld nadat het script was bewerkt, geactiveerd en vervolgens gedeactiveerd. Het profielscript blijft nu in de bewerkte status staan. (TGT-43249)
* Probleem verholpen waarbij de volgende fout is opgetreden bij een poging een publiek naar een andere werkruimte te verplaatsen: &quot;We kunnen je aanvraag niet voltooien. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-43212)
* Correctie van een fout die een fout veroorzaakte bij het klonen van aangepaste codewijzigingen voor App-pagina&#39;s (SPA) van één pagina. (TGT-43137)
* Probleem verholpen waarbij de oorspronkelijke aanbieding werd beïnvloed nadat een ervaring was gedupliceerd en de promotie vervolgens was bewerkt. (TGT-41775)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie voor meer informatie [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Zie voor meer informatie [Opmerkingen bij de release van vorige releases](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie voor meer informatie [Opmerkingen bij de release Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie, zie [Opmerkingen bij de doelversie - Prerelease](/help/main/r-release-notes/target-release-notes.md) pagina. |
