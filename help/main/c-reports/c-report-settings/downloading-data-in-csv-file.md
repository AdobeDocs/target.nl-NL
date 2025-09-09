---
keywords: rapporten;downloadrapporten;csv;succesmetriek;orderdetails
description: Leer hoe te om gegevens van Adobe  [!DNL Target]  activiteiten in een formaat CVS voor de snelle invoer in Excel, Toegang, of andere programma's van de gegevensanalyse te downloaden.
title: Hoe kan ik rapportgegevens in een CSV-bestand downloaden?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: c0342f51d998d27eef9af189c7ebb364095699ed
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# Gegevens downloaden in een CSV-bestand

Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in [!DNL Excel] -, [!DNL Access] - of andere programma&#39;s voor gegevensanalyse.

Gegevens downloaden in een CSV-bestand:

1. Klik op **[!UICONTROL Activities]** en klik vervolgens op de gewenste activiteit in de lijst.

   Als u vele activiteiten hebt, klik het pictogram van de Filter ( ![ pictogram van de Filter ](/help/main/assets/icons/Filter.svg)) om de lijst te filtreren door opties van [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] drop-down lijsten te selecteren.

1. Klik op de tab **[!UICONTROL Reports]** .
1. Klik het **[!UICONTROL Download]** ( ![ pictogram van de Download ](/help/main/assets/icons/Download.svg) ) pictogram, dan selecteer een rapporttype voor analyse in Excel en andere hulpmiddelen te downloaden.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

## [!UICONTROL Export Report to CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Het [!UICONTROL Success Metrics] -rapport bevat informatie over uw succesmaatstaven en de volgende meetgegevens die niet beschikbaar zijn in de [!DNL Target] -gebruikersinterface:

* Gemiddelde tijd voor conversie in uren, zodat u kunt zien hoe lang het duurt voordat de gemiddelde bezoeker het conversiepunt bereikt
* Som van inkomsten, uitgedrukt in kwadraat, voor berekeningen van het off-line statistisch vertrouwen

Gegevens worden opgeslagen tot het einde van de activiteit.

