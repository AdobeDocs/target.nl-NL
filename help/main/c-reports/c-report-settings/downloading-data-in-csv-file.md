---
keywords: rapporten;downloadrapporten;csv;succesmetriek;orderdetails
description: Leer hoe u gegevens kunt downloaden van Adobe [!DNL Target] activiteiten in een formaat CVS voor snelle invoer in Excel, Toegang, of andere programma's van de gegevensanalyse.
title: Hoe kan ik rapportgegevens in een CSV-bestand downloaden?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: fc1dcc2b6de1248c35191c1ecd7b36aeb891fd3f
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Gegevens downloaden in een CSV-bestand

Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in Excel, Access of andere programma&#39;s voor gegevensanalyse.

Gegevens downloaden in een CSV-bestand:

1. Klikken **[!UICONTROL Activities]** en klikt u vervolgens in de lijst op de gewenste activiteit.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van te selecteren [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] vervolgkeuzelijsten.

1. Klik op de knop **[!UICONTROL Reports]** tab.
1. Klik op de knop **[!UICONTROL Download]** en selecteert u vervolgens een rapporttype dat u wilt downloaden voor analyse in Excel en andere gereedschappen.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

   ![Downloadopties](/help/main/c-reports/assets/download-options.png)

## [!UICONTROL Export Report to CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

De [!UICONTROL Success Metrics] het rapport toont u informatie over uw succesmetriek, en de volgende metriek die niet beschikbaar in [!DNL Target] UI:

* Gemiddelde tijd voor conversie in uren, zodat u kunt zien hoe lang het duurt voordat de gemiddelde bezoeker het conversiepunt bereikt
* Som van inkomsten, uitgedrukt in kwadraat, voor berekeningen van het off-line statistisch vertrouwen

Gegevens worden opgeslagen tot het einde van de activiteit.

>[!NOTE]
>
>Het CSV-rapport bevat alleen onbewerkte gegevens en bevat geen berekende gegevens, zoals inkomsten per bezoeker, lift of betrouwbaarheid die worden gebruikt voor A/B-tests. Download de [!DNL Target] [Complete betrouwbaarheidscalculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel-bestand om de waarde van de activiteit in te voeren of te reviseren [Statistische berekeningen voor A/Bn-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Export Order Details to CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

De [!UICONTROL Order Details] geeft u informatie over uw bestellingen, zoals:

* Datum en tijd van bestelling
* Het bedrag van de orde (als u een doos van de Orde van de Plaats opnam)

   De [!UICONTROL Order Details] het rapport werkt slechts als u orden hebt.

* Order, markering (dubbele of extreme orders)

   Een orde wordt gemarkeerd als uiterste als het meer dan +/- 3 standaardafwijkingen van de gemiddelde ordewaarde is. Bij deze berekening wordt de laatste maand van de gegevens gebruikt (tot het tijdstip waarop de berekening is gemaakt). Een activiteit zal zijn extreme orden uitgesloten zodra de activiteit een uur of tot na 15 orden heeft gelopen, welke eerst komt. Zie voor meer informatie [Exclusief extreme bestellingen](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* Product-id

   De totale lengte van product IDs, samengevoegd met komma&#39;s, zou niet 255 karakters moeten overschrijden of IDs niet behoorlijk in het rapport tonen. Als uw bestelling bijvoorbeeld producten met de id&#39;s &quot;aa, bb&quot; bevat, is de totale lengte &quot;aa,bb&quot; = 5.

* Ervaring

   In de [!UICONTROL Order Details] verslag voor [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT), en [!UICONTROL Multivariate Test] (MVT) activiteiten, [!UICONTROL Experience] kolom bevat de ervaring `localId`. Dit is de waarde die wordt uitgevoerd door de `$campaign.recipe.id` in aanbiedingen tokens.

   Er is geen [!UICONTROL Experience] kolom voor [!UICONTROL Automated Personalization] (AP) activiteiten. De huidige [!UICONTROL Algorithm Name] kolom is vervangen door &quot;Control&quot; versus &quot;Targeted&quot; terminologie, zoals elders in [!DNL Target].

   Er was geen invloed op [!UICONTROL Recommendations] activiteiten.

>[!NOTE]
>
>* De gegevens van het orderrapport bevatten vier weken gegevens voor de standaardomgeving (hostgroep) en twee weken voor alle niet-standaardomgevingen.
>* De metriek van de opbrengst die aan &quot; worden geplaatst[!UICONTROL Increment count and keep the user in the activity]&quot; alleen de gegevens van de logboekbestelling voor de eerste bestelling die door dezelfde bezoeker is uitgevoerd. Alle volgende bestellingen verhogen het aantal conversies, maar voegen geen inkomsten toe aan RPV/AOV/Sales en worden niet opgenomen in de [!UICONTROL Order Details] verslag.


## Aanbevolen werkwijzen

* Als u een orderrecord wilt opnemen, `orderTotal` parameter moet worden doorgegeven.
* Waarden die via de `ProductPurchasedId` mbox-parameter wordt vermeld in de [!UICONTROL Order Details] verslag.
* De beste praktijken moeten omvatten `orderID` en `orderTotal`. Hierdoor kunnen dubbele orders automatisch worden genegeerd.

## Caveats {#section_49B9590904A645B18E694B4EFFFC1DEF}

De volgende informatie is van toepassing op de [!UICONTROL Download] optie:

* U kunt beide rapporten downloaden voor [!UICONTROL A/B Test], [!UICONTROL Automated Personalization], [!UICONTROL Experience Targeting], en [!UICONTROL Multivariate] activiteiten. U kunt de [!UICONTROL Success Metrics] verslag voor [!UICONTROL Recommendations] activiteiten.
* De [!UICONTROL Download] optie is niet beschikbaar voor [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] activiteiten die vóór [!DNL Target] versie 15.7.1 (juli 2015).
* Ervaringen zonder bijbehorende gegevens worden niet opgenomen in het gedownloade rapport.
* Publiek dat wordt toegepast in de [!DNL Target] rapportage-UI gaat niet over naar het downloadrapport.
* Rapporten die worden gegenereerd om te worden gedownload als CSV-bestanden, zijn inconsistent als de activiteit meer dan één metrische waarde gebruikt. Het downloadbare rapport wordt geproduceerd gebaseerd op de rapportmontages slechts en beschouwt de zelfde waarde voor een andere gebruikte metriek. De bron van de waarheid is altijd het verslag dat in het [!DNL Target] UI.
