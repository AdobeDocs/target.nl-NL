---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;rapport;rapporten;mening rapporten;rapportering;telmethode;impressies;bezoekers;standaard metrische;activiteitconversies;niet nader gespecificeerd
description: Zoek antwoorden op vragen die vaak worden gesteld over het weergeven van rapporten wanneer u Analytics gebruikt voor [!DNL Target] (A4T). Met A4T kunt u analytische rapporten gebruiken voor [!DNL Target] activiteiten.
title: Antwoorden op vragen over het bekijken van Rapporten met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '2507'
ht-degree: 1%

---

# Rapporten weergeven - Veelgestelde vragen voor A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over het bekijken van rapporten wanneer het gebruiken [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T).

## Kan ik mijn [!DNL Target] activiteitsgegevens in Analysis Workspace? {#workspace}

U kunt [!DNL Analysis Workspace] om uw [!DNL Target] activiteiten en ervaringen. De [Analyses voor venster Doel](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Hiermee kunt u optillen en vertrouwen zien voor maar liefst drie succesmetingen. U kunt ook dieper graven met behulp van tabellen en visualisaties.

Voor gedetailleerde informatie en voorbeelden opent u het dialoogvenster [Analyse en doel: Best practices voor zelfstudie Analyse](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), verstrekt door Adobe Experience League.

## Waar kunnen segmenten worden toegepast in Analysis Workspace? {#segmentation}

Segmenten worden meestal boven aan een deelvenster in de neerzetzone van segmenten gebruikt. Het segment wordt toegepast op alle tabellen en visualisaties in het deelvenster. Deze techniek is het meest nuttig om te zien hoe de test een subset mensen beïnvloedt (bijvoorbeeld hoe heeft deze test voor mensen in het Verenigd Koninkrijk gepresteerd).

Een segment kan ook rechtstreeks in de vrije-vormlijst worden gelaagd, maar merk op dat u het over de volledige lijst moet bedekken om de lift &amp; betrouwbaarheidsberekeningen binnen het Comité te bewaren A4T. Segmenten op kolomniveau worden momenteel niet ondersteund in het deelvenster.

## Wanneer ik een raaksegment voor een specifieke toepassing toepast [!DNL Target] activiteit , waarom worden er niet-verwante ervaringen geretourneerd ? {#activity-segmentation}

De [!DNL Target] variabele verzonden naar [!DNL Analytics] heeft een standaardvervalperiode van 90 dagen. (Opmerking: deze vervalperiode kan indien nodig door de klantenservice worden aangepast). Wanneer bezoekers door de site navigeren gedurende dit verloopvenster, maken ze deel uit van een groot aantal [!DNL Target] activiteiten, die allemaal in de dimensie worden verzameld.

Wanneer u voor een activiteit segmenteert om in een klap aanwezig te zijn, krijgt u alle ervaringen die deel van die activiteit uitmaken *plus* alle andere ervaringen die bij die treffer blijven opdoen.

## Waarom heb ik tijdens het configureren van mijn Goal Metrics geen toegang tot Geavanceerde instellingen?

Voor activiteiten die [!DNL Analytics] als rapporteringsbron (A4T), het doel metrisch gebruikt &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; en &quot;[!UICONTROL On Every Impression]&quot;. Deze instellingen zijn *niet* configureerbaar.

Voor meer informatie, zie &quot;terwijl het vormen van mijn doelmetriek, waarom kan ik niet tot de Geavanceerde opties van Montages toegang hebben?&quot; in [Metrische definities - Veelgestelde vragen A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Moet ik bezoekers, bezoeken, of activiteit impressies als mijn normaliserende metrisch (d.w.z. telmethode) gebruiken? {#metrics}

Er zijn verscheidene opties voor het normaliseren van metriek in A4T rapportering. Deze maatstaf, ook wel de telmethode genoemd, wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast.

* ***Unieke bezoekers*** Eenmaal verhogen wanneer een gebruiker voor het eerst in aanmerking komt voor een activiteit.
* ***Bezoeken*** verhoging voor elke zitting zodra een gebruiker (Unieke Bezoeker) een activiteit ingaat, zelfs als de activiteit niet in verdere bezoeken wordt bekeken.
* ***Activiteitenindrukkingen*** telkens wanneer de inhoud van de activiteit wordt gediend, wordt verhoogd. (Gemeten door [!DNL Target]).

Wanneer een bezoeker een pagina weergeeft die een activiteit bevat, wordt een variabele ingesteld voor die bezoeker die de naam van die activiteit bevat. Zie de gedetailleerde scenario&#39;s hieronder voor hoe elke telmethode vergelijkt.

Overweeg het volgende:

* De bovenstaande metriek activeert wanneer een gebruiker in aanmerking komt voor een activiteit en inhoud wordt geretourneerd door [!DNL Target]. Dit betekent niet noodzakelijk dat de gebruiker het aanbod zag. Als een activiteitenervaring onder de vouw is en de gebruiker niet onderaan de pagina scrolt, dan werd de aanbieding gediend door [!DNL Target] maar niet door de gebruiker gezien.
* [!UICONTROL Activity Impressions] (gemeten met [!DNL Target]) en [!UICONTROL Instances] (gemeten met [!DNL Analytics]) gelijk zijn, tenzij er meerdere mbox-aanroepen op dezelfde pagina in dezelfde activiteit plaatsvinden. Dit veroorzaakt meerdere [!UICONTROL Activity Impressions] , maar slechts één [!UICONTROL Instance].

Zie voor meer informatie [A4T-rapporten instellen in Analysis Workspace voor Auto-Target-activiteiten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.

## Waarom zijn &#39;activity impressions&#39; en &#39;activity conversions&#39; in Analysis Workspace hoger dan Reports &amp; Analytics? {#sametouch}

[!DNL Reports & Analytics] past een attribuutmodel met dezelfde aanraakinstelling toe op &#39;activity-impressions&#39; en &#39;activity-conversies&#39;, terwijl [!DNL Analysis Workspace] geeft de onbewerkte maatstaven weer, die kunnen worden opgeblazen als gevolg van de persistentie van de [!DNL Target] dimensie.

Om nauwkeurig te evalueren [!UICONTROL Activity Impressions] en [!UICONTROL Activity Conversions] maatstaven in [!DNL Analysis Workspace], zorgen ervoor dat beide meetwaarden [!UICONTROL Same Touch] toegepaste toewijzingsmodellen. U kunt modellen toepassen door op het tandwieltje voor kolominstellingen te klikken, zodat [!UICONTROL Non-default attribution models]en selecteert u vervolgens [!UICONTROL Same Touch]. Meer informatie over attributie in [Overzicht van IQ-kenmerken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) in de *Handleiding Analysehulpmiddelen*.

## Wat betekent de &quot;activiteitomzettingen&quot;als de teller een metrische Analyse tijdens activiteitenopstelling plukt? {#section_F3EBACF85AF846E9B366A549AAB64356}

&quot;Activiteitenomzettingen&quot; zijn leeg als een [!DNL Analytics] De metrische waarde is geselecteerd als de conversiemetrisch voor de activiteit.

## Waarom zie ik &quot;niet gespecificeerd&quot; in de analytische rapporten? Wat betekent het? {#unspecified}

In andere rapporten betekent &quot;niet gespecificeerd&quot; dat gegevens niet aan een classificatieregel voldeden, maar in A4T zou dit nooit mogen gebeuren. Als je &#39;unspecified&#39; ziet, dan is de classificatieservice nog niet gestart. Over het algemeen duurt het 24 tot 72 uur voordat gegevens over de activiteit in de rapporten worden weergegeven. Hoewel de activiteiten pas op dat moment in dit verslag worden vermeld, worden alle bezoekersgegevens die met deze activiteiten verband houden, vastgelegd en weergegeven wanneer de classificatie is voltooid.

Na de indelingsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

Voor het geval dat de classificatie voor die activiteit werd gedaan, en u nog een &quot;Niet gespecificeerde&quot;rij in het rapport ziet, zorg ervoor dat het rapport geen niet gebruikt[!DNL Target] metrisch om de gegevens te tonen. Tenzij het rapport een [!DNL Target]-specific metrisch, dat de &quot;Niet gespecificeerde&quot;rij gebeurtenissen voor vraag bevat die niet met worden geassocieerd [!DNL Target]. Die rij bevat geen [!DNL Target]-gerelateerde informatie (bijvoorbeeld bezoekers/bezoeken/indrukken).

## Waarom? [!DNL Target] metriek die naar Analytics wordt verzonden zelfs nadat de activiteit is gedeactiveerd? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

De [!DNL Target] variabele verzonden naar [!DNL Analytics] heeft een standaardvervalperiode van 90 dagen. Deze vervalperiode kan indien nodig door de klantenservice worden aangepast. Deze instelling is echter algemeen voor alle activiteiten, zodat ze niet voor één geval hoeft te worden aangepast.

Misschien ziet u [!DNL Target] variabelen verzonden naar [!DNL Analytics] na de vervalperiode omdat de vervaldatum 90 dagen is, maar alleen als die gebruiker geen andere A4T-modus ziet [!DNL Target] activiteit. Als een gebruiker op dag 45 terugkomt naar de site en een andere activiteit ziet, wordt de teller van de hele A4T-eVar opnieuw ingesteld op 90 dagen. Dat betekent dat de eerste campagne vanaf dag 1 nu tot 45 + 90 = 135 dagen zou kunnen duren. Als de gebruiker blijft terugkomen, zou u aan het punt kunnen komen waar u metriek wordt verzonden naar [!DNL Analytics] in uw rapportering uit veel oudere activiteiten. Wanneer gebruikers cookies verwijderen en niet terugkeren naar de site, nemen de nummers in die activiteit af, maar kunt u ze wel zien.

Dit betekent dat de activiteiten paginaweergaven, bezoeken, enzovoort blijven krijgen, tot 90 dagen nadat de activiteit eindigt voor bezoekers die deel uitmaakten van de activiteit terwijl deze actief was. Als u echter kijkt naar de [!UICONTROL Activity Impressions] metrisch, zou u geen beelden moeten zien nadat de activiteit beëindigde.

Dit is normaal en verwacht gedrag. De variabele A4T werkt net als elke andere eVar. De waarde wordt aan de gebruiker gekoppeld totdat deze de verlooptijdperiode (90 dagen) bereikt. Als een activiteit dus slechts twee weken actief is, wordt de waarde nog steeds geassocieerd met de gebruiker gedurende ten minste de volgende 90 dagen.

De beste praktijken zijn meningsrapporten voor die activiteit slechts voor de periode dat de activiteit levend was. De datums moeten standaard correct worden ingesteld wanneer u de activiteit in [!DNL Analytics], dus tenzij u de datum handmatig hebt verlengd, dient dit vanuit een rapportagerefase geen probleem te zijn.

Laten we er bijvoorbeeld van uitgaan dat de variabele A4T na 90 dagen vervalt en dat de test van 1 januari tot en met 15 januari actief is.

Op 1 januari komt de gebruiker naar de site en ziet activiteit XYZ eenmaal en heeft daarna vijf paginaweergaven. In de komende twee weken keert de gebruiker nooit terug naar de site. De gegevens zien er voor deze gebruiker als volgt uit:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

De gebruiker keert op 1 Februari terug, bekijkt vijf meer pagina&#39;s, en ontmoet geen meer activiteiten van het Doel en de originele activiteit is niet meer actief. Hoewel de activiteit niet meer actief is, volgt het nog steeds de gebruiker via persistentie van de eVar. De gegevens zien er nu als volgt uit:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

De gebruiker komt terug op 1 maart en ziet een nieuwe activiteit, ABC. De gebruiker geeft ook vijf pagina&#39;s weer. Omdat de activiteit XYZ nog de gebruiker door persistentie volgt, en deze gebruiker dan ABC reeks heeft, zult u twee lijnpunten in het melden zien:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

De gebruiker komt dan terug op 1 april, bekijkt nog vijf pagina&#39;s en koopt. De vervaldatum van 90 dagen van die eerste eVar wordt opnieuw ingesteld op 1 april, zodat u dat ziet in de rapportage. En alle activiteiten van het Doel de gebruiker ziet ontvangen het krediet voor de omzetting, maar het totale aantal omzettingen wordt gededupliceerd:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers | Orders |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Totaal | 2 | 20 | 3 | 1 | 1 |

Omdat beide ervaringen werden gezien vóór de conversie, krijgen ze allebei &#39;krediet&#39; voor de bestelling. Maar er vond slechts één orde plaats in het systeem en het totaal weerspiegelt dat. Voor [!DNL Target] rapporteren, omdat u geen [!DNL Target] Als u een andere activiteit wilt gebruiken om te zien wat beter werkt, maakt het niet uit dat alle activiteiten die de gebruiker zag, krediet hebben gekregen. U vergelijkt de resultaten van twee items in één activiteit. Het is voor een gebruiker niet mogelijk om verschillende ervaringen in dezelfde activiteit te zien zodat u zich geen zorgen hoeft te maken over kruisbesmetting van orderkrediet.

Zie voor meer informatie [Conversievariabelen (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) in de *Handleiding Analysebeheer*.

## Waarom zie ik nog meer indrukken nadat mijn activiteit is gedeactiveerd? {#deactivated}

Een bron van beelden aan het rapport van een activiteit A4T na deactivatie kan verkeer QA-wijze zijn. Het doel registreert normaal geen gebeurtenissen voor een gedeactiveerde activiteit, maar de Analyse heeft geen manier om te weten dat de impressies uit wijze QA komen. Wanneer het de activiteitenrapport van het Doel van Analytics wordt teruggewonnen, toont het deze beelden. Dit werkt zoals ontworpen omdat de klanten een manier nodig hebben om A4T rapporten te controleren zelfs als de activiteit niet actief gebruikend wijze QA is.

## Waarom berekenen Analytics en Analytics voor Adobe Target (A4T) aantallen voor de Unieke metrische bezoekers verschillend? {#section_0C3B648AB54041F9A2AA839D51791883}

Wanneer u een test A/B in werking stelt, die de Studenten t-test (betrouwbaarheidsmetrisch) gebruikt om een winnaar van een test te kiezen, één van de veronderstellingen is dat er een vaste tijdhorizon is. De test is alleen statistisch geldig als u naar die vaste steekproefgrootte kijkt.

De [!UICONTROL Unique Visitors] De metrische waarde is anders in [!DNL Analytics] en [!DNL Target] alleen als u een periode bekijkt die korter is dan de werkelijke test. Als u de grootte van het monster niet hebt bereikt, is de test minder betrouwbaar. Zie [Een A/B-test niet uitvoeren](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) op [De website van Evan Miller](https://www.evanmiller.org/index.html) voor meer informatie .

De [!UICONTROL Unique Visitors] In de metrische code wordt het aantal personen weergegeven dat tijdens de opgegeven periode aan de test is blootgesteld en dat de site heeft bezocht. Deze mensen maken deel uit van de test en moeten worden geteld. Als u slechts het aantal mensen wilt zien die tijdens één enkele week werden blootgesteld, kunt u een segment van bezoekers tot stand brengen die een activiteitenindruk hadden en het toepassen op het rapport.

U kunt de hoeveelheid tijd verkorten [!DNL Target] de variabele blijft tot een zitting voortbestaan; Dit is echter problematisch voor tests waarbij de conversiegebeurtenis minder waarschijnlijk binnen dezelfde sessie plaatsvindt.

## Waarom wordt dezelfde bezoeker soms geteld in meerdere ervaringen in Analytics? {#section_1397E972D31C4207A142E4D2D6D794A2}

In de volgende lijst worden de redenen uitgelegd waarom dezelfde bezoeker in meerdere ervaringen kan worden meegeteld in [!DNL Analytics]:

* De [!DNL Target] het profiel is verlopen maar [!DNL Analytics] cookie is er nog steeds. In deze situatie [!DNL Target] herevalueert de gebruiker maar [!DNL Analytics] beschouwt de bezoeker als dezelfde persoon.
* Als de bezoeker de `mbox3rdPartyId`, wanneer de anonieme bezoeker wordt samengevoegd met het profiel van de derde-partijidentiteitskaart, [!DNL Target] kan de bezoeker in een andere ervaring plaatsen om overeen te komen met de id van een derde. Zie voor meer informatie [Real-time profielsynchronisatie voor mbox3rdPartyID](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] verschillende apparaten zoals dezelfde bezoeker mogelijk op een andere manier bijhouden dan [!DNL Target] volgt deze apparaten: de installatie van de id van derden in [!DNL Target] is anders dan in Analytics.

## Steunt A4T virtuele rapportseries? {#virtual}

Hoewel de virtuele rapportsuites niet inbegrepen in [!UICONTROL Report Suite] lijst, om het even welke gegevens A4T die met een rapportreeks worden gedeeld die met een virtuele rapportreeks in wordt verbonden [!DNL Analytics] heeft toegang tot die gegevens. Merk op dat om het even welk publiek dat van een virtuele rapportreeksen wordt gecreeerd niet kan worden gedeeld terug naar [!DNL Target].

## Kan ik het percentage van verkeerstoewijzing in een activiteit veranderen die A4T gebruikt nadat de activiteit is geactiveerd?

Het wijzigen van het percentage van de verkeerstoewijzing in een activiteit na activering kan leiden tot inconsistente rapportage in [!DNL Analytics] omdat de wijziging alleen van invloed is op nieuwe bezoekers . Terugkerende bezoekers worden niet beïnvloed.

Als beste praktijken, zou u de bestaande activiteit moeten tegenhouden en dan een nieuwe activiteit creëren in plaats van het percentage te veranderen na activering. De rapportage voor de nieuwe activiteit begint met nieuwe bezoekers en de gegevens van terugkerende bezoekers veroorzaken geen inconsistente rapportage.

## Hoe worden bezoeken geteld in Analytics en omzettingskrediet toegewezen in een auto-Doelactiviteit die A4T gebruikt?

Wanneer een bezoeker in aanmerking komt voor een A4T-activiteit, de inhoud weergeeft of omzet, [!DNL Target] verzendt gebeurtenisgegevens naar [!DNL Analytics]. Deze gebeurtenisgegevens staan [!DNL Analytics] om conversiegebeurtenissen en andere klikstreamgebeurtenissen die op de pagina plaatsvinden, toe te schrijven aan de relevante [!DNL Target] activiteiten en ervaringen.

Hier enkele punten waarmee u rekening kunt houden bij het weergeven [!DNL Analytics] rapporten:

* In het algemeen is het verstandig om uw rapportvenster te beginnen vanaf de begindatum van de activiteit.
* Als een omzetting buiten het venster van het rapport gebeurt, is de omzetting niet zichtbaar in [!DNL Analytics].
* Wanneer in het &quot;gerichte&quot;gedeelte van verkeer voor [!UICONTROL Auto-Target] bezoekers kunnen verschillende ervaringen zien van de ene sessie tot de volgende . Als bijvoorbeeld hun profiel of context is gewijzigd en [!DNL Target]De computerleeralgoritmen bepalen dat de kans groter is dat ze op een nieuwe ervaring worden omgezet. Wanneer bezoekers van ervaring naar ervaring gaan, neemt het aantal bezoekers toe voor elke waargenomen ervaring. Dit is anders dan bij gewone A/B-testactiviteiten waarbij de ervaring bij bezoekers blijft hangen.
* Als een bezoeker meerdere ervaringen tijdens een bezoek ziet, wordt elke conversie altijd toegeschreven aan de laatste ervaring die de bezoeker heeft gezien. Zoals vermeld, neemt het aantal bezoeken toe voor elke ervaring die de bezoeker zag. Dit kan de conversiesnelheden per ervaring kunstmatig verlagen bij het bekijken van ervaringen onder &quot;[!UICONTROL Targeted]&quot; dimensie in [!DNL Adobe Analytics] rapporten.
