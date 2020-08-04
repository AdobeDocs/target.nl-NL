---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics;advanced settings
description: In Adobe Target zijn succesmetriek parameters die worden gebruikt om het succes van een activiteit te meten. Succeswaarden omvatten belangrijke bedrijfsmaatregelen waarmee u het succes van een bepaalde ervaring of aanbieding in een Target-activiteit kunt bepalen.
title: Succeswaarden in Adobe Target
uuid: 24e9ae0f-099b-430b-b2bb-03b405f88929
translation-type: tm+mt
source-git-commit: 4fd2de5600060d58759ffa54a771a45b263f115b
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 0%

---


# Succeswaarden{#success-metrics}

In [!DNL Adobe Target] succesmetriek zijn parameters die worden gebruikt om het succes van een activiteit te meten. De metriek van het succes omvat zeer belangrijke bedrijfsmaatregelen die u toelaten om het succes van een bepaalde ervaring of een aanbieding in een [!DNL Target] activiteit te bepalen.

U kunt bijvoorbeeld bepalen of een nieuwe aanbieding uw omzet per bezoeker verhoogt of een item aan een winkelwagentje toevoegt. Succeswaarden kunnen nuttig zijn voor het opsporen van problemen met registratie, bestellen of aanschafkanalen, maar ook eenvoudig met betrokkenheid van bezoekers of klanten.

## Overzicht

In [!DNL Target], worden de succesmetriek pre-gevormd met de optimale opties voor zowel het melden als het volgen doeleinden.

Conversiegebeurtenissen worden standaard ingesteld op &quot;[!UICONTROL Increment count & keep user in activity].&quot; Conversies worden slechts eenmaal geteld, er worden geen terugkerende conversies geteld en de bezoeker ziet altijd de inhoud van de activiteit.

De metriek van de opbrengst die aan &quot;[!UICONTROL Increment count & keep user in activity]&quot;logboekorddetails slechts voor de eerste orde worden geplaatst door de zelfde bezoeker. Alle daaropvolgende bestellingen verhogen het aantal conversies, maar voegen geen inkomsten toe aan RPV/AOV/Sales en worden niet in het [!UICONTROL Order Details] rapport opgenomen.

>[!NOTE]
>
>Het standaardgedrag voor activiteiten waarbij [Analytics als rapportagebron](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) wordt gebruikt, is &quot;[!UICONTROL Increment count & keep user in activity]&quot; met &quot;[!UICONTROL Once per entrant].&quot;

De volgende succeswaarden zijn beschikbaar:

| Metrisch met succes | Meetmethode | Definitie |
|--- |--- |--- |
| Conversie | Op basis van conversie | Omzetten is wanneer een bezoeker een door u gedefinieerde handeling op uw site uitvoert, zoals <ul><li>Klik op een knop</li><li>Pagina&#39;s weergeven</li><li>Een enquête voltooid</li><li>Een aankoop gedaan</li></ul>Een conversie kan één keer per bezoeker worden meegeteld of telkens wanneer een bezoeker een conversie voltooit. |
| Ontvangsten | Op basis van conversie | Door het bezoek gegenereerde inkomsten. U kunt uit de volgende opbrengstmetriek kiezen:<ul><li>Opbrengst per bezoeker (RPV)</li><li>Gemiddelde bestelwaarde (AOV)</li><li>Totale verkoop</li><li>Orders</li></ul> |
| Paginaweergaven | Op betrokkenheid gebaseerd | Elk uniek bezoek wordt geteld als conversie. |
| Aangepaste scores | Op betrokkenheid gebaseerd | Geaggregeerde score is gebaseerd op de waarde die is toegewezen aan pagina&#39;s die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergave- [!DNL Target] aanvraag van de activiteit ziet. |
| Tijd op de site | Op betrokkenheid gebaseerd | De tijd die in het bezoek (in seconden) wordt doorgebracht vanaf het punt waarop de bezoeker het eerste weergaveverzoek van de activiteit ziet voor het laden van de laatste pagina met een verzoek in de sessie. [!DNL Target] |

Voor op betrokkenheid gebaseerde metriek (in tegenstelling tot op conversie gebaseerde en op opbrengst-gebaseerde metriek) moeten bezoekers opnieuw in aanmerking komen voor de activiteit op elk bezoek om de telling voor die zitting te verhogen. De bijbehorende metrische waarde begint na herkwalificatie te stijgen en stopt aan het einde van de sessie van elke bezoeker. Een sessie eindigt na 30 minuten inactiviteit. Daarom zult u resultaten niet onmiddellijk tijdens het testen zien; alle resultaten van die sessie zijn echter beschikbaar binnen een paar minuten na afloop van de sessie .

## Aangepaste succescijfers

U kunt ook aangepaste succesmaatstaven maken.

