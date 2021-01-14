---
keywords: reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Rapporten bevatten informatie over de prestaties van je Adobe Target-activiteiten
title: Rapporten
feature: Reports
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---


# Rapporten{#reports}

De rapporten verstrekken informatie over de vooruitgang en de resultaten van uw [!DNL Adobe Target] activiteiten die u helpen besluiten nemen die op uw gegevens worden gebaseerd. Met behulp van rapportgegevens kunt u bepalen wanneer een activiteit moet worden beëindigd, u laten zien welke ervaring met het aanbieden de winnaar is en kunt u inzichten of lessen bieden die u nodig hebt om de volgende acties te bepalen.

## Een rapport {#section_C4591A32F6D04C95A1AD5A377C27C28B} weergeven

1. Klik **[!UICONTROL Activities]**, dan klik de gewenste activiteit van de lijst.

   Als u veel activiteiten hebt, kunt u de lijst filteren door opties te selecteren in de vervolgkeuzelijsten [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] en [!UICONTROL Activity Source].

   U kunt bijvoorbeeld [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] selecteren in de vervolgkeuzelijst [!UICONTROL Type] en [!UICONTROL Live] in de vervolgkeuzelijst [!UICONTROL Status] om alleen A/B-tests en Experience Targeting-activiteiten weer te geven die actief zijn.

   In de volgende afbeelding ziet u de vervolgkeuzelijst [!UICONTROL Type] met twee geselecteerde typen: [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting]. De drie typen A/B-tests (Handmatig, [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) en [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md)) zijn standaard geselecteerd. U kunt desgewenst een of meer typen deselecteren.

   ![Rapporten filteren op type](/help/c-reports/assets/report_filters-new.png)

1. Klik op het tabblad **[!UICONTROL Reports]**.

   Elk rapport bevat een legenda om u te helpen het rapport te begrijpen.

   ![Legenda rapporteren](/help/c-reports/assets/report_menu_bar-new.png)

   De legenda geeft de volgende informatie weer:

   * De status van de activiteit, inclusief het datumbereik waarop de activiteit werd uitgevoerd.
   * De [geprojecteerde winnende ervaring](/help/c-activities/automated-traffic-allocation/determine-winner.md) (indien beschikbaar).

   >[!NOTE]
   >
   >Ervaringsresultaten verschijnen nadat ten minste één kandidaat de ervaring heeft gezien.

1. (Optioneel) [Configureer het rapport](/help/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) naar wens.
1. (Optioneel) [Download het rapport in CSV-indeling](/help/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) voor analyse in Excel en andere tools.

   De volgende opties zijn beschikbaar:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Optioneel) Klik op de pictogrammen **[!UICONTROL Table View]** en **[!UICONTROL Graph View]** om te schakelen tussen de rapporteringsindelingen.

   ![Pictogrammen voor tabel- en grafiekweergave](/help/c-reports/assets/table-and-graph-icons.png)

   Afhankelijk van het type rapport dat u hebt geselecteerd, zijn mogelijk andere weergaven en rapporten beschikbaar:

   | Rapporttype | Weergave |
   | --- | --- |
   | [Automatisch doel](/help/c-activities/auto-target/auto-target-to-optimize.md) | Klik op de pictogrammen **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]**.<ul><li>Het [Rapport Geautomatiseerde Segmenten](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend aan de aanbiedingen/ervaringen in uw AP/AT activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.</li><li>Het [Belangrijke rapport van Attributen](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Naast de [Samenvattingsrapporten van Automated Personalization](/help/c-reports/reports-ap.md), kunt u **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]** pictogrammen klikken.<ul><li>Het [Rapport Geautomatiseerde Segmenten](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend aan de aanbiedingen/ervaringen in uw AP/AT activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.</li><li>Het [Belangrijke rapport van Attributen](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [Multivariatietest](/help/c-activities/c-multivariate-testing/multivariate-testing.md)  (MVT) | Naast [Experience Performance report](/help/c-reports/experience-performance-report.md) kunt u op het pictogram [Location Contribution](/help/c-reports/location-contribution-report.md) klikken om het rapport om de bijdrage per locatie weer te geven. |

## Aanvullende rapportageinformatie voor specifieke activiteitstypen {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Naast de algemene rapporteringsinformatie in dit onderwerp en zijn subtopics, is de extra informatie specifiek voor individuele activiteitentypes elders in deze gids beschikbaar:

| Type activiteit | Details |
|--- |--- |
| [A/B-test](/help/c-activities/t-test-ab/test-ab.md) | Zie [Een A/B-test plannen](/help/c-activities/t-test-ab/sample-size-determination.md) om inzicht te krijgen in lift en vertrouwen en de statistische benaderingen die worden gebruikt in [!DNL Target]. |
| [Rapporten automatisch toewijzen interpreteren](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Interpreteer de resultaten van een [!UICONTROL Auto-Allocate] A/B activiteit door belangrijke indicatoren, met inbegrip van lift en vertrouwen, in [!DNL Target] UI te onderzoeken. |
| [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md)  (AT) | Informatie over het [!UICONTROL Summary] rapport voor AT activiteiten. Zie [Samenvattingsrapport autom. doel](/help/c-reports/auto-target-summary-report.md) voor meer informatie.<br>Informatie over de twee  [!UICONTROL Personalization Insights] rapporten voor AT en AP activiteiten:  [!UICONTROL Automated Segments] verslag en  [!UICONTROL Important Attributes] verslag. Voor meer informatie, zie [Rapporten van de Inzichten van de Personalisatie](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informatie over de twee [!UICONTROL Automated Personalization Summary] rapporten voor AP activiteiten: [!UICONTROL Activity Level]-rapport en [!UICONTROL Offer Level]-rapport. Zie [Samenvattingsrapporten van Automated Personalization](/help/c-reports/reports-ap.md) voor meer informatie.<br>Informatie over de twee  [!UICONTROL Personalization Insights] rapporten voor AT en AP activiteiten:  [!UICONTROL Automated Segments] verslag en  [!UICONTROL Important Attributes] verslag. Voor meer informatie, zie [Rapporten van de Inzichten van de Personalisatie](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Multivariatietest](/help/c-activities/c-multivariate-testing/multivariate-testing.md)  (MVT) | Informatie over de twee verslagen over MVT-activiteiten: [!UICONTROL Experience Performance] rapport en [!UICONTROL Location Contribution] rapport. Zie [Experience Performance Report](/help/c-reports/experience-performance-report.md) (MVT) en [Location Contribution Report](/help/c-reports/location-contribution-report.md) (MVT) voor meer informatie. |
| [Adobe Analytics als rapportagebron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md)  (A4T) | Informatie over het gebruik van [!DNL Adobe Analytics] als rapportagebron voor [!DNL Target]. A4T geeft u toegang tot [!DNL Analytics] rapporten voor uw [!DNL Target] activiteiten. Zie [Analytics for Target (A4T) Reporting](/help/c-reports/analytics-for-target-a4t-reporting.md) voor meer informatie. |

## Blokrapportgegevens van opgegeven IP-adressen

U kunt bezoekers van gespecificeerde IP adressen van worden geteld in rapporten blokkeren. Dit is bijvoorbeeld handig om rapportgegevens van uw interne bezoekers te blokkeren.

[Contact opnemen met Client ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Careto-set met IP-filters. Dit filtreren is niet van toepassing wanneer het gebruiken van [Analytics voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als uw rapporteringsbron.
