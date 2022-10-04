---
keywords: Doel;rapporten;rapport montages;veelvoudige metriek;metriek;getoonde metriek;verborgen metriek
description: Leer hoe u meerdere metriek selecteert om in een rapport te bekijken met Adobe Target.
title: Hoe bekijk ik Meerdere metriek in een Rapport?
feature: Reports
exl-id: 8d8aedd8-4583-4131-8ae0-df14e071940a
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Meerdere metriek in een rapport weergeven

U kunt meerdere metriek selecteren om te bekijken in een [!DNL Adobe Target] verslag.

Houd rekening met de volgende informatie wanneer u met meerdere meetgegevens werkt in rapporten:

* De mogelijkheid om meerdere metriek weer te geven is beschikbaar voor [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md), [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md), en [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten.
* U kunt niet meer dan 20 metriek aan een rapport voor een activiteit toevoegen die gebruikt [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). U kunt zo veel metriek toevoegen zoals u in uw activiteit hebt aan rapporten voor activiteiten die doen *niet* gebruik A4T.
* U kunt de [Downloadoptie](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) om rapporten naar CSV te downloaden als u veelvoudige metriek hebt geselecteerd. U moet één enkele metrisch slechts selecteren om toe te laten [!UICONTROL Download] optie.
* U kunt geen veelvoudige metriek voor activiteiten bekijken die vóór Juli 2015 worden gecreeerd [!DNL Target] release (30 juli 2015).

**Om veelvoudige metriek te selecteren in het rapport te tonen:**

1. Als u een rapport wilt weergeven, klikt u op **[!UICONTROL Activities]**, klikt u in de lijst op de gewenste activiteit en klikt u vervolgens op de knop **[!UICONTROL Reports]** tab.
1. Klik op de knop **[!UICONTROL Report Metric]** vervolgkeuzelijst om de [!UICONTROL Shown Metrics] en [!UICONTROL Hidden Metrics] lijsten.

   ![multiple_metrics-afbeelding](assets/multiple_metrics.png)

   U kunt de [!UICONTROL Search] om snel de beschikbare metriek te vinden die aan [!UICONTROL Shown Metrics] lijst.

   U kunt meerdere metriek selecteren in het dialoogvenster [!UICONTROL Table View] en [!UICONTROL Graph View] de wijze van verslaglegging.

1. Houd de muisaanwijzer boven de gewenste maatstaven in het dialoogvenster [!UICONTROL Hidden Metrics] lijst en klik vervolgens op **[!UICONTROL Select]** om ze naar [!UICONTROL Shown Metrics] lijst.

   of

   Sleep de gewenste metriek vanuit de [!UICONTROL Hidden Metrics] aan de [!UICONTROL Shown Metrics] lijst.

   Er moet ten minste één metrische waarde in de [!UICONTROL Shown Metrics] lijst.

   U kunt de metriek opnieuw rangschikken door deze in de gewenste volgorde te slepen [!UICONTROL Shown Metrics] lijst. De geselecteerde volgorde wordt weerspiegeld in de [!UICONTROL Table View] en [!UICONTROL Graph View]. Om metrisch uit metrisch te verwijderen [!UICONTROL Shown Metrics] Plaats de muisaanwijzer boven de metrische waarde en klik op de knop **X** pictogram.

1. Klikken **[!UICONTROL Save]** wanneer gereed.
1. (Voorwaardelijk) Terwijl het bekijken van het rapport in [!UICONTROL Table View]Plaats de muisaanwijzer op de kolomkop van een willekeurige meting om een blauwe pijl weer te geven. Klik op de pijl om de tabel uit te vouwen om de [!UICONTROL Lift] en [!UICONTROL Confidence] voor die metrische waarde.

   ![multiple_metrics_table image](assets/multiple_metrics_table.png)

   U kunt slechts één metrisch/kolom tegelijk uitvouwen. Klik nogmaals op de pijl om de kolommen samen te vouwen.

1. (Voorwaardelijk) terwijl het bekijken van het rapport in de Mening van de Grafiek, kunt u individuele metriek selecteren om van de drop-down lijst te tonen:

   ![multiple_metrics_graph image](assets/multiple_metrics_graph.png)
