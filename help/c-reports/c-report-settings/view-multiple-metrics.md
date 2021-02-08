---
keywords: Doel;rapporten;rapport montages;veelvoudige metriek;metriek;getoonde metriek;verborgen metriek
description: Leer hoe u meerdere metriek selecteert om in een rapport te bekijken met Adobe Target.
title: Hoe bekijk ik Meerdere metriek in een Rapport?
feature: Reports
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# Meerdere metriek weergeven in een rapport{#view-multiple-metrics-in-a-report}

U kunt veelvoudige metriek aan mening in een [!DNL Adobe Target] rapport selecteren.

Houd rekening met de volgende informatie wanneer u met meerdere meetgegevens werkt in rapporten:

* De capaciteit om veelvoudige metriek te bekijken is beschikbaar voor [A/B Test](/help/c-activities/t-test-ab/test-ab.md), [Auto-Toewijzing](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md), en [Ervaring richten](/help/c-activities/t-experience-target/experience-target.md) (XT) activiteiten slechts.
* U kunt niet meer dan 20 metriek aan een rapport voor een activiteit toevoegen die [Analytics voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt. U kunt zo vele metriek toevoegen aangezien u in uw activiteit aan rapporten voor activiteiten hebt die *niet* gebruiken A4T.
* U kunt de [optie van de Download ](/help/c-reports/downloading-data-in-csv-file.md) niet gebruiken om rapporten aan CSV te downloaden als u veelvoudige metriek hebt geselecteerd. U moet één enkele metrisch slechts selecteren om de [!UICONTROL Download] optie toe te laten.
* U kunt geen veelvoudige metriek voor activiteiten bekijken die vóór de release van juli 2015 [!DNL Target] (30 juli 2015) worden gecreeerd.

**Om veelvoudige metriek te selecteren in het rapport te tonen:**

1. Als u een rapport wilt weergeven, klikt u op **[!UICONTROL Activities]**, klikt u in de lijst op de gewenste activiteit en klikt u vervolgens op het tabblad **[!UICONTROL Reports]**.
1. Klik op de vervolgkeuzelijst **[!UICONTROL Report Metric]** om de lijsten [!UICONTROL Shown Metrics] en [!UICONTROL Hidden Metrics] weer te geven.

   ![](assets/multiple_metrics.png)

   Met het vak [!UICONTROL Search] kunt u snel beschikbare metriek zoeken die u aan de lijst [!UICONTROL Shown Metrics] wilt toevoegen.

   Merk op dat u veelvoudige metriek van zowel [!UICONTROL Table View] als [!UICONTROL Graph View] wijzen van het rapport kunt selecteren.

1. Houd de muisaanwijzer boven de gewenste metriek in de lijst [!UICONTROL Hidden Metrics] en klik vervolgens op **[!UICONTROL Select]** om deze naar de lijst [!UICONTROL Shown Metrics] te verplaatsen.

   of

   Sleep de gewenste metriek van [!UICONTROL Hidden Metrics] lijst aan [!UICONTROL Shown Metrics] lijst.

   De lijst [!UICONTROL Shown Metrics] moet minstens één metrisch bevatten.

   U kunt de metriek anders rangschikken door hen in de gewenste orde in [!UICONTROL Shown Metrics] lijst te slepen. De geselecteerde volgorde wordt weergegeven in de [!UICONTROL Table View] en [!UICONTROL Graph View]. Als u een metrische waarde uit de lijst [!UICONTROL Shown Metrics] wilt verwijderen, plaatst u de muisaanwijzer boven de metrische waarde en klikt u op het pictogram **X**.

1. Klik **[!UICONTROL Save]** wanneer gebeëindigd.
1. (Voorwaardelijk) terwijl het bekijken van het rapport in [!UICONTROL Table View], beweegt uw muiswijzer op om het even welke metrische kolomkopbal om een blauwe pijl te tonen. Klik de pijl om de lijst uit te breiden om [!UICONTROL Lift] en [!UICONTROL Confidence] voor dat metrisch te tonen.

   ![](assets/multiple_metrics_table.png)

   U kunt slechts één metrisch/kolom tegelijk uitvouwen. Klik nogmaals op de pijl om de kolommen samen te vouwen.

1. (Voorwaardelijk) terwijl het bekijken van het rapport in de Mening van de Grafiek, kunt u individuele metriek selecteren om van de drop-down lijst te tonen:

   ![](assets/multiple_metrics_graph.png)

