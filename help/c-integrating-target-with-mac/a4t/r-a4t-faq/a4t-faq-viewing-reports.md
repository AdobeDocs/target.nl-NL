---
keywords: faq;frequently asked questions;analytics for target;a4T;report;reports;view reports;reporting;counting methodology;impressions;visitors;visits;default metric;activity conversions;unspecified
description: Dit onderwerp bevat antwoorden op vragen die vaak over het bekijken van rapporten wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.
title: Rapporten weergeven - Veelgestelde vragen voor A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 6659e444ffd680d87a90ded6bb9020a90ea22433
workflow-type: tm+mt
source-wordcount: '2244'
ht-degree: 1%

---


# Rapporten weergeven - Veelgestelde vragen voor A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gevraagd over het bekijken van rapporten wanneer het gebruiken van [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T).

## Kan ik mijn doelactiviteitengegevens in Analysis Workspace bekijken? {#workspace}

U kunt [!DNL Analysis Workspace] gebruiken om uw [!DNL Target] activiteiten en ervaringen te analyseren. Met de [Analytics voor het doelvenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) kunt u optillen en vertrouwen voor maar liefst drie succesmetingen zien. U kunt ook dieper graven met behulp van tabellen en visualisaties.

Voor gedetailleerde informatie en voorbeelden opent u [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), geleverd door Adobe Experience League.

## Waar kunnen segmenten worden toegepast in Analysis Workspace? {#segmentation}

Segmenten worden meestal toegepast op de bovenkant van een deelvenster in de neerzetzone van het segment. Het segment wordt toegepast op alle tabellen en visualisaties in het deelvenster. Deze techniek is het meest nuttig om te zien hoe de test een subset mensen beïnvloedt (bijvoorbeeld hoe heeft deze test voor mensen in het Verenigd Koninkrijk gepresteerd).

## Wanneer ik een klapsegment voor een specifieke activiteit van het Doel toepast, waarom zie ik verwante ervaringen teruggekeerd? {#activity-segmentation}

De variabele [!DNL Target] die naar [!DNL Analytics] wordt verzonden heeft een standaardvervalperiode van 90 dagen. (Opmerking: deze vervalperiode kan indien nodig door de klantenservice worden aangepast). Wanneer bezoekers door de site navigeren gedurende dit verloopvenster, maken ze deel uit van veel [!DNL Target]-activiteiten, die allemaal in de dimensie worden verzameld.

Dientengevolge, wanneer u voor een activiteit segmenteert om in een klap aanwezig te zijn, zult u alle ervaringen krijgen die deel van die activiteit *plus* om het even welke andere ervaringen uitmaken die op die klap voortzetten.

## Waarom heb ik tijdens het configureren van mijn Goal Metics geen toegang tot Geavanceerde instellingen?

Voor activiteiten die [!DNL Analytics] als rapporteringsbron (A4T) gebruiken, zal doel metrisch altijd &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;en &quot;[!UICONTROL On Every Impression]&quot;montages gebruiken. Dit is *niet* configureerbaar.

