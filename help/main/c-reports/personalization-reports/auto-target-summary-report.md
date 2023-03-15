---
keywords: rapporten;autoTarget;autoTarget;AT;report
description: Leer hoe u het rapport Overzicht autom. doel in Adobe Target interpreteert. U kunt op de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen van dit rapport schakelen.
title: Hoe gebruik ik het overzichtsrapport voor automatische doelen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 0%

---

# Samenvattingsrapport voor automatisch doel

Informatie over hoe u de [!UICONTROL Auto-Target Summary] rapporten in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Het is niet opgenomen in [!DNL Target Standard] zonder [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium).

Als u het dialoogvenster [!UICONTROL Auto-Target Summary] rapporten:

1. Van de [!UICONTROL Activities] pagina, klikt u op de gewenste [!UICONTROL Auto-Target] activiteit.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van te selecteren [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] vervolgkeuzelijsten.

1. Klik op de knop [!UICONTROL Reports] en klikt u op het gewenste pictogram:

   * Tabelweergave
   * Grafiekweergave
   * Geautomatiseerde segmenten
   * Belangrijke kenmerken

## Tabelweergave

De volgende illustratie laat zien hoe een typisch samenvattingsrapport er uitziet in [!UICONTROL Table View] wanneer u een [!UICONTROL Auto-Target] activiteitenverslag:

![Rapport voor automatisch doeltabelweergave](/help/main/c-reports/assets/at-table-view.png)

Tijdens het interpreteren van uw [!UICONTROL Auto-Target] rapporten:

* De verschillende rijen in de tabel geven inzicht in de prestaties van de activiteit.

   * De bovenste twee rijen in de tabel op de rapportagepagina tonen de resultaten van een A/B-test tussen de bezoekers die aan het besturingselement waren toegewezen (d.w.z. willekeurig bediende ervaringen) en de bezoekers die aan het verpersoonlijkingsalgoritme werden toegewezen. Deze informatie kan worden gebruikt om te meten hoe het verpersoonlijkingsalgoritme in vergelijking met de willekeurig-gediende controle uitvoerde.
   * De resterende rijen tonen resultaten op ervaringsniveau. Voor elke ervaring is er een vergelijking tussen de gemiddelde respons van bezoekers die deze ervaring als een willekeurig bediende controle hebben getoond, en de gemiddelde respons van bezoekers die de ervaring met het personalisatiealgoritme hebben getoond.

* Het groene controlepictogram naast elke ervaring in het rapport geeft aan dat er een gepersonaliseerd model voor machinaal leren is gegenereerd voor die ervaring. Het klokpictogram wijst erop dat niet genoeg verkeer is gediend om het model te bouwen.

   * Omdat het model per ervaring wordt gebouwd, is het mogelijk om een model voor sommige ervaringen met een groene controle en anderen met een klokpictogram te zien.
   * In dit geval, om de snelheid van de activiteit te verhogen die modellen heeft voor alle ervaringen worden gebouwd, wordt het extra verkeer verzonden naar ervaringen met ongebouwde modellen.
   * Er moeten ten minste twee ervaringen zijn met ingebouwde modellen (groen vinkje) voordat de personalisatie kan beginnen.

* Het vergelijken van de omrekeningskoers van ervaring A met ervaring B is niet de juiste vergelijking [!UICONTROL Auto-Target]. De vraag is of ervaring A beter presteert wanneer op een intelligente manier dan een willekeurige manier wordt gediend (met andere woorden, tegenover de controle). Marketers moeten ook voorzichtig zijn met het interpreteren van de liften van individuele ervaringen, omdat het verpersoonlijkingsalgoritme probeert de maatstaf voor succes te optimaliseren over de gehele activiteit, niet over elke individuele ervaring.
* Ervaringen met de hoogste lift kunnen worden opgevat als een zo groot mogelijke differentiatie binnen de bevolking. Dat is het algoritme heeft een segment gevonden dat het meest van die specifieke ervaring houdt.
* De verschillende kolommen in de tabel geven het aantal bezoeken, de omrekeningskoers, de gemiddelde lift en het betrouwbaarheidsniveau en het vertrouwen weer. Zie voor meer informatie [Statistische berekeningen in A/B-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Grafiekweergave

De volgende illustratie laat zien hoe een typisch samenvattingsrapport er uitziet in [!UICONTROL Graph View] wanneer u een [!UICONTROL Auto-Target] activiteitenverslag:

![Rapport voor automatisch doelgrafiekweergave](/help/main/c-reports/assets/at-graph-view.png)

Zoals hieronder getoond, kunt u de twee drop-down lijsten gebruiken om de gewenste metriek, telmethodiek, en meer te kiezen. Zie [Overzicht van rapportinstellingen](/help/main/c-reports/c-report-settings/report-settings.md) voor meer informatie :

![Rapport voor automatisch doelgrafiekweergave](/help/main/c-reports/assets/at-graph-view-2.png)

## Geautomatiseerde segmenten

Klik op de knop [!UICONTROL Automated Segments] pictogram. Dit rapport laat zien hoe verschillende bezoekers anders reageren op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

![Pictogram Automatisch segment](/help/main/c-reports/assets/icon-automated-sements.png)

Zie voor meer informatie [Rapport Automated Segments](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Belangrijke kenmerken

Klik op de knop [!UICONTROL Important Attributes] pictogram. Dit rapport toont aan hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

![Pictogram Belangrijke kenmerken](/help/main/c-reports/assets/icon-important-attributes.png)

Zie voor meer informatie [Rapport Belangrijke kenmerken](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).