Selecteer de maatstaf voor succes en selecteer de actie die een bezoeker heeft uitgevoerd om het doel te bereiken. Kies bijvoorbeeld een [!UICONTROL Conversion] metrische waarde, stel in dat de waarde één keer per bezoeker moet worden geteld en stel vervolgens in of succes wordt behaald wanneer een bezoeker een bepaalde pagina (of set pagina&#39;s) bekijkt, een specifieke [!DNL Target] aanvraag weergeeft of op een specifieke koppeling klikt.

Als deze optie is ingeschakeld, levert het [!UICONTROL Estimated Value of one conversion] veld (niet beschikbaar voor de [!UICONTROL Page Score] meetgegevens) een waarde voor uw doel, maar niet voor andere meetwaarden. Met deze waarde kan een geschatte lift in inkomsten [!DNL Target] worden berekend. Dit veld is facultatief; de incrementele inkomsten voor elke metrische waarde die geen inkomsten oplevert, kunnen echter niet zonder deze methode worden berekend. Voor alle opbrengstmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), gebruikt de raming [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency. Zie [Schatting van Lift in Revenue](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie.

De succesmetriek u voor uw activiteit kiest zijn beschikbaar in de rapportmontages wanneer u een rapport voor de activiteit bekijkt.

Sommige metriek, zoals [!UICONTROL Custom Scoring] en [!UICONTROL Revenue Per Visitor], vereisen een aangepaste implementatie die in informatie zoals ordetotalen en orde IDs overgaat.

## Geavanceerde instellingen {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Gebruik de geavanceerde instellingen om te bepalen hoe succesvol u bent. U kunt onder andere de metrische waarde per impositie of één keer per bezoeker tellen en kiezen of u de gebruiker in de activiteit wilt houden of deze wilt verwijderen.

Klik op [!UICONTROL Advanced Settings] > om de **[!UICONTROL vertical ellipses]** opties te openen **[!UICONTROL Advanced Settings]**.

![Het menu Geavanceerde instellingen](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als rapportbron gebruikt, worden de instellingen beheerd door de [!DNL Analytics] server. De [!UICONTROL Advanced Settings] optie is niet beschikbaar. Zie [Adobe Analytics als de rapportagebron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md)voor meer informatie.

U kunt de geavanceerde montages ook gebruiken om afhankelijke succesmetriek tot stand te brengen, die één metrisch slechts verhogen als een bezoeker een andere metrische eerste bereikt.

![Afhankelijkheid toevoegen](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

Een testconversie is bijvoorbeeld alleen geldig als een bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat deze wordt omgezet.

Afhankelijke succeswaarden worden ondersteund in A/B-tests, Automated Personalization, Experience Targeting en Multivariate testactiviteiten. Recommendations-activiteiten ondersteunen momenteel geen afhankelijke succesmaatstaven.

>[!NOTE]
>
>Afhankelijke succeswaarden worden in de volgende gevallen niet omgezet:
>
>* Als u een cirkelgebiedsdeel creeert waarin metrisch1 van metrisch2 afhankelijk is en metrisch2 van metrisch1 afhankelijk is, kan noch metrisch omzetten.
>* Bij Automated Personalization-activiteiten worden gebruikers vrijgegeven en wordt de activiteit opnieuw opgestart wanneer conversiemetriek wordt bereikt. Eventuele metrische gegevens die afhankelijk zijn van de conversiemetrie worden dus niet omgezet.


Gebruik de geavanceerde montages om te bepalen wat gebeurt nadat een gebruiker het doel metrisch bereikt. In de volgende tabel staan de beschikbare opties:

| Nadat een gebruiker dit metrische doel heeft aangetroffen | Opties |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | Geef op hoe het aantal wordt verhoogd:<ul><li>Eenmaal per deelnemer (standaard)</li><li>Bij elke afbeelding, pagina-vernieuwingen uitsluiten</li><li>Op elke indruk</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | Selecteer de ervaring die de bezoeker ziet als ze de activiteit opnieuw betreden:<ul><li>Zelfde ervaring (standaard)</li><li>Willekeurige ervaring</li><li>Onzichtbare ervaring</li></ul> |
| [!UICONTROL Increment Count, Release User, & Bar from Reentry] | Bepaal wat de gebruiker ziet in plaats van de inhoud van de activiteit:<ul><li>Dezelfde ervaring, zonder reeksspatiëring (standaard)</li><li>Standaardinhoud of andere activiteiteninhoud</li></ul> |

>[!NOTE]
>
>Als u metrisch aan één van de (bovengenoemde) opties vormt, neemt de metrische telling correct toe eens per ingang op het bezoekersniveau slechts. [!UICONTROL Increment Count] De metrische tellingen stijgen eens per bezoek voor elke nieuwe zitting op het bezoekniveau.

## Trainingsvideo: Activiteitenstatistieken

In deze video&#39;s wordt uitgelegd hoe u de maatstaven voor activiteiten kunt gebruiken.

* Begrijp &quot;doel&quot;metriek
* Omzetten, Inkomsten en Betrokkenheid begrijpen en bouwen
* Bouw metrisch klikken-volgend

>[!VIDEO](https://video.tv.adobe.com/v/17380)