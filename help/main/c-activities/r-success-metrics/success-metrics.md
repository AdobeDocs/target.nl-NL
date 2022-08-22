---
keywords: Doelstelling;succes;omzettingsmetrische;paginascore;metrische paginamontages;opbrengstmetriek;tijd op plaats metrisch;geschatte waarde;geavanceerde montages;succesmetriek;gebiedsdeel;Afhankelijkheid;De Telling van de verhoging & houdt Gebruiker in Activiteit;De Telling van de verhoging, de gebruiker van de Versie, & Toestaan de Telling van de verhoging, de Gebruiker van de Versie, & Bar van Ingang
description: Meer informatie over succesmetriek in Adobe [!DNL Target] die u helpen het succes van een activiteit bepalen. Tot de succesmetingen behoren Conversie, Inkomsten, Paginaweergaven, Aangepaste score en Tijd op de site.
title: Wat zijn succescijfers?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: 7dd3e3167b7dcb4de9e2980e6fc41661a2574abc
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# Succeswaarden

In [!DNL Adobe Target] succeswaarden zijn parameters die worden gebruikt om het succes van een activiteit te meten. De metriek van het succes omvat zeer belangrijke bedrijfsmaatregelen die u toelaten om het succes van een bepaalde ervaring of een aanbieding in een [!DNL Target] activiteit.

U kunt bijvoorbeeld bepalen of een nieuwe aanbieding uw omzet per bezoeker verhoogt of een item aan een winkelwagentje toevoegt. Succeswaarden kunnen nuttig zijn voor het opsporen van problemen met registratie, bestellen of aanschafkanalen, maar ook eenvoudig met betrokkenheid van bezoekers of klanten.

## Overzicht

In [!DNL Target], worden de succesmetriek pre-gevormd met de optimale opties voor zowel het melden als het volgen doeleinden.

Conversiegebeurtenissen worden standaard ingesteld op &quot;[!UICONTROL Increment count & keep user in activity].&quot; Conversies worden slechts eenmaal geteld, er worden geen terugkerende conversies geteld en de bezoeker ziet altijd de inhoud van de activiteit.

De metriek van de opbrengst die aan &quot; worden geplaatst[!UICONTROL Increment count & keep user in activity]&quot; alleen de gegevens van de logboekbestelling voor de eerste bestelling die door dezelfde bezoeker is uitgevoerd. Alle volgende bestellingen verhogen het aantal conversies, maar voegen geen inkomsten toe aan RPV/AOV/Sales en worden niet opgenomen in de [!UICONTROL Order Details] verslag.

>[!NOTE]
>
>Voor activiteiten die [Analyses als bron van rapportage](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), zal het doel metrisch altijd &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; en &quot;[!UICONTROL On Every Impression]&quot;. Dit is *niet* configureerbaar.

De volgende succeswaarden zijn beschikbaar:

| Metrisch met succes | Meetmethode | Definitie |
|--- |--- |--- |
| Conversie | Op basis van conversie | Omzetten is wanneer een bezoeker een door u gedefinieerde handeling op uw site uitvoert, zoals <ul><li>Klik op een knop</li><li>Pagina&#39;s weergeven</li><li>Een enquête voltooid</li><li>Een aankoop gedaan</li></ul>Een conversie kan één keer per bezoeker worden meegeteld of telkens wanneer een bezoeker een conversie voltooit. |
| Ontvangsten | Op basis van conversie | Door het bezoek gegenereerde inkomsten. U kunt uit de volgende opbrengstmetriek kiezen:<ul><li>Opbrengst per bezoeker (RPV)</li><li>Gemiddelde bestelwaarde (AOV)</li><li>Totale verkoop</li><li>Orders</li></ul> |
| Paginaweergaven | Op betrokkenheid gebaseerd | Elk uniek bezoek wordt geteld als conversie. |
| Aangepaste scores | Op betrokkenheid gebaseerd | Geaggregeerde score op basis van de waarde die is toegewezen aan pagina&#39;s die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergave van de activiteit ziet [!DNL Target] verzoek. |
| Tijd op de site | Op betrokkenheid gebaseerd | Tijd doorgebracht in het bezoek (in seconden) vanaf het punt waarop de bezoeker de eerste weergave van de activiteit ziet [!DNL Target] verzoek om de laatste pagina te laden met een verzoek in de sessie. |

Voor op betrokkenheid gebaseerde metriek (in tegenstelling tot op conversie gebaseerde en op opbrengst-gebaseerde metriek) moeten bezoekers opnieuw in aanmerking komen voor de activiteit op elk bezoek om de telling voor die zitting te verhogen. De bijbehorende metrische waarde begint na herkwalificatie te stijgen en stopt aan het einde van de sessie van elke bezoeker. Een sessie eindigt na 30 minuten inactiviteit. Daarom zult u resultaten niet onmiddellijk tijdens het testen zien; alle resultaten van die sessie zijn echter beschikbaar binnen een paar minuten na afloop van de sessie .

## Aangepaste succescijfers

U kunt ook aangepaste succesmaatstaven maken.

