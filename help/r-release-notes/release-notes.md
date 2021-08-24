---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en bibliotheken JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Welke nieuwe eigenschappen worden inbegrepen in de huidige Versie?
feature: Opmerkingen bij de release
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: afa370a38921ab76babf5e49edc1e4b23ee807b0
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard]- en [!DNL Target Premium]-versie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, [!DNL Adobe Experience Platform Web SDK], at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].)

## om 2.6.1.2021 (16 augustus 2021)

* Bugcorrectie voor &quot;Geen artefact in cache beschikbaar voor hybride modus&quot; bij gebruik van apparaatbeslissingen.

## [!DNL Target] node.js SDK 2.2.0 (11 augustus 2021)

* Toegevoegde SDK-telemetriegegevensverzameling
* Automated Delivery API client openapi-codegen

Voor meer informatie over deze en vorige versies, zie [Logboek van de Verandering ](https://github.com/adobe/target-nodejs-sdk/blob/main/CHANGELOG.md) in [de documentatie van SDK van het Doel knoop.js](https://github.com/adobe/target-nodejs-sdk) op Github.

## [!DNL Target Standard/Premium] 21.8.1 (10 augustus 2021)

Deze onderhoudsversie bevat vele achterste verbeteringen, waaronder de volgende klantgerichte wijziging:

* Probleem verholpen waarbij rapporten werden gegenereerd voor [!UICONTROL Auto Personalization]-activiteiten die zijn gemaakt in [!UICONTROL Form-Based Experience Composer] om te verwijzen naar verwijderde aanbiedingen in rapporten. Dit gaf het volgende foutenbericht aan vertoning toe, &quot;wij hebben probleem het terugwinnen van gegevens voor dit rapport. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-41028)

## [!DNL Target Delivery API] (3 augustus 2021)

Deze release bevat de volgende verbeteringen:

* De limiet voor mbox-parameters is verhoogd tot 100 parameters. De vorige limiet was 50 parameters. (TNT-41717)
* De limiet voor `categoryId` is verhoogd tot 256 tekens. De vorige limiet was 128 tekens.
* De volgende [!DNL Adobe Audience Manager] (AAM) details zijn toegevoegd aan de leverings-API:

   * UUID AAM: De interne AAM-id die wordt gebruikt om een gebruiker op unieke wijze te identificeren.
   * dataPartnerId: Identiteitskaart voor een gegevenspartner.
   * dataPartnerUserId: De gebruikers-id die door een gegevenspartner wordt verstrekt.

   Eerder bevatte de leverings-API alleen `dcsLocationHint` en `blob`. (TNT-41644)

## om 2.6.0 uur (27 juli 2021)

* Beveiligd kenmerk toegevoegd aan cookies wanneer de instellingen `secureOnly` op `true` zijn ingesteld.
* De tokens van de reactie zijn nu beschikbaar wanneer het gebruiken `triggerView()`.
* Probleem verholpen met betrekking tot de gebeurtenis `CONTENT_RENDERING_NO_OFFERS`. Deze gebeurtenis wordt nu correct geactiveerd wanneer er geen inhoud wordt geretourneerd van [!DNL Target].
* [!DNL Anlytics for Target] (A4T) klik metriekdetails correct zijn teruggekeerd wanneer het gebruiken van  `prefetch` verzoeken.
* Bij UUID-generatie wordt `Math.random()` niet meer gebruikt, maar wordt `window.crypto` gebruikt.
* De vervaldatum van het `sessionId` cookie wordt correct verlengd bij elke netwerkaanroep.
* De [!UICONTROL Single Page Application] (SPA) initialisatie van het meningsgeheime voorgeheugen wordt nu correct behandeld en handhaaft montages `viewsEnable`.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie  [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C) voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de  [Versie voor vorige versies](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release  [Experience Cloud voor meer informatie](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van prereleaseinformatie, zie [de Nota&#39;s van de Versie van het Doel - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
