---
keywords: Doelstelling;succes;omzettingsmetrische;paginascore;metrische paginamontages;opbrengstmetriek;tijd op plaats metrisch;geschatte waarde;geavanceerde montages;succesmetriek;gebiedsdeel;Afhankelijkheid;De Telling van de verhoging & houdt Gebruiker in Activiteit;De Telling van de verhoging, de gebruiker van de Versie, & Toestaan de Telling van de verhoging, de Gebruiker van de Versie, & Bar van Ingang
description: Leer meer over succesmetriek die u helpen het succes van een activiteit bepalen. Tot de succesmetriek behoren Conversie, Inkomsten, Paginaweergaven, Aangepaste score en Tijd op de site.
title: Wat zijn succescijfers?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: a34d40bef584bfa941731df718cb402c658f5d28
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 0%

---

# [!UICONTROL Success metrics]

Succeswaarden in [!DNL Adobe Target] zijn belangrijke indicatoren die de prestaties van uw activiteiten helpen meten. Deze metriek vangen belangrijke bedrijfsresultaten zoals omzettingen, opbrengst per bezoeker, en klantenovereenkomst aan, die u toestaan om het effect van specifieke ervaringen of aanbiedingen te evalueren.

U kunt bijvoorbeeld bijhouden of een nieuwe aanbieding de omzet per bezoeker verhoogt of ertoe leidt dat er meer objecten aan winkelwagentjes worden toegevoegd. Succeswaarden helpen u ook problemen in gebruikersstromen te identificeren, zoals registratie-, afrekenings- of aankoopprocessen, terwijl ze inzichten bieden in het algemene gedrag van de bezoeker.

## Overzicht

In [!DNL Target] zijn succesmetriek vooraf geconfigureerd met de aanbevolen instellingen voor nauwkeurige rapportage en effectieve tracering.

Conversiegebeurtenissen gebruiken standaard de instelling **[!UICONTROL Increment count & keep user in activity].** Deze instelling houdt in dat elke bezoeker slechts eenmaal wordt geteld als een conversie. Geen herhaalde omzettingen worden geteld. Deze bezoekers blijven de inhoud van de activiteit tijdens hun zitting zien.

Voor inkomstenmetriek die het zelfde plaatsen gebruiken, slechts de eerste orde van een bezoeker registreert orderdetails. Terwijl volgende bestellingen het aantal conversies verhogen, dragen ze niet bij aan op inkomsten gebaseerde meetwaarden zoals [!UICONTROL Revenue per Visitor (RPV)] , [!UICONTROL Average Order Value (AOV)] of [!DNL Total Sales] . Deze extra bestellingen worden ook uitgesloten van het rapport [!UICONTROL Order Details] .

