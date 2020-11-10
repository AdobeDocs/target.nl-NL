---
keywords: Targeting;AP reports;automated personalization reports;activity level report;offer level report;offer detail report
description: Speciale rapporten zijn beschikbaar voor gebruikers van Automated Personalization-activiteiten in Adobe Target.
title: Samenvattingsrapporten van Automated Personalization
feature: reports
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Automated Personalization Summary-rapporten{#automated-personalization-summary-reports}

De gespecialiseerde rapporten zijn beschikbaar aan gebruikers van [!UICONTROL Automated Personalization] activiteiten in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Het is niet inbegrepen met [!DNL Target Standard] zonder een [vergunning](/help/c-intro/intro.md#premium)van de Premie van het Doel.

1. Klik **[!UICONTROL Activities]**, klik de gewenste [!UICONTROL Automated Personalization] activiteit van de lijst, dan klik de **[!UICONTROL Reports]** tabel.

   Als u veel activiteiten hebt, kunt u de lijst filteren door [!UICONTROL Automated Personalization] in de [!UICONTROL Type] vervolgkeuzelijst te selecteren.

1. (Optioneel) Klik op het [!UICONTROL Download] pictogram om de overzichtsweergave te downloaden (bijvoorbeeld door Control en gericht verkeer te vergelijken), onderverdeeld op basis van alle beschikbare succesmetingen.

[!UICONTROL Automated Personalization] bevat de volgende rapporten:

## Rapport over activiteitsniveau {#section_6F72FC5C790B4492B3DCECBFFA971337}

Het [!UICONTROL Activity Level] rapport vergelijkt de gezamenlijke prestaties van het gebruiken van een [!UICONTROL Automated Personalization] algoritme met willekeurig gediende inhoud (controle).

![Rapport over activiteitsniveau](/help/c-reports/assets/box_plot_ap.png)

De standaardregels voor de interpretatie van resultaten voor A/B-tests zijn nog steeds van toepassing, zoals lift, betrouwbaarheid, trending, duur, enzovoort. Zie [Informatie over de conversiesnelheid](/help/c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844)voor meer informatie over het interpreteren van resultaten.

## Rapport op aanbodniveau {#section_CAA6409879E349C6906E2BE8156D87A1}

Het [!UICONTROL Offer Level] rapport voor de Willekeurige Boservaring vergelijkt de prestaties van elk algoritme-toegepast aanbod aan het zelfde willekeurig gediende aanbod (Controle). Daarom mogen de aanbiedingen in dit verband niet met elkaar worden vergeleken.

Klik op het ervaringsalgoritme (Willekeurig bos of besturingselement) om het [!UICONTROL Offer Level] rapport weer te geven.

![](assets/ap_OfferLevelRpt.png)

De aanbiedingen kunnen binnen rapportgroepen worden getoond, en deze rapportgroepen kunnen worden doen ineenstorten en worden uitgebreid. Selecteer [!UICONTROL Reporting Group] in de drop-down lijst aan mening opgerolde informatie door rapporteringsgroepen, eerder dan door aanbiedingen.

>[!NOTE]
>
>Het klokpictogram wijst erop dat het algoritmemodel nog bouwt. Het vinkje geeft aan dat het basisalgoritme is ingesteld.

## Geautomatiseerde segmenten

Klik op het [!UICONTROL Automated Segments] pictogram. Dit rapport laat zien hoe verschillende bezoekers anders reageren op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

![Pictogram Automatisch segment](/help/c-reports/assets/icon-automated-sements-ap.png)

Voor meer informatie, zie het [Geautomatiseerde rapport](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md)van Segmenten.

## Belangrijke kenmerken

Klik op het [!UICONTROL Important Attributes] pictogram. Dit rapport toont aan hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

![Pictogram Belangrijke kenmerken](/help/c-reports/assets/icon-important-attributes-ap.png)

Voor meer informatie, zie het [Belangrijke rapport](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md)van Attributen.