Voor meer informatie, zie &quot;terwijl het vormen van mijn doelmetica, waarom kan ik niet tot de Geavanceerde opties van Montages toegang hebben?&quot; in [Metrische definities - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Moet ik bezoekers, bezoeken, of activiteit impressies als mijn normaliserende metrisch (d.w.z. telmethode) gebruiken? {#metrics}

Er zijn verscheidene opties voor het normaliseren van metriek in A4T rapportering. Deze maatstaf, ook wel de telmethode genoemd, wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast.

* ***Unieke*** bezoeker die eenmaal in aanmerking komt voor een activiteit.
* ***De*** Bezoekopdracht voor elke zitting zodra een gebruiker (Unieke Bezoeker) een activiteit ingaat, zelfs als de activiteit niet in verdere bezoeken wordt bekeken.
* ***De*** impressiesnelheid van de activiteit neemt toe telkens wanneer de inhoud van de activiteit wordt gediend. (Gemeten door [!DNL Target]).

Wanneer een bezoeker een pagina weergeeft die een activiteit bevat, wordt een variabele ingesteld voor die bezoeker die de naam van die activiteit bevat. Zie de gedetailleerde scenario&#39;s hieronder voor hoe elke telmethode vergelijkt.

Overweeg het volgende:

* Alle bovenstaande metrische trigger wanneer een gebruiker in aanmerking komt voor een activiteit en inhoud wordt geretourneerd van [!DNL [!DNL Target]]. Dit betekent niet noodzakelijk dat de gebruiker het aanbod zag. Als een activiteitservaring onder de vouw is en de gebruiker niet onderaan de pagina scrolt, dan werd de aanbieding gediend door [!DNL Target] maar niet door de gebruiker gezien.
* [!UICONTROL Activity Impressions] (gemeten door  [!DNL Target]) en  [!UICONTROL Instances] (gemeten door  [!DNL Analytics]) zijn gelijk, tenzij er meerdere mbox-aanroepen zijn op dezelfde pagina in dezelfde activiteit. Hierdoor worden meerdere [!UICONTROL Activity Impressions] geteld, maar slechts één [!UICONTROL Instance].

## Waarom zijn &#39;activity impressions&#39; en &#39;activity conversions&#39; in Analysis Workspace hoger dan Reports &amp; Analytics? {#sametouch}

[!DNL Reports & Analytics] past een attributiemodel met dezelfde aanraakinstelling toe op &quot;activity impressions&quot; en &quot;activity conversions&quot;, terwijl de onbewerkte maateenheden  [!DNL Analysis Workspace] worden weergegeven, die opgeblazen kunnen lijken als gevolg van de persistentie van de  [!DNL Target] dimensie.

Om nauwkeurige [!UICONTROL Activity Impressions] en [!UICONTROL Activity Conversions] metriek in [!DNL Analysis Workspace] te evalueren, zorg ervoor dat beide metriek [!UICONTROL Same Touch] toegepaste attributiemodellen hebben. Modellen kunnen worden toegepast door op het tandwieltje voor kolominstellingen te klikken, [!UICONTROL Non-default attribution models] in te schakelen en vervolgens [!UICONTROL Same Touch] te selecteren. Meer informatie over attributie in [Overzicht van Attributen IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) in *Handleiding Analytics Tools*.

## Wat betekent de &quot;activiteitomzettingen&quot;als de teller een metrische Analyse tijdens activiteitenopstelling plukt? {#section_F3EBACF85AF846E9B366A549AAB64356}

De &quot;omzettingen van de Activiteit&quot;zal leeg zijn als [!DNL Analytics] metrisch als omzettingsmetrisch voor de activiteit werd geselecteerd.

## Waarom zie ik &quot;niet gespecificeerd&quot; in de analytische rapporten? Wat betekent het? {#unspecified}

In andere rapporten betekent &quot;niet gespecificeerd&quot; dat gegevens niet aan een classificatieregel voldeden, maar in A4T zou dit nooit mogen gebeuren. Als je &#39;unspecified&#39; ziet, dan is de classificatieservice nog niet gestart. Over het algemeen duurt het 24 tot 72 uur voordat gegevens over de activiteit in de rapporten worden weergegeven. Hoewel de activiteiten pas op dat moment in dit verslag worden vermeld, worden alle bezoekersgegevens die met deze activiteiten verband houden, vastgelegd en weergegeven wanneer de classificatie is voltooid.

Na de rubriceringsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

## Waarom worden de metriek van het Doel verzonden naar Analytics zelfs nadat de activiteit is gedeactiveerd? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

De variabele [!DNL Target] die naar [!DNL Analytics] wordt verzonden heeft een standaardvervalperiode van 90 dagen. Deze vervalperiode kan indien nodig door de klantenservice worden aangepast. Deze instelling is echter algemeen voor alle activiteiten, zodat ze niet voor één geval hoeft te worden aangepast.

U kunt [!DNL Target] variabelen zien die naar [!DNL Analytics] na de vervalperiode worden verzonden omdat de vervaldatum 90 dagen is, maar slechts als die gebruiker een andere A4T-Toegelaten [!DNL Target] activiteit nooit ziet. Als een gebruiker op dag 45 terugkomt naar de site en een andere activiteit ziet, wordt de teller van de hele A4T-eVar opnieuw ingesteld op 90 dagen. Dat betekent dat de eerste campagne vanaf dag 1 nu tot 45 + 90 = 135 dagen zou kunnen duren. Als de gebruiker blijft terugkomen, zou u aan het punt kunnen krijgen waar u metriek die naar [!DNL Analytics] in uw rapportering van veel oudere activiteiten wordt verzonden. Wanneer gebruikers cookies verwijderen en niet terugkeren naar de site, gaan de nummers in die activiteit verloren, maar blijven deze zichtbaar.

Dit betekent dat de activiteiten nog steeds paginaweergaven krijgen, bezoeken, enzovoort, tot 90 dagen nadat de activiteit eindigt voor bezoekers die deel uitmaakten van de activiteit terwijl deze actief was. Als u echter naar de metrische waarde [!UICONTROL Activity Impressions] kijkt, ziet u geen indrukken nadat de activiteit is beëindigd.

Dit is normaal en verwacht gedrag. De variabele A4T werkt net als elke andere eVar. De waarde wordt aan de gebruiker gekoppeld totdat deze de verlooptijdperiode (90 dagen) bereikt. Als een activiteit slechts twee weken actief is, wordt de waarde dus nog steeds geassocieerd met de gebruiker gedurende ten minste de volgende 90 dagen.

De beste praktijken zijn meningsrapporten voor die activiteit slechts voor de periode dat de activiteit levend was. Als u de activiteit in [!DNL Analytics] weergeeft, moeten de datums standaard correct worden ingesteld. Tenzij u de datum handmatig hebt verlengd, moet dit dus geen kwestie zijn vanuit rapportoogpunt.

Laten we er bijvoorbeeld van uitgaan dat de variabele A4T na 90 dagen vervalt en dat onze test van 1 januari tot en met 15 januari actief is.

Op 1 januari komt de gebruiker naar de site en ziet activiteit XYZ eenmaal en heeft daarna vijf paginaweergaven. In de komende twee weken keert de gebruiker nooit terug naar de site. De gegevens zien er voor deze gebruiker als volgt uit:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 3 | 5 | 3 | 3 |

De gebruiker keert op 1 Februari terug, bekijkt vijf meer pagina&#39;s, en ontmoet geen meer activiteiten van het Doel en de originele activiteit is niet meer actief. Hoewel de activiteit niet meer actief is, volgt het nog steeds de gebruiker via persistentie van de eVar. De gegevens zien er nu als volgt uit:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 3 | 10 | 2 | 3 |

De gebruiker komt terug op 1 maart en ziet een nieuwe activiteit, ABC. De gebruiker geeft ook vijf pagina&#39;s weer. Omdat activiteit XYZ de gebruiker door persistentie nog volgt, en deze gebruiker dan ABC heeft geplaatst, zullen wij twee lijnpunten in het melden zien:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 3 |
| ABC | 3 | 5 | 3 | 3 |

De gebruiker komt dan terug op 1 april, bekijkt nog vijf pagina&#39;s en koopt. De vervaldatum van 90 dagen van die eerste eVar-waarde wordt opnieuw ingesteld op 1 april. Dat zullen we in de rapportage zien. En alle activiteiten van het Doel de gebruiker ziet ontvangen het krediet voor de omzetting, maar het totale aantal omzettingen wordt gededupliceerd:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers | Orders |
|--- |--- |--- |--- |--- |--- |
| XYZ | 3 | 20 | 4 | 1 | 3 |
| ABC | 3 | 10 | 2 | 3 | 3 |
| Totaal | 2 | 20 | 3 | 3 | 3 |

Omdat beide ervaringen werden gezien vóór de conversie, krijgen ze allebei &#39;krediet&#39; voor de bestelling. Maar er vond slechts één orde plaats in het systeem en het totaal weerspiegelt dat. Voor [!DNL Target]-rapportage, omdat u geen [!DNL Target]-activiteit tegen een andere activiteit plaatst om te zien welke meer succes heeft, maakt het niet uit dat alle activiteiten die de gebruiker zag, krediet hebben gekregen. U vergelijkt de resultaten van twee items in één activiteit en het is voor een gebruiker niet mogelijk om verschillende ervaringen in dezelfde activiteit te zien, zodat u zich geen zorgen hoeft te maken over kruisbesmetting van orderkrediet.

Zie [Conversievariabelen (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) in de *Handleiding Analysebeheer* voor meer informatie.

## Waarom berekenen Analytics en Analytics voor Doel (A4T) aantallen voor de Unieke metrische bezoekers verschillend? {#section_0C3B648AB54041F9A2AA839D51791883}

Wanneer u een test A/B in werking stelt, die de Studenten t-test (betrouwbaarheidsmetrisch) gebruikt om een winnaar van een test te kiezen, één van de veronderstellingen is dat er een vaste tijdhorizon is. De test is alleen statistisch geldig als u naar die vaste steekproefgrootte kijkt.

De [!UICONTROL Unique Visitors] metrische waarde is verschillend in [!DNL Analytics] en [!DNL Target] slechts wanneer u een periode bekijkt die korter is dan de daadwerkelijke test. Als u de grootte van het monster niet hebt bereikt, is de test minder betrouwbaar. Zie [Een A/B-test niet uitvoeren](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) op [De website van Evan Miller](https://www.evanmiller.org/index.html) voor meer informatie.

De [!UICONTROL Unique Visitors]-meting geeft het aantal personen weer dat tijdens de opgegeven periode aan de test is blootgesteld en dat de site heeft bezocht. Deze mensen maken nog steeds deel uit van de test en moeten worden geteld. Als u slechts het aantal mensen wilt zien die tijdens één enkele week werden blootgesteld, kunt u een segment van bezoekers tot stand brengen die een activiteitenindruk hadden en het toepassen op het rapport.

U kunt de hoeveelheid tijd verkorten de [!DNL Target] variabele tot een zitting voortduurt; Dit is echter meestal problematisch voor tests waarbij de conversiegebeurtenis minder waarschijnlijk binnen dezelfde sessie plaatsvindt.

## Waarom wordt dezelfde bezoeker soms geteld in meerdere ervaringen in Analytics? {#section_1397E972D31C4207A142E4D2D6D794A2}

In de volgende lijst worden redenen beschreven waarom dezelfde bezoeker kan worden geteld in meerdere ervaringen in [!DNL Analytics]:

* Het [!DNL Target]-profiel is verlopen, maar het cookie [!DNL Analytics] is er nog steeds. In deze situatie herevalueert [!DNL Target] de gebruiker, maar [!DNL Analytics] beschouwt de bezoeker als dezelfde persoon.
* Als de bezoeker `mbox3rdPartyId` gebruikt, wanneer de anonieme bezoeker met zijn of haar profiel van de 3de-partijidentiteitskaart wordt samengevoegd, [!DNL Target] zou de bezoeker in een verschillende ervaring kunnen zetten om met 3de-partijidentiteitskaart aan te passen. Zie [Real-Time Profile Syncing voor mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732) voor meer informatie.
* [!DNL Analytics] Verschillende apparaten zoals dezelfde bezoeker kunnen op een andere manier worden bijgehouden dan deze apparaten  [!DNL Target] bijhoudt: De instellingen van de id van derden in  [!DNL Target] zijn anders dan in Analytics.

## Steunt A4T virtuele rapportseries?

Virtuele rapportsuites worden *niet* opgenomen in de [!UICONTROL Report Suite] lijst en het publiek van virtuele rapportsuites wordt niet gesteund in A4T rapportering.

## Kan ik het percentage van verkeerstoewijzing in een activiteit veranderen die A4T gebruikt nadat de activiteit is geactiveerd?

Het wijzigen van het percentage verkeerstoewijzing in een activiteit na activering kan leiden tot inconsistente rapportage in [!DNL Analytics] omdat de wijziging alleen van invloed is op nieuwe bezoekers. Terugkerende bezoekers worden niet beïnvloed.

Als beste praktijken, zou u de bestaande activiteit moeten tegenhouden en dan een nieuwe activiteit creëren in plaats van het percentage te veranderen na activering. De rapportage voor de nieuwe activiteit begint met nieuwe bezoekers en de gegevens van terugkerende bezoekers zullen geen inconsistente rapportage veroorzaken.

## Hoe worden bezoeken geteld in Analytics en omzettingskrediet toegewezen in een auto-Doelactiviteit die A4T gebruikt?

Wanneer een bezoeker in aanmerking komt voor conversie, inhoud weergeeft of in een A4T-activiteit converteert, verzendt [!DNL Target] gebeurtenisgegevens naar [!DNL Analytics], waardoor [!DNL Analytics] conversiegebeurtenissen en andere klikstreamgebeurtenissen die op de pagina plaatsvinden, kan toewijzen aan de relevante [!DNL Target]-activiteiten en -ervaringen.

Hier volgen enkele punten waarmee u rekening moet houden wanneer u [!DNL Analytics]-rapporten weergeeft:

* In het algemeen is het verstandig om uw rapportvenster te beginnen vanaf de begindatum van de activiteit.
* Als een omzetting buiten het venster van het rapport gebeurt, zal de omzetting niet in [!DNL Analytics] zichtbaar zijn.
* Wanneer in het &quot;gerichte&quot;gedeelte van verkeer voor [!UICONTROL Auto-Target] activiteiten, zouden de bezoekers verschillende ervaringen van één zitting aan volgende kunnen zien. Als hun profiel of context bijvoorbeeld is gewijzigd en de computerleeralgoritmen van [!DNL Target] besluiten dat deze eerder zullen worden omgezet in een nieuwe ervaring. Wanneer bezoekers van ervaring naar ervaring gaan, neemt het aantal bezoekers toe voor elke waargenomen ervaring. Dit is anders dan bij gewone A/B-testactiviteiten waarbij de ervaring bij bezoekers blijft hangen.
* Als een bezoeker meerdere ervaringen tijdens een bezoek ziet, wordt elke conversie altijd toegeschreven aan de laatste ervaring die de bezoeker heeft gezien. Zoals vermeld, neemt het aantal bezoeken toe voor elke ervaring die de bezoeker zag. Dit kan de omzettingssnelheden per-Ervaring kunstmatig drukken wanneer het bekijken van ervaringen onder de &quot;[!UICONTROL Targeted]&quot;dimensie in [!DNL Adobe Analytics] rapporten.
