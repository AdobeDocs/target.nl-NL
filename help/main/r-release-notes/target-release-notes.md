---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: eaba6fe562644874fc800612894218094ca37f1b
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatste bijgewerkt: 8 April, 2025**

>[!NOTE]
>
>Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel ](release-notes.md). [ De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## Update voor doelmachtigingen (22 april 2025)

Deze toekomstige update verbetert de organisatorische controle over [!DNL Target] instantieconfiguraties, die toevallige updates verhinderen die activiteitenlevering over diverse test en verpersoonlijkingsteams zouden kunnen beïnvloeden.

Vanaf 22 april 2025 kunnen alleen [!UICONTROL Product] - en [!UICONTROL Solutions] -beheerders instellingen in de [!UICONTROL Administration] -secties bijwerken, ongeacht hun rollen in [!DNL Target] -werkruimten. Gebruikers zonder deze machtiging hebben alleen-lezen toegang tot de secties van [!UICONTROL Administration] .

Voor meer informatie, zie [ Doel beheren ](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.3 (10 april 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij de koppeling [!UICONTROL Activity QA] in de [!UICONTROL Form-Based Experience Composer] -pagina onjuist werd omgeleid naar de [!DNL Adobe Experience Cloud] -startpagina. (TGT-52055)
* Er is een foutbericht toegevoegd om gebruikers te begeleiden bij het oplossen van dubbele opties in een activiteit. (TGT-51927)

## [!DNL Target Standard/Premium] 25.4.2 (8 april 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij extra pagina&#39;s die aan de [!UICONTROL A/B Test] -activiteit zijn toegevoegd, niet werden behouden na het opslaan en opnieuw openen. (TGT-51994)
* Probleem verholpen waarbij klanten stijlen niet konden verwijderen uit de sectie inline stijl. (TGT-52070)
* Herstelde toegang tot [ kaarten van de publieksdefinitie ](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) in de [!UICONTROL Activity QA] dialoogdoos, gelijkend op erfenis UI. (TGT-52056)
* De bijgewerkte interface heeft pagina&#39;s of publiek niet zonder wijzigingen opgeslagen. Als klanten nieuwe pagina&#39;s of publiek aan een activiteit toevoegden maar geen veranderingen in hen aanbrengen, [!DNL Target] verwierp het ongewijzigde publiek bij het bewaren. Meldingen zijn toegevoegd op relevante plaatsen om gebruikers op de hoogte te stellen van dit gedrag. (TGT-52104)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
