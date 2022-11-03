---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen en verhogingen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 145f4bd2b3353e429ce968622e47653170a60fda
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 19 oktober 2022**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target] Standard/Premium 22.10.3 (gefaseerde release 25-27 oktober 2022)

Deze release is beschikbaar volgens het volgende schema:

* **25 oktober**: Europa, Midden-Oosten en Afrika (EMEA)
* **26 oktober**: Regio Azië-Stille Oceaan (APAC)
* **27 oktober**: Amerikaanse regio

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| Geoptimaliseerde A4T-meetwaarden voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]<br>(Beschikbaar om klanten te selecteren voor testen. In een toekomstige release beschikbaar voor alle klanten.) | Houd rekening met de volgende wijzigingen:<ul><li>Extra ondersteuning voor binaire en maximalisatiemetriek in [!UICONTROL Analytics for Target] A4T-rapportage voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten</li><li>Behoud van gedrag voor bestaande activiteiten tot februari 2023. Na deze datum zullen de activiteiten worden stopgezet om de migratie van bestaande activiteiten naar nieuw gedrag af te dwingen</li><li>Vanaf 20 februari 2023, ondersteuning voor `averagetimespentonsite`, `bouncerate`, en `entries` maatstaven in [!DNL Target] de activiteiten zullen worden afgekeurd .</li></ul> |

* Extra knopinfo in het dialoogvenster [!DNL Target] UI om klanten te helpen efficiënter navigeren de publieksbouwer en te leren hoe te om eigenschappen te gebruiken die onvertrouwd zouden kunnen zijn. (TGT-44139)
* Extra functionaliteit om te voorkomen dat klanten een activiteit bewerken die door [!DNL Target] omdat er niet-ondersteunde meetgegevens worden gebruikt. Een bericht in UI geeft klanten de opdracht om de activiteit te dupliceren en dan omzettings metrisch bij te werken.

   Met deze release `averagetimespentonsite`, `bouncerate`, en `entries` maatstaven in [!DNL Target] de activiteiten zullen worden vervangen voor nieuwe activiteiten . Bestaande activiteiten kunnen deze cijfers tot mei 2023 blijven gebruiken.

* Knopinfo toegevoegd in het dialoogvenster [!DNL Target] UI om klanten te helpen een optimalisatiecriteria te selecteren terwijl het creëren van of het uitgeven van een [!UICONTROL Auto-Target] activiteit die A4T gebruikt.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |


## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
