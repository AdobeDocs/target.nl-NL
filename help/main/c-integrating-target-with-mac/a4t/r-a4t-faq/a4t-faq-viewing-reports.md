---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;rapport;rapporten;mening rapporten;rapportering;telmethode;impressies;bezoekers;standaard metrische;activiteitconversies;niet nader gespecificeerd
description: Vind antwoorden op vragen die vaak over het bekijken van rapporten wanneer het gebruiken van Analytics voor  [!DNL Target]  (A4T) worden gevraagd. A4T laat u Analytics gebruiken die voor  [!DNL Target]  activiteiten rapporteert.
title: Antwoorden op vragen over het bekijken van Rapporten met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: c747a8a0ed480130f254818e21b98addca16ca41
workflow-type: tm+mt
source-wordcount: '2539'
ht-degree: 1%

---

# Rapporten weergeven - Veelgestelde vragen voor A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over het weergeven van rapporten wanneer [!DNL Adobe Analytics] wordt gebruikt als rapportagebron voor [!DNL Adobe Target] (A4T).

## Kan ik mijn [!DNL Target] activiteitsgegevens weergeven in [!DNL Analysis Workspace] ? {#workspace}

+++Antwoord
Met [!DNL Analysis Workspace] kunt u uw [!DNL Target] -activiteiten en -ervaringen analyseren. De [&#x200B; Analytics voor het paneel van het Doel &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=nl-NL) laat u optillen &amp; vertrouwen voor maximaal drie succesmetriek zien. U kunt ook dieper graven met behulp van tabellen en visualisaties.

Voor gedetailleerde informatie en voorbeelden, open [&#x200B; Analytics &amp; Doel: Beste praktijken voor het leerprogramma van de Analyse &#x200B;](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), dat door [!UICONTROL Adobe Experience League] wordt verstrekt.

+++

## Waar kunnen segmenten worden toegepast in [!DNL Analysis Workspace] ? {#segmentation}

+++Antwoord
Segmenten worden meestal boven aan een deelvenster in de neerzetzone van segmenten gebruikt. Het segment wordt toegepast op alle tabellen en visualisaties in het deelvenster. Deze techniek is het meest nuttig om te zien hoe de test een subset mensen beïnvloedt (bijvoorbeeld hoe heeft deze test voor mensen in het Verenigd Koninkrijk gepresteerd).

Een segment kan ook rechtstreeks in de vrije-vormlijst worden gelaagd, maar merk op dat u het over de volledige lijst moet bedekken om de lift &amp; betrouwbaarheidsberekeningen binnen het Comité te bewaren A4T. Segmenten op kolomniveau worden momenteel niet ondersteund in het deelvenster.

+++

## Welk Attribution IQ-model wordt gebruikt in [!DNL Analysis Workspace]?

+++Antwoord
Als u [!DNL Target] activity-impressies en conversies gebruikt in [!DNL Analysis Workspace] , is het Attribution IQ-model &quot;Same Touch&quot; het standaardmodel dat op de meetgegevens wordt toegepast om een nauwkeurige telling te garanderen. Dit model werkt in 99% van de gevallen goed. U kunt deze standaardtoewijzing echter overschrijven in Attribution IQ.

+++

## Wanneer ik een raaksegment toepast voor een specifieke [!DNL Target] -activiteit, waarom worden dan verwante ervaringen geretourneerd? {#activity-segmentation}

+++Antwoord
De variabele [!DNL Target] die naar [!DNL Analytics] wordt verzonden, heeft een standaardvervalperiode van 90 dagen. (Opmerking: deze vervalperiode kan indien nodig door de klantenservice worden aangepast.) Wanneer bezoekers door de site navigeren gedurende dit verloopvenster, maken ze deel uit van veel [!DNL Target] -activiteiten, die allemaal in de dimensie worden verzameld.

Wanneer u voor een activiteit segmenteert om in een klap aanwezig te zijn, krijgt u alle ervaringen die deel van die activiteit *plus* uitmaken om het even welke andere ervaringen die op die klap voortbestaan.

+++

## Waarom heb ik tijdens het configureren van mijn [!UICONTROL Goal Metrics] geen toegang tot [!UICONTROL Advanced Settings] ?

+++Antwoord
Voor activiteiten die [!DNL Analytics] als rapporteringsbron (A4T) gebruiken, metrische doel gebruikt &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;en &quot;[!UICONTROL On Every Impression]&quot;montages. Deze montages zijn *niet* configureerbaar.

Voor meer informatie, zie &quot;terwijl het vormen van mijn doelmetriek, waarom kan ik niet tot de Geavanceerde opties van Montages toegang hebben?&quot; in [&#x200B; Metrische definities - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Moet ik bezoekers, bezoeken, of activiteit impressies als mijn normaliserende metrisch (d.w.z. telmethode) gebruiken? {#metrics}

+++Antwoord
Er zijn verscheidene opties voor het normaliseren van metriek in A4T rapportering. Deze maatstaf, ook wel de telmethode genoemd, wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast.

* ***Unieke bezoekers*** toename eens wanneer een gebruiker voor het eerst voor een activiteit kwalificeert.
* ***bezoeken*** verhoging voor elke zitting zodra een gebruiker (Unieke Bezoeker) een activiteit ingaat, zelfs als de activiteit niet in verdere bezoeken wordt bekeken.
* ***de impressies van de Activiteit*** toename telkens als de activiteiteninhoud wordt gediend. (Gemeten door [!DNL Target]).

Wanneer een bezoeker een pagina weergeeft die een activiteit bevat, wordt een variabele ingesteld voor die bezoeker die de naam van die activiteit bevat. Zie de gedetailleerde scenario&#39;s hieronder voor hoe elke telmethode vergelijkt.

Overweeg het volgende:

* De bovenstaande metrische trigger wanneer een gebruiker in aanmerking komt voor een activiteit en inhoud wordt geretourneerd vanuit [!DNL Target] . Dit betekent niet noodzakelijk dat de gebruiker het aanbod zag. Als een activiteit onder de vouw is en de gebruiker niet onderaan de pagina scrolt, dan werd de aanbieding gediend door [!DNL Target] maar niet door de gebruiker gezien.
* [!UICONTROL Activity Impressions] (gemeten door [!DNL Target]) en [!UICONTROL Instances] (gemeten door [!DNL Analytics]) zijn gelijk, tenzij er meerdere mbox-aanroepen op dezelfde pagina plaatsvinden in dezelfde activiteit. Hierdoor worden meerdere [!UICONTROL Activity Impressions] geteld, maar slechts één [!UICONTROL Instance] .

Voor meer informatie, zie [&#x200B; hoe te opstelling A4T rapporten in Analysis Workspace voor activiteiten Auto-Doel &#x200B;](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=nl-NL) in *Zelfstudies van Adobe Target*.

+++

## Waarom zijn &#39;activity impressions&#39; en &#39;activity conversions&#39; hoger in [!DNL Analysis Workspace] dan in [!UICONTROL Reports & Analytics] ? {#sametouch}

+++Antwoord
[!DNL Reports & Analytics] past een attributiemodel met dezelfde aanraakinstelling toe op &#39;activity-impressions&#39; en &#39;activity-conversies&#39;, terwijl [!DNL Analysis Workspace] de onbewerkte metriek weergeeft, die opgeblazen kan lijken vanwege de persistentie van de [!DNL Target] -dimensie.

Als u nauwkeurige [!UICONTROL Activity Impressions] - en [!UICONTROL Activity Conversions] metriek in [!DNL Analysis Workspace] wilt evalueren, moet u ervoor zorgen dat op beide metriek [!UICONTROL Same Touch] -attributiemodellen zijn toegepast. Modellen kunnen worden toegepast door op het tandwieltje voor kolominstellingen te klikken, [!UICONTROL Non-default attribution models] in te schakelen en vervolgens [!UICONTROL Same Touch] te selecteren. Leer meer over attributie in [&#x200B; overzicht van Attributen IQ &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html?lang=nl-NL) in de *Gids van Hulpmiddelen van de Analyse*.

+++

## Wat betekent &quot;activiteitconversies&quot; als de markeerteken een [!DNL Analytics] metrische waarde tijdens het instellen van de activiteit kiest? {#section_F3EBACF85AF846E9B366A549AAB64356}

+++Antwoord
&quot;Activiteitsomzettingen&quot; zijn leeg als een [!DNL Analytics] metrische waarde is geselecteerd als de omzettingsmetrische waarde voor de activiteit.

+++

## Waarom zie ik &quot;unspecified&quot; in de [!DNL Analytics] rapporten? Wat betekent het? {#unspecified}

+++Antwoord
In andere rapporten betekent &quot;niet gespecificeerd&quot; dat gegevens niet aan een classificatieregel voldeden, maar in A4T zou dit nooit mogen gebeuren. Als je &#39;unspecified&#39; ziet, dan is de classificatieservice nog niet gestart. Over het algemeen duurt het 24 tot 72 uur voordat gegevens over de activiteit in de rapporten worden weergegeven. Hoewel de activiteiten pas op dat moment in dit verslag worden vermeld, worden alle bezoekersgegevens die met deze activiteiten verband houden, vastgelegd en weergegeven wanneer de classificatie is voltooid.

Na de rubriceringsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

In het geval dat de classificatie voor die activiteit werd gedaan, en u nog een &quot;Niet gespecificeerde&quot;rij in het rapport ziet, zorg ervoor dat het rapport geen niet [!DNL Target] metrisch gebruikt om de gegevens te tonen. Tenzij het rapport een [!DNL Target]-specifieke metrische rij gebruikt, bevat die rij &quot;Niet opgegeven&quot; gebeurtenissen voor aanroepen die niet aan [!DNL Target] zijn gekoppeld. Die rij bevat geen aan [!DNL Target] gekoppelde informatie (bijvoorbeeld bezoekers/bezoeken/afdrukken).

+++

## Waarom worden [!DNL Target] metriek verzonden naar [!DNL Analytics] zelfs nadat de activiteit is gedeactiveerd? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

+++Antwoord
De variabele [!DNL Target] die naar [!DNL Analytics] wordt verzonden, heeft een standaardvervalperiode van 90 dagen. Deze vervalperiode kan indien nodig door de klantenservice worden aangepast. Deze instelling is algemeen voor alle activiteiten, maar moet daarom niet voor één geval worden aangepast.

U ziet mogelijk [!DNL Target] variabelen die naar [!DNL Analytics] worden verzonden na de vervalperiode omdat de vervaldatum 90 dagen is, maar alleen als die gebruiker geen andere A4T-ingeschakelde [!DNL Target] activiteit ziet. Als een gebruiker op dag 45 terugkomt naar de site en een andere activiteit ziet, wordt de hele eVar-waarde van A4T opnieuw ingesteld op 90 dagen. Dat betekent dat de eerste campagne vanaf dag 1 nu tot 45 + 90 = 135 dagen zou kunnen duren. Als de gebruiker blijft terugkomen, zou u aan het punt kunnen komen waar u metriek die naar [!DNL Analytics] in uw rapportering van veel oudere activiteiten wordt verzonden. Wanneer gebruikers cookies verwijderen en niet terugkeren naar de site, nemen de nummers in die activiteit af, maar kunt u ze wel zien.

Dit betekent dat de activiteiten paginaweergaven, bezoeken, enzovoort blijven krijgen, tot 90 dagen nadat de activiteit eindigt voor bezoekers die deel uitmaakten van de activiteit terwijl deze actief was. Als u echter naar de metrische waarde van [!UICONTROL Activity Impressions] kijkt, ziet u geen indrukken meer nadat de activiteit is beëindigd.

Dit is normaal en verwacht gedrag. De variabele A4T werkt net als elke andere eVar. De waarde wordt aan de gebruiker gekoppeld totdat deze de verlooptijdperiode (90 dagen) bereikt. Als een activiteit dus slechts twee weken actief is, wordt de waarde nog steeds geassocieerd met de gebruiker gedurende ten minste de volgende 90 dagen.

De beste praktijken zijn meningsrapporten voor die activiteit slechts voor de periode dat de activiteit levend was. De datums moeten standaard correct worden ingesteld wanneer u de activiteit in [!DNL Analytics] bekijkt. Tenzij u de datum handmatig hebt verlengd, moet dit dus geen kwestie zijn vanuit rapportoogpunt.

Als voorbeeld, veronderstellen wij dat de variabele A4T na 90 dagen verloopt en de test van 1 Januari door 15 Januari actief is.

Op 1 januari komt de gebruiker naar de site en ziet activiteit XYZ eenmaal en heeft daarna vijf paginaweergaven. In de komende twee weken keert de gebruiker nooit terug naar de site. De gegevens zien er voor deze gebruiker als volgt uit:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

De gebruiker keert op 1 Februari terug, bekijkt vijf meer pagina&#39;s, en ontmoet geen meer activiteiten van het Doel en de originele activiteit is niet meer actief. Hoewel de activiteit niet meer actief is, volgt deze nog steeds de gebruiker via eVar persistentie. De gegevens zien er nu als volgt uit:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

De gebruiker komt terug op 1 maart en ziet een nieuwe activiteit, ABC. De gebruiker geeft ook vijf pagina&#39;s weer. Omdat de activiteit XYZ nog de gebruiker door persistentie volgt, en deze gebruiker dan ABC reeks heeft, zult u twee lijnpunten in het melden zien:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

De gebruiker komt dan terug op 1 april, bekijkt nog vijf pagina&#39;s en koopt. De vervaldatum van 90 dagen van die eerste eVar-waarde wordt opnieuw ingesteld op 1 april. Dat zie je in de rapportage. En alle activiteiten van het Doel de gebruiker ziet ontvangen het krediet voor de omzetting, maar het totale aantal omzettingen wordt gededupliceerd:

| Naam activiteit | Instanties (impressies) | Paginaweergaven | Bezoeken | Unieke bezoekers | Orders |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Totaal | 2 | 20 | 3 | 1 | 1 |

Omdat beide ervaringen werden gezien vóór de conversie, krijgen ze allebei &#39;krediet&#39; voor de bestelling. Maar er vond slechts één orde plaats in het systeem en het totaal weerspiegelt dat. Voor [!DNL Target] -rapportage, omdat u een [!DNL Target] -activiteit niet tegen een andere activiteit plaatst om te zien welke meer succes heeft, maakt het niet uit dat alle activiteiten die de gebruiker zag, krediet hebben gekregen. U vergelijkt de resultaten van twee items binnen één activiteit. Het is niet mogelijk voor een gebruiker om verschillende ervaringen in de zelfde activiteit te zien zodat moet u zich niet over kruisbesmetting van orderkrediet ongerust maken.

Voor meer informatie, zie [&#x200B; Variabelen van de Omzetting (eVar &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html?lang=nl-NL)) in de *Gids Admin van Analytics*.

+++

## Waarom zie ik nog meer indrukken nadat mijn activiteit is gedeactiveerd? {#deactivated}

+++Antwoord
Een bron van beelden aan het rapport van een activiteit A4T na deactivatie kan verkeer QA-wijze zijn. Het doel registreert normaal geen gebeurtenissen voor een gedeactiveerde activiteit, maar de Analyse heeft geen manier om te weten dat de impressies uit wijze QA komen. Wanneer het de activiteitenrapport van het Doel van Analytics wordt teruggewonnen, toont het deze beelden. Dit werkt zoals ontworpen omdat de klanten een manier nodig hebben om A4T rapporten te controleren zelfs als de activiteit niet actief gebruikend wijze QA is.

+++

## Waarom berekenen [!DNL Analytics] en [!UICONTROL Analytics for Adobe Target] (A4T) getallen voor de [!UICONTROL Unique Visitors] metrische waarde verschillend? {#section_0C3B648AB54041F9A2AA839D51791883}

+++Antwoord
Wanneer u een test A/B in werking stelt, die t-test van het [&#x200B; Welch &#x200B;](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} (het vertrouwen metrisch) gebruikt om een winnaar van een test te kiezen, is één van de veronderstellingen dat er een vaste tijdhorizon is. De test is niet statistisch geldig tenzij u die vaste steekproefgrootte bekijkt.

De [!UICONTROL Unique Visitors] -metrische waarde verschilt alleen in [!DNL Analytics] en [!DNL Target] als u naar een periode kijkt die korter is dan de werkelijke test. Als u uw steekproefgrootte niet hebt bereikt, is de test niet zo betrouwbaar. Zie [&#x200B; hoe niet om een Test A/B &#x200B;](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) op [&#x200B; Evan Miller&#39;s website &#x200B;](https://www.evanmiller.org/index.html) voor meer informatie in werking te stellen.

De [!UICONTROL Unique Visitors] -meting geeft het aantal personen weer dat tijdens de opgegeven periode aan de test is blootgesteld en dat de site heeft bezocht. Deze mensen maken deel uit van de test en moeten worden geteld. Als u slechts het aantal mensen wilt zien die tijdens één enkele week werden blootgesteld, kunt u een segment van bezoekers tot stand brengen die een activiteitenindruk hadden en het toepassen op het rapport.

U kunt de hoeveelheid tijd verkorten die de [!DNL Target] variabele tot een zitting voortduurt; nochtans, is dat problematisch voor tests waar de conversiegebeurtenis niet zo waarschijnlijk binnen de zelfde zitting zal gebeuren.

+++

## Waarom wordt dezelfde bezoeker soms meegeteld in meerdere ervaringen in [!DNL Analytics] ? {#section_1397E972D31C4207A142E4D2D6D794A2}

+++Antwoord
In de volgende lijst worden de redenen beschreven waarom dezelfde bezoeker kan worden geteld in meerdere ervaringen in [!DNL Analytics] :

* Het [!DNL Target] -profiel is verlopen, maar het [!DNL Analytics] -cookie is er nog steeds. In deze situatie herevalueert [!DNL Target] de gebruiker, maar [!DNL Analytics] beschouwt de bezoeker als dezelfde persoon.
* Als de bezoeker de `mbox3rdPartyId` gebruikt en de anonieme bezoeker wordt samengevoegd met het profiel voor de id van derden, kan [!DNL Target] de bezoeker in een andere ervaring plaatsen om overeen te komen met de id van derden. Voor meer informatie, zie [&#x200B; Real-Time Profiel die voor mbox3rdPartyID &#x200B;](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732) synchroniseert.
* [!DNL Analytics] volgt mogelijk verschillende apparaten op een andere manier als dezelfde bezoeker dan [!DNL Target] deze apparaten bijhoudt: de instellingen voor de id van derden in [!DNL Target] verschillen van die in Analytics.

+++

## Steunt A4T virtuele rapportseries? {#virtual}

+++Antwoord
Hoewel virtuele rapportsets niet in de lijst [!UICONTROL Report Suite] worden opgenomen, hebben alle A4T-gegevens die worden gedeeld met een rapportsuite die is gekoppeld aan een virtuele rapportsuite in [!DNL Analytics] toegang tot die gegevens. Merk op dat om het even welk publiek dat van een virtuele rapportreeksen wordt gecreeerd niet kan worden gedeeld terug naar [!DNL Target].

+++

## Kan ik het percentage van verkeerstoewijzing in een activiteit veranderen die A4T gebruikt nadat de activiteit is geactiveerd?

+++Antwoord
Het wijzigen van het percentage verkeerstoewijzing in een activiteit na activering kan leiden tot inconsistente rapportage in [!DNL Analytics] omdat de wijziging alleen van invloed is op nieuwe bezoekers. Terugkerende bezoekers worden niet beïnvloed.

Als beste praktijken, zou u de bestaande activiteit moeten tegenhouden en dan een nieuwe activiteit creëren in plaats van het percentage te veranderen na activering. De rapportage voor de nieuwe activiteit begint met nieuwe bezoekers en de gegevens van terugkerende bezoekers veroorzaken geen inconsistente rapportage.

+++

## Hoe worden bezoeken geteld in [!DNL Analytics] en conversiekrediet toegewezen aan een [!UICONTROL Auto-Target] -activiteit die A4T gebruikt?

+++Antwoord
Wanneer een bezoeker in aanmerking komt voor, de inhoud weergeeft of in een A4T-activiteit converteert, verzendt [!DNL Target] gebeurtenisgegevens naar [!DNL Analytics] . Met deze gebeurtenisgegevens kan [!DNL Analytics] conversiegebeurtenissen en andere klikstreamgebeurtenissen die op de pagina plaatsvinden, toewijzen aan de relevante [!DNL Target] -activiteiten en -ervaringen.

Hier volgen enkele punten waarmee u rekening moet houden bij het weergeven van [!DNL Analytics] -rapporten:

* In het algemeen is het verstandig om uw rapportagevenster te laten beginnen vanaf de begindatum van de activiteit.
* Als een conversie buiten het rapportvenster plaatsvindt, is de conversie niet zichtbaar in [!DNL Analytics] .
* In het &#39;beoogde&#39; gedeelte van het verkeer voor [!UICONTROL Auto-Target] -activiteiten zien bezoekers mogelijk verschillende ervaringen van de ene sessie tot de volgende. Als hun profiel of context bijvoorbeeld is gewijzigd en de machinaal leeralgoritmen van [!DNL Target] beslissen dat ze eerder zullen converteren voor een nieuwe ervaring. Wanneer bezoekers van ervaring naar ervaring gaan, neemt het aantal bezoekers toe voor elke waargenomen ervaring. Dit is anders dan bij gewone A/B-testactiviteiten waarbij de ervaring bij bezoekers blijft hangen.
* Als een bezoeker meerdere ervaringen tijdens een bezoek ziet, wordt elke conversie altijd toegeschreven aan de laatste ervaring die de bezoeker heeft gezien. Zoals vermeld, neemt het aantal bezoeken toe voor elke ervaring die de bezoeker zag. Dit kan de conversiesnelheden per ervaring kunstmatig verlagen wanneer u ervaringen bekijkt onder de dimensie &quot;[!UICONTROL Targeted]&quot; in [!DNL Adobe Analytics] -rapporten.

+++

## Hoe kan ik bij gebruik van [!DNL Analysis Workspace] (A4T) activiteitsindrukkingen in [!UICONTROL Analytics for Target] bijhouden? {#activity-impressions}

+++Antwoord

Activiteitenafbeeldingen weergeven in [!DNL Analysis Workspace] :

1. Klik in de gebruikersinterface van [!DNL Target] op **[!UICONTROL View in Analytics]** .
1. Voeg de **[!UICONTROL Activity Impressions]** kolom aan het [[!DNL Analytics Workspace] &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=nl-NL){target=_blank} rapport toe.
1. Klik in de kolom **[!UICONTROL Activity Impressions]** op het pictogram [!UICONTROL Gear] .
1. Klik op **[!UICONTROL Use non-default attribution model]**.
1. Selecteer **[!UICONTROL Same Touch Model]** > **[!UICONTROL Apply]** .

+++
