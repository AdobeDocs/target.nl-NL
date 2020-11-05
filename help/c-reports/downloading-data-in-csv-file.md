---
keywords: reports;download reports;csv;success metrics;order details
description: Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in Excel, Access of andere programma's voor gegevensanalyse met Adobe Target.
title: Gegevens in een CSV-bestand downloaden met Adobe Target
feature: reports
subtopic: Multivariate Test
topic: Standard
uuid: 9ac151e1-45a9-4d46-b23b-e7c9ae518253
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# Gegevens downloaden in een CSV-bestand{#downloading-data-in-a-csv-file}

Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in Excel, Access of andere programma&#39;s voor gegevensanalyse.

Gegevens downloaden in een CSV-bestand:

1. Klik **[!UICONTROL Activities]** en klik vervolgens in de lijst op de gewenste activiteit.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] drop-down lijsten te selecteren.

1. Klik op het **[!UICONTROL Reports]** tabblad.
1. Klik het **[!UICONTROL Download]** pictogram, dan selecteer een rapporttype om voor analyse in Excel en andere hulpmiddelen te downloaden.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

   ![Downloadopties](/help/c-reports/assets/download-options.png)

## Rapport exporteren naar CSV {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Het rapport Metriek van het Succes toont u informatie over uw succesmetriek, evenals de volgende metriek die niet beschikbaar in het Doel UI zijn:

* Gemiddelde tijd voor conversie in uren, zodat u kunt zien hoe lang het duurt voordat de gemiddelde bezoeker het conversiepunt bereikt
* Som van inkomsten, uitgedrukt in kwadraat, voor berekeningen van het off-line statistisch vertrouwen

Gegevens worden opgeslagen tot het einde van de activiteit.

>[!NOTE]
>
>Het CSV-rapport bevat alleen onbewerkte gegevens en bevat geen berekende gegevens, zoals inkomsten per bezoeker, lift of betrouwbaarheid die worden gebruikt voor A/B-tests. Om deze berekende metriek te berekenen, download het dossier van Excel van de Rekenmachine van het Doel van het [Volledige Vertrouwen om de waarde van de activiteit in te voeren, of herzie de](/help/assets/complete_confidence_calculator.xlsx) statistische berekeningen die door Doel [](/help/assets/statistical-calculations.pdf)worden gebruikt.

## Bestelgegevens exporteren naar CSV {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Het rapport Bestelgegevens bevat informatie over uw bestellingen, zoals:

* Datum en tijd van bestelling
* Het bedrag van de orde (als u een doos van de Orde van de Plaats opnam)

   Het rapport Bestelgegevens werkt alleen als u bestellingen hebt.

* Order, markering (dubbele of extreme orders)

   Een orde wordt gemarkeerd als uiterste als het meer dan +/- 3 standaardafwijkingen van de gemiddelde ordewaarde gebruikend de laatste maand van gegevens (tot het tijdstip waarop de berekening werd gemaakt) is. Een activiteit zal zijn extreme orden uitgesloten zodra de activiteit een uur of tot na 15 orden heeft gelopen, welke eerst komt. Zie [Extreme bestellingen](/help/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA)uitsluiten voor meer informatie.

* Product-id

   De totale lengte van product IDs, samengevoegd met komma&#39;s, zou niet 255 karakters moeten overschrijden of IDs zal niet behoorlijk in het rapport tonen. Als uw bestelling bijvoorbeeld producten met de id&#39;s &quot;aa, bb&quot; bevat, is de totale lengte &quot;aa,bb&quot; = 5.

* Ervaring

   In het [!UICONTROL Order Details] rapport voor [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT), en [!UICONTROL Multivariate Test] (MVT) activiteiten, bevat de [!UICONTROL Experience] kolom de ervaring `localId`. Dit is de waarde output van de `$campaign.recipe.id` in aanbiedingstokens.

   Er is geen [!UICONTROL Experience] kolom voor [!UICONTROL Automated Personalization] (AP) activiteiten. De huidige [!UICONTROL Algorithm Name] kolom is vervangen door &quot;Control&quot; versus &quot;Targeted&quot; terminologie, zoals elders in [!DNL Target]het document wordt getoond.

   Er was geen invloed op de [!UICONTROL Recommendations] activiteiten.

>[!NOTE]
>
>* De gegevens van het orderrapport bevatten vier weken gegevens voor de standaardomgeving (hostgroep) en twee weken voor alle niet-standaardomgevingen.
>* De metriek van de opbrengst die aan &quot;de telling van de Toename worden geplaatst en de gebruiker in het activiteitenlogboek orddetails slechts voor de eerste orde houden die door de zelfde bezoeker wordt gemaakt. Alle volgende bestellingen verhogen het aantal conversies, maar voegen geen inkomsten toe aan RPV/AOV/Sales en worden niet opgenomen in het rapport Bestelgegevens.


## Aanbevolen werkwijzen

* Als u een orderrecord wilt opnemen, moet de `orderTotal` parameter worden doorgegeven.
* Waarden die via de parameter `ProductPurchasedId` mbox worden doorgegeven, worden vermeld in het rapport Order Details.
* De beste praktijken moeten `orderID` zowel een als een `orderTotal`. Hierdoor kunnen dubbele orders automatisch worden genegeerd.

## Caveats {#section_49B9590904A645B18E694B4EFFFC1DEF}

De volgende informatie is van toepassing op de optie Downloaden:

* U kunt beide rapporten downloaden voor A/B Test, Automated Personalization, Experience Targeting, en Multivariate activiteiten. U kunt het rapport Metriek van het Succes niet voor de activiteiten van de Aanbeveling downloaden.
* De optie Downloaden is niet beschikbaar voor activiteiten van het type A/B en Experience Targeting die vóór Doelversie 15.7.1 zijn gemaakt (juli 2015).
* Ervaringen zonder bijbehorende gegevens worden niet opgenomen in het gedownloade rapport.
* Het publiek dat in het Doel wordt toegepast meldt UI niet over aan het downloadrapport.
