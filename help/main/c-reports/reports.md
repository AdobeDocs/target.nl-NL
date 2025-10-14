---
keywords: rapporten;blok ip adres;blok bezoeker van ip adres;download rapporten;csv;rapportering
description: Optimaliseer uw activiteiten door  [!DNL Adobe Target] rapporteringseigenschappen te beheersen om besluitvorming te verbeteren en ROI op te voeren.
title: Hoe kan ik rapporten weergeven?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: bd65cb9339dbe4b79d26c314cfb81d1fc7226fd2
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---

# Rapporten

Rapporten bevatten informatie over de voortgang en de resultaten van uw [!DNL Adobe Target] -activiteiten die u helpen beslissingen te nemen op basis van gegevens. Met behulp van rapportgegevens kunt u bepalen wanneer een activiteit moet worden beëindigd, u laten zien welke ervaring of aanbieding de winnaar is en kunt u inzichten of lessen bieden die u nodig hebt om de volgende acties te bepalen.

## Een rapport weergeven {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Klik op **[!UICONTROL Activities]** en klik vervolgens op de gewenste activiteit in de lijst.

   Als u vele activiteiten hebt, kunt u het pictogram van de Filter ( ![&#x200B; pictogram van de Filter &#x200B;](/help/main/assets/icons/Filter.svg)) klikken om de lijst te filtreren door opties van [!UICONTROL Type] te selecteren, [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], [!UICONTROL Decisioning Method], en [!UICONTROL Activity Source] lijsten.

   U kunt bijvoorbeeld [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] selecteren in de vervolgkeuzelijst [!UICONTROL Type] en [!UICONTROL Live] in de vervolgkeuzelijst [!UICONTROL Status] om alleen [!UICONTROL A/B Test] - en [!UICONTROL Experience Targeting] -activiteiten weer te geven die actief zijn.

   De volgende afbeelding toont de vervolgkeuzelijst [!UICONTROL Type] met twee geselecteerde typen: [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] . Merk op dat de drie types van Tests A/B (Hand, [&#x200B; auto-Wijs &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) toe, en [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) door gebrek worden geselecteerd. U kunt desgewenst een of meer typen deselecteren.

   ![&#x200B; de rapporten van de Filter door type &#x200B;](/help/main/c-reports/assets/report-filters-refresh.png)

1. Klik op de gewenste activiteit in de lijst om de bijbehorende [!UICONTROL Overview] pagina weer te geven.

1. Klik op de tab **[!UICONTROL Reports]** in de linkertrack.

   ![&#x200B; A/B- rapport &#x200B;](/help/main/c-reports/assets/reports-refresh.png)

   Elk rapport bevat een legenda om u te helpen het rapport te begrijpen.

   De legenda geeft de volgende informatie weer:

   * De status van de activiteit, inclusief het datumbereik waarop de activiteit werd uitgevoerd.
   * De [&#x200B; geprojecteerde het winnen ervaring &#x200B;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (als beschikbaar).

   >[!NOTE]
   >
   >Ervaringsresultaten worden weergegeven nadat ten minste één kandidaat de ervaring heeft gezien.

1. (Facultatief) [&#x200B; vorm het rapport &#x200B;](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) door het pictogram van de Montages van het Rapport te klikken ( ![&#x200B; pictogram van de Montages van het Rapport &#x200B;](/help/main/assets/icons/Setting.svg)).
1. (Facultatief) klik het pictogram van de Rapporten van de Download ( ![&#x200B; pictogram van de Rapporten van de Download &#x200B;](/help/main/assets/icons/Download.svg)) [&#x200B; het rapport in formaat CSV &#x200B;](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) voor analyse in Excel en andere hulpmiddelen downloaden.

   De volgende opties zijn beschikbaar:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Facultatief) klik **[!UICONTROL Table View]** ( ![&#x200B; pictogram van de Mening van de Lijst &#x200B;](/help/main/assets/icons/Table.svg)) en **[!UICONTROL Graph View]** ( ![&#x200B; pictogram van de Mening van de Grafiek &#x200B;](/help/main/assets/icons/GraphTrend.svg) ) pictogrammen om tussen het melden van formaten te schakelen.

   Afhankelijk van het type rapport dat u hebt geselecteerd, zijn mogelijk andere weergaven en rapporten beschikbaar:

   | Rapporttype | Weergave |
   | --- | --- |
   | [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Klik **[!UICONTROL Automated Segments]** ( ![&#x200B; Geautomatiseerde het rapport van Segmenten &#x200B;](/help/main/assets/icons/AutomatedSegment.svg)) of **[!UICONTROL Important Attributes]** ( ![&#x200B; Belangrijk pictogram van Attributen &#x200B;](/help/main/assets/icons/ViewList.svg)) pictogrammen.<ul><li>Het [[!UICONTROL Automated Segments] rapport &#x200B;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend op de aanbiedingen en ervaringen in uw [!UICONTROL Automated Personalization] of [!UICONTROL Auto-Target] activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen worden gedefinieerd, op de aanbiedingen en ervaringen in de activiteit hebben gereageerd.</li><li>Het [[!UICONTROL Important Attributes] rapport &#x200B;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker aan zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Naast [[!UICONTROL Automated Personalization Summary] rapporten &#x200B;](/help/main/c-reports/personalization-reports/reports-ap.md), kunt u **[!UICONTROL Automated Segments]** klikken ( ![&#x200B; Geautomatiseerde het rapport van Segmenten &#x200B;](/help/main/assets/icons/AutomatedSegment.svg)) of **[!UICONTROL Important Attributes]** ( ![&#x200B; Belangrijke het pictogram van Attributen &#x200B;](/help/main/assets/icons/ViewList.svg)) pictogrammen.<ul><li>Het [[!UICONTROL Automated Segments] rapport &#x200B;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) toont hoe de verschillende bezoekers verschillend op de aanbiedingen en ervaringen in uw [!UICONTROL Automated Personalization] of [!UICONTROL Auto-Target] activiteit antwoorden. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen worden gedefinieerd, op de aanbiedingen en ervaringen in de activiteit hebben gereageerd.</li><li>Het [[!UICONTROL Important Attributes] rapport &#x200B;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) toont hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker aan zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.</li></ul> |
   | [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MV) | Naast het [[!UICONTROL Experience Performance] rapport &#x200B;](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), kunt u [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) ( ![&#x200B; pictogram van de Bijdrage van de Plaats &#x200B;](/help/main/assets/icons/LocationContribution.svg)) klikken om het rapport te schakelen om bijdrage door plaats te tonen. |

## Aanvullende rapportage-informatie voor specifieke soorten activiteiten {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Naast de algemene rapporteringsinformatie in dit onderwerp en zijn subtopics, is de extra informatie specifiek voor individuele activiteitentypes elders in deze gids beschikbaar:

| Type activiteit | Details |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | Om lift en vertrouwen en de statistische benaderingen te begrijpen die in [!DNL Target] worden gebruikt, zie [&#x200B; Plan een Test A/B &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [&#x200B; interpreteer [!UICONTROL Auto-Allocate] rapporten &#x200B;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Interpreteer de resultaten van een [!UICONTROL Auto-Allocate] A/B-activiteit door belangrijke indicatoren, waaronder lift en vertrouwen, te onderzoeken in de [!DNL Target] -gebruikersinterface. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informatie over het [!UICONTROL Summary] -rapport voor AT-activiteiten. Voor meer informatie, zie [[!UICONTROL Auto-Target Summary] Rapport &#x200B;](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br> informatie over de twee [!UICONTROL Personalization Insights] rapporten voor activiteiten van AT en AP: [!UICONTROL Automated Segments] rapport en [!UICONTROL Important Attributes] rapport. Voor meer informatie, zie [&#x200B; de Rapporten van de Inzichten van Personalization &#x200B;](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informatie over de twee [!UICONTROL Automated Personalization Summary] -rapporten voor AP-activiteiten: [!UICONTROL Activity Level] -rapport en [!UICONTROL Offer Level] -rapport. Voor meer informatie, zie [&#x200B; de SamenvattingsRapporten van Automated Personalization &#x200B;](/help/main/c-reports/personalization-reports/reports-ap.md).<br> informatie over de twee [!UICONTROL Personalization Insights] rapporten voor activiteiten van AT en AP: [!UICONTROL Automated Segments] rapport en [!UICONTROL Important Attributes] rapport. Voor meer informatie, zie [&#x200B; de Rapporten van de Inzichten van Personalization &#x200B;](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MV) | Informatie over de twee rapporten voor MVT-activiteiten: [!UICONTROL Experience Performance] rapport en [!UICONTROL Location Contribution] rapport. Voor meer informatie, zie [&#x200B; het Rapport van de Prestaties van de Ervaring &#x200B;](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) (MVT) en [&#x200B; Rapport van de Bijdrage van de Plaats &#x200B;](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT). |
| [[!DNL Adobe Analytics]  als Rapporterende Source voor Adobe Target &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informatie over het gebruik van [!DNL Adobe Analytics] als rapportagebron voor [!DNL Target] (A4T). A4T biedt u toegang tot [!DNL Analytics] -rapporten voor uw [!DNL Target] -activiteiten. Voor meer informatie, zie [&#x200B; Analytics voor Doel (A4T) het Melden &#x200B;](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |
| [[!DNL Target]  rapporterend in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | Informatie over de integratie tussen [&#x200B; Adobe Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/customer-journey-analytics){target=_blank} en [!DNL Target] die krachtige analyse en tijdbesparende hulpmiddelen voor uw optimaliseringsprogramma verstrekt. |

## Blokrapportgegevens van opgegeven IP-adressen

U kunt bezoekers van gespecificeerde IP adressen van worden geteld in rapporten blokkeren. Deze optie is bijvoorbeeld handig om rapportgegevens van uw interne bezoekers te blokkeren.

[&#x200B; de Zorg van de Cliënt van het Contact &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) aan opstellingsIP filters. Dit het filtreren is niet van toepassing wanneer het gebruiken van [&#x200B; Analytics voor Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als uw rapporteringsbron.
