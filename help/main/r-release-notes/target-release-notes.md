---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: bdc2f76af2a1f1554556d56a983748aa2c9caf2c
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatste bijgewerkt: 14 Maart, 2025**

>[!NOTE]
>
>Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel ](release-notes.md). [ De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.3.7 (26 maart 2025)

Deze release bevat de volgende correcties en updates:

* Oplossing voor een probleem dat het opslaan van activiteiten met meerdere pagina&#39;s blokkeerde als een pagina na wijzigingen werd verwijderd. (TGT-51988)
* Oplossing voor een fout die optrad tijdens het bewerken van een activiteit: `default message [Invalid optionLocalIds: xx]]` . (TGT-51985)
* Oplossing voor een probleem waarbij het toevoegen van nieuwe wijzigingen aan een activiteit bestaande wijzigingen verwijdert. (TGT-51981)
* Oplossing voor een probleem waarbij het vervangen van een publiek door &quot;[!UICONTROL All visitors]&quot; tijdens het maken of bewerken van activiteiten ertoe leidde dat een fout &quot;Duplicate audiences are not allowed&quot; werd weergegeven. (TGT-51978)
* Oplossing van een probleem dat bij het opslaan van een [!UICONTROL A/B Test] -activiteit een fout in de gebruikersinvoer heeft veroorzaakt. (TGT-51976)
* Oplossing voor een probleem waardoor berekende metriek niet correct kon worden weergegeven op de pagina [!UICONTROL Goals & Settings] . (TGT-51975)
* Oplossing voor een probleem dat ervoor zorgde dat `companyName` en `reportSuite` niet konden worden vergeleken in de [!DNL Analytics] -configuratie voor de `pageviews` -meting. (TGT-51965)
* Oplossing van een probleem waarbij de omschakelingservaringen in een activiteit wijzigingen hebben verwijderd. (TGT-51945)
* Oplossing voor een probleem waarbij door het verwijderen van een paginapubliek ook [!UICONTROL ClickTrack] kiezers werden verwijderd. (TGT-51935)
* Oplossing voor een probleem waardoor een activiteit na het openen van de [!UICONTROL Overview] -pagina niet meer bewerkbaar werd. (TGT-51931)
* Oplossing voor een probleem dat een `[Unused optionLocalIds: 0]]` -fout veroorzaakte tijdens het maken van activiteiten. (TGT-51920)
* Correctie van een probleem waarbij sommige wijzigingen niet correct werden omgezet nadat wijzigingen in de tekststijl waren verwijderd. (TGT-51876)
* Oplossing voor een probleem dat ervoor zorgde dat doelgroepen niet correct konden worden bijgewerkt in de [!UICONTROL Form-Based Experience Composer] . (TGT-51845)
* Correctie van een probleem waarbij de URL in de [!UICONTROL Visual Experience Composer] niet correct werd bijgewerkt tijdens de navigatie. (TGT-51832)
* Oplossing voor een probleem dat ervoor zorgde dat aanbiedingen niet konden worden weergegeven in de gebruikersinterface van [!UICONTROL Offers] , ondanks de correcte weergave bij het maken van een activiteit en het toevoegen van aanbiedingen. (TGT-51805)
* Oplossing voor een probleem waarbij bij sommige activiteiten geen fallback-scherm beschikbaar was om standaardinhoud weer te geven wanneer gepersonaliseerde of gerichte inhoud niet kon worden geleverd. (TGT-51638)
* Oplossing voor een probleem dat ervoor zorgde dat liveaanbiedingen en bepaalde mappen niet correct konden worden weergegeven in de gebruikersinterface van [!UICONTROL Offers] . (TGT-51628)
* Oplossing voor een probleem dat ervoor zorgde dat sommige URL-tekenreeksen en goURL&#39;s niet correct werden gelokaliseerd. (TGT-35741)
* Probleem verholpen waarbij werd voorkomen dat rollen ( [!UICONTROL Approver] , [!UICONTROL Editor] en [!UICONTROL Observer] ) correct werden gelokaliseerd in de [!DNL Target] gebruikersinterface. (TGT-29925)

## [!DNL Target Standard/Premium] 25.3.6 (14 maart 2025)

Deze release bevat de volgende correcties en updates:

* Oplossing voor de fout &#39;&#39;Ongeldige gebruikersinvoer&#39;&#39; in [!UICONTROL Visual Experience Composer] -activiteiten (VEC) waarbij [!UICONTROL Click Tracking] ingeschakeld is wanneer dezelfde [!UICONTROL ClickTrack] -kiezer meerdere keren wordt gebruikt. (TGT-51921)
* Correctie van de fout &#39;&#39;Ongeldige gebruikersinvoer&#39;&#39; in VEC-activiteiten met gedeelde locaties (bijvoorbeeld HEAD-kiezer) en identieke aanbiedingen. (TGT-51879)
* Probleem opgelost waarbij ervaringswijzigingen werden gedeeld door het publiek. (TGT-51815)
* Validatiefouten zijn opgelost bij het maken van activiteiten vanwege conflict met segment-id. De fouten traden op wanneer [!DNL Target] bestaande activiteiten met anonieme segmenten detecteerde. (TGT-51784)
* Correctie van het probleem dat [!DNL Target] ervan weerhield activiteiten met uitsluitingsregels in een publiek op te slaan. (TGT-51581)
* Oplossing van het probleem waardoor klanten geen mappen konden maken, verwijderen of verplaatsen zonder toegang tot de standaardwerkruimte. (TGT-51499)
* Oplossing van het probleem dat ertoe leidde dat GET-aanvragen mislukten bij het ophalen van de [!DNL Analytics] metrielijst. (TGT-51106)

## [!DNL Target Standard/Premium] 25.3.5 (11 maart 2025)

Deze release bevat de volgende correcties en updates:

* Oplossing voor een probleem dat ervoor zorgde dat gebruikers de aanbiedingen in het deelvenster [!UICONTROL Modifications] niet konden wijzigen. (TGT-51800)
* Oplossing voor een probleem waarbij handelingen onjuist in het linkerdeelvenster werden weergegeven voor ervaringen en publiek, waaronder in de modus [!UICONTROL ClickTrack] . (TGT-51895)
* Correctie van een probleem waarbij [!UICONTROL ClickTrack] kiezers niet werden toegepast op de juiste publiekspagina. (TGT-51871)

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

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html) {target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
