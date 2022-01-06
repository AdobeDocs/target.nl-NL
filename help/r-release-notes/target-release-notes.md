---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: df00a36ea3440ebd959351fcfc6a24f6bd9fe8b8
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 6 januari 2022**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021, [!DNL Adobe Target] ondersteunt de bibliotheek mbox.js niet meer. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en hebben deze invloed op uw pagina&#39;s die [!DNL Target] activiteiten die worden uitgevoerd door het bedienen van standaardinhoud.
>
>Als u potentiële problemen met uw sites wilt voorkomen, migreert u naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js. Zie voor meer informatie [Overzicht: Doel voor client-side web implementeren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 22.1.1 (6 januari 2022)

Deze release bevat de volgende nieuwe functie:

| Functie | Details |
| --- | --- |
| Aanbiedingsbeslissingen gebruiken in doelactiviteiten | U kunt nu [!DNL Adobe Journey Optimizer] besluiten aanbieden in [!DNL Adobe Target] A/B Test and Experience Targeting (XT)-activiteiten om de volgende beste aanbieding voor uw bezoekers op het web en mobiel te bepalen en te leveren.<br>Zie Aanbiedingsbesluiten gebruiken voor meer informatie.<br>**Opmerking**: Deze mogelijkheid is beschikbaar voor [!DNL Target] klanten die ook toegang hebben tot Offer decisioning en een [!DNL Target] implementatie die op het Web SDK van het Platform van de Adobe Ervaring wordt gebaseerd. |

## at.js versie 2.7.0 (28 oktober 2021)

Deze release bevat de volgende verbeteringen:

* Extra ondersteuning voor [Webcomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Deze versie van at.js wordt vereist om gepersonaliseerde ervaringen en aanbiedingen op douaneelementen en op elementen binnen douaneelementen tot stand te brengen en te testen. Deze functionaliteit is opgenomen in de [!DNL Target Standard/Premium] Release 21.10.5.

## [!DNL Target Standard/Premium] 21.10.5 (28 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | Extra ondersteuning voor [Webcomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). U kunt persoonlijke ervaringen en aanbiedingen maken en testen op aangepaste elementen en op elementen in aangepaste elementen.<br>Zie voor meer informatie [Opties voor Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#custom). |

## [!DNL Target Standard/Premium] 21.10.4 (21 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| Recommendations op basis van winkelwagentjes | Er is een nieuwe reeks algoritmen toegevoegd om aanbevelingen te doen op basis van de inhoud van het winkelwagentje van de bezoeker.<br>Zie &quot;Op winkelwagentje gebaseerd&quot; in [Criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md) en &quot;Winkelwagentjes toevoegen/winkelwagentjes weergeven/uitchecken van pagina&#39;s&quot; en &quot;Items uitsluiten die zich al in het winkelwagentje van de bezoeker bevinden&quot; in [Recommendations plannen en implementeren](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen, correcties en wijzigingen:

* Opgeloste problemen waardoor klanten de [!UICONTROL A4T] in [!DNL Analysis Workspace] door op de knop [!UICONTROL View in Analytics] knop in [!DNL Target] activiteitenrapportage. (TGT-42099, TGT-42100)
* Het probleem dat de oorzaak was van de [!UICONTROL Edit Design] knop niet weergeven tijdens bewerken [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten die de [!UICONTROL Form-Based Experience Composer]. (TGT-41980)
* Het probleem dat ervoor zorgde dat de [!UICONTROL Compatible] selectievakje van weergave in selectie criteria tijdens het maken van een nieuwe [!UICONTROL Recommendations] activiteit. (TGT-42053)
* Probleem verholpen waarbij een foutbericht werd weergegeven dat niet kon worden geselecteerd [!DNL Analytics] als rapportagebron (A4T) wegens gebrek aan [!DNL Analytics] machtigingen. (TGT-41954)
* Geïmplementeerde veelvoudige toegankelijkheidsmoeilijke situaties om toetsenbordnavigatie over de [!DNL Target] UI.

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
