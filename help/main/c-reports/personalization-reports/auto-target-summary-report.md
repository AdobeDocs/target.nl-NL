---
keywords: rapporten;autoTarget;autoTarget;AT;report
description: Leer hoe u het rapport Overzicht autom. doel in Adobe Target interpreteert. U kunt op de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen van dit rapport schakelen.
title: Hoe gebruik ik het overzichtsrapport voor automatische doelen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Reports
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# [!UICONTROL Auto-Target Summary report]

Informatie over het interpreteren van de [!UICONTROL Auto-Target Summary] -rapporten in [!DNL Adobe Target] .

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. Het is niet inbegrepen met [!DNL Target Standard] zonder a [&#x200B; Target Premium vergunning &#x200B;](/help/main/c-intro/intro.md#premium).

De [!UICONTROL Auto-Target Summary] -rapporten weergeven:

1. Klik op de pagina [!UICONTROL Activities] op de gewenste [!UICONTROL Auto-Target] -activiteit.

   Als u vele activiteiten hebt, klik het pictogram van de Filter ( ![&#x200B; pictogram van de Filter &#x200B;](/help/main/assets/icons/Filter.svg)) om de lijst te filtreren door opties van [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] drop-down lijsten te selecteren.

1. Klik op de tab **[!UICONTROL Reports]** en klik vervolgens op het gewenste pictogram:

   * **[!UICONTROL Table View]** ( ![&#x200B; pictogram van de Mening van de Lijst &#x200B;](/help/main/assets/icons/Table.svg) )
   * **[!UICONTROL Graph View]** ( ![&#x200B; pictogram van de Mening van de Grafiek &#x200B;](/help/main/assets/icons/GraphTrend.svg))
   * **[!UICONTROL Automated Segments]** ( ![&#x200B; Geautomatiseerd rapport van Segmenten &#x200B;](/help/main/assets/icons/AutomatedSegment.svg))
   * [!UICONTROL Important Attributes] ** ( ![&#x200B; Belangrijk pictogram van Attributen &#x200B;](/help/main/assets/icons/ViewList.svg) )

## Tabelweergave

Tijdens het interpreteren van uw [!UICONTROL Auto-Target] -rapporten kunt u enkele tips en overwegingen opgeven:

* De verschillende rijen in de tabel helpen u de prestaties van de activiteit te begrijpen.

   * De bovenste twee rijen in de tabel op de rapportagepagina tonen de resultaten van een A/B-test tussen de bezoekers die aan het besturingselement zijn toegewezen (dat wil zeggen, willekeurig bediende ervaringen) en de bezoekers die aan het verpersoonlijkingsalgoritme zijn toegewezen. Deze informatie kan worden gebruikt om te meten hoe het verpersoonlijkingsalgoritme in vergelijking met de willekeurig gediende controle uitvoerde.
   * De resterende rijen tonen resultaten op ervaringsniveau. Voor elke ervaring is er een vergelijking tussen de gemiddelde respons van bezoekers die deze ervaring als een willekeurig bediende controle hebben getoond, en de gemiddelde respons van bezoekers die de ervaring met het personalisatiealgoritme hebben getoond.

* Het groene controlepictogram naast elke ervaring in het rapport geeft aan dat er een gepersonaliseerd model voor machinaal leren is gegenereerd voor die ervaring. Het klokpictogram wijst erop dat niet genoeg verkeer is gediend om het model te bouwen.

   * Omdat het model per ervaring wordt gebouwd, is het mogelijk om een model voor sommige ervaringen met een groene controle en anderen met een klokpictogram te zien.
   * In dit geval, om de snelheid van de activiteit te verhogen die modellen heeft voor alle ervaringen worden gebouwd, wordt het extra verkeer verzonden naar ervaringen met ongebouwde modellen.
   * Er moeten ten minste twee ervaringen zijn met ingebouwde modellen (groen vinkje) voordat u kunt beginnen met personaliseren.

* Het vergelijken van de conversiesnelheid van ervaring A met ervaring B is niet de juiste vergelijking in [!UICONTROL Auto-Target] . De vraag is of ervaring A beter presteert wanneer op een intelligente manier dan een willekeurige manier wordt gediend (met andere woorden, tegenover de controle). Marketers moeten ook voorzichtig zijn met het interpreteren van de liften van individuele ervaringen, omdat het verpersoonlijkingsalgoritme probeert de maatstaf voor succes te optimaliseren over de gehele activiteit, niet over elke individuele ervaring.
* Ervaringen met de hoogste lift kunnen worden opgevat als een zo groot mogelijke differentiatie binnen de bevolking. Dat wil zeggen, het algoritme heeft een segment gevonden dat die specifieke ervaring het meest leuk vindt.
* De verschillende kolommen in de tabel geven het aantal bezoeken, de omrekeningskoers, de gemiddelde lift en het betrouwbaarheidsniveau en het vertrouwen weer. Voor meer informatie, zie [&#x200B; Statistische berekeningen in tests A/B &#x200B;](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Grafiekweergave

Gebruik de twee vervolgkeuzelijsten om de gewenste metriek, telmethode en meer te kiezen. Zie [&#x200B; overzicht van de montages van het Rapport &#x200B;](/help/main/c-reports/c-report-settings/report-settings.md) voor meer informatie:

## Geautomatiseerde segmenten

Dit rapport laat zien hoe verschillende bezoekers anders reageren op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

Voor meer informatie, zie het [&#x200B; Geautomatiseerde rapport van Segmenten &#x200B;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Belangrijke kenmerken

Dit rapport toont aan hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

Voor meer informatie, zie het [&#x200B; Belangrijke rapport van Attributen &#x200B;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).
