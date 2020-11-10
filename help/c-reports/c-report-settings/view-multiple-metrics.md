---
keywords: Target;reports;report settings;multiple metrics;metrics;shown metrics;hidden metrics
description: Selecteer veelvoudige metriek aan mening in een rapport gebruikend Adobe Target.
title: Meerdere metriek in een rapport weergeven met Adobe Target
feature: report settings
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---


# Meerdere metriek in een rapport weergeven{#view-multiple-metrics-in-a-report}

U kunt veelvoudige metriek selecteren om in een [!DNL Adobe Target] rapport te bekijken.

Houd rekening met de volgende informatie wanneer u met meerdere meetgegevens werkt in rapporten:

* De capaciteit om veelvoudige metriek te bekijken is beschikbaar voor [A/B Test](/help/c-activities/t-test-ab/test-ab.md), [auto-Wijs](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [auto-Doel](/help/c-activities/auto-target/auto-target-to-optimize.md), en [Ervaring richten](/help/c-activities/t-experience-target/experience-target.md) (XT) slechts activiteiten.
* U kunt niet meer dan 20 metriek aan een rapport voor een activiteit toevoegen die [Analytics voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt. U kunt zo vele metriek toevoegen aangezien u in uw activiteit aan rapporten voor activiteiten hebt die *geen* A4T gebruiken.
* U kunt de optie [](/help/c-reports/downloading-data-in-csv-file.md) Downloaden niet gebruiken om rapporten naar CSV te downloaden als u meerdere metriek hebt geselecteerd. U moet één enkele metrisch slechts selecteren om de [!UICONTROL Download] optie toe te laten.
* U kunt geen veelvoudige metriek voor activiteiten bekijken die vóór [!DNL Target] versie van juli 2015 (30 juli 2015) worden gecreeerd.

**Om veelvoudige metriek te selecteren in het rapport te tonen:**

1. Als u een rapport wilt weergeven, klikt u op **[!UICONTROL Activities]** de gewenste activiteit in de lijst en klikt u op het **[!UICONTROL Reports]** tabblad.
1. Klik op de **[!UICONTROL Report Metric]** vervolgkeuzelijst om de [!UICONTROL Shown Metrics] lijst en de [!UICONTROL Hidden Metrics] lijsten weer te geven.

   ![](assets/multiple_metrics.png)

   U kunt het [!UICONTROL Search] vak gebruiken om snel beschikbare metriek te zoeken die u aan de [!UICONTROL Shown Metrics] lijst wilt toevoegen.

   Merk op dat u veelvoudige metriek van zowel de [!UICONTROL Table View] als [!UICONTROL Graph View] wijzen van het rapport kunt selecteren.

1. Houd de muisaanwijzer boven de gewenste maateenheden in de [!UICONTROL Hidden Metrics] lijst en klik **[!UICONTROL Select]** om deze naar de [!UICONTROL Shown Metrics] lijst te verplaatsen.

   of

   Sleep de gewenste metriek van de [!UICONTROL Hidden Metrics] lijst naar de [!UICONTROL Shown Metrics] lijst.

   De [!UICONTROL Shown Metrics] lijst moet minstens één metrische waarde bevatten.

   U kunt de metriek opnieuw rangschikken door deze in de gewenste volgorde in de [!UICONTROL Shown Metrics] lijst te slepen. De geselecteerde volgorde wordt weerspiegeld in de [!UICONTROL Table View] en [!UICONTROL Graph View]. Als u een metrische waarde uit de [!UICONTROL Shown Metrics] lijst wilt verwijderen, plaatst u de muisaanwijzer boven de metrische waarde en klikt u op het pictogram **X** .

1. Klik **[!UICONTROL Save]** wanneer gebeëindigd.
1. (Voorwaardelijk) terwijl het bekijken van het rapport in de [!UICONTROL Table View], beweegt uw muiswijzer over om het even welke metrische kolomkopbal om een blauwe pijl te tonen. Klik op de pijl om de tabel uit te vouwen en de metrische waarden [!UICONTROL Lift] en [!UICONTROL Confidence] waarden voor de tabel weer te geven.

   ![](assets/multiple_metrics_table.png)

   U kunt slechts één metrisch/kolom tegelijk uitvouwen. Klik nogmaals op de pijl om de kolommen samen te vouwen.

1. (Voorwaardelijk) terwijl het bekijken van het rapport in de Mening van de Grafiek, kunt u individuele metriek selecteren om van de drop-down lijst te tonen:

   ![](assets/multiple_metrics_graph.png)

