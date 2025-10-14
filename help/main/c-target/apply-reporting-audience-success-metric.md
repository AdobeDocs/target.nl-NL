---
keywords: gericht;publiek;rapportering;succes metrisch
description: Leer hoe te om metrisch succes in  [!DNL Adobe Target]  te kiezen dat de gebruiker voor het rapporterende publiek kwalificeert.
title: Kan ik een rapporteringspubliek op een succes metrisch toepassen?
feature: Success Metrics
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
source-git-commit: bcbb6dec9d6add07c109b07bf125c1356ad2a8b9
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Pas een rapporterend publiek op succes toe metrisch

Kies een succesmaatstaf die de gebruiker voor het rapportagepubliek in [!DNL Adobe Target] kwalificeert.

Voor alle activiteiten, laat de [!UICONTROL Applied At] drop-down lijst u een publiek op succes metrisch toepassen zodat kunt u rapportaantallen bekijken nadat metrisch is bereikt en voor verdere acties.

![&#x200B; success_metalimage &#x200B;](assets/success_metric.png)

Stel dat u een activiteit hebt gemaakt voor alle bezoekers die uw startpagina betreden en de conversiepagina bereiken, maar u wilt ook meer informatie weergeven over bezoekers die meer dan € 50 aan de winkelwagentje hebben toegevoegd voordat u deze omzet.

De vervolgkeuzelijst [!UICONTROL Applied At] bevat mogelijk drie categorieën:

* Alle bezoekers van de activiteit
* Alleen bezoekers die een bepaalde stap in de activiteit bereiken
* Alleen bezoekers die conversie bereiken

Of, om het anders te formuleren, kunt u specificeren dat een bezoeker een mbox op de ingangspagina van de activiteit moet hebben bereikt, een doos die één of ander punt in het midden van de activiteit, of de omzettingsmbox aan het eind van de activiteit bepaalt.

>[!NOTE]
>
>[&#x200B; metriek van het Succes &#x200B;](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) is beschikbaar slechts als u hen voor uw activiteit hebt gevormd. Als u geen succesmaatstaven hebt gedefinieerd, ziet u slechts twee opties in de vervolgkeuzelijst: [!UICONTROL Campaign Entry] en [!UICONTROL Conversion] .


## Overwegingen

Overweeg de volgende informatie wanneer het toepassen van een rapporterend publiek op succes metrisch:

* Alleen succesmetriek die begint bij degene waarop het publiek is toegepast, toont rapportgegevens die door het publiek zijn gesegmenteerd
* Geslaagde metriek voorafgaand aan degenen waarop het publiek wordt toegepast zal niet door het publiek worden gesegmenteerd, en zal alle bezoekersgegevens tonen
* De metriek worden beschouwd als gebaseerd op hun volgorde in de activiteitdefinitie, waarbij [!UICONTROL Primary Goal] de laatste is.

## Segmentering weergeven in rapportage

Als u de segmentatie in de rapportage wilt weergeven, selecteert u het gewenste publiek in de vervolgkeuzelijst [!UICONTROL Audience] in het activiteitenrapport.

![&#x200B; reporting_publiek_dropdown beeld &#x200B;](assets/reporting_audience_dropdown.png)

## Voorbeeld

Overweeg een activiteit die Metric1 van het Succes, Metric2 van het Succes, Metric3 van het Succes, en het Primaire Doel heeft.

Veronderstel u rapporterend Audience1 die op &quot;Ingang&quot;en rapporterend Audience2 op Succes Metric2 wordt geplaatst. Het publiek filtert de rapportgegevens als volgt:

|  | Bezoekers | Metrisch1 met succes | Metrisch2 met succes | Metrisch3 met succes | Primair doel |
| --- | --- | --- | --- | --- | --- |
| Publiek1 | Toegepast | Toegepast | Toegepast | Toegepast | Toegepast |
| Publiek2 | Niet toegepast | Niet toegepast | Toegepast | Toegepast | Toegepast |