>[!NOTE]
>
>Het CSV-rapport bevat alleen onbewerkte gegevens en bevat geen berekende gegevens, zoals inkomsten per bezoeker, lift of betrouwbaarheid die worden gebruikt voor A/B-tests. Om deze berekende metriek te berekenen, download het [!DNL Target] [ Volledige dossier van de Rekenmachine van het Vertrouwen ](/help/main/assets/complete_confidence_calculator.xlsx) Excel om de waarde van de activiteit in te voeren, of herzie [ Statistische berekeningen in tests A/Bn ](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Export Order Details to CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Het [!UICONTROL Order Details] -rapport geeft u informatie over uw bestellingen, zoals:

* Datum en tijd van bestelling
* Het bedrag van de orde (als u een doos van de Orde van de Plaats opnam)

  Het rapport [!UICONTROL Order Details] werkt alleen als u bestellingen hebt.

* Order, markering (dubbele of extreme orders)

  Een orde wordt gemarkeerd als uiterste als het meer dan +/- 3 standaardafwijkingen van de gemiddelde ordewaarde is. Bij deze berekening wordt de laatste maand van de gegevens gebruikt (tot het tijdstip waarop de berekening is gemaakt). Een activiteit zal zijn extreme orden uitgesloten zodra de activiteit een uur of tot na 15 orden heeft gelopen, welke eerst komt. Voor meer informatie, zie [ Excluding Extreme Orders ](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* Product-id

  De totale lengte van product IDs, samengevoegd met komma&#39;s, zou niet 255 karakters moeten overschrijden of IDs niet behoorlijk in het rapport tonen. Als uw bestelling bijvoorbeeld producten met de id&#39;s &quot;aa, bb&quot; bevat, is de totale lengte &quot;aa,bb&quot; = 5.

* Ervaring

  In het [!UICONTROL Order Details] -rapport voor [!UICONTROL A/B Test] -, [!UICONTROL Experience Targeting] - (XT) en [!UICONTROL Multivariate Test] -activiteiten (MVT) bevat de kolom [!UICONTROL Experience] de ervaringsgegevens `localId` . Dit is de waarde-uitvoer van de `$campaign.recipe.id` in-aanbiedingstokens.

  Er is geen [!UICONTROL Experience] -kolom voor [!UICONTROL Automated Personalization] -activiteiten (AP). De huidige kolom [!UICONTROL Algorithm Name] is vervangen door &quot;Control&quot; in plaats van &quot;Targeted&quot; in de terminologie, zoals elders in [!DNL Target] wordt getoond.

  Er was geen effect op [!UICONTROL Recommendations] -activiteiten.

>[!NOTE]
>
>* De gegevens van het orderrapport bevatten vier weken gegevens voor de standaardomgeving (hostgroep) en twee weken voor alle niet-standaardomgevingen.
>* De metriek van de opbrengst die aan &quot;[!UICONTROL Increment count and keep the user in the activity]&quot;de gegevens van de logboekorde slechts voor de eerste orde worden geplaatst door de zelfde bezoeker wordt gemaakt. Alle volgende bestellingen verhogen het aantal conversies, maar voegen geen inkomsten toe aan RPV/AOV/Sales en worden niet opgenomen in het [!UICONTROL Order Details] -rapport.

## CSV-downloadindeling voor populariteit en op sleutels gebaseerde algoritmen {#format}

Het CSV-downloadbestand geeft consistent de resultaten weer die zijn gegenereerd na uitvoering van de back-endcriteria.

**voor populariteit algoritmen (niet op sleutel-gebaseerd), omvat het dossier:**

* Een rij back-upaanbevelingen met *
* Aanbevelingen voor een aparte rij op basis van algoritme-instellingen

**voor op sleutel-gebaseerde algoritmen, omvat het dossier:**

* Een back-uprij die lijkt op populariteitsalgoritmen
* Meerdere rijen in sleutelwaardeformaat, waarbij de eerste vermelding de product-id van de sleutel is, gevolgd door door door komma&#39;s gescheiden product-id&#39;s die de kandidaten van de aanbeveling vertegenwoordigen

## Aanbevolen procedures

* Als u een orderrecord wilt opnemen, moet de parameter `orderTotal` worden doorgegeven.
* Waarden die via de parameter `ProductPurchasedId` mbox worden doorgegeven, worden vermeld in het [!UICONTROL Order Details] -rapport.
* De beste manier is om een `orderID` en een `orderTotal` op te nemen. Hierdoor kunnen dubbele orders automatisch worden genegeerd.

## Caveats {#section_49B9590904A645B18E694B4EFFFC1DEF}

De volgende informatie is van toepassing op de optie [!UICONTROL Download] :

* U kunt beide rapporten downloaden voor [!UICONTROL A/B Test] -, [!UICONTROL Automated Personalization] -, [!UICONTROL Experience Targeting] - en [!UICONTROL Multivariate] -activiteiten. U kunt het [!UICONTROL Success Metrics] -rapport niet downloaden voor [!UICONTROL Recommendations] -activiteiten.
* De optie [!UICONTROL Download] is niet beschikbaar voor [!UICONTROL A/B Test] - en [!UICONTROL Experience Targeting] -activiteiten die zijn gemaakt vóór [!DNL Target] versie 15.7.1 (juli 2015).
* Ervaringen zonder bijbehorende gegevens worden niet opgenomen in het gedownloade rapport.
* Soorten publiek dat wordt toegepast in de [!DNL Target] -rapporteringsinterface, worden niet doorgestuurd naar het downloadrapport.
* Rapporten die worden gegenereerd om te worden gedownload als CSV-bestanden, zijn inconsistent als de activiteit meer dan één metrische waarde gebruikt. Het downloadbare rapport wordt geproduceerd gebaseerd op de rapportmontages slechts en beschouwt de zelfde waarde voor een andere gebruikte metriek. De bron van de waarheid is altijd het weergegeven rapport in de gebruikersinterface van [!DNL Target] .
