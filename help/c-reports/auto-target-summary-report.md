---
keywords: reports;auto-target;auto target;AT;report
description: Informatie over hoe te om het auto-Doel Summiere rapport in Adobe Target te interpreteren.
title: Samenvattingsrapport voor automatisch doel
feature: reports
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Auto-Target Summary-rapport{#auto-target-summary-report}

Informatie over de interpretatie van de [!UICONTROL Auto-Target Summary] rapporten in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Het is niet inbegrepen met [!DNL Target Standard] zonder een [vergunning](/help/c-intro/intro.md#premium)van de Premie van het Doel.

De [!UICONTROL Auto-Target Summary] rapporten weergeven:

1. Klik op de [!UICONTROL Activities] pagina op de gewenste [!UICONTROL Auto-Target] activiteit.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] drop-down lijsten te selecteren.

1. Klik op het [!UICONTROL Reports] tabblad en klik vervolgens op het gewenste pictogram:

   * Tabelweergave
   * Grafiekweergave
   * Geautomatiseerde segmenten
   * Belangrijke kenmerken

## Tabelweergave

In de volgende afbeelding ziet u hoe een typisch samenvattingsrapport eruit ziet [!UICONTROL Table View] wanneer u het rapport van een [!UICONTROL Auto-Target] activiteit bekijkt:

![Rapport voor automatisch doeltabelweergave](/help/c-reports/assets/at-table-view.png)

Tijdens het interpreteren van uw [!UICONTROL Auto-Target] rapporten kunt u enkele tips en overwegingen opgeven:

* De verschillende rijen in de tabel helpen u de prestaties van de activiteit te begrijpen.

   * De bovenste twee rijen in de tabel op de rapportagepagina tonen de resultaten van een A/B-test tussen de bezoekers die aan het besturingselement waren toegewezen (d.w.z. willekeurig bediende ervaringen) en de bezoekers die aan het verpersoonlijkingsalgoritme werden toegewezen. Deze informatie kan worden gebruikt om te meten hoe het verpersoonlijkingsalgoritme in vergelijking met de willekeurig-gediende controle uitvoerde.
   * De resterende rijen tonen resultaten op ervaringsniveau. Voor elke ervaring is er een vergelijking tussen de gemiddelde respons van bezoekers die deze ervaring als een willekeurig bediende controle hebben getoond, en de gemiddelde respons van bezoekers die de ervaring met het personalisatiealgoritme hebben getoond.

* Het groene controlepictogram naast elke ervaring in het rapport geeft aan dat er een gepersonaliseerd model voor machinaal leren is gegenereerd voor die ervaring. Het klokpictogram wijst erop dat niet genoeg verkeer is gediend om het model te bouwen.

   * Omdat het model per ervaring wordt gebouwd, is het mogelijk om een model voor sommige ervaringen met een groene controle en anderen met een klokpictogram te zien.
   * In dit geval, om de snelheid van de activiteit te verhogen die modellen heeft voor alle ervaringen worden gebouwd, wordt het extra verkeer verzonden naar ervaringen met ongebouwde modellen.
   * Er moeten ten minste twee ervaringen zijn met ingebouwde modellen (groen vinkje) voordat de personalisatie kan beginnen.

* Het vergelijken van de omrekeningskoers van ervaring A met ervaring B is niet de juiste vergelijking [!UICONTROL Auto-Target]. De vraag is of ervaring A beter presteert wanneer op een intelligente manier dan een willekeurige manier wordt gediend (met andere woorden, tegenover de controle). Marketers moeten ook voorzichtig zijn met het interpreteren van de liften van individuele ervaringen, omdat het verpersoonlijkingsalgoritme probeert de maatstaf voor succes te optimaliseren over de gehele activiteit, niet over elke individuele ervaring.
* Ervaringen met de hoogste lift kunnen worden opgevat als een zo groot mogelijke differentiatie binnen de bevolking. Dat is het algoritme heeft een segment gevonden dat het meest van die specifieke ervaring houdt.
* De verschillende kolommen in de tabel geven het aantal bezoeken, de omrekeningskoers, de gemiddelde lift en het betrouwbaarheidsniveau en het vertrouwen weer. Voor meer informatie, zie [Gemiddelde Lift, Lift Bounds, en het Interval](/help/c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md)van het Vertrouwen.

## Grafiekweergave

In de volgende afbeelding ziet u hoe een typisch samenvattingsrapport eruit ziet [!UICONTROL Graph View] wanneer u het rapport van een [!UICONTROL Auto-Target] activiteit bekijkt:

![Rapport voor automatisch doelgrafiekweergave](/help/c-reports/assets/at-graph-view.png)

Zoals hieronder getoond, kunt u de twee drop-down lijsten gebruiken om de gewenste metriek, telmethodiek, en meer te kiezen. Zie Overzicht [van](/help/c-reports/c-report-settings/report-settings.md) rapportinstellingen voor meer informatie:

![Rapport voor automatisch doelgrafiekweergave](/help/c-reports/assets/at-graph-view-2.png)

## Geautomatiseerde segmenten

Klik op het [!UICONTROL Automated Segments] pictogram. Dit rapport laat zien hoe verschillende bezoekers anders reageren op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

![Pictogram Automatisch segment](/help/c-reports/assets/icon-automated-sements.png)

Voor meer informatie, zie het [Geautomatiseerde rapport](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md)van Segmenten.

## Belangrijke kenmerken

Klik op het [!UICONTROL Important Attributes] pictogram. Dit rapport toont aan hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

![Pictogram Belangrijke kenmerken](/help/c-reports/assets/icon-important-attributes.png)

Voor meer informatie, zie het [Belangrijke rapport](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md)van Attributen.
