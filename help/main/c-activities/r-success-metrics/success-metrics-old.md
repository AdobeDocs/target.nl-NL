---
keywords: Doelstelling;succes;omzettingsmetrische;paginascore;metrische paginamontages;opbrengstmetriek;tijd op plaats metrisch;geschatte waarde;geavanceerde montages;succesmetriek;gebiedsdeel;Afhankelijkheid;De Telling van de verhoging & houdt Gebruiker in Activiteit;De Telling van de verhoging, de gebruiker van de Versie, & Toestaan de Telling van de verhoging, de Gebruiker van de Versie, & Bar van Ingang
description: Leer over succesmetriek in Adobe  [!DNL Target]  die u helpen het succes van een activiteit bepalen. Tot de succesmetriek behoren Conversie, Inkomsten, Paginaweergaven, Aangepaste score en Tijd op de site.
title: Wat zijn succescijfers?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 0%

---

# Succeswaarden

In [!DNL Adobe Target] zijn succesmetriek parameters die worden gebruikt om het succes van een activiteit te meten. Succesvolle maatstaven omvatten belangrijke bedrijfsmaatregelen waarmee u kunt bepalen of een bepaalde ervaring of aanbieding een [!DNL Target] -activiteit heeft.

U kunt bijvoorbeeld bepalen of een nieuwe aanbieding uw omzet per bezoeker verhoogt of een item aan een winkelwagentje toevoegt. Succeswaarden kunnen nuttig zijn voor het opsporen van problemen met registratie, bestellen of aanschafkanalen, maar ook eenvoudig met betrokkenheid van bezoekers of klanten.

## Overzicht

In [!DNL Target] zijn succesmetriek vooraf geconfigureerd met de optimale opties voor zowel rapportage- als trackingsdoeleinden.

Standaard worden conversiegebeurtenissen ingesteld op &quot;[!UICONTROL Increment count & keep user in activity]&quot;. Conversies worden slechts eenmaal geteld, er worden geen terugkerende conversies geteld en de bezoeker ziet altijd de inhoud van de activiteit.

De metriek van de opbrengst die aan &quot;[!UICONTROL Increment count & keep user in activity]&quot;de gegevens van de logboekorde slechts voor de eerste orde worden geplaatst door de zelfde bezoeker wordt gemaakt. Alle volgende bestellingen verhogen het aantal conversies, maar voegen geen inkomsten toe aan RPV/AOV/Sales en worden niet opgenomen in het [!UICONTROL Order Details] -rapport.

