---
keywords: rapporten;blok ip adres;blok bezoeker van ip adres;download rapporten;csv;rapportering
description: Leer hoe u de rapportfuncties in Adobe gebruikt [!DNL Target] om de prestaties van uw activiteiten te onderzoeken. Maak betere besluiten die op uw gegevens worden gebaseerd om ROI te verhogen.
title: Hoe kan ik rapporten weergeven?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 0%

---

# Rapporten

De rapporten verstrekken informatie over de vooruitgang en de resultaten van uw [!DNL Adobe Target] activiteiten die u helpen besluiten te nemen die op uw gegevens worden gebaseerd. Met behulp van rapportgegevens kunt u bepalen wanneer een activiteit moet worden beëindigd, u laten zien welke ervaring met het aanbieden de winnaar is en kunt u inzichten of lessen bieden die u nodig hebt om de volgende acties te bepalen.

## Een rapport weergeven {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Klikken **[!UICONTROL Activities]** en klikt u vervolgens in de lijst op de gewenste activiteit.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van te selecteren [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] vervolgkeuzelijsten.

   U kunt bijvoorbeeld [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] van de [!UICONTROL Type] vervolgkeuzelijst en [!UICONTROL Live] van de [!UICONTROL Status] vervolgkeuzelijst om alleen A/B-tests en Experience Targeting-activiteiten weer te geven die actief zijn.

   In de volgende afbeelding ziet u de [!UICONTROL Type] vervolgkeuzelijst met twee geselecteerde typen: [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting]. Merk op dat de drie typen A/B-tests (Handmatig), [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), en [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) zijn standaard geselecteerd. U kunt desgewenst een of meer typen deselecteren.

   ![Rapporten filteren op type](/help/main/c-reports/assets/report_filters-new.png)

1. Klik op de knop **[!UICONTROL Reports]** tab.

   Elk rapport bevat een legenda om u te helpen het rapport te begrijpen.

   ![Legenda rapporteren](/help/main/c-reports/assets/report_menu_bar-new.png)

   De legenda geeft de volgende informatie weer:

   * De status van de activiteit, inclusief het datumbereik waarop de activiteit werd uitgevoerd.
   * De [verwachte succesvolle ervaring](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (indien beschikbaar).

   >[!NOTE]
   >
   >Ervaringsresultaten verschijnen nadat ten minste één kandidaat de ervaring heeft gezien.

1. (Optioneel) [Het rapport configureren](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA), naar wens.
1. (Optioneel) [Het rapport downloaden in CSV-indeling](/help/main/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) voor analyse in Excel en andere hulpmiddelen.

   De volgende opties zijn beschikbaar:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Optioneel) Klik op de knop **[!UICONTROL Table View]** en **[!UICONTROL Graph View]** pictogrammen om tussen rapporteringsformaten te schakelen.

   ![Pictogrammen voor tabel- en grafiekweergave](/help/main/c-reports/assets/table-and-graph-icons.png)

   Afhankelijk van het type rapport dat u hebt geselecteerd, zijn mogelijk andere weergaven en rapporten beschikbaar:

   | Rapporttype | Weergave |
   | --- | --- |
   | [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Klik op de knop **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]** pictogrammen.<ul><li>De [Rapport Automated Segments](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend aan de aanbiedingen/ervaringen in uw AP/AT activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.</li><li>De [Rapport Belangrijke kenmerken](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model beslist om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Naast de [Samenvattingsrapporten van Automated Personalization](/help/main/c-reports/reports-ap.md), kunt u op de knop **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]** pictogrammen.<ul><li>De [Rapport Automated Segments](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend aan de aanbiedingen/ervaringen in uw AP/AT activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.</li><li>De [Rapport Belangrijke kenmerken](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker aan zijn hoe het model besluit om zich te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [Multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Naast de [Experience Performance Report](/help/main/c-reports/experience-performance-report.md), kunt u op de knop [Locatiebijdrage](/help/main/c-reports/location-contribution-report.md) pictogram om van het rapport te veranderen om bijdrage door plaats te tonen. |

## Aanvullende rapportage-informatie voor specifieke soorten activiteiten {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Naast de algemene rapporteringsinformatie in dit onderwerp en zijn subtopics, is de extra informatie specifiek voor individuele activiteitentypes elders in deze gids beschikbaar:

| Type activiteit | Details |
|--- |--- |
| [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) | Om inzicht te krijgen in lift en vertrouwen en de statistische benaderingen die worden gebruikt in [!DNL Target], zie [Een A/B-test plannen](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [Rapporten automatisch toewijzen interpreteren](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | De resultaten van een [!UICONTROL Auto-Allocate] A/B-activiteit door belangrijke indicatoren, waaronder lift en vertrouwen, in de [!DNL Target] UI. |
| [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informatie over de [!UICONTROL Summary] verslag voor AT-activiteiten. Zie voor meer informatie [Samenvattingsrapport autom. doel](/help/main/c-reports/auto-target-summary-report.md).<br>Informatie over beide [!UICONTROL Personalization Insights] rapporten voor AT- en AP-activiteiten: [!UICONTROL Automated Segments] verslag en [!UICONTROL Important Attributes] verslag. Zie voor meer informatie [Persoonlijkheidsrapporten](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informatie over beide [!UICONTROL Automated Personalization Summary] rapporten voor AP-activiteiten: [!UICONTROL Activity Level] verslag en [!UICONTROL Offer Level] verslag. Zie voor meer informatie [Samenvattingsrapporten van Automated Personalization](/help/main/c-reports/reports-ap.md).<br>Informatie over beide [!UICONTROL Personalization Insights] rapporten voor AT- en AP-activiteiten: [!UICONTROL Automated Segments] verslag en [!UICONTROL Important Attributes] verslag. Zie voor meer informatie [Persoonlijkheidsrapporten](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informatie over de twee verslagen over MVT-activiteiten: [!UICONTROL Experience Performance] verslag en [!UICONTROL Location Contribution] verslag. Zie voor meer informatie [Experience Performance Report](/help/main/c-reports/experience-performance-report.md) (MVT) en  [Locatiebijdragerapport](/help/main/c-reports/location-contribution-report.md) (MVT). |
| [Adobe Analytics als rapportagebron voor Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informatie over het gebruik [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Target]. A4T geeft u toegang tot [!DNL Analytics] rapporten voor uw [!DNL Target] activiteiten. Zie voor meer informatie [Analyses voor doelrapportage (A4T)](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |

## Blokrapportgegevens van opgegeven IP-adressen

U kunt bezoekers van gespecificeerde IP adressen van worden geteld in rapporten blokkeren. Dit is bijvoorbeeld handig om rapportgegevens van uw interne bezoekers te blokkeren.

[Contact opnemen met de klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om IP-filters in te stellen. Deze filters zijn niet van toepassing bij gebruik [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als uw rapporteringsbron.
