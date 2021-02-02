---
keywords: rapporten;downloadrapporten;csv;succesmetriek;orderdetails
description: Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in Excel, Access of andere programma's voor gegevensanalyse met Adobe Target.
title: Gegevens downloaden in een CSV-bestand
feature: Reports
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---


# Gegevens downloaden in een CSV-bestand{#downloading-data-in-a-csv-file}

Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in Excel, Access of andere programma&#39;s voor gegevensanalyse.

Gegevens downloaden in een CSV-bestand:

1. Klik **[!UICONTROL Activities]**, dan klik de gewenste activiteit van de lijst.

   Als u veel activiteiten hebt, kunt u de lijst filteren door opties te selecteren in de vervolgkeuzelijsten [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] en [!UICONTROL Activity Source].

1. Klik op het tabblad **[!UICONTROL Reports]**.
1. Klik op het pictogram **[!UICONTROL Download]** en selecteer vervolgens een rapporttype dat u wilt downloaden voor analyse in Excel en andere gereedschappen.

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
>Het CSV-rapport bevat alleen onbewerkte gegevens en bevat geen berekende gegevens, zoals inkomsten per bezoeker, lift of betrouwbaarheid die worden gebruikt voor A/B-tests. Als u deze berekende metriek wilt berekenen, downloadt u het Excel-bestand [Complete Trust Calculator](/help/assets/complete_confidence_calculator.xlsx) om de waarde van de activiteit in te voeren of bekijkt u de [statistische berekeningen die door Target](/help/assets/statistical-calculations.pdf) worden gebruikt.

## Bestelgegevens exporteren naar CSV {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Het rapport Bestelgegevens bevat informatie over uw bestellingen, zoals:

* Datum en tijd van bestelling
* Het bedrag van de orde (als u een doos van de Orde van de Plaats opnam)

   Het rapport Bestelgegevens werkt alleen als u bestellingen hebt.

* Order, markering (dubbele of extreme orders)

   Een orde wordt gemarkeerd als uiterste als het meer dan +/- 3 standaardafwijkingen van de gemiddelde ordewaarde gebruikend de laatste maand van gegevens (tot het tijdstip waarop de berekening werd gemaakt) is. Een activiteit zal zijn extreme orden uitgesloten zodra de activiteit een uur of tot na 15 orden heeft gelopen, welke eerst komt. Zie [Extreme bestellingen uitsluiten](/help/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA) voor meer informatie.

* Product-id

   De totale lengte van product IDs, samengevoegd met komma&#39;s, zou niet 255 karakters moeten overschrijden of IDs zal niet behoorlijk in het rapport tonen. Als uw bestelling bijvoorbeeld producten met de id&#39;s &quot;aa, bb&quot; bevat, is de totale lengte &quot;aa,bb&quot; = 5.

* Ervaring

   In het [!UICONTROL Order Details] rapport voor [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT), en [!UICONTROL Multivariate Test] (MVT) activiteiten, bevat de [!UICONTROL Experience] kolom de ervaring `localId`. Dit is de waarde-uitvoer van de `$campaign.recipe.id` in aanbiedingstokens.

   Er is geen [!UICONTROL Experience] kolom voor [!UICONTROL Automated Personalization] (AP) activiteiten. De huidige [!UICONTROL Algorithm Name] kolom is vervangen door &quot;Controle&quot;versus &quot;Gerichte&quot;terminologie, zoals elders getoond in [!DNL Target].

   Er was geen invloed op [!UICONTROL Recommendations] activiteiten.

>[!NOTE]
>
>* De gegevens van het orderrapport bevatten vier weken gegevens voor de standaardomgeving (hostgroep) en twee weken voor alle niet-standaardomgevingen.
>* De metriek van de opbrengst die aan &quot;de telling van de Toename worden geplaatst en de gebruiker in het activiteitenlogboek orddetails slechts voor de eerste orde houden die door de zelfde bezoeker wordt gemaakt. Alle volgende bestellingen verhogen het aantal conversies, maar voegen geen inkomsten toe aan RPV/AOV/Sales en worden niet opgenomen in het rapport Bestelgegevens.


## Aanbevolen werkwijzen

* Als u een orderrecord wilt opnemen, moet de parameter `orderTotal` worden doorgegeven.
* Waarden die via de parameter `ProductPurchasedId` mbox worden doorgegeven, worden vermeld in het rapport Order Details.
* De beste praktijken moeten `orderID` evenals `orderTotal` omvatten. Hierdoor kunnen dubbele orders automatisch worden genegeerd.

## Voorwerpen {#section_49B9590904A645B18E694B4EFFFC1DEF}

De volgende informatie is van toepassing op de optie Downloaden:

* U kunt beide rapporten downloaden voor A/B Test, Automated Personalization, Experience Targeting, en Multivariate activiteiten. U kunt het rapport Metriek van het Succes niet voor de activiteiten van de Aanbeveling downloaden.
* De optie Downloaden is niet beschikbaar voor activiteiten van het type A/B en Experience Targeting die vóór Doelversie 15.7.1 zijn gemaakt (juli 2015).
* Ervaringen zonder bijbehorende gegevens worden niet opgenomen in het gedownloade rapport.
* Het publiek dat in het Doel wordt toegepast meldt UI niet over aan het downloadrapport.
