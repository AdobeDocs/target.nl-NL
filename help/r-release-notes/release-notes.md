---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en bibliotheken JavaScript.
title: Welke nieuwe eigenschappen worden inbegrepen in de huidige Versie?
feature: Opmerkingen bij de release
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 29b8bf64b0ce4e7e830d9fff5341849799072dfa
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard]- en [!DNL Target Premium]-versie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].)

## Target Standard/Premium 21.5.1 (7 juni 2021)

Deze release bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| ![Premium ](/help/assets/premium.png) [!DNL Recommendations] [!UICONTROL Catalog Search] badgeAPI | Zoek in uw [!DNL Recommendations] product- en inhoudscatalogus via de API programmatisch naar items die voldoen aan een zoekcriterium en vereenvoudig het beheer van uw catalogus.<br>**Beperkingen en opmerkingen**:<ul><li>Cataloguszoekopdrachten via API worden niet ondersteund voor omgevingen met meer dan 2.000.000 items.</li><li>Zoekresultaten van catalogi via API worden sneller bijgewerkt dan zoekresultaten van catalogi via de gebruikersinterface [!DNL Target]. Het zoeken naar catalogi in de interface [!DNL Target] kan extra tijd vergen om de meest recente resultaten weer te geven.</li></ul>Zie [Zoeken in entiteiten](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) in de handleiding *[!DNL Adobe Target][!DNL Recommendations] API* voor meer informatie. |

Deze release voor onderhoudsdoeleinden bevat de volgende oplossingen.

* Probleem verholpen waarbij de standaardwerkruimte werd gewijzigd in een andere werkruimte tijdens het vernieuwen van de pagina [!UICONTROL Audiences]. (TGT-38871)
* Probleem verholpen in [!UICONTROL Administration] > [!UICONTROL Implementation] die soms een foutbericht veroorzaakte met de tekst &quot;Uw globale box is mogelijk niet synchroon. Probeer het opnieuw op te slaan.&quot;

## ![Adobe Experience Platform Web SDK ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] badgeversion 2.5.0 (1 juni 2021)

Deze versie van [!DNL Platform Web SDK] omvat steun voor het volgende:

| Functie | Details |
| --- | --- |
| Ondersteuning omleiden met [!UICONTROL Analytics for Target] (A4T) | De SDK van het Web van het Platform steunt nu [!DNL Target] omleidingen wanneer het gebruiken [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Zie  [Analytics  [!DNL Target] for implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) voor meer informatie. |

## at.js versie 2.5.0 (13 mei 2021)

Deze versie van at.js bevat de volgende verbeteringen en wijzigingen:

* [Ondersteuning voor ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) beslissingen op het apparaat voor at.js.
* [Ondersteuning voor ](/help/c-activities/c-activity-qa/activity-qa.md) koppelingen voorvertonen voor Automated Personalization-activiteiten

Deze versie verwijdert ook ondersteuning voor Microsoft Internet Explorer 10, Internet Explorer 11 en alle oudere versies. Microsoft Edge wordt nog steeds ondersteund in at.js 2.5.0 en hoger.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
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