>[!NOTE]
>
>Voor activiteiten die [&#x200B; Analytics als rapporterende bron &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) gebruiken (A4T), het doel metrisch gebruikt altijd &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; en &quot;[!UICONTROL On Every Impression]&quot;montages. Deze montages zijn *niet* configureerbaar.

De volgende maatstaven voor succes kunnen worden geconfigureerd in de sectie [!UICONTROL Reporting Settings] op de [!UICONTROL Activity Settings page] , onder de stap [!UICONTROL Goals & Settings] :

| Metrisch met succes | Meetmethode | Definitie |
|--- |--- |--- |
| [!UICONTROL Conversion] | Op basis van conversie | Omzetten is wanneer een bezoeker een door u gedefinieerde handeling op uw site uitvoert, zoals <ul><li>Pagina&#39;s weergeven</li><li>Een box weergegeven</li><li>Op een element klikken</li></ul>Een conversie kan één keer per bezoeker worden meegeteld of telkens wanneer een bezoeker een conversie voltooit. |
| [!UICONTROL Revenue] | Op basis van conversie | Door het bezoek gegenereerde inkomsten. U kunt slechts één metrische omzet kiezen:<ul><li>Een box weergegeven</li></ul>Voor meer informatie over veranderingen in bijgewerkte [!DNL Target] UI aangezien het aan de metriek van het opbrengstsucces heeft, zie [&#x200B; Bijgewerkte  [!DNL Target]  veranderingen UI &#x200B;](#changes) hieronder. |
| [!UICONTROL Engagement] | Op betrokkenheid gebaseerd | Betrokkenheid bij het bezoek. U kunt uit de volgende betrokkenheidsmetriek kiezen:<UL><li>Paginaweergaven: elk uniek bezoek wordt geteld als een conversie.</li><li>[!UICONTROL Custom Scoring]: geaggregeerde score op basis van de waarde die is toegewezen aan pagina&#39;s die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergave van de [!DNL Target] -aanvraag van de activiteit ziet.</li>[!DNL Time on Site]: De tijd die in het bezoek (in seconden) is doorgebracht vanaf het punt waarop de bezoeker de eerste weergave [!DNL Target] van de activiteit ziet bij het laden van de laatste pagina met een aanvraag in de sessie.</UL> |

Voor op betrokkenheid gebaseerde metriek (in tegenstelling tot op conversie gebaseerde en op opbrengst-gebaseerde metriek), moeten de bezoekers voor de activiteit op elk bezoek opnieuw kwalificeren om de telling voor die zitting te verhogen. De bijbehorende metrische waarde begint na herkwalificatie te stijgen en stopt aan het einde van de sessie van elke bezoeker. Een sessie eindigt na 30 minuten inactiviteit. Daarom ziet u niet onmiddellijk resultaten tijdens het testen; nochtans, zijn alle resultaten van die zitting beschikbaar binnen een paar notulen van de zitting die beëindigt.

## Aangepaste succescijfers

U kunt ook aangepaste succesmaatstaven maken.

Selecteer de maatstaf voor succes en selecteer de actie die een bezoeker heeft uitgevoerd om het doel te bereiken. Kies bijvoorbeeld een [!UICONTROL Conversion] -metrische waarde, stel deze in op één keer per bezoeker en stel vervolgens in of succes wordt geboekt wanneer een bezoeker een bepaalde pagina (of set pagina&#39;s) bekijkt, een specifieke [!DNL Target] -aanvraag weergeeft of op een specifieke koppeling klikt.

Als deze optie is ingeschakeld, biedt het veld [!UICONTROL Estimated Value of one conversion] (niet beschikbaar voor de [!UICONTROL Page Score] -meetgegevens) een waarde voor uw doel, maar niet voor andere meetwaarden. Met deze waarde kan [!DNL Target] een geschatte lift in inkomsten berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), gebruikt de schatting [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency. Zie [&#x200B; Schatting Lift in Inkomsten &#x200B;](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie.

De succesmetriek die u voor uw activiteit kiest zijn beschikbaar in de rapportmontages wanneer u een rapport voor de activiteit bekijkt.

Voor sommige meetgegevens, zoals [!UICONTROL Custom Scoring] en [!UICONTROL Revenue Per Visitor] , is een aangepaste implementatie vereist die gegevens doorgeeft, zoals ordertotalen en bestellings-id&#39;s.

## Geavanceerde instellingen {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Gebruik de geavanceerde instellingen om te bepalen hoe succesvol u bent. De opties omvatten het toevoegen van gebiedsdelen, het kiezen of om de gebruiker in de activiteit te houden of hen te verwijderen, en of om metrisch één keer per ingang of op elke indruk te tellen.

Om tot de [!UICONTROL Advanced Settings] opties toegang te hebben, klik het **[!UICONTROL More Actions]** pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)), dan klik **[!UICONTROL Advanced Settings]**.

![&#x200B; Geavanceerde het menu van Montages &#x200B;](/help/main/c-activities/r-success-metrics/assets/advanced-settings-refresh.png)

Voor meer informatie over [!UICONTROL Advanced Settings] opties (&quot;[!UICONTROL What will happen after a user encounters this goal]&quot; en &quot;[!UICONTROL How will the count be incremented]&quot;) zie [&#x200B; wat gebeurt nadat een gebruiker dit doel metrisch &#x200B;](#what-happens) ontmoet?

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als rapportbron gebruikt, worden de instellingen beheerd door de [!DNL Analytics] -server. De optie [!UICONTROL Advanced Settings] is niet beschikbaar. Voor meer informatie, zie [&#x200B; Adobe Analytics als rapporteringsbron voor Adobe Target (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Afhankelijkheid toevoegen

U kunt de geavanceerde montages gebruiken om afhankelijke succesmetriek tot stand te brengen, die één metrisch slechts verhogen als een bezoeker een andere metrische eerste bereikt.

Een testconversie is bijvoorbeeld alleen geldig als een bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat deze wordt omgezet.

De functionaliteit van de afhankelijkheid wordt *niet* gesteund voor het volgende:

* [!UICONTROL Recommendations] -activiteiten. Deze functionaliteit wordt ondersteund voor alle andere typen activiteiten.
* Als u [&#x200B; Analytics als uw rapporteringsbron &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt.
* Het metrische type &quot;Viewed a Page&quot;.
* Het metrische type &quot;Clicked an Element&quot; voor VEC-activiteiten (Visual Experience Composer).

Afhankelijke succeswaarden worden in de volgende gevallen niet omgezet:

* Als u een cirkelgebiedsdeel creeert waarin metrisch1 van metrisch2 afhankelijk is en metrisch2 van metrisch1 afhankelijk is, kan noch metrisch omzetten.
* Met [!UICONTROL Automated Personalization] -activiteiten kunnen gebruikers de activiteit vrijgeven en opnieuw starten wanneer conversiemetriek wordt bereikt. Metrische gegevens die afhankelijk zijn van de conversiemetrisch worden dus niet omgezet.

### Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet? {#what-happens}

Gebruik de geavanceerde montages om te bepalen wat gebeurt nadat een gebruiker het doel metrisch bereikt. In de volgende tabel staan de beschikbare opties:

| Nadat een gebruiker dit metrische doel heeft aangetroffen | Opties |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | Geef op hoe het aantal wordt verhoogd:<ul><li>Eenmaal per deelnemer (standaard)</li><li>Bij elke afbeelding, pagina-vernieuwingen uitsluiten</li><li>Op elke indruk</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | Selecteer de ervaring die de bezoeker ziet als hij of zij de activiteit opnieuw betreedt:<ul><li>Zelfde ervaring (standaard)</li><li>Willekeurige ervaring</li><li>Onzichtbare ervaring</li></ul> |
| [!UICONTROL Increment Count, Release User, & Bar from Reentry] | Bepaal wat de gebruiker ziet in plaats van de inhoud van de activiteit:<ul><li>Dezelfde ervaring, zonder reeksspatiëring (standaard)</li><li>Standaardinhoud of andere activiteiteninhoud</li></ul> |

>[!NOTE]
>
>Als u metrisch aan één van de [!UICONTROL Increment Count] (bovengenoemde) opties vormt, neemt de metrische telling correct toe één keer per ingang op het bezoekersniveau slechts. De metrische tellingen stijgen eens per bezoek voor elke nieuwe zitting op het bezoekniveau.

### Hoe wordt het aantal verhoogd:

Kies het gewenste gedrag:

* Eenmaal per gegadigde
* Op elke indruk (pagina-vernieuwingen uitsluiten)
* Op elke indruk

## Bekende problemen

* De metriek van het succes met de geavanceerde optie &quot;hoe de telling&quot;zal worden verhoogd geplaatst aan &quot;elke indruk&quot;of &quot;elke indruk (exclusief vernieuwingen)&quot;kan niet als succes worden gebruikt metrisch dat een andere metrisch afhangt.

  Wanneer een succes metrisch wordt geplaatst om op elke indruk te verhogen, [!DNL Target] telt opnieuw de bezoeker telkens als de bezoeker dit succes metrisch bezoekt. [!DNL Target] herstelt dan het succes metrische &quot;lidmaatschap&quot;aan 0 zodat kan het opnieuw op de volgende indruk tellen. Dus als een andere metrische waarde vereist dat deze metrische waarde als eerste is gezien, herkent [!DNL Target] nooit dat de gebruiker de eerste metrische waarde heeft gezien.

## Bijgewerkte [!DNL Target] UI-wijzigingen {#changes}

De [[!DNL Target Standard/Premium]  versie 25.2.1 &#x200B;](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2), gelanceerd op 17 februari 2015, introduceerde bijgewerkte [!DNL Target] en [!UICONTROL Visual Experience Composer] (VEC) UIs. Deze sectie schetst de belangrijkste verschillen tussen de erfenis en bijgewerkte UI, specifiek aangezien zij op het vormen en het beheren van succesmetriek betrekking hebben.

### Wijzigingen in de gebruikersinterface die betrekking hebben op gegevens over succes van [!UICONTROL Revenue]

In de bijgewerkte interface [!DNL Target] is de vervolgkeuzelijst [!UICONTROL Default View for Reporting] verwijderd. Dit veld is overbodig omdat eerder de standaardrapportweergave onder [!DNL Overview] > [!UICONTROL Reports] is opgeslagen in de oudere gebruikersinterface.

Met de bijgewerkte UI, is standaard rapporteringsmetrisch nu altijd plaatste aan [!UICONTROL Revenue per Visitor (RPV)]. U kunt de weergave in de sectie [!UICONTROL Reports] nog steeds aanpassen om metriek weer te geven die het meest relevant zijn voor uw analyse.

Deze wijziging heeft geen invloed op de maatstaven van de levering. Deze wijziging is alleen van invloed op het standaardfilter dat in de rapportweergave wordt weergegeven. Omdat RPV het meest gebruikte metrisch onder klanten is, werd dit gebrek geselecteerd om rapporteringswerkschema&#39;s te stroomlijnen. U kunt op elk gewenst moment binnen de sectie [!UICONTROL Reports] naar andere metriek overschakelen.