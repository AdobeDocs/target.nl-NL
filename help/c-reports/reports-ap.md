---
keywords: Targeting;AP reports;automated personalization reports;activity level report;offer level report;offer detail report
description: Speciale rapporten zijn beschikbaar voor gebruikers van Automated Personalization-activiteiten in Adobe Target.
title: Samenvattingsrapporten van Automated Personalization
feature: Reports
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# ![Samenvattingsrapporten ](/help/assets/premium.png) PREMIUMAutomated Personalization{#automated-personalization-summary-reports}

De gespecialiseerde rapporten zijn beschikbaar aan gebruikers van [!UICONTROL Automated Personalization] activiteiten in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de  [!DNL Target Premium] oplossing. Het is niet inbegrepen met [!DNL Target Standard] zonder een [vergunning van de Premie van het Doel](/help/c-intro/intro.md#premium).

1. Klik **[!UICONTROL Activities]**, klik de gewenste [!UICONTROL Automated Personalization] activiteit van de lijst, dan klik **[!UICONTROL Reports]** tabel.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door [!UICONTROL Automated Personalization] van [!UICONTROL Type] drop-down lijst te selecteren.

1. (Optioneel) Klik op het pictogram [!UICONTROL Download] om de overzichtsweergave te downloaden (bijvoorbeeld door Control en gericht verkeer te vergelijken), onderverdeeld op basis van alle beschikbare succeswaarden.

[!UICONTROL Automated Personalization] bevat de volgende rapporten:

## Rapport over activiteitsniveau {#section_6F72FC5C790B4492B3DCECBFFA971337}

Het [!UICONTROL Activity Level] rapport vergelijkt de gezamenlijke prestaties van het gebruiken van een [!UICONTROL Automated Personalization] algoritme aan willekeurig gediende inhoud (controle).

![Rapport over activiteitsniveau](/help/c-reports/assets/box_plot_ap.png)

De standaardregels voor de interpretatie van resultaten voor A/B-tests zijn nog steeds van toepassing, zoals lift, betrouwbaarheid, trending, duur, enzovoort. Voor meer informatie over het interpreteren van resultaten, zie [Ongeveer het Tarief van de Omzetting](/help/c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844).

## Rapport Aanbiedingsniveau {#section_CAA6409879E349C6906E2BE8156D87A1}

Het [!UICONTROL Offer Level] rapport voor de Willekeurige Boservaring vergelijkt de prestaties van elk algoritme-toegepaste aanbieding aan het zelfde willekeurig gediende aanbod (Controle). Daarom mogen de aanbiedingen in dit verband niet met elkaar worden vergeleken.

Klik op het ervaringsalgoritme (Willekeurig bos of besturingselement) om het [!UICONTROL Offer Level]-rapport weer te geven.

![](assets/ap_OfferLevelRpt.png)

De aanbiedingen kunnen binnen rapportgroepen worden getoond, en deze rapportgroepen kunnen worden doen ineenstorten en worden uitgebreid. Selecteer [!UICONTROL Reporting Group] in de drop-down lijst aan mening opgerolde informatie door rapporteringsgroepen, eerder dan door aanbiedingen.

>[!NOTE]
>
>Het klokpictogram wijst erop dat het algoritmemodel nog bouwt. Het vinkje geeft aan dat het basisalgoritme is ingesteld.

## Geautomatiseerde segmenten

Klik op het pictogram [!UICONTROL Automated Segments]. Dit rapport laat zien hoe verschillende bezoekers anders reageren op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

![Pictogram Automatisch segment](/help/c-reports/assets/icon-automated-sements-ap.png)

Zie [Rapport Automated Segments](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) voor meer informatie.

## Belangrijke kenmerken

Klik op het pictogram [!UICONTROL Important Attributes]. Dit rapport toont aan hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

![Pictogram Belangrijke kenmerken](/help/c-reports/assets/icon-important-attributes-ap.png)

Voor meer informatie, zie [Belangrijk rapport van Attributen](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).