>[!NOTE]
>
>Voor activiteiten die [&#x200B; Analytics als rapporterende bron &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) gebruiken (A4T), zal doel metrisch altijd &quot; [!UICONTROL Increment Count & Keep User in Activity]&quot;en &quot;[!UICONTROL On Every Impression]&quot;montages gebruiken. Dit is *niet* configureerbaar.

De volgende succeswaarden zijn beschikbaar:

| Metrisch met succes | Meetmethode | Definitie |
|--- |--- |--- |
| Conversie | Op basis van conversie | Omzetten is wanneer een bezoeker een door u gedefinieerde handeling op uw site uitvoert, zoals <ul><li>Klik op een knop</li><li>Pagina&#39;s weergeven</li><li>Een enquête voltooid</li><li>Een aankoop gedaan</li></ul>Een conversie kan één keer per bezoeker worden meegeteld of telkens wanneer een bezoeker een conversie voltooit. |
| Ontvangsten | Op basis van conversie | Door het bezoek gegenereerde inkomsten. U kunt uit de volgende opbrengstmetriek kiezen:<ul><li>Opbrengst per bezoeker (RPV)</li><li>Gemiddelde bestelwaarde (AOV)</li><li>Totale verkoop</li><li>Orders</li></ul> |
| Paginaweergaven | Op betrokkenheid gebaseerd | Elk uniek bezoek wordt geteld als conversie. |
| Aangepaste scores | Op betrokkenheid gebaseerd | Geaggregeerde score is gebaseerd op de waarde die is toegewezen aan pagina&#39;s die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergave [!DNL Target] van de activiteit ziet. |
| Tijd op de site | Op betrokkenheid gebaseerd | De tijd die in het bezoek (in seconden) is doorgebracht vanaf het punt waarop de bezoeker de eerste weergave [!DNL Target] van de activiteit ziet die wordt aangevraagd voor de laatste pagina met een aanvraag in de sessie. |

Voor op betrokkenheid gebaseerde metriek (in tegenstelling tot op conversie gebaseerde en op opbrengst-gebaseerde metriek) moeten bezoekers opnieuw in aanmerking komen voor de activiteit op elk bezoek om de telling voor die zitting te verhogen. De bijbehorende metrische waarde begint na herkwalificatie te stijgen en stopt aan het einde van de sessie van elke bezoeker. Een sessie eindigt na 30 minuten inactiviteit. Daarom zult u resultaten niet onmiddellijk tijdens het testen zien; nochtans, zijn alle resultaten van die zitting beschikbaar binnen een paar notulen van de zitting die beëindigt.

## Aangepaste succescijfers

U kunt ook aangepaste succesmaatstaven maken.

Selecteer de maatstaf voor succes en selecteer de actie die een bezoeker heeft uitgevoerd om het doel te bereiken. Kies bijvoorbeeld een [!UICONTROL Conversion] -metrische waarde, stel deze in op één keer per bezoeker en stel vervolgens in of succes wordt geboekt wanneer een bezoeker een bepaalde pagina (of set pagina&#39;s) bekijkt, een specifieke [!DNL Target] -aanvraag weergeeft of op een specifieke koppeling klikt.

Als deze optie is ingeschakeld, biedt het veld [!UICONTROL Estimated Value of one conversion] (niet beschikbaar voor de [!UICONTROL Page Score] -meetgegevens) een waarde voor uw doel, maar niet voor andere meetwaarden. Met deze waarde kan [!DNL Target] een geschatte lift in inkomsten berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), gebruikt de schatting [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency. Zie [&#x200B; Schatting Lift in Inkomsten &#x200B;](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie.

De succesmetriek u voor uw activiteit kiest zijn beschikbaar in de rapportmontages wanneer u een rapport voor de activiteit bekijkt.

Voor sommige meetgegevens, zoals [!UICONTROL Custom Scoring] en [!UICONTROL Revenue Per Visitor] , is een aangepaste implementatie vereist die gegevens doorgeeft, zoals de totalen van de volgorde en de id&#39;s van de bestelling.

## Geavanceerde instellingen {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Gebruik de geavanceerde instellingen om te bepalen hoe succesvol u bent. De opties omvatten het toevoegen van gebiedsdelen, het kiezen of om de gebruiker in de activiteit te houden of hen te verwijderen, en of om metrisch één keer per ingang of op elke indruk te tellen.

Klik op [!UICONTROL Advanced Settings] > **[!UICONTROL vertical ellipses]** om de **[!UICONTROL Advanced Settings]** -opties te openen.

![&#x200B; Geavanceerde het menu van Montages &#x200B;](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als rapportbron gebruikt, worden de instellingen beheerd door de [!DNL Analytics] -server. De optie [!UICONTROL Advanced Settings] is niet beschikbaar. Voor meer informatie, zie [&#x200B; Adobe Analytics als rapporteringsbron voor Adobe Target (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Afhankelijkheid toevoegen

U kunt de geavanceerde montages gebruiken om afhankelijke succesmetriek tot stand te brengen, die één metrisch slechts verhogen als een bezoeker een andere metrische eerste bereikt.

![&#x200B; voeg Afhankelijkheid &#x200B;](/help/main/c-activities/r-success-metrics/assets/UI_dep_success_metric.png) toe

Een testconversie is bijvoorbeeld alleen geldig als een bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat deze wordt omgezet.

De functionaliteit van de afhankelijkheid wordt *niet* gesteund voor het volgende:

* [!UICONTROL Recommendations] -activiteiten. Deze functionaliteit wordt ondersteund voor alle andere typen activiteiten.
* Als u [&#x200B; Analytics als uw rapporteringsbron &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt.
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
>Als u metrisch aan één van de [!UICONTROL Increment Count] (bovengenoemde) opties vormt, neemt de metrische telling correct toe één keer per ingang op het bezoekersniveau slechts. De metrische tellingen stijgen eens per bezoek voor elke nieuwe zitting op het bezoekniveau.

### Hoe zal het aantal worden verhoogd:

Kies het gewenste gedrag:

* Eenmaal per gegadigde
* Op elke indruk (pagina-vernieuwingen uitsluiten)
* Op elke indruk

## Bekende problemen

* De metriek van het succes met de geavanceerde optie &quot;hoe de telling&quot;zal worden verhoogd geplaatst aan &quot;elke indruk&quot;of &quot;elke indruk (exclusief vernieuwingen)&quot;kan niet als succes worden gebruikt metrisch dat een andere metrisch afhangt.

Wanneer een succes metrisch wordt geplaatst om op elke indruk te verhogen, [!DNL Target] telt opnieuw de bezoeker telkens als de bezoeker dit succes metrisch bezoekt. [!DNL Target] herstelt dan het succes metrische &quot;lidmaatschap&quot;aan 0 zodat kan het opnieuw op de volgende indruk tellen. Dus als een andere metrische waarde vereist dat deze metrische waarde als eerste is gezien, herkent [!DNL Target] nooit dat de gebruiker de eerste metrische waarde heeft gezien.

## Trainingsvideo: Activiteitenstatistieken

In deze video&#39;s wordt uitgelegd hoe u de maatstaven voor activiteiten kunt gebruiken.

* Begrijp &quot;doel&quot;metriek
* Omzetten, Inkomsten en Betrokkenheid begrijpen en bouwen
* Een metrisch object voor klikken bijhouden maken

>[!VIDEO](https://video.tv.adobe.com/v/17380)
