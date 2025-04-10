---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 8af56181ea0ed74eb41d799908ce50f0436d330c
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**laatst bijgewerkt: 10 april, 2025**

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

* Probleem verholpen waardoor klanten de publieksinformatie-pop-up voor bepaalde [!UICONTROL Experience Targeting] (XT) activiteiten niet konden openen. (TGT-52049)
* Probleem verholpen waardoor klanten [!UICONTROL Experience Fragment] niet konden invoegen in de standaardwerkruimte. (TGT-52073)
* Probleem verholpen waarbij een aanbieding liet zien dat &quot;Inhoud niet gevonden&quot; en niet op de pagina [!UICONTROL Offers] werd weergegeven voor een [!UICONTROL Automated Personalization] -activiteit (AP). (TGT-52150)
* De mogelijkheid toegevoegd om dubbele doelgroepen binnen een activiteit toe te staan. (TGT-51200)
* Probleem verholpen waarbij de verkeerde naam van het selectievakje op de pagina [!UICONTROL Goals & Settings] werd weergegeven voor een XT-activiteit na bewerking. (TGT-52026)
* Correctie van een probleem waarbij `defaultContent` werd weergegeven in opties ondanks dat het zich niet in `experiences/optionLocations` bevond. (TGT-52036)
* Oplossing voor een probleem dat ervoor zorgde dat lege tekenreeksen niet werden omgezet in null-waarden. (TGT-52037)
* Probleem verholpen waarbij klanten de [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] op de [!UICONTROL Goals & Settings] pagina na bewerkingen opnieuw moesten configureren. (TGT-52071)
* Probleem verholpen waarbij een activiteit zonder leveringsregels voor pagina&#39;s meerdere regels op de pagina [!UICONTROL Overview] weergaven. (TGT-52084)
* Er is een foutbericht toegevoegd voor gebruikers die een aanbieding proberen op te slaan met tekens buiten het meertalige basisvlak, zoals emojis. (TGT-52105)
* Probleem verholpen waarbij het openen van een activiteit het foutbericht veroorzaakte: &quot;Deze activiteit gebruikt een of meer soorten publiek die bij de bron zijn verwijderd.&quot; (TGT-52120)
* Probleem verholpen waarbij ClickTrack-meetgegevens niet werden weergegeven in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) tijdens het bewerken. (TGT-52152)
* Probleem verholpen waarbij een URL met een queryparameter als de activiteitenlocatie de queryparameter niet op de pagina [!UICONTROL Overview] van de activiteit weergaf. (TGT-51635)
* Probleem verholpen waarbij de volledige URL voor de beleving niet kon worden weergegeven in [!UICONTROL Browse mode] binnen de [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* Probleem verholpen waarbij tijdens het bewerken van een activiteit de levering van een pagina ertoe leidde dat &#39;/&#39; aan het einde van de URL werd toegevoegd, waardoor deze ongeldig werd. (TGT-52114)
* Probleem verholpen waarbij de koppeling [!UICONTROL Activity QA] in de [!UICONTROL Form-Based Experience Composer] -pagina onjuist werd omgeleid naar de [!DNL Adobe Experience Cloud] -startpagina. (TGT-52055)
* Er is een foutbericht toegevoegd om gebruikers te begeleiden bij het oplossen van dubbele opties in een activiteit. (TGT-51927)
* Probleem verholpen waarbij extra pagina&#39;s die aan de [!UICONTROL A/B Test] -activiteit zijn toegevoegd, niet werden behouden na het opslaan en opnieuw openen. (TGT-51994)
* Probleem verholpen waarbij klanten stijlen niet konden verwijderen uit de sectie inline stijl. (TGT-52070)
* Herstelde toegang tot [ kaarten van de publieksdefinitie ](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) in de [!UICONTROL Activity QA] dialoogdoos, gelijkend op erfenis UI. (TGT-52056)
* De bijgewerkte interface heeft pagina&#39;s of publiek niet zonder wijzigingen opgeslagen. Als klanten nieuwe pagina&#39;s of publiek aan een activiteit toevoegden maar geen veranderingen in hen aanbrengen, [!DNL Target] verwierp het ongewijzigde publiek bij het bewaren. Meldingen zijn toegevoegd op relevante plaatsen om gebruikers op de hoogte te stellen van dit gedrag. (TGT-52104)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html) {target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
