---
keywords: rapporten;blok ip adres;blok bezoeker van ip adres;download rapporten;csv;rapportering
description: Optimaliseer uw activiteiten door  [!DNL Adobe Target] rapporteringseigenschappen te beheersen om besluitvorming te verbeteren en ROI op te voeren.
title: Hoe kan ik rapporten weergeven?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: 5c963e97dae11326396a5c1c5e32d19f4d463c74
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Rapporten

Rapporten bevatten informatie over de voortgang en de resultaten van uw [!DNL Adobe Target] -activiteiten die u helpen beslissingen te nemen op basis van gegevens. Met behulp van rapportgegevens kunt u bepalen wanneer een activiteit moet worden beëindigd, u laten zien welke ervaring of aanbieding de winnaar is en kunt u inzichten of lessen bieden die u nodig hebt om de volgende acties te bepalen.

## Een rapport weergeven {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Klik op **[!UICONTROL Activities]** en klik vervolgens op de gewenste activiteit in de lijst.

   Als u veel activiteiten hebt, kunt u de lijst filteren door opties te selecteren in de vervolgkeuzelijsten [!UICONTROL Type] , [!UICONTROL Status] , [!UICONTROL Reporting Source] , [!UICONTROL Experience Composer] , [!UICONTROL Metrics Type] , [!UICONTROL Decisioning Method] en [!UICONTROL Activity Source] .

   U kunt bijvoorbeeld [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] selecteren in de vervolgkeuzelijst [!UICONTROL Type] en [!UICONTROL Live] in de vervolgkeuzelijst [!UICONTROL Status] om alleen [!UICONTROL A/B Test] - en [!UICONTROL Experience Targeting] -activiteiten weer te geven die actief zijn.

   De volgende afbeelding toont de vervolgkeuzelijst [!UICONTROL Type] met twee geselecteerde typen: [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] . Merk op dat de drie types van Tests A/B (Hand, [ auto-Wijs ](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) toe, en [ auto-Doel ](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) door gebrek worden geselecteerd. U kunt desgewenst een of meer typen deselecteren.

   ![ de rapporten van de Filter door type ](/help/main/c-reports/assets/report_filters-new.png)

1. Selecteer de gewenste activiteit in de lijst.

1. Klik op de tab **[!UICONTROL Reports]** in de linkertrack.

   Elk rapport bevat een legenda om u te helpen het rapport te begrijpen.

   De legenda geeft de volgende informatie weer:

   * De status van de activiteit, inclusief het datumbereik waarop de activiteit werd uitgevoerd.
   * De [ geprojecteerde het winnen ervaring ](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (als beschikbaar).

   >[!NOTE]
   >
   >Ervaringsresultaten worden weergegeven nadat ten minste één kandidaat de ervaring heeft gezien.

1. (Facultatief) [ vorm het rapport ](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA), zoals gewenst.
1. (Facultatief) [ Download het rapport in formaat CSV ](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) voor analyse in Excel en andere hulpmiddelen.

   De volgende opties zijn beschikbaar:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Optioneel) Klik op de pictogrammen **[!UICONTROL Table View]** en **[!UICONTROL Graph View]** om te schakelen tussen de rapportopmaak.

   ![ de meningspictogrammen van de Lijst en van de Grafiek ](/help/main/c-reports/assets/table-and-graph-icons.png)

   Afhankelijk van het type rapport dat u hebt geselecteerd, zijn mogelijk andere weergaven en rapporten beschikbaar:

   | Rapporttype | Weergave |
   | --- | --- |
   | [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Klik op de pictogrammen **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]** .<ul><li>Het [[!UICONTROL Automated Segments] rapport ](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend op de aanbiedingen en ervaringen in uw [!UICONTROL Automated Personalization] of [!UICONTROL Auto-Target] activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen worden gedefinieerd, op de aanbiedingen en ervaringen in de activiteit hebben gereageerd.</li><li>Het [[!UICONTROL Important Attributes] rapport ](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker aan zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Naast de [[!UICONTROL Automated Personalization Summary] rapporten ](/help/main/c-reports/personalization-reports/reports-ap.md), kunt u de **[!UICONTROL Automated Segments]** of **[!UICONTROL Important Attributes]** pictogrammen klikken.<ul><li>Het [[!UICONTROL Automated Segments] rapport ](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend op de aanbiedingen en ervaringen in uw [!UICONTROL Automated Personalization] of [!UICONTROL Auto-Target] activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen worden gedefinieerd, op de aanbiedingen en ervaringen in de activiteit hebben gereageerd.</li><li>Het [[!UICONTROL Important Attributes] rapport ](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker aan zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MV) | Naast het [[!UICONTROL Experience Performance] rapport ](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), kunt u het [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) pictogram klikken om het rapport te schakelen om bijdrage door plaats te tonen. |

## Aanvullende rapportage-informatie voor specifieke soorten activiteiten {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Naast de algemene rapporteringsinformatie in dit onderwerp en zijn subtopics, is de extra informatie specifiek voor individuele activiteitentypes elders in deze gids beschikbaar:

| Type activiteit | Details |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | Om lift en vertrouwen en de statistische benaderingen te begrijpen die in [!DNL Target] worden gebruikt, zie [ Plan een Test A/B ](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [ interpreteer [!UICONTROL Auto-Allocate] rapporten ](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Interpreteer de resultaten van een [!UICONTROL Auto-Allocate] A/B-activiteit door belangrijke indicatoren, waaronder lift en vertrouwen, te onderzoeken in de [!DNL Target] -gebruikersinterface. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informatie over het [!UICONTROL Summary] -rapport voor AT-activiteiten. Voor meer informatie, zie [[!UICONTROL Auto-Target Summary] Rapport ](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br> informatie over de twee [!UICONTROL Personalization Insights] rapporten voor activiteiten van AT en AP: [!UICONTROL Automated Segments] rapport en [!UICONTROL Important Attributes] rapport. Voor meer informatie, zie [ de Rapporten van de Inzichten van Personalization ](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informatie over de twee [!UICONTROL Automated Personalization Summary] -rapporten voor AP-activiteiten: [!UICONTROL Activity Level] -rapport en [!UICONTROL Offer Level] -rapport. Voor meer informatie, zie [ de SamenvattingsRapporten van Automated Personalization ](/help/main/c-reports/personalization-reports/reports-ap.md).<br> informatie over de twee [!UICONTROL Personalization Insights] rapporten voor activiteiten van AT en AP: [!UICONTROL Automated Segments] rapport en [!UICONTROL Important Attributes] rapport. Voor meer informatie, zie [ de Rapporten van de Inzichten van Personalization ](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MV) | Informatie over de twee rapporten voor MVT-activiteiten: [!UICONTROL Experience Performance] rapport en [!UICONTROL Location Contribution] rapport. Voor meer informatie, zie [ het Rapport van de Prestaties van de Ervaring ](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) (MVT) en [ Rapport van de Bijdrage van de Plaats ](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT). |
| [[!DNL Adobe Analytics]  als Rapporterende Source voor Adobe Target ](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informatie over het gebruik van [!DNL Adobe Analytics] als rapportagebron voor [!DNL Target] (A4T). A4T biedt u toegang tot [!DNL Analytics] -rapporten voor uw [!DNL Target] -activiteiten. Voor meer informatie, zie [ Analytics voor Doel (A4T) het Melden ](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |
| [[!DNL Target]  rapporterend in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | Informatie over de integratie tussen [ Adobe Customer Journey Analytics ](https://experienceleague.adobe.com/en/docs/customer-journey-analytics) {target=_blank} en [!DNL Target] die krachtige analyse en tijdbesparende hulpmiddelen voor uw optimaliseringsprogramma verstrekt. |

## Blokrapportgegevens van opgegeven IP-adressen

U kunt bezoekers van gespecificeerde IP adressen van worden geteld in rapporten blokkeren. Dit is bijvoorbeeld handig om rapportgegevens van uw interne bezoekers te blokkeren.

[ de Zorg van de Cliënt van het Contact ](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) aan opstellingsIP filters. Dit het filtreren is niet van toepassing wanneer het gebruiken van [ Analytics voor Doel ](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als uw rapporteringsbron.