Selecteer de maatstaf voor succes en selecteer de actie die een bezoeker heeft uitgevoerd om het doel te bereiken. Kies bijvoorbeeld een [!UICONTROL Conversion] metrisch, plaats het om één keer per bezoeker te tellen, dan plaats of het succes wordt bereikt wanneer een bezoeker een bepaalde pagina (of een reeks pagina&#39;s) bekijkt, bekijkt een specifieke [!DNL Target] of op een specifieke koppeling klikken.

Indien ingeschakeld, wordt de [!UICONTROL Estimated Value of one conversion] veld (niet beschikbaar voor de [!UICONTROL Page Score] metriek) verstrekt een waarde voor uw doel, maar niet voor andere metriek. Deze waarde schakelt [!DNL Target] een geraamde verhoging van de inkomsten te berekenen. Dit veld is facultatief; de incrementele inkomsten voor elke metrische waarde die geen inkomsten oplevert, kunnen echter niet zonder deze methode worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency. Zie [Schatting van de opbrengst](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie .

De succesmetriek u voor uw activiteit kiest zijn beschikbaar in de rapportmontages wanneer u een rapport voor de activiteit bekijkt.

Sommige metriek, zoals [!UICONTROL Custom Scoring] en [!UICONTROL Revenue Per Visitor]hebt u een aangepaste implementatie nodig die gegevens zoals ordertotalen en bestellings-id&#39;s doorgeeft.

## Geavanceerde instellingen {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Gebruik de geavanceerde instellingen om te bepalen hoe succesvol u bent. De opties omvatten het toevoegen van gebiedsdelen, het kiezen of om de gebruiker in de activiteit te houden of hen te verwijderen, en of om metrisch één keer per ingang of op elke indruk te tellen.

Om toegang te krijgen tot [!UICONTROL Advanced Settings] klikt u op de knop **[!UICONTROL vertical ellipses]** > **[!UICONTROL Advanced Settings]**.

![Het menu Geavanceerde instellingen](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als uw rapporteringsbron, worden de montages beheerd door [!DNL Analytics] server. De [!UICONTROL Advanced Settings] is niet beschikbaar. Zie voor meer informatie [Adobe Analytics als bron van rapportage voor Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Afhankelijkheid toevoegen

U kunt de geavanceerde montages gebruiken om afhankelijke succesmetriek tot stand te brengen, die één metrisch slechts verhogen als een bezoeker een andere metrische eerste bereikt.

![Afhankelijkheid toevoegen](/help/main/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

Een testconversie is bijvoorbeeld alleen geldig als een bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat deze wordt omgezet.

Afhankelijkheidsfunctionaliteit is *niet* ondersteund voor:

* [!UICONTROL Recommendations] activiteiten. Deze functionaliteit wordt ondersteund voor alle andere typen activiteiten.
* Als u [Analyses als uw rapportbron](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Het metrische type &quot;Viewed a Page&quot;.
* Het metrische type &quot;Clicked an Element&quot; voor VEC-activiteiten (Visual Experience Composer).

Afhankelijke succeswaarden worden in de volgende gevallen niet omgezet:

* Als u een cirkelgebiedsdeel creeert waarin metrisch1 van metrisch2 afhankelijk is en metrisch2 van metrisch1 afhankelijk is, kan noch metrisch omzetten.
* Bij Automated Personalization-activiteiten worden gebruikers vrijgegeven en wordt de activiteit opnieuw opgestart wanneer conversiemetriek wordt bereikt. Eventuele metrische gegevens die afhankelijk zijn van de conversiemetrie worden dus niet omgezet.

### Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet?

Gebruik de geavanceerde montages om te bepalen wat gebeurt nadat een gebruiker het doel metrisch bereikt. In de volgende tabel staan de beschikbare opties:

| Nadat een gebruiker dit metrische doel heeft aangetroffen | Opties |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | Geef op hoe het aantal wordt verhoogd:<ul><li>Eenmaal per deelnemer (standaard)</li><li>Bij elke afbeelding, pagina-vernieuwingen uitsluiten</li><li>Op elke indruk</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | Selecteer de ervaring die de bezoeker ziet als ze de activiteit opnieuw betreden:<ul><li>Zelfde ervaring (standaard)</li><li>Willekeurige ervaring</li><li>Onzichtbare ervaring</li></ul> |
| [!UICONTROL Increment Count, Release User, & Bar from Reentry] | Bepaal wat de gebruiker ziet in plaats van de inhoud van de activiteit:<ul><li>Dezelfde ervaring, zonder reeksspatiëring (standaard)</li><li>Standaardinhoud of andere activiteiteninhoud</li></ul> |

>[!NOTE]
>
>Als u metrisch aan één van het [!UICONTROL Increment Count] (hierboven vermeld), neemt het metrische aantal correct toe één keer per ingang op het niveau van de bezoeker slechts. De metrische tellingen stijgen eens per bezoek voor elke nieuwe zitting op het bezoekniveau.

### Hoe zal het aantal worden verhoogd:

Kies het gewenste gedrag:

* Eenmaal per gegadigde
* Op elke indruk (pagina-vernieuwingen uitsluiten)
* Op elke indruk

## Trainingsvideo: Activiteitenstatistieken

In deze video&#39;s wordt uitgelegd hoe u de maatstaven voor activiteiten kunt gebruiken.

* Begrijp &quot;doel&quot;metriek
* Omzetten, Inkomsten en Betrokkenheid begrijpen en bouwen
* Bouw metrisch klikken-volgend

>[!VIDEO](https://video.tv.adobe.com/v/17380)
