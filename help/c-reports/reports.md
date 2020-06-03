---
keywords: reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Rapporten bevatten informatie over de prestaties van uw activiteiten
title: Rapporten
subtopic: Multivariate Test
topic: Standard
uuid: 8d20f4e7-72fd-4872-a21f-54ce16a2d2ab
translation-type: tm+mt
source-git-commit: 316c1157a4dff346f16862cfd7a04994c6a1bc7d
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---


# Rapporten{#reports}

De rapporten verstrekken informatie over de vooruitgang en de resultaten van uw activiteiten die u helpen besluiten nemen die op uw gegevens worden gebaseerd. Met behulp van rapportgegevens kunt u bepalen wanneer een test moet worden beëindigd, u laten zien welke ervaring met de aanbieding de winnaar is en kunt u inzichten of lessen bieden die u nodig hebt om de volgende acties te bepalen.

>[!NOTE]
>
>U kunt bezoekers van gespecificeerde IP adressen van worden geteld in rapporten blokkeren. Contact opnemen met de klantenservice om IP-filters in te stellen. Dit filtreren is niet van toepassing wanneer het gebruiken van [Analytics voor Doel](../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als uw rapporteringsbron.

## Rapportage-informatie voor specifieke soorten activiteiten {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Naast de algemene rapporteringsinformatie in dit onderwerp en zijn subtopics, is de extra informatie specifiek voor individuele activiteitentypes elders in deze gids beschikbaar:

| Type activiteit | Details |
|--- |--- |
| [A/B-test](/help/c-activities/t-test-ab/test-ab.md) | Om inzicht te krijgen in de lift en het vertrouwen en de statistische benaderingen die in [!DNL Target]dit verband worden gebruikt, zie [Plan een A/B-test](/help/c-activities/t-test-ab/sample-size-determination.md). |
| [Rapporten automatisch toewijzen interpreteren](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Interpreeer de resultaten van een auto-Wijs A/B activiteit door belangrijke indicatoren, met inbegrip van lift en vertrouwen, in het Doel UI te onderzoeken. |
| [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) | Informatie over het [!UICONTROL Summary] verslag voor AT-activiteiten. Voor meer informatie, zie [auto-Doel Samenvattingsrapport](/help/c-reports/auto-target-summary-report.md).<br>Informatie over de twee [!UICONTROL Personalization Insights] rapporten voor AT en AP activiteiten: [!UICONTROL Automated Segments] verslag en [!UICONTROL Important Attributes] verslag. Zie [Persoonlijkheidsrapporten](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md)voor meer informatie. |
| [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informatie over de twee [!UICONTROL Automated Personalization Summary] rapporten voor AP-activiteiten: [!UICONTROL Activity Level] verslag en [!UICONTROL Offer Level] verslag. Voor meer informatie, zie de [Geautomatiseerde Rapporten](/help/c-reports/reports-ap.md)van het Overzicht van de Personalisatie.<br>Informatie over de twee [!UICONTROL Personalization Insights] rapporten voor AT en AP activiteiten: [!UICONTROL Automated Segments] verslag en [!UICONTROL Important Attributes] verslag. Zie [Persoonlijkheidsrapporten](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md)voor meer informatie. |
| [Multivariatietest](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informatie over de twee verslagen over MVT-activiteiten: [!UICONTROL Experience Performance] verslag en [!UICONTROL Location Contribution] verslag. Zie [Experience Performance Report](/help/c-reports/experience-performance-report.md) (MVT) en [Location Contribution Report](/help/c-reports/location-contribution-report.md) (MVT) voor meer informatie. |
| [Adobe Analytics as the Reporting Source for Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informatie over het gebruiken [!DNL Adobe Analytics] als rapporteringsbron voor [!DNL Target]. A4T geeft u toegang tot [!DNL Analytics] rapporten voor uw [!DNL Target] activiteiten. Voor meer informatie, zie [Analytics voor Doel (A4T) Rapportering](/help/c-reports/analytics-for-target-a4t-reporting.md). |

## Een rapport weergeven {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Klik **[!UICONTROL Activities]** en klik vervolgens in de lijst op de gewenste activiteit.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] drop-down lijsten te selecteren.

   Bijvoorbeeld, kon u selecteren [!UICONTROL A/B Test] en van de [!UICONTROL Experience Targeting] drop-down lijst en [!UICONTROL Type] van de [!UICONTROL Live] [!UICONTROL Status] drop-down lijst om slechts A/B tests en de Gerichte activiteiten van de Ervaring te tonen die in een actieve staat zijn.

   In de volgende afbeelding ziet u de [!UICONTROL Type] vervolgkeuzelijst met twee geselecteerde typen: Doelstelling A/B-test en -ervaring. De drie typen A/B-tests (Handmatig, [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)en [Automatisch](/help/c-activities/auto-target-to-optimize.md)) zijn standaard geselecteerd. U kunt desgewenst een of meer typen deselecteren.

   ![Rapporten filteren op type](/help/c-reports/assets/report_filters-new.png)

1. Klik op het **[!UICONTROL Reports]** tabblad.

   Elk rapport bevat een legenda om u te helpen het rapport te begrijpen.

   ![Legenda rapporteren](/help/c-reports/assets/report_menu_bar-new.png)

   De legenda geeft de volgende informatie weer:

   * De status van de activiteit, inclusief het datumbereik waarop de activiteit werd uitgevoerd.
   * De [geprojecteerde winnende ervaring](/help/c-activities/automated-traffic-allocation/determine-winner.md) (indien beschikbaar).
   >[!NOTE]
   >
   >Ervaringsresultaten verschijnen nadat ten minste één kandidaat de ervaring heeft gezien.

1. (Optioneel) [Configureer het rapport](../c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA)naar wens.
1. (Optioneel) [Download het rapport in CSV-indeling](../c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) voor analyse in Excel en andere tools.

   De volgende opties zijn beschikbaar:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Optioneel) Klik op de **[!UICONTROL Table View]** pictogrammen en **[!UICONTROL Graph View]** pictogrammen om te schakelen tussen de rapportopmaak.

   Afhankelijk van het type rapport dat u hebt geselecteerd, zijn mogelijk andere weergaven en rapporten beschikbaar:

   | Rapporttype | Weergave |
   | --- | --- |
   | Automatisch doel | Klik op de **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]** pictogrammen.<ul><li>Het [Geautomatiseerde rapport](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) van Segmenten toont hoe de verschillende bezoekers verschillend aan de aanbiedingen/ervaringen in uw AP/AT activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.</li><li>Het rapport [](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) Belangrijke kenmerken toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | Geautomatiseerde Personalisatie (AP) | Naast de rapporten [van het Overzicht van de](/help/c-reports/reports-ap.md)Geautomatiseerde Personalisatie, kunt u de **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]** pictogrammen klikken.<ul><li>Het [Geautomatiseerde rapport](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) van Segmenten toont hoe de verschillende bezoekers verschillend aan de aanbiedingen/ervaringen in uw AP/AT activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.</li><li>Het rapport [](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) Belangrijke kenmerken toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | MVT (Multivariate Test) | Naast het rapport [van de Prestaties van de](/help/c-reports/experience-performance-report.md)Ervaring, kunt u het pictogram van de Bijdrage [van de](/help/c-reports/location-contribution-report.md) Plaats klikken om het rapport te schakelen om bijdrage door plaats te tonen. |
